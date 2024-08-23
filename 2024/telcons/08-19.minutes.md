# TAG Teleconference
#### 19-21 August 2024

---

## Agenda:

### Breakout B (California / Europe)  - [2024-08-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240819T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo
* [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon
* [Early design review: Storage Access Headers](https://github.com/w3ctag/design-reviews/issues/982)

### Breakout D (California / Australia) - [2024-08-20](https://www.timeanddate.com/worldclock/converter.html?iso=20240820T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Spec review for Snap Events](https://github.com/w3ctag/design-reviews/issues/943) - @hober, @martinthomson
* [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober
* [Spec review for scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/966)
* [Design Review: Prioritized Task Scheduling (big picture)](https://github.com/w3ctag/design-reviews/issues/967)

### Breakout E (Europe / China) - [2024-08-21](https://www.timeanddate.com/worldclock/converter.html?iso=20240821T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Before 6 August 2023 -- Guidance on Applying WCAG 2 to Non-Web Information and Communications Technologies (WCAG2ICT) - Google Chrome - Daniel (w3.org)](https://github.com/w3ctag/design-reviews/issues/973)
* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @rhiaro, @hadleybeeman
* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962)
* [Vibration API](https://github.com/w3ctag/design-reviews/issues/971)

### Plenary Session - [2024-08-22](https://www.timeanddate.com/worldclock/converter.html?iso=20240822T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout B

Present: Peter, Yves, Amy, Tess

Regrets: Dan


### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

Hadley: following a trail of links... we encouraged them to engage with PATCG about a month ago. Does this apply here?

Peter: we declined attribution reporting and encouraged a more single consensus based approach. This might be that. This is coming from PATCG. Anyone have more context?

Yves: [Mozilla standards position](https://github.com/mozilla/standards-positions/issues/805) with a comment from Martin. Would be good to know if it's in PATCG why we are reviewing it right now. Is it still under discusison or do they plan to move to the next step?

Peter: the readme says it has not been adopted by the PATCG. We could say to come back when the PATCG adopt this

Hadley: request also says it's being driven by privacy sandbox

Amy: sounds all out of date

Peter: readme was updated wthin the last month. Strong connection to Protected Audience bothers me a lot. also seems to be all about ads.

Hadley: ...

Peter: Martin is expressing general support for tools to aggregate... 

Yves: is it related to firefox doing privacy preserving ad relevance

Peter: guess there isn't any relation

Yves: ..

Peter: intent to ship, and have made changes since the review request. We closed Protected Audience unsatisfied, it's connected.

Yves: if there is a dependency...

Hadley: I think getting consensus out of the PATCG applies

Amy: we could ask Martin/Tess/Jeffrey if they know more about PATCG

Peter: revisit at plenary?

Hadley: I'll ask in core-tag

*Tess appears*

Tess: last I heard there was an ongoing effort to merge the three proposals and I think i'ts pretty far along but haven't checked in a while

Peter: should we wait to review until things settle down?

Tess: that's what we agreed in Seattle

Peter: there was another one...

Tess: there's three. We shouldn't review any of them.

Peter: chrome intent to ship asking for TAG sign off

Tess: can't they wait until they're combined and ship that..? If it seemed unlikely they were going to converge I'd be all for reviewing all three, but they seem to be figuring out the middle ground themselves

Hadley: and if that were the case the questions asked would be framed differently

Tess: rather hear what Martin has to say before we close

Hadley: up for declining it, but I've asked so give them a chance to reply

### [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo

Amy: no response to our requests for more info in the explainer

Peter: I'll ask for updates

### [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon

Yves: it makes sense. Would require people well versed in intricate optimisation of js engine to say if it's okay. They considered i18n, many issues, it makes sense

Tess: you can tell they put a lot of effort into it. We don't have the expertise. It's very dense. It's probably fine.

Yves: the fact they were discussing issues with different encodings and things like that is good

Tess: if you want someone who is not working on it and has all the domain knowledge...

Yves: the number of people able to know that is very limited

Amy: if there are no conflicts or issue with other things in the web platform, that's probably all we can bring at this point

Tess: I don't think it's architecturally unsound to do this. They do seem to be tackling someof the challenges head on.

Yves: did they have i18n review?

Tess: don't know what kind of HR the WASM folks do. A lot of this happens in the CG.

Yves: Looks good to us, but if they are looking at an edge case please ask the i18n WG to review this

Tess: works for me

Draft closing comment, to be reviewed before plenary:

<blockquote>

Thank you for your patience while waiting for us to take a look at this.
  
Whenever dealing with strings on the web platform, <abbr title=internationalization>i18n</abbr> issues inevitably arise. Have the <abbr title=WebAssembly>WASM</abbr> folk gotten i18n review of this?
  
Otherwise, the <abbr title="Technical Architecture Group">TAG</abbr> currently lacks domain expertise in the internals of JavaScript and WASM implementations, so we're ill-equiped to do a deep dive here. You've clearly put a ton of effort into this, and your document more than adequately addresses the handful of things that came to our minds while reviewing it.
  
We'll close this review for now. Please let us know if your design substantively changes, and we'll take another look.

</blockquote>

### [Early design review: Storage Access Headers](https://github.com/w3ctag/design-reviews/issues/982)

Amy: there are no user stories involving actual users :'(

Tess: the thing asking for storage access has a frame in the page. There are some sites that don't have a frame. What they're looking for here is if you use http headers to convey storage access information you won't need an iframe in the page to get at those cookies. The storage access api has a user gesture requirement, by design you don't get storage access unless you ask the user and the user grants. If it's rpeviously granted the promise resolves immediately but you have to call it and the user has to thinka bout it. if it's happening at the network request level when and how do we prompt the user? Do we block th enetwork request until we've got a response from the user? Very unusual circumstance to make fit with the storage access api privacy model, that everything is gated on meaningful user consent. I understand they don't want to rearchitect the code that doesn't require an iframe but... user needs something to click on. This makes the storage access api adoption a bit of a smoother expeirence for some existing code paths which potentially increases adoption overall so it's tempting. But feels like it's fundamentally subverting the design of the api. Jeffrey and Martin will have different opinions. Storage access api is spposed to be inconvenient. That's the idea.

Peter: feature is access without ser interaction "in cases determined to be safe". How are they determined to be safe?

Hadley: a list in the browser? They also say they are working with PrivacyCG chairs to adopt as a work item. There is no multi stakeholder approach here.

## Breakout D

Present: Tess, Martin, Peter

Regrets:


### [Spec review for Snap Events](https://github.com/w3ctag/design-reviews/issues/943) - @hober, @martinthomson

Closed satisfied

### [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober

Propose close

### [Spec review for scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/966) & [Design Review: Prioritized Task Scheduling (big picture)](https://github.com/w3ctag/design-reviews/issues/967)

Doing some offline consultation with other experts on event loop


## Breakout E

Present: Max and Martin agreed to call this one off.

Regrets:


### [Before 6 August 2023 -- Guidance on Applying WCAG 2 to Non-Web Information and Communications Technologies (WCAG2ICT) - Google Chrome - Daniel (w3.org)](https://github.com/w3ctag/design-reviews/issues/973)

### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @rhiaro, @hadleybeeman

### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962)

### [Vibration API](https://github.com/w3ctag/design-reviews/issues/971)


## Plenary Session

Present: Peter, Martin, Tess

Regrets: Matthew

### Breakout Rollup


### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

First attempt:

> We appreciate you bringing this to us.
> The relationship with the aggregated attribution proposals is particularly difficult.
> The PAT\[CW]G is working on the synthesis of three different proposals.
> We'd like to encourage you to spend time on the convergence of those proposals.
>
> The additional value that comes from a more generic version of the same mechanism is where this is most challenging.
> We recognize that value of generic features, but insist that they be justified by their use cases.
> The TAG has already come to a conclusion about Protected Audience (#723), which is one of the identified uses of this.
> We find the building of market demographics across sites to be insufficiently compelling as a justification.
>
> With that all in mind, we're going to decline this review.

Jeffrey's improved version, minus EWM:

> We appreciate you bringing this to us. We see that Chromium has already shipped this API, so this comment primarily applies to your efforts to bring it to other browsers. We [understand this to be a generalization](https://github.com/patcg/private-measurement/issues/22#issuecomment-1734280125) of the three advertising attribution proposals that the PAT\[CW]G is working to unify, and we think it'll be most productive to finish that work before refining this generalization.
>
> We recognize that it's usually beneficial to generalize features, but when those features come with privacy risks, we think it's important to balance those risks against the value of the additional use cases. This explainer only identifies two additional use cases. One of these is Protected Audience, about which the TAG has already expressed concerns (#723). We did not find the building of market demographics across sites to be sufficiently compelling to justify this whole generalization.
>
> Given that the short term focus should be on finishing the attribution API, we're going to decline this review. However, if more use cases turn up for the generalization, we'd be open to looking at it again.


### [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon

<blockquote>

Thank you for your patience while waiting for us to take a look at this.
  
The <abbr title="Technical Architecture Group">TAG</abbr> currently lacks domain expertise in the internals of JavaScript and WASM implementations, so we're ill-equiped to do a deep dive here. You've clearly put a ton of effort into this, and your document more than adequately addresses the handful of things that came to our minds while reviewing it. We don't see any obvious issues with the proposal as it stands.
  
We'll close this review for now. Please let us know if your design substantively changes, and we'll take another look.

</blockquote>

Posted and closed as satisfied.


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


### Breakout Rollup


#### Breakout B

#### Breakout D

#### Breakout E

### Issue Triage
