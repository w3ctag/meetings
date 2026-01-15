# TAG Minutes — Week of 12 January 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/01-12-agenda.md).

## Atlantic Breakout (America / Europe) - [2026-01-12](https://www.timeanddate.com/worldclock/converter.html?iso=20260112T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Jeffrey, Sarven, Christian, Yves
    
Regrets:
    
Scribe: Jeffrey

### [design-reviews#1171: [wg/dx] Dataset Exchange Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1171) ([Github](https://github.com/w3ctag/design-reviews/issues/1171)) - @csarven

Sarven: Reviewed https://github.com/w3ctag/design-reviews-private-brainstorming/issues/226#issuecomment-3734793121

Sarven: This charter ended, and they're renewing it with new deliverables. Group has been around for a while; other work items have been through related WGs. e.g. Government LInked Data. 3 items: want to continue maintaining Data Cube and Dataset Catalog vocabularies. New item is Variable Descriptions vocabulary. Some work is coming from the DDI alliance. Some work is coming from social sciences. Collections of surveys and research data. They want to standardize DDI alliance work via the W3C. Connects in some ways to the existing work. That's all great. Highlighted a couple things to reflect on: FAIR Principles (Findable, Accessible, Interoperable, Reusable). They mention that as a possible input. I'm a bit allergic to it: in the context of W3C specifications, FAIR is unnecessary and not particularly useful. It's too high-level. Don't bother mentioning it, although it's of interest in these circles. They gave the example of one spec that follows FAIR: RO-Crates. Continue mentioning that spec, and possibly concrete inputs.

Jeffrey: Justification for removing the FAIR principles shouldn't claim that the WG 

Sarven: I'll adjust the wording.

Lola: Can you explain why FAIR isn't relevant for W3C things?

Sarven: We have the Web Architecture, which talks about global identifiers. We have accessibility principles. Everything we do is interop. They have principles for how research should be shared, but when you look closer, the manifestation of these principles isn't always interoperable within their ecosystem. Some of the realization follows Linked Data principles, and some is off the web. The context here is for things that are on the web, and for that subset, we have the specifications and principles already.

Sarven: They have a long list of liaisons, and it's not clear which are important for normative dependencies, and which are just coordination. They could clarify that.

Sarven: I was involved in some of this. The DDI-RDF discovery is important, and they should consider whether it's important to include. We can suggest it, and let Pierre-Antoine work it out.

Lola: Sounds like there's a revision to make, and then people should comment on the issue.

Sarven: I'll update.


### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

Jeffrey: I put together an initial draft for the beginning of the document in a Google Doc, which is easier to collaborate on (https://docs.google.com/document/d/19K0CXPUvPaeM7OxaciOZl2gNoAQTK16SMWcUY6VZc7M/edit?tab=t.0#heading=h.ud7dyes4v2k). A lot to comment on.

… Overall, it could use some editing, they should have a look at a tech styleguide. Don’t have a definition of sustainability in this document, and they should have one.

…A lot of details: The talk about the guidelines and regulatory compliance, seems kind of backwards. Suggest to drop that they do this because of regulations.

…They talk about measurability, point at the WSG organization. They don’t justify how much impact things have. Suggested that they double-check that. They have a spreadsheet where they rated things along three axes (datacenter, network, device). Not every guideline breaks down well to those axes. For each of the guidelines, there’s a bunch of questions. Some seem redundant and could probably be merged.

… It may be better for people to skim the comments offline, and then I’d like to post it to see what they come back with, before we continue with the next sections.

Lola: Anything in particular you want things to double-check or comment on?

Jeffrey: Not really.

Lola: Should we say, "we've reviewed the first two sections" and then go on? Or do it internally, and give them a whole document?

Jeffrey: Normally, I would like to do the whole thing at once. As I found so many comments, I would like to do it step by step.

Lola: Wonder if we could split up that work. It might be good to have two or three more people on this, with every person reviewing a section. Suspect they want us to review everything. I don’t mind being assigned as well.

Jeffrey: Would love more people to review. Didn’t stop because it was so big, but the quantity of comments. May not be worth reviewing something that would have to change significantly.

Ehsan: I could also help.

Lola: Let’s give them your comments, and maybe it’s worth having a discussion with them. It may tie in with the societal impact questionnaire. Maybe there’s even an opportunity to collaborate here. 

… We will have a look at your comments, post it, and figure out the rest later.

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) - @csarven, @lolaodelola

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

We add 2 issues to agenda+.

### [user-agents#38: Define the general class of user agents that web user agents are members of.](https://github.com/w3ctag/user-agents/pull/38) - @jyasskin

Lola: Quick summary?

Jeffrey: PR elaborates on the difference between web, and AI and other user agents.

Lola: You need comments on your PR?

Jeffrey: Yes.

Lola: Will review this.

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Jeffrey: Matthew sent a comment last week, and we got a reply. Feel like the reply doesn’t change anything and we should close it as "unsatisfied." Feel a little uncomfortable doing that without Matthew.

Lola: Can you message Matthew?

Jeffrey: Sure.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Ehsan: Jeffrey and I commented. We decided on feedback. Asked last week. How long do we wait?

Jeffrey: We mark it "pending", so it doesn't come up on the agenda until they reply.

### [design-reviews#1179: [wg/vc] Verifiable Credentials Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1179) ([Github](https://github.com/w3ctag/design-reviews/issues/1179)) - @csarven

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola


### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Yves: Drafted a comment, and waiting for Ehsan to add to it. 

Ehsan: I'm discussing inside Samsung. I agree with your points, and will add 1-2 things, which need discussion. I'm wondering what happens if the CSP and allowlist overlap, or one is missing. Couldn't find a place that discribes the conflict. They should clarify the hierarchy, which takes priority. Second, maybe it can be used to fingerprint? Looking for a concrete example, but I think it can be used.

Yves: Think fingerprinting is probably less important and probably reuses the same thing as exfiltrating data. Except maybe a timing attack, since you refuse the connection before starting it. 

Ehsan: They mention something about side-channels, but they don't clarify.

Yves: Worth mentioning the possibility of problems so they can add it to the security considerations.

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: I have a draft comment based on last week's discussion. This helps developers migrate within the same site. Based on too many things that aren't part of the web platform yet. ID requirement and re-using scope extensions. We wanted to suggest an HTTP redirect.

Jeffrey: I'm worried that an HTTP redirect will break browsers that don't support this feature.

Christian: That's why not to close the review. But they should say whether this is reasonable.

Yves: It would be a combination of 301 + a content type. So they have the chance to act based on what's in the body. And the body can be content-negotiated. Do you both apps will be live at the same.

Jeffrey: I suspect so, since they'd leave the old one until users have migrated.

Yves: maps.google.com does redirect to google.com/maps. If it can use the manifest to also migrate data, that'll just help.

Jeffrey: I suspect that sites will be reluctant to redirect while some browsers don't support the full migration, to avoid the ugly second URL bar that appears when a PWA navigates outside its scope. But that supports Christian's approach of letting them reply.

Christian: The review starts with "we think this is a problem worth solving," but we should find the best solution.

### Appointments

Yves: Meeting of appointments committee will happen right after this. I might not attend plenary. 2 EU members and 2 US members. Will keep the chairs informed.

## Pacific Breakout (Asia / Australia / West America) - [2026-01-13](https://www.timeanddate.com/worldclock/converter.html?iso=20260113T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Martin, Dan
    
Regrets:
    
Scribe:

### [user-agents#33: Define "user agent" as distinct from "web user agent"](https://github.com/w3ctag/user-agents/issues/33) - @jyasskin

Martin: How you use the term seems fully consistent with how Marcos has laid things out in his feedback.  Seems OK to proceed.

### [user-agents#38: Define the general class of user agents that web user agents are members of.](https://github.com/w3ctag/user-agents/pull/38) - @jyasskin

Jeffrey: Made a change like the first you suggested. I think the second comment didn't need a change to the text.

Marcos: All seems ok.

Jeffrey: I will take Martin's change and then merge the whole thing.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

Jeffrey: [Repeats review]

Marcos: As a model, this is the right one, whatever WebKit thinks.

Jeffrey: Didn't like "garbage collected" since you're only supposed to collect garbage with no references, but the point is that JS does point to these things.

Marcos: Think it's inconsistent across UAs. They're all weak references.

Jeffrey: I used "released" in my question, but I'd like to get a sense of how the HTML editors want to refer to these things.

Dan: "Destroy a document" is a spec concept. I will also review this. Documents can also be "unloaded".

### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Martin: There are a couple suggestions. I found the example less compelling after our discussion and gave a suggestion. Also Xiaocheng.

### [ABCDE](https://github.com/w3ctag/abcde)

First look

Martin: Got feedback from Matthew. The basic sketch is in the repository. CG formed from a couple of TAG chairs, and a group of people who volunteer to do a low level of reviewing. Trying to be timely about the reviews, and look from a high level. The people who do the reviews can take in the design guidelines, and apply their own perspective, in doing a review of new work that comes in. Hopefully this can catch the basic stuff, with an extra pair of eyes on specifications. Details on how it fits together would be a next step. Haven't designed the details. I imagine that people sign up, say they're willing to do N reviews/year (1-2?). Pool of people who are available, and draw at random as things come in. Operate in parallel with TAG review process. If the reviews are timely, we can defer to them if they're good. Or migth decide to reduce the things the TAG looks at. We like fixating on the difficult review challenges, but there are a bunch of CSS things that haven't been a great use of our time. Could defer to a group like this to check that the explainer makes sense and give high-level feedback. TODO: HTML previews

Jeffrey: If it's public, GH Pages work.

Martin: Wanted the TAG to check it first.

Marcos: Sounds ok. Picking at random might not find the right skillset, but people could say what area they want to focus on.

Martin: I like the idea of it being a collection of generalists. But there are a number of ways to approach that, if people have interests, could pick them more aggressively for particular topics. Breadth rather than depth. But we'll have to adjust it. With the IETF directorates, there's a generalist one that uses random allocation. The specialist ones have the chair pick a particular person.

Marcos: Something like that could work.

Martin: Would be nice to have tooling that suggests a random person, but could flag that particular people have expressed interest in particular areas. Chair could choose that option. Key to managing this is that it doesn't ask too much of any one person. The less we ask, the more people will volunteer. Want a lot of people.

Martin: In the IETF, review quality is uneven. The Area Directors do some work to filter out the bad reviews. The TAG can serve that purpose. Could reduce the TAG's workload. It's a good system.

Jeffrey: I personally don't like the ABCDE name: should be more straightforward. We'll also need to widely review this charter. Heather Flanagan and the AB had opinions.

Martin: TAG, AB, Horizontal leadership, chairs of groups.



### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Plenary Session - [2026-01-14](https://www.timeanddate.com/worldclock/converter.html?iso=20260114T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Martin, Matthew, Lola, Ehsan, Yves, Xiaocheng, Christian, Marcos
    
Regrets:
    
Scribe: Martin

### Discuss TAG appointments - @ylafon & co

Time to talk about appointments!

Shortlist is in place.  Yves shares some names that won't be minuted.

Lola: How is the team deciding from this list.

Yves: First, we'll ask if the people are available and willing.  The task force will decide from those that are available who are the best fit and balance for the TAG.

Jeffrey: You don't have a sense for who is actually available.

Yves: No.

Jeffrey: Trying to think about what combinations would be bad.  Maybe a heavy overlap in expertise.

Yves: The goal is to find a mix of expertise to maximize coverage.

Xiaocheng: asks for a list of names.

Jeffrey: This is highly confidential right now.  Please do not share.

Jeffrey: Is there any people on the fence and is there something the TAG can do to make it easier for them to participate?  Something for us to consider and for the task force to maybe help us learn.

Lola: There might be a missing piece in the job description about motivating people to join.  What are the benefits of someone joining.

Yves: Agrees.  Even for new TAG members, describing those things.

Matthew: When elections are up, the description of time commitment is not always realistic.  Maybe we can delay an update until we get the CG process active.

Jeffrey: We are hoping the CG will shift workload, but we shouldn't bank on that.
... We should seek to improve gender diversity if at all possible.  We are a little unbalanced in that regard.

ACTION (yves): provide the list to the TAG, in confidence

### Meet the TAG in London - Matthew

Matthew: I think I have worked out how to host this.  I spoke with the team that organize the events at Samsung KX (Kings Cross).  They have a stage, seating, capacity for 120, places for snacks and drinks.  We need to have Samsung on the banner.  I've copy-pasted the agenda from the meeting in Hong Kong.  They are keen.  We need official approvals, which might take a week or two.  Tentatively booked for the 4th.  We might consider the 3rd.  We can't do the 5th because of Martin.
...For timing we have 1900 (when the store closes) to 2145, although that is super-hard.  Everyone absolutely has to be out by 2200.
...London means we might get a lot of people.  It's a very central location, very well connected.  There will be a registration desk, which we might need to help out with.  Not sure what we want to do with ticketing.
...Catering: list of companies they work with.  If we do drinks and maybe cold snacks, we need to get budget, arrange with the caterers, and then inform the venue.  I don't know if I can do that.
....We might want to look into backups, but I'm pretty confident that this will work.

Lola: For Hong Kong, the organization we partnered with handled ticketing.  They used meetup.com, who are doing an account purge.  That might be easiest if we need to run ticketing.

Jeffrey: If we want someone to fund catering, they might need to be able to say that they are co-hosting.  Is that possible?

Matthew: I will ask about that.  That is reasonable, but I can find out.  I will try to find the budget myself and I have no idea how or what it might cost.  But I have some pointers now.

Lola: You should ask **name redacted**.  He might be able to help.  When he was on your team, he helped.

Poll for dates.  No preferences expressed. Will try to commit to the 4th.

Marcos: I might have to attend this meeting remotely.  Can't justify that much travel for that little meeting.

Discussion about the State of the Browser conference on the Saturday beforehand. https://2026.stateofthebrowser.com/ 

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Jeffrey: Status?

Matthew: Still working on one thing, to contact pointer events people (chairs) to ask if they have come against this issue.  That is, the absence of a long press event.  They might know more.  That was one of the sticking points.  Will do that regardless of the disposition of our review.

### Age restrictions/signals follow-up

Jeffrey: Nick Doty reached out about this.  Would like to schedule time at the next plenary to discuss this. Rick Byers might be able to call in.

Marcos: Related/unrelated.  The EFF is having a panel this week to be published online.  Excited to hear what they have to say on the topic. https://www.eff.org/event/effecting-change-human-cost-online-age-verification
Thursday, January 15th 12:00 PM - 1:00 PM Pacific

Jeffrey: It might also be useful if you can find someone at Apple to join as well.

Marcos: I would need to understand the different concerns are.  None of the solutions feel adequate at the moment.

Jeffrey: Will add Rick (or a substitute), Nick, Tara, and Ben VanderSloot to the next plenary.

### Breakout Rollup

## Eurasia Breakout (Europe / Asia / Australia) - [2026-01-15](https://www.timeanddate.com/worldclock/converter.html?iso=20260115T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Christian, Xiaocheng, Matthew, Ehsan, Yves, Martin, Marcos

Regrets: That I never had a chance to...

Scribe: Christian

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: It looks like we’re waiting for input from them. We’ve been talking in APA and the Cognitive Accessibility …, they have additional considerations. We could put them on this thread or in the repo. Can point them out once it’s fully reviewed.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) (Refine CG proposal) - @

Martin: There is a new repository (https://github.com/w3ctag/abcde). If folks have comments, please take a look.  Matthew and I aren't completely done.

Matthew: I work on a PR. Fantastic start, the name is brilliant.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel

Christian: No update.

Matthew: No update.

Martin: It might be interesting asking Tess to comment on this one. There was a similar proposal in the past. Tess had a strong opition that this would not be great for the web, given browser vendors want to make navigations quick, and this might add artificial delays, knowing that animations could potentially cover this. Issue was that the site doesn’t get the choice. It’s a different of covering the gap.

Christian to message Tess.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Xiaocheng: Want to have Matthew drive this review, as I was involved in the spec process, and I’m obviously very positive. I proposed a lot of ideas. My question is, there was a concern raised by Mozilla, but I think it is wrong, and I’m trying to confirm this.

Lola: Matthew, are you okay driving this? Do you need another reviewer?

Matthew: APA is looking at this at the same time, we are working on suggestions for the A11y considerations section, and should be done on that fairly soon. Not sure if we commented on this before. Will keep you all updated. Core thing that it does is really good for accessibility. Seems like a nice feature. There were a couple of concerns about the accessibility considerations section. We are working on some suggestions, more on this soon.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: Proposed by Open UI. We had some questions, they got back to me. We are in agreement. We didn’t discuss what to do with it, but I would suggest to close it as "satisfied."

Martin: What’s the implementation status?

Matthew: There isn’t an indication from the other two.

Martin: Whis is unfortunate, as it could be good.

Matthew: Should we reach out to Mozilla/WebKit?

Lola: Not really our business.

Matthew: Concern is, I can’t see anything in here that would be hard to implement.

Lola: Think we don’t have to have a resolution right now, we can go back to them and ask them regarding the implementation status in browsers, and let them come back to us. 

Matthew: Could put a comment, had you have any concerns raised by implementers?

Lola: Or, if they know about implementation commitment.

Matthew: What we don’t have, but we could ask if things are hard to implement.

Christian: "The other two" was Gecko/WebKit?

Matthew: Confirmed.

(Group consensus: Not closing as satisfied yet.)

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: This one is very interesting, close to my heart, want to see it happen. Think it could be a lot simpler. User should have a bit more say in it. Made the suggestions, quite a bit of activity on the thread which I haven’t caught up with. Will prepare comments in the private thread for next week.

### RDF

#### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

#### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven

#### [design-reviews#1174: WG Revision: SHACL 1.2 SPARQL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1174) ([Github](https://github.com/w3ctag/design-reviews/issues/1174)) - @csarven

#### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Xiaocheng: Review was posted early, but overlooked it. Definition of when a pixel is painted on a screen is out of scope for web specifications. Seems that we’re introducing something not very useful. The timestamp doesn’t mean much to end users.

Martin: Wonder whether browsers would game the benchmark.

Yves: Wonder if new timings in the rendering pipeline could be used to perform side-channel attacks, e.g. exfiltrate canvas data to someone else.

Lola: Do you want to resolve this as "unsatisfied"?

Xiaocheng: Want to ask for alternatives first.

Lola: Alternatives to?

Xiaocheng: Something that makes more sense to end users. I’ll figure out the wording later.

Lola: Consider this is an early TAG review, so they may not have alternatives yet, and may come back with something different later.

### [design-reviews#1176: Incubation: @supports at-rule](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1176) ([Github](https://github.com/w3ctag/design-reviews/issues/1176)) - @christianliebel, @lolaodelola

Christian: No update.

Lola: No update.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: At the end of last year, I had some concerns, and I thought we agreed that I would raise them, but I don’t see them here. Some of it was, "if they do it this way, authors will have a hard time implementing this for all the different vendors", leading to potential mistakes. If you are happy with those concerns, I could post them.

Lola: The blink-dev discussion is internal to Google, right?

Matthew: I think, largely.

Xiaocheng: Microsoft is also involved.

Matthew: I can check the previous discussions, and if they are good to post. Just wanted to make sure that there haven’t been any updates since. Main concern is to not put the burden on authors on all of the possible permutations (perfers-*). If the author is being responsible for highlight colors, and the site changes independently, so how do you get it right? What even is "right"? User agent may be in the best position to decide. It looks like they want to rely on the author, and I see a lot of problems there.

Martin: (Question on defaults)

Matthew: Will check in what the latest is on that thread. Having reasonable defaults would be good. Defaults could be that the user agent chooses based on the page. Will check up whether this is still valid. In the meantime, I could post the "workload on authors" part.

Xiaocheng: Doesn’t selection highlights have the same issue? What is our opinion on that?

Matthew: Yes, but it’s already there. Don’t have a huge experience of sites that use a custom selection.

Martin (via chat): Crbug landed mid-november, you may want to check out https://issues.chromium.org/issues/462131663.

Lola: I think I’m leaning more towards what the proponents are proposing. Don’t think this leads to huge overload for authors. This is not integral for web development, but could help improve highlight functions in a website. An author may choose to do that in a different way. Think there is an opportunity for the authors to have some kind of advice in the spec how to do this well. A lot of MDN guides that impact accessibility in some way have guidance on color selection, etc. You would want to highlight potential accessibility concerns in the technical documentation to make developers aware. I’m not agreeing that this would be a big deal.

Matthew: I see it as a feature of the user agent, I think is what Safari also means. They take care of it, dim the page, and highlight the match, also ensuring the accessibility of it. I don’t think you can recreate this with this proposal. So, is this a user agent feature or a website feature? Shouldn’t we think about the consistency of the web? It may effect the user’s experience.

Lola: Very helpful. It may make sense to go back and ask them, also considering Martin’s comment on defaults.

Matthew: I could really just focus on that, user agent vs. platform feature in the comment. Can we support both things? UA-provided defaults, able to be overwritten by the author? Or have the author choose something and override that by the UA if it doesn’t fit?

### [design-reviews#762: MiniApp Packaging](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/762) ([Github](https://github.com/w3ctag/design-reviews/issues/762)) - @ylafon, @maxpassion, @xiaochengh (pending for >6mo)

Xiaocheng: Close as time out.

Xiaocheng to close as time out.

### Issue Triage

Lola: Two things that are unassigned and untriaged. 

#### [design-reviews#1183: 
Incubation: new speculation rules action: prerender_until_script 
](https://github.com/w3ctag/design-reviews/issues/1183)

Lola: Anyone interested?

Xiaocheng: Can have a look.

#### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://github.com/w3ctag/design-reviews/issues/1184)

Ehsan: Let me have a read, and then decide.

### Other business

Lola: Regarding the F2F, please fill in your legal name and dietary restrictions in Jeffrey’s sheet. Looks like the developer meetup will take place on March 4. Jeffrey has also posted a PDF, so you can have a look at the options.
