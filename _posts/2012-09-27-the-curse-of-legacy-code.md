---
layout: post
title:  "The Curse of Legacy Code"
date:   2012-09-27
---
I've inherited a mess. Not just a simple, static mess, but a critical ongoing mess. It's enormously depressing to face this on my own, day after day, being expected to understand, extend and re-factor it. So, how do I deal with it?

I'm currently drawing a lot of strength from ["Brownfield Application Development in .NET"](http://my.safaribooksonline.com/book/programming/microsoft-dotnet/9781933988719) and ["Working Effectively With Legacy Code"](http://my.safaribooksonline.com/book/software-engineering-and-development/0131177052).

What's encouraging is finding that a few techniques I've developed over the years before discovering these books are actually recognised within them and that I'm not completely ineffective for using them.

In particular, one thing I find myself doing a lot of is ["Scratch Refactoring"](http://my.safaribooksonline.com/book/software-engineering-and-development/0131177052/i-don-t-understand-the-code-well-enough-to-change-it/ch16lev1sec3). This is particularly useful when it's more than just the codebase that you don't understand. In my case I've been working on large brownfield sites and only simplistic greenfield sites for such a long time that there are quite a few techniques and technologies that have gone unexplored and unused. For example, it's difficult to make a case for exploring the use of [Entity Framework](http://www.asp.net/entity-framework) when there's a complex, monolithic, hand-rolled data access layer in use and the risks of switching are poorly understood. Inversion of control containers may have been in vogue for some time now, but when extending and supporting a system with a well-defined but archaic architecture, how do you start to use them and become familiar with them?

So, I find ripping things to pieces and building them back up with no intention of necessarily checking that code back in to the VCS can be a wonderful, occasionally cathartic, learning process. I think the only issue I have with it that still gives me pause, is when your manager thinks he needs to measure progress on a daily basis. Personally I think this is a matter of you successfully managing your manager's expectations - if they don't understand why you occasionally need to charge headlong down what could be a blind alley, then you need to retrain them.