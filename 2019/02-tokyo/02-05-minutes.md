## TAG F2F
##### 05 February 2019

Present: Hadley, Peter, Dan, David, Alice, Tess, Travis, Alex, Sangwhan, Kenneth, Michael[tm] Smith, Yves (aft)

Regrets: 

---

Agenda:

1. Agenda bashing (10:00 - 12:00, hopefully not that long)
2. New members
3. Process introduction
4. Triage
5. Issues

---


## Agenda Bashing

Hadley: I'd like to be on the ethical web discussion. (Happening Wednesday afternoon.)

Dan: Then that should be put on later tomorrow afternoon.

David: Mike Smith says he should be here.

Dan: After lunch today Mark Nottingham will be dialing in to discuss QUIC. Any other points? Think we need to discuss F2F schedule. We need Yves for this so this should be on Wednesday morning. Lukasz needs to be here for the privacy / security discussion, let's schedule that on a afternoon.

Dan: What is happening with TC39?

Kenneth: There is decorators and some other stuff.

Sangwhan: We can talk about some of the stuff they wanted us to review. (To happen Tuesday morning)

Dan: Andrew wanted us to look into feature policy, we should have him dial in. (Thursday morning tentative.)

David: Think we should give him a option of two slots.

Alice: I have some updates on signed exchanges and bundling. We could bring in some local folks into the discussion. (To happen 10AM Wednesday.)

(Mike joins)

Mike: I have some input on your agenda. Signed exchanges. Also portals.

Travis: Already in our review list.

Mike: The issue hasn't had any feedback.

Dan: We'll get to it. There is also design principles document work that isn't in the issues.

Mike: The other reason why I mention this is because Kenji is here. It's not a controversial feature.

Kenneth: HTML modules?

Mike: HTML modules would be nice if there is time.

Mike: WebGPU if you have time.

[Discussion of our work modes]

(Related: https://groups.google.com/a/chromium.org/d/msg/blink-dev/dxqWTSvyhDg/Ucs0xWl-AQAJ)

Mike: Would like you to discuss Web Share, Web Share Target, Web Locks.

Sangwhan: We did review all of those.

Dan: Today I'll be using #general for the online discussion.

## New member introduction time

Alice: Thank you so much Alex and Travis, for your contributions, great to be here.

Tess: (smiles)

## Process introduction

Dan: We are using milestones in github to mark which telcon/face to face should have this on its agenda. (Looking at the backlog.)

## Triage

[Link](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+no%3Amilestone)

(~Skipping HTML issues, chair decision.~)

### [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311)

Dan: [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311). We have marked this as extra time.

Travis: I have looked into this, and I like it. This is a new and improved way of day/time tracking in Javascript, it's a better typed system; times and dates that are not tied to global time. Instances which are on the global timeline, you can go back and forward between civil and global. Also possible to use arithmetic operators on this.

Alex: It seems like it lacks deltas. Anne asked about whether or not Gregorian is enough. Would be interesting to hear about alternative use-cases. Not sure how to re-construct non-Gregorian calendars to Gregorian and vice versa. Integration with input types seems like another issue; would be good to see this aligned with HTML. The idea of adding more high precision timer types which do not line up is a bit strange.

Dan: Extra time.

RESOLUTION: Extra time.

### [Base used to resolve relative URIs to absolute URIs in HTML5 data-blocks](https://github.com/w3ctag/design-reviews/issues/312)

Dan: [Base used to resolve relative URIs to absolute URIs in HTML5 data-blocks](https://github.com/w3ctag/design-reviews/issues/312).

David: This is JSON-LD related. This is to put script-like data that isn't a script into a document.

Hadley: Explainer is pretty good.

Alex: A lot of cases duplicate state of JSON-LD.

Dan: Some issues were raised, and PRs were raised and closed; is this something we need to look into even further?

Alex: They asked us to join a call.

Hadley: We could do this.

RESOLUTION: Hadley to follow-up.

### [Wide Gamut for Canvas](https://github.com/w3ctag/design-reviews/issues/315)

Dan: This is on extra time.

David: That's from the last F2F.

Dan: Do we have enough here?

David: Not enough to close in the next four minutes..

RESOLUTION: Extra time.

### [HTML Modules](https://github.com/w3ctag/design-reviews/issues/334)

Dan: This is pretty new. Kenneth? Sangwhan?

Kenneth: I looked into this and raised a couple issues.

Alex: We can imagine a surface syntax on top of this, as a module? e.g. Script type module - we can put a declarative thing on top; what is the behavior of the default export. Is there an explainer on this?

Tess: Think the default is on the document.

Mike: Anne had some comments, probably on Mozilla standard positions.

Dan: Running out of time, extra time?

RESOLUTION: Extra time.

### [Heads up!](https://github.com/w3ctag/design-reviews/issues/335)

Hadley: They did in the past request us to not review their spec when we raised our first review issue.

Tess: There was a workshop in Seattle about this.

Dan: Should we close and request a new review when it is ready?

Travis: We could just review.

Dan: Do we have consensus to do a review?

RESOLUTION: Extra time.


### [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336)

Dan: Anyone looked at this?

Alex: Every chat application needs this. They want this for the away status; currently it is hard to do.

Alice: Is this possible in native?

David: Is there different definitions between interacting with app vs. computer?

Alex: Not really.

David: Okay, so system level.

Dan: Happy to see a sec/priv section. Especially that they indicated privacy implications.

Sangwhan: What if a ad network ads for this permission?

Alex: Probably should be a top-level restricted feature.

Dan: Should be part of the feedback. Should probably hear from other browsers.

David: Should anyone write a comment on the issue on the top-level constraint?

RESOLUTION: Extra time.

### [Contact API](https://github.com/w3ctag/design-reviews/issues/337)

Dan: Is this to access phonebooks? 

Alex: Yes.

Dan: This is not the first time this happened.

Alex: Persistent silent access to your contacts is scary; this API does not do this. Initially it started as a input type which lets users pick from their contacts list. The specific case that came up is about social network bootstrapping; they push users to native applications so they can harvest all of the contacts.

Dan: Isn't this exactly the problem with (redacted social media service name), tricking users into harvesting user information?

Alex: This is sort of a way against making that happen in a really bad way.

Dan: But if you do a one-time thing, doesn't that not help with bootstrap?

Alex: It does; one time to bootstrap, but at least that's not as terrible as persistent access.

Hadley: that nefarious persistent silent access is a big part of what GDPR is tackling... Fines have already been issued. Wonder if that changes the landscape here.

RESOLUTION: Extra time.

### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338)

David: This is about task queueing and prioritization.

Travis: queueMicroTask?

David: Related-ish, but not quite. This is to coordinate prioritize work within/between content.

Sangwhan: Nice?

David: Prioritization for example in a context of searching and scrolling, where one could switch the priority between one or another.

Alex: I'd love to talk more on this topic.

David: There are a bunch of interesting stuff in here worth diving into.

Alex: We've discussed this in the past; developers should have access to those lower level timings.

RESOLUTION: Extra time.

### [Feature policy control over sandboxed features](https://github.com/w3ctag/design-reviews/issues/339)

Dan: David, you had something on this?

David: I looked at it quickly and realized that the spec link was not particularly useful.

Alex: Is there an explainer?

David: The spec link is a intent, not an actual spec.

Travis: The FP spec says it isn't intending to replace CSP.

Dan: No sec/priv section.

RESOLUTION: Extra time.

### HTML Issues

Alice: I really want to look into focus.

Sangwhan: Spatial navigation also is connected to that.

Dan: I'll put you on this one as well.

Hadley: There was something on chromium.org about ad blockers. This feels a bit like taking away power from the user. https://docs.google.com/document/d/1nPu6Wy4LWR66EFLeYInl3NzzhHzc-qnk4w4PX-0XMw8/edit#

Alex: This is aligning with what Apple has been doing on iOS, which has huge performance benefits.

Dan: Are we talking about web app manifest or extension manifest?

Alice: Extension. In particular related to the request API.

Hober: This is a product-level decision. Out of scope for us. 

Dan: We do some times look at things like this. 

DAvid: I would quibble that it's out of scope, becase the reality is that there is some degree of interop already. There is a community group, but Chrome isn't interested so it doesn't have much traction. 

Alex: We are evolving this, which is inevitably going to break things.

Dan: If there is going to be a new extension API, that might be a good place to talk about it?

Alex: depends on how much extensions need to be interoperable. Open question here

Hober: ??

Dan: the TAG could play a role here, encouraging people to talk about this. We could issue a finding. 

Hadley: I do think we need to worry about ad blocking... but this sounds like it's more about browsers diverging and competiting. Which is healthy; gives users choices about how they experience the web. 

Dan: It sounds like this is breaking one approach. 

Travis: It seems clear that the ability to block ads is not going away. It's changing. 

## Issues for this F2F

### [Clear site data](https://github.com/w3ctag/design-reviews/issues/62)

Sangwhan: Waiting for mkwst on this, not sure if this will ship is still relevant.

Dan: Bump and ping?

Hober: Can you put me on this? This API is interesting if you partition your cookie jar.

Dan: Want to discuss this week?

Hober: No.

Dan: Revisit on 2/26.

### [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72)

Sangwhan: Related to the other one?

David: Yes, related to the task queues thing. There is a pile of stuff that we should look into, that we haven't yet.

Dan: Sometime this week?

Kenneth: Related to Houdini?

David: Somewhat, like batching and flushing. People insert a lot of stuff into the pipeline and I'm not always convinced in terms of interop.

Dan: Breakout?

David: Probably. Would like to write tests, but not sure if that is breakout-appropriate.

(Discussion about scoping and whether or not we will break out.)

Dan: I think we shouldn't do a breakout during this F2F and revisit later after David has spent some time on this.

### [With credentials](https://github.com/w3ctag/design-reviews/issues/76)

Travis: Not sure if anything has changed.

Mike: We need Yves needs to be here for this topic. Also Tim.

Travis: I think a workaround was provided.

Alex: We did ask webappsec to provide a version of fetch that just goes and fetches. I'd like us to revisit it from that aspect.

Mike: Not sure if webappsec can do much here, since it's owned by a different group.

Hober: Is there a reason why this can't be done through a library?

Alex: It'll have to be an inefficient library.

Mike: Think y'all will have to discuss with Anne.

RESOLUTION: Extra time, revisit when Yves is here.

### [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101)

Dan: We've been kicking this around for a while. I believe Lukasz volunteered to work on this.

### [Serialization of i18n](https://github.com/w3ctag/design-reviews/issues/178)

David: I raised a couple issues, don't think we need to work on it during this F2F.

Sangwhan: Will give it a look later, but not as part of the F2F agenda.

### [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198)

Travis: Requested to take a second look.

Sangwhan: This was redesigned, so should be looked into again.

Dan: Breakout.

### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201)

Dan: Alex was on this.

Alex: I need to follow up on this again.

Dan: Any actions needed?

Alex: Think we should escalate a bit more in the direction of IAB.

Dan: Should we breakout and write something concrete and send it to them?

Alex: Yes.

(Discussion on action plan)

Alex: There is a email that I should/can follow-up on on this topic.

### [Link rel modulepreload](https://github.com/w3ctag/design-reviews/issues/213)

Dan: Alex is on this.

Alex: Have some concerns; mostly because this feels like a one-off.

Ken: What is different between this and just preload?

Alex: This traverses a graph, the other does not. Module preload might be the right thing to do, but what is the equivalent for CSS?

Hober: Not sure if module preload is the right thing for CSS.

Alex: I'm concerned about all these special case one-offs.

David: The other thing is link rel preload "as" foo. Why are these inconsistent?

Alex: They should be.

David: Are there any fetch options that do graph traversal?

Dan: So the consensus is that this is the wrong approach?

Alex: I think we have a gap here; it feels like we are plugging on specific case which isn't ideal.

David: Wrong approach vs wrong name for the feature.

Hober: +1

RESOLUTION: Extra time.

### [VISS](https://github.com/w3ctag/design-reviews/issues/234)

Dan: Looking at the feedback; feels like they think there isn't much we can do here at this point.

Sangwhan: Think we should close this one off.

Dan: During TPAC we had some feedback on the general direction.

(Discussion about protocol related work in W3C)

Dan: I think we should close.

RESOLUTION: Close.


### [We wish we had Service Discovery](https://github.com/w3ctag/design-reviews/issues/240)

Sangwhan: This is a bit macro, one part is about no consistency between discovery mechanisms and the other part is about no generic service discovery mechanism at all. Need Peter for this; probably should push to some other day and not this F2F.

Peter: +1


### [Layered APIs](https://github.com/w3ctag/design-reviews/issues/276)

Dan: Travis left notes in October.

Ken: Think Domenic was reconsidering this.

Sangwhan: I was told that this was being re-worked.

Alex: I believe there is work happening, not sure about the status.

Dan: Should I ask Domenic?

David: There is progress is package name maps, which is related to import maps.

Hober: But that is for stdlibs.

Alex: The naming of stdlib is a very live one.

Travis: Do we have issues on import maps?

Hober: Considering the work in TC39, not sure if there is much to do on layered APIs.

Alex: There are interesting aspects about for example, the virtual scroller. First time dash is mandated in a userland element. Do module maps have to be synchronously provided? Lots of questions remain to be answered here.

Dan: Hober thinks we should close.

Alex: I have some questions, can post on issue.

Dan: Let's post and ping Domenic.

RESOLUTION: Not for extra time, future telco.

### [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282)

Sangwhan: Someone in this office worked on this, think we planned to involve the implementor in this discussion.

Alex: Checking availability.

RESOLUTION: Extra time.

### [ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285)

Dan: Dave proposed a workshop on this.

Hober: This feels like the right people should have been part of the discussion.

Alex: Do they feel blocked by us (the web)?

RESOLUTION: Chair to discuss with Dave.

### [Offscreen Canvas new commit()](https://github.com/w3ctag/design-reviews/issues/288)

Dan: Pending external feedback.

Ken: Checking with WebASM folks.

Dan: So we are waiting?

Ken: Yes.

# Lunch!

## Discussion with MNot :)

DA: Ye 'ole IETF update? But more specifically QUIC or other interesting things going on?

MN: IETF met in Tokyo recently--came out much better than we thought. Figure mose folks are exhausted. Not full-stack interop, but at least lower-level interview. Got through the issue list... Will be changing the work mode to help folks get to interop more quickly. (Want to cut the churn in the drafts.)

DA: Link to the issue list?
MN: https://github.com/quicwg/base-drafts/issues


MN: Will know more where we'll be at about the middle of the year (on interop). Hope to wrap up in near future (+1 year). HTTP3 is not changing in how developers percieve the protocol. Changes are from TCP to QUIC... No lonter seeing TCP head-something blocking. 

MN: From someone using fetch (at that layer of API), shouldn't see a change.

DA: Useful for the TAG to help out? If so, how?

MN: We'd bring the TAG in if there was pressure to add new (or remove) new HTTP features. Not seeing that.

AR: Any change to origin model?

MN: Connection coalescing is an issue, but not really one for HTTP3 (it's pretty early issue)--haven't yet seen how this is going. There's a fair amount of complexity here.

MN: Other stuff... structured header work. Coming along quickly. Expect to ship "shortly".

AR: Last time, we talked about error reporting and a use case for arbitrary nesting. Will we see guideance?

MN: Guidance might be forthoming.. Will encourage (but not require) structured headers...

AR: We tried encouragement, but hit a wall. Would be nice to make the guidance more concrete that we could write in.

MN: See the FAQ in the doc. Look forward to your feedback.

MN: I may also consider adding a new type for JSON--but could be an "attractive nuisance".

AR: An encoded CBOR? Some other way of having nesting?

MN: Well, goal was to hit 80% case, and I think we did that...

MN: Unstructured headers...

MN: We're putting together the next HTTP workshop now. Fair interest in partial reliability, for things like QUIC. Discussion about the future of push...

DA: I hear about HTTP push... what's the real take-up?

MN: Folks who've tried it seem to think it's not as great as advertised, and difficult to use. May not be well suited for regular browser use cases. A lot of folks seem to think you get bytes for free when pushing, but in reality there's other congestion, and UA's know priorities better.

AR: Speculative push. "Cache digest" is a way of statistically letting the server know... 

MN: Cache Digest died a copule weeks ago--lack of implementer interest.

AR: Service workers let the client avoid pushing.. there's a technique on the server too... but it's a question of who does the bookkeeping.

MN: General concensus now, just leave it alone... From API POV, not a lot of interest from folks. Push is still relatively undefined--know one is really willing to put the work into making it better defined.

MN: Also, it would be politically hard to pull it out of the spec.

MN: Folks interested in traffic analysis. We encrypt all we can, into the handshake... QUIC is the next iteration such there's not a lot of data available--but traffic analsysis is still a think. Is there some mitigation that can be done, that would be a great push forward.

MN: Prioritzation in HTTP is another area we think we could improve. Best practices for current ones, or finding a new one?

AR: Dependency trees are still bad...

MN: Seeing a scheme like SPDY could help?

AR: Global ordering will still be figured about by the UA... Yoav's work on resource priorities gives us three levels, but still relatively unexplored. CAn't really go deep because HTTP semantics are unexplored.

MN: Dependency trees have been suggested for a while now, but really looking for data. Maybe it could be done in time of H3, but otherwise, we'll continue.

MN: Web Packaging; will be coming to Prague. Will determine whether we need a working group, but will need to come from the proponents...

DA: What aspects needs a WG?

MN: Signed exchanges have been in WG scope for a while... Bundling? If there is a tight linkage, could be a reason to keep them in one WG.

DA: Bunding's on our agenda.

Mike Smith: Would be good to have MNot in that discussion.

DA: 9am Tokyo.

MS: Joint workshop... still working on it. May have a venue, wondering about timing. Does it makes sense to gather feedback before or after the work goes to a standards body. We're probably in a different place re: the specs that we were 6 months ago.

MS: There's now an i2s from Google for signed exchanges

MN: I'm seeing feedback that Google engineers will bring from their deployment. 

AR: Expecting changes that are mainly compatible.

MN: Workshop: I think we've got reasonable agreement on the scope. Now wondering about whether want to standardize first or discuss first.

MS: Any comments about Client Hints, Mark?

MN: Client Hints, was self-contained spec, then Ilya/Yoav split off some of the hints into Fetch and other specs... Kept the spec in HTTP to be generic framework. Now seeing pushback from Mozilla saying it shouldn't go into fetch. Not sure what this means for client-hints in the long run. Seeing lots of hints in the industry.

SangWhan: Mark's take on Raw quic getting siloed into WebRTC world?

MN: Feedback from QUIC folks (re: protocols); this is not done yet.

SM: Should we think about exposing raw-quic as a socket?

MN: I'd rather build that power into the protocol.

AR: Doesn't address the useage for develoeprs that may want to do it... Binary data, push over websockets don't work particularly well. Ex: your stuck with websockets for many scenarios.

MN: many folks do that over H2 push...

AR: but not in user land. Doesn't have an API.

MN: It works

AR: It doesn't work

<fight!>

DA: OK, take it outside boys.

MS: Will need to get engagement from the securty folks for next-gen QUIC API.

MN: I think it would be pretty possible to switch WebSockets over QUIC.

AR: What about WebSockets over H2?

MN: I'd say just use WebSockets and wait for the protocols that power it to improve. May need to wait for extensions to access special properties of QUIC (partial reliability)

# TC39

KC: On classes

KC: Decorators are stalling... Folks afraid of abuse of the features. Looking to solve with tooling.

KC: JS standard libraries. Daniel tried to get feedback from dev-commuity, but got huge amounts of feedback.

KC: https://github.com/littledan/js-shared-interfaces/

KC: Trying to document the differences between browser JS and Node JS.

DA: Have seen that opinion is that JS is JS -- don't fork, please converge. There are vocal people on both sides who oppose.

KC: We're seeing TC39 proposals coming to TAG. This is good.

AR: There's some fear about how DOM can preclude language work. 

SM: Node folks wondering about creating a conformant version of fetch on Node? They'd have to "interpret" the spec, which they think is risky.

AR: Promises, fetch. (History lesson about AbortController)

DA: We should maybe encourage something into our design-principles...

YL: What's the status of streams? Discussions around Node + streams?

<nothing much>
  
DA: What other things (high-level) should we be considering?

SM: Was asked if we could weigh in on the standard library discussion?

AR: Well, know one is in a better possition...

DA: New issue.

AR: May want to put a frameing around it--that can be our most valuable contribution.

SM: Serializable objects, and lack of round-trip? Should we weigh-in?

DA: Let's ask for a TAG review!

DB: Decorators? Saw one explainer...

https://github.com/tc39/proposal-javascript-standard-library

https://github.com/littledan/proposal-operator-overloading/

https://github.com/littledan/serializable-objects

### [User Activation API](https://github.com/w3ctag/design-reviews/issues/300)

DB: User Activation API - API to expose user activation state. User Activation v2 - about changing the way the UA state is computed.

DB: One of my concerns is that many use cases are about sites that want to bake-in browser-specific behavior. (They want to emulate a browser's permssion model.)

DB: Ex: WebRTC perms in Chrome (maybe) depend on UA happening before asking for permission. Flip side, in Chrome, that permission is persistent. In Firefox, there's no UA pre-flight, but the permission is not persisted. Devs are authoring to Chrome. The site puts a button on page to get the User acivation. Totally unnecessary in Firefox. So, should this be in UA API, or maybe it should be part of Permissions API? E.g., more depth out of permission query.

AR: Sounds like feedback we gave to the permissions workshop: that request to review permissions is a permission. 

DB: Expose through permission API, rather than User Activation, so that devs can do the right thing.

TO: Is there a use case for UA API that *isn't* trying to work around the browser permission model?

DB: Might have been one... but I had to re-write it... may not be a clear use case.

TO: DB's use case seems totally reasonable. Exposing this API makes that behavior the default, vs. putting in permisssions API helps encourage the right behavior.

### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301)

DA: Hadley asked about this--no response.

MS: Richard Ishida also asked, and is not sure why this is necessary?

DA: Will put a comment to ping the author.

### [Review MathML](https://github.com/w3ctag/design-reviews/issues/313)

MS: Math work hasn't been active for quite a while. Not seeing a change in implementer interest.

AR: Yes, a change. An offer from Igalia to implement. So, we're open to it, if done right (spec, tests, quality, layering). TAG can help inform about modern spec, etc.

SM: Open question- whether MathML has a future?

AR: When we sat in on MathML on the web, they weren't interested in MathML. They wanted to make sure it was accessible, etc. Should address what it solves, etc.

MS: Another arch. issue about MathML... was maintainability of the code--root cause was MathML had a different display model that didn't fit well with CSS. It's different-enough from CSS.

MS: What problems is it going to solve to implement in modern engine. MathJax is already so good...? JS Perf is pretty good.

AB: The important thing for a11y is syntax. As long as syntax stays around in MathJax, then it can stay accessible. Thus it can be consumed by ChromeVox and MathPlayer... Not sure whether native vs. non-native would then make a difference. It's about what can be consumed--AT consume the markup.

YL: Leonie Watson pointed me to Math Braille. There was a 1:1 mapping with MathML?

AB: Yes, MathPlayer handles the translation. Important thing is the markup.

YL: Nothing in the rendering that would prevent the AT from working?

AB: Display can impact when the tool uses a highlight during announcement/reading of the content.

DA: We're still not converging. What should we be recommending?

AR: We have some feedback on record. We can relay.

SM: We can also suggest that some things are missing from the platform... stretchy brackets?

https://docs.google.com/document/d/1-Yp1dZUvAIKvg0qearliHM_XEuWrolYLH1Ui1pdAYXA/edit

TL: If folks want to final-review and post into the issue, that'd be great.

### [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318)

AR: Have some feedback that we'll paste into the issue.

### [Migrating some high-entropy HTTP request headers to Client Hints.](https://github.com/w3ctag/design-reviews/issues/320)

TL: Take to break out?

### [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321)

### [Querying Encryption Scheme Support Through EME](https://github.com/w3ctag/design-reviews/issues/322)

TO: This is great; Safari has a different encryption scheme than other EME implementations.

AR: Should try to line up with getMediaCapabilities()

DA: Take to breakout?

### [EME Extension: HDCP Policy Check](https://github.com/w3ctag/design-reviews/issues/323)

TO: Hmm, shouldn't do this. Privacy issue. Today the only sites that can detect it, must do playback. Need a relationship with the CDM. Adding the pre-check increases the fingerprinting surface.

DA: Is there some feedback you can add?

TO: About getting some specific performance metrics.

### [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324)

TL: have some feedback to write-up and discuss.

### [WebRTC DSCP Control API](https://github.com/w3ctag/design-reviews/issues/325)

DA (and others): trying to figure out what DSCP means...

DA: I'll drop a note.

### [Element Timing API for img](https://github.com/w3ctag/design-reviews/issues/326)

DA: Extra time.

### [imagesrcset and imagesizes attributes on link rel=preload](https://github.com/w3ctag/design-reviews/issues/329)

DB: If you already have link rel=preload as=image, then of course you want this... but maybe we need to question the original assumption.

### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330)

DA: Extra time.

### [Portals](https://github.com/w3ctag/design-reviews/issues/331)

DB: For Wednesday.

AB: Want to get Kenji for this too.

### [transferable streams](https://github.com/w3ctag/design-reviews/issues/332)

SM: Invite Adam to the subclassing of transfer streams discussion.

### [Web Bluetooth Scanning](https://github.com/w3ctag/design-reviews/issues/333)

DA: Knee-jerk--no!

AR: Say I want to setup an IoT device...

AR: What is the prompt that native apps ask to get the bluetooth infra?

DA: I question why we need to give this capability to the web? It's privacy-busting! Could enable a web app to know who's around you.

DA: Take to extra time. Need to craft a reply.

### Documenting our Process (Lore)

Dan: some to-dos for the "how we work" document - updating language, removing EWS stuff, giving better expecation of what people should be expecting from us.

## Breakouts (Group Awesome)

### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338)

DB: 1) Queues for managing the priority.
DB: 2) Parts that are important to implement in JS vs Internally

DB: One of the things I'm worried about... Some people are deferring work using Promises (read about this in the doc). This isn't the way that promises work.

DB: We have a bunch of APIs that schedule things, and developers may be chosing them for their familiarity rather than what their timing is. Perhaps we could decouple timing.

DB: What sorts of thing can you process on the task queue? Putting them into one queue system would be aweful because they all work in very different ways.

DB: How do we tie *any* of the legacy APIs into the task queues? Seems to be hard.

TL: The legacy APIs can't be used at the same time as these proposed new ones.

TO: If the intent is to add a new API that allows the web dev to schedule at any one of the exiting timeings... thens what's the value?

SM: Are these customers only frameworks?

TO: We could do for scheduling what fetch does for loading. Maybe that's where we can help?

DB: We could just let them noodle on this more?

### [Contact API](https://github.com/w3ctag/design-reviews/issues/337)

DB: Digging up all the legacy contacts APIs I can find...

TO: Given the history of failed attempts: what are you doing better this time; what makes you think this is better?

SM: Does an OS provide a way of partitioning the contacts? Maybe the API could provide a way to separate the request?

TL: Perhaps the spec should additionally specify a Permission entry (rather than user activation behavior.)

### [Heads up: Verifiable Credentials review request coming shortly](https://github.com/w3ctag/design-reviews/issues/335)

Taken up during the Tokyo F2F.

Thank you for letting us know. Please file a new review request when you have a specification ready to review. We will be closing this for now.

RESOLUTION: Close.

### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330)

KC: Sites that animate in content...spin images, etc.

TO: This shouldn't be a separate doc... really belongs in Web Animations, not as a monkey patch.

TO: How do they handle layout cycles? Scroll triggers layout, which changes scroll behavior, which changes layout...

TO: Section 5: Why did this get cut? Safari was able to show a prototype of this in the past? Too hard seems like a weak reason to me.

DB: Spec is still pretty vague

---comment--

Thanks for filing this review! 

We're excited to see this spec continue to improve.  It looks like there's still quite a bit that still needs to be filled out, and that's OK at an early stage as long as you're aware that there are a bunch more pieces that need to be written.  (For example, what happens if the `<time>` argument to `scroll()` is omitted?)

We note that the web animations spec has high coupling with this proposal... is there an intent to re-integrate into that spec in the future?

## Breakout (Group Modest)

### [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) 
Alex: is there a sandbox attribute for feature policy?  In the pointer lock example, what causes this not be the same thing as an extension to the syntax... 

Meta-discussion on articulating the user benefit in explainers.

Related to review request for feature policy https://github.com/w3ctag/design-reviews/issues/159

### [HTML Modules](https://github.com/w3ctag/design-reviews/issues/334) 

PUNT

### [Web Bluetooth Scanning](https://github.com/w3ctag/design-reviews/issues/333)

Dan: strong concern about the privacy issue.

