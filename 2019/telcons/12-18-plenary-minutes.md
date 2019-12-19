# TAG Plenary 2019-12-18/19

Chair: Dan

Scribe: David

Present: Lukasz, Tess, Yves, Alice, David, Dan, Hadley (end of call)

Regrets: Sanghwan, Peter, Hadley (first 2/3)

## Readouts from breakout sessions

Dan: Thinking about design reviews we looked at in breakouts:  anything notable?  Progress since breakouts where we discussed them?

Tess: I think so, from the github channel.  [Raw clipboard access API](https://github.com/w3ctag/design-reviews/issues/406) got comment yesterday afternoon.

Dan: This looks promising.

Tess: Maybe some progress there.  They're going to get an explainer out for the pickling alternative, though not sure if instead or in addition to the unpickled version.  I'm hoping for instead.

Tess: Another one with a bunch of comments:  [custom state pseudo-class](https://github.com/w3ctag/design-reviews/issues/428) issue.

Alice: Meta-point:  this is kind of derailed a bit by WebReflection.  Makes it hard to figure out where we are.

Dan: Opinion of this person's comments?

Various: A lot of text.

Dan: Tricky -- some of us have been going out and encouraging developers to get involved in our issues -- but maybe right amount of involvement versus dominating the conversation.  On the other hand, if the feedback is relevant... one thing to jam an issue with a bunch of personal opniions.  Kind of a judgment call.  Don't know enough to know which side of that I'd come down on.

Dan: Relabel, for breakout next working week?

Tess: APAC/California time?

Dan: Though Kenneth was on it.   Alice, did you want to be on it?

Dan: Compressed Streams, offscreen canvas (oh, it's closed, why are people leaving comments on closed issues?)

Dan: Anything else people want to raise from things that came out of breakouts earlier this week?

Dan: Should we do a readout of each one?

Tess: yes

### Breakout A

Dan: [JS self-profiling API](https://github.com/w3ctag/design-reviews/issues/366).  Closed it.

Dan: [proliferation of manifests](https://github.com/w3ctag/design-reviews/issues/423), migrated into design-principles issue

Dan: [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394), pending external feedback

Dan: closed the 2 Web of Things issues ([thing description](https://github.com/w3ctag/design-reviews/issues/357), [architecture](https://github.com/w3ctag/design-reviews/issues/355))

Dan: [Contact API](https://github.com/w3ctag/design-reviews/issues/337).  Just triaged it?

### Breakout B

Tess: closed [Modal window](https://github.com/w3ctag/design-reviews/issues/427).

Tess: Looked at [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) and agreed we needed a deeper dive on it.

Tess: had a long conversation on [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) and what to do with it.  Didn't end up with much of a conclusion.  David filed a design-principles issue on naming that could hep with some of it.

Tess: Didn't get to [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) or [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) .

Tess: Minutes were in same doc as Breakout A minutes.

Alice: Couldn't find cryptpad.

Dan: Can just go to cryptpad and start a code pad.

Dan: Did we agree to put all the minutes in one document?  But then somehow we put them in 3 different documents... or 2.  I think next time we should do one doc like we said.

### Breakout C

Dan: We started with [Serial API](https://github.com/w3ctag/design-reviews/issues/431).  Sangwhan and Ken were going to leave feedback.

Dan: Then talked about [MathML Core](https://github.com/w3ctag/design-reviews/issues/438).  A lot of back and forth about this.  Sangwhan was going to leave some comments.

Alice: I was supposed to as well, haven't yet.

Dan: Talked about [CompressStream](https://github.com/w3ctag/design-reviews/issues/410) and closed it.

Dan: So we didn't get to: [WebTransport](https://github.com/w3ctag/design-reviews/issues/389), [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370), or [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425).  Should schedule for next week or raise issues here if anything key.  I'll schedule them for first week of January.

## Triage of HTML Horizontal Review issues

Dan: Also in Breakout A we did a bunch of triaging of open design review issues.  Issue list now under 100.  If you look at untriaged we're downo to 3.  All 3 HTML issues.

Dan: [Subresources and navigation](https://github.com/w3ctag/design-reviews/issues/448).

Tess: How about me and Yves?

Yves: sure.

Dan: [security](https://github.com/w3ctag/design-reviews/issues/451).  

David: last 3 (of the 4 items) look pretty related.

Alice: can we consult?

Alice: What to do if we don't have expertise to look at things?  e.g., I could ask Mike West.

Lukasz: I should probably assign myself.  (inaudible)

David: Some of these things might not need a lot of review from us; might be well-sorted out.

Lukasz: Part of a big thing.  I had a quick look before we started this telecon and maybe it doesn't look that complicated.  So I'd agree with David on that one.

Dan: On to [browsing contexts](https://github.com/w3ctag/design-reviews/issues/452).

Dan: what's new about this?

David: browsing context group

Tess: and refactored creation of browsing conexts

Dan: Do we need to comment?

Tess: So when we did the initial triage of these things, we were looking for someone to look at them to make this determination.  Entirely possible that all of these PRs may fall into that category.  Browsing context groups may be interesting, rest of them may not be.

Tess: I'm happy to be assigned, but with someone else.

Dan: I'll jump in, can help out.

## Triage of HTML General Review issues

Dan: Down to 96 issues, which is good.  Also have a bunch of old HTML General Review issue which may need to be closed.  Everything from 242 to 269.  Tess, is that something you all looked at in breakout B?

Tess: I went through all of them, and commented on ones that I thought could be closed because I thought there was an obvious forward dupe in the horizontal review ones.  I'm pretty happy with how that will go.  Given the plan of record to do this style of horizontal review annually, I think it's reaonable to leave these open and close them as we actually do horizontal review in the relevant area.  Or mas close them now and hope they'll be covered by horizontal review as we go forward.

Dan: I feel like if there's been something like linking where it's been opened up, hasn't been any work since 2018.  And we're not going to look again for a year until another horizontal review, I'd rather bulk close these rather than have them sit here and create friction in our issue list.

Tess: works for me.

Dan: Unless we're actively working on them, I don't think we should...

Dan: Are there ones in this list that I mentioned... that are something we should really be keeping open?

Tess: offhand, no, but I wasn't here when these were opened.

Dan: They were opened in a process, by Travis.  I think... I'm not against lcosing them.  I think it would be better to close them.

David: Given resources/proces, I think it makes sense to close.  But one of the rationales for openng these was to look for things that should be in the platform but aren't, e.g., for extensibility.

Dan: Are there specific areas among these where we think there ought to be work done?  Does keeping these open help us identify those missing pieces?

David: I don't think so.

Dan: Finally 2 more: cross-document messaging and server-side events.

Dan: Barring objections, I'll also close these.

Dan: down to 81 open issues.

Dan: I'm encouraged by feedback we got on clipboard thing.

(Hadley joins)

Dan: [re: clipboard] good to see engagement.

Dan: Hadley, one thing we mentioned was that we closed WoT issues.  Did you get any feedback directly?

Hadley: No, will double-check my email.

## Design Review Triage - assign things to next milestone (6 Jan week-of)

## Design Principles Triage

Dan: In our [design princples issue list](https://github.com/w3ctag/design-principles/issues) we have many unassigned.  Don't have the wealth of labels.  Could go through and assign some of them.  Could assign somebody to think about what labels we should have in this repo to help progress.  Should we dedicate more of our time on first week of 2020 to design principles?  We'll be coming out of holiday season, not much will have happened.  Maybe a good time to come back to design principles.

Hadley, David: sounds good

Alice: We talked about making one week a month a bigger picture week.  Should that be first week of every month?

Dan: Not sure about every month, but think it makes sense for start of January.  Though I think in some cases we might need to move it around.  Let's try to do design principles and bigger topics the first week of January.

Dan: We have a fair number of open issues, could at least assign them.  A number of older ones assigned to ex-TAG members too.

Hadley: Another comment: WoT may be distracted by review of charter.

Dan: This issue list is a mess.  Need a dedicated breakout to go through this.  Unless people want to jump in and take particular issues right now.

Dan: A bunch are tagged with "write me".

Dan: I could ping Travis and see if he remembers what he was going to write, if he could comment and say what his opinion is.  We can come back first week of January, and start working on these in breakouts.

## Wellington

Alice: Wellington is confirmed.  Have meeting rooms, offered to cater lunch.  Offered an hour to talk about stuff they're interested in.  Some sort of welcome.

Dan: Maybe welcome in context of a developer meetup?

Alice: I did say we'd had a developer meetup in the past.  She said would be nice, would be nice to have in a different venue.  Would ask around to see if anyone wants to help.

Dan: Would be good to get developer meetup on people's calendars sooner rather than later.  Would want to do something that makes sense for community there.  Ideally driven by local meetup.  Could you cc: me on thread?

## Mini-retro on this week
