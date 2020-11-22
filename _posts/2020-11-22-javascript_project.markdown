---
layout: post
title:      "! JavaScript Project !"
date:       2020-11-22 05:22:51 +0000
permalink:  javascript_project
---


Hello 90’s kids!!! Remember TamaGotchis??? Great! Who doesn’t???
Ever wanted to own a corgi, but for some reason you can’t?
Well now you can have the best of both worlds!
My project is inspired by TamaGotchis and my corgi Anakin. You can adopt your own happy lil corgi and play with them until they grow up and have to leave to the big city to provide for the family!
As fun and as cute as this project came out, it took everything out of me. Once again I overestimated how hard this would be. I thought that after the smooth sailing of finishing up my Ruby backend in a day that the rest of the project would just flow. 
Spoiler Alert! 
I was wrong.
I think my biggest problems with this project were 
1. ORDER! Order matters. 
2. Getting things to show up the way I wanted to.
3. Having my frontend communicate with my backend.
4. typooooooossssssss
For starters I knew order was important, but I didn’t know where it was important. So I spent a good amount of time stressed out about my .js files trying to organize each function in the way I wanted it to go off, when in reality I needed to set up my sources correctly in my index.html. Once I figured that out my next problem was getting things to show up the way I wanted to. I couldn’t figure out why some of my divs were still showing up when I didn’t want to. The thing with JS is that you have to manually make things appear and disappear. My solution was just making seperate functions so that when one div was supposed to show up the other one needed to be “hidden”. The code for that was 
```
function newPlayer(){
   mainSection.innerHTML += newPlayerForm
   const newPlayerSubmit = document.getElementById("new-player-submit")
   newPlayerSubmit.addEventListener("click", loginNewPlayer)
   hideNewPlayerDiv()
}
 
function hideNewPlayerDiv(){
   document.querySelector("#newplayerdivy").style.display = "none"
}
```
So when I wanted the NewPlayer form to be added to the main section of my index.html then the other div in this case “#newplayerdivy” had to be hidden or marked as “none”.
My final problem was having my frontend and backend communicate with one another. For both of my classes I just needed to collect the value of what was being inputted in the form, then grabbing that value, and making that value the variable that is then saved into my fetch request so it can go back into my backend. Aside from those main problems, I can’t stress enough how important it is to double check your code FOR TYPOS because a lot of headaches and TIME could have been spared by just making sure everything was written out correctly. 
As hard as this project was, of course it was yet another learning experience and I feel so much more confident with my JS skills and the outcome of it was more than I could have ever expected it to be. 

