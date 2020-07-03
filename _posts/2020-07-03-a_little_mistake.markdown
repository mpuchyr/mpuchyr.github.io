---
layout: post
title:      "A Little Mistake"
date:       2020-07-03 17:44:30 +0000
permalink:  a_little_mistake
---


This past week I was experimenting with both React Hooks and API for IMDB. The overall goal was learn more about Hooks and working with data I did not personally create.

Unfortunately, an overlooked error in my code caused the app to continually fetch data. I'm not entirely sure where I went wrong, but I suspect it was a combination of how I had used hooks and called on the fetch request. As the app kept attempting to fetch data, the number of requests quickly balooned to an unmanageable number before I could pull the plug. 

As I was using a free API with a request limit of 500 per month, that limit was quickly exceeded, preventing me from making any more requests for this month. As it was the beginning of July when this happened, I now have to wait until August to continue to work on this particular application. 

The lesson that I took away was this: be a bit more careful when combining React Hooks with fetch requests.
