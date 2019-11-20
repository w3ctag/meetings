## TAG Teleconference
##### 19 November 2019

Present: Dan, Kenneth, Peter, David, Alice, Lukasz, Yves, Tess, Hadley

Regrets: Sangwhan

Scribe: Kenneth

---

### Agenda

* Still trying to confirm guests for: [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @torgo, @hadleybeeman
* [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman
* [CSS intrinsic-size](https://github.com/w3ctag/design-reviews/issues/437) - @alice, @dbaron, @plinss
* [Get Installed Related Apps](https://github.com/w3ctag/design-reviews/issues/436) - @torgo, @kenchris, @hadleybeeman, @lknik
* [ fetch() upload streaming](https://github.com/w3ctag/design-reviews/issues/434) - @ylafon, @hadleybeeman
* [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) - @cynthia, @dbaron
* [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @alice, @hadleybeeman
* [Serial API](https://github.com/w3ctag/design-reviews/issues/431) - @cynthia, @kenchris
* [HTMLVideoElement.requestAnimationFrame()](https://github.com/w3ctag/design-reviews/issues/429) - @cynthia, @dbaron, @kenchris
* [[WebComponents] Custom state pseudo class](https://github.com/w3ctag/design-reviews/issues/428) - @hober, @kenchris, @plinss
* [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @cynthia, @alice
* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @kenchris
* [Microtransaction payment handlers](https://github.com/w3ctag/design-reviews/issues/422) - @dbaron, @kenchris
* [Web Bluetooth Scanning](https://github.com/w3ctag/design-reviews/issues/333) - @cynthia, @dbaron, @torgo, @kenchris, @lknik

### [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @torgo, @hadleybeeman

Dan: I reached out to Alex Russell and Rick Byers 3 weeks ago and haven't heard back. Also no feedback from Darwin after my and Tess' feedback. Schedule for F2F and get them on the line or there in person?

Do we have visibility on whether these issues are being addressed?

Alice: Let me check whether I have gotten any email on the subject.

Dan: It poeple actually working in this or is it one of these issues that just fades away and wastes out time. Suggestion is to move this to F2F and I will press to get someone to join us.

### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

Dan: I personally haven't done anything

Alice: Same... schedule breakout? Let's take it offline

Dan: Let me put it on for next week (breakout)

Hadley: I am on board

### [CSS intrinsic-size](https://github.com/w3ctag/design-reviews/issues/437) - @alice, @dbaron, @plinss

Dan: What is the latest

David: I took a look yesterday my concern seems to be fixed. I had a whole lot of comments from CSS WG member, but from TAG perspective I think it is fine - low level CSS stuff.

Dan: Sounds like we can close, Alice?

Alice: I should have a closer look, as I have some understanding of display locking and that has some accessibility tree implications

Dan: Can we bump it to next week?

Alice: I will be out next week, bump it two weeks?

Dan: I am bumping it to the F2F. Let's try doing it on a breakout

### [Get Installed Related Apps](https://github.com/w3ctag/design-reviews/issues/436) - @torgo, @kenchris, @hadleybeeman, @lknik

Lukasz: its basically a functionality for web apps to see if there is a equivalent native app installed, so to not prompt to install native app etc.

Very simple features based on manifest file, and I am OK with all of that

My only concern is around incognito that is should not return that the app is installed. But then maybe the app can check whether we are in incognito or not.

Dan: Or that you don't have the app installed.

Lukasz: Yes.

Dan: What is the deal with manifest

Ken: They are linked together. This is mostly for not showing double notifications etc.

Dan: Couldn't any app install a manifest and then probe to see if you have certain applications installed?

Ken: you need Digital Assets Links on your website that needs to match your app.

Dan: (Regarding prior comment of seeming anti-Web.)  If the intent is that you have web app and native app installed, and this makes all the traffic go to the native app rather than the web app -- could confuse users.  What if I made the explicit choice to use the web app... suddenly find that all my links have been going to the native app.

Kenneth: Already does that given that apps register for URL patterns.  If it's doing this test every time, if it figures out native app is uninstalled, could send notifictaions to web app.

Dan: Maybe be more explicit about what happens when both native app and web app are installed.  We don't want to put functionality in people's hands that favors the native experience over the web experience.


### [ fetch() upload streaming](https://github.com/w3ctag/design-reviews/issues/434) - @ylafon, @hadleybeeman

Yves: Anne thinks it is too early to do review. (some technical comment that I cannot follow - nothing major)

Dan: Should we put this on ice?

Yves: we could do that yes...

Dan: Progress something not really stalled... needs new label maybe...

Dan: May I close?

Tess: Sounds good

Dan: Doing!

### [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) - @cynthia, @dbaron

Dan: David?

David: Looked briefly - it seems probably good for a high level perspective but I think we should maybe look closer if we have the expertise.

Dan: If we do this at the F2F we should get an external expert.

### [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @alice, @hadleybeeman

Tess: Jeffrey Yaskin did a [privacy review of TTML2 for PING](https://docs.google.com/document/d/1115LZYzMXc9ZwOA8mjePtk3Bb4ID3AOk0n8_Q4tMrw4/edit#heading=h.7zy3ua9hwhc); we should take a look at his document and the [minutes of the TTWG telcon](https://www.w3.org/2019/11/14-tt-minutes.html#x04) in which they discuss his feedback.

Dan: Bump to next week and see if we can make some progress

### [Serial API](https://github.com/w3ctag/design-reviews/issues/431) - @cynthia, @kenchris

Dan: Ran into Suz from Stripe last week and she showed me why these APIs are so important from a maker perspective. It makes it so easy to get some hardware and configure/build  your own gadget in contrast to the mass produced privacy infrigting gadgets from large companies. This is different than the enterprise perspective we have heard before. I would like to get her comment on this.

Kenneth: Sanwhan and me looked at that spec and it is in a bad shape, contradictory texts, empty tables. I talked to Reilly at CDS and he has been implementing it for blink and a polyfill on Web USB and is concentration on getting the functionality and API shape right and not on fixing the spec at this moment. He will file a clarifying note in the issue on what we would like feedback on.

Dan: Bump a week?

Ken: Sounds good

### [HTMLVideoElement.requestAnimationFrame()](https://github.com/w3ctag/design-reviews/issues/429) - @cynthia, @dbaron, @kenchris

Kenneth: I haven't looked at that yet.

Dan: Let's bump this a week

### [[WebComponents] Custom state pseudo class](https://github.com/w3ctag/design-reviews/issues/428) - @hober, @kenchris, @plinss

Peter: Bump it, I haven't filed my feedback yet.

### [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @cynthia, @alice

Tess: We talked about this a couple of weeks ago and wanted to do a breakout

Alice: I am sure that we actually did a breakout! It is less of a proposal for a specific API and more a feature that various APIs can use which is not spelled out by the explainer.

Tess: I will try to dig up what my comments were going to be and actually post them.

Dan: Some new comments from Marcos around user gesture.

Alice: this made me believe this is not a standalone API.

Dan: F2F

Tess: Sure

### [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @kenchris

### [Microtransaction payment handlers](https://github.com/w3ctag/design-reviews/issues/422) - @dbaron, @kenchris

### [Web Bluetooth Scanning](https://github.com/w3ctag/design-reviews/issues/333) - @cynthia, @dbaron, @torgo, @kenchris, @lknik

Dan: Heard good feedback at TPAC, asked about it in issue and author didn't know about the feedback


