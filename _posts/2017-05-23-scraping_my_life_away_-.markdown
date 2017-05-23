---
layout: post
title:  Scraping My Life Away -
date:   2017-05-23 00:58:42 +0000
---


As I sat down to write my CLI Application for my first assessment, I was nervous.  Rightly so, as it turned out.  What should I scrape?  That was the first hurdle.  It reminded me of playing the game where you have to think of something in a given category before the time runs out.  Your mind goes totally blank.  You can't think of a single thing in the category, despite the fact that at any given moment if the timer wasn't running you could literally think of dozens.  I thought "scrape something you would enjoy."  All of a sudden I had it.  Real estate!  I love real estate.  It is a lot like wall street.  A big market where buyers and sellers are trying to find that one price that clears the market.  And it's all about relative value.  To judge relative value, you need a lot of data.  Perfect!

I decided to have three classes:

1. CommandLineInterface - It is command central.  It controls the flow of the application, looks up the zipcode that the user supplies, invokes the scraper, creates house objects and prints out the listing information.
2.  Scraper - Finds all the properties available in a given zipcode by scraping the data from www.realtor.com.  It returns a hash of attributes and values to House for mass assignment to the House object that invoked the scraper.  If the user wants further information Scraper gets the property's detailed information off the page for that specific property
3.  House - Creates house objects with all the available information on the given property.  It only gets the detailed information if the user requests it and thus storing it because necessary.  

It seemed easy.  Until it wasn't.  I hadn't really thought about the fact that real estate listings are very fluid and there is a lot of inconsistency from house to house.  And the website I was scraping from, was also getting their data from elsewhere.  It was a stuggle to find a way to make the scraping process flexible enough to handle any situation.  But I learned a lot in the process. A few of my epiphanies were:

*  It was often easy to find the data by going deep enough in the html, but it was actually trickier to find the level above that that wasn't TOO deep so that it would include all the instances or features  and allow them to be grouped appropriately.
*  Sometimes you just can't get there from here.  Sometimes I could get specific information and assign it to an attribute, but sometimes I couldn't and had to use an array to hold that data.  The attribute was therefor a section array, where each item in the array was itself an array with two items in it: a section title (eg Garage and Parking), and an array of features in that  section.
*  It is as important to print it in a nice format as it is to get good information.  If it is unreadable, no one will want to see it.
*  There are a stunniing number of Gems out there that can do amazing things.  I used two:  **area** which took a 5 digit zipcode and returned the associated town and 2 letter state abbreviation and **table_print** which took data and printed it in a nicely formatted table.
*  I can't walk away easily from a detailed project like this.  I would think "Oh, I know what it is!  Let me try one more thing."  Before I knew it would be 11pm and I hadn't eaten a thing all day.
*  A corrollary is that I do my best thinking when I am not thinking about it.  I would finally stop for the day and the next morning in the shower the answer would come to me.  Maybe I should get a water-proof computer!

One thing that really hit home in this process was the importance of building data heavy websites in a well-laid out way.  If you don't step back and rationally lay it out, any modifications to it will be a nightmare.  Hopefully not my nightmare!  As a first attempt at a project like this I am proud of how it turned out.  Although I know that in the shower tomorrow I will think of a million things I want to do to make it better!



