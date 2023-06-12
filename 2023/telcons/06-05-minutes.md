

1

# TAG Teleconference

2

#### 5-7 June 2023

3

​

4

---

5

​

6

## Agenda:

7

​

8

### Breakout A (Europe / US) - [2023-06-05](https://www.timeanddate.com/worldclock/converter.html?iso=20230605T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

9

​

10

* [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov

11

* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou

12

* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss

13

* PR [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

14

* PR [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

15

* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

16

* [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391) - @LeaVerou

17

* PR [First pass at #11, lots of TBDs](https://github.com/w3ctag/design-principles/pull/403)

18

* [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou

19

* [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)

20

* PR [Make 6.1 more inclusive of non-Web JS APIs](https://github.com/w3ctag/design-principles/pull/435)

21

* PR [Fix link to live-vs-static](https://github.com/w3ctag/design-principles/pull/439)

22

* PR [Give more guidance about how to monkeypatch well.](https://github.com/w3ctag/design-principles/pull/441)

23

​

24

​

25

### Breakout C (APAC / Europe) - [2023-06-06](https://www.timeanddate.com/worldclock/converter.html?iso=20230606T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

26

​

27

* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo

28

* PR [Restrictions](https://github.com/w3ctag/design-principles/pull/363)

29

* [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia

30

* PR [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)

31

* [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo

32

* [Request for design principle clarification: Warn explicitly against getters throwing exceptions](https://github.com/w3ctag/design-principles/issues/400)

33

* PR [Warn against getter throwing exception since it is a side effect](https://github.com/w3ctag/design-principles/pull/408)

34

​

35

### Plenary Session - [2023-06-07](https://www.timeanddate.com/worldclock/converter.html?iso=20230607T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

36

​

37

* How are we doing on this: [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)  

38

* Likewise: PR [Start developer version](https://github.com/w3ctag/design-principles/pull/386)

39

 

40

* Breakout Rollup

41

* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

42

​

43

-----

44

​

45

​

46

## Breakout A

47

​

48

Present: Peter, Amy, Tess, Lea, Yves, Rossen

49

​

50

Regrets: Dan

51

​

52

​

53

### [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov

54

​

55

PR [First pass at #11, lots of TBDs](https://github.com/w3ctag/design-principles/pull/403)

56

​

57

Lea: discussed at f2f. We got some TC39 input. PR 403 is way outdated.

58

​

59

Peter: can we close this, or use it as a starting point?

60

​

61

Lea: closing it.. we've discussed this extensively with Sangwhan in the meeting and it seems there is something to tweak the principles, but there's way more nuance than just don't have classes when you have both data and behaviour. There are a [bunch of ideas](https://github.com/w3ctag/design-principles/issues/11#issuecomment-1515585583) .. and some responses from TC39 people. Converting between objects and data-centric classes should be simple. Having properties on the APIs classes are associated with, needs further discussion.

62

​

63

Tess: something Anne and Dominic didn't agree with?

64

​

65

Lea: ..namespacing. Anything here we have consensus on that we could write?

66

​

67

Peter: I don't disagree with any of it. Comment about math.. doesn't seem to be a problem, but still worth documenting so it never becomes a problem.

68

​

69

Lea: fine with that. Pushback in the past about documenting principles that haven't come up as problems in reviews or apis.

70

​

71

Peter: lots of things that haven't been issues because everybody knows not to do this, and that should be documented. Common knowledge like that can get lost; documenting this stuff is our job.

72

​

73

Lea: some fluctuation around this if tc39 is discussing.. and about native modules that didn't really go anywhere that seems related. If we are going to document this I'd probably deprioritise it compared to other things.

74

​

75

Peter: we can refer to tc39 documentation

76

​

77

Lea: they don't have principles, but discussions about starting something

78

​

79

Peter: guidence .. as long as it's written down somewhere. Action to write a new PR?

TAG Teleconference
5-7 June 2023
Agenda:
Breakout A (Europe / US) - 2023-06-05

    Classes (WebIDL interfaces) should only be used when you have both data and behavior - @cynthia, @LeaVerou, @atanassov
    New principle: Guidance on when to use a child element vs an attribute - @hober, @LeaVerou
    Guidance about which state properties should be reflected as HTML attributes - @hober, @LeaVerou, @plinss
    PR New text re: balancing concerns between interoperability and implementability
    PR First pass on backwards compatibility principle
    New principle: Discourage overloading (in HTML) - @hober
    New principle: Guidance on options dictionaries and default values - @LeaVerou
    PR First pass at #11, lots of TBDs
    Web platform features that augment HTML elements en masse - @LeaVerou
    New principle: Avoid adding (non-constructor) functions to the global scope
    PR Make 6.1 more inclusive of non-Web JS APIs
    PR Fix link to live-vs-static
    PR Give more guidance about how to monkeypatch well.

Breakout C (APAC / Europe) - 2023-06-06

    General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)? - @cynthia, @torgo
    PR Restrictions
    New principle: Naming of factory methods - @cynthia
    PR New principle: Identity on the web
    New principle: Data Minimization - @torgo
    Request for design principle clarification: Warn explicitly against getters throwing exceptions
    PR Warn against getter throwing exception since it is a side effect

Plenary Session - 2023-06-07

    How are we doing on this: [Meta] Tackling design problems earlier than design review / A Q&A section for API design

    Likewise: PR Start developer version

    Breakout Rollup

    Issue Triage

Breakout A

Present: Peter, Amy, Tess, Lea, Yves, Rossen

Regrets: Dan
Classes (WebIDL interfaces) should only be used when you have both data and behavior - @cynthia, @LeaVerou, @atanassov

PR First pass at #11, lots of TBDs

Lea: discussed at f2f. We got some TC39 input. PR 403 is way outdated.

Peter: can we close this, or use it as a starting point?

Lea: closing it.. we've discussed this extensively with Sangwhan in the meeting and it seems there is something to tweak the principles, but there's way more nuance than just don't have classes when you have both data and behaviour. There are a bunch of ideas .. and some responses from TC39 people. Converting between objects and data-centric classes should be simple. Having properties on the APIs classes are associated with, needs further discussion.

Tess: something Anne and Dominic didn't agree with?

Lea: ..namespacing. Anything here we have consensus on that we could write?

Peter: I don't disagree with any of it. Comment about math.. doesn't seem to be a problem, but still worth documenting so it never becomes a problem.

Lea: fine with that. Pushback in the past about documenting principles that haven't come up as problems in reviews or apis.

Peter: lots of things that haven't been issues because everybody knows not to do this, and that should be documented. Common knowledge like that can get lost; documenting this stuff is our job.

Lea: some fluctuation around this if tc39 is discussing.. and about native modules that didn't really go anywhere that seems related. If we are going to document this I'd probably deprioritise it compared to other things.

Peter: we can refer to tc39 documentation

Lea: they don't have principles, but discussions about starting something

Peter: guidence .. as long as it's written down somewhere. Action to write a new PR?

Lea: I've written what came out of the breakout. Need to hear from others about what needs to be written and how it should be prioritised.
Meta

Lea: reoccurring problem about where certain design principles should live. CSS in particular.

Tess: if CSS produced principles and wanted to own it, we can link to it. They're welcome to.

Peter: we shouldn't be writing principles for other standards bodies like tc39

Lea: WHATWG and TC39 are both creating javascript apis, according to different principles. We shouldn't favour one over the other.

Tess: with both we need to work with them. It's easy with WHATWG because of shared history and way of working. TC39 is pretty distinct. We should work with them, but be careful not to step on toes.

Peter: tc39 do other things than for the web

Lea: value for everyone of the js apis are consistent, whether for the web or not. Fine to make this an explicit goal. Be great to have a process that applies to w3c groups and non-w3c groups. A task force? Where we collaborate with the group on the principles that apply. It would mean splitting out the CSS design principles to be separate from the rest, or separate JS API design principles. I think it's worth it to get more input for these groups. Better than fragmentation between different principles documents. Last bullet contentious. First bullet not relevent. Middle three something we can write about?

Peter: yes

Rossen: I don't see agreement on the middle three. But not pushing back?

Lea: yeah, same assumption. Ask explicitly?

Rossen: ask through a PR

Peter: we can add all the points and settle contention in a PR. Just needs someone to write.

Lea: it's already to-write for me. Could see two principles coming out of this.
New principle: Guidance on when to use a child element vs an attribute - @hober, @LeaVerou

Tess: I'll attempt to do this this week
Guidance about which state properties should be reflected as HTML attributes - @hober, @LeaVerou, @plinss

Lea: On me, but can't do it this week. Doable for next month.
PR New text re: balancing concerns between interoperability and implementability

Tess: Dan and I worked on it in Tokyo. Things we didn't get to. Need to re-read. Many rounds of edits took us away from the original point - documenting tradeoffs in a failure case. Text doesn't make it clear that it's bad that we're here, but here are ways forward (which are differently bad). Sangwhan had feedback that it ought to be more positive. That would stop it communicating the right thing, that we dont' want to end up in this situation. Not ready to merge. Also doesn't hit Alice's lead with the conclusion. There isn't a singular conclusion/takeaway - it's "please don't end up in this state". Hard to summarise. Also looking at Dan's suggestions. I'd like Alice's review before merging even when it's ready.
PR First pass on backwards compatibility principle

Tess: unresolved comments.. Comment from dbaron, might need a new paragraph.

    I think another question worth considering is something like "is the feature specified well enough and open enough that implementations that don't already implement it can do so". (If the answer is no, I think that's an argument in favor of either (a) removal or (b) doing the work to change the answer to yes.)

New principle: Discourage overloading (in HTML) - @hober

On Tess to write. She'll try to set aside time this week for this.
New principle: Guidance on options dictionaries and default values - @LeaVerou
Web platform features that augment HTML elements en masse - @LeaVerou
New principle: Avoid adding (non-constructor) functions to the global scope
PR Make 6.1 more inclusive of non-Web JS APIs
PR Fix link to live-vs-static

merge
PR Give more guidance about how to monkeypatch well.

Lea: we had some feedback. Some edits I haven't reviewed yet. Some tc39 folks have weighed in.

Rossen: who added the CSS one?

Lea: Jeffrey, with feedback from CSS folks.
Breakout C

Present: Amy, Dan, Max, Yves, Sangwhan

Regrets:
General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)? - @cynthia, @torgo
PR Restrictions

Sangwhan: needs editorial changes. Needs guidence on roughly what to use when. What would be the best choice by default. Need to spend some time on this. Noninteroperable stuff should be thrown out.

"Do this; if your design does this, use this, if your design does this, use this, otherwise ..."

Sangwhan: what we're trying to do here is - for majority of cases use our guidance...

Max: I can work on this. There's also a TODO note - should do this first?

Sangwhan: and check if the interoperability has changed in the last year. Permission Policy is now in TR. Secure Contexts is interoperable, think Document Policy isn't yet but it might have changed.

Max: interoperable means if there is a published standard?

Sangwhan: if there's at least one implementation.. some are not implemented at all. Ideally two. Two engine implementations as the gate for putting it in a principle. Or if it's in TR space it's formal enough, unless it would break things.
New principle: Naming of factory methods - @cynthia
PR New principle: Identity on the web

Amy: No update
New principle: Data Minimization - @torgo
Request for design principle clarification: Warn explicitly against getters throwing exceptions
PR Warn against getter throwing exception since it is a side effect

Dan: raised by somebody in the community on the basis of #400. Been some discussion, work by Tess and Lea. What's the story?

Sangwhan: we need to merge. Main blocker was bikeshed errors.

Dan: one outstanding suggestion not marked as resolved

Sangwhan: Lea wants it to be setters, not sure if I agree with that.

Dan: leave a comment and let's try to merge this at the plenary call.

Amy: merge without lea's change and..?

Sangwhan: lea can add another PR if she disagrees.

Dan: we can merge and talk about it on the plenary call

Sangwhan: to incorporate this we'd need to make other changes too, so happy with that

Dan: [comment and merge]
Societal Impacts Questionnaire

Dan: Web of Things filled this out recently. They've done a good job. They've talked about general internet of things, rather than spcific features of their spec

Amy: they have written that many of the questions assume a web browser but that was not my intent so that's another feedback point.

Dan: we should get some wide review

Dan: good feedback from Rick Byers

Amy: good feedback from AC

Sangwhan: some redundancies with S&P questionnaire... technical questions... opt out.

Amy: not only a technical question. Need to make that more clear. I'd like to draw that out - if the reaction is "there is a tech solution" but actually not. Also this not a test you pass or fail. Intended to get people thinking about this. Right now it's difficult to fill out.

Dan: key part of the purpose, to get people thinking about the impacts, similar to security & privacy questionnaire. Simplifying would be a good way to help. Crisp but nuanced.

Yves: maybe something like adding examples, eg. q2 has one. We can add more. Eg. battery sensors - was used to raise the price of something so people had to decide quickly. Bad examples of features added wth intent to be useful, but were misused or lead to privacy invasive things.

Sangwhan: battery sensor not a great example. Attack was theoretical, not much in the wild, mitigated before there was wide adoption.

Dan: geolocation. Introduced early on, but started to appear more and more on the front page of things..

Amy: there's an issue for adding examples - suggestions would be good there

Sangwhan: brings the bar very high for people bringing us reviews. Uncomfortable making this compulsory.

Amy: agree, concerned about that too. we don't know how we would use it - we don't want to increase the bar - point to make that people building powerful features on the web platform should perhaps slow & think about these issues.

Sangwhan: I like the intent of making people think about it. Similar to the intend with the a11y questionnaire. Making it a lean process could make it easier for people to go through it.

Dan: trying to think of wording we could put in issue template - encourage you to take a look, optional. What we do with BFCache - item in the design principles. We could add something that is something like do not cause harm to society.. already in ethical principles.. something more design princple-y that riffs off that, with a link to the additional document.

Amy: optional considerations - and we could bring it out for particularly contentious design reviews....

Sangwhan: we should use it for powerful features...

more discussion of how this fits into TAG

Dan: let's figure out how to make it visible - whole point is to raise awareness to engineers creating new features but may not have been thinking about this or be incentivised to think about these issues. Similar to privacy principles and priority of constituencies. Point of wide review. But also don't want to overwhelm them with too many things or feel like they're being preached to or that it's adversarial. We've got to have the right balance.

Sangwhan: we want to be careful about mandating... e.g. some CSS features might not have any societal impacts...
Plenary Session

Present: Peter, Amy, Yves, Rossen, Hadley, Max

Regrets: Dan
DPUB ARIA

Okay to close?

Rossen: looked through this, familiar with ARIA and mapping. One part that wasn't super clear was what was in scope for our review. First CR? Fine with this.

closed
How are we doing on this: [Meta] Tackling design problems earlier than design review / A Q&A section for API design

Lea: there have been some discussions. People dont' know yet what kind of questions to post. I think we should seed it ourselves to demonstrate. I tried to do when I was editing color api spec. If any of you are working on specs where api design questions come up that are too small for review it would be good for you to post them. Or when people reach out, direct them there to ask. We need to push it a little bit.

Peter: and we need to make sure we're paying attention to give answers

Lea: so far every question has discussion. Broader TAG community is fine, not just us

Peter: do we have enough visibility to know these conversations are happening - not on our agenda yet.

Lea: motivation was that we wouldn't be bringing them up on our agenda.

Peter: how do we get people on the TAG to pay attention?

Amy: we could just check on it monthly in design review week like we are right now

Lea: lots of questions may spark a design principles issue that will go on the agenda

Peter: standing item to review discussions. Chicken and egg - if people do post questions and don't get useful questions it's not an incentive. We do also need to fill the pipeline. The last comment on our issue was that Rossen was going to reach out to blink-dev and Tess was going to follow up with webkit. Did that happen?

Lea: I got useful responses about the color api from anne and dominic. A lot of the time is all you want is figuring out precedent. Just to try to have it more top of mind. Do people get these questions? Sometimes people reach out to me and ask things. I have tried to direct people here.
Likewise: PR Start developer version

Lea: Sangwhan and I need to sit down and work on it. Hoping for in f2f but there was no time. Nice to prioritise this next time - assign to a breakout with me and Sangwhan. It's a lot of work, not difficult.
Next f2f

Nothing scheduled until TPAC.

Lea: CSS WG meeting in California - 4 of us in CSSWG - could do it at the end of that. July 18-21.

Peter: could do a split f2f - Europe and CA. We typically don't get a lot of TAG time at TPAC so usually have extra time before or after.

discussion about how great Edinburgh is

Pencil in: week of 10th July (Hadley can't do before 26th). Rossen can't do week before CSS. We could do them separate weeks. Lea to ask for more feedback in Slack.
Breakout Rollup
Breakout A

Committments to write things up from Tess and Lea. Alice's feedback needed for one PR.

Did anyone ping Alice about feedback?

Update on monkeypatching - ready to merge?

Lea: change seems good to me. Can nitpick - change assumes different communities, but monkeypatching can happen in the same community. But it's clear enough.

Peter: Concern is groups patching other people's stuff.

consensus to merge
Breakout C

Max agreed to work on a PR. We merged a PR 400 without incorporating feedback from Lea, Lea may want to follow up with Sangwhan. Talked about societal immpact questionnaire.
Issue Triage
