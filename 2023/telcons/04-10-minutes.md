## Call Agenda

### Breakout A (Europe / US) - [2023-04-10](https://www.timeanddate.com/worldclock/converter.html?iso=20230410T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [(Document Subtitle): Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo
* [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman
* [Background Blur API](https://github.com/w3ctag/design-reviews/issues/826) - @torgo
* [Early design review: scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/827) - @hober, @plinss
* [Spec review for Scroll-driven Animations](https://github.com/w3ctag/design-reviews/issues/828) - @hober, @LeaVerou

### Breakout C (APAC / Europe) - [2023-04-11](https://www.timeanddate.com/worldclock/converter.html?iso=20230411T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

Taking a look at [response on topics review](https://github.com/w3ctag/design-reviews/issues/726#issuecomment-1501975149).

Also context: https://privacysandbox.com/intl/en_us/news/working-together-to-build-a-more-private-internet/

*Discussing what we can do in Tokyo with this...*

Amy: I'm around async for f2f...

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman
* [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss
* [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman
* [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro
* [Review of DPUB-ARIA 1.1 and DPUB-AAM 1.1](https://github.com/w3ctag/design-reviews/issues/821) - @rhiaro

### Plenary Session - [2023-04-12](https://www.timeanddate.com/worldclock/converter.html?iso=20230412T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes 

### Breakout A (Europe / US) - [2023-04-10](https://www.timeanddate.com/worldclock/converter.html?iso=20230410T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Rossen, Dan
Regrets: Hadley

#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Rossen: we need to move this forward in a focussed way. 

Dan: I assigned Lea. Let's put this on the agenda for next week and tackle it with Lea and Tess if possible Rossen (remote) to chat on a breakout at the f2f.



#### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

Dan: Josh has [responded to our questions](https://github.com/w3ctag/design-reviews/issues/747#issuecomment-1482807424)... 

Dan: Finding this difficult to parse … particularly the response to how this fits together with other privacy sandbox initiatives...

Rossen: clarification is warranted... also not seeing this from their explainer... 

Dan: we're also reviewing `requestStorageAccessFor`... I'm concerned about developer complexity. I still don't understand when a developer would use each of them...

Peter: Mozilla's standards position is negative... linked in the issue.

Peter: I'm concerned about output gating of this. Anyone can write into the shared storage but reading is restricted. Seems like the output gating is entirely based on budget. Budgeting approach here is completely inadiquate.

Dan: I'll also note the user needs are not well articulated in the explainer. 

Peter: all the needs are advertising based... 

Peter: my concern - i don't see how it protects user privacy. Budgeting just allows user privacy to be violated by a small set of entities...

Rossen: *[leaves comment](https://github.com/w3ctag/design-reviews/issues/747#issuecomment-1502037976)*

#### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

*punt to plenary*

#### [(Document Subtitle): Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo
#### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman
#### [Background Blur API](https://github.com/w3ctag/design-reviews/issues/826) - @torgo

*We agree to close with *satisfied with concerns* : see https://github.com/w3ctag/design-reviews/issues/826#issuecomment-1502014618 for closing comment.*

#### [Early design review: scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/827) - @hober, @plinss



#### [Spec review for Scroll-driven Animations](https://github.com/w3ctag/design-reviews/issues/828) - @hober, @LeaVerou

### Breakout C (APAC / Europe) - [2023-04-11](https://www.timeanddate.com/worldclock/converter.html?iso=20230411T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### post 3p cookies finding

*we agree to take the current text from the design reviews repo and move it into its own repo, ready to publish as a finding*

*We deploy on https://w3ctag.github.io/web-without-3p-cookies/ and start a new repo https://github.com/w3ctag/web-without-3p-cookies*

*Abstract Noodling that did absolutely not come from ChatGPT:*

This finding discusses the deprecation of third-party cookies, the reasons for restricting them, and the challenges in removing them from the web platform. We highlight some use cases that depend on third-party cookies and offer some examples of designed-for-purpose technologies that can replace them. Specification authors are expected to ensure they do not undermine the benefits of removing third-party cookies when proposing new web platform technologies.

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman
#### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
#### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
#### [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman
#### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss
#### [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman
#### [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro
#### [Review of DPUB-ARIA 1.1 and DPUB-AAM 1.1](https://github.com/w3ctag/design-reviews/issues/821) - @rhiaro

### Plenary Session - [2023-04-12](https://www.timeanddate.com/worldclock/converter.html?iso=20230412T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Sangwhan, Yves
Regrets: Hadley, Lea, Peter, Max

*we held a short meeting focusing on f2f logistics for next week*

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
