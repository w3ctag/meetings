# TAG Teleconference
#### 02-04 May 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-05-02](https://www.timeanddate.com/worldclock/converter.html?iso=20220502T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)
* [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)
* [New principle: Inclusive Naming Choices](https://github.com/w3ctag/design-principles/issues/253) - @hober, @rhiaro
* [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
* [New principle: Leave it better than you found it.](https://github.com/w3ctag/design-principles/issues/340) - @LeaVerou, @torgo
* [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober
* [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober
* ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov
* [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober, @alice
* [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris

### Breakout B (US / APAC) - [2022-05-03](https://www.timeanddate.com/worldclock/converter.html?iso=20220503T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion
* [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou
* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
* [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
* [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov
* [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou

### Breakout C (APAC / Europe) - [2022-05-03](https://www.timeanddate.com/worldclock/converter.html?iso=20220503T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo
* [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2022-05-05](https://www.timeanddate.com/worldclock/converter.html?iso=20220505T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Dan, Peter, Yves, Rossen,

Regrets: Lea, Sangwhan


### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

Rossen: [reviewing Ken's comment](https://github.com/w3ctag/design-principles/pull/354/files#r791499568) I don't agree with listifying ...

Peter: I tend to agree since it also refers to the next para....

[...discussion...]

Rossen: [adds suggestion]



### [New principle: Inclusive Naming Choices](https://github.com/w3ctag/design-principles/issues/253) - @hober, @rhiaro

### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon

### [New principle: Leave it better than you found it.](https://github.com/w3ctag/design-principles/issues/340) - @LeaVerou, @torgo

Peter: should we add outdated API patterns as well?  e.g. CSS OM... 

Rossen: [leaves some suggestions in the PR]

Rossen: should we list - all communities - security & privacy listed but what about accessibility?  We should add accessibility to this list.

Peter: if the list is too exhaustive then people might say "my thing isn't on it"...

Rossen: ```...for example, security, privacy, accessibility, etc...```

Peter: should we have the reasoning for this?  For example - just because there is a bad thing somewhere doesn't mean we won't fix that one day and if we have another example of it then it will make it harder to fix...

```Parts of the web platform evolve independently.  Issues that are present with a certain web technology now may be fixed in a subsequent iteration.  Duplicating these issues make fixing them more difficult.  By adhereing to this principle we can make sure overall platfrom quality improves over time.```

Yves: you can't open a second hole of the same size.

[we wordsmith this addition]

**we agree to merge**

**also closed issue 340**

### [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober

### [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober

### ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov

### [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober, @alice

### [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris


## Breakout B

Present: Rossen, Peter, 

Regrets: Sangwhan, Lea, Max


### [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion

### [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou

### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou

### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

### [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris

### [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou

### [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou

### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

Worked on a PR

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

### [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov

### [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou


## Breakout C

Present: Dan, Yves, Amy, Hadley, 

Regrets: Sangwhan, Max


### [User Activation PR](https://github.com/w3ctag/design-principles/pull/365)

Amy: we worked on this during the f2f in London

Dan: maybe we should merge it?

Amy: we should give Tess a chance to look

Dan: [leaves note in slack, merge at plenary]

### [s/Design/Expose/](https://github.com/w3ctag/design-principles/pull/364)

*reviewed and merged*

### [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo

### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman

Hadley: i still think this is too big and too exploratory an area for us to be helpful.

Amy: agree.

Hadley: looks like it hasn't moved in... don't know if we're waiting on a closing comment or .. what the status is.

Dan: not clear to me there are architectural principles we can apply to this space that would be very helpful. Feels like the work is ongoing. Anything we do would be extraneous noise

Hadley: or prematurely limit

Amy: I can write a closing comment that points to some places this is being worked on

Hadley: very blurred line with identity / identifiers / authentication / credentials / ..


### Discussion on Ethical Web Principles impeding submission to Statement track

[discussion of need for new intro text]

Amy: we could maybe just do a read-through and do some small tweaks.

Hadley: in the abstract we say "The following document sets out ethical principles that will drive the TAG's continuing work in this direction." but we are changing the purpose.

Amy: should we change it to "the w3c's continuing work"...

Hadley: yes.

Dan: and change the last paragraph about purpose. Rather than replacing TAG with W3C we can say the purpose is to inform horizontal review or general review of new specifications.. need to rewrite

Hadley: agree.. and not limit to review

Dan: agree

Amy: worth splitting purpse into subsection of intro to make it obvious?

Hadley: suggest that whatever the process is, should take into account thesse principes, but not dictating process

Yves: part of horizontal review for TAG for example

Hadley: useful for team, chairs, contributors, to be thinking of it, not just be a sort of review stage

Yves: same for all horizontal review docs - you have guidelines and the goal is to go to the review by having nothing to be reviewed, nothing that will be triggered during the review because you followed the guidelines

Amy: [wil start PR]

Current para:

```The purpose of this document is to inform TAG review of new specifications and candidate additions to published recommendations, and to inform other documents such as the Web Platform Design Principles, Self-Review Questionnaire: Security and Privacy or other similar checklists and sets of principles used by specification authors and editors. It also serves to raise awareness of the ethical responsibilities of web makers.```

New para proposal:

````
1.1 Purpose

The purpose of this document is to inform thoughtful development and wide review of new charters, process evolution, new specifications and candidate additions to published recommendations, and to inform other horizontal review documents such as the Web Platform Design Principles, Privacy Principles, Self-Review Questionnaire: Security and Privacy or other similar checklists and sets of principles used by specification authors and editors.
````

## Plenary Session

Present: Dan, Peter, Amy, Yves, Hadley

Regrets: 


### Breakout Rollup

#### Breakout A

Dan: progressed PR 354

Peter: responded to some feedback

Dan: Rossen added a suggested change, should commit that

Peter: yeah

Dan: need Rossen to address other feedbacks

#### Breakout B

Peter: Rossen and I worked on a PR for CSS serialization guidence #367. Need feedback from Lea.

Dan: Anne left feedback.

Peter: we were trying to avoid the term idempotency because I don't think a lot of people know it

#### Breakout C

##### [EWP intro edits](https://github.com/w3ctag/ethical-web-principles/pull/77/)

Peter: changes look good to me

Dan: approved. We want Hadley's review.

Hadley: looks good. Looking at change line 107 .. implementations in conflict.. as opposed to web technologies or proposed web technologies.. particularly in early design review

**we wordsmith the introduction and then merge the results**

Peter: can we advance [to Statement]?

Dan: I think so.

**we resolve to ask Yves to publish it to TR**

##### Identity principles issue

Amy: went to close this after discussion in C, but reflected further, and decided not to. We suggested to close because of so much ongoing work in the area, but counterargument is that we should say something to guide this ongoing work to make sure it goes in a good direction, rather than standing back completely. Will think more about it.

Hadley: makes sense

### Issue Triage
