## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/08-21-agenda.md).

### Breakout A (Europe / US) - [2023-08-21](https://www.timeanddate.com/worldclock/converter.html?iso=20230821T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
  * https://github.com/w3c/edit-context/issues/38
  * https://github.com/w3c/edit-context/issues/53
  * https://github.com/w3c/edit-context/issues/54
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov
* [TAG spec review of Bounce Tracking Mitigations](https://github.com/w3ctag/design-reviews/issues/862) - @hober, @hadleybeeman

### Breakout C (APAC / Europe) - [2023-08-22](https://www.timeanddate.com/worldclock/converter.html?iso=20230822T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @cynthia, @torgo, @ylafon
* [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
* [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo

### Plenary Session - [2023-08-24](https://www.timeanddate.com/worldclock/converter.html?iso=20230824T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Call Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/08-21-agenda.md).

### Breakout A (Europe / US) - [2023-08-21](https://www.timeanddate.com/worldclock/converter.html?iso=20230821T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Yves, Hadley, Peter, Rossen
Regrets: Lea

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
  * https://github.com/w3c/edit-context/issues/38
  * https://github.com/w3c/edit-context/issues/53
  * https://github.com/w3c/edit-context/issues/54
#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

Rossen: will work this week on it with Sangwhan.

#### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov



https://github.com/w3ctag/design-reviews/issues/846
#### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

Dan: Lots of proposals in this space...

Rossen: Hard to figure out the overlapping / competing functionality

Dan: IPA has meta and mozilla working together.. private aggregation is google.. private click measurement is apple (not submitted for tag review but is implemented).. and attribution reporting (google). Some may or may not have a relationship with protected audience?

Amy: and shared storage

Dan: in attribution reporting, 3 weeks ago we asked how it relates to this one.. I'd like an explainer on how these things fit together.

Amy: ... protected audience, topics .. all use specialist language - specific to the ad tech industry - we should ask for any explainer to not use this kind of language, it's very complex and there's a lot of nuance

Hadley: e.g. difference between targeted advertising vs remarketing

Dan: we dont' need to become adtech experts in order to understand. They need to limit their use of terms of art from the adtech world to explain them from a web development perspective

Hadley: agree

Rossen: agree. To better understand are these apis useable only for adtech, or for something else? To me that's unclear.

Amy: we could ask the PATCG to put together a comparison matrix, and various stakeholders can fill it in for their specs. I'm not sure exactly what would go in the matrix, they're better placed to provide that

Dan: who is representing them?

Hadley: Aram Zucker-Scharff and Sean Turner. They have a mailing list.

Yves: was thinking of Nick Doty..

Dan: [emails Nick]

#### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
#### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov

Yves: isn't the information served from the cache a possible issue? if you do that effectively but add some delay to make it so it doesn't look like it was served from the cache? we were discussing mitigations on double key cache and a way to use the cache without ... I would like to look at this

Rossen: we had a long conversation during the f2f that we didn't capture in notes...

#### [TAG spec review of Bounce Tracking Mitigations](https://github.com/w3ctag/design-reviews/issues/862) - @hober, @hadleybeeman

Amy: [good comments]... Would like to ensure they work in a collaborative manner... 

Hadley: could we close it saying we like the design but that we'd like to see more multi-stakeholder engagemet and we'd like to see it again when it's more mature.

*agreed to close*

### Breakout C (APAC / Europe) - [2023-08-22](https://www.timeanddate.com/worldclock/converter.html?iso=20230822T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Torgo, Amy, Hadley, Yves, Sangwhan

#### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

*some discussion on how this relates to Topics*

*discussion on how ad blockers or ad blocking web browsers might not implement or disable these ad tech specific APIs*

Amy: locally executed decision about what ad to show instead of executed on the server...

[discussion about "ad creatives"]

Sangwhan: [glossary about video](https://www.iab.com/wp-content/uploads/2016/04/Glossary-Formatted.pdf). [Wider glossary now gated behind a login](https://www.iab.com/insights/glossary-of-terminology/)

Dan: what does "temporarily relaxed version of a Fenced Frame" mean? Does fenced frames not service their use case? Can we clarify?

Amy: it would be helpful if there was a glossary from the PATCG... 

Dan: the explainer should be self contained and explain the advertising jargon they use

Amy: we can add a bit to the issue template that says "are there any specialist terms of art you use in your explainer? Please include a link to your glossary here"

Dan: added issue https://github.com/w3ctag/process/issues/32

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Yves: interesting discussion in mozilla standards proposal discussion about reliability : https://github.com/mozilla/standards-positions/issues/691 - the issue is about subframe navigation.

Sangwhan: [re the previous discussion at the f2f] I can get started on a design principle on this...

Sangwhan: I think the [multi-stakeholder situation is improving] - mozilla although they only have partial support for permission policy...

*bumped 2 weeks*

#### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo

Dan: proposed closed, but have concerns about multiple browser support. Any further information since July?

Sangwhan: Probably some of this is going to launch.. [experiment](https://www.iab.com/insights/glossary-of-terminology/) ongoing

Dan: based on discussion at the f2f the concerns were not applicable to the latest version.. that they'd been addressed?

Sangwhan: yes, it's been completely redesigned

<blockquote>
Hi Anssi - thanks for this review. We're generally happy with the design and the articulated user needs. We remain concerned about multi-stakeholder support. We note that this API is going to experimental implementation. We'd be interested to review the results of that experiment. Thanks! 
</blockquote>

**closed**

#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @cynthia, @torgo, @ylafon

**Sangwhan to reach out**

#### [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro

Dan: they replied to Peter's comments. We should ask Peter.

*bumped to plenary*

#### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

Sangwhan: we have [responses](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1673246468)..

Dan: this is good well written information. They argue it's better than the current situation, but I'm left with the feeling this is a stop gap. I'm concerned it can become the permanent solution. How do we stop that from happening?

Hadley: that's something we talk about regularly. We dont' have a design principle about that do we?

Sangwhan: Nothing can really stop that from happening. 

Hadley: We could design more permanent solutions..

Sangwhan: they're designing around pci restrictions. It's either do this or don't do anything.

Amy: in general we could ask for deprectation paths as part of the design

Dan: we could ask if they have that

Sangwhan: whether they can do it..

Hadley: at some point pci is going to change

Sangwhan: I think that's the hope. if we have evidence we can provide a secure transaction experience while also being able to provide customisability, keeping security guarantees intact. PCI is a fundamental distrust in transactions on the internet overall.

<blockquote>
Hi Stephen - thank you for this really clearly written summary and response to our feedback - it's greatly appreciated! We discussed again in today's TAG breakout. We're still concerned that this is a stop gap in anticipation of WPWG coming up with a better long-term solution?  Do you have an idea for how we can stop the stop gap from becoming the de facto permanent solution?  
</blockquote>

#### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
#### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo

### Plenary Session - [2023-08-24](https://www.timeanddate.com/worldclock/converter.html?iso=20230824T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Dan
Regrets: Max

#### "Web not versioned" finding?
#### Move breakout C a half hour later?

*we agree to trial this*

#### Breakout Rollup

*we go through breakout C*

#### [blobs](https://github.com/w3ctag/design-reviews/issues/820)

Peter: I'm happy to close.

**peter to close and leave closing comment**

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

