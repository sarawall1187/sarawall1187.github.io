---
layout: post
title:      "Connecting the dots, Understanding AJAX "
date:       2019-07-11 17:07:33 +0000
permalink:  connecting_the_dots_understanding_ajax
---


AJAX IS SO HARD. No like really. I would say I have pretty good reading comprehension, and I have never felt like I had no idea what I had just read until I got to this section of the curriculum. I was terrified to begin this project. I didn't even know where to start. 

Well I started with some YouTube videos (thanks, Cernan!). That got me off the ground. First logical step: change your controller action to respond to a JSON request when its made. Then move on over to your JavaScript file. Make sure you can actually hijack the event you want to takeover via AJAX before getting too far. That can be a challenge all on its own. I like to use an alert versus console.log-ging because its real nice and obvious when it pops up in your face that it worked. Once you get the listener working, time to make the request to your API endpoint- your controller action. I used Fetch which is a JavaScript promise for this. Convert that response to JSON data using the handy .json() function!

Whew, halfway there to rendering a get request dynamically! Once we get our converted data, I moved over to build a constructor function so I could use that data to make objects. Then it made sense to go ahead and build a prototype function so I could format the HTML on the page once my object was made. Last step is to just append it to the DOM- WAT? Meaning, make it show up on the page! Grab an empty div and use the append() or html() functions to insert it into the div. 

This was harder than this blog post makes it sound. But considering I didn't even fully understand what AJAX was when I started, I feel about 90% more confident in my understanding of it now. Being forced to debug and work through the problems I feel like is a huge benefit for me this go-round. I'm looking forward to a career in coding the more about it  I learn.
