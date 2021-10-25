# W3C TAG Minutes - Mon, 18 October 2021

### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/10-18-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-10-18](https://www.timeanddate.com/worldclock/converter.html?iso=20211018T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Auto-expanding details elements](https://github.com/w3ctag/design-reviews/issues/677) - @hober, @LeaVerou, @rhiaro, @kenchris
* [HTMLPopupElement - &lt;popup>](https://github.com/w3ctag/design-reviews/issues/680) - @hober, @LeaVerou, @kenchris, @atanassov

### Breakout B (US / APAC) - [2021-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20211019T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

### Breakout C (APAC / Europe) - [2021-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20211019T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Pre-CR review of CSS Cascading and Inheritance Level 5](https://github.com/w3ctag/design-reviews/issues/678) - @torgo, @rhiaro

### Plenary Session - [2021-10-20](https://www.timeanddate.com/worldclock/converter.html?iso=20211020T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [charter process](https://github.com/w3c/w3process/issues/580)

* Breakout Rollup
* Issue Triage


## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/10-18-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-10-18](https://www.timeanddate.com/worldclock/converter.html?iso=20211018T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Peter, Lea, Yves, Amy, Rossen

Regrets: Hadley, Ken

#### [Auto-expanding details elements](https://github.com/w3ctag/design-reviews/issues/677) - @hober, @LeaVerou, @rhiaro, @kenchris

Dan: opener responded helpfully with a PR

Lea: do we need to wait for it to be merged to close?

Dan: looking at PR.. [writes closing comment](https://github.com/w3ctag/design-reviews/issues/677#issuecomment-945932450).

#### [HTMLPopupElement - &lt;popup>](https://github.com/w3ctag/design-reviews/issues/680) - @hober, @LeaVerou, @kenchris, @atanassov

Lea: Domenic left a really good issue we hadn't discussed... recently they opened a new review... for anchored positioning proposal. Domenic raised an issue around semantics. It's an antipattern to add a new element that requires ARIA attributes to give it its semantics.  A good point.

Dan: looks like an open discussion, ongoing. Might be worth supporting Dominic's point if you thnk it's good?

Lea: could upvote.. don't want to add noise

Dan: positive reinforcement..

Peter: i do agree - it gives a bit of pause - feels more like a base class than an element. if the goal is to create a toolkit for custom element creators then one could argue there's a role for that.

Peter: having lower level nonsemantic behaviours that have components - makes sense. If that's what they're trying to do and this is one of several - i can accept that as a design pattern.

Lea: good question to ask.

Peter: I've wondered if we shouldn't make HTML elements more geared towards building apps...

Lea: any precedent for native elemnts ... can browsers add a native element in future that inherits from popup? 

Rossen: ..composition of form elements.. input is the base for a few different elements.. input type text, date, color.

Lea: I found one - html video and audio element inherit from media.  Although there the base class is abstract.

Peter: this popup feels more like a base class.

Lea: which supports Domenic's suggestion...


#### XR Raw Camera Access

Dan: I think we need a call to unstall the review. Emailed Dom about limiting harms from getUserMedia because now the threat model has changed... get video stream and direct to face recognition etc.. Could we play a role in helping to raise that? The thing with Web XR augmented reality getRawCameraAccess is that they're trying to enable something using a proper webxr api that people are already doing, using getUserMedia not in the context of webxr apis, just doing ar in the browser and hacking it, so they want to create a proper api to allow people to do this including image recognition for ar trackers, markers. Real use cases. At the same time, risk. Hoping for a special session on monday.

Rossen: agree. Perhaps there's something we're missing?

Dan: talking at cross purposes in the issue. Maybe we can get to a point where there ar emitigations other than scary warnings to the user

### Breakout B (US / APAC) - [2021-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20211019T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present:

Regrets:

### Breakout C (APAC / Europe) - [2021-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20211019T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Yves, Sangwhan, Amy

Regrets: Hadley, Ken

* [Pre-CR review of CSS Cascading and Inheritance Level 5](https://github.com/w3ctag/design-reviews/issues/678) - @torgo, @rhiaro

Amy: one of their 'major unresolved issues' has been closed now

Dan: Updated issue templates...

[reviewing changes](https://www.w3.org/TR/css-cascade-5/#additions-l4)

Lea: we ahve [already reviewed cascade layers](https://github.com/w3ctag/design-reviews/issues/597)

Sangwhan: all the changes seem to be cascade layers related

Lea: not sure if all.. not sure what we're reviewing

Amy: shall we review the [major open issue](https://github.com/w3c/csswg-drafts/issues/4838) to do with FETCH?

Sangwhan: seems like a fundamental issue... this issue would be there even without the new mechanisms...

Sangwhan: I say leave this up to whatwg...

Lea: I agree.

Sangwhan: it's unrelated to these changes... I don't think anything changes with the new layer functionality.

Dan: they haven't asked us to weigh in, though they have listed it in the request

Lea: don't see any evidence they discussed it in a telecon, wouldn't call it a major issue

Dan: they anticipate it will be fixed before REC. I think they're just noting it as an issue. I say we close this.

```
Hi @fantasai - Thanks for this.  On review it seems the major changes are all to do with cascade layers which the TAG has already reviewed favourably: https://github.com/w3ctag/design-reviews/issues/597 so on that basis I we're happy to see this move forward.
```

Amy: Looks fine.

Sangwhan: LGTM

Lea: looks good.

### Plenary Session - [2021-10-20](https://www.timeanddate.com/worldclock/converter.html?iso=20211020T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Peter, Dan, Sangwhan, Rossen, Amy

Regrets: Yves, Lea

* [charter process](https://github.com/w3c/w3process/issues/580)

Dan: discussion on ac-forum, but nothing so far about TAG's role. Added some things to note it. I think we need a consensus view about what we think TAG's role should be. We should have some kind of veto power but not be involved in the critical path of charter development and not require TAG to sign off on every new charter. But have some kind of trigger based thing if someone requests a review or there is an objection or the TAG takes an interest then the TAG can review a charter and if the TAG does review it and finds issues that finding is taken into account in the charter review process. Right now it feelsl ike that happened with the DID work and as Hadley pointed out DID stuff went ahead anyway (without any judgement about DID) but noting the charter review ended because we felt the charter didn't include the information we were looking for on the use cases and it never came to a successful conclusion. That information should probably have gone into the review process but I don't think it did.

Sangwhan: sensible for us to chime in whne there's an FO at the chartering phase. obviously that should be baked into the process doc. YOu did say about a veto... there's going to be some interesting points where the FO raiser a member that is also in the TAG. I don't know how to deal with that. If we have veto rights does that given an org double veto rights?

Peter: one thing for a member of the TAG to raise an FO, another for the TAG to raise an FO with consensus

Sangwhan: the TAG can be another member org that can veto things?

Peter: yeah. We require TAG consensus, not an FO on behalf of an employwer

Dan: weird, if there's an FO that triggers a council which also includes TAG members. In this other chat around current/former TAG members make a statement about web3, that actually would / could poison the council process in some way.

Peter: I don't think the TAG would do a proper FO in this scenario, just a hard or soft veto and say there's a seroiusly problem and we get listened to. Also any objections we ahve should be limited to technical or architectural issues. Doesn't fit with web tech or violates this principle, not we just don't like it and want to see different deliverables. Don't want to get into the political side at all.

Sangwhan: risk.. don't know how big.. in terms of w3c having the objective function of trying to get as many members as possible, so getting people to charter things relevent to the web to increase membership. Plenty of stuff in the recent couple of years that didn't seem like it should have been a wg in w3c but it still happened

Dan: don't know if we need to get involved in that kind of argument. Tha'ts one reason I don't think it makes sense for TAG to be involved in every charter discussion. If w3m want to bring in a bunch of widget manufacturers and want to create a widgets and the web wg, it's not the TAG's job to say widget manufacturing is not compatible with web architecture. It might be our job to sa that, but not to say this isn't related to the web. 

ROssen: is this a matter of the chartering process itself? 

Dan: how do charters get reviewed in w3c process. What official role does TAG play in that process? That's what's being discussed on this process cg issue. If we have opinions I think we should be voicing them. 

Rossen: maybe in the minority, I don't think TAG should be involved in every single charter or recharter. Majority are just process

Dan: I agree

Sangwhan: totally agree. Proposal I put up was to only look at it if there is FO. Use the FO as a trigger

Rossen: arguably with the council and all of this we'll be involved anyway. OUtisde of that why should the TAG be involved directly prior to the FO? 

Sangwhan: my proposal was not about prior to the FO. I don't think we have capacity to look at every single charter

Dan: this is not about FOs. This is about getting the TAG involved earlier in charter development to forstall future FOs. One of the summaries of the discussion that I took away from the ac list was if the TAG were involved earlier in the charter process we wouldn't have this FO. I said I'd be reluctant to involve the TAG in every charter because.. and someone said we'll have to invent a new group for charter development. He does have a point that having the TAG have an official role in charter development might be a good idea, but not for every charter, only on a request basis. If someone is developing a charter and there's a question about it, it might not get to FO stage, someone has a question or the Team might want TAG opinion. At which point what is the output of that opinion and what standing does it have in the process? I think more formal standing than advisory.

Rossen: maybe. Slippery slope.. "but the TAG said.." becomes a way during further charter discussions and maybe will discourage some groups from raising FOs because now they see a higher upward battle if the TAG seems to agree with something. The fact that TAG is in the capacity to weigh in on both sides meaning in the chartering and in the FO stage is kind of .. we will be seen as playing both sides

Dan: I see what you mean

Rossen: for that reason alone I'd say charter whatever you want, you will have to get all of your specs and features reviewed anyway. At that time on the technical level we are engaged, we will provide al of the feedback and potentially steer additional discussions, but that's just what the TAG does today. Seems sufficient. 

Dan: whatever happens has to be in such a way that it doesn't politicise the TAG. We don't have a very political atmosphere here. I don't want that someone creates a technical charter review board that is by de facto making architecture decisions and then we've got two architecture boards in the w3c and we end up with tribalism and saying we dn't know what they/we're talking about.. 

Rossen: agree

Dan: chatted with team about the funnel charter process.. maybe raising awareness to TAG of new charters, having stuff in our agenda where we have 5 mins to review charters in development and just keep our finger on the pulse of it

Rossen: isn't this mostly the same as what we are already kind of doing with incubation community? In WICG when new things come on board we want to be there so we are providing early feedback as necessary. To me charters are essentially a group process of ideas moving forward. To me that's basically in the same level of priority or engagement as anything new to WICG. Something is about to be happening, this group of features and work not just a single one, FYI, and at that point, if it's non-binding then we are in a position to go and engage, otherwise not approved or unapproved, just goes through without TAG saying anything

Peter: not require TAG approval for a new charter, but give us an opportunity to review and weigh in. The only thing missing there is if we say we have a problem with a charter for technical reasons, I don't think anybody has any obligation to listen to us. That's what probably needs to be changed.

Dan: exactly

Peter: dn't want to be rubberstamping charters, and don't want to have to review every charter. Just a ping to say there's a new charter and we can do a sniff test to decide whether to get involved. It can move on without us, or we can rase objections and they have to be addressed. Not formal objections with the council.

Dan: I don't like the idea of the TAG raising a formal objection.

* Breakout Rollup

Dan: [recaps A&C] closed some things

* Issue Triage

