## TAG Teleconference
##### 12-14 October 2020

---

### Agenda:

#### Breakout A (Europe / US)

* [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482) - @hober, @dbaron, @torgo, @kenchris
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo
* [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538) - @hober, @hadleybeeman, @atanassov

#### Breakout B (US / APAC)

* [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss
* [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511) - @alice, @kenchris, @atanassov
* [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

#### Breakout C (APAC / Europe)

* [WebRTC-SVC (Scalable Video Coding)](https://github.com/w3ctag/design-reviews/issues/396) - @cynthia, @kenchris
* [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

#### Plenary Session

* Planning for joint meeting:

  * [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov
  * [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561)


* Breakout Rollup
* Issue Triage


-----


### Breakout A

Present: Tess, Dan, Peter, Rossen, Yves

Regrets: Kenneth


#### [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482) - @hober, @dbaron, @torgo, @kenchris

Peter: marked as pending feedback and looks like we [got some](https://github.com/w3ctag/design-reviews/issues/482#issuecomment-698009331)...

Tess: ... kind of "the entire thing" - I'll reply.

Peter: going to waiting for feedback?

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

Peter: Chris did respond to our concerns - should we invite him to a meting...?

Rossen: I think we should discuss in a plenary session.  Are there any changes on either side we can or should do? 

Hadley: feels like there's a differene between when you would ideally do a TAG review vs when you would be in trouble if you haven't done one?

Rossen: also - chromium and w3c and TAG - how do the processes intersect?  

Dan: So let's get him to a plenary session - maybe after TPAC week? Like 1st week of November?

Peter: maybe the 11th of November?

Peter: I will reach out to Chris about the 11th.

#### [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538) - @hober, @hadleybeeman, @atanassov

Rossen: main question - does the TAG have an opinion on present day disparity between browsers... moreso than the actual proposal.... I don't think we've discussed that particular part....

Dan: having disparity between browsers is bad.

Rossen: yes especially when it comes to privacy. Expectations from users ...

Rossen: current handling in Safari and Firefox... 

Hadley: they've broken it down by browser in [their issue 13](https://github.com/privacycg/proposals/issues/13). ... what they are toying with doing is standardizing removing the referrer in an HTTP call?  In certain contexts - like crossing origins. If that's correct than 1st thought is it's an IETF spec. I think they're right that this would impact the ad ecosystem.

... feels like to me the first thing, looking at their issue 13 - privacy cg 

... personally I understand and agree with their concern that referers leak browser activity - but it would be helpful to lay out use cases... Where people are using it now.  Feels like we should ask them for the use cases...  Without the use cases this feels like the kind of thing that could be well intentioned but could screw up usefu stuff.

Rossen: An ask from the edge engineering team to chime in - we experimented in the dev channel - [comment from April 30th](https://github.com/privacycg/proposals/issues/13#issuecomment-622029248).

Rossen: ripple effect - in making such changes often difficult to detect. Tips the balance between privacy & functionality?

Dan: are the perceived losses in functionality from an end user persctive or from a publisher or advertiser perspective?  

Rossen: not being able to process a payment - is a pretty fundamental thing.  I don't know how much of the tail end of the web this effects.  1st example is the one that gives me the most heartburn.  How much in the tail end will break because of something like this?  Will impact users, publishers and advertisers.

Hadley: I'm not necessarily against breaking things.  But... in /TR space we have normative references - in CSP 2 ... CSP violation reports...

Rossen: HTML refers to it a lot - document.referrer. 

Dan: one thing thay comes to mind - Brave docunmented their more restrictive approach [here](https://github.com/privacycg/proposals/issues/13#issuecomment-654404602) - but it's not clear to me that their approach is the same as what you're talking about, Rossen – would the.... Is there any consensus about what change in policy would be positive privacy but not break stuff....?

Hadley: I think what we have at the top of our issue - "At the very least it seems like we can align on defaulting to strict-origin-when-cross-origin"... But "But even this default can still be overwritten by motivated adversaries. This leads to the question of why only change the default, and not permanently trim cross-site referrers with no way to override?" which they go on to say that Brave has done and not encountered web compat issues.

... they go on to say - chrome is planning on shipping. as there is cross-browser consensus on chaning default referer policy. If that's the case.

Dan: we could say "That sounds good to us . we think more strictions (permanently trim cross-site referrers) would be good as well. More work needs to be done to explore where this would potentially break existing content - especially in the long tail."

Hadley: seems ok - ...


### Breakout B

Present: -  didn't happen - 

Regrets: Sangwhan, Tess, Rossen, David







### Breakout C

Present: Kenneth, Dan, Alice, Yves, Hadley, Sangwhan

Regrets: 

#### [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

Ken: streaming not happening is basically the take-away. 

Alice: strong pushback by [webkit on streaming support](https://github.com/w3ctag/design-reviews/issues/494#issuecomment-698646259)...

[reviewing whatwg issue](https://github.com/whatwg/dom/issues/831#issuecomment-650107249)

Alice: I think what is saying you can't ... [suggestion is] you either do streaming now or not at all.  

Ken: process of insterting nodes is observable... revelaing the state of streaming.

Alice: that's him arguing it can't be optional.  Because you can observe tghe timing of nodes beint attatched.

... then Mason says consensus to add later.  then Ryosuke says no you can't...

Dan: do we need to adjuicate this dispute?

Alice: it looks like they are waiting for an update from Ryosuke.  

... it seems like - i could comment saying "i read the linked issue.. it seems it's not clear to me that webkit is pushing back on streaming so much as implementation optional streaming support... " but I see why they have made the decision to punt it. So maybe we don't get streaming.  Maybe that's OK. I'll make a comment.

Alice: I'll proposed close saying the main feedback we are having ...

#### [WebRTC-SVC (Scalable Video Coding)](https://github.com/w3ctag/design-reviews/issues/396) - @cynthia, @kenchris

Ken: no big update...  I think we should close it.

Sangwhan: yeah. I don't like how they did the enums in a table through a dom string but...  

Yves: it's a design detail - so seems good to me.

[closed]

#### [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

Ken: they want to have a discussion at TPAC.

Dan: What venue?

Sanghwan: "Web apps editing" - 

Dan: Should we wait or be a part of it?

Ken: let's let them come to conclusion.

Dan: Ok let's bump this issue until after TPAC.


#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

Dan: Still waiting on an explainer update.

[bumped]

#### [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511) - @alice, @kenchris, @atanassov

Alice: Skimmed the combined explainer.... Looking at responses.

Alice: a new privacy & security section

Ken: [lists some fixes]

Alice: the idea is so you can't do a brute force attack

Ken: also prevent building out a string of what the user is searching for

Alice: that makes sense.  Also got my head around -- one of the alternatives when you get a match is to show it. I understood why they don't want that. once it's showing you don't know when to hdie it again...  So putting the developer in charge of when it closes but because it's a CSS property it becomes ambiguous . So in order to not have to answer questions - you have it closed when the property applies and have the developer manually open it.

... so when I suggested a pseudo-selector. They mentioned as a use case wanting to highlight the search string. ... you can only get the berforematch event on hidden matcheable content. And you have to remove hiddenmatcable... 

... but - say I'm typing lorem ipsum and I've typed "lore" and it's matched.. 

Ken: we don't want the web site where content is moving forward and back... so a grace period.

Alice: that's my one remaining question - fairly straightforward. Any other web spec that works like that where CSS gives you access to a DOM feature?

Ken: painting and layout?  We have `contains` and with the Houdini APIs some of the other CSS properties will be exposed... resize observer and it won't resize because it's not doing layout...

Alice: those are my 2 main thoughts - can they be more percise about the 2nd security mitigation; other one is having the event only fire on content in the DOM tree of a hiddenmatchable element <- seems like a good security measure but not sure if there is a precedent between events and CSS properties.

Alice: maybe coming to us earlier would have been better.

[ken leaves a comment](https://github.com/w3ctag/design-reviews/issues/511#issuecomment-707593876)

[alice will leave a comment]

[bumped]

### Plenary Session

Present: Kenneth, Peter, Tess, Dan, Yves

Regrets: Alice, Hadley

#### Roll-ups from Breakouts

Tess: (breakout A) URL Protocol Handler Reg for PWAs... We got some feedback. I replied. Then we talked about the blink shipping process. Chris wilson to meet with us on the 11th of Nob. Then we talked about referrer handling request.  Dan commented.  A lot of different moving parts.

Peter: B basically didn't happen.

Dan: C - declarative shadow dom - 

Ken: left comment - we understood how it's working - streaming is not happening and we're kind of fine with it. Things become observable.  

Dan: We closed webrtc SVC - 

Kan: sangwhan wanted an enum instead of a string.. 

Dan: but we could live with it...

Dan: VirtualKeyboard API - show/hide policy

Ken: people are scheduling a talk at TPAC

Dan: beforematch event - 

Ken: they talk more about mitigations in the explainer - I filed a comment.  They fixed some issues.  Maybe a grace period to deal with the "fast typing" scenario - we gave feedback.

#### Triage

5 untriaged issues

[Storage Buckets API Progress: untriaged Review type: early review](https://github.com/w3ctag/design-reviews/issues/562)
#562 opened 7 days ago by ayuishii 1 of 1
 
Ken & Tess

[APA Pronunciation Explainer Progress: untriaged Review type: early review](https://github.com/w3ctag/design-reviews/issues/561)
#561 opened 8 days ago by alice   2020-10-12-week

Hadley & Tess

[WebRTC Priority Control API Progress: untriaged](https://github.com/w3ctag/design-reviews/issues/560)
#560 opened 20 days ago by caribouW3 1 of 1
 
Sanghwan & David
 
[Review for CSS property "aspect-ratio" Progress: untriaged])(https://github.com/w3ctag/design-reviews/issues/559)
#559 opened 22 days ago by cbiesinger 1 of 1
 
Tess: [raises hand]

Dan: yes
 
[CAPTCHAs are horrible Progress: untriaged Review type: early review](https://github.com/w3ctag/design-reviews/issues/558)
#558 opened 25 days ago by plinss

Dan: others are working on it? Trust tokens?

Peter: reasonable but lacks form support...

Dan: maybe we need to engage some other peoplein the discussion?

Peter: maybe not the right venue?  I could start something on WICG...  

Dan: Maybe loop a few people in on the issue.  Propose a TPAC breakout if there's still time?


#### Going through no-milestone issues

**HTML Event Loop**

Tess : a big spreadsheet has been produced and that's where it stands... 

Peter: assigning to a future milestone

**[CSS Page orientation](https://github.com/w3ctag/design-reviews/issues/515)**

Peter: proposed coding but didn't close it.

[consensus to close]

Peter: 55 open issues from f2f



#### TPAC 

Peter: joint meetings - 2 meetings planned with APA - both in TAG calendar.  1st is tomorrow 7am pacific - personalization task force - 2nd friday at 8am pacific for pronounciation.  Alice not able to join either.    DIDs Nov 3 - it's in the calendar.

#### TC39 - wondering how TC39 could engage more with the TAG - @alice

They have meetings every 2 months - would it make sense for TAG to get a summary - JavaScript features that may impact the web?  [e.g. shared multi-threading] [agenda](https://github.com/tc39/agendas/blob/master/2020/09.md)

Dan: I think it would be useful.

Peter: in the  past we had TAG members on TC39 - should we have a standing invite to someone to come chat to us (at a plenary).

Dan: yes but low stress 

Peter: more of an informal chat vs a presentation

Dan: yes 

Peter: also someone to ask questions to

Ken: yeah I know people there as well.

#### Next f2f

Peter: tentative dates for November 30th...
