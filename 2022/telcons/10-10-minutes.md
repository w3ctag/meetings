# TAG Teleconference
#### 10-12 October 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-10-10](https://www.timeanddate.com/worldclock/converter.html?iso=20221010T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Review request: linear() easing function](https://github.com/w3ctag/design-reviews/issues/761) - @plinss
* [Delta review (to CR) of WebXR Augmented Reality Module](https://github.com/w3ctag/design-reviews/issues/769) - @torgo
* [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro
* [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro
* [CORS Requirement for 3rd party sources in &lt;model> tag](https://github.com/w3ctag/design-reviews/issues/775) - @LeaVerou, @torgo, @atanassov
* [Early Design Review: Page Unload Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2022-10-11](https://www.timeanddate.com/worldclock/converter.html?iso=20221011T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Privacy Stuff
  * [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
  * [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
  * [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
  * Focus on draft feedback
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo
* [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman
* [Web Machine Learning Model Loader API](https://github.com/w3ctag/design-reviews/issues/759) - @cynthia, @maxpassion, @hadleybeeman
* [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon
* [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon
* [Output Device Selection in Web Audio API: AudioContext.setSinkId()](https://github.com/w3ctag/design-reviews/issues/766) - @torgo, @maxpassion
* [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon
  
### Plenary Session - [2022-10-12](https://www.timeanddate.com/worldclock/converter.html?iso=20221012T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion
* Any update on miniapp feedback?
  
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


-----


## Breakout A

Present: Peter, Dan, Lea, Yves, Rossen, Hadley

Regrets: Amy


### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Peter: **I will send a ping.**  Still no feedback.

### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Peter: some responses to your last feedback, Lea.

Lea: they pointed us to the OpenUI document.. have not finished reading.

Rossen: what was the point? 

Lea: they see being a popup as being a trait in same way that index is a trait of a tab element... 

Rossen: not sure I agree.

Lea: I also had trouble seeing that reasoning.

Rossen: maybe we should get on a call with them?

Lea: I think that would be helpful.  To have a proper breakout about this.

Rossen: I think they will be amendable to this... 

Dan: I suggest a separate call at a timezone that makes more sense to the group involved.

Rossen: **I will reach out.**

Peter: attribute argument makes more sense to me if elements that are popups also are displayed in flow - but I don't think that's the use case here.  So doesn't fit with tabindex or conteeditable.  

Rossen: next thing they want to bring forward is selectelement... What you're saying (peter) makes total sense.

Peter: Suggest using the breakout B timeslot.

Lea: difficult for me.

### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

Hadley: Dan asked if it'll happen in privacy cg .. or privacy sandbox ...

Dan: there is a document we're working on .. 

*Hadley leaves comment*

### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

**bump to C**

### [Review request: linear() easing function](https://github.com/w3ctag/design-reviews/issues/761) - @plinss

Peter: I asked if we even need to review this...

Lea: seems like a fairly small feature.

Peter: just another easing function - don't see any architectural concerns.

Peter: shall we close?

Lea: happy to close with res: satisfied.

*consensus recorded*

Peter: **I will close this**

### [Delta review (to CR) of WebXR Augmented Reality Module](https://github.com/w3ctag/design-reviews/issues/769) - @torgo

Dan: I don't think [any of the chanegs](https://www.w3.org/TR/webxr-ar-module-1/#changes-from-20191010) represent any architectural changes from the previous positive review.  Privacy considerations looks great.  My proposal would be to close this - considering the small list of chnages from the workign draft.

**agreed to close as satisfied**

### [Delta review (to CR) of WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/770) - @hober, @torgo

Dan: less certain on this one as [list of changes](https://www.w3.org/TR/webxr-gamepads-module-1/#changes-from-20191010) seems similarly small but Tess might have more opinions.

Rossen: in their explainer - they allow you to map gamepad behaviour to other sources such as occulus touch, daydream, etc... which is good. the thing that's interesting: the gamepad instance must not be included... ID must be entry string, etc... 

Peter: one of their changes - they're allowing it even if there is no xr session.. if they're gonna do it then it seems odd to exclude it from the regular list of gamepads... So seems a little thought needs to go into it.

Dan: so they are positioning this as an alternative to the gamepad API?

Peter: sort of, yea.... 

**Dan leaves 2 comments - marked pending feedback**

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro

**bump plenary**

### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

**bump to plenary**

### [CORS Requirement for 3rd party sources in `<model>` tag](https://github.com/w3ctag/design-reviews/issues/775) - @LeaVerou, @torgo, @atanassov

Peter: image, video and audio all predated CORS - would we require CORS now if we were adding them? I think the answer is yes.

Dan: I agree.

Rossen: sounds sensible.

Hadley: me too.

Yves: for consistency it would be good to have CORS for everything.  Img, etc.. are weird in that regard...

Peter: think of it like https...

Peter: 2nd question: should it be restricted to secure contexts?

Dan: yes.

Peter: haven't seen any mention of it...

**Dan leaves 2 comments** 

Dan: let's wait til **plenary** to get wider TAG consensus...

### [Early Design Review: Page Unload Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

**bump to plenary**

## Breakout C

Present: Max, Hadley, Sangwhan, Dan

Regrets: Amy,


### Privacy Stuff
  
#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
 
#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
 
#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

#### Focus on draft feedback

Hadley: I really the emphasis on use cases - i wonder if the authority might be better from us - recognizing history of 3rd party cookies - as original use vs.. current use... that goes against EWP... if we're going to be improving this one feature that will be used for many things - then it makses sense ... in our wheelhouse as stewards of the architecture of the web. as opposed to privacy for its own sake. 

Dan: agree ...

Hadley: even stronger rather than listing... full list of use cases that we see privacy sandbox techs attempting... 

"Signifigantly better privacy rather than slightly better privacy."

### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

Dan: can we close this based on the fact that they've updated their explainer?

Sangwhan: I'm Ok - they will haev to figure out how to actually implement this...   What I triued to flag here is that there are a bunch of reasons why bfcache cannot kick in - this allows develoeprs to tap into that info so they can correct their mistakes. This is info the devs will be able to get access to - if they look at debug logs.  Not particularly risky - but what might be risky is if you have extensions that disable bfcache as a side-effect then that info might leak - about which extensions the user has installed.. Their updated explainer addresses this concern.  I'd be OK closing this one.

Dan: In privacy TF - talking about telemetry... we might want to mention that.

Sangwhan: I thought there might be privacy issues but I don't think so - if you exclude the extensions discussion.  I think info this particularly exposes is not risky.

Dan: 👍

**Sangwhan to close with resolution satisfied**

### [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman

Max: We are expecting an update to the explainer .. more use cases... They did send a link to the answers to the questionnaire... You suggested to update their explainer... 

**dan leaves comment**

### [Web Machine Learning Model Loader API](https://github.com/w3ctag/design-reviews/issues/759) - @cynthia, @maxpassion, @hadleybeeman

Max: I think they got the point about the DRM issue... Maybe we can provide a suggestion...?

Sangwhan: I think the DRM discussion is moot - because there's no hardware support that could make this possible at the moment.  You'd need to have an EME-like thing... that the user cannot access. No support for this at the moment.  No tech solution... 

Dan: we could resolve 'satisfied' but with caveat that we don't think DRM for models is a good idea.

Sangwhan: what about other things that have IP protection like VR models...

Hadley: this represents my views - we don't want to be endorsing DRM... rest of it seems largely fine.  Recording our intentions in reolsoving as not endorsing DRM is important...

Sangwhan: API surface I'm Ok with it.   There is a question of why tensor has to be created as a factory rather than a construcor. I will leave feedback. It goes against our design principle.

Dan: still Ok to resolve satisfied?

Sangwhan: satisfied with concerns and pointing to reference to the design principle. 

**Sangwhan to close and leave closing comment - resolution satisfied with concerns**

### [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon

Yves: I looked at this a bit - they want to hide info about the file... I wonder why they are not generating URN IDs for that... what they described is a URL resolver of some kind... I will propose that even though URNs are not the best...

Yves: they are hiding things with UIDs for local files ... probably a good thing - from a pov of obfuscating... based on time for example you might not get the same UID... also they want that to be keyed with the web site as well... You cannot infer from the UID what files you're working on...

**yves to leave comment**

### [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon

Yves: I sent a request for clarification.. they want to only have `/*.` ... issue is the same issue Nick reported... all on or all off... difficult to exclude some domains... or restrict by pattern... they say they want it to work with CDNs for 100s of domains... I wonder if finer grain matching would be better.  Probably something we need to disucss...

Sangwhan: this looks super risky.

Yves: I proposed partial matches or negative matches ... i understand it would be difficult to implement.. but partial matches would probably be a good move here.

Dan: I'd like to get Andrew's perspective...

Sangwhan: MNOT maybe as well...  One concern I have also - we have varying kinds of wildcard syntaxes... across the platform.  We'll have to deal with this technical debt.  In service worker there's another wildcard...

Yves: it's different but they still don't want to implement regex in general.  There's also the `*` or something that is similar to regex without it being a regex...

Dan: Should we open a design principle issue?

Sangwhan: it's a best practice, but everyone is doing their own thing...

**Yves leaves comment**

### [Output Device Selection in Web Audio API: AudioContext.setSinkId()](https://github.com/w3ctag/design-reviews/issues/766) - @torgo, @maxpassion

Max: Had a look at the explainer... very good question asked by Chris - why does web audio API need them... and why does HTML not have them... and should it?  Also looked at the design of the API.. a lot of questions of other ways to work around this... one suggestion is to suggest the author to update the explainer to answer the 2nd question - why HTML doesn't solve the problem.. a selectaudiooutput api can do the same thing - but authors should update the explainer to explain why this API is not suitable for web audio... 

Dan: that sounds great..

**Max to leave comment accordingly**

Sangwhan: is it an output device request?

Max: to enable the developer to select the output...

Sangwhan: user choice

Max: from the github discussion looks like the user also gets a notification... 

Dan: Web Audio community have good track record... Also notable that this is multi-stakeholder (Google and Mozilla).

Sangwhan: concern: any API recently minted with a device selector -- firstly it would be a promise... You'd have the UA give a selector.. trying to understand if that pattern exists here or not...  The issue opened in 2014...   Some legacy elements about implicit device choice in Web Audio API that don't match current patterns.

### [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon

**bumped**

## Plenary Session

Present: Peter, Dan, Yves, Hadley, Sangwhan, Rossen

Regrets: Lea, Max

### Breakout Rollup

#### On [Model TAG CORS requirement](https://github.com/w3ctag/design-reviews/issues/775)

Peter: a lot of extra overhead if we don't require it....

Peter: Domenic filed an issue in webkit.. model   

Sangwhan: I'm not entirely convinced that a declarative model is ok because these are massive payloads...  It's ok that there's a tag for it - but I see issues with the implicity fetch kicking in... What are the benefits of having that implicitly fetched? 

Dan: good that it's in immersive web...  it also allows you to easily add 3d models to your pages... good for long tail..

Peter: yes.  their draft report has a lot of blank sections...  I think it's good.  I'd like us to do a more thorough review.

Sangwhan: [on CORS] - the XR folks don't want CORS.. they want TAG to weigh in because there is disssagrement within the group. But a lot of them don't.   Thinking about it : only benefit I see is from a maintainability perspectibve - having another carved out loading model for this would probably not be good. User needs are more important. They suggest no-cors is better for user needs.  Anne thinks they should use CORS.

Yves: it's more consistent with the platform.

Sangwhan: single, unified fetch model with the tested security guarantees. But if you carve out a special loading mechanism then it's yet another thing that has to be tracked as a special case.

Rossen: that sounds like a good reason of why they should use CORS. 

Peter: Not buying that it's better for users -- it may be better for developers but possibly worse for users due to security issues.. Currently you can't render a model into a canvas .. but when someone adds that then we would need CORS. I think the default should be CORS. "CORS is the security model of the web. If you don't want to use it then you need to justify why..."

Rossen: We have a principle?

Peter: no but there is an issue...

Rossen: on their issue 15... 2d resources can fetch resources... 

Peter: More of a CSP issue.

**Sangwhan to leave short comment**

Rossen: is the intent here to enable some of the distributed app model type of resource sharing?  So I can provide my own models... as part of ...

Dan: interacting with a 3d model in a declarative way...

Rossen: [Domenic said](https://github.com/immersive-web/model-element/issues/56#issuecomment-1221856280) CORS is foundational mechanism for enforcing the same origin policy.

Dan: good to know we are aligned.

**and closed**

#### Breakout A

#### Breakout B

#### Breakout C

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro

### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

### [Early Design Review: Page Unload Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

### [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

### [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion

### Any update on miniapp feedback?

### Issue Triage
