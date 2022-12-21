# Tar
extract
```
tar -xf something.tar.gz
```
extract to new directory
```
tar -xf something.tar.gz -C /new/directory/path
```
verbose
```
-v
```
```
tar -xvf something.tar.gz
```

---
<sup>[cheatsheet](https://github.com/Lockyc/cheatsheet) | [dotfiles](https://github.com/Lockyc/dotfiles)<sup>


# Fix Invalid Package Name “.DS_Store” for Node.js NPM Global Update on macOS
```
find /usr/local -name '.DS_Store' -type f -print -delete
```

```
find ~/.nvm -name '.DS_Store' -type f -print -delete
```

# Function parameters

```
# Documentation for regularily used function parameters
# Argument accssing
# $_ is last argument
# $@ is all arguments
# ${@:1} array access, 1 based
# ${@:2} would skip the first argument
testing(){
	echo "\$_ = " $_
	echo "\$0 = " $0
	echo "\$1 = " $1
	echo "\$@ = " $@
	echo "\${@:1} = " ${@:1}
	echo "\${@:2} = " ${@:2}
	echo "\${@:3} = " ${@:3}
}
```

# ohmyzsh Commands

| Command         | Description                                                                                |
| :-------------- | :----------------------------------------------------------------------------------------- |
| `mkcd` | Create a new directory and change to it, will create intermediate directories as required. |
| `take` | Like `mkcd`, but also knows how to handle remote URLs. When given an argument that looks like a URL (something that ends in `.git` or `.tar.(gz\|bz2\|xz)`), download the remote resource and extract it (if necessary) into the current directory. Then change to the newly extracted/downloaded/cloned directory. |
| `..`       | `cd ..`                                    |
| `...`      | `cd ../..`                                 |
| `....`     | `cd ../../..`                              |
| `.....`    | `cd ../../../..`                           |
