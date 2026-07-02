# TAG minutes, week of 29 June 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/06-29-agenda.md).


## Plenary Session - [2026-06-30](https://www.timeanddate.com/worldclock/converter.html?iso=20260630T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair: Christian, Hadley, Marcos, Matthew, Ehsan, Heather

Scribe:

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/06-29-minutes.md

Raw minutes: 

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Heather: any opinion?

Christian: q is how to tackle this. last time we worked on a google doc for prompt api. should we do the same for this?

Matthew: that is a good question. I am happy to contribute to those.

Marcos: I think we should do it differently than prompt one cause I wrote few version of the review and it got messy and we did not have concensus on the core ideas. I think we first need to gather all the positions in the google doc (I did that on slack briefly) and make sure if we cover all the ideas. I want to make sure if folks in data space has a chance especially Sarven and Hadley has more opportunitites to express ideas. I think if we don't get ahead of it, it is going to be a good response. Once the ideas colelcted, we can start generating a coherent opinion on this. Someone would need to lead on putting the ideas together.

Heather: why this is different than private gh?

Marcos: it is also fine in gh. Google doc can be more collaborative, I think it makes collaboration better.

Christian: can you send the slack message Marcos?

Matthew: on the procedure, is it correct that we have pieces collected and then [[??]]

Marcos: we can get our personal positions on gh or google doc, both would work but it is the process I suggest.

Matthew: I think I like the idea of google doc, as Marcos pointed it can get messy. If we want to collect them separately, we can put together a single response in gh private for the record.

Christian: the converstaion can be more efficient in google doc as it can make the conversations better too.

Heather: I like the idea of spanchatting to the private gh. I am happy to start the doc and will send it to the all.

Christian: great, any deadlines?

Heather: I think a week from today sound fair and we can discuss our position by next planery.

Marcos: it is doable. I finished it in an hour and it is not a big proposal.

Matthew: just a thought about deadlines, TAG has been asked to go to the charter of web ML WG. we wanat to make sure if this is based on the timeline they propose.

Ehsan: I think it has been discussed last Thursday.

Marcos: I don't think Apple will oppose to the idea so I don't think it is a blocker.

Heather: shall we take that as action item and move on?

Matthew: yes

### [design-reviews#1127: WebAuthn Level 3: Related Origin Requests](https://github.com/w3ctag/design-reviews/issues/1127) @ylafon

Heather: Yves asked this to be here. I think based on what I see, we are waiting for the WG. Ehsan is only there.

Matthew: there is a transition request 4 days ago.

Heather: did they do what we asked them to do?

Matthew: it is unresolved in the Gh, and they have not respond on this. Can they respond after the call?

Hadley: yes they can

Matthew: it looks like they did add the things we told them not to. 

Heather: phillip said "please re

Hadley: we can reopen issues.

Matthew: it doesn't seem like a good precedent so I am not for it.

Hadley: I don't think it matters for others.

Matthew: I put the link in the chat that goes directly to the text that looks like they added the piece precisely to the spec.

Hadley: what is it that they wanted?

Matthew: it looks like related origins is the issue.

Heather: it seems like they did what we asked them not to. what should we do now? should we reach out phillip and express we are not for it.

Hadley: has our position changed since then?

Matthew: it is a shame they did not respond. Shoudl we ask the chairs of the group and asked them has it changed and did they di anything as a result of our position?

Hadley: yes, for transparecncy, we can put the text in the reposnse and ask the chairs if anything changed based on that.

Matthew: I have put the link, I think Yves already put a comment on this, expressing the sae concern.

Heather I think we need to assign someone as it looks lengthy.

Hadley: I am half way through and it seems no much changed except for the beginning.

Heather: what does it mean to have a MDN checkmark in the diff?

Hadley: I guess reviwed by MDN?

Marcos: it documented and linked to the documentation. The checkbox means it is supported by browsers.

Heather: in that case, if there is no relevance to the topic, what changed?

Matthew: I have put a link in chat on the changed. The section on cross-origin is added. 

Matthew: section 14.5.5 seems to be thee change. It seems it is fair to ask them. I think Ives asked that though. 

Heather: I think we need to ask as TAG that we agree with Ives questions and ask chair about what is going on.

Heather: do you think Hadley should do it or I?

Hadley: it doesn't matter.

Heather: who want to talk about it to webauthn?


### [meetings#60: Agenda building for the TAG f2f: 7–11 September 2026](https://github.com/w3ctag/meetings/issues/60)

Matthew: I have one, I want to point out since the last F2F, I notice this one and webpayment, we have to look at the use cases to check. I think wheels are invented a couple of time. There seems to be duplication of events and it is good to discuss it in F2F. Also, we talked about this last week, that we see couple of different proposals that point to .well-known and because there is not one-to-one communication between UA and server, there's some sort of routing layer on top, which is bespoke - I think we should try to harmonize or standardize this.

Marcos: I won't dive into payment detail but Matthew is correct about the cross-site relations. Some related to capabilities and some related to access control and they are related to each other. I am interested to put a TAG finding I wanted to work on long time ago.

Hadley: I have a big list for this

Marcos: should we have a repo for this?

Hadley: sounds like a good idea.

Hadley: I also see the pattern in advertising where advertiers/intermediatories want to have a trusted relationship with the top-level page so it can inherit some of the permissions (to make them special). this is alarming as it will be bad for the web.

Matthew: we should make it a pinned repo on the TAG repo as we want encourage people to give us feedback on it. It was a time ago we had something about gaps. It is worth if there is anything there we can put for agenda.

Marcos: I remember it wasn't a good experience. I remember we could not bring them over before as they were not good fit for purpose (?). The web is absolutely comptetive so it is better this is tried on other platforms. I would be motivated to ask "what would be good for the users, from the gaps", we can discuss it in the f2f. 

Matthew: I agree. I have not seeing it getting compared to other platforms and this is areasonable thing. Shall we change the repo name to "wishlist"? I don't thin the intend here is to call for things missing...

Marcos: I agree with that.

Hadley: I am offering renaming it. I wonder if we go with the wishlist, whether it will include that we spot and bad for the web and we want to be removed from the web. I don't want to ??

Matthew: we could propose closing the ones that won't fix. we can keep them open forever.

Hadley: maybe. we can also have the discussion in the future and adapt based on what happens.

Heather: we need to focus on the scope of the thing.

Heather: any more topic?

Hadley: we started to talk about a document about gathering things that web pages do things that a user would not expect. I want to work on that.

Matthew: I would like to contribute to that document. For me, "people think that the data they put in a form only goes on when people press submit button". Is there any private repo as I want to put agentic finding there.

Marcos: it is private-by-default.

Hadley: do we have a repo on the draft finding.

Matthew: is there any developer meet-up in the F2F?

Hadley: yes

Marcos: I need to find space in the Vancouver office. We can ask Mozilla office as they seem to have an office there and they have developer offices usually.

Heather: this sounds like something that is traditional.

Marcos: yes it is

Hadley: the theory is that we get with developers so we can have feeling of the real challenges. we used to have hackathon and we can do those too.

Marcos: I can ask over slack but need to colect info on the people attending for sending to security office.

Hadley: put that in the document you shared with us.

### Breakout Rollup

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Pacific Breakout (Asia / Australia / West America) - [2026-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20260701T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Cancelled

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu

### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu

### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

### [design-reviews#1233: WG Revision: CSSPseudoElement](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1233) ([Github](https://github.com/w3ctag/design-reviews/issues/1233)) - @bkardell, @xiaochengh


## Atlantic Breakout (America / Europe) - [2026-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20260703T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Present: Matthew, Heather, Yves, Christian, Mike

Chair: Christian

Scribe: Matthew

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/06-29-minutes.md

Raw minutes: ...

### [design-reviews-private-brainstorming#217: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217) - @csarven

(Skipped.)

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

(Skipped.)

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

(Skipped.)

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

(Skipped.)

### [user-agents#2: Do we need a "discretion" duty?](https://github.com/w3ctag/user-agents/issues/2)

(Skipped.)

### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin

(Skipped.)

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

(Skipped.)

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @hlflanagan, @lolaodelola

(Skipped.)

### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

Heather: Did we decide this was out of scope, or we are unable to participate? Team working on it?

Yves: Simone worked on this from a security perspective.

Heather: Should we say this is individual participation only; not TAG?

Yves: Depends on scope of the review. If it's security related then it's better to have security people work on it.

Heather: So individual contribution is OK? But not TAG?

Yves: I think it would be hard for TAG to come to consensus?

Christian: Is it architectural? Or just definitions? What's the scope of the review request? The entire document?

Heather: Looks like.

Christian: It's very long. Not sure we can do this at all. Think we should decline it, stating we can't do it in that timeframe. I think it's within TAG's scope, but too long for us to process in the timeframe that remains.

Christian: Yves, could you check with the team if/how we can engage with this request, and what the scope is?

Yves: Yep

Christian: I'll send a response in the GitHub thread, and Yves is going to check on it within W3C.

### [design-reviews#1236: Other Spec Review: `textStream()` for `Blob` and `Body`](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1236) ([Github](https://github.com/w3ctag/design-reviews/issues/1236)) - @dandclark, @lolaodelola

(Skipped.)

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

Matthew: Proposed the beginning of a comment. Need to verify how the video element works, will ask them tomorrow.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Yves: I think last we discussed this, we arranged to put it on the f2f agenda, and revisit there.

Heather: Yes, it's on the agenda.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Heather: I looked at this and posted a few questions in brainstorming. Had some about whether I was reading it correctly and if this is turning browsers into advertising data processors, and whether we are OK with that, as it seems like a big leap in terms of what browsers do.

... Also some decisions like making empty allowlists meaning global permissions, which seems inconsistent with the rest of the platform, and general convention, and thus concerning.

### [design-reviews#1223: Other Spec Review: Responsively-sized iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1223) ([Github](https://github.com/w3ctag/design-reviews/issues/1223)) - @dandclark, @toreini

(Skipped.)

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

Yves: It's more generic, about service discovery. I said last time, using DNS for this seems clunky, and prone to spoofing. Mark Nottingham wrote an article about .well-known - need to discuss with far more people to solve it.

Heather: we did add this to the f2f agenda as we agreed there's no good way to do this. The WG is going ahead with the idea of a .well-known as they don't have better ideas. This is going to be another bespoke solution, until everyone figures out a path to service discovery.

Yves: Original question was about a 'web way' to do service discovery.

Matthew: There were a couple examples that I'm aware of about using .well-known but then needing to do something on top. One was for discoverable destinations. Helping people navigate around sites. There's also a proposal for accessibility problem reporting; if you're having a problem accessing a particular website, they could have a service set up to receive reports. Is the service a subdomain or a route? There are several more. We could collect them... The one for changing passwords: there is a W3C spec for that . IT could be struggling with the same thing. We have someone from the Adapt [sp?] task force; you could have one password for one subtree of a site but a different password for other subtrees.

Mike: Might we apply an issue label for "service discovery" so that we can begin to build a corpus of case-studies?

Heather: We had a bit of a discussion at plenary about labels and how tomake them as useful as possible, w/o having a proliferation that we can't track. Maybe instead of labels, we could have an issue that we link other things to (like the 'make progress on' issues). Anyone willing 

Mathew: I agree with the idea of using an issue to track this. I guess we would put it in Design Reviews--a separate type of issue. I guess we'll see if we break TAG Bot by doing that. I guess if it's a design review, we can put the design review number, and if it's something else, we can just put a link.  I will create this issue.

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: We discussed this a bit, and I looked back into, and it looks to me like we can close it as "satisified". There is work they need to do about developer awareness, but that doesn't need input from us, and they don't need any help.

Christian: Should we simply say, "We are satisfied"?

Matthew: We've had a good conversation with them already, and it's been a while since then. I could post, "we are going to close this as satisfied" by the end of the week.

Heather: I like that approach.

Matthew: Then I will do that.

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Mike: Last week Ehsan volunteered to incorporate feedback into the comment and post it. I'll ping Ehsan in Slack.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

(Skipped.)

## Issue Triage

### [design-reviews#1241: [wg/atag] Authoring Tools Accessibility Guidelines Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1241) ([Github](https://github.com/w3ctag/design-reviews/issues/1241))

Matthew: A question could be, when is this expected to be done?

### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240))

Heather: I'm interested in this. This would be a good one to get Marcus to review if he would be up for it.

Christian: He should be there tomorrow.

Yves: Just looking at this briefly, I wonder if this might be related in some ways to BF Cache--extending how things are evicted from the cache. I didn't review the spec text.

Christian: Maybe can assign the three of you tomorrow

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235))

Heather: This has been open for a while, and we're trying to find another person who is qualified to look at it. So far, we've looked at is on the Pacific call and said, "no one here wants it."

Matthew: I think someone on tomorrow's call will be able to do it. Maybe Luke, Brian (or Lola, though she hasn't returned, yet)

Christian: Okay, let's try tomorrow, then.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-07-02](https://www.timeanddate.com/worldclock/converter.html?iso=20260702T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Present: Marcos, Matthew, Ehsan, Luke, Christian, Yves

Chair: Christian

Scribe: Matthew

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/06-29-minutes.md

Raw minutes: ...

### Renaming 'gaps' repo

Matthew: Talked about this yesterday. Shall I ping in Slack?

Marcos: There was a good name...

Matthew: 'Wishlist'?

Marcos: Yes. But there's also a proposals/wish list for WICG - https://github.com/WICG/proposals/

Matthew; I think the aim of the 'gaps' repo is higher level than proposals / earlier. We must've been aware of this when setting up the 'gaps' repo... maybe we wanted earlier, or more direct, dev input? Having a very easy way for devs to provide feedback.

Ehsan: Is that the idea, the audience is more open to developers.

Marcos: Concern about people inadvertently contributing IP they don't have a right to.

Luke: What's to stop someone just filing an issue on the HTML repo asking for a particular feature? Wouldn't it have the same problem? We're looking for thigns they want to do / gaps, not an API shape, which is where I think IPR stuff would come in more. WICG proposals are more oriented at an understanding of the solution, even if it then gets incubated and changed.

Marcos: We should check with W3C legal that this is OK. If you file a new issue for WHATWG there are contributor guidelines.

Yves: Basically the same in W3C... if you just file issues it's not usually IPR protected, but if you propose a solution for something. text in a normative spec that adds more than editorial changes, then either you're backed by your employer (if W3C Member) or there's a page where you have to commit to rights agreements. That's the point of the bot we have that goes through all the PRs on specs, and blocks if the IP is not clear. It can be dismissed because it's editorial only, or the people went through the declaration. It's automatic if people linked their GitHub account to their W3C account.

Matthew: Propose rename gaps to wishlist, happy to do that. Good to have a place where people can file stuff in a chill environment. I will put a question in Slack in tag-all, pin it, and give people a week to respond.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: Waiting for a thumbs-up from Lola to say we are satisfied.

Luke: "No one filed an issue" is not necessarily proof that developers are not confused. Not sure if developers would do that. Maybe we should push back on this mindset.

Matthew: Will have a look, might add that to the comment.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

(Skipped.)

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

(Skipped.)

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

Matthew: Is ARIA Notify architectural or not? My understanding is: This is not controversial. Checked browser positions, and didn’t notice any controversies. Luke, any background on browser positions?

Luke: Haven’t looked into this, no pushback whatsoever. Work needs to be done on the screenreader side, but that’s for the next iteration. Same as live regions. Recollection is that it is well supported by everyone.

Matthew: MDN says it’s not implemented yet.

Christian: So do you want to close it as "satisfied" now?

Matthew: Not controversial, think it’s good, but lacking support as per MDN. Don’t want to special-case this.

Luke: MDN is not super clear. Implemented in Chromium (Win, Linux), and is in Firefox. Believe it is in Safari as well. There is a WebKit standards position that is supportive.

Christian: Which would support "satisfied"?

Luke: Doesn’t have anything for Braille though. There is an ARIA Braille label, where you can provide a different version. Does it need that? Don’t think it blocks V1, but maybe should be added?

Matthew: Think that was covered in the explainer, and think it was postponed to the next iteration. Will check that, and if it’s missing, add it to the comment. Will be satisfied.

Luke: Agree.

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @ylafon, @csarven

Yves: We had a meeting on Tuesday, in which I explaiend my draft comment's position. It's all about predictabiltiy of what is going to happen next, and it allows you to have a strategy about what happens next (future versions). Agreed it needs to be discussed. There's not a possibility to solve it now, but they need ot be clearer for the future. So I will move my comment to the public repo.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Yves: Action was on Ehsan to write closing (satisfied) comment.

Ehsan: Correct; will do.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Matthew: Last time Luke mentioned an issue whether it renders elements that are outside of the canvas. Elika gave me a link to that issue, so I put that in my private comment. Seems to me that things like that would change developer experience significantly. Seems like details still need to be worked out. Everyone please look at the proposal. Also found things related to the text metrics which we discussed. There are also some general concerns. Also, asking to extend the scope to address the text metrics proposal. Could start drafting a comment along these lines.

Luke: SGTM, specific/general concerns should be included so they can respond. Issue that Elika re child nodes is important and should be added. On a11y, is that part of what is shipping? Seems there is no reason to do the other proposal. Important to point out.

Marcos: Should we drag them into a call?

Matthew: Person presenting on text-metrics was acknowledging the TAG feedback, but said it would ship anyway. I might add a comment on the closed text message thread, and ask things not to be done until HTML-in-canvas is done. On Elika’s issue, need more time to respond to this. There was another proposal, do you have the URL?

Luke: Supporting adding a comment right now, and add details later, don’t think this needs to block the comment.

Matthew: Will do a quicker comment, we might even get it out this week. Draft it today.

### [design-reviews#1228: Other Spec Review: overscroll-behavior: chain](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1228) ([Github](https://github.com/w3ctag/design-reviews/issues/1228)) - @lolaodelola, @lukewarlow

Luke: I will double check the minutes, but think the conclusion was we were happy with this overall, but provide some input on bits that were missing from the explainer. Will follow up with Lola.

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

Matthew: Another one where I proposed a shape of a comment. Got the impression that everyone except me like this. See the benefit, but I also see why this can be a really bad feature. Recommend that UAs can opt-out of that via a toggle in a11y settings. Seems like introducing non-determinsim to layouting. Wonder how this will affect developer experience. WCAG 3 approach is slightly different. Might make things much harder to read.

Luke: On turning it off, in an ideal world that would be great. In a real world I don’t expect UAs to implement that, similar to interest target and the delays due to observability. Personal opinion is, a11y concern should win. If the feature seems very problematic, we should then rather say that.

Matthew: We could say "don’t make the text too large/too small“, but that might break the feature. Generally, a11y and design don’t have to be in conflict, but sometimes it’s inevitable. We shouldn’t put people in a position where they should trade off a11y with privacy. Will come up with an indication of how it affects (how many) people. It may only be a few, but they may be heavily affected. Worried about privacy issues related to a11y, but this is an aesthetic thing. Might discuss this during a breakout at TPAC. Would love other people’s opinion on this.

Luke: This key bit needs a discussion, it has come up before. Like, "this is our red line," and then we need to stick to this. Guess that’s like CSS grid lanes, which doesn’t see much usage. Is that worth it with the possible harm? Personal opinion is no.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow

(Skipped.)

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

(Skipped.)

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

(Skipped.)

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

(Skipped.)

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

(Skipped.)

## Issue Triage

### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240))

Marcos assigned.

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235))

Luke will join the review.

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242))

Matthew & Christian added.
