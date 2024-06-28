# TAG Teleconference
#### 24-26 June 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-06-24](https://www.timeanddate.com/worldclock/converter.html?iso=20240624T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [Wide review request for Pointer Events Level 3](https://github.com/w3ctag/design-reviews/issues/941) - @LeaVerou, @matatk
* [document.caretPositionFromPoint API in shadow DOM scenario](https://github.com/w3ctag/design-reviews/issues/949) - @LeaVerou, @matatk

### Breakout B (California / Europe)  - [2024-06-24](https://www.timeanddate.com/worldclock/converter.html?iso=20240624T153000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @rhiaro
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou
* [Requesting review of HTML Ruby Markup Extensions](https://github.com/w3ctag/design-reviews/issues/959) - @hober, @LeaVerou

### Breakout C (California / Australia) - [2024-06-24](https://www.timeanddate.com/worldclock/converter.html?iso=20240624T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober

### Breakout E (Europe / China) - [2024-06-26](https://www.timeanddate.com/worldclock/converter.html?iso=20240626T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo
* [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion
* [Timing Info for ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/958) - @martinthomson, @torgo, @maxpassion
* [`noopener-allow-popups` value in COOP](https://github.com/w3ctag/design-reviews/issues/964)

### Plenary Session - [2024-06-27](https://www.timeanddate.com/worldclock/converter.html?iso=20240627T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Max, Matthew, Yves, Hadley, Lea

Regrets: Amy

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

Dan: bump to the f2f - as it's part of a wider discussion on Privacy Sandbox and we need to have a separate session on it and other privacy sandbox things...

Hadley: I'd like to be a part of that, if I can

Dan: We'll try to put it on the agenda for a morning slot then


### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

Matthew: [we discussed last week](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/06-17-minutes.md#view-transition-classes---matatk-plinss) - there have been no objections to closing it as satisfied.

Matthew: from an a11y perspective, aware of the work on this - all being done with accessibility in mind and not breaking it...

Dan: there is multi-implementer support - at least [from webkit](https://github.com/WebKit/standards-positions/issues/321).

*out of band, recording Martin's +1 to closing this as satisfied*

<blockquote>
Hi @vmpstr - thanks for sending this our way and thanks for bearing with us.  We're going to close this as `satisfied`. We're happy for this to proceed.
</blockquote>

*re-opening discussion with Lea present*

Lea: It seems like an incremental feature on top of an existing API...  

### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

Matthew: one of the two where we had 2 similar APIs to solve similar problems... We [did hear back from them](https://github.com/w3ctag/design-reviews/issues/939#issuecomment-2112744241)...  

Dan: what does cooperating mean?

Matthew: means "bad guys"...

Dan: right...

Matthew: There was a similar kind of attack for the compute pressure API - and they had a review from PiNG - they did some mitigations in the implementations... Anssi or Kenneth could point them to the details.  https://github.com/w3cping/privacy-request/issues/113 I'd like this team to look at that.  In particular https://github.com/w3c/compute-pressure/issues/197 

Matthew: I think they have made a good argument that this is a different problem space & therefore different API.  I think Lea, Tess & Peter have commented before... Let's chat more about it at the plenary... 

Matthew: it's in WICG currently..

Dan: they think it will go to the Audio WG... 

Matthew: they are clear on what the differences are - we need to establish TAG consensus that we agree...

*bump to plenary*

*Matthew posted a [comment about the potentially similar side channel mitigations in Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/939#issuecomment-2186080264) in the meantime*

### [Wide review request for Pointer Events Level 3](https://github.com/w3ctag/design-reviews/issues/941) - @LeaVerou, @matatk

Matthew: no blocking concerns from an a11y perspective - a few things that APA might suggest... we're working with those in the group. Nothing that I can see that would block this...  

Lea: I didn't see anything concerning...  This is widely implemented.

Dan: suggest we close and get it off of our plate.

Dan: **closes as satisfied**

### [document.caretPositionFromPoint API in shadow DOM scenario](https://github.com/w3ctag/design-reviews/issues/949) - @LeaVerou, @matatk

Lea: they've [changed it to a dictionary](https://github.com/w3ctag/design-reviews/issues/949#issuecomment-2179464895)... 

Dan: Multi-implementer...?  https://github.com/WebKit/standards-positions/issues/301 (webkit support) and https://github.com/mozilla/standards-positions/issues/1012 (firefox positive). So great to see that.

<blockquote>
  
Thank you for being responsive to our feedback.

Indeed, consistency is a good point, though depending on the use cases, it could end up being a good choice to change *both* of these methods. Therefore, it would still be good to list use cases (starting with *user needs*).

Nevertheless, we see a `shadowRoots` argument as a low-level primitive that could later be expanded so it's ok to start from it, especially if it has already shipped in other methods. I would reiterate that `elementFromPoint()` could also be expanded in the same way for consistency (and I suspect there are plenty of use cases for that too).

It's great to see support from additional implementers.

We’re going to go ahead and close this. Thank you for flying TAG!
  
</blockquote>

## Breakout B

Present: Peter, Yves, Dan, Hadley, Lea

Regrets: Amy


### [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @rhiaro

### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

Lea: has anyone been in contact with TC39? 

Yves: I don't see any particular signal...

Lea: I can ping some TC39 folks and ask...

Yves: would be good to know if there are outstanding issues from their sides...

Lea: no webkit standards position...  at least 3 tc39 folks have "thumbs-uped" my comment...

Yves: the comment on the webkit standards position - discussion between Anne and Dom ... discussed the idea of bringing this to a TC39 group.. a discussion in progress... https://github.com/WebKit/standards-positions/issues/292#issuecomment-2177303724

Peter: a whole section in their explainer about standards venue...


<blockquote>
  
Hi @domfarolino,
  
We looked at this today during a breakout. We do have consensus on most of the concerns I expressed above, especially around standards venue.
  
Furthermore, we had some questions about the API shape that we couldn’t figure out from the explainer, and we were hoping you might be able to clarify.

It _seems_ (though we are not 100% certain) that this is a separate primitive than `EventTarget` and simply integrates with it. If that is correct, the current explainer is a little unclear on what the boundaries of each are. Does it use the same `Event` objects? Does it register event listeners behind the scenes? How does bubbling work? Does it support bubbling to parent objects when not using the `EventTarget` integration?
  
- All examples are about listening to predefined events on existing objects. How do authors create objects that can emit events? Today they need to extend `EventTarget` which is suboptimal. Does `Observable` enable a new pattern for this?
- Do you folks have any plans to integrate with any of the other pub/sub mechanisms on the web platform or JS runtimes? E.g. all the `*Observer` objects, or Node’s Event emitter?
- While the code examples are certainly succinct, we had trouble figuring out how many of them worked and extrapolate how to write code about use cases not listed in the explainer. We were especially unclear on the arguments of `subscribe()` (what does `next` do? How does it differ from `callback`?)
  
We think a reworking of the explainer would really help answer these types of questions. Some (non-exhaustive) suggestions:
- Start from use cases and user needs.
- Include some simple code examples before the more pragmatic ones, so the reader can understand how the primitives involved work
- Include code showing how authors can use this to enable their own objects to emit events.
- A clear separation of what is `Observable` and what is `EventTarget`.
  
  
@littledan @ljharb @ctcpip @robpalme We saw you folks upvoted my last comment. Has there been any recent discussion in TC39 around this? Any plans to discuss it in the upcoming Plenary?

</blockquote>


### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou

### [Requesting review of HTML Ruby Markup Extensions](https://github.com/w3ctag/design-reviews/issues/959) - @hober, @LeaVerou


## Breakout C

Present: Peter, Tess, Martin

Regrets:


### [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo

We sadly didn't minute a really good conversation we had about this in some previous breakout (or at least we were unable to find minutes of it).

Draft comment

<blockquote>

Hi,

@plinss, @hober, and I took another look at this in a breakout today.

If there is a problem here, and this is almost certainly true, that problem has not been articulated clearly. Instead, this is adding another thing to the pile of problems in this area.
  
There are costs to making this sort of change.  While it isn't obviously a big deal to add another `<meta name>` type to the already large pile of `<meta name>` types, there are ongoing costs that this will incur.  Extra bytes to transfer, maintenance, and the possibility that integrating this into a more rigorous model of titling could become more cumbersome.
  
It is usually at this point that the TAG recommends that you develop some more complete model of what it is you are changing from and changing to.  There is a lot of structure that is common.

For instance, consider the contents of `<title>` on a typical GitHub issue:
  
. Title of Issue · #Number of Issue · org/repo

Or Google docs:
  
. Title of Document - Google Docs
  
Or Facebook:
  
. (Badge Number+) Title of Post - Author of Post | Facebook
  
Or Fastmail:
  
. Number of unread · Folder – Title of email | Fastmail
  
Or Slack:
  
. Name of Channel - Name of space - Number of new items - Slack
  
There are a number of vocabularies that already encode this sort of metadata (Dublin Core, OpenGraph, whatever Twitter Cards uses, Schema.org, etc...).  Reusing an existing vocabulary, even if it doesn't quite match your precise use case, is likely preferable to inventing a new thing.
  
We also don't see how this should be a different mechanism for an installed web app versus a regular web page. (The name you've chosen, `app-title`, seems to be specific to installed web apps.)
  
</blockquote>

### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
  
https://github.com/mozilla/standards-positions/issues/805#issuecomment-2164513098

  
Punt to plenary, need help with this one.

### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

### [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober


## Breakout E

Present: Matthew, Dan

Regrets: Amy, Max

### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

### [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo
  


### [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion
  
Matthew: They've taken up the suggestion of adding some non-normative text about the gpu issue we raised. However, However the methods for mitigation vary. In terms of this design review / issue, TAG needs to decide is that enough? .. or do we want to push on this more actively?  Don't know how far we want to push this.
  
Dan: another issue ... 
  
Matthew: [Tess and Martin](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/06-10-minutes.md#webnn) both had concerns...  
  
Dan: suggested that the API should be higher level abstraction...

Matthew: it tries to be fairly low level to avoid some problems...  
  
Dan: they have chosen a certain level of abstraction.  Tess and Martin were asking if indeed the API should be a higher level of abstraction - at the level of "face detection" for example instead of the middle level of abstraction they've chosen.
  
Matthew: if you want to use the CPU you can use WASM.. if you want to solve it in a GPU way you can use WebGPU.  WebNN is trying to cover all of those bases...
  
Dan: there is discussion of "NPU"s in the spec...
  
Matthew: but the industry does not know what a machine learning processor is yet.... when we know, when it's settled... then there might be an obvious abstraction that works across the different types of processor... 
  
Dan: **plenary?**
  
Matthew: let's take it to the plenary and then we can [formulate the feedback].
  
Matthew: in "getting started" section in the explainer ... 

Dan: Maybe a "satisfied with concerns" outcome... where the concerns are to do with lack of multi-implementer support (possibly due to non-support for certain types of neural accelerator chips?)

Matthew: interesting thing about jsml frameworks being a key customer... assumes that web developers won't use it directly... like webXR... this isn't "you can do face detection" it's "use this to build the thing that does the face detection"..  they're chaining the instructions...  Question is : what are the low level instructions for a neural processor?
  
<blockquote>

  Hi - thanks again for bringing this to us. We appreciate that you've been responsive to our feedback. We still have some concerns, but considering the current status of the work, we are planning to close the current review with a 'satisfied with concerns' label.
    
  Our main concern is: has this API considered the full range of hardware that it might need to run on?  We see this running on CPUs without neural processing extensions, GPUs without extensions, CPUs with extensions, GPUs with extensions, and dedicated ML hardware.  What steps have you taken to ensure that this runs across all of these targets, considering the range of hardware that exists and might exist?
  
  Our second and related concern is about multi-implementer support.  If this is going to be ubiquitous as an approach to "do NN on the web" then it really needs to be implemented across different platforms and different hardware.
  
  We encourage you to consider these issues as the spec and technology continues to evolve.

</blockquote>
  
  
### [Timing Info for ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/958) - @martinthomson, @torgo, @maxpassion

Matthew: the comment so far is good. but one thing might not be clear... 
  
Dan: w
  
  
### [`noopener-allow-popups` value in COOP](https://github.com/w3ctag/design-reviews/issues/964)

Matthew: Off-topic, but: the explainer for that talks about where you have multiple, separate applications in the same domain... that's the same topic we're working with in API - known destinations... 

## Plenary Session

Present: Matthew, Dan, Tess, Martin, Peter, Yves

Regrets: Hadley, Amy


### Breakout Rollup

#### Breakout A
  
*webaudio statistics API*

Dan: are we ok with [their explanation](https://github.com/w3ctag/design-reviews/issues/939#issuecomment-2112744241)  
  
Peter: seems one could be built on top of the other... different use cases but similar in data and functionality...
  
Matthew: when they say the whole audio pipeline are they talking about the whole system?... 
  
Peter: could also include devices youre streaming to...
  
Peter: my main concern was "are these people talking to each other?"
  
Matthew: we dis ask ... one is being incubated in audio wg, .. playout statistics is in WICG and is destined for webaudio... I'm not 100% clear if that means they're talking to each other... 
  
*yves to check with webaudio folks*

*later, from Yves: it was not controversial in the Audio WG, it is linked to several (closed) issues in the WG, and they are just incubing it in WICG, see
https://github.com/WebAudio/web-audio-api/issues/2563 , https://github.com/WebAudio/web-audio-api/issues/2444 and https://github.com/WebAudio/web-audio-api/issues/373*

#### Breakout B

#### Breakout C

#### Breakout E
  
WebNN discussion.... [see above]

### Issue Triage
