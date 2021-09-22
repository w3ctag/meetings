# TAG Teleconference
#### 20-22 September 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-09-20](https://www.timeanddate.com/worldclock/converter.html?iso=20210920T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @kenchris, @hadleybeeman
* [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss
* [WebXR Depth API](https://github.com/w3ctag/design-reviews/issues/550) - @torgo
* [Early design review of light-DOM CSS Scope proposal](https://github.com/w3ctag/design-reviews/issues/593) - @hober, @LeaVerou, @kenchris
* [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov
* [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov
* [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2021-09-21](https://www.timeanddate.com/worldclock/converter.html?iso=20210921T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia
* [Back/Forward Cache](https://github.com/w3ctag/design-reviews/issues/628) - @hober
* [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov
* [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

### Breakout C (APAC / Europe) - [2021-09-21](https://www.timeanddate.com/worldclock/converter.html?iso=20210921T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo
* [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov




### Plenary Session - [2021-09-22](https://www.timeanddate.com/worldclock/converter.html?iso=20210922T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)


* Breakout Rollup
* Issue Triage
* [New principle: Do not design around third-party tools unless it actually breaks the Web](https://github.com/w3ctag/design-principles/issues/335)


-----


## Breakout A

Present: Dan, Peter, Amy, Rossen, Lea

Regrets: Kenneth


### [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @kenchris, @hadleybeeman

plenary

### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss

plenary

### [WebXR Depth API](https://github.com/w3ctag/design-reviews/issues/550) - @torgo

Dan: A [response from Piotr](https://github.com/w3ctag/design-reviews/issues/550#issuecomment-920217096)... doesn't think it'd be controversial to add more text.. similar conversation around raw camera access, he's getting a lot of feedback about fingerprinting and privacy issues.. I want to say we'll review it when there's a PR

Rossen: yeah.. a lot of squishy language, UAs 'could'.. prefer to see more normative

Dan: yeah

Rossen: if this is a note that'd be fine. if this is a spec they need to work more on the language, but right direction

Dan: in your note about fingerprinting he did talk about the S&P questionnaire. I'm wondering if there's anything else we can point him to, unsactioned web tracking finding or something, that would underscore the issue. Great feedback that there needs to be more normative text.

Rossen: can leave a comment, schedule for next week. Outside of fuzzing, once this is done, we should consider closing it?

Dan: I think so.

### [Raw camera access](https://github.com/w3ctag/design-reviews/issues/652) 

Dan: I'm in the middle of trying to write a response to Piotr's response to my question about making it privacy friendly. Prompting is necessary but not sufficient. Needs to be some intrinsic part of the API that makes it more privacy friendly. Maybe again that's advanced fuzzing, I don't know. So I'll write a response. Discuss at plenary.

### [Early design review of light-DOM CSS Scope proposal](https://github.com/w3ctag/design-reviews/issues/593) - @hober, @LeaVerou, @kenchris

Dan: there was a [response](https://github.com/w3ctag/design-reviews/issues/593#issuecomment-920291268) to Lea's comment...

Lea: I think the main issue with this is that it introduces two things - oen to do with selection logic, one to do with scoping. The scoping thing is ?? but selection thing looks like it would fit better as a selector, but difficult to invent a selector around it, but she's listing ideas in her post. Maybe we should say it's a good direction and close it. Can't just keep pushing a selector, if they looked into it and it's not possible..

Dan: it's happening in CSS WG.. it's CSS WG's job

Lea: yeah

Dan: as long as we think it's not breaking the web we ought to close it

Rossen: makes sense. Feedback provided already is outlining different options and opportunities to explore. As TAG we've done our job in providing feedback, we can't design the feature

Lea: resolution satisfied? [will comment and close]

### [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

Dan: noted we feel it's blocked behind FPS. Feel like we need another session with Kaustubha where we talk about this, FPS and CHIPS. Next week?

### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov

Lea: I didn't see a response

Dan: wait more

### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov

Dan: Rossen left a comment last week, they've got back to you

Peter: not sure they got the point of [rossen's](https://github.com/w3ctag/design-reviews/issues/632#issuecomment-920456385) comment.

Rossen: they're saying we need client code to change so that you're pulling all the time?

Peter: "..always expected to require new resources" - I don't think that's true

Rossen: it's not. When I go to print I don't necessarily have to go and redownload everything

Peter: possible to do that if you want to shave a few bytes of some stylesheets or you have significantly different media, but not a requirement. 

Rossen: either we're talking past each other.. but I'm surprised. Yoav's part is more about where the work happens. I'm surprised by Thomas' response because I thought i was pretty clear when I explained the fact that styling is clientside operation today. I can see having a document that relies on clinet hints only for downloading everything

Dan: and you get a static html?

Rossen: you're in light mode for example, you make your initial request, client hints say you're in light mode, get a bunch of resources for light mode, done. The next thing is they go into a darker room and their device automatically switches into dark mode. In that scenario where this document was written using client hints only because the platform allows me to just rely on client hints only, so now I'm going to send a UA client hint that says dark, which means the server needs to recognise that you went from a light to a dark mode, that's a change, I need to send a whole bunch of new content, stylesheets, images, etc. Which means the state is now being transferred over to the server side

Dan: is that really what they want? That can't be what they're designing for

Rossen: this is how the current feature will work. I don't believe they want this.. I'd be surprised. However you're giving me an API I'm going to use that API and nothing else. So now I'm changing the way i communicate about media features to be directly on client hints only. This gives me performance.. The point is when you change the API which is currently available on the client only the client does all of the different media or feature detection, change detection. Through style recalc it recognises what needs to be changed and fetched. This is why users are adding all existing logic for dealing with media changes inside the document - light stylesheet, dark stylesheet, etc. They're setting up all of that on the clientside so when the client starts making decisions locally they can fetch the things that the authors expect them to fetch for that particular media environment. Put that on the server side as a set of hints, now as an author I don't have an incentive to put all of that stuff on the client. I can say the server will take care of it somehow. I'm hinting that i"m in dark mode or want reduced motion so the server needs to give me that stuff. The first time I navigate there the server will take the ints and give me the right stuff. But as the hints change the server needs to recognise this and say you just changed from light ot dark so I need to give you a new stylesheet. That change detection needs to happen on the server, and that is a very different model than the way styling happens today

Peter: I think they're coming from the author would still put the logic clientside and this would inline or optimise.. you can design all the logic clientside and do a small optimisation using this hint, or you can totally screw it up and do all of the logic server side

Rossen: you're promising this api is going to be so much faster and better, I'm going to jsut use this API, and it's the only thing I'm going to use. Now I screwed up everything because media detection needs to happen on the server side.

Peter: I accept it's an opportunity for small optimisation. You already need the round trip for the client hint. By the time you've made the round trip you could have just pushed all the logic... even if it's used properly I'm not sure it's buying all that much

Rossen: let's say for very heavy traffic websites it buys a lot.. Minor saving on initial load, however it comes at the cost of changing style, media logic to be pushed onto the server side. In the worst case where I only depend on client hints. We just changed everything.

Peter: one thing Tom mentioned is the server could inline some stylesheets.. not sure that buys a whole lot of optimisations in an h2 world

Rossen: agree. Server inlining styles great.. but you're still pushing logic onto the server side

Dan: what's our suggestion? Cut the feature?

Rossen: that would be my proposal

Dan: if it really overcomplicates things for developers by creating these two different paths

Rossen: duplicating capabilities. We don't do that anywhere else. [will leave comment]

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Lea: open for a while.. push back mainly from Apple.. said we'd bring people to a special session or something. it's implemented in Chrome, nobody else seems to be interested in implementing it.

Dan: multi stakeholder red flag. Could close it satisfied with concerns, feature looks fine but nobody is implementing it?

Lea: there is a big philosphical debate around the feature.. authors should use the default control as much as possible, so if removing a button makes people use default controls so be it. Other side says if people want to do something user hostile usch as removing a download button we should make it difficult and they should use custom controls. Apple is worried that if ithis goes through people will exclude safari based on the fact it doesn't implementing the download button at all. Google wants to provide useful features and it doesn't scale to have everything visible by default. you can still right click and download the video but it's less discoverable.

Dan: If there's a debate and we don't feel like we sholud be in the middle we should close with ambivalent?

Lea: there is a position for the TAG to discuss it and decide on the larger issue here, but it's a long discussion. There is a larger issue.

Dan: plenary? 

## Breakout B

Present: Peter, Rossen

Regrets: Sangwhan

### [HTMLScriptElement.supports(type)](https://github.com/w3ctag/design-reviews/issues/674)

Rossen: [Closed with comment](https://github.com/w3ctag/design-reviews/issues/674#issuecomment-923490992)

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

### [Back/Forward Cache](https://github.com/w3ctag/design-reviews/issues/628) - @hober

### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov


### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov

### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov


## Breakout C

Present: Dan, Ken, Yves, Amy, Sangwhan

Regrets: Lea


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo

Dan: 5 days ago we left [feedback](https://github.com/w3ctag/design-reviews/issues/523#issuecomment-920704365).  They've opened an issue looks like they will discuss...

### [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov

Dan: we fed back what's going on because Speculation Rules themselves are sitting in some private repo and looks like there's not consensus on them to begin with. I mentioned this to Chris H and he said he'll progress it. Nothing happened yet.

Sangwhan: seems like it's driven by people in Tokyo and it's a holiday in Tokyo this week

Sangwhan: a lot of web sites do click tracking - don't know how they plan to address this - sure they've thought about it.  The concern I have is that this can trigger false clicks because the click tracking works via a rediretc. The prefetch will hit the redirect which will log a click that didn't happen. That's worth thinking about. Prefetch will destroy all of it.

Amy: I asked about that for the first speculation rules issue - [response was that there's a prefetch header](https://github.com/jeremyroman/alternate-loading-modes/issues/56#issuecomment-805144539) - but that means there would need to be code updates.

Sangwhan: won't work 

Amy: other response was that prefetch doesn't run JS so any JS-based analytics won't run - which is good.

Sangwhan: but for an externally tracked redirect - that would render the prefetch refresh because the page you want to fetch is gated behind the script... it's worth asking.

Amy: it may be in the [speculation rules](https://github.com/w3ctag/design-reviews/issues/611) explainer, at least there's discussion about it in [the issue](https://github.com/jeremyroman/alternate-loading-modes/issues/56).

Dan: there's lots of work on this, lots of contributors, and it's not in a CG, IPR policy is still unclear. Why isn't it in WICG?

Dan: [leaves comment on our original issue](https://github.com/w3ctag/design-reviews/issues/611#issuecomment-923754268)

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

Sangwhan: will block out some time, it's a massive spec

Ken: would be nice if people who created babylonjs or threejs to give feedback

### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov

Dan: we closed #649 which is related. One issue is just as with 649 it jumps right into talking about sites that want to continue using sharedarraybuffer must opt in to cross origin isolatuion, it doesn't talk about use cases

Ken: they have a section called 'what are anonymous iframes', 'documents can create..' - is this a new thing? Sounds like something you can already do

Dan: that's the proposal. Later on it says something about autofill.. is that one of the main uses?

Ken: difficult to dissect this. Sounds like they want this by default in anonymous iframes so for some reason that makes it safe?

Sangwhan: what's the final end user use case?

Ken: I'm wondering what is the use case where you don't have any credentials but you have anonymous iframe and want to use sharedarraybuffer. Getviewportmedia I assume is for camera acess?

Dan: [drafts feedback]
```
Hi @camillelamy I have similar feedback as i did for #649 which is that the explainer jumps right in to talking about how "sites that wish to continue using SharedArrayBuffer must opt-into cross-origin isolation" without first talking about the end-user use cases (the user need).  What user need is being served by the use of SharedArrayBuffer in this context that this set of mitigations is aimed at securing?  You talk about password managers later on in the doc - is that one of the primary use cases? Can you please amend the explainer to start with a few user needs to help us set the context? 
```

Sangwhan: I understand the S&P needs but not when this would be useful. What applications does this have?

Ken: me neither but they mention getviewportmedia.. 

Sangwhan: screen sharing

Ken: i want my anonymous iframe to get my screen?

Sangwhan: camera and screen

Ken: definitely want opt in for iframes to get my screen and camera. I don't want embedded iframes to get access whether they're anonymous or not

Sangwhan: Feedback is - who is the consumer of this thing?

Dan: Hadley did already ask about the user need and Camille did respond, but it's still not reflected in the explainer

Dan: [leaves amended comment](https://github.com/w3ctag/design-reviews/issues/639#issuecomment-923765868)

### [Back/Forward Cache](https://github.com/w3ctag/design-reviews/issues/628) - @hober

Sangwhan: set to proposed closing

Dan: Two PRs, one on s&p questionnaire and one in design principles that landed. I think it should be closed. We need Tess in the room. Plenary?

Sangwhan: I'll take a look before that. Seems like it's not a new proposal, but to define stuff thatw as never defined properly. We don't have much to say in terms of if it's a bad idea - it's already been done, they're just writing it down.

### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov

Dan: 8 days ago work going on on the spec

Ken: payment integration...

Sangwhan: I see what they're trying to solve, this makes sense. Doesn't seem compatible with.... the capability delegation protocol and capabilities should probably be aligned with what we have in permission policy

Ken: yeah, what capabilities is this going to apply to?

Sangwhan: right now it's payment request

Ken: and fullscreen

Sangwhan: it's in the example and they've been thinking about it but current origin trial is just for payment request. The use case is fine. Seems a little bit unaligned with permission policy. It should be delegating a permission based on a user activation and request? If you're delegating an iframe to be able to do getusermedia based on the parent being granted getusermedia... should that be possible or should that be a separate permission? if you do getusermedia request on an iframe you're going to get a permission request on a different origin than what the user is looking at.. that's weird.

Dan: i was tracking down multi implementer support angle.. Chrome status page says positive feedback from Mozilla but when I followed that link it goes to a mozilla standards position where Anne says "I'm not 100% sure I understand this correctly" but does say agree it seems useful... but I think this is more.. positive engagement.

Sangwhan: not affirmative

Dan: yeah

Sangwhan: a bunch of unanswered questions, the fact that user activiation doesn't pass through iframes correctly at least from a scripting perspective is problematic. it is a user activation but in certain cases it doesn't work from an end user perpsective which is confusing. User activation gating is our problem not their problem as an end user. i have to think about this more. I can see the utility, definitely. There's a problem that needs to be solved, just don't know if the proposed api is the right way to approach it. 

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/655#issuecomment-923775239). Come back to it at plenary.

## Plenary Session

Present: Peter, Dan, Yves, Lea

Regrets: Amy, Sangwhan, Kenneth

### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

### [New principle: Do not design around third-party tools unless it actually breaks the Web](https://github.com/w3ctag/design-principles/issues/335)

Lea: naming things certain ways to avoid collisions with SAss seems backwards to me.

Peter: we had this issue years ago with grid.  There were issues with collisions with Sass. I was against that... CSS has extensions points..  

Lea: in 20 years from now CSS will still suffer from these design decisions but sass may not be around...

Peter: extremely dangerous to design the language around a tool that extends the standard in a non-standard way.

Yves: sets a precedent ... 

Rossen: We didn't design the C# language around visual studio... what Peter said makes a lot of sense...

[we got dogpiled]

Lea: It's not about theortical purity - it makes CSS a bit harder to use to avoid inconveniencing the users of the 3rd party tool.

Rossen: On a technical level - I'm having a bit of disconnect. Let's assume this is another tool - dev tools - that has some kind of eventing expectation out of dom.  If I understand the intent - the way I perceive it - "we have a tool - this tool creates a bunch of habits in people - now we work on a platform that has capabilities exposed by API - the tool interacts with the API to make things more convenient - the chain of dependency only goes up the stack - you cannot depend on a tool from a platform - we can't depend on something on top of us - just as we can't tell a lower level platform what to do." So there's a layering problem here. Secondly we have clear rules and guides - a boatload of people who are getting together and talking about this platform.  We have established process of making things happen [in CSS wg]. We cannot take explicit dependency on upper layer expectations.  We should not introduce breaking changes fot the hell of it... But this community - we cannot ignore them - but we need to make it clear to them why we make the decisions at the appropriate level. They should come join us in CSS or at WHATWG if they want to influence the standard...

Peter: that's my attitude - but back when we had this issue with the parentheses in grid ...

Lea: it seems like if 2 options are sort of equiv then it makes sense - but if one has clear usability advantages over the other then it doesn't make sense to choose the less usabile one because of a 3rd party tool.

Rossen: could some of the feedback be because of how the issue is worded - "do not design" - i think we have an opportunity to start changing the direction around dependencies .. 

Lea: I agree it's worded too strongly.

Yves: in this case there are specific rules for doing extensions that don't clash... In the case of XML, CSS etc.. you have ways of doing this in the right way. In the Sass case they didn't do it.  They should use an extension...

Rossen: I agree. We should also figure out a way to shift the topic away from Sass and CSS... Other examples we can offer that are similar? To point out this is about layering.

Yves: 1st point - your tech should have extension points; 2nd point: what happens when despite rules to avoid clashing someone makes something that clashes - do you need to reserve some spaces for this or should you not care?  It would make it more generic.

Lea: we should try to shift the whole thing from Sass and CSS.  That debate should happen in a CSS working group issue.

Rossen: I'm happy to jump in and be the new tag member on this - and invite people to debate this in the css wg - and repivot the discussion on this issue to the generic issue.

Lea: the general issue needs discussing.

Yves: doesn't capture the fact of something done against extension rules... 

Dan: Something about designing good extension mechanisms...

Yves: and what to do when people do not conform to that extension mechanism...

Peter: [relating to the Sass issue] there *has* been an extension mechanism... CSS has had vendor prefixes since the 90s... They could add a single dash `@-if`. I will reply to one particular point that Natalie made.

Yves: many people commented on the thread about the use of prefixes... 

### [Raw camera access](https://github.com/w3ctag/design-reviews/issues/652) 

Dan: I left [a comment](https://github.com/w3ctag/design-reviews/issues/652#issuecomment-924333585) but no response yet.

### [PR on the issue template](https://github.com/w3ctag/design-reviews/pull/653)

[squashed and merged]

### [WebXR Depth API](https://github.com/w3ctag/design-reviews/issues/550) 

Rossen: [drafts closing comment](https://github.com/w3ctag/design-reviews/issues/550#issuecomment-925057369)

**CLOSED**

### Issue Triage

[4 issues triaged and set to next week]
