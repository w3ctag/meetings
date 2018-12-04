## TAG Teleconference
##### 04 December 2018

Present: Dan, Kenneth, Peter, Sangwhan, Yves, Alex

Regrets: David

---

Agenda:
* [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282)
@cynthia
@kenchris
@travisleithead

* [Background fetch](https://github.com/w3ctag/design-reviews/issues/279)
@slightlyoff
@kenchris
@travisleithead

* [HTML General Review: Web Sockets HTML](https://github.com/w3ctag/design-reviews/issues/268)
@slightlyoff
@ylafon

* [Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/235)
@slightlyoff
@dbaron

* [Should WebRTC be [SecureContext]](https://github.com/w3ctag/design-reviews/issues/228)

* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218)
@cynthia
@plinss

* [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213)
@slightlyoff

* [Serialization of natural language in data formats such as JSON](https://github.com/w3ctag/design-reviews/issues/178)
@cynthia
@dbaron
@travisleithead

* [Review Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134)
@torgo
@travisleithead

* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62)
@slightlyoff

---

### [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282)

Kenneth: Looking at issues around typing and TransformStreams.

Sangwhan: some people have issues with UTF-8 being the only encoding.

Yves: last telcon, we discussed the fact that natively js is ucs2 not utf8 - so the current name might be misleading

Kenneth: up-to-date example code?

Alex: no constructor so can't subclass?

Kenneth: domenic says you can

Alex: still an issue with subclassability - have followed up on the issue.

### [Should WebRTC be [SecureContext]](https://github.com/w3ctag/design-reviews/issues/228)

Sangwhan: This has been fixed on the wg side I have checked... "WebRTC is now secure"

### [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218)

Sangwhan: travis had something on the naming - 2 properties returned - smooth and power efficient  - frame rates- fractional nuumbers delivered as strings - they are reconsidering as 2 integers.

Alex: why not floats?

Sangwhan: they said floats dont cut it. but it's being reconsidered from strings.

Bumped to next week.

### [Background fetch](https://github.com/w3ctag/design-reviews/issues/279)

Kenneth: I am fine with this, Travis had a few comments, espacially about the name of downloadTotal.
Waiting on Travis before closing the issue.

### [HTML General Review: Web Sockets HTML](https://github.com/w3ctag/design-reviews/issues/268)

Will wait for Travis to send issues in the WhatWG spec, bumped to next week.

### [Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/235)

Alex: happy with that answer... 
Closing the issue.

### [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213)

Bumped for the 18th, need Travis' feedback.

### [Serialization of natural language in data formats such as JSON](https://github.com/w3ctag/design-reviews/issues/178)

Bumped to next week, waiting for @dbaron.

### [Review Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134)

Dan: It seems that we can close this and wait for next stage, waiting for Travis' input before doing so.

### [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62)

Dan: I will check the status of this with Mike West.

### MathML Position

Sangwhan: what's the group's position?

Alex: we've had a long running discomfort with MathML (in chromium). The rendering is underspecified. We would like to see that improved. 2nd - no explanation (primitives). We told people to wait for Houdini.  Math interest group want this. MatgML doesn't cover their needs. That has to be explained. Goal is to make sure that a clear bar is set to implement mathML. Then answer those questions.

Sangwhan: TAG's position?  My view is that this is a necessary feature but not in that form.

Kenneth: but it's there and implemented elsewhere.

Sangwhan: but it doesn't really work... Chromium doesn't support. Rendering is inconsistemt across browsers...      
  Not right to have a mode switch of layout There's a section of math community that wants primitives.

Dan: web components story - wasn't this supposed to become a web components library

Alex: math ig has asked for additional stuff that is not there in order to be able to make this happen. We are waiting on infrastructure.

Dan: is math a thing? yes. Does it need to be on the web? clearly, yes. Is mathml therefore the answer? not clear.

Alex: next steps: finding the group that can work on this.

Sangwhan: ergonomics and accessibility of mathml are not good.

Dan: numbumped to next week - let's try to have a more coherent discussion then and maybe bring it to the next f2f agenda.




