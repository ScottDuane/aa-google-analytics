# Google Analytics Walkthrough

## What is Google Analytics? Why should I spend 5 minutes to set it up?
* It is a web traffic tracking system built by Google that is completely <b>FREE</b>
* Just create an account and put a piece of JavaScript tracking code into your site and it will run with every page of your site
* Once inserted into your code, the code records how long they were on your site, what device type they used, the number of page views, where they came from, etc.

## The ABCs of Google Analytics. You should be able to determine:
<b>A:</b> How many companies/recruiters/hiring managers are visiting my site?<br>
<b>B:</b> Am I creating content that is aesthetically appealing and easy to use for recruiters? <br>
<b>C:</b> Do I need to improve my site to increase callbacks from recruiters?

## Comparing Full Stack Projects
For 6 weeks, we tracked students’ full stack projects and these were the results…
* The more applications a student sent out, the more website views it had that week
* Visitors are looking at your sites and staying on them for an average of 30-90 seconds
* Sites with easy guest login, awake dynos, and visually appealing sites have longer session durations (2 min+) and lower bounce rates (50%, which is a good thing!).  We’ve found correlation to shorter job search duration (limited data so far suggests ~23 days)
* Sites that are harder to navigate and take longer to load (dyno asleep, ~10 second page load) have a higher bounce rate (90%) and have a longer job search duration (60+ days)
* As of October 2016, we do not know why a large number of 0 second sessions show up in the data, skewing the bounce rates to appear higher than expected.  Also, keep in mind that your own visits to the site may affect the data.    

Google Analytics **does not** naturaly tell you who the person accessing your site is.  All information is anonymized bfore being displayed, so you can not view visits by IP or any other identifiable information. There are ways around that and we'll cover them ahead.

There are 3 parts to a Google Analytics account:
* Account: You should have only one of these;
* Property: The sites you'll register. If you have more than one site that you want to track, and you want to track them sepeprately, you should create two separate properties. **Each property has its own tracking ID and snippet.**
* View: The information that gets displayed to you. For example, if you have two site that don't need to be in different properties, you can instead create two views: one that displays data for curie.cats.com and the other for markov.cats.com. Make sure you always have one for "All Web Site Data", so you can have a broader picture of your site's usage.

Since our goal is to see how many of your applications are rendering clicks, we won't go fancy and will keep all of our site (FS, JS and flex projects) under one single property.

## How to Install and Set Up Google Analytics for your FSP/Javascript/Flex:
* [Watch This Video](https://www.youtube.com/watch?v=Va-b-K5oqYs) (Only watch up to 3:00)
* After registering your site, copy and paste the Google Analytics snippet to your site, **before the closing `</head>` on your page**. The snippet should be present in whatever page you want to track. This means that:
    * If it is a **static site**, meaning there's only one HTML file to it, just place it on that single file;
    * If it is a **dynamic site**, like a Ruby+React SPA, you should make sure your code is in a central file, like the `/app/views/layouts/application.html.erb`. DO NOT copy paste the code on every single HTML/jsx file, since maintaining it becomes a nightmare.
* See if you didn't break the site on your local. If all is fine, deploy!
* Example of a student's project with Google Analytics inserted into the code: [Example 1](http://imgur.com/a/PXwI4)
* The snippets executes asynchronously, so it won't impact your page's performance.
* For more help, you can check out the [official Google docs](https://support.google.com/analytics/answer/1008080?hl=en).

## Important interface pieces
Every time you land on the Google Analytics page, you will see an accounts list that has the page you just registered, as well as 4 tabs: 
* **Home**: Displays the accounts and sites you have;
* **Reporting**: The main reporting area, where are the graphs and stats are displayed;
* **Customization**: You can build customized reports from here. We will no be covering this section;
* **Admin**: Where you view the settings of your whole account (Account, Property and View).

## First things first: Testing your tracking code
Click on the **Reporting** tab. Then expand the **Real-Time** section and click on **Overview**. You will see how many people are on your site at that moment. Now pop a new tab and go to your site. You should now see yourself on Google Analytics (it might take no more than 10 seconds for you to show up):

**@@@@@ GIF @@@@@**


#### Note: After you start sending out applications, recruiters and hiring managers should be clicking on your material. If you notice no one is visiting your site, you may have the code snippet in an invalid location in your code.

## Analyzing your web traffic
### Audience overview, Acquisition overview, Behavior overview
* [Watch This Video](https://www.youtube.com/watch?v=xZbd_yEN5nE) (9:16)  
* As you start seeing numbers increase, it is important to know what these numbers mean:
    * Sessions- a group of interactions that take place on your website within a given time frame. For example a single session may contain multiple screen or page views.
    * Users- a user is a combination of a unique random number and the first time stamp. The first timestamp is the time of the first visit by a user or the time when the Google Analytics cookie was first set for the user.
    * Pageviews- A pageview is defined as a view of a page on your site that is being tracked by the Analytics tracking code.          * If a user clicks reload after reaching the page, this is counted as an additional pageview.
    * Pages/session- total duration of all sessions (in seconds) / number of sessions. Individual session duration is calculated differently depending on whether there are engagement hits on the last page of a session.
    * Bounce rate- the percentage of single page visits (or web sessions). It is the number of visits in which a person leaves your website from the landing page without browsing any further.
    * % new sessions- first time users visiting your website compared to visitors who have previously visited your site

## Case Study:
* A student added google analytics on her flex project during the time period of July 27-August 18, 2016.
* Her project was a video game stats website for Destiny. She shared the link on Reddit and it gained a lot of traction in the video game community resulting in the numbers you see below!
* Since her website gained such popularity, she was able to track many things about visitors to the website, where they were coming from, and how long they stayed on the site. She was even featured on GameRant. Check out her flex project [here] (https://destiny-data.herokuapp.com/#/?_k=jy5wf6).  
* Although most projects don’t attract this high a volume of users, this data may be useful to demonstrate how Google analytics is useful.

[Screenshot of her Google Analytics](http://imgur.com/a/KWL3h)

## A note on finding extra help
Back in 2013, Google launched the new version of Analytics called Universal Analytics (UA). The old one was the ga.js and is now flagged as legacy. All of Google's official docs for ga.js have a warning, but you might find older StackOverflow answers that are about ga.js. Make sure you're looking at the right version before trying to implement the answer you're looking at.