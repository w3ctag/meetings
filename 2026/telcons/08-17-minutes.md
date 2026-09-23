# W3C TAG meetings for week commencing 17 August 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-17-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-08-19](https://www.timeanddate.com/worldclock/converter.html?iso=20260819T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Call Cancelled

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @jyasskin, @marcoscaceres, @bkardell
### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel
### [design-reviews#1255: Incubation: Application Capability](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1255) ([Github](https://github.com/w3ctag/design-reviews/issues/1255)) - @hlflanagan
### [design-reviews#1251: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1251) ([Github](https://github.com/w3ctag/design-reviews/issues/1251)) - @jugglinmike, @marcoscaceres, @bkardell
### [design-reviews#1246: WG New Spec: Additional Windowing Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1246) ([Github](https://github.com/w3ctag/design-reviews/issues/1246)) - @jugglinmike, @bkardell
### [design-reviews#1224: Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1224) ([Github](https://github.com/w3ctag/design-reviews/issues/1224)) - @hlflanagan, @xiaochengh
### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan
### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

## Atlantic Breakout (America / Europe) - [2026-08-19](https://www.timeanddate.com/worldclock/converter.html?iso=20260819T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola

Scribe: Heather
    
Attendees: Heather, Luke, Brian, Lola, Christian, Matthew, Dan, Mike, Yves, Hadley

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-17-minutes.md

Raw minutes: ...

### [design-reviews#1254: Incubation: Cross-Origin Storage](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1254) ([Github]
(https://github.com/w3ctag/design-reviews/issues/1254)) - @bkardell, @christianliebel

Brian: The rationale's given for the design includes the fact Google is already shipping the non-isolating cache. The argument is that the sites in the hash list are so common you wouldn't easily be able to tell something about an individual. The cache list, though, seems very large. It feels like this could actually give away a lot of trackable information. There also seems to be information about how to clean up the cache. It seems like anyone can widen the cache but no one can narrow it. That seems uneven in terms of who can say what about the list (anyone can grow it, whether I personally want it to grow or not.) Am I understanding this proposal correctly? 

Luke: That hash string sounds particularly dangerous. It might not identify users at a global level, but it can identify users at more local levels and even that is dangerous. For the particularly popular sites, do you want other sites to be able to tell you visited those sites? The whole point is that you shouldn't be able to track people across the web. Even if it's a large bucket, it's still a contained bucket that can be data-mined. I'm generally un-keened on these cross-origin things. We should just accept the performance hits.

Christian: I am a co-author on the proposal, so we should talk about how I'm to review this. The use case is cross-origin. I share the concern re: cross-origin sharing, but sometimes it is inevitable. The use case that inspired this is AI models. If you have one API but different browsers, you might end up with a different AI model in the background, leading to interop problems. So, what if you can pick the model and download it yourself? It's possible, but AI models are very large. Due to cache partitioning, every origin would have to download their own copy of the model. It's less a performance issue and more a disk space issue. This proposal, not using links or URLs as keys, uses hashes calculated over the file contents, so you can't know if the user accessed a site. The PHL contains resources so pervasive that we can assume it's fine to make them visible to all origins by default (e.g., Google Fonts). We have a different PHL for cross-origin storage compared to the Chromium implementation. 

Lola: How is this any safer than any other cross-origin shared storage proposal (e.g., Shared Storage API, First Party Sets)?

Christian: The main different is using hashes.  You need to know what you want to get.

Yves: We worked a few years ago with someone on the issues of caching and partitioning (see https://w3ctag.github.io/caching-bundling-sustainability/). At that time, there were a lot of privacy issues even with faking the timing for people. There was an issue with payload content. So, it wasn't really doable. Was there a privacy review of this proposal? Also, is it really storage or is it shared cache that you can't write to? Storage suggests you can set things that will be read by another site easily, in which case that is problematic as there could be collusion. 

Dan: I was clicking through the Public Cache List explainer and wanted to know if "some browsers" mean just Chromium browsers? What is the state of the art with proprietary browser solutions?

Brian: I don't think that's the comparison they are trying to make. Chrome is the first one to ship this list, but there are other lists Google works on with other browser vendors. If we can find a single universal interfact to an AI model and allow you to bring your own model, I can see how that would be helpful. We could build a few design principles around the global components for this. A more general cache seems like a harder problem to solve.

Christian: yes, please raise that proposal. To Yves' question, it is not meant to be easily accessible storage. You need to know what you're looking for on the device. That was what we tried to do to enhance privacy. Happy to do a demo on a future breakout. For Dan, also surprised to learn about the pervasive resource list. For Brian, yes, we thought about introducing an API for AI models only, but how do we define an AI model? It's a blob. 

Lola: Please continue discussion in private brainstorm. Dan will be added as the second reviewer. 

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

Brian: There is one we've discussed a few times when talking about Web views: see https://github.com/w3ctag/user-agents/issues/36#issuecomment-5331981342. A lot of the conflict comes with talking about other libraries. Not sure if we need to make that distinction at all. Propose removing that for now.

Heather: If we could add something about the definition of when something turns into a user agent (as per Niklas' content) that would be useful.

Lola: Let's add to the f2f agenda. 

Hadley: I've added it to the spreadsheet.

### [societal-impact-questionnaire#2: Examples]
(https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

skip

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

skip

### [user-agents#56: Use declarative duty language instead of terms overlap with RFC requirement levels](https://github.com/w3ctag/user-agents/pull/56) - @csarven

skip

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

skip


### [design-reviews#1253: Other Spec Review: CSS navigation-based styling](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1253) ([Github](https://github.com/w3ctag/design-reviews/issues/1253)) - @matatk, @dandclark

Dan: I have questions about how this works. Need more time to finish the review.

Matthew: Nothing specific I want to ask right now; am still thinking on it.


### [design-reviews#1249: WG New Spec: Recognized Entities v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1249) ([Github](https://github.com/w3ctag/design-reviews/issues/1249)) - @hadleybeeman, @hlflanagan

Heather: I put some comments in the private brainstorm list.

Hadley: I think I have answers to some of those questions. Will review. This might be more interesting in the context of EU legislation.

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @hlflanagan, @lolaodelola

Lola: Resolved as satisfied


### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

Lola: Waiting for Ehsan to post.


### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

Brian: Luke has been out and we have not had a chance to sync up on this. 


### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

skip

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

Brian: Commenting right now. I'm suggesting some minor tweaks. 

Matthew: The focusability thing came up because they needed it as a building block for carousels. They've also used it for some aspects of scroll. There are some situations where we're concerned this will effect ordering in unpredictable ways. So, unanswered concerns. 

Brian: If we want to try and do something like this (focusability), I think we need to be very careful. The questions need to be answered and we need to point out where they appear to be contradicting themselves. 

Matthew: Then I agree with your suggested paragraph on focasability and that they need to clear up the apparent contradictions. 

Brian: Go ahead and post when you're ready.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

skip

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Heather: This looks good. Waiting for Ehsan to incorporate Brian's feedback and then post. 

Lola: Is this a closing comment? What is the resolution? Need to decide that before the response is posted. Will discuss on the Eurasia call with Ehsan. 

<!-- Reviews that have been pending external action for at least 6 months -->
### Timing Out Reviews (pending external feedback >6months)
### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

Lola: We just need to decide on a resolution and close. Adding to Eurasia. 



## Eurasia Breakout (Europe / Asia / Australia) - [2026-08-20](https://www.timeanddate.com/worldclock/converter.html?iso=20260820T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Luke, Lola, Christian, Yves, Ehsan, Matthew, Marcos
    
Regrets:
    
Scribe: Christian

### [user-agents#22: Implementing the web platform](https://github.com/w3ctag/user-agents/issues/22) - @csarven, @marcoscaceres

Skipped.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Skipped.

### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @ylafon, @marcoscaceres, @christianliebel, @lukewarlow

Christian: I'd like to discuss this in during the f2f, since it's linked to the larger topic of "do we want to have installs"?

Luke: there is a bit of back and forth in the public issue, and maybe we should hold off on that until we have the f2f discussion. Maybe we should even leave a comment that we will discuss the larger topic at the F2F.

Hadley: Should we invite proponents to the F2F discussion?

Luke: Sounds like a good idea. May or may not be linked to the larger topic of installs.

Christian: Would support inviting Alex Russell for the first ~15 mins of the session, and then use the rest of the time for TAG-internal discussion.

Lola: Individual vs. TAG representation is a topic that came up more often.

Hadley: Think we should do a longer session, 20–30mins maybe.

Christian: Happy to facilitate. What is the time frame?

Hadley: Depends on the questions?

Christian: Ok.

Marcos: 

Hadley: Think we have some big picture questions about what we think is good for the web, and separate is what are we going to do regarding what the proponents of this API ask. Christian, can you prepare the session?

Christian: I will, coming back to Marcos first and then to the larger group.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Needs to decide on a resolution label

Lola: Discussed this yesterday, is "satisfied with concerns" correct?

Ehsan: I agree. How is the review communicated to the proponents? Wanted to ask for the strategy first.

Lola: They are going to the Privacy WG call today, after an email thread.

Ehsan: Will read my comment again, if specific questions come up, I will let you know in Slack.

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

Needs to decide on a resolution label.

Hadley: Let’s message Sarven and time this out if we don’t have a closing comment soon.

Yves: Can check the situation.

Lola: From what I read, this can be closed and should be "satisfied." There is a question we could ask Sarven about.

Hadley: My instinct is to close as "satisfied with concerns," seems concerning that there’s no response from the other end. It’s still a working draft, so I don’t think it’s too late. Yves, could you ask the staff contact?

Yves: I will check. Did some research, SHACL 1.2 is currently in wide review.

Hadley: So apparently it didn‘t advance much.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Matthew: Received replies from the proponents, specifically regarding Xiaocheng’s comments on painting. Need to think about them some more, as I’m not an expert in that area. There was helpful explanation regarding the a11y efforts. They didn’t reply to the text metrics question. Would be nice if we could close that gap there instead of having the other proposal for text metrics. This is not included in the answer. But so far, so good, and I will have a look at the reply.

Luke: Haven’t looked at the response in detail yet. Sounds it’s going in the right direction. We should point them at the questions they haven’t answered. I'll spend some more time looking at this and will talk to Matthew.

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Christian: we have a separate meeting planned to discuss this tomorrow.

Marcos: Can somebody jump into the discussion? Comments are piling up and people seem to be jumping to conclusions which aren’t true.

Hadley: I’ll tell them we have an internal discussion planned and will come back to the issue afterwards.

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

Luke: Supportive of this, there was discussion regarding a potential breaking change. Ehsan, are you satisfied with this?

Hadley: Any architectural impacts?

Luke: Not really. It’s changing how scroll containers work in a specific way. It’s an improvement to the current situation (clip keyword but was linked to visibility). Now they are changing it that the clip keyword actually does the clipping. The main thing is the breaking change. Will check the minutes.

Ehsan: I remember this, will look it up today.

Luke: There’s no real rush, I believe this was shipped already.

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh, @lukewarlow

Luke: Previously looked into this. I think I had a TODO which I haven’t done yet. Integration into Navigation API seemed a bit hand-wavy. This is at the edge of my expertise, is anyone else interested? Would that be "satisfied as concerns", if this is editorial instead of architectural? Implementation is there, it just could be written down better. Not sure if that makes for a concern.

Hadley: Depends on whether you think it’s bad enough to hurt the architecture of the web?

Luke: Ok, will check.

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

*Matthew (recently) posted comment; pending external feedback.*

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

*Matthew still working on comment.*

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: Still waiting for the proponents to get back to me on the last comment.

Hadley: Yves, are you interested in this? Looks like you’re not assigned?

Yves: Yes, I’m the team contact, so I would like to avoid being assigned.

Hadley: After another week, we could post another nudge that we’re working on this.

Ehsan: Sounds good.

### [design-reviews-private-brainstorming#217: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217) - @csarven

skip 

### [user-agents#57: Remove overloaded credible commitment](https://github.com/w3ctag/user-agents/pull/57) - @csarven

Hadley: Do we have a session on user agents during the F2F?

Lola: Yes, also regarding web views. Should we do a doc day?

Hadley: Makes sense.

skip 

### [user-agents#54: Clarify payment doesn't change loyalty duty](https://github.com/w3ctag/user-agents/pull/54) - @csarven

skip 

### [design-reviews#1250: Incubation: WebRTC Diagnostic Logging](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1250) ([Github](https://github.com/w3ctag/design-reviews/issues/1250)) - @lolaodelola

Lola: Does not really look architectural, and it’s only about logging.

skip 

### [design-reviews#1256: [wg/immersive-web] Immersive Web WG 2026 Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1256) ([Github](https://github.com/w3ctag/design-reviews/issues/1256)) - @matatk

Matthew: there were two architectural issues. 

1) around this idea of spatial CSS, and we discussed it last week. it's a big feature and they've clarified that they are going to work on that with the CSS WG, it will probably be a CSS WG deliverable, so the right people are working on this. I'm aware that Meta has a different proposal for doing similar stuff, and I asked about it but don't think I got a direct reply. I think Meta has people in CSS, and they'll probably sort that out themselves.

2) High resolution haptics, speicifically in the context of game pads (but not just in game pads). that feels like something you'd want from any part of the platform, not just webXR. And that's the answer that I got. 

A few other points on naming the APIs.

The answers we got were good thus far. 

Luke: There is a participant from Meta in CSS, but I’m not sure if they are aware of that CSS proposal. Is this from Apple?

Matthew: I think so.

Hadley: Does it matter if there’s a competing proposal? Unless there’s a big impact on the web?

Luke: I think it might have such a big impact, also regarding privacy. Interop is a big part of the web architecture. Think Meta is a big player in immersive web. Would be unfortunate if people went down two different paths.

Matthew: +1, concern is if the conversations happened in the right places. Will ask ??? and maybe push a little more on the charter thread.

Hadley: There have been other occurrences where proposals were competing within the same working group. Also, policing the process is not our job. So, is it architectural? We’ll leave this to Luke and Matthew, and we respond next week?

Matthew: Ok.

### [design-reviews#1263: WG New Spec: Verifiable Credential Barcodes v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1263) ([Github](https://github.com/w3ctag/design-reviews/issues/1263)) - @hadleybeeman

Skipped.

### [design-reviews#1248: Other Spec Review: CSS scroll-axis-lock](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1248) ([Github](https://github.com/w3ctag/design-reviews/issues/1248)) - @matatk, @lolaodelola, @lukewarlow

Luke: Discussed last week, seems Matthew is okay with it. I’m satisfied with this personally.

Matthew: APA ran out of time this week, but I agree—I don’t see anything bad. TAG can be satisfied and APA can follow up if need be.

Lola: From my understanding, this hijacks the scroll?

Matthew: it unhijacks the scroll.

Luke: Today, if you move your finger diagonally, browsers will pick a direction and scroll in that. This is a way of opting out of the browser doing that. Think panning on a map, and others.

Hadley: Next actions? Satisfied and be done?

Matthew: Yes.

Luke: Will write up a comment, and post it in the private brainstorm thread.

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242)) - @matatk, @christianliebel

Christian: I'm satisfied with this. It's a low risk proposal, about declarative UI. there si one concrete question here: why are we not reusing a specific HTML element `menu` that has been used before? They said ti might be problemantic for assistive technology. I'm satisfied. Matthew?

Matthew: I'd like to look at it. I saw the answer and thought it was thoughtful. I feel like it should be possible... but Luke suggested things we could find in the archive to see how widely used it is. It would be interesting to do that, see how breakign this would be if you use the original one, If you read Scott O'Hara's article aobut it, it does come full circle.

Christian: the question is: do we have to perform that analysis, or can we ask the proponents to do that for us? I'm not sure we have the capacity

Hadley: we can do either. I don't think it's our responsibility to, we can just ask the question,. but if we're curious...?

Luke: I think the Chrome use counter could be helpful here. It may be enough for us to say "we understand the web compat perspective. do you think this is actually a prolbem in practice? Do you have the data to say that it is?"

That question on whether to use a new element or reuse the menu element will probably come up in WHATWG as well.

Christian: then I was suggest to close this review as satisfied, and ask them to clarify the compatibility story down the road.

Also it doesn't have multistakeholder support right now. There is no security and privacy self-review. Could go in the closing comment. 

Hadley: If the issue is fundamentally if it should reuse an existing element, I’m sure we have design principles that are relevant. Given this is an early review, we could point to them. Who writes the closing comment?

Christian: I will do that.

Hadley: Not sure if we should do satisfied, or satisfied with concerns.

Christian: Let’s go with "with concerns," with the concern being the element reuse uncertainty.

Matthew: +1

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

Matthew: I asked about the braille thing, am waiting for an answer. we'll probably close it as satisfied. 

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini



### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres



### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon



### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk



### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven



## Plenary Session - None

## Uassigned

### [design-reviews-private-brainstorming#302: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/302)
### [design-reviews-private-brainstorming#284: WG New Spec: Attribution](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/284)
### [user-agents#6: A duty of Negotiation](https://github.com/w3ctag/user-agents/issues/6)

