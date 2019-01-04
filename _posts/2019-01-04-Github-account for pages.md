# Github - account for pages	
Username: matt.burton@healthcare21.co.uk
Password: HealthCare2!
**@Hc21dev**!

Building Jekyll locally - Installing with home-brew:
[Install Jekyll on macOS Mojave](https://desiredpersona.com/install-jekyll-on-macos/)

Running Jekyll locally:
` bundle exec jekyll serve`

Server runs at:
 http://127.0.0.1:4000/

## Adding posts
You must include this at the top of your markup 
```
---
layout: post
title:  "Running Jekyll - github"
---
```
You can also add other items here - for  categories etc.

You also need to put the file in the _posts folder and name it with the date at the start eg:

2019-01-04-Hello.md

so the process I used was -
Export from  Bear as markdown into the _posts folder 
-Edit the file and add the header as above- *This doesn’t seem mandatory but we should definitely look at categories
Rename the file as  - 2019-01-01-Github-account for pages.md
Jekyll should rebuild the local copy

Happy - push to git and away you go.