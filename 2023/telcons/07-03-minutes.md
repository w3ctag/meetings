## Agenda

### Breakout A (Europe / US) - [2023-07-03](https://www.timeanddate.com/worldclock/converter.html?iso=20230703T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov

### Breakout C (APAC / Europe) - [2023-07-04](https://www.timeanddate.com/worldclock/converter.html?iso=20230704T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman
* [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman
* [VC-JWT](https://github.com/w3ctag/design-reviews/issues/857) - @rhiaro, @hadleybeeman
* [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-07-05](https://www.timeanddate.com/worldclock/converter.html?iso=20230705T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo
* [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss
* [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss
* [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo
* [RDF Canonicalization](https://github.com/w3ctag/design-reviews/issues/855) - @rhiaro, @hadleybeeman
* [API for capturing all screens](https://github.com/w3ctag/design-reviews/issues/856) - @torgo, @rhiaro, @hadleybeeman
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2023-07-03](https://www.timeanddate.com/worldclock/converter.html?iso=20230703T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tess, Amy, Yves, Peter, Rossen, Lea, Hadley
Regrets:

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman

Dan: No updates since last time we looked at this.

#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

Dan: We left many 2 major comments last week and have received no responses yet.

#### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

Dan: Big [response](https://github.com/w3ctag/design-reviews/issues/747#issuecomment-1555083090) to our comments...

Dan: noting no multi-stakeholder buy in.

Amy: noting [negative mozilla standards position](https://github.com/mozilla/standards-positions/issues/646). 

Dan: leaves comment asking about multistaheolder.

#### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia

Peter: we questioned the utility, they responsed with this already shipped in all major browsers. 

Peter: not sure it's actively harmful.  It's a foot gun but... there are async alternatives... 

Dan: close as **overtaken**?

Amy: "satisfied with concerns" and keep an eye for deprecation in the future?

Peter: this is part of the whole "do we want to add an entire posix layer to the web platform"... 

**we agree to close it with *overtaken* **

Rossen: why not "unsatisfied"

Peter: not harmful. They asked for tag review then it shipped.

#### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

Peter: we haven't looked at this yet

Tess: at a glance this seems reasonable. One of the complaints from e.g. banks with bf cache - I'm on a page, i log out, a hit the back button, i can still see my balance. Off hand this seems reasonable. 

Yves: i looked at it and had the same feeling that it was OK.

Rossen: when they say it's an "early review" - do we know if there's experimentation happening?  

Dan: question on multi-stakeholder - so far no info.

Dan: *leaves comment*

Rossen: in considered alterantives they've listed a header... choice to use js api is "arbitrary" ... appreciate transparency but curious... open to both... 

Yves: there's a difference between not storing in a bfcache and not storing... I think that going to header only might be more difficult.

Dan: it's possible to use bfcache without javascript so...  normally we would encourgae a non-js-centric solution...

Rossen: it seems like this is really "early"... 

Dan: cache-control: no-store would be inapproproate because...

Yves: it's a different kind of cache and there is a use case for purging the bfcache only at logout while keeping it active during the navigation. Using headers at logout would be possible but it raise the issue of invalidating pages that are not related to the requested URI and possibly not considered anymore as part of the navigation.

#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

Peter: no response to our latest comment

Tess: I'll draft a comment [raising this issue](https://github.com/WebKit/standards-positions/issues/41#issuecomment-1492378094) re: device independence.

Tess: on IOS the picture-in-picture API has media controls and you have to feed it media content.. so you woulnd't be able to interact with controls... etc...

Rossen: is the pip supposed to be interactive?

Tess: i think that's the point. One use case is you want your own media controls that you've implemented in js, and you think the ux is jarring of switching between your media controls and the systems controls when the video goes into pip, so you want a document fragemnt for the video and controls to go into pip. Or you want to control the media loading and selection so mid stream you can do ad insertion. Or there's some region of the page that you want to be pip'd like a notetaking screen that isnt' video at all, so you can have that persist on the screen and you can type notes into it quickly. At the end of the day I don't see yhow you could do this api on ios

Rossen: most of the lower level platforms support pip in a media streaming only way. when I hear picture in picture my immediate understanding its a picture. Not an app in app. Which is what you're describing here. Where you have input, and everything else that comes along, with a different engine

Tess: when we asked about how you'd do this on ios the first reply we got form one of the proposers was "I'm not sure how to address this ... weren't focussed on android/ios feasability". Shouldn't we be designing web stuff that works on all major platforms?

Dan: considering majority of web usage happens on mobile devices, we need to focus on that

Rossen: their first goal is to allow a website to display an arbitrary htm lelement that is always on top of the window. It has nothing to do with picture in picture

Tess: either they want the fullscreen api.. but they don't.. because they want it to be outside of the window. or they want window.open

Lea: confused about .. I know on osx there is a flag to keep a window on top at all times, I've used this. What are the actual differences between the PIP api in osx and havin ga window that is always on top, besides presentational differences? Is it media controls? performance improvements? What would make a window that is always on top a bad candidate for PIP?

Rossen: at least in other platforms, the ux of PIP is very well expected already. The control of the window and its behaviour. It's always a small portion of the screen. If you expand it and it takes over everything. There's an expected windowing behaviour of the pip experience that is very hardcoded, and I'm assuming most operating systesm,  it's not something you can control at all. You can't say make it half of hte screen. You get the tiny window always. Will they also want to control the size of the window and its position? Basically, everything you get with window.open. So why not window.open?

Lea: but then it would not be PIP. I thought that was the whole argument.

Tess: maybe you add an always on top flag to window.open

Lea: that's what we proposed

Tess: I think that's fine

*Tess to leave comment*

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

Yves: Need to evaluate the API change made, ex: removing `src` and adding a new `FencedFrameConfig` interface, to be used by [shared storage API](https://github.com/w3ctag/design-reviews/issues/747)

Yves: they did change the API - adding a config ... we need to re-review. Noticed that Anne did some review in the webkit stds position... 

*bumped to next week*

#### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

Yves: No activity (from us) at all. Using added noise + rate limiting to reduce the privacy issue

Yves: work done in PATCG... might surface in a coming working group...

Hadley: [the mozilla position](https://github.com/mozilla/standards-positions/issues/646) on shared storage (linked) is negative.

Dan: so this has a dependency on shared storage...

#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

Amy: No activity at all. They stated a deadline of 16th June, but not what this was for. Chrome status says it's shipping (117). Positive signals from firefox.

Amy: Proposal: is this noncontroversial? Just okay it? (this is a q for Peter and Lea)

Lea: looking at it right now it looks quite well designed to me - developers need this desperately. Seems like a really well thought out API.

Rossen: concerned with the default fallback behavior. It requires authoring rather than having an esxpected behavior handled by the UA.  There are a number of choices we could take - absolute element... default static position.

Lea: that would not work for tool tips and stuff...

Rossen: what would happen to UAs that dom't implement it?

Lea: *will write comment after the call*

#### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

Back and forth between mnot and chris L about negative feedback from http folks (apparently addressed in explainer). No input from TAG yet.

Tess: there was an altenate proposal I thought was better but ... 

Amy: we need to do some work on this... 



#### [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov

Lea: First time we look at this.

- Mozilla is positive, no response from WebKit. 
- Requires *both* opt-in from both pages, AND same-origin. 
- Opt-in is HTML, for a CSS feature, which seems suboptimal. CSS proposal may be better, though not colloquial to CSS as is.
- Opt-in might be too general, aren't there use cases where you only want to opt-in more conditionally? [they said this is still fleshed out]
- +1 for Declarative API!
- A bit unclear what happens if both documents opt in, but there is no JS to customize the transition.
- A bit worried about the user experience on slow networks. Does the transition abort at some point?
- sticky transition bugs: if some JS code sets the transition params, and a different part of the code calls `event.preventDefault()`?

<blockquote>

We were happy to see cross-stakeholder support, though we'd like to see WebKit’s position as well. We also liked the secure-first design, with two-way opt-in and a same-origin restriction. Is cross-origin a non-goal because there are few use cases for it, or because you are not confident in the security of a cross-origin opt-in?
  
It seems a little inflexible to have the opt-in be HTML (as you point out); A CSS mechanism would indeed be preferable, though the proposed syntax is not idiomatic to CSS, since there is no precedent of @-rules that take values (this does not necessarily mean this is a bad idea, but when something creates a new precedent, we should spend extra effort to make sure there is no alternative design that is more [consistent](https://w3ctag.github.io/design-principles/#consistency) with the existing Web Platform without sacrificing usability.
  
Props for a declarative-first API too!
  
We had a few questions, that we didn't find the answers to in the explainer:
- What happens when both documents opt in, but there is no JS to customize the transition?
- What is the user experience on a very slow connection? We see there is an implementation-defined timeout, we do worry that clicking on a link, then nothing happening, then suddenly a transition could result in jarring user experience.
- What is the user experience if one part of the code customizes the transition parameters, and another calls `event.preventDefault()` so the navigation never actually happens? 
  
</blockquote>

Rossen: comment looks great. concern with slow connection - how does it differ?

Lea: transition need to wait... how long does it wait... what happens? From user's pov?

Rossen: *looks at spec*. In [section 7.4](https://drafts.csswg.org/css-view-transitions-1/#setup-view-transition-algorithm) - a quick algo - 4 main steps - 

Rossen: proceed with the comment - lea's point about the slow connectiom might be answered by the timeout... which cancels the transition.



### Breakout C (APAC / Europe) - [2023-07-04](https://www.timeanddate.com/worldclock/converter.html?iso=20230704T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Max, Hadley, Yves
Regrets: Sangwhan

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman 

Dan: new stuff in the explainer around motivation...... Webkit standards position still has concerns regarding convergence with Private Click Measurement.

Amy: Also IPA..

Dan: Yes...

Amy: can we look at multi-stakeholder buy in for this, IPA and PCM? 

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo 

Max: This proposal permission policy to disable upload handler... Long history of discussion... Recent [comment 3 weeeks ago](https://github.com/w3ctag/design-reviews/issues/738#issuecomment-1588909384)... They've provided a link... also said they highlighted the differences:

* unload is disabled by default but can be enabled by Permissions-Policy
* it's too dangerous/disruptive to just go straight there, so we would start with a default of enabled and gradually flip the default until 100% of pageloads have unload disabled by default

Dan: both Firefox and Safari have come back negative on it according to Chromestatus. *Asking about multi-stakeholder if it's shifted.*

#### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman 

Dan: [response from Johann](https://github.com/w3ctag/design-reviews/issues/808#issuecomment-1582413909) - on timngs...

Hadley: 2 comments .. from Johan.

*bumped to 4-september*

#### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman

Amy: They've responded to our qs. Also some conversation and changes to the spec since it was reviewed in Tokyo. We should re-review. They have some open questions, so if we have the right expertise in the TAG we can offer advice, but otherwise we should probably wait for it to settle down

Amy: How does this fit with Attribution Reporting API? (It's the same problem?)

Dan: Any neutral opinion / summary on the three proposals?

Amy: Maybe Nick Doty / Sam Weiler?

Dan: *i'll take the action to reach out to Sam Weiler & Nick Doty*

#### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo 

Dan: response [from requestor](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1613989213) 4 days ago... HTML PR "close to approval". Support "from payment providers."

Hadley: I think it's weird... that it's coming from WhatWG and google... saying that payment providers are enthusiastic about it... is it not something that the payments wg / cg should be interested in?

Dan: ask for some feedback form payment providers?

Hadley: if there is signifigant pull-through - next step would be to connect with other payment activities rather than doing it in isolation.

Dan: ask them to run this by the Web Payment CG ?

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1619722534)

#### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman 

Hadley: Restricted to (dependent on) Isolated Web Apps, which is Chrome only. No signals from Firefox or Safari.

Dan: so there is a dependency on [isolated web apps](https://github.com/w3ctag/design-reviews/issues/842).. 

Yves: and there should be coordination between them and miniapps...

Max: they need to provide more use cases from the user's perspective.

Dan: let's bump this to the plenary... 

#### [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman

*bumped*

#### [VC-JWT](https://github.com/w3ctag/design-reviews/issues/857) - @rhiaro, @hadleybeeman 

*bumped*

#### [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman 

*bumped*

### Plenary Session - [2023-07-05](https://www.timeanddate.com/worldclock/converter.html?iso=20230705T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Max, Lea, Yves, Amy, Hadley, Dan
Regrets: Dan

#### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo

Amy: this is a dependency for Borderless mode.

Hadley: borderless mode is google only, no signal of interest from other browser vendors. Doesn't make sense outside of that context

Lea: don't know enough about CSP to evaluate the API.. The use case does seem motivating. Woudl love to add more features that discourage people from moving things to electron apps. People still feel they need native apps, I wish we could reduce that need. Whether this is reducing the need in a good way, not sure if I can evaluate that.

Hadley: packaging and bundling?

Lea: do you have to install it?

Peter: seems like they're leaving that as a problem for other people. Don't see the mechanism for how you sign... can sign the web app in its entirety, not a bundle of resources, but where is the signature, how it's controlled, how it's distributed... seems to be missing from the explainer.

Max: should have some description from the user experience perspective

Lea: goal of having apps that have powerful APIs make sense... lots of use cases for these powerful APIs..  a model like this could make access to these APIs a possibility.  Right now if you want to have an editor .. you have to store files in the cloud... The model where a webapp opens files and saves is not possibile. People need to trust cloud servers with their data. Also motivates people to move away from the web platform because native apps can do this trivially. So I think it's important ... to make these types of things secure for web apps.  Maybe something like this could be that mechanism but these kinds of use cases should be taken into account.  Not 5 different installation mechanims ... 

Dan: +1

Hadley: +1

Hadley: related work part of the explainer - they've said there's other stuff going on but it's different.

Lea: it's missing comparison to related work.

Hadley: good topic for a workshop or for a task force.

Dan: how does this relate to pwes? can look at in the browser, also has manifest, and can save to home screen, may have service worker etc. This feels like another step beyond that? Rather than something orthogonal. Regular web app, PWA with these aspects, then Isolated Web App which is like a PWA but with even more restrictions.. both using web app manifest. But there's no wording in the explainer to indicate that there's any relationship to all of the prior art on PWAs. That is bothersome. Are they thinking about what's gone before?

Hadley: chrome status says it's an extension on existing work on pwas that provides other protections against server tampering... presumably take over from PWAs?

Dan: they don't use the words desktop or mobile anywhere in the explainer. They need to be explicit about the types of user experiences they're trying to enable. Is this purely about editor applications on chromeos that need access to local filesystem? Or is this about something I could potentially encounter as an end user. Like i really want a video editing application provided by vimeo that I install in the same way I would have installed a PWA but now it's got these extra characteristics that allows me to read and write files off my local file system?

Peter: what concerns me is their non-goals, which seems to exclude that

Hadley: should not be considered desriable for most web based applications... why not? why aren't we aiming for that?

Lea: user experience must be impacted in some way that means the tradeoff is only worth it for certain security-sensitive applications. But they're not describing the user experience, so we have no way to evaluate that tradeoff ourselves

Peter: I'd like to see an upgrade path from an installed pwa to an installed web app. Seems like they're not thinking that, but more like a replacement for electron, installed completely outside the web.. though uit's updated through the web (somehow).

Dan: we shouldn't be promoting the elctron model of downloading an application and installing it, but yet it's a web application. I have 5 different web runtimes on my computer right now.

Lea: since chrome status mentions it's part of a separate app installation mechanism... I guess it doesn't present an app installation mechanism, that's separate?

Peter: are we saying we think it should?

Lea: have we reviewed pwa web packaging work that they allude to?

Peter: they link to [web bundles]()..

Dan: it's not the same as bundling, pwa installation is basically a bookmark. But on android there's webapk, which bundles up that bookmark with a signature provided by the Play Store that enables it to have additional access to resources or capabilities, and operate more like a native app on android. There's no equivalent on iOS. Web bundles stuff I thought we'd just heard they're moving away from.

Peter: also assumes signed web bundles. I don't see any spec for that. Curious why they don't do something more like a lock file that package managers use. Then the bundle could be optional.

Lea: I'd like to see some use cases that do not involve end to end encryption and messaging. If all the use cases considered are the same thing, there's a higher concern that this api may be overfitting.

<blockquote>

Hi @reillyeon,
  
We looked at this today during our plenary call. First, we do agree that the use cases should be possible to address within the Web Platform itself, but do have some concerns:

1. We are unclear on how this compares to some of the related work on this topic (a lot of which is also listed in the explainer). Given that the use cases presented are all different brands of the same use case (end-to-end encryption for instant messaging) we are a bit concerned about the solution being overfitted to very specific use cases, and having to be redesigned later, as more diverse use cases emerge.
  
Given that this presents an app installation mechanism, we think it's important for it more broadly take the use cases for app installation into account (e.g. installation as a more explicit indication that certain very powerful APIs should be available, where a permissions prompt or user activation is not a sufficient signal). We don't want the Web Platform to end up with several *different* installation mechanisms.
  
2. The explainer mentions signed web bundles, but there is no reference to how signed web bundles would work. Is that in scope for this work? Is it defined somewhere else? How do developers sign these?
  
3. We are unclear on what the user experience looks like from the end-user’s point of view. You mention that this is not a desirable model for most web applications, which implies that the user experience is impacted in some way that makes the trade-off only worth it in security-sensitive applications, but there is no description of what this user experience looks like.
  
4. What’s the upgrade path from a PWA of today into an Isolated Web App? 
  
5. We are concerned about the lack of multistakeholder support. Looking at the [Chrome Status](https://chromestatus.com/feature/5146307550248960) entry, there are no signals from any other stakeholder, not even web developers. If this is going to be a thing we think it's really important to get other stakeholders involved. A W3C workshop or a TAG task force might be an appropriate mechanism to achieve multistakeholder support and to bring in existing related work.

6. We want to note that [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) has a dependency on this work. We are concerned about going ahead with that before these packaged and signed apps are consensus-based and more stable.
  
Thank you for working with us, and we look forward to your thoughts.


</blockquote>


#### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman 

#### [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss

#### [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss

#### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo

#### [RDF Canonicalization](https://github.com/w3ctag/design-reviews/issues/855) - @rhiaro, @hadleybeeman

#### [API for capturing all screens](https://github.com/w3ctag/design-reviews/issues/856) - @torgo, @rhiaro, @hadleybeeman

#### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov
* Breakout Rollup

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

