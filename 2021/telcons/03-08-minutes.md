# TAG Meeting Minutes - week-of 8 March 2021

## Agenda
  
### Breakout A (Europe / US) - [2021-03-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210308T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Early design review of light-DOM CSS Scope proposal](https://github.com/w3ctag/design-reviews/issues/593) - @hober, @LeaVerou, @kenchris
* [Early design review for the FLoC API](https://github.com/w3ctag/design-reviews/issues/601) - @torgo, @rhiaro, @plinss, @atanassov
* [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @kenchris, @atanassov
* [Web Serial](https://github.com/w3ctag/design-reviews/issues/431) - close it or is there a security concern?
* [Get installed related apps](https://github.com/w3ctag/design-reviews/issues/436) - can we close it?
* [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo, @atanassov
* [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @LeaVerou, @torgo, @kenchris, @atanassov
* [HTMLPopupElement - popup](https://github.com/w3ctag/design-reviews/issues/599) - @hober, @LeaVerou, @kenchris, @atanassov
* [WebCodecs (again!)](https://github.com/w3ctag/design-reviews/issues/612) - @cynthia, @kenchris

### Breakout B (US / APAC) - [2021-03-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210309T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [high priority] Design Principles PR 262 - can we land it?
* [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @plinss
* [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @hober, @torgo, @plinss
* [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia
* [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou
* [Declarative Link Capturing](https://github.com/w3ctag/design-reviews/issues/589) - @cynthia, @kenchris, @plinss
* [Support WebOTP API and origin-bound one time code in cross-origin iframes](https://github.com/w3ctag/design-reviews/issues/604) - @hober, @cynthia, @kenchris
* [inert attribute](https://github.com/w3ctag/design-reviews/issues/610) - @hober, @LeaVerou
* [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris
* [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo
* [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris


### Breakout C (APAC / Europe) - [2021-03-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210309T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Early Design review of App History](https://github.com/w3ctag/design-reviews/issues/605) - @kenchris @cyntia - how can we progress quickky?
* ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon
* [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman
* [Suggested file name and location for the File System Access API.](https://github.com/w3ctag/design-reviews/issues/598) - @kenchris
* [Media Session: video conferencing actions](https://github.com/w3ctag/design-reviews/issues/608) - @ylafon, @kenchris

### Plenary Session - [2021-03-10](https://www.timeanddate.com/worldclock/converter.html?iso=20210310T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* meta issue - how to priotize early reviews
* Breakout Rollup
* Issue Triage

## Minutes

### Breakout A (Europe / US) 

Present: Dan, Peter, Lea, Amy, Kenneth, Tess, Yves, Rossen, Hadley

Regrets:

#### [Early design review of light-DOM CSS Scope proposal](https://github.com/w3ctag/design-reviews/issues/593) - @hober, @LeaVerou, @kenchris

Lea: our feedback is being brainstormed on... no news as far as I know

Dan: so pending ext feedback still?

Lea: believe so... feedback was that the points make sense and they are working on it...

Dan: if they're really working on it then it's pending editor update.. that's the label that means we're waiting for them to make a change that reflects the feedback. Could ping again to avoid stalled.

Ken: ask to ping when something new to share

Dan: future milestone, see if it has progressed then

Ken: will leave that comment

#### [Early design review for the FLoC API](https://github.com/w3ctag/design-reviews/issues/601) - @torgo, @rhiaro, @plinss, @atanassov

Amy: left feedback, still waiting

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/601#issuecomment-792910873)

... they replied: 'still thinking' will respond in a week or two.

#### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @kenchris, @atanassov

Ken: has encorporated feedback from me and Jake Archibald. so that's good. Seems sensible. One thing now is that when youc call `getscreens` you get a `screens` object ... could be a naming issue...  `screens.screens`... An earlier version of this implementedis what is in the spec today. They are incorporating this into a new explainer - it's not spec'ed.  

Dan: should we try to close this?

Ken: I'm concerned it might ship if we don't provide our feedback...

Ken: I think this is pretty good - they are going through and origin trial to get more feedback.

Dan: security and privacy?  I can review.

Rossen: where does end up? what spec?

Dan: second screen working group ... is what's indicated. Is there multi stakeholder support?

Ken: will leave naming feedback.

Peter: somee thoughts - aware of work on foldable screens... Intending to harmonize. My concern is that someone ships part of this before rest is baked and we end up with multiple multi-screen APIs... 

Ken: I think we're pretty aware... they want to make sure this fits together...  

Peter: it's a meta-concern.

Peter: my other concern - takes all the screens and puts them into one virtual coodinate space - does that have the best developer ergonomics?  Should we be able to target a specific screen object?  

Ken: 3 TVs as a big canvas... [as a use case] 

Peter: in some cases a developer will want to taget a window a specific screen - and with this approach you have to do the math to figure that out.

Rossen: in the other case where we consider screen-local coordinates - you still have to do the math... however you look at it you have to do math.

Ken: unless you want to do something on a specific screen full screen, which could be a common use case.

Rossen: `requestfullscreen`...

Peter: but you're not always gonna want full screen. Just a question of convenience for developers.

Rossen: i'd like to see how other platforms are handling this... 

Dan: worth asking the question on the issue...

Peter: will do.

Peter: changing behaviour of how it works today.. breaking exisitng implementation 

Peter: my proposal is to add an optional parameter - move to x,y (& this screen). And also wondering how `moveto` works today in a multi-screen setup.

Rossen: pretty sure you have a canvas (across) both windows...  could be platform specific.

Rossen: in windows we draw the distinction between displays and screens... multiple displays that you can enumerate...

Dan: point on developer ergonomics is good. Web doesn't necessarily want to map platform features into identical js apis. Wants to make sense for web devs.

#### Meta-point on early design reviews

[Meta point: should we provide fast feedback on early design reviews or will this mean that things that close...]

Amy: could send wrong signal, that we don't need to hear anything more from them if we close

Lea: prioritize new design reviews over re-discussing design reviews we've already provided feedback in

Ken: if we close things we could end up something shipping before it gets to next stage...

#### [Web Serial](https://github.com/w3ctag/design-reviews/issues/431) - close it or is there a security concern?

Dan: provided feedback that they took concerns into account and documented in security considerations, about allow/blocklists of types of devices. I don't think we can say there's TAG consensus about adding to web platform, but that the API design is okay.

Yves: it's WICG, we will have another say as part of horizontal review. Okay to close now.

Dan: where after WICG? that is feedback we can give:

`Hi @reillyeon we're happy with the API design as indicated and looking forward to hearing about the incubation experience within WICG. We'd also like to understand better where this work is intended to end up after WICG. Will this be going to a working group such as Devices and Sensors, for example? Also it remains a concern that Mozilla's position remains as *considered harmful.* We encourage you to work with them and other implementers on mitigation strategies against the issues they have raised.`

#### [Get installed related apps](https://github.com/w3ctag/design-reviews/issues/436) - can we close it?

Ken: [leaving feedback about alternate proposal from Mozilla](https://github.com/w3ctag/design-reviews/issues/436#issuecomment-792945735)

#### [HTMLPopupElement - popup](https://github.com/w3ctag/design-reviews/issues/599) - @hober, @LeaVerou, @kenchris, @atanassov


#### [WebCodecs (again!)](https://github.com/w3ctag/design-reviews/issues/612) - @cynthia, @kenchris

[bumped]

#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo, @atanassov

Rossen: They have not taken our feedback into consideration... a bit disappointed.

Dan: I'll ping the group chair about it... ?

Rossen: they have no examples of how it should be used...  the current incarnation of their spec has no intention to be read by developers. 

Dan: proposes closing comment:

`We're going to close this off. The TAG is satisfied with the design and that feedback has been taken to account, however there is still a lack of uses cases and examples as @atanassov has pointed out in the last comment. We would therefore strongly encourage that these be added to the spec in subsequent revisions. We `

[we acutally decide not to leave this comment yet]

Dan: will reach out to group chair

[bumped]

#### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @LeaVerou, @torgo, @kenchris, @atanassov

### Breakout B (US / APAC) 

Present: Lea, Peter, Rossen, Tess

Regrets: Sangwhan

#### [Design Principles PR 262](https://github.com/w3ctag/design-principles/pull/262) - can we land it?

Added some comments, shifdted to breakout c.


#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @plinss

Bumped, waiting for feedback

#### [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @hober, @torgo, @plinss

Deferred.


#### [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia

Looked at, no comments, seems reasonable, bumping to next week for Sangwhan's input.

#### [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou

Pending feedback, bumped.

#### [Declarative Link Capturing](https://github.com/w3ctag/design-reviews/issues/589) - @cynthia, @kenchris, @plinss

Tess will write feedback re: new_client behavior on platofrms that don't support multiple windows.

#### [Support WebOTP API and origin-bound one time code in cross-origin iframes](https://github.com/w3ctag/design-reviews/issues/604) - @hober, @cynthia, @kenchris


#### [inert attribute](https://github.com/w3ctag/design-reviews/issues/610) - @hober, @LeaVerou
#### [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris
#### [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo
#### [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris


### Breakout C (APAC / Europe) 

Present: Ken, Amy, Yves, Dan

Regrets: Sangwhan

#### [Design Principles PR 262](https://github.com/w3ctag/design-principles/pull/262) - can we land it?

[bumped as we don't have sangwhan]

#### [Early Design review of App History](https://github.com/w3ctag/design-reviews/issues/605) - @kenchris @cynthia - how can we progress quickly?

Dan: early in the design process and they will come back for further review after.

Ken: making sure that the right use cases work, the current history API is really broken for app experiences. If you want to do something like twitter with different tab but you want each tab to have a different URL that you can share, but you want to click back, but  you don't want if you click between tabs and press back it goes between them. In native apps you go one back. Making those experiences and still getting a shareable URL is really complicated. You end up with an experience where people press back and it closes the PWA. Or it's cycling through tabs and you don't know where next. 

.. the main problem is the browser inserts things into the history out of the apps control. Solving by history created directly by the application. It's important.

Dan: scoped to same origin

Ken: like what you can do today but better

Amy: read the s&P questionnaire response and half the explainer and nothing jumped out...

Ken: not loading a separate HTML file but changing the URL and showing a different UI

Dan: no feedback from gecko or webkit

Ken: looking at all the details and use cases will take some time. [feedback on initial impression](https://github.com/w3ctag/design-reviews/issues/605#issuecomment-793527466)

#### ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon

Yves: it's under discussion. Multiple proposals. My position is to recommend they pick the solution that is the easiest to use for an end user (web developers) and easiest to understand so it doesn't add extra complexity. Will send feedback later.

Dan: propose close.. until they have something specific to review.

#### [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman

Dan: explainer link points to a section of the webxr device api explainer which doesn't hav eits own set of use cases?

Ken: depends on driver support..

Hadley: use case is rendering scenes with varying levels of complexity. We could ask them to flesh out use cases more.

Ken: means they render it with high resolution because people are going to get closer? sometimes its the opposite, far away you want low resolution?

Hadley: looks like it

Dan: it's a delta on an existing spec. What are we being asked for?

Ken: have they got developer feedback? Feedback from people working on 3.js or babylon js would make sense.

`Some questions: have they got developer feedback - e.g. from library developers - on this approach? Can you flesh out the use cases a bit? Since the explainer link points to a subsection of the WebXR explainer can this be considered to be a "small delta" on an already existing spec, rather than a new thing? If so, are there key questions or issues you would like our feedback on?`

Hadley & Ken: [thumbs up]

#### [Suggested file name and location for the File System Access API.](https://github.com/w3ctag/design-reviews/issues/598) - @kenchris

Dan: good response on security.. can close?

Ken: we already looked at it and it was positive.. no further comments

Dan: close in plenary

#### [Media Session: video conferencing actions](https://github.com/w3ctag/design-reviews/issues/608) - @ylafon, @kenchris

Dan: if there are no privacy concerns might be good to docment why not...

Ken: they're considering naming feedback. What is the cross browser story?

Dan: the spec should contain what he wrote about security and privacy.. is that added? Yes.

Ken: will leave closing comment

#### FLOC

[left some additional feedback]



### Plenary Session - [2021-03-10](https://www.timeanddate.com/worldclock/converter.html?iso=20210310T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Tess, Amy, Peter, Dan, Hadley

Regrets: Sangwhan

#### Breakout Rollup

##### Breakout A

Dan: light-DOM CSS scope - pending external feedback.
... FLoC API: we received feedback that they are considering our feedback.
... multi screen: developer ergonomics, Peter left feedback
... webserial: close
... get installed related apps: Ken left feedback, bumped
... popup: didn't get to
... webcodecs: bumped
... webxr hit test: group chair is looking to progress on their side. Immersive web is a really good example of standards in action. Started with a CG, people who came togther, developed early standards (webVR) and more became involved, started a WG, encouraged new companies to join w3c, clear progression of things incubating in the CG and going to the WG for standardization, multiple implementers. What has emerged - TAG review requests that come through with group chairs or editors are different from those with a chromium person as a contact. We need guidence for people in Blink team that the group chairs should be involved with registering a TAG review.

Tess: in breakout B we looked at webOTP review.. I'm an editor of one and I didn't know about the review, and the feature is in PR with issues and hasn't been merged.

Dan: it's a misunderstanding of the process

Hadley: it's what it says in blink process

Dan: they need to modify the process, so TAG reviews for things in w3c groups need to involve the w3c group people, not a review for the implementation. I can feed that back for webxr.

##### Breakout B

Peter: we left feedback on PR 262. 
... talked about WebOTP

##### Breakout C

Dan: app history API: this is big, and a priority for them. Important, looks well thought out. Ken is keen, going to make a comment. We need to do a more comprehensive review. Hopefully we can do more in depth discussion next week.
... credentialless embedder: close until they have something to propose, Yves left a comment.
... webxr dynamic viewport scaling: can this be considered a small delta? no explainer. Long response. See if we can close next week.
... file system access api: proposed close, they've listened to feedback, good responses about privacy. Closed.
... video conferencing actions: responsive to our request for elaborated explainer; answers about privacy are reasonable. Closed.

Dan: Also bumped popup to next week, noting last comment from melanie richards.

#### meta issue - how to prioritize early reviews

Peter: tooling for that in progress

#### Issue Triage

* [document.prerendering](https://github.com/w3ctag/design-reviews/issues/613) - Tess & Rossen
* [ARIA in HTML](https://github.com/w3ctag/design-reviews/issues/614) - Tess & Rossen
* [viewport height client hint](https://github.com/w3ctag/design-reviews/issues/615) - Yves & Peter
* [subresource loading with web bundles](https://github.com/w3ctag/design-reviews/issues/616) - Tess & Dan
