## TAG Teleconference
##### 03-05 August 2020

---

### Agenda:

#### Breakout A (Europe / US)

* [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss
* [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris
* [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss
* [Import Conditions](https://github.com/w3ctag/design-reviews/issues/535) - @hober, @kenchris
* [Pointer Events Azimuth Angle and Altitude Angle](https://github.com/w3ctag/design-reviews/issues/537) - @hober, @hadleybeeman
* [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538) - @hober, @hadleybeeman, @atanassov

#### Breakout B (US / APAC)

* [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477) - @hober, @cynthia, @dbaron, @hadleybeeman
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
* [Storage Pressure Event](https://github.com/w3ctag/design-reviews/issues/533) - @hober, @dbaron, @plinss
* [VisibilityStateEntry](https://github.com/w3ctag/design-reviews/issues/534) - @dbaron, @atanassov
* [CSS Color Mix](https://github.com/w3ctag/design-reviews/issues/526) - @alice, @dbaron, @atanassov

#### Breakout C (APAC / Europe)

* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris
* [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo
* [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov
* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo

#### Plenary Session

* Breakout Rollup
* Issue Triage
* Finalize dates for our next virtual F2F

-----

### Breakout A

Present: Dan, Peter, Rossen, Yves, Tess

Regrets: David, Kenneth


#### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss

[bumped]

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris

Tess: Ken and I looked at this at a breakout - and I raised some concerns that they haven't addressed.  Things have changed a bit since then.  Concern I raised: bundles are attempting to address some of the downsides of AMP - one of those being the default rendinering of AMP is to have a fake address bar. We don't like that.  Could be described as deceptive.  The question is how do you display the package URL for an unsigned bundle in the browser. If the publisher and package URL are different you could display the package URL directly (opaque), the publisher's origin (promoting the deceptive practice) or the distributor URL (encourages existing package - the fake URL bar). Doesn't look like they replied to that.  Also it looks like some things have changed - one issue got closed. 

... this is the document that replaces that open issue: https://github.com/WICG/webpackage/blob/master/explainers/bundle-urls-and-origins.md

... I will review.

Rossen: So any time you have publisher / distributor difference - you're creating an easy to exploit vector for phishing. That's terrible.

Tess: the key is this is for unsigned.

Dan: what are the use cases?

Tess: suppose you're a professor and you're putting together a bundle of article - you have no authority to make a signed exchange for any of these things...

Dan: what about use of some mechanism e.g. a University server or a letsencrypt / equiv ..

Tess: the publisher signes it - not the distributor. 

Tess: you load a web page adn want to share it with your friend over p2p - like bluetooth.

Dan: once again in that case there should be a warning on the receiver's device...

Tess: yes - maybe we should ask the people invlolved about this kind of UI...

Rossen: how does the UA detect this ?

Tess: either for all unsigned bundles - or all bundles of unsigned exchanges where the distbutor origin is not the publisher origin.

Dan: isn't this putting the cart before the horse?

Tess: so far in the web we only use UI like that for insecure things...  Might be a hard sell that this should get such a warning.

Rossen: unless the proof is there that this concern is not a concern.  At this point I am way more leaning towards requiring - pushing back on that basis - from the PoV... \\

Dan: [leaves a comment]

Peter: could we eliminate the idea of unsigned bundles by making it a requirement to sign the bundle - even if it's self-signed?  If we just always require that every bundle is signed by whoever made it - might shift the problem.

... also - if I download something over TLS can I store something from the TLS session such that I include the cert fromt he original site such that a 3rd party could verify that this came from the original site - and thereby preserve the provenance of the original data.  Maybe a future extension to TLS?  Surfacing more of the handshaking to the parts of the browser that would generate a bundle.

Tess: it's weird that this is separate from TLS and existing mechanisms...

[bumped]

#### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss



#### [Import Conditions](https://github.com/w3ctag/design-reviews/issues/535) - @hober, @kenchris

Tess: my very short review is it seems fine

Yves: use of types that are not media types is confusing... Otherwise it seems OK.

Tess: the string json is hard coded... into the spec... should have been media type json?

Yves: yes - a +JSON extension to the generic media type...

Peter: if you're going to use a specific media type it should be filtered to that media type... I like having just plain JSON but needs to be clearly defined what that maps to.  

Yves: restricted set of types they are allowing... 

Peter: we need to specify that the media type should be something+json... 

Tess: what about text/plain?  Some issue with web server configuration... as i read it: If you say type json it tries to parse it as json and if that parse fails it fails the import.  

Peter: kind of scary to me that it relies as parsing. some stuff that isn't json could parse as json... I guess for json it's probably safe. More concerned about other things.

Tess: yes fair to be concerned about other cases...

Yves: more about the processing model of json rather than the type.

Yves: probably ok as it is.

Peter: yes probably.

Dan: we should close?  I think any thing else we discussed could be handled by extensions down the road.

Tess: I can write a closing statement.

[agreed to close with thumbs-up]

Peter: Tag Ken in the issue [since he's not here this week and he's an assignee.]

#### [Pointer Events Azimuth Angle and Altitude Angle](https://github.com/w3ctag/design-reviews/issues/537) - @hober, @hadleybeeman

Ran out of time before we got to this.

#### [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538) - @hober, @hadleybeeman, @atanassov

Ran out of time before we got to this.

### Breakout B

Present: Peter, Rossen, Tess

Regrets: David, Alice, Sangwhan

#### [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477) - @hober, @cynthia, @dbaron, @hadleybeeman

Peter: I think we should close this.

Unminuted discussion. Plan to draft a closing statemnt for the plenary.

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov

Pending extenal feedback. Monitoring.

#### [Storage Pressure Event](https://github.com/w3ctag/design-reviews/issues/533) - @hober, @dbaron, @plinss

Ran out of time before we got to this.

#### [VisibilityStateEntry](https://github.com/w3ctag/design-reviews/issues/534) - @dbaron, @atanassov

Ran out of time before we got to this.

#### [CSS Color Mix](https://github.com/w3ctag/design-reviews/issues/526) - @alice, @dbaron, @atanassov

Deferred until Alice is available.

### Breakout C

Present: Dan, Yves, Hadley

Regrets: Alice

#### [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477) - @hober, @cynthia, @dbaron, @hadleybeeman

[we discussed the current status and requestor's latest changes in response to Mozilla feedback]

Hadley: Martin might have a point in terms of recommenders not being good for humanity. There might be something under ethical web principles relevant to this. On ther other hand it's already going on out there. Some people might think recommendations are useful for users.  We can't stop people from doing this but we can help make it safer for users.  Declaring a potential conflict of interest with schema.org. Should Schema.org not be approrpriate, the normal approach would be to spin up a w3c wg to define a vocab. Not the most expedient approach.

Dan: I also don't think it's accurate to say that Schema.org is a "existing Google data format". ... [for further discussion at plenary]

#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia


#### [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris


#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

[bumped to the 17th]

#### [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov


#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo


### Plenary Session

Present: Dan, Peter, Tess, Hadley, Yves, Rossen

Regrets: David, Kenneth, Alice

#### Breakout Rollup

##### Breakout A

Tess: (on breakout A) We talked about navigation to unsigned web bundles mostly.  Trying to figure out what kind of feedback.  Dan left a comment. I have a comment pending.  We then talked about import condtions from tc39. We said it's ready to be closed.  

Peter: anyone not want to close this?

[no]

Tess: It's assigned to Ken & Me so I will draft a closing comment.

##### Breakout B

Decided to close Import Conditions.

[consensus recorded to close with this feedback]

##### Breakouts B & C: Media Feeds

Peter: yes we talked about media feeds.  consensus in the breakout that we should close this as unsatisfied. 

Tess: issues with media feeds:
1. lack of receptiveness to feedback - unwilling to change things based on feedback or consider alternatives
2. only use case they gave is reifing youtube recommendations into browser chrome which is typically considered trusted UI. Considering the societal problems around this kind of recommendations, we shouldn't encourage this kind of integration. I don't think the web community should be excited about that.  

... Those are the things I want to say.

Hadley: i mentioned in breakout c - i saw a link with the ethical web principles.  Looking at this it all looks like it's markup in the content - not sure how it integrates into the browser?

Tess: there were some mockup screen shots where in the Chrome browser chrome there is a media player and this would feed into that. maybe that was in an earlier version of the explainer.

Hadley: given that that's disapeared can we count that as progress?

Peter: but this has no other use but coming up in the browser chrome.

Hadley: but the explainer doesn't explicitly mention chrome.

Tess: as far as the format goes all it is is a podcasting format just in json not rss or atom.  I filed an issue and the response was "youtube already uses this". I don't think it's a good answer.  I like Atom/RSS feeds and subscribing - and not having to go 50 web sites to read news. So it's weird to push back on this pre-existing, widely-deployed and interoperable ecosystem. But this is narrowly constrained.  It's restricted to video because it's specifically for integrating the browser with this one youtube feature. 

Hadley: we can hang a lot on that it should be more extensible. It is weirdly specific.  This is a data format. Architecturally, I can't see why this should be specific to videos and to recommendations. I can think of a lot of other use cases for non-video recommendations (like shopping sites), or video or audio playlists (without recommendations). One format for all would be cleaner and more elegant.

Tess: they are not trying to solve this in a general way - they are trying to put something specific for a specific product (youtube) into chrome.

Hadley: part of the explainer that talkes about recommendations gets to specifics - content ratings etc...

Tess: you can do that with existing extensibility points in Atom or RSS, e.g. Atom's `<category>` element. Could be layered on existing syntaxes. 

Hadley: "browsers don't have native support for Atom and RSS" 

[consensus recorded to close unsatsified with Rossen drafting feedback]

##### Breakout C

Dan: in C, we bumped webxr anchors module. we need to bump the other things. we didn't have the right people to talk about WebHID.

#### MiniApp Update (Yves)



#### Issue Triage



#### Next virtual F2F: week of 21 September?

Yes.
