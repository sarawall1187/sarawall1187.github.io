---
layout: post
title:      " My Jewelry Store CLI project"
date:       2019-01-09 11:43:05 -0500
permalink:  future_title
---

I decided for my CLI project to choose something familiar for a domain model- I worked in retail jewelry sales for 11 years  before my venture into code started. So I figured if I understand anything in this world: its a jewelry store and the relationships between the collaborating objects that can be modeled. 

My CLI begins with greeting the user and asking the user if they would like to shop for jewelry or need a repair? Lets talk about the repair option first: I added in the repair method more to be cutesy. It doesn't do much right now besides add a time stamp for seven days from the current time...HOWEVER... I felt like adding this as even a simple function would leave room in the future for expounding upon this method and even other areas of the entire program. There is a lot of room for growth. Plus, in doing the time stamp for a repair, I learned about how to find my own Ruby Gem to require with my program to allow me to call DateTime.now + 7 to add seven days instead of just 7 seconds like the built-in Time.now would return. So it was cool either way.

Now, of course, the bulk of my program involves shopping for jewelry. Obviously thats the fun part! If shop is chosen on the start menu, the user is then directed to choose if they would like to shop for rings, necklaces, or earrings. As a defense against user error I allowed my user to input any of these words either singular or plural- because I myself as the developer found myself interchanging the two. I also defended against wrong input altogether by letting my user know if it was invalid and then looping the options back around to them. 

Once the user has chosen what category of jewelry they wish to view, a list of jewelry items available- defined by a short description of the piece- is returned. The user can select a piece by choosing the correlating index number. A longer description of the piece including a metal type, center stone description, and the price are then returned to the user. From there, the user can choose another category to view, choose to do a repair, or exit the program. All user input options were given a fail-safe to guard against invalid inputs and every menu will allow the user to get back to any options available to them. 

During this project, I learned a lot. But one of the things that stands out the most is I learned that I know more than I give myself credit for. And don't we all do that? This is the very first program that I have ever been responsible for creating, writing, and then implementing. My advice for others going forward is to do one thing at a time. After each step, check if it works. Meaning, check if the output you received is what you were expecting. Google your problems. And mostly, enjoy it! This was truly a more fun an exciting experience that I anticipated. It was very fufilling to see my code working and in action. So celebrate the small wins! 
