---
layout: post
title: Bamboo Can’t Git
date: '2018-05-11 16:11:16 +0100'
categories: Rants and Scribbles, Software
comments: true
---

Bamboo is undoubtedly the weakest link in the Atlassian family. Somehow it seemingly did not enjoy the same level of love and attention as its siblings, Jira, Bitbucket, you name it. It’s the middle child, the Ringo Starr, an app that apparently put together by a gang of 3-rated grumpy developers from some forgotten location. It’s so irrelevant that it even got it’s ‘cloud’ status confiscated.
<!--MORE-->
Now compare with other homogeneous products in the market, I still struggle to find anything attractive about Bamboo. It does not have a free tier. The starting teasing rate supports merely 10 jobs, improbable for any serious development teams. Well, I don’t personally pay the bills. This scribble is more about something else I was crossed on. That Bamboo just doesn’t know Git.

### Why You No Tag
Having the ability to initiate a build from a list of tags in your version control system can never be too much to ask from a CI tool. Which very feature had been collecting dust in Bamboo’s backlog for 5 years despite numerous requests raised.

I don’t get it.

You can work around this annoyance by triggering a custom build with the revision number of the tag as a parameter, which reminds me of using the early versions of Code Collaborator from SmartBear. That was a horrendous tool. At my old firm, they retired Code Collaborator with Bitbucket and made a conscious choice to adopt TeamCity rather than Bamboo. Kind of a smart move thinking of that really.

### Local Git Cache, For What?
Many of you must have been using CI tools to construct release artefacts. You run

```bash
mvn release:prepare -B
```

To roll the versions, build the tags.

I did the same on Bamboo. Ran that Maven goal. I looked at my git repo and scratched my head – Where did my tag go?

Turned out Bamboo caches Git remote to a local directory (look how contradictory that sounds). That’s right, you can try pushing commits to remote all you want in your build tasks. They just won’t go anywhere.

Surely, you can compensate it by running

```bash
git remote origin set-url your-git-tag
```

Before that maven release goal. Then you are walking straight into another pitfall. Setting your git remote makes your repositories in inconsistent state. If you happened to have deleted a tag from your real remote, Bamboo’s local cached ‘remote’ will not know about it and goes all confused.com when you trying to create that tag again. Why did they do that?

I don’t get it.