# W3C TAG Minutes - Week of 29 Sept 2025

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/09-29-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please edit this document.


## Breakout A (Asia / Australia / West America) - [2025-09-30](https://www.timeanddate.com/worldclock/converter.html?iso=20250930T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Dan
  
Regrets: Martin

Scribe: Jeffrey


### [design-reviews#1130: Incubation: An `Origin` Object](https://github.com/w3ctag/design-reviews/issues/1130) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1130) - @csarven, @dandclark

Jeffrey: That looks good. Dan to post?

### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://github.com/w3ctag/design-reviews/issues/1134) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1134) - @jyasskin, @dandclark

Jeffrey: Dan's draft comment looks good. We should rephrase some of the review bullets, concatenate it, and post it.

Dan: I'll clean this up and post it tomorrow.

### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh
### [design-principles#590: Add principles for task sources](https://github.com/w3ctag/design-principles/pull/590) - @marcoscaceres
### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres
### [design-principles#594: Clean up link-defaults.](https://github.com/w3ctag/design-principles/pull/594) - @jyasskin
### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres
### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

[Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Breakout B (America / Europe) - [2025-10-01](https://www.timeanddate.com/worldclock/converter.html?iso=20251001T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Martin, Yves, Sarven, Dan

Regrets: Matthew, Ehsan, Hadley, Lola

Scribe: Sarven, Jeffrey

PRs and Agenda+

### [explainer-explainer#9: Update the WebIDL guidance for explainers](https://github.com/w3ctag/explainer-explainer/issues/9)

Jeffrey: Do we want to moderate that? Certain reviewers say "never do this".

Martin: Explain the thing you're doing in the best way you possibly can. If we say "never", we should say why it's wrong and what would be better instead. There are cases where they explain their API high-level and the only thing they can reach for is the IDL instead of the details. "These are the basic capabilities we are looking to expose" rahter than saying the canonical UC we have. The MLS API, multiple ways to interact with that system, and the example that's shown is not the good example, so both example and the API makes sense. The IDL might move to a spec so don't need to put it in the explainer.

Jeffrey: I think you're saying always include examples in JS first and IDL is acceptable for wha tyou think is best.

Martin: But only if you think that's best. Whether there are pitfals for people we need ot advise people.

Yves: WebIDL might show optional parameters that we'd want to discuss. Using only WebIDL would be bad because it won't show how to use the API for most of the time but it is good to have it. It is not mandatory but good for some edge cases, and might change the reading of the API.

Jeffrey: I like Martin's use IDL only to show if that is the best. Enough for me to PR.

### [design-principles#584: Replace asking for users for consent with designing for user intent](https://github.com/w3ctag/design-principles/pull/584) - @mharbach

Martin: Marian is doing good work here. This one is more about getting on the underlying principle. Probably a couple of things still outstanding on this one, and not ready for wide-review. If you get a chance to review now and finalising, it'd be good. Difficult topic but this PR is significantly for the better. There are a couple of **questions for the examples**.

Jeffrey: I think David Baron was satisfied with that question.

Martin: Also looking at overall as a principle whatever fits with your understanding of the situation.

Jeffrey: So TODO for people to review this.

Martin: Should say it is mostly done.

### [prevent-credential-abuse#52: Add discrimination based on certain fields under Exclusion](https://github.com/w3ctag/prevent-credential-abuse/pull/52) - @csarven

Sarven: Follow-up to discussion at the F2F. There was a change about harm. Added a bullet point that gets more to the heart of the issue. Something might conform, but because certain fields are exposed in the credential, it's a target for misuse or for discrimination. 

Martin: Not clear how this connects to your example, or maybe that wasn't the intent.

Sarven: Overlap in place of birth in passports. I added gender. Date of birth is required in passport standards. Thought 1-2 examples was good enough.

Martin: Your example was about the structure of the credential, but this PR is about the content being used to discriminate. It's tenuous to use this example here.

Sarven: If certain optional fields are forced, there's a danger of being misused. Birthplace would be a way to filter people.

Martin: This is more about when a credential contains secondary/extraneous information, that extraneous information that the recipient doesn't have a real right to ask for, but the credential system includes it ... it's used as the basis for discrimination. We should say that more directly. "Where credentials contain extraneous information, that offers new opportunities for discrimination based on the value of those fields."

Sarven: Want me to try to edit that? Or make a change request.

Martin: I might suggest text. This is also related to minimization stuff we talk about later, but it's a good example of how inflexibility in credential systems can lead to downstream consequences. I'll suggest something.

### [user-agents#25: Add Audience section](https://github.com/w3ctag/user-agents/pull/25) - @csarven, @csarven

Sarven: I thought in the F2F discussion we decided to limit it to the list in the PR. Covers similar roles. Marcos suggested adding web developers, which I think is not the target audience. Potentially we could list all sorts of roles. But if we do that, it widens the scope of the document. By limiting it, maybe certain content is attractive to target audiences. I thought web developers shouldn't be one of the targets since they're not directly implementing how a UA needs to behave. Of course might build a web page. We do have specifically UA developers. 

Sarven: Original proposal was "technical authors", which covers spec authors and others. As opposed to explicitly saying "spec writers".

Jeffrey: People reading that may not think spec writers are part of tech authors  but agree re tech authors

Jeffrey: Web developers sometimes think the UA serves them instead of the users. It'd be useful to point them to this document to say "no, you're wrong". I'd lean towards adding that because they care less about the details.

Sarven: My understanding of target audiences is about who should read the document. There's material here where, for example, a policy maker might want to quote this. Think you're saying something similar. Unless we put specific text, it might imply there's nothing here for you. Maybe distinguishing them from UA developers. Don't want to draw attention to too many roles. Don't want to make people waste their time, since there's likely nothing they can apply in their work. But anyone could potentially read this document and make their own call. Don't have a strong opinion but didn't feel like adding a laundry list of roles.

Jeffrey: I don't feel strongly either.

Yves: There shouldn't be any priority. List shouldn't be ordered.

Jeffrey: Take it up again.

### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin

Sarven: Didn't get a change to reflect on comments, so don't want to spend time on it.  I don't know that this was c ontentious.

Jeffrey: YOu suggested some changes, e.g. talking about distinction between 1p and 3p and you didn't like that it was subjective, whereas I thought that was a feature.  A few other points.

Sarven: Loosely speaking, it was because that subjective view or where the boundaries being unclear that might make it difficult to make a recommendation on something should be. Maybe there is a technique to making recommendations with that fuzzineess in the concept, but we usually provide concrete examples.  Address bar/padlock.  Those are concrete.  And there is a point of reference that we say is part of 1p vs. 3p  For me when I read it, that type of clarity is useful.  Without it, what would reader take away from reading?

Jeffrey: The padlock is not good, because browsers don't show that.  Address bar I added as an example.  The key question is what the users experience and expect.  I don't think we should specify the UI that makes that difference, but instead say that what the experience is.  Is that not clear enough or do you disagree?

Sarven: That's a good approach.  Don't disagree.  How does a user distinguish.

Jeffrey: We can't be sure how users will distinguish things. Address bar is a good example.  But applications could come up with a different way, that might not be automatically wrong.

Sarvan: I see the change that you integrated, that might be a good direction.  I will read and response to the other notes.

Jeffrey: Were some other potential disagreements too.

### [user-agents#28: Add loyalty guidance for facilitating users switching UAs](https://github.com/w3ctag/user-agents/pull/28) - @csarven, @csarven

Jeffrey: This was something about users switching UAs.  And who facilitates that.  You said "not obstruct", which is fine with me.

Sarven: I updated based on Martin's and Jeffrey's suggestions. Xiaocheng made a suggestion, but I took Jeffrey's tweak to his wording. Martin, does this work for you?

Martin: Think your general sentiment is right, but there's a challenging practical matter. E.g. blocking access to user data. "must not block access to ... " ungrammatical.

Martin: Don't know what identity information is. Passwords get interesting. E.g. passkey portability is a big sticking point. Expectation that passkeys are stored in a TPM or non-portable storage. Not trivial to get a passkey from 1 browser to another. Credentials are difficult.

Jeffrey: Apple's PK seems to coming along in the right direction.

Martin: Then it's more than not obstructing. 

Jeffrey: Could argue putting it in a TPM is obstruction (even if that was a core part of the design of the feature) so by facilitating transfer they're undoing that obstruction. Comfortable with Sarven's wording, or with an adjustment.

Martin: Sarven's version seems compact so may be hard to fiddle with it.

Sarven: "identity" was "users can sign in" or credit cards or addresses, which go into form fields.

Jeffrey: So autofill.

Sarven: Thinking about how users can port that. Wasn't thinking about anything more complicated than usernames+passwords.

Martin: But it's gotten more complicated. Some websites don't even have passwords anymore. Great if you belive in passkeys, but leads to lockin. Maybe Jeffrey's finagling is the right way to think about it: they put up an obstacle and then tore it down. Don't know that Apple's thing will get the adoption.

Jeffrey: It's a FIDO standard, but you're right that we'll see if it gets adoption.

Martin: It's also about dealing with the UX problem of having multiple passkey stores, and ensuring that cross-device syncing is available.

Jeffrey: Sounds like we want a sentence on passkey, and some grammatical, and after that merge.

### [explainer-explainer#33: Add internationalization to the list of considerations.](https://github.com/w3ctag/explainer-explainer/pull/33) - @jyasskin

Jeffrey: I suspect this is fine but need an approval.

Sarven: Seems fine.

Jeffrey: I will merge.

### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin

### [design-principles#588: Rewrite the "removing features" section, incorporating "Support Existing Content" from the HTTP Design Principles](https://github.com/w3ctag/design-principles/pull/588) - @jyasskin

Jeffrey: Will revisit.

Design Reviews

### [design-reviews#1150: [wg/json-ld] JSON-LD Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1150) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1150) - @csarven

Jeffrey: The only point I know of where we disagree is whether we ask the WG to discuss the distinction between JSON and JSON-LD, whether we ask they do not, or we do nothing, or we note that the TAG disagrees.  How do people feel?

Martin: I raised this because it's mentioned in the charter. By doing so, they did themselves a disserrvice because the spec is good on this point. I'd suggest they duck the issue. The work they're doing has done a good job.

https://www.w3.org/TR/2020/REC-json-ld11-20200716/#interpreting-json-as-json-ld

Jeffrey: Missing something in spec that says "here is how you decide to use this instead of JSON".

Sarven: This is where I'm not sure that the charter needs to address this.  I like the idea about guidance, if they want to incorporate that into the spec or other documentation, but from the point of whether they need to make the case for JSON-LD at this point.  EIther that case was already made, starting from incubation, etc...  Lots of stuff already uses it.  Don't need to rejustify JSON-LD and its existence.  Maybe that guidance can be highlighted in this next spec version, that's fine.

Jeffrey: Fracture was mentioned in the review request.  VC split into two because of this JSON vs -LD "split".  I will probably make a comment as an AC rep about this; the fact that it has split a working group makes it our concern.  That's why it should be in the charter.  Not just because it exists, but they should document what should cause someone to use JSON or -LD in their work. 

Sarven: Does the content/paragraph capture the recommendation we are trying to make?

Jeffrey: Sarven is saying that they should clarify.  I'm saying that it should be in scope.  The question is what should the TAG recommend they do.

Sarven: Does this explain why JSON-LD exists?

Martin: Question is, given an application, how would you decide that JSON-LD is the right choice, as opopsed to raw JSON. What's the processing model? All those questions need to be more thoroughly addressed in an application spec. Section 6.1 discusses how to treat JSON as JSON-LD.

Jeffrey: that question is that one I'd suggest they try to answer in their spec.  They say that if you have linked data here is how you serialize that in JSON.  That's not the use case that JSON-LD claims.  Maybe consider the new use case that has appeared.

Sarven: It would be a good service to the community to include that in the spec.  THen other people can use that in their work.  To eliminate or elevate disputes.  I'm OK with that.  It's clear enough that we can .  WIthin what we were thinking.  Guidance to that extent is fine.  I was more worried about justification.

Sarven: Would like to draft that.  Do we need approval of that sentence.  Was planning to post already.

Jeffrey: Would like to double-check, but feel like just the two of us are the only ones who need to approve it.

### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1041) - @martinthomson, @jyasskin, @csarven

Martin: Mozilla looked. Freddy Braun decided he doesn't like it, because it doesn't provide the same capabilities as the other SRI. Extrapolating, maybe calling it SRI is a mistake because it promises properties that aren't at all the same. It's a new thing. What you really want might be message signatures, which covers metadata. Not sure that's what the authors have in mind. Freddy was concerned about the potential for misrepresentation. It's really not an integrity mechanism. Worries about how you deploy this sensibly.

Jeffrey: Your point about naming it something different is a solid thing for the TAG to endorse.

Martin: Wait for Freddy to post publicly.

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1092) - @martinthomson, @jyasskin, @marcoscaceres, @toreini

## Breakout C (Europe / Asia / Australia) - [2025-10-02](https://www.timeanddate.com/worldclock/converter.html?iso=20251002T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Christian, Marcos, Yves, Xiaocheng, Matthew, Ehsan, Sarven
  
Regrets: Max, Hadley, Lola, Martin

Scribe: Christian

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Matthew: Don’t think we decided to do anything with this yet. Lola added some sub issues.
Sarven: Don’t think there was any progress, let’s skip.
(Skipped)

### [design-principles#585: Clarify when details should go on events vs targets](https://github.com/w3ctag/design-principles/pull/585) - @jakearchibald

Matthew: This is a PR we just got from Jake, anyone seen this?
… Martin accepted it, Xiaocheng has a review request.
… Martin asked for a few changes, looks like it’s still pending.
Xiaocheng: We are waiting for edits.

### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://github.com/w3ctag/design-reviews/issues/1140) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1140) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Matthew: Proponents have asked for a full TAG review.
Marcos: Since Martin and Lola are not here, is anyone interested?
Matthew: Marcos, anything specific you would like to add?
Marcos: Worried about the duplicative nature, and the element does two roles: Permission and location updates.
… Do we want these elements to have the same behavior as the Geolocation API or not?
… Or should it just use the permissions? Cool thing is that they would participate in forms submission.
… At the same time, also somewhat unneccessary.
… Should they just be permission enabling things?
… How dynamic is it? How would you style it? A bunch of things that is not yet clear.
Matthew: It would be great if we collect the points that we already have consensus on.
… Can you draft a comment in the private brainstorming?
… And if we get that agreed during the rest of this week, we could post this?
Marcos: Yes.

### [design-reviews#1142: Incubation: FormControlRange - Live ranges for <input> and <textarea>](https://github.com/w3ctag/design-reviews/issues/1142) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1142) - @csarven, @matatk

Matthew: Think we are in agreement that this is a good idea. Sarven wrote a comment, Xiaocheng wrote good points. Even if they think there are no accessbility considerations, there should be a section that they thought about it. Should be very easy for them to add that. Think the images in their explainer are broken. Sounds like we could just add those two or three things to Sarven’s comment.
Sarven: Agree, but minor comment: I don’t see broken images.
Matthew: I see that under point 2 user facing problem, but can file this as a separate comment.
(Discussion about potential network problem, not everyone has this problem.)
Matthew: Okay, let’s ignore this for now.
Sarven: Can post the comment.
Matthew: Sounds good, and mark the issue as satisfied.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://github.com/w3ctag/design-reviews/issues/1136) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1136) - @toreini, @lolaodelola

Matthew: Any updates?
Ehsan: Have read the explainer, preparing review on it, hope to have the review by next week.
… Don’t have any critical objections up until now.
… Maybe next week we can discuss it in more detail.
Matthew: Think we discussed this during the F2F in HK,  there was confusion about a potential duplicate between issue #1145 vs. #1136. Let’s discuss this next week.

### [design-reviews#1139: WG Revision: Dubbing and Audio description Profiles of TTML2 (for 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/1139) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1139) - @matatk

Matthew: This is one of the issue where … and Hadley are the experts. They have given us a list of significant changes. Don’t see those changes as architecturally significant. APA is reviewing this from an accessibility perspective.
… My view on this so far is that I don’t see anything of significance related to architecture.
… Are people happy with this?
… Sounds like we are happy to close this as satisfied. Will put a comment to the private brainstorming. If I don’t hear anything else, I would post it next week.

### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Matthew: We do have some comments from Martin and Jeffrey. What they are proposing is that we ask some questions to get on the same page about it. There are a lot things that Martin has raised. Marcos, have you seen Martin’s feedback in the private brainstorming? Can we phrase this as a series of questions? Martin would be well placed to do this. Seems like it is worth to ask them publicly.
Marcos: I don’t see anything particularly problematic. Some things seem to need clarification from the Working Group.
Matthew: Seems like we should give Martin and Jeffrey a chance to put the questions across once they are available.

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1128) - @toreini

Ehsan: I posted my initial draft comment, waiting for Jeffrey to comment on it. No update for three weeks.
Matthew: I think we should ping Jeffrey.
Ehsan: Main issue with this is that there are some issues, at this stage the explainer is messy in many ways. Maybe that’s the first thing I want to raise, if they can properly edit the explainer. For the other concerns, I will ping Jeffrey.
Matthew: Think we can do something with this, as you have more detailed technical points. We should get them something. Sympathetic about your comment regarding the explainer. We could hint to the explainer explainer. If there are specific suggestions, we can support them to improve it. Can you draft it as a private comment? We should be able to get thumbs-ups quicky. We should also apologize for the delay.
Ehsan: I like that idea.

### [user-agents#25: Add Audience section](https://github.com/w3ctag/user-agents/pull/25) - @csarven, @marcoscaceres

Matthew: What is the status of this?
Sarven: Discussed this yesterday in breakout B. We are a bit in disagreement, not sure about the real target. Impacts the language. That’s why we didn’t resolve it yesterday.
Matthew: Looks like there are two questions: 1) The order of the audiences, 2) the name of the audiences. Marcos made concrete suggestions for alternative phrasings. Can we have a discussion about whether these phrasings work?
Sarven: Doesn’t quite work for me, but I can walk through quickly. Main one is that technical authors is getting changed to spec writers. But not everyone is neccessarily writing a spec.
… Pushback is also on web developers. As it is written, this document is not something that developers would read and could implement it. It may be interesting information, but that could be true for any other kind of document.
Matthew: Does that make sense for you, Marcos?
Marcos: Are web developers listed in some of the principles that we have? My approach for writing specs is writing them for implementers, but with a heavy focus on web developers. Don’t disagree with what Sarven is saying, but at the same time, the assumption is that web developers would be looking at the spec. Don’t have a strong opinion. Like acknowledging web developers. The platform is made for them.
Matthew: There’s a subset of the design principles relevant for web developers. Is that not the case for the user agents document? Could a subset be included for web developers? Or is there a primary audience?
Sarven: The text is not particularly useful for web developers. The primary audience is these three. If we had more content that would be relevant for developers, we could add it. Don’t think we want this document to be targeted at any end user.
Matthew: Sarven, I think we could discuss the order of the audiences, and the exact naming of the roles. I wonder if Yves could tell us what the house style is for referring to those people.
Sarven: Completly open to the order, I think you suggested that, don’t have a strong opinion on the order.
Yves: Don’t think we need to have a specific order. Was wondering if adding this paragraph is neccessary at all.
… As long as we write it for the audiences we want to reach, that should be enough.
Sarven: Cool with either way, the list is unordered. User agent developers are probably the main target here. Think there’s a difference between what we have and the Priority of Constituencies. We could put it in rough order.
Marcos: Biased as an implementer and a spec author. Sarven’s point about documentation writers is valid. It details why we developed this document and how the language is focused. I think this is quite important why we are writing in a particular way. This is not in the level that, say, lawmakers require the document to be in. Looking at the history why we defined this: When we use RFC verbs, they need to apply to a product.
Matthew: Wonder if we do have some intro here, we could also highlight that the web is for everyone, so we could link to the Priority of Constituencies. Let’s move on and we come back to this.

### [design-reviews#1135: Incubation: Inline Integrity](https://github.com/w3ctag/design-reviews/issues/1135) [History](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/issues/1135) - @toreini

Ehsan: Reviewed it, no major issue. Posted by initial draft review. Jeffrey got back to me with feedback. In general, seemed fine with the overall feedback. Will prepare a draft final review.

### [design-reviews-private-brainstorming#211: Draft WebMCP review](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/211) - @xiaochengh

Xiaocheng: They still seem to be rapidly iterating on this. Want to make sure we send out our review before it is too late. Drafted a response to be posted to the WebML comment. I don’t fully understand Jeffrey’s comment, can somebody have a look?
Matthew: Like your comment, agree that it’s early days. Jeffrey is talking about the fact that this could be declarative. Anyone else have particular thoughts on this?
Christian: I'm able and happy to look at this - can we come back to it next week?
Matthew: Ok. We talked about the context, e.g. for email fields, and from an accessibility perspective. But it doesn’t sound there’s anything particular we could do with this.

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

Matthew: No real update from my side.

### [design-reviews#144: WG Revision: Geolocation](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/1144)

Marcos: This issue is unassigned, can somebody have a look at it? Should be a quick review.
Christian: I can do it.
Marcos: Ok, let’s stay in the call.

[Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Plenary Session - None

