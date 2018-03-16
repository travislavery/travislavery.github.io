---
layout: post
title:      "Magic is hard sometimes"
date:       2018-03-16 23:24:47 +0000
permalink:  magic_is_hard_sometimes
---


React and Redux are both incredible. I have absolutely loved the ability to take any part of an app, break it down into little tiny pieces, and then like a jigsaw puzzle put them all back together. Redux makes it possible to do this, by letting me access the data I’m getting back from my rails API in a non hair-pulling and screaming way. I can at any point decide that this piece of the app needs access to that part of the state data, and boom, it’s done in like 5 lines of code. I can pass along information to the small, dumb, reliable and pure little pieces, so they can do their thing. Thanks React, cool move. 

All of that being said, error handling was a beast. Of course this was the first time that I created a React Redux application, but goodness sometimes it was difficult to follow the trail of component crumbs. I realize now that the best and easiest way to avoid such difficulty finding errors to make LOTS of small, pure, dumb components and try to keep my containers dealing with very specific tasks, so when something goes wrong I can narrow it down to 1 or 2 files very quickly. The reason I did not do this when I started this project was 1.) I didn’t realize how difficult it would be to find errors, 2.) I didn’t realize the true power of Redux, and 3.) I thought that I should have only 1 container per reducer, and then pass all pieces that needed the info props. Only later did I realize that is exactly was Redux eliminates the need for! Next time, I’ll structure it better from the get go.

One thing that I did notice, and really appreciated, about React was that it made single purpose components so easy to make! By extension, it made it so that when you read your containers, you can picture the thing as a whole much easier. I also noticed very early on was that I constantly broke components into smaller and smaller components, and I had to catch myself from doing this in cases where it wouldn’t be useful to break it down further. And then I’d come back later, add more code, decide it was getting too impure, and then break it up anyways. Lesson learned. 

Overall, I think that these two tools are going to be a part of my arsenal forever. There is still so much to learn and master about them, I’m just getting started, but the future sure is looking bright. I’m ready to take on the world, graduation here I come. 

