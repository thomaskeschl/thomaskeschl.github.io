---
title: 'Streaming with Java 8'
layout: post
---

First, all apologies for the absence. The new year has found me playing more games than I was playing at the tail end of last year. Everyone needs to geek out sometimes. Still, it's not as though my projects have been on hold. On the contrary, I've added two new repositories to the 'Hub.

The first, [eu](https://github.com/thomaskeschl/eu), is an attempt to learn the Java 8 Streams API whilst completing the [Project Euler](http://www.projecteuler.net) problems. More on this in a bit.

The second, [strident](https://github.com/thomaskeschl/strident), was a hobby project specifically designed for me to learn about procedural noise and Ken Perlin's algorithms. This was all with an eye on procedurally generating terrain, either for a 3D game or for a side-scroller like [Terraria](https://terraria.org) (which is one of the aforementioned games keeping me from posting here, by the way). It was also an attempt to play around with VisualStudio for the first time since my Master's project. I must say, it is a good product, and it was uncharacteristically kind of Microsoft to produce a community edition. I have loved C# for a long time and now there's no excuse to not go forth and code... unless you don't have Windows, I suppose. I don't think MS will ever community edition that beast.

Anyways, on to the titular subject of this post: Java 8 Streams. I first encountered them when looking into GWT's new changes for 3.0. I'm a huge GWT fan (nothing can quite do what it can, yet... I'm looking at you [Duocode](http://duoco.de)) and I haven't yet had the chance to play with Java 8 as we're stuck with 7 until GWT pushes out a new release. But what I saw had me pretty hooked; better event handling syntax with lambda expressions, more expressiveness, defender methods... it all looks pretty great. Let's be honest, anonymous inner classes make my eyeballs bleed.

<div style="text-align:center; font-style:italic;"><img src="http://stream1.gifsoup.com/view5/3019573/indiana-jones-face-melt-o.gif" border="0"/><p>The horror!</p></div>

But that all got me thinking, "What's actually *in* Java 8?" And that's when I made a wonderful discovery about Streams. Imagine all those functional type things you wanted to be able to do to collections in Java that dynamic languages, functional languages and Go could do forever. That's pretty much what Streams are. It's LINQ for Java. It's generators for Java. It's awesome sauce with lambda expressions and a bowlful of elegance. Java 8 takes the programming language you use to like until you used Python or Groovy and makes it over enough to seem new and fresh. Which is great news for those of us who work with the damn thing.

Take this old school Java 7 code, for instance. Here, I'm trying to find the sum of all numbers divisible by 3 or 5 below 1000:

    int sum = 0;
    for(int i = 0; i < 1000; i++) { // eww, for loops
        if(i % 3 == 0 || i % 5 == 0) {
            sum += i;
        }
    }
    return sum;

Now look at the new hotness:

    return IntStream.limit(1000)
                .filter(num -> num % 3 == 0 || num % 5 == 0)
                .sum();


Da fuq? Could it be this clean? Hell's yes it could and it is! Now, there's nothing wrong with for loops (even if I did make fun of them earlier), but how could you not love this new, expressive Java?

My other remark is that it is *fast*. These streams are incredibly efficient at doing what they're doing, as they are parallelizable if you aren't doing something that's order dependant. The filtering conditions also allow you to reduce the amount of stuff being stored in memory, which was really handy for writing my Sieve of Eratosthenes [implementation](https://github.com/thomaskeschl/eu/blob/master/src/main/java/problem/Problem3.java).

Bottom line: if you've moved on to other, less verbose languages, now might be a time to look back. Streams aren't perfect (lack of a takeWhile() and takeUntil() are kind of glaring omissions) but Java 8 definitely polishes the chrome on an aging language. Thanks, Oracle and the Java community, for keeping this language relevant.