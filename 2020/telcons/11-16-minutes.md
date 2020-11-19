## TAG Teleconference
##### 16-18 November 2020

---

### Agenda:

#### Breakout A (Europe / US)

* [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @dbaron, @torgo
* [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov
* [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron, @atanassov
* [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov
* [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

#### Breakout B (US / APAC)

* [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @dbaron, @plinss
* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @alice
* [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov

#### Breakout C (APAC / Europe)

* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris
* [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov
* [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

#### Plenary Session

* Breakout Rollup
* Potential "FYI" design review issue? [Unadjusted Pointer Lock Movement](https://github.com/slightlyoff/unadjusted_pointer_lock_explainer/blob/main/README.md)

* Issue Triage

-----


### Breakout A

Present: Kenneth, Peter, Rossen, Hadley, David

Regrets: Dan, Tess


#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @dbaron, @torgo

#### [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov

Reviewed progress, generally happy with the task force's response. Want to clear the advertising angle with Alice. Rossen will bring up at breakout B. 

#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron, @atanassov

#### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov

#### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

Reviewed updates to explainer and concerns from HTML folks. Rossen raised concerns about possibility of realms being used as communication channels.

Overall happy with approach.

### Breakout B

Present: Alice, Peter, Rossen, David, Issac

Regrets: Tess, Sangwhan


#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @dbaron, @plinss

Peter: Re-opened as they published a new version of their API.

... Last time we looked at this we pushed back, saying why not use a font picker. I don't see that taken on here...

David: Some of the folks who wanted this might have been design tools folks like Figma. Examples in the old explainer didn't really motivate it very clearly.

Peter: ... don't necessarily want just local fonts, but also web fonts.

Rossen: Won't this go against efforts around privacy and not allowing system fonts to be exposed? Two opposing forces working against each other.

... I remember discussions with the CSSWG in Fukuoka TPAC. There was a strong push-back on this one then. But I don't remember much else.

Peter: (quoting) ... haven't heard interest in a font picker implementation. People aren't asking about a privacy-preserving version.

Rossen: The explainer doesn't give the impression that privacy is top of mind.

Alice: Spec does talk about privacy options in the goals...

Peter: How useful is this API in the case where everyone gets the same small set of data?

Alice: Seems like the intention is that the "full" set will be given (only) in trusted contexts, with that being left up to the UA to determine.

Peter: I see lots of references to partners... it reads like it's designed for one application.

Rossen: Did we ask how this could benefit the rest of the web platform beyond the one (presumed) use case?

Peter: Looking over our comments, we previously closed the issue for lack of progress. There is a new version but I don't see anything that addresses our earlier feedback, and most of the issues we previously filed are still open.

... What feedback could we give that would be productive?

David: From Tess' comment, 6 issues are listed, 1 is closed, 4 still open, and 1 is a broken link.

Alice: Perhaps we could just ask for a summary of what's changed and why? And possibly for more clarity around intended use cases (beyond the "goals" and the tightly scoped "key scenarios" - what is the context for these goals and scenarios?)

Peter: I'll try and leave that feedback.


#### [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov

Alice: Left a comment.

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @alice

Deferred since Tess was unavailable.

### Breakout C

Present: Alice, Yves, Dan, Ken

Regrets: Sangwhan, Hadley

#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris

Dan: asked for current status - looks stalled - hopefully we get feedback by the plenary and close it off.

Ken: Sounds good to me.


#### [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov

[reviewed Alice's comment](https://github.com/w3ctag/design-reviews/issues/476#issuecomment-728652058)

Dan: Agree.

#### [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

Yves: there are new comments that seem to go in the right direction.

Ken: this sounds OK

Dan: OK enough to close the issue?

Ken: yeah I think so.

Dan: It's already set to proposed closed - let's close it in the plenary.

### Plenary Session

Present: Dan, Peter, Alice, Hadley, Sangwhan

Regrets: 

* Breakout Rollup

Dan: Breakout C we proposed to close virtual keyboard API show/hide...  Reading [new comment](https://github.com/w3ctag/design-reviews/issues/408#issuecomment-728994329)... looks like Ken needs to respond to Ian's response. 

.. [Personalization semantics](https://github.com/w3ctag/design-reviews/issues/476).

Hadley: Tess's original question on the ad ecosystem woudln't be supportive so who would developers bother to use it?

Alice: they didn't seem to really take that on board... 

Hadley: my conclusion - my thought - they are saying: if this is how users want to see content then presenting it in this way will lead to more users completing their tasks ... clicking on the ad ... rewarding the site host and the advertiser.  the only way that makes sense is if the advertiser uses the semantics...  The `distratctions` markup intends ...  you'd have to design your layout accordingly .. so your ads get included rather than excluded in user experience. Substantial difference to "iframe" hands off approach. 

Alice: if someone has a distracting ad on their web site it's distracting for everyone - which is a much bigger problem for someone with an attention propblem - but will be distracting for everyone.  So it would be nice if they could demonstrate what incentive to lead a website to use that attribute on an ad.

Hadley: use case of html newsletter... very basic layout of paragraphs of text.  Bold faced word at beginning of paragraph.  They have been putting adverts in text inline with the text.  Has been annoying distracting - requires cognitive effort to jump over.  Example of ads surviving reader mode.

Peter: they did make a point that sometimes content authors add things that are not ads but are distracting.

Alice: And that's what `prefers-reduced-motion` media query is for.

Peter: could be something that is not moving - e.g. paralax, funny scrolling effects... 

Alice: that's motion...

Dan: Yeah I kind of agree with Alice... anything that fits under the concept of distraction and isn't an ad fits under `prefers-reduced-motion`

Feels like we have a bit of a Rube Goldberg thing here, of nested distraction and not distraction tags.

Peter: pull quotes... done to draw your eye...  a screen reader wouldn't bother with pull quotes... There may be a use case for marking something as distracting.  

Alice: looking at [values]() they have ... messages - a chat bot - overlay - offer (ad) - sensory (movement or audio).

Hadley: we talked about auto-play not being on by default...  UA should be able to do that.

Alice: Agree. It seems like the kind of thing that UAs should be able to detect. If there's auto-play. If there's something that's animating.... a GIF... Only one of those that's difficult to detect is like the feed that moves under you when you're trying to read it...   Stock ticker... And what's going to consume this and how?

Hadley: couldn't find a good answer.  

Dan: any additional feedback we can leave?

Hadley: I think we've given the feedback we can...

Alice: ARIA: necessity being the mother of invention; but this is trying to generate an ecosystem.  For each subset of users (e.g. ADD users) what tooling might they be using and what subset of the vocab would those tools use?

Hadley: we could say : we look forward to seeing the full toolchain for each type of user- and then talk again.

Alice: I'll leave the comment and propose closing.  

* **virtual keyboard show/hide**

Sangwhan: I was OK with (closing) this...  I will write closing statement.

[closed]



[bumped to next week]

* Potential "FYI" design review issue? : Blink Process / TAG

  - [Unadjusted Pointer Lock Movement](https://github.com/slightlyoff/unadjusted_pointer_lock_explainer/blob/main/README.md)
 

Alice: How do we feel about stuff shipping in blink that hasn't gone through TAG review... Do we want a heads-up on spec changes in Blink that may be of interest but dont' need a review?

Hadley: e.g. things that are blink-specific ?

Alice: e.g. In the above issue - it's a change to the pointer lock behaviour - it's not cosmetic - but should it go through the review process?

Dan: if it has an impact on other things - an architectural or substantive change ...

Alice: they people (in Blink) making that call would be the API owners.

Sangwhan: I think they can make a reasonable judgement.  I don't think it should be mandated.  We're already pretty slow.

Hadley: it's a good point.   Wondering what we would do with this kind of a review.

Alice:  would it immediately go into the abyss?

Hadley: sure we could read through it and come back with suggestiions but does it help the web - progresing the big picture stuff we are here for?

Dan: Yes, there is a danger that we get caught up in too much of hte detail. Coming back to virtual keyboard show/hide, we highlighted an issue about how this isn't just about keyboards, and could be related to other specs. Doesn't that reinforce what Sangwhan was saying, that we shouldn't force the API owners in blink to make a review request for every little thing?

Alice: question becomes "what is the value to us"?   The API owners have a good idea of what is and isn't notable.  This example is right on the line.   Would there be value to us from an explainer coming in but with a non-blocking tag... helping us get visibility - and direction.

Hadley: I'd love a list curated for us...  

Peter: maybe as requesting review as non-blocking we could have an FYI category - just a heads-up.

Alice: if it's non-blocking it could stay open.  

Peter: up to us whether we want to review... 

Sangwhan: what would we do with that?

Dan: I think it would be taken care of in the triage process. We'd either label it an FYI or open a review. If they wanted an FYI and we close it, we aren't holding them back.

Alice: that would mean setting up an FYI label, the expectation 

Dan: Do we need a minimal explainer?

Alice: what would go in such an explainer? 

Hadley: if I'm working on something on the blink team and I know it has to go to the TAG, I'm incentivised to label it FYI since I won't have to do as much work...  that is dangerous.  

Alice: My expectation is that the API owners, not the API develoeprs, would be the one to make the call...  It does involve the risk of coupling our process to the blink process.  If someone puts an FYI on something that is actually quite large... the "owners" would look at the TAG thread and request a full review.

Alice: sounds like we're cautiously in favour of an fyi process - write a minimal explainer - tbd.  


* Issue Triage
