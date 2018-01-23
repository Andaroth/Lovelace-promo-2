# Exercise: Protected folder file Explorer

- Repository : `bcd-protected-folder-file-explorer`
- Mode: alone or in 2 : a frontend and a backend
- Allowed time : 22 days for "functional", + 3 days for "pretty"

## Mission
We have a folder full of interesting files : pdfs, epub, graphics, sometimes videos and audio files, zip and rar files.     
We would like to share it to a group of selected folks but protect it from the outside world (including the Googlebot ;-) ).  
 
Could you provide us with a protected online place where our folks would have to login (one password for all) ? Once logged in, they could navigate the hierarchy of files and folder and view / download the files inside ?

## Learning objectives
- Backend language (PHP, RoR or Python) : 
	- 	password protection
	-  serverside user sessions
	-  reading inside a folder
	-  create a file &amp; folder navigation
	-  possibly: database design and implementation
	-  dependancy management via composer
-  Frontend :
	-  Third-party CSS Framework
	-  lighthouse test
	-  bonus : PWA
	-  icon fonts
	-  sass workflow
	-  dependency management (via yarn or npm)

## Specifics

### Must-have features

Logged in users must be able to :

- navigate through the file and folders using their browser
- download files of interest
- preview images, videos and audio
- sort by : title name, file type, file size, file date.
- The overall User Experience must feel professional : no spelling mistakes, no bugs, no 404. The interface is cross-platform, and when viewed on a mobile, a prompt suggest the user to pin the website on its homescreen (PWA).
- Each file has an icon relevant to its file type (audio, video, pdf, zip, rar ...) .
- php dependency management via composer
- frontend dependency management via 

### Nice-to-have features
These features should only be developed once the must-have features are in place.  

This set of features will require the use  of a database.
Logged in users should be able to :

- search through all files directories by keywords
- see the number of times each file has been downloaded.
- usage of a PHP microframework ([fatfree](https://fatfreeframework.com), [Slim](https://www.slimframework.com/), ... ).

## Deployment
Your own php/mysql hosting
- heroku for php
- freemysqlhosting.net for databasing

## Deliverables
 Repository with 
 
 - sourcecode + SQL creation file
 - installation instructions
 - maintenance documentation.

## Project steps

- build a team (if not alone)
- create the repo
- study the project
	- mockups
- frontend: html/css prototype
- backend: identify the functional implementation challenges

## A last word.
This may seem daunting at first. Don't worry. Face the challenge with an open spirit. Break the challenge into smaller problems that are easier to tackle.  

Start with the login form. Make it pretty. Then move up. Make it functional. Once it is functional, learn how to read a folder to retrieve the content programmatically. Get comfortable with the problem. Don't try to get rid of it, get to know it.

Still cared?  Try the haka dance.

![Giphy](./haka.gif)

