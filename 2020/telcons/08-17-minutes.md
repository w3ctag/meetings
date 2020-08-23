## TAG Teleconference
##### 17-19 August 2020

---

### Agenda:

#### Breakout A (Europe / US)

* [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss
* [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris, @atanassov
* [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron, @atanassov
* [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

#### Breakout B (US / APAC)

* [CSS color-mix function](https://github.com/w3ctag/design-reviews/issues/526) - @alice, @dbaron, @atanassov
* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo
* [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

#### Breakout C (APAC / Europe)

* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [WebRTC Insertable Streams](https://github.com/w3ctag/design-reviews/issues/531) - @hober, @cynthia, @ylafon
* [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris
* [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo
* [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris
* [MediaStreamTrack Content Hints](https://github.com/w3ctag/design-reviews/issues/539) - @torgo

#### Plenary Session

* Breakout Rollup
* Issue Triage

-----

### Breakout A

Present: Peter, Tess, Rossen

Regrets: David, Kenneth, Hadley

Scribe: Rossen (mostly), Tess (a bit)

#### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss

Skipped.

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris, @atanassov

Discussion of jyasskin's reply, Rossen and Tess posting followups.


#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron, @atanassov

Tess: This is a big chunk of work. Ideally we can come up with a table of all features, APIs and what their behavior is in terms of capabilities inherited by parent browsing context etc.
... I will schedule time for myself and Rossen to work on this tomorrow.

#### [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris

Tess: Good conversation on the issue but we don't really know if Dan or Ken have further issues that what's there. We shouldn't sign off without the assignees being here.

Peter: Has anyone contacted libs devs who would build on top ot this?

Rossen: Don't know.

Tess: Motivation stated is customer feedback, thus, we could assume they are interested.

Peter: That's reasonable.

Rossen: Push to Breakout C?

Peter/Tess: Yes.

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

[all reading the proposal]

Tess: We are mentioned a number of times and it seems like we come into play after step 3, which is after feature-complete. That sounds a bit too late but the next section reads that this is when feature development starts...? 
... It feels like it will be good to have an earlier input from TAG/Standards. Perhaps this isn't there so that we don't have as heavy of a load on reviews as we do now?

Peter: Not sure if WICG should be the gate keeper for standardization. Not looking for negative signal but rather a positive signal of sorts.

Tess: Right, and this is somewhat what you'll need to get going with WICG... some engagement and thumbs up from others on discource.
... Also, previously we used to get a number of reviews for documents on random personal repos, having the WICG step there should help.

Peter: TAG review at Step 3 probably is better done at Step 2

Tess: And move the "you should have TAG sign off by now" to Step 4; it should be part of "evaluating readiness to ship".

Rossen: [many things which sadly didn't get minuted]

Tess: From the Blink side, I think they want our review to (A) be useful, and (B) not delay their product schedule. From our side, we want to feel like (C) our reviews (can) be impactful, and (D) our reviews are not rubber-stamping. Moving starting TAG review from step 3 to step 2 could help with (C), and moving completion of the review from step 6 to step 4 may help with (D).

[failed to minute]

Peter: Note that they require TAG review, they don't require favorable TAG review.

Peter: Deprecation process should likely involve a standards body at some point.

[failed to minute]

### Breakout B

Present: Peter, Alice, Rossen, Tess

Regrets: David, Sangwhan

#### [CSS color-mix function](https://github.com/w3ctag/design-reviews/issues/526) - @alice, @dbaron, @atanassov

Rossen: It looks like a number of the issues and new syntax has been addressed. 

Alice: Yes, the new syntax is pretty good. The explainer looks good too.
... It would be interested to understand what happens when mixing in LCH as this isn't covered in the explainer but are in the spec. How would that work and what would it mean? Not clear on the utility of that.

Tess: I don't really have good understanding of Color in terms of mixing, i.e. this feature. Ideally the explainer should be good enough for someone like me to understand what's going on, how do I use it and what to expect.

Alice: This part is only in the spec and not very clear there either.

All: Conversation about how we, TAG, should be engaging and providing feedback to design requests that are driven by others than those who wrote the spec. 

Alice: The explainer does motivate the feature and is really good. The one detail about the hue interpolation in the spec looses me and it would be great to understand it. Why are there values other than shorter?

Peter: Mostly when you're doing intepolations for transitions or animations. As clolor is a 3D space, the curves you get during interpolation between short and/or long path will give you very different light color values that you want authors to have access to. 
Maybe there are other cases when you're simply mixing between two things, why would you need anything else other than shorter?...

Alice: That satisfies my curiosity, thank you. Suggest we close as satisfied and open a bug with the spec.

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo

#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

Tess: We had a good discussion about it in Breakout A. One of the things was to step back and discuss the goals of why the Blink project would involve TAG and vise versa. 

From Blink point the expectation is that:
- TAG reviews should be useful.
- TAG reviews shouldn't be a blocker

From TAG side the expectation is that:
- TAG isn't percieved as a rubber stamping body to ship features
- TAG having a positive review shouldn't be given the weight of "this has passed sufficient wide review to be a standard"

Further, timing of when TAG is engaged is important. We concluded that we weren't sure if our decision making is going down the right path so we thought we can use the help from someone much closer to the project. (Tess restating Breakout A discussoin around moving steps from 3 to 2).

Tess: Alice, what do you think?

Alice: My raw thoughts are... the framing of the expectations from both sides is really good. Having affordances for us, TAG, to be able and handle revies on time and with high quality is important. 
An explicit exit criteria out of each step can be improved. 
Step 3 is supposed to be an iteration step. 

Tess: Yes, but at this point the expectation is to be feature complete.

Alice: Incubation depends on having code and being able to iterate with those who request the features. 
Another point that seems to be missing is calling out polyfills.

Peter: Yes, and polyfills can be used for incubation too.

Alice: The idealized theory is, you're writing code that is a proof of concept that you play with... but in reality this is usually what gets productized in the long run. By the time you have something to review, some level of buy-in is done. Similar to code review where you get a bunch of feedback after you write code and you need to change... compared to paired programming where the feedback is much more real time.

... My question would be - what kind of artifact could we review that doesn't have the problem of buy-in

Tess: Explainers are such an example which needs to be done much earlier before you write code.

[Discussion] about having early engagement that will be timely (say two week turnaround for example). Perhaps we can have a different repo ideation-reviews that will allow us to validate the use case, suggest prior art that could be missing and agree on rough path forward.

### Breakout C

Present: Alice, Sangwhan, Kenneth, Yves

Regrets:

#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

Ken: This was mostly the issue that Sangwhan had...

Sangwhan: Someone brought the issue to our attention that some devices can enable tracking... some devices can even be bricked, including one very common device... allows firmware updates.

... Also the problem that these devices also have a microphone and allow you to record sounds through HID... bypass mechanism for WebRTC permissions.

... Device that is problematic DualShock game controller (3 and 4). One of the most common gaming controllers on the market.

Yves: Playstation one...

Sangwhan: Right, it's the most popular on the Playstation

Ken: Comes with the device :)

Sangwhan: Suggestion from Chrome engineer was that 3 and 4 should be added to a blocklist that they maintain. Not a standards thing, but a Chrome thing.

Ken: Wasn't the idea for HID to support these types of devices?

Sangwhan: Right, so blocking it somewhat defeats the purpose.

... Spec author suggested that Sony and Google take the mitigation discussion off-thread... a little concerned that this is being done behind closed doors.

... Would like to hear your opinions on this...

Ken: Blocking... would it block the device itself? Or some of the specific logic for exposing the MAC address?

Sangwhan: Suggestion from Chrome guys ... block it at the OS level... expose it as a gamepad. Or, blocklist the device altogether. Can blocklist the device at the browser level... if it's a raw HID device you just blocklist it altogether... otherwise you can expose it as a very primitive gamepad.

Ken: I see they have a blocklist for all these devices... shouldn't this list be shared in public?

Yves: Shared would be good for interop.

Ken: Should devices be able to opt out of being shared on the web?

... USB can have different profiles, some of it may be no exposed?

Sangwhan: ... can set an origin .... web USB ...

... removed because device vendors wouldn't do the work needed. Also there's already a lot of devices already out there.

Ken: Blocklist should be public.

Sangwhan: List should be a shared resource, not browser-specific. 

Ken: And we need info about why the device was blocked.

Sangwhan: I don't like the possibility that websites can _brick_ people's gaming controllers. That's definitely not good.

Ken: A gaming device also seems like something people are even more likely to give websites access to compared to, say, scales.

Sangwhan: I can write some feedback... last comment seemed to have been ignored.

Ken: If we do this blocklist as a github repo or other public location then device manufacturers can ask to be blocked.

... Could have a nice README explaining how to request to add your device to the blocklist. Right now if I were a device manufacturer, and I didn't want my device accessed on the web, how would I go about that? Who would I talk to?

Sangwhan: Implementer-level blocking definitely isn't going to scale. Would like to hear what they have in mind before we go making assumptions.

#### [WebRTC Insertable Streams](https://github.com/w3ctag/design-reviews/issues/531) - @hober, @cynthia, @ylafon

Yves: We were waiting for Sangwhan's feedback, Tess added herself to the list of reviewers.

Sangwhan: I remember looking at this briefly... seemed ok to me.

Yves: Some question about why audio worklet over streams... mostly historical... not sure if they would choose streams now. Might make sense to use streams now instead?

Sangwhan: I don't have strong objections. Unless Tess or Yves have strong objections..

Yves: I'm ok to propose close and ask Tess at the plenary if she agrees.

#### [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris

Alice: I see they requested an issue for each point of feedback, so I filed a bunch of issues.

#### [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov

Alice: I see this is propose close...

Ken: Yeah, until the propose something new with WebCodec as the base primitive. Now this is about providing convenience APIs, which they say they're discussing in another issue.

Yves: Could this be related to Insertable Streams..?

Ken: I don't know.

Yves: No requirements to have streams in real time... could stop, do some editing and continue. One of the goals of insertable streams was to allow things like adding backgrounds. 

Ken: Seems anyway like this won't progress until there is this new thing...

Yves: Should we ask if they still need the review...?

Ken: Yeah, I'll write something.

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

Alice: Let's bump this to next week when Dan is back.

#### [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris

Ken: I know a lot of people really want this for performance.

Sangwhan: I don't think this partial thing is really a big deal..

... if you do a partial you're breaking transactional guarantees. If you can't do further writes you've left your database in a broken state. Have to go through the remaining... seems weird. Should be all or nothing. 

Alice: Basically in agreement with dmurph's comment..

Sangwhan: Yes.

Ken: I'm going to ask around about this, I don't know much about databases but I have friends who do, would like their input.

Sangwhan: I have some feedback...

... comment is that .. future considerations include an addAll API... similar to putAll but (??) entries in the same transaction.

... Would give feedback that that should come pretty soon rather than at some unclear future time. putAll proposal.. A=1 B=2 C=3 and A=4 in the same transaction... you're batching up a bunch of data and clobbering data in the same transaction... some cases where you want to be able to put those... some sort of programming error in a lot of cases. Would be useful to have this sooner rather than later.

... Discussion about returning to (?)... should be all or nothing.

... Happy to propose closing and discuss in plenary.

#### [MediaStreamTrack Content Hints](https://github.com/w3ctag/design-reviews/issues/539) - @torgo

Ken: I looked at it... applying other algorithms to streams, noise reduction, want this hint. I would want to make sure you're getting the right type of hint. Depends on the algorithms...

Sangwhan: Main question.. who sets the content hint?

Ken: The author.

Yves: Yeah, the producer.

Yves: Should be an option for games... low-latency... expense of (?) being more precise.. Respect a certain latency... some things hwere you don't want to have a delay.

Sangwhan: degradation preference: framerate or resolution or (?). Games might want to maintain the framerate. Not sure what might want to maintain resolution in favour of framerate.

Ken: Something in style guide about naming...

Yves: Since it's a hint, I'm ok with it.

Sangwhan: I'm also OK with this. I just have one question...

Yves: Not sure about the encoding part... don't know that they need to be hints or more enforced than hints.

Ken: I'll file an issue on (?) as well.

### Plenary Session

Present: Kenneth, Peter, Alice, Tess, Hadley, Yves, Rossen

Regrets: David, Dan

#### Breakout Rollup

Peter: Breakout A:

**Unsigned Web Bundles** talked about jyasskin's reply

**subframe/resource capabilities** planned to build up a table of the capabilities

Tess: Rossen and I had a 1:1 breakout yesterday... sketched out a spreadsheet, mostly not filled out yet.

Peter: **putAll** didn't discuss much

**Blink Shipping Process** Talked about a bunch, decided to add it to all other breakouts

Tess: **Breakout B**

**CSS color-mix function**

Some confusion because there are some features which aren't fully explained. Talked about how CSSWG could do a better job writing explainers (so it's not left up to implementers)

... actual bit we were asked to review seems great, decided to close the issue and file an issue on csswg

**Blink shipping process**

Talked some more about this.

Kenneth: **Breakout C**

Talked about **Web HID** - someone from Sony saying it's not safe to expose the PlayStation controller.. some discussion about what to do, do we block it, should the block list be public and enable manufacturers to opt in easily?

Sony device requires very careful handling, can be bricked via bad firmware upgrade.

Rossen: So proposed path forward is to come up with some kind of policy?

Kenneth: Sangwhan was waiting for some feedback...

Alice: I have an action item to get folks in touch with one another

**Insertable Streams**

Kenneth: Seems that most people were happy with this, proposed closing but wanted to check with Tess.

Tess: I think it's fine to close.

Yves: I'll close it

**Virtual Keyboard**

Kenneth: Alice filed a bunch of issues as they had asked for feedback that way.

Rossen: This isn't worked on by CSSWG as a path forward?

Alice: They initially weren't using environment variables...

Rossen: This is a complete overlap with a problem that's been discussed in CSSWG regarding things which overlap the viewport... part of one of our face-to-faces relatively recently. We have talked about this quite a bit. I'll connect the dots there and hope that this discussion continues forward with all the prior art taken into account.

**Client-side video editing**

Kenneth: Proposed close since we're waiting on a new proposal based on WebCodec.

**putAll**

Kenneth: I had asked a friend who knows more about this for feedback but haven't heard back yet. I've heard that it's a performance improvement because individual updates require individual error handling... but it needs to be an atomic operation, either all puts succeed or they all fail.

Peter: Want to make sure they're buy-in from major libraries that build on top of this, but I can't imagine why they would be opposed. They may even be the ones asking for it.

I'll add a comment.

Kenneth: **MediaStreamTrack Content Hints**

Way to say "this stream is voice" or "is music", e.g. to remove background noise from voice. I commented that some of the casing in the naming doesn't follow our design principles guidance, but otherwise looks pretty good.

Peter: Propose close?

... They asked for an issue on their repo.

(also capturing Sangwhan's comment/question.)

**Blink shipping process discussion recap**

Rossen: Few main points that were being raised...

Some of the major expectations that Tess outlined in breakout A discussion...

Tess: Point of reviewing the blink shipping process is to help blink improve it so it better meets their expectations and ours.

Blink's expectations are:
1) for TAG reviews to be useful.
2) TAG review shouldn't unnecessarily delay shipping. Don't want us to block work.

Our expectation are:
1) If we're spending time on a review, it should be impactful. Needs to be early enough that any major concerns can result in a major redesign.
2) Don't want to be a rubber-stamp replacement for wide review by the standards community.

Looked at the existing timing in the new process of when TAG is asked for review, and when we have our "last chance" to have impact/finish a review.

Two ideas for how to improve things, essentially by shifting both of those times.

One problem we've had as TAG was that the previous process had people coming to us too early, e.g. before things had even gone into WICG and were still in personal repos. Moving later than that was an improvement.

However, it's now potentially too late - feature-complete prototype before coming to us for review. Still some potential for impact there, but probably too late for us. 

There is some language in the second step about graduating to WICG, and we felt that that might be an appropriate time. Still not "feature complete".

Second change was at which point should we have wrapped our review. Currently step six, which is roughly "ship". Suggest changing it to step four, which is check readiness to ship.

If review is still open at step four, could mean that we haven't gotten to it yet, or could mean that we're waiting for a response. Moving that check to step four would give more opportunity for them to bug us or respond to questions.

Rossen: Another point discussed in breakout B... current stage for TAG review is mostly around design time of a feature... people are mostly invested in their ideas, even if this was something that was already tried and failed before. We get delayed with our backlog, and by the time we get to look at something, the design is already shipping.

Compared this with a code review, where the review process happens once a lot of work has already happened and change is painful, vs. pair programming where feedback is real-time.

Is there a way we can make our feedback more timely in that way? Perhaps we can have an early-stage review which is at the time of conception and ideation, implementers/proposers will engage with customers, users etc to understand the signals and requests. At that point we could have a "lightweight" or "ideation" review where we could have general guarantees about how quickly we respond to those reviews to give more timely feedback, and prioritise those (easier) reviews.

Then a design review for the same proposal should be easier as well, as we have already given feedback.

Hadley: Ideation review is interesting. Got me thinking about reviews where it would have been useful for us to get involved sooner. Off the top of my head... times where we have ethical or conceptual problems with a feature, such as prioritising the needs of advertisers over users. Discussion is more "should this even exist", which we don't have much influence over. 

... Other times, we've wished we had engaged earlier where we want them to think about integration with a piece of the web platform, but it requires going back to first principles to figure out how to do what they want a different way.

... Would we be able to catch those with an early review?

Rossen: We didn't really go into that much depth...

... This is nothing new, this is the process we use at Microsoft when we roll out features. We have a "strategy" discussion in the beginning, figuring out the bigger picture and should we be doing this at all. A lot of features are cut at that point. Once we have a strategy ... have a pretty good chance of rolling things out.

... Compared to TAG, we're trying to get something similar to this. e.g. for the virtual keyboard API, if the review was "we want something to enable authors to move content around a keyboard overlay, had the idea to put something on window" and we could say "go talk to CSSWG, they have already looked at this problem", we could avoid them doing a bunch of unnecessary work.

... Other part is having the different horizontals... e.g. is this going to impact privacy, fingerprinting, security, accessibility... early "sniff test"... we can validate use cases at that time. Or hey -- do you have a use case?

Alice: that is critical. I'd love to see an early stage explainer. What kind of artefact do we need from people to do that?

Rossen: Early stage of explainer... as something is matured out of this point we can mature that into a design phase... 

Restating, if this is going to be a stage where we want people to engage with us... we can help them to generate a good explainer to transition into the design review phase. As we sign off on their ideation review, can open an issue for them in our design review repo.

... Other point that came to mind... we're over-indexing on Blink. Google is not the only implementer that is engaging with us, even though Google brings the most volume. I have been observing good faith engagement from them and trying to make things better, but I would expect the same from engineering teams on any other browser etc. Let's not make this seem Google-focused.

Hadley: I don't want to design a process for a group that's not a W3C group. I wonder if there's a way for us to engage with other engine teams to see if this process fits WebKit/Gecko/Samsung Internet etc. to bring stuff to TAG as well. Don't want to build in exclusivity.

Peter: Talked about tying something to WICG... that's a more W3C-wide thing.

Hadley: Would also help avoid getting Chrome-only things that don't need to be standardised.

Peter: If we do separate type of ideation review, need to tightly scope what input we will take and feedback we will provide - more of a "sniff test" than a full review. Part of our issue templates etc.

Rossen: Would rather avoid calling it something around "ideation", something more like "signal review"

Hadley: I have been becoming frustrated with how we have been become reactionary... that kind of early-stage strategy, ideation reviews sound really fun.

Rossen: Have gone through a similar thing internally, had to design a process to do exactly what you just said, going from reactive to pro-active engagement. It's working really well. People are happy to go talk to the "big wigs" on the committee, who can help them with the discussion and ideas... Not sure how well that will translate to TAG. Extra process is extra process. I am optimistic about the potential for a positive flywheel effect.

Alice: As I said in breakout B, and re making this not just a blink-focused discussion — it would be great to see explainers from every working group.

#### Issue Triage



