## TAG Teleconference
##### 20 March 2018

Present: Peter, Dan, David, Sangwhan, Yves

Regrets: Andrew, Hadley

Scribe: Sangwhan

---

(Dan giving short update about IETF101. And packaging.)

## Agenda:

### [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - David

Alex: David and I am supposed to have a call later with Matt

David: Beginning of next week it seems.

ACTION: Bumped to next teleconference.

### [Img decoding attribute](https://github.com/w3ctag/design-reviews/issues/220) - David, Sangwhan

Sangwhan: Bottom line is I don't have any better proposal.
Some bits in the original discussion seem to have fell threw the cracks,
which I plan to look into. I'd like feedback from the other reviewers.

David: Don't have anything better at the moment.

Sangwhan: The way this is supposed to work in cases of decoded buffer eviction
is a bit unclear. I'd like to see that done better.

David: I'm supposing that you call decode() every time you need the image.

ACTION: Sangwhan to comb through the discussion and while issues on whatwg/html.

### [HTML General Review](https://github.com/w3ctag/design-reviews/issues/174) - Travis

Peter: Travis isn't here, so let's punt.

(Travis joins.)

Travis: I have been making progress. Especially on how to subdivide it into
chunks that can be reviewed by multiple people. Assumption is that larger test
suites mean more complexity - so far 25 review sections. Some sections are
pretty big - but I think I might have something to share pretty soon. Might grow
into more reviews - will share draft when I have the first draft.

ACTION: Travis to finish and share.

### [Vehicle Information Service Specification](https://github.com/w3ctag/design-reviews/issues/234) - Hadley

Peter: Hadley isn't here, so let's punt.

### [CSS Selectors 4 :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - David

(David is frozen on Jitsi. We love WebRTC.)

David: I raised the question of whether the spec is detailed enough for
conformance requirements, and the feedback was it might not be - whether
we should leave our issue open or not is unclear.

Peter: We should mark as pending.

ACTION: Revisit during F2F.

### [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232) - Dan

Dan: Not much done yet.

ACTION: Punt for two weeks. Face to face.

### [CSS ::part and ::theme pseudo elements](https://github.com/w3ctag/design-reviews/issues/230) - David

David: Feedback was given 1.5 months ago, then there was discussion on their
side and corresponding changes, which I haven't looked at yet. Suggest we delay
until next week.

ACTION: Revisit next week.

### [W3C DOM](https://github.com/w3ctag/design-reviews/issues/229) - Dan

Dan: There is a change log [here](https://w3c.github.io/dom/#historical),
so we can start from this. Would like to have a breakout on this. The question
is what technical feedback we have.

Dan: Maybe we should have some people do a first pass on this.

Sangwhan: I can volunteer.

Travis: Likewise.

ACTION: Travis and Sangwhan to take a first pass review, possibly revisit during F2F.

### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - Alex

(Alex is having connectivity issues. To be revisited.)

### [ResizeObserver](https://github.com/w3ctag/design-reviews/issues/187) - Alex, David

David: Not much progress on this, unfortunately.

ACTION: Revisit next week.

### [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101) - Hadley, Lukasz

Lukasz: let's simply publish the Findings asap.

ACTION: As noted above.

### ["With Credentials"](https://github.com/w3ctag/design-reviews/issues/76) - David

Travis: Where are we on this?

David: I need to talk to Yves about this.

Travis: Any other feedback on this since January 31?

David: To some extent.

Yves: I'll contact you about this.

ACTION: Revisit during F2F.

---

## Backlog:

### [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Alex / Hadley, Travis, Peter

Travis: Just as a FYI, it's now called WebXR. The one bit is that there is
discussion on making a extended or better gamepad API for new types of
controllers.

Dan: Is this extending on the original gamepad API?

Travis: The last time I discussed this it seemed like that the gamepad API
wasn't great - and needed to be reworked. There is room for building something
that isn't just an array of buttons. Not sure who is the best to do this.

Dan: My concern is that WebXR shouldn't be working on their own gamepad API.

Travis: I agree. The new gamepad API shouldn't be explicitly for just WebXR.

Yves: Would it make sense for the TAG to look into the current specs and try
to find what the common ground is, and what is missing on either side?

Travis: I think that should be something we should be looking into, rather than
chase the rAF bunny.

Yves: Maybe look at this during on the F2F?

Sangwhan: I can volunteer to look into this before the F2F.

Travis: I think I should file some spin-off issues and get the official feedback
back back to the WebXR people, unless anyone else sees other issues worth mentioning
missing.

ACTION: Travis to clean-up and follow-up on this.

### [OffscreenCanvas](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan, David, Travis

Travis: To be taken care of as part of the HTML breakout. It's part of canvas in
that review.

David: Looks like most of the recent discussion was about rAF and related topics.
We said we'd come back to this, but I don't remember what we wanted to say.

Travis: I think I should take a look at this.

ACTION: Discuss during F2F after second pass review.

### [Review Accessibility Object Model ](https://github.com/w3ctag/design-reviews/issues/134) - Sangwhan, Travis

Sangwhan: We should have sent and email to Alice about this, which we didn't.

Travis: Alice I believe is in .au so might be good to try having her dial in during the Tokyo F2F.

Sangwhan: +1

ACTION: Sangwhan to set reminder and follow-up.

### [&lt;link&gt; rel=modulepreload](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew

(Missing reviewers, punt)

### [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/213) - Andrew

(Missing reviewer, punt)

* [Decentralized Identifiers](https://github.com/w3ctag/design-reviews/issues/216) - Hadley

(Missing reviewer, punt)

* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) - Hadley, Travis

Travis: We were curious whether we should move this into incubation or do something else. Will have to read the notes.

ACTION: Travis to follow-up.

* [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David

Sangwhan: Nothing from me. :-(

Peter: Chrome has a I2S. Note here for Alex to write more feedback.

ACTION: Revisit next week.

* [import.meta.url and import.meta](https://github.com/w3ctag/design-reviews/issues/208) - Alex

(Missing reviewer, punt)

## Triage:

### [Find-in-page APIs](https://github.com/w3ctag/design-reviews/issues/236)

Travis: This has been tried before. Shepazu tried this before.

Dan: How can we make the in-browser find work more like an application find feature?

Sangwhan: Possibly pass a search intent to the application?

David: I'm concerned that the first use case for this would be to disable search..

Travis: The use cases listed in the explainer look valid, and stuff that is already
happening. Isn't this already possible?

Sangwhan: Think I've seen this behavior somewhere..

ACTION: Dan, Travis, Sangwhan to do a first pass review on this. To be discussed after the F2F.
