## TAG f2f meeting - week-of December 2, 2024

## Day Zero - Agenda Setting - 2 December (Afternoon)

Present: Dan, Peter, Hadley, Amy, Martin, Jeffrey, Matthew, Lea
Guest: Henry Thompson (TAG alumnus)

### Discussion on Related Website Sets feedback

We agree to revise the "first party sets" feedback to reflect that it's called related web site sets.

https://github.com/w3ctag/design-reviews/pull/1022 

*consensus to merge - we merge*

### Design reviews vs other topics

*consensus to focus on other topics in this f2f - especially design principles*

### We discuss Design Principles for Web Developers

Dan: we could use the same approach that we have used in the privacy principles document - labels.

*we schedule a triage session for Tuesday afternoon*

*we discuss the fact that some of the design principles are applicable to web component authors.. and other audiences .. and we can mark these as such.*

Lea: also CSS custom properties - design principles on how to design custom properties - e.g don't use boolieans.  Often the difference - something relevant to web platform designers in the future could be applicable to authors as well once they have that power.  When the existing precedent has poor ergonomics, what should developers do?

Martin: often "ergonomics are not ideal" .. shades of grey.

Martin: options dictionaries & default values (391 and also 437); PR on 496; 

## Day One - 3 December

Present: Dan, Hadley, Matthew, Jeffrey, Amy, Peter, Tess, Martin, Yves

Online: Tristan

Guest: Henry Thompson (TAG alumnus)

### Tracking issues

Matthew: we're a horizontal review group. We mostly look at design reviews. We get them earlier than other HR groups, which review specs.

There are a number of issues that as HR review groups we are exposed to and we can/must look at. Spec reviews, charter reviews (new group proposed or feedback on a charter draft, Yves monitors this and alerts us where it makes sense to weigh in). 

From an APA perspective the other HR groups keep labels for each HR group to say they've completed review.

Yves: there is one for the TAG as well, but they don't use it.

Matthew: the other type of issue is -- name varies -- where people are talking about a particular thing in their repo, developing a spec, got their own repo/issue thread, and they want some HR group's input, they can attach a label, whcih creates a tracking issue for the HR group which then go into a dashboard.

Torgo: we've made use of this from the other side: we have marked some isssues as a11y-tracking or i18n-tracking

Matthew: (opens [tracking issues](https://github.com/w3ctag/tracking-issues/issues) repo)

There is a well defined process for: these things get made, what the labels mean, there is good documentation (i18n had a big hand).

We could use this repo in 2 ways. (though process has changed over past few years)

Title will mirror the issue created in the other repo, but we can change it. So if it says "TAG checklist", which isn't obvious to us, we can rename it. The first comment has a pointer to the other issue. This is public, and we could use this issue to discuss things, or we could go to the original issue in the original working group's repository.

Each issue has labels to indicate status.

Becasue we don't look at these very often, some of these issues have been closed without our output. 

Labels: `Pending` means we haven't looked at it, and `close?` means should we look at it because the otehr side did. `needs resolution` means we've said we need a specific resolution before closing. But sometimes the group has applied the label themselves becasue they got some feedback in the design review.

So we could see this as an inbox only. The other way we can use this repo (as other HR groups do) is -- we're all familiar with the idea that when you raise issues, you raise one issue about one thing, a single discrete actionable thing. When we do reviews, we're not usually in the details becasue we see things earlier on, but sometimes we do have several points.

Other HR groups will use this as an inbox and an outbox, will draft each bit of feedback in here as a separate issue, then vote on it. When they have consensus, they follow a process to pop that in to the other issue and this becomes a tracking issue to make sure that all their feedback is followed.

I think most of the time we don't need to do that because our feedback is broader. But we could do that because the groups often make issues from our feedback in their own repo. 

We are sort of following the process. We could do more, but using this as an outbox is a bit like a public version of the private brainstorming thing (which I think is still useful). That's what w3c is saying HR groups should do.

The main question I've been looking at though: did we miss any opportunities by not looking at this?

Caveat: I looked through the latest 30 issues. Unfortunately, I looked through the latest 30 filed issues, not the 30 issues with activity on them. There was one on game pads from ages ago. Some are really long running, most aren't. This doesn't get used very much. If you ignore everything before 2020, there isn't that much of a backlog.

Do I think we've missed any opportunities? Let me share my spreadsheet.

I found: sometimes people filed issues here because we didn't respond quickly enough elsewhere. Sometimes it was the other way round, they asked for help on this repository, so they raised a design review afterwards.

The ones particularly deserve looking at are the ones only in this tracking-issues repo and nowhere else. Especially where we had the `needs-resolution` label on it, and the other group resolved it, but we didn't check that it was resolved as per our expectations. The interesting thing: only we are supposed to use that label, as I understand it. Because we didn't make issues in their repo, and they did to reflect the fact that we asked them to fix something

Torgo: so there was a design review, we requested a change, they opened an issue in their spec and added a tag-tracking label and a needs-resolution label

Mathew: TAG-needs-resolution means the TAG wants to see something happen. I think only the TAG should apply that label, but sometimes people have done that for us. And then we didn't check that it was fixed.

Yves: sometimes with PLH, we try to do some clean up where needed.

Torgo: how can we best integrate this clean-up, which we could do, into our process, so we are providing better.. the Admin stuff is irrelevant. What's relevant is providing the service to the gtroups that are asking for our advice.

Matthew: I agree the admin isn't the most important part. BUT as an HR group, if we do raise several points in a review, we owe it to the other groups to follow the process. 18n do it, it's easy.

out of the 30 I looked at, i think 3 are where we missed an opportunity to check for stuff.  Web machine learning, also web machine learning, and ... sometimes a design review is filed but we miss some of the discussion that led up to it, maybe 6 months before. depending on how early we want to go, we could've shaped things earlier if we had the chance.

Largely, we haven't missed many opportunities, but we are getting duplicates because we aren't responding fast enough, and on some things we asked for changes but never check.

There is confusion between `pending` and `needs resolution` -- which is contradictory. ones that also say `closed` are concerning because we missed the opportunities. Almost all of these are architecture stuff and having looked at them, it's probably ok.

I would suggest that I redo this exercise looking at the most recently touched issues rather than most recently filed. But at the rate these are coming in we could absorb these. 

Hadley: what is the rate?

Matthew: one every few months. APA gets them all the time, and I think we should be encouraging more of this. Both ends of the review process, early on small feedback -- and then also worth it to track things wehre we asked for things to be done but we never follow up.

Hadley: thank you! Concerns - we need to be providing as high quality and helpful help in the best time, we need to find a way to do that. And in the past, the issue template for design reviews used to say would you like us to put your feedback in this issue or open issues in our repo; many would choose the latter, we would open several issues then drown in too many discussions. We took the decision that they can manage their repo/issue, and we'll keep ours open until they come back and say yes this is done. Most of the time that works. Occasionally we don't follow up. Concerned that if we reset the boundary for what's in our attention span we will end up with a similar problem, eg. if I'm in charge of a topic do I have one issue to check or fifteen. How much time is appropriate? Third concern - TAG is not the same as other horizontal review groups. Okay for our process to be different.

*"TAG Exceptionalism"*

Dan: in favour of spending more time thinking about this kind of thing is that often we're getting dinged for being over-responsive to chromium issues and therefore letting balls drop for other things. Paying more attention to HR from other groups could be a way to mitigate that. Also share Hadley's concern about time management.

Yves: for charters, I try to alert on slack when there's something that might be of interest. plh knows when doing hr for charters if the TAG didn't say anything then it's fine.

Tess: The problem is that we allowed ourselves to become a HR group. We didn't used to be a HR group, but because design reviews looked like HR, it became part of the process. Now, I think we ought to do it the same way as everyone else. But I don't think we should've.

Dan: I don't know when that happened.

Tess: I went to try to figure it out. The process document changed version control systems, and I couldn't work it out.

Dan: my mental model of the TAG is that we have discretion on what we want to review.

Tess: I don't think that's true

Hadley: then we have a big workload problem

Yves: the rview that the TAG are doing is a bit different. We are doing more architectural things means our value is more at the beginning

Tess: right, which is why we shouldn't be considreed an HR group

Yves: where as i18n, a11y look at things later

Tess: Right ,it's a fundamentally different kind of input. We shouldn't be on the hook for late stage HR stuff.

Jeffrey: where in the process?

Tess: It's by reference to the Guide, which lists us as an HR group

Yves: the thing is that we don't have, even in the Guide, a nice place to say that we want to have an early reivew of a document. That's what's missing. If we add it there or anywhere else, maybe at first public working draft, that would take care of it. Some other HR group might want to look into a spec at that stage and then review the diffs at CR, as well.

Matthew: I hear the concerns of workload management and what is the nature of the TAG. I agree with what everyone is said. We have a mechanism to decline to review stuff. If you look at the 2 areas that come up when we talk to external parties: earlier feedback, and when we decided that something was important enough to ask for a change and don't check on it. In that case we don't need to use the `needs-resolution` label. That could help us track things that are unfinished.

right, it's not solely at HR stage, it can be things that groups raise, and we're not responding. The most interesting thing, the one about CORS, it was clearly a potentially architectural issue. We were flagged as wanting a resolution on it. I want to doubly acknolwedge Yves's work to keep tabs on this stuff. It's great, but it's also helpful for all of us to understand that that's what you're doing and why it's helping us.

When we talked to FedCM, they said this is the kind of mechanism we can use to track your feedback. 

Hadley: coming back to not wanting to lose track of feedback we've asked for - incredibly important. What is the benefit to us to going through this process in the tracking repo rather than via design reviews. 

Matthew: a lot of the time when we do a design review it's one piece of feedback that we give. When we come to a conclusion most of the time that might be it, sometimes we might have found discrete issues that we want them to fix or be aware of. Then this process is useful. Most of the time it's used by a group looking at a spec and filing a whole load of issues. We don't get that on every design review. When we do, and we say we want you to fix this, this and this, this process enables that to be automatically tracked.

Hadley: feel like I'm missing something. We often give feedback with multiple points, which each need to be resolved.

Matthew: if we do that, logically we've given them that feedback but if we were to follow the process we would file those issues in their repo and the system would track each of those 5 for us. We're not doing that step. They will take those five points from our comment and file five issues with the needs resolution flag, and that's when they appear to us

Hadley: understand the mechanics. Why is that useful for us?

Matthew: we close a design review, and then have to do work when any of those 5 were resolved. This system will track that for us.

Hadley: i'm still ot clear what value this adds for us.

Martin: why is this our problem? When we leave 5 points on a thread, the ball is now in their court. When they've resolved those issues they can come back to us and ask us whether or not the problems have been solved. We don't need to do the work to track that. Setting up a system is accepting that it's our problem when we should not be. I'd like to see a process whereby we raise whatever issues we have and signal what level we care about them. Eg. serious, or you don't need to come back to us. Ask to consult with us again when they think they've resolved it or can explain it. I'm not sure a process of this shape is going to help.

Jeffrey: the TAG tracker and needs TAG-needs-resolution are the two levels of interest mentioned. We shouldn't be reviewing the open issues with those labels. What seems would be useful is to review the recently closed issues with those labels to check they closed them correctly.

Matthew: that's how they tell us they think they fixed it

Jeffrey: the tool lists the open ones not the recently closed ones

Matthew: `closed?` means they closed it, are we happy with it

Martin: if they're clsoing issues without talking to us... that's their business. There are a whole bunch of issues with useless labels and links that point off to somewhere else. It's for them not us. 

Yves: in the case of tag neesd resolution it's also looked at when doing transition to check the process was followed and the TAG agreed on the resolution.

Jeffrey: it's a flag for us to escalate if we're unhappy with the resolution

Hadley: we have used our resolved tags in our repo for similar purposes. To say we're done with it and happy or unsatisified. There are times when transition or chartering discussions ahve taken tino account where the TAG ended up. Still unclear why we need a different mechanism. What we're currently doing doesn't get fed into the process?

Yves: this process exists for all HR groups. Simple signal. We open an issue and we do or don't care about the resolution. That's the tag needs resolution label. This is what we're not really using properly. The other one we can use or not.

Hadley: if we had a very contentious WG or design proposal that we were having a difficult time with and wanted to make sure that when they were having discussions about progressing this we wanted to make sure that our message was getting through. We'd then turn to this label rather than using it for every design review?

Yves: yes. Then it's tracked when we're looking at anything related to transition.

Dan: I have drafted a resolution... agree we should not chase whether groups have resolved issues - that's up to them. BUt it is valuable to track when groups ask for TAG feedback.

Martin: how does that differ from a design review?

Dan: it's a conversation, not a full design review request, it's a specific question

Amy: Didn't we add discussions and a different issue template existing for that...

Matthew: you can bring groups in by adding a label, the thread is already there

Peter: we need something to link threads ..

Hadley: adding a label where the thread is already there that puts a load on us to read a whole thread and understand the context of every comment. We abstract away some noise by starting our own issue

Martin: someone opening a design review puts extra work in to summarize the problem. We can look at the thread if the summary is not good enough.

Peter: if they put a closing comment that summarizes the discussion and conclusions and that gets posed back to our design review that would be awesome

Matthew: I'm not saying we should stop what we're doing now. Most of that works well. Just whether we're missing anything.

...

Tess: reviewing anything is a means to an end. We choose to do reviews because we believe it helps us remain an informed body to ensure the architectural cohesion of the web. Any access of process that has a different interpretation fo what our obligations are is a problem.

Hadley: would add that we choose to do it because it provides value.

**PROPOSED RESOLUTION** : The TAG affirms that its process includes being able to decline requests w/ prioritize our own work. The TAG would like to modify the guidance for horizontal review.  In particular, we would like to note TAG's role in giving early review, rather than horizontal review. As far as horizontal review goes, the involvement of some groups will be different according to their special role; it is often better to involve the TAG earlier.  We need to tune how w3c community ask TAG for horizontal review to ensure that this review is useful to them and that people are not doing unncessary work.  

-- 

*further discussion*

Present: Martin, Matthew, Yves, Amy, Peter, Dan

Dan: trying to come to resolution

Matthew: it might be that there is some overlap between us and these discussions [the tracking issues] anyway. I don't know if anyone is looking at the tracking issues and going into them... It could be that TAG doesn't do anything but others can look... 

Dan: if we keep the tracking issues around we should integrate them into our agenda process, according to some sensible logic.

Peter: something in gh actions to improve the signalling

Yves: we have a tracking-issues repo for that

Peter: we can modify the agenda script to scrape it but we need better signals

Matthew: Jeffrey was suggesting when "close?" is applied and it was something we flagged we care about that's when we really need to look about it. Generally the other gropu is saying they made a PR, what do we think? We don't respond, they merge and close the issue. That's when we'd see it. Be ncie if we could see it before. But at least at that stage it's very recently closed.

Yves: trackbot is putting a "close?" on issues that have been closed by the WG so we can look at that and add it to the agenda, and see if we should close.

Matthew: some are trival. Spec reviews tend to be of a similarish size of work. Design reviews are quite variable. These are really variable. Some turn into something really big. The ones flagged "close?" if we didn't put "needs resolution" we trust them to deal with it. "close?" + "needs resolution" are the key ones to review.

Dan: propose Matthew and Jeffrey to come up with logic for agenda script to flag potential tracking issues we should be talking about, for the chair to be able to put into our plenary agenda.

Martin: I propose to remove the repo entirely. There are things we'd like to be able to track. Most of them we can rely on other people to do the tracking for us. Creating the expectation that we're tracking things for people is accepting work that I don't think we should be accepting.

Peter: negative incentive of other people to do the effort to get back to us. 

Martin: I'd like to see it be the case that people who want things to happen take that responsibility for themselves. Our responsibility is to provide as many people as possible as much of our 'wisdom' as we feasibly can and the design review process is kidn of okay for that.

Matthew: also agree that we should do something decisive with it. Get rid or embrace it. What Martin said is very clear. You see this as extra work for us to track things. I think if we can talk about it later, I'm not sure I've been clear at explaining how it works. I thought it was a lot of work, but now I don't think it's a lot of work, it works for us. I don't want to go over it if I've not explained it clearly.

Martin: it's a useful tool that is doing some work. The implication of doing that tool is that you've accepted the responsibility for doing that work.

Dan: one thing we could say is ... when we make a review with multiple points of feedback. Mostly we are relying on the receiving party to deal with that feedback. We're not generally speaking tracking that they have done that work. What we usually do is wait for them to respond so at least we know they've received it

Martin: leave the issue open and use that as the means to check again.. but moving more towards just closing

Dan: yep. I don't think we need to minutely check these things. Stll argue there's a value to having groups be able to ping tag to get feedback on micro issues for input

Martin: that sounds like a problem statement to write down. that's why we created the discussions thing

Yves: when the TAG open an issue and say we really want this WG to fix that, we never track it. Th eonly way to track that is when we are doing transition checks. Did the TAG sign off on that? And I'm looking at what's going on. Having a tool that automates that. Looking at my dashboard to see an unfixed tag needs resolution lable is very easy

Martin: it's not always so easy...

Yves: when there's a timeout and it's old it's difficult to decide the status..

Martin: blink review process is the same.. they filed a review and got feedback. They don't say what the feedback was.

Peter: do we start filing FOs to enforce our opinion

Martin: that's what the object status is for

Peter: if we're not going to put stop energy in there's no point in tracking..

Amy: wouldn't it bubble up if it got to transition?

Matthew: what would block a transition request? an unsatisifed review or a tag resolution that's not closed?

Yves: both

Martin: do we want to be the gatekeepers. We haven't been and that's a feature.

Peter: reserve that for the object situation

Martin: yep, limit that power

Yves: when an horizontal group files something against a transition, eg. i18n needs resolution - if there is a disagreement the team look at that and decide whether to ask the WG to work more on that. Judgement. Either we go to a place where people can't agree and escalate, or we ask them because we see there is a potential for agreement to work more on that. Maybe they forgot. a * needs-resolution is not a block to publish the document.

Matthew: moving away from tracking what was done ... there's value in getting iput from people on specific questions. If we used this repo for the people want TAG's input on a question issue, that wouldn't be acceptable becuase you're coming in the middle of a thread? They should form a question and ask us?

Martin: yes prefer that. We've increased the barrier to epople asking us questions. We have the dispute resolution template. Might be better to add a new template that is ask the TAG a question. What is your question and please provide a link to context/discussion so far.

Matthew: so this repo would not work for that. Whilst somebody could put a summary comment you can't necessarily jump straight to that. Alternate path than filing a design review request.

Amy: in favour of having only one place to look for stuff, as long as it's set up to receive different kinds of things.

Yves: need to decide how we are part of HR. General discussion on how we interact with other groups.

Peter: we might build some actions into the existing repo - a bot that says to go file an issue elsewhere for TAG input

Yves: do we want to track FPWD instead of transition to CR?

Peter: probably

Matthew: APA goes out and looks for FPWDs to read. Early design review equivalent. Really useful or it's way too late. Earlier I was thinking is there a label that we need or oculd use on our design review threads would be like TAG needs resolution. Extremely strongly think we should delete the repo if we're not using it. Nothing is going to stop people putting the label on on their end.

Yves: it's a bot that adds all the possible labels. We can delete the labels.

Matthew: I'd like us to monitor it for a while and see..

Yves: main thing is to clear everything that has been closed

... discussion about how this impacts transition ...

Dan: design reviews are not uniform in scope. Sometimes not specs, or specs elsewhere.

Dan: **RESOLUTION: We won't actively monitor the tracking issues. We won't ask for the repo to removed at this time but we will sign post it as not being actively monitored - however Chairs and Team Contact will monitor the tracking issues and then we will revisit and potentially request closure next year. We will make it clear that we are an optional part of the horizontal review process. We will ask to modify the horizontal review page to make it clear that we would like people to request TAG feedback early in their process rather than at transition. We will add a "ask TAG a question" review request template that is much simpler than design reviews and will encourage TAG questions earlier in the process.**

Yves: lgtm

Martin: +1

Dan: let's still add something to the agenda creation script...

Matthew: +1 to proposed resolution.

Peter: should we turn off the discussions?

Martin: let's float it with the larger group?

https://github.com/w3ctag/design-reviews/pull/1025/files

### Taps


```
---------------------
              ( ^ C  |   which way do you turn the knob?
              (      |
              ( v H  |
---------------------


---------------------
              ( ^ C  |   what about this one?
           ---(---   |
              ( v H  |
---------------------


---------------------
              ( ^ C  |
              (--    |
              ( v H  |
---------------------

---------------------
           ^ C (     |
               (---  |
           v H (     |
---------------------
```
 t cluo
We have solved it. Write a standard.

Side discussion: toilet flush buttons


### Retro

Topics:

* Ratio of design review to other work
* Relationship with the rest of W3C
* Engagement / participation
* Technical leadership
* Councils
* Async work
* Face to faces
* Policy engagement
* Background noise of terribleness
* Councils
* The abyss
* Burnout
* Authority
* Developers
* Inclusion
* Relevance


#### Technical leadership

Henry Thompson: when did the TAG start providing technical leadership? The Team used to do that

Tess: it's a member org, it shouldn't be coming from employees

Hadley: especially since tim started receding from active involvement

Round question: How can we provide technical leadership?

* Writing more, especially on topics architectural and topical (which is an overlapping venn diagram)
* We only produce output that is only consumed by the people who asked for the review.
* No value in a singular vision for a technical direction; a collection of things.
* Big problems, not always entirely technical - be careful writing about social/political problems.
* Speak from the experience / authority of the TAG from which we provide credibility.
* Set the ground rules for the debate - not give the answers - in the things we write
* figure out which other groups are doing what we should be doing technical work and have a liaison connecting us to them / socialise our vision(s)
* writing things is how people find out the TAG has an opinion.
* two types of writing we could do: abstracting from experience (like the ethical web principles) but also doing high-level opinion on emerging work (AI, web 4) even if it's not ready for standardisation yet. Give a framework or people to look at those emerging technologies in the context of the web platform.
* Engage more with the community in order to drive the conversation around some of these topics. We haven't historically done this well, did in an ad-hoc way with developer meetups. Could be more structured, with less logistical nightmares: zoom meetings, webinars, podcasts... with group chairs in W3C, developers and open source commiunity outside the W3C.
* TAG podcast / tiktok
* socialising our vision
* the IAB and TAG don't officially talk to each other, and that's broken. Even more unfortunate now given the threats.
* Speak more, speak at conferences and events (that we aren't hosting). Can be invigorating, useful feedback.
* educate regulators to avoid unforseen consequences
* talk about how to join the W3C community, reduce barriers to entry (even more so for people who already work for W3C members)
* improve IE process for joining 
* route stuff ("go talk to these people, they know everything about that")
* provide pointers in design reviews to other experts. We know people.
* writing observations on how the world is and how people are reacting to it. A lot of what we do is social construct, and amplifying what we see can change the shape of that construct.
* set some goals (define success)
* We used to have the Extensible Web Summits. If we have a goal or vision or targets to nudge the web towards, we could set up something like the Extensible Web Manifesto and a similarly themed set of events.
* figure out what our vision is
* It's not enough to do the work, we have to be seen to do the work. The TAG is elected by the AC, which -- as a body -- doesn't get to know much about what we're doing. Elections, presentations twice a year, and that's it. We could email our minutes to the AC. Remind people what we do.
* We could have office hours for the AC. 
* Generate a report to the community including a summary of what we've done (published these findings, cleared this many design reviews). Not the minutes, a digest of what we think people should know.
* Have a meeting on this report
* Write a report / digest after this face to face -  Semi-automate it, the chairs can just DO it
* Change our place in the process so we aren't stuck being reactionary
* organise workshops with people who have the expertise on a particular topic. 30-40 people
* Take input from what WGs are actively doing (ground our work in this)
* Be alert to potentially similar work happening in different places and encourage consistency (and collaborations)
* run a TAG-led workshop on the commons (following AC demand) -- perhaps adjacent to the Commons workshop in June in Amherst: https://2025.iasc-commons.org/.
* recognise that the Design Principles are technical leadership
* create a new repo "technical leadership topics",
one issue per topic, with an owner, to track the progress on it. 
* Git projects board, run like an open source project.

#### Time allocation

Dan: in the context of the list of possibilities above, what should be spending our time on? We've said we don't want to drop design reviews, how should we be prioritising?

Round: how can we prioritize our work and allocate time?

* pick a day that is TAG day, so we aren't spreading the work all through the week. (For example, Monday is always TAG day)
* set targets (number of findings per year, for example) and then reverse engineer time allocation - writing, reviewing, relations (3 rs)
* design reviews should be in the service of another end, not an end in themself. Close design reviews by default (probably after a month or so), but let people flag any review as useful - important feedback, or it will teach us something; goes onto discussion queue.
* ask the blink process to remove us from their process, freeing up a lot of our time
* consider the topics most in need of our attention - that bubble up above deisgn reviews, general trends - allocate the largest amount of our time on those.
* create some means of getting them on the books so we can prioritise them. (Issues? Repos? Web platform gaps? But some of these aren't gaps)
* change how responsibilities are distributed: some of us could do design reviews while some are doing other things. 
* We could have our weekly breakout time slots set in the calendar but not have it on a call, but with the expectation that we'd default to working then.
* 70% of our time on technical leadership and 30% on design reviews
* for each week, chairs produce an "agenda" which may not be for breakouts but may be "this is the work to focus on this week"
* Plan provisional agenda weeks/months ahead
* a week focused on a topic (like "this is AI week", "Commons", "Authenticity")
* TAG island
* come up with tooling that allows the chairs to produce weekly agendas according to our themes/topics ("We're going to do stuff to provide technical leadership on authenticity. So we need to gather issues NOT from our design review repo, plan the discussion") -- to make sure that we can actually deliver something
* have someone responsible for each topic, set a few weeks ahead, with an output (workshop, a talk, a finding)
* breakouts could be a subset of the group working on the particular topic
* a target for the topic per week. First week: figure out the end goal (workshop?).
* pick a smaller subset of topics and drive them to completion, so we don't end up in a cycle that leaves 6 months before getting back to the topic again.
* parallelise some of the topics
* ask someone to provide a short briefing to introduce the topic, key issues, recommendation for our goals over the next few months -- so we can go into our meetings prepared to discuss
* In order to put something on the short list, someone has to volunteer to lead it. They then set the agenda for when it comes round.
* designate a Directly responsible individual: if we don't make progress on a thing, it's their fault.
* create a micro task force, or subcommittee, to work on a thing.
* everyone on the TAG should be the DRI of a thing. One per person driving that thing, no more than that.
* Each person participates in 1-2 other things they aren't driving.
* on a weekly basis, the last thing we do in a week is planning for future weeks.
* be clear with the membership what our technical leadership priorities are, our gaps in our skill set, and the time commitment. Some employers won't support 20%, so people need to budget for using their free time. Then we wouldn't have to use breakouts because people couldn't find the time. 
* keep a backlog of topics the TAG members don't want to or don't have the skills to lead


The very first line of The Scottish Play is "When shall we three meet again?"

### Web is not versioned discussion

*We discuss [Web is not versioned](https://w3ctag.github.io/the-web-is-not-versioned/) finding and whether to merge PRs and publish this.*

*We work through additional PRs and agree to **PUBLISH [this](https://github.com/w3ctag/the-web-is-not-versioned/blob/4ac12b405dde2922ba65a0ba33dc21e7e62a41ca/index.html) as a finding**.*

### Design Principles Session

[Update principle on HTTP usage](https://github.com/w3ctag/design-principles/pull/487)

Jeffrey: i kind of agree with Anne on the structured fields - a think that often people need to be reminded to consider - but don't feel strongly - don't insist

**merged**

[Editorial updates to media types section](https://github.com/w3ctag/design-principles/pull/488)

*discussion of this ... Anne left a comment ...*

Martin: [i disagree with Anne]

[Return undefined from side-effect-causing functions.](https://github.com/w3ctag/design-principles/pull/500)

*we review the comments and reviews and agreet to **merge**.*

[First stab at #289](https://github.com/w3ctag/design-principles/pull/501)

Martin: prefer not to do this one - 

[Prefer composition](https://github.com/w3ctag/design-principles/pull/504)

Lea: I agree with fundamental principle but the platform doesn't provide any good way to do composition. Which is why many patterns use inheretence. 

Martin: point of the principle: use inheretence where it makes sense but otherwise make the thing a property.

Tess: "stop violating" 

Martin: I agree the platform doesn't have great ways of dealing with this.

Lea: I think fundamentally you want to use inheretence when it's a kind of the other thing... and composition when it's not fundamental to the identity of the object... 

Martin: could we take this text on and do a follow-up?

Lea: it seems we have consensus - so I have some reservations but fine with merging.

*we review the comments and agree to **merge**.*

[Text formats are for people](https://github.com/w3ctag/design-principles/pull/505)

[other text formats PR](https://github.com/w3ctag/design-principles/pull/472) does a similar thing. We should merge the two. -> breakout

[New text for guidance on exposing interfaces everywhere](https://github.com/w3ctag/design-principles/pull/510)

Lea: I'm comfortable one direction and less sure other direction....

Martin: I think this is a real solid piece of advice as it is...

Jeffrey: I think we can revise it if a counterexample shows up

Tess: I don't think we should hedge it

Peter: point about the event loop is good

*we agree to **merge**.*

[Add principle on use of delta seconds](https://github.com/w3ctag/design-principles/pull/467)

Martin: there's a more general principle about how to use time in apis but it isn't this

Jeffrey: appears in json too it's not just http

Martin: I made a comment about the computers of the web not agreeing about the current time. it's a bit much.

*we agree to close*

**CSS principles in DP**

Jeffrey: We have several open issues on CSS principles. We're losing all of our CSS experts.

Lea: we need collaboration with CSS WG. We should always be engaging industry experts.

Peter: we're not dictating principles to the CSS WG we're documenting ones they already follow

Lea: and to ensure architecture principles... individual groups maintaining them doesn't accomplish that. We need the domain expertise that we don't have, and the architectural sense of the TAG.

Martin: flip side - if we are presently competent to put them in and won't be in the future we should put the outstanding issues in

Peter: if they go stale CSS WG can file an issue or a PR to update

Matthew: is our relationship with WHATWG working?


[New principle: Incorporate from existing CSS Design Principles](https://github.com/w3ctag/design-principles/issues/490)

Assign it to a breakout..

## Day 3 - 4 December 2024

### Ethical Web Principles

*We discuss the report from Max and recognize that it's not meaningful for TAG to record a consensus - but rather individuals on the council should reply to request for consensus on the draft report.*

### Session 6 : Working on Design Principles Issues and PRs

#### 6a

Present: Yves, Dan, Jeffrey

**[I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454)**

*yves working on a PR*

Yves: raised [PR](https://github.com/w3ctag/design-principles/pull/517) and asked for clarification 

**we agre to merge - jeffrey to action**

**[A Promise represents completion or a value, not a callback](https://github.com/w3ctag/design-principles/issues/496)**

*jeffrey working on a PR*

Jeffrey: That PR should be rejected - and we should do changes in other PR...

**[powerful features](https://github.com/w3ctag/design-principles/issues/481)**

Jeffrey: the only time we talk about powerful features is user activation... In WebAppSec, Mozilla in general likes the idea... maybe chrome is hesistant.  We could request a change to their doc requiring user activation or we could change our doc to say "some"... 

Dan: currently they are not talking about activation... [in their doc](https://www.w3.org/TR/permissions/) so that seems like a problem considering we recommend user activation.

Jeffrey: their issue [194](https://github.com/w3c/permissions/issues/194) proposes to deal with activation in permission...  There's a draft PR [401](https://github.com/w3c/permissions/pull/401)...  

*jeffrey leaves a [comment](https://github.com/w3ctag/design-principles/issues/481#issuecomment-2516706416)*

Dan: We should [encourage web app sec to bring this to CR](https://github.com/w3c/permissions/issues/454). I would like to link to their draft.

"In your specification, a good way to ask for consent is to use the approach outlined in the [Permissions guidlines document](https://www.w3.org/TR/permissions/) produced by the wonderful people in the Web Application Security (WebAppSec) working group."

*We discuss the idea of removing "consent" from 1.4 but land on keeping it to keep this clearer.*

Dan: Creates [PR 519](https://github.com/w3ctag/design-principles/pull/519)

**MERGED**

#### 6b

Present: Martin, Amy, Peter

**[Privacy tradeoffs](https://github.com/w3ctag/design-principles/issues/511)**

Martin: came from web fonts

Amy: feels like not a design principles issue - read privacy principles

Peter: It's fingerprinting vs cutting off an entire community from the web

Martin: suggestion that showing more prompts would be a possible way to deal with this. Browser detects the page has a bunch of things that rely on web fonts, doesn't render the web page, shows a thing taht says 'looks off?'

Peter: unless you're explaining what the tradeoff is you're not helping the user

Martin: blunts the most obvious attacks. Hard question, no guiding principle?

Peter: browsers should ship with the right fonts

Martin: what Anne said

Peter: that helps this problem, not in general

Amy: there are two issues, general, and the font one. Two tier thing here - if you are part of the mainstream web users you get to have privacy but if you have literally any other needs then you don't. I don't think we want to embed that.

Peter: the solution here is to ship all the fonts

Martin: a finding: ship a font that covers all the languages, and don't use locally installed fonts.

<blockquote>
  Discussed in a breakout: We concluded that this particular issue has a solution that does not require that we trade off privacy against accessibility of content that uses less popular languages.  That solution is roughly along the lines @annevk outlines: ship a font that has glyphs for as many human languages as possible and don't use locally-installed fonts.  For example, the Noto family of fonts attempts to do this and the number of bits that those fonts requires is large, but manageable on relatively modern computers.
  
  The general topic is not one that readily submits to general advice.  Sometimes, there will hard decisions to make where privacy is in tension with other goals.  The details of the situation will dictate the options in ways we cannot predict.

</blockquote>

Dan: do we need to follow up with Chris L? The TAG's opinion is that browsers should ship all the glyphs.

Martin: *does so*

**[HTTP Headers](https://github.com/w3ctag/design-principles/issues/512)**

Needs homework.

**[Link errors](https://github.com/w3ctag/design-principles/issues/484)**

Overtaken

**[Method args optional](https://github.com/w3ctag/design-principles/issues/437)**

Martin: intro is correct. What is wrong is "default value used is the same as converting undefined to the type of the argument" - strike that

Peter: might be a webidl thing?

Martin: already references 6.4 optional arguments provided through dicts which is nice

Martin: for boolean values the default values should be False

Peter: I thought we had that advice

Martin: we don't have advice on anything else. Numeric values, certain cases a sensible default wuld be 1 not 0

Peter: leaving it out you're passing undefined, so the code should detect undefined and conver that to 1 vs specifying the default value is 1

Martin: does js go there if someone passes an explicit undefined?

Peter: if I define a function in js with a default value and don't specify that value at calltime, I do get the default value as the argument?

Martin: yes... not the same as js function you define. You get undefined. You go searching for the value of the arg and it doesn't... oh there is a default value .. unless someone calls it with undefined explicitly

Peter: you get what you ask for

Martin: we can probably replace this with in boolean values should default to False. Mentioned in 6.4. We can move that. Move the see also down to 6.5

Peter: the boolean trap belongs in 6.4

Martin: yes. I'm talking about second reference

Peter: yes

*PR 518*

#### 6c

Present: Tess, Matthew, Hadley

##### "HTML attribute" as a term [#495](https://github.com/w3ctag/design-principles/issues/495)

We agreed that "content attribute" (the existing term) should be used.

Matthew to make a PR.

##### Assistive technology emphasis adjustments [#498](https://github.com/w3ctag/design-principles/issues/498)

Definition: https://www.w3.org/TR/WCAG22/#dfn-assistive-technologies



hadley: 
I propose that we use agreed comment. I think we should then open a separate issue to remove "without the user's consent" and add the reference to WCAG (if we're going to use it) for our own reasons. I don't think either are actually responses to Nigel's comment, they are just things that have come up in the process of discussing it. 

hober: That works for me!

Matthew: I was gonna suggest a separate issue for the definition - just so I could have time to read it. Just looking up the proposed comment.

I agree with all edits - WFM!

I was gonna suggest the first edit as a next step. All are good though IMO, thanks!

Hadley: Great. Commented and closed. And new issue filed: https://github.com/w3ctag/design-principles/issues/529

#### 7a

Present: Max, Martin, Peter

[#488](https://github.com/w3ctag/design-principles/pull/488)

martin put in a PR to change mime type to media type... 

Disagree with Anne about which terminology to use.

Tess: web platform specs reference mime

Martin: we also reference ietf specs for a lot of definitions..  having different terminology for the same thing because it collides with something else in a different domain is wrong..

Tess: taking as given that ietf and web specs are already using different terms. Why would we as the web TAG not use the web term

Martin: there shouldn't be two terms ... MIME means nothing

Peter: it has no relation to the web

Tess: neither term does

Peter: media type does ...

*naming is hard: discuss.*

Dan: I'm worried in changing it we might confuse people. List both?

*no consensus*

[Terminology..](https://github.com/w3ctag/design-principles/issues/479) - [PR to fix](https://github.com/w3ctag/design-principles/pull/525#pullrequestreview-2478634015)

Jeffrey: information implies personally identifiying..

Martin: now you've made it just about the device, but it's not just about that. Eg. LLM running in a cloud. Wanted to cut that back

Peter: identifiable, if you have access and which one

Dan: identifying information about capabilities available to the user? Would be more clear, to Jeffrey's point about differentiating from PII

Martin: context is enough?

Jeffrey: delete 'identifying'?

#### 7b

Present: Dan, Tess, Amy

**[embellishments](https://github.com/w3ctag/design-principles/issues/493)**

Tess: view transitions .. I think Peter raised a concern that it was easy to use view transitions and inadvertantly disable incremental rendering of the page.. I don't know if it's true. Concern was view transitions are neat but nothing should break if they don't happen. That isn't important enough to break more foundational stuff. Incremental rednering during pageload is a feature that distinguishes the web from other platforms.

Dan: but trasitions is an embellishment .. that's a value judgement

Tess: based on assumptions we made at the time but I don't know if they're true. How big of a footgun is it? Do we need to do anything? Needs research?

Dan: can we think of other examples?

Tess: there's a no data loss css principle. When we add new features to CSS that might casue something to be hidden from the user that should be visible we should do it in a way where information isn't lost

Amy: leave the web better than you found it

Dan: we have it in design principles in CSS

Tess: might be good enough. Not breaking a more important thing to enable a less important thing

Dan: extra text to leave the web better than you found it

*we discuss possibly adding a sentence to https://www.w3.org/TR/design-principles/#leave-the-web-better*

<blockquote>
As you add new capabilities to the web platform, do so in a way that improves the overall platform, for example its security, privacy or accessibility characteristics. The existence of a defect in one part of the platform must not be used as a license for adding or extending such defect into new capabilities and thereby further decreasing the overall platform quality. Where possible, build new web capabilities that improve the overall platform quality, and do not degrade existing capabilities without good reason.
</blockquote>

Dan: creates [521](https://github.com/w3ctag/design-principles/pull/521)

Dan: can we merge this and move on?

*consensus to merge*

**merged and agreed to close issue 493**

**[utf-8](https://github.com/w3ctag/design-principles/issues/322)**

*we review the isssue - there has been some less-than-helpful dialog, however this appears to be an important issue that we might want to action in https://www.w3.org/TR/design-principles/#new-data-formats*

Tess: the whole point of WASM is to take legacy code ..

Dan: not sure it's justa bout legacy code. A lot of people will write real code

Tess: the code inside wasm is probably assuming utf8. JavaScript strings are not UTF-8. That's unfortunately exposed to ... sending text between wasm and js you're going to constantly have to do encodes and decodes .. and that's just how it is. This is still the right change. Maybe lament the fact that people doing text manipulation on the wasm side are going to have to do some conversions, but that ship has sailed

Dan: the platform should be doing that for them...

Tess: but we don't say that here. But Dom is correct. Add a sentence to 10.3. "... new text formats should be only in utf-8". The problem with this principle as written is that it's just about media types. This new sentence is not. The name is generic sounding. The actual text is about mime types.

Amy: *Writes [524](https://github.com/w3ctag/design-principles/pull/524)*

**[497](https://github.com/w3ctag/design-principles/issues/479)**

Anne reviewed positive *merged*


#### 7c

Present: Jeffrey, Yves, Matthew

##### "while a JavaScript event loop is running." is probably not intended [#456](https://github.com/w3ctag/design-principles/issues/456)

Jeffrey is working on a PR with Jake Archibald's proposed text.

##### New principle: Patterns for URLs in APIs [#303](https://github.com/w3ctag/design-principles/issues/303)

The issue this was spawned from is discussed in https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/04-12-minutes.md, but there's no sign of what problems Sangwhan wanted to solve with guidance here.

It's hard to search the platform's WebIDL for parameters taking URLs. There appears to be a pattern of calling things `url`, `urls`, or `[purpose]URL`. Filed https://github.com/whatwg/webidl/issues/1454 to see if we can make this search easier in the future.


##### New principle: A Promise represents completion or a value, not a callback [#342](https://github.com/w3ctag/design-principles/issues/342)

This should probably be part of the run-to-completion section (see https://github.com/w3ctag/design-principles/issues/456). The timeout is aimed at avoiding user surprise, which is usually the same purpose as the [transient activation duration](https://html.spec.whatwg.org/multipage/interaction.html#transient-activation-duration). We should include transient activation as an exception to run-to-completion, like `Date.now()` is an exception, and then see if the WebRTC folks can just use that.



### Discussion of Security & Privacy Questionnaire

*We discuss the situation with the Security & Privacy questionnaire and **agree** to hand this document over to become jointly owned by Security Interest Group / Privacy Working Group.*


### Web as a Commons

Present: Dan, Hadley, Yves, Matthew, Peter, Jeffrey, Amy, Martin, Tess, Henry Thompson

*Jeffrey presents [The Web as a Commons draft in progress](https://docs.google.com/document/d/1Z5PClovDas8yzj4ya759Qf6cFQXVezm6LbSZsqErOX0/edit?tab=t.0)*

Dehumanising to talk about people as a common-pool resource. Using this terminology for now, as it's in practice how websites see their users, but call it out as a problem.

"Inventory" - what they have to sell. Exit based on the number of users they'll bring with them. Inventory is actually the space on the page, but what is really happening is dehumanising.

Issue with any framing that denies dignity of a human.

Minimising use of 'user'. There are people on all sides, and not all are end users. Visitors? User is okay as long as it's not a replacement for people.

At some point we need to clarify the categories of resources.

Likely other common-pool resources we will need to talk about.

Time instead of staff salaries at the other end. Time as the resource. Takes much longer than it used to to deaal with eg. aspects of financial life, vs having a specliast on the other end of a phone to do those things faster. Feels different from attention and others.

Related to labour in the in the sense of privacy labour. is this tangiental to the commons?

Who the community members are - end users and website authors/operators.

Focus on businesses - proprietor. Social roles on the proprietor side and others on client/user side. Distinction between proprietor and roles within proprietor are important as they have different views about what they're doing.

A question for this work - how much detail should we go into?

Proprietor side stuff in one bucket - many sites, esp social media, 98% of traffic is from user generated content. To call twitter the source of tweets is wrong.

More analysis needed. Feels too coarse currently.

User generated content fits into existing commons analysis about wikipedia and open source. THe same entities creating and using the content. Except the content is also exploited by third parties.

For many end users the value proposition is not what they're getting directly but that they're getting exposure/kudos within a peer group or reputational value which they later individually monetise. 

Social networks act as "third places".

Reasons authors produce content

Provision - teaching people to use the web, browsers, search engines.

Appropriation problems - if extraction is too high it drives people away.

Something about search engines aren't the only way people get into the web. There are still URLs in print advertising. 

Search engine as a "user agent". Positive and negative examples. Also appropriation problem.

Ubiquity of the web around people also cultivates people into becoming web users.

Browsers disappearing from the visible usage chain. 

There are no collective monitoring on the web as there is in commons discourse. This is about websites monitoring each other, not users defending themselves. More sustainable when the appropriators monitor each other.

Incentive to capture with central monitor. Exploit competitive nature of system. Appropriators can be in community with each other and discuss rules and governance so they don't overexploit. In the material commons, the resource doesn't have an ability to defend itself.

Mastodon instances as an example of self-monitoring.

We don't want to say don't install adblockers but there's some problem with doing it too much.

Default of do not track - rhetoric around default being off was the expected distribution of users that would enable it. People don't change default.

As ad blocker percentages go up you see sites retaliating against people who turn it on.

Secondary community - browsers, search engines, llms. Entities which help users overexploit website. Box that stops people from clicking through.

Secondary appropriators - adtech. & surveillance - they may or may not be useful to the commons

Physical infrastructure. Net neutrality? Distinction between internet and web as commons. NN is internet. AFfect each other.

Polluting the commons deliberately - is this missing from here so far.

Existing researchers think the biggest question is about authenticity and correctness. 

We don't necessarily need to getinto knowledge commons questions like correctness.

Knowledge commons is the category of research that includes everything other than natural research commons. Do we need a narrower definition.

Proliferation of JS related to this? The user is also providing computational and bandwidth reasources. Another cost to user, environment, commons as a whole. When websites don't care about their payload they're abusing the commons - shifting the load from their servers onto billions of users. All those devices is part of the commons.

Design principles level statements that can be drawn out? Architectural guidance?

Third parties that act on behalf of one of these categories as a thing? CDNs, data brokers

ISPs as user agents (not necessarily good ones)

How does this work turn into action?

Similar area to EWP. Produces questiosn that should be asked of any proposal.

What do we notice? Collective monitoring and sanctions. A research project and standardisation project to spin off.

Fodder for finding alternative funding mechanisms for the web. Web is a common good public resource funded through late stage capitalism and we want regulators to think about ways to shift that model. reframe the questisons regulators are asking. Stop thinking about web as owned by giant corporations.

W3C to take a policy position on this? Might be more appropriate than TAG taking a position. We can talk about webarch as being built around this idea of the commons, so requires a level of regulation that has not existed yet, and we need to be asking for that.

Societal Impacts questionnaire connection. How to align these?

People who visit websites can in theory fight back - but they can't much. No alternative to the web. Coersion.

Human Rights UN people at Hiroshima would love this. Need to express this in terms regulators are going to be into.

Would require a significant amount of upskilling on the part of regulators to act responsibly in this area. Misguieded or malicious actions.

When governments interfer with self-governance they tend to break commons - in existing research.

We have to be careful asking regulators to intervene.

Commons research has a lot of arguments about polycentric governance, people closest to the work. If we situate ourselves in the commons academic tradition, that gives us a background to say this is governance.

Defend against bad regulation by saying we're looking for regulation as a commons, not something that can be used for these purposes.

nb. not all regulation is bad regulation. Eg. cyber resilience act in europe has had positive impact.

Regulation issues can come from wrong part of government, or regulation from wrong perspective. 

Regulators are already poking into the web. We want them to know the structure and understand what they're going to break.

Easier to argue with a concrete alternative proposal.

"We study the web so we don't break it by mistake" -- timbl

Is this a two part thing - documentation of how it is, and some way sit might be improved? Start with how it is. Then action.

What needs to change in this doc before we're ready to share with academics?

Broader engagement? With commons experts?

Find someone to do a PhD on this. ISC Conference in June. CfP is closed. But we are special. Could attend.

"Stop exploiting the web" finding - but framed as "web as a commons" ... we could publish something quite small and comparatively quickly - that leans on this work. Buttress it later with academic involvement.

q+ to reinforce "web has always been a commons"...

We got people on board with EWP by reinforcing the point we've always had ethical principles, it wasn't novel. We can say the same thing about this - we've always had these principles, we're just documenting them.

"This is for everyone"

A TAG finding should be in the language of people who understand the web. - not academic jargon.


### Additional Design Principles PRs

Present+ Max, Lea

Martin: *discussion on [505](https://github.com/w3ctag/design-principles/pull/505)*

Lea: allowing ... doesn't guarantee that formattng is easy for humans ...

Martin: important to focus on *why* sentence I suggest is ... 

Lea: *makes a good point*

Martin: follow up with DRY and 

Lea: have opened an issue about not writing more code than is needed #473

Tess: question about this PR - flexibility is for authors. Not for spec writers. The way we enable author flexibility, eg. CSS's error recovery, is flexible to the author, but rigidly and precisely defined by the spec. Worry if we don't at least mention that in passing ...

Martin: I do. That's the proposal here. Easier to author and prodcues consistent results

Tess: works for me. Cross ref the bit later on in the document that says be precise. Specify completely and avoid ambiguity.

Martin: will put reference.

Lea: whitespace ... specific examlpe in mind.. not repeat mistakes of JSON

Martin: and html, which is flexible. Favours authors

Lea: document what a human readable and editable format is here? We're incorporating all of our other principles.. so many others apply. Incremental user erffort:value ... any specific advice we give in this section should really be a separate principle if we don't have one. The opint this principle is making is it should be a consideration that text formats should be human editable and readable. How to make them so is to read the rest of the principles.

Martin: I think I agree

Lea: if we start having specific advice in here it implies this is it. Maybe we should cut this down and poitn to the rest of the document about how to do that.

Martin: I don't think wer'e there on the rest of it. Talk about those other things as follow ups. We have an open issue on the incremental user effort thing which is a good separate thing. A lot of our principles are exactly like you describe. They focus on one class of thing and connect to a whole bunch of other things. It's useful to have a focus point for someone who is thinking about the difference between textual and binary formats

Tess: good sign this principle maeks you think about what might be elsewhere in the document. Suggests the document is cohering.

Martin: we can fix a see als

Tess: what would you remove to shorten this text?

Lea: the thing about flexibility and whitespace ... people epxect some amount of flexibilitiy... all ofthe advice. there are two points to keep: it is important to consider humans when designing text based formats. Point 2 is do these things to accomplish that. The latter is overlapping with other principles. The entire document is about making text based formats readable to humans. Instead of specific advice we should have the examples and link to othe rprinciples. Eg. here's how these principles apply here. Rather than repeating or embedding principles.

Martin: this stuff isn't elsewhere in the document.

Tess: I think your instinct toward brevity is admirable but what you just mentioned would remove the meat from the principle.

Lea: eg. syntactic flexiblity should have a separate principle if we think it's important

Martin: dont' disagree. Can we have a follow up?

Peter: a lot of this content doesn't exist yet. We're fine expanding some of these things into their own principles. But we either need to do that first, or land this and do that later. If we just remove this text without having the corresponding text elsewhere in the document we've lost the meat of this.

Tess: right

Peter: we're agreeing with the goal. We're proposing to do that incrementally for the bits that don't have existing principles.

Martin: looking at 473 with incremental value. that's great. We should write something on that. It will probably take some of the text out of this as a result and expand it. Right now we've got nothing.

Lea: it's not just that. The priority of constituencies apply here as well. Often text based formats are designed to make them easier to parse rather than for humans. 

Martin: not contradictory. Something more concrete to say? It's a follow up

Tess: the text should reflect the expected usage mode of the document. We expect people to receive a link from somebody else: "there is this principle you should follow" You read the principle but not the rest of the document. The text of the principle should be sufficiently complete to be actionable. I'm afrad that if we factor the content out sothere's too little left then the utiliyt of sending someon a link to this principle diminishes

Peter: we could fix that by every time we move that into a different principle we can replace it with a see also bullet

Tess: that presumes we land this first

Lea: first making the point it's important to consider this, then eg. link to the priority of constituencies. When we merge user effort principle, point to that. There are a bunch we can link to and two we don't have. If you want to merge this and have seprate issues to create principles for these.

Martin: Iv'e got two based on what you said. There are probably more. #473, prioritiy of constituencies, optimising for authoring not parsing, 

Lea: filing an issue now about ones to split out.. common things easy and complex things possible ... prefer ismple solutions. Tradeoffs between high and low level. Simplicty applies. Guidance there now murks the point of the principle. Worried people will tick the syntactic flexibility and error handling and think they're done

Martin: not convinced. When someone is trying to do a good job they'll say they've addressed all of these things, but what else do I consider to do a better job. If they're not reading it they're not there anyway.

Lea: we should link to thinks. Sounds like you have consensus.

**merge 505 and close 472**

Martin: I will get other issues open.

**[TAG alum](https://github.com/w3ctag/design-principles/pull/530)**

**merged**

**[Restrictions](https://github.com/w3ctag/design-principles/pull/363)**

Martin: it's missing the 'you should do this'. It's a useful index of the restrictive capabilities but doesn't contextulaise it

Jeffrey: still has a todo in the text

Lea: not ready to land

**[Element overloading](https://github.com/w3ctag/design-principles/pull/502)**

Martin: didn't follow up on some of this. legend caption and figcaption as same element. Sure but brevity. Link as another example..

Lea: adding another example is not a blocker for merging. Leave a comment.

Tess: Anne left a comment about adding some nuance .. input element as example. Discrimination based on type attribute was a hideous mistake and we're all very sad about it but we shouldn't slam the door completely shut on making small enhancements to input. There are cases eg the switch control which are arguably preferable

Lea: the reason input is such an antipattern is because the different modes require different api surface. Applies to some modes and not others which creates mode errors - where users make mistakes because they think theyr'e in one mode and actually in another, so discouraged. This is the same thing but applied to syntax. Attributes that only apply when other attributes are present. Same thing in CSS. a property that only works when another propery is set that leads to confusion. If the api makes sense and you just need a different presentation like switch then it's fine. Problem with input link is that you have to add all these different properites and attributes. That's why caption figcaption and legend should have been the same element, no different API surface.

Martin: don't know that Anne's input needs to text to address it.

Tess: reasonable worry that someone would interpret the text to mean we need never add anything to it ever again

Martin: I don't think it says that

Tess: this is an improvement.

Martin: *force push*

Peter: you broke everything

Martin: *force push again*

Peter: that's better

Lea: I filed a new issue about this #532 to track

Martin: that's good if we resolve that properly it will improve it

*ready to merge*

Hadley: *merge*

**[New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)**

Lea: conflict between whatwg and tc39. TC39 follows namespaces. We have examples on the web platform where functions that belong to the same api are thrown into gloabl scope. file system api - showopenfile picker, show directory picker ... we did a tag review and didn't spot that. Structured clone. And others that are very specific. I think we should advise against it. But Anne and Dominic disagreed.

Dan: what can we say that everyone will agree to? Consider these factors when thinking about how to expose.. align with other things ..

Lea: there has been a long thread but no other TAG members have expressed opinions. We might have consensus in TAG

Tess: we don't

Jeffrey: I lean toward Dominic

Tess: so do I

Lea: do we agree that what the filesystem api is doing was a mistake

Tess: I don't know

Jeffrey: I think there's decent arguements both directions. The names that the filesystem api is using are clear names that lead well and calling it filesystem.somethingShorter would read less well even though it would be easier for autocomplete to deal with. I don't know what the rule would be that would help api designers pick between them.

Lea: I don't htink that having a shared namespace means by default it has to be longer. createimagebitmap could have been imagebitmap.create which is the same. Concise names are important, rather tahn throwing multi word names into the global scope. Doesn't mean we add a namespace in front of existing names. 

Tess: concicese naems aren't importatn - clear names are important. Sometimes longer is clearer.

Lea: namespace is part of the name

Martin: adding a namespace creates context that you can use to make the other part of the name ..

Tess: shortening the bit after the namespace can create confusion not ..

Martin: Lea's example of createimagebitmap is a great one

Jeffrey: plausible principle that when there's something .create there could be patterns like this

Tess: appeal is it's consistent with other platform features

Lea: it's not just factory methods. reportError - why wouldn't that be error.report? it's the same length and benefits of namespace which adds context. Usually you can have one word names with additional context of namespace.

Dan: What burning fire is related to this principle? Are there design decision being made we know of that somebody is doing it the wrong way

Lea: several listed. Main concern is if we don't have a principle it's easy for us to miss it as well

Peter: there are two different groups following two different principles is a problem. However if we can't get those two grops to agree. Personally I have mixed feelings. I like namespaces because I think polluting the global namespace has a cost which isn't always factored in.

Jeffrey: consider whether your thing should be on a namesapce?

Peter: yeah, even saying avoid doesn't say never or don't

Tess: consider is useufl. The examlpe of imageBitmap.create .. suppose imagebitmap didnt already exist but the other create factories did. Someone following this principle would look for othe rthings to be consistent with

Dan: this was my point

Tess: the platform that exists now is inconsistent. Don't make the inconsistency worse. I could live with a principle written in that way that didn't take a stance on the question.

Dan: documenting the current stance is useful

Tess: strive to be coherant with the platform..

Amy: don't we already ahve consistency

Martin: I'd like a better principle than that

Tess: better than nothing

Jeffrey: it helps because createimagebitmap example, if anyone had thought about it .create would be clearly better.

Martin: that's a principle

Jeffrey: maybe we can say that kind of thing. Still disagreement about filesystem and report error but at least we'd be more likely to remember to discuss it and look for an argument one way or the other

Lea: agree it's better than nothing

Dan: who wants to write it?

Peter: no problem with watering down the topic.. but we shold give some kind of guidance as to why you'd pick one vs the other. consistency is a factor, but the lowest one. Sometimes we've done something in two different ways and ew've decided this way is better so new things should follow that ... but someone could argue to be consistent with the old way becuase ther eare more. We want to add here and deprecate those later. Should have the path to improve. Consistency is important but not above all else.

Martin: we have the naming principle. That applies in both directions. We have the "if you're making an instance of an object or operates on an object, make the function on that object, which points towards global namespacing." What points to unnamespaced?

Tess: frequency - fetch. core functionality that you do all the time.

Peter: fan of namespaces. But object.key and object.value is probably going too far.

Martin: yeah, the structured clone example I had trouble with .. object as a namespace for functions that work on objects ..

Tess: everything is an object

Jeffrey: we have map. things that are also an object .. a lot of the things getting hung off object are not common operations like hasOwn

Peter: every time you put something on the global namespace you're optentially polluting it. One function that makes sense in global namespace today. next year three more similar ones that all belong in a namespace. if only I'd put them in a namespace in the first place. like file picker. That's why i tend to lean towards namespaces. But I seee the point that sometimes they're annoying.

Martin: that's potentially another thing to say. three, four, five dots is not a good thing. If you have a namespace you've only got one. One should be enough.

Matthew: seems like some agremeent.

Peter: what the tradeoffs are to consider. A collection of like things, consider putting them in a collection. If it's a small collection or the things in that collection are relatively disparate. filepicker things are quite different, conceputually adjacent but not enough to gropu them

Lea: consider the namespace as context for the name so peopel don't end up adding really long names as if the namespace didn't exist. That's a lot of the concern against namespaces.

Tess: filepicker case is an illustrative one. What would the namespace be? picker.file()?

Martin: I can't think of one, so no

Dan: document the controversy

Tess: definitely cases where most people would agree we messed up. Low hanging fruit. Stuff with active disagreement about wether we messed up or not - don't use these as examples.

Martin: talk about the simple ones

Tess: intl is an example for consistency, even if it was a regrettable namespace.

Martin: if you create a bucket, the things in the bucket need to be logically consistent. if the bucket exists, use the bucket. Media devices might be less controversial. Probably a mistake because there are only two things in there. But if you're going to do thing swith media deivecs you do it in that bucket now.

Tess: fetch as a counterexample. We didn't replace xhr with xhr.fetch

*ACTION: Tess to draft in a couple of weeks*


## Day 3 - December 5th 

### Finding that defines a user agent

Jeffrey: we could take the text from the privacy principles - and that text could be taken out of the privacy principles

Hadley: a list of points - 

* the user agent serves the user, not any of the other constituencies
* RFC8890 - Internet is for people
* user agents should not be used for tracking
* we expect the user agent to: separate concerns (not leak info between tabs) strict origin-based separation / same origin policy. Duty of Discresion
* user agent's relationship with the operating system - sits on top of and may take advantage of the capabilities of
* the user can choose the user agent that works best for them? (no consensus)
* browsers, LLMs, search engines, [assistive technology](https://www.w3.org/TR/WCAG/#dfn-assistive-technologies)
* apps are a kind of user agent (webviews count)
* voice assistants are a kind of user agent
* rights and obligations
* user agents can take many forms such as ... (not just browsers)
* the user trusts the user agent, but doesn't have to trust websites and external traffic (must be safe to visit a web page)
* you also trust the browser because lots of researchers and developers are checking it, looking at what it's doing, checking open source code, etc.
* user agents can be but are not necessarily open source
* something about heuristics (extra-standard browser behaviours)
* browsers have a bunch of standardised activities and then a lot of specific features ("secret sauce")
* UA choose which standards to implement
* INFRA definition of a UA

User agents compete by how they differ: offering different feature sets, security models, UI, etc. 


#### UA finding outline 

One line summary: user agents serve their user. 

What they are
* browsers, LLMs, search engines, [assistive technology](https://www.w3.org/TR/WCAG/#dfn-assistive-technologies), voice agents
* apps are a kind of user agent (webviews count)
* user agents can take many forms such as ... (not just browsers)
* something about heuristics (extra-standard browser behaviours)
* browsers have a bunch of standardised activities and then a lot of specific features ("secret sauce")
* UA choose which standards to implement
* INFRA definition of a UA

How the ecosystem works
* user agent's relationship with the operating system - sits on top of and may take advantage of the capabilities of
* the user can choose the user agent that works best for them? (no consensus)
* the user trusts the user agent, but doesn't have to trust websites and external traffic (must be safe to visit a web page)
* you also trust the browser because lots of external researchers and developers are checking it, looking at what it's doing, checking open source code, etc.
* how users trust user agents: user agents can be but are not necessarily open source 

Rights of the user and obligations of the user agent
* the user agent serves the user, not any of the other constituencies
* user agents should not be used for tracking
* RFC8890 - Internet is for people
* we expect the user agent to: separate concerns (not leak info between tabs) strict origin-based separation / same origin policy. Duty of Discretion
* excerpt from the Privacy Principles

### AI finding

*we review some notes*

Martin: *notes that there is IETF work coming up, on the basis of a recent workshop, on refining how to sign-post how data can be used - as training data, etc... - expanding from robots.txt, but also including other mechanisms*  https://datatracker.ietf.org/doc/charter-ietf-aipref/

Amy: recommendations here... should this be framed as an observational finding?

Jeffrey: i think we should say some things about how AI works

Amy: we could talk about it in context of each of the ethical web principles

Amy: my initial reaction to this text was surprise that it is so positive

Jeffrey: My slant is to write crietria that a theoretical AI system could meet but that current AI systems don't meet

Dan: something something transparency of rights ...

Jeffrey: it should be able to cite its sources...  It could be that LLMs are not sufficiently AI to satisfy these requirements... but we should write requirements...

*discussion of Open Source licenses in LLMs*

*discussion of attribution, attribution stacking, and copyright*

Peter: a concern with the AI finding is that the term AI is meaningless - yet doesn't bind the person making the claim to any specific meaning.

Hadley: yes and .. serves us better to get it in front of people

Peter: we could say something about the term AI itself...

Max: regarding technology for AI - there is already some standards - e.g. ISO standard that defines terminology - defines what is an LLM, what is machine learning...   But not public...

Peter: I agree there are reasonable definition for GenAi but AI iteself is a blanket term that has no meaning.

Jeffrey: we use "AI" to capture... and put requirements on them.  

Yves: "Anything that needs training based on data"...

Hadley: but sometimes it's just used for a dumb algorithm

Amy: three databases in a trenchcoat

Peter: I'm not opposed to using the title, but I don't want us to use "the AI" or "an AI"

Hadley: so where does that leave us?
  
Martin: with something hugely unfocused.t With something outside of our expertise and something within our domain.

Amy: if we refer to the EWP, we can say "here is the stuff to talk to sociologists about"

Matthew: we could say "these are the things we, as technical people, don't know"

Amy: it's reasonable for us to remind everyone that the web is a sociotechnical system

Dan: that sounds like a finding. A statement that could be useful for our AI finding, user agents findin, etc.

Amy: it's the principle behind web sciences as an academic field.

Max: *https://www.iso.org/standard/74296.html*

Dan: I think it's useful to use the same tenor Dom used in his Team document. 

Hadley: yes, we were looking to cite his list of potential standardisation efforts

Martin: one of the things I'm looking for a slice of the domain in which we have expertise and experience in which we can make a statement that will have a positive effect. 

hadley: we could put a lot of effort into defining those terms for the web, but I don't think it's useful

Martin: no

Amy: There is a design issue on AI from 2017 https://www.w3.org/DesignIssues/

Matthew:
Don’t assume that the way you’re using this right now is always the way you’re going to solve this now.
Allow the user so that filter so it can only be run on-device, or 

Jeffrey: there is the question of 'is this technology ready to run in a browers?' and that's what I want this finding to solve.

Peter: is your business model a permanent part of the web? "Here's an api for an LLM", I want to be able to say no, your LLM isn't good.

I'd llike to see this finding have some broad statemetns and focus on specific LLM technologies. They're the new shiny thing. People are just throwing LLMs at everuything, and they're not suited to task 90% of the time. They don't do a good job. Yet it's what everyone is baking into everything. I'd love to have a finding that says "stop it".

Amy: can we put our review requests that requires people to fill out the societal impact questionnaire?

Peter: People are doing terrible things just to power an LLM data centre. If we encourage this to be built into the web, we are responsible for that.

Matthew: if it's this much of a marketing thing, do we just wait?

Yves: when someone has assistive technnology that takes an image, generates a textual version of that image... It's hardly possible to do it locally. It has lots of implications on privacy. The consent the site gave to a user agent and not to an LLM model, is it transferrable? If I say, "My picture, I don't want it to be used by an LLM, but a user agent can read it"

q+ to +1 the societal impacts questionnaire

Jeffrey: the folks researching this are doing stuff that is not exactly LLMs, and may be out of scope if we are too narrow. 

Peter: agreed. LLMs are an example of these problems.

As soon as we can do this stuff without terrible environmental impacts, and have technology that actually WORKS

Dan: if we came up with a finding that says "AI bad", no one will listen. And I"ve been thinking about focusing on a positive light. I've been thinking about threats and harms and mitigations and how to draw positive outcomes. Just reinforcing Amy's point about societal impacts, maybe we should be refining that? Today? 

Peter: my concerns go beyond the energy and resource requirements. But also, it doesn't work! It doesn't do what it says on the tin. I think openAI is one of the biggest grifts in society right now. I think it's a con, a means to extract money from VCs and beyond.

Beyond useless, it's actively harmful. Job applications now run through an LLM, qualified candidates tossed out. 

Amy: I've been on the other end, received thousands of applications.

Matthew: +1 to societal impact questionnaire. What do we want to get as the impact of this document? 

Martin: this could damage the reputation of this organisation as irrelevant. I largely agree with the potential for harm, it's enormous. But saying that?

Peter: Even if it goes no further, the harm already being done is unacceptable to me. Welfare recipients being denied benefits, or health insurance claims being denied. These are killing people. I don't think we can stop it, but I hope we can make some statements that will make people stop and think "we don't want to put this in our product." Like: translation engines, there was a whole lot of work that was making massive progress, and now nobody's funding it because all the money is going to LLMs. I'd love to see us say something that would make people go back to these other approaches.

Matthew: you could have a hall of fame of other, better ways of solving problems. Not to do with TAG, but a good awareness-raising thing.


### Ratification for TAG Appointees

*discussion on how appointments work*

### Awesome cosmic power (powerful features)

Dan: there was a discussion in Seville led by Lea and Sangwhan about powerful APIs in the web platform. Things that makes developers of services choose other platforms - many people who promote PWAs would talk about them in the same context - being able to have your services through the web platform you get safety and benefit through the web, safety, performance, ease of use etc.

Jeffrey: disagreement on the TAG about whether many of these powerful features belong on the web. Chromium has one position and the other browsers have a different position. I'm not sure what we could say in a finding that would get consensus.

Dan: Sangwhan and Lea talked about how the TAG should be thinking about the web from a product management standpoint which is another way tot hink about this, which led to the discussion about the gaps. Also a lot of working going on in the Baseline workstream which is about looking at those APIs that do have consensus. Approaching it from the pov of there are a lot of APIs we don't have consensus on... if we looked atit from what we do have consensus on, which powerful APIs are useful that could be a better approach. We have developed some consensus on things like install. Service workers started off like this. Consensus emerged.

... And also guidance that ensures that those APIs don't become too [awesomely cosmically] powerful

Hadley: powerful features / secure contexts from webappsec: https://www.w3.org/TR/secure-contexts/

Martin: that should not be what we use....

Dan: why? A lot of people are using that as bedrock. Can we get them to change it?

Matthew: what Hadley said... there isn't a w3c wide definition of what a powerful feature is. I think we say it's a feature that could cause harm. WebAppSec says it's a feature you have to give permission to. Similar but not harmonised. 

... Powerful features that have sort of consensus on what sort of things they are, maybe that's what we're talking about? Or is there other stuff as well?

... Also we do not have consensus on the raw sockets thing. It's so powerful it only gets exposed to offline webapps. Some might say it doesn't belong in a browser.

Dan: there's a continuum of things. There's a subset which we do have consensus on. If we try to channel energy back to webappsec for that and the permissions draft that both talk about things like this. We did some work yesterday on the design principles to having more coherant link back to the permissions draft. There's a PR on that that's active. That's an attempt to have a more coherant story to tell web api designers about powerful features and permissions and security that should be lined up between TAG and webappsec

Jeffrey: secure contexts doc used to be called powerful features. They had already moved away from it and I stole it for permissons. Secure contexts no longer talks about powerful features. Contains many things dangerous if hijacked. Mozilla believes anything new should be behind a secure context. That's reasonable. I don't think we need to be talking much about secure contexts draft. Most of it is fully consensus. Question is all features or most featurse.

Martin: that's a policy decision you make independant of secure context. The reason we insist on secure context is things that need continuity of identity or server depend on secure context to be secure, but they're not necessarily abou tthe features

Jeffrey: next level is things you need a permission for. The permissions doc says are powerful features. That's not what the discussion in seville was talking about either. I also missed that. That was talking about things like bluetooth, usb, contacts

Martin: filesystem, raw sockets

Jeffrey: that seems like the topic..

Dan: that was one part of it. There was a continuum of capabilities being discussed. There were people promoting that we should be looking at those types of apis and there was not consensus in the room that we should be. there are other apis that may be deemed to be more acceptable than others to be exposed across platforms

Jeffrey; I ran for TAG saying when one of these non consensus powerful features shows up the TAG shoudl be thinking about its characteristics and making an independant decision about whether it belongs on the web platform, nto just saying it's not consensus therefore the more agressive browser is the wrong one. That doesn't give us a document we can write here that is going to get consensus among the tag that says we shoul dhave the discussion for each feature. I have no vision for what document we could write about powerful features in general,t he details matter for each one

Martin: agree. There's a degree of paternalism in the position that says this feature is unsafe under any circumstances. it says we should not be giving the choice to people. I also think that's a recognition of the sort of fiduciary duty the browser has .. you think about someone who acts as someone's doctor. Your physician knows things you cannot possibly comprehend and so will often make decisions regarding those on your behalf that you cannot make yourself. That is true when it comes to these things. I wish it weren't the case but it is definitely the case where some things the analsysi we make as people who are experts in the development of browsers and the web platform might be to deny people the cohice to do that thing. Wev'e doen that with the raw sockets api. There are ways toa ccomplish the ends you actually want - access to email or whatever - that don't depend on creating the fundamentally unsafe thing. We've made that decision collectively consistently as a community. There are other things that are not as consistent. I don't think it is neccessary that the TAG or any sort of consensus organisation should be making the decision. There wil be features for which chrome decides it's perfectly acceptable. Chrome has decided bluetooth is acceptable to ship. Mozilla has not made up their minds on it. I believe the decision is no that's just not safe. For the same sorts of reasons you have for raw sockets. To some extent that's okay that we have a different decision on those things

Tess: it's a space in which virtuous composition happens. We can say our product differentiator is that we don't make this unsafe ... and theirs is that they enable these use cases

Jeffrey: one aspect of the way we did it is we wrote tests so the other brwosers changed their mind they can catch up quickly

Hadley: what does TAG do?

Jeffrey: I don't think there's anything. There might be.. we could say it's good for thes non consensus features to be done in a paricular way or here are the questions to ask, but we need to do more design reviews of them to discover the questions

Martin: Baseline is interesting. To a first apprxomation baseline is saying this is the web. It's nto stuff that's come out of w3c. These are the set of things that everyone agrees is part of the web

Tess: different than the things we think are good ideas...

Martin: very different. Uniformly part of the web and interoperable and shipped and available to people. That is the web. Bluetooth for all we might disagree about it is not part of the web. 

Dan: I don't think that's useful.. exclusionary. I do think we need to embrace baseline. I'd like to include the concept of baseline in our design review system. Somehow. What is yoru route to baseline? How are you going to get this thing into baseline?

Martin: but then we never get web bluetooth in front of us

Dan: the answer could be we don't know

Martin: I don't think that's it

Matthew: I totally resepct the baseline work. it does not include how accessibility supported a feature is. I know they're working on it. If TAG is going to say baseline is important we cannot do that til it supports accessibility

Tess: very reasonable

Martin: yep

Matthew: I would love to help with that.

Dan: is it useful for the TAG to enshrien a definition of powerful features that talks about it from the harms perspective?

Tess: you know it when you see it.. I don't know how to define it beyond that. 

Dan: I'm worried it becomes meaningless because multiple people have different definitions

Peter: it is a nyou know it when you see it. This seems like it's dovetailing into the UA fight... the powerful features that odn't belong on the web are the ones that cede the bounds of the UA

Martin: I don't think so. We fundamentally disagree with some of the decisions Chrome has made. But we think it's more important that they are able to make that choice and to make those capabilities avaiable than the disagreement about the details

Peter : .... guaranttees about operating as a UA

Martin: that's the decision criteria we use

Jeffrey: it's debatalbe, chrome thinks it can

Martin: and you're wrong

Peter: it's still where the line is.. we can debate where the thing fall son the line. BUt we need to agree what the line is

Matthew: interesitng.. agree on the line..

Jeffrey: I don't think we should try to claim the term from permissions. It's not the best term

Tess: the definition in permissions is ducking the question. I don't think we can define a powerful feature as things defined by permissions. Other features not gated can exist. Fundamentaly incorrect to define it that way

Jeffrey: I don't think it will help to define it from the TAG

martin: a different term

Jeffrey: category of things that UAs disagree that shoudl be exposed on the web

Dan: originally there was this document called powerful features. it became secure contexts. Then it became another doucment (points at Jeffrey). Maybe that's a sign people are going to keep talking about powerful features. Maybe turning our back on the term may be the wrong thing to do

Martin: when do we accept that the web is in competition with native

Tess: disagree with that assertion. The reason why powerful features as a term bothers me. There's an implicit premise which is if the web lacks one of these features that is called powerful the web is nto as powerful as it could be or should be. That is ceding ground I'm not interested in ceding in this conversation. 

Martin: bingo

Dan: I don't know if I agree.. powerful features is not necessarily implicitly putting us in a war of apps vs web. I don't agree with that framing. 

Martin: the framing has been used...

Dan: we could still talk about powerful features being ones that reach beyond the content .. the thing you'r elooking at inside the tab

Martin: say what it is

Dan: ...vs things we think .. not necessarily something that you want

Matthew: potentially harmful features

Dan: also footguns, things that create problems. 

Martin: consequential features... 

Dan: we talked about power because with great power comes great responsibility. Lea is a strong proponent on this stuff.

Hadley: risk that they introduce ... risky features

Dan: the other thing is gaps. I put these two things together because .. trying to channel Lea's energy around new features and gaps, to think about the web from a product managemetn standpoint. What do we think needs to be added to the web? what do we think are the problems right now? What are the gaps? Some people might think some of those gaps might be powerful apis, eg. web install. Some people might feel like the gaps are new capabilities in css or new accessibilty capabilities. how do we put more energy behidn the gaps thing? Enshrine that into the work we're doing? is gaps one of these? Brainstorm.

Tess: with my AC rep hat on at a jaunty angle.. I see the ways in which the TAG is impactful... I don't think the AC does. The TAG is an oaapque box we put elected people into and twice a year Dan shows slides. THe gap analysis from that perspective is an opportunity to go to the AC and say hey we noticed there's this gaping hole in the web, or a feature we don't have. Do you all have employees who might want to work on that? Should we organise a workshop? Charter new gropus? An opportunity for us to engage with the AC to not only try to cause work to happen to fill those gaps but to also be seen as thinking about this stuff. Technical leadership.

Dan: send email to ac-forum every so often?

Tess: "during the ongoing work of the TAG considering gaps in the web platform, we've identified a potential work area in x. This seems like something organisations might already be working in and we'd like to talk to your people in that area. There might be standardisation opportunities."

Martin: we identify something through design reviews or patterns of behaviour or discussions, and catalysing the work in that area is one of the more important responsiblities of this body

Hadley: want to avoid a scenario where we point out what nobody is working on, take it to the AC forum and it spawns a month of debate...

Jeffrey: deserves a WG or a workshop

Dan: as TAG we can say we'd co-chair a workshop

Martin: we should be willing to run the workshops

Tess: I'd expect most w3c workshops to be run by the TAG

Martin: I want a workshop on this authenticity question

Jeffrey: That is in progress: https://github.com/w3c/strategy/issues/483

*there have been emails about this*

Round: what's the biggest feature gap?

* bug reports
* service discovery mechanism
* link previews https://github.com/w3ctag/gaps/issues/8
* servers that don't have unique names are not securely part of the web  / access to local devices https://github.com/w3ctag/gaps/issues/9
* accessibility support in baseline
* sets of webs that are related in some way (not Related Web Sets)
* government ids on a device (hard reduction) - digital credentials in fedid
* payments


ACTION: Tess writeup for AC about link previews gap and send to Dan

ACTION: Dan write summary email to AC about the face-to-face

### In thunder in lightning or in rain (wrap-up session)

#### When shall we [12] meet again

Options

* Spring AC meeting in France 7-8 April - could meet the week prior
* w/c 3rd March - location tbd
* Virtual or hybrid f2f (social benefit of in person is important for onboarding new people)

Agreed: 3-7 March, holding for next f2f. Venue pending new TAG members and travel availability.

#### Associates

<blockquote>
  
### TAG Associate Program

#### Purpose

In order to build a community around the TAG, help to make TAG design reviews more impactful, and create a pipeline for prospective new TAG members, the TAG have agreed to create a TAG Associate mechanism. TAG Associates would be officially designated and would have specific duties and responsibilities, but would not be considered TAG members. 

A larger community will help us do the work we do. More people make it easier for us to do more design reviews. A broader set of expertise allows us to provide more substantive technical leadership.
  
#### Process

The TAG may appoint "associate members" by consensus. 

Any TAG member can recommend any person to become an Associate. Each TAG Associate requires that a TAG member be assigned as a mentor and primary contact.

TAG Associates are invited to all TAG virtual meetings except sessions that the chairs exclude. For face-to-face meetings, Associates might be invited to join for specific topics or sessions. They are encouraged to participate in TAG design reviews and may participate in the development of TAG findings and other TAG documents. They do not receive any of the formal powers or duties associated with TAG membership, and cannot formally represent the TAG.

TAG Associate terms expire annually, at the time that new elected TAG members join the TAG. TAG Associates must be re-nominated at the start of each term.

Two or more TAG Associates must not share the same primary affiliation. If a TAG associate changes affiliation so that this limit is exceeded, they retain their TAG associate status.

When a TAG Associate is nominated, TAG consensus is necessary to confirm the nomination. If the TAG does not reach consensus within 4 weeks, the nominee does not become an Associate. The Associate's term starts on the next business day. 

Any TAG member can request that the TAG consider the removal of an Associate. Unless the TAG makes a consensus decision to retain the Associate within 4 weeks of this request, the Associate is removed.

Note: TAG Associates are able to be nominated as a candidate in TAG elections. Upon being elected or appointed, the standard TAG process applies.

Being a TAG Associate does not grant any special status within the W3C process, though the TAG may help them apply to become Invited Experts for certain working groups. Contributions they make to W3C work are subject to the procedural rules that apply to outside contributions.

The TAG will publicly document its current and past TAG Associates.

</blockquote>

Launch via coralie email to AC. Frame carefully so it's clearly not bypassing election. Not delegating.

* What are they going to do?
* How are we going to mentor them and who is going to mentor who?

[Definition](https://docs.google.com/document/d/1DcN1IkdxKPbTZFa2vzqEaYgyP9LTqQEjjIBY3PXLbV0/edit?usp=sharing)

*Lots of iteration*

There's consensus on the above definition.

ACTION: onboarding document


FORMAL RESOLUTION: Thanks to Amy and Henry for helping to host and those companies that paid for food.

FORMAL RESOLUTION: Thanks to outgoing TAG members for the efforts that they put in.



