# TAG Teleconference
#### 28-30 August 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-08-28](https://www.timeanddate.com/worldclock/converter.html?iso=20230828T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov

### Breakout C (APAC / Europe) - [2023-08-29](https://www.timeanddate.com/worldclock/converter.html?iso=20230829T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @cynthia, @torgo, @ylafon
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo
* [ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/863) - @torgo, @maxpassion

### Plenary Session - [2023-08-30](https://www.timeanddate.com/worldclock/converter.html?iso=20230830T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Dan, Yves, Lea, Rossen

Regrets: Hadley, Amy

### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

Rossen: quite a face-lift. Most of the points were addressed... 

Dan: relevant issues:  
https://github.com/w3c/edit-context/issues/38  
https://github.com/w3c/edit-context/issues/53  
https://github.com/w3c/edit-context/issues/54  
...examples of resolved issues.

Rossen: Peter I think the one you were concerned with is 53.

Peter: I was concerned that it was underspecified...  My only other feedback was ... why aren't these in the DOM range?

Lea: being underspecified would be fine for an early review...

Peter: but this was from 2019... 

Peter: do we know the status?  There was work happening on a DOM range API... wonder if anything ever became of that?  I would suggest they incorporate that...

Lea: this seems to require a lot of manual syncing between this model and the DOM... and usually that can introduce error.  So I'm a bit worried that this is designed for the needs of big apps like google docs but not really usable by the average developer...

Peter: original model for building your own editor... 

Lea: there's a lot of projects that require that that are not maintained by large companies...

Dan: e.g. cryptpad is an example that's not...

Peter: original API design a simplistic model - editor from scratch - that may not be the only use case...

Lea: this seems to make complex things possible but simple things are not easy.

Dan: reasonable to challenge them on the developer complexity issue.

Lea: on the other hand - as a developer it looks really tedious to do but it's better than contentEditable... Maybe that's what we need.

Dan: could we ask them "what is your story for developer complexity?"

Rossen: I was pretty close to it when it started -- model made sense to me when it was text editing. Certainly needed as a base construct.  Having editors generally speaking ... the web has outpaced the capabilities of editors...  giving web developers a way to build the rich editors they want to... is the idea.  If you're building an editor, you're already an advanced developer... So... I stand behind the fact that this is a great step forward.  I don't see it as isolating any developer segment more than any other API...

Lea: Trying to think it through - one thing that gives me pause - APIs where if you want to do something custom then you have to do it yourself - APIs that have a cliff. This could be alleviated by providing a shortcut to create an editContext that already has the correct plumbing.  For example if you want to have a text editor thats a different color, or a markdown editor, these are simple use cases... but still very painful in the web platform today. it would be quite nice to not have to write a ton of code to provide an editor that has an improvement... of what the web platform has today.

Rossen: If you assume steady state of a document then you don't need anything... Editing is all about handling and reacting to the actions of the users... changing parts.. Reacting to actions... EditContext is all about reacting... When it comes to text, range API is not great...  What you're talking about are higher level edit commands that are built on top of constructs like the EditContext?

Lea: from what I'm seeing it seems you have to write code to sync up basic things - like undoing... all of these things you would normally get for free - you have to write code to sync with the DOM... I'm worried this is quite error prone.   Example 3 for example: https://github.com/w3c/edit-context/blob/gh-pages/explainer.md#example-3-mapping-the-selection-from-dom-space-to-editcontext-plain-text-space

Peter: yes this gets to my point - my concern is that it's modelled around a simple text buffer - not structured content... that's what I was asking for in the first place... 

Lea: also this https://github.com/w3c/edit-context/blob/gh-pages/explainer.md#undo web based editors rarely use the DOM undo stack.. there are many benefits from not having to maintain an undo stack of their own... for certain editors having an undo stack maintained by the browser is not workable but for something like a code editor, as long as it can be undone reasonably there are no reasons for the develoeprs to want their own undo stack...  I would much prefer see somthing that allows you to tweak the existing undo stack or replace it if you want but it shouldn't be a requirement to write an undo stack to use this... 

Dan: can we provide feedback that encompasses both positives and negative points?

Lea: I think it's about developer experience... for some use cases this is the right developer experience but for some cases it's not right...   We have a design principle... https://w3ctag.github.io/design-principles/#simplicity

Rossen: fwiw I think the undo stack is not mentioned in the spec...   Is the explainer maybe stale?

Lea: the explainer has a bunch of things it doesn't do... https://github.com/w3c/edit-context/blob/gh-pages/explainer.md#interaction-with-other-browser-editing-features

Dan: explainer updated 3 months ago...

Lea: also: when you have an API of this kind... can end up with buggy code.  buggy editors ... all over the web.

Peter: 2 models - (1) you're building an editor - e.g. google doc - this API is focused on solving that proboem .. in that regard, positive step (2) the browser already has some rich capabilities - but no way to extend / augment those - which is what we'd like to see.  My feedback is that they are trying to solve (1) - that's fine - my concern is that I don't see how this feature ties into explaining the editor functions of the browser... Imagine if we opened up the browser's editor...

Lea: meta-comment - this type of thing is exactly why we need to have this initiative [task force] to identify gaps in the web platform...  

Rossen: EditingContext is part of the editing task force that's focusing on editing... 

Lea: why is it so focused on the specific use case?

Rossen: focusing in the base primatives...

Peter: seems like a side thing of people trying to replace the broswer editor... would love to see this evolve towards a way to augment the browser editor...

```
First, it's great to see work in this direction, and we definitely recognize the need for it!
  
While many editing use cases do require re-implementing capabilities like undo or caret management, not all use cases share that complexity. Right now, it appears that this API primarily caters to the most complex of cases that require re-implementing many fundamental aspects of text editing, but introduces [sharp cliffs](https://w3ctag.github.io/design-principles/#high-level-low-level) for the simpler use cases, those that merely need to augment regular text editing (case in point: the Markdown editor right here on GitHub). As mentioned in our design principles, there's value in designing APIs that keep [simple things simple, and complex things possible](https://w3ctag.github.io/design-principles/#simplicity).
  
Could this be the begininng of an effort to support *augmenting* the browser editor capabilities, when you don't need to entirely reimplement them? This would not necessarily require a different design: perhaps it can be done with shortcuts (e.g. a way to get an `EditContext` that already has the right plumbing based on a given editable element in the DOM (`<input>`, `<textarea>`, `<div contenteditable>` etc)).
```

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov

### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

### [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss

Yves: I wrote a commnent here...  On local network you might not have https enabled devices - or https enabled sevrers that answer something different with http... in that case it's likely that you don't want to upgrade...  They said they will use what's defined in "private network access"... I proposed a way signal a http response request that you can have on a server to signal "the http content is different"...  it's not a downgrade.  Otherwise, yes - everything that allows more more https is great...

Peter: I agree with your suggestion on a header - it would not cause someone who connects on https to drop to http - but it would block an automatic upgrade - makses sense.

Dan: such a header is defined?

Peter / Yves: no

Yves: they would run this feedback by the http working group in any case.

Peter: downside of such a header - running different content on http / https is an anti-pattern - we don't want to encourage it - but it exists...

Dan: devices that are not going to get upgraded... 

Peter: right - and won't get this header therefore...

Yves: I think we can close now - we expressed a view - we expressed feedback - please run this by ieft working group. Etc...

Dan: close / satisfied

Yves: *will leave feedback*

### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov


## Breakout C

Present: Dan, Yves, Max, Amy, Sangwhan

Regrets: Hadley


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

Max: they have made some progress... [comment yesterday](https://github.com/w3ctag/design-reviews/issues/523#issuecomment-1695125119) - they have a proposal for our concerns...

https://github.com/w3c/miniapp/issues/195#issuecomment-1525435423

1. Origin Model - they proposed a detailed solution there...

2. package can be modified ...

3. Zip format ...

Dan:... talking about using something parallel to TLS...

Sangwhan: they can't use TLS out of the box so ... i'm sympathetic. It's an improvement! Need to take a look at this [more deeply].

Dan: i think it's positive and they are addressing our concerns... so deservers strong positive response.

Sangwhan: other question - does it provide the same level of security guarantees?  I will digest this myself...

Dan: concerned it allows another party to get in the middle of the train of trust...

Sangwhan: delegation to a trusted party -- could be same as the mechanism of trusting a CDN - could look at it from that angle.  Or "end to end guarantees" as with traditional TLS... Taking the CDN architecture into the picture ... "Signed exchanges" is an example of "we don't trust CDNs".

Max: They are trying to do this end-to-end - we can ask them to clarify ... that would be helpful...

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/523#issuecomment-1696947770)

### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @cynthia, @torgo, @ylafon

Dan: Some [new comments](https://github.com/w3ctag/design-reviews/issues/805#issuecomment-1688602214) from @a-sully.  They have addressed many of our concerns - in particular with regard to [security considerations](https://github.com/whatwg/fs/blob/main/proposals/MovingNonOpfsFiles.md#security-checks).  There is still a multi-stakeholder issue because webkit and mozilla both oppose.  The issue not to do with the move capability itself but the whole concept of access to local file system. 

Dan: My proposed closing comment follows:

<blockquote>
Hi folks - thanks for your responses and thanks for addressing our concerns. We're happy with the proposal as it stands, however I think the main concern we have now relates to multi-stakeholder support for the file system access API itself. We encourage you to work with other stakeholders / implementers to achieve a consensus-based approach to this capability. 
</blockquote>

Dan: Suggesting *satisfied with concerns* result. 

**we agreed to close**

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

Dan: We're gonna talk about at TPAC.

### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo

Dan: Thomas has come back with [some feedback]https://github.com/w3ctag/design-reviews/issues/854#issuecomment-1659895741).  

Max: if you look into the lego example - they use web bluetooth API - not serial API... so from some perspective it's not a justification for web serial for bluetooth - because that use case is not described.  They use 2 APIs - one is web bluetooth API - normal bluetooth to connect the web browser to the LEGO hub - the other option is to use web serial API connection – this requires USB cable. In this use case they don't require web serial API over bluetooth. In my view if you already have bluetooth why not just use bluetooth to do the connection?

*Max to ask them to ask them to clarify*

### [ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/863) - @torgo, @maxpassion
  
Max: I looked at this.  The use case - is trying to solve the problem that sometimes some JS - not necessary to run all the JS using the SW - bypass the SW in some cases. So they designed this static routing API. The question I have - looking at their descritpion - uses a mechanism that is not stable yet.  https://github.com/WebKit/standards-positions/issues/206 : comment that it builds on URLPattern but this hasn't been standardized..  

Dan: no progress on the Mozilla standards position https://github.com/mozilla/standards-positions/issues/828
  
Dan: It's going to Origin Trial according to the Explainer... 

Yves: I think URL pattern is a version of Regexp where most of the expeisnve things are removed....

Dan: [Service Worker Scope Pattern Matching](https://github.com/w3ctag/design-reviews/issues/417) also made use of URLPattern... 

Dan: I think it's concerning that something like URLPattern that is being used as a building block is still not "stable" or is sitting in WICG instead of having been brought forward... 

Dan: feels like they have to have a plan for standardization of URL Pattern

*max to leave comment*

## Plenary Session

Present: Dan, Peter, Yves, Max, Rossen, Amy

Regrets: Hadley

### Breakout Rollup

#### Breakout A

#### Breakout C

*we reviewed outcomes of breakout C*

### Issue Triage

https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22

*we triaged new issues*
