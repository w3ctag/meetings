## TAG Teleconference
##### 04-06 January 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-01-04](https://www.timeanddate.com/worldclock/converter.html?iso=20210104T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov
* [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron
* [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron
* [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185)

#### Breakout B (US / APAC) - [2021-01-04](https://www.timeanddate.com/worldclock/converter.html?iso=20210104T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov
* [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron
* [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron
* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron

#### Breakout C (APAC / Europe) - [2021-01-05](https://www.timeanddate.com/worldclock/converter.html?iso=20210105T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo
* [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon
* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice
* [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia
* [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia

#### Plenary Session - [2021-01-06](https://www.timeanddate.com/worldclock/converter.html?iso=20210106T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Scheduling the VF2F
* Breakout Rollup
* [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov
* Issue Triage

-----

### Breakout A

Present: Dan, Kenneth, Peter, Rossen, Yves, Hadley, David

Regrets:


#### [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov

Hadley: PING action - can we follow up with Hober?

Peter: let's take it to the plenary

#### [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron

David: we didn't have consensus on [my proposal](https://github.com/w3ctag/design-principles/issues/99#issuecomment-637794657)...  I think to some extent it might be a question for Peter and/or Tab about the tooling issues...

Peter: [catching up on issue] [last comment from tab](https://github.com/w3ctag/design-principles/issues/99#issuecomment-656289069) Looks like this could possibly work...  

Rossen: besides the tooling can the issue still be resolved?  

Peter: we can still resolve on "this is a good idea" - cross-linking specs that have partials..

David: the resolution could be "we don't have consensus about reducing the amount of partials in stable specs but we would support more work to do cross-linking of partials".

Peter: we could add it to the documentation - in the design principles - when you're designing partials...

David: don't know if that's actionable for spec authors...

Peter: could document the "desired path" ... - but it's not something we can "complain about" when we review a spec.

Peter: shall we close the issue?

David: [posts response and closes](https://github.com/w3ctag/design-principles/issues/99#issuecomment-754103075)

Peter: [files issue against bikeshed.]

#### [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron

David: I had a draft piece of text the last time we talked about this...  I should make a PR with this text.

Dan: where does this go?

David: in the end of the CSS section.

Hadley: i like that you've used "content" instead of data loss.

Peter: Alice suggested "perceivable." - [PR 240](https://github.com/w3ctag/design-principles/pull/240) - doesn't have exactly your text.

Rossen: not entirely ready to be merged. We should decide if we go with perceivable or viewable. I see [perceive?] where alice is coming from... Screenreaders can access text outside of the view. Composition of accessible content is rarely that of viewable - presentation meant for screen. .. on the flip side, I agree with Alice that by default CSS shouldn't prevent other presentation modes from being accessible.  So perceivable might be best.

Peter: is there a WCAG link?

Rossen: "presentable in ways they can perceive..." - language from WCAG.

Ken: for non english as first language speakers, viewable might be better.  visible?

Rossen: again that brings in the whole accessiblity issue.  

Ken: a lot of people ... need the accessiblity spelled out.

Rossen: I will link to the def of perceiveable in WCAG.

Hadley: will it have the impact?

Rossen: I think if we link to wcag it will have the impact.    We could spell it out.

Dan: I think that might be better.

David: to some extent this principle is about what happens in visual presentations rather than assistive technology...

Rossen: not sure about that. All the accessibility conversations...problems caused by "default behaviors."

Hadley: what will they do differently?  Test?

David: it's a think you should think about when you're designing a new CSS feature...

Rossen: one quick example: when we designed grid-level-1. One of the main push-backs from members of CSS motivated by accessibility scenarios is that there is no easy way to create groupings, and that brought about sub-grid. As a mitigation in the mean time to allow the accessibility constructs - especially in the context of forms, we pushed subgrid to level 2 with the added requirement that you could use grid as it is... We created a default experience that was usable to assistive tech - by default.  So this particular principle would have applied at that point. Had it been applied at the beginning at the design phase it would have motivated earlier thinking.   Earlier thinking on how to make grid and subgrid built in lock-step so you don't have the bad-experience issue with people using assistive tech.  As a base principle, this is core to CSS. CSS is mostly applied to visual... Applied to viewable content as it was initially worded (or perceivable)... makes a much stronger case.

Rossen: so spell it out and not use "perceivable"

Ken: yes I would like that

Hadley: I think that would be helpful - and we could use examples if necessary

David: I'm fine with spelling it out more

Dan: +1

Rossen: I will ready the PR for us to push the button.

Peter: end of the CSS section.

#### [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185)

Dan: reviews...

Hadley: I don't think anyone has defined web crypto architecture... specific algoritms might change much faster than the APIs that use them, etc.

Peter: related to [issue 491](https://github.com/w3ctag/design-reviews/issues/491)

Peter: I like hadley's suggestion on having a broader section on crypto...  we could add to that "algorithsms that have received sufficient review".. known bad algorithims...

Hadley: i wouldn't be bad to have but are people asking for it?

David: I think there are other principles around ...  Some people are interested in principles around algorithm choice - some people think it's better to have less choice... 

Peter: we could ... draft up a strawman PR and farm it out to crypto experts for feedback... 

Hadley: Lukash could have some opinions.

### Breakout B

Present: Alice, Peter, Rossen

Regrets: Tess, David


#### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov

Alice: In the previous discussion I noted some examples of the extreme points of high and low-level APIs might be helpful to guide discussion.

Peter: [SubtleCrypto](https://developer.mozilla.org/en-US/docs/Web/API/SubtleCrypto) is an example of an extreme low-level API

... Maybe not quite as low level as I recalled...

Rossen: Something like WebGL, anything that has to be close to the device...

... in contrast to a form element, for example?

Peter: SubtleCrypto has a big warning, "if you don't know what you're doing, you probably shouldn't be using this API" - lets you encrypt messages (?)

... higher-level system would just encrypt a message for you.

Alice: What was the design goal for SubtleCrypto

Peter: People were rolling their own crypto... avoids need for people trying to reimplement RSA encryption... if someone was making a mail client and wanted to encrypt email before sending...

... lots of risks involved with rolling your own crypto.

Alice: is this a good design?

Peter: Good low-level API design, reasons for this to exist. WebRTC will be using the same *implementation* of these APIs, even though it's not using the API directly. Similarly with HTTPS.

Rossen: Going to ask what I asked last time: can we have some kind of succinct recommentation for the altitude of ...

... couple of ways for us to go about this principle. One is much harder.

... Harder one: define criteria, boxes which fit your intended goal. Is this declarative, script, lower-level, or CSS property.

Alice: Sounds more like separation of concerns

Rossen: High vs. low is third dimension inside the boxes of CSS, HTML, JS...

... Easier method is to define a principle/set of guidelines describing how these are different, but without defining the borders of where one stops and the other begins. Declarative APIs are different from CSS properties, different from events.

... overall design guidelines spends quite a bit of time defining some of these concepts. Events, CSS constructs, mostly JS guidance.

... if we use that same approach for high/low level APIs, better chance of having something useful, than trying to define boxes.

... Wouldn't expect that using a high-level API, like an HTML form element, would disable my bluetooth camera.

... High-level declarative element should have gone through enough scrutiny, functionality and capability of high-level element encompasses a lot more intuitive and well-behaved pattern compared to a single API that could be bolted onto a device that could enable/disable or set the state of a camera.

Alice: What failure case would lead to an HTML element disabling a camera?

Rossen: Opening a web page leading to my camera being disabled.

Alice: So like some kind of element which set up a video conference, and greedily locked on to your camera.

Peter: Camera is an interesting example... you can do input type=file and set the media type to image capture... that will automatically take control of your phone camera.

... you could build your own Custom Element for `<camera>`, using media APIs. Native camera input only works on mobile. 

... `input type=date`, vs low-level `intl` APIs to format dates, all the different calendaring & numbering system, but I'm not sure those APIs expose enough raw data to build a custom date picker as comprehensive as the built-in one.

Rossen: Meta-point... if we approach this type of guidance from the point of view of starting to describe how altitudes of high/low are different, it'll be easier for us to make progress.

... is this going to be an element or a bunch of APIs?

... Reminds me of Voronoi diagrams .. define points, then allow the rest to be defined by relationships. No need to pre-compute every single line.

Alice: I like Peter's comment from last time which is about designing in layers. The subtle crypto is a great example we should capture. A combination of user case and a layer that fits the case. 
Another example is inert - a concept developed for the 'dialog' element and then found other use cases that weren't dialog specific but still usefull and where 'dialog' would've budnled too much. 
So pick out points such as mentioned by Rossen and pick specific and explicit examples that will make it easy to reason and explain. Ex. input type file or date vs lower level API that could be used to create something similar - all useful examples. 
... the summary could be something like - "starting from well defined user needs, design your API with well-defined layers and ideally expose the highest-level only."

Rossen: The first design is always complex, reflecting real-world complexity. It takes a lot of work to continue to refine and design that solution to come up with a *simple* solution which feels intuitive. This is when you have simple, elegant design.

... This is rare, we as engineers often fall in love with the first API, which is often the most complex one.

Peter: I'm mostly in agreement... concerned with blanket advice to target the highest level.

... Not necessarily always the best advice since it leads to the cliff situation.. (???) have to start from scratch. Conversely WebRTC shipped *only* low level APIs. Would love to see a higher level API for e.g. a `<videochat>` element.
  
Rossen: Shouldn't strive to only ship the high level API, but .. shipping the highest possible level API usually reduces the amount of exposure that you're going to create for your feature. If you got it wrong, you have a chance to backtrack, and it's just one API. You didn't introduce a set of N APIs which need to be composed. If you ship that top-level API like an HTML element... until people found that useful, you didn't need to invent custom elements.
    
... start from the top, and ideally stop there if you can live with it.

Alice: another benefit of starting high level... The Web is supposed to be "Batteries included" - shalow learning curve, easy to start wtih and has built in support for things like accessibility etc. With lower level APIs the first thing to usually go out of the way are things like a11y, backwards compat etc. 

... shipping something higher level enables you to get a lot of lower level platform support for the rest of the thing that authors shouldn't worry about - security, privacy, a11y etc.

... Not at all to say don't ship low-level APIs, ship them when there is a well defined user need for them.

Peter: Don't want to say ship the high level API and stop there. There is a productive tension between high-level and low-level APIs. Should expose the fac tthat this tension exists...

Rossen: Prefer shipping functionality earlier, then design the lower-level API for extensibility.

Peter: (???) extensibility. 

... Accessibility, targeting higher-level system acts as a forcing function to think about the things the web is meant to provide. Lower-level APIs allow you to leave that "as an exercise for the user".

Alice: ... benefits for both high and low level APIs. We should talk about escape patches and clifs such as a11y, performance etc. Rarely the case where you need only one vs the other. Start with the guidance of user needs, layers of the API and aiming to the highest level as a start. 

Peter: We often see in CSS, "if only there was a property that did exactly what I want", and then people design that, but without referring to existing lower layers. So this thing exists as largely stand-alone.

Alice: example of that?

Peter: We pushed back on portals because it's largely re-inventing iframes instead of extending and improving the existing `<iframe>` API.

Rossen: continuing to think about use case and layers... 99% functionality of something that exists, and you need to add anotehr 1% API somewhere else to still achieve your user need goals.

Peter: Bit unfair to expect everyone working on any one feature to understand the entire web platform, so could advice people to come talk to the TAG early on.

Alice: Like the early design review process we talked about. Can't separate process from design.

Peter: Makes sense since TAG is shepherding the architecture of the web, folks should come to us early to fit things into that architecture.



#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron

Alice: I had an action to do something about this and I haven't done it yet... let's punt again.

#### [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

#### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron


### Breakout C

Present:  Sangwhan, Ken, Yves, Dan

Regrets: 


#### [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo

Sangwhan: [writing a PR] 

... "Other considerations"



#### [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon

Sangwhan: I have [proposed text](https://github.com/w3ctag/design-principles/issues/171#issuecomment-698166432) in the comments...

Yves: ...what happens when you reuse an existing container...

Ken: Like AV1?

Yves: yes because you're not sure if the clients that support the media type of the container will support the media format that is inside.

Sangwhan: like ISOBMFF - but when you're sending that you declare the type

Yves: any MPEG format will use video/mpeg something...

Sangwhan: video/H264 and video/H265 [registration] does exist..  

Yves: that's OK then

Sangwhan: matches up with the text that I wrote...  Maybe I should mention IANA registration

Yves: yes. Also media type should be that for the video itself and not the container...

Sangwhan: in 171 we should stop relying on pattern matching - mime sniffing - there is a spec for it but new types should not rely on it.

#### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice

Sangwhan: going to be big

#### [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia

Sangwhan: I have [proposed text](https://github.com/w3ctag/design-principles/issues/70#issuecomment-698660319) in the comments...

Dan: [makes PR](https://github.com/w3ctag/design-principles/pull/262) - this just has the original text from Sangwhan.

#### [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia

Sanghwan: this one is done so we can close it.

[closed]

### Plenary Session

Present: Kenneth, Tess, Hadley, Alice, Dan, Rossen, Peter, Yves 

Regrets: Sangwhan

#### Scheduling the VF2F

Dan: last week of Jan...

Dan: week before will be agenda planning

Tess: no plenary time so.. might not be an easy thing to navigate for newcomers...

[...discussion...]

Peter: we generally invite them to join whenever they want to. As soon as it's announced we will send that out.

#### Breakout Rollup

##### Breakout A

Hadley: on [harmonizing permissions](https://github.com/w3ctag/design-principles/issues/144), we left it that there was a PING action and Tess was involved...  

Tess: I did talk with one of the PING chairs before the break... Nick D is otherwise engaged... wasn't aware of any particular time pressure... if the PING chairs - they have a call tomorrow. I'll see if it's something that comes up.

Peter: we closed 99. Looks like progress will happen.

Rossen: No data loss by default - we looked at this issue - we'll add a principle to the CSS section that content should be viewable and accessible by default. I raised a PR.  Needs review.

Hadley: Security & Crypto principle... we need some crypto resources to point to... useful to have some text - some high-level descriptions of crypto architectures - algorithms changing - we would like a crypto expert to draft that. 

... also, I created a [pull request](https://github.com/w3ctag/ethical-web-principles/pull/32) on the ethical web principles.

##### Breakout B

Rossen: high level / low level... primary discussion... the summary of the outcome is - we can turn all of this into ... what's forming as a principle we can write down... start with well-defined user needs - exposed at the highest possible level.  This allows us to validate requirements that meet user needs - once functional side of user needs are met then you can understand what the develeoper extensibility needs are to expose lower levels of API. 

Alice: we talked through specific examples - that was helpful - we should emphasize that principles should come with examples of the principles in practice. Can be hard to understand what the author was getting at.  We talked about starting at the highest level - allows you to get the funtionality to users immediately - design in things like security & accessibility - and keeps - the shallow learning curve - a valuable feature of the web.

Ken: sometimes it's valuable to think about the layering - to make sure you have something is future-proof.  It's always nice to look ahead beyond what you want to ship.  WebNFC for example - the API shape - if we were to support other things then we mapped that out - and did some exploration - was a good excercise and helped to shape the API.

Alice: we want to emphasize "think about the layers" even if you are not exposing all layers immediately.  Example of `inert` - specing it required fine tuning - because things weren't thought through. But the basic concept had already existed as a layer from `<dialog>`  

Rossen: Other major pitfall we can help prevent by starting as high as possible - if you piece together APIs to build a solution, you might end up repilcating something else.  Peter gave an example of Portals - that it's basically like an `<iframe>`.

Peter: pitfalls of designing a top-down - you could end up with something that doesn't reuse other parts of the platform even though it should. we should start with a top-level goal and then think about what other parts of the platform can be reused - but start exposing as a higher level thing. 
 
Alice: we should think about what the missed opportunity was with `<iframe>` that led to this.

##### Breakout C

Dan: We did 3 PRs in breakout C.

Dan: we closed 145.

[PR 263](https://github.com/w3ctag/design-principles/pull/263/files)

[merged some typo PRs]

[closed some obsolete PRs]

Peter: I will re-review for API vs features and will raise a new PR.

[discussion of 'API' vs 'Feature']

#### Issue Triage

