### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/02-08-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-02-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210208T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo
* [WebXR Lighting Estimation](https://github.com/w3ctag/design-reviews/issues/574) - @torgo, @atanassov
* [Web page settings to save battery](https://github.com/w3ctag/design-reviews/issues/546) - @hober, @kenchris, @hadleybeeman
* ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @dbaron, @ylafon
* [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @atanassov
* dip into triage/re-triage list below

### Breakout B (US / APAC) - [2021-02-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210209T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* dip into triage/re-triage list below

### Breakout C (APAC / Europe) - [2021-02-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210209T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Periodic Background Sync](https://github.com/w3ctag/design-reviews/issues/367) - @ylafon, @kenchris
* [hasDroppedEntry in PerformanceObserverCallback](https://github.com/w3ctag/design-reviews/issues/547) - @LeaVerou, @kenchris
* ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @dbaron, @ylafon
* dip into triage/re-triage list below

### Plenary Session - [2021-02-10](https://www.timeanddate.com/worldclock/converter.html?iso=20210210T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Finalize plans for next virtual f2f
* Issue Triage

### Triage & Retriage List

* [azimuth](https://github.com/w3ctag/design-reviews/issues/537)
* [media source extensions](https://github.com/w3ctag/design-reviews/issues/576)
* [floc API](https://github.com/w3ctag/design-reviews/issues/601)
* [insertable media processing](https://github.com/w3ctag/design-reviews/issues/603)
* [webotp API](https://github.com/w3ctag/design-reviews/issues/604)
* [app history](https://github.com/w3ctag/design-reviews/issues/605)
* [webxr dynamic viewport scaling](https://github.com/w3ctag/design-reviews/issues/588)
* [declarative link capturing](https://github.com/w3ctag/design-reviews/issues/589)
* [modal close signals](https://github.com/w3ctag/design-reviews/issues/594)
* [managed device](https://github.com/w3ctag/design-reviews/issues/606)
* [DOM review draft](https://github.com/w3ctag/design-reviews/issues/573)
* [Web auth level 2](https://github.com/w3ctag/design-reviews/issues/577)
* [multi-screen window placement](https://github.com/w3ctag/design-reviews/issues/602)
* [HTML spec treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)
* [scroll linked animations](https://github.com/w3ctag/design-reviews/issues/521)
* [webxr depth API](https://github.com/w3ctag/design-reviews/issues/550)
* [css color adjust level 1](https://github.com/w3ctag/design-reviews/issues/583)

### Issues older than one year

* [WebXR AR Module](https://github.com/w3ctag/design-reviews/issues/462)
* [webxr DOM overlay](https://github.com/w3ctag/design-reviews/issues/470)
* [webxr hit test](https://github.com/w3ctag/design-reviews/issues/463)
* [font enumeration](https://github.com/w3ctag/design-reviews/issues/399)
* [serial API](https://github.com/w3ctag/design-reviews/issues/431)
* [get installed related apps](https://github.com/w3ctag/design-reviews/issues/436)
* [background sync](https://github.com/w3ctag/design-reviews/issues/367)
* [web socket stream](https://github.com/w3ctag/design-reviews/issues/394)
* [webtransport](https://github.com/w3ctag/design-reviews/issues/389)
* [editcontext API](https://github.com/w3ctag/design-reviews/issues/416)
* [trusttoken API](https://github.com/w3ctag/design-reviews/issues/414)
* [webHID](https://github.com/w3ctag/design-reviews/issues/370)

### Issues older than 2 years

* [RTC ICE Transport](https://github.com/w3ctag/design-reviews/issues/304)
* [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311)



## Minutes

### Breakout A (Europe / US) - [2021-02-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210208T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Amy, Peter, Kenneth, Dan, Lea, Rossen, Hadley, Tess

Regrets: Yves


#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo

Tess: mounir replied that the underlying webxr platform also does what I asked about (matrices).  Why not use DOM Matrix?   Might have to send that back to WebXR group.

Rossen: this might be inertia about what they're used to.   It's a good point though.

Tess: I will file an issue on the main WebXR issues tracker about it.

Rossen: would this hit testing allow pixel readbacks

Tess: I think it's real-world only; they said virtual was "just a matter of maths (sic)"

Rossen: combining virtual and realworld testing.

Rossen: pixel reduxing would have a dependency on the graphics subsystem which would be pretty bad... as soon as you go to readback the values you have to sync the pipeline.  I will go through the proposal.

Dan: Let's try to revisit in the plenary. I will bump one mor week.

Rossen: needs use cases and test cases.

#### [WebXR Lighting Estimation](https://github.com/w3ctag/design-reviews/issues/574) - @torgo, @atanassov

[bumped 2 weeks]

#### [Web page settings to save battery](https://github.com/w3ctag/design-reviews/issues/546) - @hober, @kenchris, @hadleybeeman

Ken: no update since last comment...

Dan: i will ping Chris Harrelson and we can revisit in the plenary.

#### ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @dbaron, @ylafon

Amy: not much to report - David said looks reasonable but a lot to digest. Recent comments from today.

#### [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @atanassov

[relationship to 1st party set is an issue]

[discussion on how this depends on privacy budget and how privacy budget is not a well defined concept at this point]

Tess: large ecommerce sites often have 100s of domains that they own.. Amazon.co.uk, amazon.mx, etc... All of their national TLDs are the same set. That might be reasonable but once you get into high numbers like that then the potential for abuse skyrockets.  Ad-tech companies might abuse this. 

Dan: what's the mitigation being discussed in the Privacy CG for this?

Tess: the mitigation linked to here is that the privacy budget would apply across all sites across the first party set. Another mitigation would be to limit the size to 10 or 20 domains.  Once you get into high numbers then the harm of using it as a tracking vector overrides the benefit.

Rossen: where is the ... expanding and registering domains that are part of the set? Who registers the sets?

Tess: every party in the set needs to declare.

Rossen: legit subsidiary issues.  Also enterprises with different companies.  Does current 1st party set thinking consider these the same? Or is there a grey line?  All of your TLDs around the world.

Tess: don't know if you draw that distinction

Hadley: this is companies saying "we understand the same origin policy but we're annoyed by it so we want to scrap it in certain circumstances".

Tess: there are multiple reasons why you might want to have these sets - different properties (all the same legal entity, vs looser...)

Tess: what's tricky here is that 1st party sets is agnostic. Doesn't say what they use it for.  Same party cookies are the first example of an application of 1st party sets.  Rossen identified at least 2 cases that are interesting. I think there are more.  There could be a way to share a set of domains that share certain aspects - e.g. ethical principles...

Hadley: it reminds me of a proposal from the IAB (the advertising one)- they wanted to let brands designate places that could sell their stuff legitimately. They could use that to cut down on counterfeiting.

Rossen: what is the governance model for this?  Do we have a def of that?

Tess: not sure if there is any kind of governance.

Ken: they are sending an intent to experiment.

Dan: you would end up with defacto browser allow lists of which 1st party sets are ok

Tess: and then you have the compatiility problem.. different browsers have different lists, it's a race to the bottom

Hadley: rife for conflicts of interest.  Crosses out of user agents...

Rossen: the whole domain registry well-established governance model shifts completely.

Dan: this is a destabilizer.

Dan: doesn't this fundamentally harm web architecture? 

Rossen: should we reopen first party sets? and continue the conversation there. It's no longer "too early".

Hadley: same people? no

Rossen: some similar folks, and much livilier discussion

Hadley: 342 has discussion around governance but doesn't really conclude

Dan: [left a comment](https://github.com/w3ctag/design-reviews/issues/595#issuecomment-775327058) redirecting back to the first party sets issue.

Hadley: will leave a comment on that issue.

#### dip into triage/re-triage list below

### Breakout B (US / APAC) - [2021-02-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210209T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Peter

Regrets: Rossen

Lack of quorum.

#### dip into triage/re-triage list below

### Breakout C (APAC / Europe) - [2021-02-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210209T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Ken, Dan, Amy, Lea, Sangwhan

Regrets: 

#### [Periodic Background Sync](https://github.com/w3ctag/design-reviews/issues/367) - @ylafon, @kenchris

Ken: [issue](https://github.com/WICG/periodic-background-sync/issues/3) filed 10 days ago...  Don't think we'll get any further since this is shipping. I think we should close. We've given our feedback and they've ack'ed it. 

Dan: Ok with me.

[set to proposed close]

#### [hasDroppedEntry in PerformanceObserverCallback](https://github.com/w3ctag/design-reviews/issues/547) - @LeaVerou, @kenchris

Lea: he implemented our suggestions but not sure about this name. Not sure about names with these abbreviations. Is there a precedent? Do we have other web platform properties with "num"?

[discussion on use of abbreviations]

Hadley: we have design principles about naming - use common words, etc... 

Lea: nothing about abbreviations...

Hadley: it does say "easily readable US english" - and arguably abbreviations are not readable.

Ken: we should definitely use *Count - for consistency.

Examples - 
`animation-iteration-count
column-count in CSS
ParentNode.childElementCount
MediaTrackConstraints.channelCount`

Dan: let's leave some feedback along those lines and propose closing.

#### ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @dbaron, @ylafon

Dan: let's schedule a breakout on this at the plenary.  Maybe we can get Mike to join as well.

### [webHID](https://github.com/w3ctag/design-reviews/issues/370)

Sangwhan: we just need a final comment from them to close it off... Some final changes.  Same goes for Serial.

### [serial API](https://github.com/w3ctag/design-reviews/issues/431)

Sangwhan: it's proposed closed.

Dan: Let's close it at the plenary.

Samngwhan: **WebXR hit test**, **Serial API**, *WebHID**, **WebSocketStream**, **BackgroundSync**, **getinstalledrelatedapps** -- all proposed closing.

Dan: I suggest we go through those and close them in the plenary.

Sangwhan: **RTCICEtrnasport** - i had a call with DOM on this and am doing work. **TemporalProposal** changed very recently. 

Amy: **FLOC API**

### [floc API](https://github.com/w3ctag/design-reviews/issues/601)

Amy: a few red flags... 

[discussion of whether this fixes any problems with current ad-tech]

Ken: I don't think it helps...

Amy: I'm worried it centralizes grouping - under control of the browsers - using machine learning.

Sangwhan: fairly transparent - the alg. they are using is transparent.  Anyone can implement it.

Ken: like privacy sandbox

Sanfwhan: spin-off from privacy sandbox- instead of identifying users you identify someone as part of many groups... 

Lea: a permission?

Ken: no, but you have to opt in.

Sangwhan: i think the idea is to support it by default.

Amy: I worry about the anonymizing - youre anonymous but only in a group of x-thousand people.

Lea: are users able to change these if they think they are incorrect.

Sangwhan: I think you could scrub your history.

Lea: could still be generated incorrectly. A lot of websites that track you today allow the user to change things. It seems reasonable to give that control to the user.

Amy: sensitive categories - somne of the cohorts could be sensitive like protected classes...

Ken: what about the VPN - change country.  

Dan: what happens if you have a shared computer - like a school computer?

Amy: their answer to protected classes is "we won't do it" but need more detail.

[assigned and set for next week]

#### [azimuth](https://github.com/w3ctag/design-reviews/issues/537)

Sangwhan: angle of the pen in pointer events... 

Dan: let's discuss it at the plenary.

#### [insertable media processing](https://github.com/w3ctag/design-reviews/issues/603)

Sangwhan: I just triaged and assigned myself. 

[set milestone]

#### webotp

[ken and sangwhan assigned]

[set milestone]

#### [css color adjust level 1](https://github.com/w3ctag/design-reviews/issues/583)

Lea: assigned myself...   Not prepared to discuss now. 

[set to next week]

#### [app history](https://github.com/w3ctag/design-reviews/issues/605)

Sangwhan: [assigned and milestoned]

#### [managed device](https://github.com/w3ctag/design-reviews/issues/606)

Sangwhan: we need some security expertise here...  Not sure if this should be part of the web.  Feels like something that is part of chromeOS - leak a unique identifier to specific web sites - for managed enterprise environments.  That's my first impression.

Ken: I'm sure MS would want the same thing.

Dan: Fugu thing?

Sangwhan: I don't think so.

Ken: It's about enterprise... 

Sangwhan: there is something called "Chrome Enterprise"... lets you centrally control extensions in Chrome for employees... 

Dan: so why in WICG?

Ken: if you have to have a proprietary API for each platform...

Amy: what does a standard API solve? so an employee could choose the browser that controls them?

Ken: yes...

[...discussion on whether you need a standardised API...]

Amy: in that situation they might tell you what browser to use anyway...

Ken: you can have multiple browsers - all managed...

Amy: I don't know if it's a bad thing to increase friction for that. If they need to implement for different browsers. Anything that discourages ...

[vigorous debate of whether "the enterprise" belongs in the standardization process]

Dan: what's Apple's opinion? What's igalia's opinion?

Sangwhan: this is likely to be a chromium-specific feature. 

Dan: that also brings up the question of why do this in W3C?

Ken: we could end up with a better result if it's done in w3c...  make it as good as possible.

Lea: no strong opinions but that sounds reasonable...

Sangwhan: Ok with the use case not entirely comfortable with the venue...  Concerned.

[went over time - let's discuss further at the plenary]

### Plenary Session - [2021-02-10](https://www.timeanddate.com/worldclock/converter.html?iso=20210210T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Amy, Lea, Tess, Peter, Dan

Regrets: 

#### Breakout Rollup

Dan: **Hit test module** we said we'd revisit.. 

Tess: Rossen was going to look into something

Dan: **WebXR lighting estimation** bumped 2 weeks. **Settings to save battery**, no update since last comment, I pinged Chris Harrelson who [responded on the TAG review](https://github.com/w3ctag/design-reviews/issues/546#issuecomment-775365986). We said there seem to be privacy and security issues that need to be spelled out. Chris is saying it was an early review, we got feedback, if we proceed we'll file another review. Close?

Tess: we have a resolution state for it's too early

Dan: closing and suggesting new issue for a full review

... **credentialless embedder policy**. We said we'd schedule the breakout at the plenary... we'll do it on slack.

... **same party cookie** attribute, we discussed and reopened first party sets. Hadley was going to write a comment about the discussion we had. I raised to the attention of Chris as well since it's from Google.

... **periodic background sync** we proposed closed.  It's closed by the requester.

... **hasDroppedEntry in performance observer callback** we left feedback on the name and proposed close, I think we should close it.

Lea: they applied the new name already.. said they will.

Dan: closed with comment

... **WebHID** we need a final comment to close it off, we still need to do that, pending Sangwhan.

... **serial API** also propose closed, comment from yesterday.. pending some additional feedback from Reilly, will relabel.

... **FLoC API** some red flags

Tess: it's worked on in WICG and discussed in web advertising business group

Dan: lots of privacy concerns, Peter self assigned

Peter: very similar to something I was thinking earlier, I would like to see a browser signal that I *don't* want to see certain kinds of ads. Things like if you're an alcoholic you shouldn't be seeing ads for alcohol. Be nice to have some kinds of signal saying opt out of certan categories while still being privacy preserving. Broad signal. Not I'm not interested, but this is harmful to me.

Dan: **azimuth** we said we'd discuss at the plenary. Tess is assigned.

Tess: off the top of my head.. I think the issue was that the informatin that the api had about the orientation of the pen relative to the display wasn't in its most immediately useful form, in that for the typical use cases where you need to know the orientation of the pen it required you to do some math to do some numbers you need. The proposal was to expose the numbers everyone has to calculate anyway. It's additive, they're keeping the old numbers and providing the more useufl varients. I think it's fine, but I might be remembering a different issue.. it seems totally reasonable. It's small addition to a spec that eliminates a potential class of bugs so developers dn't need to do math themselves, and improves the usability of the API. But not something I'm an expert in. Be nice to have someone else look at it to.

Dan: Sangwhan also seemed to be interested. It's just an addition to an existing api, doesn't expose any additional information than is already being exposed.

Tess: it shouldn't add to fingerpriting surface unless you imagine a bizaare scenario where the underlying hardware has sme kind of quirkyr eporting and doesn't natively report this kind of data so the user agent has to do math to expose it and the quirky behaviour plus the math reveals you have this pen and not that pen. That's a real stretch fingerprinting wise and it would give you very little actual information so I don't think there's anything to worry about here.

Dan: shall we just close it?

Tess: has Sangwhan commented?

Dan: no, we just discussed it. He didn't say hold off I have issues or anything like that, so I think it's okay if we close it. 

Tess: I will [write a closing comment]()

Dan: **insertable media processing** sangwhan assigned and we set a milestone. **webotp** ken and sangwhan assigned.

Tess: can I be on webotp? I'm working on this, although I didn't request the review.

Dan: **CSS color adjust level 1**

Lea: No progress since last discussed. We left a comment, there was no response since then. 29 days ago.

Dan: does anybody else want to be assigned to this? 

Tess: you can add me. is this also the dark mode stuff?

Lea: also the dark mode stuff

Dan: **app history** we assigned and milestoned

... **managed devices** .. aimed at the enterprise space, device management, at the web level. We had a debate on this. Sangwhan has concerns. It's not clear there's much additional implementer interest other than google. Interested to know if there's interest from Apple. Amy expressed concerns, I share, about anything that removes control of computer somebody is using. Unintended consequences, ways I can imagine it being used outside (or inside) the enterprise space. In particular device management stuff is used for parental control stuff.  We need to have a wider discussion. We had a comment from nightpool which is interesting. We need to put some effort into this one.

#### Finalize plans for next virtual f2f

Lea: constraints from Sangwhan - not second week of May (3-6 May). I proposed third week in May. I wouldn't be able to do 17th.

Dan: 10-15th

Tess, Peter, Amy: fine.

Dan: proposing on slack.

#### Issue Triage

Dan: everything triaged. Lots proposed closed. Can we close 573?

Tess: yeah, Alice and I looked at it, it's closeable.

Dan: closes with comment

