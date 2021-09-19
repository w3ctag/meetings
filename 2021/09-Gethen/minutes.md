# TAG Virtual F2F - Gethen

Week of 13-September-2021

[Agenda](agenda.md)

This W3C Technical Architecture Group virtual face-to-face meeting was held as a series of 26 breakout slots over the course of the week of 13 September, 2021. The mintues are presented as breakout notes and are not necessarily chronological.  Many of the breakout slots are subdivded into breakout A and B - in which case a note of who attended each breakout is made.  In some cases there are some additional "rollup" notes presented in line where additional substantive discussion took place. 

Present at this F2F:

* Daniel Appelquist (Samsung Electronics) (Chair)
* Rossen Atanassov (Microsoft Corporation)
* Hadley Beeman (W3C Invited Expert)
* Kenneth Rohde Christiansen (Intel Corporation)
* Amy Guy (Digital Bazaar)
* Yves Lafon (W3C) (staff contact)
* Peter Linss (W3C Invited Expert) (Chair)
* Sangwhan Moon (Google)
* Theresa O'Connor (Apple, Inc.)
* Lea Verou (W3C Invited Expert)

### Session 1A

Present: Peter, Tess

#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399)

Hasn't been updated since January, no response to our request for update in May. [Closed](https://github.com/w3ctag/design-reviews/issues/399#issuecomment-918635792) with an invitation to the OP to reopen when and if they're ready.

#### [Raw Sockets API](https://github.com/w3ctag/design-reviews/issues/548)

Hasn't seen any updates in 1 year; the major issue in their repo related to the last round of TAG feedback hasn't gone anywhere either. [Closed](https://github.com/w3ctag/design-reviews/issues/548#issuecomment-918637185) in the same manner as the previous issue.

#### [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594)

The two of us looked at this in a previous F2F, and left a bunch of comments that Domenic addressed in a followup. Overall we both think this is basically fine, though we're still worried that "adding a bespoke <var>X</var>Watcher object to the platform for every <var>X</var> in the future wouldn't be great. [Closed](https://github.com/w3ctag/design-reviews/issues/594#issuecomment-918641861).

#### [CSS Display Level 3](https://github.com/w3ctag/design-reviews/issues/673)

Looks fine to us. The [changes](https://www.w3.org/TR/css-display-3/#changes) are bug fixes and smaller tweaks for the most part. [Closed](https://github.com/w3ctag/design-reviews/issues/673#issuecomment-918643832).

### Session 2A

Present: Tess, Rossen

#### [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) 

Rossen and Peter had a breakout about this some time ago in which they convinved themselves that this isn't a great approach. Rossen [closed with a comment](https://github.com/w3ctag/design-reviews/issues/579#issuecomment-918681465) that captures their thinking.

#### [Review Request for prefers-contrast media query](https://github.com/w3ctag/design-reviews/issues/663)

They wrote [a lovely explainer](https://github.com/w3ctag/design-reviews/issues/663#issuecomment-902980687) as a comment on our design review issue. Tess [asked](https://github.com/w3ctag/design-reviews/issues/663#issuecomment-918677100) them to find a more permanent home for it.

Otherwise things look great. [Closed with comment](https://github.com/w3ctag/design-reviews/issues/663#issuecomment-918685145).

#### [MSE-in-Workers](https://github.com/w3ctag/design-reviews/issues/656)

Good to see the [open questions](https://github.com/wicg/media-source/blob/mse-in-workers-using-handle/mse-in-workers-using-handle-explainer.md#open-questions) section in the explainer, and [multi-vendor interest](https://github.com/wicg/media-source/blob/mse-in-workers-using-handle/mse-in-workers-using-handle-explainer.md#implementation-status-as-of-last-update). It's not fully parallelizable, which is probably okay. It gets the hard work off of the main thread. And they don't end up needing any author-facing complicated locking, which is nice.

[Closed with comment](https://github.com/w3ctag/design-reviews/issues/656#issuecomment-918694564).

#### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639)

Tess: I don't like the name of the DOM attribute or attribute value, because it's not credentials that are being omitted, it's storage, and it's not so much that it's omitted, it's that you get a new, one-off partition. I think the open [issue 20](https://github.com/camillelamy/explainers/issues/20) captures this concern.

[Commented](https://github.com/w3ctag/design-reviews/issues/639#issuecomment-918700758).

### Session 3B

Present: Ken, Sangwhan

#### [Add `id` member to web application manifest spec ](https://github.com/w3ctag/design-reviews/issues/668)

set to proposed close

#### [Review of AccessHandles for the Origin Private File System ](https://github.com/w3ctag/design-reviews/issues/664)

closed

#### [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644)

closed

#### [User Timing ](https://github.com/w3ctag/design-reviews/issues/642)

closed

#### [Resource Timing](https://github.com/w3ctag/design-reviews/issues/641) 

closed

## Session 3B

Present: Dan, Amy

#### [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595)

Amy: last update is that this is blocked on FPS

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342)

Dan: Last discussed in [Privacy CG last week](https://github.com/privacycg/meetings/blob/main/2021/telcons/09-09-minutes.md)

Amy: the enforcement stuff doesn't sound like it belongs in a w3c spec

Dan: agree

Yves: getting traction from different vendors... position of power with regard to who you accept. 

Dan: would be an interesting data point to know if another browser is interested? The last I heard from MS was that they were interested in a technical-only enforcement. In the PrivacyCG minutes Kaustubha talks about the policy thing.. Asks "Do we think controllership is publicly-verifiable?" and gets into enforcement policy of who gets to be in a FPS

Yves: how do you enforce that?

Dan: right? What's the redress mechanism if it's wrong? 

Yves: can it be user overridden? Should the user say two companies should be differnt things?

Dan: and in some countries the regional data authority thinks they're different things even with common ownership. We keep pointing out the issues with having some kind of enforcement mechanism that is not technical and we should be stronger on that point

Yves: mitigation could be giving the user the possibility to split FPS? and opening the gate to extensions that can do that

Amy: Concerned about that - pushing it to something else - ie an extension - to address the privacy harms... Lots of people aren't going to bother with extensions or sorting FPSs themselves even if there are privacy harms

Amy: data on ownership of legal entities - there's little to no public data on beneficial company ownership. IEE is a concept they've invented.  There are hoards of investigavie journalists spending all their time talking about company ownership structures... It's not realistic just saying 'we can look for some company ownership data' - they get to some of this later in the privacy cg minutes

Dan: Different in every country - the feedback should be - this is not stuff for a w3c spec

[reviewing open PRs on First Party sets](https://github.com/privacycg/first-party-sets/pulls)

Dan: [PR 65](https://github.com/privacycg/first-party-sets/pull/65) still mentions enforcement agency..

Amy: not sure of enforcement agency becomes optional - could be multiple? - or still a requirement

Yves: how it works across international borders... It's moving with discussion in privacycg, on hold until they have a statement?

Amy: worried about a technical-only enforcement thing - it may only be solvable as a legal/jurisdictional issue which just puts it out of scope for w3c.  Maybe the discussion can continue and they need to figure something out... but maybe it's not possible.

Dan: Maybe first party sets technical spec just needs to punt on the enforcement and say it's out of scope for w3c?  But then that opens the door to...

Amy: saying 'how are you going to enforce this to avoid abuse?'

```
Hi we are tracking some good discussions going on in the [Privacy CG](https://github.com/privacycg/meetings/blob/main/2021/telcons/09-09-minutes.md).  It looks like there is some substantive discussion going on there about enforcement policies.  Our view is still that any kind of centralized policy-based enforcement of which parties may claim to be together in a set is problematic and that a technical-only enforcement mechanism may be preferable. However they may not be a technical-only enforcement mechanism that works in the real world because of the complex structure of ownership of legal entities and data sharing legislation globally.  We await the outcome of these discussions in the Privacy CG and would be happy to spend time reviewing PRs as appropriate.
```

Amy: asked https://github.com/privacycg/first-party-sets/pull/45#pullrequestreview-689239363 :

```
In general I think I'd like to see a lot more about what happens when a UA doesn't implement FPS when others do (including what happens to older browsers that are never going to get updated); and when different UAs ship with different FPS lists. How badly can things break from an end user pespective, and from a site owner/admin perspective?

The case I'm particularly worried about is sites blocking access to UAs that don't implement FPS (because they're old, or because they choose not to for privacy reasons) or users who have FPS turned off.
```

... but don't see a response, will open [an issue](https://github.com/privacycg/first-party-sets/issues/66).

Amy: interesting [issue about purpose of FPS](https://github.com/privacycg/first-party-sets/issues/62)

#### [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) 

Amy: didn't we agree to close this? It's proposed close

Dan: Hadley drafted feedback but it was never posted [in minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/08-30-minutes.md)

```
Hi all, 

We've discussed this in our W3C TAG meeting today. We want to thank you for a thorough and helpful meeting on this and COOP/COEP.

We want to summarise our thoughts here, so that we have the notes in one place, and then we'll close this issue. 

Our thoughts:

* We are concerned about anything that adds complexity to the web, confusing developers and making it harder for developers and site owners to produce websites. This proposal is substantially complex, though it does offer big benefits especially to users. 
* We are still interested to hear how use cases develop. In our meeting, we asked if there was an assumption that, for example, a bank will never want to surface a PDF of a customers' bank statement on another origin. It sounded like you might discover that that use case does — or doesn't — actually occur in the wild. It will be interesting to hear how the various groups impacted by this respond.
* We started a discussion with you all about how to shift the defaults on existing content to benefit from this proposal. On the one hand, that could be a very substantial shift for the web, which is always challenging. On the other hand, we are still behind our [Evergreen Web](https://www.w3.org/2001/tag/doc/evergreen-web/) finding and recognise that everything needs to upgrade. So we are interested to hear, in due course, how you want to explore this.

Thanks again, and we'll be keen to see how this develops. Please do come back to us as you learn more from your work.
```

**[CLOSED]**

### Session 4A

Present: Ken, Sangwhan

#### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512)

set to propose close

#### [WebCodecs (again!)](https://github.com/w3ctag/design-reviews/issues/612)

closed

#### [Pen Events API](https://github.com/w3ctag/design-reviews/issues/553) 

still waiting for feedback

### Session 4B

Present: Dan, Amy, Ken

#### [Ethical Web issues / PRs](https://github.com/w3ctag/ethical-web-principles/issues) 

https://github.com/w3ctag/ethical-web-principles/pulls

https://github.com/w3ctag/ethical-web-principles/issues

Dan: on [deprecating the term user](https://github.com/w3ctag/ethical-web-principles/issues/34) - draft [comment](https://github.com/w3ctag/ethical-web-principles/issues/34#issuecomment-918905123).

Amy: Agreed. Will [draft PR](https://github.com/w3ctag/ethical-web-principles/pull/46) which can close the issue.  

Dan: I think we can confidently merge this and if Hadley disagrees with some of the changes she can raise an additional PR.

Amy: agreed.

Amy: Talking about environmental sustainability - we have a [PR](https://github.com/w3ctag/ethical-web-principles/pull/31) but we agreed that this is too wordy and refernces right-to-repair which is out of scope for us. I will write a simpler [PR which capures the feedback in an additional sentence](https://github.com/w3ctag/ethical-web-principles/pull/47).

Dan: Closed issue on link to latest published version.

Amy: let's make sure we publish the latest version after our f2f.

Amy: [dark patterns pr](https://github.com/w3ctag/ethical-web-principles/pull/48/)

### Rollups on 3a,b and 4a,b

Sangwhan: closing stuff - 6.2 web codecs - usable - we clarified our message.  From their end window vs worker has been closed - it's resolved.  If there are strong objections about closing.

Dan: suggest we close it.

Sangwhan: [payment request](https://github.com/w3ctag/design-reviews/issues/512) think we should close it ... Was waiting for more feedback from Tess, but has been open for a very long time and the ship has sailed.

Dan: sounds good.

Sangwhan: [access handles](https://github.com/w3ctag/design-reviews/issues/664) - filesystem in the name - has already been addressed in fs api.  performant way of getting access to file handles..  New feature to address problems. We were happy and had thoughts about the naming but don't have better ideas.

Ken: nitpicking, it's fine

Dan: sounds good.

Sangwhhan: [ID numnbers](https://github.com/w3ctag/design-reviews/issues/668) - addresses updating PWAs packaged - e.g. from google play - you proabbly don't want 2 different PWAs... if you 

Dan: would it override one if I installed in two different browsers?

Ken: I think it would ask..

Dan: I don't think that's good [clarify: developers often want to have multiples of the same PWAs installed via various browsers for testing purposes]

Ken: implementation detail - this is about being able to identify them as being the same

Sangwhan: separate discussion about default handler - should it be the same as the default browser. Implementation detail, and not for this review. In this,they introduce ID field into web app manifest. Ties into startup URLs origin. chat.google.com + some identifier that says this is google chat. So if you install through google play and try to update through the web it'll update on that end, regardless of which path you take you can update and not end up with two google chat icons.

Dan: sounds good

Sangwhan: this is an incremental improvement... MiniApps want this functionality, they tried to introduce something to address a similar use case, someone should make them aware this is happening. Good with current proposal and would like to close.

Dan: close it!

Sangwhan: will do

Amy: We closed COOP same origin becuase we proposed close a while ago - posted Hadley's drafted feedback. Also left more comments on FPS. And noted that sameparty cookie is still blocked by its dependency on FPS. Also we did some PRs on Ethical Web Principles, merged one, some still open for review. We'd like to publish a new version in tagspace at the end of the week.

Yves: automated publishing is coming soon, but can do a batch publish after the virtual f2f

### Session 5A

Present: Yves, Peter, Rossen, Dan

#### [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572)

Yves: protecting things on private networks - but requires devices to implement this specification. I was wondering if it woudl be better to ahve the browser do some gatekeeping... Using MDNS these local services broadcast if they are on local network - browser could listen to those... and then the browser filter the request to anything on local network to see if it's accessible or not.. to access devices that are not up to date.. http not https, ... here it requires devices to be updated.

Rossen: In model you described - shift the responsibility into the UA - requires any UA to have similar capabilities -- Slack, Email client, chat system, to implement the same or similar capability. That approach is seemingly spreading that problem... 

Yves: this is for something where the main page is on the internet but you want to talk to something on your local network... 

Yves: printers.. advertises itself as e.g. airprint device... can be accessed using http. If the browser forbids all request on local network - allow only things that are advertised... ask the user "do you want to be able to share it" with external pages... user can say yes or no.

Dan: could that become a fingerprinting vector...

Yves: maybe if you have ways to list all devices...

Dan: Web Bluetooth e.g. provides a browser mediated choose function and does not provide a list back to the web site...

[discussion of risks associated with home applicanes]

Rossen: It's even worse when access is granted to gas stoves or vehicles, cars etc. 

Dan: they need to address the issue of how to deal with legacy devices...

Peter: I don't think everything that broadcasts mdns should be easily accessible this way - e.g. security cameras...   Other issue is that we have the issue of a general service discover mechanism - this should be tied into that.  I think the MDNS idea is good but there needs to be a user prompt in the way...  Also I do like that they called out that the UA can specify ipv6 public ranges as being public...

[Discussion getting into the ipv6 weeds and what constitutes a private address in an ipv6 network...]

Yves: should we consider local networks.. everything behind the router? what's in the rfc?

Peter: it should be configurable.  They did take it into account tho it's weak - a "may".

[yves to leave comment]

#### [MediaStream Image Capture (wide review)](https://github.com/w3ctag/design-reviews/issues/651)

Peter: I asked some questions - no response... I will copy the feedback to their repo....

Sangwhan: interesting API.

[later on]

Rossen: I'm ok to close.

[closed]

#### [Device Posture API [formerly Screen Fold API]](https://github.com/w3ctag/design-reviews/issues/575) 

Dan: One implementation (behind flag) in Samsung Internet right now.

Peter: ...in the example they showed a relatively modern device - that use case not covered. Existence proof of this device...

Rossen: one feedback - even motivational icon shows mutliple folds but current proposal iis for one fold.  On flip side I've asked for more use cases... They pointed us to the spec which does have one but only for the single fold scenario.

Peter: I think the problem space is complex - and the feature is too simple. Not sure it's moving in the right direction.

Rossen: but isn't it? by popping their capability higher...

Dan: moving towards more semantic description for designers...

Peter: but what do I do with that?  How do I know where the fold is?

Rossen: this is addressable.  The base : we have capabilities that are exposing pieces of screens - hinges, seams, magnets.. etc... this current one is not talking about this. It's describing the postures of devices with screens one or many...

Peter: there are other specs that will provide that info?

Rossen: yes - the media query 

Peter: i know there are multiscreen apis - how does this fit with the other specs?

Rossen: this (high level) with the spanning capabilitiy - where essentially you can 

Peter: if I have to go to 2 or 3 other APIs can't I get the info this is giving me fromn those APIs as well?  Is this useful?

Rossen: you could ask the same about @media print.  You know that you're in that environment.

Sangwhan: what media queries?

Rossen: a few different environemnt variables describe where the fold is... 

Sangwhan the fold is that you have a foldable screen.

Rossen: it's the same thing - a tent - you know where your origin is and know what your width and height is... 

Rossen: is there a media query or function today that describes this?

Dan: so would it be good feedback to ask they to explain in their explainer or spec to be specific about how authors are supposed to use ths API together with other environment variables and othert mediat queries?

Rossen: they've answererd that question. See https://w3c.github.io/device-posture/#example-2-adapting-ui-to-posture

Peter: Can't judge the usefulness of this - is it giving me useful info.

Sangwhan: Agree.

Rossen: Kind of neutral - what this bubbles up to - you have the high level media trigger - this device posture changed - there may be posture chanegs where you don't care.  From the pov - this top level switch is useful.  In the examples they give in the spec the device posture alone is not useful because you also have to look at the spanning - so you could describe everything with the spanning. When I worked on this with the folks that produced the spanning - nobody used e.g. portrait and landscape because people used the metadata. You cannot react to the posture alone and adjust your layout.

Peter: this adds one and a half bits of info - does that exist anywhere else... 

Rossen: i don't think the answer is yes.

Sangwhan: I have the same question...

Peter: in their example they say "the spanning and the posture" - do you need the extra bit of the posture.

Rossen: if you go from a laptop - and fold it flat - so one big screen - spanning works so you change the origin and orientation of both screens.

Peter: this adds tend mode - folded over... Then I'm looking at both screens.  If the spanning did not change then it adds useful info.

Sangwhan: There is a big picture here but we are only being shown a piece of the puzzle. I think we should ask for a review at the point they have the landscape sort of planned out. Either that or a landscape explainer.

Rossen: changing from screen to page you have to restyle... here you're notr eally changing.. By abstractig the spec to this level - lost the angle. 

Peter: i think it's moving in the right direction... 

Dan: I think asking for a landscape document.. sounds like a good idea.

### Session 5B

Present: Tess, Amy

#### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414)

Tess: waiting for an update from them

#### [Design Principles issues / S & P Issues]()

**[Principle about identity](https://github.com/w3ctag/design-principles/issues/324)**

Discussion on issue... ongoing open topic. Requires novel research which is out of scope for TAG? Close? There's no obvious right answer that could be incorporated into design reviews at the moment. But might send the wrong message to close as it's a pertinent issue. Leave it a bit longer.

**[Crypto principle](https://github.com/w3ctag/design-principles/pull/310)**

Giant comment on the PR.. ultimately questions validity of principle in th edocument, critical of WebCrypto as a gold standard.

Tess: re the comment.. design principles aren't comprehensive.. want to push back that it doesn't belong.. Maybe over time we'll end up with more so it feels less out of place, driven by design reviews

Amy: [suggested change to remove the bit about WebCrypto](https://github.com/w3ctag/design-principles/pull/310/files#r708375484)

**[Two new principles](https://github.com/w3ctag/design-principles/pull/320)**

Tess: approved, Sangwhan anticipated my concerns

**[Non fully active documents](https://github.com/w3ctag/design-principles/pull/317)**

Tess: [merges]

**[Non fully active document in S&P questionnaire](https://github.com/w3ctag/security-questionnaire/pull/128)**

Tess: [merges]

#### [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) 

Tess: doesn't really make sense as a design review issue

Amy: agreed

Tess: mentioned in Trust Token API thread. Close?

Amy: check with Peter..


### Session 6A

Present: Ian, Peter, Ken, Rossen, Tess

#### [Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/544)

Ian: Just to context set... web payments wg started in 2015 to streamline payments. The two main initiatives were to (1) reuse stored browser data -- enhanced autofill -- for 1-click payments and (2) connect digital wallets --payment apps-- to the web. The first did not catch on. The second has seen some implementation but has not taken over the web. But it has allowed for experimentation, of which SPC has been one.

While this was going on the payments community at w3c grew larger and stronger. In parallel we saw new ideas that bridge web payments and auth in order to satisfy use cases and some of the new EU compliance requirements ("PSD2"). Stipe did an experiment with impl in Chrome leveraging payment request API and payment handler API giving them the ability to interact with Banks (in a 1p context) as authenticator and handler - a first experiment using these capabilities as a pair.

In the future we expect to move away from payment request API. But I wanted to provide this background for why SPC is grounded in PR API.

One reason for urgency regarding the deployment of this API relates to the timing of EU requirements for strong customer authentication (SCA) for many transactions, as well as evidence that the user consented to the payment ("dynamic linking"). 

SPC involves user experience (modal window to confirm a transaction). There are two communications between the caller and the RP. The first is to get a list of SPC / FIDO credentials as input (along with challenge, amount, etc.). The second is to send the resulting assertion to the RP for validation. SPC is thus integrated into "back end" protocols, some of which may be standardized and others proprietary. Our current particular focus is integration into EMVCo's 3-D Secure, which is seen as an important tool by the ecosystem for fulfilling the EU regulations. But we are also having discussions about other integrations (e.g., EMVCo's Secure Remote Commerce and various Open Banking APIs in Europe). 

This is how we got here with regulatory pressure and industry experience. A 2nd experiemnt between AirBnB and Adyen is happening and Stripe will be doing another one.

Tess: it's been a while since I looked at this. Lots of discussion taking place last month. Let's review these first.

(discussion about current comments)

Tess: Originally I had some minor issues around payment .... I am happy with the responce around the fact this is helping especially for existing form-based payments.

Ian: Here are use cases where I think SPC can be helpful:

* Form-based payments. That's what the first Stripe experiment showed.
* Card-on file payments. (Merchant or their payment service provider stores instrument information)
* Pay buttons (e.g., on click payment service fetches SPC / FIDO credentials from server using cookie-stored user identity; triggers SPC; sends assertion to server for validation; completes payment without ever requiring login).
* Digital wallets (who may want SPC above and beyond FIDO for the dynamic linking/transaction confirmation functionality)

Ian: All of these would involve a similar user experience. From arch perspective, SPC relaxes the WebAuthn same-orgin policy. Thus, any party may authenticate using the RP's credentials. We believe this does not create risks that payment will happen by mistake because in the end the RP needs to validate the assertion and will only allow payment if satisfied with the entire transaction context, including what SPC provides evidence for.

Ian: Second arch diff from WebAuthn is the ability to register in cross origin iframe. Chrome initially required a modal window in order to draw attention to the user. But they changed their mind and so the implementation currently does not involve a browser-owned notice during registration.

Ian: Let me back up a bit:  the payments industry dislikes user friction. In this pursuit we want to have one fido registration used anywhere. Ideally with one registration you could authenticate from any browser, on any merchant web site, with that merchant using any PSP, and so on. There will be a variety of use cases, not all of which will achieve that ideal (e.g., where the PSP is the Relying Party rather than the issuing bank). Architecturally to get there, we'd like to leverage discoverable credentials, caBLE, and other Web Authentication aspirations. So we anticipate that SPC will stay close to WebAuthn to take advantage of these. In the meantime, the current API description includes some temporary "fixes" such as cacheing credential IDs. That is going to allow us to get some experience right away with SPC, but we anticipate over time that SPC will further converge with Web Authentication. In the long term, the main "non-WebAuthn" functionality will be the dedicated transaction confirmation dialog and the signing of transaction details.

Ken: So this should work with and without payment requests. 

Ian: Yes. I think there is some agreement that SPC should not (moving forward) be closely tied to Payment Request. You should be able to use SPC on its own without PR API, in conjunction with PR API, and also from a payment handler. However, you can't use a payment handler today given SPC's implementation as a Payment Method.

Tess: This is a complex problem space with so much domain specific info, thank you for all the explanations Ian. 
It looks like it is in a good shape. When we design APIs in a vacouum we don't always see the rest of the industry or user cases. This one has a lot of thought and reason to get it to this point.

Ian: The 3PC removal will, I think, have a dramatic impact on payment ecosystem operations. We thought trust tokens might help but they can't since they're not really bound to anything. (explains a payment use pattern) 
So in summary, the payments world will need architectural help with identity, risk mitigation, authentication, and instrument selection.

Tess: So next steps are to create a new issue. Let's get this one reviewed and sign off on it as the current state seems very reasonable. Some of the open questions aren't necessary concerns to TAG and could be worked in the respective working groups, you're already doing this.

Ian: I think you should review in particular the security and privacy considerations. The Crhome team has been doing great work and helped us clarify a lot of considerations identified there. 

Tess: Sounds good.

#### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532)

Still waiting for feedback

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509)

Stalled - waiting for feedback

#### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) 

Blocked behind first party sets

### Session 6B

Present: Amy, Dan, Sangwhan

#### [API for display-capturing the current tab](https://github.com/w3ctag/design-reviews/issues/625)

Dan: recent [comment](https://github.com/w3ctag/design-reviews/issues/625#issuecomment-910462274) lays out a position from Google ... we have to consider both of these issues in parallel. Elad is saying that the thing they're proposing in 625 is a temporary measure, maybe we should be saying that's great okay but why won't that then become the de facto thing that people use? The web is full of short term measures that became the long term  unfortunate thing.

Sangwhan: a lot of people are using this feature without realising its Chrome only - it's not standardised

Dan: [shares tab using the API described in 625]

Sangwhan: a lot of people are using this - though it's only implemented in chrome.  I think the trade off given the situation we're in is something we're going to have to live with.

Dan: Why don't we say we appreciate .. `thank you for clarifying that #609 is the long term proposal, we will focus our efforts on reviewing #609. Can you provide a roadmap for how you see transitioning people from use of this API to what is described in 609 once the issues are resolved?` Eg. would 609 be layered on top of 625? Based on that we could propose closed.

Dan: why is it called preferCurrentTab? [comment left](https://github.com/w3ctag/design-reviews/issues/625#issuecomment-919292704)

#### [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) 

Sangwhan: 609 we're supposed to provide feedback on path forward in terms of security. Breaks the origin model?

Dan: you can already share the screen? If you're sharing the screen what's the difference with sharing the tab? if you're sharing the screen that has that tab on it your'e doing the same thing. Firefox already lets you share screen.. you're not sharing the DOM, you're sharing an image of what's in that tab. The pixels. 

Sangwhan: there's a slidedeck.. the more secure proposal.. it was quite subtle but valid, but I don't remember the details.

Dan: we could ask for additional information and with that we can close the 625.. we're not being asked to review 625..

#### [Pickling for Async Clipboard API](https://github.com/w3ctag/design-reviews/issues/636)

Dan: they made some changes in format naming and how custom formats are read/written and want feedback

Dan: [still the basic issue with the async clipboard api](https://github.com/w3c/clipboard-apis/issues/52#issuecomment-875709431) as speced doesn't require a user gesture to read the clipboard - the issue is still oepn but other documents treat it as resolved.  

Sangwhan: it's hard to resolve - web ui component that makes a menu that tricks them to give access to the clipboard.  If you restrict it to ^c, ^c equiv - it's ok. Once you self define your ui then all bets are off.

Dan: Safar chose to go with the ^c ^v equiv option... just the native system shortcuts.

Sangwhan: you could put the user gesture in the accept cookies dialog and people will just click yes and the site gets access to the clipboard. If you restrict to just the native system context menu system shortcuts that's fine but it alienates the mouse clicking user who has to go through the menu to find copy and paste

Dan: we discussed with Alex Russell, it leads to a situation where it's possible you could have a password or other sensitiv einformation sitting on your clipboard and you bring up your browser, navigate to your tab, no user gesture, and that tab has access to the contents of your clipboard and I don't think that's acceptable.

Sangwhan: if you have given permission

Dan: if you've given permission *previously*. Not a user expectation that if you've give permission previously.. I've given permission to paste things into MSWord, doesn't mean I think MSWord is going to snoop on my clipboard. People have lots of private data in their clipboard. This is a separate issue, but I feel like we left a comment which is that there are abuse scenarios not being given enough weight. This is the problem - this issue is open - but people are saying it's already decidedin the async clipboard api - if it's decided, why is the issue open? It's been two years.

Sangwhan: agree with the principle and the risks. I don't have a solution.

Dan: it's a timebomb until somebody .. this is a huge door open for websites to snoop on your clipboard

Lea: I agree.. but it doesn't seem to be related to the pickling proposal

Dan: the issue is that this proposal calls out the fact that pickled contents of clipboards can be more damaging, more snesitive, but doesn't specifically says they can't/won't implement any additional gesture requirements or UI requirements because it's dealt with in the async clipboard api. They said because async clipboard doesn't do it we're not going to do it.

Lea: I thought the examples about private data being leaked would not require pickling

Dan: what if you had an image of your child on your clipboard?

Lea: what happens today without pickling? 

Sangwhan: image works fine right now. You don't need pickling for image support.

Lea: many applications already allow this

Sangwhan: if you do something like copy something from Sketch, a bunch of objects, then paste in the web, that becomes garbage. Either rasterizes or do nothing, or post garbage on the screen.

Lea: if there's any sensitive data in what you're copying it will still be leaked if you try to paste it today..

Sangwhan: with the current status you can get away with that as well

Lea: users try to paste whatever is pasteable, they don't know what the platform supports or what the web app supports

Sangwhan: even without async clipboard you could still access the clipboard, and that would mean you can access the problematic data. This has been here for a while. Once you have clipboards, unless you say we have a standardised way of saying all password like things or sensitive data has to be serialized in this way so every browser implementation can not leak it.. that's going to be a massive project

Dan: we should focus on the pickle aspect of the proposal, and in our closing comment we can say the clipboard access is still problematic, though we said that before and nothing happened

Sangwhan: yes. One thing pickling does let you do is you can put in carefully crafted payloads to blow native apps up. Which you couldn't do in the past. If you have.. given you can make someone click on an accept all cookies button, even if you gate writing to the clipboard behind a user interaction, if you know someone uses MSWord 2015.. you could craft a malicious payload that is targeted for MSWord 2015, hide behind accept all cookies dialog, when that user interaction happens write it to the clipboard, and hope they paste into MSWord2015 and it crashes and you get native execution.. this is hypothetical.

... Other question is how much stuff can you pickle into the clipboard? Could also use it as DoS if there's no upper limit. Here's 10gb of data into the clipboard..

Lea: can't you do that already?

Sangwhan: you could, I think...?

Lea: stuffing extra data in what they copied.. have you copied data from an article to find it has more sentences tucked into it? If they wanted to do DoS that way they could stuff in gb of data.

Sangwhan: you could just write 2 million characters in the DOM. But I think the deserialization delayed bomb is probably somethign theoretically possible. The thing is that right now images are sanitized when you copy them into the clipboard. Web images are sanitized by the browser in a way that it takes away some of the dangerous bits (but also loses some information, eg. colour spaces). The reason is because of the attack surfaces associated with that. Once you are allowing aribtrary deserializable data into the clipboard you have the problem that you don't know how to sanitize because you don't know how to deserialize. That's the risk that comes with this. We can't say we will never allow anything complex because then the web can't do complex stuff. Eg. you can't make autocad for web because we only allow rich text and images.

Lea: do we have something to suggest to make this more secure?

Sangwhan: I don't think so.. they spend all their time thining about this problem probably becuase it's the most risky aspect of this feature. They do bring this up in [this section onwards](https://github.com/w3c/editing/blob/gh-pages/docs/clipboard-pickling/explainer.md#caveat-unclear-clipboard-format-source-on-read). They have thought about this. I personally say it's worth an origin trial to see how the real world implications and applications can make use of it and what kind of limitations are hit. I'm sure there are plenty of things that have to be ironed out. I'm okay with this proposal, I'm sure there is some extra stuff that will need to be considered once we try to integrate this into an existing application, eg. something like Figma. What happens when you copy from Figma to illustrator? From Illustrator to Figma? Sketch to Figma?

Dan: I think tha'ts out of scope.. you're talking about something needed to be implemented by figma..

Sangwhan: more like can figma actually implement deserialzing something copied out of Sketch. This is a whole new beast.

Lea: this is the primary use case? being able to copy data like this from applications to web apps and vice versa?

Sangwhan: yeah. It would be interesting to see the origin trial and the feedback from different services interested in this.

Lea: we should probably phrase it in a way that is not chrome specific?

Sangwhan: makes sense

Dan: can just say trial

#### [Shared Element Transitions - Early Review](https://github.com/w3ctag/design-reviews/issues/631)

Lea: we delayed this because of a [CSS wg breakout on this topic... ](https://github.com/w3c/csswg-drafts/issues/6464#issuecomment-911788061).   My takeaway so far - the discussions around these shared element transitions - without getting too low level into the detais...  have not seen a complete proposal that addresses the multi-page transitions that is the primary use cases.. useful but doesn't address the thing people want fromt this feature... complete api needs to be there that does this.  Don't think it's the time to discuss the implementation details without knowing what the API looks like. How do authors specify this transitions? this feels to me to be in brainstorming stage.

Dan: that kind of matches my estimation of this -- good idea, but both pages need to opt in, then what happens/ Isn't there a privacy issue massively?

Lea: we could figure out privacy issues with an actual API.. I don't think we have something to review. Even if there are no security issues anywhere there is still the problem of how you express these things? How you expose things? How do authors specify things?

Dan: is that surfaced in the discussion?

Lea: there is a lot of drilling down into details but not big picture

Dan: so we should raise the higher level issue?

Lea: I think so but I'd like feedback from others

Sangwhan: the really complicated case is not defined at all?

Lea: they see the problem that needs solving, but we can't review just the problem, we need to review a proposed solution as well

Sangwhan: the bit they gave us looks okay but the bit that was not defined at all is the one we should have to review intensively because it seems hard. But it's not defined at all.

Lea: I don't think it's wise to review the smaller part and leave the other part for future. Thye need to be designed together. The API should work for both cases, not two completely different APIs. Any time the web platform provided canned effects they ended up not being used becuase designers wanted to do their own thing - web platform should define primitives so designers can do what they want.

Dan: what's the current state of this issue? Feedback from tess and sangwhan in july.. responses to lea's comment.. 

Lea: in the actual TAG review the comment is good areas to look at for inspiration.. 

Dan: if we leave a comment to the tune of what you were saying just now could we do that and say come back to us when you've got more to review? Right now we don't feel there's enough of a concrete proposal here? Therefore could we close it? If we keep coming back to it and circulating on this issue but there's nothing further look at maybe we need to ask them to reopen when they have a more concrete proposal

Sangwhan: sure

Lea: makes sense. I can leave a comment.

Dan: let's do that, and close with that if it's okay, with prioviso to ask for it to be reopened when it's ..

Lea: what resolution? 

Dan: too early

Sangwhan:

```
Apologies for the long delay! We discussed this at length during our VF2F, and while we think this would be a great addition to the platform, it's also a scary+open ended feature. The design itself I think makes a lot of sense and we are happy with it, but we'd like to see this being tried out in the wild (say, with some early adopters) and getting their feedback would be useful to know if there are details/features that we potentially missed in the initial design.

Do you think it would make sense to give it a trial run in the wild, and re-open after seeing what kind of feedback comes back? (presumably, also with updates to the design)
```

### Rollups for 5ab 6ab

#### 5a - 

Dan: we talked about CORS ... 

Peter: Yves was commenting... we didn't close it but did get a reply

Dan: media stream capture.. 

Rossen: we spent most time talking about device posture.. lively conversation.. the current proposal started with something pretty specific with a bunch of capabilities describing angles between screens and folds and whatnot. Based on our feedback they scoped it all the way down to essentially just the posture of a device epressed through a media feature and with that simplification/generalisation it basically renders the current feature almost not useful because you need to resort to things like screen spanning queries and environment variables etc. Sangwhan asked a comment and there was immediate feedback, but I'm going to add one more comment.

#### 5b -

Tess: we looked at two design reviews and some other stuff. Trust token APIs and CAPTCHAs are horrible. Trust token is potentially a solution to captchas.. what we found is we're still waiting on some updated docs from the trust token people, but we noticed we had never linked it to the captchas issue, which seemed relevant.. declarative way of linking trust tokens to html forms. Left a comment. But waiting on them for review. As far as captchas are horrible... trust tokens is an attempt to address that.. we didn't know what to do with this issue.. it's not our job to design a solution to the problem.. discussion has gone reasonably well.. ongoing work to potentially address it so our question was should we close the captchas are horrible issue? But Peter filed it so we wanted to bring it to the rollup. In four years if no-one has fixed it yet the TAG should know that. Does it always need to be in our list of open issues?

Dan: could we set an alarm to notify us in four years?

Peter: I'm happy closing it. The intention was to spark the conversation, exactly as we did. Mission accomplished.

Tess: we merged a copule of PRs, one on design principles and one on S&P questionnaire. Spent time on other design review issues. Left feedback on an open PR.

##### 6a - 

Tess: bunch of stuff - secure payment confirmation - with Ian Jacobs. Ian provided with a lot of context and backhground info that helped us understand the big picture. How they ended up with the design they ended up with. I felt pretty comfortable giving the thumbs up at the end. We will do a follow-up next week in breakout a - to possibly close the issue. Really great conversation.

##### 6b - 

Dan: capturing tabs.. left a comment that we might close 625 because the feedback was from the requester that 609 is the long term goal, but that there was this .. but 625 is already shipping in chrome and a lot of people are using it. Asked for a roadmap for when/how it gets deprecated, because the web is littered with proposals that were supposed to be short term things. Pickling for async clipboard, good discussion, tried to focus on pickling because there's also a privacy aspect that is not part of this proposal but gets conflated becuase of additional risks associated with complex formats. Sangwhan left a comment prompting about running a trial to see what comes back. Shared element transitions - Lea drafted a comment.

### Session 7

Present: Peter, Rossen

#### [HTMLScriptElement.supports(type) method](https://github.com/w3ctag/design-reviews/issues/674)

Concerns about the method name being too generic for a limited use, gave feedback about renaming.

[Transitioned the issue to in-progress and left comment](https://github.com/w3ctag/design-reviews/issues/674#issuecomment-919569046)

#### [WritableStream controller's AbortSignal](https://github.com/w3ctag/design-reviews/issues/672)

Rossen: It's unclear what the user benefits or use cases are based on the explainer.

[Left comment and cross posted to their repo](https://github.com/w3ctag/design-reviews/issues/672#issuecomment-919578419)

#### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670)

#### [WebTransport review request](https://github.com/w3ctag/design-reviews/issues/669) 


### Session 9

Present: Lea, Sangwhan

#### [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587)

[we closed it]

Sangwhan: we don't have a resolution for return errors vs throwing.  Right now no concrete guidance on this.  This is related to issue 55 in Design Principles..

#### [Early design review of light-DOM CSS Scope proposal](https://github.com/w3ctag/design-reviews/issues/593)

Sangwhan: we touched on this.  CSS selection shadow dom and light dom... 

Lea: last time we gave feedback we had concerns about this being a way to select elements that is not a selector.  I left a comment asking if there are any updates.. and if working group has explored reusing selection mechanisms... 

#### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) 

Sangwhan: there is pushback - webkit thinks this is problematic.  can be coordinated between 2 origins... mozilla said the same.  We asked the question to the OP on whether they have engaged with other implemenetrs on this. 

### Session 10

Present: Dan, Lea, Sangwhan, Amy

#### [General principles gardening](https://github.com/w3ctag/design-principles)

#### [PRs](https://github.com/w3ctag/design-principles/pulls)

**[low level vs high level](https://github.com/w3ctag/design-principles/pull/291)**

Lea: needs work.. but I don't remember

Dan: at some point what came out was too far towards a repudiation of the extensible web thinking and what came out of our discussion was it should pull back from that.

Lea: lack of consensus about whether we should recommend always going high level first. Some of us felt it lacks the necessary nuance and others felt we should go high level first which is opposite to extensible web.

Dan: I think we had a rough consensus that we can thread the needle - that's the nuance. Sometimes thinking about the high level design doesn't mean you don't also think about the primitives that are required. Thinking about design at high level, whilst also thinking about a layered solution. This is all consistent with the extensible web stuff.

Lea: the proposed changes that weren't' consistent. Rossen wanted to make some changes and the changes to the PR wouldn't be consistent.

Dan: if Rossen wants to make additional changes he can propose another PR?

Sangwhan: +1 unless there's disagreement about this text. Land it and if there are issues send another PR. Leaving PRs unattended is bad

Dan: I think we should land this..

Sangwhan: different interpretation of layered... direction you start is a thing we don't have a strong agreement on.

Dan: [comments & merges]

**[prefer simple solutions](https://github.com/w3ctag/design-principles/pull/306)**

Lea: not ready to merge, feedback to be addressed. I don't think there is nothing to add, but given we merged 291 if 306 is to be landed it probably needs rewording to be integrated into existing text

Sangwhan: agree. Leave a comment and remove agenda+?

Lea: +1

Dan: [does so]

**[crypto principle](https://github.com/w3ctag/design-principles/pull/310)**

Sangwhan: Amy made some changes.. we wrote this in a face to face

Amy: feedback from ryan sleevi - Tess and I looked at this - we wanted to keep the essence of the principle - making sure it's reviewed by experts - we can take the web crypto stuff out... it was in because we wanted a concrete example of an existing API but I think it's okay to take out 

Sangwhan: the web crypto reference was trying to say - api should be algorithm independent. Tricky thing to suggest -  Totally fine with this change....

Amy: [removes webcrypto text]

Dan: [review & merge]

**[devices principle](https://github.com/w3ctag/design-principles/pull/320)**

Dan: [did suggested change]

Sangwhan: [integrates Ken's feedback]

Dan: [review & merge]

#### [Avoid recommending DOMTimeStamp](https://github.com/w3ctag/design-principles/issues/332)

Dan: we create and land a PR? Do we agree with Yoav?

Sangwhan: I do

Lea: no objections

Sangwhan: should check interop of DOMHighResTimestamp.. 

Dan: MDN doesn't know.. that's strange

Sangwhan: caniuse [data](https://caniuse.com/high-resolution-time) shows good interop.

Sangwhan: why are we defining quirks between domtimestamp and domhighrestimestamp here?

Dan: yes, belongs in the spec. Let's simplify here.
https://github.com/w3ctag/design-reviews/issues/674#issuecomment-920144169
Yves: +1

[text wrangling]

Dan: [approve & merge]

#### [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55) 

Lea: ...other people thought it's fine to throw an exception.. some people though rejecting a promise is lighter.. We closed the eyedropper issue in our previous breakout because we forgot about this issue.. Main problem is we don't have consensus.

Sangwhan: this is a one hour discussion...

### Session 11

Present: Rossen, Ken, Dan

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652)

Dan: (summarizes his conversation with Ada)

Ken: the webrtc api - getusermedia - has all the confuiguration stuff that webxr raw camera access is missing.

Rossen: Right, is that a superset of the rawimage?

Dan: they can get access to the raw image but also need to request acess to room geometry and other sensors data. So the bottom line is that this is achievable today without these API and the question is, should we enable these on WebXR and somewhat compromise privacy or not?

[Left comment](https://github.com/w3ctag/design-reviews/issues/652#issuecomment-920101955)

#### [WebXR Depth API](https://github.com/w3ctag/design-reviews/issues/550)

Dan/Rossen: [writes proposed comment](https://github.com/w3ctag/design-reviews/issues/550#issuecomment-920111677)

#### [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/545)

```
Just noting that work is progressing on the [accessibility requirements](https://github.com/immersive-web/webxr/blob/main/accessibility-considerations-explainer.md) which is great to see. On this basis we're happy to close this issue. We look forward to a WebXR future.
```

#### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) 

Dan: Taking at look at the [response to our last comment](https://github.com/w3ctag/design-reviews/issues/662#issuecomment-905904873).  Looks good to me.

Rossen: they are coalescing everything by design in a single packet...  

[Left few comments during breakout 12b](https://github.com/w3ctag/design-reviews/issues/662#issuecomment-920160505)

### Session 12A

Present: Dan, Amy, Yoav Weiss, Yves, Mike Taylor, Peter, Henri Sivonen

#### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) 

Mike: update on what's happened since we last chatted - we have yesterday [published an update](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) on the user agent reduction timeline. Before it was an abstract plan, now there are milestones associated with the changes (Chromium milestones). We still plan to give the ecosystem plenty of time to test. An origin trial starts next week and runs for 6 months. Sites can opt in to our vision and give us feedback and let us know - hey this breaks the web, we're doing it wrong, we'll evauate that feedback. That's the UA reduction bit, I think that's less controversial, I understand mozilla is positive onthat set of changes, but can't speak for them. In terms of user agent client hints, we've ladned a few changes since some of the feedback we recieved. Henri in particular had feedback it would be impossible to represent the real gecko version in addition to if they had to spoof as some other browser. We landed a new hint last week called the [full version list hint](https://wicg.github.io/ua-client-hints/#sec-ch-ua-full-version-list). This is in response to feedback we received from edge team, as chromium embedders that the original design was too tightly bound to Chrome thinking.

Dan: one of the things I'm keen to hear about is the feedback on the use of client hints separate from the feedback on client hints themselves. I'm curious to know what if any is the feedback on this proposal stemming from a general antipathy towards client hints, or is there a middle ground of the use of client hints for some metadata that we could stake out a consensus view on. I may be jumping ahead of the discussion but that's a thought I had. Get under the skin of the feedback and whether or not we can drive some good discussion for consensus.

Mike: Full version list client hint allows a browser to send multiple version, eg. gecko could send a gecko version adn a chromium version if it was compatible with that set of features. Embedder like Edge which operates on different versioning schemes could do so.

Henri: the main issues are is this shuffling stuff around, can we not do the reduction in the old place and then how wasteful is this in terms of adding headers even though header comprehension exists.. added stuff to everything.. what if this catches on just enough that some sites use it but most don't, okay it didn't work out but some sites got stuck with it. How difficult is it to take a step back? One of the concerns that we had that seems now resolved that makes the objection less strong than it was is the thought that this would expose stuff that wasn't currently exposed or was otherwise going away. So that if actually it is so that this doesn't expose things that weren't previously like the specific patch level of the engine or the OS or the model of the mobile device, if that's the case, then obviously that objection isn't strong and is a misunderstanding.

Mike: Martin Thomson [filed a really nice issue on github](https://github.com/WICG/ua-client-hints/issues/255) - I'll try to address that in the next week or two - to clarify we do not intend user agent client hints to be a honeypot for additional entropy or information that's not currently available. Privacy is the primary goal here. For user agents that do not currently expose some information, firefox historically has not epoxed device model, the spec will not require that they start doing that. I'll go in and try to make that extra clear. I'm happy to hear that we're aligned on that.

Henri: the issue of to what extent less structure is a bug. Clearly it is a bug in the sense that there is a long history of user agent detection going wrong because of the non structured ness of this data. But then to what extent it's a feature, all the browsers that have claimed that put the name of the previous market leader at the time of their launch in their UA string, IE did this, safari did this, chrome did this.. so clearly there is this use case of making things sniff both ways at the same time, so IE sniffs as mozilla, webkit sniffs as gecko, chrome sniffs as safari, especially the ua full version didn't have this kind of having it both ways and opened the question of if the ua full version is going to happen does it mean that it's just a complicated calendar that's based on chrome's release cycle, instead of saying a year and a month you map it to chrome's release calendar and go from there?

Mike: yeah we built a really complicated calendar, unintentially. We took that feedback about UA full version and recognised that this is not great. We updated the spec with the idea of a version list. We could represent your full version which should be different from chrome's but you could also send a chrome version for a certain site that was doing bad things the idea that you mentioned about the lack of structure being a feature not a bug we've tried to design with that princople in mind. We have this notino of a brands list, you don' thave to say hey I'm chrome. Currently al ot of browsers have user agent spoofing mechanisms, for certain sites they'll say I'm the more tested browser so the idea of this brands list and the version list is you can say I'm chrome and also firefox .. I support the same things that this other mor ewell tested browser supports so you shouldn't block me from your website. 

Dan: from a perspective of the Samsung minority browser, we run into the issue of where ua sniffing locks us out because somebody goes to a website using samsung internet, it works completely fine, but they see samsung and they say you must use chrome. How does this proposal address that case?

Mike: this concept of a brands list, where you have a brand which is defined as your marketing version name - samsung, chrome. You also have these equivalency classes. You can stick as much or as little in yoru blrands list as youw ant. You might want to say I'm samsung and I'm chromium. that's true. We want to encourage sites to feature detect and care about capabilities and not strings, but in the case where they make some misguided decision where they say we require these apis that are only spuported in chromium, if samsung is presentin gits brands list as samsung and chromium and the site is looking for chromium that sholud be a better outcome. Developers are clever so they may do different weird things. But that's the intent. There's this notion of ?? in the brands list, sticking this nonsense string in there to prevent sites from hardcoding a serialised list. If you do that yo'ull fail, it changes from version to version. TO encourage people to make smart choices and not do the old style exact match ua sniffing.

Peter: from the positon of why do people sniff ua strings and one of the more common use cases is detecting what level of js so we know what version of compiled script files to send. Struck me as odd that wasn't called out in the client hints. If we're reducing ua strings the fact you can no longer get that behaviour, seems like a common use case we want to support

Yoav: I think people will still be able.. because th elevel of js support is something tha tis dependant in the broader brand and singficant version that is somethig npeople will be able to do. Ideally we would provide an alternative mechanism for them to do that. There has been a long discussion on the html issue regarding what such a mechanism may look like. there is not a lot of consensus around what we can expose and how we can claim that js support. Theoretically we could say ES18 is suported and that means something. But it's hard to get everyone to agreeon what that something would be. So i'm hopeful we'll be able to do that but this is not part of user agent client hints right now. Or in general we also talked about declarative mechanisms to do teh same thing as an attribute on script tag which would have been useful but thep roblem is defining what the thing is rather than the deliver mechanism. Once we have defined a way to do that negotiation it can be either on the client side or on the server side using client hints

Peter: wanted to make sure it's part of the pipeline. Detecting brand or engine is fragile. What happens with a new brand comes out?

Yoav: agree

Henri: one point: the documents didn't motivate - multiple headers on http caching... some edge caching concerns... to what extent is it considered - instead of browsers adding new headers - add response headers - caches adding new features to be able to vary on contents of ua string ... mobile header is a boolean - looking for mobi substring - browsers wouldn't have to send that on every request if there was a cache feature - this cache entry is for ui hearder that doesn't contain mobi, this one is...

Yoav: multiple proposals in http working group for creating a better vary - key header was a proposal and died. Now variations proposal. Generally modify how caches work is hard - and caches don't update as often. I understand it - there could be potential for better variance mechanisms - but likelylook for deployment is not high...

Henri: "lets add this stuff ot every request in browsers because this other software over here won't update" isn't that great

Yoav: not the only motivation, but.. I think we can talk about the actual cost. It's a non zero cost is true even with h2 and h3 header compression but becuase they are static request headers the cost for the first request is the full length of the header but for follow up requests, long lived collections, the cost per request is in theorder of a few bytes. Would you agree?

Henri: I havent measured it. That seems plausible in the presnce of cross request header compression.

Yoav: from that angle the extra cost doesnt' really .. assuming the headers are used the extra cost is not high. Even when they are not used they are not likely to be the extra bytes that throw the request above the threshold of an mtu and move it to the next ?? beyond the current conditon window. I suspect that event hough you're right an dthe cost is nonzero it is very close to zero in real life at least for h2 compression scenarious

Henri: since there is now a proposal for requesting these opting in on the tls layer what are the implications ... that on its own feels very complicated, should we back down if it gets this complicated? but if that complication is going to be there do these headers still need to be sent by default as opposed to the default set being empty and having to opt into each and everyone on on the tls layer

Mike: the complication is real. There's two modes to do this, we call this client hints reliability. oneis not complicated, there's a http header call critical ch - pass client hints tokens as you would accept-ch. Doesn't require any special backend knowledge, just http. If you can use client hints you can use critical-ch today. The accept_ch tls frame bits is more complex but it's no more complex than deploying h2 if you're already sending ?? strings we're effectively doing the ame thing there. Kind of a choose your own adventure - opt into a as much complexity as you need depending on your use case. Not a requried path for average web developer or ecommerce site or whatheveyou. Second part about the headers default headers?

Henri: shold the default set be empty so anyone who wants to have them in the as soon as they appear in the current default scenario that anyoen who needs them on the first request would negotiate them on the tls handshake?

Yoav: the decision from my perspective to make those headers on my default rather than off by default like all the other client hints was that they covered a good chunk of todya's use cases and therefor it seemed reasonable to continue to expose them byd efautl without requiring folks to go to the length of making sure they're tls stack supports the accept_ch frame. Also in terms of order accept_ch was added later. It's still not necessarily as easy to deploy as we would like. It's a new feature taht requires support from the tls stack. It's a new frame for h2 and h3 but it requires some tls support for th eunderlying mechanism to deliver those frames. At least for the basic case of people using passive entropy that we send by efault ain the ua string it seemed reasonable to cover most of those cases mainly bug workarounds that are based on browser version, mobile adaptation based on the mobileness bit or mobi string so people can serve a desktop site and a mobile site even though that's also not a practice i'm a fan of but this is how the web works today. The recent addition for platform which mike can speak more on the motiation behind that, but the justification for why it's okay to expose it is it's already sniffable. The entropy is already exposed through the tcp stack in many cases. there were use cases for that as well.

Henri: the reason for not to do that was considering entropy rather than considering do we want to send these bytes along

Mike: it's a privacy plus compatibility motivation. We're ranking those ahead of network cost. not saying one is not important but that's the primary thinking. 

Dan: something yoav said about the mobi-ness bit - if responsive design is something we want to push people towards becuase its more inclusive and can make a better web for everybody should we b adding features to the platform that help people reinforce this bad practice of having a mobile site insteda of using the tools of responsive design? Trying to think, there are a lot of other reviews we've done of new tech wehre the somebody says we're just trying to replicate something that's happening on native and that feels almost similar. Wait a second, we're supposed to be having a higher quality bar for new things coming onto the web. i take your point about not breaking things that are working a certain way but is there a way to design this feature that could encourage, to make it more dificult.. wouldn't it be better ot add an extra step forr people who want to kno wwhether it's mobile or not vs just using the tools of responsive design to begin with?

Mike: good question. My natural thinking here is.. I don't have a great answer. One of the arguements we're making with this api is an improvement over ua parsing which is fragile. if we apply structure to whatever signal the ua string is providng that feels like an ergonmics win for developers. But I hear you is that a carrot we should be providing? If it didn't exist would people stick to the old methods that are hostile to new mobile browsers, etc? Even though in a perfect world we all just do responsive design

Henri: this goes to the core of client hints in general. If we consider a client hint for the viewport width vs media queries. In netscape 4, maybe earlier, pre gecko, there was a time when if you resized the window in netscape under certain conditions would cause a reload. With media queries all th einformation is on the clientside so if you hav ea mobile device and you rotate it the width media query matches and after you rotate it it adapts on th device instead of reloading. If you hav eaclient hint on the http layer that declares viewport width is this, then you rotate the device, do you go back to the pre gecko days of that causing a reload? or you have the request what they were before you rotated it and now you do whatever the css says within the constraints of what the requests were. If you want th efull adaptation you need to reload. The act of resizing or rotating a mobile device causing a reload is very clearly a step back. That's my general concern with client hints the original set and I think this quesiton that Dan asked is pretty much on the same theme in terms of okay there are people who ant to do this adaptation on the server but we have this stuf fin css and so forth that does it on th eclien tand it's better. But they still want to do this other thing, so do we do more specific and granualr tools to do the sort of thing, or do we tell them no you're doing it wrong and use this thing that's conceptually on the other side

Dan: my initial uesion was not about shoul dthe information be available at all, but rather should it be available by default? by making there be an extra step in order to understand that bit of information might that nudge more content to be built along responsive design means?

Yoav: Changing the way that the web is built today is not trivial. Client hints gives us a way to do that in steps in a way. Yes we can expose the mobile bit today but a few years down the road make it an opt in rather than being exposed by default, or add some cost to it. I don't know. at the same time there are also.. initially we weren't planning on exposing it by default and there were a lot of use cases and people crying otu saying that this is how they serve their site and otherwise they will just have serve bloated sites to people in developing countries and that would result in an adverse effect. there's a complex tradeoff here

Dan: there's reality vs theoretical purity..

Dan: it was good to hear Henri some of the objections seem to have been addressed or .. I'm tryign to think about this from the perspective of our review. One thing we try to focus on that we have a strong TAGvalue statement about multiple implementations. When we're reviewing something and we all are nodding our heads there oculd be a group think going on and if we then see a negative review coming from an implementer or we see signals that one implementer is interested but others aren't interested or actively think it's harmful then that's a signal that plays into our review. It's important that we're not fragmenting the web by making more code paths necessary becuase certan thing work with certain browsers, there's already too much of that. I'm interested to know is there a core of this proposal that mozilla would consider implementing?

Henri: I can't make a statement of that kind

Mike: go back and chat with your standards leaders. Marcos had a suggestion in the thread - based on the current reading it's confusing that it's harmful... path forward.. acrobatics.. an http ua ch and a js ua ch... mozilla has interestin the js side of things

Henri: considering that the navigator objects fields are already more structured than the ua string itself what do you see as the main benefit of a new js api compared to the current level of structuredness of navigator.oscpu or navigator. anything else?

Mike: really not that much structure.. user agent echoing http.. oscup which is gecko only.. navigator platform.. some notion of architecture.. appinfo.. you have if you squint structure. You still have to parse these strings and subset them and try to do clever things due to that. So structure is one of the most important arguments there. Right now the firefox people are doing experiments what happens when we hit version 100. We're starting to think about this as well. one of the bugs filed was osmeone was doing an index of and math to know which version and which codepath to take. that stuff goes away if you have clean interfaces to get at platform os etc. The other argument which i know mozilla was in favour of.. martin talked about, the standards position talked about, when you've go tthese active interfaces on the clientside the os can audit them. You can see the callers knwo the origins, something could hook nicely into enhanced trakcing protection. Strict mode doesn't get any ofthis stuff, standard mode gets low entryopy stuff. hard to do when navigator.useragent has a big old string.. you odn't know what folks are asking for and what they're trying to do. in terms of user control you can do interesting product things through this type of api

Henri: navigator.stuff is not strucutred in the right way?

Mike: you could say that.. it's a "hot mess" is how you'd say that in Texas. One of the nice things about the api that sits on top of navigator, you have this get high entroy pmethod.. we split up between low entropy and high entropy, we claim mobileness platform signficant version is low entropy, other stuff like cpu or device model .. if you're trying to provide an optimised download experience or work around a bug, you need to request that, it's an async interface, th eua can make different decisions, browsers can have differne tpolicies, you can reject it based on user choice or ua policy

Henri: is it web compatible every to reject tha tpromise as opposed to always accept it and make the apis return lies?

Mike: I'm bad at predicting the future. i would hope it's web compatible. Ithink if you have the most tested browser ships one behaviour and its the only browser that ships it for 10 years it's sailed.. if we have multiple implementations with differnet opinions developers need to make better choices. If a browser like safari has something like itp has something liek a browse rlike firefox which has something like etp or chrome which has privacy budget.. there is a possible future where developers ar etrained to get this right. Realistically though like you're saying history has not always been kind ot us and browsers have to lie. 

Dan: what do we expect very privacy focussed browsers to do with this technology? is the expectation that they would 'lie'? If you're Tor you want to advertise that everybody using yoru browser is using window,s firefox, that they have this completely generic advertisement of what they are so it makes it more difficult ofr peopel tp rofile and fingerprint the users. Is that something that's allowed for?

Mike: yeah. It's allowed, you should be able to do that. the Spec explicitly carves out.. I'l try to make this more clear, but today it talks about the empty string is always a valid answer and you're allowed to return other values. Some browsers would want to lie, hide in the crowd, give as little entropy as you can. Firefox has a resist fingerprinting mode that does somethign similar. there's nothing in the spec that requires you if you wanted to pass all the tests to give away something you don't believe should be given away.

Dan: this has been a good discussion, teased out helpful stuff.. I'd love to hear more about if and how anything today changes the official mozilla standards position on this? that would deifnitely be useful to know for the purposes of resolving our review. What would you like to see TAG do next? Our default would be to continue to monitor this issue and see if consensus starts to emerge we can say it looks like things are moving and close it.. but if there continue to be major disagreements there's a role for TAG to play in trying to mediate that discussion.

Mike: sounds good. We have some feedback from mozilla that I need to address in the spec, especially around privacy and entropy. Once I do that maybe I might open a new standards position issue and say we think this should be considered?

Henri: probably better to open a new one and refer to the old one, so that whenever there's a change there is an issue for that, but point people subscribed to the old one to the new one. 

Mike: I'll ask mozilla.. and we'll take it from there. I'd love to know Apple's opinions. (And then I'll ping the TAG thread with the new issue, so everyone can be aware.)

Dan: we won't take any action at this point but it's clearer where we're at.

### Session 12B

Present: Rossen, Ken

#### [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648)

Rossen: feedback addressed, closed

#### [PWAs as URL Handlers](https://github.com/w3ctag/design-reviews/issues/552)

Rossen: going to be closed as no change because the proposal is outdated and overtaken by another spec with scopes, that's already acknowledged in a new explainer. How to close? Overtaken.

[Closed with comments](https://github.com/w3ctag/design-reviews/issues/552#issuecomment-920213019)

#### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650)

#### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) 

Rossen: [wrote closing comment](https://github.com/w3ctag/design-reviews/issues/602#issuecomment-920210615)

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509)

### Session 13

Present: Peter, Rossen, Sangwhan

#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)

#### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655)

#### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) 
```
@plinss, @cynthia and myself did another review of this during our Gethen vf2f. First of all, thank you for following up on with your security team and getting an LGTM from them. I personally won't push on this further given it's already captured.

Another issue with this proposal is the affect it has to existing styling patterns. All conditional styling today takes place on the client as a result of style recalc in combination of various environment changes - color scheme, reduced motion, transparency etc. Exposing this through client hints will promote such conditional handling on the server side which will arguably negate some of the perf wins described and also require that state is kept on the server side. Ex. UA navigates to a.com in light mode exposed in the client hints. The server provides a light version of style.css and appropriate other content. The mode changes to dark in the same session - the server needs to recognize the change and this implies the client needs to reload possobly all the resources.

Finally, I don't believe CSSWG is the approriate venue for this work. It is the right place to define media capabilities, not client hints.
```

### Session 15 

Present: Dan, Lea, Ken, Sangwhan

#### [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) 

Ken: sounds like this has support from Google and Microsoft... 

Dan: [last comment from anssi](https://github.com/w3ctag/design-reviews/issues/570#issuecomment-911858866) sums it up well. They have made a numnber of changes based on our feedback. It's all tracked in their repo. They have transitioned from CG to WG in the mean time. 

Ken: [leaves comment on readability of code examples](https://github.com/w3ctag/design-reviews/issues/570#issuecomment-920621844)

Dan: [leaves comment asking about multistakeholder support](https://github.com/w3ctag/design-reviews/issues/570#issuecomment-920624634)

Sangwhan: I [still] have some concerns regarding the design of that API (in particular, the low level nature of it) [but] feel free to close 


#### [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55) 

Lea: this recently came up again because of the [eyedropper API](https://github.com/w3ctag/design-reviews/issues/587)... 

Ken: it all depends - is it an expected error or an unexpected error?  

Lea: is it on the expected path of user interaction?  

Ken: an out of memory error would not be a return value.

Lea: not selecting color is part of user interaction - so not an error. So the existing way the file picker API works is wrong.  In eyedropper they were trying to be consistent with filepicker API.

Ken: it's not an **exception**al situation.

Lea: [Domenic's comment](https://github.com/w3ctag/design-reviews/issues/587#issuecomment-911939070)..  looks like abort error might be a special case...  So in that case EyeDropper is not wrong because it's using AbortError.

Dan: And `AbortError` is specifically intended for a user action to abort?

Lea: not necesarilly...

Lea: another big debate about using exceptions for flow control - and this colors this discussion.

Lea: a number of things throw `abortError` ...

Sangwhan: Should we try to write something?

Lea: we should make special mention of `AbortError` - i have reservations about it being an exception but that ship has sailed.

Lea: looks like `abortError` is an established pattern so consistency is more important that theoretical purity.

Sangwhan: what's a good example of an error value.

Ken: -1?

Lea: yeah -1 or ... it sounds like an error object but that's not ...

Sangwhan: from a reader's perspective error value sounds like a specific error class - that's not nice.

Dan: should it be in a primitive type?

Sangwhan: you want to be able to check it with a diff - you want to be able to check for "not return value" - for performance.

Lea: are all the examples about error values... all about the absence of a value?

Ken: a string comparison function...

Lea: What if we use "absence of a result"? Even in the case of string comparison, -1 is the absnce os a result (we have no index)

[we collaborate on some text]

```
## Use of Exceptions vs Returning Error Values

Generally do not use exceptions unless there is an exceptional circumstance. Do not use exceptions for control flow. If something is on the expected path of user interaction then it should not be an exception.  For these cases, return an error value or null.

Examples of error values: String `indexOf` returns -1; Element `id` returns null; [need more examples here]

For cases where an interaction cancels an operation, preventing the algorithm from returning a meaningful value, use AbortError. For example, when a user dismisses a payment request, an AbortError is thrown.

[More examples of things that use AbortError?]

```

Sangwhan: let's get a PR out of this and then iterate.

### Session 16

Present: Dan, Sangwhan, Amy, Yves

#### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591)

Sangwhan: this was proposed closed a while ago  and then Richard came in and wrote some stuff

Dan: it keeps getting updated which is good

Sangwhan: they can discuss with Richard on the issue but from our end it's okay.. problem is rtl and ltr switching.. eg. writing arabic and then numbers and back to arabic.. becomes icky with handwriting recognition. I don'tk now of an engine that does this well. The API and design doesn't factor this is in is based on the current state of affairs

Dan: I don't think we need to weigh in on that, one of the things that Rossen said in may was it's not clear about fingerprinting.. I would note that there's a very comprehensive [privacy considerations section](https://github.com/WICG/handwriting-recognition/blob/main/explainer.md#privacy-considerations) in the explainer which talks about the different fingerprinting risks associated with different types of recognisers which looks like they've spent some time thinking about this which is good to see. From that perspective they've taken some feedback from TAG into account.

Yves: the rtl ltr discussion started during review but it's still continuing, I don't think we should close we should wait for completion of the discussion on that aspect. And it's good that richard came up with very specific examples.

Amy: shouldn't that conversation be in i18n horizontal review ticket?

Sangwhan: that's [issue 4](https://github.com/WICG/handwriting-recognition/issues/4) on their end with details and they're discussing there so that's fine. Can continue over there. From a design perspective I think we're okay.

Yves: as long as it's tracked somewhere

Sangwhan: it is tracked and linked to our issue

Dan: I think we should close it. [writes comment]. Multistakeholder?

Sangwhan: apple might implement it..

Dan: no signal no signal.. web developers like it

Sangwhan: a challenge - to be able to ship such a feature you need a handwriting recognition engine and not many companies have that. Mozilla doesn't have one. They'd have to duck tape some open source thing into the browser ot implement this. There is a bit of a only rich companies can implement this problem and I'm not sure if that should be factored in to a design review.

```
Thanks for the very comprehensive privacy & security section in the explainer. We're basically fine with the design. Since this relies on the presence of a handwriting recognizer software component that raises some concerns about implementability - especially across lower spec devices and in open source efforts.  There seems to be an issue regarding multi-stakeholder support as there's no documented support from other browser engines on Chrome Status - can you provide any feedback there?  What is the trajectory for this spec after **incubation** in WICG?  Where do you see this going?
```

Dan: [comment left](https://github.com/w3ctag/design-reviews/issues/591#issuecomment-920713338)

#### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523)

Sangwhan: my question is .. we don't have a lifecycle document for pwas and we don't have a good document for pages, but now we have one for osmething that is very specific and do we want that?

Dan: maybe we should have a lifecycle document for web applications that includes things like .. I don't think we should have it for pwas, not a concept we should canonicalize, but we should have a lifecycle document for web applications that includes the mechanisms used by pwas such as installation via a manifest and we could use this document as a template.

Sangwhan: I'm looking at their explainer.. i'm not so sure if i agree with their service worker to application launch mapping.. those are largely different concepts. Why they need a new spec?

Dan: you mean in the comparison with related work in w3c? Page lifecycle is something in WICG

Sangwhan: page lifecycle hasn't been updated for a while. They said it doesn't do what they need to do and i agree because it's not maintained. Last update Sept 2019. 

Dan: I don't think service worker install is the same as application launch. and service worker activate doesn't have anything to do with application shown

Sangwhan: service worker is not an application, it's a data source

Dan: we could leave that feedback

Sangwhan: you don't think pwa lifecycle should be defined?

Dan: I think web application lifecycle should be defined. Part of web application is the optional installation. Part of the install is service worker activation etc.

Sangwhan: that's part of the page lifecycle draft

Dan: the whole thing with a 'pwa' is that it's optional if the user decides to install it or use it within the browser context. Gives the person the choice of if you think this is useful then you can choose to install it on your device and activate it and it takes advantage of the things in the manifest file, but youc an also continue to use it within the browser and either way it might be using a service worker. It doesn't make sense ot have a separate lifecycle document that only covers when you choose ot install something on your device because that's only one user flow

Sangwhan: right

Dan: so maybe we should be updating this page lifecycle document.

Sangwhan: they also want to define their own set of api events. I think miniapp doesn't actually have installs.. it says "miniapp is install-free"

Dan: ...download miniapp resource... hosted native app... you could say the same thing about pwas. The installation of pwa is simply you coudl have it installed but the browser has chosen to de-register the service worker and cleared the cache but all of that stuff can be reestablished from the server when needed. It's the same lifecycle. You could say pwas are install-free as well, the only sense in which they're installed is that there's an icon on your screen

Sangwhan: I'm pretty sure they had installation through non-web delivery mechanisms in one of their documents but I can't find it

Dan: this document should be webapp lifecycle and should include things like service worker registration, manifest file. Tis document doesn't have anything about manifest file

Sangwhan: they have a separate manifest spec... that's a good point. I don't know the installation process for this thing

Dan: separately we could be prompting and say someone shoudl be taking this lifecycle work on.. but we've got to focus on giving feedback to miniapps. The comparison or mapping of different things to service worker and other types of .. what's this page visibility level thing?

Sangwhan: for when you have multiple tabs and one thing is in focus and others aren't in focus

Dan: in the miniapp lifecycle they're not referencing service workers at all

Yves: they don't rely on service workers

Dan: neither manifests. Part of our feedbackto them has been make use of manifest

Yves: they are working on manifest file

Dan: why isn't that called out in the lifecycle?

Sangwhan: good question. Can ask.

Dan: they are not using service worker?

Sangwhan: no. I think you can but it's not a mandate

Dan: why not?

Yves: probably dn't need to cache things that are already in your.. from external interactions for example

Sangwhan: I don't think miniapps were designed with offline in mind

Dan: [writes comment]

```
Hi @xfq  – We're just reviewing in the TAG virtual f2f today. A few things we noted:

1. The mapping of Miniapp states to other w3c specs may be innacurate - in particular the mapping to service worker states.

2. The lifecycle document doesn't reference Manifest at all. It was our understanding that Miniapps would use the manifest file with the Miniapp extensions and that doesn't seem to be referenced in the document.

3. It doesn't look like you're referencing ServiceWorker either - is there a Miniapp state which makes use of ServiceWorker?

4. When a Miniapp is launched what origin can it be said to have, with regard to the web's security model? That would seem to be important from a lifecycle point of view.

We also note that the Page Lifecycle document that you point to as comparison is out of date and itself needs to be updated (in particular to reflect installation via Manifest, which is missing). 

We think it's worth considering whether these lifecycle efforts (MiniApps, web pages, PWA) could be consolidated or brought together in some way.
```

Sangwhan: I'm not sure why they want this extra event system for this. Seems like they're modelling around the android apis, but I don't know. 

Dan: I'm not sure I agree its worth consolidating all of the lifecycel efforts into a single spec. Worth considering if they could be brought together, but I don't envision that there could be a document that pwa people are referencing and updating that also has all of this optional stuff that only relates o miniapps.

Sangwhan: okay

#### [EME MediaKeySessionClosedReason](https://github.com/w3ctag/design-reviews/issues/671) 

Sangwhan: it's a very small thing. On mediakeysession which is an object inside eme there is an attribute called 'closed' and this adds a reason to why it was closed

Dan: what's the user need? In service of need? Is this shown to the user?

Sangwhan: usually to do error handling for the application to reinitialise the eme stack. You would have a couple of errors.. it's an enum, internalerror, closedbyapplication, etc, comes back from the content decryption module. Also resourceevicted. The content decryption module dpeends on hardware for example and ran out of memory and had to release the resources or stuff like that. This would be information usable in terms of the video streaming application knowing what to do next if the decryption failed or if it's closed. This doesn't add more damage.

Dan: I've marked it as small delta.. 

Sangwhan: there's a tricky bit.. I think EME doesn't have a working group?

Dan: Media Working Group

Yves: yes

Sangwhan: I'm okay with this. Can write a closing comment. I'm not sure if this is an actual attack... the state change can leak information across origins. But there's a bunch of other stuff that could trigger this so I'm not sure if it's a big issue.

Dan: One of the things we kept talkinga bout intially with the EME review was that it can leak information to you because the content decryption module is a black box it can have access to information like your location and that can..

Sangwhan: it is not supposed to but yes

Dan: that lead to the whole discussion about wanting some kind of statement a waiver about security and privacy experts auditing how these systems work and that should be considered an exception, they should not be prosecuted under the digital millenium copyright act, and there ended up not being that [covenant](https://www.w3.org/blog/TAG/2015/11/16/strong-web-platform-statement/), it wasn't part of EME even though TAG recommended that it should, is there something similar to that where this nformation could reveal something about the user across origin, or is thsi purely mechanics? 

Dan: Also worth noting our [feedback from 2017](https://github.com/w3c/encrypted-media/issues/389) on this issue.

Sangwhan: imagine the gamepad API.. some implementations broadcast the input to all tabs because it's an event. In this event you could listen to gamepad input and match up a user by listening to the gamepad events, if a user presses right multiple origins will get that. This is the same kind of mechanism that will happen. Multiple things are using the EME stack and the CDN goes bonkers and everything shuts down for the same reason it could identify the user, I'm not sure if that's a realistic or useful attack surface.

Dan: maybe ask that?

Sangwhan: I don't think it's preventable. It's in 2.1 in S&P - information will be exposed indirectly to some websites. [reads] I don't think it's a huge issue to be honest.

```
(Setting aside all debate about whether or not EME should exist in the first place, since the cat is out of the box. For that bit, please refer to our [feedback from 2017](https://github.com/w3c/encrypted-media/issues/389).)

Given that this is a small incremental change to an existing spec that improves developer ergonomics, we are happy to see this move forward. Thanks for bringing this to our attention.

Noticed that the EME spec doesn't have a S&P section - think it would be worth adding something there (not just for this feature, but for EME as a whole) if possible.
```

### Session 17A

Present: Dan, Amy, Peter

#### [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240) 

Peter: has anything happened?

Dan: comments recently.. 

Peter: ... MDNS is part of it - but the other half is SRV records - DNS records - there adre a number of federation protocols - e.g. matrix - you do a SRV lookup on xyz.com and find out there is a matrix server here... because that doesn't work on the web everyone has to use a well known URI.  We don't want to give broad access to DNS to a web client - but limited access to e.g. SRV lookups would be useful.

Dan: when I type in w3.org there's already a record which points my browser to the appropriate ip address to make the http request.. why do we need something .. a second level of indirection where we?

PeteR: that's an A record.. for matrix, I run a matrix server, but my matrix id is peter:linss.com .. how do you find my matrix server? the standard way to do that is look up the service record

Dan: but that's a record for a specific entity

Peter: it's a record for the service

Dan: you at that service.. you described a string that is you at that service

Peter: the record name is _matrix._tcp ... it's a pattern for service records. Anybody gives you an address that ends inlinss.com it looks that service record

Dan: why is that useful for the web?

PeteR: it's about you typing in my matrix id..

Amy: something about acitivitypub

Dan: I'm talking about how people use the web in the browser

Peter: if you want to build a web client you need to be able to do this level of discovery. If i want to put something on your calendar you need to be able to type my email address into your calendar

Amy: in the social web we use relations - you have the profile URL - your name at your domain.. you look that up and get a link relation in the header or the HTML - 

Peter: you have to build a http level protocol so the clients can use this.  Matrix did the same - but it's a pain to put a well known URL in linss.com... same person might not own the matrix server...

Amy: that's why we didn't use well known urls in Social Web WG ...

Peter: single scoped DNS lookup...  Don't want to add general DNS capabilities to the browser.  Doesn't change how I would pull up a web site.   If I type w3.org it could require a SRV look up but i don't propose that. it's for service - e.g. a calendar.  

Dan: right now if I want to subscribe to a calendar I need a full URL. It might simplify thigns like subscribing to a calendar, which in some cases is not using a traditional web browser but some other client. In some cases you can take a calendar url and subscribe from a calendar app or inside a web app. Either way you've got a full url. 

Peter: I can give you a url to my calendar.. you should be able to type in my email address and a web client should be able to figure that out by doing service discovery, because my servers do advertise the correct dns and txt records to do that lookup. A native calendar app can do that, a web calendar app cannot

Dan: in the world where people who create calendars and advertise those calendar urls, where they're all calendar.google.com how does that help me?

Peter: it deson't help to have your calendar on google.com....

Dan: I know that. But if I change my calendar from one cloud service to another, it's still hosted by somebody but it's at my torgo.com address..

Peter: you update the service record at torgo.com and I can go find your calendar server, whichever one it is

Dan: how does it help people who use highly used services on the web right now? vs people who want to tinker around with their own xmpp servers

Peter: it gives you a level of indirection so I don't have to advertise the fact I'm using googles calendar, just the fact that I have a calendar. And that gives me freedom to move my calendar around without breaking all the links. I'm asking for two method calls on the browser, one to do an mdns query looking for a local service and one to do a service record lookup. We don't have to call it that, but I sholud be able to pass in a domain and the name of a service and under the hood it does a srv lookup and a txt record lookup and it gives me the url, port, domain. That's all this is about. Clients can't do that now cos they can't do dns lookups.

Dan: is there a browser that is close to being able to do this? what does firefox do?

Peter: nobody I know of has anything like this. If you know of a DOH server you can implement this clientside. You can do any dns query over http but that's it's own nightmare.

**Reviewing the Chromium proposal on this https://developer.chrome.com/docs/extensions/reference/mdns/ which is marked as deprecated**

Peter: doesn't do SRV records...  

Dan: i wonder if it was deprecated because of security concerns

Peter: this is entirely about local discovery

Dan: we talked about local network accses but even thatn eeds to be a picker UI so you're not allowing random web apps to scan your local network. I don't think there's a similar issue with what you're taling about. Just giving the client ability to do dns queries

Peter: public information..

Peter: sangwhan and I discussed just writing a polyfill and seeing if anybody cares at wicg

Dan: I wonder if Andrew Beck would be interested in helping with that, coming at things from the cdn perspective. Keep it open as a placeholder for that activity?

Peter: sort of. I don't think it's the TAG's job to design and build this feature. But something I could do on my own because I care.. as far as the TAG's role, we've identified a hole in the platform. I thin it's our job to do that and call it out and try to get somebody in w3c to work on it.

Dan: one mechanism could be a finding... or a blog post. More public than an issue register

Peter: maybe a blogpost. Also w3c strategy funnel..

Dan: **action** is on Peter to write a blog post

Peter: k

### Session 17B

Present: Lea, Rossen

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416)

Rossen: Still no progress from filers. [Left comment](https://github.com/w3ctag/design-reviews/issues/416#issuecomment-920963453)

#### [CanvasRenderingContext2D API Improvements](https://github.com/w3ctag/design-reviews/issues/627)

[Closed with comment](https://github.com/w3ctag/design-reviews/issues/627#issuecomment-920982811)

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) 

Lea: [Left comment](https://github.com/w3ctag/design-reviews/issues/521#issuecomment-921027219)

### Session 18A

Present: Dan, Amy, Rossen, Lea

#### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624)

Dan: not much since may...

Rossen: we have a css wg resolution a couple of days after the last comment which constrains ... to auto matches only... by virtue of doing that we are scoping its effect quite a bit. So that part is fine. That was one of the points raised initially by ..? Some of it started from Lea's feedback. We have a good resolution on that issue. 

Dan: can we close? if they've taken on board our feedback in their design. Do we have further objections? Can we live with it? And/or is there additional work going on in css so it doesn't need to be on TAG's docket?

Rossen: Definitely work going on. in terms of capability.. 

Dan: there's no privacy and security section. They say there's no need.. have we addressed that previously?

Rossen: I don't think so

Dan: is there some kind of privacy aspect?

Rossen: i don't see how

Lea: they've reduced the cases that violate CSS reactivity but it's still violating it part of the time.. philosophical purity is at the bottom of our priorties so if authors really want this and it's really needed then I guess it shold be fine. I don't like it but.. whatever.

Rossen: essentially this is a broader effort to reduce the overall resource loading during initial loads, there was an umbrella feature called ... where you don't have the content as part of the layout and rendering, but if you search for something with ctrl+f you actually will force the content to get populated and you will get from a user pov what you would have had anyway, however ..

Dan: if something only partially loads, like article text?

Rossen: right, you have loaded your content but you're not necessarily building the rendering part for it, you've parsed it and have the content and you can search it, might do initial layout for it, this is where thesee things are coming into play, the sizes for things, arranged that way, scrollbar has the size it would if laid out normally, but it's not rendered. Now when you go to search and for example scroll into view now the implementation needs to catch up and make sure what's in front of hte user is not a bunch of blanks. This is this whole feature. It had some weird name. This is part of it where the intrinsic size is for an image which is not rasterized and decoded yet, so you don't know what the intrinsic size of the image is

Dan: all aimed at faster page load?

Rossen: yes. And improve other thigs like battery life, memory footprint, cpu etc. Benefits for sure. But these are UA performance optimizations targeted features

Dan: lea what's your objection?

Lea: same objection that we have discussed in the past and gave as feedback - that css has always been this nice reactive language hin which things apply and stop applying without side effects. No ordered steps, current state is always a function of what is currently applying. Value in that simplicity. Last remembered state introduced here breaks this fundamental assumption. First css feature to break this, introducing side effects that persist after certain state has stopped applying introduces state that is not inspectable and has no obvious cause. But it's a philosophical objection.

Dan: I see.

Lea: breaks one of the assumptions of CSS. It is about authors - this is an assumption authors could make, whereas now thye have to take side effects into account. I don't want to stop a feature that is going to help authors

Rossen: users more than authors. From a tooling pov the simplicity that you were referring to also is a huge help to tooling. WYSIWYG developers.

Lea: I hadn't even thought about wysiwyg. Yeah. Also given it works in that way I'm not sure what is the benefit over a js library. that's exactly what a js does, remembers th elast state. Seems the main benefit of this is avoiding including a js library. The drawback is that it breaks one of the very fundamental design principles of css

Dan: you say the theoretical purity is ..

Lea: is it theoretical purity?

Dan: not if that's a principle that has all of these other benefits for developers and for the platform and tools. It's not theoretical purity, it's more.. purity.

Lea: I don't want to stop progress because of purity

Rossen: not about stopping progress, it's about whether or not the language constructs are invalidated

Dan: if other things make that assumptions, tools and stuff that processes css or that authors css makes that assumption and that assumption is broken by this thing.. the feedback from someone else - is that the side effect introduced does not persist after the property has stopped applying. Does that mean there's no side effect at all?

Rossen: well. *after* the property has stopped applying. You have to ask - what is that 'after' point? If the property applies at a particular frame, when all of the stylesheet and everything is calculated, then this is consistent with css. The effect of the property here is based on some user action, scroll things into view etc.. 

Dan: if there's something to push back on from a purity perspective we're definitely the ones to do it. We shouldn't pull back from that unless we think they are willing to clarify the design or change the design so it does not have this property

Lea: where do you see this quote?

Dan: in [comment from 28th April](https://github.com/w3ctag/design-reviews/issues/624#issuecomment-828597281). 

Lea: a different property.. if contain intrinsic size auto is applying, the size is remembered for as long as content visibility auto is applied as well. If content visibilty auto is removed the ua forgets about the size. So there is a side effect when contains intrinsic size auto is removed

Dan: why don't we clarify that?  I'm sympathetic to the use case of faster rendering

Lea: that's why I'm saying I'm not sure we should stall progress

Dan: worth continuing to raise the issue. There are side effects to changing this side effects thing. there are unintended consequences where if you change a precept that everyone working in this space knows and agrees to then there are the possibility of unintended consequences

Lea: we said they're breaking the princiople 100% of the time and they made a change so they're breaking it 30% of the time.. but if they're breaking it even 1% of the time it's no longer a universal assumption. Every tool that processes css now needs to take that into account, this edge case, this different behaviour

Dan: that needs to be written down in our feedback.

Lea: I can write a comment

#### [review request, CSS Masking and Clipping](https://github.com/w3ctag/design-reviews/issues/665)

Lea: that is a very advanced spec

Rossen: personally at a loss what to do. Sometime back one of th eideas we had was for such CSS requests to have the non-CSS people do them so you can get exposed to a whole feature area of css that is moving forward and is mature etc. Spot checking this work from someone who hasn't been jaded so much for so long.

Dan: if I were addressing this issue from the beginning I'd say it's not a link to the explainer, it's to the ED, and it doesn't start with user needs, and it doesn't explain the feature.. Is that useful in this context? Obviously a huge amount of work has gone into it.

Rossen: this has been shipping across all browser for 3-4 years maybe more

Lea: way more

Rossen: I remember doing this in IE9

Dan: in order to do this kind of review where people not immersed in the community can com einto the material and understand what it is without that archaeology we need a real explainer. Is there a halfway where we could .. another approach someone who is part of the community presents it to the people who are not.

Lea: who is the explainer for? if it's to help us review the design then do we need really need one? It's very mature, we're not going to say change stuff. We don't actually need an explainer. Do we need user needs to know this drawing primitive of being able to clip or mask parts of elements is important? This is a fundamental drawing primitive

Dan: yeah..

Lea: I'd be inclined to close it, ask for future design reviews to include an explainer.

Dan: also looking to see if there's already an explainer on MDN

Lea: I don't want someone to be tasked with writing an explainer for this if we don't need it

Rossen: I agree. The problem is the design review template assumes new design. This is a different template, this is simply rubberstamping something going into REC

Dan: still feel it is worth pointing out that yes the spec has nice pictures and people who are familiar with drawing will know that masking and clipping are important aspects. AT the end of the day the reason why some developers find parts of the web platform very opaqe to learn is because this kind of material never emerges, where someone says "when you want to draw things.. the concept of clipping and masking is important.. this is what this is *for*" MDN documentation is all the same sort of thing and assumes you know what a mask is.

Rossen: [makes a covid mask joke]

Lea: there is a lot of material on the web discussing these features

Lea: [writes closing comment]

Dan & Rossen: +1

#### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) 


### Session 18B

Present: Dan, Rossen, Amy

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516)

Dan: I think we need to close this one.. we have multiple ways of communicating with Blink.

#### [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) 

Amy: the specs its based on were closed satisfied, but were early review. This a case of a feature being built on something that is not a standard yet

```
Hi @mfalken - one thing to note is that Speculation Rules itself is still in a private repo. 

@jeremyroman is this indeed in WICG? Yes there has been a positive TAG review that was based on an "early review" - if this feature itself is still in incubation then maybe it's premature to start building stuff on top of?   

Regarding speculation rules, Chrome Status still shows "no signals" from other implementers or developers. Is there any multi-implemnter implementation?  Again - a lack of consensus on speculation rules itself could mean that it's premature to base other features on it.
```
#### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) 

Blocked behind First Party Sets
