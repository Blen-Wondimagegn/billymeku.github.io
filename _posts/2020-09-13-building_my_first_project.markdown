---
layout: post
title:      " Building my first project "
date:       2020-09-13 09:15:26 +0000
permalink:  building_my_first_project
---

Building my first App 
Starting out this week working on my first project was a bit overwhelming and difficult for me due many reasons. I am going to be sharing the process and how I overcame some of these issues. As far as getting data from a website, I decided to go with scraper.  
First, I had a hard time finding a website that was interesting to me and at the same time had valuable information for me to work with or enough data to scrape. I am not going to lie, it took me several hours to find the right website. After hours and hours of searching, I am came across this website :

https://www.amnh.org/exhibitions/permanent/planet-earth/how-do-we-read-the-rocks/three-types. 

The first thing you would say when you see this website is that it is neat. I liked this website because the concept of Geology and rocks has always fascinated me, and the information it contained was short and precise. 

Here are some steps I followed before starting my project:

 1. After carefully looking through the website, I made a list of things that could possibly be used as a menu(look for lists).
 
 2.If you are going to go with Scraper, I highly recommend experimenting with this
         https://repl.it/@TheGingertonic/ScraperChecker.
				 
 3. As it is my first project I focused on implementing all the lessons I have learnt and understanding how object relation works.
   
 4.To get more idea about opprating cli and scraping this video help me out a lot https://www.youtube.com/watch?v=KwBMwZ89Hj8&list=PLc6AmvC5Zybybc-NjUUwQwTtUEXH4iB2s&index=2&t=
 
My cli project is a database for the three rock types,It contains bin and lib directory, the bin directory is where I actually run my ruby file. In my lib diectory I have my cli,scraper and rock files. In my cli file is where I interact with the user using a menu that loops until the user wants to exit. The most challenging part of my project was executing the menu method that I had in my cli class inside the lib directory. So the issue that Iwas having was that I was able to grab all the right data from the website and display that data but when it comes to picking a specific option It didn’t that is where .all + my rock class (Rock.all) came in handy. Next I was having a hard time looping through my menu method still but I finally figured it out with( loop do).
