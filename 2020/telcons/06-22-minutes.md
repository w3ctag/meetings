## TAG Teleconference
##### 22-26 June 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20200622T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov
* [WebAssembly SIMD review](https://github.com/w3ctag/design-reviews/issues/487) - @hober, @kenchris
* [PWA Change logs](https://github.com/w3ctag/design-reviews/issues/484) - @torgo, @kenchris
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

#### Breakout B (US / APAC) - [2020-06-22](https://www.timeanddate.com/worldclock/converter.html?iso=20200622T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo
* [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo
* [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov
* [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss
* [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris

#### Breakout C (APAC / Europe) - [2020-06-23](https://www.timeanddate.com/worldclock/converter.html?iso=20200623T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman
* [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon
* [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris
* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo
* [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524) - @cynthia, @torgo

#### Plenary Session - [2020-06-24](https://www.timeanddate.com/worldclock/converter.html?iso=20200624T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @cynthia, @alice, @torgo
* Breakout Rollup
* Issue Triage


-----


### Breakout A

Present: Kenneth, Peter, David, Rossen, Dan

Regrets: Tess, Yves

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Peter: marked proposed closing..

Dan: (reading issue replies) ... 

David: what people use writable ones for in the wild... what is the existing set of writable vs 

Ken: you can make them read-only and that's what would use in a commercial deployment

... when you buy NFC tags they are read/write... but they can be made read-only (and then no way to go back)

Dan: Reasonably happy with the answers. Should be more discussion in the privacy section.

David: the other concern we have is whether the permission prompts are adequate. The concern is that there are a set of things out there that support reading and writing NDEF - some of those are things like Yubikeys (which you can read the current one-time-code from).  Yubikeys themselves are blocked but what about other Yubikey-like things. Not clear that this explains those risks to the user in a way that is adequate. We've disagreed on this but we should mention that again if we're going to close it.

Dan: we should be erring on the side of more rigorous prompts.

Ken: you can prompt each time... i discussed that with the chrome team they said they didn't want to do that. Whenever it's reading you see a prompt...  So we have a semi-permanent prompt.

David: the other question is whether more prompts would help.  The underlying concern is you don't know what the devices are that support NFC so you can't explain the risk to an end user in a prompt.

Ken: like that for many things

David: the assumption on native is you're trusting the app but on the web you can go visit a web site and there is not the same assumption of trust.

Ken: examples of linux system ...

Ken: i was suggesting an active "scanning" visual indication that something is going on and is temporary.  Very user-visible.  And at any time you can hit cancel.  I like that approach.  I see a use case where this won't be useful - scanning multiple - and that might require a different prompt. Having said that NDEF is inherently supposed to be like post-it notes... so this issue will always be there...

Rossen: seems like if we need to be prescriptive about UI ...

(discussion of Dan's proposed comment)

David: distinction from camera API is that yes, there are security risks to a photo with your environment, but it's also not a distinction about technical expertise where users who aren't technical enough to know what NFC is don't understand what data are sent.

Rossen: I keep running thru this example in my head of what prompting could look like - some parallels with geoloc - where you are still providing personal info ... The common UI is "the web site wants to use this service .  Allow/disallow" one time decision... If I draw a parallel with this one the problem is that geoloc data is very uniform. And the contract between you and that website is a ... obviously the data is changing but the same kind of data. Here, the data could be anything.

Ken: but you have to physically take the phone and scan something.

Rossen: i could boobytrap my store with all kinds of tags.

Ken: but you need to be within 5cm.. the phone needs to be unlocked. the screen needs to be on. Sometimes with geoloc you have the option of "always allow for this website" - so now if similar pattern was adopted for WebNFC that to me sounds concerning. Is this a good parallel to draw?

Ken: to come back to my idea of indicator - the example of how that is done is to say "now I am scanning" and you can't do anything on your phone until that is scanned. So that mitigates this idea - it can't be scanning in the background.  In some cases (e.g. a game with lots of tags) it can't work... but there can be another option for that.

Dan: I propose I leave this comment and we talk about closing at the plenary.  We can leave further comments, and we might have to mark as closed with no consensus.

#### [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov

Peter: missing Tess and Hadley...

Rossen: summarizing... the issue was looked at by myself and Tess... during one of our breakouts. A the time when we looked at it we did an analysis.  It looks like the proposal is good and going the right direction. We had some followup questions - one was what is the actual API going to look like. One idea was to explore an API ideally on the window object document.domain. Turns out that was one of things they wanted to remove instead of adding the API there. I still need to add a comment and close that conversation. During the virtual f2f, David gave it a quick read and found some concept inconsistencies... Anne and Domenic proposed some changes to the explainer and some examples. I think what they are proposing sounds good.   I don't think there's a lot left to get us to close on this.  We could move this to "proposed closing"? Hopefully Tess will have a chance to give her view.

David: I read the replies - it makes sense. 

Dan: I can ping Hadley about it.

#### [WebAssembly SIMD review](https://github.com/w3ctag/design-reviews/issues/487) - @hober, @kenchris

Peter: updated explainer...  Missing Tess. Should we defer this to another breakout?

Ken: I'm fine with it. It's web assembly only. Designed in a way that works across architectures... So I think it's pretty well designed.  Heavily used in codecs, gamed, machine learning. It would be sad not having access to this on the web I think.  Tess said should we have this on javascript - some performance issues with that. It is specialized but for people that use WA it makes a lot of sense.  I don't see anything wrong with the proposal.

Peter: marks as proposed closed - and let's close it at the plenary.

#### [PWA Change logs](https://github.com/w3ctag/design-reviews/issues/484) - @torgo, @kenchris

Rossen: I will chase this up with MS people.

Dan: let's discuss at the plenary.

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

Dan: i think we should punt this to the plenary as well.

### Breakout B

Present: Alice, Peter, David, Rossen

Regrets: Sangwhan, Tess

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo

Alice: Suggest we push this for another week until both myself and Tess catch up on this one.

#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

Alice: Left a comment on this one. 

Rossen: One of our main confusions was the use of Anchor in the web platform to mean something other than ... anchor :)

Alice: (reads comments)
... Still don't get what Anchor Space is... (reads explainer) and it still doesn't help.

Peter: Anchor == 3d point in space. It can be used to associate a given model with the surrounding space - example, putting a flower pot on top of a physical table.

Alice: If this is really a term of art in 3d I understand but it's still better if they can come up with any other name.

All: discussion on what and how anchorSpace, pose and anchor all relate to each other.

Peter: It will be good to request better example code and use case that readers can visualize and understand for themselves. Alice, can you add comment?

Alice: yes, I'll also comment about the naming of the API. 
... also, are we happy with the API? It seems pretty straight forward but there's also lots of missing info about how the API is to be used.
... we still have a problem with the API not explained well in the explainer. How do we explain the API without using IDL?

Peter: I do like having IDL in explainers...

Alice: Ideally the explainer is what you'd see on MDN.
... OK, I'll add request for better example, less IDL and the naming issue.

#### [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov

Rossen: Not much to talk about here, maybe. Lots of comments on the TAG review issue though.

David: Was trying to encourage getting issues filed against HTML and CSS. https://github.com/w3ctag/design-reviews/issues/488#issuecomment-635010629

Peter: Chris is saying the color on the web CG will file issues as they find them.

David: I think we decided last time we were happy to close this, encouraging the CG to file issues on the relevant WGs sooner rather than later.

Rossen: We discussed figuring out how we can do color contrast in terms of computed values... can we create a Typed OM color object to easily answer some of these questions. Lea mentioned some kind of color space agnostic color object. They are working on trying to release as a library soon-ish.

... Then, how do we standardise color, what is color, getting very philosophical. https://github.com/w3c/css-houdini-drafts/issues/989

... I also recall us discussing closing the TAG issue, allowing progress to continue in the CG, HTML and CSS. 

... Main feedback was about the color object, having an API to compare colors. These things are all on their radar.

Alice: How would this work in other parts of the platform, per David's original feedback?

Rossen: Color object will be color space agnostic... can you translate colors outside of the sRGB gamut .. for canvas?

David: CG is doing a bunch of that work. It's more than just canvas - things like filters and interpolation, etc.

dbaron: Possible closing comment:

> We're looking at this in a TAG breakout today, and I think we're happy closing this issue at this point, which we propose to do in this week's plenary.  We've provided a few pieces of feedback above that seem to have dealt with (see [previous summary](https://github.com/w3ctag/design-reviews/issues/488#issuecomment-620098626)), or are being actively worked on:
> * One of those is the review of sRGB dependencies in other parts of the platform, which it seems the Color on the Web CG is working on.  We'd strongly encourage getting those issues filed against the relevant specs sooner rather than later so that the working groups involved can get started on fixing them sooner rather than later.
> * Another seems to be the desire for better color conversion APIs, for which a color object proposal seems to be forthcoming.

#### [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

Alice: The last sticking point was about streaming. We tried to ask for streaming being the default right away or not at all. Mason agreed that that will be a reasonable default and made arguments about being high implementation cost especially not seeing it used in practice. I'm somewhat sympathetic to this. Further, no other engines have indicated any interest in implementing it.

Peter: I'm willing to accept that. We can be happy with a design that says "it's impl choice" but at least the design should be "streaming by default" and hope impls can make that happen later.

Alice: Perhaps that wasn't captured well in prev comments. Can you add that comment?

Peter: Sure.

#### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris


### Breakout C

Present: Alice, Dan, Kenneth, Sangwhan, Yves

Regrets: 

#### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

All: Having a look at [Brian's latest coment...](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-640917806) 

Sangwhan: tricky - leaning towards option 1

Alice: that was my gut instinct as well

Sangwhan: it feels like we don't know the exact usage patterns of an href in a mathml context well enough.  

Alice: what would be the downside of option 1?

Sangwhan: people may not like it...

Alice: they can wrap it - put an a-tag around the number.

Sangwhan: option 3 is very unlikely to happen.

Yves: are mathml elements considered as a block or not?  

Sangwhan: that's a big meta-question. Are components of mathml text-y or SVG-y ...? not sure it matters.

Yves: if you had a solution of a polynomial equation .. and want to link a whole part of the equation to something... is it possible or not?

Sangwhan: seems logical that you would like to hyperlink parts of an equation ... 

Yves: ... and we don't know the constraints put by mathml itself...

Sangwhan: ... or the implementations....

Dan: So option 1 ...

Alice: [[reviewing example given here](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-644412830)]

Sangwhan: it will be painful in the way you do it there - where each and every variable gets its own annotation.... would have to define multiple text elements... 

Alice: looking at the actual mathml... they've added hrefs to everything... 

Sangwhan: this is one example but  doesn't demonstrate anything that touches on grouped components for example...  

Alice: all leaf nodes.

Sangwhan: yes.  If you think of how href behaves in the web - it does not work only on bottom level leaf nodes.  I don't think this (example) alone defines a representative usage pattern...

Alice: if i put an A around a ... will it mess up the rendering?

Alice: we could say "Our first instinct is that (1) would be the simplest solution and to guide any future investment in (2) or (3) it would be useful to have a better understanding of how people are using hrefs. The last comment gives one example but that example has all the links on the leaf nodes and may not be representative of how people are using links."

Sangwhan: for this case I don't think it's particularly useful...

Alice: not clear the value you get from it...  

Alice: I can leave that feedback.

Alice: the stuff that we've deferred they were wondering if we had opinions.. If we can see any obvious "foot guns". If they do want to add custom elements later on and shadow dom have they done anything to make that not possible?

Alice: .. scrolling through integration to web platform section .. 

[discussion of ins and outs of shadow-dom]

Alice: they would need to come up with their own safe-list. I agree they did the right thing to punt.  Seems like a niche thing.  

#### [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon

#### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo

#### [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524) - @cynthia, @torgo

[discussing TAG feedback on miniapps]

Sangwhan: does webapp manifest allow for extensibility?

Kenneth: yes you can do this... 

Dan: do we need to create a new doc for "web app lifecycle" which incorporates both PWA and MiniApps?  There's an old PWA lifecycle doc... 

Sangwhan: we could suggest adding some new editors...

Dan: feels like a lifecycle doc should document things from a developer perspective.

[bumped and Sangwhan will work on fleshing out the doc for next week]

#### [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

[we did not get to]


### Plenary Session

Present: Dan, Peter, Tess, Yves, Alice, David,

Regrets: Kenneth, (Sangwhan), Hadley 



#### [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

#### Breakout Rollup

##### Breakout A

Dan: Discussion on **Web NFC**. Trying to figure out if we can close with consensus, or whether there was no consensus. Going back and forth about privacy prompts, privacy considerations - whether the prompting regime that's required is forceful enough. David seemed to have the strongest concerns. Kenneth has commented suggesting a stronger, non-interruptive prompt that shows the user when it's scanning. More detail in the issue. Don't know whether we can resolve this today. Might need to bump.

Dan: **Origin Isolation**. We were missing Tess and Hadley who were on the issue. Rossen summarized it a little. He was happy with it. He said not much left to do to close. I was meant to reach out to Hadley, I haven't yet - this is bumped to next week

Dan: **Web Assembly SIMD**. Kenneth is fine with it, we were missing Tess so deferred. Proposed close. Should we close it?

Tess: Sure.

Yves: [yes]

Tess: I'll close it.

Dan: **PWA change logs**. Rossen isn't here, perhaps we can come back to it when he shows up.

Peter: it's closed actually.

Dan: Okay then.

Dan: **Blink shipping process**... need to punt, still waiting for more info.

##### Breakout B

Alice: **Dom overlay module** punted to next week. **WebXR Anchors** - some comments left for them on the explainers.  might want to update the explainer explainer based on their feedback.  Other comment we left was use of the term active space - not defined. They said "it should be clear if you read the webxr spec" and we think it should be defined in the explainer. We discussed it a bunch and I asked some questions - an anchor is a set of coordinates in reference to an object in another space. The use case - you've got an object and you want to put other objects on top of it so when you move it, the other objects move with it - and that object can be a real world object [AR].  Use case is simple.  We need to schedule a chat about what a good explainer looks like.

Peter: i *do* like having IDL in explainers.

Alice: [opens issue on explainer explainer]()

David: **on color `lab()`, `lch()`** I already wrote a comment in the issue that we were planning to close this issue.  Being worked on in CSS...

Peter: close?

[agreed to close]

Alice: **on declarative shadowdom** the last sticking point was stream - we felt the best design for users would be streaming by default..  so Mason pointed out that streaming has a lot of implementation cost.  Not just complex implementation - being careful not to introduce security risks & bugs. Peter made a comment on ways to make streaming the default but to have that be open to implementation choice.  by default stream but doesn't have to. Mason made a straw-man proposal.  

[bumped]

##### Breakout C

Alice: **mathml core** we left a comment saying this looks good - and we're going to propose closing. Brian responded with 2 questions - 1 is "do we feel the issues they deferred can be deferred" - couldn't immediately figure out what those were but i remember it was largely around how mathml elements interact with shadowdom and custom elements. I commented it makes sense to defer those - because you want to have a good think about the use cases.  So yep.  Second question was how links could embedded in mathml. Brian had [given 3 options](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-640917806) - 1 is don't have links for now... Sangwhan noted he's leaning towards don't include links just put html inside mathml tags. [Another comment](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-644412830) came with some examples, but didn't make the range of use cases clear. So we left [a comment](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-648004081) - so we liked the first option the best and we thought if they wanted to pursue one of the other two options it would require additional research.

Peter: anything with an href comes from back when this was xml ..

David: I think like linking a variable in a formula to something is not that unusual a thing to want.  In wikipedia - if you have an equation with the gravitational constant in it you might want to link the "G" to an article about the gravitational constant.

Alice: Brian suggests you can embed HTML - so that is what we were going off.  It seemed implied that you can only embed it at the left node level so a variable would be fine. [Brian did respond](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-648157757). Yves gave another example - quadratic formula.  Sangwhan [also commented](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-648861529) suggesting something like an image map...

Peter: feels like there is still one open issue here. 

Alice: I was going to file an issue and the existing issue for links (in their repo) hasn't been touched since April. So I brought the discussion back to our repo.

Peter: maybe we should just re-open the issue?

Dan: let's be clear we are reopening it just for this specific (link) discussion.

[alice reopens it]

Dan: I still feel option 1 is the best...  

#### [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @cynthia, @alice, @torgo

Dan: I think they're happy and we're happy so let's close.

Peter: [closes]

#### Issue Triage

##### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) 

Tess: we're worried about script isolation... iframes... Take a step back and make a holistic review.  

[Tess & David]

##### [css color mix function](https://github.com/w3ctag/design-reviews/issues/526)

Rossen: rather straightforward review... i can be on it.

[Rossen, David & Alice]

##### [Cross-origin opener policy reporting API](https://github.com/w3ctag/design-reviews/issues/527)

[many]

##### [webxr layers](https://github.com/w3ctag/design-reviews/issues/528)



##### [geolocation api](https://github.com/w3ctag/design-reviews/issues/529)