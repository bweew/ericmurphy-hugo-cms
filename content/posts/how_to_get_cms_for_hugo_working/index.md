---
title: how to get CMS for Hugo working
date: '2024-03-14'
author: bweew
description: ''

---



* download quiqr
* import your hugo site from github
* import the dark theme community template
* cd into  quiqr > your sites folder > main >quiqr > model > 
* copy the contents of includes and partials into your templates includes and partials
* in includes update collections.yaml
* make sure content/pages matches the name for where your pages are stored
* in templates
* in main directory edit config.toml if needed to change what shows up on your main site
* in config.toml i had to change posts to post for my page link to work properly

## TO PREVIEW:
- must change site config base url 
- http://localhost:1313/posts  for when you push to github
- / for local development

### its http://localhost:1313/posts
its not http://localhost:1313/posts/ no slash on the end!
oh in my case it was localhost:1313/post bc the path in the directory was that

its kind of annoying :( switching back and forth but the beauty of the cms is you don't need to really preview it you can just keep writing in the editor and push when your ready. so for the most part maybe il leave it on localhost:1313? hmm maybe in the github actions theres a way to fix this?

To get it back up on github
* cd user/Quiqr/sites/yoursite/main
* open up your terminal and do your git stuff

## make a shortcut for git
in shortcuts
* ask for input with commit message
* run shell script
* cd to the main directory
* git pull git add . git commit -m "PROVIDED INPUT"
* git push

when the shortcut is run it will ask for input. I like to pin this to menu bar.
### a step further
- write it to an nfc tag, trigger it by tapping your phone
- name it something easy and trigger it with siri