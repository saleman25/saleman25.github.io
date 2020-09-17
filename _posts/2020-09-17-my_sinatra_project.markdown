---
layout: post
title:      "My Sinatra Project! "
date:       2020-09-17 21:56:12 +0000
permalink:  my_sinatra_project
---


Do you ever just see a dog and think “man i wish i had somewhere to write this memory down”? WELL NOW U DO 
For once, what I wanted to do came naturally to me. I love dogs and I immediately knew that I wanted to create a Sinatra App that had to do with dogs. Imagine twitter but JUST for dogs you see. 
I set up my migrations for both dogs and for the users, once that was established I created the relations that each model would have with the other, (has_many, belongs_to, etc). Easy enough. I wrote little notes on my views about what I wanted each erb file to do. My login page, my signup page, how I wanted the dogs to be displayed. Again, a little easy. When I started doing the controllers, I was scared I’d get confused because so much was going on, and I definitely did. The hardest part of this whole project was to make sure the controllers worked the way I wanted them to. 
I think the biggest errors I had was 1. Being able to edit an instance of a dog, and 2. User authentication. For the edit portion I had to go through so much trial and error to make sure it came out correct. The forms weren’t routing the way I wanted them to and when I finally submitted the edit form it wasn’t reading it correctly and sending me an error message. With alot of trial and error and help from my teacher I was able to figure out that the main problem was A TYPO and I forgot to add a value to my submit button. Once that was cleared up the next hurdle was the user authentication. I was able to input a username and a password, but 1. The password wasn’t being encrypted, and 2. If I signed up with another user with a totally different username, password and email, I was still receiving the data from the previous user. For the password I realized my error was that in the form where you entered “password” I had the value set to “text” instead of “password”. For my second error I didn’t realize I was returning all of the dog instances as opposed to returning the dogs associated with each individual user. 
Now that all my errors were cleared up and it was working the way I wanted it to, I could finally have fun with all the CSS. Coming into this I knew next to nothing about CSS and having to learn and teach myself was truly such a fun experience. I was able to put my personality into the project even more so than I did with my CLI project. Of course because I didn’t know what I was doing it did get a little annoying when things weren’t showing up the way I wanted to, but the more I read and played with font-types, font-colors, BUTTONS, and how to override some of the previous CSS that came with my browser, I had such a blast. 
The more I’m in this curriculum and the more I learn, the more I’m having fun no matter how stressed out I get, and I am so happy I’m finally doing something I love. 

