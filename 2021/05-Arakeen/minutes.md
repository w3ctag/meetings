# TAG Virtual F2F - Arakeen

## Week-of 10 May, 2021 

This W3C Technical Architecture Group virtual face-to-face meeting was held as a series of 18 breakouts over the course of the week of 10 May, 2021. The mintues are presented as breakout notes and are not chronological.  There are some additional "rollup" notes presented at the bottom of the document where some of the sessions are futher summarized. In these rollup sessions, there is often further discussion and issues are sometimes closed.

## Breakout Track A

### Session 1

Present: Rossen, Tess

#### [ARIA in HTML review](https://github.com/w3ctag/design-reviews/issues/614)

Rossen: Here's the link to set of changes we should focus on https://github.com/w3c/html-aria/issues?q=is%3Apull+closed%3A%3E2018-11-01

... Rossen and Tess looked through many PRs and found nothing problematic. Rossen left a [closing comment](https://github.com/w3ctag/design-reviews/issues/614#issuecomment-837491905) and resolved the review.

Ran out of time before getting to any of our other issues; moved them to 2A.

### Session 2

Present: Rossen, Tess

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509)

Rossen: This is pending external feedback, since October 2020. Let's mark it as stalled.

Tess: WFM

#### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117)

Rossen: This one just needs a PR written, and Lea took the action to write it, so there's nothing for us to do on this one right now

Tess: OK

#### [Early Design Review: document.prerendering](https://github.com/w3ctag/design-reviews/issues/613)

Rossen and Tess went spelunking in [the explainer](https://github.com/jeremyroman/alternate-loading-modes/blob/main/prerendering-state.md) and [several](https://docs.google.com/document/d/1Xzw0k8DgltI2ohapuDKmjRZLv7NVrRFGusW8IBtiCT0/edit) [other](https://github.com/jeremyroman/alternate-loading-modes/blob/main/browsing-context.md) documents it links to. This feature is very hard to evaluate on its own given that it depends on a bunch of other stuff that we've not seen before / that hasn't landed in the platform or been brought to us for review.

Tess [left a comment](https://github.com/w3ctag/design-reviews/issues/613#issuecomment-837532516) & marked it as `propose close`.

#### [Back/Forward Cache](https://github.com/w3ctag/design-reviews/issues/628)

Tess looked at this. This broadly consists of three things:

1. tighten up the existing specification of the bfcache to try to get implemnentations to converge & to make it easier to write WPT tests for it
1. fix places in specs that don't correctly take bfcache into account (e.g. things that just check for visibility)
1. update the design principles and the sec & priv questionnaire to give spec authors guidance

Overall it seems like they've done a really good job finding the things that need doing and they're tackling them.

Tess [left a comment](https://github.com/w3ctag/design-reviews/issues/628#issuecomment-837570345).

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)
  Rossen: Did another read through the issue and linked documents. The state of `focus` in HTML is still incomplete. As originally pointed out by Alice, we should continue/complete this review once the linked work matures. 

#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

Ran out of time before we got to this.

### Session 3

Present: Lea, Ken

#### [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587)

Looks stalled, posted to ping them.

#### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621)

They need to explain more about why CPU utilization and clock speed are both needed. Would it be better to have a higher level "CPU load" factor? More complexity could be available, but shouldn't be mandatory.

### Session 4

Present: Ken, Lea, Sangwhan, Amy

#### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512)

Ken: [leaving comment] depending on @hober

#### [Web Neural Networks API](https://github.com/w3ctag/design-reviews/issues/570)

Sangwhan: raised issues, not satisfied, don't know how to deal with this

Ken: make sense to summarise in the issue?

Sangwhan: API is not great

Ken: support from MS and google?

Sangwhan: MS and intel pushing it. Parts I did not like... see [issue 89](https://github.com/webmachinelearning/webnn/issues/89), [139](https://github.com/webmachinelearning/webnn/issues/139) is my main gripe

Ken: can live with low level API, but want to make sure it's futureproof

Sangwhan: also annoyed about [138](https://github.com/webmachinelearning/webnn/issues/138). Need background knowledge. Bits that are extremely tied to specific hardware accelerated NN features. Gated Recurrant Unit.. used to remove background noise in video conferencing. LSTN is more common but not supported.. hardware acceleration for GRU, found it strange

Ken: some of the use cases driving this.....

Sangwhan: weird restrictions for GRU, weird inconsistency in the API

Ken: sounds like a good comment

Sangwhan: I've been saying this, they say it's because of hardware. 

Ken: how does the hardware look in five years?

Sanghwan: Exactly. 

Ken: what hardware? Intel, Apple? Might differ.

Sangwhan: I suggested.. if there's hardware that doesn't support it I suggested it should throw, they said no.. suggested canPlay type mechanism to probe if you can do it... they said no. 
... Invite these people to a call? Issues are difficult because you need a lot of background to get started.
... Push to plenary.. see if chairs can help.

#### [Web Codecs](https://github.com/w3ctag/design-reviews/issues/612)

Ken: discussion around timestamps. Not really timestamps.. offset inside the stream. Also depends on playback speed. Normally playback correlatest o timestamp but you might be able to change playback..

Sangwhan: a timer that starts at beginning of stream?

Ken: they want to use unsigned microseconds but depends on playback speed. A lot of issues. Makes sense to me to use unsigned microseconds. Can add timestamp if there's really a need.

Sangwhan: also asking about window environments, detach codec inputs..

Ken: only on worklets or workers initially.. a lot of people who want it on window as well.

Sangwhan: on window not harmful unless there's an implementation detail..

Ken: wanted it not to be a blocking api..

Sangwhan: don't necessarily always want a worker, more involved

Ken: if no-one sets up a worker you end up with crappy web experiences

Sangwhan: going to block the main thread.. very heavy stuff.. people won't do that

Ken: if it's heavy it should always be in a worker

Sangwhan: image decoder part.. 

Ken: can we expoes that to the main thread?

Sangwhan: use cases like short video transfer you can block for a little bit while you're encoding it.. makes sense on window. 

Ken: makes sense to start on workers, then if you have those use cases add it to window. You can always add it to window. If you add it now you cannot remove it again. Gradually build API. Makes a lot of sense. [leaves comment]

Sangwhan: by having it worker only, using it in webrtc is going to be a pain.

Ken: those people work on webrtc

Sangwhan: on worker only, someone will polyfill for window. When there's enough usage on window, say it's time to expose it to window.

Sangwhan: PR for image encoder/decoder API.. we haven't had that.. it's a common thing people want to do. 

Ken: PR is pretty big. Metadata as well?

Sangwhan: seems like no api for that... [reads stuff] ... [discussion] ... [drafts comment]




#### [Managed Device](https://github.com/w3ctag/design-reviews/issues/606)

Amy: they've not responded to torgo's last comment, or addressed all of nightpool's points (but did address some, updated security and privacy)

Sangwhan: part of me thinks should not be on the web, part of me thinks it should...?

Amy: introducing friction to surveillence is not necessarily a bad thing (imo)
.. I'd like to go through this in detail again and leave a nudge comment

Sangwhan: we should have group consensus about whether it should be part of the web or not, potentially close it off. It's contentious.

Amy: worth opening a specific issue in their repo about asking for documenting abuse cases?

Sangwhan: yep

### Session 5

Present: Lea, Tess

#### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624)

TODO: Lea leaves comment after breakout (Done)

@hober and I discussed this in a breakout today during our VF2F.
We think that the improvement this feature offers over the existing JS library appears to be very incremental, so it appears that the benefit of adding this feature to the Web Platform does not outweigh the additional complexity, and the cost of breaking one of the fundamental assumptions of CSS.

#### [CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584)

Issue fixed, review closed!

#### [CanvasRenderingContext2D API Improvements](https://github.com/w3ctag/design-reviews/issues/627)

Notes:
- CSSColorValue is intended to represent CSS syntax in Typed OM, not as a general purpose Color object for the Web Platform. It would require substantial changes to be used in that way. However, there are plans to eventually define a `Color` object that other APIs can use as input.
- Filter syntax is less expressive than SVG 
- We were concerned about `ctx.reset()` but we see that it's being discussed productively.
- Clear [feedback](https://github.com/whatwg/html/issues/5620) from implementors that perspective transforms are not implementable 
- camelCase font properties are not consistent or predictable. Might be better to instead expose an API that accepts the actual CSS property as a string. Also, why expose `font-variant-caps` but none of the other `font-variant-*` properties, or even `font-variant`  itself?

TODO: Lea works on finishing draft comment and posting it after the breakout (Done)

Draft comment:

Hi @mysteryDate & @fserb!

@hober and I took a look at this during a breakout this week.

Overall, we're happy to see that each of these additions is being discussed in [various WHATWG HTML issues](https://github.com/whatwg/html/issues/5613) where you've gotten a lot of feedback from other stakeholders. For instance, the ongoing discussion on [the reset function](https://github.com/whatwg/html/issues/5618) has been fruitful and we look forward to seeing what conclusion everyone comes to.

Regarding [using CSSColorValue for input](https://github.com/whatwg/html/issues/5616), and as @plinss [already expressed](https://github.com/w3c/css-houdini-drafts/issues/1014#issuecomment-837168505) in the Houdini TF discussion on this, we don't think `CSSColorValue`, as currently specified, is an appropriate object to use here. CSSColorValue is intended to represent CSS syntax in Typed OM, not as a general purpose Color object for the Web Platform. It would require substantial changes to be used in that way. However, there are plans to eventually define a `Color` object that other APIs can use as input.

On the proposed [CSS Text Modifiers](https://github.com/whatwg/html/issues/5617), we're concerned about the choice to use camelCased names instead of the actual CSS property names. The names currently proposed are not just camelCased versions of their CSS counterparts (e.g. `textLetterSpacing` instead of `letterSpacing`) , but even if they were, there is both mental and coding overhead to converting, compared to being able to use the CSS property verbatim. It might be better to instead expose an API that accepts CSS property names if you are looking to expand the set of CSS properties that you support. The set of properties proposed is also a little unexpected, for example `font-variant-caps` is exposed but none of the other `font-variant-*` properties, or even `font-variant` itself.

You've gotten strong implementer feedback that [perspective transforms](https://github.com/whatwg/html/issues/5620) aren't feasible in at least one implementation. Perhaps it's best to leave this for the future, in case that stops being the case later on.

The syntax proposed for SVG filters is strictly less powerful than SVG filters, [as pointed out previously by @smfr](https://lists.webkit.org/pipermail/webkit-dev/2021-May/031850.html). Adding APIs that are very similar to other APIs but different in subtle ways is likely to be confusing to authors.

We did not see any issues with any of the other proposed additions.

#### [Early design review of light-DOM CSS Scope proposal](https://github.com/w3ctag/design-reviews/issues/593)

This is still pending external feedback.

#### [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299)

Ran out of time. Tess will try to incorporate Lea's PR feedback.

### Session 6

Present: Tess, Peter, Rossen, Amy, Dan, Hadley

#### [WebID](https://github.com/w3ctag/design-reviews/issues/622)

Amy: bundling identity with credentials

Hadley: talking a lot about the problem but I'm missing the user need.

Amy: I get an idea that it's about 3rd party cookies going away so it's about federated login...

Hadley: it would be nice to have it spelled out.

Dan: what breaks without 3rd party cookies?

Peter: SAML doesn't require 3rd party cookies but the logout is fragile - and some solutions people have come up with iframes... fragile.   Flourishes and add-ons e.g. embedding your github identity into dev.to so it skips that step - that requires a 3rd party cookie.

Dan: But maybe I don't want Dev.to to know what my github ID is...?

Peter: once you've logged into github via dev.to then they can cache the information but until you've done that login why do they have access to that information? Fundamentals of these systems aren't broken, other aspects.. single logout issue is more complicated but there are other solutions. They're driving towards something where federated identity is moderated through the UA, and I'd like to see something like that. 

Dan: that could allow your UA to display.. you go to dev.to, your UA says this thing accepts 'WebID' based logins from github would you like to use your github identity? If I select no dev.to is none the wiser. If I select yes then there's an interaction.

Peter: I don'nt want to stop the work, the goal is a good goal. Not sure if all of this is justified

Hadley: agree with both. I like anonymity on the web. But aware that if I'm on a reputable site that I don't go to often and it gives me the usual 'would you liked to log in with facebook etc' I'll make a new account. If It said 'hi Hadley would you like to log in with your google account' I'm more likely to continue. A UX flow thing. If you have an interest in keeping people using your ecosystem I can understand that you'd wantthis

Peter: dark pattern

Dan: having it mediated by the UA could make it less of a dark pattern

Hadley: definitely

Dan: I don't know if we can say federated login is a dark pattern

["Federated Dark", the new film from Christopher Nolan]

Peter: the dark pattern is enticing you to bind your identity on this site to your facebook/google/etc

Tess: distinctions between federated login providers where the purpose is to join your identity across sites, vs other login providers whose goal is not to do so. One problem with status quo is that user agent cannot distinguish between the two. The threat of signing in with facebook is real. If there was an equivalent sign in with Tor kind of thing where you knew they won't join identity across site... if the user is concerned about the kind of identity joining, how do you tell the difference? The mediated variants are trying to address that, where the federated login provider can't reuse the same thing across sites because the browser introduces some kind of complexity to it. There are existing federated identity providers that try to mitigate this today. How does the browser know that they're doing that well? without being involved in the process. If you involve the browser in the process of doing the differentiation between the identities then the browser knows the identity.. 

Hadley: people want fewer usernames and passwords to remember..

Tess: status quo is signing in with email addresses, most logins are not federated identity. That's extremely joinable. People do that all the time. I don't want us to conclue that a private web doesn't support federated identity at all, we'll be back at square one.

Dan: are the privacy considerations around websites participating in the federation not knowing that the user is part of a particular identity ring until the user gives their consent through the UA part of the proposal?

Tess: looking....

Hadley: [leaving comment about user need]

Tess: yes.. [identify the problems here](https://wicg.github.io/WebID/README.html#the-end-state) but doesn't say the identity provider shouldn't be able to do that... IDP shouldn't be involved without justification.. doesn't say they aren't join your identity across sites. Is in [threat model](https://github.com/WICG/WebID/blob/main/privacy_threat_model.md#identity-provider-collecting-information)

Peter: Mozilla did work on Persona... 

Rossen: is cited in their prior art section. About BrowserID proposed, and link to post mortem

Tess: threat model bit does talk about this

Rossen: do we have enough to write a comment?

Dan: feels like we should organise a separate session with Sam about this. Initial comments.. and schedule a separate breakout.

#### [App History](https://github.com/w3ctag/design-reviews/issues/605)

[naming is hard]

Hadley: something about how all the javascript options change how your back button works

Dan: there is already a history API, we can't call this history API but it provides additional functionality, why isn't this just a revision..? There's a mechanism in place for creating new versions of APIs.

Tess: part of explainer that talks about integration with existing history API

Rossen: is the scope the same?

Dan: if it's not is the history api currently being worked on? Developers trying to wrap their heads around the different APIs... not the history API, the *App* History API... this is a problem.. we keep adding new things without reivsing the existing things

Tess: sympathetic to this in general. In the case of fetch, we couldn't just remove XHR. XHR is a mess.. what we did was designed a new model that unified sub resource fetching and came up with a clean api and it was worth the redundancy, and we have to live with that forever because of compat. Does the same reasoning apply here? We can't remove the old history api..

Dan: I don't think so, the old history api does something different.. they both manipulate history

Tess: in the spec it says it's layered on top of existing history api

Peter: says the existing *concepts*, not the API.. not inventing new notions of what history is

Tess: in that case it sounds like XHR and fetch. There's a legacy API and a modern API built on the same underlying model. In XHR and fetch from a developer standpoint it's easy to know which to use... the existing one has a really obvious name which is exactly what you want, whereas in the case of XHR it was this bizarre thing

Dan: this is flipped.. history is the thing we want it to be named, app history is confusing

Tess: right, what do apps have to do with it. Do we have another example of doing this in a good way? 

Dan: my primary concern is developer confusion. has something to do with naming, but also the proliferation of new APIs.

Tess: reassuring to see they didn't add an incompatible mechanism. Sits on top of current model. Agree it's worrisome that in a world where these two APIs exist the one we want people to use is the weird named one and the one we don't want people to use is the obvious named one.

Peter: options are extend existing history model or break existing code... if they're different enough, extending existing history doesn't make sense. Could be a sub object. `history.altview` or whatever.. 

Rossen: prior art to similar patterns, pointerevents and touch events came to mind and how one took over the other over time. Similar naming and concepts, one being a lot more extensible, future proofed than the other, shipping later, consuming the other. In that case we went with completely different api naming rather than trying to reuse touch events.

Dan: we have given comments, at least one is addressed and merged. Got some framework authors to comment. More value we can provide? Should we say we think there's an issue with the name, appreciate the work, no additional feedback? 

Peter: very happy to see an effort to make a better history API. 

Rossen: design intended to be a lot more pleasant. We can't overhaul history in its existing state. We'll see what they come back with in terms of bikeshedding.


`We're happy to see this effort happening.  Thanks for listening to our feedback.  Adding additional complexity to the web platform remains a problem.  We're concerned about adding a new API that has to do with history which developers will find confusing on top of the existing history API. At the same time it's clear that it's meeting a user need. The example of XHR and Fetch came up in our discussion.  In that case, it was clear what we were asking developers to do - migrate to Fetch.  Can we do the same with this API?  So we'd like to better understand how this can be added to the web platform whilst also mitigating against the complexity issue. However we're generally happy to see this go forward.`

Dan: it's more than the name. Are we telling developers don't use the history API, use this new thing, or history for one set of things and new history api for other set of things

### Session 7

Present: Rossen, Sangwhan

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416)

Sangwhan: Doesn't look like there has been much progress.

Rossen: Let's leave a comment that we will punt this until they update us.

#### [Pen Events API](https://github.com/w3ctag/design-reviews/issues/553)

Rossen: It looks like they got back to us instead of their repro. The last comment attempts to address all previous questions at the same time. 
  ... First concern was about aligning the button click with mouse click events which have down/up capability. The answer was that this is a limitation of the current hardware.
  ... From reading the explainer it seems that this might be related to piping the up/down events through pointer events?

Sangwhan: If this is the case I'm not sure why this isn't just using the pointer events instead?
  
Rossen: This is a valid point and we should just ask for further explanations.

Sangwhan: The next part about the connect behavior, the response looks very specific to the Windows platform. I'm not sure the behavior of the Windows Shell makes sense to be exposed to the web.

#### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591)

Proposed comment:

`During our May 2021 vf2f, @cynthia and myself did another pass at this review, thank you for all of the answers. Regarding adding a direction hint to the recognizer - we found that to be a useful futureproofing feature and recommend that you do. After going over the privacy & security questionnaire I am still not clear if the API exposes additional fingerprinting capabilities. With exposure of strokes, ordering of strokes and timing of strokes, I worry that models can be trained to easily recognize patterns for various disabilities. This will be a very unfortunate byproduct of this API. Is this something that you considered and could expand on?`

#### [PWAs as URL Handlers](https://github.com/w3ctag/design-reviews/issues/552)


### Session 8

Present: Rossen, Tess

#### [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579)

We talked a bunch (and failed to minute) about why `overflow-clip-margin` doesn't apply to `overflow:hidden` or even `overflow:visible`. Tess captured the conversation in [a comment on the issue](https://github.com/w3ctag/design-reviews/issues/579#issuecomment-839322127).

#### [SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595)

Marked this as `blocked on dependency` (waiting on [#342 First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342)).

#### [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538)

This has been marked `propose close` since October. Let's try to close it in the rollups.

#### [Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611)

Ran out of time.

### Session 9

Present: Amy, Dan, Hadley

CAPCHAs topic - it's horrible - not 

Dan: Peter may have additional info...


#### [Linked Data Signature Working Group Charter Proposal](https://lists.w3.org/Archives/Public/semantic-web/2021May/0001.html)

Hadley: different issues floating around... no technical definition for Linked Data.  They're focusing on RDF serialized to json-ld.  Also the concern of environmental impact of blockchain technologies.  "proof of work" is in the charter?

Amy: It's in the explainer, not the charter.

Dan: do we need to have a finding about "the web should not depend on the 'block chain' while there continues to be environmental impact"?

Hadley: another argument : it biases power to those with lots of computing power.

Amy: which also has an environmental impact.

Hadley: and disadvantages marginalised 

Amy: no dependncy on "proof of work" - only given as an example of "digital proofs".  Not a hardcore blockchain dependency.  Not a proof of work dependency.  Some orgs are using permissioned ledger - not distributed ledgers.  

Amy: they responded in a thread on the semantic web mailing list... they changed a bunch of wording in the charter in response to Dan Brickley's concerns.  Back to RDF - the charter does mention RDF (which was the other potential issue) - it's not hidden.  

Hadley: context files in JSON-LD - 1.1 - you have a graph of data - and metadata in a context file. you can use someone else's context file - you may not have control over it. The question is - if you're trying to sign a json-ld graph and say "this is what I say at this moment" - the context file may then change. 

[discussion on signing JSON-LD assertions and context files]

Amy: [out of scope]... they just want to sign some bits... 

Hadley: it does say that the linked data security vocab is in scope...

Amy: a lot of orgs trust vocab hosting orgs like schema.org - they just want to be able to sign a graph that you can seralise however you want to...  There's lots of work on versioning of contexts - best practice to snapshot a context rather than fetch it all the time.  

Hadley: it sounds like they're aware of these issues and the working group is going to address them. doens't feel there is anything we [the TAG] should do.

Amy: I am sympathetic to the concern the concern that the group [gets bogged down in philosophical debate].

Hadley: can we help them make the charter more concrete?

Amy: i think it's very specific. 

[reviewing the deliverables and discussion over whether it's focused enough]

Hadley: [concern about wording about "not relying on specifications produced by this working group"]

Hadley: the other thing... if this is as mature as it sounds ... this sounds like it should have come to the TAG for review. the concepts...

Amy: the specs have not caught up with the implementations...

Hadley: it would be good for the TAG to review in the normal way...  We might have opinions about [the scope of deliverables]... and provide feedback to the wg ...

[...discussion on whether and how we review charters...]

Hadley: e.g. Data on the Web Best Practices working group - included "the deliverable is a best practices document... has this function..."  We weren't working with docs that come out of CGs....

[...discussion on whether we should request them to request review...]

Amy: ...review the charter to make sure the docs make sense.. but should we review the input docs?

Hadley: I don't think we need to formally review the input docs - but we need to see them - and see the logic of how we went from the input docs to the charter and deliverables... and why we're shaping it this way. that should be in the explainer. 

Dan: could we suggest that they add it to the explainer?

Hadley: sure.

Amy: will suggest.

Hadley: thinking about the reviews we've done on DIDs - we gor involved when the specs were fully baked - and didn't have the opportunity to help at a big picture stage.  A design review rather than a doc or spec review.

[...decision to ask them to request a TAG review of the charter using the existing explainer...]

### Session 10

Present: Sangwhan, Lea, Yves, Dan

Capturing tabs vs capture tabs...

[discussion on which to close]

Looking at [609](https://github.com/w3ctag/design-reviews/issues/609) and [625](https://github.com/w3ctag/design-reviews/issues/625).  

Lea: explainer still doesn't have use cases...

Yves: same use case but different solutions??

Sangwhan: the one that Dom did is actually a dispute resolution.  

Dan: what's the dispute?

Sangwhan: 2 different proposals...  One from Chrome is the one that all the applciations implement. 

Dan: What's different about Mozilla's proposal?   Is there a substantive difference?

Sangwhan: the one that content on the web actually uses is the one that chrome ships.  E.g. I couldn't do tab streaming in whereby in firefox but could in chrome.

Dan: is the issue to with privacy?

Sangwhan: privacy.

Yves: I think it's more to do with security than privacy - ensuring that it stays on the same tab.  I think you can probably do the same with the other one. 

Lea: is it actually a good pattern that they're bringing 2 different proposals to the TAG for review?

Sangwhan: we do have a process - a dispute escalation - where the groups can't agree on a single solution. but they didn't use that template.

Yves: different sharing modes - screen or tab?  You can say you want to share one tab and share that tab even if you move to another tab.  Or you may want to share your viewport... 

Lea: both proposals have very similar mock ui... share screen, current tab and other tab....

Sangwhan: functionality wise it feels like they're equivalent. 

`The user need is clearly articulated. There should be one approach to this. One of the proposed APIs enjoys existing implementation. `


Sangwhan: i think we should sit down and find out what discussion has happened...

Dan: I'll ask Dom for an update....

#### [Web Transport](https://github.com/w3ctag/design-reviews/issues/389)

Sanghwan: i set it to proposed close - i think we shoudl close it.

Dan: OK

Yves: yeah and re-open if they want more feedback.

[closed]

#### [RTC Ice Transport](https://github.com/w3ctag/design-reviews/issues/304)

Sangwhan: we shoulc close...

Yves: it's implemented... 

Sangwhan: by chrome...  not implemented by other browsers...

Dan: maybe we should point that out in the closing comment - as an issue?

Sangwhan: I sent out some feelers - noone is particularly against this but there are inconsistencies between implementation.  But it's not a high priority...

Dan: yes we should close it then if we don't have anything to add.

#### [Event Naming](https://github.com/w3ctag/design-principles/issues/280)

Sangwhan: past tense, current tense, future tense... 

[reviewing all events on the web platform]
 
`abort
ended
addtrack
change
removetrack
messageerror
message
animationcancel
animationend
animationiteration
animationstart
copy
cut
DOMContentLoaded
dragend
dragenter
dragleave
dragover
dragstart
drag
drop
fullscreenchange
fullscreenerror
gotpointercapture
keydown
keypress
keyup
lostpointercapture
paste
pointercancel
pointerdown
pointerenter
pointerleave
pointerlockchange
pointerlockerror
pointermove
pointerout
pointerover
pointerup
readystatechange
scroll
selectionchange
selectstart
touchcancel
touchend
touchmove
touchstart
transitioncancel
transitionend
transitionrun
transitionstart
visibilitychange
wheel
afterscriptexecute
auxclick
beforescriptexecute
blur
click
compositionend
compositionstart
compositionupdate
contextmenu
dblclick
DOMActivate
DOMMouseScroll
error
focusin
focusout
focus
gesturechange
gestureend
gesturestart
mousedown
mouseenter
mouseleave
mousemove
mouseout
mouseover
mouseup
mousewheel
msContentZoom
MSGestureChange
MSGestureEnd
MSGestureHold
MSGestureStart
MSGestureTap
MSInertiaStart
MSManipulationStateChanged
overflow
select
show
underflow
webkitmouseforcechanged
webkitmouseforcedown
webkitmouseforceup
webkitmouseforcewillbegin
open
loadend
loadstart
load
progress
webglcontextcreationerror
webglcontextlost
webglcontextrestored
toggle
cancel
close
beforeinput
input
formdata
reset
submit
invalid
search
canplaythrough
canplay
durationchange
emptied
loadeddata
loadedmetadata
pause
playing
play
ratechange
seeked
seeking
stalled
suspend
timeupdate
volumechange
waiting
slotchange
cuechange
enterpictureinpicture
leavepictureinpicture
versionchange
blocked
upgradeneeded
success
complete
devicechange
mute
unmute
merchantvalidation
paymentmethodchange
shippingaddresschange
shippingoptionchange
payerdetailchange
resourcetimingbufferfull
resize
bufferedamountlow
closing
tonechange
gatheringstatechange
selectedcandidatepairchange
statechange
addstream
connectionstatechange
datachannel
icecandidateerror
icecandidate
iceconnectionstatechange
icegatheringstatechange
identityresult
idpassertionerror
idpvalidationerror
negotiationneeded
peeridentity
removestream
signalingstatechange
track
audioprocess
activate
contentdelete
install
notificationclick
pushsubscriptionchange
push
connect
audioend
audiostart
end
nomatch
result
soundend
soundstart
speechend
speechstart
start
voiceschanged
boundary
mark
resume
beginEvent
endEvent
repeatEvent
unload
removeTrack
afterprint
appinstalled
beforeprint
beforeunload
devicemotion
deviceorientation
gamepadconnected
gamepaddisconnected
hashchange
languagechange
offline
online
orientationchange
pagehide
pageshow
popstate
rejectionhandled
storage
unhandledrejection
vrdisplayactivate
vrdisplayblur
vrdisplayconnect
vrdisplaydeactivate
vrdisplaydisconnect
vrdisplayfocus
vrdisplaypointerrestricted
vrdisplaypointerunrestricted
vrdisplaypresentchange
timeout
inputsourceschange
selectend
squeezeend
squeezestart
squeeze`
       
[following on from previous discussiin with Lea, Ken and Sangwhan]

Sangwhan: e.g. connected events  - should we have WebHIDconnected, webusbconnected, etc...? 

Lea: big can of worms...  One of the main issues is - the current patterns that are more common make the names less readable. tension between readaility and consistency. Discussing some other issues - should we recommend that they always have a subject? If so, first or last?  We should document common verbs. E.g. `change`.  Also what about before and after prefixes... Most of the discussion was on tenses and where subject should go... 

Sangwhan: my take is - it's best that we have something concrete - a blurb that we'd like to put into the principle. And start the discussion from there.  A draft principle - in github for people to pick at. 

Sangwhan: we need more pattern recognition... we haven't identifed all the patterns yet.

Lea: I tried to identify some in the issue but there are more.

Lea: we should focus on common events...  Is there a systematic way we can find out what's common?  Use http archive?   Crowdsource the pattern generation...   Twitter?

### Session 11

Present: Hadley, Lea, Tess

#### [Early design review: Sanitizer API](https://github.com/w3ctag/design-reviews/issues/619)

Lea: we've given feedback, they've made some changes and explained why they can't address others. I think we're done here. Tess?

Also, sanitize to string vs sanitize: they have two methods, and they've received criticism for that. We pointed out that a document fragment serialization algorithm doesn't belong in this disucssion. So I opened an issue in WHATWG. I think it's stalled, but there wasn't push back against it.

Hadley: do we have danger if we bake the algorithm into the spec? With crypto, we've said "expect algorithns to evolve faster than the spec"

Tess: Yes and no. the editors of the HTML spec will have to be vigilant and keep this up to date, and browser engineers to be vigilant and implement those changes. But that's better than the status quo. Sanitisation is done by JS libraries, which may/may not be maintained, on sites that may/may not be maintainted. So this probably a win over the status quo.

Lea: Agreed. In most cases, it would be tweaking the default config.

Tess: right. Suppose some broswer impelenents a new element befoer others, or suppose a browser engine has implementations of non-standard elements that aren't exposed to the web but are exposed to other clients. Ex: webkit has `<attachment>`, which is not exposed to the web. It's used for mail clients, to signal the web view.

In webkit, I would expect the default block list for the sanitiser to include `<attachment>` when that element is enabled.

Lea: Does their spec allow for default config?

Tess: it's not a browser. The mail client would have this turned on (add attachment to the blacklist), and would be great client of this sanitizer API. If you think about parsing a mail message itself, you're parsing the hierarchy of MIME parts. Each step of THAT is untrusted. People try to do buffer overruns in mail clients by having weird names for attachments.

This seems fine.

I agree that sanitiser strings seems misplaced, if we want to way to serialise a document fragment, we should just have one. And you'd just sanitise the string by calling this.

Lea: Re UAs supporting proprietary elements and needing to add to config... could this apply to browsers? Would it be helpful to allow UAs to extend this default config?

Tess: I think UAs should be allowed to extend the default config mostly because... I think we want the default config to be safe. And authors to have to opt in to less safety. But you could imagine a browser like Brave might want one even stricter than default.

Lea: or the user to customise it

Tess: sure.

Browsers are free to violate specs, and if they do in practice we can update the spec to match that reality.

We shouldn't add it unless we need it.

hadley: what definition of funky?

Tess: I'm proud that they have a definition of handleFunkyElement. hyperlinks with js URLs, form elements whose action element has a js url, and input/button elements that have a form action attribute with a js url.

Hadley: 'funky' is not a very helpful descriptor, may not be useful for people outside the group.

Lea: I don't have a problem with 'funky'. My main issue is that it talks about elements but 75% of it is attributes.

Tess: moving this functionality into the browser is much better, because the browser is more likely to be aware of new elements in HTML. We added the template element not long ago, and there are lots of sanitiser libraries that don't handle it. I'm inclined to say thanks for doing this important work, let us know how it goes.

Lea: I'll comment and propose closing. 

#### [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583)

Lea: this is a very confusing name

hadley: agreed

Tess: especially when the main issue is "should my background image print?"

[discussion on Alice's question: One thing that I note is that "normal" is more or less synonymous with "light", in practice. Why have two values which mean roughly the same thing? Could "normal" be replaced with "light" as the default?]

Tess: It seems the WG looked at it and decided that on some devices (like TVs), normal is actually dark rather than light. 

They have considered all of Alice's feedback, have come to conclusions on all of it. I'm satisfied that they've considered it all. Not sure if Alice would agree. But I'm inclined to say okay.

Agreed: we'll propose closing it

Draft closing comment:

Hi @fantasai, @TabAtkins!

Hadley, Lea, and I took another look at this during a breakout this week. Overall we're happy with this set of features that solve a number of real problems. @alice raised a number of points, and we see that the WG has considered each of them.

Thanks for bringing this to us!

#### [Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/544)

Started to talk about this but we quickly ran out of time.

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521)

Ran out of time.

### Session 12

Present: Kenneth, Lea, Peter

[Realms](https://github.com/w3ctag/design-reviews/issues/542)

Questions about importValue() method: how does this work with default exports, is there a mechanism to get multiple exports in one call or is it required to call importValue for the same module for each export? (If so, we presume the module is only imported once)

The mechanism for passing values to imported callables is unclear. There are mentions of transferrrables, but non-transferrable objects can be passed to? If so, what's the mechanism, copy? If the same object is passed multiuple times, the realm sees different objects?

What's the relationship between compartments and realms now? Will compartments allow sharing of objects?

Not sure about the name of 'importValue'

### Session 13

Present: Peter, Tess

#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399)

This has been pending external feedback for a while. They said they would update the explainer "soon", in January. Tess pinged them for an update.

#### [Raw Sockets API](https://github.com/w3ctag/design-reviews/issues/548)

Also pending external feedback (we sent them a bunch of feedback on this in September.) But it's possible they didn't see it because they requested that we open issues in their repo. Peter filed our feedback from September [there](https://github.com/WICG/raw-sockets/issues/1#issuecomment-840144834) so they don't miss it.

#### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532)

In exactly the same state as the Raw Sockets API one. Tess pinged ms2ger to see if he'd seen the feedback from September.

#### [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594)

Peter & Tess talked about this [at our last F2F](https://github.com/w3ctag/meetings/blob/gh-pages/2021/01-Kronos/minutes.md#594-early-design-review-of-modal-close-signalsmodalclosewatcher) but never posted public comments after that discussion; we've now [done so](https://github.com/w3ctag/design-reviews/issues/594#issuecomment-840150249).

### Session 14

Present: Tess

Merged a bunch of PRs:

* https://github.com/w3ctag/security-questionnaire/pull/114
* https://github.com/w3ctag/security-questionnaire/pull/115
* https://github.com/w3ctag/security-questionnaire/pull/118
* https://github.com/w3ctag/security-questionnaire/pull/119
* https://github.com/w3ctag/security-questionnaire/pull/120
* https://github.com/w3ctag/security-questionnaire/pull/121
* Fixed the build.

And closed a couple of open issues:

* https://github.com/w3ctag/security-questionnaire/issues/125
* https://github.com/w3ctag/security-questionnaire/issues/104


### Session 15

Present: Amy, Dan

#### [Ethical Web Principles](https://github.com/w3ctag/ethical-web-principles/)

[PR 32 priority of constituencies](https://github.com/w3ctag/ethical-web-principles/pull/32) - updated with suggested changes and merged.

[PR 31 environmental concerns](https://github.com/w3ctag/ethical-web-principles/pull/31)

Hadley: not sure we need this level of detail

Amy: it's nice because it references the [right-to-repair stuff](https://www.theguardian.com/world/2020/mar/11/eu-brings-in-right-to-repair-rules-for-phones-and-tablets). A bit out of scope for Web.

Dan: so maybe we like this sentiment but we should discuss it... could be condensed down. Makes sustainability principle much bigger than the rest. Too much detail. [left comment](https://github.com/w3ctag/ethical-web-principles/pull/31#issuecomment-840356391)

Amy: I'll take the action.

**[Issues](https://github.com/w3ctag/ethical-web-principles/issues)...**

Amy: closing 39 as dup of 26. For 26, respec bug. Will open issue asking why no track docs don't link to latest published version.

Hadley: 38 still needs addressing

Dan: 34 - deprecating the term "user". Personally agree. But we use "user needs", really good job of getting people to focus on important things.

Amy: "people who use the web" gets wordy. haven't thought of a better term

Hadley: users is a role. Other roles like developers. Good to not lose track of people who are in those roles

Dan: when we talk about users somtimes people get confused, like my advertising agent realtime bidding network is a user.. maybe we could have a stylel guide kind of approach where we say..

Amy: define what we mean by user, specifically

Dan: first use of term user in EWP... 

Hadley: intro, third paragraph

Dan: We could change some of the references to users to people to make it clearer, and maintain continuity.. "represents the needs of people using the web"

Hadley: not sure I'm in favour, but we could have a glossary.. useful for user agents as well as users.. people reading this who will not appreciate that user agents mean browsers or things beyond browsers

Amy: user agents is jargon

Hadley: this is a foundational piece for the community, be great to have everybody agreeing about what we're discussing

Dan: can do both.. glossary at beginning, and take a look at every instance of "user" and ask if it can be changed to "person"

Hadley: another for glossary might be i18n and l14n

Amy: assigned

Dan: [25 - avoid dark patterns](https://github.com/w3ctag/ethical-web-principles/issues/25). Discussed before, should be in design principles. Open issue in design principle and in security and privacy questionnaire.

Amy: feel like generally the whole EWP encompasses this sentiment

Hadley: feels like some of the problem is in those places but some is not at the spec author level, but some is at the website level. The people reading the security & privacy questionnaire is not the website authors. EWP has a broader net.. platform providers, hardware.. if we are talking to site authors it might belong in here.

Amy: want to go through discussions of dark patterns and see where this stuff can be integrated into existing parts of EWP and see if there are any major gaps

Dan: agree. Interesting hearings in US about dark patterns at the moment. A lot more documentation out there about dark patterns. We could have a reference to dark patterns in the same level as i18n, a11y, privacy, security, those are patterns. Reference a definition, and see what we can add, if anything, to each principle.

... two other meta issues - numbering principles, we should do that.

... new document type that is W3C statement which could be used for a note, finding, or something else from a WG that is not rec track, so no IPR, but is intended to get W3C community consensus behind it. Targeted at findings. They mention EWP as one of the candidates to go through this process first. I think that's positive, but will subject this document to wider review. Statement is voted on by the AC.

Amy: Tangent - dystopia avoidance checklist.. centralisation concerns.. something like that 

Dan: might fit into design principle and security & privacy - concerned about having another document to update

### Session 16

Present: Sangwhan, Lea, Amy, Dan, Yves, Hadley (part way through)

Sangwhan: design principles weeks... difficult to schedule.

Lea: yes - the current way things work is not sufficient to make good progress on design principles.  Given that we have this breakout feature.. 

Sangwhan: work mode in design principles week is one thing... principles breakouts... or make sure the design principles week is never allocated for other purposes... 

Lea: would be nice if we could work on design principles more frequently... 

Samngwhan: we could allocate one of the weekly breakouts to a design principle... 

Lea: What if we had one design principles issue on every breakout when it's not design principles week?

Dan: right now we assign issues to milestones, milestones represent each week, in the design principles weeks the issues are drawn from design principles, ethics and security and privacy questionnaire. It's a shorthand for everything besides design reviews. Intention was that we weren't getting to design principles at all.. design reviews can eat up as much time as they're' given. We've got to ringfence time for design principles. We've done a fairly good job. I like the idea o fmore time.. part of the problem is if we are only spending one week a month on design principles we lose context. Everybody needs to get back in the mindset of design principles. I like the idea of keeping design principles as a thread throughout the week, especially if we are trying to close design review issues. Cautiously optimistic about the idea of adding a design principle to each breakout.

Sangwhan: if there is a PR would be a good start for putting it on the breakout. Sometimes I write PRs and getting them reviewed takes a lot of time.

Dan: we can also automate that. Leave it to judgement about landing PR in breakout or going to plenary

Amy: I also think an issue/PR on design principles each week is a good idea

Sangwhan: even quick review. Principles are pretty short. Land in plenary if everyone agrees.

Dan: opening a [new issue](https://github.com/w3ctag/process/issues/24) in process repo

Lea: label for PRs that need discussed in breakouts? PRs that are too early could always be marked as draft. Or PRs already reviewed.. not sure it should be as simple as pick up whatever PRs there are

Sangwhan: you could set a milestone on a PR

Dan: we don't have milestones set up right.. label might be better - "agenda+"

Sangwhan: stuff we can't immediately land, external feedback to discuss. Adding "agenda+" to anything that looks moderately complete or is worth discussing

Lea: the more we work on design principles saves us time in the long run from doing design reviews, fewer things to explain, we can just link

Sangwhan: aside from one with a lot of comments from alice, put agenda+ on every other PR

Dan: we'll try next week, see how it goes

Sangwhan: Our chat is inactive... we should have more async dialog.  

Dan: I get a notification on core-tag whenever any mention or channel or here. My intention is to be active. I'd encourage everyone else to do the same. Everybody is busy. Always going to be a challenge.

Sangwhan: make it a habit to communicate more over chat..

Lea: be good to have more async

Dan: I don't know I agree it's inactive.. there's activity every day.. could have some bots..?

Lea: noise... more about how long it takes to get a response to a question. 

Sangwhan: is chat for discussions or just pinging? more of the latter in our case.

Dan: how can we encourage everyone in TAG to treat the chat more as an interactive mechanism?

Hadley: I feel like it's not very ... I'm used to IRC.. you can reply in slack to comments that aren't the most recent, I missed my chance to comment on older messages..

Sangwhan: threading allows you to revive stuff. You can bring back old threads.. checkbox to revive the message

Lea: as much as I like open protocols I haven't seen an IRC client that comes close to slack

Sangwhan: irc cloud is not even close

Dan: personally moving back to IRC would make me less active

Lea: same

Amy: fortunately bridges exist

Sangwhan: Peter is against slack and prefers matrix, but matrix is not great. Agree in principle

Dan: with him in theory..

Amy: not a tooling issue

Lea: is if people don't have slack open all day but have irc... informs how fast to reply

[disussion of notifications]

Dan: keep in mind core-tag is private for the TAG and is not archived. If we're having substantial technical discussion we should be having it elsewhere. More ephemeral. Should we be using our open channel or using some more open channel or on w3c community slack for discussions, enabling anyone in community to see what we're talkinga bout, and only using private channel for informal stuff.

Yves: fact that core-tag is not archived gives people possibility to speak freely

Sangwhan: archiving should be explicit not automatic

Dan: the point being we should be trying to do as much work as pssible open and archived such as minuted discussions. Having technical discussins in github issues is better because it's more transparent. Agree that sometimes you need to have discussions about things where we need more privacy.

Sangwhan: large list of topics where we want group consensus before we say anything public

Hadley: agree. On the other hand, looked at tagmem channel on IRC and there's about 20 people in it who are lurking, some of who is us. Audience there that is presumably expecting us to do something..

Sangwhan: we could make a channel on community channel.. but bigger slack is the faster the messages disappear, a lot of people in it

Dan: we have one. *dusts it off*

... Can we do something like have a culture of checking in every day?

Yves: we can try to push for having more work on the design principles done in the chat

Sangwhan: sounds great

Dan: should we swap to whereby?

Lea: better interface

Dan: we've been swapping back and forth... whereby is not open source.

Yves: advantage of jitsi is possibility of fine tuning video quality and bandwidth

Sangwhan: whereby has mobile mode

[settings discussion and pros and cons...]

Hadley: happy jumping around but we only need one channel during f2f

Sangwhan: i propose breakouts for design principles week

[playing with whereby breakouts]

Dan: using webrtc is the important thing

Dan: breakout times? Discuss later

### Session 17

Present: Dan, Rossen, Amy, Hadley, Tess

#### [Web Authentication Level 2](https://github.com/w3ctag/design-reviews/issues/577)

Dan: we left some feedback, we got [a reply](https://github.com/w3ctag/design-reviews/issues/577#issuecomment-809737874).

Hadley: seems like compensation for the fact there isn't standardisation somewhere else - need to support different vendor attestation formats - coping with all that complexity rather than having a format for it. Sounds out of scope ofr this group, but it's a shame.

Dan: considering the cross browser support I don't know how useful.. where to put our energy? Push on that issue, or leave it as a closing comment?

Hadley: the concern is that in our original feedback in March we asked for information about device vendor specific mechanisms being required. They said because the world is complex and that's what we've got to deal with

Tess: true

Hadley: looks unfortunate to be baking that into the web when it goes against our design and ethical web principles. But I don't know what they can do differently.

Tess: don't think it's as concerning as that. The website is in the middle. One side you've got authenticators from different vendors that have different security properties. On the other hand, backend services that the website has to deal with that migiht have their own reqs about what kindof security is good enough. Putting aside the vendor specific question, we were always going to end up at a place where there needs to be some kind of negotiation between the client with an authenticator and mediated by the website and the people behind that who have requirements. I think they were always going to end up with a technical solution with this level of complexity. That had multiple attestation formats, different authenticators with different characteristics. Unsurprising market reality that some of those distinctions have fallen on vendor lines as opposed to other lines. Don't disagree, but would be surprised if in a world where we didn't have this on vendor lines it would be other lines.. and the architecture would be the same or more or less the same. Architecturally I don't know if they're doing anything wrong. Reflecting reality of different platform authenticators and people like banks and govt agencies have different requirements. Probably okay. But we don't have to be happy about it. This is much better than EME, which has complete black boxes. In this case the different attestation formats are formats you can inspect and see what they say and verify cryptographically that the person you think said them said them.

Hadley: agree.

Dan: close with recommendation that we think this is problematic and we understand the compelxity and constraints but we wonder if there couldn't be a better..

Hadley: I'd like us to do that, in the future we'll want to know what we were thinking when this came up, be nice to have those comments in one place

Dan: I'd like to push on the incognito thing as well. The response to my question is reasonable.. it's gated behind a permission.. might want to consider it being done differently in incog

Hadley: response.. I'm not sure how it answers question. User is opting into fingerprinting?

Dan: yep

Hadley: okay? not sure user is going to get that

Tess: imagining the case... comes up because i have a keyfob authenticator thingy and I'm using someone else's computer to log into my bank, so I start private browsing, go to bank site, log in with 2fa, browser asks for permission, I say yes, do the hardware dance, now what has the site learned about me that it didn't already know?

Dan: learned the type of computer you're on

Tess: which in this scenario is someone else's. Interesting because it adds to the overall sense of where I spend my time and who with, but they only have general device fingerprint, but also IP address

Dan: already know what kind of computer you have because of the UA string.. if you were using private browsing you could be obfuscating that

Tess: they have a better idea of the computer you're on than before. If it's incog on your own device and you're using a platform authenticator they might learn a lot mor eabout the device you're on because only certain devices are capable of doing that. Myabe part of why this is hard is you use webauthn on banking sites.. places where they already know a lot about you. So people say of course they're going to learn about you. We have these very silo'd part of our lives. My bank knows all about my finances but not my sexual preferences... probably figured out from credit card history.. but a lot of things your bank doesn't know because you try to silo them into financial stuff. If theyr'e able to learn enough about your device in incognito mode because you used webauthn where they didn't have enough to go on before, if that was th edelta they ndeeded fingerprinting wise...

Dan: mistake to make the assumption tihs is only going to be used for banking or financial services

Tess: agree, not assuming that. Even if you restrict the analysis to the case where it's highly sensitive, it's usually a case where they might kno sensitive info but it's siloed. They could learn a hell of a lot more by fingerprinting, especially if they work with a third party identity broker they can cross link and learn other things that are none of their business. That said, it's probably the case that it's easy to fingerprint users in incog mode already. Not any worse than status quo - crappy argument, status quo is unacceptable

Rossen: bad argument

Hadley: agree. User giving permission is also bad. "access to learn about your keyfob and also match it with high accuracy a bunch of other information?" wouldn't be in the permission

Tess: permission is targeted - just want auth - not give the keys to the theoretical mansion

Rossen: META: do we need a "Resolved : OK with concerns"

Tess: if we're going to close it in that state we should make sure the steps to remove that concern are clear. Disable the feature incog mode? Conflicts with principle about undetectability of incog

Dan: making it more clear to users that information is being shared with a third party that could allow them to be tracked?

Tess: yeah. probably the case that they can't prescribe ui stuff, but can add a note to the spec saying when you ask for permission here make it clear that there's more to it than just doing the authentication. UA probably won't follow that adviec because number of words in a prompt is small

Rossen: even those who do it, users are not necessarily going to... even if they read it.. not going to understand the implications

Dan: when it has to do with tracking, just read only 5% of people are turning on tracking. People are not just tapping that away. 

Tess: would you be satisfied with them adding a non normative note to the spec?

Dan: would be fine. They should add something in the considerations section?

`Having said that, we understand the constraints you're under regarding the attestation formats.  For our own notes, we'd like to say that it isn't ideal to bake vendor-specific attributes into the web platform and that it would be ideal if they all converged on a standard. But we recognise that is out of the remit of this work.

We remain concerned about fingerprinting. The argument that users give permission feels weak to us because they are not explicitly giving permission for access to information which could be used for fingerpinting (and down-stream tracking).  Could a note be added to the spec (eg. where the feature is described as well as highlighted in the privacy considerations section) that could guide implementers that when users accept the prompt they may be sharing information that could allow them to be tracked?  

Other than that we are fine with this work. Thanks for bearing with us regarding the long delay in getting you feedback.`

#### [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529)

Rossen: I remember looking at this.... what's new?

Tess: seems like they've identified 4 changes from the last time they went to REC. One of those is webidl fixups, fine. One is only exposing in secure contexts. Also fine. Geo is sensitive. Control by feature policy, probably a good thing, it would be funny if random iframes could do this. 

Rossen: is webkit committed? according to issue 41 about feature policy it looks like everyone but webkit is committed

Tess: not in the devices and sensors wg, so weren't there to say. Also fixing confusing thing. That's probably fine. But there has been all sorts of discussion since then. Hadley noticed a weird thing with privacy, marcos fixed it

Hadley: looks resolved

Rossen: I'm good with this

Tess: deeper dive than that?

Hadley: still weird from a privacy standpoint to create a spec that says hey developers please don't take advantage of this sensitive information, when developers may have a lot of incentives to do otherwise. 

Dan: privacy and security considerations.. saying be nice, don't abuse this. This is information for recipients, not for implementers. Could we recommend that implementers make their UI explicitly inform users when sensitive information is being shared?

Tess: next section implementation considerations goes into that a bit. the API itself is gated behind a permission?

Rossen: yeah but

Dan: also visual information that you're being tracked, regular prompts, that user agents and OSs do

Tess: would be great for their implementer part to go into great detail listing all those things for privacy and security

Dan: be more explicit about other things implementers can to do mitigate against misuse of information - additioanl prompts, visualisation of when location is being used, periodic prompts ("continue to allow"). Non-normative. But would be for the implementers rather than for the receivers of information, which is weak.

Hadley: makes sense. Last bit of section 3.2 says implementers are advised to enable user awareness of location sharing ... revoke permissions... sounds like it's easy to exxpand that into what you're saying.

Tess: exactly

#### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414)

Dan: is this in privacyCG?

Tess: no. WICG.

Dan: explainer updated.. rereview?

`Hi @csharrison @dvorak42 - we're picking this up again at our virtual f2f this week. It looks like this work is ongoing in WICG. Can you provide any further updates? Any response to @martinthomson's message above? Should we be re-reviwing? If so can you let us know what's recently changed in your design?`

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342)

Dan: no update yet. They're still working on it.

Tess: that's fine. PrivacyCG f2f coming up

[bumped to w/o 5-24]

### Session 18

Present: Tess (late), Yves

#### [Review request: Partitioning Network State](https://github.com/w3ctag/design-reviews/issues/596)

Propose close.

Draft closing comment from @hober:

Hi @MattMenke2!

@ylafon and I took a look at this during a breakout this week. Overall we're really happy that you're tackling this work; it's really important to the future of the Web.

> > I think whatever we do, SW (and all storage) should ideally be partitioned by network partition key. If you have B->C->B and use the full path as the key, the inner B would have its own SW, which would certainly a bit funky.

We have a separate design review request that came in recently, [Partitioning Storage, Service Workers, and Communication APIs](https://github.com/w3ctag/design-reviews/issues/629), and that for them, [cookies and network stack related state is out of scope](https://github.com/wanderview/quota-storage-partitioning/blob/main/explainer.md#non-goals). We hope that you're working with them to make sure that the SW/storage partitioning key is the same as the one you're proposing.

We note that the multi-vendor effort to coordinate on all these types of partitioning questions is happening [in the Privacy CG's `storage-partitioning` repo](https://github.com/privacycg/storage-partitioning), which you're hopefully already aware of and pitching in on, which will help ensure that all implementations converge on the same partitioning keys for each kind of partitioned data or state.

Mostly our concern is that there are so many related-but-distinct efforts going on here, we want to make sure that we don't end up with subtly-different and incompatible solutions in each case of partitioning.

Thanks for bringing this to us, and please don't hesitate to come back to us if there are substantive changes that you'd like us to take a look at.

#### [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564)

Set to `pending external feedback` since Mike hasn't gotten back to us since January. Pinged him.

#### [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549)

Yves wanted to make sure they were talking to the right groups at IETF about this, and they are. Propose close.

Draft closing comment from @ylafon:

``Thank you for those answers. From a TAG standpoint we are happy to let the discussion continue in the HTTPBis WG.``

# TAG Virtual F2F - Arakeen

## Breakout Track B


### Session 1

Present: Peter, Sangwhan

Check the schedule / Triage any new issues
------------------------------------------

Sangwhan: 629 and above are not assigned.

Peter: Create 17b?

(Created 17b and put the three new issues into 17b)

### Session 2

Present: Peter, Sangwhan

(Merged 2 issues, asked Rossen for feedback on one - sequence/arrays)

### Session 3

Present: Sangwhan, Amy

Crypto and security principles - draft from last f2f

Fits where in Design Principles? Section 9

Sangwhan: should be actionable by the reader - 3 and 4 are, 1 and 2 aren't
... missing: expected to keep your crypto up to date.. shouldn't be using SHA-1

Hadley: phrase around impartiality... 

Sangwhan: common bindings? 

Amy: see webcrypto spec

Sangwhan: has algorithms such as `encrypt` with algorithm as a parameter

Hadley: could say that, changing algorithms doesn't change the api implementation

Sangwhan: naming of algorithm should not be part of api naming. Should recommend strong, reviewed, up to date crypto. Vendor specific details feels like a separate principle - a bunch of other cases wehre this would happen

... vendor agnostic stuff already in section 8. "Underlying protocols should be open "

Amy: something specific to crypto about algorithm not being baked into api design. Can be generalised but doesn't hurt to be explicit too

[conversation about smartcards]

Amy: maybe we're covered and don't need to mention smartcards

Hadley: I can see us going through this thought process again in future, should make it explicit

Sangwhan: concerned about cluttering document with something that hasn't happened yet. Smartcard stuff already rejected in web crypto. IP committments.

[section name bikeshedding]

Hadley: could add to underlying protocols should be open about smartcards.. many smartcards and other devices come with closed protocols and proprietary IP

Sangwhan: most hardware anyway?

Hadley: could make it broader. It's a design principle right there. Most hardware comes encumbered with proprietary IP.

Sangwhan: I need to know the history of smartcards

Amy: we can sneak in "for example, smartcards"

Hadley: would make me happy but maybe we need a new issue and a proper discussion

Sangwhan: this is a vendor lockin issue rather than a crypto issue. A security issue because you have to trust hardware vendor, but it's a separate discussion outside of the web platform.

Amy: will open an issue

Sangwhan: will make the PR with what we have so far, after discussing the phrase "neutral security experts" in the readouts

### Session 4

Present: Yves, Dan

Talking about [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572).

Yves: def of local networks... what does it mean in ipv6... blur of def of local networks in ipv4... def of what is local is difficult. 

Dan: taking a look at requesor's [latest response](https://github.com/w3ctag/design-reviews/issues/572#issuecomment-819519940).

Dan: requestor seems to be engaging with the comments from IETF... is it beneficial for us to be involved?

Yves: do we agree that it's a good idea to have this kind of specification...

Dan: this is a real problem that addresses a real user need. Many "consumer" devices in the home provide configutation management consoles over web UI..  (e.g.)

Hadley: i think it sounds worthwhile.

Yves: i think we should led the discussion continue but as the TAG, we should say we support the work but we leave the discussion in the hands of the IETF.

Dan: feels like not in our wheelhouse.

Hadley: that's how I'm feeling - and we don't see any red flags.

[discussion on whether to close it]

Hadley: should we suggest the discussion move to their repo?

Dan: i feel like we should suggest the discussion move to their repo.

Hadley: I think it would be useful to see the outputs - when there's a next draft, etc... so we can make clear that we'd like to see it again when they finish with the IETF and the spec is more mature.

'Hi [requestor] - OK we are just looking at this again in our virtual f2f. It feels like you are engaging with the feedback raised in IETF.  The TAG is generally supportive of this work and we understand and agree with the user need as documented.  There still seems to be some work to do with the IETF feedback. However we're going to close this for now here and we suggest that further discussion should happen in the spec's repo. Please re-open this issue when you have a new version to review and we can take another look.' 

### Session 5

Present: Amy, Dan Rossen

#### [WebXR Plane Detection Module]	(https://github.com/w3ctag/design-reviews/issues/620)

Dan: [PR](https://github.com/immersive-web/real-world-geometry/pull/31) that addresses our feedback.

Rossen: things demystified.. added required name... good.. must not reveal details of people.. 

Dan: PR is merged. We should close this.

Rossen: [leaving comment]

Dan: this is a success story. Do we need wider review? Proposed closed?

Rossen: closed it.

Rossen: [closing with comment]

#### [Early design review for the FLoC API](https://github.com/w3ctag/design-reviews/issues/601)

Amy: lots of community discussion (negative).. no more followup from original requester.. more issues coming up.. cohort size.. forging FLoC ID.. matching it with existing user data.. rolled out but not being trialled in EU..

Dan: we should leave strongly worded feedback about no action happening on issues raised, and it's shipped

Rossen: agree.. invite them for a call?

Dan: not a separate document

Rossen: nothing substantial addressing review feedback. Evidence of additional community feedback which isn't being taken in.. but we're not here to manage and channel community feedback. Considering closing as unsatisfied based on lack of engagement. Happy to arrange a breakout with them to have that conversation.

Amy: [will leave comment](https://github.com/w3ctag/design-reviews/issues/601#issuecomment-840667844)

#### [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575)

Deferred to future

#### [Web Share API review](https://github.com/w3ctag/design-reviews/issues/554)

Rossen: treating it as delta review

Dan: we said we're fine with the original API in 179. 

Rossen: in september we did a review not realising it was already signed off. 

Dan: marcos said we should do a delta review

Rossen: PR 137 is a breaking change.. 

Dan: doesn't seem like we need to comment on that. Check with everyone. [proposed closed]

#### [WebXR Augmented Reality Module](https://github.com/w3ctag/design-reviews/issues/462)

Dan: big PR addressing our comments

Rossen: I like the fact that they demystified categories.... Happy with the privacy statement that they added - strengthening the fact that camera images must not be exposed.

Dan: My proposed closing comment

'Hi @Manishearth we are just coming back to tidy this up at our virtual F2F this week. Thanks for making note of that PR. This looks good to us and we're happy to close on this basis. Thanks for working with us and taking our comments into consideration.'

Dan: [done](https://github.com/w3ctag/design-reviews/issues/462#issuecomment-838676220)

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470)

### Session 6

Present:

### Session 7

Present:

### Session 8

Present:

### Session 9

Present:

### Session 10

Present:

### Session 11

Present: Dan, Ken, Rossen

#### [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482)

Ken: I know that Diego was involved with this issue but I don't see him as part of the primary contacts. I will reach out to him and ask if he can be added.

Dan: I agree with Marcus' statement about "apart from subtle things nothing else will be different".

[discussion on whether you need this or if register protocol handler is enough?]

Rossen: would the same be applicable in app to app scenarios?    More applicable example - i click on an email, my handler has outlook PWA registered. in outlook i should be able to click ...

Dan: Or example where you have email client running in a Tab.. and you want clickin on an email link to bring you to that tab and open up a compose function there...  Can register protocol handler do that?

Ken: Yes.

Ken: I think it's the same... it just calls that function underneath.  So that it gets registered when you install the app.  That's fine - it's not something you want every site to do, but when you install something it could be a good time to ask.

Dan: so it's fine - as long as regular web apps running in other tabs for example also have access to the same functionality.

Ken: yes and that seems to be the case.

Rossen: I think that if Diego or Aaron engages it will move this along.  

#### [window control overlay](https://github.com/w3ctag/design-reviews/issues/481)

Ken: this is also moving along ... [article from google](https://web.dev/window-controls-overlay/) ...

Dan: At this point I don't see why we shouldn't close the issue given we have answers to the spoofing concerns.

Rossen: Sure, let's close it.

> *Spoofing*  from article by Google  
> Giving sites partial control of the title bar leaves room for developers to spoof content in what was previously a trusted, browser-controlled region. Currently, in Chromium browsers, standalone mode includes a title bar which on initial launch displays the title of the webpage on the left, and the origin of the page on the right (followed by the "settings and more" button and the window controls). After a few seconds, the origin text disappears. If the browser is set to a right-to-left (RTL) language, this layout is flipped such that the origin text is on the left. This opens the window controls overlay to spoof the origin if there is insufficient padding between the origin and the right edge of the overlay. For example, the origin "evil.ltd" could be appended with a trusted site "google.com", leading users to believe that the source is trustworthy. The plan is to keep this origin text so that users know what the origin of the app is and can ensure that it matches their expectations. For RTL configured browsers, there must be enough padding to the right of the origin text to prevent a malicious website from appending the unsafe origin with a trusted origin. 


#### [ModuleServiceWorker](https://github.com/w3ctag/design-reviews/issues/617)

Dan: [left comment](https://github.com/w3ctag/design-reviews/issues/617#issuecomment-839846164) asking for an explainer.

Ken: this looks good to me.

#### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

Ken: we should close.  

Dan: they're going to come back to us when ...

Ken: when they get cross-browser buy in. 

[closed]

#### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602)

Ken: ... some changes with this....

[reviewing]

Dan: there's lots of fingerprinting info exposed as document in their answers to the s&p questionnaire. Is any of this mitigated against e.g. via a permission request?  [this](https://github.com/webscreens/window-placement/blob/main/security_and_privacy.md#22-is-this-specification-exposing-the-minimum-amount-of-information-necessary-to-power-the-feature) would seem to indicate that access to this kind of data is limited behind a permission.



### Session 12

Present: Hadley, Yves, Amy

#### [Registries](https://github.com/w3ctag/design-principles/issues/68)

Amy: is this made redundant by new w3c process?

Yves: linked to something in the AB? but not

Hadley: in the abyss. Discussed last year... from 2018 asked by the AB..

Amy: [registries track being considered in new process draft](https://www.w3.org/Consortium/Process/Drafts/#registries)

Yves: seems like we can close this.. link to [this issue](https://github.com/w3c/w3process/issues/329)

Hadley: trying to figure out where this came from, and it's originally from us...? 
 if this hasn't come up since 2017, and the Process document has evolved accordingly — I'm not sure this is a good use of our time.

Yves: the work is happening, PR merged into the process. The guide is being tracked in another issue in the process so we should close our issue. If peolpe want to comment on those they can follow the link


#### [Digital goods API](https://github.com/w3ctag/design-reviews/issues/571)

Amy: sort of seems like this should be a library rather than a browser API.. a bit of a hack because stores like Play store don't want an http api for web apps to use

Yves: I thought it was for doing small payments without requiring too much verification, might be a good thing. Ask up front if you can spend that much and then an authorised prepayment and spend based on that amount... 

Hadley: i'd rather spend pennies on a news article than ads and tracking. No API for that. It's not that.

... Amy said this is for smaller stores to compete with mainstream ones, and they're saying they're not interested in that. Maybe we should say they should be interested in that? or to evolve into that? A shame to end up in 6 months or a year having that conversation. Howo can the web better support payments for individual merchants, and have this API that's close but can't be extended

Amy: I'm not sure if they're not interested or they're planning to make it impossible. 

I'm still struggling with this, and how to configure it to work with the specific digital goods store you want to use. To me, it feels like a library which covers different APIs for the different stores, to call the functions that you want to use for that specific store. But they're trying to essentially polyfill this, so you have one API for every store.

Is there a finite amount of stores this covers? It seems like hard coding the Samsung store and Play store? But what about the others we know about (and those we don't)?

Yves: I talked to Ian Jacobs for Web Payments WG, and he pointed me to [an issue](https://github.com/w3c/payment-request/issues/879) where Google wants to allow ammount-less payment. You want to buy something based on the SKU, not on the price. 

Hadley: that sounds risky.

Yves: The plan is to get the details for the country you're in to get that, so it is a negotiation with hte store for the price.

Hadley: should we introduce them?

Yves: I think they are talking already.

```
Sorry about the delay. @hadleybeeman, @ylafon and I discussed this in our virtual face-to-face today.

> the UA needs to have custom code to interface with each store. Each store has a slightly different API

Given this, it seems like only a finite number of specific stores could be realistically supported.

1. How many stores are expected to be added,
2. and which ones so far are involved?
3. Are all browsers expected to support the same set of stores, or is it likely that users will get a different experience in different browsers? 
4. Which browsers have expressed intent to work on this?

We're a bit concerned about further entrenching the 'big player' stores. In the explainer this is compared to the Payment Requests API, as there are a finite number of supported payment providers. We're not sure this is a fair comparison, as in practice anyone can spin up a web store to sell digital goods, and as payment providers face regulatory limitations, this pattern should be an exception rather than something to be repeated.

> I'm not sure "Lookup/Listing" is broad enough

It sounds a bit like you're saying payment is both in and out of scope of this API. If this API passes payment to the Payment Request API, then I think it's okay for the name of this API to be less broad. Something like the Digital Goods Inventory API? (Which a developer can expect to use before calling the Payment Request API?)

```

Hadley: naming issue.. saying payment is in scope for this API even though it's separate from the payment API doesn't make sense to me..

Amy: agreed

... Also related: https://github.com/w3ctag/design-reviews/issues/512 - changing the Payment Request API for the Digital Goods use case

Amy: explainer compares it to payment request API because sites need to integrate with individual payment providers, but I don't think that's fair because there are far fewer payment providers than ptentially stores

Hadley: not a pattern we want to enable, payment request API is an exception

Amy: seems to entrench existing powers

Hadley: plus it's just not scaleable. Payment providers are limited by regulatory things..

Amy: anyone can spin up a web store

Hadley: unfortunate compromise we had to make for payments, but be great not to make it anywhere else. Should have a design principle discussion around it. 

### Session 13

Present:

### Session 14

Present:


### Session 15

Present:

### Session 16

Present:

### Session 17

Present: Peter, Yves

#### [Reporting](https://github.com/w3ctag/design-reviews/issues/585)

Reviewed their feedback to earlier review. We're satisfied with the responses and don't see any issues.

``@plinss and I took a look at this during our virtual F2F, thank you for filling the Security and Privacy questionnaire.
At this point we don't have any further comment on this, this looks OK to proceed. Thanks!`` (to be validated during the rollup -> propose closing)

#### [jxl Content-Encoding](https://github.com/w3ctag/design-reviews/issues/541)

Reviewd their feedback, propose closing satisfied, still not sure the result is worth the effort but not harmful. To be seen if this is more popular that simply swithing to a jxl image format and mime type.

#### [Partitioning Storage, Service Workers, and Communication APIs](https://github.com/w3ctag/design-reviews/issues/629)

We're satisfied with this approach, would like to get Amy and Tess' feedback as well. Propose close satisfied.

We have a small concern with the carve-out for blob url's, but it looks like that's driven by a compat issues.

#### [Service Worker subresource filter](https://github.com/w3ctag/design-reviews/issues/630)

Propose close. This seems way to early for the TAG to get involved. Further, the URL fragment approach seem very limited and tied to a specific use-case. We question why scoping wouldn't be handled during the service worker registration.

#### [Shared Element Transitions](https://github.com/w3ctag/design-reviews/issues/631)

### Session 18

Present: Lea, Hadley, Dan

#### [Consistency](https://github.com/w3ctag/design-principles/issues/285)

Dan: this is a broad issue. I feel like it would help to be specific.

Lea: this is something that keeps coming up on design reivews, leading us to: what kind of consistency should we prioritise? Consistent with what? Often those things are at odds, and we have to prioritise one type of consistency over another.

Hadley: Agree ... it's a theme in a lot of our reviews.  Also the more specific we can be the better our advice will be.  The evergreen web finding - says that the web is continually evolving and that's a good thing.  This came out of device-specific subsetting - hbbtv - TVs weren't getting updates.  SO we said "this ecosystem is evolving." So you could use consistency as a rationale for not improving things. So we should find a way to express this for where we can articulate it being helpful - but doesn't stop us from continual evolution. 

Lea: i don't think it should hold the web back but it should be an intentional choice to diverge from precedent - shouldn't just happen accidentally.  Also sometimes there's nothing wrong with precendent - just that there's different precendents. 

Rossen: there is Concistency under Naming...  BTW closely related to this principle - another one that I have open. Principle that [new features must not break existing ones](https://github.com/w3ctag/design-principles/issues/285). 

Lea: is an example of this `displayConternt`? 

Rossen: consisteny with existing platform could also be "don't break it".

[discussion on whether to move Consitency out of Naming]

Lea: I think if we add a consistency section in (1) or (2) we could link to the Naming consistency section.

Rossen: Prefer Consistent Solutions... after Prefer Simple Solutions ... 

Lea: Not sure it's useful there... There are multiple conflicting precendnts - we should have more detail - API ergonomics, older APIs vs newer APIs.  E.g older DOM APIs vs newer WhatWG editions.  Internal vs external consistency.  Guidance for how to choose what to be consistent with. 

Rossen: to some extent the entire doc is about consistency.

Lea: it would be good to provide a framework.

Dan: Axes of consistency? 

Lea: Bullet points [in the issue](https://github.com/w3ctag/design-principles/issues/285#issue-804375081) (conflicting Web Platform precedents, ergonomics vs consistency, internal vs external consistency --- which may include 3 layers: external precedent, web platform in general, specific web platform technology)

Dan: What guidance to provide?

... (internal vs external) think of what the majority of users will be 

Lea: In most cases the majority is web developers

Rossen: decision flow-charts - for this kind of decision matrix

Lea: a flowchart implies it's deterministic. It's sort of more nuanced than that. They still need to weight the different factors.

Rossen: maybe we could...

Lea: what's the relative priority of factors and within them what's the relative priority?   In prose we can say "choose based on these 3 factors" but if it's a flow chart... 

[discussion on what is obvious vs non-obvious]

Dan: I suggest Lea opens a PR with a modified version of the 3 bullet points - as a subsection of 2 - with a reference to the naming>consistency section.  With some additional factors to consider... 

META: should we stick to one assignee for design principles issues to make it clear who is on tap for each one?


## Breakout Track C


### Session 3

Present: Yves, Dan

https://github.com/w3ctag/design-reviews/issues/545 webxr device API

Yves: issue of allowing access to info of what WebXR gear you have - you may not want a shopping site (for example) to know that you have the latest and greatest gear.

Dan: proposed comment:

`Hi folks @toji @Manishearth @adarosecannon we're just picking this up at our virtual f2f to see if we can close it. I'll note that the accessibility issue that was raised a while back is still open. It would be great if you could put some additional energy there. We also have been thinking about the privacy issues related to fingerprinting. In the case where a shopping site, for example, is invoking the WebXR device API it may be possible for that site to determine that the user has the "latest and greatest" gear. In some cases this may not be beneficial to the user, as the site may then choose to jack up prices. Some sites are known to employ this kind of mechanism (arguably a "dark pattern"). It may be useful in some circumstances to allow the user to only advertise "basic support"... Have you considered this abuse case and possible mitigations?`

https://github.com/w3ctag/design-reviews/issues/550 WebXR Depth API

Dan: [left a comment](https://github.com/w3ctag/design-reviews/issues/550#issuecomment-837955408) asking for status. Looks like no implementation signals from other implemeters, and the spec itself is still marked as "unofficial draft" though it's been updated as of April 2021 so work looks active.

Dan: meta comment on both these: can we close them off?  Is there additional value we're adding by keeping them open?

Yves: rest of the API seems OK.



### Session 5

Present: Yves, Peter

https://github.com/w3ctag/design-reviews/issues/618

Discussed, satisfied with current direction, propose close.




### Session 9

Present: Lea, Ken, Sangwhan

#### [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279)

#### [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271)

#### [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286)

#### [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280)

Past tense would have been more usable if we were to design the Web Platform today, but that ship has sailed.
Tension between usability and consistency. Every pattern we can find makes events less readable!
Some events look really weird in the present tesne, e.g. advertisementreceived -> advertisementreceive, serviceadded -> serviceadd
Also noun first doesn't read as nicely as noun second, like natural language (mousemoved vs movedmouse), but it namespaces.

( Looking at list of events https://codepen.io/leaverou/collab/dyvGYoV )

Maybe part of the guidance should be that a verb needs to be included, otherwise it's unclear when the event is fired, e.g. `identityresult`, `datachannel`, `audioprocess`, `deviceorientation`, `track`

Sangwhan: Common verbs that have been used in the past: start, end, change

Consensus toward recommending present tense even if it doesn't make sense.

`rejectionunhandled` and `handledrejetion`!!

Sangwhan: `mute` and `unmute`: unclear what was muted
Lea: You can always inspect event properties. is the subject needed for namespacing or can different event classes use the same event name?
Sangwhan: I think they can but not sure.

1. Find common patterns in what is currently shipping (e.g. subject verb etc.)
2. Define a list of common verbs
3. Present vs past tense?
4. Patterns on how to detect provenance of event (prefix source or inspect event?)
5. Should the subject be before or after the verb? Currrent usage very inconsistent but mostly points to before.
6. When should we mandate a subject?
7. before\*after\*, \*end\*start?



## Rollups

### 1

### 2

### 3a

Lea: me and ken.  We discussed edropper.  it's been stalled - we nudged.  We had a long discussion about compute pressure...  Ken left a comment...  Also a design principles discussion...

Ken: Abbreviations... We also talked about web codec.

### 3b 

Amy: me hadley and sangwhan - we turned the text drafted in last f2f into something more appropriate.  We wanted to run the phrase "neutral security experts" as opposed to "internationally recognized" 

Hadley: wanted to check the wording.

Dan: i think it works for me.

[we agree on some wording that Sangwhan will make a PR]

### 3c

Dan: Yves and I talked about WebXR Device API and Depth API... basically both of these are a bit stalled.  WebXR device api is already shipping in multiple places. They haven't done accessibility requirements work that they committed to do. Yves pointed out additional fingerprinting mitigation they need to think about - specifically whether a website an figure out whether they're using the latest hardware, could be used for profiling. We raised that. We want to close it, this is the second review request.

... Also webxr depth API. Seems to be shipping in chrome 90 but has no signals of support from other browser engine. The API itself seems fine but no information we have about implementation status and whether it's intended to go to immersieve web wg vs community group. Asked that question.

### 4a

Sangwhan: we talked about total value... pending feedback from Tess.  next web neural networks...  I think we need to escalate a potential issue.  I've raised concerns about the design and the substantial concerns not being addressed.  I think we should set up a cross-group call.  This is one of the issues where our concerns weren't properly addressed.  Some issues raised are e.g. the design with hardware acceleration in mind, and ergonomics not good. 

Lea: we discussed having a design principle for this.  we should bump up its priority.

Dan: I'll try to organise cross group working session

Sangwhan: web codecs - we left some feedback. We addressed everything they asked for feedback on. Waiting for response.  Next managed device API.  I think we should have a position on this.  

Dan: I have left my view

Amy: I was going to open an issue on their repo asking them to enumerate the abuse cases... 

Dan: I think we should mark this issue as at risk somehow...

### 4b

Dan: Cors rfc1918 - closed. The feedback was from IETF.. valid, well documented user need, remaining issues outside of our wheelhouse. Bring it back when IETF issues are resolved.

### 5a

Lea: me and Tess. We intrinsic size.. didn't think the improvement was signifigant over the javascript library this is designed to replace. Also breaks a CSS precept - introduces state that cannot be described with what is currently there. Would need to be a significant improvement... custom hightlight API module. left comment.  Then spent some time on canves rendering context 2d - color values - also they proposed a filter syntax similar to SVG but not as expressive. That would be confiusing to authors.  We left feedback we thought it would be better to add css properties verbatim instead of cAmElCaSe properties with different names. So we left a comment. We also discussed livedom CSS - pending ext feedback. We also had design principle "simile things should be easy" there is [a PR](https://github.com/w3ctag/design-principles/pull/306) that needs reviewing.

### 5b

Rossen: Me, Dan and Amy... We started off with webxr plane detection.  We had provided feedback.  The authors of that issue did some PRs.. cleaned up things in a nice way. We thanked them, expressed satisfaction and closed. We then moved to screen fold - that's pushed to the future. 

Dan: been renamed to the device posture API - i will ask them to re-submit a review.

Rossen: webxr AR module - good example of folks reflecting the feedback into the explainer and spec text. They went through and added defintiions of concepts. They strengthened the Privacy & Security section.  We closed it.  Next we did web share API.  Another interesting review - we looked at it, we reviewed and it turned out it had already been reviewed.  We gave them a choice of doing a delta review - we went back to their GitHub repo and looked at the merged PRs.  Nothing that stood out. One issue was marked as breaking change but wasn't signifigant.  Looks like the churn has been editorial mostly.  We're proposing we close this.

Rossen: FLOC - we're writing some additional feedback and inviting them to a separate session to discuss. They haven't been responsive to our feedback thus far.

Peter: re FLOC - i have higher level concerns with the privacy sandbox initiative.  Seems to be focused on 1. preserve privacy 2. enable targetted ads. I feel targeted ads are a bug not  a feature.  We should have consensus before raising it as a larger scope issue.

Rossen: some of the efforts they have are tryng to allow for monetization + privacy.

Peter: but being able to have ads doesn't mean you have to have targeted ads.  

### 5c 

Peter: we had one issue - never sniffed mime types - we didn't have a lot of feedback. we left feedback in the past - generally we are OK with it.  We're adding a lot of multi-acronym mechanisms  that are hard to understand... we set it to proposed closed. 

[consensus to close]

### 6

### 7

### 8

### 9a

Amy: we looked at the linked data proposed charter.  some had raised issues about rdf vs linked data and mention of proof-of-work. We asked them to submit a design review request for the proposed charter. I emailed Ivan.  We punted on our other issues... sanitizer API - it looks like they are being responsive... 

Dan: Moved sanitizer to 11.

Lea: Looks like they were responsive. Work is ongoing. Open issues from TAG review. I'll take a closer look to see how it's going.

### 9b 

Yves: Media Source extension for web codecs - discussion about whether it's the right solution, and about hardware implementation details (in their repo). Plan to close, looks fine, WG needs to agree on the solution. No stance from us. Insertable media processing using streams - still discussion about readable/writeable stream going on. Wait until they make progress before closing.

### 9c 

Lea: me and Ken. We talked about event naming.  We looked at event names on the web plarform.  We remarked on how inconsistent they are, etc... we should priotise consistency even if it leads to reduced readability.  E.g. we should probably recocommend present tense.  subjects, prefixes, suffexes...   We also discussed on 10a.  I posted [to twitter](https://twitter.com/LeaVerou/status/1392403095234228231) to crowdsource...  I asked http archive analyst if they could help..

### 10a 

Dan: capturing tabs - two issues. Turned out they're two different proposals. One is a Chrome proposal and the other is Mozilla. We need to find out the current state. From their issues maybe they're more close to merging the two / resolving the conflict than we think. Want to check with Dom. Maybe we can close both.

... WebRTC ICE transport, closed, Web transport, closed.

... And talked more about event naming.

### 11a

Tess: Hadley, Lea and myself.  We talked about sanitizer API.  We think it's in good shape.  Lea took an action to write a draft closing comment. [issue closed] We talked about CSS color adjust. Some stuff we're not hot on.  Main thing is the name but that ship has sailed. Alice had voiced some concerns.  CSS wg considered those points.  They did the appropriate amount of homework.  We're satisfied.  We'd like close this one. [closed] Then we talked about secure payment confirmation. Need to do a deep dive.

Hadley: it feels like they want to use biometrics through fido to give another assurance to the bank that it's actually you. 

Tess: My pain concern: i think it's redundant to what payment request already does.  raised that on the issue - but they said they need it for regular form-based payments. but those don't use payment request api...

### 11b

Dan: URL handler for PWAs: we were happy with.. listened to feedback, built on top of protocol handler, my understanding is they've changed the design so they're proposing an addtion to the manifest but it's effectively a convenience, doesn't add any functionality that the webapp couldn't do anyway. We got feedback that people at MS working on it .. related changes in whatwg / html5, had some back and forth. Based on that we decided to close with a closing comment.

... window control overlay - also closed. Found they were responsive to our feedback, especially around spoofing concerns. They had specific wording which is the mitigations against spoofing concerns we had about putitng UI in the trusted UI area. We called out some stuff that had been written in an article posted by google on web.dev which talks aabout this issue and what they're doing to mitigate. Closed with proviso that we're happy however not happy with the fact that there isn't multiple implementations.

... module service worker - new feature. THey haven't explained it, included a link to explainer but it's a google doc design document. Said they need to move it, and then read it and realiesd its not an explainer. Asked them to write one. Looks like strong support from other implementers though which is a positive sign. Did not close it, waiting for update to exlpainer.

... web socket stream - sitting for a long time. No cross browser buyin. Ken closed it with come back to us with that.

... multi screen window placement - re-reviewing, left comments, need to revisit this. Good they wrote about fingerprinting. But still work to do.

### 12a

Lea: Ken, Peter & Me – Realms - we were confused about parts of the API - imports.. exports... main issue.  [no comment left so still work to do here]

### 12b

Amy: open issue about best practices for registries since 2017 - in summary we discussed we can close ours since it's being discussed in w3c process.  

Dan: let's close it.

Amy: we talked about digital goods API - drafted a comment - talked about how it's creating an interface to native goods stores in the browser... no http API for those stores - basically a hack because stores don't want to implement http API... so we were concerned that ... a finite number of stores can be supported... each store has its own proprietary API... seems centralizey... comapred to payment request... 

Dan: what's stopping App stores from providing an http API that retuens JSON like the rest of the Internet?

Tess: both payment request and EME are somewhat appropriate analogies... EME has content decryption modules that are secret sauce... there are licensing requirements and business deals ... I can see them making the argument that their hands are tied in the same way that as EME ... But I agree that the app store case isn't ... what's the secret sauce here [what's special about it]? Also EME and payment request aren't examples to follow - they're examples of what you have to do sometimes - and in this case it's not clear you have to do it? ... in both EME and payment request there are compelling arguments... 

Dan: agree - this doesn't feel like ti should be part of the web platform.

Hadley: our question about browser interest may give us ammunition on this point.

Dan: I think we need to consider this one 'at risk'... [sets milestone for next week]

[discussiomn of relation to payment request API]

### 13a

Peter & Tess had four issues, poked the ones that were pending external feedback, and commented on the others.

### 14a

Tess merged a bunch of S&P Questionnaire PRs

### 14b

Sangwhan and Peter worked on various Design Principles PRs and issues.

### 15a 

Dan: ethical principles. Landed PR 32 priority of constituencies. Talked about PR 31, contributed by someone in community, trying to level up our guidence around environmental considerations, agreed that it's a good sentiment but too wordy, Amy took an action to write some more concise wording. Also looked at open issues, closed one as a duplicate. Opened a respec bug to do with keeping a link to the latest published version. Looked at deprecating the term user. Not going to deprecate the term but going to minimise the use of the term, and include a glossary that makes it clear when we're talkinga bout users we're talking about a person. Talked about avoiding dark patterns.. possibly we need to add something

Lea: people using dark patterns are intentional

Dan: don't design things that lend them towards dark patterns, or so they cannot be used for dark patterns

Sangwhan: not obvious when you propose a design or an api... 

Dan: consider the abuse cases. Not going to add a new principle, but might add the term into the intro and see what we can bolster in the existing principles, and see what we can do generally in design principles and security and privacy questionnaire. Amy was going to explore do we need a dystopia avoidance questionnaire.

Lea: one questionnaire with privacy & security, and general dystopia section..

### 15b

Lea: design principle of introspection – we resolved it needs to be written... we looked at older ... we created a new label - "write me ASAP" - we scheduled a breakout tomorrow between me and sangwhan to work on these issues.  Did not close any of them.

### 16a

[working practices discussion]

### 17a

Hadley: Dan, Rossen, Amy, Tess, Hadley

Tess: WebAUTHN lvl 2- we talked through the concerns and the market reality... Dan drafted a comment about how they should add something to their privacy considerations... new label for 'satisfied with concerns'

Hadley: ambivalent?

Dan: implies we don't have consensus. this is different. [creates label of **resolution: satisfied with concerns**]

[closed]

Tess: Geolocation API - we talked through what they were asking us to review - we agreed they need more text in their privacy considerations section about informing users to make informed decisions... [Hadley commented](https://github.com/w3ctag/design-reviews/issues/529#issuecomment-840648473). I think we could propose close after they get back to us. 

Tess: trust token API Dan [left a comment](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-840634149)... we have a response. [bumped]

Tess: first party sets - decided to bump - there's a privacy CG f2f next week - we bumped it to 5-24. 

### 17b

Peter: Yves and myself - we looked at the reporting framework.  Feedback all looks good.  We're satisfied - but all report-by-report concerns - doesn't apply to mechanism.  I will draft a coment and **close**.

Peter: next is JXL content encoding - we think there's no harm. So meh. We think the market will deprecate this within a few years.

Tess: a lot of discussion from external folks - Anne had raised some issues om the blink thread... about loading it in browsers... that it shouldn't be sniffed and that it should fale safe not fail open... Both of those are in line with our design principles.  People other than us have been pointing to our design principles, which is a good thing. 

Peter: we have separate issue on the jxl format - but this one is just on encoding. immediately decode back to a jpeg.

Tess: that sounds fine.

[agree to **close**]

Peter: partitioning... same thing - we wanted to get feedback from Amy & Tess -using double-keying for storage, service workers, other api surfaces... carve-out for blobs...  [issue 629](https://github.com/w3ctag/design-reviews/issues/629)

Tess: Yves and I looked at a related issue. Will take a look at this one.  Risk that as we partition more things that people will use different keys in different contexts. 

Peter: [Service worker sub resource filter](https://github.com/w3ctag/design-reviews/issues/630) - may be too early -already got pushback. We should push back.. and by the way the approach doesn't seem good. Already a mechanism to scopye URLs - they should work on extending that rather than inventing http headers.  

Dan: +1 [something about complexity for web developers]

Peter: they should come.

### 18a

Tess: Yves and me - we looked at [Review request: Partitioning Network State](https://github.com/w3ctag/design-reviews/issues/596).  Fundamentally we're glad they're working on this. but is everyone who should be talking to eachother talking to eachother?  We wrote a long draft closing comment - we're proposing to close it. 

[consensus to close]

Tess: we talked about deprecating document.domain. We pinged Mike.  We looked at client hint reliability mechanisms - we weren't sure if they were talking to the right people in the IETF. They have replied in the affirmative. We're going to close it. [consensus to close]

### 18b

Lea: we discussed consistency - [design principles issue](https://github.com/w3ctag/design-principles/issues/285). We agreed to write something.  Also meta issue about design principles - so we were wondering how we indicate who is on tap to write a thing.

Tess: i used a project board .. found this helpful. 

[discussion on what constitues an assignee]

Amy: github API should expose who commented...  You can filter by that.  

[more process change discussion]

