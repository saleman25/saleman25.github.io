---
layout: post
title:      "My CLI Movie Project"
date:       2020-08-23 00:31:39 +0000
permalink:  my_cli_movie_project
---


Who would have thought I’d be able to get through this week! This project really tested me on how well I could do under pressure. 
I knew the hardest part for me would be picking a topic and setting up my IDE and to be fair those two little things took me a whole day and a half because I just couldn’t get the hang of setting up my IDE  and as a Libra I just couldn’t decide on what I wanted to do. However once I overcame that I knew I was going to be okay. 
I’d also like to say that it wasn't for the help of my cohort lead and being able to google my errors as well as being able to look back to our previous lessons, I think this project could have easily gone south. 
I did my CLI on movies, my original idea was to do movies and tv shows but the more I was coding the more I realized I was a little in over my head to be able to execute all of that cleanly and clearly. 
**API class**
I decided to do an API as opposed to scraping so I can have more control over the data I was receiving and not have to worry about things changing later on if I had chosen to use a scraper method instead. After finding a good API to use, themoviedb.org, I was able to retrieve the URL information that will allow me to output the top 20 most popular movies at the time. After having that down I set up a second method to help me retrieve individual movie overviews by using the movie’s ID code. 
**Movie class**
The movie class was probably the easiest part of my project because all I did was initialize a title and an ID code as well as have a second method that would assign the overview accordingly to each movie when it was called on.
**CLI class**
This was what I was excited about and where I knew I felt the most comfortable. I started off with the basics of having a welcome message and asking for a user to input whether they were ready to begin or not. From there I would list the movies and then I'd ask for input again if they wanted an overview of the movie they selected. This is where I ran into trouble because this is where I had trouble in my API class as well. In both classes, being able to retrieve the ID code and then be able to put it into the URL and have the URL give me an overview was very confusing for me and I had to keep playing around with different methods and variables to finally get the response I needed. All I can say is thank god for binding.pry! Once that was done I continued fixing the code so that all my bases were covered. Such as if there was a wrong input what would happen, or how long of a pause should there be in between messages. Once all the hard stuff was done, I had a little fun with my output messages. I tried to make it cute and fun the best I could do with what I knew. I didn’t want it to be plain so I added asterisk art into my messages. I know this isn’t needed for my project but it made it fun for me and it felt more personalized and more than just a project I had to do for school.

I truly learned so much from this experience and even though I did get overwhelmed and stressed out I had so much fun doing it and I hope whoever uses/sees it enjoys it just as much as I did creating it !

