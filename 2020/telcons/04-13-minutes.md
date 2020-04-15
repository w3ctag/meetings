## W3C TAG Minutes for Week-of-April-13, 2020

### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/04-13-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2020-04-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200413T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Peter, David, Tess, Dan, Rossen

#### [Imperative Shadow DOM Distribution API.](https://github.com/w3ctag/design-reviews/issues/486) - @hober, @kenchris

Tess: Part of the goal is that  .. no slot ... imperative API lets you manually slot everything... Doesn't solve the usability issue - if you want to implement something like details .. one or two that have special slotting behaviour and rest auto - this not solved. They replied to this issue. I need to digest the response. 

Dan: they said already looked at?

Tess: yes - my cocnern was raised years ago... can polyfill.. need to look into it more.  Was nice to get a response promptly.  Work in progress... 

Peter: might be interesting to have a declarative way of doing this - could be as a polyfill on top of this API. A map of selectors... 

Tess: that's what Shadow DOM v0 did. There were some complicated rules ... shadow dom v1 dropped that and has a model of explicit name slotting.   Could be worth exploring again.

Peter: might be worth at some point revisiting the declarative...  so you can build custom elements without having to write any [javascript].

bumped

#### [Delegated Ink Trail](https://github.com/w3ctag/design-reviews/issues/473) - @dbaron, @atanassov

David: comment from dlibby - said will work on addressing points.

Rossen: all of the edits are in - all adressed in WICG in terms of PRs.  As far as the authors understand it, the ball is in our court.

David: Ok - i will do this and let's bump till next week.

bumped

#### [Layout Instability Shifted Element Surfacing](https://github.com/w3ctag/design-reviews/issues/485) - @dbaron, @atanassov

Rossen: need to spend some additional time on this one.  The overall feedbeack was "sounds like a useful thing"... "why didn't the previous approaches work?"

...addresses layout jank across 

[bump 2 weeks]

#### Design Principles PRs

Tess & Alice will have a breakout to look through their PRs

#### When should the plenary call be this week?

We're going to stick to what's in the agenda for this week, and then likely alternate.

### Breakout B (US / APAC) - [2020-04-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200413T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: David, Peter, Rossen, Sangwhan, Tess

Regrets: Alice

Scribe: Sangwhan

#### [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon

Tess: We raised a couple issues and set it as PEF, few weeks ago we checked, and a couple hours ago they are still open. What should we do? Leave open or something else?

Tess: The issues are around the monkeypatching design. 

Tess: Yves and Dan are both on Breakout C; I'd like each of them to take a look to see if they have ideas for what to do next here.

#### [isInputPending](https://github.com/w3ctag/design-reviews/issues/475) - @cynthia, @dbaron

David: This is marked as untriaged, which seems like an error on our end. There is a run-to-completion violation, which may or may not be a significant issue.

Peter: There can be cases where it makes sense to violate. Is there already a navigator.scheduling interface or does that need to be created?

David: Doesn't exist in Gecko as of now

Sangwhan: Have minor comments, but not significant enough for minutes, will comment later

Peter: Any other feedback? One thing that is weird is that requires instantiation? The notion of "continuous events" sounds foreign, is this specific to this spec? Otherwise seems okay with me.

There is also a mention of isFramePending..

David: Did you have any comments on continuous events?

Peter: I was concerned that it was a spec-specific nomenclature, should probably be defined elsewhere

#### [Image Resource](https://github.com/w3ctag/design-reviews/issues/490) - @dbaron, @atanassov

Rossen: This seems quite straightforward. David had some questions unadressed.

David: Not sure if it makes sense to go in to the techicalities, this is effectively a struct

Rossen: The sizes part of this spec is a bit strange, do we have other cases that provide an interface that should be matched for consistency?

My question is - if a specific size fails, should it throw or try to fall back to a default size?

David: There is a section in the HTML spec about parsing (shares link)

Rossen: But this doesn't match up with what the spec says. The spec has a hard throw if it fails, which doesn't look possible in the HTML spec parsing.

Peter: Explainer?

Sangwhan: Doesn't exist but not sure if it's worth picking the fight

#### [Data for measuring audio-video synchronization and end-to-end delay in realtime communications](https://github.com/w3ctag/design-reviews/issues/493) - @cynthia, @dbaron

David: Was hoping Sangwhan had some comments.

Peter: I'm a little bit concerned that we'll miss important comments because this is outside of our field of expertise.

Sangwhan: So the original question I had was are there any security implications of having a somewhat disentaglable sum of delays which map to your hop route - and I don't know. I'm sure someone with the right security experience can find a way to abuse this but all I know is that given small enough hops and the sums of maybe 2-3 users it seems numerically possible to unmask, whether or not hat that is useful.. no idea.

Re-inforce the original "please discuss with IETF" after repeating the original question?

#### Design Principles PRs

### Breakout C (APAC / Europe) - [2020-04-14](https://www.timeanddate.com/worldclock/converter.html?iso=20200414T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Dan, Yves, Ken, Sangwhan

#### [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

Ken: they haven't done the explainer yet. I pinged them again.

Sangwhan: if they don't come back by our next milestone, suggest we close.

#### [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon

(see minutes above)

Yves: I don't think it's a huge issue... The other issues about negative/positive seemed a bit more concerning.  Issue #27 on their repo. They have to coordinate with the gamepad people.   They marked this as pre CR so they must fix it before it before it goes to CR.  Looks like they have agreed.

Sangwhan: some mixed opinions about the monkey patching. 

Yves: I can live with it. We raised it. They've made an informed decision.

Sangwhan: they wanted to do it this way because it's unclear when the gamepad spec will go to CR. Technically, i think monkey patching is not great ergonimically. 

Ken: things get out of sync.

Dan: but we are OK with it - I agree with Yves's comment that we have raised the issue. I think we should close, considering they are addressing both the issues that we've raised.

#### We triaged some new issues

#### [issue 495 - AVIF Decoder](https://github.com/w3ctag/design-reviews/issues/495)

Sangwhan: what do they want?  I'm looking at the chrome issue tracker - this is transparent decoding.  

Yves: this is in line with the crypto one - depends on the buy-in and patent related issue... not really technical.

Sangwhan: they are adding a new image format ... it's a browser feature.  From a greater perspective, it should be "is the web going to add a new image format"?

Ken: too early to do a recommendation for that.

Sangwhan: this doesn't ask for any of that. 

Dan: shall we propose close, sumarilly, and just say "it's not in TAG's wheelhouse"?

Ken: better format than web-p... 

Dan: is this related to HEIC?

Sangwhan: No. Related to AV1. Key frame format for AV1. 

Ken: supported by Netflix - much better quality than JPEG

Sangwhan: no hardware support.  WebP has some level of hardware decoding.

Sangwhan: as a recommended format, I think we need to consider it, but as a pure technical perspective, let's not consider.

Ken: this is really good for the web because it's much mroe open....

Sangwhan: we should look at this in the sense of : is this an official format for the web?  The web platform does definitely need a better image format.

Dan: other dependencies?

Sangwhan: clipboard

Ken: canvas API

Sangwhan: another API:  [Web codecs](https://github.com/w3ctag/design-reviews/issues/433)

Ken: also multiple file extensions... why?  That's gonna be a pain. 

#### Design Principles PRs

### Plenary Session - [2020-04-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200415T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Tess, Kenneth, Dan, David, Peter, Rossen, Yves

Regrets: Alice

#### Merging [Design Principles PRs](https://github.com/w3ctag/design-principles/pulls)

https://github.com/w3ctag/design-principles/pull/167

https://github.com/w3ctag/design-principles/pull/163

[Unable to merge this week - pushed to plenary next week.]

#### Breakout Rollup

[summary discussion on breakouts]

Rossen: re: [**Layout instability**](https://github.com/w3ctag/design-reviews/issues/485) - there have been some answers.

david: on [**isinputpending**](https://github.com/w3ctag/design-reviews/issues/475): ... 

Peter: do we think we can close it?

David: I'd like to hear back about the continuous event thing.

Peter: we left a bunch of comments - let's mark as pending feedback.

Peter: [**Image Resource**](https://github.com/w3ctag/design-reviews/issues/490)

Rossen: question about the parse logic...  Sizes attribute - why is it throwing?  verified that none of the sizes attributes currently throw. This one was kind of odd. Will leave comment.

David: some of issue is which piece of the HTML spec it should be citing.  

Peter: [**audio-video synchronization**](https://github.com/w3ctag/design-reviews/issues/493)

Tess: it seems like it would be courteous of us to go to the IAB to raise it...

David: but it might not be the IAB - but dispatch...

Tess: I don't like the implication that we're being used as a review board in lieu of IETF review. If they're not going to take it to IETF then we should raise it to IETF.

Peter: agree.

Yves: we could ask the IETF liaison to work on that. Wendy.

Tess: can you take an action?

Yves: yes.

Peter: we could also arrange a joint meeting if necessary.

Tess: we could transfer the issue.

Dan: suggest we ask w3c ietf liaison to take it up and then close in a week if they are able to take it up.

Dan: [**MediaStream Image Capture**](https://github.com/w3ctag/design-reviews/issues/358)

Ken: they are working on an explainer 

[set for 2 weeks]

Peter: [**WebXR Gamepads Module**](https://github.com/w3ctag/design-reviews/issues/430)

Tess: they need to work with the gamepad people to fix [the monkeypatching issue].  This is an example : XR is its own little world and redefining things - in some cases not working with relevnt people in other areas. Why is it hard to land that upstream?

Yves: there was also the issue of registering a specific value - and having a registry for that. the issue was 2-fold.

Tess: they should ask the gamepad people...

Dan: i marked it as proposed closed as it seems people can live with it...

[consensus to close]

Dan: I will write summary and close.

#### [issue 495 - AVIF Decoder](https://github.com/w3ctag/design-reviews/issues/495)

Dan: AVIF decoder - 

Ken: I looked through this... left some comments.. on what else we need to change 

Peter: seems we're lacking the proper layering...

Tess: that's what the web codecs APi is supposed to do...

David: this is just a new image format...

David: web codecs is more centered around audio & video...

[discussion of how this relates to web codecs]

Peter: I would like to see - before we add new black boxes - let's make these things extensible.  E.g. with webaudio... 

David: other question is - what APIs do you need?

Ken: hardware acceleation - which you don't get with webassembly

#### Issue Triage
  * [Review request: HTML Standard Jan 2020 Review Draft](https://github.com/w3ctag/design-reviews/issues/499) & subtasks

Peter: **All HTML issues**

Tess: this is another batch of HTML issues so that the HTML wg can advance the whatwg spec to Rec.  HTML group provided list - I split into 6 buckets.  We need to assign each bucket.

[imnage element](https://github.com/w3ctag/design-reviews/issues/500) - sangwhan and tess

[User interaction, user activation, focus, tabbing,](https://github.com/w3ctag/design-reviews/issues/501) - Dan, Rossen

[Windows, navigation, agents and agent clusters](https://github.com/w3ctag/design-reviews/issues/502) 

Tess: one is a small changem the other 2 might be more inetresting.

*Assigned David, Tess*

[Documents, DocumentOrShadowRoot, etc.](https://github.com/w3ctag/design-reviews/issues/503) - Alice, Ken

[Event Loop, task queues, etc.](https://github.com/w3ctag/design-reviews/issues/504) - David, Ken

[misc / reorg / cleanup](https://github.com/w3ctag/design-reviews/issues/505) - Dan, Tess

499 to be closed as soon as other subtasks are closed.


#### f2f schededuling

David: all 3 weeks we polled have someone with a conflict

Tess: spread it over 2 weeks?

Peter: w/o 25th of spread it out?

David: spread between 2nd and 3rd weeks?

Peter: first half of w/o 25th but with some joint session with AB week before.