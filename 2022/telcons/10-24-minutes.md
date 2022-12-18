# TAG Teleconference
#### 24-26 October 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-10-24](https://www.timeanddate.com/worldclock/converter.html?iso=20221024T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [CSS Overflow for replaced elements](https://github.com/w3ctag/design-reviews/issues/750) - @plinss, @atanassov
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro
* [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo
* [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

#### Popup API Joint Meeting

### Breakout C (APAC / Europe) - [2022-10-25](https://www.timeanddate.com/worldclock/converter.html?iso=20221025T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon
* [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon
* [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion
* [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon
* [Requesting TAG review for Trace Context Level 2 changes](https://github.com/w3ctag/design-reviews/issues/777) - @ylafon, @maxpassion
* [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2022-10-27](https://www.timeanddate.com/worldclock/converter.html?iso=20221027T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Yves, Hadley, Rossen, Lea

Regrets: Dan, Tess, Amy


### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Agree to close.

### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Lea left comment asking for clarification.

### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

Lea left comment asking if the TPAC session was recorded.

### [CSS Overflow for replaced elements](https://github.com/w3ctag/design-reviews/issues/750) - @plinss, @atanassov

Doesn't seem to need TAG review. Minor concern about iFrame but seems to be addressed. Closed satisfied.

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro

### [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo

### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

### Popup API Joint Meeting

Guests: Mason Freed, Aaron Levanthal, Dan Clark, Scott O'Hara, Greg Whitworth, Chris Harrelson

plinss: Thanks for joining us. We have questions, wnated a higher-bandwidth discussion. Who wants to start?

Lea: I was wondering about this minimum-role idea. What kind of use cases does this serve that having a default role wouldn't serve?

Aaron: Popup attribute can be used with anything, like a table. We don't want to remove those useful semantics that are already there. But if there are are no semantics, and it's just on div... We need to have at least a role of group.

We also think we need it for other rhings: contentEditable attribute

Scott: contentEditableIndex... other things on any HTML attribute. This would greatly improve the accessibility of various elements on the web.

Rossen: Let's have context on how we got here. You started with one proposal, a scriptable API to expose this. From there, you went on to define the popup element. The popup is an interface that defines this behaviour that some elements may not benefit from etc.

The popup element proposal was great, except our only question: what is this element on its own?

And then you swung away to this being an attribute. And we wondered what this means on a table column?

We had a conversation at TPAC. Thought we should use the ARIA role button and align that attribute with this set of elements.
Then we came back here and discussed it as an attribute, and still the group in the TAG conversation felt that the popup element was still a better path forward. 

So this is where we are.

Lea had some questions around it being an attribute, and exploring/reiterating why an attribute makes more sense than an element.

Mason: We didn't have a js API to start with, it was a popup element. At that point, we all agreed, it was the most straightforward. Problem: we ran into fundamental accessibility, semantic issues. It's unclear what it is, what it represents, what role it should have. We ran into that issue in the second of the three tag reviews. It was a very slow turning of the barge to move from element to attribute.

I fought hard, thought we should have a popup elemenet -- but was convinced after the discussion and input from a11y folks... we would be doing a disservice by introducing an element.

So we said what about introducing an attribute, so the element provides the semantics? This solves all the issues. The behavriou is presentational. It's also more flexible, once you're used to grabbing an attribute to do this, the rest is pretty natural.

Everyone seems to be in agreement.

Finally, we've also had people say this should be in CSS. it's a presentational thing. it sounds right until you dig into the details, and there is a whole doc that i put together designing this in css, and there are some real issues with that.

That's why we're here.

Lea: can you share these use cases only served by the attribute?

Mason: re table... make an element that is a popup version of every other element. There is a slippery slope to another 105 elements that all popup.

Lea: why would you not wrap the table with a popup? It's what you do with a dialogue

Mason: let's say you have an element and you wrap the table... what is that popup element's role?

Scott: I brought this up... pathway was not acceptable by the HTML editors. They said there is no difference between adding elements you want ot be the popup and adding an element to do it. You could do it at the table row, but you'd have to put other elements in the table... There are more use cases to applying the attribute to the element, than there was to create a generic element solely to put semantic elements inside it.

Mason: that's why we thought this was the more natural solution. You have an element like a table row. We don't need to add a new element, just add the behaviour via an attribute. 

Lea: it's fairy common in HTML to have elements with a single child, like with dialog

Mason: yes, but both the dialog and the child has its own semantics. This generic element doesn't have that. The generic popup element would be like div, having no semantics. HTML editors said we have span and div for that. And you can put a popup attribute on it.

...We went down this road pretty far. We started with this generic popup element. there are some use cases you want people not to do with a generic popup element, lke a list box. Actively harmful for a11y. We enumerated them, and the ones left over for a generic element were the bucket of things we can't think of right now. 
 
Lea: since we're introducing minimum role, which is a group... why couldn't hte popup element have this as its default role, and could be overwritten?

Mason: this problem is more than just this behaviour. It exists for contentEditable, etc.

Rossen: Let's get more specific on these problems with a11y. Could you share one or two?

Also, is there an expectation of popup behaviour in terms of multiplicity? Do you anticipate being able to have a list of popups all at once, or one to one

Mason: pop-ups are one at a time. If you have one list popped up, and open a second, the first goes away.

Rossen: no, I want to open two at once

Mason: that isn't part of the API. You can have popup=manual, like toast. but not the nice behaviours. But... unless they are nested, then you can have two. It's UI pattern, people don't generally have two unrelated popups. 

Rossen: Not sold. It's a good answer, but it's not really satisfying. You're precluding a UX pattern by default, by saying it's always one at a time. Functionally being able to take a list and pop all of them up, that shouldn't be a problem, regardless if you're using the attribute or the element

Mason: mechanically, sure. But is this a good use case for users?

Rossen: Not a UI expert, but for me it's not out of the realm of possibilities. For automation, or some other ability to... taking a quiz, showing all the questions. Point is, there could be more use cases.

But let's not worry about the UX, but would a grouping or element make sense, or the attribute be easier?

Mason: mechanically, both could be done, with an element or an attribute. I think a decent chuck on the value of this API is the number of things it does for you in a "correct" way, many common things that are difficult to get right. This is bad for users. 

Rossen: we are sold. Don't get us wrong. It's the details here that matter. But on the hehaviour and goals, we would've signed off a long time ago

Lea: and because the use cases are so common, that's why it's important to get it right.

Chris: we sent a doc on how it pertains to a11y, as discussed at TPAC. Should we discuss?

Rossen: I thought it made sense

Greg: If you all have this list enumerated, I know the group is interested. We've just filed another one from whatWG. WE have talked about this for many months, and we do have the use cases, we would just have to go dig for them. So if we could turn these into concrete issues, that would be great. I'm happy to create them if you want to enumerate them by email

Rossen: you mean issues outside of our tag issue?

Greg: well, splitting them up so you all can ask your questions, drive them to completion.

Mason: your 2-popups-at-one-time thing might be one

Rossen: the popup element that can potentially introduce semantic changes -- this is hwere i need confirmation -- for example, if a wrap parts of tables, then the fix up of the table might get screwed up. which isn't desirable. the popup element at that point becomes part of the solution

plinss: that introduces structure of the list in ways I may not have intended, as an author. so i find that compelling.

lea: is it a common use case, for a table row?

peter: yes

scott: more so than showing multiple popups at once

... it would allow the row to go to the top layer, breaking out of any overflow. I have teams that want this, a row with focus or hover in it. This would make it work, not break the parser.

peter: separate question: you mentioned doing this behaviour in css vs attribute. for what i've seen, a large percentage of what people do with popups in css. why is the behaviour still forced and not done in CSS?

mason: we designed this for display top layer. Biggest issue: a lot of the value is the behaviours -- if you click somewhere else, it goes away. CSS can't do that. 

peter: same is true for all the other things. I saw a demo of a menu on the side that also slides. but whether the thing is active as a popup or not, i could use a css pseudoclass. and all attributes match that pseudoclass.

mason: if you give it a pseudoclass, you have issues. But let's say you do that, and it gets light dismissed so it's no longer showing, then you as a developer, what do you do? Put it back in the top layer?

lea: my understanding is that it was a separate closed/open state. there is no circularity, because you cannot get that state in css.

mason: 

lea: whether or not it's in the top layer is presentational, and open/closed is a separate thing.

mason: we designed the entire feature in css, and we can share our conclusions and process with you.

peter: i'm sorry we don't have time today to dig into that.

lea: i'm not arguing this should be an exclusively css feature. 

peter: the behaviour is the important part, and should be controlled as you've done it. I'm just not sure why this one bit is CSS.

We're out of time, thanks for joining us

Lea: let's continue this in the issue.


## Breakout C

Present: Amy,  Hadley, Yves, Sangwhan

Regrets: Dan


### [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon

Yves: still pending feedback. Bump by two weeks as I won't be here next week.

Hadley: do we need to nudge them?

Yves: I don't think so, I can look at other places where it might be discussed

[bump +2 weeks]

### [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon

yves: still waiting for feedback on their side. Amy?

Amy: I  haven't looked recently...

yves: disucssion is they want to allow only * , with nothing else. We thought it was a nice way to shoot yourself int he foot. They wanted to solve the issue of CDN with a large number of networks. The issue is there, we've asked for a way to mitigate that.

so... still pending external feedback. I've bumped the deadline.

Sangwhan: [nudged requestor]. hopefully they'll get back to us before the plenary.

### [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion

Max: Sangwhan says he has comments but hasn't responded yet. Will follow up.

Hadley: hopefully Sangwhan can respond before plenary

Sangwhan: they want us to choose option 1 or 2, and i'm not sure about either. 1 is all async, and 2 is sync and add async as a suffix. both are ugly. if it's inevitable in the platform, we should have a principle for it. Seems there is an implementation detail here being unnecessarily exposed to the user. imagine you locked everything down to be sync or async.. you'd have to change the paradigm. I wanted to ask domenec, but I feel like both approaches are not great. If you think about making an asyc message sync, there is a semantic for that already. I'm sure they considered it.

what do others think about putting sync or async at the end of every API call?

Amy: why is the wg asking the TAG?

Sangwhan: they couldn't come to consensus

Amy: have they shared their minutes where they show their thinking?

Sangwhan: I read some....

Amy: I suppose a TAG perspective would be about consistency on the web platform?

Sangwhan: there is nothing to be consistent with.

Amy: so it would be setting a precedent

Yves: we usually try to move away from sync calls. Better for performance.

Sangwhan: yes. if we had to chose, it would be asyc by default and sync by exception. but do we want these patterns?

Yves: TC39 might have a voice? 

hadley: what's the best way to take this forward? a call with them? including tc39?

sangwhan: we lost our TC39 liaison, so i'm going to message Dan Eranberg to see what we can do.
https://cryptpad.w3ctag.org/code/#/2/code/edit/XbFesGNiFynT3ReFOoiiYEIN/
hadley: okay, then do you want to pick a time with breakout C for that call?

sangwhan: may be us/APAC. if it's the same liaison. Let me check with times and see what we can do.

But given that there is an await semantic, i feel like putting it into the API naming is not great. if we're going to do it, we should write a principle about it.

Both seem to be ugly. Not sure what others think.

Yves: it's not nice, but it may be the less evil of all the things. 

sangwhan: there is a gap, in await, that we're missing that should probably be addressed. rather than stick sync on everything.

yves: that's why it's better to bring in TC39. 

hadley: so when we do have this call with TC39 and the authors, that will be the same question?

sangwhan: semantically, xsync() vs await x should semantically be similar things but there is clearly a gap here. 

Sangwhan: I'll report back on who should be involved, and will make this call happen. 

### [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon

Yves: no progress. I want to look at the impact of the new syntax on the existing parser and things that can be treated as ? identifiers or not

Hadley: before plenary?

Yves: I won't be in plenary

Hadley: Dan said 6 days ago that we'd hope to get back to them soon. Can Dan carry it on while you're gone?

Yves: I can comment to say it looks good but need to work on a few things.

### [Requesting TAG review for Trace Context Level 2 changes](https://github.com/w3ctag/design-reviews/issues/777) - @ylafon, @maxpassion

Max: I looked today, this is an updated version from an existing standard. The main update, explained in the explainer, is to introduce a new flag called randomTraceID. When this flag is set, the rightmost 7 bytes on the trace id will be randomly generated. the purpose is to use the global unique randomly generated id to for eg. sampling purposes. I think it makes sense, and don't have other comments since it's only updated.. [max dropped off the call]

Yves: I looked at it and agree with Max. It doesn't seem to be adding anything harmful. Looks okay, not contentious.

Max: agree

### [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman

Sangwhan: late review, more concrete proposal without FPS

Amy: will look at this later this week, [bumps milestone]

## Plenary Session

Present: Peter, Amy, Hadley, Max

Regrets: Dan, Tess, Lea, Rossen


### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

### [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

### Breakout Rollup

#### Breakout A

Hadley: we agreed to close 705, and 750, and had the popup API meeting, which we agreed to continue in the issues.

Peter: Lea left a long comment. Valuable points, but I don't see that changing about element vs attribute. My main concern is the behaviour of being popped up pushes it into the top level presentationally and I think that should be done with CSS. They argue you can't do it all with CSS, which i agree with, but the behaviour of being open can be controlled by the popup api but not the presentation. We need to mint a new css property to control the top layer behaviour, we can't do it with position or display, more of a z-index. No reason that behaviour can't be by default in the UA stylesheet and not baked into the algorithm. That gives authors a lot more controls. But we can have that argument in the CSS WG. Worth TAG having input there to say let's not cross the streams of semantic and behaviour and presentational all at once. Let's focus on behaviour. Leave presentation for CSS.

Hadley: they said they've thought through CSS implications, but didn't give any specifics.

Peter: I looked at their arguments, I think they were based on a different model doing a whole lot more through CSS. One of the original designs was to have this top layer pseudoclass and use that to control top layer, does create circularity problems, that's off the table now so there's no reason you can't control top layer behaviour with an open and close class without being circular. It's like being hovered or clicked or checked. The open state will be controlled in the DOM. At one stage they had problems that it wouldn't work, but in the current design I think it's fine. I think we should push back on that, and let the CSS WG hash that out.

Hadley: what's the best way to do that?

Peter: input into their issue. Lea did touch on that point as well. We should separate the two arguements, and have the presentational discussion indpendantly from the element vs attribute discussion.

#### Breakout C

A couple of issues we thought might be updated by plenary, but they haven't been.

Max: seems no issues with 777 - wanted to ask for other opinions, but if not can close satisfied.

Peter: go ahead and close


### Discussion on scheduling meetings

This meeting time doesn't seem to be wokring for many TAG members

peter: in theory, once the time-change vortex settles, we may not need to have this time.

hopefully we can figure something that works.

### Issue Triage
