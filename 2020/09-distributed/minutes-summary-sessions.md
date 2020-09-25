

## Summary For Sessions 1, 2

### 1a

Sangwhan: we looked at schedule.posttask API we think it's good.  Doesn't have a spec - just an early review. We wrote we're happy to move it fwd. Proposed closed.

Dan: SGTM

Sanghwan: **closed**

Sanghwan 2 virtual keyboard specials... 

Ken: visual viewport API is shipping in IOS13. 

Sangwhan: problem is that we raised an issue of is it good enough - and whether that should be improved instead of virtual keybaord specific thing.  If it's in the virtual keybaord then everyone has to invent their own thing - which seems like an antipattern. We suggested it should all be in the same place. Not exactly the visual viewport.  Occlusisons are like an inverse of visual viewport... Other part brought up is "how about multiscreens"?

Alice: the problems do seem close to one another...

Ken: which is why I filed an issue on windowplacement API regarding visual viewport and how they interact...

Dan: so ...

Sangwhan: we don't have consensus on this design - we proposed to maybe talk during TPAC.  This design is contentious.

Dan: so where do we need to engage in TPAC?

Sangwhan: editing TF maybe - I will check the schedule.

Dan: add a label? [label here](https://github.com/w3ctag/design-reviews/labels/Progress%3A%20needs%20consensus)

### 1b

Dan: Alice and I talked about WebXR Layers... got into a meta-discussion about explainer quality and whether or not we need to edit the explainer explainer to prompt people to give more context earlier on in the explainer...

... First have someone read the explainer who isn't familiar with the problem space and see if they can understand it... repeated problem of explainers jumping right into the solution without explaining the problem that thye're trying to solve.

... Might put some of this into a talk for TPAC and guidance to be shared with chairs.

... Some feedback on this WebXR layers thing.

Alice: I should leave some feedback in my own time.

Dan: Talked about incorporating extensible-web.md into design principles... 
https://github.com/w3ctag/design-principles/blob/master/extensible-web.md

.. probably subsumed by existing principles, should get rid of the original doc, it's just an artefact.

Sangwhan: Yes, incorporate and delete sounds good to me.

Alice: my thought was that it's already subsumed...

... I think this is subsumed by the discussion around [high level vs low level APIs...](https://github.com/w3ctag/design-principles/issues/117) and [separations of concerns](https://github.com/w3ctag/design-principles/issues/169)

... also wondered ... whether we still stand behind this advice.  Low-level capabilities composed into coarser features.  I think you ship things according to user needs.  David had some good language around : your design should include the layers of abstraction that makes sense.

Dan: Current advice in design principles doc seems to be more nuanced. So perhaps we should sunset/obsolete this doc.

Sangwhan: I don't know if we have guidance that touches on this particular nuance. 

... Is there still traction around this movement? Some of the Fugu APIs seem to be primitives, so yes, but I'm not sure what the message should be.

Alice: Perhaps we need to leave this one open, and discuss it as a full plenary.

Sangwhan: I think we can sunset this document, and not take a position on it for now.

Dan: People might visit this doc and interpret it as TAG guidance, and not visit the design principles sections which are relevant.

... not all of this is incorporated into the design principles.

... Maybe we could put a note at the top of this document, saying it is out of date, and to check the design principles doc. ... we are still in the process of incorporating this guidance into the design principles doc, with a pointer to issue 182.

Sangwhan: I don't have strong feelings on what stance we should take on extensible web in general.

Alice: it was behind the design of web componebts, shadow dom and so-on. I'm still actively involved in the relevant discussions for those things.  Sometimes primitives for the sake of primitives is not right - in opposition to user needs.

Sangwhan: the question is: is the web for framework developers or for web developers. 

Alice: if there's only one right way to do things don't make develoeprs do that every single time. Just ship the one right way. Encapsulating the thing that does the thing that you need.

Ken: high level primitives like button but with some escape paths...

Alice: More nuance requried. E.g. the Dialog element. People are still asking for the Dialog element but we didn't ship it across the board due to feedback that it wasn't primitive enough.

Dan: Perhaps we should leave this open, and change the title to reflect that the world has changed, e.g. "what is the modern interpretation of the extensible web principles"


... Also talked about dark patterns, asked Tantek for examples.

### 2a

Alice: me and sangwhan - we went through some of the readability edits. CSS section. I will use my session with tess. JS section ready to go but needs Dan to approve.  Event session we spent the bulk of the time on - one new proposed change. A couple sections in there are too long.  Guarding against recursuion and events vs recusion. Should these both be mini documents and pulled out of the design principles?

### 2b

Dan: Ken and I talked about ...

... [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481)

... I'm still concerned about privacy, allowing malicious websites to put things into the title bar to trick the user. It's not in the privacy section in the spec; I wrote a comment asking about that.

... Ken noted it should reference display_override, a manifest file new feature.

... [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408)

... Need to understand what the state of this is regarding wide review. Left a message asking about that. Need to discuss in wider plenary, not sure where we can add value at this point.

... [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536)

... Think we're ready to close. Let's just close it.

(all agree)

... [Best practices for feature detection of DOM API](https://github.com/w3ctag/design-principles/issues/137)

... The PR for this landed, Ken thinks we should close.

Alice: I agree.

Dan: Ok, I'm going to close it.

## Summary For Sessions 3, 4

### 3a

Rossen & Tess - we had 4 issues

Tess: [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

... we created a spreadsheet.. we wanted to draw attention to it.

... [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - not much to do.

... high level and low level in Design Principles - I took an action to draft a PR. The PR is in the minutes...

... [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - our previous comments haven't been answered.  a big difference between the same origin case and cross origin case. Rossen wants to split into 2 parts.  I agree.  Same origin casee is fine more or less.  We haven't seen any progress with problems raised on the x-origin case.

Dan: SGTM I think he should do that.

### 3b

Trust Tokens

Dan: These could potentially be useful to eliminate CAPTCHA from the web; web users everywhere would rejoice. There's still an issue with the fact that the issuer can know where you've been. It's a tracking issue. Peter to open an issue on their repo for this. I also asked for a status update.

COOP Reporting API

Dan: We decided to close in the summary session.

[Consensus to close. Peter to write closing statement.]

Best Practices for registries

Dan: If registries are sometimes inline in specs, could there be a microformat so those could be easily crawled, to ease automation. I left a comment to that effect.

Peter: I filed a Bikeshed issue to add it as well. I'll work with Tab to make it happen.

### 3c

...

### 4a

MiniApps

Dan: Yves gave us an update on MiniApps. The community has really taken our feedback on board. They're looking at incorporating their requirements into Web App Manifest. They're reconsidering doing their own URI Scheme. They may proceed re: packaging, though. Overall a good, positive outcome for our review.



### 4b

Ken & Tess 

Tess: We picked 2 issues ... we talked about [546](https://github.com/w3ctag/design-reviews/issues/546) - web page settings to save battery.  Both kind of not sold.  Maybe a reason from the signal the author is to inform the site that you are doing the throttling... but if you tell the site "we're running out of battery please stop" authors often have misconceptions about how web sites perform... the alternative is jusy as likely to do worse for batter. 

... video case is a good example of a site that won't cooperate.   We commented on the issue.

... 482 - URL protocol registration for PWAs... we left a comment in may and there have been no replies.  

Dan: should we sumarily close?

Tess: I pinged the issue. 

## Summary For Sessions 5, 6

### 5a

Alice: We spent most of the time talking about separation of concerns. Trying to come up with cases that problematize the separation, what kind of tradeoffs have existed in the past. We could potentially come up with some guidance from these cases. The characteristics of DOM, cascade, scripts, etc. Features that went into one of those that could have ended up in another one.

Tess: For example, something that ended up in CSS that ended up in DOM. We should be giving both positive and negative examples - we have both cases, and mistakes should not be repeated.

Alice: We also discussed media queries based on preferences (e.g., `prefers-reduced-motion`). We had orthogonal views on this, whether this should be a media query, CSS, or implemented in DOM. We had a long discussion but don't think we are ready to write something.

### 5b

Rossen: Essentially we discussed...

... Task Scheduling issue ... #72

David: Closed it in the sense that there's not much to be done with it at this stage.

Rossen: Walked through the chain of linked issues, what's linking to what... convinced ourselves that there's enough linkage back to this issue, that if it becomes relevant again we can find it.

... Also linked to a test case David wrote which fails in all browsers, demonstrating that it's not interoperable.

... Couple of related issues in CSSWG... flushing layout when it happens. Other issue against HTML spec. 

David: Blurring two issues, one of which is still open.

Rossen: VisibilityStateEntry...

... went through this, by the end chased discussions happening in peformance timeline repo. Some of the latest chatter between Ryosuke and Nicolas suggested we can rethink this issue. Nicolas is going to get in touch with Yoav, might put it into some kind of throttling state API.

### 5c

Sangwhan: This breakout is 404 due to a technical complication on my end.

### 6a

Tess: Got through 4 issues...

... Storage pressure event...  one small issue with explainer, otherwise looks fine. Propose close.

... QuotaChange event, would tell you whether you're under storage pressure. Seems reasonable... well-behaved sites that are trying to do the right thing can listen for that event and scale back storage. Doesn't negatively affect sites that aren't doing the right thing. Browsers need to mitigate risk of sites causing the device to run out of storage regardless of this API.

... Issue is around example code in explainer suggests that the event always means that there is storage pressure, as opposed to being a transition between. There is already an issue filed on that.

Rossen: Is pressure UA defined? I mean quota.

David: There is flexibility on this. Firefox does something different from Chrome. This is a fix for a fix for a fix at this point... there was a security problem with the original fix, and privacy, so then there was a fix for that, but that had another problem, and now we're here, so the amount of thought on this is substantial.

All: let's close

Tess: ... isFramePending. David and I looked at this in a breakout in Cupertino, been pending external feedback ever since.

... poking once more then closing.

... IFrame Execution Pausing. Was blocked on another review which has closed. Pinged.

... Design Principles issue around monkey patching. Had a good conversation about this... we think it's at the point where we could take a stab at writing a draft PR. I agreed to do that "soon".

... Framing of "don't monkeypatch" is negative, but there is a positive side which is "think about accessibility", design extension points in your API so that people don't *need* to monkeypatch. Need to write guidance for both sides.

... "try not to monkeypatch", but also "if people are monkey patching, see if you can change your design not to need it"

### 6b

Alice: We talked about wake locks. We were both happy with the API, there is an object on navigator that returns a wake lock (gated by a promise), which also provides a sentinel which lets you control the lock. The only comment that I had was that the request method takes a parameter (e.g. screen) but why there is a parameter is not explained. Presumably this is for future extensibility, but it would be good to have an explanation. We might even want to add it to the good explainers list. We proposed to close this.

... Then we talked about debuggability in specs, which is an issue that was raised by someone external. One of the positive examples the issue raised was about web animation debuggability; and a negative example was flexbox. The OP suggested that intermediate states should be exposed, which we don't think is a good idea. Sangwhan suggested that there should be a normative context for inspector/debugger/WebDriver environment, like we "have" with private browsing mode. The action we have is to add text into design principles, one to add "please consider author needs" in the priority of constituencies section, and another in the "clear algorithms" section about intermediate state/debuggability there.

... We punted the "debugger mode" discussion for later, as it was considered pretty substantial.

Rossen: Question about the debuggability; UAs do specific things when debuggers are on. Is the intent to standardize some of this?

Sangwhan: Yes.

Rossen: It is a hard problem. Currently debuggers can only provide information on where you are, not how you came here.

Sangwhan: I think the point is that we lack the infrastructure for specs to refer to being in a "debugger" entirely.

Alice: Does it make sense to have a place where APIs explicitly aimed at testing/debugging can live?

Rossen: If you open the network logger in Chromium, you can get a lot of information that might not be useful to the general audience.

Alice: The audience of these tools are web authors and to some extent browser engineers. I think the difference is that we put an API on it. (formally)

Rossen: I'm not suggesting this is a bad idea, it's just that we might be sending the wrong message. Spec authors might suddenly feel pressured to add debugger APIs, which is probably not ideal.

Alice: We have no plans to say that.

Rossen: Users shouldn't have to suffer because the debug mode switch was flipped. Layout related matters are really complicated, especially when you want to consider cases like interpretability.

David: Another source of complexity with layout is that there is only a loose mapping between the spec and the implementation... in other parts of the platform, implementations more closely match the spec.

Rossen: Houdini layout APIs continue to evolve and get wide adoption... might be lucky and stumble on something we can use as a hook for tracing or something similar... your custom layout is just a tracer, you just get back the current state as you go. 

... This will be mostly accidental, and highly aspirational.

## Summary For Sessions 7, 8

### 7a

Sangwhan & Ken

Sangwhan: **Native filessystem** has some changes - we're happy with the changes and we'd like to close. 

Ken: They incoproated a lot of our feedback. Seems to be in a good shape.

Sangwhan: namespace question.

Dan: why shouldn't web users world wide be alarmed by the possibility of a web page reaching into their native filesystem?

Sangwhan: users have to select - displays a file picker dialog - sort of a nicer way of doing input type=fiile. Users have to opt in.  Drag & Drop.. or display a file picker.  There are mitigations against privacy abuses.

Alice: the explainer looks very nice as well. This seems like a good outcome.

Dan: I'm happy with it.

Sangwhan: [**closing**]

Ken: no update on video encoding.... 

Sangwhan: we didn't hear back.

Ken: kind of the same with serial API... Reilly said they would get back. We chased.

### 7b

Dan: I approved the changes  design principles js api section...

### 8a 

**MathML**

Alice: we spent time on this...  One open issue was links.  Brian had put the question to us on how to handle links.  A lot of exisrting code that people don't want to update and that implementation already works in Firefox with hrefs. So we left a comment saying that we should be backwards compat but that this puts it in a tough spot regarding shadow roots. You could make it allowed by deprecated. Not too worried about the shadow root situation .. Punted back to mathml group.

Dan: and we proposed to close this with this feedback.

Alice: [**closed**]

**WwbXR Device API redux**

Alice: we looked at this - the filed a follow-up review because they're close to shipping.  We looked at it - not much has changed. We left a comment asking about accessibility and unanswered questions. Meta-point that this is a timely issue - right time to think about accessibility. Left it open to see if they engage.

**WebXR Depth API**

Alice: Early stage. Getting sensor data about the geometry of the space that you're in. Missed opportunity to provide a non-visual use case.  They're using unsigned ints for coordinate system - some more explanation needed. Also mysterious property `normtexturefromnormview`... Asked for pointers.

### 8b

Sangwhan: Yves and I discussed **transferrable streams**. This is another proposed closing. Work is solid and use cases are solid.  No s&P concerns. Useful features.

[consensus to close]

Sanghwan: [**closes**]

Sangwhan: **miniapp URI scheme** - work still in progress.

Yves: they are backing away from the solution of a new URL scheme.  OS-level options... 

[we keep open for now]

Sangwhan: we'll revisit when they have a better proposal.

## Summary For Sessions 9, 10

David, Rossen, Tess, Hadley, Peter, Dan, Ken

### 9b

Ken & Tess

Tess: ken & I got through scheduled for 9b. Total field optional in payment request API... they never requested another review - so we pinged them. We looked at a declariative shadow dom issue. Ken left a comment which Alice & Peter should look at [494]. Multi-screen [522] is closed. Guidlance on ... [design principles 111] - pending ext feedback. We looked at [544] secure payment confirmation.

Ken: seems to be created due to regulations in e.g. EU - where there are out-of-band auth requirements. 

Tess: some existing paymentds methods - e.g. Applepay - already have strong 2nd factor auth. So unclear that any change is necessary. So they've added a new method... I'll take a deeper look & leave some comments.

... we looked at WebAssembly JS Types. Very low level and awkward to use. And naming - type table (nothing to do with HTML tables). We have a PR in the design principles about web consistent naming. Once we land that we can refer to it here.

### 9a

Dan & Hadley

Hadley: we looked at a couple of issues in Ethical web Principles - Tantek opened an issue to avoid enambling Dark Patterns. It's an important issue - but how much dark patterns are full-on fraud .. abuse scenarios.  A lot like what we ask them to do in security & privacy reviews.  Abusing users' trust. Is this an appropriate realm to add into the security & privacy questionnaire. 

Tess: OK!

Hadley: Also spent time on issue 19 - back up with previous decisions & experiences. We feel it's useful to document where these came from. Some of it is not TAG reviews - e.g. the principle against state surveillance and sponsorship - pointing to the STRINT workshop. We saw that Tess addeda PR to pervasive monitoring finding.  So we agreed to leave the issue open to collect instances ike that.

Tess: That sounds great. I like how succint the existing doc is. So this idea makes me think (1) we could probably avoid making the doc longer if we added the example boxes - a bit about the background - a casual reader could skip those boxes. (2) I have that PR - used the standard ref syntax. It makes it appear inline in [BRACKETED] form... and makes a references section. One one hand I'm used to writing docs that use references in that manner. I'm not necessarily the best gauge of how references should work. Users are more used to links.  More webby.

Hadley: yes. we need to preserve the usefulness of the doc. I brought up the issue - the [BRACKETED] is not very modern webby.

Tess: I'm happy to re-work that PR....

Tess: a compromise - this doc is in respec - it should be possible to do the links conversationally but also cause a references section to get generated. 

Dan: I think that would be the best of both worlds.

Hadley: totally in favour.

### 9c

Peter & Rossen

Rossen: we spent the bulk reviewing the **web share API**. In review we discussed the broader project - how it fits into everything else.  It would be a good addition in terms of capabilies - most of the feedback was about the shape of the APi and how it can be improved going forward. Currently on `navigator` - and a promise. Next issue was what webshare works with.  UA is the mediator of shared data - users choose something to share. browser gives you options.  Thing you can share currently is a file or a URL.  The observation is - why file couldn't be blob - image shared directly from camera. Additional thoughts around shared data extended with more info.  Bunch of comments. Overall the API capability does look useful.  We'll file some issues to their repo.

Peter: did it.

Rossen: web share target API was not part of this review.

... we did 2 quick rubber stamps of CSS issues. One exposing an additional API on font face... signed off and closed it.

[our issues closed]

### 10a

Tess & Dan

Tess: we looked at geolocation and we'd like to propose close.  Everything straightforward.

Hadley: from a process perspective - it doesn't have an explainer.  There's no point though?

Tess: I think it would be great if they had an explaier. However they had only 4 changes since they went to rec - so we just looked at the 4 changes.  As far as the scope of the review goes...

Hadley: the reason I was looking for an explaienr - when we met with them in Sopporo - privacy aspects. 

Tess: WebXR PRs - we haven't got responses to our feedback. So we followed up.

Tess: we then looked at Security & Questionnaire PRs and made some progress.

### 10b 

Rossen, Hadley, Yves, Peter

Peter: content encoding type for jxl - wreird but OK. 

Rossen: DID issue - 1.0 - we talked about it. They are not seeking feedback ? We looked at the examples. Well articulated.  Without diving deeper into technical details it's hard to say. 

Hadley: we should do a deep dive.

Rossen: they want to go to CR by TPAC.  

Dan: any browser tech we can review?

Rossen: DID core is filled with issues and questions...

Dan: let's allocate a breakout session for it in next 2 weeks.

Peter: we did a review of `rawSocket` API - I'm giving feedback.  We said  better to have high level APIs... 

## Summary For Sessions 11, 12

### 11a

Tess & Sangwhan

- [Constant bitrate audio encoding with MediaRecorder](https://github.com/w3ctag/design-reviews/issues/540)

Tess: Only thing we didn't like was a naming issue that I raised, months ago. Propose close - would prefer if they fix the naming thing, but it's fine either way. No other concerns.

Sangwhan: Future references to variable bitrates should be called variable, for consistency.

- [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-principles/issues/157)

Tess: Tantek filed this when he saw issues with JSON modules (?)

... Only one design review case where this has come up, we think design principles should result from seeing the same thing a number of times so we understand the nuances.

... Were waiting for TC39 to make progress, and they have made progress, and it looks great, so we propose close.

### 11b

Alice & Rossen

- [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511)

Alice: spent a bunch of time on beforematch event.  Kenneth had left some comments.  A little skeptical about whether it could stand alone apart from `content-visibility: hidden-matchable`.  Comment from Joey(?) agreed, maybe makes sense to combine them.

... also left from questions about some points the explainer didn't make clear.  They landed on `beforematch` event.  Listed alternatives considered, but kept saying *** without spelling out how the current proposal doesn't allow that.

... So suggested combining the explainers and combining the reviews, since they form one conceptual API.

Alice: Second part of comment about was trying to understand becoming hidden again.  If you find text in a hidden section, text will expand.  At some point in the future the section should close, but was never clear when or how it should close.  So left a comment asking for gaps in explainer to be filled in to explain this.


### 11c

David & Peter

- ["With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76)

David: Poked around reading things, changed some of the labels on the issue. \o/

... Couldn't figure out how to make progress, but didn't want to close.

Peter: We need to find the relevant people and get them together, which unfortunately is going to be impractical with a virtual TPAC.

- [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197)

David: Was left open for an issue in IO dependent on an issue on HTML dependent on and issue in CSS which is referenced from *another* of our issues, so propose close.

[#489](https://github.com/w3ctag/design-reviews/issues/489) is what references all of the above issues.

... we closed another issue closely related to that issue yesterday.

- [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172)

David: Talked about a better way to word this, left a brief proposal in the issue. Fine to leave this as a comment for now until readability edits all land.

### 12a

Alice, Sangwhan, & Tess

- [EditContext API](https://github.com/w3ctag/design-reviews/issues/416)

Tess: All three of us spent quite a while reading the updated explainer. Does seem quite promising, solves real user needs. It's pretty hard to understand.. the explainer isn't bad, but the names of the APIs combined with the complex code examples make it hard to understand, so we each left comments asking for clarificaitons or expansions on the explainer.

- [To fulfill or to resolve](https://github.com/w3ctag/design-principles/issues/135)

Tess: Decided this issue should be on the Promises guide. The clearest explanation is the "[States and Fates](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md)" document by Domenic, but it's lacking in code examples which would illustrate each of the terms.

... Decided we should add the definitions from states and fates to the Promises guide, but with examples to illustrate each of the states and fates.

- ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154)

Tess: I have a script for the S&P question to extract the questions, so people have something to easily copy and paste, and I thought we could use that strategy.

... Sangwhan and I both have WIP scripts to do this for the design principles doc.


### 12b

David & Rossen

- [give advice on read-only lists](https://github.com/w3ctag/design-principles/issues/50)

David: Read a bunch in WebIDL, made some notes in the issue that might help move things along in future.

## Summary For Sessions 13, 14

### 13a

Sangwhan & Dan

* [Miniapp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523)

Sanghwhan: Miniapp specs.... we talked about lifecycle and manifest.  In lifecycle we asked what they mean by "worker" ... we punted reviewing until there is more work done on their side. 

* [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524)

As for manifest - this will change signifigantly - it will be an extension of webapp manifest as per our review comments - which is great. When that change happens we will review the new version - removing the milestone and leaving the issue open.

* [adding new media formats](https://github.com/w3ctag/design-principles/issues/171)

Sangwhan: Then we discussed about media formats.  Some draft text posted as a comment on the issue.  Domenic suggested something about fetch-likes and I split that into a [new issue](https://github.com/w3ctag/design-principles/issues/238).

[discussion on the new text]

### 13b

Ken & Yves

* [Periodic Background Sync](https://github.com/w3ctag/design-reviews/issues/367)

Yves: good to have automatic subscription ... 

* [hasDroppedEntry in PerformanceObserverCallback](https://github.com/w3ctag/design-reviews/issues/547)

Ken: sometimes you can subscribe to too much - so this helps. feature makes a lot of sense... made a comment.

### 14a

Kenneth & Sangwhan

* [Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112)

Sangwhan: usefiul feature we don't support at the moment.  Design is strange.  No best practices existed... Pattern is not what we've used in the past. We discussed at length - we'd like to promote a pattern of using postmessage to transfer the actual object. Then the main thread would no longer has access. This is same pattern as used as transferable streams. If implementers think it's possible. I will draft a section that mentions it.

* [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

Sangwhan: no progress - we punted

* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370)

Sangwhan: we should pay attention - dangerous. We need a better mitigation. Maybe we can bring the peiople together in TPAC.

* [Service Worker Scope Pattern Matching ](https://github.com/w3ctag/design-reviews/issues/417)

Ken: Looking at most common library - path-to-regex ... would be used in serviceworkers... Generally it looks like a good proposal. 

Dan: Can we close?

Ken: Should be an early review and I think we should close it.

Dan: sounds good to me.

### 14b 

Hadley & Dan

Dan: We landed a PR that Tess wrote on ethical web principles, normalizing the reference section at the end of the doc. Uses a local biblio for some of the references.

... Now we need to add some additional references to underpin some of the statements we've, made, e.g. pervasive monitoring is an attack RFC, reference from statement on government surveillance. Not sure what form those refs should take... inline links, additional text?

... Taking a look at what those references should be, dropping links into issue #19 on the ethical web principles.... ???/ workship, RFC Internet is for End Users, internet society policy briefs on privacy and freedom of expression. Need to collect some external references to authoritative papers, academic papers etc. to underpin our statements. Including evergreen findings.

Hadley: We have this long paper trail as a community, it's helpful to tie that in to the principles.

### 14c 

Alice

False dichotomy between logical semantics and 

... started looking at promises states ...

Dan: can we provide additional guidance in the promises guide?

Sangwhan: i could provide some sentences...


## Summary For Sessions 15, 16

### 15a (Hadley & Tess)

Tess: We only had time for one of our issues, [the one David filed re: JSON-LD](https://github.com/w3ctag/design-principles/issues/128). That issue went on a few tangents, but we got back to David's original concern which relates to how JSON-LD is a single format with multiple processing models (JSON-LD and JSON). We thought that the issue he identified is really a more general one, related to polyglot formats in general, so I filed [New principle: Discourage polyglot formats](https://github.com/w3ctag/design-principles/issues/239) to capture this concern.

... the main tangent in the original issue was related to the JSON-LD spec's use of Web IDL. We think this discussion can continue in an existing issue, [New principle: Web IDL is for APIs exposed to the web by browser engines](https://github.com/w3ctag/design-principles/issues/216)

... We hope that these two other issues exhaustively cover the concerns from the original issue, which we'd like to close. David, could you take a look and confirm?

David: Yes.

### 16a (Hadley & Kenneth)

Kenneth: Looked at the realms proposal. Top level global browser object concept. The proposal is to have a top level isolation allowing you to run script that doesn't affect the global object of the parent, unline window.top in the case of iframes. You can call fetch() from that level since you don't have access to the global. 
... Left comments.

#### 101 Temporal

Kenneth: A replacement for DateTime. Has been reviewd and closed by Sangwhan. If we are going to recommend the usage of this we need to have a story that tells how people should be transitioning from existing DateTime to Temporal. 
... Left comments.

### 16b (Rossen & Tess)

### [WebRTC playoutDelayHint](https://github.com/w3ctag/design-reviews/issues/441)

Rossen: This is somethign we have already reviewed in last real F2F in Wellington and we were quite happy with the overall use-case and shape of API at that point but we had one concern - seconds instead of ms. And they are doing because WebRTC uses that - so it is consistent, so we would like to close it. So we want to add some recommendation to use ms per default if there is no prior art.


### [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549)

Rossen: We spent most of the time on this one, the rest of the hour. Most fo the discussion was around the fact that that client hints are intented to help with user  fingerprinting and some of these claims have beenmade in the past. This particular review starts with a statement that there is no security and compliance template filled out, just referst to the existing client hints one, stating that it doesn't add any significant new info to be accessed - very hand wavey

The fun part as we were chasing similar issues from otehr WGs and previous TAG reviews we dicovered interesting discussions. Client Hints can solve exising ... basically increasing fingerprintability.

Where is Client Hints in terms of review - have we signed off on this?!? Some was closed as it looked as it would not be ready before 2021... so no approve/disapprove from the TAG PoV.

We hae a request for them to reivew and fill out the security and privacy document.

Dropped the last issue - ran out of time.


## Summary For Sessions 17, 18

### 17a (Tess & guest Pete Snyder)

#### [Security & Privacy Questionnaire PRs](https://github.com/w3ctag/security-questionnaire/pulls) & [issues](https://github.com/w3ctag/security-questionnaire/issues)

Tess: With Pete Snyder from Brave. Intent was to look at all open PRs and issues. We merged [Revise 2.6 for clarity](https://github.com/w3ctag/security-questionnaire/pull/98) and [editorial + sec/priv sections rewrite + howto rewrite](https://github.com/w3ctag/security-questionnaire/pull/103). Made some progress on the open issues.

Tess: Tried to define what the connection is with the design principles. Mostly ended up becoming on the same page, which was useful.

### 17b (David & Sangwhan)

#### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389)

David: Not much discussion, but Sangwhan said he had talked about this with Yves in the last F2F and for a early review it's fine to close for now. Since we don't have much networking expertise, it might be best to later revisit this with people who know better.

#### [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304)

David: We tried to understand this, and wasn't that successful. Sangwhan took an action to talk to Dom to figure out what this is about. We all agreed with Peter's comment on the raw socket API, and we'd like to know if this is just another version of this. Hard to tell.

#### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341)

David: Not a lot of progress, but we found the registry and managed to connect the dots on how this eventually evolved. We had this issue and #525, principles #41, and principles #144 which are all interconnected and linked a bunch of issues. Otherwise, we didn't make a lot of progress.

Sangwhan: For #341, one of the issues has been resolved by factoring parameterized policies out to Document-Policy, so some of the confusion in Andrew's initial issue has been fixed.  As for `lazyload` policy that's somewhat inconsistent, still not sure if it was addressed by refactor.

#### [Need guidance on returning error values vs throwing exceptions](https://github.com/w3ctag/design-principles/issues/55)

/dev/null.

### 17c (Alice & Rossen)

#### [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476)

Rossen: Very large issue. There was a new explainer that Alice helped with, which is better. The motivation is better explained. Links to three modules. The module we looked at is [Personalization Semantics Content Module 1.0](https://www.w3.org/TR/personalization-semantics-content-1.0/). The basic idea here is a proposal to expose data attributes on HTML to provide additional semantic information about various cognitive or learning requirements. We reviewed all of the key-value pairs and found a bit of inconsistencies - the high level feedback was how is this expected to work from the UA, AT, or script/extensions. The other point was that some of the attributes were dupes of existing features, such as `data-purpose` is same as autocomplete.

Alice: This case was a 1:1 mapping of autocomplete.

Rossen: We saw a similarity with microformats, some of the stuff defined here touched on addresses and phone numbers which microformats already does. No idea if there is collaboration.

Alice: We realized that the user needs is solid, although we had questions about the consumption pattern, and noticed there is a overlap with existing work. The other is distraction, which boils down to 1) is this an ad or promo, or 2) is this a distraction or both. e.g. Is this is an ad, overlay, or sensory which is a repeating animation. All of the ad based ones are at risk, because it is a revenue generator. Unlikely it will be adopted. The sensory value overlaps with the preference for reduced motion and associated MQ.

### 18a (David & Sangwhan)

#### [CSS page-orientation descriptor](https://github.com/w3ctag/design-reviews/issues/515)

David: Page orientation I already reviewed for Mozilla standards position, it's a hack but it's fine and we were happy to consider closing it.

#### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41)

/dev/null

#### [should provide advice on when it's good to return the same object again](https://github.com/w3ctag/design-principles/issues/46)

David: Sangwhan already had some draft text for principles #70, and thought it made sense to address both in the same text. So we now had a draft in #70 that addresses both issues.

### 18b (Alice & Tess)

Tess: Helped Alice land few of the readibility PRs to the principles doc. In particular we got to review the CSS PR and landed it!

#### [Readability edits: Cascading Style Sheets section](https://github.com/w3ctag/design-principles/pull/221)

#### [Readability edits: JavaScript API Surface Concerns section](https://github.com/w3ctag/design-principles/pull/228)

Tess: We did not look at anything assigned to this breakout. We looked at a couple of Alice's readability PRs. I reviewed and approved both of them. Alice made some edits based on Dan's comments, so it's probably safe to land soon.

Alice: I ended up landing the CSS section, which in retrospect should have been reviewed David, so I removed a whole paragraph regarding complexity - mostly because I did not understand it. We should discuss later whether or not this section should be put back.

Alice: Also made some edits to the types and units section. Also spent some time on event design section, so those sections probably need another round of review. Would be good to land all of these ASAP so we can go back to adding stuff to the document directly. (instead of GH comments.)

(Closing remarks. Beer time!)