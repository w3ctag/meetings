# TAG Meeting Minutes - Week of 3 Feb 2025

## Agendas

### Breakout A (California / Europe)  - [2025-02-03](https://www.timeanddate.com/worldclock/converter.html?iso=20250203T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014) - @jyasskin, @torgo
* Web as a Commons update?

### Breakout B (California / Australia) - [2025-02-04](https://www.timeanddate.com/worldclock/converter.html?iso=20250204T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039) - @martinthomson, @jyasskin, @marcoscaceres
* [On-device Web Speech API](https://github.com/w3ctag/design-reviews/issues/1038) - @jyasskin

### Breakout C (Europe / China) - [2025-02-05](https://www.timeanddate.com/worldclock/converter.html?iso=20250205T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion
* [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk
* [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman
* [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk
* [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @hadleybeeman
* Societal Impacts Questionnaire

### Plenary Session - [2025-02-06](https://www.timeanddate.com/worldclock/converter.html?iso=20250206T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* reassign [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* reassign [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* reassign [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss
* reassign [CSS if() function](https://github.com/w3ctag/design-reviews/issues/1045) - @LeaVerou
* [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)
* [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* Face-to-face update

## Minutes

### Breakout A (California / Europe)  

Present: Dan, Lola, Jeffrey, Matthew, Yves, Sarven, Hadley
Regrets: Tristan

#### [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014) - @jyasskin, @torgo

Jeffrey: propose we close this as "satisfied with concerns" - we found pros and cons... I think we said the useful thing we can say.

Dan: I agree - let's try to close it *at the plenary.*

#### Web as a Commons update?

Jeffrey: Tristan & I had a conversation with Brett & Greg Bloom about Brett's opinion of seeing the web as a commons. He was optimistic and offered to introduce to the Knowledge Commons - the research effort that Brett is helping to organize. Run from University of Indiana. They will introduce us to the professor - there may be PhD students who could [help].  There's an open question of whether we can participate in the commons workshop in Amherest in June. I might be only person who can attend - but also not sure it's worth going...  We have a document ... sense of the TAG is that we don't want to publish it as a TAG document. It argues that part of the structure of the web is that web sites see their visitors as a commons reseource. We may want to figure out what the TAG wants to say about this and what practical impact we want have. I want others to suggest things.

Lola: What's the plan?

Jeffrey: this structure came from the knowledge commons research framework: https://knowledge-commons.net/research-framework/ I would be fine publishing this as a draft note... but others may not support....

Dan: [f2f minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2024/12-edinburgh/minutes.md#web-as-a-commons) where we discussed this...

Hadley: I agree with summary from jeffrey

Jeffrey: also thinking about digital commons ideas: e.g. wikipedia, software... falls into digital commons .. and web doesn't seem to fit into that...  

Dan: so... what is the actionable advice? We had that interaction with Nikki on Mastodon, who was talking about this. I think she was saying: that we should not be tryingto say "you posted it on the web, therefore it's a commons and anyone can use it however they want". Then we're in a discussion about copyright, fair use, which is different in different countries. We should be careful not to wade too far into htat pond. However, we have a history of writing docs like the Ethical Web Principles that put guard rails in place. We can say, "In order to fthe web to remain healthy,... THIS!" And it is not healthy for the users of the web to be seen as a commons reosource that companies are able to exploit.

So, maybe something that could flow from the ethical principles, that could set some guard rails? That we could then draw some actionable guidance from.

jeffrey: commons misunderstanding is that commons are free-for-all. the key aspects of this academic work is that it's not. The knowledge commons work is overly focused on legalities. But a key aspect of commons work is that it's not based on legalities. It should have enough legal legitimacy that government doesn't interfere with it. It should be "people making things happen". We're seeing some of this emerge for AI - e.g. tools you can host on your web site that will trap AI crawlers and give them garbage... There's a lot more to do. We should be thinking about how do we enforce rules on the commons resources. 

Dan: re rules we could push for: links. there is this tussle between people that want to put lots of links vs for instance social media sites that are giving lower priority to posts with links in them (vs those that don't have links in). That comes back to web architecture, old-school web.

Matthew: my impression.. in Edinburgh we were talking about providing tech leadership for the web. There's this whole body of research... it looks like the web might be one of those systems (a commons.) If it turns out that the web is one of those systems, the people in the web sphere might not be aware of it... that might enable the stuff - how to keep it sustainable and healthy. It's not up to us to say "the web is a commons" - but with external help we can do that and then that gives us the basis on which to build guidance on how to steer it.

Jeffrey: that sounds right to me...  Question is how do we decide yes or no? The commons research talks about things that have social dilemas... A bunch of shared resources... it's a normative quesiton. 

Hadley: I think ... that we should be careful about not describing the world as we see it.  The commons research is small number of people describing the world as they see it... we shouldn't take that as something set in stone.  Same thing about government policy... part of how laws evolve is based on what we're doing... 

Dan: I can't help but think about how the EWP evolved. We leaned on some work that had already been done, reviewed with some academics and got feedback, but a lot of what htey said was "this looks good if it works for you." and "we don't see a major problem with this." It was interesting that people didn't jump in to say "you're using the wrong language, or framework here". So I'm trying to htink about how we can use this to solve thep roblems we see on the web, evidenced by the design reviews etc that we see. By leaning on this research, we can apply this to that, but we should be opinionated about that. We shoudl not just be trying to reflect existing academic research. We should be opinionated. The AC wants us to be opinionated.

Sarven: in Weaving the web Tim talks about web of people... touches on this topic of designing the web so it works for society... The one angle for TAG is: how do we get things lined up so the type of things - e.g. in freedom of expression, privacy, child protection, intellectual property, ... governments do have a role... but ... what jumps out ... various things in the world are are commons. What are we doing here to make sure those things are effective on the web... Are we making sure people do have their privacy?

Dan: you're wondering how the web enables other commonses?

Sarven: yes - "we all have to ensure the society we build with the web is of the sort we intend" (quoting weaving the web)... some stuff we can tap into... We can see if this works in the way it was originally intended... It's not just whether the web is part of the commons - but also how the web should work ... to make sure that the things in society are still applicable here.

Jeffrey: Good point - part of thinking of web as a commons is that there are nested structures ... how the web enables the stuff that's nested inside it... Web is inside the internet... A bunch of things like wikipedia are inside the web... The research that I've seen talks about "questions to ask" and doesn't proscribe any answers... I think we should work on answering the questions... Then we can take those answers to figure out what practical changes the imply... which is what I've put in my document. What we do with that is a separate question. 

Dan: maybe we should reread Jeffrey's document and the minutes from the f2f and revisit at the plenary?

I'd like to get to where we have actionable guidance, to answer the "so what?" We can work on that in Paris.

Jeffrey: my preference is to keep those in separate documents. Separate the factual and normative documents. I think it will be easier to iterate on them separately. They have different audiences, different expert reviewers. Feels like two different categories of statement. 

Jeffrey: read [robin's thoughts](https://lists.w3.org/Archives/Public/www-tag/2024Nov/0001.html) - though I don't agree with some of these points 



#### Reassigning Issues

Matthew: CSS issues...  We need to start working on associates...

Jeffrey: *will create slack channel to start putting together associate nominations*

[Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - reassigned to Hadley and Lola

Lola: need infos

Dan: https://tag.w3.org/workmode/ and https://tag.w3.org/workmode/design-reviews/ are good places to start on design reviews...

Hadley: looking at our last comment -- saying last month that use case can also be abuse cases... we haven't heard back from them... So now we have to get their attention... or do we close it?

Jeffrey: I can escalate to them... Don't have answers but can ask - escalate.

#### Ownership of Documents we're Writing: User Agents, Explainers, AI, etc...

### Breakout B (California / Australia / China) 

Present: Martin, Jeffrey, Xiaocheng

Scribe(s): 

Chair volunteers?



#### [Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039) - @martinthomson, @jyasskin, @marcoscaceres

Martin: Doesn't engage with what we want to have happen here. There's a clear direction in the Identity community to move to the 3-party model. Good direction. Details matter. Mechanism in the main explainers allows Issuer-Verifier linkability: If they collude, they can join their information. Selective Disclosure, and you refuse to share a piece of information, the Verifier can just ask the Issuer to fill in the blanks. Whether that's acceptable depends on the use case, but it's hard for users to understand it. Need to work out the details. This gets back to the FedID FO.

Jeffrey: Any other proposals for this?

Martin: There are other formats, which the proposal doesn't dig into. Other formats allow better privacy properties. Those aren't well-enough developed to be able to ship. The crypto exists, but the concrete systems haven't been built. 

Jeffrey: We could talk about what properties we think are appropriate on the web.

Martin: Many use cases with different requirements.

Jeffrey: We want an explainer that lists the use cases, and the properties that are available, so we can discuss them.

Martin: Age verification: common, governments like it. All of those systems have dire properties. You can build a system with zero knowledge and unlinkable, but it's prone to abuse. If I have a token I can share to a website, I can give you that token. Building that out requires extra machinery. Other cases: I have a driver's license, and want to attest to my name. Different use case. In those use cases, we have to engage fully with who issues the credential, who's able to use the credential. "What problem do you want to solve and why?" before mechanisms. Mechanisms may also be problematic. System they describe might have Verifier-Verifier linkability if you're not careful.

#### [On-device Web Speech API](https://github.com/w3ctag/design-reviews/issues/1038) - @jyasskin

Jeffrey: wrote up a very long proposed comment https://github.com/w3ctag/design-reviews-private-brainstorming/issues/98#issuecomment-2634875066

Martin: This might reasonably live on the user agent, which is a prerequisite. Domenic proposed a typing-completion API, which seemed to require a large model. So maybe let the website bring the necessary compute. Having a browser API means browsers are forced to be in the middle.

Jeffrey: And there's some work in Chromium about letting websites share model downloads, which is difficult for privacy reasons.

Martin: Speech recognition might be small and useful enough that we'd assume they're present. 

Jeffrey: But that raises questions for the multi-language support.

Martin: If you're recognizing the language the user of the device is producing, that's likely ok. But recognizing a remote person's language, maybe you can't assume that's available.

Martin: Question of local vs cloud is important and needs to be resolved. I think that before we add APIs for this, there should be a reasonable expectation that it'll be local. A lot of the discussion so far has been about LLMs, which are big.

Xiaocheng: Huawei is interested in enabling on-device models. It's a provider of both the device and OS and browser. What approach is appropriate? Query a local model registry?

Jeffrey: Lots of entities are interested in that (e.g. ChromeOS, Apple, Intel). It's difficult to both support hardware advances and work across all platforms, and especially to support browsers that aren't tied to specific hardware or OSes.

Martin: When it comes to larger models, or experimental models, doesn't make sense to have a web API just yet. Let sites experiment, and identify commonalities later. In the case of speech recognition, which is a core OS feature, making that core OS feature available seems reasonable. Have to do it without local personalization.

Jeffrey: Talk to Domenic Denicola.

Jeffrey: I'm hearing concern about cross-language packs, but not concern about the capability at all. I'll edit that into my comment before plenary.

Martin: Distinguish speech recognition on device for form entry, from this capability where the site recognizes.

[Discussion of the permission shape. This spec doesn't cite getUserMedia.]

Jeffrey: The spec isn't in good shape, but I don't know that it's worth saying that given all the other commentary.

Martin: Call out the fingerprinting risk of onDeviceWebSpeechAvailable(). 

Martin: Bilingual people may speak multiple languages in one chunk of text. The models can often deal with that, but this API can't.

Jeffrey: That's probably a larger change than they're hoping to do in this update.

Martin: But maybe they should do it right. I think this is dated enough that it needs work.

Martin: Themes: where the model lives; API shape in general; unnecessary fingerprinting risk. Will talk to Paul Adenot.

Jeffrey: My sense is we should make sure the new parts are good, but leave the old thing alone.

Martin: Vs build a new thing to replace the old thing. You probably want a stream. Then you'd drop the integrated microphone permission, you'd add language to the stream (where unrecognizable text would say [unrecognizable text]). Fingerprinting exposure is related to the text you put in, where the audio-stream input makes fingerprinting worse.

Jeffrey: Would prefer not to tell them definitively to do this over, but we might request that they think about alternatives more thoroughly.

Martin: Yes.

Jeffrey: Will update the comment for plenary.

(side discussion: the question about what we might do about how models are run is one that the TAG should perhaps think about putting a finding out)


#### Reassigning Design Reviews

Look through [issues owned by Amy, Lea, Peter, or Tess](https://github.com/w3ctag/design-reviews/issues?q=state%3Aopen%20(assignee%3Ahober%20OR%20assignee%3ALeaVerou%20%20OR%20assignee%3Aplinss%20OR%20assignee%3Arhiaro)), and claim any you're able to work on finishing.

#### Ownership of Documents we're Writing: User Agents, Explainers, AI, etc...

* Second editor for [User Agents Finding](https://w3ctag.github.io/user-agents/)
* Two editors (ideally) for [Explainer Explainer Note](https://w3ctag.github.io/explainers/)
* Owners for [website maintenance](https://github.com/w3ctag/tag.w3.org/)

Martin: We also share the Design Principles, so I don't want to volunteer for others.

Jeffrey: And I don't want to make Xiaocheng commit to anything in his first week, but please consider these.

#### What do you want 

\[General discussion of plans and goals]

### Breakout C (Europe / China) 

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: last time we wanted them to close it, security review. We wanted Martin to weigh in. 

Martin: think they addressed our comments.

Yves: I'll draft a closing comment and close it.

#### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

Yves: they sent two sets of slides,

Martin: they're both enormous

Max: Matthew, you said you joined the working group at TPAC? Any updates?

Martin: the right thing is to wait on actual updates 

Matthew: nothing to add. We've got the most direct reference to the info, in the thread.

They had the discussion at TPAC, I wasn't there. We should at least check their plans for what's next. My recollection is that Martin (and we) had concerns about the handshaking aspect of it, and other SDOs

I'll check in the minutes/slides

Martin: they are resolving some of the same problems being addressed in groups in the IETF. They are in a better position to do protocol work and the auth/security stuff to get this off the ground. Those groups don't have a web focus. 

Hadley: so there is at least an opportunity for working together

Yves: I note they are referencing the Open Screen Protocol, which is discontinued as of Dec 2024.

Martin: side project? 

Matthew: last line of the minutes from the TPAC discussion mention the IETF https://www.w3.org/2024/09/27-webscreens-minutes.html#t11 

They're talking about moving OSP to the IETF.

Martin: good for them.

Matthew: sounds promising. seems like they're going in the direction we'd ask them to. We should encourage them to do that, and maybe specific groups in IETF, give them pointers to previous work. 

Martin: One of their slides talks about a split between network and application. 

Hadley: so we give the feedback and can ask them to get back to us in due course?

Martin: let's let them get on with it.


~~~
We see that there has been some discussion about a split between networking parts and the application pieces.  It seems like this will result in some significant changes, including a potential move of large parts of the proposal to the IETF.

We are interpreting the material you have linked as an opportunity to give the folks working on the proposals some space to refine their proposals.  To that end, we'll put this issue on hold.

If there is anything the TAG can do to help or if you think that the proposals have stabilized to the point that a review would be helpful, please let us know.
~~~

#### [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk

Matthew: Jeffrey and I came up with a comment... Framed their problem where any of this should be normative, if it will solve particular problems, and could the rules be integrated into mainstream testing projects (headless and the like), and we haven't heard back. We didn't say "we want to hear back from you", but expected feedback. 

We're not concerned, it's a good thing they're doing this. Tehre is a lot of inconsistency of WCAG etc. Consensus here would be good. But hte comment we made: getting the max possible impact from it. Make sure they were pursuing right track in W3C. We weren't asking them to do something, just get their ideas for where they wanted to go.

Hadley: should we explicitly ask?

Matthew: I'll draft something. Wouldn't be terrible to just close it, but I'm curious about the plans and whether we could help. Will prod and will ask Jeffrey to help. 

#### [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman @csarven

Max: one comment: the use case is more focused on web based payment. but what is the user experience for native apps? Maybe they can clarify.

Sarven: I raised considerations along those lines. If this makes its way in, how would it play out for the user? Concern re HTTP URLs... URI schemes specific to bitcoin or a wallet, the user would know what to do with it, especially if it knows which other app to trigger to deal with payments. But the majority of the web deals with HTTP URLs, and there is no specific URI template for those payment pages, so the UA can't do anything with them. So the utility of the way they're presenting their case is on custom URI schemes. The concern: this is a solution pitched as good for the web. But what's really useful is URI schemes for payment. There was an example with PayPal, but I couldn't find a URI scheme for it.

Max and Sarven to craft a comment. 


#### [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk

Matthew: [summarises the discussion thus far]
We are awaiting feedback, but they haven't yet. At the plenary, we can ask Jeffrey if he knows anything procedurally.

Xiaocheng: if the current API is to permissive, what is our appraoch to further restrict it?

Matthew: we're still working it out. If it's an existing API which we don't expect is going away, we can file a bug on it. In this case, the intention is for this new stuff to replace the old, so we are concentrating on making the new stuff safe for users. Once that's been implemented, we would advocate for removing the old and unsafe stuff. But we haven't had a concensus fro mthe TAG on this. 

Xiaocheng Hu: I see. So, another decade's work.

Hadley: Yes

Matthew: let's check this again at the plenary.

#### [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @hadleybeeman

Hadley: [reviews last week's discussion] Conclusion: we decided we needed Marcos's input.
Matthew: I'll assign him and ask him for his input. 
Hadley: If it's possible to feed in before the plenary, that would be amazing. Quick turnaround though. 

Look at the plenary. 


#### Societal Impacts Questionnaire

hadley: to Tristan and Sarven, is there anything useful we can do with this time?

Sarven: No, I just need to get started with editorial pass and process issues etc. Discussion with Tristan.

Tristan: Same thing. 

Sarven: Also we need to see where the web sustainability interest group is going with it, understand their angle.


#### TAG documents with the new TAG

Martin: As discussed in B, the Explainer explainer, the website as a whole -- fewer than two editors. 

Yves: and we need to look at assiging people to issues, those people who have left.

Martin: we agreed to have two active people on an issue, but not removing old TAG members so we can see who was involved.  

Sarven: I'd love to contribute to User Agents Finding as second editor, help Jeffrey.

Hadley: talk to Jeffrey directly

Sarven: done.

#### carbon.txt

Tristan: how can we feed back to the Green Web Foundation?

Yves: include https://datatracker.ietf.org/doc/html/rfc5785

Matthew: so instead of squatting on that URL, you'd have a well-known URL for finding that. We'd be suggesting they register that with IANA. I don't know what Martin's idea was, but his comment was entirely on how you get to the information.

Yves: it's just to avoid overusing things in the top level of a website. 

Matthew: Threads are for doing that (in slack). I'd be interested to see where this goes, so I wouldn't like to lose visibility. 

Hadley: procedurally, we can have a quiet word with them, open a design review, or write a blog post, note or finding.

Sarven: Would it be help to publish a response within w3c/tag space, then share a copy on their issue or reference it? (Somewhat in contrast to us showing up to their issue and making suggestions)

Hadley: if you feel something benefit from TAG discussion, bring it up. There is too much for everyone to track/process. 

### Plenary Session 

Present: Dan, Martin, Tristan, Jeffrey, Matthew, Yves, Xiaocheng, Hadley, Max

#### TAG associates nominations



#### Breakout Rollup

##### Breakout A
* Close [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014) with `satisfied with concerns`? "We're concerned about the small number of websites that seem likely to be able to use this, but that's balanced by the large number of users who could benefit. Thanks for bringing it to us."

Dan: Lots of discussions about the commons work, minuted.
Jeffrey: No followups or changes since monday.
Dan: Something happening in June, which we might participate in, though that shouldn't be what drives our schedule. We can start thinking about some of the "so what"(?) stuff now.

Dan: We did a bit of reassignment of issues.  Fenced frames to Hadley and Lola.
Dan: Talked about the ownership of documents we have.  Sarven and Tristan will take over the societal impacts questionnaire.
Dan: Incumbent on us to each jump on for work.

##### Breakout B
* Proposed comment for [On-device Web Speech [Recognition] API](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/98#issuecomment-2637714938)

jeffrey: not entirely done with a comment to post... Other people should take a look and say if you have concerns.

Martin: signal from the group chair that this isn't ready for TAG review... Although the requestor says it is.  It is being used in other browsers.

Dan: this chair issue is important

Martin: they (the cg) said they want to bring it into the CG and then...

Dan: I think this should go back then... and we should decline.

Jeffrey: I am worried that if we just decline then blink owners....

Martin: we should say clearly that the CG / WG has recently taken an interest and plans to make signifigant changes.

Dan: Agree.

Martin: also want to flag - downloading models and responsibility of APIs that involve models... We may have found the path to avoiding that question in this API.  Looks like a recurring pattern.  If API invovles a model.  Expectation that UA sorts that model...

Matthew: Exactly what I was going to ask about - similarities with translation that has the same issue. We had a discussion on the translation one - consider allowing user / author or both...  They've moved away from doing a "fake download". We should discuss in Paris. It might be vital to have a consistent approach and control for user and author. 

Dan: is this something for the Design Principles?  Let's raise an issue? Or is it an AI finding thing?

Jeffrey: It's not necessarilly AI specific - it's about when it's appropriate for browser to download a model.

Yves: also should this be part of the OS? Like fonts for example?

Martin: we've discussed this at Moz quite a lot - and come to some interim conclusions - one of the lines we drew is "is this reasonably a capability that the UA would have" in which case it's reasonable to expose it to an API... Jeffrey quite usefully highlighted in these audio cases it's probably useful for the UA to recognize the user's voice - but maybe unreasonable to transscribe any language...

Martin: will raise issue in principles repo...

* [Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039): Some ideas for a comment...

Jeffrey: Martin drafted a comment... I think we should post that.

*we agree to post*

##### Breakout C

Hadley: webapp scope extensions - yves to draft closing comments. Martin & Matthew were going to work on a comment for peer-to-peer API... 

Matthew: I think it's necessary and sufficient.

Martin: another comment in the minutes...  

Matthew: *agree on Martin's comment*

*Martin to post*

Hadley: we talked aboout a11y conformance testing.

Matthew: I have a a proposal... *matthew to post*

Hadley: we talked about payment link type in HTML... 

Max: Sarven would prepare a comment but not ready yet.

Hadley: clipboard change event API...  

Jeffrey: I met with them and suggested they re-do their explainer to explain how this works with Safari and Firefox UI Model and they were amenable but no update yet. I spoke informally to [redacted] at Safari to check this and got positive feedback.

Hadley: the 7 verifiable credentials... we punted for Marcos's input...

Matthew: I posted in Design Reviews in Slack... with some thoughts...  

Hadley: suggest we give Marcos until early next week to reply...  We went on to talk about Societal Impacts questionnaire.. Tristan & Sarven outlined next steps.  We also talked about TAG documents... Sarven mentioned he'd like to volunteer as 2nd editior for UA finding.

Jeffrey: +1.

*sarven to send a PR to add himself*

Hadley: we talked about carbon.txt and feeding back to green web foundation... also meta topic of how TAG gets involved in non-w3c activities... all the ways in which we can provide input ... to speak on behalf of the TAG etc... 

Tristan: I saw Martin filed a bug... The conversation is happening with them over there. I know some of the folks over there... 

Tristan: In the conversation around the bug report by Martin - they are asking for help... How do we feel as TAG to help them? 

Martin: I was providing in their personal capacity.. I suggest we do the same unless they request formal feedback from the TAG... If we feel effort is going in a constructive discussion then we can give more TAG time.

Jeffrey: I'd like them to describe their use cases. It feels nice to provide it, but what are they expecting anyone to use this data for?

Dan: Informing decisions: do you want to interact with this company?

Jeffrey: what's the path for a user to make this decision? I won't read an annual report for every website I visit

Dan: A search engine could focus on sustainable sites

Jeffrey: but how?

Matthew: I discovered a browser extension that has parallels to this... called TOS;DR - terms of service; didn't read - puts an icon that gives the web site a grade from A-F according to how privacy respecting the TOS is... This is how they surface it...

Hadley: I wonder if schema.org or an equivalent markup would make it easy for machines to find the relevant data in a more unstructured document (like an annual report)...

Dan: unless we're giving conflicting info from different TAG members, I don't think we need to make this a formal TAG work item at this point.


#### Associates

Jeffrey: we opened a slack channel... each tag associated nomination gets a thread.  We discuss in thread.  If there is no response then we verify at plenary... 

Dan: we do need a decision point at plenary

Jeffrey: Also a sense to limit the number...

*we discuss additional people*



#### Reassign issues
[Issues owned by Amy, Lea, Peter, or Tess](https://github.com/w3ctag/design-reviews/issues?q=state%3Aopen%20(assignee%3Ahober%20OR%20assignee%3ALeaVerou%20%20OR%20assignee%3Aplinss%20OR%20assignee%3Arhiaro))

##### reassign [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

##### reassign [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss

##### reassign [CSS if() function](https://github.com/w3ctag/design-reviews/issues/1045) - @LeaVerou

##### [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)

##### [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)

##### Reassignment of FedCM issues
 @martinthomson is taking these, but he needs help

#### Face-to-face update

#### Chairing!

Volunteers? Preferences? Concerns? Consensus?

##### Meeting scheduling

Fill in the Cryptpad linked from https://w3ctag.slack.com/archives/C089QPD49SA/p1738607594667669.

#### (Auto-)Publish Explainer Note?

https://w3ctag.github.io/explainers/

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
