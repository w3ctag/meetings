## TAG Face to Face
##### 05 April 2018

Agenda: https://github.com/w3ctag/meetings/blob/gh-pages/2018/04-tokyo/agenda.md

Present: Peter, Dan, David, Yves, Sangwhan, Alex, Travis

Remote (starting 1am/2am!!): Ken, Hadley

Scribes: David (AM), Travis (PM)

Invited Guests: Andrew-sama, Mike Smith, Mark Nottingham

Regrets: Łukasz

---

### Welcome

Dan: Let's welcome Kenneth to the TAG.  It's our first TAG meeting with the additional number of people under Process 2018.  I'm excited.  And Andrew joining us as a TAG alum and honored guest.

### Agenda bashing

Dan: We have a draft Agenda in GitHub.  Mostly from issues list.  Mark joining noon today, Wendy joining 9am tomorrow.  Which items do we think require scheduled agenda point and which require timeboxed issue triage?  And other big topics?

Hadley: Do we need external people for WebRTC in secure contexts?

Travis: Not that I remember.

Sangwhan: This is an interop issue; two implementations already do this.

Alex: WebRTC and getUserMedia are potentially distinguishable.

Dan: Do we need anyone external to this room?

Hadley: Tie to design-principles discussion on secure contexts?

Dan: That's more about TC39 making a call about secure contexts.

Alex: I think TC39 was pushing back.

David: I need to think about how to make progress on it.

Dan: OK, on agenda for tomorrow after lunch.

Dan: We should also talk to Mark about BCP56bis.

Dan: Anything else for fixed agenda points?

Dan: Alex, ads.txt?

Alex: Haven't had further conversations.  Pinged; will ping again.

Dan: Saturday?

Sangwhan: Accessibility Object Model.  ??? about talking to Alice.

Dan: Andrew, thing you added about Client-Hints purpose?

Andrew: I was talking to Mark about Accept-CH.  Said Client-Hints only for resources and not for pages.  Want to dig in.

Alex: I'd like to make sure we minute our conversations carefully.

Dan: Should we open a new issue or is there an existing issue we should document the outcome of the discussion in?

Andrew: Tangential, triggered by Accept-CH, but want to dig in about Client Hints only being for resources.

Dan: OK, if not related to particular issue, let's put on agenda for a specific time.  OK, after Mark.

Andrew: Or talk with Mark about it.  In the discussion with Mark.

Andrew: Is there a hole in link prefetch in terms of CSP?  (I added to agenda.)

Dan: OK, for this afternoon after discussion with Mark.

Dan: OK, talk about next meeting next.

Dan: And also evenings for this meeting.  Tonight just dinner.  Andrew can organize.  Friday there's the thing Andrew organized.  Anything Saturday?

### [Next meeting](https://github.com/w3ctag/meetings/tree/gh-pages/2018/07-seattle)

Travis: I have 3 conference rooms for the tentative dates on 4th floor of Westlake building.  Catering all set up.  I don't have developer meetup locked down, but want to do something.  Have feelers out for venue in same building -- Microsoft Reactor, a space for developer meetups.  Need to pick a day.

Dan: I think we should have a half day workshop on Friday the 27th.  Run it like the Melbourne one.

(Mike Smith joins.)

Kenneth: how's that?

Dan: We've been doing developer outreach events, sometimes just panel discussion in the evening.  In some cases whole day "Extensible Web Summit" unconference events.  Lightning talks at start to set the stage.  Then agenda set in unconference format, and sessions with tracks (depending on venue/time), take minutes, and do wrap-up at the end.  That's what I had in mind for Seattle.

Kenneth: Wondering about people's willingness to speak up.

Hadley: It depends on the local culture. We've had it work well in London and San Francisco, but less well in some other places.

Dan: I think it's been helpful to have some premeditated topics.  My sense is the audience in Seattle will probably be willing to engage.

David: I think Boston worked well.

Yves: And Berlin

Dan: Though Berlin didn't have breakouts... oh, I remember the other Berlin one you're talking about

Dan: The all-day one at FluentConf went well.  Not sure how Melbourne one went; I wasn't there.

Dan: If reactor space there is like London... one big room?

Travis: Yes, but big room that can hold 300.

Dan: We can have breakouts.  Need a space to bring everyone together.

Dan: If announced enough ahead of time, people might travel.

Travis: Friday

Dan: I was thinking afternoon to evening?

Kenneth: How does afternoon fit with peoples' day jobs?

Dan: If we give enough advance notice, people can arrange to take the time.  You do get a different crowd for daytime workshop/conference versus an evening meetup.  I think if we give enough notice.  If we can lock in the venue... we can promote locally and get a fair number of people.  Would be great to attract people from Edge team, any Mozilla folks in the area...

Travis: TC39 also meeting in Seattle, some TC39 folks might still be around and able to join.

Dan: TC39 did a meet-TC39 thing.  Should we join forces?

Alex: I'd prefer that.

Dan: Could we do a joint workshop?

Travis: Yes.  I can talk to folks.

Travis: I'll work on confirming venue for 27th afternoon, though if needed could push to 6-9pm evening.

David: If evening, maybe not Friday?

Travis: I think turnout higher if evening.

Dan: Yeah, if evening should be a day we're meeting.

Dan: But also depends on when the venue is available.

Travis: I thinkit is Tuesday or Wednesday; haven't asked about Thursday or Friday yet.  And I'll ask TC39.

Dan: MDN board is meeting following week so I'm staying over, so might get some overlap... maybe a lightning talk?

Hadley: For travel I'm happy to stay through Friday if event is on Friday, but would be good to know for planning.

David: double-check everyone OK with the dates?

RESOLVED: dates still good.  Confirmed.

### Next next meeting

David/Dan/Yves: Next was for Paris, week after TPAC in Lyon.

Alex: week before IETF (November 3-9)

David: ... in Bangkok.

Dan: MozFest is that weekend (October 26-28) in London.  I might be there.

Dan: And no mini-meeting at TPAC.

Peter: usual coordination.

Dan: Right after TPAC should be productive.

### [CSS :focus-visible selectors](https://github.com/w3ctag/design-reviews/issues/233)

David: Not sure if there is much to discuss ATM, awaiting a PR. (Network issues.)
I guess one of us should look at this at some point, but I need to revisit this when the PR is in.

Alex: Is there anything controversial about this?

David: I believe the conformance criteria was unclear. But I don't think this needs group time - I can look at the PR.

Dan: Revisit during this week?

David: Possibly, bumping to later is also fine.

ACTION: Revisit on Saturday.

### [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231)

David: I raised some points, no response so far. I believe this is an important spec that might not be as the authors think

(Travis raises a question - didn't hear)

David: There is a payment method manifest spec, and a payment method URL based spec but they could be better connected. Payment handler lets you define payment logic in a SW.

Dan: Is this how you provide support for cryptocurrencies on the web?

Alex: To some extent, yes

Travis: So how is the spec not ready?

David: There are some issues, the spec mentions something that looks like a browser chrome, but in reality isn't. Other browsers have been against this. The question here is whether or not this could be a workaround for the API not having enough data for the content to actually render a meaningful UI. Also want to check configuration of new payment mechanisms.

Dan: So what is the course of action?

David: The other bit is the long list at the end of the spec.

Dan: So I believe we are pending external feedback.

David: Some of this might be helpful to get an extra pair of eyes.

Dan: Extra time? (marked for extra time and added alex)

David: Would be helpful to have Alex around for this.

Alex: I can dig up the implementation status.

ACTION: Extra time. (when? Dan to fill in blank)

### ::part and ::theme

David: this is legitimately pending external feedback.  We were expecting edits, didn't happen yet.

### Should WebRTC be SecureContext?

(rapid-fire discussion connecting to other topics)

Dan: Alex pointed out getUserMedia and rest of WebRTC are 2 things

Travis: This got spun out of WebRTC stats review.  I think it should probably be SecureContext... how do you ??? with the rest of the prerequisites for a WebRTC call.  Should those also be SecureContext?

Mike: getUserMedia still not [SecureContext]

sangwhan: implementation-wise it is

Dan: Difference between [SecureContext] in spec versus are implementations requiring secure context?  Should the TAG be pushing for [SecureContext] in the spec?

Mike: From developer perspective... if spec doesn't say [SecureContext] but if developers write to the spec...

Alex: Does anyone do that?

Travis: Will implementations adapt?  If they don't limit to secure context today, will implementations migrate their existing getUserMedia into secure context only?  If you were asking me for Edge, seems a bit risky to take it away.  Seems like it would break somebody.

Mike: Both Chrome and Firefox have done that.

Sangwhan: Safari too, only secure contexts.

Alex: [MDN page](https://developer.mozilla.org/en-US/docs/Web/Security/Secure_Contexts/features_restricted_to_secure_contexts), seems like it could use some updating.

Alex: Firefox appears to allow, only for temporary grant but not permanent grant.

Dan: Question:  Since this hasn't been requested by anyone... what's the mechanism that if we feel getUserMedia and/or uother WebRTC related specs should be marked...

Yves: we can raise an issue on their repo

Dan: ... are they receptive?

Alex: I think they will be.

Alex: We could point out that implementations vary... now a way to do this in IDL... frame it as a question as to whether group would accept the substantive change?

Mike: Talk to Dominique Hazaël-Massieux (Dom) first?

Yves: File issue first, then talk to dom?

Alex: TAG issue first, talk to Dom, then their issue?

Dan: I'll ping Dom on our issue.

Dan: Put in an extra time bucket and come back on Saturday?  Don't want to just punt to another meeting.

Yves: I'll talk to Dom this afternoon.

### Lunch

### [Well-known](https://github.com/w3ctag/design-reviews/issues/237) and [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232)

(Guest for this session: Mark Nottingham)

Discussion of whether the TAG is interested in supporting an increase in .well-known.

Mark noted that in an extreme case, any new service could be automatically configured with a .well-known.

Specifically, do we have concerns with non-web scenarios.

Alex: Do we have examples of designs that Mark has pushed back on?

Mark: There are proposals to change how browsers behavior, and even their network services... eventually folks will start deploying services on the same origin as other web content, while not understanding how the web origin security model works--and this could open them up to vulnerabilities (e.g., like XSS). Most of the folks designing these protocols don't know the Web security model very well. Worst case scenario: browsers might have to start sandboxing well-known.

Alex: Advice: if you're designing a new protocol, don't use an existing resource location. Maybe we need a new content-type?

Mark: So... don't hear major concerns about opening up .well-known; just that we think careful about the security model. Could open up the registry, and include a bunch of security considerations.

Peter: What's wrong with service records? It's hard to do a web service because the browser can't lookup the SRV record--sees this as a problem that could be solved. Ex: matrix protocol--could have used a .well-known if the browser was able to lookup a service record. (You have to type this in manually.). Summary: I'm a fan of service records--I think we should just make them work.

David: Any restrictions on what HTTP methods are used?

Mark: no.

David: So, different security considerations depending on what method is used.

Mark: Oh, BTW, Web Sockets and ?? are also using .well-known URIs. This came from the folks that wanted to map from another protocol into web sockets.

.. So, tentative conclusion: the TAG has no architectural concerns, just wants to make sure security concerns are reviewed/addressed.

Dan: Should folks in the TAG help write this? Mark: treat this feedback as preliminary, then expect a formal review later when this is more polished/ready.

Alex/Dan: The TAG is also generally available for IETF documents to use for review.

Mark: We can draft a proposal and get back to you. This issue is pretty devisive.

Dan: What to do about the open issue?

Mark: Please provide relatively short answers to the questions posed in the issue. Also note: please come back to us for spec review.

Dan: We'll take extra time to come back to that later during the F2F.

## Topic: BCP56bis @torgo (talk with mnot) (https://github.com/w3ctag/design-reviews/issues/232)

Mark: Understand the implications of using HTTP. Some foks were minting new methods,... other things that go counter to the architecture of the web. Also tends to paint themselves into a corner where they can't evolve with HTTP or exposes them to security issues. The document is meant to (in the nicest way possible) use HTTP correctly.

Section on co-existing with web browsing (more relevant to the TAG); also "application boundaries". Doc is getting close to last-call (maybe in the next few months).

Please keep in mind, it's for IETF working groups (not general). These are groups who are "charmingly new" to the web.

Dan: We need to treat this as a design review topic. I'll stay the assignee...

HTTP Extensions--would like to have "input" as it's not quite ready for review. Mostly editorial work.

Dan: OK. Will keep in mind.

## The Workshop

Dan: Had a discussion around web packaging and specifically signed exchanges. From IETF perspective--

1. Signed exchanges is a draft. Not formally considered for adoption. Lots of use cases. Lots of historical interest--won't be surprised if it gets adopted. Others have expressed concerns about sigining these exchanges. We need to talk through these concerns.

2. Big impact of adopting this tech is AMP--is seen as a replacement for AMP. Can load someone else's content from your URL. Publishers seem to have love/hate relationship with this... Maybe we need a TAG/Publishers meetup to discuss. To discuss about these big changes. If we can get publishers and folks to agree, then there will be very little reason to push back.

Dan: Agree, getting publisher's voices via a workshop would be great. Have been working to find a subject for some IAB/TAG workshop in the past--this could be it.

Alex: I was there too. A number of publishers were also there. I think it would be great to get folks together for a workshop.

Mark: Could we have a publisher host it (to help it be more successful)?

(Discussion of whether this adds to or subtracts from a goal of decentralized web.)

Hadley: I see value in getting everyone together to talk about common use cases and the impacts on the architecture of the web. At least we'd all be aware of each other's motivations.

Dan: How can we help get the workshop started?

Travis: How does the workshop timeline work with Chrome implementation plans?

Alex: Chrome is implementing (Signed Exchanges) now to understand whether the tech meets goals, etc.

Mark: Next step; whip up a doc explaining the workshop scope etc.

Dan: I'll help.

Andrew: We should ensure commercial voices from publishers are represented (not just tech leads and CTOs, but director of commercial).

Kenneth: How will Signed Exchanges deal with content take-down requests (e.g., as happens in EU - "the right to be forgotten")?

Alex: Today they will be time-limited to the duration of the exchange (7-days), but these are great questions to be brought-up and discussed in the workshop.

### Client Hints Discussion

Andrew: Are we targetting resources, or is this intended for navigations?

Alex: This is highly political at Google. Team feels politically blocked to get the data to prove that hints at navigation are useful. If we can get it shipped for resources, we can start to gather data. Concerns: total size of headers sent at every request. Don't know how much is too much. (But there's not data on how much is too much!) If folks want to use it for navigations, we it be useful to anyone.

Mark: Feel like I can gather some of that data. Confused why this is coming-up for Client-hints (vs. lots of other hints released over the years.)

Alex: Concern is with the opt-in. Sites with Latency/bandwidth constraints will view the hint as a switch to top-level responses. (Stop the guessing.) Getting that effect today requires a redirect. Debate is about whether the opt-in is meaningful.

Mark: Opt-in was originally put-in to mitigate against those who were nervous about the extra size. If you send client-hints by default, you swap from active probing to passive fingerprinting. The privacy concerns...

Alex: Re; Fingerprinting, TAG has decided this is largely not a huge problem (especially for same-origin) given the number of ways the passive fingerprinting can happen.

Mark: If you're willing to sacrifice first nav, and set a long lifetime for the hints, then ...?

Andrew: not just for big sites. If CH are for resources only, then the spec'd content works fine, but rename please!

Mark: Whether it's used for nav is for HTML to decide...

Alex: We're talking about what we send on the navigation. We would like to.

Mark: Well, then we come back to the privacy discussion.

Alex: Have a write-up planned with the feedback.

Mark: If the TAG were to send it... IETF doesn't have a lot of respect for the larger institution... personal engagements in Github issues may be the best place to engage.

Andrew: I think two ways to go with this. Either "its resources", or we will expand to generic framework for all navigations.

Dan: If we go to extra time, could we get something written-up for this?

## CSP + &lt;link rel=prefetch>

Andrew: [Recent post](https://hackernoon.com/im-harvesting-credit-card-numbers-and-passwords-from-your-site-here-s-how-9a8cb347c5b5) about how "I can steal your passwords". One of the workaround approaches is to use link rel=prefetch to get around CSP! Didn't see if this was mitigated.

Alex: Note [here](https://w3c.github.io/webappsec-csp/#directive-prefetch-src) that there's a directive... (preload is excluded, but prefetch is covered.) prefetch is covered.

Alex: rel=preload as=script covers it.

So... it looks like this hole is plugged!

Alex: Was fixed quickly: https://groups.google.com/a/chromium.org/forum/#!topic/Blink-dev/By3kslc6g1M

All: Mike is amazing.

Hadley: Yoav also points out this issue in webappsec: https://github.com/w3c/webappsec-csp/issues/107

## WHATWG Stuff

Mike Smith TM: Still seems likely that W3C will publish a DOM and HTML spec. (Probably not the rest of the specs.)

Dan: Will the process change?

MS(TM): Problem for our editors. W3C specs are not as up-to-date. Is a real problem for work happening in other groups. Bad for broken references. Hope the W3C version is kept up-to-date. 2012-2015 the docs were up-to-date, but after that no... Is the TAG aware of this?

Dan: 2 thinks: 1) does W3C still have a version of HTML? 2) Other specs that refer to HTML? What stops Mike from changing his refs to WHATWG specs? Can't W3C reference other specs (see Fetch).

MS(TM): Perception problem? Bottom line--creates problems for folks like Mike West to get specs done. If W3C changed normative reference policy, then problem would go away.

Alex: would like the TAG to not get involved, as this seems more relevant to the W3C Team and WHATWG SG to work-out.

MS(TM): Ideally, there is an up-to-date copy of W3C HTML/DOM that reflects what is real and referenceable.

## Signed Exchanges @slightlyoff

Alex: happy with this feature!

Travis: I'd like to review

Peter: I have some questions about cert revocation...

Alex: Take a look a sections 4 & 5--it might have an answer to your questions.

## DOM/HTML Reviews

Travis: Let's have extra time for these. I also will split the issue tonight and mark the derivative issues with 'extra time'.

## [Web Components Guidelines Doc](https://github.com/w3ctag/design-reviews/issues/227)? @torgo

Dan: Kenneth, interested in authoring?

David: Who's the target audience?

Kenneth: Web developers? We need a set of questions--what do folks want answered?

Sangwhan: We don't do a good job of keeping docs up-to-date. Maybe we should try to put it onto MDN at the end-of-the-day. (Then it looks like a community-owned document rather than a TAG-owned.)

David: the guidance might be wider than just web-components--could be helpful to discuss how to build a polyfill for a feature destined for standardization.

Alex: still struggling to understand how we (the TAG) can make a meaninful contribution here.

Kenneth: Added a bit of resources to https://github.com/w3ctag/design-reviews/issues/227

## CSS Layout API In Progress @dbaron @torgo @travisleithead

Travis: I have some review feedback to post into the issue.

## CSS Selectors 4 In Progress @dbaron

Discussed the :something proposal--TAG is generally happy with this (doesn't think it's worth changing). Also grudging happy about column selectors being a pipe '||'.

Alex: Will write up our conclusions and close the issue.

## Web Locks API @dbaron @triblondon

David: our feedback in the issue resulted in a spin-off issue being filed.  https://github.com/inexorabletash/web-locks/issues/35  We should probably respond to some of the comments there, feels like some of our commments may have been misunderstood.

Peter: taking to extra time.

## &lt;link> rel="modulepreload" @slightlyoff @triblondon

Peter: sending this to extra time.

## Transform Streams In Progress @cynthia @slightlyoff @dbaron

Travis: Generally happy with this.

Sangwhan: Yeah, had some original feedback around tee(), but given where we are it seems fine with me now.

Travis: These Streams are low-level. Could be used to implement something like web audio on top of this.

Alex: But it will be on the main thread - not worklets.

Travis: We could supply this as a future direction to take Streams.

Alex: Wrote up our feedback and closed the issue.

## ads.txt @slightlyoff

Alex: no updates; will checkin with George.

## Intersection Observer review @slightlyoff @dbaron

David: Not much to discuss here, since no progress on the existing issues. But I do want to keep it open.

Peter: move to next F2f.

## ReportingObserver @cynthia @slightlyoff

Peter: they still have a bunch of open issues.

Travis: Let's loopback in a month; will give me time to follow-up on the individual issues.

## Review request for ResizeObserver @slightlyoff @dbaron

Peter: I still have concerns around the lack of fragmented layout boxes in this API.

David: It might be useful to offer suggestions about how to structure the API in a way that will make it work for fragments but at the same time not complicate the API for users who aren't dealing with fragments.

## Secure Contexts - in Design Principles

Reviewing Pros/Cons of existing PR.

Can't seem to get consensus on whether using SecureContext as a carrot for HTTPS is something everyone in the room can get behind.

Alex: I propose we look for a different way of framing this.

Potential draft content:

> Should your feature be enabled only in a [SecureContext]?
>
> It may save you significant time and effort to pre-emptively restrict your feature to Secure Contexts.
>
> The TAG is on the record in supporting an industry-wide move to [Secure the Web](https://www.w3.org/2001/tag/doc/web-https) and applaud [efforts](https://blog.mozilla.org/security/2017/01/20/communicating-the-dangers-of-non-secure-http/) to shift web traffic to secure connections. A great deal of effort has gone into debating which features should be restricted to [Secure Contexts](https://w3c.github.io/webappsec-secure-contexts/). Opinions vary amongst engine vendors, leading to difficult choices for feature designers. Some vendors require _all_ new features be restricted this way, whereas others take a more selective approach.
>
> This backdrop makes it difficult to provide advice about the extent to which your feature should be restricted. What we _can_ highlight is that Secure Context-restricted features face the least friction in gaining wide adoption amongst these varying regimes.

David: I would like to 3rd, 5th, 6th paragraphs of the current PR, covering advice on how to limit features, making sure feature detection works right, and still giving strong advice about features with privacy/security risks.

Sangwhan: If feature A, you depend on, depends on [SecureContext], then you could be in trouble. (May be worth making in the above draft.)

Open issues:
* Review of signature-based resource loading restrictions. @cynthia @hadleybeeman @plinss
* Review OffscreenCanvas, including ImageBitmapRenderingContext @cynthia @dbaron @travisleithead
* Review Accessibility Object Model @cynthia @travisleithead (if alice responds)
* "With Credentials" flag possibly inconsistent with web architecture @dbaron
* Task Scheduling

### Break

### Signed Exchanges
