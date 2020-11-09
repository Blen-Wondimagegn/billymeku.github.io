---
layout: post
title:      "Kpop Rails Project "
date:       2020-11-09 01:58:15 +0000
permalink:  kpop_rails_project
---

For my Rails project, I decided to take my Sinatra project and add has_many through relationship elevate the  contents by adjusting them to fit the Rails frame work, on my previous project I had a user that  has_many  kpop groups and kpop groups belong to user associations. My Rails application is for Entertainment company to keep track of their Solo Kpop Artists and Glam Squads that belongs to the company and the Artists. My join model is the Glam model, which has a belongs to user and belongs to artist relationship and has attributes of its own that are only in the glams model(glam_squad, makeup, hair and wardrobe). The artists has many glams and has many users thought glams, and users has many glams and has many artists thought glams. 

Active Record is really good at managing complexity of our associations for us however, as I was working on this project there were some challenges. Here are a couple of issues I run into while working on this project that I thought were interesting and helped me understand the associations better, manly the has_many thought relationships portion. The first thing was creating a glams_squad for an Artist. Originally in my create method I had:
 def create   
      @glam = Glam.new(glam_params)
      if @glam.save
        redirect_to @glam 
      else
        render :new
      end
    end 

 To create new instance for the glam_squads, what happens with this was it takes in all the params but doesn’t create the instance. So I had to adjust the my code to look like this:
 
 @glam = current_user.glams.build(glam_params)

This line of code allowed me to create an instance for glam_squad for a specific user. This will return a new Glam object with the current user_id already set. build works just like new. So the instance that is returned isn't quite saved to the database just yet. You'll need to # save the instance when you want it to be persisted to the database.

The relation between Parent and child class goes deep as far as not leaving child class behind when you delete the parent class. When I attempted to delete Artist which has Glams associated with it as a child I used the following code which was giving me errors:

def destroy
      @artist.destroy
      flash[:notice] = "Artist deleted."
      redirect_to artists_path
    end
Adding has_many : glams, depenent: :destroy to my Artist model fixed my issue with the delete method. 

Over all I enjoyed working on this project as it let me explore my own unique ideas and incorporate them in to my application. 








	I

