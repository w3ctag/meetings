# TAG Minutes document - Mon 26 August 2024

## Agendas

### Breakout B (California / Europe)  - [2024-08-26](https://www.timeanddate.com/worldclock/converter.html?iso=20240826T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou

### Breakout D (California / Australia) - [2024-08-27](https://www.timeanddate.com/worldclock/converter.html?iso=20240827T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Early design review: Storage Access Headers](https://github.com/w3ctag/design-reviews/issues/982) - @hober, @martinthomson, @jyasskin
* App Stores Finding Discussion
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Breakout E (Europe / China) - [2024-08-28](https://www.timeanddate.com/worldclock/converter.html?iso=20240828T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @martinthomson, @LeaVerou
* [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [WebXR Device API (delta/aiming 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/983) - @torgo
* 3p Cookies Finding Issues & PRs

### Plenary Session - [2024-08-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240829T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

2024-08-26-week
* Breakout Rollup

## Minutes

### Breakout B (California / Europe)  - [2024-08-26](https://www.timeanddate.com/worldclock/converter.html?iso=20240826T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, jeffrey, Tess, Yves,
Regrets: Hadley, Peter

#### Review last week

Yves: we closed an issue related to web assembly...  Otherwise we discussed private attribution API...

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou

Jeffrey: my impression is that this gets discussed across engines in the WASM CG and WG... they do a good job in catching stuff. I suspect that in general we should be declining... Like "we trust the web assembly group"... at some point maybe they will step into an arch issue... but this doesn't strike me as worrying...

*Jeffrey to review and propose to close as `decline` if appropriate*

> Thank you @fgmccabe for bringing this to us, and we apologize for taking so long to respond to it. We appreciate the work to integrate Promises into Web Assembly. We think the Web Assembly CG is/has been the right place to review it, so we're going to decline the review here.

#### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

Dan: I think we need Lea here...

#### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

Jeffrey: a proposed comment in last week's minutes....

Dan: yes that's why I added it to the agenda today....

Tess: we wanted to check with Jeffrey...

Jeffrey: I checked this comment and I think it has consensus with the TAG and also checked it with the private agg people...

Comment from Slack:

> We appreciate you bringing this to us. We see that Chromium has already shipped this API, so this comment primarily applies to your efforts to bring it to other browsers. We [understand this to be a generalization](https://github.com/patcg/private-measurement/issues/22#issuecomment-1734280125) of the three advertising attribution proposals that the PAT[CW]G is working to unify, and we think it'll be most productive to finish that work before refining this generalization.
>
> We recognize that it's usually beneficial to generalize features, but when those features come with privacy risks, we think it's important to balance those risks against the value of the additional use cases. This explainer only identifies two additional use cases. One of these is Protected Audience, about which the TAG has already expressed concerns (#723). We did not find the building of market demographics across sites to be sufficiently compelling to justify this whole generalization.
>
> Given that the short term focus should be on finishing the advertising API, we're going to decline this review. However, if more use cases turn up for the generalization, we'd be open to looking at it again."

*we agree Tess to paste comment and close the issue as `decline`*

Tess: **closed**

#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

Jeffrey: chrome shipped it... CSS discussed... chrome fixed certain things... still [one disagreement](https://github.com/w3c/csswg-drafts/issues/10321#issuecomment-2272165809)... otherwise it feels fully discussed in CSS... Think there aren't architectural things for the TAG to address.

Tess: is [the thing where](https://github.com/w3c/csswg-drafts/issues/8398) we cause a pile of compat problems every time we try to make a heretofore-not-a-shorthand thing a shorthand...?

Jeffrey: Yes. I would like to close it as `satisfied`.

Tess: this feels like a classic theoretical purity vs. compat risk ...  I'm fine with closing it as satisfied.

Dan: *sets to proposed closed*

<blockquote>
Hi @xiaochengh and @tabatkins, thank you for bringing this to us and for thoroughly discussing it in the CSSWG. We're happy to see this feature being added to the web platform, we don't see any architectural concerns, and we're happy to see the CSSWG continue to work out any remaining details.
</blockquote>

Dan: great! let's revisit at the plenary call.

#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

This is pending external feedback since Tess' [comment on 17 June](https://github.com/w3ctag/design-reviews/issues/864#issuecomment-2173934184).

*some discussion on this point*

Jeffrey: I can poke the implementers to raise this with the working group... it might be a good idea to raise the issue directly with CSS... 

Tess: I can look ...

Dan: can we close?

Jeffrey: I think satisfied with concerns would make sense... ?

Dan: if it's an issue that is actively being worked on then it would be `satified`.

Jeffrey: can we say 'hyphenation with oprphans is sufficient'?

Tess: I think `satisfied with concerns` is overstating it...

Jeffrey: it's an easy enough thing to change... blink could ship an alias... if the wg has already discussed "pretty" and said it's the right name then we should accept that... 

*bumped to next week*

#### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

Tess: I will look at the revised explainer 

Dan: and we can wait until Matthew is back...

#### [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

Dan: *outlines history*

Jeffrey: seems like cross-origin case exists in order to compete with native apps so - do we think of new APIs as changing the web or changing the whole ecosystem... centralization/ decentralization...

Tess: I usually talk about ... camp that thinks that the web and native are in competition... and that's the battle ... there's another camp that sees them as complementary... The first camp can often come across as antagonistic towards native & think we need feature parity..

Tess: on same origin... are we agreed that any web site can call it? Originally there were a bunch of requirements - e.g. manifest, manifest can have a bunch of things in it... to me, as long as it's gated on a user gesture, it feels like any web site can call it.

We take a look at the explainer - it says 

> In order for an application/site to be installed, it must comply with installability criteria. This criteria is entirely up to the UA, can vary depending on the installation target, and can be optional.

Tess: I get that... 

<blockquote>
Hi Diego - thanks for sending this our way.  We're happy to see this move forward and would like to review again when you have a specification in the Web Apps working group. 
  
We're happy to see that the installability criteria is indicated as up to the UA.
  
We're going to close this for now with a `satisfied` label. Please ping us to re-open when you want a follow-up review.  
</blockquote>

Dan: we can review at the plenary.

#### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
#### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou

### Breakout D (California / Australia) - [2024-08-27](https://www.timeanddate.com/worldclock/converter.html?iso=20240827T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Tess, Jeffrey; Regrets: Martin

#### [Early design review: Storage Access Headers](https://github.com/w3ctag/design-reviews/issues/982) - @hober, @martinthomson, @jyasskin

Jeffrey's proposed comment:
> This strikes us as a good direction for the evolution of the storage access API, and we'd like to see the Privacy CG continue to iterate on the details. We don't expect to have much to contribute to a review of the final specification and are happy for that to proceed through the Privacy CG and WHATWG processes without our further review. We also encourage further work on allowing authenticated embeds to work with Javascript completely disabled, acknowledging that this is difficult given the goal that storage access should only be granted after user interaction with the cross-site content.

Tess: I was worried about this because "when does the user gesture requirement apply"? And Storage Access lets different browsers experiement. Does this cut off some branches of experimentation?

Jeffrey: Add to the comment something about "don't close off experimentation."

Tess: Also make sure they go through the PING?

Jeffrey: I feel like this particular extension won't raise privacy risks, even if Storage Access as a whole should go through PING.

> This strikes us as a good overall direction for the evolution of the storage access API.
>
> One concern: the Storage Access API is architected such that implementations may differentiate themselves by imposing stricter or more lax policies on sites. Does this feature narrow the window of possible policies? Put another way, could websites misuse this feature such that some policies would fail to work? If this header becomes widely adopted, could browsers find themselves needing to change their policy for compat reasons?
>
> Another minor concern: We find the use of the `Sec-` prefix to be unnecessary.  Sites presently receive requests with and without cookies.  That a new signal might elicit new and inappropriate reactions from a server is possible, but not a particularly credible one.  Denying web applications the option to elicit one more inappropriate action using this mechanism is wasteful.
>
> We'd like to see the Privacy CG investigate this and continue to iterate on the details.
>
> We don't expect to have much to contribute to a review of the final specification and are happy for that to proceed through the Privacy CG and WHATWG processes without our further review. We also encourage further work on allowing authenticated embeds to work with JavaScript completely disabled, acknowledging that this is difficult given the goal that storage access should only be granted after user interaction with the cross-site content.

#### [Controller Document](https://github.com/w3ctag/design-reviews/issues/960)

Brief conversation about this, but nothing concrete.  (continued on slack)

#### App Stores Finding Discussion
#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

Present: Dan, Tristan, Matthew, Martin
Regrets: Max, Amy

### Breakout E (Europe / China) - [2024-08-28](https://www.timeanddate.com/worldclock/converter.html?iso=20240828T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Martin, Tristan
Regrets: Max

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

*bumped*

#### [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @martinthomson, @LeaVerou
#### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk

This sits on a list of features that Google has deployed without standardization (this is still in Origin Trial, I believe).

Problems here are the same as those inherent to screen sharing.  Some fingerprinting risk, but the primary risk is that this enables capture of content that a site might not otherwise be authorized to obtain.

Dan: what's the permissions story? do they document abuse cases / mitigations?

Martin: The explainer ... they are relying on screen capture permissions model etc... they are just looking to double down on that.

Dan: so we are not asking the user to share...

Martin: there was a debate on what influence the application should have over the shape and scope of the permissions window... targeting screen sharing. One potential outcome is that the web site can share itself... there is a spec for that.

Martin: 625 was an APi for capturing the current tab... the key problem with screen capture - allows the web site to see what is on the page. It can frame in content from another site and screen capture the current page including that content... this is why we have permission prompts that put user interests ahead ... element capture gives the ability of not just capturing whats on screen but what is off-screen, including cross-origin...

Dan: in what cases cross-origin?

Martin: if the element you identity is or contains an iframe for example...

Dan: what if the spec said "no cross-origin"? would that mitigate?

Martin: that was one of the mitigations discussed... we also have viewport media function...

Martin: getviewportmedia has a site isolation requirement... which uses the same COEP for shared array buffer access... so from that perspective it's probably OK. Element capture in that case would be fine...  GetDisplayMedia gets you some piece of screen realestate - GetViewpoertMedia gets the current tab...

Dan: is that feedback we could provide?

Martin: it looks like they required the target to opt in... that changes things a little bit.  The cross-tab... you select a different tab and within that tab you want to focus on a specific chunk of that tab. and it looks like the target tab chooses what is captured...

Dan: I have a presentation running in one tab and I want to share it - but only the presentation, not the controls, to another tab that is webrtc session... 

Martin: that looks like a good use case...  this does look like it's cooperative...

Dan: Seems brittle.  Needs coordination.  Is it specific to the capturing or captured application or specific origins.  Seems to lack detail.

Martin: Might ask for more detail.

Dan: Sympathetic to the use case.  Either present the whole tab or the whole screen, but then you can't see people.  Moving away from the tab can destroy the stream.  Need to understand how this changes the permission flow.  If you are locked in to a specific target... Are you allowed to override what a site says you can share?  Could people be railroaded into a specific selection?

https://w3c.github.io/mediacapture-viewport/

Martin: let's say that you've identified that element and you can render that element to a stream - and not the elements "on top" of it - what happens with transparency?

<blockquote>
Hi - some pieces of feedback from our TAG breakout this morning where we reviewed this:
  
It seems like the explainer is very lean.  We think that there are a number of issues that need to be more fully explored before we can be more sure about this proposal.
  
In the use case that you're sharing a specific content area to an embedded iFrame (the use case in the explainer) what is the permissions flow for this scenario?  For example - in  current screen sharing scenarios, the user may be prompted to share a tab, a window, or the whole screen. What would the user be prompted for in this case? Would they be able to choose an alternative sharing target such as an other tab or the screen or is it envisioned that in this case they would be constrained to only share content from the designated application?
  
Can this be treated like an extension to [ViewPortCapture](https://w3c.github.io/mediacapture-viewport/)?  We note that this sort of sharing carries similar security risks at that API, and the additional constraints on capture in that API might be better suited to this use case than the more general getDisplayMedia.

The proposed API starts by preparing to share the whole of the content, and then restricting it to a particlar part - have you considered ways to _start_ with the specific part to be shared instead? (How would this affect occlusion?
  
You have a goal of avoiding occlusion, but what about elements that are partially-transparent?  Would this capture what is rendered behind an element?

</blockquote>


#### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

Martin: there will be a breakout session in TPAC about this...  defer until after that.

#### [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk

*bumped*

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

*bumped*

#### [WebXR Device API (delta/aiming 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/983) - @torgo 

Martin: it's pretty big...  It's hard to put your web frame of reference into the XR space... No safe space, no chrome...

#### 3p Cookies Finding Issues & PRs

### Plenary Session - [2024-08-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240829T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Max, Matthew, Martin, Tristan, Jeffrey
Regrets: Peter

TPAC Agenda time

Don't want to spend all of our time in meetings on single issues or cloistered.  Keep a time box on requests like that from Michael.

*We discuss setting up a meeting with Michael Kleber at TPAC to discuss 3p cookies & trajectory of privacy sandbox.* Tentative 11am Monday.

2024-08-26-week
#### Breakout Rollup

Dan closes [CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) as *satisfied*

Dan closes [same origin install](https://github.com/w3ctag/design-reviews/issues/888) as *satisfied*.

We close [promise integration](https://github.com/w3ctag/design-reviews/issues/809) as *declined*.

[TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Martin: I think this needs more [thought]...

Dan: *leaves response letting LuHuang know we are on it*

[Early design review: Storage Access Headers](https://github.com/w3ctag/design-reviews/issues/982) - @hober, @martinthomson, @jyasskin

*We review the proposed comment and agree to close it as **satisfied**.*

#### Triage

##### https://github.com/w3ctag/design-reviews/issues/959

I suspect we have nothing useful to say about https://github.com/w3ctag/design-reviews/issues/959, the Ruby extensions. I'm uncomfortable with this group of elements that is only useful for east-Asian text and isn't designed to represent any other kind of explanation of how to read confusing text (e.g. https://github.com/w3c/tpac2023-breakouts/issues/71), but I think saying that as the TAG is just going to frustrate people. So I suggest we decline the review.

*we agree to fast track close it as `decline`.*

##### https://github.com/w3ctag/design-reviews/issues/962

Martin: a bit of dispute... an issue raised... https://github.com/w3c/mediacapture-handle/issues/11

... 2 concerns - one is that this invents a new cross-origin communication mechanism. Maybe we should be using post message. Other concern: when you capture something and screen share it, the messages that come through from the other end.. e.g. requesting that page scroll or zoom - the design seems to make this indistinguishable from a regular input. Makes a machine available for remote control. This is at tension with user agency. It should be possible without the knowledge of the application, but heightened security... 

Dan: abuse cases... we need to take seriously.

Martin: ... I'll take it, but we also should say "please talk to the wg"...

##### https://github.com/w3ctag/design-reviews/issues/966

Martin we were gonna assign it ... this is a piece of a larger thing. Piece looks fine on its own... but would benefit look at broader effort. 

##### https://github.com/w3ctag/design-reviews/issues/971

Martin: I don't like this API....  

*we put on for next week*

##### https://github.com/w3ctag/design-reviews/issues/973

Matthew: APA already gave feedback... they are working on .. overall it's a really good update... 

*matthew to leave comment*


