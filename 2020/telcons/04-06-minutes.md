## TAG Teleconference
##### 06-08 April 2020

---

### Breakout A (Europe / US) - [2020-04-06](https://www.timeanddate.com/worldclock/converter.html?iso=20200406T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris, @atanassov
* [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov
* [Scheme-bound Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon
* [Imperative Shadow DOM Distribution API.](https://github.com/w3ctag/design-reviews/issues/486) - @hober, @kenchris
* [WebAssembly SIMD review](https://github.com/w3ctag/design-reviews/issues/487) - @hober, @kenchris
* Review Design Principles PRs

### Breakout B (US / APAC) - [2020-04-06](https://www.timeanddate.com/worldclock/converter.html?iso=20200406T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [Delegated Ink Trail](https://github.com/w3ctag/design-reviews/issues/473) - @dbaron, @atanassov
* [Layout Instability Shifted Element Surfacing](https://github.com/w3ctag/design-reviews/issues/485) - @dbaron, @atanassov
* [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov
* [Image Resource](https://github.com/w3ctag/design-reviews/issues/490) - @dbaron, @atanassov
* Review Design Principles PRs

### Breakout C (APAC / Europe) - [2020-04-07](https://www.timeanddate.com/worldclock/converter.html?iso=20200407T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris
* [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @cynthia, @alice, @torgo
* [Service Worker Scope Pattern Matching explainer](https://github.com/w3ctag/design-reviews/issues/417) - @cynthia, @torgo, @kenchris
* [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @alice, @torgo, @kenchris, @plinss
* Review Design Principles PRs

### Plenary Session - [2020-04-08](https://www.timeanddate.com/worldclock/converter.html?iso=20200408T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Design Principles PRs
* Badging API
* Breakout Rollup
* Issue Triage

-----

### Breakout A

Present: Dan, Kenneth, Peter, Tess, Rossen, David, Yves

Regrets:

Tess: please go look at the [design principles PRs](https://github.com/w3ctag/design-principles/pulls) and evaluate them so we can merge on the plenary.

#### [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris, @atanassov

Tess: we were leaving this open to track where it went - we should keep it open.

Rossen that sounds right. I chatted with Dan Clark who was engaged on the review and he was in the same position.

[bumped a few weeks]

#### [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov

Rossen: this is a [big] proposal.  Getting up to speed.

Tess: bump one week?

Dan: schedule a special breakout?

[scheduled between Rossen and Tess and left on this week]

#### [Scheme-bound Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon

Dan: Started looking at this couple of weeks back (summarizes the GH conversation between him and Mike West)
Is there a standards position from Mozilla on this?

David: Don't know but there are a number of folks interested and looking at it.

Dan: It would be great to have an official standards position on it

Yves: It could be worth experimenting and see how it goes. The fact there are 2nd ... cookies it will require some coding from the site side. Otherwise I'm all for it.

Dan: Should we keep this open or record positive feedback from TAG?

Yves: Lets do that, record positive position and keep open to track feedback.

Dan: So we can put Pending External Feedback

Yves: Tess, can we get Apple's position on this?

Tess: I can ask around.

Dan: Yves, can you make these changes to the issue please?

Yves: ack, will do later today

Dan: Peter, can you bump couple of weeks again?

Peter: ack

#### [Imperative Shadow DOM Distribution API.](https://github.com/w3ctag/design-reviews/issues/486) - @hober, @kenchris

Tess: overall I think this looks good. I have one concern I'm writing up right now.  This proposal says - when you create a shadow dom you can choose manual or automatic. Automatic is the status quo. New mode: you have to use an API and slot things in different places. One cited advantage of the API is implementing something like the details element.  before having this feature you can't implement that feature on top of web components. One downside of the exclusivity of the two modes (man/auto) is that it's sometimes advantageous to have special behavior with some descendants but have the rest auto. My feedback is that I'd like them to make that case easier - some manual slotting and then "everything else auto".   Otherwise it looks great!

Ken: I looked it and also liked it.

Tess: i will mark as pending ext feedback

#### [WebAssembly SIMD review](https://github.com/w3ctag/design-reviews/issues/487) - @hober, @kenchris

Ken: I think it's pretty good. 

[discussion of JS SIMD]

Tess: it's surprising to me that there would be a desire to expose SIMD just to WA and not JS.

Tess: worried that the shape of the API of the web is being driven by expediency... that worries me.  I don't like the idea of JS and WA have different capabilities.

Ken: [WA] does have threading as well.. They are working on it [JS SIMD].

Tess: i will take a look soon.

Ken: our Intel SIMD experts have looked at this and ensured that it meets requirements...  I could have a talk with internal team .... This covers the use cases they have.

Dave: have some people reviewed that it makes sense across other architectures? 

Ken: it works on ARM.

Ken: will get additional feedback this week.

Peter: let's try to close it off at the plenary session≥

#### [WIP: Attempt to address some of the naming feedback in #132 and #149.](https://github.com/w3ctag/design-principles/pull/163)

Tess: Alice and I are working on changes.

#### [Add a section on CSS principles](https://github.com/w3ctag/design-principles/pull/166)

David: i added a whole section with 5 different principles... Tess reviewed it and had a few comments. Tab had some comments. I will see if I can get through those before the plenary. Also hoping to get more review.

Tess: I'm really excited about it.

[Fixes #126.](https://github.com/w3ctag/design-principles/issues/126)

[wide support]

Peter: in last paragraphs you talk about avoiding values like yes/no true/false... i wonder if that could be expanded to other areas as well.. Using enums as opposed to booleans.

David: I did think about that.

Peter: [puts note in]

#### [New principles related to private browsing mode and assistive technologies. Fixes #97.](https://github.com/w3ctag/design-principles/pull/167)

Tess: Dan & I had a breakout on this and this PR is a result. We came up with several distinct principles. One is a general "you should think about how your thing behaves in PB mode" .. it can be complicated.  The simpler principles are : BP mode should not be detectable by the page.  There are a number of concrete problems that happen when PB is detectable... e.g. paywalls detect PB mode.  The main concern is that people use PB mode because they need to - e.g. they live in a house with an abusive partner and they are looking up resources on how to get out of that situation. Important that it not be detectable. We also came up with "use of assistive technologies" should not be detectable. This came up a couple of years ago with AOM and AT.  These are the principles. We also added text to the "new features should be detectable" talking about how some features shouldn't be.

Dan: [approves]

Tess: I linked to the ethical web principles as a motivator - we should link the two where it makes sense.

Dan: I fell like this ready to be merged at the plenary.

### Breakout B

Present: Tess, Peter, David, Rossen

Scribe: Tess

Regrets:

#### [Delegated Ink Trail](https://github.com/w3ctag/design-reviews/issues/473) - @dbaron, @atanassov

Rossen: David and I looked at this in Wellington. We left detailed feedback that was largely agreed upon with the authors. I pinged the author and he said the current version of the explainer is ready for review, and it has incorporated the feedback.

... If you go to the current explainer that's proposed, you'll see this one is marked as archived, because the explainer moved to a WICG repo

... we've adopted this document status policy for all our (msft's) explainers

David: I've updated the issue to use the latest URL

Rossen: Are you able to follow up with the feedback you left, to see if the current version addresses it?

David: It looks like he filed a bunch of issues from our feedback and those issues are resolved; i need to look at the issue resolutions to see

Rossen: he did a good job of linking to the PRs that addressed each one.

... [gives example]

Tess: push this out a week or two?

David: Sure

[pushed out one week]

[rossen drops]

#### [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov

David: I was reasonably happy with how the blink-dev thread evolved

... I think people eventually agreed that there's more work to be done

... what is the TAG supposed to be doing about this? Fundamentally, lab and lch are simple, except that there's all this color gamut stuff, and I don't know coordination will happen if we don't do it, but I don't know if the TAG is particularly good at that

Peter: It is something we should do, whether or not we're good at it. Who should we reach out to?

David: I'm not entirely sure. I don't completely understand some of the color profile stuff. The other questions are how does it interact with canvas and compositing.

... does it make certain compositing optimizations more observable now?

Tess: I can run this by Simon and Dean

David: we should be making sure that the right people are looking at this

... it would be nice if some of the chromium folks working on this were also doing that

... seems the person working this on the chromium side is new to colors

Peter: are there any other places on the platform where color is exposed

Tess: HTML legacy (color attributes, input element), CSS, SVG, all different canvas contexts (2d, webgl, webgpu), media (video, images)

David: videos may be particularly interesting

Peter: WebXR?

David: the media stuff probably already has a bunch of color space stuff that isn't quite right

Tess: what's the next step here?

David: what are we concerned about? if we ask people to review, what do we want them to keep an eye out for?

... 1a. do you have the ability to specify all the colors you want to specify in this place

... 2. do you get interoperable results (lack of interop could be things like different working color spaces; different clamping to device gamuts; other things)

Peter: at some point things that expose raw bitmap data will want to do something more than 24 bits

David: 1b. so it's not just specify, it's also can you get them out

... another part of 2. making sure we don't create a bunch of corners... avoiding things being "whatever you want" rather than defined... e.g. untagged images in the past (now treated as sRGB). we want to avoid new things like that.

Tess: This plus the list of places to look at earlier create a review matrix

David: another part of 2: the definitions of `color-interpolation` and `color-interpolation-filters` properties in svg may have an interesting list of things that could be affected

[rossen returns]

Tess: could design-principles come out of this?

Rossen: this could be a good set of design principles, lots of cross-cutting concerns

David: I'll try to write a comment in the issue, summarizing the conversation we just had, and we should all try to rope in experts to do the review

... maybe Chris Lilley

Tess: when should we push this out to?

[push out two weeks]

#### [Layout Instability Shifted Element Surfacing](https://github.com/w3ctag/design-reviews/issues/485) - @dbaron, @atanassov

Rossen: this moved to WICG, the explainer link won't get you there

Tess: can you fix the link in the issue?

David: most recent comment says it's in the master explainer now

[aside conversation about change policy related to documents under review. rossen explained how it works for another api review board he participates in. we don't currently have such a policy. Hard to have document stability when reviewing living standards.]

Tess: L.I.S.E.S. is a very dense name. what does it even mean? ELI5

David: does "surfacing" here mean "we are surfacing this data with an API"

Rossen: yes.

... the idea is you compute a layout stability score, which is an approximation of how much layout has changed between rAF frames. 0 means no change. anything more than zero means your layout is not stable.

... this score is computed based on shifts that are not caused by transforms or scrolling. IOW if you're animating with transforms, your layout is actually stable. this is to catch dom nodes being inserted / removed, etc.

... this feature is intending to compute the cost of reflow at the document level by aggregating these per-frame scores.

... they have a couple of different multipliers, an impact fraction and a distance fraction. the impact fraction is a bit confusing. it computes a fraction based on the elements box in comparison to the overall animation frame. i don't know how and why that matters that much. distance is straightforward.

David: this came in post-wellington and assigned to today. i haven't looked at it. i feel some deja vu looking at this. there have been multiple attempts to solve this problem before. we've reviewed 2 or 3 of them.

Tess: why will this approach succeed when the previous ones didn't?

David: one thing I'm not understanding: how does what we're being asked to review here relate to the overall API we reviewed in [w3ctag/design-reviews#393](https://github.com/w3ctag/design-reviews/issues/393). i think what we're reviewing now is the "source attribution" section.

... i should read the source attribution section more closely.

... this is about saying in these layout shift reports it will put up to 5 elements and list them so the website can figure out what the problem is when it sees high layout shift numbers.

Tess: should we push this out?

David: i just read it. it has the feel of a lot of the web performance work. sites are having these problems, so we fish around for metrics to expose to help people debug their problems. the way to find that out is to get it out there and see if it's useful for people.

... one question: do these accumulate in a way that will keep orphaned nodes alive? i should add a comment with some questions.

Tess: okay, let's leave those questions & mark as 'pending external feedback'.

Rossen: in the privacy section, it says this exposes resource timing, and that means fingerprinting. it's limited to the current browsing context. re: resource timing and fingerprinting, i don't see why this doesn't apply to this api too.

Tess: sounds like a good question to ask them

[push out one week]

#### [Image Resource](https://github.com/w3ctag/design-reviews/issues/490) - @dbaron, @atanassov

[ran out of time; push out one week]

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

[ran out of time; pushed to breakout C]

#### Review Design Principles PRs

[ran out of time]

### Breakout C

Present: Ken, Dan

Regrets: Sangwhan, Alice

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

Dan: I don't feel like we can deal with this one without Alice & Tess... Let's bump to the plenary call.

#### [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

No explainer still; milestone changed to next week

#### [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @cynthia, @alice, @torgo

Dan: I asked Ada to comment. From my PoV I think we should close but I just wanted to be sure.  Let's hopefully have a discussion and be able to close it by the plenary call.

#### [Service Worker Scope Pattern Matching explainer](https://github.com/w3ctag/design-reviews/issues/417) - @cynthia, @torgo, @kenchris

Yves: still same version as presented in TPAC

Ken: yes.  so far nothing has happened.

Yves: let's bump it a month and see if it's changed...

Dan: has it been shelved?

Ken: yes, but not as quickly as the author would like. so it's not forgotten.

Dan: let's close it and ask him to reopen when he has something new.

Ken: closed for now

#### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @alice, @torgo, @kenchris, @plinss

Ken: good to see change

Dan: agreed

Ken: they are experimenting with it in chrome right now

Dan: I asked Amanda if there is a mitigation against the issue Rossen raised. Hope we can get a reply before the plenary.  I don't think there additional issues.

#### Review Design Principles PRs

### Plenary Session

Present: Alice, Ken, Peter, David, Dan, Tess

Regrets: Sangwhan

#### Plenary Scheduling

Plan is to stick to 20:00 UTC until Sangwhan becomes available again, and then switch to 05:00 UTC.

#### [Design Principles PRs](https://github.com/w3ctag/design-principles/pulls)

Peter: 163 (naming feedback)

Tess: not yet updated.

Alice and Tess to find time to coordinate on it.

Peter: 166

David: that's the big new section on CSS principles. It does have a working preview link now. Addressed most of the feedback. 3 pieces I haven't addressed. 1 of them was a small comment from peter that maybe something should be in the naming section. Could be deferred.

Peter: sure

David: ... all the remaining unaddressed feedback is about the first section - I could pull that section out and merge the rest. We could open up another issue or discuss it in another issue.

Tess: I think that's a good plan. In the project I'm tracking to migrate the html design principles [i can track this].

David: i will merge after i remove this first section

[consensus]

Peter: 167

Tess: we talked about it - Dan approved, David sent comments. the comments seem reasonable. If anyone else wants to review that would be great. 

Alice: will do.

Tess: maybe this is the same as the naming one - push out a week.

#### Breakout Rollup

**Breakout A:**

*CSS Modules* - bumped - progressing in tc39

*Origin Isolation* - scheduled a breakout for tomorrow

*Scheme-bound cookies* - Yves wanted to keep this open until expressed interest from other implementers

*Imperative Shadow DOM Distribution API* - overall liked the look and wrote a comment. Pending ext feedback.

*SIMD* - 

Ken: i said I'd talk to some of our people at Intel and I did.  One to one mapping for arm.  Work happening on the explainer.

Peter: can we close it off?

Ken: they're gonna write a better explainer - then we could have a look at it.

Tess: we should wait until they have a better explainer?

**Breakout B:**

*Delegated Ink Trail* - newer explainer; moved to WICG; Bunch of issues filed. Those issues have been resolved but we haven't looked how they've been resolved.

*CSS Color* - took a step back. our concern is arch consistency.  we generated a list of places to look where colors are used in the platform... and David made a list of interop concerns. we will find domain experts to assess the state of the platform for interesting color gamuts. Pushed out 2 weeks.

*Layout Instability Shifted Element Surfacing* - Rossen gave a summary.  David had a concern. David & rossen to followup.

**Breakout C**

Capture pan/tilt - we bumped it but it may get bumped more

WebXR: Dan to write question asking about accessibility

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

Alice: [reads her comment](https://github.com/w3ctag/design-reviews/issues/387#issuecomment-605769642) from 10 days ago and Matt Giuca's reply.

Tess: I don't have a strong preference between document or navigator.

Dan: Can we close?

[agreed to close]

#### Scheduling of virtual face-to-face

From David:

> BTW, I'm looking at the dates we've been thinking about for our [distributed face-to-face next month](https://github.com/w3ctag/meetings/tree/gh-pages/2020/05-distributed).
>
> Our current week has the issue that it has conflicts with the AC meeting plenary sessions (Mon & Tue) and with a holiday in France & Denmark (Thursday). The AC meeting session conflict would probably mean we'd need to move the Mon/Tue US/Europe session an hour or 90 minutes later (depending on whether we wanted a 30 or 60 minute break between).
>
> The week before looks like it has no holiday conflicts, although it would conflict with the materials coming out for the distributed AC meeting that many of us would want to look at.
>
> And there's probably some conflicts in that date range that I don't know about.

#### Issue Triage

* [untriaged design-reviews](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

**SM series algorithms in Web Cryptography #491**
 
David: They left out some material - i commented.

... checking for blink intent thread ...  none found ...

Peter: venue? this isn't even in wicg?  we don't want to review ideas for one engine unless they are in a venue 

Dan: [and have a trajectory]

Tess: we could ask them to run it by web crypto mailing list?  I will ...

Peter: ...and what's the venue for standardization....

**Window Segments API #492**

Peter: related to foldable stuff?

Ken: yes.  [assigned self

Dan: yes.

**Data for measuring audio-video synchronization and end-to-end delay in realtime communications #493**

Alice: i also assigned Sangwhan as he had some feedback on this.  Gave some feedback... WebRTC related... they want to ship this in next Chrome.   Sangwhan raised a compat risk. 

David: feels like there is more to discuss here  - also all the experts in the IETF on this topic.

David: I will reply re: IETF

**Declarative Shadow DOM #494**

Ken is on... Alice is on... Tess is on... Peter is on...

**AVIF Decode #495**

Ken: new image format; Dan

**















