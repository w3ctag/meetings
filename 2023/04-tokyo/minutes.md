
# First Day

## 1a

Present: Dan, Sangwhan

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831)

*triaged and assigned issue to us and labeled it*

Sangwhan: I think this is very useful.  Multi-frame forms seem very complicated.  Dan.com can say "sangwhan.com is my trusted payment provider so sangwhan.com forms can be autofilled if they are embedded in dan.com"... The pattern itself we need a long-term solution for .. because this is too convoluted.

<blockquote>

Thanks for bringing this to our attention. We looked at this during our F2F, and overall we are happy with this. It solves an immediate user need, which is being able to autofill cross origin forms, which as far as the user is concerned should work like any other form.

We have two concerns here, both of which are likely out of your immediate control but would like to see some progress on.

1) Interest from other implementors. This seems like a useful, safe feature which would be more powerful if at least one other implementor is interested in implementing this (setting aside the depedency on permission policy, which is a dependency).
2) We do see the immediate reason *why* multi-frame forms is a thing, but we would like form domain experts to think about a future direction where we move away from this somewhat convoluted architecture. We understand the proposal is working around layers of limitations, but we feel like it shouldn't be this way.
3) In an ideal world, the solution to (2) might be web payments.

</blockquote>

Dan: +1

### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795)

Sangwhan: compute pressure makes a lot of sense. the new design is good. the re-design driven by Ken.  Some privacy concerns.  I think every new capability feature we have to think about the potential trade-offs. The immediate user need is...

Dan: You read my mind.

Sangwhan: if you are web app that is compute heavy - or a video conf that has background blur - the applications dont know when the CPUs are starved. The apps can take away certain non-critical functionality to serve the needs of the user. E.g. non-critical features in video conf deprioritised compared to hearing the person... If they know how much pressure they can adapt. Right now on the web there's no way to adapt. On top of that you have artificial compute pressure - e.g. battery saver - you're trying to save resources. Compute pressure is a way to convey that... Some level of concerns from app implementers that the level of info exposed is not enough - but this is a good compromise...

Dan: is there a permission required for even this level?

Sangwhan: no.   You can use compute presure as a way to expose info... 

Sangwhan: i have a conflict of interest as I work on this topic in ChromeOS. 

Sangwhan: from a user and application dev pov - it sucks if the app is just blasting the CPU... 

... [621](https://github.com/w3ctag/design-reviews/issues/621) was the original issue.... A lot of privacy discussion happened on the previous one.  They are aware of the privacy concerns....

Dan: from [their privacy considerations](https://w3c.github.io/compute-pressure/#security-and-privacy-considerations) it looks like they are excercising [data minimization](https://www.w3.org/TR/privacy-principles/#data-minimization)... one of our privacy principles...  Also lots of other mitigations against privacy issues listed.

Sangwhan: one thing that may be a small concern is syncronization... 

Dan: You could establish cross-origin correlation... I think that should be discussed in the privacy consideration section...

Sangwhan: it would be a very expensive way to do it...

Sangwhan: Overall we see the developer needs are pretty clear. 

Dan: data minimization important...

Dan: what's the problem with doing this as a permission gate?

Sangwhan: most video conference apps have to ask for 3 permissions already... how you would convey this to average users is really tricky... 

<blockquote>
 
Positive feedback on data minimization approach detailed in the privacy & security considerations seciton - see [data minimization](https://www.w3.org/TR/privacy-principles/#data-minimization) for our emerging work in this area. Also the user needs are well defined in the explainer.

We'd like to hear what the developers think about how useful this is especially in multi-core (especially heterogenous) setups, once it moves on to trial.

We noticed that WebKit position is WIP, could you poke that thread and see what they think?

</blockquote>

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772)

### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805)

*we discussed some issues the current state of the review and process - e.g. lack of an expaliner and any prviacy & security considerations section*

## 1b

Present: Léa, Yves

### [TAG review of the proposal to use the RegExp `v` flag instead of `u` for the HTML `pattern` attribute](https://github.com/w3ctag/design-reviews/issues/832)

Some pause wrt backwards compat, but after looking into what the `v` flag can do, we think the tradeoffs are very worth it.
Very little breakage, in very few cases, and very little harm in these cases, since client-side validation is a hint anyway.

Propose closing, and plan to close in Plenary.

<blockquote>

Hi @mathiasbynens,
  
@ylafon and I looked at this during a breakout today. While we were slightly concerned initially about the backwards compat implications, we do think the benefits `v` brings far outweigh these concerns, and we are happy to see this go forwards.
  
Thank you for flying TAG!
  
</blockquote>


### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829)

Lea: WRT [csswg-drafts/#4441](https://github.com/w3c/csswg-drafts/issues/4441) very glad they resolved the way they did instead of adding extra syntax. This is intuitive for authors, does not require learning anything else, and performant for UAs, win-win.

...: WRT [csswg-drafts/#6429](https://github.com/w3c/csswg-drafts/issues/6429), this seems reasonable, but we see there is a lot of discussion after the resolution to adopt this proposal. Are the details still being fleshed out? If so, is it a good time for shipping this?

...: Note, dialog example explainer has a bug, `step-end` will only work one way.

... WRT [csswg-drafts/#8174](https://github.com/w3c/csswg-drafts/issues/8174), agree that use case should be solved.
A bit concerned that `initial` would be confused with the `initial` keyword, which is an entirely separate concept. 
Agree with @nt1m that this seems designed around browser engine internals rather than concepts web developers understand. 
Agree that there should be a way to animate newly inserted elements that does not also animate them if they are present when the page loads.
Missing an actual definition for this `@initial` rule that people started talking about at some point.

Yves: Definition in https://github.com/w3c/csswg-drafts/issues/8174

Lea: That's the one I was looking at. Discussion goes from `:initial` to `@initial` but I cannot see any proposal or strawman for the latter.

Yves: Would be good to have a concrete proposal for `@initial` (or whatever name is chosen) 

... WRT [csswg-drafts/#8389](https://github.com/w3c/csswg-drafts/issues/8389), `inert` CSS property seems useful, and explaining HTML `inert` attribute in terms of that is good practice. Unfortunate it was resolved against, as now developers have no means of opting out of this behavior, but this is better than not having the behavior at all.

<blockquote>

Hi @josepharhar,
  
@ylafon and I spent quite some time during our Tokyo F2F looking at the various issues, and the explainer.
  
Overall we like the direction that this is going.
Designing a solution to this problem as small independent improvements on existing features that can together be leveraged for entry and exit animations is a good practice.

We also like that existing transition syntax could be leveraged to do the right thing, rather than introducing new syntax.
We see discussion went from `:initial` to `@initial` due to specificity issues (?), but we could not find a definition of what `@initial` is/does. We are also concerned that the name will be confusing for authors, as `initial` is an existing, unrelated concept in CSS (initial values).
  
Making transitions to `display: none` inert seems preferable, though it is unfortunate the `inert` property was resolved against, and thus authors can not opt out or use this behavior for other use cases.
  
For some of these issues (e.g. 6429) there seemed to be still active discussion after any resolutions, making us wonder if shipping this might be a little premature.
  
</blockquote>

### [Spec review for Scroll-driven Animations](https://github.com/w3ctag/design-reviews/issues/828)

## 1C

Present: Peter, Tess

### [scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/827)

Concerns about multi-stakeholder commitement to the underlying model.

Left feedback about intention of options params (e.g. can it be implemented without the rest of the scheduler changes?), and conflict with abort signal naming.

### [COOP: restrict-properties](https://github.com/w3ctag/design-reviews/issues/760)

Peter & Tess worried (yet again) about how, in a post-Spectre world, there are many knobs web developers / web server operators need to turn in order to regain access to features like `SharedArrayBuffer`, and with proposals like this it feels like we keep adding more knobs.

It would be great if there were a one-stop-shop document that spells out, in as straightforward a manner as possible, what a web developer needs to do, and for such a document to be maintained as more knobs get added. Perhaps we should spin up a TAG task force to do this? Perhaps such a task force could also tackle [Overall review of features which enable/disable subframe or subresource capabilities #525](https://github.com/w3ctag/design-reviews/issues/525)…

### [Pre-CR review: HTML Review Draft — Published 18 January 2021 #657](https://github.com/w3ctag/design-reviews/issues/657)

Closed.

### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

Discussion about the conceptual overlap between these feature controls and the Spectre/Meltdown mitigations, wondering if the same task force that looks at CO* headers should look at these controls. Ideally maybe a common control layer can be created for authors to enable features that also mitigates Spectre/Meltdown under a layer of abstraction.

## BFCache Discussion

Present: Dan, Peter, Sangwhan, Tess, Yves, Lea
Guests: Rakina Zata Amni (Google), Fergal Daly (Google)

Sangwhan: how can we help with the bfcache...

Fergal: interaction with web transport... someone asking "do we care about befache" - it would be good to have a clearn statement that the web platform does care about bfcache...

Dan: **recording decision to request a TR space URL bfcache guide** 

*discussion on what that should be*

**we agree /TR/bfcache-guide**

Dan: is it named in any standards yet?

Fergal: no not yet... but nobody has objected... salvageable...

Rakina: i think after domenic and others re-wrote the history in whatwg it mentions bfcache...

Dan: mozilla's pov?

Rakina: we got the mozilla and webkit teams to review our bfcache guide.

Tess: we should always get reviews from other implementers...

Dan: should we amend the template?

Lea: i would be worried about expanding it.

Fergal: it's also not relevant to a lot of specs...  One possibility would be to change the template - sections, e.g. navigation... 

**discussion that people are using outdated version of the security & privacy questionnaire**

Sangwhan: where bfcache is a little specific... this is part of wide review... bfcache not included in wide review.

Tess: part of wide review we're supposed to be doing -- not in itself and area of horizontal review.

Lea: can we define what kind of APIs this refers to?  We could in the future have a more dynamic wizard instead of a static templat that shows appropriate questions depending on the type of feature, in such a thing it may make more sense to include a BFCache questions, only where relevant.

Fergal: not-relevant would include CSS, rendering. Relevant would be navigation, or state - stored, state... 

Lea: can we document the answer to this somewhere so that we have this info if/when we move to a more dynamic issue template?

Dan: I've documented it in the minutes

Fergal: the end state is looking pretty good.... The concern I have is that APIs go through review and should have been flagged as needing bfcache specification and it isn't... don't know how much awareness there is 

**discussion of checklist of principles**

Sangwhan: we should apply this... 

Rakina: with web transport thing - the feature already shipped - 

Sangwhan: web transport is chrome only?

Yves: it's in latest firefox... 

Dan: did we do a review on web transport?

Sangwhan: before we started to care about web transport.

Yves: they will ask for wide review soon. in Nightly.

Fergal: the API is not incompatible with bfcache... Changing this before it becomes widely adopted would be good.  If people don't implement a close handler then it will be broken ... 

Yves: how is it done for web sockets?

Fergal: it's blocked - the reason we haven't pushed on that is that websockets is widely deployed. we don't want to break a lot of stuff.. But with web transport it's the right time... people experience the interaciton with bfcache...

Sangwhan: retroactively allow apps to opt into bfcache?  (web sockets)  If they want to have an extra level of lifecycle management... Feels like ...

Fergal: on websockets - obvious thing is to close the socket ... it should correctly handle going into bfcache and going out again...  But on webtransport side of things I'd rather people don't have to opt in.

Sangwhan: i think we can just weigh in proactively...

Sangwhan: BFCache x WebTransport: https://github.com/w3c/webtransport/issues/326 

Fergal: another discussion about broadcast channels. firefox & chrome work.. safari ... we think either give the page ... correct behaviour (as if you hadn't gone into bfcache) - you assume that you've either got all the messages or be reloaded... we should have a reliable platform... waiting for a response from webkit...  I would like to have a statement that "currently reliable things can be treated as fully reliable even if you go into bfcache"...

Fergal: sometimes we have a choice.. go with the status quo or spec that the broadcast channel is unreliable.. 

Dan: should that belong in the bfcache guide?

Fergal: going forward I'd like it to...  Chrome has been conservative. we block bfcache in "interesting" situations... feel webkit has been less conservative....

Tess: not many bug reports... For places where the status quo is inconsistent ...

Fergal: for new APIs I'd like that....

Rakina: we do have a "discard non-fully active documents for situations not supported"

Sangwhan: the messaging ...

**sangwhan takes on TAG owner of the bfcache guide**

### [permission policy unload](https://github.com/w3ctag/design-reviews/issues/738)

Fergal: main concern raised - stops the inner page from executing code that may be imported...  I need to update .. in the last few days I've written a change that flips to to default off and you can opt back in to unload working again.  Could be quite disruptive...   The main concern raised there .. there may be sites that depend on the unload handler executing in subframes..  logic that should fire when those subframes are destroyed.  We're adding code to see how often that happens... hopefully it will be small and we can document that.  then we would like to gradually roll it out so by the end of the year unload handlers are off by default.. 

Tess: and some kind of Telemetry of opting back in.

Fergal: spec: you run unload handlers unless the page goes into bfcache...  So firefox, chrome, safari on mobile all skip unload if page goes into bfcache... we don't see an easy way to transtiion 99% we will load the unload handler to 60%... it's unpredictable ... something in the subframe would block bfcache... 

Dan: end user experience of failure mode?

Fergal: all the documentation pushes you away from using unload handlers anyway... Most unload handlers don't do anything visible for the end user.. people are sending back telemetry... it's not users seeing an impoact from this. It's sites, ad networks... we've pushed the major vendors away from unload... 10 t 20 % pages on desktop that ...

Sangwhan: any common libraries?

Fergal: we worked with facebook.. we talked to a lot of the third party libraries...  One answer is to make it unreliable... but getting there from where we are is not pleasant.. if we're gonna end up breaking things let's break them more visibly so people who do care will get a signal that the thing is broken...  Where unload is now opt in.

Tess: in webkit we did make this change and we didn't have any blowback... 

Fergal: it can do weird things like bias your data in weird ways...

... tried to find out from vendors if they noticed any skew... in data... it should give them more accurate data. don't have any responses yet..

### [bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786)

Fergal: another thing - cache-control no-store.. If you set cache-control no-store then it doesn't go into bfcache.. e.g. on mdn. but deleted from mdn. No longer good advice. It's a large blocker... across all the browsers... what if we just monitor cookies .. if we see cookies changing then we don't restore from bfcache... a few other ideas... End proposal is: you tell us what cookies you care about and if any of those change then we evict your pages, and if we see you using the authentication header at all then we evict... This is kind of risky... don't know if that covers everything... 19% pages on desktop blocked from cache-control no-store. If you don't tell us what cookies you care about then we default to all https cookies. 

Tess: what group?

Fergal: not in any...

Tess: wicg? requires statement of interest... 

Dan: would be good to see it going to a venue...

## Packaging Discussion

Present: Dan, Yves, Tess, Sangwhan, Lea, Peter, Max
Guests from Chrome: Kenji, Patrick Meenan, Javier Visiedo,  Jiachen Guo, (xxx Chrome team)

Kenji: We have a deck about compression dictionary... can walk you through that..

Patrick: at a high level we're walking away from packaged bundles with specific APIs and moving towards delta compression at the transport layer... so they can use whatever packaging people use today but whatever goes over the wire can be a delta in whatever has changed... Something we're working on and trying to ship for a few decades... atomic incremement. If you change ine module in  your webpack build then you ship the delta.

### Brotli

Kenji: brotli presentation at IETF... not the first time people have tried this... 

Patrick: another thing when we first shipped h2 - delta transmissions - but was abandoned.  

Yves: when they changed to hpack...

Patrick: yes because of side-channel timing attacks.  The side-channel attacks made it so things compressed across streams was readable across stream... 

Kenji: *brotli* 20-30% compression rate.  Tighter security model, better layering, dictionary scope, deployability...  

Patrick: Security model - operating on a per-resource basis... Both dictionaries and compressed resource need to be CORS readable ... handwaving away the side channel attack but requiring resources to be readable by the client.  Layering the dictionary negotiation as separate from the actual content encoding.

Yves: cacheability of all of that?  Does the client cache only the uncomrpessed version?

Patrick: the dictionaries expected to be cached... vary the responses based on the advertised client dictionaries... What we've tested so far  with delta compression... 10 to 50 times smsaller than shipping the full version of the JS... 

*presents flow diagram*

...at build time app developers build compressed versions for delivery...

...issues around CDNs... sinc they can't read the delta compressed versions of resources...

...most of cases we've seen dictionaries compress fairly well... the "cost" of downloading the dictionary is made up for with the savings over time for pages, etc...

...we're seeing html pages 50%-60% smaller commonly...

Yves: h2 push?

Patrick: gone as far as we're concerned... the problem is it doesn't have visibility of what's in cache...

(scribe missing)

Peter: So you will build the tooling?

Patrick: Yes

Patrick: tooling also tooling for CDNs

Peter: dynamic compression... require support on the sevrer... ngnx plugins?

Patrick: my expectation is that most will be the static case where people can add it to their build pipeline... A lot of companies that will see the big benefit - don't use off-the-shelf - some work with all of them to make sure that the brotli or z-standard apis...

Peter: just concerned... about how long ngnx takes to add quic support... should be not just for amazom, facebook, CDNs... 

Peter: you're requiring CORS headers... doesn't help about side channel attacks.  If I can grab TCP packets - the common side channel attack on compressed data over TLS - looking at the size of the data... that would be still possible.

Patrick: it doesn't offer new protections...

Peter: most best practices turn off compression over tls... 

Kenji: if you have private info ... you wouldn't put it there...  

Patrick: the assumption is that response is readable by the client...

Peter: this will incline people to not run this on dynamic content...

Patrick: correct... 

Peter: that should be disclosed as a threat...

Sangwhan: how would this work when you're transporting over websockets, web transport,rtc....

Kenji: not specified

Patrick: brotli and gzip both streaming compressions..  

Dan: any feedback from IETF / Mark Nottingham

Patrick: yes that's the main person we've been talking to...

Sangwhan: multiple codecs?

Patrick: we're positioning this as dictionaries rather than shared brotli... 

Kenji: for static use case built into tool chain...

Patrick On calls from positions - lots of people weighing in. I'm assuming many are waiting to see how it goes in the wild...

Yves: for static public use case... the saving should be the same as a crompressed archive vs indidivual files...

Peter: over the long haul we'd like to see bundling isn't so much of a thing... let's say I use 100 little files and rely on QUIC to handle that. Will the delta compression still be a win?  At the transport layer you can take a look at a set of files...

Patricl: we tried to ship that when we di H2... it's possible something like that can be done. I expect we will be in a world where packaging needs to be done... 

Peter: doesn't work well for images?

Patrick: no - and for fonts there is a separate spec for fonts.. 

Patrick: we expect WASM to use this a fair bit.

Peter: very positive on this... 

**TAG review request will be filed**

### Packaging

Sangwhan: miniapp packaging... some people want it. epub is another package format.. we've been going around suggesting exchanges. it doesn't seem like there's been much .. curious : if this isn't being worked omn then maybe we shouldn't send people in that direction... 

Kenji: it depends.. signed exchange assumes origin and verifying.. 

Dan: lots of complexity around signed exchanges... as well... 

Kenji: the idea of having a zip file... is appealing... for an ecosystem like miniapp... 

Dan: can we have a simple package + origin?

Peter: this is the path that signed exchanges started on but then became too ephemeral. It would be nice to have a code-signing cert that verifies back to the same origin as tls does

Sangwhan: isolated webapps proposal...  more "secure" context... https://chromestatus.com/feature/5146307550248960 If we can come to some level of agreement on where we want...

Yves: hashes in the domain record... not the same level of security but one level of security ./..  But you wouldn't accept for a banking app...

Sangwhan: TWAs on Android...

Yves: **Universal link** on IOS, **Android App Links** on Android

Sangwhan: we could copy the ACME approach.. verifying ownership...

Dan: many applications now require security ...

Tess: any messaging function in an app...

Yves: zip inefficiency  is not particularly an issue for miniapp

**much discussion on miniapp, signed exchanges, etc...**

Peter: a week ttl is not tenable for things like miniapp... Also letsencrypt certs get expired every 12 weeks..  you could have a counter-signatory with a longer lived cert

Peter: when I go to letsencrypt I verify my domain through ACMe but maybe I can use something stronger to verify my identity and it's longer-lived but also associated with my domain, maybe the longer lived cert countersigns the web server's cert... for installation of a package...    that's the holy grail .. a package that claims to be from an origin, it's verifiable... is treated as the same origin. Browser treats it the same.

## Findings

### [Web Without Third Party Cookies](https://w3ctag.github.io/web-without-3p-cookies/)

Lea: definition of collective privacy - 

Dan: should be a link to https://w3ctag.github.io/privacy-principles/#collective-privacy

Yves: should we list google's planned deprecation of 3rd party cookies?

Peter: in section 2 first paragraph some text that doesn't track properly.

Lea: I'm a but wary of restricting general solutions ...

Tess: What we know is that general solutions are problematic...

[Discussion about the pros and cons of specific examples in the doc]

Dan: https://github.com/w3ctag/web-without-3p-cookies/pull/6

Sangwhan: it's better for the web - to deprecate - that's why Chrome wants to do it.

Hadley: Lots of good stuff here... hard to pick out the message... lots of individual points... the beginning of the section leaving the web better... we start by saying not what we're going to talk about... 


Start section 4 with:
```
We support deprecating third-party cookies from the web platform, and we embrace the opportunity to improve the privacy features of the web. When we review new technologies to replace third-party cookies, we need to ensure that the replacements do not recreate the same downfalls to privacy. 
```
And then move this paragraph to before the last paragraph: 
```
We are strongly in favour of innovations to build sustainable business models on the web platform, but an in-depth discussion of the various possibilities are outside of the scope of this document. From an architectural standpoint, web standards should avoid encoding particular business models that are available to authors, publishers, and web content creators.
```

## Roll-ups

Present: Dan, Sangwhan, Tess, Lea, Yves, Hadley, Peter, 
Guest: Florian


### 1a 

Dan: *summarizes 1a*

Compute Pressure - 

Tess: concerned about detecting the machine is idle so you can start doing more compute-heavy stuff... I'm just wondering - by carving out to schedule extraneous computation are we encouraging web sites to drain users' battery.  Will leave a comment on this issue...

### 1b

Lea: *summarizes 1b*  

### 1c

Tess: *summarizes 1c*

Tess: for coop restrict properties maybe we need a task force to create a document that talks about sharedarraybuffer and what you need to do in a post-spectre world.

Dan: this would be a perfect topic for https://www.w3.org/2023/03/secure-the-web-forward/

Tess: also closed 657

Tess: also on 525 - this is similar to the task force idea...

Peter: maybe we combine these 2 fundamental issues - a ahigher level of abstrction for flipping features on or off.. a new abstraction layer to gate all of these types of things....

# Second Day

## 5a

Present: Lea, Sangwhan

We discussed Class vs Behavior. Our conclusions are recorded in https://github.com/w3ctag/design-principles/issues/11#issuecomment-1515585583

We also looked at these PRs, but they need rebasing to be reviewed properly, and we are not sure about whether the changes are an improvement:
- https://github.com/w3ctag/design-principles/pull/412
- https://github.com/w3ctag/design-principles/pull/409

## Design Principles Plenary

Present: Dan, Lea, Sangwhan, Tess, Yves, Peter

Sangwhan: trying to introduce a principle on when to use classes vs objects...

Lea: I started a draft PR but not sure I agree with this.. Recorded the jist of our discussion here: https://github.com/w3ctag/design-principles/issues/11#issuecomment-1515585583 ... classes that only have data could evolve to mutate the state ...  When the input of an API is a data centric object the API should object it... We think that's a good pattern. Also the webRTC thing should not be repeated.... 

Sangwhan: regarding editorial tweaks from Gibson (https://github.com/w3ctag/design-principles/pull/409 and https://github.com/w3ctag/design-principles/pull/412) I will take some part sand credit him as author but will reject the PRs and (will let him know that).

### [Warn against getter throwing exception since it is a side effect](https://github.com/w3ctag/design-principles/pull/408/)*

Lea: i have some thoughts in the comments...  

Yves: if you set something and processing needs to happen...

Lea: then that shouldn't be a getter

Tess: sometimes it has to be because it does more work...

Yves: it shouldn't throw... 

Tess: probably a bad thing for getters to return promises..

Sangwhan: that shouldn't be a getter it should be a method...

Sangwhan: the suggestion itself is pretty simple - there have been antipatterns where the getter throws.  Are we OK with that at a high level?

Les: yes i'm a bit skeptical on the justification listed

Tess: Yes I think it should be a should not a must. if the underlying assumption of the API is wrong but for compat reasons ... in these cases we don't have a time machine... it now interacts with a different feature... the result is what was originally a simple getter needs to throw in some cases.

Lea: there should be no **must**s in the design principles.

Lea: there's an implicit should because it's design principles...  I think we should have this as part of the introduction... 

Yves: e.g. "getters must not have side effects"... 

## 5b

Present: Dan, Tess

*We look at **overloading** https://github.com/w3ctag/design-principles/pull/372*

Tess: *does a review*

Tess: not all optional arguments are good... this need re-wording... 

*we review the examples and try to develop some new examples*

*we dropped the examples and landed https://github.com/w3ctag/design-principles/pull/372 and opened up a new issue https://github.com/w3ctag/design-principles/issues/431 to find examples*

*We look at **Serialization** https://github.com/w3ctag/design-principles/pull/367*

We made editorial changes and merged https://github.com/w3ctag/design-principles/pull/367.

*We look at **interoperability and implementability** https://github.com/w3ctag/design-principles/pull/290*

We committed many suggestions, simplified and did not land the PR but there has been good progress.

## 5c

Present: Peter, Yves

Concerns about keeping up-to-date comprehensive list of all the specificiations relative to permissions, would be better to link to a curated list maintained by groups working on that subject (see COOP: restrict-properties above) 


Did some spelunking here to try to recover the context, the PR is exrtemely sparse.
https://github.com/w3ctag/design-principles/issues/41
https://github.com/whatwg/html/issues/2259
The issues link to old minutes on the etherpad that weren't captured on GitHub, plinss is working on recovering those.

See also https://github.com/w3ctag/design-reviews/issues/339#issuecomment-461115034 re: when to discuss adding new restrictions

## 7a 

Present: Lea, Sangwhan, Tess

### [(Document Subtitle): Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819)

Sounds like they may be taking this in a different direction, based on the discussion about this in WebKit's standards-positions repo. Closing for now; we'll take another look when they've made those updates.

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776)

Yves noted that they're using HTTP GET inapproriately. It also looks like they're working on a very big change to this, so perhaps we should defer reviewing it until that happens.

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721)

We left several comments on the review with things we spotted, including:

```
Hi,

@cynthia, @LeaVerou, and @hober took a look at this during our Tokyo F2F today.

We are sympathetic to the requirements this sets out to fulfill. The complexity of [document rules](https://github.com/WICG/nav-speculation/blob/main/triggers.md#document-rules) is concerning. While having solutions that can cover the whole spectrum of use-cases is nice, significant added complexity will have adverserial effects on adoption - and whenever possible we value [simpler solutions](https://w3ctag.github.io/design-principles/#simplicity) that an average developer could easily understand and make use of.

If you could propose a simpler approach that could cover say, [80% of the use cases](https://lists.w3.org/Archives/Public/public-html/2007Aug/0495.html) as an alternative - we would love to see this. One example that came up in our discussion was an attribute on `<a>` elements instead of an entirely separate technology. After all, more complex approaches can always be added later, if the need arises.

One bit about eagerness - it would be useful to state (maybe not normatively?) that ideally implementations should provide  a way for the users to set their prefetch preferences, and user preferences should be treated as higher priority than the page-declared eagerness preference - in particular in low-data/bandwidth scenarios.

```

## 7b

Present: Dan, Yves

### [Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798)

Yves: How was it different from popover...

Yves: if you have an image editor and you have side toolboxes... which would be a better model? Popover or picture-in-picture?

Dan: my sense would be popover...  but it kind of depends... 

Yves: depends on what capabilities are for exchanging data from one window to another...

### [wildcards in permission policy origins](https://github.com/w3ctag/design-reviews/issues/765)

*looking at latest comment / version: https://github.com/w3ctag/design-reviews/issues/765#issuecomment-1468200656*

Dan: noting a positive review on the initial Mozilla standards position request but no response yet on the most recent [request](https://github.com/mozilla/standards-positions/issues/760).

Dan: looking at comments [left by annevk](https://github.com/WebKit/standards-positions/issues/51#issuecomment-1470519891) on the webkit standards position...  However it does look like there is work going on to address the issues Anne has raised...

Yves: [on hostname matching] They are matching what's in CSP but that still opens things too much. The possibility of having a wildcard and removing a few things might have been good. The fact that they are reusing what is in CSP is a good thing even if it doesn't solve our original comments.  

**We [close](https://github.com/w3ctag/design-reviews/issues/765) this one.**

## 7c

Present: Peter, Max


### [Web Bluetooth exclusionFilters option in requestDevice()](https://github.com/w3ctag/design-reviews/issues/830)

Seems like a small and reasonable extension, closed satisfied.


### [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820)

We have questions:
1) The explainer talks about a 'small amount of data', why is this called 'largeBlob'?
2) Why is it called a blob if it's reading and writing array buffers? The property name should be relevant to the data type, either make the API accept a Blob or use a name that doesn't imply Blobs.
3) What's the size limit of the data? If there any way for the RP to know what's available?
4) Is there expected to be a mechanism for the user to clear this data? (Independent of clearing the entire auth for the RP) Either via UA UI or a future API call?

Posted questions to the issue.


### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813)

Posted a question about user consent and possibly replay issues.

## TAG Future

Present: Dan, Lea, Tess, Yves, Sangwhan, Peter, Hadley
Guest: Florian

Agenda:
* Appointments
  * Additional members
* Councils
* Additional Responsibilities with Director-Free
* Succession - current members' time commitments & limitations
* Future additional role of the TAG guiding / steering / etc...
  * Charter Review
  * Technical Vision

### Appointments

Dan: Appointments - where do we stand?

Florian: 3 difference proposed in 2023 process.  First difference is the appointments happen after and not before the election.  Secondly, the team not the "director" is supposed to do it and enforce the real consultation and ensure the needs of the community are met.  Ratififcation step which is AB and incoming TAG.  Third, term limits.  No term limits for being elected.  Limit of twice in a row for being appointed.  Starting from now.  Fourth difference: TAG picks its chairs now.

Lea: how does this work for chairs?

Tess: in process 2023 - pre-existing status quo is that Tim is chair. In a diirector-free world Tim is not chair of the TAG...

Florian: TimBL is a permanent member as himself but not chair.

*all fine*

Lea: it takes very specific skills to be chair of the TAG.  If the chais don't get elected we might not be able to...

Peter: question on term limits - if the appointment is happening after the election... say I'm appointed twice more. Now I have stand for election. Am I then eligible for appointment the next term. 

Florian: then you would have to set that term out.

... if at the next election peter stands for election and loses he can be appointed.

Peter: term limits are two back to back not two cumulative...

Tess: I think if your term is up and you want to remain on the TAG you should stand for election.

Peter: two concerns - one is ... - reality is that most of the AC are low information voters and don't engage with the TAG. If an incumbant runs they will be voted for.  I'm worried the AC won't understand the subtleties here. Therefor there is a bias against appointed people... Appointment system could be used to back fill.  If we had an informed electorate...

Tess: I agree. Issue Yves identified - if you have qualified candidates and others get bumped... not necessarily a bad thing. I think we should be aiming for results where the TAG changes over time.

Peter: some amount of churn is good - a lot of churn could be disruptive.

Hadley: particularly if TAG is supposed to figure out the gaps, and if they haven't done the job before, it's hard to identify those gaps...

Florian: ratifying is not just by the TAG also by the AB...  Appointed by "their old friends" that looks bad... That provides an extra ...

Peter: after the election the team or whoever sends to the AC for a simple up/down vote.  

Florian: it's to AB and TAG for a simple up down vote.

Yves: we don't want a second election...

Peter: the fact that appointed members have to sit out a term ... if we don't have someone within the membership who wouldn't suitable as chair and a person who would be a good chair wouldn't be suitable... 

Tess: then we might have bigger problems.

Florian: if the people appointed will be same people... by the time we've hit the term limits we will have had time to revise the process... 

Hadley: enough core in the TAG to keep the consistency ... sense of skills... what's needed for good appointments. Don't see a better way forward...

Tess: the existing schedule of elections and appointments... staggered terms... even if an election cycle / half the TAG is still incumbents... 

Hadley: if only one year of TAG service I can imaging a scenario with 3 or 4 well meaning people who haven't been on it long enough to know how to proceed...

Florian: occationally the AC wakes up... in 2013 the AC with lobying the AC did vote in radical change in the TAG...

Tess: I would prefer entire tag stands at once... The middle way would be the status quo of staggered terms... 

Hadley: I agree with the halfway point. I want to put on record: I think it's dangerous to give AC unfettered authority... One of the befits of having appointed roles is that AC can be captured by trends, by interests... 

Tess: which is why the teams with the TAG and AB do it.

Hadley: agree.  But some have said AC should be ultimate authority and I don't agree with that.


Yves: every time you put TAG in a decision making role it's susceptible to political bias instead of technical-based voting...

Tess: 

Torgo: this implies a lot more time/work for TAG members, to meet with the AB, to hammer out appointments 

Florian: we (TAG/AB) are ratifying, not making appointments. It's the team's job to ratify the appointments, the team talks to whoever they need to to work out who is missing.

Torgo: so the TAG needs to come to consensus. How?

Peter: an email vote, using WBS for example.

Torgo: this starts next December.  I will run for election next december.

Lea: One concern regarding the chairs... we can't just appoint anyone... it needs to be someone...

Hadley: a lot of responsibility for maintaining continuity would come to the team...

Peter: some knowledge... required to keep continuity... Avoid repeating past mistakes... institutional knowledge...  Outgoing TAG members are invited to meetings after their terms are over... So if there is the opportunity to knowledge-transfer.

Sangwhan: we could introduce a handover period...

### Additional Members

*discussion of STV* (See [Arrow's Paradox](https://en.wikipedia.org/wiki/Arrow's_impossibility_theorem) )

Tess: there's responsibilities, time and people to do the work... adjusting one of those things without adjusting others doesn't work... increasing the responsibilities means we need more people... 

Dan: +1

Florian: does the TAG wish to have more members?

Tess: councils = a new responsibility... theoretically they don't hapeen that often... countils are a time sink... And they require all TAG members.  Adding seats might produce undesirable results - but it behooves us as the TAG to say "we sign up to this level of work" and if the work load is changing then we can't commit to that same level/quality of output.

Sangwhan: the one member per company restriction? Not making an argument either way

Dan: I think some companies would take advantage of that, and I don't think it would be good for the TAG or the web. 

Lea: if TAG members aren't representing their organistaions...

Dan: because they carry the bias of their organisation. That's a human nature thing.

Florian: It's not about saying what your organisation tells you to say; it's that the environement in which you exist, the viewpoints that you are exposed to, they influence you...

Tess: it's that you are seen to do the right thing. relaxing that urle would change the percpetion of the TAG.

Lea: Doesn't have to be black or white?

Florian: What happens when one preson switches affiliation? That's different

Lea: you could finish your term

Peter: currently, you can remain in your seat until the next election, whether your'e up or not in that election.
Also, in the past, we have lost valuabe tag members becuase of that.
But I do agree with Dan and Tess; this rule is important. if we were going to relax it, I would say at most two people and one of them has to be appointed. So the influence of the organsation could be taken into account during the appointment process.

Lea: If we make it 2 people, we could add protection like "these people must have been in the TAG before their affiliation changes."

Tess: We already have an eception for that case

Peter: but if you allow peopel to continue on, then you have an incentive for someone company to poach all places in the TAG

Lea: so two person maximum

Sangwhan: and special rules for councils

Florian: if you continue to do the same job, plus new jobs -- yes. if the workload stays the same, but the TAG is more focused on high level things than being in the trenches... create a task force for the breakouts. Offload that off the TAG. Have the TAG do more of the high-level things we think are appropriate.

Yves: Creates the issue -- might reduce the credibilty of the people on the TAG

Sangwhan: in the Task Forces, there is no forcing function of neutrality.

Dan: we have handpicked people for task forces. Whatever they come u pwith still needs to be ratified by the tag. Design reviews can't be delegated, has to be done by the TAG.

Tess: In our last f2f in London, we discussed this. Discussion: are we focusing on things in our deign reviews that we have horizontal review groups for? If there were enough horizontal review groups, then we wouldn't have to do this at all. In practice, we see that the results of horizontal review vary widely. Most of the groups that ask for TAG review don't ask other groups for hoizontal review. If we really wanted the TAG to do fewer design reviews, we would need to see evidence that this is done.

Florian: I think the TAG should make sure those groups exist

Sangwhan: it's likely that the group proposing the review are the same experts in that topic. Domain experts for task forces: group is small, and they often have a vested interest in each proposals.

Yves: This is the Directorates that the IETF are using... a small set of people appointing people from that group to review specs. It's probably not as healthy as using a set of neutral people 

Lea: I like the idea of outsourcing. We could ask these groups for review, reduce the time for us. I disagree that if evertything was handled by these groups than TAG review isn't needed.

Tess: i agree

Lea: I don't think a lot of design review can be outsourced -- evaluate for architectural consistency. That's ours

Dan: Problem with outsourcing: horizontal review groups aren't elected, they are self-selected. They aren't necessarily effective or efficient or balanced.

Florian: the TAG could be appointing them. 

Sangwhan: If we outsource and there is no rules on neutrality...

Yves: occasionally we ask some people for input on some reviews. We do get a specific viewpoint when needed

Dan: and we have this concept of TAG diaspora, people who have been in TAG, run for TAG, interacted with us a lot. We informally reach out to them for help.

Lea: what if we significantly enlarge the TAG, and assign people to groups, formalise the group for design review in each of the horizontal review topics, and each subgroup needs to sign off on each design review

Dan: My counterproposal is to request 2 additional seats. Have them still be generalists, overarching view of the web platform. We will have specialisms of those people, but that will naturally occur. I feel like that's how we're currently organising the breakouts.

Tess: if you rapidly increase the size of the TAG, that causes concern. So we'd have to do a small, bounded increase. If we don't increase it at all, and keep adding responsibilities, the quality of output is going to suffer.

Yves: instead of addding responsibilities, you can add another body that can ask the TAG for details.

Florian: adding 2 people is probably a good idea. We could say we added them to the AB a few years ago, but actually we need them in the TAG instead, especially since the board of directors has taken responsibiliteise from the AB.

Tess: At IETF there are two bodies that correspond to the TAG: the IAB, and the ADs who do the reviewing. Offhand, I don't think adding a body is a bad idea. But it's a more radical change.

Dan: it is. But I think it's clear we need more seats.

[break]

### Councils

Lea: i think it's wasteful for all tag members to participate in every council...

Florian: there's no recusal. but you can say "i'm not going to participate because I don't have relevant experience"  It's listed in the process that you can show up at the end and say "given who was part of this I trust the result."

Lea: that doesn't work for reducing the workload of the TAG...

Florian: on TT it was harder than I thought it would be... having people with experience in those types of specs was relevant...

Sangwhan: can't the TAG nominate some subset?

Lea: maybe we could institute this.

Florian: I don't see anything in the rule presenting this...

Tess: part of the reason why the AB and TAG both constitute the councils.. by the time it gets to council its oftena  mixture of technical and procecural concerns... if the TAG were to nominate people and the AB was fully represented I'm worried.

Peter: if we see that happening we could send more people than the AB...

Florian: you send a subset and if you trust the subset it's fine and subset can ...

Yves: another idea would be to reduce the number of councils by letting team close more aggressively some disputes.

Florian: there is a provision for this - the team is allowed to make a recommendation.  More likely to be used to repetitive cases...

Dan: do we have TAG consensus that we would like the team to be more proactive in stopping things from coming to council?

Tess: Yes. 

[discussions of specific councils/formal objections]

Dan: do we have consensus on selecting subsets of TAG members for councils?

Tess: I like the idea of doing that, but I don't like the idea of committing to always doing it.

Sanghwan: subset could also be the whole TAG.

Florian: even if you decide to trust someone, you can still put your name against the decision

Hadley: I think it's worth trying, iron out the wrinkles as we go

Peter: My worry is that no one will want to go

Sanghwan: we could make a rotation -- whoever didn't do it last time

Lea: but we do want it to loosely correlate with expertise.

Florian: just councils and the election / chair picking 

*some discussion on CEPC violations that have occurred during the context of councils*

* **TAG Resolution** to ask Florian to ask the AB about the idea of indemnity insurance for council members*

*fully gaveled* 

### Additional Responsibilities

Florian: lack of technical guidance for consortium ... one example is in chartering... Where does team derive the legitimacy from...?    In theory the team and team alone put the charter forward... in practice some wgs decides on the new charter. 

Tess: tim had moral clarity of what we're trying to do here.. what should we add to the web and what souldn't we. Absent that vision..  w3c is a member consortium... the business model of w3c is to have members who pay dues. The incentive is to have new members from new in new industries. Incentivies enlarging to areas that don't represent the web's values... tim used to be stop gap. In the absence of tim i don't see how we do that now.

Florian: BD presentation to the board... the essence is that a sales machine is a sales machine... not the sales people's job to figure out who they go after. they don't have someone to tell them who to go after.. 

Hadley: we as the TAG come up with holes in the web architecture - things that need to be done, or gaps between working groups' efforts - and we have nowhere to take that. we try to send it to members of the team and communicate it ... that should inform the chartering and the sales machinery...

Tess: we need to have a technical vision... help the consortium skate to where the puck's going to be....

Sangwhan: web as a product vision ... the web needs a product manager...

Yves: *funding model*

Yves: every week I have a global meeting with w3c team where I report on the TAG... occasionally it sparked new conversations... there needs to be a better way - for example when we identify a need for new work - to get that done...

Florian: Hadley said sometimes you observe gaps... when the bizdev machine says "hey we're going to go after xxx what do you think" they should loop you in.

Florian: BD asks for a body to exist that informs the BD work...

Florian: do we need a product manager or define what the web will be? i don't think people are looking to the TAG for that...  I think if we predict the future we get it wrong... however we can manage the scope... and say "this a distraction"

Sangwhan: +1 on that - but what we could do on w3c is to provide feedback on gaps on the web.

Tess: one to the things about what you just said - there are a lot of gaps in maintenance of the web platform that are "boring"... BD will never go to thes topics... they won't bring new members... 

Dan: security is a good example... 

Yves: issue for wide reviews where we need... 

Florian: point the sales machine somewhere...

*scope of the TAG*

Tess: we spend too much time on design reviews... are we missing the forest for the trees...

Tess: saying don't go into the valley...

Hadley: all of the TAG work is currently reactive... we should be proactive...

Yves: findings are proactive... we're not making enough of them...

Florian: plenty of good people on the team... we don't have a deliberate policy of what kind of people to recruit. that too can be part of filling the gaps...

Tess: example: we sould hire a second Richard Ishida... 

Peter: The "moral centre" of the web should fall to the TAG...

Florian: it may mean the TAG becomes political...

Peter: the TAG should and can remain focused on the technical and architectural  aspects... I argue the ethics of the web art part of the architecture of the web... it's our job. we can hold as part of our charter...

Yves: Ethical Web Principles started with common points we were seeing when we do our reviews...

Tess: my talk from last TPAC - shows the linkages to everything in the EWP...

Peter: it's the TAG's charter to take that kind of knowledge to document it.

Tess: [EWP presentation](https://tess.oconnor.cx/2022/09/ethical-web-principles)

# Day 3

## Session 9

### Elections Redux

Present: Peter, Florian, Lea, Sangwhan, Tess, Dan, Yves

Florian: yesterday we discussed 2 extra people for the tag. question in return: now (for 2023) or next process cycle?  It's doable now with some effort...   So if we want to do it for next election we have to do it now.

Lea: one idea I proposed : even if this ends up being an elected seat - so we can appoint someone now - and then at the next election cycle it becomes and elected seat... Because we don't want special elections.

Tess: Perception of cronyism... 

Dan: An additional elected seat and an additional appointed seat?

Lea: seams 

Sangwhan: seems we're changing the appointment process we could change that later...

Florian: if you add 3 seats - 2 elected, one appointed, that might be good for election cycles.

Lea: my worry is about auto-election.

Florian: run campaigns....

Sangwhan: 3 seems radical...

**Proposed resolution**: ask for 3 new TAG seats to be added in Process 2023. Two elected seats and one appointed seat. The appointed seat's term should align with the existing "odd person out" appointment, so that each election cycle 2 TAG appointments happens. Each new elected seat should line up with each of the two current TAG election cycles. As soon as Process 2023 is adopted, the Team should immediately fill the appointed seat for what would be its remaining term.

**RESOLUTION: SO RESOLVED**

Dan: Additional proposl about "TAG Auxiliary".  TAG to be able to appoint some number of 

Lea: I like the idea - if we want it to work then it needs to sound a lot better. People should be mentioned on the TAG web page. Needs to have some level of prestige. WOuld you fund me to travel. 

Tess: Deputy? Assocoiate? I think we should resolve on it. 

Sangwhan: the high level idea is good.   Person gets their name on the web site. The title should sound quasi powerful. 

Dan: who gets to decide.

Tess: We need a consensus view. If someone objects then no. Everyone can veto.

Dan: each aux person can sponsor a person and only one person.

Florian: you probably want to continue ...

Tess: amonsgt the deputies have an affiliation limit.

Lea: if every single 

Dan: i think it's a bad look if we use this to bring in people from the same company / org...

*some debate but consensus that deputies themselves should not enable us to bring in any more than one extra person from an org that already has a TAG member affiliated.*

Peter: restriction that the deputy has to be sponsored by a member. Fine with having both restrictions..  Also just to keep in mind. these are things we're placing on ourselves... We can choose to relax our restrictions if we want to.

**new topic*

Florian: in the previous election cycle the Ab thought that giving aadvantage to the incumbents wasn't good..  we have monthly open zoom... using one of those as a meet the candidates... Any question asked during the session would be transcribed... we're going to apply this to the AB. Should we also have this for the TAG?

Tess: Yes

Sangwhan: yes

Dan: yes

**SO RESOLVED**

Lea: what if we say "we want an AB member in each f2f"

Sangwhan: if there is a member of the other org nearby...


## 9a

Present: Lea, Yves, Sangwhan, Peter

Sangwhan: Let's discuss naming of factory methods 

Lea: I want to solicit TC39 input on this, so I'm creating an issue in our Reflector repo

...: Actually, there are several issues where we'd need their input on. Can we discuss what these are so I send them a list?

Peter: Let's create a label, and try to have TC39 automate monitoring/referencing the label like other W3C groups do

Lea: Great idea, what label?

Peter: TC39-tracker

(discussion about which issues to add)

Lea: I want to send them to https://github.com/w3ctag/design-principles/issues/11 but don't want people to have to read the entire discussion to get to the last comment with our current position, do you think it's ok to edit the first post? It's by Domenic.

(discussion about minutiae of how precisely to do so to not look like we're taking over his post)

Peter: What if you add it to the end?

Lea: SGTM

Lea: is https://github.com/w3ctag/design-principles/issues/400 relevant? It seems to mostly apply to non TC39 specs

Sangwhan: Yeah, I think a lot of these antipatterns mainly happen in Web-only stuff

## 9b

Present: Dan, Tess, 
Guest: Florian

### [New principle: Guidance on User Activation #314](https://github.com/w3ctag/design-principles/issues/314)

Closed as we [landed a PR addressing this](https://github.com/w3ctag/design-principles/pull/365) last year.

### [New principle: When to use client hints #307](https://github.com/w3ctag/design-principles/issues/307)

Tess: Ok from [minutes here](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/06-14-minutes.md#breakout-a) it's clear there is an RFC... we could cite the RFC and have a principle.

Dan: makes sense.

Tess: in a sense the principle is redundant.  However many are not looking at the RFC... 

**Principle "Client Hints must not be used to expose information that is not already exposed to web pages"

Client hints are an important optimization, but cannot be the sole means by which information is exposed to sites. As it says in <cite><a href=https://datatracker.ietf.org/doc/html/rfc8942#section-4.1-5>RFC 8942 §4.1</a></cite> where client hints are defined: 

<blockquote cite="https://datatracker.ietf.org/doc/html/rfc8942#section-4.1-5">
<p>Therefore, features relying on this document to define Client Hint headers <strong>MUST NOT</strong> provide new information that is otherwise not made available to the application by the user agent, such as existing request headers, HTML, CSS, or JavaScript.
</blockquote>

Dan: Where shoudl this live?

Tess: in Section 10, Other API design considerations, since we don't have a dedicated HTTP section.

Dan: *writes [PR ](https://github.com/w3ctag/design-principles/pull/434) for this*

### [New principle: New features must not break existing ones #297](https://github.com/w3ctag/design-principles/issues/297)

Tess: this is a backwards compat principle... If you look at the HTML design princoples document: "support existing content" - and Elika [wrote a blog post](https://fantasai.inkedblade.net/weblog/2019/designing-css/#compat) ... overarching project that the design principles covers the items in the HTML principles doc... We need to add something.  But - and all do credit to the html design principles doc - it's short and there is nuance. It's possible to "break" an existing feature without breaking content.  For example the `marquee` element... so - when such an element is parsed currently it parses as "unknown" ... but what we did instead is add advisory - to the rendering of HTML.. here's how to approximate it in CSS... So technically it's broken, but content works the way it used to... It's not an absolute rule.. So `isindex` tag ... was a parser macro... it would create a form element, etc... This was removed from html... There was a desire to remove it from html ... parser macros are difficult to explain... There was some analysis of usage in the wild... we determined that the amount of content that would break was "acceptable". 

Florian: not infrquently in CSS we change behaviours... 

Tess: in CSS there is a principle of not failing hidden... If a browser doesn't support a new feature the rendering of the content .. "no data loss"... [also in the Elika's blog post]. Sometimes we are going to break things but we need to do hat responsibily....  This is an interesting principle. A lot of nuance. We can't have the principle say "never break anything".  The nuance is the improtant part.

Dan: the principle should be "Break the web carefully"

Tess: as a general rule you shouldn't break things.. however sometimes you need to break things. And you need to do it in a careful and measured way.

Dan: `SharedArrayBufffer` is another example.

Tess: removing it was the right choice for user safety... it broke a lot of content. we brought it back with [guardrails].  In CSS - aliases... we have this feature that was just working with flexbox... we want it for grid too.. we'll keeo the old flexbox specific version... and define it in the spec as a new thing...  but not totally the same...

Tess: please assign me the action to take a shot at this...

## Plenary Session - session 10

Present: Dan, Lea, Yves, Sangwhan, Peter, Tess
Guest: Florian

### 9a roll-up...

Lea: since we want to push tc-39 people to issues... useful for them to be self-contained... GitHub has a system to highlight but it's based on upvotes... we want people to not have to read the entire thread ... we ended up adding an edit at the end... current TAG thinking. We did this in issue-11 so far....

### 9b roll-up

Lea: on [client hints]() are we saying "when adding a client hint that exposes new information don't do that" ... Is it a privacy pricniple?  

Tess: in order to add a client hint, the info exposed in the client hint must also be exposed elsewhere.  

Lea: the gudiance is it must be exposed elsewhere...  That could be made more explicit...

Peter: Just because you want to expose info through a client hint doesn't mean it should be exposed elsewhere. The right answer is don't expose that information at all.

Tess: right.

### Caching and Bundling Finding

Sangwhan: jist of this document is addressing the pain - shipping around piles of JS and bundling... double-keying... cache can't be re-used. The finding says "this is a concern - antipattern on the internet" it seems to be getting worse.

Yves: the presentation we got on delta encoding earlier in the week might be a good solution to this... 

Sangwhan: agree - we could put that in as one form of minfiication.. Also - are we cargo-culting double-keyed caching...

Yves: EWP... trade-off of what it costs in terms of caching and sustainability. It would be good to link to the relevant part of the ethical web principles...

Tess: All implementations are moving to cache partioning... gekko and blink moving there... while it's true there is a sustainability cost for partitioning , we can't roll it back...

Yves: introducing smart delays to avoid timing attacks, for example...

Sangwhan: the doc doesn't suggest we should remove double-keyed caching...

Sangwhan: if there is a way to make the opacket cost cheaper...

Lea: it doesn't seem we should be fetching over and over...

Sangwhan: we're not saying the privacy aspects of this are invalid... We introduced a mitigation against timing attacks but it's a first world solution...

Tess: over all it's not a "this is bad it needs to change" - it's "we the TAG hope to see experimentaiton in the direction of reducing the cost of double-keying"... Trying to inspire people to go work on it is awesome.

Lea: the doc needs an abstract...

Tess: the intro provides background. The call to action should be in the first sentence...  First thing should be an active voice call to action. "the TAG would like to see investigation into reducing the cost of cache partitoning..."  I think the text in the hidden cost of bundling... I feel like there are 2 conclution. One conclusion us "the TAG is happy to see ongoing work to address bundling at the transport layer" the other conclusion is "the TAG would like to see experimentation."  We should "observe" there is existing work...

Dan: sounds like we have consensus on the basic idea and rough outline...

Sangwhan: I will transform into a markdown document by end of day...

## Session 11

### Accessibility Questionnaire

Present: Dan, Peter, Tess, Sangwhan, Yves, Lea
Guest: Florian

*We go through some changes to a propoosed accessibility questionnaire developed by Sangwhan and Alice*

**RESOLUTION TAKEN: We resolve to publish the accessbility checcklist and make this a part of the design review process. We will exempt people from filling it out if they have already requested a more formal accessibility review.**

*some debate on where the canonical link should be...*

Peter: it should be in tag.w3.org

Dan: +1

### TAG Charter

Present: Dan, Peter, Tess, Sangwhan, Yves, Lea
Guest: Florian

Florian: the TAG has a charter which has not been updated since 2004. It claims a whole bunch of things that are not true.  It's unclear that we need one.  Some people think charters constrain what you do...  Some others think it's constrained only Process and the election...

Tess: the AB does not have a charter.

Dan: as long as the Process document contains the 3 bullet points of our scope then I'm Ok with getting rid of the charter.

Tess: AB and TAG are special... the must exist... 

Peter: yes agree.

**RESOLUTION TAKEN: The TAG charter should be discarded as it is out of date, no longer relevant, redundant with process text and in conflict with that text. The TAG is and should continue to be defined solely by text in the Process document. Its activities are guided through elections.*

*we discuss how we need to document our process, specifically the voting procedure, and bring this into a wiki*

Peter: just to add more weight - the charter is also in conflict with the process document.

## Session 12

### [Make 6.1 more inclusive of non-Web JS APIs](https://github.com/w3ctag/design-principles/pull/435)

*some debate on WebIDL vs JS terminology....*

Tess: 

Lea: so much esoteric knowledge & terminology ... API design guide written for API designer... esoteric ..  I think it should be more friendly for JS developers to join standards efforts... 

Tess: I think 

Peter: JSIDL ... didn't get very far. if we did that then it would make sense to use JSIDL ... JS terminology...

Lea: when WebIDL was designed it was supposed to cover multiple languages and right now it just is used to describe JavaScript... I'm not suggesting web abandon WebIDL.. just about the prioritization in the text....

Sangwhan: antipatterns that we have to fight back about... 

Lea: I think someone who knows only about JS accessors will be put off by WebIDL syntax... 

Tess: most of the people who hack on these APIs don't understand JavaScript...

Peter: the developer version of the doc should be JS focused. The w3c spec writers' version should be webIDL.. not sure how we do this.

Tess: might be useful to write a separate document .. bridge the gap between JS objects and WebIDL... as an artefact of the TAG the design principles doc helps by listing things we have seen so we stop seeing those things...

Lea: people who are seeking to make standards proposals- they should be reading the original version... And these people would be able to understand that if it uses terminology they are familiar with...  Already so many barriers to getting involved in standards...

Tess: i think it's less clear

Sangwhan: In principle we want to make the doc more inclusive... 

Lea: webIDL is a huge barrier...

Dan: I support the idea of being more inslusive... We need people who are primarilly JS developers to be able to engage in ... 

Sangwhan: I'm not in disagreement about the principle.

### [web without 3p cookies finding](https://github.com/w3ctag/web-without-3p-cookies)

[issue 7](https://github.com/w3ctag/web-without-3p-cookies/issues/7)

Lea: I think the suggested rephrasing is good.

Tess: don't support making this change...

Peter: the problem we keep facing is that people keep coming to us with general purpose solutions that recreate these problems... Maybe more inviting...

Hadley: the language is "we discourage" - it doesn't say "must not" but also "at risk" - explains...

Peter: bottom line is if people coming to us with a general solution we will shoot it down unless they proove it doesn't recreate the 3pc issues.

Lea: I don't have a very strong ... opinion,...

Sangwhan: i want to reword it... 

[issue 13](https://github.com/w3ctag/web-without-3p-cookies/issues/13)

Tess: I like Nick's suggested text...

Sangwhan: I think Nick's text is better.

[issue 14](https://github.com/w3ctag/web-without-3p-cookies/issues/14)

Sangwhan: I don't support

Tess: I'm sympathetic

Hadley: the text already says it's there... We could add a parenthetical...

Sangwhan: let's not 

Tess: *writes PR*

Dan: do we have consensus on https://w3ctag.github.io/web-without-3p-cookies/ to publish as a finding?

Sangwhan: will make change of "single sign-on" to "federated sign-on"

Peter: give Amy a chance to review one more time as well... 

**RESOLUTION: We agree that we have TAG consensus as is - the current text. We agree to publish it by Monday.**

### Privacy Sandbox Issues

[Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747)

*Reviewing [last comment from josh larkin](https://github.com/w3ctag/design-reviews/issues/747#issuecomment-1514767098)*

Yves: one concern is that it could be used as a super-cookie, by leaking correlation data between sites - so a replacement for 3rd party cookies...

Hadley: The [Mozilla standards position](https://github.com/mozilla/standards-positions/issues/646#issuecomment-1238792961) is instructive. 

<blockquote> 
Having reviewed the Mozilla and Webkit position discussions, the TAG shares the privacy concerns Mozilla raised regarding this. We'd like to see these use cases worked on in PATCG, with broader participation from other implementors. 

We are concerned about the privacy implications of any storage intended to be available across sites or origins without the user's explicit permission, and see that this could lead to capabilities used to create a drop-in replacement for third-party cookies as they work now. This goes against the Ethical Web Principle [The web must enhance individuals' control and power](https://www.w3.org/TR/ethical-web-principles/#control). The TAG is explicitly trying to encourage development of new web technologies to replace 3rd party cookies that do not replicate the privacy pitfalls of 3rd party cookies. See our draft finding [Improving the web without third-party cookies](https://w3ctag.github.io/web-without-3p-cookies/).
  
We are concerned that the user needs given aren't technical needs. For example, a comparison table between the way these use cases are currently serviced and the way they are envisioned to be serviced with this new technology in place, and what the user benefit would be, would be more like what we're looking for. We recognise the use cases (cross-origin A/B experiments, user measurement, etc — which are site owner or developer needs) can provide value, but are not convinced that the value is worth the compromise to users' privacy.
  
We'd be grateful if you would please clarify the user needs as outlined above.
 
One last more general question we'd like to get a clear answer on is on a scale of 1 to 100, what pieces of the proposals in privacy sandbox will need to be in place to have a clear deprecation plan for third-party cookies, and how much does Shared Storage get us there? With so many related proposals coming in, we are concerned that the collective amount of entropy might result in a supercookie that maintains the status quo. We would likely be able to be able to provide more constructive (and likely pragmatic) feedback with some level of clarity on roughly how close we will be getting to deprecation (of third-party cookies) with the current set of proposals.
</blockquote>


## Wrap-up

**RESOLUTION RECORDED: thanks to Google and to Sangwhan for hosting us this week!**
