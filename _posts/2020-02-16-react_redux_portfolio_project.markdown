---
layout: post
title:      "React Redux Portfolio Project"
date:       2020-02-17 04:22:36 +0000
permalink:  react_redux_portfolio_project
---


The idea that I had for this project was a movie archive app, where the user could enter a title, synopsis, image-link, and genre or browse movies that had been previously entered into the archive.

The first thing I did was create a Home container component. At first, it would fetch all of the movies from the rails api backend and display the posters of all the movies. 

Going from there, I created a MovieShow container component to display the title, synopsis, and larger image of the movie's poster. I wanted the background of this component to be a blurred image of the film's poster. To do that, I had to create another component which I named MovieShowBackground. I sent the movie's id and all of the movies (found in MovieShows props) to the MovieShowBackground. The MovieShowBackground sorted through the movies, much like the MovieShow component itself, then created a div containing an img whose source was the movie's poster url. 

From there, I made another container named AllMovieShow. This component fetched all the genres and movies from the database. From there, it sorted the movies by genre and title. AllMovieShow displayed the movie posters that would link to each movie's show page, which I named MovieShow.

The most difficult part was implementing the ability to edit a specific movie, since this component required its state to be set with the movie's information as well as updated. After much trial and error, I discoverd that I need to call the fetchMovies action in componentDidMount(), then (inside a .then block) call this.setState() to actually set the state properly so that it could be manipulated.

Styling the project was pretty interesting. To get it exactly how I wanted it, I had to look up how to create a fixed navigation bar and a scroll to top button that appeared only when the user scrolled past a certain point.
