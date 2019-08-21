---
layout: post
title:      "Daily-Diary, A React Application"
date:       2019-08-21 21:54:18 +0000
permalink:  daily-diary_a_react_application
---


I really enjoyed this project. It felt girly and I was excited about the concept which always helps for motivation. Its a diary application that allows users to create an account and write daily diary entries. Pretty straightforward. 

I started with the good old `create-react-app` command and, boom, instantly I had the makings of my application. It comes complete with CSS filesa public folder for your index.html and all the node_modules that you should never touch or even look at. I backed it up with a Rails API backend for data persistance. I even went the extra mile and consumed an external API to render a "Quote of the Day" which is fun. 

React has a lot of great tools that you can easily install and import. I used `react-router-dom` to render new routes in the url even though I wasn't technically changing pages. I also used `react-bootstrap` to make styling a breeze. I used `react-redux` and `thunk` to store all of my application's state in one place. Biggest thing to know about Redux is for every action you need a reducer which has a built in method `dispatch()` you use to put it all in motion. Don't forget to add the reducer to your store you've created using the `createStore()` function. 

What I like about React is how lightening fast it is. Things happen in a literal instant. Its also very broken down so your code is well organized- you just may have to dig through a few files to find where that code you were looking for is again from time to time. The React Docs are awesome too, very well documented and straight to the point with good examples. 

Overall my experience with this project was fun and I learned a lot as usual. Connecting the dots seems almost impossible unless you are building it yourself. You can read until you're blue in the face and it won't click. So do yourself a favor and build a React app! 
