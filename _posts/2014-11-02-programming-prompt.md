---
title: Programming Prompt
layout: post
---

I've been taking a break from the pure HTML and CSS experimentation this blog provides in favor of finally starting a JavaScript project. Usually, just like when I'm confronted by a blank sheet of paper (or a new Google Doc), I have a hard time deciding what to do, unless something was really compelling me to go create. In this case, I had nothing in mind at all for the project, just that I wanted to do *something* in the language that would help me down the path of learning it.

Now, before attempting the project, I did brush up on my knowledge of the subject by reading a few books that I found immensely helpful for padding my background knowledge in the subject, so I'll recommend them here:

* [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742) by Douglas Crockford
* [Effective JavaScript: 68 Specific Ways to Harness the Power of JavaScript](http://www.amazon.com/Effective-JavaScript-Specific-Software-Development/dp/0321812182) by David Herman

The first book was a fantastic primer on JS, especially due to the fact that I already had more than a passing familiarity with it and what it could do. I still considered myself a noob, but I have been working with GWT for just over two years, and have had to dip into the native JS a few times over the course of the project. I would definitely recommend *JavaScript: The Good Parts* for anyone who is already familiar with another programming language and has tried to monkey around with DOM programming in the past. For more elementary knowledge, this may not be the text to start with.

The second book was one I downloaded on a whim. It didn't provide any specific advice that I made use of, but I found that reading both *Effective Java* and *Effective C#* raised my code quality significantly, so I wanted to take the same approach when writing my first JS app. It was especially important to me that I have some sort of best practices to strive for with this application, because aside from some pretty broad practices, the community doesn't seem to have nailed down a comprehensive list of do's and don'ts. I find that having such a list is really good for me when I'm starting anything new, so I'm not bogged down in semantics.

When I finally felt ready, I ended up spending a surprising amount of time staring at the charcoal gray of IntelliJ doing nothing but thinking. What the hell was I going to work on? I googled a bit, browsed a bit, thought a bit more and still didn't have an answer. I mean, I knew I wanted to do some sort of game, and I wanted to play with canvas, but a platformer seemed a bit ambitious for my first foray into the JS world.

So I did something I never thought I'd do. I made a Tic-Tac-Toe game.

And it was surprisingly fun!

I never knew that this particular game had some pretty interesting algorithms involved in calculating scores, which you're almost forced to implement by the sheer inefficiency of calculating the scores for each player. More than that, it was the perfect level of coding to learn how to manipulate the canvas object. And once I was done my initial implementation, the project transitioned to a refactoring effort, and that led me down some pretty interesting learning paths. Now, I still have some components I want to decouple, but I'm pretty proud of what I've accomplished, and you can check it out [here](https://github.com/thomaskeschl/experiments).

The last thing I want to say about this is that the exercise worked just as a writing prompt does for students: it served as a jumping off point for a world of ideas. I already have a ton of things in mind that I want to do to make this more than just a boring old Tic-Tac-Toe game. Perhaps each square can be contested and retaken. What if there were a mini-game that launched to determine whether or not you can actually claim a square? Maybe the grid can overlay a procedurally generated map, and the terrain of a square effects what happens in the mini-game. If I make the grid huge, I suddenly have a host of new UI things to work on: zoom, edge scrolling and so on. I also want to implement a HUD around the canvas element that will be used to display game data, replacing the very basic alert and confirm dialogs I'm using now. The list goes on and on...

This has been so rewarding that I'm going to do it again with Pong or Breakout for the next language I pick up. But that might be a while...