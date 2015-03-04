---
title     : Charts and Visual Encoding
layout    : post
category  : hands-on
tagline   : 
tags      : [week03, charts, visual encoding]

---

In a data visualization, every element is *encoding* something. Placement, spacing, color, height, width, area -- each has meaning. But what meaning? 

The [Data Visualization Catalog](http://www.datavizcatalogue.com/) is a great resource for thinking through encoding.


# Hands on

We're going to start with a simple chart project. Rachel can tell us where she got this data, but ...   


#### Criminal Deportations
	Region and country of nationality,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013
	El Salvador,2805,2827,3850,4949,5558,6344,8368,8507,8674,9440
	Guatemala,2176,2143,3850,3917,5138,6547,9432,11718,13494,15365
	Honduras,2544,2704,5752,5236,5476,6998,10420,10825,13815,16609


#### Child Migrant Apprehensions

	Country,FY 2009,FY 2010,FY 2011,FY 2012,FY 2013,FY 2014,FY 2015
	El Salvador,1221,1910,1394,3314,5990,16404,1797
	Guatemala,1115,1517,1565,3835,8068,17057,3548
	Honduras,968,1017,974,2997,6747,18244,951


Your first step is going to be to copy this into a spreadsheet and if it doesn't immediately break into columns, use `Data > Text to Columns` to break it out. As ever, read all dialogs closely. Understand, don't just click "okay"

We're going to use a few mechanisms to re-arrange these numbers so we can try charting them in ... 

* Medium's [Charted](https://medium.com/data-lab/introducing-charted-15161b2cd71e)
* Quartz's [ChartBuilder](http://quartz.github.io/Chartbuilder/)
* [RAW](http://app.raw.densitydesign.org/) -- for flat graphics to edit in illustrator

Charts and things has a nice post on [choosing the best form](http://chartsnthings.tumblr.com/post/36904562002/choosing-the-best-form). 
