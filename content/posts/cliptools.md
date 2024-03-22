---
draft: false
externalLink: ""
authors: []
slug: ""
title: coder theme hugo/ making frontmatter using smartclips on mac
date: 2023-12-09 20:50:53
tags: []
categories: []
description: ""
---


3 killer things I learned today
- [coder theme for hugo](https://github.com/luizdepra/hugo-coder)
- [smartclips for frontmatter](https://apps.apple.com/us/app/cliptools/id1619348240?mt=12)
- [keybind to create txt file on mac](https://apple.stackexchange.com/questions/129699/create-a-new-txt-file-in-finder-keyboard-shortcut)
## making a new file
- ive set ctrl-n to make a new file

this is the applescript i used:
```
set file_name to "untitled"
set file_ext to ".txt"
set is_desktop to false

-- get folder path and if we are in desktop (no folder opened)
try
    tell application "Finder"
        set this_folder to (folder of the front Finder window) as alias
    end tell
on error
    -- no open folder windows
    set this_folder to path to desktop folder as alias
    set is_desktop to true
end try

-- get the new file name (do not override an already existing file)
tell application "System Events"
    set file_list to get the name of every disk item of this_folder
end tell
set new_file to file_name & file_ext
set x to 1
repeat
    if new_file is in file_list then
        set new_file to file_name & " " & x & file_ext
        set x to x + 1
    else
        exit repeat
    end if
end repeat

-- create and select the new file
tell application "Finder"

    activate
```
## the frontmatter

using cliptools to write frontmatter for hugo blog posts is amazing. Beats doing "hugo new file.md" command in root directory. it was annoying to have to cd back and forth 3 directories over and over. I found it very disorienting.
That smartclips feature in cliptools is essential. hugo sorts your posts by date its critical that you get it in the right format its super tedious to type by hand and really hard to remember otherwise. its sooo good how it just plugs it in in the curly brackets. this is smartclip i use:

```
+++
draft: false
date: {date:yyyy-MM-dd HH:mm:ss}
title: ""
description: ""
slug: ""
authors: []
tags: [] 
categories: []
externalLink: ""
+++
```

## Hugo "coder theme" 
I kind of gave up on hugo for a while but i saw this nice minimal dark theme and its kind of perfect.

{{< youtube id="q6EoRBvdVPQ" title="yee" >}}

- aww yeah its all coming together.
system preferences > keyboard > shortcuts > services > new terminal at folder.


## FULLY VIM'd out blogging experience!!
Yesterday i tried to use some ancient python script from 2013 to try to post to bblogger from vim. added a bunch of crap to my vimrc. had to install some plugins read a bunch of docs. I installed some ruby thing.. granted some random package oath to access my blog (must remember to revoke that) and it didnt work. i was able to pull down previously posted blogs and read the std out in the terminal but i could'nt figure out a way to post new blogs. big waste of time. Then i remembered ol' hugo... thats why I decided to give it another chance.

Ive learned alot since My first attempts at a hugo blog. thats why my other main site was named site2. I had that foresight to know.

>> "everything you do you'll probably suck at doing for at least 2 years."
I feel like its finally starting to click.
### Vim Fugitive
- Git add .
- Git commit -m ""
- Git push

I learned how to properly use nerd tree. i have it set to ctrl-t and learned that m pulls up the option for doing stuff like file creation. I have ctl left/right arrow to switch buffers in vim.
