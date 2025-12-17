# TAG Minutes - week of 8 Dec 2025

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/12-08-agenda.md).


## Breakout B (America / Europe) - [2025-12-08](https://www.timeanddate.com/worldclock/converter.html?iso=20251208T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Christian, Matthew, Lola, Yves, Hadley
    
Regrets: Serena
    
Scribe: Jeffrey

### [design-reviews#1138: [wg/webextensions] Web Extensions Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1138) ([Github](https://github.com/w3ctag/design-reviews/issues/1138)) - @csarven, @matatk, @toreini, @christianliebel

Matthew: Sarven posted a link.

Christian: We can close it as satisfied. I'll take care of it.

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18)

### [user-agents#33: Define "user agent" as distinct from "web user agent"](https://github.com/w3ctag/user-agents/issues/33) - @jyasskin

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github]
(https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger

Matthew: Some concerns. Comment in brainstorming. It doesn't seem too bad, but it's part of the Carousels thing, and it'll be used in conjuction with that. 
1. Whether pages will get into the pattern of only loading things dynamically in response to scrolling. Will some content be invisible to AT?
2. Scrolling and animations in general can be hugely distracting. prefers-reduced-motion? But what guidance can we give authors to ensure authors use that effectively? "Scrolly-telling" ("storytelling") where scrolling is integral to the story. If you disable scroll-based animations in response to prefers-reduced-motion, that disables the story. Spec should address this.

Lola: Not having read the spec, I'm not positive about this kind of interaction. Don't think it's good for the web. "scrolly-telling" isn't good for the web. It's exclusionary and not enough people who benefit from prefers-reduced-motion actually turn it on. I get motion-sickness, but I don't use prefers-reduced-motion because motion-sickness isn't a disability, but I do get triggered by web animations. Other web users might not immediately think "there's something I can change in my computer to make my web experience better." Hesitant to introduce more things that impact users' day-to-day experience that aren't integral to the web. We don't need scroll-triggered animations: it's aesthetic rather than functional.

Jeffrey: Question of loading things by scrolling is not enabled by this. I think it doesn’t give you more tools to react programmatically to animations. Don’t like this kind of animation though. It exists on the web, they are trying to simplify a common pattern. But when these things are on the web, you trigger them multiple times, can make the page hard to deal with. Haven’t seen anything in the spec to remove that tendency. Would like them to address common failure modes, and do something in the spec to reduce them.

Matthew: I quite like scrolly-telling, which is odd: I'm remarkably visual for someone with a visual impairment. But it's often inaccessible because it doesn't react to my font size. A bit like carousel, but I'd rather make it not suck. I think this is salvagable. If we can widen it to talking about common failure modes, that'd make it much more robust. And more likely to play nicely with other features like large font size. I'm concerned, but there's a possibility to do it more robustly. From Lola's comment, I think there's a gap about reducing motion. I agree that there's a problem that people don't get help for minor-to-moderate impairments because the UX of the system isn't conducive. Accessibility is about big things that don't change, but there are lots of things in the system that would be useful. Maybe you only want reduced-motion sometimes. Raising awareness of the features. How should the system do that? Some is outside of our scope, but maybe we can work on it a bit.

Yves: If we tell the proposer to do it differently, that's more actionable than if we just say we don't like it.

Christian: I like this kind of feature. Sometimes newspaper articles are very visual, and are fun to read through and scroll through. Not harmful.

Jeffrey: This is not the scrolly-telling animations that you might now, they are not linked to the scroll timeline, but triggered by scrolling the element in or out. On prefers-reduced-motion: Do you know Microsoft’s picture of temporary disabilities? (https://inclusive.microsoft.design/tools-and-activities/Inclusive101Guidebook.pdf#page=22, https://www.learntoenable.co.uk/everydaybarriers) I wonder if the APA could state a position on how people should be able to find a11y angles. It could be much more visible in browser UIs.

Lola: I've added myself. Would lean toward satisfied-with-concerns now, but can have more discussion.

Matthew: We should discuss with the proponents. The in-site tools to adjust font size are great for local accessibility within a site, but imply that users can't do it to other sites, which of course they can with browser tools. Want to post something this week, so I'll finish drafting by Breakout C.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49)

Hadley: Close the issue?

Jeffrey: Martin was going to propose a CG to do reviews, kinda like the IETF directorate process.

Yves: Might include other HR in a reviews CG.

Hadley: Don't we lose the ability to choose who they are?

Lola: Might not be a bad thing, since more people can more easily get involved.

Hadley: Concerned about letting anyone who volunteers speak on behalf of the TAG.

Lola: Think we could change some of the processes. Maybe associates can review but not post publicly.

Matthew: I think this was in the minutes from the plenary, but my understanding was Martin proposed we carry on with Associates, but start a CG in parallel. Most associates were pleased to have the program. Point about what you do with self-selecting membership: Martin suggested that you don't assign reviews to problematic people. We'd still assign reviews. I volunteered to help with documentation to set this up and explain to people what they need to do. Makes sense to change the focus and assign me and Martin.

Lola: I didn't think martin was saying we'd do both.

Jeffrey: Think Martin wanted the CG program to replace the TAG Associates, but I think we were happy with both. We can still review it next year and decide to close one of the two programs.
    
Hadley: Appreciate the thoughts about how to mitigate my concerns about a malicious person joining. The chairs and previous chairs have worked hard to create an environment where we know and trust each other. Can say things not in the minutes. Don't know how to preserve that if we open the calls to the general public. Would be a shame if the TAG were totally public. Don't know the answer, and not sure the CG can't work, but wanted to raise the concern.

Lola: That's a valid concern. Maybe CG might not be the best avenue since it's public. Think the nature of the work would attract existing W3C members, since the TAG is intimidating. Especially if we don't publish agendas in advance. Probably won't be ambushed by the public, but might be ambushed by spec authors. We've had some contentious issues, and it might have been better to handle them over VC. Could let people be rude, but we have a code of conduct.

Matthew: The suggestion isn't to have these people join TAG calls. Idea is that the CG is called something about getting reviews from subject-matter experts, which could feed into TAG reviews but not constitute TAG reviews. Other SDOs have this, and don't even have calls, just an email list.

Jeffrey: Suggest we let Matthew & Martin write up the proposal and discuss that.

Hadley: If we're not talking about having people in TAG calls, doesn't disrupt personal dynamics. Potential problem for workload, since someone has to manage this group. We all have to read this group's output.

Yves: For the workload reason, I thought it would be useful to include other HRs. Might be a good discussion to include the other ones.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

skipped

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

skipped

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

skipped

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin

Jeffrey: Martin and I have been going back and forth on this, we are close on finishing it. If anyone wants to review it, please do so now.

### [prevent-credential-abuse#58: Add region locks to Identity Abuse section](https://github.com/w3ctag/prevent-credential-abuse/pull/58) - @christianliebel

Christian: One additional risk that came to mind. If you have a credential, it gives away a piece of geographical information, which could implement region locks. It's not in the document aside from a more global point. We say you shouldn't be exclusionary based on characteristics.

Jeffrey: Reminds me of a paper I saw last week, doing credentials without revealing the issuer. We could point to that paper to make creators of such a credential aware that this mechanism exists. Will look up the paper and post it in Slack.

Matthew: I’m interested as well.

### [societal-impact-questionnaire#26: Exclusion Example](https://github.com/w3ctag/societal-impact-questionnaire/pull/26) - @lolaodelola, @csarven, @jyasskin

Lola: Think this is approved, but there's one more thing for me to do. Once I've removed the "Example:" text, this'll be good to go.

###  [societal-impact-questionnaire#31: Turn on PR Preview](https://github.com/w3ctag/societal-impact-questionnaire/pull/31) - @jyasskin, @csarven, @lolaodelola

Jeffrey: we don't need to discuss this, just merge it.

Lola: done.

<!-- Design Reviews -->

###  [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @lolaodelola

Yves: bump to next week.

Hadley: They updated the explainer 4 days ago, so we're not far behind.

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: Thought this seemed pretty good. Haven't checked with the wider APA. This is one of the few things that's made me feel disabled on the web, that it doesn't reflect my chosen font size. If designers are faced with a situation where font sizes will change, designs will get more flexible and fluid.

Matthew: Good for them to scale font size keywords too, and they're planning that. They talked about having 2 modes: First do scaling linearly, so 2x font size can make some headings very huge. Second they might have a mode with non-linear scaling, with some way to specify that. Don't remember if they thought it should be under the author's control. But really it should be under the UA's control, since the user knows what works best. Don't know why it would need a separate keyword, since the UA can override it. The argument against the UA overriding this is that layouts aren't flexible enough, so they'll break. But this opt-in should be enough sign that the layout can cope with new sizes, including non-linear ones. So prefer 1 keyword. Might be ok for the author to also give some input, but UA should keep control. Kinda like when UAs all decided to ignore the maximum-scale keyword that disabled pinch-to-zoom. Let the UA control it. Think that's all compatible with their proposal. Would be ok if they still wanted 2 modes, but would encourage UAs to take a more active role.

Hadley: Big +1 to that, now that I'm more reliant on reading glasses.

Lola: Would this impact performance? Would someone with a custom font see a performance problem if user starts scaling?

Matthew: Don't think so. This says that sites can opt into the user's chosen base font size. On iOS or Android, you can say you want super-big fonts, and it does nothing on the web, which is wrong. Scaling will only happen once. Has a knock-on effect by adjusting the layout, which CSS can react to. No different from zooming in on desktop. Probably no performance impact. I also asked Serena for input. If nobody else has input, I should draft a comment for them.

Lola: Sounds good.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: Will look at their latest comment.

### [design-reviews#1174: WG Revision: SHACL 1.2 SPARQL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1174) ([Github](https://github.com/w3ctag/design-reviews/issues/1174)) - @csarven

Skipped

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven



### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven



### [design-reviews#1160: WG New Spec: RDF 1.2 Semantics](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1160) ([Github](https://github.com/w3ctag/design-reviews/issues/1160)) - @csarven

Skipped

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Skipped

###  [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Skipped

###  [design-reviews#1171: [wg/dx] Dataset Exchange Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1171) ([Github](https://github.com/w3ctag/design-reviews/issues/1171)) - @csarven

Skipped

###  [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: Will get to this by Breakout C.

### [design-reviews#1158: ViewTransitions: waitUntil() method](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1158) ([Github](https://github.com/w3ctag/design-reviews/issues/1158)) - @christianliebel, @lolaodelola

Lola: Breakout C. Generally looked good, but had one concern.

###  [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Skipped. Needs Ehsan.

###  [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Last discussion, we had some thoughts about how to move it forward. I was going to ask other groups like Pointer Events how they handle this gap. 

###  [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Matthew: We were going to close this as unsatisfied. Jeffrey linked to how HTML-in-Canvas will address the problems. Will draft.


## Breakout A (Asia / Australia / West America) - [2025-12-09](https://www.timeanddate.com/worldclock/converter.html?iso=20251209T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Marcos, Jeffrey

Regrets:
    
Scribe:

###  [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

Martin: I don't think we can do anything here.  Still waiting on Marcos to respond to Jeffrey.

Marcos: ECMAScript doesn't define garbage collection, but maybe we can assume people know what it means.

Martin: Feel like "destroyed" is better.

Marcos: It's not supposed to be visible, but it is in this case. In Gecko, many fields become null that are formally non-nullable. If you're holding a reference to the old target, it's a weird case. They're edge cases, but they come up. In WebKit, we observe the destruction of the context, and that's why I'm writing this, because I hit it for Digital Credentials.

Marcos: Overlap with bfcache: I'd like to keep them completely separate. bfcache should be less observable than this one. It has its own set of rules. This one the objects get destroyed; bfcache the objects don't get destroyed.

Jeffrey: if we want these separate, we've made a mistake in the spec language we use.  "Not fully active" is used for both, so if we need separate treatment, we need separate language.

Marcos: bfcache is not fully active, but script can't get to it.  Related, but not destroyed.  In geolocation you might stop sending events.  If you monitor geolocation, that doesn't send updates.  Some weirdness to cleanup maybe.

Martin: Is it the case that the references that become null for gc'ed objects, go to null for bfcache?

Marcos: You'd never see that because the whole JS environment is frozen, and you can't check. There are similar cases that have been sent to the TAG: 
There was a thing with videos that pause when they go off screen.  They were adding them back in an iframe, which restarted everything and bloated resource consumption.

Jeffrey: If you hold cross-window references, can the window navigate and end up in the bfcache?

Marcos: Maybe.  Might be fun to test.  You might need to debug the browser.  Potential case.

Jeffrey: Do iframe navigations end up in bfcache?

Marcos: Might be wrong, but I don't think they do.  Only top-level navigations end up in bfcache.

Jeffrey: If we need different treatment, we need different terminology.  We shouldn't have two sections that talk about non-fully active documents where there are different treatment for each.

Marcos: Will have to re-read bfcache text. It has been too long.  The thing is that the concept that HTML defines for this.  That's the check.

Jeffrey: If that works, then that is good.  One set of treatment for all the situations is easier on spec authors.  But not if that doesn't work out.

Marcos:  bfcache is different from where the context is destroyed.

Jeffrey: bfcache authors were very much focused on bfcache, so maybe didn't consider the other cases where things are destroyed

Marcos: Still think they're different, since that section goes into supporting bfcache, which is extensive. bfcache situation asks if it invalidates the cases. What's the effect of the feature on the cache. Whereas here it's "surprise your browsing context is gone.

Marcos: Mine could go above the bfcache section, and be followed by the more specialized bfcache section.

Action: Marcos to brush up on bfcache and respond on the PR with suggested outcomes.



###  [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Jeffrey: Also seem to be waiting on Marcos.  Mostly just minor suggestions.

/marcos takes a few of the suggestions.

Marcos: The lock icon thing is maybe good.

Jeffrey: Agree. 

### [prevent-credential-abuse#56: This is about government issued credentials](https://github.com/w3ctag/prevent-credential-abuse/pull/56) - @martinthomson

We agreed to close this.

### [design-reviews#1169: Incubation: Email Verification Protocol](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1169) ([Github](https://github.com/w3ctag/design-reviews/issues/1169)) - @martinthomson, @hadleybeeman, @christianliebel

Jeffrey: Concerned about saying "you need to do this in the IETF", but fully on board with "you need to talk to the IETF".

Martin: Agreed. Think the IETF is the "right" place for this sort of security protocol. The API should happen in the W3C, but it should refer to a protocol developed somewhere that has email people, and there aren't enough email people at the W3C.

Jeffrey: Will let Martin and Christian figure out the exact comment.

### [design-reviews#1092: Web Authentication Immediate Mediation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1092) ([Github](https://github.com/w3ctag/design-reviews/issues/1092)) - @martinthomson, @jyasskin, @marcoscaceres, @toreini

Jeffrey: I think this comment is ready to post.
    
Martin: Tim's requirement is probably achievable. 

Jeffrey: I asked questions about who is running origin trials and how they are approaching UX.  Lots of enthusiasm for the feature though few using it in the trial.  Some (Amazon, Paypal) show full-page login screens anyway.  Conditional UX might serve their needs just as well if that is their choice.

## Breakout C (Europe / Asia / Australia) - [2025-12-11](https://www.timeanddate.com/worldclock/converter.html?iso=20251211T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Lola, Matthew, Sarven, Yves

Regrets: 

Scribe: Sarven

### [design-reviews#1169: Incubation: Email Verification Protocol](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1169) ([Github](https://github.com/w3ctag/design-reviews/issues/1169)) - @martinthomson, @hadleybeeman, @christianliebel

Yves and matthew: Martin reviewed a few hours ago.

Hadley: Will encourage him to post this but apparently he did publicise it. Let's wait and see what they say.

(late comment) Martin: I got positive feedback from the other breakout, so went ahead, making it clear that these were my words, but reviewed by the TAG.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github]
(https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger

Matthew: I've put something in. We talked about it on Monday. Lola put some comments in. I drafted a comment. Do we think the draft comment is going in the right direction? Jeffrey +1'd.

Lola: I think this comment is fine. Question: So they would put that in the accessibility consideration?

Matthew: Sometimes they do. CSS has a lot of specs. Generally there'd be an accessibility consideration but if a spec like CSS is broken up, some of them don't need an exact section because the parent might. I don't know about this one in specifically. We don't want to encourage bad practice.

Lola: Am not against them putting it under accessibility considerations, but have seen other CSS specs in terms of access, not disability, and they highlighted as part of the spec, e.g., font-something, and they put the advise/note there in the spec. For something like this, I'd prefer it along those lines. I'd caution against a section where they'd do that for devs.

Matthew: Agree, makes sense to tell people where the issue is. This is part of a bigger thing.

Lola: ??? Timeline. That spec doesn't say it.

Matthew: ... Put the guidance for devs, and so consult this section - if it is big. They have their own conventions for this. Two sides to this. For implementers, there isn't much for them. But this may be an occassion where devs can refer to. Pointer to WCAG's. We could put another point here about focus.

Lola: I think we should ask re focus.

Matthew: Add and share?

Lola: Sounds good.

###  [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: They added some more info. One of the concerns was re dark/light: there is a lot of colour combinations needs to be specified as author. Ditto with media queries, and system may override, but not sure if that reduces dev burden. 

They said they'd update the explainer and so we should nudge on that. 

One of the suggestions was, "why not let the UA handle this?" and we have at least one UA doing this (Safari), but maybe it was specified like highlighting something on the table and there is search text in the tr, and it would highlight it. So giving more flexibility as a designer. The answer they gave wasn't accurate. They cited some privacy things - ??? and grammar check. We may be talking past each other.  ??? if the UA itself could just decide to override whatever the page specifies. If the UA is making a decision "should I override?" I don't know what the performance implications would be compared to UA just deciding to do it.

Hadley: Did you ask that?

Matthew: No. We suggested the UA should make the choice. They came back with even if we ship this it could still be overridden. But most people (devs?) wouldn't know how. If the UA decides to act on behalf of the user because the contrast is too low. I didn't ask that but would like to look at that in the future. One other area is whether the UA will handle it - we should be aware of the Blink thread and that seems like people are implementing it. Tests need to be written for spelling and grammar. There is a CR bug to improve highlight colour. Even in that bug it says that maybe the UA should default to its own. I don't think they have thought out how this fails for the users. We already mentioned a matrix of preferred colours, and also taken into account by author - something like six variants. Also like background/foreground colours, and sometimes sections alternate in colours - to pop up - and that all has to worked out, and if you decide to do that there is a choice, and so I'm going to flip the fore/background colours, and then the search results would be inconsistent and hard to read. And if you don't do that then it'd be more consistent but not necessarily easy to identify. Perhaps I should post something in the Blink thread.

Hadley: Next steps?

Matthew: I need to ask a clarification on a number of things. Making sure we are talking about the same purpose. yes, there are privacy issues. Also need ot ask how feasible it is for UA to do this (not just Safari). And if they agree with my concern on problem expanding, and maybe do a mockup of what I'm talking about, which would be useful but take a lot of time.

Hadley: Encourage you to do that. Anyone want to join this issue?

Sarven: +1. I think Matthew has substantial info that we should put out there anyway.

Matthew: Mention that I'm working on an example and also check if they have one going.

### [design-reviews#1158: ViewTransitions: waitUntil() method](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1158) ([Github](https://github.com/w3ctag/design-reviews/issues/1158)) - @christianliebel, @lolaodelola

Lola: Christian posted a comment and has closed.

### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven

Sarven: Drafted a review at https://github.com/w3ctag/design-reviews-private-brainstorming/issues/215#issuecomment-3640921722 
They want a review on a working draft. they are referring to their primer as their explainer. I think they weren't clear on the idfferences betwen RDF 1.1 and 1.2 concepts in abstract data model, but that's mostly editorial work. I suggested they bring some of the explainer material, especially changes, from the specific specs up to the higer concepts spec in the primer.

The only technical concern I had: as it stands, the mediaType that concrete RDF syntaxes has registered at IANA do not mention the optional parameter stuff that could be used, like the version. this group is trying to do: version 1.2, that needs to be parsed differently by consumers than RDF 1.1, so the version is a way of giving heads up to the consumer of how it should be processed. Because the original mediaType doesn't indicate the version, any existing 1.1 client/consumer would not observe what that version parameter would be. if there is a version information included as part of the document or payload, inline, then 1.1 parsers would fail, because that isn't valid 1.1.

The group is doing fine. They've done 1, with the n-triples format, so they're sending a submission to iana to update the mediaTypes to introduce an optional version parameter. I think they need to do that consistently for all specs, and they need to be more clear about how things should fail, error handling. As it stands, it's not clear how the error handling might be, so I'm suggesting that they work on that. It's a working draft, so it's not so bad right now, but one really needs to read the thing and juggle all the specs in parallel (RDF concepts abstract model, and then concrete syntaxes: JSON-LD, Turtle, etc. So the Concepts realise how the RDF is encoded.)

I'm suggesting this should be marked as satisfied. This particular document seems to be on the right track. 

I'll look at the other ones in depth (RDF 1.2 semantics and RDF 1.2 n-triples), and will review those. But it's fine. 

Hadley: for the future, if you find yourself doing research into other specs, it's fine to ask the submitters to put more into their explainer.

Sarven: ok

Marcos: Have they really verified the versioning thing with mime types? Unless they have done it very carefully? If x doesn't do it right, they may get themselves into a bad situation.

Martin: With mime types there should be negotiation

Sarven: they did highlight the negotiation in the spec. They did say how clients should approach unrecognised versioning. I agree with you, Marcos, that type of error handling or reccommendation for devs should jump out more. It's a working draft, so fine for where it is, but it needs more iterations.

Marcos: we shouldn't solve it for them, but it sounds a bit concerning, that they're getting into that situation.

Sarven: i'm not personally crazy about the direction this has taken with the versioning, but I'm not sure there is a lesser evil. They're introducting a new feature, the alternative was introducing a new media type. From the RFCs, the version is discussed there and it should only be used to clarify and add info to the current media type, not to signal new feature. Theyll ground that by updating the media type to bring the notion of an optional parameter like version type, which I think is acceptable. the alternative is worse. 

Martin: In general if you change the media type in any way, that basically signals it is incompatible with the other thing, and lot of content negotiation would ignore versioning. So might as well define a new media type. Which is also true for version in-line. Media type determines the model so don't put version in media type and in content because there is already good 

Marcos: that's what i heard too.

Martin: "the registration for the media types do not define the version parameter."

Sarven: the concrete ones are making an update to the registration. But I agree with you. Even the version: the parameter is only intended to clarify. If the turtle is saying 1.1, tha'ts fine, but you don't want to say 2.7 to hijack it as a new version. Updating the registration is the only safe and less breakage.

yves: I. agree with martin that if they are incompatible, it shoudl be a different media type to avoid issues. Is the format describing, and is there a way to do graceful degradation: is it compatible with previous version just missing one point, or do they need to update the processing of it becasue the changes are differet? If they ahve te capabiliteis of that, it's fine. If not, it's missing.

Sarven: they do, RDF 1.1 is still valid 1.2. 

Martin: is RDF 1.2 valid 1.1?

Sarven: No. That's why you say the version. Fail the 1.1s early. For example, if a client were to include Accept, if they didn't include Accept, the server has the option to return with the version if they want to. If a client asks with a version, and the server accepts it, the conneg will figure it out.

Martin: So if I undestrand this correctly: 1.2 adds featurees that a 1.1 parser won't handle?

Sarven: yes

Martin: did 1.1 add a version on the media type?

Sarven: no

Martin: that's bad. the spec is bad on how you handle uknown parameters. It may treat the whole thing as an opaque stream, treating it as a different media type. The other way to interpret it: unknown parameters are ignored.

Sarven: does not change the core interpretation of the model. Providing additional info to signal, similart to the profile parameter. Will say what that payload is going to include.

martin: so you have a major interop problem. the 1.1 parser will throw away the version attribute, say "I know how to process this!" and fail in interesting ways, because it has 1.2 features. The only sensible thing to do is to get a new media type.

Sarven: they are being a bit, as I understand it, done some survey to understand the adoption of this and how ready the parsers will be able to migrate over. There is more nuance to this.

Martin: I understand. And they may think they can survey the full set of implementations. My experience with the web is that that is impossible. I think the only adivsable thing to do is to define a new media type.

Marcos: I agree. 

Martin: the 1.2 parsers can understand both media types, 1.1 and 1.2.

Marcos: "you broke the thing, ti's fine, declare a new media type and be more careful in the future." We need to make that recommednation as the TAG, and they can go from there.

Hadley: do we have consensus on that?

Sarven: I'm 75% ok with what they say. They do have a note saying "clients should be prepared... consider downgrading the content."

Martin: is that text that only appears in 1.2?

Sarven: yes

Martin: but the 1.1 impelementations will be looking at the 1.1 spec.

Sarven: nobody uses old versions of HTML

Martin: modern borswers use the docType to agree that the content is HTML5, which is annoying and not a pattern I would recommend, which is why we have conneg and media types.

Sarven: How is CSS doing... it's using hte same media type. What does a 2.1 parser do when it encounters a CSS 4 payload?

Martin: I'm not sure, because thins like app support have added ne wthings. but they've relied on that the olde parsers do brace matching, which is sufficient to make sure the new content will cause the old content to choke. It's effectively a forward-compatible format. I'm hearing from you that RDF is not. Which is understandable. In that context, with a compatibility break, the sensible thing is to define a new media type.

Marcos: there is no versioning in CSS. there are levels

Martin: And the levels are not about the grammar. That grammar works in a CSS parser from 10 years ago. The features may not work, but it will parse. The rules that parser does understand will apply, so it degrades gracefully. Building a language that has that capability is a pain, and the CSS people that was important enough to do all that work. It's being authored by humans.

If RDF doesn't want to put the work in, which is a valid choice, it's a compatibility break between versions, and therefore they have different formats. That's ok.

Sarven: I don't disagree. Updating the media type is a valid path. So if updating means there are incompatbilites between the latest update with the prior version, then the web platform is itself permitting that.

Martin: but by retroactively putting requirements on implementaitons on the old spec, you're banking on the idea the at the implementations will be all updated in a reasonable timeframe. Every time we've tried to do that on the web, it's failed. Which is why we have those hacks in HTML.

Marcos: 15 years

Martin: after that point, we were much more cautious about how we were managing the format. Still ongoing, but the work is worthwhile.

Marcos: like all tags in HTML must have a closing tag. That is the compromise we made.

hadley: what are we going to do with this?

Sarven: If Martin and Marcos want to add/update the review i've made, that is a way we can move forward. Personally I'm ok with what they want to do

hadley: if we don't have consensus, we can share that, and explain. or keep discussing until we do.

Martin: our responsbility is to point out the risks. And suggest. 

Sarven: I'll think about how to handle this. Martin/Marcos, if you could write something, that might help

Hadley: You also have the minutes from this discussion to pull from. 
