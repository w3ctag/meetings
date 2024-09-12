# TAG Minutes - week of 09-September-2024

## Agendas

### Breakout B (California / Europe)  - [2024-09-09](https://www.timeanddate.com/worldclock/converter.html?iso=20240909T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk
* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman
* [Vibration API](https://github.com/w3ctag/design-reviews/issues/971) - @martinthomson, @torgo, @matatk

### Breakout D (California / Australia) - [2024-09-10](https://www.timeanddate.com/worldclock/converter.html?iso=20240910T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Design Review: Prioritized Task Scheduling (big picture)](https://github.com/w3ctag/design-reviews/issues/967) - @hober, @martinthomson
* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion
* [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk

### Breakout E (Europe / China) - [2024-09-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240911T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @martinthomson, @LeaVerou
* [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou, @nitot
* [WebXR Device API (delta/aiming 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/983) - @torgo

### Plenary Session - [2024-09-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240912T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
  * Actions taken
    * Closed/satisfied with Speculation rules: target_hint field
  * Pending Plenary decision
    * Entry and Exit animations
    * View Transition Classes 
    * Early TAG review request for Playout Statistics API for WebAudio 
    * Web Install API - Cross-Origin 
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout B (California / Europe)  - [2024-09-09](https://www.timeanddate.com/worldclock/converter.html?iso=20240909T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tess, Jeffrey, Yves, Hadley, Amy

Regrets: Lea, Matthew


#### Ethical Principles

*we discuss the formal objection and whether it could be possibly be downgraded .. in any case it feels like we can make the requested changes.*

*we discuss and agree with BBC's proposed changes*

*noting that comment close tomorrow*

Hadley: the 2nd point from the Centre For Accessibility Australia folks - i agree with the text they propose but not their logic for getting there, so... let's go with the change they suggest. But I wouldn't want to pit misinformation against state censorship, or to get into the position of choosing which is worse. But the proposed rewording is fine from my PoV.

Amy: also +1.

#### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

Jeffrey: It's been a long time .. it's in "interop 2024"... agreement between 3 browser engines to focus on interop on certain features... no arch issues raised. Dbaron mentioned offline that he's not happy with some details but that's something CSS wg can focus on. so Nothing for us to do here.

Dan: I'm happy with that... 

Dan: let's check with Lea before closing - we can close at *plenary*.

Yves: also - the issues raised in CSS wg for that were closed...

<blockquote>

We see that the browsers have agreed to focus on implementing these features as part of [Interop 2024](https://wpt.fyi/interop-2024). While some of the details may still not be optimal, we don't think there are any architectural concerns, and we think the CSSWG is the right place to continue refining the design, if necessary. Thank you for bringing us this review!

</blockquote>

**Closed as satisfied** at plenary

#### [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo

Tess: looks like ... jeffrey asked some questions ... could mark as pending ex feedback?

Jeffrey: I'm assuming they will say it's gonna take a year...  Totally possible it will be a constraint for webkit and mozilla also ... only concern I saw is maybe this shows that mozilla is right ... to use anchor tags...

Tess: I think micro-syntax ... knee-jerk reaction is .. we won't need it.

Jeffrey: moz's approach is to design a different micro-syntax... Not obviously better. The comment might be 'please keep working with moz to see what the right syntax is'.

Tess: that would work for me.  We could close it now...

Jeffrey: this is a real small tweak to bigger pre-rendering issue.

Tess: this has arch implications because it's redundantly specifying...

<blockquote>

Please keep working with Mozilla to figure out the right syntax for this, especially whether the need for `target` information reinforces their preference to re-use &lt;a> elements. Beyond that, we don't see any architectural issues and (ignoring any worries about the underlying feature) are `satisfied` with this extension.
  
</blockquote>

**We agree to close.**
  
#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

*we need Peter*

Dan: let's revist at **plenary**.

#### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

Tess: both martin and matthew had thoughts and I think they were answered satisfactorily... I think we'd like a better explainer... I'd be unformfortale with closing without matthew and martin...

Dan: let's try to close at **plenary**.

#### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

*we discuss how this is related to [Ethical Web Principle issue 120](https://github.com/w3ctag/ethical-web-principles/issues/120)*

*we discuss the security characteristcs of apps and how web inherently doesn't need this*

*we discuss the discoverability use cases*

*given that the discoverability use case is the key one, is it enough the warrant to the added complexity / potential security issues*

Jeffrey: there is the security argument - some web sites are malicious and will trick you into entering your credit card - safe browsing is the thing... user's browser will block sites... a store might do a better job. this API doesn't allow the store to do the better job...  One defence for this if it improves security - and it doesn't. This is not a discoverability mechanism... but without it, there is an "extra click". That sounds like a rel attribute to me, "please install this", and then the browser can decide whether or not to do it.

Tess: yes exactly...  One counter-argument - why it's an API... a rel attribute value is not gated by user activation... you can cause the link to be followed from script. But the browser could tell and only do the special thing if activation is observed... 

Dan: It would be declarative that way....  So yeah... Maybe this would be a good idea?

Tess: rel="install"

Dan: there's another goal, the 'app store' to know whether I've installed it or not and provide a different UX if so

Tess: right now we allow a visual distinction between visited and unvisited links, and sites cannot detect visited link styling so they can't tell if you've gone there or not. There's ane xisting mechanism for us to do something different for different kinds of links on the page. The browser could know. Different pages which link to the same app should not know that I instaslled it from somewhere else. But arguement to expose it to the original page

Dan: other goals - they want to track the fact you installed and report back

Tess: it's clear a rel="install" doesn't get you everything that the API gets you. We could do a styling thing to visually distinguis (I don't think it's a good idea). Tradeoffs. If a rel="install" gets you 80% of what you want simply and declarative

Dan: wondering if [web app scope extensions](https://github.com/w3ctag/design-reviews/issues/875) could help in some way. Same people. Bidirectional agreement between origins. If we say we don't think they should be able to do cross origin installation, but if they used this declarative appraoch and there was a bidirectional agreement between the parties. You could do that out of band.

Tess: something in the web manifest, which is more or less what they already had. Also `rev`.

Dan: if I follow a link that says rel="install" because of the referer header it will know where the link came from.

Tess: you don't even need to rely on that. If you want to require an opt in what you would probably do is just fetch the manifest immediately. Could prefetch the manifest for every link on the page

Dan: a way to achieve all their goals without building a whole new api

Tess: it doesn't handle the payment and conversion tracking cases. In the same origin case .. in safari and macos you can add to dock any website. User doesn't care about the manifest. Weird disconnect between same origin and cross origin. Cross origin requires a bunch of infrastructure. There's an arguement for it, but if yo've already adopted the same origin install api on your own site and someone reaches out to include the app.. the hoops to do that are a lot. A rel install wouldn't require those extra hoops.. it's a bonus, but..

Dan: The browser is going to that place where the app is, which it needs to do anyway. The delivery of the code is not centralised.

Tess: the UI flow in the browser for a rel install could be streamlined; a double opt in from both sides. If there's no opt in the browser might get more in your face to the user about whether they want to do it.

Jeffrey: will write notes into issue. We may want to invite them to talk to us directly.

Proposed comment: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/27#issuecomment-2339370537


#### [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk

Jeffrey: this has been supported by all 3 browsers... sounded like reasonable support ... generalizing media chapter might be a way to go in the future... 

Dan: let's close it...

Jeffrey: I think we need to file the issue on some relevant repo [Yves: https://github.com/w3c/mediasession/issues/] so it doesn't get lost...

Dan: adds it to **D** agenda and marks as proposed-close.

Martin opened https://github.com/w3c/mediasession/issues/340

#### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman

Jeffrey: they replied to a couple aspects of it... they replied to the [issue I raised](https://github.com/w3c/controller-document/issues/94) on their repo...  I can discuss with them, but should I take questions back to the TAG?

Hadley: fine with that... if you want TAG backup you're welcome to back to us...

Amy: +1 - yes i clicked through to their minutes... reviewing...

#### [Vibration API](https://github.com/w3ctag/design-reviews/issues/971) - @martinthomson, @torgo, @matatk



### Breakout D (California / Australia) - [2024-09-10](https://www.timeanddate.com/worldclock/converter.html?iso=20240910T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Jeffrey, Peter, Martin, Tess, Scott Haseley (Guest from Google to discuss Task Scheduling)

#### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

[We sent them a question that hasn't been answered yet, so skipping this week.]

#### [Design Review: Prioritized Task Scheduling (big picture)](https://github.com/w3ctag/design-reviews/issues/967) - @hober, @martinthomson

Martin: Naming discussion seems to be ongoing. 

Scott Haseley: "render" is the only piece that's still up in the air. Noam threw out other ideas. Maybe pursue "render" as an argument to "yield". You're yielding but also waiting for rendering. Last comment was that there's another use case where you want high-priority rendering updates, which might benefit site performance. I'm not convinced we should couple those, but it made sense to experiment. Developers were happy with "yield". TAG reviews had asked for the bigger picture. Some pieces are far along, but "render" is fairly early, although some folks are interested. Might bring this up at TPAC in WHATWG/WebPerf.

Tess: Is the intent that ends up in WHATWG specs? Is it along the WHATWG Stages process?

Scott: Not yet. Had offline conversations with Anne. Didn't hear objections, but nothing formal has started. Goal is to integrate it into WHATWG: HTML and DOM.

Tess: Worth getting into the WHATWG Stages process sooner than later. TAG is elected, while WHATWG has the expertise.

Scott: There was activity from Anne and Ollie when we asked for standards positions. But +1 on moving to WHATWG.

Martin: 3 threads: 
  1. yield, which you think is far along and is a candidate for WHATWG. 
  2. "render" question: I'm convinced that it's good to have it as a central part of the API. I want a replacement for `requestAnimationFrame()`. Integrate the entire thing, don't just work around the one pole. See if the pole shoudl stay or you need to build something else. Request rendering and react to rendering. I'm equally convinced that the "render" spelling isn't right.
  3. This is framework for other parts of the platform. When fetch or another async process wants to put something back into the event loop, they need a framework. That needs more thinking. You won't necessarily build an API for that, but you'll build a framework.
  
Scott: Prioritization for (3)?

Martin: Yes.

Tess: Like Fetch defines a JS API but also spec hooks, this needs to provide spec hooks.

Martin: Don't expect anything earth-shattering, but need hooks.

Scott: Thought about hooking into Fetch and Message Channels, in the explainer.

Martin: This is one of the m ore useful/fundamental pieces of work that's happened recently. You don't think of setTimeout() because it works, and it's almost enough.

Scott: Yep, until they're not. Like when people use MessageChannel to send a message to themselves.

Scott: Like hooking into rAF, there's overhead. 

Tess: We should capture this on the issue.

Scott: If things come up, should I just file an issue?

Tess: Yes.

Peter: Also a Discussions area.

<blockquote>
  
  Thanks for doing this work.  We see three general threads to this work, each of which are at a different stage, but all of which are worthwhile.
  
  1. The work around basic task scheduling APIs, (`yield` and `wait` or whatever those end up being called).  This is good stuff.  We'd encourage you to take this to WHATWG and get that into their process now.  Aside from maybe that open naming issue, it is pretty solid.
  
  2. The work around `render` and `requestAnimationFrame`, which deals with how the event loop interacts with the rendering process.  That seems less well formed, but still quite important, perhaps even more important than the first item.  Having a firm understanding of that interaction and clear means of controlling it would be a significant contribution to stability and performance of sites.  We'd encourage you to continue that work to understand that.  Please, don't feel constrained by how `requestAnimationFrame` is; if there are ways in which that could be improved and integrated into a more comprehensive scheduling system, that would be excellent.
  
  3. A general set of hooks that other APIs might use for scheduling work on the main event loop.  To give an analogy, Fetch has an API for fetching stuff, but it also has a bunch of hooks that any other API can use if they need to obtain connections or resources.  That's a useful contribution here also.  For message channels or Fetch or WebRTC or whatever, the ability to schedule and prioritize work will be very useful.  That aspect too needs work, but that can be taken to WHATWG also.
  
</blockquote>

#### [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @martinthomson
*suggest we close this : see convo in breakout B*

Martin to file the relevant issue and **close** this.

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

Yesterday's breakout thought this could be closed, but needed to go through Peter first.

Peter: I had more thoughts that I wanted to throw into the issue, so I'd like some more time.

Peter: They're associating things with content, but CSS already has selectors for that. Using the same name for different concepts is concerning. Have to assign the names with selectors anyway, so why aren't we using selectors? If we need indirection, there are other ways we do that in CSS. Don't see the need.

Jeffrey: Has this gone through the CSSWG?

Peter: Think so, but I haven't been following there. My read on this seems to be so they can capture what transitions apply when content go away. But I think that's an implementation detail. There's a problem that the content's gone so selectors won't match. But the content's gone, so the associating selectors won't match either. So you had to capture them somehow; use that again.

Peter: Also concerned about how they're using a pseudo-element tree to define the transition. But that's completely separate from this issue.

Martin: I share the concerns about the indirection layers. Noam points out that we need some sort of indirection thing to avoid error-prone cases. Using a class at a layer down doesn't help. Building a document tree before and after. Need to say which things are the "same", and apply a transition. Selecting those things is currently new identifiers, but applied using selectors. So just use selectors. The work will be in articulating that more clearly.

Jeffrey: Should we invite the proponents to this breakout? [No, Noam's in Europe; Breakout B.]

Peter: CSS also has some techniques for grids, which we could re-use.

Martin: Find some time at TPAC? 

Jeffrey: I'll raise that with the proponents.

#### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

Tess: If we think this is a bad idea, we should lead and trail with "this isn't a great idea", but we can include advice in between.

[Missed some minutes]

Tess: There are lots of things app stores do. Do they make sense as separate APIs? We should try to tease apart the use cases, and evaluate each one.

Tess: If we encourage them at all, are we doing them a disservice?

Martin: It's not them who gets the disservice. It's what it does to the web.

Jeffrey: Note that https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/WebInstall/explainer_cross_domain.md#non-goals includes several of Tess's orthogonal pieces.

Martin to draft a new proposed comment in https://github.com/w3ctag/design-reviews-private-brainstorming/issues/27.

### Breakout E (Europe / China) - [2024-09-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240911T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: matthew, martin, yves, amy, tristan, dan
Regrets: max

#### Read-out from Breakouts B & D?

Martin: we discussed web install cross-origin and did not resolve... Jeffrey would like to steer the direction in a more positive one - a few things suggested around harm minimization...  But [I'd like] to say "don't do that" first.  It seems like the folks driving this aren't inclined to listen... Would prefer a much stronger don't do that.  A lot of these things can be achieved by having the store that links to a page on the site that will install the application. The one additional click that that would require is a cost but it comes with benefits. That's my position. If you go with the don't-do-this approach it would be better. The declarative approach would be an improvement.

#### Privacy and Ethical Principles Statements Progress

*we discuss the current state, post polls...*

*dan files PR on Ethical Web Principles to address the Centre For Accessibility Australia proposal https://github.com/w3ctag/ethical-web-principles/pull/135*

#### [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @martinthomson, @LeaVerou

Martin: I think this is *satisfied* but there is a need for greater coordination across the platform for how color is handled... The CSS area is more advanced with color spaces, the media pipeline is more advanced with HDR. They're not talking to each other.

Yves: name might not be right ... because it's doing a conversion to RGB... instead of just copying to something...

> Thanks for giving this opportunity to review this work.  We see this as a useful addition to the platform.
>
> We do observe that there is a lot of uncoordinated work on color across the platform.  Our understanding of the situation is that CSS is quite advanced with its work on color spaces and the media pipeline (video and so forth) is more advanced with high dynamic range content.  Having a uniform platform-wide would be desirable and we'd encourage you to engage with CSS folks on the subject to have that happen. You might consider proposing a [TPAC session](https://github.com/w3c/tpac2024-breakouts/issues) on this topic?
>
> We do think that the name is a little misleading here as the "copy" part of the operation isn't the most important aspect; it's the conversion or transform that is the important action.  Is this something that warrants a new API?  `copyTo` looks to be relatively new, is it possible to choose a better name?
>
> Finally, from a process perspective, we'd strongly encourage you to take this work to the Media Working Group repo rather than sitting in someone's private GitHub account.
>
> Either way, this work looks like a useful contribution, so we're closing this as `satisfied with concerns`.

**No objections** and **posted**

#### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk

Matthew: thoughts... first of all they [responded positively](https://github.com/w3ctag/design-reviews/issues/954#issuecomment-2340918041) - that's good.  They posted a blog and some of this should have been in the explainer... would have answered some of our questions. One thing clatified is that they are doing occlusion - you will only get a video stream of that element (not occlusions). They also address the issue whether you should be able to share a particular element... didn't address something that might be off-screen. They do address the transparency... Also with respect to the API shape, we had a question - starting with the TAB and then drilling down - the reason they started that way - (1) it leands on existing infra for permissions and (2) that it sets expeections about what could be shared. I'm torn on it because I see what they're saying but it feels like extra work.

Dan: notes lack of multi-implementer support.

Matthew: one other thing - they said they did consider the alternative we suggested but there is no alternatives suggested in the explainer...

Martin: this is better than the original version but didn't address the concerns that Mozilla had... And I would like to have that discussion (about viewportcapture).  I think the right thing would be to ask for the explainer to be updated... then we can move on to the next step.

*matthew to ask them to update the explainer and ask about off-screen elements*

*[Matthew's posted comment](https://github.com/w3ctag/design-reviews/issues/954#issuecomment-2344584220)*

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Matthew: ... interesting ... the central problem they are trying to solve is one that's been there for a long time - 2 phases - i didn't see anything concerning with the first part - i haven't given the 2nd part enough of a review. This particular thing they are trying to do is straightforward and good. But the point Jeffrey raises is interesting... we need to be somewhat careful. It sounded like Jeffrey's idea was to have more discussion...

*defer to plenary where we can have Jeffrey*

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Martin: this was an early design review - they are going off and updating the spec. I think our involvement should end. We should ask them "when you're done, come back."

Dan: sounds reasonable to me.

Martin: because it's an early review... 

***Closed as "validated"***

#### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou, @nitot

*let's bring to the plenary*

#### [WebXR Device API (delta/aiming 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/983) - @torgo

*let's bring to plenary and if not by next week*

### Plenary Session - [2024-09-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240912T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tess, Jeffrey, Max, Martin, Amy, Hadley, [half way] Matthew, Peter, Yves

Regrets:

#### Breakout Rollup

#### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

JeffreyL: we were waiting on a plenary discussion but Lea thumbs-upped it.

Dan: can we close based on the text we wrote above?

**closed**

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938)

Jeffrey: we will discuss at TPAC (lots of time zones to coordinate on this one; Lea and Peter have reservations)

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Jeffrey: I don't want tod elay anything with that comment.
If they found a way forward for any part of it then they should take that path, to make progress.

Jeffrey: we should review phase ii but we should also approve phase i.

*jeffrey to write comment*

#### [Cross-Origin Install](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/27)

Martin: we had a discussion last session... we came to the conclusion that we didn't particularly like the overall proposal... some "don't do that" some "i think it can be fixed". I wrote something up... Jeffrey contributed.

Dan: I'd like to be more conciliatory but 

Hadley: i'd like us to be, but this topic keeps coming up... what we put on record should be clear and decisive.

*jeffrey to leave the comment and then we will schedule follow-up discussions*

#### Ethical Web & Privacy Principles Statement Review

*we review this [PR](https://github.com/w3ctag/ethical-web-principles/pull/135) to address the australia accessibility proposal*



#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

https://github.com/w3ctag/design-reviews/issues/989

Martin: action is probably nothing...

https://github.com/w3ctag/design-reviews/issues/990

Jeffrey: i asked some questions... I'd like to wait for answers to those before we review...

Martin: jeffrey's concerns are good.. don't see how this one works

https://github.com/w3ctag/design-reviews/issues/991

Martin: ... summarizer engines ... 

Tess: if summarizers make up stuff that is not true...  then how does it fit with our misinformatiom principle...

Matthew: namespace issue...
