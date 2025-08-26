# TAG Minutes - Week of 11 August 2025


## Breakout A (Asia / Australia / West America) - [2025-08-12](https://www.timeanddate.com/worldclock/converter.html?iso=20250812T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, just Martin. And separately, Max

Apologies: Xiaocheng, Jeffrey

Called off after ~10 minutes.

<!-- Design Reviews -->

### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh
### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Marcos has a message to post.  It looks like ChatGPT wrote it, which I wouldn't be proud of, but it's there.

### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark

## Breakout B (America / Europe) - [2025-08-13](https://www.timeanddate.com/worldclock/converter.html?iso=20250813T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present:

Regrets: 


### [societal-impact-questionnaire#4: Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4)

Lola: This was filed in 2021. Since then, a lot of development has happened, even within W3C. I think deferring to the [Ethical Principles for Web Machine Learning](https://www.w3.org/TR/webmachinelearning-ethics/) would be a good idea, possibly also the Ethical Web Principles. Is there any reason to include here?

Hadley: I concur.

Lola: Things like bias and power are also already considered in the Societal Impacts.

Sarven: Sounds like a good assessment. I think the question is: is it something specific to AI that we need to highlight, or if you break it down to whether it's about the forms/kinds of AI that are actually used out there. Algorithmic bias is a good idea - maybe the document should cover more towards that angle, rather than umbrella AI.

Lola: Should we focus on algorithmic bias over other types.

Sarven: Algorithmic bias, but also centralization, sustainability, 

Lola: I'd like to be cautious, as there's already Ethical Principles for Web Machine Learning, which covers every kind of concern you one might have.

Hadley: Thinking about the users of this document. There's a lot of stuff out there that covers a range of important things. When people are filing a review request, are we saying that we want people to consider a certain subset of things, or _all_ of the related documents that are out there. Good example is accessibility screener, as we're just asking about the things that people may not have thought about that may mean they need expert input.

Lola: Accessibility one is largely about things people may not already know about. ML is so specific that I can't imagine someone's creating a technology, and they don't know it's going to be using ML. They wouldn't need prodding to go and read the principles. With privacy they may not understand the impacts of what they're doing. Maybe it's like WebGPU - it's so specific that it's known e.g. that there's a certain kind of hardware needed. It couldn't be designed without that intrinsic nature.

Sarven: I think there's something to say about AI but I'm not sure of the angle. E.g. bias, spreading of misinformation, accountability... We know that browsers have new features that may be leading users to type into a text area. There is a lot of stuff we could highlight, but not sure how to package it. Don't think it's about "AI is bad; be careful about it" but when we break it down, what kind of patterns come out of some of these implementations that we need to warn about. If you're building a future into the browser that processes the user's input/thoughts, don't throw that into some cloud/storage without their consent.

Lola: +1. Next steps could be Sarven could have a think on possible angles, and comment on the issue thread, and we can discuss async, and in next week's meeting.

Sarven: That's a good way to move forward.

Hadley: +1 but one more thought... another viewpoint may be that we wouldn't want people working on AI-related ML stuff to scan through this and think "this has nothing to do with me" - maybe there's value to mentioning it so that they're kept in the audience.

Lola:  AI is the hot thing right now, but it's one of a few different web technologies that have potential negative impact. Highlighting only AI may be missing other things, and we don't want proponents of the other things to think _they're_ not included.

Sarven: We also know there are benefits to certain groups whom it may provide assistance. On the one hand there are some benefits, e.g. accessibility, but what are the trade-offs; what are they giving up? E.g. Web Speech - some uses of this could help with accessibility, but those voice patterns could also be stored. This could be a great example to get the reader to reflect.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: I think we should eventually have examples for each item. To start off I've created two sub issues for 2.3 Spec Misuse and 2.5 Excluded Web Users. Sarven has provided two examples: Geolocation, Web Speech, Digital Credentials. I am happy picking any one. DCs is happening but is not yet solidified. I feel like Geolocation and Web Speech are, though I could be wrong. Thoughts?

Sarven: I wonder if the section should highlight a spec and mention where it could be misused _or_ whether it should not name a spec, but name the general concept; geolocation or credentials could be simple and clear examples for people, regarding how they could be misused, e.g. via the info being stored. Specs should have "considerations" sections that highlight the risks. If we identify something that wasn't included in the spec, is that something we should be following up? What do people think about the approach?

Matthew: we try and avoid naming and shaming, but in the Ethical Princples we have included examples of where we got things wrong as a community, but ancient ones so as to not be encouraging drama. Ones where there is consensus generally on them. Ok to do that. If we can do the general principles, like things around minimalisation. one of the privacy principles around data minimisation... justification for it. Might reinforce things.

Hadley: One of the things I'd like to do with the Ethical Web Principles... we've talked for ages about putting examples next to each principle, to demonstrate the credibility of the principles. "This principle isn't just a random idea we've had, this is hard-won knowledge from this situation, and that situation..." Doing the same here would enable someone new to the questionnaire to appreciate why the questions are important.

Lola: I think a good example of spec misuse is Autoplay. It was created; a bunch of people misused it; and things were added to the spec to caution people around this, and to provide attributes to help control it. This is about the effects on users: motion sickness etc. If we can provide examples of specs created, of course in good faith, were misused, and then either changed or deprecated, that could be a good way of touching on Matthew and Hadley's points. These are examples, but we're learning, and speaking from a place of experience.

Matthew: I felt disabled with the Meta ViewPort tag MaximumScale. I hated it. And everyone (the implementers) just ended up ignoring it. It was beautiful. 

Lola: So for this, i think we should find specs that have been misued and have been corrected. 

Matthew: +1; nice and positive!

Sarven: I think your suggestion of third-party cookies is very good. We have a finding on that for easy reference. Historically, everyone remembers the automatic window pop-up without the user's consent. That functionality got misused, and browsers took measures to not do that anymore. When we look back there are interesting examples. It needs to be something current/relatively current like 3pc, or more historical things that nobody's going to dispute.

Lola: Let's put this on the agenda for two weeks' time, so we have more time to think of examples async.

### [societal-impact-questionnaire#11: centralization](https://github.com/w3ctag/societal-impact-questionnaire/issues/11)

Lola: I thought 2.8 in the questionnaire covered this; Sarven agreed but thought we could say more; I think what Sarven suggested is fine. Can you make a PR so we can review?

Sarven: The credentials finding has related sections on centralization and control. There are disadvantages and advantages, for both implementers and users. We need to be concerned with who's being left behind, who's being taken advantage of.

... There are different kinds of centralization: technical; political; governance; ... consider the drivers for centralization (or not).

Lola: Added to f2f agenda (expect there will be wide interest within TAG, and it needs more time).

... Next steps on this: open a PR with your thoughts, or at least include the questions you raised in the thread.

### [user-agents#7: Consider applications with both 1p and 3p sections](https://github.com/w3ctag/user-agents/issues/7)

*skipping*

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14)

*skipping*

<!-- Design Reviews -->

### [design-reviews#1127: WebAuthn Level 3: Related Origin Requests](https://github.com/w3ctag/design-reviews/issues/1127) - @toreini

Matthew: Martin proposed a comment; LGTM; shall we ask him to post it?

Lola: Agree LGTM. Anyone have concerns?

Hadley: I don't disagree with any of it, but it's unclear to me what we want them to do.

Lola: When we resolve as unsatisfied, do we have to have an action item for them?

Hadley: No, but I would want to know what to do in order to make the TAG happy.

Lola: This seems simlar to RWS or other cross-origin stuff, where we say this goes against what we say for the web.

Hadley: I'd like to see something that gives them a next step.

*Hadley requesting this on the private thread - we could come back to this in the plenary*

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) - @toreini

*bump to C please*

### [design-reviews#1129: Incubation: `CrashReportStorage` API](https://github.com/w3ctag/design-reviews/issues/1129) - @christianliebel

*skipping*

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

*skipping*

### [design-reviews#838: Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola

Lola: I posted my thoughts on the internal thread; looking for review.

*Group resolves that Jeffrey's work on the "TAG bot" site that brings together discussions around issues is awesome!*

Hadley: it doesn't look like there's consensus within TAG about the resolution of this?

Lola: There was a discussion about the privacy impact of this.

Matthew: This one from Martin? https://github.com/WICG/turtledove/issues/990

Lola: Yes.

Lola & Hadley: we'll continue reviewing, and wait until Jeffrey's back.

## Breakout C (Europe / Asia / Australia) - [2025-08-14](https://www.timeanddate.com/worldclock/converter.html?iso=20250814T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Hadley, Matthew, Ehsan, Marcos

Apologies: Xiaocheng, Jeffrey


### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Ehsan: Jeffrey and i are still discussing. I'm waiting for him to sum up. Martin?

Martin: I haven't had a chance to look at those, nor the issue that Sarven has raised. I had hoped Sarven would attend today. 

MArtin: a few issues to still meaning to work on. We had reviews and checking the work has happened. Need time to go pass JEffery's review and made a few sub-issues. Now there are 5 issues from Sarven and another comment from Ehsan on that. 

HAdley: shall we create sub-issues?

MArtin: not on the wide 

MArtin: need help

Ehsan: I am happy to help.

Martin: Anything to discuss right now?

Ehsan: I think that harm and abuser are used interchangeably in the document. it might be good for the trerminology to clarify. i cited a couple of papers to make that distinciton, but I wanted to see what you thought.

Martin:  abuse is using something in a way that wasn't intended. harm is when there are consequences for that person. if we're careful about using both terms appropriately -- and we may not be, I'd appreciate your help in getting there -- we should be ok

Ehsan: I can help

Martin: i haven't gone through all the details of your comments. We did have a discussion in the individuals-to-business-entities one

Ehsan: we are waiting to see what jeffrey said as well. You'll see why i proposed that. We can have an agreement on that. I agree with you last time you mentioned agentic AI and how it can be done. I'm happy with the consensus here. if you think it should be included, I'm fine, if not, I'm fine as long as you are on the same page on the reasoning.

Martin: Our user agents finding will cover off the agentic AI side. Identifying businesses andthings otehr than people is best to keep. out of scope.

Ehsan: fair enough. Differential vulnerability, as a concept... you mention it I think in section 5. Maybe we can bring that out, make it more explicit? the concept of vulnerabilty is differetn for different demographic kinds of people. 

Martin: I'm looking

Ehsan: it's appropriate to mention in section 2? 

Martin: Ok. If you can come up with a short addition or a tweak to something?

Ehsan: Ok.

Martin: the other one you raised: what is the root of trust on these things? there is a lot we could say here.

Ehsan: I understand the complications behind the disucssion. and I understand your reasons for not wanting to open that door. But I think it needs to be mentioned at some point, "You need to be careful about that aspect as well", without opening the can. It might not get things for granted as it is from ??? point of view. The things I discuss can happpen, and they are happening as I said in the thread. With other verification companies, it is not uncommon for that to happen. It needs to be mentioned, that you shouldn't put all your trust in the digital wallet anyway. But we're not going to discuss it. 

Martin: There is smoethign to say, I just don't know what the message would be be or whether it would detract from the other messages. most of the messages are bout the use and abues. When it comes to trusting wallets, we could say that the wallet is a user agent and has all the responsibilities. IF we had a finding a finding on the user agent. 

Hadley: I wouldn't rule it out because the user agent finding isn't ready. We've often distilled findings from points we've made elsewhere.

Martin: right, but making the relevant points here could detract. it's easier to say "this is covered elsewhere"

Martin: the question here, is do we want to address teh abuse case. You Hadley are issued a credential by the UK government and you give it to someone else to use. Do we wnat ot address that abuse case? We don't have similar controls on website identity. Why would we have it on people?

I don't know that we need to include that. Priority of constituencies: abuse of people before abuse of websites.

Hadley: agreed. that also sounds like something that belongs in the age verification workshop/discussions.

Martin: This is why we have hardware attestations and all the other things associated with wallets. I don't think the systems people are building suffer from that vulnerability. Apple's TPM takes the credential and it doesn't come out again — that credential is not portable.

Hadley: right. Assumming no one else uses the device.

Ehsan: one last thing: do you want to include cyber bullying or misinformation campaigns etc, as a harm?

Martin: because people would then use other people's credentisals to shield themselves from consequence? that's another step removed again. it doesn't come back to a user benefit.

We could boil the ocean. Putting a scope on these things is often the hardest part. I'm inclined to say no.

Hadley: ok so what do we do with this?

Martin: there are multiple levels of trust. trust in the wallets — we can acknolwedge it as a problem but being out of scope. 

Ehsan: We can make a PR.

Hadley: Who is going to do what?

Martin: Ehsan, if you want to flag something you start working on, I'll do the same. I think we both have an understanding of where these issues are heading. I don't mind if I get half way through something and you come up with a better solution. 

Ehsan: we will coordinate over slack. I'll start with the PR. 

Hadley: keep this agenda+?

Martin: yes. I don't know if anyone has started a document on the f2f agenda?

Hadley: it is better we wait for Jeffrey

<!-- PRs -->

### [w3ctagbot#72: Bump vite from 6.3.5 to 7.1.1](https://github.com/w3ctag/w3ctagbot/pull/72) - @dependabot, @jyasskin

Hadley: anyone else other than Jeffrey working on this?

Martin: it has been used to attack things, not clear what we are protecting?

Hadley: ....

Matthew: the bot had done this. we cna wait until Jeffrey comes back.

Martin: the automatic checks failed, so we can defer this.

Hadley: let's leave it for next week.

<!-- Design Reviews -->

### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @matatk, @xiaochengh

Matthew: Xiaocheng is not here and I am not CSS expert. Our question is why not using selectors. They had reasons, but waiting for their response. It might be related to selectors and they filed an issue on they should explain it. I am inclined to believe there are good reasons, and it fits the CSS ecosystem. We will get the explanation. With respect to question ... : they confirmed they should work on that and it needs to be clarified. They also were talking about scoping these triggers same as anchor-position. I don't think there is a problem but it is not included in the explainer. They seem to be planning it later. 

Hadley: do they have a plan for this?

Matthew: it is not clear. I am not quite calibrated on how pushy we should be in the explainer but we need to make it reasonbly for other to read. They need to put it in the explainer then.

Hadley: so we can put it in our response.

Matthew: I asked them a question and waiting for Xiaocheng to respond. Do we want a CSS expert to have a comment on this?

Hadley: I leave the decision to you. Peter is a good person on CSS 2, Tess also is. 

Matthew: reviewed Xiaocheng comment, seems TAG is happy but I will ask Peter. I will double check not avoid asking them double questions. I will ping PEter to ensure things are ok, then I can put a closing comment then and ping on Slack.

Hadley: frame it to Peter in next 2 days. We don't want to rush him.

MAtthew: agreed.

Hadley: should we agend+?

Matthew: keep things as is: not agenda+




### [design-reviews#1130: Incubation: An `Origin` Object](https://github.com/w3ctag/design-reviews/issues/1130) - @csarven, @dandclark

Hadley: Sarven and Dan not here so skip it.

### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @martinthomson, @matatk, @toreini

Martin: waiting for one of the reviews to appear so we can close it. just checking. I did not post the commment, will do it now. Looking at the top-level issue... sub-issues are still pending.





### [design-reviews#1125: Probabilistic Reveal Tokens (for IP Protection)](https://github.com/w3ctag/design-reviews/issues/1125) - @martinthomson, @toreini, @lolaodelola

Martin: messaged privately to someone working on this API, got a response, not good. It seems they do not have an idea on our negative view and they did not address the question we had. Their architecture is not ideal. I will talk to David so he can put me in connection with someone with more knowledge. 

HAdley: if you have trouble accessing 

MArtin: I think there are many other options out there so there is no need to reveal IP addresses. I need to have more discussion with someone

Hadley: do we need to do anything to the issue?

Martin: I am happy to involve other but I can do it. If necessary, I 'll ask him to come to TAG meeting.

HAdley: okay, we'll leave this with you

Ehsan: would asking them directly "what is your threat model?" would help here? 

Martin: I did ask more direct questions in the follow-up. we'll see how it goes. 



### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Hadley: where are we on this?

Martin: no progress from me.

Marcos: on the WG, we had discussions on the basic model. We are blocked by different arguments on different items, including interaction between APIs. Different suggestions. It is tough.

Hadley: what does it mean for TAG?

Martin: last time we discussed, we asked for some clarification. If it is blocked, we can come back to it.

Hadley: is it helpful if TAG does it?

Marcos: it is good if TAG looks at if it is a sensible architechtural machinery that is required.

Hadley: TAG response: these items are missing, and second: ...

Marcos: I could ot attend WG last week, I am hoping that would happen next week so we could resolve this.

Hadley: can Martin, Ehsan and Matthew come up with a comment?

Marcos: what does is it relate to?

Martin: my biggest problem is the lack of algorithms and not having anything in the registry.

Marcos: this is interesting discussion. There has been complications on registry over github.

Martin: I don't like their interactions. They had long responses, with no conclusion.

Hadley: I am still want to conclude on what to do with this. We can put comments, or officially ask to hold off and resubmit when you are ready.

Martin: my preference is to wait for the working group.  But if you can ask something more concrete, we can act on that.

Marcos: I will put the comment on behalf of WG.




### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion

Hadley: let's skip this.

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Matthew: I wrote a draft comment. I am waiting for a comment from O'hara. If people are happy with the comment, I can post it but I am not happy with it. My concern is to allow CSS to be parsed with semantics. 

Martin: this is good. The whole idea is to give CSS to control the nature of the content where it did not have before.

Hadley: it had be extensively covered.

Martin: it was a difficult one. There are extensive discussions on it.

Matthew: is it appropriate to ask them comment on something?

Hadley: yes, go for it.

---

Hadley: ok, let's conclude.

Marcos: I might not be in the planery, I will try my best to be there.


## Plenary Session - [2025-08-13](https://www.timeanddate.com/worldclock/converter.html?iso=20250813T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

We'll be having Nick Doty join us in the last 30mins to discuss the collection of cross-origin/shared-X type design reviews, and how privacy working group can start thinking about it.

### Reassign Xiaocheng

#### Issue 1120 - CSS find highlight https://github.com/w3ctag/design-reviews/issues/1120

Martin: We were talking about the response here. Not sure we need to get into details
but I don't find response satisfactory. @supports isn't really for feature-detecting
forever. I am overloaded with issues.


Matthew: Maybe Marcos?
It changes the presentation. Would you need to use @supports? Maybe Safari would overload
and ensure good contrast. If you don't, is it acceptable outcome?

Lola: I'd like to avoid getting in the weeds of these issues, there are 11 to get through.
Let's assign and get into the weeds in the breakouts.
Matthew are you OK being the only assiggnee to this?

Matthew: We'll need some CSS input. Do we want an associate specifically for CSS?
Maybe Peter, but not sure how busy he is.

Hadley: Peter is unlikely to be associate given demands on his time, but he could
probably help with an issue.

Lola: Unless we have a specific person in mind, we should move forward with people like Peter.
Maybe we can ask Peter to look at urgent things, the rest we can split amongst ourselves.

Hadley: Other CSS-focused TAG alumns, Tess, Lea...

Matthew: Let's look at the other issues, I can be the only person on this for now.

#### Shared lifetime workers: https://github.com/w3ctag/design-reviews/issues/1089

Lola: Last comment was June 19. I think we're waiting for them.

Matthew: They're waiting for us, Domenic replied. Can anyone take this on?

Hadley: There's a comment from Xiaocheng reaady to post, Jeffrey agreed.
Let's see if we're OK with it and then post.
We need someone to pull up the other alternatives we discussed.

Lola: This seems low-lift, does anyone have bandwidth?

Matthew: Where are the other discussed alternatives?

Hadley: Should be in the conversation

Matthew: Jeffrey and I had two examples

Lola: I can take this; will find the 2 alternatives, and post the existing comment

#### Declarative interactions - https://github.com/w3ctag/design-reviews/issues/1111

Matthew: Talked about this this morning.

Lola: Are you on top of it then?

Matthew: Yes

#### MiniApp Lifecycle -- https://github.com/w3ctag/design-reviews/issues/523

Lola: This is in Max and Xiaocheng's wheelhouse

Martin: This has been there for years, OK for it to sit longer

#### MiniApp Packaging -- https://github.com/w3ctag/design-reviews/issues/762

*also old, OK to let sit*

#### [HTML] Canvas place element -- https://github.com/w3ctag/design-reviews/issues/997

Matthew: We posted comment, Xiaocheng was wondering if we should ask for more detail.
Maybe we meant to close this, or it's pending external feedback.

Hadley: Let's time out out, tell them to reopen if they like.

Matthew: I'll post that comment

#### CSS dynamic-range-limit -- https://github.com/w3ctag/design-reviews/issues/1027

Hadley: Needs HDR/color expertise?

Lola: Maybe ask Lea to look a this?

Lola: Potentially fine because waiting on issues to be resolved, haven't
gotten word that they have.

Hadley: Unsatisfied then?

Lola: Or timed out?

Matthew: One of the issues resolved, one still open.

Hadley: Put that in closing comment?

Lola: Maybe they're still working on the other one? So time it out?
Who is on it?

Martin: I can post and close.

#### CSS if() function -- https://github.com/w3ctag/design-reviews/issues/1045

Lola: CSS if. Xiaocheng is only one assigned.
He asked them to revise explainer.

Hadley: I'd time this one out.

#### CSS Stylable Columns -- https://github.com/w3ctag/design-reviews/issues/1056

Lola: Part of CSS carousel stuff, styleable columns.
Per Xiaocheng's last comment, should be unsatisfied.
It's resoled unsatisfied, needs to be closed. I closed it.

#### CSS View Transitions - Nested View Transition Groups -- https://github.com/w3ctag/design-reviews/issues/1061

Hadley: This looks timed out too. I'll close it.

#### CSS find-in-page highlight pseudos -- https://github.com/w3ctag/design-reviews/issues/1120

Matthew: I'll need to look at this more. Touches on how browsers should present
things to people. If Safari guarantees no contrast issues, question is
if author provided styles and didn't use @supports, is this a problem?
But don't want you to have to do that.
I'll ask the CSS people.


### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @martinthomson, @matatk, @toreini

Lola: Martin posted draft comment, Hadley wanted to review. It's already closed.

Martin: We discussed in last session, closed everything.

Lola: I wrote draft comment referring to your sub-issue Martin.

Martin: I posted the text you proposed.

Lola: That's fine, as long as we mentioned we're not happy with related origin.

Hadley: So we have resolution: Satisfied on the whole spec. Do we want that?

Lola: Yes. Wanted to only mark sub-issue unsatisfied.
Do you still want to have an ask for them?

Hadley: Don't care that much.

Nick: They'll hear similar from Privacy WG.


### Third party cookie replacements, with Nick Doty

Lola: Want to discuss 3P cookie replacements. Getting a lot of design reviews
for things that deal with cross-origin stuff. Related website sets, things of that nature.

Things tapping into storage access. We're not happy with any of it.
Declining all of these things, but it's clear browsers want a mechanism to do
this stuff that 3P cookies used to do.

Want to talk to privacy WG to see if there's a healthy way to transition off storage access. And/or also find better ways to do the cross origin stuff.
Thought talking to privacy WG would be a good first step.

Matthew: There's a couple privacy-related infra things we've discussed. But they're
different problems. One is to ensure we eventuallly transition away from these solutions.
Other is about when sites want to express they're related to each other.
They facilitate payments, provide useful functions, they're stuff with web apps,
we looked at manifest changes proposed. Want to express relationships when one company
buys another, want to have a relationship between the domains but 
as a user you don't want all data
to be handed over automatically. Or you might be fine with it.
We don't want people reinventing the wheel, want to see when we're looking at problems
other groups are solving. Want to make sure architecture is streamlined but that it's
doing the right thing for the user, not sharing data without consent but not 
overwhelming with prompots.

Nick: I think there's work to do. Referencing TAG's docs (Privacy Principles, and the Third Party Cookie finding). I think it's a good idea,
there's both interest and skepticism in the rest of the Privacy WG.
I don't know the set of proposals you're seeing frequently.
Chrome abandining 3P cookie deprecation...seems like these are already having
issues with adoption. Not sure why we think there's a lot of proposals/work there.
But design for purpose is good long-term strategy to help sites migrate away
from 3p cookie tracking.

Lola: I'm confused about chrome's status. Jeffrey is best person to ask about this.
I think they are moving forward with some bits, but not others.
But a good point -- if other browsers don't implement, does it matter?

Nick: Websites won't implement, they'll keep using 3p cookies.

Martin: If websites continue with 3p cookies they won't be interested in building
up these more expensive, complicated alternatives.

Hadley: I put a link to a review we're talking about yesterday, webauthn, found it
to be too close to model of data crossing origins.
Still a lot of this kind of paradigm coming up.

Lola: This was part of joint effort with pepole who are not Google/Chrome.

Nick: If there are other browsers interested, then maybe there's work there.
Certainly are privacy questions. Introduces data sharing risk.
Could work on it on design for purpose way. Maybe still interest;
My question from TAG is what can the privacy WG do if there aren't other
browsers interested? If others are, and you're seeing more proposals,
that's a more specific work item I can discuss with group.

Lola: Would it be hepful if we label design reviews we're seeing related to this?

Nick: Yes. Might be some things in anti fraud space, or fedCM.

Lola: I'm doing review for fenced frames.

Nick: That seems in that area of potential work.
I think having more of list would make for more informed discussion.
Other question is, what do you want us to do?
Proposals like this will come up, something designed for purpose is better.
Need to determine cost, utility for users? Need to give more specific guidance?

Lola: Hard to answer, I don't know expertise of everyone in PrivacyWG.
Don't want to make more work if it'll be difficult to accomplish.
But if possible, more specific guidance if that's realistic for PrivacyWG.
A lot of the principles we have now apply to thsee things. We reference them.
If this is something people in addition to Chrome want to do, we should
help them do it in a privacy-respecting way.

Nick: Let's assume we have the expertise. Is there something that a perfect
author could write that could be useful? Or can we not be more specific
than the privacy prnciples?

Lola: If we have perfect expertise, we'd be more involved in design of the spec.
Whether that's privacy WG, or another group getting involved in creating ht ething.

Nick: Often when we write guidance docs, e.g. on fingerprinting, we looked at
lots of specs, noticed pattern of issues, write down in guidance doc.
Question is for x-origin limited sharing, do we have things that didn't work,
things that did, that we could write down in doc?

Lola: We have many bad examples. Hadley, Martin, Matt?

Martin: Lots of things in this space that are potentially problematic.
Lots of things that are problems worth solving but have eluded solutions.
Is this a human? (Fraud-management side of things)
has thrown out bad solutions. We looked at probabilistic reveal tokens earlier today.
TAG thinks this is bad idea. The more general anti-fraud system is in poor state.
I think it's difficult problem. Not sure it's anyone's fault, or it's a systemic thing.
Aside from maybe looking at use cases more closely not sure what more we can do.

Hadley; Another pattern is saying effectively "3p cookies bad, but we need
cross-site data access for just this one use case". The limitations are ridiculous or ineffective. People
think that if we just focus on this one use case, the tech won't cause trouble in
other areas.

Lola: ``<missed>``
  
Martin: One case that recenty came up, the proponents had thought through their
scenarios but hadn't thought through abuse cases.

Nick: When principles say you should use design for purpose mechanisms,
say you should design something just for this, not suitable for general tracking. that's
easier for users to control. We've been recommending pepole do this.
Not sure if there's success stories yet. Maybe FedCM.
Not happy with `missed`. Maybe we need some positive examples of design for purpose.
Maybe can give more guidance. "here's all the things to consider when you're introducing
new token for human-ness". But not sure we can give more general guidance from WG
beyond just Privacy Principles.

Lola: Still helpful to see the list of stuff?

Nick: Yes. If there's list, PrivacyWG should discuss. (just speaking for myself).
Worth an agenda item and discussion. Might say it's interesting, need to wait
for positive examples. Or can say there are 2-3 categories where it'd be useful
doing work in anti-fraud or credentials group. Seems most likely direction.
Need something design for purpose, not sure how, someone could come up with
something in this direciton, we can write down advice, once we've done
it a few times we can have general advice.

Hadley: Should be easy to add another topic label.
Quesition for Nick. Conversation theme is dancing around or trying to ignore
priority of constituencies, ethical principles.
Coming up against someone saying advertising is important too.
As you and the group come across this, if you see edits to any of our docs
that would be helpful, are higher-level than the kinds of things we've been
discussing, let us know. Maybe what we've got isn't used or is being ignored.
We should address that if we can.


Nick: DRM/EME comes to mind. That group rechartered to do more EME.
Some of us raised concerns. Now that group is tryhing to write something
into their spec to say how they will balance concerns of content owners vs
everyone else.
I think that's rewriting pririty of constituencies to demote users.
Maybe the TAG or someone could help. Their use cases aren't going away.
Everyone won't stop limiting content access.
Even that WG knows it, has impression that we'll do it in limited way.
But they don't have much guidance other than we should care about users.
TAG has told them before, there's a purported bargain that browser is
making on behalf of users -- we'll help users get access to more content
by doing a bit of restriction or privacy invasion. But we have little
guidance on how to explicitly do that.

Hadley: Next step?

Nick: Would be interesting if there were a "here's how to implement priority
 of constituencies".
 "This is how you could consider other constituencies without reordering priority."
 
Hadley: Let's find a way to continue conversation.

Lola: Slack? There's a privacy channel.


* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

