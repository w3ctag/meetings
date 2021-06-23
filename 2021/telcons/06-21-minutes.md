### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/06-21-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20210621T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @torgo
* [Canvas 2D color management](https://github.com/w3ctag/design-reviews/issues/646) - @LeaVerou, @atanassov
* [Design Principles PR: Prefer Simple Solutions](https://github.com/w3ctag/design-principles/pull/306)

### Breakout B (US / APAC) - [2021-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20210622T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Design Principles PR: High level vs Low Level](https://github.com/w3ctag/design-principles/pull/291)
* Proposed closed
  * [WebID](https://github.com/w3ctag/design-reviews/issues/622)
  * [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538)
  * [Early Design Review: document.prerendering](https://github.com/w3ctag/design-reviews/issues/613)
  * [Early design review: opaque-blocklisted-never-sniffed MIME types](https://github.com/w3ctag/design-reviews/issues/618)

### Breakout C (APAC / Europe) - [2021-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20210622T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Proposed Closed:
  * [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478)
  * [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524)
  * [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603)
  * [DFesign Principles PR: devices](https://github.com/w3ctag/design-principles/pull/320)
  * [Pre CR review request of CSS Multi-column layout Level 1](https://github.com/w3ctag/design-reviews/issues/634)
* [First Party Sets PR 45](https://github.com/privacycg/first-party-sets/pull/45) addressing some TAG feedback

### Plenary Session - [2021-06-23](https://www.timeanddate.com/worldclock/converter.html?iso=20210623T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* New privacy model finding

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2021-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20210621T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Rossen, Peter, Yves, Lea, Tess

Regrets: Amy, Kenneth, Hadley

#### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

Peter: wanted to make sure Lea & Tess got eyes on it...  Domenic's proposal limits realms to callables.  Seems like there's a library that allows you to emulate shared objects using callables.

[discussion on these options]

Tess: either way authors will end up with an API that sounds pretty nice and lets them do things they currently can't do.  Opportunity cost.  Right thing might be to take a step back.

[set to proposed closing and we can discuss closing comment at the plenary]

#### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @torgo

Dan: Multi-browser?

Tess: webkit did an experiment - have they addressed the issues?

Tess: one of the enginess proposing to standardize something that is happening - what the standardization change?

Dan: UA string not specified anywhere to begin with

Tess: maybe Fetch should specify it?

Dan: Mozilla position "[not harmful](https://mozilla.github.io/standards-positions/#ua-client-hints)."

Dan: they've listed [some feedback](https://github.com/WICG/ua-client-hints#challenges) from Safari's UA string freeze. 

#### [Canvas 2D color management](https://github.com/w3ctag/design-reviews/issues/646) - @LeaVerou, @atanassov

Lea: left a few comments - 

[discussiom of p3 color spaces]

[reviewing comments]

Lea: pretty satisfied with all of his answers. One small thing - `getImageData` returns sRGB data even with a p3 canvas - don't think that's a good idea but he said this has already been fixed.  One of the concerns I have - consistency with getContext.  I guess it's fine. you set the color space when getcontext is first called - subsequent calls return context already created even if the options are different - he said that's consistent with existing context attributes like alpha.  Not happy 8bit by default forever - but you can get away with 8bits in p3 though - there will be worse banding than sRGB but not super bad - so i think that's OK. 

Lea: colorspace attribute mutable ? arguments pro and against. right now it's immutable. if you wanted to extend to paint API we can't.  however we don't really need it there.  

Rossen: need to further review.  They would have the recreate only the predefined color space and 2d settings context?

Lea: you'd need to create a new canvas and paint the previous canvas on the new canvas. 

Rossen: from the use case - how often do you change color space...  either use initiartiated - moving to a different device - or changing the color settings...

Lea: It's unrelated to the output device. You *could* be working on a P3 canvas, on an sRGB device. You obviously wouldn't be able to see the non-sRGB colors in that case, but their coordinates would be unchanged.

Rossen: trying to identify the use case - when you would want to change the color space - it seems like it's pretty rare.  based on that the immutable principle will reduce complexity downstream.

Lea: Agreed, also it can be made mutable in the future if there are enough use cases.

Yves: if you're changing the color space you're better off creating a new canvas anyway...

Rossen: probably cheaper from a compute point of view.

Peter: could happen a lot by accident... e.g. some library might assume sRGB... 

Lea: that's what my concern was... You get back a P3 context not expecting it.

Peter: might be safer if it throws an exception ...  If I create a canvas in p3 and get rendering context in srgb - it could give me a context that is srgb and does the math - or it converts the backing image store.. losing data.

Peter: mutable would be problematic.  could potentially destroy data.  returning an unxpected color space could cause you to draw wrong color.

Lea: silent failure worries me.

Rossen: a long transition for libraries to get onboard with color management. 

Peter: safer: getConext gives you whatever space you asked for.... 

Lea: we don't want getContext to change what's displayed on the canvas - it should not be destructive.

Rossen: but how would the conversion happen?  

Dan: what should we ask them.

Rossen: if the getContext has the explicit color space - create a context and call getContext 2d - that assumes sRGB. From this usage point of view you can throw - and teach using a stick.

Lea: he made the point that browsers who don't know about the feature would not throw.

Rossen: but for them it will be sRGB anyway... Once the feature is there and supported - you expect the library to respect it or you don't support it at all which is fine because everything is in sRGB...   So teach [libraries] with a stick or carrot?  carrot would be don't throw an exception but do some kind of magic that converts the colors... 

Lea: what about the argument that this is the way alpha works already, so consistency. If you call getContext() with alpha: true and you have previously called getContext() with alpha: false on the same canvas, you'll silently get a context without alpha. No errors thrown. 2nd: we need to consider the case of 2 libraries working on the same context object... if the canvas changes the 1st library wouldn't know that - that would be messy.   Breaks expectations of existing code... 

Tess: In the current design the 2nd call to getContext returns the same context - we're concerned about the case where the 2nd caller doesn't know about new feature. Is it inspectable?

Lea: queryable using getContextAttributes - it's unclear to me whether an unsupported color space becomes sRGB or ... 

Tess: I think Peter's solution of returning a new context that does the conversion - a proxy - that would break the fewest sites. But color space conversions though not computational expensive it's non-zero. Ethical Web Principle of sustainability - making lots of extra calculation is not great.  Libraries don't get update so throwing sucks.   Visible bugs - color space conversion errors - visible bugs might cause someone to update the library.  Library authors shiould check the return color space - best practice.

Dan: that's where they're headed anyway...

[yes]

Dan: let's put it to proposed close and close at the plenary if appropriate.

ACTION: Lea to draft comment before the Plenary

###### Proposed comment:

Hi @ccameron-chromium,

We reviewed this proposal this week and overall we are happy with the direction. We were initially troubled by some of the design decisions, but after [discussing](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/06-21-agenda.md) them further, we came to the same conclusions. 

Therefore, we are going to close this issue. We are looking forward to seeing this feature evolve further.


#### [Design Principles PR: Prefer Simple Solutions](https://github.com/w3ctag/design-principles/pull/306)

### Breakout B (US / APAC) - [2021-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20210622T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Peter, Sangwhan,

Regrets:

#### [Design Principles PR: High level vs Low Level](https://github.com/w3ctag/design-principles/pull/291)

Stakeholders not in the call, punt.

#### [WebID](https://github.com/w3ctag/design-reviews/issues/622)

Both: Think this can be closed during plenary.

#### [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538)

Both: Think this can be closed during plenary.

#### [Early Design Review: document.prerendering](https://github.com/w3ctag/design-reviews/issues/613)

Ok to close.

#### [Early design review: opaque-blocklisted-never-sniffed MIME types](https://github.com/w3ctag/design-reviews/issues/618)

Sangwhan: Awaiting feedback on a question from Yves.

### Breakout C (APAC / Europe) - [2021-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20210622T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Ken, Amy, Dan, Lea, Hadley

Regrets: Yves

#### [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478)

#### [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524)

#### [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603)

#### [DFesign Principles PR: devices](https://github.com/w3ctag/design-principles/pull/320)

#### [Pre CR review request of CSS Multi-column layout Level 1](https://github.com/w3ctag/design-reviews/issues/634)

Dan: given [this](https://github.com/w3ctag/design-reviews/issues/634#issuecomment-847672934) feedback ...

Lea: not sure what we can do here..

Dan: let's close.

#### [First Party Sets PR 45](https://github.com/privacycg/first-party-sets/pull/45) addressing some TAG feedback

Amy: they are using "sites" vs "domains"  e.g. ""

> "**All sites** with use-cases that depend on cross-domain, same-party communication will be required to declare one (or more) sets."

vs

> "No domain can appear in more than one set."

Dan: also where does "origin boundary" fit in here?

Amy: also the submission process to the UA - 

Dan: would require a submission process for every UA... 

Amy: that's my concern.  it's open and they're not defining it right now - but given a potentially infinite numner of UAs.. difference for mobile browsers?... and what if different UAs ship different lists... what's the worst-case scenerio?

Dan: at the root of the whole policy thing... how allow lists get registered? is there an approach where such a registration process would not be necessary?

Dan: one central list? (like PSL)

Amy: I got the impression they wanted this kind of thing, with a third party to oversee it. But don't see all UAs agreeing on that especially privacy-preserving browsers...

Dan: then the issue of gracefully failing in the case of the browser not supporting fps?

Dan: also a question in privacycg - what's to stop large websites from penalising users that come to their properties, with FPS off or with a browser that does not support it by saying you can't get the full experience

Amy: like turn ad blocker off or we won't show you this... also older browsers...

Dan: could they design the system ... so that it would make it less possible to do that... 

Amy: mitigate the potential fragmentation.

Dan: bit about same origin policy.. first party cookies can't be shared between origins in the same set? confusing?

Amy: for same-party cookies..

Dan: [leaves comment]. This comes right after "browsers may consider using FPS in new privacy features..".. so this provides a new mechanism.. it's true that IndexedDB databases wouldn't be shareable, some new kind of thing/database that we are allowing access to, while we might say the people creating that new api might choose to give it the FPS security characteristics

Amy: static lists being unscaleable if this is possible for any/all sites to use.. needs the verification process for preventing abuse, but registring with UAs creates barrier to entry and scaleability issues.

Dan: registration of FPS is essentially a commercial activity.. something businesses want to do to make ops more streamlined, to build sites that operate along their business rules.. what happens if there's an economic embargo against a country and a site provider in that country wants to register a FPS... possibility of fragmenting the web this way.. Not clear what the abuse cases are of there not being a static list

Amy: about verification.. if a bunch of small ad comapanies got together and declared themselves a set .. doesn't pass the test of first party setness... 

Dan: comes back to how do you determine what is the same org..?

Amy: UAs all get together and decide on their policy rules and write it down, they just haven't yet

Dan: I can't envision what that would be

Amy: agreed

Amy: sites self-declare then UAs would crawl that to see if sites still declare and then check it against a centralized list to see if it's not an abuse case and then will let those sites share same party cookies... Somewhere it's declared in their well known and then they have to go to each UA and register... maybe UAs have heuristics to not depend on the central list all the time for verification on the fly? but not clear how it fits together or where the dependencies are

Dan: the proposed criteria for domains being in an approved first party are: common owner, common controller, common group identity easily observable to user, common privacy policy.

Amy: not automatically checkable

Dan: and none stops a bunch of ad companies banding together to create an ad network that uses FPS in order to get around blocking third party cookies. All those sites need to do is create an association that holsd the domains in a trust and agree a privacy policy

Amy: same logo in corner of every site as a visual indicator for the user

Dan: if there's no way to stop this, the anser has to be don't ship it or ship it with no verification system, no registration system, and rely on a technical means to mitigate against the abuse cases that we don't want people to use this for. If it's not meant to be used by advertisers for this, design it in a way that it can't be used by advertisers for this.

... The question is: is there a way that this technology could work without needing a registration system at all? That would eliminate the need for a centralised static list of any kind, would eliminate the need for registration with different UAs, would eliminate the centralization issue, and it would eliminate a lot of compleixity in how it works. It's not clear that the registration criteria that the PR talks about would stop the kind of abuse case that we envision, specifically ad networks using this technology effectively as third party cookies after third party cookies have been deprecated. Given that, would it be possible to design the technology itself to mitigate against those abuse cases? So you wouldn't need a registration system in the first place.

Amy: would leave it up to the UA to decide on the fly - and doesn't preclude UAs from getting together to agree on a policy.  Either all the UAs agree on the same criteria (same as Disconnect situation) or they don't and we get fragmentation...

Dan: would limiting the number of sites possible in a first party set help to mitigate against a FPS misuse? Completely arbitrary number.

Amy: would be interested to hear more from other stakeholders who support this. Will ask on our issue

Dan: two open issues that link to ours... technical only enforcement of UA policy (their 43)

### Plenary Session - [2021-06-23](https://www.timeanddate.com/worldclock/converter.html?iso=20210623T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Tess, Dan, Rossen, Dan, Hadley, Yves, Amy, Lea

Regrets: Kenneth

#### New privacy model finding

#### [Design Principles PR: High level vs Low Level](https://github.com/w3ctag/design-principles/pull/291)

Peter: merging with alan kay principle?

Tess: we discussed and agreed they are distinct

Rossen: action on Lea and me to wordsmith the final proposal and then go from there. 

[will try to agree on the chat to merge - async]

#### Breakout B Timings

Peter: Hour earlier? 

[agreement to move it an hour earlier]

#### Breakout Rollup

##### Breakout A

Tess: Talked about **[Realms](https://github.com/w3ctag/design-reviews/issues/542)** - may be overtaken by events - alternative proposal - we agreed to propose close and propose a comment asking them to come back to us when the dust settles.

Dan: also wanted to wait for comments from Ken. However I feel like we should not prolong, but just close it. We can reopen if Ken objects.

Tess: sounds good

Tess: I'll write comment.

[closed with comment](https://github.com/w3ctag/design-reviews/issues/542#issuecomment-866932393)

Dan: we talked about **[UA strings](https://github.com/w3ctag/design-reviews/issues/640)**... 

Tess: this is the case where chromium engineers proposing partial freezing of UA string and adding client hints. Not clear to us if they had taken into account partial UA freezing other agents are shipping.  To what extent do the partial freezings align vs diverging?

Dan: I asked for more data on that and haven't heard back. Firefox are already doing partial freezing, I noticed the UA seemed to indicate windows even though it was Mac. They're doing some normalisation of the UA strings.

Tess: **[Canvas 2D colour management](https://github.com/w3ctag/design-reviews/issues/646)**.. big topic. Ended up coming to the same conclusion they did on the right behaviour for a subsequent getContext. You call getContext and it displays display p3 and another library calls it after without it... ended up where they were anyway. Agreed to propose close. Lea drafted closing comment.

Lea: haven't posted it yet. Rossen wanted to take a closer look, and something i wasn't sure about - if authors use an unsupported colour space what happens? It throws in that case. 

Rossen: wonderful, that's what we wanted.

Lea: no way to get the list of supported colour spaces, besides try catch multiple and see if it works.

Rossen: is that a bug or a feature?

Tess: sounds like a feature to me

Rossen: reducing entropy

Lea: given that the number of supported colour spaces can be determined based on browser version I'm not sure how they're increasing fingerprinting vectors.

Rossen: I don't know. Generally when it comes to increasing entropy always erroring on being conservative. Initial gut reaction is to challenge adding or extending this. To your point, a lot of the colour spaces could be tied in to combination of browser and version.. don't kno wwe're strictly increasing entropy in this case. Can't really rationalise it for myself that we're not.  With my conservative approach I'd err on the ..

[reviewing lea's comment]

[nodding]

##### Breakout B

Dan: talked about high vs low already. **[WebID](https://github.com/w3ctag/design-reviews/issues/622)** - we think this should be closed in the plenary. Close it?

Hadley: not disagreeing

Dan: We've been asked for feedback, provided some in the session we held, do we know that they are doing a CG?

Tess: there's a charter that Heather (?) has been working on. I think they are going to start a CG, active work.

Dan: closing comment should be come back when this group has output that we can review. Not that we're done. Sounds good, headed in the right direction, come back with specific drafts.

Hadley: that's what I was aiming for in my comment.

Dan: we should be more explicit.

Rossen: we support the problem framing and proposed direction, given that this is more or less a grouping and introduction of an area that encopasses a lot of features, we look forward to helping you evaluate and review individual features as they come along. Re-reading the last sentence one more time makes me happy, thank you Hadley.

Dan: closed? closed.

Dan: also proposed close: **[referrer handling](https://github.com/w3ctag/design-reviews/issues/538)**.. 12th oct last year..

Rossen: why didn't we close it?

Dan: I don't know... 

Rossen: write a comment that it must have slipped off the radar, but discussion was done a long time ago?

Dan: [closing comment]

Dan: proposed close: **[document.prerendering](https://github.com/w3ctag/design-reviews/issues/613)**

Peter: I gave feedback they're taking on board, really early review, so I'm fine closing this.

Dan: **[never-sniffed mime types](https://github.com/w3ctag/design-reviews/issues/618)** - Sangwhan said waiting for feedback from Yves

Yves: after discussing with Sangwhan I figured out that equivalent of the + something is implemented by the essence of mime type definition. Seems okay for me. Close successful.

##### Breakout C

Dan: didn't talk about miniapps because sangwhan needed to be in that.

Rossen: I'd love to be in that in the future

Dan: issues have no milestone. Talk about them next week? **Media stream insertable processing using streams** set to proposed close.. Sangwhan left the last comment. We didn't get to it. Bumped to next week.

.. Design principles PR on devices.. didn't get to either. Milestone for design principles week.

.. **First party sets PR** is where we spent most of our time. Left some feedback, had no engagement so far. We tried to prompt them on this thing about what if there wasn't a registration system at all, could there be a technical only enforcement mechanism that doesn't allow for the misuse in the way they don't want it to be misused rather than having to have a registration system which would centralise things and has scalability problems. And the question remains what's to stop sites from penalising users for using browsers that block FPS in the same way they do to with ad blockers. "Please upgrade your browser to use this site". Third thing was they say it doesn't change origin because cookies would behave thes ame way.. a.example can't read b.example's cookies. But don't mention this other thing, same-party cookies, which would allow a.example to read b.example's cookies. So why doesn't in a FPS world just replace third party cookies? We're back where we started. 

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22)

