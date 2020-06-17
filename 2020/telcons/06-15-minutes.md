### TAG minutes - week of 15 June 2020

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/06-15-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2020-06-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200615T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Same-Origin iframe document-access limiting attribute](https://github.com/w3ctag/design-reviews/issues/397) - @hober, @kenchris
* [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov
* [Record and Tuple ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/518) - @hober, @kenchris
* [design principles pulls?](https://github.com/w3ctag/design-principles/pulls)

### Breakout B (US / APAC) - [2020-06-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200615T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477) - @hober, @cynthia, @dbaron, @hadleybeeman
* [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris
* [Behavior of the "disabled" attribute for HTMLLinkElement](https://github.com/w3ctag/design-reviews/issues/519) - @hober, @alice, @dbaron
* [CSS Overflow: scrollbar-gutter](https://github.com/w3ctag/design-reviews/issues/520) - @alice, @dbaron, @atanassov
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov

### Breakout C (APAC / Europe) - [2020-06-16](https://www.timeanddate.com/worldclock/converter.html?iso=20200616T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Allow audio packet rate to adapt in realtime communication.](https://github.com/w3ctag/design-reviews/issues/517) - @cynthia, @ylafon
* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo

### Plenary Session - [2020-06-17](https://www.timeanddate.com/worldclock/converter.html?iso=20200617T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### Design Principles Edit from Alice

* Breakout Rollup
* Issue Triage

### Logistics

Chair: Dan

Scribe:

Bridge: https://meet.jit.si/w3ctag first then going to https://whereby.com/w3ctag as a back-up

* Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/06-15-minutes.md

### Breakout A (Europe / US)

Present: Peter, Kenneth, Dan, Rossen, Tess, Yves, David (regrets for first ~half)
Scribe: Tess, Dan, Rossen

#### [Bias – needs to encompass a fuller set of considerations](https://github.com/w3ctag/security-questionnaire/issues/85)

Tess: I think there's a point buried in here that we should highlight when closing. Namely, the security & privacy questionnaire narrowly focuses itself on two of the W3C areas of horizontal review, and that we should consider writing or collaborating on self-checks for the other areas. That said, the S&P questionnaire rightly focuses itself on its two areas.

Dan: I'll close with a comment along those lines.

#### [Same-Origin iframe document-access limiting attribute](https://github.com/w3ctag/design-reviews/issues/397) - @hober, @kenchris

Kenneth: this prevents iframes from getting script access

Kenneth: the naming is weird and there's a separate set of considerations

...: they suggested a number of other names, and i don't like the alternatives

...: though i don't have any suggestions

Dan: definitely don't like DOM Worker

Kenneth: this is only script isolation

Dan: have they been receptive to the comments?

Kenneth: yes, we even got a comment from Domenic explaining how this differs from the other knobs

...: filing iframes so they don't have direct document access

Ken: Dominic suggested disallowdocumentaccess... 

Tess: don't dislike "disallowdocumentaccess" name - i have a concern "too many knobs" that tweak too many distinct but related things when it comes to iframes. I worry about the overall cognitive burden on developers. It's not an issue with this proposal - it's a big picture issue. On this specific issue I think they've ended up in a good place, but as the TAG we should step back and do a holistic review of all the ways authors have to tweak iframe capabilities and restrictions - and suggest a way to simplify or consolidate.  It could be that there are 2 knobs that are distinct but the use cases could be satisfied by one.

Dan : this is exactly what we should be doing as the TAG. how do we capture this in an issue? Is there anything we could take out of that that could help these people in this case? If not, maybe we should close this off.

Tess: I'll file a design review issue.

Dan : let's propose close and discuss in the plenary

Tess, Kenneth: okay

#### [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov

Ken: there is overlap between this and web codecs.  I have been following discussions on blink-dev - looking at this API, for me it seems nice. This seems like a good API. but it was pointed out on blink-dev that these are not the most common use cases. But a comment people have given is that it doesn't scale.

Tess: the lesson from that is layering. This captures common use cases and those should be easy. If it can be defined in terms of the lower level stuff then that's good.  If the convenient stuff works for you then great.

Rossen: it does hit and address the most common cases which are ~80% of what people need. Where the strggle that comes out - it was one of the issues that was raised - one of the main weaknesses of the API is splicing differently encoded and different types of media... This API becomes lossy for that.  It will have to renormalize to something that loses the original quality. On the flip side, from experiments that [MS] team has run with real media, they have run a number of partner use case verifications and the results were overwhelmingly positive. Today this is very painful. In the most common use cases - e.g. trimming a video, it helps.

Ken: would it be possible to show a slider with frames?

Rossen: scribing?  I think this is capable through video element and API. the point is what happens next. Today you send it back to the server. There are some JS libraries that have performance cliffs.  As a general principle, I'm aligned to what Tess said about reducing developer pain.

Ken: some examples missing for how to tie this together with playback.  Seems like something very separate from playback.  As it's supposed to be simple, some examples of how to tie it together with playback would be useful.

Rossen: yes, the main selling point is ergonomics. Showcasing an end-to-end authoring case would be good. I will add the comment.  Push a couple weeks?

Ken: OK

#### [Record and Tuple ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/518) - @hober, @kenchris

Tess: before this was raised as a design review with us, I raised this with idl and webidl... Both of those are being looked at.  I think that's going fine.  It will may result in one of them being renamed. If you have a webidl interface that accepts a webidl record, one of these ECMAScript records would work - so that might be fine.  Overall I think it's great.

Ken: Yeah. I agree, looks great. At some point, spec authors would want to know what to use in their specs.

Tess: I think the open issues on webidl will cover that.

Ken: maybe we should update the design principle.

Tess: a lot of good browser vendor representation in TC39 but it's often people not as familiar with webidl.

Dan: can we close this?  

Ken: I think we need to right a good answer to them. 

[Tess to write a closing comment]

#### [design principles pulls?](https://github.com/w3ctag/design-principles/pulls)

Dan: hopefully we can land at the plenary call.

### Breakout B (US / APAC) - [2020-06-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200615T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Tess, Alice, Sangwhan, David, Rossen, Peter

Scribe: David, with some help from Alice

#### [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477) - @hober, @cynthia, @dbaron, @hadleybeeman


Tess: I raised two issues on their repo - one in March, one three weeks ago, and David also raised one three weeks ago. Looks like the spec was using rel=feed... 

Tess: David raised issue about rel=feel, seems like weird anachronism; used to be a feed relation type, no longer implemented.  Started discussion between Becca and Kevin Marks about figuring out what `rel` value to use and where to register it.  Becca changed spec 6 days ago to change `rel` type to `media-feed`.  What did you think of that?

David: Given that it's a weird thing, probably better?

Tess: Should we keep this issue open or close it?

Tess: Issue I filed 3 weeks ago:  she replied, I need to read/process reply.  Seemed odd that this was creating a new JSON feed format when there is one already.  Some of the arbitrary design decisions differ between the 2.  Why gratuitously be incompatible?  I need to read/understand her reply.

Tess: So we should each look at responses to those issues and figure out next steps.

Tess: Should we close after that?  Or generate more feedback?  Propose to close at plenary.

#### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris

Tess: Suggestion that this should be merged into Digital Goods API design review.  Not sure what I think about that.

Tess: The change to this spec can be motivated by some other spec.  Feel like it needs to stand on its own merits.

Tess: Figure out course of conversation prior to that -- confusion about pending totals versus optional totals.  Different use cases.

David: Is part of our design review process judging whether things are useful?  Other than that, it's pretty independent, but that could be big...

Tess: I like the idea of closing one rather than keeping 2 reviews open indefinitely.  But still an open discussion I want to drive to some sort of conclusion.  I think that's on me; need to go through comments after my last comment.

(does Digital Goods API review even exist?)

Tess: Push a week or two, give time to both follow up on above and time for them to file Digital Goods API.

#### [Behavior of the "disabled" attribute for HTMLLinkElement](https://github.com/w3ctag/design-reviews/issues/519) - @hober, @alice, @dbaron

Tess: I haven't looked at this.

David: I haven't looked either; I should do so!

Rossen / Tess: A few comments so far that haven't been answered.

David: Emilio is an author.

Sangwhan: Looks like this is all landed at WHATWG HTML already.

David: I suspect this is general interop improvement, but we should take a look given that we were asked.

Alice: Should the 3 of us schedule 15-20 minutes to look closer?

(will do)

#### [CSS Overflow: scrollbar-gutter](https://github.com/w3ctag/design-reviews/issues/520) - @alice, @dbaron, @atanassov

Rossen: A rehash of topic discussed in CSSWG for quite some time.  Issue linked (4674) discussed at length, agreed on general shape of the API, and agreed to move on and start specifying it in css-overflow spec.  So in terms of venue and having folks engaged I think we're there.  Question is does this property and behavior overall make sense from the TAG's PoV.

Discussion of `&&` in CSS syntax.

Rossen: General idea is to make layouts more stable for scrollbars or other UI types for scrolling, custom scrollbars, etc.

Peter: Always weird that change to layout in one dimension can cause scrollbar in the other dimension

Rossen: It's become sort of natural to me :-)

Alice: Looks pretty good, the illustrations help.  Would be nice to see each value compared between classic and overlay instead of this big thing.  Only question would be why is the current bad behavior the default?

Rossen/Peter: history.

Alice: Looks good to me, but makes me sad we can't fix the default.  Maybe explainer should say?  Maybe I'll ask in the issue even though I have know the answer.  Would be nice to know what would break?

Peter: Some OSes almost always do overlay scrollbars and sidestep the issue.

Rossen: I'm adding comment now to encourage authors to transfer the examples over to the spec since the spec doesn't have any.  Would be great to have them in the spec.

Alice: In the context of the spec they'd have no choice to show the classic and overlay examples per-value.  It's really only stable that behaves differently between classic and overlay scrollbars.  Seems like stable would be a good default, but it's not.

David: probably pages that know there are never scrollbars, would break.

Rossen: Aside, why not an event to say whether there's a scrollbar?

David: Though there was an `overflow` event... oh, it's Gecko-specific.

Rossen: Back to `scrollbar-gutter`, seems overall ok... does the TAG need to do more?

Peter: Don't see anything architectural.  Though question of where this fits into things like APIs and events that we're missing, I think that's valid feedback.

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov

Rossen: a complicated one.  I've been wondering how unstable... There's only one new step added in the pipeline, between dispatching rAF and updating web animations.  And that one...  When I looked at this, I thought this specific updated could be unstable based on some of the layout or paint results.  And I was trying to find a way to find a way in this explainer that this is addressed.  They do talk about it a little bit.  But I'm curious if any other TAG reviewers have answers to that.

David: something I knew something about 2 years ago and haven't looked at since.

Alice: Found the explainer hard to read because of all the animations; would like markdown to not animate GIFs by default.

Sangwhan: WebP!  (So they don't show up in Safari!)

Alice: That aside, I need to have a closer read.  I asked a similar question on something else to do with animations on how we might deeply integrate this with prefers-reduced-motion.  I feel like that was blown off a little bit last time.  Authors can use `prefers-reduced-motion`... but I think there should be a sensible default so that things `prefers-reduced-motion` disables animation effects by default unless authors specifically opt in to it.  So the default shouldn't be for the prefers-reduced-motion setting to do something -- authors should have to opt in for it to do nothing.

Rossen: So today it's on to authors to stop/throttle animations based on `(prefers-reduced-motion)`.  So authors who don't care

Alice: ... or on deadline...

Rossen: ... anything engines do by default today?

Alice: I think we stop animated GIFs.

Alice: That's a good question.  Chromium has code that looks at that setting other than the code that exposes it to `(prefers-reduced-motion)` media query, but I don't remember what that code does.

Rossen: If you don't do anything as the author, besides GIFs, sounds like nothing else stops animating.

Alice: I'd have to check -- don't remember.

Rossen: Does WebKit or Safari do more?

Tess: I'd have to ask James.

Peter: Would be interesting to have users have to opt in to animations, rather than opt out and hoping the authors respect their choice.  Is there a middle ground, not switching off all forms of animation by default?  Or are there subtle ones that are more ok?

Rossen: I wanted to see how much of the behavior can/should be forced onto the content.  I can see a path forward where something like prefers-reduced-motion can throttle everything down by 50%, slow down timers, etc.  Make it to the point where authors will have incentive to pay attention to it.

Rossen: Or you can go further -- I can see UAs going and being more forceful and stopping more than animated GIFs.

Peter: There's a lot of code that stops things like autoplaying videos.  People consider a lot of these animations to be obnoxious.  Can we determine obnoxiousness?  How far/fast pixels are moving?

David: Maybe also users for whom slowing things down makes things worse?

Peter: Could slow things down into ranges that trigger epilepsy, could be dangerous.

Alice: Questions:
1. What should the default behavior be given that the default should respect the setting and not require authors to opt in?
2. Whose responsibility is it to figure out what the default should be and how do they do that?

Alice: Do you shut off animation by default?  That could cause problems as well?

Peter: There are subtle animations that are often good for accessibility?

Rossen: Same thing for anything based on timers?  Same for transitions?

Sangwhan: Feels like this could be a smaller breakout at some point.

Sangwhan: How many problems require this treatment?  Does anybody really know?

Alice: Maybe the AOM meeting a good place to discuss this?  (Yes.)  I'll put it on the agenda.

Alice: Not sure if I should comment until we've had that discussion.

Rossen: Reasonable to ask... ?

Alice: I'll hold off for now.

Rossen: Yeah, not sure what's actionable.  Today Web Animations doesn't do anything; this builds on top of Web Animations.

Rossen: Issue is pretty new.

Sangwhan: Was a previous review in [#330](https://github.com/w3ctag/design-reviews/issues/330).

(discussion about adding comments)

Peter: I'm looking at the IDL in this spec -- why object or domstring if the only valid string is an enum, why not the enum?  Are there other string values?

Rossen: Looked at this in Kyoto during Houdini meeting, feedback was this  (missed) -- let's see how this can work with Web Animations?  Renewed proposal a year later, had timeline.  Scroll timeline was introduced, started to be merged with web animations.  In general, overall feature and its place in the platform is sort of the right spot.  I think we're getting lost in details (plenty of them, a big feature).  Does anyone think overall feature is in a bad spot in terms of where it falls in the platform?

David: I really don't remember it...

Rossen: push out by 2 weeks and hope we get to it?

Tess: Sounds good to me.

Peter: I think I answered by question about the IDL -- seems like they also take length and percentage.  I'd like them to use Typed OM rather than string.  Would like to start pushing people to use that instead.

Rossen: +1.

### Breakout C (APAC / Europe) - [2020-06-16](https://www.timeanddate.com/worldclock/converter.html?iso=20200616T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### [Allow audio packet rate to adapt in realtime communication.](https://github.com/w3ctag/design-reviews/issues/517) - @cynthia, @ylafon

Sangwhan: I'm totally OK with this. it's very webrtc specific - it's a minor change. i don't see why we should say no to this.  The best explanation is it's mpeg-dash for webrtc audio streams...

Yves: one of the main issues - they're defining something network related in the encoding... but they provided explanation of why they needed to do it there - can't change the settings on the connection metadata. So for them this is the easiest way and it actually makes sense. No security & privacy things added. Minor change that makes sense. Not at the ideal place but most convenient place.  We should say "go ahead" and close it.

Alice: i care about audio quality of video calls - how will this effect user experience?

Sangwhan: it will make it lower quality in exchange for less choppy.

Yves: it will modulate the bandwidth used for bandwidth - meaning it can decided to send less packets.  Will allow the session to change to a lower quality encoding and also send less packets so use less bandwidth.

Alice: would that be responsive to for example turning off video feed?

Yves: depends on implementation.  Goal is to reduce the bandwidth so people don't hear robots.

[closed by consensus]

#### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo

Sangwhan: I looked at this - their lifecycle is effectively defining a PWA. It's petty much the same as the PWA lifecycle. [goes over how many things in the explainer can be mapped to PWA life-cycle].  Foreground and background mode... background not well defined.  Some API differences.  

Yves: media types, parameters - they want to be able to figure out its a mini app before they open the URL. 

Sangwhan: a miniapp URL is a miniapp:// a miniapp url has a dereferencing process... can be re-written into a HTTPS url so becomes a web URL.  Effectively a https url in a different format.

Dan: could we encourage them to merge this with a general web app lifecycle document (so encompassing both PWAs and miniapps).

Sangwhan: [web app lifecycle doc](https://wicg.github.io/page-lifecycle/) exists...

Dan: looks like it hasn't been touched since Sept 2019.

Dan: we need to ensure the coherence of the web platform.

Dan: [we decided to author a miniapps feedback document to encompass feedback on miniapps URL, miniapps lifecycle and miniapps manifest]

Dan: we could try to ship them some feedback next week.



### Plenary Session - [2020-06-17](https://www.timeanddate.com/worldclock/converter.html?iso=20200617T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Peter, David, Sangwhan

Lack of quorum.

#### Design Principles Edit from Alice

#### Breakout Rollup
##### Breakout A
##### Breakout B
##### Breakout C
#### Issue Triage

