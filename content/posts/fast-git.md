---
draft = false
date = 2023-12-15 01:23:32
title = "Giggity git: the fast git script"
description = "a script to make a git a bit easier to deal with"
slug = "fast-git"
tags = ["bash", "hugo", "vim"] 
categories = []
---

# simplifying version control
git can be complicated.
I made a little bash script to make life easier.
it pulls, adds, commits, pushes.
the nice thing is it asks you for your commit message.
> always pull before pushing.
> always wipe from front to back.
avoid those merge conflicts like the plague.

add an alias to this to your .zshrc or .bashrc.
i called mine giggity.sh
of course dont forget to chmod +x it.


```
#!/bin/bash

# Perform a Git pull to update the local repository
git pull

# Add all changes to the staging area
git add .

# Prompt user for commit message
read -p "Enter commit message: " commit_message

# Commit changes with the provided message
git commit -m "$commit_message"

# Push changes to the remote repository
    git push
```

add this to your .vimrc:
```
" my cool git shortcut
command! -nargs=* Giggity :execute '!bash /Users/bweew/Documents/bash/giggity.sh' <args>
```
then you can run the command :Giggity to push to git

### changed for linux
it worked fine on my mac made some updates to work on my linux mint computer

```
command! -nargs=* Giggity :execute '!/home/mint/Documents/bashscripts/giggity.sh' <args>
```
