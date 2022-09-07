---
created: 2022-09-07T10:48:29 (UTC +10:00)
tags: []
source: https://www.atlassian.com/git/tutorials/dotfiles
author: Atlassian
---

# How to store dotfiles | Atlassian Git Tutorial

> ## Excerpt
> Learn how to store your dotfiles using a bare Git repository. You can easily get started using the code snippets in this step-by-step tutorial.

---
## The best way to store your dotfiles: A bare Git repository

_Disclaimer: the title is slightly hyperbolic, there are other proven solutions to the problem. I do think the technique below is very elegant though._

Recently I read about this amazing technique in an [Hacker News thread][1] on people's solutions to store their [dotfiles][2]. User `StreakyCobra` [showed his elegant setup][3] and ... It made so much sense! I am in the process of switching my own system to the same technique. The only pre-requisite is to install [Git][4].

In his words the technique below requires:

No extra tooling, no symlinks, files are tracked on a version control system, you can use different branches for different computers, you can replicate you configuration easily on new installation.

The technique consists in storing a [Git bare repository][5] in a "_side_" folder (like `$HOME/.cfg` or `$HOME/.myconfig`) using a specially crafted alias so that commands are run against that repository and not the usual `.git` local folder, which would interfere with any other Git repositories around.

## Starting from scratch

If you haven't been tracking your configurations in a Git repository before, you can start using this technique easily with these lines:

```
git init --bare $HOME/.cfg
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
config config --local status.showUntrackedFiles no
echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> $HOME/.bashrc
```

-   The first line creates a folder `~/.cfg` which is a [Git bare repository][6] that will track our files.
-   Then we create an alias `config` which we will use instead of the regular `git` when we want to interact with our configuration repository.
-   We set a flag - local to the repository - to hide files we are not explicitly tracking yet. This is so that when you type `config status` and other commands later, files you are not interested in tracking will not show up as `untracked`.
-   Also you can add the alias definition by hand to your `.bashrc` or use the the fourth line provided for convenience.

I packaged the above lines into a [snippet][7] up on Bitbucket and linked it from a short-url. So that you can set things up with:

```
curl -Lks http://bit.do/cfg-init | /bin/bash
```

After you've executed the setup any file within the `$HOME` folder can be versioned with normal commands, replacing `git` with your newly created `config` alias, like:

```
config status
config add .vimrc
config commit -m "Add vimrc"
config add .bashrc
config commit -m "Add bashrc"
config push
```

## Install your dotfiles onto a new system (or migrate to this setup)

If you already store your configuration/dotfiles in a [Git repository][8], on a new system you can migrate to this setup with the following steps:

-   Prior to the installation make sure you have committed the alias to your `.bashrc` or `.zsh`:

```
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```

-   And that your source repository ignores the folder where you'll clone it, so that you don't create weird recursion problems:

```
echo ".cfg" >> .gitignore
```

-   Now clone your dotfiles into a [bare][9] repository in a "_dot_" folder of your `$HOME`:

```
git clone --bare <git-repo-url> $HOME/.cfg
```

-   Define the alias in the current shell scope:

```
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
```

-   Checkout the actual content from the bare repository to your `$HOME`:

-   The step above might fail with a message like:

```
error: The following untracked working tree files would be overwritten by checkout:
    .bashrc
    .gitignore
Please move or remove them before you can switch branches.
Aborting
```

This is because your `$HOME` folder might already have some stock configuration files which would be overwritten by Git. The solution is simple: back up the files if you care about them, remove them if you don't care. I provide you with a possible rough shortcut to move all the offending files automatically to a backup folder:

```
mkdir -p .config-backup && \
config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | \
xargs -I{} mv {} .config-backup/{}
```

-   Re-run the check out if you had problems:

-   Set the flag `showUntrackedFiles` to `no` on this specific (local) repository:

```
config config --local status.showUntrackedFiles no
```

-   You're done, from now on you can now type `config` commands to add and update your dotfiles:

```
config status
config add .vimrc
config commit -m "Add vimrc"
config add .bashrc
config commit -m "Add bashrc"
config push
```

Again as a shortcut not to have to remember all these steps on any new machine you want to setup, you can create a simple script, [store it as Bitbucket snippet][10] like I did, [create a short url][11] for it and call it like this:

```
curl -Lks http://bit.do/cfg-install | /bin/bash
```

For completeness this is what I ended up with (tested on many freshly minted [Alpine Linux][12] containers to test it out):

```
git clone --bare https://bitbucket.org/durdn/cfg.git $HOME/.cfg
function config {
   /usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME $@
}
mkdir -p .config-backup
config checkout
if [ $? = 0 ]; then
  echo "Checked out config.";
  else
    echo "Backing up pre-existing dot files.";
    config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | xargs -I{} mv {} .config-backup/{}
fi;
config checkout
config config status.showUntrackedFiles no
```

## Wrapping up

I hope you find this technique useful to track your configuration. If you're curious, [my dotfiles live here][13]. Also please do stay connected by following [@durdn][14] or my awesome team at [@atlassiandev][15].

[1]: https://news.ycombinator.com/item?id=11070797
[2]: https://en.wikipedia.org/wiki/Dot-file
[3]: https://news.ycombinator.com/item?id=11071754
[4]: https://www.atlassian.com/git
[5]: http://www.saintsjd.com/2011/01/what-is-a-bare-git-repository/
[6]: http://www.saintsjd.com/2011/01/what-is-a-bare-git-repository/
[7]: https://bitbucket.org/snippets/nicolapaolucci/ergX9
[8]: https://www.atlassian.com/git
[9]: http://www.saintsjd.com/2011/01/what-is-a-bare-git-repository/
[10]: https://bitbucket.org/snippets/nicolapaolucci/7rE9K
[11]: http://bit.do/
[12]: http://www.alpinelinux.org/
[13]: https://bitbucket.org/durdn/cfg.git
[14]: https://www.twitter.com/durdn
[15]: https://www.twitter.com/atlassiandev
