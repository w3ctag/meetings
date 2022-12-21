# TAG Minutes Doc - Mon, 19 December 2022

## Call Agenda

### Breakout A (Europe / US) - [2022-12-19](https://www.timeanddate.com/worldclock/converter.html?iso=20221219T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [CR Request for WAI-Adapt: Symbols Module](https://github.com/w3c/transitions/issues/478) - @ylafon
  * related to https://github.com/w3ctag/design-reviews/issues/476 and https://www.w3.org/2022/09/13-apa-minutes.html#t01
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2022-12-20](https://www.timeanddate.com/worldclock/converter.html?iso=20221220T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia, @rhiaro
* [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro
* [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon
* Privacy Specs Document


### Plenary Session - [2022-12-21](https://www.timeanddate.com/worldclock/converter.html?iso=20221221T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780) - @hober, @torgo, @hadleybeeman, @plinss
* [Design and specification review of CSS Container Queries Style Features](https://github.com/w3ctag/design-reviews/issues/787) - @LeaVerou
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Breakout A (Europe / US) - [2022-12-19](https://www.timeanddate.com/worldclock/converter.html?iso=20221219T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Yves, Lea, Tess
Regrets: Amy, Hadley, Rossen

### [CR Request for WAI-Adapt: Symbols Module](https://github.com/w3c/transitions/issues/478) - @ylafon
  * related to https://github.com/w3ctag/design-reviews/issues/476 and https://www.w3.org/2022/09/13-apa-minutes.html#t01

Yves: APA got a review for personalization document... they got a review from the TAG .. last TPAC... meeting with Rossen... we told them they didn't proceed with the comment we sent. Blocking their CR.  In the comment Rossen said the "symbos were loooking good".  So they've published that as a CR despite lack of clarity from the TAG... We need to respond to the CR request.  Either we say "it's ok - publish it" or "please we need to do a proper review".  

*Dan leaves message for Rossen we can come back to it at the plenary or breakout C*

### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

Tess: if factory method has landed ind esign principles.. then we should let them knpw - but beyond that we should keep waiting...

Peter: they did open an issue about the constructor argument... as I recall we didn't have an issue with them as a factory method...

Lea: *looking through thread* we're asking why it's a factory method on that class... 

Peter: they opened an issue in [whatwg issue 1110](https://github.com/whatwg/dom/issues/1110) - some pushback from Domenic.

Peter: i have mixed feelings... the original task of adding a new factory method - i'm fine with that.  We had some suggestions about making it developer friendly.. common use case would be to use it with another abort signal. We had pushback from Domenic ... So is there a design principle we can pull out of this?  We should either accept and document what Domenic's principle is or have a counter argument.

*Domenic's comment https://github.com/whatwg/dom/issues/1110#issuecomment-1242811392 in the WhatWG issue*

Lea: he's making multiple claims... differnet parts of the web platforn.. also discussion on `AbortController` ... he needs to file design principles issues about these.

<blockquote>
Hi @domenic,

We looked at this again today.
On the linked WHATWG issue you've [made the comment](https://github.com/whatwg/dom/issues/1110#issuecomment-1242811392):

> I think this proposal is a bad idea and would be poor API design. The constructor of an object should vend its fundamental capabilities. It should not provide a syntactic shortcut for saving an extra line of setup, by connecting the constructed object to a totally different part of the web platform. (In this case, the event loop and timer subsystem.)
> 
> Furthermore, `AbortController`s created in this way are harder to reason about. They have a hidden, implicit caller of `abort()`, which you cannot see. You have to know that whoever created it, hid such a call from you in the constructor. You can no longer scan for all `abort()` calls to find all ways the controller might be aborted.
> 
> I don't think we have evidence that the use case in question (roughly, creating an `AbortController` that is controlled by both a timeout and other callers) is very popular. And if we did, I don't think we have evidence that being explicit, using `setTimeout()`, is a huge burden. (Note that `AbortSignal.any()` is not actually needed, you can do `const controller = new AbortController(); setTimeout(() => controller.abort(), 5000);` and then pass `controller` onward.)
> 
> I hope we keep the `AbortController` constructor simple and focused on its core capabilities. Any syntactic sugar should continue to be done at the `AbortSignal` level, like we've done with `AbortSignal.timeout()` and like we're proposing to do with `AbortSignal.any()`. Static factory methods there both avoid messing up the API construct of the controller's constructor, and can pull their own weight by saving more than a single extra line (since they abstract away the entire `AbortController` object).

There are several design principles implicitly assumed in this message, and we'd like to discuss them separately, because we may or may not agree, and in any case it's good to get the benefit of a documented discussion that is separate from this particular issue. 

For example, things like:

- "The constructor of an object should not provide a syntactic shortcut for saving an extra line of setup"
- "It should not [connect] the constructed object to a totally different part of the web platform. (In this case, the event loop and timer subsystem.)"
- That having a hidden implicit call to `abort()` is a bad idea — why?
</blockquote>

*support from Peter, Tess, Dan*

Lea: *leaves comment*

Dan: we can bring this back to the **plenary** too... 

### Meta: *discussion on what to do when issues are not updated - issue openers don't engage in the issue*

Dan: should we close it and let them know they should re-open?

Lea: I'm fine pushing it to another milestone - but we should have a standard policy.. and outline that somewhere... "we're gonna bump it for this many months"

Dan: Also : that we expect them to engage in the issue ...

Dan: update needed to https://tag.w3.org/workmode/

Dan: I can do a PR.

Peter: I do agree there's a problem with people opening a TAG review... making closing issues algorithmic shouldn't be an option - there should be humans in the loop.  In some cases things might need to be open for a year... we need to make sure there's always a human in the loop.

Dan: +1

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Tess: looks like they filed a couple of issues based on Lea's feedback.. one of them is closed and the other hasn't had comments...

Dan: [parsing Domenic's response](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1336649923) - yes the complexity is the http header - requring server configuration... I'll make that clear.

### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

### [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Peter: one of thos sync / async / flush style... I don't think we can advance until Houdini work has been done.

### [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Dan: Webkit "[support](https://github.com/WebKit/standards-positions/issues/74#issuecomment-1344405135)" as of Dec 21.

Peter: I have concerns over top layer...

Lea: same... Maybe we should close and say "satisfied with concerns"?

Peter: I'm not happy with that - who is defining top layer and where is that happening?

Rossen: in the fullscreen spec?  https://fullscreen.spec.whatwg.org/#top-layer

Peter: i'm not happy with top layer being defined without participation of the CSS wg.

Rossen: curious if we have it reflected anywhere?

Peter: they're monkey-patching CSS and not involving CSS wg in the design.

Lea: yes, agree.

Peter: i don't think it's been discussed in CSS wg... but I don't recall a serious conversation about what it is...

Dan: maybe ask Chris H. in our issue?

Dan: *bumps to early Jan*

### [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

Lea: we talked aout developer complexity -- jake wants to have a call - we haven't scheduled it yet. 

*dan reschedules for week of jan-9 and Lea will try to set up call with Jake before then*

### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

### [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo

*we agreed to close*

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia


## Breakout C (APAC / Europe) - [2022-12-20](https://www.timeanddate.com/worldclock/converter.html?iso=20221220T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Yves
Regrets: Sangwhan

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

Amy: they have a paper - [analysis of cross-site reidentification risk](https://github.com/patcg-individual-drafts/topics/blob/main/topics_analysis.pdf)... not sure if it's up to date with their latest changes. It's great that they did it, but would be preferable to see this sort of an analysis from someoen independant.

Amy: appreciate the work that's gone into this... but also ...

Dan: *noting it's Google Research and Chrome people - no outside contributors*

Dan: in a world where the topics api is the only way to do any kind of targeted advertising that is not only contextual, this would be a net positive over where we are now. 

Amy: *noting user control and how much control the user has over it*

Dan: considering this would only be used for ads, and further targeting ads, the person would have the option of using a browser that does not ship the topics api and therefore self select...

Amy: unless they detect the api is not implemented and refuse to serve a page in that browser, then we have fragmentation - they have mitigations against some ways to detect if the user has disabled the api or is in incognito mode (empty array returned)  - but don't know what happens in the case where the browser hasn't implemented it at all... 

Dan: if the behaviour is the same in incog mode as a user who has disabled it, that should not be detectable

Amy: but if a browser hasn't implemented it at all, would you still get an empty array or would you get an error?

Dan: writes comment..

<blockquote>
Hi @jkarlin thanks for this. We discussed in [breakout today](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/12-19-agenda.md). One concern we have is the risk that publishers might try to detect whether the user is using a browser with the topics API loaded / enabled and attempt to deny service if the API is not implemented. This is a similar issue what was discussed in your response to the security & privacy questionnaire for the API's behaviour in incognito mode. In both cases it feels like the result should be that the publisher should not be able to tell whether the topics API is disabled/not implemented. Is this the case?
</blockquote>

Amy: then there's the whole Dmarti issue about centralizing power in larger publishers...

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

*bumped to plenary*

### [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman

Amy: danbri replied to say it's fine. I think we can close this.

Dan: agreed

Amy: [closing comment](https://github.com/w3ctag/design-reviews/issues/758#issuecomment-1359003548)

**closed**

### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Amy: they haven't responded...

*bumped to next year*

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia, @rhiaro

*bumped to next year*

### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro

Dan: there's an [explainer](https://github.com/a-sully/fs/blob/6abfb840112d137c22fbf0fb986471dfe63a89fc/Remove.md) now...

Amy: I left a comment with concerns ... I don't think they've addressed that. Also no security & privacy ... There's a security considerations and mentioned recursive directory removal is "already possible" .. I want to believe they've thought about the footgun implications of this. Overall it's probably fine. 

Dan: there's a gecko positive link, but it's just to a comment from Anne not an actual standards position

Amy: Does seem like it might be problematic if it's inconsistently implemented between browsers though

Dan: will ask if there's a mozilla standards position

Amy: their "developer: positive" is an issue with 3 comments on it.

Amy: in the explainer they haven't really expressed it in terms of user needs. But it's a bigger concern if only one browser implements this, as developers will need to right multiple code paths anyway, so it doesn't solve the problem they are trying to solve

Amy: we need feedback from Sangwhan, Lea...

*Bring to plenary*

### [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon

Yves: goal was to close with concerns or unsatisfied. The IETF group in charge of URLs should discuss it.

Dan: I don't think we're satisfied

Yves: we voiced our concerns and we would like those to be discussed in an ietf group

Dan: I also dont' think we can say unsatisfied... ambivalent or out of scope?

Yves: ambivalent would be better, but clearly we need more stakeholder support as well. Browsers indicated they didn't want to implement it.

Dan: so it should be unsatisfied.

Yves: this still shouldn't be a blocker - ietf might find a way that will work.

<blockquote>
Hi folks - We've expressed some concerns about the current proposal especially around the use of '%' as a delimiter.  Also it seems there is lack of implementer support, which is a concern to us.  Hence we're going to close this one with an "unsatisfied" label.  Our suggestion is that discussion should continue at the IETF, with the group in charge of RFC3986.  We look forward to hearing from you again when these issues have been resolved.
</blockquote>

Dan: *cloeses and leaves comment*

### Privacy Specs Document

Amy: [committing draft privacy doc to reviews repo](https://github.com/w3ctag/design-reviews/blob/main/reviews/web_without_3p_cookies.md)



## Plenary Session - [2022-12-21](https://www.timeanddate.com/worldclock/converter.html?iso=20221221T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Yves, Dan, Rossen, Peter, Lea
Regrets: Hadley


### [CR Request for WAI-Adapt: Symbols Module](https://github.com/w3c/transitions/issues/478) - @ylafon
  * related to https://github.com/w3ctag/design-reviews/issues/476 and https://www.w3.org/2022/09/13-apa-minutes.html#t01

Yves: *reviews state*

Yves: they didn't have a proper OK from the TAG or we need to tell them we need more time to review.

Rossen: the version that they linked is on July 26...  Looking at [this](https://raw.githack.com/w3c/adapt/CR-content-2022-07-26/snapshot/CRD-adapt-content-20220726.html#action-explanation)... 

Yves: And [here](https://raw.githack.com/w3c/adapt/CR-symbols/snapshots/symbols/Overview.html)

Rossen: all makes sense... 

Dan: there was a meeting at TPAC - Rossen you gave feedback - was that applied?

Rossen: in their initial proposal many ... the feedback that was given was that the initial set of attributes were too many... some expressable and close to CSS some of them ... the one that was straightforward was symbols... they took the spec and stripped out everything except the symbols... They're motivated to publish this.

Dan: so we're good.

Rossen: yes.

Rossen: *will leave a sign-off comment*

### [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

### [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780) - @hober, @torgo, @hadleybeeman, @plinss

### [Design and specification review of CSS Container Queries Style Features](https://github.com/w3ctag/design-reviews/issues/787) - @LeaVerou

Lea: can we close this?  There were no objections in the design review async chat we had. 

Rossen: I like the explainer.

Lea: not a new feature - it's extending container queries which [we have reviewed](https://github.com/w3ctag/design-reviews/issues/592) before.  No signals form gecko or webkit...  No response to the standards positions requests...

Rossen: from TAG's PoV I feel this is definitely the right way to go about this feature.  

Peter: I agree I don't think there are any architectural issues... 

Dan: Lea can you write a closing comment?

Lea: Can write that the comment I wrote reflects our consensus. 

*consensus: yes*

### Breakout Rollup

Dan: on Topics API - *gives summary* also Anne has come back [with a webkit position](https://github.com/WebKit/standards-positions/issues/111#issuecomment-1359609317) that is not favourable. 

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
