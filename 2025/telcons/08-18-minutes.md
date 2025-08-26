# TAG Minutes - Week of 18 August 2025

## Breakout A (Asia / Australia / West America) - [2025-08-19](https://www.timeanddate.com/worldclock/converter.html?iso=20250819T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Serena, Jeffrey, Marcos, Max

Regrets: Xiaocheng

Scribe:


Attendees are generally underprepared for the discussions, so we're picking out the useful agenda items.

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola
### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Martin: Went through Jeffrey's comments, and made some significant changes. Haven't looked at Ehsan's comments yet.

Jeffrey: Age verification relationship to the finding.

Marcos: Looking at the fallout from the UK rollout.

Martin: Looking at https://zhibosun.com/assets/publication/usenix/adultapps.pdf. (A survey of Android apps' age verification practices.)

Jeffrey: On "no papers", it feels like this is urgent because people are rolling out age verification.  We could leave age verification out, but we might miss the chance to say something.  Everyone reading it will be asking.  So we should say something.

Martin: Don't feel like it should be a primary focus, but maybe include it as a use case. Form of age verification that's associated with having a government-issued document.

Marcos: Mozilla sending someone to Age restrictions workshop? (https://datatracker.ietf.org/group/agews/about/) Ben Vandersloot? 

Martin: We'll put the papers out in public, and Ben has a paper with a preferred approach. I'll be chairing and so not so opinionated.

Jeffrey: I'll also take another look through the changes.

### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Marcos: I put together a position, which might be ready to publish.

Jeffrey: Data governance?

Marcos: LLM brings this into question. Fonts question, model might be tuned based on your preferences. Whether there's a way to stop it from doing that is unclear. 

Jeffrey: I think they clearly say it must not save the user's data.

Marcos: Don't know if that's possible.

Martin: This is a UA. So when the input goes in, that's data provided by the website, and it's working for the person using hte computer.

MArcos: Example I ran into today, an input field using Apple Intelligence. It shows up in ChatGPT history.

Jeffrey: Seems like an implementation bug.

Martin: Maybe a feature, since ChatGPT is a UA, and users might want that.

Marcos: But does it save it in private browsing mode? ChatGPT doesn't have that. And it saves customizations into private browsing.
.... It will learn about you and respond in a way that is tailored to you.

Jeffrey: We need to justify this kind of comment, or they'll think we just didn't read the explainer.

Martin: There is a case for saving this for the user. Maybe as a user I want to save a log. Maybe to know the resources used. "Must not save" isn't necessarily the right thing to say, except in private browsing.

Jeffrey: It is more that saving must not affect the model operation in ways that might affect privacy.  We need to respond to the explainer, not assume that it is incorrect. 
... Fingerprinting risk is perhaps another example of that.

Martin: Computation risk is one of my major concerns. Why are users expected to provide the compute? The explainer doesn't really explain this.  There's a trade-off there, but they don't really do that analysis.

Jeffrey: Think they'll be able to come up with an argument for that, but fair to say the explainer doesn't do it yet.
...Structured output is interesting.  You are right in that this is a hole in how these things work, but that doesn't mean that we shouldn't try.  People seem to be taking advantage of the mostly-structured output these things can create.

Marcos: There's a person trying to standardize something that defines the structured inputs and outputs that websites want. Proposing something for TPAC. You prompt the model and also define the structure for the application. The Prompt API doesn't handle that gracefully.

Martin: If you ask for a particular structure, especially the smaller models will _occasionally_ diverge from that. E.g. https://gist.github.com/simonw/25e7b7afd6a63a2f15db48b3a51ec9bc#response-9 (pelican riding a bike)

Martin: Do you have more to say on progressive enhancement? That section is terse.

Marcos: I can add something.

Martin: Kagame's translation API alternative. Domenic's proposal is straightforward. Kagame's is "here's some DOM, please translate it." Would be entirely declarative. Does that work for a prompting API?

Marcos: Seems like that should work. Lot of subtleties that are lost in just taking text.

Martin: Declarative API would just do what the in-browser translation feature does, which could keep images in place.

Martin: I might disagree with the "difficult to polyfill" point.

Marcos: It's difficult if you don't have access to the large models ...

Jeffrey: The Prompt API proposal is to use a downloadable model, which could be downloaded onto the device.

Marcos: The objections here are assuming that you need a cloud model. Local models aren't very useful.

Jeffrey: We should make that explicit. Could ask the proponents to show that their proposal to use a local model is "good enough".

Martin: Especially on lower-end devices. Speed and output quality.

Marcos: The prompts themselves. The complexity of the prompts can be unbounded.

Jeffrey: Think there are token limits. Summarizer definitely has one.

Marcos: Not even about limits, but the complexity of the query. If you're asking the model to act adversarially.

Martin: Comes down to the quality of the model.

Marcos: Yes.



### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @martinthomson, @jyasskin, @csarven

### Update on IETF AIPref WG

Martin: EU set some targets for getting industry standards for opt-outs for their TDM laws. Ties into copyright regime. Had Text and Data Mining exclusion on the books. If someone provides content, they could opt out of TDM generally. People doing TDM have to respect that. There's a general copyright exclusion for TDM, and copyright applies again if someone has opted out in a machine-readable fashion. Happened before AI exploded. Looiking at adding some things to robots.txt and HTTP headers, to say "yes this, no that". Umbrella that corresponds to TDM in EU law, and some things for AI training. "This is my content; I'd prefer it not be used in AI training." Or generative AI training. "If you're building a model that'll act as a competitor to me, don't do that". Those 3 categories came out of early discussion. Part of that was to put that in robots.txt. General contract with robots.txt is that if someone's crawling, they're doing a search engine, so they're sending you traffic, which benefits you. We realized that if we give people the opportunity to say no to TDM, they're saying no to building search engines. So lots of discussion about the inference side of AI. Primary thing people want is a carve-out for search. "no TDM except for search that shows links to the page". taht gets very complicated because search is a complicated product that does many things. E.g. AI overviews that supplant need to visit the thing in the first place. Documents are rough but readable.

Martin: Definition of "AI" is a big question. We wrote it down in a couple sentences based on laws and long papers. Someone complained that it covered any statistical technique. No bright line between ordinary least-squares and the complicated stuff LLMs do. Maybe least-squares _is_ AI. Or maybe there's a line.

Serena: My if-else statement is AI.

Martin: Most of the definitions I found were "computer does stuff".

Jeffrey: I suggested a couple months ago that the rules focus on the outputs rather than the guts.

Martin: Think that's where we're headed, except for AI training.

Serena: Was there an attempt to define categories of technologies or uses?

Martin: That's the work. "Under what circumstances is it ok to use the work?"

Jeffrey: Useful to post the "outputs" thing again?

Martin: We're getting to that.

Jeffrey: I'll hold off until you holler.

Martin: We're looking at this as a single user being the recipient, as opposed to building a model and using it for many people.

Serena: Is the idea that at some point we'll come to an agreement about various categorizations and have a new standard for robots.txt? How does that get rolled out and adopted?

Martin: Basic technical mechanism is that a crawler grabs a bunch of stuff and looks at robots.txt to see what it gets and can't get. It learns which categories are ok to use, and attaches that to the content. And that determines how the content is used.

Serena: What compels the actors to abide by the new categorizations?

Martin: Nothing in the technical standards. Adoption is voluntary, nudged by things like the EU AI code of conduct. It pointed at robots.txt, which might be just about crawling and not the AI things. But AI companies have interpreted that as a threat to their business, which has been disruptive to the WG. Difficult because there are genuine concerns, but also concern trolling.

Serena: Because current situation is a free-for-all?

Martin: Various companies have said their use under copyright is fair-use. Seems that in the U.S. there's political protection. There's a case that an AI is learning something. And also a case that the AI is creating the ability to compete, and copyright law makes that affect fair-use. 

Serena: Target date?

Martin: Original date was this month, but we have a meeting in October.

Jeffrey: Maybe we should chat about this in Hong Kong.

### Reviews that would benefit from UX lens?

Marcos: PEPC things too.

Martin: There are constantly UX-y things, and things that don't get a UX view that should.

Serena: Review load makes it hard to find UX-y things.

Jeffrey: Maybe we make a label to highlight UX-y things so Serena can focus?

[general approval]

Serena: Even the Prompt API explainer makes it hard to find the use cases. Maybe that's the case for broad APIs that are really flexible.

Martin: Many of us have a bunch of context built up over years that makes it easier to skim an explainer.

Jeffrey: But it's the explainer's fault if it's hard to find the use case.

Martin: Two things in explainers that matter most: what is the use case and, if the user doesn't benefit from the use case, how do they benefit?

Jeffrey: I'll make a Focus:UX label to make it easier to focus on these.

## Breakout B (America / Europe) - [2025-08-20](https://www.timeanddate.com/worldclock/converter.html?iso=20250820T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Jeffrey, Dan, Matthew

Regrets: Christian, Sarven

Scribe: Dan

### [societal-impact-questionnaire#11: centralization](https://github.com/w3ctag/societal-impact-questionnaire/issues/11)

Lola: Discussed last week. We added to agenda+f2f because a lot of people will probably have opinions.
Will be good opportunity for dedicated session. I'll copy the minutes from last 2 weeks into GitHub for review.
Can discuss either at plenary or F2F.

### [societal-impact-questionnaire#4: Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4)

Lola: Also spoke about this last week. Sarven will open PR with text. I don't think we should add anything
specific about AI to societal impact questionnaire, it's too specific. List of specific techs could be endless. Keep it general.
Sustainability, privacy, environment, security, bias, covered by questions in this questionnaire or other docs.
Don't need to repeat ourselves here if these concerns are already covered by other docs. But didn't come to ressolution.
So Sarven will write PR.

### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark

Jeffrey: Proponents updated explainer, reviewed by Dan. I left quick thoughts in brainstorming issue.

Dan: Can we declaratively appply non-declaratively imported contents?

Jeffrey: Author is asking for FOUC.

Dan: It's an open question. I hope we don't add FOUC.

Jeffrey: There's the blocking attribute.
My sense is we should mark it as satisfied or validated, with this list of things for future reviewers to pay attention to.
They'll be talking to CSSWG and HTML WGs. Adding Dan's use case to things to keep looking at is the right way to go.

Lola: Dan do you want to write that closing comment?

Jeffrey: Let's collaboratively write it and I'll post it.


### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: This is another where we want to have an example for everything. I need to open PR.
Last week we decided to use examples of specs that were misused and corrected.
E.g. autoplay. Now there's a note in the spec of how to use. I need to do that, create a PR.

### [user-agents#7: Consider applications with both 1p and 3p sections](https://github.com/w3ctag/user-agents/issues/7)

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14)

Jeffrey: We marked this as needing to be written. I haven't but will do it. Will try in the next week.
Matthew, should we split them (7 and 14)?

Matthew: I'm happy to do one.
Previous definition of UA from TAG was narrow -- that might have changed given current makeup of the TAG.
I can look back on last week's conversation to see where this might have shifted. That's issue 14.

Lola: Since Xiaocheng is out, also look at UA definition as it relates to MiniApps?

Jeffrey: I'll do 7, Matthew 14, and we'll pull in Max as needed.

### [explainer-explainer#30: Say how to explain developer-focused features.](https://github.com/w3ctag/explainer-explainer/pull/30) - @jyasskin

Jeffrey: I made progress on this. Moved chunk of it to appendix. In issue 7 we talked about when you have security feature
you should say "security is useful for users because..." and it's the same for every security feature, dones't make sense
to have every author come up with it on their own. So I came up with boilerplate for it.

Lola: Example you gave on CSS nesting, affecting file size. I worry about that example because I think it should have been in 
the sense that the developer is the primary concern, but there's a negative impact on users -- if using CSS nesting inline
bloats the file size that could have negative impact. But it's a justified risk.

Jeffrey: More likely it'll shrink file size because it'll reduce repeating selectors. But that's not the main point of the feature.

Lola: Could you be more explicit in saying that?

Jeffrey: What should we say? Or we could pick another feature.

Lola: This example is fine.

\<brainstorming of wording\>

Lola: Matthew do you want to review?

Matthew: I will after this call.

Jeffrey: Good to merge once Hadley and Matt have approved.

### [explainer-explainer#9: Update the WebIDL guidance for explainers](https://github.com/w3ctag/explainer-explainer/issues/9)

Jeffrey: No progress

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://github.com/w3ctag/design-reviews/issues/1120) - @matatk, @xiaochengh

Lola: I was looking at this earlier. Matt posted comment 2 weeks ago, no resolution. Asked them about Safari, they responded.

Matthew: They allude to it being detectable with @supports. But it overwrites what author does.
So I'm not sure you acutally need to query it as an author. I think it's OK that Safari won't implement it because they don't need to.

Jeffrey: [Concern in blink-dev thread](https://groups.google.com/a/chromium.org/g/blink-dev/c/U-6tIuuGtgo/m/3SdA3iFVDAAJ) is that this shouldn't be a feature.

Matthew: From a11y perspective I'd have to agree. But seems to violate cardinal principle that you don't tell browsers how to do their UI.

Jeffrey: We probably wouldn't standardize what happens. But if devs forget to do this, it's bad for users.
So we should do the right thing for users

Matthew: Not sure I agree with this, but brainstorming: should you be able to impart a personality for this, like with a dark-mode? But maybe you shouldn't have to do that,
UAs should do it for light-sensitive users. Could make same argument.

Lola: I have concerns from a11y perspective but haven't fleshed those out. There are a11y issues with highlight in general.
If Safari UI is better for a11y, 

Jeffrey: different from dark mode, that's the whole page, all colors need to work together.
But this is one chunk of text. So browsers' problem is easier.

Matthew: I agree, just want to make sure reasoning is sound. It's about a small portion of content at one time. Bad if inaccessible.
Not covering keyboard interactions, right? Cooperating iwth existing browser UX.

Dan: Yes

Matthew: So browser is doing most of a11y effort here. Just for colors...probably preferable for browser just to do it.

Lola: What's the concern? I'm using non-Chrome chromium browser, browser already does this. When I search, it highlights
search text. 

Dan: Bro2wser UI might have lack of contrast with site content. 

Lola: We can rely on UA for this, but don't need to. Different from dark mode, but similar enough. If I control the design
of the website, I want to control the design of things and make sure the colors work. Why would we want to default it to the UA?

Matthew: It takes control away if we say the UA should do it. It would also guarantee sufficient contrast.
In theory user could change in UA settings, like a theme.
With Safari you don't have the control of theming, but they provide a consistent and clear look and feel.
You're taking control from the site in exchange for it being consistent across sites.
You're relieving the developer of the burden to get the constrasts right.

Jeffrey: Dan also pointed out authors can attack users with this by disabling find on page, which is reason not to do this.

Lola: Do we want to resolve unsatisfied?

Matthew: I propose to draft comment that puts it to them, why not just expect UAs to do this? Plus other points we discussed.
Would like to hear their response even if we disagree.


### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @matatk, @xiaochengh

Matthew: We're getting much closer. I posted question about why not just selectors -- why have that layer of indirection.
They (Tab) said there are good reasons, apply to lots of different CSS props, we use this pattern of providing a name and referencing that, why not document centrally rather than putting in every explainer.
Then Brian Kardell created that issue and said selectors are more readable, asked for central documentation.
They've had the discussion. Got me thinking about priority of constituencies. I accept this is idiomatic CSS, it's considtent with the rest of CSS.
But I think selectors are more readable. The reason they have it performance, harder to parse selectors.
Putting them in more places causes problems for implementers.
It's interesting -- is this an author or a user feature?
But I'm happy with this aspect of it, reasons they gave to do this are good.

That leaves the otehr part of it which is it's underspecified. They're not saying which UI events.
They said it's an early design review, they're aware they haven't said much about that side of thigns, are working
on the syntax.
In terms of what we asked for, we'd proably close as satisfied with request that they come back when they have a spec
with more detail.

Jeffrey: this is interesting because they're cross-linking elements. CSS does it by defining a name and then using it elsewhere.
HTML does it with idrefs. There's cascading attribute sheets, which also allows cross-linking attributes.
TAG should have an opinion on how to do this. I don't know what the answer should be. Maybe just that should be
compatible with these other efforts, let's all work on something that can cross all these domains.

Hadley: Sounds like something for design principles.

Matthew: I hadn't thought about it in this lihgt but I agree it's that problem again, would be great to come up
with more flexible solution. I like cascading attribute sheets. I think if they do this the way they want,
wouldn't preclude us from solving that problem still. It's much better than the inert stuff.
This is just carrying on doing CSS in consistent way.
If we do close as satisfied, should mention it's an instance of this issue.

Jeffrey: I agree, shouldn't be unsatisfied just because they haven't solved background problem.
But should maybe mention it as a concern.

Lea's issue: https://github.com/w3ctag/gaps/issues/2

Lola: Should we invite CSSWG folks to this issue?

Hadley: Sounds like there's an architectural topic there that would be good to have a more public discusion on.

Matthew: Should we do a workshop on this?

Jeffrey: Should have TPAC breakout first.

\<agreement from the room\>


### [design-reviews#1129: Incubation: `CrashReportStorage` API](https://github.com/w3ctag/design-reviews/issues/1129) - @christianliebel


  ### [design-reviews#1130: Incubation: An `Origin` Object](https://github.com/w3ctag/design-reviews/issues/1130) - @csarven, @dandclark

Dan: Some of the motivation is to handle opaque URLs. They should flesh out that motivation, and possibly add a targeted API for that.

Matthew: API shape suggestion is interesting. Christin said it's not useful enough to add to platform.

Dan to draft a comment with Christian.

## Breakout C (Europe / Asia / Australia) - [2025-08-21](https://www.timeanddate.com/worldclock/converter.html?iso=20250821T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Matthew, Ehsan, Martin, Lola, Christian, Max, Marcos

Regrets: Xiaocheng

Scribe: Christian

### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Hadley: we talked about renaming this repo. Don't know what happened with that

Ehsan: I added a pull request this morning, but my editor messed it up.  Will need to redo it after. 

… Did my pass, don't know what Martin wants to add.

Martin: Jeffrey raised a point about (…), halfway through it, one of the topics where it makes sense to spend an hour of time during the F2F in Hong Kong.

Hadley: Is there a label yet?

Martin: Put it in Jeffrey's spreadsheet, in the "other topics" section.

Hadley: We also have a F2F Agenda+ label in the design reviews repo.

Martin: Want to close the issue before the F2F.

Ehsan: You have one issue about age verification? Wondering if you have added it as a use case or…?

Martin: Want to recognize that age verification might cause people to become accustomed with sharing identity verification when visiting websites. Not something that we want to do.

… Have all of the text already, just want to get the messaging right.

Marcos: in the UK, large adults sites are using the Credentials Management API, with zero knowledge proofs. It begins!

Martin: who is generating the proof?

Marcos: I think it's format specific.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: We can skip that, it's the master issue, need to remove the agenda label from it.

Hadley: Anything you want to discuss?

Lola: No, discussed it yesterday.

### [design-reviews#838: Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola

Lola: Saw your comment on this, Hadley. What did you want to add?

Matthew: Liked the comment, have raised it before. Threat of information leakage, don't think it was fully adressed. Feels like we should be mentioning it in the closing comment.

Lola: Think this should have been scheduled for yesterday's meeting to Jeffrey could have checked it. Can bring it to Jeffrey's attention.

… We have a very rough draft of a comment. If anyone wants to review, that would be great.

Hadley: Ok, come back to me after you've talked to Jeffrey.

### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @lolaodelola

Lola: Jeffrey mentioned updating Xiaocheng's comment including the previous examples and suggested alternative approaches that haven't been mentioned to the group.

… Couldn't see where those alternatives are. Everything I've read has already been suggested to the group. @Martin: Any insights?

Martin: No. Do you need help?

Lola: Last time, we wanted to take Jeffrey's suggestions for the comment into Xiaocheng's draft comment. If we do want to be clearer about the several other alternatives we've discussed, maybe it makes sense to flesh those out. But they aren't written down anywhere. Not in minutes, brainstorm, …

Martin: There are some in the brainstorm?

Lola: The ones in the brainstorm have been suggested to the proponents before. Xiaocheng has been in conversations with them since May.

… Was wondering if one of the things he was taking about was regarding the code that was reviewed.

… Guess I need some help to find out which one of them haven't been suggested.

Martin: Don't see any evidence…

Lola: In the main thread, not the brainstorming, Xiaocheng first suggests making Shared Workers more accessible and introducing a new global scope (?), suggestes `lifetime: true` to every shared worker or new worker that is designed for such a use case.

Martin: Don't think there is any discussion about the use of the extended lifetime.

Lola: Should I re-suggest that?

… Jeffrey said they should consider a Lifetime Promise API via internal channels.

… Assuming what Jeffrey has proposed built up on what you proposed, Martin?

Martin: Yes.

Lola: Go with Jeffrey's suggestion?

Martin: Yes.

### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Martin: We were asked to wait, should be stop waiting?

Marcos: We have consensus to move on. Expect to merge some stuff in the following two weeks.

Hadley: Can we change progress to stalled or pending external feedback?

Martin: Think this is the sensible thing to do, if it could be two weeks.

Hadley: Need to know if I should put this on the agenda.

Marcos: Depends on how TAG wants to communicate with the Working Group, and about what. Architectural details? Usage of APIs? Depends how folks are doing the review.

… Thing exists in the world today, people are using it. How do we want to proceed based on those facts?

Hadley: Was under the impression that we were blocked by the WG getting consensus.

Marcos: Reality of the situation is that N number of sites are using the thing, pressure is different. It wasn't a week ago.

… Irrespective of the PR that is blocking. Will not change the view of the world.

Martin: I _do_ want to have the discussion that Marcos talks about.

Hadley: Should we have it in the issue?

… Matthew, Ehsan, any thoughts?

Matthew: Agree we should have the discussion, but wasn't aware of the time scale. Can we cover it in the normal breakouts? Are we talking about this in the F2F?

Marcos: There's real concern now that this is deployed to the masses through one of the largest websites of the world. Not affecting other jurisdictions apart from UK, but that might change soon. You could image other sites quickly using this API. Now is the time.

Hadley: Options: 1) Start the conversation, 2) schedule an additional meeting, 3) put it off to plenary of F2F, 4) too late, nothing we can do.

Martin: Last one is not an option. Don't think we can get away with saying nothing. The finding may be all we say. We do owe people a proper review on this one. Think we don't only need the low level (UX etc.) but also high level review on this one.

Hadley: What do you need to do to get this review done this week?

Martin: This is not possible, next week… maybe.

Hadley: Still worth doing?

Martin: Would be surprised if we can be done in two weeks, because of the nature of the work. But it is a much more reasonable timeline.

Ehsan: Do we have an idea of what we want to say?

Lola: Think we want to have the four of us discuss this separately to brainstorm together. Martin, you have a lot of expertise, but it shouldn't all be dependent on you.

Matthew: Two questions, 1) unclear if we should take the extra material into account that Marcos talked about, sounds like we should to it, 2) I think the review of no papers, we need to rename the repo. Should we publish it soon?

Hadley: Re 1), The link is in the comment. WG is still getting consensus, we cannot assume that yet.

Marcos: It's a very thin UX-related change, has no bearing on the rest of the thing. Wouldn't worry too much about this one. Not architectural.

… I'm available to the reviewers to join whatever call as an editor. Might accelerate things, even though I might be biased. I'm very sceptical myself.

Matthew: Timeframe for publishing the finding? Ahead of the F2F would be good, and think we should rename the repo, but don't have a suggestion.

Hadley: Thought this task was with Jeffrey.

Martin: Suspect we will make a publication decision in Hong Kong. Would be good if we had it sooner.

Marcos: Think it would be worthwhile to put it out in the world.

Martin: Would be comfortable if the rest of the TAG agrees with the points raised there.

Hadley: Martin, think the decision falls to you.

Martin: Want to see if everyone approves the publication. Think we're getting close to that point. Might be easier in Hong Kong, but if we could do it sooner, we should do it sooner.

Hadley: We also have a plenary next week, if you want to present the points?

Martin: Would be much happier if people would read it. It's not that long. Plenary sounds good. Hope it to be done for the plenary, a "please read it" pitch.

Hadley: I will make sure it's on the agenda.

Lola: The API doesn't have an explainer. They put what have been the explainer text in the spec text. Do folks feel they need an "alternatives considered" section?

Marcos: There is a whole document on the alternatives, and that's the custom schemes one. There was no time to come up with other things. But they were designed over the last couple of years.

Martin (chat): There is an explainer, and there is such a section. Thought it was pretty reasonable.

Marcos: Official explainer is at https://github.com/w3c-fedid/digital-credentials/blob/main/explainer.md

Martin: Don't think explainers need to be maintained in the same way. Good thing that the explanation moved to the spec and is kept up to date there.

### [design-reviews#1125: Probabilistic Reveal Tokens (for IP Protection)](https://github.com/w3ctag/design-reviews/issues/1125) - @martinthomson, @toreini, @lolaodelola

Ehsan: Agree with Martin's point, at least the response wasn't convincing for me. Still waiting for them to respond to Martin's latest comment. Suspect it to be the same response as before.

Martin: Problem here is that we asked a question regarding the requirements, but it spoiled down into details.

… Had a conversation with someone on Google's Networking team that is aware of the proposal. Expects to get a negative response.

… Could be perceived as a thing that Google is doing in their browser.

… Think the implicit question is, is this good for the web? Think we can categorically say no.

… It's not correct to advertise a tool that is claiming to hide IP addresses, if it's not really doing that job.

Hadley: Think there is TAG consensus. Can you write a closing comment?

Martin: We should have the conversation, but I think the response will likely still be no.

Hadley: So we wait for a response?

Martin: Yes.

### [design-reviews#1092: Web Authentication Immediate Meditation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @toreini

Ehsan: Jeffrey wanted to know more about the justification. They added an explainer, but there are two more issues me and Martin put in there repo where they haven't responded yet. Waiting for their response.

… Still kind of undecided, leaning towards negative. Want to imitate Android behavior inside the browser, not really justified. Not sure which value it adds from the web point of view.

Martin: I'm with you. Not enough justification to do that. "Unconvinced" is the state I would leave it in.

Hadley: Wait for Jeffrey?

Martin: Yes.

Hadley: Ok, and then do something with this issue, probably close it. From the external perspective, I feel we left it hanging. Ehsan, can you drive this?

Ehsan: Yes, I can do it.

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) - @toreini

Ehsan: Had an initial review, Jeffrey and Martin got back to me. Had a conversation to make a decision on that. Needs more clarification from them. This is progressing, for now.

Martin: Took a brief look at it, explainer is poorly written. Doesn't really explain the how and why.

Ehsan: Looks more like a brainstorming document. Doesn't come to a single proposal.

Hadley: It's totally fair to say that to the proponents, and having them come back.

Ehsan: I would respond to Jeffrey and once he has feedback for me, and ask them to make the explainer more clear. If that looks sensible?

Hadley: Yes. There's a label for "too early," which might be appropriate here.

## Plenary Session - None

## Misc

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven
### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
