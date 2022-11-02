# TAG Minutes - Week-of Mon, 31 October 2022

## Agendas

### Breakout A (Europe / US) - [2022-10-31](https://www.timeanddate.com/worldclock/converter.html?iso=20221031T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia
* [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro
* [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo
* [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman


### Breakout C (APAC / Europe) - [2022-11-01](https://www.timeanddate.com/worldclock/converter.html?iso=20221101T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman
* [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon
* [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion
* Privacy Paper

### Plenary Session - [2022-11-02](https://www.timeanddate.com/worldclock/converter.html?iso=20221102T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2022-10-31](https://www.timeanddate.com/worldclock/converter.html?iso=20221031T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Peter, Lea, Hadley

Regrets: Tess, Rossen

#### Breakout times

Breakout C remains 0800 GMT Tuesdays. 

Breakout A will be at 1700 GMT / 0900 PT from next week.

Start putting some design principles issues on the regular agendas, but not cancel the dedicated design principles (etc) week.

#### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia
#### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro
#### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro
#### [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo
#### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
#### [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss

Dan: talked about this with Chris H. He wanted to know what he could do to help nudge this. Should we close it, or push more?

Lea: the issue is that this wouldn't work for externally loaded import maps which we don't yet have right?

Peter: yeah

Lea: but can you dynamically create a script element and append it with an import map? Then you have the same issue of import maps being created afterwards. If that works, and if you can create importa mpas at any point in time, even if this was async it still wouldn't account for that. So maybe it's okay that it's syntactic sugar over what authors can do already and therefore it's sync?

Peter: leaning toward it just being sync, a snapshot of the current state. TC39 already dealing with this. node shipped an async version and they're changing over to a sync version. I don't think we were complaining about it being sync, I think we were just curious about some behavioural issues.

Lea: looks like we're okay with this being sync? [leaves closing comment]

**agreement to close**

#### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Lea: I pinged Rossen on slack. I've spent time looking at this and [replying with my own feedback](https://github.com/w3ctag/design-reviews/issues/743#issuecomment-1292624647). They want a response that reflects TAG consensus.

Peter: there was still a bunch of pushback on element vs attribute. I'm convinced that attribute is fine. Maybe at some point in the future it makes sense to have an element as well but I thinka ttribute is the right direction. I do agree that I don't believe the popup should be controlling the top layerness of it - that should be controlled by CSS. The attribute should just control whether open and close pseudoclasses are being applied.

Lea: that's the point I'm making.. they said I didn't read the document. The fundamental disconnect here, why some people see it as trait vs identity of element, is that their explainer is inconsistent in this. They talka bout popups sometimes as if their main thing si being at the top layer. The example they gave of a slider that is on top of a video, the only thing that slider needs is being at the top layer - no other behaviours of popups. I don't see why it's described as a popup. And the tr example as well. I'm unclear why you'd want to put the table row at the top layer to highlight it. You don't need dismiss, ARIA roles, you don't need all the other stuff that come with a popup - just some way to style an element for being at the top layer. If we separate these concepts, an element being at the top layer doesn't need to be a popup.. then it becomes a nice package of separate behaviours...

Peter: there are other examples, tab index.. there are other examples of popupness that are orthogonal to being top layer, top layer is not required and shouldn't be tied to that. But it is a convenient mechanism of managing state. Being able to assign that behaviour to other elements is useful. 

Dan: we just need Rossen.. Peter can pipe up on the issue?

Peter: I agree with part of it. Can chime on the CSS presentational aspects of it. Don't know Rossen's opinion on that yet. I don't know if we have consensus on attribute vs element. Not sure popup is even the right name for it any more, especially if it's just the behaviour of being open or closed. Some of their examples are menus that slide in from the side. It's the same as a details element, you're giving that behaviour to any random element.

Dan: makes me think about developer confusion. If we're naming something in a confusing way and say use popup for this but it's not actually a popup that's going to be one more thing where people say just use it but don't worry about the name...

Lea: it's now popover. popup clashed with other parts of the web platform. iframe sandbox keyword, allowpopups, unrelated - about window.open.

Dan: maybe we can get Rossen's feedback by plenary and discuss more

#### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

#### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Amy: left a comment last week, no response

Hadley: is there another way we can nudge them?

Dan: can ping on slack

[bump a couple of weeks]

### Breakout C (APAC / Europe) - [2022-11-01](https://www.timeanddate.com/worldclock/converter.html?iso=20221101T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Sangwhan, Amy

Regrets: Hadley

#### [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/779#issuecomment-1298200582) asking for further info.

Amy: Finds [Mozilla Standards Position](https://github.com/mozilla/standards-positions/issues/678) and [Webkit position](https://github.com/WebKit/standards-positions/issues/50).  

Dan: Let's re-review at the plenary.

#### [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon
#### [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion

Sangwhan: there is work in ECMA to make this less terrible. One year out until we can use it. Asking to follow that pattern they will have to wait a year to ship. Async by default and sync as explicit will be the less terible default. That should be the recommendation we push for.  It would be nice if things could be done in an idiomatic way. I will also draft a principles section on how to deal with this - and also note that once there is an idiomatic pattern in place then consider following that patttern. 

Sangwhan: **[files issue](https://github.com/w3ctag/design-principles/issues/402) in design principles**

Dan: would this be a temporary design principle until TC39 bakes this into js?

Sangwhan: correct. Might be longer than temporary. So feedback on this issue is to recommend the less terrible option.

#### Privacy Paper

### Plenary Session - [2022-11-02](https://www.timeanddate.com/worldclock/converter.html?iso=20221102T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### Privacy Document

Amy: working on adding citations...  Sangwhan raised some concerns about sharing...

Rossen: can we ask sangwhan and then bring it to the github?

Amy: Can people also look for "to do" and see if they can add?

Amy: we can also share with the privacy task force

Dan: let's try to get the draft out by tomorrow.  The point is to put it in github - marked as a draft (not final) and begin circulating to a wider audience for comment.

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
#### [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

Dan: two weeks ago we asked for information, they said it shouldn't have been marked as early but they appreciate TAG feedback including [specific question].

#### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Dan: we've had some comments..

Lea: I'm not following the argument

Peter: the aspect that makes sensne to me is mixing sync and async functionality, some will affect layout and some won't

Lea: if the API is async it will give them stale information?

Peter: I'd think it would give you more up to date inforation

Lea: exactly

Peter: to me it's an argument that all these other APIs should be async

Lea: Perhaps there's a misunderstanding about what an async api would do if they think it will result in stale information

Peter: looks like argument is about raf(?) callbacks so .. you get the result but in the process raf is called and somebody has changed the DOM. I don't know if that would have been called before or after the async stuff would have resolved

Lea: right. Who can we ask? Seems like a low level question. Should we ask an implementer if this is accurate?

Peter: isn't Vlad an implementer who would know? Trying to work out if it really matters.. if you have raf callbacks and you're manipulating the dom.. it just changes the order of execution I guess, the information wouldn't be stale but it will c hange things anyway so what does it matter

Lea: appplies to any async api about layout

Peter: not sure the argument is complelling

Lea: so it's correct?

[scribe missed a bit]

Dan: let's ask Tab

Peter: I don't recall this being discussed recently in the CSS WG

Lea: it was discussed a lot a long time ago, but not so much sync vs async, but more about the name and what visible actually means etc.

Dan: who is vmpstr ?

Rossen: Vlad from Google.

Peter: it's part of a bigger problem that we have a number of sync methods that should have ben async from the get go and we're just adding more. We need a comprehensive look at all of these and move towards making them all async rather than arguing each one

Lea: we do have a design principle for that 

Peter: the problem is.. I don't think we're going to get that end result of where's the effort to fix this problem as a whole as opposed to fighting it for each individual new feature. To me that feels like a Houdini problem. What's happening with that?

Rossen: every time I ask folks, they say "we should!" And that's where it ends.

[discussion about how CSS WG works]

Peter: propose opening Houdini issue...

Rossen: There's [issue 5115](https://github.com/w3c/csswg-drafts/issues/5115) in css working group... if we have more specific guidance from CSS on this issue then we can apply it here [in #734]. This is how you avoid breaking the loop... 

Peter: My concern: giving more APIs that are async ... it's related... we need a definition of what the loop is and what it does. Follow-on task : proposing async replacements... 

Rossen: we can open a separate Houdini issue and have discussion there... 

Rossen: Tess & I concluded (in review of event loop) that if we have this [5115] issue done and something we can point to then everything else becomes much easier.

Peter: **I will file an issue in Houdini and reference these other issues and we go from there.**


#### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Rossen: I don't have an opinion stronger than before...  For myself I'm convinced that the attribute approach makes more sense given the disruption that elements can cause... 

Lea: the use cases where this is a problem are also use cases where all you want is to place something on the top-layer, you don't need any of the other popup behaviors in those cases it seems. In most cases popup is used as a container, with `<div popup>`.

Rossen: the disruptive behaviour that the element solution has walked me back from that idea... we don't design features that work for a majority of use cases and have known bad effects. This is an example of that - it has known bad effects.  I'm happy to let them continue pursuing this. However I'm still missing the a11y point they were making. I'm willing to believe they are taking a11y seriously due to the people involved. 

Lea: i have strong reservations about this approach but it's OK.

Peter: I still have reservations about the top layer behaviour.  Painting order? Designer view of top layer vs User Agent top layer. One at a time? Does it close other things that are already in the top layer?  

Lea: Things in the top layer are painted in the order they are added".. 

Peter: "UAs can ..."

Lea: one of the arguments against CSS syntax: they would have to use a different UA top layer and a 2nd class developer top layer... if developers could put anything in the top layer. Once developers start putting popus all over the place that could also become a problem. It seems like some of these use cases are conceptually popups and some are "i just want to put this element on the top later" ... if popup needs to account for all of these use cases then that makes for a clumsy API...  Orthagonal concepts....

Dan: I'm trying to figure out how this won't cause a huge mess from a user perspective. If you have multiple.. if you have ads and other 3p content in the page, isn't there going to be an arms race to see who can get on the top layer first and obliterate the other top layer..

Lea: z-index 999 problem all over again. Not sure using an attribute is going to fix that

Peter: I don't buy the argument that the popup api avoids the z-index problem. The whole notion of top layer feels underspecified and undefined

Rossen: and not necessary as part of this feature/behaviour?

Peter: agree. I'm fine with popup being an attribute for now although I agree with Lea's point that once we decouple everything the attribue argument makes less sense. But first I think the top layer behaviour should be decoupled from the top layer element. Describing behaviour, triggers pseudoclasses. How something renders, what layer it renders on, should be defined completely in css. we can have all the other discussions about that. The notion of layers needs to be better thought out and defined - done independantly in CSS. (I don't think it shoudl be done via position or display, a separate property. I think we should do this as part of a bigger project to fix the z-index problem. z-index acts within a layer, and let that be author defined.. it's a separate discussion.)

Dan: sounds like a bag of feedback... what can we leave in the issue? Can we say we're okay with the attribute thing and say we have other concerns? And we'll work on documenting them?

Peter: [will post a response]

#### 

#### Breakout Rollup
#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
