## TAG Teleconference
##### 01 May 2019

Present: Lukasz, Tess, Dan, David, Peter, Alice, Sangwhan

Regrets: Hadley, Kenneth, Yves

Scribe: David

---

Agenda:

* [LazyLoad (loading= attribute)](https://github.com/w3ctag/design-reviews/issues/361) - @hober, @cynthia
* [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris
* [Autoplay Detection API](https://github.com/w3ctag/design-reviews/issues/356) - @hober, @hadleybeeman
* [Backdrop Filter](https://github.com/w3ctag/design-reviews/issues/353) - @hober
* [Subresource prefetching+loading via Signed HTTP Exchange](https://github.com/w3ctag/design-reviews/issues/352) - @torgo, @hadleybeeman
* [Alternative Text for CSS Generated Content](https://github.com/w3ctag/design-reviews/issues/351) - @alice
* [CSS Animation Worklet API](https://github.com/w3ctag/design-reviews/issues/349) - @hober
* [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @alice
* [Web Publications review](https://github.com/w3ctag/design-reviews/issues/344) - @dbaron, @torgo, @hadleybeeman
* [Verifiable Credentials Data Model 1.0](https://github.com/w3ctag/design-reviews/issues/343) - @hadleybeeman
* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @dbaron, @torgo, @lknik
* [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice
* [WebRTC DSCP Control API](https://github.com/w3ctag/design-reviews/issues/325) - @hober, @cynthia, @torgo
* [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @hober, @dbaron
* [EME Extension: HDCP Policy Check](https://github.com/w3ctag/design-reviews/issues/323) - @hober, @cynthia
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman
* [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240) - @cynthia, @hadleybeeman, @plinss
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @slightlyoff, @hadleybeeman, @travisleithead, @plinss
* [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) - @dbaron

---

## Design reviews

### [LazyLoad (loading= attribute)](https://github.com/w3ctag/design-reviews/issues/361) - @hober, @cynthia

will postpone to another time

### [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

Pending external feedback.

### [Autoplay Detection API](https://github.com/w3ctag/design-reviews/issues/356) - @hober, @hadleybeeman

Tess: A few days ago Peter suggested drafting a reply in-channel to get async consensus.  I posted it today, so there's a draft reply in Slack.  It looks like several of you have commented; I should revise accordingly before signoff.

Tess: It's long.  I was considering separating out the tactical advice that is neither technical nor procedural.

Dan: Feels like something that ought to go to WICG chairs.

Tess: I was there, and we didn't ask the chairs.  In this write-up I ask if they did-- although I know they didn't.  Need to reword this to be clearer.

Dan: Collective we...

Tess: So not entirely sure about this feedback coming from me, but maybe I should get over it.

Alice: You have some context as to why the WICG chairs weren't involved.

Tess: I don't think it even occurred to anyone.  That's not how things work in WICG.

Alice: Maybe reword as "like you, it didn't occur to me there, but..."

Tess: yeah, that sounds good

Tess: So hopefully a bit of tweaking and can resolve async in channel with a 24 hour window or something.

Dan: Yeah, don't need to wait until next week's call.  Unless there are other objections.

Alice: I wrote a quick comment in Slack -- I don't have full context but I got some offline -- but it seems to me that they've expressed some frustration that other browsers are saying "we can implement this as synchronous" whereas unwillingness to do so is being read as arbitrary whereas it's not.

Tess: they had a clear technical rationale.

Alice: I think they haven't done a clear job of communicating the cost to users in the Chrome implementation of it being synchronous.  (Priority of constituencies.)  They conveyed to me, vaguely, that there's a cost to users.

Tess: Recollection: cost to users that's a consequence of design decisions that were implementation details that weren't necessary to the feature.

Alice: Though those aren't arbitrary.  Reasons that seem important to them to design it that way.

Dan: Is there a disagreement about who the users are in this discussion?

Tess: I don't think so.  People looking at websites.

Dan: OK, will revisit on next call.

### [Backdrop Filter](https://github.com/w3ctag/design-reviews/issues/353) - @hober

Tess: Bump this.  I was in Toronto for other face-to-face.

Dan: 1 week or 2 or face-to-face?

Tess: 1.  Feeling ambitious.

### [Subresource prefetching+loading via Signed HTTP Exchange](https://github.com/w3ctag/design-reviews/issues/352) - @torgo, @hadleybeeman

Dan: I haven't looked at it.  Bump to next week.

### [Alternative Text for CSS Generated Content](https://github.com/w3ctag/design-reviews/issues/351) - @alice

Alice: Was just chatting with Sangwhan in Slack.  I filed this review, so it sounds good to me, of course.  Sangwhan had some good points.  I think it's OK the way it is.  This went through quite a bit of discussion in CSS WG.  The proposal is to, in a `content` property you can have a trailing slash following by a string, that will be treated as the alt text for the content where it at applies.  Could be an element or a pseudo element, but with different rules.  Sangwhan was proposing that wrapping the alt text in `alt()` would make it more readable; like James Craig's proposal.

Sangwhan: My feedback would be as somebody who inherited code.  Not obvious what it does with the `/` syntax; `alt()` would be much more obvious.  James Craig raised a background compatibility issue.  Peter, were you involved?

Peter: nothing significant to add

Dan: I haven't been involved in this work.  Coming into it... haven't been involved in the review.  I'm sure it's been discussed already.  Doesn't this break the model where we have separation of content and presentation?

Alice: This is the fourth time I've had this conversation.

Dan: Maybe a couple sentences in the TAG review / minutes?

Alice: What I wrote:  Anne filed a meta-issue about separation of style and content.  I  think it's a false dichotomy that accessibility tree, find-in-page, etc.  [PASTE THIS IN LATER]

Alice: There's another issue on AOM... looking at standardizing how accessibility tree gets built.  DOM semantics aren't the same as accessibility semantics.  We prioritize keeping the a11y tree semantics as close to the default UI semantics as we feasibly can, with caveats where certain things don't map onto the AT paradigm.  DOM semantics can provide good signal to intended semantics

Dan: [back to the order of constituents] the needs of the user outweigh ideological purity

David: separation was broken when `content` was created.  (Was intended for limited use.)

Sangwhan: The unfortunate reality is that there is a lot of content out there that uses this, which isn't accessible. This is a bug fix for that.

Dan: so are we done?

Alice: Sangwhan, Do you want to leave your feedback?  I agree that `alt()` syntax would look nicer.  My inclination would be to take that back to CSS WG and see what they say.

Sangwhan: I think I should just at least write formal feedback on this, and then I'll do that.

Dan: close issue, or pending external feedback?

Sangwhan: I'll mark it pending after I write the content.

Alice: pending feedback from whom, CSS Working Group?

Sangwhan: yes

Dan: I'll set milestone to face-to-face.

---

Lukasz: Question about alternative text for accessibility.  If it's intended for screenreaders if no image is being displayed, would you consider the image still be downloaded?

Alice: 

Lukasz: Is it just a matter of display and the content is being downloaded regardless?  It's a text to replace the image if one is using screenreader.

Alice: Your Concern about checking whether the image has been downloaded or not?

Lukasz: Is there established practice here that you're aware of?

Alice: In Chrome, typically, running assistive technology doesn't have any impact on whether images are downloaded or not.  You could (if we still have a setting) turn off download of images, but we don't have any branching for how the page is rendered.  The only thing that branches is whether we compute the a11y tree.

Lukasz: If someone wants to optimize things for screenreaders.  If someone optimizes away then someone can see that user is using screenreader.  Maybe spec should have a tip that this shouldn't be the case.

Alice: My hesitation is that most UAs would work this way anyway.  If someone is using assistive technology we don't know why they're using it.  They might see the screen but be using the accessibility infrastructure to run an input device.  And there are screenreader users who are sighted as well; they might be able to see the image but not be able to read text well.  Most user agents would be building for those use cases so there wouldn't be a risk that they would try to optimize downloads like that.

Lukasz: If this is so complex, how does the screenreader decide when to ... never mind about that?

Lukasz: Should I write a comment in the github and ask about it?

Alice: Sure... worst case we can reply on the github issue to explain the situation in case someone else comes across it.

Sangwhan: I don't think this particular issue is affected.

Alice: We can have this discussion in the github issue so it can be captured.

### [CSS Animation Worklet API](https://github.com/w3ctag/design-reviews/issues/349) - @hober

Tess: bump a week, please

### [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @alice

Alice: I had a read through it.  I read through the issue thread as well.  Anne had some questions about interaction with shadow dom, and some questions about the implementability of the spec.  Does anyone else have context on pointer events?

David: IIRC, multitouch was original motivation.  Redesign mouse events with knowledge that multitouch exists.

Sangwhan: competing with touch events, but it has issues.  So we have 3 different things to capture pointer input.

Dan: Many loud advocates for pointer events approach that want it implemented more widely.

Alice: So, this didn't have an explainer.  Looked at the demo, didn't have explanation.  Was a bit frustrating.  It adds some APIs into the `PointerEvent` interface:  `getCoalescedEvents` and `getPredictedEvents`.  I don't know what predicted events are...

Dan: Maybe we should just push back that there's no explainer; we should ask for that before we do a review.

Alice: Open questions:  what are predicted events for?  (second question missed)  Plus Anne's comments about implementability of the spec.

Alice: OK, I can comment with that.

(digression about knowing who's commenting on the issues)

(Lukasz leaves)

Sangwhan: I can see if I can disambiguate this -- been a long time since I touched pointer events in Presto.

Dan: Co-owner of issue with Alice?

Sangwhan: I can.

Dan: Postpone to when?

Sangwhan: This was expedited... so next week if possible?  If Alice has time I could set up a separate call this week or next to discuss this.

Alice: next would be good

Dan: So next week, but bump to later if you want to.

### [Web Publications review](https://github.com/w3ctag/design-reviews/issues/344) - @dbaron, @torgo, @hadleybeeman

David: Read explainer, use cases and spec, probably in that order.
Use cases document seemed scary. But then the spec seemed much less scary.
So perhaps the use cases document should be revised? Perhaps not?

David: The concept of a canonical identifier was interesting. Might not be the URL from which you're accessing it. Quasi URN type thing but they're using a URL. 

David: Use of JSON-LD - may be interpreted as JSON or may be ... processed into a graph? Would like to be explicit that it's intended to be read purely as JSON.

Dan: Where is this comment?

David: In the 3rd paragraph in the long comment, and the third bullet point in my earlier comment.

Dan: I need to catch up on your comments.

Tess: I read it on a plane, and my impression was that it was very thorough.

David: I disliked their use of WebIDL's `partial` everywhere, and I don't think I like `partial` in general because it's like a `goto` but in reverse.

Tess: Yeah it's more or less a syntactic sigil that you're doing monkeypatching.

David: In each section they monkeypatch the previous section.

Dan: Need to message Hadley since she's on the issue as well. Seems like we may be almost ready to close this off.

David: They wished to have comments in advance of their f2f which is next Monday and Tuesday.

Dan: Well, we have left comments. We should leave additional comments individually if we have them. Let's revisit on the 8th and see whether anything comes back from them as a result of the f2f.

David: I should also file an issue with them.

Dan: Marking as pending external feedback.

### [Verifiable Credentials Data Model 1.0](https://github.com/w3ctag/design-reviews/issues/343) - @hadleybeeman

Dan: I'll move this to next week.

### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @dbaron, @torgo, @lknik

Lukasz (in minutes before he left): [MW](https://github.com/w3ctag/design-reviews/issues/342#issuecomment-484487107)'s reply on GH looks good to me.

Dan: David, have you read mike's comment?

David: not yet

Dan: move to face-to-face; Mike is joining us there.

### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron

Dan: bigger issue rather than review?

Sangwhan: I'd be happy to kick to face-to-face.

Dan: How should we structure?  Bring in people who are working in the feature policy space?  Facilitate a discussion between us and Andrew and others?  These issues still seem to be quite open.

Sangwhan: I think I need to digest the potential of what is currently shipped and get myself filled in on background, and then involve other people.

David: Also related to an issue we have elsewhere, maybe design-principles, about six different mechanisms for blocking stuff.

David: Maybe need work before the face-to-face if it's going to be useful -- need to figure out how.

Dan: I'm commenting on the issue.

Dan: Will bump a week.  Let us know if you have ideas about how to structure discussion.  This isn't a review in that sense, but feels like something we ought to be paying attention to.

---

Alice: Does it feel like something that could feed into design principles doc?  Would be *very* specific.

Tess: definitely

Tess: feature policy is a client api, naming is part of good api design.  One of issues here about how weird the naming is.  There's a broader question about design of the feature in the future.

David: I don't feel like it's too specific for design-principles doc.  Would be good if other spec bits link to it.

Tess: There's a separate doc about promises.  We don't have a separate thing for the things you should think about when designing a feature policy; it should go in the catch all.

## Other business?

Dan: Anything we can deal with quickly?

Sangwhan: Also, meta question, what if person who raises issue never gets back to us, e.g., in 323 (HDCP Policy Check).

Dan: We should have a policy.  Could be part of our discussion of how we work and what we could do better; definitely something we cover at face-to-face.  On this particular topic, could write a note:  if you don't have feedback on this, we could close it, but not a successful review.  The issue they raised (their #7) doesn't have anything in it whatsoever.

Sangwhan: can we close with a specific label?

Alice: I can follow up, and we can close if we haven't heard anything by next week?

Dan: put this in an "at risk" status.  We can discuss these at the face-to-face.  Are we spending more time thinking about this topic than they are?  I'll set this to next week for now, can see if we can close for next week.

Alice: Are we capturing this type of meta-issue somewhere?

Tess: On previous topic on this call, autoplay stuff, I raised meta concern in design-reviews repo.  Any reason not to open meta issue?

Dan: Maybe start adding to agenda document for face-to-face?

Dan: If we wanted issues opened up, we could open them in the meetings repo.

Dan: But to David's point, we could just (Dan makes editing sounds) start adding items into README.md as items that we want to tackle.  Either place would be a good place to leave things.

## Issues we didn't get to
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice
* [WebRTC DSCP Control API](https://github.com/w3ctag/design-reviews/issues/325) - @hober, @cynthia, @torgo
* [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @hober, @dbaron
* [EME Extension: HDCP Policy Check](https://github.com/w3ctag/design-reviews/issues/323) - @hober, @cynthia
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman
* [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240) - @cynthia, @hadleybeeman, @plinss
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @slightlyoff, @hadleybeeman, @travisleithead, @plinss
* [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) - @dbaron

* [LazyLoad (loading= attribute)](https://github.com/w3ctag/design-reviews/issues/361) - @hober, @cynthia
* [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

