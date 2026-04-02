# TAG minutes, week of 30 March 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/03-30-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20260401T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Brian, Heather, Jeffrey, Marcos, Dan, Xiaocheng
    
Regrets:
    
Scribe: Heather

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu
### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu
### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu
### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu



### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Jeffrey: Sent them a comment; they've sent a reply. I need to look at that.

Dan: I am a co-author so I'm biased. Kurt had agreed that fetching is fine; they avoided it in the first place because there's an intermediate step that might cause a fetch arrive at the wrong time. Ordering needs to be maintained. Maybe a placeholder style sheet? But it's probably weirder not to do the fetch at all. Currently, the ccs style sheet object only gets created after the fetch arrives, but we can probably change that with minimal impact. Experimenting in Blink suggests this is doable.  The other question is attribute vs link; not sure if there's a hard opinion on this one way or the other. Dan and Kurt are leaning towards the attribute. A declarative approach would have to use links that would be left around after. 

Jeffrey: That all makes sense, though I'm still nervous about it. Having the ability to have a link seems to be the metric the way other style sheets work, but I haven't investigated this deeply. The attribute definitely makes sense as a shorthand, even if links are available. 

Brian: I looked at the replies the other day, but there have been more since then I haven't had a chance to think about. The trouble I have is that I've observed this from the start and I keep losing state and having to re-learn the topic. 

Jeffrey: So, wait until you come up with a comment?

Brian: If you feel you have a good answer, I'm willing to accept that. I don't think I'll ever love this as a feature. 

Marcos: I only know this thing you're describing as a user, not in any technical detail. But I'd be happy to review if that would be helpful.

Jeffrey: We have the technical detail in Dan. We're trying to make sure this works for more naive developers; getting that perspective from Marcos will be helpful. Brian, I think you're finding this difficult because of the difference between adopted style sheets and [???]

Brian: Yes. I'm not sure it fully handles all the problems it needs to.

Dan: It's been a long road trying to find something that works well enough for everyone.

Jeffrey: Sounds like we should take another week and discuss on Slack if any questions come up.

### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1134) ([Github](https://github.com/w3ctag/design-reviews/issues/1134)) - @jyasskin, @dandclark

Dan: Left a comment before a few minutes before this call. They have offered more information as to why they made the choices they made; would like to see them put that in the explainer. Still don't love the complexity, but I don't see enough reason to go back and change an earlier satisfied resolution.

Jeffrey: I'm not entirely convinced by the use cases the processing instructions enable. I don't know that we need to argue this further, though.

Dan: Can we go back and suggest they update the explainer?

Jeffrey: Yes. Dan, will you post?

Dan: yes.

Jeffrey: OK to just post; we don't need to go through brainstorming

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Marcos: Similiar concerns that I raised with the DAS specs. This feels very foot-gunny. There isn't enough context to make these adjustments. The challenge for this spec would be to prove you can do this that is not foot-gunny when all other previous attempts have not ended well or proven useful. 

Jeffrey: Can you be more specific about how the developer will shoot themselves in the foot?

Marcos: It makes an assumption about my CPU but in 5 years, those assumptions won't be valid. The developer will degrade the user experience based on information that doesn't apply.

Jeffrey: They have addressed that part. The buckets have a stable meaning; bucket 4 will always mean the same thing, but in five years there may be 8 or more buckets. 

Marcos: Do I make a determination about performance over time? If it's point in time, I could be runing a video or AI job that will skew the numbers.

Jeffrey: Sounds like we should wait for a week and you'll post your comments.

Marcos: OK.

Brian: The scaling factor they have in here is going to be tricky because it's allocation specific. So, the tiers don't have specific meaning and they can't over time. Seems very impossible to have this develop well over time. Is there any prior art that does this well?

Jeffrey: In simpler cases, yes: memory buckets. But that's simpler than GPU/CPU performance. The definition cannot be implementation defined; websites can't guess what the implementation has decided. We might be able to say we have consensus that they need to make the buckets not implementation defined and come back to us with a definition of the buckets. That might make the review easier.

Brian: I don't know if that's my take. I don't see how these can have arbitrary meaning that is left entirely to implementations, that will change over time, and developers are just supposed to make good decisions that will evolve over time. 

Jeffrey: It is not supposed to change over time. This machine is in bucket N forever. 

Brian: This machine is, but the scale is not. When you get to "unknown", will that be because it's too old or too new? I can't imagine how you do this. The message I want to send is more than "define this". 

Jeffrey: How about we post: "We haven't finished discussing this, but one thing we're skeptical about is the idea of leaving the buckets implementation-defined. Can you give us a rough algorithm that might be interoperable?"

### [design-reviews#1196: [wg/webperf] Web Performance Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1196) ([Github](https://github.com/w3ctag/design-reviews/issues/1196)) - @jyasskin, @marcoscaceres

Jeffrey: Marcos posted some comments. We should review and see what we agree on. The expressions of interest is from the charter template. We should probably keep iterating on the template, but let this charter proceed with this in the charter.

Marcos: WebKit people are very concerned; I've raised those concerns indepently of the TAG. The other things are fairly small. The frustration they are having is they haven't worked out a process on how they handle their own changes. Their consequence of their proposed changes here is that they want to put stuff into a spec to incubate it rather than tightening up the working group process to make sure things are being properly implemented. 

Jeffrey: I've also been talking to Yoav about the process questions, which are not TAG questions. Am worried about the single engine bit, but we can probably come up with something. Should I draft a comment to discuss? 

Marcos: Yes, that would be great.

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @xiaochengh

Xiaochengh: haven't had a chance to look at their reply yet. Will review by the Eurasia breakout.

### [design-reviews#1194: WG New Spec: HDR on the web (CSS, Canvas, WebGL, WebGPU)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1194) ([Github](https://github.com/w3ctag/design-reviews/issues/1194)) - @jyasskin, @xiaochengh

Jeffrey: I posted a comment to private brainstorming; they are addressing HDR in a coherent way, which is what we'd asked for in the past. I'm not an expert in the area, though. They have asked a question about how to express headroom. HDR is the idea of being able to show a color brighter than white. Most CSS colors operate in linear space. Camera shutters and image specs operate in the log 2 of that. They seem to be saying that when they do linear things, they will put linear in the name. They aren't clear if they don't have linear if that means it will always be log 2. We should suggest put either linear or log2 in the name to avoid confusion. I do have one worry about whether they need a more complicated CSS thing to match CSS colors with image colors. 

Marcos: I've only dealt with this a tiny bit when discussing a brightness lock. 

Jeffrey: This is a very detailed space, and Chris's the intro explanation in a bunch of forums was great. If there are no other thoughts, I'll draft a comment and check in with people this week.

### [design-reviews#1193: Other Spec Review: The revert-rule keyword](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1193) ([Github](https://github.com/w3ctag/design-reviews/issues/1193)) - @xiaochengh

Xiaochengh: Minor comment regarding the explainer - they don't have an alternatives considered section. They have a filter extension section that is a mix of alternatives and the actual filter extentions. The proposal looks fine overall except a concern about implementation complexity. With revert, we need to maintain every rule from each origin, and then each layer. We can't drop anything. 

Jeffrey: That sounds like a good thing to flag.

Xiaochengh: It does sound like someone has implemented it, though, so I'm not sure how they did it.

Jeffrey: They have, but they haven't filed any positions yet. 

Xiaochengh: It's already in the CSS 5, but those editors may add things before they are implementable. 

Brian: These are from whether its implementable or not.

Jeffrey: It's from the Chrome team, but the other engines may have different architectures.

Dan: The other engines have file positions, just haven't shared with us.

Jeffrey: So it may not be worth us asking again. 

Xiaochengh: If others are not concerned, then we can resolve and say it's good. Will send that comment.

Brian: You can say that broadly speaking it seems ok, but of course browser architectures will vary. So, subject to reality, there may be other constraints that make this more difficult/costly to do in some engines than others.

Jeffrey: And your comment that they're missing alternatives is worth keeping.

### DAS Chartering discussion

Jeffrey: Marcos and I have been going back and forth on this one. We need consensus on what we want to say.

Marcos: At the bottom of the design review, there is a summary of everything. <https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187>. 

Jeffrey: There's also the PR <https://github.com/w3c/charter-drafts/pull/784>

Marcos: Reminder that they are on a tight timeline. There can only be two charter renewals; if they don't do a point-by-point response, the W3C has made clear that they'll be done. 

Brian: It looks like 770 was merged by Reilly?

Marcos: It became overwhelming. I will create new issues. Would appreciate if people could look at the proposed changes and whether they address TAG's concerns. Note we have the making of a process here for handling this level of contention. We need to be clear on whether issues must remain open until we have consensus. We need to be clear as to when and where an individual drafts responses before TAG approves it. Given the question came up "who is Marcos speaking for", we should be ready to resolve that. Part of the process needs to be how we engage with the working group. The human dimension is missing. 

Jeffrey: I'll iterate on Slack, but we should also bring it to the Eurasia breakout. 

## Atlantic Breakout (America / Europe) - [2026-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20260401T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Brian, Dan, Yves, Matthew, Jeffrey, Mike, Christian.

Scribe: Matthew

### [explainer-explainer#34: Structure alternatives as: Alternative → Pros → Cons → Reason for rejection.](https://github.com/w3ctag/explainer-explainer/issues/34) - @jyasskin, @matatk

Matthew: Haven't done this yet, but promise to get to it soon.

Jeffrey: Think this is on my list, but I also haven't done it.

Brian: Thinking back to the first/an early Explainer I read... Service Workers. It was very readable. It gets hard to keep them up to date over time. We want to keep them up to date, but coming to them afresh... it can be overwhelming to re-open a 6,000 word document, because of the sheer amount. Service Workers is an incredibly complex feature, but the Explainer was really small, and wouldn't seem apt today, but it's really good. Should we give other advice about making it more easily consumed... breaking off historical parts, or maybe using summary details to focus the main parts or something?  Am I the only one who feels this way?

Lola: No you're not the only one who feels this way. We recently had a big discussion on GitHub outside of this group about the lifecycle of the Explainer and the difficulties it introduces in some cases, and the pros and cons of having the Explainer be included in one way or another into the spec, so you konw it's up to date.

Jeffrey: The issue is https://github.com/w3ctag/explainer-explainer/issues/19 "Explainers are an anti-pattern" from Manu

Lola: We agreed at the time that people who submit design reviews can do either/or - we need to have the info that the Explainer says, which can be in the spec, or in a seprate document. I think there are a lot of times when it makes snes for it to be a separate document. You just raised concerns about the lifecycle and having key parts in the spec helps with that.

Matthew: +1 to Lola. And we've been thinking of ways to make maintaince easier, e.g. moving things from explainer to spec but having explainer near spec allows us to review things that may not be suitable for spec. We've had feedback on this, which was about readability and accessibility and making these docs more inclusive to people who aren't used to reading such technical docs. Your comments are in line with the feedback. A member of our team is also trying to work on this.

Jeffrey: I think it's somethign we always need to be thinking about, but we'll never get it perfect, or easy. It's hard to write a doc that explains a new technology to new audiences. There will always be challengs. It will take effort and experienced people to figure out what to do. We shouldn't expect to be perfect, but patches welcome.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Matt will update next week

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Jeffrey: I saw glimmers of discusion from last week. Brian had questions about what the document is for. Wanted to make a chance to answer that, or redirect.

Lola: Any outstanding questions about its purpose?

Brian: Marcos and I met last week, opened issues 47 and 48. I think this is trying to serve mulitple purposes. One is to replace the WHATWG UA definition. That's what it says in the README, though I think it's trying to do more than that. A key thing: how would we achieve that in the first place?

Lola: We should track issues 47 and 48.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

*bump*

### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Brian: Discussed in last breakout.

Jeffrey: There's still worries that the attribute might not be enough in the long run, but it's a reasonable thing to start with. It avoids a proliferation of link tags. It avoids inconsistencies with the way that ____ works witht the adopted style sheet lists, particularly as the DOM is mutated. What they're proposing is a good first step. Debating whether I should propose 'satisfied' or 'satisfied with concerns' - this design is basically right, so leaning to 'satisfied'

Lola: What would be the concern if it was 'satisfied with concerns'?

Jeffrey: The attribute doesn't allow you to configure all of the things that the `<link>` element allows you to configure, and doesn't improve consistency across the platform as much as it could.

Brian: There's a lot of history, decisions, conversations to go back over. I would need some time in order to comment. I'm OK with the group's view. I don't think any solution is going to really make me love this feature. We're probably teetering on how good it's going to get.

Lola: This doesn't sound like 'satsified' to me.

Jeffrey: We're not completely clear on what we mean by 'satisfied with concerns' - how many concerns it implies. The history of this whole space is messy; been under development for a long time. The things that shipped initially may have been done differently with what we know now, but no feature has the benefit of hindsight. I lean to 'satisfied' even though it's not perfect.

Lola: I'm happy with group view, but would like you to include the concern in the comment, regardless as to label.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Lola: I'd like to follow this.

Brian: Is it OK if we review this, because I think this is not hard to get your head around. I'd appreciate Mike's input on this one. This started with the deprecation (attempt) of XSLT by Chrome in WHATNOT. All of the engines agreed that they'd like to get rid of it. It is problematic. Someone opened a thing suggesting W3C should obsolete XSLT. Then there's the question of lots and lots of other things that that opens. Then Danbri wrote in and suggested that we have difficulty defining this because there's a long tail of other stuff that's valid, and reliant on things like RDF triples and semantic web ideas, even if not done in RDF, and there are semantic things that are used outside of the browser. We need to come to how we reason about them.

... Relevant to my interest in the UA Finding, and the current CRA standards that are being built that talk about different kinds of user agent, and what has to be supported. The question is how do we do that, and what would we do? Yves and I spoke a bit about this last week. We condensed it into a tiny space that I think fits nicely.

... The MiniApps and other WGs are coalescing with WebViews. The concept of 'Embedded Web' is emerging. Can we paint some advice around this?

Lola: Sarven, Yves, and I also discussed this a little bit in a round-about way last week. It'd be good to hear how others want to respond to Brian's comments. I have a question: Jeffrey: you are working on the Web Platform Architecture doc.

Jeffrey: Aspirational, but yes.

Lola: How does that fit in to this? And the UAs Finding. Is there space to define this in that Web Architecture document?

Jeffrey: Yes. This touches on a question that [Dan Appelquist posted](https://www.torgo.com/blog/2026/03/yes-but-is-it-the-web.html) recently - 'what is the web?' There are 3 categories:
    
 * The web (linked resources)
 * Web browsers (UAs for visiting a subset of those resources)
 * Web technologies (HTML, CSS, JS, XML, ...) which are used to build those resources but they can also be used in other non-linked areas
    
We should probably write this down.

Brian: I think that document is going to be hard to write already.

Jeffrey: Maybe start with a Finding. Or individual findings on the sub-pieces.

Brian: +1

Lola: Do we want to start breaking this down into what Findings we'd need.

Jeffrey: This issue may be a reaosnable base for a Finding. We don't need to figure out the architecture of the architecture before we start this.

Brian: There are interesting related questions around security. XSLT has a lot of nice characteristics for offline. Putting it in the browser brings characteristics that may be negative.

Jeffrey: The XSLT security issues were totally solvable. But it didn't have the adoption to justify that.

Brian: But it wasn't done.

Jeffrey: It was put in when a C implementation was reasonable. But not enough adoption to justify moving on. Nor to justify implementing versions 2 and 3 in the browser.

Brian: There is some debate over this; a Finding could help.

Jeffrey: We should split this Finding from detailed questions of XSLT. E.g. there was no reason to deprecate versions 2 and 3.

Brian: It helps to have a thing that helps you to ask questions.

Jeffrey: There's a lot of XML formats that are not browsable in web browsers, but are perhaps part of the Web. XML is based on something that came out of the Web, so they're the Web technologies category.

Yves: There's a difference between the web platform, which is everything browser-related, and the web, which is everything linked. A browser can't process everything that is linked, or has linking capabilities. That's the crux of the definition. I think there's something like that in The Architecutre of the Web.

Mike: Would Atom be one of those?

Jeffrey: Yes in my opinion.

Lola: Next steps on this? We're going to write a preliminary Finding based on this issue here?

Brian: I'll continue to work on it.

Lola: If you want to discuss things in these meetings, keep the agenda label.

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Sarven: Noted Matthew's and Jeffrey's comments after my draft. I'll try to re-capture / draft the (new) concerns or things that need a clarification.

Jeffrey: I wanted to ask for our sense of how much to push on this. 1.2, at least Turtle and N-Triple formats are backwards-incompatible (they add new grammar that older parsers won't understand). The behaviour when finding unkown things is undefined. My impression from Sarven is that parsers vary. The WG has a statement in 1.2 that says parsers reject new syntax, but I'm not sure how correct it is. If they reject new syntax, that's like CSS. But in an RDF context, maybe that's the wrong behavior. The WG has not addressed these questions - they have simply said it's not a problem.

Lola: They've not said why?

Jeffrey: Pretty much; they've not discussed it with us. So do we trust them, or do we push on this?

Matthew: It's such a low-level technology, concerned about the ramifications. If it's not a problem, can't they convince us? Parroting Martin's concern about how changeable the parsers are in the wild.

Lola: Agree, also concerned. Could we invite them to a plenary?

Christian: +1. We have the same thing when we discussed the new PNG adjustments. The new formats there, and we had the exact same concerns. We should apply the same logic. Ask them to make sure this transition can work.

Lola: I can't make the next plenary but can someone invite them?

Jeffrey: Yes, I can.

### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

Lola: Ehsan to write a comment for their GitHub. He did. Heather +1'd it. I'll do the same and then it can be posted.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: Had a lot of discussion about this. I'm working on a revised comment, but I wanted to check a couple of things. Want to ensure I'm capturing Brian's feedback. 2 things: (1) Behavior in relation to covering shadow roots or not. Historic discussion resolved on it being opt-out of affecting shadow roots. Seems to have stuck. You commented that it should be opt-in. Want to clarify. True, and how strongly do you feel?

Brian: No memory of any of that.

Matthew: It seemed important a couple weeks ago. Was hard to follow with the historical decisions. You also mentioned (2) ... I mentioned modifier keys. Don't think they addressed it in the explainers. But a more general version: you talked about systems where people can switch to spatial navigation (perhaps using D-pads), and that's not covered. I agree and happy to raise that. Will suggest that spatial vs linear navigation be addressed int he explainer. When would you see people navigating with a D-pad? E.g. TV and they only have a remote? Or as assistive technology?

Brian: Could be any of those. Can make arrow keys work. I'll note that in the very recent past, around the time of this discussion. Jihye Hong who worked at Igalia and worked on spatial navigation before that. She commented. Can find the link. It's already been brought up by others.

Matthew: We should reference that. I'm incorporating some other things that I don't need to ask about today.

Brian: It is on the WHATWG HTML issue https://github.com/whatwg/html/issues/11641#issuecomment-4028039082

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

skip

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Lola: Thought we decided this was satisfied. But Dan put in a comment, which could be useful. Our concern was about the level of support in other browsers. Seems good to me. I'll write a closing comment.

Matthew: Other engines haven't responded.

Lola: In Slack, Jeffrey mentioned that Moz+Webkit usually participate in CSS, so they'd often object there if they have concerns.

### [DAS Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187)

Jeffrey: Marcos, Christian, and I came up with a position on the charter. However I think this needs more discussion before we can say if we have TAG consensus. Would like more eyes on it.

Christion: Happy to help. I have a call with Marcos before the Eurasia breakout, which is the right place to discuss.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-04-02](https://www.timeanddate.com/worldclock/converter.html?iso=20260402T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Prsent: Christian, Lola, Matthew, Marcos, Yves, Ehsan, Xiaocheng

Scribe: Matthew

### DAS Chartering discussion
Long thread at https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187. Marcos has a charter PR at https://github.com/w3c/charter-drafts/pull/784. Need to figure out how to distinguish TAG consensus from individual thoughts.

Lola: Discussion with Marcos, Christian, Yves, on Slack. What needs to be discussed in this call?

Marcos: We raised 'satisfied wtih concerns' re the DAS charter. Sent to WG. Been waiting for WG to address them. There hasn't been much movement on this. Jeffrey and I jumped in with suggestions as to how to address their concerns.  The TAG doesn't have a process to handle when we have disputes. We can engage with the WG, but some of it was TAG feedback and some is what would be considred wide review feedback. We were both giving contradictory feedback. So, when is the TAG vs W3C member speaking? We identified a process problem: when we have disagreement, what is the TAG's position? The interpretation of the concerns we had listed differed in our minds.

...We came up with a model where we deputise someone to speak on behalf of the TAG so we don't conflict. We should clarify the process. I proposed a deputising process on Slack, discussed with Christian. The idea is that when we publish a potentially contentious position, we deputise an individual to speak on behalf of the TAG, and have them speak with the group. This allows us to have a single voice through the TAG. Rules on how we get consensus were proposed, and who's entrusted to take actions.

Lola: Sounds like there are 2 things going on. 1 is disagreement on the DAS charter (you and Jeffrey). The other is the deputy process. I think next week's plenary is the best place to tlak about this.

Matthew: (can't we just _____)

Lola: (check thread - confusing as to who's speaking as what - helps everyone to have a TAG voice)

Marcos: We had consensus on the concerns, but not how to address them.

Christian: I'm happy to serve as that deputy here. Want to build consensus. Charter comment deadline is soon.

Marcos: Yves may have more input on this. The process is a group can only be extended twice, and then it has to go to the AC.

Yves: Will check.

Lola: Thanks Marcos & Christian for that explanation. Jeffrey mentioned this was added to this agenda so we could talk about the points where Marcos and Jeffrey are not in alignment. Shall we do that?

Marcos: The point of disagreement is essentially: there's a set of specs that are single-implementer specs. We proposed that, at a minimum, there would be a prominent developer-friendly notice to warn developers about this (that it is blocked getting to CR) and the reasons why. The 'reasons why' part is where we disagree (that that is necessary). Jeffrey and I disagree on this. Christian may be able to represent what web developers want to see there. And from there the whole TAG can weigh in.

...I had a go at this - sending 11 PRs, all of which were rejected. Would be nice to have a discussion about them. Going back to the process: TAG could've discussed internally and formulated the text, before sending it as a draft representing TAG's thoughts.

Lola: I see also in Slack you've put an updated comment for that warning. Has Jeffrey seen this?

Marcos: Unsure.

Christian: Best that Jeffrey looks at those and comments, especially if I'm to be the deputy. I think we have a little longer than 2 weeks.

Lola: Let's discuss at plenary.

Marcos: This is where conflics of interest come in - conflicted people shouldn't be deputies. Some people are talking from the perspective of an implementer (the implementer in this case). We should have a process to ensure that a deputy is not too conflicted. It is good to have the conflict overall, as there are real perspectives, but the deputy shouldn't be conflicted.

...We had an exercise where we each submitted our suggestions about this text together, and identified what may have consensus. We collect what everyone wants; compare; and then find a solution.

Yves: There's a value in declaring that we don't have consensus. If so, we let the WG decide what to do. Ultimately it's the AC that decides.

Christian: I agree, e.g. we had a review on the Prompt API that had no consensus. In this case I think we can come to consensus and I would like to build it.

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: Open for a long time. This is a way to migrate a PWA from one same-site origin to another. However, it's not really webby, and there's the open question of the manifest's ID, which needs to be resolved in the WG. So I suggest 'validated' or 'ambivolent' - I can't say with even 80% certainty that this should be the way that PWAs should be installed or migrated on the web platform. I can't commit to that. I am OK with 'validated' becuase it works, but not sure if we have consensus. I don't expect our opinion to change from 'ambivolent' though.

Yves: The approach seems to be backwards - the redirect is from the new one to the old one. The example is combeining 2 applications in to 1 that does what both of them did. I think there's an issue in the way that they presented it. I still think over-using well-known URL for this is non-webby, and should be done a different way (<link> headers, other manifiest ideas, ...). I agree that we shouldn't close it as satisfied (even with concerns). There are more things that need to be worked on before it's a spec. I'm looking into it more.

Lola: I wonder if it's worth, after you've looked into it, if we should indicate those issues/work that needs doing.

Yves: We should be open about the use case being useful but the current solution is not what we'd like.

Christian: Will draft a closing comment.

Lola: With 'unsatisfied'

Yves: But note that the use case is valid, but it needs more work.

Chrstian: Is 'unsatisifed' too strong?

Lola: Use case is good, but implementation seems not to be. We can discuss.

### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel

Christian: We feel this will be satisfied with concerns. We asked them to add fingerprintabiltiy information, but this was ignored. They said it's been covered already, but adding the quality dimension adds a lot of fingerprinting vector.

Marcos: We can see the problem again where we're closing issues but then have no mechanism to follow up - e.g. Christian said it would be nice to see certain things. Maybe we should file bugs relating to those concerns? Then they can't avoid the feedback we give them.

Lola: We've spoken about this in relation to other issues.

Matt: We have process for what you just described Marcos. We can see in one place when groups have closed issues, if they've addressed resolutions, etc. We have it and we could use it.

Christian: Should we try out that process here?

Matt: I'm working on guidance for how to do this, I'm happt to take that and make it applicable for TAG but docs are needed. Happy to take it on and work with chairs.

Lola: Let's write the closing comment for this, and then figure out with chairs, Matthew, and anyone else, how to track things.

Christian: Let me know on the proosed comment.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew to write comment

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

Matthew to make PR

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

*bump*

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

Christian: We are collecting concerns at the moment.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh

Xioacheng: This is a new version of a previous proposal. I am very interested, but at the same time I think it needs a lot of work. First concern: privacy. We raised privacy concerns previously. What kind of data an be drawn into a canvas. In the current explainer they listed a range of things they considered. They also listed things they can't consider regarding privacy, like scrollbars etc.

...I am concerned they're not doing enough. I'm wondering if they have higher-level criteria for judging what's sensitive and what is not. The list is incomplete - we may find later that things should've been considered privacy-sensitive.

...the paint event is a new event. The idea is whenever the rendering of a child of the canvas changes, a paint event is triggered. Then the listener can update the image in the canvas. I think we need more work on the kind of changes that can trigger this paint event. There are some changes that might not trigger the update of the rendering. E.g. video playback, or image animation, or just a blinking caret. These kinds of changes... not sure if they're completely exposed to JS. UA can do lots of optimizations to put them on other threads. I am wondering if there would be interop risks, e.g. if some new implementation offloads work to a differnet thread, but we require them to change it.

...Also concerned as to whether we want to keep the descendents as interactive, or how to achieve interativity, Current approach seems hacky. The draw element-image method returns a transform matrix, and then put that matrix on the element's styles so it's transformed. This feels both unergonomic, and error-prone. What if we draw the same element twice? What if there are multiple elemlents but we draw them in an order that's different to DOM order?

Lola: You said that using the trasnform matrix and applying to element is hacky. If we draw the same element twice, what is the effect? Wouldn't we want the same thing to happen to both of them?

Xiaocheng: There's no way to apply one transform to one of the elements only - e.g. when we are doing hit testing.

Lola: Makes sense.

Matthew: APA is looking at it.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Proponents responded to us asking for clarifications. I drafted something about the side channel. There is a concern about reporting, to which I think Yves is more eligible to respond.

Yves: I remember that Mike had in mind an attacker being on the network, and not being the site itself.

Ehsan: I think in general we are positive about it.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Matthew to write comment

### [design-reviews#1035: CSS Gap Decorations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1035) ([Github](https://github.com/w3ctag/design-reviews/issues/1035)) - @matatk, @xiaochengh

Xiaocheng: we reviewed the previous version as satisfied. This refresh doesn't add anythign that is architecturally contraversial. It's well written. Safe to say satsified. Leave technical details to the WG.

Matthew: +1

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew to write comment

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew to make proposal based on discussion and breakouts day session.

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @xiaochengh

Xiaocheng: Last time we raised concerns about privacy and when to trigger the rendering. They replied and clarified 2 things:

First, this new type of prerenderign is supposed to be used differently from existing speculation rules. Existing rules can be included in HTTP respons or <script>. For form submission prerendering, they clarified that the developer should dynamically insert it via JS when the use is about to submit. This seems weird as it's very different to all the other types of specultion roles.

We asked about how to prevent submitting kinds of user data via speculative loads. If I understand their response correctly, they're saying that they only allow speculative form submission loads with exact URLs but not pattern matching. So I assume the intended use case is that first the developer should detect the user is about to submit the form, e.g. if the submit button is hovered, and then they extract the form data and create a speculation rule and insert it into the document. I assume that's the intended usage, which again sounds weird to me.

Lola: Would you like someone else assigned?

Xiaogheng: I'm worried about the inconsistency.

Lola: I think that's very ipmortant to raise. Have you raised this with them already?

Xiaocheng: No. I can send a response first to confirm that my understanding is correct.

Lola: OK. I'll post in the design reviews channel to see if anyone else wants to get involved.


## Plenary Session - None
