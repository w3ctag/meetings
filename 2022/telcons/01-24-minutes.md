# TAG Teleconference
#### 24-26 January 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-01-24](https://www.timeanddate.com/worldclock/converter.html?iso=20220124T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris
* [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)
* [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)
* [New principle: Avoid introducing new parser-blocking features, fixes #329](https://github.com/w3ctag/design-principles/pull/347) - @cynthia

### Breakout B (US / APAC) - [2022-01-25](https://www.timeanddate.com/worldclock/converter.html?iso=20220125T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov
* [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober
* [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober
* [should provide advice on when it's good to return the same object again](https://github.com/w3ctag/design-principles/issues/46) - @cynthia, @dbaron
* [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober

### Breakout C (APAC / Europe) - [2022-01-25](https://www.timeanddate.com/worldclock/converter.html?iso=20220125T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo
* [Add guidance for attributes vs methods. Resolves #70.](https://github.com/w3ctag/design-principles/pull/350) - @cynthia
* [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

### Plenary Session - [2022-01-27](https://www.timeanddate.com/worldclock/converter.html?iso=20220127T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Kenneth, Peter, Rossen, Yves, Lea, Tess

Regrets: Hadley, Dan


### [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris

Reviewed Marcos's PR. 

Discussion about monkey patching vs extention points e.g. partial.

Feedback for Marcos:

- Clarify difference between monkey patching (bad) and modularization (good)
  - Maybe also link to https://en.wikipedia.org/wiki/Monkey_patch
- Examples from the past to make said difference more clear, the more concrete the better


### [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)

Discussion about feature detection even when funtionality doesn't make sense.

Ken will start a PR.

### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

Tess to address existing feedback

### [New principle: Avoid introducing new parser-blocking features, fixes #329](https://github.com/w3ctag/design-principles/pull/347) - @cynthia

Adjusted text based on Jake's feedback. Merged PR.

## Breakout B

Present: Peter, Rossen, Max

Regrets:


### ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov

### [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober

Added Max, going to try to write something up.

### [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober

### [should provide advice on when it's good to return the same object again](https://github.com/w3ctag/design-principles/issues/46) - @cynthia, @dbaron

### [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober



## Breakout C

Present: Ken, Dan, Max, Sangwhan, Yves

Regrets: Hadley, Lea


### [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo

### [Add guidance for attributes vs methods. Resolves #70.](https://github.com/w3ctag/design-principles/pull/350) - @cynthia

Ken: re [lea's comment](https://github.com/w3ctag/design-principles/pull/350#discussion_r765085577) for me an attribe is reutning something... you don't expect it to do expensive operarions...

Dan: concerned about the example

Ken: yes not a big fan.. wouldn't call it a notable failure - maybe a box saying "Note: we have a few of these issues in the platform"...

Yves: "expsneive operation" seems to be not really well defined... The definition of expensive operatioon needs better wording.  Side effects - e.g. when you do a layout operation not only calculating the thing you want to get but many others... 

Sangwgan: [makes changes]

**We squash and merge**

### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

Sangwhan: this doesn't fit the [style guide](https://github.com/w3ctag/process/blob/master/style-guide.md) - needs a tl;dr 1 sentence as first sentence. "New features should not break existing content."  We have an expectation that when shipping new features it doesn't break existing content.   "Support Existing Content" as a heading.

Sangwhan: needs to be condensed down a bit. Also needs to be in active voice aligned to the styleguide...

## Plenary Session

Present: Peter, Kenneth, Dan, Amy, Yves, Sangwhan, Tess

Regrets: Hadley, Max

### Breakout Rollup

#### Breakout A

Peter: we talked about monkey patching - marcos issued a PR - we had some feedback.  

Ken: Anne gave feedback 2 days ago - so he will update the PR.  Ongoing.

Peter: we talked about guidance on window vs. worker... Ken 

Ken: I did [a PR](https://github.com/w3ctag/design-principles/pull/356) - got some feedback from Anne.

Tess: I think it's ok to file issues for other worker types but land this first.

Sangwhan: that lgtm.. the audience of this doc should now what a worker is, if not we should have a reference instead of explaining it ourselves. Happy to land without that change. 

Dan: looks fine to me

Sangwhan: I can fix the reference when I'm home. Let's land it and I'll file an issue to follow up.

Ken: **squash and merge and dramatic music** 

Peter: we talked about PR290 - Tess...

Tess: I will look at feedback.

Peter: on PR347 we merged it - parser blocking features.

#### Breakout B

Peter: Max did jump in on issue 16. Exotic objects... 

#### Breakout C

Dan: Adding guidence for attribute vs methods.. Sangwhan made some changes and we merged. Spent time on backwards compat principle, our first attempt to bring over another html design principle into the design principles and Sangwhan made a point that it doesn't fit the current style guide so it needs to be updated and reworded. 

Sangwhan: I have a draft, can share later

Dan: we can try to do that async. In particular Tess had initiated this, it would benefit from your attention

Tess: okay

### [Describe what to do when a feature is temporarily only available on some platforms](https://github.com/w3ctag/design-principles/pull/357)

Dan: what is the context?

... examples?

Peter: sounds like the opposite of .. 'design your code so it works where it doesnt work'

Sangwhan: gracefully fail?

Peter: sounds like its asking for a polyfil or something. An example of what kind of feaeture might help here. Exposing an OS platform feature rather than a web platform feature.

Dan: maybe not ready to merge. Ask that question?

Sangwhan: yeah. I wrote a suggestion but it doesn't entirely make sense.

### Issue Triage


