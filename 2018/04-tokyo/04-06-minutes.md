## TAG Face to Face
##### 06 April 2018

Present: Dan, Travis, Hadley (remote), Alex, David, Peter, Sangwhan, Yves
Invited Guests: Andrew-sama, Mike Smith (tm), Wendy Seltzer (morning)

Regrets: Łukasz, Kenneth

Scribe: Andrew-sama (AM), Alex (PM)

---

Agenda:

* Security and Privacy self-review

---

[ Special guest for a few topics: Wendy Seltzer ]

### Security and Privacy self-review

[Andrew starts scribing rather late]
  
Issues: https://github.com/w3ctag/security-questionnaire/issues

Dan: No-one is actively maintaingin this, since 2016.  Bunch of issues.  Is IG interested?

Dan: We took resolution in London that we (TAG) are taking ownership

WS: I'd like to co-ordinate better.  Different repos.  Things have been done, in variety of places

Dan: People are using this document, so we need to assign someone who can do that work
... Hadley, wdyt?

Hadley: I care about it.  Feedback needs to be taken on board somewhere.

Dan: I'll reach out to the [PInG](http://www.w3.org/Privacy/) chair.  AC seems to want us to do more privacy things since they elected Lukasz.  WS, any other feedback we should take on board?\

WS: PInG generated a longer list of questions on privacy.  Most people thought it was too detailed for a general purpose doc.

### IETF update

WS: I attended London at the end of the week.  Web packaging was the main thing where TAG feedback was solicited.

Dan: We're on it.  Let's use Strint (?) as a model for how a workshop could be successful.  Anything else?

WS: Web auth is in CR.  Exciting.  What else can be build with web auth n.  Workshop idea.

Dan: We don't have a review for web auth

Travis: recently closed?

Dan: no.  Is it appropriate for us to do a review?

WS: Yes if you haven't done one

Dan: we had an issue related to FIDO, but we should be doing a review in the spirit of the other reviews we're doing.  Could the chairs submit a review request?

> we discover there was in fact a review: https://github.com/w3ctag/security-questionnaire/issues

Dan: ok, there's one issue open from that older review, but we closed the review.  Can TAG be useful in any other way?

WS: This one has a lot of eyes on, reviewing stuff.  You could poke more at the privacy questions, but that's also gotten review.

WS: curious about ads.txt

Dan: us too

Alex: we don't have any updates just yet.  I've had convos with the person most responsible at Google. There has been a learning process happening about manny areas of the problem space.  They're learning about specs.  We're learning about their requirmenets.  Assertions about 3rd parties that can be enabled/disabled can be delivered over insecure HTTP, so it doesn't seem to be reasonable to trust them.  We're going to be waiting for ads platforms to stop accepting plain HTTP before we can make substantial progress.

... They meet in an ad hoc way.  Hopefully sometime in the summer.  Hopefully google will stop accepting ads.txt insecurely.  Ads industry is trailing us (browsers) on TLS adoption.

WS: We've been working to bring together a group (Improving web advertising business group) to talk about advertising.  Very slowly gathering momentum. Group: https://www.w3.org/community/web-adv/

Dan: any overlap with ads.txt?

WS: not to my knowledge.

### QUIC

Hadley: there's a debate going on around spin bits.  Net neutrality implications.

WS: people are looking at the anti-middlebox-mucking-with-the-traffic issue.  There's a general sense of where the whole group is going.

### "Strategy funnel"

WS: Sync between what the TAG is looking at and what we are investigating as potential areas of new work.

Hadley: geolocation?

WS: folded into devices and sensors

WS: There's a perpetually upcoming workshop on permissions and consent.  Browsers are making different choices in UI.  We could give guidance: 'it's not safe for a user to expose this information with explicit permission' etc.

Hadley: 'perpetually upcoming'?

WS: we're trying to make it happen this fall

Travis: how do you fill your [strategy funnel](https://github.com/w3c/strategy/projects/2)?

WS: public issues list (https://github.com/w3c/strategy/issues/).  Some things are very hypothetical, doesn't mean we're about to take it on.  eg. MathML, packaging.

Dan: anything else?

WS: secure contexts discussion?

Travis: where do you stand on it?

David: we made some progress but we recognised that we could not give decisive advice.  I merged Alex's suggestions with mine.

Yves: Specifically for webrtc, I spoke to Dom about it, they are pushing it in the WG.

Dan: Hopefully we'll have some consensus text in the design principles doc soon.

> Wendy exits

### HTML

Mike: HTML spec is incredibly broad and deep, mostly to the detriment of developers, but there are parts that are marked for use of developers.  These explain things in terms of what devs need to know rather than how to implement it in the browser.  The dev stuff falls short of what it could be if we wanted to make things clearer for developers, this would be useful and actionable.

... If there are sections with IDL that do not have a corresponding DOM intro, that we need to fix.  In reality the main audience for the DOM intro stuff is MDN, etc, people writing their own resources for developers.

Alex: HTML is now a maintenance project.  With new things, we want explainers.  There were features in HTML5 that have been removed, which had 'thin' rationales.  But I'm interested in knowing how these things are connected to one another.  Forms; microdata.

Mike: Mozilla pulled their impl of microdata API

Alex: Would it be valuable for us to identify how features are used together

Mike: yes

### Offscreen Canvas (141)

Alex: we had questions about raf.

> Moved to extra time

### Accessibility object model (134)

We're going to try and arrange time with Alice.

### WithCredentials (76)

Alex: We asked the WG at TPAC to come up with a means of allowing content to be loaded.  `*` does not really mean `*`.  Hard to know if you will be allowed to load things in different situations.

Yves: It needs to represent as something that's different to a network error.

Alex: Might enable port scanning

Yves: Want to avoid URL + context for fetch.  Abstracting retry into libraries.  I prefer public-deauth.

Travis: either automatic retry or a differentiated error?

Alex: Or both

Dan: any reason to have a breakout on this?

Yves: tag Mike west and brad hill?

Travis: are there tests?

Mike: Yes, the coverage could be better

### Task scheduling (72)

Alex: breakout pls.

Travis: I heard from some Edge folks that they plan to align with Chrome (re requestAnimationFrame timing).  David and I rooted out some issues like whether RAF should be before or after layout.

### Keyboard map (238) and gamepad API

Alex: this is the ability to understand the physical layout of the keyboard

David: Abstract says it's keys and codes

Yves: gamepad?

Travis: There's a gamepad spec

Alex: hard to know when people remap keys or use different keyboards.

David: Primary use case is giving users instructions about what keys to press (need to know whether they have that key and where it is).

Travis: Allows discovery of physical key codes and letter codes before user pushes the button.

Sangwhan: Gamepad API is not good

> Extra time, review in conjunction with Gamepad API

### Design Principles open issues

Dan: we have 40 open issues. Do we have an extra-time label on these? Plan is to spend 10 minutes triaging.

https://github.com/w3ctag/design-principles/issues

Dan: I'm going to start from the bottom

Dan: developer considerations. Both marked big and small? Issue #2

Dan: my view is that this issue is too broad. We should close and re-open sub-issues as we find them.

Travis: agree.

https://github.com/w3ctag/design-principles/issues/3

Dan/Travis: <discuss what to put in the doc>
  
Dan: should we create a label that something needs to be written and then assign it?

(discussion about work mode; some discussion of adding these issues to our weekly calls)

"write me!"

https://github.com/w3ctag/design-principles/issues/9

Closing.

https://github.com/w3ctag/design-principles/issues/10

Travis: Closing 10, will keep #72 instead.

Dan: David, could you write text for this?

David: yes (sigh).

https://github.com/w3ctag/design-principles/issues/11

Dan: this was worked on in July '17

Travis: we agree, ready to write

https://github.com/w3ctag/design-principles/issues/16

(discussion of how Map-like and Set-like objects force exoticness)

See, e.g.: https://cs.chromium.org/chromium/src/third_party/WebKit/Source/core/css/FontFaceSet.idl?q=fontfaceset&sq=package:chromium&dr=C&l=31

Also: https://github.com/heycam/webidl/issues/100

Alex: it seems like we're struggling with Map-like/Set-like/Array-like objects. IDL doesn't have an easy way to get this right today

Travis: will write something and we can discuss

https://github.com/w3ctag/design-principles/issues/18

(wide agreement; Travis to send a PR)

https://github.com/w3ctag/design-principles/issues/21

(commented and closed)

https://github.com/w3ctag/design-principles/issues/35

(Alex commented; to write text for this)

https://github.com/w3ctag/design-principles/issues/38

(Travis to write it up)

https://github.com/w3ctag/design-principles/issues/39

(Sanghwan to write up a PR before the end of this meeting)

https://github.com/w3ctag/design-principles/issues/40

(already addressed; David to close)

https://github.com/w3ctag/design-principles/issues/41

(Travis to write it up per previous conversations)

https://github.com/w3ctag/design-principles/issues/44

(Alex to draft a PR)

https://github.com/w3ctag/design-principles/issues/46

(David to draft a PR)

https://github.com/w3ctag/design-principles/issues/48

(Travis to draft a PR)

https://github.com/w3ctag/design-principles/issues/50

(not touching, David may revisit)

https://github.com/w3ctag/design-principles/issues/51

(Travis to gank from Domenic)

https://github.com/w3ctag/design-principles/pull/80

(Alex to revise)

## Death row

Going through the requests in [Chaals's email](https://lists.w3.org/Archives/Public/www-tag/2017Apr/0010.html).

David: The process now has a superseded status, and the initial request mail is before this status was in place, so some of them should be superseded, not obsoleted.

Dan: Well noted.

### ATAG 1.0

https://www.w3.org/TR/2000/REC-ATAG10-20000203/

> General consensus seems to be happy to obsolete.

Alex: Some of this might be owned by another group.

> Investigation on working group ownership proves otherwise, consensus to supersede.

David: Should we try to loop in some of the people involved in the specs originally?

**Resolution: Superseded - ATAG 2.0.**

### CC/PP

https://www.w3.org/Mobile/CCPP/
https://www.w3.org/TR/CCPP-struct-vocab/

Sangwhan: No working group owns this.

Alex: Seems quite old - mentions Symbian.. Are there implementations?

> Checks, found one: http://delicon.sourceforge.net

Dan: Doesn't matter, we are here to check if this is technically useful to the web platform.

**Resolution: Obsoletion.**

### MathML 1 and 2

Sangwhan: There is MathML 3, seems like no working group on this anymore.

> Group looks into status

**Resolution: Superseded - MathML 3.**

### PICS and Friends

https://www.w3.org/PICS/

Dan: This should be obsoleted.

Alex: What is this for?

Yves: It is for ratings.

> Looking at the background, and checking if any working group owns this

**Resolution: Obsoletion.**

### POWDER

Yves: Safe to obsolete, I believe.

> Looks into background

**Consensus: Obsoletion.**

### P3P

David: There's already an obsoletion vote for P3P.

**Resolution: Do nothing.**

### WebCGM

https://www.w3.org/Graphics/WebCGM/

Alex: We looked into this a while ago. Don't think it's common.

Yves: It's a web profile of an ISO standard.

Sangwhan: I don't see browser implementations at least, Illustrator seems to support it though.

> Checks background, seems to be save to supersede with WebCGM 2.1 and ideally SVG

**Consensus: Superseded - [WebCGM 2.1](https://www.w3.org/TR/2010/REC-webcgm21-20100301/) or SVG.**

...

**RESOLUTION**: Recommend to the team to supercede ATAG 1.0, MathML 1, MathML 2, WebCGM 1.0, and WebCGM 2.0, and to obsolete CC/PP, PICS, PICS Rules, PICS Rating systems, PICS Label distribution, and POWDER.

## Design review breakouts

Breakout group 1:
*  David
*  Peter
*  Alex
*  Travis
*  Andrew
*  Issues: 235 233 231 224 222 217 213 206 188 141 72
  
Breakout group 2:
*  Hadley
*  Sangwhan
*  Yves
*  Dan
*  Lukasz
*  Issues: 238 237 232 229 225 203

Dan: Try to do something now, all together?
Andrew: Issue 224.

### CSS Layout API (#224)

(discussing Travis' feedback: https://github.com/w3ctag/design-reviews/issues/224#issuecomment-378824908)

Travis: should this be Border Box?

David: it's a tradeoff based on how often you have to type it

Travis: I'm hearing "not worth mentioning"?

David: I wouldn't want it to be that verbose

Travis: is everything border-box based anyway?

Alex/David: not really.

Alex: you can flip the general thing based on the `box-sizing` property

Peter: you should probably be setting `box-sizing`

David: at this API level, you always want to deal with a specific thing. If you're writing layout code, you want to produce box sizes that are a consisntent thing

David: it's also the offsets. If anything, I'd name the fragment as `LayoutBorderBoxFragment` or something like that, but it won't show up in the code, so I don't know that it matters

Travis: example 1: so we're talking about layout fragments and example 1 introduces almost every concept right away...hard to digest.

Peter: layout's hard, yo

Travis: was hopign it could be moved later after other concepts are introduced

(discussion of examples in Explainer vs. in Spec)

Travis: in general, `yeild` can return whatever it wants...is there any validation? Does it throw?

David: is it also sensible syntax? (the return statement)

Travis: yes, that's legit. It's object destructuring.

(discussion of destructuring)

David: this example could use some code comments

Alex: another way to think about that destructuring thing is that maybe it's insufficiently typed? For instance at the end of the example, you hand back an untyped object...what is that thing?

Travis: it's a dict defined later

Alex: ok, but what the heck? How would you debug that?

Travis: that was my next comment: it's unclear what these types are. And you yeild something different than what you return.

David: some code-comments would maybe be helpful here

Travis: regarding `create a layout fragment`, there's a structured deserialize which can fail...what happens if it does?

Alex: what's the general error handling model? if you throw in your worklet, do you keep getting called for the next layout? I'd assume so

Travis: don't know. not sure that's outlined

Alex: does a worklet get onerror? Unclear from our code.

Travis: `IntrinsicSizes`: I was curious about the expected lifecycle. Does the worklet global scope reused? If you cache one of these, and you read it at different times, do you get different values?

Alex: I don't think they're destructed per layout/frame, but they *can* be.

Travis: need more details on the expected errors

Travis: in all code samples, there's a call to `layoutNextFragment` which takes `LayoutConstraints`, but examples don't construct them

Alex: are there big open questions with the model?

Travis: should they continue down the generator path? or move to a promise-based API. Having spent time with the generator approach, the promise verison sounds attractive but I don't know what that would look like

Alex: that sounds like somethign that should be in considered alternatives in their Explainer, right?

Travis: it also wasn't clear to me how request objects get processed.

David: it seems like the array gets turned into a set of sizes once you've yeilded

Travis: if you call it and get the requests back but never yeild them, what happens?

(discussion of how to find out)

Travis: that is all outlined in Section 5, at the end. I'd sort of like the explanation of how the overall model works to move earlier in the spec.

(discussion of iterators and what it means to `tick` the generator)

David: if this is your first intro to generators, it's going to teach you weird things about them

Alex: is it weird that you're defining an API where you get different value types through the iteration phases?

Travis: entries(), values() get you consistent types, e.g.

Travis: the "intrinsicSizes" name is used multiple times, but when you call layout on your children, you use a different name. Should it be "layout" in all cases? You're going ot be layed out and then you're going ot lay out your children.

David: intrinsic sizing and layout deal on fragments very differently. Intrinsic sizing deals with them all at once, but layout does one at a time and may create more fragments.

(david explains layout and why it's hard, yo)

Travis: I see...so there's no shortcut

David: there's no single right answer.

David: it isn't clear to me how you get all the fragments...if a child fragments itself in response to it's layout call, how is the parent informed of that? Maybe the break tokens handle this...or maybe the examples just assume that doesn't happen.

Travis: the code you were asking about, David, is in the [`run a generator` algorithm](https://drafts.css-houdini.org/css-layout-api/#run-a-generator). It handles pumping the generator.

David: seems like this should break at step 6?

Travis: yeah, where do you check `done` here?

Alex: why doesn't this link to the Explainer? *sigh*

Alex: are there other big issues? I'm as (or more) interested at the Explainer at this point given that there aren't impls

Travis: there are a lot of nits and some issues with how ti feels, and I don't know if it's going ot work, but it feels like it could.

Alex: I don't see anything about considered alternatives in the Explainer...that feels like a mistake

Travis: I wasn't looking at the Explainer...should have looked at that first!

Travis: I'm going to file a few issues

David: would like to look at this from a CSS perspective to see if it fits with how engines do layout

Travis: takign a step back; this is really impressive. What it will enable is awesome and it'll be really cool

Travis: there was some reporting of size properties...was wondering if they should be aligned with the TypeOM? E.g., the `LayoutEdgeSizes` object: https://drafts.css-houdini.org/css-layout-api/#edges

Peter: the CSS OM is more about CSS values rather than pixels

Travis: so is the typed OM about being able to convert?

Peter: it's more about represnting CSS as objects isntead of strings

Travis: as opposed to innerWidth/etc.

Alex: those handed you pixels and to get that you had to run layoutto ge



Open issues:
* Review of signature-based resource loading restrictions. @cynthia @hadleybeeman @plinss
* Review OffscreenCanvas, including ImageBitmapRenderingContext @cynthia @dbaron @travisleithead
* Review Accessibility Object Model @cynthia @travisleithead (if alice responds)
* "With Credentials" flag possibly inconsistent with web architecture @dbaron
* Task Scheduling	




