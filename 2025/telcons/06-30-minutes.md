# TAG Minutes - Week of 30 June 2025

Face-to-face scheduled in Hong Kong for Sept 15-18. We plan to organize a developer meetup during that week.

## Breakout A (Asia / Australia / West America) - [2025-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20250701T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Marcos, Max, Martin

Regrets: Xiaocheng

Scribe: Jeffrey, Martin

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola
History in https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1052.

Jeffrey: I think the next action is for Martin to write a comment. Last meeting's discussion indicated that they should bring this up with WebAppSec and prove that it's useful beyond just Google.



### [design-principles#567: Add 'Choose the Appropriate WebIDL Construct for Data and Behavior'](https://github.com/w3ctag/design-principles/pull/567) - @marcoscaceres

Martin: Not perfect, but we should merge the improvement anyway.

1 comment left from Martin, and add IDs to all headings. Async.

### [design-principles#501: Guidance about reflecting state in HTML attributes](https://github.com/w3ctag/design-principles/pull/501) - @LeaVerou, @martinthomson, @xiaochengh

Jeffrey: I think we should close this without prejudice, and say that anyone who wants to proceed should open a new PR. 

Martin: https://github.com/w3ctag/design-principles/issues/289

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson

Martin: I don't think this is compelling, but I see why they do. It's about how we balance the objectives. Whether this delivers user value vs value to the websites. Not sure I agree this gives user value. Might be negative user value in some of the examples, like in cookie clearing. If it becomes trivial to reactivate a passkey after a cookie clearing, there are confirmation attacks. 

Jeffrey: Think they still show the dialog.

Martin: If you've decided to clear cookies because you want the site to forget whether you've been there, then a 'no' on the dialog is distinguishable from the user never having been there. Not justified by the use case. They're trying to avoid showing people login forms.

Jeffrey: We can make the TAG position "don't think this is worth it", but we should also file that as an issue so it's a privacy consideration even if they go ahead against our advice.

Jeffrey: I want to double-check if I can be convinced that this is good, but right now I also don't see the case for this. Action Item for me.

Martin: This is the first time that the form is shown (in that context), so this isn't a recurring experience for people returning to sites to log in.


### [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres

Marcos: Wondering what Safari's behavior is.

Jeffrey: Old issue, which doesn't have standards-positions. I think it's generally ok. Lets top-level frames block things. Or if Safari blocks by default, might allow Safari to re-allow it if the top frame opts in.

Marcos: I didn't like that it used permission policy without an actual permission.

Jeffrey: True, but it's far from alone in doing that.

Marcos: It doesn't fit into the model. Doesn't make sense without having a permission. There's allow= and sandbox=, which could be used. Even their own attributes could be used. 

Martin: Wasn't sure that was the point of permissions policy. It's an attempt to unify a lot of those things, and didn't need to have a user interaction involved.

Marcos: I've been discussing this with Ian (PP editor). Were going to unify them and make it a requirement. Our thinking was to move it in that direction.

Martin: Let's say we do define a new permission. Under what circumstances would it make sense to do that?

Marcos: On the permissions spec side, you end up with policies that the user can enable or disable, hidden in settings. 

Martin: Browser wouldn't necessarily expose it to user choice, but could define a permission.

Marcos: It's supposed to be controlled by the user. Gets weird if it's not. For 3p iframe, enabling it is enabling it. "I trust this iframe to do the right thing." Goes into permissions db. Can query for it. What's it mean to query for autofill. Makes a mess of the permissions database. 

Martin: Concrete example. Give the top-level site permission to run JS. Grant by default, and could logically say is a user-driven permission, like autofill. Autofill lets the site read cross-site state, which is significant. Not a huge bridge to say it's a permission. Maybe there are a lot of things. 

Marcos: Changing the intent of permissions and feature policy. Architecturally. Isn't about perrmissions and enabling features that require permission prompts. Exceptions were sync XHR, at least on the WebKit side where we only support a tiny number.

Martin: XHR, modeled this way, is "permission to jank my experience."

Marcos: Exceptional case.

Martin: Thinking of the sandbox example, might be a good counter-example. E.g. ability to run JS. That's one that's harder to reason about.


Jeffrey: You should write a description of your objection to this formulation in permissions policy.  You are questioning whether this is OK in general and we could escalate with webappsec and have a discussion in the appropriate forum.

Marcos: We have been having those discussions. Would have to find a link.  WHATWG somewhere.  Maybe about autoplay.

Jeffrey: If there is an objection to the general theory, that should be a single decision that covers everything.

Marcos: Questioning on an indiv. basis so far, not overall.  WebKit doesn't support very many of these.


Martin: Conceptually, some could be hardcoded to say "this is allowed" in a particular browser. But policy hooks could be present. Browser says yes always, but the top level site might  not delegat. That's a healthy way to structure these things. But there's additive features, like this autofill thing, which is a new capability that would be granted to a frame. But sandboxing is subtractive. Frames that would previously have expected to do something might have it withdrawn.

Jeffrey: There's a default


Martin: Tightening the default: 

Marcos: gamepad and web share.

Martin: We might have wanted to restrict things, but once cows have escaped. Defaults might be more permissive than we'd wanted. Also can have an acknowledgement when you're restricting it.

Jeffrey: C??P? 

Martin: And you'd only load the iframe if it acknowledges that it can work under the constraints.

Jeffrey: All permissions policies are phrased as positives, and some have a default of "on", and the top level can turn them off.

Martin: Some, like JS, might need the acknowledgement, and that might be Marcos's line.

Marcos: It has a name and can be queries. Which could be fine... But it reflects into other APIs. Not convinced this makes sense for iOS, but they're not harmful.

Jeffrey: Ok with this or want to write up something to start the wider discussion?

Marcos: I'm ok with it. Do like the origin binding. 

Martin: Much better than `sandbox`.

Jeffrey: I can draft a "satisfied" comment?

Marcos: but presumption would need to recheck that each browser does the same thing. Don't think Safari autofills in frames.

Martin: Don't think we do that presently. Sites want to build these horrible things. Talk to John Wilander. He told a story: Credit card form on the web page is a series of frames, which cover just the important pieces. Payment provider has just the credit card fields. Name and address are on your site. You take all the fields and pass them to the credit card frame, so it gets what it needs, and that's protected by PCI-DSS. But you can collect the other stuff. 

Jeffrey: Will ask them to describe existing behavior across browsers so they can defend the defaults, and I'll ask them to ping the standards positions.

### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman

Martin: If the model is that this is a call to PaymentRequest, they should just call that. Don't think we can justify a standardized URL format.

Jeffrey: They see this as a way to  If we're not ok with this, we should invite them to talk to us.

Martin: We should invite them. Would be nice to allow variation in how it's presented, and also to have a standardized form for the information so it could be interoperable.

Jeffrey: I will invite them. Probably needs to be a plenary.

### Jeffrey away next week.

Agreement to hold the meeting anyway.

## Breakout B (America / Europe) - [2025-07-02](https://www.timeanddate.com/worldclock/converter.html?iso=20250702T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Christian, Matthew

Regrets: Sarven, Lola, Hadley

Scribe: Matthew

Reminders:
* Vote in the Vision poll: https://www.w3.org/wbs/168502/202506VisionUSC/
* "Plenary" discussion of https://github.com/w3ctag/process/issues/42, leading to https://github.com/orgs/w3ctag/projects/6/views/1 for prioritization.

### Concerns about modifying roles based on CSS properties

https://github.com/w3c/csswg-drafts/issues/12122#issuecomment-2920507737

Is it just pseudo-elements? Check on duplication with internal links. 


### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @torgo, @lolaodelola

Waiting on Dan & Lola.

### [tag.w3.org#88: Add Ehsan Toreini as a TAG Associate.](https://github.com/w3ctag/tag.w3.org/pull/88) - @jyasskin

Merged based on Christian's review

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @matatk, @dandclark

Matthew: Discussed this with APA earlier. HTML-in-Canvas would be better. Think we're unsatisfied.

Jeffrey: Checking on the two "TAG thinks" claims: "TAG thinks it's likely to be more future-proof to provide a whole point" and the sense that this capability is ok but they should consider a knob.

Matthew: APA was thinking canvas should be an image, with alternative text. WCAG could do more to encourage semantic alternatives to canvas. APA should keep having this discussion.

Agreement to post the comment.

### [design-reviews#1107: echoCancellation mode](https://github.com/w3ctag/design-reviews/issues/1107) - @matatk

Matthew: Did a PR to request a typo. Didn't see any concerns. Appreciated the accessibility & privacy considerations. Concerns APA might have apply more broadly to how cancellation is done. Some people have speech patterns that might get cancelled. But this is narrower. Want to put that on a parent spec. Wasn't entirely clear on how this works: they talked about wanting to cancel screenreaders that the system is generating. Sometimes the browser is playing a stream. but if it knows the screen reader is running, it can cancel that, but can the browser know that?

Jeffrey: I'm guessing based on their description: it sounds like it's the OS doing the cancellation rather than the browser, but we could ask that.

Christian: I've done some reviews for this area, so I'll help with this.

Matthew: This is an example of where we had a boolean but we want to make it an enum without breaking existing code. So they allow both boolean and enum values. Has been done before: ARIA does it with "true" "false" strings. Is it ok to do it this way, with boolean|enum?

Christian: It's been done before, and in WebRTC. Not an unusual pattern.

Jeffrey: ARIA is particularly bad, since "false" evaluates to a true boolean. I think their pattern is fine.

Christian to draft a comment. `satisfied`

### [design-reviews#1110: windowAudio for getDisplayMedia](https://github.com/w3ctag/design-reviews/issues/1110) - @christianliebel

Closed earlier today after Martin's review.

### [design-reviews#1105: ScrollIntoViewOptions container attribute](https://github.com/w3ctag/design-reviews/issues/1105) - @zcorpan, @dandclark

Jeffrey: I wrote a draft comment for this (proposing satisfied; asking for some intro text for the spec).

*Call approves; Jeffrey posts comment*

### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @torgo, @ylafon

Jeffrey: Yves wrote a comment - is to propose a finalized version of it. Marcos had some concerns. There is no WebKit position. Suggest replacing Dan with Marcos on this review.

### [explainer-explainer#28: Fix two pubrules errors: metadata and an editor outside the TAG](https://github.com/w3ctag/explainer-explainer/pull/28) - @jyasskin

Christian: *approves*

Jeffrey: *merges*


### Accessibility Questionnaire

[Title and intro phrasing are slightly confusing, and contradict each other #6](https://github.com/w3ctag/accessibility-questionnaire/issues/6)

Matthew: Yves asked what self-review means. "Short Accessibility Checklist" Several reasons to use checklist. APA may use "Full Accessibility Checklist". Want to give the wider TAG a chance to comment. Can raise a PR, but should ensure this gets discussed.

Jeffrey: Two thoughts: (1) I think APA should own this rather than the TAG, as we're not the experts here and are not using this repository; and (2) maybe this is an "accessibility screen" as the point of answering these questions is "do you need an accessibility review?" so it's letting people screen their spec for whether it needs a full review.

Matthew: Two more thoughts: (1) I like the idea of APA having the short and long questionnaire in APA space, but that's just me as APA co-chair. Needs to be a reason. This is a really good screening exercise, which was made by TAG people. Reason they did it was for early design reviews to see whether they needed an accessibility review, from the explainer. Done as part of TAG review process. Can attach a11y-tracker label. Useful for the TAG. Useful for anyone starting a spec in a CG. Every single spec will get horizontal review. It's really about how early we spend effort. Maybe make that clearer in intro text. If it becomes a spec, it'll get accessibility review, but you might need it earlier. "Screening" is great. Can have that as well as checklist or best practices. Doesn't really matter who owns it. Dan might be one of the few TAG members who was involved in this. Think Dan would argue for it being in the TAG space because it was intended to help early design reviews. Wherever we put it, we should signpost it. 

Jeffrey: My core concern is we're not using this repo and people are not finding it - maybe we should reference it in the Explainer Explainer - and a section about screening and writing about it in Accessibility Considerations.

Matthew: Sounds great. Agree people won't find it in this repo. Think we agree that the results of the form should go into the spec's repository. Idea was to modify intake. Have a PR saying to link to the accessibility answers. Instead of this being a markdown file, host the HTML form that creates an issue in their spec.

Jeffrey: Makes sense.

Jeffrey: The intake changes are merged so you can make changes. Xiaocheng was also talking about doing something in that direction.

Matthew: And should rename the repo to "accessibility screener". Will put things in it. If APA asks for it, can do that then. Will make an explicit reference to APA in the intro text.

Jeffrey: Mostly about who feels empowered to propose/review/make changes.

Matthew: If TAG makes changes, should get APA review.

### Cascading Attribute Sheets

https://gist.github.com/tabatkins/4074abaf486af5b3f7ac289737e216e4

Jeffrey: I posted this to general channel on Slack; not sure who should work on it. I raised all the qeustions we had about CSS touching semantics and accessibilitiy things. With the idea that applying HTML attributes with selectors is better than duplicating those things in CSS.

... Tab came back with this proposal (originally made in 2012, but maybe now's the time).

... Lea re-raised the point about an alternative being needed for IDREFs needing to be assigned to everything. I posted a comment on the gaps repo about creating cross links with selector https://github.com/w3ctag/gaps/issues/2#issuecomment-3025816272

... This might fix the problem with Carousel whereby if you put anchors and links, you have to create a matching ID for everything - whereas if you cross-linked with CSS you could have those generated.

... How do we as TAG encourage someone to design and pursue this? A question I want to start raising.

## Breakout C (Europe / Asia / Australia) - [2025-07-03](https://www.timeanddate.com/worldclock/converter.html?iso=20250703T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: 🪑

Present: Matthew, Yves, Martin, Sarven, Marcos

Regrets: Lola, Hadley

Scribe: Sarven

Reminders:
* Verify that 4 days in Hong Kong, Sept 15-18, works for everyone.
  - Yes!

### Check on PR on accessibility questionnaire: https://github.com/w3ctag/accessibility-questionnaire/pull/7

Matthew: Made some proposed changes to clarify purpose and scope prior to us putting the HMTL version in. We'd like to call it Accessibility Screener. No longer uses the name "self review" as that could be different things to different people. If no objections, may be okay. Aware of input from other experts.

Martin: Seems like a reasonable thing to do. One concern was treating the security questionnaire as a checklist - it kind of is but the approach was intended is to think through about them.

Matthew: Right, it was to encourage.

Martin: Idea is to seek help from experts where needed regarding the Considerations. Perhaps clarify framing re thinking through the questionnaire and asking for support.

Matthew: Generally agree. May open an issue on this and merge what we have.

### [design-reviews#1112: [wg/social] Social Web Working Group new charter](https://github.com/w3ctag/design-reviews/issues/1112) - @csarven

Sarven: I drafted a reply that will go into the w3c/strategy repo. There are no major architectural concerns. Clarifying comments around what they mean by 'maintenance'. Some other HR comments that I agree with - to update Considerations sections.

... The original WG came about 10 or so years ago. This is a new charter to maintain some of the specs in there - following the SWICG. By default they're taking the same specs that were proposed as input. Other HR is saying that we now have a bunch of questionnaires that didn't exist back then, so please update your Considerations sections when it happens. Make sure things are aligned with Explainer Explainer guidance.

... I created an issue mentioning the groups and organisations they should try to co-ordinate with. Currently only mentions the CG. The DID group proposed some vocab that was being maintained by the CG - so WG may need to potentially work with those groups.

... There were a bunch of specs proposed in the end, with some overlap. Some different types of communities that came together and some did their own thing. There's a suggestion that they should make some effort to bridge between these different solutions.

... Jeffrey agreed - I incorporated his changes into the draft.

... The HR review deadline is upon us. Can I post the comment?

Martin: Send it - it helps to make the charter better.

Matthew: +1

Sarven: Ack.

Sarven: Should it be satisfied with concerns, or satisfied?

Martin: They're relatively minor, but use your judgement. Generally 'with concerns' means that we really want to see them make those changes.

Sarven: I think in this case 'with concerns' is appropriate.

### [design-reviews#1097: Browser Bound Keys for Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/1097) - @torgo, @yoavweiss, @marcoscaceres

Yoav: I think last time we agreed to refer them to the WebAuthn folks.

Matthew: Marcos is referring them to the web authentication WG.

### [web-no-papers#6: Phone numbers](https://github.com/w3ctag/web-no-papers/pull/6) - @martinthomson

Closed.

### [web-no-papers#3: Add some text about email addresses](https://github.com/w3ctag/web-no-papers/pull/3) - @martinthomson

Closed.

### [design-reviews#1116: TAG review for Local Network Access(LNA)](https://github.com/w3ctag/design-reviews/issues/1116) - @martinthomson, @ylafon

Martin: Consent/permission is bad.

Yves: People will click through without understanding, for sure.

Martin: for localmess, that's probably OK

Yves: Not convinced of that.

Yoav: There are legitimate use cases for local network access (tv streaming, etc...)  There is also a ton of abuse.  We need some way to draw a line.

Martin: Best we can do for now. Even if we don't settle.  PNA failed badly.

Martin can draft something.

### [design-reviews#1113: Expose resource dependency in Resource Timing](https://github.com/w3ctag/design-reviews/issues/1113) - @yoavweiss

Yoav: This exposes resource timing dependency chaining on resource loading and uses URLs to do that. TRaditionally the URLs are not great for this b/c multiple URLs for the same resource loading at multiple times. In practice it is fine. Previous iteration added IDs. This ignores that URLs are good enough for this purpose and probably correct in 99% of the cases.

Martin: What happens if you get the wrong URL in this case? 

Yoav: If you get it wrong and refer to the wrong resource, the conclusion is still the same. The UC here is for reporting and figuring out dependency loading chaining that you want to load thing you want, or modular preloads. If you get it wrong, it won't matter so that's a good point. Overall it looks good and reasonable.

Martin: Then shoul give a thumbs up. One sentence brief? And post it.

Yoav: Ack.

### [design-reviews#878: confidence reporting for PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @jyasskin, @yoavweiss

Yoav: posted what we talked about. What's left is to say put a label on it - satisfied?

Martin: Think that's right. I'll do that and close it off.

### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

Skipping.

### [design-reviews#1115: Expose unprintable areas via CSS](https://github.com/w3ctag/design-reviews/issues/1115) - @xiaochengh

Skipping.

### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @xiaochengh

Skipping.


### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Matthew: The outcome of various people expressing concern having the interactivity ... addressed the concern. I guess we need ot make a judgement on whether that is sufficient ot close. I can follow-up. Jeffrey may be able to tell us whether to leave at that. Someone poeinting out if you're using AT, it'd be hard to find stuff - it used to be difficult - there is a lot of issues with carousels. We discussed in breakout B - checking how serious it might be.

Martin: Did you see Tab's CAS idea: https://gist.github.com/tabatkins/4074abaf486af5b3f7ac289737e216e4

Matthew: Looks cool, also discussed in braekout B. Discusses some of the gaps. Lola is involved in some discussions on that. It seems so much more better way to do it.

Martin: ... there is a standard list of ... Much easier to author than putting the attributes in.

Matthew: Right now, you can key your CSS styles of the semantic state of the element. If form is invalid, that encourages you to set that correctly before. The challenge of coming up with something better rather than coming up with ids. This could take care a lot of problems.

Martin: ... This is generally to say that the CSS works by default.

Matthew: Will catch up with L and X, and come back.

### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @torgo, @matatk

Matthew: Probably needs others to be assigned. SM?

Martin: Discussed with Tim and Matt N.

Matthew: Are we waiting for more info?

Martin: Feedback was partly private. I think there was some feedback on related website sets-like feature.

Matthew: Maybe there are some aspects of storage access. IIRC, that should be done in Privacy WG. Or is that someting we can still do as a TF w/i TAG?

Martin: Probably not P WG needs to do but may be there for consultation purposes. The analogy to FedCM was interaction flows. User being involved. Could be possible to choose the interaction. Having theuser choose means the pass key involved is their choice, not something that is pushed on them.  It is not perfect but does work better than some intercation models that people have.

Matthew: I can assign Ehsan.

### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @marcoscaceres, @ylafon

## Plenary Session - [2025-07-02](https://www.timeanddate.com/worldclock/converter.html?iso=20250702T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Xiaocheng, Marcos, Martin, Liu, Christian

Regrets: Lola, Hadley

Scribe:

Reminders:
* Vote in the Vision poll: https://www.w3.org/wbs/168502/202506VisionUSC/

### Hong Kong F2F: Sept 15 - Sept 18?

Max & Marcos are ok with this. Martin reminds us of the suggestion for 4 days but fewer hours per day.
Angel offers to help coordinate a developer meetup.

### [process#42: Reduce the TAG's design review workload](https://github.com/w3ctag/process/issues/42)

Jeffrey: How do we develop a unified prioritization out of 

Martin: Once someone has been assigned some work, they're out of contention for the other things, so others' preferences can go.

Martin: Round-robin claim issues. Only work on the top ones.

Jeffrey: That's nearly the same as my suggestion.

Martin: Some discipline about how many people get.

Jeffrey: Can display a count of how many issues each person gets. What do we do with ones people don't claim? I suggested if it's not claimed within 1 month, we automatically close it.

Martin: Say I've reached my 3-issue saturation.

Jeffrey: We don't need a hard limit, but should resist after getting >3-4.

Xiaocheng: Might we lose relevance?

Jeffrey: I think we can explicitly decline things. Chromium has shipped 

Xiaocheng: Should we set priorities?

Jeffrey: How, and what would we use it for?

Martin: It's multidimensional. So something like a Kanban board. Rank them subjectively. Assigning "priority 4" is likely to be difficult. But a total ordering of 48 issues isn't that bad.

Jeffrey: I worry that people wouldn't feel empowered to reorder things, since one person's opinion isn't TAG consensus.

Jeffrey: You're thinking of a single ordering?

Martin: Wouldn't object to multiple tracks. Could have a track per breakout. Then the group of people at the breakout would maintain their set.

Jeffrey: We could set that up and see how it goes.

Martin: Looking at things like FedCM, and thinking we should probably call it and say we're not going to say anything. Whereas I'd rate Page-Embedded Permission Control as more relevant to architectural TAG guidance.

Jeffrey: Actions:
* Set up the Kanban boards by breakout. <- Martin
* Implement autoclosing never-assigned issues after 2 months, to be tuned. <- Jeffrey
* Implement counts of how many issues each person is assigned. <- Jeffrey

Xiaocheng: Assigned issues that are pending external feedback, and without activity for a long time.

Martin: Ping after 1 month, then close after 2 more weeks. They can reopen after that.

### [explainer-explainer#25: Say that explainer contents should move into specifications.](https://github.com/w3ctag/explainer-explainer/pull/25) - @jyasskin, @torgo, @matatk

Marcos: Looks like the right change. Should be good to merge the whole thing. My confusion is that it's not forceful about when you can kill the explainer you should kill it. We end up with people referring to the explainer as if it's the spec. Or people referring to out-of-date explainers. And these explainers get actively harmful. But this is an improvement.

Jeffrey: Merging

### [design-reviews#1102: Rethink the TAG's review intake process.](https://github.com/w3ctag/design-reviews/pull/1102) - @jyasskin

Xiaocheng: Can we ask what horizontal area considerations they're aware of?

Jeffrey: Seems reasonable, but I suggest merging this and then Xiaocheng can you send a PR to do that.

Jeffrey: Anyone else concerned about merging this?

[Crickets]

Jeffrey: Merging.

### [explainer-explainer#19: Explainers are an anti-pattern](https://github.com/w3ctag/explainer-explainer/issues/19) - @jyasskin, @torgo

Jeffrey: I think there's general agreement that they're not an anti-pattern, and that the previous 2 changes have fixed the issues Manu has complained about. Can someone volunteer to draft a closing comment?

Martin: Manu has a point here.

Jeffrey: I think Manu will be fine with closing this, but maybe we should just ask him.

Martin: I'll ask Manu directly about his opinions.

### Findings and higher-level documents

Xiaocheng: After 5 months, I only have the time to work on design reviews. Not the right level. It's discouraging because design reviews are saying a lot of "no" to good ideas. Not talking about the future, but saying "don't do that". Appreciate the effort to redesign the design review process. On writing Findings, what's the right granularity for a finding? E.g. Correct and Incorrect usage of Service Workers? 

Jeffrey: No right answer to that question; it's up to TAG members. The history is at https://tag.w3.org/findings/. Also I completely agree with your problem statement. Everyone should feel free to contribute to the processes, not just chairs.


