# TAG Minutes Doc - Week-of Mon, 28 November 2022

## Call Agenda

The agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/11-28-agenda.md).

### Breakout A (Europe / US) - [2022-11-28](https://www.timeanddate.com/worldclock/converter.html?iso=20221128T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [Design and specification review of CSS Container Queries Style Features](https://github.com/w3ctag/design-reviews/issues/787) - @LeaVerou

### Breakout C (APAC / Europe) - [2022-11-29](https://www.timeanddate.com/worldclock/converter.html?iso=20221129T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* https://github.com/w3ctag/design-reviews/issues/762#issuecomment-1328793218
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon
* [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion
* [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon
* [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman
* [Content-type in Resource Timing](https://github.com/w3ctag/design-reviews/issues/785) - @maxpassion

### Plenary Session - [2022-12-01](https://www.timeanddate.com/worldclock/converter.html?iso=20221201T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780) - @hober, @torgo, @hadleybeeman, @plinss
* [WebXR Device API XRSession::enabledFeatures attribute (CR Delta)](https://github.com/w3ctag/design-reviews/issues/782) - @torgo, @maxpassion, @atanassov
* [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro
* [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia
* [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

## Breakout A (Europe / US) - [2022-11-28](https://www.timeanddate.com/worldclock/converter.html?iso=20221128T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Amy, Yves, Rossen,
Regrets: Lea

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

Dan: concern to do with underspecified behaviour of elements with children.. There were updates in November.. pinging again

#### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov

Dan: can this be closed? They've pointed us to a new review, #767

Peter: looking at the difference between the two... is 767 looking at only a specific part of this spec? They have a separate explainer.

Dan: last feedback from Rossen about specific issues. New review request was in response - attempts to address concerns. Either this is a replacement, or ..

Peter: we had closed it in 2021 and they reopened it to ask us to look at multi screen part. 602 changed.. I believe we can close 602 now and move on with 767

#### [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

Dan: shipping, early, no signals from other engines

Amy: A couple of still-open moz standards positions [636](https://github.com/mozilla/standards-positions/issues/636) and [542](https://github.com/mozilla/standards-positions/issues/542)... not closed, lots of back and forth about security issues, not looking great on surface-level analysis.

Dan: "There is no obvious way for a web application to detect support for the proposed feature." Doesn't sound great.

Rossen: what does it mean for the primary contact to be the incubation group?

Amy: Also looks like there was a [conversation at TPAC](https://www.w3.org/2022/09/16-webscreens-minutes.html)... 

Rossen: One thing: how would I map parts of the elements' subtree - hello world e.g. centered inisde of the element. How would a screen reader get the relative coordinates of that element in respect to the screen reader? In order for the screen reader to draw its focus rectangle it would need to know where the element is. That location is usually relative to the window... since AT API allows you to keep traversing up to the screen you will know you're relative to a screen but if you're part of a document how would you know you're relative to a different screen.  I get how it works with multi-windows - but in here you have essentially one window.

<blockquote>
Hi @michaelwasserman yes probably it would have been better to request a spec review for something this far along in the process. We're concerned about the lack of multi-stakeholder support or signals thereof. We note extensive discussion on the security considerations in mozilla/standards-positions [#636](https://github.com/mozilla/standards-positions/issues/636) and [#542](https://github.com/mozilla/standards-positions/issues/542) which don't seem to have come to resolution yet. Any update on this or info on other implementers supporting / working on this?  Lack of feature detection is also concerning and goes against our [design principle](https://w3ctag.github.io/design-principles/#feature-detect) on detectability.
</blockquote>

*[posted](https://github.com/w3ctag/design-reviews/issues/767#issuecomment-1329477196)*

#### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

*bumped to next week*

#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Amy: they reopened the review for prefetch - though it's pre-rendering.  

Dan: Same comment left in the [Mozilla standards positions](https://github.com/mozilla/standards-positions/issues/613) and no response. Likewise discussion about prefetch.

Yves: adding a new http header is not an issue in itself. All the things people need to configure is becoming a bit much. Would be good to either reuse something existing by adding a new value. Even that adds to complexity. Or finding a way to .. define profiles that will select a set of behaviours or something like that. Still need to have a more comprehensive description of all the knobs used for security wrt all the http headers. We miss a comprehensive picture of all the http headers and their interactions, not only for this proposal, many recent proposals

<blockquote>
We're noting a lack of multi-stakeholder interest in this. Do you have any info on this can you can share? We're concerned about developer complexity when it comes to this feature, especially considering the need for a new HTTP header that requires server configuration. Is there an alternative design that wouldn't require as much complexity? Never the less, regarding the design it's good to see it's an opt in. 
</blockquote>

*[leaves comment](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1329510775)*

#### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

#### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

#### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Peter: we opened up the issue in Houdini about sync/async as a bigger deal... 

Dan: shall we put this on hold?

Rossen: it's not necessarily CSS only related.. We could spend some time on CSS call this week, some of the right people could be there.

*bump to plenary for maybe an update from CSS*

#### [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

#### [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

#### [Design and specification review of CSS Container Queries Style Features](https://github.com/w3ctag/design-reviews/issues/787) - @LeaVerou

### Breakout C (APAC / Europe) - [2022-11-29](https://www.timeanddate.com/worldclock/converter.html?iso=20221129T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Amy, Max
Regrets: 

#### [MiniApp wg discussions](https://github.com/w3ctag/design-reviews/issues/762#issuecomment-1328793218)

Dan: they want to have a discussion with us about our feedback. [Their issue](/64)

[scheduling - 30 mins 2nd half in Breakout C Dec 13th - Yves asking if it suits]

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Dan: [their feedback](https://github.com/w3ctag/design-reviews/issues/760#issuecomment-1318834700)

Max: In the last sentence - they said they'll come back and provide more info based on the trial. 

Dan: should we wait for their response?

Max: they suggested that the trial will give a better understanding. Probably we can wait for more information, then discuss with more information.

#### [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon

... still waiting

#### [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion

Dan: no new information. Will ask Sangwhan.

#### [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon

Dan: mixed messages..

Yves: it's right that malformed url or wrongly decoded url will be rejected, but this is not the proper way to do processing and escaping. It's relying on the fact there won't be bugs in parsing of things that have an escape char that is not an escape char. To me it's bad design. For the attacks, it's like many other things that can be attacked using local addresses. The IETF people against it need to fight. We expressed our concerns. I asked to have more discussion with the people in charge of revising the URL RFC, I think that's the proper place to discuss that. We can close with concerns and say we want to have that resolved in IETF.

Dan: I could ping mnot and ask him to weigh in on the issue, but perhaps we shouldn't do that

Yves: we can ask mark and martin if that would be a good course of action for them as well. Discuss closing at plenary.

#### [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman

Amy: they've updated the privacy & Security questionnaire but it's still not up to date with the spec (they missed a bit about PII). I'm reviewing the [moz standards position as well](https://github.com/mozilla/standards-positions/pull/682/files).  Maybe we should close with satisfied?

Dan: Leave the comment  and we can discuss it at the plenary and hopefully close based on their feedback. *sets to proposed closed*

#### [Content-type in Resource Timing](https://github.com/w3ctag/design-reviews/issues/785) - @maxpassion

Max: seems not very complex - proposed extension to draft of performance resource timing. This is used by developers to measure web page performane. They propose to add content type info used by developer for analysis... if content type is image or other media .. user experience is different. That's the purpose.. Personally don't have other comments. Straightforward.   

Dan: I think I understand the user benefit

Yves: a developer benefit. Figure out if you are using conneg for two different types of images, if you are talking to the server or cdn, if the cdn is doing conneg or not, gives you the smallest version or not. That's what you get adding the proper content type sent by the server, not the decoded information

Max: ask them to add information from the user experience perspective? I understand its aimed to be used by the developer for analysis

Dan: might have a second order effect on user experience because it will lead to more fasterer webpages. Is there something else we are missing in terms of.. information that could be leaking through this side channel that could be revealing something about the user?

Yves: I can't see anything that is not exposed otherwise.

Max: [will leave comment and close]

#### VISS - 768

Amy: need help on this one.

Yves: I will talk to the team contact.

### Plenary Session - [2022-12-01](https://www.timeanddate.com/worldclock/converter.html?iso=20221201T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Max, Peter, Dan, Amy, Yves, Hadley, Sangwhan
Regrets: 

#### [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780) - @hober, @torgo, @hadleybeeman, @plinss

Dan: is this replacing 3rd party cookies?

Hadley: use ase to avoid fraud, but not cookies in the traiditional case

Peter: original design used zero trust cryptography. Client would go to the token issuer and send a nonce and the issuer would sign that, untwist it and get the signature. The signature can be verified but nobody knows what was actually signed. The signing site couldn't correlate the eventual bearer of the token with the person that got the token issued unless they used a unique key to sign that one token, and there were mitigations against having too many keys. They could use a small handful of keys to categorise users, but we're talking 3 to 5 keys over thousands of users. That was the original design. Looking for a change section.

Dan: [early review](https://github.com/w3ctag/design-reviews/issues/414)

Hadley: some sense of how this has changed would be useful

Peter: +1

Dan: [leaves comment]

[Discussion about related IETF work]

#### [WebXR Device API XRSession::enabledFeatures attribute (CR Delta)](https://github.com/w3ctag/design-reviews/issues/782) - @torgo, @maxpassion, @atanassov

Dan: claiming they don't need a new explainer because its an elaboration on an existing thing. They pointed us to the overall webxr explainer and a section of the spec

Peter: seems minor

Dan: there's multi stakeholder support (Google, Apple, Microsoft are primary contacts). Shall we close it?

Peter: +1. I don't see any privacy issues. Can't think of any harm from this. Seems reasonable. They have a note about dynamic viewport scaling

Dan: that was resolution satisfied

Dan: [leaves comment and sparkles]

#### [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo

Dan: there was a response... should we wait for Tess?

#### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro

Amy: Sync and async discussion... in the thread...

Sangwhan: I can comment on this as well... In the [web NN api](https://github.com/w3ctag/design-reviews/issues/771#issuecomment-1332346304)... ...Interesting work-around... sync APIs only available on workers... to mitigate the damage. We could incorporate that guidance into the design principles...? In the context of NN API that's fine..   The sync suffix guidelines maybe applies here as well.  We do have to have a deprecation path for these things as well.  Going to be difficult to remove later on.

Peter: it's not horrible to have sync stuff that's only on workers... possible to feature-detect on the main thread though?

Sangwhan: this would be implementation-specific... On Firefox and Chrome it's possible... We could solicit some feedback - worker-only enforceable?  

Amy: question from littleDan in this thread... wondering how we should handle cases going forward... 

Sangwhan: he was suggeting we could leave room for WASM promise integration... but that's not shipping yet.  So we should wait for that until we make it a principle.  Can loop him in [to the design principles issues](https://github.com/w3ctag/design-principles/issues/402).

Peter: one concern: are we going down the path of adding a full posix layer to browsers?

Sangwhan: probably yes... 

Peter: might be worth taking a step back and asking the question - is there a line that we need to draw?

Sangwhan: the posix model doesn't fit with the main web... the threading model doesn't quite work... `main()` loop paradigm not compatible with the web...   This happens because we want to re-use code on the web, but a lot of it isn't compatible.  

Peter: it leads down the path that browsers ship a complete copy of linux... 

Sangwhan: there are companies that want to do this.

[Agreed that we should get into this issue, separately.]

Dan: we continue to bang on about developer compexity... this falls into that catetory. What are we trying to do here?

Hadley: What do we need to do on this?

Sangwhan: I'll dig up ongoing relevant work and we can carve out a separate discussion for that, as an architectural thing.

Also a design principle needs to be drafted and reviewed.

#### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

Amy: seems like a small thing... seems reasonable.  Related but differrent to the previous one.  Not much in the way of multi-stakeholder.  

Peter: I'm concerned - in the explainer - what happens if you get a file handle from **open file** and decide to delete ... 

Sangwhan: shouldn't that **throw**?

Peter: the explainer is a PR...   Not exactly the best way to review.

Amy: the Security & Privacy doc just goes to the general S&P doc for the overall spec - not specific to this change.

Dan: should we force them to do some work?

Peter: I kind of think so.  It does reject unless you have read-write permission.  

Sangwhan: we should ask the question.

Peter: allows recursive directory removal...  could be dangerous. Let the user pick a random system or home dir and recursively delete everything in one call

Sangwhan: yeah i guess if the user does something ..  I think the root dir is disallowed... There's a platform-specific list of things you can't do... 

Peter: a lot of damage you can do below root

Sangwhan: list of things you can't do are very platform-specific

Amy: [will draft comment]

```
Thanks for your review request. On the surface, the developer need you have laid out seems reasonable. Could you articulate this in terms of the impact on the end user, in a small standalone explainer please? Also it would be helpful if you can respond to the security & privacy questionnaire in a way specific to this addition to the spec. We would like clarity on cases where the file handle is obtained from an open file (as opposed to from `showSaveFilePicker()`), as well as mitigations against the risks of recursive directory removal using this method.
```

#### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

*bumped*

#### First Party Sets

Sangwhan: they have made some signifigant changes to FPS -- feel they've addressed moth of the issues we raised.  They'd like us to take a second look at the spec.  

Sangwhan: they got rid of one thing we had issue with...  Should they re-open the existing review?

Amy: didn't we decide that this was unfixable?  We spent a lot of time on it.

Dan: i suggest we ask them to provide us with a set of changes, update our issue on here's what we've done and how it addresses your issues?

Sangwhan: do we want a new review or a comment on the exisitng review?

Dan: I think existing review. And we can look at it asych, and decide how we want to approach it. Also, I don't want this to get in the way of other stuff.  


#### New repo for bfcache doc

Sangwhan: we should do a breakout and land principle... 

Dan: will assign to breakout C next week.

#### Breakout Rollup

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
