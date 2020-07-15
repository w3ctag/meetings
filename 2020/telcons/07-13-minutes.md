 ## Agenda

### Breakout A (Europe / US) - [2020-07-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200713T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @hadleybeeman
* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo
* [Cross-origin opener policy reporting API](https://github.com/w3ctag/design-reviews/issues/527) - @torgo, @ylafon, @plinss, @atanassov
* [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov
* [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529) - @torgo, @plinss
* [Security & Privacy PRs](https://github.com/w3ctag/security-questionnaire/pulls)

### Breakout B (US / APAC) - [2020-07-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200713T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo
* [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
* [CSS color-mix function](https://github.com/w3ctag/design-reviews/issues/526) - @alice, @dbaron, @atanassov

### Breakout C (APAC / Europe) - [2020-07-14](https://www.timeanddate.com/worldclock/converter.html?iso=20200714T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman
* [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov

### Plenary Session - [2020-07-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200715T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

## Minutes

Present: Dan, Kenneth, Peter, Hadley, Tess, David

Regrets: Rossen, Yves

### Breakout A (Europe / US) - [2020-07-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200713T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @hadleybeeman

Hadley: having looked at the change history - it's a small incremental change on their part. They are pinging the TAG for horizontal review.  The deadline may have lapsed. There are symantic changes and syntactic changes. I don't see issues with either.  I think this is isolated to TTML2. They do remove XML base...

Tess: As an HTML person that sounds good.

Hadley: I feel comfortable greenlighting this.

Tess: The only places I can think of - edge had a subset but with the chromum adoption might be moot The 2nd is no browser that I know of implements but a bunch of fairly big sites use IMSC1, a profile of ttml. BBC uses this.  Don't know that profile is tracking this change.   DOn't know if they've done the due dil.

Hadley: my guess would be that the group has done it.

Dan: propose close in that case?  

[Hadley to write closing statement.]

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Dan: i propose we close this as the webnfc spec has taken into account.

David: The thing we weren't decided on last time was what we'd say when we closed it.

Dan: I suggest "We acknowledge the work the spec authors have done to mitigate against the issues we have raised and while we believe privacy issues still exist, we think it's now up to the working group to address these issues.  Hence we're planning to close this."

David: I think a different approach would be a different spec that had devices more explicitly opt in to being on the web gave more info to the user agent about what nfc is doing.

Tess: Looks good to me.

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

[bumped]

#### [Cross-origin opener policy reporting API](https://github.com/w3ctag/design-reviews/issues/527) - @torgo, @ylafon, @plinss, @atanassov

Peter: primary feedback was yet another header...

[bumped to B]

#### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov

[bumped to B]

#### [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529) - @torgo, @plinss

David: this looks like a revision of the existing spec. Not the new spec.

Dan: there are several changes - highlighted in the request - we need to review these and maybe we can close this in the plenary call this week. I will review the feature policy bit.

Tess: I will also look at it.

[bumped to plenary]

#### [Security & Privacy PRs](https://github.com/w3ctag/security-questionnaire/pulls)

Tess: Dan's left some review comments on each of these; I'll update the PRs ASAP to take his feedback into account.



### Breakout B (US / APAC) - [2020-07-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200713T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Alice, David, Tess

Scribe: David

Regrets: Rossen

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo

Alice: some additions to the explainer

(reading of explainer)

Alice: side note: should we add the Declarative Shadow DOM explainer to the list of good explainers?

Tess: some thoughts:
* many readers of explainers aren't AR experts
* we're also not the explainer police.  Does us saying we won't review until we can parse/understand the explainer cause improvements or do they just move on?  That is, what do we accomplish by saying it's hard to review given state of explainer.

Alice: but how much TAG time should we dedicate to something that they should have been making easier to read?

Tess: TAG became relevant by providing reviews that people find useful.  How do we send people away with the feeling that it was worth coming to us?  (And is the effort differential of *that* worth it?)

Tess notes that the "design sketch" link in the explainer errors out.

Alice: Why have `root`?  In what context would you use the other elements on the page?

Tess: Are the other elements for when you're not in the immersive experience?

Tess: The element is forced to fullscreen.

David: I think maybe what it's saying about fullscreen is that the fullscreen mode in the HTML spec applies, but it's not necessarily taking up the full screen?

( disagreement within the TAG about which parts of the two screenshots are supposed to be the overlay!  Disagree about the green rectangle or purple swirl, or the "Enter VR" and "Exit AR" buttons.)

Alice and Tess to add specific questions and David to comment about the explainer

#### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris

Tess: Last time we talked about this, we were asked to wait for the TAG review of the digital goods API, so we can skip this for now.

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov

Alice: question about sensible default for `prefers-reduced-motion`.  Example from James Craig: Safari on phone lost a zoom out animation because couldn't tell which was the current tab; fixed that problem.  Using that as example why you shouldn't turn off all animation when using `prefers-reduced-motion`.  But I thought it was an example of the contrary -- probably better to close the wrong tab than going around triggering people's vestibular disorders.

Tess: Somewhere in the middle: a designer who's aware of `prefers-reduced-motion` and aware of it could find milder animation for that setting rather than none at all.  But the default without writing any media queries, if the default is disable it, hopefully they'd know that and be able to code to that case. [...missed...]

Alice: Are user needs better forced by turning off by default or on?

Tess: Risk of creating a mechanism for users to opt back in

David: I think there have historically been two approaches to this in CSS.  Some things, like Presto's handling of `projection`, detect the presence of a media query and have different defaults when it's present.  This can behave quite badly when libraries are in use; if one library is aware of `prefers-reduced-motion` and has appropriately-reduced animations, and another doesn't, it leads to bad results.  I think the model of [`color-adjust`: `economy` | `exact`](https://drafts.csswg.org/css-color-adjust-1/#perf) where things are individually designated as being OK (in this case, to print backgrounds) is a better one.

Alice: Yeah, agree that it's better to say "this animation is OK".

Alice: This discussion doesn't apply to just this API.  Not sure if it makes sense to comment on this API or whether it's a broader comment for CSS WG.  Should all animation APIs require an explicit opt-in to work when a `prefers-reduced-motion` media query would match?

Tess: I'd expect to be shot down by a compat argument that too much existing content would break...

Alice: ... stop triggering vestibular disorders.

Tess: ... seems like an improvement.

David: Is there any relevant experience from having shipped `prefers-reduced-motion`?  Or is the interesting experience that we'd get if browsers actually disabled animations by default for reduced motion settings?

Alice: I think I've seen complaints that sites still move a lot when users enable the reduced motion setting.

(complaint about Parallax example in explainer)

Tess: Parallax example is a great example of something that should be disabled.

Alice: I think there was an Apple blog post about types of animations that tend to trigger vestibular disorders.

Alice: Should we bump the rest to next week and revisit then for rest of the API?

#### [CSS color-mix function](https://github.com/w3ctag/design-reviews/issues/526) - @alice, @dbaron, @atanassov

[Ran out of time before we got to this.]

#### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron

[Ran out of time before we got to this.]

### Breakout C (APAC / Europe) - [2020-07-14](https://www.timeanddate.com/worldclock/converter.html?iso=20200714T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present:  Dan, Alice, Kenneth, Sangwhan, Hadley

Regrets:

#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

Sangwhan: I read the feedback. I am unconvinced that there is no way to mitigate the problem. I think we should request exclusive access. 

Dan: I support.  I think web APIs should not allow for unsanctioned tracking.

Sangwhan: Even making it more uncomfortable - e.g. making the user re-allow permissions - would siginfigantly change things.  If the user is asked for HID permission for e.g. Reddit then they might know something fishy is going on.  Anything that makes it annoying to do this practice of cross-origin communication.

Dan: what is the argument about only allowing one origin?

Sangwhan: i think there is a valid use case but it's not a commmon one.  

Hadley: what's the use case?

Sangwhan: one example: music controllers.  E.g. drum machine - on native you can have it read by different pieces of software... 

Dan: That sounds like the web midi API....In in our Security and Privacy checklist, it asks things like "does the utility of the thing outweigh the risk?" One corner case maybe doesn't happen on the web then?

Sangwhan: maybe something you have to explicitly opt in for it...  There may be valid use cases...  Default should be signle origin exclusive access.

Ken: then you can see if people actually request this other feature...

Sangwhan: when you switch tabs and go to a new device you don't just magically get access... I will have a chat with the spec author.

Ken: I could imagine playign a game , a chat window opens, and then you lose the connection...

Sangwhan: [will take offline]

[bump this 2 weeks]

#### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

Alice: ...the story so far...

Sangwhan: Brian asked me about [my question](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-648861529).

Alice: that's like an extra level of complexity I don't think we need to consider.

Sangwhan: something that isn't quite solved but might be useful.. math would suffer from this being not there - especially when moving symbols around...

Hadley: if the benefit of that is any instances of a variable resolve to some instance of the variable... doesn't feel that different from the rest of the web - to do it in a CSSey way or instantiate each time.

Sangwhan: My response to Brian was:

*Okay, so imagine a simple equation like this:
y = ax + b
Where ax links to something. Now twist this a bit:
y / a = x + b / a
But you want to note that / a, x, and the other /a all link to ax, since the term is there - pointwise links for each of them is doable, but then the semantic group connection is lost.
y ^ 2 = ([ax]) ^ 2 + 2[a]b[x] + b ^ 2  or something like this where the [] indicate the group*

... I told them I don't want this solved now. But the example they linked was way too simplistic for common use cases for longer equations.  Don't care if it's not solved right now.  Feels like doing something premature would not be good.

Alice: but what do we do about what's already shipped with hrefs?

Sangwhan: un-ship?

Alice: breaks a bunch of existing content...  Brian said towards the end of that call... a lot of people are saying "my code won't work in Chrome then.. oh well".  This is supposed to be about creating an interoperable baseline standard.

Dan: We're not the ones controlling the code base. We could issue a recommendation...? We could do what Sangwhan said...

Sangwhan: ...that we already rushed out MathML and that's why interop is hard now. Maybe take it step-by-step and try to do it better this time. It's not interoperable right now. Safari, Chrome and firefox already have three different implementations. Not good.

Dan: Could we favour option 1 becasue there isn't enough concensus about the right answer? and if you ship anything other than that, make sure people know it's an experimental feature and not part of the spec?

Alice: but it's been shipping for decades. This is the thing, why they had to do this project so carefully. there is all this MathML out there, all edge-case-y and fragile. Do we break all that? What's the cost of that? Can we get the browser vendors that are shipping MathML to buy into unshipping it and breaking all of that content? 

...Possibly shadow DOM is the most compelling reason. I linked in my comment to a discussion they were already having. Attaching shadow roots depending on whther there was an href. But that's funky, right? So maybe we should say for future compatibility with shadow DOM, option 1 is a very neutral option, and doesn't lock you into requring special rules. Option 3 might be one possible future direction once we understand the use cases more fully — but it might be a good idea to revisit the use cases, and see if a more nuanced design can be reached. This does mean a lot of existing mathML won't work in chrome and will stop working in other implementations. That is regrettable, but — it will be trivial to write a little polyfill that at least repairs the functionality for leaf nodes. 

Hadley: it feels like we need the working group to figure it out.  I'm hearing the wg's work doesn't have buy-in from all the implementers. We could come up with a solution but we aren't the right people.

Alice: Implementers ... existing implementations in webkit and firefox that go back years - implemented in the early days - when blink forked from webkit we removed mathml. Not sure if the implementers already shipping would buy in to unshipping href everywhere. The folks who are saying "i don't like anything that doesn't involve href everywhere" are not implementers.  They have content.

Hadley: both of those problems feel to me - 

Alice: they've discussed it at length and that's why they asked us.

Hadley: our response should be: this is us operating in a perfect world vacuum but we feel like the implemeneters, authors and developers ideally should reach consensus.  Our job should be to help them set bounderies.  Feel this shouldn't be out respnsibility.

Alice: what flavour of advice would be appropriate?

Hadley: level you were talking about is fine. Adding a line or 2 about how all of these points of view should come from implementers, browsers, authors, developers.. we are proxying for them. means that we encourage the WG think about bringing these views to the table.

Alice: value of option 1 is that it doesn't require extra work but gives you the capability to add links - and is future proofs; option 3 can be disregarded - can come later as an add on. Option 2 rules out option 1 and makes option 3 moot but it has the value of being backwards compatable. 

Hadley: maybe share that feedback.

Dan: I feel like our response should lean towards option 1. And then see what happens in the implementation and content space and revist.

Hadley: ... close to the way you do things in [html] content ...

Alice: option 2 is the href on every mathml element...

Alice: [on option 1] simplicity, doesn't put you in an awkward position re shadow roots, and it does put you in a position to come up with a more nuanced solutuon re: sangwhan's point.

Dan: I will come up with a proposed closing comment based on our discussion that we can agreeon at the plenary call.


#### [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov

Ken: touches on the same area as webcodecs.  They are looking about how to use this on top of web codedc.  Hard dependency.  This API is a more user friendly API running on top of codecs. 

Ken: propose close

Sangwhan: 2nded

[closed]

#### Miniapps



### Plenary Session - [2020-07-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200715T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Kenneth, Alice, David, Peter, Tess, Rossen

Regrets:

#### Breakout Rollup

#### Breakout A

Dan: Breakout A..

... Talked about **TTML**, agreed to propose closing, Hadley made the point that it's an incremental update. Tess had some concerns around existing implementations...

Tess: I was ok with closing it.

Dan: Decided to close it, Hadley commented. Suggest we close this now.

All: Aye.

Dan: Closed.

... **Web NFC**... kicked around for a while, hasn't been TAG consensus on whether or not ... on a number of issues, primarily to do with privacy mitigations described in spec. Lot of back and forth with Vulkan in particular on this topic. I propose closing... done with value that we can put into this. I feel that they've done a lot to include information/sections in spec that acknowledge the issues we raised and to mitigate some of those issues, it's up to them to solve those issues. 

.. Added a closing statement, suggest that we close.

Tess: I was there... David and I had pretty similar takes on it.

Dan: Is my closing statement overly positive?

Tess: Seems good.

Alice: What changed? Folks were opposed to this...

Tess: Don't think that changed...

Alice: Ok so we're just saying we've done what we can in this review?

Kenneth: We're just horizontal review.

Dan: Folks seem less unhappy because of some of the mitigations and additional considerations in the spec based on our feedback. That's not to say that they're actually happy.

Tess: that sounds about right.

David: I'm not so sure. A lot of different people have different opinions, though. Some of the people who were unhappy would be happier if the *device* had to opt into being used on the web...

Tess: I am one of those people, I think.

Dan: Maybe we add an additional closing comment to that effect? David, would you be ok with leaving that comment?

David: Like this thing is NDEF ... some different four letters that meant "NDEF for the web"... opted in to being used by websites. I'll leave that feedback.

Dan: Then we can close the issue.

David: Ok, I'll close it as well.

Dan: **Blink shipping process** nothing yet, bumped a few weeks.

Dan:: **Cross-origin opener policy reporting API** bumped to B and **WebXR Layers** similarly...

... **Geolocation API** bumped to plenary...

... **S&P PRs** I reviewed, Tess still to respond.

#### Breakout B

Tess: Talked about **Web XR DOM overlay module**. Had another go at reading it, found it to be difficult to read. Presumes the reader knows a lot about XR/VR/AR stuff. Identified some questions, but may have been due to misunderstanging the explainer.

... Skipped **making the "total" field optional** issue.

... Looked at **Scroll-linked animations**, ended up mostly talking about default behaviour of animations when prefers-reduced-motion is on, that was a great discussion but then we ran out of time.

Alice: They left a comment saying they will raise that with the CSSWG.

#### Breakout C

Dan, Alice: Oh yeah, I was there for that

Dan: **WebHID API**... Sangwhan reiterated the feedback that he gave which is that this can be used for cross-origin tracking, unsanctioned tracking mechanism. Said he was going to talk to device authors, pretty important, not ok with spec authors pushing back on this..

Kenneth: Happy with it working on one site at a time, issue is with device working on multiple sites at once...

Dan: Sangwhan's point is that even if it can be made more difficult/annoying that would be a start

... **MathML core**, don't really want to recap this discussion. Links again. Zeroed in on option 1, (the no-op option) - "doesn't require extra work, future proof".

Alice: Hadley had some good points about the level of advice we should give - helping them frame the discussion and encouraging them to bring more people to the table.   I will frame that feedback - the best outcome will depend on these 3 things : the extent to which implementers currently shipping mathml are prepared to unship this href everywhere... ; what use cases there are for linking in mathml to begin with.  On me to leave that comment and then close.

Dan: yes.

Dan: So, that's math. **Client-side video editing** ... closed this. Why did we close this?

Ken: Based on WebCodecs... simple API, they want that, but everyone is pushing for WebCodecs to be the basis, so they have to re-think the API. They shoudl re-file once they've reworked.

Rossen: They are pulling out of this per it's current iteration.

#### MiniApps

Dan: [MiniApps workshop](https://www.w3.org/2020/07/miniapp-virtual-meeting/) ... some aspects of a workshop e.g. talks, deadlines to register. This meeting will precede any finalized charter recommendation of a new working group for miniapps.

... Members of w3c management team, PLH, Jeff, Wendy S, members of Chinese W3C Team attended - everyone on call was sympathetic to the views that we'd posted in the miniapps document but cautious. Went through the feedback we gave at fukuoka - framed the discussion around the 3 reviews we've been asked to do. URI scheme, manifest, lifecycle. They are looking to charter a working group. If a new WG gets chartered, part of that charter is a new miniapps manifest, that would be a problem as we've already given feedback that they shouldn't make a new manifest type - requirements should be folded into the existing webapps manifest, and we have design principles text saying to avoid adding manifests.

... That would be the clearest example of something we would prefer to avoid with miniapps.

... How does W3C Team help guide the miniapp community towards that goal?

... Lots of proposed edits in our doc from the folks on that call. The doc will be made public once we're happy with all the edits - it's a roll-up of feedback on the three issues mentioned earlier.

... Miniapps meeting will be on the 30th and 31st of July and help inform the charter of whatever they're going to propose creating. First item on the agenda for that is our statement; second item is Project Fugu which was another part of the feedback that we gave... they should ... many device APIs being developed elsewhere in w3c, e.g. devices and sensors and WICG, and that we don't want two sets of APIs, don't want a parallel web.

... Security model, certainly don't want a parallel web for miniapps and absolutely not one which has a much weaker security model. Also need to add security to their agenda.

David: Hadley made a point when we were talking about this in Breakout A, which was the connection to origins. Should make sure that's part of our feedback.

Dan: ... miniapps and other types of webapps e.g. PWAs should be interchangeable... share code, share all the benefits of having one platform. 

... Workshop coming up, Sangwhan and I will participate.

#### [Design Principles PRs](https://github.com/w3ctag/design-principles/pulls)

Alice: Should I go ahead and land the style guide?

Dan: Should it be in the Design Principles repo or general repo? That's what stopped us last time.

Tess: Process repo.

Alice: I'll land it in the process repo.

Alice: I made a merged PR...

Rossen: I had a look at one of the long PRs that you posted last week, nothing since then...

... happy to file issues later if you're ready to merge at some point.

Dan: I left some feedback on one of the PRs...

https://github.com/w3ctag/design-principles/pull/219

Alice: David and I had a discussion on that...

Dan: (reads) Ok, fine to leave it as is.

David: I'll think about what needs to be said there.

Dan: Most helpful would be to leave reviews on the individual PRs right?

https://github.com/w3ctag/design-principles/pull/219
https://github.com/w3ctag/design-principles/pull/220
https://github.com/w3ctag/design-principles/pull/221
https://github.com/w3ctag/design-principles/pull/222
https://github.com/w3ctag/design-principles/pull/223
https://github.com/w3ctag/design-principles/pull/224
https://github.com/w3ctag/design-principles/pull/225
https://github.com/w3ctag/design-principles/pull/226
https://github.com/w3ctag/design-principles/pull/227
https://github.com/w3ctag/design-principles/pull/228

... I skimmed the "all edits" PR, didn't see any show stoppers, but want to look more closely at the individual PRs.

#### Issue Triage

Dan: 3 new review requests...

... **[Visibility State Entry](https://github.com/w3ctag/design-reviews/issues/534)**

... From the WebPerf working group. 

Ken: Explainer is a Google Doc...

Dan: ...

David: I often do WebPerf things, I can take a look...

Rossen: I'll join you in learning

David: These APIs are for developer tooling so it's more difficult to explain the user need...

Dan: Assigned, milestone of two weeks.

**[Import Conditions](https://github.com/w3ctag/design-reviews/issues/535)**

Tess: I self-assigned.

Dan: Milestone? 

Tess: 2 weeks sounds good.

**[IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536)**

Ken: One of the pain points with IndexedDB, hard to do bulk (imports?). This is addressing that pain point.

David: Defined in WebApps.

Dan: Putting a milestone of next week. Might be very straightforward.
