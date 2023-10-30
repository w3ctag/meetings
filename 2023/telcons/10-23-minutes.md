# TAG Teleconference
#### 23-25 October 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-10-23](https://www.timeanddate.com/worldclock/converter.html?iso=20231023T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov
* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov
* [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov
* [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss
* [CSS State Container Queries](https://github.com/w3ctag/design-reviews/issues/885) - @LeaVerou, @atanassov
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov

### Breakout C (APAC / Europe) - [2023-10-24](https://www.timeanddate.com/worldclock/converter.html?iso=20231024T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman
* [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman
* [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman
* [Web Audio API: User-Selectable Render Quantum Size](https://github.com/w3ctag/design-reviews/issues/895) - @ylafon, @maxpassion
* [Tag review request for the "Dubbing and Audio description Profiles of TTML2"](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-10-25](https://www.timeanddate.com/worldclock/converter.html?iso=20231025T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
-----


## Breakout A

Present: Amy, Peter, Hadley, Rossen, Lea

Regrets: Dan, Sangwhan, Yves


### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov

Rossen: not sure where this is going. No engagement from anyone in accessibility or DOM space. There was some initiative by rakina .. nothing from pinging people. Bigger motivation at the time was the way the different implementations were handling focus. Discrepency between trident and gecko and blink/webkit. Blink/webkit focus management was pretty consistent. Not the case with gecko and trident. Since then trident is no longer. Don't recall the differnce between gecko and blink and webkit.. the rest is trying to essentially clarify how does the focus element vs tab index vs active element internally represented and how is it exposed to the web. That's the write up that we were asking for so we can have a better explainer. We can close it.. keeping it open hasn't resulted in anything fruitful.

Peter: nice to not have this hanging over, but we could wait until spring and see if anyone new wants to move it forward

### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

Peter: they asked us to reopen this.. and have asked some questions

Amy: I don't think I have any insight for these questions

Peter: Let's review and look next week

### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

Hadley: they're intending to ship enhancements.. don't look like massive changes to the overall api, but we haven't given a clear response on that... I would like to talk to Tess about this

### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov

Rossen: needs Tess... plenary?

### [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov

Rossen: initial lightweight feedback, well received... it's complex. If the system is already under heavy load you'll experience different performance characteristics compared to if it wasn't. This is one way of allowing you to better profile your payloads. Straightforward from addition pov. 

Peter: I asked about side channels and they answered with a question. Also about whether something comes out of a cache or not.. curious if someone can use this flag if the system is lying about other metrics.. depends on how it's implemented. There are other cases where the system is going to load it from the cache but pretend it's nto loading it from teh cache so you don't get a timing attack. Is this going to report that the system is under high load or not? If the system isn't hitting the network it's hitting the cache maybe this would reveal that the other api is lying and expose information

Rossen: the cache api or the performance metrics api?

Peter: the perf metrics of loading. Faking a network request but pulling something out of the cache

Rossen: the system is under normal load, and your nativation takes a long time vs a short time?

Peter: maybe under normal circumstances if the resource wasn't in the cache your system would be under heavy load, but now it's in the cache but your system is pretending to load it, but the system isn't under load, by exposing the system load you can infer that this really was cached after all and we negated the mitigation in the other place where we were lying about the fact it was in the cache. Not perfect, but it's information. Other things like battery status where people can use very scant information to pull pretty accurate information

Rossen: I can remember the battery discussions.. the strong feedback from mozilla at the time. Not sure how this compares to it though

Peter: not convinced this is a problem. Just concerned that it might be and I'd like people who know better to look at it. I can leave the feedback.

Rossen: trying to wrap my head around how detecting of the cache usage happens with this new entropy state. Let's see what they come back with

### [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss

Lea: added pending external feedback, that's the status

Peter: anyone else to ping? I can ping Yoav

### [CSS State Container Queries](https://github.com/w3ctag/design-reviews/issues/885) - @LeaVerou, @atanassov

Lea: seems great, does address real author needs. What percentage of use cases would be esatisfied by container queries. Eg. stack elements with position sticky, want to style stack element not descendents. At least it introduces a workaround whereas right now you have to use js. Didn't get the part about a two pass rendering update that this introduces. Does anyone understand it better?

Peter: cycles in rule matching you avoid with container queries but if you detect something being stuck and you change sizes of things it could no longer be stuck, right?

Lea: can it? Something that is stuck is also positioned

Peter: but it can scroll or be stuck to the edge based on the scroll position

Lea: in my opinion cycles are something that prevents implementers from implementing css that might involve cycles, it's not usually usability concern. A lot of very useful features are not being done because they could introduce cycles. If this has implementer support I'm not that concern. Remember when I proposed a design principle that css features could not have cycles? Peter said rather not because lots of useful things can introduce cycles. If implementers are happy I'm happy.

Peter: agree with that. I don't think the fact it can cause cycles is a reason to not do it. CSS just needs better detection and resolution of cycles. If they're willing to do the work of dealing with it then great.

Rossen: agree. Is this different than the scroll driven animations have? If it exacerbates it or it's more or less the same.. at the high level as a proposal I'm happy with it.

Lea: Are implementers happy with this? Everybody seems to be... there are no signals from mozilla or safari on the chrome status issue. I don't know if standards positions have been filed

Rossen: it's also an early review

Lea: [writes comment]

### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov

Rossen: first time around the work explained was very similar to efforts worked on by dbaron and emilio that describe what are blocking vs pipeline flushing states in the css subsystem, and ... push to plenary, discuss with Tess. Sounds like there was some tpac session on it. Missing context.

## Breakout C

Present: Amy, Max

Regrets: Dan, Sangwhan, Yves


### [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman

Hadley: don't see any problems. Minor niggles on their response about use cases. Can easily see this  being an opportunity for joining things up further down the line. Having said that it's hypothetical - no particular overlap they should be working on. Just makes me nervous about the self-imposed vaccum. Not concrete enough to put that back on the WG. We can sign this off.

### [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman

[bumped]

### [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman

Max: had similar opinion to Amy about security and privacy

Amy: did you understand Orie's reply?

Max: they mentioned the privacy conern in their explainer.. but they don't explain how to address this

### [Web Audio API: User-Selectable Render Quantum Size](https://github.com/w3ctag/design-reviews/issues/895) - @ylafon, @maxpassion

Max: not sure whether this api.. it's used by one particular web application, to set the rendering frequency of the device. Wondering whether this will apply to other applications. Is it per application? Should not have any influence to other applications running on the devices, one particular application wants to use it. [will leave comment]

### [Tag review request for the "Dubbing and Audio description Profiles of TTML2"](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman

[bumped]

## Plenary Session

Present: Peter, Hadley, Max, Amy

Regrets: Dan, Sangwhan, Yves

### Breakout Rollup

#### Breakout A

### Private aggregation 

Bumped to next week

## Verifiable Credentials Status List

Hadley leaving comment asking for clarification

#### Breakout C

### Issue Triage
