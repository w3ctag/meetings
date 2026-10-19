# TAG Minutes — Week of 12 October 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/10-12-agenda.md).

## Pacific Breakout (Asia / Australia / West America) - [2026-10-14](https://www.timeanddate.com/worldclock/converter.html?iso=20261014T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Heather, Brian, Jeffrey, Dan

Regrets:

Scribe: Heather

#### [design-principles#621: Add new fragment directive guidance](https://github.com/w3ctag/design-principles/pull/621) - @tabatkins

Jeffrey: Fragments depend on the media type, not URL or scheme. The proposal is to define a syntax and URL for the source of the link. That's not formally how fragments work. So, not really sure what to do about this. We could suggest they try to modify SVG. The definition of the fragment comes from the media type, so they'll have to say something in SVG about what these mean. I also put something about this in the design principles text. 

Marcos: Makes sense.

Jeffrey: I will message @tabatkins tomorrow for him to review my comments to the PR. If others have time to review, that would be helpful, but that can be done async. 

#### [install-finding#2: Add section on engine fairness](https://github.com/w3ctag/install-finding/pull/2) - @christianliebel

Marcos: I haven't had a chance to look at this yet. 

Brian: This also have the phrase "the platform's default browser." Does that mean if you choose a different default browser vs the one that is the pre-installed default, does that change the intent? I think it matters. 

Jeffrey: We could say "any default browser the platform provides." Sometimes there is a default, but not always.

Dan: If I'm on Windows and I install Firefox and I set my default browser to Chrome, what would a PWA open with? We should define behavior.

Marcos: On Apple's platform, the thing that runs the installed web app is not Safari, it's its own user agent. It's a separate app using a particular web engine. 

Jeffrey: The second paragraph covers that. It should be the same browser and not the same web engine. This isn't about what Apple does but what should be done on the web. What the finding is saying is that the user should be able to pick a browser that would support the options they prefer. It shouldn't just be the operating system's decision. 

Marcos: Articulating that to users is extremely difficult. It's a flawed idea because it doesn't always make sense for an installed app to pick up ALL the aspects of the installed browser (e.g., permissions, badges, login/logout). I will have another read and see if I can suggest ways to clarify this. 

Brian: This includes "if you install something and are already logged in, you should be automatically logged in to the new PWA." Does autofill also carry across between app and browser?

Marcos: Yes, it's a functionality of the UA. 

Jeffrey: The text is trying to say the user should be able to keep the autofill from the browser they select. 

Brian: I've commented on the "we expect" language. 

Jeffrey: I think Christian was trying to avoid "should". I think it's consistent across this finding. 


#### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Marcos: I'll look at the additional comments later today. 


#### [user-agents#70: Focus only on web user agents.](https://github.com/w3ctag/user-agents/pull/70) - @jyasskin, @marcoscaceres

Brian: Will ping Dom to comment one way or the other. 

#### [install-finding#1: Add section on capability gating](https://github.com/w3ctag/install-finding/pull/1) - @christianliebel

Heather: Looks like Jeffrey approved the PR and some commits were made. is there anything else to discuss on this one?

Marcos: I think this looks fine. I am concerned about citing incubations. I will leave a comment about that. 

Brian: Incubations also are pretty early to make any solid determinations about .

#### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Brian: They have asked us to wait while Mozilla works on this with them.

Marcos: It's great that they are making changes based on feedback, but I don't think it will make any material difference to our input at this time. 

Heather: We'd be offering an early review anyway, so that should by itself be valuable. I don't think we should wait.

Dan: We can post what we have without closing it with a resolution. I think they are worried that there will be a blocking recommendation on our part, something negative that might indicate we're done with it. Maybe some of those fears can be lessened with language.

Heather: I thought we'd worked on language to indicate feedback to support incubation?

Dan: Yes, I think we're evolving the language in our response.

Brian: We should stress this is an early review, so you should expect a lot of feedback. And if/when you do come back, we hope to see these things addressed. 

Marcos: I thought we were going to publish the comment this week?

Dan: There are still a lot of comments in the doc that is still being addressed, and the question of separating out finding text on agentic browsing. It's not ready yet. 

Marcos: I'll take a look today. 

#### [design-reviews#1273: WG New Spec: VCALM v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1273) ([Github](https://github.com/w3ctag/design-reviews/issues/1273)) - @jyasskin, @hadleybeeman, @hlflanagan

Heather: I have suggested text to request more information; I don't think we're ready for a final resolution. Waiting for Jeffrey to review.

Marcos: Agree that posting questions is the reasonable next step. 

#### [design-reviews#1285: Incubation: Declarative Performance Observer](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1285) ([Github](https://github.com/w3ctag/design-reviews/issues/1285)) - @bkardell, @hlflanagan

Brian: I haven't had a chance to look at this yet.

Heather: I'd love to know if others see similarities to the concerns we had about Attribution spec. 

#### [design-reviews#1224: Incubation: Lightweight and Conditional Tracing for long animation frame timing API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1224) ([Github](https://github.com/w3ctag/design-reviews/issues/1224)) - @jyasskin, @hlflanagan, @xiaochengh

Heather: I missed seeing Jeffrey's comment on this. Does anyone have any concerns with his follow up question?

<no concerns>

#### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

Heather: I can draft something further based on mine and Jeffrey's response.

Brian: I think we're still also waiting on Matthew and Marcos.

#### Triage

https://github.com/w3ctag/design-reviews/issues/1266 - was assigned to Luke, who is out of office for another week. Should we still be reviewing this one? 

Brian: if we can't probably not the end of the world. But we can also just leave it and see what Luke says when he's back.

https://github.com/w3ctag/design-reviews/issues/1282 - no one on the call has the background knowledge for this one

https://github.com/w3ctag/design-reviews/issues/1283 - Brian will take it

https://github.com/w3ctag/design-reviews/issues/1287 - (Brian) think we should pass; CSS has done enough review on this.

https://github.com/w3ctag/design-reviews/issues/1290  - (Dan) similarly, we're not likely to come up with anything the CSS group hasn't considered on this given the time spent on it

https://github.com/w3ctag/design-reviews/issues/1291 - (Marcos) probably better left to the WG than to us; it's very specific. 

## Atlantic Breakout (America / Europe) - [2026-10-14](https://www.timeanddate.com/worldclock/converter.html?iso=20261014T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Heather, Mike, Sarven, Jeffrey, Lola, Christian, Matthew, Dan, Hadley, Brian, Yves

Regrets: Luke

Scribe: Sarven, Mike

#### [install-finding#2: Add section on engine fairness](https://github.com/w3ctag/install-finding/pull/2) - @christianliebel

Christian: Context: The finding is a draft now. It currently contains stuff on consensus on during our Vancouver F2F. There are optional sections which did not have direct consensus or which we deprioritized. This is the section on engine fairness. 1) We want OS vendors to give all browsers the same access to website installation. 2) We want OS vendors to open installed apps in the same browser that installed them. The question is whether we want to adopt this section in our finding.

Heather: We also discussed in the Pacific call (line 25). More detail need for osme things. Broadly speaking things made sense, an installed app would inherit some things but no consensus inheriting all things.

Jeffrey: I think that Marcos' concern was in the weeds. Our message here is that users should be able to choose behaviours by picking the browser. Neither should be the one true way. What's here says that. So, I think it is ready for merge, and if Marcos has a particular suggestion, we can look at that too.

Lola: Is there a middle ground where we don't have to get into the weeds but still make Marcos' point?

Jeffrey: we can list several of the options. I suggest we merge what's here and add another PR for range of options.

Lola: Sounds good. Christian?

Christian: Sounds good, I will merge it.

Lola: Findings in general: Someone was pointed at the draft finding (https://mastodon.social/@benfrancis/117429804318887432). Not really ready for public consumption. Is there a standard for a convention of some sort to do or not doing this?

Jeffrey: I was a bit uncomfortable when it was pointed out but as soon as we publish on GH people are going to find it. I think no harm was done. 

Christian: At some point we need to publish it any way. By design it is already public. Certainly easier for us if the audience is only the TAG.

Brian: Can we say "encourage to" or "the tag recommends" instead of "we expected"?

Jeffrey: https://w3ctag.github.io/install-finding/#expectations-on-providers starts with "In this section, we set out our expectations on user agent and operating system vendors." and it'd be fine with me to change that.

Lola: Sounds like no one is opposed to Brian's suggestion.

Jeffrey: Brian should send a PR.

Lola: Do we want a deadline for this?

Christian: Would like "soon". Discussed for ages. Publish it next week at plenary?

Lola: We can add to list.

#### [user-agents#66: Add an EME example of making credible commitments.](https://github.com/w3ctag/user-agents/pull/66) - @jyasskin, @hlflanagan, @npdoty, @csarven

Jeffrey: I rewrote this, I think it addresses most of the comments. People may not have reviewed but think it is ready.

Sarven: I'll review after this meeting. I'm fairly confident that, as Jeffrey said, it's in a good place to be merged.

Lola: Was there not some controversy?

Jeffery: Yes. They raised this, and I acknowledge the controversy in my response--that there was a collective bargain but also that it wasn't a violation of loyalty to attempt that bargain.

#### [user-agents#70: Focus only on web user agents.](https://github.com/w3ctag/user-agents/pull/70) - @jyasskin, @marcoscaceres

Jeffrey: I agree this is ready; it's been reviewed by a lot of people.

Lola: Sounds good. Any opposition? Hearing none...

Jeffrey: We used the term "user agents" and elaborated to "web user agents" and "general user agents" a while ago. This change refocuses the conversation on web user agents (and just acknowledges the term's meaning in other contexts).

Sarven: Yeah, I think this is good. I felt the context is clear whther it's "user agents" or "web user agents." But before we merge it, I want to be sure that no infrastructure will be broken--redirects or referencese. The moment we merge this, it's going to change the short name. I want  Yves to make sure that we're turning the right switches on (or off as the case may be).

Jeffrey: I think we're covered, there.

Sarven: Specifically, I can make the pull request, but I don'tknow when it will be merged. I want to make usre redirects are set apprpriorately.

Jeffrey: Publication will happen after the merge

Sarven: So, we can do it in parallel: merge, then have a specref pull request and cross fingers.

Jeffrey: Right. I'll merge this.

#### [societal-impact-questionnaire#44: Add example-ai-footprint](https://github.com/w3ctag/societal-impact-questionnaire/pull/44) - @csarven, @lolaodelola

Lola: I thought this needed specific review from specific people that the other PR did not need. Hidde de Vries and Marcos have reviewed. Sarven: do you know anyone else?

Sarven: Not anyone in particular, now. I think this covers the main aspect of the "AI" concern. As you said, this was split off from another pull request--there's one on machine learning and another on AI. I think it's good to be merged now

Lola: As an overview: the societal impact question about the impact on the natural environment. Sarven added an example about the footprint of AI. There's an unresolved comment: where "not every feature needs a model", the commenter talked about on-device models.

Sarven: I don't want to address that comment because I don't have sufficient data to engage. I can only link to things that are relatively authoratative/reputable. If anyone (including Marcos) has a better way to express what Marcos is getting at, provided that there is data to support it, then it will hold. Otherwise, it isn't undermining the point.

Lola: Right, I think that's right. He *does* say that "the point still stands", so I think it's fine to merge as-is.

#### [design-principles#628: Add the improve-existing principle](https://github.com/w3ctag/design-principles/pull/628) - @csarven, @jyasskin

Jeffrey: I haven't managed to review this since Sarven's last update.

Sarven: I noticed a gap, but I held it off because the changes that I made based on the changes from everyone else--the cost of forking (or when a fork is justafiable). That had to do with when you're concerned about compatibility, and at some point, you can't worry about compatibility because you need to start off fresh. Forking is justifiable when you have A and B and there is an understanding that A should no longer be maintained (e.g. HTML and XHTML, where there was an understanding that we should just stop XHTML, and it is no longer running in parallel with HTML). I can make a separate pull request on that as it is a separate part of the spec. But regarding these examples, it isn't needed.

Jeffrey: I think you're right not to pyut that extra discussion in here. If anything, we should be trying to shorten it... But yes, we can also think about what to say about forking. This patch looks generally good to me.

#### [design-reviews#1265: WG New Spec: Global Privacy Control (GPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1265) ([Github](https://github.com/w3ctag/design-reviews/issues/1265)) - @hadleybeeman, @toreini, @hlflanagan, @lolaodelola @bkardell

Brian: I see that Ehsan and Jeffrey have been having a back-and-forth. We had proposed a shorter take a few weeks ago. Debatably it was too short, but it was concise and definitely written by a human. In the end (and Jeffrey, correct me if I'm wrong), the main thing that have been added are that we believe it would make sense that user-agents add a header if added through JS--basically the three bullet points at the end of the conversation.

Hadley: I'm a bit behind, but my meta question is: how is this functionally different from Do Not Track, and are these people who need to be taken through the history? [Eats dinner]

Jeffrey: I think Ehsan's first two points were good, but his third and forth turned into the stuff at the very bottom. If Brian could merge them into his list of comments, that would be ideal

Brian: Those bullets that he sharedat the end (there are three or four)?

Jeffrey: Yes

Heather: How are we resolving this? Asking for clarification?

Brian: Through this comment

Jeffrey: In reponse to Hadley: the proponents are aware of the DNT history. But this has a law that it is directly attached to, but DNT do not.

Hadley: I saw the reference to the California law, but I didn't  know if there was actually political momentum.

Lola: Yes, there is.

Dan: The proponents could save themselves some time by mentioning this in the explainer.

Lola: I gave a talk on this topic a number of years ago.

Dan: We should recommend that they add a reference to one of the many sources explaining this.

Brian: so I'll merge my comments with the results of Jeffrey&Esan's comments. Then folks can review it, and we can post it maybe tomorrow.

Lola: The Europeans are likely finishing work after this meeting. I doubt between now and Eurasia that will happen.

Brian: Sure, I meant maybe 26 hours from now.

Lola: Do we have a resolution?

Hadley: It sounds like we're asking for clarifications

Brian: I'm satisified

Lola: I think we're asking for a couple things, but in general, we are satisified.

Matthew: I tend toward "satisified." We've raised concerns about jurisdictions, and we don't know how that's going to play out.

Brian: The main thing we came up with which is potentially a real problem (that Ibelieve Heather noticed), we comented directly on the issue. They responded and said, "we didn't think of that" and have since resolved it.

Matthew: I also agree with the advice to put the "legal teeth" in the explainer itself.

Hadley: I don't see any problems.

Jeffrey: I personally have concerns because of how tightly it's tied to US-style laws, and I think they should have allowed for preferences to be attached to other sorts of types of laws. If it were up to me, it would be "satisfied with concerns."

Hadley: That's reasonable!

Lola: I agree

Heather: That matches what I'd said in a comment. For something that's global, it's also US-specific.

Matthew: Has the approach they've taken procluded the possiblity of extending it later? I remember some conversation aboutan enum that couldn't be extended...

Brian: Their solution to extensibility is to make a different header that's very similar.

Lola: Why don't they just make THAT header?

Brian: The original Do Not Track was complicated in that regard, and I think they were trying to avoid those same complexities. I don't disagree with Jeffrey: I think more extensibility would have been better. But it does raise additional questions, and in the end, you can define a different header. Presumably, we could develop something very similar for, e.g. Europe, based on what's here. I'm okay with "satisfied with concerns"; it's what I would have preferred. The concerns are minor, but that's still appropriate.

Lola: Great. Reviewers, please try for tomorrow if possible. Otherwise next week

#### [societal-impact-questionnaire#45: Publish this document as NOTE before TPAC 2026](https://github.com/w3ctag/societal-impact-questionnaire/issues/45) - @csarven, @lolaodelola

Lola: Sarven and I would like to publish. There are one or two pull requests that need to be merged, but it's looking good for the most part. "Before TPAC" would be great, but since that's less than 2 weeks away, we recognize that might not be realistic. Any objection? Hearing none.

Sarven: Just so that we, as TAG, acknowledge potential concerns about Notes going on for years--I think it's worthwhile to think about when we can possibly say that a note is "done". The reason that may be a concern (especially for a document like this) is that society is always evolving, and different people are going to be looking at this document at different times through different lenses, e.g., the same question/concern would reveal different perspectives. It's not that the document can't continued to be improved (there's a lot of room for improvement); the proposal is a good representation of what we've been looking at in the past few years. As some of you know, it came off the work from ethical web principles, so it's fairly well-incubated. It's clearly by no means exhaustive, but it is what it is right now, so let's not write it in stone and never revisit it.  We're saying two things: it's good for a note, and it's also our intention to continue iterating.

Lola: It sounds like everyone's okay with that.

#### [design-reviews#1268: Other Spec Review: Registries developed by the Media WG](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1268) ([Github](https://github.com/w3ctag/design-reviews/issues/1268)) - @hlflanagan

Heather: This turns into a meta-question. I thougth the question about a registry was interesting. I took some time to learn how I would do such at hting, that led me to interact with ChatGPT a bit. It came up with two questions: "For the HDCP registry, are all of the semantics needed by getStatusForPolicy()—including any version ordering or compatibility assumptions—fully defined outside the registry? For registries that permit an underlying specification not to be public, can an independent implementation nevertheless implement all Web-facing behavior of the registered entry solely from publicly available specifications?"

Heather: I think they're good questions, but they came from an LLm, so I'm not sure what to do with them,

Lola: I can remember one instance of a registry in my tenure on TAG. The conclusion was "this shouldn'tbe a registry."

Jeffrey: It sounds lke those are questions abot the design of the registry. Regardless of th equestion's providence, if it's a good question, we should ask it. The second one sounded like an interface question ("does the registry have the right fields?") I would want to verify the assertion about the carhacter of the registry. But that seems like an easier one to answer.

Heather: I'll ask those questions for clarification, and we'll decide on a resolution based on their response.

Lola: Do you want someone to join you?

Heather: Sure

Jeffrey: can you check the "get status for policy" question?

Heather: sure

Hadley: We prreviously talked about duplicating existing registries. That's sometihng else to consider.

Lola: I'd like Heather to help us understand if this should be a registry, and to Hadley's point, make sure there aren't existing registries that could be used/extended.

#### [design-reviews#1251: Other Spec Review: JS Self-Profiling Markers (ProfilerSample.marker)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1251) ([Github](https://github.com/w3ctag/design-reviews/issues/1251)) - @jugglinmike, @marcoscaceres, @bkardell

Brian: Mike and I met and drafted a comment that Mike posted today. If you could review that draft response. I've tagged Luke.

Lola: Who can do that?

Brian: I tried to loop in Luke because he has worked a bunch on commands. Dan and Jeremy would also be helpful. We thought maybe this could be declarative, and it would be safer and easier, in a way.

Dan: I will take a look!

Brian: Oh, sorry, what I said earlier was for the Windowing proposal.

Jeffrey: Can you link to Ryoske's comments instead of just saying "the issues"

#### [design-reviews-private-brainstorming#341: Other Spec Review: CSS line-clamp](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/341)

Brian: approved

Heather: We discussed it on last night's call; it didn't seem like anything we need to review.

Brian: It's used by 40% of page loads today. It's popyular because there's no alternative way to do what it's trying to do. It un-prefixes it and gives it some new features (e.g. max-height)/

Lola: My concern isn't specific to this, but clamp-type things sometimes have accessbility issues. Has this come through APA? Have they reviewed it?

Brian: This doesn't add any new features. It's implemented by all browsers today.

Lola: But if it's going to be specified, and there are accessibiltiy issues...

Matthew: It's a shorthand for existing properties. I guess this would fall under WCAG. It's three thirngs you could use in a particular way, and you need to be aware of X Y, and Z. It would be about adding authoring guidance. 

Hadley: Are the accessibility people on this? We might jsut need a pointer saying, "we understand this is unresolved"

Matthew: I'm not immediately sure if the accessibility people are on this... There is a tracking issue. It's interesting: sometimes, you might want to hide it from everyone (otherwise it could get confusing), but how will that work with interactive stuff? This has long been open, but it was only closed via a commit from a week ago. I'll put this on the APA agenda.

Jeffrey: I heard a glimmer of an argument with which I want to disagree. Just because it is a shorthand, that doesn't mean it's "probably okay". We wouldn't want to add a shorthand that makes a bad practice easier or creates a footgun.

Brian: Line clamping is when you wind up with an ellipses.

Lola: We're at time. It sounds like Brian has a comment ("This is fine"), but we should wait for APA before posting.

Brian: Let's assign it to Matthew and let him use his discretion.

Hadley: I was thinking we could close it and just refer them to APA.

Lola: Can you post that? "We are declining to review--just make sure that APA is doing the accessibility review"

Brian: Sure

#### [state-of-3pc#1: Retire this finding](https://github.com/w3ctag/state-of-3pc/issues/1)

Agreed.

#### [w3ctagbot#222: Organise Issues and PRs According to Meeting Labels](https://github.com/w3ctag/w3ctagbot/pull/222) - @lolaodelola, @jyasskin



#### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov



#### [privacy-principles#469: Suggested new sub-section to 1.2 (Vulnerability), titled "1.2.2 Vulnerability Impact"](https://github.com/w3ctag/privacy-principles/pull/469) - @toreini



#### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel



#### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven, @ylafon



#### [design-reviews#1254: Incubation: Cross-Origin Storage](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1254) ([Github](https://github.com/w3ctag/design-reviews/issues/1254)) - @ylafon, @bkardell, @dandclark



#### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven



#### [design-reviews#1253: Other Spec Review: CSS navigation-based styling](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1253) ([Github](https://github.com/w3ctag/design-reviews/issues/1253)) - @matatk, @dandclark, @lolaodelola



#### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan



#### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman



#### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel



#### [design-reviews#1246: WG New Spec: Additional Windowing Controls](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1246) ([Github](https://github.com/w3ctag/design-reviews/issues/1246)) - @jugglinmike, @bkardell



#### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk



#### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow



#### [design-reviews#1249: WG New Spec: Recognized Entities v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1249) ([Github](https://github.com/w3ctag/design-reviews/issues/1249)) - @hadleybeeman, @hlflanagan



#### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan



#### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow



#### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven




## Eurasia Breakout (Europe / Asia / Australia) - [2026-10-15](https://www.timeanddate.com/worldclock/converter.html?iso=20261015T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Ehsan, Hadley, Yves, Sarven, Lola, Matthew, Christian

Regrets:

Scribe: Sarven



#### [user-agents#63: Scope the arbitrary-content claim to the public web](https://github.com/w3ctag/user-agents/pull/63) - @marcoscaceres

Sarven: this PR has a couple of overlapping lines, or ideas being updated in other 2 PRs. I suggested we should resolve those first and then see if changes should be made. We may not even need this. 

#### [user-agents#68: Fix spelling and enhance user agent descriptions](https://github.com/w3ctag/user-agents/pull/68) - @marcoscaceres

Marcos: Will follow up on the review.

#### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: Waiting for authors to come back.

Yves: Will ping them.

Ehsan: There are only non-blocker two minor questions for them.

Hadley: No deadline, correct?

Yves: No need because it was already published as CR, so it is just extra feedback.


#### [design-reviews#1265: WG New Spec: Global Privacy Control (GPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1265) ([Github](https://github.com/w3ctag/design-reviews/issues/1265)) - @hadleybeeman, @toreini, @hlflanagan, @lolaodelola @bkardell

Ehsan: Like where the discussion is going but agree with Jeffrey's last point that if you ask ??? . Had back and forth with Jeffrey. On paper I don't think there is any difference. There are some inconsistencies that I highlighted and Jeffrey agreed. Overall I agree with the comment that's drafted. Which is also aligned with yesterday's discussion. Will modify Brian's comment.

Hadley: Lola, Are you aware of a deadline?

Lola: No. That was because Brian wanted to potentially send the comment today. And I wanted to include today's discussion.

Hadley: Leaving that with you Ehsan.

#### [design-principles#619: Question: can we better define the intention of the "disable scripting" user preference ](https://github.com/w3ctag/design-principles/issues/619) - @marcoscaceres



#### [private-browsing-modes#7: Enhance documentation on lockdown modes and private-mode behavior](https://github.com/w3ctag/private-browsing-modes/pull/7) - @christianliebel, @marcoscaceres, @hlflanagan, @jyasskin



#### [install-finding#1: Add section on capability gating](https://github.com/w3ctag/install-finding/pull/1) - @christianliebel



#### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel



#### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Christian: We have a draft finding, with one open PR for Jeffrey to review. And we need to agree the label. I'm thinking "concerns — non blocking"? A new label. 

Hadley: Has there been any disagreement to that?

Christian: I suggest concerns not blocking - the label doesn't exist but we were working on it. We don't want to satisified or unsatisfied.

Lola: "satisfied with concerns" causes confusion. Some see it as "the TAG are satisfied with the concerns" and some as "the TAG are satisfied but have concerns." Satisfied and have concerns?

We have discussed this. https://github.com/w3ctag/process/issues/50 "Proceed with caution" was one of the finalists. There were others. 

Matthew: Did we agree "satisfied with concerns" to the new one? Maybe something to look into when people look back at the history.

Christian: Tricky topic. Perhaps use our time to steer.

Hadley: {reads some of the labels} "Satisfied with concerns" does say explicitly "The TAG is satisfied with this work overall but requires changes." While there may be some confusion out there but hopefully ok for us within the TAG.

Lola: There was some confusion among us.

Sarven: Should we mark old labels as historical? We did make those decisions. 

Marcos: I agree with Christian. I'm not convinced that WebMCP is a foregone conclusion, it's just one solution amongst potentially thousands.

And with Device and Sensors, we saw a group recognising the "satisfied" and ignoring the "concerns."

Yves: we've seen this before, where they saw the "satisfied" and ignorned the "concerns". Fortunately the same issue was raised PiNG. 

Hadley: What's next?

Yves: Resolve label naming.

#### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow



#### [design-reviews#1284: Incubation: Web Haptics API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1284) ([Github](https://github.com/w3ctag/design-reviews/issues/1284)) - @christianliebel



#### [design-reviews#1286: [wg/dp] Digital Policy Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1286) ([Github](https://github.com/w3ctag/design-reviews/issues/1286)) - @csarven

Hadley: We touched on this and will come back to it next week.

#### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @christianliebel, @xiaochengh, @lukewarlow



#### [design-reviews#1278: [wg/ARIA] [Accessible Rich Internet Applications] Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1278) ([Github](https://github.com/w3ctag/design-reviews/issues/1278)) - @lolaodelola

Lola: LGTM. Marking as "satisfied".

Matthew: Fine with the charter as well. They are in conjunction with CSS group on ??? mapping. I don't htink that's a deliverable of the ARIA group. It is probably going to be a joint deliverable.

Lola: Says tentative deliberable for ARIA. The charter includes some new deliverables , protocol allows you to access screen reader and hopefully other AT. I think they should consider ... want to also discuss at TPAC.

Hadley: Which

Lola: I dont' want them it to consider it coming from Lola@TAG but Lola@Individual.

Hadley: Perhaps open issue in their repo and say as without TAG hat on.

Lola: There are other groups that'd be interested in this work too so didn't want it to be a blocker. Happy with the charter as is for the review.

Hadley: That's all fine, don't need to feel constrained.

#### [design-reviews#1266: Other Spec Review: Scroll snap for single-axis scroll container](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1266) ([Github](https://github.com/w3ctag/design-reviews/issues/1266)) - @lukewarlow



#### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1037) ([Github](https://github.com/w3ctag/design-reviews/issues/1037)) - @matatk, @lolaodelola, @xiaochengh

Lola: There was consensus last time that it can be closed with satisfied. We agreed that we shouldn't be doing this much investigation, and instead they should. Open over a year. It is not ready and seems like accessibility professionals not want this.

Matthew: I tried to summarise 5 major issues that still need investigation. One thing we agree on is if there is a better way to do this, great. But maybe it needs an element, and understand why it was discounted bceause it is not extensible, or even if a couple of elements. Ok to explore this but ran into edge cases that don't quite work well in the end. And we felt that CSS carousels is probably a dead-end. To fix the accessibility problem they have to break their own model and using it in HTML would've been fine.

Hadley: What would you like them to do?

Matthew: Asking do we need "this" in CSS or HTML. We do want to make this problem better b/c people use carousels so it is a good effort to try to fix it. But maybe we should suggest OpenUI should have a look and explore so it is workable for the whole community. Perhaps it is relitigating what some think/doing. I think an element is not a bad idea and OpenUI may find that one or a couple of elements find it workable.

Lola: If we can get a comment out before TPAC including the suggestion for OpenUI. They have an accessibility session and perhaps that can be discussed in that context.

Matthew: Sounds good.

Hadley: Agree.

Hadley: For the comment, we are sure of some things, some things need to be explored. We discovered the limtiations in CSS and causing troubles. Perhaps saying TAG discussed this and say in one comment.

Matthew: Will do. I want to suggest positive things. Will draft. Lola can look?

Lola: Next week.

Hadley: ok .. it might be useful for a couple of us to guide open ui convo if it needs clarification.

Matt: I want to go

Hadley: if you can't go, can you appoint someone else?

Matt: yes

#### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

No updates

Hadley: we good for timing?

Matt: There's stuff for me to catch up on

Hadley: [catches group up on comments] we need actionable tasks

Matt: I have a question about agents. I've skimmed the comments. My comments and theres is enough to draft someting

Christian: I'd like to contribute too, just need time

Hadley: Yoav responded 6 weeks ago, we should say something. Matthew can you have an action

Matthew: I can try

#### [design-reviews#1263: WG New Spec: Verifiable Credential Barcodes v1.0](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1263) ([Github](https://github.com/w3ctag/design-reviews/issues/1263)) - @hadleybeeman, @toreini

Hadley: Will come back to this.

Ehsan: I drafted something and would like your opinion.

#### [design-reviews#1218: Media Capture Capability Elements  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Ehsan: I'm drafting another response. Assuming it'll be async with Mike. 

#### [design-reviews#1250: Incubation: WebRTC Diagnostic Logging](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1250) ([Github](https://github.com/w3ctag/design-reviews/issues/1250)) - @lolaodelola



#### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon



#### [design-reviews#1243: Service discovery](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1243) ([Github](https://github.com/w3ctag/design-reviews/issues/1243)) - @matatk



#### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola



#### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh



#### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini



#### [install-finding#2: Add section on engine fairness](https://github.com/w3ctag/install-finding/pull/2) - @christianliebel

Christian: We merged this yesterday, but there were some possible additions Marcos might want to make. FYI to Marcos to send any inputs as a PR.

Marcos: Ack.


#### [design-reviews#1256: [wg/immersive-web] Immersive Web WG 2026 Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1256) ([Github](https://github.com/w3ctag/design-reviews/issues/1256)) - @marcoscaceres, @matatk


## Plenary Session - None



#### Breakout Rollup



#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)



