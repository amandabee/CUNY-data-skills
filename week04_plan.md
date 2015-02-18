
## Map Examples 
[Most Common Job, By State](http://www.npr.org/blogs/money/2015/02/05/382664837/map-the-most-common-job-in-every-state)  
[Inside AirBNB](http://insideairbnb.com/index.html)  
[CA Drought](http://www.motherjones.com/blue-marble/2014/07/watch-drought-take-over-entire-state-california)

+ WNYC [Sandy Flooding](http://project.wnyc.org/flooding-sandy-new/#12.00/40.7378/-74.07020)
+ ProPublica [Government Lends to Rebuild in Flood Zones](http://projects.propublica.org/sandy-sba/)
+ NPR [Zoom In On Oklahoma Tornado Damage](http://apps.npr.org/moore-oklahoma-tornado-damage/)
+ [As Bloomberg Built Affordable Housing, City Became Less Affordable](http://www.wnyc.org/story/304422-new-york-remade-city-more-desirable-ever-also-too-expensive-many/)
+ [map as navigation](http://www.telegraph.co.uk/news/worldnews/asia/japan/9134487/Graphic-Aftermath-of-Japan-earthquake-and-tsunami-and-Fukushima.html)



[More maps](http://dataskills.tumblr.com/tagged/maps)

[Alex Howard on Data Quality](http://radar.oreilly.com/2013/01/data-journalism-analysis-accountability.html)

We don't deal with [projections](http://xkcd.com/977/) but they matter. 


More notes
http://maptime.io/lessons-resources/


## CartoDB
# CartoDB BLS

In 2011, the BLS published a [map of fatal workplace injuries](http://bls.gov/opub/btn/volume-2/death-on-the-job-fatal-work-injuries-in-2011.htm) by state. 

Good discussion questions:
Are these colors continuous or categorical? Should they be? Is anyone surprised that CA and TX have a lot of workplace injuries? How can we improve on this?

Takeaway: BLS data is mapped, but it isn’t normalized to the population and the gradient makes no sense at all.

So we'll recreate it: 
+ [BLS Fatality Data (csv)](cartodb/)
+ [2011 Population Estimates](https://www.census.gov/popest/data/state/totals/2011/tables/NST-EST2011-01.csv) (via [census.gov](http://www.census.gov/popest/data/historical/2010s/vintage_2011/state.html))

Combine those two in a spreadsheet, first.  Use "Save As" to create a new spreadsheet so you don't clobber your data. 

Use `=find()` to confirm that state names match. They will until ~New York

Use `=G10/E10` to get fatalities per capita, talk about scientific notation, then `=(G10/E10)*100000` for per 100,000

##Upload to CartoDB

Upload the CSV to CartoDB. Now you need a shapefile. Get a US State file from [NationalAtlas.gov](http://nationalatlas.gov/mld/statesp.html) or [NOAA](http://www.nws.noaa.gov/geodata/catalog/national/html/us_state.htm) or this [much, much smaller](http://geocommons.com/overlays/21519) file from GeoCommons. (Use the KML, the shapefile doesn't have a projection)

GoogleMaps will only take KML files, CartoDB will take ShapeFiles or KML, but don't use Safari -- a shapefile is a bundle of database files, you don't want to unzip it. 

### Merging
CartoDB used to make merging harder but they've worked a few things out. 

Keep both open: what columns can we use to combine these two? 

CartoDB has a [good explanation](http://developers.cartodb.com/tutorials/joining_data.html) of the join process. It isn't actually straightforward.

	UPDATE fatalities_per_capita
	SET the_geom = 	us_states.the_geom
	FROM us_states
	WHERE us_states.state = fatalities_per_capita.state
		

#### Note
The first time I tried this I went the other way and hit some useful errors. Noted here for future reference. 

Add a numeric column: "bls_fatalities_per_100k"

	UPDATE us_states 
	SET bls_fatalities_per_100k = 	fatalities_per_capita.fatalities_per_capita
	FROM fatalities_per_capita
	WHERE us_states.name = fatalities_per_capita.state

Error: `column "bls_fatalities_per_100k" is of type double precision but expression is of type text`  -- what do we think that means? 

A little more on [double precision](http://www.postgresql.org/docs/current/static/datatype.html). We have two choices: we can go to the first table and change the column type to numeric. Or we can use `to_number(fatalities_per_capita.fatalities_per_capita, '999D9999999')` to transform the string into a number in the query. 

### Display
Use the wizard first. Bubbles for population, color for percapita. 

What do methods mean? [Learn](https://github.com/amandabee/cunyjdata/blob/master/lecture%20notes/cartodb.md#method) This was a little [buggy](https://gis.stackexchange.com/questions/84562/am-i-misunderstanding-equal-interval) but might be fixed by now.

### Put it on a web page


### Where to Find Boundary Files
+ [NYC:](http://www.nyc.gov/html/dcp/html/bytes/dwndistricts.shtml)
+ [CUNY Research Center](http://researchcenter.journalism.cuny.edu/digital-maps-database/)
+ [Google Fusion Table search](http://www.google.com/fusiontables/search)
+ [NYC Data sets](https://github.com/jweir/nyc-gov-data/blob/master/data/nyc_data_sets.markdown)
+ [GeoCommons](http://geocommons.com/)
+ [CartoDB's Common Data](https://cunydata.cartodb.com/dashboard/common_data)
+ [Census.gov](https://www.census.gov/geo/maps-data/)

### How to Geocode
If you need to transform addresses into lat/lon pairs, you have a couple of options:

+ Fusion Tables will do it, but their terms of service say you have to use that data on a Google Map. 
+ Geocoder.us Will do one address at a time, or you can pay for a batch
+ CartoDB gives you a bunch free and you can pay for more. 
+ More [suggestions](https://stackoverflow.com/questions/373383/geocoding-libraries)





## Storyboards
