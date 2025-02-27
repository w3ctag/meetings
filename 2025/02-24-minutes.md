# TAG Minutes - Week-of 24 February 2025

## Agendas

### Breakout A (California / Europe)  - [2025-02-24](https://www.timeanddate.com/worldclock/converter.html?iso=20250224T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [(brand new ✨) Web Install API](https://github.com/w3ctag/design-reviews/issues/1051) - @torgo
* [Unicode MessageFormat 2.0](https://github.com/w3ctag/design-reviews/issues/1042) - @jyasskin, @torgo
* [Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @jyasskin, @csarven
* [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @marcoscaceres, @hadleybeeman
* Paris Agenda Planning

### Breakout B (California / Australia) - [2025-02-25](https://www.timeanddate.com/worldclock/converter.html?iso=20250225T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [CSS `shape()` function](https://github.com/w3ctag/design-reviews/issues/1033) - @martinthomson, @xiaochengh
* [Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @jyasskin, @csarven
* Paris Agenda Planning

### Breakout C (Europe / China) - [2025-02-26](https://www.timeanddate.com/worldclock/converter.html?iso=20250226T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Normative Changes of the Input Events Level 2](https://github.com/w3ctag/design-reviews/issues/1019) - @matatk
* [CSS Inline `text-box`, `text-box-trim`, and `text-box-edge` properties](https://github.com/w3ctag/design-reviews/issues/1021) - @xiaochengh
* [CSS Scroll Buttons](https://github.com/w3ctag/design-reviews/issues/1054) - @xiaochengh
* [CSS inert](https://github.com/w3ctag/design-reviews/issues/1055) - @xiaochengh
* [WebRTC API Proposed Amendments](https://github.com/w3ctag/design-reviews/issues/1026) - @matatk, @lolaodelola
* Paris Agenda Planning

### Plenary Session - [2025-02-27](https://www.timeanddate.com/worldclock/converter.html?iso=20250227T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* Paris Agenda Planning

## Minutes 

### Breakout A (California / Europe)  - [2025-02-24](https://www.timeanddate.com/worldclock/converter.html?iso=20250224T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Lola, Hadley, Sarven, Jeffrey

#### [(brand new ✨) Web Install API](https://github.com/w3ctag/design-reviews/issues/1051) - @torgo

Jeffrey: I left a comment saying "they haven't addressed"... I think we can postpone... 

Dan: breakout on this at the f2f?

Jeffrey: their [non-goals](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/WebInstall/explainer.md#non-goals) .. a bunch of capabilities around how you pick applications... Talking about the whole problem space makes sense...   They are clearly looking at this whole space. Our perspective should be about the space.

Dan: they think they have addressed some of the concerns that we have raised...  

Jeffrey: I could leave a comment asking them ... 

Dan: Yes please...

*jeffrey to leave comment*

#### [Unicode MessageFormat 2.0](https://github.com/w3ctag/design-reviews/issues/1042) - @jyasskin, @torgo

Jeffrey: the glance that I've taken, it looks fine..  Will look more. Not for Paris.  Suggest bump to after f2f.

Dan: Will do.

#### [Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @jyasskin, @csarven

Jeffrey: Martin has been iterating on this... 

*Rescheduled for breakout B*

Sarven: concerns about compromised keys and manifests...

Jeffrey: i do think they talk about compromised keys (rotation)... manifests yes.

Sarven: Asked about signed manifests: https://github.com/w3ctag/design-reviews/issues/1041#issuecomment-2679225817

#### [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @marcoscaceres, @hadleybeeman

Hadley: we are waiting for Marcos's feedback... 

Jeffrey: he said he would have a chance to look at this in a couple weeks... I will poke.

Yves: giving a deadline... saying we have a f2f and will give an update after that...

Dan: Would prefer to close this before Paris.

Jeffrey: I think it's ready enough...

#### Paris Agenda Planning

Lola: i'm closing the form (asking developers which issues we should prioritise) at 1pm tomorrow UK time, but I'll share once more this evening for the American folks.

It's mostly CSS stuff. 1021 (though it's proposed-closing), 

Torgo: in the meantime I've created a sheet to collect design reviews for our f2f agenda planning. (reviews methodology)

Lola: and incremental font transfer, https://github.com/w3ctag/design-reviews/issues/1057, has a lot of interest and is on people's radar. Don't think it needs discussion at the f2f though.

Jeffrey: we probably don't have to discuss a lot

Yves: if I recall correctly, they are resubmitting it

Lola: also 1054, CSS scroll buttons

Jeffrey: this is the carousel group

Lola: maybe worth discussing the whole thing? https://github.com/w3ctag/design-reviews/issues/1037 

[agreed]

Lola: 334, HTML modules 

Jeffrey: feature itself got stalled but parts are moving fwd in CSS...

Jeffrey: let's ask Dan Clark if we should discuss at the f2f?

Hadley: I will leave a note to ask him

Lola: Also, I'd suggest Device bound session credentials, 1052. Privacy, does it reinforce the idea that cookies are not going away?
  
And 1050, permissions policy reports for iFrames. 

Jeffrey: device bound session credentials - reducing the number of times that sites make you log in again...

... no bucket for permissions policy reports...

#### Sidetrack on [fetch metadata request header](https://w3c.github.io/webappsec-fetch-metadata/)

Dan: any reason why this hasn't been promoted to CR?

Jeffrey: not sure.. though some issues have been reported with header size...



#### Associates at F2F

Jeffrey: we should have a teleconference going and invite / welcome to everything but not expected to attend.

Hadley: OK - sounds sensible - we need to think if first session is just about the TAG...

Torgo: for this f2f, maybe emphasise the breakouts 

Jeffrey: if we don't have good telecon facilities for the breakouts, could be better for plenaries?

Dan: Breakout A to always be in the conference room - of sessions 9 and 10, currently scheduled for Tuesday afternoon 14:00 CET and 15:25 CET.

### Breakout B (California / Australia) - [2025-02-25](https://www.timeanddate.com/worldclock/converter.html?iso=20250225T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Xiaocheng, Martin, Jeffrey

#### [CSS `shape()` function](https://github.com/w3ctag/design-reviews/issues/1033) - @martinthomson, @xiaochengh

Jeffrey: It looks like Martin's concerns are resolved. Xiaocheng, can you draft a closing comment?

Xiaocheng: Will do.

Jeffrey: And we can double-check in plenary.

#### [Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @jyasskin, @csarven, @martintomson

Martin: Based on the discussion with Mike, there are several corner cases that haven't been worked through. Some fundamental pieces that aren't clear. Would be best to defer until some of those are sorted out. E.g. What if you say you need a signature-based SRI and there's a redirect? A core attack is a bunch of resources are signed, and you substitute one resource for another. Implication is that you need to sign the identity of the resource. But when you do that, you engage the whole redirect problem.

Jeffrey: What about naming resources, where the name isn't equal to the path, but is signed?

Martin: That's the "nonce" approach. Need to resolve that too. It's tricky, but Mike has all the tools to work through it. We won't be helping as the TAG.

Jeffrey: I assume we're supportive of the direction?

Martin: Not excited, since it's narrowly applicable. But we've already solved the low-hanging fruit, so this is ok as long as it doesn't lead to major complexity problems downstream.

Martin to write a closing comment.

Posted: https://github.com/w3ctag/design-reviews/issues/1041#issuecomment-2683769144



#### Paris Agenda Planning

We assigned several topic areas to time slots.


### Breakout C (Europe / China) - [2025-02-26](https://www.timeanddate.com/worldclock/converter.html?iso=20250226T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Hadley, Tristan, Xiaocheng, Matthew, Martin, Dan, Yves, Lola, Max

#### [Normative Changes of the Input Events Level 2](https://github.com/w3ctag/design-reviews/issues/1019) - @matatk

Matthew: looks ok - no reason to keep it open.  We're looking at it still in APA.

Dan: would like to resolve satisfied.

Martin: these all look very reasonable. I'm satisfied if Matthew's satisfied.

**Matthew to leave closing comment and resolve as satisfied**

#### [CSS Inline `text-box`, `text-box-trim`, and `text-box-edge` properties](https://github.com/w3ctag/design-reviews/issues/1021) - @xiaochengh

Xiaocheng: about vertical alignment ... e.g. aligning something to a capital letter's basline of a passage of text... difficult to do... can only align to the containing box ... another case is veritcal align a line of text with something else... and identify the middle line of the line of text.. This proposal introducuces `text-box-trim` - most basic usage is trimming the letting above and below the text... then use this to vertical align with some other content. In general I'm pretty positive with this proposal... Very multi-stakehodler.  Solving an alignment problem ... might have interaction with borders, background, highlights... not sure if it's considered... 

Martin: [I have to say: I've wanted this for some time for my own use: aligning baselines of different boxes is super fiddly.] I think it's the right thing to do is to ask the question about alternatives considered... "I know this changes the size of the box. Have you considered the implications..."  Seems unlikely that they haven't considered this...  Because we don't have an explainer here... I think it's good to ask them to explore some of the alternatives.

Dan: should we ask for an explainer?

Xiaocheng: there is an explainer...  but we should ask them to put it in the CSS wg.

Martin: it's a good explainer... 

**Xiaocheng to draft some feedback in the issue asking for alternatives**

#### [CSS Scroll Buttons](https://github.com/w3ctag/design-reviews/issues/1054) - @xiaochengh

Xiaocheng: this is one of the carousel issues... Approach is like identifying the common design pattern... Really complicated to design as a whole.. so the approach is to identify common parts of the carousel pattern... 

[Lola: we agreed in breakout A to talk about this in a session.]

Matthew: There is a discussion in CSS that APA has been tracking... related to this. A bit unclear as the intent of the CSS wg here... Element would need to be focused.. which is different to how focus works now... different from a keyboard interaction perspective. 

Martin: ... pseudo-elements are focusable - doesn't imply they have to be focussed ...  ... would be good ... not clear from the explainer... "can be focused" - 

Xiaocheng: they are treating scrollers as special case of carousel...  Regarding other issues: for this they are defining a pseudo-element for interaction purposes... Can be focused ... Is that a good approach from an a11y perspective? 

Martin: don't we already use pseudo elements for various forms? e.g. inoput type=file?

Xiaocheng: with event listeners?

Martin: I think so.

**Matthew to draft a comment requesting further info... we can agree to leave it async or agree it at the plenary**

#### [CSS inert](https://github.com/w3ctag/design-reviews/issues/1055) - @xiaochengh

Xiaocheng: also part of carousel... CSS inert introduces a new property called interactivity - 2 values - auto and inert. The idea is to use a CSS property to mark an element as inert. You can sense it with CSS selectors instead of JS.  Context is ... having a bunch of items ... scrolling .. an item at the top and you want to make the other items "inert"...

Dan: e.g. greyed out?

Martin: say you have a scrollable region and some items are offscreen .. and therefore inert... say you use right arrow or tab to scroll to something and nothing happens because it's 'inert'... that seems like a failure mode... so I'm interested what they think is happening?  When we have a scrollable container in regular content, stuff that is offscreen (or not visible) doesn't become inert just because it is scrolled out, it's just not presently in view.

Xiaocheng: do we have any position on using CSS for non-styling... interactive property has nothing to do with styling ... quite an exception in the CSS area... Other exceptions are user select which controls whether part of the region is selectable or not.. and ... Also proposals of introducing these type of properties that got rejected .. e.g. `user-modify`...  it was rejected in 2015 or 2016 .. reason is it's about JS and HTML rather than styling...

Matthew: I think Martin has nailed it with that use case... About interactivity question... is it too unrelated to styling .. I wonder if pointer events would be seen as a precedent?  Probably is worth having that discussion... 

Dan: CSS is more than styling ... as far as the developer community is concerned...

Martin: e.g. [pseudo-elements with 'content' is an example of more than styling
background images, not just styling]

Xiaocheng: the recommended usage of these things is for presentation purposes... 

Martin: i don't know that it's an abuse in this case... but it could be problematic in this case with the focus.. The user-select property .. also crosses the line between presentation and content... 

Xiaocheng: both user-select and user-modify have crossed the line... One got accepted and the other rejected

Dan: do we need a design review issue? though they aren't always welcome on CSS. To discuss at f2f? Do we have feedback to share here?

Martin: it's not clear what model they're operate under. They've pointed at accessibility guidelines, but they may not apply... But let's ask 

**Martin to leave comment**

Dan: And let's put the design review question on the agenda for the f2f

#### [WebRTC API Proposed Amendments](https://github.com/w3ctag/design-reviews/issues/1026) - @matatk, @lolaodelola

Lola: we agreed it's probably fine .. waiting for Matthew .. to do an a11y review ...  To catch folks up .. these changes are minor for WebRTC ... brings spec into alignment with RFC... some already implemented in browsers...  

Matthew: our [APA]'s RTC experts have looked at it and I think are ok with it, but I will check before the plenary ... there may have been a trade-off with privacy? I'll confirm

**re-address at plenary**

#### Paris Agenda Planning

### Plenary Session - [2025-02-27](https://www.timeanddate.com/worldclock/converter.html?iso=20250227T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Jeffrey, Hadley, Matthew, Dan, Christian, Sarven

Regrets: Xiaocheng, Martin

#### Chairing

We have consensus that Hadley Beeman, Dan Appelquist, and Jeffrey Yasskin should chair the tag for the current term (or [until chair selection needs to be re-run](https://www.w3.org/policies/process/#tag-participation)). The decision was not unanimous, and we're working on https://github.com/w3ctag/process/pull/39 to improve some of the concerns that came up.

##### Summary 

It looks like consensus has been reached, based on the W3C's definition of consensus: "A substantial number of individuals in the set support the decision and there is no sustained objection from anybody in the set."

- Jeffrey posted the initial proposal, which came out of our plenary call last week.
- Initially, Martin raised an objection, proposing an alternative (Hadley + Jeffrey as co-chairs and Dan as "Secretary").
- Dan expressed willingness to do less chairing over-all, but was not willing to take on the proposed "Secretary" role.
- Jeffrey clarified and reiterated the proposal: Dan, Hadley, and Jeffrey as co-chairs with Dan stepping to do less chairing over-all, with an alternative that we ask the Team to decide. He asked the TAG to feed back by EOD Tuesday.
- The only comment on the thread before the deadline was from Sarven, who said it would be better to reach consensus than take this to the Team.
- Martin, despite his concerns, explicitly stated he would "stand aside" if the group preferred the DHJ co-chair arrangement.
- No one else in the group put forward an alternative slate of chairs.
- Sarven confirmed support for DHJ as co-chairs, clarifying that his earlier comment was not an objection.

Since there is no longer a sustained objection, and the proposed co-chair slate (Dan, Hadley, Jeffrey) has broad support, consensus has been reached on that arrangement.

#### Associates at the f2f

Jeffrey: We said we would have a telecon set up most of the time - and Associates are welcome to attend any sessions they want to remotely.  We have one room that can do remote breakouts.

Hadley: we're trying to figure it out as we go...

#### Breakout Rollup

**CSS Scroll Buttons**

We agree Matthew's comment and he posts it.

**WebRTC proposed amendments**

Matthew: we're fine in APA...  a11y strange interaction between a11y and privacy... might require some TAG input...

Dan: Should we keep it open then?

Matthew: APA will be talking to this group... picking up the thread.  Might have been already resolved...

Jeffrey: If there is a targetted question of a11y vs privacy then it should be its own issue...

*we agree to close with satisfied*

*Matthew to leave closing comment*

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
#### Paris Agenda Planning

Matthew: things shipping that have only gone through the CG process... I'll add it to the spreadsheet.

Jeffrey: yes absolutely add it...  Does it fit in the 3rd item in section 6?

Matthew: I think it's important... 

Hadley: is it architectural? or is it AB and process? 

Matthew: if we have consensus that it's an issue then that gives me a mandate to talk to other groups etc...

Jeffrey: we've talked about the TAG identifying new work for W3C... e.g. anti-fraud stuff... Chromium has a requirement that things be adopted by a working group. No easy on-ramp process to do that... TAG could be involved.

Hadley: Put it in section 11 along with Explainer Explainer?

Matthew: works for me... 

##### Preparatory work

* Expectation-sharing: come with some ideas for the culture you want to establish on the TAG. Things you want to do, things you want the rest of us to do, and things you want the chairs to do.
* Claim a "major topic", and write a 10-minute presentation to introduce us to it.
* ???

* reviewing [code of conduct](https://www.w3.org/policies/code-of-conduct/)
* scribes - we should have scribe assignments
* assign session leaders

#### PROPOSED TOPIC: Change status of Societal Impact Questionnaire to DNOTE

Sarven: PR https://github.com/w3ctag/societal-impact-questionnaire/pull/16 resolving issue (mentions why): https://github.com/w3ctag/societal-impact-questionnaire/issues/15

Sarven: brings in line with Security & Privacy questionnaire... this sort of doc as an ongoing doc that improves over time .. should be a note rather than a finding which I think would be more appropriate to what this document is intended to be - evolving and not so fixed. And Note track would potentially set it up for a Statement down the line?

Yves: note track is the lightest of all tracks on TR... When we want to elevate to a statement, gets more tricky...
