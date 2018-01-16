## TAG Teleconference
##### 16 January 2018

Present: Dan, Yves, Lukasz, David, Peter, Andrew, Sangwhan, Hadley

Regrets:

---

Agenda:

* [London meeting](https://github.com/w3ctag/meetings/tree/gh-pages/2018/01-london) location?

dka: We have a location for the dev meetup at GDS, 1 Feb 2018.  After this call I'll put together the invite.  (Hadley: yeay!!)

dka: Did Alex confirm we have St Pancras location for all three days?
dbaron: Last I saw, it wasn't set.
slightlyoff: looks like we're at Belgrave House for the first day, St. Pancras for Thurs/Fri. Still trying to wrangle a room at St. Pancras for Weds. Will keep you updated.

---

* [Tokyo meeting](https://github.com/w3ctag/meetings/tree/gh-pages/2018/04-tokyo) dates/location?

Sangwhan: I talked to the Keio host. They are willing to host. Due to policy, meeting rooms can't be booked until Feb.  They'll then book for this — full day bookings are uncommon.  If they succeed, they'll come back to us.  Hopefully will provide lunch, which is good because there aren't restaurant alternatives. In the Meto Campus inside Tokyo.

dka: Sounds good

(discussion about hosts and food)

---

* [permission delegation](https://twitter.com/mikewest/status/952807134454009856) (and see [proposal](https://docs.google.com/document/d/1x5QejvpyQ71LPWhMLsaM1lWCfSsBsSQ8Dap9kJ6uLv0/edit)) do we need an issue on this?

Lukasz: I read the document. The plan is to make top level sites to ask permission. If the user grants it, all the iframes also have permission.  It would work with geolocation, for example. I think we might track it.  I'm not sure how advanced this proposal is.  You can imagine misuse: for example, if a website should be acting irresponsible.

dbaron: I think cross-origin subframes wouldn't inherit the subframes by default. If they needed it, they would have to be given that permission by the top level frame.  I'm not sure if that's changed?
Essentially, they are cutting off the ability for the subframe to aks for permissions. If we refuesed to give child frames permissions, people would write libraries to do that via postmessage or whatever else.

dka: Has this come out of the blue? I couldn't find a TAG issue or a work item in WebAppSec. Have they discussed it?

Sangwhan: From the explainer, it seems that Chrome considers this a UA-specific feature. Which is why they haven't stnadardised it.

dbaron: I'm supportive of that from a technical perspective.  But I almost asked.

dka: Risk? 

dbaron: now, subframes can ask for permissions. Which is confusing.

Hadley:  I worry about overly trusting the top level document when it may or may not - when the user may or may not expect what applies to the top level document to also apply to cross origin iframes... feels like opens door for confusion.

[some discussion on this issue here](https://docs.google.com/document/d/1x5QejvpyQ71LPWhMLsaM1lWCfSsBsSQ8Dap9kJ6uLv0/edit#heading=h.wkyy3sgn1dyl)

dka: Should we open an issue? We haven't been requested to, but I think there is a lot to discuss. 

dka: Lukasz, you seem to have some specific risk cases in mind?  Could you write them into that new issue?

Lukasz:  Code injection. If you're loading CNN.com and there is a malvertising campaign taking place, and you see that CNN wants to access your geolocation or microphone.  Some users may trust CNN, so would grant access — but it would a third party host.

Sangwhan: But if the malware happens on the top level frame, this is an issue anyway
...The iframe in this context is from the same origin.  It's likely that other parts of the origin are contaminated as well.

Lukasz: Yes.  Yes, but they are talking about third-party iframes, yes?

Sangwhan: iframes from the same origin. 

Lukasz: If this doesn't concern third party iframes, then it's not as big a deal.  But from the proposal, I thought it would delegate permissions to other origins.  Am I incorrect?

Sangwhan: Yes. If you look at the intent to implement...

Lukasz: Their example is from paymefast.com, which is loaded in an iframe.

Sangwhan: the Proposal document has a section called "Relationship to Feature policy"...

Lukasz: If it has to be specified by the website.  Specifically delegated perissions... that might be okay, assuming that there are no alternative misuses.  If the iframe contains something else and the permissions are being delegated transitively.  There is nothing here about that, yes?
...It would be good to establish if this proposal includes that. 

dka:  I suggest we open an issue in our repo to track this.  It should link through this convo.  I'll do that.  Lukasz, put your concerns into the comments and tag mikewest so that he can reply. 

Lukasz: Right

---

* [&lt;link&gt; rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew

Andrew: Initially, I didn't understand why it wasn't just an as, rather than a rel. We hwave rel=preload, and I thought this is a different kind of new preload as ad.

(was there discussion here about an as= attribute?)

...This kicks off a different algorithm under the hood which preloads the dependenceis. It's not a preload, it's a module preload.  We should discuss that.  Should it be surfaced to the developer? They probably don't care, but these authors thought it was important to refer to it in a different way.

...Put on the agenda for the f2f?

dka: Sure.

Andrew: Otherwise it seems sensible.  Not a lot to it; just a case of getting things loaded earlier, which makes sense. It's really just the syntax. 

dka: Okay, I'll put it in the f2f agenda. And will set a f2f milestone. 

Andrew: There has been some commentary where someone suggested calling it preloadModule.  

...Also worth mentioning: this was merged into HTML spec on 14 December. While our TAG review was opened on 7 November, we didn't give feedback before 14 December, so I suspect they probably aren't accepting any now. Chrome Status says it's shipped in 64, but it is behind a flag.  It will be in Stable by the f2f but should be still possible to make changes (assuming it hasn't been shipped by anyone else).

dka: Then let's timebox it at the f2f and address what we our options are. 

---

* [Files and Directory Entries API with webkit prefixes](https://github.com/w3ctag/design-reviews/issues/215) - Andrew

Andrew: We should come back to this next week. 

---

* [Media auto-play as a permission](https://github.com/w3ctag/design-reviews/issues/203) - Alex, Dan, Hadley

hadley: remember we talked about it in nice and there is a fundamental issue relating to the permissions API.

dka: Let's readdress/close it out at the f2f. 

---

* [Serialization of natural language in data formats](https://github.com/w3ctag/design-reviews/issues/178) - Sangwhan, David, Travis

Sangwhan: Nothing from the group, punt to next call or maybe 2 weeks down the road.
Dbaron: Sangwhan and I are waiting for I18N to come back to us with a written recommendation.

---

* [Web Locks API](https://github.com/w3ctag/design-reviews/issues/217) - Andrew

Andrew: In general I thought this was fine, but I have other considerations to include next week. 

---

* [`saveData` attribute](https://github.com/w3ctag/design-reviews/issues/204) - Alex, Sangwhan

Alex: This is related to Accept-CH (for client hints). 

Andrew:... which is a response header asking for requests. // me is breaking up here.. 
...Is it because you would include saveData in your Accept-CH?

Alex: yes

Andrew: We thought this was a little too much orchestration, unnecessary. And we should accept the value regardless.

Alex: Yes, I can't use this for the initial response as a result of this design. If I am a server and want to sened a different version of my page, conneg style, I can't understand that the user was looking for this behaviour until a subsequent request

Andrew: You can imagine a large difference between a normal version of a site and a saveData version.  CNNlite vs CNN for example.

Alex: Or worse... everyone always gets a redirect.

Yves: In the issue thread, Ilya said he's working with mnot on variants as well, which works on the first request. It would be good to ask for progress on this. 

(discussion on variants)

Andrew: I've said this seems like something we should do in the connection handshake not in the content of the response. Ilya didn't agree.

Alex: My request, to mnot and ilya: the style of this design choice is wrapped up in the idea that we're out of space in the headers. That we shouldn't add another header without ruining HTTP. So: how much is too much, or where is that line?  If we're past "too much", then shouldn't you be asking us the TAG to prevent anyone from adding any headers anywhere, and to roll back the ones we have?
...Or: what are we doing here?

Andrew:  (reads Ilya's reply)

dka: I think we should register this confusion on the issue. 

Sangwhan: On privacy: I don't know if this is serious, but — this is about the change handler in the navigator.connection.onChange. Given that you have a bunch of web applications in different origins but you want to be able to track the user across these applications (as a single user) — if you put something in the change handler th at does an XHR to a tracking origin, and since it origins from a single IP around the same time stamp, — I was concernd this could be abused.

Sangwhan: hashing a user across different origins... if onchange sends off an xhr to the same origin - a tracking endpoint - if x amount of pages have set up this tracking request at the same time [then you can correlate requests].

Dan: bumped to f2f

---

* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221)



Followups:
* [import.meta.url, and import.meta generally ](https://github.com/w3ctag/design-reviews/issues/208) - Alex
* [`Accept-CH` header is weird](https://github.com/w3ctag/design-reviews/issues/206) - Andrew, Alex
* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - David, Alex

Triage:
* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) 
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) 
* [CSS Selectors 4](https://github.com/w3ctag/design-reviews/issues/219)
* [Async Clipboard Text API](https://github.com/w3ctag/design-reviews/issues/222)
* [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223)

---

Lukasz: hi all ;)






