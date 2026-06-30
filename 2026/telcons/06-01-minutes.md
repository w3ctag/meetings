# TAG minutes, week of 1 June 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/06-01-agenda.md).

## Plenary Session - [2026-06-02](https://www.timeanddate.com/worldclock/converter.html?iso=20260602T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Lola, Jeffrey, Brian, Heather, Xiaocheng, Christian, Ehsan, Matthew, Hadley, Yves

Scribe: Heather

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Lola: There has been a lot of back-and-forth. The group reached consensus for "satisfied with concerns". Does that change the draft comment? The main concerns were the issue with keyboard and touchscreen stuff.

Matthew: Well done, everyone! The two tweaks I suggest I think we can deal with on this call. Not entirely comfortable saying "one member of the TAG did not agree". Seems like exposing more information than necessary. 

Lola: We do have consensus, but we do not have unanimity. We don't all agree but we can all live with the outcome. Since we have consensus as the W3C defines it, we don't need to pick that apart. So, agree, we can take out "one person doesn't agree."

Matthew: The other edits I suggested were fairly minor, breaking up a paragraph and bolding an item particularly important to me. 

Jeffrey: I have added your changes.

Heather: I don't like including the mention of one person disagreeing; it opens us up to nitpicking later.
    
Jeffrey: I do want to mention the opinion and indicate it was the minority, but we don't have to say it's just "one".

Lola: I think Apple's standard position should reflect the minority opinion, since that's more what Marcos' opinions were about. They can also go into a lot more detail and nuanced back and forth. 

Matthew: Effectively I'm looking at text we agreed to and want to be extremely conservative in changing it. I think we need to reflect there is a minority but significant concern (that's already in the text). I just don't like to use "one member of the TAG". If we take out the whole thing, we significantly change the meaning of the text we agree to.

Lola: Jeffrey's comment probably covers that concern; it holds the minority opinion without saying "one member of the TAG".

Matthew: The PR removes the "one member of the TAG" but you also removed more that I think is important to keep. Maybe go with what Brian suggested and say "a minority" and keep the rest of the concern?

Jeffrey: OK

Xiaocheng: Also do not want the words "one member". Instead, say "significant concerns have been raised, without TAG consensus, that..."

Lola: It sounds like we're happy with the change. Let's post that. 

### Interim Chair(s)
Lola: Two of the chairs are going to be offline for the same time in June, and the third chair will be offline the first week of July. Responsibilities include: building the agenda (Jeffrey has a tool to help) and chairing the plenary, admin-related things like liaising with other groups (e.g., the AB).

Hadley: Also on the list of responsibilities: a chair meeting alternating weeks to the plenary. For process reasons, we do need to vote, and we shouldn't do it today as everyone should be on the call.

Lola: Already, three people on this call wouldn't be able to do all of it. We should continue to discuss options for that period of time. Maybe focus on design reviews? Jeffrey will start his leave next week.

Jeffrey: For the process, replace me as chair and can choose to replace me back later.

Hadley: I think that sets the wrong expectation.

Brian: So many people aren't going to be available the week of the 15th, we should cancel.

Hadley: Any objections? <no> 

Lola: I'll cancel them in the calendar. We'll come back and discuss. Heather and Christian are happy to step up, but we'll see if anyone else wants this.

Hadley: We'll give people until Friday to give +/- to Yves in Slack.

### [AI in design review process](https://github.com/w3ctag/explainer-explainer/pull/39)

Lola: We started talking about this in the last plenary. 

Jeffrey: There is a PR for a skill to help LLMs review explainers. I was working on evaluation for that skills so that if someone changes the skills, we can see how it effects the review. Microsoft has a tool to help evaluate the change, but it assumes that an AI would do the review and we want a human. The progress I've made so far is in the PR, but it isn't done.

Lola: Since this is using Copilot, note that Microsoft has made changes to their pricing model. Not sure how that impacts what we're doing. 

Jeffrey: It will stop running when I run out of free credits. The skill itself has a chunk at the end about how to edit it; that should probably be deleted. 

Lola: Matthew will publish this since he's handling the Explainer Explainer.

Jeffrey: Heather should also review since she's the other person that uses LLMs. Christian will also review. 

<!-- Reviews that have been pending external action for at least 6 months -->

### [design-reviews#1041: Signature-Based Integrity.](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1041) ([Github](https://github.com/w3ctag/design-reviews/issues/1041)) - @martinthomson, @csarven

Lola: This is pending external feedback but has been waiting since 2025. 

Jeffrey: Why did we make this pending external feedback? We should review <https://github.com/w3c/webappsec/blob/main/meetings/2025/2025-11-TPAC-minutes.md#integrity-signature-based-checks-for-subresources-and-inline-content>

Lola: Looks like they were still looking at what needed to be solved. Any objection to closing this? No.


### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @lolaodelola

Lola: They wanted to discuss our comments in a WG meeting. Should we still leave this open?

Heather: Should we at least give them a nudge to see how it's going?

Lola: It is a big piece of work and we want to avoid too-early reviews, but we can ask.

Jeffrey: Looking at the PRs and Issues, it looks like most of the work is done. So a ping is probably worthwhile. The biggest question was whether "resolution" was the right word at all. I think they found a way to explain that, and if so, it will be time for review.

Heather: I will be happy to take that review when it comes in.

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1128) ([Github](https://github.com/w3ctag/design-reviews/issues/1128)) - @toreini

Lola: They have not responded since October. Should we close this?

Ehsan: Looks like they haven't been updating their explainer in the last six months. 

Lola: Closing.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

- https://github.com/w3ctag/design-reviews/issues/1233 (CSSPseudoElement) - will assign to Brian and Xiaocheng

- https://github.com/w3ctag/design-reviews/issues/1224 (Lightweight and Conditional Tracing for long animation frame timing) - want to assign a second to work with Xiaocheng. Will assign to Heather.


## Pacific Breakout (Asia / Australia / West America) - [2026-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20260603T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Jeffrey, Christian, Heather, Brian, Dan

Regrets: Marcos

Scribe: Brian

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu

Jeffrey: I haven't looked at this since last week - heather replied and a bunch of us agreed, but we don't have a PR. Let's skip this one today. The attached PRs are plausible, let's consider the ones there over the next weeks.

### [design-principles#592: Event names should use the present tense](https://github.com/w3ctag/design-principles/pull/592) - @xiaochengh

Jeffrey: The PR was merged because several of us approved it.  Nothing left to do, it was on here because the agenda already existed.

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan

Jeffrey: I updated this with Marcos' latest draft. I started writing an evaluator, and I put a copilot account there - it didnt' get very far.  I found a possible tool to do the evaluation (https://github.com/microsoft/waza) it's not a perfect match, but anyone who picks this up could try to use that. It appears to want an AI to evaluate the skill output and I thiink we just want it to print and be evalutated by a human, but it might be a good place to start.

### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu

skip

### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu

skip

### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu

skip

### [design-reviews#1230: [wg/browser-tools-testing] Browser Testing and Tools Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1230) ([Github](https://github.com/w3ctag/design-reviews/issues/1230)) - @marcoscaceres

Jeffrey: Marcos left a comment that we should just say satisfied unless someone objects. He said he reviewed it.  https://github.com/w3ctag/design-reviews-private-brainstorming/issues/285#issuecomment-4507014307

Heather: You had a comment there...

Jeffrey: I was repeating a concern of Marcos' - I think my comment doesn't matter.  

(we reach concensus that marcos should post it)

### [design-reviews#1224: Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1224) ([Github](https://github.com/w3ctag/design-reviews/issues/1224)) - @xiaochengh

Jeffrey: Xiaocheng drafted a response https://github.com/w3ctag/design-reviews-private-brainstorming/issues/279#issuecomment-4542454000

Heather: I have no problem with the draft response. We are just making comments, not asking questions - would we close it or leave it open for them to respond.

Jeffrey: I think this is a good question for Xiaocheng because they didn't suggest whether it is "satisfied with concerns" or wanted to ask questions

Heather: Could we leave it open for a set period of time

Jeffrey: Or we could ask a question.. I see that Matthew had been involved in the previous approach - I would like to ask Matthew what he thinks - and otherwise say this breakout is happy with the reply.

Brian: That sounds reasonable.

Jeffrey: I have replied to the brainstorming issue - once they are happy they can just post.

### [design-reviews#1220: [wg/wasm] WebAssembly WG rechartering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1220) ([Github](https://github.com/w3ctag/design-reviews/issues/1220)) - @bkardell

Brian: Looked at this and talked to ms2ger and Andy. Looks pretty good. Don't see a reason for us to have concerns. Inclined to say "TAG approves this message".

(ap for brian)

Approved

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @dandclark, @xiaochengh

Dan: I had drafted a comment, I was hoping that Xiaocheng would review it - it probably should be "satisfied with concerns" rather than just "satisfied" - I would really like them to approve it.

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

Heather: We are waiting on Marcos to develop more of an opinion

Jeffrey: He had asked about standards positions and I looked and neither WebKit nor Mozilla had replied.

### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Jeffrey has finally drafted a comment: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/250#issuecomment-4607924888

Brian: Yes, that looks good!

Heather: Ship it.

### [design-reviews#1214: [wg/math] Math Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1214) ([Github](https://github.com/w3ctag/design-reviews/issues/1214)) - @christianliebel

Christian: Basically, I had a look at this, it seems fine.  I think we talked about it a bit recently - the only concern I had architecturally was that in the charter they added that they wanted to make it more searchable, however, I am not sure what other changes in the charter support that.  They dropped some things about hyperlinks and line wrapping.  

Jeffrey: No concerns from other reviews that affect the charter.  it is probably most effective to post questions to the strategy review rather than the design review.

### [design-reviews#1221: WG Revision: Selectors 4](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1221) ([Github](https://github.com/w3ctag/design-reviews/issues/1221)) - @bkardell, @lukewarlow

Brian: Propose that we're satisfied. Jeffrey agreed.

Christian: Happy to support that.

Brian to post.


### Rewording TAG review outcomes - @bkardell

Brian: Commented that we have "validated" that's about early reviews. But doesn't apply to others. We could have "completely/mostly/partly" satisfied. Call them "early satisfied" vs "satisfied".

Heather: I have an action item to create an issue so we can hash this out coherently.

Brian: We've been iterating in a doc.

Jeffrey: "validated" is kinda "we agree that the use cases are good".

Brian: We could have that opinion in a late review.

Jeffrey: Might be good to have a label focused on our evaluation of the use cases.

### [design-reviews#1205: WG Revision: MathML 4](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1205) ([Github](https://github.com/w3ctag/design-reviews/issues/1205)) - @jyasskin, @matatk

Draft comment at https://github.com/w3ctag/design-reviews-private-brainstorming/issues/260#issuecomment-4493218520

Approved to post.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-06-04](https://www.timeanddate.com/worldclock/converter.html?iso=20260604T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Lola, Luke, Yves, Ehsan

Scribe:  Ehsan

Regrets: Christian, Matthew

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Lola: Matthew has not filled the draft comment, I will have a look and draft a comment.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: I have drafted a comment.

Lola: If you want Jeffrey's comment, do it today as he will be off from Friday.

Ehsan: what do you think about it Ives?

Ives: I will look and let you know soon.

Ives: I had a look, it looks fine. My comment was less general but this 

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

Lola: Luke?

Luke: I have not had a chance yet.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Luke: I have made a small draft comment. Matthew mentioned there is accessibilty draft going and wanted to check with him on that ifwe can refrence a conversation and include them. I will ping Matthew on it.

Lola: you can just let them know we are still reviewing and we can give a proper review when we knw more about accessibility conversations.

Luke: I am drafting a comment in line with that.

### [design-reviews#1228: Other Spec Review: overscroll-behavior: chain](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1228) ([Github](https://github.com/w3ctag/design-reviews/issues/1228)) - @lolaodelola, @lukewarlow

Lola: I left draft comment. It seems fine and they have not given us much to work it. I don't see any critical accessibility issues. Some parts of it is good for cognitive accessibilities.

Luke: is there a chance to ask them on S&P section?

Lola: there is not much from them, but they included S&P section in the spec itself. It fullfils those requirements; however, I don't see accessibility consideration. Maybe worth asking them as it has positive impact on it.

Luke: I think this aspect is fine, the reason why they are doing that is more important.

Lola: do you want to review it Luke?

Luke: I don't have any concrete feedback. I think it is fine for you to draft a comment.

Lola: ok.

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

Ives: I have not got a chance to review it propoerly. will do that soon.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow

Luke: I left a comment this morning, stating we are waiting for official position from webkit.

Lola: is this pending Marcos?

Luke: yes, it is pending the final position from webkit. This feature makes sense to wait for this as webkit approach is different and it is important to have their take.

Lola: ok

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Lola: skip

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: I had drafted my comment, if there is any objections.

Yves: It looks similiar to the previous one we discussed, except for minor changes.

Ehsan: yes.

Lola: do we need a response from the propoentns or is it closing comment?

Ehsan: it needs reponse from them, so better wiat to see how they respond.


### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

Lola: skip

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow

Lola: luke do you have anything to add?

Luke: I am writing draft comment now regarding position-visiility which I think doesn't necessarily meet the requirement. I might write a comment to mention the comments and then check with them how it works before shipping it.

Lola: this pattern is happening more often recently. This maybe because we have a long backlog. 

Luke: yes, this is from Dec 2025, but this is not massive long wait to justify the shipping in the browser.

Lola: we can have a look in the closing comment as I can't remember from the top of my head.

Lola: Oh, there is a comment from them pending from 2023.

Luke: Oh, so I don't include this in my comments, so I will double check and modify my comment.

Lola: Jeffrey did mention it in the gh comments, so you can find it.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Lola: Skip

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Lola: Skip

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

(added during TAG Atlantic breakout on 2026-06-03 at Lola's request)

Lola: we discussed it yesterday and we added it for a reason here. We wanted to get Hadley's input. Ehsan can you do that?

Ehsan: yes.

----

Lola: Also, no open issues for the triage. any other business? Luke and Ehsan, just remember Jeffrey will be on leave from Monday and we are not having meeting on the week of June 14th. We are also voting for interime chairs. If you want to be chair, send + or if you disagree send -.

Ehsan: can associates be chair?

Lola: I don't think so, I will ask the chairs.

Ives: I am not sure if the interim chair is official chair, need to check with W3C and we need to discuss that.


## Atlantic Breakout (America / Europe) - [2026-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20260605T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending:  Brian, Jeffrey, Mike, Lola, Heather, Matthew, Dan, Yves

Scribe: Mike

Regrets: Christian

### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin

Jeffrey: we made a decision: Wer'e going to try to put together a patch to infra. I'm not going to get to that this week. Marcos replied in the infra issue with that plan. I'm not sure what needs--I think someone will need to add to infra to cite this spec.

Lola: When that probably becomes absolute, feel free to update and clsoe this.

Brian: we need this to move along before adding to infra

Jeffrey: We could wait until it's a published finding, but we could also move it along in the mean time.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Lola: Last time we discussed this, we said if we coul not find a co-chair for Matthew, we would drop it. Is anyone willing to co-chair with Matthew? If not, we can ask in the other sessions or in Slack.

Heather: I don't have bandwidth

Lola: I think that's generally true. As a reminder: this is not a weekly meeting. It's more about managing assignments of design reviews and helping onboard people as they join. It's more experimental

Matthew: Right. It's more of a group where we won't be meeting. Right now, bandwidth is an issue for me. I'm sure everyone's busy. I actually really would love to try this. The challenge is the activation energy. If we haven't got bandwitdh to do it right now, maybe we should reconsider this around the Vancouver TAG meeting time. The one thing I could do in the mean time is to look back in the minutes where specific things have said, "I'm not clear on XYZ." Those signal opportunities for improvements to the draft charter. I'd like to do that. Maybe we just wait till we meet in Vancouver--use that as a cut-off point. By then, I should be able to clear up those other questions.

Lola: I agree. I would discouage you from chairing this group at this time based on what you've previously shared with us about your availability. However, the activation for this work might not be as hard if we wait till TPAC. TAG doesn't typically host sessions, but it could be successfully even for a room of 10-15 people. Let's revisit in Vancouver. Just note that is close to a new set of TAG people jioining. The term will be ending for at least half of the people in this group (and I don't know who will be running for reelection). I will remove the "agenda" label for this, and we can discuss in Vancouver

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Jeffrey: Nothing to bring up here. Sarvin is feeling overloaded, and I'm going on leave. We might want someone else to jump in if we want to keep progressing it over the summer or we might want to pause it.

Lola: Any interest?

Brian: I can try to help. I will be gone for the same three weeks as you, Lola, so I won't be available during that time (or immediately before and after), but I'm happy to add my name and help when I can.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Lola: Same question. I'm assuming nothing to add, either? Okay, cool.

Lola: Explainers have been a requirement for TAG review as long as I've been here. For some reason, that has been a bit controversal, at least over the past few months. We recently made changes so that as long as some key parts of the explainer are in the psec, there doesn't need to be an explainer: alternatives considered, accessibility, intro, etc. Maybe there's confusion about those recent changes--that's just a hyptheiss

Jeffrey: There are no hard-and-fast rules. That may be a problem. There's nothing that only belongs in the explainer. That might confuse people--they want rules, but the guidance is "start by putting all this in an explainer, and when you write a spec, you can move it as ncessary".

Lola: I think people may start writing explainers after writing the spec, which is always a mistake.

Matthew: I agree. I've seen where there is duplication between the explainer and spec. It seems confusing to me. We don't want to increase burden on editors. I wanted to take the temperature of the room: when Lola was speaking and when Jeffrey spoke: I've never seen "alternatives considered" in the spec--that only belongs in the explaner to me. Maybe because it makes the spec seem less authoritative...? I might suggest that always belongs in an explainer rather than a spec, but maybe that's me.

Dan: I agree. Important in an explainer but perhaps not in a spec (at least not with the level of thoroughness we expect)

Jeffrey: We should do a better job of documenting architectural decisions, and maybe ADRs (https://adr.github.io/) are the way to put this next to the spec.

Lola: If folks are not going to maintainer explainers, I think we need a place for things like "alternatives considered", especially if we want non-oimplementer audiences like policymakers. That info would be useful to them, but that's just a minority of people.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Lola: I was under the impression that there was no longer attribution.

Brian: I've been looking at this. It's kind of complicated. There's a lot there and a lot of history and a lot of controversy. A lot of pushback on their mailing list. It kind of bifurcates the conversation. One thing I noted in the issue that I don't understand: they have this thing were you have to choose--basically there's a service in the browser that's exposed that will record impressions, basically. You want to say, "they were shown this ad." It records these things locally. Then, a little like the report-only feature in CSP (not right this second, but it will batch and send to a service so it can't be tied to you or a specific time or event). It exposes a collection of URLs that are the service endpoints where the data will ultimately be sent. Thebrowser ships with support, or it has to go get support from somewhere (a third-party service like Mozilla). You have to pick one of those URLs. The obvious choice is to pick the zeroeth one. They allow for fallback options. But then they have a thing where you can provide a URL. I don't understand why. They say if you give a random URL, it won't work; it has to be in a list.. It feels similar to a lot of other things we've tried to standardize in the web platform that have been miserable, like voices in Web Speech. I'm curious about that particular design decision.

Matthew: I can't answer that directly, though I'll definitely look into it.

Jeffrey: The usual reason to do this is that the web service needs to trust one of the services (that's what happens in Federation). I don't know if that applies here. If there's not a "website trust" decision, then that would be appropriate. The browser supports certain servers. The Website can decide, "I trust these bu tI don't trust those". The website may not trust everything that the browser trusts (since the browser is the user's agent).

Brian: It's not the negotiation that I have a prolem with. It's that you have to provide a URL that has to be present in the browser list. Why not tive you back some thing that represents the service opaquley. It says "service URL",  but you can only supply whichever one which happens to be present in that browser .All of the things that effect the available voices for web voices apply here, too

Jeffrey: This shows up in payments, too. The payment providers and the underlying contracts. It's also just a string.

Lola: An explainer would have helped with that. We need to tell them to write an explainer for this.

Matthew: I had a different question, more basic. .I'm aware of three proposal for attribution reporting: Googgle's for privacy sandbox, Mozilla and Meta had one (IPA, I believe), and Apple had one which was PAM (private attribution monitoring). Google's has two parts: a batched differential privacy part and a more real-time part (more privacy leakage but more info for advertisers). The others don't have the real-time part--just the batched part. My understanding is that Google's w/o real-time and the other two are very similar, and that this is an attempt to harmonize. I don't see Apple participating here, though, so I don't know where they stand.

Brian: There's a web-standards position open for it. It doesn' thave a position, yet, though. We know that Mozilla (in the sense of the people working on it) are supportive. It'd be a surprise if they changed. I don't know about Apple.

Jeffrey: I think they've been participating, but I can't find a source for that.

Lola: We can ask Marcos in Slac.

### [design-reviews#1223: Other Spec Review: Responsively-sized iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1223) ([Github](https://github.com/w3ctag/design-reviews/issues/1223)) - @dandclark, @toreini

Dan: I have one main concern: this is a two-way opt-in. The embedding site lights up the feature for iframe, and the iframe has a one-bit opt-in--a meta tag that they include. The embedee does not make any decision about who they enable it for. Multiple embeddees can pull in an embedder if they don't set their CSP properly. I'm not the only one to rasie thise concern, so we can "plus one" the existing critique. I want to be more constructive, though. Should the op-tin be CPS, similar to frame ancestors? I don't know that I have enough of a feel for all of the CSPs to know if that's an appropriate use. If anyone has thoughts on that, I would love input.

Jeffrey: CSP is very complicated, and I'm reluctant to say "please add more stuff to it". Maybe we stick the list of domains in this meta tag. Or we say, "find a way to put this info next to each other."

Dan: I can draft a response along those lines. I'll check with Esahn before I post.

### [design-reviews#1221: WG Revision: Selectors 4 (Github)

Brian: nothing to add . This has been completed.

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github]
(https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Mike: I posted a draft response. This element represents the first time a spec has recognized "pausing" a video/media stream as a feature. Wondering if there's an opportunity to provide more security guarantees. Right now, authors can pause, and there's no guarantee about what it means. More to be done? Pausing in a standardized UI might be safer since your stream couldn't be re-enabled without your consent. This spec just sets the 'enabled' property, which developers can modify. Room to make it so they can't?

Lola: Think that sounds positive. 

Matthew: One of the WCAG guidelines is that videos should be pausable. Seems like a good thing. 

Jeffrey: This is about recording.

Matthew: Also sounds like a good thing.

Lola: Review Mike's draft? Jeffrey's thumbs-up'ed.

Heather will. Once it's thumbs-up'ed, Mike feel free to post.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Lola The last update was on Slack--Brian is having Dan Applequist on his podcast

Brian: Previously, we decided to hold off on publishign a finding. I recorded the podcast with Dan this mornig. I'll be writing a blog post with my own thoughts and return here.

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

Brian: We don't have any upate other than what's on the issue.

Lola: You haven't posted anything publicaly, so maybe you have a draft that needs to be posted.

Dan: It might be good for TAG to weigh in on the level of dynamism that should be supported .One extreme is that wehn you create the element, its behavior is "locked in". Other extreme is more like the <input> element today; it can switch at any moment. The current propose tries to split the baby on this: when you attach internals, you decide on the behavior to lock in. You can defer that decision to when you append it to the DOM, though. If Luke or anyone has an opinion on that, it might be a good place to comment.

Brian: Luke and I have differing opinions. I would rather not enable changing dynamically. It feels really easy to just allocate another element that shares almost all of the same stuff.

Dan: My thinking agree iwth yours: input types chould be considered bad. The current design represents a compromise based on author feedback. Even if the TAG statement is that we couldn't reach consensus on this point, that coul be a useful datapoint for the editors.

Brian: I haven't reviewed this in maybe two weeks. We should circle back on it.

### design-reviews#1205: WG Revision: MathML 4 (Github)

Jeffrey: We finished this--posted a comment yesterday

### [design-reviews#1209: [wg/ag] Accessibility Guidelines Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1209) ([Github](https://github.com/w3ctag/design-reviews/issues/1209)) - @jyasskin, @matatk, @hlflanagan

<closed>

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

(Sarven not present, skipped)

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: nothing to add here

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: Nothing to add here


### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Matthew: Jeffrey and Hadley's input was requested; maybe we can get their input on this call.

Lola: It's a long one, so maybe Jeffrey can thumbs-up or thumbs-down async.



* Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
