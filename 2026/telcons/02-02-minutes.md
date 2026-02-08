# TAG Minutes - Week of 2 Feb 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/02-02-agenda.md).

## Atlantic Breakout (America / Europe) - [2026-02-02](https://www.timeanddate.com/worldclock/converter.html?iso=20260202T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Christian, Matthew, Dan, Jeffrey

Regrets: Ehsan, Yves, Sarven

Scribe: Matthew

### Discuss the "Ballot for ratification of the Team Appointment to the TAG"

Jeffrey: The full TAG members should have an email - please reply! We can discuss things as required.

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

bump

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Jeffrey: We added something last week; nothing for this week.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

*added [suggested structure for alternatives considered section](https://github.com/w3ctag/explainer-explainer/issues/34) to agenda*

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

bump

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: We talked about this last week, and I might just need to write a closing comment. I'll do this. The concern we seem to have is that it doesn't have a statement of support from the other implementers.

Jeffrey: I think we should have our own opinion?

Matthew: I think it's great. Couldn't say if it's impossible to implement, although I'd be surprised. There are standards positions open. They heard back that Mozilla had a comment, on the PR to HTML. Didn't seem blocking. It's just that they haven't said they're going to implement it, and they have been asked.

Jeffrey: We should have a position that we're encouraging other implementers to impelemt, or we should have other concerns.

Matthew: Hadley suggested that our concern be that there wasn't other implementer support, but you're suggesting we be more active, so I'll draft something and bring it up in Eurasia.

### [design-reviews#1146: Incubation: Proofreader API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1146) ([Github](https://github.com/w3ctag/design-reviews/issues/1146)) - @matatk, @toreini, @christianliebel

Christian: I had a look this morning. We said satisifed with concerns to translator API. Also has a model download system, which we also criticised in the Prompt API review, where we did not reach consensus. I was also leaning to 'satisfied with concerns' but then saw Marcos and Jeffrey's comments from November and they may be right that proofread is implemented on so many levels already, e.g. UA, OS, UA Extensions (e.g. Grammarly). So: Do we actually need this? That's the first question we have before diving into a review.

... I prepared a comment, Ehsan wants to add something to it. Want to check with Jeffrey that this next step is what you wanted to do back in November.

Jeffrey: I'm a little unconfortable with them doing this on top of Prompt, as prompt is more general, this is finely tuned. This seems more useful than some of the other AI APIs - I have more confidence in a proofreading use of LLMs than others. Asking what are the use cases makes a lot of sense.

Christian: Removed the sentence about Prompt API. Let's wait for Ehsan, and then post.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel

bump to Eurasia

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

bump

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Loading; please wait.

### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

Jeffrey: Think this is ready to post. The people who have been most active in reviewing my draft aren't here, but I think it's about ready. Will post to design reviews channel, and wait a couple of hours.

Christian: I'll take a look at the proposed comment.

## Pacific Breakout (Asia / Australia / West America) - [2026-02-03](https://www.timeanddate.com/worldclock/converter.html?iso=20260203T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Cancelled due to short agenda.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20260205T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Christian, Matthew, Sarven, Xiaocheng, Yves, Marcos, Ehsan

Regrets: Hadley

Scribe: Christian

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Matthew: We have a complete charter which Martin wrote. There are some remarks, which we need to clarify under us. It’s pretty much there. Everything is pretty clear, except for the name.

Lola: I’m assuming that you or Martin are posting the link to the repo once it’s done?

Matthew: I thought it would be available for TAG members? But will post. Will see that Jeffrey and I can resolve the PRs, and then we will open it up. Early next week. Thanks to Martin, he did all the work

### Discuss the "Ballot for ratification of the Team Appointment to the TAG"

Sarven: I’m concerned about the selection process, and that I can only respond with APPROVE or REJECT. Prefer not to vote / abstain this time. Unrelated to the individual, but for me, it’s important that the TAG has a broader perspective than it currently leans towards. I'm not particularly convinced that the proposal meets the aspirations of the Process e.g. diversity.

Lola: Indeed, many people work for browser companies, either directly or indirectly. Think this is related to the kind of design reviews we get, so I understand how it comes to happen.

Yves: Would more options help, like abstain, concur, etc.? Will tell Ralph that we should consider adding these options as well.

Sarven: Not sure if the process allows that.

Lola: If we allow concur, and everyone decides to concur? Do we have any insights how many people voted?

Yves: Don’t know, it’s a secret vote.

Lola: People who received the email, please vote!

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: I think we posted on this yesterday. Think we’ll just say, I haven’t seen anything architectural, except for being very clear about the implications of using it. Makes it easier to build inaccessible, exclusive experiences. Takes things off the main thread, which we are usually happy about. I don’t think we need to add anything specific to the TAG response. Still working on the proposal with APA, but will send it separately, but that would go to the A11y section. Not to "stop it completely." Just waiting for an answer from them, and APA can file the issue separately.

Lola: Think I disagree with the "we shouldn’t say stop it," I think we should. But we can wait for them to come back before coming to a resolution.

Matthew: It’s labelled "pending external feedback." Shall I ping them?

Lola: You can do that.

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) - @csarven, @lolaodelola

Lola: I have a PR (https://github.com/w3ctag/societal-impact-questionnaire/pull/33/changes) on this. It’s just for expressing an idea, doesn’t have to be merged right now.

… This issue was opened during the Paris F2F. Forgot what the core idea was, and it’s been a while.

… Whenever we discuss Societal Impact Questionnaire, there’s a misunderstanding regarding the purpose of the document. This is not another horizontal review document. If there’s still confusion in this group, we should clarify that in the document. So in the intro of the document, I added a paragraph to clarify the status of the document. That it’s not a formal requirement or checklist.

… Would be great if you could review that, Sarven and everyone else.

Sarven: I’m fine with it, approved it, only minor editorial suggestions.

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

Sarven: No update, currently taking on other work.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Skipped.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Skipped.

### [design-reviews#1179: [wg/vc] Verifiable Credentials Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1179) ([Github](https://github.com/w3ctag/design-reviews/issues/1179)) - @csarven

Sarven: We responded to this last week, shared it with Strategy. There’s nothing new here. There is thumbs-up from others. The charter is up for AC vote. Can we close this on our end?

Yves: Yes, we can close the TAG issue.

Sarven to close it.

### [design-reviews#1174: WG Revision: SHACL 1.2 SPARQL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1174) ([Github](https://github.com/w3ctag/design-reviews/issues/1174)) - @csarven

Sarven: We responded, no feedback from the group.

Sarven to close.

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Xiaocheng: Checked their latest response (https://github.com/w3ctag/design-reviews/issues/1013#issuecomment-3792116303), which convinced me. Previous concerns were … In the latest response, they clarified that. Seems aligned with animation timelines, so we can get a measurement. Think these are still reasonable usages. Propose closing as satisfied, with a remark that the spec should be clear about paint/presenting timestamps and their limitations.

Matthew: Agree. Their latest comment is very clear, agree that we should ask them to make the spec clear. Should we ask them to include it in the explainer?

Lola: Yes.

Matthew: Or, they add it to the spec.

Lola: Or whatever the process is now, so that the key parts of the explainer are part of the spec.

Matthew: If there’s a section in the explainer where this should go, I think it should go in there too.

Xiaocheng: I think previously we said that the explainer is not a temporary document, and it should remain an up-to-date reference for later.

Lola: I think TAG agrees, but it seems controversial outside of this group. I think the middle ground is, put it somewhere and keep it up-to-date in one of the two documents. And that needs to be linked for us.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: Waiting for feedback, no update. The label "pending external feedback" was missing, just added it now.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Matthew: Could not think of any architectural no-nos. There is a11y stuff that we are working with them separately, we are help them to revamp their a11y considerations section. Somebody raised the question if this could worsen the situation for screen magnifier users. Xiaocheng and I don’t think so.

… While you end up with a couple of harmful side effects (two-dimensional scrolling in the web page and the virtual computer screen), which is why … layouts are great. Other thing is, if a dialog pops up somewhere on the screen, you may not see it. If it’s a native dialog, focus usually moves. But things like tooltips etc. may not have this behavior. Might only be a problem if you have zoomed-in significantly. However, I don’t think it’s worse than the status quo, with the benefit of not having to write the JavaScript glue code. Xiaocheng agrees. Don’t think this is a reason to say no, and there are quite some reasons to say yes. Agree that you would need to have some communication between the page and the AT (?) which we may not want to have. We don’t think this makes it any worse, and we should be positive about this.

Xiaocheng: Agree.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Skipped.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Emailed my friend who’s the editor of Pointer Events if there’s any prior discussions on long press. Funnily, people started an issue just last week (https://github.com/w3c/pointerevents/issues/636) to add gesture support. Waiting for the response. Suggest waiting until next week, then close with "no consensus," and go with the Pointer Events effort.

Marcos: Need to check with the Pointer Events WG, they seem to move outside of there scope. That would be a big, big no-no. Their WG is tightly scoped. We might have to inform them about that.

Lola: Two questions, 1) Would you consider Interesttarget outside the scope of pointer events, 2) Do we know who the staff contact is?

Matthew: They are not talking about adopting interesttarget, but add long press support.

Marcos: Think this falls into dangerous territory. Input events are on the WICG side, WebApps owns a bunch of events as well.

Yves (via chat): Staff contact for Pointer Events is PLH.

Lola: Why would long press be a pointer event?

Marcos: It’s a mouse event, but also a general event as well. Came up previously, has implications on various platforms.

Lola: Could mean something different based on the platform?

Marcos: Yes. It’s kind of that, specifying behavior without broad implementer participation.

Lola: If you agree, Christian has captured your concerns in the minutes, I can engage PLH that this is something they should be aware of?

Marcos: Having a look.

Lola: Ok, then just drop a message in the chat.

Matthew: Can we do the same thing here as for #1182? Will draft a comment. Want to wait for a reply. In terms of interesttarget itself, this would be my final attempt. We may have to say "no consensus."

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Right after this meeting, I will post my final comment to the proponents. Then Yves and Jeffrey can have a look. Basically the concatenation of all previous comments, just looks fancier.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: We were in agreement, but a slight nuance: Proposed a private comment (https://github.com/w3ctag/design-reviews-private-brainstorming/issues/207#issuecomment-3850062247) to hopefully address the different views that we had. One of them is "satisfied with concerns," with the concern being that only Blink implements it. Other one is, we like it but shouldn’t say "satisfied" until there’s such commitment. Proposed a comment that tries to combine those. We might need to ask Jeffrey and Hadley to review the comment.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel

Christian: No update.

Matthew: No update.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Ehsan: My review is almost done, think can post it by next week. Suggestion is to put it for discussion on next Thursday meeting so I can get Matthew’s opinion.

Lola: Please ping Hadley, as she’s in charge for the agenda for next week.

### Issue Triage

### [Incubation: Cryptography usage in Web Standards](https://github.com/w3ctag/design-reviews/issues/1190)

Lola: Martin has opened an issue to look at a document regarding crypto in web standards, and Martin has concerns. Think we should assign Martin, anybody else interested? Just to be clear, purpose is to check if the goals are good, and the document meets these goals.

Ehsan: Happy to support.

Yves: Is Martin available for this, given his term ended?

Lola: Right. Let’s assign Ehsan and me.

### [Incubation: Web Speech API: On-Device Recognition Quality](https://github.com/w3ctag/design-reviews/issues/1189)

Christian and Matthew are assigned.

### [Other Spec Review: Scoped View Transitions](https://github.com/w3ctag/design-reviews/issues/1188)

Xiaocheng and Matthew are assigned.

### Other business

There’s a plenary next week, prepare F2F stuff.
