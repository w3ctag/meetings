## TAG Teleconference
##### 18 September 2018

Present: Kenneth, Dan, Peter, Lukasz, Travis, David, Yves

Regrets: Alex

Chair: Peter

Scribe: Dan

---

## Agenda:

* [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @travisleithead

Travis: I've been trying to review this - following up on Alice's comments - so far looks good she addressed some issues in her comments. Also crosschecking with html issues - 100s of comments - reflecting ARIA properties with ID refs. ARIA folks want to make sure those refs can be assigned acassigned across shadow dom bounderies. Push back from moz and apple. So changing direction. Not ready to close the issue. Take-away so far : all the right conversations seems to be happening. Will contnue dialog.  Let's bump a couple of weeks out.  We can close this issue out waiting for another review.

Dan: do we know when this will be discussed at TPAC?

Kenneth: maybe should be discussed in Web platform wg?

Travis: I'll check in with alice.

*bumped 2 weeks*

* [User Activation v2](https://github.com/w3ctag/design-reviews/issues/295) - @dbaron @hadleybeeman

* [User Activation API ](https://github.com/w3ctag/design-reviews/issues/300) - @dbaron @hadleybeeman

David: for this one and 300, the questions have been answered and there have been some updates to the explainers. We should review them now (on that basis).  We should push out a week or 2 and look at them in more detail.

* [RTCIceTransport & RTCQuicTransport ](https://github.com/w3ctag/design-reviews/issues/296) - @cynthia

Sangwhan: jist is that M. Thompson from IAB is concerned about using QUIC at this stage because it's not finished. I agree. We should say it's too early in development. ITCice transport - not to review the icetransport but to review extensions. That seems to be K but concerns about using that as a generic mechanism for socket communication. Other ideas?  Otherwise I think the icetransport concerns raised by martin are valid. This could enable a lot of stuff...  APIs not very [webby].  A lot of QUIC transport APIs seem to enable this characteristic.  Do we want to cotninue that?

Dan: isn't it time to (fix issues with WebRTC)

Sangwhan: someone else who has more knowledge on WebRTC could spend some time on this...

Travis: I could get bernard.

David: Martin could be someone to add to that.

David: some of martin's cocnerns are that - when you expose ice as a general API you're making something that requires some CORS like permission model in order not to open up arbitraty content.

Sangwhan: intersting and very dangerous. Useful addition but could open up a huge can of worms. 

David: some procedural issues here as well.

Sangwhan: why is this being pushed out so early?

Peter: looks like we should close 296.  Closing.  [adds travis, david and sangwhan to new issues]

Sangwhan: will comment that it's too early ... we would like to have more time, but depending on QUIC this early is probably a bad idea.  

Peter: they are asking feedback because of intent to implement behind a flag.

*sangwhan to file comments*

* [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288) - @slightlyoff @dbaron @travisleithead

[general shaking of heads]

Travis: angst regarding porting code that runs synchronously onto the web ... commit w would be synchronous - they don't want to adadpt that code base to async techniques. We need more time - let's come back to this. 

*bumped 3 weeks*

* [DOM](https://github.com/w3ctag/design-reviews/issues/229) - @cynthia @dbaron @travisleithead

Sangwhan: Travis & I went through - we've done some work, but not done - one thing that sticks out is "abortcontroller"  - a mechanism for a cancelable promise. Why is this in DOM was our main question. [possibly not the best place for it] 

Travis: I'm looking at another issue on DOM on observables. Talk about integrating that with abortcontroller - this could have been done in TC39 but was moved into WhatWG.  

Sangwhan: there could be another place where this could go. But my main question was - this and observables - do they belong in DOM? Neither relate to the document object model.

Travis: these are language features. There's not a lot of homes though.  Their own spec... DOM, HTML, webIDL. Not sure if we need to get worked up over it.

Sangwhan: I'd like to spend some more time on this - in a month or so. 

Travis: call next week?

Travis: most of this stuff has shipped for many years - but if we can get it done this week then I'd like to try to close the issue.

*agreed - bumped 1 week*

* [Web Components Guidelines Doc](https://github.com/w3ctag/design-reviews/issues/227) - @kenchris @travisleithead @plinss

Dan: we need to fix up the status of this document because it's still draft

 ## Triage
* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297)

*2 weeks*

* [Support codec and container switching with MSE using SourceBuffer.changeType() ](https://github.com/w3ctag/design-reviews/issues/298)

Travis: we're pumped about it.

Sangwhan: i'd want to look at this.

*bumped 3 weeks*

* [WebAssembly Threads ](https://github.com/w3ctag/design-reviews/issues/299)

Travis self-assigned

Travis: I'm curious on how this goes.  Any other threading experts?

Sangwhan: I'm not sure what they want us to review.

David: yeah OK

Sangwhan: wow... just wow. looks ninteresting.  Hardware that doesn't support this .. ugly.

*milestone - 2 weeks*

* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301)

Dan: assigned and preemptively assigned Hadley 

*bumped 3 weeks*

* [Canvas TextMetrics](https://github.com/w3ctag/design-reviews/issues/302)

Peter: aligning this with the houdini spec - which is stalled... 

*David assigned*

*bumped 1 week*

* [TAG Review Request: Form Participation API](https://github.com/w3ctag/design-reviews/issues/305)

Travis: yes please!

Travis: enabling a custom element to participate in a form submission process.

David: enables elements other than the submit button...

Dan: isn't that a big wooly security hole for bad stuff?

David: doesn't feel like it?

Travis: @lukasz would you like to also review #305? (from a privacy perspective)

*bumped 3 weeks*

* [TAG Review Request: Display Locking](https://github.com/w3ctag/design-reviews/issues/306)

David: i talked to [someone] I can be on it. I'm not crazy about the proposal. 

Sangwhan: this freezes an element so it doesn't render.  

David: let's add an ability to freeze something.  There are a pile of interesting implications.  [bunch of stuff]  

Sangwhan: seems like a feature useful for certain cases but a blunt tool.

*preemptively assigned alex*

*bumped 3 weeks*

---



