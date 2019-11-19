# dotfile-wsl-ubuntu

Dotfiles for Ubuntu on WSL

## Ideas

- Create Go application for installation + templating? DONE: [TwinProduction/gemplater](https://github.com/TwinProduction/gemplater) 


i.e.

The file `.profile` would look like this:
```
export EDITOR="__EDITOR__"

export LANG="en_US.UTF-8"
export LC_ALL="en_US.UTF-8"
export LC_CTYPE="en_US.UTF-8"

export GOPATH="__GOPATH__"
export GOBIN="$GOPATH/bin"
export PATH="$PATH:$GOBIN"

export GO111MODULE=on

[[ -f ~/.bashrc ]] && . ~/.bashrc
```

and to install it, you'd have to:

```
$ <installation-app-name> install .profile
Enter value for __EDITOR__ (default: nvim): 
Enter value for __GOPATH__ (default: $HOME/go): /mnt/e/Go
```

the installation/template file should support both files and folders as options.

