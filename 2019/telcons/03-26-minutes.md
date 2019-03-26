## TAG Teleconference
##### 26 March 2019

Present: Alice, Tess, Peter, Sangwhan, Kenneth, Dan, Yves, David

Regrets: Hadley, Lukasz

---

Agenda:

* [User Activation Delegation through postMessages](https://github.com/w3ctag/design-reviews/issues/347) - @hober, @alice
* [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo
* [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @kenchris, @lknik
* [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff, @dbaron
* [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) - @slightlyoff, @dbaron
* [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @dbaron, @travisleithead
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @torgo, @hadleybeeman
* [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241) - @dbaron, @ylafon, @hadleybeeman, @lknik
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @slightlyoff, @torgo, @ylafon
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @slightlyoff, @hadleybeeman, @travisleithead, @plinss
* [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) - @dbaron
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) - @hober

---

### Tidying agenda

[Closing issue 312 - based on Tess's feedback.]

[punting web publications and audio books]

Tess: I wrote some stuff into audio books [345]. This is ongoing.

### [User Activation Delegation through postMessages](https://github.com/w3ctag/design-reviews/issues/347) - @hober, @alice

David: he responded to the substantive questions

Peter: he checked "issues in their repo" for feedback.

Tess: mark as urgent? he said we need to do it quickly.

Dan: Feels like he is dismissive of the privacy concerns. Yes, this is info that can be collected via other mechanisms, but does it make it easier to collect and share?

Peter: is this a high level feature that we even want to expose?

Tess: the case of the iframe that wants to tell its parents to resize it but only under user gesture. - a reasonable case for wanting to write web content that restricted itself to a user gesture.  Prior to thinking of that use case I thought it could be gated in other ways. the iframe resizing case was a reasonable counter-argument.  It's a bigger question than the scope of this design review.

Dan: i think it's reasonable for us to highlight this.

Tess: say you've got 2 fingers on the screen on 2 different elements... 

Sangwhan: is the activation state exploitable like how you could use hsts to fingerprint people?

Tess: not obvious off-hand to me if this would make it more possible.

Sangwhan: is there some kind of cache of activation state? Not sure how persistent that is. 

Tess: the persistence of that cache is concerning because...

Sangwhan: hsts state can be cached and can be used [for fingerprinting]. Is that in any way possible with this info.

David: if the user activation state is cached it's cached for a few seconds, not permenantly like HSTS.

Dan: ok - other than that I think we are happy - so let's bump it a week just to come back to it and hopefully close it up then.

Alice: if they decided next week to ship [in chromium] would anyone have a strong objection?

Peter: my concerns escalate as I see more and more APIs coming in that have a similar scope and nobody is looking at the big picture. These are all being taken in different directions.

Dan: what can we do about that?

Tess: 2 parts of that - would these things be unified in some way and how, and what is the right approach? also a process question - if we get 5 reviews that are all urgent that all have longer-term implicaitons, how do we give effectivefeedback in the time requested and simultaneously do right by our chartered obligations. if we're always udner pressure to not strongly object because of time-pressure then what is the point of the process?

Dan: +1

Dan: what are the similar things?

Peter: issue 356 - autoplay detection - feels like it should be harmonized with some other APIs.

Tess: there's a 

Peter: that was just an example of one more interesting aspect

Sangwhan: RTCquic transport - also an exmaple of different groups going in different directions for one problem set. Spatial navigation and html focus... 

Dan: I think it should be explored...

Peter: how? 

Dan: meta-issue in design reviews repo?

Peter: i will do that.


### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron

[punting]

### [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo

Tess: I'm concerned about the comment re: tag vigilance.

David: we had another issue in the design guidelines repo - we have 6 mechanisms that look similar, whats the rule for deciding which one to use?

### [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241) - @dbaron, @ylafon, @hadleybeeman, @lknik

[closed]

### [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @kenchris, @lknik

Kenneth: We gave a lot of feedback - events or observers - they are implementing the idea we raised. They still have some design questions. Not sure if we should close for now... wait for them to close back.

Sangwhan: i think we should remove the milestone and put it to pending extenral feedback.

Dan: suggest we put it to the f2f.

Sangwhan: i couldn't figure out whether it was supposed to be an observer or an event.

Further discussion on design principles to happen [here](https://github.com/w3ctag/design-principles/issues/127).

### [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff, @dbaron

David: punt 4 weeks?

### [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) - @slightlyoff, @dbaron

David: we wanted to invite stefan at some zeger point.

Dan: put it to the f2f and ask this person to dial in?

David: i should explain my concerns in the issue first...  3 weeks for now or later works for me if someone else can schedule it.

Alice: i can chat with him. What will the date be?

Peter: the 16th - 10 pm west coast time

Alice: i chatted with stefan and he can make it. 

### [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @dbaron, @travisleithead

David: this review was mostly travis - it would be good if someone else replaced travis.

Tess: i can try to be travis.

Peter: Punt 2 weeks.

### [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron

[urgernt / blocked]

David: i am basically OK with it unless something has changed recently.

Peter: Alice some responses here to your questions...

Alice: i need to clarify this...  I can take it off-line.  

Peter: loop back in a week?

Alice: yeah.


