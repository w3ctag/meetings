# TAG Teleconference
#### 07-09 February 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-02-07](https://www.timeanddate.com/worldclock/converter.html?iso=20220207T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @atanassov
* [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @hadleybeeman
* [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @torgo, @rhiaro, @hadleybeeman, @plinss, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov
* [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @plinss, @atanassov
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov

### Breakout B (US / APAC) - [2022-02-08](https://www.timeanddate.com/worldclock/converter.html?iso=20220208T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion
* [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou
* [ObservableArray, and its use by adoptedStyleSheets](https://github.com/w3ctag/design-reviews/issues/693) - @LeaVerou
* [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/704) - @hober, @atanassov
* [[CSS-Values-4] FYI review of Allow infinity, -infinity and NaN in CSS calc()](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov
* [Review request before CR:  CSS `selector()`](https://github.com/w3ctag/design-reviews/issues/709) - @LeaVerou, @atanassov

### Breakout C (APAC / Europe) - [2022-02-08](https://www.timeanddate.com/worldclock/converter.html?iso=20220208T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo
* [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @cynthia, @rhiaro, @hadleybeeman
* [`handle_links` manifest field ✨](https://github.com/w3ctag/design-reviews/issues/695) - @cynthia, @ylafon
* [HIDDevice forget()](https://github.com/w3ctag/design-reviews/issues/703) - @cynthia, @torgo
* [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo
* [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon
* [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @cynthia, @LeaVerou, @torgo
* [Review request for Confirmation of Action API](https://github.com/w3ctag/design-reviews/issues/713) - @torgo, @rhiaro

### Plenary Session - [2022-02-10](https://www.timeanddate.com/worldclock/converter.html?iso=20220210T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage


-----


## Breakout A

Present: Amy, Dan, Peter, Yves, Hadley

Regrets: Lea

### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @atanassov

### [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @hadleybeeman

[everyone watches videos: [registration](https://www.w3.org/2021/10/adyen-spc-reg.mov), [authentication](https://www.w3.org/2021/10/adyen-spc-auth)]

Dan: it's a seperate flow from webauthn even though from end user perspective they might be seeing similar kind of UI. Have we answered the question - is information being transmitted to the website that discloses something about the authentication capabilities of the client during this transaction? Ian is saying with web authentication only the RP... can the website tell something about which authn mechanisms exist on the client in a way they can't do in a webauthn session? 

```
Hi @ian - it's not clear to me if the web site (or another party) would, in the context of this transaction, be privy to information about the authentication mechanisms on the client which might give them more info about the end user than the user would expect to be sharing?  For example - would the web site know that a biometric dialog had been shown to the user?  What if the user chose to dismiss that dialog and opt for another authentication mechanism?  In other words - they click "cancel" on this dialog box?  Would the web site be able to detect that?
```

Rossen: good question. I hope the answer is no the website doesn't learn anything other than if the transaction completed or not.

Peter: 3 parties - user, web site, bank... What about the Payment Service Provider - and an API... web site always uses an API to the PSP... I never talk to the bank. Like Stripe. I have an account with them - i give them the CC info and PSP handles the interation with the actual bank.  

Rossen: that's the equiv of you working with the bank directly... where the middleman comes into play is they create a one to many relationship.  From the PoV of you being hte web site author - whether is is PayPal or BofA - it's the same thing.

Peter: concern is - the way it works is that I register a public/private key pair with my bank as a consumer.

Rossen: which you have given to paypal...

Peter: I go to web site - they don't talk to my bank... they talk to paypal. is there a backchannel... 

Hadley: PSPs are higher liability transaction providers... 

Peter: one would presume the existing flow of dealing with a PSP - this would be the same. PSP should be able to talk to the bank ... Don't see it described anywhere.

Rossen: from my recollection - i'm convinced the range of parties are involved.  

Peter: i want to talk to one payment processor.  Comment from Ian that it doesn't depend on bank collaboration. Do I have to register with e.g. Stripe or Paypal? 

Peter: [posts question]

Hadley: standardized payment method identifiers... behaves - you as merchant you need to have the URL to the payment provider that the purchaser intends to use...

Dan: that might be accomplished in a js library you bring down from stripe?

Peter: as a website developer I have refused to use js libraries that payment processors have asked me to use becuase they contain other things like unsanctioned tracking. So I don't want them to have to grab the whole bundle and let them run whatever code they like

Hadley: this is an important issue and we do need to go down this rabbithole. Do we want to open another issue for this? Wnat to make sure we can give it its full due.

Rossen: I agree. If we start it as part of this issue then fork it into a broader scope issue that will end up in their github repo that will give us better visibility to drive it.

### [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @torgo, @rhiaro, @hadleybeeman, @plinss, @atanassov

Dan: I'm looking at the response to Peter's question about private keys on devices.. I don't understand why "most websites would not use this" or how what he describes is different from what you said you thought it was..

Peter: what I was thinking was a system wehre you have a hardware key which is non extractable and a set of softwar ekeys which are syncable and you use the hardware key to countersign the public keys of the syncable keys. 

Dan: I think they're thinking about this in terms of keys that are already being synced across some back lane, so the main key is not a hardware based keys, it's a key being synced.. the website that's using it wants to have some additional information about 'you're now authenticated on thsi device and I know this public key is only associated with a private key that's only for this particular device and I have that in addition to the main synced key' - so that would provide some kind of additional 'we haven't seen you on this device before' type thing. The whole thing is based on the idea that the main key is not tied to a specific device

Peter: looks like their extension is you sign in with two keys, neither of which signs the other, but one is tied to a device and one is synced, so you know it's you and you know which device it's coming from. That looks like what they're talking about.

Dan: I do wonder why they think most sites wouldn't use it

Peter: maybe most people wouldn't bother or care

Hadley: worth asking

Dan: [leaves comment]

Peter: the fundamental problem with syncable keys is creating a vector for the keys to leak. What I was describing was you still have a physical key that you only use once every so often, when your other keys expire, to resign all of your syncable keys, but on a daily basis you use your syncable keys. It doesn't rptoect you from being leaked but lets you rotate keys frequently in case they do get leaked, and sites still know who you are because your identity is based on your hardware key

Hadley: and I was asking about the states where....

Yves: key repudiation? I don't know.. can you inform the site a specific key has been compromised?

Peter: is there a mechanism for revoking key like that? Instead of whatever the sites mechanism is?

Yves: replace it with a new key or a repudiation system?

Peter: afaik with sites i"ve used webauth on so far you just log in and replace your key or tell the site you're no longer using that key. I don't know of a platform way. Something where you tell the browser they key is no longer good and the browser tells sites not to use it?

Yves: that would be something

Hadley: like telling your bank you've lost your credit card

Dan: I also asked about the design Peter mentioned. We talked last week about in the larger response from Adam it seems like he's really pushign back on requirements about safety of the key sync fabric as you suggested Hadley and I'm wondering what we ought to do about that

Hadley: I'd think at a bare minimum it would not be inappropriate to lay out in the spec these are dangerous. Not uncommon to do. If memory serves they don't yet have a spec for this. If nothing else, being able to share with implementers we thought through some potential pitfalls or drawbacks - we're sharing with you so you can take stesp to minimise them. 

Dan: implementers should be cautious of

Hadley: that's different than coming up with a set of normative statements

Dan: My preference would be to leave that comment, get the feedback on whether they've thought about this alternative design, and try to close the issue based on that? We're pointing out the issues but I don't think anything here is a killer

Hadley: sounds sensible

Dan: the other thing I see, which I appreciate, is that this is a working group proposal, multi stakeholder, the contacts are not just the implementers, this is good

Hadley: and early enough to talk about the design, but also mature enough that there's something to work on

Dan: the group chair is one of the contacts, but is there any controversy about this approach in the WG do we know?

Peter: there are a few things in the explainer we haven't really looked at. Conditional UI.. preventing unintended credential overrides..

Dan: we closed conditional ui review last week. I think that's okay. 

Peter: thing that lets the website tell the device a key has been deleted... seems useful. Leave feedback about doing that the other way around? Browser could tell sites?

````
Thanks for the thorough and thoughtful reply, @agl.

While we appreciate that you aren't keen for the spec to list mitigations or privacy protections on the part of the credential sync fabric providers — which we understand — it is useful to brainstorm them. You, as a working group, will have put more thought and energy into threat modelling than anyone else at this point. It's valuable to capture that.

We'd recommend that you include something in the spec, when you get to drafting it, to share some of this thinking with implementers (even something as simple as "users are trusting credential sync fabric providers to keep their keys secure. While the mechanisms of demonstrating that trust or keeping those credentials secure is out of scope for this spec, we are flagging to implementers that they may need to focus on this problem. Without it, the entire feature won't work."). 

While the implementers may choose to address the issue in different ways, it's still helpful to give them that warning/benefit of your advanced thinking. 
````

### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

### [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov

### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov

### [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @plinss, @atanassov

### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov


## Breakout B

Present: Peter, Max, Lea

Regrets:


### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion

Max did some review, will coordinate with other assignees.

### [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov

Left questions about shape of API, overall looks reasonable so far.

### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

Left question about API shape.

### [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou

### [ObservableArray, and its use by adoptedStyleSheets](https://github.com/w3ctag/design-reviews/issues/693) - @LeaVerou

### [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/704) - @hober, @atanassov

### [[CSS-Values-4] FYI review of Allow infinity, -infinity and NaN in CSS calc()](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov

Left question about NaN converting to infinity.

### [Review request before CR:  CSS `selector()`](https://github.com/w3ctag/design-reviews/issues/709) - @LeaVerou, @atanassov

Reviewed, non-controvertial, closed satisfied.


## Breakout C

Present: Sangwhan, Max, Dan, Yves

Regrets:

### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo

Sangwhan: updated explainer but fundamentals have not changed

Max: updated but not addressed all the comments from the TAG review

Sangwhan: we brought up the idea of trying to merge it with page lifecycle, not sure what else we can do

Dan: they say page lifecycle is a wicg work item and they're not sure if there's interest from other groups to develop it. Maybe we can say thank you to Qing An for the updated explainer but can they further address the issues that we've raised

Sangwhan: [leaves comment]

### [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @cynthia, @rhiaro, @hadleybeeman

Dan: **punt to plenary?**

### [`handle_links` manifest field ✨](https://github.com/w3ctag/design-reviews/issues/695) - @cynthia, @ylafon

Dan: extension to the manifest file, to do with handling links

Yves: difficult to review without looking at all things -- goal is to replace pwaURLhandler - here they want to be able to use mediatype regexp on URL (which is **bad**) - so really need more time to look at all ramifications... so `handle_links` in manifest seems pretty harmless but need to look at big picture.

Sangwhan: it seems reasonable. 

Dan: why do they need regex on urls?

Yves: they want to use regexps to understand if it's a media file etc...

Dan: that's not happening. 

Sangwhan: [not mninutable]

Yves: in the past they defined new protocol handlers... so it's getting a bit better but still need to focus on using proper media type - can be dedicated for e.g. if you have audio/something then can pop up audio player - use the scope as a way to match. Still - it should be based on media type.

Dan: you can't assume based on the contents of a link

Yves: you might have a permission prompt or a login. And it's not playable.

Dan: this is basic web architecture

Sangwhan: there's a question about if iti's possible to change the handle after the pwa has been installed. I'd guess no?

Yves: the manifest should be a hint, just sets the initial value in that case

Sangwhan: and you have a getter and setter against the manifest?

Yves: against the manifest I don't know but may be used as an initial setter for the app, depends how it's used

Sangwhan: imagine the case where you have a settings dialog where the user can switch between open in the pwa or as a new thing. That would require modifying the value from the application, I don't know if that's possible. Seems like something application would want to do?

Yves: should be based on user preference

### [HIDDevice forget()](https://github.com/w3ctag/design-reviews/issues/703) - @cynthia, @torgo

Sangwhan: this is lgtm - obvious addition - we should think about adding more of this pattern - allow apps to give up permissions and request as they see they need it. Right now the permissions dialog - people don't give a damn about it (data shows). 

Dan: can we cite published results about that?

Sangwhan: https://developer.chrome.com/blog/permissions-chip/ -- "most permissions dismissed or ignored" -- maybe we should revisit permissions in web architecture.

Dan: that brings the topic of permissions budget or privacy budget...

Sangwhan: back to original topic - forget is a mechanism for a web site to - they have a handle to the device - and forget releases that handle.  

Dan: why would they do that?

Dan: Left a [comment](https://github.com/w3ctag/design-reviews/issues/703#issuecomment-1032384025) - maybe we can still aim to close this week.

**François left a response -- we can discuss more in the plenary**

Max: what is the user interaction? If the HID device forgets, does this notify the user?

Sangwhan: there's no interaction from the user end, the user is not notified

Dan: but after it's forgotten if it needs to be reacquired a new permission request will have to be made.

### [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo

Sangwhan: the jist is - it lets you stream over a shared screen an element - e.g. one ``<div>`` - the target is an element, not a region. So the name is confusing. You feed it an html element and it starts streaming it. 

Dan: Over web rtc?

Sangwhan: whatever.

Dan: [reviewing s&p questionnaire responses] ... LGTM *proviso that users may not know what they are sending when they select a target... Sangwhan to clarify in question*.

Sangwhan: produce crop target will always ... what should happen - you can create a new html element that is detached from the DOM - what happens when you feed that ... that's one question we can ask. Also not sure how you can convey to the user what is going to be sent over the wire.  Don't understand the user flow - you could hover on that div and share that... you could put an event handler on it...

Sangwhan: I think it would be better if it was not element bound, but box bound

Dan: that would be more intuitive for the user. if they just want to share one section of the document, but if they start adding text to that section it starts to get bigger

Sangwhan: one div and you're writing stuff in that div

Dan: is that the intended use case? That's not in the explainer

Sangwhan: what I think this is going to be used for... to share the part where the document is.. 

Dan: question you should still ask is how this works from an end user perspective, how can they be informed about what they're sharing and not sharing, and why isn't it just a good idea to send a crop of the area

Sangwhan: the box. For example you'd be letting users select stuff, completely bizarre because you'd be doing the equivalent of [opening the inspector] ..

Dan: use case of selecting a div, dev tools came to mind

Sangwhan: how to find the common denominator [from the source code] of what to project. I'll ask those questions.

Dan: it's officially adopted by the webrtc wg as a work item

Dan: could users unintentinally expose more than what they intend?

Sangwhan: I was going to ask about the preview. User should know what they're sending.

Sangwhan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/710#issuecomment-1032403736)

### [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon

Yves: seems weird that you want to give specific settings for something that is remote -- what happens with the maintenance of those hints - what happens if the URL doesn't require those hints any more - i will look into it...

### [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @cynthia, @LeaVerou, @torgo

**punted to plenary**

### [Review request for Confirmation of Action API](https://github.com/w3ctag/design-reviews/issues/713) - @torgo, @rhiaro

**punted to next week**

## Plenary Session

Present: Tess, Peter, Amy, Dan, Max,

Regrets: 

### Breakout Rollup

#### Breakout A

Dan: we talked about secure payment confirmation, and wrote a note about a privacy / fingerprinting issue - what information is available to the website, and analysis on the user flows that Ian had sent us (videos), to understand if the website would be able to tell that the user had chosen not to use a biometric confirmation, exposing user choices in a way they might not expect. Ian has [got back to us](https://github.com/w3ctag/design-reviews/issues/675#issuecomment-1031789463) - the spec specifically addresses the issuse. The requesters have been receptive to our feedback and are doing the right thing. There's an ongoing discussion with Anders but I think it's out of scope. My suggestion is to close.

Peter: I would like to post a comment first.

Dan: then commented on broadening the base of webauth, about syncing private key credentials across different devices. Peter, Hadley and I left questions. Probing the issue of how much they can put into the spec to ensure there's appropriate security in place for private key credentials. FIDO is based on a secure key but if you take away the secure key and replace with a software layer that is syncable how d you maintain the integrity. Adam has responded suggesting a PR. 

#### Breakout B

Peter: Max, myself and Lea.  Max had done some review on WebGPU ... to coordinate with Sangwhan... Setting offline time. We looked at #694. Mostly OK.  Asking questions on shape of API.  Abort signal timeout #711. Need to respond to Dominic. Allowinf infinity... #708... posted a question - got a response from Tab.  I think it's OK. Need to think how it plays with variables.  More of a CSS implementationd detail.  CSS selector for supports - fine by us. #709 - closed (satisfied).

#### Breakout C

Dan: assigned Max to miniapp lifecycle, Sangwhan left a comment. EPUB punted to plenary. Handle_links manifest has some issues because of url regex. 

Tess: is that using the url pattern thing that gets used somewhere else? or its own bespoke thing? Ben Kelly at google was driving the url pattern work? If they're doing some kind of regex in urls they should align with that. Probably is the same thing.. 

Dan: it doesn't mention url pattern in the explainer. Could you leave that comment?

Peter: used in manifest somewhere?

Tess: it's intended to be used in more than one place.. Probably service workers? Probably elsewhere too.

Dan: HIDDevice forget() is about forgetting handles. This is an additional feature on top an existing API. Is this about privacy budget? Answer was kind of no. Also a response to Max's question. I think we need to think about this more. It's simple but wait til next week to close. They haven't provided an explainer. Articulated system need but not user need. Region capture #710 - in webrtc wg - capture a segment of a document to stream. Sangwhan left a comment, received a response, continue next week. Yves working on markup based client hints delegation. Dark mode support punted to plenary. Confirmation of Action API punted to next week.

### [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684)

Amy: we've opened issues in their repo and they've discussed in their meetings, addressed some - they're listening but no action yet.

### [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/704)

Dan: I asked about venue.. WHATWG..

Tess: some things into the Fetch spec

Peter: looks pretty straightforward....  

### [Dark mode](https://github.com/w3ctag/design-reviews/issues/696)

Tess: I was involved ... i think it's fine ... i wish there was more alignment between CSS and web manifest in terms of how things are expressed.  But two languages are under diffeent constraints considering processors that handle web manifest files and how much of the web stack is available to that processor... certainly they ended up with a solution that's fairly simple and extensible to other theme color type things... like having colorscheme .. seems sensible to me.  These are initial thoughts.  

Dan: they punted on s&p review, does it make much of a difference? Information already exposed through CSS. Multistakeholder support? After incubation?

Peter: colour scheme and a set of keys rather than colour scheme _ is more fragile for extensibility. How adding more css colour scheme media features fits in, if they're putting values with the key names

Tess: fair feedback. Doesn't seem that bad now because they only have this once case, but adding more gets ugly

Peter: only dark and light right now, but others might be defined in the future

Dan: punt to next week

### Issue Triage
