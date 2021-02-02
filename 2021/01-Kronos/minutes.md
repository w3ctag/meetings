## TAG F2F Minutes : “Kronos”
### 25-28 January 2021

Agenda: https://github.com/w3ctag/meetings/blob/gh-pages/2021/01-Kronos/agenda.md

NB: The breakout minutes themselves are presented here in chronological order.  The “rollup” minutes (which summarize the outcome of each breakout, often with additiondal discussion) appear the bottom of the document.

## Breakout 01a:

Present: Peter, Tess

#### 399: [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399)

Tess [wrote up a comment](https://github.com/w3ctag/design-reviews/issues/399#issuecomment-767195003) capturing our current thinking on this re: a picker-style alternative API approach.

#### 558: [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558)

Peter: Dan reached out to Wendy to see if there's any appetite for a workshop on this topic. As far as I know he haven't heard back yet.

Tess: Maybe the best thing to do is just to ping her again. It'll be tough to make progress on a CG or workshop without anybody in the driver's seat of this.

#### 594: [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594)

Tess: I've been meaning to talk to jcraig about this; I'm reminded of IndieUI. This looks to be solving a narrower problem, though in a more imperative & complicated way.

Action: Tess to talk to jcraig

Peter: Thoughts on the API surface: 
* Activating a modal watcher via construction seems odd, would be nice to be able to construct one and activate it later, maybe something closer to the AbortController API.
* No way to tell if a given watcher is the currently active one.
* What happens when a watcher gets destroyed or a signalClose, but it's not the active watcher? e.g. a modal dialog opens another modal dialog, then the parent times out or gets a network event.

Tess recapped a bit about the accessibility events in AOM that got replaced with synthetic keyboard events, & some about the Indie UI "dismiss" event.

We contemplated the apparent fact that the web, for better or worse, has ended up with a 1990's desktop computer (monitor, keyboard, mouse) as it's basic abstraction. We agreed that having to add a bespoke XWatcher object to the platform for every niche X seems unoptimal, and suspect a simple, higher-level approach (like Indie UI's "dismiss" event) would enable browsers to solve the Android back button problem without all this complexity.

We also discussed the possibility of a higher level modal controller that also captures event, etc. e.g. all the things you need to do when starting a modal session, rather than small bits that you'd make one of those out of. Modal elements like Dialog could simply have one of those.

[Tess notes from rollout discussion, to turn into comment] We would prefer sending synthetic ESC key presses if/when the modal is either a real `<dialog>` or is marked up with ARIA. This problem seems the same as the increment/decrement synthetic arrow events thing in AOM—authors simply do what they should be doing anyway (provide aria attributes to say what their div soup is doing) and then the browser sends the events as needed.

#### 507: [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) 01b

Alice: Refreshing memory on the comments...

... Looking at the linked issues, I see they're all closed.

... [Relationship with VisualViewport issue](https://github.com/MicrosoftEdge/MSEdgeExplainers/issues/389)

... Argument is that we don't want a general-purpose occlusion API because not every occlusion should be reacted to by the page.

... [VisualViewport draft](https://wicg.github.io/visual-viewport/) doesn't list any user needs, hard to tell what was intended.

Sangwhan: I explicitly said web application-initiated occlusion, PiP being a good example.

... Putting the occlusion information in the keyboard namespace seems like something we're going to regret later.

Alice: Any other examples of occlusions we might be interested to react to?

Sangwhan: WebPayments - although some may disagree.

Alice: That's the "pay sheet" or whatever it's called, right?

Sangwhan: There's something native in Chrome, and there's content inside it.

... The response on [Relationship with VisualViewport issue](https://github.com/MicrosoftEdge/MSEdgeExplainers/issues/389) starts with "... [VisualViewport] is not a general purpose reporter of occlusions and provides no information today about occlusions. ... I wouldn't want web pages updating their layout as I ALT+TAB to another application that overlaps my browser, or have a web page fight me as a drag around a floating keyboard or a picture-in-picture window."

Alice: I don't think they ever replied to the question asking why it couldn't be a live set of bounds... CSS variables are live, but that doesn't help with the canvas case.

Sangwhan: They added an example for the canvas case, but that's listening to `geometry change` and then requesting the (live) bounds in a `rAF()`.

Alice: Oh, so the bounds are live now?

... Right, I see it's in the Web IDL now. Oh, and we had actually filed an issue on that that they responded to with that change. [Bounding rect property - possible to have it live on `virtualKeyboard`?](https://github.com/MicrosoftEdge/MSEdgeExplainers/issues/386)

... They did have an issue on the `navigator` question: [Is `navigator` the right place?](https://github.com/MicrosoftEdge/MSEdgeExplainers/issues/387)

... The response there is "Navigator by definition is the place to represent the state of the user agent, and VirtualKeyboard describes whether the user agent is in a state that could shrink the visual viewport when the virtual keyboard comes up."

Sangwhan: They previously implied that VisualViewport was abandoned, but it's shipping in Chrome and Safari.

... Leaving a comment

#### 589: [Declarative Link Capturing](https://github.com/w3ctag/design-reviews/issues/589) 01b

Alice: This is very much an "early review".

... looks promising to handle the use cases that are described

... to note that there are a narrow set of use cases in the first place

... lots of actions in capture-links, would be nice to know when to use what (e.g. examples)

... wonder how this works in mobile OSes, where one runs one app at a time

Sangwhan: There was a previous attempt to address this and that wasn't very well accepted (sw-launch)

Alice: Not clear to me whether it wasn't accepted, or just ran out of steam...

Sangwhan: Or they realised it would be too hard to implement, decided to go for a simpler API

(Alice typing a draft comment, Sangwhan reading explainer)

Sangwhan: This makes sense. Why was this not there in the first place?

#### 416: [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) 01b

### Breakout 02a:

Present: Alice, Tess

#### 521: [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) 02a

Alice: Looks like there's been no real progress on the prefers-reduced-motion issue. Left a comment prompting an update.

#### 494: [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) 02a

Alice: We had this as propose close - one outstanding issue Mason mentioned was the use of this feature as a potential sanitizer bypass.

Tess: Hm, that sounds like a real problem...

... [mitigation](https://github.com/mfreed7/declarative-shadow-dom/blob/master/README.md#mitigation) also seems reasonable. 

... I think we can close it.

#### 468: [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) 02a,

Alice: Looked at the PR on making `:focus` match on shadow hosts... https://github.com/whatwg/html/pull/4731

... This decision seems to have been made for reasons which conflict with the priority of constituencies: it shows a confusing focus style to users in order to avoid revealing the existence of a shadow root.

... I would have liked to see an explainer of user needs and platform constraints which led to the current design, as well as a description of the current design.

... In particular, `tabindex=-1` is more or less a historical accident due to some ancient behaviour in Internet Explorer, and there is no way to tell from the IDL `tabIndex` attribute whether an element is programmatically focusable, or not focusable.

... I started trying to explore the needs for this feature in https://github.com/WICG/webcomponents/issues/762#issuecomment-692416176 and a later comment on that issue, but it would be good to have a full "focus on the web" explainer.

## Breakout 02b:

Present: David, Rossen

#### 581: [css3-text](https://github.com/w3ctag/design-reviews/issues/581)

Rossen: was a previous discussion at a face-to-face, which Elika joined.  We asked her to list concerns, she talked about things that could be improved... so we didn't sign off then.  I'm not concerned with anything here.

Rossen: I'd be comfortable proposing to close this one.

David: One interesting thing in here is auto-hyphenation requiring authors to specify the content language.  I wonder if this is something that the spec should require in other places, or something that should be more visible.

David: ... but I'm fine with proposing to close this.

https://github.com/w3ctag/design-reviews/issues/581#issuecomment-767211799

#### 525: [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

Rossen: I think Tess and I had a spreadsheet.... did we ever find it?  We spent an hour building it in a breakout at some point.

(pinged Tess and got a [link to the spreadsheet](https://cryptpad.w3ctag.org/sheet/#/2/sheet/view/vsERK6AXCJecXP+cbJjHtiStBSz3R20DPbV7W53wpSY)).

#### 534: [VisibilityStateEntry](https://github.com/w3ctag/design-reviews/issues/534)

Rossen: David, there's a reply to your comment from the last time

David replies in https://github.com/w3ctag/design-reviews/issues/534#issuecomment-767216686

Rossen: also concerned about privacy.  Pointed us to privacy section in page visibility spec.  Could an author add entries that expose information that isn't currently detectable?  Explainer says that this is the same information as page visibility.

David: same information, just with performance entries rather than events?


Rossen: ??? about ETW events in Windows, can be used for generic buffering of information.  There's a hard requirement in that design that that they aren't used to drive any other behavior... so they might break.

... so when I read this... and hear David saying "they'd use the events for that case".... seems like they'd provide useful info to developers who want to optimize their pages, could also cause harm.  On the other hand, we don't change the web platform that disruptively.

Rossen: if a window on Windows is minimized, and a user hovers and gets the preview, what does that imply about performance entries?

Rossen: seems like a good use case

David: I'm probably ok with closing this.

Rossen: throttling... other reasons for delays... not sure how it affects entry (or feature).  If you have a process that's being suspended for some reason... when you're intending to navigate.  E.g., on iOS, if I move from browser to different app, page load might be suspended by the OS.  Then go back to Safari, and this is when they want the page visibility to fire... the intent of the proposal.

David: I think it should fire in that case... although maybe tab switching is a simpler case to think about?

## Breakout 02c:

Present: Peter, Sangwhan

#### [Permissions policy (formerly feature policy) evolution](https://github.com/w3ctag/design-reviews/issues/341)

Feature policy was split into permissions policy and document policy. All the issues we had were either addressed or moved into document policy. Closing.


## Breakout 03a:

Present: Ken, Lea

#### 563: [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563)

- We'd like to see screenshots from different platforms and/or dark mode to make sure this generalizes well - scrollbars look ver different on Windows where there are arrow buttons that have hover effect and can be pressed. Also they look different when two scrollbars meet
- Maybe allow `auto` instead of either of the `<color>`'s  to auto-generate the other with proper contrast.
- Control over scroll indicator vs scrollbar. What if I want a scroll indicator but not a scrollbar? (scroll indicators are painted over the website and auto hidden, scrollbars are always there). Some developers don't like scrollbars that take up space as they can change rendering when they appear and disappear, like on YouTube where scrollbar can appear because you open the drawer, ending up resizing all thumbnails. Slack as one example turns off naive scrollbars and draws their own scroll indicators which we would like to avoid as it can have a performance penalty. We think a third property is needed to control this distinction.


#### 592: [Early design review of CSS Container Queries proposal](https://github.com/w3ctag/design-reviews/issues/592) 

- Perhaps add physical keywords as well?
- Can you nest MQ inside this?
- We are happy to see this work and the proposal seems well thought out. It is unclear whether the additions to containment are only `inline-size` and `block-size` or their physical counterparts as well. We would recommend that both be available.

## Breakout 03b:

Present: Amy, Hadley

#### 240: [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240)

Hadley: This was waiting for a blog post by Peter and TPAC breakouts in 2019 with Peter and Sangwhan. We should ask them in plenary where this is and what to do about it. 

#### 571: [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571)

Thoughts: this could be good for smaller creative artists (musicians, designers, etc), to have app stores that aren't the existing ones.

This could prompt the creation of more app stores, which is good for decentralisation.  It could enable aggregation/search/discovery/similar services over the top of diverse digital goods app stores?

Have they thought about this use case, and is there anything in the design that would make this explicitly difficult?

What about other big stores than Play and Samsung? Other expected implementers like Apple, Kindle, Spotify..?

Concerns about the name, because it's so general.

[Our comment](https://github.com/w3ctag/design-reviews/issues/571#issuecomment-767393475)

## Breakout 03c:

Present: Alice, Dan

### 470: [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470)

[looking at the updated explainer](https://github.com/immersive-web/dom-overlays/commits/master/explainer.md)

Also taking a look at Ada Cannon's [example app](https://medium.com/samsung-internet-dev/making-an-ar-game-with-aframe-529e03ae90cb) which demonstrates the use of DOM Overlay.

Alice: on [input event duplication](https://github.com/immersive-web/dom-overlays/blob/master/explainer.md#input-event-deduplication) the "bubbling" seems backwards...

Alice: on [Compositing](https://github.com/immersive-web/dom-overlays/blob/master/explainer.md#compositing) - couldn't they specify the alpha blend blend mode for DOM content [automatically]? 

Dan: [the way they have it] seems unfriendly.

[Discussion on what is the default dom overlay type?]

Dan: Code has comment  ` // Show which type of DOM Overlay got enabled (if any)` so what does that mean?  Can you have a dom overlay without a type?

Alice: [writes up comment](https://github.com/w3ctag/design-reviews/issues/470#issuecomment-767375543) 

...discussion on whether users might consider overlay content as trusted UI and therefore is there a need for additional mitigation against 3rd party content... we decided not to leave an additional comment...

### 479: [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479)

Alice: they added terminology which I appreciate.  The explainer has gotten a lot better.

Dan: Seems like the updated explainer **did** [answer](https://github.com/w3ctag/design-reviews/issues/479#issuecomment-724975325) the question.

Alice: This is really good now.

Proposed close. 

### 545: [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/545)
### 550: [WebXR Depth API](https://github.com/w3ctag/design-reviews/issues/550)
### 588: [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588)

## Breakout 04a:

Present: Lea, Alice

#### 587: [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587)

- Missing a list of use cases

Lea: Top of mind for me is color format. We're not going to present all on-screen colors in implemented CSS>

... Bunch of color formats can go beyond sRGB gamut, but they're not implemented yet, and it seems that this API shouldn't block on those.

... However, only returning sRGB also seems bad. 

... CSS color is lagging... hex colors have a specific meaning today, which is not device RGB but sRGB. They can't represent up to 1/3 of on-screen colors... most Apple devices, many other high end devices have (?) screens.

... Remaining issues are syntax/API issues.

... They modeled it after `<input type=color>`, but that has different constraints. Native OS X color picker has an eye dropper... that opens in sRGB mode which somewhat mitigates the issue.

... Can't interpret non-sRGB coordinates as sRGB coordinates because it will be the wrong color.

... If we return an sRGB color, it's losing information.

... But waiting for the device-independent colors to ship everywhere would block them for an indeterminate amount of time.

... Shipping in Safari, but not yet implemented in Gecko/Blink.

... Could return LAB or LCH... Display P3 would solve the immediate problem but may run into issues further down the line.

... Ideally want them to return LAB or LCH.

Alice: Makes me wonder what their stakeholders are planning to do with the picked color.

... If they clip the color at the edge of the sRGB gamut, the color will be wrong.

Lea: Difference could be up to 7 delta-E units, and 2 units is perceptible.

... P3 color space is 50% larger than sRGB by volume, and as technology evolves this difference will only increase.

Alice: there was some talk about implementing LAB/LCH in chrome, but it was blocked on plumbing the higher-definition colours throughout

Lea: WebKit has managed to keep some colors as 8-bit and some as 16bit, with a flag explaning which is which...

... We can't be unable to represent so many of the on-screen colors in CSS. People are already asking why the most saturated red in CSS isn't as bright as the brightest red on their scheme

... People using images with embedded colour profiles to display the brightest green.

... Can we block their API until LAB colors are implemented?

Alice: is there a Color object as part of the the CSS OM?

Lea: Not yet... there's a lot of discussion going around but nothing yet...

... There is need for an actual Color object.

Alice: Not clear that CSSColorValue is really representing the same thing as a potential generic Color object.

Lea: Problem is representing the user selection in a way that can round-trip.

Alice: Even just as a programmer, having the color be a string makes me sad.

... Not clear to me that the rest of the application is going to be viable without high definition colors on the web - say you're creating a web-based image editing application and you want to be able to apply colors...

... Seems like there's no "happy" solution here - either you design a special purpose extensible "color" API for this one API (or this and color pickers), OR you limit both to sRGB, OR you sit back and wait for the CSS color work to be completed.

Lea: 4th option: spec it to return an LAB string rather than an sRGB hex string. But that's still a string, so it still has that problem.

... The rest of the API, `open()` is asynchronous. They note that it could show a permission.

... Seems to me that this is analogous to the file picker API.

Alice: Agreed.

Lea: Also a lot of complexity about allowing you to select multiple colors. Usually when you have some UI that does that, you can exclude the UI from being picked.

... Would be much easier if it was promise-based, and then you could re-`open()` the picker to select another color.

Lea: Lots of implementation details around coordinates, when it's not clear what they're for, and they're not always provided depending on where the point is (whether it's in a document from a similar origin or not).

... Using an event-based model makes the API harder to use, so it should be justified with concrete use cases.

... The simple case (picking a single colour) is unnecessarily complex.

Alice: Why does multiple selection require excluding the picker?

Lea: It doesn't - but you get feedback of what color you selected. Need to show the user feedback that their action has had an effect.

... Designing the API around single colour selection would avoid errors like forgetting to close the picker or having error handling mean that the picker is left hanging.

Alice: The UI could allow the user to pick colors until they find one they like, but only return one to the application.

Points:
- 4 ways to deal with color output, none ideal (1. wait 2. sRGB hex 3. lab() string 4. Special-purpose color API e.g. `srgb` property, `hex` property). Make sure to mention roundtripping.
- What are the coordinates needed for? The API is designed around these coordinates (PointerEvents) but coordinates are not always provided. It's unclear what use cases the coordinates are addressing.
- The API is designed around multiple color selection. The multiple color selection is primarily for fine tuning, but the UA can take care of fine tuning by showing appropriate UI and communicating the final color selection back to the app, which is also more privacy preserving. This would allow a promise based design and prevent bugs where the eyedropper mode is left open because something (e.g. an exception) intercepted the call to `.close()`.

Draft comment:

We discussed this today in our VF2F and have the following feedback.

a) The biggest issue is color output. There are four ways to address this, none ideal:

1. The Web Platform is currently in a transitional state wrt color. Possibly the best solution is to wait until there are more implementations of non gamut restricted color formats and/or a `Color` object.
2. You could clip or gamut map the selected color to sRGB and return an sRGB hex value (or other sRGB color format). The problem is that color **selection will not roundtrip** for at least 1/3 of onscreen colors in today's displays (and as display technology improves, this will increase). Given that many eyedropper use cases need precision, we do not think this is a good solution. We also think returning strings is suboptimal. For example, a user could have a Photoshop window side-by-side with a web application and use the eyedropper to select a color from the mockup to apply to their document in the web application. The color should be identical to serve this use case.
3. You could return an `lab()` or `lch()` string, which can specify any visible color. This does roundtrip, though is also a string. Another problem is that implementations of these formats are currently limited.
4. You could build a special-purpose color API, with `srgb` and `hex` properties. We do not think this is ideal, as it duplicates the Color API that the Web Platform will eventually get, and it's still unclear what the primary returned value should be.

b) The API is designed around using a `PointerEvent` but it is unclear what the use cases are for coordinates, espcially since their presence cannot be guaranteed and selection cannot be constrained to only areas where coordinates can be returned. 

c) The API is designed around multiple color selection as the primary use case, requiring use of events and explicit `close()`. However, as pointed out by the authors, the multiple color selection is primarily intended for fine tuning, but the UA can take care of the fine tuning by showing appropriate UI and only communicating the final color selection back to the app, which is also more privacy preserving. This would allow a promise based design and prevent bugs where the eyedropper mode is left open because something (e.g. an exception) intercepted the call to `.close()`.

## Breakout 04b:

Present: Ken, Dan

#### [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482)

Requested an update...

#### [Get Installed Related Apps](https://github.com/w3ctag/design-reviews/issues/436)

Ken: [left a comment](https://github.com/w3ctag/design-reviews/issues/436#issuecomment-767402072) asking for info on implementation status...

Dan: left a comment on lack of multi-stakeholder support...

#### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481)

#### [seeking beyond the end of a file](https://github.com/w3ctag/design-reviews/issues/600)

we proposed closed

#### [Suggested file name and location for the File System Access API.](https://github.com/w3ctag/design-reviews/issues/598)

Ken: Good explainer....

Ken: Left [comment](https://github.com/w3ctag/design-reviews/issues/598#issuecomment-767422304) generally supportive.

Dan: Left [comment](https://github.com/w3ctag/design-reviews/issues/598#issuecomment-767423162) asking about privacy issues.

## Breakout 04c:

Present: Sangwhan, Yves, Amy, Hadley

### 370: [WebHID API](https://github.com/w3ctag/design-reviews/issues/370)

Sangwhan: Propose closing and see where it goes

Hadley: security and privacy issues are thes same as other peripherals, they might get something out of looking at other ones. 

Sangwhan: it doesn't let you fingerprint based on number of devices because you get a device picker, you get to know only one

### 591: [Handwriting recognition API](https://github.com/w3ctag/design-reviews/issues/591)

Privacy concerns? Supposedly doesn't collect new information about the user. Drawing data can already be collected with the canvas.

Sangwhan: why is it on the navigator?

Yves: about i18n - how do they recognise vertical vs horizontal, mixed ltr and rtl?

Sangwhan: guessing they delegate it off to a native library? It's unclear

Yves: they have the basic order of strokes, but wondering about the result of the API? Text, text with information about orientation?

Sangwhan: when you create a handwriting recognizer you pass the language you want to recognize

Yves: for japanese you can write it horizontally or vertically

Sangwhan: I don't think I've seen implementations supporting vertical on a digitizer, but theoretically people might

Yves: prediction result is a JS object containing the strings.. one string without i18n information is probably missing something

Sangwhan: how do you deal with codeswitching?

Yves: right, you have an EU language with Arabic mixed in. Multiple strings with different information, how do they handle that? We make them get a review from the i18n group?

Sangwhan: what is distance measured in? Pixels?

Hadley: would guess pixels but they should make that explicit

Yves: physical or logical pixels?

Sangwhan: and how does it tie in with the API? Will ask.

Sangwhan: you can collect more information than the canvas with a dedicated writing surface. People would consider this as a handwriting input method rather than a scribbleboard. Can probably be used to collect more information? not from the API level but from how users interact with it? Not convinced it operates on the same magnitude as canvas. I don't recall ever writing a full sentence on the canvas surface. More likely you would write a full sentence here.

Yves: tablets are the main use of handwriting recognition

Amy: could be purposed to collect signatures, even though they are not needed to be recognised?

Sangwhan: and why do they want this exposed to the web? should be an IME?

### 478: [Mini Apps URI scheme](https://github.com/w3ctag/design-reviews/issues/478)

Yves: feedback that it's not a good thing to define a new URI scheme. They will be exploring using https only. We can probably close that one. Especially now there is a [WG](https://www.w3.org/2021/miniapps/) in W3C, they will probably give us things to review once they have something back.

Sangwhan: URL scheme is not part of the charter?

Yves: something about defining a proper way to address mini app, that rules out URL scheme

Hadley: one of our early concerns was that they wanted to get rid of the same origin policy. Hopefully [charter](https://www.w3.org/2021/01/miniapps-wg-charter.html) covers that as well?

Yves: that might be different. If they're using https there will be proper origin. They may decide to define a new security model, we need to be careful they are not doing that. But at least the origin would be there, compatible with the web platform.

Hadley: does this mean the first part of the scope includes the basic architecture and essential functions..

Yves: it's all the issues we have to review

Hadley: I had thought that what we were hoping for was each of those issues would be discussed with the rest of the web platform that's relevent. Manifest would be looked at in the context of existing manifest, packaging with existing packaging work (webappsec?), addressing with the context of URI standards in IETF? Is it likely that because those sectiosn are written separately to coordination that the WG will go off and do their own thing?

Yves: The goal was that manifest would be done in sync with webapp manifest. Addressing is more or less the same, it's about the URL scheme with implications on the security model, origin etc. Lifecycle there was discussion about aligning it with the page lifecycle work that is going on in W3C as well. Recognizing that there are different constraints in the miniapp world. At least being compatible on some part of the lifecycle.

Sangwhan: page lifecycle doesn't define PWAs very well so it's a good opportunity. And page lifecycle was abandoned, they could pick it up and fix it up. It's dormant.

Yves: I propose for the issues, now that there is a WG charter we should close those and wait for the next version from the WG.

Hadley: sounds good to me

Sangwhan: packaging is the really tricky one

Yves: When I looked it was mostly in relation with the work inside IETF Jeffrey Yaskin, secure exchanges thing. There might have been a need for delegating authority on the specific cached version, but the fact that addressing will work on that there is no need to add that in the packaging, they can use what they want. they currently are using a zip file and there's no need to be compatible with other packaging systems because there is no shared properties there. Discussion about packaging was look at other thigns and see if that fits and if not that's fine. Depends if you need some properties from them or not.

Sangwhan: rest of web platform has been pushing for signed/bundled exchanges but they don't work for this use case. The other part I'm concerned about is that they're using a zip file,which is bad for random access.

Yves: especially because the catalog is at the end, you have to download everything to start processing

Sangwhan: zip is not the answer for this kind of packaging. The alternative is signed/bundled exchanges and signed doesn't work for them and bundled is only halfway done. We've been trying to get a unified packaging format but I don't think bundled exchanges is ready to be promoted.

Yves: packaging is not what concerns me the most, it's reallye verything related to the security model. Addressing, lifecycle and of course manifest. We have to ensure there is no weird reason to do things on their own without coordinating with webapps.

Sangwhan: iw as concerned about their native widget embedding thingy, extremely scary. There's an API in one of their proposals. Hybrid rendering. Render a native UI component inside a webpage.

Yves: that could be 'interesting' for security.. A new WG has been created and they got oru feedback, so we can close the current issue and review again when thee's more. One week ago it was approved.

Hadley: difference between miniapps and PWAs?

Yves: the main diff is the installation process, and trust being in an app store instead of using only the origin to install the service worker.

Sangwhan: you can't currently preinstall a PWA, but supposedly you are able to pre-install a miniapp, otherwise none of the device vendors wold be interseted

Yves: a chat app, you can't in PWA rely on the fact the service worker will be always alive, can be installed every time based on constraint of the engine. Miniapp is mix of native app and webapp, you will always have the state of the chat application.

Sangwhan: the initial proposal contains some very powerful APIs like filesystem access. I don't think that survived into the charter aside from 'other components may be included by rechartering'

Yves: and about pre-defining specific web components

### 523: [Mini App Lifecycle](https://github.com/w3ctag/design-reviews/issues/523)

Ask at plenary if we leave this open or can close it as well

Yves: I think it's better to have proposed close on both

Sangwhan: lifecycle has not changed, maybe we should leave that open

### 524: [Mini App manifest](https://github.com/w3ctag/design-reviews/issues/524)

Proposed closed

## Breakout 05a:

Present: Lea, Tess

### [Early design review of light-DOM CSS Scope proposal](https://github.com/w3ctag/design-reviews/issues/593)

- Querying logic of "match A down the tree until B" should be separated out into a selector
- There should be an implicit `:scope` before scoped selectors that do not contain a `:scope`, which *might* already be the case but it isn't clear. Tess has asked a clarifying question.

### [Requesting a TAG review of CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584)

* We talked about the suitability of using this API for syntax highlighting
* Why is `HighlightsRegister` setlike and not maplike? Poor developer experience if one needs to iterate over it to see if an existing `Highlight` with the same name is registered

### [Review for CSS property "aspect-ratio"](https://github.com/w3ctag/design-reviews/issues/559)


## Breakout 05b:

Present: Dan, Peter, Amy

#### 414: [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414)

Hadley: I would like to ping the requestor again and see where they are now...

[disussion on trust tokens]

Hadley: possbility for misuse ... totalitarian govts...

Peter: concern of being able to categorize people based on metadata from the tokens... De-anonymization ... e.g. sign in to cloudflare sign-in with google... Cloudflare knows you're using google. Trust tokens could be used to allow anonymous access.

Hadley: it looks like after that initial discussion they are working on it...

Peter: as I recall there are mitigations... 

Hadley: [Mozilla supprotive](https://mozilla.github.io/standards-positions/#privacy-pass) of the ideals and goals but needs more securty analysis...

Amy: user activation at issuance of the token - I can't picture what that would look like. https://github.com/WICG/trust-token-api#mitigation-dynamic-issuance--redemption-limits

[we left more feedback on the issue and are waiting for response...]

#### 572: [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572)

Hadley: the big picture concept makes sense to me...

Hadley: CORS over private networks... 

Hadley: 3 layers - localhost, private IP addresses, and public IP addresses.  Local, private and public as layers... And mapping IP addresses agains them...  They are in RFC-1918.

Peter: the web site can make requests to web sites on local addresses - like your printer - and without CORS prefetch. A lot of these devices presume they will run on a firewall are not secure.  What they want to do - make any request on local host or a private network we do a CORS pre-flight and include a special header. Prevents the browser to making requests to local devices unless they specifically opt in.  Some concerns - e.g. HP has 2 /8 networks...  Every device on their network has 2 IPv4 addresses ... in IPv6 that is the norm.  Many ISPs give you IPv6... 

Peter: this doesn't stop you from opening up a connection to your device... it only stops an external web site from knowing if you're out of magenta.

Dan: IPv6 very common.

Peter: some variance on what ISPs give you...

#### 529: [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529)

Dan: [left comment](https://github.com/w3ctag/design-reviews/issues/529#issuecomment-767630093)

Hadley: notes the Privacy section of spec... feels very weird to have in a spec.

Dan: is it non-normative?

Hadley: it's normative.

Hadley: [leaves additional comment regarding privacy & security requirements](https://github.com/w3ctag/design-reviews/issues/529#issuecomment-767635629)

Amy: looks like most of the changes are implemented in browsers...

Hadley: in the s&p section they have 2 sections - one for UAs and one for recipients

Dan: they can't put normative requirements on recipients of the data, they're not implementing the spec so there's no teeth

## Breakout 05c:

Present: Rossen, Ken

### 509: [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509)

Ken: After talking to Daniel Ehrenberg it appears so that there is a new bundles proposal called "Resource Bundles". From the conversation it seems this will be a superset of the signed/unsigned bundles and will most likely obsolete this proposal. 
... Let's add a comment to this in the issue and move on to the next one.

### 511: [Beforematch event and content-visibility: hidden-matchable](https://github.com/w3ctag/design-reviews/issues/511)

Ken: It looks like this was reviewed with the CSSWG already and they deffered to TAG.

Rossen: That's right, we did talk about it with CSSWG but did not accept the feature. Instead of accepting, the SCSWG resolved to have TAG look at it first and then only move forward with working on it further.

Rossen: I'm still a bit worried about the a11y aspect of the feature. The change in behavior here can have the subtle affect of content not being available to users as it used to before. In other words, I'm a user opens a long Word document they are expecting that all headers, paragraphs etc. to be available to them. Setting `hidden-matchable` inside such document will now hide sections until they're in view or matched. Unless the AT query for the next header is the equivalent of a find-in-page, which isn't the case today, the content won't be abailable to the user and apear broken.

... I have two consecutive sessions with Alice later today. This seems to be one of the last issues with the proposal, let me go over it with her quickly and propose next steps.

Ken: Sounds good. Also, it does seem that the path forward for the feature is with the CSSWG as a property and not an HTML attribute for example.

Rossen: Agreed.

### 533: [Pen Events API](https://github.com/w3ctag/design-reviews/issues/553)

Rossen: This issue hasn't had much engagement by the authors since it was opened. I reached out the them yesterday in hope we will get them to respond.

Ken: That's right. Also, they indicated that issues should be opened against their repo.

Rossen: Correct. I'll go ahead and transfer the issues there and expect more details.

## Breakout 06a:

Present: David, Amy, Dan, Yves

### 76: [withCredentials](https://github.com/w3ctag/design-reviews/issues/76)

Dan: can we close it?

Yves: I'm not sure Tim would agree on closing it...

... there was a proposal on the [WHATWG issue](https://github.com/whatwg/fetch/issues/517#issuecomment-607623268) - it didn't get traction.  It was closed by Anne because of lack of interest.

Amy: there is another proposal - [878 on Fetch](https://github.com/whatwg/fetch/issues/878) - which is also part of this. 

[discussion on issue]...

Yves: no way to figure out whether resource exists or not.. security feature hiding everything behind... needs extra context besides URL to access something.  

Amy: if the server says "allow origin" - then you can't send credentials... 

David: depends what the values are...  Browsers can have access to stuff on another site that they can't sure with the first site.  Intranets and ambient authority. Access control allow origin * - simple value that tells the browser it can do anything for .. makes resources as safe... relatively safe thing for server operator to do - but then you have the problem that if you use cookies to get that resource then you can't share it with another site. So you need to tell the browser "don't send cookies to get this resource" - but some sites require a cookie to get a resource - and those need special headers to mark that these resources are safe to use...

Yves: access control allow origin * has been misleading to many developers.   This is what bothers people who say it's a "free for use" resource even though it may be accessed publicly with or without cookies.

David: I think some of these use cases [in 878](https://github.com/whatwg/fetch/issues/878) are suspicious.  When you dig into it - you have to ask what is the data for. If Tim has access to use the data then I can write a web app that accesses the data with tim's credentials and get a copy of it.  That's why I find some of these use cases suspicious.

Amy: that's the whole model of how the SOLID stuff works - the webapp doesn't care about the data but the webapp accesses the user's data with the user's credentials but in theory it's not sending it somewhere else.

David: but a browser can't trust any webapp to be acting on behalf of the user.

Amy: Maybe that's the fundamental issue that the SOLID stack is having?

Amy: ~~the assumption with SOLID is that you are using a webapp then you trust it.~~ edit: may be wrong about this these days, [related](https://solid.github.io/specification/protocol#cors) and something about users pre-approving trusted apps

Dan: but if I follow a link it must be safe - so could be my bank or evil bank...

Amy: client-side cert is one answer....  In theory if you didn't trust that app (like if it's a phishing attempt) then you could deny access at that point.

Dan: what about the [response doc](https://w3ctag.github.io/with-credentials/) we wrote?

Yves: that was the first proposal we wrote... 

Dan: so out of date effectively... 

Dan: If there are no open issues on this in WHATWG then maybe we should close this issue here? 

Yves: pretty sure we won't make progress unless there is buy-in from vendors and if clients don't give feedback in that way there's not much we can do to fix it.

### 582: [credentialless embedder policy](https://github.com/w3ctag/design-reviews/issues/582)

David: Mike west aske for review of credentialess embedder policy... 

David: connected to SPECTRE mitigation... 

Dan: I would like more context in the explainer - getting at the user need and the issue with SPECTRE veunerablity... 

David: browsers can't trust the CPU to maintain isolation between processes anymore. 

David: ways to turn sharedarraybuffer back on... 

Dan: [left comment](https://github.com/w3ctag/design-reviews/issues/582)

David: need to digest a bit more... Seems not unreasonable on the surface.

# Breakout 06a:

Present: Lea, Rossen, Peter

#### [Review of CSS Sizing 3](https://github.com/w3ctag/design-reviews/issues/565)

Rossen: (summarizing CSSWG/TAG reviews, explainers etc.)

Peter: The changes section looks good. What was missed by the original list of added features is `box-sizing` and to be fair this dates way back to the 90's so it's fine.

Rossen: Ack. Leaving comment and closing then.

#### [jxl Content-Encoding](https://github.com/w3ctag/design-reviews/issues/541)

Peter: My first reaction is - why isn't this just a mime type and Transfer-Encoding?

Rossen: Would that work in all scenarios? For example, going through proxies etc. and coming back with the original encoding?

Peter: It should be able to send a jpg from the server, encode it into jxl along the way, transport it assuming all proxies support it and finally get decoded as jpg back in the browser.

Peter: It seems like very much an edge case for which we're trying to add a lot of overhead for very little benefit.

Lea: It's not clear if and what the savings could be compared to other encodings that are already widely used, gzip etc.

Peter: Computation cost of the encoding/decoding isn't clear. Should they need both copies on the server and rely on content negotiations?

Rossen: Let's leave a comment and move on.



#### [Reporting](https://github.com/w3ctag/design-reviews/issues/585)

Rossen: This looks like a lot of potential PII problems.

... After a longer discussion we left a number of questions in the issue about privacy, API, naming and overall design.

#### [Early design review of Cascade Layers](https://github.com/w3ctag/design-reviews/issues/597)

Lea: Some initial thoughts. The name should be changed and we alredy have an issue about that. There is a well established visual interpretation of "layer".
... It seems like there is no way to define a layer with lower priority than unlayered styles. Often with libraries and frameworks you want to set defaults that sit above the browser defaults, but still want authors to be able to override them without wrangling specificity. It seems that all current syntaxes for defining layers do not provide a way to do this.

## Breakout 07a:

Present: Alice, Rossen

Rossen: Was discussing an issue with Ken that we thought you should take a look at.

... `content-visibility: hidden-matchable`

### 511: [Beforematch event and content-visibility: hidden-matchable](https://github.com/w3ctag/design-reviews/issues/511)

Rossen: Caught up Alice to previous 5c discussion.

Alice: Cleared up the expectations of proposed behavior. The feature applies to content that is already part of the DOM but kept out of the render tree, similar to display:none with the only difference that if a Find-on-page algo runs, it will match the query.

Rossen: Great, why isn't this an optional value of display? Something like display:none matchable; This way we have clear expectations of the behavior inside the element (no animations, transitions etc.) while allowing matches.
... Further, is the content inside the hidden-matchable available for name computation of ARIA?

Alice: It should be similar to the way we do it for display:none. Also, the intent of the feature is to apply to the contents only and not the element itself.

Rossen: Sounds good and I'm convince we should let the work continue moving forward with CSSWG. I'll add closing comments and suggest adding a WPT test along that verifies ARIA name computation works as expected.



> @kenchris, @alice and myself took another pass reviewing the final proposal of the feature during our "Kronos" VF2F. 
> Overall we are happy with the current design being a CSS property instead of HTML attribute. The functionality is similar to `display:none` if we were to add an optional `matchable` value and make it apply to the contents of the element and not the element itself.
>
> One important question that came up during the review is whether we have verified that this new way of making content hidden is handled correctly per the [Name Computation](https://www.w3.org/TR/accname-1.1/) algorithm. Since this feature makes content hidden our expectation is that the behavior will be similar to that of `diaplay:none` and we ask that you consider adding a WPT test to cover that scenario.
> 
> Specifically, that an `aria-labelledby` or `aria-describedby` attribute which refers to an element within a `content-visibility: hidden`, `content-visibility: auto` or `content-visibility: hidden-matchable` block will correctly expose the text of the element as contributing to the name/description of the referring element:
>
> ```html
> <input aria-labelledby="a-label">
> <div style="content-visibility: hidden-matchable">
>   <span id="a-label">This should be the label of the above input</span>
> </div>
> ```
> 
> Thank you for working with us.



### 583: [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583)

Alice: Took a look earlier and didn't see any comments since my last feedback. Noticed that they want issues in their repo, so I'll go ahead and transfer the issues there and wait for a response.

### 586: [ARIA 1.2](https://github.com/w3ctag/design-reviews/issues/586)

Rossen: Took a look at the explainer, but it wasn't very helpful.

... Looked at the spec, focusing on section [B.2 - "substantive changes from ARIA 1.1"](https://www.w3.org/TR/2019/WD-wai-aria-1.2-20191218/#substantive-changes-since-the-wai-aria-1-1-recommendation).

... spinbutton changes look good. rowheader, also looks good, group as child of listbox should have always existed so that's good. 

... "paragraph" role ... seems weird, I guess you could use it on a flexbox?

Alice: I think that's mostly about reaching parity with HTML.

Rossen: ... aria-expanded for menuitem, makes sense for sub-menus. 

... aria-errormessage has some normative usage changes. A little confusing, multiple negations... 

Alice: It's forbidding you from having an aria-errormessage when something is explicitly marked as valid using `aria-invalid=false`, because that's an inconsistent experience.

Rossen: Makes sense.

Alice: What about the IDL changes?

Rossen: looking..

... Are they following our suggested naming conventions? Looks like it.

Alice: There was some discussion at that point about whether some of those attributes should reflect to something other than DOMString..

Rossen: Right, some of these are numbers... For example [https://www.w3.org/TR/2019/WD-wai-aria-1.2-20191218/#aria-valuemax](aria-valuemax) is defined as a `number` by ARIA but reflected as a DomString.

Alice: There's an [open issue](https://github.com/w3c/aria/issues/1110) about this.

Rossen: We should check the WebIDL part once it's in a more mature state. The rest of the additions seem fairly straightforward.

... Leaving a comment and proposing close.

## Breakout 07b:

Present: Peter, Sangwhan, Tess

#### 578: [Require embedees to opt-in](https://github.com/w3ctag/design-reviews/issues/578)

No issues except compat concerns.

#### 596: [Review request: Partitioning Network State](https://github.com/w3ctag/design-reviews/issues/596)

Left comment about potential harm to end users re power and bandwidth consumption, but overall OK with this. Suggested mitigation for timing attacks aside from partitioning.

## Breakout 08b:

Present: Alice, Rossen

(Some time spent following up on [content-visibility: hidden](https://github.com/w3ctag/design-reviews/issues/511)) 

### 476: [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476)

Rossen: We have made it clear that we agree with the use cases and that these problems need to be solved, but we don't agree with the proposed solution.

Alice: I think we unfortunately have to give them some feedback that they're not going to be happy with.

... We've pointed out that their work identifying the problems to solve is extremely good, and that the problems are real and should be solved.

... However, the shape of the solution as an ARIA-like vocabulary doesn't seem like a good fit.

... ARIA had the characteristics that it was based on an existing vocabulary (MSAA), and was intended to be consumed by a single class of technologies (screen readers, later expanded to other types of assistive technologies.)

... In contrast, this vocabulary seems like it would have a wide range of consumers, and it's not clear that those consumers have been brought in as stakeholders to this design process.

... We suggest that instead of trying to solve all of these problems with one solution, that you could take the excellent work already done identifying problems, and look at solving them individually, working with the relevant stakeholders. 

... Some of these problems may be "stickier" than others; for example, trying to come up with a system to allow users to avoid unwelcome distraction from revenue-generating ads is going to involve buy-in from the publishers who need that revenue in order to keep operating as a business.

... However, other problems, like annotating words with the relevant Bliss or other symbol, seem very well scoped in terms of user need, authoring responsibility, and assistive technology implementation requirements.

... Not all of these solutions may even need to go through a standardisation process immediately, but may be better suited to [incubation](https://wicg.io/) to allow prototyping and rapid iteration as a collaborative process with the various stakeholders, before settling on a standard.

... We know this is not the feedback you were likely hoping for, but we would like to emphasise how rare it is that we get a proposal with the level of work put in to user needs as we have seen here, and that this is one of the most critical parts of the design process.

... We would love the opportunity to continue working with you on better scoped proposals to address subsets of the user needs you have identified, including very early stage ideas.

Rossen: We can use this opportunity to suggest that rather than shying away from media queries, that MQs may work well for some subsets of these problems.

Alice: Posted comment.

Rossen: Posted follow-up around working with CSSWG and media queries.



## Breakout 09a: Ethics Doc

Present: Alice, Dan, Lea, Amy, Hadley

### Ethical Web Principles

Hadley: Talking about collecting stories/issues to be added as footnotes/examples for each of the principles.

... We're not ethicists, but we're sharing our hard-won experience as a community.

Dan: Also coming from TPAC session called something like "towards an ethical web"

... That was a great session, and completely orthogonal from our document. We don't have the input from that type of diverse community, and bringing different use cases with societal implications. Getting other perspectives would be good. 

... How do we solicit and accept critical feedback?

Hadley: Felt like the folks in that session had a perspective beyond the web standards community, and how the web was working for them or disadvantaging them and their communities.

Dan:

https://www.w3.org/2020/10/TPAC/breakout-schedule.html#ethical-web

... Came out of p5.js community group; Boaz Sender had reached out to that group. I spoke to Boaz after TPAC about how we might get input from that community.

... He made the point that you can't just ask people to give their time for free, which is fair. Would need to find some budget for that.

Amy: Could go find the talks they've already given, and articles they've posted.

... There was also the Consentful Communication session, which was also really good.

https://www.w3.org/2020/10/TPAC/breakout-schedule.html#consentful-comm

Dan: Could talk about how the ethical princples relate to the design principles.

... Could start with open issues.

... Suggested principle: [user data freedom portability](https://github.com/w3ctag/ethical-web-principles/issues/5). Can we make SOLID part of the ethical web principles?

Hadley: Yeah... GDPR. I think the issue is also talking about GDPR... SOLID at a procedural level, and GDPR at a behavioural level.

Amy: Yeah, not just SOLID, also social and non-social applications.

Dan: As a former co-chair of the Social Web Incubator group... I am supportive of this, but it's a tricky one.

Amy: Related, the EU is working on interoperability.

... As a *current* co-chair of the social web incubator issue I also support this.

Dan: We have activitypub... 

Amy: Also several other standards...

Dan: Hadley mentioned this on Mastodon which runs on top of activitypub, and has a bunch of users. Might be worth giving it a bump in our principles, or the ideas behind it. 

Amy: There was some consultation in december about it; we had a social CG meeting about it.

... Digital Markets Act seems to be the name of it. https://www.csis.org/analysis/digital-services-act-digital-markets-act-and-new-competition-tool

Hadley: Amy, are you able to propose some text around that?

Amy: I would be happy to do that.

Hadley: We need to be careful to keep this grounded in current practice...

Dan: The EWP has "The web should support human rights, dignity and personal agency." This is enmeshed with that. As a person, you should have control over what happens when you use the web, and that should extend to the data that you create. 

Amy: Ideas around consent and how they fit in with interactions on the web, EULAs etc.

Hadley: That's a lot more nuanced than we have been so far.

Dan: Discussion around dark patterns... ethical principles should set the stage, be a high level principle that guides the design principles rather than trying to cram everything into that one document, so we need to weigh what goes where.

... Backing up each principle with references to previous TAG decisions... or should we talk about dark patterns?

... Let's get into the dark patterns issue. We added an issue in the S&P questionnaire to capture abusive patterns.

Amy: Dark patterns is about UI design and behavioural standards, so it doesn't necessarily fit well into web standards.

Hadley: We've tried not to limit ourselves to any one part of the web in the principles, but it's targeted to people creating new designs and specs.

... Might make sense to have it more as a warning to implementers.

Alice: I asked Tantek for examples of how this intersects with web standards & API design - haven't seen an answer - we can agree that dark patterns are bad but what can we do about it?

Amy: An example from a spec I've worked on ... activitypub, you have some numbers like likes, followers, reshares etc... looking into de-gamifying that, make it a more respectful place.

... Some of the activities are "like", and you can have a "total" for that.. and if we had had this guidance then, we might have done something different.

Dan: One of the things we've done around speaking to people that are writing, developing and designing new web technologies... we've couched advice like that in terms of "technologies we build should not amplify, should not be aimed at amplifying these kinds of anti-patterns".

... Going back to secure contexts, it's an anti-pattern that information you provide, such as geolocation, might be accessible unencrypted, because it might be accessed by parties that you didn't mean to share it with. So we're requiring things like that to require secure contexts.

... Could apply that same thinking to this arena. Does that mean we need a statement about dark patterns? [e.g. "technologies we build should not enable or amplify dark patterns"]

Hadley: We could try for one, at least.

... I'm not sure what we currently say about our responsibility towards thinking about these things in advance

... I keep thinking about Tim talking about in the early days of email, and that you could receive emails you hadn't asked for, but nobody played through the scenario of spam. They could have attached a "policy paragraph" saying "this is out of scope for what we're building, but legislators might like to think about it". We've found other ways to cope with spam... but it feels like the person/people thinking about a new feature are in the best position to anticipate these kinds of issues.

Amy: And they have the responsibility..

... "isolation and addictive behaviours" section might capture the dark patterns issue to a large extent already

Hadley: Maybe... it's definitely relevant.

Alice: as someone in the API design camp - I'm wondering how would I know - can we provide examples of how things should not be done or things we've recommended against int he past or a thought process we go through.

Hadley: There's a process of brainstorming and prototyping and coming up with your thing, writing your explainer, getting other collaborators and implementers, getting TAG review... around that time, when you've got a relatively good idea of what the design is...

Amy: It's a dystopia avoidance questionnaire

Dan: Is the technology featured in a Black Mirror episode?

Alice: philosophy of technology - speaks to how science fiction shows how tech can [be misused]

Amy: Larger project around this... when your working group is being chartered, a study of the potential effects on marginalised communities.

Dan: Vulnerable communities is often where we see the blind spot... things seem great until you talk about marginalised communities, like the real names on social media argument.

Hadley: That's a great argument we can reference externally.

Dan: Issue 25... doesn't seem like we need a new principle; as Amy pointed out, the original principles capture some of the issues. But maybe we need to capture something about dark patterns or "dystopia avoidance". This is already quite a long principle... could we consolidate the wording in this principle a little bit and have it say more of this stuff? Then we could close out this issue.

... We could specifically talk about vulnerable groups or marginalised communities... or unintended consequences.

Amy: Unintended consequences could be a principle on its own...

Hadley: That would draw it out and make it more explicit. 

Amy: "The web should not cause harm to society" does mention vulnerable people.

Hadley: A paragraph in the intro or somewhere else... I learned to drive at 16 and got a booklet from the DMV saying "these are your responsibilities as a driver", and I read it from cover to cover, and I felt like I'd been introduced to what I was taking on. We don't do anything similar for anyone who wants to design a web feature.

Dan: That's kind of what the design principles is meant to be... to the point that some have made that the design principles is too long...

... I'm in two minds about adding a new principle. I think we should be conservative about adding new principles. Wording about unintended consequences would be a good thing. Sometimes the consequences aren't exactly unintended. 

Lea: Intent is the difference between a poorly designed feature and a dark pattern.

Hadley: I created a PR about not mentioning advertisers explicitly, and didn't attach it to an issue... could we get that sorted.

Dan: Amy can you own this issue?

Amy: Yep, I can take it.

Dan: Was that issue 32 about clarifying the priority of constituencies? https://github.com/w3ctag/ethical-web-principles/pull/32/files

... All of our documents are riddled with the term "users"... I'm receptive to the argument that the term "user" is not that great. Maybe that's a separate issue. 

... When we talk about user needs, we think about the end user... people that are in the advertising community might take that to mean advertisers... advertisers are users... anything "above" a certain level is in "user space", I think we should be more explicit about people.

Hadley: Changing users to end users is out of scope for the PR.

Alice: Could we be more specific about "advertisers"? Advertising companies, companies which advertise, sites which host ads?

Hadley: All of those should be less important than the needs of the end user.

[discussion on advertising and what we mean by advertisers in this context]

Alice: [example of "distracting" label]

Alice: tech that helps advertisers know when an ad is viewed - it's a benefit to users in terms of performance but only because the page needs to run ads in order to make money and the way that revenue flows from advertising is to know when an impression happened.

Hadley: ... at the expense of the end user's privacy...

Alice: from an ethical PoV do we say "this is going to harm the end user" - systemically it harms the end user.  Like: if you have a specific event for knowing when user is using assistive technology. It has some user benefits but entrenches advertising... But without advertising publishers would suffer. 

Hadley: do we have fundamental problems with the ad ecosystem?  and/or are we saying that there will be ethical dilemas...

Alice: if we're going to mention advertisers we should say something about it.

Dan: would it make sense to say something that encourages ethical advertising? Advertising is part of the fabric of the world and part of the problem people have is the way in which web advertising breaks privacy and the bad practices. advertising itself isn't necessarily the problem. Encouraging a more ethical approach to web advertising might be something we could put into this document. 

Hadley: we would need to flesh out what ethical advertising means

Dan: there's a proposal about private click measurement now, measuring when someone clicks on an ad but trying to do so in a way that doesn't use third party cookie tracking. Feels like there are proposals out there that are trying to achieve that goal.

Hadley: be great if we can find some more time for this..



## Breakout 10a:

Present: Lea, Amy, Dan, Alice

### Design principles 2

[Reviewing the minutes]

Alice: anne and lea have left comments on the PR in question ([262](https://github.com/w3ctag/design-principles/pull/262))

Dan: let's look at untriaged issues

... a whole bunch of things starting from 245, everything from there up doesn't have an owner. Alice, do you have a sense of priorities?

Alice: the one about formal grammars, Anne commented with some examples, that would be an easy first PR for someone. Inclusive naming choices looks interesting. Some editorial. WebIDL...

Dan: from May 16th, incorporate some of CSS2 design principles [#188](https://github.com/w3ctag/design-princples/issue/188)

Alice: I think David did do some of that

Dan: that isn't reflected

Lea: some of these generalise beyond CSS

Alice: the HTML ones are the same, some are right at thet op of general design principles. We should just generalise whenever we can

Dan: I'm going to leave a comment asking David whether he thinks we can close this

Alice: you might be write, maybe it hasn't been done. We have prefer simple solutions which is analagous. Device independance we have a principle for that. Complimentary to structured docs, that gets into separation of concerns. Flexibility seems very generic. 

Lea: I'm not sure how that generalises, it seems specific to CSS

Alice: it could go in our CSS section. I'm not sure how you apply it to a specific API. It's more of a feature of the design of CSS as a system.

Lea: not sure this is a design principle, it seems to describe CSS more.

Dan: the HTML design principles and the inclusion of those in the document, there was also a discussion on twitter with tobie langel which was about clarifying the relationship between our design principles and the HTML design principles document. WHich he put [into a issue](https://github.com/w3ctag/design-principles/issues/160#issuecomment-766342618).

Alice: Tess replied that the intent is to fold them into this document
... I think Tess has done a lot of work on that already.

Dan: Do we need to clarify that in our document itself? There's not much we can do about the HTML design principles document but we could put somew ording in to say to make that explicit. We do reference the document, I think?

Alice: at the bottom in the acknowledgements
... There are open issues linked off this about backwards compat [17?]() and separation of concerns [169](). 

Lea: they are also part of CSS design principles, they should be generalised

Alice: I think we're rewriting them from scratch in any case and using that as an opportunity to revisit 
... on my agenda for tomorrow is to look at separation of concerns specifically.

Dan: Are you going to write a PR in that session?

Alice: hopefully

Dan: maybe it makes sense for us to focus on other areas

Alice: any input you want to give on it that would be great, if not let's look at something else

Dan: in terms of trying to assign issues, I think if 188 incorporates some of CSS2 is that something Lea might want to be assigned?

Lea: I could give it a shot

Dan: assigning it doesn't necessarily mean you have to write something, in terms of keeping it on your radar

Lea: Sure

Dan: I'm going to go through the unassigned issues so we can assign things.

... 203: Require device identifiers to be origin unique. Raised by Sangwhan .. assigning Sangwhan.
... 212: extend other API considerations to include expanded impacts. From the community. 

Alice: echoing what we were talking about earlier. Section 9, other API design considerations. 

Dan: I could link it to the issue we discussed in the ethics session, the dark patterns issue.

Alice: dark patterns is sort of specific, this is more general

Dan: I'll take this one. Assigned it to next week.

... 213: discouraging novel microsyntaxes, raised by Tess... assign it to Tess.
... 216: WebIDL is for APIs exposed by browser engines. This might be something for Tess.
... 231: when APIs that take a buffer are considered ok. Lots of discussion with no TAG members. Any ideas?

Alice: it doesn't seem to give any negative cases, where passing a buffer is bad. Anne's introduction talks about solutions for perf sensitive APIs.. none of it is about when not to use it, which I guess is by default or when you wouldn't run into the issues mentioned in the second comment. Feels like something Sangwhan would have opinions on. I'm going to assign Sangwhan and Tess.

Dan: 245: guard against recursion section si very long, opened by Alice. This came out of discussion of merging editorial changes.

Alice: it is such a specific problem and it's over a page of content. Lea, did you read this entire section or did you skim it? 6.6 in event design and 6.8 is longer

Lea: I don't remember thinking it was particularly long, but it was over 2 weeks ago..

Dan: it doesnt' seem particularly long to me. There's an example which takes up a lot of space.

Alice: if you look at 6.1 t 6.5 each is a short paragraph and an example, so it is disproportionate compared to the other ones. It's not that we need to cut it shorter, it needs to be that long, I tried, but I'm wondering if it could be a standalone document like promises. Maybe the answer is no and we close the issue.

Lea: I don't think there is a problem here.

Dan: the problem might be with readability and the evenness/consistency of how much material is in each section. One of the ways to mitigate is this idea of a design principles checklist/summary/flash cards that makes them more digestible

Alice: compared to principles near it it goes into a lot of detail

Dan: maybe we need more detail in the other sections...

Alice: or maye we don't.
... That one and events vs observers really stood out to me. A level of detail that most of the other principles don't have. It's a little how-to as opposed to a principle. If you want to go ahead and create a companion document that we keep up to date, or a tiktok channel, go ahead. I fall back to lets keep things in one place and make that one place accessible. 

Dan: I agree

Lea: what if it can generate it so we only have to maintain one thing, if we can generate a summary from the design principles.

Alice: Sangwhan had a go at generating a brief version from headings and first sentences. 

Lea: where is that?

Alice: a proof of concept

Lea: it sounds like a good heuristic, we could annotate different sentences to be the summary

Alice: writing the first sentence as a summary is good practice anyway

Lea: Is there an issue about that?

Dan: not about creating a summary, there should be

Lea: I think I saw something somewhere about a cheatsheet during design reviews, but I dont' remember where.
... maybe opened by Tess?

Alice: Rings a bell
... issue 154 assigned to Tess in design-principles

Dan: coming back to the recursion, I want to close this off. I don't know .. I want to change it to both that section and the events vs observers section maybe need to be condensed, an editorial pass.

Alice: good luck. I really tried. You can also try.

Dan: maybe we should just close this.

Lea: I vote for closing

Dan: 179: discuss searchability and naming, added by peter. 

Lea: I'm not sure it's a good idea to go with overly long names for searchability, context can be added to search itself

Alice: doesn't have any examples of good or bad. Assign to Peter?

Dan: Yeah. Adding a comment.

... 177: rethink information architecture, opened by Alice

Alice: for example, splitting long sections out into their own documents.

Lea: one thing to take into account is some are only useful to spec authors designign web tech, but a lot are useful more broadly to authors as well. Is this something we should highlight in some way? I would like ot see authors also referring to some of these design principles, a lot of themw ould benefit. Eg. naming. All the naming princples apply to developer code as well, not just specs. Other things like WebIDL doesn't apply to developer code. Or even getters vs methods, can also help with author code as well. Most of CSS stuff doesn't apply. In general it's a mix. A lot of the JS API stuff applies to author code as well. I was thinking maybe there could be some sort of annotation that allows us to generate a subset of design principles targeted to authors. 

Alice: like the HTML spec has?

Lea: exactly

Alice: new issue and assign it to Lea?

Lea: Okay

Dan: really good idea

Alice: link it to the architecture issue

Dan: Alice filed this in may, since then a lot of work has been done, should we close 177?

Alice: i was going to suggest that. We didnt' really change the structure at all.. no, it still needs some thought. Someone who is fresh to the document might be able to have some thoughts

Dan: should we do a survey of readers? Actually do a survey of people who are writing specs and ask them for feedback on the design principles?

Alice: what would we ask?

Dan: for specific feedback on categorisation, were the sections helpful, would you suggest other sections, did you feel like things were miscategorised? with a specific focus on information architecture of the document. Anything we could do to organise the information to make it easier to us. Also in general when engaging with the design principles do you read it or do you use it as a reference?

Lea: many people would read it first and then use it as a reference

Alice: that's what I would hope

Dan: maybe we should not close this issue for now, but assign it...?

Alice: might be nice if someone who is a content specialist could take a look at it. Someone with actual expertise. Do you know any tech writers?

Dan: MDN/open web docs

Alice: if we could pay someone to look at this that would be phenomenal. Making clear that the intended audience is primarily spec authors and TAG members, and secondarily web developers in general. 

Dan: I'll take this one

Lea: 251? I'm not sure if it's something we should address, or on the side of allowing custom properties to be more powerful. It's a good guideline, I would not want to see the guideline be changed just because custom properties are not that powerful. I have been doing work in CSS WG to help address this. Until it is addressed ins ome way we should have a note or something. Not sure where the design principle is, there's no link. It could be either in design principles or in the guidelines for web components authors.

Alice: it might have been that

Lea: it must be in the one for web component authors. Is it off topic here?

Alice: [TAG finding Guidelines for creating web platform compatible components](https://w3ctag.github.io/webcomponents-design-guidelines/#native-html-elements)

Dan: do we need to have a principle that talks about this that references the finding and incorporates Lea's additioanl text?

Lea: that would make sense. The design principle can't really bea bout custom properties unless we explicitly ack that the design principles are aimed at authors as well. right now they're all structured around writing specs. Spec authors do not define custom properties. It's a generally useful principle to define properties instead of attirbutes for styling, but doesn't come up very much in design reviews, spec authors don't do that any more.

Dan: we need to think more about where it goes, we generally don't amend findings. If we want to do something more on this.. We can amend the findings.

Alice: we found the wrong thing

Lea: findings can become stale

Dan: we haven't done it in a while, but it's fine. We should referencei t from the design principles. It comes back to your point about design principles being relevent to web content authors as well as web spec developers. This is a very good example of that. 

Lea: A lot of guidelines in this document could make good design principles

Alice: we have design principles for CSS and JS and less for proposing changes to the HTML spec

Lea: I think there should be a section for HTML just like for CSS and JS.

Alice: file an issue and take a break.

Lea: Issue about creating an HTML section? Okay I'll file that. (filed: https://github.com/w3ctag/design-principles/issues/269)

## Breakout 10b:

Present: Sangwhan, Ken

#### 431 [Web Serial](https://github.com/w3ctag/design-reviews/issues/431)

Propose close

#### 512 [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512)

Dependency on digital goods, asked if Tess has issues with the feature

#### 580 [Limit allowed "accepted" extensions in File System Access API file pickers](https://github.com/w3ctag/design-reviews/issues/580)

Looks sensible, but none of us have ever see .c++ file extension

## Breakout 11a:

Present: Kenneth, Peter, Tess

#### 532: [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532)

#### 542: [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542)

#### 544: [Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/544)

## Breakout 11b:

Present: Rossen, Dan

### 462 [WebXR Augmented Reality Module](https://github.com/w3ctag/design-revieWebXR Augmented Reality Modulesues/462)

Dan: privacy & security considerations section is a bit small.  The API allows access to the camera image for use in compositing - however does not allow the web site to access the actual camera image.  I think it should be clearer from that section about why the web site doesn't get access - also this is non-normative so is this a requiement of the API or is it an artefact of the implementation?

Rossen: let's say we have a simple scenario - we want to try a new couch and place it in my living room.  In the AR subsystem - it receives an object (a model) that reprenets the couch and it handles everything else.  From this PoV the only interaction between the browser and AR subsystem is a black box iframe.  So is the opposite direction possible?   Can the web app say "well the couch doesn't fit" - so if I provide that info back to the site, that is PII.

Dan: that also needs to be called out in the privacy & security considerations ...

Dan: 2.5 needs some example code to show what is going on - and to clarify the use of the word *Content*.

Dan: I note there is a requirement (normative): "The XR Compositor MUST NOT automatically grant the page access to any additional information such as camera intrinsics, media streams, real-world geometry, etc."

Rossen: so it is a black box.

Dan: yes - however I still think this needs to be expanded on in the privacy & security considerations section.

Rossen: so your session capability allows you to determine if AR is supported - you can create a session - if successful you can use it in 1 of 3 mondes - opaque, adaptive and alpha-blend. 

Dan: I think we need more clarification on the types, opaque, pass through and additive light and how they fit together with opaque, adaptive and alpha-blend?  

Rossen: and also how is Opaque AR?

### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528)

Rossen: The last comment added by Rik is what was missing. With that information we can have a clear expectation of the texture lifetime management and why this isn't a vector for security concerns.

Rossen: propose closing this.

Dan: A-OK

### [Web Share API](https://github.com/w3ctag/design-reviews/issues/554)

Dan: It is a duplicate of #117 however that was a review from when it was in WICG. It's now in WebApps.... 

Rossen:  We could close this as a dup and move on.  Or if they are getting close to a transition along Rec status - then we could view it as a transition review.

Dan: 3rd option - we could ask the requestor what is the delta, if any, between this and where it was in in 2017 when we reviewed it in WICG - and therefore is there any benefit we can provide for the delta?

https://github.com/w3ctag/design-reviews/issues/179#issuecomment-306526807

Dan: it's exactly the model we have been promoting - specs that move through incubation in a CG or WICG and then move to a formal working group for standardization.   Also it has multiple implementations see [caniuse](https://caniuse.com/web-share).   This is a success story.

Rossen: Added comment.

## Breakout 11c:

Present: Amy, Hadley, Lea

Topic: https://github.com/w3ctag/ethical-web-principles/issues/19

Lea: This could actually be useful for the design principles too
Hadley: I propose we go through the principles and we come up with examples from our experience
Amy: I should dig up my thesis, I had examples there
Hadley: That would be great, it would be great to have examples that come from our community
First principle, we don't isolate large parts of the web, it's meant to be one thing that's more or less technologically the same, people should be able to view web pages from anywhere connected to the Web. 
Amy: How does that relate to certain countries blocking certain sites, GDPR etc?
Hadley: I was talking more about network level blocking than e.g. websites seeing you're in the EU and suggesting the EU site
Lea: But what about the more common case where they force redirect you to the EU site, blocking you from accessing the other ones?
Hadley: Should this be in scope for this principle?
Lea: Not sure

Hadley: Let's move on to "the web should not cause harm to society"
Amy: dystopia avoidance
Hadley: Recognizing we have a lot of power in what we do, what we do with that power. ...priority of constituencies..., open processes really matter, we've been frustrated before with closed communities
Amy: or specs behind a paywall
(discussion about paywalled specs, joint specs etc)

Amy: Should we replace "end users" with "people" everywhere?
... a lot of criticism about this word by people outside W3C, it's indicative of toxicity
... should I [open an issue](https://github.com/w3ctag/ethical-web-principles/issues/34)?
Hadley: Yes
Lea: Yes

Hadley: "The web must support healthy community and debate", harassment, persecution, gamergate, bot farms on Twitter, anyone of any minority background or position of power feeling these communities are not for them. Dan was keen that we not exclude social media platforms from the scope. Twitter being part of the platform, not using web technologies in any way that misuses anything that's written in a spec.

Amy: There's the Credible Web CG
... I took over chairing recently, and we need to formally adopt a CoC. There's the W3C one, it explicitly says you cannot discriminate against political views, but we are worried about influx of (basically) nazis. We need to find a way to perseve the right to refuse them
Lea: This sounds like a bug in the W3C CoC, it should guard against the issue raised by the paradox of tolerance
Amy: It's a fine line though
Hadley: We can't discriminate based on political views, and we shouldn't. The problem is not the views, it's their actions. For people who are coming and disappearing, it feels like a chairing challenge, we need to make sure that everyone gets a balanced view. There should be some things that people are doing that are inappropriate and grounds for removal. The more we can ground those in this is bad for the web or the project, the better.
Amy: I should write community guidelines that we don't tolerate this
... People in the community whose very presence is harmful, it could make other people feel unwelcome 
... I would be upfront and explicit about community values
... we've already had obviouslt alt.right people on the forum, on mastodon
Hadley: I hear you, but I'm very concerned about anything that sounds like it leaves discretion to the chair. I think you might do better to look at the deprioritization features for campaigning (?)

Hadley: "The web is for all people" inclusivity at a functional level, i18n, localization, how we create specs, the sort of nudge to all of us who get lost in our privilege, that we all have moments to remember that not everyone else is on the same platform
Amy: [Blog post by Terence Eden about importance of websites working on low bandwidth](https://shkspr.mobi/blog/2021/01/the-unreasonable-effectiveness-of-simple-html/)

## Breakout 12a:

Present: Dan, Rossen, Peter, Amy


#### 574: [WebXR Lighting Estimation](https://github.com/w3ctag/design-reviews/issues/574)

Dan: the XR stuff is notable for one of the risks being that it might make users physically ill, if it's implemented incorrectly, time lags, if the VR doesn't match head movement, there are actual real risks.

Rossen: seizures if done badly, it's very hard getting it right

Dan: thumbs up on [security and privacy questionnaire](https://github.com/immersive-web/lighting-estimation/blob/main/security-privacy-questionnaire.md), they did a good job

Rossen: we don't consider this to be exposing underlying platform config information do we? They are saying none. In general, do we consider hardware capabilities of underlying platforms as config data that is exposed?

Dan: so whether the platform itself supports this api at all?

Rossen: can I use this to fingerprint devices? in a different way that I couldn't before. 

Dan: yeah, that could be expanded on here.

Rossen: I am assuming that they will probably come back... this is exposing lighting capabilities

Dan: there is a section in p&s considerations that says lighting estimation provides additional opportunities for side channel attacks and fingerprinting risks, discussed in [this section](https://github.com/immersive-web/lighting-estimation/blob/main/lighting-estimation-explainer.md#security-implications)

Rossen: it's great that it's there but not mentioned in the privacy questionnaire

Dan: They should have pointed to this section, they do link to it from the security and privacy self check response. Their mitigation against the fingerprinting risk is that the XR light probe should only be accessible during an active webXR session, that's one mitigation. 

Rossen: the rest is pretty straightforward. There's not a whole lot that is being exposed.

Dan: there's good information here about the .. it says in the explainer the mitigations against fingerprinting but looking to see if that information is reflected in the actual spec itself. There's a MUST in the explainer but that text does not appear in the spec. It probably does but using different wording.. it's not specifically called out in the privacy and security considerations section of the spec (which is non normative). That's one piece of feedback.

Rossen: you want to summarize this?

Dan: yeah. Other feedback?

`
Hi XR folks! Thanks for this review request. We note that the response to privacy & security section is great. One thing we felt was missing was the mitigation information on fingeringprinting - which is actually discussed in the privacy & security considerations section of the **explainer**.  And it also seems like there are requirements in the explainer - e.g. quantization - which do not actually appear in the spec itself? 
`

Rossen: from my point of view it's really straightforward. The use case is valid. If you don't get light correctly then your experience sucks. 
... I would add from a functional point of view the proposal seems like a great addition to XR

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/574#issuecomment-768431095)


#### 595: [Same party cookies](https://github.com/w3ctag/design-reviews/issues/595)

Dan: what is the status of this work?

Peter: tied to first party sets

Dan: there was significant pushback from other parties, was discussed in the PrivacyCG. I think the tie in is it's using the same conceptual framework

Rossen: it builds on it. Are we assuming that first party sets are a thing?

Dan: our [review of first party sets](https://github.com/w3ctag/design-reviews/issues/342) is closed - and we identified issues which were not resolved to my knowledge ... [Mozilla thinks its harmful](https://github.com/mozilla/standards-positions/issues/350).

Rossen: the first party sets itself is problematic. It says we don't trust who is first and third party, we will tell you who is first party, we are going to group domains to say they are first party, trust us. Based on this proposal is extending it and we'll also tell you what third party cookies are on top of this first party sets. In the security and privacy, they are going to good detail to what the different proposals are.

Dan: I want to push back and say before you start building stuff on top of first party sets then asking the TAG to review it, get yoru story straight with first party sets and get consensus and multiple implementations behind first party sets. this is not a thing where some browsers can support it and some can't and that's okay, this is much more fundamental to how the web operates. If you don't have inteorperability it's not going to function and there's something to the notion it might be a harmful feature.

Rossen: No official MS position, I have my personal opinion that doesn't stand for MS.

Dan: where is this being worked on?  In a private repo.

Dan: proposed comment
`
Hi folks - this is an interesting proposal.  We are just picking it up at our virtual f2f this week and discussing. I note that it builds on First Party Sets, which we previously reviewed and found issues with, which were not resolved. Furthermore there seems to be lack of multi-implementer support for First Party Sets based on e.g. the Mozilla feedback. Therefore it feels to me like it's premature to build things on top of First Party Sets?

`

#### 575: [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575)

Dan: it's shipping behind a flag [on Samsung Internet].

Rossen: these scenarios are supported in Surface devices

Dan: [privacy issue](https://github.com/w3c/screen-fold/issues/45) came up about knowing the angle. Some mitigations suggested and ongoing discussion on this issue. Talking about removing the angle itself and having access to different postures, rather than knowing specifically the angle that the screen is folded at

Rossen: that's closer to the previous MS proposal which had a few different modes that you're in, then based on those its' split screen or not, etc.

Dan: this work is ongoing, it may be premature to be doing a TAG review

Peter: I don't think so. I have some major issues with this, I think it's going the wrong direction. This has come up in CSS before. One is that this and almost everything else on foldable screens is very tightly coupled to existing screen tech and mobile devies. It's not forward looking at all. It's a matter of time before someoe makes a device with two hinges. An ipad with two smaller screens that fold out and aren't the same size, it's going to happen. 

Rossen: more than one hinge as a forward looking issue, and that screen size is not necessarily homogenous in this example?

Peter: Yes. Third at some point in the future screens ize will not be static, rollup displays with pulling out as much screen as you want. It's been done in scifi so you know it's coming in reality.

Dan: there was an article about rollable screens

Peter: rolling or stretching

Dan: you could say that about almost anything that comes through w3c. I remember having the same argument about PWAs and the idea of a manifest and having an icon and peopel arguing that's so tied to the way people use smart phones, yes, but also there are many things about the way we use the web that are tied ot particular tech, liketouch screens, why have a touch api when we can be talking about generic interactions that could also allow for thought retrieval

Peter: that's pie in the sky, this is something we already have counter examples that are coming within a year. These APIs are very narrow and should be a bit more broad. My other concern is that it's not dealing with the desktop scenario at all. I'm sitting in front of 3 screens, two at angles. Why can't that be represented, why isnt' it in that API?

Dan: valid concerns. My concern, one of the reasons Samsung is interested, is how do we enable the developer access to that informations o they can make a choice ot create a user experience that fits that form factor. One of the things you can often do, that many applications that ship with the folding Samsung phones do is change the UI when you start folding the screen. There's an animated transition. When the phone is out and you're looking at the camear you might see the whole screen is the camear but when you start to fold it changes so the bottom is the controls and the top is the image. This is about enabling that on the Web. That's the goal. If we can comment back to the spec authors in a way that is encouraging and says if you take this into account you can achieve those goals while also being more forward looking to future display, that's very valid.

Peter: not just forward looking, past lookinga s well. I have a friend with 4 screens in a 2x2 grid. If the window spans the gap in the screens why shouldn't the web app know that?

Dan: this is different because there's a dynamic element to it. In the case I described you're in the same application. Your application might want to detec tthat and change the UI accordingly.

Peter: in a desktop scenario and drag the wndow the app would want to adapt in the exact same way, and use the same API to do that. Desktop is still a dynamic environment, it's the window moving not the display moving. 

Dan: I see them as two different htings partially because of the mode of operation. Having it in your hand is a different kind of thing. This is a mass market case.

Peter: I don't want to pander to a short term mass market device with a lifetime of 2 years and ignore 20 years of legacy on desktop and 20 years of future mobile. The relatinoship between the app window and the screen is the same problem is whether it's the window moving on a fixed device or the device moving on a fixed window. It should not be a different api or developer experience or user experience for that.

Rossen: On principle I agree with Peter, in terms of future proofing, not as much as designing for the future as much as not blocking future designs by default. I'm not in favour of asking the authors to go and say tell me how it's going to work on a scroll. A little too far. But it should be fair to say if we had a scroll will this scenario prevent anything. Perhaps not. They can say if your scroll is not folding then this API is not going to kick in, we're not doing anything to prevent it.

Peter: in that case the screen seize is changing dynamically. I'd like to see an API for the screen topology not just the screen fold

Rossen: we're circling the same point, there is a lot of legacy and present that is developing, however you look at it a lot of the capabilities on what we have on the web today which are device centric, are driven by devices, we are always playing catchup with the current underlying OS. So we've been shipping OS capabilities for 2 years now that allow develoeprs to build native apps that take advantage of screen folds. So my question is how long do we keep the web from being able to use that? To hold our high bar of making the Web more pure. There must be a balance there where we allow the web to quickly catch to device capabilities while not fully handicapping ourselves for what's next.

Peter: I agree. My concern with the existing API shape is it is making presumptions about a single fold and a single direction and that's clearly inadquate. The other thing is this is device driven and thsee devices evolve rapidly and become obsolete rapidly. This is not goign to get to rec in 2 years and what's going to be new and shiny in 2 years?

Dan: I don't knwo if I agree with that. We've had stagnation in device design, industrial design, for years now. What I see happening is Apple is supposedly looking at foldable displays, foldable display itself is a new.. it's hard to say if it's a fad or not. Really  hard to say. It is qualitiatively new and different. it has been proved to be manufacturable at scale. A scroll or wrinklable screen not so much. 

Peter: we don't have to plan for arbitrairly wrinklable surfaces, but this doesn't plan for thing sthat have been proven to exists

Dan: multiple folds is valid feedback. We should be feeding back somethign that helps them but doesnt' block them because otherwise we are holding back out of purity

Peter: I'm not saying don't do this, I'm saying this approach is inadequate, so rethink it a little bit so we can move forward in a way that can be extended in a way that handles future tech and past tech that hasn't been considered yet like multiple screens on desktop. When some of these early fold proposals came to CSS it was around MS devics with a physical hinge, and that is a tech constraint that is likely to go away really quickly, so do we want to bake taht into an API for the web.

Dan: Leave some of that feedback on the issue and get the discussion going

## Breakout 13a:

Present: Alice, Tess

### 573: [DOM Review Draft — Published 15 June 2020](https://github.com/w3ctag/design-reviews/issues/573)

Alice: Opening each of the changes they listed in order.

... [Define ParentNode's replaceChildren()](https://github.com/whatwg/dom/commit/3a11492f09212c944a1b495c47ce3c850136b296

Tess: This just seems like a win.

Alice: Agreed.

... [Avoid enqueuing a tree mutation record when there is no mutation](https://github.com/whatwg/dom/commit/d4535b467b793d450c1fb3e61d4956503b6a2515)

Tess: This just sounds like a bugfix.

Alice: What's the assert for?

Tess: In case there are other callers to the "queue a tree mutation record" algorithm.

Alice: Makes sense.

... Actually looking at the bug, it's making the spec match implementations.

... [Use self.origin instead of document.origin](https://github.com/whatwg/dom/commit/55379a77690afcc656728179d4e828373952c870)

Tess: It's redundant with `self.origin`.

Alice: What is `self`? Oh, it's synonymous with `window`... https://developer.mozilla.org/en-US/docs/Web/API/Window/self

Tess: Looking at the discussion on this bug, it seems good... removing something that's now only in one engine, and is redundant with something that's implemented everywhere.

... [Replace child text content change steps](https://github.com/whatwg/dom/commit/ce4c6ba5b6e8e26e9c0e6f157243df9942d8b52a)

Alice: What is hr-time? 

Tess: High-Resolution Time. It was removed because of Spectre... now being added back.

... They replaced "child text content changed steps" with "children changed steps". It's a spec organisation question. Bikeshed would catch any errors where something is referring to the old steps.

... [Address infinite loop in TreeWalker's nextNode()](https://github.com/whatwg/dom/commit/868f1734717c791261e75687ba3ce12bfedfae8e)

Tess: Sounds like a great bugfix!

... [Change add/remove event listener behavior for service workers](https://github.com/whatwg/dom/commit/7a48d64b41c586afc2e57d25eab99e8cfba5de1a)

Alice: ... ok

... [Define the onabort event handler IDL attribute](https://github.com/whatwg/dom/commit/e017c7ad4c24d9870f4029564d820243d90cf4c6)

Alice: Great.

Tess: Good bugfix.

... [Add the DOM XPath interfaces](https://github.com/whatwg/dom/commit/dea5d92156f144faf57d1a5e54a17227139ca3c5)

Tess: This is where browsers have a weird subset of an old version of XPath, and nobody wants to specify it.

... So now DOM is going to define it, and this is the beginning of that work.

Alice: Looks good.

... [Add StaticRange constructor](https://github.com/whatwg/dom/commit/a93f9f8be626740f6ac4a459bfb28322e27646d1)

Alice: Apparently this one was our fault. "Somehow StaticRange got added to browsers without the TAG noting the lack of a constructor. #589 adds StaticRange to the DOM Standard."

Tess: It's good that they're fixing it. 

... The algorithm steps for the constructor don't do much validation, which is good because the code that handles them handles invalid ranges already.

... [Catch errors while upgrading customized built-in elements](https://github.com/whatwg/dom/commit/543b7e33487be5e733b0a715eaf71d027e354a50)

Tess: It's just adding a try/catch, more or less.

... [Avoid enqueuing "disconnectedCallback" on detached custom elements](https://github.com/whatwg/dom/commit/de29633694822f4fd0bab61a2d142de2298dc88b)

Tess: Another bugfix.

... [Add delegatesFocus to attachShadow and flag to ShadowRoot](https://github.com/whatwg/dom/commit/4cf85efcbc22cc25a0917ceb18deac8b8f3e9246)

Alice: Doesn't define what it is, but it's defined in HTML.

Tess: I wish the DOM spec did a better job of explaining those external dependencies.

... this looks fine.

... [Define the onslotchange event handler IDL attribute](https://github.com/whatwg/dom/commit/a6c6d984e756ad099624350f62c97ab902956cce)

Alice: Just adding the idl attribute.

... [Run adopt as part of insert](https://github.com/whatwg/dom/commit/c825ceaf3cb77943f487f85533d8be79bccd2fe3)

Tess: Issue boils down to a concern about DocumentFragments, and that's what gets fixed in this PR.


## Breakout 15b:

Present: Alice, Dan, Lea

Dan: Would like more information about things coming into our design review process from Blink engineers.

... 2 failure modes: one where our input is required urgently, another where our input is no longer relevant.

... 

## Breakout 16a:

Present: Lea, Ken, Sangwhan

Lea: Why this complicated object structure based on what parts of the date you have? This means that as a user fills in a date in a UI, you have to keep converting between objects. Why not have properties that can be undefined when not available? This means cognitive overhead every time you want to calculate anything about dates, because you at the very least need to decide what object you need.

Lea: Also, why have so many factory methods instead of constructor overloading? I seem to remember there was a note on why, but can't find this now. But it's poor DX if you create objects by using the constructor sometimes and the factory methods sometimes.

Sangwhan: Can't do math on dates easily

Sangwhan: Don't quite understand the rationale behind using the factory pattern vs constructor. Not sure how useful these "partial" objects can be. Why not have a single object that is missing some information? I'm sure they have reasons but it's not explained at all

Ken: And there's no explainer.

Typo in Temporal.Duration, it should say "seconds"

What's the difference between unit and largestUnit in duration.total()?

Temporal.Duration.round: Why does largestUnit normalize instead of clip?

Sangwhan: This is a powerful API but is "pointy". Beginners will not be able to make sense of this, and that's bad. 

Sangwhan: I'm not sure what's the use of creating your own calendar

Lea: This is optional in every method, so you can use the API completely unaware of the existence of calendars.

List of use cases??

Draft comment:

@cynthia, @kenchris, and I discussed this in our VF2F today. 

Since there is no explainer but only documentation & the spec, we missed a list of user needs, which would facilitate review. 

However, based on the documentation, we are concerned that while powerful, this API is very difficult to use for simpler use cases (see [principle of Least Power](https://w3ctag.github.io/design-principles/#simplicity)).

One source of cognitive overhead is the deep hierarchy of objects, the distinction between which is based on what information is available (e.g. day+month vs day+month+year vs month+year or types without a timezone and types with a timezone). Not only does this mean that when objects are constructed based on incremental user input, the developer will need to continuously convert between types, but it also forces the API to promote factory methods for object creation which need to be learned separately, as opposed to constructors. We were wondering about the reasoning behind this decision, compared to a single object, with some of its information `undefined` or `null`. 

While reviewing, we also spotted a typo in your documentation: in the [example here](https://tc39.es/proposal-temporal/docs/index.html#Temporal-Duration) the unit is probably `"seconds"`, not `"minutes"`.

## Breakout 17a:

Present: Ken, Lea, Dan

Talking about [battery saving](https://github.com/w3ctag/design-reviews/issues/546)

Lea: I think an opt-out would be better than an opt in...

Ken: one of the cases - a site that runs for a long time - like video conferencing - the site will say "please throttle me" - that doesn't make sense because no site will say that. The other one is - user is going into low batetry mode because they want to save battery. So now do something.

Dan: - similar to dark mode -

Ken: if the user decides - 

Lea: 2 features that might be throttled - one of them a media query. One of them is reduced script speed, however the UA reduces script speed in other cases too, e.g. when the tab is not focused. It seems that anything allowing aithors to respond to reduced script speed, should allow them to handle both of these cases at once.

Ken: giving an option of what should be throttled first...  I don't see this in examples.

Lea: It seems we have consensus that an opt in is not a good idea.  What about an opt out?

Ken: if you're a web site doing a background thing - e.g. generating pdf - then having a focus on webasm and javascript running as fast as possible is important. But not so much UI. For another site you want animation but background not so important.

Dan: So much of this depends on what the specific web app is.

Ken: yes. 

Lea: given an opt-out websites could set is as a boilerplate, defeating the purpose

Dan: [we don't need extra tech to do this...?]

Lea: instead of web sites opting in our out they could set a priority of features?

Ken: yes.  Or maybe ask me if I should throttle?

Dan: shouldn't that be a function of the browser itself?

Ken: yes - like detecting whether you are plugged into a socket or on battery... 

Ken: I think we should suggest prioritization... 

Ken: I think we should have a hint for power-save mode... low power mode...   Web sites that care about engagement would do something to conserve battery...  What can a site that doesn't want to lose their users do?  What does that site find acceptable to throttle.

Lea: 2 ideas - 1 - site to declaratively hint the priotity - and 2 - site to get an indication of whether user is in low power mode. Also, do sites need to react to energy savings, or to specific kinds of throttling, regardless of what causes it? (low battery, idleness, unfocused tab etc)

Dan: Privacy and security issues, but no response to questionnaire. 

[working on wording of comment](https://github.com/w3ctag/design-reviews/issues/546#issuecomment-769191105)

[Periodic background sync](https://github.com/w3ctag/design-reviews/issues/367)

Ken: Pending feedback and they are not responseive...


[hasDroppedEntry in PerformanceObserverCallback](https://github.com/w3ctag/design-reviews/issues/547)

Ken: this is about naming

Lea: the name is not something developers typed, it's a parameter

Ken: you should understand what it means, it means you didn't get all the data. I had no idea what hasdroppedentry meant. Means the buffer is full so they dropped some entries. How did they drop them? Last, first?

Lea: I think that's vague on purpose. Besides the name, is it a good idea as an argument? It's never called by developer code, but we do have guidence against boolean

Ken: I don't feel strongly, just wonder if people know what it means

Dan: what do you think abut it from a design perspective?  

Dan: nice to see that they have [filled out](https://github.com/npm1/hasDroppedEntry/blob/master/security-and-privacy.md) the security & privacy self check.

Ken: I think it's fine that you know something was dropped. Suddenly not understanding why some info looks different, it's nice to know it's because something was dropped. It might be nice to know more about how it's dropped. Nice ot know that something happened. Whether it should be an error instead, I don't know. It's like entries exceeded the buffer / buffer full.

Lea: one thing that gives me pause is I don't like adding these primitive positional arguements every time something comes up. What happenes next time something needs to be communicated to the callback? If someone doesn't need that arg they still need to capture it.

Ken: and if there's another one after it? You can use underscore in JS now.

... maybe it should be a dictionary instead?

Lea: yes, you can always destructure it. Then order stops being significant. The relevent design principle does and doesn't apply.

Ken: I think it's fine to point to it.

Lea: what about listTruncated for a name?

Ken: any way you can check the buffer size, if you had the list you could manually check the size.. no it would be full.

Lea: would it be useful to know how many entries were dropped?

Ken: potentially, especially in the future if you could set the size yourself. Maybe they add that to performance observer in the future, an optional dict and you can set the buffer size. That could happen?

Lea: it looks like knowing how many entries were dropped would mesh well with the goals. User agents optimising buffer sizes if they become full.. how many entries were dropped is significant for that. It's different if you have 1000 vs 1 entries dropped.

Ken: they have options when you call .observe. One of them is buffered. In the future you might get some way to set the size. It would be nice to know exactly how many items were dropped.
... I think it should be a dict because you might add other things in the future. Performanceobserver init gets a way to set the size of teh buffer and you might want to have other information about how many were dropped. numberOfDroppedEntries. Not both, just one. 

Lea: will leave feedback

Dan: milestone next week, then we can propose close after the feedback and response.



## Breakout 18a:

Present: Dan Rossen Tess Amy

Tess : we had a breakout yesterday  (14a) - it went well. 

Tess: [gives overview]

Tess: we went through open PRs - tried to move them forward and wrote PRs. and then looked for stuff that needs fixing.

Amy: been on the receiving end - in working groups that had to respond

Tess: there are parts of the questionnaire that feel like an interrogation.

Amy: the doc is focused on browser implementations so puzzling for people from non-browser world.

Tess: wondering if there is a way to subset the documet - "if it's browser then answer this - if not then youc an skip to question xx"

Rossen: any specific sections of doc that we should tackle?

Tess: Question 16 - downgrading default security characteristcs... Not sure what is going on here...

Tess: how can we help spec authors determine if a feature does this?  And no discussion of mitigation strategies... 

Dan: instead of listing the bullets out, it should say briefly how each one of those is an example of this and then it should have what the mitigation strategy of that thing is. 

Tess: like 2.5 - new state across origins - enough text and examples.

Dan: even if we had one of the bullets with more text it would be better than what is there now

Tess: [issue 102](https://github.com/w3ctag/security-questionnaire/issues/102)

Rossen draft for 102: `
Does your feature enable changes to default security protection?

Are features in your spec capable of allowing sites to opt-out of security settings in order to accomplish some piece of functionality? If so, in what situations does these features allow such security setting downgrading? What mitigations are in place to make sure optional downgrading doesn’t dramatically increase risks? 

Some examples of specs that do this kind of downgrading are: ...
`

Dan: And come up with some text for document.domain and [cors].


Rossen filed an [issue 116](https://github.com/w3ctag/security-questionnaire/issues/116) for adding to the front matter something about how browser-centric this document is

Mitigation for document.domain is to remove it: https://github.com/w3ctag/design-reviews/issues/564

Tess to work up a PR for this


## Breakout Rollups

---

### Breakout 01-02:

Present: Sangwhan, Peter, Tess, Alice, David, Rossen

Tess: 1a 

... Talked about 3 things... 

... Font Enumeration API, I took action some time ago to summarise our thoughts and write them up on the issue, so I went ahead and did that

... CAPTCHA issue, a little unclear what the next step is. Dan had reached out to Wendy to see if a workshop might be appropriate, no response yet.

... Modal close signals, this reminds me a lot of IndieUI, some of the AOM accessibility events stuff. Feels awfully complicated for what seems like a simple case. I reached out to James Craig to get his thoughts. 

... Peter noticed the way these modal close watchers get activated is by constructing them, which we thought was clunky, and an abort controller might work better. Action of activating is tied more closely to an API call. I think though we could just add an event.

Alice: What is the need for this?

Tess: The considered doing a synthetic `esc` keypress... on Android you have a hardware back button and the browser needs to know whether it means "go back" or "modal dismiss". If the page has created a modal close watcher, then the browser knows unambiguously

Alice: What does the user see when the back button is pressed?

... If you show a modal and they press back, for example on Android

... You would only close the modal if you listened to it

... Otherwise it would minimize the app

... Why not close by default?

Tess: You need a mechanism for the page to capture

Alice: So this entire proposal is to capture an edge case

Tess: IndieUI identified a bunch of abstract things for example hardware buttons

Alice: Seems like it would be about differentiating the back button intent to close the modal or go back

Tess: Using ARIA looks like a possible option to declaratively tell the browser

Alice: Seems to be against the ARIA guarantee

Tess: As far as the page is concerened nothing change

... the browser can do something about unexpected input

Alice: In AOM we suggested that increment/decrement events as ARIA roles

Tess: In this case they should send synthetic escape

Alice: I agree

Alice: 1b

... Virtual keyboard occlusions, trying to figure out what the next thing is

... we raised a bunch of issues, they closed most of them aside from visual viewport

... they indicated that it was sort of abandoned

... seems like it would be worth a conversation about whether the user needs align

... seems close to the intent of visual viewport

... the difference is that the visual viewport shrinks

... we talked about other occlusions probably necessary to be exposed to the application

... Sangwhan commented that there should be a discussion with visual viewport

... Declarative Link Capturing - a way to opening the app instead of a new browser window in a PWA

... early stage review, still a WIP

... we looked at it and seemed like a sane solution

... this came from the SW launch proposal, which has been slow to spec/implement

... new-client is defined as open a new window

... what to do when the underlying platform only allows one "app" at a time

... lots of options, which we'd like to know what they do

... we did thank them for making a simpler API

... did not get to the last issue (EditContext API)

Tess: 2a was Alice and me.

... Scroll-linked animations hasn't changed since we gave them feedback a while back. Alice gave feedback around triggering of vestibular disorders and the interaction with the prefers-reduced-motion preference. 

... That has been discussed at CSSWG but no conclusion yet, and explainer hasn't been updated in some months.

... Declarative Shadow DOM was a proposed close and we closed it.

... They had one question related to XSS scripting, but they had already come up with a good mitigation and documented the problem and mitigation well in their explainer. Looking to see if we had additional thought/analysis, but we were happy with their work.

... "Task" issue to review HTML spec's treatment of focus. Bigger project than we had time for.

... Alice wrote up a comment with some thoughts indicating potential future work in this area.

David: This was Rossen and me. We got to 2/3 issues.

... Formal review request for CSS Text level 3. Some previous discussion of this, but we concluded this has already had enough review and we propose to close it.

... One thing that it does that is interesting is automatic hyphenation, which only works if the site explicitly declares the content language. Web pages should do this, but they often don't. Automatic hyphenation is deeply language dependent and only works in the case where the language is explicitly declared, alternative would depend on the browser assuming the content language matches the user's preference.

... Performance ???

... Performance timeline metrics like first paint, first contentful paint. Sometimes meaningless if user switches to a tab after it loads in the background.

... Use case is sort of clear, question whether the thing they're reporting exactly corresponds to that use case or not. But I'm not inclined to keep this open just for that.

... Didn't get to the subframe/subresource issue, that seems to need a 1hr breakout on its own. At least managed to get the URL from when Tess and Rossen previously discussed this.

Peter: Did you mark that issue as free to be reassigned?

David: Not yet.

Peter: Should we add the language (explicitly declared language) thing to the design principles?

David: Possibly.

Sangwhan: we already discourage sniffing for MIME types etc, so it seems aligned with that. I'll open an issue on design principles.

David: The two issues are propose closing... should we close them now?

All: yes.

Peter: 2c: me and Sangwhan.

... Feature policy/permissions policy/document policy. Everything we had been tracking here had been moved to the document policy.

Sangwhan: Closed it.

### Breakout 03-04:

Present: Alice, Dan, Ken, Lea, Amy, Sangwhan, Hadley

#### 3a

Ken: we looked at the scroll box... setting color for scroll bar.  Lea said you don't need to set background color and color of knob.. system could calculate other color to ensure contrast.  Scroll indicators are popular on mobile but also desktop...  Some implement their own scrolling system. It would be nice if we could handle cases like that as well. We gave that feeedback and asked for additional screenshots.

... CSS container queries... asked are we able to nest media queries - we believe so but asked to clarify. Generally looks great.

Lea: One issue that ken pointed out - right now proposal suggests new keywards - we suggested logical and physical - based on width and height.

#### 3b

Amy: We looked at the "needs a service discovery" issue - we concluded that it was in Peter's court.

Amy: we looked at the digital goods API and left them some feedback....  How does it play into an ecosystem of many, diverse independent digital goods stores...

Hadley: big opportunity for decentralization...

#### 3c

WebXR FTW... 

Alice: We got through 2 - webxr DOM overlay module - we'd previously left feedback that explainer was hard to read.  They have improved it.  We left some comments.  Some specific feedback on the APIs.

... we looked at WebXR anchors - that explaienr was 100% better now.  We proposed closing for that one. [closed]

... We punted the others...

#### 4a

Lea: we spent most of the hour discussing what color format it should return...  It starts in  

Alice: lots of color space explanation

Lea: colors don't round-trip. Most modern screens support p3 - which is 50% larger than SRGB which CSS supports.  Today we are in a transitional stage where CSS colors can only specify SRGB but CSS Color 4 supports new color formats.  Problem is that CSS color 4 but implementation limited to webkit.  We also don't want this API to return a string.  We came up with 4 ways forward. (1) wait for a better state (2) return a srgb hex color and colors outside of srgb could be clipped - but won't round-trip (3) 

Dan: frustrating user experience...

[discussion on profiles in CSS and Canvas]

Sangwhan: I don't think Canvas supports...

Ken: they are working on the canvas thing... 

Sangwhan: [canvas](https://github.com/WICG/canvas-color-space/blob/master/CanvasColorSpaceProposal.md)

[discussion on examples]

Alice: any app that wants this will want high-def color in general. So waiting might not be terrible.

Lea: [leaves feedback]

#### 4b 

Ken: protocol handler - seems like nothing has happened so we asked for an update. We looked at installed related apps - and implementation story.  Dan left request for multi-stakeholder support... 

... we looked at windown-control-overlay - seems to be stalled - we asked a question.

... we looked at new open design-review issues. 2 extenstions for file system API - first is seeking beyond the end of the file...  this can be done with current API but cumbersome. They are proposing a simple fix and we propos closing.  

Sangwhan: zero-writing could be performance issue.

Sangwhan: i could look at the explainer...

#### 4c

Sangwhan: mini-app URL scheme chaged, and miniapp manifest - we are closing.

Sangwhan: next is webhHID - we are closing as we have been on this for a long time. We suggested that the app should request an exclusive... propose closing.

Sangwhan: min-app lifecycle - we didn't get to it.

... handwriting API... we provided some comments but didn't get into the details.  Questions on multi-lingual. Also question on API surface - why on `navigator` ?

### Breakout 05-06:

Present: Tess, Dan, David, Amy, Kenneth, Rossen, Peter, Lea, Hadley, Vyes

#### 5a

Tess: custom ... something ; looked at `aspect-ratio` property...  Overflow clip and clip margin..  no explanation of user needs.

#### 5b 

Hadley: Trust Token API - we were unsure about how much security research has been done... Fed back on issue and waiting for responses.  CORS-RFC1918 - we talked about how it's ipv4 centric - we asked about that.  and multi-implemneter - and what IETF activity.

Peter: I did look and added info on that to our issue. 

Hadley: we looked at 529 - geolocation API.  They hadn't written an explainer.  But the changes have been implemented in most browsers. Still some privacy questions... a normative section for sites receiving Geoloc data which sounds GDPR-ish and not something you would expect to see in a spec for a web standard. Other than that the review is stalled.

#### 5c

Ken: nav to unsigned web bundles... another proposal called resourcebundling - in colab with Yoav and Yaskin.  We asked if that replaces this effort. We covered pen event API - will file issues in their repo. Beforematch event - some accessibility concerns. 

Rossen: something already discussed - some followup sessions with Alice. I will ask at those. Main issue - by using the feature you can essentially render out valid accessibility scenarios .. if screen readers are expecting to have all the content available to them - this feature will eventually "click" all of them... There are some other developments ...  The feature itself belongs to CSS.  No reason to consider it as an HTML attribute.  CSS wg did not really accept it - waited for the TAG response first. 

#### 6a 

David: we had 2 things about credentials - we took the new one first - credentialless requests - proposal by Mike West - motivated by the SPECTRE mitigation stuff. Dan asked for a bit more explanation in the explainer. From my PoV it looks good.  

Dan: we talked around the background of withCredentials, Amy provided use cases from experience in Solid. My point is there is no open issue on fetch that we can really latch onto. All the issues.. there is one (878) which looks like it may be related, still open, but it is a wider issue than this particular thing and the question is if this proposal is not being entertained in the whatwg community then what's the role of us having an open issue on the TAG side? Is it better for us to remove that cognitive load from our deliberations and move on. That's why I suggested closing. (for now, and reopen at the appropriate time when implementer support grows). We have used 'unsatisfied' in the past.

Yves: we ack there is an issue, we proposed options, it didnt' get traction and there is no way we can get traction any time soon so we can close unsatisfied

#### 6b

no-op - re-assigning issues...

#### 6c

Rossen: 4 issues -  CSS sizing level 3 - rather quick discussion - closing the issue with satisfied.  Spec review was focused on 3 additions on overall CSS.  Despite the comment on adding motivations - Tab pointed out that most of the spec is motivated by CSS2 use cases from years ago.  We left a comment and close the issue.  Next one was JXL content encoding.  We had a quick re-review of the issue. Peter brought up - can it be used for mime type... Yves.. had most of the comments.  Peter left a comment asking ...

Peter: asking why not just - the issue is that the server re-encodes JPEGs on the fly - wouldn't it be more CPU efficient to have JPEG and JXL files on the serve and use conneg?  

Yves: I prefer that implementation. Images can be well compressed.

Rossen: we moved to reviewing reporting - we left a comment with a whole bunch of feedback and discussion with privacy concerns, API naming in the design.. from a privacy PoV there were concerns about what such reporting would mean for PII.  One of the explainer items is 'browser crashes' - if that's part of the reporting then this could bring a lot of PII as part of the reporting.  We also wanted to know what are going to be all of the types of reporting - they are listing a number of them as motivation... not a specifc list of types of reports. Not clear if theses reports should be visible to script. Reports could expose info to 3rd party by design. Discussion on whether this would be moe appropriate to be an event rather than an observer pattern. and some stylisitc naming issues.  Privacy & secuity questionnaire missing.

Lea: about cascade layers - we did ack that this addresses real needs - we had some feedback on unlayered styles - and ack'd the existing feedback about naming... layer is confusing...

Rossen: from TAG PoV - this addresses a valid user need - happy for it to proceed forward. Details to be worked out at CSS WG. 

### Breakout 07-08:

Present: Peter, Alice, Tess, Sangwhan, Rossen

#### 7a

Rossen: This was me and Alice.

... Covered issue 511 about content-visibility: hidden-matchable. Went over it one more time to get the bottom of the intended design, why this makes sense to be in CSS, how it works with accessibility.

... Convinced ourselves that the proposed path forward is good; closed test with a suggestion for a test case around name computation for aria-labelledby/describedby.

... Then moved on to looking at css-color-adjust-1. We had previously left a comment but not got any responses, realised that they wanted issues filed, so we filed some linked issues.

... Looked at ARIA 1.2 review. Diff between 1.1 and 1.2 looked good. Web IDL section was the only thing that stood out; they're specifying the existing roles and attributes as IDL attributes. We noted we would like to review that later on down the path, when they're closer to finalising the shape of this API.

... One example is that something like `aria-valuenow` is intended to be read as a number, but defined as a `DOMString` IDL attribute. We asked them to bring it back to us and open a new issue once that API is more complete.

#### 7b

Peter: This was me and Sangwhan, and Tess joined for part.

... 2 issues, mkwst joined on requiring embedees to opt in, restricting iframes to same orgin.

... .... sites break ... 

Tess: Classic mkswt "yes go ahead and break the internet, let us know how it goes"

Peter: Network partition... cache, socket, partitioning them ... privacy and security reasons.

.... Concern ... pushing extra costs... power consumption ... all users.

... Privacy and security.

... Sangwhan raised some concerns about how many keys we keep adding until nothing is cached...

... Some of the concerns are timing attacks... visitors. ... lookup came back quickly

... Mitigate by all dns requests .... burning CPU and network

Sangwhan: responded positively, not sure what next action for us is.

... Tess has replied, would be good to get her second opinion here.

#### 8a

Sangwhan: Design principles.

... Tess is writing a PR for cleaning up the ???

... Discouraging image sniffing.

... Someone has to LGTM this.

... Did one change to attributes vs methods which needs a review. Pushed another PR about inclusive language.

... 2 PRs awaiting review. Actually a third is awaiting feedback from annevk.

#### 8b 

Rossen: Alice and me again. This time looking at Personalization.

... Spec which is addressing a great set of problems and use cases... problem is that they are taking ARIA as a precedent for their approach, to go and create their own vocabulary and create a new meta-language on top.

... One of the last comments they left was in response to a point Alice brought up... around the overlap with Media Queries. They agreed that some particular use cases are close to things that could be solved with MQ5 and concluded that that meant that they couldn't use MQ.

... Alice left a closing comment reiterating that we were convinced that the problems they were solving were good and well-defined, but that we were not satisfied with the shape of the solution.

... I followed up with a comment encouraging them to work with the CSSWG.

... Also took a quick look at https://github.com/w3ctag/design-principles/pull/240#pullrequestreview-576924597, happy to pull.


### Breakout 09-10:

Present: Ken, Alice, Dan, Amy, Sangwhan, Hadley, Lea, Yves

#### 9a: Ethical Web Principles

Alice: we took an action to watch the consentful communicationa nd ethical web sessions from TPAC... Starting point for how to get more diverse points of view - beyond web standards community. Discussion on how to think about unintended consequences. Amy suggested - have a study done for new web standards about how they might effect marginalised communities. We attempted to talk about "dark patterns" proposal - we came up with some examples - example about ActivityPub moving away from numeric counts on things that gamifies behavior. Other anti-patterns. Noted that there is some language about addictive behaviors and impact on community... asking API designers about speculating worst-case outcomes for their APIs. Tried to talk about Hadley's PR introducing advertisers as one of the constituencies we need to consider and I tried to bikeshed that - what do we mean when we say advertiser and some APIs close to advertisers are designed to be beneficial for users - e.g. intersection API, private click API... 

Hadley: we also scheduled a follow-up for later.

#### 9b: 

Yves: I looked at bytestream and commented on that and marked as proposed close. Implemnter support and it's an optimisation... 

Dan : we could close now...

Yves: I think it's OK to close it.

Yves: WebRTC priority control API - ads priority parameter to dictionary used to create a WEBRTC connection - based on IETF drafts on how to handle conjection. Adds something to dictionary more or less. Seems fine.

Dan: suggest we close both.

Sangwhan: +1

Yves: I will take care of that.

Yves: RTC ICE transport - web transport through firewalls... will have more understanding later today.

Sangwhan: I'll put that on my list.

#### 10a: Design Principles

Dan: Went through a bunch of issues, assigned a lot of issues

... Talked about whether incorporation of CSS design principles was done or still in progress.

... Does the recursion section need to be split out? Discussed this, should we reduce the size... ended up "giving up".

... I took an action on the information architecture issue to find tech writers who can (on paid time) take a look at the doc from an IA point of view

... Assigned some unassigned issues.

... Took a look at Lea's issue which turned out to be an issue on a [inding written by Kenneth](https://www.w3.org/2001/tag/doc/webcomponents-design-guidelines/) led to a discussion about whether we should reference that doc from the design principles, to what extent does the design principle speak to web developers vs. web spec authors... 

... Can we create a version of the design principles for web developers?

... We will have a design principles week next week.

Sangwhan: Added a propose closing issue on design principles. Two issues raised by non-TAG folks that I don't believe are valid... 259 and 261

All: Agreed on both

#### 10b

Ken: Web serial API - going to ship in next chrome version 3rd of march...  They responded to our comments and we are satisfied.

Sangwhan: pretty happy.

Dan: privacy & multi-stakeholder support? 

Sangwhan: multi-stakeholder is in 

Hadley: Mozilla's [standards position](https://github.com/mozilla/standards-positions/issues/336) is "harmful" 

Sangwhan: originally written by someone at Mozilla.  Also the feedback is correct which is why it's gated behind a permission.

Ken: It's gated by a prompt where you have to select the device...

Sangwhan: if your laptop has an LTE modem it would most likely show up in drop down of devices - and you could break an LTE modem because you could do firmware updates to it. That said I'd like to see if that kind of attack happens in the wild... You would have a blocklist of devices you would not want to expose to the web.

Dan: We should reference the mozilla standards position in our feedback even if we are closing the issue.

[discussion on how modems are exposed]

Ken: file extensions in file pickers... currently allows lots - but they want to limit to ascii characters - including + and # - found examples of $, !, ~... either you just support . or you support all of them.

Dan: Close?

Ken: waiting for response.

### Breakout 11-12:

Present: Amy, Tess, Kenneth, Dan, Rossen, Yves, Peter, Lea

Tess: on 11a - 

Rossen: on 11b - Dan and Me.  3 things - 2 webxr, and web share. WebXR AR module - sent a comment. we went through privacy & security section - low on detail.  Model of the underlying subsystem... need more clarity in the spec about concepts of Content - is it the XR content or page content... sometimes a bit difficult to decipher.  WebXR layers - that review is pretty much done.  One last question in terms of security. He addressed it in his reply but it's not in the spec or the p&s response. Las was **web share API**.  We realized we had done a review signed off 3 years ago... so last f2f we reviewed and gave a bunch of feedback - but people came back and said "you already reviewed this". So we took a step back and asked them what they would prefer as next steps.

Amy: 11c - extra **ethics** section - we started looking through the ethics points on eby one - looking through background of various preinciples. One was [use of the word "users" and whether that's harmful](https://github.com/w3ctag/ethical-web-principles/issues/34).  Another was about codes of conduct.  

Rossen: 12a - amy, myself, peter, Dan. .. thanks to Amy for great notes.  3 issues - **WebXR lighting estimation** - spec is pretty good.  We added a comment encouraging them to add a little more info dealing with fingerprinting.  Otherwise on a functional point of view the added capability it's good.  Next was **same party cookies** - a feature built on top of first party sets. Overall feedback was - too early, we have to see what happens with first party sets. **Screen fold API** - jist of this is that current proposal could be too restrictive and specific. One thing we all agreed for such capabilites it is important to enable device capabilities but not handicaping future improvements in tech or depending too much on current devices.

Yves: 12b - **client hints reliability mechanism** they want to do a redirect using a 200 code - also some optional features... we sent back a bunch of questions asking them to get in tuch with http wg in IETF... waiting feedback.

Ken: **pwa URL handlers** - they are coming up with custom. Only for URL activation for native apps - and this should also work with PWAs. So pointed that out. 

Tess: **deprecating document.domain** - changing defaults - we like the idea; it has compat implications that are scary. We encouraged them to try it and see how it goes.  Yves highlighted we need to be clear with our developer messaging when we change long-standing defaults.

Tess: Also I just made a [PR](https://github.com/w3ctag/design-principles/pull/272) on the design principles... Someone else should take a look.  Requested reviews.

### Breakout 13-14:

Present: Alice, David, Tess, Peter, Sangwhan

#### 13a

Tess: We reviewed the changes to the DOM standard. They were fine. 

... I took an action to complain to Anne about the DOM defining things to be used by other specs, without explaining why they're there. This could potentially be fixed by some kind of bikeshed feature.

#### 14a

Tess: Sangwhan and I looked at the S&P questionnaire. This was meant to be with Pete Snyder but oops.

... We looked at the open PRs, wrote several new ones, reviewed each others' PRs.

Sangwhan: Group may like to take a look at the questionnaire....

Tess: I've been editing the whole doc for clarity. Each phase of editors has brought its own idiosyncracies. Trying to do a rewrite in the same vein as the design principles rewrite.

... Doing one question at a time, currently up to q7. 

... Sangwhan took a pass on a later question which was very unclear.

... Pete Snyder is also helping with that process.

Alice: Does the style guide cover this adequately?

Tess: Mostly. Some content was written with an assumed audience of security experts, so the style guide's advice on audience is helpful there. Finding myself rewording similar domain-specific language again and again, could have a cheat sheet specifically for this document.

Alice: Could we write guidance for questionnaires specifically?

Tess: Style guide says that the first sentence should get to the point. In a questionnaire, first sentence (after the question) needs to establish why it matters. Make sure the reader understands as quickly as possible why their answer matters.

#### 14b

Alice: Me and David. While David was on leave I landed some stuff for CSS on the design principles.

... David started on some edits, landed one PR, and some other WIPs.

... Tweak to the "use the computed value" part that had some inaccuracies.

David: There might be some other things that I want to put in that section, but have to think about it.

... one of these days.

Alice: Separation of concerns, didn't have time to do.

... need to set some time aside for future TAG consideration.

### Breakout 15-16:

Present: Amy, Alice, Ken, Lea, Dan, Sangwhan

Ken: 15a - [Web Neural network API](https://github.com/w3ctag/design-reviews/issues/570) - gave some feedback on the explainer.  We pointed out a lot of things that could be approved or at least explained.

Sangwhan: I don't like the API - ergonomics.  For machine-generated code.  Weak layer of code between some kind of native API and the web - can't just be a header file. Wrote a bunch of comments.

Ken: The storage buckets API... Already looked at it and satisfied.  Proposed closing.  

Dan: let's go ahead and close.

[closed]

Alice: Blink Shipping Process - we talked about how to continue to have an open line of communication with google / blink team specifically.  We talked previously about moving the review point earlier - earlier than "intent to prototype"...  

Lea: [on speed] we can prioritize giving new review requests and initial response - we can build a script that will help.

Ken: we are also sometimes slow that it ships in chrome...

Lea: 16a - we looked at [temporal](https://github.com/w3ctag/design-reviews/issues/311) ... big picture feedback... we wrote the following [feedback](https://github.com/w3ctag/design-reviews/issues/311#issuecomment-768948852).

Dan: close on this feedback?

Ken: maybe we should wait for response.

Lea: we also discussed [abort signal](https://github.com/w3ctag/design-reviews/issues/569) - it looks good to us.  It's proposed closed.

Ken: I closed it - it's done.


### Breakout 17-18:

Present: Tess, Dan, Amy, Yves, Lea, David, Peter

#### 17a

Dan: Battery saving thing [546](https://github.com/w3ctag/design-reviews/issues/546), fed back thoughts, that it was probably the wrong approach, that opt-in didn't really work, and left feedback, the other thing was that it wasn't clear where it was going or what the status was or if there was implmenter feedback, no privacy and security self check. It came in in august so we should have already noticed that it didn't have the right information, we should have fed that back very early in the process and that's a process fault. Now it's pending external feedback.

...periodic background sync. Pinged them to ask about feedback from september by Yves. It's shipping and to my understanding there is some implementer interest, but the review is stalled because we don't know what the current state is.

... hasDroppedEntry in performance callback, Ken was happy with that but they want feedback on the name. Lea left the comment that reflected our discussion about using a dictionary and we had a suggestion on the name as well. That one was a very well written request, including all of the information and a great resposne to multi stakeholder review and security & privacy self review, so I noted that as well.

#### 17b

Tess: two issues.. webXR hit(?) test module, proposed closed back in November so we should probably do that. We did notice one or two little things, we asked about why they chose their data structure for matrices and asked to respond to a comment from many months ago.

David: did respond.. said prior comment was a response

Tess: seems like our matrix feedback should go to the base webxr spec. We should probably file a followup and decide if we're satisfied with that answer. Are we ready to close?

David: I think it's okay to close, I'll reply anyway.

#### 18a

Tess: privacy and security questionnaire, we talked through the status of the document and made a little progress and worked on a couple of issues, I'm writing a PR based on some of our discussion around one of them. It was good. One thing that came up that we need to figure out is that the document is very browser centric and there are a bunch of w3c specs that don't get implemented in browsers but do have security and privacy concerns so we should help folks who are working on such specs make use of the parts of the questionnaire that are useful and help them figure out what parts to skip that aren't relevant.

#### 18b

David: web transport and web socket stream. Web sockets tream we proposed to close because it's not clear what the state of it is right now. It seems.. not clear if there's other browser interest, might get taken up in the web transport wg.

Yves: the first one we want to propose close is web socket stream. It's a way to recast web socket using a stream interface. There is work.. it's inside whatwg, currently no known traction yet from browser vendors. Adam Rice is also in the web transport wg which is working on a way to do client-server communication using streams that has more use cases in mind and exchange patterns as well. In the end we might have a web socket ++ and web transport, have the two merged, or being different, but it's not known yet. That's why we want to close, and ask them to revisit when there is known traction and a real spec behind it. For web transport... it's now in a WG, it was in early review, there will be a lot of changes in the WG and we might just revisit later when there is something more stable.
