---
title     : Gists (Advanced)
layout    : post
category  : hands-on
tagline   : Getting fancy
tags      : [week09, week10, git, html, gists]

---


**Git** is a distributed version control system. You've been using it quietly for a while already. **[Github](http://github.com)** is a service that provides hosted, centralized git repositories. There are a lot of other services that do the same thing. A **gist** is github's term for what is effectively a mini repository. It doens't have all the bells and whistles of a full repository but it is a quick and easy way to get a document online. You can actually [do rather a lot](http://www.labnol.org/internet/github-gist-tutorial/28499/) with gists, including run them through <http://bl.ocks.org> to view them as HTML. 

There are plenty of good git tutorials available. Here are three:

+ <https://try.github.io/>
+ <https://digitalfellows.commons.gc.cuny.edu/2015/03/10/intro-to-github-part-i/>
+ <https://18f.gsa.gov/2015/03/03/how-to-use-github-and-the-terminal-a-guide/>

# Your first repository.

Head over to <https://github.com/> and look for a giant `+` in the upper right. You're going to `Create new > New repository`.

Name your repository "Community Profile". 

Normally, I'd tell you to check the box next to "Initialize this repository with a README" -- if you're starting from scratch, you definitely want to do that. But in this case, you're not starting from scratch. So instead, I want you to just go ahead and create.

Then, look for the `import code` button. 

Your gist is actually a mini repository, and you can clone it by looking for the `HTTPS clone URL` and pasting that in the URL field. You should either get an error, quickly, or some indication that github is importing your repository. If you get an error, [ask for help](https://github.com/amandabee/CUNY-data-skills/issues)!

## `gh-pages` branch

Once your gist repository is imported to your new "community profile" repository, you've got a few more things to tweak.
Don't skip any steps. Trust me -- every one of the next steps is super important. If you get stuck or confused, [ask for help](https://github.com/amandabee/CUNY-data-skills/issues).

On the "Branches" pulldown, create a branch called `gh-pages` -- you need that to be exact. As you type it in a "Create a branch" button will appear. Click it when you're done typing. That *should* copy all of your files to a new branch.

Under `Settings` (on the right hand side) you're going to change your default branch to `gh-pages`. The default branch pulldown is right up at the top of your settings.

Then, still in the `Settings` dialog, look for the `Collaborators` menu on the left. Find your partner's handle, and add them as a contributor on your community profile.

Now you can stop and take a deep breath. You did it. 

Once you've confirmed (and showed me!) that you can edit your partner's repository and they can edit yours, you should probably delete at least one of them. :)

## Check out your project

Anything on the `gh-pages` branch of a git repository *on github* is visible online at `https://{username}.github.io/{repository_name}`. Since my username is `amandabee`, my `CUNY-data-skills` repository is visible at <https://amandabee.github.io/CUNY-data-skills/>. Pretty cool, eh? 

### What was that branching thing?

Git's [branching](http://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) functionality is very powerful and way, way beyond the scope of what we're up to this semester. For now, all you really need to know is that Github's "pages" system will make any HTML on the `gh-pages` branch available through a webserver. One that updates immediately when you save to it. 

## Nothing is without compromises

You can choose to make a gist public or keep it private. Even with a free account. A github repository is always public unless you've paid money for (or they made a mess of your life and tried to make it better by giving you) a premium account.

If you want to get fancy, the instructions below will get you halfway down the road to use your private gist as a collaborative repository. Once you get through the process of adding an image, [let me know](https://github.com/amandabee/CUNY-data-skills/issues) and I'll add instructions for the next step.




# Using Git to Manage a Gist

And Mike Bostock has written a great rundown on how to add binary files (like images) to gists. [Read it](http://bost.ocks.org/mike/block/). But these steps will work. If you're using Windows, I don't have a good solution for you. That doesn't mean one doesn't exist, just that I haven't tried it. 

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