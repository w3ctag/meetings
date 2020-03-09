## TAG F2F - Wellington
##### 05 March 2020

---

Present:

### Agenda:

* 14:00 (UK) - 16:00 (UK) - Breakout UK3
* 08:30 - 08:50 Arrive
* 08:50 - 09:30 Plenary (40m)
* 09:30 - 10:30 Breakout 11 (60m)
* 10:30 - 10:50 Tea (20m)
* 10:50 - 11:30 Breakout 12 (40m)
* 11:30 - 11:50 Break (20m)
* 11:50 - 12:30 Breakout 13 (40m)
* 12:30 - 14:00 Lunch (90m)
* 14:00 - 15:00 Breakout 14 (60m)
* 15:00 - 15:20 Tea (20m)
* 15:20 - 16:20 Breakout 15 (60m)
* 16:20 - 17:00 Readouts (40m)

### UK3

#### [guidance on use of json-ld](https://github.com/w3ctag/design-principles/issues/128) - design principle

Considering [Marcos's comment from 4 Feb](https://github.com/w3ctag/design-principles/issues/128#issuecomment-581749625)

Also considering [JSON-LD best pracrtices](https://w3c.github.io/json-ld-bp/)

Hadley: also noting that JSON-LD is on millions of web sites by way of expressing schema.org semantics has a lot of take-up.

Dan: do we need a taskforce?

Hadley: I'd like to ask the chairs - this may be a solved problem or may not be an issue in the chairs' minds.

Hadley: reviewing WEBIDL dependency...  I am not yet convinced that the problem Marcos outlines is a problem... I propose we ping the editors or wg chairs and get them into the conversation.

Dan: Concerned with causing trouble...

Hadley: JSON-LD is a JSON based serialization of linked data, not a general JSON-based data protocol.

Dan: but is it true that in some cases, systems that process JSON-LD don't need to understand the full expressiveness of JSON-LD and can effectively process it as they would any other JSON documents?

...discussion about how this came up in [Web of Things Description](https://w3c.github.io/wot-thing-description/#json-ld-ctx-usage) review...

Dan: would a piece of guidance to make it clear to implementers where JSON-LD processing is required be useful / address David's issue?

Hadley: we could make this an example of simplicity. I want to be careful about recommending specific technologies in the same way as we wouldn't want to get involved in an XML vs JSON decision tree.

Hadley: we could ask the question to the JSON-LD chairs: "Are there situations you can imagine putting JSON-LD into a spec but it being swappable with JSON on its own?"

...If there is an architectural question, it should be ours.

Dan: I think Marcos's issue may be different than David's.  I think it's worth also asking the JSON-LD group chairs what they think about the dependency on WebIDL and Marcos's comment?

Hadley: I don't think JSON-LD is intended to be rendered in the browser - so I wonder how much of this is a clash of communities and use cases...

Dan: also considering Node-JS implementations of JSON-LD... 

Hadley: Let's look at the [Web of Things implementation report](https://w3c.github.io/wot-thing-description/testing/report.html)

### Discussion on next face to face

Peter: The AC meeting has been cancelled in Seoul. Our next meeting was set for Seoul... what should we do?

Dan: We've been talking about doing a remote face-to-face anyway... Should we use this time?

David: We could do 5 hours a day over 5 days instead of 8 hours per day over 3?

Rossen: How is this working for remote participants?

Hadley: Well. Though I second the idea to make the next meeting remote

Dan: Agreed. Especially because the connectivity has been so good. If we can make sure we can support breakouts...

Resolved: Next F2F will be remote. Details TBD.

### Readout from UK breakout on JSON-LD

[dan & hadley discuss json-ld guidance discussion]

Dan: maybe a design review issue needs to be opened up on the issue that David has raised regarding ambiguity in JSON-LD on implementation.


### Breakout 11A

Present: Alice, Rossen, Dan (R)

#### [Intrinsic Size](https://github.com/w3ctag/design-reviews/issues/437)

Alice: Now it's become "contain intrinsic size" [reviewing the issue]

Alice: Seems like reasonable use cases but where is the rest of the explainer?

Rossen: my take on it - it's a narrow use cases. it has a weird codependency on the contain property. This only kicks in when the contain resizes. Interdependency... from a TAG PoV there is nothing necessarily against principles. It's not overly specific.  this has now been worked on. From the TAG PoV we can close with "satisfied"...

Alice: I believe the explainer is still a work in progress.

Rossen: I think the work is being transferred down the standards path...

Dan: I think we *should* ask them to update the explainer... and reiterate the "explainer is not just for the TAG review" explanation...  Maybe put in "proposed closed" pending an update to the explainer?

Alice: there is a display locking explainer that may cover this.  Though you may still have an MDN page on this one thing. We could frame it around: the spec text is now where the explanation  & example code is. Perhaps it might make sense to include some of that in the explainer for the purposes of creating future developer documentation... ... Display Locking explainer has a lot more examples.. might be nice to have non-display locking examples in the contain intrinsic size explainer.

Rossen: [writes up some comments to the authors]

#### [Personalization Smantics](https://github.com/w3ctag/design-reviews/issues/437)

[Discussion about the fact that the explainer they've provided is not an explainer but is more of a use cases & requirements document in w3c format.]

Alice: an explainer shouldn't have modules.

Dan: the explainer should start with user need.

Alice: the explainer should be brief and should be in markdown.

Dan: we don't really need the w3c boilerplate and normative vs non-normative. nothing in an explainer is normative spec text.

Alice: their considered alternatives section is ok.

[alice writes a response asking them for updates on their explainer]

Dan: we need some specific examples of specific assistive technology scenarios that would make use of these semantics... it needs to start with that.

#### [Ads.txt](https://github.com/w3ctag/design-reviews/issues/201)

Alice: There was an update [from 30 Jan](https://github.com/w3ctag/design-reviews/issues/201#issuecomment-579850491)...  They want to know how to write a good spec...

[we closed with a request to file a new issue when they have something new for us]

### Breakout 11B

#### [WebOTP API](https://github.com/w3ctag/design-reviews/issues/391)

We discussed several concerns, primarily around the JavaScript API, and captured those concerns in several issues:

* [JavaScript API can't be used for polyfilling autocomplete=one-time-code in practice](https://github.com/samuelgoto/WebOTP/issues/18)
* [privacy differences between declarative and imperative forms of API](https://github.com/samuelgoto/WebOTP/issues/19)
* [Permissioning, user consent, and the Imperative API](https://github.com/samuelgoto/WebOTP/issues/20)
* [Why is the JavaScript API tightly bound to SMS?](https://github.com/samuelgoto/WebOTP/issues/22)

We also [pinged them again](https://github.com/w3ctag/design-reviews/issues/391#issuecomment-594853798) to please fill out the security & privacy questionnaire, and David left [asked why this is on ServiceWorker](https://github.com/w3ctag/design-reviews/issues/391#issuecomment-594862598)

[Tess had to reconstruct these minutes because Cryptpad ate them]

### Breakout 11C

Present: Ken, Yves

#### [Periodic Background Sync](https://github.com/w3ctag/design-reviews/issues/367)

Yves: it should be possible for server targeted to block possibly unwanted traffic, or at least end syncs. It would mitigate DDoS attacks. There may be a quota of data retrieved in the background as well, ie: ways to limit data usage.

Ken: It should be disabled if the Save-Data header is present

### Plenary Session

Peter: design reviews that are coming in that are not on a real standards track and are being shipped without being standardized properly. 

Peter: e.g. contact API, Font Table Access, and Font Enumeration (last two are heading for origin trial, but are still in a private repo, and not WICG)


Dan: Covered some of this in a meeting with Alex recently

... Discussion in Cupertino about Clipboard, for instance. It's clear to me that there are two things which are both true:

- Positive for things going through Blink process to request TAG review, as it is evidence of wide review
- TAG review cannot be used as a _replacement_ for going through a proper standards track

... Also, many things that are going through WICG are being referred to as standards track, when they're not on a standards track - WICG is incubation (prior to standardisation, potentially)

... I think in some ways, this is why we brought in the wording in the issue template regarding venue, and the "needs venue" label. Might be worth strengthening that language in some way.

... Even if they bring something to us very early on, there should be a trajectory through standards.

... Would like to encourage people to stop putting explainers in their own repos, but instead have a project-specific repo for explainers that makes the provenance.

Alice: What is a project in this context?

Dan: Intentionally vague... provenance. Could be an open source project, could be a vendor, could be from Chromium, could be from Microsoft, could be from Samsung.

Alice: Kind of the relevant organisation?

Dan: Right.

... Has relevance for w3c standards track as well. That's all done by organisation.

Tess: MS explainers repository is vendor-specific; WebKit is an open source project repository.

Hadley: Does this imply that we won't look at proposals that don't come from something established? Is this weeding out "one person having a go" type attempts that risk burning a lot of our time on education?

Rossen: Not necessarily.

Dan: We would like to encourage...

Tess: We would like to prioritise things that have a viable future.

David: We haven't done a lot of interaction with these repos, I'm concerned about filing issues on them. Currently we can file an issue on the repo for the spec, and then bulk move those issues to a WG.

... I'm supportive of the provenance idea, but hesitant about encouraging project explainers until we've had experience interacting with them.

... Need to make sure issues will be noticed by the right people.

Rossen: At MS, we have a private repo where a lot of internal incubation happens, before we work on something publicly. Reason for having the MS explainers repo, is that we can engage with the community to check viability before we spend more time on things.

... Intended for introducing idea and problem space, not intended to be a replacement of standards, simply a place to engage. 

... Highly encouraged to file issues there, people involved in these documents are heavily involved and engaged.

Tess: I created our repo, I could give a similar blurb... the reasoning is fairly close to Rossen's. Want to get people filing issues and engaging. Which of our ideas do people actually want? What should we move forward with?

Hadley: I'm still confused what problem we're trying to solve...

Dan: Original issue is not about provenance, but destination - where the spec is going to. That's the second question.

... We need to strengthen the design review request procedure to encourage - to make the assumption - even if something is not _currently_ in a standards track or working group or community group, we should assume that it will eventually.

... Right now we ask the group where the work is intended to be done in the future. Maybe we need to strengthen that wording?

Rossen: We had a side conversation... it should be expected, or at least highly encouraged, when a spec is being brought in, with a clear venue of further progress... at least the subject matter experts in that community are notified.

... Whether they engage early on as part of TAG review process, that could actually help us in adding a lot of subject matter expert feedback... 

... could be simply us saying ok this spec is coming in, it's clearly supposed to be part of the the WebXR working group, let's make sure the chairs are notified. At the very least there is a level of awareness and the right people are getting involved from the get-go.

... Concern raised form 2 or 3 incidents, specs like... 

Font Table Access
Font Enumeration
Contact Picker
CSS Custom Element State pseudo-class - happening in WICG without awareness of CSSWG

Peter: Re Font APIs, they are shipping only as an origin trial.

... Specs are still in a personal repo, not even in WICG.

... My concern is that there is no clear trajectory for these features beyond shipping, to bring it back into the proper standards track

... Love that TAG is getting these early, but my concern is that the pattern is "let's throw out an idea, submit it for TAG review because it's part of Blink process" - it ships, sometimes even against TAG opposition, then becomes a de facto standard

Dan: This was the case with Clipboard API - went viral ??? didn't get the kind of feedback they wanted.

... Totally agree, I think raising the level of expectation .. we've asked what's the venue and people say they didn't know it was a requirement. We could make it a requirement. 

... Don't know if that fixes the issue with what's going on in WICG, which is a venue according to us, but not a venue according to someone else. Do we want to litigate what is and isn't a venue?

... We've been treating WICG as a venue, putting it at the same level as other venues, but we could be encouraging things in WICG to move beyond WICG.

David: I heard two different suggestions. One was ... the idea of having a target venue, that is good. You don't need to already be in that target venue, but making people say what their target venue if the incubation succeeds is, is reasonable and encourages people to think about that.

Peter: I think that's fair... I don't want people to not come to us if they don't have a target venue... we can help _create_ one. If you don't have one, you're signing up for us to help you find/create one.

... WICG isn't a destination.

David: I think 'having a venue now' is too strong an expectation.

Hadley: I've found that a lot of our interactions, particularly with the Chrome team, which may be because we're a part of the Blink process, combined with project Fugu creating a lot of collaboration outside the formal standards process... I'm concerned that the wide review we have found so useful that has historically been based in w3c under patent protections is happening informally before it comes to us... by the time people come to us they feel they have already had wide review. So once they've ticked the box with us, they're going to ship it, wrap it up and go work on something else. 

... The patent protection, the openness, the things we have in our process that were painful lessons that we had to go through are at risk of slipping out of the process.

... Partially reacting to the conversation we had at TPAC on this... I heard him say that he felt like the standardisation process was long and laborious, while he wanted to deliver and move on with other things... as someone running a team I sympathise with that, but the reality is that the standardisation process is long and laborious.

Dan: So how can we ... have an impact on people's behaviour? How can we positively impact this? Get better feedback and quality of reviews from us if you ... have a good idea of the target venue, taking into account that WICG and other CGs can't be the end point. 

... WICG is a good venue, but it can't be the end of the story.

Rossen: It's in the name: Incubation. 

Dan: Do we think adjusting the design review issue templates is sufficient

Alice: there's tension between I'm exploring and don't know where it would go. Unclear of at what point can we have this influence.

Rossen: How many of these cases are going to be similar to the AOM example?

... To be clear, AOM is probably a prime example of something that should be on its own. 

... There are a few venues that you want to solicit participation and feedback from... idea of target venue is "who else from the broader community are you going to engage with to continue evolving this idea"

... Folks working on specs know people in other working groups

Dan: On the issue of AOM... that is a spec that came to our radar very early, we actively recruited you to bring it to us. We need to know what's going on, to bring things to the TAG which may be of interest. We shouldn't simply be reactive.
 
... Not sure whether this is the same problem as that.

Hadley: suggesting a venue with the proposer may be difficult if the proposer is not in a member organisation

... Speaking as a former chair of formally chartered working groups, we worked hard to agree a charter... then having TAG bring stuff to me that's tangentially related that I can't really do anything with unless we were to recharter. I don't know what to do about that.

Dan: Amending the issue template is necessary but not sufficient... 

Peter: I think it's a good start... we need to make it part of our policy that if there's no clear venue that we will push back on/question that. Ask if they need help creating a venue. Trying to engage, not gatekeep. Stick to positive reinforcement.

Dan: It's frustrating to keep running into these things... would be nice to focus on encouraging the positive things

... Badging API feels like it's on a better track, for example.

Peter: Can someone take an AI to edit the template?

Dan: Maybe someone can do that in a breakout today?

Rossen: Someone here will take it on.

David: I can give it a go.

### Breakout 12A

Present: Alice, Tess

#### [HTML Horizontal Review: Modules](https://github.com/w3ctag/design-reviews/issues/460)

Tess: We should have closed this before; doing so now

Alice: Will they see that comment?

Tess (TAG hat off, HTML hat on): Yes

#### [expand on consistency of naming](https://github.com/w3ctag/design-principles/issues/149)

We started to write [a PR](https://github.com/w3ctag/design-principles/pull/163) to address this.

### Breakout 12B
#### [Delegated Ink Trail](https://github.com/w3ctag/design-reviews/issues/473)

Present: David, Rossen

Reviewed the explainer in more details and left actionable comments to the authors. 

Next review set for March 23.

### Breakout 12C

Present: Peter, Yves

#### [Clarify appropriate and inappropriate use cases for AbortController](https://github.com/w3ctag/design-principles/issues/138)

Issue closed by opening a new issue on the [Promises Guide](https://github.com/w3ctag/promises-guide/issues/65)

### Breakout 14B

Assigned: David, Sangwhan

?

### Breakout 14C

Present: Rossen, Tess

#### [HTML horizontal review: Subresources and Navigation](https://github.com/w3ctag/design-reviews/issues/448)

Rossen and Tess split up the 6 PRs and individually reviewed them. We did not identify any specific architectural concerns with them. We spent much of the breakout spelunking on [whatwg/html#4031](https://github.com/whatwg/html/pull/4031) together.

#### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414)

We had some difficulty parsing [dvorak42's latest comment](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-594011150), so we [asked for clarification](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-594987557).

### Breakout 14A, the Issues lightning round!

Present: Alice, Kenneth, Peter, Yves

#### [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285)

Yves: Will comment on the issue asking for status.

#### [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339)

Alice: We probably need David to comment on this

Peter: We should assign it to him

#### [HTML horizontal review: Browsing contexts](https://github.com/w3ctag/design-reviews/issues/452)

Alice: Needs a substantial amount of work, currently assigned to Tess and Dan. Nothing to do right now.

#### [Cookie Store API](https://github.com/w3ctag/design-reviews/issues/469)

Peter: This is the async cookie API

Alice: Assigning to ken

Ken: Commenting

Alice: This reminds me, I wanted to suggest we make a checklist for TAG members for initial review of a review request. [Issue filed.](https://github.com/w3ctag/tagdocs/issues/2)

Peter: Was also thinking about having the agenda planning tool look at all repos for potential agenda items, and possibly using GitHub actions to create a "live doc" of recently updated issues.

#### [Async Clipboard - image/delayed content](https://github.com/w3ctag/design-reviews/issues/350)

Alice: Last comment is from Anne and off-topic (albeit responding to an earlier topic-adjacent comment from Alex)

Alice: Trying to remember what was going on with this... points about transcoding as sanitization, loss of metadata and colour space issues...

Yves: Transcoding is only part of the issue.

... Drag and drop needs to be taken into account, shares similar mechanism.

Alice: This has shipped, since June 2019.

Yves: Should ask if Sangwhan is ok closing this. Gary said the drag and drop issue was a bit different.

Alice: Labelled as proposed closing, will follow up with Sangwhan.

#### [Web HID](https://github.com/w3ctag/design-reviews/issues/370)

Ken: Had some questions, looks like we got a response...

... Issue was whether people could use from different sites to identify the user across different sites connected to the same device.

... e.g barcode scanner, gamepads.

Peter: how does this relate to the gamepad API?

Ken: Gamepad is actually listed as one of the use cases, so that's a good question.

Peter: Is it related, completely orthogonal, ...?

Ken: Drivers...

Yves: Gamepad will have different mapping of keys based on which device you have, usually done ... 

Ken: Devices can communicate with each other using this API.

Yves: that was Sangwhan's comment.

Ken: They're saying that indeed isn't impossible.
... They do mention the gamepad API...

Yves: Can change state of things on the HID that could be read back by another client of the API.

Peter: One of this and gamepad API should be explained in terms of the other.

... well, specifically that the gamepad API should be explained in terms of this API.

Yves: Discussion about USB ID... vendor:product ID. Whether it was accessible or not. Deciding if a USB device is an HID or not is based on the product ID.

... Would be quite difficult to actually define a scheme that wouldn't involve disclosing the scheme...

... For gamepad, if you don't have the product/vendor ID, it's almost impossible to get the proper mapping to actually use the device.

Ken: (Reading from explainer)

Yves: Want to be able to add a user-defined mapping...

Ken: Seems to be mostly because of gamepads.

Peter: All sorts of other generic devices that could expose themselves as HID devices. Seems to be related to Fugu project. I'm happy with the general concept, could be useful for assistive devices etc.

Ken: HID unit system has SI and English units, but not all English speaking countries use imperial units. Going to comment. 

Yves: Issue of being able to use HID devices as a communication channel seems very risky.

Alice: To summarise what I'm hearing in the discussion... we think this is a valuable use case, but:
1) The Gamepad API should be based on this API, particularly since many of the stated use cases are around Gamepads
2) The ability to communicate across domains which should be isolated from one another via the device seems like a major security hole which we are deeply concerned about.

#### [Same-Origin iframe document-access limiting attribute](https://github.com/w3ctag/design-reviews/issues/397)

Peter+Ken: There are other specs in this same domain so maybe this should not be its own things. Like the origin isolation from Domenic and maybe also some overlap with document feature policies.

### Plenary

#### Design Review issue templates: [Solicit additional information about standardization venue](https://github.com/w3ctag/design-reviews/pull/480)

Tess: The last plenary we had kind of ran out of time, did we want to pick that up again?

Rossen: David took an AI to write a PR on the templates, which I marked Dan to review.

Tess: Do we feel like that template change will substantively improve things?

David: I made slightly different changes to the two issue templates.

... the early design review one, I clarified that we want to know what group within which the incubation/design work is being done, and added a question of which group standardization will occur

... the change to the other template is similar

... trying to be more open about not knowing what the venue should be in the earlier case, and be more insistent about it for the later design case

Rossen: Would that have worked for you in the AOM case, Alice?

Alice: Yes

Alice: Should we suggest a boilerplate answer?

Peter: I want to make them think about it

Alice: We'll get lots of N/A

Peter: That's not a valid answer

Alice: We'll get them anyway

Tess: We can summarily close requests that don't answer our questions adequately

Peter: If the group is N/A, that indicates that they don't intend to standardize this. If the answer is I don't know, we can ask if they want our help to find or create one.

Peter: "none" or "n/a" is a signal that we should push back before looking at anything else in the review

#### Spring Virtual F2F

Sangwhan: Where/when will the next F2F be?

Peter: We're cancelling Seoul and will restructure it into a virtual F2F. Exact details TBD.

Peter: We can schedule the breakouts for it that work for different time zones. David will work out the schedule.

Sangwhan: I may be in Pacific Time in May; will that make things easier?

David: A bit

#### F2F Feedback from Rossen

Rossen: Hour-long breakouts felt rushed sometimes, because some issues are very deep, and you spend most of the breakout time warming up, then once you're ready to talk about it, you've used up all your time.

... happened with Yves and me on the UA Client Hints issue

... One of the review process principles we have internally is that you need to be prepared ahead of time

... People have different tolerances for that

Alice: Not tolerances, time. We're all extremely busy.

... I don't think it's realistic; I don't think any of us can spare the time to deeply prepare on all of the issues before a F2F

Kenneth: We're already doing much more than we were before, with the new weekly breakout schedule.

Peter: Technically we've signed up for 20% of our time for TAG

Rossen: I didn't feel like we have an algorithm for how we do the reviews

... In some we stared by reading the previous comments, in some we jumped right into the explainer

... it wasn't clear to me where into the algorithm we were jumping each time

... is there one? if not, maybe an opportunity to make one

Alice: [shows Rossen open issue to write this down]

Alice: The faster the mechanical feedback to folks, the better.

Yves: grouping issues into breakouts, some breakouts got very easy things to process and some got multiple difficult / large ones; the grouping maybe wasn't realistic in some cases

Rossen: One of the things that helped us quite a bit in CSS was when we started creating F2F agenda ahead of time. Early on, I realized bucketing issues into related groups helped a lot

Alice: How do you do the grouping?

Rossen: by knowing the space

Rossen: Maybe here we could group things by intended venue

... might be better to do, say, 3 hour breakouts on a thematically homogenous set of issues

... we can group things by area

... the fewer cognitive context switches we have to make, the better

Alice: I'd like to write down the process that we used to create the schedule this time, once we've done that, we should capture these ideas to improve the process next time.

Alice: What else did you find fun or valuable or useful?

Rossen: The scope is really appealing. Being able to deep dive into all these different areas gives me an opportunity to read up on so much that is happening

... this is the kind of thing i really appreciate

Tess: I loved how much time we spent on the design principles document

Alice: back to the point of being prepared, I don't think we can expect anything more than the level of prep we can bring to the telcons. Can we structure the pre-plenary breakouts as 1:1 pairs as opposed to how we do it now? So, more like we do in the face-to-face

Peter: Currently we gather up the issues from the week and put them in the breakouts based on assignees

Alice: We keep the existing times, but meet 1:1 instead of mini-plenary

David: I like the idea if we have the resources to plan it well

... the other thing we'd need to do well is we'd need people to rsvp for the breakouts a week in advance

Kenneth: I like hearing about things that the other folks in the breakout are working on

Tess: me too

Peter: we can be opportunistic about parallelizing the breakout, because things are pretty fluid. We can keep the existing meeting URLs and figure out how to split at the beginning of each breakout ... [gives several alternatives]

Alice: if you can suggest pairings without it being too much work for the chairs, yeah

Sangwhan: we could look at the intersection of topic labels and people; that's probably automatable

Peter: some of the issues are really strongly on one or two people; other times, it's overconstrained. we can factor this into the weekly planning, which currently takes about 15 minutes with the existing glitch app

Rossen: when we start working on the steps of the algorithm and figure out what we should do ourselves v. what we should push down to WGs, when are we doing api design review?

... there was one breakout that was actual API review, that I had with David

... maybe it's because the other ones were more mature and i hadn't been on the TAG yet when the API review happened

David: I think that happened in that one because the API surface was small enough that we could read it all during the breakout

... bigger cases we really can't fit that into a call or breakout

Rossen: should the really detailed API review be done by the tag at all, or should it be done at the working group level?

... i don't know if our design principles are followed well in working groups

Peter: in general we take a broad look at the shape of the api, we look for code smells, are they using good patterns

... a lot of WGs are working in isolation so they don't know about similar problems elsewhere that got solved differently

... it's part of our remit to help catch cases like that, and to give feedback on how the api layers with other things perhaps in other WGs

... this kind of feedback can sometimes send people back to the drawing board

Kenneth: some apis don't fit into well-established working groups, so it's good they come to us

Peter: especially as we get more things from incubation, its from folks who may not have experience working in w3c, in other wgs

Alice: we did a lot better job minuting our breakouts than some other times

... the minuting does seem to fall disproportionately onto me, tess, and david

... because we notice it's not happening and then get saddled with it

... lots of people read our minutes, having good minutes is really valuable

... it shouldn't be on a small subset

... please volunteer more

David: I may take minutes in plenary sometimes but I'm really bad about it in breakouts

Kenneth: I added a few after the fact

David: sometimes instead of minuting we're directly writing a comment on an issue, or filing one, etc.

Alice: it makes sense to note in the minutes that you wrote a comment, and link to the comment

David: one of the things that discourages me from doing that is that cryptpad is slow and cpu-hoggy and i need to avoid leaving it open all day because it'll blow up the machine

Kenneth: same

Peter: I'm not married to cryptpad at all; we switched to it from etherpad, which had its own problem

... we also have OnlyOffice available on my server

... or we could adopt a completely different tool

David: i like the feature set but i can't run cryptpad and jitsi at the same time

Rossen: TTS or dictation?

Sangwhan: there's been a lot of pushback

... you can't really do real-time transcribing

... you need a full recording

Tess: and if there were a recording made, I would likely not say anything.

Peter: we hired a scribe in CSS

Tess: Yes, and it's awesome how that goes

Rossen: I'm hearing that there have been some attempts or parallels being drawn with youtube live captions that have been sort of shied away from

... there are some solutions that are pretty good when only one person is talking

... i would challenge you to take better notes than we would get from these tts solutions

... it's unnecessary to put recordings out there

... powerpoint and google slides have solutions here

... we could write a simple app that routes that kind of thing into a text file

... we could then redact and paste the result

Alice: I'm skeptical; maybe you could provide a proof-of-concept

Yves: what about folks with strong accents or who speak incredibly fast?

Rossen: I'm hearing a lot of skepticism

Tess: No one's telling you to not build a PoC

Peter: let's try it while simultaneously hand minuting and compare the results

Sangwhan: I've raised this idea in the past and asked Dan if i could make a recording to prototype this

... i was rejected

... that's where i got stuck

Rossen: if there were a solution that were mildly successful, it sounds like we might be willing to adopt it

Alice: there would likely be the same amount of work in the end, or more

Rossen: unfortunately I've seen people taking minutes and being very selective of what goes in the minutes based on their personal preferences. humans are biased during minuting. robots aren't.

Alice: I don't disagree, i don't think that's the problem

Tess: I find it very difficult to scribe and participate in the conversation at the same time. In the past, we've had backup scribes who take over when the scribe is speaking. That goes pretty well.

Sangwhan: if everyone's okay with it, i could try to see what the results would be with a 15min consented recording on a filtered list of topics

... but people would need to be comfortable with a small amount of recording like that

Rossen: if these companies don't stand behind their privacy polices, that on them

Sangwhan: it may be possible to get a good result from only 10sec

David: identifies many-channel problem with recording webrtc

Sangwhan: it's harder to minute a f2f because we all talk more

Alice: yes

Rossen: during breakouts it's the hardest

Alice: no, it's partly hardest because you don't want to have the cryptpad window open

... a brief comment for breakout sessions is adequate

... if it takes 30secs to open the editor, you won't do it

### Telcon times

David: in Cupertino the conversation got cut short before we were able to consider the nuance of which tz to pin to

... the plenary is pinned to EU time on one calendar

... the breakouts are pinned to UTC

... we need to decide if they should be pinned to UTC

... the US/Europe one shouldn't probably

... we want 9a/5p not 10a/6p

... I'm inclined to pin it to Europe

... the timezone gaps force us to pin the plenary to Europe

... the others are maybe okay, because alice switches one way and everyone else switches the other way

... my inclination is to pin A to Europe and B and C to UTC

Sangwhan: i don't have time changes

... the plenary is a bit problematic

... I'm indifferent about the breakouts

David: B and C shouldn't cause a change for you since you don't have a summer time change

... so then there's the plenary

... in the past we've switched to an entirely different time when Europe goes to summer time.

... we could have used the other time for the winter

... i think the past few years we've done this jump

... should we keep on doing it?

... so we switch to last year's summer time in three weeks when Europe changes

Alice: and would it move earlier or later in time

David: it used to be Tuesday in California for both of them

... we could go to either Tuesday night in California or Wednesday night in California

[... details of what happened last time we did the change ...]

Peter: if we shift it'll be April 1st

David: reads out last summer's schedule

David: or do we want to keep what we're currently doing, but that messes with Europe and japan

Sangwhan: yep nope

b [scribe gives up trying to capture the nuance of scheduling this, but suffice it to say, it's hard to find a time that works for everyone]

[the result is that we will do what we did last year]

Peter: Are we meeting next week?

Tess: I can't make the breakouts, but could make the plenary

[general discussion of this]

Peter: we'll have a plenary but not breakouts.

## Adjourned
