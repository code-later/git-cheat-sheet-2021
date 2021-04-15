# Git Cheat Sheet

My awesome collection of useful `git` commands!

## Create new project / repository

```
$ git init <project-name>
$ cd <project-name>
```

## Config

```
$ git config --global user.name "Ada Lovelace"
$ git config --global user.email ada.lovelace@example.com
$ git config --global core.editor vim
$ git config --global init.defaultBranch main
```

## Add first file (README)

```
$ git status
$ vim README.md
$ git add README.md
$ git status
$ git commit -m "Initial commit"
$ git status
```

## Interact with git objects

```
$ git log
$ cat .git/objects/XX/.....
$ git cat-file SHA
$ git cat-file -t SHA # Show type
```

## Create first branch

```
$ git checkout -b add-create-new-repo-part
$ git status
$ git vim README.md
$ git add README.md
$ git commit -m "Part about branches"
$ git checkout main
$ git merge add-create-new-repo-part
$ git branch -d add-create-new-repo-part
```

## Interact with GitHub

* Create repository [on GitHub](https://github.com/new)
* [Choose a license](https://choosealicense.com/)
* Pick a [`.gitignore`](https://github.com/github/gitignore)
* Configure local clone (depending if you already have a local repository or not)

```
$ git push -u origin main
$ git pull
```

* Configure "branch protection" -> Go to "Settings" of your repository
* Only work with branches / Pull Requests
* Add templates for Pull Requests and Issues

## Bonus: `.zshrc`

```
export PATH=.bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="~/.oh-my-zsh"

ZSH_THEME="sorin"

COMPLETION_WAITING_DOTS="true"
DISABLE_AUTO_TITLE="true"

# Which plugins would you like to load?
plugins=(
    brew
    chruby
    docker
    emacs
    iterm2
    git
    history-substring-search
    osx
    rake
    ruby
    tmux
    tmuxinator
    vagrant-prompt
    vagrant
)

source $ZSH/oh-my-zsh.sh

# User configuration

# You may need to manually set your language environment
export LANG=en_US.UTF-8
export LC_NUMERIC=en_US.UTF-8
export LC_TIME=en_US.UTF-8
export LC_COLLATE=en_US.UTF-8
export LC_MONETARY=en_US.UTF-8
export LC_MESSAGES=en_US.UTF-8
export LC_ALL=en_US.UTF-8

# # Preferred editor for local and remote sessions
if [[ -n $SSH_CONNECTION ]]; then
  export EDITOR='vim'
else
  export EDITOR='vim'
fi
```
