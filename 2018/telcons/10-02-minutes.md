## TAG Teleconference
##### 02 October 2018

Present: Dan, Peter, Lukasz, David, Mr Moon, Yves, Travis, Alex

Regrets: Kenneth, Hadley, 

Chair: Peter

Scribe: Dan

---

Agenda:

* [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) - @cynthia @dbaron @travisleithead
* [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) - @cynthia @dbaron @travisleithead

Sangwhan: read Martin's comments. he raises good points. e.g. Quic isn't complete; this is a streamish level socket API... why is this restricted to webRTC. 

David: I think some of the ideas are making it less restricted to WebRTC - opening up some of WebRTC to other things. Martin says that raises inteeresting questions.

Sangwhan: it's defined as a webrtc related spec which seems strange. I would like to set up a call witolh the IETF folks about this. 

David: i thinkt this is some proposals from a few companies, mostly google. .. The people who are working on QUIC think it's not ready yet. ICE is what's used to initiate the WebRTC connection. If you expose it more generally then you expose a mechanism to open up a connection to some port on some other machine... and Martin wonders anout whether the permission model is thought through to do that a(outside of the RTC context).

Travis: this is about using the RTC Quic transfer outside of a peer connection.  I have a bunch of feedback about that.  I had some higher points of feedback - their explainer is … light on details. The design section is … [short]. I would like to see an signifigant update thto the explainer: motives, rationale, security considerations, privacy considerations, etc... Also i don't like interface names that have the technology name in the title.  When I see "RTCQuicTransport" etc… directly reflects underlying tech. Term "peer connection" is o. k. 

Sangwhan: I agree [with naming issue].

Travis: I understand the motivation behind it... had to look into RTC Data Channel a bit - RTC data channel is message based. It tries to map onoto ther existing web socket usage pattern. Very "webby". This quictransport is supposed to expose a more primative form of transport. Not geared to client server. Building a communication channel that is lower level than an already low level message passing API. Is that really necessary? Also introduces another stream in the platform.  Maybe not aligned with Srreams.  Using the constructor pattern is good - introducing a constructor for the rtcice transport.  That's good feedback.  Explicit start and stop APIs - might dinterfere with... []. It's [RTC] already complicated to use.

Dan: what is the motivation?

Travis: the goal is - from a capabilities standpoint - byte level messaging through p2p connections... 

Dan: but what functionality does it support?

Travis: whatever it used to do but more securely / betetr / faster because of quic.

David: based on EWS ideas.

Sangwhan: do we want something that is based on webrtc at the moment.

Travis: RTC data channel is already a thing...  There is already something out there. What does this add on top of that? Speed, access to a lower level of data passing, access to more of the connections set-up... RTC interfaces have been the victim of STP.  

Dan: so all of that should be documented int he explainer...

Peter: can it open up a random port to a random machine?

Travis: you need a signalling layer. ICE can help you.  

Peter: ..e S.uses STUN and TURN... im curious if this wraps enough around ICE to ... have sufficient security.
 
Travis: looks like in WebRTC there is an automatic set-up option.  

David: i think there's a related question with WebRTC - in that design there is atrade off between 2 webrtc endpoints inside the firewall...

OOPeter: there would be things that would be awesome to do on the web - e.g. making my own connection to port 993 and be an imap client, but also don't want to make the web browser into a port scanner or ddos machine. Even behind a user permission that's not necesarilly good enough. ... same origin doesn't help us here.      

Sangwhan: invite the IETF folks?

Dan: I suggest we ask them tu o update the explainer.

Sangwhan: I will do that [update the issue].

Peter: who to innvitvite?

Travis: martin thompson, ekr, 

Yves: domenic ?

Sangwhan: domenic seems to be fine with the pseudo-stream design.

Travis: we should have documented how the 2 relate to eachother.

Peter: give them a week?

David: it would be useful to have the update explainer... it might turn out that a good time to do this is at TPAC.

Peter: bumped for a week and then we check in.



* [Canvas TextMetrics](https://github.com/w3ctag/design-reviews/issues/302) - @dbaron

[bumped a week]

* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @torgo @hadleybeeman

Dan: I will try to connect with Hadley on this and try to come back with an update by next week.

* [User Activation API ](https://github.com/w3ctag/design-reviews/issues/300) - @dbaron @hadleybeeman

Alex: we should bump it.

* [WebAssembly Threads](https://github.com/w3ctag/design-reviews/issues/299) - @cynthia @dbaron @travisleithead

Travis: i took on this ... overview : this is nit ot a proposal for a new thread function call. it adds primiatives to the core of the web assembly language to implement their own threads in web assembly. Just like in TC39 where they introduced shared array buffer and atomics, this proposal similarly adds  way to make a buffer as a shared buffer and extensions to their native integer types - I32 and I64 - you can use .atomic. and exposes a few atomic operations - load/store, read/write/modify, or ans xor. Some of these atomic operations allows you to create mutexes and semaphores.. wait and wake operators... sthe ones you use to block and start a mutex. With all of this and the ability to mark target memory as shared I think you've got what you need to create a threading model of your own design. YYThreads in web assembly.

Peter: is the shared array buggeffer shareable to JS?

Alex: yes. sharable to JavaScript.   Shared mutable memory access. 

Dan: we're building the web into a much lower level application development and deployment environment. (between this and the transport topics we already talked about)

Alex: we talked about .. image decoding ... media .. encoder... we're missing hooks to make that work efficiently.

Alex: my earliest feedback was - don't reinvent new execution context. I stt st seems they have fonollowed that advice.

Travis: yes - you need to spin up a worker. 

oPeter: are we happy with it? any more feedback?

Alex: make sure there are issues with synchronous/async

Travis:Nothing raising red flags with me. The call is webassembly.memory constructor. You pass in a disctionary and it's been extended with a shared flag. Memory can be enlarged. That shared flag applies to the entire memory buffer you're creating.

Travis: it's nice to see an example - appreciated that. [at the top of their explainer]

Alex: it all looks good to me.

Travis: full approval.

Dan: security / privacy issues?

Alex: it creates new operations on existing types but doesn't create new types / allow new...

Peter: they did fill out the privacy / security questionnaire. they said they could potentoally get higher percision for SPECTRE type
type attacks.  
  
Peter: they need a good feedback for doing a good explainer here.  

Dan: gold star.

* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @hadleybeeman @travisleithead

[bumped]

* [User Activation v2](https://github.com/w3ctag/design-reviews/issues/295) - @dbaron @hadleybeeman

Peter: we already briefly talked aoout it.. 

David: this is the one about trying to spec a new behaviour when the activation occurs. We made some requests for updating the explainer.. it was updated 5 days ago - have not reviewed yet. SUggest we bump.

Peter: bumped.

* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff @dbaron

Alex: I had a conversation - but ..it was blocking on an issue at CSS working group...

Peter: Which issue?

David: I wanted to look at a bunch of these timing issues.

Peter: what should we do?

vidDavid: the substantive thing i'm worried about - their event loop - they inserted some text - one of the problems was we disagreed over where it should go - disagreement over what the existing spec meant.  We need to sort it out. Implementers all understood offne thing which [didn't match]. Havne't had a chance to sort out yet.

Dan: TPAC discussion?

David: depends if we can get right group of peopltogee togetehr... Bump 2 weeks?

Peter: OK 

---



