---
layout: post
title:  "Continual Replacement"
date:   2017-10-22 00:00:00 +0200
categories: software
---

#### *This post is still a draft. Help me write it up*

A few years back while still working together at Fidor, Rado and I were exploring ways to solve our legacy code problem. We had a big old Rails app. Legacy monoliths seem to be a recurring situation with mature Rails projects. But nevertheless everyone is always shocked by it. We couldn't rewrite it, so Rado wanted to follow a proven concept of his of refactoring "islands" — logical parts of the monolith app that can be prepared to be taken out as micro-services. Even if a micro-service doesn't make sense, at least refactoring the code into a module that can be handled easily in the future. So when somebody is doing a change, they would first conduct a small research to try and find out if the peace of code they are about to work on can be reworked in that way and perhaps with some reasonable overhead a new island will emerge within the monolith. We were much smaller team back then, with a smaller code base. So the idea was not at all crazy or far-fetched.

So I read [this post](https://dave.cheney.net/2017/11/30/never-edit-a-method-always-rewrite-it) by Dave Cheney recently. He's a Go-contributor who writes a nice blog covering mostly software engineering topics.
*Never edit a method, always rewrite it* -- more of a talking point and less an idea presented at a conference by Chad Fowler, a Rails guru. I wasn't at that conference but I gather the point made was suggesting software can mimic biological systems. Like complex organisms build from tiny cells undergoing constant renewal, etc... And as already mentioned by Dave Cheney it was in fact pointed out as a not very good idea. But if you actually read the post, I would say I find myself in agreement with him — yes, immutable source code is probably an unworkable solution. However it is a nice goal to aspire to. I see a lot of parallels between that and the "islands" approach.

Especially with so many "mature" Rails projects teams need an understandable, low-threshold solution for dealing with the mess of legacy monoliths. Even if it's not that effective. Because that fable complete rework you always wanted to do and is probably hanging as a post-it note somewhere in you office will likely never happen.
