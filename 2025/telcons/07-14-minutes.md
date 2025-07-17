# TAG Minutes - Week of 14 July 2025

## Breakout A (Asia / Australia / West America) - [2025-07-15](https://www.timeanddate.com/worldclock/converter.html?iso=20250715T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Max, Jeffrey

Regrets: Xiaocheng, Marcos

Scribe: 

<!--Agenda+-->

<!-- Design Reviews -->

### [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres
### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh
### [design-reviews#1115: Expose unprintable areas via CSS](https://github.com/w3ctag/design-reviews/issues/1115) - @xiaochengh
### [design-reviews#1043: CSS.highlights.highlightsFromPoint API](https://github.com/w3ctag/design-reviews/issues/1043) - @torgo, @xiaochengh

### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Max: Last week we thought this might cause interoperability problems, because not every model will have the same features. Marcos drafted something. 

Jeffrey: Some pieces of Marcos' draft feedback are good, but other parts don't make sense. "The presumption that the model is on device is wrong" can't be right, since the proponents say they're proposing to keep the model on the device. We probably can't agree to post anything here without Marcos.



### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres

### Prioritization

We allocate all issues in https://github.com/orgs/w3ctag/projects/6/views/1 to breakouts, and roughly sort the Breakout A issues.

## Breakout B (America / Europe) - [2025-07-16](https://www.timeanddate.com/worldclock/converter.html?iso=20250716T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Ehsan, Martin, Lola, DanC, Jeffrey, Yves, Hadley

Regrets: Matthew, Christian

Scribe: Jeffrey


Lola: Face to Face venue changed. Check your hotels.
<!--Agenda+-->

### [explainer-explainer#7: Explain why to focus on the end-user's need, and/or moderate that advice](https://github.com/w3ctag/explainer-explainer/issues/7) - @torgo

Jeffrey: We've been pinged a couple times on this, so we should ensure it gets addressed.

Lola: DanA promised to get to it. I'll ping him.

### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @torgo, @lolaodelola

Lola: DanA's looking at this one too. Give him until next week.

<!-- PRs -->

<!-- Design Reviews -->

### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @torgo, @matatk, @toreini

Lola: We talked about this last week but were unsure about the next steps.

Jeffrey: I think this is Martin's call.

Martin: There was something around the Related Sites feature that needed more work. 

Jeffrey: We should make that explicit. And we were looking at how the platform should handle groups of related sites in general.

Lola: I put that on the Privacy WG agenda for tomorrow. Martin can you leave a Related Sites comment?

### Organizing the design review priority list for breakout B

https://github.com/orgs/w3ctag/projects/6/views/1 

We go through the issues.

* Canvas place element #997 was renamed to HTML-in-Canvas
* Web Speech API contextual biasing #1121: DanC says we should handle it quickly or not at all. Jeffrey suggests that it's low-priority. Lola suggests declining but will look.
* FedCM: We have lots of FedCM issues. Discussion of DanA's opinion on declining these. Jeffrey suggests we should decline because they're too old for us to have an effect, and they're small tweaks to FedCM. Hadley closing these.
* Permissions Policy reports for iframes #1050: closing while WebAppSec figures out a consensus proposal to bring back to us.
* Permissions Policy Reporting and Report-Only mode #909: marked as timed out.

DanC: One design review got reopened that isn't on the project board: Declarative CSS Modules and Declarative Shadow DOM adoptedstylesheets attribute #1000. 
[Agreement to put that at high priority in breakout A]

### Documents


Lola: Docs CG discussed the explainer explainer. Want to invite Jeffrey and Matt. Tuesday the 29th at 4pm BST == 8am US-Pacific.

Martin: Need to finish the Digital Credentials one (web-no-papers). DanA and I have done most of the work that's on us. Marcos didn't hate it. Need critical feedback about whether it's the right messaging. Is it tight enough? Need more material in an area?

Jeffrey: I want to review this, but wider, how do we get the right level of attention? I have a theory that we should file a "TAG, please review this" issue on the repository, and agenda+ that issue.

Lola: Can we assign a group?

Martin: I think everyone on the TAG should read it, to ensure we stand behind it.

Ehsan: I'm happy to do that. I've also filed issues on this repo.

Lola: Need to have a streamlined process for managing documentation reviews. Since we want to prioritize documentation.

Jeffrey: What should that process look like?

Lola: Have comparable partner repo to design-reviews. People open issues like design-reviews with a link to the document. We can assign people to that review. Conversation on the issue, and everything's in one place, so the assigned person has all the context. 

Jeffrey: So one doc-reviews repo, with an issue for each document? Suggest filing a "TAG-wide review" issue with agenda+ in each repo. 

Hadley: Assign all TAG members?

Lola: Assign the people focusing on it, and let the presence on the agenda notify others?

Hadley: 2 steps: second step is to assign everyone so that everyone gets pinged. That way we can get TAG-wide consensus to publish. 

Lola: Should we document this somewhere?

Jeffrey: We should document it in the w3ctag/process repo. On my TODO list but never bubbles to the top. 



### Accessibility

Lola: where are we on this?

Jeffrey: Matthew has someone writing an HTML page to help people do the review and file an issue. Discussion over where it should live. Might be good to ask Matthew in C.


### User agents

Lola: Accessibility of UAs? I was reading WCAG's definition of accessibility-supported. 2 components. First is that the way the tech is used must be supported by assistive technology. Second includes that the tech must have accessibility-supported UAs that are available to users. What is "accessibility-supported UA"? The discussions with experts indicate that there's no guidance on how UAs should be accessible. There's a UA document, but it's out of date. No ownership. https://www.w3.org/WAI/standards-guidelines/uaag/

Jeffrey: Lots of issues filed, but I and Sarven haven't found time to tackle them. 

Lola: Holidays. Postpone discussion until everyone's present. Maybe a week where we tackle these issues.

### Societal Impacts Questionnaire

Lola: Work for Sarven and me. Won't block on Tristan.

### Architecture of the Web

Jeffrey: I want to work on this but haven't found time. 

Lola: Maybe I'll find time.

Jeffrey: I have 2 presentations that might have useful bits.

### Web Without 3p cookies

Hadley + Jeffrey: Think we've published that as a finding.

Lola: Still has 4 issues.

Lola: We should have a way of identifying what's a draft and what's published.

Hadley: We do invite comments on published findings.

Yves: We have a list of approved findings. We could annotate the GH repos that are no longer in draft status.

Lola: Web isn't versioned.

Jeffrey: I think that's also finished.

Lola: Privacy Principles and Design Principles?

Jeffrey: Privacy Principles is waiting for a pile of issues for us to work on. Design principles is in active maintenance, but perhaps we should look through its issues and see which ones we ought to prioritize more highly.

Lola: Add Design Principle issue triage/prioritization to next week's agenda.


### F2F Agenda

Jeffrey: We also have a F2F coming up.

Hadley: I always think there should be a better way to set up that agenda. There is some script that pulls out everything into a Google Sheet. Then we manually pick out priorities, group by breakout. Doing it manually gives us the leeway to say "J you're needed in 2 groups and can split them." Automatically wouldn't let us do that.

## Breakout C (Europe / Asia / Australia) - [2025-07-17](https://www.timeanddate.com/worldclock/converter.html?iso=20250717T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Hadley, Matthew, Ehsan, Lola, Max, Yves

Regrets: Xiaocheng, Christian

Scribe: Lola

<!--Agenda+-->

<!-- PRs -->

### [accessibility-questionnaire#7: Clarify title, and scope](https://github.com/w3ctag/accessibility-questionnaire/pull/7) - @matatk, @matatk

Matt: Martin made suggestions last week and I've encorporated those suggestions.

We are also saying last week that we will add this a11y-tracker label onto the issues that have a review, so that the APA are aware of it.

Are we happy with this suggestion: https://github.com/w3ctag/accessibility-questionnaire/pull/7#discussion_r2212685689

There isn't a reliable way to add label automatically but it's fixable. We can merge if we're happy with above suggestion.

Haddley: What do you need to merge?

Matt: Can the people here give consensus? Should we promo on slack?

Hadley: If there's anything contentious, post to slack. If not, go ahead.

Matt: I don't think it's contentious but I can ping on slack and merge tomorrow barring any issues.

Hadley: You might be being overly cautious.

Matt: We can merge it, and let people raise issue if there are any.

Hadley: I'll commit your suggestion

(GH issue with committing suggestion arises)

Matt: I'll make changes and ping you when it's ready

### [web-no-papers#10: Adding a conclusion](https://github.com/w3ctag/web-no-papers/pull/10) - @torgo

Hadley: where did we land on the torgo issues? I think he wanted to stay an editor on this

Lola: I think we need to chat to Dan, maybe face-to-face, to figure out how to handle this.

Hadley: He and I disucssed whether it made sense ot create a little task force for these documents.

Lola: I said something similar last week. 

Hadley: I'll take the action to arrange a call with him. 

<!-- Design Reviews -->

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @toreini

Ehsan: We're still discussing and have asked the people involved to clarify some things

Hadley: is it urgent?

Ehsan: It doesn't seem to be urgent since it seems like a small addition but I can double check with Jeffery and Martin

Hadley: It's concerning when one conversation is happening across issues, do we have links connecting the relevant issues so that we're aware of relation?

Ehsan: yes, in the project brainstorming

Hadley: Brilliant

### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @matatk, @xiaochengh

Matthew: we had some queries about htis, Martin is particularly interestsed and I agree: why are they adding an extra layer of indiection here, why are they not using selectors? Xiaocheng hasn't come back to clarify. 

We did talk about: 1. Asking that (above), 2. it's very underspecified in terms of the set of functions. We assume they come from UI events, but we wouldn't want to use the whole set. but there are things in there that wouldn't make sense as triggering functions. 

Looks like no one has asked the question. We could ping Xiaocheng at the plenary, and then I could draft a comment. 

### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Matt: There's a lot of internal discussion. I like Xiaocheng's idea but there's still not consensus in TAG on what to do, Jeffery has shared Moz standards position. The proponent has been invited to July 31st Plenary. Nothing to do for now except catch up on brainstorming thread on the issue.

### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @ylafon, @marcoscaceres

Yves: I've made some progress, but not done yet. My questions are around is it wasting rescources if we're keeping things alive? How useful is it really vs destroying the frame all together? If something becomes invisible, the default should be that it stops and you should enable it. I'll update the private brainstorming

Hadley: Are implementers in a rush?

Yves: No, it's early review

### [design-reviews#1117: Add IndexedDB getAllRecords() method and update getAll()/getAllKeys() to support direction option](https://github.com/w3ctag/design-reviews/issues/1117) - @martinthomson, @christianliebel

(Martin & Christian not here)

### Organizing the design review priority list for breakout C

https://github.com/orgs/w3ctag/projects/6/views/1 



## Plenary Session - [2025-07-17](https://www.timeanddate.com/worldclock/converter.html?iso=20250717T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Attending: Lola, Christian, Matthew, Ehsan, Yves, Jeffrey, Hadley

Regrets: Xiaocheng, Sarven

Scribe: Matthew


### Usual agenda

<!--Agenda+-->

#### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

[WebAppSec discussed this yesterday: https://github.com/w3c/webappsec/blob/main/meetings/2025/2025-07-16-minutes.md#dbsc--browser-initiated-vs-server-initiated-flows]

Jeffrey: The proponents are coming back with an update as a result of that discussion, so we should wait for now.

#### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Matthew: Still working on proposed comment - I have an outline in the private thread - could you check anything is missing?

Lola: Many documented UX issues. Trying to make the pattern native to the web, without addressing the known issues, isn't a good idea.

Jeffrey: This is a reasonable thing for us to say. We could recommend reconsidering based on this. I think they'll say people want to do this kind of UI so we are making it work better.

Lola: Sara's 'blog post was illuminating.

Matthew: I'll include that and think about how to more strognly word the caution, in light of what we've found doing the review.

#### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman

Jeffrey: Martin and Marcos were concerned about it. I think it's prety well justified. At most we should be satisfied with concerns because it's not fully specified, but this is just a declarative way to trigger the payment request call. It has some issues but seems like a reasonable extension. I don't know that we can conclude on it without Martin and Marcos to give the counter argument.

Matthew: I recall Sarven being concerned that it's opaque. Did we resolve that?

Jeffrey: The opaqueness of the URI *looks for Sarven's comment* - I feel like a payment URI is always going to be a bit opaque. They're identifiying a transaction rather than being readable. You can do something with the origin, but the rest is up to the site. Maybe Sarven had something I am missing. Not sure how to respond further.

Lola, Hadley: Sarven seems interested.

Lola: Any further concerns?

#### [design-reviews#1012: User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012) - @matatk

Matthew: Looks like OK to time out as discussed but would appreciate once-over from someone on the question of whether it leaks more than was already available - S&P answers sort-of seem to say no, but I'm not 100% sure.

#### Accessibility Docs - @matak

Matt: We're ready to merge, repo needs to be renamed to accessibility screener & we'll shortly follow up with HTML repo & try to setup a11y-tracker tag. We agreed about APA having a headsup for these questionaires.

(Matt & Hadley sort out GH permissions/assignment stuff)

Matt: We're also reworking APA fast checklist in the same way, and updating APA's questionaire for reviewers.

### W3C budget and funding activities

Lola: Discussions have been going on. Application for IEs to attend TPAC is now open. Due by 8th of August IIRC. Thanks to Jeffrey and Yves for helping to make this happen.

https://github.com/w3c/AB-memberonly/blob/main/documents/budget2026-feedback.md (Last year's budget: https://www.w3.org/Member/financials/2025/fy2024-financial-report.html)

Jeffrey: Various groups have asked for AC feedback about the W3C budget. The Team is in charge of doing the budget, though they are not as active in collecting feedback. There is some feedback about technology strategy, which should come to TAG. I wanted to create some space for us to talk about it.

... Two things I thought of: (1) ensuring there is budget for IEs to travel - ought to be in the budget for next year officially; and (2) we identify gaps in the platform but we can only talk about them - maybe W3C should be able to fund work on the gaps we identify. Is that TAG consensus? What else should we say about the budget?

Hadley: Broadly agree. We haven't funded work directly in the past. Sometimes it could go badly; hard to separate our expertise from a lot of drafting work. Not against it, don't see how it would work, but not against exploring it.

Jeffrey: The idea of contracting out web platform work has matured (e.g. Igalia). Regarding things like [ID and Attribute Sheets idea](https://github.com/w3ctag/gaps/issues/2), and we know former TAG members who we trust to work on this.

... I'm imagining that the TAG decides on the work, and someone (likely the Team) picks someone to do the work. That layer of indirection might make it appropriate for them to hire a TAG member, but it may not. But the stuff we know about, there are non-TAG members who are appropriate.

Hadley: examples?

Jeffrey: many in the Gaps repo: https://github.com/w3ctag/gaps/issues.

Lola: E.g. the work we discussed regarding figuring out all the use cases for related web sites. May not be a priority for Privacy group, and they meet infrequently. Could be good to find someone to engage on this.

... What would be the next steps?

Jeffrey: Based on these minutes, I can reply to the AC forum thread and say what TAG would like.

### F2F Agenda

Hadley: I think there is opportunity to make the process of planning the F2Fs a lot more efficient.

*group looking at agenda planning workbook* https://docs.google.com/spreadsheets/d/1D7low9ygKMXzzFcClTh5Q75JQwHTLdzpW0qPv1BSsUU/edit?gid=32429984#gid=32429984

Different sheets for different aspects of the meetings (e.g. food, issues, ...)

The issues sheet: a script or something (?) pulls out a list if issues, which we allocate interest to, which then allows us to start allocating breakout sessions.

Any given slot on a day has n (usually no more than 3) breakouts, each breakout focusing on a particular set of related topics.

Problems arise from tying IRL and virtual re time zones. Also figuring out which breakouts to assign people to (laborious).

Jeffrey: In Paris we had topics, where each person would make a short presentation on their topic, then breakouts would discuss in more detail (in parallel), try to come to consensus, and then report back to the wider group afterwards.

... the Paris one was a bit hastily planned in that respect; need to find out if this worked for people.

Hadley: Found the big-picture topics useful. We were in the middle of shifting focus towards wider issues rather than just design reviews, so helpful. Depends what position we are in in HK.

Lola: What are our goals for HK? There's stuff from Paris that we wanted to follow up on in HK.

Jeffrey: I expect the 3 chairs will talk about this in a bunch more detail, so we should listen to what the rest of the group wants in these calls.

Hadley: We also want to ask the editors of the documents in process.

Lola: IIRC we said we wanted to focus more on documents.

Matthew: Could go over Explainer Explainer.

Lola: And accessibility screener?

Matthew: Yes we should have some datum points by then.

Jeffrey: Recruiting for the TAG election.

Yves: Elected or appointed seats?

Jeffrey: Elected first, how we can increase the field.

Matthew: Was thinking recently about how it would be good to have consistency for how elections are run (meet the candidates (with TZ considerations), qeustions, email ettiquette, ..., preferably by comming to community consensus rather than rules). Should TAG discuss? Should I email AC forum?

Yves, Jeffrey: best to contact the AB first for this. Could present a TAG view to them.

Lola: Thus, topics for HK @@@@@@@@ missing; including ^ @@@@@@@@

Lola: Are there obvious things to focus on, certain documents? The way we did it for Paris might work well, and not be too much of a lift. And as we're more on top of design reviews, not having so many breakouts on this.

Hadley: I haven't heard anyone saying we ened more time for design reviews.

Jeffrey: This seems like a good general direction.

Hadley: We should ask all the document editors what they want next week.

Matthew: Really thought it worked well in Paris; people owned topics but everyone collaborated on everything. Good mix of technical leadership plus day-to-day design reviews. Enjoyed it!

### Breakout Rollup

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)





