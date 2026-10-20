# TAG Minutes — Week of 19 October 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/10-19-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.


## Plenary Session - [2026-10-20](https://www.timeanddate.com/worldclock/converter.html?iso=20261020T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Heather, Sarven, Christian, Hadley, Jeffrey, Dan, Lola, Marcos
    
Scribe: Sarven

<!-- Agenda+ -->

### Publish Findings

#### [user-agents#73: User Agents](https://github.com/w3ctag/user-agents/issues/73) - @jyasskin, @csarven

Jeffrey: We're hoping to publishing the doc as a note before TPAC. There is one PR we can discuss just before. npdoty reviewed. I think we should merge and publish.

Hadley: A little concerned that we didn't give anyone a heads up before publishing. Did everyone review / have a feeling? {Noticing nods}

Hadley: Let's carry on.

Hadley: Do we have consensus to publish this (now that PR 66 is resolved)? Noting no concerns.

[The TAG has consensus to publish this as a Note.]

Jeffrey: Good to go. Two follow ups. Sending a PR to infra to update the def and taking the duties the out of privacy principles doc and referencing this instead.

Sarven: and thanks to everybody for getting this out the door, and guiding everybody. and for helping me figure out things since I started working on the TAG. And to Jeffrey, for bearing with me. We've come a long way with this.

Jeffrey: and thanks for pushing us to actually publish this.

##### [Add an EME example of making credible commitments. user-agents#66](https://github.com/w3ctag/user-agents/pull/66)

Jeffrey: Somewhat of a long example on how EME happens. UA vendors negotiating an agreement effectively between users and websites. A part of that is commitment device mentioned in the loyalty section. The content of a bargain depends on the content. Need to look at whether the UA vendors did a good job at collective bargaining.

Hadley: What now?

Jeffrey: Should we merge this?

Heather: more of a procedural q. Is there a process to update a Note later?

Jeffrey: We can update as we go. Any PR after this we'll want to get the same consensus as though publishing a Note.

Hadley: We can do the same procedurally for Findings too.

Hadley: Noting a mild potential reputation risk. Happy to defer to editors re EFF stuff.

Jeffrey: We kind of cover all - everyone happy and mad.

Hadley: Editors can decide.

Jeffrey: Will merge.

Hadley: Would anyone like to do a blogpost on the Note?

Jeffrey: Sarven and I can.

#### [Install Finding](https://github.com/w3ctag/install-finding/issues/9)

Christian: Ready to publish. One point raised by Brian on some wording. We can make some adjustments. Apart from that ok to go.

Hadley: Second Brian's concerns. Good change.

Jeffrey: Happy to help write that PR. Maybe w/ a day for people to object.

Hadley: Do we want to get consensus now pending that change - may be a bit awkward.

Christian: It'd be good to do that if possible. Changes perhaps the intensity and not much of the content.

Hadley: A small possibility someone may object but besides that it is probably fine.

Jeffrey: We can discuss on Slack.

Hadley: Do we have TAG consensus to publish this Finding? Any abstain or disagree? {Looks} Sounds like consensus to me.

[The TAG has consensus to publish this as a Finding.]

Hadley: Would anyone like to do a blogpost on the Finding?

Christian: I can.

#### [Agentic Browsing](https://github.com/w3ctag/agentic-browsing-finding/issues/3)

Christian: Context of WebMCP review. It'd be cool ??? Parts related to Agentic browsing and do the review in parallel. Label with proceed with caution. This finding may be one piece of the puzzle. I'd like to have a larger discussion on the topic and not specifically on the finding.

Hadley: Makes sense. One bit to focus on first. You mentioned one we might not have consensus yet.

Christian: ... to address Jeffrey's issues. To do it async.

Hadley: We can ask for consensus today. Expecting it?

Christian: No.

Heather: I don't tihnk we can get consensus yet.. a lot of PRs to have a look at. Need time to think about it.

Jeffrey: There are also style guide issues after that. It points in the right direction but not polished yet b/c we need to have a better look.

Hadley: If ideally people can look by Sunday, we're meeting on Monday.

Christian: Sure. It won't resolve the WebMCP side of things. I'm personally all in to get something out by TPAC.

Hadley: Are the issues substantive or editorial?

Christian: Editorial.

Hadley: You can send a heads up note to the working group about that so no shockers by Monday.

Heather: EVen if we have consensus but it won't get published until after TPAC.

Hadley: My question was whether a Finding makes sense given how fast this lanscape is moving. I wanted ot ask that question. Separately, we have in the past, e.g., third-party cookies, privacy-sandbox, we just wrote a doc and eventually published. It wasn't formally like a W3C, and we looked at it from different angles. It was very hands on so that we didn't need to repeat ourselves. It served its purpose then. We have choices depending on what we want to accomplish with this.

Jeffrey: In response to current state of play, things might change in a year, but this is our opinion now. I think some of the issues are not entirely editorial. The quesiton of what we say about private browsing mode for example. It doesn't change the overall direction but it would help the doc to be taken more seriously.

Christian: I lean to Jeffrey's opinion. The question is there needs to be a finding. All of our current understanding. I think we should say what we think. We should settle down somehow.

Matthew: One of the things I suggested was to separate re agentic browsing and webmcp, ??? happy to do that . Point that it is not just WebMCP. Defining the Agentic Web Finding is perhaps describing agentic browsing in more general terms.

Sarven: +1 to Hadley, Jeffrey, Christian that the landscape is moving. I'm not sure to what extent our understanding of it is stable enough for a finding. But also, it is our understanding, which is good.
Next weeks we will even improve our understanding or knowledge oabout what hte webmcp folks think. is there a rush to have this consensus now rather than after TPAC?

Christian: I think it's pretty... what we want to say is stable. I don't expect big changes here. But I support doing all the stuff, not rushing the finding and still sharing our thoughts. 

Hadley: Glad we talked it through. What is the next best step for that?

Christian: I can come up with a draft still captures what we think. And group can async. A draf to the comment.

Hadley: No harm in duplicating that in the finding. SEnd to the group with a timeout date if I don't hear from you

#### Societal impact questionnaire

Sarven: Lola and thought we could talk about what kind of feedback we're willing to incorporate on this particular note and what to leave behind for future updates. We already have TAG consensus to publish, but are just doing due diligence.  https://github.com/w3ctag/societal-impact-questionnaire/issues/49

Hadley: if you've already got consensus, then the feedback should be for the future? 

Sarven: we didn't want to get heat from the community. We're aware that we don't have to ask for wide review for Notes per Process.

Hadley: The TAG doesn't have to do wide review, we only speak for ourselves. it's ok to say "we will consider this in a future round," or "we are going a different direction with the document."

### [process#50: Re-wording TAG review outcomes](https://github.com/w3ctag/process/issues/50)

Heather: We've talked about this several times. Reworded several things. What else does the group want to do? Do we need end-to-end list of what we'll do? Or just use the issue?

Hadley: Reading the issue, we don't quite have a proposal on how to proceed. What's the decision on?

Heather: Sounds like what people are looking for is an end-to-end proposal to get a thumbs-up or not. Happy to do that, but it would be helpful if, in the comments, to give comments thumbs-up/down. Also on Yves' comment.

Hadley: Feedback now or in issue?

Heather: If people need some time, I'll keep an eye on it. Not super-time-critical, because we're not making the WebMCP comment today. But want it ready for that.

Christian: It’s also not super time-critical anymore given we won’t put out the WebMCP comment now.

Hadley: My big concern is where we have authority and where we don't. We have experience and time commitment to do stuff for the web. I've seen where we think something is bad for the bad, blocoking/stopping but we don't have authority in the process or in the discussion. We have opinion. If we can raise more comments along the lines of what's going to work or not, to the webarch, and we want you to stop, then that can be said with more confidence.

Heather: can work with that.

Jeffrey: I htink Heather's most recent comment does a good job of that. The alternative would be like objecting, even if we can't block. Ok with the latest proposal. Where Yves says blocking, which is more worrisome.

Heather: THe full list is what people thought may be hard to get consensus on but instead drill down on what we need the most - e.g., proceed w/ caution.

Hadley: I'd feel better rather than block or not. If we are in a position to block it changes the nature of the TAG. We give advice. Want to move away from that flow.

Heather: "can if you like"

Hadley: Feel the same for proceed w/ caution.

Heather: I have enough to play w/ here.




<!-- PRs -->

### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan, @jyasskin

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

<!-- Design Reviews -->

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Hadley: Good discussion for TPAC.

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel




## Pacific Breakout (Asia / Australia / West America) - [2026-10-21](https://www.timeanddate.com/worldclock/converter.html?iso=20261021T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: 
    
Scribe: 


<!-- Agenda+ -->

### [design-reviews-private-brainstorming#306: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/306) - @bkardell, @jugglinmike, @marcoscaceres
### [design-principles#619: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-principles/issues/619) - @marcoscaceres

<!-- PRs -->

### [design-principles#621: Add new fragment directive guidance](https://github.com/w3ctag/design-principles/pull/621) - @marcoscaceres, @bkardell, @dandclark, @jyasskin

<!-- Design Reviews -->

### [design-reviews#1268: Other Spec Review: Registries developed by the Media WG](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1268) ([Github](https://github.com/w3ctag/design-reviews/issues/1268)) - @hlflanagan
### [design-reviews#1246: WG New Spec: Additional Windowing Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1246) ([Github](https://github.com/w3ctag/design-reviews/issues/1246)) - @jugglinmike, @bkardell
### [design-reviews#1251: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1251) ([Github](https://github.com/w3ctag/design-reviews/issues/1251)) - @jugglinmike, @marcoscaceres, @bkardell
### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres



## Eurasia Breakout (Europe / Asia / Australia) - [2026-10-22](https://www.timeanddate.com/worldclock/converter.html?iso=20261022T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: 
    
Scribe: 


<!-- Agenda+ -->

### [design-reviews#1256: [wg/immersive-web] Immersive Web WG 2026 Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1256) ([Github](https://github.com/w3ctag/design-reviews/issues/1256)) - @marcoscaceres, @matatk

<!-- PRs -->

### [w3ctagbot#222: Organise Issues and PRs According to Meeting Labels](https://github.com/w3ctag/w3ctagbot/pull/222) - @lolaodelola
### [privacy-principles#469: Suggested new sub-section to 1.2 (Vulnerability), titled "1.2.2 Vulnerability Impact"](https://github.com/w3ctag/privacy-principles/pull/469) - @toreini

<!-- Design Reviews -->

### [design-reviews#1283: [wg/rml] RML Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1283) ([Github](https://github.com/w3ctag/design-reviews/issues/1283)) - @bkardell
### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel
### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow
### [design-reviews#1284: Incubation: Web Haptics API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1284) ([Github](https://github.com/w3ctag/design-reviews/issues/1284)) - @christianliebel
### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @christianliebel, @xiaochengh, @lukewarlow
### [design-reviews#1278: [wg/ARIA] [Accessible Rich Internet Applications] Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1278) ([Github](https://github.com/w3ctag/design-reviews/issues/1278)) - @lolaodelola
### [design-reviews#1266: Other Spec Review: Scroll snap for single-axis scroll container](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1266) ([Github](https://github.com/w3ctag/design-reviews/issues/1266)) - @lukewarlow
### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh
### [design-reviews#1263: WG New Spec: Verifiable Credential Barcodes v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1263) ([Github](https://github.com/w3ctag/design-reviews/issues/1263)) - @hadleybeeman, @toreini
### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow
### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk
### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola
### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh
### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini


## Atlantic Breakout (America / Europe) - [2026-10-23](https://www.timeanddate.com/worldclock/converter.html?iso=20261023T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: 
    
Scribe: 


<!-- Agenda+ -->

### [design-principles#628: Add the improve-existing principle](https://github.com/w3ctag/design-principles/pull/628) - @csarven, @jyasskin
### [design-reviews#1286: [wg/dp] Digital Policy Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1286) ([Github](https://github.com/w3ctag/design-reviews/issues/1286)) - @csarven
### [societal-impact-questionnaire#45: Publish this document as NOTE before TPAC 2026](https://github.com/w3ctag/societal-impact-questionnaire/issues/45) - @csarven, @lolaodelola
### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini
### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell
### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

<!-- PRs -->

### [user-agents#66: Add an EME example of making credible commitments.](https://github.com/w3ctag/user-agents/pull/66) - @jyasskin, @csarven
### [agentic-browsing-finding#2: Add section on the Lethal Trifecta](https://github.com/w3ctag/agentic-browsing-finding/pull/2) - @christianliebel, @jyasskin

<!-- Design Reviews -->

### [design-reviews#1254: Incubation: Cross-Origin Storage](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1254) ([Github](https://github.com/w3ctag/design-reviews/issues/1254)) - @ylafon, @bkardell, @dandclark
### [design-reviews#1291: Incubation: WebAuthn Conditional UI without Autofill](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1291) ([Github](https://github.com/w3ctag/design-reviews/issues/1291)) - @toreini, @hlflanagan
### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven, @ylafon
### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven
### [design-reviews#1253: Other Spec Review: CSS navigation-based styling](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1253) ([Github](https://github.com/w3ctag/design-reviews/issues/1253)) - @matatk, @dandclark, @lolaodelola
### [design-reviews#1285: Incubation: Declarative Performance Observer](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1285) ([Github](https://github.com/w3ctag/design-reviews/issues/1285)) - @bkardell, @hlflanagan
### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan
### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk
### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini
### [design-reviews#1249: WG New Spec: Recognized Entities v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1249) ([Github](https://github.com/w3ctag/design-reviews/issues/1249)) - @hadleybeeman, @hlflanagan
### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan
### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow
### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven
### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon, @hlflanagan



### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
