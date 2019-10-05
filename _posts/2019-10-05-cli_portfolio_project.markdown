---
layout: post
title:      "CLI Portfolio Project"
date:       2019-10-05 15:13:08 -0400
permalink:  cli_portfolio_project
---


I'd have to say that the most difficult part of the project was choosing the site to scrape. All of my initial ideas (Fantasy Flight Games, local movie theaters, Fathom Events) relied too much on javascript to get all of the information from them that I'd need. So, after a google search for camera gear sales, I wound up on the Lens Authority deals page.

A quick inspection led me to the conclusion that I'd finally found a viable site.  I jotted down some notes about how I wanted the layout of the CLI, then got to work. 

The first thing to do was set up both my Scraper class to get the information and the Item class to store that information. The Scraper class took care of getting the initial item info from the main list on the site, as well as gathering further details from each item's page on the main website. While I didn't specifically write any tests, I compared the results of each method to that of the website to make sure that I was getting what I expected.

Once the Scraper and Item classes were good to go, I created the CommandLineInterface class to get things up and running. I decided to use a number-based menu system to allow the user to navigate quickly. The 'exit' keyword to quit the program was used instead of a number to avoid any possible conflicts with further menus. This had the project usable, but it was still very bare bones and running kind of slowly.

The first fix I made was in the CommandLineInterface class, where I had the program calling the Scraper on the main site, then immediately scraping every single individual page to populate all of the item details right away. I changed it to only scrape the individual item page when the user wanted the information. I further improved that by only calling on the scraper if that item didn't already have its details.

One difficulty I had populatinng the item details was getting only the description of the item. Because of the way the site is set up, using css selectors only got me so far. There was always a portion that added information about 'What if the item is out of stock?', and many times there was a portion of text that included the purveyor's opinion on the item. I just wanted the description, so I split the text at 'What if the item is out of stock?' or I used regex to split the text at the opion portion of the text and only saved the description.

Another diffuculty was getting the information from the table on each item's page. As there weren't css selectors beyond tr and td, there wasn't a way to get more specific with them. I had to take all the text from the table and split it at the line breaks. Then, I had to enumerate over each portion to get the information in the correct place.

In the Item class, I expanded on the find_by_name method to search for an entire name or by keyword. The user can enter an item name. Then, if there is no exact match, the user's input is divided up into pieces and the method looks for items that contain at least one of the pieces.  Also in the Item class, I expanded the search_by_starting_price method to include all items whose starting price is lower than the user input as well.

Finally, I added color to improve the aesthetics of the program and also added a bit of functionality so that the user could return to the main menu by pressing 'b'. 






