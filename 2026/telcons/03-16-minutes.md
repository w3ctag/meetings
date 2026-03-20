# TAG Minutes - Week of 16 Mar 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/03-16-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20260318T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Brian, Heather, Sen Yu, Jeffrey, Marcos, Dan (late)

Regrets: Xiaocheng

Scribe: Heather

### Web Views

Jeffrey: Note that the issue is the general description; the PRs are the more specific suggestions. 

#### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu



#### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu

Sen Yu: When we show a permission alert, some mini-app vendor show multiple permission in one alert/confirm button, but that's not good. 

Jeffrey: is the super app or the. mini app?

Sen Yu: It's the mini app that want to get multiple permissions, but they are only showing one alert. The user agent should make every alert for one permission, I think. 

Jeffrey: We should put details like that int he permission specs, which talks about the detail of asking permission. If there's an example to help users avoid deception, that fits here. It's right to list all the permissions and to encourage apps to request them in context, but if an app needs a group of permissions (and we've done this with device orientation sensors, where there's potentially three sensors that need one thing) then asking all at once is a reasonable option. 

Sen Yu: That makes sense. But when a developer of a miniapp asks permission, the user always say yes.Multiple ok's are more informative than just one bulk one.

Brian: I agree it makes sense to put this in the permission. But I'm curious about the grouped permissions - are we saying "ask for multiple permissions," but being able to revoke individual permissions independently? If you do ask for them together, do they have to be independently revocable?

Jeffrey: I think yes. Independently grantable. I want to find a way to get at Yu Sen's point as a general principle. The problem here is that mini-apps and some super apps are allowing users to get overwhelmed with a collection of requests, and we don't think the user understands all of it. We want the user agent to present the request in a way the users actually understand what they're being asked. If we can find a way to say that principle, that makes sense in this doc. 

Sen Yu: Let me update the PR after the meeting.

Jeffrey: Happy to iterate on wording in Slack or in the PR.


#### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu

Sen Yu: the cross binding interface element - the text, the permission prompt, and other interface elements. 

Jeffrey: so when you have an embedded thing and you're asking for permission for that thing, how do you tell the user exactly what you're asking for?

Sen Yu: Because the embedded web view is large, and the interface element might encounter much areas, there is not much information that can be shown in the available area. So the prompt indicates very small and the user cannot see it. 

Jeffrey: So, the prompt is constrained to be inside the embedded web view?

Sen Yu: Such interface elements are in the border of the web view. 

Jeffrey: That feels like a mistake on the user agent's part. 

Sen Yu: You see the permission request as full screen? The interface elements such as the indicator about the web view is getting location, or is open in camera - that should be inside the web view or outside the web view overlay.

Jeffrey: In traditional web browsers, we talk about the "line of death" between the URL bar and the content - if you stick something in the content, the user can't tell if it's coming from the browser or the content provider.  So the question is what do we write here to capture that. Like, iFrames and embedded web views impose their own set of problems in interface design.

Sen Yu: For example, should the UA show the UI in the content or over the content?

Jeffrey: In browsers we say no, but for chatbots we might start saying yes. 

Sen Yu: So you think in browser, no?

Jeffrey: In a browser, we treat the iFrame as a top level page and we've moved away from letting the iFrame request its own permission. That's not necessarily appropriate for miniapps and chatbots. It makes sense to have text in here to talk about what to do with embedded content. We need to iterate on that text.

Brian: So, maybe an issue to work it out where the goal is to explain the boundaries of the problem we're trying to articulate?

Jeffrey: Yes

Sen Yu: I will open the issue after the meeting.

Brian: Yes, open up the issue and link to this PR. Thanks!


#### [user-agents#42: Webview: continuous capabilities style](https://github.com/w3ctag/user-agents/pull/42) - @imsenyu

Jeffrey: I suggested some shorter text. Let me know if that's what you were getting at?

Sen Yu: It's ok. What next?

Jeffrey: If there's more than one suggestion, you can commit them in a batch. But since there is only one, just click "commit suggestion" and give it a title. (Maybe apply suggestion. Who knows what GitHub is doing right now.)

Brian: Then we can merge this?

Jeffrey: Yes. Merging. We try to make sure one person has approved the patch, then the author can click squash and merge (usually use squash instead of rebase or merge).


#### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu

Jeffrey: This is a useful example, but I think it's separate from the place you've put it. 

Sen Yu: Should I put this somewhere else? 

Jeffrey: I think you should add another div class example. I don't have an opinion on the order. Then put this in that section. 

Sen Yu: I will do that after this call. 


#### [user-agents#39: Add sth about webview](https://github.com/w3ctag/user-agents/pull/39) - @imsenyu, @jyasskin

Closed.


### [design-reviews#1196: [wg/webperf] Web Performance Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1196) ([Github](https://github.com/w3ctag/design-reviews/issues/1196)) - @marcoscaceres

Marcos: Does anyone want to collaborate on this one? I think it's ready for review.  

Jeffrey: If no one else is interested, I can look along with you.

Marcos: I think it's straightforward, but they've changed the text around the CR criteria and I haven't figured out if that has architectural concerns or not.

Jeffrey: Sounds like we need to wait until we've reviewed next week. 

### [design-reviews#1194: WG New Spec: HDR on the web (CSS, Canvas, WebGL, WebGPU)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1194) ([Github](https://github.com/w3ctag/design-reviews/issues/1194)) - @jyasskin, @xiaochengh

Skipping for now. 

### [design-reviews#1191: Incubation:  Spell Check Dictionary API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1191) ([Github](https://github.com/w3ctag/design-reviews/issues/1191)) - @marcoscaceres, @dandclark, @toreini

Jeffrey: We ought to get this one out. I think we agree on the content of the comments, so we just need to finish putting into one block of text. 

Brian: Yes. I was saying it's there, but I feel weird about putting those words together since I'm on the doc.

Jeffrey: You can propose the text and one of us will post it.

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Jeffrey: I've left some thoughts, but we should discuss. 

Marcos: This triggers the same concerns as DAS; it feels a bit self-damaging. Will review again to see if it's different from what's been proposed in the past. 

Jeffrey: The approach with buckets helps, because you can always run a benchmark and get detail on the CPU's performance. They propose that the buckets be implementation-defined, and that might be a problem. 

Marcos: I will do a first-pass reaction, not a position, in the brainstorming repo, and we can go from there. 


### [design-reviews#1193: Other Spec Review: The revert-rule keyword](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1193) ([Github](https://github.com/w3ctag/design-reviews/issues/1193)) - @xiaochengh

Jeffrey: I've left a private comment that we should probably decline this as a detail the CSS WG does not need to check with us on. I also filed a bug (https://github.com/w3c/csswg-drafts/issues/13510) that I read its spec and didn't see something I was looking for, but that wasn't a TAG comment. But I want to check all that with Xiaocheng. Anyone else have opinions?
...

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @hlflanagan, @christianliebel

Heather: This is what I asked about on Slack with Marcos and Christian, to see if they were doing what I thought they were doing. 

Marcos: I haven't read this yet.

Heather: Marcos and Christian should absolutely be on the tech side of things; I'm particularly interested in the broader ramifications of how this might be used.

Marcos: Definitely raise points that don't make sense from a human perspective. they'll help all readers.

### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Jeffrey: Thought we had finished, but apparently not? I will follow up and draft something.

### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1134) ([Github](https://github.com/w3ctag/design-reviews/issues/1134)) - @jyasskin, @dandclark

Jeffrey: I was asked to look at the comment, I think it's good, shall I post?

Marcos: Sure.


### AOB

Marcos: As part of the DAS charter discussions, we gave them a bunch of feedback and they are excited about standardizing WebBluetooth, Web USB, and other things. See https://github.com/w3c/strategy/issues/530#issuecomment-4072954477.  I think that's cool, but I suggest they bring that to the TAG, but it does fundamentally add an additional architectural layer to the discussion. Architecturally, what hasn't been defined is how to enable the APIs. Chrome uses permissioning, whereas Mozilla throw up a scary permission UI and then a plugin. Those are two different models to enable these APIs, and then there's the larget discussion about how Safari enables similar-but-different powerful features like WebPush. If we're going to standardize Web Bluetooth, we need to think about what model we should be applying to enable these things. Is permissioning enough? There are years of history here that will need to be navigated. This is a great opportunity for the TAG to do something, but it's going to be huge. The other things that play into this about installability - what is it, how to do it.

Jeffrey: This sounds related to what Christian was talking about with regards to the Powerful Features Task Force. Maybe its a design review, maybe it's a finding, but let's start with a design review to capture the space we're looking at the and the question of how installability impacts the permissions requests you get. 

Marcos: We do have time pressures on this. DAS has been given a three-month extension, but there are other efforts also underway. Not sure if we can do this in that three-month window without de-railing DAS.

Jeffrey: File the design review and we'll discuss.

Marcos: What's the good high level?

Jeffrey: I have strong opinions about all this, but I don't want to run over everyone.

Marcos: That's important; we want those strong opinions. 

Jeffrey: It sounds like Brian and Christian are excited to participate, and they weren't involved in the original design, so I'd love for them to drive and chime in. 

Marcos: Maybe you and I could be part of the discussion but recuse ourselves from the final position? Or maybe not quite that far, but some way to recognize the biases. 

Jeffrey: The other thing you brought up that we need to decide whether we have an opinion on: The allocation of specifications to working groups. 

Marcos: What is a TAG concern is whether there are primitive changes/additions the web platform.

## Atlantic Breakout (America / Europe) - [2026-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20260318T180000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Matthew, Dan, Christian, Sarven, Jeffrey, Heather, Yves, Brian

Regrets: Ehsan

Scribe: Matthew


### [user-agents#45: Suggested text for AI-enabled browsers](https://github.com/w3ctag/user-agents/pull/45) - @hlflanagan

Jeffrey: Sent a couple of comments. How's the group feeling about it?

Sarven: Browser warns you when trying to re-submit a form - this could have consequences - this came into my head when reaidng what Heather wrote. It covers AI too. A lot can fit under this category and people may interpret it differently. What's the intention? To be specific, or broader? Where should the explanation fit?

Heather: I was trying to get at the split between being a real-time rendering platform to what AI browsers are starting to do, which is take that a step father, and perform and chain actions without the user necessarily being immediately present. That stretch is what I was trying to capture here.

Sarven: Do we have existing examples of UAs making that stretch.

Jeffrey: I think this is new

Heather: +1, would love to have examples if they exist.

Jeffrey: The document should show up that it's starting to become common.

Brian: Reader mode?

Jeffrey: Reader mode is still consumption; it's interpreting the page in a different way.

... Reading the PR, I think the original wording covers this, if you read between the lines, if you make the reader squint - but we shouldn't do that.

Heather: +1. I think there are things breaking into the UA space - they may not realise they're UAs. The AI companies. I'm trying to put language in here to say 'this means you too'

Sarven: Thinking of examples. Infinite redirects - when the UA notices this may be happening, it may do 5 or 10, as configured, but will stop at the max and tell the user it stopped. Less mature UAs may get sucked into that hole. We don't want the UA to be in that situation. Trying to think of examples where the UA is making decisions.

Jeffrey: I feel like the distinction is whether the user asked for that particular action (directly) or whether they asked for a goal, and the UA is performing the actions. I think Heather's wording is pretty good. I think it's close to landing. We should let Heather thing about my suggestions, and let Sarven review. Sounds like there aren't big concerns, so we could agree on Slack that it's ready to merge.

Sarven: I'll read more.

Heather: Do we need to ask anyone else? Put that out there. How much review is required?

Jeffrey: Sarven and I are editors; this feels like generally not much of a change, as you said, and people should be watching the repos that they care a lot about. We usually accept changes after a breakout discussion if we don't expect someone to have a concern. But if anyone wants us to change that policy, feel free to speak up. But for now let's do that for this change.

### [explainer-explainer#34: Structure alternatives as: Alternative → Pros → Cons → Reason for rejection.](https://github.com/w3ctag/explainer-explainer/issues/34) - @jyasskin

*bump*

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Jeffrey: This means keep making progress on the Design Reviews CG. At f2f the consensus I think was we need to describe it more clearly. Needs a bit more iteration.

Matthew: +1

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

*bump*

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

*bump*

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

*bump*

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

*bump*

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Sarven: We closed the 'concepts' one recently. Now we're looking at what to do with this last one. The group is asking, based on changes they made, can they close the issue. I left a comment just before this call. My concern... I think they went on in this 'versioning' direction, but because of the way RDF is designed, it doesn't have clear error handling descriptions for implementations.

RDF 1.2 introduces some backwards-incompatible changes. 1.1 processors, when they encounter some of the new features, who knows what's going to happen. In reality implementations are decent, but on paper it's not good. The concern I had for the concepts issue is that they did some updates to it, but they didn't respond back to our concerns about implementations that can't handle this stuff. They said they'd fix it in the concrete syntax. We also raised the concerns more concretely. When we look at the N-Triples they touch on it, but not in a way that addresses our concerns.

... I don't know what would be an appropriate TAG response... we told them what we think they should consider. Unless we think that they really need to address this? Not sure where to draw the line.

Jeffrey: I think you're raising important concerns and I think you're right that they've not adequately addressed them. The case of the 1.1 parser running into 1.2 data is really important on the web. We publish the data, we can't control which clients see it. So you need some sort of negotiation. But the MIME type solution wouldn't work becuase old things are not going to be looking at the version part. If new things are required to send the header, maybe that's a solution.

Yves: It's way more complicated than that due to CDNs etc that are not likely to change.

Jeffrey: So if they're not doing the negotiation, they need to handle this in some content way, and it seems they're not. And this is not acceptable for a format on the web, in my opinion.

Sarven: So how do we resolve this? I don't want to repeat what we said either.

Jeffrey: Their reply on the concepts review says they'd rather get that comment on the individual format reviews, so repeating si the right thing to do. The question is whether we are unsatisfied, or satisfied with concerns.

Sarven: The original comment in the concrete one, we did link back to the original review and said 'take this into account'

Yves: It's up to them whether they want to break things or not. We have our opinion bu they are making an informed choice, so it should be 'satisfied with concerns'

Jeffrey: I'm wanting to make sure that we're looking at this from a web format architectural perspective - if you are a web format, forwards compatibility is very important. This design constraint is not something that people who are at the bleeding edge of their domain, working with up to date parsers might be considering.

Matthew: Another aspect of this is we don't know how much in practice the damage will be, but they might not be able to predict the damage either, because we don't know how many 1.1 parsers are out there that can't be upgraded. This could be 'unsatisfied' because we're concerned that this will break things over the web. If we don't have data saying 'all parsers can be upgraded it's fine', then in practice it could be a real problem. Did we suggest or tell them that they shoudl just have a new MIME type, because the semantics are different?

Sarven: 1.2 isn't introducing something that the 1.1s aren't equipped to handle. Even without 1.2, 1.1 can encounter any random thing, and they'll be in the same situation. The version thing being in the payload isn't a new problem category. They'll behave in the same way. 1 possibility is that because they have this new feature written down, there may be a path for 1.1s or their owners to upgrade published data. On the media type, the concern was that in the ecosystem, there are so many different ways of having RDF syntax, so introducing another one makes the Accept headers way too long. Gets the applications into CORS. Concerns about having too many media types. Application shouldn't need to include too many. That's part, but not the whole reason. It's been discussed.

Sarven: quoting RDF 1.2 Turtle https://w3c.github.io/rdf-turtle/spec/#sec-version :
>      This allows parsers that do not support these features to detect      the presense of such features early, and potentially       inform the user, giving them an opportunity to stop the job      or otherwise act on the fact that some amount of the input data       will not be processed as desired.    

Matthew: Everything you said, I accept. But we've had this discussion a few times. I'm sure we had a call where we agreed that there would be a difference in output in 1.1 vs 1.2 parsers over the same document, so it's a semantic fork. If that's correct, it's problematic. Think we should double-check.

Sarven: Isn't that point in the comment I wrote?

Matthew: Might be.

Jeffrey: If we are valuing things differently, we can say, 'we're not convinced by your response; here's our opinion; do what you will' and they can carry on. We don't have to figure out ourselves whether there is this semantic fork. We can ask them to figour out what will happen between parsers and document versions.

... I feel like we should flag that this is a big concern. Sarven is the domain expert here, so if you feel this is only a 'satisfied with concerns' level of concern I'm OK with that - but we should let them know.

Sarven: Highlighting a sentence in the spec: [LINK]

Jeffrey: I think that would have been adequate if that had been there from the beginning, but now they have a pile of 1.1 parsers that don't expect that versioning parameter, and they need to think about what is going to happen when they get unexpected data.

Sarven: But this isn't introducing a new problem to 1.1s. Becuse 1.1 doesn't have that strict way of handling unknown features. That's no different to the ones with this version thing. The problem exists without 1.2 in the picture.

Jeffrey: I think you're saying that the forwards compatibilty is that 1.1 parsers drop data they don't understand, so 1.2 lines in a file will be ignored. I think that's a reasonable answer if that's what the WG says is the forward compatibility story.

Sarven: That was our reasoning as to what the situation is. I suggest they tighten the language in the sentence I just read. I'll leave a draft comment in the private thread.

Jeffrey: Please leave the comment and we can review. Satisfied with concerns sounds like the direction. Can do async.

### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

*bump*

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk


### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Jeffrey: Ehsan proposed a comment; I suggested some adjustments; the group should review the adjustments.

Heahter: Does this relate to the FedCM finding?

Jeffrey: I think it relates; it's one of the little features that might not be in the Core.

Heather: Should we cross reference?

Jeffrey: I think we won't get the finding out in time.

Matthew: Jeffrey's comments look great. Concern about lack of cross-browser support for bounce tracking mitigation - does that mean we can't recommend this approach?

Jeffrey: I think this is not actively harmful without baunce tracking mitigation, but less helpful without it.

Brian: So we should say it's very helpful to also have bounce tracking mitigation, and less helpful without it?

Jeffrey: Yes

Brian: Then I agree with your comments.

Jeffrey: I'll work on this with Ehsan.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Matthew: Outstanding concern was about the level of support from other engines.

Jeffrey: Will ping Lola

## Eurasia Breakout (Europe / Asia / Australia) - [2026-03-19](https://www.timeanddate.com/worldclock/converter.html?iso=20260319T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Luke, Christian, Sarven, Yven, Marcos, Matthew

Regrets: Yu Sen, Lola, Ehsan

Scribe: Christian, Sarven

### TAG Associates

Welcoming Luke Warlow! :)

### [societal-impact-questionnaire#35: Add use case diversity](https://github.com/w3ctag/societal-impact-questionnaire/pull/35) - @csarven

Sarven: Waiting for a PR review. Actually unsure why this is still a PR.

Hadley: Think it’s fine for now!

Sarven: Heading in a good direction. Already limits the potential problem, which was the general tangent.

Hadley: We don't want it to be confused with ethical web principles, but that probably was about the mental health proposal. Anyway, you have my green light.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: We (APA) looked at it, had most of the suggestions in the a11y considerations section that we would have raised. Leaves developer ergonomics. Need to draft a comment.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

(Skipped.)

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Sarven: General housekeeping stuff like adding examples. We have examples for some, but not all questions. Besides the issues on GitHub. Think there were some discussions on what to do with AI. That was split into centralization concerns. Not tackling it directly, though.

Hadley: Centralisation is a good theme there. Anything you or other people need to do?

Sarven: No.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh

Luke: Looks like a replacement request.

Matthew: From last week, didn’t see it yet. Jeffrey put a comment that this replaces [design-reviews#997](https://github.com/w3ctag/design-reviews/issues/997).

Luke: Dubious of privacy impacts on painting on the canvas. Because it can read back pixel data, it might lead to fingerprinting. Think accent colors in form elements. That is being handled, but still, many things could be left over.

Yves: There were timing attacks in the past. Can be bad. Needs care.

Hadley: Luke, if you’re interested in this, read the design review and participate in the private brainstorming thread.

### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel

Christian: this is related to the Global Browser Component topic we discussed in our f2f. Previous TAG said saistisfied or satisified with converns, but not for the baicl local web speech API. Now they want to extend that local API by giving you a quality property, the level of speech recognition quality. Marcos looked at the pull request. Hard to say anything other than satisfied by concerns because we already said that.

Marcos: perfect summary. 

Christian: shall we close it with satisfied with concerns, where the concerns being fingerprinting?

Matthew and Marcos: yes

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @xiaochengh

(Skipped.)

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

(Skipped.)

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Matthew: There’s a reply about one of Xiaocheng’s questions pointing us at Web Platform Tests.

… From the private thread, we ended up with a private comment. From the breakout minutes, we talked about adding that earlier reviews would be helpful. Looks like no one picked this up. Will take care of this, put it in Slack, and then post. We might have to wait until Xiaocheng is available.

Sarven: If they're offering to provide more data, could we get that in any way? Difference between the to engines?

Matthew: Two threads, Xiaocheng raised a question and got a specific answer, and Jeffrey talked about the general timing of reviews before things go to CR. Will draft something and ping Xiaocheng.

### [design-reviews#1035: CSS Gap Decorations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1035) ([Github](https://github.com/w3ctag/design-reviews/issues/1035)) - @matatk, @xiaochengh

Matthew: APA looked at this separately and didn’t have any concerns. Some suggestions about the actual document, but that’s a separate thing. Mainly looking at this from an a11y perspective. See that Lea Verou raised DX-related things some time ago. Checking if that is still relevant.

… Reason why we didn’t close it was because they didn’t put alternatives into the explainer. They have done that in the meantime. Think we can close this fairly soon with satisfied, but want to double-check with Xiaocheng.

Hadley: This is open for a long time, is our feedback still useful?

Matthew: Yes, I think so. Was in touch with the proponents recently, and they’ve updated the draft. Also, they did was we asked.

Hadley: Which happend a year and a half later. Actually surprised that they came back to it.

Matthew: Think it makes sense to take quick look.

Hadley: You and Xiaocheng?

Matthew: Yes.

### [design-reviews#1191: Incubation:  Spell Check Dictionary API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1191) ([Github](https://github.com/w3ctag/design-reviews/issues/1191)) - @marcoscaceres, @dandclark, @toreini

Marcos: Was closed yesterday.

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @hlflanagan, @christianliebel

Christian: this is interesting. The proposal wants to solve this: for example, if you change the country in a form due to an autofil request by the user ("fill in my personal data" in the browser), this may lead to a re-rendering of that form becasue address lines work differently across different countries. And if you re-render the form, the autofil content is lost. So they propsoe providing an event where you can programmatically trigger a refill after basically rearranging the form. Currently what web authoris do is they add all the forms inputs, make them hidden and then physically just move them around.

Sarven: I'm curious about this, concerns on the accesibility repainting or changing visibilitly of forms, values going missing. Were there a11y concerns to begin with with live-updating teh form ,I presume the web page is not updated, it's just a DOM update. Were concerns raised?

Christian: not yet. This is new, we've just started looking at this.

Luke: I wonder if the atomic move DOM operation somewhat solves this case? would rely on them using that for doing their rendering. you can move around elements in the DOM already. I'm wondering why the current solutions clear the autofill. Seems like getting rid of the entire form and re-rendering it, maybe it's not the best way of building the form in the first place.

Hadley: Have a suspicion, form may be structurally different after changing countries, for exmaple counties which are important in UK, but don't exist in American addresses. If you don't find the answer to your question in the explainer, we should ask.

Marcos: Just had a look at the API design. Because you have all of these hidden elements, you may fill in too much fields. Autofill has been around for a long time. Wonder what the privacy implications are, and if it makes the situation better, but suspect that the proponents from Shopify already thought about this. Anyway, these are my initial thoughts, need to check it in more detail.

Matthew: Generally very concerned about the privacy aspects of it. Think I’ve heard people saying that this is a legitimate use case. Seems like a very specific use case. Want to mention what Sarven asked about a11y. Think there’s nothing to this other than dynamic form. The best practice is that you shouldn’t change form fields that are above the current focus. Don't change forms the user has already filled in. Already covered by WCAG. I am pretty interested in this.

Sarven: Also, the browser still needs to differentiate between what is potentially autofillable vs. the parts that were autofilled in the form. The form may have autofilled a bunch of things. What happens if the user cleared an autofilled field and now the form is rebuilt and the field is refilled? To add to Matthew’s point, if it updates things prior to the current focus, they may even end up submitting the form with parts that they didn’t want to submit.

Hadley: +1 to that, this is a big worry. Wanted to say that solutions for very specific use cases can lead to making the big picture worse.

Marcos: Concern is that sites may block/disallow autofilling ("you must type your email").  This might do bad things.

Luke: that's already detectable to say.... there's stuff like the autofill pseudo element and studio class. which sites can use to detect the field being autofilled. so it would be new in that it's more easily script observable. Because I think you'd have to request annimation fram, matches check or something. 

Marcos: WebKit actually types it in, letter by letter.

Luke: Also, validations. Might this work around validations?

Marcos: Really good input, we can try to bring all those aspects together. Need to check what the autocomplete attribute does.

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: We already replied to it. Essentially about how to mirgrate for an installed PWA from one to another. The proposal relies on some assumptions that are not part of the web platform yet - e.g., requiring id in the manifest. Doesn't feel "webby". Yves also suggested some potential alternatives. They replied. They still think they want to continue with the proposed way. The use case is fine but personally not sure if that is the solution - doesn't feel like it. My proposal would be to say ambivalent.

Luke: The same-site restriction makes the use case is smaller in reality. Most of the web is same origin so not sure about same-site makes sense either.

Hadley: Not sure if that migration is mich better, given how big some sites are.

Yves: Comment on multiple PWA re same-origin seems weird. Manifests at the same URL or something else? If you're doing a redirect you already know. Would like to know more about what they mean - ask for clarification.

Hadley: Does Christian's comment in private-brainstorming capture that Yves? Sounds like it'd be good to get something out because they're asking us.

Christian: I don't expect my opinion to change drastically.

Hadley: And also start asking questions and hold off on the comment for later.

Marcos: Haven't had a chance to look into it yet but can.

Christian: Marcos are also editors, so makes sense to have Marcos on board too. I can reply to their question - "we're on it, please give us more time". Not sure if asking questions will lead us anywhere.

Hadley: asking about multiple PWAs on the same-origin is a fair one. Might land better to reply with a question rather than holding off on a comment.

Christian: v1 to v2 of something would be same-site.

Hadley: Something to indicate more is coming. Comment next week?

Marcos: Will look into it.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: The last one we ended up with a philosophical question. They replied. Our question was if they think this is more of a browser feature or feature of a webpage. Seemed like we're putting a burden on the webpage author, and if they want it to do with different colours, they need to do it six times for the different display modes (dark mode, light mode, high contrast, not high contrast, etc). And that's assuming the same colour combination works across the entire site, which it probably doesn't. Getting authors the flexibility and the responsibility, they're keen to do it but the question is what the safeguards are. If behaved differently on different sites, and we've seen variation with colour/size, and ... should be able to do that. Everyone seems convinced. Justification to do with just CSS could do nice effects like match a table row that contains the search text, but it might not be possible either. We're not very convinced for spelling case either. Opening the Pandora's box.  What does everyone think? Resolve in some way? Don't see new arguments. I don't see things changing too much.

Hadley: Say that?

Matthew: Any feeling on this? If it is going to ship - encourage in most accessible way, and maybe just say that, as opposed to just stop it.

Hadley: Make sure to be on the same page with Xiaocheng. You weren't originally talking about accessibility and now you are?

Matthew: I was the whole time. They have to pick colours that work for people. The UA is a better a place to do this. If they're going to style their take search results, dark mode, light, high/normal contrast, and a lot of combinations there. Concern: developers will say "I can use my own search result colours!", seems cool, but then it breaks in ways that they didn't predict for different outcomes. If UA is doing it, it'll pick some colours, and

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

[Matthew to look at this]

## Plenary Session - None




### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
