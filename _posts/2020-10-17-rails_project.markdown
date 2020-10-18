---
layout: post
title:      "Rails Project!"
date:       2020-10-18 02:23:22 +0000
permalink:  rails_project
---


This project was an uphill battle from beginning to end. I created  App where you can store Trips as well as potential Trips. So in retrospect a passport app that allows you to input a country and city and the details of the trip and then allows you to "stamp" it if youve been or if its just somewhere you would like to go.
I think my downfall was thinking that I wasn’t going to encounter any errors. 
My main problems were: 
1. I didn’t know how to associate my models with one another and set up a join table. 
2. Omniauth 
3. Nested Routes

So let’s unpack this a little. After my two previous projects, I’m starting to get used to the github setup and I knew to start off my project I had to do rails new. From there I created my three migrations: users, vacations, and locations. I set up the basic CRUD functions for the models, has_many relationships, and logging in and logging out. THIS IS WHERE I GOT CONFIDENT. The more I started coding I realize my relationships didn’t make sense because location just had one option for a country and it just wasn’t making sense. So I had to reset my database with rake db:reset and delete my schema and start over, and went with a visit model that had a boolean option of have_you_visited_before. Since this was giving me a headache I decided to leave my nested routes for last, yet another slip on my part. I started my Omniauth setup and to be fair, I don’t think I had any serious problem with it . It was more of me having to mess around with it alot to be able to save and log someone in correctly due to the fact that in my Users model I had a validation for a presence of a :name, :username, :email, and :password, and my Omniauth for Github was only giving me a username input, so I had to get around it by hard coding a fake email, password, and name to allow someone to be able to use it. My last problem, the gift that keeps giving if you may, my nested routes. I think I spent the most time with this because I had to scratch so many ideas and start from new multiple times. I finally set it up so that you enter in a trip normally and then there would be a link where you can add if youve been there or not. It'll link you to your show page, but when you exit out theres an option in a nav bar for places youve been to and places you want to.  
Aside from all these issues, my favorite part of this whole project that I am so proud of is that I made a scraper so I can scrape a wikipedia page and get a list of all the countries and then implement it into a drop down menu. Since I was scraping a wiki page I also converted it into a json file in case of anything. My scraper code was:
 
 ```
  def self.scrape_locations
 
	 doc = Nokogiri::HTML(open("https://simple.wikipedia.org/wiki/List_of_countries"))
	 country_arr = []
	 doc.css('b').each do |row|
					 country_arr << row.css("a").text
		 end
 File.write('country.json' , country_arr.to_json)
 country_arr
end
```

And in my form it looked like 

```
<%= f.label :country %>
   <br>
   <select name="country" >
   <% LocationScraper.scrape_locations.each do |country| %>
     <option value="" disabled selected hidden>Choose a Country...</option> 
     <option> <%= country %> </option>
       <% end %>
       </select>
```

I think because i really tested my knowledge and because it wasn’t a requirement i am so happy and proud of it and to see my work displayed just how i wanted it to be was so euphoric. I do hope that when I have more time, and when I know more skills, I can come back to this project and really fix it to my liking. 

