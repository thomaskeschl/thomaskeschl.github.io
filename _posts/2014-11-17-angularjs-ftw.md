---
title: AngularJS FTW!
layout: post
---

Just a very quick update tonight, but one that I just felt I had to make: AngularJS is pretty great.

I know that for most of you, this will seem like old news, or that I'm late to the party or whatever, but I've only spent a few hours playing with it and I love it! For work, I'm playing around with GWT, Google's original foray into web frameworks. This caused me to investigate other frameworks like Django, Grails, Ruby on Rails, Dart and, lately, Node. When I first looked into Dart (just before 1.0 was announced and around the same time I was playing with Go) I saw a reference to the Angular project and thought it was pretty neat, but decided to postpone my Dart experimentation due to the fact that it just wasn't *there* yet. I encountered it again in the following months when looking into using Go to serve a web app (I'll have to rustle up a link to the tutorial I was looking at some time in the future, it was a good one). Finally, there came a time where I couldn't ignore it, so what did I do? I toyed around with Grails and Django.

Turns out that while I was puttering around with these frameworks, Angular kind of exploded.

Now I can see why. After setting up the tutorial yesterday and puttering around with it today (mostly following the tutorial, but some branching out) I am firmly in the Angular camp. It solves a huge problem that I've been struggling with on my client side JS (modularization, which I could make the subject of another blog post... seriously, wtf JavaScript... facilitate the breaking apart of files fugawdsakes) and it does so in what I find to be an elegant way. Sure there's browserify, but I don't want to have to run some post process on my web app just so people can see the damn thing... I just don't like that workflow. I just can't settle for it. I want to be able to see my web app without having to use a build tool to get everything where its supposed to be. That smacks way too much of the Ant scripts I have to use on a daily basis.

Anyway. Modularization is a nice bonus, but you also get html templating that is minimally invaded by ng directives (at least, with what I've seen so far) and I like that it's all client side. Though the templating in Django and Grails is similar, it bugs me that that templating is all server side. You're still going to have to add in and manage scripts, and I don't think these frameworks do it quite gracefully enough. And don't you start arguing performance with me... I'm fully aware that Twitter made a huge splash by saying they were going back to a more server based templating model, but... let's be practical here. Not every website is going have Twitter numbers. I would choose elegance, maintainability and readability over performance almost every time. That's probably the poet in me, though.

I guess this wasn't as quick as I thought it would be, but I hope it wasn't boring. Long story short, if you've been wondering about client side templating, but haven't gotten around to it, perhaps you should consider taking the plunge. The documentation and tutorials are excellent, and the tutorial gives you a lot for a small time investment.

There's more than just Angular out there (and lets be honest, I'm still a doe-eyed honeymooner), so if you have any recommendations for me, I'm all ears.