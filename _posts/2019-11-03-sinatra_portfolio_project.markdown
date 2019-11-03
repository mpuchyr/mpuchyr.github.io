---
layout: post
title:      "My Sinatra Portfolio Project"
date:       2019-11-03 16:32:17 -0500
permalink:  sinatra_portfolio_project
---


For this project, I decided to create something to keep track of a Lego collection. Why? Well, there just might be a number of lego sets scattered around my home... 

The basic part of the project was simple enough: creating the models for a User, a Lego, and a Theme. The User could have many lego sets, and the Theme could have many lego sets, but each Lego set could only have one User and one Theme. The User would have a username and password, and the Theme would only need a name. The Lego was a bit beefier, having a name, a number of pieces, a user id, a theme id, and an optional link to an image.

After those were in place, it was a just a matter of filling each route and creating the associated pages for them. I wanted to be sure that any given user could see everything, which is why I added place to view every set by all users, but didn't want them to be able to edit. I included that check on each lego page, so that the option to edit would only appear if it was owned by the current user. 

The interesting part was getting the errors to show up if, for instance, a new user tried to sign up with an existing username or they didn't fill in all the required information. Once I figured out how to get the error message, I added them to the session and redirected the user to the page they were just on. I used an instance variable to store the error messages from the session, then deleted those message from the session. In the layout page, I added a place to show the error message if there was one.

And I think that more or less sums up my Sinatra project.
