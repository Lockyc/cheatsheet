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
