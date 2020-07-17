---
layout: post
title:      "Practicing the Basics"
date:       2020-07-17 17:31:22 +0000
permalink:  practicing_the_basics
---


This past week, one of the projects I've decided to work on was buidling a personal website from scratch. This particular website is meant to be a coding/professional portfolio, demonstrating past projects as well as linking to my professional profiles such as LinkedIn.

I decided that this would be a good project to practice the basics with. As such, I'll be using plain old vanilla html, css, and javascript. 

In the process of building, I looked up how to include videos on a website with html. Naturally, there is a video tag, which I had never used before. It's a fairly straightforward tag to use. You can specify height, width, and whether or not you want to have controls right in the tag, which looks something like this:

<video width="640" height="480" controls></video>

Then, before the closing tag, you specify the source with the source tag, as well as including a message in case the user's browser does not support the video tag:

<source src="myvideo.mp4 type="video/mp4">
Sorry, your browers doesn't support the video tag.

Altogether, it would look like this:

<video width="640" height="480" controls>
   <source src="myvideo.mp4" type="video/mp4">
   Sorry, your browser doesn't support the video tag.
</video>



