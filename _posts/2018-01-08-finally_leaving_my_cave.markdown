---
layout: post
title:      "Finally leaving my cave"
date:       2018-01-09 04:18:15 +0000
permalink:  finally_leaving_my_cave
---


> "It is during our darkest moments that we must focus to see the light." 
> --Aristotle Onassis

Darkest moments indeed. Geeze, where to begin. I guess with context about what I'm even talking about would be good. So, just finished my Ruby Data Gem Project, except that I decided to take it to the next level of challenge. Instead of just scraping one website and accessing it with a CLI, I decided to scrape two, splitting that data into two seperate Classes (Movie, and Theater). It complicated things. But I am done! I got it to work! Certainly there is more that can be added, and if I stared at the code for a few more hours I'm sure I'll find more things I want to refactor to simplify and improve the code, but I think I've already met the expectations, many times over. I guess we'll see, huh? 

First, I'll describe my app. It takes data from two different theater websites. All of the movies, their showtimes, etc. Then, it combines the information from the both of them, ending up with a single Movie object for each film, without creating duplicates of the same film if both theaters were from showing it. I then connect each Movie object to the two Theater objects (though I made sure that if I were to ever add anymore theaters, I wouldn't have to change any of this code), but only if that Theater was showing that specific movie. This was crazy hard, because I didn't want multiple Movie object of the same movie, and didn't want to cheat and just add that information to the Theater class, I wanted them linked. 

Long story short, I got it to work, along with many other little problems that popped up. Geeze did binding.pry come in handy these last few days. Finally, I made the CLI more than just a scroll with information, I made it interactive. You can look at the current movies(current day only) with the showtimes from both theaters next to eachother, then select any one of those movies and get extra information about it. Alternatively, you can take it from the approach of the theaters, getting information about them and then viewing the showtimes for just that theater. Same functionality as viewing them all together, selecting individual films for more info. At any point, you can type in 'main' or 'exit' to get back to the main menu, or close the app. I did this by every time I needed input from a user, I ran it through a method that checks and verifies the input before ever trying to plug it in anywhere. All in all, not to shabby!

I constantly had to refrain myself from taking the easy path and just meeting the requirments. Not only because I wanted to challenge myself, but because I didn't want to just 'finish another lab'. This was honestly the hardest thing to do, because I knew that all I had to do was take 10 minutes to dumb down my code (significantly), and I'd be done. Thankfully, that's just not the kind of person that I am, so instead I dug myself deeper and deeper. I know that there are several things that need to be changed, but being as this is the first time I've made a functioning ruby application, I just don't know what they are. I'm looking forward to the video review so I can learn using my own creation's mistakes.

Once again, that feeling of accomplishment and realization that if I needed to do something like this again, I'd do it at least twice as fast. Feels great. God I love programming. 
