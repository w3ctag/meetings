# TAG Teleconference Minutes - Week-of 4 September 2023

## Call Agenda

### Breakout A (Europe / US) - [2023-09-04](https://www.timeanddate.com/worldclock/converter.html?iso=20230904T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Tag review for Compression Dictionary Transport](https://github.com/w3ctag/design-reviews/issues/877) - @cynthia, @ylafon, @plinss
* [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss
* [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss
* Issue Triage

### Breakout C (APAC / Europe) - [2023-09-05](https://www.timeanddate.com/worldclock/converter.html?iso=20230905T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss
* [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo, @maxpassion
* [ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/863) - @torgo, @maxpassion
* [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon


### Plenary Session - [2023-09-07](https://www.timeanddate.com/worldclock/converter.html?iso=20230907T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov
* [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov
* [Extending the PointerEvent with Unique DeviceId Attribute](https://github.com/w3ctag/design-reviews/issues/880) - @torgo, @atanassov
* [`prefers-reduced-transparency` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/881) - @torgo, @atanassov
* [`inverted-colors` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/883) - @torgo, @atanassov
* [CSS State Container Queries](https://github.com/w3ctag/design-reviews/issues/885) - @LeaVerou, @atanassov
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov
* [Specification Review: FetchLater API](https://github.com/w3ctag/design-reviews/issues/887) - @cynthia, @ylafon
* [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @cynthia, @LeaVerou

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Call Minutes

### Breakout A (Europe / US) 

Present: Amy, Dan, Yves, Peter, Lea

*NB: This is day is a holiday in the U.S.*

#### [Tag review for Compression Dictionary Transport](https://github.com/w3ctag/design-reviews/issues/877) - @cynthia, @ylafon, @plinss



#### [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss

Peter: looks like performance

Lea: one basic thing I'm unclear on is soft navigation something that happens anyway and this is allowing developers to observe it and react to it? Or is this something that developers opt in explicitly?

Peter: something developers do, like by using the history api to go to a url without fetch

Lea: I thought it was about soft nav that already happens, but unclear if clicking on a hash is soft navigation, or only things initiated from history or navigation api?

Peter: good question. also, triggered by user gesture and modifies dom. Does that exclude fragment navigations? Not sure every soft nav will change the dom... but probably true.

Lea: what is the purpose of the criteria that it needs to change the dom? If it is to detect navigations in an spa that change the page vs navigations that scroll you to a different section, what about cases where developers use hashes to display a different part of the page and hide other parts, or implement tabs. All sorts of these things sound lke they should be soft navs but it wouldn't modify the dom if it's all done through css.  And what about cases where you have a component which changes its content and changes happen in shadow dom.. does that count as a dom change? seems hairy. How long after do you listen for a dom change? what if the navigation happens now and the dom change happens seconds later because there was an animation first?

Peter: seems like a weird requirement. The purpose for changing the url is to reflect state, that you want the user to be able to share. Maybe they should describe it that way somehow. But they're talking about a  heuristic that the browser can use to detect that this happened. Then I'm wondering why it's the fact that you called the api to change the url? Unless they do want to distinguish just changing the fragment. But why exclude that? Could be state.

Dan: motivation section is well written, I understand where they're coming from. From a performance standpoint.

Peter: in general .. seems like a hole that these soft navs aren't triggering performance apis

Dan: is soft navigation a term of art? I couldn't understand if they're defining this term, or are they saying this is what soft navigations are and this is what the soft navigation api is... are they making an assumption that we already know?

Peter: my take is that they're defining the concept of soft navigation, but I don't know if this is a common term

Dan: related to Lea's point - it seems very narrow, this definition. There could be other ... it sounds to me like a UI/UX thing. Rather than a api.. sounds like a pattern .. they're defining an api and a pattern? Is there a term of art already used for same-document navigation?

Peter: same-document navigation

Peter: not just that there's a dom manipuplation, but a 'meaningful' one. "reasonably considered navigations" - sounds scary. How will they make that work? They have an open question about gmail's compose button, and argue that would be considered a soft nav, or could argue it's an interaction.  Trying to determine some definition of interaction vs navigation.. not sure if that's a distinction with merit, that a heuristic can reasonably determine, except for on a handful of known sites like gmail. Does that make sense?

Lea: yes

<blockquote>
Hi @yoavweiss -- thanks for bringing this to our attenntion.  Our biggest question has to do with the question of DOM modificaitons. You state a soft navigation "modifies the DOM" but it's not clear why this is a requirement? It seems like you're trying to make a distinction between "navigations" and "interactions", it's unclear how this subtle (and underspecified?) distinction can be reliably determinied by your proposed heuristics. We can imagine that the heuristics can be defined to catch current examples but would be wrong about future applications. We wonder if simply using the navigation API should be the trigger, and then possibly provide the developer a hook to filter out navigations they don't feel are worth tracking would be more reliable?
  

</blockquote>

#### [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss

Amy: I looked at this - seems probably fine - they've identified a problem and made an effort to solve it.

Amy: my other thought with FedCM is that a lot of it is early - and we're spending time on small feature reviews...

Dan: if it's being put forward as a more privacy preserving alternative for federated sign-in and enjoys some level of multi stakeholder support , any way we could accelerate it through .. if we can add energy into that it's positive. One of the things people want to replace the use of 3p cookies for is federated ID - it would be nice if we can say they can use fedcm. In Chrome status it says firefox under consideration, and going to origin trial.. For this feature they have an indication of positive or non-negative feelings from mozilla but link to a github thread.. not to any standards positions. We could ask about that.

Dan: can't find a moz standards pos.

Peter: a little confused - it looks like the problem they are trying to solve is IDPs silently tracking users - solution is IDP telling browser - wouldn't it be a problem if the IDP is malicious?

Amy: Isn't it a malicious RP not malicious IDP?

Peter: in their pdf they say the problem is the "tracker" gets a credentialled request that allows them to track the user at the RP.. makes it sound like the "tracker" is the IDP. You're visiting an RP and they want to expose some UI that says go sign in with google or whoever and they don't want to show that if you're not logged into google. So the browser can make a request to google to check if you're logged in.. which lets google know you're visiting the RP. Stopping the RP from calling the IDP if the IDP says you're not logged in. In an example they show the "tracker" is an IDP

Dan: wnat to clarify the problem they're trying to solve, and how to mitigate against a malicious IDP

peter: IDP has to opt in to giving a mechanism it can't use to track you. I don't see why an IDP that wants to track you can't just opt out.

Amy: the fedcm people have made a PR to the login status API that is currently [under review](https://github.com/privacycg/is-logged-in/pull/54). Lots of multistakeholder discussion

Dan: login api doesn't look very active, lots of open issues. We haven't reviewed it. Would be useful to know more...

<blockquote>
Hi @cbiesinge: a few questions came up in our discussion today on this one:

1. Our understanding is that this is designed to prevent an IDP from tracking users. However, the mechanism provided allows the IDP to optionally signal the signed in status of the user to the UA. Couldn't an IDP that wants to track users simply not send the signed-out signal and thus still get the silent requests?
  
2. Regarding multi-stakeholder support, we see from ChromeStatus that Firefox is listed as "under consideration" - however I don't actually see a Mozilla standards position on this - is there one? Is there a webkit standards position? 
  
3. What is the general status of FedCM from an implementation stand-point?  What is the multi-stakeholder story with FedCM right now and when do we expect to achieve "critical mass" for FedCM?  This is especially relevant to the discussion on deprecation of third party cookies, as federated sign-in is often cited as a use case supported by third party cookies.
  
4. Small addition question - you've reference a PR [against is-logged-in](https://github.com/privacycg/is-logged-in/pulls) in your explainer - however the is-logged-in API itself seems to not be very active – and we haven't been asked to review it. Can you shed some light on the status of this API?
</blockquote>

#### Issue Triage

### Breakout C (APAC / Europe) 

Present: Dan, Amy, Max, Yves, Sangwhan (2nd half)

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
#### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
#### [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss

Dan: closed this because there was no explainer but they've done one now. Has multistakeholder support.

Yves: I don't see any issue.  I think we should close.  Maybe wait for Sangwhan...?

Dan: I'm happy to close...  Let's set it as proposed close and close it at the plenary.

<blockquote>
@Orphis thanks for this updated explainer.  It's really good to see that this proposal enjoys support from multiple browsers.  Ideally I'd like to see a bit more discussion of user needs – which you may feel boil down to "more seamless video calls" – but it would be nice to have that spelled out.
</blockquote>

Sangwhan: happy to close.

**closed**

#### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo, @maxpassion

Sangwhan: the permission model - serial needs permission and bluetooth needs permission - those are separate.  How does that work?  Do you need both bluetooth and serial at the same time?  The permission gate would be at a different API surface trigger... couldn't see how that's supposed to work.   There might be cases where you want to grant browser enumeration of serial devices but not bluetooth serial?

Yves: you will enumerate on bluetooth and then it ..

Dan: feels to me this is something the browser should be doing - seems like this is a bluetooth thing but it's using the serial profile so browser exposes it using the webserial api to the application and as far as the app is concerned it's a serial device

Sangwhan: so browser does the initial... pairing process.. at the point you paired.. is that required before you can enumerate a serial port? 

Dan: in that case.. most devices have a mechnism to pair a bluetooth thing that's built into the OS. Why not have the device do the pairing? Abstract away the fact that's bluetooth. Why does the web application have to know that it's bluetooth? Why doesn't it just see it as a serial device and bluetooth is hidden away

Sangwhan: that's what I think I'm reading from the explainer. There's an implication that the bluetooth connection has already been made and that i'tll be exposed a serial, but who does the bluetooth pairing? If it's the browser.. what is the lifecycle that goes from bluetooth pairing to this. I don't undderstand how that's supposed to work. If the implication is that the OS is supposed to have paired it .. if it's a serial port already at the point it reaches the browser that's fine, but what if you want to do it fully on the browser? How do permissions work in that case?

Dan: agree. It's obviously using the serial api

Sangwhan: but what happens before that

Dan: what's the full flow

Sangwhan: it's valid to answer that it's supposed to be paired at the OS level. But then I have questions about ChromeOS.. (homework for myself)

Dan: drafted my comment.. I'm personally not against this API. I'll leave it and Sangwhan you can follow up with anything additional

<blockquote>
There's no doubt that communicating with devices, particularly in an educational context as you've elaborated, is a compelling use case for computer programs.  Clearly, however, there is a difference of opinion amongst implementers about whether web applications should be empowered to make such connections.

We've reviewed the [Web Bluetooth API posotively](https://github.com/w3ctag/design-reviews/issues/139).
  
We've also reviewed the [web serial API](https://github.com/w3ctag/design-reviews/issues/431) - for which we recognized the use case but also we expressed concerns about multi-stakeholder support.

Speaking personally, I'm a big supporter of these APIs. I've personally demonstrated Web Bluetooth on stage at developer events.  I fully get it.  However, as TAG I have to acknolwedge that the development of these capabilities has not brought other implementers along.
  
Putting aside the multi-stakeholder considerations, we're not clear on some aspects of the user flow and permission model.  The explainer could benefit from spelling out how a device gets connected, how the permissions are requested, etc... ?
</blockquote>
  
#### [ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/863) - @torgo, @maxpassion

Dan: Some discussion... URLPattern is spec'd in a CG but not a standard due to other browsers not implementing. Doesn't sound like there's a technical issue with it.. Anne said they'd be supportive of it if the venue was resolved

Yves: position from other browser vendors is clear

<blockquote>
Hi @domenic - thanks for that clarification.  As with a number of other current reviews, in that case, I'd like to express concerns that we are building new capabilities on top of shaky ground – that is, existing specifications that do not have consensus and do not have multiple implementations across multiple browsers.
  
Further to that, we have another open review, [Compression Dictionary Transport
](https://github.com/w3ctag/design-reviews/issues/877) which also makes use of "URL Patterns" but [does not appear](https://github.com/WICG/compression-dictionary-transport/blob/main/README.md#dictionary-options-header) to reference the URLPattern spec.
  
Could there be an option here to work together to specify static routing without relying on URLPattern, or to specify a fall-back?
  
Alternatively, [is there a way forward](https://github.com/WebKit/standards-positions/issues/61#issuecomment-1527486428) to bring URLPattern forward for standardization that could unblock multiple implementations?
</blockquote>


#### [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman

<blockquote>
  
Hi @mkhraisha thanks for your review request.

Is it possible for an issuer to use their own value for the `statusPurpose` field? It's clear that the strings `revocation` and `suspension` must be used correctly as defined in the spec, but given the extensible nature of JSON-LD it looks like it would be possible for additional terms to be introduced here. Is there a risk of this being overloaded and potentially leaking other information about the credential? Should the spec be explicit about constraining the values *only* to these strings, or has it been deliberately left open to permit other strings to be used without additionals to the spec? If it's the latter, what other (legitimate or malicious) values do you think we might see here?
  
Do the vavlues of `statusMessages` carry simiar risks related to overloading/data leakage, as these are defined by the issuer?
  
I have more general concerns about malicious issuers tracking credential holders, which I've no doubt has been thought about at length in the WG and wider community. It would be great to see pointers to more work on this, and mitigations in particular, given the types of organisations which are likely to issue credeintials, the limited options people may have for credentials that are accepted, and the power dynamics involved here.
  
Thanks for your suggestion in the Security & Privacy questionnaire about asking about maturity of dependencies. I've [raised an issue to add this to the questionnaire](https://github.com/w3ctag/security-questionnaire/issues/155). Do you have an answer in mind for this question for the VC Status List spec?

</blockquote>

*amy to post*

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon


### Plenary Session - 


Present: Peter, Amy, Dan, Max, Sangwhan

Regrets: Yves

#### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
#### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov
#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

Sangwhan: I will reach out to TC39 folks to discuss this / we can also discuss at TPAC.

#### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov

Sangwhan: multiple subsystems in the web platform... webrtc and webaudio... webaudio is carved out as its own island.  Mainly because of the latency requirements... This proposal is trying to address this - that's great - but only for webaudio. WebGPU and WebRTC...  Maybe we could discuss at TPAC because we have a necessity to solve this problem. 

Dan: Noting multiple stakeholders - Google and Mozilla people involved. 

Sangwhan: Converging worker and web audio...

#### [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov

Peter: entropy probably the wrong name... I think this is OK but would like to get Rossen's opinion.  I have a concern about how this might expose additional fingerprinting surface or allow side-channel attacks.  I accept it's "past" state but it's also coming along side of some high resolution timers... which can be used for side-channel attacks.

*peter to leave comment*

#### [Extending the PointerEvent with Unique DeviceId Attribute](https://github.com/w3ctag/design-reviews/issues/880) - @torgo, @atanassov
#### [`prefers-reduced-transparency` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/881) - @torgo, @atanassov
#### [`inverted-colors` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/883) - @torgo, @atanassov
#### [CSS State Container Queries](https://github.com/w3ctag/design-reviews/issues/885) - @LeaVerou, @atanassov
#### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov
#### [Specification Review: FetchLater API](https://github.com/w3ctag/design-reviews/issues/887) - @cynthia, @ylafon

Sangwhan: I have looked at this... I like it. 

Dan: It's WICG .. it's BFCache ... It's WHATWG...

Sangwhan: if you have a document and user closes the tab... if you have a fetch in flight you can't know if it happened.  So there is the beacon api... which didn't follow the fetch pattern. So they redesigned it... New name is FetchLater. Less confusing... It implies it's a delayed fetch but what it really does is add a guarantee... The part where I have questions is the use cases.. They provide a high level use but not a real application use - what kinds of user-facing functions would this be used for? It's clear what the telemetry use cases are...  I don't see it as harmful.

Dan: adds complexity to the web platform - if it's only for telemetry ... then is it worth it?

Sangwhan: they could also use it in cases where they haven't finished sending the final state of the app back to the server - e.g. writing a form and therte is a heartbeat where it's saving your current progress... Some anti-patterns such as "do you want to close this tab?" blocking - could go away.

Sangwhan: *will leave comment and speak to the requestor*

#### [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @cynthia, @LeaVerou

Dan: there's going to be a breakout on installation at tpac, but I can't be there. Sangwhan can you be there?

Sangwhan: yes

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Amy: what actual additional power does this grant? What happens if a site lies about their urls?

Peter: the manifests scopes down the origin.. and this expands it... doesn't say if it grants access to *data* of the other origins or not. Doesn't say one way or the other. Does allow you to capture links. You download a malicious app, install it, it declares it's scoped to your bank, it has a link to your bank, displays a url that looks like your bank, and it fishes all your credentials from a login page. It does say your bank has to have an intercept links authorization for that to happen

Dan: where is that configured? THe bank?

Peter: presume that would be in a manifest file for your bank

Amy: as long as that's opt-in..

Peter: maybe not for a random bank, but amazon might use this and say yes intercept links because they're using it within their own domains, so a malicious app could then use it to phish your amazon credentials. It says it's allowing anybody to intercept links, not a specific list of other origins to intercept links. If it's a bidirectional association and both sides have to have installed apps with that association in the manifest, and all it does is allow link capturing and prevent the ui from saying you're going to another site, and doesn't expose any origin information, I could live with this. But there's a bunch of ifs.

<blockquote>
Hi @diekus – Briefly, we're very concerned about the way that this proposal changes the same-origin model, which is a fundamental part of the security aparatus of the web. Hence we think we need to tread very carefully.  We think the explainer should be very explicit about what the expanded scope does and does not allow access to.  We'd also like to see some specific use cases and discussion of abuse cases (and how those abuse cases are mitigated). E.g. if you are tricked into visiting or downloading a malicious app that is spoofing your bank, and it includes your bank's origin in its scope_extensions field, are there additional exploits that the malicious party could exploit (e.g. obtaining credentials or capturing links)? Are there any implications for access to local storage from different origins?
</blockquote>

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
