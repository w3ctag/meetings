## TAG Teleconference
##### 17 July 2019

Present: Kenneth, David, Peter, Dan, Lukasz, Tess, Hadley, Yves

Regrets: Sangwhan, Alice

Scribe: David

---

Agenda:
* Blog post on questionnaire
* [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393) - @alice, @dbaron, @lknik
* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [Web of Things (WoT) Thing Description](https://github.com/w3ctag/design-reviews/issues/357) - @torgo, @ylafon, @kenchris
* [Web of Things (WoT) Architecture](https://github.com/w3ctag/design-reviews/issues/355) - @torgo, @ylafon, @kenchris
* [Element Timing API (images and text)](https://github.com/w3ctag/design-reviews/issues/326) - @dbaron, @kenchris
* [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @dbaron, @kenchris

---

### Blog post on questionnaire

Will follow up on Slack.

### [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393)

Lukasz: The ? part of the reply I'm not commenting on.  There are more metrics out there.    The last part says we have nothing to worry about because there are other ways to do that... do what?  Can I ask what it is that might be an issue?  I'm more and more skeptical about this point of view -- just because something is possible with something, doesn't mean it's ok to add other things that do the same.  Or at least have it catalogued.

Dan: Sounds good to me.  Often claims of no privacy concern say "the information can already be found with this other API".  I'm skeptical; is that a reason to dismiss that the new API can be used to get private data.  I think it's worth asking that question.

Lukasz: So I'll reply.

Dan: Other thoughts?

David: I'd like to look at it more. For the interaction with layout perspective.

### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389)

David: Sangwhan wanted to do breakout 2 weeks from now, so bump to 3 weeks from now?

Dan: Looks like there's been response to your initial comment.

### [Badging API](https://github.com/w3ctag/design-reviews/issues/387)

Tess: We got a big response late last night addressing several of the points we made; haven't yet had a chance to digest the reply enough to respond.  It was also in reply to Alice's comments; would love to hear her thoughts.

Dan: Bump it a week?

### Web of Things (WoT)
* [Web of Things (WoT) Thing Description](https://github.com/w3ctag/design-reviews/issues/357) - @torgo, @ylafon, @kenchris
* [Web of Things (WoT) Architecture](https://github.com/w3ctag/design-reviews/issues/355) - @torgo, @ylafon, @kenchris

Dan: Kenneth, have we heard back?

Kenneth: no

Dan: Well, there's been one thing; did get a reply from the chair in 355.  Suggested focus on specific chapters.  And there's a bunch going on in issues in their repository.

Dan: Let me look at 357 as well.

Dan: Bump both?  I'll take a look at the sections of the architecture document that he pointed us to.

Dan: Hadley, did you have specific feedback on the things description?

Hadley: Haven't looked yet, but happy to do that.

Dan: We could do another breakout on this in a Europe-friendly time.

Dan: We'll do a breakout later timeslot on Thursday.

[bumped a week]

### [Element Timing API (images and text)](https://github.com/w3ctag/design-reviews/issues/326) - @dbaron, @kenchris

David: the order has the harder one first. there was a bunch of stuff related to text that wasn't fleshed out last time we looked. we should probably split images and texts into different reivews

kenneth: they also had questions re shadow dom, and wanted to move this to web performance 

David: (currently WICG)

torgo: doing something useful and specific sounds like the right approach to me. 

David: Yes. We should probably open the other review ourselves for text and close this one.

Originally this wasn't meant to include text... we tried to add it in, but that probably wasn't ideal. 

Assuming Kenneth is okay with the images part

Kenneth: Yes

### [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @dbaron, @kenchris

David: i'm fine with closing this 

Kenneth: I can close it then

### All Other Business

#### Triaging [Web Socket stream](https://github.com/w3ctag/design-reviews/issues/394)

David: any relationship to [Web Transport](https://github.com/w3ctag/design-reviews/issues/389)?

Ken: we reviewed web sockets ... this address some issues TAG identified with existing APIs... everything to be streamable - this tackles that.  They are doing some clean-up in the API as well...

(discussion of venue and it being early stage work)

Hadley: feels early for us to engage.  Is there related work we should link to?

Ken: also related to web transport... mentioned in the explainer as web transport may supercede this.

Dan: Agree with Hadley, not clear how we should engage given that it's somebody's private repo + google doc with no chosen venue.

Dan: Let's bump two weeks and wait for responses.

#### [Ethics issues](https://github.com/w3ctag/ethical-web-principles/issues)

Dan: Hadley, new issues in ethics stuff?

Hadley: Not specifically; I just was looking for time to come back to all of them.

Dan: Maybe we could also use the breakout tomorrow at 5pm London time for that.

