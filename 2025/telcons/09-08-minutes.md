# TAG Minutes - Week of 8 Sept 2025

## Breakout A (Asia / Australia / West America) - [2025-09-09](https://www.timeanddate.com/worldclock/converter.html?iso=20250909T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Jeffrey, Xiaocheng, Max, Marcos

### F2F Planning - Comment on draft agenda and claim topic introductions and breakout sessions.

Martin to take Digital Credentials intro. Maybe Marcos can intro the current state.

AI is probably several pieces. Anyone looked into Perplexity/Comet/OpenAI browser?

Martin: Consider making space for stuff that's not on the program. You have essentially a 3-hour block for each topic; we'll need breaks.

Jeffrey: We can take some time from the 1.5h broken-out period, or from the concluding section.

Martin: Think the concluding session will use the whole time.


Xiaocheng: Will consider offline and update by breakout C.


### [web-no-papers#37: Editorial pass](https://github.com/w3ctag/web-no-papers/pull/37) - @martinthomson

Martin: Merging this.

### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @martinthomson, @jyasskin, @toreini

Martin: This is ready to re-review. Un-ticked things from https://github.com/w3ctag/web-no-papers/issues/15#issue-3261471067 are either WONTFIX or maybe-fixed. I'll take another look at those.

Jeffrey: I can re-review based on that statement.

----

Xiaocheng: Do we have thoughts on legal regulations on government-issued credentials?

Martin: It does touch on that. Jeffrey's review suggested that we push harder on saying the legal restrictions exist. Don't know if it was made clear enough. My knowledge is that the EU is the weirdest and most forthright in levying requirements on how websites can use identity. But they do exist in other places. They've also been unsuccessful in implementing those.

Xiaocheng: Wondering if the issues mentioned in the document might be out of the scope of technical solutions. What if verifier insists to track people? Record user data and sell it?

Martin: It comes down to legal recourse. Contract that's being signed up to when providing the information. in the EU framework, the website , when it asks for the information, it's under the understanding that they've gained permission or published the reasons. If they stray, that's a matter for national data protection authority to fine them or whatever. Entirely outside of the technical frameworks.

Jeffrey: Technical frameworks can ensure transparency and make violations visible.

Martin: Need to enable those things when building these systems. Encouraged by what Rick was telling me. Don't like it but it's better than the baseline by far. Apple's done a similar thing. They have huge problems, but also a long way better than the baseline. In both cases, if you want to use a credential, in the Google system there's a scary interstitial that's shown if you use it without registering, and in Apple's case you can't use it at all. Once you're registered, there's some commitment that you're requesting particular information for a particular purpose. Google makes a public record. Don't know about Apple.

Marcos: Handled by a different part of Apple than I'm involved with.

Martin: Gave Tommy a hard time when he used it for Privacy Pass.

Xiaocheng: Is the scary prompt shown to the user?

Martin: Yes. https://issues.chromium.org/issues/440387001 has a screenshot.

Xiaocheng: There's definitely something not possible within the technical framework. And we're a technical group, not a legal group. 


Jeffrey: My styance is that we are in charge of safeguarding the web architecture.  Sometimes these aspects threaten the architecture, how people can use the web, what structures evolve.  We need to think about the political implications of our decisions.  We can only make technical changes.  We can say things about the structure of the web outside of that structure operate in order to protect that core.  We are therefore in-bounds in saying that.

Marcos: TAG has done that before, maybe for EME.

Martin: It comes up occasionally. Usually it's a technical topic, wereas here the technical architecture is relatively small compared to the size of the component we're talking about. Social and political architecture are more relevant. But we talk about those too. We have Ethical Web Principles which isn't strictly technical.

Xiaocheng: We should provide technical designs that are easy to cooperate with government regulations.


Jeffrey: We would really like input to the technical bits, so that we understand what effect the technical bits have on policy.  California is writing a law to require GPC settings.  Our user agent finding might be relevant to that finding.  We need policy people to tell us how we can structure that finding so that is most useful for lawmakers.  (Global Privacy Control: https://www.w3.org/TR/gpc/)




### [process#45: Add an AI policy that we don't use AI to generate human-read text or summarize human-written text.](https://github.com/w3ctag/process/pull/45) - @jyasskin

Jeffrey: How do you feel about this?

Xiaocheng: Looks good. We should avoid using AI to process issues, aside from proofreading.

Jeffrey: Let me know about any changes, and we'll come back at plenary.

Martin: Question about quality of explainers continues to be a point of tension. But not sure this is the right place to litigate it. Good as a general principle to say that if we're trying to communicate with other people, we should try to write the words or be responsible for the words. Ok if the AI writes it if we stand by every word on the screen.

[Marcos arrives]

Marcos: This doesn't reflect how these tools are used. Generally yes, but this isn't how they're used.

Martin: How so?

Marcos: The way they're used is, you do a lot of back-and-forth with the tooling to get the thing you want. It's not like spellcheck where you do it once. You debate with it, and come up with a thing, where the end text reflects the back-and-forth between the model and human. You can do it and tell it not to write anything, but it's counter-productive. You don't go to chatgpt, or Github ... it gets you into the flow of seeing the things it's getting wrong, because it's bad at the thing, and eventually you get to a steady state. This takes an old-school view of how the tooling is used. It's radically different today to the examples given here.

Jeffrey: This doesn't have examples. This says that we don't write to other people

Marcos: Don't think that's realistic. Most people will go back and forth, like a code review.

Jeffrey: That's fundamentally disrespectful to the other people. You're dumping work on them.

Marcos: That'll be the norm for most people. Most people will use it in that way. "Go do some research; what will they argue with? Integrate that into the text." You fundamentally use it to create a final text. It's checked by people to make sure they agree. You want it to do as much of the writing as possible. 

Jeffrey: Checking a lie is much harder than avoiding writing a lie in the first place.

Marcos: Not once you have the experience.

Jeffrey: I'm proposing that we learn elsewhere. We can always change the rule later, once we have more experience.

Marcos: Might be ok. We can use the tool in parallel to prepare things, and then come back to writing a thing based on the output. 

Martin: And using it to proofread, suggest grammatical corrections. Those systems do work. The whole-cloth stuff that tripped us up in the Prompt review. Missing things is human.

Jeffrey: Are we ok with this restriction, at least until it's time to change it again?

Marcos: Yes.

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @jyasskin, @marcoscaceres, @toreini

Jeffrey: We need to propose a consensus comment. Think there's some continuing disagreement within the TAG.

Martin: Comes down to whether the privacy risk is justified. Website currently iterates down the login methods; maybe browser can do it.



## Breakout B (America / Europe) - [2025-09-10](https://www.timeanddate.com/worldclock/converter.html?iso=20250910T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Dan, Matthew, Sarven, Jeffrey, Christian, Yves

Regrets: Hadley, Ehsan

Scribe: Matthew

### F2F Planning - Comment on draft agenda and claim topic introductions and breakout sessions.

*Looking at spreadsheet*

Lola: 2 relevant sheets: HK 2025 topics; HK 2025 schedule. We've scheduled pretty-much everything except for 19a potential drops - 3 topics that we think we would need to discard due to time constraints. If you feel they're important to discuss, please raise these now. Carrying semantics in URIs or content; Decentralisation (Societal impact); Cryptocurrency.

Jeffrey: Carrying semantics in URIs: (Martin's suggestions) some proposals send the context in the URI, but should we be sending that in a document, and make a format for those semantics. One reason to drop: other proposals don't come to mind, so maybe can handle as part of the design review.

Matthew: Might DIDs be relevant?

Jeffrey: For DIDs, they _name_ a document. Interesting example, but lean towards the content answer.

Lola: Seen Sarven's merged your PR following our meeting last week. This was part of the reaosn for potentially dropping - we have discussed it now (but hadn't when it was added ot the agenda); is that OK?

Sarven: Yep; this is OK for now.

Yves: We need to talk about the upcoming appointments, what is missing from the TAG and what the TAG would like to see from the new appointees.

Jeffrey: Adding for Thursday afternoon. The last block is scheduled for doing a retrospective and doing any changes on how we need to work. Another topic is how to recruit candidates for the election.

Lola: Brings us to HK 2025 schedule. For people not attending in person, Sarven, Hadley, Yves, we've tried to schedule these for times you'd be available in your timezone, which is usually our afternoon.

Sarven: Some may need moving. After 1530 I can make things.

Jeffrey: The idea was to take two topics in parallel, with an intro, then parallel working, then summarization to the group. Maybe instead of taking Wednesday afternoon off, we should take Wednesday morning off, and move design principles to Monday afternoon.

Lola: I'd like to check with Martin as he's suggested we take Wednesday afternoon off becuase the dev meetup goes quite late. If we do that (take Wednesday morning off), maybe we could start Thursday later? e.g. 10 instead of 9.

Jeffrey: That's plausable.

Sarven: On Monday I could join at 11:15 to 11:30 if needed.

Lola: Suggestion above (re Weds/Thurs) would be my preference - will confirm tomorrow after planning meeting with chairs and Yves.

Sarven: It's not clear to me how long the slot would be for web-no-papers and UAs.

Jeffrey: the idea is to tak the whole afternoon for both. But we could move this earlier, break it aorund lunch.

Lola: Any other thoughts/questions about the schedule?

Jeffrey: 2 other things we need to do: (1) assign people to present the introductions on each topic, to get people thinking in the right direction for the topics; and (2) split out AI & the web into mutliple topics.

Lola: Any objections to current schedule?

*none*

Lola: Did anything come out of Breakout A?

Jeffrey: Martin will do the introdcution to Digital Credentials. Xiaocheng will come back with what he'll present.

Jeffrey: People mark which topics they're intersted in on the grid. Need to socialize this.

Lola: Anyone want to do intros? Also before that we should split out AI & the web. Then easier for people to choose what they want to lead on.

Jeffrey: the 2 sub-topics I have in mind are: (1) protecting web sites from AI crawlers and substituting AI output for the web sites' output (taking users away); and (2) maybe there's a future where everyone's interacting with AI and current web sites go away and are replaced by something. What do we want the _something_ to look like? There's probably other topics I'm not thinking of right now!

Lola: Any recent relevant design reviews? Prompt API; NLP? Are there pattnerns.

Matthew: Might not be a pattern, but a big issue from Ehsan: Research and some recent design reviews indicate that when a model runs in the browser, there should be stricter security. They should be treated with similar restrictions to web extensions.

Jeffrey: I've been talking with people along similar lines; another angle is MCP: how do we mediate capabilities?

Lola: Any volunteers?

Jeffrey: I can introduce 'the transformed web' idea.

Sarven: More on general AI and the web. Any discussion along the lines of cognitive accessibility?

Matthew: COGA has thought about this. Tip of the iceberg is in finding appropriate help for people. Video, text, human, AI chatbot. Different channels are appropriate for different people. They've written about it.

Jeffrey: Is this something _we_ should be discussing rather than leaving it for accessibility groups?

Sarven: That's what I'm wondering too and whether there are architectural concerns we need to discuss. https://w3c.github.io/coga/

Jeffrey: Suggest Matthew takes securing AI.

Matthew: Yep, sure.

Lola: If somethign calls to you, feel free to update. I just took @@@@@@@@@@@@ and co-ordinating with Yves, Hadley, and Jeffrey tomorrow. Thanks for all your work on this Jeffrey.

### [design-reviews#1137: [wg/didmethods] DID Methods Working Group](https://github.com/w3ctag/design-reviews/issues/1137) - @jyasskin, @csarven

Sarven: Reviewed https://github.com/w3ctag/design-reviews-private-brainstorming/issues/192#issuecomment-3269883653

Jeffrey: Ready to send a comment - after checking with rest of the group.

*group is OK with it*

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

Sarven: When last we discused it, we said we should just put something out there and go from there; we have plenty of material.

...I think [Implementing the Web Platform - issue 22](https://github.com/w3ctag/user-agents/issues/22) rolls under the same scope of what is a UA. I think it adds to that discussion rather than being separate.

Jeffrey: I don't think you have to implement the whole platform to be a UA. I think it's OK to consider them as related.

Lola: So situation still is there's no update right now; we are waiting PRs.

### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin

Jeffrey: Think this is ready to merge; waiting for people to review it. Messaged the Web View WG to check with them. We need people from TAG to review.

Lola: Anyone up for reviewing?

Jeffrey: California is passing a bill that requires browsers to support GPC. This may have an effect on that legislation.

Sarven: I'd like to review.

Lola: +1

### [accessibility-screener#9: Convert to HTML form](https://github.com/w3ctag/accessibility-screener/pull/9) - @ananya-ky

\[Discussion of action items identified in https://github.com/w3ctag/accessibility-screener/pull/9/files#r2334860052]

Jeffrey: I think this is ready to merge now, and the action items can be follow-ups.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://github.com/w3ctag/design-reviews/issues/1120) - @matatk, @xiaochengh

Matthew: Discussion is being restarted on the blink-dev about the other approaches. There was a prior proposal that's closer to what we suggested (UA-controlled colors). We're expecting the explainer to be updated with abuse cases and alternatives considered. A point of concern showed up in WebKit standards positions thread. It would be interesting to look at the Blink discussion and how it's going. Are the proponents hoping to move forward with this?

Dan: blink-dev discussion is at https://groups.google.com/u/0/a/chromium.org/g/blink-dev/c/U-6tIuuGtgo/m/TgCkWVWoAQAJ

Jeffrey: I think Martin suggested that Safari look at the other use cases for this, such as highlighting a whole row of a table, for example. We can look at the abuse cases and make an assessment as to whether it should ship.

Dan: My understanding of the current proposal is that it doesn't support highlighting the full line of the table that the match is on. The set of highlights would be used for setting colors, text shadow, but not ::before, ::after - if we think something more powerful is needed, this won't address that.

Jeffrey: I thought you could say :has(::search-text) to highlight a row of a table.

Dan: Maybe... would need to check on that.

Lola: Sounds like we're not sure about our position on this. Matthew, do you want to clarify them as to their plans, or wait to hear back?

Matthew: I should add 'pending external feedback' re the Explainer. Good to have clear comms with them, so we don't lose the thread. If the UA were to override the choice of colours, would that be compatible with the current proposal?

Dan: I see the discussion on the blink-dev thread looks to be going in the right direction - considering other use cases. We could add more, like highlighting a line of the table. The other question I have asked and maybe TAG could too: if browsers automatically ensure there was not contrast issues, like Safari does, would develoeprs want this? Looking at the analagous selection APIs, dethe answer is 'yes' as developers want that for aesthetic reasons. Whether it would apply here I'm not sure.

Lola: Someone mentioned aesthetic reasons, branding, before. I'm concerned about the accessibility aspects. It's the proponents' responsibility to do the user research to show there's an appetite for it. This should be in the Explainer (if it's not). Sounds like Matthew needs to change it to 'pending external feedback' and we want to ask them a few different things about what they're doing right now.

*Matthew subsequently posted <https://github.com/w3ctag/design-reviews/issues/1120#issuecomment-3276112848>*

### [design-reviews#1143: [wg/png] PNG Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1143) - @christianliebel

Christian: 4th ed includes HDR/SDR. 5th edition includes new compression algorithm that will break compatibility with existing image files. Thoughts so far are that we're fine with it, but they need to make sure you can treat the new images files safely. Martin suggestetd that if you need new code to interpret it, then it's a breaking change.

Yves: Same issue with all the containers that embed differnt formats. E.g. video like Matroska. I treat this as the same case.

Matthew: My read was that if it needs new code to interpret it, it's a new format. A way to make it safe is to duplicate the old format, but then you've lost the benefit. Don't see how this is fine if that's the way to solve it. That would be hard.

Jeffrey: There's a comment Christian linked to in the discusion that makes the point I would make: if existing decoders can't decode new files, then it's a new format. It's true that's been done in video codecs, but I think it's new for images, and we should hold that line. We also have 2 new generations and 3 new formats for images WebP, AVI..., JPEG XL that all do better than PNG. Any suggestion to break compatibility with PNG needs to be compared to those new formats and justify itself. We should be sceptical of any backwards-incompatible changes.

Christian: Do the same review resolutions apply to charter reviews?

Jeffrey: There are no rules; we can use what's appropriate. The text of the charter review is more appropriate than the code - it'll be pasted into the strategy repo thread.

Christian: I'd remove the resolution, add what you said to the proposed comment, and then we can discuss again. Will post to (TAG's) private repo for discussion.


## Breakout C (Europe / Asia / Australia) - [2025-09-11](https://www.timeanddate.com/worldclock/converter.html?iso=20250911T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Matthew, Christian, Yves, Lola, Sarven, Xiaocheng, Marcos, Liu

Regrets:

Scribe: Sarven


### F2F Planning - Comment on draft agenda and claim topic introductions and breakout sessions.

Lola: Discussed in breakout A, B. Are there other topics folks here can lead on?

Xiaocheng: I'd like to take the AI topic.

Lola: We have sub-topics.

Xiaocheng: Can lead the Exposing MCP topic.

Lola: A 10m intro to topic and we breakaway, then we come back to discuss as a group.

Xiaocheng: I'd like to rename Agentic Web.

Sarven: What was "taking users away"?

Matthew: If traditional webpages go away, then what happens? Perhaps just the near-term.

Matthew: A 10m intro like in Paris is suitable. We split them into 3 half hour discussions. An intro would be much smaler than 10m, e.g., a third of the time. Could we double check on Plenary?

Lola: Ack. With the AI and Web, I definitely think we can discuss that in Plenary because it is different from the others. Chairs will meet to finalise this but we may changing around so that we have to accomodate folks dialing in remotely.

Lola: If any associates want to join for sub-topics, let us know.

Lola: Noting that Topics and Schedule look okay to folks in the room.

Xiaocheng: Regarding the logistics, for venues: a room for at most 20 people and 2 small rooms for breakouts.

Lola: 2 is okay for every day except Tuesday I think.

Xiaocheng: Can check.

Xiaocheng: re IT requirements, for joining remotely GOogle Meet?

Lola: I don't think anything has been decided.

Xiaocheng: The meeting rooms are set-up for someting else.

Lola: Marcos you had concerns re security?

Marcos: Already addressed.

Sarven: Could use Jitsi as fallback.

Xiaocheng: Need presentation setup.

Lola: We had a board but didn't have a screen.

Hadley: We had a screen.

Yves: A good way ot have one central point.

Xiaocheng: re food, do we eat on our own or how we can provide food. If latter, we need to collect dietary restrictions.

Hadley: It'd be great to have food provided, helps some of us and can continue discussing/socialising.

Lola: I'll help fill out the dietary req after the call.

Xiaocheng: re Wifi connection troubles, let me know.

Lola: Thank you Xiaocheng for organising all this.

### [societal-impact-questionnaire#23: Introduce concerns about centralization](https://github.com/w3ctag/societal-impact-questionnaire/pull/23) - @csarven

Sarven: Got merged.

### [societal-impact-questionnaire#4: Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4)

Lola: Sarven will have some text on how AI-like question may be worded.

Sarven: Will look into PR.

Lola: Will take agenda+ off.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: I'll prioritise this.

### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Lola: Any update?

Marcos: Not yet.

Lola: We're discussing this in HK, as part of Web-no-papers session.

Lola: Matthew, Ehsan, aything to add?

Matthew, Ehsan: No.

### [design-reviews#1131: Approximate Geolocation](https://github.com/w3ctag/design-reviews/issues/1131) - @marcoscaceres, @toreini, @christianliebel, @lolaodelola

Ehsan: Will raise any issues in the repo separately. 

Matthew: One conern re Ehsan's comments, unclear ot me the Explainer is ... it is not in the spec, and there should be one. Don't know if that decision was finalised. Some of the things in the Explainer whether there'd be a prompt.

Yves: Part of the draft response I made was not treating it the same was as IP location. By default, it says if you're using a prompt, continue using it. Depends on the rest of the specification.

Ehsan: Jeffrey mentioned there is a prompt section in the spec and somehow implies mandatory prompt. 

Marcos: Not yet clear what fingerprinting risks are.

Lola: What would be significant enough?

Marcos: We don't know what it looks like. re legal, wide enough? e.g. 500something meters enough vs. like country-wide. We don't know at this point what that looks like. What the underlying platform gives. Could chopping off the coordinate system be enough.

Ehsan: Whether that approximate data is good enough to mask the exact location. Having that approximate data from Android, then with like 1000 data points to get accurate data. It is mentioned in the spec that the frequency in that approximate is every 15m. These combined increases the attack vector significantly.

Ehsan: The other concern is about getting more precise geo location data. Like people's locations. I don't know if the Explainer accurately mentions, whether same concern as precise. What do others think?

Marcos: These are valid points / explorations on how all this could work. The general idea is possible but how it works in practice needs ot be raised.

Hadley: 500m may be okay to obscure identity in the city but not in the country. It could be identifiable in some rural areas. So the population density makes a good difference.

Ehsan: I think population factors into geolocation in operating systems. It's in the explainer.

Hadley: Reassured to hear that.

Lola: Sounds like there is still some info the group is waiting for some legal stuff to happen?

Marcos: There are the legal things in place and what the right thing is for users. They weren't always designed with privacy in mind, more focused on battery usage. Whether the privacy goals can be made by the platform. If the thing was designed around battery usage, then that might or not be an issue. It can be done in a country wide. There are some great unknowns.

Lola: Sounds like the group still has some work to do. We tell them our concerns / questions around the prompt stuff. So, comment can go on the main thread. Who is going to draft the comment?

Ehsan: There is a draft.

Lola: Noting Yves has a comment. Also you want to add stuff about prompting to Yves' comment.

Matthew: Maybe we're happy with it.

Lola: Will leave it to Yves.

Yves: If Ehsan has additional comments, please add to private brainstorming.

### [design-reviews#1135: Incubation: Inline Integrity](https://github.com/w3ctag/design-reviews/issues/1135) - @toreini

Ehsan: Will finalise review.

### [design-reviews#1142: Incubation: FormControlRange - Live ranges for `<input>` and `<textarea>`](https://github.com/w3ctag/design-reviews/issues/1142) - @csarven, @matatk

Matthw: I haven't thoroughly looked at this yet.

### [design-reviews#1130: Incubation: An `Origin` Object](https://github.com/w3ctag/design-reviews/issues/1130) - @csarven, @dandclark

Sarven: If an additional review is needed, I can otherwise Dan seems to have covered a lot of ground already.

Lola: Dan's last comment was yesterday.

### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://github.com/w3ctag/design-reviews/issues/1140) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Lola: Doesn't seem like anyone else brainstormed further.

Matthew: We've discussed last week but didn't make it to the issue.

### [design-reviews#1139: WG Revision: Dubbing and Audio description Profiles of TTML2 (for 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/1139) - @matatk

Lola: Is this the one they know more than us so let them be?

Matthew: Yes, and APA is reviewing stuff for them as well. This is specific tech and APA doesn't generally have concerns about it. I don't know how architectural it is or how widely it is used. Broadcast media is widely used but not sure outside of that. The consensus last week was that they're the experts - and I agree.

Hadley: My general approach with them / TTML, they are indeed the experts, we joined them up with CSS for something overlapping they're doing. So I'm 95% on board with we declare victory and close this. May want to double check with them re concerns for other parts of the web.

Matthew: Checking to see if there are substantive changes since previous review. There are quite a bit of changes listed. Maybe I can go through the changes and flag anything architectural in nature. One is labelled as at risk. Will do offline.

Hadley: You could also just ask them questions, e.g., what do we need to pay attention to?

Matthew: Sure, will ask for clarification.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://github.com/w3ctag/design-reviews/issues/1136) - @toreini, @lolaodelola

Lola: I haven't looked at this yet.

Ehsan: I haven't read it carefuly. Don't have concrete opinion yet.

Lola: Am a bit biased the title doesn't fill me with hope.

Ehsan: It seems like the discussions have been around for a long time (2020?) I see Martin has an interaction so will ask him later for opinion.

Lola: I may be wrong about this but this is one of the proposals related to third-party cookies.

Matthew: What's the diff with https://github.com/w3ctag/design-reviews/issues/1145 ?

Lola: I'll ask them.

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) - @toreini

Ehsan: I submitted my review and internally discussed. Waiting for final go from Jeffrey. More or less there.




## Plenary Session - [2025-09-11](https://www.timeanddate.com/worldclock/converter.html?iso=20250911T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Jeffrey, Sarven, Martin, Matthew, Ehsan, Philippe Le Hégaret (guest), Christian, Marcos, Yves, Xiaocheng, Hadley

Regrets:

Scribe: Sarven

Special guest: PLH to discuss the W3C Technical Strategy Task Force


Jeffrey: PLH will introduce us to W3C Tech Strategy TF.

Philippe: CEO was tasked by the board to develop a strategy for the consortium.  We are to establish several TF to split tasks, one of which is Technical Strategy. (https://www.w3.org/2025/06/w3c-2025-roadmap-to-develop-a-strategy/index.html#5-5-technology-strategy) It doesn't exist yet but we are here ot talk about how to interact with TAG, as well as joining the TF. The timeline to deliver is 2026-Q1. The plan is to establish Tech Strategy (TS) for 3 years (2026-2028) help us understand the priority and how to approach them.

Philippe: First time I'm doing this exercise. I believe we should get as much input as possible from membership and staff, challenges for W3C and the web, and use that to inform the strategy. If everything goes well, we need a questionnaire by TPAC2025, a month to answer, and hten in the month of January, we process the input, then release to at large by early February. Get early feedback and iterate. It should be highlevel TS. We are not to tell the TAG what to do but we should draw the lines on what W3C should spend its time on TS. There are some challenges ahead of us. TS that doesn't talk about AI nowadays will be questionable. We have no choice, so we'll talk about it. Also User Agents (UA), without it would be lacking. Also divergence re Linked Data (LD) people and non-Linked-Data people. W3C historically has been leaning toward LD. Need to ask if this is the right way forward. Thanks to TAG we have some principles. At least we can expect to follow some principles. We have a platform to put limits on the web on our strategy coming forward. The web also of course uses mobile phones. The experience on the mobile phones is not as good as we'd like. The strategy ??? mobile first and desktop second. So, I should stop here and hear feedback here.

Jeffrey: Questions for the group. Who is willing to vounteer in the TF and what initial thoughts the group has. We also have F2F to develop more thougths.

Lola: Question about time commitments. How much would this require and how frequent whould meetings be?

Philippe: 1-2 meetings before TPAC. 1 meeting before end of meeting potentially, and then 2-3 meetings in early 2026. ~7 hours + email + slack.

Hadley: How does this TS work compared ot others? We have in the past things coming fomr the ground up. We have some statements of this is a hole we need to fill in the TAG. It feels like we have the potential to spend energy at W3C... may not allow evolution for W3C ot have. Wondering about how to keep the work relevant and all the things going on in the community.

Philippe: As you said we can't predict the future and we shouldn't. W3C need not go into details. Making sure that W3C relevant being able to adapt to new tech as well. If we feel that our current strategy is reactive enough then we can say that and nothing to change. But if we are lacking in reactiveness, then we should also say that as well. Don't need to provide solutions but provide direction for the next years.

Hadley: Sounds like needs discussion and also concerned about time commitments.

Martin: You identified the mobile experience as potential problem. I'm almost convinced that this is not a tech problem. That might be of an indicative of a problem not necessarily tech. We tend to talk about last years problems. We have all been .. what our experiences has been in the past. We talked about different pipes, also AI, ... I'm concerned about top-down tech strategy is going to change anything for the better. Can you spend more time to convince me where I can think I can believe in for the TS for W3C. Rather than bottom-up.

Philippe: W3C is going through different roadmaps. If that doesn't talk about tech ...

Martin: We also have the Vision (from the AB). That talks about how we produce rather than what / technical. What they did was perfectly fine.

Philippe: I agree with that. I tis a highlevel vision. I'd expect no less from TS. I'd use few examples / ideas. Except perhaps for AI. I believe the current approach we have doesn't necessarily need a correction. W3C is looking at AI and how it is going ot impact the web and the UA, and reflecting that in the strategy. We are going ot hav eot stay high level. doesn' thave to be "5 pages". 1 page would fulfill a goal here. I've never done this exercise here. This is first here. W3C hasn't done this before. We are going ot have to learn. This is one of several TS. There is another for Structural Evolution. This is not the goal of the TF. Re "mobile first", I met a lot of pepole in China tha tdon't believe that we need a more tech solution to solve the problem.

Martin: Yea, I think they are using apps aren't they?

Philippe: Miniapps and modifying their own views for their own purposes.

Jeffrey: I wanted to add two things and also to volunteer on the TF. We can decide on presciptive and descriptive. We are only trying to predict several years out. I think even just describing the overall direction is going ot be valuable even if we don't expect it to go that way. I think looking at tech from other places (???) would be good input.

\[Martin]: You might find some inspiration in https://lettersofnote.com/2011/07/22/the-internet-tidal-wave/

\[Philippe]: https://www.ietf.org/media/documents/IETF_Administrative_Strategic_Plan_2024_-_FINAL.pdf

Matthew: I'm still trying to visualise the goals and what the outputs look like. We talked a little bit about whether there is overalap between what this TF will do and various other groups. We talked a bit about purticular tech, reacting to change, and how quickly and not reacting to some others, incubation, monitoring traction. All that seems to be all about the rates of change. It seems there is some relation there. I was also thinking if this is stuff happening outside of W3C and what could be doing ourselves. It is well known there are other tech orgs we have shared interests, so would this strategy include we can't guarantee but we'd like ot collaborate with these orgs. There is one thing along those lines it is a challenge in our industry: different actors, SDO, what the threat model is and whether the browser is part of that, ... it seems like this sort of tech is going ot be fundamental and we don't necessarily agree as an industry. So far our approach has been let it come forward, and maybe we should have an ??? there is pressure to resolve. I'd be interested. I'm not 100% sure how much to contribute. Not sure how many you're looking for.

Philippe: In terms of final shape of the output, we can talk abotu that in the TF itself. In terms of number of people 5-6 max in the TF. 1-2 from TAG. 2-3 would be appreciated. I have shamelessly cornered DA to participate, and he ok'd.

Xiaocheng: How different will this TF be interms of ... What's the diff between this TF and making strategic planning.

Philippe: We didn't make strategic planning before that. Can't compare. If that's what you're asking.

Xiaocheng: How did we decide what direction to go?

Philippe: That's going to be the discussion for the TF. We'll need input from members of the community as well. I don't htink we should work in a vacuum.

Jeffrey: There is a strategy on GH. 

Hadley: There are a lot of things like momentum of the group, interest in particular tech, spawning the groups, someone looking at the big picture.

Xiaocheng: Top-down?

Hadley: That's what we are discussing. How much should it be top-down.

Philippe: While we should giv a high-level direction, we are not in a position what they are not going to do. I think the community does appreciate general direction from time to time.

Xiaocheng: I'm also interested in join but worried about time commitment.

Philippe: Mentioned 7-8h video conferencing beetween now and end of March. Plus email and Slack.

Lola: I'd like to volunteer myself as well.

Philippe: If whole TAG wants to participate you'd be welcome.

Hadley: I have written gov and tech strategies. It is somewhat similar. I'm happy to share that where that's useful. When we started to work on EWP, I was initially very against it and DA was very for it. We may/could say things right/wrong.. and not until talking about users the underlying principles sat better. Where we were saying things again and again, and this is part of a bigger whole, and until we got into the Statement process, ??? the angry TAG members yelling at the clouds. How do you see this TS to be applied?

Philippe: Didn't talk to BoD about that.

Hadley: That'd be a discussion to have. Perhaps the TF should work it out.

Martin: There are always trends in technology that rise and fall. A three year strategy cannot identify particular trends, so we will not seek to do that.  Instead, we will dedicate our efforts toward making a venue that people choose for standardization. We will seek to establish processes that can quickly identify emerging trends and provide a welcoming venue for people to work together on developing standards for these trends. We had lots of trends come and go. Even while in TAG. Some things have stuck around. Like the work being done in UX of/on the web. Who knows, AI may not be a thing. So setting up a strategy like that may be challenging.

Sarven: Have you considered having a group like the W3C Council (AB+TAG) come up with this instead of a Task Force?

Philippe: I was tasked with creating a Task Force. Councils were created to deal with Formal Objections, not direction, so they have a different purpose. Dan Appelquist is now on the AB, so we may have an AB member. I haven't talked to the AB as a whole.

Sarven: Challenge that a bit. I used the Council as an example because of its collective understanding. And social challenges as much as technical. Even within the TAG, we're not just looking at technical challenges in a vacuum. Not challenging W3C's decision to have only specific names instead of groups. Might be more to get from the group on the direction.

Jeffrey: I expect we'll have some folks from TAG by F2F for the TF.


Volunteers:
* Lola
* Jeffrey
* Xiaocheng (depending on time)
* (Dan Appelquist from PLH's previous conversation)
* Hadley

### [process#45: Add an AI policy that we don't use AI to generate human-read text or summarize human-written text.](https://github.com/w3ctag/process/pull/45) - @jyasskin

Jeffrey: Anything to tweak before merging?

Matthew: IIRC, it was Martin that AI may be an accessibility tool to some people. I think on that people were on that board with the idea that people will use those tools for themselves, but not specifically about just summarising things. The title of the issue may be a bit misleading.

Hadley: I don't think there is a problem with saying we'll user summary tools. 

Xiaocheng: What's the diff between AI and manual summarisation? In some ways we are using a summary of explainer to understand. It is our responsibility to make sure we undersatnd. In which we understand ??? 

Jeffrey: When we read/skim something to summarise to ourselves, and understand our mental proceses. "I believe the explainer says this" whereas with machine summarisation we don't know what it did. It may have missed a piece. Wehn we are writing comments based on machine's we don't see the shortcuts the machine took.

Xiaocheng: I don't trust myself skimming either. To understand, we need to go through it ourselves.

Matthew: Agree with the concerns that you've raised Jeffrey about if there is a problem and how it went wrong. My approach has been reading the explainer. My native language is what most explainers are written in. I think we want to avoid you've raise dand important to do that. Also strive to read that whole explainer. We should go from the source material. If some people have summarisation then to read the whole thing.

Jeffrey: If you do the summary and then read the explainer..

Hadley:  I think this similar to the conversation we had when we started asking for the explainer in the first place, when we couldn't cope with the workload of reading every spec, understanding all context and design decisions, etc. To speed up  understanding / make it easier to work with. If we were to use AI summaries tofill that role, I don't think it's a good thing. I wouldn't want to move away from the explainer solving that problem, so if explainers aren't working for us then I think we should adapt them.  I think there is a certain amount of work we're expecting and understanding with the community. There is value in writing down our side of the social contract: you do this work, and in return, we will do those things (like: read your explainer).

Sarven: Re mental processes, that idea needs more refining because some tools do show some form of steps they went through before generating a process. I think the point you're trying to make is about the value of us going through the manual exercise because that helps us better understand the material, and making our own connections with the things we know. As for the summaries themselves, I think the Explainers are already summaries themselves to begin with - condensing a lot of stuff / showing key considerations that can be used to help us evaluate. If there is an additional summary of that by a tool, that may be excessive - reinterpretation. I'm not suggesting that these tools shouldn't be used but that they introduce the possibility of misinterpretation. This is all even in addition to us reviewing the Explainers and discussing them in meetings which are in themselves summaries. So, the more summaries we have it increases points of failure / misinterpretation. To me reducing those misinterpretations is key.

Marcos: Appropriate use of the tool while having human checking is best approach.

Jeffrey: With prompt API humans didn't successfully check the incorrect generated text.

Jeffrey: Let's come back to this as it is not ready to be merged it seems.


### F2F Planning

## Grab bag of design reviews for filling extra time

### [design-reviews#1135: Incubation: Inline Integrity](https://github.com/w3ctag/design-reviews/issues/1135) - @toreini
### [design-reviews#1142: Incubation: FormControlRange - Live ranges for `<input>` and `<textarea>`](https://github.com/w3ctag/design-reviews/issues/1142) - @csarven, @matatk
### [design-reviews#1130: Incubation: An `Origin` Object](https://github.com/w3ctag/design-reviews/issues/1130) - @csarven, @dandclark
### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://github.com/w3ctag/design-reviews/issues/1140) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola
### [design-reviews#1139: WG Revision: Dubbing and Audio description Profiles of TTML2 (for 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/1139) - @matatk
### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://github.com/w3ctag/design-reviews/issues/1136) - @toreini, @lolaodelola
### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://github.com/w3ctag/design-reviews/issues/1134) - @jyasskin, @dandclark
### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres
### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) - @toreini
### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion
### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @martinthomson, @jyasskin, @csarven

### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
