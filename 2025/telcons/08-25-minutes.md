# TAG Minutes - Week of 25 August 2025

## Breakout A (Asia / Australia / West America) - [2025-08-26](https://www.timeanddate.com/worldclock/converter.html?iso=20250826T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Martin, Marcos, Serena, Dan

Regrets: Hadley

Scribe: Jeffrey

<!-- Agenda+ -->
### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Marcos: Domenic commented on the Writing comment. But we're not going deeply and instead focusing on the overall issues. Before we'd dive into the smaller issues, we'd have to accept that the overall idea is good.

Martin: In these sorts of scenarios, we're expecting a model, system prompt from the browser, and then an application-level set of instructions. And then the prompt. Is that right?

Marcos: My understanding is that there's a role, inputs, outputs, query coming in.

Martin: Concerned about alignment. We're relying on prompting for alignment. == "It does what 'who?' wants it to do?" What the site wants is one thing, and what's good for users is potentially another thing. It's an API for the site, so maybe that's the most important.

Marcos: You can signal who it's for. Can say the user's prompting or the site's prompting. As the site, you could ask for a summary of some data or answer the query.

Jeffrey: Does this concern need to be in the comment?

Marcos: Think not; focus on the broader stuff. The explainer has 'role'. e.g. role=system, role=user. 

Martin: Isn't that just to supply context? "We've had the following conversation in the past."

Marcos: Who said what. Model might understand who they are.

Serena: Who's providing the role here? The website?

Martin: Yes, so it can put words in the assistant's mouth that never came out of the assistant. Can do interesting prompt injection this way.

Jeffrey: Any harm from that?

Martin: Don't think it's bad for the user to do that. Site could do it anyway. If site does this to itself, does it expose itself to more prompt injection? Just an application integrity question and not a major problem.

Jeffrey: Is this ready to post?

Martin + Jeffrey: Go ahead.

Marcos to post.

### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark

Also see Domenic's feedback at https://github.com/whatwg/html/issues/10673#issuecomment-3222362601

[Jeffrey answers a question from the brainstorming repo: thinks imports can come from both specifier and url space. Exports shouldn't export to URL space.]

Martin: Specifiers and urls are "in the same space" since they're both strings. If the string is specified somewhere, are there constraints?

Dan: Specifier gets resolved into a URL. Constraints on what a valid specifier is, which we'd expand a bit. Before import maps, a specifier had to look like a URL. There were steps to resolve it against the page URL. Import maps let is be a raw specifier. With this, a raw string might not be resolved by an import map, but is still usable.


Marcos: resolution?

Jeffrey: I think we're satisfied or validated. We shoudl close this, let them finish the design, and keep them paying attention to a list of issues.

Dan: Domenic's in the same place.  It's all complicated, but my sense is that the complexity is justified by the constraints and use case.

Jeffrey: Domenic did ask for them to sketch JSON exports. I'm not sure they need to figure that out, but there are some clear ways to do it.

Dan: Maybe we need to undertstand how this needs to look, but not deal with it completely.  Don't want to foreclose on a solution, but that's all.

Jeffrey: Will propose another comment and close that out.

### [user-agents#7: Consider applications with both 1p and 3p sections](https://github.com/w3ctag/user-agents/issues/7) - @jyasskin

### [explainer-explainer#7: Explain why to focus on the end-user's need, and/or moderate that advice](https://github.com/w3ctag/explainer-explainer/issues/7) - @jyasskin

Actually https://github.com/w3ctag/explainer-explainer/pull/30.

Matthew was worried about https://github.com/w3ctag/explainer-explainer/pull/30#discussion_r2290389823

Martin endorses the suggested change (https://github.com/w3ctag/explainer-explainer/pull/30#discussion_r2292234371), and Jeffrey merges it.

<!-- PRs -->

### [web-no-papers#27: Age verification concerns](https://github.com/w3ctag/web-no-papers/pull/27) - @martinthomson

Martin: You had questions around introducing this section. I wanted to provide
some of the context but that's not really the point of this doc, to talk about
pros & cons of age verification. As soon as we step into that, have to address
the problem more directly. As soon as you put those words have to put problem more completely.
All I want to put here is some govs want to do age verification, it's in the laws.
I don't want to engage with "should it exist".

Jeffrey: If we're calling it overuse, have to ack that there's smaller use that would
achieve the same goals.
The UK gov is requiring in a lot of places, so don't know that people are doing it more
than required. 

Martin: It's a difficult statment to make.
I do think it's easier to implicitly say they're asking for it too much
rather than trying to do a proper treatment of the topic in 3 paragraphs.

Jeffrey: We should get a sense from the larger section of the TAG.

Serena: This webpage that we're writing. Who are we expecting to read it, and what context?

Jeffrey: I hope regulators will read it. We're in charge of charting the architecture of the web, so anyone who wants that opinion will find it. We're not quite as authoritative as a W3C statement, but they did pick us to talk about this.

Serena: Do we have rough idea of the kinds of regulatory forums that TAG findings tend to be brought up in?

Jeffrey: Martin is more familiar with whether regulators look at what we write.

Martin: They do. Don't want to say too much because we've got more comoing, can be more direct if we do proper treatment of the subject later on.
Jeffrey is correct in asking for the text to be there at some level.
If we don't address it right now, people will say "what about this thing" that's been coming up in the media.

Jeffrey: What if we put a placeholder here?
"we're worried about the implications but waiting until workship is done."

Martin: That might be the way to go.
Say it's the topic of upcoming workshop, will say more after.

Serena: These findings, we can update them any time?

Martin: With anything like this there's a point in time problem, some people
will read once at the time it goes out. But we do occasionally go back and fix them.

Jeffrey: 3p cookies has been updated, makes a splash every time.

Martin: was confluence of events.

Jeffrey: We won't publish as finding until after workshop

Martin: I was thinking we might do in Sept rather than Oct.
Workshop is oct 7-9.
Still PRs to get to.

Martin: Some regulators will read this stuff because they've got the resources.
What' s more likely is that some civil society or lobby group will use this as part
of supporting material. They'll make a suggestion about legislation and use TAG's
voice as part of that.
Don't know there's special attempt on our part to engage in publicity, it just happens.
With the cookie one, people were paying attention to that area.


Jeffrey: Only other thing we might have disagreed on is what to say about selective
disclosure vs zero-knowledge proofs.
I was trying to say solutions need to prevent this linkage.
You had something about zero knowledge proofs oding that.
But also happy to say don't use selective disclosure.

Martin: Zero-knowledge is form of selective disclosure.
Don't want to get too technical. Key is to say there are solutions
that exist without the privacy problems.
Suggested refarming of text to say zero-knowledge proofs would help
reduce privacy risk without taking position.
It's important we don't take position at the moment.

Jeffrey: Should say in addition "don't use those".

Martin: I'm behind that.

Jeffrey: After that (and the workshop reference), this is ready to merge.

### [web-no-papers#28: Provide a link to mandatory Aadhaar use](https://github.com/w3ctag/web-no-papers/pull/28) - @martinthomson

Already merged.

### [web-no-papers#29: Address government mandates (by example)](https://github.com/w3ctag/web-no-papers/pull/29) - @martinthomson

Martin: Moved this up, is context that applies to the overuse thing.

Jeffrey: Not sure this should close 18. But it's good, we should merge it.

Martin: What's your thinking there?

Jeffrey: I felt like we actually do understand most of the reason why sites
seek to obtain and use identity. Mix of tracking because gov asked them to.
But looking again I think you might already say that.
This sentence just says what this section will talk about.
Fix might be to just make it clearer this is saying we don't understand, it's 
saying what this section will explain.
Could say "sites seek to obtain idenitity for several reasons"
Wouldn't do that as part of 29

Martin: This is in section 3?

Jeffrey: Section 7 is the one 18 was about

Martin: So this is use cases, we start talking about sites 
seek to obtain for multiple reasons, see section 3.

Jeffrey: Right.

Martin: Mash to paragraphs together to make it shorter

Serena: Related question. Usually when we write these up, do we go out
and interview folks, e.g. who have worked on Aardhar and the Estonian ID stuff.
How do we get perspectives?

Jeffrey: In the year I've been on TAG we haven't.
Findings published before that, should have gotten a wider review.
I don't know what was happening several years ago but I do think we should
often send these out for review before publishing.

Serena: Not just having them read what we wrote, actually going out and asking them.

Jeffrey: Yes we should do that. Question is how we make it happen.

Serena: How do we decide to write a paper about something?

Martin: One of those things where it's exigent need. These systems are in process
of being build, we review them, see there's bigger issue not being discussed.
That's usually where findings tend to come up.
Cookies finding came out of a lot of discussions around privacy, cookies,
evolution of the web, tracking...was a need of some clarity, statement was
the perfect vessel for making that info available. This is what the TAG thinks,
informed by the work going on. This is another one of those cases.
Informed by the work going on for different credential systems.

Serena: For the gov entity paper, would it be useful to ask for more 
If I go into my networks and look for folks who worked on the Estonian ID,
ask them to give their thoughts. Is that worth doing?

Martin: Never the wrong time to get more info. Not sure it would change trajectory. It might.

Jeffrey: Might give us extra case studies.

Martin: Not sure any gov has nailed it yet. UK gov did great job early on in terms
of national ID card. It failed so hard people thought UK would never get national ID card.
When idea was floated, was political poison. Could come back, but not anytime soon.
Lots of history around all this. Sarven had great example with Uruguayan passport
no one would accept because of missing field.
That's context but doesn't necessarily end up in the doc.
There is always more info to be had out of these things. But have to make forward progress.

Jeffrey: I want to avoid publishing this and people reading it say there's a great
counter argument that wasn' addressed. If people feel there's a good counter arg
we shoiuld have mentioned it.

Martin: Well known counter argument that's unaddressed looks bad for us.

Jeffrey: Hoping to avoid that mistake.

Serena: Less worried about specific paper, more about how we put in practice 
the act of interviewing folks. 

Jeffrey: Useful to have researcher around, we don't have that backgorund. SHould figure
out how to incorporate into prcess.

Serena: Even if very casual interviews, talk to anonymous person that uses the tech,
don't necessarily have to parrot back what they say, just use in our findings.

Martin: papers available for age verification workshop: https://datatracker.ietf.org/group/agews/materials/.
One of those is user research. That was good, they got a bunch of people to test
age verification. Told them it was for gambling platform, naturally these things
have age check on them, that's what was really being tested. Interesting to find
the ways people bounced off the different proposals.

Serena: Which specific paper?

Martin:  https://datatracker.ietf.org/doc/slides-agews-paper-measuring-user-responses-to-age-verification-architectures-evidence-from-a-deceptive-online-experiment/


### [web-no-papers#30: Maybe we can say something about phoning home](https://github.com/w3ctag/web-no-papers/pull/30) - @martinthomson
### [web-no-papers#31: Write something about wallets](https://github.com/w3ctag/web-no-papers/pull/31) - @martinthomson
### [web-no-papers#32: Fix some uses of "this"](https://github.com/w3ctag/web-no-papers/pull/32) - @martinthomson
### [web-no-papers#33: Cherry pick some feedback from Ehsan](https://github.com/w3ctag/web-no-papers/pull/33) - @martinthomson

### [web-no-papers#34: Add a more thorough treatment of statelessness](https://github.com/w3ctag/web-no-papers/pull/34) - @martinthomson


<!-- Design Reviews -->

## Breakout B (America / Europe) - [2025-08-27](https://www.timeanddate.com/worldclock/converter.html?iso=20250827T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Matthew, Jeffrey, Dan, Christian

Regrets: Hadley, Yves

Scribe: Jeffrey

<!-- Agenda+ -->



### [explainer-explainer#9: Update the WebIDL guidance for explainers](https://github.com/w3ctag/explainer-explainer/issues/9)
### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Jeffrey: Should we queue anything for the F2F?

Lola: Centralization is Agenda+'ed. Input is particularly valuable for this one, and I'll also look through the other issues.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven
### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

<!-- PRs -->

### [explainer-explainer#30: Say how to explain developer-focused features.](https://github.com/w3ctag/explainer-explainer/pull/30) - @jyasskin

Jeffrey: Checking if Martin's right that I should link to the appendix as a whole?

Lola: Think it's right to link to the subsection.

Jeffrey: Will merge.

<!-- Design Reviews -->

### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Lola: I noted that they should flesh out the explainer in the spec, but I haven't finished otherwise. Matthew?

Matthew: I noted quite a bit in the private brainstorming thread. There's a list of things we haven't brought up before, and a copy of an old thing. The long section is varying levels of importance, but it's all worth asking. It's a reflection of the fact that as Martin said, there's a lot of detail missing. Some is suggestions that we should put prominent notes pointing out to other documents. One typo I did a PR for, so it's not in the list anymore. Feeling on whether we have rough consensus that these things are worth mentioning? Martin was saying that the vibe is that these are things we should be asking.

Lola: On point 3, "Does the verifier get any information on the wallet model? like some digital credential are to be held in government official wallets so it might reveal the citizenship of the user to the verifier as side channel? (e.g. through 'the data member' request data to be handled by the holder's credential provider, such as a digital identity wallet.)"

Lola: My sense is that the verifier and issuer don't know anything they don't need to. Verifier shouldn't know anything about the wallet?

Matthew: In theory yes, but say your gov't issues stuff comes from a particular wallet that only holds that stuff. Does that leak somehow? Credential has to come from this kind of wallet, so this person is German?

Lola: When I read the spec, I thought the answer was 'no'.

Matthew: They expressed a desire, but we're wondering if the tie of a credential type to a kind of wallet makes it clear.

Jeffrey: I think the identity of the issuer is necessarily exposed and reveals things like "I'm German". But the identity of the wallet could be private in other ways, and if the spec doesn't guarantee that it's kept private, that's something we should ask them to guarantee.

Lola: Think there's no harm in asking the question. Maybe they'll just need to be clearer.

Jeffrey: This is a good list of things to ask them. We should flag that it might not be complete.

Lola: "16. Accessibility considerations: UI isn't specified, but it would be vital to ensure that any info presented in a non-text way has an alternative. So far I haven't seen any such info though." -- Is that the spec's responsibility since UI is out of scope?

Matthew: We know that UI is out of scope, but if there's the possibility of showing non-text data.

Jeffrey: Photo?

Matthew: Non-text data needs to have an alternative, probably text-based. Might be that the answer is that it's not up to the spec since it's format-agnostic. But then it should be a requirement for protocols to be allowed in the registry. Definitely also author/issuer, but probably schema too.

Jeffrey: Do make it clearer, since you're expressing a very technical requirement on the data format that expresses the credentials.

Matthew: I'll do a pass with the above updates, will post a draft comment to brainstorming.

Lola: This list is long, and everything present should be present. Martin might add things. Should we do one long comment? Think we shouldn't merge the two.

Jeffrey: I think we shouldn't wait for Martin's review, and should give them the feedback we have when we have it.

Matthew: Martin's comment might be more architectural, while mine is more a spec review.

Lola: I also plan to do a review, and I'll avoid re-posting things that aren't in Matthew+Ehsan's review.

### [design-reviews#1130: Incubation: An `Origin` Object](https://github.com/w3ctag/design-reviews/issues/1130) - @csarven, @dandclark

Lola: In the docs CG, we experimented with explainer reviews. Consensus on another proposal for Origin objects was "why?"

Dan: I reviewed this, and asked why. Also comments on considered alternatives.

Christian: I like the response.

Lola: Do we need to wait for Sarven?

Dan: Think it's just Christian and me.

Lola: If Christian's happy, I think that's fine.

Dan: Ok, I'll post.

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

Matthew: From Edinburgh, we only had consensus that web browsers were web UAs. But lots of different options. Different people had different subsets. In Paris, we talked about mini-apps and super-apps, and had slightly conflicting views on whether super-apps were UAs. Thought mini-apps were not. We should discuss, and I copied Max. I also downloaded the whole meeting minutes repo, and grepped it for user agents. It comes up a lot. Could dig some more to see if there's historical consensus.

Lola: Do we need to queue this up for the F2F?

Jeffrey: Think we should queue the whole finding, and this is an important issue.

Matthew: I think browsers in XR devices are browsers, but they're somewhat different. Might edit the list.

Lola: If you're an app, like Slack. I click a link that opens in an in-app browser.

Jeffrey: If we look at the definition currently in the doc, we say
 (https://w3ctag.github.io/user-agents/#what). Includes in-app browsers. I think this gives answers
for several of the things in this list.
There are UAs that are not web UAs, e.g. wallets.
The thing I'm writing a patch for is about apps that have both 1p and 3p content,
like slack, how those apps distinguish to users the different parts of themselves.
Only constrained by the duties for the 3p parts.

Lola: Are there apps that scrape from the web and show things in the app, but aren't
browsers themselves.

Jeffrey: That steps into AI question. If you're showing people stuff that wasn't
created by the author of the AI, pulled from the web, you're effectively a web UA
according to current definition. The question for the current issue is should we change that defintion.
What do the examples say about whether that's the right defn. Can give examples
of how that applies to different things. 





### [Issue Triage](https://github.com/orgs/w3ctag/projects/6)

Lola: Moving crash reporting to B.

...


https://github.com/w3ctag/design-reviews/issues/1139

Jeffrey: Tempted to say we should decline this one. We don't generally have anything to say, and TTML isn't too attached to the web.

Lola: They change attributes on text elements.

Jeffrey: Think that's just their own XML elements.

Lola: Someone do a once-over?

Matthew: me.

https://github.com/w3ctag/design-reviews/issues/1140

Jeffrey: Copy the people over from PEPC.

...

## Breakout C (Europe / Asia / Australia) - [2025-08-28](https://www.timeanddate.com/worldclock/converter.html?iso=20250828T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Martin, Matthew, Ehsan, Christian, Sarven

Regrets: Hadley,

Scribe: Ehsan

<!-- Agenda+ -->

### [design-reviews#838: Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola

Lola: f-first thing to discuss, I wrote a response in the private-brainstorming with Martin, Jeffrey and Mat. I responded to the commetens too. I have follow-up question for Mat. The last comment in the issue mentioned they had mitigations in place for the proposed attacks. Should we include the lack of mitigation and conclude the proposal is unsatisfied.

**Christian and Sarven joined**

Matthew: it takes me longer to catch up, I was raising MArtin's issue so we can shortcircuit this by asking him.

Martin: let me look at the comment. where is the brainstorming?

Matthew, Lola: already put in the chat

Martin: so you modified?

Lola: I included Jeffrey's comment on the fact that protected audience has a dependeny on fenced frame but it is not true the other way. Martin commented, I responded on agreeing with you, but I removed the sentece because it provides alternate solutions outside fenced frame so I concluded this might be out-of-scope. In addition, what matthew asked on the issue on tutlelove and Matthew was suggesting to include that in the comment but it needed more clarification as the last comment in the issue included the CAPTCHA as an exception. 

Matthew: issue #990 in the turtlelove was the issue we talked about.

Lola: I posted that in the chat too.

Lola: are you still catching up?

Martin: in a bit.

Martin: it is the critical weakness.

Lola: so should I acknowledge that we can see they are working on this I don't think they should reopen.

Martin: is this something else or is it worth it to accept there is weakness in the design and the fact that they are working on it. We don't know if the mitigation coming soon. Given the strength of the usecase, we can include it in the comment.

Lola: I will include it. Thanks Matthew and Martin. I will have a draft for that by next week (maybe today or tomorrow) for you to review. 

Sarven: I had a question in the channel on looking into the workflow?

Lola: if you are interested...



### [societal-impact-questionnaire#11: centralization](https://github.com/w3ctag/societal-impact-questionnaire/issues/11) - @lolaodelola, @csarven

Lola: the last I remember, Sarven was going to have a pull request.

Sarven: it didn't happen

Lola: that is fine.

### [societal-impact-questionnaire#4: Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4) - @lolaodelola, @csarven
### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: we wanted to pull to have ageneral text to have a look?

Sarven: I have not looked at this. I need to catch up on this.

Lola: ok, we will discuss it later. I need to add examples for the excluded web users. Specifically, the users that has been corrected.

<!-- PRs -->

### [web-no-papers#26: notes on harm and no passport](https://github.com/w3ctag/web-no-papers/pull/26) - @toreini

Ehsan: I had a couple of PRs, and discussion with Martin, who integrated some of them in another PR, with which I'm happy. For the other bits and pieces there's still a discussion happening, but I'm happy with the shape of the document at the moment. Is any further clarification needed from me?

Martin: I need to take another swing at this. There are only one or two PRs that have questions around them at the moment; will get those in and then come back to you with further comments. The document is in much better shape for all the work being put in.

<!-- Design Reviews -->

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) - @toreini

Ehsan: Think we discussed last week too; generally happy with the purpose of the spec, though the explainer is not in a good shape. I have asked them @@@@@@@ if they can clarify the explainer. We are discussing in the private thread. Martin and Jeffrey had comments/clarification requests. I think we're waiting for Jeffrey to have a look at my response.

### [design-reviews#1129: Incubation: `CrashReportStorage` API](https://github.com/w3ctag/design-reviews/issues/1129) - @christianliebel

Christian: I lost my script, sorry. 

Lola: I sent you a link it is in the chat.

Christian: it is a small API, it sets context in case a crash happens. It is somehow a storage. The piece of the API seems fine and validated by JEffrey. This is not the entire review of the overall API but this smaller piece seems fine so I sugegst we go with the validated comment.

Lola: is this smaller part of the crash report API?

Christian: yes

Lola: does it mean we agree with that?

Christian: yes, validated. If agreed by you we can close it.

Lola: it looks like Jeffrey reviewed it as well.

Christian: yes.

### [design-reviews#1125: Probabilistic Reveal Tokens (for IP Protection)](https://github.com/w3ctag/design-reviews/issues/1125) - @martinthomson, @toreini, @lolaodelola

Martin: we reuested to retract the request. as it was negative in our opinion

Lola: does it mean they make it better?

Martin: no, they already implemented it.

Lola: too bad.

MArtin: it is product for them, that is their practice.


### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @toreini

Ehsan: Last comment from Martin... I agree with his point. The use case seems more like a usability practice, but it comprompises privacy for the sake of usability, which is not that usable in the first place. Overall I was leaning towards disagreeing with this proposal, as I don't think it is going to be helpful for the users. What does Martin think?

Martin: Yep.

Ehsan: We already put an issue in their repo for them to resolve; Jeffrey validated this. I think they'll resubmit at some point. It's on their RADAR.

Lola: Do we want to wait for them to resolve the issues Martin and Ehsan opened in their repo? also, Martin: the comment that you drafted... do we want to make this into a TAG comment, or are you speaking on behalf of yourself?

Martin: I'm happy for it to be me, but if the rest of the TAG agrees, we can say it as TAG.

Lola: I think as Ehsan agrees with you, we could say it from the TAG perspective. And that makes the position of the TAG clear. Do we want to include anything about the isseus that you and Ehsan have opened on their repo?

Martin: I don't think that's going to change the dispostion overall. If folks agree with the comment, then I'm happy to post it, and note that the TAG generally agrees.

Lola: I do agree and am comfortable with that.

Martin: We could have someone else say that we broadly agree that the privacy leak isn't justified.

Lola: Is it important to present the comment from your perspective specifically (e.g. 'I think' vs 'we think')

Martin: No - it's just that this is fairly opinionated - which is fine if the TAG does have that opinion. From conversation with the proponents, I understand vision is for all the login actiities be activated through a similar UX (passkey, federated login, etc.). The vision is cool, but they are going to the next step, but that gets sketchy as they're relying on the web site to choose which options are available, rather than the browser. HAving the web site choose is a privacy leak.

Lola: I'm not opposed to having this come from TAG, so we could include more 'we' language.

Martin: Let's give it a couple of days for review?

Lola: +1

Ehsan: +1. This is a classic example of how much agency to give to various parties. Not worth it in this case in my opinion.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://github.com/w3ctag/design-reviews/issues/1120) - @matatk, @xiaochengh

Matthew; I proposed a comment last week and had a response from Jeffrey. He is asking to substitute something. I am fine with changes he proposed. If you are happy with mine and Jeffrey's sugegstion, then I can post it. I put a link to it.

Lola: yes please.

Matthew: just did. 

Martin: JEffrey's comment is to recognise the background colours.

Lola: I think this is fine.

Matthew: so I will post it.


### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @matatk, @xiaochengh

Matthew: we had a whole discussion on this related to gaps issues or why selectors are like that in CSS and some more @@@. I proposed a comment last week and Jeffrey posted "the text seems ok". Are people happy with me posting with this one?

Lola: yes, that is fine.

Matthew: I wonder if I did already... it should have appeared in the tagbot.

Lola: it is not there so post it please.

Matthew: will do please.

----

Lola: is there anything else to discuss?

Matthew I have a question on F2F. It seems I do not need visa but I wonder if there is a system to register to entering Hong Kong.

Lola: I went on the .gov site and it says as UK citizens we do not need to do this.

Matthew: there is a web app for Japan that you need to register for that. You don't have to, but you should. I wonder if there is anything similiar like that for Hong Kon to avoid confusion on border entery.

Lola: I don't know.

Matthew: I will ask in the slack.

Lola: is everyone ready for Hong Kong? Seems yes. Please do label the ones you want to discuss in f2f so we don't miss anything. 

Lola: Martin sent a link for Hong Kong entry. please post it in Slack.


Matthew: how to close the declarative interaction as there is a list of comments.

Lola: I think this has been validated, so we can post it that way. There is clarification on what the label means.

Martin: we can say we checked, there is no further problem so TAG is done with it.

Lola: any other business? If no, have a good rest of day.



## Plenary Session - [2025-08-27](https://www.timeanddate.com/worldclock/converter.html?iso=20250827T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Martin, Matthew, Sarven, Lola, Christian, Ehsan

Regrets: Hadley

Scribe: Matthew

### Incorrect claims in Prompt API review

https://github.com/w3ctag/design-reviews/issues/1093#issuecomment-3222435561 includes quotes from the explainer that don't exist. How did this happen, and how can we prevent it from happening in the future?

[discussion about next steps]
Lola: ... In terms of using AI, we should be clear about what is acceptable.  I also use AI for a11y.  Difference between taking text from the LLM vs asking questions and exploring ideas.  We need to be more specific about what acceptable use looks like.

Christian: Most of my texts go through an LLM for proofing; it's helpful for me as a non-native speaker, but factual content should be validated. ...

...

Jeffrey: ... I think 'Do not generate any parts of your proposed comments with an LLM' might be a good policy. They do a good job at answering questions to inform the review, but I think using them to generate text for discussion with TAG, or as output of the review, is out.

Sarven: It's beyond just hallucinations that's an issue with these tools. If you ask a question about a spec, it may be referring to an older version, or something not even true, for example. Regarding Explainers, I know some of us can see where a feature may be going, but I find value in really studying the Explainer, so that when we're writing a response, we're talking about the same thing - puts us in the same mental space as the designers - even if we don't have all the details behind the spec. I think this is something that LLMs can't achieve. They may not even be referring to the Explainer.

Jeffrey: I've had the experience of asking one to summarize an article, but it gave something one might expect that actually said the opposite of what the article was saying.

Lola: Do we need to discuss this at the f2f? Are we happy with the position that we're not going to post public comments that have come from AI, or should we discuss this further?

Jeffrey: May make sense for one of us to do a patch on the guide for new TAG members; I can work on this. Can discuss at f2f if it's not finished by then.

Lola: +1

Jeffrey: I'd welcome Christian's insight on how does one use LLMs safely.
---

Christian: Resolution on this?

Jeffrey: We need to re-review it, having apologized.

Martin: Can we put that note in today, so Dominic isn't left with a wrong impression?

Lola: We already have a note on there saying we're going to review the issue and will review at this meeting.

Jeffrey: We can post an apology immediately after this meeting. Can you Lola?

Lola: Yes.

Sarven: If we wait until publshing the minutes, we could provide reassurance that it's been taken seriously.

Jeffrey: I think it's worth publishing something today, as the minutes are 3 days away.

### Planning the Hong Kong F2F

Jeffrey: Does the proposed developer meet-up schedule work for us. It's about an hour longer than the Paris one, but similar shape.

* Developer meetup schedule
  * 19:00 - 19:30 Reception with refreshment 
  * 19:30 - 19:45 Opening by Codeaholics
  * 19:45 - 21:15 W3C TAG panel discussion, Q&A
  * 21:15 - 21:45 Networking 
* Daily schedule 
* Topics

Martin: Seems workable. Is there any attempt for us to seed the ground with topics that we'd like to discus, or are prepared to discuss? Of course we should be willing to talk about anything relating to the architecture of the web, but is there anything in particular?

Jeffrey: The organizers suggested we prepare some fallback questions, but be prepared to answer whatever people ask. The plan would be, as with Paris, to go around and make intros first, which may seed the discussion.

... If things wrap up faster, noone's going to blame us.

Martin: We should definitely talk about the role of AI on the web. I'd like to hear what other folks think on the topic.

Jeffrey: I'll say this schedule is good for us. We were also asked for an approximate number of people. I'll check with people on this.

Jeffrey: *Looking at planning spreadsheet*

Jeffrey: Please go through and mark issues as 'Agenda+ F2F'

Jeffrey: Wanted to see how people feel about the overall schedule shape. It has a bit more break time in it. I put in a 9-noon session and a 2-5 session, which puts some extra break time at lunch, but is that the right way to do it?

Sarven: Seems reasonable to me.

Martin: My experience is, if it's full-on, by the end of the third day you're very tired. So if we have slightly later start time, breaks, maybe taking an afternoon off, the total time will be 3-and-a-bit days. We always have the flexibility to stay a little later to get things done, but this will prevent it being too intense.

Sarven: Wednesday afternoon for longer break?

Martin: That may work due to Wednesday being developer meet-up day. Might suggest 9am for turning up, 9:30am start. The workshop we are running has what looks like a shorter day, but it makes sense to space it out a bit, and the time around the sessions is often where the real work happens (people getting to know eachother; identifying issues outside of the structure).

Jeffrey: ISO C++ meetings are 5 days; start at 08:30, have evening sessions.

Martin: Where they productive?

Jeffrey: They were productive, but also intense.

Jeffrey: Officially start 9:30; 2-hour lunch; end at 5 by default. As we get some more topic over the next week or two we'll add them to the schedule. Feedback welcome.

### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @lolaodelola

Lola: My closing comment was an amalgamation of a few comments that came before it - this could do with some review. May need to be particularly careful in light of the Prompt review.

Martin: You can start the shared worker ahead of time; this deals with the constraint that it has to be created with the fact that its lifetime might be extended past the lifetime of the page.

Jeffrey: I think we didn't do enough of a good job of explaining what this API shape will do. If we get to exit without cancelling this, then we start the shared worker.

Lola: ________

Jeffrey: I feel the name is clear enough, but it clearly needs elaborating what these calls will actulaly do. I can respond to Dominic.

Martin: You could speak to the web lock question.

Jeffrey: You start the shared worker, then start an extendable task inside of it.



<!-- Agenda+ -->

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

. . .

### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Martin: The request is to review between now and the time we meet in HK. I got great reviews from Jeffrey, Ehsan, and Sarven so far. The state of the document right now is reaosnably good if you take into account the ~5 PRs. Need to do a little bit of re-org, which will hopefully happen before the end of this week, after which it'll be much closer to a final document. Right now, most of the changes that have happened have been relatively cosmetic, and adding references to make the arguments more complete. Future changes are likely to remove things. Scope/content shouldn't change much from here on in. If you review this week, it may shift a bit, but input would still be helpful. You'll see there've been some additions recently that talk about age verification, mostly referring to the workshop that's coming up. Maybe we'll be able to take a position after that. My sense is that within the next day or so you'll see a document that's essentially complete.

... My request is that everyone in HK will have read it, so we can discuss it there.

... Mostly this is about: don't create a system that can be abused. There aren't too many concrete suggestions; we don't want to be over-prescriptive about what WGs can do.

Jeffrey: I think my review from here on is going to be asking: what can we recommend; how can be a bit more pointed.

Martin: +1 ACK your pushing on the age verification issue. There are potentially other relevant issues too.

Sarven: I created issues at the time I reviewed; will follow up on Martin's comments. Some points came from concerns others have raised that seem relevant. E.g. the passport concerns. (https://github.com/w3ctag/web-no-papers/issues/20, "Uruguay issues passports following ICAO Doc 9303, which says including "place of birth" is optional ... Germany, France, and later Japan refused to accept these passports for certain travel and administrative purposes")

Martin: Great example. Need to generate better interop.

Sarven: There is a standard for it, but it's not being acknowledged. If we have something that's encouraging DCs, it's going to have the same side-effects.

Martin: That Uraguy example would've been great when I was writing RFC____ as it shows how the standard is _this_ but in practice it's something else, and you end up with interop problems. Need to align the two sides (standard and reality, whichever tunrs out to be the right thing, after discussion).

Sarven: Does the example not fit here?

Martin: I couldn't see a way to put that scenario into the document as an example of exclusion. It seemed like more of a bug, as it's now been fixed, it will not affect future people anymore.

Sarven: Are we taking random things from the world and writing case studies? When I wrote it, I didn't meant it as top-level thing, but an example.

Jeffrey: I think the question for this finding is: what concerns do we have when we translate physical documents to being trasnported over the web. We need to figure out how any example (such as this one) is a cuationary tale for online documents. It was a failure for offline documents, rather than online ones.

Martin: The general message is when you get a digital identity doc, there will be some that aren't accepted by some sites for whatever reason - because of a bug in this case - so people who can only obtain that type of document are excluded. The question is whether this example strengthens that text. It's pretty clear from the text that this is a possibility, so the further back-up wasn't needed.

Jeffrey: Wendy filed an issue about whether they should have a registry of protocols, and what acceptance criteria would be. This example shows the importance of a standard for interop. They had one in this case, but didn't ensure everyone could support the minimum level of interop with it. Maybe this example belongs in the DCs API feedback?

Martin: Agree; *makes note*

<!-- PRs -->

<!-- Design Reviews -->

### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion

Jeffrey: The Web Payments WG is trying to adopt this work (https://github.com/w3c/webpayments/wiki/Agenda-20250828), at which point they'll ping the TAG review. Stephen asks what questions they should prepare to answer. I gave my guess at the list based on looking over the discussion, but any other questions are welcome.

Martin: I'd like to see this be a standard format for the link. So there's a standard set of slots. So that you understand that the item you're paying for goes in one slot, and ____ goes in others.

Jeffrey: PaymentRequest has a field that is a blob that corresponds to this.

Martin: Can the TAG say anything negative about crypto?

Jeffrey: We can, assuming consensus. We will get complaints from at least one person. Payments in general, or what to do with cryptocurrency?

Martin: Cryptocurrency specifically. This has come up in DIDs, DCs, it's a common theme in some parts of the community that you make an empty bucket and fill the bucket any way you choose - but drawing the line on what's in the standard and what's not is an important area.

Sarven: How does TAG respond to design constrictions around the interplay between web and non-web. Taking this example of payments, they say it's strictly not HTTP. How do we respond when others are using the web as a way to get to the non-web things? It's a common thing, that people want to hook other systems to the web. We need a common position on it. If one of these services is used for evil, we don't want to allow it. Then every time a similar topic comes up, we don't need to revisit.

Martin: This comes back to a topic the TAG of yore would be interested in. If you have a URI, conveying the content packed into that - e.g. MIME types. If you have an HTTPS URI and you pull the content, and get back a document that describes what you'll get. It gives you the option to be more flexible about what you are going to get. Packing things into the URI is quite different. Thinking of Henry (our host in Edinburgh). Would be interesting to get folks' opinions on this.

Jeffrey: This has come up in AI and Agents: what is the web? It's possible that interacting with stuff via agents will make web pages very different (or go away) in future, but what would it need to look like in order to count as the web, if it's not over HTTP. For discussion in HK.

Sarven: As an example, the `file://` scheme. It's off the web, but the platform has an opinion on how to treat it. There's an opportunity to say what the UA should do for any givne scheme. How do we deal with S&P considerations for non-HTTP schemes? There are a bunch that UAs have encountered, and decided how to treat, in the past.

Jeffrey: I think this will help inform the discussion with the proponents.

### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @martinthomson, @jyasskin, @csarven

<!-- General stuff -->

### Any other business
### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Logistics

Chair:

Scribe:

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/08-25-minutes.md

Raw minutes: ...


## Local Call Times


### Breakout A (Asia / Australia / West America)

<table>
<tr><td> San Francisco (U.S.A. - California) <td> Monday, August 25 at 20:00 PDT</td></tr>
<tr><td> Boston (U.S.A. - Massachusetts) <td> Monday, August 25 at 23:00 EDT</td></tr>
<tr><td> London (United Kingdom - England) <td> Tuesday 26 August at 04:00 BST</td></tr>
<tr><td> Paris (France) <td> mardi 26 août à 05:00 UTC+2</td></tr>
<tr><td> Beijing (China) <td> 8月26日 星期二 GMT+8 11:00</td></tr>
<tr><td> Sydney (Australia) <td> Tuesday 26 August at 13:00 AEST</td></tr>
<tr><td> Corresponding UTC (GMT) <td> Tuesday 26 August at 03:00 UTC</td></tr>
</table>

### Breakout B (America / Europe)

<table>
<tr><td> San Francisco (U.S.A. - California) <td> Wednesday, August 27 at 10:00 PDT</td></tr>
<tr><td> Boston (U.S.A. - Massachusetts) <td> Wednesday, August 27 at 13:00 EDT</td></tr>
<tr><td> London (United Kingdom - England) <td> Wednesday 27 August at 18:00 BST</td></tr>
<tr><td> Paris (France) <td> mercredi 27 août à 19:00 UTC+2</td></tr>
<tr><td> Beijing (China) <td> 8月28日 星期四 GMT+8 01:00</td></tr>
<tr><td> Sydney (Australia) <td> Thursday 28 August at 03:00 AEST</td></tr>
<tr><td> Corresponding UTC (GMT) <td> Wednesday 27 August at 17:00 UTC</td></tr>
</table>

### Breakout C (Europe / Asia / Australia)

<table>
<tr><td> San Francisco (U.S.A. - California) <td> Thursday, August 28 at 02:00 PDT</td></tr>
<tr><td> Boston (U.S.A. - Massachusetts) <td> Thursday, August 28 at 05:00 EDT</td></tr>
<tr><td> London (United Kingdom - England) <td> Thursday 28 August at 10:00 BST</td></tr>
<tr><td> Paris (France) <td> jeudi 28 août à 11:00 UTC+2</td></tr>
<tr><td> Beijing (China) <td> 8月28日 星期四 GMT+8 17:00</td></tr>
<tr><td> Sydney (Australia) <td> Thursday 28 August at 19:00 AEST</td></tr>
<tr><td> Corresponding UTC (GMT) <td> Thursday 28 August at 09:00 UTC</td></tr>
</table>

### Plenary Session

<table>
<tr><td> San Francisco (U.S.A. - California) <td> Tuesday, August 26 at 23:00 PDT</td></tr>
<tr><td> Boston (U.S.A. - Massachusetts) <td> Wednesday, August 27 at 02:00 EDT</td></tr>
<tr><td> London (United Kingdom - England) <td> Wednesday 27 August at 07:00 BST</td></tr>
<tr><td> Paris (France) <td> mercredi 27 août à 08:00 UTC+2</td></tr>
<tr><td> Beijing (China) <td> 8月27日 星期三 GMT+8 14:00</td></tr>
<tr><td> Sydney (Australia) <td> Wednesday 27 August at 16:00 AEST</td></tr>
<tr><td> Corresponding UTC (GMT) <td> Wednesday 27 August at 06:00 UTC</td></tr>
</table>

