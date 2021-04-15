# Git Cheat Sheet

My awesome git cheat sheet.

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
