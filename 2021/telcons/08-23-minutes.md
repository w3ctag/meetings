# TAG Teleconference
#### 23 August 2021

---

## Agenda:

### Breakout C (APAC / Europe) - [2021-08-31](https://www.timeanddate.com/worldclock/converter.html?iso=20210831T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @kenchris
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @togro, @kenchris 
* [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss  

### Plenary Session - [2021-09-01](https://www.timeanddate.com/worldclock/converter.html?iso=20210901T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS tree-scoped at-rule names and references](https://github.com/w3ctag/design-reviews/issues/659) - @hober, @leaverou, torgo
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @leaverou, @atanassov 
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo 

* Breakout Rollup
* Issue Triage

-----

## Breakout C

Present: Dan, Ken, Amy, Yves

Regrets: Lea, Hadley

### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @kenchris

Ken: this makes sense. They're not going to remove polling so you can still poll if you want. Getting events seems reasobable.  One issue - button down or up - people are moving to a world where it depends how much the button is down, adaptive triggers - depends on how much or force feedback.  Should some thought be given on how to support this as well?

Dan: kind of out of scope for this propoosal... 

Ken: some considerations... a whole new API - or a buttonPressed event, buttonReleased event?

Yves: wouldn't it be better ... poll at regular intervals?

Ken: that's what they have today - it means if you're not good at polling enough then you lose event data.

Yves: if it's an analog value every small change in the pressure will release lots of different events. How do you filter? what is the granularity?

Dan: coalescing strategy for event mitigation

Ken: get coalesced events that returns the events combined

Yves: as multiple events?

Ken: you get one event that is the coalesced event, but you can get the original events

Yves: you can imagine you want the median value of ten different events that happen roughly at the same time?

Ken: that's what they give you by default. Some kind of medium.. join the events somehow. But then you can get the original events by calling getCoalescedEvents

Dan: the proposal is by google people. Scant information on additional support for this (e.g. in the ChromeStatus)

Yves: do they have specific events for accelerometers?

Ken: I don't know.. pretty sure they did something for VR

Yves: pretty sure accelerometers should be read every time because you want to know exactly what's going on

Ken: you don't want to coalesce accelerometers... draft doesn't seem to have anything on accelerometers

Dan: [writes comment](https://github.com/w3ctag/design-reviews/issues/662#issuecomment-904422451)

Ken: does the event have a timestamp? In the gamepad interface.. why does that have a timestamp? Not part of the... [leaves comments]

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @togro, @kenchris 

Dan: there's a [PR](https://github.com/immersive-web/raw-camera-access/pull/5) which addresses some of our feedback

Ken: do we already have camera access for web xr? What's different that makes it raw?

Dan: this provides more direct access to the camera pixels

Ken: texture, camera image.. are there different similar apis? They get an XR camera width and height, and getCameraImage which just gives you texture

Dan: you don't get that..

Ken: not much of a raw thing, more of a texture thing. Wondering whether people who work on media capture should look at this, whether they're doing liason with these people. An alternative camera api.. there's no configuration of the camera here. Cameras today we can do pan/tilt/zoom. Why is that not useful in this situation? Especially turning my head, maybe I want to do panning. What about configuring the camera? I don't want HD I want SD... doesn't seem like I can do any of these things with this API. Seems like a new API to do a specific use case, and it's an alternative, so all the existing API features are just gone. Half a year from now we'll get a new request to add new features instead of starting out with that. This is a paraellel API for a specific reason..

Dan: the current method of getting access to the camera, the website itself does not get access to the image of the user's environment. You get abstract concepts like being able to know where surfaces are, rather than actually seeing what the desk looks like. That works for many AR scenarios. But it doesn't work if you want to layer .. if you want to actually process the image, to provide a filtered version of it

Ken: i get it but it's still a different api that lacks a lot of features that i expect people would want

Dan: at the moment it's only AR concepts

Ken: only want SD stream, how do I select my camera? That's a basic thing. Just require camera access and you get this camera thing, but which camera is it? Is it HD, is it 4k? Seems to be a lot of things missing here. [leaves comment]

Dan: I'm still concerned about privacy. There's no additional scary privacy notice for raw camera access, so why wouldn't every AR request raw camera access, which destroys the mitigations of regular camera access. [leaves comment]

### [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss  

Dan: last comment from the requester.. saying there's been a lot of changes which address some of our issues [leaves comment]

Yves: will look next week

## Plenary Session

Present: Peter, Kenneth, Dan, Tess, Yves, Amy, Rossen

Regrets: Hadley, Lea, Sangwhan 

### [CSS tree-scoped at-rule names and references](https://github.com/w3ctag/design-reviews/issues/659) - @hober, @leaverou, torgo

Tess: my recollection - where it ended up - the purpose of the shadow dom is encapsulation - this design doesn't bring encapsulation. But intuitively matches.. ... it's what web developers who aren't familiar with programming languages expects - and what people familiar with lexically scoped languages expect. It's intuitive.  Some slight oddities.  But I'm happy with it.  I see in the Moz standards position thread therw was some discussion.  I can't say "great" before we get input from people familiar with implementation of CSS features and can look at it and say "this introduces a fundamental complexity" or something similar. I think the working group is getting this feedback.  The right people are engaged. From an authoring perspective i think it's great.

Rossen: I agree with Tess regarding the authoring excpectations.  It will enforce good practice.  From an implementation PoV, it feels like we have 2 opposing efforts - 1 to encapsulate for performance benefits - 2 (this) the reverse look-up problem: as you find things in such a subtree then you have to go back and find it.  Do we preemptively propogate properties and values down? That comes with some expense. Since it's "automatic" it will come at some cost for implementers and run-times.  It's not all great.

Dan: what should we do? Wait?

Tess: I would be comfortable closing it as long as we said "We'd like to encourage the wg to solicit implementation complexity feedback from folks familiar with CSS implementation in browsers."

[Closed with comment](https://github.com/w3ctag/design-reviews/issues/659#issuecomment-905639305).

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @leaverou, @atanassov 



### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo 

Dan: good discussion here.. I asked about UAs telling the truth more often.. [reads response]

Rossen: is your point that you want to reduce the amount of UA impersonation?

Dan: mike talks about a "hot mess" - what's that about? isn't it the lying? There's so much nonsense in the UA string

Tess: still going to be lying in the new stuff

Rossen: a lot of times we had to impersonate other UAs just so you can get the content. Sometimes you have to pretend you're a different version of yourself because there's content targeted to a version. Content matching is defintely something needed going forward

Dan: I'm wondering if the lying that happens now, the targeting towards specific user agents or versions, is encouraged by the current UA system we have and if there is this additional roundtrip required with client hints would it intrinsically discourage that approach? Would it make i tmore likely we'd see more adoption of feature detection and other things against this trend of ua sniffing?

Ken: some is for analytics

Rossen: if you took your example to the extreme and there are no ua strings at all, everything is done through client hints and feature discoverability, that is the utopia? That way you have various user agents with variosu capabilities and they get the content based on these capabilities. Today for better or worse a lot of these capabilities are discovered through the UA string. That is just yet another capability descriptor, on a macro level. From that point of view I don't think that ua hints add or remove any of the complexity about discoverability, referred to here as 'lying'. The question you probably want to asnwer is if we wanted to have this what is the path forward, is client hints the path forward, to ultimately drop ua string?

Dan: even the proposal on the table doesn't drop the ua string entirely, it simplifies ua string and puts stuff in client hints. To engage with the feedback, part of it was that there are things that are being put into t he clien thints which are additional entropy which are not really needed from a fingerprinting perspective add problems. that's a different issue. That's what's being discussed between henri and mike. I think mike has addressed the issue that I raised.

Rossen: good conversation after it

Dan: trying to figure out how best we can engage

Rossen: conversation is still alive. Maybe best path is to let it play out for longer?

Peter: was there a client hint about what level of js is supported?

Rossen: there could still be new client hints.. 

Peter: one of the primary use cases for client sniffing is js detection [leaves comment]

Dan: good point about that being one of the core reasons for ua sniffing. Also interesting from an analytics perspective. Important for a minority browser. If every browser masquerades it really doesn't help browser diversity

Tess: in the case of Tor it's a minority browser that really does want to look like every other.

Dan: when you're an effort working in a company and you need to justify the existance of that thing, it's important. Different from Tor. [leaves comment]

### [Process CG Issue](https://github.com/w3c/w3process/issues/465#issuecomment-898646568)

Peter: Process CG asking about increasing the size of the TAG.

[discussion on issue]

### Breakout Rollup

#### Breakout C

[dan sumnmarizes breakout c]

### Issue Triage
