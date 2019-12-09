---
layout: post
title:      "Rails Portfolio Project"
date:       2019-12-09 02:23:22 +0000
permalink:  rails_portfolio_project
---


This project was a bit tricky for me, as I had been struggling a bit with Rails. 

I started off with the idea for a photoshoot scheduler where a user could sign up as either a model or a photographer, then making the photographer model have many models, and models have many photographers, with the join table being a photoshoot. 

After going along that path for some time, I realized I was overcomplicating things. This was especially true when I attempted to integrate omniauth into the project. It was at this point that I scrapped everything and rethought the project.

Instead of having a separate model for models and photographers, I instead went with just a 'user' model. Then, I thought about what other attributes that photoshoots have, which led me to 'start_time', 'end_time', 'comments', and 'location'. It was the location that could have many photoshoots, as well as many photographers *through* the photoshoots. Having stumbled upon this epiphany, I got to work again. 

Things were going smoother from that point, until I ran into timezones. I was using datetime select on the forms for the creating/updating of photoshoots. No matter how I tried to integrate time zones into the project, error after error just kept popping up. The most noticeable being the need to refresh a page *no less than 5 times* just to get changes to the time zone just to show up. And even when it did, time zones got screwed up elsewhere in the program.

It was after many struggles that a thought finally occurred to me: I didn't actually need time zones for program I was working on! All I needed was to let the user set a time. Before the changes, the time would automatically start with current time (which is why I thought I would need to use time zones). After a little digging into the how a datetime select works, I managed to use prompts to show the user what they were selecting on each dropdown list. Also with a little reworking, the date selection no longer started at the current time, which made things work better.

Once the datetime selection was tweaked, I finally had the program up and working the way that I wanted it to.
