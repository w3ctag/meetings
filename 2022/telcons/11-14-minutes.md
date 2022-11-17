## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/11-14-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2022-11-14](https://www.timeanddate.com/worldclock/converter.html?iso=20221114T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
* [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro
* [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

### Breakout C (APAC / Europe) - [2022-11-15](https://www.timeanddate.com/worldclock/converter.html?iso=20221115T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [FYI review of Writable directory prompts for the File System Access API](https://github.com/w3ctag/design-reviews/issues/749) - @torgo
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon
* [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion
* [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon
* [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2022-11-16](https://www.timeanddate.com/worldclock/converter.html?iso=20221116T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Special session on units principle [2022-11-17]

https://github.com/w3ctag/design-principles/issues/344


## Call Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/11-14-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2022-11-14](https://www.timeanddate.com/worldclock/converter.html?iso=20221114T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Lea, Yves, Peter

Regrets: Hadley, Tess, Rossen

### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov
### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

Peter: we had the joint meeting and epxressed our concerns about having a way to serialise and resotre the state, and unify this with other notions of presentational state. They took that feedback positively, but don't know what happened since.

Dan: what did we decide about this issue? Let's record something about where this stands. Are we just waiting on them to do something?

Lea: I don't think we're waiting, we had the meeting and there's no outstanding request.

Peter: it was early review, so we can close with message of bring it back when you've got more

Dan: [closes]

### [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov

Dan: [their response](https://github.com/w3ctag/design-reviews/issues/742#issuecomment-1218229578)

Peter: response seems to support my point.. keep doing what they're doing with accses to extra cookies and data for as long as possible

Amy: they want to avoid anonymous iframe so they can keep doing bad 3p cookies stuff? we reviewed that positively. How does this relate to fenced frames

Peter: not sure difference between fenced frames and iframes. Their response says we don't want to switch to anonymous iframe as that will have consequences for our ad performance. But they need a different solution than just not doing the privacy-enhancing stuff.

Dan: Mike wrote a bunch of stuff and asked for clarification.. Peter wrote clarification and Mike didn't respond, someone else did. We need to signal to them we're not happy with this?

Peter: It looks like there are other uses related to sharedarraybuffers, maybe. Clearly the obvious use case is ads and they're making that very explicit.

Dan: we can ack the other use cases, but there's no way to only use it for the not-bad stuff.

Amy: one comment says that the alternative to going through with this is to just use anonymous iframe undconditionally. Best case from our perspective is doing this, right?

Peter: that's what I'd like us to say

Amy: there's a [commit message](https://github.com/mjfroman/moz-libwebrtc-third-party/commit/92f9a6b1c7b6b58f7ecf2fc674ed7d5ad8691e1e) that says there was positive signals from webkit and mozilla, and that anonymous iframe depends on coep reflection.. but anon iframe now decoupled

Dan: anonymous iframe removing dependency on coep is a good sign, anon iframe will exist regardless

Amy: [mozilla](https://github.com/mozilla/standards-positions/issues/645), [webkit](https://lists.webkit.org/pipermail/webkit-dev/2022-June/032259.html) .. responses are minimal

Peter: initially I had the same reaction - it's information you can already get so why not expose it. But if you think about it more and abuse cases, you start to get concerned

<blockquote>
Hello folks. As things stand we're not convinced this is sufficiently in users' interest / addresses user needs. It looks to us like this circumvents privacy controls that are being introduced in the platform to the benefit of advertisers. There may be additional use cases as described by Mike above, but it's unclear how these could be enabled only for those non-ad use cases.  Chromestatus still says no signals from Safari or Firefox. However we've seen some info from [Mozilla indicating support](https://github.com/mozilla/standards-positions/issues/645). However, it's not clear that they've considered the abuse cases as described above. So at this point we're leaning towards closing this issue with "unsatisfied" – unless there's some further info forthcoming.
</blockquote>


### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Rossen: approaching closure?

Lea: last time we were discussing this we had lack of consensus. Concerns.. posted minutes..

Dan: a few comments since..

Lea: oh no did we not post [the minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/10-31-minutes.md#the-popup-api---leaverou-atanassov)? 

Rossen: what are you not still agreeing with?

Peter: I don't think the popup should be controlling whether something is presenting in the top layer - should be done by CSS. It should only control the psuedoclasses, and rendering is controlled by css. We need to add additional properties to css to codify the notion of a top layer, maybe create user defineable layers to fix the z-index problem. 

Lea: what Peter said. And also, once you can control top-layeredness through CSS, the problems with having popup as a separate element disappear. All of the problems are around making an element on the top layer without requiring any of the other behaviours of popup

Rossen: did you propose this?

Lea: I have tried to make this point. It's minuted previously. I don't want to hold this up.

Rossen: so no engagement with them?

<blockquote>
Hi - we discussed in our plenary call [on 11-2](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/10-31-minutes.md#the-popup-api---leaverou-atanassov-1) - discussion includes some thoughts from @LeaVerou @atanassov and @plinss. Concerns center around what is and is not controlled by CSS and whether popup/popover should be the only way to place an element on the top-layer. Once you can control "top layered ness" as a CSS property, the use cases that prevent this from being an element are easily dealt with. 
</blockquote>


### [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

**bumped to plenary**


### [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo

Dan: Rick has said that the intent is to clarify a gampad can be exposed through regular api and webxr at the same time... I don't think they've really addressed the issue.

Yves: was okay minus this issue with negative index [??] - they need to fix that

Dan: about this particular thing, the webxr gamepad, their list of changes is small. I feel we need to set this to proposed closed. I don't think we can close without tess. Can we close at plenary?

Yves: I don't think there is something more as a delta

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro

### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

Amy: looked through the security & privacy responses - no red flags so far but a bit more work to do.

### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

Lea: pending external feedback, why is it on agenda?

Dan: because it's been pending for ages

Lea: will look for developments...

Dan: we'll ask

### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

Lea: still pending external feedback since august? This is another review pushing for synchronous layout stuff.

Peter: pushing off into Houdini land.. what do we do to help get to the state of this becoming async?

Lea: [drafts comment asking for updates]

Peter: I'd like to see evidence that they're discussing making this async in the WG

### Breakout C (APAC / Europe) - [2022-11-15](https://www.timeanddate.com/worldclock/converter.html?iso=20221115T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
### [FYI review of Writable directory prompts for the File System Access API](https://github.com/w3ctag/design-reviews/issues/749) - @torgo

Dan: closed as they never got back to us with an explainer.

### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Max: Dan [asked](https://github.com/w3ctag/design-reviews/issues/760#issuecomment-1282022620) what's different with 649 but we haven't got a response. Looks very similar.

Dan: security review is not complete

### [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon

Yves: no response to my question but apart from that it seems reasonable. So suggest we close.

Dan: happy to **close** on that basis.

### [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon
### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Amy: chaneged milestone to next week. Asked for a better explainer. Talked about nudging the team contact...

### [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion

Dan: bump to plenary

Amy: [they have this issue about naming](https://github.com/gpuweb/gpuweb/issues/3594)

### [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon

Yves: they replied but I don't think the refutation they gave is necessarily good. 

Dan: Martin Thompson said he'd [given feedback](https://mailarchive.ietf.org/arch/msg/ipv6/lkrJjMUwZrUC7jYAo2mYCS4fpeA/). Would be good to respond as Yves said, and to acknolwedge Martin's message which seems to suggest lack of implementer support. "Considering the lack of implementer support mentioned, it doesn't seem likely we can review this positively"

### [Cookies Having Independent Partitioned State (CHIPS) specification review](https://github.com/w3ctag/design-reviews/issues/779) - @torgo, @rhiaro, @hadleybeeman

Dan: they gave us a list of substantive changes.

Reviewing https://github.com/privacycg/CHIPS/issues/30

Dan: Seems resolved.

Reviewing https://github.com/privacycg/CHIPS/issues/48

Amy: Major credit for all the stakeholder involvement here. Seems really good..

Dan: after reviewing these and the removal of the dependency on first party sets my instinct is to close this...

Amy: Ask Privacy sandbox people to fill out the societal impacts questionnaire? 

Dan: As beta testers?

Amy: Yes.

Dan: good idea.

Amy: They have yet to update their answers to the security & privacy questionnaire. I'll leave a comment asking for this and indicating we'll close [positively] after that.

Dan: +1

### Plenary Session - [2022-11-16](https://www.timeanddate.com/worldclock/converter.html?iso=20221116T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

### TTML Council 

*we agree to sacrifice breakout A next week for the ttml council meeting - Amy is chairing*

*we agree to not have any meetings next week as it's a US holiday week*

### Breakout Rollup

#### [PopOver (née Popup)](https://github.com/w3ctag/design-reviews/issues/743#issuecomment-1314204961)

Peter: agreeing and agreeing.

Peter: if CSS has a formal notion of rendering layers ... no reason why one shouldn't be reserved. I think CSS wg hasto have a discussion about rendering layers.

Rossen: is there an issue?

Lea: worried they just decided not to do this in CSS by discussing in OpenUI without ever bringing it to the CSS wg....

Rossen: we can help build that bridge.

Lea: https://www.foodnetwork.com/recipes/ina-garten/popovers-recipe-1914814

Dan: can someone in TAG who is part of CSS open this issue?

Lea: i can.

Rossen: i think this is a good idea.

**Rossen finds a [relevant CSS issue](https://github.com/w3c/csswg-drafts/issues/4998) which may already covers this**

**rossen to write comment**

### [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

Peter: some activity in CSS about this having to do with pseudo-elements. Has the explainer been updated to reflect those changes?

Dan: there has been some pushback on our points but do we care enough?

Lea: this seems too complex. 

Peter: i feel the same way - too complicated and bolted onto the side... Also this is a complicated problem to solve so this may be the best solution.  

Lea: kind of inclined to say "OK" ... 

Peter: i feel like i need to play with it to better understand it.

Lea: they want to push it forward... 

Lea: the concerns are about complexity...  

Peter: if we just say "yes we have concerns we think this is too complex" i don't think that will cause them to step back and revisit their design.  My concern is : is this the right approach?  I hate to give them that feedback without understanding a better way to do this.

Dan: can we couch it in terms of developer ergonomics.  something about layering?

Peter: if we can't easily wrap our head around it...  Authors should get some high level thing that they can just use...  I'd like to see that.

Dan: can we leave feedback ....

Lea: there's an experimental implementation in chrome...

Dan: have developers been using it?

Lea: that would be great... 

Dan: something like:
<blockquote>
Current status: we're concerned about developer complexity and ergonomics.  Can the requestors address this issue: how will developers actually us this?
  
Do you have any feedback from the current exerpiemntal implementation that could help to answer this question?
  
Is the implementation up to date with the current syntax?
</blockquote>

<blockquote>

@jakearchibald

We looked at this again today and had some questions:
- Is the current experimental implementation in Chrome up to date with the current syntax? 
- Do you have feedback from authors that have used the experimental implementation? Have you observed any of them using it and seen what they struggle with? 

We are particularly concerned about the complexity and ergonomics of this API, and we (TAG members) have not yet had the a-ha moment where we fully understand how all the pieces come together to create a transition in a real use case from scratch. Given the trouble we've had with it, that gives us some pause about DX in the wild. Perhaps it's an inherently complicated problem and there cannot possibly be a simpler solution, but it is a concern that came up several times in our discussions.

Regarding https://github.com/w3ctag/design-reviews/issues/748#issuecomment-1225922770 , the main issue I see is that with the current API, `updateTheDomSomehow()` needs to be repeated twice, which is fine when it's a separate function, but it means all such DOM modifications need to become separate functions, which as an author I'd find annoying. 
  
</blockquote>

**lea to leave comment**

### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss



### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
### [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Special Session on Units Principle

Attendees: Dan, Sangwhan

https://github.com/w3ctag/design-principles/issues/344

Sangwhan: the miliseconds makes sense for DOM APIs... very common in DOM.  

**Discussion of [temporal proposal](https://github.com/w3ctag/design-principles/issues/101) in ECMA and how it should impact 8.4.**

Sangwhan: it's being implemented in Chrome .. [intent to prototype](https://bugs.chromium.org/p/v8/issues/detail?id=11544) .. we should get clarification from other browsers besides Chrome before including it in design principles...

Filed https://github.com/tc39/proposal-temporal/issues/2436

```
8.3. Use milliseconds for time deltas, but adapt for interoperability 
If you are designing an generic API that accepts a time delta, express the time delta in milliseconds, unless it breaks interoperability.

Even if seconds (or some other time unit) are more natural in the domain of an API, sticking with milliseconds ensures that APIs are interoperable with one another. This means that authors don’t need to convert values used in one API to be used in another API, or keep track of which time unit is needed where.

Common APIs such as setTimeout() and the Date API follow this convention, along with many other DOM APIs.

However, if the surrounding APIs do not use milliseconds, it is best to follow the types used by adjacent APIs for developer ergonomics. Some examples include:

- HTMLMediaElement APIs use seconds
- window.performance uses DOMHighResTimeStamp
- Web Codecs use microseconds


```

**sangwhan to do a PR on 8.3**
