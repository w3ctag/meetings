## TAG Teleconference
##### 17 April 2019

Present: Tess, Lukasz, David, Daniel, Hadley, Peter, Sangwhan

Guest: szager

Regrets: Alice, Kenneth

---

Agenda:

* [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) - @slightlyoff, @dbaron
* Iceland Dev Event Update
* Triage some new issues
* [tilt, pan, zoom, etc..](https://github.com/w3ctag/design-reviews/issues/358) - @kenchris  
* [Audiobooks](https://github.com/w3ctag/design-reviews/issues/345) - @hober, @cynthia, @dbaron
* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @dbaron, @torgo, @lknik

* [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo
* [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @travisleithead, @plinss
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @torgo, @hadleybeeman
* [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @slightlyoff, @torgo, @ylafon
* [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) - @dbaron
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) - @hober

---

### [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) - @slightlyoff, @dbaron

David: recounts the issue including Mozilla's standards position

Dan: Interop diversity is important.

Tess: I can't think of additional areas besides ink overflow for this specific case

Stefan: i made it an up or down flag because I didn't want to get into issues of measurement too much...

David: boolean design will be better... 

Stefan: we can define ink overflow better - that would be a good thing.

David: that would be a good thing. There is interop risk - and value in fixing one piece of the foundation.

Stefan: we have shipped it in chrome and i am working out bugs in the implementation - it's intented to be used in the security setting i am discouraging people to rely on it until kinks are worked out. Intention is that this is used very narrowly unline v1. Some time until we see sites using it - and relying on it as a "golden signal" - so some runway to do the ink overflow spec.

David: sounds great.


### Iceland Dev Event Update

Torgo: I've been working with Vivaldi, and we've got 10 or so registrants so far. We need to do some outreach. we have one lightning speaker from Vivaldi, and I want to have three more from the community. 

...I've put it on the 21st, the first night. So it's out of the way, then we can spend the second and third day in the context of whatever we learn.


### Triage some new issues and issues without milestones

#### [MediaStream Image Capture API Pan/Tilt feature](https://github.com/w3ctag/design-reviews/issues/358)

Torgo: Kenneth, the thing you brought up... The Tilt Feature? Want to explain this to us?

Sangwhan: This isn't high priority for us, except that Blink intent to ship is delayed for our trip. But they do intend to implement and ship at the same time which is unusual.

...This is an extra capabiltity for webcam control -- rotate it, point to an object you want to focus on. Thus far, it's been proprietary APIs in Chrome. 

...This is the first time we've introduced something something that physically moves into the web access

Torgo: moves and sees

Sangwhan: it does require you to grant access to the camera though. Which I think is good.

...They use slightly strange units, for reason. Arc-seconds, which is what UBC uses. But on Windows, half APIs are degrees based and half are seconds-based. 

...Do we have plans to add more things that rotate into the platform? And are they okay with arc-seconds?

David: CSS has multiple angle units (e.g., for transform, radial gradients) and none of them are arc-seconds.

Torgo: Where is this? a PR on media capture API?

Sangwhan: Yeah.

Torgo: but this has been merged in the actual draft version?

Sangwhan: I believe so 

Torgo: I just want to make sure this isn't only in a googe doc somewhere that we don't have access to

Sangwhan: No, it's been added to media capture.

Torgo:  okay. Did you get a response about units?

Sangwhan: I understand wh ythey're doing this. it's because of rounding error potentials if you're using larger units. I think it's fine, but I don't think anything else on the web platform uses it.

...But given that the other things that also rotate are servo motors, I thin kthis is a good compromise.

DAvid: This ought to be designed so the capabilites of hte hw can change. today, the cameras in the laptop basically point straight ahead. But in the future they may rotate...
and people will want permission to rotate it.

Torgo:  I just saw a device with a camera that has the same housing, with a camera that flips from looking at you and looking away. Could be a privacy issue, "I granted you permission to see me, but not the room that I'm in". but if the remote user can tell the camera to move around... normally that's under user control. That seems like it would go against user expectation.

sangwhan: re david's question re extensibility... the constraint is an object.

Re privacy concerns... yeah

David: More... could permission prompts be added without breaking it. In other words, if it has to be synchronous without a prompt it nthe middle...I'll comment in the issue

Torgo: i'll add my privacy concern there

sangwhan: applied constraints does the rotation. and it is asych and uses a promise. Could have a permission, but isn't in the spec now. 

Torgo: feels to me like it should be possible for implementations to add a permission where it fits the use case

sangwhan: it could look at hte constraints being passed over and say "these are dangerous". But that's later; it's not possible now.

...Add me to it.

This is being implemented by Intel.

Torgo: I'll put you and Kenneth on it. Let's come back to it on the 24th

Peter: this is only part of hte image capture? So if you have a video stream and you're just trying to get control of tilt for an image capture to take a high res photo in the middle of a stream... what does it mean?

sangwhan: you'll have to set it twice.

Peter: so there's no way of moving the camera as part of a regular RTC stream without taking a photo?

sanghwan: you'd have to set up the RTC stream first

Peter: right, but can I move the camera without grabbing the image?

sanghwan it's on the video track, actually. that correcsponds to the device, and you add the constraint to the track.

(Assigning the rest of the new issues to TAG members)

#### Our work mode

Torgo: by the way, I'd like to spend half a day in Rekjevik on how we work, optimising our work mode, as Alice suggested

Re this: https://github.com/w3ctag/design-reviews/issues/362 The explainer is in a google doc. And the spec is in a private repo

(Lukasz: there's more here? https://fernando-80.github.io/gamepad-light-indicator-api-draft-explainer.pdf)

Sangwhan: private repo isn't bad. locked google doc is a problem

Torgo: Yeah, I think part of how we work better might include having the spec they're asking us to review in some standards fora -- WICG issue, etc. 

Hadley: That may get in the way with what Alex was trying to do, with the blink process

Peter: Alice brought this up last week. She's keen on it. it's a bit of a DOS on us.

David: it's a tradeoff, becasue we want to see things when it's still influenceable. 

Torgo: What can  we do to get pepole to think about bringing stuff to a standards body before TAG review?

Peter: Sometimes it does feel like we're the Google Crazy Idea Review Board...

(back to assigning issues)


#### https://github.com/w3ctag/design-reviews/issues/362

Sangwhan: This is a pretty big feature. We should prioritise it.

Torgo: I'll put it down for the 24th.


#### https://github.com/w3ctag/design-reviews/issues/348

Tess: CSS will be disucssing this tonight

David: I think this is pointing out a gap in the design principles doc... we ought to be able to document how people make this sort of decision so people do it with some sort of consistency. I'll open an issue on that doc.

Peter: We've been down this road before on the design principles

Sanghwan: and we never actually fix the document

Peter: I know CSS WG have done this before...

David: You're right, it's issue 55 that is closest to this. I'll link to it.

Torgo: Is there a link to the CSS Agenda?

David: https://lists.w3.org/Archives/Public/www-style/2019Apr/0012.html

Torgo: MIlestone for next week


#### https://github.com/w3ctag/design-reviews/issues/356

Tess: There are a lot of strong opinions. Last time there was confusion on what were being asked to review. Consensus first would be great. I'll talk to them before next week

#### https://github.com/w3ctag/design-reviews/issues/359

Sangwhan: Add me

### Other topics?

Torgo: great. I'll go through issues with milestones in the past before next meeting. We have 5 mins left... Does anyone want to focus on one short issue? 

Sangwhan: 346 has an urgent tag. Pointer event extension

Torgo: True, but Alice has it set for the 24th. 

Lukasz: For 342, bump it 2 weeks or so. Or leave it for the face to face. 

Torgo: I'll comment in the issue, ask Mike West if the f2f is too late to be useful, and/or if he can join? 

Torgo: Anyhing else?

Tess: Re audiobooks... did you manage to catch Tsviya in Quebec on this?

Torgo: No, unfortunately. We mostly discussed code of professional conduct stuff. I'll move this milestone to next week and try to talk to her. 

#### https://github.com/w3ctag/design-reviews/issues/301

Hadley: We had dtapuska on a call, and he still doesn't seem to agree with our suggestions about how the web platform works. Not sure what we should do next?

David: My memory of that thread is that there was also a fair bit of misunderstanding in the issue. 

Hadley: Which misunderstandings are you thinking of? If we can, that would be useful

Torgo: Let's look at it next week. If we still aren't happy, having cleared up those miscommunications... I'll add David to it, since he's going to do that.


