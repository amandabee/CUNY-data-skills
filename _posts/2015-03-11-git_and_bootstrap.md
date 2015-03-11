---
title     : Git and Bootstrap
layout    : post
category  : hands-on
tagline   : 
tags      : [html, bootstrap, git]

---


# Git

**Git** is a distributed version control system. You've been using it quietly for a while already. **[Github](http://github.com)** is a service that provides hosted, centralized git repositories. There are a lot of other services that do the same thing. A **gist** is github's term for what is effectively a mini repository. It doens't have all the bells and whistles of a full repository but it is a quick and easy way to get a document online. You can actually [do rather a lot](http://www.labnol.org/internet/github-gist-tutorial/28499/) with gists, including run them through <http://bl.ocks.org> to view them as HTML. 

There are plenty of good git tutorials available. Here are three:

+ <https://try.github.io/>
+ <https://digitalfellows.commons.gc.cuny.edu/2015/03/10/intro-to-github-part-i/>
+ <https://18f.gsa.gov/2015/03/03/how-to-use-github-and-the-terminal-a-guide/>

And Mike Bostock has written a great rundown on how to add binary files (like images) to gists. [Read it](http://bost.ocks.org/mike/block/) 

I used

    git clone git@gist.github.com:/5b0cf270dfee2511a946.git
    
to make a local copy of the gist at <https://gist.github.com/amandabee/5b0cf270dfee2511a946>. I had no trouble pushing my edits back up, using my password. If you want to *collaborate* on gists, you'll need keys, which is more complex than we're going to get today. 

# Bootstrap

Now that you can clone your Gist locally, you can start playing with really improving on the HTML. 

HTML is markup. It defines paragraphs and links, lists and headers. Everything we do to line things up, make them pretty, make them ugly -- that almost all happens in CSS. We're not writing CSS from scratch, however. We're going to be using [Bootstrap](http://getbootstrap.com/).

So our first project is to transform our chart assignment into an HTML page that uses Bootstrap to do better layout. Bootstrap gives great instructions for downloading their scripts and stylesheets and adding them to pages. Don't!

Instead of downloading anything, we're going to use a content delivery network to host our CSS and JavaScript files. There are [tons of good reasons](http://encosia.com/3-reasons-why-you-should-let-google-host-jquery-for-you/) to do this. Tons. But it is also much easier. 

So take a look at my Bootstrap [Templates](https://github.com/amandabee/CUNY-SOJ-data-storytelling/tree/master/lecture%20notes/bootstrap) templates and copy one into your own text editor. 

We'll work together on editing it. I'll make a clean post out of my [old HTML notes](https://github.com/amandabee/CUNY-SOJ-data-storytelling/blob/master/lecture%20notes/html.md) but in the meantime there are some good resources there as you bushwhack your way through HTML. 

# Viewing it in a Browser

We may not get to this but you're looking for `python -m SimpleHTTPServer` which will start a little web server at <http://0.0.0.0:8000>.
