## TAG Teleconference
##### 24 April 2019

Present: Tess, Kenneth, Dan, Peter, David, Sangwhan, Hadley

Regrets: Alice, Yves

---

Agenda:

* [Gamepad Light Indicator extension API](https://github.com/w3ctag/design-reviews/issues/362) - @cynthia
* [Additional reading methods on Blob and File](https://github.com/w3ctag/design-reviews/issues/359) - @cynthia, @kenchris
* [LazyLoad (loading= attribute)](https://github.com/w3ctag/design-reviews/issues/361) - @hober, @cynthia
* [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris
* [Web of Things (WoT) Thing Description](https://github.com/w3ctag/design-reviews/issues/357) - @torgo
* [Autoplay Detection API](https://github.com/w3ctag/design-reviews/issues/356) - @hober, @hadleybeeman
* [Web of Things (WoT) Architecture](https://github.com/w3ctag/design-reviews/issues/355) - @torgo
* [Design questions for Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/354) - @torgo, @hadleybeeman
* [Backdrop Filter](https://github.com/w3ctag/design-reviews/issues/353) - @hober
* [TAG review of whether element.pseudo(":unknown") should return null or throw](https://github.com/w3ctag/design-reviews/issues/348) - @hober, @alice, @dbaron
* [User Activation Delegation through postMessages](https://github.com/w3ctag/design-reviews/issues/347) - @hober, @alice, @plinss
* [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @alice
* [Audiobooks](https://github.com/w3ctag/design-reviews/issues/345) - @hober, @cynthia, @dbaron
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman
* [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff, @dbaron

---

### [Gamepad Light Indicator extension API](https://github.com/w3ctag/design-reviews/issues/362) - @cynthia

Sangwhan: modern gamepads: you can control the lights through USB HID - make the lights pink for example. It's behind a permission... the gamepad API itself the button order is different across different implementations - and now repeating the same thing with lights. Other issue I have : doesn't require permission and I don't think it'e easy to add permissions. If you have RGB lights you can do intra-origin communication - you can treat it as a 3-byte wide memory - e.g. tracking IDs... 

Kenneth: what tis the use case for reading these?

Sangwhan: I don't know why you would want to...  one case you would want to - you ahve a gamepad and you lose battery and you want to be able to check the light status - continuity.

Kenneth: could you "just allow read once"

Sangwhan: I am not sure.  Don't know enough about the use cases of the RGB lights. Not in the explainer.  I have provided feedback. It's pending external feedback - about the communicaiton thing. 

Peter: I don't see where you can actually read the colors in the spec.

Sangwhan: I'm pretty sure I saw it when I was reviewing...  Will double-check...  My bigger concern is around interop / consistency.

Peter: you'd have to know what game pad you're dealing with. Specs should provide guidance on that.

Kenneth: as far as I can see you can't read back.

[looking for the explainer]

[set for f2f]

Hadley: it would be nice to have more concrete use cases.


### [Additional reading methods on Blob and File](https://github.com/w3ctag/design-reviews/issues/359) - @cynthia, @kenchris

Sangwhan: a helper function - non-controversial. This is just a helper that makes it easier to read and write files - write slightly more idiomatic code.  No issues with this.

Kenneth: me neither.

Peter: Seems reasonable to me.

David: Based on experience using Blob, it seems like a good thing, even if I haven't looked at exactly what it's adding.

Sangwhan: we can probably close this one.

Peter: let's close it.

### [LazyLoad (loading= attribute)](https://github.com/w3ctag/design-reviews/issues/361) - @hober, @cynthia

Tess: suggest pushing this out - there is active discussion - good feedback - would rather review when it settles out

Peter: didn't chrome ship this?

Sangwhan: presto had this as a non-standard feature.

Peter: "Opera did it first" [meme]

Tess: it's been quite active - maybe pushing it a week would be the right amount of time.

Peter: let's push it a week.

### [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

Kenneth: additional permission prompts?

Sangwhan: don't think that's a good user experience.

Peter: happy-ish with the feedback to my comment.

Sangwhan: from an implementation perspective - if you want to have it separately then - underlying native api had to hold on to same object...

Peter: David did they address the comment about the prompt?

David: I haven't dug into the spec to know what that means.

Dan: fold two prompts into one?

Sangwhan: how?

Peter: you get one prompt when you invoke getusermedia. Theoretically you could get one prompt that asks for video feed and pan/tilt... then habe to re-apply constraints.

Kenneth: you will see what they are looking at.

Dan: yes if there is self-view.

Hadley: it feels weird to me - violating expectations and confusing users.

Sangwhan: I haven't seen other examples. Personally I think it's something that could be patched in later.

Kenneth: i think it's ok to have a notifciation "remote user is trying to move your camera" 

Kenneth: professional google hangouts does that, right.  Some will use machine learning to focus on who is speaking, for example...

Sangwhan: there are restrictions from blocking other party from messing with your camera.

Dan: blah blah blah ethical web

Sangwhan: permissions in the web are pretty bad. If we had a non-broken permissions.  I'm OK with this shipping then we can add a permission later.

Dan: i think we should be challenging them to come back with a solution that addresses these concerns..  

Hadley: i second.

Dan: this

Hadley: i'm conscious of how often you joke about when you take video calls what is off camera. I worry about violating that at a platform level - that doesn't fit with the user being in control of their experience of the web.

Peter: i agree with that but there are valid uses for remtoe control.  I can imagine a camera that flips back and forth between front and rear facing - but that'd be a different API.

Kenenth: on new phones you have "selfie lens"... like wider angle  view.

Peter: i beliebe there's a zoom feature here already 

Sangwhan: there is.

Dan: isn't it desirable that we should be asking the developer to ask multiple permissions?

David: the UA might be able to bundle or could split them out but only if the API is 

Hadley: I'm comfortable leaving that to the user agent.

David: In order to leave the choice of whether to bundle the permissions to the user agent, the user agent would need all the information at the time it's asking the user for the first permission.

Sangwhan: that makes sense.  The feedback we would liek to bring back is that we'd like it o be a secondary permission but so you can ask for that permission in a bundled way.

David: assuming there's a reasonable way to do it.

Peter: when you call getusermedia you pass in a set of constraints that you're asking for - you try to set pan/tilt constraints then you could bundle it in one prompt.

David: that's even the sort of thing that could be patched later but it might be good to get it up front.

### [Autoplay Detection API](https://github.com/w3ctag/design-reviews/issues/356) - @hober, @hadleybeeman

Hadley: I looked at this - i'm suspicious of anything that surfaces info about the user's preferences. It's an API to expose whether video will autoplay in the user's browser. One thing I would like to see is what it does to the fingerpinting surface. Could be a copy-paste from intersection observer and the like....

Tess: It's a little hard to follow from the design review issue filed.  There is a fundamental disagreement on the shape of the API. There was a f2f in NY in March where we discussed this.  The gekko and webkit media folk would strongly prefer it to be a syncronous propery lookup. The blink engineers want it to be promise based. 

...There's reasonable arguments to be had here. Autoplay is a weird area - different enginess have different policies, applied differently. Architecture in Blink involves XPC.  If they have to prefetch this at page load time then it hurts page performance. Both gekko and webkit policies work differently from that. no consensus in the room whether it should be sync or async. 

...Raising this to the TAG was maybe intended to both be a simple design review and partially invoking TAG as an esclation path.  I think there are 2 relevant html design principles. One is priority of constituencies - improving experience for users comes first before browser enginers. Second is avoiding needless complexity. Since two independent implementations prefer the simpler API, this feels needlessly complex.  We should prefer the simpler API.

David: are there other APIs that synchronously need this information? Like play APIs where you can detect if it works?

Tess: yes.

Sangwhan: you get a promise.

Tess: this is trying to add convenience on what you can already do.

David: if some browsers have this per element this is n issue if the API is per document.

Tess: the API is both. Programatically detect behaviour under different implementations. You do need document and element level. One architecture issue is that you shouldn't have this divergence to begin with.

Sangwhan: i did look into this - i couldn't get to the bottom of how autoplay is actually implemented. i could not figure it out.

Hadley: yeah i went digging into that too.

Sangwhan: i looked at both sides of the argument - property vs. async - it feels more ergonomic to have it as a property - as someone who might use it as a web application. 

Peter: one argument in favour of a promise base... []... but one argument is this can change so you might want an event.

Tess: one option considered in march is an object could receive an event. It ended up being the most complicated.  So it's worth saying that the underlying implementation issue (XPC in Chrome, and that loading it is expensive): in webkit I think we do XPC at pageload time for a variety of reasons already. So i don't think "we do xpc here" justifies the complexity. 

Peter: i agree it shouldn't be async just because it's more convenient for browser engines.

Tess: i think it's unfortunate that autoplay policies differ so widely, but also it's an area of innovation where browsers compete to better serve users

Hadley: +1 for the curmugeon's view. Autoplay never meets my user needs.

Peter: we'd rather see one single mechanism...  Also: the API shape is weird to me on the media element, just returning a boolean.

Sangwhan: what we have been asked to review is just the chrome proposal. More browsers seem to want the other one.  That part is not clear from the request that they sent us.

[some discussion about the quality of the issue and whether it accurately captured the discussion]

Dan: where was the alternative (sync) version documented?

https://github.com/WICG/autoplay/issues/7
https://github.com/WICG/autoplay/pull/8

Hadley: We definitely should steer clear of criticising individuals.  But yes, if this is an indication of any one group having an undue influence on the web, like Google having an outsized influence on WICG's activities, then I think we should discuss it. The whole reason we do standards is to bring everyone together and balance out different agendas with consensus. 

Tess: there is an issue procecurely we should consider in the TAG... it's unclear if this issue was raised as a dispure resolution vs. a design review request.

David: seems like the template needs an option.

Sangwhan: would it be fair to ask them to provide more info and be clear that maybe TAG could be a tie-breaker?

Tess: it also feels like ... suppose this was being done in a working group and this disagreement happened and everyone threw up their hands. It would be the role of the chairs of the wg to drive consensus. The WICG doesn't do that. It feels weird to come to the TAG [to play that role].  Feels like skipping a step.

Hadley: i think this is important - and one of the issues that comes up when we are hit with so many ideas from chormium that haven't gone through a working group process. then that becomes part of the web platform primarily because they got there first.

Peter: any quick wrap-up? Should we just push back. 

Dan: there does seem to be a preference for simplicity.

David: if we're gonna tell them to come back when they're ready. If there is a particular dispute they want us to adjudicate then they need to lay that out.

Hadley: pros/cons; i agree

Tess: i don't think it would work to say go away and come back with an agreement

Hadley: can we have a word with the WICG chairs?

Peter: we could invite the interested parties to the call?

Tess: it's a lot of people...












