# W3C TAG Minutes - Week of 13 Oct 2025

## Breakout A (Asia / Australia / West America) - [2025-10-14](https://www.timeanddate.com/worldclock/converter.html?iso=20251014T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Xiaocheng
    
Regrets:
    
Scribe:

### [design-principles#590: Add principles for task sources](https://github.com/w3ctag/design-principles/pull/590) - @marcoscaceres
### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres
### [design-principles#600: Avoid abbreviations for strings and enums](https://github.com/w3ctag/design-principles/pull/600) - @marcoscaceres
### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres
### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin

No updates since last time.

### [design-principles#584: Replace asking for users for consent with designing for user intent](https://github.com/w3ctag/design-principles/pull/584) - martin, jeffrey, marcos
### [design-principles#585: Clarify when details should go on events vs targets](https://github.com/w3ctag/design-principles/pull/585) - martin, xiaocheng, marcos

Xiaocheng: Still waiting on a reply to https://github.com/w3ctag/design-principles/pull/585#discussion_r2397614878. 

Jeffrey: Before we ping Jake, we should also wait for Martin's and Marcos' comments.

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @jyasskin, @marcoscaceres, @toreini (in A for Martin, Marcos, Jeffrey; in B for Jeffrey & Ehsan)


### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion (in A for Jeffrey & Max; in B for Jeffrey & Sarven; in C for Max & Sarven)
### [design-reviews#1157: WG New Spec: DID Resolution](https://github.com/w3ctag/design-reviews/issues/1157) - @jyasskin
### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres
### [design-reviews-private-brainstorming#211: WebMCP Review](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/211) - @xiaochengh

Xiaocheng: They clarified that this isn't trying to port the exact MCP to web. Concerned that they're not doing it at the right level. They're proposing a specific high-level API, which resembles MCP with some differences. Directly enables agent integration with web apps. Concerned that it might be too specific. 

Jeffrey: To be actionable, I think we need to give them a hint of what the low-level API would look like.

Xiaocheng: Vague idea is that right now they're building the API using abstractions that MCP uses. What if there's another protocol that uses different abstractions.

Jeffrey: And I'm not sure that there are other protocols for this purpose yet.

Xiaocheng: There are other protocols but maybe not for this exact purpose.

Jeffrey: Maybe the lower-level protocol is a general way to expose things to the outside world. Maybe that's just the 'tools' parameter.

Xiaocheng: Tools might be general enough, but elicitation might be very MCP-specific. Next step might not be to say they're doing it the wrong way, but initiating a discussion. Concern, but initiate a discussion. 

Jeffrey: It would be nice to encourage the use case if we do agree with it. Sounds like we might be positive on the 'tools' arguemnt but skeptical of the other pieces?

Xiaocheng: Yes. And the data format? Using the same format to expose tools as MCP.

Jeffrey: Haven't reviewed the format in detail, but I think they'd be open to suggestions.

Xiaocheng: And they're working with the AI Agent CG.

Jeffrey: I want to make sure they're also targeting things like Accessibility Tools, which could also take advantage of the semantic actions exposed by things like MCP.

Jeffrey: We should also mention that this should be exposed in the manifest, and not just in live Javascript.

Xiaocheng: They did mention that: https://github.com/webmachinelearning/webmcp?tab=readme-ov-file#progressive-web-apps-pwa
https://github.com/webmachinelearning/webmcp/blob/main/docs/proposal.md#web-app-manifest-other-manifest-based-or-declarative-approaches

Jeffrey: I think that this is important enough to expose in the first version, although I could be convinced otherwise.

Xiaocheng: Why is it important to expose it in the manifest? In their alternatives considered, they said it's limited to PWAs.

Jeffrey: Manifest isn't limited to PWA. Could imagine a browser, or even a search engine remembering the manifest. In a search result, the engine could direct users directly to an action instead of making them load a page first.

Xiaocheng: They consider a search engine to be a "backend" integration, that doesn't directly involve user interaction. They're targeting frontend integration, where the user is actively interacting.

Jeffrey: Think you're right, but not sure they're correct to focus just on that. 

Xiaocheng: Maybe that's just MCP?

Jeffrey: I think MCP is about keeping the interaction inside the chatbot, while this would allow a search engine to direct users to do the action in the website's context. Although MCP could always return a URL that could be navigated to do the same thing.

Xiaocheng to draft an updated comment.



## Breakout B (America / Europe) - [2025-10-15](https://www.timeanddate.com/worldclock/converter.html?iso=20251015T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Jeffrey, Yves, Christian, Matthew
    
Regrets: Hadley
    
Scribe: Christian

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

Matthew: Think we were supposed to close this, becuase we think what we got is fine. Will do it after this call.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven
 
Jeffrey: We still have some open PRs, we don't need to discuss it here.
 
### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: This is a parent issue to some PRs, so I will talk about it then.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: Nothing to discuss there.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Matthew: There is a small PR coming up, don't expect it to be controversial, will post to Slack once it’s done.
Jeffrey: Upcoming Docs CG meeting at TPAC might be helpful.
Lola: Nothing in the explainer-explainer issue you want to track?
Matthew: Not now.

### [design-principles#588: Rewrite the "removing features" section, incorporating "Support Existing Content" from the HTTP Design Principles](https://github.com/w3ctag/design-principles/pull/588) - @jyasskin, @csarven, @lolaodelola

Jeffrey: Need to ping Sarven and Martin. Thank you for the review, Lola.
Lola: Martin provided a review?
Jeffrey: Ok, only need to ping Sarven then.

### [societal-impact-questionnaire#25: Make Tristan former editor](https://github.com/w3ctag/societal-impact-questionnaire/pull/25) - @lolaodelola

Lola: This is manly for Hadley, and Hadley is not here. Tristan has resigned from TAG, so I made him a former editor on the societal impact questionnaire. It’s a very small change. Thanks to Jeffrey, Yves and Sarven for the reviews. Will merge once Hadley’s review is done.

### [user-agents#28: Add loyalty guidance for facilitating users switching UAs](https://github.com/w3ctag/user-agents/pull/28) - @csarven, @csarven

(Skipped)

### [societal-impact-questionnaire#26: Exclusion Example](https://github.com/w3ctag/societal-impact-questionnaire/pull/26) - @lolaodelola

Lola: Need reviews on this, only have Sarven at the moment. This adds an example for specifications that have excluded users in some kind of way. Used WebGPU as an example. Would need another person to review this language-wise (tone, etc.). Similar to the next PR. Any takers?
Jeffrey: I can look at this one.

### [societal-impact-questionnaire#24: Misuse example](https://github.com/w3ctag/societal-impact-questionnaire/pull/24) - @lolaodelola

Lola: Same here, similarly small change, adding an example for misuse, added the Web Speech API. Any takers? It’s only five lines.
Christian: Ok, will do it!
Jeffrey: I’m worried about this one, using Web Speech as an example. It’s true, but listing the microphone is handled the same way. Is this the feature you want to highlight? Or do you highlight something more subtle?
Lola: That might be harder to detect that this is a thing that could be misused?
Jeffrey: Yes, using Web Speech would signal that it wouldn’t be hard to think about this, as this is very obvious.
Lola: I have a list with other examples (https://github.com/w3ctag/societal-impact-questionnaire/issues/21)
Matthew: Have one that is very juicy and subtle. Compute Pressure API did a proof of concept where a side-channel attack was possible and you could send messages between tabs. They mitigated this, and the analysis and mitigation was super cool. … Will find the the part in the spec.
Jeffrey: I like that example.
Matthew: Will put the link there.
Lola: … (we should be clear about what is legitimate spec behavior, and what is potential misuse)
Jeffrey: The fact that Sarven wrote "that implementations adopt" at the end of this comment is if he thinks the implementation is the source of the misuse. I rather like to think of a website of the bad actor rather than the implementation.
Yves: If you find something in that regard, you should link the TAG finding [“Unsanctioned Tracking.”](https://www.w3.org/2001/tag/doc/unsanctioned-tracking/)
Lola: Would read this doc. We should link to it if the example has tracking implications. Other thing to consider, haven’t seen headings or subheadings that had more than one example, so I kept it like that. Think the example should be a) very obvious or b) tracking.
Jeffrey: Think that you should have an example that has tracking. The original Cookie spec had a section on potential cross-site tracking, that could be cited.

### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin, @csarven

Jeffrey: Waiting for Sarven to reply.

### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion (in A for Jeffrey & Max; in B for Jeffrey & Sarven; in C for Max & Sarven)

Jeffrey: This is being discussed at TPAC with the Web Payments group. Want Marcos and/or other TAG people to join the meeting.
Lola: I can ask Marcos in C.
Jeffrey: Thanks, and I don’t think there’s any update until TPAC.

### [design-reviews#1155: WG Revision: Screen Orientation](https://github.com/w3ctag/design-reviews/issues/1155) - @matatk, @christianliebel

Matthew: I like Christian's comment.

Christian: I'm satisfied. Very minor: 1) resolving the promise after the event is fired. 2) Hidden pages shouldn't be able to lock the orientation. Everything is fine.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://github.com/w3ctag/design-reviews/issues/1152) - @matatk

Matthew: Think it needs a bit more work. Will have another look.

### [design-reviews#1151: Other Spec Review: TCP Socket Pool per-Top-Level-Site](https://github.com/w3ctag/design-reviews/issues/1151) - @ylafon, @toreini, @lolaodelola

Lola: We closed this as too early earlier this week.

### [design-reviews#1147: WG New Spec: FedCM—Support Structured JSON Responses from IdPs](https://github.com/w3ctag/design-reviews/issues/1147) - @lolaodelola

Lola: Jeffrey proposed to close this, as it’s a minor thing and they’ve got the expertise for it. It is also so small that I don’t understand the benefit of a review. This essentially changes a property from a string to structured JSON data. They are changing it to accept both of which. Serialization/deserialization seems easy in JavaScript though.
Jeffrey: Think it is super minor. One reason we shouldn’t try to second-guess them. They talked to developers, they seem to be happy, so they should be able to make that change cheaply.
Lola: That was my inclination as well. @Jeffrey, what is the benefit to decline?
Jeffrey: Want them to improve the quality of the reviews.

### [design-reviews#1146: Incubation: Proofreader API](https://github.com/w3ctag/design-reviews/issues/1146) - @matatk, @toreini, @christianliebel

Christian: Didn’t have a look yet.
Matthew: Would need a little bit more time.

### [design-reviews#1150: [wg/json-ld] JSON-LD Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1150) - @csarven

Jeffrey: I think we can just close this. Will do that.

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @matatk, @dandclark

Matthew: This came up last week, didn’t it?
Jeffrey: Think we were supposed to resolve it, and then dropped it.
Matthew: Like your point about shipping the low-level thing second?
Christian: Which “thing”?
Jeffrey: They want a way to gain fine-grained control about how text is rendered. There is a high-level API which may allow assistive technology to see it. The low-level API only gives you the pieces to draw it yourself. We want them to do the high-level API first, and then the low-level API in case it is still needed.
Lola: What do we need for this?
Jeffrey: Matthew and I need to write a comment.
Lola: Sounds could be resolved as satisfied?
Jeffrey: No, it’s unsatisfied, as they are doing it in the wrong order.
Matthew: (…) HTML-in-canvas won’t help with that ever?
Jeffrey: There is a tiny change in API shape required for HTML-in-canvas to address this.
Lola: Is this the closing comment?
Jeffrey: Think so, but we should bring it back to the whole group.
Matthew: What do we do about i18n? If it doesn’t make a different, we could drop it.
Jeffrey: We should mention that. Maybe it changes our mind.
Matthew: Will draft an initial comment.

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @jyasskin, @marcoscaceres, @toreini (in A for Martin, Marcos, Jeffrey; in B for Jeffrey & Ehsan)

(Skipped)

### Logistics

Lola: Adjusted the meeting times for DST. Please double-check that it makes sense. Not meaning it is the most convenient for everybody. My methodology was that no one should have to join later than 12 AM.

### Issue Triage

(No issues to triage.)

## Breakout C (Europe / Asia / Australia) - [2025-10-16](https://www.timeanddate.com/worldclock/converter.html?iso=20251016T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Matthew, Christian, Xiaocheng, Lola, Ehsan, Marcos, Sarven 
    
Regrets:
    
Scribe: Matthew

### [prevent-credential-abuse#52: Add discrimination based on certain fields under Exclusion](https://github.com/w3ctag/prevent-credential-abuse/pull/52) - @csarven, @martinthomson

Sarven: I think this is good to go; it's assigned to Martin so he should make the call to merge it.

Hadlay: Can you drop a note in to the PR?

Hadley: ...unless the TAG bot works for discussions in PRs? Seems not, so please drop a note into the thread.

Sarven: Done.

### [user-agents#25: Add Audience section](https://github.com/w3ctag/user-agents/pull/25) - @csarven, @csarven, @marcoscaceres

Sarven: I revised it; it's assigned to Marcos. I lightened the section on regulators/policy-makers. The idea was to make it more understanding for those parties, rather than looking for specific criteria.

Marcos: I'd still like the order to be changed, but the text seems fine. Have proposed the edit.

Sarven: I'm fine with this. Anyone else? Yves, I think you mentioned something about order.

Yves: I said in the past that it might not be necessary to do this, but as there are explanations of what people will find in the document, it's fine. Happy with the new ordering.

Marcos: Approved.

Sarven: I think Jeffrey's OK with this; merging. Do we have a process on whether we are doing rebase and merge, or squashing?

Marcos, Hadley: Both.

Matthew: Squashes are nice as they condense the minutae of the PR development into one commit.

Marcos: Single commits are good.

Sarven: Squashed and merged.

Yves: What is seved from GitHub.io should be Editor's draft only. I can make a PR to modify this.

Marcos: GitHub pages appears correct now.

Yves: Ah, a couple of days ago it wasn't.

Hadley: Maybe we should keep an eye on this across our documents.

Yves: It applies to the societal impact questionnare.

### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @martinthomson, @csarven

Sarven: Mike West commented a couple of months ago; we need to come back to it. I can look at it in the coming week.

Hadley: Looking at the TAG bot, we discussed it last week, and were going to wait for Mozilla's comment to consider it. Jeffrey says he doesn't have strong opinions. Do we know anythign about Mozilla commenting?

Sarven: Looking back; I commented back in February. Long time ago. I think Martin, myself, and others need to discuss this. Not sure if the latest in the private thread reflects the latest in the public. We need to have a look at this.

Hadley: Could you put it into Slack to restart the converstion there?

Sarven: Yep, sure.

### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion (in A for Jeffrey & Max; in B for Jeffrey & Sarven; in C for Max & Sarven)

Lola: I put it in all breakouts because all participants are spread across the globe. Note for Marcos regarding this being scheduled at TPAC.

Hadley: Jeffrey notes that we need to send relevant people.

Marcos: This (Tuesday) appears to clash with my charing Web Platform WG. I'll see if I can attend on Monday.

Hadley: We shoudl let Web Payments WG know so they can arrange their agenda accordingly.

Marcos; Will ping Ian.

Hadley: ACK that they were hoping for Tuesday.

Marcos: May be able to share the chairing with the other chairs.

Hadley: Sarven: are you able to attend?

Sarven: I am interested, have signed up to everything so far; still planning.

Hadley: It's good to give chairs heads up by registering, it's not necessarily necessary - it is culturally OK for TAG members to attend the parts of meetings they need to.

Sarven: I'll do my best to drop in.

Hadley: There's scheduling info and a link from Ian on our thread (a couple of weeks ago). Woudl be kind to let them know, anyone, if you think you're going to attend. Everyone else interested is welcome to join the discussion.

Sarven: Will look at this.

Hadley: Given it's been a couple of weeks, it'd be great if we can confirm attendance in the next couple of days.

Maros: Have emailed Ian.

Hadley: Would also be helpful to put it in the issue so we can see it next time.

### [design-reviews#1148: Incubation: Preventing User Dictionary Leaks via ::spelling-error and ::grammar-error CSS Pseudo-Elements](https://github.com/w3ctag/design-reviews/issues/1148) - @ylafon, @xiaochengh

Xiaocheng: This proposal is about adding restrictions to the triggering of the spell checker to reduce leakage of user dictionary. I suggested the spell checker only be triggered by user actions, which seems like the right thing to do. As this is an early incubation review, I think that's sufficient. We can leave the exact wording to the future.

Yves: Xiaocheng wanted to close as 'validated' and I think we should close as 'satisfied' - completely agree on Xiaocheng's analysis.

Hadley: Who'll write the closing comment.

Xiaocheng: I reviewed the code too.

*Group is happy for Xiaocheng to post it*

Hadley: may be good to add that we're happy and looking forward to talking with them in the future.

### [design-reviews#1135: Incubation: Inline Integrity](https://github.com/w3ctag/design-reviews/issues/1135) - @toreini

Ehsan: Already validated and posted comment - it's an incubation, so we'll review it later (liked Xiaocheng's way of putting this). Do we wait for anything?

Hadley: Mike West said he's incorporated Jeffrey's comments. What else are we waiting for?

Ehsan: Don't think we're waiting for anything else.

Hadley: What's 'resolution: validated'?

Lola: There are some new resolutions. 'Validated' is for something that's very new, an early, idea, and we think it's good. 'Satisfied' is for more mature things under review.

Ehsan: Should we close it?

Hadley: Sounds like it - if you want to put another comment along the lines of Xiaocheng's about being happy to open a new one later, feel free, if you think it's worranted.

Ehsan: will do.

### [design-reviews#1156: WG Revision: CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/1156) - @lolaodelola, @xiaochengh

Xiaocheng: This is just about reviewing the changes after the spec has reached CRD. I listed the changes in the private thread. All of the changes look straightforward to me. I don't think there's anything contraversial here.

Matthew: Thanks for your comment - was helpful. I agree with your assessment.

Hadley: Sounds like we can close as satisfied.

Xiaocheng: will do

### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://github.com/w3ctag/design-reviews/issues/1140) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Marcos: Given it's a new paradigm that we'd be introducing to the web, I see a lot of issues with how it's specified right now - it needs a bit of work. I think we should discuss it at TPAC as a general model. It doesn't add a lot of value, and the mitigations that are in place are not implementable. But the underlying model has some merit. It's whether we continue on and pursue this path or not.

Hadley: They opened this in August. Are they OK with us waiting until TPAC?

Marcos: I think they have to be - they know this is a radical proposal. it's a pretty radical shift aware from the web's permission model. It solves for re-prompting but it doesn't solve for error recovery. If I haven installed web app, and the user denies the permission. On iOS it would not be possible to re-prompt if the user goes back to it later. You can't change OS-level permissioning. So from that perspective it's not implementable, at least on Apple's platforms. Some of the other issues I already outlined in the private thread. The utiltiy of the element is limited by the need to re-prompt when the user interacts with it. Also how they're using events is a bit confusion.

Hadley: Where at TPAC are we going to discuss this?

Marcos: Possibly in the DAS and Web Apps joint meeting. I can put on my TAG hat there. That seems the most efficient way. There are larger discussions around this - this has implications for the platform. Similar for the Web Install in Web Apps.

Marcos: For accessibility the promting is similar to how it is now. But in terms of UA considerations and the wider shift in the platform that it represents, it will be an interesting discussion.

Marcos: Discussion at TPAC: https://www.w3.org/events/meetings/4a477bab-4672-4d26-a890-49420725079f/
Wednesday
13 November 2025, 09:00–12:30 Japan Standard Time

### [design-reviews#1153: WG New Spec: Direction feature for `scroll-state()` query](https://github.com/w3ctag/design-reviews/issues/1153) - @matatk, @xiaochengh

Xiaocheng: This is about expsoing the current scroll state - whether you're scrolling up/down or scroll is currently snapped, so CSS can be done based on these factors. I think the use case is strong as it's a frequently-used design pattern. E.g. we want to show the header bar when scrolling in one direction, and hide it when scrolling in another. If you can do it in a declarative manner that'd be good. I didn't identify anything beyond the typical scope of concerns of CSS. The explainer already contains a lot of considerations such as whether we're exposing it via a container query or pseudo class.

Matthew: I haven't ben able to look at it in detail yet. Ome thing I would've been concerned about is if this is affecting anything other than presentation and it sounds like it's not. So I'd be ok with that.

Xiaocheng: Also, I'd like to confirm if there is any security/privacy considerations specific to this new feature. those sections in the spec are for the entire spec.

Another one, I'd like to discuss here. It's on eof those trendy, new CSS features that adds style dependency on layout. Some features are carefullly designed to avoid cyclic dependency, but others are more hand waving. Basic idea: i take a snappshot of the current layout and use that as input ot hte next styling. and there is a maximum number of retries if the layout doesn't stabilise. Something we should be aware of. 

Hadley: Seems like a good idea to raise the point. Are you saying that in this case there's a possibility of it but it won't actually happen.

Xiaocheng: Currently the responsibility to avoid the cycling dependences is left to the developer.

Hadley: Sounds like this gives us or them two choices: (1) redesign it so it's impossible to have cyclic dependencies; and (2) provide information for developers to help them avoid cyclic dependencies, e.g. mdoc warnings, comments. Not sure what would be useful for implementers. I think it's worth asking them the question about how to avoid developers making mistakes with this. We should ask them this and about the S&P section.

Lola: Matthew mentioed that his is presentation-only... are we sure? Is there a scenario where a screen reader user won't be able to access or interact with something they need to.

Matthew: That's a good question. I haven't looked at it in huge detail. I was reassured by Xiaocheng's comment. I know he's thorough and good at explaining things. Your question is really good, but I think this is providing a way for developers to do somethign they can already do. So the prolem you're describing is something that would exist right now. Maybe they shoudl put in a note to remind authors that "If you do this pattern, you have to be aware of certain things?" We could start that off and get APA to comment. It wouldn't change anything, but woudl let us raise awareness.

Lola: even if developers are doing the thing now, in a different way, that doesn't mean that some users aren't being excluded. and we woudln't want this to be a better way to exclude users. So I just wanted to raise that in case. If it's a non-issue...? I would be comforted if APA could have a look.

Matthew: I agree. We don't want to make it too easy to do a bad thing. I'm now wondering too about the cases where this might be a bad thing. Let's bring it to APA and look at where to put notes or warnings in for authors. I suspect it's not necessary, but it's a good opportunity to check.

Hadley: actions arising: Xiaocheng to draft a comment; Matthew to ask APA to look into authoring considerations.

### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Matthew: It was a long thread, we talked with the proponents, and we were much happier with this then. More recently, the form factor of XR headsets has been brought into the mix, and now we don't have conensus becasue it's the overloading issue again. 

Xiaocheng commented last week. It would be interesting if you could elaborate more. You can't make the same input across form factors or modalities, and we should concentrate on the semantics. I was wondering if you had more thoughts on it.

Xiaocheng: I looked at Anne's comment in the WebKit positions thread, and I don't buy it. I summarise his argument: the hovercard UI pattern is bad becasue we can't achieve the equivalent on touchscreen platforms. I think this is too much, trying to achieve equivalent UI patterns on all platforms.

I want to know what Marcos thinks.

Marcos: Not every platform has all those affordances, though this sets out to solve it for all platforms. The objections include privacy concerns for visionOS (we can't reveal where the user is looking); for touch screens it's trying to take over an affordance that's already part of the platform there (disrupting a system-level wide behavior for links - users have an expectiation about how it will work). We've already seen issues around preventing the default behaviour (such as pasting, or right-click - very annoying for users that sites can do that, and this is similar).

Right now we're a bit stuck because there's no solution for this on touchscreen platforms. Google has similar situation. Up to them what they decide to do, but those are Apple's objections.

Hadley: It sounds like there's a lot we're not going to get consensus on here. At some point we need to be able to say which bits we do and don't. It also sounds like there's something really important here on how we're dealing with different modalities that is going to probably come up as a design pattern and I wonder if there's something here that we should write. I wonder if it's part of the design principles or its own finding.

Matthew: there is a parallel here with WICG. An equitable user experience is not an equivalent one. WICG has protections in it that you can't remove content or functionality because you can see the user is on a small screen. There's more to discuss here. 

Hadley: How can we come back to the proponents at this point? Leave a comment saying we're still discussing this? We should say something to them. It's been three weeks. Marcos?

Marcos: Yep.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://github.com/w3ctag/design-reviews/issues/1136) - @toreini, @lolaodelola

### [design-reviews#1139: WG Revision: Dubbing and Audio description Profiles of TTML2 (for 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/1139) - @matatk

*Out of meeting note from Matthew: we said we'd close this - I have pinged on Slack about it*

### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola



### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) - @toreini



### [design-reviews-private-brainstorming#211: WebMCP Review](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/211) - @xiaochengh


