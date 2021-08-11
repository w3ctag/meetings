# TAG Teleconference
#### 09-11 August 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-08-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210809T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov
* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov
* [Request for review: CSS tree-scoped at-rule names and references (for @font-face, @keyframes, etc.)](https://github.com/w3ctag/design-reviews/issues/659) - @hober, @LeaVerou, @torgo

### Breakout B (US / APAC) - [2021-08-10](https://www.timeanddate.com/worldclock/converter.html?iso=20210810T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober, @cynthia
* [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov

### Breakout C (APAC / Europe) - [2021-08-10](https://www.timeanddate.com/worldclock/converter.html?iso=20210810T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro, @hadleybeeman
* [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov
* [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman

### Plenary Session - [2021-08-11](https://www.timeanddate.com/worldclock/converter.html?iso=20210811T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage


-----


## Breakout A

Present: Dan, Peter, Amy, Rossen, 

Regrets: Lea, Yves, Hadley, Kenneth


### [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov

Rossen: [CSS thing and chromium implementation]

Dan: notes "positive" signals in the Chromnestatus page from Safari. - good for multistakeholder.

Rossen: between Tess & I we spoke about it - how it would apply to different kinds of overflow... whether it's programmatic or through UA - eg panning. Main question - 2 types of overflow. Overflow that is scrollable or manipulatiable - and one that isn't. `overflowVisible` creates overflow but it's not scrollable. `overflowClip` if applied to visible will constrain the bounds but doesn't change the bounds.  We gave reasoning why the proposal seems a bit confusing and more explanation is needed.  [Response](https://github.com/w3ctag/design-reviews/issues/579#issuecomment-856915250) has not addressed the issue - followup discussion is needed.  Explainer in-lined into the comments - i don't appreciate the corner cutting. One of the main reasons for the explainer is to satisfy the criteria - use cases - how the feature addresses the use cases - what other other methods were considered to satisfy? Is this the best way to go... Plus security & Privacy...  They are talking about experimentation...  The chromestatus page only talks about overflow-clip.

Peter: the issue is about both.

[mozilla shipped clip but ...]

Rossen: don't see anything about margin from reading the Mozilla intent-to-ship.    Somewhat misleading on Chromestatus.

Rossen: more discussion warrented.  I don't think overflow clip margin is shipped.

Peter: i have concerns about clip.  One of those things where we have multiple ways of doing something in CSS.  This whole thing feels bolted on the side instead of fitting in well with CSS.

Rossen: what's a better approach?

Dan: because they don't provide the user needs, can you tell me what this is used in? 

Peter: anything that has a specified or constrained size that is smaller than what it would need to fit its content can potentially overflow

Dan: right, so something might overflow the bounds of an iframe?

Peter: not an iframe, but a paragraph with a really long word. Something is going to have to give. The question is how doe sit give? overflow:visible you draw the contents extend outside the box. Auto or scroll you add scrollbars and don'td raw the outside but allow the user to scroll. Hidden you don't draw the outside, dont add a scroll but you could programatically still scroll it. The author can add some other mechanism to display it. This, if I'm reading correctly, you don't draw the overflow, no mechanism to scroll it whatseover, the margin basically says go ahead and draw some extra, eg. by 20px worth of the overflow but no more than that. Lets you expand the clipping region.

... One of my questions was why should the margin only apply to clip, why not over-flow hidden? Main concern was that when you overflow there's a side effect. Scroll or auto, and start scrolling, auto you only scroll if you have to, scroll you always have a scrolling mechanism. Side effect is when you get a scrolling mechanism you get a stacking contet. Everything in the box is an atomic unit for rendering. Eg. with z ordering things things can't be in the middle. It isolates that whole thing into its own rendering area. One purpose is to control overflow without generating a stacking context.

Rossen: which is not great

Peter: I think that's why you can't scroll programatically because if you don't have a stacking context you can't do all of the math, it's too complicated

Dan: where the need for the explainer would come in is talking about that, and also the use cases that make this important. Obviously it's being driven by some user need - who is it and what is the need? That justifies the added complexity and the difference between this and the case where its scrollable but only programatically

Peter: CSS has made this msitake in several places - switching some property has a main effect and a side effect, like creating a stacking context or becoming a containing block. We wind up with people doing things like making something position relative then not offsetting it, becuase it has the side effect of creating a stacking context. You want to force the thing to be a stacking context or containing block. My desire has been that these side effects should just have their own switches. If I want to force something to be a containing block or a stacking context I should be able to say containing-block: always, and not have to trick the engine into that state. I think this is one of those things where we're adding a property that people are going to use for its side effects more than its effect and we should just enable direct control over the side effect that people want.

Rossen: I think you need to give your comment more gravity and then continue the conversation

Peter: I said what I meant.. he responded with 'why not a scrollable context'.. which is not what i was saying. I'll respond.

Rossen: will leave feedback about explainer

### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo

Dan: Mike Taylor responded 11 days ago to the feedback.. we've had discussions.. I don't see how Mike is addressing the issues raised by Henri. A key issue is about the severity of the issue they're trying to solve.. Henri is saying have you structured.. Mike is saying the UA has been misparsed or all mobile browsers have similar UA strings.. there are a lot of ways that websites misinterpret and send the wrong content because they misinterpret the users intent. The UA string plays a role in many but not all of those. I just saw a tweet from Terence Eden talking about how his portrait orientation monitor means that on some websites he gets a big notice on this monitor saying we don't have a mobile version of this site becuase they assume that if the viewport is portrait it must be mobile. I'ts an example of misunderstanding.

Peter: parsing UA strings has always been hot flaming garbage.[+1 dka] Mainly because all of them lie. Every UA is claiming to be Mozilla. As soon as sites it get it wrong the clients lie about who they are. Standardising what the UA is and doin git in a structured way that parsers are not going to misinterpret is good.

Dan: if we could get consensus on that point it'd be useful to feedback into this arguement. The rest of Henri's argument is this thing you want to make a client hint for isn't very useful and will decrease user privacy. That's an argument that needs to happen at some level, but not sure we need to get into the weeds on which thing eeds to be in the client hints vs not. Feeding that back that it would be a good thing to have more structure, and this is a good proposal for that structure, would be a positive. But I don't know. Good to talk about at plenary?

Peter: I have concerns that.. I accept that client hints break out the aspects, instead of sniffing and deciding i must be mobile because you're in portrait mode I can see you're mobile becuase you're mobile and not make these assumptions. How long is it going to be before someone is incented to lie about this too? Then this will degrade the same way as the UA string. To the extent that this is welld esigned and the dimension sthat you care about are isolated there may not be a need to lie, I hope. 

Dan: another point we could ask Mike - why does Mike think that restructuring the UA in this way will incentivise people to lie less? Structurally, is it less incentive for them to lie?

Peter: there's maybe not a good reason to lie about are you mobile or not. They're still giving away I'm version x of safari and if someone makes a presumption based on that because they're doing a bug fix and they didn't check the version, and safari fixed the bug but sites are still working around it, then devices are incentivised to lie about itself. Browsers lie becuase websites make assumptions. Almost every engine claims to be almost every other engine somewhere in its UA string and is doing it to fool a website that has tailored code against their engine that they're trying to avoid.

Dan: asking that in the comment

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

Dan: comments not responded to. Plenary.

### [Request for review: CSS tree-scoped at-rule names and references (for @font-face, @keyframes, etc.)](https://github.com/w3ctag/design-reviews/issues/659) - @hober, @LeaVerou, @torgo


## Breakout B

Present:

Regrets: Sangwhan


### [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober, @cynthia

### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov

## Breakout C

Present: Dan, Ken, Amy

Regrets: Lea, Yves, Hadley, Sangwhan

### [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro, @hadleybeeman

[closed on the basis of the PR]

### [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov

Dan: no explainer [grumpy comment](https://github.com/w3ctag/design-reviews/issues/644#issuecomment-895823217)

Kevin: [slightly less grumpy comment]

Amy: no response to Sangwhan's request for delta

### [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman

Dan: checking [minutes from meeting with Mike on the 19th](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/07-19-minutes.md#breakout-a-europe--us---2021-07-19-1).. questions are still around when they would activate it by default... I think we should close this with thanks for the explanation, we understand you're going to be trialling this in q3 so we'd appreciate hearing what the feedback has been on the trial. Our concerns about complexity remain and we'd like to understand more about any developer research you have which supports this approach, is one of the things I asked... I think we've provided what feedback we can.

## Plenary Session

Present: Kenneth, Sangwhan, Peter, Dan, Amy, Tess, Rossen

Regrets: Hadley, Yves, Lea

### Breakout Rollup

#### Breakout A

Dan: spent most of the time talking about overflow clip margin. Doesn't look like anything has progressed. Rossen said he'd leave feedback.

Peter: I have feedback as well. We also talked a lot about client hints. A lot of feedback on that issue.

Ken: that has started to ship right?

Dan: it's the deprecation of the UA string that's really.. Yesterday Mike Taylor left some comments. We really need to spend some time.. there's quite extensive stuff from 2 days ago I haven't read. I'd like to read before we discuss further. Week after next breakout C? I'll try to progress this tomorrow.

Peter: okay. Also a note on CHIPS to discuss in the plenary.

Dan: we haven't got any feedback on points raised 8 and 5 days ago. Feel like we need a more focussed discussion on this about ..

Ken: how urgent? Face to face?

Dan: the september one, good idea

#### Breakout B

Peter: didn't happen, scheduling conflicts

#### Breakout C

Amy: we closed an issue!

Dan: best terminology for data urls, 635. They made a PR based on our feedback and merged it. Performance timeline...

Ken: don't have an explainer.. but not explanation of what changed between level 1 and level 2. I know some things have been reviwed but I don't know what and don't want to give feedback on something that's not going to change becuase it's shipping

Dan: we don't have basis for review, asked for further info or we'll close. No feedback so far. Then we talked about COOP same-origin-allow-popups thing.. question is have we provided the feedback we can provide? What's the value add we have to have this issue open? This is trying to close a security issue that is exactly the kind of security issue that malwares take advantage of. We want to support closing security loopholes. Not sure there's much more we can feedback on this. We talked about is the basic user need of using the technology that can be exploited and therefore this technique needs to be layered on top to stop the exploit - is that something strong enough user need .. use of sharedarraybuffer .. I don't think we have a good answer. The answer to that question from Mike was basically that doesn't matter becuase people are using it anyway and there's such strong usage of thsi technology that it would break the web to deprecate it so we need to have a fix, is my interpretation. We've asked for more developer research, we've asked for answers to concerns regarding complexity. 

Peter: I have an issue keeping all the coop/coep etc straight, what they're trying to do. When we talk to Mike it all makes complete sense but I can't reconcile that to what I'm reading in the specs. Things seem backwards when I look at the specs. I trust Mike that they're not designing something broken but I think we're missing a better way of explaining what all this is.

Dan: if things were starting from the user needs instead of 'sharedarraybuffers are often used'... it should say 'web developers want to do this becuase people want to do that, eg. log in across different sites. One technique used to do that is this. Developers often use a sharedarraybuffer in that context. Because of that it will create these vulnerabilities, therefore...' to me that's what's missing. Doesn't mean it's wrong, just difficult to parse.

Rossen: not only the security, difficulty comes from the process model and what they're trying to align to. Major benefit there is closing a larger security hole. I don't disagree about tying this back into user needs or practical scenarios.. I'm sure they will come up with those but it doesn't mean their specs will be less complex. Or the way they are interlinked with each other. One document he sent out.. that tries to tie everything together: [notes on threat model of cross origin isolation](https://arturjanc.com/coi-threat-model.pdf) paints a decent picture of the technical problem and solution. I found the motivation here pretty decent as an engineer reading this

Dan: is that referenced in our issue? I don't think it is

Peter: there is a reference to the post spectre web dev which has a reference to this document

Rossen: I think the other issue remaining is how all of these features are intended to adopt legacy content. What is the default use case for the legacy content that's not capable of changing? Not able to change? They did a good attempt at describing their approach to acquiring new content and trying to onboard legacy content with some defaults but I didn't see that in any of the documents, I didn't see a clear explanation saying these are going to be the default policies and these are the consequences of having defaults. Are they making it better or worse? I can't answer thi squestion. If the default case is not making it better for eg. Tim's website from 30 years ago that is not going to change... I feel like we already left that feedback

Peter: we've talked about that in one of the other CO* issues. I understand due to spectre you need to isolate things and there are cases where you don't want to isolate or it breaks functionality, but these switches seem to be opting into isolation rather than out of. Given how hard CORS is to get right, I'm worried that developers will get this right. Is this deployable?

Ken: is there any statistic on the usage? I guess a lot of people are not becuase its ver complicated?

Rossen: the existing expiermental stuff?

Ken: all the coop/coep stuff - it's opt in. How many sites opt in?

Rossen: isnt' the current status that they're trying to get this off the ground?

Ken: I don't now. Some is already there? 

Rossen: CO embedder policy.. whoever is embedding stuff, it's their policy

Ken: how does this relate to iframes with geolocation and policies..? Already existed for a while

Rossen: it's a little more than that.. in a way that you're able to create.. One of the issues we were reviewing had a good explanation for what you're talking about. Cross origin iframes..

Ken: just wondering whether people that actually want to deploy this can find a place to learn about what to do. Even today it's complicated. I kno wthese things exist, proactively looking for it you won't find out. Very big websites are going to deploy it but the long tail..

Rossen: that was exactly my previous point, about the legacy web and how do you adopt that

Ken: not just legacy, long tail

Peter: google, facebook, microsoft are going to deploy and that's it because nobody else has a team that can keep all this stuff straight.

Rossen: I don't think that's quite it. Even for those properties the problem.. a ton of user generated content you have no control over. Maps for example has loads of usergenerated content that is not moveable. What's your default policy? How do you embed safely? My question I didn't find a clear answer to is how are these defaults affecting me as the user? Are they status quo or better, or are they going to somehow compromise my security/privacy/rendering performance..?

Peter: my understanding is that what happens to legacy sites that don't opt into these headers are those that do cross origin resources are going to randomly break becuase they don't end up in the same process

Rossen: exactly. Safe defaults..

Ken: a popup blocked do you want to enable anyway?

Rossen: have we reviewed and signed off on all of the actual policy stuff? CO*? 

Peter: I don't think so

Rossen: are we back in this limbo where we're reviewing stuff built on thing snot signed off?

Dan: we have cross origin reporting.. origin isolation raised in 2020 (#464) is closed.. 

Rossen: I think I remember this

Dan: I don't think we specifically reviewed COOP and COEP

Rossen: it's cited here as adjacent work

Dan: I think they think that when we reviewed the origin isolation that that was inclusive of COOP and COEP. 

Rossen: I think that's right

Dan: I don't remember having a detailed discussion on COOP and COEP and the need to opt in

Rossen: what would be super helpful is if we can find a timeline and sequencing of all of these features and how they fit together. I asked for a document that ties all these things together from implementation point of view for us to be able to orient where everyone is, what we're reviewing.. reviewing something early? or something already shipped? I don't have a clear picture. They might be getting frustrated..

Dan: In this case they're prototyping and talking about it being part of canary in q3. I do'nt think we're at that stage wtih this, or CHIPS or some of the other things. 

Rossen: if we don't have the sequence knowing we've reviewed and have agreement on the base, ground level understanding of what's there and how stuff builds on top, it will be difficult ot hold all of that context every time

Dan; that is a common high level pattern for a lot of our work. We jump around so often between different parts of the stack. I keep coming back to.. the complexity of the topic but also comes back to not starting from user needs, and also the point that Peter was making that this is a technology designed for industrial scale web development rather than for individual web developers to understand. When you have a web security team then they will be the people that understand this technology but if you're a .. Can we feedback someof what we've said around developer complexity and how this impacts legacy content and reexamining the user need and understanding if there's another way to achieve this same user need without having to.. sholuld we (the web community) be encouraging web developers to not use sharedarraybuffer but some other technique if they're using sharedarraybuffer and we think there's a vulnerability

Peter: this is a developer feature. TO me it's mor elike if you want ot use feature x here's what you have to do and here's why. That's what I'm missing.

Dan: ties back to user needs with why ar eyou using feature x, and if you are using feature x to serve these use rneeds maybe there's a different way to serve these user needs, eg. web payment instead of having a popup window that requires this conplex security confiiguration.  Not everyone is going to be able to do that but feels like it's missing from the discussion

Peter: makes sense. To the extent that it could all be bypassed had we just built a different set of features, or if there are existing features that make you not have to worry about this. I'll try to leave feedback.

Dan: punt to virtual f2f in september

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Tess: needs Lea

Peter: tentatively for next week

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

Ken: it's about associated data that you propagate. Need to read in detail.

Peter: next week?

### [Request for review: CSS tree-scoped at-rule names and references (for @font-face, @keyframes, etc.)](https://github.com/w3ctag/design-reviews/issues/659) - @hober, @LeaVerou, @torgo

Peter: needs Lea as well?

### [FLoC](https://github.com/w3ctag/design-reviews/issues/601)

Amy: they responded ot say based on our feedback they're redesigning it. Close and ask to reoopen or open a new one when they have a new design?

Dan/Peter: yep

Amy: [closes with comment]

### Issue Triage
