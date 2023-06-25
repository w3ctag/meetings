## Call Agendas

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/06-19-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-06-19](https://www.timeanddate.com/worldclock/converter.html?iso=20230619T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov
* [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov

### Breakout C (APAC / Europe) - [2023-06-20](https://www.timeanddate.com/worldclock/converter.html?iso=20230620T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss
* [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman
* [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman
* [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo
* [RDF Canonicalization](https://github.com/w3ctag/design-reviews/issues/855) - @rhiaro, @hadleybeeman
* [API for capturing all screens](https://github.com/w3ctag/design-reviews/issues/856) - @torgo, @rhiaro, @hadleybeeman
* [VC-JWT](https://github.com/w3ctag/design-reviews/issues/857) - @rhiaro, @hadleybeeman
* [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20230621T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* debrief from Privacy Sandbox session
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2023-06-19](https://www.timeanddate.com/worldclock/converter.html?iso=20230619T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves
Regrets: Hadley, Amy...

Dan: NB: it's a holiday in the US today so we might have low attendence.

#### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia
#### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
#### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman
#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
#### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
#### [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov
#### [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss
#### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov

### Breakout C (APAC / Europe) - [2023-06-20](https://www.timeanddate.com/worldclock/converter.html?iso=20230620T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### Discussion on Privacy Sandbox Breakout

Dan: one concrete action - could we host a breakout session about `requestStorageAccessFor()` where we bring together webkit and chromium (and Mozilla) folks. It seems there was a genuine technical misalignment - maybe we could play a role in helping to sort out.  Dan to reach out to Michael about it.

**timeline for eow to publish last week's minutes, giving Michael a chance to review**

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
#### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss


Amy: They've asked "since there's no new API should we close this review"?

Yves: and they've said they align with firefox.

**set to proposed closing and bumped to f2f to close**

#### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

**no feedback since last week**

#### [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss

Max: Had a quick look at this one - straightforward proposal.  No explainer. They've provided slides to explain the requirement. Enables the change of active codec without renegotiation of the session... They've designed an API...  They haven't provided an explainer...

Dan: it's in the webrtc wg.  Wondering what the multistakeholder story is...

Max: we can ask them to provide multistakeholder info togetehr with the explainer...

Dan: **leaves comment**

#### [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman

**bumped**

#### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman

Hadley: no security & privacy review... There's a security considerations section of the explainer...  They do mention the scenario I was worried about - giving the site the ability to replace the title bar you could spoof the titlebar.  To mitigate this threat they've only made it available for "[isolated webapps](https://github.com/w3ctag/design-reviews/issues/842)"

Dan: so there's a dependency on isolated webapps...  Which is also in our review queue.

Sangwhan: this is less complicated than isolated webapps - but some intesting risks. URL bar spoofing, phishing, etc... some gates to prevent that.  Not likely that it would happen.

Hadley: I think it would be good that we'd like it to stay in that explicit context.  It says in the explainer "at least for now" only in isolated webapps..

Sangwhan: overall... PWAs give more customizability... whether that's the correct choice given that the user has chosen to install the application... 

Dan: can we clarify what exactly this is doing because to my understanding PWAs can already come up "full screen"... 

Sangwhan: not zero risk but less risky than letting regular PWAs to do it.. 

Yves: relationship between Isolated webapps and miniapp...

Sangwhan: philisophical difference between IWAs and miniapp.. 



#### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo
#### [RDF Canonicalization](https://github.com/w3ctag/design-reviews/issues/855) - @rhiaro, @hadleybeeman

**bumped**

#### [API for capturing all screens](https://github.com/w3ctag/design-reviews/issues/856) - @torgo, @rhiaro, @hadleybeeman

Dan: Do we need this in the web platform itself? isn't his better put at the system level?  Why does this need to be in a browser API?

Sangwhan: Proctored exams (monitored exams), monitoring employee productivity, call centers...

Amy: it says it's behind an enterprise policy - we've pushed back before on this kind of surveillance in the web platform ... eg. [managed device API](https://github.com/w3ctag/design-reviews/issues/606)

Hadley: aren't enterprise policies usually at the OS level?

Dan: we said fine if they want to add it to Chrome as their own thing, but maybe not appropriate for standardisation

Sangwhan: jist is that the proctored test is usually a web application - on the web. You'd either have to make a native application to do the same thing - which is what is going on right now  - this moves some of that horrible stuff to the web.  I can see who wants to use it and why it makes sense...  You can give the user a capture that this is being captured... User permission requested.  In the browser. In native code, all bets are off. In that sense I think it's better than being in native.

Amy: they don't list exams as one of their use cases...

Hadley: I'm hesitant to respond to a use case they haven't made explicit.

Yves: if it's an enterprise based installation, they can probably install a native extension to chrome that may be needed for the same thing. Dangerous to have that avalable for everyone on the web.

Amy: they don't go into detail about the end user needs, just high level summary use cases

**Sangwhan to leave a comment**

#### [VC-JWT](https://github.com/w3ctag/design-reviews/issues/857) - @rhiaro, @hadleybeeman
x
**bumped**

#### [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman

**bumped**

### Plenary Session - [2023-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20230621T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Peter, Max, Hadley, Amy (2nd half)
Regrets: Lea, Sangwhan

#### debrief from Privacy Sandbox session

Dan: Maybe do something with `requestStorageAccessFor()` - 

Hadley: maybe discussion was also for shared storage API?  We shouldn't be in a position of being the champion of a proposal because stakeholders aren't getting along... that's not our role.

Hadley: our involvement should be under the "user need" not the specific api.

Dan: picking up the discussion on PSL...

Peter: I could see how FPS could replace the PSL but they are not built for the same purposes. I see them as orthogonal

Hadley: They are tangential, I think. I could see maybe a w3c workshop on future of PSL ... FPS could be a small part of that discussion, but not the centrepiece.

Yves: PSL not in IETF, or ICANN... I feel it should be in ICANN.  e.g. timezone registry - is maintained by one person.  Fragile.  I can raise that to W3C strategy.

Hadley: should we do something in parallel about getting rid of 3rd party cookies... all the work is happening in Privacy Sandbox or PATCG... People haven't come together to think about the situation.... Replacements for 3pc...   I think it would he helpful to do that work... More of a mandate across the w3c that this is a useful direction to go.

Yves: moving ethical web principles to a statement could help...

Dan: how to advance ewp? 

Dan: we could add an acknowledgements section... 

Yves: we need to demonstrate horizontal wide review...   We need a formal wide reviews from horizontal reviews in w3c.  We should also ack the whole TAG.  It would be good to ack the feedback we got ... 

#### Breakout Rollup

*Closed 813*



#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
