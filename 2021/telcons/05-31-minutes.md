# TAG meetings week-of 31 May 2021 

## Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/05-31-agenda.md).

### Breakout A (Europe / US) - [2021-05-31](https://www.timeanddate.com/worldclock/converter.html?iso=20210531T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @torgo
* [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529) - @hober, @torgo, @hadleybeeman, @plinss
* [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris
* [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov
* [Partitioning Storage, Service Workers, and Communication APIs](https://github.com/w3ctag/design-reviews/issues/629) - @hober, @rhiaro, @ylafon
* [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov
* [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro

### Breakout B (US / APAC) - [2021-06-01](https://www.timeanddate.com/worldclock/converter.html?iso=20210601T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov
* [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov
* [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2021-06-01](https://www.timeanddate.com/worldclock/converter.html?iso=20210601T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo
* [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris
* [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo
* [API for display-capturing the current tab](https://github.com/w3ctag/design-reviews/issues/625) - @cynthia, @LeaVerou
* [Shared Element Transitions - Early Review](https://github.com/w3ctag/design-reviews/issues/631) - @cynthia, @LeaVerou, @plinss

### Plenary Session - [2021-06-02](https://www.timeanddate.com/worldclock/converter.html?iso=20210602T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Status check on [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [WebID workshop](https://docs.google.com/document/d/1nZt-bU-9FeoaavSuB6KPC7d3vyKuOhnA5QAd8kTN0z0/edit) updates?

* Breakout Rollup
* Issue Triage

## Minutes

### Breakout A (Europe / US) 

Present: Dan, Yves, Rossen, Amy, Hadley, Tess

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @torgo

Dan: came back to us with a bunch of stuff they have done, responses to Alice's comments. A number of closed PRs referenced.

Tess: would like to look at the PRs to see if they adequately address things we brought up before

Dan: [proposed close] something something the abyss looking into you

#### [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529) - @hober, @torgo, @hadleybeeman, @plinss

Hadley: still waiting...  We've been concerned about the privacy implications and  that the p&s section was written from PoV of developers... it could help to put some stuff in for implementers - periodic permission prompts, visual indicators, etc... 

Dan: not really engaged with P&S self checked, just linked off to their considerations section

Hadley: they didn't have an explainer, but updated the readme

Dan: this is from so long ago...

Hadley: can put in a comment suggesting clarifying our advice was for geolocation not permissions

Dan: gaguing the response, maybe thinks this is more a generalised permissions issue... what do we think? Visual indication thing is not.

Hadley: yeah

Dan: because geo is the kind of api that is used.. I dunno.. because other types of apis used in the backround include ambient light sensor, camera, audio, geo can be used in the background. How can we focus our time? we've been back and forth. If there's nothing further to say should we close it?

Hadley: agree although ... we haven't put issues in their repo. Issue marcos is linking to on permissions api references issue 69 in geo which says explicitly limit permission lifetimes. So they're already talking about it.

Dan: we've left the feedback.. I don't know if we should keep it open?

Hadley: [leaves feedback, propose closed]

> Thanks, @marcoscaceres. To clarify: we were thinking more about advice to implementers of geolocation, rather than making changes to the Permissions API. Repeated prompts and UI indicators should be in the suite of options that browsers can use to empower/inform their users.
> 
> Beyond that though, we don't think we have much more to add. We're glad to see the progression this effort has taken, given the years in its development and our privacy concerns on earlier iterations. We are proposing to close this issue, but let us know if we can help with anything else.

Dan: I remember original geo api, there were objections on privacy grounds from center for democracy and technology i think? there was a big fight over this. Some of those concerns were well placed. This was before https. Got into platform without requirement for secure contexts. Good to see they're tidying it up.  I think that's what this is about, we should be supportive. But still this permissions api thing which isn't uniformly adopted.

#### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

Tess: wasn't clear to me that Dominic's concerns were being adequately addressed, but been a while. Was a TC39 plenary since then. We need to find out if there have been any major changes.

#### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov

Dan: punted to the plenary.

#### [Partitioning Storage, Service Workers, and Communication APIs](https://github.com/w3ctag/design-reviews/issues/629) - @hober, @rhiaro, @ylafon

Yves: we wanted to have coord between different efforts to partition things - so using the same key for example. 

Yves: in 596 it [was noted](https://github.com/w3ctag/design-reviews/issues/596#issuecomment-840716598) that they do use the same partitioning key.

Yves: so I'm fine with this. 

Tess: I'm comfortable closing it.  Folks from different implementers doing a good job.  I'm inclined to just say. thumbs up.

Yves: porposed close and close at the plenary.

Dan: i'd like to see a closing comment from someone saying that.

Tess: I can draft a closing comment.

#### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov

Rossen: will to ahead and post a comment here.

Dan: I don't think they need to block...

Rossen: i will post an issue on fingerprinting - easier evasion. 

#### [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro

Tess: Talked to Rossen and Lea about this... forced colour mode is part of windows accessibility settings. On windows, Rossen doesn't believe that the system colours doesn't give you any more information than the media query you can use to find out what kind of forced colour mode you're on. Eg. background dark and foreground light? Then the system colours reflect that, but you don't learn anything new about the state of the computer that you didn't already know because of the media query. In practice there isn't a concern on windows. I was concerned, the fact there is an implementation of this and that is the case in that implementation is relevent information but the kinds of implementation decisions that windows made aren't requirements of the spec itself. Very easy to imagine other kinds of forced colour implementation where the system colour values provides additonal information. So we talked through a couple of theoretical examples. One I made up: a portable system with a display capable of extreme brightness, you can imagine it having an ambient light sensor and forced colour mode can adjust system colours dynamically based on ambient light to make the screen the most readable in the current situation. So the media query would match 'yeah' but the system colour values would change independant of that. I don't know if that's realistic. The point was I don't think there's anything here that requires the windows behaviour. I think while the fingerprinting concern from the system colour values may only be theoretical presently, it's real enough that CSSWG should make a note of it. On implementations where system colours can vary independant of the media query, this could be additional fingerprinting information. I need to comment on the thing - practically there isn't a problem, but enough of a theoretical thing.
... this came to us as an escalation, so not sure if that's the right asnwer.
... Lea, Rossen and I are all in the CSS WG. We agreed that if the CSS WG is escalating something to the TAG it shouldn't just be CSS WG memebers on TAG who come up with an answer.

Dan: value to having th ediscussion with the rest of the TAG. Folks on TAG and CSS have a unique understanding. By explaining it to us i think you're getting validation of the issue. I don't disagree with what you're saying. I remain concerned about any fingerprinting issue.

Tess: also - there's a [blog post from PING called antipatterns in web privacy or something](https://web.archive.org/web/20210419085236/https://www.w3.org/blog/2019/06/privacy-anti-patterns-in-standards/) - that mentions the arguement, it's okay to add this thing that has fingerprinting bits because thos efingerprinting bits are already exposed elsewhere. It addresses that. It's still a problem. You are doubling the ways in which they are accessible, doubling difficulty of removal of feature. So in the windows case where the system colour values don't provide mor einfo than the media query, it is the case that they provide the same info, which may be problematic. We want to feel like experts from outside CSSWG are looking at this more objectively than folks already in discussion.

Rossen: Both. Nothing wrong with subset of CSS folks. Shouldn't feel like a CSS WG topic is pushed to be discussed by a smaller group of CSS WG folks on the side. Tapping into additional opinion here is a must. We attempted this a couple of times. Arrived at the same conclusion. We either restrict colour values to keywords, or section off a part of the css object model that has fine colours that are a lie, or a default value, not mappable to the real actual colour being used. Same technique we used to evade detection of visited links so you can't fingerprint what a user has been browsing. 

Dan: right now nothing in the issue. Can someone add that in? This is an answer that we have.

Rossen: [will serialize this]

Dan: [proposed closed]

#### Federation & Browsers workshop

Tess: workshop report... sizeable group of people who want to figure out how to make sure identity federation can continue to work in a world without 3rd party cookies.  Also clear that that group should continue to tru to work together.  The workshop organisers might create a CG

Dan: i fed back that I didn't think it belonged in WICG. Pointed to the case of webxr and privacy being good examples of engaging with wider community. That would be a good thing, a CG that focuses on ID federation

Tess: also a sizeable contingent of people who seem to think the attempts by browsers of coming up with a privacy-preserving way to have federated identity without 3rd party cookies is bad.  Some policy and legal questions.  Brad Hill from facebook - read prepared remarks - which I didn't find terribly useful.  

Tess: all in [the minutes](https://docs.google.com/document/d/1nZt-bU-9FeoaavSuB6KPC7d3vyKuOhnA5QAd8kTN0z0/edit?usp=sharing).

Dan: are 3rd party cookies the main issue?

Tess: overall it was a mixed bag. 

#### Discussion of CEPC PR 

Tess: opened [a PR](https://github.com/w3c/PWETF/pull/171) - related to behaviour we have seen in the TAG repos. Has got good feedback so far.

### Breakout B (US / APAC) 

#### [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov
#### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov
#### [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss
#### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

### Breakout C (APAC / Europe) 

Present: Ken, Amy, Dan, Yves, Sangwhan, Lea, Hadley

#### [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo

Ken: it's proposed closing

Dan: can we? Plenary?

#### [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris

Dan: we asked for additional use cases, referenced pervasive monitoring is an attack rfc. Was an input for a joint TAG/IETF workshop from 2014 where amongs other things we had the call for moving more of the web to https. It's clear we can't give this a pass, we can't say it's fine to add to the web platform.

Amy: +1

Dan: and they haven't replied.

Sangwhan: the catch is it'll be implemented regardless

Dan: we can say they can code whatever but not into the web platform as a standard

Amy: anything they can say to make us say it's okay? Don't think so

Dan: if they're not going to engage for a whole month..

Ken: leave a comment asking for engagement?

Yves: do we want to make a statement? a longer thing? I think we all agree that the use case itself is dangerous

Sangwhan: has anyone seen intent to implement?

Ken: implemented.. flag you can turn on. In WICG repo. Chrome flag definitely implemented. Requires Chrome 90+

Dan: I could [write something, saying we'll close unsatisfied](https://github.com/w3ctag/design-reviews/issues/606#issuecomment-851925571)

#### [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo
#### [API for display-capturing the current tab](https://github.com/w3ctag/design-reviews/issues/625) - @cynthia, @LeaVerou

Ken: Still needs explainer

Dan: need to resolve is 625 a duplicate of 609?

Lea: understand it's not, but they're working together to consolidate them. Ken and I were in this call with Dom where he explained. 

Ken: Dom said he wants to reopen a TAG review with updated materials, updated exlpainer and S&P. Don't need the TAG to pick. Wanted to determine whether either request was safe. That was two weeks ago.

Lea: still pending external feedback? What about the other one?

Dan: 625, also 14 days ago Dom sent something. Multiple arguments going on with different people in these discussions. TAG feedback should be for them to sort it out..

Lea: not the TAG's job to consolidate

Dan: right, shouldn't be two issues open for us. But got pushback. Posting on both issues.

Yves: another option to close both and open another one if there is a dispute they want feedback on. 

Lea: last resort to use us to resolve dispute

Hadley: encourage them to work together

Dan: we need more guidance to figure out what we should be reviewing.

#### [Shared Element Transitions - Early Review](https://github.com/w3ctag/design-reviews/issues/631) - @cynthia, @LeaVerou, @plinss

Lea: not had time to look

Sangwhan: same

Hadley: user needs would be helpful. Jumps straight into how it works, features in android

Lea; they're assuming it's obvious, but it's not

Dan: there's a video.. Unclear what they're displaying

Lea: unclear why they can't do it with existing CSS transitions and animations, or an improvement that is incremental instead of a different API. 

Dan: there's previous efforts but no alternatives examined in the explainer.

Lea: is it page navigation transitions?

Sangwhan: except it's not really a page, but a state transition between to pages in a SPA

Lea: transiiton between two states in a SPA can be done with CSS transitions already. If it's a page transition that cannot be done right now. Significant difference.

Sangwhan: I don't think it's a full page transition

Ken: it's called element transition

Sangwhan: they have this promise they're resolving and it seems like..

Lea: I would like explanation on why existing web platform tech can't deal with these use cases

Dan: it says with some work the above effects can be achieved with existing frameworks. But don't say what they mean by that.

Ken: maybe this is to make it easier. A lot of people have wanted something like this for a long time but couldn't have have figured out how to do it. We had other efforts in this area, navigation animations etc before. Navigation transition design.. about having these animations, if you load a new page it ends up in the same page so will look like a nice transition instead of one load, another load.. you can do it today but it's difficult and a lot of people have no idea how. THey should state that this is about making it easier to use for developers.

Lea: so it's about having a bunch of transitions so developers don't have to thinka bout which properties to animate to what values

Ken: so it's loading another page over the same thing, loading a different document, and those things will line up. From google search you can click something, it animates out and loads a different page

Lea: point is that CSS transitions are too low level

Ken: that would be my guess, but they should make that clear. Coordination between different pages to make sure everything just works. Scrolling etc.

Yves: isn't it more about page contexts?

Ken: previous effort was having different pages loading, something animated so it looks like a smooth transition. Especially the use case was that you don't always control everything so you have to coordinate, eg. between google search and google maps, and they'd like it to look very integrated.

Sangwhan: I'd love to see their explanation of use acses. Example code doesn't give us much of an idea.

Hadley: and what they're trying to accomplish

Lea: I can write a comment, what I'm hearing is they need to describe use cases, how existing web platform features do not cover these..

Ken: or how this makes it much easier or more approachable to developers

Lea: is it about making CSS transitions more approachable, or does it do something that CSS transitions can't do today?

Hadley: sounds like we have questins about the user needs, and the developer needs. May have opinions on either or both.

Lea: Right

Dan: if it's doing something in a more easy way, that can be done using CSS transitions, it should be built on top of CSS transitions, layered approach that we promote, rather than a separate thing. Important to ask if it does something CSS transitions can't do.

Lea: exactly

Ken: about coordination between different sites, if it's going to ease that. Seems to be coordination required between different documents if you want to animate something together. Is it making that easier? Thinking about previous efforts. Don't see much in this document and don't get the examples. Could imagine that you make an animation and the new page gets the values where it ended up so it can show something at that place.

Lea: [will comment]

Ken: they have this shared element.. trying to understand how it's shared.. oh its a selector list. Confused that it's called elements if it's a selector list.

Dan: looking at S&P..

Ken: loading new page in the background.. and it will animate between the old document and the new document. I think that is the new thing, you don't have access to two different documents. Example, document transition start, and give it a list of shared elements, and document new.. in prepare you give it the old one. So it's going to load the new one in the background?

Dan: the multi page API? 

Ken: looking at shared element transitions example

Dan: they say the multi page API is still being designed, link to an issue

Ken: multi page is across origin?

Dan: SPA transition case has a working API, but MPA equivalent unsure, needs design. Linked from their S&P, their issue 2

Ken: not in the explainer. Second example looks designed to work across pages. Guess it could also work on the same page.

Dan: privacy issue they highlight is in the cross site navigation transition case... whether source and destination need to opt in to the API to learn about the content of the destination or vice versa. API allows customisation of UX when navigating between two sites. Is it okay without destination explicitly opting in to this behaviour? I'm on .... reddit, and I'm linking to CNN.. and both sites have opted in to use the transition API, and I then get some kind of animated transition that brings me to the CNN article. I don't get what the problem is. 

Sangwhan: question about accessibility. Animations should be controllable as a preference.

Dan: Right.

Ken: this seems to be a specific API to do the flip animation that people are doing today. Abstract that a way,a nd maybe designed in a way that could work across documents.

Sangwhan: tricky bit is there has to be a story on how users can opt out of this. Don't see that here.

Lea: prefers reduced motion? Or a different opt out?

Sanghwan: yeah for example. No way to opt out, no accessibility story

Ken: can you do that with web animations today?

Sangwhan: I think so? If not, that's a bug.

Lea: idea is web devs are supposed to check the media query.

Ken: yeah

Lea: wouldn't be good if turning that optin on would blanket cancel any animation that's already running. Reduced motion is not zero motion, some is okay, some is slow, some might not result in any motion... I think it's okay to leave it up to the developer, but that's a different issue.

Dan: ask them to clarify the issue in the S&P. They've asked a question. Is it okay to show a transition to a shared element on a destination site without the site opting in. And I don't understand this case. I want them to flesh this out a bit.

Ken: seems a bit scary.. if you depend on another site to do animations.. no coordination is going to be terrible UX

Dan: I don't think this opt out.. need to clarify. I'll leave that as a [separate comment](https://github.com/w3ctag/design-reviews/issues/631#issuecomment-851943792).

Draft comment:
```
Hi there @ianvollick!
We looked at this today during a breakout and we had several questions for you:

- The explainer currently lacks a list of use cases, so it's difficult to assess whether this covers the user needs and developer needs it was designed to address, or even what these are.
- It was unclear to us whether this API adds new functionality that is not possible using existing Web Platform features (such as CSS transitions and animations, or Web Animations), or whether it's a higher level abstraction of commonly needed functionality that is already possible, just harder.
- It was unclear to us what the reasoning is for an entirely new API over a more layered approach over the existing Web Platform features mentioned above.

Could you please clarify?
```

### Plenary Session 

Present: Tess, Yves, Ken, Dan, Hadley, Rossen, Amy

#### Status check on [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @torgo

`Thanks for bearing with us. We're happy to close this as satisfied. We appreciate the changes you made based on our feedback.  Thank for sailing with TAG.`

[posted and closed]

#### [Partitioning Storage, Service Workers, and Communication APIs](https://github.com/w3ctag/design-reviews/issues/629) - @hober, @rhiaro, @ylafon

`Thanks for bringing this to us for review. We're happy to see that engineers who work on all three engines are involved or are being consulted, and that there's a real effort to converge on one, interoperable partitioning model. Please do request another review in the future if your approach substantively changes!`

Tess: concern with interop- they seem to have the right people in the loop. seems to be doing well. We should encourage them to keep at it.

[posted and clsoed]

#### [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro

Rossen: I posted [a comment](https://github.com/w3ctag/design-reviews/issues/637#issuecomment-853079678).

Dan: looks good let's close.

[closed]

#### Client hints thingy

Dan: François [asked about](https://github.com/w3ctag/design-reviews/issues/632) a concrete example of evasion ...

Rossen: I see his point... but I don't think i can provide a very detailed example. I'll find a way to communicate.

#### [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529) - @hober, @torgo, @hadleybeeman, @plinss

Hadley: in the spec - in implementation considerations - advice to implementers on location sharing and revocation of permission. The thought is there that browsers have some responsibility. 

Dan: Agree.  So let's close on that basis.

#### [WebID workshop](https://docs.google.com/document/d/1nZt-bU-9FeoaavSuB6KPC7d3vyKuOhnA5QAd8kTN0z0/edit) updates? @hober

#### Breakout Rollup
#### Issue Triage