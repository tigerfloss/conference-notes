# Introduction to git (even for Non-Developers)
Speaker: John Anderson, @genehack, os101/columbia, infinity interactive

>We are _humans_, working with _humans_, to develop a software for the benefit of _humans_ ~the shirt he's wearing

## What is git?
distributed revision control system

distributed ~~revision control system~~ track changes

### revision control system
(rcs, cvs, svn, tfs, git, etc)

> I am getting tired of interviewing students with fresh CS degrees who doesn't know rcs

git is not only for **code**

git is **not** *github/gitlab*

Learning the basics of git will help
regardless of what git hosting is used


### Getting git
	(git-scm.com)

#### cli versus gui

### we need to tell git who we are
```md
git config --global user.name "Put your name here"
git config --global user.email "your email here"
```
### Obtaining a Repository
#### Clone
`git clone <url>` 
#### Second Option: DIY
`git init my-new-project`

### Add files
#### create file
`touch README.md`
#### what's going on?
`git status`
#### add README.md
`git add README.md`

### lifecycle of files according to git
* untracked
* staged
* committed
* modified

git wants commits to have an accompanying _commit message_

`git add` takes files from 'untracked' to 'staged'
`git commit` takes files from 'staged' to 'commited'

`git diff` compares the files

adding and editing files are not that different


`git log` see the history of the repository

`git log -p` see the history and the changes

### Branch 
is a new working copy of your repo
allow you yo make chagnes without altering the underlying 

### Merge
when the work on the brach passes review

### Pushing
sending changes to some other copy of the repository

### Remote
the location where you are sending the changes

## What to do when things go *bad*?
### two fixes that (almost) always work
	1. make a copy of and fix it there
	2. rename you repo directory (from `repo` to `repo.bad`) and the **re-clone** the repo

`git status` - hey what's going on?

`git add` - unknow state -> staged

`git commit` - staged -> committed

`git diff` - compare the differences

`git push` - send changes

[interactive git tutorial tool](try.github.io)
