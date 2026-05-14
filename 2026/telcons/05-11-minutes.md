# TAG minutes, week of 11 May 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/05-11-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-05-13](https://www.timeanddate.com/worldclock/converter.html?iso=20260513T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Heather, Brian, Marcos

Regrets: Dan

Scribe:

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu



### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu



### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu



### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu



### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan

General sense that we can merge something like the v3 skill. Jeffrey points out some redundancy in the skill, which Marcos runs through the Anthropic skill-writing skill again.

Jeffrey: I'd ideally like to have a GH Action that shows us how the output changes when there's a PR against this skill. But that doesn't need to block merging the initial skill.

This is approval to merge Marcos' latest output.

### [design-reviews#1213: Question: Capability Delegation stalled -- specs are implementing local workarounds](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1213) ([Github](https://github.com/w3ctag/design-reviews/issues/1213)) - @jyasskin, @hlflanagan

Rick Byers thinks this might be a red herring.

Marcos: It's a common problem, and some of the solutions have some problems. Is the navigation-based system even necessary, since you could do it with a full-screen iframe?

Jeffrey: Rick pointed out that Chromium implemented Capability Delegation. Mozilla is implementing. Maybe Apple should implement before suggesting that we extend it?

Marcos: Independent of WebKit, the pattern is showing up repeatedly. If we can't do it with iframes, maybe we need an HTTP header. Don't be biased by a single solution, like the one coming from payment request.

Heather: What do we do? Take it back since WHATWG doesn't seem to be dealing with it? Lean on WHATWG?

Brian: Marcos, you said it expected to go to WHATWG but didn't. Can add it to WHATNOT. Don't think you're wrong that there's something different that people keep re-solving, that has similarity. Maybe there's an underlying primitive. Seems like a good place to bring it up. I can carry it over. 

Marcos: In the DC API, Mohamed proposed relaxing activation for [navigation]. That's counter to TAG advice not to weaken things further.

Heather: And the justification was that WebAuthn did it. So it's ok in the same family. That's evidence that it's important. 

Marcos: WebAuthn case is peculiar because it's doing something slightly different. How did WebAuthn get away with it? Ricky M on the WebKit side said it's privacy-protecting because X. For payments, it does something different. Becomes Chrome-specific. Things went different direction. Then on redirect. Mohamed, Mustaq, and I will talk. Brian, good to talk to WHATWG once it's in a good state. Would be good to get TAG input. We might be too credential-focused. Big project.

Jeffrey: Suggesting the TAG say: 1) Endorse idea of bringing existing Credential Delegation to WHATWG, and encouraging all implementations to implement it for iframes. 2) Be careful when extending this to navigations. Please bring us a fleshed out design review, with consensus from the various groups who want to design this.

Brian: Random thought: Has there ever been a time when TAG tried to do outreach to find out if there are other similar use cases. To say "we've observed X, Y, Z; gathering more information; tell us if your group is experiencing this." We have 2 use cases, and we're only seeing a tiny look at specific things.

Jeffrey: It's expensive to do that. Don't know we have an available neutral TAG member.

Brian: We could agree on a request, and email it to all chairs.

Jeffrey: Someone just needs to write that request. 

Brian volunteers.

Jeffrey will post the above suggestion as the answer to Marcos' design review question.

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

Heather: I asked a question about nested frames. What now?

Jeffrey: I think you can ask clarifying questions at any time.

Marcos: Will take a look.

Jeffrey: Ask the question now, in the public issue, as yourself, and then we can discuss whatever their answer is.


### [design-reviews#1211: [wg/webauthn] Web Authentication Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1211) ([Github](https://github.com/w3ctag/design-reviews/issues/1211)) - @marcoscaceres, @hlflanagan

Heather will post her comment to the strategy issue and close our design review.

### [design-reviews#1215: [wg/wot] Web of Things Working Group rechartering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1215) ([Github](https://github.com/w3ctag/design-reviews/issues/1215)) - @jyasskin

Jeffrey: Was concerned that WoT was having challenges. They are actually using URLs and the .well-known namespace and have provisions for accessing these over the Internet. Biggest concern is that they don't have a description of how they are re-using existing authentication protocols. Need to ask about that. They also don't describe coordination with oauth or any of the standard authentication systems mentioned. Beyond that, no obvious architectural concerns. 

Heather: Authentication touches on my favorite things. I'm happy to let this progress but do want to comment on authentication things.

Jeffrey will draft a comment.

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @dandclark, @xiaochengh



### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark 

Brian: Responded because this keeps coming up. Dan's wording is a little confusing. Said we're ok with the specifier attribute but the example above it also uses specifier attribute. Probably could be rephrased to be clearer. Domenic is channeling what I was saying. It's ugly but probably necessary. More or less I'm ok with what Dan proposed, but we should clarify the specifier attribute.

We'll do that and give Dan the go-ahead to post.

Brian: Re-read Domenic's thing again today, was relieved that we agree.


### AOB

#### Satisfied with concerns

Brian: The "satisfied with concerns" label is confusing. "Satisfied but we have concerns" or "satisfied with the concerns". 

Jeffrey + Marcos: We're happy to relabel.

Marcos: Confused Anssi. 

Jeffrey: Think only Anssi was confused.

Brian: I've talked to others.

#### 

Heather

## Atlantic Breakout (America / Europe) - [2026-05-13](https://www.timeanddate.com/worldclock/converter.html?iso=20260513T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Heather, Brian, Luke, Christian, Dan, Matthew, Mike, Hadley

Regrets: Ehsan, Sarven

Scribe: Christian

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: Replied with a question, they've responded. (Reading the comment.) Wonder what Lola says, I need more time.

Jeffrey to post request for Lola’s review in the private brainstorm.

Jeffrey: Looks like this is nearing completion. Hope to close this next time.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Jeffrey: Suspect nothing has happened.

Matthew: Confirm.

Brian: We had six associates this year, and the issue is about how to proceed?

Jeffrey: We discussed this during the F2F, and indeed we didn’t update the issue. More for remembering what the state is.

Brian: So this is about the Design Review CG?

Jeffrey: Yes.

Brian: Believe we should not do that.

Matthew: Does the bot track this? We had a good discussion a while ago, where people looked into the proposed charter. Would like to make improvements to that charter, to make it clearer what we are proposing to do. Need to look up the minutes.

Jeffrey: Can you update this issue with a current state?

Matthew: Will do. The bot does not track this, right?

Jeffrey: Exactly, this is only happening for design reviews.

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

(Skipped.)

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

(Skipped.)

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

(Skipped.)

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

(Skipped.)

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Matthew: We’ve got a number of things where we have an explainer and a spec. Some people are not sure about what should go into the explainer and what into the spec. Want to add a section on that if you think this is worth of sending in a PR.

Jeffrey: If it has confused people, that seems worth adding. You can also open an issue if somebody else wants to write it, but also happy to receive a PR.

### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin

Jeffrey: Answer we got from Anne was he doesn’t want people to reference a normative spec. Asks to send patches to Infra to make the spec align with what we write here and to have Infra cite the document. But not update the global definition, it should remain pointing to Infra.

Heather: Manually keep specs in sync? That doesn’t sound right.

Brian: Think we suspected that may happen. Wanted to have a single place for what is a user agent. Curious if we just update the one that exists, it would inevitably have to be shorter than the full document that we are writing here now. We can certainly write more as its own finding and link it up. This seems like a clarifying opportunity. What is the goal/scope of this effort? If it needs improvement, we should work on it.

Hadley: Totally behind what you’ve said, don’t think the vehicle matters. The fact that it came from the TAG is what matters. Don’t think it’s a huge problem in day-to-day life, and we can’t tell others what to do. If it’s useful, Anne can decide to take it or not.

Jeffrey: So, we shouldn’t try to update the global definition what a user agent is? We should just write our document and let others decide what to do with it?

Hadley: It’s fine to let them know what we have written. But if he’s not interested, that’s okay too.

Jeffrey: Think he’s up for working with us. But suspect he’s not up for adding the entire user agent document to Infra. Sounded open to take patches for the Infra definition. Right now it’s still close to what we have in our document. Brian’s question is important though, given that Infra has  a definition, already, then what is the document’s goal? List of duties, kinds of user agents, etc. Duties are already in privacy principles. But this is broader. Also, we cover the ecosystem they sit in. Would be worth publishing even without that component.

Hadley: Would it be worthwhile having a discussion about user needs?

Jeffrey: Think we’ve talked about that, also wanted the tech press to use it, and maybe regulators.

Hadley: So this gives us the framework whether the ecosystem stuff should go in there.

Jeffrey: Think it helps to some extent to notice when the ecosystem is breaking down.

Hadley: Feel I’m too far away from what you’re doing here, so I can’t really help.

Brian: Sounds like good answers, I’m curious about which parts we want to upstream, and what we don’t. And how to make that split. Duties are something we came up with more or less. Think the Infra standard does not have the concept of a web user agent?

Jeffrey: Yes, it assumes it’s the web.

Brian: So where is the web view line? Is there a line? Or is it two lines? Feel this needs like a significant amount of time if we want to do it.

Jeffrey: On our section on web views (https://w3ctag.github.io/user-agents/#ua-as-software), the web view group said this is useful. And the CRA spec…

Brian: Nicola (?) contributed to this, I know there’s a discussion they could use that in ETSI/CRA. But doubt it will be done in time.

Jeffrey: Apparently it just has to be in TR so that an ETSI spec can refer to it, and that’s already the case here.

… Think we need to figure out how to deal with Infra, but we won’t update the global definition of a user agent (https://infra.spec.whatwg.org/#user-agent).

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow

Matthew: We got some replies on this. We asked them about 1) updating the explainer around modifier keys, 2) spatial navigation, and if somebody uses a d-pad, spatial navigation mode, etc.

… Think the spatial navigation isn’t really progressing, but they’ve replied that they’ve updated the explainer, and provided links to 1) and 2), so it seems fine and they’ve addressed the concern. Need to read the part on spatial navigation, but the answer seems positive. Just need to check the explainer if the content is there.

Brian: Also think these look like completely reasonable answers. Talked about _CSS_ spatial navigation that didn’t make progress. Spatial navigation itself did advance.

Hadley: Use case?

Brian: Uses the d-pad to move around the focus items, points of interest, or on a game console. Lot’s of things. It’s not standard already (so a lot of stuff is weird), at least this is a definition that is standard, so it’s way easier for people to build on that. Believe it’s very positive.

Luke: Reviewed the PR to the explainer, think it addresses the points exactly. Happy with the result.

Matthew: Sounds like this is likely a positive (satisfied) closing comment. Okay if I draft this? Would raise it if any concerns should come up.

(Agreement.)

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: Sounds really good, need to refresh myself on the context, believe they are in harmony with the idea of making it simpler in the future than it might have been, which was my main concern. Will take a little bit of time to double-check on that. But seems good.

Jeffrey: So you plan to close this as "satisfied?"

Matthew: That's a good idea. Paul Grenerra (APA) ? raised that there are other areas that deal with scaling text.

Jeffrey: text-fit?

Matthew: Yes, but also shrink and grow and the others. There are some related issues. On this particular one, sounds like it’s heading in the right direction.

### [design-reviews#1206: Other Spec Review: OpaqueRange](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1206) ([Github](https://github.com/w3ctag/design-reviews/issues/1206)) - @matatk, @lukewarlow

Luke: Had a look at this, API itself seems good, not heavily scoped on form controls like it used to be, they’ve fixed that. Might be used on custom elements on the future. One issue that I still have is, for one of the use cases, a CSS counter part around anchor positioning may be useful for this. Left a comment on the private brainstorm, maybe Dan can answer this. There is an emoji picker when you type a colon. It would be good to know if that’s a limitation of the demo or if it’s not part of the API design.

Dan: Yeah, the demo should have a "scroll" listener... contenteditable, drawing a range around the selected text, drawing a bounding box around the selected text. There’s maybe another feature proposal that could be considered future work. I think of this as a way to get people started … you would need a scroll listener to do this right

Luke: Agree it’s making one part of this nicer, and follow-ups are possible.

Jeffrey: Feel without anchor positioning this is never scrollable on the background thread, so we could say we are hoping or a follow-up feature. But sounds like satisfied?

Luke: Yes. It's also not just the scrolling, but block flipping.

Jeffrey: Do you want to take a look at this before Luke sends a comment?

Matthew: Don’t let me block it. I’ll take a look as soon as I can, but I don’t think there’s anything significant I could add.

Luke to write a draft comment.

### [design-reviews#1187: [wg/das] Devices and Sensors Working Group 2026 Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187) ([Github](https://github.com/w3ctag/design-reviews/issues/1187)) - @jyasskin, @marcoscaceres, @christianliebel

Christian: We're on it. 5 major points. In the deputy process. Think we have consensus for some but not all points. We'll let DAS know. Effectively it's the existing things, and we've prepared charter text and PRs to resolve the comments. We'll see if the WG is fine with the changes.

Jeffrey: Update on the timeline, they try to finalize the disposition of comments today, and then we’ll see if and how they reacted to our suggestions.

### [design-reviews#1194: WG New Spec: HDR on the web (CSS, Canvas, WebGL, WebGPU)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1194) ([Github](https://github.com/w3ctag/design-reviews/issues/1194)) - @jyasskin, @xiaochengh

Jeffrey: Marked this as satisfied, but forgot to close. Closing it now.

### [design-reviews#1035: CSS Gap Decorations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1035) ([Github](https://github.com/w3ctag/design-reviews/issues/1035)) - @matatk, @xiaochengh

Matthew: Think this is a quick one. You thumbs-up’ed my closing comment, which I then didn’t post. So I can just close the issue, sorry for the delay. We will close this as satisfied.

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini 

Matthew: Ehsan put in a comment on that one.

Jeffrey: That’s on whether the user media explainer needs it’s own S&P section. Which I agree with. Don’t think we need to block on them adding them, and then do the review. However, I expect there are interesting implications for usermedia where they should consider alternatives.

Brian: Is it shipped?

Jeffrey: It’s not shipped. They are pausing their launch and extending their origin trial. (https://groups.google.com/a/chromium.org/g/blink-dev/c/V_ef1L9BtHw/m/FTqZZLOSAQAJ) However, I don’t expect that we will get feedback in time. We should post those comments in parallel, with asking for the alternatives considered and other sections for this explainer.

### "Satisfied with concerns"

Brian: It always struck me that this sounds like we’re satisfied with the concerns. Sound’s like "well, ok." Sounds like, we don’t like it. Think the label is misleading at worst, but not very clear at the very least. Wonder if we can think about another label for that, that would be clearer?

Matthew: +1. Will think of some.

Dan: Can we just add a comma? (satisfied, with concerns)

Brian: Not sure if there are commas in GitHub labels. Think it would be better if we said something else.

Jeffrey: "satisfied, but concerns?"

Hadley: Are we satisfied in these cases, though?

Jeffrey: Normally it is, "we won’t make a fuzz around the concerns."

Heather: (AC review)

Jeffrey (chat): "does not support incorporating the proposed corrections and additions in the W3C Recommendation for the reasons cited in comments but is not raising a Formal Objection (your details below)."

Luke: TAG can’t block things, "unsatisfied" is not more blocking than "satisfied with concerns". But it could be clearer. Unsatisfied = we don’t approve this, SwC = …

Hadley: In the past, this meant we’re not 100% behind it, but progress was good, …

Matthew: If we ware doing some wording changes, we should make sure that the set of possible outcomes appear to be on one particular axis. If we change this to "concerned, but not objecting" it does not fix on the "satisfied … unsatisfied" spectrum. It should be obvious where it is on that set. AC already has a nice vibe. We can certainly object on stuff. Happy to help renaming the label. We need to be clear.

Hadley: We should be very careful about that, to not break the previous structure. But if we need more, we need more.

Jeffrey: We have 14 resolutions right now.

Brian: Interesting point on "blocking" things, which we can’t. Maybe "strongly suggest…" or something would work. "strongly dissatisfied"…

Matthew: Seems like there are two proposals for axes. How do we feel about it in terms of satisfaction, and the other one is the magnitude of changes we’d like to see.

Jeffrey: Suggest that a group of interested people come up with a suggestion (new labels, merging existing ones, …)

Matthew: Happy to do that, also put that together visually.

Luke: We should try not to change the meaning of the existing labels too drastically. If unsatisfied is the default "we’re not happy with this", we should move SwC to unsatisfied, and make unsatisfied "deeply unsatisfied" or smth.

Hadley: Believe Lola was involved in the last version of expansion. If there’s a discussion, make sure to involve Lola, or at least ask.

Jeffrey: Suspect you will file an issue in the process repo with Agenda+.

Heather: Happy to assist.

Matthew: Can you put tables in Slack?

Christian: Yes, there's a canvas feature. You may want to have a separate channel for that.

Matthew: Maybe a Google Doc?

## Eurasia Breakout (Europe / Asia / Australia) - [2026-05-14](https://www.timeanddate.com/worldclock/converter.html?iso=20260514T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Ehsan, Matthew, Luke, Hadley, Christian, Marcos

Regrets: Lola

Scribe: Christian

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

(Skipped.)

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: Posted my proposed comment, no one else assigned. How does it work?

Hadley: Is any TAG member expected to disagree with you?

Ehsan: Don’t think so… if others could have a look, that would be good.

Hadley: Editorial thoughts, we need to be very clear about what we want them to do. Hearing their thoughts? Requesting changes?

Ehsan: It’s mainly questions from me, I didn’t expect any actions. For the second one, that’s more like a recommendation for the future than something concrete expected from them. At least for now.

Hadley: Recommend you restructure your asks accordingly. Ending with "we look forward to hearing your thoughts." Any thoughts on the actual content?

… Another editorial thought, can you say "can you?" instead of "proponents." You can put your privacy concerns with connection stats and frame it as a question.

Ehsan: Good point. Can also directly post them as an issue.

Hadley: Let’s start with asking a question.

Ehsan: Ok. If anyone has a remark, please reach out to me. Overall, I think this seems fine.

Hadley: In terms of process, you should reach out to Yves.

Ehsan: Will do.

Hadley: As this is not a closing comment, I think you’re doing all the right things. You don’t need to get full consensus for that, as we’re still in exploring mode.

Ehsan: Ok, will get as many responses as possible, in a reasonable time.

(Later:)

Marcos: I may have a look, happy to read stuff.

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

Matthew: Jeffrey posted a good point on this one (requirements changing in WCAG 3). He suggested that we raise that as a question. Will draft something along these lines. Number of concerns, related to CSS, about growing or shrinking the problem. Ironically, growing the size can turn out to be a problem if you zoom in. I will check to see if there’s anything we’ve got that we can forward to APA. There’s a lot of concern about this. Lots of author consideration required. Not as helpful as what Jeffrey suggested. Will work on a comment.

Hadley: Priorities? Deadlines?

Matthew: Was merged into CSS three weeks ago, we didn’t have long. Guess this is rather urgent. Lots of open issues.

Hadley: As they are asking, we should give them feedback.

Luke: Think merging into a draft with open question seems fine. Seems like this is how CSS works.

Hadley: Seems to be a Chromium thing without a position from Mozilla or WebKit.

### [design-reviews#1214: [wg/math] Math Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1214) ([Github](https://github.com/w3ctag/design-reviews/issues/1214)) - @christianliebel

Christian: Didn’t get to this, will do it next week.

Hadley: We should ask Yves regarding the deadline.

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: Waiting for your thumbs-up in the brainstorming, Hadley.

Hadley: Seems great. Would add a closing like, we're closing now because we think we've helped as much as we can here; if you want to have a conversation, feel free to reopen. 

I don’t need to see that addition, happy to trust you to draft it.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel, @xiaochengh

Christian: this is fine for me. I can draft a comment based on our recent brainstorm discussion

Matthew: Think the comment looks great. Slightly out of touch with this one, is it sufficiently clear, that we are not happy about the imperative one? Noticed that even the proponents said it seems footgunny.

Christian: Think we’re satisfied with the imperative version, and can make that very clear in the closing comment that we’re concerned about the imperative one.

Matthew: Yes, because it’s very complex/footgunny. Apart from that, agree with what has been written.

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

*closed*

Christian: This should not be closed, we are asking for feedback.

Marcos: Right, it should stay open.

Hadley: Ok, will reopen it.

Matthew: I added the "waiting for external feedback" label.

Christian: And then we should wait for the proponents to respond.

Hadley: Will reach out to Heather that say that we've done this.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh

Matthew: Need to catch up with this. No update apart from that there’s a lot of approval regarding this from the a11y side, but also a lot of concerns from the rendering side. Nothing definitive yet. What does TAG feel? Any milestones/deadlines coming up?

Hadley: Lot of good opinions in the brainstorm.

Matthew: Luke, you had concerns about privacy?

Luke: I wasn’t at the meeting. There’s a lot of private data already accessible, most of those are handled. As for deadlines, I don’t think there are any immediate ones. No immediate timeframe. They want to make this happen, but it a way that it works for everyone. Would be curious to hear a11y folks what they think. From what I’ve heard, feedback was positive so far.

Matthew: Oh, definitely! We were asking for this for a long time. A lot of nuances, some of them are quite big. Certainly seems worth that one of us (also meaning someone with an a11y perspective) to join the WHATNOT meeting.

… About the privacy stuff, know that people think the data they enter into a form is only sent to the server when they hit "submit," which may not be true. As you say, a lot of things people think are private may not be actually private. 

… We shouldn’t necessarily object to things if they don’t make the status quo worse. If the status quo they’re building on is already bad, what should they do?

Hadley: +1, and would like to work on a finding with one of you if form data is sent over to a server, TAG finds this harmful.

Luke: Trying to be better with agendas planned beforehand regarding the WHATNOT meetings. We could do an extraordinary call like we had for interestfor if needed. Agree that bad precedent shouldn’t be used as precedent. For example, there’s some things that SVG filters can do. That shouldn’t be baked into HTML in canvas. So we have to draw a line somewhere. Where we draw that line is gonna be interesting.

… Regarding the finding, think from a privacy perspective, that would really be interesting. If we can have such examples where the user expectation does not match reality, it seems reasonable detecting them.

Hadley: Let’s have a look at that during documents week.

Matthew (via chat): Would be happy to be a part of that effort.

Ehsan: Agree there should be some form of technical analysis, is there a plan or follow-up?

Luke: If we can find research on this, that would be helpful.

Ehsan: Think this is a cross-culture, cross-border, demographical thing.

Hadley: Feels like there's a lot left to do in this discussion. Some is TAG, some is in other groups (e.g. APA, ...). TAG may be happy to defer to other groups. We've not put anything on this issue yet. Can we construct an update. We can point to things that are in progress in other groups. Do we need a holding statement? What is clear at this point?

Luke: Having a comment about the ongoing issues - which are blockers to us being satisfied - there are too many unknowns at the moment. They don't need to be concrete, but just pointers to the discussions. We should let the discussions pan out before we form an opinion.

Matthew: I think the one thing TAG agrees on is that this is worth solving.

Marcos: Good summary, but it has to be constrained. We can’t go outside the browser, so things should stay in their lane. There are things beyond the browser’s control, such as platform APIs or OS.

Hadley: Is it heading in that direction?

Marcos: Not sure, need to check.

Hadley: If it didn’t come up so far…

Marcos: Ok, will check. 

Hadley: Action for Luke is to draft the interim update.

Luke to write a draft and put it in the private brainstorm, to clear with Matthew and Xiaocheng.

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

Luke: Need someone to help me draft a comment. Looked into this, think there are quite some serious problems. API design is mostly ok, but there are other things. Seems they only want to ship submit button to start with.

Hadley: What’s the tl;dr of this?

Luke: Original form of this was that you could customize custom elements and add extra behavior. WebKit was opposed for a very long time, so there’s a new effort to see if WebKit could be brought on board. It gives you implicit submission behavior for a custom element. Not sure if we need this, but people have asked for it. Would be interested on what the other behaviors would look like. Might be ok depending on the behavior set, e.g. draggable. That depends on the design. Think Brian agrees with the submit button overfocus. Wider explanation of separate behaviors would be helpful.

Matthew: +1.

Luke to draft a comment and ask Brian for input.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Working on making a final review, Yves had some concerns on the reporting process which I agree with. Need some more polishing for that. We are clear on it. Jeffrey’s or Yves’s thumbs-up would be required. Happy to incoporate additional considerations into the draft comment.

Hadley: Could you put a comment in private brainstorm to ask them for the feedback you want?

Ehsan: Will do that. Good to ask the proponents about the privacy thoughts that Jeffrey raised.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Hadley: Would love to discuss this with them.

… There’s this long-standing disagreement between browser people and semantic web people on if the web = the browser, if RDF is part of the web, etc. Comes up regularly.

Marcos: haha, turns out the Semantic Web people were right... because AI loves to consume that data 🤣

Luke: Does this include stuff like XLST 3, MathML, etc.? Also, web views, …

Hadley: Yes, this is all in scope.

Marcos: Browser perspective, web has the Same Origin Policy  security model. Anything that can’t enforce that, is not the web platform. The platform is built around the privacy and security principles. CORS, realms, … Behaviour changes if you don’t have origins. Specifying for anything else is possible but not helpful. Think AI browsers. Suddenly the inferencing is an interesting thing, AI is good at that stuff and consuming those ontologies, and the semantic web data is interesting and widely useful.

(On AI etc.)

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow



### [design-reviews#1205: WG Revision: MathML 4](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1205) ([Github](https://github.com/w3ctag/design-reviews/issues/1205)) - @jyasskin, @matatk



### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola



### [design-reviews#1209: [wg/ag] Accessibility Guidelines Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1209) ([Github](https://github.com/w3ctag/design-reviews/issues/1209)) - @jyasskin, @matatk, @hlflanagan



### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh



### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini



### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh




<!-- Reviews that have been pending external action for at least 6 months -->
### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1128) ([Github](https://github.com/w3ctag/design-reviews/issues/1128)) - @toreini



### [design-reviews#1153: WG New Spec: Direction feature for `scroll-state()` query](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1153) ([Github](https://github.com/w3ctag/design-reviews/issues/1153)) - @matatk, @xiaochengh



