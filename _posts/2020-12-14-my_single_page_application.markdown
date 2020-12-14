---
layout: post
title:      " My Single Page Application "
date:       2020-12-14 05:40:35 +0000
permalink:  my_single_page_application
---

As we are approaching the end, all the different projects we have done are slowly coming together. I am looking forward to diving deep into JavaScript as it is a complex topic and is used it to add interactivity to a website. For my JavaScript and Rails project I have decided to take my Rails project and extend it as we are required to have JavaScript as frontend and a backend API that I build with Ruby and Rails. As far as relation I have one Artist: has_many glams and Glam: belongs_to glams association. 

I have got to say the tricky part was getting the right response when using fetch dealing with respond and request. There are a couple of issues that I came across: understanding the concept of CORS and setting Rails routes correctly matching the fetch request to get a Promise that resolves to the Response to that request. Another thing I have noticed was the importance of rendering. While the data was working exactly how I wanted it to in the rails console, I was having problem with it when I run Rails server, what I mean by that is that I was trying to access my index page for glams class, but I was getting error where it only displays glams with [“id”, 1] which was not the ideal data due to the fact that I was excepting it show all the glams and it is nested with artist like so: 

resource :artists do
     resource :glams 
end 

resource :glams 

 I was expecting the following line to be valid to look up all the glams for an artist => /artists/:artist_id/glams, only it was not, it was showing glams/1 [LIMITE, 1] error, I had realized it was because I was missing => render json: @glams in my index route in my glams_controller.
 
 Because of the above error I was having another error on my frontend in my  fetch() method to get nested routes as well, it was promise failed. It took me a while to figure out that my fetch was not working because my route was not correct, because I had worked with nested routes in my previous project I had assumed the problem was with my frontend, but I was wrong. So, it is important to check on your data and routes on your backend first before fetching any information.




