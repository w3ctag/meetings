# TAG F2F Wellington March 2020 Minutes Day 1

Present: Ken, Tess, Alice, Peter, Yves, Rossen, David, Hadley (Remote), Dan (Remote), Sangwhan (Remote)

### Agenda

(Should be the same each day)

* 14:00 (UK) - 16:00 (UK) - Breakout UK1 
* 08:30 - 08:50 Arrive
* 08:50 - 09:50 Plenary (60m)
* 09:50 - 10:30 Breakout 01 (40m)
* 10:30 - 10:50 Tea (20m)
* 10:50 - 11:30 Breakout 02 (40m)
* 11:30 - 11:50 Break (20m)
* 11:50 - 12:30 Breakout 03 (40m)
* 12:30 - 14:00 Lunch (90m)
* 14:00 - 15:00 Breakout 04 (60m)
* 15:00 - 15:20 Tea (20m)
* 15:20 - 16:20 Breakout 05 (60m)
* 16:20 - 17:00 Readouts (40m)

## Minutes

### Readout from UK1 breakout

Hadley: [readouts from UK breakout]

### Breakout 🇬🇧1

Present : Dan, Hadley

#### [Screen Capture 2019](https://github.com/w3ctag/design-reviews/issues/440)

Hadley: good to see that Mozilla, Cisco and Google people are involved in this spec.

...discussion of how this relates to [last screen capture review](https://github.com/w3ctag/design-reviews/issues/309)... (issue 309). To be clear, this looks like continuation of 309.

...reviewing the explainer, reviewing the spec, reviewing the security & privacy questionnaire responses...

... lots more in their s&p questionnaire from last time... 

Hadley: section 8.1 .. does a good job of laying out the problems...  How to designate what is background and what's not thought?

... "Window display surface" is defined - "display surface" is all the windows available to an application...

[discussion of what constitutes the background]

... hence the "MUST NOT" ...

[discussing permissions & consent]

8.2.1 - it's not clear exactly what they're talking about... maybe need some more explanation of what is meant by "active user consent" ... 

Same with 8.2.2 - Need more explanation of how this could be used to circumvent cross-origin protections, and for who (the sharer or the receiver)... Need to define what they mean by elevated permissions and how these are acquired, etc... Are they in the OS? Or for the website? 

Whole sentence "A user agent SHOULD persist any elevated permissions that are granted to an origin. An elevated permissions process in part relies on its novelty to ensure that it correctly captures user intent.".. needs further elaboration or a reference to some other place where these concepts are defined and discussed.

Dan: So that's security and privacy. What else can we help with? 

Hadley: section on device identifiers...  something needed about how they're issued? "must not be enumerated by `enumerateDevices`" - great.  So does the implementation come up with new, temporary device IDs?  Does it need to spell that out? (this in section 5.1)

[we left some feedback on the issue]

Dan: could still benefit from someone who has more webrtc expertise looking at it from an API design perspective.

#### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438)

Reading [comment from 4 days ago](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-592066616) from Brian...

Hadley: not sure I understand - he's reiterated his points that he wants mathml to be less special - wrt the dom, css, html, etc... (e.g. units)... introducing a few new things... He's had to make compromises to make it backward compatible.  How do we help developers where this fits with CSS and where it doesn't?

Dan: it's about the developer experience - especially someone who has experience with web technologies : html, css, dom, etc.. but is now trying to make use of mathml.

Hadley: exactly.  It would be good to make it a little more obvious (to developers).

Dan: one might say that this is not necessarily the job of a W3C spec.. but it may be the job of the explainer - especially if the explainer then becomes the seed of a documentation set e.g. on MDN.

Hadley: my bias is that specs I've been involved with have been developer focused. Maybe we should ask in a kind of helpful way if he's planning to produce documentation for developers and if so to cover off that point.

Dan: Agreed. And my personal opinion would be that MDN would be the right place for that. - e.g. going along with the existing MDN mathml docs https://developer.mozilla.org/en-US/docs/Web/MathML

[left some further questions for Brian]

#### [Design issues for signed exchanges](https://github.com/w3ctag/design-reviews/issues/354)

We discussed and left a note requesting feedback from Jeffrey and indicating intent to close this week if we don't hear back.

#### [Subresource prefetching+loading via Signed HTTP Exchange](https://github.com/w3ctag/design-reviews/issues/352)

This has been proposed closing since 3 December and it looks like some updates to the explainer have been merged by horo-t based on our comments, so we are going to close.

#### [HTTP state tokens](https://github.com/w3ctag/design-reviews/issues/297)

Reviewing [comment from Mike](https://github.com/w3ctag/design-reviews/issues/297).

Hadley: mike is in favour of closing it.

Agreed to close.

#### [Get installed related apps](https://github.com/w3ctag/design-reviews/issues/436)

Dan: Comment [from Rayan on the 29 Nov 2019](https://github.com/w3ctag/design-reviews/issues/436#issuecomment-559760309)... talks about adding abuse considerations to the explainer...

Also of note, looks like Microsoft is supporting this API...

Hadley: implementation doc is a google doc...

Hadley: we should look at the explainer... Also is this another example of where people are saying "this is rubbish already so we're not making it more rubbish" - and do we want to support that?

Dan: I think it's an example of someone saying "it's already like that in native, so why does the web have to be different?" And I think the web does have to be different; see the Ethical Web Principles.

...My point was: if they already have a PWA, and they prefer to use the PWA, but the API doesn't know that the PWA is installed... We should be building this API to encourage the use of web applications. 

Hadley: I agree. 

Dan: This API is built around native applications, and how web applications interact with native applications. But if the user has already made an affirmative choice to use PWAs, then the web platform should support that use, rather than redirecting them  to native applications.

[looking at the spec https://wicg.github.io/get-installed-related-apps/spec/]

Hadley: it's web app to native app, in the spec.

Dan: Right; that's the problem. If a user has installed a PWA, and a w3c-specified manifest file has designated that PWA, then this API should at least acknowledge the existence of installed web applications.

Otherwise, what are we building here? we're not building anything coherent. This is an architectural issue.

Hadley: this proposal is building a way out of the web. 

Dan: If I were to channel Tess, she might say: wait a sec: the idea of an installed web application is not a fully implemented, across the board thing. And webkit has some issues.

...But on the other hand, they partially support the manifest file, and the manifest-file-based installation of web application on a device is supported across browsers. 

...That should be taken into account in this. 

## Plenary day 1, morning

[Discussion of when to meet with Alan to talk about DIDs]

### Readback of UK breakouts

**Screen Capture**

Hadley:

- Explainer has improved
- More on privacy and consent
- Still need more info on use cases
- Discussion on device identifiers - mentions that enumeration must not happen but doesn't mention the alternative

David: An alternative to Device enumeration could be letting user pick what to capture, rather than having enumeration in the API at all

Hadley: They didn't spell that out explicitly... maybe they should?

Tess: (may have opinions)

**MathML**

Hadley: 

- Largely in better shape, more fleshed out
- Trying to make it more webby, but trying not to break backwards compat. Somewhat supporting CSS... would be helpful to describe for developers where this fits...

Dan: I feel like this may be ready to close. Let's wait for the answers from Brian though, in case he has any more questions for us.

**Design issues for signed exchanges**

Hadley: 

- Asked if there was anything to keep this open on

**HTTP state tokens**

Hadley:

- Closed.

**Get installed related apps**

Hadley: 

- API to direct from a website to a native app.
- As Dan was pointing out, we have a lot of cross-browser momentum for webapps installed on the device (i.e. PWAs) whereas this takes you away from the web
- Would be nice to see encouragement of using PWAs, this API should at least acknowledge installed PWAs.

### Breakout 01a

Present: Tess & David 🇳🇿, Dan, Hadley 🇬🇧, Special Guest Dan Brickley  

Scribe: Dan

#### [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477)

Tess: you have a web site that has some kind of interesting sequence of media and it wants to specify a feed you can subscribe to .. the idea is that user agents can detect there is such a feed by including it as content on the page.  My initial take: we already have feeds.. they already have media specific support.. that's how podcasts work.. so why do we need something different?

Hadley: i think we should give that feedback...  Explainer says media/rss is an alternative.. but not enough detail... 

Tess: I think that is not true.

[danbri enters the room]

Tess: proposal is in-page blob of json-ld - contains schema.org info about the nature of the media.. and so in this explainer they say they didn't consider using RSS because they can't express the detailed metadata.. but you can express schema.org semantics in an atom feed just as easily as json-ld. so i feel this is a misinterpretation of rss/atom.

Danbri: rss & atom don't model e.g. the episode number etc...

Tess: they could say "atom + some schema.org stuff".

Hadley: is anyone still looking after atom? 

Tess: it can be extended... You can already link to an atom feed from html... Generating a novel feed format...

Dan: do we want to say "don't use this JSON thing, use this XML thing instead?"

David/Tess: but people are using that technology already... 

Danbri: the schema side of thing should sit on top of everything.  At Google we pull in info from netflix and other tv providers using this format...  writing another parser to pull it out of atom is not rocket science.  Hard part is the semantics.

Hadley: good thing to phrase back to whoever the author is - what are the benefits of going for a new format vs using ATOM?

Dan: does this embed the feed data?

David: this isn't embedding within a document - it's adding the feed URL to the webapp manifest.

Tess: i will try to distill this conversation into a comment ...  Interoperating with existing tools, why invent a new format... cost of introducing new formats to the web is high.

Hadley: if we're going to turn this into a [discussion] between XML and JSON, there are enough who roll their eyes between different formats that this might not be a good decision to base on those loyalties...

Filed [an issue](https://github.com/beccahughes/media-feeds/issues/10) on the proposal with the above feedback.

#### [HTML horizontal review: CSS](https://github.com/w3ctag/design-reviews/issues/456)

Tess: two issues to review html issue #4406 - 

David: Firefox used to implement what the spec said and then there were web compat problems - spec changed to match what webkit and blink to. This has to do with images and alt text...

Tess: we think this looks fine. checking this off.

Tess: now looking at html issue #4747  This is the case of parsing ... 

David: 3 separate issues that this fixed...  This is not architectural.

Tess: I think we can summarily check this off.

[issue closed]

#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463)

[left to another day]

#### [HTML horizontal review: XML](https://github.com/w3ctag/design-reviews/issues/455)

Tess: one pull request - html issue #4384 - 

Hadley: [resorts to higher authority]

Tess: if you navigate to an xml doc and the namespace of the root element was known to be processed by another tool you have installed that the browser dispatch the document to another tool

David: in lieu of parsing it... e.g. maybe it's a feed and you should do feed handling

Dan: It sounds like a dead dream.

Tess: seems like a clean change to remove. comfortable that there are no architectural issues.

DanBri: You might try a mailing list to see if people are using it.

Tess: original issue filed in May 2017. 3 years - plenty of time to comment.

Tess: also it got removed in Feb 2019 - that is when this merged. noone has noticed.

Hadley: it's waiting for us.

Tess: the review we're doing is stuff that was merged between specific dates - do we notice anything concerning?

David: this is our processing of the HTML WG's horizontal review request .. Firefox used to have some RSS support support, but even that didn't use this.  Other support link rel=.. then we should show an icon.

Tess: I'm gonna close.

[recording consensus to close]

### Breakout 1b

Present: Alice and Peter

#### [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198)

Mike notes that there is an [intent to ship](https://groups.google.com/a/chromium.org/g/blink-dev/c/Il-wfnw9TAw/m/n3BUe4MgBgAJ), but urges us to provide any feedback we may have.

Peter: Not clear that every possible injection sink has been covered and that all future sinks will be. How do we ensure that this policy is adhered to?

... This provides an alternative to strings at injection sinks... you pass this in instead of a string. I wonder if we should add new APIs should just use trusted types...?

... e.g. instead of .innerHTML = TrustedHTML, add a new API which only uses trusted types, something like .setTrustedHTML(TrustedHTML). Then all new APIs going forward should only use the trusted types.

... Then the policy could turn just off the string-based APIs.

Alice: Might be good to have David and/or Sangwhan take a look at this, given they've had comments.


#### [Custom State pseudo class](https://github.com/w3ctag/design-reviews/issues/428)

Peter: I think the CSSWG has this under control.

... Closing with a note.

#### [CSS intrinsic-size](https://github.com/w3ctag/design-reviews/issues/437)

Alice: Seems like this has changed into a different API, per the last comment. The explainer has been removed. (And in fact no use cases could be found for `intrinsic-size` per https://github.com/w3c/csswg-drafts/issues/4531#issuecomment-572184579)

Peter: Some use cases mentioned by David in the [CSS issue thread](https://github.com/w3c/csswg-drafts/issues/4531)

### Breakout 1c

Yves and Rossen

(minutes taken during readouts by David)

Yves: We discussed only the issue on freezing the UA string.  We didn't get to the other two. 

Rossen: Yoav is going to close this issue and try to come back with ... proposed that the issue be closed, and the discussion move to principles of how this should be done from the POV of the TAG, and what Yoav is asking about.

Yves: There's a lot of discussion in that issue that goes beyond the issue at stake.  Multiple issues.  What happens when you have privacy features that forbid using Client-Hints infrastructure?  How do you do feature detection?  Does it discourage use of those privacy features?

Rossen: If you have a user privacy setting, would requesting and allowing client-hints circumvent that?  I don't think that was captured in issue here.

Tess: In the past we've had the idea that private browsing mode shouldn't be detectable.  So if you have an enhanced privacy mode of some variety that sends fewer Client-Hints, doesn't that expose that it's on?

Rossen: Yves's framing in the morning was interesting.  The proposed GREASE or randomness to discourage disallow lists, will work fine but not help in the allow-list use cases.  Arguably less used but still used.

Yves: Also UA detection happens on the second interaction but not the first.  In some cases you want it to work on the first one, e.g., for `Upgrade-Insecure-Requests`, where you really want to know in advance to avoid mixed content that doesn't work.

Rossen: Another point raised in the past is that GREASEing will have inadvertent negative effect on unpopular/small usage browsers, because they'll have a hard time passing the GREASE factor.  Rossen: A [good summary](https://github.com/w3ctag/design-reviews/issues/467#issuecomment-586202321).

### Breakout 2a

Present: Alice & Tess (NZ), Hadley & Dan (UK)

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)

Tess: the thing to read is: https://blog.whatwg.org/focusing-on-focus 

[reviewing]

Alice: I don't think click focusable should be a thing at all... Long web components discussion of types of focus...  

Dan: you think click focusable is the same as sequentially focusable?

Alice: by and large yes....  some differences in implementation exist between safari and others...

Dan: so you have a fundamental issue with the approach described in this post [since the introduction of the concept of click focusable seems to be kind of a key part of it]

Alice: [tests out behaviour of different browsers]

Alice: if something is not sequentially focusable why is it click focusable? what does that achieve? It means anyone who is a dedicated keyboard user can't focus on it. It would be nice to get an insight into why something might be click focusable but not sequentially focusable? My beef is more with the behaviour of tabindex opting into the irritating behaviours... tabindex -1 opting into click focusability. no way to opt out of click focusability while being programmatically focusable. Issue I'm filing offers a way around that...

Tess: I think this has all be a mess on the platform - i like the general idea of trying to clean them up..

Dan: [sympathetic to click and sequential being the same and therefore could this could be simplified further]

Alice: 2 cases where they diverge - Safari's behaviour where you have to opt in a certain approach.. To me that seems odd behaviour... however the other exception - in every browser, something with tab index -1 intended to be excluded from sequential tab order but is always click focusable - which never makes sense...

Dan: so a developer might be thinking "these are the fields that the user will want to tab through" without thinking "these are the ONLY fields that someone only using a keyboard will want to use"?

...That fits with my experience

Alice: ARIA guidelines... use of -1 .. 

[discussion of tabindex -1 and why it's useful]

Alice: also managing focus around transient ui... people will set focus to a container div with tabindex -1 to ensure that the scroll goes there & that the tabindex starts there...

Dan: is there a receptive audience in WhatWG to these issues?

Dan: write some feedback on our issue and get feedback from the WhatWG people (e.g. Rakina) who are working on this...

Alice: click focusability in the absence of sequential focusability is a concept that is problematic in 2 cases. One - in safari - elements that are click focusable but not tab focusable are not always [accessible]? **So I think the concept would make more sense as "user focusable".** Elements that take text input or are select boxes should be sequentially focusable everywhere. 

Dan: issue with use of the term "click - i like the more generalized approach ('User focusable').

Alice: tabindex -1 click focusable but not user focusable - i think that's incorrect. but I think we should survey developers about this.

[action for Alice to write that up as an issue on the whatwg spec with a TAG hat on]

Alice: I will write feedback in our issue first.

#### [HTML horizontal review: Accessibility](https://github.com/w3ctag/design-reviews/issues/459)

[closed]

#### [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432)

[reviewing the current status of the issue]

Hadley: syntax changes and semantic changes...

Tess: from a perspective of arch consistency.. do they parse non-negative reals the same way we do elsewhere on the platform?

Hadley: 
 https://github.com/w3c/ttml2/issues/943 <- explains how they want to do it...
 
Tess: suggest Hadley & Tess do a breakout separately ...?

Scheduled for 11a

#### [Revitalizing and generalizing the "HTML Design Principles" document](https://github.com/w3ctag/design-reviews/issues/426)

[bumped]

### Breakout 2B

Present: Kenneth, David

Went through three sets of HTML issues, nothing popped up, closed all three sets.

* [HTML horizontal review: Form controls](https://github.com/w3ctag/design-reviews/issues/449)
* [HTML horizontal review: The Event Loop](https://github.com/w3ctag/design-reviews/issues/453)
* [HTML horizontal review: Canvas](https://github.com/w3ctag/design-reviews/issues/454


### Breakout 2C

#### [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400)

#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399)

Peter: no responses to the feedback Tess and I gave at Cupertino F2F.

Rossen: concerns about tight coupling between these two apis.

propose closing unsatisfied.

#### [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413)

Peter: again no feedback since comments left during Cupertino F2F.
... concerns about tight coupling to window placement api which has not yet come up for TAG review
... concerns about how this intersects with foldable screen work

Rossen: api seems to expose everything about screens despite that being listed as a non-goal.t

### Breakout 3A

#### [Web Components](https://github.com/w3ctag/design-reviews/issues/458)

No concerns with the PRs.

#### [Foldables CSS](https://github.com/w3ctag/design-reviews/issues/472)

Ken: Looks like there's active discussion in CSS on this

Tess: It's strange that you can expose the spanning information to iframes with feature policy but the iframe may not get the other information needed to reliably use that information (cross-origin iframes)

Tess and Ken both commented on the issue

#### [Scripting](https://github.com/w3ctag/design-reviews/issues/457)

No concerns with the PRs.

#### [Agent Clusters](https://github.com/w3ctag/design-reviews/issues/450)

No concerns with the PRs.

Tess: It's a bit easier to read this text now, yay!

### Breakout 3B

#### [Edit Context API](https://github.com/w3ctag/design-reviews/issues/416)
Alice: it will be great to have code examples of what's bad today and needs addressing. Ex. using hidden elements to capture input etc.

... Linking the examples in the explainer to the list of proposed API will vastly improve this proposal

... The WebIDL section should be moved to the very end

Example 1 - What's the HTML behind? What's the sate and how does it change? 

Alice: It looks like the focus() on EditContext is better described as activate() ? This is to say that when the containing element delegates 'focus' to the active editContext, it is essentially activating it rather than focusing.

... It would also be nice to see examples of how the API could be used to solve each of the problems listed in the ["Real world examples"](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/EditContext/explainer.md#real-world-examples-of-text-input-issues-in-top-sites-and-frameworks) section.

### Breakout 3C

Present: Peter, David, Sangwhan, (Yves)

#### [HTML Modules](https://github.com/w3ctag/design-reviews/issues/334)

David: HTML modules has been delayed until other module types ship, and was expected to be visited after this work is done.
Leaving HTML modules as stalled seems fine; doesn't seem to be activity right now.

#### [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405)

David reads [last comment](https://github.com/w3ctag/design-reviews/issues/405#issuecomment-578858875) which suggests we could close soon.

Peter still isn't happy about forbidding `@import`; it doesn't seem like there's anything here that can't exist with existing platform features like dynamic insertion of `@import` rules.

David filed [issue](https://github.com/w3c/csswg-drafts/issues/4821) on CSSOM.

#### [Curve25519](https://github.com/w3ctag/design-reviews/issues/466)

Discussed briefly and closed issue  

### Breakout 4A

Chat with Alison Jack and Jason Kiss

Alison:

- Working on structured content model

What goes out to agencies should be fully optimised for web standards

SEO built in
Accessibility built in
Analytics built in

Proof of concept shows having a central content repository that can push out to different CMSes.

Design system is in progress, but no subject matter expert (SME) involved as yet.

Something like a rates table - superannuation rates. 200 different examples, some work well and some don't.

Talking to agencies to see what barriers are.

Pushing for a design system, want to make sure everything is Accessible.

Victoria government in Australia, and UK, are further ahead with this type of work.

Australia.gov has a design system, and UK has a design system.

Many govt agencies that don't have useful resources, even large govt. departments don't have resources as they've outsourced.

Need more a11y experts.

Jason:

Web a11y has been cabinet mandated since 2003 in NZ

Still not a single website actually meets requirements, for lots of reasons

- Widespread lack of relevant skill in govt
- And within vendor community
- Majority of work is outsourced
- Can't even assess whether deliverables meet a11y requirements due to lack of skilled auditors in govt
- Latter situation is slowly improving
- No central govt authority
   - Can't centrally mandate a11y - nobody has authority
- Standards --> WCAG 2.1 AA and Web Usability Standard
- Practitioners want to do more, asking for help, guidance, support from management
- Executive level management, middle management lack awareness
- Very small team unable to provide support
- Going to draw on other govt's public resources

Tess: Need something like 18F in the US

Lee: We have a lot of trouble allocating small amounts of work like adding alt text, vs huge projects, as govt.

Allison: Web a11y is always the first thing deprioritised in shipping a build

Jason: Vendors make accessibility an upsell - charge more

Alice: in the a11y community we all know it's so cheap to do it if you do it up front

Jason: Increasingly including a11y as a contractual commitment

Rossen: Do you have any kind of auditing mechanism?

Jason: Not centrally.

... Can use an automated tool to get the low hanging fruit for very little cost

... Latest strategy for digital public service, it references web a11y standards a handful of times.

... Referring to "web accessibility standards"... it's in the strategy

... Accessibility charter... minister for accessibility issues. Piece of paper that obligates the signatories to make sure public information and services are accessible.

... Everyone has signed it, but no traction

Jason: Practitioners want to know more about a11y... quality is a11y

Agencies self assess against web standards

Each agency self-assessed 80 pages in 2018 manually - lot of work. Each page is ~2 weeks work. Learned a lot. They all wanted to do it again, even though it was painful, because it got a lot of funding out of management to address the newly visible issue.

... In 17, ran aXe across several viewport dimensions, plus several cheap and easy tests such as heading hierarchy, tab order, etc.

... Tests chosen for top issues in terms of frequency, tend to also have a high impact.

... Agencies learned how to do self-testing, how to remediate?

... Implementing a "micro-credential" - short course, gives you points towards degree. 6 week course. [Intro to digital accessibility](https://ped.wgtn.ac.nz/courses/1153-introduction-to-digital-accessibility-delivering-inclusive-digital-content).

... Syllabus very similar to [w3c course](https://www.w3.org/WAI/curricula/).

... Could look at developing more focused micro-credentials.

Rossen: Earlier talking about design system, components can you expand on what and how is this supposed to work and be audited?

Alison: Want to re-use content, stop creating same components over and over again

... Eligibility criteria, how much it costs, how to apply
... Travel agent site could host 

... Can collate info from various sources 

.. Want to break down sharing further

... Auditing will be handled by Jason

Alice: what does it mean for one of those components to be accessible?

Jason: It's content... semantic structure of the content

... Heading levels have to fit

Alison: also tables


Alice: You mentioned alt text a couple of times. How do you make sure it's included, it's correct.

Alison: it'll be a database of content, and it'll be mandated to use the content from the database

Jason: they would be chunks of structured HTML content, so the specific image, src, alt all hardcoded

Alice: Like web components; it includes the content and the element containing the content

Alison: yes

Alison: We're using schema.org for semantics, particularly voice

Alice: it's static content, by and large?

Alison: yes, though we are heading toward personalization / customization... will need to be able to tailor

Alice: [something about a future breakout topic on personalization]

Jason: we'll need to demonstrate the benefit to the other agencies to get uptake

Lee: current strategy going forward is that the public service needs to rebuild it's capability

Alice: more like the 18F model?

Jason: it's not the lack of a stick that's a problem, it's the missing capability in departments

Lee: it calls for empowering people to do this kind of work, instead of [...]

Alice: there's a bunch of common issues?

Jason: heading structure, tab order, alt text, keyboard functionality, color, etc.

... on average, we hit about a 65% pass rate. the accuracy of the assessments themselves were around 75% ... lack of knowledge

Alice: how can we make these things easier to get right? heading order and the outline algorithm. how do you fit some content in when you don't know what heading level it should use?

... focus, keyboard functionality, this is something i've been frustrated with for a long time

Alison: and we've just been talking about web, but we've moving to an omnichannel model. what about the apps they're delivering this content in, or other channels?

Alice: Could you give us issues you keep running into with keyboard functionality? focus-visible

Jason: yeah. legacy of css resets that set outline to none everywhere

... or interop issues, they've broken the focus in firefox but not chrome or safari

... lack of keyboard functionality can be because they roll their own stuff with just divs and spans

Alice: Why does that happen, do you think?  Why aren't they using buttons?

Jason: often folks don't know html, they just use frameworks and don't understand the underlying technology

Rossen: lots of damage being done by frameworks?

Jason: by default, they output div soup. you have to know what you're doing to get them to update accessible content

Rossen: the major frameworks i've worked with are usually doing pretty well in this space

Jason: anecdotally this has been my experience; frameworks may be playing a contributing role but it's not their fault

... how much of the frameworks doing this well is because of specific people

Alice: work done retroactively by heroes

Jason: yeah, and then they get tired and move on

Alice: these frameworks take you away from html and into the framework's abstraction, so you're removed from what the browser's doing and why

Jason: lots of developers don't get what role HTML plays in accessibility, in exposing your content to platform a11y tools

Alice: What are the frameworks providing that HTML is not?

Jason: scaling, smaller teams producing more quickly

Alice: I don't have a good understanding of how frameworks provide such scalability

Rossen: there are a lot of readily usable, prebuilt things, pull in an npm package and now drag and drop works, but you don't have to know how or if it's accessible

Rossen: to sum up, the aspirations here are great. we (at msft) work on a lot of different products. the thing that seems to help the most is to have an automated auditing system that each product can run their own content and scenarios against

... the hero model is maybe not achievable 

... automation is key. being able to capture your a11y principles into tools

... such auditing is very effective when mandated

... there are lots of such tools

Alice: doesn't everyone use aXe?

Jason: the 2017 self-assessment had them using aXe on 20 pages per dept

... we've had talks with our digital inclusion folks, may be able to work with them on an automated tool we can provide to the other agencies

... compliance mindset v. delivering on a11y mindset; need to make sure people understand a tool can only do so much

... it would help us communicate to management where current levels of compliance are now

Jason: the design system has stalled; alpha was full of a11y issues. the website hosting the design system itself wasn't accessible. we haven't worked on it in months; i'm worried we've lost momentum

Alison: a fully extensible design system would be fabulous

Rossen: what is the design system

Jason: styles, components, patterns, like gov.uk's

Alice: what technology are they in?

Jason: layer of abstraction on top of things like react, angular, silver stripe, whatever language you want

Alice: what do the templates look like?

Jason: dunno; it may be openly available

Alice: locates [a link to the design system](https://design-system-alpha.digital.govt.nz/components/Radios/)

Jason: easy to add new language, it's really great

... [Common Web Platform](https://www.cwp.govt.nz/)

...

Alison: the big three agencies haven't adopted CWP

Alice: sounds like the major challenges are: lack of enforced requirements in accessibility leading to a lack of expertise; widespread use of frameworks which abstract from the web platform without supporting the platform's built in a11y

Jason: yeah, also maybe vendor/contractual relationships. there's a handful of firms providing services to all the different agencies; no one ever says "hey, the contract required this to be accessible, why isn't it?"

Alice: what can we add to html, to js, etc. to add the right abstractions so people don't have to use these inaccessible frameworks

... if we were designing a new framework today, what abstractions would we want to have so this wouldn't happen? can we bake those abstractions into html instead?

Lee: some combinations of things in html are invariably inaccessible; can you show the developers warnings?

Jason: that's where the auditing tools come in

Lee: black text on black background is a bad idea

Tess: can address that in web inspector / dev tools

Alice: still on the tools side; what can we do in the language itself to help?

Alice: i want an api for the top layer (that fullscreen and dialog use) that has a concept of a modal

... whatever gives you the visual look has to give you the behavior

Alice: flex-order

Tess and Rossen apologize for their respective mistakes









### Breakout 4B

Present: Sangwhan, Yves

#### [WebRTC Priorities](https://github.com/w3ctag/design-reviews/issues/465)

Yves: I've commented on this, I think this should be hints. We should probably be firm on that.

#### [MiniApp URIs](https://w3c.github.io/miniapp/specs/uri/) [#478](https://github.com/w3ctag/design-reviews/issues/478)

Sangwhan: Made one drive-by comment on this, don't understand why it uses a custom scheme over a standard HTTP URL.

Yves: The rationale seems to be for offline loading, but that should be done by the cache..

Sangwhan: The meta-question is is this even part of the web?

Yves: Probably, the delivery is over the web after all.

Sangwhan: So what feedback should we leave?

Yves: Generally, it's not a good idea to invent a new URL scheme - there should be a [RFC](https://tools.ietf.org/html/rfc7320#section-2.1) about that. The question is why are they using a new scheme? What is the goal here? It seems like the rationale is to move it to a specific processor (e.g. like iTunes) - which is an antipattern. Curious if this is about package-to-package RPC or subresource addressability (which could be valid) or just as an entry point.

Sangwhan: Another issue I see is that they mention pre-installation, which effectively is a mechanism that can be used to break the trust chain. If a runtime from a malicious actor decides to pre-install a commonly used app with a backdoor, there is no way in the current system that allows to verify the provenance.

Yves: We should also note about [URI Templates](https://tools.ietf.org/html/rfc6570) and using content types for triggering rather than magic schemes.

#### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389)

Yves: Didn't like the constructor magically connecting. Should probably be a promise that can reject. Other issue is that there is no list of forbidden ports, that would prevent port scanning.

Sangwhan: Agreed, given the power of this feature it feels like gating it behind a promise (and in turn, permission) might be sensible.

### Breakout 4C

Present: David and Kenneth

#### [Display Locking](https://github.com/w3ctag/design-reviews/issues/311)

see comments in issue

#### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

see comments in issue

### Breakout 5A

#### [Serial](https://github.com/w3ctag/design-reviews/issues/431)

Sangwhan: I've provided feedback, but haven't heard back.

Kenneth: Let's change the status and wait until they get back with an update.

(meta discussion about origin hashing IDs of devices)

Kenneth: Looks like spec hasn't changed much.

(ping and wait)

#### [Native FS](https://github.com/w3ctag/design-reviews/issues/390)

Kenneth: They said something about design changes and what being implemented being slightly different from the spec, but have not heard back.

Sangwhan: Looks like that's still the case. Let's ping and wait.

#### [WebASM x ESM](https://github.com/w3ctag/design-reviews/issues/377)

Kenneth: Says it depends on top level await, which is pretty far in in terms of progress. They say attributes are nice but not required.

Sangwhan: I'm not quite sure, JS has more power than WebASM..

(commented concerns)

#### [WebRTC-SVC](https://github.com/w3ctag/design-reviews/issues/396)

Sangwhan: Pretty old, should do something about this. This feature is sort of like adaptive streaming for WebRTC.

Kenneth: The naming and mime types are interesting..

Sangwhan: Feature-wise, I think this is a necessary feature - one of the examples seems to only assign a data structure to a variable though - not sure what the intent of that is.

Kenneth: Also, are uppercases valid in the context of content-types?

Sangwhan: Looks like this particular case comes from RFC7741, but in RFC2045 it says it's handled as case insensitive so in practice (given conformant implementations) I don't think it matters, while it does look weird

(commented concerns)

### Breakout 5B

Present: Alice and Tess

Breakout scheduling for Wednesday

### Breakout 5C

#### Design Principles

David looked at https://github.com/w3ctag/design-principles/issues/126 a little and filed https://github.com/w3ctag/design-principles/issues/158 .

Rossen looked at naming issues, particularly https://github.com/w3ctag/design-principles/issues/108

### Readouts




#### Discussion about closing issues and leaving things to working groups

discussion that started from discussion of closing the [Custom State pseudo class](https://github.com/w3ctag/design-reviews/issues/428) issue in breakout 1B.  (And similarity to intrinsic-size.)

Unminuted discussion about the signal we send when we think we don't need to look at something closely because we trust the working group to handle it, and don't think there's any high-level coordination issues that require the TAG's involvement.  We want the signal to be clear that it's "follow the working group process" and not "good to ship". (Especially for early reviews) 

Importantly, we don't want to _discourage_ filing these types of issues, but rather close them with minimal effort on all parts.




David: quotes [comment](https://github.com/w3ctag/design-reviews/issues/466#issuecomment-593676485) from earlier today

Peter: should we add to design review template... seems it's there already.

Peter: People are listing community groups in that field when they really should be listing working groups.  People should have a proposed venue to move it beyond a community group.

Alice: File an issue on the processes repo to wordsmith something for the issue template, and assign it to plinss and rossen?



Readouts only got through 1c.
