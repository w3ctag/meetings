## TAG Teleconferences
##### 13-15 January 2020

---

### Agenda:

### Breakout A (Europe / US) - [2020-01-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200113T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris
* [Event-Level Click Conversion Measurement API](https://github.com/w3ctag/design-reviews/issues/418) - @hober, @torgo, @hadleybeeman, @lknik

### Breakout B (US / APAC) - [2020-01-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200113T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) - @hober, @cynthia, @dbaron
* [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris

### Breakout C (APAC / Europe) - [2020-01-14](https://www.timeanddate.com/worldclock/converter.html?iso=20200114T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @alice, @torgo, @ylafon

### Plenary Session - [2020-01-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200115T210000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

-----

### Breakout A

Present: Lukasz, Tess

Regrets: Dan, David, Kenneth

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Did not discuss; regrets from all assignees.

#### [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris

Did not discuss; regrets from all assignees.

#### [Event-Level Click Conversion Measurement API](https://github.com/w3ctag/design-reviews/issues/418) - @hober, @torgo, @hadleybeeman, @lknik

Lukasz: It looks like the Apple folk and the Google folk are working together on layering their APIs (and that's great because there won't be two specs to solve roughly the same problem space, which is kind of better for the web platform); can we close this?

Tess: Closing is okay. I'd like to encourage them to come back to us when they've makde more progress on the layering with PCM; it'll be more meaningful to evaluate it then.

### Breakout B

Present: Alice, Sangwhan, Tess, David

Regrets:

#### [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) - @hober, @cynthia, @dbaron

Sangwhan: I think we can close this?

Tess: We've been waiting to hear back since early 2019... coming up on a year pending feedback. Don't think we should keep it open indefinitely.

Sangwhan: That's my take as well.

David: I think that's reasonable. Do we want to express any opinion on the issue before we close it?

Sanwhan: We should report the two [feature requests](https://github.com/w3ctag/design-reviews/issues/213#issuecomment-494788291) somewhere.

... I filed a comment asking where to file the two feature requests.

Alice: I also filed an [issue](https://github.com/w3ctag/process/issues/1) on our process repo about what to do in cases like this.

David: I think maybe an issue against fetch, and an issue against HTML.

#### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris

Sangwhan: Not much to say on this one.

David: We commented on this at our f2fs last year.

Sangwhan: What is the shipping status?

Alice: [In development](https://www.chromestatus.com/feature/6031161734201344).

Tess: Do we need time to generate more feedback?

Sangwhan: Seems premature to close this... but if we're not going to provide any useful feedback, we might as well.

David: Looks like the explainer might have been updated... not clear how experimental this is and at what point we are going to expect a spec which would allow interoperability. We would want a spec by the time we're shipping, and I'm not sure where this is on that path.

... Worth taking another look.

Alice: Bumped out to week of 3 February.

### Breakout C

Present: Alice, Kenneth, Yves

Regrets: Dan, Sangwhan, Hadley

#### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon

Kenneth: Looks like no update since December...

Yves: Could use the constructor to scan hosts and ports. Might want to return (?) an object in a promise so it can check if it's allowed or not...

Kenneth: Did you leave that feedback somewhere? I just added the Pending External Feedback label.

Yves: I will add that.

Kenneth: David asked about handling consent to communicate in his [comment](https://github.com/w3ctag/design-reviews/issues/389#issuecomment-561365768). Might need to bring someone on to a call...

Yves: Perhaps we could ask David to invite someone from Mozilla...

Kenneth: Seems to be a pretty fundamental technology as well, definitely want the right people looking at this.

Yves: We need more expert review on this. 

Alice: How...

Yves: Would be good to have Dan weigh in on whether to use plenary time for this. I'll talk to Dan about how to organise that.

Kenneth: Only three examples in the spec... and they're actually very similar. Oh.. there's more in the explainer.

... APIs on the web don't really fit together... mediaSource, they have to wrap everything in promises.

Yves: There's an existing [issue](https://github.com/WICG/web-transport/issues/13) regarding violation of same-origin policy.

#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

Alice: Bumped a week since Sangwhan sent apologies

#### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @alice, @torgo, @ylafon

Alice: This has been open a long time. I am extremely confused by it.

Kenneth: It's not really a W3C spec either.

Alice: I suggest we ask Dan in the plenary what he'd like to happen with this.

Yves: Agreed, I would ideally like to close it.

Kenneth: Is anybody using this today? Could we propose something else? If people are already using this, is there anything we can do?

Yves: The issue notes that Alex and Andrew have previously contacted the IAB, but neither of them are still involved with TAG.

Kenneth: Might also be worth reaching out to Alex to see who he contacted within Google. If nobody is using it it's not relevant, would be nice to know who is using it and whether we have contacts to affect usage before we spend more time on it.

### Plenary Session

Present: Lukasz, Kenneth, Rossen, Tess, Yves, Hadley, Peter, David

Regrets: Sangwhan, Dan, Alice

Scribe: David (sort of!)

#### Readouts from breakouts (summarizing minutes above)

Peter: let's bump #201 to next week, hopefully Dan can make it

#### Triage

##### [WebXR Augmented Reality Module](https://github.com/w3ctag/design-reviews/issues/462)

David: I guess this isn't the part that has things like pupillary distance and eye tracking.

Kenneth: Seems like this explainer could better explain the use cases.

Assigning Dan (in absentia), David, Hadley, Rossen

##### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463)

Tess: Are we going to define hit testing in XR before in the rest of the platform?

Tess: I wonder if we should be figuring out how to expose hit testing more generally and then figure out how to apply it in XR

Assigning Tess and David

##### [Origin Isolation](https://github.com/w3ctag/design-reviews/issues/464)

Tess: assign me

Hadley: and me

Rossen: and me

David: some ties to Spectre mitigation

Peter and others discuss milestones for issues



