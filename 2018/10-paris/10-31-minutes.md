## TAG F2F Paris
##### 31 October 2018

Present: Lukasz Olejnik, Kenneth Rohde Christiansen, David Baron, Travis Leithead, Alex Russell, Sangwhan Moon, Daniel Appelquist, Yves Lafon, Peter Linss, Hadley Beeman

Regrets: **(this space intentionally left blank)**

---

Agenda:
* Design Reviews!!!

---

## Triaging 

https://github.com/w3ctag/design-reviews/issues/241

Lukasz: some comments on privacy & fingerprinting

Burning down this list: https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22extra+time%22+sort%3Acreated-asc

https://github.com/w3ctag/design-reviews/issues/277


Alex: did they respond to our feedback?

David: yes; issue raised and PR filed

Alex: is the exclusivitiy of ownerhsip a general thing?

Kenneth: probably.

Alex: should we write something up in our design guidleelines? I expect this to come up again with other sensors.

Kenneth: I will


Async Local Storage

https://github.com/w3ctag/design-reviews/issues/278

Peter: Creates an indexdb database ... I think that's OK. I wonder if we want to make a standardized way of reserving namespaces?

Alex: they're going to create one database ...

Alex: do we care?

Travis: I don't.

Alex: they filed an issue on us asking for review.

https://github.com/w3ctag/design-reviews/issues/287

Alex: big open issues in the core of this design....

Peter: we should take this to extra time.

https://github.com/w3ctag/design-reviews/issues/292

Alex: I'm working on feedback for this. Leave it with me.  (And Kenneth and Travis)


https://github.com/w3ctag/design-reviews/issues/293

Yves: this looks pretty specific to the Chrome implementatin, rather than an interoperable spec

Alex: there is a separate explainer... It says that it will only affect subresources.

...I want to say "this looks great" and move on. Not sure there is more to do.

Yves: This is about how the RFC is impelementable specifically in Chrome. That's how I read it.

Peter: is this a new parameter for the cache control parameter?

Yves: Yes. So it has implications for how you get things form the cache and how much time you want to ??? the content.

Peter: So, after this amount of time, try to see if it's still valid, but return the stale response anyway.

Dan: So can we close it?

Yves: Sure


Dan: Let's take a look at the HTML-labeled issues and see if any are awaiting respnoses on their comment threads. https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3AHTML

Dan: if we're not going to take some time on these, we should take of the extra time label. 

Peter: but it does show that we've seen them in triage...

Dan: that's true. 


Dan: Okay, so let's look at the issues that are not HTML-labeled https://github.com/w3ctag/design-reviews/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+-label%3AHTML+

...Let's triage these.

David: We did some amout ont of triage yesterday. Should we take everything that has the Paris milestone and set the label?

Dan: Yes please.


Dan: Let's see what else isn't tagged for Paris and should be. 


https://github.com/w3ctag/design-reviews/issues/134

Dan: Issue 134: Can we review this? 

Travis: I'm not sure there is much to do on this one.

Dan: Shall we close it? Extra time?

Travis: sure.


https://github.com/w3ctag/design-reviews/issues/141

Dan: (reviews what's in the issue)

...Let's keep it in extra time.


https://github.com/w3ctag/design-reviews/issues/214

Dan: Can we discuss whether to close this? Can we close this?

Travis: We moved this to the W3C Strategy Funnel.

Hadley: Ah yes

Travis: Let's close this.  I'll do that.

Alex: I'm concerned about streams here... I'll add to the strategy funnel issue



https://github.com/w3ctag/design-reviews/issues/218/

DSangwhan: Extra time


https://github.com/w3ctag/design-reviews/issues/235

Dan: This needs more discussion. All of us or in breakout? 

Hadley: "This allows AMP to fix its URL problem..." should we do this before the workshop?

Alex: waiting til the next face-to-face is quite late.

Dan: ok


https://github.com/w3ctag/design-reviews/issues/240

Peter: Let's look at this again at our next face-t-o-face


https://github.com/w3ctag/design-reviews/issues/276

Kenneth: at TPAC, Domenic had some question on this.

Alex: Let's ask if this is an urgent review


https://github.com/w3ctag/design-reviews/issues/278

Dan: this is fine; already marked for discussion here


https://github.com/w3ctag/design-reviews/issues/279

Hadley: They were aiming to ship in July or Aug... have they?

[everyone checks]

dan: if we can't find i

yves: implemented behind a flag in chrome 71. people expressed interest but it's still under discussion.


https://github.com/w3ctag/design-reviews/issues/280

Dan: already on our list this week. Putting to extra time.



https://github.com/w3ctag/design-reviews/issues/282

Dan: pending external feedback

https://github.com/w3ctag/design-reviews/issues/288

Sangwhan We should discuss this with 141


https://github.com/w3ctag/design-reviews/issues/295

Dan: we've got to talk bout this. So... extra time label


https://github.com/w3ctag/design-reviews/issues/297

Dan: we need to talk about this. 

Hadley: good


https://github.com/w3ctag/design-reviews/issues/298

Sangwhan: I think we said this looks good. 

Dan: can we close it?

Sangwhan: Travis, thoughts?

Travis: Yes, let's close it.


https://github.com/w3ctag/design-reviews/issues/302

Alex: Let's wait for them to update us on the status.


https://github.com/w3ctag/design-reviews/issues/303 , 304

Dan: Let's reassign them to another milestone... 

Travis: Martin said he wants 6 months.

Alex: What are they asking of us here?  They filed this in September. 

Sangwhan: I think we can hold this off until we understand how it all fits together. It's going to be a long discussion, especially since we aren't all in the details on QUIC

Alex: Can we process the input soon and get back to them? Today, ideally?

Sangwhan: It's a big topic for this face-to-face. Maybe a break-out today or a break-out call?

Dan: I'm trying to limit the stuff we hve on our list for today

Travis: I'd like to come up with some opinions with a half hour in breakout. 


https://github.com/w3ctag/design-reviews/issues/305

Alex: We talked aobut htis at TPAC. I have concerns.

Dan: so... extra time label then.


https://github.com/w3ctag/design-reviews/issues/302

David: I thought we might be close to closing it

Alex: can we do that now?

David: Quickly: Some of htis was weird becasue it was a review request for a modification t othe HTML spec, but the motification got reverted before I did the review. So what they asked us to review isn't there anymore.

...I filed some open issues in their repo

Alex: What should we do?

Kenneth: Can we close and ask for another request when they're ready?

David: I don't thik nayone is paricularly focused on this right now. leave it open and come back in a few moths?

Peter:... something something houdini

David: It's pending external feedback?

Alex: if there's nothing for us to do, let's close. And reference this issue in future discussions.


### Quick diversion to Security and Privacy Questionnaire

Lukasz: Incidentally, I do not believe that PiNG want a separate questionnaire for escurity and privacy. I will continue as usual with Jason.


### Back to triaging issues in the design review repo

https://github.com/w3ctag/design-reviews/issues/306

Kenneth: there was a breakout session at TPAC, with invisible searchable DOM 

(Alex: control-F on a website)

Dan: Still useful for us to feedback then?

Alex: They wrote a good explainer

Kenneth: and there is a WICG thread

Dan: so not putting this to extra time for now?

Alex: what was the outcome of the TPAC chat?

Kenneth: that there is overlap in the two solutions

Alex: So, given that, let's ask them if they still want us to review this.

Kenneth: agreed.



https://github.com/w3ctag/design-reviews/issues/307

Travis: this needs attention. I assigned myself to it yesterday.

Yves: I can look at it too.


https://github.com/w3ctag/design-reviews/issues/308

Peter: Kenneth and I gave feedback. Pending external feedback

Dan: Great; will move the milestone.



https://github.com/w3ctag/design-reviews/issues/309


Hadley: I guess we should talk about it. It was opened 21 days ago.

(Discussion of the use cases)


https://github.com/w3ctag/design-reviews/issues/311

Dan: putting this on extra time.


https://github.com/w3ctag/design-reviews/issues/313

Dan: Are we going to do this today? 

Hadley: We didn't really ask for feedback; we told them we are looking into this one

Dan: okay


https://github.com/w3ctag/design-reviews/issues/314

Dan: this is one of those TC39 issues we asked them to open.

...Putting this on extra time.

David: Should we have a label for TC39 issues?

Dan: Yes

Sangwhan: I'll do that.


https://github.com/w3ctag/design-reviews/issues/315

Alex: did we start this yesterday about Canvas?

Dan: there are two issues referenced in the whatwg repo

Yves: Did CSSWG reivew this?

David: add me


https://github.com/w3ctag/design-reviews/issues/316

Hadley: side note: we are getting further and further from plain English.

Dan: This is was raised 13 hours ago. 

David: The spec URL is actually a PR against their spec.

Sangwhan: I think we should defer on this. 

Kenneth notes deadline of end of this quarter.



https://github.com/w3ctag/design-reviews/issues/317

Dan: Who else wants to join this? 

Alex: I saw Web Perf WG while they were discussing this. To the extent that they are happy, I am very happy.

Dan: I'll take it to extra time. Anyone else to join?


[Full group effort on clustering people and issues... @triblondon, we miss you]


[coffee break]



## Future meetings



### February 2019

Tokyo

Host: Google

5-7 February. These dates are FINALISED. 


### May 2019

Rekjavik

Host: Vivaldi

Tentative - week of 13 May 2019

Suggested 14, 15 and 16

Or week of 20th -- Sangwhan will check with the host.

Update: they are fine with those dates.



### September 2019

Before TPAC

10 - 12 Sept - Tues, Weds and Thurs the week before. 

Dates might be problematic due to Autumn Festival


### TPAC - September 2019

(for the calendar; not a TAG meeting but we're expected to be there)

Fukuoka, Japan

16 - 20 September

### Jan/Feb 2019?



## Breakout group 1

People: Hadley, Dan, Kenneth, David

### Javascript decorators

https://github.com/w3ctag/design-reviews/issues/314

D(much discussion on the use cases/problems to solve and lack of explainer)

Kenneth: this has been through a lot of review already, especially by typescript developers

Dan: So we can write up additional feedback from perspective of web compentent developers, etc.

Kenneth: I'll write it.

David: I'll add something.

### Screen capture API

https://github.com/w3ctag/design-reviews/issues/309

Left feedback and set to pending.

### Base used to resolve relative URIs to absolute URIs in HTML5 data-blocks

https://github.com/w3ctag/design-reviews/issues/312

Hadley: worry that we say this has to be part of the DOM when in some cases it doesn't apply.

David: argument on the flip side - usually these 2 things are the samewu. Question is why do people put in base elements. I use it for testing. Is there a reason for this to be different from everything else.

Hadley: I asked them for use cases and user needs. They wrote that in their explainer.

Dan: This is pretty strong, do we agree? "Knowledge graphs of all descriptions would fail to coalesce if the resolution is not deterministic and left up to individual implementers to decide on the method."

Hadley: Yes. Linked data works because data is addressable with a globally unique URI. Going to relative URIs already pulls you farther away from that; to then have multiple possible absolute URIs from relative ones ... makes heads explode

### hrefTranslate attribute

https://github.com/w3ctag/design-reviews/issues/301

[reviewing explainer]

[discussion and wrote many things into our issue]

# User Activation v2

https://github.com/w3ctag/design-reviews/issues/295

David: i told them we are happy ppy for now and to report back with the results of the trial.

David: their goal is to redesign how this thing works.

Dan: so at some point they will have a new spec?

David: hope so.

Dan: Where?

David: not sure.

## Breakout Group 2

People: Peter, Travis, Yves, Lukasz, Sangwhan, Alex

### AOM

Alex: The AOM spec changed a lot since we last looked at it

Travis: We got an update yesterday, couple points being responded to - including an example. You can get computed accessible node I'd like to see it work more like the input type attribute.

Travis: Does anyone have strong opinions on how aria roles should be reflected into the dom?

Alex: Depends.

Travis: There is an extra step involved in the example described.

Alex: What is the extra step?

(Discusses example: https://github.com/w3ctag/design-reviews/issues/134#issuecomment-420102289)

Alex: I think what you were flagging was that this looked like sync work, is that the case?

Travis: I think my issue is that role should return something more meaningful than just empty string

Alex: So you want this to be a dasync property?

Travis: Somewhat.

### OffscreenCanvas and commit()

Tons of(tons of converastion and swapping the whole space back in, particularly re our previous feedback to the VR/XR groups about how rAF was inherited/fused and the various new XR Device API proposals)

(we found Greg Tavares' feedback partiuarly compelling and, in working through the scenarios in which something like XR devices drive a separate (faster) rAF, were happy to see these unlocked, preserving implicit commit for multiple rAF drivers but from a single execution context)

Alex/Travis draft feedbak:

> Hey all,
>
> Took this up again at today's F2F in Paris. 
>
> Thanks for patiently explaining a complex space to us.
> 
> While we recognize the scenarios for having an explicit blocking `commit()` (e.g., porting native code to the web with near-zero change), we don't think that the case is yet sufficiently compelling to offset the architectural concerns raised by blocking commit.
>
> Shared Array Buffers and atomics now allow developers to guard critical sections, and that *may* seem in conflict with a rAF-based solution, but the extent to which that is true isn't clear from discussion or the examples we've been able to read.
>
> One of the most complex scenarios we've been pondering has been the need to [run multiple displays at different rates](https://github.com/immersive-web/webxr/blob/master/explainer.md#mirroring), driven from the same GL context. This arises in VR and XR scenarios and we're very happy to see the progress made in providing [`requestAnimationFrame` fused to the `XRSession` object](https://immersive-web.github.io/webxr/#dom-xrsession-requestanimationframe), rather than an implicit higher frame rate (which is what commit appeared to enable in a world where the worker itself might only get a 60fps rAF).
>
> This progress in XR takes a lot of the pressure off of the necessity of `commit()` (in our view) and we'd like to see the community move forward with this model if possible. If not, we'd like to discuss further, perhaps on a future call, to help clarify the (perhaps glaring!) gaps in our understanding.
> 
> Cheers -- Alex & Travis

Media capabilities draft feedback:

> Hey all,
> 
> Thanks for filing this issue. We took it up during our Paris F2F. Apologies that it took so long.
> 
> I had a question about how this could be use to test capabilities in a multiple media stream context. For example, can we understand if it's possible to efficiently decode more than one video stream at once? Or get a maximum number of streams/channels/densities at which the client would hit limits? This case could come up in an RTC scenario. There may be cases where decode won't be smooth when you have two decoders or a encoder and decoder pair running, for example.
> 
> We also had questions about naming and types of the returned capabilities, specifically `smooth` and `powerEfficient`. These names imply a guarantee - despite what you've already written about how they are not. Have there been any alternative names considered? Curious if this can be addressed somehow? (We ballbrainstormed ''`janky` or `powerInefficient` as poor choices, but with the logic inverted.)
>
> Thanks again, and looking forward to hearing back.

SXG draft feedback:

> Hey Jeff,
>
> We reviewed the latest draft and explainer updates at today's F2F in Paris and are very happy with the progress and direction of the work. In particular, the proposed placement of Service Workers vs. SXG in the loading pipeline looks great and we're happy to see it. Looking forward to hearing how security review of this setup goes.
>
> We were hoping to find more details about the `validity-url`. What happens if oa cert matches but the validity URL does not load? Does that fetch never happen?
>
> Most of our open questions relate to Bundles, which we realize aren't in scope for this review. Specifically, we'd like to see:
> 
> * A discussion of how SXG and Bundles are handled when directly `fetch()`'d. We presume those will be different (an individual SXG yeilding the content, whereas a bundle might not unwrap the content)?
> * An API for opening Bundles and dealing with their content; e.g. how can I populate a SW cache out of a few resources from a Bundle fetched over `fetch()`? We have a general interest in seeing the platform's encoders and decoders exposed to userspace to enable better layering.
 > * PRegarding the last point, any plans to provide a CBOR encoding/decoding API as part of this work?
>
> Overall we're excited that this work is moving forward quickly. Hoping to hear what you're able to learn from the Origin-Trial.
>
> 

ISOBMFF

> As for delivering web content through a MPEG container, we have looked at the proposal and believe that a more adequate approach would be to use web packaging to contain the content, which leaves room for extensibility and doesn't require reinventing a new mechanism. On top of that, using signed exchanges this can prevent tampering with the content, which could be a extremely useful feature given that a DTV transport stream cannot be considered secure against MITM attacks. This is slightly harder when the package is not self-contained, and we believe that this would be more future proof than the proposed approach.

Spatnav

> Hey all,
>
> Thanks for filing a review. We noted excitement about this at TPAC and are glad to have the opportunity to work with you on this. Thanks also for the detailed explainer.
>
> We spoke with folks working on this recently in an ad-hoc discussion, wanted to get some of these thoughts written down.
>
> [Hostile iframes](https://github.com/WICG/spatial-navigation/issues/58) seem like a serious issue, but we're curious about how they're different to other sorts of focus capturing issues; e.g. the fullscreen API. Those APIs preserve a keyboard shortcut to allow escape. Is something like thpossible? The proposed feature policy seems like a promising direction.
>
> The traversal (distance computation) algorithm seems to have properties which result in unexpected (at least from a user's perspective). A potential improvement has been noted in your issue tracker - https://github.com/WICG/spatial-navigation/issues/122#issuecomment-433053747 although there are probably better ways to approach this.
>
> Are Focusable Areas seem to have a correspondence with Intersection Observers. Has a similar set of [rootMargin and threshold options](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API#Creating_an_intersection_observer) been considered?
> 
> An interesting point of feedback from other communities was around the right-left (start on one element, traversal, where focus does not return to the element the user came from, this seems like a limitation that should either be addressed or explicitly noted.
>
> Minor nit: The spec text for defining P1 and P2 could be clearer.

# Fin
