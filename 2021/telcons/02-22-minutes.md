
## TAG Teleconference
##### 22-23 February 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-02-22](https://www.timeanddate.com/worldclock/converter.html?iso=20210222T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @LeaVerou, @torgo, @kenchris, @atanassov
* [WebXR Lighting Estimation](https://github.com/w3ctag/design-reviews/issues/574) - @torgo, @atanassov
* [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman
* [Early design review of Cascade Layers](https://github.com/w3ctag/design-reviews/issues/597) - @LeaVerou, @atanassov
* [HTMLPopupElement](https://github.com/w3ctag/design-reviews/issues/599) - @hober, @LeaVerou, @kenchris, @atanassov
* [Early design review for the FLoC API](https://github.com/w3ctag/design-reviews/issues/601) - @torgo, @rhiaro, @plinss, @atanassov
* [inert attribute](https://github.com/w3ctag/design-reviews/issues/610) - @hober, @LeaVerou


#### Breakout B (US / APAC) - [2021-02-23](https://www.timeanddate.com/worldclock/converter.html?iso=20210223T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia
* [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia
* [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov
* [Early Design Review: Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611) - @hober, @rhiaro, @atanassov
* [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo

#### Breakout C (APAC / Europe) - [2021-02-23](https://www.timeanddate.com/worldclock/converter.html?iso=20210223T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @kenchris, @hadleybeeman
* ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon
* [Media Session: video conferencing actions](https://github.com/w3ctag/design-reviews/issues/608) - @ylafon, @kenchris

#### Plenary Session - [2021-02-24](https://www.timeanddate.com/worldclock/converter.html?iso=20210224T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo [suggest to close this as we have a process in place now]
* Time change for the plenary?
* F2F scheduling
* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Dan, Peter, Rossen, Amy, Lea, Tess

Regrets: Hadley, Ken

#### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @LeaVerou, @torgo, @kenchris, @atanassov

Dan: doesn't make it easy to figure out what to do next

Rossen: proposing to add capabilities for controlling colour and width for scrollbars

Dan: we had discussion last time. We discussed scrollbar gutter, and we should have realised we had reviewed scrollbar gutter. My question is, what is there for us to review here? Ken's points are important.. one is asking for more use cases. Some in a wiki. If we ask them to amend the explainer with the use cases and come back to use - then are we done, or do we need to come back to it? Or should we close it and say please do that, let us know if you need more help?

Lea: he did mention usec ases. Our feedback was not just about scroll indicators, but also about being able to specify one colour which is being discussed in an issue (no resolution yet). So still in progress.

Dan: maybe we could say yes to update the explainer and we think these are the outstanding issues that need to be resolved. 

Rossen: can I summarise where I see this work being. This work came about from mozilla two or three years ago when they were facing a lot of comapt issues with scrollbar customisation, going all the way back to i5 or i6 which is when scrollbar colour customisatins were exposed as propietary css properties that allow you to style the track, the arrow and the sub parts of the sscrollbar controller was one of the motivations. The spec was codifying that capability. When it camee to CSS WG the feedback was wait what about the other customisation that was also exposed through webkit prefix properties that allow even greater expanse of scrollbar customisation to the point where you can target individual parts. That became the feedback and the expectation of the overall direction of the spec was to figure out what from the combined set of historical behaviours what is the most actionable path forward. Reading the use cases - they still refer to parts and bits and pieces of specific behaviour that was enabled before. The spec here is a pretty coarse approach. The width is the entire scrollbar component, you cannot target the indiidual components. the colour is also a one stop shop, you can only apply the colour to the entire control. That's where the spec is currently. The current proposal, if we believe it is part of the platform whcih should allow developers to have these two quick and massive behaviours to control the size and the colour of the scrollbars independently that will allow them to create their own components, that's great. All of the details will be worked out further in CSS WG, so we shouldn't sweat those here. The general question for us is as developers is this enough?

Dan: there's an existing set of webkit apis which do more than what this does. So there's an existing implementation. Has that implementation been proposed by anybody?

Lea: I don't think just standardising the webkit implementaitonw ould be a good idea, it's painful to use. There are so many things that need to be customised and often you just want to set the colour of the scrollbar and you have to set a bunch of CSS rules, I don't think that's a good direction.

Dan: I wasn't suggesting we should propose that, just saying to Rossen's point about not micromanaging the styling of scrollbars, but what is appropriate for us to do is talking about browser compatibility and one web and the fact that web developers expect to be able to do the same thing across browsers, the same capabilities or similar, so that would be a good reason to make that comment that Rossen made about it not being fine grained, maybe?

Rossen: yes. To our previous unfinished rule about high vs low level primitives, this fits nicely because it starts high, starts to expose capability at the top level only, the scrollbar control is a black box thing you can shrink or expand as a whole, or style it, that's it. That doesn't prevent if we want to further break down and expose additional capabilities later. We'll start approaching both the ie styling mostly around colours as well as the webkit styling around the different parts inside and placement and sizing.

Lea: in terms of low vs high level, that's just right. 

Rossen: I'm of the mindset that we dont' need to give them too much hard time n this proposal, from the point of view of what they're trying to achieve, can they make the explainer better absolutely. In terms of the intended path forward for this kind of capability - I'm close to the spec, biased opinion.

Lea: I agree with Rossen. Ken felt very strongly about the point about scroll indicators vs scrollbars. Do you think it would be a good idea to discuss this when Ken can weigh in before we leave feedback

Rossen: sure

Dan: I can leave [a brief note]() saying thanks and sorry about scrollbar gutters.

[will discuss at plenary]

#### [WebXR Lighting Estimation](https://github.com/w3ctag/design-reviews/issues/574) - @torgo, @atanassov

Dan: we left feedback. Mitigations listed not spelled out in security and privacy self check adequately. [They responded](https://github.com/w3ctag/design-reviews/issues/574#issuecomment-777778988). Happy to close?

Rossen: I think so

Dan: propose closing at plenary

#### [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman

Dan: [will leave a note](). Will try to work on it next couple of days.

#### [Early design review of Cascade Layers](https://github.com/w3ctag/design-reviews/issues/597) - @LeaVerou, @atanassov

Lea: we had left comments, but based on misunderstanding about priorities. Everything is good. Maybe close?

Rossen: what is left? nothing? I agree. *evangelizes*

Lea: [closing comment]()

#### [HTMLPopupElement](https://github.com/w3ctag/design-reviews/issues/599) - @hober, @LeaVerou, @kenchris, @atanassov

Lea: I have opinions. [Left a comment](https://github.com/w3ctag/design-reviews/issues/599#issuecomment-772497485). The use cases are obvious, no doubts about that. Seems like a bunch of things all together and the utility has to do with positioning and overflow, and these are things that should be solved in CSS instead of adding more magic that cannot be described by the stylesheet. Already proposals in CSS WG about how to deal with it, space for more. I don't think we should solve this with a new html element, should solve in CSS and use it in UA stylesheet. Some more points about attribute names.

Tess: the html folks don't like to have magic either. I agree with Lea that positioning stuff, whichi snot spelled out, is the interesting part - missing in CSS that would be useful for tons of things. Beyond how the positioning works, it's not novel or challenging.

Lea: I think there are use cases for stuff beyond positining. Could come with basic defaults. Coule help with accessibility, tabbing order, things CSS can't address. Eg. anchor the popup to an element which could affect tabbing order.

Rossen: majority is already in dialog

Dan: so why are they proposing it? a lot of people behind it. Is it ergonomics? an easier way to do something that can be done already? Does the need for this highlight a hole in the platform that we need to be responsive about?

Lea: the platform doesn't do this, it just shouldn't be done by an html element. The behaviour of popups spilling out of a container with overflow:hidden there's no way to do that today declaratively. Ergonomics like the light dismiss behaviour, can be done already but is just a convenience. A bag of features that come with it, they're all useful, but not sure it's the right place.

Rossen: yep. Feedback I had from them was around that, compared to dialog there are problems they want solved. 

Tess: I can leave a comment

Peter: the light dismiss behaviour, another review Tess and I did on [??] that should be coordinated into this. Should reuse instead of inventing something else.

[reassign at plenary]

#### [Early design review for the FLoC API](https://github.com/w3ctag/design-reviews/issues/601) - @torgo, @rhiaro, @plinss, @atanassov

Dan: be good to get a PING opinion. Should we start the conversation?
... privacy and security self-check... 

Rossen: any reason to rush?

Dan: not that I know of. It says early review. Profiling people based on sensitive criteria can be harmful to them. Targeted ads to do with baby care because of a certain age range, etc. There are plenty of high alarming value type stuff. Is there something we can say immediately to provoke that discussion? Have they already accounted for it?

Amy: they say something about sensitive categories, that they will just not use them... but not clear who decides what is sensitive.

Tess: if catgories are algorithmically generated and not designed by humans you can't say you're not going to make sensitive ones. And who watches the watchers? how do they decide what's sensitive and what's not?

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/601#issuecomment-783553848)

Amy: I will [leave a comment](https://github.com/w3ctag/design-reviews/issues/601#issuecomment-783780556) about the centralisation of the lists, transparency of that to users

#### [inert attribute](https://github.com/w3ctag/design-reviews/issues/610) - @hober, @LeaVerou

Lea: concern that this is a boolean attribute, once you turn it on for a subtree there's no way to turn it on for a descendent element, which I think there are use cases for ([comment]()) but otherwise straightforward.

Tess: the way dialog and inert are built on the same model... dialog imposes inert on everything else whereas inert imposes it on a subtree. But i agree punching out of inertness in a subree is useful outside of the dialog scenario

Lea: dialog doesn't even use this? 

Tess: the point is that the concept of inertness in the spec that underlies the inert attribute is also used by dialog. But dialog is not using the inert attribute because these are two ways of exposing a similar behaviour in two different parts of the tree.

Dan: needs security and privacy review - pending. Premature to close. [Two weeks](https://github.com/w3ctag/design-reviews/issues/610#issuecomment-783558270)

### Breakout B

Present: Lea, Peter, Rossen, Tess

Regrets:

#### [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo

#### [Early Design Review: Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611) - @hober, @rhiaro, @atanassov

#### [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia

#### [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia

#### [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov

Peter: Latest comment sugetst there's a second screen F2F taking place in the next few days. We should try to provide feedback before that. Remember a proposal by Microsft that allowed deailing with things like hinges, gaps,  etc.

Rossen: It's not but this proposal does take the Microsoft Duo devices as part of its use cases. I also recall an issue about explicit angles.

Peter: My feedback is as before - this is too specific of a hardware use case and the API follows that requirement instead of a more generic approach.

Rossen: Have you provided the feedback? Seems like a valuable conversation for their f2f.

Peter: I will.

Rossen: Lea, are your happy with the responses to your questions?

Lea: Yes. The proposal is designed around current devices with one fold etc. The response was that the complexity of the fold etc. will become preventable quickly and they don't anticipate more than 2 folds. 
... Had some more syntactic feedback that was addressed.

Rossen: How does this feature intersect other features such as orientation?


### Breakout C

Present: Ken, Dan, Amy, Sangwhan

Regrets:

  
#### [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @kenchris, @hadleybeeman

Ken: we gave feedback, they filed issues.

Sangwhan: issues with API design... I provided [some feedback](https://github.com/w3ctag/design-reviews/issues/570#issuecomment-768875996). I suggested an alternative design to [this](https://github.com/webmachinelearning/webnn/issues/135). Factory that creates another factory... factory for oepration. Model builder give me an add operation.. model builder give me an xyz operation...

Dan: is the way they are building this coherant? The way the community builds these kinds of things? 

Sangwhan: no

Dan: why are they building it this way?

Sangwhan: mapping native optimisation APIs straight to the web. Inspiration from Android API. Not justifiable. [This JS example](https://github.com/huningxin/webnn-samples/blob/master/lenet/lenet.js#L32). They're saying it's for frameworks so it's fine.

Dan: this is an area we can provide feedback not specific to the neural network use case. Does design principles say don't do that? Low level vs high level. If you're designing this for the web you really need to think about how web developers are going to use it, not simply rely on frameworks. Parts of the web people dislike working with are the parts that have been designed in this way.

Ken: if you can make the api nice even if it's low level... might be use case for this in the future

Sangwhan: a couple of things they ignored in the principles, constructors. Everything is a factory pattern, but you should bind when you compile the graph and transfer it to the coprocessor, that's more common in actual frameorks. The only framework that does that they're doing now is tensorflow. *types code in jitsi chat*

```
model = nn.Sequential(
        nn.Conv2d(in_channels=1, out_channels=6, kernel_size=5, stride=1),
        nn.Tanh(),
        nn.AvgPool2d(kernel_size=2),
        nn.Conv2d(in_channels=6, out_channels=16, kernel_size=5, stride=1),
        nn.Tanh(),
        nn.AvgPool2d(kernel_size=2),
        nn.Conv2d(in_channels=16, out_channels=120, kernel_size=5, stride=1),
        nn.Tanh(),
        nn.Flatten(1),
        nn.Linear(in_features=120, out_features=84),
        nn.Tanh(),
        nn.Linear(in_features=84, out_features=10),
        nn.Softmax()
    )
model = model.to('cuda0')


with tf.device('cuda0') as d:
    blah blah blah
```

Dan: I opened up a [design principles issue](https://github.com/w3ctag/design-principles/issues/288) to capture this.

Ken: sounds like you have good arguments about why they should redesign this

Sangwhan: I do.

Ken: I think they have implemented and have polyfills.

Dan: what's the advantage of having this api vs someting that sits in webassembly

Ken: they can use hardware

Dan: doesn't webGPU give you..

Ken: some of it, but hardware made for machine learning is always better

Sangwhan: in mobile phones you have a neural coprocessor which is not a GPU. A multiplication machine.

Ken: these are becoming more and more common.

Sangwhan: I don't think gup based computation is going to be a very common thing to do for this.

Ken: the approach is the same as WebGL. Mapping the OpenGL API to the web, and it's a terrible API for JS developers, which is why everyone is relying on frameworks [e.g. 3js] because it's so difficult to use. For WebGPU they're actually trying to make an API you can use as a developer directly, even though you might want to use a framework. WebGL feels like a C API, very foreign to web developers.

Sangwhan: I will join one of their calls

Dan: can we summarize into or issue?

Sangwhan: wanted to bring up priority of constituencies, but doesn't capture that APIs should be useable by average devs. When we bring that up there are plenty of counter-examples... extensible web manifesto says apis should be low level

Dan: We have more nuanced language in there now

Ken: something low level doesn't have to be bad

Dan: milestone to 29 March

#### ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon

[punted]

#### [Media Session: video conferencing actions](https://github.com/w3ctag/design-reviews/issues/608) - @ylafon, @kenchris

Ken: toggling....

Dan: they do need to further explore the use cases in the explainer. 

Sangwhan: design-wise I think it's fine.

Dan: good to see multiple impementers.

Sangwhan: [writing feedback](https://github.com/w3ctag/design-reviews/issues/608#issuecomment-784005526). Method for mic is muted and camera is turned on, which is the opposite. One checks if it's off, one if it's on, that's weird.

Dan: considering actions that can activate/deactivate camera/mic is there enough thought that's gone into the [privacy design](https://github.com/w3ctag/design-reviews/issues/608#issuecomment-784009677)?

Ken: this is common in apps people are used to use. 

Sangwhan: the media session thing is a mechanism for you to react to things like media keys. If you have a remote or multimedia keyboard, you press a hardware button and send it to the application and it knows instead of having to listen to key events. Something that comes from the system, an intent. In this case it's a mute button on your hardware mic. I don't have good ideas of how this could be exposed in a securty and privacy manner.

Ken: the user is doing an action somewhere and expects something to happen.

Sangwhan: who knows, there might be a loophole.

Ken: you can already turn on the camear on the web. You get a notification the first time, and it has to be visible. I think it should be handled by what you can already do. 

Sangwhan: feels more like a convenience mechanism. If you have actual conferencing equipment you have these buttons you can use.

#### [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia

Sangwhan: we should hold off on this one...  webcodecs is going through a change.

#### [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia

Dan: Reviewing answers to privacy & security questionnaire. Looks good.  Do we know what the implementation plan is for any other browser? [leaves comment](https://github.com/w3ctag/design-reviews/issues/603#issuecomment-784014532).

Sangwhan: there may be some conflict because webcodecs moved away from streams... I will review.



### Plenary Session

Present: Peter, Sangwhan, Amy, Tess, Dan, Rossen

Regrets: 

#### Breakout Rollup

##### Breakout A

Dan: good discussion about scrollbars #563, left a note, asking for use cases. Bumped.
... WebXR lighting #574 proposed closed, happy with changes
... WebXR dynamic viewports #588, gotta do some work
... cascade layers, #597, closed
... HTMLPopupElement, #599, left feedback, waiting for response
... FLoC #601, left feedback

Tess: talked about requesting PING review, there's a conversation going on

Dan: inert attribute #610 needs security and privacy, alice replied that it's now linked, need to discuss in breakout again

##### Breakout B

Peter: Talked about ScreenFoldAPI, left feedback #575. Second screens WG is having a f2f so we wanted to get feedback to them.

##### Breakout C

Dan: Web neural networks API #570

Sangwhan: I'm supposed to join one of their calls

Dan: one of the key points is that they're designing for frameworks, mapping Android API, rather than thinking about what would be good for web devs. Opened a design principles issue on that.
... Media session video conferencing actions #608, waiting for response
... Media source extensions for webcodecs #576, on hold

Sangwhan: no longer on hold

... insertable media processing using streams #603

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo [suggest to close this as we have a process in place now]

Dan: can we close this? Do we want continuous issues? We have a point of contact for Blink shipping process and have a process in place.

Peter: we had some actions to make additional issue templates for different phases of their shipping process, did we do that?

Rossen: that plus incorporate with early WICG stage proposal to surface early review. Other than that I agree with Dan, happy to close.

Dan: those are issues for process repo and work on it next week

Tess: there's a mailing list for whenever a repo gets created at WICG

Dan: [creates issue](https://github.com/w3ctag/process/issues/23) to track this.

#### Time change for the plenary?

[discussion on possible new time for call]

Breakout B one hour later - good for Sangwhan, Peter, Rossen, Tess; need to ask Lea

Plenary: Are we all saved by Daylight Savings?!

#### F2F scheduling



#### Issue Triage
  
  
