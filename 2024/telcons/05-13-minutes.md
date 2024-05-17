# TAG Teleconference
#### 13-15 May 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-05-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240513T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion
* [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion

### Breakout B (California / Europe)  - [2024-05-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240513T153000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### Breakout C (California / Australia) - [2024-05-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240513T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [Wide review request for Pointer Events Level 3](https://github.com/w3ctag/design-reviews/issues/941) - @LeaVerou, @matatk
* [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk

### Breakout D (California / Australia) - [2024-05-14](https://www.timeanddate.com/worldclock/converter.html?iso=20240514T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

### Breakout E (Europe / China) - [2024-05-15](https://www.timeanddate.com/worldclock/converter.html?iso=20240515T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo


* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @torgo
* [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @torgo

-----


## Breakout A

Present: Max, Matthew

Regrets: Dan, Yves, Amy

### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

Max: The use cases make sense for me, and are clear. We may have some queestions regarding privacy protection and the security perspective. Some questions raised on the thread, and an offer of joining a meeting. Breakout A would be good for me - not sure if for Lea though.

Matthew: Let's chat internally about having a meeting (and when).

### [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion

Matthew: I think we're happy with this - pending some internal thinking we're doing on the fit of the transformers. It's a living document, so we can give them feedback as we have it. The delta from the group was helpful.

Max: I'm happy with this; agree.

### [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk

*This will come up in Breakout C later.*

Matthew: concern about how users will understand the use of automated translation - will it be obvious that it's automated to users? So they know there are risks. Also don't want to encourage the reapeated use of ML instead of professionally done translations, but understand that is not always possible. (Similar example: captions on videos for accessibility - helpful, but the ideal is always going to be to prodcue captions, rather than have ML work on them, for accuracy, inclusion, and sustainability.)

Max: If the device doesn't have the requisite hardware (e.g. GPU) the UX could be downgraded - important to consider this.

### Stuff to raise at plenary?

Max: We discussed before about GenAI - is there anything TAG can do?

Matthew: +1. Some issues: educating users around managing expectations when using GenAI - how can we indicate that it's being used? Also around content provenance - what approaches are there, and what are the trade-offs? I think we can really help with the awareness-raising here.

Max: It's an interesting topic and I think we should kick off discussion - not sure what the concrete work is, but we should start discussing. Maybe a starting point is to evaluate existing and potential solutions, as Matthew suggested, whether they fit the web architecture.

Max: Another is guidelines/consdierations from the TAG re GenAI.

Matthew: +1; could start by feeding back on the [AI & the Web](https://www.w3.org/reports/ai-web-impact/) document.

## Breakout B

Present: Matthew, Peter, Lea

Regrets: Amy

### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

Peter: Response to Lea's feedback, though unclear as to the answers to Lea's specific questions (on why this isn't just part of `window.open()`). They raised the point that they want gestures to work the same way as if the PiP window was an `<iframe>` - though that doesn't fully explain it to me.

Lea: All of the differences that it has from `window.open()` would actually be useful there - like closing the windows that an opener has spawned. I'd argue for that being the default - we can't do that, but we could make it possible.

Peter: Control over how things close would be good.

Lea: There was discussion on implementability. The [WebKit position](https://github.com/WebKit/standards-positions/issues/41) indicates that PiP is video-specific on iOS. Are there use cases that need more than video? If needing to use feature detection, can't currently use `window.open()` (though that could be added there).

Peter: Is there a use case for making `window.open()` async?

Lea: One reason for not using `window.open()` was the requirement for this to be aysnc. There is a `requestWindow()` method that resolves to a promise. Why is that necessary to be async? So why can't we just improve `window.open()`?

Peter: Because they want to have a permission on it - that's also useful for `window.open()` and was my thinking too.

Matthew: +1 to improving `window.open()`

Lea: All of the extension seem appropriate for `window.open()`

Peter: I get that `window.open()` can't be used for this, but a better `window.open()` (would need to have a new name if async) would be a good idea.

Lea: agree. There were proposals for a better `window.open()` that was async (so, different name) in WHATWG - I linked to them in [my first comment on the issue](https://github.com/w3ctag/design-reviews/issues/798#issuecomment-1587692945).

<blockquote>
Hi folks,
  
We discussed this again during a breakout today.
  
Overall, we see *why* the current `window.open()` doesn’t work for what this API is trying to do, however it appears that *all* of these differences are things that would be useful for `window.open()` as well:
  
- An async API to allow gating behind a permissions prompt
- Feature detection for individual parameters
- Allowing up to one window per top-level traversible
- Ability to create "always on top" windows
- ...
  
We understand that improving `window.open()` is a substantial undertaking, however from an architectural point of view, we cannot justify creating a parallel, more narrowly scoped API for the sole reason of avoiding that work. Instead, we encourage people to work on the [existing effort](https://github.com/whatwg/html/issues/7485) to modernize `window.open()` and ensure it covers these use cases as well.
  
The video-specific use cases appear to be covered already by `video.pictureInPicture()` so designing this as a more general API seems appropriate. It is unfortunate that not every existing platform can implement this API, but it is clear that there are use cases that go beyond video, so we think that as long as feature detection is possible and has good ergonomics, this may be worth doing. 
</blockquote>

### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss


## Breakout C

Present: Tess, Peter, Martin, Matthew

Regrets:

### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

*general discussion of spec; concerns around complexity of @position-try; whether anchor positioning could be more of an extension to absolute positioning; and the use cases for the fixed position aspect (explicit DOM relationships seem preferred - the explainer doesn't elaborate)*

Peter: Feels related to work that went on in SVG to produce links between objects (at least in use case). There's an example of anchoring to two other elements. Maybe useful for SVG?

Martin: @position-try seems like a whole new feature - concern about how it fits with the rest of the platform.

Peter: Agree

Martin: At what point do you try one of the alternatives? Why is there no declarative way of saying what would cause you to try an alternative? Currently seems like the only reason is if overflow is detected. It's possible to generate a situation that will never trigger overflow.

Matthew: [prefers-interaction-side proposal](https://github.com/w3c/csswg-drafts/issues/10244) may provide a reason to try things in a different order? (Either physical preference, or viewport aspect ratio)

Martin: Privacy concerns three. It's better to provide non-exposed preferences to support use cases like this. Better to find ways to adapt content based on screen size (media query @screen) than to have passive fingerprinting.

Matthew: Maybe we should ask Lea (who is participating in CSS) what the status in the WG is.

Peter: Needs Lea's input, but not sure when we can.


Starting some *draft* feedback...

<blockquote>
  This looks like a generally useful feature to have.
  
  Discussions on blink-dev suggest that there might not be WG consensus on the maturity of the specification.  The recently-opened issues also indicate some unresolved questions.
  
  FIXME(grammar): Unclear what the implications of `anchor-name` and `anchor-scope` for authors.
  The algorithm for finding anchors is [complex](https://drafts.csswg.org/css-anchor-position-1/#target) and not exactly intuitive.
  
  `anchor-scope` does not appear in the explainer(s) and does not appear to feature in the algorithm that finds an anchor.
  
  Interactions with shadow DOM are not covered by the explainers (though it is in the specification)
  
  Not clear about `position: fixed` vs `position: absolute` and how this works. e.g. why an author would choose one vs the other. This doesn't appear to be explained in the spec. A related question is why not a new position type vs extending absolute/fixed, e.g. position: anchor(ed). This could also result in renaming the anchoring specific `position-*` properties as `anchor-*` and making it clearer that they only apply in the anchor use-case.
  
  We're concerned about the status of the explainer relative to the Chromium blog post.
  
  The `[@]position-try[-options]` part seems like it might not be baked.  We observe that this produces an alternative set of styling rules that can be activated under specific conditions, but those conditions cannot be specified by authors and are limited to when elements overflow. A better alternative might be to either put all the positioning controls into a `@position` (or `@anchor` or even `@alternative`) rule and just refer to that from the style declaration (which could then be a list of positions, rather than set of properties and then a list of overrides to try), or to have a syntax that keeps the alternatives in the primary delcaration. Some future planning as to other triggers for alternate positions may be warranted as well.
</blockquote>

### [Wide review request for Pointer Events Level 3](https://github.com/w3ctag/design-reviews/issues/941) - @LeaVerou, @matatk

*we didn't get to this one*

### [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk

*we didn't get to this one*

## Breakout D

Present: Martin, Peter

Regrets: Dan

### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

Matthew is not present, so we decided to pass on this one.


## Breakout E

Present: Dan, Martin, Matthew, Amy

Regrets: Max

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

Martin: epsilon value for their privacy reporting is 14 for evennt-level - effectively unlimited. For their aggregated one it's between 1 and 64. 64 is a joke. They are trialing.  Default is 10 which I also think is not meaningful.

Dan: is there any allowance for the browser to make that choice? Like a privacy-focussed browser could dial everything down to the lowest epsilon value.

Martin: 0.001 turns out to not be very useful, a lot of noise. Discussions in patcg have prodcued a design that will allow different browsers and even different users to set differente epsilon values. The designs that we're talking about hide contributions so if you set your epsilon very low then you don't participate but to the outside world you appear to be participating fully

Dan: that's good

Martin: I like it

Dan: the issue you've raised with the default values is more about chrome's decision.. the api itself sounds like a good design

Martin: what the TAG has been asked to review is what google is shipping, their proprietary solution. It's not what's been discussed int he community group. We need to make that clear distinction. There are similarities but they're different things.

Dan: the TAG usuaully doesn't weigh in in... instead of declining to comment we could say you've asked us to review this but instead we're going to review that... giving this feedback about in this differential privacy world allowing for different browsers and users to be able to set their preferences with regard to this epsilon value could be good feedback that they need to hear. If I were using chrome, installation of a privacy preserving extension would then automatically set that value low or zero.

Martin: I'm not sure whether a browser like brave would implement this. That's a discussion I've had with peopel at brave and not got much traction on. Our intent is to implement this but have a different epsiolon value to the one google has. After the last PATCG thing we solved a lot of questions about what a merged design might look like.

Martin: there's another one used in the context of protected audience which is separate from these but similar.. I don't think they've asked us for that

Martin: Microsoft might object to this characterization of multi-implementer interest.  I don't know if they back this proposal.

Dan: we propose to close this one as `resolution: decline`. - let's take it to the plenary.

<blockquote>
You asked us to review three things here (event level attribution measurement, summary attribution measurement, and cross app and web attribution reporting).  We're explicitly declining to review the implementation (ARA) that Chrome proposes to ship as multi-implementer support is not evident here.
  
We expect the [Private Measurement](https://github.com/patcg/private-measurement) API being developed in PATCG will receive multi-implementer interest. Our initial read of that is that its design is broadly reasonable.
</blockquote>

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

Dan: *reviewing status* looks like nothing has happened....

Martin: giving sites ability to deny 3rd party content access to your info and equally denying people access to autofill when it would be desirable.

Martin: i think the assertion that the cardholder name is "necessary" to remain on the merchant origin is questionable at best.

Dan: the payment flows I like are where you go a website and say I want that rake, and it says pay with apple pay or web payment, and then it doesn't ask for any information, it just displays a payment dialog and the information flows through that. You could say in that case my name and address is being provided through the payment api to the merchant. it's happening at that point in the flow

Martin: to the merchant or the payment provider?

Dan: to the merchant as they need to know where to send the rake. Unless it's digital goods in which case they don't need to know.

Martin: this is my fundamental concern. There is an expectation on the part of some actors that they have access to certain information without concretely establishing they have that right. Thye just have an expectation. When words like 'legitimate' and 'necessary' are used, that's not true.

Dan: one of the things we were takling about is that it wasn't well documented the abuse scenarios, the ways in which this could be used to trick the user - information about what the user has agreed to share with whom via autofill. Still a question of do you want to autofill your information being asked at some point? Maybe your mobile browser asks you this - do you want to autofill? Yes, okay for rakes.com. But actually that's being autofilled not to rakes.com but to evilpaymentprovider.com which is being used by rakes.com. Rick's point is that's how ecommerce works. There are payment providers and are ubiquitous on the web so that's less useful feedback.

Martin: more sympathetic to Rick's argument in this case. You're interacting with rakes.com and if rakes.com wants to use a third party service payment provider to accomplish what it wants to accomplish then rakes.com is still ultimately responsible for what happens in that context - compliance with data protection and security and other consequences. Ultimately from the user perspective you're giving this information to rakes.com. How rakes.com wants to manage all of that is then their business. I don't see there's much business in having minute control over the number of the card going to the third party, and the name is going to the merchant and the third party... I don't think is really something that people...

Dan: that's fine, agree. The worry we expressed was in the context of autofill this could be used to trick the user if there was malicious content being embedded. If there was a malicious ad could it be used to trick the user? Autofill could just spew your name and phone number into a random form, when maybe that wasn't the intention of the first party site. What are the controls that mitigate against that? That was missing from the proposal.

Martin: would this be something for permissions policy? As a top level site the default is that autofill doesn't happen in frames. BUt you can set a permission policy that says this site gets autofill that' would be a fine solution. Is that not what they're saying?

Dan: they could have updated it.. last updated 10 months ago

Martin: it says it's a policy control feature which is consistent with my interpretation

Dan: might have been prompted by our feedback, we had a good conversation at tpac last year but no update in our issue

Martin: if they are using permision policy.. I think it's a good thing in total. What I thought this work would run into was the potential for a website to deny access to autofill in certain circumstances where they thought it was not appropriate. if I wanted to build a website (like many do, despite it being bad) that blocked use of a password manager for password entry, I'd accept it from an iframe but deny the cross origin iframe access to autofill capabilities. I suspect they already have addressed that in the whole thing by there being a direct user override for any form field. If they don't that's a problem.

<blockquote>
Hi @rbyers - we were just briefly reviewing status on this.  First of all, has there been any update that we should be aware of?  Should we be re-reviewing at this point?
</blockquote>


### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

Martin: protected audience has a bug - with fenced frames - https://github.com/WICG/turtledove/issues/990

Martin: *describes a threat vector of bad actor using a capcha style UI to get someone to decribe contents of a fenced frame (contents that the site should not be able to learn)*

Martin: Any secret information is released if someone clicks on it.. and there are no controls over how big a fenced frame is or the content that it shows...

Dan: [explainer and spec changes came in last month](https://github.com/w3ctag/design-reviews/issues/838#issuecomment-2059474413)

Martin: macros gives the outside site the ability to pass variables into the URL...

Martin: suggest that we could decline and refer to [Protected Audience](https://github.com/w3ctag/design-reviews/issues/723)

Matthew: Say we decline this but we are expecting consensus in the community with respect to attriibution - wouldn't we want to see something like this with respect to attribution? it would improve the situation slightly when it comes to privacy...

Martin: i don't see that this works for any scenario unless you click on the fenced frame... navigation causes information to flow between web sites...

*discussion about need for fenced frames*

Martin: there are things on the platform ... non-cross-origin images (not marked CORS) - if you have one of those on the web site you don't get to know what the pictures are that were drawn on the screen... once we start talking about more and more capabilities it gets more difficult.  If you show an ad on a page and the ad is replaced with nothing or a white square then the page doesn't get to know about that. It's necessary for some a11y scenarios...

<blockquote>

Hi @blu25 - we are just reviewing it today.  We appreciate you taking the time to collate the information you've provided. However, it's difficult for us to parse the list - which is a lot of links to PRs where you need a lot of context to understand how they fit in, context that we lack.  This is one reason we ask for explainers with reviews - which provide that context.
  
I'd also like to point out that we've returned a [negative review on Protected Audience](https://github.com/w3ctag/design-reviews/issues/723#issuecomment-1944367149). So if there is a hard dependency now between this work and Protected Audience then it's unlikely that this will get a positive review from TAG.
  
Even so, we strongly recommend that you write an **explainer** which talks through this proposal, starting from **user needs** - as documented in our [explainer guide](https://tag.w3.org/explainers/).
</blockquote>

### [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @torgo

### [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @torgo


## Plenary Session

Present: Matthew, Peter, Martin, Max, Dan

Regrets: Amy (belated)

### [Charter review FedID and digital credentials](https://github.com/w3c/strategy/issues/450)

Martin: Potential new finding .. not having to choose is a luxury... proliferation of alternative formats. E.g. identity people are providing a "range of formats" (unspecified)... that has consequences for users...  Lots more examples of when 2 groups in a standard go off and deliver 2 separate things...  e.g. video format question ... 

*discussion on WebRTC as one example of this*

Martin: in WebRTC there was a long debate of vp8 vs. h264 as the video codec of choice. the resolution was that some small group would support both and everyone else would talk to those people. that has poor negative effects on those who have to do both. but it turned out ok. a patterm - when you have 2 options, someone has to do both... 

... in identity speace there are multiple identity [verified id] document formats ... they have refused to decide on what the format is and letting everyone else to decide. what's likely to happen is that web sites will be forced to support multiple formats... people don't have a choice: they get their id in a particular format from their government.  so web sites will choose "i will use this format since most people coming to my web site are from xx government" and therefore exclude others.. that's not a good outcome, and doesn't fit with "one web".

... the right thing to do is to standardize and pick a format ... maybe the web isn't important enough to force a resolution but it's worth saying.

Dan: *use case of showing up at a border and being able to aseert one or the other nationality, as a dual national, rather than having the web site I'm using know about both idneities*

Martin: that's not how it works today.

Peter: or... i am of legal age to buy alchohol. ..

Peter: how do you proove the negative... you're in a juridstiction where you've lost the legal right to alchohol. How do you fail to assert you have the right to alchohol.

Martin: the documentation -- there is discussion of selective disclosure - but there are secondary cobsequences. Often selective disclosure comes with linkability characteristics. Probably on the web we don't want any linkability...  One case is linkability across presentations - e.g. crossing the border - linking that to the next time that you present in that same situation. 2) linking it in a different context.  May be a desirable property... in the "can buy alchohol" - if i go to multiple stores, those institutions being able to link to one person is undesirable. 3) linking it back to the authority that says "you're eligible to buy alchohol"... 

Peter: in the US there are laws about certain kinds of alergy mecicine... 

Martin: that's a right limiting thing - and all of these 0 knowledge systems have right limiting characteristics.

Peter: 2 audiences  one is the standards groups - the other audience is all the legislation about digital identities...  I hope we're early enough to influence those conversations... 

Matthew: our friends in the UN could help us with that awareness raising...  Also some work that that the APA did on use cases for identity... e.g. eligible to park in a specific space. 

Martin: might be reasonable for someone to scan a QR code... 

Peter: i want to be able to run a web server that holds my medical records... and allow selective access to my records... but I want accountability if access is abused

*discussion on what to do with targeted feedback on identity*

Peter: it can be helpful to have a document - to help influence legislation, etc... a finding could be useful. Something that other people can cite and reference...

Matthew: I think both discussions are super important... 

Peter: could be a blog post...

### GenAI & C2PA

*discussion on what TAG can do to on this topic*

*discussion of whether a C2PA task force could be appropriate*

Martin: there's a number of concurrent efforts that seek to establish provenance or authenticity... Also there are generative AI watermarking techniques ... my view is that the AI watermarking stuff is flawed.  it's an escalation war. You tag content in a way and someone can spoof that tag...   What C2PA does is try to do the inverse "this content comes from an authentic source" - a camera can sign the photos that come out of that camera - and you can have reasonable assurance. where C2PA fails is being able to preserve. 

Martin: I think it's impossible... it's a cat and mouse game...

Peter: signing bits off the sensor... 

Peter: if you have a chip on the camera that has a private key... if I use a guaranteed version of photoshop... 

Martin: the only assertion you can make is that this came from an unmodified sensor...

Some links:

* https://www.starlinglab.org/78days/
* https://www.bbc.com/rd/blog/2024-03-c2pa-verification-news-journalism-credentials
* https://investigation.rollingstone.com/dj-photo-war-crimes-bosnia/
* https://dispatch.starlinglab.org/p/authenticated-attributes-an-alternative?triedRedirect=true
* https://www.hackerfactor.com/blog/index.php?/archives/1010-C2PAs-Butterfly-Effect.html
* https://www.hackerfactor.com/blog/index.php?/archives/1013-C2PAs-Worst-Case-Scenario.html
* https://www.hackerfactor.com/blog/index.php?/archives/1019-Save-The-Date.html

Martin: i'm not sure if that will work for the web...   BBC might have journalistic mechanisms .... but not sure it belongs in the browser.

Peter: trusted CAs... being to authenticate ...

Matthhew: web of trust... 

### [This comment](https://github.com/w3ctag/design-reviews/issues/723#issuecomment-2100898391)

Martin: i suggest no response...

### Breakout Rollup

#### Breakout A

Local peer-to-peer - call time?

#### Breakout B

#### Breakout C

Reviewing and hopefully posting CSS Anchor Positioning feedback

#### Breakout D

#### Breakout E

### Issue Triage
