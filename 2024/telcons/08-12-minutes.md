# Tag Minutes Doc - Thu, 12 August 2024

## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/08-12-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout B (California / Europe)  - [2024-08-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240812T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

### Breakout D (California / Australia) - [2024-08-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240813T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
* [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss
* [FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974)

### Breakout E (Europe / China) - [2024-08-14](https://www.timeanddate.com/worldclock/converter.html?iso=20240814T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)


* 3p Cookies Finding Feedback from Privacy CG Call
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk
* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @rhiaro, @hadleybeeman

### Plenary Session - [2024-08-14](https://www.timeanddate.com/worldclock/converter.html?iso=20240814T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Call Minutes

### Breakout B (California / Europe)  - [2024-08-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240812T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Matthew, Peter

#### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

Dan: I suggest we close this as the requestor did respond to Lea's feedback and it's been in the abyss since... 

Yves: mozilla standards position was [positive for list of types](https://github.com/mozilla/standards-positions/issues/905)... 

Dan: so tick mark for multi-implementer support...

Dan: Where is happening?

Yves: CSS....

Dan: So shall we close it as **satisfied**?

Peter: seems we're looking at details but I don't have a good understanding of big picture. 

Dan: looking back at original review: https://github.com/w3ctag/design-reviews/issues/748 we said satisfied with concerns.  We did articulate our concerns...

Peter: i agree we gave view transitions a pass but the things they are adding to it seem suspect to me...

Dan: Does it have CSS wg consensus?

Peter: not sure.  ...concerns about list of types...  changes to the javascript APIs... so let's go ahead and close it.

**CLOSED AS SATISFIED**

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

Matthew: some discussion...

Peter: this doesn't make sense to me... seems one way or the other you've got to cache what things .. apply to.   I'll make a comment ... asking that.

Matthew: If we have to have something else other than just a selector, why don't we call it something other than viewtransitionclass - like viewtransitionname - not using the word class.

Peter: I agree - using *class* is confusing ...

Dan: *Support.*

*peter leaves a comment*

Matthew: I do understand that this is a separate concept to viewtransition name... they are trying to do the same thing with css classes and used the same name. that's why they've used the same name... BUT they aren't classes... I appreciate why they want a way to indicate it syntactically... and classes in a concept of CSS is doing the same sort of thing. But this isn't a CSS class so it's tricky. I think this could be a "foot gun" for DX.

Peter: yes I think they are re-using the concept of class... But it's not a class. I don't think they should use the `.` syntax... If that pseudo-element took a name... but I don't think it does. So no reason for the `.`.

Matthew: i think you can do view transition group...

Peter: if that's the case then they do have to distinguish... 

Matthew: according to [the explainer](https://github.com/vmpstr/web-proposals/blob/main/explainers/view-transition-classes.md) - the needed a higher level thing so decided to do "class"...

Peter: in that design, the `.` makes sense... 

Matthew: they address by saying "there is an `*`"... 

Peter: don't need a `*`... but they say in the background... 1-7... why can't it just be "list item 1, list item 2, " etc...

Matthew: shall we ask them?

Peter: *[posts comment](https://github.com/w3ctag/design-reviews/issues/938#issuecomment-2284511391)*

Matthew: +1

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Matthew: need more time - but a couple of thoughts... the problem is definitely one that needs solving. Broken up into different phases. First phase solves a simpler part of the problem which looks good. They want feedback on phase 1. looks promising. Phase 2 looks well thought out but is complex. They reference other proposals and I don't know if those proposals are ongoing or were shelved... I also noticed that it's moved... it was in AOM and now it's in Web Components... So I'm figuring out what that means... also it would be good to ask people who develop ATs what they think...  It looks well thought out...

Matthew: *will leave some feedback*

#### [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

Peter: there is a lot of commonality with cross-origin... e.g. manifest IDs... a lot of these features in the same origin case seem to be tied into cross origin... 

Dan: feels like same origin API should be the less contraversial and simpler thing...

Peter: .. i think certain things (like IDs) are in there to support the cross-origin cases. So why have an ID separate from the URL? Why not just the URL of the webapp?  You're giving the URL of the webapp you's installing... so don't see what the ID does. The reason for having the ID in the API is when you're installing an app that doesn't have a manifest... so having that ID is only useful in the appstore context.

Dan: Having an ID ... unique ID ... that is extraneous to the URL for the APP... is adding developer complexity... 

Peter: I'm ok with being OK with this API but pushing back on "why the ID"?

<blockquote>

Hi @diekus we discussed on today's call. One thing we are not clear on is the need for the separate ID in the case of same origin installation. Are there other cases, not related to app store cases, that would require a separate ID (separate from the URL to the webapp itself)?  Otherwise it seems like this could be simplified (and thereby reduce developer complexity) by removing the need for a separate ID?

</blockquote>

Dan: *[leaves comment](https://github.com/w3ctag/design-reviews/issues/888#issuecomment-2284547460)*
  
### Breakout D (California / Australia) - [2024-08-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240813T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present:

#### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

#### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

#### [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss

#### [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss

#### [FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974)

### Breakout E (Europe / China) - [2024-08-14](https://www.timeanddate.com/worldclock/converter.html?iso=20240814T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present:

#### 3p Cookies Finding Feedback from Privacy CG Call

Matthew: *channeling feedback from the privacy CG call* The two most important things about the finding are: there is broad agreeement with it, specifically with the ways we've discussed evolving the finding document. That brings it closer to where people would like to see it go. E.g. documenting the use cases. Martin's PR goes in the right direction. If we had a list of use cases / developing solutions, that would solve a lot of the feedback we got. We're in a similar place to most people it just wasn't 100% clear to them. That's good news. It was interesting to see that some people hadn't quite picked that up and others had and were chiming in with support. Minutes haven't been published yet. *Someone* working for an IDP, they specifically were saying about "good" and "bad" uses for 3p cookies. We aren't sayng they can't be used for good things. They would like to see the TAG distinguish. I don't think we see it that way. We're saying "they are so easy to abuse that there aren't really 'good' third party cookies" - that we would prefer people move to specific APIs for these use cases. We should be trying to replace them even though some/most people are not abusing them... There are some industries we regard as being high tech - and they have to use technology but they have extremely low margins. So you can understand the reticence to move to something else if it's not going to improve things that are important to them.

Dan: Payment use cases can be a good example of that.

Matthew: issue : we don't actually know what the browser is doing... with heuristics...

Dan: I want to enumerate these use cases and be specific about them... and put them into [the issue](https://github.com/w3ctag/web-without-3p-cookies/issues/30).

Matthew: agreed. Part 2 is more concerning to me. We've talked about the tension between domain-specific APIs that are high level and low-level infrastructure APIs... In case of cookies ... a spectrum of support for specific high level API and then the middle ground of things like chips and storage access API... Those are things about improving what we've got. On the other other side of the spectrum you've got replacing cookies with something very similar (but more secure) aka Shared Storage. So I think we have a challenge - if we feel the way the platform needs to go is to more problem-specific solutions then we have a lot of convincing to do...

Dan: I think it's also related to our past support for the "extensible web" way of thinking... which was to build low level APIs and build on top of them...  I do think that's still appropriate in some domains... But what we're trying to articulate with this fidning is that maybe in the privacy domain - since the low level APIs bring with them a specific harm - it's not appropriate. Expsosing low level networking primitives could be another example. So it's nuanced. Maybe we need something in the design principles that cannonizes this.

Matthew: one of the use cases might be "general"... D

Dan: just noting that we did return an unsatisfied review on shared storage: https://github.com/w3ctag/design-reviews/issues/747

Dan: maybe in tomorrow's plenary we can merge Martin's PR as a start?

*discussion on single sign on*

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: I reached out to Diego to ask him to help clarify whether 👍 means "yes" to our proposal. If so, I suggest we close this as satisfied at the *plenary*.

#### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

Matthew: they respinded... with information. We asked for the explainer to be update to contrast this spec with other one - render capacity. They did update the explainer.  They added info on the side channel stuff. Looked at rate limitations mitigations... We've raised it with them, they are looking into it.  With respect to the difference between the 2 APIs, they've added something that addresses that.  So they are different APIs - although could have the same impact (reduce complexity or ask user to close other apps to free up resources). So they've done what we've asked and documented it fairly clearly. I think it'd be good to get others' views. But render capacity is on pause. So it's not like we have these 2 things active at the same time.

Dan: What's the multi-implementer story?

Matthew: according to chrome status no info from anyone... but we established they are talking with the audio working group.

Dan: if we return a positive review we should couch it in terms of "yes, please take this to the audio working group." 

Matthew: I think if Tess also thinks they are different enough then we should give it a positive review.

Dan: *sets to proposed close* let's talk about it at the **plenary**.

#### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

#### [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk

Matthew: looked at the proposed API - the way that you show or hide the button is by adding or removing an event handler for it... Fine... Assume that's consistent with other stuff... judging as it's part of media session... It looks like from this that the appearance of the button is UA controlled. So that removes one avenue for a11y issues .. if the user agent is rendering the button then the responsibility for a11y is on the user agent.  The one thing I didn't yet determine is how to get to a PiP window with the keyboard... If you can't then that's a bigger problem... it does need to be keyboard accessible.  Will try it out.   Peter raised the point : should it be on the platform because it admits advertising as a business model for the platform... there isn't a position from mozilla. I'm reading a bit of pushback from webkit... 

Dan: can you leave some feedback on the issue? We could also ask if this could be generalised .. Considering we generally don't have ad-specific APIs then maybe we could ask them to generalize this?

Dan: leaves [comment](https://github.com/w3ctag/design-reviews/issues/957#issuecomment-2288097776)



#### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @rhiaro, @hadleybeeman


### Plenary Session - [2024-08-14](https://www.timeanddate.com/worldclock/converter.html?iso=20240814T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Matthew, Martin, Hadley, Amy

#### Breakout Rollup

#### Breakout E topics

##### Merge https://github.com/w3ctag/web-without-3p-cookies/pull/26 ?

##### Close https://github.com/w3ctag/design-reviews/issues/875 ?

##### Close https://github.com/w3ctag/design-reviews/issues/939 ?

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
