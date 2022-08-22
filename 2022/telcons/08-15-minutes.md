# Minutes Doc

Week of 15-aug-2022

## Agendas

### Breakout A (Europe / US) - [2022-08-15](https://www.timeanddate.com/worldclock/converter.html?iso=20220815T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
* [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov
* [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss
* [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

### Breakout C (APAC / Europe) - [2022-08-16](https://www.timeanddate.com/worldclock/converter.html?iso=20220816T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Privacy Sandbox Doc Discussion
  * [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
  * [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
  * [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
  * [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @hadleybeeman, @atanassov
* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

### Plenary Session - [2022-08-17](https://www.timeanddate.com/worldclock/converter.html?iso=20220817T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Logistics

Chair: Dan

Scribe:

## Minutes

### Breakout A (Europe / US) - [2022-08-15](https://www.timeanddate.com/worldclock/converter.html?iso=20220815T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Tess, Peter, Lea, Rossen, Hadley
Regrets:

#### [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov

Peter: I think we did not get to this at the f2f. Chrome is shipping.

Lea: didn't we recommend they have a picker instead? How is this different?

Peter: originally they had an api that enumerates all the fonts - we pushed back and said do a picker. They came back with a picker that is multi select and makes it easy for the user to pick all the fonts on the system. They wanted to expoxe open type metrics, we said how about being format agnostic. They said here's a blob with all the data, you parse it. They say they have a use case for raw font data for libraries. Acceptable for give me a blob of font 2, but I suspect they are focussing on one use case and aren't looking at bigger picture. Suspect authors want to be able to get some metadata without bringing in a big font parsing library.

Rossen: they don't seem very receptive to our feedback. For private browsing mode point they say ack but they won't do anything about it. Less than great. Given how much fonts are used for tracking I don't now about making this explicitly available will improve anything.

Tess: over the course of this review - a couple of years - we've filed a bunch of issues on their repo, at least 6, more, and at least 3 are still open. The ones that are still open feel pretty foundational to me. I'm not terribly enthused with the charging full speed ahead while leaving those things unaddressed

Dan: sounds like not satisfied - level of engagement, taken our issues seriously, and moving forward with major points unresolved

Amy: and not satisfied with adding an api that increases fingerprinting?

Dan: +1

Tess: there are some hardliners who don't want to add any more bits at all and that's not as nuanced as it needs to be. There are some APIs that are incredibly beneficial that adds some fingerprinting, let's do it. But in this case getting interesting font data for a specific font is potentially many interesting bits of fingerprinting, so the benefit has to be proportionally massive to justify that. We're working with a theoretical privacy budget of 31 bits or whatever before you're done, that's a small number of bits, this could blow right past that.

Rossen: how is allowing the file upload in incognito the same as exposing specific fonts on the system or elsewhere?

Dan: it's not, it's a total red herring

Rossen: they're saying that.. exposure of specific fonts seem comparable. I don't see how that is the case.

Tess: \<devil's advocate\> let me make the argument for a second.. file upload dialogue, I pick something unique from my filesystem, game over. Also a thing I can do with a filepicker is go to wherever the os keeps the fonts and pick the font file and upload that. If there's a specialised api that only lets you get at the font data, that's a strict subset of what the file dialogue can do.\<\/devil's advocate\>

Rossen: one is an explicit user action where I go and choose a bunch of stuff. The other is a function someone wrote running on my system selecting fonts and sending them to somewhere else...

Tess: I think that's why that argument doesn't hold water. From the user perspective they're totally different things.

Dan: *writing "unsatisfied" closing post*

Tess: Anne wrote issue - the crux ofthe matter - we need to be deliberate as stewards of the web platform about the question of how do we represent fonts. We need to specify that really well and not just punt to common file formats. That's a lot of work. I understand they're reluctant. But without serious thought about what is an abstraction that fits the use cases that we can code to so we're not dependant on file format details, that we're future-proofed, would go a long way to mitigate the privacy concern as well. The way that a specific opentype font got expressed into that platform abstraction could be done in a way that hid the sensitive stuff and let through the glyph information they need or whatever it is. That's a lot of spec work. The timelines that we do work on the web platform need to be long term.

Peter: I think they are focussed on enabling certain functionality and not thinking about the overall state of the web

Tess: it's our job to comment on that

Amy: could we be more strong about it being harmful?

Peter: I'd be okay with that

Dan: I don't think it would help

Tess: I like your comment as drafted. I don't think we need to say more about that.

<blockquote>

Hi folks. The issues as we see them so far:
  
  1. there are a number of unresolved issues which have been raised during the course of this review (e.g. [#19](https://github.com/WICG/local-font-access/issues/19), [#20](https://github.com/WICG/local-font-access/issues/20), [#62](https://github.com/WICG/local-font-access/issues/62), etc.)
  2. the fingerprinting risk is quite large here. There's always a tradeoff to be made regarding fingerprinting surface area and new functionality - however in our view the high risk is not comensurate with the benefit in this case.
  3. the API seems to be on a trajectory to ship regardless of our feedback and the other negative feedback surfaced on this issue.

In conclusion: we think we should be more deliberate as stewards of the web platform in terms of how we represent fonts.  We don't think this is the right approach to solve these use cases in the context of the wider web.
  
</blockquote>

Rossen: [posts comment](https://github.com/w3ctag/design-reviews/issues/400#issuecomment-1215333348)

#### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

**closed as timed out** 

#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Dan: requester has responded to Lea's comment and indicated that .. I asked for some clarification, sounds good to me.

Lea: one of my issues is that we should have identified a problem but we weren't necessarily saying this is the solution, but that the issue needs to be addressed. I'm not sure what we proposed is a good solution, just something we came up with on a call. But sounds like they want to go with it. The crux of our feedback is they need to think about this problem, not here's how to fix it.

Dan: they seem to be receptive to the idea of fixing the problem. We could close the issue and say satisfied with concerns and say thanks for being receiptive, to be clear we want to encourage you to think about this problem and implement a solution that makes sense for you, please don't simply take our idea without discussion.

Lea: sounds great

Rossen: mixed .. loading different resources, potentially different fonts.. no answer to that. Answer in March was the query will evaluate however media queries evaluate. I get that. I don't get then what happens? Do you restyle the page? Or not?

Peter: the response does seem to be reload everything, not just continue in mixed mode.

Rossen: that's clear. Now I'm going back and forth between cell towers so my page is reloading every time I do that...

Peter: suggestion was you flip one way and never flip back. If they take that suggestion it's not an issue. I agree with you Lea, I'm not saying they should just do that.

Lea: it was not that you never flip back, it was that you only flip from high to low but not from low to high.

Rossen: don't understand. If I'm not able to see netflix in high res why wouldn't I flip from lower to high

Lea: it's not necessarily a good idea, that's my whole point! Not necessarily what should be implemented, I don't lik that they're going to run with it.

Dan: we shouldn't be coming up with a solution for them.. Close with concerns?

Rossen: problem is it's a very simple API that exposes holes with something we've been poking since the begining of the reivew. None of the feedback we provided seems to stick in a spec that makes for better user experience. But we want to rush and close it?

Dan: I'm not pushing to close. Agree we should be going for higher quality. Let's not close it if that's not right.

Peter: my suggestion is we ask them to re-open or ping us when they have a solution

Rossen: in which case I think we should make the closing resolution stronger than just 'with concerns'. 

Lea: since they seem to be willing to work in it isn't our usual process to leave it open pending feedback? They can come back and tell us the change they made. Doesn't seem en par with our usual process to close and say reopen it. 

Dan: let's leave a comment along those lines - we really think you need to come back with a solution and document it in the explainer

<blockquote>
  
Thanks for being receptive to our feedback. To be clear we want to encourage you to think about this problem and implement a solution that makes sense for you, please don't simply take our idea without discussion. We look forward to hearing what you come up with - please document it in your explainer and let us know.
  
  
</blockquote>

#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

Dan: did say it's a big chunk of work

Lea: seem to remember this wouldn't happen async

Dan: schedule a separate call for it?

Peter: no response to my comment, but it was more bigger picture concerns

Dan: concerned with state.

Peter: this is all about state

Dan: can we get dbaron to join us for a special session? We talked about issues with people using this as a state preservation mechanism. They haven't responded. Maybe we should reach out for a discussion.

Peter: happy with that. Feels like something that should be discussed more within the CSS WG.

Dan: that's another option. We can give them parameters of discussion.

Lea: I've heard that Chrome plans to ship this. They feel it will help with a lot of pain points for developers.

Dan: Let's get David on the call and have more back and forth

Lea: that would be great

Dan: who else should we invite?

Lea: Maybe Tab and Miriam?

[scheduling - start at half past Breakout A next week]

#### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
#### [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov
#### [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov

Dan: Peter left a message.. can we close?

Peter: they haven't really responded, we got a reply from someone else. We pushed back saying doesn't this just help advertisers keep abusing users. They have not answered that.



#### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
#### [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss
#### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

### Breakout C (APAC / Europe) - [2022-08-16](https://www.timeanddate.com/worldclock/converter.html?iso=20220816T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Max
Regrets: Lea

#### Privacy Sandbox Doc Discussion
  * [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
  * [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
  * [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
  * [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @hadleybeeman, @atanassov
  
**On topic of larger document**

Hadley: we do need to be able to talk about each spec on their own merit. The main reason to do a document is that informative presentation where they talked about big picture motivation. Feels like a lot of our feedback in our debrief was concernsa bout big picture, concerns about trying to preserve targeted advertising, the overarching narrative separately to specific concerns about how each of the pieces work. Useful to put that in something that we could refer to in each of the separate discussions.

Amy: we could progress the ones that are less controversial, and refer back to a document for the more challenging ones if we need to rationalise the review status for them

Hadley: vocally encouraging the move away from 3rd party cookies - we should do it - it may be disruptive to some people.  Some parts of the community may disagree. But I don't think that's a reason not to do it.

Amy: We don't have to represent consensus of everyone on the internet.

Amy: Do we want to ack the pushpack against the concept of 1st and 3rd party?  

Dan: I think we should reinforce the concept - it's an architectural plank. People getting confused about 1p and 3p by talking about 2p or 5p.. it's not that kind of thing. We need to be clear about that. Maybe wording in the privacy principles doc we can align with.

Hadley: agree. A big part of our pushback to first party sets was that it was redefining what a 1st party is. Helps to be able to point to something with a definition everyone is using and why it's so damaging.

Sangwhan: we should probably reinforce that concept

Amy: I'd like to see notes / thoughts from everyone and I can try to turn it into a consolidated text

**On CHIPS**

Amy: the [PR](https://github.com/WICG/CHIPS/pull/44) removes references to FPS. 

Dan: can we progress this review separately? And make the point in our document that there are things coming out of privacy sandbox with wider support

Hadley: makes sense

Sangwhan: CHIPS is fine

Amy: removed dependency on FPS was our last blocker. Feedback from PrivacyCG about positive support for other implementers

Sangwhan: we can say that in our closing comment

Hadley: bigger question about how developers will adopt it. They were saying once they get rid of 3p cookies this is going to be the most attractive option for advertisers. Also about whether it's a step back for Safari and other browsers. Meta concern about browser buy in.

Amy: [note about other browser support](https://github.com/privacycg/proposals/issues/30#issuecomment-1113257336)

Dan: proposed closing comment -

<blockquote>

Hi @krgovind, we're happy to see the update to the explainer which removes the dependency on First Party Sets.  This was the key blocking issue in our view.  It's good to see this proposal has good [traction from implementers](https://github.com/privacycg/proposals/issues/30#issuecomment-1113257336).  We remain concerned about how/why developers will take this up - we understand this will depend on the deprecation of third party cookies, which we welcome.  The TAG view is that this proposal will improve privacy on the Web.
  
</blockquote>

Hadley: not better in the context of non-tracking ads..

Sangwhan: nothing to do with advertising

Dan: this fixes a problem with cookies, rather not mention advertising

Hadley: we might regret not making this point here...

Amy: there *are* non-adv use cases for chips.

Hadley: happy.

#### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
#### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

### Plenary Session - [2022-08-17](https://www.timeanddate.com/worldclock/converter.html?iso=20220817T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Rossen, Peter, Hadley, Amy, Lea,
Regrets:

#### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

...[reviewing explainer](https://github.com/WICG/shared-element-transitions/blob/main/explainer.md)...

Dan: is this designed in the right way to enable the UX they want to enable. Inevitably we'll have to get into the question of could there be leakage between two different documents in a way that violates privacy or breaks web security.

Dan: noting that this is purely for same-origin transitions and that cross-origin transitions aren't part of the proposal; additionally there are some noted security considerations.

Dan: reviewing the [s&p questionnaire responses](https://github.com/WICG/shared-element-transitions/blob/main/security-privacy-questionnaire.md); looks good as long as it's confined to same origin. Cross-origin will be trickier and will require more thought.  We should note that in the review response.

Dan: note other things to take into account if it was cross-origin, so we should note our response is purely in the context of same-origin

Lea: from an API point of view, do you understand how to use it? as an author? 

Peter: I don't entirely follow the design

Lea: it's a very thoroughly written explainer... but I don't get it.

Hadley: doesn't have use cases from a user flow perspective

Lea: I think there are many use cases, but I don't understand how to use this to get them to work

Rossen: if you look at the default setup and how it's used in the customisation of an animation I think it's pretty easy to follow. You set up your animation as a property bag that you transition through, then execute it in the context of the new document. Querstion - if you have a log running animation, not sure what type of effect would that have? Your property value is going to be kept alive for the duration fo that animation, as stated in the section for ending the transition. Other than that it sems straightforwad.

Lea: how low level is it? Right now with CSS transitions and animations it's a significant problem that authors cannot animnate between auto and other numbers. If a container has auto dimensions in both documents can you still animate between them?

Rossen: nothing changing on the basis of this of what values are animateable. Exactly the same behaviour as any other in-page animation or transition. Intent is not to extend that. That is one of the non-goals. Not precluding that in the future.

Lea: if you use this by default you get a crossfade, and everything else is a customisation from there? That's cool.

Dan: Hadley, you mentioned you didn't think there's enough initial discussion of use cases?

Hadley: I understood they're trying to make transitions more seamless?

Rossen: the use cases are well articulated. Preamble.. different design language currently being useed in native platforms and how they benefit native applications in their transitions

... author of one page wants to fade their content out... keeping the load going in the new destination and then can kick off the animation and give you a nice transition.

Hadley: that's helpful - addresses my concerns...

Lea: if you're using an app on a phone for ex, you get these transitions - but you don't get these on the web in multi-page web applications so this can bridge that gap... 

Dan: or people are forced to create SPAs in order to achieve this effect. Ideally they'd be multi-page, which would fit bitter with web architecture. Individually addressable pages. One thing that aids my understanding of it is that it's sprinkled with videos and images which help to reinforce what they're talking about

Lea: still some questions- the explainer mentions you use a `prepare()` method with a callback. In the example it updates the dom somehow. 

Rossen: This is the time when you have the ability to handshake between the two states - and add additional state into your new environment.  What they're doing: they are highlighting the fact you can use the same for both - for in-pave and between-page?  Happy to look further.

Dan: I'm generally concerned about complexity, although maybe this is inevitable

Lea: I don't know..

Rossen: every time you try to create a pattern that's intended to transfer a state from one navigation to another - privacy securty, etc... - and make it execute into that new context you're going to have a set of complexity... Is it the simplest way of doing it? Not sure. On the surface when I read the explainer it didn't seem overly complex compared to the goals they're trying to achive.

Lea: if we feel it would be useful Jake could join a call... 

Rossen: ...could be helpful...

Lea: hesitant to say let's move forward because I don't feel I understand it well enough. But also the use cases are very important and need solving. 

Rossen: We want to do a good job of proving good reviews.... We could say we had a good initial discussion where we validated the use cases but for examople I haven't validated what it means for accessibility - certain live regions on the new document that may be covered with other content. Other one is the privacy - which is mitigated by it being same origin. Next logical step is how do we make it work for cross origin. Don't want it to be carried forward to cross-origin.  They already have some experimental implementation.  My suggestion would be to load up one of their examples and get a feel for it.  

Dan: Agree with Rossen. I don't think we need to bring Jake onto a call given our schedule. We should be able to accomplish some additional work with him or the requestors async. Would it be possible Lea to leave some comments on the thread asking the questions that you have? One thing that does strike me [... misse d a bit...] there's some more example text in the spec, but it's not exactly what I'm talking about, maybe that doesn't exist

Peter: I remember a tweet from Jake linking to some demos, but can't find it

Dan: we could ask him

Peter: I know he has these resources. He can probably link us.

Lea: Might be easier to wrap our heads around it if we have a presentation

Hadley: separate call?

Dan: let's ask some questions, then decide if we want to bring someone in

Lea: there are code samples without visuals.. I'm having trouble connecting code samples with the output

Dan: yes

Lea: some are more clear. The customisation of animations section is the most clear one. That is what got me to understand. But animating width and height shows a nice animation. What is the code that produces that animation? How do you get that kind of effect? I don't understand.

Rossen: transition both the width and height properties into 100%

Lea: that is not the only thing that is happening there

Dan: under that one there's a link that says this is relatively easy...

Lea: [clicks link]. Before formulating questions I need to spend more time in case there are links with answers.. I want to respect the time they spent writing that.

Dan: there's a lot of links to a chrome developer document from about a year ago which ... should be in the explainer

Lea: I can ask about examples more tied to animations

Peter: let's just ask Jake if he has more concise code, then look at that then decide. Agree with Lea, obviously a lot of effort went in. But as I go through this there's a lot of handwaving and presumptions of knowledge which is not necessarily clearly laid out in the explainer. Big chunks I'm missing. Not seeing.. to me a lot of the design of this feels weird. I accept that it's probably necessary, but why the design turned out this way and the reasons is not explained either

Lea: yeah, there must be something we're missing..

Peter: some shared knowledge that is not being expressed

Dan: maybe we need to ask them to write down more explicitly use cases.. they are expressing use cases, but I'm not sure.. sentence about ...

Rossen: what if you ask Jake to provide .. to pick any two examples and provide the end to end code. 

#### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo


* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

