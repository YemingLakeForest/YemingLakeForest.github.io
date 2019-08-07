---
layout: post
title:  "Forget TDD – Design Driven Development!"
date:   2018-04-27 16:11:16 +0100
categories: Software
comments: true
---

When it comes to software testing, [Test Driven Development](https://en.wikipedia.org/wiki/Test-driven_development) (TDD) is the new politically correct. TDD, alongside with its variants, like BDD (Behaviour Driven Development) are particularly en vogue these days with dozens of projects built around these concepts. You can’t even go into any job interviews without claiming you are a true believer of TDD.
<!--MORE-->
Before going any further on, I want establish that I am fully in support of TDD. It can be beneficial, when it’s done right. Although, same as any other ‘methodologies’ out there, agile, XP, CI, CD, you name it, it is paramount for one to understand the concepts behind them. Look under the bonnet, ask yourself why things are done in certain ways. It is definitely easier to turn in your right to think and follow the rituals brainlessly. And ‘hope’ for the best. We have a word for it. It’s called following  cult.

Back on TDD, let’s first have a look at what actually is test driven development. Here are the typical steps TDD specifies:

* Think about what you want to do.
* Think about how to test it.
* Write a small test. Think about the desired API.
* Write just enough code to fail the test.
* Run and watch the test fail. Now you know that your test is going to be executed.
* Write just enough code to pass the test (and pass all your previous tests).
* Run and watch all of the tests pass. If it doesn’t pass, you did something wrong, fix it now since it’s got to be something you just wrote.
* If you have any duplicate logic or inexpressive code, refactor to remove duplication and increase expressiveness.
* Run the tests again, you should still have the Green Bar. If you get the Red Bar, then you made a mistake in your refactoring. Fix it now and re-run.
* Repeat the steps above until you can’t find any more tests that drive writing new code.
Source: [WikiWikiWeb](http://wiki.c2.com/?TestDrivenDevelopment)

To be honest, I am not a huge fan of this doctrine. It’s too rule-y, a bit of over-specification on how you should write code. Don’t get me wrong, I believe it is the right thing to do to write code first, then the logic. But follow the **write-one-test-then-write-minimal-code-to-pass-test-then-refactor** 
rituals? Ain’t nobody got time for that.

I remember this job interview I went to. It was a typical talk and code pair programming session on an IDE. I was quite comfortable with the problem. To try to show that I know what I was doing, I used TDD. I started laying down my tests as I thought through the APIs the classes I am going to write.

“You should write a small enough test to start with.”

“Don’t worry about refactoring just yet.”

“Have you re-run all of your tests?”

The supposedly smooth programming session was full of bumps and hiccups of such. Needless to say, the interview as a waste of everyone’s time. And the condescending attitude of the interviewer and his TDD fundamentalist believe surely didn’t help.

### Cargo Cult
Tanna is a small Melanesian island situated in the middle of nowhere in the Pacific Ocean. During World War II many of the islanders were recruited by the United State for their war efforts. These indigent people were exposed to first world living first time in their entire history. The Americans pulled out after the war ended, abandoned their airstrips and military bases. Attempting to bring back the cargo drops and manufactured goods, local inhabitants started to mimic the Americans by wearing their uniforms, carving out wood guns to perform parades. Reported to their wood-made headphones on their replicated control towers to try to bring back the US planes. Built wooden planes and hoped that somehow they might attract back their metal made kinds. Yup, this is ‘Cargo Cult’.

Hilarious, were they not? But if you find yourself following TDD methodologies so literally as if mimicking these islanders mimicked their colonial masters, you wouldn’t be laughing so loud.

### Design Driven Development
To me, Test Driven Development can be simplified and abstracted into 3 letters – DDD. You don’t have to always start by writing the bare minimum test, and make it pass by just enough code. **Test Driven Development is Design Driven Development**. Think about the design of your classes, before you write them, by writing tests. Design the APIs, parameters and returns, their types. Think about how exceptions should be handled, what are the edge cases. Capture them all in tests. Sometimes you don’t even need to write the test themselves, just by laying out the tests skeletons gets you a long way to clear up your mind on what you are trying to implement. The tests are the blueprint, scaffolding and documentation of your software, you should treat them the way they deserve.

Indeed, some rituals are proven to be beneficial. People actually stand up in stand-up meetings to be more engaged in the conversation. It also helps keeping the meeting short by making everyone a bit less comfortable. Point is, rituals are not unconditionally good. Those wooden planes didn’t bring back the canned food, jeeps and meds to the Islanders, and don’t imaging following TDD, as it’s specified, would automagically improve software quality. One should always prosess a critical mindset and curiosity to unpick and extract the essence of thosr doctrines. This is true, for software development, and same for arts, science, politics and everything.

Let me know what you think in comments. If you skipped through the whole page and somehow ended up here anyway, have a nice day. And don’t forget to be awesome 