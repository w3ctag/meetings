## TAG Teleconference
##### 21 August 2019

Present: Alice, Peter, Lukasz, Dan, David, Hadley

Regrets: Tess, Kenneth, Sangwhan

Scribe: Dan

---

Agenda:

* Issue Triage
* Ethics update - @torgo, @hadleybeeman
* [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @alice, @torgo
* [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393) - @alice, @dbaron, @lknik
* [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392) - @hober, @alice, @dbaron
* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [JavaScript Memory API](https://github.com/w3ctag/design-reviews/issues/386) - @cynthia, @kenchris
* [Web Authentication Feature Detection](https://github.com/w3ctag/design-reviews/issues/383) - @dbaron, @torgo, @hadleybeeman
* [Web of Things (WoT) Thing Description](https://github.com/w3ctag/design-reviews/issues/357) - @torgo
* [Web of Things (WoT) Architecture](https://github.com/w3ctag/design-reviews/issues/355) - @torgo

---

### Triage

[WebRTC-SVC](https://github.com/w3ctag/design-reviews/issues/396) 

Assigned tentatively assigned to Sangwhan and Kenneth

[Same-Origin iframe document-access limiting Feature Policy](https://github.com/w3ctag/design-reviews/issues/397)

Assigned Lukasz and tentatively Tess

[Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399)

Assigned David, tentatively Tess

[Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400)

Assigned David, 

[Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406)

Peter: this makes me worry

Assigned Hadley, Tess, 

Hadley: it does reference the Async Clipboard API

[More restrictive hasEnrolledInstrument() for autofill data](https://github.com/w3ctag/design-reviews/issues/407)

Assigned David

Hadley: What is an enrolled instrument?

David: proably like a credit card?

Hadley: what is it enrolled in?

David: good question...

Hadley: local vocabulary...

Alice: it boils down to : you have to have all the info stored... in order for autofill to work - also seems to be implementation specific.

Hadley: given that that's the case, if it's checking autofill data for completeness & validity that sounds like an implementaiton-level thing.

David: i think the fact that it's not in the standard might meand that ... 

Peter: hadley raises an interesting point: is this something we should be looking at?

Dan: maybe someone could c omment and ask if TAg review is necessary since this is an implementation issue rather than a spec change...

Alice: they probably felt better safe than sorry - we might be better to see it and say "we don't need to see it but thanks for being cautious".

Dan: [+1]

Hadley: [+1]

[Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408)

Alice: seems like it's out of the points from Andrew ...

Dan: assign me and I can contact Andrew

[Rendering Independent Scroll Offsets](https://github.com/w3ctag/design-reviews/issues/409)

Peter: another change without spec changes.... 

Alice: please assign to me

### Ethics

https://github.com/w3ctag/ethical-web-principles/issues

Dan: Hadley & I had a breakout... Accessibility topic...

Hadley: also the conversation that we have a browser centric view of the web.. Therefore we are proposing to include a Para that broadens the defitinition... See : https://github.com/w3ctag/ethical-web-principles/issues/4#issuecomment-521720123 

Dan: plan would be to issue an update at the f2f with some of these small changes in it...

Hadley: Sgtm

### [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403)

Alice: I statred reading it - i was wondering if I might do an editing pass? Explainer text - I would make a PR - here are a bunch of suggested edits none of which you are obligated to accept. 

Dan: I think that would be well received. Let me check with Ada. 

Alice: Also I feel it's longer than it maybe needs to be. Some stuff I didn't fully understand...

Alice: it's very thorough - all the info that needs to be in there is in there. Didn't have an specific questions about the spec (API) yet. 

Dan: I got a ping from Nell asking about them joining us to talk through it - i suggest TPAC.

Hadley: I'm not clear why the WebVR API is deprecated and therefore why replace it?  Sure there are good reasons but would be good to understand the journey.

Dan: I'll ask Ada about getting some time on their Agenda at TPAC.

### [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393)

Alice: Breakout in which we will file issues - regular breakout time, 5pm Thursday US Pacific time.

### [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392)

David: I had a note to schedule a breakout...  

Alice: didn't we discuss this at our last breakout?  

David: yes - I think Tess was going to write something..

Alice: let's bump it until she's back.

### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389)

David: I should try to schedule that breakout - but it's been blocked by vacations.

[bumped]

### [Badging API](https://github.com/w3ctag/design-reviews/issues/387)

Alice: i spent time working with Matt on this one. Looks like they are going to split it out into document badging vs. scope badging - scope badging will be more useful for the app use case and document badging will be more useful for the tab use case. 

https://github.com/WICG/badging/issues/49#issuecomment-521882946 

... I was fairly convinced that this was the right thing to do - they ended up here based on Tess's comment on feature detection. Scope level would be: everything with the same URL would have the same badge status, whereas you could imagine different documents having different badge statuses.  e.g. github comments.  Then once you have the 2 different types of badging. You can get scope like behaviour using the document API - 2 windows open to the same gmail inbox they will both get the same info fromt he server about the nunber of unread emails...

Hadley: wouldn't gmail be scoped anyway?  Issues in github - makes sense 

Alice: you could have 2 tabs opened to the same github issue but ...

Alice: they have work in progress to split.

Dan: what if I am writing a simple application and I just want to set a badge and I don't care if it's a document or a scope?

Alice: the fact that there are these 2 close concepts means .. if as a developer you want both then you need to set both.  if you're writing something that can be installed (a manifest) then you will need to set the scope-level

Hadley: 2 different scopes ...

Alice: it's about whether the info you're conveying via the bedge makes esnes for the scope - an origin sort of - vs the document.

Hadley: granularity.

Alice: you could have both. you could have 2 windows open to the same gmail inbox.

Alice: they are going to write it up... Otherwise they will get back to us. [pending external feedback]

[bunped to f2f]
