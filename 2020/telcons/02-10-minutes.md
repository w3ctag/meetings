## TAG Teleconference
##### 10-13 February 2020

---

### Agenda:

#### Breakout A (Europe / US)

* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @torgo, @ylafon, @hadleybeeman, @lknik
* [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris
* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov
* [Partial freezing of the User-Agent string](https://github.com/w3ctag/design-reviews/issues/467) - @dbaron, @torgo, @ylafon, @hadleybeeman
* [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471) - @torgo, @plinss

#### Breakout B (US / APAC)

* [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) - @hober, @cynthia, @dbaron
* [Gamepad Light Indicator extension API](https://github.com/w3ctag/design-reviews/issues/362) - @cynthia
* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [File Handling](https://github.com/w3ctag/design-reviews/issues/371) - @alice, @dbaron, @kenchris
* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo
* [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris

#### Breakout C (APAC / Europe)

* [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo
* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo
* [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman
* [Cookie Store API ](https://github.com/w3ctag/design-reviews/issues/469) - @torgo
* [WebRTC DSCP Control API](https://github.com/w3ctag/design-reviews/issues/465) - @cynthia, @torgo, @ylafon

#### Plenary Session

* Breakout Rollup
* UA String Fun
* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @torgo, @ylafon, @hadleybeeman, @lknik
* Issue Triage

-----

### Breakout A

Present: Tess, David, Yves

Regrets: Dan, Kenneth

#### [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297)

(reading issue to try to figure out what the state of it is)

Yves: maybe try asking Mike to figure out what the plans in this space (including for cookies) are?  Get clarification on upgrade path?  Perhaps we should ask the chairs if we want to try to make further progress on the issue -- we can discuss that in the plenary.

#### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338)

(reading issue)

David: comment 10 days ago suggests API has changed quite a bit, we should probably take another look

Tess: needs new assignees, new milestone?

David: 3 assignees may be enough, we just need to take another look

Tess: look again in this afternoon's Calif-APAC call?

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461)

David: I need to take another look at Maciej's comments.

Tess: Annevk's point in the [last comment](https://github.com/mozilla/standards-positions/issues/238#issuecomment-582424598) on Mozilla issue was great; it's not enough to enumerate threats and make sure there's flexibility to address them, need an affirmative belief thatsome kind of UI.... just paraphrasing, you should read it.  Maybe worth reflecting in text for design principles doc?  Might be worth getting something in the privacy and security self check?

David: Maybe I'll have time to look between now and plenary?

Tess: Maybe we should propose this breakout session be 24 hours later?

#### [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464)

Tess: Haven't managed to spend time on this yet.  At high level sounds good to let origins opt out of features in general.  Need to look at details.  Push this out 2 weeks?

#### [Partial freezing of the User-Agent string](https://github.com/w3ctag/design-reviews/issues/467)

Tess: busy github thread...

Yves: A lot of discussion about lying to pretend you are/aren't Chrome.  Will moving to Client Hints be better or not at avoiding sites that work only with one browser?  Discussion about GREASE.

Tess: Need to catch up on thread.  We as the TAG probably should have a concern about changes to web architecture that could make it more difficult for a new minority browser to take off.  Concerns in the thread around that.

Yves: Two issues here: identifying browser capabilities so user can have good experience, but second not to rely on those capabilities to block certain implementations.  Balance between the two.  But having a way to know capabilities of the browser is essential.  Got that when doing upgrade-insecure-requests.  Wanted to know which version of differentbrowsers were doing that -- had to do filtering.

David: We have a design principle that features should be detectable -- we encourage that at the feature level.

Yves: Detecting too many features can be problematic - UA string used as baseline.

Yves: We should probably discuss this together in plenary at face-to-face.

David: Are there things we should do before F2F?

#### [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471)

David: We have none of the assignees here...

David: Maybe a face-to-face issue?  But will we have time to discuss in depth there?

Tess: At least push it out a week until we have the assignees?

### Breakout B

Present: Alice, David, Peter, Rossen, Tess

Regrets: Sangwhan?

#### [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) - @hober, @cynthia, @dbaron

All: this issue has been open since 2017. Yikes.

David: Has this shipped in Chrome?

Tess: [since Chrome 66](https://www.chromestatus.com/feature/5762805915451392)

David: Recursive fetching makes sense if you have a type-specific API, but a fetching API for fetching a generic resource doesn't feel like recursive fetching makes sense, really.

Peter: Can you do preload off HTTP headers? Or rather modulepreload...

David: I think so?

... Seems like we may as well close this... if we'd filed feedback sooner it might have been useful, but at this stage it seems unlikely to be so.

Rossen: Should we wait for the WHATWG issue to be resolved?

David: Might be a moot point at this point.

Rossen: Close?

Peter: Yep, let's tentatively close and confirm at the plenary.

David: I'll write a comment.

#### [Gamepad Light Indicator extension API](https://github.com/w3ctag/design-reviews/issues/362) - @cynthia

Rossen: This is still pending updates from the developer. Platform abstraction should be there. That comment was added half a year ago.

#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

Skipping, Sangwhan is absent

#### [File Handling](https://github.com/w3ctag/design-reviews/issues/371) - @alice, @dbaron, @kenchris

Alice: Still pending feeback.

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo

Peter: Concerned about conflating XR events and DOM events...

... 

David: Extra events seem ok, as long as normal events also happen

Peter: I'm reading it as the select events being overloaded to mean different things... I could be wrong.

Rossen: Is this running under the assumption that there can only be a single such layer?

Tess: the API assumes that...

Rossen: that seems unnecessarily restrictive...

Peter: Can see you might want to have multiple overlays in different places

Rossen: One of the early discussions I had with hololens... we were working on the browser and how we could decompose the browser and use HTML in scenes, especially int he immersive world... is geared and focused toward having multiple interactive HTML panels.

... imagine you want to put a <streaming TV service> player on your wall. That's what holo experience allows you to do... you pin these experiences and it serialises all the geo-locked data for you so can recosntruct your experience
  
... want to be able to incoropoate your daily activities in the scene... restricting the experience to saying you can only hve one HTML-based panel that is going to be always in front of you sounds like you are solving a specific use case... having a hard time imagining why this should be restricted to only one...
  
... we don't have these types of restrictions elsewhere int he platform
  
Tess: Well, fullscreen is a counter-example...

Rossen: Watch this space...

... Just not sure this restriction is warranted

Peter: How will this interact with future APIs that let you push DOM content into the scene? Is this just a special case of that? Should they be different APIs at that point?

Peter: They asked for issues in their repo for each point of feedback, so we can each open an issue and link it back to the TAG review.

#### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris

Tess: Only had David from the assignees in Breakout A... still only have David. 

### Breakout C

Present: Sangwhan, Alice, Kenneth

Regrets: Yves

#### [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo

Sangwhan: I had a chat with Cyril (?) abot this at TPAC
... seemed unconvinced about the issues we raised. We can't tell them it's a bad idea, if they pursue a bad idea in some other standardisation body we can't really do antyhing about it.

... Suggest we leave a last comment saying we had a short chat about this... don't know why a bunch of new types, seems like it's trying to reinvent a file system... maybe this should be consiolidated into a package inside a video.

... Could end up creating a loop since you can put a video inside the data inside the video...

... I want to close this, I don't think we're going to get any traction here. Seems like a really bad idea.

#### [WebRTC DSCP Control API](https://github.com/w3ctag/design-reviews/issues/465) - @cynthia, @torgo, @ylafon

Sangwhan: I looked into this, but I still don't understand it. The WebRTC parts I understand are the encoding parts... this is networking. Packet prioritising etc... can use this API to divide traffic unequally over several channels. I don't understand the use case.

Kenneth: The explainer doesn't explain much either....

Sangwhan: Need to defer to Yves here. I don't understand the value.

Kenneth: Added comments to the issue about explainer and spec returning 404

#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo

#### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

(Discussion on mixing layout and semantics, and legacy compat elements)

Alice to comment.

#### [Cookie Store API ](https://github.com/w3ctag/design-reviews/issues/469) - @torgo

Kenneth: Looks pretty sensible, I don't know all the details. 

Sangwhan: Does this guarantee transactionality?

Kenneth: Not sure. There's an onchange event listener...

... some shorthands... guess that's fine...

... Will leave a comment about ???

#### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris

(out of time)

### Plenary Session

Present: Ken, Peter, Rossen, Dan, Alice, Tess, Yves

Regrets: Sangwhan

#### Breakout Rollup

[summarizing what happened in breakout sessions]

**HTTP State tokens:** should we continue or close this issue?

Yves: we were wondering about the upgrade plan...  Documenting everything that could be a [transition plan]...  do we do a transition or just continue to imporove cookies?  What are the benefits and could those be ... I will leave a comment asking what the current status is. Ask for comment from mike before closing...

**Scheduling API** nothing done so far - kick this down the road.

**WebNFC** David wanted to read some Mozilla comments before we work on this.  Still pending.

**Origin Isolation** Pushed 2 weeks.

**UA String** lots happening here - we can schedule a special session at the f2f.

**Securer context** kicked

**rel="modulepreload"** 

David: nobody has responded to the feedback and this has shipped in chromium so maybe we should close the issue.

Dan: should we resolve "unsatisfied"?

David: it's not super clear why this is a new rel value ... the other question was - some people aren't too much of a fan of preloading every module... there are tradeoffs.  more work for authors as a tradeoff for getting more effective prefetching.

Dan: is anyone else looking at this besides chromium?

David: not sure.  Some feedback left on the issue.

David: will close with no further comments.

[consensus]

**Gamepad Light Indicator** Defered

**WebHID** defered 

**File Handling** Pending feedback.

**WebXR Dom Overlay** 

Alice: Rossen made the most critical point - putting a dom into a scene is a non-goal. If that future API comes to exist wouldn't that be a generatlizartion of this and therefore why would we want both. This API is limited to an overlay layer - why wouldn't you want the generalized version of that?

Rossen: Yes.

Alice: we discussed around that and the use cases for the more general API...  Tess & I talked about the hit test API and intersection of this API. 

Tess: I left some feedback on the hit testing issue related to this.

Alice: some concern from Peter about events... reuse select events... input section is very unclear. I will distill that feedback and leave it for them.

**ISOBMFF**

Need to check with Sangwhan?

Tess: fine by me to close it.

Dan: I'm ok with closing it.

Dan: I think Sanghan should write the summary.

**MATHML Core**

Alice: still interested to get Hadley's thoughts.  I worked a lot with Brian to shape up the explainer to explain things better. I think the explainer does a better job.  There is addiitional feedback about mixing layout and semantics... purely layout elements + some math semantic elements mixed. Some legacy compat elements that it's unclear what the intention was yet.  Parsing... do the elements need explicit closing?  I will leave those comments.  I would like Hadley to also take a look at it.

**Cookie Store API**

Ken: new async API for accessing cookies.  Seemed fine to me - nothing major.

Peter: not purely for serviceworkers?

Ken: no. It kind of makes sense - they want it for serviceworker but they want to mimic it for other places.

Peter: we have a sync API on window...

Dan: should we reach out to Lukasz and get his feedback from a privacy perspective?

Ken: I don't think this changes anything about cookies...

Dan: does it open up new avenues for tracking that weren't there before?  Are there unintended consequences?

Ken: Unchange event on cookiestore... inconsistency between get and set <- comment already made

**WebRTC DSCP control...**

Peter: explainer fixed..? Don't see any changes to the explainer yet. Spec URL has been updated.. Waiting for updates to the explainer.

Ken: issues with the explainer... I sent them that feedback.

#### Issue Triage

[Foldable CSS](https://github.com/w3ctag/design-reviews/issues/472)

Rossen: i could help...

Tess: +1 me.

#### AOB

Dan: talking about [Developer needs assessment survey](https://insights.developer.mozilla.org/) and how it called for better platform APIs including a [native filesystem API](https://github.com/w3ctag/design-reviews/issues/390)

Tweaking breakoutd discussion - Peter to do a doodle poll. next week will move Breakout A to 1hour later on tuesday.