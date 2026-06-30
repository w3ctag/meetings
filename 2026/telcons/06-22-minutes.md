# TAG minutes, week of 22 June 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/06-22-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-06-24](https://www.timeanddate.com/worldclock/converter.html?iso=20260624T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attendees: Heather, Dan

Cancelled due to lack of quorum

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov
### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres
### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan
### [design-reviews#1233: WG Revision: CSSPseudoElement](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1233) ([Github](https://github.com/w3ctag/design-reviews/issues/1233)) - @bkardell, @xiaochengh
### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh
### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel
### [user-agents#2: Do we need a "discretion"  duty?](https://github.com/w3ctag/user-agents/issues/2)
### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu
### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu
### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu
### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu
### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin

## Atlantic Breakout (America / Europe) - [2026-06-24](https://www.timeanddate.com/worldclock/converter.html?iso=20260624T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attendees: Heather, Dan, Matthew, Christian, Marcos, Mike
    
Primary Scribe: Matthew

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @lolaodelola

Heather: I'll take this one.

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Yves: I looked at the PR they are submitting. It's not very clear. E.g. it throws an error, but then does it stop processing? Need a clear understanding of what they want to do. The goal was not to document what past parsers do, but going forward, if there's a new version, how this works with new 1.2 parsers. We need the behavior to be more clearly specified. I'll follow up.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Matthew: Ehsan's revised his comment; needs feedback.

Heather: will ping Hadley.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Yves: I still think this is worth doing. Not sure what Brian's current line of thinking is.

Marcos: I'm worried this is going to eat up a whole bunch of the TAG's time. I think it's important; needs to be done eventually, but is it a priority relative to the other stuff we have at the moment?

Heather: what about a timeboxed conversation at the face-to-face?

Marcos: +1

Heather: I'll add it to the GitHub issue for the face-to-face.

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

Heather: Mark Nottingham blogged on this recently. Don't think we've got back to the WG.

Yves: ...DNSSEC.. could be vulnerable to man-in-the-middle attacks. Concern about using well-known for service discovery. I don't think DNS is the right option.

Heather: there's no good solution but is there a least-bad solution? The group could do with our help on this.

Matthew: I've seen a couple things recently that use ".well-known/" in a way that seems not appropriate. For example, we (as in one of the task forces in APA) about not using ".well-known/" because there isn't a one-to-one correspondance between an origin and what some users would consider a "website." The well-known is too globa for that. I've seen a couple things where it look slike people are using well-known because it's well-known, but then they have to invent their own layer of structure to accommodate a more nuanced definition of "website." This seems like a common enough pattern that we might need to look at it directly.

Heather: I know service workers is having a similar problem. Microsoft in particular is interested in this.

Heather: Could add to the f2f agenda - see if we can find a better path forward.

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Mike: Moving forward with Heather and Ehsan. We are consolidating input. Expect to post a comment tomorrow.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Marcos: Will check to see if there is a WebKit position published on this

### [design-reviews#1223: Other Spec Review: Responsively-sized iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1223) ([Github](https://github.com/w3ctag/design-reviews/issues/1223)) - @dandclark, @toreini

Dan: Will reach out to @toreini to determine what the mutual position is

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

Matthew: See my comments; if others have suggestions, please add. I will work more on this next week.

### [design-reviews#1236: Other Spec Review: `textStream()` for `Blob` and `Body`](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1236) ([Github](https://github.com/w3ctag/design-reviews/issues/1236)) - @dandclark, @lolaodelola

Dan: Worked on this with Luke and Lola; will work up a comment.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

*bump*

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

*bump*

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

*bump*

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

*bump*

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

*bump*

### [WebMCP](https://github.com/w3ctag/design-reviews/issues/1238)

Marcos: Intro to it... We have AI agents. They are being integrated into all sorts of software, including UAs. The agents can look into a page, figure out what the user is doing here and how can they help (give a summary of the page, or fill in forms, tools/tasks users might need help with). An example might be booking flights for the user (can help people for whom calendars present usability or accessibility barriers).

Idea of WebMCP: web pages are hard for AIs to figure out. We may need to do visual analysis. WebMCP gives agents data structures that, for example, describe a search form to the agent, which is more digestible. It will descirbe the inputs and outputs. We are defining tools (the web apps) that the agents can use to do tasks for the user.

Heather: what fundaementally makes WebMCP different from MCP?

Marcos: The explainer acknowledges this is a misnomer. MCP is a protocol layer Anthropic came up with. This uses concepts from MCP but isn't that. So it mirrors what MCP is but it isn't MCP.

Matthew: This is describing tools - the web apps - that have capabiltiies that your agent in the UA can then use.

Marcos: There are two parts to this - e.g. you could ask the agent to write you an email. Right now, the whole thing (including the subject) will just end up in the 'body' field becuase it doesn't understand the structure. WebMCP allows you to specify where is the subject, the body, etc.

... This is about in-page tooling (not things like (native) apps that the agent could open to do a task).

... I've tried to describe it factually. WebKit found some problems with it, which I will go into...

... It gets interesting when we consider the tooling and agents behaving as assistive technology.

Heather: Checking standards positions. Mozilla thinks it's interesting; monitoring what happens. WebKit is negative. Does Chrome have a position?

Marcos: They're the proponents. (I opened the TAG design-reviews issue.)

Heather: I feel like we need time to read this through in order to have a sensible conversation about it.

Marcos: One of the considerations architecturally is what primitives is this seeking to add to the platform.

Matthew: I haven't read the WebKit position, yet. I have some concerns, but I'll save them until tomorrow

## Eurasia Breakout (Europe / Asia / Australia) - [2026-06-25](https://www.timeanddate.com/worldclock/converter.html?iso=20260625T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attendees: Ehsan, Matthew, Hadley, Christian, Marcos, Yves

Scribe: Marcos

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh


Matthew: still working on it. Hopefully next week. 


### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: we are largely ok with this. We asked them about contain and cover. They came back with solution that wasn't idea. But Lola didn't want to block on it. We can't really change it because it's layered with scroll driven animations. So we probably close it.  The concern was that the solution would be confusing to developers, but they said they hadn't recieved such feedback. But becasue they haven't received nagative feedback or confuion, it doesn't mean that there isn't confusion out there. However, we are not going to block. 

CL: Lola comes back next week, but it would be great to Lola's input. 

MK: Drafed a response that we are satified. Waiting on Lola to give a thumbs up. 

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: very good convesation with proponents. Was going to check if the updated text will conflict. Don't think it will. I think we can proceed with "satified". The proponets have confirm around doing avengalism about it and get it into frameworks. There's not much left for the TAG to do, so we can just close as "satisfied" 
 MC: has there been standards positions? 

Matthew: Mozilla is positive. WebKit is questioning as to why this didn't got to HTML.

Matther: we could respond that it's looking good to us, but they should push for them to get a position from WebKit. 

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: We agreed on a comment, asked Mike West about it, and he came back. I’m happy with his response about my concern. What do you think, Yves?

Yves: Works because the processing of CSP and allowlist is explicit in the response, so we can close it as satisfied.

Ehsan to draft a final comment, discuss it with Yves, and close it as satisfied.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow

Matthew: Both Luke and Xiaocheng have raised good questions. Think the last comment in the private thread has a very specific and focused technical question which we should pass on to the proponents. Luke is expressing some concerns and created a demo. I think it would be a good idea to pass that demo as well. Plan is to draft a comment, want to leave it to Luke to pick up the demo and Xiaocheng’s concern.

Christian to ask Luke.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Matthew: we all agree that it is a good thing and something that developer want to use, and it has  accessibilty options. We could say that we are supported of the use cases, but there are areas of concern around accessibility. There is a thread that it should be able to render elements that are outside of the canvas, which is kind of a big deal from a11y. We are far from done from the all1y side. Lots of technical issues and lots of people are thinking about and discussions. We also see a good opportunity to leverage this to fix other things - like text having special control over glyphs? in text and animating those. We were unsatified with that proposal, but this could make things better... so there's some specific concerns, general concerns, and opportunities. So I think we could say that... i drafted a comment last night, but wanted other folks to check to see if it's fine with the rest of the TAG:
    
For TAG folks to have a look  (private comment)   https://github.com/w3ctag/design-reviews-private-brainstorming/issues/259#issuecomment-4794567175  

Christian: that makes sense.. let's have a look. 

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

Matthew: we need to give them some feedabck. This came in a while ago. Basically, I put in a very early draft that could be turned into a comment. Jeffrey wanted something a bit more concrete, but it might be ok. I can see why developers would want this. But this might be something that users might want to toggle this off in the browser. Do TAG members agree with this overall feature? We could take my initial text as a draft... there's some significant a11y issues that have gone quiet, so we could poke them. 

Christian: turning it into a comment seems reasonable. 

Matthew: there's not mozilla or webkit position yet. 

Christian: seems that it's all still in the discussion phase. 

For discussion
https://github.com/w3ctag/design-reviews-private-brainstorming/issues/263#issuecomment-4797237927 

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: conversation continues. I misunderstood one of the functions and confirming that details. But the fact that I understood it means that the propsal is a bit confusing and could use some clarity. There's some other bits that are ambigous and could use a re-write. The feedback so far has been good with the editors. In general, I'm positive. 

Yves: ... we remamed to that it's server authentications. 

Ehsan: that's one of the changes is one that let me understand the prposoal better. In general I'm positive.  

### [design-reviews#1214: [wg/math] Math Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1214) ([Github](https://github.com/w3ctag/design-reviews/issues/1214)) - @christianliebel

Christian: I have a draft commnent., 
https://github.com/w3ctag/design-reviews-private-brainstorming/issues/269#issuecomment-4797233220

Chrstian: I added you comments. Matthew. Do you want your comments and concerns to be integrated? The one from April.  

Matthew:  notes on MathML... haven't seen a group do this before. It's stuff that I havent' seen groups take this approach before. It's good that they are focusing on a11y. I think it's fine to leave it as what you've got. 

Christian: I'll go ahead and post the comment if that's ok. Probably just say "satisfied". 

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

*bump*

### [design-reviews#1228: Other Spec Review: overscroll-behavior: chain](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1228) ([Github](https://github.com/w3ctag/design-reviews/issues/1228)) - @lolaodelola, @lukewarlow

*bump*

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

Matthew: APA is currently reviewing this. It seems good. APA has some questions in relation to some new roles.. .added new "sectionheader" and "sectionfooter" roles. I was concerned about them being new landmarks. But they are not, so I'm still waiting to hear about how these new roles will be used. There's a new ARIA notify API. It is an alternative to the existing live regions, which are regions that get announced to the AT if something changes (e.g., think like an auditory status bar). The declaritive way to do it is live regioins but doesn't work for some cases. Here is where an imperative API is simpler and very privacy preserving. It's a good example of a "author proposes, user disposes" principle. 

Christian: how do we move forward here?  Wait for Lola to return? 

Matthew: they changes are not exactly architectural. I could draft it and maybe get someone else on the TAG to reivew it. The are on a deadline so maybe we can just post it this week. The deadline might be this week or early next week. 

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @christianliebel, @marcoscaceres, @matatk

Christian: Saw discussion from yesterday.

Marcos: Next step of the discussion is gathering the independent thoughts. Discussions around moving this to a WG. Independent from the WebKit position, I documented the concerns in the Slack. I am very concerned and ask the rest of the TAG to have a look. Might have the most significant impact on web architecture I’ve seen, and quite naively so. Needs a larger TAG reviewership because of the API shape and impact.

Slack: https://w3ctag.slack.com/archives/C03RSJGSCJD/p1779960423515319 

Matthew: I'm pretty concerned about this for a number of reasons, privacy concerns, whole sort of meta concern about this is very new. We don’t know where it’s gonna go. But: People want to do stuff like this. So if we’re going to say no, can we offer a subset or a minimal part of it that can be used by people to experiment (the web builds itself; people are going to want to do this, so if we can give them a safe way to experiment that won't impact the rest of the platform until it's mature, and we're really sure it's OK to add any part of it)? The Group is aware of the S&P concerns, but the work carries on. From a11y perspective, there’s a lot of potential. Discovering help for very prevalent minor-to-moderate impairments is very difficult in traditional interfaces (people don't identify the barriers they face as ones that could be fixed; they don't discover helpful features that are present). One position wrt WebMCP is that the semantics added here could be added through the a11y tree. Really interesting question, can see both sides of the arguments. Some of the consequences have already come up, where people are stuffing stuff into ARIA attributes that are for agents, not for people. … AT is for people … We really need to think about the consequences.

Matthew: Here's one of the issues I mentioned re accTree: https://github.com/webmachinelearning/webmcp/issues/91

Christian: Remain positive, but let’s collect all of the valid feedback and put it into a draft comment, that is true.

Ehsan: Worried about privacy, group knows about it, and my gut feeling is: This will be exploited. We need to be careful. How can we direct it in the right way without blocking it? Even if the privacy concerns are serious, I think this is going to happen, so we should steer it.

Marcos: Believe this is very bad. webkit is very against this. we've encouraged them to stop that work and make a new forum.

what I realy like is that this really touches now on the semantic web stuff. we now come full circle on every aspect of what hte TAG has done for the past 20 years or whatever. it's so important for accessibility, privacy, not replicating what the web already does so beautifly, so important not to hand the web over to machines in such a naive way. there are use agents that I already know doing simiar stuff without dumping this problem on developers and keeping it in a privacy-insecure way.

Christian: we need a bigger discussion on this. Let's pick it up in next week's plenary. 

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

*bumped*

## Plenary Session - None

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
