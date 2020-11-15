## TAG Teleconference
##### 09-12 November 2020

---

### Agenda:

#### Breakout A (Europe / US)

* [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov
* [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @torgo, @plinss
* [Review for CSS property "aspect-ratio"](https://github.com/w3ctag/design-reviews/issues/559) - @hober, @torgo
* [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @torgo, @kenchris

#### Breakout B (US / APAC)

* [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @dbaron
* [WebRTC Priority Control API](https://github.com/w3ctag/design-reviews/issues/560) - @cynthia, @dbaron
* [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511) - @alice, @kenchris, @atanassov

#### Breakout C (APAC / Europe)

* [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @kenchris
* [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris
* [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

#### Plenary Session

* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo w/ Guest Chris Wilson

* Breakout Rollup
* Issue Triage



-----


### Breakout A

Present: Ken, Dan, Tess, Peter, Rossen, Yves, Hadley

Regrets: 


#### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov

Rossen: we said "this is great" on face value - we need to go and look at the details.  I will leave a comment.  We need to spend a good time reviewing this.  

[bumped to next week, rossen & dan to have breakout]

#### [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @torgo, @plinss

Peter: I want to get rid of them.   Browsers know that they're being driven by a human. Can browsers send a meaningful signal as part of form submission?

Rossen: that's a strong statement. The browser does **not** know that it's being driven by a user.

Tess: in trust token world - a trust token would be issue some number of trust tokens - it sees this `<input type="token">` and sends one of these.

Peter: it doesn't intrinsically know but it can determine it once and then fill it into forms automatically.  Do it in such a way that the browser can display a captcha.

Tess: trust token API that people are working on doesn't have any form submission integration .. this is a natural approach.  However if a browser doesn't recognize a type value it displays it - but it could be set to `display=none` - it would be easy to polyfill.

Rossen: I agree with the premise of the issue.  I want to see how it ties into identity... Stronger mechanisms that could be present to signal that a human is driving the browser.  Reducing the repitiveness of capchas would be a huge win.  Perhaps this is a case where the trust token is indefinite?

Dan: [raising the issue about fraudsters using farms of workers to mint 50 tokens at a time]

Rossen: ... the tokens need to be scoped at the session or something... it would be great to (a) tie it into user identity - verifiable identifier that says I'm logged into a session... browser and slack [running as electron app] - should use same underlying tech.  I'm the same user.  Can this be somehow associated with a larger scope session?

Rossen: where do we go from here? 

[Tess left a comment and @-mentioned others]

Tess: Being worked on in WICG... some concern about the cryptography involved.  


#### [Review for CSS property "aspect-ratio"](https://github.com/w3ctag/design-reviews/issues/559) - @hober, @torgo

Tess: I like it. The capability of using tha adder function... It a good addition to CSS.   Solid spec work.

Rossen: Agree. I was there from the beginning. Quite comfortable.

Tess: We might be too close to be objective.

Tess: Some elements have an intrinsic aspect ratio.  e.g. an image. some don't, eg. `div`. This property allows you to set an override. If you set an aspect ration then the set aspect ratio wins, if not then the intrinsic aspect ratio wins.  Important for images for example.  Other ways to do this are very tricky to use. This property slices through that - you can just set the ratio and you get that for free.  This is useful not just in new layout systems. It's very helpful in normal flow layout.  As far as syntax it's about as simple as it can be.

Dan: any inetraction issues?

Tess: when you over-specify - when you set a width and height and an aspect ratio then width and height win. It might be difficult where you're setting height and width in one stylesheet and aspect ratio somewhere else. That's the only one I can think of.  Don't know the state of developer tools support.

Yves: syntax, is it the same as media query aspect ratio?

Rossen: I don't think so.  

Yves: just at a syntax level to figure out if it's a ratio..

Tess: double-checking...  Yes, it's the same CSS syntax.

Dan: suggest we set it to proposed closed and close it in the plenary.

Tess: sounds good.

Tess: they suggest that the form is too complex - should we have a lighter weight form for a straightforward thing like this?  

[discussion on this]

Tess: this has been extensively vetted by layout experts.


#### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @torgo, @kenchris

Tess: Storage standard... very abstract.  defines conceptual framework that other storage mechnisms can hook onto.  E.g. as other specs are built on top of Fetch.   Similar idea here.  Also specifying what happens when you "clear storage data" button .etc...


... key value store.  Key is what origin and what kind and value is what the backing store is.  Not really something that's exposed to authors. Definition of something called a storage bucket. All the storage for an origin fits into the same bucket.  API allows for programmatic access to storage buckets.  We now live in a world of partitioned storage.  E.g. facebook.com is one bucket, facebook.com in an iframe on NYTimes is a different bucket. API helps websites understand when the bucket under them is changing.  Can allow sites to create an ephemeral storage bucket. Adding an API to it might require more work.

Ken: I went to TPAC breakout.  You can delete some of these buckets if there is a right to be forgotten request.  For login info you really don't want that to be gone - or for a boarding pass - giving developers more control or due to regulatory requirements.  

Tess: Dedicated proposals for login or regulatory consents... Site wouldn't have to use its own storage for that.

Ken: normally you have to write to people "we're going to store this for xyz timeframe" and after that's it's gone [under gdpr].

Dan: is there a privacy concern - data leakage between buckets?

Tess: example of 2 tabs open to facebook - it can already know...

Dan: container tabs?

Tess: it would have no way of knowing. This doesn't change that.  Useful for things like storage access API - and storage access changes - getting notified that the bucket is invalid.  "What happens to temp storage" - how do you swap it out in a way that's safe?  Uncommittedd indexdb transaction... This API helps with defining that precisely.  Super unclear how this should work right now.

Rossen: biggest worries?

Tess: I deeply understand why we need to do this but haven't reviewed if this is a good design.

Rossen: Reading the privacy assessment - on the question on deistinguising between 3rd and 1st party context - not proposing any distinction between 1st and 3rd.  Down the road it may restrict access to 3rd party.  That is a warning flag to me.  

Tess: what's unclear from the explainer - defining partion storage is an ongoing effort. That's "in flight". I agree with the worry but since it's in flgiht it's probably appropriate. 

Ken: this is early days.

Tess: I think we should take a closer look at the API itself.

Dan: I'll do a stronger review of the privacy & security response.

Ken: I'll look at the API.

Rossen: Storage buckets - the API is hanging off of navigator.  That's for the current origin?  

[bumped 2 weeks]


### Breakout B

Present: Alice, Peter

Regrets:


#### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @dbaron


#### [WebRTC Priority Control API](https://github.com/w3ctag/design-reviews/issues/560) - @cynthia, @dbaron


#### [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511) - @alice, @kenchris, @atanassov


### Breakout C

Present: Ken, Hadley, Dan, Yves

Regrets: Alice

#### [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @kenchris

Hadley: relationship with generic sensor API?

Ken: this is very low frequency unlike generic sensor API.

Ken: We were OK with this last time we looked - now there is specificaiton.

Dan: is it part of DAS? Seems related to DAS.

Hadley: checking new charter.. it's not there.

Dan: So what is the trajectory for this work? Where does it go after WICG?

Dan: [asking](https://github.com/w3ctag/design-reviews/issues/336#issuecomment-724536903)

Dan: so basically we need to take a deeper dive into [this spec](https://wicg.github.io/idle-detection) now that there is a spec. 

Ken: I gave feedback in the first review - they seem to have implemented it.

Sangwhan: it's not as scary as you might think - but a question of usefulness. I can think of one use case - 

Ken: they want it for the chat apps.  That's a pretty compelling one.

Sangwhan: it's not the end of the world without it.

Yves: they want indication of are people looking at ads or not. It could be used for that as well.

Sangwhan: you could use intersection observer for that...

Yves: if you are on your mobile and there is a popup app and you drop your phone waiting for it to start then you will be "idle" so I think it would be used for that.

Dan: I think that's a privacy issue.

Sangwhan: as for the spec at hand I haven't looked at it yet - the updated one.

Dan: I can review for privacy

[bumped 2 weeks]

#### [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

Ken: could we ask them to post a summary of their breakout session?

[bumped a week pending that feedback]

#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

#### Discussion on Council 

[we agreed to increase the plenary to 90 mins this week to accomodate discussion on the council and the formal objection]

### Plenary Session

Present: Kenneth. Dan, Peter, Sangwhan, Yves, Hadley, David

Regrets:

#### [discussion of council

#### Breakout rollups

##### Breakout A

Dan: We bumped webxr layers; we talked about how horrible captchas are;

Peter: Some feedback on that issue already.

Dan: aspect-ratio ; i did take a look at it, I don't see anything to indicate that we shouldn't give this a pass.

Peter: I can write up the comment.

[agreed to close]

**Storage Buckets**

Dan: ken was going to look at the API. I'm going to look at the privacy issues. We bumped it 2 weeks. 

##### Breakout B

[no quorum]

##### Breakout C

**user idle detection**

Sangwhan: nobody has done anything with it.

Dan: should we put it in deep freeze? 

Sangwhan: they are supposed to revisit in a week or 2.

[no relationship to DAS formal objection]

Dan: notes that Reilly doesn't have a working group in mind.

Sangwhan: should probably be in webapps if anything...

**virtual keyboard show/hide**

Ken: i asked them about the summary of TPAC - no response yet

**WebXR anchors**

[bumped]

#### Triage

**Byte Streams**  
#567 - 

**Review of NativeIO**  
#566 - @cynthia, @kenchris  

**Review of CSS Sizing 3**  
#565 - 

David: guts of CSS

Dan: Should we punt on it?

Ken: i wonder what we can contribute?

Peter: mixed feelings

Dan: if we do a review then we should ask for an explainer and what the user need is...



**Deprecating `document.domain`.**  
#564 - Yves, Tess in absentia

**CSS Scrollbars: scrollbar-color, scrollbar-width**  
#563 - assigning Torgo & Ken

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo w/ Guest Chris Wilson

Guest was a no show.

### Special Session on [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528)

Present: Dan & Rossen

Rossen: From previous meeting, we do like the general direction and this session is about digging further into the spec and all functions that it brings with it.

Dan: on security & privacy questionnaie, they have not answered it, pointing only to answers being "in the spec" but there is a small one-item securty & privacy considerations section. Will ask them to expand. [left comment](https://github.com/w3ctag/design-reviews/issues/528)

Rossen: When going through explainer it was difficult to understand what other options were considered and why these ones are the best. Perhaps they can add a section with that explanation.

Dan: loving the diagrams in the doc

[discussion of the `nativeProjectionScaleFactor`]

Rossen: this isn't something we've had elsewhere in the platform...   I don't believe we have a scale factor today that would give users the ability today to let users understand what the scale factor is for a layer or view. Could be effected by either the user (e.g. pinch zoom) or the content. As an author I don't have access to this info from the platform. This API will enable that but in an awkward way - creating a webGL binding etc..  Meta point is we're either missing a way to bubble this up a bit further as a more generic platform capability - more than just the webxr context - or be very careful here and maybe not expose it.  These have been a pain in the platform - e.g adjusting content to prevent scroll bars - capability has been sought after since forever.

Dan: also - a potential fingerprinting issue.

Rossen: proogogating anything up from the underlying platforms should be done carefully.  It's not obvious to me if there are platform layer violations in this spec.  Another main scrutiy & privacy concern: how easily and quickly would such capability allow readbacks from unintended actors?  Just because my bank added a twitter logo and pulled in some twitter iframe - i don't want them to be able to get a hold of my layer buffer.  
