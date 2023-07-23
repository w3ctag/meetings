## W3C TAG Minutes - Week of 17 July 2023

### Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/07-17-agenda.md).

### Breakout A (Europe / US) - [2023-07-17](https://www.timeanddate.com/worldclock/converter.html?iso=20230717T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Detect UA Transitions on Same-Document Navigations](https://github.com/w3ctag/design-reviews/issues/834) - @hober
* [Disabling UA transitions for same-document navigations](https://github.com/w3ctag/design-reviews/issues/835) - @hober, @LeaVerou
* [WebRTC-SVC (Scalable Video Coding) ](https://github.com/w3ctag/design-reviews/issues/837) - @hober, @torgo
* [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov
* [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov

### Breakout C (APAC / Europe) - [2023-07-18](https://www.timeanddate.com/worldclock/converter.html?iso=20230718T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Sustainability of Bundling and Caching](https://w3ctag.github.io/caching-bundling-sustainability/)
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
* [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman
* [API for capturing all screens](https://github.com/w3ctag/design-reviews/issues/856) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2023-07-19](https://www.timeanddate.com/worldclock/converter.html?iso=20230719T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2023-07-17](https://www.timeanddate.com/worldclock/converter.html?iso=20230717T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Tess, Yves, Dan, Amy, Peter, Hadley, Rossen
Regrets: Yves, Lea

#### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo

Dan: this is old and has been bounced around a lot. Is this out of date?

Tess: I recall they told us they were taking a step back or reworking it. I'm not sure if we're waiting for them to come up with revisions.

Dan: **asks if I can close it**

#### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

Tess: ...linked to the agreement that we came to on [their issue 70](https://github.com/WICG/pending-beacon/issues/70#issuecomment-1525821663) ... there's [actually a PR on the fetch spec](https://github.com/whatwg/fetch/pull/1647)... I thought we should close it. Fergal said the changes are in the API... 

*triaged*

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

#### [Detect UA Transitions on Same-Document Navigations](https://github.com/w3ctag/design-reviews/issues/834) - @hober

Tess: had a conversation... 

Tess: I think this is fine.  There's something weird - a web-facing feature - exists because browsers differ on the way the render history transitions... like in Safari you do an edge swipe and you can see the page you're going back to.  It feels weird that there's a web facing feature here... but given the use case - trying to stop a doulbe-animation - I think it's reasonable to have a straightforward workaround.

Dan: privacy

Tess: only revealing one bit of fingerprinting - whether you're using a browser that has this feature (animations) or not.. It's possible that there could be a feature that changes...

Dan: API itself doesn't reveal anything about the history - simply the mechanism of the browser...

Dan: put in *proposed close* and close at the plenary?

**Tess to leave comment**

#### [Disabling UA transitions for same-document navigations](https://github.com/w3ctag/design-reviews/issues/835) - @hober, @LeaVerou

Tess: if you have a browser that has a pretty UI effect... I think it's what the user of the browser expects... If authors could cause that to be disabled it could cause the user to be confused...

Dan: it's the same explainer.. [leaves comment]

Tess: they're trying to add features to add some of the appealing user interface abilities of single page apps. The motivation seems reasionable. Detecting the case wehre the UA is doing an animation is fine, because you want to make sure you don't also do one. But if you're doing a navigation in a browser that does som ekind of visual transition as part of its basic regular operating, you're just going to confuse the user and they're going to think something is broken

<blockquote>
Hi @khushalsagar we're taking a look at this today and realized there are 2 reviews that are both referencing the same explainer. Can you give a bit more context on why these are 2 separate review requests?  For the disabling we're slightly concern that disabling a browser feature like this might cause user confusion. We're more positive on #834 where being able to detect the presence of a navigation animation seems fairly benign. Have you discussed this user confusion issue? 
</blockquote>

#### [WebRTC-SVC (Scalable Video Coding) ](https://github.com/w3ctag/design-reviews/issues/837) - @hober, @torgo

Dan: dom [got back to us](https://github.com/w3ctag/design-reviews/issues/837#issuecomment-1633748262). 

Dan: I asked Dom about the dependency on the media capabilities API.. it looked like a lot of changes... Dom said it isn't the only substantive change, but probably the most impactful one. List of PRs seems fine. Good to close?

Tess: yes I'm not worried about anything in that list.

Rossen: close now?

Dan: Happy to close now.

**closed**

#### [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov

Hadley: We've discussed in the past that this is similar to other features, like kiosk mode. But this is for launching a pop-up in fullscreen on a separate screen. 

...My privacy/spoofing concerns were that someone could use to spoof, on a second screen, a different site, including the URL bar. But they have put this behind a permission prompt, and have thought through a similar scenario (that a site is spoofing part of the user's operating system desktop instead). 

...This functionality already exists through several steps, and they're using this to collapse it down to one. Reduces developer complexity, which is a win.

Hadley: specific to a separate display... behind a perimssiom prompt is helpful. Overall functionality exists through several steps already - they're colapsing down to one step. Helps with developer complexity. Builds on APIs from second screen wg ... 

Rossen: We talked about this .. at the time we discussed simplification of existing functionaltiy - we asked why not just extend window.open. On spoofing my main concern is opening transparent windows and doing bad things... user consent is fine ... i'm worried that prompt exhaustion leads to always-open behaviour...

Hadley: it is building on window.open - they are adding a boolean "fullscreen". 

Dan: multi-stakeholder?

Hadley: it's in a working group - so multistakeholder as a working group - work done by google and intel. We can ask...

[Mozilla standards position](https://github.com/mozilla/standards-positions/issues/714)

[Webkit standards position](https://github.com/WebKit/standards-positions/issues/101)

Dan: leaves [comment](https://github.com/w3ctag/design-reviews/issues/840)

#### [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou

Dan: looks very desktop centric...

Tess: also wondering ... to what extent are browsers just free to do this already?  What's stopping browsers from doing this already?

Peter: what happens if PWA opens a window...

Dan: current behaviour is opening in an in-app view.. I think they want to be able to have this type of app already have a tab..? I don't really know how it would work on mobile. 

Peter: new tab button..  

Rossen: their use cases - more motivated by productivity apps - you want to go work on multiple docs in the same space without having to launch multiple windows... Works more on desktop...

Dan: concerned about mobile... *leaves comment*

Rossen: browsers have fairly elaborate tabbing capabilities.. I think it's a fairly simplistic use cases... Is the next thing tab groups?  browsers go to a great extent to differentiate ...  I don't think the concerns stop at desktop vs. mobile...  what about tab tearing?  I'd presume they want to have the same bahaviour...  what happens when you have 2 windows and you pull one tab to another... Also as it's a PWA why would it suddenly want someone else's UI?

Dan: *writes [comment](https://github.com/w3ctag/design-reviews/issues/841#issuecomment-1638523792)*

#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

Tess: some discussion on CSS calls... I think people are actively working on a counterproposal.

Tess: css f2f happening soon - let's hold off...

#### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

[possibly an unresolved issue between mnot and chris]

*bump to plenary*

#### [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov

[long reply to Lea, plus an ED is out]

*bump to plenary*

#### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov

[small delta? about to ship in chrome but in a web perf wg ED]

Amy: might be quick to review... *bump to plenary*

### Breakout C (APAC / Europe) - [2023-07-18](https://www.timeanddate.com/worldclock/converter.html?iso=20230718T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Amy
Regrets: Max, Sangwhan

#### [Sustainability of Bundling and Caching](https://w3ctag.github.io/caching-bundling-sustainability/)

#### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Amy: Explainer, no user needs, too high level - we asked them to re-write - they have also not filled out the security & privacy questionnaire.  No action recently.

Dan: *marks as stalled and closes*

#### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo

#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

Dan: [response](https://github.com/w3ctag/design-reviews/issues/805#issuecomment-1637273114) from them.. 

Yves: I think other browsers won't support because they won't want to give access to filesystem outside of bucket file system in general...

Dan: My suggestion is to close this at the plenary with "satisfied with concerns" - specifically the concern about multi-browser support.

**sets to proposed-closed**

#### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

Dan: they [fed back](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1620409445) on my comment from 2 weeks ago. [Number 3](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1620413725) is the thing we're concerned about.

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1639668379)

#### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo

#### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman

#### [API for capturing all screens](https://github.com/w3ctag/design-reviews/issues/856) - @torgo, @rhiaro, @hadleybeeman

Amy: feedback before is that this is an enterprise thing ... maybe not in the web platform? Their response assumes an extension is untrustworthy, but I don't understand, as in this situation wouldn't they be the ones providing the extension?

Yves: if you know that the enterprise is putting extensions on you then you know what to expect - if it's part of the web platform in general then you don't. 

Amy: ... APIs the admin might not know about.. isn't it the duty of the admin of an enterprise system to know about what they're telling their users to install/use?

Dan: ... safe to browse... 

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/856)

### Plenary Session - [2023-07-19](https://www.timeanddate.com/worldclock/converter.html?iso=20230719T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan
Regrets: Tess, Amy

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

#### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

#### [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss

#### [Detect UA Transitions on Same-Document Navigations](https://github.com/w3ctag/design-reviews/issues/834)

Peter: there was a long discussion in the CSS wg...   I don't think anything about the detection was discussed. I think this is a simple one we can just close.



#### Breakout Rollup

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

862 - "intended for adoption for all browsers"...


