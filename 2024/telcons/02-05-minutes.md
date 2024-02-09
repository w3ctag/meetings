# TAG Breakouts - Week of 5 February 2024

## Agenda

### Breakout A (Europe / China) - [2024-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [Feature detection for supported clipboard formats](https://github.com/w3ctag/design-reviews/issues/901) - @LeaVerou, @torgo, @rhiaro

### Breakout B (California / Europe)  - [2024-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791) - @LeaVerou, @plinss
* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo
* [`field-sizing` CSS property](https://github.com/w3ctag/design-reviews/issues/890) - @LeaVerou, @rhiaro

### Breakout C (California / Australia) - [2024-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @hadleybeeman, @plinss
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### Breakout D (California / Australia) - [2024-02-06](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Open Design Principles PRs?
* Review additional reviews [pending external feedback](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+pending+external+feedback%22) to see if feedback has come in?

### Breakout E (Europe / China) - [2024-02-07](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman
* [TAG spec review of Storage Access Heuristics](https://github.com/w3ctag/design-reviews/issues/919) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2024-02-07](https://www.timeanddate.com/worldclock/converter.html?iso=20240207T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Minutes

### Breakout A (Europe / China) - [2024-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Matthew, Amy

#### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Amy: we talked about closing this unreviewed at the [f2f discussion](https://github.com/w3ctag/meetings/blob/gh-pages/2024/01-london/minutes.md#review-request-for-protected-audience)

Matthew: we talked about what the impact of closing vs not closing would be. Is it worth trying to communication with that team? Also wanted to ask - is one of the objections to the api the registration? Not sure if they've changed that. That's a big aspect of it.

Dan: attestation and enrollment

Amy: yes that's good to raise .. they've got that on several of their privacy sandbox things now.

Dan: I'd like to separate that from the APIs themselves... suggested a separate review for the enrollement attestation thing. We could start a discussion, or a finding on this? Should it be a design principle?

Dan: I think we should start a design principle...

Amy: I might already be captured by design or ew principles on centralization or others... 

Yves: [RFC9518](https://datatracker.ietf.org/doc/rfc9518/)

Amy: should we prioritise moving the review along for the privacy sandbox requests instead?  
Amy: they replied to our questions from the f2f -- they wrote "We believe that facilitating remarketing and custom audience advertising post third-party cookie deprecation maintains critical web site revenue and is thus fundamental to the functioning of the web and justifies adding the Protected Audience API to the web".  I disagree with the statemennt that you need targeted advertising in order for the web to exist.

Matthew: I respect that position - originally the CMA said "this isn't a good way to do it" because centralizes the stack with google only. So they advocated a proposal... since that they closed their investigation - but they [CMA] are monitoring ... But is there a third way? An option between "not having any revenue" and "it all going through one organization"... If you do accept that advertising is part of the web - isn't there another way - creation of a market... 

Dan: but is targeting necessary? Contextual... etc... 

Dan: even if you agree that advertising is necessary, does that imply that user tracking and remarketing are all part of that?  e.g. blog post https://blog.sentry.io/we-removed-advertising-cookies-heres-what-happened/ that talks about alternative approaches to ads and marketing.

Amy: +1

Dan: we've heard about companies experiences with reomving 3p cookies and not having the same tools available to them, but they've bene able to work around them by using other techniques - not targeting but contextual

Yves: I think Robin posted something around those lines. When they say functionality of the web requires 3p cookies or advertising... it's not true, it's not part of the architecture of the web. It's a business model for many companies around the world. That's fine, but it doesn't mean the architecture of the web has to be bent towards that use case only

Amy: +1

Matthew: we've got several different places on the spectrum.. the intereting thing is where are the competing proposals that are at these different places on the spectrum? Why is there only one? There was another company wanting a market... and we've talked about different approaches.. I wonder where they're being discussed. It's not our remit to come up with alternatives. Be interesting to see serious discussion of them going on.

Amy: some in PATCG. Also not all of them need new apis or changes to web arch. Be good to discuss with Martin.

*bumped to plenary*

#### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman


Yves: there is support from Wordpress for the functionality... same for payments... part of the ongoing attempts to poke holes into iframes isolation...

*also bumped to plenary*

#### [Feature detection for supported clipboard formats](https://github.com/w3ctag/design-reviews/issues/901) - @LeaVerou, @torgo, @rhiaro

*we take this to breakout b*

### Breakout B (California / Europe)  - [2024-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Matthew, Peter, Amy, Yves, 

Regrets: Hadley, Dan, Lea

#### [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791) - @LeaVerou, @plinss

Yves: should close

Peter: agree. As good as it's going to get. Would like to have Lea sign off.

Yves: Lea's latest comment was to ask if they have remaining issues. I'd say we've done our job, they can file new issues. We can invite them to file additional issues as appropriate.

Peter: there's a CSS f2f, so expect remaining issues to be resolved soon. Good to close.

Lea: happy about how this went

<blockquote>
We're closing this review as satisfied, glad to see the major issues resolved. If the CSSWG needs feedback about any of the remaining issues please file new requests.
</blockquote>

**closed**

#### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo

Matthew: mentioned in the feedback from them is the tradeoff between making IWAs deep linkable... something related to miniapps having solved this?

#### [`field-sizing` CSS property](https://github.com/w3ctag/design-reviews/issues/890) - @LeaVerou, @rhiaro

Matthew: [Considered alternatives](https://github.com/tkent-google/explainers/blob/main/form-sizing.md#considered-alternatives) were added to the Explainer, as requested.

Amy: proposed closed in December, will just check with Lea

Lea: we discussed this... adding new keywords.. won't be able to apply other keywords to a form control. Fair enough, I'm convinced.

**closed**

#### [Feature detection for supported clipboard formats](https://github.com/w3ctag/design-reviews/issues/901) - @LeaVerou, @torgo, @rhiaro

Amy: looks like we can close this. Possibly with concerns. Lea thumbsed up this idea in slack. I can draft a closing comment and run it by Lea.

Matthew: +1

**closed**

### Breakout C (California / Australia) - [2024-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Tess, Martin

Regrets: Hadley

#### [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @hadleybeeman, @plinss

The below was filed as [`w3c/editing#459`](https://github.com/w3c/editing/issues/459):

@plinss, @hober, and I discussed the feature.  This seems fairly reasonable on the surface, but https://github.com/w3c/editing/issues/439 is particularly concerning.

It seems like there is an inherent privacy issue here in that the target application reveals something about itself when pasted into.  The suggestions that have been made in the issue, which involve resolving the clipboard items on a timer, would seem to undermine the key advantage of the deferral and do not provide protection within the timer.

The key thing to realize is that the clipboard is a communication medium between the copied content and the application that receives a paste.  This is unavoidable given our current model where a website can put whatever it pleases on the clipboard (with the only condition being that they receive an interaction of some sort).  That communication is currently one-way and websites don't necessarily get to know about the destination or control it.  That makes the channel less effective as a means of learning things about people.  The delayed rendering creates a potential bidirectional channel, with the destination choosing from a multiple choice selection.  The site learns what choice is made.  The choice itself carries novel private information.  The timing of the paste is also revealed.

There are other approaches:

1. Render all formats when paste occurs.  This still reveals timing, but would not reveal the choice of format.
    1. A variant of this would be to generate the requested format and a randomized subset of the other formats (differential privacy)
2. At copy time, produce a single format from which all others can be produced.  Let the destination application perform format translation.
    1. As an option, if the single format is not supported at the destination, sites could provide a worklet that can perform translation into different formats.  This worklet would be denied access to any communication, so the source site would not have any means of learning the choice of format.
3. Finally, we could define a new media type that carries a URL.  That URL, when resolved, provides the destination application with information in whatever form it desires.

#### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

https://drafts.csswg.org/css-color-hdr/ !

Tess: There's a `PredefinedColorSpace` WebIDL enum [defined in HTML](https://html.spec.whatwg.org/multipage/canvas.html#predefinedcolorspace). CSS Color Level 4 defines `<predefined-rgb>` as [a different list](https://drafts.csswg.org/css-color-4/#typedef-predefined-rgb), and [Level 5 adds more](https://drafts.csswg.org/css-color-hdr/#predefined-HDR). We should really have one WebIDL enum that gets pulled in by reference everywhere, so we ensure we don't have regretable collisions later on. That is, there should be one source of truth for the names of color spaces in web specs.

### Breakout D (California / Australia) - [2024-02-06](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Martin, Peter, Tess, Lea 

#### Open Design Principles PRs?

#### Review additional reviews [pending external feedback](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+pending+external+feedback%22) to see if feedback has come in?

### Breakout E (Europe / China) - [2024-02-07](https://www.timeanddate.com/worldclock/converter.html?iso=20240205T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Matthew, Max, Yves

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

*dan chases contact at google*

#### [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman

*need amy or hadley*

#### [TAG spec review of Storage Access Heuristics](https://github.com/w3ctag/design-reviews/issues/919) - @torgo, @rhiaro, @hadleybeeman

Dan: proposes close.  *polls TAG out of band*

Martin: (out of band): +1

Matthew: the changes in the explainer look good. In user signals & preferences section it talks about how Firefox does it. so they have listened to the feedback.

*We held additional discussions in chat and agreed to close this with a positive review, emphasizing the continued need for cross-browser engagement and consensus.*

#### Triaging

##### [device orientation](https://github.com/w3ctag/design-reviews/issues/928)

Matthew: this is interesting... started in 2011... in 2016 it had a CR but then retired... and now has come back in 2019... since 2022 has had loads of work... Seems pretty well fleshed out. APA had some accessibility consideraitons... these can be worked out...



### Plenary Session - [2024-02-07](https://www.timeanddate.com/worldclock/converter.html?iso=20240207T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tess, Matthew, Yves, Martin, Amy, Peter, Lea (last bit)
Regrets: Max, Hadley

#### Breakout Rollup

Dan: talked about protected audience... including the attestation / registration, and how that's problematic. But that's separate from the api itself. Consensus is the attestation part is not a good idea, centralisation. Yves brought up RFC 9518 - could we refer to this? Something to discuss. On protected audience... they gave us feedback... 

Amy: I disagree with that

Martin: so do I

Dan: there's a lot of debate... what should we do with this review?

Martin: it's a difficult question to ask what to trade for remarketing and custom audience construction. The privacy properties of the api as described are not good enough. There are a lot of holes. It's a bad trade.

Matthew: Understand that this has been going on for a long time and want to resolve it. Would waiting until we see who is appointed, in case there's an opportunity to bridge with this team? Also, are there any remotely credible alternatives being discussed? There's a whole spectrum and this is just one point... anything we can point to and say why don't you do it more like this?

Martin: I'm not aware of anything in this space that competes with it. Most of the other alternative approaches to this particular problem have been subsumed into protected audience. There's been a long number of debates over time in the web advertising business group and other areas, where people did come up with alternative proposals. This rolled a lot ofthe best attributes of those proposals into one thing, getting bigger and bigger. I don't think we need to fall foul of 'we need to do something, this is something, so we do this'

Dan: can we provide feedback on the specific privacy holes? Is there a point in us doing that?

Martin: it's difficult.. the proposers imperative to do something like this is very strong. I don't think engaging on minutuae is something the TAG should be doing unless that would be impactful. The sort of feedback we should be concentrating on is the high level stuff, is this good for the web? That's the question in front of us. If we start picking at the details without addressing the big question I don't think we're doing a service

Amy: +1

Dan: we have talked about things like topics.. there are other things that are being put out there that are advertising related that may not be addressing the exact cases we're talking about here, but could be things where in our feedback we can point to those so they don't assume we're compeltely anti advertising...

Amy: i'm not sure that we do need to preempt accusations that we're anti advertising

Peter: I'm not against advertising.. against targeted advertising because I don't see a way it can be done without harm. We've taken that stance before, prove you're doing it without harm. It's a high bar, and if you fail to meet that bar our answer is going to be no. If it's in chrome and not in other browsers that's a differentiator

Martin: we've got to engage with what it is

Peter: privacy sandbox is less harm than we have now... but it's not good enough to bake it into the platform

Tess: also ... it's (privacy sandbox) is not better -- it's better than what is currently in chrome but not better than what is in other browsers... I sicnerely see them as trying to move the needle in a positive direction but it's a regression compared to other implementations... because of that maybe people are holding it to a different kind of bar?

Dan: they've said it's essential for the web... but these other browsers are already disallowing the technology that enables that..

Tess: we've said that..

Peter: yeah it's harm reduction and we don't discourage harm reduction. 3p cookies and what chrome has now isn't a feature, it's a bug. It wasn't designed into the platform to begin with. if we were changing a platform feature into a less harmful feature, I'd be behind that. But takng a security hole and turning it into a platform feature is not something we want. It's not the same as other situations with incremental improvements and harm reduction.

Dan: how can we roll this into feedback and close the issue? 

Martin: many facets... need to think about it.



#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

