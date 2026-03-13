# TAG Minutes - Fri, 6 Mar 2026 - London F2F

Present: Marcos, Matthew, Lola, Hadley, Yves, Brian, Christian, Heather, Yu Sen, Xiaocheng, Jeffrey

## Working mode

Scribe: Matthew

Hadley: I've collected some things we talked about over the past few days...

Heather: Not sure what that "working mode" means exactly?

Hadley: Thus far, everything has come up from what work we focus on. to how we organise ourselves. tooling we use to manage our work; what we do when we don't have consensus; how we bring in external guests. Everything except what we're going to deliver on a particular topic. The list...

* Would be helpful to have an understanding of why we do late reviews (too late?) Should we? Discuss.

* What to do when we don't have consensus

* Identifying targets, deadlines, outcomes.

* More external people coming in to discuss stuff. The mechanics of this.

* Martin mentioned IAB has a person assigned to an issue to get it into a state for review - we could consider.

* An AI to help people write explaienrs

* An AI for reviewing explainers

Expect we don't have consensus on the latter two.

Brian: Curious about the IAB thing - is it like TC39 Champions? You need somebody to get on board and represent what's your feature, leading it through. I don't know that that works here. Is it like that?

Heather: The TAG's purpose would be supporting said champion.

Jeffrey: IIRC IETF calls them a Sheppard

Hadley: It'd be someone to help get the explainer etc into a state for review.

Heather: A Shephard is more about making sure the process is followed.

Yves: Which is the role of W3C team contact

Jeffrey: Except for early work, which doesn't have one.

Hadley: It's not TAG team's contact to help someone to get input on their proposal

Yves: Agree, but the Sheppard would help with progressing through the publication track.

Jeffrey: I think we should not do it. Anyone reviewing work that comes in should do it with an eye of helping the work get finished, rather than just judging it. But I don't think we sjhould ask that person to take responsibiltiy for guiding the proponent.

Brian: That's my question - how to do that - particularly if it's something you're critical of?

Marcos: We should be asking people questions to lead them, but not engineering solutions for them, as this would mean we are generating IP for them. We can direct them to the principles, and add new principles as needed. E.g. architectural concerns around using an array for soemthing that could go over an IPC pipe. We can speak to the architecture.

Hadley: Agree with Jeffrey that this isn't a role we can play, due to lack of time. Plus many of them are not willing to do the work. On the IP point, all of our contributions are covered by teh patent policy, no?

Jeffrey: It's a grey area.

Yves: +1

Hadley: So we should be OK re IP but my concern about the rest remains.

Jeffrey: I think we're done with this topic, except to add:

* I think we need to do more on documents; we are biased toward design reviews and don't decline them.

Xiaocheng: What do we do if a feature has launched but we don't agree with it?

Hadley: We may decide it's too late and we give up, or we review and express concerns.

Heather: I agree assigning a helper, not just a reviewer, is more time-consuming than we have capacity for. Also good to work on documents. We could shed late reviews, on the basis that they are too late?

Lola: If we're going to ditch late reviews, we really need to be very specific and clear about what stage something shoudl be coming to TAG. We decline things for being too early, and too late, and that's going to cause confusion.

Jeffrey: It will cause issues for the Chromium process if we don't want to do late reviews. If we remove ourselves from it, we will have less influence, and far fewer reviews. The process requires TAG feedback when something is about to ship. We also get early reviews, but most are what we call late reviews. I think we can still have an effect if one browser has shipped them and we can affect the way other browsers think about it. This can encourage changes.

Hadley: So we need to define what's too late and too early, to Lola's point?

Jeffrey: When it's early we may have _something_ to say. I would not want to decllne on the basis of being too early.

Christian: huge +1. Installlable Web Apps we talked about the other day. Some are 10 years late. Agree earlier ones useful, but let's not ditch late ones.

Yu Sen: What factors do we consider when accepting or rejecting potentially breaking changes? (e.g. the 3pc work)

Hadley: In general early reviews are good, but there are some things I think are too early: cases when someone is new and submits something to the TAG before discussing with their colleagues. Another cases is when we get requests from the Chrome team for what are UA features. That's more out of scope than too early. Want to be able to say thanks but we can't help you right now.

Jeffrey: For Chrome we can ask people if they have a spec mentor, which is someone with experience who can sheppard things. Yes, if it's a browser feature we should decline it for that reason.

Yves: Early reviews and late reviews are way different. Early is about advice to help the work progress, and late is about checking that there is nothing major wrong. If the early review is done, the cost of the late review is minimal. Late reviews is part of W3C HR process - the reviews that they are coing through during CR time. We could decline more of those, as there are others doing those (particularly security and privacy). If we see there is no issue, we may decline and spend less time on those, but we shouldn't drop them completely.

Matthew: Horizontal reviews are inherently too late. The Team is aware and working on that. If it's about ready to ship, also, we can't have that much of an influence.

Xiaocheng: We should add the question about how to address breaking changes to the list. We should probably update the design principles, regarding deprecation. Referencing Chrome process, we could say that 'intent to prototype' marks the boundary between too early, and not too early. Getting to 'intent to prototype' means the feature has gone through some rounds of disucssion and shape has been fairly fixed, so we have something fixed to reiew.

Brian: +1 to Yes and Matthew. W3C process is the thing that is too late in wide review, in all the places. It's unfortunate and I think that's the thing we need to help fix as much as possible. TAG isn't in charge of process, but we can give feedback into the system as to our concerns. As Yves was saying, early review and later review are different things. I would love to be able to speedrun early reviews - I don't expect them to have all the answers to all of the questions. Eg. Adopted Stylsesheets explainer.. This is complex for an early design review. I would like to see something more terse. How do people feel about having an 'elevator pitch' explainer to get a picture of the thing, and maybe you can expand details on the finer points.

Hadley: Building on what Brian said, do we want a different approach for early and late reviews. We do have different templates with slightly different questions, but the Explainer Explainer is still the same. Should we have a different explainer template for early and late?

Jeffrey: A late review comes with a spec, but an early review is just an explainer. By the time it's late and they have a spec, the spec should be enough.

Brian: Specs don't contain alternatives considered. I want to get it before it's shipped in Chromium.

Jeffrey: We talked about how explainer content lives on after the spec exists, and how it (except for alternatives considered) could move into the spec. We are also talking about ____ which is how people can record the alternatives considered whils the spec is developed. Eplainer alternatives considered sections tend to be too short. We could even require sas part of W3C process that specs come with a directory of alternatives considered throughout its lifetime. That shouldn't get lost.

Hadley: The initial catalyst for explainers was to pull out the key things from specs that exist (not for early reviews, as we did less of them).

Jeffrey: We are focusing here on design reviews, not documents - how do we decide when we're done on these? We have a principle for breaking changes, but may want to do more.

Matthew: Can follow up separately on the above discussion on explainers and review stages.

Lola: Marcos mentioned in the chat: 2 people per review.

Marcos: Assigning people with expertise can miss opportunities to have a wider perspective..

Jeffrey Hadley: +1 (we try to assign 2 people)

Brian: It should be documented what an early review is and isn't. There's a desire to think that you've got other people on board with you. We see people presenting WICG work as being W3C work. It's really an incubation. They also say 'this got a positive TAG review' but this is an early review.

Hadley: Sometimes us saying 'we don't see a problem' is interpreted as 'this is great'

Jeffrey: We could have boilerplate in early reviews to say that we have validated it, but it doesn't necessarily mean endorsement.

... If we think all 3 engines have shipped something that's bad, we can still comment on it.

... If it's shipped in one engine, it's not too late, becuase we can still affect what the platform does.

Hadley: Yes, and I agree what you say if we're talking about browser features. There are some groups like TTML, VC, ..., who do their own thing for a few years and ask us to look, and it's a massive set of specs that can take years to wrap your head around how all the pieces fit together. Having sat in some sessions at TPAC, the negotiations are very detailed, and compromise occurs that seems to result in nobody being happy - but that is genuinely too late, they're not going to start over at that point. So our review goes nowhere. I would love to avoid that point of frustration.

Jeffrey: A lot of times we should trust WGs to know their domain. But it's possible that a WG has gone off in the wrong direction for a couple of years, and we are able to notice. It might be frustrating, but it's important that we have that opportunity. I would like us not to close off that opportunity.

Hadley: Could we have some guidelines around this?

Yves: We have the opportunity to file issues in the other group's repo, labelled with 'TAG needs resolution' which will block TR changes.

Brian: But it doesn't change a lot in terms of real-world things.

Yves: Agree.

Jeffrey: The guideline should be that we trust domain experts, and the longer it goes on, we can trust they found most of the problems, but we need to recognise that sometimes we can spot things.

Hadley: With e.g. TTML they are experts and we can be confident in their work - we did once ask them to talk with CSS more about some things that were related, and they did, and our part was finished. General concern that we need to be alert to any architectural implications, but in some cases/projects, our feedback may be too late.

Heather: You can trust experts to know their stuff, but e.g. browser and identity people were in different domains, and sometimes, the spec authors are not the implementers. TAG can help connect people across these pages.

Lola: +1 to Hadley and Heather; CSS Carousels is another example where domain experts created something that was generally frowned upon. Also the size of late reviews - there's a differece between reviewing scroll-tiggered animations which is fairly contained, and something like carousesls, which was so big we had to split it into 4 other issues, and was a late review. Should we have some guidance on this?

Jeffrey: Sounds like consensus that we should continue to do late reviws. Maybe some documetaton on how/what.

Hadley: I would say we can't _not_ do late reviews - we do need to do some. They're not a fail state, but they're not as good as being able to see stuff early.

Xiaocheng: Is it fair to say we strongly discourage late reviews?

Yves: They're part of the process.

Hadley: We could take ourselves out?

Matthew: would prefer to change the process to make _all_ reviews earlier.

Yves, Hadley, Matthew: +1; need early input on _all_ horizontal issues.

### Documents

Hadley: We seem to be better at raising/resolving issues, and making PRs, than drafting things initially. One motivation behind Breakouts was to give people writing time, but we don't use them for that anymore. Is this a problem for the rest of you?

*group has consensus that it is a problem*

What can we do about that?

Heather: I like writing. One thing is that you could bring in new members that have writing skills. I anticipate being better at document writing than design reviews.

Lola: +1 to Heather's suggestion. I also like writing, though we still need to figure out how to make time for those who want to contribute to documents. I think many people do. +1 to Hadley's suggestion about making time. If a breakout could be dedicated to working on documents that'd be helpful.

Marcos: +1 to Lola. I write a lot and always try to get better. Appreciate Jeffrey and TAG members' feedback. It can be difficult to find people that have all the skills needed, we all have strengths and challenges - the division of labor within the TAG could shift in order to be more efficient with reviews.

Jeffrey: We still need to get design reviews done, even if we allocate breakouts to writing. We could find agreement on reviews online. We could agree to a protocol for this. Generally, people haven't been using our online channels for this. If people want to use breakout time for writing, we would need to do this.

Hadley: My time is dictated by my calendar. Most of my TAG time is either in breakouts or other time carved out of my calendar. Working on it. The scenario you described I feel would be challenging, as I would feel the need to be on call to Slack

... How we've looked at it in the past.. some sessions are on documents and some are on design reviews. In 2019 we started a cycle where every first week of the month was all on documents, and the next 3 weeks was on design reviews. We could re-use/adapt that approach if helpful?

Matthew: Acknowledging Hadley's point. Like the idea of being more asynchronous. Those of us who are suited to that, do it. It's good to get a broader perspective, so a little live discussion is helpful. Also want to find a way to work on documents. Is the proposal what Hadley said, where there's scheduled time to work on documents, in the breakout time. Is that on a call together or just calendared time.

Brian: Do whatever works for people.

Hadley: Would be unhelpful if it were time that people can skip.

Matthew: If it were "you can allocate time to do this", I might allocate different time. But if we do want to meet, and that makes sense if you're drafting with someone else, could do a 1:1 call. If it's just about writing, we should manage the scheduling ourselves. If we say a breakout is focused on a document, is that about writing it there, or talking about the grand scheme? E.g. next finding, agreeing on philosophy?

Hadley: Depends on personalities and ways of working. Before we had breakouts, we had 1 TAG meeting/week. That particular TAG found it challenging to carve out time beyond that 1 meeting. My personality needs time on the calendar. If we had 1 set time, everything else would squeeze out what I want to do. But if you're disciplined, I don't want to get in your way.

Matthew: Need to fix the expectations of new people. And need support from organizations to spend the time.

Xiaocheng: Like the idea of being more asynchronous, but not sure because the calendar helps with allocating time. If I'm going to work asynchronously, latency might be big. Is it possible to set priorities to agenda items? Some design reviews are simple and non-controversial enough that we don't need to bring it to breakouts. If all assignees think this is simple enough, they just resolve it.

Jeffrey: If all the assignees would thumbs-up a proposed resolution we'd do that, but it hasn't been happening.

Marcos: Breakouts are good for status updates and some discussion, which is good. But they are never long enough. We could try an 'office hours' thing - e.g. Christian and me have this, where we sit on the call together and work on things. We tend to get a lot done being in the same space with the microphones muted, and it seems to work quite nicely. At the same time, a ot of the reviews, for me to do a review can take multiple days. There are a lot of facets and things to consider. Some can be small, but any I've done so far has taken multiple days to work on. This was my 'working sessions' suggestion.

Hadley: There used to be a web site where you could log in and be assigned to a working buddy. There was a sense of accountability.

Marcos: 'shut up and write' sessions

Lola: All the ideas so far are ones I can get on board with, especially working sessions. What I want to caution against is saving all writing work or discussion of documents to these sessions. Let's say we do Hadley's suggestion of splitting months. I would still like to talk about writing during design review weeks, as often people who are not editors could have contributions.

Matthew: Echoing Brian, we're not just writing stuff, we're writing for a reason. When will we discuss current affairs and our aspirations into a plan?

Heather: Sympathetic to being driven by my calendar, though not for writing, for me. So those sorts of sessions would be challenging for me. For writing I am more driven by to-do list.

Hadley: Another proposal: If we can come up with categories of kinds of meetings we want, then we can schedule them:

* Discussions on what we should write

* Writing sessions

* Reviewing issues etc.

Can we find a pattern for these sorts of meetings across the month? Is that helpful, or is it better to do it ad hoc? I'm all for being fluid, but we do need to write agendas, at least a few days in advance. I'm looking for a way to have that settled enough such that everyone who needs a plan has a plan.

Christian: ACK and +1 to everything and all of you. The working sessions are good for me, but I can understand how they may not be for everyone, so maybe they can be optional scheduled blocks? Additional to breakout times - but then there are TZ issues, and time pressures. As Marcos said, it helps even if it's just 45min a week.

Jeffrey: I like Hadley's list of kinds of work we need to get done. Despite that I've been pushing us to work more on documents, we still have design reviews, whcih don't go well if we take several weeks off and have to iterative with the proponents. So we need to make sure we do each thing on the right cadence. I like the idea of saying 'this week's meetings have agenda time for doing this purpose' with the larger documents. Not sure how we'll agenda this in practice - thinking about how we write the agenda (requires all state in my head - to pick the design reviews that need iteration this week - maybe we could figure it out).

Matthew: If work sessions are 1:1, the timetabling gets exponentially easier.

Jeffrey: Picking the 2 peole who need to schedule - not sure the chairs can do this - it's going to be more participatory.

Hadley: We could say in the previous week's meetings: Editors of the documents: what do you need to accomplish? Then it's up to you as the editor as to whether you want a working session, schedule it, or use breakout time, or what the chairs need to do in order to support it. Depends on what's appropriate for a document.

Jeffrey: This also means we need a larger fraction of the group to be editors. E.g. if only half of the group is editors, half doesn't have anything to do.

Hadley: and/or the editors seek review and contributions from others. I would be thrilled to have time to catch up on what everyone else is doing.

Jeffrey: I'm hearing every couple of weeks we say 'this is a week for documents' like the TAG of a couple of years ago used to do. 1 week on documents, 2 on design reviews. Once we have PRs to review, I think the breakout session works well for reviewing them.

Hadley: +1

Hadley: Interesting for chairs - one will be 'the document chair' - could be interesting.

*consensus on giving this a go?*

Hadley: When TAG doesn't have consensus I think we should be stating the different opinions that exist, as those differing perspectives could help the proponents. Thsi would be more helpful than us saying nothing.

*there seems to be consensus on this :-)*

[During break] Christian: What is consensus?
https://www.mnot.net/blog/2024/05/24/consensus
https://www.w3.org/policies/process/#consensus-building

## Next F2F

Heather: Second half of September would be good. I'm Booked from mid-October

TPAC: Oct 26 – 30 in Dublin

Hadley: at TPAC we typically book-end the week with TAG plans and debrief, but we don't actually meet as TAG outside of that.

Yves: We used to have 4 meetings per year. When COVID happened we moved to remote, but it doesn't work that well becuase people are distributed, and it's hard for people to be present. Depending on the amount of work we do, we may revert back.

Brian: Web Engines Hackfest event in Spain , June second week 15017

Lola: I don't think we should have 4 meetings this year - any meetings we have should be later in the year, Sept/Oct would be reaonsable.

Christian: After TPAC maybe?

Jeffrey: Late September is the right time, otherwise we have two meetings very close. +1 Lola that 4 meetings a yaer is a lot of travel.

Christian: Sept 7?

Matthew: 2 meetings + TPAC?

Hadley:  we could also have a virtual f2f where we clear our calendars?

Heather: I would discount the timing as to whetehr we're too close to TPAC or not becase we would be having a very different meeting at TPAC (not meeting, but co-ordinating). For June if we do a virtual f2f, I like the idea of a variety of breakouts which we can manage. I free up June ??

Hadley: For virtual f2f, in the past, we've done I would suggest 3 blocks of sessions around the clock, and each person attends two of them. With big breaks in between.

Lola: Why are we discussing additional meetings? Were the 2 last year insuffiicient? Is the virtual one necessary?

Matthew: Could do the first 2 weeks of Sept, but not the later 2.

Hadley: To Lola's question: I feel mildly that it helps us get a substantial amount of work done, spend time together, build trust. I feel like waiting until September is a long time.

Heather: Sept 1-3 is [Global Digital Collaboration](https://globaldigitalcollaboration.org/). Fine with Sept 7.

Brian: I think what we did in this meeting is valuable, but if we did it virtual I suggest we use it to process the work queue - more like our normal meetings.

Marcos: Can offer the Apple Vancouver office.

Tentatively Apple Vancouver, Sept 7-10.

## Associates

Luke Warlow, Ehsan Toreini, Dan Clark approved as TAG associates.

More to be nominated later in the year.

## ABCDE CG

Matthew: We resolved to change the name. Changed the charter name. Have an issue to rename repository and update readme. Once that's done, we can open it.

Jeffrey: Need to pick 2 chairs.

Matthew: Also fix the "if TAG doesn't update chairs" On Jeffrey's plate.

Lola: How frequently would the group meet?

Jeffrey: The intent from the charter is not necessarily to meet, but to do reviews, and report them on the mailing list.

Hadley: I have concerns about this, though I had on the associates program too, and that worked out very well. Biggest one is how to integrate these reviews into the TAG process - adding a lot of additional people and differing opinion management that we need to do.

Brian: A lot of this stuff will be reviewed already by HTML and WHATNOT - those are open meetings now. I wonder if these should be a somehow unified effort.

Heather: I know little about this group, and am chairing several groups, so have reached capacity, but one of the thigns that came up earlier today in workmode was about ensuring we have sufficient perspective. I wonder if this would be a pool of people for when we don't have the necessary experience in TAG. This could be a group we could pull from to get help, but not necessarily say that every review goes their first.

Hadley: that's part of why I'm not really putting a lot of weight behind my concerns, as it could work out.

Jeffrey: Suggest we pause discussion on this until we have someone willing to chair.

Matthew: Proposed charter designed to take some of the load off of the TAG. We need to do lots of reviews; we don't always have the expertise. We keep Associates, but we need more people to help with reviews. There's the IETF system with a pool of experts, who do 1-2 reviews/year. Will broaden our perspective. On an individual review, there will only be 1 person.

Lola: With that in mind, I can probably chair, with the expectation that we would not be meeting but when we identify we need some extra expertise it can be managed via email.

Jeffrey: I think that may introduce too much latency. My vision for this group would be that the chairs monitor incoming TAG design reviews and parcel them out as soon as they come in, with the hope and expectation that having extra eyes on it will always be good.

Lola: That means we'd need to know the expertise of everyone in the group.

Jeffrey: This means we need to ask people for their area of expertise when they join.

Heather: With security reviews for IETF, the reviews just cycle through the experts on the list.

Xiaocheng: What do we expect from this group? What would a participant expect from the group? If we just want to offload the design reviews, this feels like an associate

Matthew: Associates is quite heavy, and we expect them to be involved with a lot. Takes a lot of management from our side. Great if we want a long-term relationship. But maybe other people don't have time on a weekly basis. Expertise on an ad-hoc basis. They might enjoy the reviews. Helping as experts. But low time commitment. Keeping Associates, but this is more focused on helping us with a review. Not more than 1/month, or 1-2/year.

Xiaocheng: Not optimistic when the time commitment is too low.

Matthew: Not getting rid of Associates.

Hadley: If we put every review out to a group, we say everyone in the group, we want you to look at this, we don't get to control who's in the CG and this gives us a lot more to deal with in terms of starting and managing reviews. This makes it easier for troublemakers to have an effect. We have worked hard with associates to respect each other and our areas of expertise and to listen to each other. I don't know how to keep that going with a group of people we don't know. The other thing that concerns me is that the people we know who are really god on architectural stuff, or experts who _could_ be good be architecturally are overload.

Matthew: My understanding is that we don't show the incoming reviews to everyone. The chair picks the one person they think is best suited to the review. Process in the charter says the group doesn't do work unless it's assigned by the chair. If there's a troublemaker, you don't assign them reviews.

Xiaocheng: What if they volunteer and are the only one?

Matthew: The chair asks someone. Group is there to declare their expertise.

Jeffrey: *cites part of the charter relating to this*

Brian: I don't think we need a CG for this. TAG can tap people. This has happened before. There's no need for a CG for this if that's the design. I think there's a risk that you get to rubber stamping. There are not so many people who are super active, and when they are, we say 'maybe you should be a TAG associate'. People who are active are also going to be bringing work.

Christian: +1 to Xioacheng and Brian. I think it's a good idea, but if nobody wants to chair it, and if we have a parallel infrastructure with associates and can just loop people in then I would also suggest it be tabled. We can bring it back. I don't feel like there's much support for it at the moment.

Lola: I am hearing two different purposes for this group in this conversation: ease the load of TAG reviews becuase it's too much, and the other is get specific expertise for specific reviews. To Brian's point, if we need specific expertise we can speak to indivisuals directly; if we want to ease our load, then the group makes more sense. if there's already a list, people can't volunteer, the chair is in control of who's assigned to what, then we need to keep track of who's got expertise in what, but we are tapping you because we are overloaded with reviews, and in that sense I'm not worried about bad faith actors or people lacking experience, becuase the chair has the power.

Matthew: This is very helpful input. I very strongly feel that we should have a goal of being as transparent as possible. I agree with Brian that there's a hardcore bunch that moves things forward the most. It would be healthier if we had a more open participation system for that. If someone turns up they might become part of the community that moves things forward. At the dev meetup, there are people there who might sign up. This is worth trying, to both lighten the load. Bring people into the community, get expertise. Don't think we _have_ to do this, but it might be beneficial. Idea for workload is to have chairs assign someone to every review. We don't have to think about who to tap, we just assign things. I also love the Associates program, and different people suit different ones. We've seen this work well in other contexts. Maybe it helps along the lines to improve diversity.

Hadley: I'm on board with these goals. I'm concerned that the more we farm out the work, the less it's a TAG review, and we end up with another horizontal review. I think we should give our iews or clearly decline that we are not going to give our views.

Jeffrey: My impression was that we get someone from this group to write a review, which is something we can read when we write our review. This group's reviews are not TAG reviews. This group can take some/all/none of the CG review into account when writing the TAG review.

... Can we get to consensus one way or the other? It was sounding like we had several people with concenrs about this, so should we pause it and discuss it later. On the other hand if people are enthusiastic, we can create a CG without the TAG deciding to do it. Could be awkward if the TAG doesn't want to pick chairs.

Lola: I'm happy to chair and run this as an experiment. At the moment if it's only 3-5 reviews per week that's not a lot of work.

Xiaocheng: I'm still concerned with how this group is supposed to work. Sounds like they are participating but they don't get to decide what they work on. Sounds like a CG that's totally controlled by the TAG with zero autonomy, which doesn't seem right to me. I think this sort of working mode could be discouraging to the participants. Can we alllow open application of associates? I like the idea of involving more people in the desgin reviews process. I think what we need is more associates.

Yves: If we have a CG which is public, it would be good to not restrict it to TAG reviews, but most horizontals. So discussing with other horiztonals before doing it would be good. There are issues with other horizontals, so if this helps, it could help those. Would this, like IETF, be targetted more at late reviews?

Yu Sen: I'm not sure what the difference is between this and associates program. Sounds like more people, and less formal. Do we want to expand or change the associates program?

Jeffrey: When we discussed this previous times there were worries about making the associates program more open because we invite associates to all of our meetings. If we have people that we don't know coming to all of our meetings, it could dramatically change the way the TAG works - we know and work with each other well. Trying to figure out the next steps...

* Suggestion to talk to the other horizontal review groups to see if they would make amendments. I have heard interest in getting the other HR groups to participate.

  Yves: would need to make charter more visible, and be very clear it's a proposal.

Jeffrey: I hear Lola enthusiastic to chair. We can see how enthusiastic people are about joining without control over the group. If people don't join up, there is no harm.

Hadley: I have a number of concerns, but I'm happy to be proven wrong; appreciate the chance to share my concerns.

Marcos: +1 to what Hadley said, but I was quite sold on Martin's arguments for trying it out. Happy to see where it goes.

Jeffrey: It feels like people are leaning back towards trying it as an experiment.

Brian: Can I propose that we table this for this f2f and to choose to not decide today? I have worries that if half or more of the TAG isn't really sure what it is, nobody else is going to be sure what it is, and I think that's a problem? Bring it back at the next plenary. TAG members should think about it and about how to improve or clarify it.

Matthew: I like Brian's suggestion. PRs welcome. Next plenary gives us time to put PRs across. Silence is not objecting.

Hadley: On chairing, it would good to have 2 people. [Matthew is willing]

Matthew: Should we be concerned about getting fewer reviews?

*group considers that it comes in waves*

Heather: If it doesn't have 'AI' in it, it doesn't seem to be happening. AI seems to be being looked at as a discrete, not web-focused, technology.

Jeffrey: There's WebMCP and agentic things (a lot is browser features) but that hasn't been sent to us yet.

Brian: Did we get a review of toolbar?

## Retrospective

Jeffrey: At the beginning of the week there was a request that we be concsious of talking over women and I wanted to know how we did

Lola: I felt like it was much better than when I was hong kong.  I felt pretty good and listened to.

Hadley: Yes, I did as well.

Heather: I didn't notice anything untoward.

### What went well?


* I really liked starting at 9:30...

* I think the new structure to go another day, and have less pressure on one day is better - it's helpful to be in the right state of mind in the meeting.

* I felt comfortable in figuring out how I was going to fit

* I liked the focus areas and how we focused on more high level things. I liked that more that trying to work through a list of design reviews. I liked the focus on documents and talking about the other thingshappening in W3C and so on

* "Big picture" is how my brain works - and despite jet lag I was able to engage.  I also appreciated being fed :)

* I feel like we got some important work started, that is satisfying and given the good start, I think it will continue

* I also liked taking a break from design reviews.  I hope we are going to have a new photo on the tag page

* I liked the planning for this better - there was an effort to build the schedule before hand that was helpful.

* I liked our AI session - we pulled on a lot of things that were bouncing around in my head in a vague way, into a nice place where we can all discuss them and move towards doing something about them

* In the past we did a lot of breakouts and doing design reviews - it's "fixed" somehow... we have more work power with the associates maybe.  It allowed us to focus more on bigger topics where the fact that we are all together helps us make more progress.

* Minuting was excellent

* I appreciated contributions of asking us to explain where things seemed obvious to the people who were talking about it - it helps us think through and see where we need to clairify.

* I have recieved many ideas here, when I particpated many times before I assumed that we would do much more detailed design review - but since I saw the topics it is much more high level and principles.  This is very different from my company where I am a developer. This is very useful for me to understand the whole W3C community.

* I like that we did broad overall strategy questions - i think it will lead to more informed detail work in the future.

* I always find the f2f time rewarding and valuable - and too short.

* I feel much more like we are a team now, and I like that. I feel confident about our abilities to work through issues together.

* I liked that we did a developer meet-up. I've organised them in the past, and it helps make this group more grounded, and more relevant. I'd like to see us do more outreach, communication with developers, efforts to connect and understand what developers are trying to do and getting frustrated, and to communicate things that are important but not easily understood.

* Thanks to Matthew for putting together the developer meetup - it was stressful for you, but you did an amazing job.

* It was interesting learning about different people's styles of working to the extent that I can understand "this person is going to be incredibly helpful for me to work with"

* Our work will be important  towards helping companies to decide what to do with AI and what not to do.

* I liked that we were able to work out the mechanics of the week together, to adjust to what people needed and not being caught in a very strict "this is the way it is done".

* I also think that the outreach and the developer meetup are very useful and important - the findings especially are useful. It is also helpful and useful to the W3C.

* I like the social time with people

* I felt it was very nice to meet people in my first f2f. I think it went very well especially given all of our differences. Thank you all.

* I like that we agreed to say that it's okay that we don't agree.

## What can we do better at our next f2f

* I think we could do better at managing the goals of the topic - things wandered a bit. It might be something that chairs can help with - the chairs could have checked in with people managing a topic to make sure it styed more on track.

* control the pace of subtopics next time.. We have a lot of subtopics but then we spend too much time on the first one.

* I'm not sure how to organize these complex conversations - we need to figure everything out, but any one of these topics could easily occupy the whole week.  We need to find ways to make progress on them

* We need to try to encourage the most salient points ...  Some groups are very good at managing time.... We talked about this last night, it's on everyone equally, but I think we just need to make sure everyone is included in plans outside the room as well.

* I wonder if we have missed an opportunity to publish something... in the past f2f's seem to be a moment of momentum where we sometimes have published, but I don't see anything on the agenda I would have dropped.

* Slightly sad about the fact that we didn't manage to get more finding material perhaps as well, but we did a lot including onboarding new TAG members.

* I would like to see us make progress. Lots of the talk is good, but it should go somewhere eventually. One thing we could do better, maybe, — at [day job] we have long meetings like this with lots of decisions, we encourage people to record and provide presentations a week in advance. So you can take your time, consume a talk, maybe one at a time rather than eight in one day. And then when you come, you are prepared, we don't have the presentation, we go straight to the discussion, and everyone is ready, well primed.

* Communicate better about plans outside of specific TAG meeting.

* See all the information from others before the meeting. Maybe it is more efficient. Maybe take five minutes after the presentation to think about it, and then discuss.

* We can have more actionable items as the outcome.  This week we have discussed a lot but not produced much action items.

* I don't like the way that queueing causes the conversation to go.  I don't know a better way to do it either.  I would like to find some way to do it better.  My interpretation of 2 suggestions ago ("see all the information from others") was sort of we go through the slides and then we write questions down together and can see them and then we discuss...

* We didn't do the hard work, produce results in the form of design review comments or documents or findings. However, based on the conversations we had, I think this is ok. It would be good if we focused on a particular thing a our next face-to-face. But with our new members, this was helpful.

* We do not vote. It has disadvantages, becasue you're bound by it. but it has advantages.

* Queueing — we could do two hands up, to reply to the immediate topic.

* We did not use IRC for queueing (it would allow the "two hands up" approach)

* I've been thinking about the queueing thing too - it felt like there was a lot of branching and it made it somewhat harder to follow.

* I don't want us to stifle conversation and working together with our method of queueing or managing the conversation.

* I want us to do things, to communicate more, but also appreciate that we took up some of these high-level comments.

* I agree with the comment about branching conversations.

* I like that we agreed to say that it's okay that we don't agree. Is there value in publishing things that aren't findings, like "we had a face-to-face and this is what we did. And there are things we didn't agree on, and that's ok"? A blog post?

* in past f2f's we've discussed things in retrospectives. I don't know that anything from hong kong retrospective, we have actually done anything with that.  If you present something, assume you are in charge of taking that forward.  It's not just the chairs, we have to think about these things and look foward to improving them for Vancouver. If there were discussions, review the notes of your topic - see if there are action items and help move them forward.  For the chairs it is to review this list in preparing for the next face-to-face.

* Another group that I am involved with meets twice a year and they are very different meetings, they alternate... One is big picture and the other is specific.  I definitely needed this big picture meeting, I would think the first one people come into you make bigger picture - maybe one meeting a year.

* Sharing context in writing early would help non-native English speakers

* I think we need to figure out how to integrate the skills that are outside what I will say the common skills - and help lean on their strengths. I feel like we missed some opportunities there.

* We know the election cadence so the big picture as the main topic of one makes a lot of sense, but we can incorporate things as they are necessary.

* I'm going to the bar.

Action: Heather to do a first draft of a blog post covering this face-to-face for the W3C Blog.



## 3PC/FedCM

Slides: https://docs.google.com/presentation/d/17NuqH2DD2bICbD1N1S9D6EeaE4sWKIPybSF6lUkfNZQ/edit?usp=sharing

[ Slide 2 ]

Heather: We coud talk about 3pc, and FedCM (either in relation to 3pc or on its own). FedCM could take away a reason for 3pc - recommend using the link on the 2nd slide to find out. https://github.com/fedidcg/use-case-library/wiki/Primitives-by-Use-Case

[ Slide 3 ]

TPAC 2024: Mozilla & Apple pointed out the experience on the web is now fragmented.

[ Slide 4 ]

Heather: Started at Internet Identity Workshop in CA in 2021. Has gone through a couple of name changes.

Education (SAML) technically doesn't require 3pc but partners use 3pc. Advice in that setting is to not use Safari.

Mozilla felt like it was becoming a Chrome browser feature, and so they stopped working on it.

Google continued to work on this as broadly useful for identity on the web, and I think there's a lot to be said about that. I have some personal concerns that it's too broadly useful...

[ Slide 5 ]

Heather: Broken out into ~15-20 APIs. Many get early TAG review. This is huge. They are following, more or less, TC39 stages.

[ Slide 6 ]

It's a browser API. So who's taking advantage of it when it's there?

Shopify is definitely one. There are others. The others are largely treating it as a produc offered by Google - so discussion is happening in Google lists etc. They are not discussing it as a standard. I have expressed concerns to the editors, as chair, I do not know what's being worked on. The editors say they're busy.

The AT protocol people find that there are pieces of this that are relevant. Particularly identity registration.

[ Slide 7 ]

As TAG member I'm interested in the first two; as a WG member and chair I'm interested in the third.

Lola: This is a different question... is it likely that 3pc could still fall out of use even though Google's not getting rid of them becuase of the position of the other two engines, and because of FedCM.

Heather. There is an aspect of that. The other thing to remember is there are many sites that say 'just use Chrome' - you don't _have_ to implement FedCM but as there are 3pc there are other ways to do things there.

Hadley: If Chrome are driving the work, who else is in the working group or community group, and are they having an impact?

Heather: Emily Lauber from Microsoft recently became editor. But the implementations are Chromium-based, so not sure that counts. I have thoughts on what makes a successful standard. Have chatted with people that are not participating because Google has a code-first design focus. This can be good but also is discriminatory. Microsoft feels that.

... We are seeing Microsoft and the AT Proto people getting involved. Education has been trying to understand this from the beginning. But for something as broadly impactful as it could be, we have about 250-300 on the CG and about 15 show up to calls.

Brian: I wanted to ask about general involvement, but also, even if it's Chromium, that is a big community of downstream browsers. Microsoft, Samsung, Opera, Vivaldi, Brave, Meta. Some of these are pre-installed on OSes. Is there even consensus among the Chromium downstream that this is what we want to do?

Heather: I don't think we've asked that question that way. Microsoft has concrens, but after engaging for a while, they've decided to engage with this via Emily being an editor. Brave - there were concerns about federated tech in general. There was an FO about DC, but in general there are concerns about federation.

Brian: Vivaldi, Opera, not involved?

Heather: no

Jeffrey: The future involves 1 engine with 3pc and 2 engines without - that's an issue for the web. We should have an opinion about it that is more than just 'Chrome is wrong' as that's not going to have an effect.

Heather: I agree.

Matthew: I believe there was some discussion around a more lightweight appraoch to fedcm, which did use 3pc but also something like CHiPS to make sure they were used responsibly. Easier to implement. What is the status of that?

Also, you mentioned about using it on browsers that were not chrome, and it reminded me that lots of browsers have heuristics we don't know bout, that could be as simple to "let everything (all third party cookies) through," or more clever to make sure things work, and we've talked in TAG about how it would be nice to bring this out, shed some light on it. Make it clearer.

Ladybird, because their focus is on impelmenting the standards, might help shed some light on this.

Heather: Lightweight FedCM, which we tried to transition into being FedCM core (what all browsers would impelment, and everything else woudl be extensions), was driven by Mozilla, and when they dropped, Google thought the scope should be all of it. So the concept of it fell away.

Brian: Xiaocheng, do you know what Servo is doing?

Xiaocheng: I don't know about that.

Yves: Organization could be: browser, ad company, hosting company. Some organizations are combinations of these. That leads to different attitudes to support and data collection.

... We've seen interim solutions being proposed to 3pc that have similar issues. 3pc hasn't even disappeared from engines that deprecated 3pc. I am wondering if, because of the pressure from that, what solution is needed. Are you aware of any other solutions to these issuess?

Heather: not aware of any

Hadley: I have a strong opinion that I expect doesn't reflect TAG consensus. I think the most important reason to get rid of 3pc is becuase of how they are used in tracking. So I don't think FedCM is enough, but it's a good start. I think there are other use cases that 3pc cover that FedCM doesn't cover, so the job isn't done.

... We have seen proposals for systems that replicate 3pc from people who are in the ad industry, but they have the same issues.

Yves: TAG produced a finding that 3pc are harmful, so we had consensus on that.

Hadley: We did - but we do have different people now.

Xiaocheng: Heather said Google dropped the concept of FedCM Core since Mozilla stepped away. I'm concerned about this and I think it's harmful behaviour and introduces a lot of obstacles to others who want to implement it. They don't care about the structure of the spec as long as they can implement it. I think we should avoid such things.

Ehsan: Following on from what Jeffrey said, about fragmentation in the future. If we change the UA to AI agent, does it mean AI agents in the future need to support cookies?

Hadley: I'm glad you brought that up, it's a horrifying question. It could easily go in a direction that is very bad for privacy.

Jeffrey: If you want FedCM core to exist, all you have to do is participate and maintain it.

Xiaocheng: What if those people who want it join much later after it's implemented in Chrome?

Jeffrey: It's a risk, but it's hard to justify working on a thing without someone to support it.

Xiaocheng: Servo has to keep up with so many features. It's hard to identify the core.

Jeffrey: Looking at the use cases on the FedCM wiki, most don't seem to need 3pc. It seems like Safari is getting on fine with dropping support for those use cases. Looks like paving the cowpath but not blocking 3pc removal.

Heather: I've been focusing on FedCM as a response to 3pc and that's where it started. It's not all of where it is right now. There's a new explainer on how FedCM will make agentic AI easier, when choosing accounts etc. It's drifted from that core purpose. They're moving in other ways. If you are trying to select which acount to use, does FedCM have a role? So it's gone from 'how do we make identity on the web work without 3pc' to this.

... I agree it's scary that we don't have FedCM Core. If Servo wants to come in, we have a document as to what we think should be in Core. We need someone to validate wheither this is _still_ the right thing.

Hadley: what is the AI agents use case?

Jeffrey: AI agents are part of the browser, so they need to know the semantics of what the page is doing. The agent is trying to fulfil the user's request... If I'm logging into a web page as an agent (I have some thoughts on the agent logging in as itself vs. agent logging in as user). The semantic action is accomplished by typing into a form and clicking submit, _or_ by clicking a button that links to Facebook or Google or something. The agent has to figure out what to click on the page in order to accomplish login. That's harder to do unless it's programmatically declared. So FedCM, especially with some annotations, allows them to work out how to log in.

Hadley: Helpful thanks

Heather: There's an explainer on this that came to the group about a month ago.

Jeffrey: Sam Goto has been talking to me about it. We are leaning towards adding some HTML elements that say 'here's a federated log-in button'.

Hadley: Sounds like, for as long as people are uisng the web, there's value in pursuing FedCM for humans and machines.

Jeffrey: I would like to make them the same thing.

Hadley: +1

Jeffrey: Exposing it to the browser is helpful for the human as it can say 'here are the accounts you used with this site' - though Mozilla and Safari don't seem to think that.

FedCM doesn't help with being logged in with two accounts.

Heather: Mozilla had started work.

Lola: Why has this not caused problems for Mozilla and WebKit

Matthew: They let some through

Jeffrey: that's not all of it

Heather: When people in education encounter this, they just use Chrome.

[break]

Matthew: The UI issues. Of course we don't tend to tell browsers what to do with UI, for good reasons. But the UI presented in chromium (the only one that supports it), is this thig that puts a pop up in the web page with your full name and email address. Way aroudn that is to have one browser profile and you can say "this is my work tab" and "this is my coding tab"

Jeffrey: it displays your name but the content can't see it. If it's using FedCM. But you also have third party cookies enabled, and the sign-in might be doing something else that's not FedCM as well.

Matthew: So one solution is to compartmentalise your tabs, but most people won't do that. The UI is difficult to get right, might be why no one else has done it.

Also, TAG has had discussions about this spectrum of proposals to replace third-party cookies, according to the use cases. FedCM is one, and you'd need different solutions for the other ones.

We said that high-level focused api approach is the right approach because we hadn't seen any low-level secure implementation of something to replace third-party cookies. But I like the idea of a high-level focused API.

Heather: I know the TAG published a Finding on 3pc being harmful (https://www.w3.org/2001/tag/doc/web-without-3p-cookies/) and you (Hadley) said what was the consensus then. How much does TAG relitigate previous decisions?

Hadley: Rarely, we often say 'we wrote this, go and take a look' but that shouldn't bind anyone who wasn't here when a Finding was done. I don't want to reopen everything (nor encourage people to try) but that's the overall situation.

Heather: Re what Matthew said about high-level API needed because the low-level one doesn't serve everyone's needs, I think that's great. You can build a house with bricks, but you can also throw the bricks through the window. 3pc is a brick. FedCM doens't solve the whole problem. If it can do the identity selection part, where the UI is useful, that is good.

Hadley: Re bricks, we have a design principle on this.

https://www.w3.org/TR/design-principles/#high-level-low-level

Please check it out and let us know if you think it needs changes.

Jeffrey: 2 questions here: 'FedCM?' and '3pc?' It sounds like we're generally agreed that FedCM is a good idea but there's a problem that it's only one engine. This is a situation we find ourselves in a reasonable amount. We could write something saying 'Hey Mozilla and Apple, please engage with this, because we think it looks nice' - not sure if that'd help.

... It sounds like FedCM doesn't address the problem of 3pc as other engines have abandoned enterprise users.

Heather: Chromium supports all users - if you use FedCM great; if you don't there's 3pc. The other browsers drew a line that says 'it may break, but that's because you designed your protocols wrong; fix OAuth and OpenID connect'

Jeffrey: is it _possible_ to fix those protocols and still serve the use cases?

Heather: I don't know. I know who I'd ask.

Jeffrey: MIght be good for us to ask those people.

Heather: Regarding could we bring Mozilla and Apple back into the fold... I think the agentic AI component might be very compelling to them in the same way that IDP registration was compelling to the AT Protocol people. Does that put those things in Core? Are they _only_ going to work on those components? Will they be willing to work on the other parts of FedCM that they don't like as much?

Jeffrey: That still sounds like a plan.

Heather: It's the only one we have.

Jeffrey: Seems like a reasonable route. Wanted to see a conlusion on the FedCM topic. Is that the conclusion? We want to get them back in, we think that agentic browsing might do that, let's proceed. Sound good?

Hadley: Yes. But I feel we're on shaky ground saying what people should do. We are on much more solid ground talking about the architecture of the web. We could say 'the web is fragmenting - we need to avoid sites that only work on one browser'. It's a short concept, but uisng our position to shine a light on it may help. Maybe Apple and Mozilla will jump back in, but it's not us telling them what to do.

Jeffrey: I like it.

Hadley: Who's going to write it?

*Group decides Heather and Jeffrey will work on it; Lola and Matthew to review*

Matthew: is there any other area where there is fragmentation? Our biggest concern is FedCM, but it's even less telling people what to do if there are other cases.

Yves: Sensors.

Xiaocheng: Can we work with the interop and baseline groups to push for interoperability?

Brian: Interop is an annual project, so it's done for this year. What happens in the submission is that me and somebody from Apple, Google, Microsoft, act as proxies to review those thigns, and see where we can get agreement.

Jeffrey: and there are silent vetoes

Brian: We need things that are in specs, further along, no objections. Could use this to get a webkit or mozilla position - is there one?

Heather: The definite reply is 'no objection' - this isn't helpful, as we don't know if it meets your needs, is it going in a direction you'd actually support?

Brian: There is a problem with the investment in the commons and maintenance of new features, and it's not really a useful standard until it becomes baseline, and is baked into the soil. When that happens, sometimes investing yourself in implementation is a way past that, because if the big barrier is just it not being on the priority list, having the resources to develop it, sometimes somebody else funding that work can help. Might be useful to look for a sponsor of that work.

Jeffrey: E.g. Shopify might be interested?

Hadley: Let's set a deadline for publication and work backwards...

... Something we've done in the past is write a Finding that is technical and as timeless as possible, and writing a 'blog post that goes alongside it to point out that this answers the current question.

Jeffrey: I don't think we should include sensors, as it's controversial (there are objections). I do think we should be clearer about telling people what to do.

Yves: Sensors was just one example of where there are missing implementations. There could be others.

Jeffrey: Yes, but I think we should concentrate on FedCM in this case.

Action: Jeffrey and Heather to bring a draft to the TAG by the next plenary, in two weeks.

### 3rd party cookies (3pc)

Jeffrey: We have the finding that is effectively criticising one browser.

... We are in a situation where we have some browsers with, and some without, 3pc. What should we do about this? We want to discourage fragmentation. Should we talk to regulators?

Lola: This week I learned that CHIPS might not be being developed as actively as I thought. It was paired with third party sets, was separated, and then we likedit. A lot of stuff that's come to use that's 3pc related is the low-level shared data API stuff where we've said that data should not be being shared acorss 3p boundaries in this way. We need to know what work is going on in this space. E.g. PAT. We need to know about everything that's happening around 3pc. We should ask Martin.

Brian: +1

Jeffrey: Maybe Ben VanderSloot

Matthew:  I don't know that we can unilaterally decide to talk to regulators.

Hadley: Agreed, we shouldn't do that. we can describe the situation as it is, with regulators in mind as an intended audience.

Matthew: ACK; like how we did with the Digital Credentials Finding

Jeffrey: CHIPS - seems to be the right way to do things in Chromium. Seems to be working for Safari users. Not sure, but Mozilla may be backing off becuase it isn't working for their users. CHIPS doesn't violate any of the boundaries we want to enforce.

Matthew: Re attribution: @@@FIXME: mentioned 2 parts to ARA, but taking off the realtime part, everyone's proposal is on the same page, and could potentially be sufficiently privacy preserving (realtime part is not).

Lola: Are the active 3pc replacements: FedCM, CHIPS, and Attribution?

Heather: And Storage Access

Jeffrey: And the Google proposal for top-level to opt out of 3p cookies for iframes.

Jeffrey: I think so (the other privacy sandbox APIs are designed to replace other 3pc uses, but they are not being developed). Storage Access is WebKit.

... We could encourage opting out of 3pc in iframes. If regulators required this (ban 3pc to transmit info in bad ways), and everyone opts out, then Chromium could turn it off.

... Previous complaints were that technical measures to replace 3pc impact small companies.

Brian: Just moving it out of cookies doesn't help anyone. This is why the law should be clear about what 'bad things' are. It would be nice to have increasing legislation that says what you can and can't do with user data.

Lola: Think some jurisdictions have regulation about what sharing is acceptable and not. GDPR to some extent. Not sure about elsewhere. CCPA, but that might be more about sale. Hear 2 things: Within W3C to corall browser vendors/spec authors to be more collaborative. 2) Toward regulators to advise about restricting use of 3p cookies in browsers, and being clear about why and defining what "bad things" is.

Yu Sen:  Android applications when targetSDKVersion is latest are required to comply with privacy policies and obtain user consent before accessing location, storage, and IMEI information. Governments have mandated this through executive orders for internet companies over the past few years. Perhaps some W3C user privacy standards could follow this.

Lola will draft a finding on this. Brian will help. Summarize the state of things in W3C, active work on these replacements of 3p cookies. We want to replace them because they have these impacts, and that's a good idea. Don't know when. There's a Government Digital Standards conference in 2 weeks. Hadley might be speaking.

Xiaocheng: What's the message we want to send? Is it "the usage of 3p cookies should be illegal."

Jeffrey: "Websites should not track with cookies" is not a sufficient message. Instead, we could say "websites should block 3pc from their iFrames except for very specific instances."

Lola: focus more on the impact to users rather than what we want regulators to do. Also, earlier you said, the tech we have to replace 3pc are not enough for the CMA. Why not, what's missing, and should we mention that?

Jeffrey: The reason they are not is that they don't replace the utility for advertising.

Matthew: We were talking about saying we shouldn't do these bad things with user data but we don't want to move bad things from cookies to something else. That's why we need the regulators; we don't want bad things regardless of mechanism. Things like GDPR and CCPA already say those things but they say them "without user consent" and so we have consent boxes. Given this is already regulated for, isn't that sufficient? Maybe not since it's not regulated everywhere.

Brian: There are use cases now using 3pc that if you don't support 3pc you're not fulfilling those use cases. Are they just because applications are making those choices or is there something fundamental about them?

Jeffrey: there may be some fundamental ones (e.g., comment widgets). There may be other use cases like that.

Brian: so, people keep designing things that use 3pc and not trying to move away from them?

Jeffrey: There are the FedCM use cases but not sure I want to commit past that use case. That said, there were no other big areas in the Privacy Sandbox.

Brian: If Apple and Mozilla are not serving those use cases, then what happens?

Jeffrey: You have to open those things (e.g., comment widgets) in a top-level domain.  There are ways around that with permission dialogues, but the user experience is bad. I would like to add to the finding that regulators can say it's illegal to track users with this data, but if a website has 50 clients, then it is hard to have the one cheating service providing. Allowing websites to opt-in to technical measures is therefore helpful.

Matthew: It's payments, isn't it? That's a use case where they have to use 3pc or it breaks?

Jeffrey: No. If they have 3pc they'll use them. They'll use any fingerprinting info they have. The "we'll text you a code to use with your bank" does not require 3pc.

Lola: the process you are describing is not common in other parts of the world. There is a process whereby you try to pay for something, you don't get a text, you get an iFrame that tells you to go to the bank for verification, but the countdown in the iFrame and in the bank are synced.

Yu Sen: For the wallet, the process for payment is that you go to a website and the server calls the payment server. to create order. and redirect to page providered by payment company to complete the verification and payment (the relevant callback information will be embedded in the URL query).

Matthew: I've spoken to various browser developers and they've said they have special, unique browser heuristics that allow 3pc without telling the user and regardless of the browsers "blocking" 3pc. Not sure if or how much that's universally true.

Ehsan: Is there any correlation that as 3pc were turned off, did other tracking (e.g., navigation-breaked tracking) go up?

Brian: Is the question whether when Apple turned of 3pc, were orgs able to track Apple users anyway?

Jeffrey: Not sure that data is being (publicly) tracked. Someone might have, but not sure where to find that. Some recollection that people saw fingerprinting and bounce tracking go up.

Matthew: Are we doing a finding?

Jeffrey: Yes, Lola and Brian are going to try and draft something to socialize at an upcoming conference in 2 weeks. No promises.
