---
layout: post
title:      "Sinatra Project K-pop Group"
date:       2020-10-12 01:33:09 -0400
permalink:  sinatra_project_k-pop_group
---


On this project I was able to see the concept of basics of Ruby and ORMs,Activerecord come together in real time. What makes this project interesting is that Sinatra development framework lets you develop all sort of applictions in a simple way that could be easily understood.When Bulding my Application I have used Model View Controller architecture. It has a few simple models that interact with various routes in the controller which then composes and serves the different pages through the views. My model  includes Users which would write and edit groups, which would in turn have many kpop_groups. All KpopGroups belong to a User, so you can easily list all of the kpop groups. Sinatra has a unified router and controller. In my controller I used a separate controller for each model which helped organize all the different routes and actions. In my views directory I applied Embedded Ruby to dynamically generate html web pages and serve requested content. Each views correspond to the routes/actions in the associated controllers, so there are views for showing diffrent pages to render  by using route/action .
Here is my File Structure for my application.
```

├── CONTRIBUTING.md
├── Gemfile
├── Gemfile.lock
├── LICENSE.md
├── README.md
├── Rakefile
├── app
│   ├── controllers
│   │   ├── application_controller.rb
│   │   ├── Kpop_groups_controller.rb
            ├── session_controller.rb
│   │   └── users_controller.rb
│   ├── models
│   │   ├── Kpop_group.rb
│   │   └── user.rb
│   └── views
│       ├── index.erb
│       ├── layout.erb
│       ├── kpop_groups
│       │   ├── new.erb
│       │   ├── edit_tweet.erb
│       │   ├── show_tweet.erb
│       │   └── show.erb
│        ─── sesstions
│				 			└── signup.erb
│ 
│       └── users
│           ├──login.erb
│      
│           
├── config
│   └── environment.rb
├── config.ru
├── db
│   ├── development.sqlite
│   ├── migrate
│   │   ├── 20151124191332_create_users.rb
│   │   └── 20151124191334_create_kpop_groups.rb
│   ├── schema.rb
│   └── test.sqlite
└── spec
    ├── controllers
    │   └── application_controller_spec.rb
    ├── models
    │   └── user_spec.rb
    └── spec_helper.rb
```
