# TAG Minutes - Week of 23 Feb 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/02-23-agenda.md).

## Atlantic Breakout (America / Europe) - [2026-02-23](https://www.timeanddate.com/worldclock/converter.html?iso=20260223T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Heather, Brian, Matthew, Jeffrey, Lola, Ehsan, Hadley, Dan

Regrets: Christian

Scribe: Matthew

### [explainer-explainer#34: Structure alternatives as: Alternative → Pros → Cons → Reason for rejection.](https://github.com/w3ctag/explainer-explainer/issues/34) - @jyasskin

*bump*

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Matthew: We need to update the name in the README and rename the repository. We called the group "Architectural Design Review CG", so architectural-design-review.

Lola: Also need to pick chairs.

Matthew: Maybe after opening the repo? Also the description is wrong.

Brian: Don't think you can pick the chairs before spinning up the CG. 

Lola: I've had a different experience.

Heather: the CGs are not as tight in process, we can choose how to do it. we can say, "since this is supporting the TAG, a specific TAG member will be chair or liaison or supporting, etc."

Heather: *query on context behind this issue in the agenda*

Lola: We have some issues named like 'review progress on X' to indicate that there is an ongoing document/task on which we want to allocate time to specific issues. So this one is more like a placeholder in the agenda.

Jeffrey: Brian's right that you can't put chairs into the tool until the CG's open - we've already deciced that the TAG will pick the chairs, so we can do that first and then enter them into the tool at the right time.

Lola: Matthew to make the changes, then we can start publicising.

Jeffrey: First step of that would be to propose the CG.

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

Matthew: will work on this

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

Jeffrey: Got WebViews up. Are there any other issues on which folks think we should make progress soon? Becuase the f2f is next week, perhaps we should look over the whole finding next week?

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Heather: *asks about process for picking issues*

Jeffrey: we make issues 'agenda+' to flag what we want to work on each week.

Brian: There were a lot of related sessions at TPAC last year - MiniApps, embedded apps, ... - seems there's not a great definition of what a User Agent actually is.

Jeffrey: You (all new members) are welcome to start editing documents - I can add you.

Lola: Suggest this as a topic for f2f. Please all look at issues and agenda+ them.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Jeffrey: we have a couple of agenda+ things, and a longer set of issues. We have enough queued up and look at this at the f2f and think about it as a whole and what priority we want for the issues we've got.

### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Jeffrey: We've discussed this quite a bit and need to come up with an answer. We have discussed a lot. the Aproach of allowing a template to adopt a stylesheet by naming a specifier was generally the right direction to go. There's a disagreement, IIRC in Mozilla standards position, that this should be targetted to the server-side rendering situation where you'll always have that specifier, it'll be an internal rather than external (needs fetching) stylesheet. They felt that if a URL is named here, it shoudl fetch (even though this is not expected, as the expected pattern of use is with internal stylesheets). Fetches need CORS info, need to know if they block rendering, how to handle errors - the specifiers approach can't provide that info. So they were thinking of using `<link>`s instead - but then you would be using a `<link>` _without_ an `href`.

Jeffrey: specifiers are e.g. if you said `import string` to define a package to be imported. A URL is a string that could go there, but it doesn't have to be. It relates to a package/other resource. Currently I think they're using blob URLs. Having `<link specifier>` instead of `<link href>` is quite a change. Dominic Denicola was concerned about this. I'm not as concerned, but I think we need to be clear on it.

Brian: There's a discrete question: 'should it?' and I think the answer is 'we think probably yes'. But also we should comment that we should really work on getting commitments from other implementers, which should work on answering some of the open questions in the explainer, some of which are rather hard. I think they should take a second look at some of the things they've previously rejected. Some got rejected perhaps too easily. We introducted constructable stylesheets, adopted stylesheets, each adding its own nuances and complexities that developers have to understand. There are probably opportunities to keep it simpler, which I realise is hard. I think some ideas have been thrown out quickly, whereas others have boiled the ocean. I don't think the proposal is terrible, but we could say 'yes' to the discrete question, and give these bits of feedback.

Jeffrey: Some issues include the differences between constructable stylesheets and normal ones - seems CSSWG wants to decrease these differences over time, and we should encourage that. I think some good points on the design constraints have been ignored (not solving the problem that needs to be solved) but I think the proponents are too tied to the solutions that have been used before. Not sure why the constraint that this must result in sheets being included in the adopted stylesheets list _is_ a constraint.

Dan: I understand it's part of this being a declarative counterpart to the current imperative approach - that the DOM would be in exactly the same state. There's a question about whether that is the real design constraint.

Jeffrey: One of the tools I think the use to to server-side rendering is they ask for the InnerHTML of the thing that got rendered, which seems to be sufficient in more situations than I would've expected. Makes sense to provide something that serializes the thing that the imperative JS produces. The `<link>` option provides a way to do both. The adopted stylesheets approach produces references (rather than copies). That difference happens in computer science all the time - I don't think we should necessarily be trying to remove that difference. This gives devs choices.

... That feels like enough for a comment, so someone should draft it.

Lola: do you need input from anyone else?

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Hadley: Need feedback from Marcos and Yves. Sounds like we're close to having a comment to post.

### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1134) ([Github](https://github.com/w3ctag/design-reviews/issues/1134)) - @jyasskin, @dandclark

Jeffrey: Please look at proposed comment.

### [design-reviews#1079: Page-Embedded Permission Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1079) ([Github](https://github.com/w3ctag/design-reviews/issues/1079)) - @martinthomson, @marcoscaceres, @matatk, @heisenburger, @lolaodelola (**Pending >6mo**)

Jeffrey: this has kind-of been replaced by different elements, some of which we may've got individual reviews for. We should be thinking about the individual elements rather than PEPC. E.g. [`<geolocation>`](https://github.com/w3ctag/design-reviews/issues/1140), `<install>`, `<login>`, ...

### [design-reviews#1012: User-defined script "entry points" for performance timing](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1012) ([Github](https://github.com/w3ctag/design-reviews/issues/1012)) - @matatk, @lolaodelola

*marked as pending external feedback*

### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

Lola: Ehsan put in some comments and covers a lot. IIRC Hadley mentioned we could open this as an issue on their repo, but that'd be hard for us to track - but they've not asked us to review this anyway. So what do we want to do with these comments?

Hadley: It'd be helpful for us to keep a copy of our comment in our repo, and open a blanket issue in their repo to point to the TAG feedback. They can consider it and do what they think right with it.

Whoever opens the issue in their repo should be extra kind, since they won't be expecting our review. 

Lola: Heather: does Ehsan's comment cover your concerns too?

Heather: yes.

Lola: I like Ehsan's comment - want to include some editorial issues. Ehsan: Once you've posted your comment, please open an issue in their repo, and point them to it.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

*bump*

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: Brian asked some interesting questions. I'll answer them. About compound attribute value, and wondering about Mozilla's comments.

Brian: Mozilla also made comments on the HTML PR, but they were just asking some questions. Related to my questions, which I also asked in the Open-UI discord: There are things that enable spatial navigation, e.g. with some control key. Should this specify what happens to those? Hard to say what it shoudl or shouldn't say, but didn't see anything addressing those, and they exist in real life. Lots of interfaces that don't work with dpad controllers. Does it take the writing mode into account? Not all questions are answered. Might not be the same: tabs are more like selects than radio buttons in that regards, w.r.t. what reverses and how it interacts with keyboard. Those questions are being asked in lots of places, and we could just endorse the questions.

Matthew: That's a few important questions. Mozilla person was asking about modifier keys. They need to address that cluster of questions. I had a proposed comment, including a request to update the explainer. We have a few questions they should add to the explainer. Orientation thing + internationalization: I don't know. Part of the challenge is they want parity, for good reasons, with how these are named in ARIA. Wider issue that we need CSS logical properties applied to ARIA and this. Can think of good arguments both ways. It doesn't exist yet, so maybe it should exist properly. "Address it before it gets worse."? I'll update my proposed comment to include the questions you just raised. 

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Hadley: We had a good conversation about this last week... there was consensus that this is bad for the web... waiting on Ehsan to update the proposed comment.

Ehsan: Expect to propose the comment tomorrow.

Jeffrey: I'm worried about saying this is bad for the web because the other implementations haven't adopted it - I think we should encourage everyone to adopt it, or everyone not to - others have had the opportunity to comment.

Hadley: We discussed that Jeffrey would need to be part of the discussion.

Lola: I think we may need to reword the design principle about multiple stakeholders in implementation. The design principle can't be 'it must have multiple implementations or it's bad for the web' - multi stakeholder input needs to be considered. (Ref last week's discussion.)

Ehsan: +1 to Lola. Also, as it's mentioed to be related to the agentic web, it may set a foundation for what is to come, so we really need others' input.

Heather: The point I raised last week is that the other browser developers are not active anymore. Apple never was, and Mozilla pulled out. Thus they're taking a position of 'we're not saying no, but we're not roadmapping it at this time'. FedCM as a whole is a heavyweight set of APIs. The bigger it gets without multiple implementations, the more of a challenge it is going to be.

Jeffrey: FedCM exits because of third-party cookie deprecation. Mozilla and Apple are handling it by giving undocumented exceptions to make things like login work. Chrome is trying to get federation right. The undocumented exceptions are bad for the web. We should be encouraging participation by more stakeholders. Not sure how we can do this, but we need to try.

Hadley: A good topic for the f2f. 

Lola: This is part of the feedback we got on the 3pc Finding. We should liase more closely with the Privacy group. At the last meeting, seems like they review specs as they come in for horizontal review, and also is actively working on Global Privacy Control (GPC). I wonder if there's space here for them to be advocating for 3pc replacement work that is moving in the right direction.

Hadley: Last time we had a great converstation, but we didn't clarify what's happening next. Shall we do that now?

Ehsan: I think the plan was that I redo the draft comment that I did, discuss with Hadley and the whole TAG. Then post it for the proponents if it gets consensus.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Jeffrey: On the question of Mozilla and Safari support, this was adopted by CSSWG and they're usually paying attention there, so I've been looking at where it was discussed and checking minutes to see who seems interested. My suspicion is they're interested but haven't replied on the standards positions as that's for Chromium's benefit, so think it's likely they are OK with it. Maybe we should change our intake process to allow proponents to point to support from other vendors in any place. Maybe TAG would want to get hold of any evidence of support that may exist.

### Meet the TAG updates

Matthew: Need to answer a couple questions this week.

Matthew: Catering is sorted for 70 people. We have 17 signed up. Wonder if Dave can send an email to London Web Standards before Saturday. We need to tell them numbers this week, but State of the Browser is Saturday.

Lola: He's been advertising other events, so he can probably boost this. Can also ask Coralie to post. Can post on W3CTAG socials.

Matthew: How many people will be on the stage?

Brian: We could email the AC list and encourage other W3C members in the area to to come if they're interested.

Matthew: I can do that.


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)



## Pacific Breakout (Asia / Australia / West America) - [2026-02-24](https://www.timeanddate.com/worldclock/converter.html?iso=20260224T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Heather, Jeffrey, Xiaocheng, Dan, Marcos

Regrets:

Scribe: Dan

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu

JY: I promised to write a draft, haven't done yet. Happy to hear more discussion otherwise I'll get to it at some point.

### [design-principles#612: Disambiguate when to add global event handlers](https://github.com/w3ctag/design-principles/pull/612) - @domfarolino, @marcoscaceres, @jyasskin

JY: This is a PR that Dom Farolino sent for design priniciples. Think we have agreement to merge, but was a mini discussion between Anne and Dom, but don't think that affects the PR. Think we can merge, then they can make changes if they want.

XH: Can we just say if events need to be handled by [missed].

JY: If we just say elements people will assume HTML. Current approach will help us remember it's all of themn.

XH: That's fine

JY: Sounds like consensus to merge but checks are failing. I'll look into it and get it merged.

### [design-reviews#1191: Incubation:  Spell Check Dictionary API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1191) ([Github](https://github.com/w3ctag/design-reviews/issues/1191)) - @marcoscaceres, @dandclark, @toreini

JY: We maybe have disagreement, or maybe something to send.

MC: I was reading Xiaocheng's commentary about using AI models. Think that's fine but not sure any OS does that. It's good to project future implementations, but proponents should talk about how it's implemented in current OSs. We did that on the TAG side. iOS takes whatever UIKit thing [missed], would be interesting to see how it's done on the Windows side. Web share explainer has good explanation of how to do it on different platforms. That'd be a nice one to point to as an example. ANd give them the feedback that using an array is not going to fly for the reasons I mentioned in my analysis.

JY: Can you link to the xplainer you're talking about? 

MC: Yes. Might have been badging or something.
https://github.com/w3c/web-share/blob/main/docs/native.md

XH: I looked at design doc, think this is not related to OS spellchecker integration. The design doc looks pretty simple, they just unmark words in the custom dictionary. Nothing about OS integration.

JY: I jsut clicked thorugh the design doc link. Looks like it's taking the OS spellcheck result and unmarking the words you said to ignore. Seems usable but not necessarily best option. Makes sense to call that out.

XH: OK approach for preserving privacy, not leaking the custom dict to other origins.

JY: Interesting question about whether calling these APIs might leak info outside hte origin. Looking at the Apple ones I think it won't. But it's possible, Marcos was saying the obvious way to do with Hunspell is to write files, which would leak things. They seem to be assuming they will not leak them, that's the rght assumption.

MC: That's the property it should have, but how is it implementable is what they should investigate.

JY: Given the design doc, question is 'are you sure this is the best way to impl, shouldn't you be integrating with OS APIs. We can send after redrafting, I will redraft comment tomorrow if no one else has.

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @xiaochengh

XH: This is a proposal from Chrome team. Major goal is to support prerendering of form submission navigations. e.g. search results page. This is not covered by existing spec rules API. Motivation makes a lot of sense but I have some complaints, first is non technical. I don't see enough dev signals. They refernce Chromium bug with only 2 stars. Then, regarding their approach, don't see enough justification to add form submission. First reason they give is it allows Chrome to bypass internal checks, don't think this is valid. Second reason is this allows spec rules to avoid waste which I also don't think is good motivation. It's ok if you allow developers to write [missed]. Third point is I do think [missed]. Last thing is speculation rules for form submission, we need to be much more careful because the URL contains user input. E.g. we don't want to do prerender each time the user types. Don't see much consideration of that. I also have a question regarding this part, because it can be considered part of UA duties, but a naive implementation [missed]. Must this actually be specified, or is this something a UA can use to differentiate?

JY: I think this kind of thing should be specified. Otherwise there might be extra fetches if not implemented. We can agree on what the first implementation does, or make changes, but they should start by writing down what they're doing. Separately, this is good feedback.

MC: Haven't looked at fallback model. It adds that new property there. That was the only thing that jumped out at me.

JY: I think it's not described.

MC: It's a dictionary so in old browsers would be ignored so you'd still fetch everything.

JY: Might not fetch it because there wouldn't be links, would be a form action. As Xiaocheng pointed out, they wouldn't actuall prerender the form actions. Might still be worth asking them to write that down in the explainer. Xiaocheng are you good to ac Marcos' concern and send?

XH: About the fallback model. I don't see any problems with that. Re: Marcos' concdrn, in my understanding, speculation rules don't support form submission navigation.

MC: If parser who doesn't know about these, does it drop the prop or the entire rule?
So they have two prerender properties, is really confusing.

JY: In example it's not the same.

MC: If you look at the object, it's two different things.

JY: Won't work

MC: Yeah

JY: I think form_submission=true won't break on browsers that won't recognize it.

MC: My question still holds, it's still weird.

JY: I'm sure that's an accident, you can't make a diciontary like that.

XH: Still a good question to ask. My gut feeling is it'll be dropped if not recognized. I also feel like it probably doesn't matter because form submission is unlikely to appear

MC: Still feels weird because you've got prerender, form submission, a bunch of URLs, if they made a mistake, how do they say to do form submission without a bunch of URLs? Something is weird here.

JY: They've also done something weird in the HTML spec. Don't know that we need to comment on this but hte HTML spec says the ruleset the values corresponding to the rulesset must be valid rules, must not inlcude this key, so you must violate the rule in HTML to use this rule thing. But this kind of MUST is the wrong style of rule in the spec, we constrain the UA, not the document, so there must be another rule that says what to do.

XH: Just noticed Marcos' point, won't be a valid object

JY: Actual parsing says skip the rule if it's invalid according to the rules. It'll skip anything with the form submission field. So not dictionary parsing, it's their own thing. I still feel Xiaocheng's comment is the right one to send.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

JY: CPU performance API https://github.com/w3ctag/design-reviews/issues/1198 buckets CPUs into 4 groups. There's at least one issue about it being implementation defined how they're numbered. I'll assign myself this one, if anyone else wants it feel free to jump on it.

MC: I might.

JY: They fixed some of the issues by fixing the coarse buckets. But it'll be interesting to discuss.

Incubation: Autofill Event #1197 https://github.com/w3ctag/design-reviews/issues/1197

MC: I can participate.

JY: Christian might also be a good person to give it to.
I'll mark it as payments even though it's about checkout.

HF: I'm interested in this one. It has interesting implications.

MC: We should add a Forms topic.

WG New Spec: HDR on the web (CSS, Canvas, WebGL, WebGPU) #1194 https://github.com/w3ctag/design-reviews/issues/1194

JY: All these areas have started adding HDR support but not in a coherent way. Chris is trying to do this in coherent way. This is the kind of thing we should review but not sure we have the expertise.

MC: Lots of people on the WebKit side working on this. There's lots of HDR stuff in iOS.

JY: Who on the TAG is likely to know about or be interested in reviewing this?
<crickets>

If nothing else we should encourage the work to happen. I can assign myself for that.

XH: Don't have much knowledge of HDR but can see if I can help.

MC: I would recommend if they have something concrete, seeking standards positions.

JY: They've filed them.

MC: There's a bunch of people doing stuff on webkit side, so should be able to get good feedback there, I''l bug people in Apple.

Other Spec Review: The revert-rule keyword #1193 https://github.com/w3ctag/design-reviews/issues/1193

XH: I'll look at this.

HF: We talked about the cryptography one (https://github.com/w3ctag/design-reviews/issues/1190) in the morning call this week and last week.

JY: I'll mark as in progress

## Plenary Session - [2026-02-25](https://www.timeanddate.com/worldclock/converter.html?iso=20260225T220000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Heather, Xiaocheng, Christian, Matthew, Yu Sen, Marcos, Dan, Lola, Jeffrey, Brian, Sarven

Regrets: Yves

Scribe: Christian

### Issues from breakout sessions?

Jeffrey: Anything from breakouts?

Heather: Examples?

Jeffrey: If a breakout thought it deserved more attention from the whole group. That’s good things to raise at breakouts.

Marcos: Maybe the DAS issue, which goes a bit back and forth. It may be good to have a TAG response, so it’s not just me.

Jeffrey: Noticed that to happen, I am in contact with Anssi.

Lola: Any other people involved?

Christian: I’m also on that issue. Can bring the concerns forward.

Marcos: Remember that we operate on the TAG level, so this should be regardless of the person bringing the message.

Jeffrey: PLH is on it. Agree that the process parts should be addressed. We are not in the position to block WGs, though. We should reach out to PLH if the next round is unsatisfactory.

### F2F planning

Jeffrey: Should have a look at the Hong Kong and Paris schedules.

Lola: Clarification on row 19, AI?

Jeffrey: Not a particular goal, just felt that topic was missing.

Matthew: Many things to discuss, Ehsan and I talked more about where the model is run, who provides it, etc. Want to give user agents the option to decide where a model could run. Maybe have a standard set across APIs to make it consistent. It may be legally required anyway.

Lola: Is WebGPU related to that?

Jeffrey: Not necessarily, but it may be.

Brian: Can you give me a little more context for the points?

(Going through the points.)

#### Global Component Design Principle

Lola: This comes up recently, it is used when AI models are downloaded locally. Querying locally installed models may create a fingerprinting vector.

#### 3rd party cookies

Heather: Interesting problem space since they are not deprecated in Chrome, but other vendors plan to.

#### TAG Tool

Christian: At Manifest, we have trouble bringing the meeting minutes and issue comments together. This is what the TAG tool does, can we (or others) also use it?

#### Other W3C Task Forces

Heather: Should W3C embrace OSS communities? Or is that too early?

Jeffrey: Certainly makes sense!

#### Health of the Web: Strategies and Metrics

Jeffrey: Big area, can present on Chrome data.

Marcos: That would be interesting.

#### AI

Xiaocheng: Would like to add Generative UI to the AI umbrella. Think it may be too early to write a finding, but raising awareness would be good.

#### Powerful Web Platform TF

Christian: An effort that Lea and Sangwhan wanted to do some years back. Discussions around that topic regularly happen. May make sense to have a discussion platform.

Brian: Agree this would be helpful. Somewhat related to user agents, MiniApps or UI. Discussions with vendors lead to different results. Not exactly sure where the line is.

#### Meta (on scheduling)

Sarven: Not sure if we should split it up on that level, or take a step back.

Jeffrey: We have more topics than slots, so we will have to condense them.

(Group votes for topics.)

#### Topic Assignment and Scheduling

(Topics have been assigned to speakers and scheduled.)

#### Dietary Requirements

Lola: Reminder to fill in the dietary requirements.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-02-26](https://www.timeanddate.com/worldclock/converter.html?iso=20260226T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Sarven, Matthew, Lola, Xiaocheng, Hadley, Christian

Regrets: Yusen

Scribe: Sarven

### [societal-impact-questionnaire#34: Add section for well being](https://github.com/w3ctag/societal-impact-questionnaire/pull/34) - @csarven

Sarven: Updated and merged.

### [societal-impact-questionnaire#32: Explicitly address mental health and psychological well being considerations](https://github.com/w3ctag/societal-impact-questionnaire/issues/32)

Sarven: Resolved.


### [societal-impact-questionnaire#19: Consider societal impact of narrowly scoped use cases](https://github.com/w3ctag/societal-impact-questionnaire/issues/19) - @csarven

### [societal-impact-questionnaire#35: Add use case diversity](https://github.com/w3ctag/societal-impact-questionnaire/pull/35) - @csarven


Sarven: a lot of use cases stem from what a group is loking at. if there is an agreement on use cases, tehre is an exercise to carry this out, and it can unfold in a different way, and then it's in the perspective of what is deemed to be a sensible use case for hte problem they want to solve. it conludes asusmptions on which gorups can implement this, and who will be less or more able to address their needs on the web. there could be implications of the power dynamics in the use cases, so I don't think any spec should just look at the technicalities of how a requriement is written down, but go back and question whether the use cases are well-grounded.

That's the argument about why the group or spec authors should be careful about what htey take on board, and what those architectural decisions may be for the people in a long enough time line. 

Hadley: is this like how we get proposals for slightly better user tracking, but it's still user tracking?

Sarven: sure. it could be a small-scale server or a large-scale. A company that has a lot of users could favour people that ... those decisions could have more harm becasue those servers get to see a lot more data from users, as opposed ot a small server that sees data from 5 users.

I also mention regions and regulatory context. For example, in the Positive Work Environment, there was discussion on whether the US's first amendment should be incorporated into the Code of Conduct. And then others said that the rest of the world doesn't follow the same rules. so that is a case of fitting things to one region, not applicable to everyone else.

Another example: if something is optimised to high-bandwidth speed connection, for a feature to be useful, that might play out for people that are accessing the web from places that have lower bandwidth, are on mobile, etc. It comes back to "which use cases did the group start with."

Hadley: I'd like to have a look at the PR. 

Sarven: another example I've seen: a group wants to have a complex specification, which can be implemented by only large teams. That weeds out who can implement it, and who can't. 

They're different perspectives to look at, how a group selects use case.

Hadley: Both the regional rules and the bandwidth issue, as well as complexity for developers, that we put into EWP and design principles (DP). and want to make sure we are not affectively asking people to jump through different documents. Agree with you that it is an important point. And hoping people don't justify the thing multiple times.

Lola: I wouldn't see it like that. I think this is slightly different than EWP and deisgn principles. I see it more like reinforcing. If we can link to those documents, I think we should take it. If someone submits a review to us, we don't need to say that it is breaking this Ethical Web principle or x,y,z in SI questionnaire and this design principle, and if they are making same or similar point. EWP and DP, carry more weight in some way. This document isn't really as I've been thinking about isn't necessarily for - it is for, more of the beginning of the process, who is affected, and why. I wouldn't necessarily think of people thinking of looking at different places but more reinforcing, and expecting people would be using at an earlier point of the process. Not like you broke this in DP or EWP.. and who is impacted by people and as they're building put the guard rails in place and maybe they can justify in their work.

Hadley: That's a helpful clarification. Using the document at different stage is helpful. Also making explicit is very helpful. Leaving the breadcrumb trail would be a lot easier. Good that you're thinking about this. Making amendments is always on the table re EWP or DP.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: Proponents came back to our comment. Answered question about the DOM and they'll come back to it. Whether it effects focus: it doesn't. performance. The other is cognitive issues and animation could cause barriers, which APA and AG is looking at. The interesting thing is that they've identified there is no specific accessibility consideration for CSS animation, and so they're working on it. so there is a lot in common between two pieces of text which is a good sign. APA will work with them on that. When we / TAG comment, will point that out. Lola had a comment last week.

Lola: Had questions about, their response basically. They mentioned things that I wanted clarifying.  They suggested using contain/cover, for separation between trigger points. Good to use established syntax, but contain/cover is used in a completely different context. This feels like going against work keywords already used. Similar issue with inert issue we had with CSS carousels. Maybe the context is different enough that it wouldn't be confusing, but I doubt it because it is still CSS. 

The second is about wording. They say, whether elements are loaded dynamically or not. Elements coming in or out of the viewport, which are typically elements already loaded into hte DOM. I think our expectation is that we expect it to be done this but it might not be done this way. If the latter, it should be called or addressed.

Hadley: Did you ask these questions or we should?

Lola: I wanted to discuss in the group. Questions are in https://github.com/w3ctag/design-reviews-private-brainstorming/issues/223

Xiaocheng: 
    
Matthew: If we can't readily find contain/cover use of those terms, we should ask them about that.

Lola: 
    
Matthew: The question is worth ask explicitly about causing developer confusion.

Hadley: Reasonable to ask. It's the sort of thing we'd hope to see in an explainer. 

Matthew: The question about stuff in the DOM / if rendered, there is something else about this question, which is, ties into other barriers as well. If animation is critical to the content on the page, then it is not necessary in the DOM. You have to explore them. The animation is when it wants to happen, not when you want to. It might be too fast for some people with accessibility or cognitive disabilities, or distracted. One of the things the APA is drafting is, the animations are not used for absolutely critical and/or the user agent gives the user some agency on the speed that these things that happen. This was also mentioned in the CSS group / that pleased me because they're thinking that. I don't know if the UAs enable that. In general we don't want to use this type of animation unless it is absolutely critical. There are videos where you can provide an alternative, in which case the animation is decorative, in the body or something like that. It is important and there is a more fundamental thing. Good to expose but if the user doesnt have a chance to grasp it before it goes away, there is not much point.

Hadley: Re speed of animation, as a user, would I know enough from the site to adapt it? I'm guessing it is a decision the site developers made beforehand, the speed of animation. Or maybe I could adapt it after I found the site frustrating?

Matthew: Thinking that this should be something the UA should have an idea about on behalf of the user. UAs could do this and they're not writing...

Lola: On the speed of animation thing, what do current animation folks do now. This wouldn't be the first time that issue would've been raised. With other animations or in general, how do they handle that issue.

Matthew: For housekeeping: the consideration section would cover all of it. There is a number of different ways this could be handled to include in our response. Web Platform issue: https://github.com/w3ctag/gaps/issues/15 . It does mention some very high level user requirements. Plenty more we could add, but they wanted to just publish it. This might be a good place to discuss for more cross-platform stuff.

Xiaocheng: Re animation speed, if we're talking about conventional animations, the animation speed is always set by developer, the scroll linked animation is only mechanism where user can decide the animation speed. Re whether in the DOM or not, I'm not sure about any mechanism about animating anything not in the DOM. if the page wants to load. domething dynamically, it has to be done by other means, and then after it's loaded, we add animations to it. Re discoverability of these elements, there is a very similar thing added to the spec, discrete transitions, if we display the type from none to block, with traditional transitions we can't add animations but with discrete transition we can have fading animation. And starting state of transition is display none, and I'm not sure if AT is undiscoverable.

Matthew: display none removes things from the Accessibiltiy Tree.

Xiaocheng: have we reviewed this before?

Hadley: let's check our github issues.

Xiaocheng: Previous design reviews for discrete transitions:
https://github.com/w3ctag/design-reviews/issues/829 
https://github.com/w3ctag/design-reviews/issues/825

Sarven: This is a good topic. it for input the user agent's doucment about...the UA has a good shot, a good sense of hte user's capabilities and needs. So in the UA doucment has an understanding that there are duteis o the UA to fulfill, to protect the user and so on. I can have a look at the doument and see how we can caputre this point about ensruing the user's needs or capabilities are factored in to its decision-making. The UA should provide the controls to control that 

Hadley: I think it's great to put this into the UA document.

Matthew: Sarven just made me say this, 100% million agree. Priority of constituencies! The author's viewpoint has been more important than the user and that's where the problems have come from. Priority of constituencies is super important. This is how I imagine it to work. I have turned up text size in the OS, and the browser doesn't see it but does reflect it. It could be done transparently to the author.

Hadley: why do that in the OS instead of the browser?

Matthew: I need it for other apps too
    
Sarven: another example is dark mode or light mode, which is in the OS and inherited in the browser. I prefer to have that, I trust my OS most, and I want to dictate how the rest of my interaction happens on my computer and browsers want context. so if I set it to dark mode at night, I like my UA to adhere to that. Similar ideas to the controls that are there in the OS for the user's vision... I don't know what controls are there but the UA should acknolwedge that. Without leaking info to the website. 

Hadley: Sounds like we have TAG opinions on this. Happy to support APA on this. Should we put a comment to reflect our opinions on this?

Matthew: We just had a chat that seem to be on the same page. The direction we'd like to see. They already say the UA suggestion, so maybe we take that from them because they wrote it down already. Discretely, 1-2 questions Lola raised, most impotrantly the dev confusion. And UA feature. I'd like to say something about motion gap. 

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) - @csarven, @lolaodelola

Lola: Skip

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: Skip.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Sarven: Ack.

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh

Matthew: We asked questions in 2025-08-14... It is kind of dangling. They took out some stuff most concerning for accessibility but there are some others. Still pending some external feedback.

Hadley: Reason not to?

Matthew: Maybe we should.

Lola: I can ask what the status update is.

Matthew: We asked last about their thoughts and we go no thoughts.

Xiaocheng: +1


### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel

(Christian/added before the meeting: This is pending external feedback.)


### [design-reviews#1188: Other Spec Review: Scoped View Transitions](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1188) ([Github](https://github.com/w3ctag/design-reviews/issues/1188)) - @matatk, @xiaochengh

Xiaocheng: We responded with a question have they considered other alternatives. They replied and updated the Explainer with very detailed alternatives consideration. So closed with satisfied.

Matthew: Yes, good update.

Xiaocheng: Closing...


### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel, @xiaochengh

Christian: We'll come back to this at the f2f

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Matthew: we were pretty happy with this. APA are working with them separately on accessibility considerations. Jeffrey said it would've been helpful to do an early design review of this, but it's a late review. I agree, and I think we can just post Jeffrey's comment.

Hadley: We could say that we can be much more helpful at a later stage. Add to private brainstorming?

Matthew: Done. Do we want satisfied or satisfied with concerns?

Hadley: Expressing our concerns in the closing comments should cover it enough.

Matthew: Drafting. Post it or have reviewed?

Hadley: Happy to let you do it.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Exciting because something happened. =) Heard back from Patrick... long press hadn't been considered and doens't work across platforms. My view is if we can find a way to do it cross platform semantically, because people whilst these interest pop-ups, like the ones on github that tell you the the status of issues, are not giving not giving you anything you couldn't find by visiting the link. Getting the information without visiting the link is great, because everything takes you longer as an assistive technology user.

It's nice to see people exploring this. 

One or more of us should attend the breakout. It seems related. tldr is that it doesn't bring us closer to reaching consensus on this issue - so say we dont' have consensus yet?

Hadley: If you see we don't have consensus but have thoughts of TAG members it'd be a good way forward.

Matthew: Will do and run it by others before it goes out.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: Skip.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)


