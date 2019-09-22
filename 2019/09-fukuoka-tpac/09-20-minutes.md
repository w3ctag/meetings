# TAG meeting - end of TPAC 2019

Present: Peter  
Sangwhan  
David  
Ralph (special guest)  
Hadley  
Yves  
Dan  
Kenneth  
Alice  
Tess  

### WebGPU

Issue of data format of shader language... They are having a f2f next week in New Orleans. Topic for there. Either they make a decision or take the quesiton to the TAG... SPIR-V & WSL.  (WSL was for a time called WHLSL.)

### DID working group

discussion of how the working group is transitioning from a CG to a WG

### JSON-LD & I18N

r2l and l2r languages in one string/phrase - they need to come up with a proposal

### Immersive web

https://github.com/w3ctag/design-reviews/issues/403

We reinforced Alice's feedback in our TAG review github issue re the accessiblity story needs to be addressed as early as possible. specific questions on zoom and the explainer is framed around the visual UI without mentioning other modalities. 

We got good feedback from the editors. A good and constructive interaction with the working group.

* registeries vs partial enums... no design pattern
* permissions that enable stuff that is from the same source (e.g. webxr permissions vs device orientation permission) - ths also came up in media working group

[other issue on `partial`, w3ctag/design-principles#99](https://github.com/w3ctag/design-principles/issues/99)

## Media working group

* permissions that enable stuff that is from the same source (e.g. webxr permissions vs device orientation permission) - ths also came up in Immersive Web

## Mini apps (plenary day)

We issued a statement (thanks for presenting, Dan):

> The TAG has been asked for feedback on miniapps. If you were in the minitapps session you heard some of my feedback already which reflects the discussions in the TAG.

> There have been multiple efforts to sets of specifications and bring them to W3C for standardization. In many cases these have not integrated well with the web platform as a whole. A technical review from the TAG left us with the impression that the activities for miniapps have the potential risk of repeating these past mistakes. And we would like to help miniapps avoid this. Conversely, the current work on web apps are a good example of how requirements that come from a number of sources can converge on a platform that then becomes widely implemented (webapp manifest and service workers are good examples of this).
(sss)
> There have been significant amounts of work we as a web have put in to make it a powerful, secure, private, and user friendly environment. The outcome of this effort includes webapp manifest, permissions, packaging, and many other features which are now in wide use. It would be extremely useful if the miniapps community would bring their requirements and efforts to existing specifications where those exist. We would like to see a path forward where this community actively engages with the rest of the community and become a first-class citizen of the platform, even if it takes more time. These requirements need to be taken seriously by existing parties in W3C in order for this to work. Both parties need to engage.

> A CG or a task force with the WebApps group seem appropriate. It would not be a good idea for there to be a working group with the charter reflecting exclusively the needs of mini-apps because that would create a parallel webapps in w3c that is not part of web architecture. However a new working group for items that are not currently being worked on in w3c may be appropriate - as long as there is a strong connection to webapps and other appropriate group. The TAG commits to help guide this convergence effort.

A [miniapps community group](https://www.w3.org/community/miniapps/) has been created to sort out what of their work belongs in which W3C group and what needs a working group.

Some other Chinese vendors (e.g. see list of editors in the [MiniApp whitepaper from the Chinese Web IG](https://www.w3.org/TR/2019/WD-mini-app-white-paper-20190912/)) are also looking at mini-app type stuff.  they are trying to make new web dev platforms in some markets...

## Project fugu breakout

They presented; we had a bit of a discussion. Dan asked them to be more proactive in seeking feedback with other parties who aren't part of the Chromium family. They were keen to see that they put stuff in the open, and Dan said they should do more to solicit feedback. Gave the example of an SMS API, when there were alternatives. That collaboration then formed at TPAC. 

Also discussed privacy implications of some APIs (content picker, bluetooth scannning etc) they had very good stories for that. We were concerned about their attention to marginalised communities, which was reflected by others of the attendees. 

## Horizontal review

## MDN Developer survey

Incredibly useful. One of the key developer pain points is interoperability between browsers. 

## "Fugu APIs" project

some confusion on the part of 3rd parties about where to go with new API ideas - google, wicg, etc...?  

## Web incubation

Had a good discussion about where the TAG and WICG should interact. Marcos agreed to take an action to look at putting TAG review in the WICG process -- in the right place, so we aren't overwhelmed.

There is an imbalance right now because we are referenced in the blink process, but nowhere else. 

### We talked about the blink process and TAG

### WebML - only 

Web neural networks plus algabraic operations.  Tensorflow js is growing really fast. They don't want to standardize .. they were presenting from .. LMIR discussion.. 

Sangwhan: against LMIR coming to the web.

### Second Screen

They are creating a protocol. Looking at integrating with webcodec proposal, want to use QUIC... 

### WebBluetooth

Discussions around the scanning thing - the legacy APIs, should they improve them. Big discussion of abort controller... this also came up about wakelock...  Design principles issue filed.

### Devices & sensors working group

They are moving the battery status to only work on secure origins (secure contexts)...

### WebApp Manifest (in webapps)

There is alot of interest in new things like shortcuts... dark mode... minor things.. Microsoft is working on this. [samsung also working on this]

### Badging API

They had taken TAG feedback and redesigned it... and we redesigned again.  And it has ended up in a place that works well.  Tess will sumarize the conversation we had on our existing issue and then close it.

### Highlight API

Tess: Interacts with other parts of the platform ... a way to categorize, collaborative editing selection mode, spell checker, etc... many touching a lot of things.  the model they came up with was independent from DOM and conversation here was about how it should be closer to DOM.  Some progess made.

Alice: any accessibility discussion?

Tess: not with me.

Explainer link: 

Hadley: Exit, pursued by danbri.

### Horizontal Review Session

Tess: Highlighted that we need to have clarity with other groups that are also part of wide review. Opportunity we should follow up on.

Dan: the idea of a horizontal review dashboard came up; would like to see this

### Media Working Group

Tess: we talked about emerging media proposals and how they tie into existing work - things happening in many groups ... media wg could do unofficial horizontal review.

### Bots for chairing

Tess: Ada ran this [session](https://www.w3.org/2019/09/18-groupautomation-minutes.html) on wednesday and highlighted new API features & stuff.....

### Service Worker Scope & Manifest Scope

David: I had discussion on this - on our TAG review issue for service worker scope stuff.. 

Yves: another proposal from ben kelley : scope matching... 

### Permissions & Feature Policy

Sangwhan: many thoughts and feels on this

### Accessibility tripwire checklist

Alice & Sanghwhan worked on this - 
Related work from Michael Cooper: https://www.w3.org/2019/Talks/0516_FAST_MC

### Houdini

Peter: Font enumeration - folks from Apple pushing back - suggestion to drop in favor of a font picker... Fingerprinting and privacy issue. The API may be dropped.

### Trust Tokens Session in Plenary Day

https://github.com/dvorak42/trust-token-api

### Portals

Peter: they are making better use of fallback content.  

Peter: We had a discussion with them about the feedback we gave in our review.  Expose this as a set of lower level primitives and let's fix iframe...

### ServiceWorker

Yves: Some issues around periodic background sync... lots of discussion about scope matching, routing... 

Ken: They want to restrict the design of the URL pattern... fruther allow certain uses of the API to disable certain features...

Dan: service worker development and debugging are big issues I am hearing from developers...

Ken: tooling like WorkBox can help.. 

Dan: & PWA 

### GamePad

Yves: Meeting with WEBXR.. Good coordination. identification of a particular gamepad. They decided to have a gamepad available only after user activiation...

### Fingerprinting

It sucks. Need to remind people of [Unsanctioned Web Tracking](https://www.w3.org/2001/tag/doc/unsanctioned-tracking/).

### Sangwhan's notes:

Open JS Foundation - not sure what exact role is, but something new

Hosting reference polyfill projects in Open JS foundation

Making stuff potentially work on non-web

*WebCodecs* - video/audio stream decoding api

Opens up some potential for image decoding (which is something the platform lacks) - unfortunately out of scope, will follow up

*WebML* - some issues with scoping of functionality - like how to do custom operations and whether or not that should even be possible. Will follow up. vv

*WebGPU* - shader format conflict - asked for API level review when there is something (sans-shader format)

Have some unaddressed questions on current main thread execution design

*Audio WG* - working on a new dedicated realtime priority audio worker proposal (needed as process priority in anything else is not realtime), early design to be raised as a review to us

#### Permissions, quasi-permissions, and feature policy

Got a hold of previous editors, had a 1h discussion - lack of other implementor interest is a current bottleneck for API

Naming consistency issues

Same source different permission is a problem

Permissions and feature policy parity (permissions should always have a corresponding FP)

We need a name for quasi-permissions, and define it somewhere

*Publishing* will collaborate and potentially make radical design changes to audiobooks

Will also be looking into bundled exchanges in depth

Provided some actionable improvements for throttling/triaging reviews toward Blink people

James, Alice, and I worked on a a11y quick checklist. Shared on core-tag.

#### Failures:

Webauth - nothing. Not in agenda, walked out.

WebTransport.. did not have enough time to get a hold of the people behind it, did discuss 
with mnot and at least mnot wasn't wildly against it

### Open JS Foundation

Dan: they might be able to help by opening projects when a W3C spec has new APIs

Ken: and polyfills