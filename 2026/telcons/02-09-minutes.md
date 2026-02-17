# W3C TAG Meeting Minutes
Week commencing 9 February 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/02-09-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.


## Atlantic Breakout (America / Europe) - [2026-02-09](https://www.timeanddate.com/worldclock/converter.html?iso=20260209T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Ehsan, Jeffrey, Matthew, Christian, Yves, Dan

Regrets: Hadley

Scribe: Christian

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: Looks positive b/c they work on an a11y section which we can have a look at APA. Was thinking about the robustness section, want to be the behavior more robust. Looks like they’ve considered that with scroll timelines, ranges API. Looks very promising, would respond with a positive comment.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Jeffrey: Nothing that we wanted to add today. If anyone sees something in the issues list, happy to add it to our stack (https://github.com/w3ctag/user-agents/issues).

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Matthew: Jeffrey’s comment is awesome, and great to post!

Jeffrey: Could you post?

Matthew: Will do.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Matthew: Need a couple more days.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

(Skipped.)

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

Matthew: Reason why I raised it, have been asked if non-goals is out-of-scope. Comes up a lot in other explainers. Phrase that exists. Asked for clarification, Martin pointed out that it could mean "out-of-scope" for some people, an anti-goal, or not sought but achieved anyway, or a combination of all.

Jeffrey: We should try to remove that ambiguity.

Matthew: Will draft a PR.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

(Skipped.)

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: No issues to add, but I need to create some. There was one issue from the Paris F2F where we discussed this quite a look. Was looking to find something specific. Thought there’s a bunch of stuff that we should keep track of. Try to get all action items from the Paris F2F into GitHub issues. Would like to work on this before London F2F, but can’t commit.

### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

Ehsan: Not finished yet, but started looking into it.

Lola: That was the issue that Martin opened?

Ehsan: Yes.

Lola: If someone else wants to join, feel free to assign yourselves. We’re not reviewing a specific design review, that’s just work happening inside W3C that he thinks we should be aware of.

Jeffrey: Basically a design principle, asked Google security people to have a look.

Lola: Martin was concerned. Not that we should be biased, but be aware of that.

Ehsan: Share Martin’s impression.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Thanks to Jeffrey, changed the word "tracking" to "leak." Posted the final draft in private-brainstorming. Would post to proponents today if no one objects.

Lola: Yves, are you able to review?

Yves: Doing it right now!

### https://w3c.github.io/differential-privacy-guidance/

Jeffrey: PING just published this document. Sent it to the former Google Privacy Sandbox team, they said that some of their suggestions haven’t been incorporated and don’t feel the document is particularly useful. Asked the PING to write it, and don’t know what to look for, so I asked them to write it up. At some point, we may want to do a design review on this, just a first draft.

Ehsan/Lola: Can we assign ourselves to that design review?

Jeffrey: We can open a design review right now, but you can always read it and file issues.

### Issue Triage

Spellcheck dictionary API

Lola: Is this part of the AI work?

Jeffrey: No. Allows users to have a local dictionary for spellings that they can save.

Lola: Anyone want to look at this?

Ehsan: I can!

Dan: Me too.

### London F2F

Lola: Will look for restaurants soon. If someone has gone to London before and has preferred restaurants/bars, please reach out to me. Assume everyone has filled in their dietary requirements in the spreadsheet. If you haven’t done so yet, please do so, as Jeffrey needs that for office entry.

## Pacific Breakout (Asia / Australia / West America) - [2026-02-10](https://www.timeanddate.com/worldclock/converter.html?iso=20260210T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Marcos, Yu Sen, Brian, Jeffrey, Dan, Xiaocheng

Regrets:

Scribe: 

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu

JY: we have comments from Yu Sen and Martin

Yu: should we consider accessibilty. Should we consider the user agent as a web view. It seems we missed accessibilty. If they cannot read and interact with the content they use agent might need more duties. When the user navigates to an unknown page and through multiple redirections the user agent can take action to protect the user.

JY: We haven't talked about how user agents protect users. Browsers have malicious site protections. 

Yu: for example, when we use a web view to display a chatbot, it could work as user agent.

Jy: we have considered AI agents potentially as user agents, but we haven't addressed their treatment. 

Xiaocheng: In the last f2f we concluded that we didn't consider super apps as user agents. I'll try to come up with some text to explain this.

Jy: I agree that super apps are user agents, but webviews maybe not. 

Yu: There are mini-app pages, there are installed web apps, etc. It's not one user agent in these apps. 

Jy: 

Yu: A miniapp develoeper can use a web view to some particular content to users with some API restrictions. The webview inside the miniapp is treated as a different user agent. 

Jy: the super app is user agent... the super apps I assume tells the user what URL they are viewing, then the super app fits the definition of a user agent. It's still up to me to write a comment about the discussion in 36. You should feel free to send a PR to discuss duties.   

### [explainer-explainer#34: Structure alternatives as: Alternative → Pros → Cons → Reason for rejection.](https://github.com/w3ctag/explainer-explainer/issues/34) - @jyasskin

Jy: this is one that I haven't made progress on. Mathew was also going to take a look. 

Jy: People stuggle with the considered alternatives. We need to give better guidance there. We probably need someone to pilot this before we put into the main document. But I need to send a PR before there's going to be a lot to discuss. 

Bk: It seems like a good idea. Even when not on the TAG, I found myself wanting more discussion in those sections... even how alternatives envoled over time. Sometimes you go around in a big circle. 

JY: Yes, that can happen and it can be frustrating for those making the proposal. 

DC: The reason for not going with a proposal it might be to do with the pros/cons.  

### [design-principles#612: Disambiguate when to add global event handlers](https://github.com/w3ctag/design-principles/pull/612) - @jyasskin

Jy: We need to review if this is what we want to say. This is stuff that Dominic and Annevk have pushed for in the past, so might be worth considering. But we should check if we agree with it. 

MC: I'll take a look also. 

JY: Feel free to merge it. 

BK: It's a very small change. Math event doesn't have any events, but it would apply in the same way. If we are going to mention SVG, then we might also mention Math ML. 

JY: I'm worried that if we mention math ml it might be confusing. Do events propagate through MathML?

BK: yes, and you can embed foreign objects. 

JY: Would you like me to add a comment.

BK: Yes please. 

JK: I've commented... we can merge after we make that change.


### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1134) ([Github](https://github.com/w3ctag/design-reviews/issues/1134)) - @jyasskin, @dandclark

JY: Noam reopened this. The design changed form attribute/elements to processing instructions. It adds processing instructions, which is not something we have traditionally have had in HTML. 

DC: It talks about how to patch sub-trees, and things that are very complicated. Are we sure this are use cases that need to be supported. 

JY: I'm worried about the strange sub-trees you can create. 

DC: I'll try to comment something soon. 

### [design-reviews#1187: [wg/das] Devices and Sensors Working Group 2026 Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187) ([Github](https://github.com/w3ctag/design-reviews/issues/1187)) - @marcoscaceres, @christianliebel

JY: I'm worried about the length of the comment, and the assumption that Chromium-only APIs shouldn't be in a WG.
    
MC: Let's split that into parts. There's vibration and battery status which are chrome only now but were in all browsers, or that was the intention. But some browsers decided to remove tjem. The chrome-only ones fall into the discussion around generic sensors. There's a question of whether use case fort those is valid. The proximity API doesn't list any use cases. So I don't think it's about that it's Chrome only, it just happens that they are. It's more around the architectural models are using the generic sensor. Do these APIs have activity. 
Going back to the start, the motivation was that devices have these sensors, there's APIs to access them, so let's access them; rather than, is this a good idea or not.

JY: Sounds like a.request to write expaliners for each API, if can't write a good one then drop the API.

MC: Could be an explainer or anything that explains the use case, but needs to make a strong case as to why you might have it. So hopefully that covers at least the chrome-only part, which isn't that relevant. If they're a great idea then they shoujld be starndardized. But larger question is, given the arch. was rejected, their utility is in question -- that's the interesting architectural quesiton.

JY: Makes sense to ask them to describe use cases for all APIIs.

MC: Yeah, or at least revisit them.

JY: Just that would be short comment.

XH: I'm wondering how they would anwser use case question.

JY: I thikn it''d be the user-serving purpose of the API.

MC: The web plat is its own thing -- considering is it available to native apps is not an interesting argument. 

XH: But they want to replkicate native app. 

JY: My argument is I don't want their to be a reason to write a native app

MC: That's the correct framing. Comes back to, what is not achievable by the web plat today. What problem is this solving for users.

JY: THinking about whether this is good charter feedback, or good spec feedback. 

MC: I think it's a charter question. This group is tasked to do stuff, they've done stuff over the yeras, based on particular premise abut how we're doing APIs 10-15 yrs ago. It's been rechartered, but completely fair to say in this modern world, is this stuff still relevant? Wake lock API is an example. There's nothing new being proposed from this group, but if they do, should be looking at it in this way. There's also this old stuff: asking, is it worth pursuiong those, put them on recommendation track, which is the larger question. To me that's a charter concern.

JY: Question of do you have use cases for all the specs, and how do you balance specs that allow some abuse but have use case -- good to include in a charter. One other point about which statuses they should develop specs under. Process forbids moving some of these to note track; can't be done after it's patent draft.

MC: In those cases would be nice if there was signaling even in title to say it's a maintenance thing. 

JY: I would want to see examples in other specs we could ask a WG to copy.

MC: Yeah, maybe in payments WG we violated, took the ??? event and moved it out.
This is why it's dangerous -- group very quickly moving things into CR, because it creates bad situation where something is in the rec track and we can't move it out.

JY: That's one of the questions I'd like to get a formal rejection council to talk about. What are the formal requirements to get something into CR. Not really a chartering question yet; could get a formal objection and ask council to review it, but not something I want in a charter review before that point.

MC: Can they drop to working draft?

JY: Yes. But if has ever been patent draft, can't switch tracks, go to note.

BK: Could go to deprecated.

JY: Eventually the ones that are duplicated by consensus spec shouldl eventually go to discontinued/superceded.

MC: That's the real solution here depending on what they want to do. They have these specs with features that may or may not be interesting...if there are cool features, should bring those over to other specs. Hopefully that's conveyed in the comment.

JY: At least for the things that overlap, should be building on consensus spec.

MC: That's the bit I'm unsure of, don't know if there's anything interesting in the other specs.

JY: Marcos can you write concise omment or should I?

MC: If you write I'll focus on making more consise..

BK: We do have group of other things we've been talking about being new charter that would cover webviews, maybe miniapps, IWAs. I can see them being different in some of these areas. Curious about if we ask this question about: based on never getting Apple and Moz to sign on to it, but maybe that's just in the browser itself. Maybe a world where they could be standardized but not in the way we have now. Does that modify this feedback in any way.

JY: I think this might be something where Marcos and I disagree. I think we should be able to get things to rec even if only in chromium. Device APIs don't touch engine much, if they have multiple implementations at OS side and UI side, should be ablet o get to rec.

MC: Don't necessarily disagree -- only on the assumptions on which the APIs are built. We evaluated other things on the same basis. Embedded in Brian's question is about other platforms having these capabilities, we want the same capabilities where possible across all UAs. Don't want different permission/feature model, want cohesive architecture. But there are APIs only exposed in certain contexts, like Badging API, only makes sense in WebApp. MiniApps may fall into this category. Or Push notifications only available in installed WebApps.

### Other business 
JY: if new members of the TAG need guidance or questions please ask. 

BK: There's been a flood of stuff coming in. I'm sure I'll have a lot of questions. I'll probably have a lot of questions at the F2F. 

JY: The current meeting is not at a great time for everyone. We are considering moving it. I'll wait to see that there are no other objections before changing it.

BK: I'm sure I will have more questions

Xiaocheng: Is there a specific channel for TAG member only discussions around TAG appointments. 

YJ: Yes, the appointements 2026 channel
 

## Plenary Session - [2026-02-11](https://www.timeanddate.com/worldclock/converter.html?iso=20260211T220000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)


Present: Jeffrey, Lola, Brian, Dan, Yu, Matthew, Yves, Marcos, Christian, Ehsan

Regrets: Sarven

Scribe: Christian

Chair: Jeffrey

### Intro to Yu Sen and Brian Kardell, the TAG work mode, how everything can change if the TAG members want it to - @hadleybeeman, @lolaodelola, @jyasskin

Jeffrey: Warm welcome to Yu Sen and Brian Kardell!

… Existing participants, anything to share that you would like to have known when you joined?

(No responses.)

Jeffrey: We should write that down.

Jeffrey: Reminder to send in your ratification, so the candidate can join the F2F.

### Reminder that we’ll agree new call times once the second appointment is made

Jeffrey: When everyone is on board, we can finalize the new call schedule. We can also do that during the F2F.

### Chair selection

Jeffrey: There’s a channel in Slack called #chair-selection-2026, where Martin is coordinating selection. If you are willing to chair, raise your hand. If you have suggestions, also put them there.

Lola: You can also ask the chairs how we found chairing over the past year. In one of the Slack channels, there was a discussion about the responsibilities that we had apart from joining the meetings.

Brian: Any progress so far?

Jeffrey: Would be willing to continue.

(Brian expresses support.)

Jeffrey: Not much progress on chair selection until now.

Lola (via chat): Would also be willing to continue.

Jeffrey: Just to be clear, Lola, Hadley and me are the current chairs. I assume we all would be happy to continue.

Lola: We are also happy if somebody else will take it over. Quite helpful that we have one chair from North America, and two from Europe, which helps for the schedule. It would be helpful if that remained.

Jeffrey: Once we talked about chairs, we should also talk about associates. We have this program where we can add associates to the program. Ehsan and Dan are currently TAG Associates, their terms officially ended Feb 1. I should actually re-nominate them. Two or more associates may not share the same affiliation. There is a page about the requirements here: https://tag.w3.org/associates/ Program proved to be helpful.

### F2F planning

#### Developer meetup details - @matatk

Matthew: 12 attendees so far for "Meet the TAG." I guess we need some more promotion. Sent in the proposed slides for web standards to the chairs. Maybe you can use it as a starting point. Hope everyone is aware of the link: https://ti.to/web-standards/meet-the-w3c-tag.

… Hope that we can get the budget from us if possible. Unfortunately, I’m OOO next week. Ehsan has volunteered to take over while I’m away. Will give him the admin for the ticket site. Catering is in progress.

… Couple of questions on organization. We said we expect 70 people, which is a little more than in Hong Kong, as we expect more developers in London. Maximum attendance is 120. Will keep them updated as we sell the tickets.

… Asked for a low stage. I will gave a little presentation (on the sponsorship of the venue), then go into discussion. They ask if we want lowstools or comfy bar chairs, prefer the latter? (Agreement.) We will get some mics. Need to tell them how many chairs, assume 8?

Jeffrey: I would guess 11. I expect Marcos is not joining in person?

Brian (via chat): Would also prefer not to be on the stage.

Matthew: We have a strong anti-competitive device policy, which should only be applied to Samsung employees. Not sure if they extend it to other people, but I ask you not to use devices obviously. If I need help with a top-up, I will keep you updated.

Lola: Thank you, Matthew, for the hard work on this.

Matthew: It was actually fun!

Brian: Do we already have dates and locations for following F2Fs?

(No.)

Brian: Would like to suggest WebEnginesHackfest week in Spain, already have a big space, and it’s a developer meetup. So we could arrange a special event. It is like ”TPAC2“! Happens early June. Happy to offer that.

Jeffrey: Last year, we only did two F2Fs, one in Europe, one in Asia. But it’s good to have a venue and an invitation.

… We also cancel our videos the week after a F2F, should we also do this this time around?

(Agreement.)

#### Agenda planning

Jeffrey: Several years ago, there was this big spreadsheet of all the issues that were open, and then they split it up into sub-breakouts.

… Starting about two F2Fs ago, we focused on larger issues, and presented a larger question in one session, and then broke out into smaller sessions to talk about it, and then came back together.

… Do we want to do this now or asynchronously on GitHub? We don’t have to agree on it now.

Lola: Feel like we have fewer open issues this year than we did have in September or this time last year, and also fewer issues that require significant discussion. Hadley suggested spending more time on writing documents, to publish some, or make significant progress.

Yves: We recently discussed to work on F2F which topics would mandate a finding, open-ended discussion what would be an interesting subject, and to publish more of those.

Jeffrey: We also have a couple of new members that they may want to do certain efforts during their term.

… We will continue to talk about that over the next couple of weeks, and the chairs will come up with a draft agenda.

Lola: Can you come up with a spreadsheet?

Jeffrey: Will do.

Lola: And then folks can populate it.

Jeffrey: Will also post the catering menu from the Google office, so people can comment what I should order.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Jeffrey: This is about making the Reviews CG happen. There is a draft by Matthew and Martin: https://github.com/w3ctag/abcde

Matthew: 99% Martin! There is a few suggestions you posted, Jeffrey. I think it makes sense to open the repository, or close the issues before that.

… One of the points you made is about the name of it. We want to treat this as a high-priority one before we socialize it (https://github.com/w3ctag/abcde/pull/5).

Jeffrey: There are three PRs open. Should we go through them and then make it public?

Matthew: At the moment everyone in TAG can see it?

Jeffrey: Yes.

Matthew: But people probably didn’t have time to check them. Want us to go through them now?

Jeffrey: We can at least have a look.

#### https://github.com/w3ctag/abcde/pull/5

Jeffrey: Suggested that ABCDE is not a great name for the group, and we should call it “Design Reviews CG.”

Matthew: ABCDE is for Architectural Basics, Consistant Design and Ethical Review.

Lola: Agree the abbreviation is not really helpful, and if you expand it, it says more than "Design Reviews."

… Sometimes people are surprised that there’s and ethical component to it. Not married to the name.

Matthew: Love the acronym, think it’s very elegant. Think it’s very clear if you expand it, but will be abbreviated most of the time. Expanding ABCDE tells people what to do.

Brian: We can do both? "aka ABCDE" To newcomers, may be more accessible. Better name to not do that.

Jeffrey: Where is the group leaning?

Matthew: If we can make ABCDE prominent in the document, that would be cool. But agree we should make it accessible. Lovely third way.

Jeffrey: Architectural & Ethical Design Review CG could be another option. Do folks have a preference?

Yves: If it is public, it makes sense to be more explicit about what it’s doing.

Matthew: Architectural Design Review would make more sense. Don’t think we want to change the entire horizontal review process.

Jeffrey: Then I suggest Architectural Design review. Will update my PR.

#### https://github.com/w3ctag/abcde/pull/6

Jeffrey: This is a detail. Made a list of what the group should define. If the chairs of the CG notice that people don’t do good reviews, they may just not assign reviews to those people. Mitigates the risk that people join that group on purpose, so chairs can act against that.

Lola: Assume one of TAG members is chairing?

Jeffrey: Yes.

Lola: What if people don’t know they are doing bad reviews? Or are targeted to be not helpful in doing that?

Jeffrey: We can talk to them about it. If someone feels targeted, people can go to the team. CGs are not required to operate by consensus, and single people trying to undermine reviews can easily be stopped in doing so.

… Fine to merge?

(Agreed.)

#### https://github.com/w3ctag/abcde/pull/7

Jeffrey: Next one is Matthew’s addition of the accessibility screener, which looks fine to me. Ok to merge?

(No objections, merged.)

Jeffrey: Will then update my PR. Any objections to make the ABCDE repository public after that? It’s just the charter, then we need to socialize it.

(No objections.)

### Breakout Rollup

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

### AOB

Matthew: DST changes?

Jeffrey: Meeting times are a mess, three DST changes in March. Will switch in March, and it will be problematic for a couple of weeks.

Brian: What is the process for selecting reviewers?

Jeffrey: When issues come in, we have the issue triage link (https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29). Anyone interested in reviewing a proposal assigns themselves.

… In theory, if nobody steps up to review a proposal, we would close it. In practice, this never happens. Believe we don’t decline things as often as we should.

Lola: But we do it, for example, if designs don’t have enough buy-in, is outside of our area of expertise. So we do decline some things.

Brian: Communication channels?

Jeffrey: Mostly Slack, we also have www-tag@ (public) and tag@ but rarely use them.

Lola: We expect people to attend two breakouts a week plus the plenary that happens every other week. Not sure about your time zone. Please enter your availability in the time zone document (https://cryptpad.w3ctag.org/code/#/2/code/edit/z8mqupjDY-jNRfco0d8Gw9Zg/). If you are in North America, you can obviously only do one. If the schedule would change, we would expect you to do the two, though.

Brian: What’s the process on the CG? Sounds like everybody can do that? Can you give me more context?

Matthew: We have a huge volume of design reviews on our plate, and don’t always have the right expertise. In many cases, the WG requesting review would be the expert.

… CG is modeled a bit on the way the IETF works, where work is spread across more people. Nobody says that the TAG design review process would change though, so the group could provide additional input for example.

Brian: In the US, we have certain stamps that consumers trust. Review process could be like a long list of check boxes, similar to Chromium launch process, where there’s security reviews, etc.

Matthew: Great questions! Think we’re going to find out. Think we could try and find people to do that kind of thing.

Jeffrey: There were various proposals, current charter is leaning towards picking a person twice a year or so. Goal would be to find "a reviewer." But if there’s more interest, I’m sure we can produce an output that matches that kind of input. At least initially, would not push for a Blink process change.

Dan: Would this replace the Associates program? Would all Associates join the CG? Something in between?

Jeffrey: Think we don’t know yet. This idea came out of us asking how did the Associates program go. Think most people thought it went well, but Martin thought it could be better. Think there’s space for both. Associates is a picked group of people, CG would not be invited to TAG people. Associates could also work on Findings.

Lola: From my understanding, one of the points of the Associates program is people get a feel of how TAG is, and if they like it, they can run. That’s not necessarily the goal if you are in the CG.

Jeffrey: Believe Martin thought the CG would also help people to qualify for TAG:

Brian: Like the Associates program a lot. A lot of times, super-qualified people don't get elected because they are not well-known. Can imagine companies to pay for an Associate to do things, maybe less for the CG.

Jeffrey: It’s not going away, we are trying the CG in addition.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-02-12](https://www.timeanddate.com/worldclock/converter.html?iso=20260212T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Yves, Christian, Xiaocheng, Marcos, Ehsan

Regrets: Hadley, Yu, Sarven

Scribe: Christian

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) - @csarven, @lolaodelola

Lola: We should close this now, mainly because this came up during the Paris F2F. I’m not quite sure why we need this any more, so suggest closing.

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

(Skipped.)

### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel

Christian: Marcos mentioned this has the same issue as PromptAPI, you can query if there is a model present on the device suitable for a certain level/language, this could be a fingerprint vector. I want to reccomend they look at Prompt API review.

Ehsan: Isn't this the same problem with all language based models? Maybe we can have a consistent answer.

Lola: Do you suggest we should have a document on language-based models?

Ehsan: That would be my suggestion. Come up with a document that describes all of that. Should be done at the WebML groups. Think this is coming up more often.

Marcos: It’s a more general problem of downloading system components which then you can query, because then they become global.

Lola: To make this even more general, should we have a position on downloading system components? Or is this restricted to this use case?

Marcos: No, could be related to everything. Codecs, etc. Should be a design principle.

Lola: Who would be willing to write that? We also have another plenary before the F2F.

Christian: Could offer to do that, would be my first design principle, and a topic where I’m interested in.

Ehsan: Same here. Would be good to have a more experienced TAG member on that as well.

Lola: Design principles is owned by Jeffrey, so we can talk to him about that.

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

Matthew: My view is, Martin makes a good point, will come up with a PR to clarify that the ambiguity is on purpose.

### [design-reviews#1188: Other Spec Review: Scoped View Transitions](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1188) ([Github](https://github.com/w3ctag/design-reviews/issues/1188)) - @matatk, @xiaochengh

Xiaocheng: Extension to the existing view transitions. They are for the entire document, this is an extension that allows transitioning just a subtree. Overall motivation is reasonable. Weak part is in the explainer, where they didn’t talk much about alternatives. I’d like to ask the question how developers would to about the existing technologies, and if they considered alternative ways to introduce scoping, e.g. shadow DOM scoping?

Lola: You will post a comment asking about the alternatives considered?

Matthew: Big +1 to what Xiaocheng said, haven’t looked into enough detail. When the content is available in the DOM would have impact on assistive technologies. Know we had extensive discussions about that last time. This is my main concern, and there may be a similar one regarding animations, it would be cool if UAs provided an option to ignore them. I will read the proposal before officially commenting.

Lola: Ok, will ask you a follow-up question in Slack re animation ignoring.

Xiaocheng: Should I include Matthew’s question in the comment?

Matthew: No, because they may have answered that. Want to check by the end of the week.

### [design-reviews#1187: [wg/das] Devices and Sensors Working Group 2026 Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187) ([Github](https://github.com/w3ctag/design-reviews/issues/1187)) - @marcoscaceres, @christianliebel

Christian: We have consensus on our comment. Need input from the wider group on the comment - it may be contraversial.

Marcos: It also has to go out today (the 12th, US East Coast time)

Lola: Still need additional review?

Christian: We had a good discussion and we feel the comment is balanced. Will post it right after this meeting.

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh

Matthew: We last posted August last year, where we concerned. Need to catch up with that this week.

Lola: Will also have a look at the comment. Has it shipped?

Matthew: I don’t know. Will have another look.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: We weren’t sure what to do with this, keep it open, satisifed with concerns, or we would want other engines to implement it. This is in the draft comment, which is there to be reviewed.

Lola: So you need a couple of people to have a look at the draft comment?

Matthew: Yes, and we didn’t quite reach consensus yet on what to do next (explained in the private comment).

Lola: If folks could have a look that would be good. Do you mind posting a request for more eyes on your comment in Slack, please?

Matthew: Yes.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel

Christian: We were looking for Tess' input - wasn't able to reach her, so took a look. I would suggest Xiaocheng take a look as it feels similar to view transitions. It wants to defer page swapping to a later point in time in order to avoid flickering, and animations stopping when the headers of the new page come in.

... Two solutions proposed; imperative - very complex, but intended to gather feedback, according to the proponents.

... The other is a one-liner in CSS which would be rolled out later.

... Martin was concerned, channelling Tess, that this would slow down navigations.

... I'm concerned about the complexity of it too. But looking for more expert opinion.

Lola: Did you read the [minutes from their meeting at TPAC]{https://www.w3.org/2025/11/11-whatwg-minutes.html#fb7a}? Seems short, but maybe helpful.

... Maybe if we can't get through to Tess, we could speak to Anne.

Christian: Skimming the WHATWG minutes, it looks like they had similar questions. Explainer is still not properly formatted. I'll talk to Anne and come back here.

Lola: Can ask them about the things that we need to understand better.

Christian: May I have Xiaocheng's support on that?

Xiaocheng: Will add myself to the issue and come back.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Ehsan: Finished my review, will post it very soon. My main concern is that I see this as a stepping stone for more Agentic-related specs coming. I don't see any position from other stakeholders on this one. Because it seems like a stepping stone, I think we need to push for a clear position from other stakeholders first (Mozilla and WebKit).

Lola: We look forward to your draft comment.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Matthew: Think I know what we’re doing with this, but the discussion isn’t in the TAG bot. Two of us were in agreement that this is a step forward. APA thinks this doesn’t make it any worse, and it does some really good stuff as well. There’s an a11y section coming from APA that is in the works. Propose a closing comment along those lines. Correct, Xiaocheng?

Xiaocheng: Yes.

Lola: If TAG bot is dropping comments, let us know in Slack.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Don’t think I received a reply to my email yet. Will try pinging Patrick on Slack and make sure it didn’t go to spam. Will do that this week and come back based on the outcome of that. Probably a comment that we don’t have consensus. Marcos was concerned that this would go out of charter. We should contact PLH that we are concerned about that.

### Issue Triage

### [design-reviews#1192: Incubation: speculation rules form_submission field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @matatk, @xiaochengh

Xiaocheng to take a look.
