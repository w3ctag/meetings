# TAG Minutes Doc - week-of 1 April 2024

## Agendas

### Breakout A (Europe / China) - [2024-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Harmonize with WebAppSec Powerful Features Draft](https://github.com/w3ctag/design-principles/issues/481)
* [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion
* [Add principle on use of delta seconds](https://github.com/w3ctag/design-principles/pull/467)

### Breakout B (California / Europe)  - [2024-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: Events should only fire during actual state transitions](https://github.com/w3ctag/design-principles/issues/483)
* [New principle: HTML attributes can affect semantics](https://github.com/w3ctag/design-principles/issues/478)
* [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)
* [First pass at #453 (text-based syntaxes should be designed for humans)](https://github.com/w3ctag/design-principles/pull/472)
* [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453) - @LeaVerou, @torgo, @hadleybeeman
* [New principle: Document whether to add things to Document, Navigator, Window, or SomeOtherInterface](https://github.com/w3ctag/design-principles/issues/448)
* [New principle: Consider many & diverse use cases to avoid overfitting](https://github.com/w3ctag/design-principles/issues/450)
* [New principle: The value of HTML boolean attributes doesn't matter](https://github.com/w3ctag/design-principles/issues/451)

### Breakout C (California / Australia) - [2024-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou
* [New principle: Incremental user effort should result in incremental value (or more)](https://github.com/w3ctag/design-principles/issues/473)
* [[WIP] add forwards compatibility / graceful degradation principle.](https://github.com/w3ctag/design-principles/pull/468) - @hober
* [New principle: APIs which vend byte buffers should return a Uint8Array](https://github.com/w3ctag/design-principles/issues/463)
* [More detail on why events should fire before promises](https://github.com/w3ctag/design-principles/pull/460)
* [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457) - @hober
* [Terminology jumps away from principle's subject ("Use care when exposing identifying information about devices")](https://github.com/w3ctag/design-principles/issues/479)

### Breakout D (California / Australia) - [2024-04-02](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### Special session with W3C Team on Appointments

### Breakout E (Europe / China) - [2024-04-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456) - @cynthia, @torgo
* [New principle: When introducing heuristics, also include a way to override the heuristic](https://github.com/w3ctag/design-principles/issues/455)
* [New: Avoid revealing that consent was denied](https://github.com/w3ctag/design-principles/issues/475)
* Design Review: [gamepad trigger](https://github.com/w3ctag/design-reviews/issues/934) - @torgo, @matatk
* Design Review: [WebNN](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion
* Design Review: [WebApp Scope Extensions](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454) - @ylafon


### Plenary Session - [2024-04-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240403T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)


* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* W3C @ AC Meeting


## Minutes

### Breakout A (Europe / China) - [2024-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [Harmonize with WebAppSec Powerful Features Draft](https://github.com/w3ctag/design-principles/issues/481)

Dan: *talking with Marcos about this*

Matthew: a couple of things - example that's given is the geolocation API which we don't think meets our principles of privacy preservation... as part of this, we could sort that out. Other thing is: the definition [of powerful features] is very accurate .. because people don't want to bother the user if they don't have to, there's discussion of what shouldn't go behind a permission... but there is no definition of what *would* cause you to gate sometning behind a permission. It would be interesting to come up with "when might you gate something behind a permission" - and sometimes the browser decides for you...

Max: In their document they have a definition ... probably we need to make sure that we have the same definition if we use that term.

Dan: Agree.

#### [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion

Max: I made some comments... have reviewed the discussions.. the suggestion - I agree with what Yves suggested... we can't give a very complete list. For example -  update the referrer policy... third one is to remove "document policy" - so we can't include in our current version.

https://github.com/w3ctag/design-principles/pull/363#issuecomment-2029225167

Dan: that sounds fine to me.





### Breakout B (California / Europe)  - [2024-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Lea

Regrets: Matthew, Yves

#### [New principle: Events should only fire during actual state transitions](https://github.com/w3ctag/design-principles/issues/483)

#### [New principle: HTML attributes can affect semantics](https://github.com/w3ctag/design-principles/issues/478)

#### [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)

#### [First pass at #453 (text-based syntaxes should be designed for humans)](https://github.com/w3ctag/design-principles/pull/472)

#### [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453) - @LeaVerou, @torgo, @hadleybeeman

#### [New principle: Document whether to add things to Document, Navigator, Window, or SomeOtherInterface](https://github.com/w3ctag/design-principles/issues/448)

#### [New principle: Consider many & diverse use cases to avoid overfitting](https://github.com/w3ctag/design-principles/issues/450)

#### [New principle: The value of HTML boolean attributes doesn't matter](https://github.com/w3ctag/design-principles/issues/451)

Peter: ...allowing an attribute to say it's false would not be backward compatible... 


### Breakout C (California / Australia) - [2024-04-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Tess, Peter, Martin, Lea

Regrets:

#### [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou

#### [New principle: Incremental user effort should result in incremental value (or more)](https://github.com/w3ctag/design-principles/issues/473)

#### [[WIP] add forwards compatibility / graceful degradation principle.](https://github.com/w3ctag/design-principles/pull/468) - @hober

#### [New principle: APIs which vend byte buffers should return a Uint8Array](https://github.com/w3ctag/design-principles/issues/463)

#### [More detail on why events should fire before promises](https://github.com/w3ctag/design-principles/pull/460)

Cleanups and merged PR

#### [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457) - @hober

Martin: *cleanup... PR* #485

#### [Terminology jumps away from principle's subject ("Use care when exposing identifying information about devices")](https://github.com/w3ctag/design-principles/issues/479)



### Breakout D (California / Australia) - [2024-04-02](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Ralph, Phillipe, Matthew, Martin, Yves, Coralie, Tess

Regrets: 

#### Special session with W3C Team on Appointments



### Breakout E (Europe / China) - [2024-04-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240401T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Max, Yves, Matthew, Dan

Regrets: 

#### ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456) - @cynthia, @torgo

#### [New principle: When introducing heuristics, also include a way to override the heuristic](https://github.com/w3ctag/design-principles/issues/455)


#### [New: Avoid revealing that consent was denied](https://github.com/w3ctag/design-principles/issues/475)

*we look at [Jake's proposal](https://github.com/w3ctag/design-principles/issues/456#issuecomment-1840349922) and see if we can drop it in as a replacement...*

Matthew: this is for an API designer...  I think his comment is useful background but we can't just drop it in as it's coming from a slightly different angle.

*We looked at this again today and we're going to work on making a PR in the coming weeks that adapt's the text Jake provided above.*

#### Design Review: [gamepad trigger](https://github.com/w3ctag/design-reviews/issues/934) - @torgo, @matatk

Dan: we talked about closing this last time...

Matthew: yes I agree - and they answered the questions about why this is necessary, and what comes next.

**agreed to close as satisfied**

#### Design Review: [WebNN](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matack, @maxpassion

Max: I think they accepted previous round of review... I don't see any issue. 

Dan: **Lea** also responded that it looked good to her from an API design pov.

Yves: I also looked at it and the changes looked good to me.

Matthew: I had a question... They've done some stuff that's in line with what we asked... There's another thing it looks like they added.  They added "matcher types" for certain problems... E.g. face detection or other common tasks. And i'm not sure whether we've done a review of that.  One other thing: there is no security & privacy section in the explainer... but they did fill in the questionnaire... Answers are "no" which is true ... but I wonder if it's worth linking to the ethical web machine learning principles from this document...

*we look at the spec*

Matthew: oh there's "[ethical considerations](https://www.w3.org/TR/webnn/#ethics)" - the link is there. 

Matthew: still wondering about the custom transformers... [webnn issue 375](https://github.com/webmachinelearning/webnn/issues/375).  

Matthew: it would be great if they gave a summary of what changed since last time...?  One other thing from an architectural pov.. I believe they resolved to drop support for webgl and concentrate on interop with webgpu... just noting that.

Yves: the diff: https://services.w3.org/htmldiff?doc1=https%3A%2F%2Fwww.w3.org%2FTR%2F2023%2FCR-webnn-20230330%2F&doc2=https%3A%2F%2Fwebmachinelearning.github.io%2Fwebnn%2F - the only mention of transformers in current spec is "adding new operations and data types needed for transformers..."

<blockquote>
Thanks @anssiko, @dontcallmedom for the review request. We were wondering, could you clarify the changes around transformers? We note you've added new data types and operations in support of them (is there a list?) - did you also add/remove any transformers?
</blockquote>

#### Design Review: [WebApp Scope Extensions](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: *we analyze [LuHuang's comment](https://github.com/w3ctag/design-reviews/issues/875#issuecomment-2024257259)*

Matthew: a couple of things from that and also [from Daniel Murphy](https://github.com/w3ctag/design-reviews/issues/875#issuecomment-2032471170) - "there is a 2 way handshake that is there to ensure that both origins are cooperating." ... also "This does NOT show content from one origin on another origin"  They give a concrete example with zoom... 

*we read through Daniel's zoom example*

Yves: does "in scope" mean sharing things like array buffers or even cookies?

Yves: the proposal is not only about subdomains - but about any other domain...

<blockquote>
Hi folks - I think we can best progress this review with a call where we can talk through the proposed use cases a bit more interactively.  Given that we have the W3C Advisory Committee meeting coming up, I'd like to suggest that we hold this call in our of our TAG breakouts the week of the 22nd of April.  I'll follow up by email to arrange.
</blockquote>

#### [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454) - @ylafon


#### Generative AI

Max: I spent some time to think about this generative AI doc... The Tean's document did some research within W3C and outside W3C... We could do analysis - what existing w3c standards can be used to address generative AI and then identify gaps... 

Dan: I've been looking at C2PA...   Maybe a workshop would be a useful outcome?

Yves: we should talk to Dom

Matthew: we should check in with web machine learning and specifically ethical principles...

Max: actually working on some documents would be useful... 


### Plenary Session - [2024-04-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240403T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tess, Martin, Peter, Yves, Matthew, Lea

Regrets: 


#### [Add principle on use of delta seconds](https://github.com/w3ctag/design-principles/pull/467)

Martin: question here is - should the design principles cover the notion of how to use http... and whether or not we can just say "use this document over here"... 

Dan: point people to http design principles...  ? https://httpwg.org/specs/rfc9205.html

Martin: i did have some text ... i could put it in a PR

Yves: I think most people will interact with http with fetch or similar...

Martin: with custom headers you're not insulated from fetch...

Martin: general advice on using time - i have text for that - and then 2nd thing - I want to re-do a http design principle and point to 9205.

Dan: that makes sense... need to be more concrete?

Martin: need more concrete problem to apply it to...  Delta seconds are used in cache control...  Establishes a common reference point for the time... 

#### Breakout Rollup

#### looking at https://github.com/w3ctag/design-principles/pull/480

Martin: going into API surface concerns...

Dan: are we OK with this?

Martin: there was an issue that was open... some conversation in WhatWG.. and I've had this problem come up a number of times... In WebRTC -- returned a bag of bits and it wasn't clear what the advice was...


#### looking at https://github.com/w3ctag/design-principles/issues/456

Matt: I think what Jake wrote is good to help us understand the background but we have to distill it into something that makes sense... 

Matt: I can take a look at it after the AC meeting.

**agreed to merge**

#### Some discussion on the appointments

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

#### W3C @ AC Meeting
