---
layout: post
title:      "Javascript and Rails Portfolio Project"
date:       2020-01-19 00:40:03 +0000
permalink:  javascript_and_rails_portfolio_project
---


Given the constraints of the project, I first decided to make a random movie quote generator that pulled from a prewritten list of movie quotes and movies. However, that soon evolved into a movie quote guessing game.

The first thing I did was write functions that fetched both the quotes and the movies, storing them in their respective global variables. 

For the quotes, I wrote a function to generate a random quote from the available fetched quotes. Following that, was a function to create the HTML that would be added to a container class for the user to see.

Once the quote is randomly chosen, a randomMovies function is called. Using the movie that the random quote is from, it used a while loop to randomly choose two more movies from the movies array to generate the choices for the user. Those movies are then shuffled with the shuffleRandomMovies function so as not to have the correct answer in the same place every time. Those choice are then used by the addMovieButtons function to generate the buttons that the user can actually click on to make a guess. Naturally, I had to use an addButtonFunctionality function so that the buttons actually did something when the user clicks on them.

From there, I made a function anmed gameStart that took the previous functions (except for the functions using the fetch requests) and executed them synchronously to set up the game. Within gameStart, I included and if else statement to encompass a game over eventuality. That game over state being running out of quotes or the user acquiring three strikes.

I also wrote a function, resetGame, that used the fetch requests and call upon the gameStart function. The resetGame function is called upon once the page loads, or when the user clicks on the reset button.

The program also allows the user to create a new movie quote and movie. In the backend, the user entered quote is looked up to see if it already exists. If it doesn't exist, then the program looks up the movie. If the movie exists, then the quote is added to the movie. If the movie doesn't exist, then both the movie and the quote are created. Once a user creates a quote, the quote is added to the database and the game is reset so that the newest quote and movie are added to the pool. 
