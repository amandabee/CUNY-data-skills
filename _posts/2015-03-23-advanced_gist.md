---
title     : Gists (Advanced)
layout    : post
category  : hands-on
tagline   : Getting fancy
tags      : [week09, html, gists]

---


If you're using Windows, I don't have a good solution for you. That doesn't mean one doesn't exist, just that I haven't tried it. 

## Step 1: Install git

This is kind of cheating, but it works. Install Github's GUI for your operating system. You'll get to an option, once it's installed, to Install command line Git tools. Do it. 

(The alternative approach is to install [Homebrew](http://brew.sh/) and use Homebrew to install git and create an ssh key pair. And then you'll have to copy your SSH key to Github to authorize it. You can do all that, it just happens to be more complicated. 

## Step 2: Clone the Repository

Every Gist is actually a mini repository, which is super handy. You can "clone" the gist on your own computer if you know the right URL -- look for a box on the right-hand side of the screen that say something like "SSH clone URL" followed by "You can clone with HTTPS or SSH." -- if you see "HTTPS clone URL" click on the "SSH" link and the URL shoudl change to something that starts with `git@gist.github.com:` For example, one of mine is:

`git@gist.github.com:/e79ec70b209f033708bf.git`

Once you've got Github's gui installed, you should be able to open a terminal client (Applications > Utilities > Terminal) and run:

`git clone git@gist.github.com:/e79ec70b209f033708bf.git`

to create a directory (it will be called `e79ec70b209f033708bf` by default, but you can rename it without breaking anything) in your home folder containing all the files in your gist. 

## Step 3: Add your images

To add an image or other binary file, you'd first copy the image into your new directory. Then use `cd` to change directories into your gist folder. Then you can run `git status` and you should see a list of "Untracked files" that includes the images you just added. Use `git add .` to add them all at once. Then use `git commit -m "Adding image files" .` to commit them ("Adding image files" is your commit message in this case. You can, of course, change it.) and push them up to the server with `git push`.

Now your images are available as part of your gist bundle!
