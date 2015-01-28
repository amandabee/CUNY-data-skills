---
layout : page
title : Syllabus, Data Skills
tagline : Social Journalism Spring 2015
categories : [syllabus]

---
{% include JB/setup %}

| Room 438 | Wednesdays, 2:30 - 5:30 |
|---|---|
| Amanda Hickman  | <amanda.hickman@journalism.cuny.edu>  |
|  Tumblr:       | <http://dataskills.tumblr.com> | 
| Class Wiki:    | <https://github.com/amandabee/CUNY-data-skills/wiki> |

It isn't hypberbole: journalists today have access to more data than ever before, as well as to better tools to understand that data and retell the stories it holds. Whether you want to understand your own audience better, measure the impact of efforts to expand your reach, or just tell stories about the impact of policy, a little bit of data can go a long way, *if* you have the skills to put data to use.  

This semester we will work together to gather, analyze and visualize numbers you need to understand your audience and to tell interactive data-driven stories. 

We'll look at the data that helps us *listen* to audiences -- who are they and what are they asking? We'll *gather* data that can help answer those questions, *interrogate* the data to make sure we have clear and realiable answers, and we'll *present* that data in clear engaging stories and reports. 

We'll use Excel (or LibreOffice's Calc) and some command-line tools like CSVkit to dig into numbers and we'll use web-based tools such as CartoDB and HighCharts to create maps and charts that clearly illustrate your findings. You'll pick up a little HTML, CSS and jQuery along the way -- just enough to show off your work online. This is not a course in coding, but programmers of all skill levels are welcome.

Note: this class will go deep on some data analysis tools, such as spreadsheets, that you will be expected to master. We will aslo introduce more complex advanced tools that you won't master in a semester. 

## SYLLABUS in BRIEF

Lecture: what you can expect from me | Homework: what I expect from you    |
---|---|
**Jan 28**: Finding and defining data, Context   | Readings                             | 
**Feb 04**: Visual Encoding, CSVs, Pivot Tables  | Pre-pitches -- data you're interested in            |
**Feb 11**: Cleaning data with OpenRefine, FTP   | Spreadsheet exercise, <br />Pitch (community profile)   |
**Feb 18:** Monday Schedule | |
**Feb 25**: Mapping                              | Data cleaning exercise               |
**Mar 04**: Finding patterns with maps           | Map exercise, <br />Storyboard (community profile)  |
**Mar 11**: Charts, Visual Encoding              | Map exercise 2, <br /> Pitch (data driven story)   |
**Mar 18**: Presentation, Navigation, Bootstrap  | Chart exercise                  |
**Mar 25**: Completeness, Advanced Chart Layout  | Chart exercise 2, <br />Storyboard (data driven story)|
**Apr 01**: Building forms, Writing surveys      | Rough Draft (community profile)      |
**Apr 08**: Spring Break |  |
**Apr 15**: Community Study critique             | Survey exercise, Final  (community profile)  |
**Apr 22**: Command line tools, CSVkit           | Revised survey exercise, install CSVkit              |
**Apr 29**: Show your work, publishing numbers   | Rough Draft (data driven story)      |
**May 06**: Hands on TBD                         | CSVkit Excercise, Final (data driven story)  |
**May 13**: Data Driven Crit, Hands on TBD       | Revisions Community Study            |
**May 20**: Wrap Up                              | Revisions Data Driven                |


| Project              | Pitch  | Storyboard | Draft   | Final  | Revision| 
|----------------------|--------|------------|---------|--------|---------|
| Community Profile    | Feb 11 | Mar 04     | Apr 01  | Apr 15 | May 13  |
| Data Driven Story    | Mar 11 | Mar 25     | Apr 29  | May 06 | May 20  |
 

**Course outcomes**  
This semester you'll learn to:

+ Compose forms that gather the data you need from respondents.
+ Work with data from a variety of sources for use in reporting.
+ Identify new data sources to help you understand your own audience better.
+ Understand the context of the numbers you're working with.
+ Edit and organize data while maintaining its integrity.
+ Use basic statistical methods to summarize data.
+ Recongize and evaluate patterns in data.
+ Write basic SQL queries.
+ Use basic regular expressions for more powerful searches.
+ Design clean, compelling data visualizations.
+ Apply the fundamentals of effective visual communication to data driven-presentation.
+ Identify the elements that make a particular data driven project successful.
+ Skim technical instructions for examples you can use.
+ Ask for help when technology challenges you and the manual is too dense.
+ Prepare for and adapt to an ever-changing landscape of software tools.

The skills we build in this course will be as applicable to reporting as they are to the work of interpreting signals from your audience. 

## About the Faculty

**Amanda Hickman** works at the intersection of journalism and civic engagement, and especially values reporting that makes it easier for individuals to participate in democratic processes. As program director at DocumentCloud, she helped reporters around the world analyze, annotate, and publish primary source documents. Amanda managed development of a series of games about public policy issues as Gotham Gazette‘s director of technology. She has spent more than a decade reporting on local and international events and working directly with community based organizations to understand, and draw their membership into, the political process. Amanda has taught at Columbia Graduate School of Journalism, NYU’s Gallatin School and CUNY Graduate School of Journalism.

## Software Requirements 

We'll be using a handfull of [free](https://fsf.org/) and open source software tools this semester and a few that are just free of charge: 

* [Tabula](http://tabula.nerdpower.org/) allows you to extract structured data from PDFs
* [Open Refine](http://openrefine.org/) is indispensable for cleaning messy data
* CUNY recommends Fetch for FTP, but we're going to use [Filezilla](https://filezilla-project.org/) 
* [Firefox](https://www.mozilla.org/en-US/firefox/new/) is indispensible, as is the [Web Developer Toolbar](https://addons.mozilla.org/en-US/firefox/addon/web-developer/) add on. 
* [Python](https://www.python.org/) ought to be installed on your computer already. We'll use it to install [CSVkit](http://csvkit.readthedocs.org/), a command-line tool that lets you investigate data in comma delimited text files. 
* [Mou](http://mouapp.com/) is a handy cost-free OSX app that makes basic HTML markup easy, without tempting you to get fussy with layout. Linux users can get much of what Mou offers from [ReText](http://sourceforge.net/projects/retext/), which is free. 

You [should](http://tech.journalism.cuny.edu/documentation/software-installation/) already have [TextWrangler](http://www.barebones.com/products/textwrangler/) and Excel installed. You'll need both. If you don't have Excel, you can also use [LibreOffice Calc](http://libreoffice.org/) for all our spreadsheet work. 

You will need to create accounts on [JS Fiddle](http://jsfiddle.net), [CartoDB](http://cartodb.com/) and [Stack Exchange GIS](http://gis.stackexchange.com/). *Important!* Before you create your CartoDB account, make sure you have the information you need to get the student discount. Their standard free option is not adequate to our needs and upgrading is much more difficult than using the discount in the first place. 

## Major Assignments

Students will work in pairs to complete two major assignments. In addition, regular homework exercises will reinforce skills we've learned in class.

Assignments will be timed to allow you to dig deeper into your work in Information and Communities and your reporting course. You will complete two major assignments: one a community profile, the other a reported data-driven story. Students will work in pairs on the two major assignments and will develop a compelling pitch, a clear storyboard, a comprehensive rough draft and a complete final piece for each. 

### Community Profile Guidelines

We have ready access to rich and varied data about communities of all shapes, whether those communities are joined by geography, interests, heritage, age or a combination of all of those. We'll use that data add quantitative understanding to what you already know about a community. 

Students will work in pairs to compile a portfolio of data about a single community, based primarily on publicly available data, though where appropriate students are welcome to incorporate proprietary intelligence. Identify at least eight salient characteristics (is income relevant? educational attainment? is this community anchored in a single location or geographically dispersed?) and points of comparison (neighboring communities, for instance, in the case of a geographically-based community), and find data to quantify those characteristics. 

Your final product will be a short report that describes the community in numbers and puts those numbers in context. 

### Data Driven Story Guidelines

Just how many hospitals have closed in New York State in the last two years? Where were they and who was impacted? Do low-income New Yorkers have better access to fresh produce than they did ten years ago? Can they walk to green markets? Where are the most dangerous intersections in New York City? How many of them are near schools? These are all examples of questions we can answer with data that is already accessible to the public. 

For the data driven story, students will work in pairs to identify newsworthy data, pitch and report a story of no more than 600 words that includes at least two visualizations of that data. The story should have news value and the reporters should demonstrate a clear understanding of the data and its limitations. Students should speak with as many experts as necessary to write responsibly about these numbers. 

|


## Absences and Tardiness

Participation and attendance are required and are important to your success in the class. This is a fast moving, skills based class. We'll be tackling new tools every week and it will be very, very difficult to get caught up if you miss class. 

Please be on time for class and back to class from breaks.     
 
## Grading

 Your grade is determined by three factors: active participation in class, homework assignments, and the two major team assignments. 
 
| Course Grade Overall |       | 
|---|---|
| Participation        |  20%  |   
| Homework assignments |  20%  |
| Community Profile    |  30%  |
| Data Driven Story    |  30%  |

 Grades for your two team assignments are further broken down as follows:

| Assignment Grades | |
|---|---|
| Pitch        |  25%  |   
| Storyboard   |  15%  |   
|  Draft       |  25%  |   
| Final        |  25%  |   
| Revision     |  10%  |   

This means that if you complete a brilliant story or profile but don't put real effort into your pitch or rough draft, you can't get better than a C on the story.

 **Pitches:** <a id="pitch"></a> A complete pitch should tell me who cares, why we care now, and what pre-reporting you’ve done. You must include:

 + a proposed title or headline  
 + a story slug -- up to three words that capture the essence of your story
 + a list of the story's key elements  
 + a news hook, or explanation of why this story matters now  
 + a description of and link to the data (which means you have to find your data!)  
 + For your reporting piece: one source you have already spoken with or at least three potential expert sources and your plans for reaching them
 + For your community profile: propose at least ten data points you'd like to work with and explain why each is relevant.

 **Storyboards:** <a id="storyboard"></a> A storyboard organizes your content conceptually and spatially. This semester, when you turn in storyboards, you should also include a revised pitch and a proposed nut graf. Your nut graf will change your story develops, but it should capture all of the main elements of your story. 

 We use wireframe and storyboards interchangeably here. We’re looking for a simple sketch (on paper, in Word, or PowerPoint, Illustrator, or any number of online storyboarding tools) that shows us how you intend to integrate your visualizations, words, and navigation elements. Use simple boxes to tell us where your different elements will be positioned in a design, and how a user will navigate through the content. Check out [Mark Luckie’s thoughts on sketching/storyboarding](http://www.mediabistro.com/10000words/the-importance-of-sketching-and-why-you-should-be-doing-it_b837), with examples, from 10,000 Words. 

 **Rough Drafts:** <a id="roughdraft"></a> A rough draft does not have to have the polish of a final project, but it should be close. You should have created the visualizations that you plan to use. Your classmates should be able to evaluate a rough draft on its merits, without a guided tour of forthcoming features. A complete rough draft includes: 

 + Clean data in spreadsheets, already normalized, sorted, manipulated  
 + Visualizations of the data with labeled axes  
 + Captions  
 + Credits  
 + A headline  
 + For your reporting piece: at least three links to other reporting that puts your story in a broader context.  
 + Introductory text that includes information gleaned from at least one human source.  
 + For your reporting piece: A source list


 **Final Story:** <a id="finalstory"></a>Your story must be uploaded to digital storage. Post an excerpt and a link to the class blog.  

## Plagiarism and Copyright

 It is a serious ethical violation to take any material created by another person and represent it as your own original work. Any such plagiarism will result in serious disciplinary action, possibly including dismissal from the CUNY J-School. *Plagiarism* may involve copying text from a book or magazine without attributing the source, or lifting words, code, photographs, videos, or other materials from the Internet and attempting to pass them off as your own. Please ask the instructor if you have any questions about how to distinguish between acceptable research and plagiarism.

 In addition to being a serious academic issue, *copyright* is a serious legal issue.

 Never "lift" or "borrow" or "appropriate" or "repurpose" graphics, audio, or code without both permission and attribution. This applies to scripts, audio, video clips, programs, photos, drawings, and other images, and it includes images found online and in books.

 Create your own graphics, seek out images that are in the public domain or shared via a creative commons license that allows derivative works, or use images from the AP Photo Bank or which the school has obtained licensing.

 If you’re repurposing code, be sure to keep the original licensing intact. If you’re not sure how to credit code, ask.

 The exception to this rule is fair use: if your story is about the image itself, it is often acceptable to reproduce the image. If you want to better understand fair use, the [Citizen Media Law Project](http://www.citmedialaw.org/legal-guide) is an excellent resource. </a>

 When in doubt: ask.   

# SYLLABUS in DETAIL <a id="detail"></a>

 **Festival of Data:** Every week one student will choose a data driven story to present in class. Prepare to discuss the strengths and weaknesses of the story, the authors’ use of data as well as their use of interactivity, and to identify the underlying technology. Blog your story in the "Festival of Data" category by 5 PM on your week.

 **Weekly Reading:**  

 + Read Kevin Quealy’s blog, ["Charts and Things"](http://chartsnthings.tumblr.com): <http://chartsnthings.tumblr.com>
 + Read [Source](http://source.mozillaopennews.org/en-US/learning/), Knight-Mozilla's blog on code and journalism <http://source.mozillaopennews.org/en-US/learning/>  
 + Read Marketing Sherpa ([Email Subscription](http://www.marketingsherpa.com/newsletters.html))

 *Due Week 01:*  <!--deets-->
 Read: [Searches for "sundown" on Yom Kippur](http://www.washingtonpost.com/blogs/wonkblog/wp/2013/09/13/this-is-an-awesome-chart-about-yom-kippur-really/), [Homicide Watch intervew](http://contentsmagazine.com/articles/homicide-watch-an-interview/), [Homicide Watch on Search Queries](http://www.poynter.org/latest-news/mediawire/149294/homicide-watch-d-c-uses-clues-in-site-search-queries-to-id-homicide-victim/)

### Jan 28 | Week 01: Defining and Finding Data  
 Discussion: Welcome and Expectations  
 What is data, what are data stories? 
 How does data provide context? What can't data answer?
 Discussion: How does data help you understand a community?
 Discussion: Finding data  
 Festival of Data: ["In Climbing Income Ladder, Location Matters"][4]  

 *Due Week 02:*  <!--deets--> 
 Pre-pitches: Identify three datasets that interest you. Write a short blog post that describes the provenance of the data (who maintains it?), where the data can be found (include a link) and in less than 200 words each, explain why the data is interesting. This can be data that gives context to the community you're working in, or data that is worth doing some reporting on. Post these pre-pitches to the class blog. 

 Make sure that [Firefox](https://www.mozilla.org/en-US/firefox/new/) is installed on your computer, with the [Web Developer Toolbar](https://addons.mozilla.org/en-US/firefox/addon/web-developer/). Install [Tabula](http://tabula.nerdpower.org/), Create an Academy account with CartoDB -- start from <http://cartodb.com/academic> to get the education discount. You will not be able to do the necessary work in this class without an "Academy" CartoDB plan.  

 Read Cairo: The Functional Art, Reading part 1: pages 25-31, 36-44, on thinking through a visualization as a tool for the reader; what graphical form best serves the goal? On e-reserve in the Library

 Read [The Perils of Polling Twitter](https://source.opennews.org/en-US/learning/perils-polling-twitter/)

### Feb 04 | Week 02: Visual Encoding, CSVs, Pivot Tables  
 Discuss homework: Problems, challenges, solutions  
 Discuss: Visual Encoding, Story expectations  
 Hands-on: Tabula and Pivot Tables    

 *Due Week 03:*  <!--deets-->
 Spreadsheet exercise, Pitch your community profile, Make sure [Open Refine](http://openrefine.org/) and [Filezilla](https://filezilla-project.org/) are installed on your computer.

### Feb 11 | Week 03: Cleaning data, SFTP, Pitch  
 Hands-on: Basic HTML and moving files with SFTP
 Hands-on: Cleaning data with OpenRefine
 Workshop Community Profile pitches: are these the right data points to consider? What else would you wan to know to understand this community? 

 *Due Week 04 :*  <!--deets-->  
 Open Refine exercise, make sure you have [TextWrangler](http://www.barebones.com/products/textwrangler/)  installed. [Map reading](http://vis4.net/blog/posts/choropleth-maps/) 

### Feb 18 | No Class
 No class. CUNY will meet on a Monday schedule.

### Feb 25 | Week 04: Mapping  
 Discussion: Asking good questions
 Discussion: Limitations of maps, impact of mapping choices
 Hands-on: CartoDB, PostGIS

 *Due Week 05:*  <!--deets-->
 Mapping exercise, Pitch 2, Readings: Steele and Iliinsky, _Designing Data Visualizations_ Chapter 4: Choose Appropriate Visual Encodings (in Library); Cairo: _The Functional Art_, Reading part 2: pages 118-129, on Cleveland & McGill’s perceptual accuracy

 ### Mar 04 | Week 05: Finding patterns in geospatial data
 Discussion: Review Maps, Maps as Research
 Hands-on: Troubleshooting map exercise;
 If we get there: Advanced GIS queries

 *Due Week 06 :*  <!--deets-->
 Storyboard (Community); Mapping Exercise #2; 


### Mar 11 | Week 06: Charting, Pitch (Data Driven Story)  
 Discussion: Pitches, Visual Encoding  
 Hands-on: Making charts  
 Workshop Data driven story pitches: is this interesting? Is this the right angle? What would make this story something you'd like to read?

 *Due Week 07:*  <!--deets-->
 HighCharts exercise, 
 Read Cairo: The Functional Art, Reading part 3: pages 73-86, on presentation;

### Mar 18 | Week 07: Presentation, Navigation  
 Hands-on: Using Bootstrap templates
 Hands-on: Putting a Highcharts function in an HTML page  

*Due Week 08:*  <!--deets-->
Highcharts exercise 2, Storyboard (data driven)
Read selections from Tufte, Quantitative Display of Information, on e-reserve in the Library: pages 91-105, 176-190.

### Mar 25 | Week 08: Completeness, HighCharts API  
Hands-on: Highcharts API
Hands-on: Redesign exercise

*Due Week 09:*  <!--deets-->
Rough Draft (community)

### Apr 01 | Week 09: Forms and Surveys
Discussion: Polls, samples and surveys
Writing questions people will answer, getting data into and out of a data store

*Due Week 10:*  <!--deets-->
Final Story (Community), Survey excercise

### April 8
No class. Spring break.

### Apr 15 | Week 10: Community Study Critique
Workshop: Surveys -- too many questions? Too few? Would you answer these? 
Workshop: Community Study  

*Due Week 11:*  <!--deets-->
Revised survey exercise, install CSVkit

### Apr 22 | Week 11: CSVkit and Command Line Tools
Hands-on: Regular Expressions and CSVkit to work with big text files


*Due Week 12:*  <!--deets-->
Rough Draft (data driven story), install MySQL query browser
-
### Apr 29 | Week 12: Command Line Tools  
Hands-on: Regular Expressions and CSVkit

*Due Week 13:* <!--deets-->
CSVkit exercise, Final story (data driven)

### May 06 | Week 13: Infographics  
Discussion: infographics for print and web
Hands on: infographic redesign

*Due Week 14:*  <!--deets-->
Revisions to Community Study
Infographic exercise

### May 13 | Week 14: Story 2 crit, Hands on TBD  
Hands on: we'll take stock of how much we've learned and either go deeper on a tool you'd like more of, or tackle a new tool.  

*Due Week 15:* <!--deets-->
Revisions to Data Driven Reporting

### May 20 | Week 15: Wrap Up
Discussion: closing thoughts  
Fill out student evaluations

