# TAG Teleconference
#### 12-14 July 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-07-12](https://www.timeanddate.com/worldclock/converter.html?iso=20210712T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

[punted to next week priot to meeting]

* [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @kenchris, @hadleybeeman, @atanassov
* [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober

### Breakout B (US / APAC) - [2021-07-13](https://www.timeanddate.com/worldclock/converter.html?iso=20210713T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* `¯\_(ツ)_/¯`

### Breakout C (APAC / Europe) - [2021-07-13](https://www.timeanddate.com/worldclock/converter.html?iso=20210713T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon
* [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov
* [Capture Handle](https://github.com/w3ctag/design-reviews/issues/645) - @rhiaro
* [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris

### Plenary Session - [2021-07-14](https://www.timeanddate.com/worldclock/converter.html?iso=20210714T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage
-----


## Breakout A

Present: Dan, Peter, Rossen, Tess, Hadley, Yves

Regrets: Lea, Ken, Amy


### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss

Dan: sending message to Chris Harrelson - will report back at plenary

### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

Dan: there is [a reply](https://github.com/w3ctag/design-reviews/issues/571#issuecomment-861188412) from the requesteor.

Tess: it's very worrisome that it's only Chrome and the play store that are are working on this or interested in it.

Dan: can we say "this shouldn't be part of the web" - but is more of a chrome thing.

Hadley: lack of other implementer interest means it's a chrome thing.

Tess: sometimes things end up being web things - maybe this will go well - if there is a lot of demand for it.  Or maybe we will get feedback from another browser that they want to implement - which could be a signal for standardization. So it feels premature to standardize.

Peter: it's always been fine for individual products to experiment - or have a proprietary feature - but when it steps on a standardized name space.. should we recommend they use a chrome specific name for the API?

Tess: would html be better off today if the canvas element were named apple-canvas? Unlike canvas, this seems like a proprietary feature for chrome to integrate with google play.

Dan: could it be similar to the [Enterprise api](https://github.com/w3ctag/design-reviews/issues/606)...  managed device web api... talks about the "Chrome API"...  Is this in WICG? [yes] Why is it even in WICG if it's totally Play and Chrome based...

Hadley: in the explainer they do analyze the samsung in-app purchase API.  But see no evidence that they have talked to Samsung [or any other third party].

> Thanks, @phlogenix. We've looked at this again in our W3C TAG breakout session.
> 
> Given that only Chrome has expressed interest in this, and Google Play Store is the only store that you're working with -- we're not sure this is a standardisation effort. It looks like a product-specific API within one company.
> 
> In that light, we are proposing to close this review, and we recommend you name this API something specific to Chrome or the Google Play Store, for example something like "Chrome Digital Goods Inventory API". Alternately, you could engage with some additional parties now and design a higher level API, covering multiple stores. 
>
> We wish you luck in incubating and trialing this API. Please do come back to us if you get interest from other parties and are looking to make this a web standard that interoperates with other browsers and stores. 

Rossen: proprietary or non-proprietary name?

Tess: canvas is a general purpose api - this isn't.  This feels like "chrome wants to expose the google play API."

Rossen: if it's a functionality for allowin in app purchases - digital goods could be generic and underneath there could be google play or propietary. That way if it cathes on there would be the long lived API... 

Hadley: if we did that who is going to design the higher level API when no 3rd parties at the table.

Rossen: yes - we want to have the higher level API - but they are designing one API.  If they are up for it they should bring more folks to the table and design the higher level API.

Hadley: I agree, but I don't see how that can happen without multi-implementer group coming together...

### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov

Rossen: tiny little proposal.

Hadley: functional but it doesn't have a user need.

Rossen: the user - the platform's developers... 

Hadley: presume it's supposed to be more secure for users but they don't spell this out

Tess: this isn't the only new iframe like proposals - do we need a Cambrian explosition of new iframey things?

Hadley: at least they should be talking to each other

Rossen: i agree - they should all be talking to each other.  Attempting to extend iframes into a useful mechanism for sharing data without breaking CORS - creating a bunch of policies the document can opt into or opt out. From a PoV of extending existing tech and making it more fitting into that example it's decent.  Good enough complexity that requires a careful review IMO.  because they are changing the cross-origin policies essentially - they have to go in and add a bunch of things - e.g. credentials - this to me is a path forward to other changes that would be necessary to land it functional and complete.

Dan: there is a data sharing aspect... feels like these things are being developed in isolation from each other. the potential for developer confusion is high.

... Also, want to support what hadley was saying re user needs. We can ask for that. They need to be very clear.

Peter: should we recommend a task force about iframes?  Get all these diffeent efforts to coordinate?

Tess: I think they are talking - but only maybe in places that are opaque - e.g. blink dev - not collaborating with other engines...

Peter: ... or broader W3C community.

Hadley: that's important.

> Hi @camillelamy! Thanks for this review request.
>
> 1. What end user needs are you trying to support? When would this feature be useful to a user, and why is it worth adding to the web? It would be great if you could add this to the explainer.
>
> 2. We are seeing a number of iframe related proposals, all of which would benefit from input from the rest of the W3C community. To help bring that together, we will be recommending the W3C create a task force on iFrames, and we would very much welcome your participation.
>
> 3. Could you elaborate on the answers in the Security and Privacy questionnaire? For example, where you've just said "No", can you give more detail? 

Rossen: - security & privacy questionnaire answers - enable origins to downgrade default security protections?  they answer "no" - they should have more to that answer about why they believe that this will not allow downgrades - if I have credentials set to emit - and I go and change something that gets me into a cross-origin state... then ... would an iframe without credentials propogate up into a parent browsing context and change its siblings credential states. if so, lowering their state, or increasing the credential sharing? This would introduce new threat vectors.

Hadley: .. a nonce only available to that page .. clears when pages not avaulable...

Rossen: 2 iframes - one iframe an ad and another my bank - i don't want the ad to be able to increase the capabiities of my banking iframe....

Hadley: no different keys - [ref diagram in explainer]

Rossen: i saw the diagram and I couldn't convince myself it was impossible...  We should just ask them if they can provide additional detail on the s&p questionnaire responses..


### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo

Dan: some resent [comments from mike tayor](https://github.com/w3ctag/design-reviews/issues/640#issuecomment-867683881) addressing our questions...

Dan: cross-browser discussions important...  should we try to help make them happen?

Tess: I think they are happening -- i feel there are good discussions on the open issues...  good engagement... one remaining open issue from webkit folks: https://github.com/WICG/ua-client-hints/issues/151

Dan: which leads to - considering we've already fed back positivel on CH - maybe we should close this with a positive review and encourage them to documet all their findings as they progressively freeze out parts of the UA...

Tess: I'd like to say something about the remaining open issue... it would be nice if they resolved it.

Draft closing comment:

'We're largely positive on the approach that is outlined here.  We've already positively reviewed client hints.  We appreciate the time and effort being spent on trying to ensure a cross-browser solution and also on mitigating against ecosystem issues (breaking existing web content).  The privacy benefits of this approach seem clear. We hope that you resolve [issue 151](https://github.com/WICG/ua-client-hints/issues/151
) in a way that improves the multi-vendor consensus around this feature.  We'd also encourage you to engage with the Privacy Interest Group to get their views. However we are happy to close this review as satisfactory.'

[NB based on further discussion in plenary we decided not to post this.]

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Punted to next week prior to meeting.

### [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @kenchris, @hadleybeeman, @atanassov

### [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober

## Breakout B

Present:

Regrets:


## Breakout C

Present: Dan, Amy, Yves, Hadley

Regrets: Ken, Sangwhan, Lea


### ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon

Yves: specific issue with service worker and cache....  looked at discussion.  2 different caches could be a mitigation - one private cache with credential and one without.  

Dan: mark proposed close and close at plenary?

Yves: I will leave some comments in the issue.

### [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov

### [Capture Handle](https://github.com/w3ctag/design-reviews/issues/645) - @rhiaro

Amy: capture handle lets the captured app communicate witht he capturing app - share info with the capturing app - on top of the existing screen share API.  

Dan: What's the usert need.

Amy: Explainer is a google doc - 4 uses cases - sharing in video conference via another tab - being able to change slides without switching tab. Another about analytics.  Not convinced - some surveillancy thing possibly. Detecting unintended captures... "you're about to screen cap this maybe not a good idea..." Then avoiding the hall of mirrors.

Dan: Why would you want to avoid the hall of mirrors? 

Amy: would like to see abuse cases spelled out.  They're S&P questionnaire answers is minimal.  On the basis that the captured app is the one deciding what to share.  

Dan: the captured app needs to opt in?

Amy: yes - 

Dan: we could ask them to put it in markdown - and elaborate on the abuse cases... 

Amy: it's been moved to WICG.  Contraversial issue - they've listed it in the request - problems with Mozilla and Apple - that might be out of date.

Dan: where would it end up after wicg?

Amy: it started in webrtc maybe?

Dan: Was there not consensus in webrtc wg on it? 

Hadley: it would be useful to know more history.

Dan: [left a comment](https://github.com/w3ctag/design-reviews/issues/645#issuecomment-878880998)

Amy: will follow up about abuse cases and multi stakeholder support, and check for relation/dependencies to capturetabs

### [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman

Hadley: seeing this in the context of developer needs (rather than user needs)

Dan: the developer need as articulated by artur is .. restrictions are onerous for developers in complex apps, eg. cross origin sign on. 

Hadley: maybe it should be onerous.. breaking same origin policy right?

Dan: statement about "this proposal makes it easier for developers to enable COOP+COEP without reducing the security guarantees provided by cross-origin isolation" is the key thing that needs to be demonstrated

Hadley: did we review cross-origin isolation? COOP thing? Seems recent from search results (apr 2021) [eg. blog post](https://web.dev/why-coop-coep/)

Dan: [origin isolation 464](https://github.com/w3ctag/design-reviews/issues/464) from jan 2020... Mozilla still views it as 'worth prototyping'. Safari is neutral. What's the implementation status on this? If we're now building stuff on top of origin isolation and it's not fully implemented across other browsers..

Yves: development requires consensus among implementations?

Dan: for building stuff on top of it, for a key architectural plank, it needs to be stable

Yves: needs to be implemented by everyone or sites won't work in some browsers

Hadley: I see Chrome and WHATWG.. 

Hadley: `WindowOrWorkerGlobalScope.crossOriginIsolated` is a specific property of this concept? If so [MDN has a breakdown of implementations](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated) which includes firefox and opera but not safari and IE on desktop, and only incudes chrome android and samsung internet on mobile, if this is accurate

Dan: includes firefox is less concerning, but safari is a worry

Hadley: struggling with what they're trying to solve

Yves: also ask about discussion in webappsec?

```
Hi @arturjanc. Just reviewing in this morning's [TAG breakout](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/07-12-agenda.md). I think the phrase "...without reducing the security guarantees provided by cross-origin isolation" is really the key and this requires some additional elaboration.  The security considerations and privacy considerations sections of the explainer need to spell out some of the abuse scenarios - not from a security-jargon perspective but from a user-needs perspective.  "e.g. bad actors will try to do xxx to use this to steal users' infos". Likewise the user needs at the root of the problem need to be better spelled out - again in terms of what user problem this helps to solve. If it doeesn't solve a user problem but only makes it somewhat easier for developers, and it achieves this by weakening security & privacy guarantees and opening up potential for abuse then maybe it's not a good idea? On the other hand, if it's intended to encourage developers to adopt better security practices then overall it can be a good trade-off.  I think that's what you're getting at but can you try to spell it out a bit more from an end-user perspective?

Also quick question: Referencing our previous review of origin isolation https://github.com/w3ctag/design-reviews/issues/464 and looking back at the implementation status, it looks like there is not good support across engines for this underlying tech (COEP/COOP) yet. Is it premature to start building stuff on top of it?  Are there additional implementer signals for this specifically? Chrome status still shows "no information". 

Also if developer feedback is the thing driving this then maybe this should be linked to in Chrome Status or in this review?

Finally, has there been any relevant discussions in WebAppSec that we should know about?
```

Dan: [posted](https://github.com/w3ctag/design-reviews/issues/649#issuecomment-878903613)

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris


Dan: looks like the requestor has enagged with our feedback and added materail to s&p considerations section... I'd be happy to propose close given it's not a full spec but an addition. Should get Ken's feedback. Plenary..

Hadley: can of worms.... thinking about the fact that raw camera access is being able to access the images that the camera can see right? So in COOP and COEP which we were just looking at the webdev blog post was saying one of the main drivers was the spectre vulnerability, which through timing attacks makes it possible for a window to work out what data is in the image coming from another resource. I don't know how much that screws up what we're trying to do with web xr....

Dan: oh no

Hadley: on that note, plenary

## Plenary Session

Present: Peter, Dan, Lea, Tess, Rossen, Amy

Regrets: Hadley

### Breakout Rollup

#### Breakout A

We closed 

Tess: UA-CH - Mozilla have [changed their position](https://github.com/mozilla/standards-positions/issues/552) to "harmful".

Peter: I read most of his position and agree.

[we review]

[agree it's worth considering changing our stance based on this.]

Dan: I think it's approriate to rethink our feedback based on this - it's the kind of feedback we were asking them to make sure they get.

Rossen: [I was also expressing concerns]

Tess: yes agree.

Peter: Agree.

#### Breakout B

#### Breakout C

Dan: capture handle... it sounds like there's a dispute in WebRTC which is why it's in WICG. So TAG is being asked to intercede in a dispute... 

`Hi Elad - we much prefer progress to be made in a multi-vendor way that emphasises consensus-building. We haven't been part of the discussion but it sounds from what you've said that Mozilla is making an effort to achieve consensus. The role of a standards group is for people to work together to achieve consensus. We'd really like to encourage you to engage in the webrtc group on a path that would be acceptable to all parties. We think doing an experiment with this as an origin trial could be a really good way to gauge developer feedback. However we caution against moving beyond that stage without bringing the results of that research back into the wider discussion and trying to achieve that consensus approach.  In the mean time we are going to close this review as 'too early' and we hope to review a future API that represents the outcome of multi-stakeholder consensus in the webrtc working group.`

Dan: will chat with Amy about it before closing.

Amy: +1

Dan: webxr camera access api which I will write feedback on. Hadley found a can of worms. Worried about camera access opening up attacks. We need to do more here.

### Media WG webcodecs issue (Tess)

Tess: deadlock on the question of the webcodecs api - window vs worker object. Good arguments on both sides.. Disagreement whether to "immediately" expose it on window, or to first ship it just on Worker & come back to the Window question later. Timing question.  I encouraged consensus building.  It could come to us to look at.  

### Issue Triage
