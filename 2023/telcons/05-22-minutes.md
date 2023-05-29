## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/05-22-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-05-22](https://www.timeanddate.com/worldclock/converter.html?iso=20230522T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [Spec review for Scroll-driven Animations](https://github.com/w3ctag/design-reviews/issues/828) - @hober, @LeaVerou
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Triage new issues!](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Breakout C (APAC / Europe) - [2023-05-23](https://www.timeanddate.com/worldclock/converter.html?iso=20230523T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon
* [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-05-24](https://www.timeanddate.com/worldclock/converter.html?iso=20230524T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Cookie Pop-Ups Discussion
* Breakout Rollup
* [Issue Triage!](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Call Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/05-22-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-05-22](https://www.timeanddate.com/worldclock/converter.html?iso=20230522T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo

Tess: In tokyo there was less enthusiasm... 

Dan: certainly true for signed exchanges...

Dan: should we put this on the back burner?

Tess: I suspsect so...    I will ping the issue.

ACTION: Tess to ping the folks on the issue (and maybe Kenji).

#### [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Peter: one of the synchronous APIs we think should be async... Some work to make older APIs async?

Tess: all kinds of issues - opacitiy 5%... etc.. API will lie and say it's visible when humans can't see it. If it's being used for ad impression measurement use case then it's not resiliant to fraud. 

Peter: the explainer talks about visibility, opacity, display:none,.. talks about closed shadow tree... talks about 'would it be visible in the viewport'... links to draft spec..

Dan: [asks for an update](https://github.com/w3ctag/design-reviews/issues/734#issuecomment-1557523904)

#### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia

Tess: they want to change it from async to sync because of wasm... "async calls not fully supported on wasm yet"... so ... that **yet** feels important to me.  This is trend we see: Sometimes people want a new feature because some other feature isn't quite right... so this is a stop gap... right way is to fix the other thing...  Isn't the right thing for WASM to make async calls work better?

Peter: in general I agree with you - but also, there has been lots of cases of people creating a stopgap which needs to be supported forever... sometimes the stop gap takes longer than fixing the thing they are working around.

Tess: that said, if this is an API to use from WASM and workers then sync might be the right shape for it... If they are design it only from workers or work like context ... then it might be more ergonimic... broadly share the concern with adding sync apis but maybe it's OK when you can't block the main thread?

Peter: I remember discusson on this - part of this is to make more of a POSIX like layer... seems like we're trying to ad POSIX layer across the web platform...

Tess: e.g. cross-compiling C code... if you can make porting to the web easier then maybe it's a good thing?

Peter: I raised a concern: is it a good thing to turn the web into a POSIX layer?

Tess: they did address my issue in a comment [here](https://github.com/w3ctag/design-reviews/issues/772#issuecomment-1295243104)... [LittlDan commended](https://github.com/w3ctag/design-reviews/issues/772#issuecomment-1293897839) in october that async should be available in WASM in the near future... Does WASM now have adaquate support? [WASM Promises Integration](https://github.com/WebAssembly/js-promise-integration/blob/main/proposals/js-promise-integration/Overview.md) is at Phase 3.

Tess: 

<blockquote>
What's the current state here? Given that the main motivation for this is WASM and the WASM people are saying they are working on it from their end, is it still necessary to have this feature? 
</blockquote>

Tess: [leaves comment](https://github.com/w3ctag/design-reviews/issues/772#issuecomment-1557559477)

#### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
#### [Spec review for Scroll-driven Animations](https://github.com/w3ctag/design-reviews/issues/828) - @hober, @LeaVerou

Dan: positive statements from Safari and Firefox

Lea: lots of activity around this - in the working group as well

Tess: enough flux in the design ? should we try to review this snapshot?

Lea: shipping in Chrome 115 - next major version... I would have liked to look at the syntax more closely... 

Tess: haven't looked at it - the basic ideas using a scrollbar as a tme source is great.

Lea: the explainer is doing a good job.

Tess: these days the web animations spec defines the basic animation model - things like CSS animations and CSS transitions are on that same model. 

Lea: from a quick look looks like this plugs in the same way.

Dan: they've filled out the s&p questionnaire - that looks good.

Lea: seems to be a very well done proper review.

Dan: should we delay..?

Peter: we did a previous review of this and raised some concerns - and it looks like they took care of those... Looks like they took our feedback on board.

Lea: bit of a shame that all of the explainer examples are using the css syntax... However my initial view is that it's pretty good. it covers edge cases... it's built on primitives. A little uncomfortable as haven't had time to look in depth but I like what I see.  I'm inclined to say let's close it.

Peter: I agree. My one concern is that this is overdone... if we make it easier will people abuse it?

Tess: one thing nice about baking it in - is that's in annoying because it's a little off. So making it frame-accurate animation will make it less annoying.

Peter: also prefers-reduced-motion to turn it off.

Lea: also can build extensions to block that particular thing.

<blockquote>
Thank you for taking our previous round of feedback into consideration and making appropriate changes. Also thanks for such a well written, exemplary explainer! We looked at this today during a breakout and we think it looks great. We're happy to see it move forward!
</blockquote>

**CLOSED SATISFIED**

#### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
#### [Triage new issues!](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Breakout C (APAC / Europe) - [2023-05-23](https://www.timeanddate.com/worldclock/converter.html?iso=20230523T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max
Regrets: Hadley, Amy, Yves

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Dan: they got back to us with user needs - it looks better.

Max: could be more detail in the user neeeds.

Dan: Drafts [comment](https://github.com/w3ctag/design-reviews/issues/760#issuecomment-1558672827)

Dan: Developer complexity also an important issue here...

#### [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion

Max: I think the authors are still working on this.  I noticed they have an open issue in miniapp packaging - following the discussion.  Hope for progress in the near future.  Basically they are following our recommendations - and trying to resolve the issues.

#### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
#### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
#### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

[Hadley: regrets for this breakout C, but it looks like it's with Johann. They have put out an intent to ship, but our concerns haven't yet been resolved.]

#### [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon

Max: Yves said we can close this.

Dan: will mark as proposed closed and we can close at the plenary.

#### [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

[Hadley: Regrets for this breakout, but we have asked them to join us for a call after 29 May and are awaiting a response.]

### Plenary Session - [2023-05-24](https://www.timeanddate.com/worldclock/converter.html?iso=20230524T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Max, Dan, Hadley, Peter, Rossen, Lea
Regrets: Amy

https://github.com/w3ctag/design-reviews/issues/833 <-- can we figure out what to do with this?

#### Cookie Pop-Ups Discussion
#### Breakout Rollup

##### Discussion on [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734)

Dan: It *is* already shopped.

Peter: CSS wg has approved it...

Peter: it's on Element...

Dan: Other implementations?

Peter: from [caniuse](https://caniuse.com/?search=checkvisibility) blink and firefox - so at least 2 implementers...

Rossen: so fairly down the path. What can we add?

Peter: I think it's fodder for sync vs/async discussion...

Rossen: I think we should close this one and have the discussion in the principles issues...

Peter: That's reasonable... I'm fine with closing this one... Not sure if we should do the same with the others yet.

<blockquote>
Thanks for that @josepharhar. We discussed again in today's TAG plenary call. Regarding multi-stakeholder support, we also note from [caniuse](https://caniuse.com/?search=checkvisibility) data that there are multiple implementations, which is also not reflected in Chromestatus. Can you please update, or maybe start using the [BCD data](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Page_structures/Compatibility_tables) which powers CanIUse to also power this indication? We still have some reservations regarding sync vs. async as [plinss highlighted](https://github.com/w3ctag/design-reviews/issues/734#issuecomment-1162190144) however we are going to move that discussion to our Design Principles work.
</blockquote>

Peter: fine closing it with concerns.

Dan: closed with "satisfied with concerns" label.

##### RequestStorageAccessFor

Hadley: sounds from Johan's last comment that they want us to leave it with them...  So should still be open.


<blockquote>
Thanks @johannhof, we'll keep this open for now. For our TAG processes, we are keen to not let issues stand open and inactive for too long, so we'd be grateful if you could give us a quick update within 3-4 weeks at the most.

  </blockquote>
  
#### [Issue Triage!](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

