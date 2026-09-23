# W3C TAG Minutes for week commencing 31 August 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-31-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-09-02](https://www.timeanddate.com/worldclock/converter.html?iso=20260902T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair:

Scribe:
    
Attendees: Brian, Marcos, Dan

### Reminder: Please review TAG F2F Agenda Planning

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan
### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @jyasskin, @marcoscaceres, @bkardell
### [design-reviews#619: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-principles/issues/619) - @marcoscaceres
This came up in the context of webmcp. When JS is disabled, should declarative WebMCP also not be allowed?
When JS is disabled, JS in trusted contexts like Browser UI and extensions will still run.
To what extent should the webmcp tool registrations be treated as trusted?
They seem like they are fundamentally separate things to control -- disabling JS need not disable declarative webmcp.

This led to a discussion about WebMCP. Marcos talked about an alternative which would be to standardize the compact representations of sites that browsers are already building to hand to agents. The hope here is that standardization would better allow developers to understand and debug how their sites are being seen by agents. WebMCP proponents have suggested that these approaches don't work well, but Marcos has seen better results. It's something we should discuss further. 

### [design-principles#620: Link to the Design Principles doc](https://github.com/w3ctag/design-principles/pull/620) - @tabatkins
This is straightforward, merged.

### [design-principles#621: Add new fragment directive guidance](https://github.com/w3ctag/design-principles/pull/621) - @tabatkins
This references a WICG doc: https://wicg.github.io/scroll-to-text-fragment/#fragmentdirective
Somehow all the browsers shipped this but it was never moved into the HTML spec.
Marcos left some feedback on the PR.


### [design-reviews#1224: Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1224) ([Github](https://github.com/w3ctag/design-reviews/issues/1224)) - @hlflanagan, @xiaochengh
### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)


## Atlantic Breakout (America / Europe) - [2026-09-02](https://www.timeanddate.com/worldclock/converter.html?iso=20260902T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Christian

Scribe: Matthew

Attendees: Christian, Matthew, Dan, Brian, Yves, Hadley

Regrets: Ehsan, Heather

### Reminder: Please review TAG F2F Agenda Planning

https://docs.google.com/spreadsheets/d/1D7low9ygKMXzzFcClTh5Q75JQwHTLdzpW0qPv1BSsUU/edit?gid=389598608#gid=389598608

Brian: *asks about UAs (especially web views) finding - who is best placed to present*

Hadley: Others could step in if needed - we are looking for someone to start the discussion off.

Brian: I think UAs and Global Components are very related; would be happy to switch them, as I think the Global Components discussion may influence the other.

Christian: There were fewer items suggested than slots, hence all the docs slots.

Christian: We can put Global Components and UAs back-to-back.

### [design-reviews#1251: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1251) ([Github](https://github.com/w3ctag/design-reviews/issues/1251)) - @jugglinmike, @marcoscaceres, @bkardell

*skip*

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

Matthew: We got some feedback. There’s a couple of interesting things. Florian replied with insightful stuff. (reads Florian’s response) There’s a WHATWG issue that controls (?) are still an open issue on their side: https://github.com/whatwg/html/issues/12318 (…) Overall, they’ve addressed the vast majority of our concerns.

Brian: Can ping Florian if that is still relevant.

Matthew: I think we got our external info, but we want to wait for external feedback, but expect us to be either satisfied or satisfied with concerns.

### [design-reviews#1265: WG New Spec: Global Privacy Control (GPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1265) ([Github](https://github.com/w3ctag/design-reviews/issues/1265)) - @hadleybeeman, @toreini, @hlflanagan, @lolaodelola

Brian: Heather and I commented on this in the private thread. It seems pretty good. Heather had a comment about workers that I don't think is answered here. They say it's based on what the top-level page sends, but what if you have a shared worker? It seems like a simple start on a better version that is working how Do Not Track was intended to. The spec is much simpler. You can advertise that you support this via a well-known URL. A user can say 'hey, don't sell my information' via a single setting. If you give the signal, there are many places in the world, especially states in the US that are passing laws that can be enforced once you have this in place. There already are lawsuits that are influencing actors on how they work. The spec is super short. I enjoyed reading it.

Christian: So we're waiting for info from the others, but sounds positive so far.

Brian: For me, yes, and for Heather mostly too I think. Heather had that question, we should ask.

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews/issues/1161) - @csarven

*skip*

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

*skip*

### [design-reviews#1246: WG New Spec: Additional Windowing Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1246) ([Github](https://github.com/w3ctag/design-reviews/issues/1246)) - @jugglinmike, @bkardell

Brian: There are a lot of related WebKit standards positions; following up on the threads.

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242)) - @matatk, @christianliebel

Christian: I have a draft comment (posting after this); Matthew, please review.

Matthew: will do

### [design-reviews#1264: Incubation: Filterable select](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1264) ([Github](https://github.com/w3ctag/design-reviews/issues/1264)) - @matatk, @dandclark

Dan: No comment yet, but have been looking over the issues. There are 3 options given in the explainer, think they are asking for info from us. The nicest option (B) involves the options being within the element, but this may not work from a webcompat perspective (may break the parser). Option A involves hooking things up with IDs (referencetarget may be needed for shadow DOM). Makes sense but needs more tags. Option C involves an attribute you add to the `<select>` which magically adds the required elements, but then would require pseudo elements for the styling. Not keen on it due to that, but it seems to be the one gaining momentum.

Dan: Option A seems to be the best in terms of clarity. I don't have strong feelings so am concerned about how it will come across if I appear to endorse one particular one.

Matthew: Same as for reference target, problematic if developers need to do non obvious stuff, will look at it as soon as possible.

### [design-reviews#1254: Incubation: Cross-Origin Storage](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1254) ([Github](https://github.com/w3ctag/design-reviews/issues/1254)) - @ylafon, @bkardell, @dandclark

Yves: I've not commented yet, but I have two issues. The first is the prefilled list. It may promote sites that you have a relationship first. The other issue is when you're sharing things and putting them in the cache, if you can check something is there, that gives you 1 bit of info. If you add 10 things to the cache (they could be small) then you have 10 bits of info. If it bypasses the restriction of cross-site sharing, but works in this way, there is still a perfect (if limited) channel for sharing info.

Brian: I left a comment. This is currently a Chrome-only feature. It's only enabled when you have 3pc because it doesn't make the situation any worse. TAG already has expressed an opinion that 3pc have to be removed, so entrenching them should not happen. I had other parts to my comment, but that's the most straightforward.

Yves: I saw the 3pc requirement, but if the spec evolved to work even if 3pc are not set, by using the hash-only checking, then it has the issue that I hightlighted, which is being able to share things bethween colluding sites that may check the same hashes from different origins.

Brian: I commented also that you'd have to specify so many things that aren't specified in order to make this work at all. It sounds like the performance gains from this in cases that are not the AI case are disappointing. I think you'd have to specify things to the degree that this would be a different proposal. I don't think it's possible to address these concerns.

Christian: The idea is that you'd have to show permission prompts if you want to access the cross-origin storage. If you really share data via caching cross origins and the prompts are turned off if 3pc are on, that part is only about the prompting. Good points and I will check out your comments.

### [design-reviews#1253: Other Spec Review: CSS navigation-based styling](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1253) ([Github](https://github.com/w3ctag/design-reviews/issues/1253)) - @matatk, @dandclark

Dan: I had some surface level questions (a couple of weeks ago) that maybe we should post; I am hoping to have more time to look in more detail and maybe come up with more comments.

Matthew: We did have a back-and-forth with them regarding a11y, right?

Dan: Yes.

Matthew: One of the goals that they state is how a user interface is changing if they interact with it. I’m a bit sensitive about if the user would understand that. If the visual design has a semantic relationship, that needs to be expressed. There are other ways to understand the UI. Visual cues/structural stuff/focus management that we need. Trying to make that transition more accessible by adding more metadata doesn’t seem like the right approach. Think we should keep the momentum going. Appreciate the additions that they’ve made.

Dan: I will post what we’ve got, and then we can look at it async.

### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

*skip*

### [design-reviews#1255: Incubation: Application Capability](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1255) ([Github](https://github.com/w3ctag/design-reviews/issues/1255)) - @hlflanagan

*skip*

### [design-reviews#1249: WG New Spec: Recognized Entities v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1249) ([Github](https://github.com/w3ctag/design-reviews/issues/1249)) - @hadleybeeman, @hlflanagan

Hadley: Heather's done some work on this; it's in my queue to review.

### [design-reviews#1256: [wg/immersive-web] Immersive Web WG 2026 Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1256) ([Github](https://github.com/w3ctag/design-reviews/issues/1256)) - @matatk

Matthew: A couple of deliverables they listed I wanted to check that they are immersive-specific. One was higher resolution haptics for Gamepads.

… Left a comment on the charter on behalf of APA.

https://github.com/w3c/strategy/issues/564#issuecomment-5298679608 - questions 4 and 5 were the most potentially architectural

… Last one is a PCM thing I wanted to check. Don’t think it is WebXR-specific. They are developing use cases rather than a spec, and another group would do that. Another one is CSS Spatial Layout. There are at least two proposals for doing “spatial” as in depth. There’s an Apple proposal; Meta has a different approach to a similar problem. Wanted to make sure that this is being discussed. We need to make sure that people are aware this is being worked on. Need to send the link to Marcos.

Matthew to send the link to the #design-reviews Slack channel.

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @hlflanagan, @lolaodelola

*skip*

### [design-reviews#1248: Other Spec Review: CSS scroll-axis-lock](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1248) ([Github](https://github.com/w3ctag/design-reviews/issues/1248)) - @matatk, @lolaodelola, @lukewarlow

Matthew: This seems really good, next steps we had were checking with Luke and Lola, can get more opinions from APA.

### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

*skip*

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

Brian: Luke and I met about this. We met with Anna and Dan to talk about the challenges in the space. There's a lot that's up in the air in terms of past efforts making progress - are we going to get traits, mixins, custom attributes? The're all in a similar space. Also `referencetarget`

Dan: *confims it's shipped in Chromium and will land in HTML spec soon*

Brian: What's the simplest case? Have you talked to the FAST people about it? Seems ideal.

Dan: We have conversations coming up with FAST e.g. they have a custom button that appears and disappears, though we were asking why not have it always there to be delegated to. This could work now `referencetarget` is a thing. Contrasting the semantic delegates and PEPC approaches.

Brian: I thought they were saying 'in order to make this work, you have to put your actual element in the light DOM' but people don't want to do that. Now I think they are adding the element into the light DOM in a clipped manner, so it can handle form submission etc.

Brian: Luke had a proposal that was related and would solve some of these problems and only took 2 hours to implement. It was essentially to allow the element with the shadow root to attach to a form. We thought that might happen relatively easily but it got pushback from WebKit. If you include a custom element that has named form elements, you can reason about them.

Brian: I think closeShadowRoot was a big architectural mistake.

Brian: I think the proponents have a sense of what we're thinking, and so there isn't a huge rush to come to a position on it.

Dan: Action is on Ana and FAST to engage with web developers to see what is actually needed here. Which direction allows them to delete code.

### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

*skip*

### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres



### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon



###n[design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk



### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola



### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

*skip*

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman



### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell



### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

*skip*

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

*skip*

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk



### [user-agents#58: push several example changes from prose to callouts](https://github.com/w3ctag/user-agents/pull/58) - @bkardell



### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

*skip*

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Eurasia Breakout (Europe / Asia / Australia) - [2026-09-03](https://www.timeanddate.com/worldclock/converter.html?iso=20260903T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola

Scribe: Christian

Attendees: Christian, Lola, Marcos

Regrets: Yves, Luke, Ehsan, Matthew

### Reminder: Please review TAG F2F Agenda Planning

Marcos: I’m taking care of everything, for the social outing, whale watching may be expensive—so I’m still thinking about that. I’m there from Friday and setting everything up.

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh



### [design-reviews#1263: WG New Spec: Verifiable Credential Barcodes v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1263) ([Github](https://github.com/w3ctag/design-reviews/issues/1263)) - @hadleybeeman, @toreini

*skip*

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel



### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @ylafon, @marcoscaceres, @christianliebel, @lukewarlow



### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh, @lukewarlow

*skip*

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

*skip*

### [design-reviews#1250: Incubation: WebRTC Diagnostic Logging](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1250) ([Github](https://github.com/w3ctag/design-reviews/issues/1250)) - @lolaodelola



### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

*skip*

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

*skip*

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

*skip*

### [user-agents#22: Implementing the web platform](https://github.com/w3ctag/user-agents/issues/22) - @csarven, @marcoscaceres



### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

*skip*

### [user-agents#56: Use declarative duty language instead of terms overlap with RFC requirement levels](https://github.com/w3ctag/user-agents/pull/56) - @csarven

*skip*

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

Christian: Let’s schedule that for the F2F during one of the docs sessions.

### [user-agents#57: Remove overloaded credible commitment](https://github.com/w3ctag/user-agents/pull/57) - @csarven

*skip*

### [user-agents#54: Clarify payment doesn't change loyalty duty](https://github.com/w3ctag/user-agents/pull/54) - @csarven

*skip*
