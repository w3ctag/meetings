## TAG Teleconference
##### 12 March 2019

Present: Lukasz, Tess, Dan, David, Yves, Peter, Kenneth, Alice 
Guests: David Singer, Brent Zundel, Dan Burnett, Manu Sporny, Kaz Ashimura

Regrets:

---

Agenda:

* [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo
  * With special guest David Singer
* [TAG review request:  Verifiable Credentials Data Model 1.0](https://github.com/w3ctag/design-reviews/issues/343) - @hadleybeeman
* [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @travisleithead, @plinss
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice, @dbaron
* [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321) - @alice, @dbaron, @kenchris
* [User Activation API](https://github.com/w3ctag/design-reviews/issues/300) - @hober, @dbaron, @hadleybeeman
* [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241) - @dbaron, @ylafon, @hadleybeeman, @lknik
* [Serialization of natural language in data formats such as JSON [I18N]](https://github.com/w3ctag/design-reviews/issues/178) - @cynthia, @dbaron

---

### [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo

DS: I'm chair of the group but didn't write the spec.

DS: 2 problems they are trying to solve in this spec - (1) you want to present a lecutre and [allow the user to manipulate the stream] as it is being watched. richer multimedia experience. also ad insertion. that's sync of web & media technologies (2) they also want to package that into a single [delivery]. that is where ISOBMFF comes in. if you are retreiving a package from a web server then local names can be treated as relative resources. there is a packaging desire and a sync desire. i think there is too much in the specification. they package many kinds of resources together - html, css, js, images, timed resources, overlays...  This has been going through MPEG for a while.  I think we need to get [various experts] and tech suppliers together in a workshop.

Yves: when the mpeg container is transfered through eme does that mean that eme black box can run js trackers and privacy invasive things without being noticed? is that desirable?

DS: The ability of the web page connected to the same origin - there is no attempt to package things from other origins or resources.  

Yves: if it's encrypted through eme then the browser may not have complete control of what is going on.

Dan: concerns from TAG in context of this, and of HBBTV, have to do with security, e.g., knowing what the origin is, and that the security model of the web is so tightly bound to origin.  Are these packages being retrieved over the internet, are they being broadcast, etc.?

DS: In order not to run afoul of multiple origin problems... where the spec says URL, it should have said local name, which you can compose with the package's URL.  You got the package from somewhere, that's your base for any operation.

Dan: what if the package comes down over a broadcast channel?

DS: Like FLUTE, MBMS or ...?

Dan: or ...

DS: FLUTE names resources by URLs -- so you get a URL for that.

Dan: We also spent a lot of time on securing the web -- securing the web is about tying the security model to the HTTPS delivery as well.

DS: The only aspect I've looked at is the HTTP delivery.  I don't think MBMS and FLUTE have enough security inspection because nobody's thought of deplopying them.  You could construct an MBMS multicast that claims to have URL names claiming to come from example.com, and then presumably example.com would be same origin.  That's not a problem with this packaging, it's a problem with FLUTE MBMS protocol.

Dan: Sounds like something to discuss at this theoretical workshop.  Seems like packaging itself should be something more like signed exchanges.

DS: This problem would come up with simple HTML pages over FLUTE MBMS.

Dan: Then it's inherently unsound.

DS: We're talking about just synchronization of web resources and packaging.

Dan: We've been looking at signed exchanges -- if we say web packaging must have those kinds of properties, that seems to me to be something that could hlep -- we're removing the issue from the delivery.

Tess: From 10000 feet, feels like there have been so many attempts at packaging web content.  Curently there are several simultaneous mutually incompatible attepts.  Seems like publishing people, AMP people, MPEG people -- not talking to each other, may have incompatible requirements, will something work for all or most of them.

Dan: +1

DS: may also be an opportunity -- publishing people talk about books, audio books, narrated books.  Video people approaching same user space from opposite ends.  Image file format packaging untimed resources together -- new adif image format, in Mac OS, Windows, android builds.  A lot of the technology already there.  I have no particular axe to grind here.  Getting the interested parties together to work out uses and what to solve.

Peter: curious where this intersects with ttml

DS: i've wanted to use a text track as a metadata track. ... one waay to tie slides to video time ranges... 

Yves: in webrtc they have separated data, audio and vidoe channels there may be something here.

DS: w3c is obvious place to catalyze such a worksho. 

Tess: there could be interest this year. typically w3c workshops are looking longer term and are about breaking new ground. 

Peter: anything else TAG can do?

Tess: we had a finding on packaging?

Dan: Could we get this MPEG group looking at the security & privacy self check?

Peter: thanks david!

Dan: thanks!

--

* [TAG review request:  Verifiable Credentials Data Model 1.0](https://github.com/w3ctag/design-reviews/issues/343) - @hadleybeeman

Manu: the v.c. working group chartered to work on a data model - we were not cleared to work on a protocol or crypto - spec is going into candidate rec. Broad consensus. We've had multiple reviews from i18n.  There is a group called "rebooting the web of trust" - meets every 6 months - through that venue we've had a lot of engagements out of the traditional community... so quite a bit of review.

We are looking for a sanity check from the TAG from an architectural perspective and on the data model itself.  Multiple organisations implementing the spec.  Being used in product now.  Most of the focus after in CR - and if the work gets to rec is going to be standardizing moving the credentials around. Protocols... 

Dan: what is the time frame?

DanB: asap 

Lukasz: fairly large privact & security section - i like it. might even be too verbose.

DanB: i wanted to comment on lengh and verbosity - PING wanted our best thinking of how it cold be used by others. so we definitely look at your suggestions for compressing the text but PING has requested detail.

Dan: I will ask Hadley to feed back to you asap.


### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron

[punt]

### [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @travisleithead, @plinss

KC: nothing much has happened since f2f. 

Dan: who are we waiting for feedback from?

KC: we got them to to back to the drawing board and consider if it could be based in iframes.

David: we had comments on their explainer.

David: has the explainer been updated?

Lukasz: the document is unfinished in my opinion - i am seriously concerned with the privacy [discussion] in the github thread. data leaks between the origins. not clatified in thread.

Dan: maybe bump and come back to it?

Peter: bump and wait?

KC: lot of feedback from Alex Russell here.

KC: I can monitor it.

Peter: kicked it 3 weeks.

### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice, @dbaron

David: bump 1 week

### [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321) - @alice, @dbaron, @kenchris

Alice: they agreed it's not really ready for another look. I asked if it's ready for feedback. They have said not ready yet.

David: other option is to move milestone to next f2f.

[decidion to close it for now with a comment asking them to file a new issue or ping us to reopen]

### [User Activation API](https://github.com/w3ctag/design-reviews/issues/300) - @hober, @dbaron, @hadleybeeman

Tess: if the expaliner were updated ... he was able to clarify everythng but i want to see it reflectedin the explainer.  will ask for an updated based on the call we had last week.

Peter: sounds good.

Tess: we coudl close and and ask them to re-open.


[agreed to move to jitsi due to some issues with appear.in this week]