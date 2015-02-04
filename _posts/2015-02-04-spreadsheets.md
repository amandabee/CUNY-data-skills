---
title     : Spreadsheet Skills
layout    : post
category  : hands-on
tagline   : Digging in
tags      : [week02, spreadsheets]

---

I keep a running list of my favorite spreadsheet commands on the [cunyjdata wiki](https://github.com/amandabee/cunyjdata/wiki/Tip-Sheet:-Spreadsheets). That's a great resource. 

## From this week's assignment:

Cristina found a [pretty interesting data set](
http://www.nyc.gov/html/dot/downloads/misc/outreach_schools.json) that is in JSON. 
There are a lot of different ways to convert JSON to CSV. [This is one.](https://json-csv.com/)

+ Convert it to CSV
+ Open it in Excel
+ Pivot -- you probably *don't* want column A. 
+ Let's use `features__properties__Activity` as our Row Labels and a count of `features__properties__FID` for our Values

So what have they been up to? 

+ Add the dates as a column label, and then right click on **row 4** of the pivot table itself to `group` by `Month`.

## Education Outcomes

Download [2005-2010 Graduation Outcomes Data](https://data.cityofnewyork.us/Education/Graduation-Outcomes-Classes-Of-2005-2010-By-Boroug/avir-tzek)

Pivot, use Boroughs as row labels, Demographic as column labels, % of cohort as the Value. 
Play around. Add "Cohort" as a row label. 

In groups of 3, what's interesting about this data? What would you like to chart. How could you pivot to get to what you want to chart?

## Flu Trends

Google tracks searches for flu-related terms. Start at <http://www.google.org/flutrends/> -- it is worth reading up on how they produce this data so you have a sense of the limitations of it, but we're just going to play with it. 

Open it in a spreadsheet. Use `Data > Text to Columns` to break it up if it isn't already broken up. Hint: it is "comma delimited" 

+ In which week did which country have the most flu searches?  
	`=Max()`  
	`=Match(criterion, range, 0)`  
	`=Indirect(“A”&cell)` to get date or re-order columns
+ How much more did that country search for flu in that week than average?
+ Order the countries by most flu searches (SUM...choose arbitrary 2012-13 to capture searches from all countries, Transpose countries-values to make a quick bar chart)

## Noise Complaints by CD

Starting at [the dataset of datasets](https://nycopendata.socrata.com/dashboard), find 311 complaints and filter for noise. 
