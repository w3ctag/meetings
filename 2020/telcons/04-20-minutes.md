## TAG Teleconference
##### 20-22 April 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-04-20](https://www.timeanddate.com/worldclock/converter.html?iso=20200420T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris, @atanassov
* [Delegated Ink Trail](https://github.com/w3ctag/design-reviews/issues/473) - @dbaron, @atanassov
* [Image Resource](https://github.com/w3ctag/design-reviews/issues/490) - @dbaron, @atanassov
* [Window Segments API](https://github.com/w3ctag/design-reviews/issues/492) - @torgo, @kenchris, @plinss

#### Breakout B (US / APAC) - [2020-04-20](https://www.timeanddate.com/worldclock/converter.html?iso=20200420T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) - @cynthia, @dbaron
* [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov
* [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @dbaron
* [Data for measuring audio-video synchronization and end-to-end delay in realtime communications](https://github.com/w3ctag/design-reviews/issues/493) - @cynthia, @dbaron

#### Breakout C (APAC / Europe) - [2020-04-21](https://www.timeanddate.com/worldclock/converter.html?iso=20200421T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon
* [Scheme-bound Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon
* [AVIF Decode](https://github.com/w3ctag/design-reviews/issues/495) - @cynthia, @torgo, @kenchris
* [Schemeful Same-Site](https://github.com/w3ctag/design-reviews/issues/497) - @torgo, @ylafon
* [VirtualKeyboard API](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris
* [Data for measuring audio-video synchronization and end-to-end delay in realtime communications](https://github.com/w3ctag/design-reviews/issues/493) - @cynthia, @dbaron

#### Plenary Session - [2020-04-22](https://www.timeanddate.com/worldclock/converter.html?iso=20200422T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage



-----


### Breakout A

Present: Kenneth, Rossen, David, Peter, Yves

Regrets: Dan, Tess

#### [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405)

(trying to understand state of issue)

(Discussion around whether we should close it, as the right people are on the remaining issues - proposed closed)

Peter/Yves/Ken (discussions around adding tracking labels on the external issues)

#### [Delegated Ink Trail](https://github.com/w3ctag/design-reviews/issues/473)

Rossen: David still has some open questions in the issue

David: but he did miss the points about diameter and what units it is in. Also Web IDL errors.

Ken not a big fan of them doing prematurely extensability - added comment to the issue.

David: Fine with closing, no strong opinions.

Rossen: Same - but too close to the issue to make the call.

Ken: Let's defer to the plenary

#### [Image Resource](https://github.com/w3ctag/design-reviews/issues/490)

David: Propose closing it - we spent a lot of time on this given its small size.  I think we've given them a lot more feedback than those 3 paragraphs would have gotten had they stayed in their original spec.

Ken: I am OK with that.

David: Defer to plenary whether we will close or not.

#### [Window Segments API](https://github.com/w3ctag/design-reviews/issues/492)

Ken: Added comment about hinge area

Peter: What about ordering (top, down -> left, right) and what about multiple dimentions. I will add comments.

### Breakout B

Present: Alice, Peter, David, Rossen

Regrets: Tess, Sangwhan

#### [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433)

Discussed closing at the plenary.

Peter raised a question about using these codec apis in existing codec usage, such as MediaRecorder. 

#### [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488)

Alice: would be nice to have a discussion of how you'd choose which one to use.

Alice: also curious if we could see explainers for CSS specs, which would help people who weren't in the meetings understand them.  More examples might be useful; conversion description seems very underspecified (no links).

Alice: WCAG [specifies](https://www.w3.org/TR/2008/REC-WCAG20-20081211/#relativeluminancedef) color contrast using an algorithm based on YCbCr.  Could this be useful in computing color contrast ratio values?  Could we give people something that would let them do math on their CSS values for color contrast?

Rossen: ...

Alice: If we can get the computed values in lab() and then map the luminance there to something used in the existing color contrast calculation?

Alice: I could look at comparing lab() lightness ratios with WCAG contrast ratios.

David: [equations](http://www.brucelindbloom.com/index.html?Eqn_Lab_to_XYZ.html)

Alice: But the main question I don't know:  can we get computed values in lab()/lch()/etc.

David: part of a different spec?

Rossen: (looks through [w3c/csswg-drafts#4647](https://github.com/w3c/csswg-drafts/issues/4647), then looks for a different issue)

Peter: could be handled by [Typed OM](https://drafts.css-houdini.org/css-typed-om/), but I don't see anything there about colors at all

David: should we try to come back to this in a week or two?

#### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489)
#### [Data for measuring audio-video synchronization and end-to-end delay in realtime communications](https://github.com/w3ctag/design-reviews/issues/493)


### Breakout C

Present: Ken, Dan, Alice

Regrets: 

#### [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon

Dan: Tess was happy to live with it thought it is a bit of a hack... but we have given our feedback

Ken: their issue #27 has "needs resolution" and Yves says we shouldn't close it...

[closed]

#### [Scheme-bound Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon

Dan: The one thing that I would say is that there is a discussion from Anne about HTTPS. I don't think this is worth discussion, in particular because we are under unanimous agreement that HTTPS is the future.

Dan: The TAG is on record as being in favour of the move to HTTPS, so we can take that off the table in this discussion.

... May want to schedule a special breakout to talk about this.

[special breakout needed]

#### [AVIF Decode](https://github.com/w3ctag/design-reviews/issues/495) - @cynthia, @torgo, @kenchris

Sangwhan: i don't know what they want reviewed

Ken: AOM - AV1 - for image format - these are from mpeg... heif - this is related to patents

Sangwhan: policy wise we do not discuss patents

Dan: Agree

Yves: from what I've heard - avif is believed to be RF.  But not proven. And HEIF has patents. 

Ken: if you read the spec, the container is based on heif .. what is inside the container is av1 based.  this is based on isobmff ... 

Ken: how should we ask that question...    will write it.

[bumped]

#### [Schemeful Same-Site](https://github.com/w3ctag/design-reviews/issues/497) - @torgo, @ylafon

Dan: we asked for more explainy explainer, and how it fits together with scheme bound cookies.

[bumped]

#### [VirtualKeyboard API](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

Ken: 2 issues here, related but different. I think it would be better to split it up. Even 2 explainers.  One of the APIs being explained is - if you have docked virtual keyboard, where is the keyboard?  The other one is when the keyboard shows up you have more control over when it shows up and when it disapears...  I think they are kind of distinct.

Dan: can you ask them to create a new issue?

Ken: I will create a new issue and copy the text.  Creates [#507](https://github.com/w3ctag/design-reviews/issues/507)

Ken: [on show/hide] MS has some good examples... examples from excel online... some other cases as well... when clicking from cell to cell... 

Ken: there is a [whatwg issue](https://github.com/whatwg/html/issues/4876) - they have 

[discussing comments on the whatwg issue]

Alice: you've got to use the virtual keyboard policy to get that behavior.

Alice: It's not clear to me that it addresses the earlier comment about requiring a user action... 

Sangwhan: if you just call focus with javascript you could force the virtual keyboard to show up...

Alice: i wonder if that's calling focus or using autofocus...

Ken: reads [comment from oct 11](https://github.com/whatwg/html/issues/4876#issuecomment-541232517)

Dan: anne seems to be saying this has already been discussed, but their [whatwg] issue is still open...

Alice: person who filed our issue is did comment on their issue. 

Dan: So should this have been filed as a dispute resolution?

Sangwhan: i can ask

#### [Data for measuring audio-video synchronization and end-to-end delay in realtime communications](https://github.com/w3ctag/design-reviews/issues/493) - @cynthia, @dbaron



### Plenary Session

Present: Peter, Dan, Tess, Sangwhan, Alice, David

Regrets:

#### Breakout rollup

##### Breakout A

Dan: I wasn't there for this one, can someone who was there read back?

Peter: **CSS Modules**... we decided to maybe closed, talked about using the new tracking repo, set up a bunch of external tracks on the other issues and proposed that we close this at the plenary.

Dan: Shall we close it? There are open issues but we're happy that they're being addressed.

Peter: I will close it.

Peter: **Delegated Ink Trail**... propose closing, there are some open issues still.

Dan: Fine with me...

David: Fine with closing. For early review, it's fine.

Dan: Are we marking these as resolution satisfied? I like to mark things as satisfied. I'll do that.

Dan: Image resource... 

Peter: This was also propose closing...

Dan: Are there still open issues?

Peter: Don't think so.

Dan: Domenic says ... 

David: The references in the spec aren't quite right, but that's way more nitpicky than anything we'd normally point out (or even pick up, generally)

Dan: so closing all three of those! yay!

Peter: **Windows Segments API** - Ken and I left some comments, waiting for feedback.

Dan: Does it have a venue?

... Adding a label for needs (proper) venue.

... and I see you set it to a future milestone.

##### Breakout B

Peter: **WebCodecs** - discussed closing at plenary. Had a brief comment, which I posted... 

Sangwhan: I'm going to raise an issue about ????

Dan: Should we defer closing?

Sangwhan: No need to defer.

Peter: I'm ok closing this.

... discussion of adding the tag trackback label ....

Peter: Rest of the breakout we spent talking about **lab/lch colour**

Alice: We were discussing whether the L value from LAB/LCH for computing color contrast ratio: we can't.

David: There are a few other things I'd like to leave it open for...

... a bunch of other places on the platform that should be consistent with colour spaces

... No need to block shipping on that, but makes sense to get started on that work.

... My worry with laying out all the work that needs to be done is that it gets overwhelming and people don't even start on it, but what we actually want is for it to just be going on slowly in the background.

Dan: I re-set the milestone for next week, I'm hearing there's more work to be done

... Alice to write up her thoughts.

Dan: The other things you didn't get to?

Peter: we punted one to C, the other....

##### Breakout C

Dan: Talked about **WebXR Gamepads** module... closed it, I wrote a note about it.

... Talked about **Scheme-bound Cookies** from Mike West... we felt there was a special breakout needed. And we had a discussion with james roswell about https. Special breakout because it's a vague architectural issue. Peter should be on that, for architecture expertise. Yves should be on it. Maybe it's a California/Europe breakout. Maybe on Friday?

*** scheduling occurs (8am California / 4pm London / 5pm Paris, Friday) ***

Dan: **AVIF decode**, we bumped. Lot of discussion about container format.

Sangwhan: When adding a new image format, what parts of the platform does it affect? e.g. canvas image export?

... I looked at the patch and this is effectively a Chromium feature that just adds the decoder. There's no API.

David: The blink-dev thread had questions about accept headers and if they should be modified, which gets back to the "What do you do if you're adding a new image format".

Sangwhan: We don't have a process for that.

Dan: Is that a TAG thing? Should WHATWG handle it?

Sangwhan: It could be a finding? 

Dan: If you're adding a new image format, here's all the things you need to do...

Sangwhan: I'd be interested to write this, if I have time...

Dan: Maybe you could create a repo?

Sangwhan: I'll start with a private doc shared to the channel.

David: Also a question of whether it should be its own document, or in the design principles.

Sangwhan: Design principles is getting fairly large and this seems very specific.

David: Putting it in the design principles doc will make it more findable, at least, since people are visiting that doc regularly.

Dan: *mild shock that people aren't regularly reading the findings*

... *musing on best way to get more people to read the findings*

Dan: **Schemeful same-site**. We bumped this... questions remain on "What is this" and "how does it relate to scheme-bound cookies"... there is an explainer but the explainer is very terse, so I wrote a couple of questions, Ken wrote a question. 

... Can you put this in context and explain the user need, that's where we left it - really needs an explainer. 

... It may indeed by trying to add more security and privacy constraints, but depending on the relationship with scheme-bound cookies it could create overwhelming complexity.

Dan: **Virtual keyboard API**, we talked about a lot... Ken split out a new issue #507 ... 


... Some discussion (via Anne's comment) about whether this is a new proposal, or a dispute resolution given there was discussion on the WHATWG comment thread.

.. Sangwhan asked that question, we actually got a reply... need to take another look next week, and take a look at that reply.

Sangwhan: Sounds good.

Dan: **Data for measuring audio-video synchronization** (etc) 

Sangwhan: I suggested that we close... 

... technically we don't have strong opinions on this particular proposal

... I had one question about the privacy implications, but it's hypothetical. I don't have a strong argument that it's making user privacy worse.

... Other comment is that it's not really our field of expertise.

Alice: probably worth summarizing those comments -- help people who are new to the TAG process.  First, summarizing the possible privacy issue and suggesting taking to relevant experts.  And also getting feedback elsewhere.

Dan: Who wants to leave that comment?

Sangwhan: Most of that information was in my last comment...

Dan: Sangwhan, could you comment with a summary and close it?

Sangwhan: Sure.

##### Design principles

Alice: Tess and I Haven't had a chance to get to this yet

Dan: Ok let's punt that to next week.

... I wrote some [slides](https://slides.com/torgo/tag-update-for-ac-may-2020) and recorded a video... talking about the design principles and all the work we're doing... specifically I screenshotted the front page of the design principles, which has the new stuff that Tess did about priority of constituencies and points to the ethical principles, so I made that point.

... Basic, standard here is the TAG.

##### Issue triage

Dan: We have a new [design review request](https://github.com/w3ctag/design-reviews/issues/506) from jungkee... asking whether to file a design review. Yes, we do think so.

... I'm going to comment and close this issue, saying they should file a design review.

... Then it's just the Virtual Keyboard issue Kenneth raised in Breakout C... #507... copied a comment over from the other issue. Already been some discussion on it. Ken should be assigned.

Sangwhan: and me

Alice: and me

Dan: What's the venue

Alice: Editing TF

Tess: Part of the WebApps WG.

Dan: That's good.

##### AOB

Sangwhan: what's going on with our virtual f2f?

David: Three days are sorted, not sure about the fourth day.

... Based on the polls, the middle of the week after the one after we were originally planning. Those are in the calendar.

... Tuesday/Wednesday/Thursday (May 26-28) for everyone except Japan/Australia which has Friday morning (May 29) instead of Tuesday morning

Dan: What do we do with these slots?

... Do we take the process for weekly breakouts and plenary and expanding it?

Alice: Would be nice to do something more like the regular face-to-face with 1:1 breakouts

Alice: Would also be good to do a retrospective on our process at some point, e.g., are we happy with the three meetings per week.

Dan/Alice: discussion of whether we want any everybody-plenary time

Discussing maybe doing agenda bashing in regular TAG call on May 19/20.  (5:00 UTC)

Alice: could also maybe use some of the breakouts








