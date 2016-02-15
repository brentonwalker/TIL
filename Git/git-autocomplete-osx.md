#Autocompletion in Bash on OS X

[Source](https://git-scm.com/book/en/v1/Git-Basics-Tips-and-Tricks#Auto-Completion)

1. Install homebrew by running this script:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
>if it gives you problems about ownership of /usr/local permissions, change ownership like this:
>
>  ```
> chown -R $USER:admin /usr/local
> ```


2. Install Git and bash-completion:

```
brew install git && brew install bash-completion
```

(Note: If this install fails with a 404 error, and you already have git installed, just remove the git part of this brew install)
Add bash-completion to your .bash_profile:

```
if [ -f `brew --prefix`/etc/bash_completion ]; then
    . `brew --prefix`/etc/bash_completion
fi
```
