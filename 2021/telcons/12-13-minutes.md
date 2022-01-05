# TAG Teleconference
#### 13-15 December 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-12-13](https://www.timeanddate.com/worldclock/converter.html?iso=20211213T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @LeaVerou, @atanassov
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov
* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov
* [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober
* f2f scheduling

### Breakout B (US / APAC) - [2021-12-14](https://www.timeanddate.com/worldclock/converter.html?iso=20211214T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

### Breakout C (APAC / Europe) - [2021-12-14](https://www.timeanddate.com/worldclock/converter.html?iso=20211214T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou

### Plenary Session - [2021-12-15](https://www.timeanddate.com/worldclock/converter.html?iso=20211215T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Year-End Social Time

-----


## Breakout A

Present: Dan, Peter, Ken, Amy, Hadley, Tess, Rossen

Regrets: Lea


### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @LeaVerou, @atanassov

Peter: last comment [from Tess](https://github.com/w3ctag/design-reviews/issues/521#issuecomment-963391874) asking for new direction... 

Tess: we've been waiting on them... should we ping again?

Rossen: I remember the discussion... at end of sept.  We took some resolutions in CSS wg... Linked from our issue #6674. Resolution 29 - adopt the new direction for declarative scroll linked animation. Since then I don't see evidence that that landed into the spec. Also the discussions I see here are not challenging that direction. From what I can tell folks are working on adopting that new direction and hopefully we can have an update here.  We should leave it for now.

Peter: **bumped to next year**

### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo

Dan: Some updates from September.. no update recently. Looks like there's work ongoing.

Rossen: we discussed UA client hints..

Dan: mozilla said it was harmful, authored by henri, so we got them on a call, sounded like some softening of mozilla's position but I haven't seen.. but good discussion between them. I don't know what has happened since then.

Ken: do they want to ship this in the next version?

Dan: mozilla has [changed their position](https://mozilla.github.io/standards-positions/#ua-client-hints) to be non-harmful

Ken: in the next version of chrome they have [something](https://chromestatus.com/feature/5703317813460992).. a subset that is going to ship?

Dan: I'll write a comment asking for more info.

Peter: concerns about proliferation of headers, and js versioning. Looks like they're working on it.

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Tess: when I last looked at this Lea and I needed to have some time to work on it. 

**will try to schedule a special session**

Peter: I'm not a fan but not sure there's a good answer either way.

### [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov

Tess: cool idea.. definitely some questions, need to read it to see if they're answered. What happens if you call showPicker on input type text?

Rossen: you might get suggestions...

Peter: input type password might activate your password managers. The hardest thing historically with datetime inptus was detecting whether the browser supports it properly

Tess: at least it's easy to feature detect if showPicker is there. Does it do something useful...

Peter: I can see browsers implementing it for certain types of inputs but not with a good widget

Ken: depends on platform as well, what is applicable

Tess: show if picker is applicable... *reading spec text* ... has a fallback... any relevent user interface.. if no UI applies, does nothing. 

Peter: my concern is I need to know whether it showed something or not. Maybe I have my own UI, but want to defer to the browser if the browser has one. Fair to give me a result that says I can't do this vs user hit escape

Ken: you don't want to show a button if it doesn't do anything

Tess: I don't think there's a way to detect that

Peter: feels problematic

Rossen: behaviour discoverability is important. If you're going to trigger a UI, successful or not, you need to know what actions to take, whether before you call the API or as a result of it. This is missing.

Peter: will leave comment

Rossen: alternatively they can start by restricting this to file picker. They will throw an exception if it's not supported. 

Peter: isn't there a situation where it may silently do nothing?

Tess: that's correct

Rossen: if the elements relevant global object does not have transient activation it will throw a not allowed error... but to the point of input type text.. can be used to suggest stuff to the user

Peter: I can't see picker cases for text.. there are other flavours of text input. I'll leave a comment.

Rossen: otherwise direction and general intent is good. This is needed. a step in the right direction.

### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov

Rossen: there's nothing easy about this issue. Deserves an entire breakout, at least one hour, between Tess and myself.

### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober

**...also bumped.**

### F2F Schdeduling

**We agree tentatively to hold next f2f in Edinburgh week of March 7th 2022**

## Breakout B

Present:

Regrets:


### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov

**closing**

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

## Breakout C

Present: Dan, Ken, Yves

Regrets: Amy

### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou

Ken: part of the display locking effort...

Ken: they said they'd update explainer but so fare not...

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/676#issuecomment-993326348)

### WebGPU Discussion

Ken: the explainer looks really good. 
