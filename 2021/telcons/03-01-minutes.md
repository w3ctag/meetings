## TAG Teleconference
##### 01-03 March 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-03-01](https://www.timeanddate.com/worldclock/converter.html?iso=20210301T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [give advice on read-only lists](https://github.com/w3ctag/design-principles/issues/50) - @atanassov
* [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @atanassov
* [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron
* [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185) - @hadleybeeman, @atanassov
* [Integrating with the WICG process](https://github.com/w3ctag/process/issues/23)

#### Breakout B (US / APAC) - [2021-03-02](https://www.timeanddate.com/worldclock/converter.html?iso=20210302T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55) - @cynthia, @dbaron, @timbl, @plinss
* [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron
* [Add naming tips for getter-likes/selector-likes](https://github.com/w3ctag/design-principles/issues/136) - @cynthia
* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron

#### Breakout C (APAC / Europe) - [2021-03-02](https://www.timeanddate.com/worldclock/converter.html?iso=20210302T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @kenchris
* [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia
* [describe principles for naming of locking/unlocking APIs](https://github.com/w3ctag/design-principles/issues/85) - @cynthia
* [Clarify events vs observers even further if possible](https://github.com/w3ctag/design-principles/issues/127) - @cynthia, @kenchris
* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @torgo
* [Linking Design Principles with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282) - @rhiaro

#### Plenary Session - [2021-03-03](https://www.timeanddate.com/worldclock/converter.html?iso=20210303T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Review Crypto Principles](https://cryptpad.w3ctag.org/pad/#/2/pad/edit/GtHEsEypYgImN8PckR3U+jdY/)
* Design Principles PRs to review and/or merge
* Breakout Rollup
* Issue Triage

-----

### Breakout A

Present: Kenneth, Peter, Amy, Dan, Rossem, Tess, Hadley, Lea

Regrets:

[we broke out into breakouts]

#### Rossen, Lea, Tess ####

Tess: progress made on all of the above.

##### [give advice on read-only lists](https://github.com/w3ctag/design-principles/issues/50) - @atanassov

**Rossen**

Rossen: mine is mostly there...

##### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @atanassov

**Lea**

##### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron

**Tess**: [PR is up](https://github.com/w3ctag/design-principles/pull/290)

#### Amy, Hadley ####

##### [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185) - @hadleybeeman, @atanassov

Hadley: we looked at the web crypto spec -- 

Amy: we wrote [some text](https://cryptpad.w3ctag.org/pad/#/2/pad/edit/GtHEsEypYgImN8PckR3U+jdY/)... 

Peter: we'll take a look at the plenary...

Hadley: we need review from crypto experts too.

#### Peter, Dan ####

##### [Integrating with the WICG process](https://github.com/w3ctag/process/issues/23)

Peter: Dan & I worked on WICG integration - I migrated the MATRIX server to the new version which will help as MATRIX has a slack bridge and a mail integration... That will also give people Matrix and IRC as options...

Dan: [wrote design review lifecycle text] for review


#### Ken #### 

Ken: looked at issue #39 - 

### Breakout B

Present: Tess, Peter, Rossen, Lea, 

Regrets:

##### [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55) - @cynthia, @dbaron, @timbl, @plinss

##### [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

Tess took an action to go spelunking in our meeting minutes to assemble links to previous discussion on this topic.

##### [Add naming tips for getter-likes/selector-likes](https://github.com/w3ctag/design-principles/issues/136) - @cynthia

##### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron

### Breakout C

Present: Amy, Sangwhan, Dan

Regrets: Kenneth

##### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @kenchris

##### [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia

Sangwhan: [recounts discussion in the comments for PR 262](https://github.com/w3ctag/design-principles/pull/262)

Sangwhan: [writes some additional text]

Sangwhan: added a comment on the issue...

##### [describe principles for naming of locking/unlocking APIs](https://github.com/w3ctag/design-principles/issues/85) - @cynthia

##### [Clarify events vs observers even further if possible](https://github.com/w3ctag/design-principles/issues/127) - @cynthia, @kenchris

##### [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @torgo

Sangwhan: solved by PR [264](https://github.com/w3ctag/design-principles/pull/264) (which was already merged)?   No I don't think it does entirely...

Dan: so more work to be done.

##### [Ethical Principles spell out TAG]

Sangwhan did a thing.

##### [Linking Design Principles with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282)

Dan: we could put some words in the Abstract

Amy: we could write an intro paragraph in section 1 before 1.1

"Design principles talk about the design aspects of web APIs and sometimes touches on user needs when they affect technical decisions.  The Design Principles are built on and informed by the [Ethical Web Principles](https://www.w3.org/2001/tag/doc/ethical-web-principles/) which lays out a basic ethical framework for the web platform. The principles in this section are practical implications/considerations/?? derived from the high level ethical considerations in this framework. "

The Ethical Web Principles are a foundation. Design Principles builds on that
ethical web -> therefore "safe to browse"


Dan: 1.2 should reference https://www.w3.org/2001/tag/doc/ethical-web-principles/#privacy

Dan: 1.3 should reference https://www.w3.org/2001/tag/doc/ethical-web-principles/#verify

Dan: 1.4 should reference https://www.w3.org/2001/tag/doc/ethical-web-principles/#control and maybe privacy as well

Dan: 1.5 should reference https://www.w3.org/2001/tag/doc/ethical-web-principles/#multi

In EWP - not all principles translate to API design - note this explicitly [issue](https://github.com/w3ctag/ethical-web-principles/issues/37)

Dan: will write the PR with the links

Amy: will write the PR with the intro text

Also briefly discussed: Back up each principle with references to previous TAG decisions/experiences 
https://github.com/w3ctag/ethical-web-principles/issues/19

### Plenary Session

Present: Kenneth, Dan, Peter, Tess, Amy, Lea, Hadley

Regrets:

##### [Review Crypto Principles](https://cryptpad.w3ctag.org/pad/#/2/pad/edit/GtHEsEypYgImN8PckR3U+jdY/)

[discussion on Amy & Hadley's draft and need to get feedback]

[agreed to put the text in the issue on github and continue the discussion there]

##### Design Principles PRs to review and/or merge

###### [Added some text for "Attributes vs Methods"](https://github.com/w3ctag/design-principles/pull/262)

Tess: put this on the agenda for breakout C next week and try to close  [merge] then?

Dan: will do.

###### [Use Bikeshed syntax for more things.](https://github.com/w3ctag/design-principles/pull/272)

Tess: this got merged. 

###### [HTTP header syntax definition principle](https://github.com/w3ctag/design-principles/pull/287)

*Discussion on [Anne's comment](https://github.com/w3ctag/design-principles/pull/287#discussion_r576155786)*

Tess: what is argument against?

Peter: "if structured fields isn't rich enough then... "

Peter: [will do a reply]

###### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

Tess: wrote this week after discussion in breakout A. Got good feedback in B.  This came out of a couple of design reviews that Alice & I did together... Try to capture how to navigate failure modes...  Alice & I agreed it's contextual and a lot of trade-offs.  Sometimes it might be right for multiple implementations to ship the same API and have them behave differently... or other options... Need feedback. Not ready to land.

###### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117)

Lea: we discussed this in breakout A - when I was writing it - and wrote a [pull request](https://github.com/w3ctag/design-principles/pull/291) - a lot of this guidance comes from minutes..  In some cases the low level APIs cannot be exposed.  Security & Privacy are the obvious reasons that come to mind.  We should explicitly say this. 

Tess: it's not all the time that they can't but that sometimes they shouldn't.  Adding new high-level APIs that have magic inside that doesn't match the magic of other similar things... means you have redundant code paths a bitrot..  E.W.M. said "build high level things on low level things" - that's great, but the pendulum has swung too far in the other way - meaning anything high level now needs to be built in JS. There is a happy medium we can strike.  For `portal` example - it's not clear that iframe and portal should be built on the same thing - maybe both iframe and portal should exist but they should still be built on the same low-level model. 

Lea: If we just give people a blanket pass to not expose the low level building blocks is too blanket.

Ken: the EWM was also trying to explain the platform to developers - but sometimes if you have to expose low level building blocks... if you need to deal with a new thing .. so you have to invent your own typed array - that is too low level.  Bulilding up different building blocks that are not part of your API...  A logic gate - that's too low level.  When it's too low level you start exposing the specific APIs that comes from your platform.  

Tess: ties the web to a specific implementation - the web should have an abstracted model of a computer - a 2d display, a keyboard and mouse, etc... for Key Events - key down, key up, we don't have different sets of key events for ADB keyboards, Sun keyboards, etc...  If Tim had exposed just NeXT keyboard events, that would not be good for the web. You don't want websites to code to that level of abstraction.  The web is bigger than platforms and will outlive all the platforms we are using right now.

Ken: especially if you don't have clear use cases...

Dan: Web neural network API... Sangwhan commented that it looked like that's what that API was doing, building on the android NN API.

Tess: shape detection and face recognition are higher level and more portable as a result. Web platform isn't the same kind of thing as the other platforms, it's a meta platform. When we chase native platform features and try to expose them we often screw up that layer of abstraction and pay a maintenance cost forever.

Ken: makes sense eg with web assembly

Tess: none of the principles are absolute, exceptions to everything. Principles should cause you to think it through and have a compelling case for execption. The simd stuff is a good example

Lea: meta principle?

Dan: we identified that we don't really have a good introduction

Tess: open issue to add an intro..

Dan: related to breakout C, we wrote it specifically as a good way to relate to the ethical web principles, but that's only one function of an intro. Another line could be that none of these principles are absolute. 

Tess: it's more like tradeoffs.. I worry about people taking the list as stone tablets from the top of the mountain with rigid rules to follow. It's a guide, helping people do the right thing.

Hadley: always a danger with anything we write, better than not sharing what we learned

Tess: anything we say people could over apply the principles. we want them to consider them.

Hadley: we faced it with the ethical web principles too. "This principle can't be right because.." and edge cases in which it didn't apply, which were valid and right. We're not doing normative specs with test suites..

Dan: Lea you actually wrote text in [a PR](https://github.com/w3ctag/design-principles/pull/291/files).. 

Lea: I'm hearing that another reason is to avoid tying the API to a specific implementation detail. Any other reason? Should it be an exhaustive list?

Tess: we shouldn't claim the list is exhaustive. Point out examples.

Lea: doesn't give that a blanket pass to implementers?

Tess: they can already ship whatever they want, we're trying to help them do the right thing. I don't think I know everything that should be in the list. We can't say it's exhaustive.

Lea: okay

Ken: people look at it and normally come up with an answer. But it's not clear cut. Consider this and maybe find a better solution.

Lea: if you have more examples in mind those are welcome.

Ken: webassembly and simd is a good example. It's not just written for arm or intel, it's a standard to help everyone and is future proof for future hardware. When people try to go really low level they invent objects that are not part of this api, but a general concept you should be building upon. Need to find a generic solution for those that works for everyone. If you're at that level, take a step back. Aim for as little tech debt as possible.

Peter: also houdini? very high level APIs and now looking for commonalities to expose lower levels

Hadley: definition of high and low level APIs. Travis put it in the original issue. 

##### Intro Text

"Design principles talk about the design aspects of web APIs and sometimes touche on user needs when they affect technical decisions.  The Design Principles are built on and informed by the [Ethical Web Principles](https://www.w3.org/2001/tag/doc/ethical-web-principles/) which lays out a basic ethical framework for the web platform. The principles in this section are practical implications/considerations/?? derived from the high level ethical considerations in this framework. [something something these rules are not set in stone]"

Dan: we're not having principles in design principles that are ethical statements. the design principles will be actionable things that designers can use when they're thinking about how to design something that are built on that foundation. Additional work to do on ethical principles next time, where we make more linkages back to further work that underpins the ethical principles, and forward links to design principles.

##### Issue Triage

[we triaged unassigned issues and closed one redundant issue]