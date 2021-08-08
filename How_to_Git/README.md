# Sections

## 1. and 2. Preparation

Setting up name and email can be pretty straightforward, but what may matter is setting up autocrlf to true on windows and safecrlf to warn. [Read more](https://githowto.com/setup)

git config --global user.name "Andres"

git config --global user.email "nanoandres_24@hotmail.com"

git config core.editor "vim"

## 3. Create a project

- git init
- git add FILE
- git commit

## 6. Staging the changes

A git add can be reverted via git reset. Git reset won't undo commits or pushes

## 10. History

git log 

We can get a simplified log to only yield the commit's key and the commit message by using...

**git log --pretty=oneline**

This can be manipulated further with options like 

```
git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=<your name>
git log --pretty=oneline --all
```
### Fancy formatting

git log --all --pretty=format:"%h %cd %s [%an]" --since='7 days ago'
git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short

- %h is the abbreviated hash of the commit
- %d commit decorations (e.g. branch heads or tags)
- %ad is the commit date
- %s is the comment
- --graph tells git to display the commit tree in the form of an ASCII graph layout
- --date=short keeps the date format short and nice
