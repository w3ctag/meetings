# TAG Minutes - Week of 9 June 2025

## Breakout A (Asia / Australia / West America) - [2025-06-10](https://www.timeanddate.com/worldclock/converter.html?iso=20250610T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Max

Regrets: Xiaocheng, Martin

Scribe: Jeffrey

### Agenda+
#### [install API redux](https://github.com/w3ctag/design-reviews/issues/1051)
#### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

Max: They added a response to the explainer: https://gist.github.com/domenic/c5bd38339f33b49120ae11b3b4af5b9b#doing-this-automatically-or-with-an-opt-in-from-within-the-worker

Jeffrey: Interesting reply. They (Chrome + Mozilla) are saying it's about as expensive to extend the lifetime by one task as to extend by ~30s. Don't know the implementation well enough to challenge that.

Max: They also point to Safari feedback.

Jeffrey: Which looks negative from Anne.

Jeffrey: Privacy difference from my suggestion is negligible since the developer can always intentionally extend up to the UA's limit.

Jeffrey: I'm inclined to see what Xiaocheng thinks. He and Dan C have the most context.

Max: Their S&P Questionnaire says they plan to add Connsiderations to the HTML spec.

Jeffrey: And it's just an early review.

Jeffrey: I note that the explainer, with the alternatives considered, ought to land somewhere. A Gist isn't a long-term home.

Jeffrey: I'll work with Xiaocheng to post a comment.

#### [design-principles#501: Guidance about reflecting state in HTML attributes](https://github.com/w3ctag/design-principles/pull/501) - @LeaVerou, @martinthomson, @xiaochengh

Jeffrey: Question is whether we close this until lukewarlow or someone else drafts text, or leave it open.

Max: Wait a little more, since it's only been 2 weeks.

#### [design-reviews#1096: WebRTC Encoded Transform  Audio Level](https://github.com/w3ctag/design-reviews/issues/1096) - ready to close? - @martinthomson

Max: Use case looks reasonable.

Jeffrey: Martin's draft comment looks good to me.

[Agreement that Martin should post his comment.]

### PRs
#### [design-principles#567: Add 'Choose the Appropriate WebIDL Construct for Data and Behavior'](https://github.com/w3ctag/design-principles/pull/567) - @marcoscaceres

Jeffrey: Needs Marcos to update this. I'm inclined to mark it as Draft until Marcos comes back to it. I'll suggest this on #design-principles and wait until next week to do it.

### Additional Design Reviews
#### [design-reviews#878: confidence reporting for PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - see new comment, responding to @martinthomson - @jyasskin, @yoavweiss

Jeffrey: I think Martin's right that the performance APIs are a fingerprinting vector, but I don't know how much of a problem it is. We should have a discussion about what the TAG's position should be.

Max: If that's a concern, the design of the API should have some mechanism to mitigate it.

Jeffrey: They did try to mitigate it, but Martin's unhappy with the differential privacy they used.

Max: Need more discussion.

Jeffrey: If we schedule it for Breakout C next week, Yoav might be able to dial in.

#### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres
#### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres

Max: There are plenty of applications that have this feature, but it's built on existing APIs. Proposal is to define browser API. 

Jeffrey: Goal would be to do the inference locally without incurring the download cost for every website.

Max: I share Mozilla's worry that it might not be worth it.

Max: Can the developer choose the model?

Jeffrey: No, which is safer for Writing Assistance than Prompt.

#### [design-reviews#1080: [wg/payments] Web Payments Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1080) - @marcoscaceres, @maxpassion

Jeffrey: The Team has sent the AC review for this, so the review is up to AC reps.

Max: We want clarification about digital wallets in the charter. Not technical concerns.

Jeffrey: It's about how much they coordinate or take over the design from the identity WGs.

Max: Scope includes digital wallets. If Marcos has time, he should finish his work.

Max: I'll propose a comment in Brainstorming and let Marcos check.

## Breakout B (America / Europe) - [2025-06-11](https://www.timeanddate.com/worldclock/converter.html?iso=20250611T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Yves, Matthew, Lola, Christian, Serena, Jeffrey, DanA (2nd half)

Regrets: Hadley, Sarven

Scribe: Matthew

### Agenda+
#### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

Jeffrey: This got a reply from the proponents; feel it's a question for Martin mostly. Anyone else watching?

Lola: +1 seems for Martin

Jeffrey: Bumping to next session. My summary is that Martin's suggestion is to use cookies and sign the cookies, and he shows ways to get back all the features that the DBSC has, but at least his servver-side picture looks more complex than what is being proposed. However I and the proponents don't seem to be convinced.

Lola: How would we resolve something like that?

Jeffrey: We don't have to agree with the proponents; if the TAG thinks there's a better way to do it, and the proponents are not convinced, we resolve as unsatisfied. If there's not consensus in TAG, then we say that. There's a resolution label for that. (There's 'ambivolent' and 'lack of consensus' so we can pick whichever is best.)

#### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @torgo, @lolaodelola

Jeffrey: This is specifically about shared workers. There was discussion over the last couple of weeks.

Recent discussions: https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/906

Yves: Action on Dan to write the closing comment.

Matthew: We talked about doing some long-term planning on this too (also relating to related sites TF, that I think we're going to set up).

Lola: +1 on doing more work - aligns better with Privacy WG? Planning to pitch to Nick.

Jeffrey: Do you have a sense of whether the WG or CG is the better venue?

Lola: Haven't been involved in CG in a couple of years. Could pitch it there too.

Jeffrey: I'm neutral too. The spec is officially in the CG, but don't know if they discussed this change.

Lola: For this specifically I think the CG is best, but I'm thinking about the proposed TF work (on specifying related sites).

Jeffrey: Catching up with minutes.

Lola: Also sharing data across domains. Trying to address the umbrella thing.

Matthew: Pretty sure I suggested Ehsan to participate in this, who I nominated as an Associate. There are multiple efforts in different groups to express relationships between sites. Different use cases, privacy/security properties. Reduce wheel-reinvention. Relates to the recreation of 3p cookies. User control in addition to author control. 

Lola to file the WG issue / Talk to Nick Doty. After hearing from DanA. Re-discuss tomorrow.

*We came back to this later*

DanA: This is a good idea, to raise it with the Privacy WG.

Lola: I will create an issue; can be taken off tomorrow's agenda.

#### [explainer-explainer#19: Explainers are an anti-pattern](https://github.com/w3ctag/explainer-explainer/issues/19) - @jyasskin, @torgo

Jeffrey: Related PRs, which I propose as solutions to this issue:

* [design-reviews#1102 Rethink the TAG's review intake process](https://github.com/w3ctag/design-reviews/pull/1102)

  Jeffrey: We discussed the 're-think the TAG intake process' 2wks ago. I got updates made on Monday. Have people looked at it enough to discuss it?
  
  We think explainers are useful, but if you're already writing a spec the info may be in there. So whilst we will likely reject the issue overall, we need to fix the problems Manu raised.
  
  This one asks for an explainer in all cases, but makes it optional after incubation.

  Matthew: Won't be able to review this in detail this week. I can't ever remember reading a spec that contains alternatives considered, but it's vital for reviewing it. Do agree that lots of stuff could end up in the spec. Then the explainer ends up as a series of links to the relevant spec sections. But want it to be in some form. Don't want busywork, especially not duplicate. But surely there will always be things that you wouldn't put in a spec.

  Jeffrey: Think you're saying we should always insist on an Explainer, but some of the sections will end up as links to sections in the spec.
  
  Matthew: Yep!
  
  Yves: Some groups want to produce Primers. That could replace the need for Explainers. It would be more general to explain, usually for a set of specifications, not just one. Can be very useful.
  
  Lola: We discussed this in Docs CG last week. Consensus was Explainers are incredibly useful when writing web docs targeted at developers - e.g. translating a spec into MDN docs. People doing that will use the Explainer if they know it exists. There's a period where the Explainer is not useful anymore, even to those people. For me personally, when I'm reviewing a spec, the Explainer is incredibly useful, even when it's been incubated. There's a way people write in specs vs in Explainers that's more approchable in Explainers. Even if you're linking to sections in the spec (from the Explainer) it's going to take longer to understand. I'm OK with there not being an explainer if spec authors write in a way that's more approachable in the spec, but that's a harder ask. We're not copy editors. Apprehensive about linking to parts of the spec.
  
  Jeffrey: To Yves' point, Primers may replace the novice intro part of Explainers, but they would not likely contain Alternatives Considered, so we need to keep that.
  
  Yves: In many cases Explainers also don't contain that, and the requesters put that into the issue where requested it.
  
  Jeffrey: I recall more often they are in the Explainer than the issue, but we always ask for it when it's not there.
  
  In [the intake form](https://github.com/w3ctag/design-reviews/pull/1102/files#diff-78c184074b237b7be946da618119b421b2aeef327081d4d41bb54f9273040f47R98) I say 'An introduction to the feature, aimed at unfamiliar audiences'. In the [explainer-explainer PR](https://github.com/w3ctag/explainer-explainer/pull/25/files), I have "As your specification evolves, be sure to maintain the introduction, use cases, and examples so that novices can still read them."
  
  Can we make that cultrual change happen?
  
  Lola: I think that's going to take a lot of time.
  
  Jeffrey: Once the spec has been a spec for a while, and becomes out of date, and they're left for the introduction written for experts in the spec, so if we can make the cultural change we will be in a better place.
  
  Lola: Recent case, the WebRTC spec got some proposed ammendments, which were very minor, but there was something in there that was quite specific. I think a well-written Explainer (I think they did have one) helps to navigate that. WebRTC is a niche technology, so even without that (new) Explainer, it would have been harder to determine why the change was being made, what it was for, and how to understand it.
  
  Jeffrey: Is that something that ought to go into the spec anyway? Or only appropriate when evaluating the change.
  
  Lola: The spec doesn't keep track of every change that happens, so it was only relevant when evaluating the cahnge. The spec doesn't in detail describe every change.
  
  Jeffrey: So the question is how do we express that in our intake forms and Explainer Explainer. Suspect we will get a better answer async.
  

* [explainer-explainer#25 Say that explainer contents should move into specifications](https://github.com/w3ctag/explainer-explainer/pull/25) are ready for review

#### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @torgo, @matatk

Matthew: Last week I put in Ehsan's tuppence. Some bits are what's missing from explainers. We talked about it in TAG calls last week. Dan asked for the overall motivation. Asking for a primer about the series of specs. Looked at the feedback in Private Brainstorming, and haven't gotten to addressing our concerns. 

Jeffrey: So we need to draft an opinion comment?

Matthew: We should invite them to a TAG call. Dan's court to invite them to a call.

### PRs
#### [design-principles#575: Add Criteria for Design Principles to README](https://github.com/w3ctag/design-principles/pull/575) - @csarven

Sarven sent regrets - should we bump this?

#### [explainer-explainer#23: Auto-publish the explainer explainer to TR space.](https://github.com/w3ctag/explainer-explainer/pull/23) - @jyasskin

Yves: Should be published Thursday. Once that's done, we can set up Echidna.

### Additional Design Reviews

#### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @matatk, @dandclark

Matthew to draft, with Jeffrey's help.

#### [design-reviews#1105: ScrollIntoViewOptions container attribute](https://github.com/w3ctag/design-reviews/issues/1105) - @zcorpan, @dandclark

Jeffrey: DanC drafted a comment; we can post.

#### [design-reviews#1075: Review request for AriaNotify API](https://github.com/w3ctag/design-reviews/issues/1075) - @matatk, @lolaodelola

*Already closed*

### Page-embedded Permission Control

Jeffrey: Google and Mozilla folks met; making progress. Google's concerns around need to be able to re-request permissions, which they believe requires the browser to know the user saw UI about the permission; Mozilla would like to be able to use these to replace mute buttons. Concern around labelling of buttons. Mozilla thinks having a button and knowing where the user clicked should be sufficient to show the prompt again, but Chrome disagrees.

Serena: Sense I got from the conversation was it seemed Mozilla folks wanted an ideal end state that we could get to immediately. The Chrome people were more trying to iteratively go in a particular direction. This was another point of contention. How idealized must the first step be? Seemed like a really productive conversation. More agreement than expected.

Jeffrey: I feel there's not a whole lot for TAG to do right now; it might come back to us later. We should encourage the Safari person to talk about this also.

Marcos (12 of June): I think we should review this again.  

WebKit position: https://github.com/WebKit/standards-positions/issues/270 
Mozilla position: https://github.com/mozilla/standards-positions/issues/908 

#### [design-reviews#1104: [wg/apa] Accessible Platform Architectures Group Charter](https://github.com/w3ctag/design-reviews/issues/1104) - @matatk

Matthew: Unsurprisingly, I'm in support of this charter.

DanA: No substantive changes except for something about registries.

Jeffrey: Symbols registry doesn't seem objectionable.

Matthew: There's a potential conflict with i18n on the symbols.

Jeffrey, after meeting: The Ruby issue was https://github.com/w3c/bp-i18n-specdev/pull/145.

Consensus to resolve as `satisfied`.

## Breakout C (Europe / Asia / Australia) - [2025-06-12](https://www.timeanddate.com/worldclock/converter.html?iso=20250612T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Xiaocheng, Marcos, Dan, Christian, Yves, Max

Regrets: Matthew, Martin, Hadley, Lola

Scribe:

### Agenda+
#### [design-reviews#1101: env(preferred-text-scale)](https://github.com/w3ctag/design-reviews/issues/1101) - @christianliebel, @xiaochengh

Christian: it looks fine from my pov... some concerns jeffrey raised are also valid... ask these questions back to the proposers?

*christian to pose Jeffrey's comment and then we see if we can close next week.*

#### [design-reviews#1079: Page-Embedded Permission Controls](https://github.com/w3ctag/design-reviews/issues/1079) - @martinthomson, @marcoscaceres, @matatk, @heisenburger

Dan: *reprises discussion in Breakout B*

Marcos: need to catch up on this... given consistent feedback that ... you need an equiv JS api so... this has very little value.  That's Webkit's current position... 

... this is a signifigant shift in the architecture of permissioning.  It means there shall not be an API ... all new APIs switch to this model, or we keep having an API... It's signifigant to the permissions architecture.

Dan: Sounds like Marcos and Jeffrey need to chat about this - suggest teeing it up for breakout A next week.

#### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - check status - @matatk, @xiaochengh

Xiaocheng: we received a response and I think ... first they provided data about how common the triggering is... data is 94% of top web sites use this form... pretty solid proof of the use cases... And then discussed the clash of triggering and speculation rules... seems like this is a fixable issue. For discussion: we are focusing too much on using triggering for link preview... but could also be used for showing a "tool tip" which is not link preview. Focusing too much about conflict with another feature in link preview scenario might be not focusing on the most important stuff... So my opinion is that we may express a concern about clash but we should not make it a very strong concern...

... other thoughts?

Marcos: *concerns around long pres behaviour* 

Dan: also standardizing the long press function... might be inappropriate.

Marcos: can you cancel a default behaviour? An example might be right click... what happens when you right click is different one ach platform.  When you do a long press, is the default behaviour cancellable?  Do we believe as the TAG that ... this should be a cancellable action...?

Dan: some web sites *do* override the right click behaviour... 

Marcos: But this wrecks the UX in so many ways... e.g. you have a password field that doesn't allow you to paste... that's why there's resistence on the webkit side... But there is precedent for this ... e.g. clicks, mouse swipes, etc... it's whether it will harm the UX... We've seen in the past that these UXs **are** harmed... E.g. not being able to click the right click menu... 

Dan: feels like the UX should be up to the "marketplace"...  Proposing a *satisfied with cocnerns* with some guidance about how it could be harmful if not implemented correctly...

Marcos: for webkit it doesn't feel like something we would like to change... but that could change...  I don't know what the default behaviour in chrome... "would preventing the default do more harm than good?"

Xiaocheng: it shoes a context menu... and highlights the text... 

Xiaocheng; I think UX consistency with the platform is important but we should not disallow overriding because developers might want to ensure consistenty within their ecosystem.

Christian: I tend to agree with Marcos that ... bothers me if people block right-clicks or provide their own search interface... But ... I think it would still make sense to do it... they are proposing this to auto-open popups on web sites... on desktop the signal is hovering... What they try to look for is a signal on mobile... it would be broken if that would only work on desktop and not on mobile... it maay make sense to have it. There *was* force touch ... on IOS side ... it was made available to web sites... was exposed to develoeprs... https://developer.mozilla.org/de/docs/Web/API/Force_Touch_events 

Marcos the proposal is so large... if they strip it back to just that event ... but they have over-engineered this so much... The crux of it is... is this really just about long press or not?  In the brainstorm ... we asked "can we get this back to the fundamentals" ... 

Dan: overriding a long press could be a "primiative"...

Dan: do we need them to do this work in order to...

*debate about whether we should ask them to possibly split this proposal to "override long press" and everything else*

Xiaocheng: difficult to find a meaningful way to split it... if any part is missing... if only have the interesttaeget attribute without default triggering behaviour... but if we say "we're going to override the default behaviour of longpress" but we don't say what the new behaviour is... similar if we split the popover from this proposal then it's incomplete... splitting it doesn't introduce a complete behaviour...

Marcos: could we have a high bandwidth discussion - get them on a call?

Dan: Next week's plenary? or **breakout A**... 

Xiaocheng: it's about the scope of CSS in general.. should it just control the presentation or should it control user interaction on elements. There is a companion propsal in CSS for the "delay" to trigger that ...

Marcos: it's a good question.... 

Xiaocheng: this also came up regarding carousels...

#### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

#### [design-reviews#1097: Browser Bound Keys for Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/1097) - @torgo, @marcoscaceres

*punt to next week*

### Digital Credentials Finding


### PRs
#### [web-no-papers#3: Add some text about email addresses](https://github.com/w3ctag/web-no-papers/pull/3) - @martinthomson


Marcos: Maybe helpful https://developer.apple.com/videos/play/wwdc2025/232/ 

Marcos: I just did a talk at WWDC on this... how it's implemented... on Apple platforms. That may answer some questions... you can play with in chrome and safari in the betas... I think it would be good... I would be happy to drive and show and answer questions around the experience... and how we solve some of these issues in IOS and MacOS... And also if there are things we have overlooked .. Everyone is concerned... has the same concerns... Hopefully these can be alleviated. 

... I do think it would be good to do a finding on this but it can't be alarmist...

Marcos: can we set some time aside for Dan, Martin and I to get together...

*we discuss next week before or after **breakout C***

#### [design-principles#575: Add Criteria for Design Principles to README](https://github.com/w3ctag/design-principles/pull/575) - @csarven

### Additional Design Reviews
#### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson
#### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @torgo, @ylafon

*no progress ...*

#### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

*no update*


## No Plenary Session

## Design Reviews Backlog
#### [design-reviews#945: FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @torgo, @hadleybeeman
#### [design-reviews#974: FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974) - @torgo, @hadleybeeman
#### [design-reviews#935: FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @torgo, @hadleybeeman
#### [design-reviews#803: FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @torgo, @hadleybeeman
#### [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres
#### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman
#### [design-reviews#992: FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @martinthomson, @torgo, @hadleybeeman
