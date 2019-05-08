## TAG Teleconference
##### 08 May 2019

Present: Peter, David, Alice, Tess, Dan, Hadley, Yves

Regrets: Kenneth, Lukasz, Sangwhan

---

Agenda:

* [LazyLoad (loading= attribute)](https://github.com/w3ctag/design-reviews/issues/361) - @hober, @cynthia
* [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris
* [Design questions for Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/354) - @torgo, @hadleybeeman
* [Subresource prefetching+loading via Signed HTTP Exchange](https://github.com/w3ctag/design-reviews/issues/352) - @torgo, @hadleybeeman
* [Async Clipboard - image/delayed content](https://github.com/w3ctag/design-reviews/issues/350) - @cynthia
* [TAG review of whether element.pseudo(":unknown") should return null or throw](https://github.com/w3ctag/design-reviews/issues/348) - @hober, @alice, @dbaron
* [Audiobooks](https://github.com/w3ctag/design-reviews/issues/345) - @hober, @cynthia, @dbaron
* [Web Publications review](https://github.com/w3ctag/design-reviews/issues/344) - @dbaron, @torgo, @hadleybeeman
* [Verifiable Credentials Data Model 1.0](https://github.com/w3ctag/design-reviews/issues/343) - @hadleybeeman
* [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo
* [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @travisleithead, @plinss
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice
* [WebRTC DSCP Control API](https://github.com/w3ctag/design-reviews/issues/325) - @hober, @cynthia, @torgo
* [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @hober, @dbaron
* [EME Extension: HDCP Policy Check](https://github.com/w3ctag/design-reviews/issues/323) - @hober, @cynthia
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman
* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @torgo, @hadleybeeman, @travisleithead
* [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) - @cynthia, @travisleithead, @plinss
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @slightlyoff, @torgo, @ylafon
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @slightlyoff, @hadleybeeman, @travisleithead, @plinss

---


## Issues

### [LazyLoad (loading= attribute)](https://github.com/w3ctag/design-reviews/issues/361) - @hober, @cynthia

Tess: Question on status of the pull request... the under-specifiedness of the `auto` behaviour.  Seems to have petered out.  We could poke and ask if they came to consensus.  I will do that.

[agreed to put it to f2f]

### [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

Peter: Marked pending feedback...  We got a "thanks" - and Ken and Sangwhan aren't here. I'll bump.

### [Design questions for Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/354) - @torgo, @hadleybeeman

Tess: [to update issue with some new material]

Dan: And this has shipped...?

Alice: Signed exchange was enabled on Feb 5.. is shipping [in some Chromeium stable version] 

### [Subresource prefetching+loading via Signed HTTP Exchange](https://github.com/w3ctag/design-reviews/issues/352) - @torgo, @hadleybeeman

[both of above shifted to f2f - we will try to get someone to dial in from this work - alice is working on that]

### [Async Clipboard - image/delayed content](https://github.com/w3ctag/design-reviews/issues/350) - @cynthia

[bumped as Sangwhan is not here]

### [TAG review of whether element.pseudo(":unknown") should return null or throw](https://github.com/w3ctag/design-reviews/issues/348) - @hober, @alice, @dbaron

Tess: last time we talked about this was before a CSS call.

Peter: this wasn't discussed on the [CSS] call.

David: [nobody] really cared about this detail.

Alice: in the linked CSS wd draft issue they said they resolved null and asked us. Null seems fine to me. David saw your proposal about undefined but don't know about that.

Alice: i think our opinion is "not an exception"

Dan: can we close this?

Tess: sounds like we can to me - unless anyone has strong feelings.

Peter: i'm ok with it returning Null. Meta question: do we have advice in our API design guidelines for this sort of thing. 

Tess: can we close this issue and open up a design guidelines issue?

Alice: already have an issue - that david referenced in that review.

Tess: I'll comment on it and close it. 

[woot!]

### [Audiobooks](https://github.com/w3ctag/design-reviews/issues/345) - @hober, @cynthia, @dbaron

Tess: last i remember we were pending external feedback from tsvia

Dan: i am due to talk to her tomorrow about web publications review

Tess: in addition to punting this until we hear back from T, there was conversaiton on audiobooks.


### [Web Publications review](https://github.com/w3ctag/design-reviews/issues/344) - @dbaron, @torgo, @hadleybeeman

[i'm due to talk to Tzviya tomorrow about both of the above]

### [Verifiable Credentials Data Model 1.0](https://github.com/w3ctag/design-reviews/issues/343) - @hadleybeeman

Hadley: ...not helping with things like specific use cases... can we bump...

Dan: I've also been concerned that anything involving blockchain isn't necessarily sustainable. And I've fed back on the user stories...

Hadley: It's also not necessarily great for users in developing countries

[bumped to f2f]

### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron

David: i think we need to bump this to f2f [and 349]

Tess: do we know if Andrew will call in for it?

Dan: I will reach out to Andrew.

### [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris

[bump]

### [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo

[bump]

### [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @travisleithead, @plinss

Alice: there was a talk about it at I/O

Tess: how should we handle cases where we generated questions during our review and they go awol? Seems like we shouldn't leave the issue open indefinitely.

Dan: I think we at least need some additional labels to show when TAG feedback isn't acted on...

Alice: we need a time-out state

Tess: follow-up question which is a blink question...  is the expectation that raising the question to the tag satisfies the blink process requirement or are they expected to take the feedback into account. 

Alice: that's an active question. It suffices to file a review - the gate is a "lgtm" - link to the review - at the intent-to-ship stage you should already have a review. if in between those things the TAG review hasn't happened, it is up to the API owners to make a judgement call.  If they look at the TAG review thread and see that the requester hasn't taken the feedback onboard then they might not progress it.

Alice: what is the user-facing [end user facing] problem that this solves, what is the proposed solution, worked excamples showing how the solution solves the problem... 

Hadley: this solves a frustration I have where we are getting specs that are for developer needs as opposed to user needs.

Alice: yeah, though there are many dev-focused specs that have an end user benefit e.g. Intersection Observer.

Dan: I'd like to cover a lot of this in the f2f - including how we can be more effective / responsive to review requesters....

Alice: the last 2 comments are from us - we haven't heard from blink since feb 14.

[...discussion on closing it...]

David: there's a bunch of stuff we don't udnerstand about the design.. feels like this feature has moved forward [in blink]

Alice: we could say "we have had this feedback - no responses..."

Dan: is this overtaken by events?

Tess: I have concern - minting a new element that is a way of embedding other content.  Is adding new things like this something we should be doing instead of adding these features to iFrame. I feel like adding a feature like this has to pass a pretty high bar. Yes it's been overtaken by events in the sense that [blink] has proceeded full teams. I'm concerned about closing it "overtaken by events" and they look at this as tacit approval. 

Alice: seems like there are valid concerns - listing them out succintly...

Tess: [takes an action to summarize state on the issue]  Peter and Dan can you try to figure out set of new labels to use for this.

Dan: I'll do some research and propose something on slack.

Hadley: we could use something like "unresolved"

Tess: where we close issues and are not satisfied - in TC39 and WHATWG they have "needs x" labels. We could have "needs explainer" 

Dan: I'll add it.

### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice

Alice: one of those ones with no explainer... 

Tess: this is a candidate for a fast fail state.  They need to send an explainer.

Alice: comment on feb 6 - suggested that it remains a work in progress.

David: sort of a Houdini thing.

Dan: can i suggest we close it and ask them to come back to us when they have an explainer?

Alice: I can do that - will send a draft to the chat.

### [WebRTC DSCP Control API](https://github.com/w3ctag/design-reviews/issues/325) - @hober, @cynthia, @torgo
### [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @hober, @dbaron
### [EME Extension: HDCP Policy Check](https://github.com/w3ctag/design-reviews/issues/323) - @hober, @cynthia
### [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman
### [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @torgo, @hadleybeeman, @travisleithead
### [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo
### [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) - @cynthia, @travisleithead, @plinss
### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @slightlyoff, @torgo, @ylafon
### [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @slightlyoff, @hadleybeeman, @travisleithead, @plinss
