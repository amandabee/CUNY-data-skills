---
title    : Highcharts
layout   : post
category : hands-on
tagline  : Making somewhat fancy stuff
tags     : [week15, charts]
---

We didn't tackle [Highcharts](http://www.highcharts.com/demo/line-basic) this semester but we could have. One thing I like about Highcharts is that they have [great demos](http://www.highcharts.com/demo/line-basic) of their basic chart types, and their [API](http://api.highcharts.com/highcharts) is really nicely documented. 

Their demos open in JS Fiddle, so you can play around with tweaking them without setting up your own environment. So: start by registering with [JS Fiddle](http://jsfiddle.net/) and logging in, so you can save your work. If you get stuck, [ask for help](https://github.com/amandabee/CUNY-data-skills/issues).

**Step One: get organized**. You're going to need a few windows open. You might want to close other windows so you can focus.

+ the [Highcharts Demo](http://www.highcharts.com/demo/) page in a browser (we'll start with a basic line chart)   
+ our [sample data on Bronx graduation rates](https://raw.github.com/amandabee/cunyjdata/master/assignments/graduation_outcomes.csv) in a text editor or spreadsheet program   
+ your text editor (if you don't have one, try [Sublime](http://www.sublimetext.com/) or [Text Wrangler](http://www.barebones.com/products/TextWrangler/), or if you're feeling fancy and want free and open source software, try [Emacs](http://emacsformacosx.com/) or [Vim](http://macvim.org/OSX/index.php))   
+ [Mr Data Converter](http://shancarter.com/data_converter/) in a browser   

**Step two: get started**. Open the demo in JS Fiddle (there's a button: "Edit in JS Fiddle"), and copy your data from the CSV to Mr Data Converter. Play around with the output options and see if you can make sense of the results. Look at the three JSON options. Can you see how they differ? Do you understand how Mr Data Converter is re-organizing the data you entered? When you're done exploring, you should choose "JSON - Column Arrays" -- copy the output and paste it into a blank page in your text editor.

**Step three: make your first edit**. The title of the demo chart is "Monthly Average Temperature" but our numbers are about graduation rates in the Bronx. Find the title option and edit it. JS Fiddle does a nice job of color coding the code so you can see that the apostrophes are important to the structure of the JavaScript. Use the "Run" button to test your change. If JS Fiddle redraws the chart with new title, go ahead and save your work and keep going. If the chart pane is blank, your script is broken. Look at what you just changed -- every apostrophe, comma, square bracket and curly brace matters so make sure you didn't add an extra apostrophe or remove a comma. Keep using "Run" to test your changes.

**Step four: keep tweaking**. Start walking through the settings and making changes. After every change (every single one. Trust me.) test your work by running it and save (or "Update) your work only if the changes worked. That way you can go back to a known working copy if you screw something up.

Update the xAxis categories by copying the data from the "Cohort" array that Mr. Data Converter generated (again, this is a lot easier to do if you copy the JSON into a text editor before you start copying and pasting).

We changed the tooltip value suffix to "%" -- you can do that as you walk through the settings or wait until you've got the data in place and can see with your own eyes how silly the initial value suffix looks.

Remember your workflow: Change one setting, run, update only if the change worked.

Replace the world temperature data with graduation rates. You'll only have series (graduated and dropped out) while the demo had four. You're going to need to remove two series, so take a moment to make sure you understand where each series starts and ends and how they're delimited. JS Fiddle can really help with this! Try putting your cursor right next to a curly brace or square bracket. It should turn bright green and somewhere on the page, a matching brace should also turn bright green. Those braces are a pair. One opens, the other closes. If your brace turns red, you need to start tracing your work to figure out where you've got a missing brace or bracket.

Remember your workflow: Change one setting, run, update only if the change worked.

Tip: usually, a comma separates two items in a series, so you don't want a comma after the last item.

**Step five: get fancy**. Take a look at the [Highcharts reference](http://api.highcharts.com/highcharts) and find the line [marker](http://api.highcharts.com/highcharts#plotOptions.line.marker) option under [Plot Options](http://api.highcharts.com/highcharts#plotOptions). Read the documentation. Don't skim it, read it. Think about what it is saying. And then look at their <a href="http://jsfiddle.net/gh/get/jquery/1.7.2/highslide-software/highcharts.com/tree/master/samples/highcharts/plotoptions/series-marker-enabled/">marker demo</a>. What's a "line marker"? Can you tweak your graduation rate chart so it doesn't use line markers?

**Step six: get really fancy**. Start digging around in the demos and in the API reference. See if you can draw a plot band or move your legend or make the chart look the way you want it to look. 

Remember your workflow: Change one setting, run, update only if the change worked.

If you get stuck, leave a comment here. Give us all the URL of the last good working copy (the one you saved) and a new fiddle URL that shows the version that didn't work out so well. Tell us what you were trying to accomplish. 

## Embedding a Chart
When you're ready to embed a chart, JSFiddle's build in iframe tool is handy, but in the long run it isn't what you want. Embedding Fiddles is fiddly, so instead of mastering JS Fiddle learn how to put a chart on your own page.  

I put together some very useful [Bootstrap templates](https://github.com/amandabee/cunyjdata/tree/master/lecture%20notes/bootstrap) including two Highcharts templates that are your best starting points. If your chart isn't showing up where you think it ought to, try checking the following:

+ Did you place a `<div..>…</div>` on the page where you want the chart to appear?
+ Does your `<div>` have a descriptive, one word id? `id="container"` is not descriptive. `id="time_to_leak"` is.
+ Is your Highcharts function looking for the right id?  
`$(function () {$('#oscar_night').highcharts({` is looking for a div with `id="oscar_night"` 
+ Is your jquery call above your function? (By "jquery call" I mean the script tag that includes a minified copy of jQuery, probably from a content delivery network somewhere. Something like `<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>`
+ Is your highcharts call below your function? (That's the line that pulls in Highcharts' scripts `<script src="//code.highcharts.com/highcharts.js"></script>`)

## Good questions
**Is Highcharts free?** It is available free of charge [under some circumstances](http://shop.highsoft.com/faq#what-is-non-commercial), but it isn't [free](http://www.gnu.org/philosophy/free-sw.html) and [open source](http://opensource.org/osd-annotated) software. If you develop a Highcharts based chart for a site that is commercial and doesn't already have a Highcharts license, they will have to [purchase a license](http://shop.highsoft.com/highcharts.html).

**How do I embed this on my story?** We'll walk through this in class next week. If you want to use a Highchart for your current story and I didn't already show you how to embed it, let me know and I'll give you a clunky workaround until next week.


