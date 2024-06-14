# TAG Teleconference
#### 10-13 June 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-06-10](https://www.timeanddate.com/worldclock/converter.html?iso=20240610T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion
* Issue triage

### Breakout C (California / Australia) - [2024-06-10](https://www.timeanddate.com/worldclock/converter.html?iso=20240610T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon
* [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober
* [Requesting review of HTML Ruby Markup Extensions](https://github.com/w3ctag/design-reviews/issues/959) - @hober, @LeaVerou
* [improvements to \<details\> styling (widget structure)](https://github.com/w3ctag/design-reviews/issues/965) - @hober, @LeaVerou, @matatk

### Breakout E (Europe / China) - [2024-06-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240612T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion + Guests

### Plenary Session - [2024-06-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240613T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon [explainer has updated]

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Matthew, Amy, Yves

Regrets:


### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

We're waiting for an update on the explainer, no activity yet.

### [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion

Dan: we'd been in discussions with Sangwhan to try to channel Sangwhan's feedback. Matthew left an update and they replied.

... I think this is reasonable. There are a list of things that could have an impact on overall web perf.

Matthew: appreciate the detailed reply. It starts by saying "in Chromium on windows". So anything else wouldn't necessarily have that answer. General concern - yes there is a general thing of if you overtax the platform it goes slower. We've tried to mitigate against that in some areas in recent years with things like workers and trying to move stuff off the main thread. It seems a shame.. shouldn't we try to encourage new things to not have that type of failure mode? Where they can bring down the rest of the user experience? Most people probably will be responsible but... is that a high bar to ask? this is going to run on a lot of iddferent devices with different hardware, model sizes, processing capabilities... different \*PUs ... agree that we should try to not get into a situation with new stuff to not degrade the user experience? It may be slightly unfair to put all that effort on these people, but this is a new thing and we have an opportunity. But I don't have a suggestion to say how they could do this. Whether there's some OS level multitasking they could fall back on rather than in browser?

Yves: question about that.. easy with the modern system to get over cpu starvation. Computers ar eknown to be able to cope with that and make priorities and cap cpu usage. I'm not sure it's the case for GPU. For the GPU case, if there is the same way to be able to share or reserve only part of the gpu? Or limit it? If those capabilities are in the systems or not? A few years ago I tried to do something with the GPU and I drove it to halt because there was no way to recover from that. In CPU, it's trivial to do so. Maybe things evolved.

Matthew: I wonder if WebGPU has anything to teach us. We probably has to decide what the TAG things about whether we should try and mitigate against this type of failure mode in future apis - status quo is yeah you can slow things down and break them and it's just the way it is. Maybe as a group we would probably form consensus about how important this is for us to address. Plenary?

Amy: "leave the web better than you found it"

Dan: there's stuff in the [webgpu spec about denial of service](https://www.w3.org/TR/webgpu/#security-dos). They're talking about system requirements of implementations

Matthew: did the WebNN people move to focus on just WebGPU for this spec? Previously supporting GL but decided to drop it? If they are GPU focused that's a possible avenue for mitigation. (Update: [they resolved to drop WebGL interop](https://github.com/webmachinelearning/webnn/issues/268))

Dan: do they delegate to the webgpu spec? We should talk about it in the plenary, and write some feedback now.

<blockquote>

Hi @RafaelCintron - thanks for this detailed response. We're just discussing in our TAG breakout today. Can we just clarify 2 points: 
  
1. You say "Chromium on Windows" but does this equally apply to other platforms - particularly mobile platforms? Is there implementation guidance pertaining to this in the spec?
  
2. We agree that the performance issues we've highlighted may equally apply to other web technologies such as WebGL as you've pointed out. Since we're building a new technology into the web, we have an opportunity to do something to improve the status quo. The WebGPU spec contains specific language in reference to [denial of service attacks](https://www.w3.org/TR/webgpu/#security-dos) which seems related to our concerns. Would it be appropriate for WebNN spec to contain similar platform requirements, or at least point to this part of the WebGPU spec?
  
</blockquote>

### [New SOLID Charter](https://github.com/w3c/strategy/issues/377)

Amy: I read it and it seems fine - not oriented around SOLID as a solution - they have renamed - they've clarified which things are input docs .. other clarifications...

Yves: a solid improvement.

...

Matthew: going from one to two input documents admits the possibility of others

Yves: yes, it's open ended. Says they will consider other inputs in addition

Dan: let's re-review at the plenary - let's try to issue a response from TAG. 


### Ethical Web Principles

Dan: mnot opened two more issues

Yves: we just need to label with status of issues

Dan: #19 - agreed to back burner this?

Amy: yes

#68 - agreed back back burner

Dan: #71 rights and responsibilities - captured in privacy principles?

Amy: back burner?

Matthew: +1

Amy: we should back burner all issues that are about new principles. These are not blocking to publication. Only things thare about a fundamental issue with a principle are blocking.

Yves: change back burner to `next version` ?

Dan: *does so*

Dan: #109 out of scope? Close this? Not that I don't agree with it, just not for EWP.

Amy: +1

Amy: PR #122 consistent headings - just want this to be consistent, was overlooked before

Dan: agree to land this. I remember wordsmithing this a lot though, did we exclude it on purpose?

Amy: I thought I just missed it. Please please please can they be consistent.

Matthew: +1. It does stick out.

Yves: does this need to be re reviewed?

Dan: no it's editorial

#121 section titles..

Amy: we haven't aligned them in the direction mnot and robin want. I don't feel strongly. But not a change for now.

Dan: I don't agree with what they're saying, that they should be normative. These are guiding principles not normative statements you can test against. These are not testable.

Amy: agree they're not testable, and can't see how they can possibly be enforceable. A lot of the discussion is about the knock on effects of things and it's hypothetical

Dan: we don't talk about contravening ethical web principles in reviews usually. Use design principles, which are informed by EWP. I'm always saying these are not actionable statements. I'll write something.

Amy: what we need to know right now is if this issue would cause mark and robin to object to publication of the statement, or if we can continue this discussion beyond publication

Dan: [*leaves comment*](https://github.com/w3ctag/ethical-web-principles/issues/121#issuecomment-2157932840)


### Issue triage

  
## Breakout C

Present: Martin, Peter, Tess

Regrets: Lea

### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

### [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon

### [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober

Propose close ("thanks for flying TAG"), to be confimed at plenary

### [Requesting review of HTML Ruby Markup Extensions](https://github.com/w3ctag/design-reviews/issues/959) - @hober, @LeaVerou

Propose close ("thanks for flying TAG"), to be confimed by Lea

### [improvements to \<details\> styling (widget structure)](https://github.com/w3ctag/design-reviews/issues/965) - @hober, @LeaVerou, @matatk

Propose close ("thanks for flying TAG"), to be confimed by Lea

## Breakout E

Present: Matthew, Dan, Martin, Yves, Max
Guests: Simone (W3C), Anssi (Intel), Michiel, Wei (Intel)

Regrets:

### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion + Guests

Anssi: this is a WICG - but it's built on top of the openscreen protocol...

Michiel: implementation

Wei: implementing open screen library

Anssi: *presents [slides](https://docs.google.com/presentation/d/1YFNUpUQxgtWUzJOFcqIWzSgjJiG1kcWP1GUD-XafA6g/edit#slide=id.g2bb12bc23cb_0_140)*

Anssi: new WICG incubation ... prototyping activity going on in Chromium ... also a Go library by Michiel. This became the 2nd most discussed API in WICG... Most was positive feedback. There seems to be developer demand and user demand. We are trying to accomplish an off-line first version of peer-to-peer focusing on LAN use cases... connect securely over a local communication medium without the server in the middle.  We want to serve the needs of the user first.  The user is in control - through the user agent. We expose only the minimum functionality to get the job done. Local network currently not a first class citizen of the web... easier for the browser to trust a server far away than trust a device you have in your local network...  coined *local communication medium*. Discovery, request, connect to peers, send and receive data, enable secure https connections...  We've looked at https for local domains and incorporated... We want to build an open tech .. 

Martin: What is your security [story]? 

Michiel: from a high level .. how the 2nd screen protocol .. advertising pees over mdns... then establishing trust ... using a PIN code that you enter to connect to a device you're expecting to connect to... that creates trust. Each peer creates a self-signed cert.  Now the relationship between these 2 peers - they trust because of the handshake - then use that cryptographuc material to do bi-directional communications - then use those certs as trust anchor to do PKI for the local network.. because devices trust eachother use that to start securing services... it's all based on the 2nd screen protocl. described independent on what network you're using but initial imlementation is on local area network...

Martin: a bunch of question s... what's the origin you're talking to? this sits on top of certs. you need to opaque bind to the TLS connection... Sounds like it requires a lot of analysis. Are you asusming that the person has physical access? 

Michiel: we're replicating the same user experience [from chromecast]

Martin: there is a person sitting in front of a screen attached to both devices... that can show something... similar to bluetooth pairing codes but none of that is clear in the description.

Anssi: *use cases* off-line collaboration - tools working without internet connectivity... illustrated as a version of google docs that works offline across peers; sending and receiving files instantly; export to "nearby" devices - from a web application - you don't need to go to the cloud and back; video editing also becoming a thing on the web <- we got feedback from users; Use your mobile phone as a game controller; disaster relief - feedback from people who work in this area that there is a need for ad-hock web-based tools that work offline. Home services, IoT, attached storage... 

Michiel: use case for baby monitors at home...

Dan: *abuse scenarios, e.g. abusive partner mis-using?*

Anssi: contrasting with WebRTC we expose the friendly name.. don't provide programmitic API...

Michiel: that's a tricky one... from a tech pov it's hard to provide an answer...  doesn't create a new attack surface that doesn't exist...

Anssi: please feel free to open issues in our repo...

Simone: Considerations like the one from Dan - one level is trust between peers... Peer to peer devices can be misused... inside a network you can use these to [inject] malware... How to avoid that I have an device with me that gives my position... how to avoid... giving info with privacy.  Also with openscreen protocol ... this could be used to fingerprint the network... 

Anssi: we could document these attack vectors... and figure out how they're currently mitigated... Please open issues in our github repo... 

Dan: *abuse scenarios*

Michiel: yes we do want to do this - we have done a lot of work here e.g. fingerprinting... noe of the discovery information is leaked to the browser without user consent... I think we can step up our game... 

Anssi: we've learned from WebRTC so we can do better...

Martin: needs more detail in the spec ... or explainer ... 

Michiel: implementation on top of OpenScreen protocol...  What we're showing is what's happening at the protocol level - during the discovery phase we involve the user agent ... not exposed to the JavaScript realm...  Could be similar to the Matter protocol where the key is something on the device itself (a sticker).  Protocol negotiates which is the displaying party and which is the entering party... Uses mdns, ... they (openscreen) has a network of trusted devices on your network...  We're doing bi-directional communication - taking inspiration from RTCDataChannel... also exploarion on how we get closer to WebRTC... If we do TLS between these peers then you could create a chain of trust for certs for these web services... Mitigate agains the browser saying "this is unsafe" when you're connecting to a device next to you.

Yves: WebTransport is _not_ p2p, per charter

Michiel: we're looking a P2P version of webtransport ....

Martin: suitability of things like webRTC... there was a deliberate choice of making  webrtc and web transport different. Quic is an evolution of what we'learned in sctp... There is work in IETF to evolve... I would encourage dropping WebRTC and concentrate on webTransport... client-server roles... then we have a basis in the origin model and thinking how this fits with existing things...  One of the nice things about webtransport - once you have negotiated a connection, the API is symetric...

Anssi: *comparisin between WebRTC and Local Peer-to-Peer.* 

Michiel: we are leaning more in this direction... we would prefer to use Quic and web transport API - there needs to be some canonical library...

Martin: a few things that can't be shimmed on the top... 

Martin: that is my opinion... 

Michiel: interesting to ... be able to assign peers a clear role...

Martin: webrtc works with a signalling arrangement... an offer and an answer... one peer becomes a server and one becomes a client... here you have a clearer scenario... there's a thing sitting in the network disovered using mdns... then the browser discovers it and acts as a client... Now what you're doing is looking up a special name... most APIs won't care... they're just names - some of them end in `.local` then you're establishing a webtransport connection to that name...

Michiel: effectively all those pieces are in place... we need to figure out how to define that more properly... 

Martin: need more detail in the spec...  There's a lot of useful work on building frameworks... in IETF .. had this not already been put on the rec track... i would have advocated doing the protocl in the ietf and the API work in W3C... We're doing that in web transport... that's worked out very well... That adds rigour. 

Anssi: we did consider that... the rationale was that the openscreen protocol people were in the working group... also particiapted by people who are in IETF... it was raised but not easy decision...  It's not always smooth sailing to split work like that ... e.g. web sockets.

Martin: i think stuff after websockets has worked better.

Matthew: bootstrapping process. devices with screens... my initial thoughts was this about higher level devices... but if some devices are like a mouse that doesn't have input or output... we need to think about the bootstrapping process - in web-of-things you can get into issues with accessibility... e.g. a device where you have to press a button to reset which is inaccessible.... Just to keep in mind.

Martin: this is a fundamentally new capability ... there is some advice that a11y group can give... it would be great to signal this is coming and get people thinking about it...

## Plenary Session

Present: Dan, Tess, Matthew, Peter, Martin

Regrets: 


### Breakout Rollup

#### Ethical Web Principles

* [we discuss PR 124](https://github.com/w3ctag/ethical-web-principles/pull/124)

Dan: I feel this weakens it ...

Tess: I also feel this weakens it - "there is one web" is a stronger statement

Martin: I tend to agree on a stronger, clearer moderate statement as a statement of principles.

Matthew: I can sympathise that it needs to be imperative - counterpoint is that people might think "the web is already this so I'd better do this" ... I think 124 adds unncessary content to the titles...

* [we discuss 123](https://github.com/w3ctag/ethical-web-principles/pull/123) 

Martin: Robin has taken phrases like "we will aspire to" and change it to "we will do" - sometimes the fudge is hiding a fundamental tention - e.g. "we will mitigage or prevent harms" - this is sort of one of these difficult problems. Every change we make to the web will harm some number of people...  The hedging was trying to capture the fact that there is this push and pull - we will look at the changes we make, understand the consequences, mitigate the changes and mitigage the harms... 

Dan: thee's a lot loaded into the "try"

Martin: we keep coming back to the priority of constituencies...

Peter: on the other hand if we have the weasel wording then it's easy to say "we're going to try but not very hard" - but if we reduce the weasel words everywhere except where we know there will be tension - then we raise that point as something that has more wiggle room.. I wonder if we would better serverd by "we will do xxx" "we will do yyy" but have a footnote.

Martin: I think it would be better if we confront the weaseling straight on... As I tried to do in [PR 126](https://github.com/w3ctag/ethical-web-principles/pull/126). 

Peter: I do think this has implications outside the consortium - so it's good to not use spec-ese.  We need to be clear who we are writing this document for - so we can help shape PRs and edits...  Policy makers, etc... are an audience for the doc...

#### Breakout A

##### WebNN 

Matthew: Sangwhan's concerns were that a large model that's running on the GPU would cause performance bottlenecks. we asked them about it but the answer seemed to only apply to chromium on windows... and also a general "well if you tax it too much it's gonna slow down" but other technologies have mitigations - can we try to avoid this type of problem in future... So Dan asked them about a WebGPU spec mitigation... 

Dan: so they [got back to us](https://github.com/w3ctag/design-reviews/issues/933#issuecomment-2159340815)... 

Tess: webnnn .. not designed for running on a dedicated neural processor...

Peter: that seems problematic... it shouldn't be dependent on dedicated neural hardware... why bog down your GPU if you don't have a dedicated neural processor?

Martin: doesn't work for apple's thing?

Tess: we didn't do webgpu right away... we waited until the processors were mature enough... so it would be deployable... does that mean that webgpu is "late"? maybe? but I feel this is too much too fast... 

Martin: it seems like we have 2 solid options for people doing this - you can use WASM to use the CPU. You can also use WebGPU because the GPU allows you to do these things. Are we ready for the next step?  It may be the case that we can find a higher level abstraction that works across more of the hardware... which would give us the stop-gap. If you want to do face detection and you have a neural process or then you can save a ton of energy by using a specialized API.

Peter: maybe it's better to havea few high level APIs for the key use cases...

Dan: suggest we bring in Dom to have a chat with us in a future call...

##### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon 
* [explainer has updated](https://github.com/WICG/manifest-incubations/blob/gh-pages/scope_extensions-explainer.md)
 
#### Breakout C

#### Breakout E (peer-to-peer)

Martin: overall impression is that the folks involved are attempting to do protocol work - and solving a hard problem - how do you talk to things near you - leans heavily on things like webUSB and web bluetooth - deflecting all the security risk on end users... because it's unclear ... 

Martin: the e.g. printer would signal that it supports this new protocol...  - also screen casting... presentation APi and you project as a second screen. They're looking to do generic networking capabilities ... building on the same protocol... 

Matthew: Martin gave some examples in that call where IETF and W3C have collaborated -- is that a general direction of travel in this kind of work?  Could we help encourage this...

Martin: institutional decision that W3C needs to make - when we start talking about protocols in general (and particularly those with security implications) is that work that should happen in IETF. Anssi brought up the topic of websockets which I agree didn't go well. However there may have been a culture clash there... 

Matthew: could we mention this at the AB / BoD meeting?

Martin: there are now two examples of where W3C does to do protcol-y things .. e.g. SOLID trying to profile HTTP... there is a relatively straightforward fix...

Peter: ... what is the solution for ... https / tls ... 

Martin: there is no webPKI ... fundamentally they don't plan to have https origins... but thats nebulous... 

Peter: explainer is talking about mtls...

Martin: they're talking about using password-mediated key exchange.... They are modeling after chromecast - you connect to your chromecast and it generates a code and then you type that code in...

Peter: establish a secure connection and post-facto verifying it...

### Issue Triage

### Plenary

Martin: move to 4 breakouts and a plenary...?

*we agree to take this to chat*
