## TAG Teleconference
##### 12 June 2019

Present: Peter, Kenneth, Lukasz, David, Tess, Alice, Dan, Hadley, Yves

Regrets: Sangwhan

---

Agenda:

* [Content Indexing](https://github.com/w3ctag/design-reviews/issues/379) - @torgo, @kenchris
* [Top-level await](https://github.com/w3ctag/design-reviews/issues/376) - @kenchris
* [Alternative Text for CSS Generated Content](https://github.com/w3ctag/design-reviews/issues/351) - @alice
* [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @cynthia, @alice
* [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @slightlyoff, @dbaron, @kenchris, @travisleithead
* [HTML Modules](https://github.com/w3ctag/design-reviews/issues/334) - @cynthia, @kenchris
* [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @travisleithead, @plinss
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice
* [EME Extension: HDCP Policy Check](https://github.com/w3ctag/design-reviews/issues/323) - @hober, @cynthia
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [HTML General Review: HTML Focus](https://github.com/w3ctag/design-reviews/issues/257) - @cynthia, @alice, @slightlyoff, @dbaron, @travisleithead
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) - @cynthia, @plinss
* [``<link> rel="modulepreload"``](https://github.com/w3ctag/design-reviews/issues/213) - @hober, @cynthia, @dbaron
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @alice, @torgo, @ylafon
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @hadleybeeman, @plinss
* [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) - @dbaron
* ["With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76) - @slightlyoff, @dbaron, @ylafon

* scheduling any secondary discussions to be used during alternate call-times
* resolving what we want to do with the calendar
---

### [Content Indexing](https://github.com/w3ctag/design-reviews/issues/379) - @torgo, @kenchris

Ken: this is really early - the idea is e.g. on android you have google assistant, and native apps can give this info to the assistant and they can act on it. This is so PWAs can give data to the index.

Alice: a loose API - adding an object to the service worker registration.

Dan: lgtm

Ken: should it only be tied to service worker?

Dan: can we close this one off for now?

Alice: they did note in their alternatives considered that they considered extending the cache interface.  I was confused as to what is going to be consuming it. It wasn't clear from the explainer.

Peter: that was my wonder as well - there was a mention of android slices - but what would...

Dan: 

Peter: 

Alice: they asked us to open issues in their repo. Also: it has a needs spec comment. that could have 2 possible interpretations- we should maybe have 2 labels.

[Meta discussion on labels]

### [Top-level await](https://github.com/w3ctag/design-reviews/issues/376) - @kenchris

Ken: this is a tc39 spec - about to be implemented in v8. They've been good at following up on the comments we made. Only big comment i had - now when importing something it can be async without you knowing. .. They have considered the feedback - i think we can close this.

[consensus to close]

### [Alternative Text for CSS Generated Content](https://github.com/w3ctag/design-reviews/issues/351) - @alice

Alice: last thing was - comment from Amelia - some questions from Sangwhan about alternatives considered.  There was a proposal early on about wrapping the string in an alt function which would make the purpose more obvious. Amelia pointed out that it's noop function which is weird. And came back to this issue - which risks content and alt getting out of sync... I asked Sangwhan if he'd be OK closing it, he said OK. 

Peter: we're ready to close this.

Dan: Sangwhan should close it because he's been active on the issue [and alice has a conflict of interest]

### [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @cynthia, @alice

Alice: my feedback was asking for an explainer.  My opnion is that the API looks fine - it's adding this pointerrawupdate event which is a spammy event - finegrained events on that. spec has comments like "don't handle this unless you have fast code handling it" - the getpredictedevents API is copying some platform ... I asked a question about why the browser needs to do this. Sangwhan pointed out that if the browser is doing it it happens off the main thread...   Anne also had points about shadow dom.

David: Anne was considered that the spec was not formal enough to show it does the right thing in terms of shadow dom and that it would need to get moved into the relevant spec - pointer events and mouse events.

Hadley: I am finding it hard to engage with finding that it jumps into "how it works" and there is no explainer. 

[many ideas of what it could be used for]

David: i've seen discussion - some of it comes down to a browser diffeence - some browsers get the mouse events from the OS and fire them through to the web app. what chrome does is it fires a mouse move per vsync cycle. That's probably a better model - but if you are doing a drawing application you actually want the set of coalesced mouse positions from the whole movement. So if you care about the path, you can get them.

Ken: also for gesture recognition.

Alice: and if you're a game... also some of this info is in the intro - but the text is hard to engage with.

Hadley: this issue made me realize that our trmplate does say "explainer/requirements doc/example code" ...

David: we did change that to explainer (containing user needs and example code)

Alice: in terms of this issue - the spec quality issues may be out of our remit... 

Tess: that's the case of a lot of things that come our way...

Alice: i'm not saying we don't do the review...

Hadley: i think editorial is out of scope but if it's difficult to review it should be in scope.

Alice: it took more work  - my vote would be to say "i think the API looks fine" - would give feedback that the spec was hard to read and we asked for an explainer but you didn't provide. the spec could be made clearer and provide some example code. The API looks fine though.

Lukasz: the spec has no security & privacy considerations - I'm worried that this would be giving versatile info about the pointer movement - and this ability to track mouse movements without any prompts - there are a lot of research works indicating some possibilities of user tracking based on mouse movements - i'm wondering whether this provides something not provided by old-style API.  Should we ask them to fill in the security & privacy questionnaire.  

Ken: i think it's fine - if people start using this for tracking this would slow down the whole browser so it could be a performance issue. Maybe there should be a prompt.

[discussion on performance-related issues - slowing down the browser]

Ken: can you write some of these comemnts, lukasz?

Lukasz: how often would the event fire?

Alice: (as david said) it's only chrome thay actually does this coalescing...  

David: firefox does not, i'm not sure about pointer events....

Lukasz: i still feel there is a problem with old-style mouse tracking... 

Alice: I'm not sure what the privacy issues are ...

Ken: I think it makes sense to ask them to cosndier...

Alice: they did fill in the s&p review - all "no" -

Ken: we could ask the question thay lukasz gave...

Dan: I don't think a "no no no" answer to S&P is appropriate considering the fine-grained info theu are making available.

Hadley: If we are looking at expanding the fingerprinting surface area, we should ask them to consider it themselves, and to put it in the spec so that implementers can take mitigating actions if they want. 

Alice: Lukasz, can you file an issue on their repo?

Lukasz: OK, I will.

Alice: i will write a comemnt on the review talking about the spec quality - needs to be clearer.

Peter: also anne's comments about how if the raw/coalesced events would interact with shadow dom.

[meta-discussion on secondary call times]

