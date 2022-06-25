# TAG Minutes - Week of 20 June 2022

## Agenda

### Breakout A (Europe / US) - [2022-06-20](https://www.timeanddate.com/worldclock/converter.html?iso=20220620T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @torgo, @plinss, @atanassov
* [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
* [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov
* [CSS property object-view-box review](https://github.com/w3ctag/design-reviews/issues/740) - @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220621T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo
* [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss

### Breakout C (APAC / Europe) - [2022-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220621T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov
* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman
* [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman
* [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman
* [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman
* [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

### 
Session - [2022-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20220622T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)


* [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
  
## Minutes
  
### Breakout A (Europe / US) - [2022-06-20](https://www.timeanddate.com/worldclock/converter.html?iso=20220620T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Peter, Amy, Hadley
Regrets: 

#### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov



#### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
#### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @torgo, @plinss, @atanassov
#### [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss

Dan: no response to message 11 may...  Satisfied with concerns?

Peter: Don't know..  Yes but the concerns aren't concerns I think we can blow off. I'd like to see those concerns addressed.  Don't want to block this. 

Lea: won't this issue be present every time a new block element is added to HTML?  So every time we...

Peter: depends on what the closing tag rules are.

Lea: but most block elements close P tags..   Don't think we should be in a state where we can't add new block elements due to architectural concerns.

Peter I ageee - but this fundamentally breaks backwards compat promise.

Lea: we have precedent though....  Dit these cause problems?

Peter: We can get away with making breaking changes - we have done it. But everyone who breaks things needs to be aware of the consequences...

Lea: I think there's already a high bar.  I'm not sure what's the alternative.  We do want to be able to add new block elements...

Peter: alternative is to add a new syntax - or declarative mechanism - to indicate ...

Lea: signifigant overhead

Peter: could be a micro-syntax.. tells the parser it has this behaviour.  For example we could re-introduce the self-closing tags and have that behaviour. I think these are mistakes of the HTML5 parsing algo - and we're paying the price for those mistakes.

Dan: how about close with concerns and a post about this issue? Raise awareness that way?

Lea: fine by me

Peter: we could also open another issue just to track this. But we can't file an issue on ourselves, we need to get other html people to be thinking about it and agreeing it's an issue

Dan: could also invite anne to a call in the future. When everything is in a review it limits our ability to think about big picture issues. We don't want to block this review. We have to have a mechanism where we can bring the topic up in a wider way. TPAC session?

Peter: fine closing this with concerns and doing something else to raise the issue and get traction...


#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
#### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

[reviewing last comment](https://github.com/w3ctag/design-reviews/issues/725#issuecomment-1138032023)

Lea: Reasonable question.. prior art..

Dan: lets punt to plenary but also maybe for B.

#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

Lea: still haven't found time for substantial review.

Lea: proposal for where authors use the checkbox hack. CSS has a checked pseudoclass. CSS authors need state and there's no way to have state without writing js they end up making apps that use hidden checkboxes to maintain state, and sibling selectors and the checked pseudoclass to affect parts of the page, and use labels to check and uncheck these without having visible checkboxes. This lets authors turn any element into a togglable state, either between two or multiple states.

Dan: making CSS more apocalyptically smart? Good use case to not have to rely on a hack

Lea: user needs are quite extensive.. tabs, accordians, sumamry & details, etc... [lists loads]

Dan: what's the concern?

Lea: none, just substantial proposal and early stage, so we could influence, so want to look at it properly. Syntax is entirely new.

Dan: developers are doing this anyway so lets give them a proper way?

Lea: yes

Dan: multistakeholder support?

Lea: OpenUI CG.. people working on it are google

Amy: any alternative proposals for the same use cases that are competing?

Lea: not that I know about

Dan: in alternatives considered there's a previous year [old proposal css toggles](https://tabatkins.github.io/specs/css-toggle-states/), and [declarative show/hide](https://github.com/flackr/declarative-show-hide).

Lea: looks like evolution

Dan: worth asking about level of consensus in CSS WG?  

Peter: declarative show/hide is just prior art not competing. Visual state that is not part of the application state - can't reproduce from the URL bar. I can get my UI into a state and share the link and they're not going to see what I see. Or bookmarking after clicking on things. I know we've talked before about the difference between document state and visible state. Is this something we should consider a mechanism to encode this somehow that can be recreated?

Dan: this proposal would have that issue, but the current use of checkboxes would also have that issue. if we're doing something to actually fix or create a proper way to do this then maybe it should also have this state preservation mechanism.

Peter: in theory the checkbox hack does have the problem.. lots of apps that have state that don't refelct in the URL. The checkbox hack at least lets me serialize the document and bring it back in, because its stored in the DOM, it's presreved. But here there's no way to preserve the state unless you use a script

Lea: if you want to be able to share state through URLs even with checkbox hack you would need to do something..

Peter: right

Dan: they explicitly list this in their [non-goals](https://css.oddbird.net/toggles/explainer/#non-goals) - managing application state

Lea: line is blurry between application state and css state. Which tab you have open from an accordian, is that application state or css state?

Peter: presentational state.. I haven't switched a mode in the app or doc or whatever. If i have the same app oepn in two windows I don't necessarly want that change to refelct in the other window. If I'm looking at something and I want you to see a link and see the same thing I'm seeing, I want to send a URL and have you see the same view.

Lea: that's a good example. The other example about toggling dark mode. if you toggle in one tab you probably want it to toggle in the other tab. Does that make it application state?

Peter: could be. I think there's a mechanism for reflecting this because there will be a js api

Lea; regardless of whether this was designed for application state or not people are probably going to use it as well assuming it's easy.

Peter: in which case the spec should have clear guidence as to these are the types of things you do and don't want to use it for, and the reasons why. We have a lot of examples of apps that don't use urls properly. I'd like to not create a whole new way of web apps doing things badly.

Lea: not sure it's realistic to require the entire page state to be passed through the URL

Peter: no. There's probably lots of examples of places where you wouldn't want the state to be passed - eg. scroll position. It's a judgement call as to what should be reproduced. Some things like if I give you a url that is targetin gan anchor then one might expect css to apply to expose that anchor, eg. if it's inside a details element that should be open. I don't know how that works here.

Dan: noted it's in a personal repo

Peter: what's their normal work pattern?

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/730#issuecomment-1160656643)

Dan: but is there a more substantive comment we can leave about state?

Peter: I agree it's a non-goal but there is the other kind of hybrid display state [blurry line] to that end - does the spec have any text explaining that people should not use it for application state and explaining the difference?  People will use it for application state and get it wrong.

Peter: I can leave a comment.

#### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss

Dan: noting a11y community [feedback](https://github.com/w3ctag/design-reviews/issues/732#issuecomment-1159814503) - nice to see.

Rossen: assume it's going to evolve through appropriate WGs..

Lea: corresponding attribute to element internals? how can componenets have it by default? Can see many use cases

Rossen: absolutely. Any type of list control. Good question. The example (19) is more or less exactly that.

Dan: this explainer is very developer mindset focussed. Not stating things in terms of the user need. What we're talking about is an accessibility issue, so what accessibility problem are we trying to solve. Is that spelled out?

Rossen: in the goals

Lea: not trying to solve a11y per se, but a developer pain point about accessible interfaces. Helps accessibility indirectly.

Rossen: and connecting the other end with ATs so they can build on top of this. No accessibility solution that don't includde 3 parties - developers, engines, and the screen reader / etc technologies. Unless all of these things work together you don't have an accessible solution. Which one of these are you asking about?

Dan: trying to parse the user need from the explainer. Could be better spelled out.

Lea: I'd like to see a response to the point [in this comment](https://github.com/w3ctag/design-reviews/issues/732#issuecomment-1159814503) - seems like a reasonable question.

Dan: can you amplify the question?

Lea: yeah

#### [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov
#### [CSS property object-view-box review](https://github.com/w3ctag/design-reviews/issues/740) - @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220621T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

#### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

#### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

#### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Rossen leaving note abour explainer.

Peter left comment about not being async.

#### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

#### [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss

### Breakout C (APAC / Europe) - [2022-06-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220621T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Sangwhan, Lea, Amy, Yves

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
#### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

Hadley: K has said they are [looking to disentangle](https://github.com/w3ctag/design-reviews/issues/654#issuecomment-1136542117) this from FPS

Yves: I think we should wait...

Hadley: same thought process. They've changed their explainer 5 days ago...  *has a look* I think what they're saying is essentially : if a site is part of a first party set then the double keyed cookie is double keyed to the first party set rather than the specific domain but if it's not then everything operates according to domain / origin.  So it works with first party sets but not dependent on them.  So we can ask her if it's stable.

Sangwhan: I think it's better for the fate of CHIPS to be apart from FPS.

Hadley: it's opt in. have we talked about why people would opt in?  Content authors?

Dan: is it that it will be required?

Sangwhan: regulation might require it?

Hadley: they're aiming for it to be the only 3rd party cookie there is - because more privacy respecting. But not clear on how we get from here to there.

Dan: seems familiar like discussion with fenced frames.  Maybe worth asking that Hadley?

Hadley: alright.

Hadley: from [K's comment from 2021](https://github.com/w3ctag/design-reviews/issues/654#issuecomment-897950019) it sounds like they are expcecting browsers to enforce this. Do we know anything about buy in from other browsers?

Sangwhan: it seems like this functionality has been explored by multiple browsers - firefox and safari - similar behaviour.    

Hadley: safari has double keyed cookies

Sangwhan: I think they had to revert and do a lighter version...  Part of ITP...

Amy: it's in Chris Wilson's private repo right now...

Dan: [Chrome status](https://chromestatus.com/feature/5179189105786880) lists Safari and Firerox as having "positive" consensus. 

#### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou

Hi @vmpstr,

@cynthia and I discussed this again today in a breakout today.
On attribute vs CSS property we definitely think this is more suitable as a CSS property. This way it is easier to use it for creating defaults, including in Web components, and also given that it interacts with other CSS properties.

We are still not sure about certain details of the proposed algorithm, including my question from above about nesting higher priority elements inside lower priority elements.

We would like to see some examples of actually using the feature to target the user needs you are targeting. Are all these values necessary to address these use cases?


#### [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman

Amy: they responded to Hadley's feedback

Dan: I think they took our feedback on board. We can close this?

Hadley: fine with me

#### [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman

Amy: they lean heavily on a non-normative document... asking how they test for conformance... They have 2 security docs... Also looked through the [PING minutes](https://www.w3.org/Privacy/IG/summaries/PING-minutes-20220519#web-of-things-architecture-privacy-review)... Will check in with Tess.  lots of non-normative text in arch document. I went through the MUSTs and SHOULDs... a few are redundant... some seem like they could live in other specs... Some seem pointless / not conformance statements. 

Dan: more like a value.

Amy: you wouldnt' be looking at the spec if you weren't in some kind of network... Seems like it's not worth having it there. Whole arch section marked as non-normative... made a few suggestions for how they might rearrange the doc.  And then just reposition and turn arch doc into a note. Feel it would be much more digestable.  

Hadley: happy to ship this feedback - strengthened a bit... it would help the spec authors to think about it better to meet the needs of their users... tie it to "implementers' needs"...

Max: very good start. One comment regarding the last part - concern about abuse of connected devices.  Not relevant to this draft... the concern you raise is concern about general internet of things.  For example connecting devices to the web platform may cause concern.

Amy: my thought is that .. when bad things happen outside the web .. when they happen on the web the harm is amplified because it connects to more people. I can make it more clear.  Any potential abuses on internet connected devices would be amplified.

Dan: to amplify that... one feedback we had in the previous review was that we want the web to be a more ethical platform, which is why we wrote the Ethical Web Principles. We want the people building the web to be thinking about these use cases and to be building in mitigations. So when you use the Web of Things, it's less possible to abuse the system like you can with Internet of Things devices.

...It's one of the things that may have prompted them to include lots more security and privacy stuff in 1.1, which is great. We want to positively reinforce that, and add that we have additional thoughts, in a way that is not hitting them over the head.

Dan: Amy you are empowered to edit this feedback with the above comments taken on board and post it. And mark the issues as **proposed closing** so we can close at plenary.

Amy: I will also send a comment to discovery

**Amy's draft feedback:**

```
Thanks for the review request, and apologies for the delay. Being unfamiliar with the Web of Things work previously, I have done my best to review the set of related specs (Architecture, Description, Discovery, and security and privacy documentation) as thoroughly as possible.

We discussed this during our meeting today, and this feedback represents TAG consensus.

## Security & Privacy

Overall we are happy with the direction, and really appreciate the extensive security and privacy work that has been done. Treating all Thing Descriptions as if they contain PII is a sensible precaution. Making the Security and Privacy considerations normative makes a strong statement, though we'd like to know how you have been testing these requirements for conformance purposes?

The spec refers normatively to the [Security and Privacy Guidelines](https://w3c.github.io/wot-security/), but this is a NOTE, not a normative document and so can't be used as a normative reference. Are you planning to republish the Guidelines at some point (as it seems to have been updated since its last publication)? Also the [Security Best Practices](https://w3c.github.io/wot-security-best-practices/) document appears to currently be unpublished - what status are you planning to give to this? How does it relate to the Guidelines?

## Architecture

Regarding the Architecture specification specifically, the vast majority of the text is non-normative, and, while interesting and useful, we are not sure is appropriate for a REC-track document. Further, you have sections marked as non-normative (eg. [8. Abstract WoT System Architecture](https://w3c.github.io/wot-architecture/#sec-wot-architecture)) which contain normative MUSTs and SHOULDs.

Some of these statements could be moved to other REC-track documents - eg. regarding Thing Descriptions - if the relevant documents don't already make the same statements.

Some seem to be entirely unnecessary - eg. in [8.1.2 Links](https://w3c.github.io/wot-architecture/#links), that "Things MUST be hosted on networked system components [..]". Apologies if this has been misunderstood, but this seems more of a foundational premise than a feature to test for conformance purposes.

Some are redundant - eg. in [12.1.1 Thing Description Private Security Data Risk](https://w3c.github.io/wot-architecture/#sec-security-consideration-td-private), "MUST ensure that only Public Security Metadata is ever stored" and "MUST ensure that no Private Security Data is included" seem to be saying the same thing from different directions.

There are a number of normative references to non-normative documents - in [one case](https://w3c.github.io/wot-architecture/#bib-solid) to a document index rather than any specific specification - which need to be made into informative references.

Having reviewed all of the MUSTs and SHOULDs in the specification, our thought is to break the Security and Privacy sections into a separate, fully normative, Security and Privacy document. Then, to work through the remaining normative statements to see which are strictly necessary (ie. for interop, and testable) and of those which can fit in existing REC-track documents. The remainder of the Architecture document would work well as an informative NOTE, which provides additional background and context without implementers needing to sift through it to find what they actually need to design and build conforming Things.

We recognise that you've only asked us to review the difference between 1.0 and 1.1, and this kind of feedback is coming as a result of me personally not having been involved in the earlier review. However, given comments [1, 2] about how hard this has been to review, we'd say it's never too late (or too early) to make specifications more readable! We would be more than happy to re-review if this change is made.

[1] [2022-05-19 PING minutes](https://www.w3.org/Privacy/IG/summaries/PING-minutes-20220519#web-of-things-architecture-privacy-review)

[2] [2019-07-11 previous TAG review comment](https://github.com/w3ctag/design-reviews/issues/355#issuecomment-510337214)

## Compatibility

We can see a lot of work to survey the current (and, presumably, ever-changing) landscape of IoT devices, and the effort to bring fragmented ways of operating together. Can you summarise, or link to a summary of, what the compatibility story looks like in practice? Eg. what widely used devices would be compatible with this architecture out of the box? Or what would needed to be added to make them compatible? What is practically possible with what is out there today, if this suite of specs are published as-is? A few concrete examples would be really nice to help give us a better picture of the ecosystem.

## Bonus points

From an editorial perspective, implementers who are approaching this set of specifiations for the first time may be deterred by the volume of text. In particular where sections or paragraphs do not relate to specific, implementable requirements. The specification abstracts are all rather long and we think all of the specs would benefit from a thorough proof-read, with an eye to removing redundant text, simplifying language, removing filler, and overall shortening throughout. While background and context are useful, we would encourage containing such sections in their own documents, which may be optionally read, and keeping only the informative language that is really crucial for implementation in the specifications themselves.

We remain naturally concerned about the potential for abuse using internet-connected devices, most of which are in some way very personal even where they might be part of a large network, in a smart city or similar. The Web can further amplify such threats, or make them easier to carry out. We recognise that there is only so much that can be done in a technical specification and that ultimately you have little control over how malicious people or groups might use or mis-use devices or networks. That said, if members of the WG could find time to work through the [Societal Impact Questionnaire](https://w3ctag.github.io/societal-impact-questionnaire/), we would be very interested to see some discussion or notes on some or all of the questions from the WoT context. This is a draft document, and a work in progress, and filling it in is not a requirement for progressing the TAG review. (Feedback on the questionnaire itself, additional questions, etc, are all welcome too.)

Thanks again for your work. We anticipate closing this and the related issues, but await your acknowledgement of our feedback and an indication of your next steps.
```

#### [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman

Amy's draft feedback:

```
Overall, the direction of this looks good. The two-stage discovery process seems sensible to us. What use cases can be met after only carrying out the first step?

We note that you have deferred work on geolocation queries. This is something we will be very interested to review in the future from a privacy and security, and general social impact, perspective. We would welcome early review requests on this as your draft progresses.

The [related work](https://github.com/w3c/wot-discovery/blob/main/explainer/Explainer.md#related-work) section in your explainer contains references to other work but without any links. Could you add some?

Please also see the [review for the Architecture specification](https://github.com/w3ctag/design-reviews/issues/736#issuecomment-1162135635) as this contains feedback that concerns all of the related specs.
```

Dan: +1

Hadley: looks good to me.


#### [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman
#### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou
#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Dan: they haven't responded to my feedback  - I will ping Chris H. from google.

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

Dan: will ping Chris H. on this as well.

#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

### Plenary Session - [2022-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20220622T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Yves, Rossen, Max, Lea, 
Regrets: Amy, Hadley

#### [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss

#### Breakout Rollup
#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

##### [import.meta.resolve](https://github.com/w3ctag/design-reviews/issues/746)

Lea: I have an interest.  

#### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

**re-reviewing the explainer**

Dan: wondering about privacy - what if the user has a private session with the web site in question and also a non-private-browsing-mode session? Can data leak in that case? No mention of private browsing or incognito.

Dan: Generally concerned with any API that deals with history as this can be privacy-impacting.

Lea: it's being prototyped so we could play with the navigation and get first hand experience in using it... 

Dan: a little unclear about the [impact on the back button](https://github.com/WICG/navigation-api/blob/main/README.md#impact-on-the-back-button-and-user-agent-ui) user agent UI section of the explainer. 

Dan: a little unclear on the [joint session history](https://github.com/WICG/navigation-api/blob/main/README.md#correspondence-with-the-joint-session-history) I think the definition needs to be expaned or if it's defined somewhere else then there needs to be a linked. 

Peter: history interface on window() - the overall history of the browser. 

Dan: but this API is origin bound - 

Lea: need to be contiguous as well - only see the history entries from the latest browsing session - which seems reasonable.

Dan: would that address the private browsing mode issue I raised?

Peter: it would create another top level browsing context. Since this is related to the current session on this document it couldn't talk to another session in a private window or vice versa.  And if you go from A to B back to A 2nd instance of A can't see earlier entries from A.

Lea: it's a very large API.  The basic stuff seems reasonable.

Sangwhan: I looked at this and it looks like a good idea. API looks fine to me.

Lea: it's scoped to a single window. Private browsing is a red herring because even in normal.

Dan: they have answered "no" to the private browsing mode question in S&P questionnaire... 

Sangwhan: in some browsers you can re-open a closed private tab - behaviour isn't standardized there.

Lea: in chrome's implementation if you close a tab and re-open it the history is preserved - including in the navigation API.

Dan: is that desirable?

Lea: Yes.

Sangwhan: yes.

Sangwhan: I'm positive - I've used the alternative - push state. and this is an improvemt.

Lea: I'll second that.

```
Hi Domenic - sorry this took so long.  We've been reviewing and have had the chance to discuss on today's call. Some feedback from that session: In general we're happy with this API. We appreciate the care taken in the security & privacy considations section. One question I had was about how this impacts the behaviour of the back button - it wasn't exactly clear what you mean by "when iframes are involved" here. Can you spell it out a bit more clearly?  Is this to do with the iframe's navigation history being integrated with the parent document's history?  And what is the changed UI you anticipate?  Generally we have positive feedback. This looks like it will be an improvement over the current state of the platform. We're planning to finish the review and close next week.
```

Dan: [posted](https://github.com/w3ctag/design-reviews/issues/717#issuecomment-1163299281)

