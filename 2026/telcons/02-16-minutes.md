# TAG Minutes - Week of 16 Feb 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/02-16-agenda.md).

## Atlantic Breakout (America / Europe) - [2026-02-16](https://www.timeanddate.com/worldclock/converter.html?iso=20260216T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Matthew, Ehsan, Lola, Christian, Yves, Heather

Chair: Lola

Scribe: Christian

### Welcoming Heather

(Lola, Hadley, and Yves explain the TAG working mode.)

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Matthew: I will review Jeffrey’s PR (https://github.com/w3ctag/abcde/pull/5) today. We wanted to keep the acronym very visible, but rename the group.

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

Matthew: We talked about this last week, wanted to send in a PR that the ambiguity is on purpose, didn’t have time for it yet.

Lola: Is it urgent?

Matthew: It is, will do it when I’m back.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

(No update.)

### [tag.w3.org#97: Homepage updates](https://github.com/w3ctag/tag.w3.org/pull/97) - @ylafon, @hadleybeeman, @lolaodelola

Lola: Yves, I approved this PR, are you waiting for Hadley?

Yves: Waiting more for Sarven, but we can probably publish that as is.

Hadley: I think we can, don’t wait for me. We can add the city later, as @dbaron requested.

### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

Lola: Martin has replied to my question. Wanted Martin to be explicit in his concerns, found the original concern a bit vague. Haven’t read over the response. Heather and I have commented in the private-brainstorm, and I have two questions: 1) Hadley, you mentioned this is not… oh, Lola and Martin have replied? Does Martin still have access to the TAG org?

Yves: Yes, and it will be removed after the next F2F. Usually, we keep departing members until the next F2F.

Lola: How can we continue the conversation when he leaves the org?

Yves: There is still the Slack.

Heather: Read through the doc in question. What I saw is that it is good in defining terms, but not in providing direction. Think some of the internal comments regarding the specific algorithms, and I wanted to point out that I think the authentication definition is wrong.

Lola: Did you have a look, Ehsan?

Ehsan: I have, working on a comment. Overall, my feeling is that this could be good start, but it’s just a start. Doesn’t go further than that. Many of the things are available in the textbook as well. Is this repetition really needed? Mainly talking about concepts. Language that only cryptographers understand may not be helpful for the audience.

Lola: Think they need to pick an audience. Don’t think it’s appropriate for application developers, if this means web application developers. I think it could be appropriate for spec authors or standards peope creating standards and specifications.

… However, the document came to us not from the group, and it seems it isn’t finished. So, the group didn’t ask us, it isn’t finished, I don’t think we have to say something here. I think they are now aware of the things that we were pointing out.

Hadley: There might still be some value in pointing them out anyway.

Lola: Would a document like this usually pass our table, like a design review would do?

Hadley: Probably not, it would either come in via the Horizontal Review process or the Blink launch process. I think it’s totally fine for us if we have opinions.

Ehsan: Don’t think it’s future-proof; things like zero-knowledge proofs, differential privacy, are missing.

Heather: Agree.

Lola: Based on this discussion, I think we should open some issues on their repo (https://github.com/w3c/security-guidelines-cryptography/issues). There are a few different problem statements that we’ve identified with the document. We should convert each of those problem statements into issues. We should draft them in the brainstorming doc. Ehsan, if you are ready, could you post your review there?

Ehsan: Sure.

Lola: From my perspective, this could be a useful document for spec authors. They should clarify the audience.

Hadley: Process-wise: In the past, we asked whoever opened the review if they wanted feedback. Found we had a hard time keeping up what has been posted in other issues. Over time, we decided to keep the discussion in our repo. Do we know them?

Lola: We do know Simone. They have examples of other people opening issues. Seems like there is a process? But again, they haven’t asked us.

Yves: Yes, Simone is the staff contact.

Hadley: Two suggestions: 1) We could send a link to our GitHub issue to someone so that they are aware of it. 2) It would be helpful to have a summary of all GitHub issues that are of our concern, regardless of where they are.

… Would prefer to have that in the public-facing issue. Sometimes, people go back to previous TAG discussions and have a look at the resolution. If there is no comment that clearly lines out why we have decided like this, people may come to a wrong conclusion.

Lola: Think the first step is that we should draft a closing comment-ish comment, send a link to the group so that they are aware of it, and if they want to do something with that, they can.

(Agreement.)

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Posted the comment, the proponents responded to that, just wanted to discuss that with Yves. I can answer the questions that I have worked on, let me know what the preferred approach for your points are. Then I can forward that to Mike to keep the conversation going.

Yves: Didn’t have a look at it yet. Use case is ? between frame and document to exfiltrate data. He didn’t exactly get the scenario that I had in mind. I will have a look at that, and then we can iterate on the private-brainstorm repo.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: Wrote a comment, think that the two most important people are Hadley and Jeffrey.

Hadley: I’ll have a look.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Hadley: Ehsan has drafted this wonderful comment, which I am on board with, with two editorial contributions. Wonder if it would be better to look at the things separately. Ask them to share their thoughts and then update the explainer.

Ehsan: Ok, if you agree with the final one, just thumbs-up it, and I’ll post it.

Hadley: Ok, but generally I’m fine with it.

Heather: This is my Working Group by the way.

Hadley: Split answer: The explainer doesn’t look complete, the common-sense answer is, you need an alternatives considered section.

Lola: I think we can do both, leave it up for you to device.

Hadley: What are your views, Heather?

Heather: Don’t know your exact question. (https://github.com/w3ctag/design-reviews-private-brainstorming/issues/239#issuecomment-3908582396) This API has been in development for 4 or 5 years now. Yes, it needs the alternatives considered section. But this is basically in response to the deprecation of third-party cookies. This allows us to keep the use case. Front-channel communication in OIDC breaks. The proposal has flaws, Apple and Mozilla have dropped out. They are not actively blocking it, but won’t implement. So there is only Google. They are quite focused on implementation. Discussion results from Google with developers don’t come back to the Working Group. We have many explainers for this one API. The only goal is CR.

Lola: I think it’s worth bringing this up to Jeffrey to encourage participants to bring the information back to the group.

Hadley: We should add "missing multi-stakeholder support," and point it out when we get to that point.

Ehsan: This is a stepping stone for agentic browsing. But I think there must be some coordinated action across browsers.

Hadley: We can always say "we think this is bad for the Web."

Heather: Want the group to make their own technical and architectural decisions. Can talk directly to the editors, but want to be a relatively neutral chair when it comes to the technology itself.

Hadley: We can always add to the comment that you personally didn’t take part in the decision.

Yves: Also remember there is a requirement to have two implementers to progress towards Recommendation.

Heather: Not sure if the specification would adopt the needs of Apple and Mozilla if they would return.

Hadley: We can talk about it why it’s bad (https://www.w3.org/TR/ethical-web-principles/#multi) 

Lola: Multiple ways we can continue. 1) We can post Ehsan’s comment. 2) The consensus in this group that this is bad for the web based on the lack of multiple implementations.

Hadley: We should talk to the entire group.

Lola: Put it to the plenary?

Ehsan: This is a hype area of discussion. Genuinely think that authentication needs to be solved at some point. Also, don’t want the TAG to be seen as blocking that effort.

Lola: Don’t think this indicates that TAG is antagonistic to Agentic Browsing. We can always weigh it against our principles. If it is socially harmful or technically harmful.

### Discussion on global system components

Lola: Reminder that we wanted to talk about a new design principle on global system components?

Christian: For example, AI models that are downloaded, and then available to all websites.

Hadley: How is that different to extensions?

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Matthew: from a perspective of consistency, it seems that this is consistent with other parts of CSS. They've also tried to make it all done in the same way. Seems a useful feature, will address some of our concerns about the robustness of the animations when you go back, scroll up, etc. A solution to a genuine problem. Would appreciate another view.

Lola: I will have a look at this.

### AOB

Hadley: Heather, will you be at the F2F?

Heather: Partly.

Lola: This time, we wanted to do less design reviews, but more findings or other bigger work.

## Pacific Breakout (Asia / Australia / West America) - [2026-02-17](https://www.timeanddate.com/worldclock/converter.html?iso=20260217T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair:

Scribe: 

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu
### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @xiaochengh
### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1134) ([Github](https://github.com/w3ctag/design-reviews/issues/1134)) - @jyasskin, @dandclark
### [design-reviews#1191: Incubation:  Spell Check Dictionary API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1191) ([Github](https://github.com/w3ctag/design-reviews/issues/1191)) - @marcoscaceres, @dandclark, @toreini

## Eurasia Breakout (Europe / Asia / Australia) - [2026-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20260219T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Christian, Marcos, Lola, Sarven, Hadley, Ehsan, Yves

Chair: Hadley

Scribe: Christian, Sarven

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

Sarven: No update.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven



### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola



### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola



### [Explicitly address mental health and psychological well being considerations](https://github.com/w3ctag/societal-impact-questionnaire/issues/32) - @csarven

Sarven: Here’s a PR: https://github.com/w3ctag/societal-impact-questionnaire/pull/34

… The societal and impact questionnaire touches on mental and psychological help, but not explicitly. So the idea was to help editors reflect on whether harassment can emerge from these designs, or if you combine behaviors.

Lola: Think that we have really good examples of websites that employ designs that have been shown to have negative impacts on people’s health (infinite scrolling, algorithmic timelines). But that is in the hands of web developers. Do we have examples of web standards that have negatively contributed to mental health?

Marcos: Notifications API. Book recommendation "Stolen Focus: Why You Can’t Pay Attention" (Johann Hari). First we added notification centre, then introduced focus mode, now AI filters priority notifications. Interesting how we didn’t think about the effects of that. Think there is something to say, but at the same time, we are also not really qualified.

Lola: I guess it would be helpful if there are examples we could point to, so people could see what we mean.

Hadley: Agree we’re not qualified. Still, we’re talking about ethics without being ethicists. We’ve noted an initial pushback, but still valuable.

Sarven: There is the well-being side, and there’s a line where it crosses over to accessibility, think blink or marquee, so we deprecated that. Do we need to call out anything?

Ehsan: On the socio-technical source of trust, we had a survey. Found there’s a difference between countries and genders. Suggest to stay on the topic instead of looking at specific examples, as people will interpret that differently.

Hadley: On blink tag and privacy, think these are individual aspects rather than societal ones. Feels not right to put individual needs in the societal impact questionnaire.

… Maybe we should add Marcos’s thoughts on Notification API. Think we didn’t capture them anywhere.

Lola: Think having an example in a document like this is important. It’s very easy to dismiss things if there is no example. Agree we should keep it on a societal level rather than an individual one. Think it’s also important in a document to defer to those experts if we aren’t those experts. We can quote/reference them instead. Think Notifications API is a good example, and refer to sources like "Lost Focus" to make clear that it’s not us.

Sarven: Open to adding examples. Would be good to get some reviews, add examples, etc.

Marcos: "The Age of Surveillance Capitalism" (Shoshana Zuboff) is another good example. This is research, while Hari is more from a user’s perspective. Another example is "The Loop: How AI Is Creating a World Without Choices and How to Fight Back Hardcover" (Jacob Ward) on AI. We could say something like "consider the impacts" and have a look at these books…

Sarven: Payment-related specs, would those rise to societal-level concerns?

Hadley: What is your concern?

Sarven: Suppose if options are forcing you into getting a credit card which people may not want to. Parts of the world are unable or don’t want to get credit. There are cultures that want to have credit. Technology enables to require decisions on this.

Hadley: This sounds like a society problem vs. a web problem. Personally, don’t see a problem with the web supporting credit cards, given this is how many people pay. Not sure if we can address this inequality on an architectural level.

… Feel uncomfortable citing Hari, is a journalist, not an expert, some problems with previous publications.

Marcos: Agree, he redeemed quite a bit with this book though. On Payment Request, in some jurisdictions, you need a local phone number. As a foreigner, you get a temporary one, need to charge it at a local store… very different from western methods of payment. Some cultures are very cash focused. Payment Request supports debit cards as well. Tokenized payment was built into the system.

Hadley: Reminds me of a TPAC session, with QR codes, which a lot of Asian countries use. Needs a native app that is scanned at the PoS.

### [design-reviews#1188: Other Spec Review: Scoped View Transitions](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1188) ([Github](https://github.com/w3ctag/design-reviews/issues/1188)) - @matatk, @xiaochengh

(Skipped.)

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

(Skipped.)

### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel

Christian: We asked a question here. There is the fingerprint-ability concern. We also talked about when we review the prompt API, thinks that you can basicaly download AI models to the system as  a global compenent, and in choosing languages and other options, it becomes fingerprintable. 

That was our first reaction. Web speech API with local processing is already there, it exists. It can already download AI modules and the previous tagest with concerns to that. so now they are just adding the quality level, which is a minor change but adds to the fingerprintability. 

We are now waiting for a response. 

Hadley: maybe if we don't hear back next week, let's nudge?

Christian: sure

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel, @xiaochengh

Christian: Would allow you to play animation between same-origin page transitions. Asked some folks but haven't looked myself. Two solutions, one declarative line in CSS - and there is imperative, and 20 lines of code in JS. They could specify the declarative version, and see how it goes. I think they should design the declarative design. The ~20 lines of JS doesn't seem right for keeping around long time. Martin's concern was that the proposal could slow down pages. Next steps: Xiaochengh looked so I'd like to wait for him.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

(Skipped.)

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

(Skipped.)

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: Asked questions/suggestions. We got a response. Generally the use cases are fine. If you do rebranding and move the site across origins. The solution doesn't feel "webby". It uses some cross-vendor approaches. I marked Yves et al on how redirecting works. Marcos for the requirement as well. This is also my WG so it is a bit tricky for me so it'd be good to hav emore feedback from the group here.

Yves: Looked but not in depth. I can understand why they don't want to use redirect. Some cases are a bit weird. Changing things without changing things. So, why change then? Had to re-read. Version number of the app is an idea of sorts was discussed earlier which is problematic as well. Need to dig more into that. Won't have time before F2F. Maybe we can discuss during F2F.

Christian to add a F2F label/add it to the agenda.

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh

Lola: On the agenda because web developers raised a question.

Hadley: Why is the issue open?

Lola: Because it wasn’t resolved. This is the main issue, there have been sub-issues that have been closed, but we didn’t give this a resolution because the sub-issues have different resolutions.

Hadley: What do we need to do here?

Lola: This is not for us. They haven’t responded to Matthew since August. Haven’t shared those thoughts yet. A person from Astro (?) raised a question there.

Hadley: Suggest to reply to the person to open an issue in the CSS repo, and that it’s their responsibility. To clarify that they are talking to the right people. Could we time them out?

### [Verify Dan's comment on processing-instruction use for patching](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/189#issuecomment-3898768417)

(Group requests more time to review this. Christian to put in the Slack channel.)

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

[Coming back to this from earlier in the meeting] 

Lola: Left a comment on this in the private brainstorming, as they responded. Addressed our concerns quite well. Two things, 1) specifying the ranges using contain/cover. This is already used in other places which have to do with images. Good to use existing syntax, but could this be confusing for developers? Or is context enough? Want Matthew and Xiaocheng's thoughts there. 2) Concern about dynamically loading elements into the DOM which could cause problems with accessibility. This is their actual expectation for the API. That indicates to me that there is a possibility that this feature might not apply to elements already in the DOM.

Hadley: Did we ask that question?

Lola: Plan to do this now. Wait for Matthew to check that. Will continue whenever folks are back.

Hadley: Any time pressures?

Lola: Past the deadline.

Hadley: Might be worth asking Jeffrey if this is too late.

Lola: They have been engaging with us actively, they wrote their comment two weeks ago.

### AOB

Lola: Please fill in the spreadsheet for things to discuss during the F2F. 
