# TAG Teleconference
#### 10-12 July 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-07-10](https://www.timeanddate.com/worldclock/converter.html?iso=20230710T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [Detect UA Transitions on Same-Document Navigations](https://github.com/w3ctag/design-reviews/issues/834) - @hober
* [Disabling UA transitions for same-document navigations](https://github.com/w3ctag/design-reviews/issues/835) - @hober, @LeaVerou
* [WebRTC-SVC (Scalable Video Coding) ](https://github.com/w3ctag/design-reviews/issues/837) - @hober, @torgo
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov
* [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

### Breakout C (APAC / Europe) - [2023-07-11](https://www.timeanddate.com/worldclock/converter.html?iso=20230711T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-07-13](https://www.timeanddate.com/worldclock/converter.html?iso=20230713T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Amy, Dan, Yves, Hadley

Regrets: Peter

### F2f w/c 31st July

Yes: Dan, Hadley, Amy

No: Yves

### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo



### [Detect UA Transitions on Same-Document Navigations](https://github.com/w3ctag/design-reviews/issues/834) - @hober

### [Disabling UA transitions for same-document navigations](https://github.com/w3ctag/design-reviews/issues/835) - @hober, @LeaVerou

### [WebRTC-SVC (Scalable Video Coding) ](https://github.com/w3ctag/design-reviews/issues/837) - @hober, @torgo

### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

Yves: they changed their API and now it's using a concifg object that is stored in the shared storage.

Dan: So dependency on shared storage

Yves: yes and negative feedback...

Amy: [mentioned in webkit standards position](https://github.com/WebKit/standards-positions/issues/173)

Amy: config also seems more complicated than src. Also hooks into turtledove/fledge "Protected Audience"

Yves: this config is a way to add context or state to URLs, many people wanted this in the past

Lea: Does the dependency on shared storage improve the developer or user experience? We should ask what is the plan if the opposition continues, do they have a plan b?

Lea: what does the config class look like? we have a principle in the works that any class input to an api should also be available as a plain object

Yves: the fact they are changing from just using a url to a config object that just has a url inside is to keep more information/context about that url. Something that has been used in manyp laces to add context to a specific url. Not sure it's a good thing in general. What's the motive behind that? a URL should be self describing

Lea: the code example is more of a sketch. I can't find any description of these objects. Is it a data centric class or not?

Hadley: [in the spec](https://wicg.github.io/fenced-frame/#fenced-frame-config-interface)

Lea: interface where everything is an attribute... which accepts a string

Amy: the spec answers my question.. cannot be constructed manually from JS

Lea: this seems ergonmically bad, but there can be tradeoffs with security/privacy

Amy: presumably something to do with the url needing to be obscured by the browser... but I don't understand why that prevents the manual construction

Lea: I'd love to see an end to end example.. Even if advertising is the primary use case. Site A wants to have ads. Site B provides privacy-respecting ads. How does this work? What code do they use?

Dan: I don't know.. i'ts not written like that. We need a primer

Lea: it says it can't be constructed from js... but they have an example in their readme that does new FencedFrameConfig. Complicated. I can't tell if the use case requires this kind of complexity.

Lea: is the primary use case to protect user priacy against instances like embedding the facebook like button

Dan: I think so. But it's described in such an abstract way. "The ability to correlate the user’s identity/information on the embedding site with that on the embedded site." Seems to be that scenario.

<blockquote>
Hi @domfarolino - Some notes from our TAG breakout today:  We're noting that we had previously reviewed an earlier version of this spec and given it a positive review. In fact, we had also specifically called it out as a positive development in our finding on [Improving the Web Without Third Party Cookies](https://www.w3.org/2001/tag/doc/web-without-3p-cookies/#use-cases-previously-met-by-third-party-cookies).
  
We're concerned that the changes to this API include Shared Storage as a dependency. Please note that not only does this not have multi-stakeholder support, but important stakeholders have actively expressed opposition to it: e.g. see the [Webkit Standards Position comment](https://github.com/WebKit/standards-positions/issues/173#issuecomment-1584609387), by @annevk and the [Mozilla Standards Position](https://github.com/mozilla/standards-positions/issues/646#issuecomment-1238792961). We've also noted this as an issue in [our ongoing review](https://github.com/w3ctag/design-reviews/issues/747) of Shared Storage. Can you please clarify – is there a dependency on Shared Storage? Does this dependency improve user experience or developer experience of this feature? What's your plan in the (very likely) case that Shared Storage is not implemented by other browsers?

We are actually [working on a design principle](https://github.com/w3ctag/design-principles/issues/11#issuecomment-1515585583) that would state config objects should also accept plain object literals whenever possible. Would that guidance be helpful in your design process?
  
We appreciate the thorough job done on documenting this API. Looking through the [use cases](https://github.com/WICG/fenced-frame/blob/master/explainer/use_cases.md) though, we're struggling to find the user need. We're noting the goal articulated in the [main explainer](https://github.com/WICG/fenced-frame/blob/master/explainer/README.md#goals) but what's missing is a simple articulation of what benefit the user derives from the inclusion of this API in the platform - from the web user's point of view.  We'd also like to see an explanation and code example of how the API is used in its most simple form.
</blockquote>

Dan: [posts comment](https://github.com/w3ctag/design-reviews/issues/838#issuecomment-1629360709.)

### [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov

### [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou

### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou


## Breakout C

Present: Dan, Amy, Sangwhan [second half]

Regrets: Yves, Sangwhan [first half], Max



### Fenced frames again

Fenced Frames is NOT dependent on Shared Storage!

Followup to ask for explainer improvements, though.

### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

Dan: asking for clarity about distinguishing between local file system and Bucket file system. Does it add additional security guarantees for the local filesystem?

Sangwhan: what do normative security guarantees look like in a spec? Eg. if you say the UA must detect malware that's a wide net...

Dan: the user agent must not allow files to be moved into protected directories

Sangwhan: that's defined

Dan: it was not normative

Sangwhan: you'd have to ensure that the spec is always up to date to the OS specs. That becomes a bigger spec than the spec itself..

Dan: I don't think the spec needs to normatively define every location which is a protected directory. How does this make it clear to implementers that they must implement protections against this being used to manipulated files in protected areas? Arguably things like the downloads directory is a protected area, as Peter was mentioning. Can we ask them to strengthen the language? Based on this change they've made, which is great, that they can differentiate - what does that enable them to do to allow for protecting users? I can just ask that.

Sangwhan: fine to ask. It's difficult to define normatively.

### [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

Amy: they will be working on it in the next draft charter.  They also replied about Matter. 

Dan: *reached out to Michael via email*

### [Sustainability of Bundling and Caching](https://w3ctag.github.io/caching-bundling-sustainability/)

Sangwhan: ready to ship

Dan: any feedback you've received?

Sangwhan: I've received some... 

Amy: suggest if there is feedback you're not going to address then... take it and explain why you're not going to address.

Sangwhan: need a better abstract.

Dan: how do we get to publishing? Over the next couple of weeks?

Sangwhan: I will process feedback comments that are actionable... 

Sangwhan: I've made some changes in the google doc, so I'll bring those to github

Dan: can changes be made in github now, and issues raised be raised in the public issues stream?

## Plenary Session

Present: Peter, Amy, Dan, Tess, Hadley

Regrets: 

### F2f w/c 31st July

Tess: could do more of a f2f than normal, but will still be recovering from CSS meetings etc...

Peter: not available on 2nd and probably after

Hadley: I can make that week

Dan: will schedule

### Breakout Rollup

#### Breakout A

##### Fenced Frames

*we discuss the situation with Fenced frames*

https://github.com/w3ctag/design-reviews/issues/747#issuecomment-1629533922

Dan: we need them to be clear how it can be used in isolation without dependencies

Amy: *explainer* ad aggregation, reporting stuff... getting info about ads... https://github.com/WICG/fenced-frame/blob/master/explainer/fenced_frame_config_context.md - we need to make sure this doesn't weaken the privacy protections this brings...  We need to re-review this.

Tess: I will take a look.

Amy: also turtledove / fledge / protected audience seems to be the same thing.

Peter: I am seeing references to buyers and sellers in the spec. Presuming it's being designed purely to run advertising, auctions

Amy: when we first reviewed we asked about additional use cases besides ads - but now it looks very ad specific.



#### Breakout C

### [WebRTC-SVC (Scalable Video Coding) ](https://github.com/w3ctag/design-reviews/issues/837) - @hober, @torgo

Dan: Dom was asking for a eta

Tess: only major change.. sounds like a good thing. 

Dan: we reviwed media capabilities - satisfied with concerns. Concerns were that it was already shipping. Multistakeholder?

Tess: I think it has wider support

Dan: [supported across](https://developer.mozilla.org/en-US/docs/Web/API/Media_Capabilities_API) all browsers according to MDN - data maintained by [Open Web Docs](https://openwebdocs.org) - thank you Open Web Docs.

Tess: need to verify what they've said is the only substantive change.... doing a [diff](https://services.w3.org/htmldiff?doc1=https%3A%2F%2Fwww.w3.org%2FTR%2F2019%2FWD-webrtc-svc-20191022%2F&doc2=https%3A%2F%2Fwww.w3.org%2FTR%2F2023%2FWD-webrtc-svc-20230417%2F), looks like every word in the spec has changed. Could be editorial, but difficult to confirm the assertion that only one thing changed.

<blockquote>
Hi folks - 
  
Thanks for sending us this review.  Given what @adoba wrote above concerning the changes and the fact that Media Capabilities API [itself enjoys multi-stakeholder support](https://developer.mozilla.org/en-US/docs/Web/API/Media_Capabilities_API#browser_compatibility), we'd like to close this review. However, it looks to us like a lot of additional changes were made to the spec. @dontcallmetom can you confirm that this is the only substantive change?
</blockquote>

### Issue Triage
