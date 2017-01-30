---
title: 'Subreddify'
layout: post
---

Man, I thought I was apologizing for the absence last time. It's been almost 2 years since the last update. 2 years! The last time I wrote one of these I was in my apartment with my girlfriend and dog. Now, I'm in my house, with my wife, my daughter and my dog. And my brother-in-law. Starting to see why I haven't been focusing too much on hobby projects lately?

Lets jump right in, shall we? [Subreddify](https://github.com/syntactec/subreddify-android) is a project that came organically out of a lack of what the Reddit app can do. I recently opened up a sub for the DnD group I'm a part of, which prompted many of them to complain about a lack of notifications when people post to the sub. So, that's the problem I'm trying to solve here.

A quick note about Android development. I've been wanting to get into it for a while now, I just haven't had the proper excuse. However, coming from a previous job context where I was a GWT power user, a lot of it makes sense to me. GWT borrowed from Android a lot, I think, so conceptually, I feel comfortable. Also, the last time I started up an Android project, I was an Eclipse user.

So it sucked.

Now, I'm really happy I get another excuse to use my IntelliJ Ultimate license (money well spent, thanks JetBrains). The tooling is really smooth and the process for learning the tools wasn't bump free, but it was still pretty quick. The pregenerated project templates Studio/IDEA provides are great starting points and showcase some pretty awesome stuff that make it easy to build on.

It was fun to see that, after IDEA generated my SettingsActivity, it had most of the controls I wanted in my app. So I was able to get right to the code. After some googling, I found a really excellent REST client framework for Android [Retrofit](http://square.github.io/retrofit/) and was able to implement a basic service in minutes. Throw in some [GSON](https://github.com/google/gson) for deserialization and I was able to have a pretty quick prototype.

Then, the learning freak in me decided that I wanted to see what GitHub had out of the box for project management. I'm using BitBucket right now for a work project and have been really impressed with the power of the full Atlassian solution (JIRA <=> BitBucket), so I wanted to see what GitHub had to compete. In short, after setting up a project, a milestone and a few issues, I feel like GitHub is about even with Atlassian in most ways. Only thing I'm really missing is the ability to create a branch directly from an issue and be able to navigate to that branch at a glance. If I were more than just one developer, I'd certainly want JIRA over GH Issues, but they'll suffice for me. Go ahead and check out what I've put together so far.

That finished, I dove into my first feature: the ability to specify subreddits to monitor. First thing I did was to get sidetracked in dependency injection land for a bit with [Dagger2](https://google.github.io/dagger/). Side note: I've learned the hard way that it's better to set up dependency injection ahead of time, rather than try to back fill it when you need it. It's a pretty high barrier to entry if you're setting it up from scratch, but by the time you really need it, it'll be too late to easily retrofit your application. Younger developers, learn from my mistakes! Finally, though, I was able to make the ~20 line code change required to implement this feature.

It feels too easy. And it probably is. I'm already eyeing the generated classes for a refactor, but I don't want to slow down the race to get something usable for my DnD group by next week. So it'll probably slide until after that point. Hopefully, I'll also be getting some good feedback that I can incorporate in 2.0 (that's right, no 1.x releases, given the scope of change I already know is going in to the next version).

Anyway, if you haven't checked out these tools yet, please do. They're pretty fantastic.

Totally unrelated: Java 9 needs interpolated strings and multiline strings. And to get rid of checked exceptions. And properties. That is all.