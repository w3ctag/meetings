# Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/07-20-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.


## Pacific Breakout (Asia / Australia / West America) - [2026-07-22](https://www.timeanddate.com/worldclock/converter.html?iso=20260722T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Cancelled

## Atlantic Breakout (America / Europe) - [2026-07-22](https://www.timeanddate.com/worldclock/converter.html?iso=20260722T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair:

Scribe: Mike Pennisi

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/07-20-minutes.md

Raw minutes: ...

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @jyasskin, @marcoscaceres, @bkardell

Brian: Martin Thompson had originally opened an issue suggesting that the definition about web view libraries that aren't exactly user-agents might be required to provide user-agent duties. The discussion tended toward mini-apps, and then Heather suggested that the doc was pretty good on its own without explicit labels. I mostly agreed. My question here is, "what if that content isn't your domain? Does that matter?"

Lola: Why would that matter?

Brian: If you own domains, and  you're serving them, does that count? You could lose the hosting. It's a different thing to be serving content over the web versus not. I'm curious about others' thoughts on that. Also, there isn't currently really a way to do this other than to build a built-in profile. You could pre-install a Service Worker--it's not really external, but it's acting as if it were. There are a lot of ways to think about this, and I'm wondering if we want to be thinking about it differerently. Or if we should just consier this sufficient and close the issue.

Lola: I'm struggling to see why it would matter, so I'm inclined to say, "leave it as is." But I'm also really interested in alternative perspectives, so maybe we want to wait for Heather or Marcos.

Brian: I'm happy to close it if the answer is, "no." I do agree with Heather's point that where it might be useful is acting as a user-agent (more explicit and observable). It's not clear where that line is, and I guess that's part of it... But if people agree, I think we can close this issue.

Ehsan: Is the main concern here cross-origin? If you can formulate that, then we might have a better discussion.

Brian: When do you have to abide by the duties? The bullets that are suggested here: rendering external content (and two others). If you're serving it off of your domain (as opposed to something that's installed)... It's easy to get around this by just side-loading content. I think there's something missing here about, "Are you acting according to the user or not?"

Lola: If you're serving it from your own domain, then surely that means there's just one user, and it's you. I don't know if that would change whether a thing is a user-agent.

Brian: Maybe it doesn't.  If you're building a product, which domains you control at this point in time is arbitrary. You could control 10 domains or 0 domains. The question is: what does it mean to render external content? Or move people between two origins?

Dan: If I'm using a web view ot render documentation for my product, and it can only navigate to that, it doesn't seem like a user-agent. The distinction, maybe: "is there a static set of documents that this thing is used to view and that are enumerated beforehand?" Even if there are multiple domains. But if the user can "escape the cage" and get to the broader web, that seems different.

Brian: I agree with what you're saying. It gets tricky if your static document viewer uses jQuery from a CDN, now you own the duties, right?

Lola: Additionally, the line starts to blur because we get into the original part of the issue: mini apps and super apps. They do things differently, but I would argue that they are still user-agents because they do things on behalf of the user. I just think if you are going onto a website, regardless of whether the website is static, regardless of accessing other domains--if it's doing things on behalf of a user, then it is a user-agent.

Matthew: I tried to write an enumeration: local or static documents, domains you control (versus other domains) with caverats for external references. Then this notion of "when does it become a user-agent?" then we can be more clear. "If this happens, then congratulations, you are a user-agent"

Yves: It's all about trustworthiness of information and int he case of a CDN, you have intermediaries that can transform what is sent to the web view or whatever is presenting ot the user. Then you also have different secruity models based on the application you are using. If it's a full-fledged user-agent like a web browser, that's different from a web view. We might want to figure out a minimal set of rules that any web view must abide to. You can say that a web browser is a web view with extra things. Mini-apps is doing the same thing: a web view with an added security model and added capabilities. It would be good to have a minimal set of required behavior from a web view. It relates to adding different security models, as well.

Ehsan: This is a bit confusing than converging, but I'm going to say it: when we're talking about cross-origin, twe're talking about different domains. What about users on the same OS calling from different components? One from the OS service and another from the internals of the user-agent itself.

Brian: To me, that's what's kind of interesting about it. As I've said before, this embedded community group is talking about all manner of these problems, but we don't have a standard way to frame them. I like the idea of articulating a set of bullets. Heather has some, already, but I don't know if there are enough right now. It's all over the place: Chroms has a Web UI, and MS and Chrome are both erowkring on it, You can make a browser out of a web view, just with more HTML and CSS and JavaScript for the window parts. How does all that stuff fit and work? Anyway, I don't know if we're ready to close this issue.

Lola: We can leave it open for Heather and Marcos.

### [user-agents#22: Implementing the web platform](https://github.com/w3ctag/user-agents/issues/22)

Brian: Maybe someone else cn have a look and see whether they agree. Martin had opened a thing, and it seems like there have been several merges. If I could get a second pair of eyes...

Lola: I think it should be Marcos mainly because you're asking whether the things that have been merged address Martin's comments. I think Sarvin is an editor, as well. I'll assign them.

### [user-agents#35: what constitutes a "credible commitment"?](https://github.com/w3ctag/user-agents/issues/35)

Brian: I don't think we can deal with this here. It needs discussion. Heather was discussing. I may have been discussing with her in the channel...

### [user-agents#49: Init Introduction](https://github.com/w3ctag/user-agents/pull/49)

Lola: This has been merged, so we can skip it

### [user-agents#50: Add example for honest user agent communication](https://github.com/w3ctag/user-agents/pull/50)

Brian: I pinged Martin, and he said he was confused by the wording. I wanted to bring this up because in issue #4, Jeffrey said that we need examples of these things. I'm not sure what those look like, so I wanted to provide one and see if we agree that is how it should be. This is another alternative. We can let him reply, or if anyone else wants to comment...

Lola: We can let Martin reply, and if he says, "yes", then the editors can merge.

### [user-agents#51:fix 'should' appearing in example (only case flagged)](https://github.com/w3ctag/user-agents/pull/51

Lola: this has been merged

### [user-agents#52:Cite [evergreen] finding](https://github.com/w3ctag/user-agents/pull/52)

Lola: We can skip this (because it is merged)

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: We can skip this

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: We can skip this

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Matthew: I'm working on a number of proposals. I'll colect them in an issue comment, but there's nothing to add here at the moment.

Matthew: By the way, we have the issue thread for face-to-face issue topics, is there some place to see the state of those?

Lola: We usually have a Chairs meeting every week, but we skipped because I'm the only chair availabel this week. So if you can give us a moment, we'll pick a thing (probably the spreadsheet) and then move things to that thing and do what needs to be done.

## Open Design Reviews

* [design-reviews#1223: Other Spec Review: Responsively-sized iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1223) ([Github](https://github.com/w3ctag/design-reviews/issues/1223)) - @dandclark, @toreini

Dan: Thanks for everything on this Ehsan. I think we may be able to merge. Is there more to chat about here? Or just waiting on follow-up?

Ehsan: I don't have anything to follow-up, so we can wait for the proponents to get back to us.

### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

Ehsan: For this, I think we didn't have a lot of discussion. At least me and HEather. Either today or yesterday there was another post saying that it's been updated. My points have changed in the new development. I'm drafting something, and I hope that I will soon submit my opinions on the private brainstorm for Heather to review.

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242)) - @matatk, @christianliebel

Matthew: I have not made progress on this, yet. Sorry!

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

Yves: The only thing I had to do was to give a heads-up for them, and it's scheduled for the face-to-face.

### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk

Lola: We can skip this because it's part of the same thing

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @hlflanagan, @lolaodelola

Lola: They responded publicly to request an update. Separately, Heather has published a draft comment, so I should tell them that we'll get back to them within the next week (because Heather is away and she had questions in her draft comment that I can answer in the mean time).

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

Matthew: I need to check on whether, as we think, they plan to do Braille in the next revision of the "notify" bit. The last we commented on the aria-notify explainer, we said that we thought--I'll check there in the aria-notify explainer.

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Lola: We can skip this

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

Matthew: I proposed a ocmment fot this. It really isn't perfect--it needs some copy editing (which I can easily do), and I wanted to try and get to a concern which is, "are we heading for a local maximum?" Is there a different condition that could apply more broadly? I listed this in the "gaps" issue #15. I wanted to tease something out about that from them. That said, overall, it clealry addresses good use cases. I ust think we can address evren more. So I'm interested in expansion. That's the view I failed to articulate in this draft comment. My draft has more specific bits of feedback. For the copy editoing, I can edit the comment directly. For the "local maximum" thing, I'll follow up later. Anyone who wants to review the comment: I'll be adding, not changing something that I've already written

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Lola: This is for the face-to-face, so we can skip it

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Matthew: I don't have any updates for this, sorry

Luke: I believe we're waiting for a comment.

Matthew: I was suposed to be drafting a ocmment.

Luke: We could integrate, or maybe we could get half of the comment out and then come back with a follow-up about recent developments in text metrics.

Matthew: I love that. I have a draft that I can turn into a comment by tomorrow's meeting. I'll do that.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Lola: This was discussed in the Privacy Working Group last week, and there was a lot of discussion, actually. The propoonents of the proposal were also in the call.

Ehsan: They have not released the minutes as of one hour ago.

Lola: The overall vibe is not positive in terms of support from the Privacy Working Group. Quite a few folks spoke out against it for various reasons (including me, not as a TAG representative).

Luke: Were most of the objections a more philosophical? "We don't want this capability on the web?" Or was it about the implementation?

Lola: It was a mixture. There was a revieew of the specification which arrived via e-mail. That was more philosophical ("this is technically a good specification, but I object bringing it to the web"). Then there was a contingent that objected to standardizing industry practices if those practices are not beneficial to the user. I think that there is some techincal critique, but that there is also philosophical objection. It went on so long that we had to table it. The call was charged because we also talked about WebMCP. In both cases, they suggested that they could have a separate session with TAG.

Brian: Martin is one of the people who worked on the spec, and he was on TAG. It seems like he must have thought about users. It does feel like, in a sense, they are doing what they can to protect privacy (versus the status quo). It is better for users and worse along the business-practices lines. I'd like to read the conversation, but a thing that was recently brought up is that it is poorly-named.

Lola: Martin wasn't present on that call, for what its worth.

Lola: I raised a question that Heather had about the allow-list. That was what they said they will let the browsers handle. They don't want to dictate the UI. I said that the allow-list isn't about the UI. If there is a star in the allow-list, what happens to the actual permissions (not the permission box, but the wiring underneath it). The minutes are very paraphrased, so you might not get the nuance fo the meeting.

Ehsan: the core of my concern is that architecturally on paper, it looks okay, and the algorithms are well-established by credible cryptographers. I don't have any problem with teh core foundation. The devil is in the details. There are arbitrarily/loosely defined etails that leave a lot to the user-agents, and they can be very important in this matter. At the end of the day, we want someting that preserves privacy an that works well. I understan that there are a lot of frustrations around the model of advertising, but at the end of the day, the status quo is different from what TAG is advocating. We need to leave some room for innovations without blocking the whole thing. I understand there are frustrations, but I think it's an improvement over the status quo. That's a summary of my upcoming comment in the private brain storm.

Lola: I agree that I don't think TAG shouldn't prevent innovation, and I think that's something wihtin the W3C that various groups are wrestling with (not just the TAG). However, there is definitely an attritude of standardizing industry practice, and I don't think that's the right move, either. "The industry already does this, anyway, so we might as well, too." The industry does what it wants, often at the disadvantage of web users. That's what the TAG exists to guard against, after all. I think we need to think about the opportunity for abuse. Within the specification of third-party cookies, there is a direct call-out not to use it for tracking, yet that is still the primary use-case for third-party cookies. It falls on us to not only ask, "Does this improve the status quo" but also "is it beneficial for users?"

(Ending meeting here for lack of time)

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)



## Eurasia Breakout (Europe / Asia / Australia) - [2026-07-23](https://www.timeanddate.com/worldclock/converter.html?iso=20260723T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola

Participants: Matthew, Lola, Luke, Marcos, Yves, Ehsan

Scribe: Matthew

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/07-20-minutes.md

Raw minutes: ...

### [design-reviews-private-brainstorming#217: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217) - @csarven

skip

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: I've proposed a comment asking for some minor clarifications. Yves: what do you think?

Yves: LGTM

Ehsan: Overall, satisfied. No major concerns, but have asked them to make 2 modifications to the explainer. Should we wait for them, or not?

Yves: If it's editorial, it's up to them. If it's not editorial, we should wait.

Ehsan: Yes, technical changes. They seem to be in a direction that the group may be going in - need clarifications in the final spec (they are having discussions in their repo on fetch etc.)

Matthew: Would making the changes change it from a 'satisfied with concerns' to 'satisfied'?

Ehsan: Yes

Lola: I think you should ask them in the comment for them to make the changes, and then once they've done that, we can mark it as satisfied.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: for the f2f, how do we do better developer research? I'd like to propose a breakout session about it at an f2f. Unless there's a better solution for it and someone else is doing this? 

Lola: the WebDX (?) group solicits feedback and how they understand the web platform, MDN, etc. It may be worth speaking to Patrick or Francois about it. 

Matthew: it would be great to do it as a joint session. 

Luke: Image lazy loading doesn't work when scripting is disabled, for privacy reasons. But scroll-driven animations allow you to bypass that protection. Question has been asked about how this relates to scroll-driven animations.

Marcos: Identifying the oversight doesn't necessarily mean it's correct that you can do it. Maybe someone missed that case?

Luke: The discussions around image lazy loading were WHATWG, so different pepole to the CSS group. Seems like a lack of awareness due to the discussions being done in separate places. Should we make a TAG finding about this (or related stuff). I could be persuaded that we should just remove the restriction.

Marcos: Let's bring the people together and discuss. We could file somewhere - e.g. design principles.

Lola: Do we want to mention this in scroll-triggered animations review? We could mention we know it's not the cause, but could exacerbate the issue.

Luke: Worth a passing comment that we've discovered that scroll-driven animations can have this effect. This is specifically for image lazy loading (disabled when scripting is, for privacy reasons). Maybe worth a cursory look. Maybe worth us looking more hollistically and making a comment on all of them. May be that scroll-triggered animations doesn't have this problem.

Lola: could you make a one line suggestion for the proposed comment?

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

skip


### [tag.w3.org#101: Update Yu Sen participation](https://github.com/w3ctag/tag.w3.org/pull/101) - @ylafon, @hadleybeeman

skip


* [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

We have been waiting for feedback for 6mo - need to ping for an update.

### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @marcoscaceres, @christianliebel

Marcos: I think this will bring up things we need to discuss at the f2f. This is essentially the third time that an API like this has been requested. There's a problem here that needs a larger architectural solution. It would be great if other TAG members could have a look. At least one more person. Christian and myself are very close to this. I wrote the WebKit position on this, so I have opinions. I asked Jeremy Keith as well. He is very in tune with the developer mindset on this stuff.

Luke: I can review it.

Yves: Me too.

Marcos: I'll send the proponents an update.

### [design-reviews#1244: [wg/webappsec] Web Application Security Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1244) ([Github](https://github.com/w3ctag/design-reviews/issues/1244)) - @hlflanagan

skip


### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Marcos: Following on from our last discussion, the next step is to find time for them to come and join us in a conversation.

Lola: Privacy WG discussed WebMCP in their meeting last week. We didn't have time to complete the discussion there. Some strong opininons. They also wondered if we could have a Privacy WG, WebMCP, and TAG joint call. How does that sound?

Marcos: Sounds good but I think some key WebMCP contributors may be US West Coast.

Lola: Could just involve the people reviewing it.

Ehsan: I think that is a good idea; 1 hour wouldn't be long enough with lots of people; wouldn't lead to agreement.

Marcos: In the WebKit position I also said that we should have a workshop or simliar (multi-day) to figure out what is the agentic web, and positions, and do the standardisation properly. We need to solicit wider opinions. Good that we are getting some so far. As a community we need to create a new venue, have the discussion properly, and do the work in the traditional way that W3C starts work. Get people together, discuss the problem, propose a new CG or WG.

Lola: Two potential suggestions. First step: create a Slack channel and invite all the relevant people. At least have conversation going async there. In that channel you could schedule a series of meetings to discuss. Marcos, do you want to create it?

Marcos: Should do it on the W3C Slack. Will do.

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh, @lukewarlow

Luke: Looks mostly fine. Slightly less clear than I would've liked. Still need to check navigation API integration. Want to see if it's possible to do something more concrete.

### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres

skip

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

skip

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)



## Plenary Session - None

## Open PRs

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

## Open Design Reviews



<!-- Reviews that have been pending external action for at least 6 months -->



* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)




### Plenary Session

None
