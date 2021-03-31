## TAG Teleconference
##### 29-31 March 2021

---

### Agenda:


#### Breakout A (Europe / US) - [2021-03-29](https://www.timeanddate.com/worldclock/converter.html?iso=20210329T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss
* [Web Authentication Level 2](https://github.com/w3ctag/design-reviews/issues/577) - @hober, @rhiaro, @hadleybeeman
* [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov
* [Early Design Review: Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611) - @hober, @rhiaro, @atanassov
* [ModuleServiceWorker](https://github.com/w3ctag/design-reviews/issues/617) - @kenchris, @plinss
* [Early design review: Sanitizer API](https://github.com/w3ctag/design-reviews/issues/619) - @LeaVerou, @rhiaro
* [WebXR Plane Detection Module](https://github.com/w3ctag/design-reviews/issues/620) - @torgo, @atanassov

#### Breakout B (US / APAC) - [2021-03-30](https://www.timeanddate.com/worldclock/converter.html?iso=20210330T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @plinss
* [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia
* [CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @LeaVerou
* [ARIA in HTML review](https://github.com/w3ctag/design-reviews/issues/614) - @hober, @atanassov
* [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris

#### Breakout C (APAC / Europe) - [2021-03-30](https://www.timeanddate.com/worldclock/converter.html?iso=20210330T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @kenchris, @hadleybeeman
* [Early design review: opaque-blocklisted-never-sniffed MIME types](https://github.com/w3ctag/design-reviews/issues/618) - @torgo, @ylafon
* [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris

#### Plenary Session - [2021-03-31](https://www.timeanddate.com/worldclock/converter.html?iso=20210331T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Dan, Rossen, Amy, Peter, Hadley, Lea

Regrets: Ken

##### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

Dan: there has been some back and forth between krgovind and John from Apple. Maybe we should schedule a breakout breakout between Hadley, Amy and me? The point Hadley made about wanting to have a more full response to FPS if we want to be impactful. 

[extra breakout scheduled for tomorrow]

##### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

[bumped to b]


##### [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss

Peter: we pinged folks about IETF coordination

Dan: haven't heard anything back. I will ping Martin Thompson.

##### [Web Authentication Level 2](https://github.com/w3ctag/design-reviews/issues/577) - @hober, @rhiaro, @hadleybeeman

Hadley: I would like to have a proper look at it. 

Dan: I suggest we look at it right now

Dan: In the security & privacy responses they've said there us no special behavior in incognito modes... Should there be? If the user is using an Apple Attestation it will leak that they have an Apple device.  Other than that the responses to the privacy & security self check look good - however I'm unfomfortable with the apple-specific fingerprinting issue.

Hadley: looking at the explainer - talking about features that are changing but doesn't talk about use cases and user needs... The desfription of attestation doesn't say "why"... 

Dan: written from a perspective of people who understand the space of authentication.

Hadley: webauth level 2 - adds discoverability of credentials for the relying party web site to examine - and I'm struggling to understand why that's a good thing. When the user wouldn't want them to be discoverable... They haven't explained what they're setting out to accomplish. Looking for use cases... large blob is for ssh authentication.. credblob is for non-web context.. what's in mind for that?

Dan: in level 1 there are use cases. None in the explainer for level 2? It talks about machine auth in a non-web context..

Hadley: Right, what does that mean? There are use cases in [the spec](https://www.w3.org/TR/webauthn-2/).

Dan: same use cases as in level 1. A question about what additional use cases are being enabled if thare are no new ones in the spec and none in the explainer.

Hadley: Mike also asked for use cases

Dan: we can ping Adam and say we agree use cases are lacking and link to that comment

[from blink thread](https://groups.google.com/a/chromium.org/g/blink-dev/c/Vfg2o0peyYg/m/Vp0h8i5VBQAJ)

> The situation is that a credential is getting created on a security key via the web, but it'll later be used in a non-web context. In Microsoft's case the credBlob value will be the SHA-256 hash of some Active Directory stuff. When the user is signing into a new laptop then this that serves to convince the new laptop that the information that it's getting over the network isn't lies. It trusts that the legitimate owner inserted their security key, but it doesn't know that the network is friendly.
>
> That is not a precise description, and I might have misunderstood some details! The reason that I think the details are unimportant is that there's already a binary blob that a website sets on a new credential and which is returned when the credential is used: the user handle. So this information could be hacked in there, but Microsoft are doing it more cleanly. The only reason that this involves an IDL change at all is because of the way that authenticator extensions happened to be implemented in Blink.

Peter: that is specific to the credblob

Rossen: this is an important use case

Hadley: the next question is Yoav saying who wants to ship this, the answer is Microsoft at the moment. The rest is addressing edge cases needs. If this is to do with desktop auth why does it need to go through the web?

Peter: the enrolment happens on the web. They're wanting to reuse webauthn for other purposes. Log into your corporate laptop with the same thing as you log into corporate websites. There are other use cases like sharing SSH keys, probably part of the original intent. I'm concerned about the Apple extension being a vendor specific.. assigned to a generic web platform API seems odd to me. 

Hadley: not normally how we do things. Also one for Android. There's a design principle about not doing things specific to one vendor. There's an [ethical web principle about multi device](https://w3ctag.github.io/ethical-web-principles/#multi)

Peter: we have a principle about [native apis not translating well to the web](https://w3ctag.github.io/design-principles/#wrapper-apis)

Dan: [noodling on some comment text]

`Hi @mikewest @agl. Sorry this dropped off of our radar. We are spending some time looking at it today. We're noting a lack of use cases. It looks to me like the use cases in the level 2 spec are the same ones as in the level 1 spec - so this raises the question: what additional use cases (user needs) are being solved with level 2? Our take on explainers is that they should generally start with the user needs. I have no doubt that there are important new user needs that y'all are trying to solve with level 2- but it's not clear from the explainer what those are.  Even if the answer is : "this spec adds some commonly used authentication mechanisms to webauth."

Regarding the security & privacy self-check, the responses look good. I'm concerned about the fingerprinting implications of the apple-specific attestation format. There doesn't seem to be any discussion on mitigation against that. Also, there are no plans to have different behaviour in incognito mode. Is that a good thing, especially considering the additional fingerprinting surface area? Do you have additonal information about why device-vendor-specific mechanisms are required?  It's unusual for device vendor specific technologies in the web platform - see [Web Platform Design Principles](https://w3ctag.github.io/design-principles/#wrapper-apis) and [Ethical Web Principles](https://w3ctag.github.io/ethical-web-principles/#multi).

One side note: the explainer and response to the security & privacy questionnaire are both in google doc format and we'd really like to encourage these to be in markdown along side of the spec itself...

We're aware we took too long on this review and we're not seeking to block anything, however the we think the quality of the explainer and spec will be greatly improved by addressing the above issues.`

Dan: posted. See if we get responses by wednesday?

##### [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

Rossen: discussion was moved into first party sets right?

##### [Early Design Review: Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611) - @hober, @rhiaro, @atanassov

Amy: some replies that I still need to read. [bumped to plenary]

##### [ModuleServiceWorker](https://github.com/w3ctag/design-reviews/issues/617) - @kenchris, @plinss

[skipped]

##### [Early design review: Sanitizer API](https://github.com/w3ctag/design-reviews/issues/619) - @LeaVerou, @rhiaro

Lea: I looked yesterday - so first off lots of use cases. It's work that should be happening. Sensible defaults. Even though they have a detailed dictionary - there are some things not expressed through that. For example allow lists and block lists - but what about javascript: links on `<a>` elements. Strange to take a string as an input and return a document but I can see the reasoning. .. Unclear how someone can remove a blocked element through the default list. Not clear how you can drop one element from the allow list without specifying the entire allow list again. Noticed that the config not exposed on the sanitizer instance... That could help with customizing the default config. 

Hadley: why would you want to do this?

Lea: you want users to be able to write arbitrary HTML - but this opens up xss security issues.  There is a library called dompurify which is widely used that they are basing their work on. It would be good to have something like this in the browser.

[we can come back to it in the plenary]
 
##### [WebXR Plane Detection Module](https://github.com/w3ctag/design-reviews/issues/620) - @torgo, @atanassov

[bumped]

### Breakout B

Present: Peter, Rossen, Lea, Sangwhan

Regrets: 

##### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @plinss


##### [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia


##### [CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @LeaVerou


##### [ARIA in HTML review](https://github.com/w3ctag/design-reviews/issues/614) - @hober, @atanassov


##### [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris

Discussion about color conundrum (wide gamut, color object vs string).
Consensus to add a property that returns a hex string as long as its name is explicit about what this is 
I.e. no generic `color` or `colorString`, but something as explicit as `hex`, `hexString`, `srgbString` and so on.

Side discussion on Color object, which WG to work on it (CSS WG, Houdini, or new?). Consensus that it should not be a new group, and that it can happen in either CSS or Houdini, this should not hold up the work.

We are still concerned about the event based design and think a promise-based design would be more suitable.

With a promise based design, `open()` can allow for a permissions prompt or not, based on what the UA wants to expose.
E.g. if drag and scrub is allowed, it would make sense to have a permissions prompt, but if the UI only allows selecting individual colors by clicking, it can be omitted.

Peter: security issues, sites maliciously opening eyedropper to sniff
can be used for nefarious reasons by advertisers

Lea: should only active tab be able to open the eyedropper?

Peter: user activation state? 

Rossen: this is already in their explainer

Discussion on refining color state by multiple clicks. Should the API allow multiple color selection, or should it be up to the UA to provide UI for this? Consensus around previous feedback (API designed around single returned color, UA can provide UI for refinement)


### Breakout C

Present: Ken, Dan, Amy, Sangwhan

Regrets: 

##### [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @kenchris, @hadleybeeman

Ken: they filed issues for all of the issues - they did that on a call in the wg and they haven't finished yet.  Someone from MS commented. Seems that they are listening to our feedback.  Sangwhan seemed happy with the asnwer.  This is an early review and we've given feedback - to which they have been receptive. They are listening.  

Dan: looking at PR that resolves some issues...

Ken: unless we have major concern... i think they're handling that in the WG itself. Of course there's concern about how the field of machien learning is evolving, is it going to change, but Intel is positive, Microsoft is also positive, they believe it's the right path forward. Google had some ideas of doing something smaller, but these are the discussions in the WG. It's not shipping.

Dan: We might want to close this at the plenary. We need Sangwhan.

[sangwhan joins]

Sangwhan: they haven't addressed the ergonomics of the API. It's not developer friendly. Their reasoning is that this makes it easier for them to bind it to hardware. But I'm not sure if that's..

Dan: the point of an API is to make it easier for the developer

Ken: how is that different from webgl and webgpu

Sangwhan: I'm not suggesting those are good, a nn is more of an application API rather than a hardware API. That's the bit that makes me uncomfortable. Their rationale is that this is for framework developers

Ken: that's the same with webgl

Dan: people use things like iframe and libraries

Sangwhan: that's the main concern I have. We might want to take a position on where we draw the line of these are APIs that are for framework developers and these are APIs that are supposed to be used as-is. We shouldn't have that many that are designed only for framework developers. But there's also the extensible web manifesto that suggests everything should be low level

Dan: we have more measured wording in design principles about that now.. don't we? Are we still talking about low level vs high level?

Sangwhan: it's a standing issue. I don't have strong opinions that the web should be this or that. Feels like we should draw a line on where we say this is best as a low level API and this is best as a high level API

Dan: in the issues .. they haven't addressed all of our issues

Sangwhan: other issues I raised are minor compared to this ergonomics issue. Number 8.

Dan: they think we're asking them about the ergonomics of the examples, you responded that it's the API itself.

Sangwhan: the API is [incredibly loquacious](https://github.com/webmachinelearning/webnn/issues/139#issuecomment-782808982). You have to do a lot of boilerplate. Rationale is you don't have to invent new types and can work with hardware, but it's really not nice to use. That's my main concern. It feels like C code. They haven't addressed that.

Dan: we need to be stronger then on our response. We need to say in our issue we appreciate they're being responsive to the list of issues. The main thing we're still concerned about is the developer ergonomics and pointing to that example. That might sound like we're asking them to reinvent the whole thing. We could suggest that there need to be better developer ergonomics, ways to use this API that don't require that amount of syntax

Sangwhan: I've suggested that on their issue and the response I got was it's fine because of framework developers

Dan: my suggestion is to say that's not okay. It is worth nothing that both WebGL and WebGPU are good examples of notoriously difficult to use APIs that nobody uses and developers don't like working with because they're design in this way. That ties people to dominant frameworks. Which creates a different set of problems. 

Sangwhan: even the native people gave up on WebGL and WebGPU, that's why unity and realty are a thing.

Dan: it's example of a bad practice.

Sangwhan: I don't want to block their work or have them reinvent the API. 

Dan: they should have an optional way to interact with the API that's built in and doesn't require you to use a framework on top of it. 

Sangwhan: I'm surprised that the person who wrote the example code didn't feel the API is not user friendly. I will reply on their issue that is separate. Do we have consensus that we want developer friendly APIs over hardware friendly APIs?

Dan: this is a design principles issue 117 which is still open. We need to discuss it in that context. Feels like we do have that consensus but we haven't documented it. Lea is working on a PR, there's one open ([291](https://github.com/w3ctag/design-principles/pull/291)) which among other things talks about how you shouldn't exclusively develop low level APIs, design high level in terms of building blocks over low level... ensure continunity and ease of use.. 

Sangwhan: if we have group consensus I can say yes we don't want lots of boilerplate in the APIs

Dan: I feel like we do have that consensus. We can further discuss in the plenary.

Sangwhan: one part of the API design choice I do understand because javascript doesn't have operator overloading. Makes it hard to make this kind of API. 

Ken: wasn't there some work on that?

Sangwhan: still stage 1

##### [Early design review: opaque-blocklisted-never-sniffed MIME types](https://github.com/w3ctag/design-reviews/issues/618) - @torgo, @ylafon

Yves: it's for things they don't want to sniff for security reasons. Things that are undefined like gzip or package, word files. When you're doing inclusion.

Ken: sounds like a good thing. It's basically a block list?

Yves: Don't try to process that, we know in advance that we won't be able to use it anyway

Ken: the readme is a list

Dan: Anne responded to my question about venue, which is that it's folded into fetch, so a WHATWG thing.

Ken: if we know there are issues with sniffing but it's course to allow it but it's not going to cover all mime types. This is not file extensions I guess..

Yves: I have nothing against it. The issue is more about maintenance of this. Lack of maintenance will lead to possible security issues where you are forced to inspect something that may be malicious with an improper media type. It's not a good issue because you can always add the same kind of cntent sent with a media type that is known to be sniffed, with the wrong media type. I don't think security is a big issue. Maintenance is always an issue, there is a need to have a registry for that.

Ken: if it's just in the spec itself, as long as there are wpf tests? You want to make sure if they add more mime types that browsers implementing fetch will also add those to the browsers. Doesn't need a wiki or anything, if it's in the fetch spec that's fine. Just need to make sure they're covered by tests.

Yves: I'm wondering why they have multipart byte range and multipart signed, why not multipart/ * If you're using multipart you might not be able to figure out the real media type of the resource anyway so something can be sneaked in

Ken: that's good feedback. Would be the same for the openxml format office document?

Yves: and message/something. Font or remove all the fonts from there? Fonts should be in the excluded list. 

Ken: what is application/vnd?

Yves: vendor extension

Ken: some are from open office right?

Yves: it's media type that is not html or css or images or video. May want to exclude the + extensions, +json, +zip, +xml

Dan: I'm going to write back, they [said in response](https://github.com/w3ctag/design-reviews/issues/618#issuecomment-806017154) to my question about user needs which elaborates. Going to suggest that goes in explainer. 

Yves: will put questions into an issue comment

Dan: let's see what we get as a response and see if we can iterate

##### [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris

Dan: they had a discussion in breakout B.

Sangwhan: Lea left a note to pass it on to in particular Ken to take a look at the comments. She drafted a comment in the minutes. If we are all okay she will post it. Conclusion is that we will propose them to make it so it is extensible through some sort of string based mechanism that would let you denote the colour space, that comes in when you pick a colour, so instead of #ffcc00 you'd get rgb.. was the gist.. it has to be an object instead of just a string that comes in from the event. 

Dan: is it backwards compatible

Sangwhan: I think yes, that was part of the main reqirements. If you can break back compat you don't have to care about.. you can invent a new colour object. Interop is part of the considerations.

Dan: then that feels fine.

Sangwhan: a lot of discussion about if it should be a promise.. request a colour and the user picks a colour the promise resolves vs an event based design (which it is right now). I found the event based design strange but don't have any better ideas. Lea wanted to hear what Ken thought. Minutes will be summarized into a comment.

Ken: [reading]

Sangwhan: they had a use case they wanted to solve which is why they use pointer events

Ken: I think it's fine what's in the minutes

### Plenary Session

Present: Dan, Amy, Peter, Yves, Lea

Regrets: Hadley, Sangwhan, Kenneth

##### First Party Sets

Dan: we had a breakout yesterday. It needs a lot of tag time and energy. The proposal is to say we consider this harmful. We very rarely do that. It needs to be carefully done. This is a high profile proposal, and in the privacyCG. This changes the definition of what it means to be the first party. It's clear from the feedback from the requester that they are trying to work around origin. I referenced a draft from 2011 that talked about the origin of origin that was interesting for historical purposes (but not a finding, can we reference it?). I don't care about the mechanisms origins can self-declare because they are only allowed by browser allow lists. The whole dance of origins being able to self define their own FPS is window dressing. What we're talkinga bout here is the browser shipping with allowlists of fps which they consider to be valid. And no mechanism for how those would be applied for, vetted, how it would work across browsers. This whole thing about vagueness of scope. The proposal name indicates its everythign where we talk about parties, in fact it's really only about cookies - maybe - but the explainer talks about iframes and embedded content databases. We put about explicit restriction of scope, eg. to cookies. Context of privacy sandbox. Web privacy isn't just a marketing initiative. Restricting third party cookies is great but at the same time changes the definition of what first and third party cookies are via FPS then the entire privacy sandbox initiative feels like gaslighting.

Yves: also the browser defining the allowlist puts them in too strong position, they can block people from being in the list.

Dan: I make that point later on. Governance. In the Is this Harmful to the Web section - market power of dominant user agent. I try to say yeah .. Amy put in "yes". To qualify that statement a bit and say the reasons and "in it's current form" so there's an out.. the problems trying to be solved can be solved in other ways. And a note on dependencies on FPS because of the other proposal. We're not going to review things that are related to FPS unless there's consensus .. can't build on shaky ground, not good architecture. 

Lea: the thing with browsers having allowlists seems wrong enough to have a principle against it, but not sure what the principle should be. We can distill something from it.. probably ethical.

Yves: they already have blocklists for SSL CAs and things like that. It's not the first one.

Peter: a blocklist against a known bad actor is one thing vs an allowlist is a very different scenario

Yves: true

Dan: I shared this with mnot and he was supportive. If we can get TAG consensus I'd like to release it as a.. maybe on github in a similar way to feedback for miniapps. We could post it as a blog post, like feedback on EME. Or a full blown finding. Not really a finding. 

Peter: I agree finding is the wrong tool

Yves: same as for miniapp would be good

Dan: don't want to turn it into a grand stand type thing.. blog is too much

Peter: blog post feels like trying it in the court of public opinion. Make it direct feedback to a review request.

Yves: having a standalone document that we can refer to is better in a github comment. 

Peter: if we give a disatisfied response to the review and they proceed anyway then we can take it to a blog post..

Dan: maybe aim for next week to publish, after breakout A. We all continue to work on it.

##### [High Level vs Low Level](https://github.com/w3ctag/design-principles/pull/291/files)

##### Detectability of AT - Sangwhan

##### Breakout Rollup

###### Eyedropper

[reviewing notes from Breakout B and C]

Peter: so we should draft some feedback...

Lea: I cam do it - will leave comment.

Peter: on promises vs events - i have mixed feelings - maybe we should say "it can be done either way and depends on what the primary use case is". Not sure if the use case demonstrates a need for an event-based system. If they start with a promise-based system they can still add an event-based system later.

... if you construct an eyedropper you can get the promise from you can make that an event target.

Lea: makes sense and might be convincing.

###### Opaque blocklisted never-sniffed mime types

Dan: I wrote feedback

Yves: I wrote a response as well

###### Web NN API

Dan: responsive to our feedback, but key point is that API ergonomics are for framework devs and it shouldn't be that difficult to use. Brought up low level vs high level which is an open issue in design principles that we have a PR on. Should we have specific wording about writing APIs for framework devs being an antipattern

Lea: we'd need to define what that means. What should people avoid?

Dan: in this case Sangwhan pointed out there was a huge amount of syntax required to do every operation. Developer unfriendliness. Other ones are WebGL, WebRTC also.. people dont' use WebGL they use 3.js. Same with peer.js and WebRTC. Sangwhan didn't want to close it until we work more on this issue about developer friendliness of syntax.

Lea: issue is not developing APIs for framework devs but developing APIs that are so low level they can't be used by anyone without a ton of knowledge about the domain

Dan: true

Lea: maybe we need a principle of the sort of "simple things should be easy". Or high level vs low level.. seems like it might cover it. 

Dan: could be we need additional wording in high vs low level

Lea: so APIs should not just be low level?

Dan: we need consensus.. its' about complexity rather than level. You need a lot of experience in the domain area to use WebGL. You don't need to understand graphics as much if you use three.js because it abstracts complexity away. Then you're tied to a library. It's getting the balance right between high and low level and not being a zealot about the extensible web manifesto meaning everything must be primitive. That's the balance in the current text in the PR..

Lea: I think a good API isn't one point in the continuum of low level and high level, it progressively reveals more abilities as you need them. Can start very hgih level, sensible defaults, simple things are easy, and progressively you can customise what it does for complex use cases. That is the ideal. Simple things are easy and complex things are possible. 

Dan: I like that wording. Maybe we do need a simple things should be easy principle.

Lea: good for UIs and APIs in general as a mantra

Dan: let's talk about it next week.

##### Issue Triage
