## TAG Call Minutes - week of 31-Aug-2020

### Agendas


### Breakout A (Europe / US) - 2020-08-31

* F2F Planning

### Breakout B (US / APAC) - [2020-08-31]

* F2F Planning

### Breakout C (APAC / Europe) - [2020-09-01]

* [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549)
* [Raw Sockets API](https://github.com/w3ctag/design-reviews/issues/548)
* [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538)
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521)
* [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511)
* [WebRTC-SVC (Scalable Video Coding)](https://github.com/w3ctag/design-reviews/issues/396)
* [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

### Plenary Session - [2020-09-02] - 21:00 UK time

* What to do about TPAC 2020?
* Issues
* [Email from Henry Story](https://lists.w3.org/Archives/Public/www-tag/2020Aug/0000.html)
* Breakout Rollup
* Issue Triage

## Minutes

### Breakout A (Europe / US) - 2020-08-31

Present: Dan, Peter, Rossen, Tess

We spent much of Breakout A planning the agenda for the virtual F2F.

**NB**: we subsequently resolved a mix-up on the dates and moved the virtual F2F to the week of the 21st of September.

### Breakout B (US / APAC) - [2020-08-31]

Present: Peter, Tess, Rossen

Regrets: Alice, Sangwhan

...

### Breakout C (APAC / Europe) - [2020-09-01]

#### [WebRTC-SVC (Scalable Video Coding)](https://github.com/w3ctag/design-reviews/issues/396)

Ken: not a lot of response to our feedback...

Sangwhan: did not hear much - we should send a friendly ping.

[bumped to week of 14th Sept]

#### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

Dan: this came out of the Abyss... Should we close it?

Ken: it's behind a flag in Chrome

Sangwhan: no other browser seems to care about it?

Ken: let's do a ping and ask for an update?

Dan: can we ask what the crossbrowser support story is?  Also what's the venue and the intended venue?

Yves: nothing since April on their repo.

Ken: not sure it's a Fugu thing.

Ken: [moz standards position ... ](https://github.com/mozilla/standards-positions/issues/167) seems positive...

Sangwhan: but has that position changed?

Ken: people seem to agree it's worth prototyping.

Sangwhan: I *was* positive... but given that web transport is coming this seems a little interim. And given that other browsers don't seem to be active in implementing this could be transitional.

Ken: Mozilla put this as part of the web transport framework...  They closed their standards position issue... 

Ken: Oh it was about Web Transport: https://github.com/mozilla/standards-positions/issues/167#issuecomment-684545844

[bump to the 14th?]

#### [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511)

Ken: [reading through comments...]

... if you search for something in the DOM but it's hidden you have the ability to unhide it ...

... notifies the page when the match is found ...

Dan: let's move this to the plenary.

Ken: I think it's pretty good...

#### [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549)

Yves: let's bump this



### Plenary - 2020-09-02 - 21:00 UK time

Present: Dan, Kenneth, Peter, Rossen, Alice, Yves, Tess

Regrets: David, Hadley

#### Readouts

##### Breakout A

[blink shipping process](https://github.com/w3ctag/design-reviews/issues/516)

Dan: Should we try to get Chris Wilson in to a plenary call before the f2f? 

[general agreement]

Rossen: I can take that action to reach out to Chris.

[week of the 14th of Sept]

Dan: Other than that we did f2f planning.

##### Breakout B

Peter: was rossen, tess and myself - we dis some breakout planning. 

##### Breakout C

...

#### What to do about TPAC 2020?

Dan: what would make sense?

Rossen: it might take a month's worth of time -

Ken: if people want to invite us that might be better.

Rossen: but their meeting might be 2 weeks after the TPAC week...  and other groups meeting before TPAC.

Dan: maybe ask Chairs to sign up for times?

Rossen: we could say that our preference is for the joint meeting week - the week before TPAC is reerved explictly for overlaping joint meetings.

Dan: +1

Dan: I'll revamp the issue template we used last time and send it to the Slack for consideration.

Peter: 12-16 October is joint group meetings...

Peter: we can also drop in...

#### [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511)

Alice: was just reviewing... Reading [joey's comment](https://github.com/w3ctag/design-reviews/issues/511#issuecomment-644348937)  - not sure how useful for other things it really is...  For cases like the `details` element...

... feels like he slightly misunderstood what I said about pseudoselector... It really depends on the content - only useful for when the content was previously hidden and is being shown as a result of the user interaction that triggered this event... 

... most of the alternatives - says "doesn't allow content to become hidden again"... don't understand why the proposed solution does that.  

Ken: you can remove it... 

...[reviewing explainer](https://github.com/WICG/display-locking/blob/master/explainers/beforematch.md)...

Alice: let's ask for clarification on that...  I will take an action to read this and get to the bottom of that.  Still don't undertsand why a better design wouldn't be automatic unlocking plus a pseudoselector. 

Ken: is it always find in page

Alice: also scroll-to-text...  Seems like you're forcing authors to listen for the event - extra work for authors. Could go badly for users if authors don't do that work...  I don't understand the cons of the automatic unlocking options.

#### [Raw Sockets API](https://github.com/w3ctag/design-reviews/issues/548)

Dan: ... Already a [good comment](https://github.com/w3ctag/design-reviews/issues/548#issuecomment-684960726) from Lukasz... 

[...some skepticism from TAG members...]



#### [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538)

Dan: 9 days ago they said it's going to ship.. our window of useful feedback is slipping...

Tess: off hand I think t's fine... I'd like to have more time to look at it.



#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521)

Alice: there was an issue in CSS wg... 



#### [Email from Henry Story](https://lists.w3.org/Archives/Public/www-tag/2020Aug/0000.html)

Dan: Not sure I particularly agree with the idea that we should be baking internaional legal norms ore regimes into the fabric of the web? This seems like a doubl-edged sword.

Dan: Meta question is: what kind of substantive feedback can the TAG currently give on this kind of porposal / paper?

Peter: a lot to unpack - some things that are alarming and some things that seem to make sense.

Dan: I also just don't realy know what Henry wants back from us here.

Peter: he wants us to sign off on his concept?

Peter: in support - it would be nice if there is a machine readable way ot declaring juristdiction.  If shopping and I'm going to spend money it would be nice to know what legal recourse I have if things go wrong.  A system where you could volunrarily expose that info and do it in a way that is verifiable.  "These are the laws that would cover this transaction." Not sure if that's what he's proposing.

Dan: libel laws / speech / limits on speech ...?

Rossen: how much of this is TAG really?

Peter: we should ask him for an explainer.
