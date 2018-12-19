## TAG Teleconference
##### 19 December 2018

Present: Dan, Travis, Peter, David  
Chair: Dan  
Scribe: Dan(ish)
Regrets: Hadley, Lukasz

--

Agenda:

* [transferable streams](https://github.com/w3ctag/design-reviews/issues/332) @torgo
* [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) @slightlyoff @dbaron
* [IndexedDB Transaction Explicit Commit API](https://github.com/w3ctag/design-reviews/issues/316) @cynthia @kenchris
* [Review MathML](https://github.com/w3ctag/design-reviews/issues/313) @cynthia @slightlyoff @dbaron
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) @torgo @hadleybeeman
* [User Activation API](https://github.com/w3ctag/design-reviews/issues/300) @dbaron @hadleybeeman
* [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288)  @dbaron @travisleithead
* [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282) @cynthia @kenchris @travisleithead
* [Background fetch](https://github.com/w3ctag/design-reviews/issues/279) @slightlyoff @ @travisleithead
* [HTML General Review: Web Sockets HTML](https://github.com/w3ctag/design-reviews/issues/268) @slightlyoff @ylafon
* [Vehicle Information Service Specification (VISS) CR pending external feedback](https://github.com/w3ctag/design-reviews/issues/234) @cynthia @torgo @hadleybeeman
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) @cynthia @travisleithead @plinss
* [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) @slightlyoff14
* [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) @dbaron
* [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101) @lknik
* [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) @travisleithead

---

### [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288)  @dbaron @travisleithead

Travis: porting games over to web workers - e.g. through web assembly.

David: worklets are designed for code that's happening on the UI thread or some other existing thread - isolation but not threading...

Travis: holding pattern - 

### [transferable streams](https://github.com/w3ctag/design-reviews/issues/332) @torgo

Dan: work going on in whatwg and they asked for feedback on twitter

David: some of it is developer ergonomics

### [User Activation API](https://github.com/w3ctag/design-reviews/issues/300) @dbaron @hadleybeeman

David: [left recent comment] we can see how they respond to that. one worry is just that - if uses for this are people writing chrome specific stuff about permissions model, not so great. People shouldn't hard code how chrome's permission model into their web site. There is a way to get the permission with one click in chrome and one click in firefox but the reaity is it takes 2 clicks in firefox because of how the site asks for permission. So there will be a browser prompt each time. Chrome has user interaction - so sites have forced interaction even when they don't need it.  Real solution should be to have the permission API answer questions about - whether a permission request will be denied.

Travis: right now it's just 3 values, denied,allowed,prompt

David: there's the permissions API spec - a piece that people have agreed on - and work will happen in the new year

Travis: the proof point is - developers working around that lack of state - and providing the state should be something we [web platorm] do.

Dan: Jo from Samsung did a blog post: https://medium.com/samsung-internet-dev/a-crisis-of-permissions-80cf3b2c802e

Dan: still waiting for a workshop report- I will bug Sam from W3C about this.

Dan: David I think the issue you bring up here is important especially considering current events regarding browser engines.

Travis: maybe start a new issue?

[decided just to keep tracking it on issue 300]

### [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) @travisleithead

Travis: timing ... intersection observer ... 

[david recently suggested writing tests]

David: Intersection observer issue led me to that one.

Travis: happy to participate in some time to collaborate on writing tests... Will reach out on the 14th.

### [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) @dbaron

David: Two remaining issues - one falls back to the task scheduling issue (72). The other one was Peter's concern about string based APIs.

Peter: i think they fixed the string based APIs issue...

### call time discussion

[agreed to change call time for the 8th to 21:00 GMT on Tuesday the 8th]