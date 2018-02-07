## TAG F2F - London
##### 02 February 2018

Present: Hadley, Lukasz, Dan, David, Peter, Andrew, Alex, Travis, Sangwhan (remote), Yves (remote)
Regrets: Tim

---

Agenda:

### Feedback from last night's meet the TAG

Dan: Andrew suggested that it might've been good to do lightning talks on our current issues. But I've also received back feedback on that.  Thoughts?

Andrew: Difference between talking off the cuff about the issues we discuss vs. having some slides to show in code how you'd use them. 

Travis: When I asked, someone said "I enjoy coming to these Meet the TAG meetups because I get to learn about new breakthrough things the TAG is looking at."  I thought it was interesting because I go to hear from THEM.

...That didn't happen yesterday since we had breakouts about what people were aware of.

Hadley: Because we had a table on privacy, which was a woollier topic, we had more questions about how things work, how features interact, who is building what, etc. So it was closer to what you're saying, Travis.

Lukasz: I asked the question about geolocation and there was interest about how this data would be used in particular.  I'm still unconvinced that including a permissions message is a bad idea. I think some UAs might use it, to enhance transparency.  

...In this sense, the privacy session was informative. 

Dan: I will ask for feedback from attendees and post notes.

...The format of going to breakouts was driven by the room.  

Alex and Travis: worked well.

Hadley: Agreed — though it was loud at times.

Dan: any revelations?

Andrew: I hadn't considered web packaging as an alterative to PDFs.
David: I agree  — I think most people use it becasue it is a Thing you can Download — not because they need a PDF.

Dan: Someone was interested in using web payment for transactions for government services.
Mentioned that normal user journey assumes a merchant initiating a payment request, whereas in gov services the user sees gov as the host. 

Hadley: We talked about the differences between us few users who understand how the web works and those who don't, and how much existing browsers optimise for users who don't. We explored the implications of more browsers that tailor for specific use cases, like browsing in a complete "I don't trust the web" way (blocking all scripts til sites are whitelisted, etc.)

Peter: HTTPS in local storage devices... Encouraging the possibilities of marking these devices as being secure, but real scenarios. 

Alex: the difficulty is that if you can see them on the network but can't request resources publicly, through DNS, this doesn't work.  

Peter: Re home networks, so many firewalls and routers are doing their own DNS.  Some of us do our own DNS setups. There is a need to provision certificates and do device certification in these use cases. 
...We focused on localhost for secure contexts.

Dan: Cab we help? These issues often take a back seat to the needs of the public web.

Peter: it's TLS in general... A lot of this is IETF territory. But it would help to have more awareness of this issue, even if the solutions don't come from the W3C. 

...Someone is going to send me a paper on their progress in this space. 

## Triaging issues

### [Media autoplaying as a permission](https://github.com/w3ctag/design-reviews/issues/203)

Dan: Status?

Agreed: moving to extra time.

### [saveData attribute in Network Information API](https://github.com/w3ctag/design-reviews/issues/204)

Extra time

### [Web Lifecycle for system initiated Discarding & Stopping ](https://github.com/w3ctag/design-reviews/issues/205)

Extra time to complete review

### [`Accept-CH` header is weird](https://github.com/w3ctag/design-reviews/issues/206)

Action to write up our response: Andrew

Milestone set for 2 weeks from now

### [Sensor APIs](https://github.com/w3ctag/design-reviews/issues/207)

Sangwhan: Nothing to do until they respond, addressing our feedback.

Move milestone to 1 month from now

### [import.meta.url, and import.meta generally](https://github.com/w3ctag/design-reviews/issues/208)

Alex: [explains the issue] 

...I'm working on the feedback.  Will finish today.

Move milestone.

### [Consider general storage observer that works for cookies](https://github.com/w3ctag/design-reviews/issues/210)

Travis: This is extra time, did some research and haven't written up yet.

### [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211)

Alex: I'll write up feedback.

Move milestone to next week

### [TAG review of Web Audio API (round two)](https://github.com/w3ctag/design-reviews/issues/212)

Dan: for later today (2pm)

### [&lt;link&gt; rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213)

Andrew: [summarises his thoughts]  Seems more like a new "as" than a new "reload", from the developer's perspective.
alex: The argument here is that there is some history around 'preload'

Andrew: the main argument is around dependencies...

Dan: [calls time]

Adds extra time label.

### [Dusting off Web Speech API?](https://github.com/w3ctag/design-reviews/issues/214)

Dan: set for future telecon

### [Files and Directory Entries API with webkit prefixes!](https://github.com/w3ctag/design-reviews/issues/215)

Dan: set for future f2f

Travis: There's new feedback... let's move it to extra time.

### [Review Decentralized identifiers (DIDs)](https://github.com/w3ctag/design-reviews/issues/216)

Hadley: I need to catch up with this...

Move milestone to 13 Feb.

### [Web Locks API](https://github.com/w3ctag/design-reviews/issues/217)

Dan: Done

### [Review Request: Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218)

Sangwhan: I need time with this.

Dan: Can we do anything productive in an extra time session?

Alex: for efficient playback, getting new frames without hittering, it's necessary for most services to choose between one of many kinds of transcoded media. That decision is hardware-specific and the info isn't easily available.  The goal is to go to the page and just play the right one. So this lets the page decide.

Hadley: Sounds fingerprint-y.

Alex: It is.

Move to more time

### [CSS Selectors 4](https://github.com/w3ctag/design-reviews/issues/219)

Travis: Started this on day 1 off this F2f. 

Dan: Adding to Extra time.

### [Img decoding attribute](https://github.com/w3ctag/design-reviews/issues/220)

Already on extra time

### [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221)

long comment... extra time

### [Request review of (text only) Async Clipboard API](https://github.com/w3ctag/design-reviews/issues/222)

already extra time

### [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223)

already extra time

### [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224)

Adding to extra time

### [Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225)

Dan: adding to extra time.

### [Picture-in-Picture (PiP)](https://github.com/w3ctag/design-reviews/issues/226)

Already extra time

### [Web Components Guidelines Doc?](https://github.com/w3ctag/design-reviews/issues/227)

Dan: Leave for now

Set milestone for Tokyo f2f 

### [Should WebRTC be \[SecureContext\]](https://github.com/w3ctag/design-reviews/issues/228)



### [Web Audio](https://github.com/w3ctag/design-reviews/issues/212) 2PM

Lukasz (in advance): re-surfacing some past and current web audio concerns: https://lists.w3.org/Archives/Public/public-privacy/2015OctDec/0123.html - since 2015 much more new developments. Need to update security/privacy considerations. Have some concerns to self-review answers (i.e. points 1, 2 - the answers should be "yes"). 

Lukasz (in advance): inspecting the answers to the self-review questionnaire gives me hints onto how the changes to the self-review questionnaire.

Lukasz (in advance): where can I find a single place with all security/privacy questionnaires filled so far? 

Hadley: a google search? Try something like https://www.google.co.uk/search?source=hp&ei=BT10WrH7NIi-kwWO_5LwAQ&q=%223.3.+Does+this+specification+introduce+new+state+for+an+origin+that+persists+across+browsing+sessions%3F%22&oq=%223.3.+Does+this+specification+introduce+new+state+for+an+origin+that+persists+across+browsing+sessions%3F%22& 

David: Also some people may not write down their responses

Dan: It's a self-review, so we haven't asked people to give formal responses. 



# Breakouts

## Video Room

### Picture in Picture #226 (https://github.com/w3ctag/design-reviews/issues/226)

Hadley, Andrew, Dan and Sangwhan

[talking through use cases]

Sangwhan: Games, heads up display

...Doesn't seem possible with current proposal

Andrew:  So you can still do a hack with it pretending to be a full-screen window and just resize it.

Sangwhan: Or do it with canvas. It's an isolated element... if you want to have this as web content...  Would you allow different origin content?  Different content?  A shadow root?

Andrew: It's just like popping a window.

Hadley: that's where the fraud potential scares me - how much is user aware that they are changing contexts?

Andrew:  You can window-open anything you like... which is why pop-up windows require the address bar to be visible.  But you could open a chromeless window, which is what the developer expects.

Hadley: I'd feel better if it all came from the same origin.  More within what the user would expect. 

Sangwhan: Makes sesnse to accomodate web content, but that would require rewriting the spec.  It currently expects the content to come from the original document.

...Not sure if we should push for that.

Andrew: okay.

Sangwhan:  How do these two windows communicate? 

...The video-only use case is a bit limited.

Hadley: if we're getting content from somewhere else and user doesn't know they're getting content from somewhere else - breaking the same origin model, easy to be spoof?

Andrew: Does this require user interaction to trigger this? Or is it in the hands of the developer?

Sangwhan: It does say "user initiated", so I assume that it would happen on click or some equivalent.

Andrew: if it already says user initiated, that's fine.  What we're doing is casting an element to...

Sangwhan: No!!  (fights with mouse button)

Andrew: looks like safari already has an api for this.  

  (reviewing [explainer](https://github.com/WICG/picture-in-picture/blob/master/explainer.md))

You can't control where it appears on the screan.

Sangwhan: This is trying to standardise their efforts

...There is one property called "top" — not explained. The example code has it but the spec/API definition doesn't mention it. 

Andrew: perhaps it was previously in the spec and has since been removed.

...There is also an integer for start, which I assume is for timing.

...That would be tricky for content sources other than video.

Hadley:  that could lead to delayed pop-ups, if we're expanding it to web content.

Andrew: In canvases, it doesn't make any sense

Hadley: Agreed.

Andrew: Even the canvas modification is a huge change to this proposal.

Sangwhan:  Yes, but this is still in incubation.  I'd be willing to talk to them.

Andrew:  Let's put these points in the GH issue.

Hadley: The spec says 

The API applies only to HTMLVideoElement in order to start on a minimal viable product that has limited security issues. Later versions of this specification may allow PIP-ing arbitrary HTML content.

\[some discussion on what constitutes user initiated action\]

Andrew: [put comment into GH issue]

...Milestone of 2 weeks from now.

### [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218)

Sangwhan: This is yet another fingerprinting surface.

...I see a valid use case for this. It's covering MSCallowtype doesn't cover and the HTTP accept header doesn't cover.  But it does expose the chipset the user is on.  Which I guess isn't a huge issue because most UAs contain the model of phone/set top box, and with a look-up table you already know..

...Also this exposes power efficiency.  That could be used to do dynamic fingerprinting against a user, perhaps?

Hadley: I worry about this too, especially when we're talking about hardware. Harder to change/anonymise at the UA level.

Sangwhan:  the UA exposes a lot of that anyway. 

Hadley: wouldn't it be easier for the browser to spoof all the UA stuff and not have that materially effect the user experience whereas spoofing media capabiliies would impact what the server serves to you?

Sangwhan / Andrew: This happens already with spoofing UA.

Dan: Is there a mitigation to aks them to consider? Fuzzing, or a permission prompt?

Andrew: Fuzzing is the opposite of what we're trying to do here.

Dan:  what about a permission prompt? 

Sangwhan: That's covered in 4.2.  For privacy mode.

Andrew: but doesn't talk about explicit permission prompts.

Dan:  That's a dodge. Most users won't be in privacy mode.  When something is out there like the WebRTC IP address issue, trackers will use it immediately for fingerprinting even if they're not serving anything using that feature.  NYTimes were doing it, even though they weren't using WebRTC with their users.

...So saying "private mode should mean different behaviour" won't cut it.

Andrew: So it could require user consent regardless. Of course we also have issues with the lack of standardisation of privacy mode too.

Dan:  This is fundamentally private information. 

Hadley: I fundamentally agree.

Sangwhan: I'd like us also to review the technical aspects of this, the API surface.

Andrew:  I'm scanning it... I'm not a video person, but to me it looks fine.  Sangwhan?

Sangwhan: Could review it over lunch (GMT) and add the privacy comments. 


### [saveData](https://github.com/w3ctag/design-reviews/issues/204)

Sangwhan: This could allow dynamic fingerprinting. Since saveData could be initiated by the OS, in the event you have bad signal — you could track the user against known bad connectivity.  If you're using hte same cell network you'll have overlapping IPs where this would be difficult. But if you have two origins watching the save data and you see it changes — you could correlate that the two patterns mean it's the same user. It's a timing attack. 

Dan: Even across devices, over time.  If you have two phones — they could provide data that correlates. 

Andrew:  But I don't just leave it on...?  Is there an automatic behaviour here?

Sangwhan: well, if the OS does it automatically. Or if an operator does it in an operator-branded phone...  If a sw is running, they can correlate the usage patterns.

Hadley: Well if the threat model is the mobile network konwing where you are and what you're up to — they already have a lot of data on that. but I still would like the implementers to understand the stakes here.  Make informed decisions on how they implement this for their users.  (Or if they implement it, if they are particularly optimising for privacy.)


Andrew: Okay, let's write that up. Best we not go too far into solutions right now.

Sangwhan: Yes. In the context of which client hints are dynamic.

Andrew: So there is a meta point here: dynamic hint variables can provide trackable profiles when monitored and correlated over time.

...What else?

Sangwhan:  Seems useful. Also, we wondered if this overlaps with acceptCH?

Andrew: we'll mention it here too.

Hadley: not thrilled with shrugging on fingerprinting.  can we ask them to put a bit more time into it?

Dan: +1. We should say "great; we don't think you're taking the fingerprinting issue as seriously as you ought to be."  What they've written, to me, feels fairly dismissive, to get people off their back rather than with a desire to address the issue. 

Hadley: ....or minimise the potential for fingerprinting.

Andrew: We're assuming it exposes fingerprinting based on the OS... they're saying it's already directly measured by recent fetches.

Sangwhan: Bars on the signal

Dan: or Edge vs 3G vs 4G.  Probably a combination of factors.  

Hadley:  If you get this info from connection measurements and I give you more info through saveData... Doesn't that expand the fingerprinting surface area regardless?

\[ Dan: just to note: they list private IP address visibility in WebRTC as an example of other APIs that expose information that can be used for fingerprinting surface - that is a specific example of something that was fixed in the spec after the TAG fed back that it needed to be mitigated: https://github.com/w3ctag/design-reviews/issues/14#issuecomment-203995268 \]


### [AOM #134](https://github.com/w3ctag/design-reviews/issues/134)

Latest spec: https://wicg.github.io/aom/spec/

Travis: I see that there is a phase 1 and phase 2 spec.

Sangwhan: Behind a flag.

Travis: authors are specifically asking for a review of part 2. I read the explainer again. ... They started off with an assertion I don't think is true. "Accessibility APIs are also popular for testing and automation. They provide a way to examine an application's state and manipulate its UI from out-of-process, in a robust and comprehensive way."  The way to automate the web is "webdriver" - simulate touch, pointer, keyboard interaction -- this is how you automate testing of the web. The Accessibility APIs do not provide anything near as comprehensive.  Testing and automation is not a scenario where this could be used.

Sangwhan: it shouldn't be the main goal of the spec though it could be used...

Travis: assistive tech does not exclusively use the accessibility APIs provided by the browser - e.g. jaws will read the regular DOM to annotate and enhance what is missing from the AOM.  

Travis: Thought experiment: if an accessibility tool can read the whole dom, they can recreate the accessibility tree themselves.  So hypothesis: browsers don't need to implement an accessibility tree.

Hadley: are you proposing ...?

Sangwhan: is this for content developers?

Travis: yes. The accessibility tree is not a good data model for the application - because the DOM is a mixture of structure and vide, many applications have app logic that is external to the view.  e.g. a google spreadsheet app - it's costly to render all the cells in the DOM. You have a data model that is sparsely populated but only when the user scrolls do you render into the view. In that scenario if the view is the thing you have an accessibility mapping of then the accessibility tool would not have access to the data that is not rendered.  This is similar to the problem that is happening with content editable. 

Sanwhan: you have to make a specific transition in a specific DOM element ... to propogate down to the data model.

Travis: scenario I hear a lot is - a mail webapp - in one of those mail apps you have a list of messages. that list can be really long. 100s to 1000s. If you were to create DOM elements to represent all those messages then you would generate nodes for things thr user would never see.  You have a data model somewhere else - the list of emails - even that might not be available in the browser's memory. But if you wanted a screen reader to read that list and report how many elements - then you need a separate way of fetching that info. Hooks necessary to do that are not available. This API tries to address that scenario.  So AOM does need to exist.

Travis: going back to that - what is an accessibility tool except for a kind of web driver.  it's driven not by code but by user input. ... so if webdriver is providing all the hooks to (e.g.) iterate through items in their email list - is this AOM API necessary? \[if we already have webdriver\]

Sangwhan: ... possibly ... could be something we could raise.  Webdriver is also powerful.   Maybe more powerful than the user because it can see elements that the user can't see.  I don't know how webdriver has evolved in its security model.  It's for testing - how do you deal with scenarios where multiple entities are accessing same (tab). 

Hadley: references [webdriver spec](https://www.w3.org/TR/webdriver/) See note: 

> An activation trigger generated by the WebDriver API user needs to be indistinguishable from those generated by a real user interacting with the browser. In particular, the dispatched events will have the isTrusted attribute set to true. The most robust way to dispatch these events is by creating them in the browser implementation itself. Sending OS-specific input messages to the browser's window has the disadvantage that the browser being automated may not be properly isolated from a user accidentally modifying input source state. Use of an OS-level accessibility API has the disadvantage that the browser's window must be focused, and as a result, multiple WebDriver instances cannot run in parallel.
> 
> 
> An advantage of an OS-level accessibility API is that it guarantees that inputs correctly mirror user input, and allows interaction with the host OS if necessary. This might, however, have performance penalties from a machine utilisation perspective.

Travis: a substantial missing piece - web driver is one way. In AN AT you need 2-way - into the web page and back out - hearing where you are and where you can go next.

Sangwhan: no direct data model mapping.

Travis: there's a whole standard for accessibility mapping for items in the dom - you could take that spec and implement it in webdriver...

Travis: this is an incubation project. 

Sangwhan : 2nd issue I have is that is accessibility object model - but this isn't an object model. An element - an accessibile node - is a super object. And a bunch of dead properties.  \[questionning the need for the complexity\]

Travis: Let's set a milestone and get back to it on a call.

### [Streams](https://github.com/w3ctag/design-reviews/issues/92)

Travis: what if we closed this issue here and put it into design guidelines as an issue.

Dan: proposal: close this issue and bring the relevant info from it over to the design guidelines repo as a new issue. then hold a special part of our agenda in Tokyo for working on streams-related topics that can go into the design guidelines.

Dan: \[could we also run a similar session on web components best practices for the design guidelines and then issue a revision of the design guidelines post tokyo which has updated info on both streams and components?\]

Sangwhan: the design guidelines is for spec authors and the problem we see on web components is for devs.

Hadley: Right. so we need a separate document maybe for technical best practices for components maybe - not in the design guidelines.

Sangwhan : also for streams - we need to find what parts of the platform should have been streams / promises and are not. This is a big project that TAG should maybe try to tackle.  This is architecture - the paradigm has changed.

\[meta discussion\]

\[Sangwhan to draft a blog post soliciting public feedback on where streams or promises could be used in existing specs that do not make use of these already.  We will then funnel that feedback into a design review repo issue.\]

### [Image Decoding Attribute #220](https://github.com/w3ctag/design-reviews/issues/220)

David: browsers don't decode them until they think they're visible. one reason this API is ... is that a bunch of the engines don't trust developers to say "decode this image now" - because the engine might not want to do it.

Sangwhan: image loading logic is wildly different across different implementations.

David: the thing whre decode is synchronous - what we really need is that *if* the image is going to be decoded (i.e., it's visible), the load event doesn't fire until after decode.  That would have less synchronous stuff.

Travis: the attribute tries to stop the flashing when you switch images.  \[travis explains it all\]

David: right now browsers do different things - where someone inserts an image element into the dom when the image is already loaded. you want image decoding to be async on a different thread.

Travis: developers just care if the image is in the dom then it shows up.

Dan: why do we need this?

David: some implementers will 

Sangwhan: neither behaviour is correct - this review is about : we're making a guess based on statistics why not make this definable by the content author.

Travis: the assertion that there should never be a flash is incorrect?

Andrew: can't we use heuristics for this? if the image element has previously held another image...

David: not the same image element

Andrew: something heuristics...

Dan: there is a false dichotomy at play here

David: if all the browsers did the flashing answer then the previous 

Sangwhan: this doesn't add complexity to the platform...

Dan: giving some super web developer super powers

Andrew: no I don't think so - it's a bit like sync-xhr - we all agree it's a bad idea and we can find a better solution...

Travis: onload fires not when the data has been decoded...

David: a bunch of this is side-effects of where browsers have complicated heuristics...

...

Travis: recap...  people that are preloading images ... browser fetches the data .. it's preloaded but not displayed. when it comes time to display it you want it to be ready. there is no way to know.  

Andrew: so when you change the display state in CSS it may need to be decoded and this attribute is saying "don't actually do the paint until the decode is done".

Dan: For this use case, why would you want it to be otherway around, the browser to start painting if decoding isn't done?

Sangwhan: You can't have both easily. 

...

Travis: who cares about this?

Sangwhan: Safari cares about it.  Developer can decided based on this feature ... between importance of images vs animations...

Dan: wouldn't it be more important at the page level?

Sangwhan: no. because many of the images are UI elements etc...

...

Dan: what developers want this

Sangwhan: i think developers will want this.

Travis: i think david was saying the opposite

David: if you have animations that are tied to the main thread then they are gonna jank when you're decoding

Travis: you could get an object that represents the decoded bytes and assign it to the image... but you'd have to manage the...

Travis: the TAG could pull the EWS card and say "no you need to go back and explain this in terms of decoding as a system that makes sense - not just bolted on to the current element with more magical APIs".

Sangwhan: this is a quick fix.

Travis: the only people who ae gonna use this are the giant companies with the huge sites who can manage the complexity.

David: I'm not convinced only the biggest companies will know how to use this.

Travis: if you add an attribute to an image that is decoded synchronously and then you take an image element not in the dom and append it to the dom then it must synchonously decode and display it - otherwise it's free to do whatever it usually does. Might be sync might be async.

Sangwhan: lots of legacy content...

Andrew: we can say that there isn't consensus but that some feel it's unnecessary.

David: I think there is consensus that there is a pile of related stuff here and there is no plan for how to expose the low limited primatives.

Travis: I'd like to see an explanation of the low level primatives.

Andrew: I'd agree.

Dan: +1 - it feels like a hack

Hadley: it's a hack but the flashing doesn't bother me

Sangwhan: i will write up some feedback

Andrew: I have some sympathy for fixing this problem - native apps doen't have this problem - seeing these atefacts is a reminder that you're "on the web" but I think this particular work is not well thought through.

### [Web Locks](https://github.com/w3ctag/design-reviews/issues/217)

Andrew: In their explainer document they explain all the alternative API proposals

Travis: Can I request a 2 minute break?

\[Break\]

Travis: is deadlock possible? tentative conclusion: no...

David: it just means your promises will never resolve



### [Storage Observer](https://github.com/w3ctag/design-reviews/issues/210)

Travis: I reviewed... many things... designing a newer, better cookie API...  One of the motivations for building a better cookie API is that service workers don't have access to the document.cookie property. 

Why?

Andrew: I've wanted to access cookies in service worker almost every time I've used serviceworker. [litany of use cases]

Andrew: cookies are complicated - 

Travis: the way we interact with cookies through the document.cookie property, it's a single string which is a serialization of cookies with attributes... cookies visible to your origin... 

Andrew: also not consistent

Sangwhan: cookies and service workers have a slightly different way of defining origin. Cookies are more lax in terms of what origins it can affect.

Travis: I believe one suborigin under a TLD or something like that.
the async cookie store proposal gives you a object oriented approach to cookies
and everything is promise based

Andrew: Do we need a more generalized approach to this problem?
Do we need a better API for cookies?

Sangwhan: Yes, we do.

Travis: Do we need a general storage observer for things, e.g. cookies, localStorage etc.
I think the general idea is no - IDB is a very specific system that needs this, but how the current way cookies is done makes this design a bit tricky to fit in to this.

Andrew: How does IDB observers work?

\[Explanation of IDB observers\]

Andrew: Do we think we can generalize this?

Travis: Probably not - but the cookie API does works better. The new API introduces async APIs against cookies and also enables access from service workers. Especially, observation is important for SWs.

---


## Non-video Room

### [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224)

Discussion, David to do further review.

### [Typed OM](https://github.com/w3ctag/design-reviews/issues/223)

Discussed, issues filed. David continuing to review.

### [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221)

Discussion about url templates, filed comment about shifting to a service worker approach.

### [CSS Selectors 4](https://github.com/w3ctag/design-reviews/issues/219)

Discussion about specificity, column combinator, input element state (vs generic state mechanism for web components).

Comments filed in issue. 

### [&lt;link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213)

Discussion about preload processing of modules vs other resources with potentially deep dependency graphs, e.g. stylesheets. This ties back to the rel=modulepreload vs rel=preload as=module discussion.

Comments filed.

### Module preload

### [Web Lifecycle for discarding and stopping](https://github.com/w3ctag/design-reviews/issues/205)

### [ResizeObserver](https://github.com/w3ctag/design-reviews/issues/187)

Discussion about dom vs layout conflation. Issues filed.

### Permission Delegation


### [Web Audio](https://github.com/w3ctag/design-reviews/issues/212) 2PM 

**... continued ... (with guests Chris Lilley, Paul Adenot)**

[Discussing ultrasound privacy issues]

Dan: \[We briefly discussed some of the issues brought up by Lukasz regarding utrasound but there was no consensus on this being an issue.\]

Issue discussion on https://github.com/WebAudio/web-audio-api/issues/1471 - is it gc observability? Some discussion on this point and TAG consensus is that this is not gc observability.

Paul: if we don't correlate the change in channel count to the gc then we are OK

Travis: they should not be correlatable

David: for any case where this might be observable.

Paul: we will make a provision in the spec.

David: there's a lot here - don't want to pass judgement too hastily.

Alex: I don't think you need joe's fix. What we're trying to avoid is where you implicitly have a destructor... I don't see any risk here.

Chris: Any other thoughts from the review? specifically on worklets?

Alex: We're happy with the worklet switch.

Travis: does web audio require secure contexts

\[no\]

Alex: rates of sampling... 

Alex: will APIs allow you to invoke codecs in both directions be available?

Paul: yes it's a layering thing - e.g. media encoder...

Chris: in privacy review we got a comment if the native sampling rate was a piece of fingerprinting data - so can we force everything to be same sample rate ... fingerprinting service is not that great - usually 44 to 48 - but can be very high or very low in certian cases.  It is new information.

Paul: it's akin to your screen size and pixel density...

David: likely a characterisitc of the hardware and the OS...

Paul: don't see a correlation to the OS.

Paul: in "resist fingerprinting" in Firefox it does reduce the clock to a specific ...

Alex: one last thing: when we first started talking there is an implicity sync - the "place" the sync driven for is not defined. Having a description of whatever that sync is. 






---

Scribes:
 * Wed AM: Travis
 * Wed PM: Andrew
 * Thu AM: David
 * Thu PM: Alex
 * Fri AM: Hadley
 * Fri PM: Dan







