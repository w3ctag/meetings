# TAG Call Minutes - Week-of 22-April-2024

## Agendas

### Breakout A (Europe / China) - [2024-04-22](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk
* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @ylafon, @maxpassion
* [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* charter: [Sustainable Web](https://w3c.github.io/sustyweb/wg/charter.html)
* https://github.com/w3c/strategy/issues/450

### Breakout B (California / Europe)  - [2024-04-22](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk


### Breakout C (California / Australia) - [2024-04-22](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hober, @hadleybeeman
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### Breakout D (California / Australia) - [2024-04-23](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @torgo
* [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo
* [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou

### Breakout E (Europe / China) - [2024-04-24](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

## Minutes

### Breakout A (Europe / China) 

Present: Dan, Matthew, Yves
Regrets: Hadley

#### [Design Principles PR](https://github.com/w3ctag/design-principles/pull/492)

Yves: quick fix to fix a link...

*We merge...*

#### [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk

Matthew: no movement on the thread...  but in the WHATWG thread it's still open - one of APA's members commented on this.  There are some people in that thread who are in a position to make a change if it's needed.  It looks like we're still in an area where we could positively impact the consistency issue... So I'll bump the WHATWG thread... When I bump, I will let Lea know.  The one thing we've (TAG) asked for - to show the picker (but it's whether it gets focussed or not) - we need to make call of what the use case is... Is common use case one where it gets focus, or not? [what is the default].

#### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @ylafon, @maxpassion

Yves: this seems to be a huge chunk of work - espeiclaly aropund privacy .. didn't make that much progress yet.  We need privacy / security attention.,

Dan: should we get Anssi on a call?

Yves: yes but Amy should be ...

Matthew: and Martin...

Matthew: Well written explainer...

Yves: agree...

Matthew: local collaborative document editing... 

Max: I think it's already ... available in the OS... they just propose to add a new feature for web...

Yves: it relies on existing things... mdns... they have a toggle to make it discoverable or not as a way to secure that... not wide open.  In the browser API... it would be on the page.

Dan: ...security & privacy .. vector for malware ...

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/932#issuecomment-2068920810) suggesting first week of may for an interactive session with them.

Matthew: we should have questions written down and circulated beforehand.

#### [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion

Dan: *pings Sangwhan to get his feedback as he has domain knowledge*

#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

<blockquote>
Hi @steimelchrome can you feed back on any updates to this proposal?  Matthew [asked a question](https://github.com/w3ctag/design-reviews/issues/798#issuecomment-2004432739) above regarding Lea's feedback that looks like it's still pending. Thanks!
</blockquote>

Dan: *posts comment*

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Dan: *posts [comment](https://github.com/w3ctag/design-reviews/issues/760#issuecomment-2068941251) asking for an update*

#### charter: [Sustainable Web](https://w3c.github.io/sustyweb/wg/charter.html)

*we discuss*

Matthew: in terms of accessibility, APA didn't have concerns.. however Martin had some concerns... 

Matthew: it's in the spirit of the design principles, ethical web principles... cites us.  The concerns are that there a lot of these and ... although we're not feeding back on the document, but the charter... In terms of chartered work the scope is clearly defined...

Yves: the feedback is about the size of the document and it could lead to paralysis... 

Dan: the CG report is a collection of ideas...  

Matthew: some of the recommendations seem quite techincal and others not so much... Needs to be re-organized into "actionable technical things" vs. aspirational...  It needs to adopt the WCAG hierarchy of concreteness...  They've annotated if things are machine testable or human testable...  It's appropriate to see where it goes. I don't see anything that warrants us saying "no". I think we should be keeping an eye on how it develops...

Dan: and I think it's mostly about building web sites...

Matthew: there may be elements that are guidelines for implementers...

Dan: that should be sign posted....

Yves: Ian wanted to have a reply as soon as possible...

Dan: can you point Ian to our minuted discussion and let him know Martin may have additional feedback.

Matthew: i wonder if serialization formats is in our pervue...  JSON is inefficient .. but it's human readable and easy to edit.. Both are important things...  Ther's a balance to be struck.

#### [Federated identity wg charter](https://github.com/w3c/strategy/issues/450)

Yves: this is a [charter review](https://w3c.github.io/charter-drafts/2024/wg-fedid.html) as well... 

Yves: it would be good to have someone well versed in fediverse ...

Dan: shouldn't this belong in a different place?

Matthew: it's not very decentralised is it?  There's a digital credentials community group... 

*some discussions on the risk of digital credentials API*

Matthew: also agree there's an opportunity for the UA to protect the user... UA doesn't want to be seen as giving advice... 

Dan: worried about this work holding up the rest of the work so maybe it should be in a separate group?



### Breakout B (California / Europe)  - [2024-04-22](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Yves, Lea

#### [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

<blockquote>
  
Hi @diekus, after reading your comment both @plinss were still confused about several aspects of this API:

Wrt `related_applications`:
- We don’t understand what the use cases are. Say, I have a website with a manifest file. _Why_ would that website prefer to be installed from another repository instead of using itself as the source of truth? What are the use cases? Is it monetization? Analytics? Something else?
- Orthogonal to the use cases, it seems like it would require the Cross-Origin version of the API to work? How is `related_applications` useful if it's restricted to the same origin?

Wrt installing multiple PWAs from the same origin and `related_applications` / `prefer_related_appliations`:

When separating the API into a same-origin and a cross-origin version, it’s important that the separation is "clean", i.e. that the same origin version can be implemented independently and no parts of it should require the cross-origin version of the API. With that in mind:
- It is unclear to us what same origin use cases the parameters of the `navigator.install()` function serve, since it seems they are primarily geared around verification, which is not really needed in the same origin case. 
- Same for the arbitrary `referral-info` parameter: what is the use case for it in a same-origin context?
- Same for `related_applications` / `prefer_related_appliations`: it seems that for these to function they require the cross-origin version of the API?

Also, given the text in the explainer, it is still unclear to use what the author flow is for e.g. having a website that includes multiple apps (`website.com/foo`, `website.com/bar`, etc.). A code example would help! 

We also don’t quite understand the signature of `navigator.install()`: it seems that `manifest_id` is optional but it is possible to provide `manifest_id` without `install_url`. What is the use case of that in a same-origin context? It also seems like in the case of a single website containing multiple apps, one would probably want to provide an install_url, and it seems like it's the manifest id that should be optional?

Also please note that TAG principle around [preferring a dictionary for optional arguments](https://www.w3.org/TR/design-principles/#prefer-dictionaries).
  
</blockquote>

#### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

#### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

#### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk




### Breakout C (California / Australia) - [2024-04-22](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Tess, 


#### [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo

Tess to write comment.

#### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk

Still pending feedback.

#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

Still pending feedback, pinged.

#### [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hober, 
@hadleybeeman

#### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou

#### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss



### Breakout D (California / Australia) - [2024-04-23](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Tess, Lea

#### [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @torgo

Tess to ping Dan about this async.

#### [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo

Closed as satisfied.

#### [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss

Review on pause until Amy gets back.

#### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

Review on pause until Amy gets back.

#### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

Review on pause until Amy gets back.

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou

Lea posted in #tag-all to see if one of our illustrious former colleagues has the right background to review this.



### Breakout E (Europe / China) - [2024-04-24](https://www.timeanddate.com/worldclock/converter.html?iso=20240422T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Matthew, Dan, Yves
Regrets: Amy, Hadley, Max

#### Discussion of federated ID & credentials 

*lots going on*

Yves: IETF [Secure Patterms for Internet Credentials](https://datatracker.ietf.org/group/spice/about/) forming

Matthew: some people think of the browser as part of the "threat"

Dan: some discussion of a new task force... and also on whether this belongs in the fedID working group...

Dan: also we have discussed the idea of a finding.

Matthew: …a number of things discussed last week … leading to a more decentralized future … we accept it's going to be messy but we give people the tools to build up a "web of trust" … people are good at socially regulating … if we concentrate on the lower levels of the stack that people can agree on then it will socially regulate its way out …

Dan: we need to do this in terms of specific capabilities

Matthew: UA should be what it says on the tin - an agent acting on behalf of the user - and user has choice of which UA they use.

Yves: laying out all the different use cases - such as disposable identities - adult verification - all those use cases that are usually not take into account.

Matthew: APA's research questions task force has a wiki page that has some of those use cases on it.  E.g. "I'm eligible to park in this parking space" without having to give away a bunch of personal information. You get a token once and then use the token.  https://www.w3.org/WAI/APA/task-forces/research-questions/wiki/Some_use_cases_for_verifiable_credentials

**we need to have some more focussed sessions on this topic**

#### Discussion on IRC & Accessibility 

Matthew: collaborative tools accessibility : https://w3c.github.io/ctaur/ much higher level than WCAG type. Overview of AURs: https://www.w3.org/WAI/research/user-requirements/

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

*bumped*

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: just noting the [feedback from Lu Huang](https://github.com/w3ctag/design-reviews/issues/875#issuecomment-2059867338) - they are going to do an update on the explainer... lookling at cors, looking at URL patterns...

Matthew: interesting difference in opinion of the spec between this group and what Apple /webkit has done.

Dan: the use case itself is clearly cross platform... 

Dan: I think at this point we're waiting for an update to the explainer... 

Matthew: one other thing I noticed - i don't think they have an "alternatives considered". so they maybe should add one.

<blockquote>
Thanks @LuHuangMSFT - let us know when you have updated the explainer and we'll re-review. Much appreciated. I'd like to encourage you to include more info on abuse cases - and mitigations against these. Can you also tighten up the scope to the problem you're trying to solve and explicitly exclude things like permissions, local storage sharing, etc... Can you also please add an "alternatives considered" section of the explainer with some of the alternatives that we discussed in the call?
</blockquote>

**sent**

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Dan: reached out to Martin async.

Matthew: a lot of articulated reasons... 

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

*bumped*
