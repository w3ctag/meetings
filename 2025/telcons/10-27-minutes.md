# W3C TAG Minutes - Week of 27 Oct 2025

## Breakout A (Asia / Australia / West America) - [2025-10-28](https://www.timeanddate.com/worldclock/converter.html?iso=20251028T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Marcos, Max, Martin

Regrets:
    
Scribe: Mostly Jeffrey

### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Marcos: Will do a pass this week.

### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin

Jeffrey: Will do a pass this week.

### [design-principles#584: Replace asking for users for consent with designing for user intent](https://github.com/w3ctag/design-principles/pull/584) - martin, jeffrey, marcos

Martin approves.

Marcos: Don't remember having any objections. Merging is fine.

Merged

### [design-reviews#1093: Prompt API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1093) ([Github](https://github.com/w3ctag/design-reviews/issues/1093)) - @martinthomson, @jyasskin, @marcoscaceres

Jeffrey: Marcos wrote a draft; I left a bunch of comments. Christian offered to draft a new comment that might get consensus but hasn't written it yet.

Marcos: I think pretty firmly that the local option shouldn't be exposed at all, since it has a bunch of issues. Fine if a browser downloads a local model.  Memory management dumping on developers. The overall utility of the API. Fine to explore to see if these things are useful.

Martin: Where we disagree is the relative utility of local vs remote. Marcos said local isn't going to cut it, but is that a question of immaturity or a genuine constraint? Questions around sourcing compute in the cloud, and who's responsible for that? Would be sized to their needs instead of generic needs. 

Marcos: Should be an implementation detail whether it's doing it locally or not.

Jeffrey: Doing it locally should be allowed, but that might require a download, and the time that takes needs to be exposed to the developer.

Martin: But the language complexity is a bit of a problem.

Jeffrey: Yes.

Martin: If we accept this general approach, then having websites be aware of the capabilities of the model does create a privacy risk. If the model is there to serve the user, then the language nonsense is probably a distraction, because the user will understand some number of languages, and their model will speak their languages. Exposing the capabilities ("my model speaks only English") that's fingerprinting. If the web page is in English, then it gets an English model or no model at all.

Jeffrey: I think that's totally plausible. 

Martin: Then we probably lose out on multilingual models, without some additional steps. And that gets rid of fingerprinting concerns.

Marcos: Same as text-to-speech: I select the languages to install. 

Jeffrey: Could be a translation step separately from the Prompt model.

Marcos: Choice of the UA what to provide. With Apple Intelligence, you'll just pipe it through ChatGPT, which speaks all languages. Customization by the user, followed by "I don't speak that language". Or it downloads the thing, and it's handled by the UA at that point.

Jeffrey: Martin's point is that allowing customization or allowing downloads adds to fingerprinting risk. The time it takes to download is observable. Delays would also be a bad experience. I think what we could say on that point is we are skeptical or opposed to having a bunch of separate pieces that get downloaded individually. The model should be for the user agent version, or for the websites (current) language. The site doesn't get to choose.  You just the the bit that sells whether the model is present or not.  But that might be an acceptable amount of leakage, whereas langauges might not be OK.
...Marcos believes that we should not have the local option.

Marcos: Just don't expose where the model lives.  That's an internal detail.

Jeffrey: I think we need to expose the state in order to have a good user experience.  OK if we say that we are divided.

Martin: I think it's unavoidable that it leaks, if it requires a setup phase. Whatever the setup phase looks like, it'll leak.

Marcos: At home I get 120MB/s, so I don't care about the time. It'll take 10s. Not for the developer to make the decision for me.

Martin: On terminology, think we can just provide feedback. Non-determinism, and hallucinations, and quality are all together. Is that just an acceptable part of doing LLM stuff.

Jeffrey: I think it's yet to be seen if that's acceptable.

Martin: So we want the experiment to tell us whether 

Jeffrey: Browsers are planning to ship before the experiment results.  I'm reluctantly comfortable with that because it can be backed out.  We make the local option say that it's not available.  We would expect that a decent fraction of people are in that state anyway.  So we move all users to that state if we retract.

Martin: Thesis is that sites won't be able to depend on this being present?

Jeffrey: Yes.

Marcos: I don't know what kind of experiences people will try to build with this.

Martin: If it's a core part of the experience, and you don't have the LLM, do you get get "computer says no"?

Marcos: Could be UI design, or anything.

Max: Even without this API, the developer can use an LLM, so what's the benefit from this API?

Martin: Benefit is that someone else pays for compute. Don't have to pay a cloud providerr for compute; instead users pay.

Max: So model will be in the device?

Martin: That's one option, but it could also be in the cloud, and maybe the user pays, possibly with personal data.

Max: Makes sense for local processing and to use the models in the device.

Martin: That's my biggest concern with this API, that it offloads cost to the users.

Jeffrey: We could ask if there's a plan to make sure that's fair.

Martin: Seems like the opposite: people with expensive computers will get the privacy benefits, but others will have to pay cloud providers.

Marcos: Third tier: people with a paid ChatGPT account attached to the OS. If the API is abused, it abuses the paid account.

Jeffrey: The concrete comment is that it doesn't have any constraints on the use of a paid user-agent-provided model.  There is no way to ensure that random sites don't exhaust limits.  Flaw in the proposal.
...Maybe we need to put a comment out with all the obvious flaws so that they can fix stuff.  We don't need a position right away.

Martin: local vs remote, and who pays for compute are big

TODO: Draft a comment.


### [design-reviews#1092: Web Authentication Immediate Mediation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1092) ([Github](https://github.com/w3ctag/design-reviews/issues/1092)) - @martinthomson, @jyasskin, @marcoscaceres, @toreini

Jeffrey: Think we left this with the idea that users were opting in by turning on passkey sync, and could opt back out by clearing storage.

Martin: Passkey sync is now a thing, and it happens at a level of the OS that you don't necessarily have access to. Applications are installed that sync passkeys. So can't necessarily bank on that. If that's the only thing this is trying to solve, maybe people can click one more time to say it's ok, and we don't need this feature at all?

Jeffrey: Maybe that's the core of a comment? To ask what the opt-in is, and if there isn't one, is the feature important enough that it can't have a second click?

Martin: In the cookie clearing example, you pay the extra click. Scenario they're optimizing is that you have a credential on two devices, and you're using the second device, and have never used it with that site before. You have a credential; they want to test that it's there; maybe you don't want that connection to be made. DKG says that the world we live in where people keep asking for identity, is not a good world. Filter bubble shrinks to become a cage.

Jeffrey: "Second click" reveals the same information, so it doesn't seem to help.

Martin: This feature is about a shortcut experience where the first button logs in, but without 'immediate' you would send them to an intermediate page to select the login type.

Jeffrey: I'm still having trouble seeing why this is that important.

Martin: Distracted in terms of "can we unify the whole login experience".

Jeffrey: I think they have an implementation that shows all the login types in the 'immediate' dialog. Would it help for them to present that in this explainer?

Martin: Think it wouldn't help.

Jeffrey: My question is, once they have everything in the one dialog, why not just provide that dialog unconditionally, and have the user log in there? I think I'm convinced. Martin, want to draft a position? [Martin already had a position drafted.] I will re-review that, and propose any tweaks.


### [design-reviews#1140: `<geolocation>` element (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1140) ([Github](https://github.com/w3ctag/design-reviews/issues/1140)) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Jeffrey: They have a specification now: https://wicg.github.io/PEPC/permission-elements.html#geolocation-element

Marcos: Overall question of using this design for powerful features.

Martin: Team wants to ensure the element is on-screen when the person gives permission. Don't think it's sufficient, and they're building it to link into IntersectionObserver. Can't be activated off-screen.

Marcos: Need to check they're re-using geolocation machinery.

Martin: Yes, they are.

Jeffrey: Marcos had mentioned that IntersectionObserver isn't fleshed out enough, and would need to be finished to be used here.

Martin: Don't think it's necessary: just the fact that you click something on the page helps a lot.

Jeffrey: UAs might need to differ here. If rejections are sticky, UA might want to be confident the user saw something in particular. But if rejections aren't sticky, UA could accept many more "clicks". Do we have opinions on how?

Marcos: Amount of variance you can do might be huge. There's generated content from the element itself. Does that count as occlusion? Occlusion, style limitations, are a very hard problem.

Jeffrey: Does it work for that to be UA-defined?

Marcos: Should be ok.

Martin: Have to implement it to be sure. What it looks like on the screen, how user interactions work in your particular thing. It won't be done until there are 3-4 implementations that each take a different path. Uncomfortable how much it integrates with the permission element. 

Jeffrey: So you want it split out more so it's clear we can delete the `<permission>` element?

Martin+Marcos: yes.

Martin: Do think the internal state is potentially re-usable. Not sure you'd do it to start with. 

Jeffrey: So we advise them to wait on that until they define at least the <usermedia> element, and probably the third instance.

Jeffrey: I can draft a comment: 1) Generally support the direction. 2) Be sure this matches other form elements. 3) Allow UAs to vary on how much they restrict style and observability. 4) Define <geolocation> as its own thing, without trying to extract out "common" parts.

Martin: How does error stuff interact with form validation?

Marcos: I looked it up a couple weeks ago; don't remember the details. If you get an error, it's not validated.

Martin: Does it have :valid and :invalid CSS?

Marcos: Yes, that'll be set as well.

Jeffrey: No point in bringing up detailed validation of particular locations until someone proposes it.


## Breakout B (America / Europe) - [2025-10-29](https://www.timeanddate.com/worldclock/converter.html?iso=20251029T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Lola, Matthew, Christian, Christian

Regrets: Hadley
    
Scribe: Matthew

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Lola: Any new issues?

Jeffrey: I sent the PR to unblock publishing it as a Draft Note. Under reiew.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Matthew: Will add TPAC to TAG schedule and get prepared.

### [societal-impact-questionnaire#24: Misuse example](https://github.com/w3ctag/societal-impact-questionnaire/pull/24) - @lolaodelola

Lola: Christian posted an example. Under review. LGTM. In the Compute Pressure API spec, do they say how the API could be used to join user identities across sites.

Jeffrey: Doesn't go into the details, but the basics are that you spin JS to create CPU load (or not) and use that to send a signal to the other tab. You could sync the clocks and pull the signal out of the background noise.

Lola: I think we should add a sentence about the how. What lead the spec authors to think this could be done. The API doesn't have anything (on the surface) to do with tracking.

Jeffrey: Link to https://www.w3.org/TR/compute-pressure/#cross-site-covert-channel?

Lola: Key point is to show an example where a misuse was possible, and the spec authors put in mitigations to address it. See conversation from Sarven about in-spec vs out-of-spec misuse.

Jeffrey: I don't follow Sarven's distinction.

Lola: We spoke about this in C last week (https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/10-20-minutes.md#societal-impact-questionnaire24-misuse-example---lolaodelola-csarven-christianliebel-1; I'm unclear too. E.g. If I go on social media site and share info with them per the contract I have with them, and then they use the info outside of that (e.g. they use my image in an advertising campaign) then that doesn't seem a concern relating to web technologies/APIs. I don't think an API should caution against that.

Jeffrey: I think specs assume that once an API reveals some info, the party can use it in any way. I don't see the need to distinguish between the two uses - the spec should be concerned with limiting the transfer of information, rather than what happens when it escapes. We worry about when it escapes; we lose control; then harm can be caused.

E.g. the cookie spec talks about how to share information in certain contexts. When information gets to a third party, we assume that it can be used in any way. If the spec said you MUST NOT misuse that info, there's nothing the spec can do to enforce that.

Lola: Should we ask spec authors to think about the information escaping? Or that it wouldn't make sense becuase once they have the data they can do anything with it.

Jeffrey: Societal considerations should think about what happens when the other side gets the info - what uses coudl it be put to? Almost everything we are worried about is the out-of-spec usses of the info.

Lola: In the case of 3pc the misuse of 3pc to track users... it's not the spec author's responsibility to consider that the tech could be used to cause e.g. the Cambridge Analytica scandal specifically, rather that it can be used to track people in general.

Jeffrey: I think I disagree... that is a consequence of tracking. So things like this are possible (we can't predict it all) but it's clear that tracking can be used to target groups for political purposes, and that's one of the considerations that go into the design of the technology.

Lola: I do agree with that but it seems there is a role for regulators here. that they should define rules about hw data about the citizenship are used. E.g. 3pc could've been used in a different way. It's responsibility of the government in power to say what is acceptable use of data is.

Jeffrey: True in an ideal world but we have to accept some responsibility for when technology moves faster than what regulators can keep up with - which it did in this case. Maybe we should note that regulators need to do something before the tech can be safely deployed.

### [user-agents#28: Add loyalty guidance for facilitating users switching UAs](https://github.com/w3ctag/user-agents/pull/28) - @csarven

Jeffrey: Sarven's done all that people asked - think we can merge it. Marcos and I have approved.

Lola: OK.

### [design-principles#588: Rewrite the "removing features" section, incorporating "Support Existing Content" from the HTTP Design Principles](https://github.com/w3ctag/design-principles/pull/588) - @jyasskin, @csarven, @lolaodelola

Merged

### [societal-impact-questionnaire#26: Exclusion Example](https://github.com/w3ctag/societal-impact-questionnaire/pull/26) - @lolaodelola, @csarven, @jyasskin

Lola: ACK Matthew's comment

### [societal-impact-questionnaire#25: Make Tristan former editor](https://github.com/w3ctag/societal-impact-questionnaire/pull/25) - @lolaodelola, @hadleybeeman

Will be merged

### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin, @lolaodelola, @csarven

Jeffrey: I think this is with Sarven (comments from me, and Xiaocheng).

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Jeffrey: We shoud clarify regarding the polarity mismatch between title and explainer.

Lola: We should decline to review when there isn't an Explainer (document) (rather there is just a comment). Or we should put them in a holding pattern.

Jeffrey: Sometimes a comment is appropriate when it's a small change. But this is above that threshold.

Lola: Martin proposed adding something to the process about AI. Check out Slack.

Matthew: Can we ask for more concrete examples (maybe there's a reason why they can't)? Think that would help a lot. Did appreciate the case they raised about apps within other apps, and signing in.

Lola: We should ask, yes. Leave it to them to let us know if they can't.

Jeffrey: +1 and this is a reason why they should write an explainer rather than comments. I think Ehsan is coming up with attacks based on the 'backwards' understanding of what they're doing (because their explainer had the order backwards). We should write our comments with the threat model they have in mind.

### [design-reviews#1147: WG New Spec: FedCM—Support Structured JSON Responses from IdPs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1147) ([Github](https://github.com/w3ctag/design-reviews/issues/1147)) - @lolaodelola

closed

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Jeffrey: needs to wait for plenaries.

Previous discussion with the proponents was in https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/07-28-minutes.md#design-reviews1058-the-interesttarget-attribute---matatk-xiaochengh

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew asked for more info

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Jeffrey: Matthew and I are on the hook to write a comment.

Matthew: I will have a go. Don't think we need more discussion.

### [design-reviews#1015: Payment link type in HTML](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1015) ([Github](https://github.com/w3ctag/design-reviews/issues/1015)) - @jyasskin, @torgo, @csarven, @maxpassion

Scheduled for discussion at TPAC.

Need to put in TPAC scheduling repo

## Breakout C (Europe / Asia / Australia) - [2025-10-30](https://www.timeanddate.com/worldclock/converter.html?iso=20251030T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Lola, Martin, Matthew, Ehsan, Christian, Marcos

Scribe: Martin

### [design-reviews#1138: [wg/webextensions] Web Extensions Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1138) ([Github](https://github.com/w3ctag/design-reviews/issues/1138)) - @csarven, @matatk, @toreini, @christianliebel

Christian: we need to ask Sarven. what he wanted to address... he's reopened it. but it's fine from my point of view. 
Action on Christian to ping Sarven.

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

Matthew: I was supposed to close this.  Will do so.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: This we can skip.  Parent of two sub-issues we've already covered.  Leave it because there are going to be more sub-issues coming.  I will remove the agenda+ label.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: Skip this too.  We don't need this on the agenda next week.  These meta issues exist to ensure that we are thinking about documents in our normal agenda planning.  We have enough issues open on these documents right now.

Hadley: We're using this to decide to do nothing more, good.


### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @lolaodelola

Lola: In the wrong breakout.  Jeffrey did write a review for them and they have thanked him for that, opened issues to discuss the points in the review.  They will come back to us.  I don't know if we want to wait for them or we can close this and ask them to reopen when they are done.

Hadley: Is this a change of status review?

Lola: I don't know.  Jeffrey's review was pretty thorough, so even if it is an approval, there is enough here to require them to address that before they ask again.  Not like some of the simpler reviews lately.

Hadley: Why don't we use the "pending external feedback" label for now.  Keep it there for at least another week.  I'd be surprised if they go cold, but we can close it if they do.

Lola: I will reread comments.  They have lots of issues, they might not get them resolved in a week.  See if a week is reasonable.  Especially given TPAC.

Hadley: Maybe you should just ask when they expect to be ready.  I expect them to know.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

Skipped, since they aren't here.

### [design-reviews#1140: `<geolocation>` element (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1140) ([Github](https://github.com/w3ctag/design-reviews/issues/1140)) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Martin: I drafted a comment. General view is positive, worth doing. it's a direction we'd like to see them continue to explore, but there is feedback about finishing things. Jeffrey has agreed. Lola, can you look at it?

Lola: ok.

Martin: if it does, poke me and I'll post it. Am OK with others posting instead. Mark as validated. 

### [design-reviews#1158: ViewTransitions: waitUntil() method](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1158) ([Github](https://github.com/w3ctag/design-reviews/issues/1158)) - @lolaodelola

Lola: I haven't looked at this yet.

Christian: I can help. I'll review it. 

Christian: This is probably not horizontal review, but we don't need to stand on ceremony.

Hadley: Drop a note to let them know that.

### [design-reviews#1149: [ig/webai] Web&AI Interest Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1149) ([Github](https://github.com/w3ctag/design-reviews/issues/1149)) - @christianliebel

Christian: Seems fine even though we have CG and WG in the general area. The WG chair is fine with this.

Martin: This seems like it could be a missed opportunity in terms of dealing with the agentic browsing threat model.  Having something in the charter more explicitly would be good.

Hadley: Do we need to send this to somone else?

Ehsan: It's a bit fuzzy, because that problem Martin identified is a WebML thing as well.  How are they planning to resolve that intersection.  The focus is very much on agents, is that right?  

Martin: This work on Ethical ML is very general and not web-specifics.  Should be ruthless about scope because we don't want to be the 500th org doing general AI ethics.

Ehsan: Agree that this shouldn't do general ethics.

Hadley: Mostly agree, but don't think that agentic AI is the entirely of what the group might spend its time on.  [Autonomy](https://www.w3.org/TR/webmachinelearning-ethics/#autonomy) is potentially a topic that the W3C could constructively engage with, but could be more narrowly focused.  If I were chairing this group, I would rule things out of scope to maintain focus.

... lots of back and forth that couldn't be captured.

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

Sarven isn't here.

### [design-reviews#1160: WG New Spec: RDF 1.2 Semantics](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1160) ([Github](https://github.com/w3ctag/design-reviews/issues/1160)) - @csarven

Sarven isn't here.

### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven

Sarven isn't here.

### [design-reviews#1146: Incubation: Proofreader API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1146) ([Github](https://github.com/w3ctag/design-reviews/issues/1146)) - @matatk, @toreini, @christianliebel

Matthew: We are not the experts on these sorts of tools, but we might know people who are.
So much fail in the UK.

Christian: Not a domain expert, but it looks fine.  Check with domain experts.  Shares a lot of features with other AI-related APIs, so it is somewhat blocked by those discussions.

Hadley: i18n we have some choices to make.  We could ask the i18n folks to look into this.  They can be helpful, but it is a big ask of them.  Another option is we could go to a former TAG member with expertise if they want to help out.  No one comes to mind.  Sangwhan has an interest in i18n because we were messing with his daily life, more than a professional interest.  We could say to the group what you said and leave it at that.

Christian: I would prefer to wait on the Prompt API response.  A lot of the feedback there applies to Proofreading, especially the model download/initialization part.  We should be open about that.

Hadley: Pending external feedback?

Christian: fine.

Matthew wanted to say something about this as well, but he was having connectivity issues.

Matthew: I put in slack that Ehsan has a comment coming, but that's compatible with the above resolution.

### [design-reviews#1119: Digital Credentials API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1119) ([Github](https://github.com/w3ctag/design-reviews/issues/1119)) - @martinthomson, @matatk, @toreini, @lolaodelola

Marcos: Last time we discussed it, Martin had some feedback.  Have had the age verification[sic] workshop as well.  Enough there to provide feedback.

Marcos is working from a beach club

...GIven the workshop and given that the privacy/security aspects with some technical details are not going to impact the review.  Ideally before TPAC.

Lola: Is this to say that the stuff that is required for this to be implementable is in the spec?

Marcos: It's not all there.  Particularly the issuance stuff, but the issuance depends a lot on the formats, which are not in the spec.  Those are done by different SDOs.  Not necessary to look into those.  ISO documents are *redacted*.

Martin: I made some comments privately.  Someone can take those.

Lola: Will attempt to do that.  Will check with others.

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1128) ([Github](https://github.com/w3ctag/design-reviews/issues/1128)) - @toreini

[Ehsan is having connectivity problems]

### [design-reviews#1041: Signature-Based Integrity.](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1041) ([Github](https://github.com/w3ctag/design-reviews/issues/1041)) - @martinthomson, @csarven

Martin: there is some good discussion going on in the spec issues, around some of the things I would've recommended we put in a reivew. I was going to suggest we leave that for now. This may be worth me going to the webappsec session at TPAC, and have a discussion there. I'm increasingly of the view that this is too sharp an instrument to just be lying around, and would encourage the TAG to say somewhat negative things about it. It's not totally harmful, but also not as useful as it seems at first. People think they are getting certain security properties out of this, and they are not. 

Sarven isn't here right now. 

Hadley: do they have any deadlines?

Martin: no, it looks like an early review. 

### Meeting times

Lola : reminds everyone that the new meeting schedule starts next week.

### Any other business 

Christian: to Marcos, I drafted a question in the github thread on Prompt API, #1093; this circles around local vs remote processing.  Would be good to have a single conversation about the Prompt API.

Marcos: We probably need to go through it together. 

[They have been left to do that.]

## Plenary Session - None
