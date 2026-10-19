# TAG Minutes - Week of 5 October 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/10-05-agenda.md).

## Plenary Session - [2026-10-06](https://www.timeanddate.com/worldclock/converter.html?iso=20261006T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair: Lola

Scribe: Heather

Attendees: Brian, Heather, Lola, Matthew, Ehsan, Christian, Marcos, Philippe


### [WebMCP Draft Review Comment](https://docs.google.com/document/d/1WWFmeylMPmUqTwhdfXligSMg9nZ8LeUFM5rjsyWjr00/edit?usp=sharing) - @christianliebel, @hlflanagan

Christian: We have a draft comment ready, drafted by Marcos, Ehsan, and me. The draft resolution is that we should be unsatisfied with the current draft as it stands, but not unsatisfied with the concept of WebMCP in general. There are feedback comments from Jeffrey still to be incorporated. 

Philippe: We don't want the AI industry to take over the web, but we also don't want to push them away when they come to us with this kind of proposals. We know there are still a lot of issues. We are working on charter refinement for a new AI WG which will include WebMCP in their deliverables. Concerned about highlighting IPR concerns with the name WebMCP as that seems to be outside the scope of the TAG. 

Christian: The naming may be outside the scope of the TAG from an IPR perspective, but it does still feel somewhat in the TAG scope because of the level of confusion that will come because this has nothing to do with MCP. 

Philippe: Yes, I'm only concerned about the second part regarding IPR.

Marcos: I'm ok to remove that.

Jeffrey: This is a place where it would be helpful to have the new labels we talked about at the f2f. It sounds like the draft is leading towards the declaritive direction, and we are good with that direction.

Lola: Haven't we told them that we prefer the declaritive version?

Christian: Maybe as a path forward, we could also split all the concerns related to agentic browsing in general to a separate finding, leaving only the WebMCP material in the finding. That would move some of the concerns to a separate document. There are some areas where it is breaking preferred architecture such as cross-original components; sometimes the user will want that in this instance. After we do that, we can talk about the resolution label.

Marcos: With the declaritive side, it is problematic as well because it allows enforcement of rules that should be in HTML itself. There's a risk of overfitting to a particular model through the descriptions. So it's not that the approach is wrong, but it could be probematic.

Matthew: I agree with Marcos that there are significant issues with the declaritive version. And I agree with Christian on the agentic baseline concerns. If I had to choose right now, I would choose the declaritive version. APA posted a lengthy comment to the group and they seem like they are going to engage with it positively. I'm also sensitive to the group's point of view that some of what we're saying is inherent in anything agentic. However, I would be convinced to not include that in this comment. We can demarcate which are general agentic concerns and which are specific to this spec, but if we put the general agentic stuff in a finding, no one who needs it will read it. It needs to go in this issue because this is the first time it's coming up, and so I think it needs to be all together. I think the comment is positive and encourages exploration. 

Christian: On declaritive vs imperitive, as a developer I think imperitive is more interesting. Which brings us back to the resolution label. We could call it "too early" as more stuff needs to be fleshed out. In the end, it gets the job done, it reuses concepts developers know, and at the same time it is an invisible layer of functionality and is potentially dangerous. 

Lola: Regarding where some of this should live, in a finding or in a comment or both, the adoption of any finding is incumbent on us to refer to. I think this is a really long comment and needs focus. The reader may hyperfocus on bits of it. We can always write another comment later when we have a finding.

Matthew: That sounds great, but I think we could put headings and stuff in this to make it easier to read. It was interesting learning their perspective on what they think developers need that drew them to imperitive; APA developers found ways to do most of it via declaritive models. I don't think this is about imperitive vs declaritive. It's that one of these approaches keeps an entirely invisible layer that the user does not have access to. We won't be able to pull that back if it goes to the imperitive version.

Jeffrey: I don't think they've sufficiently thought about how to do this in a declaritive way. But we have the extensible web manifesto for a reason. We can't predict everything people will do, and an imperitive way is a good way to let people experiment and form the paths we might follow. They use AutoCAD as an example; it can perform hundreds of actions that won't be visible. But there will be declarative elements that will let them build menus. The imperitive version will be a stepping stone.

Marcos: I'm worried that if the imperitive side goes ahead it will dominate, because that's what we've seen already. 

Brian: You're not wrong that there is a risk, and I agree with the concerns. But I also agree with the issue of whether we build a thing that no one will use because they're doing something else already, we become irrelevant. Even a mediocre, standard solution will offer dividends for decades. My concerns is more that it's early to give this any kind of yes, so I'd say it's too early to say yes and we have concerns but keep experimenting. 

Lola: The current comment does not say "don't do this", it says "there are good parts, bad parts, please experiment further." So I don't think we're giving any definitive answers right now. This seems more like an early review. 

Christian: And what about "fixing" the imperitive version and forcing it to display tools the website is using - I think the imperitive version can be fixed. Maybe it helps if we just don't call it unsatisfied. I would support "too early" as a label for this. 

Lola: I don't think this is too early. I agree we should be strategic in how we label this and communicate it to the proponents, which is another push for the comment not being so long.

Matthew: How about we put the comment in the issue thread without the line about the label?

Lola: I don't think that will work for this group given how they've received our attempts in the past at being clear. 

Christian: We don't have too many options, so maybe we need a new resolution label for this. 

Lola: We have new resolution labels on the agenda later today. 

Jeffrey: On the question as to whether to include the agentic discussion on the WebMCP position, I feel strongly we need to separate them. We have to expect that people are going to mostly ignore the agentic message. Agentic browsing is a bad idea and people are doing it anyway. To the extent WebMCP encourages agentic browsing, that's a harmful aspect, but for them to make an impact, we need to focus on what they can change.

Ehsan: I agree mostly with Jeffrey. Many of their discussions are in the spec. I think the ones directly relevant to the spec text needs to be maintained in the comment. The ones mentioned in the spec need to be clarified. The agent itself is confusing for me. Their textual comprison af their intention doesn't align with the definition of agent. They need to have more careful connection to that definition throughout the text .So I would prefer to keep many of the text related bits here and leave the rest for the finding. 

Jeffrey: I am open to seeing those connections.

Lola: We need another draft of this comment to separate what is and isn't relevant for the WebMCP proponents. Christian, please share an update to the comment with the TAG, and let the proponents know we're still working on this. 

### [process#52: Contact WGs to invite members to run for the TAG](https://github.com/w3ctag/process/issues/52)

Done.

### [process#50: Re-wording TAG review outcomes](https://github.com/w3ctag/process/issues/50)

Brian: My only comment is that there are fewer outcomes that are seperable as early. So, thinking about the one we were just looking at, how would we label that.

Lola: I think it would be an "Early resolution: concerns, significant" 

Dan: I don't think we want to block this, so maybe "Early resolution: concerns, non-blocking"?

Lola: When you have an early resolution that has significant concerns, I think we should change the description to indicate the proponents need to keep working on the spec and address these concerns.

Dan: That makes sense. We should update the description.

Lola: Using "non-blocking" and "significant" feels unbalanced. It should be "non-blocking" and "blocking"

Jeffrey: I think we should say "should not become part of the web" not "should not be a recommendation". I would like a way to express excitement about a proposal. 

Matthew: One, regarding blocking/object as opposed to unsatisfied, Yves made the point that the f2f that we can't actually object (even though object is a more accessible word). People might misinterpret that as becoming a formal objection. As a horizontal review group, we can't really block. I really like the atomic approach to labeling that Marcos showed at the f2f. We should go to something like this, then make a decision later about adopting more atomic ones. Are there any existing labels that are close enough semantically that we would be renaming? It might be useful for doing queries later and doing historical-based statistics if we can rename the labels rather than to go an entirely different set.

Lola: I don't see why we shouldn't investigate Marcos' idea as well. Separate to this, I opened an issue on the GitHub bot on how we label things on the agenda. I want to have labels not just for agenda+ but also for which meeting we'd want to discuss the item. 

Matthew: Here's the example of WebKit's atomic labels: https://github.com/WebKit/standards-positions/issues/670

Lola: I think WebMCP would benefit from more atomic labels, but we need another proposal for what those labels should be.

Jeffrey: Could Marcos respond to the issue by taking the WebKit labels and translating them into TAG terms?

Marcos: Sure.

Dan: I'm not sure what the use case is for this? I can use labels to filter what the TAG has been doing for the last year, but is it useful to index at that level of granularity? Why not just read the TAG response?

Marcos: I find the labels offer a nice structure. It helps us think about what areas we'd want to consider in a response.

Lola: These labels are as much for the TAG as for the proponents. We tend to reference old decisions and if a new TAG can look at old decisions and see at a glance what the concerns were. Not all the old responses are clear as to what the TAG was concerned about as it was embedded in a series of comments. 

Heather: This runs the risk of getting out of control. We'll get hung up on the metadata as opposed to the comments itself. It's an attractive nuisance.

Brian: The thing that started this conversation was me saying "satisfied with concerns" was misleading. We have to label some things and the biggest one is "satisfied with concerns" is the most problematic. We can do a whole metarenaming, but if we could just clarify that one as a first step that would help. If you think there's something in this new list that would fix that, we could use that one. But I don't know what that would be in this table.

Lola: Christian, where would WebMCP fit here? Do any of the new labels map to what we've discussed?

Christian: I think it would be "early concerns, non-blocking" or "concerrns, significant". 

Lola: Would this be early or regular?

Christian: Early.

Lola: I think we need to dig further into clarifying the descriptions. I also don't think we should be treating early and regular the same way. I've added a comment to the issue. 

Brian: I think it's misleading to say we can block something, because we can't and it will just irritate people if we say that. It's more that we say "you should continue" and "we think you should cease and desist". Can we have a label that says "proceed with caution" and "please stop".

Lola: I don't think we'll get to something today. Please engage with the issue and offer your proposals. Marcos will add more information about how WebKit does this. 

Matthew: Remember that when we talk about indicating things, use the color and the shape. Semantic meaning in colors is a risky to depend on; we would have to make it very clear. And while "proceed with caution" and "please stop" may be abrupt, but they do get the point across. I am concerned we're going to get bogged down in this. If we can start by just fixing satisfied with concerns, we can do that quickly then consider the broader proposal. 

Lola: I don't think we're going to get satisfied with concerns in this meeting. We've already come up with three different ideas for that one. But let's focus comments on that one item by now so we have something ready when Christian publishes the WebMCP comment, and after we can iron out a longer term strategy for labels. 
    
### [state-of-3pc#1: Retire this finding](https://github.com/w3ctag/state-of-3pc/issues/1)

Lola: at the first f2f of the year, we were talikng about having a third-party cookie finding since it didn't seem like there was synergy for a solution. We wanted this finding to encourage people to settle on a direction. Things have changed since that timing and people are doing more to work together to align on a direction. So I don't think we need this finding any more. Does anyone have strong feelings about this either way?

<silence>

Lola: Then we won't work on this any more. 

### [user-agents#6: A duty of Negotiation](https://github.com/w3ctag/user-agents/issues/6)

Lola: Can we discuss in 2 minutes?

Jeffrey: Some of the ways user agents are loyal to users or ways they exist in the ecosystem is by collectively negotiating on behalf of users with websites. This comes up especially in the EME example where there are questions as to whether browsers negiotiated as well as they could have. I don't have good text to describe that.

Lola: if you have any interest in this area, please work with Jeffrey on this. 

### [design-principles#621: Add new fragment directive guidance](https://github.com/w3ctag/design-principles/pull/621) - @tabatkins

(Skipped.)

<!-- PRs -->
### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan

(Skipped.)

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

<!-- Design Reviews -->
### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @ylafon, @marcoscaceres, @christianliebel, @lukewarlow

Christian: This is ready, just waiting for final approvals from Yves and Luke. But it is what we discussed at the f2f

Lola: Then you don't need additional reviewers and can post this.

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

(Skipped.)

## Pacific Breakout (Asia / Australia / West America) - [2026-10-07](https://www.timeanddate.com/worldclock/converter.html?iso=20261007T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair: Heather, Jeffrey

Scribe: Heather

Attendees: Heather, Brian, Dan, Jeffrey


### [design-principles#619: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-principles/issues/619) - @marcoscaceres

<!-- PRs -->
### [user-agents#70: Focus only on web user agents.](https://github.com/w3ctag/user-agents/pull/70) - @jyasskin, @marcoscaceres, @bkardell

Brian: I am looking at this now. It doesn't look like Dom has replied; I'd like to know what he has to say about this. What's there does match what we've talked about; in our context, when we talk about user agents, we are talking about web user agents. I've left a comment. 

### [user-agents#68: Fix spelling and enhance user agent descriptions](https://github.com/w3ctag/user-agents/pull/68) - @marcoscaceres

<skip>

### [user-agents#63: Scope the arbitrary-content claim to the public web](https://github.com/w3ctag/user-agents/pull/63) - @marcoscaceres

Brian, Dan, and Heather looked at this and agreed with Jeffrey's proposed changes. 

### [user-agents#65: Drop the user activation claim from the multiple permissions example](https://github.com/w3ctag/user-agents/pull/65) - @marcoscaceres

Brian, Dan, and Heather likes Sarven's modifications and the overall removal of activation claim makes sense. 

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

Brian: I think this should be rephrased. It's not just about limits of time. There also limits of ability, an infinite number of configurations, so the current phrasing doesn't seem helpful. I do like Jeffrey's suggestion from two weeks ago, "widely usable by default."

Jeffrey: Your point about ability is reasonable. If we delete it, we could say later "imperfect developers" instead of "hasty developers."

<!-- Design Reviews -->
### [design-reviews#1224: Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1224) ([Github](https://github.com/w3ctag/design-reviews/issues/1224)) - @jyasskin, @hlflanagan, @xiaochengh

Jeffrey: I haven't done this yet, but will work on it.

### [design-reviews#1269: [wg/svg] Scalable Vector Graphics (SVG) Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1269) ([Github](https://github.com/w3ctag/design-reviews/issues/1269)) - @marcoscaceres

Brian: I think we should close this. It doesn't need a TAG review. 

Jeffrey: I agree.

Heather: I agree.

### [design-reviews#1277: [wg/pm] Publishing Maintenance Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1277) ([Github](https://github.com/w3ctag/design-reviews/issues/1277)) - @hlflanagan

Closed: satisfied, no concerns.

### [design-reviews#1276: [wg/did] Decentralized Identifier Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1276) ([Github](https://github.com/w3ctag/design-reviews/issues/1276)) - @hlflanagan

Heather: No concerns. Does anyone else want to look at this?

Jeffrey: They are now chartering a DID Methods WG, which is where more of my concerns lived. 

Closing, satisfied

### [design-reviews#1268: Other Spec Review: Registries developed by the Media WG](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1268) ([Github](https://github.com/w3ctag/design-reviews/issues/1268)) - @hlflanagan

Jeffrey: A registry is an interface. The things in the registry has to define the algorithms, etc, that the calling spec expects to be there. Otherwise you have undefined behavior and implementations have to guess. So it is important that registration rules say what is expected by this registry, and that needs to match what's in the spec. If that happens, no architectural review is required for the entries.

Brian: In this case, the registries all exist.

Jeffrey: I don't think these to have the problem I described, but we do have to check. Another architectural failing could be when companies add proprietary entries such that there is no real interoperability. 

Heather: I want to take another look at this with the above ideas in mind. 

### [design-reviews#1246: WG New Spec: Additional Windowing Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1246) ([Github](https://github.com/w3ctag/design-reviews/issues/1246)) - @jugglinmike, @bkardell

Brian: I would like to get someone else's thoughts on this one. I'm not sure this one makes sense for the drive-by web. It makes sense for somethings built with web technologies, but that's not the same thing. 

Jeffrey: I agree with the concern that this might not be appropriate for the drive-by web. 

Brian and Mike will discuss further.

### [design-reviews#1251: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1251) ([Github](https://github.com/w3ctag/design-reviews/issues/1251)) - @jugglinmike, @marcoscaceres, @bkardell

Brian and Mike will discuss further.

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Dan: I think Marcos' comments were addressed? When does this review time out?

Jeffrey: The proponents discussed a lot, and Marcos hasn't answered. 

Heather: I will drop a note to remind Marcos about this one.

Jeffrey: It is difficult to describe this entirely normatively, but it's also not clear where the line should be. We may jsut need to read where things are now to determine if it is all reasonable. 

### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

https://github.com/w3ctag/design-reviews/issues/1280 - Privacy WG Charter - ok to close with no concerns (Dan will close).

https://github.com/w3ctag/design-reviews/issues/1270 - Web Real-Time Communications Working Group Charter - Brian will close with no concerns

https://github.com/w3ctag/design-reviews/issues/1281 - audio group charter - Jeffrey will close with a comment to pay special attention to the Accessibility review

https://github.com/w3ctag/design-reviews/issues/1289 - Security Interest Group - Jeffrey will close with no concerns

https://github.com/w3ctag/design-reviews/issues/1279 - SVG textPath side attribute - Jeffrey will close with no concerns


## Atlantic Breakout (America / Europe) - [2026-10-07](https://www.timeanddate.com/worldclock/converter.html?iso=20261007T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair: Lola

Scribe:

Attendees: Heather, Lola, Sarven, Jeffrey, Dan, Brian, Yves

Regrets: Christian, Matthew

### [design-principles#628: Add the improve-existing principle](https://github.com/w3ctag/design-principles/pull/628) - @csarven, @jyasskin

Jeffrey: I haven't looked at this yet.

Sarven: There was an issue from Martin, https://github.com/w3ctag/design-principles/issues/539. A thread about JSON being maybe sufficient. It doesn't have some features. There's reinventing. This PR covers several aspects of "don't reinvent", even if something isn't perfect or doesn't have everything you need. Encourage authors/developers to extend what exists, or improve it in other ways instead of coming up with new formats or alternative specifications. When you invent new things, developers have to pick from the many options, which is a cost. I gave lots of examples in the PR. The cover different areas. Also an example of a good reason to accept a new solution. fetch() over XMLHTTPRequest. RDFa/microdata/JSON-ld. Tries to be positive, not just "don't reinvent." 

Brian: I made some comments but failed to send them. The URL standard tried to codify the parser that really existed, since none of the existing specs were really right.

Sarven: URL standard acknowledged RFC 3986. Don't know what you'd call that. Community was frustrated.

Jeffrey: Think the URL standard might not fit in this section. It didn't reinvent naming; it forked a spec, which has its own harms, but they're different.

Heather: Like the idea of examples. Reading through, you needed to know the backstory for the examples to make sense, and not sure if we should rely on this.

Lola: Good observation.

Jeffrey: So tell more of the backstory?

Heather: Might be political. E.g. in digital credentials, ISO and ?? did things, and now they're trying to harmonize, which causes complexity. Any examples where the new and old thing are still actively competing?

Jeffrey: RDFa/microdata/JSON-ld fight is still happening.

Brian: My other comment was about URI templates, fragment text directives, selectors states. Don't see what's an example of this or what should have been done. Why not mention xpointer? 

Sarven: The folks behind scroll-to-text have acknowledged selectors and states. Don't know how complexity is measured. Instead of squiggly, the word "selector"? scroll-to-text has parts that are a subset of selection. There was a call from folks behind selectors-and-states to the scroll-to-text folks that they should re-use it. Don't remember the rationale to not use it.

Brian: The suggestion here is that we'd be in a better place if they'd done that, and that's not clear to me.

Yves: There are still issues in the URL space between the URL document and the RFC. For fragments, the issue is that mime types define how the fragment is interpreted. For the browser, they defined the extension to bypass that. And that's probably the cleanest way to do it. 

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell
### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Jeffrey: I think we have a bunch of open PRs. We need to make progress on them. Explainer explainer is moving slowly, but I'm still overwhelmed by other things, so I don't want to add still more.

Lola: Got it; we'll give you a break

<!-- PRs -->
### [privacy-principles#469: Suggested new sub-section to 1.2 (Vulnerability), titled "1.2.2 Vulnerability Impact"](https://github.com/w3ctag/privacy-principles/pull/469) - @toreini

Jeffrey: Do we want to add this? This is the fiurst substantive change to the privacy prinvicpe since we published. I think it's headed in the right direction. We need reviewers and we need to update what it is we're doing with the document.. I'm going to reach out to Nick Doty and Christine Runnegar [sp?]. More privacy review is useful

Lola: Suspect that's enough. Their yes is worth 2-3 of our yesses. After they've reviewed, can bring it back.

Jeffrey: Once this is out, we should push out a new note revision and then ask the W3C Team to do something sensible with the note and position coexisting simultaneously.

Lola: TODO for Yves.

### [user-agents#71: Extend loyalty duty to organisations responsible for UAs](https://github.com/w3ctag/user-agents/pull/71) - @csarven

Sarven: Based on Heather's suggestion. Some editorial updates. Think it's ok. Jeffrey and Brian reviewed.

Jeffrey: I recently said that I think there may be a better way to do this, but I don't have any suggestions, so I think it's fine to go with what we already have.

Heather: I think it's good enough. Let's go with what we have.

Lola: Sarven can merge.

### [user-agents#66: Add an EME example of making credible commitments.](https://github.com/w3ctag/user-agents/pull/66) - @jyasskin, @hlflanagan, @npdoty, @csarven

Jeffrey: This is waiting on me to do a revision, but I have not done it.

<!-- Design Reviews -->
### [design-reviews#1264: Incubation: Filterable select](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1264) ([Github](https://github.com/w3ctag/design-reviews/issues/1264)) - @matatk, @dandclark

Dan: We posted and are waiting for a response.

### [design-reviews#1265: WG New Spec: Global Privacy Control (GPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1265) ([Github](https://github.com/w3ctag/design-reviews/issues/1265)) - @hadleybeeman, @toreini, @hlflanagan, @lolaodelola

Lola: Think this is open for tracking?

Heather: Brian had a comment that you wanted to rewrite it to be shorter. Wasn't 100% sure what "this" was. And did you see my comment?

Brian: Can merge Heather's comment.

Lola: Agree that the comment can be shorter than Ehsan's. 

Jeffrey: I think merging Heather's and Brian's comments is the way to go

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven, @ylafon

Yves: It's in Pierre-Antoine + the WG's court. They need to discuss our comments.

Sarven: Are they reviewing based on your feedback? You said it was a personal view; maybe they're waiting for TAG feedback.

Yves: There was a PR on their specification, and they over-worked it. Trying to figure out how to make things happen and make progress. Current state isn't useful for any subsequent version.

### [design-reviews#1273: WG New Spec: VCALM v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1273) ([Github](https://github.com/w3ctag/design-reviews/issues/1273)) - @hadleybeeman, @hlflanagan

Heather: I added a comment to this one, which boils down to, I have concerns about the scope and how it might be duplicating effort. Really want someone else with me, since I'm also chair of Digital Credentials, and this spec stomps on the same ground on purpose. Would be good to have someone not deeply involved, also take a look.

Lola: Hadley might be in a similar situation since her boss is the chair for this group.

Jeffrey: I said I'll take a look, but if someone else wants to take a look as well, that would be great.

Lola: Can we first ask why this is happening instead of them participating in other groups? 

Heather: They're trying to force the platforms to behave in a standardized manner. We don't standardize OS response.

Lola: OS, not web platform?

Heather: Yes. VCALM spec is pushing certain requirements, and they have a contract with California, which allows them to have an instance where it's useful. They can keep doing that and ignore the DC API because Apple+Google won't behave the way they want.

Lola: This is a web API trying to standardize how OSes work?

Heather: VCALM is trying to do a lot of things. DC API is doing 1 thing: web<->wallet. VCALM expands beyond that. Serves as that pipe and is also reaching a lot farther, to engage directly with the VCs that go back and forth.

Jeffrey: I think we need to develop a position before we join a plenary.

Heather: There's a join meeting at TPAC with lots of groups including this one. On Tuesday. This issue will be a big topic. https://www.w3.org/events/meetings/7f5ffe2d-c418-47f1-880a-36710212b347/

### [design-reviews#1253: Other Spec Review: CSS navigation-based styling](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1253) ([Github](https://github.com/w3ctag/design-reviews/issues/1253)) - @matatk, @dandclark

Dan: I posted some nitpicky explainer and API shape feedback a couple weeks ago, and Noam responded. Last question: do we have a take on introducing navigation information to CSS in this way? I think it's reasonable and would be happy to endorse it. Use cases are well founded. Have others looked? Matthew might have dug in. 

Jeffrey: I haven't looked enough to have an option, but it makes me think of CSS trying to interact with accessibility, so it's worth investigating further.

Lola: I can't have an opinion right now, but my spidey senses are tingling. I'll have a look and will give feedback.

Dan: Look for concrete reasons to maybe not like it.

### [design-reviews#1266: Other Spec Review: Scroll snap for single-axis scroll container](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1266) ([Github](https://github.com/w3ctag/design-reviews/issues/1266)) - @lukewarlow

Lola: Luke is no present, so we'll skip this.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Heather: I looked again. What Martin said handles several of the concerns. Were 4 things I wasn't sure about, and want second opinions.

1. Privacy parameters being implementation-defined. Let browsers differentiate, but if there could be some understanding of what properties should be guaranteed.

2. Aggregation service governance is a thing. Web PKI has substantial governance that isn't here.

3. Permissions policy might not resolve the "*" default. Why is the permissive 3p availability the right thing?

4. Not entirely comfortable with UAs taking on so much of this. Making the browser such an active participant in measurement that's not being done on behalf of the user. Whole different ecosystem All of that's in my comment; I hope other's chime in.

Jeffrey: Ont he privacy parameters being implementation-defined: there's a lack of consensus on what they should be Chrome will set them on one side; Safari and Firefox on another. Probably the spec should set Chrome's as the lower-bound. I think that's reasonable. On your third point (on permission polocy): all of the actual ads are done by third-party scripts, and the scripts run in the first-party context (which is not good), but we'd like them to run in an iframe. I think that's why we need the permission. 

Lola: Does that mean cross-origin?

Jeffrey: It's going to run in a cross-origin context.

Lola: This has been discussed in the Privacy WG twice I think. That conversation didn't go well. The group wasn't positive on the spec. An argument i've seen with Attribution and WebMCP is that the industry is doing it anyway, so we might as well do something. I'm not a fan of that. Similar to WebMCP, there's external pressure. aybe an existential question, about how we're thinking of specs that have some negative impact on the web's architecture, where we'd normally discourage them. How are we addressing things like that, vs the industry pressure.

Jeffrey: We are the group that has to make the trade-offs. The privacy group is chartered to promote privacy. Sometimes there are trade-offs. In this case, it's that the advertising industry is doing bad things when they're doing it just third-party. Blocking third-party cookies solves thast to some extent, but Chromium-based browsers aren't doing that fully, so in order to be fully compatible, Safari and Firefox have to do something. This is the "something". If we don't do that, then websites will just say "please use Crhomium", and users will receive the maximal tracking in that browser. It's our responsibility to determine whether that is a reasonable trade-off.

Heather: I think this discussion was the review I was asking for. I'll take the notes from this meeting and my comments and propose a response to see what we do. 

Lola: On the browser working on behalf of not-the-user, that's a comment worth keeping in.

Jeffrey: Some of the stuff we're currently adding to "user agents" addresses this. We should think about whether this design is an appropriate negotation, but we have the framework to think about that.

Sarven: I shared an article in Slack about AI company CEO saying "we need to accept some bad things" so AI can happen. The justification seemed absurd. In this case, it's an incremental improvement in some ways, but we might not want to accept it just because there might be something better.


### [design-reviews#1250: Incubation: WebRTC Diagnostic Logging](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1250) ([Github](https://github.com/w3ctag/design-reviews/issues/1250)) - @lolaodelola

Lola: Please review my draft comment.

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

Sarven: We had a response, they responded, we haven't responded. I looked over their response. I think we can be satisfied. The initial TAG feedback didn't have significant concerns.

Jeffrey: {thumbs up}

Lola: Thank you.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Lola: I think we can skip this; I think it's just a tracking issue.

Brian: Yes.

### [design-reviews#1254: Incubation: Cross-Origin Storage](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1254) ([Github](https://github.com/w3ctag/design-reviews/issues/1254)) - @ylafon, @bkardell, @dandclark

Dan: There's a draft PR on the explainer to make a change to decouple this from 3p cookies, which is one of the main concerns from our and WebKit's end. It's better than 3p cookies, but it's contingent on 3p cookies being enabled. PR had some feedback, and then it was marked as a draft.

Jeffrey: There's a question of whether to keep promoting this as a cross-browser feature, or, as I've suggested, to put it in a Chromium-only place.

Brian: The question of whether you can achieve it without 3rd-party cookies, and the shrug that goes with "it's no worse than 3rd-party cookies". The internal storage that treats a small number of sites specially was controversial among the Blink owners. Have they worked out something that more than just Thomas thinks can work? Even in the Intent, the data for the small list was underwhelming. I have doubts. If you could manage to figure out how to do this, it would be great, but it's not proven yet.

Dan: I can ask what the status is, and whether they intend to move forward with that they have in draft,.

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini
### [design-reviews#1249: WG New Spec: Recognized Entities v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1249) ([Github](https://github.com/w3ctag/design-reviews/issues/1249)) - @hadleybeeman, @hlflanagan
### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

Heather: I can't get past their site to post our CRA comment. Halp!

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow
### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven
### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk
### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini


### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)


## Eurasia Breakout (Europe / Asia / Australia) - [2026-10-08](https://www.timeanddate.com/worldclock/converter.html?iso=20261008T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair: Lola

Scribe: Sarven, Ehsan

Attendees: Sarven, Lola, Ehsan, Christian, Luke, Yves, Marcos


### [design-reviews#1275: [wg/lws] Linked Web Storage Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1275) - @csarven, @marcoscaceres

Sarven: I reviewed the charter, as Jeffrey and Marcos. I drafted a review which they approved, and also integrated their comments and suggestions. Made editorial updates. I can get into some details but I feel it is already in a good state. With Yves, we reached out to Pierre-Antoine to let him know the expected date for charter refinement was not clear as they posted two dates. Both informed me this is not a problem so if we agree after this meeting, we can post it and they'd be ok with it. What I noted, there are three areas that are concerning and the group should revise the charter (and possibly the work) based on them: interoperability, deliverables and scope, and data formats. The proposed charter is removing the guarantees for interoperability. Two conforming classes of products will not be guaranteed to interop with one another, while still hanging on to the justification in the motivation/scope that interop is important. The original charter contained incubated work and implenentation experience, and some guarantee of interop as it was building on prior work, but they removed that it in the new version, without actuall having similar or better demonstratable experience. The concern is that this will create clusters of implementations in the ecosystem not able to communicate with one another. Also, they are not building on existing specs without clarification on why there is a need for existance of another one.  The scope was another issue. They extended the deliverables - the restructuring is uneven -, and adding another about a year and half to the timeline for delivery while keeping the same scope, and there are concerns on that. The review request mentions that the initial charter was aggresively optimistic, but the proposed charter is more optimisitic and it is concerning (also keeping interop concern as mentioned). Data formats is another concern and it is clearly in conflict with the initial and proposed charter (i.e., new data format is out of scope) as the drafts introduce new media types. Last thing, in the fediverse/AP/social web ecosystem, there are a group of implementers that are concerned or confused about two media types to consider for AS2. That kind of awareness of the deployment experience doesn't seem to be taken into account before using that as one possible idea to rely on. In any case, besides introducing new media types in the drafted works, which violates the initial and proposed charter, which they shouldn't, the justification for it is not well grounded.

Lola: this looks good. Marcos mentioned that he does not think we should list all the specs and overlap. We should advise what group should take it. I don't see that in the text, but maybe we can do it, especially giving in direction to them.

Sarven: the charter already lists the groups to coordinate with, so they're aware. I like Marcos's idea to generalise and we agreed on that approach.

Christian: {thumbs up}

Marcos: {thumbs up}

Lola: ok, 



### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

<!-- PRs -->
### [societal-impact-questionnaire#39: Add circumstances of use and shared device consent examples](https://github.com/w3ctag/societal-impact-questionnaire/pull/39) - @csarven

Sarven: Marcos raised this issue. There were few points about it. This covers three points and two examples. briefly, shared devices if shared by many people, the one with privileges would know about what others do. There is also a typo. 

Lola: Marcos, can you review this as you were involved?

Marcos: yes

### [societal-impact-questionnaire#38: Add WebRTC example to the critical-part](https://github.com/w3ctag/societal-impact-questionnaire/pull/38) - @csarven

Sarven: this is about another example. If the protocol allows you to downgrade to something (like video/audio and there is no video or even text-only). This is to make sure people have all the resources available to prevent being locked out (like for job interviews, or online classrooms)

Lola: do you need any more reviewers?

Sarven: no, the examples are generally not strange. 

Lola: some examples are controvertial, but this one is not. I commented on one of them in github.

### [societal-impact-questionnaire#37: Add ActivityPub example to the centralization question](https://github.com/w3ctag/societal-impact-questionnaire/pull/37) - @csarven

Sarven: this is to make sure the web is not for browsers only. There are big servers with a lot users like social networks and people do visit them often, depite everyone can setup their own server. Not everyone can do that because it is costly. This is an example for that. I don't know if it a common example though.

Lola: I think that is good to me. Feel free to merge that.

### [societal-impact-questionnaire#42: Add non-malicious misuse](https://github.com/w3ctag/societal-impact-questionnaire/pull/42) - @lolaodelola, @csarven

Lola: this is an example that every misuse example is not because of bad intentions. The example was accidental misuse based on data breach of US health site.

Sarven: {nod}

### [societal-impact-questionnaire#40: Add people change during feature lifetime consideration](https://github.com/w3ctag/societal-impact-questionnaire/pull/40) - @csarven

Sarven: this was another point Marcos raised in the issue. I thought this is another topic so I added another PR. This is to point out people change and their profiles should be adjustable to take that into consideration.

Lola: you can merge that too.

### [user-agents#72: Use declarative language for 'provides'](https://github.com/w3ctag/user-agents/pull/72) - @csarven

Sarven: I noticed editorial incosistency and this is for that. I think it can be merged.

Lola: sure

### [societal-impact-questionnaire#36: Clarify questionnaire not limited to web user agents](https://github.com/w3ctag/societal-impact-questionnaire/pull/36) - @csarven, @torgo

Sarven: This was based on Dan's issue. Made PR to make it more clear.

Lola: we are changing to the user agent document.

Sarven: the PR in WUA is still open. TAG, I think, is ok with that. I suggested to wait for Dominique to have a look since it reverses an earlier PR that he made.

<!-- Design Reviews -->
### [design-reviews#1286: [wg/dp] Digital Policy Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1286) ([Github](https://github.com/w3ctag/design-reviews/issues/1286)) - @csarven

Sarven: this was recent. I have not done it yet. 

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @christianliebel, @xiaochengh, @lukewarlow

Christian: I did not look at it.

Luke: I did, I had the reviews and needed Christian's comment.

Christian: will do that.

### [design-reviews#1278: [wg/ARIA] [Accessible Rich Internet Applications] Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1278) ([Github](https://github.com/w3ctag/design-reviews/issues/1278)) - @lolaodelola

Lola: this looks fine to me. Any other one want to look? Matthew is not here and I will message him. I generally think it can be closed though.

### [design-reviews#1256: [wg/immersive-web] Immersive Web WG 2026 Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1256) ([Github](https://github.com/w3ctag/design-reviews/issues/1256)) - @marcoscaceres, @matatk

Marcos: I had no concerns. One was about PCM, but I will have a chat with them in TPAC on this.

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh

Lola: I dont think we need to do this for them. They should do it. I think it is not desired by the accessibility professionals, so it looks dissatisfied.

Luke: I agree. We have done a lot of discussions for this. I think there is a room to make everyone satisfied.

Lola: we can update Matthew

### [design-reviews#1245: Question: Review manifest-first Web Install API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1245) ([Github](https://github.com/w3ctag/design-reviews/issues/1245)) - @ylafon, @marcoscaceres, @christianliebel, @lukewarlow

Christian: Issue is closed, Rob responded, I will reply to him.

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

Luke: I closed that as satisified.

### [design-reviews#1263: WG New Spec: Verifiable Credential Barcodes v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1263) ([Github](https://github.com/w3ctag/design-reviews/issues/1263)) - @hadleybeeman, @toreini

Ehsan: My issue is that they have not clarified the priority of contituency on thtis, I have few more comments but pending Hadley's opinion.

Lola: any opinion?

Ehsan: I will ask Hadley for another review, but this is my main concern.

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Lola: we discussed it in planery. Some discussions on planery, that were leaning for satisfied with concerns. We proposed "proceed with caution". What would be the best way to help you Christian?

Christian: I need a label as long as it isn't unstaisfied. It seems proceed with caution seems fine but need final suggestion. In parallel, I am working on the finding for that. 

Lola: what would be the best for that?

Christian: ping me please

Ehsan: Did you look at the draft for agentic web Matthew shared?

Christian: I prefer to make them separate issues.

Luke: what would be the best way?

Lola: this is basically confusing and we want to avoid that.

Christian: we want to avoid people interpreting our concerns wrongly. I aim to share it with you soon.


### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

Luke: we have not posted an update since few months back. I think there is concrete feedback on that, but there is nothing fundamental change. They have been very good at responding in many occasions. We do want a closing comment that includes our discussions, but it will be non-blocking. There were some accessibility issues Matthew mentioned, I think no major blockers. 

Lola: the edit context seems a bit separate?

Luke: edit context already exists. The comment will be more focused on if there is any issues on the follow-ups and other APIs that they can interact with.

Lola: the main API allows you to include html in the canvas and the accessibility issues are related to that.

Luke: this has been updated and made it in wrapper element that can be used for various accessibility mappings to point that out. They have taken these feedbacks very good.

Lola: follow-up with Matthew on that.


### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres

Yves: to me it looks ok. I propose satisfied.

Marcos: yes, I agree

Yves: I will do that

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

Yves: i will check with Heather to make progress on this.

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

Lola: I think we can close it as satisfied.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Lola: this has been there for a long time. I want to know why. Matthew commented last two weeks ago. Matthew thinks it can be satisfied with concern for the accessibility reasons. Had anyone look?

Luke: I rememebr the conversations, I remember there was not agreement across browsers, Safari disagreed with this. I think we can close, sharing our thoughts. Considering the delay, the dissatisfied would not be helpful anyway due to delay.

Lola: anybody who thinks this is a good idea? We can consider no-concensus label.

Luke: I am leaning to the satisfied myself.

Lola: this already works across browsers differently with incosistencies. This might need more fundamental works.

Luke: the contrast is the problem and finding the balance on who holds the balance is the core issue.

Lola: ok, we should follow up with Matthew on Slack and we can figure out what to do next. 

### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)


