# W3C TAG Minutes Doc - Mon, 8 January 2024

## Agendas

### Breakout A (Europe / US) - [2024-01-08](https://www.timeanddate.com/worldclock/converter.html?iso=20240108T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov
* [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou, @torgo
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hadleybeeman, @atanassov
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [Adding a close event to MessagePort API](https://github.com/w3ctag/design-reviews/issues/923) - @hober, @torgo
* [New attribute to control UA-provided writing assistance](https://github.com/w3ctag/design-reviews/issues/924) - @hober, @matatk
* [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @hadleybeeman, @plinss

### Breakout C (APAC / Europe) - [2024-01-09](https://www.timeanddate.com/worldclock/converter.html?iso=20240109T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @cynthia, @torgo, @rhiaro
* [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman
* [TAG spec review of Storage Access Heuristics](https://github.com/w3ctag/design-reviews/issues/919) - @torgo, @rhiaro, @hadleybeeman
* [Navigation Activation Info](https://github.com/w3ctag/design-reviews/issues/921) - @torgo, @hadleybeeman
* [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman

### Plenary Session - [2024-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240111T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Progress on findings
* F2F Agenda Discussion
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
 
 
## Minutes

### Breakout A (Europe / US) - [2024-01-08](https://www.timeanddate.com/worldclock/converter.html?iso=20240108T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Yves, Matthew, Hadley, Lea

Regrets: Peter

#### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

Dan: heard some noise about from chrome on social media

Lea: I remember Tess had some comments but don't see them. Commonalities between this and window.open. Tess said the actual OS level picture in picture doesn't allow a lot of stuff from that. Should this hook into the native OS level picture in picture, or be a way to have windows that are always on top? I'm not clear what would be the difference. Would benefit from Tess's perspective.

Dan: seem to remember that Tess had input on how this would work in webkit - it wouldn't

Lea: not my recollection.. there are two components. Having a window always on top which is a concept on OSX as every operating system. My understanding is that there's always a picture in picture functionality that is separte from this concept, ipmlemented as a separate orthogonal feature. Not sure how it differs - is it UI or does it have other advantages? Like being optimised for showing video? The use cases here go beyond video.

Dan: specifically not video

Lea: then I'm not sure how the native PIP relates. Seems like what they really want a window that is always on top

Matthew: from briefly looking - an example they give is a highly custom video player, but that's no the focus. Speaking of focus... the word ofcus only comes up once in the explainer and it's about mental focus not browser focus. I don't see any mention at all ofhow they envision focus management - how do you get between the popup and where you were? I've not used this in real life but I'd be very interested as to what they're expectations are around that. Moving between the window and the document is something everyone is going to be able to need to do.

Dan: we could ask what the current state is, and see if Tess comes to plenary for further discussion

Lea: I don't see anything in the reply tha answers our questions about use cases... links to an entire thread on blink dev. Their first case is PIP with video, which exists. Seems that everything in there is something that is a window that can be on top, which has the benefit of ensuring a certain amount of browser UI around it, which prevents spoofing. I found [the comment referred to from dominic](https://groups.google.com/a/chromium.org/g/blink-dev/c/JTPl7fM64Lc/m/OfBZRdjEAAAJ) .. they don't think our advice is good... I'm not sure what this means

Matthew I think what he's saying is that you're only able to open one of these popups for a given page or tab. But it's unclear.

Lea: this could also be decomposed into a window.open concept

Matthew: There is something about window.open in the explainer: https://github.com/WICG/document-picture-in-picture?tab=readme-ov-file#since-this-is-pretty-close-to-windowopen-why-not-just-add-an-alwaysontop-flag-to-windowopen which I wonder if they added since we looked

Dan: where have they mentioned spoofing? Can't find it in the explainer

Amy: they said they added normative language in the spec

Lea: [reads it] sounds just like window.open. Generally an antipattern to introduce multiple features that do similar things in slightly different ways. Seems like none of the reasons not to extend window.open, but point to even more low level primitives that window.open needs. Seems like overfitting. Am I missing something?

Dan: what is 'enough ui'?

Matthew: imagine there's a tacit assumption that this window will only be shown as a direct result of user action, but can't find a mention of that in the exlpainer - is it too obvious or should we get it confirmed? Also does the window.open section answer any of our questions - I think it doesn't.

Dan: we should add that question about user action.. whether user activation is required is important

<blockquote>
  
Hi @steimelchrome thank you for bearing with us.  We're picking this back up today and trying to get you some useful feedback.

We're concerned about spoofing. There's some language in the spec about this now - great - but there is no discussion in the explainer about possible abuse cases and mitigations against those abuse cases - that would be very valuable. Also the language in the spec just says UAs need to provide "enough UI" which is a bit vague. Is there any non-normative language that could be added here to elaborate on the kind of UI that should be provided? Also, could you confirm that the PiP window will only be opened as a direct result of user action?

We're concerned about accessibility - specifically the explainer doesn't mention how focus management is expected to work - how will users move between the PiP window and the main document?

We are still concerned that from an author perspective, this introduces a feature that is very related to `window.open()` but solves subtly different problems. We saw the part in the explainer about this, but it may be useful to decompose the problem into the parts where `window.open()` behavior conflicts with what is desired here, and examine whether these primitives may be useful for `window.open()` as well. Based on the differences mentioned in the explainer, that does seem to be the case:
- a window that does not outlive its opener is definitely a useful concept for `window.open()`, in fact if we were to design `window.open()` today I'd argue it should be the default!
- Feature testing `window.open()` features is also a more general problem.

Decomposing this into lower level functionality that can be integrated in `window.open()` would also address the spoofing concerns as well.
An important question we need clarity on is, is there something that makes this functionality fundamentally incompatible with `window.open()` or is it about managing design & implementation effort?

Can you please let us know the current status and any response to these issues?

</blockquote>


#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
#### [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov

Hadley: we were unclear whether this reflected consensus of the 2nd screen wg... that nudged the poster to seek that consensus -- they planned to discuss at tpac. we haven't heard any update. i left a nudge to clarify - it would be good to understand whether this was the wg's consensus...

#### [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou, @torgo
#### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov

Yves: Tess and Rossen okayed closing this, satisfied

**agree to close, Yves to write closing comment - agreed satisfied**

#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

Lea: so – there is an existing value we introduced textwrap:balance - useful for headlines - often too draconian... so textwrap:pretty introduced as a high-level way to get nicer looking text balancing. The problem is that when the implementation shipped in chrome it only prevented ofphans... so devs got used to this... and it was seen only to prevent orphans... so not able to add new things. Our feedback was : give authors low-level control - but also if you ship the high level thing don't make it just do one thing... and they agreed... we also said "don't ship something that does one major thinng plus a minor thing" - and I see that koji asked for clarifications but we didn't reply... 

Dan: ask what current status is? major/minor feature type thing? looks like they've taken our feedback on board. According to chrome status other vendors support it but they don't link to standards positions. I wonder if they've received this type of feedback from other parties

<blockquote>
  
Thanks for bearing with us - we realize this response is late.
 
There's no way to quantify what is minor, **the end goal is to ensure that authors do not use this as a proxy for a single feature (preventing orphans)** which would prevent it from including more heuristics in the future. So in addition to preventing orphans, the property should control at least one more factor that is *noticeable* in common usage. 
  
Preventing "rivers of white space" in justified text is certainly not minor, but we'd love to also see something that makes a visible difference in other text alignment modes as well.
  
Again, this becomes less of a concern if lower level control over orphans ships at the same time (or earlier).

Also - can you please elaborate on the multi-implementer support - we see that the Chrome Status page lists Webkit and Mozilla as positive but does not link to standards positions.
  
</blockquote>


#### [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hadleybeeman, @atanassov



#### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
#### [Adding a close event to MessagePort API](https://github.com/w3ctag/design-reviews/issues/923) - @hober, @torgo

#### [New attribute to control UA-provided writing assistance](https://github.com/w3ctag/design-reviews/issues/924) - @hober, @matatk



#### [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @hadleybeeman, @plinss

### Breakout C (APAC / Europe) - [2024-01-09](https://www.timeanddate.com/worldclock/converter.html?iso=20240109T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Matthew, Hadley, Sangwhan

Regrets: Amy

#### [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @cynthia, @torgo, @rhiaro

Sangwhan: ... distilling a pattern ... the API shape seems to be fine... looking back... this is more of a design pattern ... we don't havea a princple... if this ships as is then this becomes a pattern....

Dan: what's the pattern?

Sangwhan: based on the webkit comment ... https://github.com/privacycg/storage-access/issues/102   "Don't re-invent access control and follow a similar pattern if you want to introduce access control..."  We could let this go an distill the pattern out ... into a principle later down the road...

Dan: propose closing this "satisfied" with the following comment:

<blockquote>
  
@archiv thanks again for sending this our way.  We're happy with the way this is proceeding. We're happy with the use cases and API shape.  And we're pleased to see the multi-implementer consensus taking shape.
  
</blockquote>

Sangwhan: +1

*no dissenters*

*closed as satisfied*

#### [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman

Hadley: they responded to us ... I'm a little concerned that Ian doesn't know of any unintended consequences...

Dan: we've raised the issue ... 

Hadley: we can't make him explore the unintended consequences... 

*discussion of security & privacy*

Sangwhan: i don't think this exposes additional bits of entropy... if you have prior knowledge of what features are available in a UA then you have same level of bits... however you'll get more info about the user and be able to triangulate the user better.. but don't know if this exposes extra info on that regard.

Hadley: that sounds consistent with Ian's review.

*discussion on how to push*

Sangwhan: it's not going to have multi-stakeholder support since permission policy is a chrome-only feature...

Dan: we should talk about this... why does permission policy not have better support?

Dan: suggest we close this as satisfied with concerns where the "concerns" are multi-implementer support.

Hadley: sounds sensible.

Sangwhan: feature / permission policy did have multi-stakeholder support... just hasn't been implemented...  We could ask again...  [So I'd prefer "satisfied"]

Hadley: but that's a signal...  We have other labels to indicate "please don't do this"... 

Sangwhan: sometimes implementers aren't building it but not against it ...

Hadley: important for us to champion multi-implementer support... a web that's interoperable... 

<blockquote>
  
We would really appreciate if you could do some additional review about unintended privacy consequences...  Could that work happen in WebAppSec maybe?
  
We remain concerned about lack of multi-implementer support for Permission Policy itself, as well as this proposal. Although this is out of scope for this review, it remains a general concern.  We'd like to encourage you to continue the multi-implementer discussions for permission policy.  Also do we have any indication of support from other implementers or stakeholders on this specific proposal?  
  
</blockquote>

Dan: ok we can come back to it in the plenary.

#### [TAG spec review of Storage Access Heuristics](https://github.com/w3ctag/design-reviews/issues/919) - @torgo, @rhiaro, @hadleybeeman

#### [Navigation Activation Info](https://github.com/w3ctag/design-reviews/issues/921) - @torgo, @hadleybeeman

Dan: One thing that comes to mind - the term Activiation is overloaded... 

Yves: change is only to add a link ... cross document...  Might have some privacy implications...  Unless it's accessible already using the history API...

Matthew: the explainer is a little minimal... I think both those points are good... It would be good to know if this exposes more information than what's before... 

Matthew: in the HTML spec most of the instances of activation are about user activation... https://html.spec.whatwg.org/multipage/nav-history-apis.html#navigation-activation-interface

Matthew: on MDN - there's a user activation of an interface ..  https://developer.mozilla.org/en-US/docs/Web/API/Navigator/userActivation

<blockquote>

Hi @noamr - thanks for sending this our way. 
  
A couple of initial questions we had:
  
1. regarding the naming of the API - it seems like the term "Activation" is a bit overloaded - in particular it's used in the context of user activation which is a completely separate concept. We're concered this could cause developer confusion. Have you consdered any alternatives?
  
2. what's the current state of this with regard to the HTML spec itself?
  
3. the security & privacy responses say that "It exposes information about the most recent cross-document navigation." It's not clear if this means it's exposing additional information that the developer wouldn't have had access to before or if it's infomation that the developer would have had access to anyway?  In general there is a lack of information in the explainer about potential abuse cases.  It's concerning that this is exposing information about navigation across documents as this could be a potential privacy issue... so I think some additional discussion of this is warranted in the explainer.

4. do you have any information about multi-implementer support?

</blockquote>

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/921#issuecomment-1882642431)


#### [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman

#### Miniapp 

Yves: Miniapp will release miniapp addressing soon.  Use case is what we discussed - a way to link into content in a miniapp - related to discussion of secure origin... 

Dan: also related to...

Yves: Manifest scope extension... 

Dan: that's maybe and opportunity to showcase what miniapp commmunity is doing to someone else...

### Plenary Session - [2024-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240111T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Matthew, Peter, Sangwhan

Regrets: Max, Yves

#### Breakout Rollup

Dan: Breakout A: we got a reply on Document PiP after leaving feedback.. We'll need to wait for Lea to pick this back up. We also got response to fullscreen popups. We closed deliveryType resource timing. Left a comment on text-wrap pretty. Breakout C: closed extending storage access to non cookie storage. Talked about privacy implications of permissions policy reporting - trying to figure out how to close. Left feedback on navigation activation info and got a reply; positive response from Mozilla. Based on this I suggest we close satisfied - they've taken on board feedback that we need more info on privacy and security and abuse cases in their explainer. [writes comment](https://github.com/w3ctag/design-reviews/issues/921#issuecomment-1886436845)

Peter: sounds fine

Matthew: *nods*

Dan: also talked about MiniApp - new addressing spec coming out.

Dan: on permission policy report... implementer support.. it's about permission policy, the underlying spec is only implemented in chrome, and this is a spec on top pof permission policy, which we're largely happy with, but the underlying technology is chrome only. However Mozilla has positive views about it, just hasn't implemented. Sangwhan made the point that .. does that bubble up to the level of concerns? 

#### talking about permission policy reporting

Dan: Hadley things "with concerns" is appropriate.  However there is another implementer, mozilla, who has said they are interested in implementing but that they just haven't implemented yet.

Amy: I think it should be satisfied with concerns, it helps us to have an indicator to look back on to remember the conversation, and also agree with Hadley about emphasising multistakeholder

Sangwhan: should we have a separate state for that? we can't fix if other implementers don't have time to implement

Amy: nobody else is going to be able to spot systematic problems with implementation if that's something that's happening

Dan: we could do more to find out what Mozilla's situation is - we're making an assumption.. there's no multiple implementations of permission policy to begin with. We should go back to Mozilla and ask what their current status is and what they think of the reporting api. Dominic asked the TAG to do more to encourage multiple implementations - this could be an example of that 

Peter: MDN reports partial support for a small amount of that API

Amy: interested to know why

Peter: looks like they just don't support all of the positions.. seems like adding to it piecemeal. Don't know enough details to know if it's deliberate, coincidental, or misreported.

Sangwhan: if it was because they disagreed with the proposal it would have been recorded somewhere

Peter: and you'd expect they wouldn't support any of it

Dan: there's a draft comment that also mentions privacy/security consequences

Sangwhan: what would be the security consequence? I can see the privacy concern.

Dan: you're right

Peter: found mozilla has recorded a positive position

Sangwhan: we do want it to happen, it's a good thing for the platform, hasn't received enough traction, which is why we don't prescribe it in any of our principles - it's not ready yet.

Peter: agree

Sangwhan: us having concerns can be considered a visible stance change. 

Dan: this is why I'm on the fence. How can we achieve both aims by putting pressure on multiimplementer support but also not closing quite yet

Sangwhan: we could nudge mozilla to see if they're considering implementing permission policy in the foreseeable future

Dan: oh I left the comment already but not closing... editing and adding about Mozilla

[discussion about multi implementer and permissions policy]

Sangwhan: maybe "what TAG expects from baseline in 2024" as a wishful thinking document...

#### Progress on findings

Dan: should have dedicated time for findings at f2f

Sangwhan: will launch accessibility checklist before london. Also putting a doc together about browser positions - eg. no response is unclear if it's negative or positive, levelling the field. also official stance vs individual views from a company.

Dan: we should publish this on tag.w3.org

Sangwhan: also if we should have a standards positions repo as part of w3c

Dan: we do have a section on /workmode/ that says some similar things - we should not duplicate this - I can do that

#### F2F Agenda Discussion

Dan: we should figure out what we are and aren't going to talk about, eg. dedicated session. Findings, privacy sandbox, retro, design reviews, design principles.. then we can set the schedule on the monday

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
