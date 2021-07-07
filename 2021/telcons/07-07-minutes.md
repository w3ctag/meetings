# TAG Minutes

## Agenda:

### Breakout C (APAC / Europe) - [2021-07-06](https://www.timeanddate.com/worldclock/converter.html?iso=20210706T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Guidance for when to use inheritance vs composition](https://github.com/w3ctag/design-principles/issues/298)
* [Two new principles (actually one existing one recycled) for devices.](https://github.com/w3ctag/design-principles/pull/320)
* [Principle against tying APIs too closely to hardware](https://github.com/w3ctag/design-principles/issues/308) - @cynthia
* [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @torgo, @hadleybeeman
* [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2021-07-07](https://www.timeanddate.com/worldclock/converter.html?iso=20210707T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [credentialless embedder policy](https://github.com/w3ctag/design-reviews/issues/582#issuecomment-854093723) - closed but they are looking for some more input
* [Security & Privacy Pull 128](https://github.com/w3ctag/security-questionnaire/pull/128)
* [Add non-"fully active" document handling guide](https://github.com/w3ctag/design-principles/pull/317)
* [New principle: Guidance on User Activation](https://github.com/w3ctag/design-principles/issues/314) - @hober, @torgo
* [New principle: When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - @hober, @torgo
* [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306) - @hober
* [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281) - @hober, @LeaVerou
* [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - @hober, @LeaVerou, @kenchris
* [Add text for low-level vs high-level APIs (related to #117)](https://github.com/w3ctag/design-principles/pull/291)
* [the clipboard thing](https://github.com/w3ctag/design-reviews/issues/636#issuecomment-859967433)
* Breakout Rollup
* Issue Triage

## Minutes:

### Breakout C (APAC / Europe) - [2021-07-06](https://www.timeanddate.com/worldclock/converter.html?iso=20210706T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### [Guidance for when to use inheritance vs composition](https://github.com/w3ctag/design-principles/issues/298)

Punted to plenary.

#### [Two new principles (actually one existing one recycled) for devices.](https://github.com/w3ctag/design-principles/pull/320)

[reviewing PR]

Ken: maybe too wordy? not a fan of "try to".  

[Ken makes some proposed changes]

[we will pick it up at the plenary]

#### [Principle against tying APIs too closely to hardware](https://github.com/w3ctag/design-principles/issues/308) - @cynthia

[the issue for above]

#### [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @torgo, @hadleybeeman

[need additional examples]

Yves: we already have principles about units - maybe it could be linked to that?

[left some comments here]


#### [credentialless embedder policy](https://github.com/w3ctag/design-reviews/issues/582#issuecomment-854093723) - closed but they are looking for some more input

Yves: re-opened - they changed the Use case.. 

Yves: use case is comms between iframes / popups and main document - mostly for webassembly - they used sharedarray buffer - and for payments.  The goal is to allow it and gate it in some way - not open to any iframe.  The change is the way to restrict / not restrict it.  The current issue - allow subresources like images to be loaded credentialless instead of sending credentials - which is the default for using non-cors subresources. 

Dan: left a comment about venue

#### [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282) - @torgo, @rhiaro, @hadleybeeman

[will review at plenary]

#### [Security & Privacy Pull 128](https://github.com/w3ctag/security-questionnaire/pull/128)

[took a look at this and it needs plenary discussion]

#### [Add non-"fully active" document handling guide](https://github.com/w3ctag/design-principles/pull/317)

[also needs review in the plenary]

Ken: describing how that lifecycle works would be quite useful.

Dan: my first read of the text is that it's quite dense and may need to ...

Ken: a drawing?

Dan: could be helpful.

### Plenary Session - [2021-07-07](https://www.timeanddate.com/worldclock/converter.html?iso=20210707T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Lea, Peter, Tess, Yves, Hadley, Amy


#### [credentialless embedder policy](https://github.com/w3ctag/design-reviews/issues/582#issuecomment-854093723) - closed but they are looking for some more input

Dan: they are moving this to WICG. They've changed something about the approach and wanted us to reopen

Yves: no longer about communication between iframe, but subresource loading in an anonymous way

Dan: what additional value can we add? They asked to reopen because our response no longer fit. We said yes that sounds fine, but the 'that' is something the ended up not choosing

Yves: as it's a completely stripped down version of the original proposal I'll need to take a look again, and ensure different stakeholders agree, which might happen in WICG

Dan: take a look and agenda for next week?

Yves: yes

#### [Security & Privacy Pull 128](https://github.com/w3ctag/security-questionnaire/pull/128)

#### [Add non-"fully active" document handling guide](https://github.com/w3ctag/design-principles/pull/317)

Tess: there was a design review issue that these PRs come out of... I spoke to the people. I am on board with what they are trying to do but haven't reviewed the PR. It's to make sure the BF cache is taken into account. Hopefully this will ensure [good things].

Dan: concerned about editorial - current text is dense - and concerned with interop.

Tess: I think it does match [other implementations].  Editorially - Alice put in another work to re-write design principles to be friendlier - I've been trying to do the same to the s&p questionnaire. this PR needs work from that perspective.

Dan: will put these on the agenda for next week.

#### [New principle: Guidance on User Activation](https://github.com/w3ctag/design-principles/issues/314) - @hober, @torgo

Dan: related to the clipboard thing

Tess: question issue is posing - should we have a principle about user activation? My answer is both yes and no. We should have a principle about user consent, that some actions should require consent. User activation is a way of guaging consent. One of several ways. A permission prompt is a way. For instance, input type file gets user consentand doesn't have a permission prompt or necessarily user activation

Dan: this comes back to argument that Alex Russell made - why should clipboard api require user activation when file access doesn't. File access api has its own UI that comes up and directs a user to find a file. Completely differet things

Tess: exactly, that's the kind of nuance the text has to have. With the clipboard thing, cntrl+v is a clear signal to paste. If we consider that in and of itself enough, maybe there's an argument. But not just a user gesture, any kind of user gesture. I tapped on the page, therefor you can read my pasteboard? no. We already have text about meaningful user consent. Talks about meaningfulness. If a permission prompt is incomprehensible to a user is the consent meaningful? probably not.

Dan: one of our top principles is [ask users for meaningful consent](https://w3ctag.github.io/design-principles/#consent).

Tess: if we're going to have text about user activation it should be in that principle. Should have some nuance about a number of ways to get meaningful consent, a whole spectrum of it, depending on context, etc.

Dan: wondering if we already said it. *reads* Doesn't really get into the nuance of sometimes consent is an explicit prompt, sometimes consent is implicit, depending on power of API you really need to figure out which you need

Tess: I think later on we... we don't. Input type=file is a fantastic example of an API that doesn't have an explicit consent check but clearly gets implicit consent in a very strong.. very strong signal. Doesn't require anything else. That should be discussed in there too. An example of a good API that is a powerful API that is able to gauge meaningful user consent in a different way that is still valid and good. Might also be [text in security and privacy questionnaire](https://w3ctag.github.io/security-questionnaire/#personal-data).

Amy: I can take that

Hadley: do we ever describe what we mean by 'powerful'? Line is hard to navigate, but context - power is multidimensional space. Narrowing it down a little is helpful

Tess: We should try to put words to it, but worried we'll leave out things we intended to leave in. That's the fun of language.

Hadley: something in what's at stake for the user.. hard to talk about without use cases

#### The clipboard thing

Dan: related - more back and forth about pickling async clipboard API. We get into [discussion](https://github.com/w3ctag/design-reviews/issues/636#issuecomment-859967433) about general issue of when the async clipboard API should have access to your clipboard. They've tried to address by adding additional requirements and strict language around user activation. Core issue remains. Not an issue on the pickling situation as much as async clipboard. Issue is [clipboard api issue 52](https://github.com/w3c/clipboard-apis/issues/52) which is still open. But getting language that it's closed and already shipped. Anyone have further insight?

Tess: no. Last time we talked about this - I think they need a new concept here, I don't think switching from sticky to transient acivation is enough. They need to distinguish different kinds of user activation. Specifically any user gesture isn't good enough. It needs to be a user gesture wehre here's a clear intent. The browser can tell that the user's intent is to give read access to the pasteboard. Cmd+C cmd+V are clear signals. Choosing paste from the menu bar is a clear signal. Tapping the screen is not. Given the sensitive nature of what people have on their pasteboards... a lot of password managers use it. You  need to really believe as a browser that the user actually meant to paste or copy. There isn't an existing spec term for that. They need to make it up and write it down. Switch from sticky to transient is good - necessary but not sufficient.

Dan: write that in issue 636?

Tess: I'll write it in issue 52, it's still open

Dan: note that it's a TAG view

Tess: what I said matches existing webkit behaviour. 

Dan: I'll write the feedback to clarify that this is TAG consensus.

`As discussed on [today's TAG call](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/07-05-agenda.md) - we think the user activation requirement needs to be very strong - e.g. ^v or selecting paste in a menu.  As I wrote in [this comment](https://github.com/w3ctag/design-reviews/issues/636#issuecomment-857829725) on our issue on the pickling review, we think there are some abuse scenarios that are not being given enough weight in the discussion here. It should **not** be possible for a web page to have access to the contents of a user's clipboard without a very high bar of informed consent.  This is pretty fundamental to what sets the web apart from other platforms in terms of user safety. Since this issue is still open, what can be done additionally to strengthen the spec (and implementations) in this area?`

* Peter: +1
* Hadley: +1
* Tess: +1
* Lea: +1
* Amy: +1
* Yves +1

Dan: [left comment](https://github.com/w3c/clipboard-apis/issues/52#issuecomment-875709431)

#### [New principle: When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - @hober, @torgo

Dan: I said I'd take a pass. Still nothing. Will continue working on it.

#### [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306) - @hober



#### [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281) - @hober, @LeaVerou

#### [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - @hober, @LeaVerou, @kenchris

#### [Add text for low-level vs high-level APIs (related to #117)](https://github.com/w3ctag/design-principles/pull/291)

Dan: After the discussion we had, I felt that having the nuanced wording about if you always start with low level it's probably not the right thing, you have to apply the right design decision based on how you think this technology is going to be used, and trying to thread that needle of that nuanced guideance

Lea: we're all in agreement that always starting low level is nto ideal, we haveexamples where it didn't work out like font enumeration api. Lack of clarity is about whether starting low level is sometimes acceptable. In the previous discssion some people thought its an antipattern to start low level, which is what the Extensible WEb Manfiesto is about. We need to be clear about whether the TAG stands behind the EWM and what the lessons learned are and what we'd need to change. I'd love to see those thoughts.

Dan: I don't think we should set it up as TAG vs the EWM. What's clear to me after the feedback I received after the minutes from the last discussion is that there are people who are positive contributors to the web community who are very passionate about the principles of the EWM and are worried about the TAG weakening it. 

Lea: I think they're rightly worried if the TAG believes that nothing should ever start low level

Dan: I don't agree with that wording, I don't think we should issue that

Lea: that was the conclusion from the previous discussion

Tess: I think the TAG at the time of the EWM the TAG probably didn't agree with it, then the new TAG got elected.. I forget the order..

Dan: the revolutinary new TAG came in...

Tess: the TAG changes over time, that's okay, it's not a monolithich thing that is identical to the TAG of the time

Dan: the ideas that are represented in the [EWM](https://extensiblewebmanifesto.org/) which were to do with layering and the idea that by building fundamental building blocks developers can iterate on top of those building blocks and make the decisions about what higher level apis work for them. I think that has an implicationn of using the mehcanisms of web components to do that, amongst other things. I think that is as relevant today as it was when the EWM was launched. However, it's not guideance that.. what we have learned is that in some cases it can produce bad results. In some cases. And that is why we need to have this nuanced wording about don't *always* jump in and think that we should be building only from the lower level. Think about the high level design that you want, the high level API you want to build, and then design the layering from the ground up to meet that design which can allow both things becuase the layering and by building the lower level you enable that creativity from the developer community, but you also give developer ssomething they can use which fits together with the web platform.

Lea: makes sense

Tess: yeah

Lea: something that describes a framework about how api designers can think about this and weigh the pros and cons of going high level or low level, instead of blanket recommending high level. Or the opposite, that would be equally bad.

Tess: one of the things here is a difference between what the EWM actually says and the lessons people took away from it and ran with for years. A lot of people seem to think we should only do low level stuff and anything higher than that we should leave to websites to have to do. Which is basically saying websites should forever have to cause a 10mb js download before they render

Lea: agree

Tess: people think that's what it means. THe people behind it it... Dan just said something about layering... is awy more nuanced than the lesson people took from it. What Rossen and I were saying last time is really all about that kind of nuance. I think where Lea might still be disagreeing is that there's an ordering in time about those layers that you end up with. When or if to expose them as API. What Rossen and I were saying is that in some cases it's definitely not necessarily the case that you shuld *always* expose the low levels as API. You need to properly layer things, that' sthe important thing. Then figure out what API you actually have to expose in order to enable developers to do the right hting. Sometimes that's a higher level or less powerful API. SOmetimes you dn't need to give people the footgun. You use fnt enumeration as a good example of a case where it's too low level. It's a good example because obviously any kind of higher level font picker has to be built on a model where there's a list of fonts somewhere. THe browser knows how to get that list of fonts and expose it to users. But then what API we expose to the web is just that high level one. One of the problems that the EWM was trying to fix was people adding high level api to the web without thinking about what is below this, what are the primitives that this is built on, and does it cohere with other features of the web that depend on slightly different primitives. One of the toints of exploring those layers and figuring out what they are is to notice I'm designing a new element that's exactly like iframe except different in 3 ways. If we could redefine iframe and my new thing in terms of a common model we could be explicit in the spec... just like fetch api.. this is how we hook into this model, we set these three things differently. The model doesn't have to be exposed, that's a separate question.... Is there an equivalence between model and api? A lot of the discussion around EWM stuff is that they are the same and I don't think they are. For instance the list of fonts that are available is clearly a concept that has to be referred to, but it's a bad thing for that concept to be API. 

Dan: The other examples that come to mind are more recent - the machine learning API; the device feature specific apis - I don't think those types of functinalities wer eon peoples minds when they wrote focus on adding new low level capabilities ot the web platform, or focus on standardising low level capabilities and building new features in terms of them. I think that what people were more thinking about other types of new web functionalities.. another example of where we have issued guidance to the effect of this should be more webby, more aligned with other parts of web platform, whcih has the implication of it should be a higher level api rather than exposing... however it still needs to be thought of in this layering approach. It's not easy. 

Lea: we all agree that layering is the ultimate goal eventually.. but like Tess said there is an ordering to it. People ahve to start somewhere. Whether they start high or low level isn't straightforward. I don't think there's any lingering disagreement about what Tess said. I think that all made sense. There's no disagreement about whether to expose low level primitives or not - sometimes they are, sometimes not. Any lingering disagreement is about the proposed lack of nuanced in the last conversation where it was like yes it's an antipattern to start low level. I don't think we can say this. I don't think we should structure the guidence around it. I don't think it's an antipattern. 

Tess: oversimplification of what Rossen was saying... 

Lea: I wanted to be crystal clear so I asked: Is it an antipattern to start low level? And I got yes it is

Tess: I tend to agree with Rossen. The goal here is to solve user needs. If you're not addressing a use case we probably don't need the api. Different use cases might require different levels of power, and differeing high or low level. All has to be traced back to a user need. We're clear about that elsewhere. Rooting thing sin user needs is..

Dan: that's the hook here. We've spent years reinforcing this poitn about user needs and starting with end user needs. The guidance abot how to design an api needs to be consistent with that. We can't both be saying start with user needs - implying hgih level - and also saying start from low level building blocks, because then you're nt starting with user need

Tess: font enumeration example illustrates this well. User needs to choose a font. Developer wants to design a UI for choosing a font. If you start with developer need, you end up with font enuemration API. User need is to pick a font, not for a website that you navigate to to know the list of fonts in your system. If we always bring it back to that user need, and the harms too, user harms, you might conclude that you don't need an api that's as low level or as powerful as that one

Lea: we all agree that security and privacy implications mean high level can be preferable - that can be epxlicitly stated. There are many cases where the quesiton of high level vs low level expses no further privacy and security and it's a case of ergonomics. It's not always obvious. There are tradeoffs involved. Sometimes a large bulk of author use cases which point towards a high level api which covers 90%. Other times the use cases are more scattered and no obvious high level api that will address them all. That's the nuance. 

Tess: that first one you mentioned - the case where you can hit 80% of the author needs with a higher level thing - it's a great example of what we want, and an example of the risk of doing it badly. If you think about the long tail of cases where that 80% high level solution isn't good enough, if you think about that you are more likely to end up with an 80% solution taht doesn't have an awkward cliff later

Dan: Lea do you feel confident to modify PR?

Lea: I think so. Seems we agree it's nuanced in cases where there's no security and privacy issue. I can iterate.

Dan: Yes.
