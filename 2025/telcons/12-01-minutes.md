# TAG Minutes - week of 1 Dec 2025

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/12-01-agenda.md).

## Breakout B (America / Europe) - [2025-12-01](https://www.timeanddate.com/worldclock/converter.html?iso=20251201T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Ehsan, Hadley, Matthew, Yves, Lola, Jeffrey, Serena
    
Regrets: Christian
    
Scribe: Hadley

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger

Matthew and Serena: not yet

Jeffrey: this was approved by blinkdev to ship last week. There is still time for the working group to suggest changes, and then for the folks to make changes.

Lola: can we get to it soon, or should we reassign?

Matthew: I'll look at it tomorrow.

Serena: I'll have time this week. 

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Jeffrey: We should actually look through the issues and pick the highest priority. We're done with the last round of them. https://github.com/w3ctag/user-agents/issues

Lola: What's pressing?

Jeffrey: Nothing is pressing. It's just... making progress on the general document.

Matthew: Last week, we discussed one of these: Define "user agent" as distinct from "web user agent". I thought we resolved to close it? This was open sufficiently early last month that the discussion we had last week does have an effect on it.

My recollection was that we wanted to just keep calling it "user agent" becasue that is what we do in our community when we refer to browsers, but acknowledge that what we are talking about is specifically "web browsers", not other types.

Lola: yes, I remember that. 

[Searching to find those minutes]

Jeffrey: Anyway, it sounds like this is the next one to deal with.

Matthew: my hope was that we'd dealt with it.

Lola: yeah, we'd come to consensus. 

Matthew: Parts of the discussion were [here](https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/11-03-minutes.md#user-agents31-publish-the-draft-note---jyasskin-ylafon) and [here](https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/11-03-minutes.md#user-agents30-dont-export-web-user-agent---jyasskin-1). There may be others. Do we have an action?

Lola: You could respond to [Max's comment](https://github.com/w3ctag/user-agents/issues/33#issuecomment-3558798353) in the thread, asynchronously. 

Jeffrey: I think I have an idea on what to do for this.

Lola: Also, [number 29](https://github.com/w3ctag/user-agents/issues/29) seems that it should happen. There is enough in the document to have an introduction, no?

Jeffrey: Yeah, I'm not sure what should wind up in an introduction. I'm not sure why I filed this, probably someone told me I should have one? I like how the document starts. 

Hadley: We try to make documents relevant by making the language useful in the longer run,  but we don't specify context. We can give context by writing introduction or blog post, so how do we want to use this as ammunition right now? What should we pick out to put in the introduction?

Jeffrey: This is here because we wrote these duties in the privacy principles, and we have needed something for documents to cite. So it's not about a particular fight, it's about an ongoing need to say "what is a user agent?"

Hadley: You could say that in the introduction? 

Jeffrey: I don't have a picture yet of what should go in there, but Hadley, let's talk more about this.

Hadley: Sure.

Lola: Can you agenda+ those two issues, so we can track them in meetings?

(Done.)

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Matthew: We've talked about being clearer about the lifecycle, for the explainer and that it's ok to move stuff out. It already says that, but more text or a diagram might be appropriate.

We did talk... I had feedback from people who don't write many specs who were confused about "non-goals" rather than "out of scope". We discused this recently; I had thought they were synonymous, but now I don't, since "non-goals" includes things we definitely don't want to happen. "Out of scope" is a more well-known phrase, but in explainers I always see "non-goals", so I think we should be clear about that.

Jeffrey has filed a few things. One came from Ehsan, and we wanted to say for each alternative considered, what it was, pros and cons, and reasons for rejecting it. So we are recommending that, and I'm happy to make a PR for that.

Lola: can you agenda+ those two issues, so we can track them in meetings?

Matthew: Yes.

### [societal-impact-questionnaire#24: Misuse example](https://github.com/w3ctag/societal-impact-questionnaire/pull/24) - @lolaodelola

Lola: I think Sarven has approved this PR, and Christian has commented. All checks have failed though, but I'm not sure why. Failed to generate the static HTML, cannot read properties of undefined... 

Jeffrey: We can debug this offline. Feel free to bug me when document generation breaks.

### [societal-impact-questionnaire#26: Exclusion Example](https://github.com/w3ctag/societal-impact-questionnaire/pull/26) - @lolaodelola, @csarven, @jyasskin

Lola: Only Matthew has provided a review for this. Your question was confusing, Matthew. What link were you talking about? 

Matthew: (reviews it)
    
Jeffrey: I think it's "what is the opt-in mechanism?"

Lola: I get it. 

Matthew: yes. 

Lola: I'll look into that.

And then Jeffrey, do you mind reviewing this as well?

Jeffrey: I think it looks fine, as soon as you add that link.

### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven

(Sarven isn't here today)

### [design-reviews#1160: WG New Spec: RDF 1.2 Semantics](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1160) ([Github](https://github.com/w3ctag/design-reviews/issues/1160)) - @csarven

(Sarven isn't here today)

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

(Sarven isn't here today)

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: I have not looked at this in detail yet, though I started to. The URL for the spec is someone's personal github account, but the explainer is in CSS WG. That makes sense.

Lola: we did discuss last week if anyone else wants to join Matthew on this issue. Please self-assign if you can. Let's ask in the Australia/Americas breakout too.

Matthew: great

### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

Jeffrey: I've not had a chance to look at this.

### [design-reviews#1171: [wg/dx] Dataset Exchange Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1171) ([Github](https://github.com/w3ctag/design-reviews/issues/1171)) - @csarven

(Sarven isn't here today)

### [design-reviews#1158: ViewTransitions: waitUntil() method](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1158) ([Github](https://github.com/w3ctag/design-reviews/issues/1158)) - @christianliebel, @lolaodelola

Lola: Christian's comment seems reasonsable but I wanted to look through the spec itself. So I'll do that.

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Jeffrey: I think Matthew had offered to clean up this comment and post it.

Matthew: We can do it async.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Ehsan: I prepared a table for this, in terms of each circumstance or combination of iframe and top origin relationship. So at least for me, I summarised my concerns in the last two items in the conclusion. There are two things: the matching process is not clear at the IDP level, and the delegation of permission is on the top origin, which I don't think can be trusted for many reasons. Overall, the main issue is the wider cases that two be shown instead of three, and I'm proposing that all situations show three. Based on an ambiguous process, some need to output two URLs instead of three, and that would make users less informed.

This is for the cases in the authentication ceremony that the top origin calls the iframe where the origin is different than the top origin, and it only relates to the UX string shown in the authentication popup or prompt. in the current situation, the iframe origin and the IDP is shown. This spec is trying to add the relationship between the top origin and iframe to the picture as well, and proposing a mechanism that in some cases shows three origins and in some, two origins.

My problem is that that process is ambiguous, and if you want to make users informed, why not show all three?

The announement of the relationship is delgated to the top origin. If the intention of the top origin is not good, then it can lead to different outputs. In the table, I'm showing my understanding of the different outputs.

Jeffrey: the proponent's counter-argument to the bottom two rows is that, if the top origin doesn't want to show the iframe's origin, it can just call FedCM directly without an iframe. So what is the difference and why is it worse to hide the iframe that it's using?

If it... wants to be showing an iframe's origin, it can just call FedCM itself?

Ehsan: In that case, there is no need for this spec. They justified that there is a genuine need for an iframe to be called.

Jeffrey: the use case is for benign top-levels.

Lola: Does that prohibit malicious...?

Jeffrey: you can't.

Ehsan: That's too much trust.

Jeffrey: This is a convenience thing. Top-level origins delegate to an iframe for sign in. Sometimes they are doing it because the iframe origin is more trusted than the top level origin (accounts.google.com in another google.com domain where accounts is resistant to XSS but the other one isn't). But if you're a malicious top-level user, you could just inline the sign-in code in the top-level origin. You aren't going to use an iframe if you don't want to show it to the user.

Ehsan: I see your point. My concern is not about the technical vulnerability, it's focused on the amount of data the user has been shown. It's a UX spec. So the attacks are focused on social engineering. I think users need to be shown as much information as possible for authentication.

Lola: I'm stuck on this: when the top origin is good and the iframe is good, and the fedCM dialogue text is the same as when the iframe is good and the top origin is bad... That, to me, is highlighting the issue of not showing all three URLs. Those two conditions are enough to be like... If you can have a malicious top level origin present the same thing as a non-malicious one, that's not good.

Hadley: Ehsan, can you describe a use case where this would go horribly wrong with two URLs?

Ehsan: UX, so it's limited to the amount of information that's shown. It should show as much as possible. If there's no distinction beetween a good and bad top-level origin, users might not learn as much as they should. I had in mind that if gogle.com as the iframe is supposed to be the iframe that's used for URL scamming, then hiding it will cause some sort of problem for someone. Imagine that gogle.com is similar to Google. Then it could be used as social engineering.

Hadley: How does having a third URL mitigate that?

Ehsan: If the top-origin has bad intention, it would be hidden from the user.

Lola: Having the third URL might prevent the user from giving the information they might normally give?

Matthew: The main situation that we're talking about: you want to sign in to a site that is bad, in collusion with gogle.com, which isn't google.com, and it's trying to phish your account details. In that situation, there is collusion between gogle.com and the top-level frame. You could have a bad top level site that genuinely wants you to sign in with your google account. Badness is in the eye of the beholder. It's not trying to address that situation. It's trying to prevent you giving up your credentials for a valid service.

If it doesn't show all three URLs, you are denied the chance to realise you are signing in to gogle.com and not google.com.

I see what you're saying that if the top frame is bad and the iframe is good, it's a different problem. That's not what the focus is here.

I tend to agree, that not showing all three is inviting more opportunities to be phished. Ehsan has asked that we get them to be clear when they propose to only show two. They talk about relying on the top level origin to make it clear that it and the identity provider are related. So the top level origin (which could be malicious) is allowed to say if the sign-in origin is related. So you could sign into maps.google.com with accounts.google.com, and it doens't show both to the use as a convenience. but the party you are trusting that decision to could be malicious. It's concerning.

Jeffrey: gogle.com isn't helpful here, because the point is that it's confusing with "google.com". Showing it to the user could make it worse. So we need another example.

Hadley: evillogin.com?

Jeffrey: Right. So if the iframe is trying to attack the user, and they are trying to phish the user, there is nothing to stop the top level site from using FedCM to use evillogin.com.

Lola: If the iframe is evillogin.com, will showing all three URLs not at least help the user know that the URL is malicious?

Jeffrey: It helps, but we can't expect a malicious site to use it. There is no benefit to saying, "If you decide to use an iframe, then you have to show it", because if you're malicious and you don't want to show it, you won't use an iframe. If you're good, there are architectural reasons to use an iframe.

Lola: You don't think this invites more malicious attempts?

Jeffrey: I'm not completely sure, but we need to provide the actual use case to explain to the proponents what worries us.

Ehsan: I think it's about helping the user make an informed decision. That will be better achieved by presenting them everything.

Jeffrey: Not always true. Sometimes too much information isn't helpful.

Ehsan: I see your point, but you said there is a problem with FedCM anyway. The problem here is that there are two URLs shown to the user; let's present as much info as possible. But they said in some cases two, sometimes three... I think there should be some consistencies in making this process. I don't think that's helpful.

Jeffrey: The site already has a choice of whether to show two or three URLs, by choosing whether to use an iframe. This lets the site decouple that decision from whether to use an iframe. The question then is: what extra attacks would this allow?

Lola: I think we should think about what this would allow, if any. But I think Ehsan's question on reasons not to show three is good to put to them too. I agree with Jeffrey's point that sometimes too much info is bad, but I'd like to hear their thoughts. I don't think I've heard much justification about how this makes it easier or better for users.

Matthew: I see Jeffrey's point about, "if they're bad, they'll do it differently". I'm not sure that gogle.com is a bad example, but I suspect that if we work through the example, it would be clearer. I'd like to see that written down. And I don't think they're explaining the user need clearly.

Could we take off the conclusion part of Ehsan's comment and post it? At the same time, we could go through a few examples with concrete URLs and domain names, and explain what attacks we are concerned about. 

Jeffrey: +1 to asking for a better explainer

Matthew: Also, is it a bug that you can call FedCM from the top level?

Hadley: Isn't that the point of FedCM?

Jeffrey: It's not the whole point, but we don't want to require that sites rely on a separate iframe to ask for federated login. You should be able to write a site on one page.

Lola: Ehsan, I think you should post your conclusion. Or just the question: why would we not want to show three? What are the use cases? Ask them specifically about the end user benefits on this? And their explainer is a comment, referring to other comments. A better one would be good.

Ehsan: I read through the comments. It has been mentioned, the problem of permission, and delegation of permission. I don't think there was a clear solution for it. I will draft a comment and post it here, so you two can make sure. Because of the history, I would like a second eye.

### Winter holidays?

Hadley: Propose to have our last meeting on Dec 18, then break until Jan 5.

Lola + Jeffrey + others: +1

## Breakout A (Asia / Australia / West America) - [2025-12-02](https://www.timeanddate.com/worldclock/converter.html?iso=20251202T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Marcos, Jeffrey
    
Regrets:

Scribe: Martin + Jeffrey


### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Jeffrey: Marcos, you are still taking an action on this one.

### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin, @martinthomson

Martin: <sends detailed review>

Martin: I'm not happy with the link relations example.  It's not a very good, simple, positive example.  It's not giving readers exactly what they are here to get.

Jeffrey: We might need to refer to an IETF registry.

Martin: Take or leave the suggestions I made as you see fit.

Jeffrey: I should add a "this is working fine, even though it's not perfect" to the Link relations example.

Martin: It's OK to say that "sometimes registries are complicated" particularly when they have history.

### [design-reviews#1092: Web Authentication Immediate Mediation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1092) ([Github](https://github.com/w3ctag/design-reviews/issues/1092)) - @martinthomson, @jyasskin, @marcoscaceres, @toreini

jeffrey: I sent in https://github.com/w3c/webauthn/issues/2228#issuecomment-3576685884 but then learned from Tim that they wanted something that they didn't write down.  They need to work with Ricky to maybe come up with a different design that does address their need, though it might not be the design they originally proposed. I will draft this.

ACTION Jeffrey to draft a new reply.

Martin: Good to hear the new requirement.

Jeffrey: Possibly everyone in the group has a different requirement, so maybe they haven't been clear about what the different requirements are.

### Upcoming holidays/break?

Hadley: Propose to have our last meeting on Dec 18, then break until Jan 5.

Martin: Off over a similar period (20th to ~2nd).

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

We propose closing https://github.com/w3ctag/design-reviews/issues/1108. 

Pointer events: Apple hasn't joined, but we believe Safari has shipped this anyway. There's some concern about the WG's ability to design features that can ship interoperably without one browser's participation, but they've managed it in the past. Don't know how you get .01 of a Philippe. Maintenance is good. " issues marked for future consideration in GitHub" are just 1 issue, so maybe drop that.


---
Thanks for the updated charter.  We think that doing this sort of maintenance is an important task and there isn't anything in particular in the charter that looks problematic.

A few nits we noticed in reading this:

The link mentioned in the "Scope" section points to a list of exactly one issue: "[see  issues marked for future consideration in GitHub](https://github.com/w3c/pointerevents/issues?q=is%3Aissue+is%3Aopen+label%3Av3)". Maybe consider doing something about that.

The scope also mentions that you plan to look at higher-level interfaces ("swipe left", "two finger tap"), but then the out of scope section that follows puts "higher-level APIs" out of scope.  You can split hairs between the two, but it might be better to change the wording for those.  I think that the first is "simplified events for common interactions", whereas the second is "APIs for interpreting abstract user intent via gestures".  Or something along those lines.

You should also coordinate with the CSS WG when defining "new CSS touch-action values".

---

Posted as satisfied: https://github.com/w3ctag/design-reviews/issues/1165#issuecomment-3600133649

### F2F Discussion

Jeffrey: Suspect March 2-5 works best, since W3C said appointment proposals were open until January.

Martin: Hong Kong's 4-days with 1 morning/afternoon off worked well.

Jeffrey: Google will provide breakfast, snacks, and lunch, and locals need to organize dinners and the dev meetup. Locals will arrange things locally.

## Plenary Session - [2025-12-03](https://www.timeanddate.com/worldclock/converter.html?iso=20251203T220000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Matthew, Ehsan, Christian, Martin, Philippe Le Hegaret, YuSen, Yves, Lola, Jeffrey
    
Regrets: 
    
Scribe: Martin

Special guests: Philippe & co to discuss TAG appointments

### TAG appointments

Jeffrey: Philippe will talk about the process and what the expectations are from the TAG as the process continues.

PLH: The Team appoints two people this year to the TAG.  This needs to be ratified by the AB and TAG. (https://www.w3.org/policies/process/#TAG-appointments)  Two years ago this was confusing and there were lots of misunderstandings.  Last year was very smooth.

What the Team needs to understand is what skills the TAG are missing.  Are there individuals we should be considering.  We had some conversations in the past about appointments, but they didn't go anywhere.  The Team doesn't have strong opinions, but would appreciate feedback.  We would like a job description for the appointee, because people ask what the role entails.  The closer we get to the end of the year, the longer it takes.  It can take 2-3 weeks to get responses from people.

Today, this is about who you would like to see on the TAG.

Lola: On the job description.  Hadley shared a description in Slack during TPAC.

Jeffrey linked the draft https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/10-20-minutes.md#tag-job-description
Discussed this in October.

PLH: Yves has it, but make sure he knows.  If it is not final, make sure that Yves knows when it is final.

Jeffrey: probably good enough to use as an indication.
...What skills are we missing on the TAG?

Lola: It would be good to know who is leaving.

Jeffrey: Martin, Max, Tristan

Lola: If Martin is leaving, someone who is quite intimate with the web platform and the infrastructure of it.  How specifications direct or don't direct the platform.  UNderstanding a proposal and its technical implications.  Non-CSS stuff.  Protocols.

Matthew: +1 to Lola.  Not sure who else is active in IETF.  It is good for us to have cross-SDO membership to make sure we are up to date with what is going on.  Hard to replace Martin.  Should we try to get more CSS expertise in?  We had a CSS-heavy TAG a while ago and it seems that we don't have many people.  Xiaocheng is fantastic and we're missing his involvement as he is on break.

Jeffrey: I want more UX people.  We often disagree with proponents on this.  It's great to have Serena here as associated, but it might be good to have a UXR or similar person as a full TAG member.

PLH: OK to push associates.

Jeffrey: Serena can't be appointed due to also working at Google.
...Christian is good on developer relations, but we might benefit from more connections with that community.

YuSen: I found there are no one familiar with GPU and Media and XR.  Is that important?

Jeffrey: We have no one from Latin America, South Asia, Africa.  It would help to have knowledge of how we are not serving those areas.

Christian: Sustainability is on the list of missing skills.

Jeffrey: I would rank that lower than others; the interest group is quite active and we hear from them often.  We see it less in reviews than other things.

Lola: Do we need to prioritize the list?

PLH: I get some indication based on comments.  After that it is about finding the right person.

Jeffrey: Would like to hear about what Lola cares about.

Lola: CSS, Martin, and UX.  I think those are quite high priority.

PLH: Any individuals?

...redacted...

Jeffrey: A vaguer area is the way that ecosystems work.  Maybe that's economics, but a very specific kind.  Someone who knows about managing a space like this.

PLH: AI will solve everything.

Jeffrey: no....
... maybe a librarian also.

...more redacted...

Jeffrey: The next we will hear is about ratifications?

PLH: Yes.

Jeffrey: We will want to have another meeting with the Team to talk about the people you select when that happens.

PLH: OK.

If time:

### [WebAuthn Related Origins](https://github.com/w3ctag/design-reviews/issues/1127) from August

Philippe: Had a discussion with the web payments working group this week.
https://github.com/w3ctag/design-reviews/issues/1127

Apparently this caused a lot of confusion.

This issue was created in the TAG repo, not in the specification review.
Martin comment and closed the issue.
We received a request for the document two weeks ago.  it looks like the WG didn't address the issue, so we declined to allow them to move forwrd, asking for clarification.  They said "the issue was closed".  We suggested that they should consider addressing the spec.
We understand that some people met with the group on Sep 3.  There were no conclusions or minutes.  I need to understand if this is OK with the TAG or if you have an issue with it.  If there is an issue, then I would like the TAG to open an issue against the specification so that the group can address it properly.

Jeffrey: I feel like the TAG still has an issue with the spec.  It's fine to ask us to open that issue. I don't think that we can decide that a spec doesn't advance, but the group should document how they handled the objection.  I think 

Martin: Can recover state and open an issue.

PLH: You are not the only one to have feedback, so this is not on the critical path. but sooner is better. We need clarity.

Matthew: From TAG perspective, it's quite clear that the way the issue was closed was not satisfied.  it was closed because our work was done.  Others can ask us to reopen if they have new information.  Maybe there is a misunderstanding about how the TAG works.  It's totally normal for a horizontal review group to raise issues in the originating repository, but I don't think that we have consensus that the TAG is a horizontal review group.  So we tend to just provide feedback on our threads and don't have issues with other groups.  The non-standard part here is that this is a separate issue; so maybe they missed it.

PLH: They weren't aware or considered the issue resolved.

Matthew: the high-level issue was resolved satisfied, so maybe there was a problem with the way the review was requested.  This was not one review for one feature.  1127 was linked from the main thread and it was clear.

PLH: If you open an issue in their repo, that will close the loop.

Yves: It's quite likely that the WG did look only at the label and not at the content of the feedback when closing the issue.  That's what I heard.
Perhaps this was not as explicit about the connection to first party sets.

PLH: This issue is not gone.  I want that to be on the record.  Both the TAG and privacy people think that this should not be in the spec.  Apparently three browsers already implement the feature.  This is not an easy issue at all.

Lola: Happy to be corrected, but we as TAG do not say whether or not browsers implement something.  We say whether or not it should be implemented as proposed.  It doesn't matter that browsers implement, because that's not what we are commenting on.  I do think that Martin's comment is quite thorough in what we disagree with on both issues and the part is what is similar to related website sets, regardless of who implements it.  They are free to pursue this, they don't need to listen to the TAG.  But I don't know how we could be clearer about the issue we have based on the comment that already exists.  Asking Martin to open an issue on their thing feels redundant.  Unless the request is to re-review what they submitted.

Jeffrey: The idea is just to ensure that the issue is tracked somewhere.

Lola: PLH, did you say that their fix is "the browsers have implemented"

PLH: I don't want to speak for them, but they are not likely to do anything.  Difficult situation.  Can we pretend that reality doesn't exist, or is there something else we can do?

Jeffrey: There is always the option to file a formal objection.  At which point we'd get another go at this on a council.
...Lola said that we don't care what is in browsers.  I think that we do care, but we are not dictators, only advisors.

PLH: Question about how much we want specs to reflect reality.

Jeffrey: We have next steps.  We will see what the WG wants.


### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49)

Jeffrey: We've looked at this in a couple of other sessions.  Will try to get minutes...
https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/11-24-minutes.md

...I put this on our agenda so that we can work out what we do in response to last week's discussions.

Lola: Based on the feedback from last week, it seems like it has been a success this year.  Maybe it's worth doing it again.  On the list, there were two that weren't as active.  Maybe you should consider finding alternatives.

Jeffrey: Terms end automatically, We have to appoint people every year.  We have to ask people if they want to continue.  Overall I agree that we should be inviting people back.

Martin: I think we're asking a lot of people, and we can't give much in return. I want to ask less, by recruiting a larger pool of people. If rather than 5 people, we had 40 people, and you got 1-2 reviews/year, and you turn up to TAG meetings when there's something to report back. A reason to have this program is to identify people who would be good as full TAG members. If people did reviews a couple times a year, people would distinguish themselves. In that case, we'd want to loosen the affiliation restrictions.

Christian: being one of the first, I didn't have the feeling that you asked too much.  Everything was voluntary, I joined meetings as I wanted.  It was good to find out if you were a fit for the role.  That was cool.  I was fine with that.  I think that I got something in return.  Felt like an active part of the group. Warm welcome and insights and feedback.  I'm quite happy with the program as-is.  We should extend it.  Talking to students who want to get into standards is good.  Maybe extend in its current setup.

Lola: Mostly agree with Martin, though Christian's experience is in contrast.  Also, Christian really wanted to be on the TAG before joining.  I have a concern in terms of people turning up to meetings only for what they are assigned.  I didn't see that work this time around.  The people who weren't as active - not to be negative - were assigned things and one turned up to a few meetings.  The other didn't and wasn't responsive.  I hear that we ask a lot and don't give a lot.  People might not turn up.  We should have a process and set expectations.

Serena: As a UX person I don't have a lot of management chain support to be here.  The reason I am here is that I think that it is important to have UX considerations.  But it is difficult to get manager support, I'm lucky that my managers are nice.  Difficult to find the time to do justice to reviews.  To read the explainers and discussion and reaching out.  I do like what Martin says about more people assigned fewer reviews.  Lola's point about not turning up might need more expectation setting about what commitment is involved.  I like this work, but it is difficult to find time for it.

Jeffrey: I was thinking about how we would put Martin's suggestion into effect.  We should appoint associates again next year, but maybe put something in parallel.  Maybe we could make a design review community group  Recruit people to it, have TAG chairs, so that they have a community and time to share their reviews.  The IETF experience is good to learn from.  I feel like that is just a mailing list and not a set of meetings.  Interested in trying to set that up.

Matthew: I don't think that I've +1'd on record before.  The program seems to have worked.  Continuing to do it is a good idea and recruiting more people.  All the experiences described by associates was useful and a good idea.  The CG idea is interesting.  We would rely on people to self-select.  We might not know them as well as we might know associates.  Good to explore.

Martin: <outlines IETF directorate process> Group of subject-area experts. Mostly the directorates have a secretary who draws the next volunteer out of a hat. Some secretaries know the involved people and select the "right" person for a review. Privacy WG has tended toward the second option. 

Jeffrey: It seems like we might have interest in a CG.  Worried that we don't get enough people and that people might not be responsive enough.

Martin: Deadlines are typically 2-3 weeks.  Can remove people from the roster. IETF turnarounds are usually 3 weeks, but sometimes a week or two.  Directorates don't really hold meetings, though maybe secretaries do.

Jeffrey: Seems interest in trialing the CG idea.  We'll get a mailing list and can manage it.

Matthew: We have some good documentation on the TAG website and some of that might be helpful in supporting this.  We might want to be more specific about what we are looking for from reviewers.  I'm doing something like that for APA and would be happy to contribute to that documentation.

Jeffrey: Who would like to help with producing documentation?

Matthew and Martin

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Marcos is not here, so we won't make good progress.

### F2F planning

Proposal is March 3-6, hosted by Google at one of their (many) London offices.

### Breakout Rollup


## Breakout C (Europe / Asia / Australia) - [2025-12-04](https://www.timeanddate.com/worldclock/converter.html?iso=20251204T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Christian, Lola, Ehsan, Yves, Marcos
    
Regrets: Martin
    
Scribe: Christian

### [design-reviews#1138: [wg/webextensions] Web Extensions Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1138) ([Github](https://github.com/w3ctag/design-reviews/issues/1138)) - @csarven, @matatk, @toreini, @christianliebel

Ehsan: We need Sarven.

Marcos: Also happy to answer questions. Had these conversations already. The WG exists for years. They all know what they’re doing, and they’re doing it successfully. I can give that context to Sarven.

_Matthew to ping Sarven._

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: We don’t need to look at this right now. Other related PR is [26] (https://github.com/w3ctag/societal-impact-questionnaire/issues/26), which is not on the agenda. Matthew, I included the link you were asking for.

Hadley: Can we close this issue?

Lola: No, this is a parent issue. We need to add other examples.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: This is a tracking issue. Hesitant to add anything yet, don’t want to create more work for the moment. Simplification of intro material (PR [18](https://github.com/w3ctag/societal-impact-questionnaire/issues/18)) might be a good next issue to work on.

Hadley: Where do we publish this?

Lola: Think this has been published as [a draft](https://www.w3.org/TR/2025/DNOTE-societal-impact-questionnaire-20251202/).

Hadley: Do you have a plan for the next publication?

Lola: No.

### [prevent-credential-abuse#56: This is about government issued credentials](https://github.com/w3ctag/prevent-credential-abuse/pull/56) - @martinthomson

Hadley: Martin is not here. I would have the same questions here, since this is published, how much do we want to tinker with it? Question for him. If he's done, it would be helpful to close this issue. 

Matthew: Think this is quite negative, but we were very positive on the design review. We should check back with Martin before he officially leaves.

Yves: As it’s a finding, it’s quite easy to publish new versions.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

Marcos: It’s on my todo.

Hadley: Any deadlines?

Marcos: No, nobody is waiting for us.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Haven’t finished reviewing it yet, try to do it next week.

Hadley: Are we ok on time for this one?

Ehsan: They didn’t mention any deadline on the issue.

Yves: I’ll try to take a look at that next week.

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Matthew: Haven’t made any progress on this, next on my list.

Hadley: Ok on deadlines?

Matthew: From the issue number, it looks like we’re a bit lagging behind. Will look at it.

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @lolaodelola

Christian: the proposal may be out of date. they may want to do cross-origin handshakes.

Lola: We need an updated explainer, if so.

I'll comment and ask. 

Yves: My concerns were mitigated by the fact that it was same-sites only. they were making an assertion on behalf of other resources. So if they've changed, i'm concerned. It's better to clarify if it has changed.

Hadley: I agree. 

### [design-reviews#1169: Incubation: Email Verification Protocol](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1169) ([Github](https://github.com/w3ctag/design-reviews/issues/1169)) - @hadleybeeman, Martin, Christian

Christian: Martin has comments, so we can draft a comment. I think this should be an IETF thing. there are solutions for it already, like webOTP. I wasn't that convinced yet. I will draft a review comment, send them the questions without a resolution.

Hadley: great, thanks. 

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: They recently added some more info, we need to catch up. Will look at it and come up with next steps.

### [design-reviews#1119: Digital Credentials API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1119) ([Github](https://github.com/w3ctag/design-reviews/issues/1119)) - @martinthomson, @matatk, @toreini, @lolaodelola

Lola: I’ve drafted a closing comment. Martin is fine with the closing comment, but it doesn’t mention any of the questions that Matthew and Ehsan had. Wanted to give you the opportunity so we can ask them if neccessary.

Matthew: There’s the fundamental issue that the user agent was acting as a pipe for the user, specifying protocols blessed by the working group — it mitigates that. Plus we have everything in our Preventing Credentials Abuse finding, as Christian mentioned.

Ehsan and I can check this by the end of the week. We will come back to this EOD.

Lola: Last time we spoke about this, Martin was ok to close this as "satisfied." Want to close this really soon.

Matthew: We will have a look right away.

Christian: Can we really say "satisfied" when we have a whole finding documenting the potential abuse factors for this API? Shouldn’t it be at least "satisfied with concerns" and point to the finding?

Several people: I agree

Lola: I'm not sure I agree. This API, if done well, will address some parts of the concerns. 

Matthew: it wouldn't solve overreach, it wouldn't solve governments saying, "You have to use this."

Lola: right, buti woudl provide a mechanism of doing it in a safe and secure way on the web. Yesterday when we were talking about WebAuthn in the plenary, we discussed if our reviews should document things as they are, or... Well, if there are implementations in the browsers, saying "satisfied with concerns" can cause a conflict. it seems like we are not being consistent. If therei s a concern with this, we should know that this is going to happen anyway.

Hadley: I think we can express that in a closing comment. Hear what you are saying. Sometimes we are writing for the immediate response, sometimes for the record. I think it would make sense to document the reservations here, also for people looking back at the issue in the future to see what the TAG thought about this development.

Marcos: With my editor hat on: Because the formats are specified, we (the W3C side) don’t have control over the bad stuff mentioned in the document. There is no way from the W3C side to prevent this. If governments want to do bad things, they can. Would be inclined to go with the concerns.

Christian: I talked to normal, random people about this, and everybody was deeply shocked. I would consider it harmful. it's not an API thing, it's the concept itself that is a problem. Not the API. I guess "satisified with concerns" seems right, with a good summary of what we've discussed.

Lola: I’m happy to make it "satisfied with concerns." Just want to make sure we close it. "We understand that the API is moving forward, and we don't necessarily disagree with the API but have concerns about the direction of the web." and point to the finding.

And then Matthew and Ehsan, you'll come back today to check that there are no outstanding things. If so, I'd like to pass on the baton to somebody else. 

Hadley: If the outstanding things come from Matthew and Ehsan, they would be the receivers of the baton?

Matthew: Yes.

Hadley: Who’s drafting the closing comment?

Lola: I will do it.

Hadley: And once Matthew and Ehsan give the all clear, you will post it?

Lola: Yes.

### Upcoming holidays/break?

Hadley: Propose to have our last meeting on Dec 18, then break until Jan 5.

*Approval from breakout C. Looking at the minutes from breakout A.*

Lola: Sounds like consensus!

### TPAC Meetings Tool

Matthew: Would like to make the tool even more useful next year, if you have any feedback, send it in.

### March 2026 F2F

Lola: The F2F is going to be happening in March 3–6 at one of the Google offices. In the chairs channel, Matthew, Hadley and I suggested to plan the London side of things. So the three of us could plan the week for our colleagues.

Hadley: Four days?

Lola: 3.5
