## TAG Face to Face
##### 07 April 2018

Present: Travis, Dan, Peter, Sangwhan, David, Alex, Yves, Hadley

Guest: Andrew-san

Regrets: Łukasz, Tim, Kenneth

---

Agenda:

## Breakouts (Group B)

### Dan, Hadley, Yves, Sangwhan

### Issue 238 - Keyboard Maps

Hadley: how much of an issue

Sangwhan: this is a real problem for people 

Hadley: are there enough situation where keyboard layout needs ot be uniform

Sangwhan: this provides an API to provide info to user

Hadley: how often is this needed?

Sangwhan: quite often -

Yves: the games ones using WASD

Sangwhan: WASD on another keyboard layout is nonsensical

Yves: US keyboard mapped to french keyboard - can I do it using this? You just get a keyboard map...

[discussion on what the interface would be]

Dan: On the explainer: re the user scenarios, starts with "applications like games use the keyboard...".  Missing: what is the user trying to do? The user is trying to play a game. And is running into these problems. 

Dan: focus on games?

Sangwhan & Yves: other apps as well e.g. CAD... word processing... Anything where you want to do keyboard shortcuts.

Dan: I'd still like to see the user scenarios in the explainer be more user-centric - describe the problem solved from the user's PoV...

Sangwhan: 3.1 (change event) needs to be better defined.

Sangwhan: if you have multiple keyboards how does this work? E.g. if you have a laptop keyboard propped up on a stand and another keyboard on your desk.

Yves: there should be a keyboard identifier. The getkeyboardmap without argument should be a default keyboard...

Sanghwan: some OSs don't let you have that kind of access.

Sangwhan: keyboard change event should be clarified

[discussion on whether it should be using promises]

Hadley: Given that what this is doing is replacing the value of a key with another value. There's nothing that would highlight the user that is going on...

Sangwhan: it doesn't replace. It doesn't change the mapping of the key.  In the UI it will say ctrl-c to copy. If ctrl-c is in an inconvenient location, and z is more convenient. Then the UI can show "press control-z to copy". But the keyboard map.

Dan: is there a way to use this to fraud the user?

Sangwhan: no

Hadley: Ah, 2.2 says it's readonly. it might be useful for them to highlight this in the explainer.

Sangwhan: there is a potential fingerprinting issue.

Dan: is there a privacy / user tracking / surveillance issue?

Sangwhan: but accept-encoding accept headers also has that information...

Dan: in which case, should we be advising that when the user is in Private mode this shouldn't work... or that the spec should indicate that UAs can normalise this if you're in a sensitive situation.

peanut gallery (david): if the user presses a key today you get this...

peanut gallery (alex): if you'd like to put it behind a permission in the future then it should be a promise.

Hadley: my OS is in french and keyboard is english. 

Sangwhan: you could harvest keys...  If you log all the keys being pressed you can deduce a lot of this info... was the feedback fromt the other group...

[we move to raise some issues ]

Sangwhan: many of these issues have been raised - they have a privacy concerns section...

### Media Autoplay As a Permission (203)

Dan: Since this is not a review of a specific spec, what is the output that we could produce here? A blog post? A finding? ... A point of feedabck on some spec that is moving forward? Is there a relevant spec? Do we have an opinion?

Coming back to the user need, this is about how user's decide whether auto-play video is OK. 

Hadley: this is about how browsers intervene on behalf of users. There are a lot of developers who want autoplay to happen regardless of user's opinion. Violation of the user's choice..  Users should have control of that.

tension between whether users control or webapp controls..

Sangwhan: would this be feedback on HTML?

Hadley: permission API is in working draft. https://www.w3.org/TR/permissions/

Alex: best place would be to raise an issue on the permissions API spec. https://github.com/w3c/permissions

Dan: a potential output is just to say to the permissions API people: the TAG have been thinking about this.  We think autoplay should be modeled as a permission.  We suggest you incorporate this into the design of the permissions API.

however: permissions API is stalled, and Mounir has said Chrome couldn't 

Dan: other option is to take the feedback on board from the commenters on the thread and close it.  Is there a TAG view that we can voice.

Hadley: the fundamental "what it needs to be for users - users need to be in control" should be voiced.

Dan: regardless of how it's implemented, the user should have control of this behaviour. That could mean for example having a setting "yes, autoplay" or it could mean orgin-specific permissions prompts. "yes, netflix can autoplay vidoes".

Dan: Either we write something and try to push on this somewhere (e.g. permissions API) or we drop it. We need to take that decision in plenary.

[taken to plenary]

Alex: is it reasonable to model this that way?

Hadley: our TAG view is that web serves the user first. So [not being able to disable autoplay] is similar to discussion on users not being able to block trackers or ads.

**RESOLUTION**: media autoplay should be under user control; that could mean for example having a setting "yes, autoplay is OK across the board" or it could mean origin-specific permissions prompts. "yes, netflix can autoplay videos". ---> therefore modeling autoplay as a permission is desirable because the diversity of effective policies will require that sites be able to introspect the policy without attempting to play media. 

### Issue 232 BCP56bis

Dan: We have been requested by Mark to feedback on this. It's gudiance for IETF spec developers on how to use Http - which is something to do with web archiecture...

Dan: there's not discussion of get method being idempotent.  This may also be covered by the "GET should not have side effects".

Sangwhan: where's the explainer?

Hadley: he asks "should a spec define a new URL scheme or port" but then recommends "establish their own" ... it would be useful to know why.

Yves: one issue when WEBDEV was done.. new http verbs minted.. it was seen as being an abuse of creation of new verbs... There was a need at that point to create original bcp56. Since then patterns of new protocols based on http have changed as well. also ... too much stuff in .well-known ...

Dan: why not stronger on https ? any new http-based protocol should be https especially when protocols are using authentication tokens.

Sangwhan: what has changed between this and bcp56?

Sangwhan: the language should be simplified to enable this to have a wider audience.

Yves: having a specific section on options might be good. 

Sangwhan: "don't use options"

Yves: it could be that.

Dan: should there be more discussion on other methods - currently some in-depth discussion on GET. 

Sangwhan: +1

Hadley: 4.12 "some considerations include" very vague. Whole section needs to be more concrete advice. More examples needed.

Yves: perhaps adding a mention of variants.

Dan: encourage a link to data-on-the-web best practices?

Hadley: yes potentially. It fits as another use of HTTP (that isn't web browsing) https://www.w3.org/TR/dwbp/ 

### Issue 237: .well-known (related to 232)

Peter: some of the things they are talking about using well-known for shouldn't be using well-known. SRV record.

[SRV records are a DNS entry]

Peter: a common thing - caldav - if I want to give you access to a calendar, I can tell you peter@linss.com - it looks lik caldav.linss.com - this is in a caldav registry.  DNS lookup for SRV record for service name e.g. caldav - that returns a host name and port number.  Like a general-putpose MXRECORD.

Dan: arguments against SRV records?

Peter: (1) you can't do a DNS lookup from Javascript in a browser. I assert that should be fixed. There should be a web API for looking up SRV records and txt records. (2) Argument that some people don't have good access to setting up DNS records. (3) you only get a host and port, not a full URL path...

Sangwhan: in enterprise environments, a massive hassle.

Peter: .well-known flow for CALDAV: i type peter@linss.com. I have to have a web server at linss.com - the browser goes and looks up linss.com/.well-known/caldav and gets a redirect.  Well-known could be a json file or some other reseource at that location. Structured data.  But a large number of things they are proposing can be done with SRV records.  It shouldn't be precluded.

Dan: who runs the registry for service names? 

Sangwhan: IANA in both cases.  Differences in the layering.

Sangwhan: I believe having this info in the web platform is useful.

Peter: yes, and therefore SRV and txt records should be available to Javascript.  .well-known should be available but not appropriate for all cases it's being put to. For CALDAV they do both.

Peter: srv records also have the benefit that you can have multiple ones. Like MX records, you can have multiple fallbacks.

Peter: well-known falls down if you're running multiple services in the same host - multiple calendars for example... 

Yves: well-known defines URL patterns...

Peter: SRV records don't have it either...

Peter: if I'm running a service that's not http, why should I have to run a http server just to aid discovery.

Sangwhan: also SRV allows you to offload discovery to DNS network... which is distributed

Sangwhan: protocol boot strapping 

Dan: if we recommend use of SRV then we should recommend SRV and txt record lookup in JavaScript

Sangwhan: DNS-based poly-fill prototype that uses DOH... for DNS lookups in JavaScript

Peter: risk is exposure of internal network info through DNS - also all sorts of other stuff you don't want to expose to JavaScript

**RESOLUTION**: we don't think .well-known is best place to do boot-strapping. We propos SRV - if there needs to be extra structured data-or sub-origins then .well-known is an option. 

Hadley: also well-known goes agains the architecture of the web - designating URLs do in fact take away the origin's authority to designate its own resources. I (generally) understand why we have the well-known URIs that we have, but I think we should emphasise that they are the exception, and new ones should be used sparingly. 

### Issue 329: 

Dan: I'll solicit mnot's feedback.

... any other issues?

David: I think it's worth experimenting with.

Hadley: how long the scaling process would take?

Alex: there is a counterpoint: as more and more of the web becomes TLS only...

Peter: if we push everything too hard to secure context and provide an escape hatch then people will 

Alex: this proposal sparks a question - would it be possible to add the secure attribute to cookies created on secure connections... natural end-point would be to switch the default...  

---

## Breakouts (Group A)

Group A participants: Travis, Andrew, Alex, David, Peter

#### Issue 233: :focus-visible

Andrew: still working to understand the use case for this...

David: Matches when the UA would show the focus-rect. Helps workaround for devs that would remove the focus styles that then impact users that need the focus ring (when the user agent would actually draw it--e.g., when the keyboard 'Tab' is used.)

All: Reviewing Rob's PR https://github.com/w3c/csswg-drafts/pull/2481 and adding comments to it.

#### Issue 206: Accept-CH

All: Reviewing Alex's proposed text

Andrew: What worries me is that this is a framework... imagine 10x the hints all flowing through. How does it make a difference to what developers will do? If developers get these hints that make it too hard to render the web page without them, they _will_ do the redirect (because they can't get the hints in the initial request).

David: Requires opt-in because it's a response header.

Andrew: Also, `Accept-` on the Response is weird.

David: Not keen on the proposed language on privacy/fingerprinting.

Alex: if you have a privacy concern--don't implement client-hints. Will work on revising...

All: Revised and commented in the issue.

#### Issue 235: Signed Exchanges

Peter: As currently specified, this uses a separate cert that prevents the cert from being used in TLS . Rationale--key leakage does not compromise your other security aspect.

Andrew: The other cert could be complicated.

Peter: Your publishing process could do all the signing offline, which raises the bar on security--so I get the split.

Alex: Are you worried about miss-issusance.

Peter: Would like to see an additional method for an offline user to validate the certs recieved are legit. The actual exchange doesn't carry the cert in-line, just a URL (all you can do is trust the Root CA issuer).

David: how do you get these certs? Can letsencrypt do it?

Alex: not yet, but maybe in the future. No block for any CA to start doing this.

Peter: What happens with HSTS/HPKP headers in the signed exchange? Should they be disallowed?

Alex: Thing about stateful headers in the spec... (looking up). Yes, disallowed; may want to include those headers specifically for clarity.

Peter: Also, `Expect-CT`, `Expect-Stable` (being discussed), etc. 

Peter: we often have "trust on first use" and I'd like to see that diversified if possible.

Andrew: Why is a request included in the response? Want to understand the use cases better? Is it because the response might vary based on aspects of the request? Are we sending it to be similar to HTTP2-push?

Alex: Some of this disucussed here: https://wicg.github.io/webpackage/draft-yasskin-webpackage-use-cases.html#rfc.section.3.1.2. Maybe you could be able to include multiple responses pairs for a given URL?

Andrew: Imagine a site with a large diversity of languages and encoding variations (gzip, etc.) as well as a large payload. If a signed exchange includes all possible variations, then that would be a huge combinatorial problem--we assume that's not the case.

Alex: Does the request (as part of a Signed Exchange) go through a registered Service Worker?

Andrew: Shall we generate a set of questions?

Andrew: Can I put exchanges from multiple origins into a package?

Alex: yes, cool eh? And they can include other packages too! But this is more a question of packaging (rather than signed exchanges).

Andrew: is the Request represented in a way that is consistent with other formats like H2-push serialization?

Alex: It doesn't do multi-plexing/fragments/chunks (like H2). The two aren't comparable. Open question was: do we want these exchanges to more closely match H2? Answer: no. Tools will be able to seek into it... enables Random access to the content (which is important).

Andrew: Interesting: hostname is in the request line? Is redundant with Host: header.

David: Turns out this is OK (supported). Apache is OK with hostname in the method request, but doesn't like it when no Host: header is sent.

#### Issue 186: signature-based SRI

Peter: I still have the concerns noted in the issue (can do this without keys--just like signed exchanges...). Signed exchanges _can_ go to certs if desired, but is not required. Mmm.

For 'hash faking' I have to keep modifying the hash--replay is not so easy. For 'signature-faking' (if I can get you to beleive my signature is someone else's), then I can just keep re-playing that signature everywhere.

Andrew: Notes that Mike's latest reply is not keen on 3rd party SRI--mostly just first-party.

#### Issue 213: modulepreload

Alex: don't think you actually can build module-preload on top of fetch (Anne's comment in the issue.) E.g., the cross-origin parts can't be parsed/figured out because fetch returns an opaque response for cross-origin content.

Andrew: and we had feedback around the name-- maybe this could be split into two--preload, plus another attribute describing what to preload, instead of potentially growing the set of `preload-*` things.

#### Issue 231: Payment Handler

All: Brushing up on the feature (thanks David)

David: Does the API make the right tradeoffs for the user? Is there such a thing as a malicious payment handler?

Andrew: What's the worst it can do?

David: Pay people my money? But it can't seem to do that on its own...

Andrew: Is it possible for a payment handler to be evicted?

Alex: yes. Evicted on the origin-level

Andrew: One service worker could handle all SW stuff--including the payment handler logic; UA's may need to mitigate this by not firing some events related to payment handlers to the service worker.

David: On number 5 - does this add new method of communicating with origins that doesn't happen today? Does it enable cross-domain comms in a way that isn't supported today? Sounds like it can be related to cross-origin iframe's and how SW work there--no new surface area.

David: Point 4, proliferation of manifest formats. Shall we ask it to merge? There are icon's for which the format for icons is different than the web app manifest's format.

Alex/Andrew: we are very much in favor of this. Yes.

We watched a clip about [a perfectly cromulent word](https://www.merriam-webster.com/words-at-play/what-does-cromulent-mean). Important cultural moment.

## Plenary discussion

### Issue 222: Async Clipboard API 

[ a bunch of unminuted discussion ]

[ Discussion about permission needed to paste, and stealing data from the clipboard ]

Many people (Hadley, David, etc.) don't think various restrictions (e.g., on user action, focus, etc.) are sufficient from a security perspective.

### Issue 72: task scheduling

Bumped to May 1. @dbaron to do some work. 

Travis : we need to end up with "this part of the event loop is good, this needs to be changed"

### Issue 105: TV-Specific Web Subsetting

Discussion of what to do with this. Should we write a new document or close this issue.

Dan: maybe we should review the new version.... 

Andrew: I'd like us to be helpful...

Dan: I will take an action on this - to get hbb people to request a review.

### wrap-up

**RESOLUTION**: Thank you Andrew for your contributions to the TAG!
