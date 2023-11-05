# TAG Teleconference
#### 30 October - 01 November 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-10-30](https://www.timeanddate.com/worldclock/converter.html?iso=20231030T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov
* [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman
* [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman
* [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman
* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

### Breakout C (APAC / Europe) - [2023-10-31](https://www.timeanddate.com/worldclock/converter.html?iso=20231031T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman
* [Web Audio API: User-Selectable Render Quantum Size](https://github.com/w3ctag/design-reviews/issues/895) - @ylafon, @maxpassion
* [Tag review request for the "Dubbing and Audio description Profiles of TTML2"](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-11-02](https://www.timeanddate.com/worldclock/converter.html?iso=20231102T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Amy, Peter, Yves, Lea

Regrets: Dan, Rossen


### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov

Yves: proposed closing. Rossen wanted to sync up with Tess, not sure if something happened

Peter: I think they're working on it

### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov

Lea: from preliminary state of html results, we had a question on that feature that had a high interest rating: 32% of people who hadn't used it said they were interested

Peter: some authors do delay injecting to try to block rendering. In general afraid of efforst that allow authors to add extra blocking, can mess things up

Lea: are these use cases better served by something less dramatic? eg. on async inserted stylesheets.. but that's not the use case. What's the usecase for an async inserted stylesheet? Is it view transitions?

Peter: looks like it

Lea: understand the idea about exposing web platform primitives, but is this really something we want to expose? Can't the browsers just do this? In general expose all the primitives to authors, but this could be harmful if used improperly. Would it make sense to block rendering on a subtree instead of the whole document? Blocking until a resource loads doesn't justify blocking rendering of the whole document

Peter: their use cases talk about situations where you'd only want to block part of the document

Lea: without view transitions are the rest of the use cases common enough to warrant the additional complexity? Shouldn't it stay browser magic for a while until we figure out the best solution?

Peter: tend to agree, but we've had this for a while. There's a long discussion in their repo. Also a note about how it can be done with computed style. A list of view transition names. Seems to be violating the priority of constituencies. Preference is to keep it automatic

Lea: I agree

Peter: hesitant to jump in without Rossen and Tess

### [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

### [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman

Amy: nothing on TR space, trying to figure out if they're going to CR... looks like it from their repo, but no FPWD. Oh, the link in their spec is broken. Looks straightforward and no major architectural implications.

Peter: i18n support?

Amy: punts that to JSON Schema spec

### [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman

### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss



## Breakout C

Present: Amy, Dan, Yves

Regrets: Sangwhan, Max, Hadley

### Solid Charter Review

Amy: Is it too late? Feedback drafted from me and Sangwhan

Yves: AC has voted against.

Dan: I see our feedback as async to that - TAG feedback could probably be useful if they are looking to rewrite the charter proposal.

*reviewing feedback*

Dan: I think that some working groups take as an input the reports from a community group - I can think of immersive web as one example where the CG develops specs and the specs are brought over to the working group once they are sufficiently mature and implementation work has begun...

Amy: they haven't presented these as inputs - they've just said "here is our thing"

...

Dan: why is that different from the immersive web community group working on the AR spec in the CG and then bringing it over to the WG for further standardisation?

Yves: in the case of immersive web the thing is that it's not bound to one particular technlology. It can be bound by one technology, but the title of the community group hints that they want to do something immersive and figure out the best solution. In the case of the solid community group, solid is the product of interest. The issue is that it's bound to a particular preexisting solution. Discussed in the CG but without input from the other stakeholders. That's why I see it as different from the immersive web case.

Dan: would like to be more foreceful in question about eg. how solid notifications protocol relates to web notifications... if they're building something in those spaces it needs to integrate with those things, or have a good explanation of why it's not

Amy: yeah

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

### [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman

### [Web Audio API: User-Selectable Render Quantum Size](https://github.com/w3ctag/design-reviews/issues/895) - @ylafon, @maxpassion

### [Tag review request for the "Dubbing and Audio description Profiles of TTML2"](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman


## Plenary Session

Present: Max, Peter, Dan, Hadley, Amy

Regrets: Sangwhan

### Solid Charter Review

*Feedback ready*

Dan: We came up with some feedback in Breakout C... review...

*We leave feedback here: https://github.com/w3c/strategy/issues/377#issuecomment-1790209071*

### Breakout Rollup

#### Breakout A



#### Breakout C

### Issue Triage
