## TAG Teleconference
##### 01-03 February 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2021-02-01](https://www.timeanddate.com/worldclock/converter.html?iso=20210201T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [give advice on read-only lists](https://github.com/w3ctag/design-principles/issues/50) - @dbaron
* [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov
* [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov
* [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185) - @hadleybeeman, @atanassov
* [Extend Other API Considerations section to include expanded impacts](https://github.com/w3ctag/design-principles/issues/212) - @torgo

#### Breakout B (US / APAC) - [2021-02-02](https://www.timeanddate.com/worldclock/converter.html?iso=20210202T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron
* [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55) - @cynthia, @dbaron, @timbl, @plinss
* [Add naming tips for getter-likes/selector-likes](https://github.com/w3ctag/design-principles/issues/136)
* [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron
* [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

#### Breakout C (APAC / Europe) - [2021-02-02](https://www.timeanddate.com/worldclock/converter.html?iso=20210202T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice
* [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia
* [describe principles for naming of locking/unlocking APIs](https://github.com/w3ctag/design-principles/issues/85) - @cynthia
* [Clarify events vs observers even further if possible](https://github.com/w3ctag/design-principles/issues/127)
* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo

#### Plenary Session - [2021-02-03](https://www.timeanddate.com/worldclock/converter.html?iso=20210203T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage


-----


### Breakout A

Present: Amy, Dan, Peter, Lea, Yves, Rossen

Regrets: Sangwhan, Kenneth, Tess

#### [give advice on read-only lists](https://github.com/w3ctag/design-principles/issues/50) - @dbaron

Dan: since rossen wrote the [last comment](https://github.com/w3ctag/design-principles/issues/50#issuecomment-698045074) with a proposal 

Rossen: this can be assigned to me - not ready to discuss at this point. 

Rossen: We went back and tried to untangle this - different types that were added. Where and how should read-only lists be used?  Parameters, Attributes and Return Values... If you go and read the initial set of guidance - it was inconsistent - some things sound immutable but may not be. There's another one - mutable data structure with immutable types inside. A lot more applicable in a functional usage... I pieced all of these together.  

#### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov

Rossen: we did have a take-away that needs to be captured in text.  Overall - start breaking down your feature into layers as much as poss, when you go about exposing it expose it from as high a level as possibile - rather than starting low from a bunch of primitives. 

Dan: Also see [minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/05-04-minutes.md#high-level-or-low-level-apis---hober-alice-dbaron-atanassov) where we discussed.

Rossen: I'll write it.

#### [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov

[moved to B]

#### [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185) - @hadleybeeman, @atanassov

Rossen: proposal to move crypto alg to web crypto...

Rossen: we're not crypto experts - unless there is a security group. Our proposal is in the issue.

Dan: Hadley possibly working on text.

[punted to C]

[also : should this be a finding?]

#### [Extend Other API Considerations section to include expanded impacts](https://github.com/w3ctag/design-principles/issues/212) - @torgo

Rossen: I have question - what exactly is the motivation? What is the ask? What other considerations should we have?

Dan: should we close this and point people to the ethical principles?

Amy: should we have text in the design principles that says "you should look at the ethical principles" to consider the effects?

Dan: we should have that wording in here.

Rossen: a good opening paragraph for section 1. One or 2 opening sentences that states that.

Lea: should there be a statement in the ethics doc saying the same thing?  There is a lot of overlap between the ethical principles and the design principles in section 1- 

Rossen: the difference in my view is that in section 1 we are .

Lea: the ethical principles should be numbered. I filed [an issue](https://github.com/w3ctag/ethical-web-principles/issues/33) on that.

Amy: i think it [ethical principles](https://www.w3.org/2001/tag/doc/ethical-web-principles/) should have a toC.

[Closed and commented]

[Issue to better link DP and EWP](https://github.com/w3ctag/design-principles/issues/282)

### Breakout B

Present: Peter, Tess, 

Regrets: Sangwhan


#### [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov

#### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron

#### [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55) - @cynthia, @dbaron, @timbl, @plinss

#### [Add naming tips for getter-likes/selector-likes](https://github.com/w3ctag/design-principles/issues/136)

#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron

#### [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron


### Breakout C

Present: Dan, Ken, Lea, Amy

Regrets: Sangwhan, Hadley

#### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice

Dan: we've looked at this several time and nothing has been written

Ken: I could look but not this week. Sounds like a breakout with me and Sangwhan.

Dan: [left a comment](https://github.com/w3ctag/design-principles/issues/39#issuecomment-771469636)

#### [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia

#### [describe principles for naming of locking/unlocking APIs](https://github.com/w3ctag/design-principles/issues/85) - @cynthia

#### [Clarify events vs observers even further if possible](https://github.com/w3ctag/design-principles/issues/127)

Ken: we have someting already in design principles?

Lea: [we do.](https://w3ctag.github.io/design-principles/#events-vs-observers). You start with events and move to observer if you have solid raesons to, and there's a list of reasons

Ken: fires too often?

Lea: in a review I was recently in Peter and I disagreeda bout whether something should be an event or observer so we should make sure we're all on the same page.

Ken: events had advantaes like bubbling, and easier tow ork with

Lea: many people see events as something that happens on dom nodes. When it's a single object do you create a single object and fire events on it or is it still an observer?

Ken: depends... you can assign event listeners and youc an start it.

Lea: that was the root of the disagreement, it was a single object that was not a DOM node. It could be an event target, Peter was saying it's fine to be an observer.

Ken: hard because we want a consistent web platform and observers is a new thing on the platform as a whole. With generic sensors, I don't think people are really using observers, but in retrospect having something firing 60 frames per second it's a lot of overhead to events. If you had an event when something changed it didnt' give you the data.

Lea: that could be part of the extra clarification. Right now there's nothing about performance. Only if observers would prevent recusion they might be a good idea, but nothing else apart from that

Ken: a callbakc sometimes is very efficient, eg. for one with event target if you don't really need bubbling

Lea: if you have a singleton that's not a DOM node or anything, is eventTarget still a good idea?

Ken: I know people use it becausae it fits with the rest of their code. If you don't have a lot of events its not an issue. Had to polyfill inheriting eventtarget in safari. Wanted to instantiate something and hook up events to it. But nt high frequency so not really an issue. You even get the high frequency issue with DOM nodes. Two days ago there was a person doing custom elements firing often, they discussed whether to use callback or events because events have overhead. When you're doing animations you want to conserve battery and get as many frames as possible. In this case having ot create an observer to listen to a DOM node, that's also a bit hostile in developer experience.

Lea: in terms of developer experience events are easier than observers

Ken: theyr'e tied to the thing you want to listen to, observers are this external thing

Lea: observers are more different, different APIs, whereas once you know how events work

Ken: what developers really want is streams in some of these cases. Like for a sensor or a rendering loopback, you want something based on streams, you're just getting data
.. the same thing with streams, it's all about the developer experience, how hard is it.

Lea: do we have streams on the web platform?

Ken: we have streams, some integration with fetch, but not in many places. It moved slowly

Yves: web transport is based on streams

Ken: web serial also is. But you don't have streams in the DOM

Dan: is that a design principle - when do you use streams instead of events or observers?

Ken: yeah

Dan: if you're dealing with a stream of data, abstracting that into events might hinder peformance

Yves: events may be paraellised and without order, but streams expect order

Ken: with a sensor you want order otherwise you can't interpret the results. It's hard to come up with a recommendation today, but we could say something about perfomrance. We had the recommendation before, if you had a high frequency event don't copy the event data with every event, just do it as a change event so the user will have to query the data themselves. Something like that could be a recommendation.

Yves: depensd on the kind of events, whether you want to have all the events you will get them because you need them, and in some cases you can drop or sample them. It depends on what you want. The possibility of dropping or sampling events can be useful.

Ken: in general a sensor is dropping because it reports at a frequency

Yves: security sensor is case where you don't want to sample

Ken: what matters is the timestamp, and order

Yves: provided an accurate clock

Dan: too low level for design principles..

Ken: record some of the things to consider, no information here about streams and we're using streams already, so that's missing

Dan: leave comments in the issue to summarise. Leaving [comment about streams as alternative](https://github.com/w3ctag/design-principles/issues/127#issuecomment-771464855).

Ken: [ramblings](https://github.com/w3ctag/design-principles/issues/127#issuecomment-771467491)

#### [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo

Ken: should be actual use cases

Dan: that could be design feedback

Ken: one thing is to say please consider debugging, maybe it should be part of the explainer.. if we want people to consider this it should be in the explainer not design principles

Dan: alice linked to [previous discussion](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/07-06-minutes.md#taking-debugging-use-cases-into-account-in-w3c-specifications---torgo) from july..
... the person who filed mentioned webanimation as a good example and flexbox as a negative example
... sangwhan mentioned meaningful errors

Ken: it's very different, flexbox is something visual, you need dev tools to help debug things, very different than a javascript api like webanimations. 

Dan: we could say something like "have you accounted for debugging in your use cases?"

Ken: adding that to the explainer draft would help. We could add it to the github issue template to submit a review request

Lea: I'm a little skeptical, it seems that with every api eventually tooling is ging to be built around it. if the API itself is designed with tooling in mind that could influence design decisions in a way that might negatively impact other use cases. Whereas, it lists flexbox as an example of an api not good for debugging, but justl ike grid there will eventually be better tooling for debugging flexbox, that happens with every feature. Seems like a temporary problem with every API, but apis should be designed to last, not designed around temporary issues

Ken: flexbox you need tooling. Other apis like js you need hooks for when things happen. But then you run into issues with fingerprinting

Lea: every api is debuggable, the question is how much custom tooling code you need

Dan: is there a generalised statement we could make that would not push people

Ken: most people wont' even find the statement in the design principles, will it make a difference? unless you're looking for it. That's why if you want something it needs to be in the explainer or issue template

Dan: yeah, the first place should be the design principles, and then in the explainer/issue template as well. if it's a principle that we're asking people to adhere to in the design of their API it should be in the design principles

Ken: what should I do to make my spec debuggable? a well defined spec and lots of tests. If behaviour is different across platforms its hard to debug

Lea: anything that makes it testable makes it debuggable

Dan: is that feedback we could leave in the issue and see if that resonates with the requestor? I'd like to be responsive

Ken: when you implement the feature for layout tests you end up adding a few extra functions for debugging, for writing tests. Maybe the text shold say maybe "you should consider whether those should be standardized or not". That happens today, I've seen that in multiple places. Consider whether that should be exposed or not.

Dan: Possible text?
`In the context of API design, consider whether hooks implemented for testing and debugging purposes should be part of the standard - if they would help web developers debug their applications. Balance this against the need to not expose additional information (e.g. device-specific information) which could be used for fingerprinting.`

Dan: the point is it should be in the standard if it is something that helps developers

Ken: and make sure you don't introduce too much fingerprinting, there are other considerations. This is a reason you don't want to expose it.

Lea: what is good for fingerprinting?

Ken: we sometimes have hooks in apis for testing that expose a lot of data

Lea: a specific example?

Ken: no, when we implemented sensors, sometimes we had hooks to turn on things, and query some more specifics like highest framerate on the sensor, to do testing, but that is really precise information you could use for fingerprinting. Sometimes when you have those hooks its worth considering whether theymake sense for other people for debugging, but you need to have other things in mind, it's always a balance. I'm just thinking out loud. Other cases with CSS tests where you have a specific function that clears state or does some layout that is really expensive. Exposing that to develoeprs might be really bad, they might abuse it. There are a lot of things to consider. Eg. function that resets state because that's often what you want for testing. That might not be cheap. 

Dan: ..is typing..
.. Leaving [comment](https://github.com/w3ctag/design-principles/issues/156#issuecomment-771456814)

Ken: will add [additional thoughts](https://github.com/w3ctag/design-principles/issues/156#issuecomment-771457810)


### Plenary Session

Present: Kenneth, Tess, Amy, Lea, Peter, Rossen, Dan, Yves

Regrets: Hadley, Sangwhan

#### Breakout A

Rossen: first topic was **read-only lists**.  This was something David and I worked on. We were able to gather the different types currently defined and arranged those as a set of recommendations.  What for parameter passing, what for return-types. All of that is ready to be written. The action is on me.  Next was **high level vs. low level**. Alice had an action item on this. We agreed to spec it. Alice might write but I will have the action.  **permissions & similar mechanisms** - we waited for tess for another breakout. **security & crypto** waiting on hadley for some text. **extend other API considerations** Issue 212 - that was motivated by Brad R. - much broader scope. Impact to to society... We agreed this is mostly in the Ethical Web Principles.  Amy also pointed out some missing correlation between design principles & ethical principles - assigned to amy. We closed this one. 

#### Breakout B

Tess: Breakout B was just Peter & me. We did a bunch of misc. things.  I landed some **security & privacy review PRs**. We renamed the default brances to main rather than master.  We talked about harmonizing permissions.  We had been working with PING to get them to elevate an email to an official PING doc - that has been stalled a bit but will happen soon.  Underlying architectural question of the issue - figuring out an appropriate venue to raise an issue.  

#### Breakout C

Dan: **privacy related design notes and device apis** I left a comment, it's old (39).

Ken: scheduled for next f2f with me and sangwhan

Dan: special breakout, and maybe not time sensitive. 
... issue 70, **improved guidence on attributes vs methods** - sangwhan was not there so we didn't talk about it.
... **clarify events vs observers** good discussion (see minutes), Ken left a comment, and assigned to next design review week.

Ken: a lot to be done, we don't have a recommendation around streams, but it's used more and more. No rec about events vs observers and when to use. Need some time to figure out the rec. We can use info in the issue in future.

Dan: **taking debugging use cases into account**, from community, long discussion. We want to be responsive. Left comments and had [one back](https://github.com/w3ctag/design-principles/issues/156#issuecomment-771514091). We need to review comment and do more work. Assigned to next design principles week.

Ken: adding debugging info is sometimes great, but there's a balance with fingerprinting and performance. 

#### Ethics - should it be a numbered list?  Should it have a ToC?

Lea: so people can refer to each more easily, and so they can be expanded in future with examples

Tess: no opinion on numbering, but an opinion about how they're marked up for citing. There's one thing in the ToC. I would like the ToC to be each principle. Numbering is for free when these are sections. I like how short they are, don't want the text to get longer. But nice to have a useful ToC.

Dan: I'm happy to do that. We did discuss about if we should have more examples. I think they might be worth having, but I want to keep the principles themselves short and sweet. The idea we had was that the ethical principles links into the design principles and the security and privacy questionnaire. That also led to discussion about adding text to design principles intro to connect the two. Newer design principles now link to relevent ethical principles, eg. priority of constituency. We need to do a read through and link to the appropriate ethical principle.

Tess: I'm for it

Rossen: numbering principles will add context and meaning to people and open the debate for which is more important than others.

Lea: our other web platform design principles are numbered, does that mean one is more important than the others? CSS is more important than event design?

Rossen: they are very different and not overlapping. Inside each we spent time ordering the subsections. So, yes. The inner order, if there is an order, will imply meaning.

Peter: we do carefully order them, not sure that implies priority.

Dan: it was intentional to put there is one Web as the first principle. A little bit of semantic meaning. But below that it's arbitrary. It's not necessarily the case that people will derive meaning from the ordering if they have a number vs if they don't have a number.

Rossen: it's easier to say we didn't order them with numbers so it doesn't matter... 

Peter: if we number them that implies we have to keep the numbers stable over time. Need to be careful about that. And if we change markup, need to make sure existing anchor stays stable

Lea: another issue - we discussed adding an html design principle - does that mean we have to add it to the end so the numbers stay stable?

Peter: I don't know that people refer to the design principles as 3.4.1

Tess: I hope they're not

Peter: we need to serve a static file not respec

Yves: easy with a gh action. Once the markup is stabalised I can work on that

Dan: do we want to try to publish this in a different way? It's in TAG url space under w3.org/2001/.. put it into TR like design principles and security and privacy questionnaire?

Tess: in the long run yes on TR. 

Yves: as a finding?

Tess: it is. Findings don't go in TR space

Ken: will regular people care?

Dan: people might get confused by 2001 in the URL. General issue. Having it in TR gives it more weight. Same place as other technical reports.

Ken: I want a short URL.

Peter: we can put up redirects at w3ctag.org

#### Design Review issues triaging

Rapid assigning of issues to people who will figure out the status.
