## TAG Teleconference
##### 10 January 2018

Present: Travis, Sangwhan, David, Peter, Dan, Alex

Regrets:

---

Agenda:

* [Sensor APIs ](https://github.com/w3ctag/design-reviews/issues/207) - Sangwhan 
* [Web lifecycle](https://github.com/w3ctag/design-reviews/issues/205) - Travis
* [`saveData` attribute](https://github.com/w3ctag/design-reviews/issues/204) - Alex, Sangwhan
* [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David
* [General Storage Observer](https://github.com/w3ctag/design-reviews/issues/210) - Travis
* [Media auto-play as a permission](https://github.com/w3ctag/design-reviews/issues/203) - Alex, Dan, Hadley
* [Serialization of natural language in data formats](https://github.com/w3ctag/design-reviews/issues/178) - Sangwhan, David, Travis
* [&lt;link&gt; rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew
* [Files and Directory Entries API with webkit prefixes](https://github.com/w3ctag/design-reviews/issues/215) - Andrew
* [Web Locks API](https://github.com/w3ctag/design-reviews/issues/217) - Andrew

Followups:
* [import.meta.url, and import.meta generally ](https://github.com/w3ctag/design-reviews/issues/208) - Alex
* [`Accept-CH` header is weird](https://github.com/w3ctag/design-reviews/issues/206) - Andrew, Alex
* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - David, Alex

Triage:
* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) 
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) 
* [CSS Selectors 4](https://github.com/w3ctag/design-reviews/issues/219)
* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221)
* [Async Clipborad Text API](https://github.com/w3ctag/design-reviews/issues/222)
* [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223)

---

#### [Sensor APIs ](https://github.com/w3ctag/design-reviews/issues/207) - Sangwhan 

Sangwhan: design flaw - this belongs to navigator. this assumes that there is only one gyroscope on the given device - or one sensor.

Travis: that's true in 99% of cases

Sangwhan: it's true in mobile cases but not with gaming headset e.g.

Travis: but those would be exposed through e.g. webvr input controllers...

Sangwhan: but these accelerometers ... 
... also privacy issue which is a double-edged sword. if you reduce the amount of frequency you can sample it makes it's less useful for a lot of use cases... but at high frequency then you expose private info to the web. Where do we draw the line? The privacy concern is very valid and needs to be addressed but at the same time how do we make it useful where you do need high-frequency?

Travis: the high-frequency scenarios required permissions from the user.

Sanwhan: yes.  Martin Thompson raised an issue on fingerprinting related to existence ...

Alex: from a fingerprinting perspective - we want developers who do the right thing not to create supercookies... [I think this meets that test.]

Sangwhan: question for the first part: how do we expect other specs to be able to use these as components on controlers that may contain these things? Should I bring that up or let it slide?

David: example?

Sangwhan: gamepad for example... the compoents are not easily attachable because of the way the spec is defined - as it's attached to the window.

Travis: i think it's good insight. the 99% use cases for mobile devices, etc... that have one primary gyroscope will be sufficient for a lot fo cases but ... if it's a generic interface that could be applied to headmounted controllers, etc... that could be useful. It sounds nice, but practically speaking we tend to do discoverability on top of objects poorly in the web platform.

Sanwhan: can i bring this up as an issue.

[consensus yes]

Travis: yes

David: yes 

Sangwhan: even stuff like you start a game with one gamepad and then swich - that doesn't work well.

David: Some APIs that try to be general to multiple things tend to be awful, and people just make guesses/assumptions.

Travis: conversely we could way over-engineer it. (cite MediaStream camera selection ;-)

David: the other thing that can happen for taking care of new things the user plugged in is that the user agent takes care of it.  That can be different from the gamepad case where you expect sensors on the gamepad.

Sangwhan: yes I will do that - 

Alex: we should have concrete advice for them - e.g. use of promises

Sangwhan: I will bring that up.  Could do things like request a specific granularity/frequency, and the UA chooses whether to ask the user for consent based on that.

---

#### location of london meeting

Peter: Alex do we have details?

Alex: I am today sending in the request for st. Pancras. I will have confirmation by end of week.

Peter: also for Tokyo - April 5-7.

David: we should run it by Lukasz for travel availability.

[discussion on venue for space]

Sanghan: Keio... it would be no frills. I will talk to them.

---

#### [Web lifecycle](https://github.com/w3ctag/design-reviews/issues/205) - Travis

Travis: I intend to be brief.  I think this is amazing.  It describes the typical lifecycle of a web page and it introduces 2 new states that a web page can go into and associated signals. The 2 new states are "stopped" (memory resident but not getting time on CPU) and "discarded" (forcefully terminated, gone) - when you see the stop signal you will be allowed to run a callback to unload some resources or prepare. After you've been stopped you may be terminated without further notice.

Dan: possible use of this to subvert user action..

Alex: the design point is that a lot of browsers are silently doing tab discarding - e.g. chrome on android, safari on IoS. They will keep snapshots (pixels) but the contetn is gone. Meanwhile a lot of content does want to live in the background - they will keep a lot of tabs open. What makes sense on mobile makes less sens on desktop - where those tabs might still be visible. That's one motivating use case. it's not designed to handle pop-up or pop-under detection on unload.

Travis: it seems the focus of the lifecycle is where the agent makes the decision to terminate. If the user closes the tab that's out of scope. Preventing ransomware pop-ups is high priority. I think it's a valid concern.

[ dbaron's machine spontaneously reboots and he disappears for a minute or two ]<sup>Citation needed</sup>

Travis: will continue writing up feedback.

---

#### [`saveData` attribute](https://github.com/w3ctag/design-reviews/issues/204) - Alex, Sangwhan

Sanwghan: I had something about privacy I wanted to add in the review....

Alex: I am a fan and want to see it move foreward.

Sangwhan: I will drop the comments in github.  Can we revisit next week?

---

#### [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David

[no progress]

Peter: what milestone?

Alex: we owe them feedback  - ... readable streams, writable streams, implicit buffers, implicit copies... back pressure.  ... largely covered. have been though about anyway.  What I don't see is an explainer.   I will ask them for am explainer.

[ bumped 2 weeks ]

---

#### [General Storage Observer](https://github.com/w3ctag/design-reviews/issues/210) - Travis

Travis: this is a derivative of our last discussion on storage observer... we couldn't get cookies and local storage to fit in that box... is there something else we need? The next step on this issue... formally async cookies api renamed to cookie store API. I've seen the explainer...

[ link? ]

... in general this looks really good. It's a relatively simple model for having rights and reads on cookies that happen asynchronously. I just noticed that there's a cookie observer... 

Alex: there's a bunch of APIs... There is the notion of being able to listen for a cookie change... get an event for that. one of the scenarios we get with auth is that the auth tokens are held in cookies and apps have legal requirements to dump local serialized data when user logs out. detecting that requires this...

Travis: that looks only applicable to service worker... 

Alex: agreed that's a good question to have an answer to.

Travis: more reading to do here before we have a more complete picture...  more time.  bump 2 weeks.

Peter: OK

---

#### [...some discussion now on AMP with and packaging...]

Travis: web package format signed by example.com (creator origin) that could be delivered to a cache and a browser would be able to put it into exampe.com's origin.

Alex: yes

Travis: svg...

Alex: web components... it's foundational.

Dan: standards approach?

Alex: a lot of it happening at IETF... some pieces may end up at w3c. Jeff Yaskin is contact person.

---

#### AOB

Peter: any other business?

