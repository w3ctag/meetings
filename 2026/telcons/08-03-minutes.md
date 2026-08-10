# Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/08-03-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.


## Pacific Breakout (Asia / Australia / West America) - [2026-08-05](https://www.timeanddate.com/worldclock/converter.html?iso=20260805T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Brian, Dan, Marcos
    
## User agent examples
Brian: the example callouts between sections is inconsistent
Dan: yes, I can see that
Marcos: agree
Brian: can we make them consistent? 
Marcos: yes
... discussion as to different options.... 
Brian: I filed an issue to try to fix them up  https://github.com/w3ctag/user-agents/issues/53

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @jyasskin, @marcoscaceres, @bkardell

Brian: Not sure there's anything to do here. Heather was articulating it about navigations between origins. For webviews, is it still an origin?
Marcos: Yes. But let me read the issue. The same origin policy still applies to webview. But on the webview running it on its own, there's no browser UI. But they have separate processes...the web security model still applies. 
Brian: The UA definition won't match the legal one. Is the screen on your blender or the infotainment in your care a UA if it only serves pages from local filesystem.
Marcos: Yes, if tries to serve mixed content, violates same origin policies.
Brian: I largely like Heather's April 7 comment. Only question if we adopt that approach is if we can make it more general/flexible. And make it more behavior based rather than strict classifications. Do we need to care about embedded scenarios like these? Should we file sub-issue for that? Heather's approach is right that spec already contains the right guts but we could strengthen the bit about making it clear when you're a user agent when you're acting like one.
Marcos: Yeah. List is good but it's too limiting. But it's hinting in the right direction.
Brian: If you're using electron, using webviews, using Sublime text, you're not really acting as UA. 
Marcos: I don't agree. Look at Slack or Visual Studio. In VS Code if you load a repo it asks if you trust the repo. That's UA behavior. 
Dan: That's not same-origin policy
Brian: Example of display on embedded device, communicating over protocol buffers...nothing about it has a sense of web pages or origins.
Marcos: Is it rendering web pages?
Brian: Rendering local pages
Marcos: Do they update?
Brian: It gets fuzzy. If you install cookbook, press a button and it fetches an update, fetches remote recipes, now it's a UA. But not if it's domain you control. 
Marcos: Even in that case the choice the manufacturer made was to only nav local files. They acted on behalf of user in that. They might have been smart about what content to let in -- so decision was made on behalf of user.
Brian: That's the same for smart TVs, they're basically running a web view. Is it a user agent?
Marcos: Probably, they're mediating between user and content. If they're stopping from accessing particular content, they've made a choice and become a UA. Falls into the responsibilities as outlined in that law.
Brian: That's where it gets tricky. Updating an embedded device, it's static files but it's like updating a serviceworker. Just using file protocol to load the content.
<discussion of what happens with embedded device document viewer when you click links>
Brian: I like the direction of Heather's work on this and would be happy to see that carry on.


### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu

Brian: How different are webviews from iframes? What the browser does with iframes you should do. Let's say you have your page and an embedded thing about payment. That's conceptually what it is. The UI requirements should be the same. Browser should tell you if domain other than the one you're on is asking permission.
Marcos: Yes. There's a bunch of specs that deal with this problem like digital credentials and storage access and webauthn. If you were to embed a webview and it loaded a document with an iframe, with another iframe, the relationship should be expressed to the user even if they can't see URL bar.
Brian: You end up with mixed content. Have a warning at the page level.
Marcos: The principle is it's the responsibility of the API where it's embedded to express the relationship between the top page and the embedded content, where the API call is made. I don't think that's been expressed clearly.
<Closed #41>
We will put something like "When embedding a webview, the embedder takes on the duties of a user-agent and becomes responsible for privacy, security, etc."


### [design-reviews#1244: [wg/webappsec] Web Application Security Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1244) ([Github](https://github.com/w3ctag/design-reviews/issues/1244)) - @hlflanagan

Marcos: Haven't looked in a while but think we're pretty much done. 
Brian: Can probably close
Marcos: I'll take a look now but think we're OK with it.

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres
### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan
### [design-reviews-private-brainstorming#302: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/302)

### [user-agents#6: A duty of Negotiation](https://github.com/w3ctag/user-agents/issues/6)

## Atlantic Breakout (America / Europe) - [2026-08-05](https://www.timeanddate.com/worldclock/converter.html?iso=20260805T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Special Focus: [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel & guests

Chair: Lola Odelola
Scribe: Dan Clark
Other Attendees:  Andrew Nahas, Andrew Nolan, Julia Pagnucco, Brandon Walderman, Brian Kardell, Christian Liebel, Johann Hoffman, Liad Yosef, Luke Warlow, Matthew Atkinson, Mike Pennisi, Domenic Farolino, Philippe Le Hegaret, Sarah Drasner

Christian: When we screen proposals people who are interested assign themselves. For webcmp we are 4: marcos, ehsan, matthew, and me. Look at the proposal, explainer, early spec text, try to check them against design reviews and also the broader angle of 'is this a good fit for the web platform', does it make sense architecturally. Helpful to have various people on the review to get broad perspective. Regarding webmcp, also have the doc we shared with you. Can see the names of who wrote feedback text. I like the proposal. marcos and ehsan are critical. Points they raise are in that google doc. But they're not here, so hard for me to represent what they said but we'll try. How do we proceed?
https://docs.google.com/document/d/1Ao32HZHk_VYzPRvUNLCKBNvpHk7naqqMqIpBc67fcsQ/edit?usp=sharing

Andrew Nolan: Should we still meet today?

Matthew: I can represent some of ehsan and my feedback. 

Lola: Scheduling TAG is hard, let's keep going.

Domenic: We talked with Marcos a bit. I want to differentiate security concerns. When working with the W3C security interest group to come up with a thread model, I realized a lot of concerns were with general AI agents using the web. Agents can mix data, sloppy one can type SSN in pizza site...lots of ways to misrepresent and misuse the web. But we found it useful to raise that solving those problems probably needs to happen at a different layer from WebMCP. Agents are already using the web, representing the user, so tying the concerns to a specific proposal (WebMCP or separate declarative proposal) is the wrong layering. All the problems in that ecosystem happen without WebMCP too. If we tie it to WebMCP and that proposal dies, we still have all these problems. So WebMCP can layer on that security work. Security IG was sympathetic to that view. Even if agents using normal HTML form, they can mix data from origins, type in personal info inappropriately. We're working on mitigating that stuff but it's not specific to WebMCP.

Matthew: I take the point. Probably don't need to dig too deep into that on this call, but sounds reasonable. However, if we bake WebMCP into the platform, that's the introduction of agentic AI into the platform. Opens the door. You can use it now and it has those risks, but when you add to the platform we want to improve on the status quo. If sec/privacy issues are unresolved, we've made the situation worse. I think that's fundamental difference of perspective. Probably won't make progress on that issue but worthwhile to have it in the open.

Lola: +1 to matthew

Sarah: I agree with Matthew. Right now, agents scrape the DOM, which happens today. Further convo on that subject should look at what happens in practice. Saying don't do anything until it's resolved is infeasible, it;s already happening. Prompt injection already happening. WebMCP improves upon status quo. In convos around security, should focus on what happens if no WebMCP vs what happens with WebMCP. Concerned we're not representing authors and creators. Want them to have a voice vs this just happening to them. 

Lola: Authors and creators of stories are not first in order of constituencies. User comes first.  If benefits autjor but risks user security, have to take that seriously . Shouldn't standardize industry practice just because it exists. We have higher set of responsibilities. Should look at what's currently happening but shouldn't be main focus.

Domenic: It's more than differing perspective. Some of the solutions that are required to secure agents on the web are not solvable by a web API. No webidl to stop claude from reading my email and putting personal info in wrong website. Should build surface area to help agents not do that. We're working as API with the parts of systme that need to solve that. But solutions will not come from JS in renderer process in one frame. AI agents are much broader than that. Actual solution must come at different layer.

Christian: To Sarah -- I'm positive on this proposal, because if you do other AI stuff, the API feels just right. The way you'd write it on a different platform. Makes sense from developer POV. But does it have to be JSON schema, or can improve HTML, or form elements to make same thing happen? This is fair question. What are your thoughts?

Brian: We don't know what the future holds. Useful to have additional info like this in HTML even if not just for AI. Good for AI, for search...for potential extensions maybe. Better if we diversify the things we try. An efficient way for machines to talk to each other, they are talking each other like humans...shoulld explore more efficient things. I question if this is the thing. Don't have info to understand why other approaches were dropped as possibilities. Want to learn more. Why specifically this one. Doesn't seem like the most efficient way for machines to talk to each other.

Matthew: Will be comment from APA on a11y angle. Exciting things in here but also concerns. Will try to keep more general here. Norm is that when we add new features we try to add them in simple declarative way that solves most use cases. Tends to be more predictable, easier to make more private. Then if we find there are more complex use cases, followed by more complex imperative way. Here we're doing it the other way round. Curious about that. Key goal stated is allowing collab between agents and humans. A11y promise seems to come in there. But thing that's specced is API that agents can call that user can't see. And very general. Declarative thing is more pinned to tasks involving filling in forms, more bounded and safe. Why not experiment with declarative first?

Domenic: We're running Origin Trial experiment in Chrome now. A couple million declarative registreations, and [missed] other registrations. Declarative can't handle nested cases, streaming...some features we do declarative initially, but lots of important ones don't. Readable streams, important stuff in popover. Lots of important imperative APIs...service workers...this is fine, it makes web relevant. Limiting to declarative limits us being compatible with actual web ecosystem. How to keep in-page agents in scope without imperative API? Just scraping the DOM isn't enough. Other concerns like about running backgorund tools in service workeres. There's lots of use cases with native apps that use like Apple's native app intent framework. If we don't support those use cases in the web it risks being less relevant. Other parts of industry have converged around solutions that fit like this. We can do better job documenting that. But I really think if we want to upend industry state of the art, need strong evidence.

Sarah: Well said. Tied to point Lola made: user first is the goal. If site devs can't think through things that are user first, passing large token overhead can be less safe if no way to declare that content is read only. The more that site dev has agency over the experience, better for the user too. Standard HTML forms have problems representing real application workflows. See this in practice in existing apps. Declarative doesn't work well for how these sites manage state. We're getting feedback like this from sites like instacart.

Andrew Nolan: +1. When we talk to devs they never mention declarative, always imperative.

Brian: Because a lot of state lives only temporary in browser? Only way people can act on things is because happens to alraedy be loaded in browser. If so, we'd be best served by throwing multlple lines in the water, see which we can fish with. Still implies you have to load the page. Regular MCP is appealing because mostly declarative, can describe in one file. See that was given up on. But wonder if there are new ways to offer people to build apps that start by defining services, let you build UIs that integrate them in appealing ways. 

Domenic: Reason people use imperative is because a lot of the tasks are not form-shaped. One example is filtering things on page, or adding overlay to picture editor. Forms default behavior is to just navigate. We find peopple want to hook into application code. Usually attach to submit event, if webmcp, do imperative work there. Is a weaker schema. Defining stronger schema end up looking like MCP.

Liad: Should separate core browsing that reiles on the existing architecture and state. If company wants to build accessibility for agents in other way, can do it without relying on web page. And generate UI for that. But it's different use case. Headless agents don't need to go through web.

Lola: Encourage proponents to think on user impact. Have heard lots of exisitng agents that do stuff on web. Want to understand need and desire for w3c in particular to stay relevant. Part of current climate is AI. User privacy, security, safety -- we've seen news about harm. While I understand need to not drop behind, hope folks are thinking not just how can we standardize, but how can we do better. Makes users AI interactions on the web better than what's commercially availabl.e

Domenic: Can you clarify? What is missing in the explainer we can clarify? 

Lola: I'm just going by today's discussion. Lots on making sure we don't drop behind. For those who are working, I want them to hold users at forefront.

Domenic: WebMCP is the result of us trying to do that.

Sarah: Keeping users safe is my only interest here. WebMCP is a potential path to better user value and security. Framing might be off on security. Difference in stating there are technical limitations to what the web can do, the standard can do...if you are providing safeguard in mcp like read only hint, still relying on agent to do that appropriately. Maybe framing is off -- yes the whole motivation is keeping users safe. I think point Dom is making is it's impossible technically speaking to do it only in the web standard. Also looking into how else we can provide safety. Don't want it to be confused that we don't see that responsibility. we want to work with everbody here to make that as good as possible.

Matthew: I looked again at spec intro. Talks about agents and human collab. Appreciate what you said on the forms-only approach, this is much more general. But it says tools can be invoked by agents, browser agents, assistive tech...two distinct things mentioned: agents, which are general. That's different form agents that live in broser, or AT which is part of browser. Also mentioned headless scenario. No human driving it. Very different cases. Would it help to separate those out? Agents hosted in UA is separate from ones that aren't.

Andrew Nolan: When we originally wrote the proposal, one of the common questions was how this works. Could anything use it, does it have to be agent. Was helpful for people to understand that it doesn't. Agents are just the primary use case. If other tech wants to use these APIs, that's possible but not necessarily the focus.

Domenic: Not seeing why the distinction matters of in-browser or shipped separately. How the product chooses to expose tools, just like dev tools protocols...why does this have impact on webmcp spec?

Matthew: My assumption was that agent outside the browser would not have access to those internal browser mechanisms. So you answered it. I assumed we treated those differently, but if you say both have access to those APIs...if it's completely headless scenario, does it go to web page to get imperative endpoint, or do something completely separate? Other bucket is UA/AT provided agents, I want help doing something on it. If it would somehow have access to the APIs I agree it's not different.

Liad: This was my point from earlier. investigation into accessing contnt headlessly, that's different use case, doesn't have to go through browser. What we're talking about here is use case where we're interacting with website.

Domenic: Distinction is minimal from webmcp perspective. Devtools protocol could drive browser which then hits webmcp. Can't verify from API perspecitve whether human is driving. It's a product decision. So we're mostly treating them the same.

Lola: Aside from Ehsan and Marcos, I know Heather and Sarven also had feedback and questions. Reviewers here today, do you have enough for draft comment or need more discussion?

Matthew: Discussing in google doc, and found this very helpful. Might need another call.

Domenic: I'd love an investigation into why we think it's possible to close the agents using Web Gap just through markup, against the grain of what every AI company is doing. We can help document. But think it's incumbent on reviewers, if we're being pushed in a direction, to help supplement with evidence. Let's be honest about what other solution precludes, e.g. no headless usage from service worker...want to make sure we're weighing tradeoffs and deciding with evidence.

Lola: That's fair can you put that in the public issue or in google doc?

Domenic: I'll put it in TAG issue.

Brian: Why is there urgency?

Domenic: I don't think there is. We've gotten so much feedback, want to get wide horizontal review. Mostly that there's a lot of attention on it, want to get lots of eyes on it.

Lola: Maybe the urgency I was referring to is more bureaucratic.
Do we need another call?

Christian: Reviewers will meet again. And look at google doc. And we'll see.

Lola: Pepople who weren't here might need to go to MCP folks rather than the other way round.


### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell
### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk
### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel
### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov
### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @hlflanagan, @lolaodelola
### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow
### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven
### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini
### [design-reviews#1223: Other Spec Review: Responsively-sized iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1223) ([Github](https://github.com/w3ctag/design-reviews/issues/1223)) - @dandclark, @toreini
### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk
### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman
### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan
### [design-reviews-private-brainstorming#284: WG New Spec: Attribution](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/284)
### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

## Eurasia Breakout (Europe / Asia / Australia) - [2026-08-06](https://www.timeanddate.com/worldclock/converter.html?iso=20260806T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola
Present: Marcos, Luke, Ehsan, Matthew, Christian, Hadley
Scribe: Marcos

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: i sent my feedback, but it's not closing comment. I'm waiting for the proponents for their feedback. I don't think there's any major concerns. Just waiting on the proponents to get back to me.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Lola: we have "resolve to close satified" 

Luke: we might post as satified with concerns, otherwise it's good to go. 

Matthew: should I do that. 

Lola: yes, go ahead. 

Matthew: Oh, there was an additional ask from us regarding scroll spies, is this okay to close then?

Lola: Does this impact our resolution?

Matthew: Agreed on closing it as satisfied with concerns.

Lola: Suggest opening an issue there, and closing this as satisfied.

Luke: CSS allows you to do CSS spies even with JS disabled, it’s different for img[load=lazy]. Is this a boundary that we should be enforcing? Matthew, do you want to go ahead and create the CSS WG issue?

Matthew: Will do.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola
### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola
### [tag.w3.org#101: Update Yu Sen participation](https://github.com/w3ctag/tag.w3.org/pull/101) - @ylafon, @hadleybeeman

Lola: Hadley, can you please review and approve the PR? 

Hadley: will do. 

### [user-agents#22: Implementing the web platform](https://github.com/w3ctag/user-agents/issues/22) - @csarven, @marcoscaceres

Marcos: I left a comment explaining that a user agent is separate from the web platform. The web platform makes use agents do stuff ("A user agent MUST...") but user agent stands on its own.  

Lola: I tend to agree with that. Do you think there's things we need to add to the user agent's document.

Marcos: Yes, we should clarify the distinction and show/prove how specs manipulate user agents.

### [design-reviews-private-brainstorming#217: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217) - @csarven



### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Ehsan: we were waiting on the proponets, but we have waited 6 months alrady. 

Lola: We can probably close it with resolution time out. 

Ehsan: I'll let them know we plan to do that. 

### [design-reviews#1248: Other Spec Review: CSS scroll-axis-lock](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1248) ([Github](https://github.com/w3ctag/design-reviews/issues/1248)) - @lukewarlow

Luke: I asked them to update their explainer with a11y text. They have now done that. I think it looks ok as is. I'm satisfied with this, but folks should speak up now. 

Lola: I haven't read this in full, but the concern was at first glance and potential for abuse. Do you think they have mitigations? 

Luke: Depends on which parts you are concerned about. It might be possible to create a bad UX. But the developer might realize they have done the wrong thing.

Lola: the XU impacts different people differently. Users with different cognitive abilities can be confused in different ways. 

Matthew: I looked at it also but didn't get time. If there's urgency we should publish a position. 

Lola: There's doesn't seem to be any urgency for it. So it's ok to wait another week. Matthew and I will look at it over next two weeks. 

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

Luke: we discussed this before and there's a breaking change.  But the breaking change is limited (to clip?). I'm convinced that... they have a usage counter that is very high, around 10% but it's unclear what they are using it for, so there's risk if it breaks stuff... so there is a compat risk. Ehsan had some concerns about the compat issue, so maybe he should have a look. 

Ehsan: sure, I can have a look. 

Luke: If the question is whether developers would be confused by this change, probably not, because this gives better behavior. 

Lola: Ehsan will review and we will figure out the closing comment.  

### [design-reviews#1146: Incubation: Proofreader API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1146) ([Github](https://github.com/w3ctag/design-reviews/issues/1146)) - @matatk, @toreini, @christianliebel

Christian: this is still pending external feedback. I would also say that this has timed out. 

Lola: setting as timed out seems appropriate. 

### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @ylafon, @marcoscaceres, @christianliebel, @lukewarlow

Christian: The WebApps WG met earlier this year to discuss how to install web applications. Marcos and I need to meet with the browser vendors and other folks again. 

Christian: This is their third iteration. I spoke with the proponents and already said it's unlikely the TAG's general position will change. The architectural change of this iteration is pointing to the manifest instead of the document to install.

Marcos: Feels like they would ignore the previous feedback and ask for a review as if that would not exist. Think we need a TAG finding around installed web applications. I think we need to settle this matter. Think we should help to set the direction here.

Luke: from previous discussions it seems to be around cross origin concerns. The proponents are very interested in the cross origin use cases. We can continue to look those aspects. It could be that we tell them that getting same origin over the line is ok. But yes, there's a discussion to be have a general discussion about what PWAs are. 

Christian: +1 to what Marcos said, maybe we can do this during the f2f, so hopefully help settle it. 

Marcos: Difficult to give the feedback as the premise on which the API is built, with my WebKit hat on, feels flawed. It’s a philosophical difference, and we need to document this. The choice has real impact on the web. To Luke’s point, I don’t think we can’t discuss the API without settling the underlying matter.

Luke: There's two opposing opinions here, I don't think TAG is ever going to change Apple's opinion and I don't think Apple will convince Chromium of their position. I also think there wont be consensus among TAG on this, so while I think we should absolutely write a document on this. I'm not sure if making it a blocker for providing feedback is going to work out.

Hadley: Seems there is still value in documenting there’s different philosophies.

Marcos: Don’t think we had the chance to present the matter to the TAG. I would like to do this.

Lola: Sounds like we should add this to the F2F agenda.

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242)) - @matatk, @christianliebel



### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh, @lukewarlow



### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres



### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon



### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk



### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola



### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven



### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow



### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh



### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh



### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini



## Plenary Session - None


<!-- Reviews that have been pending external action for at least 6 months -->

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven
### [design-reviews#1183: Incubation: new speculation rules action: prerender_until_script](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1183) ([Github](https://github.com/w3ctag/design-reviews/issues/1183)) - @dandclark, @xiaochengh

### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

