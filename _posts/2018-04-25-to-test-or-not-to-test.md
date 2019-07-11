---
layout: post
title:  "To Test or Not to Test"
date:   2018-04-25 16:11:16 +0100
categories: Software
---

Unit testing is so central to software development, that code bases with next to none test coverage hardly could make their way to production. Your blogger, same as many of you, live in a world where time and resources are scarce. One will have to be mindful of on what to test and what not to when working on an under-tested code base.
<!--MORE-->
I know what you are thinking. What about Test Driven Development? True, you should TDD. More importantly, you need to do it right. I will share my thoughts on TDD in another post. For now, let’s focus on what to do when given an under test code base.

### Algorithms vs Collaborators
There are two types of codes you’ll find yourself writing. There are classes that form a nice unit of calculation logic, which can be viewed as a black box with clearly defined input/output data. Those are the typical computation heavy logic where testing is crucial while can be done with relative ease. Things like your insurance premium calculator, trade profit and loss generator, Theresa May’s approval rating forecast service, etc. These codes can be categorised as ‘**Algorithms**‘. You can write tests around this logic by crunching data into and verify results they spit out. These codes sit right on the sweet spot of the cost-benefit ratio of unit testing. They are your obvious candidate to write retrospective tests on.

The other type of codes finds themselves in classes where they have many dependencies, while the ‘logic’ of the methods are rather simple. These classes typically tap into multiple dependants, pulling in data and whack them into downstream services. I call those the ‘**collaborators**‘. Interface adaptors, HTTP request controllers, and those do all but nothing ‘service’ layer that sits between your controller and DAO fall right into this category. Unit testing these codes are possible but yield little benefit and brittle to achieve. You threw in 10 mocks, stubbed 20 behaviours, done all sorts of reflection and power mock magic, only to find what can go wrong could still go wrong. Instead of unit tests, the validity of these sort of logic is better assured with integration testing. If you do DI with Spring, there are handy libraries out of the box that brings up your application context allowing you to write tests penetrating all of the collaborator components and validate the bean wirings. What lifesavers.

Indeed, the two types mentioned here are way too overly generalised. Real world code would lie in anywhere on the spectrum between the two ends. In reality, you may find codes that are computation-heavy, and at the same time talks to 20 other classes. These classes are precisely those what we call ‘Spaghetti’ code that you need to refactor. Encapsulate the computation logic, take them out to there own class, consider [strategy pattern](https://en.wikipedia.org/wiki/Strategy_pattern), and black box test them.

Software testing is a huge topic even unit testing is merely a small slice of the full picture. Scratching the surface of the topic, this is what I think how best to spend your time retro-actively boost up your unit test coverage. Let me know what you think in comments below.