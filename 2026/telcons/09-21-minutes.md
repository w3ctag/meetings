# TAG Minutes — Week of 21 September 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/09-21-agenda.md).


## Plenary Session - [2026-09-22](https://www.timeanddate.com/worldclock/converter.html?iso=20260922T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attendees: Lola, Jeffrey, Christian, Marcos, Heather, Matthew, Luke, Yves, Hadley, Ehsan
Scribe: Heather

<!-- Agenda+ -->
### [process#52: Contact WGs to invite members to run for the TAG](https://github.com/w3ctag/process/issues/52)

Jeffrey: Heather has drafted text of a job description. We need text for an email to send to WGs chairs.

Lola: The list of WG chairs is long. Do we want to shorten it before we send it out.

Heather: There's a chairs mailing list? Let's send to that. When I put the list together, I realized that it was really challenging. No matching timezones. If we send to the chairs and say "let us know if you'd like us there. etc." We could put the job description on the TAG wiki/website, and refer to it, and just point to it. 

Lola: What if we had a breakout at TPAC where people could come to us who are potentially interested or who we think might be interested? Will the nomination period have started by then?

Jeffrey: Nominations will be open by TPAC. That sounds like a good idea.

Lola: I volunteer to make the breakout portion happen. 

Heather will handle putting the job description on the TAG website and mailing the chairs list. I expect to lean on Yves to help with that. 

Yves: It will be better to have it in the TAG space.


### Confirm next F2F dates of March 16–19, 2027 (Tuesday–Friday), in Karlsruhe, Germany.

Jeffrey: We have a proposal for date and location. We have agreement on those dates and location. 

<!-- Design Reviews -->
### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @ylafon, @marcoscaceres, @christianliebel, @lukewarlow

Christian: This is the third iteration of the web install proposal. It has the element, the imperitive, navigator.install. Now instead of pointing to a document you point to a manifest URL. We have encouraged them to think about the same doc use case, and we said unsatisfied for the third-party install use case. I suggest is that we say the same thing we said last time: continue to explore the same-origin use case and after that, look at the third-party thing. They will do third-party work anyway, but we will be on record with our advice.

Marcos: Since the TAG has met with them, our energy is better spent on a finding. I don't think we should go around with circles with the group. We could also meet with them at TPAC.

Jeffrey: Is Christian in charge of starting the finding on web install? 

Christian: Yes. I have created the repo and will be creating the draft. 

Jeffrey: So the TAG's next step is to focus on the draft finding and not the design review?

Christian: I think we can do both.

Lola: Is this a good candidate to decline the review since we've done this review?

Luke: I agree with that. We might write a finding, and we can use the review as an opportunity to share that finding. But we can decline the review and share the finding through other mechanisms. 

Christian in chat: 
    v1.0: https://github.com/w3ctag/design-reviews/issues/888, https://github.com/w3ctag/design-reviews/issues/946 
    v2.0: https://github.com/w3ctag/design-reviews/issues/1051 
    v3.0: https://github.com/w3ctag/design-reviews/issues/1245

Marcos: I agree with the suggestion to decline the review.

Christian: I agree with declining the review and point to the previous design reviews we've done, and point to the finding, and actual feedback on the design around the manifest. I can do that in one comment. 

Jeffrey: Christian will draft the comment and we'll review at a future meeting.

Luke: The manifest URL being required is interesting. Others have done something like this in the past and some have backed it out. You can do things with the manifest that you can't do otherwise. Android's API at https://developer.android.com/reference/kotlin/android/content/pm/webapp/WebAppManager does require a manifest.

Yves: We discussed the manifest at the face to face. Treating all web pages as installable by default is an interesting decision.

Jeffrey: Allowing users to install any website, but if the developer wants to control it they should provide a manifest. But let's look at what Christian writes and see if we agree.

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Christian: Design review is stalled; they are waiting for our response. The philosophical difference is whether you think introducing this additional agentic layer which is invisible to users is a good idea or not. You can have a staticly typed interface between the LLM and the website, which can be of benefit to developers. The other view being that this is not great because you can't see it and the AI model should understand the existing DOM and accessibility tree, so instead we should focus on any necessary changes to the existing tools. My recommendation is to say no consensus and outline the pros and cons for the different perspectives.

Marcos: I would like us to reach consensus on it without getting in the weeds about the solution. This is the first cut at a significant evolution of the web. It would be more valuable to take it as a first cut. The permissioning layer is still missing, for example, and the people working on it know that. We don't have agreement in the TAG because no one is bound to a specific solution.

Hadley: Regarding the process, it's fine to do what Christian suggested. But also, there is a lot of momentum behind this and some see this is as the W3C's opportunity to impact/direct AI's influence on the web. We (the TAG) have the ability to influence things now and should take advantage of that.

Jeffrey: I've spoken with Phillipe who are very concerned if the TAG says only "we don't like this." I see some disagreement about whether to do WebMCP or extend HTML semantics. We've pushed for the latter, a declarative version, and they experimented with it and think the imperitive model is the way to go. That fits with the Extensible Web Manifesto. We could then add the "winning" semantics to HTML as a declarative form. 

Matthew: Which is interesting. APA asked for the opposite: https://github.com/webmachinelearning/webmcp/issues/65#issuecomment-5440638117. The concerns were about primarily the fragmentation this might cause. The spec says this is a way to have humans and agents to collaborate on the web, but the spec is not that. It informs the agent and the user never sees any of it. We had other concerns as well that Marcos mentioned around privacy and security. There has been interesting engagement from the group in response to this comment. We do need to help influence this in the right direction, and right now we don't agree on what that direction is. We should work on that.

Luke: Saying we don't have consensus on the overall solution of having agents on an interactive website is fine. But we can still get into further detail about the declaritive vs imperative models. We can highlight the potential problems and encourage them to keep within the permission model for the web. From a philosophical point of view of people are pushing for it so we should support the direction, I think we should be able to push back. But we don't collectively disagree with the premise. We need to find as much common ground to the comment as possible. If the imperative was based around the HTML, you'd avoid things like the screen reader getting something different than the what others see.

Hadley: To be clear, I think it will happen despite us, if we say it shouldn't. I wasn't saying we should support the direction because there is momentum there. We shouldn't back down on our opinions because of what other people want.

Marcos: That it will happen doesn't mean that WebMCP will happen. There are other solutions potentially in the works here. This is a system where prompting is used to prime the models that are being targeted, so there is a risk to overfitting to specific LLMs. There is a new risky area here because of the way it is designed. It requires natural language, and that natural language is geared towards a specific model. And if you look at the example Christian showed at the developer meetup, he had put prompt constraints that should have been in HTML (e.g., min/max). That's a break in HTML. If you give JavaScript developers a Javascript API, they will use it. Safari, Chrome, Firefox, each have an MCP. There is a format emerging for a longtail of web pages that need to work with agents. There is going to be a breakout or possibly a mini-workshop at TPAC.

Christian: I agree with all of this and it's why I think we should say "no consensus". It's something in between saying it's a great idea and it's a terrible idea, and we should be clear about that in between. I don't think we're saying anything new at this point and we should come up with a closing comment.

Jeffrey: I think we have consensus on many things, e.g., accessibility, and we have some agreement that we should try to direct them rather than stop them. We can focus on where we have consensus, and end with "we didn't come to agreement if this is the correct first step." Phillipe is trying to put together a working group to focus on helping web pages communicate with agentic browsers. That working group would be a good place to hold the conversations Marcos' mentioned. I have heard there are people working on standardizing tool descriptions. E-commerce seems to be a good example, Initially, it will be people focusing on which tool descriptions result in models doing the widest range of things. We might include that as a future direction.

Matthew: I want to make sure that Ehsan's comments went into the minute, that they do not cite the ethical web principles for machine learnings in the spec. Christian asked about i18n, and I don't know what feedback they've already gotten from that review. I agree with Marcos that they aren't trying to bring the web along via consensus.

Lola: Nick Doty, Privacy IG chair, has also opened issues on the WebMCP GitHub. See in particular https://github.com/webmachinelearning/webmcp/issues/313 which states they haven't provided any mitigations to some of the security and privacy issues. 

Jeffrey: We have a lot of things to put into a comment. We need to draft it and see what has consensus and where we can express that. I think there is a lot, even if the final conclusion doesn't have consensus. Next steps: Christian will draft a comment, but he could use help. 

Marcos: I'm happy to help. Can we set up a few hours to discuss?

Ehsan: I am happy to join. I think we should have a deadline by which we'll have a draft ready. 

Christian: I will schedule something.

Hadley: I am also happy to participate, but don't block on me. 

### Ethics CG

Lola: Want to collaborate on societal impact questionnaire.

Jeffrey: Yes we can do this.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

#### [Question: Architectural issue: local path hijacking and cloud sync lock-in vs user agency](https://github.com/w3ctag/design-reviews/issues/1272)

Jeffrey: Suggesting we decline this as out-of-scope.

Heather will draft.

#### Add keyword "pair" to scroll-snap-type for snapping to the same element in X and Y axes

Jeffrey to decline this async.

#### VCALM v1.0

Heather and Hadley

#### SVG textPath side attribute

Inclined to decline, but will give the rest of the TAG a couple days to look.

#### PrivacyWG

Big diff, but says no substantive changes. We'll probably decline or say "yay, keep doing things."

## Pacific Breakout (Asia / Australia / West America) - [2026-09-23](https://www.timeanddate.com/worldclock/converter.html?iso=20260923T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

<!-- Agenda+ -->
### [design-reviews-private-brainstorming#302: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/302)

Brian seems to have the strongest TAG opinions. There's a WHATWG issue at https://github.com/whatwg/html/issues/12775 with no discussion. PrivacyWG might have opinions.

Heather: Related to private browsing mode? Should this also be a browser choice?

Jeffrey: Hm. This is a switch that changes the overall threat model, so maybe browsers could use the help.

Dan: https://explore.microsoft.com/en-us/edge/features/enhanced-security-mode?form=MT0160 is related. Turns off WebGPU, JS JIT'ing. 

Jeffrey: We should mention Enhanced Security Mode in the Private Browsing Finding update.

Jeffrey: Kick it back to the browsers and ask them to figure out what their users mean with this setting?

Dan: What are users thinking? With ESM, enterprise handling sensitive data, or journalist being targeted by nation-state. Not sure about disabling scripting. With ESM, much of the web will still work. With scripting, much of the web will break. 

Jeffrey: Lots of people want this for dramatically simplifying pages. Not necessarily a threat model question.

Heather: Ask them to do the homework, and see what the browsers actually do. Is the browser behavior setting a user expectation?



<!-- PRs -->
### [design-principles#621: Add new fragment directive guidance](https://github.com/w3ctag/design-principles/pull/621) - @tabatkins

Jeffrey: This might be waiting on @tabatkins to update based on comments from last week. In general, I think we want this.

Dan: Agreed.

Jeffrey: I will reach out to the three Googlers most likely to have answers to my questions.

### [user-agents#63: Scope the arbitrary-content claim to the public web](https://github.com/w3ctag/user-agents/pull/63) - @marcoscaceres

Jeffrey: Still in my court to review. 

<!-- Design Reviews -->
### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

Heather: I'm ok with the response. Leaning toward satisfied.

Dan: I looked at it, and didn't see a reason to be concerned.

Will check with Marcos via Slack.

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

Will come back to this once Heather's reviewed the proponents' response.

### [design-reviews#1251: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1251) ([Github](https://github.com/w3ctag/design-reviews/issues/1251)) - @jugglinmike, @marcoscaceres, @bkardell

<skip>

### [design-reviews#1224: Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1224) ([Github](https://github.com/w3ctag/design-reviews/issues/1224)) - @hlflanagan, @xiaochengh

Jeffrey: Since we started this review, we should finish it. I'll develop an opinion.

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Need Marcos to discuss this.


## Atlantic Breakout (America / Europe) - [2026-09-23](https://www.timeanddate.com/worldclock/converter.html?iso=20260923T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

<!-- Agenda+ -->
### [user-agents#6: A duty of Negotiation](https://github.com/w3ctag/user-agents/issues/6)

Jeffrey: I see Heather's suggestion. Makes sense, but I haven't done anything about it.

### [design-reviews-private-brainstorming#217: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217) - @csarven

Sarven's on vacation. Do we wait?

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

Enough PRs out; they need review.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Matthew: Remembering the F2F ... ADRs? We mention them as an option. No appetite to promote them more. 

<!-- PRs -->
### [design-principles#628: Add the improve-existing principle](https://github.com/w3ctag/design-principles/pull/628) - @csarven

Jeffrey: I need to review in detail. It at least needs to merge duplicate parts of the sections it generalizes.

### [user-agents#66: Add an EME example of making credible commitments.](https://github.com/w3ctag/user-agents/pull/66) - @jyasskin, @hlflanagan, @npdoty, @csarven

Jeffrey: Haven't gotten to this yet.

Heather: Don't know if Nick is suggesting a change to the PR. 

Jeffrey: I think he is suggesting that I'm thinking about it wrong. He doesn't have any concrete suggestions. There is still some disagreement about whether EME was a good idea. This pull request says "it was a good idea," but maybe we don't want to say that. Maybe we want to take Sarvin's comment and leave it as an abstract principle without endorsing EME

Yves: Considering the history, it migth be better to be more abstract here.

Lola: What is this an example for?

Jeffrey: You can open up the wider document (there should be a preview link in the original comment). The idea is that--the user has downloaded a video from Netflix, and now,t hey want to save it to watch later. A User-agent that is loyal to the user would help them with that task, and [reventing them is disloyal. The user-agent can be loyal the user's entire existence. In being loyal to the user's entire existence, it needs to help them download the video in the first place.

Jeffrey: The argument is that user-agent should have driven a harder bargain. This relates to the negotiation duty that we discussed earlier. It's always going to be controversial when UAs make one of these bargains. Nick's point is about UAs bargaining collectively for their uesers, and NOT about bargaining for any single user. Maybe EME is actually an example of something else, not the "longer existence" loyalty.

Dan: When was this principle originally written? Is there anyother example?

Jeffrey: EME was what I was thinking of when I wrote the "credible committment" text. I don't know if there are other examples of this kind of loyalty.

Dan: Some of the third-party cookie stuff comes to mind, which TAG has been opposed to.

Jeffrey: Right--that's again a collective-bargaining kind of thing. This is why I'm interested in potentially re-draft. I'm not convinced we actually want to avoid controversy.

Lola: Do you think this version of TAG could come to a consensus?

Jeffrey: I haven't heard anyone here say that EME was a bad idea. I'd be curious to hear from anyone who does.

Lola: I'm not convinced EME was a good idea. Whether it was a bad idea is another issue, maybe. Do you think this would make a good discussion for plenary?

Jeffrey: I could bring it up in two weeks. That would give me time to prepare.

Dan: Do think about Attribution Reporting in drafting this.



### [user-agents#67: Clarify credible commitment](https://github.com/w3ctag/user-agents/pull/67) - @csarven

Jeffrey: I think this is ready to merge


### [user-agents#70: Focus only on web user agents.](https://github.com/w3ctag/user-agents/pull/70) - @jyasskin, @marcoscaceres, @bkardell

Jeffrey: Sarvin asked if we wanted to move the short name back to just "user agents". I changed the title from "Web user agents" to "user agents", and the document stops saying "web user agents" in most cases. I am happy with either shortname.

Lola: I think there should be consistency, but I'm happy with each

Yves: I'm not bothered by it, but maybe the webmaster

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

Matthew: this is pending external feedback, but I don't know if that feedback is coming. I was quite interested in finding out what David wanted to propose because I think it is kind of interesting. For new things, we have a "private by default" principle, so the idea of it is quite attractive. I just didn't want to bias things. We could ping again, I guess, in case he's forgotten about it.

Jeffrey: I will ping David and pick it up next week

<!-- Design Reviews -->
### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Heather: Martin got back to us with War&Peace. Very long. I haven't gotten through all of it.

Brian: Our feedback wasn't short either.

Ehsan: I saw Martin and discussed briefly. Last paragraph summarized what he thinks. "It's hard, but better than zero-sum solutions." I kinda agree. In Privacy WG we discussed extensively. Had architectural concerns, but majority were focused on usability. We didn't mention usability much in our feedback. Do we want to coordinate with Privacy on that? I think it's a good thing in general, despite its disadvantages.

Lola: Those assigned can iterate on it.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Lola: Should we keep this on the agenda?

Brian: Take it off for now.

### [design-reviews#1265: WG New Spec: Global Privacy Control (GPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1265) ([Github](https://github.com/w3ctag/design-reviews/issues/1265)) - @hadleybeeman, @toreini, @hlflanagan, @lolaodelola

Ehsan: I posted a draft comment. Included Heather's comment. I added a bit about them covering private browsing.

Jeffrey:  The GPC is very focused on the specific American laws that say "do not sell or share," and it's not very well-focused on the European laws. I told them that they ought to architect it so that it can incorporate other privacy practices, adn they did not take that advice. There's another [MISSING REFERENCE] that is that flexible, but is maybe*too* flexible. I thin kwe want something in between: the syntax of ADPR (https://www.dataprotectioncontrol.org/spec/) and the semenatics defined in another specification. If the rest of the TAG wants to say the same thing, then that's fine, but I'm not going to insist on it because I've already had my say.

Jeffrey: I don't think Do Not Track had a more flexible syntax, but I'm not sure: https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/DNT

Lola: I support getting them to work with the ADPR folks. I was ollowing this a long time ago, so I'm not sure what's changed in the time since. At the time, it was not just American-focued but specifically California-focused. They acknowledged that they needed to think about GDPR, but that was six years ago, so it's kind of disappointing.

### [design-reviews#1254: Incubation: Cross-Origin Storage](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1254) ([Github](https://github.com/w3ctag/design-reviews/issues/1254)) - @ylafon, @bkardell, @dandclark

Yves: Saw Christian's answer about 3p cookies. It's still doesn't address the fact that you can store things and use the presence to exchange data between site. Maybe having a fixed list, and not updateable, might be a good solution. Curating the list is even more important in that case.

Dan: There are some very different types of things proposed to be in here. Common libraries like React, or Google Fonts, might give very little information. Game engines, AI models, might give more information. The cross-origin thing is a legitimate concern. Explainer might address how AI models used by few people interact with libraries used by a lot. How can browsers limit the number of requests people make into the registry to limit the amount of information they can gather. This makes a lot of sense ... is there a core that would be possible? Chrome already does something like this with "cache sharing for pervasive resources". Can something like this be standardized, with better privacy guarantees?

Lola: How does this differ from shared storage access? https://developer.mozilla.org/en-US/docs/Web/API/Storage_Access_API A way for cross-site content, in 3p content, to gain access to unpartitioned state that would be available in the 1p context.

Christian: Scope is different because this isn't about cookies and small information, or the iframe boundary, but about sharing large dependencies used by multiple sites across different contexts.

Lola: Storage Access wouldn't be able to be extended to accept bigger resources?

Christian: Not sure; please add it to the brainstorming comment.

Jeffrey: Storage Access gives a third-party iframe access to its first-party sotrage. If it has access to the same iframe as some other iframe, that is not shared. Cross-origin storage is meant to share somethign that is byte-identical across different origins. I think they're different enough to have separate APIs.

Brian: Things they're proposing to be able to do, are pretty different. Not just a JS API or an attribute. Here's how you can make a local proxy/cache and use it through script include, CSS, etc. A lot more dicey than some other things you could do.

Yves: cache with preemptive deduplication

### [design-reviews#1246: WG New Spec: Additional Windowing Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1246) ([Github](https://github.com/w3ctag/design-reviews/issues/1246)) - @jugglinmike, @bkardell

Mike: Some unbaked comments: availability of an API to disallow the window from being resized ... might be naive, but a bit related to Jeffrey's discussion earlier, where the UA denies an ability to the user. Is that really desirable? 

Brian: Going to the whole-web vs platform discussion: for embedded things this is much more plausible since you'd be deploying on a fixed interface. Every browser has a kiosk mode that's not resizeable. Don't think this fits in the drive-by web.

Lola: Mike, please post your draft comments.

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

Matthew: Overall, Florian addressed all the accessibility concerns. They took out bits that would involve doing focusability in CSS, which we felt icky about. There's still a proposal to have image with a controls HTML attribute, but that's not an issue since the controls would be understandably-focusable. One unresolved thing: Adrian Roselli's comment about conveying role states to platform accessibility APIs. Would really need to happen to make this admissable. If it doesn't happen, some people won't know whether images are playing.

Lola: WIll you leave that as a review?

Matthew: As it is now, 'satisfied with concerns', pointing to Adrian's issue. Last discussion was 2 weeks ago? Has been some spec clarification. Still needs to be a mapping. Know they're working on the CSS/Accessibility API mappings, but it's not implemented yet. Needs to be resolved, but would be need it to be resolved before we're happy with it shipping. "Satisfied with big concerns". Feedback from Florian is good. Don't think we have a problem with it as a whole.

Jeffrey: If there's a piece that we think needs to be done before it ships, but we're expecting to be satisfied after that, I think it makes snese to make the whole thing as "unsatisfied" along with a comment that clearly states, "when this is done, let as know, and we will change it to "satisfied."

Lola: Matthew mentioned the CSS/AAM. They need funding.

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

Jeffrey: There was some discussion on this in August. I will review, and we can revisit it next week.

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242)) - @matatk, @christianliebel

Christian: Have a draft comment that Matthew +1'ed. I'll post that.

### [design-reviews#1264: Incubation: Filterable select](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1264) ([Github](https://github.com/w3ctag/design-reviews/issues/1264)) - @matatk, @dandclark

Dan: We wrote a response. 3 options they're juggling for how to do it, and I'm undecided which is best. Lightly endorsed one in the response. They're already engaging developers. I could be pretty easily persuaded to endorse another option, but haven't been persuaded yet.

Lola: You'll post your comment

Dan: With the accessibility note from matthew. Won't close the review, since I'm still asking some questions.

### [design-reviews#1253: Other Spec Review: CSS navigation-based styling](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1253) ([Github](https://github.com/w3ctag/design-reviews/issues/1253)) - @matatk, @dandclark

Dan: I posted some surface-level thoughts. One more-important question about cross-origin navigations. Want other thoughts, but can ask the clarifying questions. Matthew asked about accessibility, and Noam added an accessibility section. Would love your thoughts.

Matthew: I looked, and it doesn't render properly, but I think I get the gist. The spec states that the purpose of providing the transition animation is to make it easier to understand what's going on, and I'm wondering if there's anything semantic that needs to be conveyed that wouldn't be part of the structure of the page. I think there probably isn't. No major concerns or objections given their addition.

Lola: Think someone else should give this a once-or-twice-over. Not hearing volunteers. Please do look over Dan's comment.

### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini



### [design-reviews#1249: WG New Spec: Recognized Entities v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1249) ([Github](https://github.com/w3ctag/design-reviews/issues/1249)) - @hadleybeeman, @hlflanagan

Heather: I've added comments. Waiting on Hadley to see what she thinks.

### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

Heather: I like Ehsan's revised comments. He asked if he was the one to post it given he isn't an official TAG member or whether I should do it?

Lola: Heather should post.

Heather: Then do I close it?

Yves: If we don't expect a reply, it's good to close. They can reopen if they have questions.

Jeffrey: If we want to pursue them doing anything, we might want to do more than ether closing it or leaving it open. We might want to file bugs in their repository.

Lola:: Littledan opened this after speaking to me in Spain. They've had timelines that we've missed. They've posted this partially in good faith. Littledan was quite disappointed that there wasn't TAG input, and it seems like there were political things (outside of anyone in this call) about why this didn't happen. Posting this in their repo to say, "this is what we've come to," is a good idea. They can leave it at that if they wish.

Ehsan: I remember Simone was leading CRA conversations at some point. Need to have a consistent channel.

Lola: yes.

Jeffrey: I would have Heather post on their repository and say, "As a representative of the TAG [...]"

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow



### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven



### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon



### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk



### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini




## Eurasia Breakout (Europe / Asia / Australia) - [2026-09-24](https://www.timeanddate.com/worldclock/converter.html?iso=20260924T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Matthew, Luke, Lola, Ehsan, Christian, Yves, Marcos

Regrets: Hadley

Chair: Christian

Scribe: Marcos

<!-- Agenda+ -->
### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: waiting for the proponents. Gave the a nudge yesterday. That's all we are waiting on. 

Yves: I think the Chairs are out next week, so we might not hear back. But will ping them. Part of the comments were addressed in the PR. 

Ehsan: that would be great. They were editorials comments, but otherwisse all issues are addressed so should be fast to conclude. 


### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: I've unassigned myself from this. This is a parent issue, but I've added two additional issues. A while a go we took some feeback from other folks. However, I'll be focusing on some other sociatal impact issues that I'll be focusing on. 

Christian: should we close this? 

Lola: yes, let's leave it open. 


### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

(Skip)

<!-- PRs -->
### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan

Christian: this is what we discussed at the face to face. It seems close to merge this soon. It would be good to have Marcos and Dan to review it. For cotext, this adds guiadance for specifications authors and how they might write specs to deal with the various modes. 

### [user-agents#68: Fix spelling and enhance user agent descriptions](https://github.com/w3ctag/user-agents/pull/68) - @marcoscaceres

*skip*

### [user-agents#65: Drop the user activation claim from the multiple permissions example](https://github.com/w3ctag/user-agents/pull/65) - @marcoscaceres

*skip*

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

Christian: this is also from the face to face. This is in review. Marcos created it, it looks good so far. We will continue to review. 

Marcos: We are planning to merge this soon, then experiment with changes by comparing output. It's early at this point, but it's a good start. We need to merge it in order to be able to iterate on it.

Christian: Ok, will look at it again so we can close this soon and try it out.

<!-- Design Reviews -->
### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh

Matthew: there was some recent activity on this. They came back with more input in August. Largely Sarah and Robert have been commenting on that. On the TAG side, we still need to look at this more to reach consensus. There's the potential that this is changing the role/behavior, which may be problematic. There still ongoing work... like sematics created in CSS that can't be overriden in HTML remains unsolved. We need to look at the acccssible name created for scroll markers... this might cause i18n issues, so we should reach out to the i18n community about this.  

Lola: I'm going to take a different position. We've been working on this for over a year, and I think we've contributed and spent a lot of the TAG's time to this. However, we probably shouldn't be co-designing it. It's great that they are working on it and making progress, but they should really talk to the i18n folks and a11y community etc. We should really mark this as "disatified" at this point?

Luke: from day 1 this feature has been somewhat problematic. There's been a lot of workarounds and addressing concerns as they were raised. And it's been good to see how things get addressed, but it's somewhat problematic that they are addressing some of theses things in CSS instead of HTML - so there's might be some architectural misalignments. Given how many issues, I agree with Lola that maybe we can leave it and say we are disatified and say we should leave it for now. 

Matthew: I share Lola's concerns and Luke has articulated things well. Asking constructive questions might help them find alternative solutions to how to solve this problem. The TAG is very close to proposing helpful questions that might help them move along... however, there might be some deadends that they might need to reconsider. I'd like to look at how involved they have been with ARIA. At the same time, we should say we are unsatified until various things have been addressed. 

Luke: I think going about it in the way described makes sense, but it's challenging because it's shipped early in Chrome. It could be problematic that this is out in public. But it's been something we've been looking at this since 2025, so it might be time to wrap up this from the TAG side and leave them to continue forward on their own. 

Christian: I like Mathews idea that we should help them where we can, but also agreeing with Lola that we should wrap up this work by the end of the year.

Matthew: should I draft a closing comment and give them a bit more time? 

Christian: Looking at the dicussion here, I think it should be a closing comment. 

Lola: that sounds good. 

Matthew: I've got some text already set to go. 

Christian: ok, good. 

### [design-reviews#1275: [wg/lws] Linked Web Storage Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1275) ([Github](https://github.com/w3ctag/design-reviews/issues/1275)) - @csarven, @marcoscaceres

(Skip.)

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Yves: I'm working on making the sitiuation better. I should probably add myself to this issue as I'm working on it. Making some progress on it. 

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

Luke: after the discussion on tuesday, I'll leave a comment marking this as satified. 

### [design-reviews#1263: WG New Spec: Verifiable Credential Barcodes v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1263) ([Github](https://github.com/w3ctag/design-reviews/issues/1263)) - @hadleybeeman, @toreini

Ehsan: I have drafted some questions, specially around cross origin leakage this might have and their threat model. I'm waiting for Hadley to have a look also. I've only have questions at this point. No decisions. 

Matthew: out of interest, this came up in APA. We don't have any advice on this, but it would be good to have general advice on this. 

Marcos: In Digital Credentials, when you do cross-device, we show a QR code, and there is some guidance on the WebKit/Chrome/Apple Wallet side, which might help here a little bit. There’s an open issue that has examples around this. We try to communicate a lot of information there, e.g. multiple origins, QR codes, … can be overwhelming. Hope I did a good job at it! Happy to chat.

Luke: browsers have looked at this also in Web Authn. For the varifieable credentials bar codes, is there a way of doing this with NFC tags? It might be a way of doing this with NFC instead of barcodes. It's physical stuff, if you can do it with NFC and it might be easier? 

Marcos: Thing with barcodes is that you can print them out and stick them on top of the other bar code. All depends on the thread model. But possible for NFC as well.

Ehsan: Wouldn’t this apply to passports, driver licences, etc. as well?

Marcos: this is a fun security rabbithole we probably don't need to go down right now :) 

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh, @lukewarlow

Luke: I've looked at this. I'm satified as far as I understand this problem space. But i'm not sure I'm qualified enough to give an fully informed postion on it. But I'm not sure if we should just close it with satified or if other TAG members should look into it before we close it out.   

Christian: do we have additional volunteers? it would be great to have someone else look at it. 

🦗

Luke: it seems quite well thought out. I'm fairly confident it's ok. It was also presented at a conference rencently. There'e been no feedback from Mozilla or WebKit, but not sure if that's a problem.  

Christian: generally we can just leave a comment saying that there hasn't been multiple stakeholder support. 

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Christian: this has been open for a while already. 

Matthew: there was some developments with it... I have some draft feedback that I haven't posted yet. We got some answers to xiaocheng's questions. About the a11y issues, we got some responses but I need to check their feedback. We also asked about the text-matrix issues we've been seeing... at web engines hackfest there was discussion about how to potentially fix this. It would be good if they could discuss the and acknowledge the text-matrix issues and potentially spamming the a11y tree. In any case, I'll take a closer look at where things are at. 

Lola: we have been looking this for a long time, this group has been very actively engaged with ARIA. There are a lot of things amongst themselves that they need to work out. Specially around things that are drawn to the canvas but not in the a11y tree. There is still active discussion in their issue threads. But still unsure how much more the TAG should spend on it, and leave it to them to go forward and continue developing this.

Christian: so what do you propose as a resolution? 

Lola: Propose closing, it could be that we are ambivalent on it. 

Luke: I think giving them a bit more time might be good... it has actively involved. There was feedback from webkit and they have been responsive. It might be good to maybe put this on hold but asks them to come back once they've addressed some core issues. But it feels close to having an answer, even if it's potentially not the ideal architectural solution. But it would be good to pause and ask them to come back in the future once they have made more progress. With regards to the text-metrics, it would be good to ask them about it. It would be good to consolidate a solution instead of having multiple ways of doing things. Next steps is maybe Matthew share his comments with the TAG and we can send those out and then decide if we pause it or not. 

Christian: that sound good, specially because it's been open for 2 years.  

### [design-reviews#1250: Incubation: WebRTC Diagnostic Logging](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1250) ([Github](https://github.com/w3ctag/design-reviews/issues/1250)) - @lolaodelola

Lola: I reviewed this 3 weeks ago. I left some internal comments for us to consider. I had mostly editorial feedback at this point. There's some contradictory statements between the explainer and the spec and the spec should have normative language preventing things from being exposed. The conformance section points to RFC2119, but then they say that they are in lowercase. This could be confusing. 

Luke: the things in this API are somewhat noble... there is no other API where the API may or may not do something. This might not be a JavaScript userland problem. 

Lola: I don't disagree. WebRTC is somewhat unique and does things that other web platform features don't do. However, we should draft some comment.  

Marcos: Lola, that quirky thing is also across HTML and WHATWG specs. There’s another RFC that allows that. But definitely quirky.

Lola: If you can find that RFC, that would be interesting!

### [design-reviews#1256: [wg/immersive-web] Immersive Web WG 2026 Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1256) ([Github](https://github.com/w3ctag/design-reviews/issues/1256)) - @matatk



### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres



### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola



### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Private thread comment to sum up where I'm intending to go with the closing comment): https://github.com/w3ctag/design-reviews-private-brainstorming/issues/176#issuecomment-5811202052 - if you could indicate whether that direction seems good (or not) I'll propose a revised comment.


