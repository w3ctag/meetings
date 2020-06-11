## TAG Teleconference
##### 08-12 June 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-06-08](https://www.timeanddate.com/worldclock/converter.html?iso=20200608T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Same-Origin iframe document-access limiting attribute](https://github.com/w3ctag/design-reviews/issues/397) - @hober, @kenchris
* [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris
* [HTML Modules](https://github.com/w3ctag/design-reviews/issues/334) - @cynthia, @dbaron, @kenchris

#### Breakout B (US / APAC) - [2020-06-08](https://www.timeanddate.com/worldclock/converter.html?iso=20200608T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @plinss
* [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @alice, @hadleybeeman
* [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

#### Breakout C (APAC / Europe) - [2020-06-09](https://www.timeanddate.com/worldclock/converter.html?iso=20200609T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Cookie Store API ](https://github.com/w3ctag/design-reviews/issues/469) - @torgo, @kenchris
* [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon
* [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @alice, @torgo, @kenchris, @plinss

#### Plenary Session - [2020-06-10](https://www.timeanddate.com/worldclock/converter.html?iso=20200610T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Screen Capture API (2019)](https://github.com/w3ctag/design-reviews/issues/440) - @torgo, @hadleybeeman
* [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris
* https://github.com/w3ctag/process/pulls
* Breakout Rollup
* Issue Triage

-----

### Breakout A

Present: Tess, Peter, Rossen, Yves

Regrets: Kenneth, Dan

#### [Same-Origin iframe document-access limiting attribute](https://github.com/w3ctag/design-reviews/issues/397) - @hober, @kenchris

Tess: Ken had back/forth with the filer over the past few weeks.

Peter: Since Ken's been involved with this so far we should push this over to next week.

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris

Tess: Neither David nor I have looked at this since the f2f, hence no progress.

Peter: We can push this to next week.

#### [HTML Modules](https://github.com/w3ctag/design-reviews/issues/334) - @cynthia, @dbaron, @kenchris

Tess: I think we should just close this. Work on HTML modules is pending on the issues TC39 is working on, ES module attributes I think was the name. 
We should close for now with a note to come back once ready. 

Rossen: All modules or HTML only?

Tess: We're talking about HTML modules at the moment.

Rossen: Right, but there's no reason to keep CSS and JSON modules if this one closes. 

Tess: They're both already closed.

Peter: I'm fine closing with the note.

Tess: Great, I'll write the note.

#### Other business

David: I think there may be a number of issues from the vf2f that aren't assigned to milestones. 

Peter: Sounds good, I'll go ahead and go through making sure they do. We have 23 issues without milestones.

Tess: If anyone wants to review these PRs that'd be great: https://github.com/w3ctag/process/pulls

### Breakout B

Present: Peter, Tess, Alice, Rossen, David

Regrets: Sangwhan

#### [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @plinss

Tess: Looked at this in Wellington... 

Peter: It was pending feedback, but we got some feedback.

Rossen: seems like they made quite a few updates.

Tess: Certainly seems like all issues were addressed, that's good.

(pausing for further investigation)

#### [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @alice, @hadleybeeman

Tess: I vaguely recall briefly looking at this at the f2f... possibly with David.

... Seemed like changes weren't that large. But we missed their deadline of Jan 16th.

... Might be worth checking in with them whether they still want us to look at it.

David: Looks like the ED is marked January 20, 2020, but the CR is the previous revision. 

... So maybe they didn't go to CR.

Peter: They requested review because it's a process requirement, but expected that we would have little interest.

Tess: I'd like to check in with Hadley to see if this would be something she'd be up to. Seems like this isn't a high priority/timely review any more.

... I'll ping Hadley, let's push this out by a month.

Peter: There's an "add module framework" commit - that seems worth digging into

Rossen: "Defining animatable style..." also looks interesting, but it's just handling a ??? condition.

#### [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

Alice: The one major issue is involving sending a lot of boilerplate content. Ex. shadow DOM content being created by UA compared to custom element needs to "hydrate". They imagine the shadow DOM content (inside the template) will be different every time. Suggested they find out if this is really true. Mason asked how they would go about finding it out. Ans: we don't know. 

Peter: Seems like it wouldn't be hard to create a hybrid approach with custom element inside template.

Alice: Having nested shadow DOM is a problem because IDs can't be used from the light DOM. Also, what happens if you define a template shadow root and have the contents of it be referenced by another template that hasn't been processed yet. That's a pretty odd use of idref.

... Then Tess had a question about closed shadow roots. 

Tess: Response was - it's impossible, which is good. It be great if they make it clear in the explainer.

Alice: Serialization of closed shadow root from outside. 

Tess: If you get `foo.innerHTML`, and foo's child bar has a closed shadow tree, I thought that `foo.innerHTML` would include that. In their reply they said it wouldn't.

Peter: it is bad if it does serialize.

Alice: If you do server side rendering you'll have access to all shadow roots. 

Peter: If you do `element.innerHTML` you'll get no shadow roots unless you pass the parameter asking about it. So the server can generate a document that contains the closed shadow roots.
... Is there a security implication of the server side being able to fetch() and get all closed shadow root?

Tess: It is as possible as before, so nothing new should be possible.

Alice: `<template shadowroot="open" shadowrootdelegatesfocus>`, we thought this was odd from usage point of view if there will be more options to `attachShadow()`. Proposed use of token list e.g. `shadowrootoptions="delegatesfocus anotherbool someotherbool"`. The response was that ... slot assignment and we have to have all the bool parameters as one parameter and the rest as different attributes. 
... I'm inclined to say that since there aren't any other arguments, it's a bit premature to suggest combining the other non-existent things.

Tess: SGTM

Peter: The only other way would be serializing to JSON etc.

Tess: At this point we really [shouldn't be adding new microsyntaxes to HTML](https://github.com/w3ctag/design-principles/issues/213).

Alice: Last issue is - not allowing streaming into shadow root contents. Anything that has the style of `<my-app>` with a shadow root, nothing will show up until the entire document is parsed.
... (reading issue response). Bottom line, it's more difficult the implement. Once we see if/how this is causing issues to users there could be an option added allowing streaming. It seems quite reasonable to me.

Peter: Right, but it seems this will push even more complexity to the users.

David: What would be broken if implementations could do it either way and let it be a quality of implementation issue?

Peter: Guessing, one issue is scripts can be broken. 

Alice: WRT pushing complexity to author, we can say they should think about adding the option now.

Tess: A little concerned about implementations that don't allow streaming, what would be net effect - error, silent error, nothing...?

Alice: What other options are there?

Tess: What if we have a flag for the not-streaming case? Want to preserve the default of streaming case being unmarked.

Peter: If streaming is something that you need to opt into, what happens if that's downloaded by a browser that doesn't support it?

Alice: That's where feature detection comes into play right.

Peter: I think Tess' point is worth exploring. 

Alice: The problem is now framed better - 1. adding an option for it is adding work to authors while this option had to be default. 2. since this is coming later, can we make it detectable and handle it gracefully.

Peter: Well it could be done now if you define the feature from the get go but be explicit that implementations will be adding this later.

Alice: How do you detect it? Make it a readonly property?

Peter: That could work. 
... If this is going to be eventually streamable it would be nice for authors to write the code that will be streamable now.

Rossen: I think adding future-proofing and pretending that streaming is there from the get go is more problematic than not having the feature now at all and evolving it later.

Alice: So the advice is - please think carefully about the additional complexity down the road that would be pushed to authors and possibly implementation (for those implementing from scratch). They should looking into how difficult is to have streaming by default now and if the opposite justifies the additional complexity in the future. 

Peter: This is a bigger concern to me because without streaming this is blocking until you load the entire page and that degrades the overall, default experience of users.

Alice: So the proposal is stream but have some way of fallback.

### Breakout C

Present: Alice, Kenneth, Dan, Yves, Sangwhan

Regrets:

#### [Cookie Store API ](https://github.com/w3ctag/design-reviews/issues/469) - @torgo, @kenchris

Kenneth: Seems like they implemented my previous suggestions.

... Added some other options..? Disallow required dictionary, no required fields.

Dan: They're saying that they're looking at the clear cookies issue, created an issue on their repo to track it.

... If appropriate, maybe we can add their issue to our tracker and close the review issue.

... Setting to propose close, and will add the issue to our tracker once I remember how.

Yves: I can help with that.

#### [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon

Yves: Same issue as the widget URL scheme previously.

... New URL scheme raises a lot of issues. 
... Discussion going on on their repo.
... Need to realise the new URL scheme has a heavy cost. Can regular URL scheme give them what they want, using a manifest? What about media type?

Dan: Where is that feedback coming from?

Yves: Marcos has given some feedback. Currently discussed in their issue, linked from our repo.

Dan: Should the TAG have an official position on this?

Yves: We have already given that feedback...

Dan: Do we need to reinforce that? Noting that we have consensus on that view?

Sangwhan: I can leave a comment.

Dan: Need to be clear about feedback which represents consensus opinion.

... Let's chat in the plenary to make sure we have that consensus.

#### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @alice, @torgo, @kenchris, @plinss

Alice: I unassigned myself, since I've never commented.

Ken: No update since we asked for updates.

Sangwhan: Not sure how this would work on non-Windows OSes.

Ken: Definitely for desktop OSes.

Dan: Could work for DeX, windowing system for Android. Lets you use your phone like a desktop.

Sangwhan: I seem to recall this is wonky on macOS. Most apps fake the Mac window bar.

Dan: Should we bump this to the plenary to get some feedback from Rossen and Tess, respectively?

#### The AB issue on elected member communications

[will discuss in plenary]

#### Triaging

##### https://github.com/w3ctag/design-reviews/issues/514 - 

##### https://github.com/w3ctag/design-reviews/issues/519 

[discussing "disabled" attribute]

### Plenary Session

Present: Peter, Dan, Kenneth, Tess, Rossen, David, Alice, Yves

Regrets: Hadley, Sangwhan

#### Readouts?

Tess: breakout A - talked about html modules issue...  we hadn't looked since the f2f. we pushed both out a week. on html modules, we closed it.  [closes]  we also talked about PRs from the f2f.

Tess: breakout B - screen enumeration - had marked pending ext feedback, and we got some feedback and it looks good but no conclusion. TTML2 - we talked about it and it's assigned to Hadley and Tess. I'm gonna ping Hadley and see if she wants to look at it in the next month.  talked about declarative shadow DOM.  Stuck on the design decision around streaming... way that it works relative to other elements is weird.  we gave feedback, they replied... rough consensus was that streaming should be the default. feature detection issues... we didn't make a concrete proposal yet.

Alice: I left a comment.

Ken: breakout C - cookie store API - we gave feedback - they responded to feedback and made changes.  [consensus to close].  

Dan: discussed miniapps

David: do we want to have a plenary discussion about this with Sangwhan?

Dan: let's try to schedule it - 

Ken: window control overlay - no feedback yet - i pointed them to some related work ... so far no update. 

Rossen: I am following up with them. She said also they did talk to [MS] security team and they came up with some spoofing mitigation options.  They are working on this with security folks.

#### Issue Triage

[Triaged a number of issues. Did not minute the triage discussion.]

#### [Screen Capture API (2019)](https://github.com/w3ctag/design-reviews/issues/440) - @torgo, @hadleybeeman

Dan: We're done. They've taken our feedback into account. I think that's it. [closed]

#### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris

Tess: I asked them some questions, and I pulled a colleague in. They've since replied to our questions but I haven't had a chance to wrap my head around this thread since.

David: It's also interesting because of the connection to Digital Goods API.  The use case for this is really a separate spec that probably brings up more issues to think about.

Tess: push this out a week?

#### Process PR: [Update 'setting-up-github-repositories' to use GitHub Actions.](https://github.com/w3ctag/process/pull/13)

[merged]

#### Process PR: [Add text explaining how to start a new Bikeshed document.](https://github.com/w3ctag/process/pull/14)

David: points out a to-do for doing the same for respec

Tess: filed https://github.com/w3ctag/process/issues/17 as a follow-up

[merged]

#### Process PR: [Briefly explain what this repository is.](https://github.com/w3ctag/process/pull/15)

[merged]

#### Process PR: [Import the guide for new TAG members.](https://github.com/w3ctag/process/pull/16)

Tess: so we can remove the unused tagdocs repo

[merged]

#### Self-check PR: [Revise questions 2.1, 2.2, and 2.3 for ease of understanding.](https://github.com/w3ctag/security-questionnaire/pull/90)

Tess: trying to shorten, simplify, make document more accessible.  Don't think we can land it but please look at this change...

Dan: be sensitive that this is joint 

Tess: yes - absolutely

[agreement to review and discuss later]


