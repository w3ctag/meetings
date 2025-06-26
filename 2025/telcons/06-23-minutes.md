# TAG Minutes - Week of 23 June 2025

## Breakout A (Asia / Australia / West America) - [2025-06-24](https://www.timeanddate.com/worldclock/converter.html?iso=20250624T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Matthew Miller, Tim Cappalli, Xiaocheng, Martin, Marcos

Regrets: Max

Scribe: Jeffrey

### Special guests: [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @torgo, @matatk

#### Related Origin Requests

Martin: First in the list is Related Origin Requests. This smells really bad: cross-origin communication, violating the privacy principles we set up. Fact that it's user-mediated somewhat ameliorates that concern, but doesn't completely cover it. Not clear that the interaction with a token is deliberately allowing the release of information across sites like you might with Storage Access or FedCM, which are the cross-origin [ed: site?] mechanisms we have. We see the use cases, but that doesn't create a justification. Talk about this?

Tim: Both the RP ID and the origin can be presented to the origin. Restricted to 5 labels, which was consensus. Some wanted it to be much higher, but we expect this to be mostly country codes. Largest deployments wouldn't be able to use this without this feature. 

Martin: If that's the case, why have the 5-label restriction?

Tim: Just do cctld?

MArtin: Looks like you're going down the design path of Related Website Sets. That least to lots of problems. But seems like the same scenario. But you're talking about something like FedCM. Like google.com.au and use the passkey that I registered at .co.jp. In that case, it could have the same UX as FedCM.

Tim: Kinda does? Every passkey flow has a dialog.

Martin: At that point, we're not stopping Google's IDP from being used across 1M sites. You've met the same bar, so why have the restrictions on the size of the set?

Tim: Difference is that these are only same-party credentials. Federation is the opposite.

Martin: But that's an artificial construct, since google.com is different party from google.co.jp.

Matthew: There's an explicit opt-in so organizations have to establish relationships with eachother.

Tim: Far more restrictive than first-party sets.

MArtin: Good safeguards, since you want consent from entity that created passkey and RP. Saying "I have this credential, and I'm allowing some other entities to access it." That's the mutual acknowledgement. You've got this restriction on the number of origins that doesn't make sense.

Tim: We put that restriction in so a social media provider can't add all your origins to their RP. Majority of RPs needed at most 5, and jsut for vanity use cases. E.g. amazonprime.com vs amazon.com.

Martin: If we look at how FedCM operates, and it's the same or scarier. Why do you need that restriction. You say "I'm going to amazonprime.com and logging in with amazon.com credential". Looks like FedCM flow. The Amazon restriction to only 

Matthew: Dancing around the idea that federation should be the solution instead?

Martin: Trying to bring this to the user-experience level. I'd have started with "federation is my preferred approach", but that's not how the system operates. The UX is I go to a website and want to log in. Asks me for a passkey. Something happens. Some passkey I created on another website is activated. Tim pointed out that the question presented is "you're on this site; can this site log in with this other passkey". Depends on the UX whether I think it'll be acceptable.

Tim: Are you advocating for dropping the limit. 

Martin: If the defense is the UX. Problem is that the UX wasn't present. No discussion of the UX in the explainer or spec.

Tim: No UI guidance. We don't discuss UI in the spec. Origin in the url bar is what needs to be validated. This changes the selection.

Martin: Don't want to overspecify the UX; that's a browser competition thing. At the same time, if there's nothing in the spec that constrains the browsers, that's a problem.  If the expectation is that the browser will present information to the user in a particular way so the user needs to understand the interaction, we need to write that down.

Tim: Very rare that the browser will show UI. WebAuthn client is different from the user agent. WebAuthn client does this lookup.

Jeffrey: Martin is advocating for one of two things: either this is restricted to same-site (no information crosses the boundaries) OR it should have something about the UX in the spec, minimally that it should ask permission to link identities across the sites.  In the latter case, there is no need for the five site restriction.  The handshake is still useful to have sites opt-in to communication.  There has been a lot of disagreement about how much UI to put in specs.  Alex Russell argues for none, Martin and I argue for some.  For instance, you need to tell the user both sites.  It's true that browsers can't do that themselves, OS needs to.  The spec could still state requirements.


Tim: That does largely exist. Even before this, it's expected to show "you want to show this RP on this origin". That does exist. Hasn't been a huge shift here. With cross-origin create, we added the ability to pass both top-level and real origin. Don't know how to require UX for this when it's required for the other pieces.

Martin: I think that's not enough. Had a debate around FedCM. It has a chooser arrangement, not a "click here to lose privacy". Means that when you go to a website, the choice of IDP -- in this case the choce of passkey provider -- is something the user chooses from a list. Not just presented with a yes/no option. If I can't produce that UI, that's a problem. And I think you can't because it's passed to the OS.

Tim: I struggle with the comparison to FedCM: they're fundamentally different.

Martin: I don't want to be in a situation where someone's presented with an option where one is the wrong one to press, and there's an irrevocable loss if they pick the wrong one. I fyou press yes, your identity is permanently linked. E.g. Big Company buys popular service, they immeidately want to link accounts. Arrive on service you've been using for a while, and it shows a message. Gibberish. "Sure, why not?" And that's irrevocable. Scenario that'd happen with these things. Understand that most experiences aren't that. Usually easily understood.

Tim: In order for that to happen, both parties would have had to exchange their user databases on the backend.

Martin: Sure; they could already do that, but user doesn't need to be complicti.

Matthew: W3C Position or TAG position?

Martin: No, but we have principles that state people need to be in control.

Jeffrey: If a site says that they want to use a passkey, the OS might find passkeys from other places.  I might disagree with Martin about FedCM, which allows that.  Martin's goal is that it is possible to build a chooser rather than an accept/deny interaction. With a list, users are a little bit more in control.  Maybe they can see that passkeys exist and make a choice.  Passkeys could offer passwords as well, because it uses credential manager.  I'm less worried than Martin: it could be built to provide a list.

Tim: In the case you have a passkey where the RP and passkey RPID match. I have an amazon.com passkey, and I visit amazon.co.jp with an RP ID of amazon.com. It'll look for amazon.co.jp, and offer that up.

Jeffrey: That is what Martin is worried about.  Can the browser make that possible?

Tim: The user will literally not have a credential.  Large deployments say that they can't roll out passkeys without this.  Won't be able to access sites when traveling.

Matthew: Time check.


#### Cross-origin iframe registration

Martin: I'm on a vendor page, and my bank has a frame and wants to create a passkey?

Tim: Neither of us was involved in writing that. I think it is about SPC. I think it's about the get, not the initial enrollment. Let's ask Stephen. Not universal agreement on this one.

Matthew: PR is at https://github.com/w3c/webauthn/pull/1801.

#### Client Capabilities

Martin: Relatively straightforward. Fingerprinting, but mitigations are poor. Permissions policy isn't effective.

Tim: Those mitigations were from Mozilla; we didn't have any to start with.

Martin: Giving UAs discretion about what they reveal is the strongest, but worst for web compatibility.

Tim: That also came from mozilla. John wanted cross-device. Requires device to have bluetooth. If you're a browser that supports Web Bluetooth, so you're getting BT permission for other things. That should correspond. Mozilla wanted to not return it or return false. In no case where it's false in one browser and true in another, is that worse than not having Client Capabilities in the first place. If site can't tell what's there, they can only do basic flows.

MArtin: Strongest mitigation is the reduction of information along those lines. But doesn't seem liek there's been rigor put into that. There's been work on WebGPU to bucket things instead of the multidimensional thing.

Matthew: Are there any other feature-detection APIs to look to for prior art? We'd look at those for guidance. (WebGPU)

Martin: Most that exist aren't great examples. WebGL has queryable extension points, but it's too rich a fingerprinting surface. Better to say "if you have this large group of features, suddenly they all appear".  Not sure any of this is justifiable. That discussion needs to happen. How much fingerprinting, and what do we get in return?

Matthew: If it can be seen as a way to check for various features. Through that framing, how's it greater than individual feature detection that you could do without it?

Martin: typically you can feature-detect on a piecemeal bases, but it only depends on the version of the browser. E.g. Chrome 120 has one set of capabilities, and 130 has different, and every 130 has the same capabilities. HErre this might be determined by what hardware is present. Capabilities of the hardware, whether a phone is nearby.

Matthew: GetClientCapabilities doesn't expose even the perrmission that have been granted to browsers. It's whether the client's aware of it as a feature, not whether it'll be successful. RP uses GCC. "Hybrid" permission. You can invoke it in a way that Hybrid would be invoked, and GCC might return true, but the call would fail.

Tim: Only hardware element that would be exposed is if the device doesn't have BT.

Martin: That could solve that reasonably. If it's just about the browse rimplementation, then there's nothign special here, and fingerprinting isn't increased.

Tim: Use case of "is cross device available" comes from Samsung where the hardware isn't available.

Martin: Seems to me that the efforts you've taken make it sound like there's more fingerprinting risk than there really is. If it's nothing more than that, you should say that instead of putting in mitigations.


Tim: Chrome 130 on 2 devices, one with a platform authenticator, and one without, will return different values.

Martin: List those variances, and concentrate on those. For each one, evaluate whether it's worth it.

Jeffrey: For some of those, the browser would say "I have that hardware" because it understands the API call, and then it can fail at runtime.



### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson

Tim: Problem it's solving is that if you don't have a local passkey, have a remote one, they click the passkey button, see a QR code, user bails out. 

Martin: QR code is user-hostile. Why can't the devices sync their passkeys?

Tim: Lots of reasons not to sync to the device.

Martin: Scenario I'm seeing is not particularly compelling. Is there a way for the browser to not support this particular mode?

Tim: Don't have to support any of the conditional modes. Would be added to client capabilities.

Martin: FF would say "you have to go to the full login page to use this".

Tim: Modal flow is minimum bar, then autofill, then this. This is the number-1 problem we have.



Martin: If someone wanted to silently confirm that someone doesn't have a passkey, they'd risk showing the dialog. Which users wouldn't miss. Get the tradeoff.

Tim: In most cases it'll come from the platform and be very intrusive.

Martin: No major problems here. Biggest issue overall is about Related Origins. Greater clarity about which path. Need to talk to John, but there may be a path.

Marcos: Immediate still affects Credential Management, so needs to bounce through WebAppSec.

Tim: And that's L4, not L3.

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola
### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

Xiaocheng: Last time we raised the concern that dev would set the flag on all SWs to be safe. They replied that we don't see that behavior from fetch(keepAlive). It is hypothetical. Second concern is to propose a new worker type. Pushback is that introducing a new worker type is a lot of work. I don't know what to do. Presented with a bunch of bad solutions, and compare what's least bad.

Martin: Sympathize. Worker scope seems like a lot of work, but commensurate to the cost to end users? Maybe spec writer cost should match the cost to users. If pages can run things in the background after page close, that's a big ask.

Xiaocheng: How strong is this point? I'm leaning to closing as satisfied-with-concerns.

Martin: Do we have a more passive-aggressive one? "ambivalent"? 

Jeffrey: I'd be fine with satisfied-with-concerns. [other discussion]

Martin: ambivalent. If we think workers are the right thing, it should be cheaper to create a new kind of worker. New kinds of worklets are easy. New kinds of workers should be too.

Xiaocheng: It's between worklet and worker, although they gave arguments against worklets. API design is hiding the cost of doing this.

Martin: Is there a version of this that works without creating a SharedWorker in a particular mode? e.g. if the page closes and it has outstanding work, through whatever system indicates to the browser that the outstanding work exists, it can keep the worker alive?

Jeffrey: That's what I suggested, and they said that's hard to implement. I don't totally buy it, but I also don't know the implementation well enough to argue this.

Martin: When you register 'pagehide' or "I'm going to run a cleanup task", you've registered an intention to clean up after yourself on the other end. So have registering those events enable extended-lifetime on all future shared workers, or on a particular shared worker url. Register something with the browser that you want to do a cleanup. That action associates state with the new shared worker. Can mutate that over the page's lifetime. Then when the page ends, that state is passed to the shared worker.

Jeffrey: Kinda like that design better. Maybe we should suggest they consider it as an alternative.

Martin: [more discussion]

Jeffrey: Ah, the "I'm going to pass state" flag might turn out to be the same as the proposed "extended lifetime" flag.

Martin + Xiaocheng to continue iterating.

### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman

## Breakout B (America / Europe) - [2025-06-25](https://www.timeanddate.com/worldclock/converter.html?iso=20250625T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Matthew, Sarven, Yves, Jeffrey, Serena

Regrets: Lola, Christian, Hadley

Scribe: Sarven

### [design-reviews#1097: Browser Bound Keys for Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/1097) - @torgo, @yoavweiss, @marcoscaceres

Jeffrey: Skip today

### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @torgo, @lolaodelola

Jeffrey: Skip today

### [tag.w3.org#87: Adjust Dan's term after his election to the AB.](https://github.com/w3ctag/tag.w3.org/pull/87) - @jyasskin, @torgo

Jeffrey: Looks okay?

Yves: Looks okay.

Jeffrey: {Clicks a button}

### [design-reviews#1102: Rethink the TAG's review intake process.](https://github.com/w3ctag/design-reviews/pull/1102) - @jyasskin

Jeffrey: I gave another pass. Basically ready to merge.

Yves: Wondering about missing direct link to WebKit and Mozilla position.

Jeffrey: Every form has in the feedback section there is a multistakeholder part.

Matthew: Difference in description between 2 and 3?

Jeffrey: Right we should not require them to doing HR. There is a question in one of the sections, saying link us to HR that are going on.

Jeffrey: No significant changes from this group but will wait for breakout C.

### [explainer-explainer#25: Say that explainer contents should move into specifications.](https://github.com/w3ctag/explainer-explainer/pull/25) - @jyasskin, @torgo, @matatk

Jeffrey: One proposed change on top of Alice's, and then I think this is ready.

Sarven: Looking good.

Yves: Some people may want to work on Primer instead of folding everything into specification. So, Primer or another related document may be worthwhile to mention.

Sarven: Is "auxilliary" a thing that could cover Primer and related? Nowadays just Notes I think.

Yves: Used to be used might be coming back.

Matthew: Primers are more like introduction to set of related specs.

Jeffrey: Explainers are more for developing features. Do we have a definition for Primers?

Yves: We don't but can look up.

Sarven: Umbrella specifications in Variability in Specifications mentions Primer for example: https://www.w3.org/TR/spec-variability/#umbrella

Sarven: https://www.w3.org/standards/types/ is authoritative types of documents at W3C. But doesn't include Umbrella/Primer etc..

Jeffrey: https://github.com/w3ctag/explainer-explainer/pull/25/files#r2167253161 refers to umbrella and types now. Merging this. Will keep reviews open.


### [explainer-explainer#19: Explainers are an anti-pattern](https://github.com/w3ctag/explainer-explainer/issues/19) - @jyasskin, @torgo

Jeffrey: Needs to wait until we merge previous two PRs and then it could be closed.


### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @matatk, @dandclark

Matthew: Situation we are in is that we can't do any better. Jeffrey's idea was interesting but that would take time to do. The HTML in Canvas group ... one way would be for APA to check fallback and see whether we advise that. Alice is also looking into using libraries angle. Don't know if we hold this up for that.

Jeffrey: HiC what inspired my suggesiton. Maybe we should provide this only for HiC things, e.g., say you went far enough in this direction so move it towards HiC. May be frustratring for some folks. May be more effective to focus on the good thing that isn't quite ready.

Matthew: Not sure how far AT implementers are on this and whether they'll support it. If we want to resolve this quickly, fine by me but could be decoupled from design-review issue. I don't know if we have TAG consensus on that.

Jeffrey: I woudln't say we're unsatisfied with this without hecking that first. Action for me is to draft a comment where we are leaning on satisfied but with HiC direction.

Matthew: I thought you were saying this could be resolved with HiC conditition?

Jeffrey: My understand is the whole structure of this API is to draw this string into canvas with no accessible fallack. The HiC version would be a very different API shape.

Matthew: The options are fallback message works but you have to insist - MUST .. or it odesn't work and we can't suggest that - which would be the unsatisfied.

Jeffrey: When Alice says fallack content isn't fit. I feel we haven't ??? to fix it.

Matthew: There'd be a mismatch with ordering of fallback content. If canvas moves, how do you communicate that someone with assistive tech.

Matthew: I think it is more like it technicically works but it wasn't with the idea to ??? It is not that it is not going to work but it is probably going to miss some movements.

Jeffrey: Related: rearrange the DOM without moving elements. To move two swap elements, remove one and insert the other. Haven't thought of AT but it seems AT would think there is new content. There is work going on to move before function on elements to do that swap without taking that out of the DOM. And AT would have ot make a decision on announcing that to users.

Matthew: Hard ot say for so many ways this could be used. It might sound like the AT user should be told - they read it - it doesn't matter. If it moves lower down they'l discover but if above, they've already read it.

Matthew: AT users typically skip around things. If header moved to behind... this is a rabbithole. UX principles should kick in?

Jeffrey: Website uses the live region to say something moved around. If rearranged the fallback DOM and let the AT decide.

Matthew: The simple case like creating a static picture and the text is in a circle. There is mroe text below with funny colours. You can make fallback content that works for that. But Alice is saying that isn't going ot work. If it is something moving around that complicates things a lot. I think it is because the API could be called any time. The clue here is Canvas based application. Like TVs. Rich stuff.

Jeffrey: Google Docs is a canvas based application.

Jeffrey: One of the drawbacks with fallback content is if it hasn't been drawn yet. Maybe they should be working on that this style of CTM.

Jeffrey: will propose a comment in private brainstorming to use fallback content instead of raw text strings.

Sarven: Any discussion of how quickly the canvas might be moving? How frequently it should be communicated to AT? If there are 100 changes/second, what does that mean?

Matthew: Key thing is equitable user experience. Don't tell about every graphical change, but if it means something, it needs to be communicated. In an accessible game, you'd expect sound or haptics to indicate stuff. Don't need to keep re-describing the scene. Canvas is so general that it's hard to give general advice. Lots-of-updates isn't good for AT users. Hard to keep track of even group chat.

Sarven: Is this something that AT could have an event listener that picks up on it? 

Matthew: Canvas is a bag of pixels, and that's it.

Jeffrey: canvas can tell the AT there is something important. I think your idea with event listener is right ???

Matthew: ... but don't want to do that rapidly or frequently.

Jeffrey: Matthew mentioned we could put a "MUST provide fallback content" but I don't think that's effective.

Matthew: I don't disagree. Work is done on this. If we want positive change to happen we can't say stop it or ask too much. Sometimes we have to say it. If we are going ot say it we encourage the best outcome.

### [design-reviews#1110: windowAudio for getDisplayMedia](https://github.com/w3ctag/design-reviews/issues/1110) - @christianliebel

Jeffrey: Skip today.

### [design-reviews#1105: ScrollIntoViewOptions container attribute](https://github.com/w3ctag/design-reviews/issues/1105) - @zcorpan, @dandclark

Jeffrey: Suggest `satisfied` with a comment that it'd be really nice if the specification included a description of the use case and some example code.

Jeffrey: The explainer and spec has no intro section. Will suggest satisfied but with that request.

### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @torgo, @ylafon

Yves: Need to write a draft comment. Push it for now.


### Ehsan Toreini's Associate nomination

There were no objections by the June 16 deadline expressed in Slack, so Ehsan is appointed as an associate.

## Breakout C (Europe / Asia / Australia) - [2025-06-26](https://www.timeanddate.com/worldclock/converter.html?iso=20250626T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Matthew

Present: Matthew, Ehsan, Marcos, Sarven, Xiaocheng, Christian, Yves, Yoav

Regrets:

Scribe: Marcos

### ~~[web-no-papers#6: Phone numbers](https://github.com/w3ctag/web-no-papers/pull/6) - @martinthomson~~



### [web-no-papers#7: Small changes to terminology](https://github.com/w3ctag/web-no-papers/pull/7) - @marcoscaceres

Marcos: Taking the suggestions from Martin. I think identifiability is already covered in this document.

Marcos: *references last week's phone-home discussion*

Marcos: Would Ehsan agree the document makes a statementa bout identifiability?

Ehsan: Yes; case study of Aadhaar. One example may not be enough, so we could extend it to some other example that has been more successful? There are no 'pretty good' examples, but there are other examples. For me, the root of trust in this document is ambiguous. The core assumption is the ID holder has a core document issueed by the governemnt. We're making sure the person has a DC mapped to this. But what if the physical document is not genuine? How do you make sure the preson having the DC is owning the claim?

Marcos: It's verfiied in the case of enrollment, it's biometrically bound to you at that point.

### ~~[web-no-papers#3: Add some text about email addresses](https://github.com/w3ctag/web-no-papers/pull/3) - @martinthomson~~

### [design-principles#575: Add Criteria for Design Principles to README](https://github.com/w3ctag/design-principles/pull/575) - @csarven

SC: the feedback has been factored in. I think it's ready to be merged. Addressed Martin's feedback and Jeffrey's. Would appriciate further review, but I feel it's ready to go. 

Matthew: we should ask Martin for re-review.

MC: Agree. Gave it quick review. LGTM. 

### [design-reviews#1073: Column wrapping for multicol](https://github.com/w3ctag/design-reviews/issues/1073) - @matatk, @xiaochengh

(Closed)

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Matthew: there were significant a11y concerns. You could un-innert something that was innert, and this seems to be a good thing. Next steps would be for the people participating to sync up, and if this is sufficient. We can't close this just yet - but they heard our feedback and made a good change. There's issues potentially related to aria "role" and this that I'll like to raise with the TAG.  

Matthew: will bump this to next week. 

Xioacheng: will you also raise this with the CSS working group? 

Matthew: no, I need to raise them with the TAG first. 

### [design-reviews#878: confidence reporting for PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @jyasskin, @yoavweiss

Matthew: where are we with this. 

Yoav: Martin and I in agreement that performance measurements leak privacy things, but this prposoal doesn't make things worst. 

Matthew: there seems to be support in the brainstorming issue, so let's go ahead and post that. 

Yoav: Done.

### [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres

Yoav: I think the title is misleading, it's a permissions policy thing that says taht some iframes _shouldn't_ be eligible for autofill.

Marcos: Can we bump? I've not worked on it.  

### [design-reviews#1097: Browser Bound Keys for Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/1097) - @torgo, @yoavweiss, @marcoscaceres

Yoav: I asked some questions regarding the API shape. Not sure if I'm well-versed enough in WebAuthn to know if this is idiomatic in terms of API shape. Generally seems fine, but not sure if the API shape makes sense.

Marcos: Somewhat hesitant to say something here; it requires in-depth knowledge of SPC and BBC. Would advise to take to WebAuthn WG. It came form Web Payments. They will provide more meaningful feedback.

Matthew: Could you draft a comment to that effect and we can see what sort of support we get?

Marcos: Yes; Yoav: works for you?

Yoav: Yes, makes sense what they're trying to do, but the WebAuthn folks will know about the API shape.

### [design-reviews#1102: Rethink the TAG's review intake process.](https://github.com/w3ctag/design-reviews/pull/1102) - @jyasskin
Ready to merge?

Matthew: there are 4 forms being updated. The correspond to 4 categories. We are looking for feedback on this.

### [explainer-explainer#25: Say that explainer contents should move into specifications.](https://github.com/w3ctag/explainer-explainer/pull/25) - @jyasskin, @torgo, @matatk
Ready to merge?

Matthew: Some changes accepted yesterday - attempt to address the 'explainers are an anti-pattern' issue.

Yoav: Very few specs have the explainer content embedded in them. This makes sense but at the same time it's asking folks to do soemthing very different.

Matthew: the idea here was to cover the case where something from the xplainer is going into the spec. Trying to give folks less work to do.

Yoav: Aha. The PR title is a bit misleading. The text is clear. The intro, use cases and examples - do we want them to be in the explainer, or do we want people to move them to the spec? It's ambiguous.

Matthew: I think the intent is just to ensure things are kept up-to-date rather than be totally prescriptive about which.

Marcos: It does mention some sections specifically.

Matthew: Aha, ACK; oops.

Marcos: *makes suggestion about maintenance over time*

Yoav: Question of what is the ideal state? If the intro and use cases move wholesale to the spec, is this good enough? Can novices read this, or is it too scary due to being intermingled with the spec? I'm not sure what the answer is.

Marcos: +1

### Issue triage

* Assigned Yoav to [Expose resource dependency in Resource Timing #1113](https://github.com/w3ctag/design-reviews/issues/1113)

## Plenary Session - None

## Unscheduled Design Reviews

### [design-reviews#945: FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @torgo, @hadleybeeman
### [design-reviews#974: FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974) - @torgo, @hadleybeeman
### [design-reviews#935: FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @torgo, @hadleybeeman
### [design-reviews#803: FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @torgo, @hadleybeeman
### [design-reviews#992: FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @martinthomson, @torgo, @hadleybeeman
### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres
### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

