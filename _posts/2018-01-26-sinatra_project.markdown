---
layout: post
title:      "Sinatra Project"
date:       2018-01-27 03:35:46 +0000
permalink:  sinatra_project
---


So, I decided to have some fun with this project. Well of course I (almost) always have a blast programming, I decided to make something that when I explained it to my fiance, she would actually understand what was going on! She loves animals, like a lot, so for my sinatra project I created an application that I named Park and Pet. I learned a ton while making it, and not having to pass ridiculous tests was glorious. I got to name the buttons whatever I wanted! Anyways, let's start with a description.

Park and Pet is a Sinatra and Active Record application that has 3 classes: Owner, Pet, and Park. The owner class is the user, where you create a username and password, and can sign in and out. As the owner, you has_many of both pets and parks. Any of the pets and parks in the database that are yours, you can edit or destroy them, and of course you can set your pets up for adoption. If your pet has an adoption: true status, then any other owner can click 'adopt', and the pet will now be theirs. You can also send your pet to the pound, transfering the ownership to "The Pound Guy". All in all its a fun little application.

However, there were several steps in this project that took me a moment to figure out. I foolishly totally spaced the error messages that Active Record will give you an update does not work, and it wasn't until the final 2 hours of the project that I remembered them. One of the first hurdles that I came across was that I tried to complicate my life with a JOIN table that I did not need. I thought that in order for my Pets class to belong_to :owner and belong_to :park, I would need a join table. Spent about 3 hours trying to figure out why my connections weren't working, only to realize that the real problem was that I was forgetting to .save. Oh the sorrow. Little things like this are becoming fewer as I get better, but I'm certain that they will never truly go away. 

One of the steps that I took to simplify my code once I had the basic structure working was to add a few helper methods to make my erb files easier to read. I realized very late in my programming that it would have been much simpler and headache reducing if I had simply added a :name attribute to my Owner class. I decided that the refactoring to get that little tidbit to work was not worth the effort right now, but if I ever come back to this project to polish it that will certainly be one of the first steps that I take.

I am seeing the truth of the "make ugly messy code, then simplify it til it's beautiful". One thing that has been a great help is the advice that I got from one of the books that I read to make the method and variable names as descriptive as possible, while also keeping them as short as possible. Don't, the book said, sacrifice understanding for shorter names however. Keeping to this principle has made my code as a whole easier to understand.

Well, thats all for now, have a good one.
