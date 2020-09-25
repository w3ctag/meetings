# 22 Sept 2020

## 01b

Alice & Dan

### WebXR Layers https://github.com/w3ctag/design-reviews/issues/528

Alice: Nobody else has looked at this yet AFAICT.

Dan: I've looked at the explainer previously, taking another look.

Alice: I'm having trouble telling which APIs are new under the "Usage" section.

Dan: Could ask them to make that clearer, what the things are they're introducing. 

... Kind of confusing because the word 'layer' isn't used in the API definition.

... You create a canvas, and then you set it to XR compatible...

Alice: So `XR[...]Binding` is the layer factory, I guess?

... in the next section, they call `createProjectionLayer` on that object. So it seems so.

Alice: It would be nice if they could also spell out what the different `create___Layer` options are. Reading between the lines, `createProjectionLayer` creates an `XRProjectionLayer`, but what are the other layer types and how do we create them? What does `createQuadLayer` create?

... oh, later on they link to separate explainers for each layer type (other than `XRProjectionLayer`).

Dan: I just wish these explainers would start with "we want to provide a way to ..." instead of starting in with the technology. Is that a problem with the explainer explainer?

Alice: The explainer template does start with goals/use cases, so I don't think the issue is coming from there.

Dan: The first paragraph of the "Examples of use cases" section should be at the top of the document. 

Alice: Could add an extra sentence in the explainer template to emphasise that use cases/user needs are first because they are critical context for the rest of the document.

Alice: let's discuss more later

Dan: let's pick it up in the plenary

### Incorporate extensible-web.md into the design principles doc? https://github.com/w3ctag/design-principles/issues/182

Alice: What is extensible-web.md? Where does it live?

Dan: Is it the Extensible Web Manifesto?

Dan: [rummages around in Github] [it's here](https://github.com/w3ctag/design-principles/blob/master/extensible-web.md)

Alice: I think this is subsumned by the discussion around [high level vs low level APIs...](https://github.com/w3ctag/design-principles/issues/117) and [sparations of concerns](https://github.com/w3ctag/design-principles/issues/169)

... Maybe those discussions should be guided by the original [extensible web proposal](https://github.com/extensibleweb/manifesto)?

Alice: not sure I totally agree with the wording in this doc... 

Dan: maybe we should propose close based on what you've just said and the fact that we've moved on... 

...extensible.md is a kind of artefact... probably should just be cleaned up (removed) or a placeholder put in its place to refer people back to the design principles?


Dan: so yes let's discuss in plenary...

### "Don't Enable Dark Patterns" Principle? https://github.com/w3ctag/design-principles/issues/196

Alice: Feel each dark pattern has a unique set of mitigations...

Dan: The things on the wikipedia page are UX patterns.

... Where this overlaps with the work we do on API design largely has to do with permission prompts, and that kind of thing.

... related to safe-to-browse

Alice: quite a few design principles in this sphere...  Safe to visit, trusted UI should be trustworthy... ask user for permission where appropriate... 

Dan : we could say "thank you, we're already doing it." 

Alice: we could say "these are the principles we have that are in this area - i think mentioning dark patterns is too vague / not actionable.. 

Dan: this was originally filed on ethical web principles...

Alice: what is the purpose of that document? Who is it for?

Dan: can refer to in design principles, can tackle topics like the tensions between moving fast and keeping to the principles of the web, it's a decision making tool, but is also for outside audiences to make clear why we make certain decisions. X is here because it reinforces this ethical principle.

... Could go in the preamble to the EWP, I can talk to Hadley about this in 9A.


## 02b

Ken & Dan

### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481)

Ken: I will comment that it should reference [display override](https://github.com/w3c/manifest/pull/932) manifest file new feature...

[debate about PWAs and safety]

Dan: the point of PWAs is to have app-like experiences that have the same safety guarantees as the rest of the web - so if we're allowing developers to write arbitrary stuff into trusted UI then this can be a problem. It does not seem like there are sufficient mitigations.

Ken: one of the comments I gave earlier - when you install e.g. spotify - but if the title bar changes radically maybe it should warn the user.  What we're concerned about is that the web app impersonates a different web site after launch.

Dan: I'm also concerned that the web app could be installed under false pretsnses - where the user's trust is gamed by a web site or malicious advert for example, or via a URL they receive by text message or otherwise out of band...

Ken: the browser could check for a radical change....

Dan: i just feel like they need to think more about these abuse cases and come up with some mitigations. The privacy cobsiderartions section does not address this issue sufficiently.

[left some comments]

### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408)

Ken: this mostly makes sense for iframes... If I'm setting a sandbox to make sure all my images are compressed.. dealing with 3rd party content, don't show that image; but if it's "my" own image then maybe I want to just get a report. How am I going to know I have mistakes on my own content?

Ken: some admin sets the rules and other people control the content...  A CSP [reporting URL](https://developer.mozilla.org/en-US/docs/Web/API/Reporting_API)? They are having a reporting thing... There's a report-to-endpoint.  Just wasbn't n the explainer.  I think the explainer should mention the reporting as that seems to be a big deal.

Ken: left a message - maybe ask what is the additional wide review?

### [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536)

Ken: this is basically done... 

Dan: based on the dicussion in the thread I think we should close in the "summary" session.

### [Best practices for feature detection of DOM API](https://github.com/w3ctag/design-principles/issues/137)

Dan: let's close it in the summary.

## 03b

Peter, Yves, Dan

### [trust tokens](https://github.com/w3ctag/design-reviews/issues/414)

Yves: Venue is WICG -- was transfered there - 1 year...

Dan: any recent developments on this one?

Dan: [isssue from 7 days ago](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-692814080)...

Peter: re CAPTCHA - on-device trust tokens could be a good replacement for them... particulary on devices... People do automated form submission - browser knows if it's a human. Input type=captcha -> browser could have a token it could fill in there to prove it's not a bot. We could make captchas go away.

Dan: I'm sure the web users across the world would rejoice.

Yves: 1st party tracking.... if we replace capcha with a 3rd party then we introduce tracking on the same level as capchas.

Dan: shipping anywhere?

Peter: Chrome is doing some experiments.  Based on something cloudflare is doing in the user space. There are concerns about is the crypto good enough.   Going through IETF review...  

... explainer does talk about user tracking ... 

Dan: the mitigation [described](https://github.com/WICG/trust-token-api#first-party-tracking-potential) about first party tracking seems a bit hand-wavey.

Peter: because of the crypto it can't tell who you are just that you did authenticate once. The issue was - every time you go back to the issuer you are telling them who you visited. That is solvable - I proposed a solution to that.

Dan: so it assumes you trust your trust token issuer...  That ignores the possibility that you may have no choice over a trust token issuer or be compelled in some way to use a specific issuer.  Can we open an issue today?

Peter: I'll open an issue for them.

Dan: Could we also ask them for a kind of current status of how their experiment is going with this?

### [Cross-origin opener policy reporting API](https://github.com/w3ctag/design-reviews/issues/527)

Yves: we asked for the reason behind ... and it's to avoid complexity putting everything into one header.

Peter: a separate report-only header would allow you to enforce on policy and test another...

Yves: we can close it? Their reply made sense.

Peter: Yes - fine closing this.

[we'll close in the summary]

### [Best Practices for Registries (including that they should be machine readable)](https://github.com/w3ctag/design-principles/issues/68)

Yves: it's good to have an indication of how it's encoded and that it's machine-readable.  Apart from that...  not our goal to define what a registry is in general.

Dan: Agreed.

Peter: to Anne's point, in WhatWG you can put the registry right in the spec - fine for whatwg, but doesn't work for other types of spec. Some use Wikis some use text files... 

Dan: there was a long discussion about evergreen, everblue, etc... but registries weren't really discussed specifically.

Dan: I think that we may want to just stop short of telling people what file format to use for registries as long as it's machine readable. 

Yves: and the spec should have a description of what the structure is.

Peter: I think the format is irrelant if we don't agree on how to make a registry.

Yves: IANA is a centralized place for lots of registries that are mostly text. Many people would not want that as they want to control their own registry. The admin burden of having a centralized registry is not really worth it.

Peter: registry registry - where you can find all the registries?  I usually end up in wikipedia...

Yves: some markup in the spec to define that this is a registry...

Peter: microsyntax ... could be useful.  If w3c could maintain a list of where all these registries are ... one page I could go to in w3c.org to  find the registies...

Yves: crawl all w3c specs and then have a page that points to the specifications ...

Peter: sometimes the registry might be in a json file or text file in some github repo...  The microsyntax could say "the data is right here" or "the data is at this URL"

Peter: a convention using a class...

Dan: Would that satisfy the Living Standards proponents?

Peter: they could make their specs up as registries and we could discover them... 

Dan: [left a comment](https://github.com/w3ctag/design-principles/issues/68#issuecomment-696788016).

## 04b (Kenneth and Tess)

### [Web page settings to save battery](https://github.com/w3ctag/design-reviews/issues/546)

Kenneth: Was surprised to see this is a meta tag opt-in

Tess: Yeah, if user agent's are going to throttle sites that are taking too much battery, they're going to do it regardless of the site opting-in.

Kenneth: If it opts in the site could be informed of the throttling so it could help

Tess: the site is just as likely to make things worse when it gets that signal

Kenneth: [Unminited example re: media site and dropping frame] I really don't understand these use cases to be honest.

Kenneth's comment:

I don't understand the video conferensing use-cases. If I operate such a service and want to save battery etc, I would lower resolution and frame rate for instance to 15 fps instead of 30. I really don't want the browser to throttle me so that I loose frames which can result in a terrible user experience.

> If a site has some javascript tasks that might run long but do not directly impact UX, it's ok to run those tasks slower.

But this is a global thing so it would affect all tasks. It feels like the postTask scheduling proposal might fit this use-cases better.

### [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482)

Kenneth: You left a comment and May and they haven't replied yet. Still marked as `pending external feedback`.

Tess: pinged the OP

### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532)

Skipped due to time constraints / meeting conflict.

### [Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/544)

Skipped due to time constraints / meeting conflict.


## 05b (Rossen and David)

### [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72)

Rossen: This looks like one of the issues that would be great to try and close while you're here.

David: So this issues links to [#489](https://github.com/w3ctag/design-reviews/issues/489) and was held open in hope for me to write a bit more tests to identify what's consistent and what isn't from the html spec POV. For example, I wrote [one test](https://wpt.fyi/results/html/webappapis/update-rendering/child-document-raf-order.html) and it fails in all browsers. 

... My idea was to write few more of these and then identify changes that could be necessary to the specs.

... Also, there is an issue we opened with the CSSWG ([#5115](https://github.com/w3c/csswg-drafts/issues/5115)) about batching and flushing layout as part of the pipeline.

Rossen: What would it take to close this issue now?

David: Right, the main remaining question is - what's there for the TAG to do? There isn't interop but how can We fix it from TAG?  Close now, or leave open to remind us to do work *outside* of breakouts?

Rossen: I vote to close it now.

*closed*


### [VisibilityStateEntry](https://github.com/w3ctag/design-reviews/issues/534)

*reads explainer*

Rossen: I'm not convinced by the explainer.

David: I think the use case seems pretty reasonable to me.

Rossen: OK, maybe more convinced now.

Rossen: Did you see [Ryosuke's point](https://github.com/w3c/performance-timeline/issues/105#issuecomment-671681173), though?  The [comment after it](https://github.com/w3c/performance-timeline/issues/105#issuecomment-686767224) from Nicolás makes me wonder if this will be rethought again.


## 06b (Sangwhan & Alice)

### [Screen Wake Lock API](https://github.com/w3ctag/design-reviews/issues/543)

Sangwhan: Been wondering if we should gate battery-hungry APIs behind permissions so that users can reject if they're low on battery.

... actually, this one actually is gated on a permission. So I'm happy with this.

Alice: Same, I might leave a comment asking them to explain why it takes a string - I can guess the answer though, to do with future-proofing.

### [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156)

Alice: I read this as suggesting writing guidance for spec authors on adding information/suggestions to specs about how to expose information to developer tooling.

> One example is the Web Animations spec. Right from the starts, it lists use cases including an "Animation debugging" one.

> The spec could suggest UAs to surface some of this data to web authors. In particular the flex layout algorithm could be defined in a more transparent way whereby each flex item gets augmented with data about its content size, its final size, the amount of space it grew or shrunk by, etc.

> But that doesn't mean we shouldn't try to make technology at least a little bit easier to adopt at first by asking UAs to implement more than just the ability to view the code.

> I think a lot of it could actually be more advanced warnings in browser consoles.

... actionable advice? Potentially goes back to priority of constituencies, including the needs of authors as user needs, for example debugging cases.

... you (Sangwhan) earlier suggested that meaningful error messages would be a good principle.

... Could go in priority of constituencies section, after the note about documenting user needs.

Sangwhan: Specific negative example for error messages is `fetch()` - if you send a fetch request somewhere where it's not meant to go, you get this "CORS preflight error" which is very opaque.

Alice: Could add an extra section into API Design Across Languages as well, for debuggability.

... Firstly, specifying the algorithm and all the intermediate data clearly enough that debuggers can consistently retrieve the intermediate data

... Secondly, some text around error messages... where is that CORS error message specified, for fetch?

https://fetch.spec.whatwg.org/#concept-network-error

Sangwhan: Error messages aren't defined in spec. They define an exception type, e.g. DOMException. They don't say anything about what the error message should be.

Alice: Rust and clang compiler have good error messages... are those specified in some way? Could we see what strategy they use? 

... Rust is not formally specified. oh.

Sangwhan: C++ is, but not the error messages.

Alice: At some point they fixed the "undefined is not a function" thing... how did that happen?

... Oh, it was fixed in V8 specifically.

Sangwhan: We don't have an inspector/debugger "mode" like private browsing, in specs. It's very much implementer specific.

Alice: So perhaps the best we can do is advise including author needs (debugging) as user needs. I'm not sure we are able to write general advice on how to write a spec which facilitates debuggability?

Sangwhan: Some text might be something like "Make error messages meaningful. Errors should not only define the problem that is happening, but ideally a suggestion to the author on how to resolve it." 

Alice: To what extent is that under the control of the spec author?

... an adjacent issue is that sometimes the salient information involves private user information, e.g. visited links, so it's not always advisable to follow the example of the Web Animations API and expose state directly to web APIs.

... Thinking specifically of computed accessibility tree information here.

Sangwhan: Could expose sensitive information in debugger mode, but we don't have a formal definition for that. That could be a definition that specs could add. 

Alice: Right: I want the computed accessibility API as a debugger-only API. Well, also tests.

Sangwhan: well, debug/Web Driver maybe.

Alice: I think when Web Driver accesses JS APIs in the page, it's only regular Web APIs.

Sangwhan: Hm, I thought they had some extra APIs.

Alice: I'm more than happy to draft a change to priority of constituencies...

Sangwhan: I could try to write something up for the API Design Across Languages principle, but without a concept of a debugging mode, it might not make any sense.

... it's hard to make an actionable advice for spec authors here. We can write something, but it's not clear that it would actually change how specs get written.

Alice: Where might a "debugging mode" live, spec-wise?

Sangwhan: I don't think "private browsing" is defined normatively.

Alice: The OP says

> The spec could suggest UAs to surface some of this data to web authors. In particular the flex layout algorithm could be defined in a more transparent way whereby each flex item gets augmented with data about its content size, its final size, the amount of space it grew or shrunk by, etc.

... so that would be normatively exposing debugging information in all contexts.

Sangwhan: I don't think that's a good idea.

Alice: I'm inclined to agree, since it's a lot of extra data to expose which might be expensive to if there are optimised paths which bypass some steps. Similar logic applies to computed accessibility information.

... Could add a comment in to the writing good specifications section noting that well-defined specs are also amenable to exposing to debugging APIs.

Maybe let's follow up at another time to work through landing the changes to the writing good specifications section.

### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39)

Punted.

## 08b

Sangwhan & Yves

### [Transferable Stream spec](https://github.com/w3ctag/design-reviews/issues/551)

One concern is that the overrides for the methods in readable/writeable streams could be confusing initially, but users will most likely adapt to it after some initial confusion - so not an issue that should block progress, but maybe something to think about.

Overall, seems good, so we ropose closing it.

### [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478)

Discussion bout deep-linking into mini-app, with [Universal Links](https://developer.apple.com/ios/universal-links/) for IOS and [App Links](https://developer.android.com/training/app-links) for Android, the use case can be solved and keep the concepts of origin (and secure context).

The other use case was efficient dispatch to mini-app runtime, which can be achieved either by a media type, a hint on a html link...

## 09b (Kenneth & Tess)

### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512)

Kenneth pinged the OP. (We were waiting on their Digital Goods review, which hasn't come in.)

### [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494)

Tess: [recap]

Tess: It's basically just the TAG pushing for streaming on this. My understanding is that all of the implementers (not just the OP) prefer the non-streaming design.

[Kenneth comments on issue]

### [Multi-screen Window Placement features](https://github.com/w3ctag/design-reviews/issues/522)

Closed by OP.

### [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111)

We've been waiting on external feedbsck for a couple weeks. Pinging again.

### [Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/544)

Tess: I'm confused that this seems to be a new payment method. Is the site supposed to do two payment requests, the first with the real payment method, and the second with this new thing? Does that mean the user will see two sheets, and the user needs two user guestures?

> If no payment instrument specified by credentialIds is available or if the user failed to authenticate, the desired long-term solution is for the user agent to open fallbackUrl inside the Secure Modal Window

Kenneth: that's weird

Tess: Yeah, that's a non-starter. e.g. Safari's Apple Pay sheet does not display web content.

Tess to more closely read the explainer & to comment on the issue

### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532)

Tess: Some of these names seem like a really bad fit for the web, e.g. Table instead of FunctionTable

Kenneth: ElementType, that's even worse than Table

Tess: There's also something in the Naming section of our design principles about not doing this

Tess: no, wait, that [PR hasn't landed](https://github.com/w3ctag/design-principles/pull/217)

Tess: We should land that PR and then cite it in this comment.

## 10b (Hadley, Peter, Rossen and Yves)

### [jxl Content-Encoding](https://github.com/w3ctag/design-reviews/issues/541)

Discussed between Yves and Peter, sought clarification of content-encoding behavior in the wild. Clarifying if a JPEG is transmitted with this encoding, what is expected to be received, JPEG or JPEG XL.  

We agreed this might be better served as a content type rather than a content encoding, but we're OK with this approach.

If anything it seems to surface other ways in which content encoding is broken in the wild, but this doesn't make it worse.

### [Review Request - Decentralized Identifiers (DIDs) v1.0](https://github.com/w3ctag/design-reviews/issues/556)

Hadley: The last comment of the design review jumps as quite interesting. (reads comment)

Rossen: What makes the decentralized oracles are kept decentralized? 

Hadley: Referrs to the example of id issued by an university and vehicle assembly.
... The new use cases are substentially better than the ones we've seen before. In example 2.7 what jumps at me is that from a tax perspective there are times that the payer (employer) pays the tax and sometimes the payee (employee). This will require identification of the payee so that the party collecting tax can validate if they are legally able to be employed etc. and how much tax they have.

Rossen: Great, so what should we do with the review itself?

Hadley: We should look into the details more closely for any red flags and try to get back to them before TPAC.

Rossen: SGTM. I'll update the issue accordingly.

## 11b (Alice and Rossen)

### [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511)

Discussion on whether hidden-matchable nodes are included in the accessibility tree

- We had recalled that they would be, but dug up https://github.com/WICG/display-locking/issues/102#issuecomment-577482562 which suggests we came to the opposite conclusion.
- This has the downside that the AT find functionality *may* not work, but that seems preferable to the AT crashing because the page has too much content :(
- Narrator delegates find back to the browser already via UIAutomation API.

Alice: Looking at `content-visibility: hidden-matchable` and `beforematch`, we should encaurage the author to combine the two and continue the review there.

---

> After thinking about it some more, I agree with these considerations: I think that we should combine the proposals for content-visibility:hidden-matchable and the beforematch event. Should I edit the title and description of this issue? Here is the explainer for hidden-matchable.

Yeah, it seems like these two APIs really form one conceptual API together.

It would make sense to combine the explainers as well, since one doesn't really work without the other. That combined explainer could use the Wikipedia mobile page example as an end to end example illustrating how to use the two APIs in conjunction to create a good user experience.

> To talk about a specific example, imagine a mobile wikipedia page with collapsed sections. Suppose you find some word, foo, in a collapsed section. This section would have to be revealed in some way. If the user then dismisses the find-in-page dialog, or continues onto the next match, then this section should remain open. However, either the browser makes this state of being expanded sticky (meaning that the script can’t collapse the section anymore), or the section collapses automatically when there is no longer a match (which is not desired behavior). This case can be addressed by firing a beforematch event and letting script design on the correct course of action.

This is a great example. Are there any other kinds of interactions you had in mind while designing these APIs?

To flesh this out a little more, you might add some example code like:

```js
<h2>Cultural references</h2>
<section class="locked">
Octopus ...
</section>
```

So what I'm interested in here is the full flow, from loading the page, to matching "Octopus", to the section being closed again. What is the goal state here?

I'm guessing it's something like:

1. User loads the page. All subsections including "Cultural references" are hidden, with only the headings visible (similar to a `<details>` element).
2. User searches for "Octopus"
3. The `<section>` contents is made visible to the user
4. ???
5. The `<section>` contents is hidden from the user again.

Is that the flow you're designing for?

If so: what happens at step 4? How does the `beforematch` event enable it?

Also: at step 3, is it implied that the author must write code to remove the `hidden-matchable` style, by handling the `beforematch` event?

---

Rossen: This is reminding me of (positive) tabindex values, where you have to manage it everywhere. Every time you change your UI logic you have to go change all your code everywhere.

### [Web Share API review](https://github.com/w3ctag/design-reviews/issues/554)

Rossen: This is a duplicate with 09c where Peter and myself already did review the proposal and opened a number of issues to the authors.


## 12b (David and Rossen)

### [give advice on read-only lists](https://github.com/w3ctag/design-principles/issues/50)

David gets stuck in a rathole about what "passed by value" precisely means here and files https://github.com/heycam/webidl/issues/926 .

Lots of reading linked things; linked one from the issue.

Rossen adds [comment](https://github.com/w3ctag/design-principles/issues/50#issuecomment-698045074) to issue.

## 14b

Hadley & Dan

Landed [Tess's PR](https://github.com/w3ctag/ethical-web-principles/pull/29) to ethics doc.

### Ideas for additional references:

Hadley for "one web" we could reference the evergreen finding - in response to subsetting the web.  Might need some additiomnal text.  

Dan: looking at https://www.internetsociety.org/policybriefs/

... e.g. https://www.internetsociety.org/policybriefs/privacy/ for privacy & security - and freedom of expression

## 15b (None)

## 16b (Rossen & Tess)

### [WebRTC playoutDelayHint](https://github.com/w3ctag/design-reviews/issues/441)

Tess: You, Yves, and I looked at this in Wellington, and we only had one quibble, which they've adequately addressed. Propose close?

Rossen: Let's just close it.

Tess: Okay.

### [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549)

Rossen: The thing that stands out to me (and this is probably not new issue) is that neither the security and privacy questionare is completed nor there is an explanation of why this isn't making fingerprinting worse. 
... There is a linked issue that proposes we start sending media feature preferences such as prefers-reduced-motion as client hitns... how is that making fingerprinting people with vestibular issues better?

Tess: Yes, though arguably this is already a concern with the underlying CH, this proposal does seem to make it worse.

Rossen: So were CH reviewed and approved already by TAG?

Tess: #320 was about that, but that got replaced by #467 which was closed without resolution.

### [TAG review request: PWAs as URL Handlers](https://github.com/w3ctag/design-reviews/issues/552)

Ran out of time before we got to this.


## 17b (David & Sangwhan)

### [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304)

Sangwhan will ping [dom](https://www.w3.org/People/Dom/) to find out what the status of this is (and how worried we should be about consent to communicate, etc., issues)

### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389)

Sangwhan: Yves and I discussed this at our last face-to-face.  I think for an early review we're probably OK with this.  I think we're at a point we can propose closing.  I think they're prototyping in incubation.  Maybe look after experimented a little?  Maybe they can reopen once they have a slightly more concrete proposal.  I think the feature is fine.

(sangwhan drafts closing comment)

### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341)

Looked over the current state of things and found some relevant links; didn't make a whole lot of progress.  Perhaps depends on the more general issues (linked) about the different tools used for restrictions.

### [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55)

Didn't get to this one.

## 18b (Alice & Tess)

### [Readability edits: Cascading Style Sheets section](https://github.com/w3ctag/design-principles/pull/221)

[Tess read the PR and approved it]

Tess: Can't merge yet, looks like there are still some changes to be made from Dan's review

[We looked at Dan's review comments and Alice made some edits.]

### [Readability edits: JavaScript API Surface Concerns section](https://github.com/w3ctag/design-principles/pull/228)

[Tess read the PR and approved it]