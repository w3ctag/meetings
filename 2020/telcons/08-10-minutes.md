## W3C TAG Minutes Doc for Week of 10 Aug 2020

### Breakout A (Europe / US) - [2020-08-10](https://www.timeanddate.com/worldclock/converter.html?iso=20200810T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111) - @hober, @kenchris
* [guidance on use of JSON-LD?](https://github.com/w3ctag/design-principles/issues/128) - @hober, @dbaron, @hadleybeeman
* [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov
* [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron
* Security & Privacy Questionnaire Open Issue - @hober

### Breakout B (US / APAC) - [2020-08-10](https://www.timeanddate.com/worldclock/converter.html?iso=20200810T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [current PRs](https://github.com/w3ctag/design-principles/pulls) - @alice
* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice
* [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov
* [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia
* [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-principles/issues/157) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2020-08-11](https://www.timeanddate.com/worldclock/converter.html?iso=20200811T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron
* [Best practices for feature detection of DOM API](https://github.com/w3ctag/design-principles/issues/137) - @torgo, @ylafon, @kenchris
* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo
* [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon
* AB proposal on elected body communications policy

### Plenary Session - [2020-08-12](https://www.timeanddate.com/worldclock/converter.html?iso=20200812T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

## Minutes


### Breakout A (Europe / US) - [2020-08-10](https://www.timeanddate.com/worldclock/converter.html?iso=20200810T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present:  Dan, Tess, Rossen, Ken, Yves
Regrets: Peter, David, Hadley

#### [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111) - @hober, @kenchris

Tess: Still waitinf on an HTML change to land. 

[bumped]

#### [guidance on use of JSON-LD?](https://github.com/w3ctag/design-principles/issues/128) - @hober, @dbaron, @hadleybeeman

Dan: we kind of need Hadley for this one...

#### [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov

Dan: Is this a design principle? Or is it a gripe about the web platform?

Tess: This honestly feels more like a design review issue to me... Or an issue for the internal guide for doing design reviews... It probably does make sense for the design principles doc to have something about permission. Currently we have sections in the end that forward pointers to other docs. This could just be a pointer to Nick's guide. But for spec authors that want to add something that needs permission how do we guide them?  We can't (in the design principles) write a new extensible framework for permissions.

Dan: what's the status of nick's doc? 

Tess: it's being worked on in PiNG.

Tess: it is being updated but not regularly.

Dan: we could ask Nick.

Tess: I can do that.

#### [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron

Dan: bump this?

Rossen: we discussed this during breakouts - we had decent discussions about "this isn't really about data loss"... Presentational content loss... we had a discussion last time... we decided to wait for david to see if he wanted to add anything else in the CSS section around that... which is about designing CSS features... That was about it... I don't think there's anything else left. Maybe getting some text in the CSS section about preserving content presentation ...

Yves: how does it relate to the evergreen finding? If you are using a TV browser you may miss things - losing some data (presentational maybe)...

Rossen: this adds more to the point that we discussed - as we discuss "no data loss" it can be interpreted as most things on the web...  ... no content loss differential between feature implementation ... "make sure your features are backwards compatible" should be the principle. The idea is that it shouldn't break.

Yves: should it be the same if you're introducing new javascript APIs? should you warn people they should design as if some APIs may not be implemented. 

Rossen: perhaps - but not sure ... Media feeds API... some implementations want to add. WOuld that potentially result in a data loss... if I'm in a browser that doesn't have this feature...

Dan: any suggested text?

Rossen: it should have been in section 3.1 or before that... overall guidance about extending CSS.  instead 4 subsections which are the "how" so I think this principle is still missing.

Dan: could it be as simple as adding some text like you proposed - backwards compatability of features.

Rossen: yes - we've had multiple discussions 0 how do you preserve content visibility for non-siggted users or users with alternative presentational systems. We could add a a sentence about designing features for accessibility.

Rossen: I'll do a PR and we can close this issue with that.

[we'll try to close this week]

#### Security & Privacy Questionnaire Open Issue - @hober

#84 - bad or good behaviour by first parties...

Tess: [recounts issue](https://github.com/w3ctag/security-questionnaire/issues/84)  - I think one thing that has comne up is - David Baron said this in June - there is a fundamental difference between 1st and 3rd party. Users understand that they are visitng the first party and don't understand that 3rd parties are involved.

Dan: I thin it's OK to close this one.

Tess: this is a joint doc with PiNG - we need to be on the same page.  In this particular issue dbaron made the difference between 1st and 3rd parties very clear. I think we can close it using David's text as justification.

... issue 80 - that nick filed. [local storage](https://github.com/w3ctag/security-questionnaire/issues/80)

... if your browser has a "clear website data" button and it doesn't clear everything then you have a bug.  Anne is working on a mechanism for specs to hook into "clear all data"...  

Dan: move to design principles?

Tess: OK.

... [Privacy mitigations for identifiers](https://github.com/w3ctag/security-questionnaire/issues/79) - yes I agree. this is a to-do. We should go into detail on this.

... [explain how to deal with issues in their specs](https://github.com/w3ctag/security-questionnaire/issues/88) - the concern is - people fill out the questionnaire and then answer "yeah" to a bunch of questions. What happens then?  Kind of implied that you should fix the problems.  Some people see filling it out as a box ticking excercise.  So when we get things coming in for a design review - and there are concerns that they found - they shhould have already addressed.

Dan: it should at least say "talk about the issues and discuss possible mitigation strategies"

Tess: or state a rationalie for why you're not doing it.

### Breakout B (US / APAC) - [2020-08-10](https://www.timeanddate.com/worldclock/converter.html?iso=20200810T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Rossen, Peter, Alice, Tess

Regrets: Sangwhan, David

* [current PRs](https://github.com/w3ctag/design-principles/pulls) - @alice

Alice: Good time for people to start looking and providing feedback to issues that have been assigned to them.

Rossen: Looking at https://github.com/w3ctag/design-principles/pull/229 - this is a great thing to add.

Alice: This is now part of the process as issue #20 since it is more general than the principles doc.

Peter: So should we have something in the principles doc?

Alice: No, the process repo is where the style guide goes and that should be sufficient.

All: Read the PR, approved and merged.

* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice
* [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov

Rossen: So how relevant is the topic at this point?

Peter: Well, the answer to this is Layers... not an either or question

Alice: Right, you have a high level API for the convenient version and a low level API that would allow you to futher extend or adjust the behavior.
... on top of Travis' comment, also a11y API struggle from being too high level and not easy to extend.
... What guidance can we give about designing low level APIs, taking the principles about safe-to-browse etc. Is there a lowest level that we can point to?

Peter: It depends. We shouldn't encaurage such high levels that would encaurage or mean redefining or redescovering the entire stack to change one aspect.

Alice: Do we have examples of this being done well and poorly?

Rossen: The WIndows platform has a pattern of exposing low level API behind a Core namespace and convinience API of the feature built on top.

Tess: One thing I often get lost with this topic is... there is a destinction between the model behind an API and the API itself. It almost feels we're mixing few things. Should the Web even have low vs high level API? You can argue the "let's only add primitives" and you can argue the opposite. We should be doing both and have advice that suggests the model of new features conform with the current Web. Ex. JS is GC but we shouldn't be defining features that are or aren't designed around this fact. 
... What does the user need? Meet that at the appropriate need. You're building a thing that build on top of and around of other things.

Peter: Assume primitives exist and when designing features this should be considered as being exposed.

Tess: Sure, there's the forms controls recent example that is now forcing us to define the internals of things that have existed for long time.
... Priority of consituincies comes to mind - what best solves the problem of the end user?

Alice: The argument of "should be an HTML element" never happens. We've seen this with declerative shadow DOM but it shouldn't become an enemy of the shipped DOM.

Rossen: Gives an example about CSS Houdini and how we're now trying to expose lower primitieves of the underlying engine.

... discussion about the history of rendering engines and CSS Houdini :)

Alice: So is that a good pattern to follow? Is that level low enough?

Peter: It depends, for example we aim to expose the CSS parser all the way down to the token level so that people don't have to write more and more such parsers but stil be able to extend them.
... With the CSS Box tree for examples it was never defined cleanly but rhather exposed through a number of other features.
... We should be careful that we are consistent with the Web Manifesto. 

* [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia
* [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-principles/issues/157) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2020-08-11](https://www.timeanddate.com/worldclock/converter.html?iso=20200811T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Alice, Dan, Yves, Sangwhan

* [current PRs](https://github.com/w3ctag/design-principles/pulls) - @alice

Alice: some are ready and some really need input...

[Basic Principles](https://github.com/w3ctag/design-principles/pull/219)

Dan: let's land it.

[none opposed]

Alice: next one is [design across languages](https://github.com/w3ctag/design-principles/pull/220)

... Tess needs to look at it and review commments from dbaron are pending...

Alice: made the changes I could... there was one other one - don't reveal private browsing mode engaged principle - moved an example up about payment request. David wasn't sure it's a good example. He might be right.  

Dan: let's punt this to plenary to get Tess's feedback.

Alice: [CSS Section](https://github.com/w3ctag/design-principles/pull/221/) - only one review so far

... someone from CSS should look at it.    Peter and rossen need to look.

Alice: [javascript section](https://github.com/w3ctag/design-principles/pull/222)

Ken: I will have a look at that.

Sangwhan: I will take a look.

Dan: Ecmascript binding comment...

Alice: The fact that webidl puts its ecmascript separately doesn't mean you have bindings in any other language.  I should spell that out.

Sangwhan: not sure if function pointers is appropriate.  In javascript it would be a reference.

Alice: is there a better term?

Sangwhan: function reference?

Alice: changed

Ken: ..adding a lot of small comments... ... canonical URL ...

Alice: it seems like that is. using ".es" sinct it's Ecmascript.

Sangwhan: i think the rewrite loses some important info...

... looking at the part about garbage collection.  There are subtle things in here.   Need some time for this.

Ken: if something updates - examples.  

Alice: i think that's in the events section.

... on [types and measures](https://github.com/w3ctag/design-principles/pull/224)

Sangwhan: noting issue with bigint section...

Alice: I'll put it back in.

Dan: shall we punt that to the plenary?

Alice: also looking for an example of something that doesn't use `DOMError`... 

Ken: in thw webidl spec - [section 2.8.1 error names..](https://heycam.github.io/webidl/#idl-DOMException-error-names)

Yves: e.g. indexdb replaced domerror with exceptions...

Sangwhan: I think today most of these things are `DOMException`s.

Alice: can we take that out?

Sangwhan: I think so.

Dan: So change it to "Use `DOMException` for errors"?

Sangwhan: `ECMAScript` errors would be outside of the DOM.

Sangwhan: my review is in on this.

Alice: [OS & Device Wrapper APIs](https://github.com/w3ctag/design-principles/pull/225)

[discussion on fingerprinting]

Sangwhan: example might be remote playback API... you can differentiate between e.g. chromecast and appletv... 

... not sure if we can point to a specific spec... 

... webgl is another example...  You can somewhat reliably detect chipsets and driver versions... 

Alice: I will land this one now.

* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron
* [Best practices for feature detection of DOM API](https://github.com/w3ctag/design-principles/issues/137) - @torgo, @ylafon, @kenchris
* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo
* [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon
* AB proposal on elected body communications policy

### Plenary Session - [2020-08-12](https://www.timeanddate.com/worldclock/converter.html?iso=20200812T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Alice, Peter, Tess, Rossen

Regrets: David, Sangwhan

#### [Media feeds](https://github.com/w3ctag/design-reviews/issues/477)

Rossen: We drafted a response on the media feeds issue

[wordsmithing of the closing comment on this one...]

...[closed and commented](https://github.com/w3ctag/design-reviews/issues/477#issuecomment-672613700)... [based on consensus view]

* Breakout Rollupz

* Issue Triage
