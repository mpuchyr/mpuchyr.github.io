---
layout: post
title:      "Project Parts that I'm Most Proud Of"
date:       2020-02-25 22:01:02 +0000
permalink:  project_parts_that_im_most_proud_of
---


The two things that I'm proud to have figured out were parts of the Javascript and Rails Portfolio Project and the React Redux Portfolio project.

The first part would be the sorting method that I implemented in both projects, after it was given to me as a coding challenge during the Javascript and Rails project review. In the project, a movie quote guessing game, the reviewer asked me to sort the movie choices alphabetically. That was relatively easy, but I didn't want to leave it at that since there are a number of movie titles that begin with the word "the." So I decided to make the sort method ignore the "the" if it's the first word of the title. 

The code I implemented was this: 

```
const sortMovies = () => {
    moviesToGuess = moviesToGuess.sort(function(a, b) {
        let c = a.name
        let d = b.name
        
        if (a.name.split(" ")[0].toLowerCase() === "The".toLowerCase()) {
            let aName = a.name.split(" ")
            aName.splice(0, 1)
            c = aName.join(" ")
        }

        if (b.name.split(" ")[0].toLowerCase() === "The".toLowerCase()) {
            let bName = b.name.split(" ")
            bName.splice(0, 1)
            d = bName.join(" ")
        }
        

        if (c.toLowerCase() > d.toLowerCase()) {
            return 1
        } else if (c.toLowerCase() < d.toLowerCase()) {
            return -1
        } else {
            return 0
        }
    })
}
```

I modified it slightly for the React Redux Portfolio Project to ignore the "a" and "an" if a movie title begins with either of those words as well: 

```
            movies = movies.sort( (a, b) => {
                let c = a.title
                let d = b.title
                const firstWord = ["a", "an", "the"]
                

                if (a.title && firstWord.includes(a.title.split(" ")[0].toLowerCase())) {
                    let aTitle = a.title.split(" ")
                    aTitle.splice(0, 1)
                    c = aTitle.join(" ")
                }

                if (b.title && firstWord.includes(b.title.split(" ")[0].toLowerCase())) {
                    let bTitle = b.title.split(" ")
                    bTitle.splice(0, 1)
                    d = bTitle.join(" ")
                }
                

                if (c && c.toLowerCase() > d.toLowerCase()) {
                    return 1
                } else if (c && c.toLowerCase() < d.toLowerCase()) {
                    return -1
                } else {
                    return 0
                }
            })
```

The other project part that I'm proud of is showing a blurred movie poster background, which is part of my  movie archive React Redux Portfolio Project. I was trying to do everything with one component for the page that displays a movie's information, but to no avail. Finally, it popped into my head as a "duh" moment to write a separate component to display the background, imported into the display page component. From there, it was just a matter of styling everything with css.
