# TAG Minutes - week of 31 March 2025

## Agendas

### Breakout A (California / Europe) - [2025-03-31](https://www.timeanddate.com/worldclock/converter.html?iso=20250331T163000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

* [design-reviews#1051: (brand new ✨) Web Install API](https://github.com/w3ctag/design-reviews/issues/1051) - @torgo
* [design-reviews#1030: [HTML] 2D canvas floating point support](https://github.com/w3ctag/design-reviews/issues/1030) - @zcorpan, @matatk, @xiaochengh
* [design-reviews#1034: Container Timing API](https://github.com/w3ctag/design-reviews/issues/1034) - @torgo, @hadleybeeman
* [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk
* [design-reviews#468: Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @jyasskin, @matatk, @hadleybeeman
* [design-reviews#1017: ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk
* [design-reviews#1050: Permissions Policy reports for iframes](https://github.com/w3ctag/design-reviews/issues/1050) - @torgo, @hadleybeeman
* [design-reviews#878: systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @hadleybeeman

### Breakout B (California / Australia) - [2025-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20250401T220000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

* [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres
* [design-reviews#1071: Private Proof API](https://github.com/w3ctag/design-reviews/issues/1071) - @martinthomson
* [design-reviews#896: Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @jyasskin, @marcoscaceres
* [design-reviews#1061: CSS View Transitions - Nested View Transition Groups](https://github.com/w3ctag/design-reviews/issues/1061) - @xiaochengh
* [design-reviews#842: Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson

### Breakout C (Europe / China) - [2025-04-02](https://www.timeanddate.com/worldclock/converter.html?iso=20250402T070000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

* [ethical-web-principles#143: Clarify informing a broader scope of technical and community reports](https://github.com/w3ctag/ethical-web-principles/pull/143) - @csarven, @torgo
* [ethical-web-principles#140: 2.12 People should be able to choose how they engage with the web](https://github.com/w3ctag/ethical-web-principles/issues/140) - @torgo, @hadleybeeman
* [design-reviews#1047: Early Design Review: Related Website Partition API](https://github.com/w3ctag/design-reviews/issues/1047) - @torgo, @csarven, @hadleybeeman, @lolaodelola
* [design-reviews#1040: Navigation API deferred commit](https://github.com/w3ctag/design-reviews/issues/1040) - @martinthomson, @torgo, @matatk
* [design-reviews#1020: CSP report-hash keyword](https://github.com/w3ctag/design-reviews/issues/1020) - @martinthomson, @zcorpan, @marcoscaceres
* [design-reviews#1063: WebGPU Compatibility Mode](https://github.com/w3ctag/design-reviews/issues/1063) - @martinthomson, @torgo, @matatk
* [carousels](https://github.com/w3ctag/design-reviews/issues/1037) etc... 
* [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman

### Plenary Session - [2025-04-03](https://www.timeanddate.com/worldclock/converter.html?iso=20250403T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

* Associates Decision
* [design-principles#564: Add guidance for layout-forcing apis](https://github.com/w3ctag/design-principles/pull/564) - @xiaochengh
* [design-reviews#1043: CSS.highlights.highlightsFromPoint API](https://github.com/w3ctag/design-reviews/issues/1043) - @torgo, @xiaochengh
* [design-reviews#525: Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @marcoscaceres, @lolaodelola
* [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Minutes

### Breakout A

Present: Dan, Jeffrey, Matthew, Yoav, Yves

#### [design-reviews#1051: (brand new ✨) Web Install API](https://github.com/w3ctag/design-reviews/issues/1051) - @torgo

*dan summarizes*

Jeffrey: I think we should allow browsers to experiment in this area without damaging other browsers... that's where the declarative comment came from...  I haven't gone through the update yet. Want to find them a way forward.

Dan: new concept they have introduced... active tab..

Jeffrey: MS have done more to explore Install... 

*we agree to continue to review and come back to it next week*

#### [design-reviews#1030: [HTML] 2D canvas floating point support](https://github.com/w3ctag/design-reviews/issues/1030) - @zcorpan, @matatk, @xiaochengh

Matthew: I left a comment... looked at it from a perspective of consistency with other things... whether the explainer seems to be missing anything... 

... definitley some things that sound reasonable. But one thing : a separate issue thread that I've linked to...  They've explained why this format of encoding fits the hardware and matches WebGPU... They have talked about the way they have named stuff.   That's a summary of my comment. If we do have someone who is expert, then fine... 

Jeffrey: I agree it looks fine and I think Anne's concerns have been solved on the other threads.

*we agree to set to **proposed closed** and close at the plenary.*

#### [design-reviews#1034: Container Timing API](https://github.com/w3ctag/design-reviews/issues/1034) - @torgo, @hadleybeeman

Yoav: this is an extension of element timing to cover entire containers rather than specific elements... element timing covers only images and paragraph. This is a community driven effort to improve on that.

... discussed in the webperf working group... will probably be folded into the element timing spec which is in that wg. Driven by Bloomberg and Igalia.

Dan: have we done a review on element timing.

Yoav: it shipped in Chromium in 2019...

Dan: any privacy / security?

Yoav: large parts of this are polyfillable with element timing... it did have a polyfill at an earlier stage... Nothing seems particularly novel.  Would need to collect all the element timings from all the elements inside the container... At the same time it would be worth while to ask that question on the issue...

Dan: [previous tag review](https://github.com/w3ctag/design-reviews/issues/326) - we were satisfied.

Jeffrey: sounds right to me....

Yoav: moz have been somewhat supportive but no official position...

Dan: *leaves [comment](https://github.com/w3ctag/design-reviews/issues/1034#issuecomment-2766825476* Maybe we can close this at the plenary.

#### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk

Matthew: definitely the use case is a good one... I will have more of a comment by breakout C.

Jeffrey: this is an interesting one.  Martin and Tess don't like the way OpenUI are proposing this... The issue is that hover on a touchscreen is really difficult ... originally they proposed that you would express interest in a platform-defined way. They tried to provide that direction... long-press... however long-press already shows a context menu / preview (on some platforms)... and Tess is unhappy with changing that behaviour (in Safari)... We could help ...  They landed on normatively requiring long-press... Whereas we could say "it's a way"... 

Matthew: it does seem unusual to be that proscriptve about UI in a spec...

Jeffrey: we say some similar things elsewhere... but e.g. VR headsets might need an entirely different UI for "expressing inetrest"

Yoav: one more thing about this general pattern... pattern that devs have already been implementing... some conflict there with intention to prefetch... looking at speculation rules... and this pattern. They are not 100% at odds but some conflict. This pattern encourages people to engage with links without necessarily visiting. 

Jeffrey: that's a really good point that we should include.. Maybe interest target should turn off prefetching... or developers could specify how to prefetch the result...

**bump to breakout C**

#### [design-reviews#468: Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @jyasskin, @matatk, @hadleybeeman

Matthe: Marcos suggested "overcome by events"... we could go with that... If we were going to do this... it would be a good idea to "focus" on specific areas or divide between us. But there has to be some sort of goal... There's a lot of new stuff coming out of OpenUI... is there guidance we should provide?   

Jeffrey: I wouldn't suggest  "overcome by events" ... because things haven't changed... we just haven't had time to do it...  Maybe ask an a11y groupt to look at it and then we could promote into a finding?

Matthew: lots of stuff from OpenUI has come through... we don't want to invent work that doesn't need to be done. clear scope of what is needed would be good.

Jeffrey: I feel like the most likely problems are in the stuff that hasn't been touched recently... probably there are "dusty corners".. we need to look at a lot of things... not sure it's worth it.

Dan: any design principle?

Jeffrey: we could ask APA if they think there is a principle here?

Matthew: it's worth asking... the specific people in APA that do hands-on stuff in this area... I'm not sure how easy it would be to coordinate a more systematic review across html...

Dan: *suggests changing the focus of the discussion to the design principles ... maybe opening up a new issue in that repo and closing this issue*

Matthew: we do have access to a lot of academic research in this area... so there might be some stuff we can get from that to.

**Action: Matthew to ping folks in APA.**

#### [design-reviews#1017: ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk

Matthew: no new comments on the issue... but we talked about this. ..

**we move it to proposed close and we have a draft closing comment we will revisit at the plenary and hopefully close**

#### [design-reviews#1050: Permissions Policy reports for iframes](https://github.com/w3ctag/design-reviews/issues/1050) - @torgo, @hadleybeeman

Yoav: I looked at it... purpose is to warn ... permission polciies that are wrong... this is when the embedder is trying to delegate a permission they don't have access to... I haven't dug depeer than that.

**revisit in C or in the plenary**

#### [design-reviews#878: systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @hadleybeeman

Yoav: this is an effort by MS folks to expose a bimodal dimension on navigation timing... but make it privacy-preserving. They have presented at the webperf working group. They are exposing a fuzzy bit on whether the system entropy is high or low.. and as a result of that they can disect the relevant metrics... without knowing for any specific navigation, the entropy level.

Jeffrey: I suggested the fuzzy thing and focusing on the privacy implication... and they fixed the name.  It seems like they have gone in the right direction.

**yoav and jeffrey assigned and they will propose a closing comment with 'satisfied'**

#### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman

Jeffrey: they... haven't done it perfectly... they haven't got interest from other implementers... they've sketched out how it will work. How it will integrate with payment request.. They are pushing in the right direction. This is something the browsers will disagree on... So I'd like non-browser people to think about how we push payments forward... how do we pull in more stakeholders? Figure out if this is a good direction...

Yoav: a super-interesting question that I'd love to contribute to... Payment link tries to decouple the browser API.. gives apps a way to register for push payments... then gives the site a way to tell the browser preferences... at the same time I have some issues with the current chromium implementation... right now there can only be a single hint.

### Breakout B 

Present: Martin, DanC, Marcos, Jeffrey

#### [design-reviews#1017: ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk

Martin: I think the new draft is great. Let's give Torgo one more chance to review, and post tomorrow.

[General agreement]


#### [design-reviews#896: Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @jyasskin, @marcoscaceres

See proposed comment at https://github.com/w3ctag/meetings/blob/gh-pages/2025/03-24-minutes.md#breakout-b. Jeffrey's pre-meeting proposal:

Jeffrey: I think this could be `satisfied` because they're using the partitioning everyone's converging toward.

Martin: Partitioning isn't converged yet, which is why they need to refer to the common concepts.

Marcos: Testing?

Jeffrey: Something in the I2S thread about difficulty with tests.

Martin: Should be straightforward.

Dan: Tab's saying it's flaky because it's not synchronous.

Martin: That's an implementation issue, which shouldn't concern us.

Jeffrey: Mention tests in the comment?

Marcos: CSSWG hasn't been great about adding WPTs with spec wording.


`satisfied` with:

<blockquote>

We're excited that this is moving forward and that the specification has moved into https://drafts.csswg.org/selectors-4/#visited-privacy.

We encourage the CSSWG to refer to the same partitioning concepts we are using for other site-level state, instead of redefining the partition key in the Selectors spec. The three-level key does match what we understand to be used elsewhere, but you should cite either https://storage.spec.whatwg.org/#storage-keys or https://privacycg.github.io/storage-partitioning/.
  
~~We also would like to ensure that proper web platform tests are landed for the corresponding specification changes.~~ (Marcos commented about tests.)

</blockquote>

#### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres

Marcos: Primary issue is the naming.

Martin: Many things are bundled in this design review. 1) The capability is already available because the site can download the model itself. This sets up websites to rely on UA processing. Given that these are expensive and unwieldy, the UA or user has to find the compute to do that. Not going to happen on the couple-year-old phone I have. Then user has to pay for cloud compute. 

Jeffrey: Then UA should provide the cloud compute?

Martin: Assumption that user provides it, and UA might do it for them. In a few years, this might be available locally everywhere.

Marcos: Could treat it like camera, where some hardware just doesn't have it.

Martin: Can't provide a camera in the cloud if you're building the website. But in this case, the website could do the compute pretty easily if they think it's important. There are some advantages to doing it locally. But the website has the text, so the privacy concern doesn't exist. And performance might not. Only helps people with high-end machines. Massively premature.

Marcos: Use case could be secure email/messaging. Do a summary of mail messages.

Martin: Good example of something the OS can provide on new hardware.

Jeffrey: Advice might be to find a way to ensure the site provides server-side capability even if it defaults to using client-side feature.

Martin: That assumes it's ready. Not enough people have the client-side capability.

Marcos: Think about whether you can do it with WebGPU or with WebML.

Jeffrey: Any idea of what fraction of users need a capability before we provide it?

Martin: It's a judgement call. I don't see people buying new devices at a high enough rate.

Martin: Privacy aspects. Not just "does the text leave the device". That's silly because site has the text and could just send it to the server. Server can do the copmutation faster than most client devices.

Martin: P&S Considerations section: 1) there are 3 types of models available here. Some computation testing the availability of models on end device. Depending on circumstances, you could get 3-6.5 bits of fingerprinting entropy. Depending on model availability + downloadability. That seems like a lot for a feature like this.

DanC: If I know properties of models, I could prompt them to distinguish models.

Martin: Characteristics of model are highly correlated with other things you can already determine.

Jeffrey: Any sense of how many bits this is worth?

Martin: I'd say 0. Since website can already do this, either on the server or by sending a WebGPU or WebNN program.


Jeffrey: Model Cards: website might want to know if its model has been trained on copyrighted material, or if it's been de-biased in certain ways.

Martin: Which is another reason for the site to source the models itself.

Jeffrey: And does this work well enough to ship? "It's called AI while it doesn't work yet, and then it gets a more specific name." Translation API is more promising.

Martin: I think they've gotten rid of the naming problem.

Jeffrey: Domenic was asking about tests: Different models aren't expected to produce identical output.

Martin: Need a model to test the model.

Jeffrey: Ew.

Martin: Naming problem is fixed! They made `window.Summarizer` and `window.Writer`, which is another naming problem.  "Writer" isn't exactly unique or novel.
Can we ask that they rename each with a prefix, like "BullshitSummarizer"? [[1]](https://link.springer.com/article/10.1007/s10676-024-09775-5)

Martin: On testing: At least the test website will be responsible for sourcing the model it uses to evaluate summaries.

Jeffrey: That's enough questions. So we invite Domenic to a meeting the week of April 21 for a conversation. Would like to consider Translation API along with this one.

On translation...

Jeffrey: more established problem set, smaller and more efficient models, can be downloaded to more devices.

Marcos: Same thing happens there; Apple can source their own

Jeffrey: existence proof that models can be made that work well and run on lots of devices.

Martin: Mozilla also has translation models.  Lots of language, 10s of Mb each.

Jeffrey: LLMs tend to be gigabytes each.

Martin: Mozilla will propose to only provide one direction. Text -> preferred language. If lots of people are trying to communicate, each one is responsible for translating other people's speech to their own language, but you don't need the full matrix. 

Marcos: If I speak multiple languages?

Martin: Then you pick one as the preferred target language. Web page presents some content in its language, and then asks the browser to translate it.

Jeffrey: Seems even declarative.

#### [design-reviews#1071: Private Proof API](https://github.com/w3ctag/design-reviews/issues/1071) - @martinthomson

Martin: Assuming familiarity with Private State Tokens: site decides you're trustworthy, and you can take those to another website, which can consume the tokens. This is basically the same, but the decision the website takes about trust isn't a decision. Instead, when it issues the original tokens, it saves the current time. Then when it comes back, the website can ask the browser if the saved time is prior to a specified time. Doesn't know where it created the signal or any other information other than the browser having been seen at least X minutes ago. If you're running an anti-fraud system, you rely on a long history of engagement. If you have a long history, you're more trustworthy. Can use this as a sorting function between likely-safe and unknown visitors.

Martin: This removes some of the problems from the Private State Token solution, because it passes arbitrary information. 1 bit could mean anything, like "lives in particular geography". Apple system said "person has bought an Apple device". Problem with PST is the user doesn't know what the signal is. In Private Proof, you know what the signal is. Has the other problems of PSTs: you have to limit the number of entities that can use the API, or else it becomes a great fingerprint. Needs to be a system of accountability, and that system isn't clear. Proponents suggest entropy limits == cap on number of sites that can use it in a context. Works, but encourages sites to use services with the oldest user accounts, which creates a centralizing incumbency advantage. Can't rely on a diversity of antifraud providers. They don't have a solution yet. Probably on balance it's ok if those problems can be worked through.

Jeffrey: Sounds like a set of questions for the proponents rather than a conclusion yet.

Martin to draft a comment with questions, and we'll run it by the rest of the TAG.

Lots of questions: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/131#issuecomment-2770984939

#### [design-reviews#842: Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson

Martin: This has come up again because there have been new developments. There's already a comment https://github.com/w3ctag/design-reviews/issues/842#issuecomment-1989631915. Someone's proposing a dependency.

Jeffrey: Webview

Martin: Controlled Frame, which is a terrible use case. Sets up a website as a web browser, which all the access to the contents of the webview that a native app has. Don't want to stamp out alternative web browsers. This isn't the way to do it. I didn't see any reason to revise the comments we made about IWAs in the past. "Find another way"

Marcos: Seems like a bad way to make apps when it sidesteps the privacy and security and permission model of the web.

Martin: Don't want to suggest "oppose" without more discussion.

Jeffrey: Not as opposed as others.  With store-like review capabilities, this is a way to do native-ish apps with web technology.  So maybe outside of the TAG remit as not being part of the web.  Seems plausible, if not "the" web.

Marcos: End up with two different models for achieving these goals.  We have web-friendly alternatives to some of the use cases.  Similar to what miniapps are trying to do, which sidesteps all the stuff that we built to make the web safe.

Jeffrey:  Should get a full list of things that are being proposed for IWAs so that we can get a better view.

Marcos: ?

Jeffrey: We've a set of device APIs that are weaker than this and only Chrome has decided they can be shipped safely to the web.  These capabilities are not even safe for Chrome, but enterprises want them.  One is this case of letting sites record all screens and get a promise that it is all the screens.  This is super-sketchy, spy on employees API.  Enterprises use native apps.  Putting in an IWA, we can at least notify people that they are being spied on.  There is a terrible thing in native apps, but we might shift the ecosystem a tiny bit.  This is how we use browsers to improve the world a little bit.

Marcos: Bad actors might know about this transparency, so choose to stick with native instead.  It comes back to OS developers to not enable spying.

Jeffrey: The OS developers have just allowed this.

Martin: Partly by accident and partly by design. Windows just allowed installing an app, which could have root access. Windows has evolved without just breaking this, since you can't break all existing apps.

Jeffrey: The TAG could say that this isn't part of the Web.

Martin: That's why I suggest `oppose`; we should say "go off and do this, but don't call it part of the Web". If ChromeOS ecosystem wants to build this for apps on Chromebooks, go ahead.

Jeffrey: So the TAG could say "don't send us reviews for IWA APIs", which the blink process could cleanly adopt.

Leaving open who should draft this comment.

### Breakout C 

Present: Matthew, Dan, Marcos, Martin, Dan, Yves, Sarven, Lola

#### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk (bumped from A)

Matthew: I wrote a sort of proposed comment... I think the use case is a good one to be trying to solve.. some issues, particularly this changes long established behaviour. On Monday it sounded like that we (or someone) had asked them to be more specific. and actually now we're asking them to be less specific... A couple of other things - one was a question on the way focus order works... The other is: it adds a value to the CSS interactivity property which we just had a concern about in #1037. But still it's predicated on this thing that we asked people not to ship.

Dan: Dependency?

Matthew: it has a dependency on a value on the CSS interactivity property - in 1037 we asked them to not ship so this has similar issues. Jeffrey has also give some feedback.

Marcos: It seems to replicate popover... I don't agree that shifting this from developers to UAs is something that's going to work well.

Matthew: webkit supported popover=hint but not the specific interest target because it overrides the UI for long press. Also: would we want to chnage prefetch rules?

Martin: in an application if you tap on something that isn't a link then everything's fine... it's just a matter of building app such that there aren't multiple layers of interaction... This is one ... where we (mozilla) are getting pressure from Google. The upshot is still the same. There is no consensus on the feature. It requires uninform acceptance to change the bounderies of standardization. It has long been the case that long-press is UA behaviour, not something in the spec... Unless Safari willingly concedes that it's subject to standardization then I don't see this going anywhere... 

Marcos: Martin raises an interesting point around long-press.. Trying to figure out why we haven't standardized the long press...

Martin: well we had context menu for right click...

Dan: in some web applications, context menu is over-ridden.

Martin: e.g. in Google docs...

Dan: just noting that there are examples of a default behaviour and an ability to override the behaviour.

Matthew: I'm sympathetic to this use case ... especially for people who are browsing on mobile this could save users time... E.g. checking the status on a github issue...

Martin: My view is that in this example this is something GitHub could provide you. On sarari a long press already gives you a preview of the page that's at the other end.

Matthew: for me with a vsion impairment that preview isn't of use to me... So I'm sympathetic to the bounderies but also enthusiastic for the use case.

Matthew: the popup is useful because the key info is there .. the preview isn't useful because it's too small to see...

Martin: isn't that an implementation problem? The stylesheet of the 

Dan: so it would be an extension of responsibe design... 

Marcos: a design choice by GitHub (e.g.) ... other option: if you can identify a window... media query - this happens to be a preview - you could 

Dan: so a new media query type -- 

Martin: of type `preview` and adapt the content accordingly.

Matthew: one of the pitfalls .. if you didn't have the ability to reliably establish you were in a preview you would load the important info first.. rather than limit it to the contents of what you would put in the popover...  So the idea of having a special, reliable and simple way of loading as a preview here... I like it bcause it avoids that problem. I also like it because it could be generalized to other sorts of preview cards...

Dan: where does the info you're interested in come from?

Marcos: could be in the page, could be that you need to load it...

Matthew: presumably ... you get told the page is being loaded in a preview ... could do the same thing on desktop... I'm sure that involves more transfer of data... and on mobile transfering less data would be desirable.

Marcos: you could do a preview source if that was a concern... 

Matthew: we could say "interest target and interest target source"...

Marcos: there are other ways of solving this problem... for example considering using a media query, loading an alternative document, etc... 

Martin: if your list contains everything you need to display the preview fine, but in some cases it doesn't... if the goal is to use the preview as a stepping stone it makes sense to load and prepare to render the page... so having it be a different type of content... might be a bad thing. The savings is... having a bootstrap but doesn't cost a bunch extra until we load it...

Matthew: this is about avoiding the need to load the other page... I think I will rephrase the draft comment.

#### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman (timebox)

Martin: i want nothing more to do with it...

Dan: Payments is a highly regulated space... 

Yves: I know it's on the radar of the web payment working group... they should decide...

Marcos: from a security pov, it's problematic to pass links ... silently to wallet apps.

Sarven: I felt that we adaquately covered it in a technical and broader level as to concerns... not a particular thing we need to highlight. They mentioned that the URI schemes - only focusing on non-http schemes... I get that they want this on the web platform. but it's handing it off to somethong off the web.

Martin: payment request handler ... failed ... as a web site you could register to be a payment processor. they are trying to model this as a way to get into a payment request.

Marcos: where they could just use payment request to do the same thing.  This is trying to side-step a problem that needs to be dealt with in a different way.

Dan: can we close this issue ...?

Sarven: Is there a set of URI schemes that browser vendors are committing to implement?

Marcos: they fall in the remit of the web platform... Not about URI schemes.

Sarven: but the design is that they are only covering non-http. Are all browser vendors agreeing to acknowledge when they discover a payment link relations.

Martin: entirely proprietary... Chrome would have a list of schemes that it understands ... even some https URIs... a bunch would be thrown straight into apps...

Sarven: a question we could pose around that. until there's that agreement then it's going to create more fragmentation... 

Marcos: no way of checking which URI schemes are supported... so you'd have to check... They are settled on a URI scheme solution which is not the right approach...

Sarven: My concern is that majority of the web is using http payment pages... so the design is not echoing the most common use of payment on the web...  So first and foremost it should be most widely deployed...

Marcos: the use cases ... 

Sarven: the designs they are playing with... e.g. scanning a qr code...

Marcos: the problem is ... 

Dan: We should push this to the web payments working group and say that we can't really provide input usefully.  The working group can and should.  Would also like to hear the different perspective from Yoav, who isn't here.

**ACTION: Dan to draft something...**

#### [ethical-web-principles#143: Clarify informing a broader scope of technical and community reports](https://github.com/w3ctag/ethical-web-principles/pull/143) - @csarven, @torgo

Skipped.

#### [ethical-web-principles#140: 2.12 People should be able to choose how they engage with the web](https://github.com/w3ctag/ethical-web-principles/issues/140) - @torgo, @hadleybeeman

Skipped.

#### [design-reviews#1047: Early Design Review: Related Website Partition API](https://github.com/w3ctag/design-reviews/issues/1047) - @torgo, @csarven, @hadleybeeman, @lolaodelola

Lola: unsure how it relates to first party sets (related websites)... Where removing the third party relationship between domains... it makes sense for amazon ... but for the user does that make sense... 

Dan: seems like first party sets keep coming back ... 

Lola: as a user you're in site a... that lets you go to site b for customer service... so you want to maintain the support connection.. shouldn't be any accepting permissions or starting a new chat... you could just ask the user ... 

Martin: ... navigation tracking ...

Lola: they offer alternatives... and make those seem bad...

Sarven: question / concern: ti sounds like like there's a concern around phishing attacks... if you can fool the user  it looks like site A but they are really on site B. And they've granted information from the actual authoritative site... E.g. amazon.com and amazon.co.uk ... if the fake one is not actually owned but looks visually similar....

Lola: there is a "set of sites" and ownership of those sites belong

Dan: is it a bi-directional thing?

Martin: no it's on github...  As a procedural note - we've agree to decline extentions to things that we don't think are good. We should therefore decline to review.

Proposed:
> We reviewed RWS, twice ([link](https://github.com/w3ctag/design-reviews/blob/main/reviews/first_party_sets_feedback.md)).  We were not satisfied with that design. We will decline to review this as long as it does not address the issues we raised earlier.
Also: Can we flip our resolution on RWS to "resolution: object" to reflect the strength of our position.

**ACTION: Dan to review and see if I concur that it should be declined.**

#### [design-reviews#1040: Navigation API deferred commit](https://github.com/w3ctag/design-reviews/issues/1040) - @martinthomson, @torgo, @matatk

Matthew: explainer has been updated...

**ACTION: re-review with the updated explainer.**

#### [design-reviews#1020: CSP report-hash keyword](https://github.com/w3ctag/design-reviews/issues/1020) - @martinthomson, @zcorpan, @marcoscaceres

Martin: we've discussed... we think this is fine...  We minuted the thing last week...

Marcos: yeah.. this is fine.. though didn't directly address the particular use case.. 

Martin: I think we can give them that feedback..

> Thanks for bringing this here.  We think that this is a pretty good feature that will help people deploy SRI.
>
> We do note that the use cases you raise isn't directly addressed by this.  It is more directly addressed by SRI itself, which caused us some trouble.  Maybe you can update the documentation to more accurately reflect the chain of logic you need to follow to get from the mechanism to the use case.

**we agree to post the above comment and close with 'satisfied'**

#### [design-reviews#1063: WebGPU Compatibility Mode](https://github.com/w3ctag/design-reviews/issues/1063) - @martinthomson, @torgo, @matatk

**punted**

#### [design-reviews#1061: CSS View Transitions - Nested View Transition Groups](https://github.com/w3ctag/design-reviews/issues/1061) - @xiaochengh

### *readout of AI discussion*

Martin: I have concerns...   most of the writing assistance APIs sit on servers right now... why can't sites source their own compute for this?  they created a new interface on the global scope called Writer... 

### Plenary Session 

Present: Dan, Jeffrey, Hadley, Martin, Lola, Yves, Christian, Matthew, Sarven

#### Associates Decision

Jeffrey: nominating Serena for a 1 month trial.

Martin: i suggest appointing for 1 year and if she wants to walk away that's fine.

Lola: I made a suggestion of having a date attached... I think it's better to let her know that after a month she's free to go...

**we're agreed to appoint Serena to a term that ends at end of Jan (same as other associates) and informally if she decides by end of April that it isn't sustainable, just let us know** 

**Yves to handle putting her in the appropriate task force.**

Martin: I think that Lola's point is good about having a date.

#### [carousels](https://github.com/w3ctag/design-reviews/issues/1037) etc... 
#### [design-principles#564: Add guidance for layout-forcing apis](https://github.com/w3ctag/design-principles/pull/564) - @xiaochengh
#### [design-reviews#1043: CSS.highlights.highlightsFromPoint API](https://github.com/w3ctag/design-reviews/issues/1043) - @torgo, @xiaochengh
#### [design-reviews#525: Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @marcoscaceres, @lolaodelola
#### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola
#### [design-reviews#1020: CSP report-hash keyword](https://github.com/w3ctag/design-reviews/issues/1020) - @martinthomson, @zcorpan, @marcoscaceres
#### [w3c/process#986: Enable AB/TAG to remove one of their members](https://github.com/w3c/process/pull/986)

#### Breakout Rollup

##### Breakout A

https://github.com/w3ctag/design-reviews/issues/1030 - **matthew takes action to close it with an appropriate closing comment**

https://github.com/w3ctag/design-reviews/issues/1034 - **agree to close with an approved rating - dan to leave comment**

https://github.com/w3ctag/design-reviews/issues/1017 - **agree to close - dan posts closing comment from dan clark**

Jeffrey: we talked about 468 .. HTML's handling of focus... we talked about handing it to APA... 

Matthew: we [APA] have started to talk about it.  I would be on the side of closing it right.  I agree we should close on the TAG side.
ACTION: Matthew to open an issue on the APA side so that we can point to it in closing our issue.


##### Breakout B

Jeffrey: we're going to invite Domenic to join us in the coming weeks. Also there is a Mozilla proposal for a translation API which would be good for comparison.

... private proof.  Martin has written a comment. Hadley joins the issue and will review and then we can post in the coming weeks.  Some discussion of which working group it should go into - possibly a new anti-fraud wg...

... we closed visited links as satisfied. We skipped view transitions...  We had a long discussion of Isolated web Apps... We talked about asking Google to stop asking us about this... I got one last pitch... this is an attempt to do an OS with community decided APIs... that's an interesting goal. We don't have signals that others would implement this OS...  But if the TAG says "this is not the web, we don't want to see it"... then they will produce an OS that is proprietary... 

Martin: it would be more convincing if there were others involved...

Lola: seems like a threat... if we say "no" then it'll be proprietaty ... we're not saying "you can't have your toys" we're saying it's not part of the web.

Jeffrey: with IWA APIs it's segregated from the web... different from Fugu APIs where it becomes a compat risk... It's more like ChromeOS... it's not the web but you can do your OS however you want...

Dan: could we imagine a WG being formed .. maybe similar to Immersive web model?

Martin: this is similar to MiniApps.. so it's like automotive .. that's something I don't think we should spend time on .. unless it becomes a big thing. E.g. new future of apps..

Jeffrey: ChromeOS is definitley implementing this... As far as I know there are no other implementers.. The comparison to miniapps makes sense...  The suggestion to do a CG makes sense. You only need multiple interested people to do that... I think it makes sense as TAG to give them a closing comment "please proceed a CG. we appreciate the attempt to do OS APIs in the open." 

Martin: I think that's constructive. If this turns into something that has multiple implementers then we'd have to re-asses..

Christian: In some ways I disagree... difference to miniapps... it should still all be web based... packaged app to avoid tampering allows them to enable more powerful APIs .. that makes sense.. I would also agree that this didn't take off yet. It's single implementer. I've talked to developers at conferences that find this interesting. Only a few .. very specific use cases. I think the resolution makes sense. Close it for now and we can always open again.

Yves: The main issue is diverging from the web platform.. meaning if you want to adapt and enhance some spec because of a specific uses case... becomes an issue...

Christian: they hit this border of the web... they want to use sockets .. not directly... the web. Diverging of the web platform...   People are always wanting to do something extra .. and the answer is "do electron"...

Martin: the concern is not that... new capabilities .. new powerful features. the concern is to redefine how a worker works or how fetch operates... 

Jeffrey: or worse how CSS works... and no reason to do it in IWA space...
but it may be tempting to do it because it's easy. 

Jeffrey: I think martin and I are happy to collaborate on a closing comment in a couple of weeks.

Dan: steering them toward a specifc CG also means it won't be lost among everything else in WICG

**NOTE: we have an agreed direction on IWA closing comment - see above.**

##### Breakout C

https://github.com/w3ctag/design-reviews/issues/1058

Matthew: Is our advice .. ?  .. other thing - on desktop we suggest using proposed technique and other places use this preview technique.  Too ios/safari focused? Other question that didn't occur to me .. previwews wouldn't be interactive. Some of the interest target use cases ARE interactve - you can't do that if you're just looking at a preview - it is a different thing. I almost feel like we're saying "stop it" in a round-about way and I don't want to say that.

Martin: [in chat] By the way, our layout folks really don't want to be able to have a media query for previews.  They don't much like the way it might work (flipping it on and off to get a tab preview seems wrong).

Jeffrey: I like Martin's comment. I think it's interesting to bring up the idea of fetching a preview ... of a custom page. It needs to be light weight... I think that might do the idea. It might not. We should phrase this as "here's an idea that might break the impasse with [webkit]". I don't want us to say that long press doesn't work but I agree with saying don't mandate it.

Martin: I think this boils down to asking them to think outside the scope they've set themselves... about solving the use cases ... we don't have to give them the solution... we're seeing people go off and have those discussions... we don't have to be the ones responsible...

Jeffrey: I do want us to be able to say "xyz browser implementer has been unreasonable"... Folks have suggested an exploration direction, so it's not time to say that right now...

Martin: I don't think it's unreasonable what Apple have done... 

Torgo: we don't shy away from saying that something is wrong, but we need consensus to do that.  We've all had frustrations with different browser vendors at different times.

Jeffrey: Desktop has a lightweight gesture.  There's a delay when I tried it, so fetch might make sense, but sometimes fetch isn't.  How acceptable is it for desktop and touchscreen to differ a lot? The implementers disagree. An open question? 

Matthew: I am going to the AC meeting next week... My expectation would be .. TAG might come to consensus ... 

Jeffrey: I can just paraphrase the comment to Mason so he can start making progress.

Martin: i don't have a problem with that... finding a solution...

##### Next week

Lola will present Societal Impacts questionnaire.. Jeffrey, Hadley and Dan will present...

##### AB Decision Process

Martin: so.. florian put up a PR. I gave feedback at https://github.com/w3c/process/pull/888#pullrequestreview-2585601139 .. all of that feedback was ignored .. 2nd time this week that the AB has ignored my feedback.. this is frustrating.. if there is a person on the TAG or AB then it's good to have a process to ask them to leave.. the way they've set it up it guarantees that the process never works.. 

Yves: already a process existing .. asking the CEO .. can be overruled by the board ... already a mechanism to do that.. 

Martin: I prefer self governance... Suggestion I had was some kind of public reporting.. none of that was included in the PR.  There needs to be a process to retuen people to the vactaed seats...

Hadley: concerned ... I disagree with some of the points Martin raised... The mission we got from the AB/Chairs meeting ... was to gather TAG consensus... if we don't have consensus then we can give all of our views... they can't say "TAG is on board"...

Jeffrey: other comment I heard is that AB should have waited for [TAG's] review before merging this.

*consensus on this point*

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
