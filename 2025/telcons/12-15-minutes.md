# W3C TAG meetings, week commencing 15 December 2025

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/12-15-agenda.md).

## Breakout B (America / Europe) - [2025-12-15](https://www.timeanddate.com/worldclock/converter.html?iso=20251215T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Matthew, Lola, Jeffrey, Christian, Ehsan, Hadley, Yves
    
Apologies: Sarven
    
Scribe: Christian

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew to post the comment.

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

Skipped.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Skipped.

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: Proposed a comment, what to people think?

(Reading the comment…)

Lola: Looks good, one suggestion: In your "from experience" part, where you give suggestions, could you give a suggestion that they get in touch with Docs CG? They could help with guidance for developers.

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman

Yves: Started to take a look at it, but I’m not done yet. Find it strange that you have to be at the new location, and go back to the previous one. Redirect would also seem feasible. Need to figure out the choreography first. Think it’s dangerous if this is cross-origin.

Hadley: I’m very concerned about going cross-origin.

Christian: It’s related to my work. Didn’t have a look yet, but I’m happy to do so.

Jeffrey: This supports going from maps.google.com to google.com/maps, that’s why the two-way handshake is needed.

Hadley: There was a pattern we had in the past where there was an imbalance of power, think large ad networks, where one party says "do this [like post this dodgy javascript in order to get paid". And the site will do it. Two-way handshake doesn’t mitigate that.

Jeffrey: We might want to say, you can do this to become more fine-grained, but not the other way.

Yves: We could avoid transferring permissions.

Jeffrey: This doesn’t happen.

Yves: Same-site seems ok, but I think information in a redirect would be better.

Lola: Why do this instead of some kind of user-facing notification provided by the app? "Please download the new app."

Jeffrey: It would make sense to ask them that, but I think the answer is that high percentage of users don’t transfer. 

Have an answer for Yves regarding the redirect. If you redirect from one origin to another, then a UA doesn’t understand the transfer is going to give you a bad UI in the app. Looks like you’ve navigated to an external page on an installed app. So, they have to try to detect the install status before being able to redirect.

Christian: This is an issue, becasue if you install an app it's pinned to the origin you installed it from. So a redirect would give you the address bar, which is what you try to avoid when creating an app. So I think the proposal is valid, but I need to take a closer look.

Yves: It's weird. it would be better to say, "It's an installed app, and I know it's ???. I know that this app has been upgraded and I should go to this other place." It seems a better option than trying to trick what's installed. 

Christian: Need to think about this, let's keep talking offline.

Yves: That’s why I meant knowing the cheorography would help to determine if this is a good approach or not.

Matthew: I have a concern from a user’s perspective, when someone buys an app, there should be some form of opt-out rather than it’s just happening.

Hadley: Tend do agree, but if they got control of the backend, don’t they have the data anyway?

Matthew: Think there’s also a geographical vector, some jurisdictions require notification in that case anyway, don't they. 

Yves: In the case of an acquisition, it will likely not be same-site anymore.

Lola: Let's keep working on this one async then.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: Another one where the proponents came back with new information. Did put my thoughts on a comment. Most of there update seems good, still thinking about no. 1 where orientation needs to be taken into consideration. Need more time to think about it. It was a detailed answer, rest seems reasonable. Need to decide whether no. 1 is also fine, or need to ask them another question. Will either get back to them about no. 1, or post a comment on the private brainstorming thread, saying "satisfied" before Thursday.

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

Skipped.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Ehsan: Hopefully, Jeffrey and I are now on the same page on this. Wrote a draft for clarification. Seems like things have updated; it’s not clear what the current implementation is. We can coordinate that async. Jeffrey posted the structure of the questions, will double-check with Matthew and continue with Jeffrey. Will post to the private brainstorm first.

Lola: Sounds perfect, don’t wait for me, Jeffrey’s thumbs up is sufficient.

Ehsan: Try to make it by the Thursday meeting.

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Matthew: Still have a comment. Wondering if HTML-in-Canvas would solve the problem. Jeffrey and I think it would. Either I can go ahead with what we’ve got and check the two WHATWG threads Jeffrey linked to. Could also check with the ARIA chairs, if they think it would solve it. Is it worth doing that?

Lola: Think looping in the members/chairs of the ARIA WG would be good. They may be able to provide insights that we don’t have.

Matthew: I’ll do that, we want to cooperate more closely anyway. There’s no reason to wait until that’s up and running though. Do you think tidying up the comment and posting it would be worthwhile? Given this is the last week before the end of the year.

Lola: Is it a definite no? Nothing that ARIA could change?

Matthew: We are pretty confident.

Lola: Then we can say no, but leave the issue open until we have spoken with ARIA.

Matthew: OK.

### Issue Triage

Lola: We have reached the end of the list. Should we do some triage?

Jeffrey: I think we should.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) 

Lola: Is this a browser request instead of a WG request?

Jeffrey: Yes.

Hadley: Is this still CSS?

Jeffrey: Yes, it’s a refinement. Think it follows a pattern established in other designs.

Lola: I would like to be assigned to this.

Matthew: Can have a look at that as well.

Hadley: Is this a horizontal spec review? Given this is driven by a browser.

Jeffrey: Not really, but it was the most matching review type that was available.

Hadley: Small delta?

Jeffrey: Yes.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) 

Hadley: Is this also CSS?

Matthew: Yes. Happy to have a look at it.

Lola: Looks like the explainer is for two-phase transition, looks like they only ask us to take a look at one of the proposed solutions. The link directly goes to the section they would like us to review.

Hadley: Doesn’t sound like an explainer?

Lola: Think we shouldn’t review this, this very much a WIP.

Hadley: I'm adding the "explainer missing" tag.

Christian: I can do it.

Lola: Based on what I see, they’re asking us about our feedback regarding different solutions, until they find one. Explainer itself contains an overview and context. Don’t know if it is enough. There is some security and privacy, but no a11y considerations. Don’t know if it would need it.

Hadley: If we’re not sure what they want, we should try and clarify that.

Matthew: There isn’t much of an explaination of why the explainer is what it is. There’s also no alternatives considered section, and the markdown is badly formatted. Assigned myself before we discussed it. Thanks Christian for joining. We should request clarification. There are also some minutes from TPAC.

Lola: I think we should finish the explainer and then come back to us. Sounds 

Christian: If it’s okay for you, I would have a look and either ask for clarification or send them back?

Hadley: Don’t burn too much energy until their needs and intentions are clearer.

### Issues pending external feedback

Christian: What about the stale reviews that we still have? There are several design reviews labeled "pending external feedback", but nothing happened for over a year, for example MiniApps. What to do with these?

Yves: Let’s keep them open and revisit them.

Jeffrey: We can also ask Lu Sen about MiniApps.

### [design-reviews#1180: [wg/i18n-core] i18n WG rechartering 2025(https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1180) ([Github](https://github.com/w3ctag/design-reviews/issues/1180)) 

Hadley: Do we have any comments? Apart from, please continue your important work?

Jeffrey: They publish RECs.

(Hadley reads the RECs.)

Jeffrey: Doesn’t sound problematic in any way.

Hadley: Was this the review?

(Group agrees to close the review.)

### [design-reviews#1176: Incubation: @supports at-rule 2025(https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1176) ([Github](https://github.com/w3ctag/design-reviews/issues/1176)) 

Christian: Think this is about feature detecting at-rules themselves, kind of meta-feature detection.

Lola: I will have a look at this.

Christian: I will join.

### [design-reviews#1108: ServiceWorkerAutoPreload](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1108) ([Github](https://github.com/w3ctag/design-reviews/issues/1108)) 

Lola: This has been shipped already.

Christian: Close it as too late?

(Group agrees to close it as timed out.)

### Plenary chairing

Hadley: Will be travelling, someone fill in the chair for the plenary?

Jeffrey: I can do it.

### Chair picking

Jeffrey: Discussion last year tended toward appointing new chairs. However, it could be mean to ask new people to chair.

Hadley: May be mean, but not unprecedented.

## Breakout A (Asia / Australia / West America) - [2025-12-16](https://www.timeanddate.com/worldclock/converter.html?iso=20251216T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

*No meeting. Please work on these asynchronously*

### [user-agents#33: Define "user agent" as distinct from "web user agent"](https://github.com/w3ctag/user-agents/issues/33) - @jyasskin
### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin
### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

## Plenary Session - [2025-12-17](https://www.timeanddate.com/worldclock/converter.html?iso=20251217T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Lola, Matthew, Ehsan, Sarven, Jeffrey
    
Apologies:
    
Scribe: Sarven
    
### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49)

Jeffrey: Propose a CG to try out this idea. Introduced idea in the Member meeting - 6 hours ago. We need to write up the proposal.

Martin: If we are serious about it then the charter is the right step, and the charter answers some of those anticipated problems.



### [societal-impact-questionnaire#26: Exclusion Example](https://github.com/w3ctag/societal-impact-questionnaire/pull/26) - @lolaodelola, @csarven, @jyasskin

Lola: Will merge today.

### Age-restricted content workshop report - @martinthomson

Martin: There was a draft report. TAG was invited to observe. Attendees are redacted for now. In terms of details there are a lot in there. General statements and principles. Some things on architecture, such as what the roles and responsibilities are. Vocabularies. Issues discussed in the workshop. Not a lot of conclusions. Perhaps the biggest is maybe to continue talking about the topic. It turns out that being able to say that is meaningful to some members. Folks are talking to age verification verifiers/implementers (???) . I found some of the appendencies useful. Looking into high level requirements turned out to be a useful exercise for thinking about the problem. Little things like you need to accept whatever system you have ??? if this is the course you take ??? maybe we shouldn't be accepting imperfection for equity online. TO make sure everyone gets a shot at participating. Some of these systems are exclusionary. They are an inadequate consequences. For TAG, with a report like this, it is probably worth considering it is targeted to some people to look into. This is to guide future discussions, such as for privacy principles. For architectural, who is responsible and how roles are organised. That may have some value on articulating what arhictectural choices to make. Govs making architectural choices is an interesting one. A decisions a lot of govs have made and think quite reasonable and strong on their part.

Jeffrey: We have PP and section on Guardians, https://www.w3.org/TR/privacy-principles/#guardians  . A lot of age verifications ignore, and govs stepping into it, and without any considerations on the situation of individual needs. The California regulation perhaps come close, devices should express age target and websites can make decision.

Martin: For classification systems in the past, some govs have taken a part and advised the guardians to make the right choice, and when content becomes age-restricted, and so guardianship on that becomes important. Risks associated with systems is adverse. Not as blank and white.

Lola: While agree with guardian point, re document outside of "us" and W3C would be reading, ideally hopefully govs will be reading. I'm running a Q1 course for policy people and this and other things we are doing. If I bring this forward, they'd say we should be the guardians, and they'd make the argument that govs making the guardiance ??? If we are going ot make this guardian point, then we should be really explicit on what that term means and who we are expecting the guardians to be in this context.

Martin: we need to ack some of those subtleties in the doc. And as much as making it without a "political" ??? Guardianship point is useful, if you do this, then this. A lot of political discouse re children argument, appeals to notion, or rhetorical tricks, I think we can be more strict. So, gov takes a hand, for a lot of children.

Jeffrey: I wonder if we can make the appeal to child protective services. There are processes where govs overreaching. If we can make that analogy to make govs more cautious.

Sarven: Largely agree with Martin and Lola. In a course I was teaching, a paper addressed how this individual decided to leave social media, by tying some things in the web's architecture and principles in a way that didn't protect them from psychological harm. Addressed how the foundations of the web fell short in protecting mental health. Importance in how the web has evolved in a way that's not always good for younger people. Increasingly exposed to services, apps, algorithmic things. Line to the discussion here: whoever the guardians are shoudl look at it from taht perspective. Not always porn. Don't know how one would assess whether a tool could cause harm to children. Could be an angle to argue for consideration of how guardianship is put in place.

Martin: Think this point is good. Also extends to gambling and social media online, and sharpens the point well. There is an [article on online gaming sites](https://www.abc.net.au/news/2025-12-04/case-against-the-worlds-biggest-crypto-casino-stake-vip-host/105884760). It is scary. How far these sites are willing to take on addiction. People are rightly concerned.

Sarven: {example on train with child using a mobile device with sounds from the video/app resembling a casino}

Lola: re Yves comment on guardians can also be abusers, "transfender kid trying to find doc and help online". In the UK, if you have a gambling addiciton, you can notify the gov, and other financial industries you have access to. With that you are giving them permission to have a look at those accounts for certain activity. That is a good example of a model that doesn't focus on children. These things affect everyone.

Jeffrey: Age restrictions can be a lazy way to avoid actually addressing the underlying problems.

Martin: When it comes to age restrictions, at some point it goes away. And when it does, there is a blanket ban. And play out a problematic behaviour. Drinking at 21 causing people for example reaching that age abuse it, and not having tools to deal with the situation being unprepared, gambling what have you.

Jeffrey: Saw a proposal that schools run internal social networks to teach students how to deal with them.

Martin: E.g. a kid-oriented social network that verified ages and made a safe space.

Martin: I think we don't want to focus too much on mechanisms. We have bigger problems to point out right now.

Jeffrey: Are we thinking of writing a paper with IAB or on our own.

Martin: First to collect topics. Anything we say to IAB, it'd be to introduce to developing the principles. Rather than doing something separate. They may care about slightly different topics.

Martin: next steps, if anyone interested in collaborating, can collect some points and then start writing.

Lola: I'm interested.

Martin: ... showing interest by doing. Want to get the scope right.


## Breakout C (Europe / Asia / Australia) - [2025-12-18](https://www.timeanddate.com/worldclock/converter.html?iso=20251218T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Lola, Martin, Christian, Matthew, Ehsan 
    
Apologies: 
    
Scribe: Matthew

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) @csarven, @lolaodelola

Lola: Just here to remind us to work on it.

Hadley: Anything you want to record that might help later?


Lola: Nope.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Ack.

### [Explicitly address mental health and psychological well being considerations](https://github.com/w3ctag/societal-impact-questionnaire/issues/32) - @csarven

Sarven: I created an issue related to mental health and psychological wellbeing. The web principles hints on wellbeing, but it's not spelled out. Societal impact doesn't either. If we draw from EWP, we should consider saying the architicture should have some mechanisms to take those things into account. 

... An obvious one is "social web" specs (ActivityPub, ...). They have models and other things to help authors. E.g. How could the "like" activty be used / what is the effect of people seeing that their stuff is liked. How it works in practice is that some nodes don't want to show the number of likes in the UI (similar for reposts, how many followers people have - whether that info should be visible to anyone). Some of this dicussion existed in the Social Web group, and it exists out there. If we put it in the questionnaire then it may be more front and centre for specs.

... This came out of experiences of people leaving social media alltogether; how it affects young people. The web architecture didn't have the right filters/mechanisms to help prevent people from getting addicted or having other negative experiences.

Marcos: Sounds like this focuses on the negatives, but a lot of people do enjoy social media. It doesn't excuse that bad things happen. There could be a trap of protecting one group at the expense of others. Always try to keep perspective.

Lola: the societal impacts questionnaire wouldn't be specific enough to talk abot social media specifically. But it could ask people to think about the psychological effect on the users of the spec. This could apply in other areas (e.g. targetted ads, ...). Just because the technology you're working on has a negative side effect, doesn't mean we have to abandon it, but we look at what guardrails we can put in place to mitigate the harms to users.

Hadley: I was going to say something similar. to Lola. When we extracted the EWP, we looked at things that cuased harm and wanted people (implementers, spec authors, users, developers) to think about those. ... Sometimes we can give the choice to users (or vendors) as to what to do regarding potential harms (e.g. block content). We could play a useful role.

Marcos: Being as inclusive as possible is the goal here. There are some technologies (e.g. DCs) that have impacts themselves, and it's hard to know what the impacts will be. We're not standardizing social medai. Even cookies... they got abused.

Lola: The cookies spec has advice against using it for tracking.

Marcos: Yes. And it's good for keeping people logged in. But at the time we don't know what the potential impacts are going to be. We should be careful not to assume that there is a larger intent. Infinte scrolling is another one. That just came about by someone who created it, and that had the effect of being a hook.

Martin: The point about cookies is a good one, but doesn't suppport your argument, because they chose not to do the thing that was right at the time, which looking back in hindsight was a huge mistake. There were people that didn't understand the implications. When we build the components, we can't be responsible for the way in which they are used to build a system. Not true for cookies as there were people who understood the negative implications at the time.

... Infinite scrolling is a good example, as there's no one thing that enabled it (JS, HTML, AJAX, ...) and they could be used to make many other things. As much as we have a responsibility to think about consequences of what we've built, that responsibility ends at some point. I think the balance we have at the moment is relatively good. Being opne to the experience of people outside of your area of expertise is good.

Sarven: Social web is just one example. With respoect to "likes" - the spec could say "everyone must implement like functionality" but is that necessary? Considering potential misuse, and documenting that, is part of making a good spec. The Social Web community could put some sort of pressure on implementations/notes: "the spec warned us about this and you're exposing something you shouldn't in your implementation". Need something more grounded that people can lean on. Bringing this discussion into a more neutral or formal space. We should continue discussion.

Hadley: Look forward to more discussions in the new year.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: we can skip

### [prevent-credential-abuse#58: Add region locks to Identity Abuse section](https://github.com/w3ctag/prevent-credential-abuse/pull/58) - @christianliebel

Christian: We talked about this last week/2 weeks ago. My suggestion was we could add region locks as an additional concern to the finding about digital credential abuse. Sarven said it was in there, but we could add it explicitly to the list of risks or concerns. We don't have to do it - but let's decide.

Martin: The text suggests that we add a bullet point around restrictions based on location. I think the part Sarven pointed to (that says there are properties that you can't remove from a credential that could then be used for discrimination) is similar. This could be added as an example.

Christian: Should I add an example?

Martin: Could easily add to that list of properties. There are other properties that can cause prejudice (skin tone, name, gender, ...)

Hadley: +1

Christian: So should we add an example box to the part Sarven highlighted (rather than adding this bullet point)?

Martin: The risk of being too specific in these things is that people look at what you've called out, and ignore other potential misuses. We should encourage people to think about the properties that people are leaking.

... The list we're looking at is in sec 4 (Exclusions) - the range of reasons that exclusions may happen. People don't really get to choose where they live. I think it's a great example. The text has changed since Sarven's quoting of it. Maybe an example would help.

Sarven: My point was I didn't have a strong view on it, but we started with specific examples of exclusion, then took them out and went more generic (in the published document) and now we are talking about going back. When I hear "region lock" it's not as clear to me as "birthplace" or "residence" or "nationality" or whatever).

Martin: Who issued the credential - people don't think about the implications of that information being shared.

Christian: thanks for the context; happy to close

Sarven: I wasn't trying to shut it down, rather aiming for consistency.

Christian: all good.

Hadley: If we're going to talk about region locks, in whatever capacity, I think it helps to emphasize the priority of constituencies. Region locks are for rights holders. We are on the side of a more open web, which is in confict; You can see the same conflcit playing out in the "should AI bots be able to scrape the music I've made and published on the web?" debate. Some of our wording implies that the only good is to protect the user. We need to acknowledge that there are interests in other directions, but the user is still more important. Region locks are still prevalent. In taking this stance we are going counter to several established laws.

... Acknowledge Martin's point that it's market controlled.

Martin: Yves making a point in chat that where certain things are regulated, sites can be blocked.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

(no updates)

### [design-reviews#1169: Incubation: Email Verification Protocol](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1169) ([Github](https://github.com/w3ctag/design-reviews/issues/1169)) - @martinthomson, @hadleybeeman, @christianliebel

Hadley: We had concerns such as regarding the venue.

Martin: I have objections to using emails to identify people. Big question is whether they actively involve email providers in the proces. I've advocated that they do. Sam's advocated for the 3-party model. Argument is that if you use the 3-party model the email provider doesn't know you've used it. That pre-supposes that the purpose is for identification, not communication. If we are trying to communicate then email provider is going to get involved. If we are talking ID only, the internet doesn't need an identity layer. The only reason for this is to track people. There is so much more infrastructure needed for the identity case. Just checking that the email address is controlled/owned by the perosn who's visiting the website - we can already do this, directly, inline.

... If you have a 3-party system where the email provider gives people a thing that proves they own the address, you incentivize against private/throwaway addresses. And this is all for the situation where you're not uisng email for communication.

Hadley: So if the email provider is assisting with me verifying that I control the addres (send message, get code) how does this proposal enable tracking?

Martin: It's very like the DCs API - you get a credential that asserts that "this user controls this address" - the issuance is decoupled from the presentation. To do this, you have to ensure the credential is not portable across devices. You need attestation at the point of issuance. You can't do this on a device that doesn't have a secure enclave, which excludes people. It's much much much more complicated.

... My assertion is if you send something to the email provider and then send back to the website it's a very simple exchange.

Hadley: ...that doesn't require a whole load of new stuff. What do we need to do?

Martin: Take it to the IETF.

Hadley: We need a closing comment?

Martin: There's a back and forth at the moment. I agree, we need a closing comment. We need to resolve this by taking it somewhere where people have expertise in all the relevant systems, and that's IETF.

Hadley: Anything to add, Christian?

Christian: Agree with Martin, and sending them to IETF. TAG is not the wrong group to take a look at it, but concluding that they need to take it to IETF is a good thing to do.

Martin: I'm glad they asked, it's an interesting problem, there are some web-related aspects. Trying to build a PKI for email. I'll draft a comment that I think we're reaching the point of diminishing returns here, and the main point is the venue.

Hadley: Suggest emphasising that sending it to IETF has TAG consensus (setting aside the nuances of the discussion).

Martin: Agree that's where we have consensus and is the most important part.

### [design-reviews#1179: [wg/vc] Verifiable Credentials Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1179) ([Github](https://github.com/w3ctag/design-reviews/issues/1179)) - @csarven

Sarven: I haven't looked at this yet.

Yves: we have until 1 February, ideally before so that if we have feedback they can act on it.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Almost finished with it, but haven't finalized my review yet.

Yves: Making progress on it; no conclusion yet.

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Matthew: They did update their explainer. The alternatives-considered section: there was only one, which is to not-do-this. I'm not sure if we should push harder on that.

Mozilla standards position... their comments were positive. Not sure if it's official. The webkit one was interesting. They were saying this doesn't match the spec. then they updated the spec to match chrome's behaviour, so I don't know if webkit is now not compliant with the spec? 

The stuff they have proposed is reasonable. We've discussed it and didn't think it was negative. 

I'd like someone else to take a look.

Hadley: Jeffrey is focused on performance.

Matthew: I'll ask him. 

### [design-reviews#1171: [wg/dx] Dataset Exchange Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1171) ([Github](https://github.com/w3ctag/design-reviews/issues/1171)) - @csarven

Sarven: Working on this one. Can we priortiize the RDF reviews so we can close?

### [design-reviews#1120: CSS find-in-page highlight pseudos]

### [design-reviews#1174: WG Revision: SHACL 1.2 SPARQL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1174) ([Github](https://github.com/w3ctag/design-reviews/issues/1174)) - @csarven

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven

Sarven: Last draft review: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/215#issuecomment-3663084744

Sarven: We agreed last time that a new media type is the right approach. I tried to integrate that into the proposed comment. I have acknowledged what they're doing, and considerations they've made, including the need to be aware of the effect on 1.1 parsers - and that a new media type would remove the potential misinterpretation.

... There's a whole other angle on the story, re the RFC. What I want to hightlight is that, what's happening with 1.1, how it handles syntax it doesn't recognise... all of that's already there. That part is not defined by these specs. 1.2 is not introducing something new to how 1.1s are behaving in practice. As far as 1.1 is concerned, 1.2 is unrecognized/unkown syntax, same as invalid data.

... Tried to write up the space and allow the group to make their decision from that point. I think "satisfied with concerns" is better than "satisfied". What do Martin and Yves think?

Hadley: Keen to hear from Martin and Marcos, and Yves if you have anything. Suggest we be appreciative and clear in our review, and ensure they know what the next steps are (i.e. if we close it, what is next).

Martin: Saren's key point here is to be aware of 1.1 implementations. In my opinion this is not the right approach, but it's their spec and they can live with the consequences of it. I don't think this is going to work well, though it could be a small ecosystem where there will be 1.1 parsers for a long time.

Yves: I discussed with team contact for RDF group, the need to have proper error-handling around versions, so the message is conveyed. OK with Sarven's comment.

Marcos; Nothing to add after last week. We are giving them fair warning, so they can make an informed decisiosn.

Hadley: Suggest you post and close.

Sarven: Thanks all.

### [design-reviews#1160: WG New Spec: RDF 1.2 Semantics]
(https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1160) ([Github](https://github.com/w3ctag/design-reviews/issues/1160)) - @csarven

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples]
(https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Sarven: To me, the concrete syntax is less important than the concepts. The only thing that drew my attention to this is that in 1.1 it was easy to merge n-triples documents. I think this versioning approach where you declare the version inline... it's not clear what will happen if you are to merge the two n-triples documents. Suggst they should clarify that. They put in some language in the IANA registration for updating the media type. They used language like "should not" that belongs in the spec, not the registration. This is also "satisfied with concerns".

Hadley: Have some editorial suggestions, as last time - be friendly, and ensure the actions are clear. Suggest ending with a numbered or bulletted list and have them come back to us when they've done the things (mark as pending external review).

Sarven: I was hoping they'd revisit the versioning issue and, however that comes out, resolve the points we're rasing at a higher level. I don't particularly want to wait for them to come back to us. i think the problem is solved higher up.

Hadley: Suggest making that more explicit, and linking to the other issue. I would make the actions clearer as distinct from the description.

Sarven: "satisfied with concerns" OK? and a link to the higher-level issue.

Hadley: if we're really not happy with it, but closing becuase we're done with it for now, I woudl use a more neutral label. E.g. "ambivolent" or "too early".

Sarven: ACK "too early"

Sarven: Draft review: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217#issuecomment-3669215102

(https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh


