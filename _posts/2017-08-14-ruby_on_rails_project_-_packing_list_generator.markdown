---
layout: post
title:  "Ruby on Rails Project - Packing List Generator"
date:   2017-08-14 02:54:07 +0000
---


Tonight I finished my Ruby on Rails Project.  I created a useful trip packing list generator.  One of the really enjoyable things about these project is that we get to pick something we wish we had.  This project really pulled together all that we learned so far.  My favorite part of the project was setting up the views.  I got a decent layout going with a nice nav bar that displays only what is appropriate and allows the user to sign in with Facebook if they so desire.  I utilized Devise with Omniauth which worked like a charm until it didn't.  I had tested it thoroughly and was able to sign in directly or via Facebook with no issues.  After days of hard work getting everything just right I thought to sign out and in just to double check and Facebook threw me an error.  I spent an afternoon trying to figure out what was wrong and it was a mystery.  Everything looked so RIGHT.  Finally I compared everything line by line with a previous Devise/Omniauth project and suddenly I noticed that one of the Omniauth files was slightly out of place.  Don't know how I managed to move it.  Moved it back and presto - worked like a charm once again.

I tried to add a lot of features but I can see that this is something I will want to keep adding to.  When the user creates a new packing list and add items they have the choice of selecting from existing item or adding new ones.  A feature I really liked is that while the user's previous items are displayed to choose from  - only items from a packing list for a trip in the same trip category is displayed.  Thus if you are going on a beach trip you won't be searching for items to pick in a list populated with skis, boots and poles.  If, like me, the user tends to pack the same stuff for beach trips or ski trips for instance, the items displayed to choose from will include all those items.  Handy!
