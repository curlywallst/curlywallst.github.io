---
layout: post
title:  "My Virtual Wine Library"
date:   2017-06-30 14:20:44 -0400
---


I find that the hardest part of the opened ended projects is always deciding what application to make.  Much like when writing a paper I always thought the hardest thing was the first sentence.  I think that in general it is always best to choose something you are passionate about so for my MVC Sinatra application project I decided to create a vitual wine cellar.  An owner can signup for a secure account and enter each bottle in their collection to their virtual cellar.  Information about each bottle includes wine type, winery, year and price paid.  While each owner can view all the bottles in the overall universe they can only edit those in their own cellar.

One of the interesting aspects of object oriented programming is that it really makes you stop and think about how a given object really SHOULD behave.  For instance should a given owner be able to edit a winery name since wineries can be shared by many users?  I think not.  And since it is my project I get to be the object god and make all the decisions, right?  Well of course, yes, but in the end the customer is always right.  If you make the best application in the world and no one ever uses it, what's the point?  I tried to spend a good amount of time thinking about how to make my application useful by many.  Of course each user would want to be able to add, edit and view their bottles - but they also want to DRINK them so they need to be able to delete them as well!

I appreciate how this project helped me really think about CRUD - I had to admit that that pretty much sums things up.  There is not much else to do as all actions fall into this one small mneumonic.  Same goes for views.  New, edit, index, and show, if written in a general enough way, they can pretty much handle everything.  I kept trying to add more views like all the bottles in the universe - then stopped myself - it is just a bigger index than the personal cellar index.  It was not the VIEW that was different, but what was being sent to the view.  

In some past projects we put all the logic in app.rb or in app/application_controller.rb, but here again I really learned the importance of having several controllers and separating out the logic for each.  It makes it much cleaner and easier to work with.

I learned a lot from this project and hope to continue to modify it and actually use it myself going forward!
