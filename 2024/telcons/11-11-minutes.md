# TAG Minutes Doc - Week-of 11 November 2024

## Agendas

### Breakout A (California / Europe)  - [2024-11-11](https://www.timeanddate.com/worldclock/converter.html?iso=20241111T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin
* [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk
* [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk
* Progressing TAG associates

### Breakout B (California / Australia) - [2024-11-12](https://www.timeanddate.com/worldclock/converter.html?iso=20241112T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou
* [CSS Masonry Layout](https://github.com/w3ctag/design-reviews/issues/1003) - @jyasskin, @LeaVerou
* [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss
* [CSS :open pseudo-class](https://github.com/w3ctag/design-reviews/issues/1010) - @LeaVerou
* [Spec Review for scroll-start-target](https://github.com/w3ctag/design-reviews/issues/1011) - @jyasskin

### Breakout C (Europe / China) - [2024-11-13](https://www.timeanddate.com/worldclock/converter.html?iso=20241113T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996) - @maxpassion
* [Review for Protected Audiences Bidding and Auction Services API](https://github.com/w3ctag/design-reviews/issues/1009) - @jyasskin
* [Early review request for "Explicit JavaScript Compile Hints"](https://github.com/w3ctag/design-reviews/issues/947)
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

### Plenary Session - [2024-11-14](https://www.timeanddate.com/worldclock/converter.html?iso=20241114T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [ Vision for W3C: request horizontal architectural review and wide TAG review](https://github.com/w3ctag/design-reviews/issues/1008) - @hober, @jyasskin, @rhiaro
* Planning for F2F
* More discussion of TAG associates
* Councils

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (California / Europe)  - [2024-11-11](https://www.timeanddate.com/worldclock/converter.html?iso=20241111T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Matthew, Peter, Jeffrey, Dan, Hadley, Tess, Lea

Regrets: Amy, Yves

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

#### [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin

Jeffrey: I don't think we're ready to post a position yet ... Martin and I have been going back and forth on this ... concerns about the use cases ... many TAG members seem to be OK with the "NASCAR" use case - i.e. removing the need to have all the payment type buttons.  But we might have to just say there's disagreement on the use cases / disagreement on the solution... 

... then there is a question of what to do with the overall fenced frames feature - don't know what the use cases are without this (#838) or protected audience.  #975 is one of the uses for fenced frames ...

... don't think fenced frames relies on protected audience but another use supports protected audience ...

... one thing the developer team might come back with - is a general argument embedding in the web ... "we want to do authenticated embeds" and the TAG might say "unpermissioned authenticated embeds are bad".  Storage Access and FedCM as alternatives - "do we have permission to join your identity".. We don't have a solution for embeds that don't join identities.

Hadley: I think we havea fundamental problem with it...

Jeffrey: I see a use case for an embedded google doc - if the UA is incharge of the UI... If you don't let the embedded page knowledge... Render the embedded page as if it were top level - and that it's not exposed to the surrounding page.

Hadley: isn't that still partitioned?

Jeffrey: yes that's .. segregated data .. supposed to act like it's partitioned. The thing we're worried about is showing the other partition inside of the current page. If the UA rendered a google docs document as if it's a top level navigation and placed it in the ... top level area of another page - maybe the UA could do something that's sufficiently clear... Not sure that would work but it seems the most plausible...

#### [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk

Matthew: I think this has no updates... essentially we asked for their idea about use cases... we particularly pointed out that they need to behave the same way... we really wanted to know about use cases... we asked. No reply. I periodically have checked the WHATWG thread and not much activity. 

Tess: No insight.

Peter: I also had concerns about feature detection... it would be nice to tell if it's available... people outside the TAG didn't seem to care. I think it's important.

Jeffrey: it's in a weird state - caniuse doesn't mention it https://chromestatus.com/feature/5111537299881984 says it's shipped - and somewhere else says it missed a window. So I will reply on the thread and ask what happened.  Also staff changes might have disrupted work on this.

*let's revisit at plenary*

[Reply on blink-dev](https://groups.google.com/a/chromium.org/g/blink-dev/c/qew_ILTXWSY/m/w02sznv5CQAJ): it did ship in 121 and is listed at https://developer.mozilla.org/en-US/docs/Web/API/HTMLSelectElement/showPicker as having shipped in Firefox too.

#### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk

Matthew: some further info...  They updated the explainer with some of the info we requested - explained occlusion and transparency, code samples, expect Lea might have some thoughts on the API shape. They didn't answer the question about "alternatives considered what about viewport capture"... we might want an answer to that...  [Explainer diff](https://github.com/screen-share/element-capture/compare/717d20ce9cd687433361e97495feb43d97011812...main#diff-b335630551682c19a781afebcf4d07bf978fb1f8ac04c6bf87428ed5106870f5)

Jeffrey: seems they have answered that [in the main thread](https://github.com/w3ctag/design-reviews/issues/954#issuecomment-2340918041) ...   We can mention again in our closing comment but it shouldn't block us...

Dan: Any changes to the spec itself? 

Matthew: No but much better explained now.  We could bump to the plenary with **proposed closed**.

Peter: I don't see any issues with the API shape...

Lea: on cursory examination seems fine...

*we agree to close by the plenary - Lea will raise any issues if she finds them*

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

*we review a draft comment*

*bumped to plenary with a **proposed closed**

Lea: I would also remind them of the issue "let's find a better name for this" but I'm fine with closing...  That was raised in our discussions.   Other thoughs: if we go fwd with the ID syntax - how do you specify something to be fwded to the element itself...?  Plan for the map is to set defaults - and override for specific attrubutes.  But doing one off overriding but not forwarding something, that's not possible...

Dan: we should ask that.  And not close yet.

#### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

Matthew: as expected - the thing I was checking for was confirmed - leads to another question... it does effect everything - from the a11y tree it will impact the visual order.  The question next : whether this means - e.g. if you have masonry layout if there is a change in the viewport size and the layout gets changed, should we need events to AT to let it know... Usually don't need this but I don't know. I could ask an AT vendor... perhaps we should ask this question about whether assistive technologies had got far enough down the path to know this...  Given we've got the 2 people in this thread - I'll post the question and then redirect to an APA thread if so...

Dan: just post that in our thread then... 

#### Associates

Dan: *will work on this wednesday*

#### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

Jeffrey: they announced a [dev trial](https://groups.google.com/a/chromium.org/g/blink-dev/c/0KHYC3wLay8/m/0v8qAu73CQAJ) ... 

Jefrey: fedcm is for a 3rd party but this is for using a 3rd party only for authentication - but on behalf of the first party ... 

.. the explainer doesn't actually explain the use case...

*we discuss CNAMES as an alternate way of supporting an oursourced authentication service*

Peter: hard to say CNAMES is a good pattern ...

Hadley: I think there is a clear distinction in the use cases, especially re how much you need to trust the third party. You have to trust whoever is doing your authentication, because they can authenticate as anyone. You don't have to trust you advertisers though -- that's not how the ecosystem works.. 

Dan: *posts [comment](https://github.com/w3ctag/design-reviews/issues/956#issuecomment-2468795045)*

#### Research and Web as a Commons

Jeffrey: web as a commons ... point of the chat with an academic is to talk to who we should be talking to ...

jeffrey: I think that the architecture of the web is that it is a comments... e.g. URLs... But there is this emergent stuff like users and sites and search engines and browsers all feeding eachother .. I think we should get input from people who study commons and other knowledge commons.  Keeping the web healthy by supporting the kinds of actors that keep a healthy commons.. 


### Breakout B (California / Australia) - [2024-11-12](https://www.timeanddate.com/worldclock/converter.html?iso=20241112T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Jeffrey, Peter, Tess, Lea

Regrets:

#### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

#### [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou

Tess: https://github.com/w3c/csswg-drafts/issues/6245#issuecomment-2469190377 might affect this.

Jeffrey: I have posted to ask about that.

#### [CSS Masonry Layout](https://github.com/w3ctag/design-reviews/issues/1003) - @jyasskin, @LeaVerou

Lea: The spec's intro is great but isn't an explainer. I agree with Webkit's argument to re-use syntax. I'm reasonably familiar with authoring grid and flexbox. Masonry examples were hard to understand with separate syntax. They're trying to be similar to flexbox, but having to comprehend an entirely new model was difficult. It's optimized to change one property to go from vertical to horizontal, but I've never needed that. With grid, I already understood how to make a template, and could port that understanding to masonry. But I'm still not sure how to do my top use case. I needed to apply a layout multiple times: gallery of images. Dont' want to apply a grid, so images almost always want some kind of masonry. Horizonally, with tracks between a min and max, and fill rows completely. Or vertically, and set a range of column widths. Some ideas of what to try with the grid-integrated syntax, but I'm not 100% sure. But I'm not confident they would work. One Chrome argument is you coudl have better default behavior w/ separate display mode. You could have smart defaults. If a part of the template is masonry, use that default. Also, Chrome's argument about re-using patterns instead of properties: I sympathize in general, but if we go that route, we should re-use more.

Jeffrey: What do you think about my review?

Lea: Don't disagree with much, but a lot is lower-level. Big picture dilemma about whether to re-use or not. There are warts either way. Slightly prefer to live with the integrated grid warts.

Tess: I mind ishadeed's examples compelling: https://ishadeed.com/article/css-grid-masonry/. Brevity of grid-integrated approach is compelling.

Jeffrey: I wasn't sure that it's likely to need to switch between the two layouts at a breakpoint. WebKit's argument shows that switching is easier with grid-integrated, but is that really going to be a common need?

Peter: Masonry isn't a grid, in the abstract sense. Grid is great because it replicates a hundreds-of-years-old layout system. Don't want to massage it into doing everything, instead of just making it do grid well.

Lea: Looking at ishadeed's article, I don't think it shows switching because it's common, but to show the delta between what's known and what is new. It shows how little you need to learn. Dont' think fallback shoudl guide the decision.

Jeffrey: A good use of the TAG opinion is to help guide which principles probably matter.

Lea: Authors struggle with existing layout modes. "You use flex to use 1-d, grid to use 2-d." Masonry is in between. Adding a third thing adds to the confusion. Maybe make it piggy-back on flex. 

Jeffrey: Since I don't know grid, I find that I bounce off of it because it's complicated. I learned flexbox fairly easily, and masonry seems similarly simple, but making people learn grid before masonry may be an obstacle to learning masonry.

Lea: Wrapping flexbox, comes close to a horizontal masonry. But designers don't like that idea.

Tess: Trying to reason about what we think is intuitive, isn't great. 1) The thing you know is intuitive, and the thing you don't know isn't intuitive. Flexbox has been usable for longer than grid. So think the idea of masonry being kinda like flexbox is interesting.

Lea: Think we're thinking of different cases: cases where flexbox is genuinely more intuitive. More control over items themselves. Better for having an arbitrary number of items. Grid is more specific, aside from autofill. Some weird semantics.

Jeffrey: We should try to approach feedback.

Lea: We're the wrong people to figure out what's intuitive. User research! Give authors a prototype of each syntax, and see what they do.

Jeffrey: Let's include that in our comment.

Jeffrey and Lea to collaborate in a Google doc.

Tess: Consider not giving feedback, since the experts are already arguing.

Jeffrey: I want to point out the "bad" argument from both sides.

Tess: And the good arguments!

Peter: Maybe help give them a framework to make the decision.

...

Tess: There are probably some properties here that shouldn't include either "grid" or "masonry" in their names, but should apply to both, maybe in slightly different ways.

Peter: Useful to have things that define the shape of the grid, and another class of things that sit on top of the grid and snap to grid lines.

#### [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss

Peter to draft a comment.

#### [CSS :open pseudo-class](https://github.com/w3ctag/design-reviews/issues/1010) - @LeaVerou

Peter: Do we really need `:closed` in addition to `:not(:open)`?

Jeffrey: Asked in https://github.com/w3c/csswg-drafts/issues/11039, which says we should remove `:closed`.

#### [Spec Review for scroll-start-target](https://github.com/w3ctag/design-reviews/issues/1011) - @jyasskin

Peter: "start" is normally an edge in layout. Use "initial" or some other word?

Lea: "initial" is ambiguous with the property value. Just ask them to discuss.



### Breakout C (Europe / China) - [2024-11-13](https://www.timeanddate.com/worldclock/converter.html?iso=20241113T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Max, Amy, Matthew

Regrets: 


#### [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996) - @maxpassion

Max: 2 comments - 1st one - looking at the explainer, although they have given some examples (examples section) it could be better to give examples from the real user experience perspective. 2nd comment - other stakeholders - webkit seems supportive but mozilla hasn't got back yet.  Cross-browser is very important for this feature.

Dan: they're talking about credentials but not the user experience of using passkeys. The objective is very low level, user experience they're trying to service is unclear. We should ask for user needs.

> Hi @nsatragno - thanks for sending this our way. It would help us to review better if the explainer were more clear about the user need you're trying to service.  You've described the problem statement and objective in low level terms but it's not clear the UX issue you're trying to tackle here. If you can describe start with user need, that would be helpful. It's good to see support from Webkit.

*max to post*

#### [Review for Protected Audiences Bidding and Auction Services API](https://github.com/w3ctag/design-reviews/issues/1009) - @jyasskin

*Discussion of PATWG and charter https://www.w3.org/2024/11/wg-pat-charter.html*

Amy: they haven't responded to Jeffrey's comment last week.

*punt to plenary*

#### [Early review request for "Explicit JavaScript Compile Hints"](https://github.com/w3ctag/design-reviews/issues/947)

Dan: Agree with Jeffrey this isn't in our wheelhouse. Although he commented that "in HTML and CSS we don't use comments, we use attributes or properties, and the equivalent in JS might be decorators."

Yves: decorators should be the way to go, especially with minifiers

Dan: should we be pushing back on this?

Yves: it doesn't look great but might be better for TC39..

Dan: but if it's to do with browsers?

Yves: it's not only limited to browsers, any server or js engine

Matthew: in what situation would you have a load of functions and not know if they were going to be needed?

Yves: if you were using a whole library, but in that case you can't decorate it or add comments

Matthew: agree if you were writing a library not all of it is necessarily goin to be used, but if it's something running in a browser or server there's some end program there and surely there wouldn't be some functions in it that it wouldn't necessarily need. If it depends what input the user gives and it could need them then it needs them and they should be there... how would you get in that situation? If you think about the libraries your code is calling you can use things like rollup and treeshake to strip out the bits you know you don't need. I'm used to the idea of stripping out bits that you know you don't need, where this is philosophically the opposite saying things might be needed. How would you expect the browser to behave differently?

Yves: especially you need to parse it to know if you need to parse it or not..

Matthew: genuinely interested in the use case...

> In general, the TAG is skeptical of introducing a pattern which introduces semantics in comments, it would be more useful to use decorators or another pattern that cannot be stripped. It seems like this is more general than just browsers, so we feel this probably should be a topic for TC39. We're going to close this for now and we encourage you to bring this to TC39 and come back to us.

*[closed as out-of-scope](https://github.com/w3ctag/design-reviews/issues/947#issuecomment-2472843239)*

#### Progressing TAG associates


### Plenary Session - [2024-11-14](https://www.timeanddate.com/worldclock/converter.html?iso=20241114T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Jeffrey, Martin, Dan, Peter, Tristan, Yves, Amy, Matthew, Max

Regrets:


#### [ Vision for W3C: request horizontal architectural review and wide TAG review](https://github.com/w3ctag/design-reviews/issues/1008) - @hober, @jyasskin, @rhiaro

Jeffrey: they would like comments by next week.

Matthew: when APA looked at it... we did't have a11y-specific things... but it's hard to see how this can be translated into actionable... I think it's ok for it to be high level but if you can't imagine how it can be actioned then it's difficult.  So being a bit more positive / action oriented is a good thing.

Jeffrey: I don't want to block it from being published until it's perfect.

Martin: I think this document misses the thing that W3C provides : technical competence in developing standards. This document ignores that. So I'm not happy with it. The entire basis for credibility is that it produces technical standards...

Amy: vision for w3c section ... I think we could capture what Martin suggested .. technical and credibility...

Yves: considering who is working on it - I think it's better to send them an issue rather than a PR - that keeps the ownership of the text.

Jeffrety: that's fine with me...

Dan: let's agree our comment by next week - meantime I will have a back-channel discussion to give them a heads-up.

#### Planning for F2F

#### More discussion of TAG associates

#### Councils

##### Consensus to re-publish Privacy Principles?
Diff at https://services.w3.org/htmldiff?doc1=https%3A%2F%2Fwww.w3.org%2FTR%2Fprivacy-principles%2F&doc2=https%3A%2F%2Fw3ctag.github.io%2Fprivacy-principles%2F

Dan: you have until end of week to notify of any objections otherwise we will assume consensus remtains to publish.

#### Questions for TAG candidates

Brainstorm in a Cryptpad...

#### Breakout Rollup

##### HTMLSelectElement showPicker() - 

Jeffrey: folks replied that it has shipped in Chrome and Firefox...

Dan: maybe say "we're gonna close but we would have appreciated a response"

Jeffrey: the WHATWG issue is still open.

Matthew: wondering what the default behaviour was...  We looked at this in APA - a WHATWG issue with a lot of discussion... about focus ... trying to clear up misunderstandings. That thread has stopped.

*Dan to write a closing comment draft*

##### ElementCapture

Matthew: from what I can see the API seems reasonable.  Lea said not to block on her.

*Matthew to draft closing comment and close as `satisfied` later*

##### ReferenceTarget

Matthew: I drafted a comment and Lea made a slight addition...

Jeffrey: Lea also posted a question.

Dan: let's wait for their reply and then close on that basis.


##### Protected audiences 1009

Dan: they still haven't responded so let's punt to next week.

##### Animation.progress

Jeffrey: we thought there was an update but it was unrelated so propose close...

Dan: multi-stakeholder story

Jeffrey: no answered standards positions but it's in the CSS wg draft

*we agree to close as satisfied*

##### Masonry

Jeffrey: The css WG would like to have a discussion next Wednesday... We should give them a comment... Lea and I have been working on it.  It doesn't answer question ...

Peter: Lea had some more thoughts...

Jeffrey: we should have some input sent to them before the call...

Dan: send the comment before their meeting - ask TAG people for review but don't block on it.


#### TAG Associates

Yves: Talked to Seth. He agrees with it.  Need to talk to Coralie about how to communicate it to the AC.  

Dan: *i can start writing a blog post*

Peter: we should be careful how we phrase... offer to those not elected ... 

Dan: Agree... 

Jeffrey: and they automatically expire at the end of the term... So the new TAG gets to decide.

Matthew: *raising issue of the horizontal review thread - tracking issues: https://github.com/w3ctag/tracking-issues/issues - these are smaller scope - but they can be helpful in figuring out what problems people are trying to solve on a day to day basis - but we never look at them.*

Dan: Maybe we can ask associates to help...

Matthew: we shouldn't completely delegate...  Some of these will be small some might turn into something big.

Dan: let's have this in the retrospective discussion.

Matthew: I'll have a look at the issues and give a description...

Dan: 2 topics for Edniburgh - 1. what key topics have come out of the tracking issues? and 2. how do we integrate this into our process in general?

Matthew: other groups do integrate.

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
