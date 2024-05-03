 # TAG Teleconference
#### 29 April - 01 May 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-04-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240429T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion

### Breakout B (California / Europe)  - [2024-04-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240429T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

### Breakout C (California / Australia) - [2024-04-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240429T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### Breakout D (California / Australia) - [2024-04-30](https://www.timeanddate.com/worldclock/converter.html?iso=20240429T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

### Breakout E (Europe / China) - [2024-05-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240429T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

### Plenary Session - [2024-05-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240501T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Potential TAG Findings
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* Call time discussion

-----


## Breakout A

Present: Matthew, Max

Regrets:


### [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion



## Breakout B

Present: Matthew, Peter, Yves

Regrets: Lea


### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

General discussion involving wondering about why this needs to be a distinct API from RenderCapacity (maybe to allow site owners to make changes to content, rather than on-the-fly adjustments to graphs, but still seems similar).

Regarding whether this provides more/less info: discrepancy seems to be whether one's talking from perspective of CPU or Audio load specifically.

Side channel: ACK - what can it be used for? (Could it be used for general communication, like the pre-mitigation Compute Pressure API one?) Could 'blank' audio be used as part of an attack?

Yves: No signals from other implementers.

*Group notes that this work originates in a CG; the RenderCapacity work is being done in WG*

Peter: Seems clear this is about stats vs the other work is about adaptivity. We asked in the other review about why it's sending events. Seems worth seeing if the two can be combined.

<blockquote>
We're trying to understand the difference between this and #843 - this seems to be geared towards statistics, whereas RenderCapacity seems more about adaptivity, but they both seem to be giving similar information - have you explored whether they could be combined?
  
We'd like to see some further documentation around the abuse cases relating to the side channel that you describe.
  
Do you have any information on the position of other implementers on this proposal?
</blockquote>


## Breakout C

Present: Peter, Tess

Regrets:

### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

Punting as Lea isn't present

### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

Pinged Koji to answer the rest of Lea's questions.

### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou

Peter and Tess discussed this feature in the context of view transitions, prefers-reduced-motion, and the priority of constituencies. For plenary: possible TAG finding fodder.

Note for issue comment: Is there a valid use case for this feature besides View Transitions? View Transitions are not primary content (aside: they should be disabled by UAs when prefers-reduced-motion is enabled), and it's a disservice to users to block incremental rendering (a core feature of the web platform) in service of nice-to-have visual effect. Should also note browser competitiveness concern (blocking rendering appears to users as their browser being slow, which will be blamed on the browser, not the site, thus disincentivizing implementation.)

Actions:

1. Peter: file issue on view transitions re: prefers-reduced-motion, if it isn't already filed. if it already exists, chime in on it.
2. Tess: draft comment based on the above notes.
3. Peter and Tess: talk about possible finding in plenary session.

### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

Punting as Lea isn't present

## Breakout D

Present: Peter

Regrets:


### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

### [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou


## Breakout E

Present: torgo, martin

Regrets: max




#### [Permission Policy Unload](https://github.com/w3ctag/design-reviews/issues/738)

*we agree to close [Permission Policy Unload](https://github.com/w3ctag/design-reviews/issues/738#issuecomment-2088092732)*

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman


Martin:  Attended meeting in Boston (PATCG, plus some side meetings). Privacy properties of the system are "negotiable" - the web site gets to set how much privacy people get...  They used "differential privacy" as a privacy mechanism. The web site can choose a number between 1 and 64 - epsilon - determines how much privacy loss there is.  In their API, as a web site you can set whatever number your choose within a range. 1 is considered "fine" [by privacy community]. They also let you set it to 64 which is a big number. Meaningless in terms of privacy. Default is 10 and I don't think 10 is meaningful privacy.

Dan: and normative language of user control.

Martin: no user control. There is a trial running - and part of the trial is to determine which web sites can use the API.

Martin: event-level - you get a report for every "conversion" - with randomised response - some proportion of the events are randomized to maintain privacy ... One in 20 reports gets fuzzed.. statistically that's poor in terms of privacy .... aggregated report (with noise) .... They need more safeguards than what they've put in place.

Dan: trying to channel this into the issue.

Martin: the API is [not well designed]. If you want the browser to do anything you set particular HTTP header fields on arbitrary requests that come to your server.  You put in a special formatted header field - which gets big - and then that triggers actions in the browser which goes off and does a bunch of stuff in its own - no "origins" [web security model]. My suggestion is that we defer this. Ultimately they will ship what comes out of the CG/WG.   We can say "we're not going to do a complete review - but we have the following feedback - we expect a working group will go into detail on this"

Dan: is there a PATWG?

Martin: no info at this time.  Team said it would happen after AC meeting.

### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro


## Plenary Session

Present: Dan, Tess, Matthew, Peter, Martin, Lea

Regrets: Martin (partial), Amy, Hadley, 


### Breakout Rollup

#### Breakout A

Matthew: we're waiting on some feedback from Sangwhan on WebNN feedback. 

#### Breakout B

Matthew: webaudio playout statistics... how similar it feels to rendercapacity... we understand that they're doing different things but they're similar problems. So we sent a comment back to see if the two groups could find commonalities.  Some disagreement on privacy issues... 

Peter: one seems to get stats after, and render capacity api seems to give feedback back to adapt... had concerns about this being an event based systen. If you turn it into a polling API then these 2 look very much alike.

#### Breakout C

Peter: we punted anchor positioning... we talked about renderblocking... i took action to file an issue on viewtransitions... only use case is viewtransitions... treating viewtransitions as something that has to happen. User should be in control.  Should not be considered mandatory. It's progressive enhancement. tess to draft comment.

Tess: 2 things that keep happening - Maybe it should be a stand-along thing?  There are a variety of features on the web platform. Some of them are "nice to have" - embellishments. They add visual flourish but aren't essential to operation. E.g. using a CSS transition. 

Peter: they can be used in a way that helps the user - assistive to the user 

Tess: we want to say "features like that - a) if there's a way for the user to turn them off then that shouldn't break the page - e.g. prefers reduced motion." secondly "these embellishing kind of features sometimes require changes in the underlying functionality. we shouldn't make the underlying functionality worse or more brittle just because it enables an embellishing kind of feature." in this case viewtransitions is the motivation for making this change - delay in rendering- but the delay in rendering is a "foot gun".  Incremental rendering is a feature of the web platform. if you're new to the web, it's weird that your page doesn't have an idea of "done loading".  People want a reliable signal. However that could be used in a lot of places - which could defeat the work done on incremental rendering. In addition - browser competitiveness and perceived performance. Users' perception of how fast a browser is - is not straightforward - but it's "how quickly can you get something on screen user can inetract with" - if we do this kind of feature, the perception of users is that sites get slower. They are not going to blame the web site. they will blame the browser. So shipping this feature could cause people to move away from that browser.  This kind of thing has come up before... maybe it should be something more durable.

Peter: didn't see anything in the viewtransitions spec that talks about that... there has been some discussion on preferedreducedmotion in the context of scrolltransitions. Its a signal from the user - doesn't "disable"... it's up to the web page. There's needs to be another setting "don't animate transitions".

Dan: Just added https://github.com/w3ctag/design-principles/issues/493 to try to capture this.

Matthew: this has come up in accessibility conversations... but asking: imagining the work on accordion is openUI... 

Tess: on `inert` and find-in-page. There's an open issue in webkit... inert attribute does what it says on the tin... both gecko and blink, when the inert attribute is applied to an element, find-in-page no longer finds anything in that element. there's a patch for webkit to do the same. In this case there has been push back because it feels like a regression for users - who won't be able to find stuff now. 

Matthew: the classic case is hiding stuff behind stuff a modal dialog - in that case, it makes sense... but it's not really part of what you're focusing on. 

#### Breakout D

*didn't happen*

#### Breakout E



### Potential TAG Findings

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Call time discussion

We agree to move C 1 hour later.  
