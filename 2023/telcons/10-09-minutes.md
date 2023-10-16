# TAG Teleconference
#### 09-11 October 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-10-09](https://www.timeanddate.com/worldclock/converter.html?iso=20231009T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791) - @LeaVerou, @plinss
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov
* [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov
* [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss
* [CSS State Container Queries](https://github.com/w3ctag/design-reviews/issues/885) - @LeaVerou, @atanassov
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov


### Breakout C (APAC / Europe) - [2023-10-10](https://www.timeanddate.com/worldclock/converter.html?iso=20231010T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [ewp pull request](https://github.com/w3ctag/ethical-web-principles/pull/99) - @rhiaro, @hadleybeeman, @torgo
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
* [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman
* [ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/863) - @torgo, @maxpassion
* [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Specification Review: FetchLater API](https://github.com/w3ctag/design-reviews/issues/887) - @cynthia, @ylafon


### Plenary Session - [2023-10-11](https://www.timeanddate.com/worldclock/converter.html?iso=20231011T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Extending the PointerEvent with Unique DeviceId Attribute](https://github.com/w3ctag/design-reviews/issues/880) - @torgo, @atanassov
* [`inverted-colors` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/883) - @torgo, @atanassov
* [`prefers-reduced-transparency` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/881) - @torgo, @atanassov
* Offer from Google to talk about real-world-identity on the web.
* Solid charter review

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Yves, Rosson, Peter, Amy, Lea

Regrets: Dan

### Privacy Sandbox APIs gated behind attestation thing

On Topics, Shared Storage, Attribution reporting:

> FYI, Chrome plans to start gating shared storage API invocation behind the enrollment and attestation mechanism. (enrollment explainer, spec PR)

On one hand, I like that access to the APIs is restricted. On the other hand, I hate that google get to gatekeep this since they have a clear conflict of interest. Gatekeeping android development or whatever this way is one thing, but this seems deeply problematic for apis they want to standardise on the web platform.

### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

Rossen: last time we talked about it you had an action item to look through the issues that were being worked out.

Peter: I don't see how the three posted are related to what I was talking about

### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

### [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791) - @LeaVerou, @plinss

Peter: we deferred this because it was in flux.. do we think it's stable enough to review?

Lea: no. There are still a lot of outstanding issues. One of the most important ones imo that may affect what we think is .. the main problem was the implicit & and when authors would be allowed to omit the &. This evolved in a favourable direction towards the syntax that is easier for authors but more annoying for implementers. But right now there is another [issue about ordering](https://github.com/w3c/csswg-drafts/issues/8738) but I don't know if it's our place to comment on these things, we don't need to go hunting down issues.

Peter: how much is architectural vs details of css implementation?

Lea: exactly. Post to ask if it's time for us to review or if it's still in flux?

Rossen: +1

```
Hi there, sorry for the delay in following up on this. Is this ready for us to resume review? If so, could we please have an explainer that is up to date with the current syntax for this proposal and any major outstanding issues? Thank you!
```

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov

### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

Lea: we said we'll pause our review

Peter: [update milestone]

### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov

Yves: we were wondering about the use of those values in case of solution for the cache sustainability issue where you might serve from the cache without telling that it's from the cache. You ahve to be careful about what information you surface or not at the js leve. They responded that they agree that they need to do something similar. Basically we should close satisfied.

Peter: fine with closing. Minor concern that if the apis are going to start lying about whether something came from the cache how useful is this?

Yves: if you're using double key cache instead of getting things from the network, but serving from the cache but with a delay, but in that case you won't say it's from the cache as well. But it's not really lying, it's just that it's not from the double key cache, it's from the navigator cache via delay used to fake the fact it should have been from the network but it's not from the network

Peter: so the effective performance is the same as what the reported performance is, it's just the mechanism is not.. I guess that makes sense

Yves: as we are mimicking not serving from the cache..

Peter: you're not getting the perf benefit of a cache, but you are getting the network savings. I can see people wanting to measure the effectiveness of that, but it's probably not worth exposing that

Yves: you can measure it if it's same origin. Just that if you are loading the same resource from another origin you probably don't want to share that information. Only in that case it matters, not in the perf case of loading the page for the first time or reloading the same page

Peter: makes sense. Close?

[proposed close - plenary]

### [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov

### [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss

Peter: no response to Lea's last comment, 2 weeks ago

Lea: we can wait

### [CSS State Container Queries](https://github.com/w3ctag/design-reviews/issues/885) - @LeaVerou, @atanassov

### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @atanassov

### [`inverted-colors` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/883) - @torgo, @atanassov

Rossen: No explainer... such a small change though

Lea: It's so incremental, doesn't require TAG review

Peter: agree

Lea: fast track? 

Peter: naming is unfortunate, but good to close

### [`prefers-reduced-transparency` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/881) - @torgo, @atanassov

Peter: same as 883

Rossen: did we resolve on the syntax..?

Lea: webkit has a standards position against this because it adds a fingerprinting vector...

Yves: I tried to look at this and it's not properly explained. I couldn't figure out what is exposed more by using this. Apart from the fact that you're supporting that in the browser

Peter: one more bit of entropy for the user if the user has this setting turned on. Also true of 883.

Lea: accessibility needs outweigh tiny fingerprinting surface..

Peter: worth pausing to ask if there's a way to mitigate. In this case the benefit is worth the cost.

<blockquote>

We're happy to see this moving forward, so we will close this.
As part of the review we also looked at the [fingerprinting concerns raised by WebKit](https://github.com/WebKit/standards-positions/issues/145). Our opinion is that the user benefit outweighs the privacy concern. That said, exploring ways to mitigate this more generally without negatively impacting user experience, especially of users with accessibility needs, would be welcome.

Thank you for flying TAG!

  
</blockquote>


## Breakout C

Present: Dan Max Yves Amy Sangwhan

Regrets:


### [ewp pull request](https://github.com/w3ctag/ethical-web-principles/pull/99) - @rhiaro, @hadleybeeman, @torgo

Amy: *leaves review*

Dan: *squashes and merges*

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Sanghwan: *to follow up with Fergal*

### [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

Amy: Did anyone meet with them at tpac? I completely forgot we said we'd do this, and didn't make it to any of their meetings. Can we punt this? It doesn't feel like a priority, although it's an opportunity to get ahead of the game for their next charter..

Dan: to my knowledge nobody talked to WoT people at TPAC... 

Dan: considering how much we have on our plate right now I suggest we apologise and let them know we haven't been able to get to it but they should send us a review request during next charter period...

```
We're really sorry we didn't manage to arrange a time to meet with you at TPAC. We're going to close this for now, please could you file a new review request at a suitable time during your next charter period? We unfortunately don't have time for an early review of this at the moment, but will do our best to get back to you if we clear our backlog before we hear from you next.
```

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

Dan: there was some discussion about this at TPAC - reflected by [Rick Byers's comment from 3 weeks ago](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1723578050).

Sangwhan: I am mroe of a pragmatist... 

Dan: they want to switch to a trust model for embedding user data... they talked about PII Input as a name.. but it's a loaded term... but that's bikeshedding, the idea behind it sounded really good. Decouples the isue from autofill and makes it more about 

Sangwhan: 

Yves: question - is auto-fill only available on form inputs that re visible? Or can it be done for hidden fields?

Sagnwhan: i believe it can be done for hidden but in a "hackey" way... there are some hacks ... not standard behavior. 

Yves: auto-fill credit card info in a hidden field feels quite unsafe... 

Sangwhan: agreed. I'm okay with what they're doing here

Dan: I think the nuance expressed in Rick's comment addresses the issue we've raised. You could imagine how .. it's a semantic issue?  It makes more sense to me

<blockquote>
Hi @rbyers - Discussed briefly today and there is rough consensus that this is the right approach.  We'd like to see it written up in a revised proposal – is that in the works?
</blockquote>

### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo

Dan: Mozilla standards position is positive..

Sangwhan: everyone implements opfs

Dan: is the design okay?

Sangwhan: it's fine. Their response makes sense [closing comment]

Dan: concern being support for different types of filesystems

Sangwhan: that's not on this api, that's a different thing. You can use this with only opfs

Dan: I agree.. right now there's a multistakeholder label but I feel we shouldn't have that. Maybe if it's not intrinsically linked to filesystem access that doesn't have multistakeholder support this should be **satisfied**?

Sangwhan: this can be **satisified**. In terms of filesystem access on the web, one mechanism is contentious, OPFS is not contentious. Each origin gets a little virtual filesystem. This implements multiple readers and writers on both of them, but its api that works aainst the handles so it doesn't care about what backend it's using.  On the native filesystem support that's another thing, we should have a second discussion about that, it keeps on popping up whenever filesystem comes up.. the backend is very concerning. The APIs for the filesystem access that support both opfs and native are fine.

Dan: okay

**we agree to close as satisfied**

### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman

Sangwhan: can I get back to you in a week? I misunderstood what this is.

**bumps**

### [ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/863) - @torgo, @maxpassion

Max: No response from comment...  We gave them the comment that there is no standardization for URLPattern.  They gave some feedback...  

Dan: I don't think it's appropriate for the TAG to go chasing other browser vendors on behalf of Google...  My propoosal is to close this with "satisfied with concerns" - the concerns being that this is built on top of a spec that is not being standardized anywhere...  The design is fine and considering that as [Ken said](https://github.com/w3ctag/design-reviews/issues/863#issuecomment-1706146215) on sep 5, there's a polyfill available...

<blockquote>
We're going to go ahead and close this with "satisfied with concerns" - we're happy with the overall design but we remain concerned about URLPattern's status on the standards track.  Considering there seems to be a [way forward for standardization](https://github.com/WebKit/standards-positions/issues/61#issuecomment-1527486428), we'd encourage you to pursue that path.
</blockquote>

**closed with satisfied with concerns**

### [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman

Amy: I feel kind of stupid but I don't really understand Orie's response. Also it only answered half the questions.

Amy: let's punt and I can get some explainers... Tess wrote a blog post about polyglots which could be relevant..   But they've also gone to CR with most of the VC specs

**punts one week - Amy will work on getting more context**

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: ...same origin.. malicious apps.. exploits? Manifest file that in some ways mirrors the functions of FPS.. but on a web app basis.. we want to be clear about the scope

Yves: basically that. Also wondering why they don't do cryptographic verification of the other origin they want to add in like it's done for some other places. Like what we ask from miniapps. We want to ensure that the other origin that we want to cover allows being embedded in this web app. Nothing there that talks about that. 

Dan: given the response could you leave that feedback?

Yves: yes

Dan: it's a good response addressing the issues that we've raised. I don't think we should rely on something like safe browsing modes that are to protect users

Yves: thinking of things like universal links for ios and the equivalent on android which is always the canonical example I use

**punts to next week**

### [Specification Review: FetchLater API](https://github.com/w3ctag/design-reviews/issues/887) - @cynthia, @ylafon

Dan: we had a reply 3 weeks ago.. clarifying naming

Sangwhan: fetch later means any time between now and destruct.. but in reality it's as late as possible.. I'm okay with this

Yves: Same. When we first reviewed this we were concerned they were exchanging state using get and they seem to have fixed this. Okay to close.

**agreed to close - Sangwhan to leave closing comment**

### [Capture all the screens](https://github.com/w3ctag/design-reviews/issues/856)

Amy: We proposed close ages ago - can we close it?

Dan: [closes]

## Plenary Session

Present: Dan, Peter, Hadley, Rossen, Yves, Lea, Amy

Regrets: Sangwhan, Max

### [Extending the PointerEvent with Unique DeviceId Attribute](https://github.com/w3ctag/design-reviews/issues/880) - @torgo, @atanassov

**bumped to next week**



### Offer from Google to talk about real-world-identity on the web.

### Solid charter review


### Breakout Rollup

#### Breakout A rollup...

Rossen: Closed 2 issues in breakout C- short CSS proprosals for media features - transparency & inverted colors.

Amy: 3 other privacy sandbox ones - "Chrome plans to gate this behind ... method..." Reg process... you have to get a number (a company number) - it seems problematic for web platform.

Amy: first party sets -> related web sets. Spec has changed a lot. notes in the slack... 

Dan: let's discuss further and maybe we can have a focused call on this with Privacy Sandbox folks...

Any: still want to close Topics... 

Peter: 858 - marked as proposed closed... 

Rossen: will follow up offline with Tess and try to close.

#### Breakout C rollup...



### Issue Triage

*on 890 some debate on whether it's appropriate to do a TAG review at this time*

Rossen: as an early review it's Ok - if this is a review for something matyre then no...
