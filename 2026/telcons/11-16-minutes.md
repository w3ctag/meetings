# Call Agenda

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/11-16-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-11-16](https://www.timeanddate.com/worldclock/converter.html?iso=20261118T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Mike, Dan, Jeffrey

Regrets: Heather, Brian

Scribe: Jeffrey

Skipping around due to low attendance.

### [design-principles#619: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-principles/issues/619) - @marcoscaceres

### [agentic-browsing-finding#22: Proposed update to the identity delegation section](https://github.com/w3ctag/agentic-browsing-finding/pull/22) - @hlflanagan

### [design-reviews#1312: Rename "Other Spec Review" to "Browser Implementation Review"](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1312) ([Github](https://github.com/w3ctag/design-reviews/pull/1312)) - @jyasskin

Dan agrees with the direction, and suggests "Pre-Launch" review instead of "implementation". Jeffrey accepts suggestion.

### [tag.w3.org#107: Expect 8 hours per week instead of 1 business day.](https://github.com/w3ctag/tag.w3.org/pull/107) - @jyasskin, @hlflanagan

General agreement.

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

Jeffrey: Sent to changes in response to Brian's and dbaron's comments, and I think it's ready to merge after those. dbaron also suggested that we add examples, which is a good idea, but I'd like to merge without that. Will file a bug to add examples.

Dan: More examples would be good, but don't need to block.

Mike: Looks good.

### [design-reviews#1283: [wg/rml] RML Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1283) ([Github](https://github.com/w3ctag/design-reviews/issues/1283)) - @bkardell
### [design-reviews#1285: Incubation: Declarative Performance Observer](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1285) ([Github](https://github.com/w3ctag/design-reviews/issues/1285)) - @bkardell, @hlflanagan
### [design-reviews#1268: Other Spec Review: Registries developed by the Media WG](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1268) ([Github](https://github.com/w3ctag/design-reviews/issues/1268)) - @hlflanagan

### [design-reviews#1246: WG New Spec: Additional Windowing Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1246) ([Github](https://github.com/w3ctag/design-reviews/issues/1246)) - @jugglinmike, @bkardell

Jeffrey: I think this is ready to post. Mike, you can post with a preface something like: "we discussed this in a TAG breakout, with the following comment".

Dan: My comments don't change a lot in the proposed comment.

### [design-reviews#1251: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1251) ([Github](https://github.com/w3ctag/design-reviews/issues/1251)) - @jugglinmike, @marcoscaceres, @bkardell

Jeffrey: I'm cautious about endorsing Ryosuke's comments unless we've independently checked that we agree with them.

Mike: I'll double-check and then post.

Jeffrey: And the note about the marker being ambiguous is important for them to check.

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Jeffrey: I proposed a comment. Might or might not be closing; either unsatisfied or satisfied-with-concerns. Thoughts?

Dan: Most is reasonable and even actionable post-shipping.

Jeffrey: I'll give Marcos several days to comment, and then post.

### [design-principles#621: Add new fragment directive guidance](https://github.com/w3ctag/design-principles/pull/621) - @tabatkins

Jeffrey: I left several suggestions. We can merge those if y'all think they're right. There's still an outstanding comment even after my suggestions, and we can have the rest of the TAG take a look.

Dan: What's up with "for specific MIME types"?

Jeffrey: Fragment syntax itself is defined by each MIME type, so we can't define anything there for all MIME types.

Dan merges Jeffrey's suggested changes.

Jeffrey: I'll go through Marcos' comments and answer each one, and file a bug to ensure that SVG changes. I'll ensure Tab and other TAG members are happy before actually merging.

### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan, @jyasskin

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

## Eurasia Breakout (Europe / Asia / Australia) - [2026-11-18](https://www.timeanddate.com/worldclock/converter.html?iso=20261119T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Matthew, Christian, Lola, Marcos, Ehsan, Yves

Scribe: Matthew

Chair: Christian

### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan, @jyasskin

Christian: This is a simple PR; think I've closed all the review comments; just need a resolution. I think it's fine as it is, but need approval.

Marcos: Will read.

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

Christian: We have a draft skill, which we could publish. It works, though there are review comments remaining.

Marcos: We should put it into effect; it will provide good feedback.

Christian: Agree

Lola: We'll need buy in for people to use it; we should identify who's going to use it, and for how long, so we can track how it's performing.

Ehsan: I'm still trying to understand the purpose of this. There are many review requests that don't have explainers in the first place. We should have something to encourage people to contribute explainers.

Marcos: It could be adaptable to grabbing things from specs. I put in the Web Manifest spec today, which doesn't have an explainer, as we feel the examples section in the intro serves as an explainer.

Marcos: It's not meant for TAG members so much as for external people filing reviews. The question may be if TAG members find it valuable. It's intended to help proponents uncover the gaps they have in their proposals.

Christian: We'll talk about this in the plenary. Propose we can evaluate its use for a certain time and then decide what to do.

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: The proponents got back to me. They modified the spec. I asked for clarity on how pooling should work in terms of fetch - it's been resolved there, but was not reflected in this spec. They did this. I will check one more time that my other concerns were addressed. Looks good so far. Will update the group later on a resolution.

Yves: Discussion at TPAC; seems on track. Our feedback has been accepted so far.

Ehsan: Agree we could close it. *Ehsan to close*

### [design-reviews#1286: [wg/dp] Digital Policy Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1286) ([Github](https://github.com/w3ctag/design-reviews/issues/1286)) - @csarven

(Skipped.)

### [design-reviews#1256: [wg/immersive-web] Immersive Web WG 2026 Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1256) ([Github](https://github.com/w3ctag/design-reviews/issues/1256)) - @marcoscaceres, @matatk

Matthew: Marcos and I had a bunch of feedback, we are mostly happy, except for PCM haptics. Did you talk with them at TPAC, Marcos?

Marcos: Yes, I did. LGTM now. PCM will be dropped, and we are looking for a more general mechanism. Think we should give them a thumbs-up.

Matthew: There was also feedback from APA and me personally, so I’m happy with it and will close as satisfied.

### [agentic-browsing-finding#17: Remove sections which duplicate Lethal Trifecta](https://github.com/w3ctag/agentic-browsing-finding/pull/17) - @christianliebel, @toreini

Christian: PR from me, but we agreed to wait on other pending changes.

Ehsan: I think this links well with identity and delegation. I made some edits; need to check with Heather. Am working on that.

### [societal-impact-questionnaire#59: Add nonhuman animals to the natural environment question](https://github.com/w3ctag/societal-impact-questionnaire/pull/59) - @csarven, @lolaodelola

Lola: I need to review

### [privacy-principles#469: Suggested new sub-section to 1.2 (Vulnerability), titled "1.2.2 Vulnerability Impact"](https://github.com/w3ctag/privacy-principles/pull/469) - @toreini, @hadleybeeman

Ehsan: Discussed with Jeffrey during TPAC; Hadley volunteered; we will update accordingly.

### [societal-impact-questionnaire#50: Add example-attestation](https://github.com/w3ctag/societal-impact-questionnaire/pull/50) - @csarven, @lolaodelola

Lola: I will review.

### [meetings#64: Add finding publication to the agenda](https://github.com/w3ctag/meetings/pull/64) - @christianliebel, @hadleybeeman

Christian: We didn’t merge this, but discussed it, so will merge the agenda change retroactively.

### [design-reviews#1304: Incubation: Custom Highlight API Extensions](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1304) ([Github](https://github.com/w3ctag/design-reviews/issues/1304)) - @toreini

Ehsan: pending review

### [design-reviews#1296: Incubation: The `<agecheck>` element](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1296) ([Github](https://github.com/w3ctag/design-reviews/issues/1296)) - @toreini, @christianliebel

Ehsan: I have a couple of questions for Marcos (think they can be done async). I like the direction of it. Think it's necessary. I want to know the threat model better. Is there anything on that? E.g. who is the adversary, from the spec's perspective, and what are their capabilities?

Marcos: A determined teenager.

Ehsan: That's what I thought. Is it possible to have a web extension that removes all of the `<agecheck>` elements automatically?

Marcos: We have considered the threat model and build around it... but we should document it.

### [design-reviews#1300: [wg/agenticweb] Agentic Web Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1300) ([Github](https://github.com/w3ctag/design-reviews/issues/1300)) - @marcoscaceres, @toreini

Ehsan: Haven't finished the review yet; aiming to this week.

Marcos: Also working on it this week.

Yves: AC will look at the charter too.

### [design-reviews#1305: WG New Spec: SHACL 1.2 Profiling](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1305) ([Github](https://github.com/w3ctag/design-reviews/issues/1305)) - @csarven

*skip*

### [design-reviews#1306: WG New Spec: SPARQL RL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1306) ([Github](https://github.com/w3ctag/design-reviews/issues/1306)) - @csarven

*skip*

### [design-reviews#1307: WG New Spec: SHACL 1.2 User Interfaces](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1307) ([Github](https://github.com/w3ctag/design-reviews/issues/1307)) - @csarven

*skip*

### [design-reviews#1294: WG New Spec: SHACL 1.2 Inference Rules](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1294) ([Github](https://github.com/w3ctag/design-reviews/issues/1294)) - @csarven

*skip*

### [design-reviews#1301: Incubation: Responsive Image Fine-Tuning Knobs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1301) ([Github](https://github.com/w3ctag/design-reviews/issues/1301)) - @marcoscaceres

Marcos: Yet to review

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

Matthew: I think we can close it.

(Matthew to close.)

### [design-reviews#1263: WG New Spec: Verifiable Credential Barcodes v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1263) ([Github](https://github.com/w3ctag/design-reviews/issues/1263)) - @hadleybeeman, @toreini

Ehsan: Hadley provided input; I'm now drafting the closing comment. Will post and ping Hadley soon.

### [design-reviews#1284: Incubation: Web Haptics API](https:/tag-github-bot.w3.org/gh/w3ctag/design-reviews/1284) ([Github](https://github.com/w3ctag/design-reviews/issues/1284)) - @marcoscaceres, @toreini, @christianliebel

Ehsan: Proponents explained it can't be used as a fingerprinting array, but I'm concerned it can be used as a buffer with another API. This is a concern; they need to have some sort of direction for protections against that. E.g. coupled with acceleraometer.

Marcos: Agree with these concerns. If you can sense it's shaking enough, you can determine how it's being held, and that's fingerprintable.

Ehsan: It can be determined if you're running, walking, ... when you combine haptics and accelerometer.

Marcos: Gyroscope needs permission. Definitely stuff to dig into here.

Christian: I think the use case is fine. Undersand the concerns, which need discussion. The proposal seems to have stabilised following TPAC discussions with CSS. Should be good to review now. The obvious concern is user annoyance, too. This is also a feature that I personally have wished for. It's a cool addition for web apps.

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Christian: We published the interim comment before TPAC. We haven't recieved a response yet. They asked us to hold off from reviewing until they'd discussed it with other vendors during TPAC. There was agreement that this should be reframed as “WebRPC“ and the MCP part is placed on top of this. Question is: should we do the review?

Yves: We have a resolution of 'too early' that we could use.

Christian: We could talk about that tomorrow.

Ehsan: Agree with Yves. We are waiting for them to provide information that will change the core principles of the spec, so we should treat that as a new review.

Christian: I understand there may now be agreement between Chromium and Mozilla, but we need to see the details of that. *Adds to plenary agenda.*

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow

Matthew: I wrote a closing comment, think it needed a bit of work, if people could take a look?

(Matthew to post the closing comment.)

### [design-reviews#1266: Other Spec Review: Scroll snap for single-axis scroll container](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1266) ([Github](https://github.com/w3ctag/design-reviews/issues/1266)) - @lukewarlow

(Skipped.)

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Matthew: Consensus in TAG to close this. Discussed it with APA and some other groups. In one of those meetings, there were a number of issues raised related to accessibility that haven’t been resolved. Wanted to make sure nothing big remains. Need a little more time to review the minutes.

### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk

Matthew: Raised at the Vancouver F2F, since then, Heather wrote a best practices document which I need to review. Can do that soon.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Ehsan: Drafted a question for the proponents; waiting on review of the comment. Haven't heard anything from the proponents for some time, so not sure what its status is.

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @christianliebel, @xiaochengh, @lukewarlow

Christian: An extension to the performance timeline. There are 2 new measurement entries they want to add: interaction contentful paint; and soft navigation. They are useful for SPAs. Luke and I are reviewing. We're not performance experts, but it looks good to us; we suggest closing as satisfied, unless someone objects. *Will draft clsoing comment.*

## Atlantic Breakout (America / Europe) - [2026-11-17](https://www.timeanddate.com/worldclock/converter.html?iso=20261120T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Ehsan, Matthew, Lola, Jeffrey, Dan, Christian, Yves, Hadley, Sarven, Brian

Chair: Lola

Scribe: Christian

### [design-principles#628: Add the improve-existing principle](https://github.com/w3ctag/design-principles/pull/628) - @csarven, @jyasskin

Jeffrey: This needs some work. Sarven added a bunch of stuff, but hasn’t removed duplication with the other similar principles yet. Not sure if all of the text belongs here.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

Jeffrey: Believe it’s time to work on design reviews.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Jeffrey: Same here, believe it’s time to work on design reviews.

### [w3ctagbot#222: Organise Issues and PRs According to Meeting Labels](https://github.com/w3ctag/w3ctagbot/pull/222) - @lolaodelola, @jyasskin

Lola: This should go to the plenary.

### [tpac2026-meetings#50: Cancel in-progress jobs](https://github.com/w3ctag/tpac2026-meetings/pull/50) - @matatk, @jyasskin

Matthew: I think we discussed this? Can take this offline.

### [agentic-browsing-finding#18: Cite Identity Delegation](https://github.com/w3ctag/agentic-browsing-finding/pull/18) - @christianliebel, @hlflanagan

Christian: This is a one line change, adds a citation to one of Heather’s publications.

Jeffrey: There’s a larger rework happening (https://github.com/w3ctag/agentic-browsing-finding/pull/22), so I think we shouldn’t work on this right now.

Ehsan: Offer to work with Heather to merge the two documents on Agentic Web. What do you think?

Jeffrey: Haven’t read the big document yet, so I don’t have an opinion yet.

Christian: Did not read it either, but seems fine to merge?

Ehsan: Will discuss with Heather.

### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

Lola: Took myself off of this, as it’s too much for now. Jeffrey, you had a look at the first few paragraphs?

Jeffrey: Yes, but I would prefer having an additional person to take a look.

Sarven: I will have a look.

Lola: They want a realistic estimate when this design review can be completed.

Sarven: Think before the end of the month. Maybe I can do it section by section.

Jeffrey: I think I can get to it within the next couple of weeks.

Sarven: Are we past a deadline?

Lola: They have extended the charter to Apr 2027, but this is the main blocker for publishing. I guess they want to publish before Apr 2027. And they should have time for revisions etc.

… So will report that we do it by the end of November.

Jeffrey: Will reply that.

### [design-reviews#1249: WG New Spec: Recognized Entities v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1249) ([Github](https://github.com/w3ctag/design-reviews/issues/1249)) - @hadleybeeman, @hlflanagan

Hadley: Recognized Entities in the Verifiable Credentials area establishes a chain of trust, e.g. a university is actually allowed to give me a certificiation etc. Have been in touch with them during TPAC. They think there are some conflicts in our response. We need TAG consensus to post the comment, which hopefully sorts out the confusion.

(Consensus.)

Hadley: The resolution is “satisfied with concerns,” is that fine?

Lola: Main concern was JSONata and not Python or JS or something else. Reason was the implementers wanted to go with this, and parts have already been implemented.

### [design-reviews#1302: WG Revision: Creating Always-On-Top Windows (Window Management)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1302) ([Github](https://github.com/w3ctag/design-reviews/issues/1302)) - @christianliebel

Christian: Proposal to allow developers to make windows that are always on top. Scary at first, but gated behind a "manages screen setup" permission. Existing work that allows opening a window on a specific screen. Second Screen WG. This is a property in window.open() behind that permission. Seems fine because of that bar. Question of how to interface that with HTML, without window.open(). I'll work on that, but the basic idea sounds fine.

Yves: What about 2 "on top" windows? z-index?

Christian: Up to the OS. Probably the last-clicked wins.

Dan: Just on top of other browser windows? Or OS-level, which might behave differently across OSes?

Christian: Can ask that in the feedback. We also already have this primitive with picture-in-picture, which is this kind of window.

Lola: One of the alternatives is to document picture-in-picture, and they say that doesn't work. Struggling to understand: a use case is meeting notes. Tool isn't integrated into Meet (the videoconference tool). Are you giving permission for that window to know about other windows? Or just to know about another specific window? 

Christian: This is a "manage windows" permission. Number of screens, and place windows specifically at certain positions.

Lola: Isn't so much about knowing about another window, just positioning.

Christian: There's a potential alternative, to add this to the browser chrome. e.g. "pin tab" which lets the user decide. Which wouldn't need the permission.

Lola: I'm looking at you in Picture-in-Picture, and I can control that.

Jeffrey: I would add that there should be a smaller permission that allows this. Opting into sharing all screen information seems very big compared to making a window float, so they might want to introduce a "smaller" permission.

Lola: Draft a comment.

Christian: Maybe also not a closing comment. Can discuss with them. Would be cool if the bar was lower. It's fine to have the high bar, but maybe the use case deserves an easier way.

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

Matthew: We’ve got some answers. Haven’t checked them in detail, but talked to the proponents at TPAC.

… We had concerns around fingerprinting and what WCAG is specifying now and what it might do in the future. Users might zoom in and might use a screen magnifier. If this produces a nondeterministic outcome, this could pose challenges for those users, and for testing.

… They have addressed the things we asked for. It seems promising, but I need more time to think about it.

Lola: There is more context around this in https://github.com/w3c/csswg-drafts/issues/12886. There are WCAG things around spacing in general. It would be good to know if they’ve considered that as part of their design as well. E.g., I don’t know if text-fit addresses the height in any way. There are also things that are not in WCAG but might be relevant in other regions, e.g. South Korea or places which use other character systems.

Matthew: Might be more i18n warehouse, but presumably what they describe seems to be a logical property rather than a @@@ one.

### [design-reviews#1273: WG New Spec: VCALM v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1273) ([Github](https://github.com/w3ctag/design-reviews/issues/1273)) - @jyasskin, @hadleybeeman, @hlflanagan

Hadley: I remember that they have another normative reference to JSONata.

(Bumped.)

### [design-reviews#1291: Incubation: WebAuthn Conditional UI without Autofill](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1291) ([Github](https://github.com/w3ctag/design-reviews/issues/1291)) - @toreini, @hlflanagan

(Bumped.)

### [design-reviews#1264: Incubation: Filterable select](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1264) ([Github](https://github.com/w3ctag/design-reviews/issues/1264)) - @matatk, @dandclark

Dan: Expanded on this in Oct. It was discussed in length at TPAC. Joey’s response might no longer be up-to-date. Latest idea is to put an attribute or another element under select which would allow an input element to appear there. This was debated because of parser concerns, but I don’t share the scepticism. Might reach out to Joey and get his feeling how feasible it is to propose the breaking change. Would be nice if it could be done.

Lola: Why not the nested route?

Dan: MXSS issues, sanitizers, another way to branch the HTML parser…

(Dan to check back with Joey.)

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github]
(https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven, @ylafon

Sarven: We asked a question, and there’s no update yet.

Lola: This has been open for a year, I propose closing it.

Yves: Agree. Not great, but not much we can do.

Jeffrey: Think marking it as "unsatisfied."

Hadley: I would support that.

Sarven: Don’t think it’s particularly accurate. It’s a design question. If this group feels the ecosystem is well functioning without signaling versions, or error handling, that might be acceptable. There’s enough evidence that the ecosystem is working with or without that. On a theoretical level, I believe the TAG is correct what it’s suggesting. On a practical level, I’m not sure if "unsatisfied" is accurate. Don’t know whether our review should take that practical part into account.

Yves: It might be right in the current ecosystems, but future libraries might be automatically generated. What will happen? This can lead into interop issues.

Brian (chat): Which might suggest "satisfied with concerns" (despite the confusing name).

Sarven: It has worked from 1.0 to 1.1. Altough the questions is if it will remain that smooth towards 1.x.

Lola: Does "satisfied with concerns" feel more appropriate?

Sarven: Yes, and leave it at the discretion of the group.

Jeffrey: I'm uncomfortable with their approach to error handling, the notion of "we don’t care" doesn’t seem right. But would not block "satisfied with concerns" if the group decides.

Lola: What is their approach to error handling?

Jeffrey: They claim a different layer should take care of it.

Sarven: It’s used in different environments, e.g. in and outside of browsers.

Lola: Seems like WebRTC, which also isn’t a browser thing, but the things that interact with the browser are covered.

Yves: The fact if it’s a browser thing or not is irrelevant here, as we are talking about media types.

… More about, if you’re creating a software stack that is using it, something that looks like it expects @@@ but it doesn’t, it’s problematic, so leaning towards "unsatisfied".

Matthew (chat): The unspecified bits are very concerning too.

Lola: Support "unsatisfied." Anyone stronly opposing?

(Nobody opposes.)

Sarven: if and only if it is clear that the "unsatisfied" refers to the specific concern and not representative of the whole spec.

Yves: Unsatisfied, but not blocking.

(Jeffrey to draft the response. Yves and Sarven to review.)

### [design-reviews#1254: Incubation: Cross-Origin Storage](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1254) ([Github](https://github.com/w3ctag/design-reviews/issues/1254)) - @ylafon, @bkardell, @dandclark

Yves: Looked a bit at it, and the concern is now in another document, security and privacy issues. At least they are aware of the attack that I was fearing.

Brian: It’s been a minute since I looked at this. The whole thing keys on a couple of things that I’m not sure if they can hold up. Having gone to TPAC and having talked to vendors, I’m not sure if other vendors can be convinced.

… It’s treating some very problems (e.g., sharing a version with jQuery) with the same mechanism as huge AI models.

Dan: Privacy implications of sharing a game engine and an AI model seems to be different to a library. Not sure if it’s feasible to put them together under the same feature. What should the norms be around declaring "*" as the origin for resources. Not sure if it can be matched together.

Brian: But even here, it relies on the PHL. The question how big that list is, is debated. Other vendors mentioned there is potential for such a feature, but not at the scale. Think it’s a neat idea, and solves a real problem, but implausible at its current state.

Lola: Mozilla says we agree on the problem, but we’re not happy with the current solution. Sounds like they don’t have buy-in. So close it as that? Isn’t there a "lack of multi-stakeholder feedback" label somewhere?

Hadley: So more architectural than procedural?

Lola: I think it mixes both. Problem is valid, solution is problematic. The other browsers feel similarly, and that’s why there’s no multi-stakeholder buy-in.

Hadley: That makes sense. I just want to make sure we’re not policing the process, since that's not our job. We're seeing lack of multistakeholder support BECAUSE there is an architectural problem. 

Lola: This just sounds like unsatisfied, but acknowledging the problem.

Brian: "The problem" is maybe a bit vague, as it talks about a single problem. Concerns are potentially very different.

(Dan to draft the comment.)

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @christianliebel, @xiaochengh, @lukewarlow

(Skipped.)

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh

Lola: We need to close this, it’s been too long, we’re unsatisfied. Ok, Matthew?

Matthew: Think I proposed a comment for this.

Lola: Draft comment seems good, will give it a read. And then leave it up to the community to follow up.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

(Skipped.)

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman



### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk



### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini



### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan



### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow



### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon



### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh



### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan, @jyasskin



### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel



## Plenary

Present: Brian, Matthew, Lola, Ehsan, Yves, Dan, Marcos, Jeffrey, Sarvenx

Regrets: Heather, Hadley, Christian
    
Scribe: Marcos, Dan

### Associates & inviting nominees

Lola: first item is talking about nominees
    
Jeffrey: we can appoint folks after current people on the TAG ends. We can also see how folks in the community to see how they respond to reviews. It could help to see how they respond to review feedback. There's a worry that appointing people as associates is a way of getting around the election process. 

Lola: any comments or concern?

Marcos: Are there any concerns about potential candidates and associates joining for a time? 

Brian: it might be unfair for people who didn't know this needed to be a thing. As it takes a lot of resources. 

Yves: if we know that someone could be problematic, it could cause further issues. 

Jeffrey: We could allow the TAG to evaulate if a person would be someone we want to work with. 

Lola: I agree in the case where someone could be highly disruptive and known to be disruptive. 

Marcos: echoing what Brian said, basically.

Brian: it's a US holiday... then xmas... so time is very short. Even if they join for a few sessions, I don't know how much that's going to feed back to the AC. I also don't want us to be put a positon where we give a report card. 

Jeffrey: if someone doesn't have time, that's fair and something to feed back into the AC. What we could do is allow them to do a review in public that the AC can judge on.

Lola: I think it is important to feedback into the AC. During the time I've been on the TAG, I've seen people get elected and then not participate. I think it's quite a high bar... a lot of people need to get experience and will need hand-holding. We also need people who can contribute to findings, and contribute in other ways. It would be good to have nomenees.  

Marcos: That's something really important. Could be for next election: "choose your poison: contribute to findings or design review; something that'll only take a couple hours." Dumping a design review on someone, can take weeks or months. On the other hand, being on the TAG is a high bar.

Lola: I'm not hearing consensus. Should we pick this up in with the new TAG? Jeffrey can you own it? 

Matthew: +1. 
 

### [w3ctagbot#222: Organise Issues and PRs According to Meeting Labels](https://github.com/w3ctag/w3ctagbot/pull/222) - @lolaodelola, @jyasskin

Lola: most people might have not interacted with this bot. This tool is used by chairs to put together the agenda for our meetings. Labelling/scheduling things is time consuming, so this helps cut down time a bit. It makes the chairing job much easier. 

Jeffrey: is anyone worried about the extra labels and having a more stable meeting agenda. 

Yves: Does the label automatically disapear after each meeting. 

Lola: it works as it works now, but it helps with reoganizing... we need to check how it works and then adapt. There seems to be consensus, feel free to merge once you are happy and gotten everything you need. 

### [Re-wording TAG review outcomes](https://github.com/w3ctag/process/issues/50)

Lola: I see Brian has left a comment. Brian said we should use Heathers two labels: "proceed with caution" and "reconsider". 

* Proceed with caution: The TAG has substantive concerns and recommends addressing them, but does not think the work should stop.

* Reconsider: The TAG has serious concerns and recommends that the work not proceed in its current form.

Brian: I don't love Reconsider. Opposed might be better as we can't "object". 

Sarven: it reminds me of AC review, where AC members can say that they have concerns but can live with the changes not going in. I don't to bikeshed, so can live with the current ones. 

Marcos: I'd be more in favor of opposed

TAG temprature check leans towards "opposed" 

Matthew: I worry about "proceed with caution" might not be strong with caution. If the first word is proceed, it's doing most of the work. 

Yves: We have a label for object. 

Lola: I don't think we've ever used object. 

Jeffrey: only once... I don't love any of the current ones. 

Lola: proceed with caution, address concerns before proceeding,  "concerns, non blocking"

Yves: The teams considers if the TAG is unsatified, then the Team considers it blocking. 

Lola: Brian, does Yves explanation address your comment. 

Brian: it feels like we should use blocking or "opposed"... worried that people might misunderstand the process. 

Sarven: when folks come to us, what are they asking us? Are they just asking us for advice? Are we providing feedback for the AC? Where and what the feedback goes is important and could be interpreted in different ways with different weight. We are not able to "block" things, but it can have a knockone effect... we are missing some pieces of information. 

Brian: if the above is the case, the we should just be "opposed". 

Lola: but that is correct in as far as "proceed with caution" ... we are not "opposed", we are not saying the work should be stop... "concerns raised" could work potentially beucase it could signify that things are on the right and wrong track. As Yves mentions, the team and other folks look to these labels and can signal different things. Then the team or others can look up why the position was reached. 

Sarven: I find proceed with caution to fall under the same category... that things should be re-evaluated. Where opposed is more clear. 

Lola: we have consensus:
    * concerns: proceed with caution 
    * Opposed
    
Jeffrey has made the changes. We have new labels.  

### [design-principles#621: Add new fragment directive guidance](https://github.com/w3ctag/design-principles/pull/621) - @tabatkins

Jeffrey: I think it's ready to merge. Wanted to check if there's consensus to merge. 

... Jeffrey gives an overview of issue.... someone suggested xpointer... there was fragment directive and Tab was unaware... so Tab thought we should add this to the design docs so people know in the future. 

Yves: there are two types of fragments that can be defined... SVG ones and ones from browser behavior... <technical details>... 

Jeffrey: fragments are defined by their media types. It could be, for example, for CSS to say "here's how the fragment works for SVG" ... that needs to be done by SVG instead. We could question who owns the behavior of the fragment, but in the future. 

### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan, @jyasskin

Marcos: The issue is it's backwards about how it works. Having just done with with digital credentials...an example someone gave is that certain users think if you go to private browsing and log into a site, the user thinks the site doesn't know you logged in. With digital credentials, if I share a credential, they think the site doesn't know it got the license. The interesting part is when you share in private browsing e.g. drivers license as a credential and it has the licence #, it's linked with sharing in regular browsing. guidance becomes APIs should never assume they're in a mode, so they should assume they're in private browsing mode. I think that's the better guidance.

Jeffrey: Google had to change the wording of their inPrivate mode user-facing text after a lawsuit. I don't think all APIs should be designed as if in private mode. That would mean cookies would have to be designed as always ephemeral. Need somehting more; what's in the PR is not totally right.
For Marcos' case, maybe should tell the underlying system it's in private mode.

Marcos: Spec says very clearly rotate your credentials, mint a new one when asked.

Jeffrey: But if wallet is remembering you've used this cred at these times and you go into private mode, should tell the wallet not to remember

Marcos: But there's no proviision. You don't want if you went to some kinds of sites, don't want the wallet or site to know. Wallet is also adversary in some situations. No one should know user is in private mode, that's the gudance we're giving, I put a PR up in dig credentials.

Jeffrey: not sure wallet should always be adversary. But If you can christian come to a conclusion I won't second-guess.

Marcos: There's active discussion in dig credentials, we'll see how that plays out, should feed into this.

Brian: Wallet idea, can wind up with lots of things that are as-a-service. WEeb speech, chrome when you're traveling sends info to speech subsystem that's historically in the cloud. When acting as part of OS, you wouldn't want to communicate it was intented to be private. Or when acting as part of the browser itself.

Marcos: Don't think you ever want it to know.

Lola: Sounds like Marcos you will propose change to Christian's PR. Jeffrey may also want to review.

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Marcos: I think we need to get this out. I'm not prepared to re-review until they put together new proposal. If they'll rework based on mozilla's feedback, great, but current feedback stands. I think it's ready to go.

Matthew: yes. I agree. I saw good progress at TPAC. Folks working on it are up for working with APA, and listeened to the other concerns you mentioned. But we did the review, only thing I'd clarify is we'd probably publish almost the comment we proposed to publish, but should put at the top that we understand significant changes are in play, this is our feedback from before TPAC.

Lola: Marcos will post it.

Jeffrey: I haven't gotten to look at the current contents of the google doc. I worry it doesn't incoporate answers to why not only declarative. Ehsan, put the draft comment into private brainstorming thread so we know exactly what's proposed.

Ehsan: I'll do that.

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

Lola: This is the last PR to merge before we can deploy this? Jeffrey had made some comments.
Consensus?

Jeffrey: I'm still worried about it. We don't have a system for testing changes. 

Lola: what I suggested previously is to run an experiment. And we can see what is being generated and what things it does well... that could be a way to check what it does well. 

Jeffrey: it might be the best we can do given no one is testing AI stuff. 

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

