## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/09-14-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2020-09-14](https://www.timeanddate.com/worldclock/converter.html?iso=20200914T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394) - @dbaron, @kenchris
* [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538) - @hober, @hadleybeeman, @atanassov
* [Raw Sockets API](https://github.com/w3ctag/design-reviews/issues/548) - @hober, @hadleybeeman, @plinss
* [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549) - @hober, @ylafon
* F2F Agenda Planning

### Breakout B (US / APAC) - [2020-09-14](https://www.timeanddate.com/worldclock/converter.html?iso=20200914T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511) - @alice, @kenchris, @atanassov
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
* F2F Agenda Planning


### Breakout C (APAC / Europe) - [2020-09-15](https://www.timeanddate.com/worldclock/converter.html?iso=20200915T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebRTC-SVC (Scalable Video Coding)](https://github.com/w3ctag/design-reviews/issues/396) - @cynthia, @kenchris
* F2F Agenda Planning


### Plenary Session - [2020-09-16](https://www.timeanddate.com/worldclock/converter.html?iso=20200916T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo
* Breakout Rollup
* Issue Triage

## Minutes 

### Breakout A (Europe / US) 

Preent: Dan, Ken, Tess, Yves

#### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394) - @dbaron, @kenchris

Ken: no update - from 13 days ago 

Dan: for other issues that have "timed out" we've closed them...   Maybe give them one more chance?

Ken: I will also ping Alex Russell.

#### [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538) - @hober, @hadleybeeman, @atanassov

Tess: it seems like a good thing to write down... Everyone is doing this to some extent. However it's specified should allow browsers to be more aggresive than the baseline. Brave unconditionally does this to all sites (for example) and people uses Brave because they expect it to err on the side of privacy even when compat is impact - and they haven't seen any compat impact so far.  

... One of the things I think is relevant : simplicity and consistency are both important for developer expecation and understanding. So I'm sympathetic to the argument by Pete Snyder and Steven Englehart - why make the weaker change and just permenantly change referrers everywhere. The brave data suggests that there is no compat impact.

... we could say "We're glad everyone is trying to mitigate this concern. It would be good if it could be more consistent for developers."

Dan: Is that the kind of feedback they are looking for?

Tess: Yeah. They want to hear the TAG's opinion..  Suggest it should be "that sounds like a good change but in addition... " the simpler mdoel.

[agreed Tess to write the feedback and we will mark as "proposed close" and close at the plenary]

#### [Raw Sockets API](https://github.com/w3ctag/design-reviews/issues/548) - @hober, @hadleybeeman, @plinss

[lacking peter and hadley... we move to f2f]

#### [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549) - @hober, @ylafon

[assigned to f2f]

#### F2F Agenda Planning

[everyone to buy Murphy's stout]



### Breakout B (US / APAC) 

#### [Beforematch event](https://github.com/w3ctag/design-reviews/issues/511) - @alice, @kenchris, @atanassov
#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
#### F2F Agenda Planning

### Breakout C (APAC / Europe) 

#### [WebRTC-SVC (Scalable Video Coding)](https://github.com/w3ctag/design-reviews/issues/396) - @cynthia, @kenchris
#### F2F Agenda Planning

### Plenary Session - [2020-09-16](https://www.timeanddate.com/worldclock/converter.html?iso=20200916T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Tess, Dan, Kenneth, Peter, Rossen, Alice, Yves

Regrets: Hadley

#### Breakout Rollup

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

Ken: some people have been using TAG review as "it's fine" - but our review is not exhaustive. Some of these don't get wide review in W3C. Should that be part of blink process as well? Horizontal review.

Rossen: in talking about this - is Chris going to join us at some point?  

Peter: we wanted to get group consensus before inviting Chris.  

Dan: isn't there a new wide review process?

Peter: part of process 2020?

Yves: W3C review is still per domain.  

Ken: we could add it to their github template - asking or encouraging them to do wide rview...

Peter: [we did discuss this here](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/08-17-minutes.md#blink-shipping-process---torgo) (8-17 minutes)

Alice: longer conversation in the plenary in that same doc.  

[reviewing what we said]

Rossen: as a first step we can dump these things back into the issue and have a reply in the issue before moving to a synchronos discussion.  I can summarize in the issue.  We discussed  afew. The things that resonated the most with me were : what we expect from the review and what we believe that the blink process expects from the review an then based on that what is the sequence / timing?  One main point: perhaps to make the review process more streamlined / positive, to have the initial quck-signal or "idea review" - a "signal review" and have clear expectations on both sides - a time box wihtin the TAG should respond and if they don't hear they can assume it's fine.  And then some minor points of feedback - about putting the TAG review into an earlier step in the process.

Rossen: any other major points?

#### Issue Triage



#### F2F Agenda Planning

