# TAG Minutes - Week of 28 July 2025

## Breakout A (Asia / Australia / West America) - [2025-07-29](https://www.timeanddate.com/worldclock/converter.html?iso=20250729T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Xiaocheng, DanC, Marcos

Regrets: Max

Scribe: 

### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark

Jeffrey: Introduces the topic.

Dan: Bias is in favor of declarative CSS modules thing. I'm on the explainer. Justin and Rob have been super clear on their use cases. MS-internal folks have use cases for a lesser version of this. Styles that apply in a way that's inline and don't create network requests or JS. No streaming need. That surprised the MS proponents a bit, but use case makes sense. Strangest thing is the use of importmap as the global namespace. Big limitation with @sheet was how to import and export IDs through shadow root. CSS modules is because the namespace is global. Novel thing here to make references into the module map with attributes on an element. Jeffrey's connection is interesting. Implicit import map entry. On the whole seems to make sense. Team has gone back and forth a lot, on the high level directions. Looking for another opinion.

Jeffrey: Adding to import maps from inside a shadow root? Seems odd.

Dan: Putting things into importmaps from inside shadow root does feel a bit odd. Framing from Justin and Rob is that they're doing this today with adopted stylesheets. Import within Javascript, and putting that into an adoptedStylesheet array, today. Module map is already global and doesn't know about shadow roots. Want a way to serialize it into markup. They're arguing that it's just another way of doing what you're already doing. If we don't do this, the solution that we look at is to invent a shadow-piercing global ID. First use of compoennt might be nested, and then those get hoisted. Then we'll have to invent a global ID mechanism.

Jeffrey: Want them to explore the other ways of navigating IDs trhough shadow root. And explain this in terms of import maps.

Dan: And the declarative and imperative mechanisms should interact. Explainer could make this more clear.

Jeffrey: I'll write a comment that generally approves of this and asks them to explore some particular other options. I do super support the use case. Justin's been very consistent about this use case, and not everyone has heard him.

Dan: Lots of similar features. Justin described a flow chart to a fully declarative way of defining components.



### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion

Jeffrey: I owe the proponents an invitation to come talk to us. I've posted to the issue.

### [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres

Jeffrey: I appear to have drafted a comment a month ago and not followed through. Marcos, any comments?

Marcos: Seems ok to me.

Jeffrey: I'll post the comment and close as `satisfied`.

### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Jeffrey: It's incorrect to claim that this API 

Marcos: Apple's platform doesn't guarantee it stays on device. It's irrelevant if the model is on- or off-device.

Marcos: It's privacy-preserving to send it off device. Apple claims it doesn't matter.

Jeffrey: Do we need to comment on whether it's off-device, if Apple believes ?

Dan: Like with Web Speech, on-device might be weird with unusual browser architectures.

Marcos: Thing that's proposed suggests downloading N GB things, even if they're only downloaded once. In those cases, it might be in the background but processed on server while it's being downloaded. 

Marcos: "Tools" and tooling properrties got very complicated. Would be great to get even a small part to be uncontentious. And output formats are a bit presumptuous. Can't guarantee that models will produce a particular output format. E.g. on Apple, if you tell Apple Intelligence to rewrite an email in a particular way. It then puts the subject into the body of the email. Doesn't know how to format things. ChatGPT too. All pretty klunky now. Don't know about the Android side.

Jeffrey: Think we should say that the spec can require that it's "as if" it runs on-device, but a browser that can provide the same privacy properties in the cloud should be allowed. Think we can make that a MUST.

Marcos to draft a comment.

### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres

Jeffrey: Writing Assistance has been approved to ship in Chromium. Do we want to time out or write a comment?

Marcos: Many of the same issues apply as Prompt.

Jeffrey: I think it's a little easier to be interoperable, but agreed otherwise.

Marcos: Need to look at what's actually getting shipped. They're not tied to AI?

Jeffrey: Yes, they're accomplishing tasks. 

Marcos: It'll be hard to be interoperable.

Jeffrey: Microsoft's working on an implementation with very different models, and that'll help us see whether it is interoperable.

Marcos: I'm ok with timing out. Given that there are 2 models.

Jeffrey: I'll post to #design-reviews and see if anyone complains.

### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

Xiaocheng: Discussed a while ago. We should say their proposed solution is ok for the scope of the problem. Should we raise other concerns like it not being idiomatic?

Jeffrey: Think that would be fine.

Xiaocheng: Scope isn't so big, so don't want to introduce a big mechanism for it. But at the same time, but when proposing a smaller solution. Neither their proposal nor the alternatives are idiomatic enough. They look like variants of each other. Don't feel good about continuing to suggest alternatives.

Jeffrey: It's possible for us to say that the solutions are too complicated for the amount of benefit, so they just shouldn't solve the problem for now.

Jeffrey: See also https://github.com/whatwg/html/issues/10997#issuecomment-3105509844, with 2 pre-existing problems that extended lifetime makes worse. And for both, the ExtendableEvent design would solve the problems.

Xiaocheng: Not really about how we enable lifetime extension, but there are a whole bunch of issues that get worse if we enable lifetime extension at all.

Jeffrey: There's a difference in how much lifetime extension you get if you need any. N minutes vs exactly as much as you ask for.

Xiaocheng: They say you have to declare that you need lifetime extension before you use it. I'll draft a comment about being unsure that the benefits outweigh the risks of making other issues worse.

Marcos: Theory that it's time-based is not a great thing. From experience, these things should be tied to tasks. Haven't looked so much, just hearing that it doesn't sound good.

Xiaocheng to draft a comment.

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola
### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini


## Breakout B (America / Europe) - [2025-07-30](https://www.timeanddate.com/worldclock/converter.html?iso=20250730T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Christian, Lola, Yves, Hadley

Regrets: Sarven

Scribe: Hadley

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Looking at https://github.com/w3ctag/explainer-explainer/issues to try to prioritize them.

We agenda+ [#9 Update the WebIDL guidance for explainers](https://github.com/w3ctag/explainer-explainer/issues/9) on Lola's endorsement.

#### [explainer-explainer#16: Explainers should be written for a general audience](https://github.com/w3ctag/explainer-explainer/issues/16)

Hadley: The user need section should be understandable to anyone who uses the web. Especialy the impact on the end user's experience. Teh "how it works" part can have much more specific detail

Matthew; that makes sense to me .the use case is more general. if the job of the explainer is to let revierwers undersatnd the tradeoffs that were made, then we don't necessarily have to be told everything in detail, but we do need to undrsadn thteh difference in the architecture of the different choices.

Lola: This week, Jeffrey joined the DocsCG group to talk about tranferring this to them. They are mostly technical writers for things like MDN, WebDocs, etc. There was a lot of discussion on what part of the discussion could the DocsCG be helfpu and useful in maintaining, and the user need section was one that came up. So I think htere is an audience beyond just TAG: technical writers, developers, etc. 

What would be the difference between an explaienr and developer documentation? Are they the same? Maybe. It's sounding like the explainer should be written in such a way that it IS developer documentation. In Anssi's example, she says that explainers should be used by developers to understand the API in context. 

Matthew: i'm sorry I couldn't go to that Docs CG meeting.

Secondly, to answer your question: i think they're different. Developer documentation tells you how to use a web api that is explainer. the explainer will have some examples of how to use an API to explain it, to give a flavour and maybe to bring some developers on board -- but i think the audience for an explainer is reviewers and other implementers. Some of the explainer could be copy/pasted into a developer documentation, but the explainer is more than that, including the tradeoffs. The explainer is for implementers, the documentation is shop window for developers who want to use the feature. 

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven


### [explainer-explainer#30: Say how to explain developer-focused features.](https://github.com/w3ctag/explainer-explainer/pull/30) - @jyasskin
* Fixes [explainer-explainer#7: Explain why to focus on the end-user's need, and/or moderate that advice](https://github.com/w3ctag/explainer-explainer/issues/7) - @jyasskin

Jeffrey: what does everyone think about this?

Hadley: I'd like to keep the end user as the focus

Jeffrey: the point of this is like some of the improvements in CSS, which make it easier to build your style sheet. maybe it reduces the end user experience, but it's the authoring.

Hadley: I see. That really is the developer need. Well, I guess that's why we have the Priority of Constitutencies.

Matthew: we talked about deprecating document.domain. We disucssed that everything that we're doing is for the benefit of some human being. It might be that it benefits the developer more than the end user. I think it was CSS custom functions where Jeffrey said "if the develoepr has better tools, they can make more good things for the user." If it's not for the benefit of the user, then who is it for? the rest of the conversation focused on the developer. Most of the stuff that we discuss has a much bigger impact on the user.

Someone said last week, "If we could establish that it really doesn't have anything for the user, you can move down the priority of consituencies and evaluate from there"

Hadley: That's fine and roughly what I meant by entioning the priority of constituencies. But if it's a net negative for the constituencies above. E.g. amazing for developers but at the cost of the user. Admit that i haven't looked at the rest of the document, and the rest might take care of my comments.

Lola: Highlight line 106-111, where it re-emphasizes that end users come before authors, so when explaining features designed for authors, prove that end-users aren't harmed. That's pretty strong in advocating for end-user. End-user is the priority, but there are occasions where the feature is for developers. Is that enough?

Matthew: That sounds very good. Wonder if we should put that further up.

Jeffrey: it started sounding like this discussion was saying "close this, and try a different approach", and teh approach i was thinking of was a template for CSS features or security features. But now it sounds like maybe the PR *is* ok, so I'm still looking for direction.

Lola: I think the PR is okay. I think that last paragraph meets Matthew's concerns, and Hadley's. Yes?

Hadley: Probably? I don't have the document in front of me, but I'm all for prominence. 

Matthew: same for me.

Jeffrey: I'll wait for your reviews then. 

### [design-reviews#838: Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola

Lola: No real update; working on comment.

### [process#43: GH issue forms might not be right for design reviews](https://github.com/w3ctag/process/issues/43) - @jyasskin

Jeffrey: wendy Selzer filed this becasue she tried to use the issue forms and ran into a problem. I've filed discussion issues with Github, but no feedback from them. So we can either continue using the forms even with this inconveniece for people who want to review their submission before sending it -- or we can go back to the template.  Or we can wait to make a decision. 

Lola: what's the issue?

Jeffrey: Wendy wanted to file an issue, and wanted to copy it out, collaborate with her working group, and paste it back in. That was easy with the text template, but not with the issue forms. 

we have help sections for the various sections. with the template, it was with superscript charaters etc. With the issue forms, we can put down at least the top level questions. There is another problem with issue forms that you can't produce a hierarchy in the output, but it's significantly better than the old template

Hadley: have we received this feedback from anyone else?

Jeffrey: not yet

Hadley: do we think the benefits will would outweigh the costs?

Jeffrey: I think staying with issue forms would be net beneficial, because the help for people filling them out is somewhat better. the formatting we get on our end is somewhat better

matthew: I would natrually be inclined that having the forms is better, for the reasons that Jeffrey mentioned. I'm curious of how accessible they are, though I know Github is aware of accessibility. What I'm not understanding: surely once you've submitted it, you don't get a chance to preview it, but can't you edit it?

Jeffrey: Yes, but you risk bothering us. We get an email as soon as you submit it. 

matthew: yea, i can appreciate that it would be nice to have a preview. but hte likelyhood of mistakes s reduced because it's a form, i would think

Lola: i'm inclined to agree. Wendy is the only person who has brought it to us. Others may be facing a similar issue. It may just be a workflow that Wendy has? We do know that if others raise it as an issue, we can look at it again.

Jeffrey: I can add to the form "If you have problems with the form, please file an issue over here"

Lola: can you provide both? "Use this template, and then copy your answers into the form when you're ready"

Matthew: good idea

Jeffrey: I think it will be a decent anount of maintenance work, keeping both up

Matthew: a transition period? I see

Lola: i think the form is fine, but collaborating on the answers and making sure everyone is aligned on the content. that's the issue. 

hadley: on transition period: many of the poeple who open issues for us don't do it that often. So i don't kno wthat it would be helpful.

[agree on the comment]


### [design-reviews#1121: WG New Spec: Web Speech API contextual biasing](https://github.com/w3ctag/design-reviews/issues/1121) - @lolaodelola

Lola: yves and i looked at this. it's fine. Are we hapy to close as satisfied?

[Group agrees]

### Triaging new issues on the [Design reviews project board](https://github.com/orgs/w3ctag/projects/6/)




### Prep for the plenary

matthew: some people it is about longpress, and others think it's different... I think we want to ask them more about their views. There is also Xiaocheng's questions on intent.

Jeffrey: I also asked Marcos to be sure to be there. I think we'll have a good dicussion between the proponents and people who have worries. If you have questions for the propenents, I can let them know so they can be ready.


## Breakout C (Europe / Asia / Australia) - [2025-07-31](https://www.timeanddate.com/worldclock/converter.html?iso=20250731T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Xiaocheng, Martin, Ehsan, Lola, Marcos, Matthew, Christian

Regrets: Yves

Scribe: Martin

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

[Issue list](https://github.com/w3ctag/societal-impact-questionnaire/issues)

Lola: Trying to make more time to discuss the documents we're working on.  This is a meta issue.

Lola: What about https://github.com/w3ctag/societal-impact-questionnaire/issues/4 ?  Adding agenda+ tag.

Martin: Two big rocks in AI and centralization.  Might be a case of going off and doing homework.

Marcos: Lots of work being done on this and I'm not sure that there is much we can add.  Atlas of AI does a good job.  Maybe we should look at TAG reviews of APIs (prompting?).  Worried about doing a finding given how much stuff there is already written and how broad the scope of the topic is.  This is beyond our scope.  It expands into many other areas.  Risk of anything we say being not meaningful.

Lola: This is a questionnaire, so it can expand on other stuff and reinforce what already exists, rather than making a new statement in the domain. We don't have the expertise.

Marcos: On WebKit, when we looked at shape detection, the set of tests we were able to put together were pretty narrow.  Test suites (in WPT, even) are limited.  So we could make recommendations about making sure to include more diversity of conditions and subjects.

Lola: Might add agenda+ to centralization as well.  Sarven and I might go away and hack at these.

### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @lolaodelola

Lola: I closed this earlier this week with "satisfied with concerns", mostly because of concerns with SAA generally.

### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Martin: I just need to go and do the work to respond to the review.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://github.com/w3ctag/design-reviews/issues/1120) - @matatk, @xiaochengh

Xiaocheng: Still reading Matt's comment in the brainstorming thread, which is one minute old.
... My concern here is that the design is very centric to the behaviour of Chrome and Firefox and it might not work on Safari.  The proponents also said that they do not expect Safari to implement.  I wonder what this means.  No interoperability?

Martin+Lola: Not really acceptable.

Lola: Anything from Safari on this?

(Tess says that this is not possible.)

Lola: Negative?

Martin: Interop is voluntary, but no point if there is no hope of interoperability.

Marcos: Igalia is implementing on Blink.  Interesting that they didn't see WebKit as a problem.

Christian: This is tough.  The use case (sort of) makes sense.  Interest from implementers.  Not having interoperability is not great.

Lola: There are CSS highlight things going on elsewhere.  Firefox did something in the recent release; Firefox exposes this to a11y, but Chrome doesn't.  Interoperability for this stuff is already called into question.  To have a major browser not be able to implement might make this worse than better.

Matthew: There have been discussions about the semantics of highlights.  This case is separate to those. These do need to be exposed to a11y.  Like to +1 to Christian about the use case and an opportunity to improve a11y.  The proposal might not work, but it is nicely consistent with other highlighting APIs, so it would be nice if it was possible.

Lola: Can we ask that they work with Safari?  So that we get interoperability.  The other highlight isn't necessarily the same feature, but because this is highlights in general, I'm concerned about lack of adoption from developers, because brittle features won't be used.  Also, I'm not won over, just because developers want this.  Need to consider the impact on users being inconsistent or negative.

Martin: That's what we do.

Lola: I'm not in favour of saying satisfied for this reason.

Matthew: We all want the problem solved, but we know that solving the problem would mean no interoperable solution.  The issue that I've linked from my comment talks about Safari.  That might be because their colours are fixed.   Possibly something to do with system colours might provide a way to smooth this out.  Right now we can't say that it needs to happen this way.

Lola: Does that help, Xiaocheng?

Xiaocheng: Are we going to suggest that they investigate other alternatives that are interoperable?  Something like "we acknowledge the value of the use case"...  There are good parts of the proposal.  The consistency with other highlight pseudo-classes.  How many of us thinks we should raise this non-interop  concern.

(Virtually unanimous concerns with interop.)

Xiaocheng: I'll draft a comment with two points: the use case is legit and we like the consistency with existing highlight patterns BUT we don't like that this isn't interoperable.

Martin: What about Safari and the other highlights?  Because if that has shipped, an alternative design here might make it impossible to have consistency across those highlight types, which is unfortunate.


### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Lola: Looked at that this week...

Martin: My view is unsatisfied, simply because there is no spec.  There might be other reasons for that, but I can't tell.

Marcos: Coincidentally, I have the spec text now on a branch.  That fills in most of the blanks.  There is no consensus yet on some of these parts, so these haven't landed in the spec yet.

(Marcos walks through things for https://github.com/w3c-fedid/digital-credentials/pull/306)  That shows a picture of the architecture and the new "coordinator" role within the user agent, which manages access to the wallet.  Then there is the whole formats side of the protocol.  These are somewhat out of scope for the API; these dictate how you interact with different credential formats (mDoc, openID, whatever).  The reason that isn't there is that we are working through the details and the algorithms and trying to reconcile that with implementations.  Lots of reasons for not being satisfied.

Lola: We should hold off until everything is added.  Also, the explainer is not an explainer: that links to the intro section, but the explainer doesn't cover some of things.

Marcos: Alternatives were custom URLs, which is in another document.

Lola: It's not clear.  The explainer is not in our design-review issue.

Marcos: https://github.com/w3c-fedid/digital-credentials/blob/main/explainer.md should cover most of the explainer topics.
... we've been moving stuff from the explainer to the spec as the spec is filled out.  So that things don't get out of date.

Lola: Should we wait?

Martin: I'm still concerned about the formats question, which is far from being resolved.

Matthew: Can wait.

Ehsan: I have an issue related to the no papers document with respect to how the API operates.

Marcos: It would be good to have something about formats to take to the working group.  Even if the API shape is there, the formats would be good to take there.  There is also privacy/security and the working group put in a lot of work recently on that.  Would be good to see if there are things missing and set expectations.

### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Matthew: It's taken me longer to get to this than I'd hoped, but I need to cite sources properly.  What we discussed last week was broadly OK with the rough outline of the proposal.  Will post that before plenary.  Computer replacement took some time.

### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @martinthomson, @matatk, @toreini

Martin: This was presented to us as a fait accompli.  Still a problem with related sites.
Lola: What do we do with review on more than one thing?  The resolution seems to be satisfied for most, but unsatisfied for the related sites thing.
... I would suggest a separate issue for that unsatisfied piece.

### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @ylafon, @marcoscaceres

Marcos: Leaving to yves to post.
Lola: Yves is away.
Marcos: Can post then.

### [design-reviews#1117: Add IndexedDB getAllRecords() method and update getAll()/getAllKeys() to support direction option](https://github.com/w3ctag/design-reviews/issues/1117) - @martinthomson, @christianliebel

(martin) Christian did the work here and I agree that we should just post the review.  The backwards-compatibility story is a bit sketchy, but this is overall good.

### Triage
Discussed activeViewTransitions and PRT work briefly.  No other untriaged work.

## Plenary Session - [2025-07-31](https://www.timeanddate.com/worldclock/converter.html?iso=20250731T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Xiaocheng, Matthew, Jeffrey, Christian, Mason, DanC, Ehsan, Marcos

Regrets: Martin, Yves

Scribe: DanC

### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Guests: Mason Freed, Chris Harrelson, Una Kravets, Penelope McLachlan

Mason:
I will set the stage for some of the things that have been talked about.
Mostly discussed has been touch screen. But most users will be mouse users.
Many production websites use hovered content.

This is an accessibility API. Can do hover-triggered UI with JS today, but this leaves
out keyboard users.

It's also true for hover triggering, keyboard, touchscreen, you can build today in JS.
This was also true in popover. But had a11y issues, stacking issues...fixed with standardization.

This is similar.
Try it on Wikipedia -- they spent lots of time on their hovercards. Try it with a keyboard,
it's not great. E.g. can't close with Esc, can't turn off the gear icon to control them
with keyboard.

Their native app with touchscreen has long-touch mostly implemented as preview, but sometimes
uses the OS behavior.
That's the background.

There are more use-cases.

API is pretty simple. Hoping we can find a way to move past the debate.

Marcos: Is there much to discuss? It's implemented in Webkit and what other engine?

Mason: ONly in Blink.

Marcos: I saw WebKit patches?

Mason: Maybe it was Luke? That would be great news though.

Marcos: Event and attr was landed. Maybe I'm wrong though? But saw patches landed. Looking...

Mason: Luke Warlow?

Jeffrey: Not asking if has been adopted by engines.

Marcos: What I'm getting at is it has a lot of eyes on it.

Mason: It's not shipped anywhere.

Marcos: It's had more eyes than the TAG's on it. I had questions around
the event, similar qualities to longpress...is the event cancelable?

Mason: Yes. Two events, interest and loseinterest, both are cancelable.

Marcos: Doesn't interfere with longpress?

Mason: If you're using touch screen, you show interest by longpressing and choosing
option from context menu. Or with button, no context menu.
With link you get the contextmenu first, we'd add another "Show details" item to the context
menu, which triggers interest.

Marcos: Links are contentious, you'd expect behavior is preview.

Mason: That'll still happen.  This is iOS, with Safari, longpress a link, get 2 things:
preview up top, context menu at bottom. Only change would be the menu has one more item, 
"show details".

Xiaocheng: If you longpress button, triggers text selection, trigger again, contextmenu.

Mason: In Chromium, solved by setting user-select:none on buttons with interestfor.
It's a weird behavior anyway.

Jeffrey: I'm hearing mostly support. Is that right?

Lola: I'd like to hear from Matt and Mason about a11y considerations.
If issues come up with ARIA semantics, does this integrate well with AT use?

Mason: I have open a11y review to make sure of what I'm going to say.
I believe most of the a11y connections come from the popover.
When you set up button and popover today, the right a11y semantics get set up by
the platform.
We'd reuse the same ideas. If there are other things we'd like to know.

Matthew: For the reasons Mason mentioned at start, seems we're moving common pattern
to a more standard place. It's simpler than popover. From a11y perspective we're
crossing t's dotting i's. Overall use case is positive one to move into platform natively.

My recollection of TAG's discussions is there's been broad support. Areas
of concern were about how it affects current UA behavior. You've talked about that already.

Github example is good. We were looking for more examples. Maybe fleshing out those more
to further justify is good idea. But in terms of a11y this seems a win.

Mason: Section at top of explainer covers 10-14 production sites.

Matthew: Haven't looked in a while.

Marcos: Other main concern was whether it interferes with common UI patterns on mobile,
like if it prevented preview. Looking at other things concsidered cancelable, like right
click or paste, frustrating to users. Should be mindful of that when can cancel an event.
Looks like this doesn't interfere.

Mason: That's crux of the touchscreen example. So often broken; sites are face with the
choice of either giving access to context menu or the hovercard. This lets them have both.

Marcos: I get positive aspect, but always unintended side-effects.
Trying to look ahead to those. What might be negatives?

Mason: Assume you're talking mostly about touch screen.

Marcos: In general.

Mason: I think we've mitigated them. Most tricky is touch screen. Were proposing
for a while showing both popover and context menu, and some other ideas...the one we
landed on of adding context menu item feels lowest risk.
I'll mention keyboard too, had more complicated set of behaviors, stripped that out too.
Feels like where we landed is lowest risk.

Marcos: I think one of the original proposals had HTML loading stuff, that's all gone?

Jeffrey: Preloading?

Mason: Was question about speculationrules, whether it interacts with that.
If you're hovering link, should affect how you prefetch?
General feedback was it's unclear. Maybe they're less likely to click if you
show them all the info. So better for dev to control.

Lola: I'm making assumption here. This doesn't increase fingerprinting surface.
Not making changes to links on pages that reveal anything about user.
It's codifying a way for devs to do context previews. No overreaching to make
changes to actual page content or following users through journey.

Mason: That's correct assumption. Don't change anything about how links work.
Interesting bit is revealing their input modality, but that's probably available anyway.
Doesn't show whether they use keyboard or not.

Matthew: That's the go-to could be the bad thing. Reassuring. THe fact the
event fires is fingerprinting risk. But you're not saying how it was triggered, that's
reasonable. Seems like fingerprinting risk is small and being managed.
Classic example: make it so it's not possible to detect AT, but really have ways to check.
Don't think you'll fall into that pitfall because not saying how interest expressed.

Other negative things, trying to think of some. Dev could implement in a way that
causes user surprise, too many dialogs. But can do that now.
"Worst" is b/c of difference between buttons and links, will be difference in how
come to the info in links vs buttons. If only affects touch interfaces, maybe OK.
Inconsistency probably unavoidable.
Interesting general design challenge around discoverability.
Not proposing we somehow highlight all interestable things.
Only thing I can thnk of is surprising user too much, and inconsistency between
buttons and links, but not much can be done about that.

Mason: Broadly agree. One upside with shipping is if websites use it, by browser having
control, we can add a setting to never show interest.

Xiaocheng: re fingerprinting, this reduces fingerprinting surface. Reveals user intent
without revealing actions. For websites to implement same behavior, only listen to this
event instead of caring about mouse vs keyboard focus.

Jeffrey: Don't think we can say it is reducing because the other stuff is still there.
Maybe reduces what's used in practice.

Marcos: Say you're moving around with AT or touch screen. Do roles/landmarks change?
How identified by AT?

Matthew: AT can give hints about stuff. E.g. if you're on something with click handler
can say clickable. The fact these attrs exist, certain semantics and roles will be applied
that AT can pick up on. E.g. already can identify buttons with popups.
AT user might get more info that someone with no AT.

Mason: That's correct. Way it's done is with aria-details, and with an expanded state.

Jeffrey: Other thoughts?

Xiaocheng: I replied in thread with thoughts about generalizing this pattern.
Diverse opinions. Do you want to generalize this pattern?

Mason: I like this idea in spirit. Complicated today because need to consider
all the ways to express interest. There are probably other such patterns to make easier.
Don't want to include all that in this, but I like the idea.
Click is kind of like that today, really means activation.
Another effort could keep going with that.

Marcos: I saw the PR landed in HTML.

Mason: Up for review, not landed.
https://github.com/whatwg/html/pull/11006

\<confirms still open>
Command and commandfor are landing.

Marcos: That answers my question.

Jeffrey: Are we satisfied?

Marcos: Mainly wanted to give foresight of potential badness. Be mindful of that.
Not to be negative about it. All tech gets misued in some way.
Could say that.

Matthew: +1 to Marcos. One thing we could do is ask about details of what device
can be given to devs to use responsibly.
Most of the time with new CSS or HTML stuff, valuable to include rough outline of
what to say to authors. Lots covered in WCAG already. But if they're going to docs
of new feature, helpful to have awareness of new stuff there.

Marcos: Someone like Mason is more likely to catch issues here -- looking at Digital credentials, people think defensively. It's great to paint in positive light, but with
all cool tech, things go bad.

Mason: I agree, open to other things. Have been working on this for >=1 year, found a
lot of those bad things that we took out already.

Matthew: You had alternatives considered in explainer -- it's really useful for people
to know tradeoffs that have been made. Not asking for too much detail because you already have, could talk more about fingerprinting, what could go wrong...heplful for reviewers
and for future reference.

Dan: There was some recent discussion on the design review from Lea about whether this should be combined with `commandfor`.

Matthew: Good question, but I think that was addressed in the explainer.


Mason: It's how we started the API too. But as you pull the thread, find it's not the best
idea. We had lots of discussion in OpenUI. I have strong opinion that it'd be the wrong
thing to do, full of footguns.


Jeffrey: Does proposed closing comment look good?

\<general approval from the room>

Marcos: Don't just throw it on us to find problems -- but comment looks good.

Proposed closing comment:

<blockquote>
  
Thank you for coming to us with this review. We think this is a good feature, and we're looking forward to its addition to the web. We looked, and we think you've looked for ways that this might come back to bite us in the future, and we didn't find any (though we leave it to the WHATWG community to consider). It would be ideal to include that fact in the explainer. We also note that the explainer doesn't have an explicit alternatives considered section, even though you did explore many other options. But overall, we're satisfied with this API.
  
</blockquote>


### F2F planning

Jeffrey: We're in early stages of planning. Have Slack thread on hotel.
Email thread about organizing dev meetup.
Organization offering to host has venue an hour on transit or 20 min car ride away.
Is that reasonable? Or ask Xiaocheng to organize a room in central venue?
Meetups in the past have been hosted there by this organization, but our venue may also work.

Xiaocheng: This place is much more convenient.

Jeffrey: Not hearing big concerns that it'll be hard for us to get there.
So I'll reply that it'll be good to use their space.

Lola: Was thinking about if the meetup is after a day of us having met all day,
that commute might be tiring. But if convenient for devs that's fine. But could
it be towards end of week?

Jeffrey: Haven't talked about which day. Last day doesn't work because people fly out.
But could do Wednesday.
Need to arrange our schedule for dinner, transit.

Marcos: Was going to say same thing, probably doing 20 min car ride for dinner anyway.


Jeffrey: Other question is how to structure F2F.
Historically chairs (none of the current chairs) have broken days into hourlong slots.
Was a script to gather design principals and design review issues, issues from other
findings, have people claim issues, break into brekaouts, do a bunch of tracks.
In Paris instead we did longer sessions based on a couple bigger topics.
Did presentations to introduce topics, broke into discussion groups, came back to make
decisions. Current thinking was to do that again. Which larger topis to address?
I suggest making a label for F2F topic, have people file issues and mark with that.
If that sounds good to people I'll put that label on likely repos.

Hearing agreement, will add to where I think it'll be likely to be used.
People should feel free to add where they want.

Other topics for F2F?


### Breakout escalations

#### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Lola: Matt, you mentioned you'd have carousels comment ready?

Matthew: I can paste what I've got. Want to add citation.
Might need a little bit of work.
Covers the big areas we talked about, need to add link for virtual cursor.
It's here: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/97#issuecomment-3140075595
Not completely done but almost all there.
Each day I make half of the remaining progress :\)


Jeffrey: Cascading attributes issue linked from gap issue.
Is that related to carousel?

Matthew: Might be useful for carousel. Not just the idref thing, also
the imparting roles thing.

Jeffrey: So not quite ready to approve, but people can pay attention.

Matthew: I'll ping in Slack when done.

#### [design-reviews#1111: Declarative Interactions @matatk, @xiaochengh](https://github.com/w3ctag/design-reviews/issues/1111)

Matthew: Animation triggers, with layers of indirection, where's that at?

Xiaocheng: Proponents already answered questions.


### [Issue Prioritization](https://github.com/orgs/w3ctag/projects/6/)



















