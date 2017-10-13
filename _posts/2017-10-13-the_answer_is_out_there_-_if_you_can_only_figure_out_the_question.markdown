---
layout: post
title:      "The Answer is Out There - If You Can Only Figure Out the Question "
date:       2017-10-13 21:40:01 +0000
permalink:  the_answer_is_out_there_-_if_you_can_only_figure_out_the_question
---

Just finished my Packing List Generator Rails App with JQuery Back End. I learned so much through this project and much of it was via extensive Googling for answers.  I have been amazed by the sheer volume of answers that are out there if you only know the right question to ask.  Often it is an answer you stumble across which you could have come up with much faster if you knew how to phrase the question better.  It is often an iterative process whereby you see something in an early answer that causes you to refine your question in a way that leads to a whole new line of questioning.  Detective skills are a real plus when looking for answers to programming issues.

A great example of this was my effort to bind listeners to dynamically created throughout my project.  For example, a list of trips which you can click on to take you to the appropriate trip packing list.  The links looked great but I could not get a listener to bind using $('id').on("click", function( ) { }).  Everything looked good but the event listener just wasn't attached.  I googled "event listener", "event listener missing", "problems with event listeners", etc.  Nothing.  And then somewhere in the bowels of one of the many stackoverflow pages I read I noticed one that mentioned DYNAMICALLY created elements.  That lead me to the pot of gold.  The more complete syntax of:
 
												$(staticAncestors).on(eventName, dynamicChild, function() {
												         // write code here
												});
												
Eureka!  I added a static element to contain my dynamically created elements and the problem was solved.  And I added another weapon to my aresenal of very useful syntax!
