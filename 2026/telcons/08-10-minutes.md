# TAG meetings, week of 10 August 2026

## Plenary Session - [2026-08-11]

Chair: Heather

Attending: Heather, Marcos, Hadley, Lola, Christian, Sarven

Scribe: Sarven

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-10-minutes.md

Raw minutes: ...
(https://www.timeanddate.com/worldclock/converter.html?iso=20260811T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Next steps for WebMCP (meetings)

Lola: Have some notes to share for those that are considering to attend the next WebMCP

Christian: We should review the last minutes and go from there.

Matthew: Would like a debrief with those interested.

### [design-reviews-private-brainstorming#284: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) 

Heather: There was a discussion but we didn't put a draft together. Does anyone think it should go forward or with forward with specific changes?

Brian: Essan and I made some points. This is an interesting/complex thing that I'd like to understand better. Invited Martin to ??? podcast. Happy to share a rough draft this week if anyone wants to listen to it.

Hadley: Keen to know how the discussion goes.

Heather: Any feedback requesting for a proper explainer?

Brian: Only that they'd take it under consideration. Issue originally opened by ??? Not technically required by the process so doesn't block anything.

Heather: We can do the review. They did request a review so they should ideally make it easier for us.

Lola: Doesn't sound like this is something we are satisfied with. Sounds like this is probably an unsatisfied but would like to also flag that there are conversation that are ongoing, like in Privacy. No pressure to have an answer, but if we want to close this it'd be unsatisfied right now, but could give more time to deliberate longer.

Hadley: I think it is not unreasonable for us to burn more energy until a template they put together. A closing review like Lola described.

Brian: Mozilla doesn't have a standards position on this yet, which is kind of interesting.

Matthew: I think we should ask for it and they should give. There was this big problem that people are doing on the web , like cookies and it wasn't private, and this is a balance (which can be controversial. AFAICT, there was internal agreement from browsers but not a standards position released. We could do with that information. Worth pursuing that and asking for things we'd normally expect. If they reached a strike, it'd be ok to review, but there are question marks. This is a lot of work over a long time. We should encourage them so that we could review.

Hadley: Not against that. There are two architectural points that'd be good to get feedback. 1) user-agent surving the advertise, and I think that massively violates duties and PoC. 2) Effectively it is a cross-origin leakage, and so I'm concerned.

Brian: Some background on user benefits etc are in the spec. In prose and diagrams. Value in an explainer. Could tell them they have a lot of the information already but they need to put out more clearly. It is not cross-origin leakage. They're careful about that. Some things can be done / some debate on to what degree, but there are not a tonne of players in the space. This is kind of a mash of some orgs..  worth digging into where people with different background on designing something that fits. It'd be interesting to learn more.

Heather: We could invite them to one of our meetings. Not a replacement for an Explainer. Essentially we don't have enough information to settle so lets find out.


### [design-reviews-private-brainstorming#302: Question: can we better define the intention of the "disable scripting" user preference ](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1247)

Marcos: Seems like we should defer to the HTML group. interested in discussions from the HTML side.

Lola: Agree to certain extent. But don't want to completely defer / not participate because it ultimately affects WebArch. We should have folks from TAG participating in those discussions.

Marcos: Struggle to agree. When e.g. scripting is disabled is a larger discussion which could be a design principle. This is similar to when it is BFcache. 

Hadley: So, what we do within our realm, and the other is Dominique's question. I wouldn't want us to get lost in formally in our body of work in the expense of a concrete bounded question.

Sarven: If it is not out of our scope, we should respond.

Marcos: They should Initiate a discussion on the WHATWG and other potential features affected by disabling a script.

Hadley Do we not have more to say?

Heather: Marcos could you write that up?

Marcos: Ack. Done:
https://github.com/w3ctag/design-reviews/issues/1247#issuecomment-5254012945


### [user-agents#6: A duty of Negotiation](https://github.com/w3ctag/user-agents/issues/6)

Sarven: Noted, on my plate, can PR this week.

Sarven: will try to make sure (similar to the Transparency duty proposal) so that it is not overlapping with existing text.

### [Incubation: Application Capability](https://github.com/w3ctag/design-reviews/issues/1255)

Sarven: There is an explainer in the repo. As the name implies, this is a structured way for apps to publish their capabilities, requirements, and policies which can be used by other apps, servers, or user agents. Publishing means, as a standalone resource, incorporated into the Web Application Manifest, or other ways, so the app itself or other users can make decisions based on that information, i.e., what an app needs or what it’s about to do.

… One point is permissions. Today, servers might set a security policy which applies to all services there. With this approach, this information is declarative and accessible as a resource, so consumers can query it. In that way, servers can make application/resource specific decisions. Same problems have been solved in other parts of the web and operating systems, e.g., file handling.

… Some of the features of the spec allows users to choose the right applications. Also, potentially overlapping use cases with WebMCP. Contrast is that it’s purely declarative.

Heather: So your ask is to check where this should go from here?

Sarven: Yes, discussed it in SOLID CG, but the question was if there’s wider interest or another group that could take over this work, or whether a new group should be created.

Lola: What about the WebApps WG? This seems aligned with their goals.

Heather: Exploration IG was founded exactly for that.

Marcos: This is great because it covers similar grounds than WebMCP, allows you to do the same things. In WebApps it would have go through the entire incubation process. Sounds very interesting.

Brian: +1 to what Heather said. The non-goal is script-level tool calling. Rationale for WebMCP for choosing that is to extend existing applications vs. rethinking them from the ground up. Curious where this belongs in the spectrum of web services.

Sarven: It’s also about how to invoke ??? in the application.

<!-- Reviews that have been pending external action for at least 6 months -->

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

### [design-reviews#1183: Incubation: new speculation rules action: prerender_until_script](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1183) ([Github](https://github.com/w3ctag/design-reviews/issues/1183)) - @dandclark, @xiaochengh

### [Agenda building for the TAG f2f: 7–11 September 2026 #60](https://github.com/w3ctag/meetings/issues/60)

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Pacific Breakout (Asia / Australia / West America) - [2026-08-12](https://www.timeanddate.com/worldclock/converter.html?iso=20260812T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Heather

Scribe: Heather

Attendees: Marcos, Brian, Heather

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-10-minutes.md

Raw minutes: ...

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @jyasskin, @marcoscaceres, @bkardell

Brian: Added a comment just before the meeting. Web views are not dissimilar to mini-apps. Users don't recognize any difference.  Core question here is: what distinguishes a web view from a user agent, and does the distinction matter? Original framing: a web view is not necessarily a user agent, but can be. Problem is, even technically literate users can’t tell what’s a web view, PWA, or Electron app

Heather: My idea is that we focus on whatever the thing is, it's serving the best interests of the end user. Can we classify beyond that? Does that help anyone?

Brian: Web views are a thing in the world, so it might be helpful to define something.

Marcos: The separation of the web stuff - does that matter? The UA is the UA, regardless of the platform, as long as it meets the criteria we define. My proposal is "user agent concept" and the spec puts requirements on the UA for it to behave certain ways. Sometimes we go beyond what the UA is defined to do. For example, in Digital Credentials, when you have an iframe and make a request from the top-level, you should show both origins. Making that relationship clear to the user is important. In geolocation, we ask the UA via the spec to show the origin. So, in that sense, the UA comes first and the specs direct / put conformance requirements on UAs. 

Brian: i think what Marcos is saying is that they are all UAs but they all share a base definition. You can have differing requirements depending on what you're implementing. But it's still tricky because the user doesn't know. 

Marcos: I think we should drop the "web" UA part of this. It should just be UA. We have the right things there - protection, honesty, and loyalty are all broadly applicable. Then the web UA are the ones that run on the web platform and specs assign conformance requirements to it. 

Heather: So what do we need here for text?

Marcos will propose some text in the issue. 

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Atlantic Breakout (America / Europe) - [2026-08-12](https://www.timeanddate.com/worldclock/converter.html?iso=20260812T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Heather

Scribe: Matthew

Attendees: Matthew, Brian, Dan, Heather, Lola, Hadley

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-10-minutes.md

Raw minutes: ...

### [design-reviews-private-brainstorming#217: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217) - @csarven

<skip>

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

<skip>

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

<skip>

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Matthew: Would like to make sure ADRs are on the f2f agenda

Heather: They are!

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

<skip>

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @hlflanagan, @lolaodelola

Lola: I see Heather's comment - can we resolve this? Satisfied, or with concerns?

Heather: Satisfied. I'm interested in the response, but I don't think it's blocking.

Lola: We need to change the label...

Brian: I brought this up in the last f2f and we have a doc, but haven't actually made a decision yet.

Lola: If you're happy Heather, I'll resolve as satisfied. Or should we leave it open for the response?

Heather: I'll reach out to the posters directly and ask if they'll be responding to it.

### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Mike: Ehsan posted the comment.

Lola: Needs the 'pending external feedback' label (added).

### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

Lola: Ehsan posted a comment on the private thread.

Heather: It's a long and thorough proposed TAG review. Looking at it today.

### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

<skip>

### [design-reviews#1223: Other Spec Review: Responsively-sized iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1223) ([Github](https://github.com/w3ctag/design-reviews/issues/1223)) - @dandclark, @toreini

Dan: Still some questions on things like cross-origin animations; we're waiting to hear back.

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

Brian & Matthew clarified on Brian's comments, improvements to proposed review; Matthew to update the draft.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Lola: This was added to the f2f agenda, so we can skip it here.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Eurasia Breakout (Europe / Asia / Australia) - [2026-08-13](https://www.timeanddate.com/worldclock/converter.html?iso=20260813T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Hadley

Scribe: Matthew

Attending: Matthew, Christian, Hadley

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-10-minutes.md

Raw minutes: ...


### [user-agents#22: Implementing the web platform](https://github.com/w3ctag/user-agents/issues/22) - @csarven, @marcoscaceres

*skip*

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

*skip*

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

*skip*

<!-- PRs -->

### [user-agents#57: Remove overloaded credible commitment](https://github.com/w3ctag/user-agents/pull/57) - @csarven

*skip*


### [user-agents#54: Clarify payment doesn't change loyalty duty](https://github.com/w3ctag/user-agents/pull/54) - @csarven

*skip*

### [user-agents#56: Use declarative duty language instead of terms overlap with RFC requirement levels](https://github.com/w3ctag/user-agents/pull/56) - @csarven

*skip*

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

bkardell and dbaron still in discussion on this.

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

[matthew discusses trialing an AI-driven review]


<!-- Design Reviews -->

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

*TAG sub-group is scheduling our next review meeting*

### [design-reviews#1248: Other Spec Review: CSS scroll-axis-lock](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1248) ([Github](https://github.com/w3ctag/design-reviews/issues/1248)) - @matatk, @lolaodelola, @lukewarlow

Matthew: Intended for the situations where you have content which naturally should pan in all directions (e.g., a map), and then you want to lock one axis. Would make a lot of things more usable, extensive a11y section. Opt-in for the author. They also make the point that if you have a container which only scrolls in one direction, this doesn’t affect it.

… Only thing I’m worried about is device orientations, not sure if there’s a conflict. If the user wants the browser to not do anything different here, could this be a UA option? Comes back to security and privacy thing, what if the site realizes the user has blocked it? Leads to the wider discussion of fingerprinting.

… Don’t really think it’s likely people would like to turn this off. Assume authors only turn this on where it makes sense. Which would make it generally a positive thing. 

… Would be interested if Lola can think of any use cases I might have missed. Probably going to be “satisfied.” Should ask APA though. Seems well thought out.

Hadley: Next steps? Checking back with Lola and Luke?

Matthew: Yes.

Hadley: Are we ok on timing?

Matthew: PR seems to have landed, implementation seems not to have started yet, so we still have time.

### [design-reviews#1224: Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1224) ([Github](https://github.com/w3ctag/design-reviews/issues/1224)) - @hlflanagan, @xiaochengh

*skip*

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

*skip*

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

*skip*

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

*skip*

### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @ylafon, @marcoscaceres, @christianliebel, @lukewarlow

Christian: This is effectively the third iteration of this idea. We need to decide on what the install model for the web should be; we have an agenda item at the f2f for this.

Hadley: I'd like to hear more from Alex Russell.

*Christian to enumerate the architectural questions, for example: 1. do we want site-initiated install promps on the web? Tag has already answered it in: same-origin is ok, cross origin should be looked at afterwards.*

Christian: Previous TAG said it's fine to explore same-site installs (and tackle cross-origin later after getting some experience).

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242)) - @matatk, @christianliebel

matthew: i need to ask them about the usage counter in chrome and the parallels with a customisable select an old element that's reused and we provide an optim. And then there was the scope issue from last time.

Christian: Yes, let's ask the questions for now, and continue the review.

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh, @lukewarlow

*skip*

### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres

*skip*

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

*skip*

### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk

*skip* (I think we're discussing at the f2f - it was proposed for that)

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

*Matthew to check on the question around Braille, then expect to close*

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

*skip*

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

matthew: luke has proposed a comment. I'll post it. 

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

*skip*

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

*Matthew to post comment.*

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

*skip*

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

*skip*

## Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
