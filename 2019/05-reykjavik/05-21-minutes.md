# W3C TAG face-to-face in Reykjavík
## Day 1

#### Present: Alice, Dan, David, Lukasz, Ken, Peter (remote), Hadley (remote), Tess, Sangwhan
#### Regrets: Yves (partial, n delayed by flights)

### Morning Session

* Scribe: Alice
* Fallback scribe: David

#### Agenda review

https://github.com/w3ctag/meetings/tree/gh-pages/2019/05-reykjavik

torgo: In the morning, we are going to work on a retrospective of how we work as the TAG.

#### Retrospective on how we work

torgo: We are falling behind on our commitment to our stakeholders WRT design reviews.

hober: What is our commitment exactly?

torgo: To get back to them in a timely fashion. We're having an increasing number of review requests to come in, and we don't have a gatekeeping function to ensure these review requests have sufficient information, so we are spending time on triage to try and get that information.

torgo: We need to be clearer about what our requirements are to save time for everybody.

torgo: We also don't have a process for failing reviews. We like to be nice, so we just leave review requests hanging indefinitely even in cases where the review no longer serves any purpose, or lacks a clear path forward.

torgo: We may want to use some tools like new labels... 

torgo: So we have a number of issues with how we are doing the design reviews, and that has sucked the oxygen out for any other work we need to do and it's making everybody unhappy.

torgo: Review requestors are unhappy because we're not responding in a timely manner, and others are unhappy because we are spending all our time on reviews.

torgo: I'm hoping to get to a point today where we have a chance to make all our stakeholders happy.

sangwhan: We're not fast enough to close issues.

kenneth: We spend a lot of time each week looking at the same issues.

torgo: Right, we definitely need to avoid these issues lingering on, we need a process to close issues.

hober: What is the relationship between design reviews and horizontal review of architectural concerns?

torgo: They should be the same.

torgo: We should have more documents like the security and privacy self check to allow review requesters to self-serve more standard feedback.

hober: Are we getting horizontal reviews at all? As a proportion of our incoming requests it's quite small.

sangwhan: TPAC is a good opportunity to encourage folks to make those types of requests.

Alice: I'm working to improve things on the Blink process.

david: I think there is value in the TAG review happening earlier than some of the other horizontal reviews. We need to talk about whether we want TAG review to be at a single point, or whether we want it to be spread out.

sangwhan: I thought the Blink process only required a TAG review later in the process?

Alice: TAG review *now* happens at two points in the blink process:  intent to implement and intent to ship. It used to be intent to ship only, and we're .

torgo: We need to put a stronger filter on when things are appropriate for TAG review. I'd like us to have a shared understanding of what the steps in the process are, and feed that back into a formal process which we can support with templates, labels, etc.

sangwhan: Alex and I chatted about this two years ago. One of the things we struggle with is the (in)consistency of reviews (sometimes about sync vs async, sometimes about privacy, etc.); it often depends on who is assigned to the issue.

sangwhan: We floated the idea of having a checklist for requestors to review before submitting.

hadley: Many of the self-check and principles documents are not really relevant to many of the reviews.

sangwhan: covers Javascript APIs well, not other areas, e.g., CSS

hober: we could improve that

Lukasz: We need more general advice on top of the specific e.g. security and privacy checklist

torgo: Yes, that's why I'd like to have a design principles checklist.

lukasz: THere will be some things we can't catch with a checklist.

torgo: Yes. It's a trade-off. We can provide deeplinks into the design principles doc.

sangwhan: We can have authors zip through the checklist, and escalate when things are unclear.

hober: There are two sources of inconsistency - we all have different backgrounds and areas of expertise so naturally we will each pick up on different things. Secondly, there's an inconsistency of input - the earlier a request comes in the less well-formed a request might be.

kenneth: ... explainers ...

sangwhan: An explainer should cover the "what are you even trying to do" question clearly.

*~ how many web standards experts does it take to flip a whiteboard ~*

torgo: We have several phases: 

1. Entry
2. Work
3. Feedback
4. Exit

torgo: Alice shared a recent Blink document which includes a flow diagram for these phases.

torgo: Portals was an example where there is an unclear outcome from the review. We can be more assertive.

hober: is open/closed tracking whether review is done?

torgo: Let's go through a simple example.

Dan: suppose we get an explainer, ... then we're not happy about security feedback and particular issue in design principles... then they open issues.  Issues at some point get closed.  They come back to us, say feedback incorporated, then we close issue.  Ideally a wrap-up discussion.

torgo: Ideally we close in the "thank you for flying TAG" state.

hober: To what extent is the open/closed state of the issue an internal flag about our to-do list, vs an external flag about whether they can expect more feedback?

torgo: both?

david: Do they need to be different?

hadley: One thing I'm stuck on is what happens when we fundamentally disagree with what they're doing? Alex would say we have no power, which is true, but...

hober: We need a way to say we think there is a fundamental problem here.

sangwhan: We need an "unhappy" closed status. We did this with EME.

hadley: EME is a great example.

sangwhan: github isn't great at this.

hober: we can use labels for this.

sangwhan: They can reopen if they want.

kenneth: It should be communicated clearly.

david: We don't have good communication mechanisms, e.g. triggering something to be put back on our agenda, so we spend a lot of time "polling". If we can find a way to fix the notification problem, there's to some degree less urgency to get issues closed because they can be dormant.

hober/sangwhan: so we need a way to mark issues dormant.

david: and a way to un-mark.

sangwhan: something may be pending external feedback, and then we poll it in the meeting.

david: a tool may be able to say "this issue is dormant until github issue over there is closed / has a comment on it". How much of our problem would that solve?

lukasz: Can we ask for more power?

hober: If that is a topic you're interested in, you can join the process community group.

sangwhan/torgo: We can absolutely be effective with the power that we have, though.

torgo: we need to get back on track with that. I don't know that the issues we have are at the right granularity. So what is the right granularity?  Seems like we're getting reviews for this tiny feature addition to an existing spec.

Alice: If we don't want to see those, we can ask not to see those.  But we're trying to get visibility; incremental changes add up.  Not easy to tell what's a small change.  Would be nice to have templates.

Kenneth: sometimes the small things do matter

hober: Alice raising good points that it's hard to distinguish a priori between which small changes need review.  Also, venue matters:  small change owned by a healthy active WG, I feel less of a need to see that.  Already external review, and engagement with other organizations.  In the case of WICG, it's usually just the people working on the thing that are looking on it; less preeexisting external feedback.

Dan: Example of disagreement within WICG that failed to use existing WICG escalation path.  Not clear if that escalation path is set up.

hober: ...

hadley: Seems like you're saying that much of our feedback would have been given in a normal working group process.

hadley: I think there's something fundamental about W3C -- supposed to be consensus-based building of the Web.  If we're the only ones providing review and consensus... then it's not consensus-based building of the web.

hober: To use Alice's example of CSS alt -- glad you brought it to us -- but I think the CSS working gruop's process could take care of it.

alice: The reason I didn't feel comfortable saying it had sufficient review... I went looking for reasoning behind design, and it wasn't minuted/documented.  Couldn't answer the question of why alternatives weren't chosen.  Should we trust the CSS WG?

hober: some aspect of "trust but verify"

alice: I was trying to find all the info the TAG might need.

Dan: Maybe put more process around what we already do?  If nobody in the TAG an expert, we sometimes pull in other experts.  When I sat down with Tara Whalen, I said I'd encourage members of PING to weigh in when privacy is relevant.

hober: We ask every single review coming in to do the S&P questionnaire, it owuld be great if they had the bandwidth to review every request!

torgo: We may need to include in our template, what existing WG could do a first pass on this review? PING would be an example.

hober: There are a few flavours of this. One is that there is an existing group that this is in scope for. Sometimes people come to us first. Sometimes people come to us afterwards (sometimes if they don't like what the group wants).  Or useful to know that we're being asked to review something that's already consensus of CSS WG. 

hober: There is analogy - in the US the supreme court can defer to the local court.

hober: We don't have CSS design principles, but isn't that the CSSWG's responsibility? One part of our responsibility is architectural concerns, and I think that is used as a grab bag for all design concerns. We have i18n, a11y etc.  Is architecture a specific piece or is it everything? Then we have horizontal review... are we coordinating all horizontal review?

torgo: I am concerned about trying to narrow the scope to only "architectural" concerns. My idea of architecture is the communication between two systems... anything that come through the w3c has a potentia architectural concern.

hober: Privacy is a concern of PING, and they should share/own the responsibility.

torgo: The S&P self-check is co-authored between TAG and PING. I'd like to extend that model.

hober: If the checklist is a fast-fail mechanism, then you need to do your other horizontal review before coming to the TAG.

Dan: no... 

Dan: Alice, you wanted to bring up points about Blink.

Alice: most useful thing is clear guidance.  Problem we're having:  many people new to standards want to do things.  They don't have clear guidelines for how.  So first thing they might see is "ask for TAG review", without much guidance on what that means.  Trying to fix things on Blink side.  But we could also have guidance.

Hadley: Also goes back to that it' not clear what we're looking for -- if we're looking at everything, hard for engineer to know what to tell us.

Dan: Can we provide stricter guidance about input to TAG review?

hober: Overall I think Blink process that resuts in these reviews is good.  What's good about it is that it requires external review.  That's distinct from TAG review.  We're currently the sole target venue of this process; I think one piece of feedback we *could* give Blink is asking them to have multiple targets for that instead of just us.  Maybe CSS feature should go to CSS WG.

Alice: and us afterwards??

hober: not sure.

hober: Primary benefit of this process is that features are getting external feedback.  Not picking about who gives it -- needs to be a diverse selection of experts.  We're maybe not the best group to provide that in many cases.  We have a particular set of expertise.  Other groups exist that may be better suited.

hober: If we still get a design review filed on us we should do it, but if a preexisting group of experts exist and doesn't appear to be consulted, we should ask them to take it there, and come back to us if unsatisfied.

Dan: guidance: maybe request from WG, or maybe request TAG review, but if requesting a TAG review you should try to ping the members of the eexstiing community to get them to pay attention to and comment on that review.

lukasz: I used to do  privacy reviews prior to being on the TAG too.  At some point Dan asked me to look at something (while I was not at the TAG). You want to streamline requesting other groups or people to do it -- not just a group, but actual people even if external.  Sometimes security and privacy stuff is a bit contextual, sometimes very narrow/specific.  We had a discussion, I think at the occassion of TAG review of priority hints (?) talking about different types of fingerprinting (detection of feature; detection of encrypted traffic). That was not immediately evident to the requesters and until today I don't know if this is the case...

Dan: Do you agree we should get external folks to comment?

lukasz: yes... do we want to give them some sort of deadline?

Torgo: Well, they're not accountable to us

hober: In the case where a feature in CSS that hasn't gone to CSS WG -- we should ask to raise with CSS WG and close our issue -- just say come back if you still need help from us.

Alice: Back to to-do list question -- maybe our issue list might be something that's not just for us but an issue list for other grousp.

Dan: github can let you migrate an issue to another group's issue tracker.

hober: groups where it's in scope

Dan: we should be providing more guidance to requestors.  We can also do things like closed status for "go to xyz group and come back to us", or delegate directly to that group with chair's agreement.

hober: from basic input & output question:  to improve our rate of work, can close issues faster, and reduce incoming rate.

lukasz: a problem with delegation:  are we going to be sure that input we get is something we expected.  

Dan: trust but verify

lukasz: or something we do to get rid of it?

sangwhan: One way to get consistent trusted reviews is abusing TAG alumni.

Dan: Yes, but they aren't currently TAG members and it's a lot of work to ask of them.

Dan: had a good point:  in what official capacity can that be the case?  Though the TAG has in the past had task forces, chaired by ex-TAG people.  e.g., polyglot specification review.

Dan: Task force needs to have mini charter giving its scope.

Dan: So what about the idea that we might encourage ... would it break things if we tell blink people that maybe review requests shouldn't always be to the TAG?

Alice: That's why I raised question of whether our incoming issue queue should be to-dos for us.  Balance about determining who does the review.  It can't all be on us, but can't all be on Blink engineers because they may not know.

Dan: We have good enough reputation within Blink project to be a delegation point.  I think this (circles) option might be a better... if we tell engineers to request review from X Y or Z then engineers might ... if we tell them not to request TAG review might lead to less horizontal review.

hober: another way to frame that:  we could change our process of handling the review requests we get -- that's separate from how the review requests happen.  We could say "go to other group".  We could separately request to the Blink project having their process be more complicated.  Whether or not Blink does that is separate from the question of whether we should delegate to domain experts if we think that's right.

Kenneth: could be part of blink process to ask for other external review.

hober: we don't control blink process but could ask them to consider changes.  I think mandated external review for API changes is awesome, I don't think we're the best group to handle all of them.

Alice: I think the Blink process needs to fit around our process and not vice-versa.  I think we can write our process in such a way that makes the blink process that we want an inevitable outcome.  If our review template asks what other groups have reviewed this, then...

Dan: I think WG/CG/something -- we should be asking that.  What open groups -- some word that encmpases lots of standards groups-- 

Hadley: In the process document we ask people to demonstrate wide review -- does that capture what you're thinking?

Dan: more with "have you engaged at least one of these -- in which has it already been discussed"?  e.g., a Mozilla engineer working on thing in Gecko or Servo and has a WICG thread and then  -- related to CSS -- at what point did you engage with CSS group, or Web Bluetooth CG, etc., on this topic

hober: link to issue / show your work

Alice: would inevitably make sense for blink process to say: TAG's going to ask about this, so you should do it.  So if ? then fail fast or delegate.

hober: I think we change our process, and blink would change theirs as a result of working with it.

_~ a short break ~_

torgo: How shall we proceed? We've come up with a lot of good ideas; we need to make some of these things real, and map these things onto tools like the new templating thing, and new labels. What changes do we need to make?

sangwhan: Could this be a breakout?

hober: I think there could be longer-term improvements we could make with tooling, but I'd like to scope our consideration of tooling changes to using the existing tools that we have e.g. creating new labels etc. If we generate thoughts about a cool tool we should write those down, but not gate on them.

_~ a discussion on background noise, and the weather ~_

sangwhan: Specifically, we should create a document for the ideas we've discussed. Secondly, I said tooling but I mean more what we can do with the existing tooling.

torgo: Can we do this by making issues in our meeting repo?

sangwhan: _mind blown_

torgo: This is a (meta-)meta-topic. We had issues about how we do reviews.

_~ a facetious process question ~_

sangwhan: .... if I'm assigned to an issue, and it is pending external feedback, (the person assigned to the issue) I should make sure it is not on the agenda.

hober: "pending external feedback" is a milestone. 

alice: when do we check?

sangwhan: Normally I check when Peter makes the agenda. I don't have any control over that.

torgo: I've created [a document](https://docs.google.com/document/d/1QQTMjjlaIacuji4-iN1NVMka_qpKbOFm1Rzwn7Zbhvs/edit) to track the output from this discussion. It's a Google doc. 

torgo: Tess, you raised an issue on how we assign issues to milestones. In the VR working group they use labels.

hober: In CSS they 

david: The way we use milestones creates confusion for the people interacting with us. They expect us to get to things when the milestone says.

torgo: The milestone makes it easy for the chairs to create the agenda.

Alice: we have regular tasks: - create agenda for next meeting - each of us to check what we are meant to be working on

sangwhan: including pushing things that require immediate attention to the top

hober: Creating the agenda is a chair's responsibility. What can we do to make this easier on you?

torgo: For us, having the milestones represent the calls really helps to create the agendas. Being able to easily create agendas with a tool is very helpful for us.

hober: Since agenda creation is on you two, we shouldn't mess with it unless there is an issue.

david: A few of the things are about managing people's action items. Part of the way we use milestones is to track those action items. It's not always obvious what the action items are and who they are assigned to. e.g. "this is meant to be on an agenda for this date, because this is meant to be done by this date".

torgo: How might we use github issues to better solve this problem? Should we go back to having one assignee per issue?

hober: It depends what the assignee field means. If it means "this is who might look at/discuss this", then multiple is good. If it means "next action", it should only ever be one.

david: We need to be better about removing assignees.

torgo: We use multiple assignees to create breakout groups. 

sangwhan: People should be better about unassigning themselves.

torgo: I've seen people use markdown documents in github repositories for more nuanced reviews.

hadley: That makes sense when producing something; when we are making comments the comments should be on their document.

torgo: Should we be doing something more creative with labels?

hober: Yes. Labels are free, we should have many of them. Anything that can be usefully tracked on a label, create a label. Just about all of the status should be tracked using labels.

sangwhan: e.g. "label: pending-feedback-tess"?

torgo: We could use labels for meetings instead of milestones.

hober: Personally I think you should leave milestones the way you're doing them. I think we can create the labels organically. Colour coding can help with categorising groups of labels.

hober: We could create four "closed" labels - "thanks for flying", "dissatisfied", "timed out". Then review status labels: "not started", "in progress" etc. Then labels for prerequisite items e.g. "created explainer".

torgo: I am good with using more labels.

torgo: Let's talk about templates. Who is familiar with this new templating system?

hober: I read the readme. You can have multiple kinds of templates. When someone presses the new issue button, they choose what type of issue it is and that populates the template. 

hober: I'm inclined to say that figuring out that system shouldn't gate immediate improvements.

torgo: How do we want to categorise review requests?

hober: I'd rather that fall out of us doing it organically. I'm not convinced yet we need multiple templates.

torgo: Do we know enough right now to make changes to the existing template? I feel like we do. The "what other standards groups have reviewed this", and "what domain is this".

hober: I feel like it's two things... 

torgo: There may be something happening in a WICG group which is related to HTML, but has not been reviewed by the HTML group yet.

david: "What multi-stakeholder review has already happened?" You can do work in WICG with no external review, or you can do work in WICG with active engagement.

hadley: Do we want them to send us a link to external review/discussion?

alice: Some of this could be in the issue template, and some in the explainer template.

hadley: could you be more specific?

alice: some might make sense in the explainer template, e.g., for CSS alt() I gathered links to other discussions and put them as links in the explainer.  I'm not sure how long we review template to be -- versus be succinct and link out to explainer that has the relevant explanation.  Is the template a checklist?

hadley: I think the explainer isn't just for us, for lots of people to understand why the feature ended up the way it is.  If a trail of pointers to other discussions helps meet that need -- then definitely.  If it's just for us, then makes more sense in our template.

alice: who is the explainer for?  excellent question.  I've been talking to a tech writer -- Joe Medley.  He's proposing that explainers can feed into MDN articles.  On the Blink side can help answer questions about why we have to write so many documents.  Really should only have to write one, but I'd like to see explainer template that -- crib that converts to a bed -- works across stages -- for explainers.

alice: nice to have examples of each of these -- something for problem and idea stage -- something for intent to implement stage -- something for intent to ship stage.  Core things: what problem trying to solve?  what's the idea?  what alternatives rejected?

dan: explainer also to articulate the end user need.

alice: goals and non-goals.

dan: I don't think we want stuff like group enggament in the explainer -- that's part of the request template.  I think most things are request template things.

alice: may have a place in the explainer -- even if soemone reads it outside of the context of a TAG review -- should still be able to get answers to due diligence questions from the explainer

dan: I feel like it doesn't belong in explainer, belongs in the spec.  Dependencies section in the spec.

alice: I feel like explainer should answer what but also why.  Review process is part of the why.

dan: should we ask people to put this in the explainer?

hober: we need to know to what extent wide review has been happened and where.  We're not the only ones interested in that question.  Explainer audience is wider than us.  I don't see why we shouldn't put that in there.

Kenneth: great to see who's involved

David: Fan of more links.  Helps understanding, could also help people get involved.

Dan: At 11:30, can we just do a bit of editing?  Edit the explainer explainer, issue template, and review those changes.

Alice: Before that, can we come up with examples of good explainers and good reviews?

Hadley: We had some in explainer explainer.  But if we're changing it, may not be best examples anymore.

Alice: Can we look at good reviews and see what went right.

?: want an example.

Alice: I want an example that compellingly demonstrates user need.

Dan: explainers also weren't our idea; people are writing explainers for other reasons.

Alice: Related question for CSS WG; don't have explainers, write introductions to specs.

David: I think it's OK for explainers to be in the spec (e.g., in an introduction).

Dan & Alice: we should encourage it to be a separate document. It's a different audience.

David: together helps avoid explainer getting out of sync with the spec.

Kenneth: Could add section to issue template asking whether explainer is up-to-date with the spec.

_~ breakout planning for labels and templates ~_

https://help.github.com/en/articles/creating-issue-templates-for-your-repository


### Afternoon Session - Breakouts

### Readouts

Scribe: Tess (backup: Sangwhan)

#### [Temporal proposal #311 (closed)](https://github.com/w3ctag/design-reviews/issues/311)

Sangwhan: We closed this.

David: We provided some feedback

Sangwhan: They've opened up a bunch of issues on their side and are willing to address our feedback

David: They fixed some of our issues, and said that some of ours should wait until after this is a thing

David: Closed with "please fix the WebIDL thing before you ship"

#### [Contact API #337 (in progress)](https://github.com/w3ctag/design-reviews/issues/337)

Dan: We asked OP if we should defer review until the draft is more complete

Dan: We were both generally happy with the design of the API

Dan: We remain concerned with misuse by bad actors

Dan: It's gated on a user gesture, but User Activation is a low bar (e.g. ubiquitous cookie notices)

Dan: We should close this issue

Tess: Lots of autofill features for contact info in HTML - which are widely implemented. These are gated on user activation, along with user choosing the field input data. Why is that not adequate? The pre-existing API doesn't have that problem.

Ken: This is for multiple contacts.

Dan: This is for joining social networks, where you will provide them with a list of contacts. Certain actors are good at abusing this, so this is an improvement.

Tess: Isn't there a input multiple thing? Nothing in HTML that does this? If the only feature gap is multiple, since many apps abuse contact info why should we add multiple anything in the first place?

Dan: Would like you to provide feedback on this, but read the explainer before this?

Tess: Sure

Dan: let's leave it open with this milestone

#### [Web Bluetooth Scanning #333 (stalled)](https://github.com/w3ctag/design-reviews/issues/333)

Dan: Multiple issues with this. We reorganized, added lots lof labels etc., this is stalled. We've asked for updated status and said that we remain concerned about the privacy issues we raised earlier.

[aside re: appropriateness of google docs for hosting explainers]

#### [Backdrop Filter #353 (pending external feedback)](https://github.com/w3ctag/design-reviews/issues/353)

Alice: Specific draft of feedback on the issue (in slack)

Alice: [summarized Tess' draft feedback]

Dan: We should have a label for "this issue has multi-implementor implementation/implementability concerns"

David: are there major unresolved issues in the discussion?

David: Alice and I added two things to the issue template this morning, including linking to multi-stakeholder feedback and discussion

Sangwhan: I often check Mozilla's standards-positions repository and find that their opposition to an issue is clear there, but not marked in review requeasts to us

Alice: second meta issue: how do we feel about asking them to write a spec with known interoperability concerns

Tess: Where we ended up is that both approaches are not implementable by multiple engines. What we don't know is that for the common case does it matter; can we accept and move forward accepting the constraints?

Dan: If it marginalizes certain groups of users this would be problematic.

Tess: If someone tells us that the outcome will be catastrophic it would be good to know.

David: e.g. how does this conflict interop with other CSS features? and how do we deal with cases where a high profile site uses the problematic trade-off combination?

Tess: Would like to post this and continue the discussion. Alice also raised two meta issues; we should raise both of those. One is how do we track implementability concerns? Second is is it okay to sign off with interop tradeoffs?

Dan: I don't see an alternative.

Alice: Just raised an issue on this.

David: Do you want to make a comment on backdrop specifically?

Tess: Yes.

#### [Feature Policy Control over Sandbox Features #339 (external help requested)](https://github.com/w3ctag/design-reviews/issues/339)

David: One of the things that came up before was needing to offer guidance for this and related features

David: Maybe we should have WebAppSec take up that work

Dan: We'll talk to mwest about this tomorrow

#### [Transferable Streams #332 (closed)](https://github.com/w3ctag/design-reviews/issues/332)

Dan: We closed this because our feedback was recieved, they updated their explainer, so they'll come back when they have more.

#### [Text Encoder Stream #282 (closed)](https://github.com/w3ctag/design-reviews/issues/282)

Sangwhan: Closed, as the feedback of current TAG members has all been addressed.

#### [User Idle Detection & Media Stream Image Capture API (pan/tilt) #336 (stalled/review complete/pending spec update)](https://github.com/w3ctag/design-reviews/issues/336)

Sangwhan: Review completed. We are waiting for them to make the edits based on our review.

Dan: We need a new "progress: pending spec update" label

#### [Privacy Mode #101 (stalled/to be closed)](https://github.com/w3ctag/design-reviews/issues/101)

Tess: We think the current issue should be closed. It was a request for review which nobody is watching. Would appreciate help with the text for closing.

Dan: Mark wouldn't have issues us taking over. Where is this new proposal that is mentioned?

Tess: I'll paste it in the minutes

Tess: "@lknik is working on text for a possible TAG finding on this topic. Given that, I'd like to close this issue. Interested parties are encouraged to raise issues on his document once he has a draft up."

Tess: I have a question - if Lukasz' draft is going to be ready later is it okay to close the issue?

Dan: Think it's safe to close. It will be a new thing.

#### [Web publications review #344 (in progress/pending external feedback)](https://github.com/w3ctag/design-reviews/issues/344)

Dan: They were looking to update the explainer; we are pending external feedback.

David: It's also pending delegation of review of the CORS/Fetch integration to someone else

KRC: Jake [Archibald]?

#### [ads.txt #201 (pending external feedback/migration proposed)](https://github.com/w3ctag/design-reviews/issues/201)




#### [Audiobooks #345 (waiting for updated explainer)](https://github.com/w3ctag/design-reviews/issues/345)

Tess: Last time we were promised a new explainer - still waiting.

#### [LazyLoad #361 (pending external feedback/editor update/unreviewed)](https://github.com/w3ctag/design-reviews/issues/361)

Tess: Sangwhan and I sketched out a bunch of questions (internally, for us to look at). There has been a lot of work in the meanwhile, and we want to look if those questions were either solved in the PR or the upcoming patches that have been on-going.

Tess: our plan is, in between now and when they tell us they’re ready for us to review, sangwhan and tess to each read the pr in light of the questions we generated in this thread, eliminating the ones that have already been answered. Once they’re ready for us to review, we’ll then be in a good position to provide feedback.

#### [User Activation Delegation through postMessage #347 (pending external feedback)](https://github.com/w3ctag/design-reviews/issues/347)

Sangwhan: We're not convinced that this is solving a real problem

Sangwhan: This is about some features that [UAv2](https://www.chromestatus.com/feature/5722065667620864) ([#295](https://github.com/w3ctag/design-reviews/issues/295)) broke, that work in the other browsers. No one else needs to fix this case, so it's weird that the proposal is to change the Web platform to work around a bug in Chrome.

Dan: Let's punt this to tomorrow, since we only have 1 minute left.

Alice: given the last comment in the issue, they may not need more comments from us

Dan: [proposes comment on issue]

Everyone: sounds good

Sangwhan: Still want to discuss the meta issue tomorrow.	

### How did we do today?

Tess: We got through way more than we did in Tokyo, and had more chance to deep-dive. I really appreciated working through the Backdrop Filter issue, and I don't think we could have done that in the old format.

Dan: This is the one thing in reading this "leading effective meetings" book that I was concretely able to implement. Having more than two people in a breakout leads to people tuning out.











