# TAG Teleconference
#### 12-14 December 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-12-12](https://www.timeanddate.com/worldclock/converter.html?iso=20221212T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780) - @hober, @torgo, @hadleybeeman, @plinss
* [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

### Breakout C (APAC / Europe) - [2022-12-13](https://www.timeanddate.com/worldclock/converter.html?iso=20221213T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) & [Packaging](https://github.com/w3ctag/design-reviews/issues/762#issuecomment-1328793218) - @cynthia, @torgo, @maxpassion
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon


### Plenary Session - [2022-12-15](https://www.timeanddate.com/worldclock/converter.html?iso=20221215T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Amy, Peter, Yves, Hadley

Regrets: Lea, Dan, 


### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

### [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

### [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780) - @hober, @torgo, @hadleybeeman, @plinss

Amy: one of their changes is that they have a spec now

Yves: Mozilla standards position?

Amy: [deferred until Privacy Pass was done, no update yet](https://github.com/mozilla/standards-positions/issues/261)

Yves: [webkit](https://github.com/WebKit/standards-positions/issues/72)

Hadley: seems like they are building on an earlier version of privacy pass that will need to be updated

Amy: ask them if we should wait to review until they've rebased their spec on updated privacy pass? (Given they say it will be a month)

Hadley: maybe this isn't the most useful time for feedback for them

Peter: seems reasonable to ask them. We did an early reivew of this a long time ago. This still feels like an early review.

Hadley: this is already in chrome 111? [chrome status](https://chromestatus.com/feature/5078049450098688)

Amy: nothing in PING repos

Peter: weird thing about redemption.. requiring additional information beyond the URL to make the request. They have a note in their explainer about the use of it on top level navigation. That's a potential future extension, seems like more of a core use case. Wondering if the redemption should be something more ambient in the browser, rather than something explicit. What's the use case for an explicit redemption on fetch? Why do they think that's useful?

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

### [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791) - @LeaVerou

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

Amy: we talked about this a lot but haven't updated the issue. I'll go back and find past minutes.

Peter: how does EU ruling about targeted advertising on Meta play with Topics?

### [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman

Amy: [there has been back and forth on their issue](https://github.com/w3c/dxwg/issues/1530). Can we close this?

Hadley: sounds sensible. This discussion came out of joining up groups of work, so looking for an opportunity to reuse rather than create from scratch. From what they said it doesn't seem suitable unless they wanted to readdress all of RDF Lists, which isn't in their charter.

Peter: We can propose close

Hadley: will ping danbri to close the loop

**proposed closing**

## Breakout C

Present: Dan, Max, Yves, Amy, Sangwhan, Hadley
Guests in 2nd half: Fuqiao Xue (W3C), Zitao Wang

Regrets: 

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Sangwhan: I don't see a down-side...   The permission policy is a choice of the origin... to disable unknown handlers... They should be aware of the breakages that can happehn when load handlers don't kick in. If you have foreign content that ... an origin can take in foreign scripts and iframes -- if that taps into the unload handler and tries to block user from navigating away from the page then it's a bad thing. Not an origin choice to make...  One antipattern - a site hooks into unload to do weird stuff - shoot off a beacon or try to block it. 

Dan: Malicious site?

Sangwhan: this changes nothing for those cases - but if you have a modal ad - as long as the ad network script is running on the browser context... giving the origin control over that is probably not a bad thing.  This gives the origin the option to block the unload handlers... 

Sangwhan: so personally LGTM. Also makes bfcache less painful. When you have an unload handler you can't bfcache the page... so in that sense this is good... If you have the permission policy in then the unload handler will be a no-op. 

Dan: multi-stakeholder... in Sept Mozilla was asked for position, still no information

Sangwhan: Mozilla standards positions in the abyss.. new person working on that.. have suggested a connection

Dan: I'm worried from multi-stakeholder pov. Satisified with concerns?

Sangwhan: there's no *harmful* signal - but for cases where browser vendors are not responding, should we be concerned about it?

Amy: well concern is that if there's no implementer interest and it only gets implemented in one browser then what are the risks of fragmentation...

Sanwhan: e.g. mozilla have been vocal about if something is actively bad. On the fence about pushing due to Mozilla staffing issues. Chromium have contributed tests to Mozilla that have landed.

Dan: [leaves note](https://github.com/mozilla/standards-positions/issues/691#issuecomment-1347922197)

### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Amy: I had a chat with Sam W about this, PING are reviewing as well - deferred on doing a full review as they didn't have a full explainer. They've posted an update... http section is still tbc. They have a longer explainer now. 

Dan: similar discussion to miniapp...

Amy: app store model...

Amy: I'll do a proper review.  They didn't do a privacy & security... so "nothing to do with PII" - which is not what the questionnaire is about.

Dan: web security model.

Hadley: that privacy and security questionnaire is important for this. It would be good to see.

Dan: [leaves a comment](https://github.com/w3ctag/design-reviews/issues/768#issuecomment-1347906948)

### [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon

Amy: looks stalled until next year.

### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) & [Packaging](https://github.com/w3ctag/design-reviews/issues/762#issuecomment-1328793218) - @cynthia, @torgo, @maxpassion

Dan: you wanted to chat about the [feedback](https://github.com/w3ctag/design-reviews/blob/main/reviews/miniapp_packaging_feedback.md) we had sent. We were talking about packaging, in the context of lifecycle of a miniapp, and the whole question of being able to make use of the web security model is the key point. This was a TAG consensus document. As a recent example we wanted to draw your attention to discussions around the security model of apps embedding a webview component, injecting custom js, and using webviews to bypass things - happening in the webview CG - all of that is built around these notions of the web security model, based around the origin concept with content delivered over https and the UA keeps things like storage segmented, so you can multiple contexts running in the UA where information does not leak across origin boundaries. Whatever mini app does should follow that same model so we can make sure we're building something that gives the user a strong guarantee of security. We were asked for a specific recommendation, so we suggested taking a look at the packaging solution that preserves the origin model, such as what is going on in the web packaging work, bundling and signed exchanges. We hope they would be open to working with the miniapp group to solve miniapp use cases.

Fuqiao: I created [an issue](https://github.com/w3c/miniapp-packaging/issues/64#issuecomment-1326673137) on the miniapp packaging repo about this and one of the editors has some replies. He did some research and would like to talk with the TAG and web bundling folks.

Zitao: I have discussed with Martin about this part. Concern - miniapp origin .. ?? Baidu and Alibaba and other vendors are using zip format to provide the functions. We analysed potential way to make ... we can discuss in the WG meeting to find a way to consensus. 

Sangwhan: one of the things that is concerning is a de facto standard that is widely adopted in China, but that doesn't mean w3c can rubber stamp it as a standard. There are bars we have for security requirements. We see gaps here. We have flagged them. If you want to rubber stamp the implementation because it's a defacto standard that's a separate discussion. I'm not sure we're here for that. There's a parallel set of technologies that are not being used that solves some of these problems, though there are issues. Those folks are likely willing to work wth you to figure out how to solve those. If the default approach is that it's already well-adopted so we should just sign off, I'm not sure what we should do here.

Zitao: we know this. We agree. We need some way to provide a compromise. The best way to find a way good for existing implementations and also to respect the existing standards. That's why we discuss with the authors to find a way address the issues. This is our direction. We don't want to just use the existing implementation to standardise the packaging.

Dan: two issues here that are conflated. One is the web security model. The other is the packaging format itself. The TAG has raised issues on both. We can usefully separate those issues. Speaking for myself and my understanding of this, I think the web security issue is higher priority. But I think Sangwhan has raised important issues about the zip format itself from a streaming perspective that may be useful to discuss. I think we should try to discuss them separately. Even making progress on one would be a good step forward.

Max: From Martin's response he explained the reason why the design uses zip instead of other standards. Also mentioned about why the miniapp wg not using http exchanges, because there are some use cases the http signature mechanism was not suitable for miniapp. The miniapp wg experts can explain to us what are those use cases to justify what Martin concluded, that http exchange is not suitable. The other thing - about the origin, I noticed an author has replied on the issue to mention the [explainer has been updated to explain miniapp origin](https://github.com/w3c/miniapp-lifecycle/blob/main/docs/explainer.md#miniapp-origin)

Sangwhan: Zip is a bad format. But we're less concerned about that than the lack of an origin. If the security model is in place we'd be okay to make a compromise somewhere about packaging. The web packaging model does not have a good story for long term installed apps. No story for what happens when the origin disappears - that's to be addressed. But the security model is a huge issue and we don't want to compromise on that.

Dan: taking a look at the miniapp origin part of the explainer, I still don't see discussion of a cryptographically secure origin. Martin asks if HTTPS transmission of zips enables us to guarantee.. we should explore... I hadn't seen discussion of an in-zip digital signature. What format would that be? Bound cryptographcially to the... what's the chain of trust between the https origin and the in-zip signature?

Max: does the section on miniapp origin answer our concerns?

Dan: I see in Martin's comment in-zip digital signature, but in the explainer I'm not seeing anything about signatures, missing something..

Yves: there are multiple ways to ensure trust here. The full cryptographic things which can be done at one time, as in signed exchange. And ways to delegate trust to someone who did the verification first hand, which is the model you have in most app stores via universal links for apple, iOS and equivalent for android which has another name. Delegating the authenticity of the link to the party who is distributing the app. Depending on the choice that miniapps wants to do there are different solutions to ensuring that the origin model is respected here. For me, we need one. But up to the WG to decide which one is enough for the use cases.

Fuqiao: about signatures.. Dan mentioned signature isn't mentioned in the lifecycle explainer yet. I think that's because signature schemes are specified in the packaging spec. probably we should move that section, and add the signature part. The lifecycle spec I don't think it deals with the signature.

Dan: what's the signature that's used in miniapp packaging? https://github.com/w3c/miniapp-packaging/blob/main/docs/explainer.md#security-considerations

Sangwhan: pkcs7 and apk signature scheme. There's a similar thing to pwas called trusted web activities which does the same thing on the play store. That is not a standard - for a good reason. Ultimately the inherant risk is that there's always a risk that we end up with a supply chain level contamination upon delivery. One of the things is that the miniapps proposal entrusts the distribution channel to be trustworthy, and I take issue with that. Delegating that over to the distribution channel goes against the security model of the web. Google does it for the play store and I think there were discussions about standardising it but it was shot down, it's a bad idea. We want a zero trust model from origin to user, where every player in the supply chain cannot be trusted. That's the gap where we're going back and forth here.

Dan: https://web.dev/webapks/ - note existence of web apk. Having worked on Chromium based browsers, thsi was a key enabler for progressive web apps, that enabled them to get signed by a third party key server in order to appear on the device as an app even though it's a webapp. This is a technology that is out there. There are at least two implementations of it - google has one tied ot the android app store, and samsung has one for the samsung app store for web apps saved to the home screen using their browser. Might be worth taking a look at as a halfway house between... although all that i's doing is provides guarantees from a platform perspective not from an origin perspective. Maybe worth taking a look at.

Sangwhan: that is basically the scheme proposed in the security considerations for mini apps - the distributor can be trusted

Dan: but in the case of a progressive web app, it does not provide additional guarantees over and above what it would be if you simply visited that website over https from your browser. It's just that it provides some extra UI affordances in terms of being able to show up in the app list

Sangwhan: that's basically what this proposal seems to be suggesting. I'm not so sure if w3c is the right venue to sign off on a proposal like that. There's a mention about a business decision and business policy -  yes it can be business policy - but this level of ambiguity on potential supply chain attacks is something we want to adopt as a standard on rec track

Max: I notice that in the explainer link, mini app origin section, the author do clarify that they follow the same origin policy. Maybe the part belogning to business decisions should not be in the standard. Maybe it's better to clarify which part is proposed to be standardised and which part is not. That will help our discussion. Hearing what Sangwhan mentioned, assuming that all those parts will be standardised in w3c but according to the explainer I have the impression that is not the case. Some parts standardised and some parts should not be included. Can the cochairs or editors do that to help the discussion?

Dan: I think the action is for the miniapp group to come back with additional clarifying information that addresses the issues that have been raised here around how the model has been proposed preserves the web security model. New information that has been provided, including Martin's comment that we need to look at. I'd also suggest I'll sned a message to kenji from google who's the person we talked to last time from the packaging.. point him towards this issue and ask him to engage with martin. That might provide some useful discussion points.

Sangwhan: it says in the explainer that miniapp follows the same origin policies - it's without grounds unless you have a way of validating the origin. If that guarantee is gone then all bets are off. You can follow same origin policy as much as you want, but if you can't guarantee the content is from that origin there's no point.

Zitao: Thank you for the meeting and discussion. The WG need to find a way to address the issues. Provide a secure way to guarantee the origin. And to provide mechanisms to guarantee the authority chain(?). And integrating packaging.. makes sense. Next WG meeting we can have time to discuss this.

Sangwhan: really suggest you talk to kenji. They went through this entire process.


## Plenary Session

Present: Dan, Peter, Max, Sangwhan

Regrets: Amy, Yves, Lea

### [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman

### Breakout Rollup

#### Breakout A

Peter: DCAT - can we close it?

Dan: pinged hadley



#### Breakout B

#### Breakout C

##### [Issue 691](https://github.com/mozilla/standards-positions/issues/691)

Sangwhan: I suggested to close unload but ...

Dan: I asked moz what their position is https://github.com/mozilla/standards-positions/issues/691#issuecomment-1348340664 - some negative comment from smaug---- there so, also pointing to a [negative comment](https://github.com/w3c/webappsec-permissions-policy/issues/444#issuecomment-1047829132) from Anne... so...

Sangwhan: yes... it can [break iframes].  If the iframe has functionality that depends on an unload handler then it will break things.  For scripts from a 3rd party that exexcute in a doc and have an unload hancler then it would break things.  However - this is an opt in behaviour...  Given that this is opt in and gives the origin a choice - personally don't see the harm in this.

Peter: it's default allow... so basically this is just a way to allow sites to turn this off.. I thihk I agree with you it seems relatively tame. If the iframe is an ad then you don't know what ads you're going to get - so you could be breaking things you don't know you're going to break.

Sangwhan: the unload handler is used for more evil [abuse cases] than good...  For context where it makes sense - e.g. editing a document - it makes sense.  

Dan: it feels like the cases this breaks are the abuse cases of unload policy...

### Issue Triage
