## TAG F2F Cupertino
##### 05 December 2019

Present: Alex Russell (Google, guest), Dan, David, Hadley, Lukasz, Peter, Tess, Yves

Regrets: Kenneth, Sangwhan

Scribe: Hadley

---

Agenda:

* Meeting scheduling
* Fugu (with guest Alex Russell)
* Plenary
* Breakout 8
* Breakout 9
* Breakout 10

---

### Meeting scheduling

#### Next meeting: Spring 

Our next meeting is scheduled for 3-5 March in Sydney, Australia.

Torgo: we're talking about whether we should change that, due to the brush fires.

[Discussion of pros and cons, alternatives and crystal-ball gazing]

Proposed alternative: Melbourne. If that doesn't work, then Tokyo.

Alice: I'll look into options in Melbourne and Auckland; will report back in two weeks.

#### Meeting: Summer 2020

Proposed for summer: Cork, Ireland. Hosted by Apple.

We have blocked out 7-18 Sept for this.

#### TPAC 2020

Vancouver, Canada

26-30 October

#### Meeting: Autumn 2020

Probably should be in North America then.

Proposed: Seattle

If we can find a venue.

First full week in December: 2-4 December, to avoid Thanksgiving travel issues

### Project Fugu (with guest Alex Russell, slightlylate)

 Fugu outcomes:

- Stalled: we've given feedback: now what?
- We gave feedback that was negative and now... dead air?
- Went well: our feedback positively impacted, helped to make outcome multi-stakeholder
- The Abyss: high priority items we have not given feedback on.

Dan: ... we set up a "Provenance: Fugu" label on our design reviews.

... To try and frame the discussion, we came up with some Fugu outcomes that we have observed over the past year of working with these APIs.

... The good news...

- Went well: our feedback positively impacted, helped to make outcome multi-stakeholder

e.g. Badging, SMS receiver.

... From initial conversation being difficult, we ended up in a better position.

- We gave feedback that was negative and now... dead air?

e.g. Bluetooth Scanning, Raw Clipboard.

- Stalled: we've given feedback: now what?

Feedback not necessarily negative, but we just haven't heard anything back.

- The Abyss: high priority items we have not given feedback on.

Things that have fallen through the cracks, or we gave feedback in the wrong place, and are not making it on to our agenda.

Torgo: So that's what we'd like to discuss.

- Went well: our feedback positively impacted, helped to make outcome multi-stakeholder

hober: We want to put this on the record that some things have gone well.

Torgo: [Badging, issue 387](https://github.com/w3ctag/design-reviews/issues/387). Came in on 18 June, currently closed. Comments from TAG members, and then comments and engagement from the community -- especially Mozilla and Apple.

Tess: we had a number of discussion at TPAC, where they invited TAG members to come and help them. It was very productive; we basically redesigned the feature twice. Got to where everyone was happy.

Alice: I spent several hours with the google members. Let me sit down with them, create a dialogue on what we were thinking. Takes a lot of time.

Alex: That's what I hope for from the TAG. Time ivested in s collaborative, not a drive-by. Invesmtment in the success of the API, not a "this couldn't possibly work"

Torgo: I feel that is very positive, and being sensitive to hte bandwidth issue that Alice has raised... I feel like with this and other examples where things have gone well, it could encourage more collaboration that doesn't hvae to be as intensive. 

Alice: Yes, how can we reate mutual trust that means we don't have to spend hours and hours together

Tess: Let me echo what Alice said. Badging was great; but it was a tremendous opportunity cost to the way we used TPAC time. I was being pulled in may direcxtions, and it was at least 4 hours of my day. It is definitely my job, but I felt the cost of that.

Torgo: Right. So if we can establish a better mechanism for doing that, we can achieve the same outcomes with less time.

...This week, we've doubled the amount of time we're spending on TAG stuff. we've been playing with it over the past few months, and we're trying to be serious aobut that.

Alex: Right. I'd love your thoughts. Google has Alice as a TAG member, and we employ a number of ex-TAG members. If we put in place a pre-review process, within Google, it could be transparent.

Torgo: I'm reluctant to that, and I'm concerned about the phrasing. Shadow TAG assumes that Google is the opposition party.

Tess: It could be good. please pre-screen so that we know that things have buy-in before they come to us. Not just a random engineer's idea.

Alex: Nothing that comes to you now should be a random engineer's idea.

Peter: it does feel like it.

torgo: Issue 422 is an example. This really seemed kind of under specified, one person, in their repo, we don't know if this is part of Fugu, etc.

Alex It's not

torgo: this is just an example.

Alex: I hae little context about why you'll see googlers proposing things out of their personal repos. There are rules for getting your proposals into WICG. They are one of hte best places to do that. We have a policy in chrome team that everything needs an explainer. If you're getting a lot of that please let me know

torgo: that's exactly where a pre-screen could help.  This is an good example of something that isn't in our format, doesn't have a se3curity and privacy questionnaire, etc.

Alex: noted and thank you.

David: It could be useful to pre-screen for: does this explainer explain the propblem to someone not already familiar with the problem? A lot seem to be written for the person at the next desk, not someone on a different contintent who hasn't talked about hte problem beofre and doesn't know why it's being done. 

Hadley: +1

David: Some of that is just the phrasing

Alice: Yeah, we tried to work that more into the explainer explainer, to talk mroe about who the audience is, and to encourage authors to run things by others.

...I have pushed back on specific explainers, and have not received helpful engagement. 

David: Also, do the examples serve to demonstrate the need for the feature? In one case, the examples were supposed to show why the feature was needed -- but all could be done without the new feature.

alice: and pushing back on this stuff is busy-work, that we don't have time for

Tess: The fact that we're having to sort this stuff out is pushing externally to us stuff that could be done internally.

Alex: [should we only submit proposals that match a certain quality bar?]

Torgo: I don't think we should eliminate proposals that don't meet our quality bar. Just to mitigate this.

Alice: it's on us to explain what we're looking for.

Hadley: what we tried to do with teh explainer explainer

Alice: well yes, but that's a template. 

...Going back, Alex, WICG criteria?

Alex: That stuff is early. We want your eyes on things as early as they hang together. We've talked about how much bandwidth you have to help us navigate. We've seen that work, but I hear you saying its a lot. And we have examples of where it hasn't worked on either side.

...Sometimes before things have cross-party buy-in, we want you engaged. So it may not have graduated into the WICG process. So should we only send things to you once it gets to WICG? W


Hadley: That's important. Sometimes we have TAG review taken as "This is importatn and is now part of the web platform " -- vs -- "we've had a look at tried to help. now it's back to you to keep going"

Tess: The affiliation of the author is unclear in some cases. Because their github account isn't clear. Maybe we should ask in the issue template for the author's affiliation?

Tess: filed [(Meta) Issue templates should ask for the organization / project on behalf of which the spec work is being done](https://github.com/w3ctag/design-reviews/issues/444)

Torgo: Yes, and we also ask for where the target venue is for the work. If something is headed for WICG or TC39, they should know to put that in their review request. It would help us prioritise that work. I don't think we should require that it already be in WICG.

Tess: filed [(Meta) Issue template should prominently ask for the intended target venue](https://github.com/w3ctag/design-reviews/issues/445)

hadley: should we distinguish the different kinds of review? brainstormy vs transition to CR?

Alice: maybe we need different flows

Torgo: We did talk about prioritisation 

Alice: why not both

Torgo: too complicated?

Hadley: Can Alice and I look at it later today?

Torgo: Sure

Lukasz: Are you involved in the event level click conversion measurement API (issue 418)? This is not exactly something that is ??. A least some of our comments may be translated... we had concerns about security and privacy which I'm not sure are addressed. MY main concern is that there are two specifications which are aiming to solve the same thing. I'm wondering what should be the way forward? Are you aware of any situations where there were two competiting specifications at the same time, concerning the same sphere?

Alex: I know who is involed in this. But it's not my team. With my standards lead hat on, I can try to help. Are both proposals from the same team?

Lukasz: one is from google and one is from Apple

Alex: this happens often, a diversity of views on how to proceed. We encourage this. WE don't have a monopoly on good ideas.  That's the instinct behind our "fail fast" approach. WE give you a read on this early. WE use origin trials to get feedback. and there are a lot of features we have abandoned.

Torgo: So I'm hearing that you will try to provide some additional info on this issue.

...But this is related to our overall topic of working more efficiently. Is there any guidance whe something has failed, that the people who have raised the TAG issue let us know?

...Bluetooth Scanning might have happened in this way? We have no way of knowing apart from our issue. 

...The Clipboard sync APIs is another example. We made a bunch of suggestions, clsed our issue, and then came back to it when the [raw clipboard API](https://github.com/w3ctag/design-reviews/issues/406) came through. and found that none of our suggestions were taken on board. So what does it mean for the original spec? Can we get people to notify us when their work stops, and can you get them to comment on the raw clipboard issue?

Alex: On the process question: There is a long and public [process](https://www.chromium.org/blink/launching-features) that is geared with tags on getting things launched in chromium. STarts with intent to implement/experiment, which is where we ask people to first ifle their requests for TAG guidance. They iterate there. There is then eventually intent to ship. And in some cases then, an intent to deprecate.

...Once something has all the bits required from the shipping perspective at intent to ship, it's going to land in chromium. We could create some automation to updeate your issues once those phases are happening.

torgo: any automation will be fantastic.  Might not help in all cases, but would be fantastic. We can add labels or make changes in the way that we track things, to accommodate that.

alex: we're working throug han update of our public--facing tracking tool. As we do that, it's oing to be more of a clearinghouse for that kind of thing. So I'll add these in and commit to providing updates to you quarterly.

alice: any integration between TAG reviews and chrome status would be great.

alex: Maybe to start, there could be a status-tracker entry in your view template? We could make this bi-directional.

...There is a status tracker for most browsers.

Hadley: so this is somethign we can look at across the board

torgo: yeah, we can ask for the URL in the template. Helpful for tracking multi-stakeholder implementation

...We talked yesterday about how to prioritise our work. Not to leave things behind, but to focus usefully. ONe of the signals for higher priority is intended to be multi-stakeholder participation or support.

Alice: Re the blink process: there is no external engagement other than TAG.

alex: that's interesting. In a lot of cases, in the Fugu team, we're working with partners who aren't so public. But frequently those discussions are happening. Because of the NDA'ed nature of those discussions, it's often the case that we are proxying for them without their visibility.

...But I see that without the evidence, it's easy to dismiss and rightly so. I'm not clear how to sort this. Not just browser makers, but others?

torgo: Yeah, otherwise it would be multi-browser.

...Switching gears: Web bluetooth scanning: we've asked for more info, and got some agreesive pushback and then dead air.

Alex: I see feedback from mid-Sept. Air since then.

torgo: My personal impression: I sat down with one of the engineers at TPAC. WE talked a lot bou the privacy issues. Based on that discussion, I was feeling good about this work. This was someone who cares about privacy and there is work going on to mitigate against the potential issues [specifically: that the permission request would be accompanied with information about the bluetooth devices around you; we also discussed permission expiry]. So i was waiting for that to appear in the explainer or in the spec. Neither of which has happened. So I asked about it, and I got push back on that, that seemed that they didn't understand the question.

...I don't know where to go from there. I get the impression that the team working on this has felt that our feedback isn't useful. and our issue is open; it's churning up our time.

alice: meta-issue: bi-directional trust. In that particular case, that engineer was agitated with that initial review was quick enough and wasn't straight forward enough. 

alex: his first attempt at this process

Hadley: that's far from unique, unfortunately

alice: that shouldn't be our problem. And not mine as a googler.

#### [Raw Clipboard Access #406](https://github.com/w3ctag/design-reviews/issues/406)

torgo: the other issue on my mind: the clipboard story. We looked at the raw clipboard access API. We came back to the question on whether this allows an open tab to have access to the clipboard without user gesture or activiation. Then we realised we left this feedback on the previous issue, for async clipboard. 

tess: and we clsoed that, because we were done

torgo: we now see that was never acted on. the developer says now "this is indeed possible, and we have a business need for it." And frankly, i'd rather see the web die than let this happen. it's not a thing that I will ever countenance. As I say in my comment, I would never knowingly use a web browser that implemented that feature. [due to the speicifc privacy threat that a web page might be able to access your private info - e.g. a password copied to your clipboard - without an expliicity user action].

...I don't mean to be hyperbolic. I'm just trying to communicate to you the gravity of this situation. There may be some groupthink indicating that this is okay.. but it's not okay.

Hadley: +1

Alex: There is a tricky design space here. there are a set of capabilites which are extra-orgigin, or which go through to known unsafe places.

...If you were to take the surface API... like webGL as example, and say you would never want to use something to get to the graphics card... you wouldn't be an outlier. But we do extraordinary amounts of work to make sure this is safer. In chrome, we sandbox them, etc. This work is both detailed and extraordinary. There is such a track record about this tthat I'm flummoxed.

torgo: where is that written down?

hadley: and where is that in the spec? If were talking about putting this into the web, what info do we have for other browsers to protect. 

Tess: And in particular, both of the other engines have [gone on record](https://github.com/w3ctag/design-reviews/issues/406#issuecomment-542310250) as saying the proposal as it currently stands is a non-starter.

alex: we try not to put Ui in the specs. 

Hadley: but I thought you were talking about memory and standboxing, not UI?

alex: all of the above. This is a punch-through. So then the quetsion becomes: can you make that understandable? and can you constrain the situations in which it happens to ones the user expects?

...That is an open qestion. Example: native sockets. We don't think users have a concept of that. web sockets try to align that with the web model, but a lot of those actions are surprising to users too. 

...So would it be available in tab, for Dan's example? probably not. Some things are not delegated to sub documents. There are a bunch of these places where we're navigating user expectations with them.

So instead of assuming hat we're idiots...

dan and alice: no one is assuming that

dan: there is no engagement on that. I'd expet to see this in the privacy expectations, in the non-nomrative guidance.

But when we raise these issues, we get push back or dead air. 

alice: I feel like it comes down to mutual trust and respect. WE often get a response of "why don't you trust us? we have security engineers?" I get that, but the TAG needs googlers to show our work on how that can happen. And that we can specify it in such a way that these things are noted.

...If we're asking reasonable questions, we need to get reasonable responses

alex: so the question here is to expand the security and privacy considerations, and the design doc?

alice: this is a specific issue as an example of a general problem

dan: yes. I'd love to close it off in a positive way, but also i'd like to make progress on the broader issue. 

hadley: and it's not just for us to write that stuff up, but for other participants in the web ecosystem too.

alex: I'm looking at this issue. 

tess: our job is to uphold principles about the web architecture. that's our job.

alex: This feedback asks for things that weren't in his request. with my TL hat on, I don't think this is acceptable.

dan: he's stating here: there are several use cases with desktop etc, that would break with a user interaction

tess: he's valuaing solving his use case over the concerns that Dan is asking him to address.

dan: right. And I've told him I don't think that is acceptable. And that's why we're blocked here. I don't know where to go.

...And I don't think I accept your feedback. It would have been great if you'd said "I understand where you're cominng from. Here are some mitigations we propose." All I see is "no we're not going to deal with this. our business requirements are more importannt"

...That treats us a service provider to the blink process, which isn't the case.

tess: our responsibilty to the web trumps our responsibilty to the blink process.

alex: agreed. And we're not just moving fast and breaking things.

torgo: Rick Byers told us at TPAC that moving fast [at least] was the aim.

...Many people including Rick and I think you have told us that we [Google] are moving fast. You don't appear willing to slow down.  [And this may mean breaking things.]

Hadley: and many of them apparently find the standardisation process frustrating. I'm sympathetic to that. 

Tess: This response from your engineer reads as "Damn the torpedoes; full speed ahead!"

Alice: I'm not sure I agree that this is "move fast and break things"

torgo: moving fast is good. Adding APIs to the web is good. but the [TAG] feedback is not always going to be positive. And I feel like when we do that, we get dead air or push back.

alex: Dead air is not acceptable. Where we have asked for your opinion, we definitely want it, especially to make the design better.

torgo: on this particular cliipboard issue. WE are saying we think this is pretty important. Instead of digging in heels and saying "no, maybe not" -- then how about taling about mitigation strategies.

alex: pickling is here

david: pickling is for clipbaord write. less for read?

alex: both

david: i think our biggest concern is with clipboard read.

...What you just said: the possibility that you can only read things that have been pickeld: thats' a big change from the scope

alex: that's been a big debate. At TPAC. 

...There are other things that I think you're right, we haven't pointed out that UAs might want to consider. ONly installed apps get to do this. We can imagine others.

torgo: that would be great to put in the privacy and secuirty considerations section. Potential abuse cases. People do this. 

...And then mitigations, even if not normative. Ideally normative.

alex: there are a list of normative mitigations already: top level frame, secure origin only. 

torgo: those are boiler plate. They are in everything. it's baseline.

...Also it's not in the explainer. it dosn't get into the meat... it's paying lip service, without getting into the abuse cases. Which are obvious to anyone who thinks about it. 

Alex: To get back to the specific request: to expand security and privacy section: expand the abuse cases, and mitigations, spelled out in a way that's understandable to someone not familiar with the API.

torgo: yes. ideally normative mitigations, and better engagement. A more receptive audience on issues that are raised.

tess: More broadly, I feel liek the feedback from the other engines was pretty clear. the response was disheartening. I'd love to see more of a discussion with the webkit and gecko engineers who pushed back on the pickling. Are the use cases there worth it, given the privacy and security issues?

...currently the other two engines don't think that trade off is worth it. And I don't see any attempt to pursuade them otherwise. Which is scary. they aren't idiots either.

alex: I understand all the sides here. 

...I'm trying to get to the specific set of things you'd like to see, so that I can go back to the engineer. So that your time is respected and you're getting what you need.

torgo: I think you've heard our feedback. I don't think we'll get further today. Is there anything I can do? If my language has upset someone, that wasn't what I intended -- but I'm happy to receive that feedback and to apologise if it will move the issue along.

alex: That conversation is between us. 

I will make sure to work with this specific engineer, to make sure that the potential abuse cases and their mitigations are in the explainer in the next few weeks. 

torgo: Do you have feedback for us? Anything we can improve on? 

alex: We're struggling with, as I said in Tokyo, that the chromium product is very large and we tend not to centralise it. So we get lots of new people wanting to participate. So anything we can do to smooth that, guidance etc.?

alice: we (Google) do have the [engaging with the TAG document](https://docs.google.com/document/d/1wfJyV6GRut7kC5tSNiO1G1zLJgOAbBOWiRvnYvVr5og/edit).

...You and I take away this problem: we have a lot of engineers who are engaging with this; people who may not be focusing on collaboration. How can we manage that?

alex: open question here: would you like us to run more things through our people? 

Hadley: I'm not sure we have enough information to help you decide how to run things in your team

alex: sure; I'm just trying to do it in collaboration with you all.

torgo: I think it might help to encourage people who are filing these issues to at least run them by someone who has done this before. I like to point to the Immersive Web issue as an example of an issue that had a lot of the backing material in it, and was a good example of a working group and the TAG. I sat down with Ada and helped her file that issue.

...So likewise, if someone in your teams is about to file an issue, maybe that would work?

alex: Yes, that's why we're talking about internal quality control.

tess: you could do it in a low-cost way. But something like that would be great. 

alex: I'll take that away.

torgo: other issues to discuss?

alex: we've had issues on RTC come to the TAG, and rustlings of it getting better. Soem of that will be coming through the Fugu group on web codex api... a hopefully uniform API layer to underline codex implementations. HOpefully plug-able. 

...Smells like a huge pile of things that will be disaggreated in a few years. So I wanted to let you know.

torgo: How can we capture that? Design principles issue?

alex: maybe. In a previous issue... is that still open?

...I think it's probably going to be good for layering, and good for the internet overall.

torgo: good to see you, and sorry we couldn't see you in person. 

Hadley: thanks for your help in making this better, Alex.

Alex: talk soon. 


## Breakout: our work mode (Alice, Hadley and Yves)


Deliverables:

* Draft a Week in the life of the TAG member -> update the guide for new TAG members
* Change our template for creating a new design review
* Update our doc on how to work with the TAG
* Creating a process repo for us
* investigate Github Projects, to see if they are useful for us

A week in the life of a TAG member:

Audience:
People running for the TAG.
Transparency for anyone interacting with us. (Probably not the AC). People requesting help, or reading a TAG finding, someone who wants to know why things take as long as they take, who is in the room when something is discussed. And for consensus among us for how we want to work, and what we expect from each other.

Potential action: we can emphasise that who is involved in a review? Or a breakout? Maybe depends on whether we’re closing or adding thoughts?

May not give the impression that we all speak for the TAG. But it might help set expectations? It might help us reach consensus, and help us all stand behind all of our reviews.
We know who to ask or involve on the TAG. But new TAG members may not know that.

Hadley: I find it hard to remember if I was involved on old issues, so when we talk about them again I have to work that out from scratch

Yves: we could manage that with who is on the issue?

Back to a week in the life of a TAG member

Hadley: it occurs to me that we have dramatically changed our working mode on this face-to-face.

Alice: I'd like to do it aspirationally, anyway. And then we can adapt as we go.

Yves: the point is not to be rigid, but to set a good direction. If it fails, we can document something else.

Alice: yeah, that would useful data.

Alice: we have two flows here: design review weeks and non design review week.

...A review week is bookended by two plenaries.

[Alice draws on the whiteboard]

Yves: the TAG charter says that we should be expected to spend 25% of our time on reviews and guidance.

Hadley: Interesting. Tim told me a day a week

Yves: that's 20%

Hadley: And I guess if you add in the face-to-faces and average it out, it's probably 25%


**A Design-Review Week**

(Plenary for previous week)

1. Chairs generate agenda, based on various signals

This one document that covers all our meetings.

The chairs also create the document for our minutes. It is also one document for the week. 

2. Each TAG member attends 2 breakouts, 1 hour each. 

These breakouts are minuted in the minutes document for the week.

* Breakout A - webRTC video meeting (5pm Mon UTC) - for US and Europe-based TAG members
* Breakout B - webRTC video meeting (11pm Monday UTC) - for Asia/Pacific and US-based TAG members
* Breakout C - webRTC video meeting (8am Tuesday UTC) - for Asia/Pacific and Europe-based TAG members

Breakout attendees publish a new version of the breakout minutes on Github after each breakout, and link to the published minutes from each issue which was under discussion.

3. Plenary webRTC video meeting (9pm Wednesday UTC) - for all TAG members

To share readouts of each breakout, identify further discussion or reach consensus and finish/close the issue.

This also includes triage of new issues, so that the chairs know who to assign to breakouts. 

On the third week in the cycle, we need to triage the bigger-picture issues for the next week's meeting.

4. Work on our own

Each of us should allocate some time (3-5 hours outside of meeting time) for:

* Catching up on our slack channels
* Engaging with the community to help them understand how to work with us or to encourage good work
* Sharing what we're up to (tweeting, speaking)
* Keeping up with our github repos -- looking for new issues, big discussions that blow up
* Participating in our own issues and discussions on Github. 



**A Bigger-picture Week**

(Plenary for previous week)

1. Chairs generate agenda, based on various signals

This one document that covers all our meetings.

The chairs also create the document for our minutes. It is also one document for the week. 

2. Each TAG member attends 2 breakouts, 1 hour each. 

These breakouts are minuted in the minutes document for the week.

* Breakout A - webRTC video meeting (5pm Mon UTC) - for US and Europe-based TAG members
* Breakout B - webRTC video meeting (11pm Monday UTC) - for Asia/Pacific and US-based TAG members
* Breakout C - webRTC video meeting (8am Tuesday UTC) - for Asia/Pacific and Europe-based TAG members

Breakout attendees publish a new version of the breakout minutes on Github after each breakout, and link to the published minutes from each issue which was under discussion. This may be optional, because the comments may be fully captured in the issue. 

3. Plenary webRTC video meeting (9pm Wednesday UTC) - for all TAG members

To share readouts of each breakout, identify further discussion or reach consensus and finish/close the issue.

To talk about proposed new work, or to agree new repos. 

This also includes triage of new issues (particularly design review issues for the next week), so that the chairs know who to assign to breakouts.

4. Work on our own

Each of us should allocate some time (3-5 hours outside of meeting time) for:

* Catching up on our slack channels
* Engaging with the community to help them understand how to work with us or to encourage good work
* Sharing what up to (tweeting, speaking)
* Keeping up with our github repos -- looking for new issues, big discussions that blow up
* Participating in our own issues and discussions on Github. 
* Publishing any documents or blog posts
* Writing automation bots


Alice: would it be possible to keep a running "executive summary" on what has happened on each issue? This would be extra effort for the person/people writing the summaries, but would help reduce the load on other TAG members to understand the progress on the issue.

Possible strategies:
- Make notes in the breakout (possibly copy/pasted from minutes)
- Make this optional, only for very involved/contentious issues
- Where should these live?
   - Put a summary markdown in a folder in the design-reviews repo? Link to it from the issue? (Or Github projects?)

Hadley: it is extra work, which concerns me. I'm also concerned that our editorial views (not accounting for some views, or potentially misrepresenting them) might upset the comment author.

Having said that, it may not be an issue -- and i see no harm in experimenting on it.

Alice: It localises the work to whoever is working on the issue (1 person). And it saves each of us from having to reread entire threads when we come back to an issue.  So hopefully it's a net time saver.  

Hadley: what should we call the weeks that aren't design review weeks? Calling it a non- anything makes it sound less important and therefore something we are less likely to prioritise.

...We could call it an architecture week

alice: Bigger picture work?  It's not just architecture. 

Hadley: as a planner, I'd like to see something a little more concrete...  the concrete comes up most in our specific tasks. 

yves: the outcomes would be what? findings? guides?

Alice: [finds yesterday's notes]

Yves: Given that the [TAG charter](https://www.w3.org/2004/10/27-tag-charter.html) says we are responsible for:

> This is the charter for the W3C Technical Architecture Group (TAG). W3C created the TAG to document and build consensus around principles of Web architecture and to interpret and clarify these principles when necessary. The TAG will also resolve issues involving general Web architecture brought to the TAG, and help coordinate cross-technology architecture developments inside and outside W3C.

**Things to deliver in "bigger picture" time**

* Design principles
* Guides and documents to help spec writers
* Findings
* Specific collaborations with working groups
* Reflecting on themes from reviews (and deciding what to do)
* Refining our process and building tooling
* AWWW the sequel

Hadley: [struggles to come up with a more concrete name than 'bigger picture']

Alice: shall we put that on the back burner for now?

hadley: sure

## Explorations into GitHub projects

Alice: It essentially puts your issues/pull requests into a Kanban board, with *very* minimal automation available. The automation available wouldn't suit our needs, unfortunately.

## Update review issue templates?

Alice: Dan already stated his position on this, but I would like to raise again whether we want a separate template/process for "early review" type reviews.

Hadley: I don't really have a useful opinion, but perhaps we could explore what that might look like?






### Breakout: various Feature Policy issues ([#339](https://github.com/w3ctag/design-reviews/issues/339), [#341](https://github.com/w3ctag/design-reviews/issues/341), [#369](https://github.com/w3ctag/design-reviews/issues/369), [#408](https://github.com/w3ctag/design-reviews/issues/408))

(Tess, Peter, David)

We started with the [Iframe execution pausing](https://github.com/w3ctag/design-reviews/issues/369) issue and had some discussion that lead to comments directly in the issue.

Then we discussed a bunch of stuff related to feature policy that was related or tangentially related to these issues.

David raised the question of whether building a bunch of features on top of feature policy is a good idea given that not all browsers are bought into feature policy yet. Tess agreed. Ideally, we build experimental/unstable things on top of stable things, otherwise we risk building on quicksand. Peter refers to this as [Palevich](https://twitter.com/palevich)'s Law. It is also reminiscent of [Baby Steps](https://github.com/w3ctag/design-reviews/issues/426). Perhaps we should capture this in our Design Principles document.

David then had an IM conversation with Martin Thomson to understand what his objections are -- which seem to be more around (1) the "breaking pages" aspects of using feature policy to remove features from the web that pages may assume already exist, so they apply more to sandboxing-type things than to pause/resume (e.g., what happens to a page that happens to use `document.write` for its CSRF tokens if a page that contains it removes `document.write` from its view of the platform) and (2) the complexity of the origin-specific syntax and also the potential unexpected results when using origin-specific syntax.

Re: Martin's "breaking pages" concern, Tess whiteboarded a simple scenario of an embedding site (Foo) and an embedded site (Bar). If Bar is unmaintained, and exhibits behavior the embedding page (Foo) would like to mitigate, "breaking pages" is necessary. If instead Bar is being actively maintained, we can at least hope its developers will get bug reports which will allow them to understand that they are being affected by Foo's feature policies. In this case, it would be nice if there were an additional feature allowing Bar to declare "I would rather my iframe not load at all if feature X is disabled by the embedding document."

We then had a brief whiteboard discussion about the origin-specific syntax of feature policy and the possibility that a page using it to pause iframes in the `bar.com` domain would actually not pause sub-sub-frames of such a frame that are in a different domain, which would likely be contrary to expectation.



### Readouts

Tess's quick summary of issues:

Closed Portals (timed out), Audiobooks (satisfied), same site lax by default (satisfied), and intersection observer v2 (maybe sort-of-timed-out?).

Also looked at first party sets (left comments), `isFramePending` (and borrowed Simon Fraser, and left comments covering our discussion, want their feedback now), iframe execution pausing (refreshed minds, left comments, Tess needs to do some research to answer dtapuksa's question).

Then we just had a sort of general discussion about feature policy (tied to the iframe execution pausing and a little bit about the other three isssues.)  That didn't result in comments in issues; ended up in the minutes instead.  dbaron IM'd Martin Thomson as well a bit during this conversation.  We agreed to take #341 feature policy evolution in a future APAC/California breakout because we wanted sangwhan to be here.


Hadley: We had 5 deliverables, did 4, morphed one.

Hadley: (1) Week in the life of a we TAG member, we now have a guide for new TAG members.  Please review.

Hadley: (2) Alice changed template for new design review...

Alice: Created a new template for early design review, and updated the specification review template with some tweaks.  Added a one paragraph sumary of the idea as a section that they need to fill out.  Made the security privacy self review as a required bullet list item.  To-do is make a markdown template for security and privacy self-review.

Alice: explicitly request people to state their affiliation.  Hadley had idea (which I want to try) about asking who is funding the work.  Previously noted existing multi-stakeholder review.  Put them as checklist items, not just recommendation for explainer.  (lists things too fast to minute)  

Hadley: (3) create a process repo for the TAG.  Yves did.

Hadley: (4) investigate Github projects.  Alice did.

Alice: was a bust.  ...  Just another view of your issues.  That's it.

Alice: Thing we really want is automation of our workflow based on labels.

Peter: automation across repos.

Hadley: Guide for new TAG members.  Hadley goes through sections.

Tess: Seems good.  Convert to markdown, put in github, and if the folks not here don't like it they can file issues.

Hadley: Next step is to do one for people who are not the TAG.
