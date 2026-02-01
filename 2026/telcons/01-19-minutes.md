# W3C TAG Minutes for week commencing 19 January 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/01-19-agenda.md).

## Atlantic Breakout (America / Europe) - [2026-01-19](https://www.timeanddate.com/worldclock/converter.html?iso=20260119T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Lola, Matthew, Ehsan, Yves, Christian, Hadley

Regrets: Jeffrey

Scribe: Matthew

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

bump

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: APA is working with cognitive accessibility tf, if anything comes up with cognitive accessibility we can bring it to this thread but for now we're waiting for external feedback from them.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49)

Lola: We want to stay up to date in terms of the CG.

Matthew: Will finish my PR today or tomorrow, by the next time we meet we'll have something to discuss. Martin has made good progress.

[Discussion about assigning someone to this so that it can easily be assigned to breakouts in scheduling. We went with the three chairs as assignees.]

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

bump

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

bump

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Matthew: Will catch up by EOD tomorrow

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: We need to ask if they could consider HTTP redirects instead of double handshake - the private comment has two +1s on it. I have input from the other two. I will post now.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel

Christian: Reached out to Tess per the discussion last week. Awaiting reply. Explainer has received updates, but still not clear on what they're trying to do.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: Nobody has objected when I said I was happy. Martin has pointed out there's no formal position from webkit or gecko so I've asked and we're waiting. 

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: I posted a comment yesterday asking for clarification but they've positively engaged with the questions we've asked. I asked about clarifying between their two current possiblities 1. either the page doesn't opt-in or 2. the page opts in, they talk about adding another value in future but I'm unconvinced this new keyword is necessary. They want to ship by weds, what they have now is fine to ship, just think their future plans are unneccessary. [*Matthew check this*] 


### [design-reviews#1176: Incubation: @supports at-rule](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1176) ([Github](https://github.com/w3ctag/design-reviews/issues/1176)) - @christianliebel, @lolaodelola

Christian: I think this is fine. However, it has some issues. Martin observed last week that it adds some complexity, which is true. You can query for an at-rule. There's the @charset rule, which will not be detected (that is fine). It checks for the at-rule in any context. Context doesn't matter. If the at-rule is only valid in a certain sub-context, you might get a false positive. I want to ask them about this - why is it designed like this (and not, e.g. context-sensitive)?

... There's also a special case for MQs, which are parsed differently. Makes sense from a technological standpoint, but could be confusing for developers (maybe this is what Martin meant).

... I plan to ask the questions.

Lola: What is the consequence of a false positive in this case?

Christian: You could think that a feature is available when it's not.

... They have a nice example in the Explainer. Is it OK for me to ask my proposed question?

Lola: Sure

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Matthew: It's progressed a bit since I've last looked at it, will look at it this week. Note that it's not an "Other" spec review, it's a full spec review now.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Yves and I have commented, I think the comments are complementary. If we can have a discussion, or agree to merge the comments, we can post them.

Yves: Makes sense - merging the two should be good.

Ehsan: I'll merge them and await your thumbs-up, and will then post.

Yves: Great.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

*We triaged some issues*

### Do we want to write any new documents?
 
 Potential ideas
 - CDNs
 - CSAM deepfakes
 - Browser extensions
 - Geopolitical stuff (USA vs Europe)

## Pacific Breakout (Asia / Australia / West America) - [2026-01-20](https://www.timeanddate.com/worldclock/converter.html?iso=20260120T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending:  Xiaocheng, Martin, Marcos

Regrets: Jeffrey (MLK day)

Scribe: 
    
### [execution contexts being not fully active](https://github.com/w3ctag/design-principles/pull/597)

Marcos: Might be able to rely on the fact that a document is one type of execution context and just concentrate on the document parts.
...ECMA-262 uses different terms and has different expectations to HTML.
...Hard to know if this is too much with the BFCache parts included.
...If there is some UI created associated with the document, then you should make that go away.  Same for geolocation, you might want to cancel those and stop delivering events. (Cancel, not pause.)
...This never comes back again, which isn't like BFCache where things can come back again.
...Question if you can use BFCache with an iframe, which might allow the back button to work.
...Popup windows are different again, which can be navigated.  Do they get BFCache treatment?
(Martin) I didn't think popups were special.

### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Marcos: Was the explanation on the issue OK?
Xiaocheng: Yes.
Marcos: Shall we merge it?
Martin: Yes.

### [design-reviews#1183: Incubation: new speculation rules action: prerender_until_script](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1183) ([Github](https://github.com/w3ctag/design-reviews/issues/1183)) - @xiaochengh

Xiaocheng: Early design review and it proposes a new type of action for speculation (adding to prefetch and prerender).  This does prerender, but doesn't run any script.  Parsing HTML pauses if there is blocking script.
...middle ground seems good.  Like to see some study on the use of script and what the effect of this would be.

Martin: Why can't prefetch do this?

Xiaocheng: prefetch doesn't fetch sub-resources and doesn't parse.

Martin: Parsing doesn't have observable effects, it's just the subresources that matter.

Xiaocheng: Chances are that finding subresources will hit script execution.

Martin: Two things: stuff you might need as data (prefetch) and stuff that you might navigate to (prefetch or prerender).  Prerender needs extra information about where content might appear, but then you have subresource fetching (side effect) and script execution (another side effect).

marcos: Prerender creates a new context.

Xiaocheng: It does everything, short of show the content.

Martin: Is it only top-level navigation?

Xiaocheng: How about we suggest that they test for efficacy (http archive?).  Also think about strategies.  Preparsing only?  (Which would have to block on script execution.)

Marcos: prerender is only for top-level navigations.

Martin: preparse would work for an iframe, wouldn't it? (not sure)

Marcos: It does annoy me that it is for the react use case, catering to something sites that use weird tools.  It seems like it is solving the problem.  A lot of people use React and this helps, but the other side is maybe you should put content in your page and not depend on script to populate it.

Martin: Is the implication that these scripts have unwanted side effects?

Marcos: Not my reading.  Not sure what is going on with \<iframe src=javascript...

Xiaocheng: Target case is for pages that can be mostly rendered statically, they don't want to load ads until the page is shown.  Question remains: how useful is this?  How often can it be used?

Martin: Ads case seems real.  But don't ads run intersection observer?  Maybe they just want to keep load down.

Xiaocheng: they should evaluate the success rate of the strategy.

Martin: They should also look at alternatives, like just preparse as a step toward this.  So how much does the subresource loading get you?  Or, could you limit the subresource types?  That might need some controls rather than a single mode.  For example, ads might use script exclusively, so no script execution is fine.  But others use pixels for tracking and so loading images could be bad.

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Xiaocheng: I posted a reply suggesting that the time they defined might not be useful. The response was that it was useful.  There was a thread on the subject.  The thread was almost only discussing how to define the paint timing in a well-defined way.  I maintain that it's still not useful.  It is only well-defined.  They haven't offered evidence.  I can think of ways this isn't useful: images, media, gaming, video conference arrangements.

Martin: It doesn't consider composit of images?

Xiaocheng: It marks the time before composit.  Arguing that this is the latest interoperable point in time you can define.  Which is true, but still useless.  A colleague saw the life of a pixel talk, which ended at this point, then thought "but that's the start of the life of the pixel".
... We have a dilemma: interoperable, but useless; or something that matches user experience, but is completely non-interoperable.  Maybe ask them to do more work.

Martin: I would ask for proof.  Ask someone to look at two or more engines and provide metrics on this point in time vs. actual presentation time (the point the pixels leave the graphics subsystem for the screen).

Xiaocheng: A more general issue here is that this more like an attempt to replace the established paint timing with a new definition.  They want developers to move from presentation time to this new composit start time.  Do we consider this a compatibility risk?

Martin: Only if people move.  If they keep using the old stuff, we can't remove it.

Xiaocheng: I can think of a case where the move is no good.  According to the discussion, paint timing reported by Chrome is the presentation time, but Firefox presents the paint time (the new definition; time before composit). ...

Martin: Might want to fix Firefox then.

Xiaocheng: They gets two sets of data with different measures.  This is adding to the analysis cost.

Martin: How do people really use the data?

Xiaocheng: Mixing the data would be bad potentially.

Martin: But people have machines with widely variable performance, so maybe mixing isn't so bad.  The problem with what Firefox does is that it hides some of the performance cost, that's all.

Xiaocheng: Composit onwards is not in-spec.

(Discussion about value of metrics like this.)

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

Nothing to triage there.


## Eurasia Breakout (Europe / Asia / Australia) - [2026-01-22](https://www.timeanddate.com/worldclock/converter.html?iso=20260122T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Hadley, Matthew, Sarven, Lola, Xiaocheng, Martin, Christian, Marcos, Ehsan, Yves

Regrets: 

Scribe: Christian

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) - @csarven, @lolaodelola

Sarven: No update.

Lola: No update.

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

Sarven: No update.

### F2F schedule

Hadley: We've been talking about what to spend time on at the F2F.  Note that design reviews tend to pop to the top of the priority list.  Everyone, think about what we might do about things like the social impact questionnaire at this meeting (implication; also about other similar work that we're doing).

Sarven: Sounds good.

Hadley: Question came up earlier this week, what kinds of shapes of sessions do we want to have? If editors say, we want an afternoon off to make progress, this is possible.

Sarven: I’ll come back to that.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: No update.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: No update.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

Marcos: Jeffrey asked to extend it into the other BFCache section which grows the scope of the work quite a bit. Need to go back and reconsider a bunch of stuff, maybe two PRs, maybe all at once. Does change the ask from the original thing. Right now, makes it much larger in scope than I can take on right now. Will take a while. Do we want to land little bits? If Chrome folks who did BFCache would like to jump in, that would be appreciated. Would like to land that stuff.

Martin: I’d like to see this land as well, work is pretty good. Jeffrey’s comment on BFCache is a real concern, we should address it. But would like to see incremental value. Is there a clear line we can draw? So we could have a cut point where Marcos could decide what he’s addressing and what not.

Hadley: You could put something in the actual text in that says "here are additional considerations around BFCache" to serve as a public marker, and still get it out the door.

Martin: We can reference the issue from a pull request, saying "there’s more to be done."

Hadley: Who has the next action on this?

Marcos: Me and/or Yves?

Yves: Wanted to look at the impact on BFCache, and I’m happy to have Marcos for the rest.

Hadley: Ok, so you draw the line, and discuss it with Jeffrey?

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Xiaocheng: Discussed it for a while. Think we have consensus that we need evidence about whether this is useful or not. I’m going to post a comment to ask for that evidence.

Matthew: Followed the discussion and think this is a very reasonable approach to take.

(Xiaocheng to post the comment.)

### [design-reviews#1183: Incubation: new speculation rules action: prerender_until_script](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1183) ([Github](https://github.com/w3ctag/design-reviews/issues/1183)) - @xiaochengh

Xiaocheng: Discussed it at B, as we didn’t have enough agenda items. Already posted a reply. Nothing to discuss today.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Xiaocheng: I’d like Matthew to drive this review.

Matthew: As said last week, APA is looking at it, we want things specifically to put in the a11y considerations section. No additional concerns or updates since last week, we’ll be wrapping it up from an APA perspective before next week. Will mention it in Slack if anything comes up, no active updates otherwise.

Hadley: More broadly than a11y, no other feedback?

Matthew: Trying to do that from TAG perspective, but looking forward from additional insights from CSS experts.

Hadley: Want to clarify the status regarding TAG activity. You are part-way through that?

Matthew: Yes.

### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

Sarven: Skip for me, I know Jeffrey did some work. It’s a giant document.

Hadley: Are we ok on timelines? Do they have a deadline?

Sarven: I don’t know, will look at this after Data Shapes.

Hadley: Ok, let’s have a quick look at the issue.

… They are looking for feedback in February, aim to publish in April. Seems realistic?

Sarven: I think so.

Hadley: If you and Jeffrey could get a first pass until next week, we should be able to sign it off and get it out the door?

Sarven: Ok!

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Sarven: No response from the WG but they are working on our feedback.

Hadley: Should we mark it pending external feedback?

Sarven: Yes. It also doesn’t need to be in the agenda.

Hadley: We marked it done for resolution, but we aren’t done with it yet?

Sarven: Ok, so the N-triples is ambivalent.

Hadley: Ok, I would like the resolution tag off. Do you want to post a nudge to wake them up?

Sarven: I know they have a PR coming up.

Hadley: Ok, I see it in their comment.

Sarven: I think it is fine.

Hadley: Changed the progress label to “pending external feedback.”

### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven

Sarven: No response from the WG but they are working on our feedback. Think it’s also in progress.

Hadley: Are we waiting for them?

Sarven: Yes.

Hadley: How long has it been?

Sarven: Mid-December.

Hadley: Should we fully close it?

Sarven: Suggest to leave it like this, and wait for another month. Again, these don’t need to be in the agenda. Not sure if they are Agenda+.

Hadley: They’re not, they are picked up because of their label.

### [design-reviews#1174: WG Revision: SHACL 1.2 SPARQL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1174) ([Github](https://github.com/w3ctag/design-reviews/issues/1174)) - @csarven

Sarven: Review SHACL 1.2 Core. I'll do this next.

### [design-reviews#1179: [wg/vc] Verifiable Credentials Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1179) ([Github](https://github.com/w3ctag/design-reviews/issues/1179)) - @csarven

Hadley: Is this a charter update?

Sarven: Yes.

Hadley: Haven’t they rechartered? I’m not sure if we can actually add given feedback.

Yves: Think there is a timeout soon (1st of February).

Sarven: Will have a review ready by next Monday.

Yves: In history, we didn’t review all the charters. If there are no important changes, we can let the AC review it, if things don‘t change in an architectural way.

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

Sarven: Reviewed this. Here’s a draft: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/222#issuecomment-3783287203

… Don’t think there’s a whole lot to say about this. Just two minor points. One, their summary of the feature (…), Spec seems to deviate from the process. More editorial feedback than on the actual spec. Second point, if it’s optional, I want to understand how it affects a deployment, or interop. Expected entailment on same data, same shape. Some of that is beyond my understanding of how data shapes work. Other changes regarding the inner works of SHACL instead of the inner part of architecture.

Hadley: Your comment looks good to me, additional thoughts?

Matthew: Not directly architecture-related. Happened to discover this one on UI generation (https://w3c.github.io/data-shapes/shacl12-ui/), which caught my interest. Really interesting.

Hadley: I think we haven’t been asked to review this spec, right?

Matthew: No, had a look at this as a part of APA, noticed user interface, and had a look.

Sarven: I’m aware that it exists, but didn’t have a look. Ties in well with authoring systems.

Matthew: Not sure how related it is, but dynamic UI generation is really interesting. Excellent stuff, but doesn’t go nearly enough as research that is 25 years old now. They can generate UIs of all sorts, and for all kinds of constraints.

Hadley: Even if you think this is interesting and well done, this is interesting to hear for the Working Group and the TAG.

Sarven: Are we ok to send the review?

Hadley: Yes, and please add the “pending external feedback” label. Just make sure your last line matches that.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: Last week, we discussed a reframing of this slightly, and I started to work on a comment. Then realized it had a deadline. Posted it, it’s too long, happy to take any feedback on it before posting it. There were a few people interested in this last week. Lola, Martin, Hadley, Xiaocheng? Would be in the minutes.

Hadley: It’s just Lola and Martin who had a chat comment. Do you want to ask Lola to have a look?

Matthew: Lola and Xiaocheng, if you have the bandwidth?

Xiaocheng: Yes.

Hadley: Sounds like a way forward!

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: No update, will contact people to see if we can get some historical perspective on it. From my perspective, we’re pretty stuck with contemporary discussion. Try to find out if there’s anything from before.

Hadley: Just looking at the issue… this is going on for a long time, what’s going on here? Particularly, when Jeffrey posted in July, that we’re overall satisfied with this API?

Matthew: From my perspective, I think the concern is the consistency of being able to do this across different platforms. Had a concern that it would affect established behaviors on iOS Safari, where you preview a link by long-pressing it. That was resolved by them. As I understand it, there’s a concern that this wouldn’t be satisfactorily implementable on XR platforms, which we hadn’t considered at the time when posting the comment. Would like to find a path forward to make this work, but it seems we don’t have TAG consensus. Long press wasn’t considered as a platform-primitive. I’d like to ask the Pointer Events people if this came up before, how they decided to deal with this, to unblock it.

Hadley: All for getting additional perspective. We can also resolve an issue without TAG consensus, we can write up the different thoughts. Not sure when that moment is, but feel we are kind of stuck.

Matthew: Think we need a deadline to do stuff. Will make the Pointer Events contact this week and see what comes back.

### [design-reviews#1012: User-defined script "entry points" for performance timing](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1012) ([Github](https://github.com/w3ctag/design-reviews/issues/1012)) - @matatk, @lolaodelola

Matthew: This is the one that didn’t have activity in a long time. We asked them a couple of questions a year ago, and didn’t receive any answers. Should we ping them again?

Hadley: We should ping them and ask Jeffrey, given it’s a Google proposal. If we don’t get anything else or we decide we’re done with it, we can close as timeout.

Matthew: Will ping them on the public thread.

### [design-reviews#1185: [wg/webediting] Web Editing Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1185) ([Github](https://github.com/w3ctag/design-reviews/issues/1185)) - @christianliebel, @lolaodelola

Christian: this is one of the charter updates. they are only extending deadlines and adding a new spec: the caret movement specification, to control the movement of a character set, improve internationalisation support. Seems fine, propose closing as satisfied if Lola agrees.

Hadley: everyone else agree?

[agreed]

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

Hadley: No new issues.

### F2F Planning

Matthew (on the developer meetup at the Samsung venue at King’s Cross): Just a couple things, it’s all on track, working on the paperwork. Hoping it’ll be absolutely confirmed by next week. It has been approved by the people from the event space. Been asked about timings etc. People would come in at 19h, and we have to be out by 21:45h. Is that ok?

Martin: Would try to get started at 19:20h.

Matthew: Haven’t got to the catering yet. Not sure if I can get the budget for it. Ticketing, I assume there will be some cost to setup Meetup stuff. Would pay for it myself because its easier. Limits 70 to 100?

Hadley: We need to get the word out quickly. We had 2 in Stockholm up to 40, 50 people in average. How many did we have in HK?

Martin: Probably 50.

Hadley: Think 70—100 is more than we need.

Matthew: Slightly raised stage with high seats. Ticketing and catering are the most important things.

Hadley: Once you have a ticketing page, let us know so we can share it and encourage people to come. Think we used a site called Tito.

Matthew: I’ll check it out.

Hadley: Do you need any support?

Matthew: Waiting for approvals. Should be absolutely confirmed by next week.

Hadley: Thank you for your hard work!
