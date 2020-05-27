# W3C TAG Virtual F2F
## Day 1 - 26 May 2020

Agenda: https://github.com/w3ctag/meetings/blob/gh-pages/2020/05-distributed/README.md

## Slot C
### Breakouts 1 **06:30 - 07:30 UTC**

#### Breakout 1a - Ken & Sangwhan
  * <a href="https://github.com/w3ctag/design-reviews/issues/431">Serial API</a>

Sangwhan: Has anything significant happened since we last looked at this?

Kenneth: Some stuff happened on a private branch.

Sangwhan: Aside from that? Guess this isn't a super huge priority...

Kenneth: Should we ping and wait?

Sangwhan: Yes

##### <a href="https://github.com/w3ctag/design-reviews/issues/498">VirtualKeyboard API - show/hide policy</a>

Kenneth: This is the controversial feature.

Sangwhan: How many of the vendors are in disagreement?

Kenneth: AFAIK, just one.

Sangwhan: It seems like we haven't heard about the position in the last comment.

Kenneth: Think the revised proposal without the inputmode=none deprecation seems sane

Sangwhan: Likewise, should probably ask for clarification on why they object

##### <a href="https://github.com/w3ctag/design-reviews/issues/513">CSS advanced attr() function</a>

Kenneth: Why is this assigned to us?

Sangwhan: *shrugs*

Kenneth: No assignee, probably needs triage

Sangwhan: Seems like this is an expansion of an existing feature.

Kenneth: Not particularly my field of expertise, probably need someone with more CSS knowledge

Sangwhan: Seconded

##### <a href="https://github.com/w3ctag/design-principles/issues/116">How should the toJSON method be used?</a>
  
Kenneth: This one looks like a long discussion.

Sangwhan: Correct.

Kenneth: It's complex, there are a bunch of existing constraints

Sangwhan: We could try to draft up something for the design principles and solicit feedback, otherwise I don't see this 
going anywhere.

Kenneth: The problem is that JSON is lossy like you write a bigint and parsing gives you a number, same with Date, where you get a string back. There is a proposal that kind of allows you to check the source and get it as string instead and that way deserialize it yourself, but that requires everything to have a string representation which Map and Set don't today. I think this requires broader discussion in the TAG.

Sangwhan: If there is a toJSON(), shouldn't there also be a fromJSON() - so given prior knowledge about the JSON coming in one has a shorthand to reconstruct it? Seens these patterns elsewhere

Kenneth: Not sure if that would work

Sangwhan: Not for every case, definitely not - would only work for objects that only use readily exposed primitives

#### Breakout 1b - Alice & Dan

##### <a href="https://github.com/w3ctag/design-reviews/issues/438">MathML Core</a>
      
Alice: comparing the list of elements in the spec with those in the explainer... 3 elements in the spec that aren't in the xplainer and one element in the explainer that's not in the spec... menclose [?] is not in the spec. 

 more in spec that aren't in explainer: `<maction>`, `<mprescripts>` and `<none>`. `<none>` seems especially intriguing. 
 
Dan: explainer out of sync with spec?

Alice: seems likely -  may not be a big deal

Alice: integration with web platform seems to be most interesting for us...  [CSS Styling](https://mathml-refresh.github.io/mathml-core/#css-styling) - display content equiv to display none..  Event handlers - html foreign element - a special mathml linkable elemnt interface... Lots of open issues still - 

Dan: how many of these open issues are marked or commented as being part of a "v2" (e.g. [#138](https://github.com/mathml-refresh/mathml/issues/138))?

Alice: [visual formatting model](https://mathml-refresh.github.io/mathml-core/#visual-formatting-model)... extremely thorough... 

... So what should our focus be for this review?

Dan: There are a bunch of open issues, nothing that seems like a red flag... our focus is probably the [Integration in the Web Platform](https://mathml-refresh.github.io/mathml-core/#integration-in-the-web-platform) section.

... What signals do we have about this spec? Seems to be actively being worked on. Good signals about implementations. I like how they've put engine annotations in here, for every subsection.

Alice: Good to see a section on [Focus](https://mathml-refresh.github.io/mathml-core/#focus) - CSS extenstions as well...  Text treansforms have "math" and then an existing thing... 

[some discussion on implementation annotation and whether these are a signal...]

Dan: So for progressing this issue, could we say we're re-reviewing it and our questions are

... are there any blocking issues?
... are any of the features at risk?

... more spec logistics than architectural issues.

... could focus in on HTML integration issues... some are marked as V2, does that mean you think you're ready to go for V1?

Alice: could be worth noting - elements not included in the explainer... maybe just as a side note.

... I can comment on the open issues in the integration section.

Dan: Maybe we should propose close, just make the note.
      
##### <a href="https://github.com/w3ctag/design-reviews/issues/470">WebXR DOM Overlay Module</a>

Alice: Accessibility comment in second para is kind of tantalising and confusing...
  
Dan: Difficult to understand why emphasis on AR content. Would like an image explaining the difference between HTML content in the scene, and the HTML overlay

Alice: Imagine something is printed on your glasses... no matter where you look, it'll be there, because it's not *in* the scene.

Dan: It's like the Terminator's stats coming up over the scene

Alice: There is mention of fullscreen - "Fully exiting fullscreen mode also ends the immersive-ar session. Conversely, ending the immersive-ar session automatically fully exits fullscreen mode to ensure that the user doesn’t end up in an indeterminate state." How would someone exit one without exiting the other, in terms of a user gesture? Particularly since, earlier, "(Using the Fullscreen API to change the fullscreen view is blocked by the UA.)".

##### <a href="https://github.com/w3ctag/design-reviews/issues/479">WebXR Anchors Module</a>

(bumped)

#### Breakout 1c - *unused*

### Breakouts 2 **07:45 - 08:45 UTC**

#### Breakout 2a - Dan & Ken
##### <a href="https://github.com/w3ctag/design-reviews/issues/436">Get Installed Related Apps</a>
      
We have left a coment mentioning the related work going on by Mozilla... 
      
##### <a href="https://github.com/w3ctag/design-reviews/issues/469">Cookie Store API </a>
      
Ken: I believe they are about to ship this...  
      
Ken wrote some very explicit API feedback.
      
Dan wrote a comment regarding privacy factors....
      
[reviewing state of the spec and of the issue...]
      
##### <a href="https://github.com/w3ctag/design-principles/issues/148">Proliferation of manifests at W3C</a>

#### Breakout 2b - Yves & Sangwhan
#### <a href="https://github.com/w3ctag/design-reviews/issues/389">WebTransport</a>
      
Yves: There seems to be some recent discussion we did not follow up on.

Sangwhan: So one of the easier issues is about naming - one is about casing of HTTP and the other is about adding a version in the API naming, I think both of the remarks from Anne make sense

Yves: The versioning part might be a bit more complicated, since different versions may have different capabilities, hence different APIs

Sangwhan: The other discussion was around preventing port scanning

Yves: There was a recent article about eBay doing this

Sangwhan: Martin's permission-free proposal seems to make sense

Yves: I think we don't have a strong opinion on what direction it takes for the mitigation, as long as it is mitigated

##### <a href="https://github.com/w3ctag/design-reviews/issues/478">MiniApp URI Scheme</a>
Yves: Nothing happened since late March.

Sangwhan: Will write a ping.

Yves: Will ask Xiaoqian if she knows what is going on

#### Breakout 2c - Alice
##### <a href="https://github.com/w3ctag/design-principles/issues/177">Re-think information architecture for the design principles doc</a>#
### Break **08:45 - 09:00 UTC**
### Readouts/Wrap-up **09:00 - 09:30 UTC**
  
Dan, Sangwhan, Ken, Alice, Yves

Dan: we made a design principles PR on the manifest file topic.

Dan: we didn't get to WebXR anchors module... [rescheduling to 13a]

Sangwhan: we looked at serial APi which has not moved much.  We were assigned to css attributes issue... no idea why ... design principles... toJSON --- I will write something and send a PR to design principles .. for comment. 

Alice: I had in my list to rething AI of design principles doc..... Have been reading it... At the least I'd like to take an editing pass.

Sangwhan: let's coordinate on that - collaborative session.  [scheduled for 8b]

Alice: [on mathml core] I a have an action item on ut.. I printed out the spec. Specific section on integration with web platform and a section on CSS extensions. Spec is thorough and actively worked on - lots of links to issues. Will comment to ask which issues are blocking.

Dan: and we should propose-close

Alice: I will do that... 

Dan: webxr dom overlay module...  

Alice: filed an issue on the accessibility issue - is it in or out of scope?   Explainer hard to follow.  Filed an issue on event bubbling...

## Slot A
### Breakouts 3 **14:30 - 15:30 UTC**
#### Breakout 3a - Ken & Tess
##### <a href="https://github.com/w3ctag/design-reviews/issues/397">Same-Origin iframe document-access limiting attribute</a>

Tess: The discussion in [dtapuska/documentaccess#2](https://github.com/dtapuska/documentaccess/issues/2) is very interesting, and there are a couple of still-open issues that follow from it naturally: [dtapuska/documentaccess#4](https://github.com/dtapuska/documentaccess/issues/4) [dtapuska/documentaccess#6](https://github.com/dtapuska/documentaccess/issues/6).

Tess: I'm broadly sympathetic to Boris'/Anne's concerns here. What does it accomplish to deny direct script access when you can just send script source via a side-channel, eval, and send the result back via the same side-channel?

Ken: It's not supposed to be a security tightening knob, just a performance one (to let the pages be in different threads). But developers won't understand that.

Tess: right, they'll think this is about security. And it's also concerning (like Anne talks about in #6) that it doesn't match feature/document policy. Cutting across things in a bespoke manner like this is a recipe for disaster.

Ken: This is all already so messy and complicated on the platform, developers just won't get this right.

Tess: Yeah.

[Ken summarized our discussion in a comment on the issue](https://github.com/w3ctag/design-reviews/issues/397#issuecomment-634075283)

##### <a href="https://github.com/w3ctag/design-reviews/issues/482">URL Protocol Handler Registration for PWAs</a>

Tess: we talked about this on a weekly breakout call recently, and my basic concern (partially written up by dbaron in [mozilla/standards-positions#340 (comment)](https://github.com/mozilla/standards-positions/issues/340#issuecomment-631797523)) is that this new manifest feature and the existing `registerProtocolHandler()` should both be directly specced on top of a common model, like how the Fetch spec unified the model for loading subresources. That way we could all trust that these things wouldn't get out-of-sync, and that they could have consistent UIs, permissions, etc.

Ken: where should it be specced?

Tess: the manifest feature in the manifest spec, `registerProtocolHandler()` in HTML, and the underlying model somewhere (probably HTML), I don't think I have a strong preference.

[Tess commented on GitHub](https://github.com/w3ctag/design-reviews/issues/482#issuecomment-634082331)

##### <a href="https://github.com/w3ctag/design-reviews/issues/509">Navigation to Unsigned Web Bundles (Web Packaging)</a>

Tess: followed some links to [WICG/webpackage#560
](https://github.com/WICG/webpackage/pull/560) and this is interesting. With AMP you see these fake address bars in the content, which attempt to trick users into believing the URL to the AMP document is actually something else. Sometimes they even auto-scroll the page so that the browsers's address bar gets hidden. It's pretty gross. So they really want to avoid that same problem here with web packages. But it seems to me that you can't escape it: displaying the publisher hostname in the address bar is deceptive the same way the fake AMP address bars are (it puts the deception directly into browser chrome), and displaying the distributor hostname in the address bar encourages content to do the same icky stuff AMP content does today. This is just the inherent complexity of having `publisher != distributor`.

Ken: Why have authoritative responses at all here? What are the use cases?

Tess and Ken both left comments on GitHub: [Tess' comment](https://github.com/w3ctag/design-reviews/issues/509#issuecomment-634098027), [Ken's comment](https://github.com/w3ctag/design-reviews/issues/509#issuecomment-634098962)

#### Breakout 3b - David & Dan

##### <a href="https://github.com/w3ctag/design-reviews/issues/337">Contact API</a>

Dan: no updates since 6 march... 

David: "intent to ship" for an addition (address/icon support) is listed on blink dev... so probably hasn't changed much recently since it shipped a while ago.

Dan: [left a comment](https://github.com/w3ctag/design-reviews/issues/337#issuecomment-634072745) asking the editors for status...

David: leaving an additional comment.

Dan: marked proposed closed - we are not entirely happy especially if there are no other implementations in the works and the spec is not headed out of WICG in some way...

##### <a href="https://github.com/w3ctag/design-reviews/issues/461">Web NFC</a>

David: some pretty fundamental disagreements with Zoltan - about what the security constraints of web APIs should be. 

Dan: don't you need to push a button on a yubikey to make it broadcast a OTP?

David: are there other cases in NDEF usess -- and how do you explain to a user what it is they're giving permission for, given that?

Dan: this is one of those ones where I am slightly more sympathetic to the API developers - 

David: the other complex part is writing.

Dan: Agreed.  What if we recommended that they eliminiate writing - or keep witing behind some kind of flag or user permission - in order to limit the possible danger.

Dan: Case I expect to see the most is holding phone up to an NFC tag of some sort, e.g., conference badge.  Those don't involve writing.  

David: i don't know what kinds of NFC devices support writing NDEF tags...

Dan adds [a comment](https://github.com/w3ctag/design-reviews/issues/461#issuecomment-634089144) to the issue.

##### <a href="https://github.com/w3ctag/design-reviews/issues/462">WebXR Augmented Reality Module</a>
##### <a href="https://github.com/w3ctag/design-reviews/issues/467">Partial freezing of the User-Agent string</a>

Dan: Yoav posted on 20 April to chromium.org - has been [deferred to at least 2021](https://groups.google.com/a/chromium.org/forum/m/#!msg/blink-dev/-2JIRNMWJ7s/yHe4tQNLCgAJ).

David: but UA Client Hints is going forward...

Dan: so great - that would mean that we have more time to experiment with UA client hints before UA String is frozen or deprecated (in Chrome).  Can it be used in the same way and also provide 

David: some of this is about the distinction between active and passive finger printing... in client hints the site needs to send a request for it... That's a big advantage and one of the risks because you don't get it on first requests in some contexts... 

Dan: deprecation of UA string always felt premature to me because Client Hints wasn't tested and mature enough...

David: I'd agree.

Dan: so having more runway for client hints would seemd to make sense...

David: I'm not sure what makes client hints more widely adopted - it would need cross-browser support and support on the server end - getting to that level of adoption requires things being in client hints that people need. If UA String isn't deprcated than what could encourage people to make that leap?

Dan: good point.  Isn't it up to browsers that want to do this to try to show how this can be used in the wild?

David: everyone on Apache or NGINX is going to face additional problems...  

Dan adds [a comment](https://github.com/w3ctag/design-reviews/issues/467#issuecomment-634101437).

### Break **15:30 - 15:45 UTC**

### Breakout4 **15:45 - 16:45 UTC**

#### Breakout 4a - David & Tess

##### <a href="https://github.com/w3ctag/design-reviews/issues/369">IFrame Execution Pausing</a>

David adds comment about rename of Feature Policy to Permissions policy.

Tess: The issue I had been asked about before -- which isn't really related to this review -- is that when we freeze something, it's due to a resource constraint, and we *don't* want to run any javascript on the page at that point.  It's frozen because we don't want to run it now.

David: I could imagine wanting the page doing the freezing to want to do it either way.

Tess: yes, could make sense to send events for the scrolling into/out of view case.

Tess: Does the stuff about being rendered or not look right?  `display:none`, `opacity: 0`, 3-D transform that makes you orthogonal to the page.  Though `IntersectionObserver` wanted to handle that well so that things like ads can actually tell if they'r evisible.  Idea of being rendered might become complicate -- should we build other things on top of that?  And does it expose implementation details like when layout/style happen?

David: I'm not too worried about the last bit.

David: It seems like the "being rendered" definition here is `display:none`-like; that seems OK.

Tess: Given [w3ctag/design-reviews#369 (comment)](https://github.com/w3ctag/design-reviews/issues/369#issuecomment-634120677) I think we can stop here for now.

We added a new `Progress: blocked on dependency` label to capture cases like this (where one design review should wait for another to complete before proceding).

##### <a href="https://github.com/w3ctag/design-reviews/issues/407">More restrictive hasEnrolledInstrument() for autofill data</a>

(brief discussion)

David: This is a pretty small change; initially wasn't clear it required spec changes.

Tess: we should close as we proposed in March

[Closed](https://github.com/w3ctag/design-reviews/issues/407#issuecomment-634127042)

##### <a href="https://github.com/w3ctag/design-reviews/issues/489">review HTML event loop and how things fit into it</a>

David: I think one of the underlying issues here was HTML editors wanted CSS WG to define a bunch of things about batching and flushing.

Tess: In long term, we want HTML event loop to be cleanly specified, so it's obvious for spec authors of other specs how they plug into it, so they get interoperability.  IntersectionObserver was one case where maybe that was harder than it should have been.  Hoping we end up in a place where it's clear to people elsewhere how they plug in cleanly and get predictable behavior.  Given what you said, sounds like one issue is that lacking a definition for batching and flushing on CSS side, the ability of HTML editors to make that clean is limited.

David: I'd like to see this get to the point where most of the things that are meant for writes happen before most of the things that are meant for reads. e.g. rAF is meaant for writes, and IntersectionObserver is meant for reads, so rAF should be before IntersectionObserver.

...: But different people who read the current spec end up interpreting it in different ways, e.g. rniwa and myself read something differently and it wasn't super clear from the text who was right. I had always interpreted it as "this is where the default style layout flush happens" and rniwa had interpreted it as "this is where paint happens". (The spec assumes style layout is always up-to-date so doesn't explcitily have a flush concept.)

...: Maybe what we should do is file an issue on csswg-drafts to define when batching and flushing actually happen, so that HTML can hook into that directly, and these kinds of ambiguities could be eliminated.

...: what CSS spec would these issue even be filed on?

Tess: important thing is for us to file the issue.  Secondary importance to know what spec it would land in.

Tess: Just one issue, with a motivating description?

We looked to see if such an issue already exists, but we couldn't find one, so David filed [this issue](https://github.com/w3c/csswg-drafts/issues/5115) to capture this concern.

#### Breakout 4b - Peter & Rossen
##### <a href="https://github.com/w3ctag/design-reviews/issues/471">Securer Contexts</a>

Dan: bunch of replies from Mike West....

Rossen: is the overall summary of the more recent feedback - does it all have to do with added complexity / ergonomics...

Dan: yes.

Dan: I think he's responded well -

Peter: agree - we raised our concerns - he's dealing with it - 

[closed with comment](https://github.com/w3ctag/design-reviews/issues/471#issuecomment-634115543)

##### <a href="https://github.com/w3ctag/design-principles/issues/144">Harmonize permissions and similar mechanisms</a>

Rossen: Nick Doty pointed us to the 2018 workshop report 

Peter: orig concern I raised - permission and permission like things spreading out across APIs - should be a common pattern used everywhere... Something we can look for an encourage other people to fix... 

Dan: we could write up best pracice for requesting permission - and that could include info from the [2018 workshop report](https://www.w3.org/Privacy/permissions-ws-2018/report.html).

Peter: it's good info but that doesn't really talk about the API surface...

Dan: maybe we need a nother discussion 

Rossen: what's a good example out of the onces you listed?  Is the gesture delegation one a good example?  What would be great to see - along the lines of guidance - if we are going to have a permission guide - it would be great to enumerate the different layers of where web permissions surface - either API or User Ineraction..  I'm pretty sure that a lot of permissions get handled through policy - like a PWA should be able to handle permissions through policy - what is the idea here?  Recommend the mechanism by which capability discovery get hooked up and surface as a permission to the user?

Peter: we have the permissions API which seems to have not really taken off...  It would have covered most of my concern. I want access to the camera, so i request the media stream -there's no way to know if I have the permission ahead of time, etc... e.g. if that was previously denied I'd want to change my UI

Dan: The current state of permissions is kind of a mess. In the absense of good permissions it would be great to document something in the design principles doc that says, here are a set of guidelines. That would be much preferrable over trying to solve all that here and satisfy all issues. 

Dan: Feels like we should focus on the API surface ... We could say "in the absence of a unified permission API, here are some best practices to follow."

Peter:  yes - e.g. not every permission will have a dialog - but it's useful to know if something was revoked without having to know where that revocation came from...  

Dan: we could start noodling on some content for this.... [creates document](https://cryptpad.w3ctag.org/code/#/2/code/view/niOwectEny-NdqOrA994rPuAdr4B7J2N95G3NtaFcR8/)

Dan: Perhaps we should create a survey and gather feedback from developers - what works, what is discoverable or missing? Further, there isn't much about feature policy when it comes to permissions. There is a good [writeup by Andrew Betts on this](https://github.com/w3ctag/design-reviews/issues/159#issuecomment-297920860). 

Dan: What can we recommend in the absense of a unified permission API?

Peter: a design pattern or approach, but it will still be a mess.

Dan: another option is we could  adapt the [doc from Nick Doty](https://github.com/w3cping/adding-permissions/blob/master/README.md) as an elaboration of our current section 1.4.

Rossen: if I'm an engineer looking to add a capability that might need permission, i can't get an answer based on this...  It's a guidance from privacy & security pov - i like section 3 (considerations with sensors). But to Peter's point, if we are there to be proscriptive in our design principles, I don't know that this document does that.

Dan: I agree it's more high level a-la- html design principles  rather than API design guideance per se. We could put high level stuff in one place and specific recommendations in another...

Rossen: [we could also pull from] [APF's PhD thesis](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2012/EECS-2012-185.pdf).  

### Break **16:45 - 17:00 UTC**

### Readouts/Wrap-up **17:00 - 17:30 UTC**

Present: Rossen, Ken, Dan, Tess, David, Peter

Scribe: Dan

#### 3a readout

Tess: we wrote a comment on our design review ...  In 4a we looked at a different related issue.. We added a label : progress : blocked on dependency - easier to tell that it's waiting on another design review to finish.

... **URL protocol reg for PWAs**.. we said the same things... no unified underlying model

... **nav to unsigned web bundles**... we couldn't do it justice. We (the TAG) need to do some more here.  One thing htat's come up - what do you put in the address bar - there is an open issue on that discussion.  there's not a good option.  Distributor URL would be encouraging content to do fake address bars - if they put the publisher URL they would enshrine in trusted UI the "fake" address bar thing.  Also distinction between authoritative and non-authoritative ... 

Dan: What's the problem with showing the publisher URL again?  Is it that it's unsigned?

Tess: For signed, concern with displaying publisher URL, best articulated by Martin Thomson (Mozilla), about changing the origin model of the Web.  But in the unsigned case, it's lying.

Peter: why are unsigned bundles even a thing?

Tess: couple of compelling use cases - every browser has a way to save ... you could share an unsigned bundle... 

Dan: why unsigned

Tess: because the browser generated on the fly the bundle...

David: it's not different from making a PDF file and sharing that... Many PDF users want a thing that can be transfered as a single file rather than PDF's layout...  

Dan: If that's the case corp firewalls will block it -- could be full of untrustworthy javascript.

[dan argues vociferoulsy ...]

Tess: David identified 2 use cases for PDF: package, and pagination.  If you want the pagination, generate an EPUB from the webpage.  So they're trying to solve the other use case of just wanting the package and not pagination.  Could come back with "just use EPUB and turn off the paginated styling".  This design is a backformation -- they're trying to do the unsigned stuff by starting from the signed stuff.

Dan: Any mitigation around any of the security issues?  Like, scripts will not run?  Removing features?

Tess: Don't know.

Ken: Plan for sharing PWAs, but those would be signed bundles.

Dan: This doesn't sound like a good idea to me.

#### 3b readout

Dan: **Contacts API**.  Seems to have shipped.  But no hint of multiple implementations or moving out of WICG.  Want to say something about that.

Tess: I'm supportive of that concern.

(Dan and Tess discuss wording of Dan's comment in the issue)

Tess: Important to get other implementors on board -- that leads to compromises and changes to the proposal, which ideally is what we want to review in the end.  We don't want to say OK in a way that says it's fine to go ahead.

Dan posts [comment](https://github.com/w3ctag/design-reviews/issues/337#issuecomment-634163688).

Dan: **Web NFC**.  We wrote comment.  Zoltan wrote a reply, we need to read it.

Dan: Didn't get to **WebXR Augmented Reality**.

Dan: Proposed closing **partial freezing of the UA string**.  Could close now or wait until next week...let's wait.

#### 4a readout

Tess: **iframe execution pausing**.  This is blocked on one I mentioned earlier; we added label and moved on (after discussing a bit).

Tess: **payments: more restrictive hasEnrolledInstrument**; marked proposed close since march; we'd like to close it.

Dan: close it.

Tess: OK, I'll do that.

Tess: And looked at David's issue about **HTML Event Loop**.  Motivated by things that came up in `IntersectionObserver` Review.  Spec fiction that CSS style is always computed that's not true.  Has performance and timing implications.  We ended up filing an issue on the CSS Working Group, though not on aspecific spec, to specify when batching/flushing happen, so the HTML spec can hook into those definitions, and get towards interop.

#### 4b readout

Dan: We closed **securer contexts**.  Been open for ages, given feedback, happy withhow it was received.  Still concerned about complexity, and encouraged to bring to webappsec.

Dan: Also talked about **harmonize permissions and similar mechanisms**.  Noodled for a while.  Looked at Nick Doty's suggestion, document he wrote in PING.  Started noodling on a cryptpad that could become a PR to design-principles document.  We should say something bout this in design-principles.  We should talk about what API should look like when it requests permissions.  Mostly empty document with notes and scattered stuff in it but could become PR.

Tess: Yes, I saw Nick's document when he wrote it.  Happy to review a PR or help draft.

Dan: Challenge is figuring out what APIs represent best practice for API design itself.

Tess: `<input type=file>` is the gold standard. :-)

Tess: I'm happy to generate concrete examples of things that are good, and that do the best they can give other constraints.


### Slot B

### Breakouts 5 **22:30 - 23:30 UTC**

#### Breakout 5a - Alice & Tess

##### <a href="https://github.com/w3ctag/design-reviews/issues/494">Declarative Shadow DOM</a>

We each read through the latest revision of the explainer and commented on the design review with things we noticed:

* [Serialization of closed shadow trees](https://github.com/w3ctag/design-reviews/issues/494#issuecomment-634322115)
* [Multiple boolean content attributes v. a DOMTokenList](https://github.com/w3ctag/design-reviews/issues/494#issuecomment-634327314)
* [Timing of attachment and the Priority of Constituencies](https://github.com/w3ctag/design-reviews/issues/494#issuecomment-634330438)
* [idref to an existing template](https://github.com/w3ctag/design-reviews/issues/494#issuecomment-634333562)
* [please use doctoc](https://github.com/w3ctag/design-reviews/issues/494#issuecomment-634333993)

This took the full hour.

##### <a href="https://github.com/w3ctag/design-reviews/issues/392">Scroll To Text</a>

Ran out of time before we could look at this.

##### <a href="https://github.com/w3ctag/design-principles/issues/117">High level or low-level APIs?</a>

Ran out of time before we could look at this.

##### <a href="https://github.com/w3ctag/design-principles/issues/142">How do we balance concerns between interoperability and implementability?</a>

Ran out of time before we could look at this.

#### Breakout 5b - Peter & Rossen

##### <a href="https://github.com/w3ctag/design-principles/issues/romises">Guide</a>
Rossen: Had a chance to have an overview of the current draft. Having the benefit of a first-time reader I have some additional points apart from all open issues. 
[Section 2.2](https://www.w3.org/2001/tag/doc/promises-guide#one-time-events) reads much harder compared to the rest of the sub-sections in Section 2. Perhaps we should try and loosen the language a bit.

Rossen: Let's start by looking at issue 65 about recommending when Not to use Pomises.

##### <a href="https://github.com/w3ctag/promises-guide/issues/65">When not to use Promises</a>
Rossen: What was the motivation of the issue?

Peter: There was a pretty weird case of returning a Promise that never resolved. This was done originally and later designed away. This was the motivation to open the issue and add any missing examples of when Not to use Promisses.

Rossen: Agree. I can see how using Promise to make void functions async and complete the promise as undefined or something. I suppose one of the main points here is that under normal circumstances a promisse should always resolve. Further, it should be safe to chain promisses together and expect that the chain will resolve.

Peter: During the permissions workshop there were discussions about returning a promisse that will never resolve... Something to do with handingling permissions that could be neither resolved nor rejected. That meant a promisse that will never complete and that may be a poor design choice. 
The recommendation is that there must a path that the promise can always resolve successfully.

Rossen: Agreed. How about we create a new section and recommend that promises are not used if there is no clear path for completion under normal circumstances?

Peter: SGTM

##### <a href="https://github.com/w3ctag/promises-guide/issues/44">Are unresolved promises rejected prior to a window.unload event?</a>

Peter: It makes no sense to override the comments in the issue. There is pretty strong concensus that after an unload event there's not reason to go and reject all promises as no rejection-handling code will/should run. Not sure if there is any real reason or desire to change that.

Rossen: Wonder if this is already specified by now, given the issue was last updated 5 years ago.

Peter: Perhaps. It is pretty clear that the issue is asking a question and the answer is a pretty clear "no". The remaining question is - should we make that an explicit recommendation anywhere or not?
Since this came up and was answered, maybe we can just add a section or note that promises may not resolve in cases when the context is torn down or the document is unloaded or any other circumstance that renders the situation 'not-normal' from the POV of user code execution.

Rossen: Makes good sense. Where should we try and add this - design principles or promises?

Peter: Let's add it in Promise Guide under Section 4 as its own section.

##### <a href="https://github.com/w3ctag/promises-guide/issues/60">guidance on what error to specify is used when a promise is rejected</a>

Peter: The original question is about "What error to specify when you reject"?. This seems pretty clearly stated in section 4.1.2. Then the conversation goes about when to reject vs return with different value. It seems this is pretty well explained in 4.1.3. The main parralels here are - when would you chose to retun an error vs throw an exception from a syn API... and that seems described well in 4.1.3. Perhaps add one more sentence before 4.1.3. that explains:
"If you would've return an error value in case this was a sync function, then resolve the promise with the error value. If you would normally throw an exception in the same API, the go ahead and Reject the promise instead with the same exception."

#### Breakout 5c - David & Sangwhan

##### <a href="https://github.com/w3ctag/design-reviews/issues/433">WebCodecs</a>

[ discussion about @plinss's comment from April ]

DRAFT COMMENT:
> @cynthia and I are looking at this in a breakout at the TAG's virtual face-to-face.
> 
> We (the TAG) have looked at this a few times, and I think we're generally pretty happy with it.  The design looks appealingly simple -- which is either great (if it can stay simple in the end), or it's a sign that a bunch of things were missed in the design.  We're hoping it's the former.
> 
> [Peter's comment](https://github.com/w3ctag/design-reviews/issues/433#issuecomment-616863996) gets at one of the tricky issues with adding new fundamental APIs that other things are built on, when those other things already exist.  When that happens, there's generally a process of making the existing features, like `MediaRecorder`, work with the new fundamental API.  That doesn't need to happen all at once, but it does often require somebody making sure that progress happens (e.g. by filing appropriate issues on places that will need to be changed, so we don't lose track) so that the desired end state can be reached.  We hope that happens here once the foundation is ready.
> 
> So I think we're going to propose that the TAG close this issue, and thank you for requesting our feedback.  Let us know if there's anything else you'd like us to look at later on in the process.

Closed issue.

##### <a href="https://github.com/w3ctag/design-reviews/issues/303">RTCQuicTransport</a>

David: A little disturbing that RTCQuicTransport, RTCIceTransport, and WebTransport are in three separate groups.  Seems like they ought to be relatively consistent in many ways.

Sangwhan: In practice, might actually be mostly the same people

David: Though looks like `RTCQuicTransport` now subclasses `QuicTransport` from the WebTransport spec.

David: Are the handshake / consent to communicate issues handled?  How are they different for the RTC case?

Sangwhan: Access Control Lists might need to change as a function of set of peers.  Direct communication, STUN, etc.

Sangwhan: I think we can close this; layers on top of WebTransport which we think is reasonable.  Don't think it would be as platform-breaking as we thought initially.

David: What about mt's comment " No need for ICE, except where it is necessary for establishing peer-to-peer communications."

Sangwhan: This is very much about the WebRTC use case; the ICE transport is mandatory, so this doesn't do that.

> @cynthia and I are looking at this in a breakout at the TAG's virtual face-to-face meeting.
> 
> In so far as we're able to understand what's going on, and given that further in-depth review by the TAG seems unlikely, I think we're comfortable closing this review.  The TAG isn't really the best source of expertise in this area; there's a lot more knowledge of this across a number of other venues such as the IETF QUIC WG and the IAB.
> 
> Given that there have been significant changes from the original proposal, we can only extrapolate the impact of the changes in terms of these proposals as general APIs outside of a WebRTC context. An updated explainer that explains the connection between the proposals would have been useful.
> 
> That said, we're happy to see that it is at least connected to Web Transport and to `RTCIceTransport` in what I *think* are reasonable ways, although it's not especially clear that the *naming* of the classes expresses those relationships clearly.  (For example `RTCQuicTransport` and `RTCIceTransport` sound like things that are at the same layer, rather than one being on top of the other.)

##### <a href="https://github.com/w3ctag/design-reviews/issues/304">RTCIceTransport</a>

##### <a href="https://github.com/w3ctag/design-reviews/issues/341">Feature policy evolution</a>

### Break **23:30 - 23:45 UTC**
### Breakouts 6 **23:45 - 00:45 UTC**

#### Breakout 6a - Rossen & Sangwhan

##### <a href="https://github.com/w3ctag/design-reviews/issues/416">EditContext API</a>
Sangwhan: I recall couple of similar proposals from the past. One from Google and one by Microsoft, I believe around IME. 

Rossen: I'm fairly familiar with this proposal. Happy to discuss issues about it but don't necessary want to just push forward for it.

Sangwhan: What have you heard from other implementors about this proposal?

Rossen: Fairly positive.

Sangwhan: I've read the proposal. The question I have is, how does this work with an IME during selection?

##### <a href="https://github.com/w3ctag/design-principles/issues/154">"Cheat sheet" for reference during design reviews?</a>

#### Breakout 6b - Peter, Tess, David

##### [Local Font Access](https://wicg.github.io/local-font-access/) (the [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) and the [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400))

Tess: These specs have been merged.

Tess, Peter: Seems like they haven't been very responsive to our comments so far.

Peter: Seems like we should just make sure all the comments we have are reflected in issues in their repo, and then close both of our issues.

David, Peter, and Tess filed or found issues capturing the various TAG discussion on these:

* [Non-OpenType fonts #19](https://github.com/WICG/local-font-access/issues/19)
* [Anne's feedback re: Non-goals and alternative approaches #20](https://github.com/WICG/local-font-access/issues/20)
* [Fonts need to be sorted #23](https://github.com/WICG/local-font-access/issues/23)
* [mention additional fingerprinting surface in details of font versions #25](https://github.com/WICG/local-font-access/issues/25)
* [Please add a Table of Contents to the explainer #26]()
* [explainer suggests iterating all the fonts in order to find Consolas #27](https://github.com/WICG/local-font-access/issues/27)

We then closed both reviews.

##### [navigator.scheduling.isFramePending](https://github.com/w3ctag/design-reviews/issues/415)

David filed [explain relationship to DOM/JS dirtiness versus hardware vsync signals #3](https://github.com/szager-chromium/isFramePending/issues/3), which captures [a comment](https://github.com/w3ctag/design-reviews/issues/415#issuecomment-562348578) he left on this review months ago.

We decided to leave this open until the next F2F to see if they make any progress.

##### [CSS advanced attr() function](https://github.com/w3ctag/design-reviews/issues/513)

Tess: multiple changes here: (a) type parameters and (b) fallback

David: Also (c) applying to elements and not just `::before` and `::after`.

Tess (later): also (d) now `var()`-like

Peter: There is some ongoing discussion about security issues.

David: I think this feature was originally motivated by the (no longer current) desire to allow CSS to explain all the presentational aspects of HTML.

David: I think there was also discussion about URL base URLs not being right.

Tess: I have that link -- 3 open issues I think are relevant.

(Tess adds [comment](https://github.com/w3ctag/design-reviews/issues/513#issuecomment-634354739).)

### Break **00:45 - 01:00 UTC**

### Readouts/Wrap-up **01:00 - 01:30 UTC**

#### 5a readout
Tess: We had 4 things to look at and we only got through one. It was the declarative Shadow DOM. We took time to read the explainer and ended up adding 5 more comments to the issue. The explainer is long but well written.

David: It would be great to compare your set of issues with the ones we have at Mozilla standards feedback.

#### 5b readout

Rossen: This was the promises guide review. Went through the guide, tackled 4 issues total. Out of the four issues three were actionable. "When not to use promises" - decided to add a new section. "Guidance on error types" - the missing part we should add is when you should reject or complete. "Are Unresolved promises during unload?" - noted well in the issue.

#### 5c readout

David: Spoke about web codecs first and closed it. Basically it's been looked by a number of TAG members and the overall API looks good. Peter had raised an issue about media recorder. We want to see build up on such API. Left comment. 
The API looks a bit too simple at first but it works, so hey! :)

David: Next we spoke about `RTCQuicTransport`. There's a lot of context and we're not necessary the experts in this. Given that the right folks are already involved in the progress of the proposal we decided to close with a Nit comment about the class naming. (reads comment)

#### 6a readout

Rossen: Looked at two things, first is EditContext API proposal. The first set of feedback for the API has been positive - the one issue that was raised was about the privacy aspect of this, which is a non-issue. In our discussion Sangwhan brought up the question of sequence of events in a context of an actual compositional IME - but we are fairly comfortable with the high level design of the proposal. The next one is issue 145, the "cheatsheet" for referencing during design reviews. We took the TOC from the design principles document and reformulated into a list of questions. Would love to hear feedback on this.

https://cryptpad.w3ctag.org/pad/#/2/pad/view/MIJs8efMW1yTEQ3exik+-aKy1qyC5AH67r750mQ9LvI/

#### 6b readout
Tess: This was a 3 people breakout!! We ended up closing 2 issues out of 3 :) And also one extra issue closed.
First issue was Font Table API and Font Access API. These have merged into one spec, Local Font Access. We made sure that all comments we had are opened as new issues to this spec and closed the original reviews.

Tess: `isFramePending`. David left a comment few months ago but didn't get reply. Opened an issue to the spec and wait until it gets addressed.

Tess: The bonus issue was the CSS Attr issue from Breakout 1B. There are 3 open issues on CSSWG related to this. The design review perhaps came too early since it is under very active CSSWG work. We'll wait until it matures and review a bit more.

Rossen: That feels a bit backwards - reviewing mature APIs retroactively without early feedback/consideration doesn't seem right. Especially with regards to security issues.

Tess: It is happening - one of the issues is a security issue
