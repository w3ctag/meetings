# TAG Call Minutes - Week of 28-feb-2022

## Agenda

### Breakout A (Europe / US) - [2022-02-28](https://www.timeanddate.com/worldclock/converter.html?iso=20220228T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @cynthia, @torgo, @atanassov
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov
* [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @plinss, @atanassov
* [`handle_links` manifest field ✨](https://github.com/w3ctag/design-reviews/issues/695) - @cynthia, @torgo, @ylafon
* [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo

### Breakout B (US / APAC) - [2022-03-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220301T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov
* [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov
* [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou

### Breakout C (APAC / Europe) - [2022-03-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220301T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion
* [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @torgo, @maxpassion, @hadleybeeman
* [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon

### Plenary Session - [2022-03-02](https://www.timeanddate.com/worldclock/converter.html?iso=20220302T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

## Minutes
  
### Breakout A (Europe / US) - [2022-02-28](https://www.timeanddate.com/worldclock/converter.html?iso=20220228T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Rossen, Tess, Yves, Amy, Lea

Regrets:

#### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @cynthia, @torgo, @atanassov

Rossen: Close?

Dan: pending external feedback. Need to be happy with response. Need Sangwhan's input.

#### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov

Rossen: both (689 & 690) are being experimented with

Dan: Peter asked a question about object vs DOM rect. No response yet.

Rossen: what would be the lifetime of such object? The beauty of rects is that they're immutable valid for the time being. If I return object now we're talking about bringing in the whole kitchen around the sink with events..

Peter: doens't need an event, doesn't need to be live, could be a snapshot. This isn't a blocker. Just a question. Negotiating API shape, overall happy with the feature.

Dan: Close with that question? Ping requester again?

Peter: worth completing the conversation

Dan: could close on wednesday if we get that feedback

#### [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @plinss, @atanassov

Rossen: we thought of signing off on this and moving forward. Then someone added something for security and privacy, we challenged and asked for something in particular. It's been a month since we asked. I'm very happy with the CSS primitives one, but close to it. Don't want bias. Ken was also pretty happy with this. The final thing is that (with CSS bias) CSS WG is favourable to this approach.

Dan: I'm happy with it, also work for a company with devices with folding displays. It's in the correct place. Concern about multiple implementations. No Chrome status link.

Rossen: Weird. https://chromestatus.com/feature/5310356412956672

Dan: I think Samsung is going to implement, that's Chromium

Peter: question - looks like you can use environment variables in media queries? 

Rossen: You can, yes

Peter: that was a concern I had, I wanted to make sure you could do media queries based on the size of a segment. Given tahts the case I wonder if the number of segments should just be exposed as an environment variable as well. Utility in having the number of segments as an environment variable, that's a new question

Rossen: what are you intending to do? Focus management?

Peter: is there a use for having that? For consistency does it make sense to have everything exposed as environment variables, then wondered whats the use case for that. Definitely use case for the size/dimensions of the viewport as environment variable, but wondering if there's a use case for the nubmer of segments

Tess: if it's greater than 1 that's a simple test. Maybe I want to refocus the 'primary' on essential information

Peter: you have the media query for that. A high level property that you can query. Does it make sense t have as an environment variable as well so you can use it in other properties?

Rossen: example usage? I'm detecting horizontal viewport segments 2, and I have a bunch of details to layout things properly, query env vars to figure out how big are segments, and do sutff. But I'm already in the context of 2, I know i Have 2. How am I goingto use that information i nthat block?

Peter: not useful in that block. Is itu seful outside of a media query block in some other property?

Tess: if you're doing a calc with a modulus, you might want to .. if you're trying to place something on one of the segments but you're trying to do it in a generic way with any number of segments

Rossen: starting to get a use case in mind.. I'm curious on whether or not this is something that is needed to start with? This is a purely additive feature. You acn express the same thing right now with a variable, doc variable, doesn't have to be environment variable, can set it inside the media query block. Then use it everywhere else. If we detected this as a very popular use case we can drop that into an environment variable at that time. 

Peter: I accept that. Thinking that if there's a use case later on and we add an environment variable it would seem weird t have a high level property and an environment variable exposing the same thing. Redundant. If that's the case, if we can predict that, does it make sense to make it all environment variables right now. I don't have a strong argument, just wondering. In any example I think I'd use this feature in a media query I'm 90% sure I'm going to be querying other aspects of the viewport as well. If a segment is very very narrow I maybe dn't want to split my layout into two parts. That can very easily be the case if I have a window not taking full screen and mostly on one segment and partially on another segment. Only 50px on one segment I dont' want to split my layout into 2 halves. If every media queriy is going to include number and an env var about segments maybe let it all be env vars

Rossen: I think what you're describing is probably something that we need to work at with the CSS WG. And we can and should record this as a feedback, here or in a CSS issue. Stepping back, from the pov of TAG and signing off on this review, do we have any reasons to push back? What we're talking about is additional shape considerations that can be worked out by the right people.

Peter: not trying to make that deciision, I agree that CSS WG is the right place. Is there enough agreement in TAG to ask that? Then we leave it as feedback and let CSS WG decide

Tess: It seems like it's not a blocking thing. Definitely something that the CSS WG should think about. Do that via part of our closing comment or filing an issue.

Peter: yep

Rossen: my take as well. Definitely capture it.

Dan: agree to close with a positive comment?

**agreed to close positively**

#### [`handle_links` manifest field ✨](https://github.com/w3ctag/design-reviews/issues/695) - @cynthia, @torgo, @ylafon

#### [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo

### Breakout B (US / APAC) - [2022-03-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220301T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Rossen, Max

Regrets: Sangwhan

#### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @cynthia, @torgo, @atanassov

'[from a]'

Punted to C for Sangwhan

#### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Punted to F2F for Lea and Tess

#### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

Reviewed status, punted to F2F.

#### [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo

Punted to C for Sangwhan

#### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov

Punted to F2F

#### [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou

Punted to F2F

### Breakout C (APAC / Europe) - [2022-03-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220301T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Hadley, Max, Sangwhan, Yves

Regrets:

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Dan: Will ping group chairs.

#### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion

Max: waiting for the authors to respond... 

#### [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @torgo, @maxpassion, @hadleybeeman

Hadley: waiting for responses

#### [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon

Yves: want to answer, the crux is that their solution doesn't fix the issues with the use of CSP .. [??] and use of http-equiv for that is not really good

Dan: can we get other voices to support? mnot?

Yves: would make sense

#### [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo

Dan: proposed closed, waiting on a closing comment about changing name

Sangwhan: I'll do that right now. There's a user need about capturing one area of the screen.. why only window or desktop? And this featuer dosen't give user control of exact bounding box but lets application choose, another unfulfilled user need here

Dan: and user sharing what they don't expect to be sharing?

Sangwhan: application chooses what is shared, so far nothing outside of user's viewport. However there is no way for the user to decide which part of a document to be shared, nor a way for the user to..

Dan: the application decides "this is the appropriate thing to be shared when you select my tab"

Sangwhan: this is fine, but why are we not giving the user a choice

Dan: the application might say it's the content well that is the appropriate thing to display, but the user might actually want to be displaying the navigation because they're in a customer service scenario to say 'the menu option you told me about doesn't exist' or something like that. Strange to be constraining the user choice that way.

Sangwhan: at least two native application focusing tools let the users do that. 

Dan: that's the articulation of the user need that you mentioned. I want to display this section of the screen, it's a different thing.

Sangwhan: different but wanted to keep it on record. [close with comment]

```
Thank you for the clarification!

> I think you initial interpretation was in fact correct. The element defines a bounding box to be streamed.

I think there is a minor misunderstanding here, we understood this as a bounding box (draw a rectangle) in any part of the desktop - which is not what this proposal is about.

Given that the naming/expectations might introduce confusion - may we suggest renaming this to something that suggests a specific scope? (e.g. "Tab" Region Capture)

Additionally, we'd like the group to consider the unfulfilled user need of "stream arbitrary region from any part of the screen" in WebRTC at some point.

Thank you for bringing this to our attention, and we are happy to see this proposal move forward.
```

**closed**

#### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @cynthia, @torgo, @atanassov

Dan: The issue that Ken raised has not been.. not clear whether it should be a blocker. I think this sounds fine. 

Sangwhan: some flaws in original gamepad API - they're aware of this - this is trying to fix some of them... 2ndary interface.

Sangwhan: ... I think this is fine.  

Dan: Ken is comparing it to generic sensor API?

Sangwhan: Ken's idea would make things complex - for each event listener you would have differnt ways of handling things -- complicate implementation.  I can understand both sides of the argument... 

Dan: if it adds complexity.. The user need is articulated well. People want to play games.

Sangwhan: writing games with current web tech is not good, you have to implement a poll inside RAF. This fixes some of that because it lets you develop games in a way that web apps are supposed to be made, so the api is less horrible. I feel like this is good.

Dan: agree

Sangwhan: I'll say if it's a tradeoff with complexity it's okay for now, might want to revisit in the future

### Plenary Session - [2022-03-02](https://www.timeanddate.com/worldclock/converter.html?iso=20220302T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Dan, Max, Rossen, Peter, Hadley, Yves, 

Regrets:

#### Breakout Rollup

##### Breakout A

Dan: Closed gamepad API events 662 with a :) Viewport segments property.. potentially closing.

ROssen: thought we closed it

Peter: we were hoping they'd give us a response to our last comment

Rossen: I did ping the team internally, they ack'd. If a response is not blocking then we close it.

Dan: feel like we should not close until we have closure.. on for f2f

Dan: foldable device primitives closed, satisfied. Handle_links not progressed; new comment. Reassign to f2f. Dark mode support, pending external feedback

Peter: no response to Tess

Dan: on for f2f. 

##### Breakout B

Peter: Max and I were there. Issues needed someone who wasn't there; moved to f2f or C. Talked about distributed tracing, no progress.

##### Breakout C

Dan: closed region capture. Raw camera access.. limbo, will ping group chairs. JS self-profiling, waiting for response. Web app launch andler, still waiting for responses.  Markup based clinet hints delegation; Yves following up

Yves: asked why it's not CSP.. their solution is not any better

Dan: come back to it at f2f

#### Issue Triage

Maybe look at: [Confirmation of Action](https://github.com/w3ctag/design-reviews/issues/713) 

Rossen: for this one I know there has been work with folks from Google.  Aaron L. - member of ARIA group -  in terms of venue it's where it's heading.  The user need and capability - a pain for quite a while now - the work arounds are ugly and tend to break content.

**on for face to face**

Also [Large, Small and Dynamic Viewport sizes](https://github.com/w3ctag/design-reviews/issues/706) 

[Digital goods](https://github.com/w3ctag/design-reviews/issues/571) where do we want to take this?

Peter: shape has changed... 

Dan: I put on the agenda for the f2f

[EditContext](https://github.com/w3ctag/design-reviews/issues/416) - shall we close it?

**assigned to f2f - hopefully to close**

[Deprecating document.domain setter](https://github.com/w3ctag/design-reviews/issues/564) - feedback from requestor received - shall we close?

**on for 3-14**

[HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - we're going to discuss it at the f2f -are there questions we want answers to?

Peter: waiting for Lea and Tess to be both be on a call

**face to face**

[Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - all 4 issues closed - can we review what kenji had to say? <- high priority

**will review and close at f2f**

[\<search\> HTML element](https://github.com/w3ctag/design-reviews/issues/714) - we need to re-triage

**on the f2f agenda**

Amy: explainer not a stand-alone document ?

Dan: needs to lead with user needs

[ObservableArray](https://github.com/w3ctag/design-reviews/issues/693) - introducing the observable array pattern to the web -  we need to add assignees & re-review

**on for f2f**

