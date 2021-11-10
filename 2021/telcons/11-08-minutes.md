# TAG Teleconference
#### 08-10 November 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-11-08](https://www.timeanddate.com/worldclock/converter.html?iso=20211108T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @LeaVerou, @atanassov
* [SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov
* [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov
* [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov
* [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @kenchris, @hadleybeeman

### Breakout B (US / APAC) - [2021-11-09](https://www.timeanddate.com/worldclock/converter.html?iso=20211109T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [WebTransport review request](https://github.com/w3ctag/design-reviews/issues/669) - @plinss, @atanassov

### Breakout C (APAC / Europe) - [2021-11-09](https://www.timeanddate.com/worldclock/converter.html?iso=20211109T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou, @kenchris
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris

### Plenary Session - [2021-11-10](https://www.timeanddate.com/worldclock/converter.html?iso=20211110T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Peter, Ken, Dan, Hadley, Amy, Yves, Tess, Rossen

Regrets: Lea

### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

Amy: I've asked more questions and there hasn't been a response.

Dan: any action on spec or issues?

Peter: doesn't look like it

Dan: will ping

### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss

Ken: new doc called privacy framework

Dan: I asked whether the privacy framework doc could point to the privacy principles doc. Jeffrey Yaskin made a [PR to do that](
https://github.com/WICG/trust-token-api/pull/93). Good sign. I was unclear what the other privacy principles doc was that they were pointing to, apparently a Chrome one, better to refer to a more community driven one. 

Ken: no spec yet?

Dan: we closed the captchas are horrible issue on the basis this is being worked on

Tess: one of the things is that it depends on the privacy pass stuff at ietf. I can't evaluate the crypto properties of that stuff. I would feel better if I saw some independent analysis of it by someone who does understand cryptography. I assume that's already happened and they can just link us to it.

Peter: i recall this was based on zero knowledge proof crypto

Tess: mozilla's position on privacy pass is 'defer', states they defer until the protocol and novel crypto principles have had more thorough security analysis. [I'll quote that in a comment.](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-963382808)

Dan: where are they talking about doing this work? [raises comment](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-963383997)

Peter: explainer is in wicg

Dan: then where does it go?

Peter: I see Hadley opened a couple of issues in their repo... two years ago. Which have been responded to but still open

Hadley: feels like there's still a situation where the user ends up having to choose a token issuer that isn't reputable.. I take that back, if the site has narrowed down the list of token issuers they will trust the worst thing it can do is track the user across other properties that are controlled by the same site.. I guess that is more of a privacy compromise than is possible just from the issuing site. I don't feel like the answer has been fully bottomed out. Did they flesh out the use cases? I'd like more time to dig into this.

### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @LeaVerou, @atanassov

Dan: there is a response..

Tess: if they're considering rethinking the syntax shouldn't we say cool come back to us when you do so, or not, so we can review the thing you want us to review instead of reviewing something that will radically change?

Peter: sounds right

Tess: they haven't asked us to review the alternative

### [SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

Dan: still blocked on FPS. 

### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov

Rossen: i think their answer to my question is these are non-transitional values. It is what it is.. they still need to make that more clear in the spec, otherwise they're not introducing anything necssarily new here in terms of transtions and animations, so from that point of view I think the feedback is to update the spec. Now the rest of this seems to be going towards closure.. I'll respond, can mark as proposed close

Peter: close in plenary?

Rossen: if they reply by then.

Peter: I'm concerned about making it non-transitional.. bad develoer experience

Rossen: auto is almost always non transitional. Don't know of cases where transitioning from or to auto is transitional

Peter: cases where it could be, but complicated

Rossen: I'm not going to ask them to invent better css out of that feature

Peter: fair enough

### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov

Dan: last thing I remember is this needs to be consolidated with all the other iframe proposals.. but not reflected in the issue.. we need to make some progress. I think Arthur's response to my question is compelling.

Hadley: did that end up in the explainer as well as responding to your question?

Dan: [writes response]. Are there other issues here? Is this linked to the other COEP / COOP thing where there was going to be a chrome trial period and we wanted to wait for the output of that? We had a discussin with mike west about it.

Tess: I commented with an issue that's still open, I don't think it's changed. On one hadn it makes sense to bucket it with the COOP and COEP stuff that we're waiting on. On the other hand this feels like a feature that is primarily a faster stop gap, peolpe can't adopt COOP and COEP yet because it's hard, maybe we're doing them a disservice by delaying.

Dan: we should close it on the basis of thanks for that information? Looks good as a stop gap

Tess: and please make progress on the open issues.. The name is terrible and actively misleading.

Dan: other question is where does this go?

Tess: I'd expect HTML. It's an iframe attribute

```
Thanks @ArthurSonzogni  that's very helpful. Can this info be brought into the explainer to make that document more clear (including the linked user needs)?  This looks good to us on the basis of it being a stopgap. Can you please progress the open issues including the one [Tess pointed to](https://github.com/camillelamy/explainers/issues/20). Spec-wise where is this going? Is this headed to HTML?
```

Dan: proposed close, for plenary

### [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @kenchris, @hadleybeeman

Dan: what's the current status?

Hadley: can come back to this next week, need to dig in

Dan: I want to know the implementation status. Worked on in the Web Payment WG. Multiple orgs working on it. What are the real issues?

Peter: Chrome shows shipping in 95, no signal from firefox or safari

Dan: we could ask multistakeholder

Ken: Stripe etc have been testing this. As I understand, we have this 3D secure in europe, whenever I use my card it has to go through this other authentication thing with my bank, I have to auth with an app on my phone. ???? Webathn and FIDO will provide the same security and avoid all these extra steps ?????

Tess: of issues I raised, one was answered to my satisfaction. Not excited that they're leaving in the callback mechanism for the future, but raising that didn't change anything.

Peter: come back to this next week

## Breakout B

Present: Peter, Rossen,

Regrets:


### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

### [WebTransport review request](https://github.com/w3ctag/design-reviews/issues/669) - @plinss, @atanassov


## Breakout C

Present: Dan, Ken, Amy, Yves, Hadley

Regrets: Lea


### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou, @kenchris

Ken: someone new is taking over.. maybe Intel

Dan: so nobody currently driving this?

Ken: officially they're still working on it. There are people with interest in it, but can't commit to anything. Hopefully will know soon

Dan: [...sounds like some resourcing issues...]

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris

Dan: they have responded, sounds like they're still waiting [writes comment]

Amy: response about locking down other APIs looks good, if they're actually going to do it. Even if they just mention it in privacy considerations as potential mitigation that'll be a start

## Plenary Session

Present: Peter, Dan, Yves, Lea, Hadley, Rossen

Regrets: Sangwhan, Amy, Ken

### Breakout Rollup

#### Breakout A

Dan: [gives run-down]

[We agree to **close** CSS contains intrinsic size.]

#### Breakout B

#### Breakout C

### Issue Triage

