# TAG Teleconference Minutes

## 21-24 February 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-02-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220221T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @atanassov
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov
* [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @plinss, @atanassov
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-02-22](https://www.timeanddate.com/worldclock/converter.html?iso=20220222T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov
* [&lt;search> HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou
* [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

### Breakout C (APAC / Europe) - [2022-02-22](https://www.timeanddate.com/worldclock/converter.html?iso=20220222T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion
* [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @torgo, @maxpassion, @hadleybeeman
* [`handle_links` manifest field ✨](https://github.com/w3ctag/design-reviews/issues/695) - @cynthia, @torgo, @ylafon
* [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon
* [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo

### Plenary Session - [2022-02-24](https://www.timeanddate.com/worldclock/converter.html?iso=20220224T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* F2F decision
* Breakout B time adjust?
* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Dan, Yves, Amy, Peter

Regrets: Rossen, Lea, Hadley


### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo

Dan: 51degrees think this is a major change that hasn't been thought out enough. One is compatibility with existing content and software layers. In June with Mike Taylor and Henri and Yoav we queried this, they said they've beenr esponsive to community feedback on this point, and the current proposal was to leave enough of the UA intact that it wuld not have this kind of impact, especially on software layers. Talking about in some countries, especially African countries as an example, are making a lot of use of transcoding platforms that make use of UA string information. Mike and Yoav think they have addressed this issue. Jo also brought up where is this being standardised? The UA client hints spec itself is in wicg. There hasn't really been any official trajectory beyond wicg. They think it's going to go somewhere in w3c. I think that's a completely valid concern. It's pretty major and it's just being incubated in wicg. Slightly mitigated by the fact we did have these discussions with the mozilla folks, they do seem to be moving on their position. From a multistakeholder perspective, I think it's a little bit better. However it still really should be moving to a proper standards group. I don't think they have a good answer to that yet. On the issue of compatibility... Mike Taylor left a response and noted.. second part of the issue, that the underlying client hints spec, is in ietf, but marked as experimental. After checking, I don't think that's an issue. Consensus around the underlying client hints mechanism itself. Cnsensus is not around where it should be applied. We've been vocal in the past about hwere it should not be applied. My proposal is to close with satisfied with concerns:

* we want the proposers to make sure they're taking into account the wealth of existing content out there and be receptive to the community feedback about content breaking;
* they should be moving the client hints UA spec, actively, into a w3c WG.

Yves: by freezing the UA string it removes concern about cacheability and certain content negotiation based on the UA string. I'm pretty sure they'll keep it for a while for compatiility purposes. I odn't think 3 is really an issue. Issue is nly implementation is chrome. Needs to be accepted as a standard somewhere and implemented before being widely used. Also a way to do some discovery mechanism, the UA string, need to ensure all the discoverability capabilities exist. If the other UAs are not implementing that, what are they implementing for discoverability of capabilities?

Peter: the client hints are supposed to expose what is in the UA. It's been around for a while but it's a mess, lots of things have been built on it that shouldn't. Some extent of sniffing still needs to be around. Needed more in old days becuase of the lack of interop. Situation is a lot better these days. Do share your concern Dan about where this is going to go. Wondering where all the other client hint specs are winding up, there's a bunch.

Dan: [writes comment](https://github.com/w3ctag/design-reviews/issues/640#issuecomment-1047101251)

Yves: this rfc is in the http-bis working group. Some are experimental and not in a wg but this is okay.

Peter: concerns that nobody else seems to be taking client hints up. And not this, but other client hints being abused, user preferences stuff. I'm not all in on client hints in general. But fine wiht the UA string being frozen and stripped down over time. Firefox and Safari have already been deploying this and are not providing a way to recover the information. I don't have a problem with a mechanism to get the useful information in a reliable way, but concerns some of the approaches they are talking about are just as bad as what was done with the UA string, that browsers will lie about what they are. But in general, the direction is right. Just needs to be handled more carefully. 

### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @atanassov

Dan: Got a response, but can't progress without Rossen. Plenary.

### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov

Dan: I know there are multiple implementations. But all in Chromium. Different stakeholders are interested. Looking at S&P.. don't think theyre exposing any extra info. I think this is good, but I've been kind of working on it.

Peter: one concern is that the segments array is just a bunch of DOM rects. Comments between Ken and darktears that maybe it should have some embedded... should return objects, so room for expansion. Can leave comment. Other concern in general is that they seem to degrade very quickly into only dealing with one particular hardware situation, eg. screens are all the same size, or only two segments. This one doesn't suffer from that, the segments could be anywhere in space. No information aside from doing math with rectangles to figure out hwo they're oriented. Maybe there's metadata thtat can be added later. 

Yves: related to second screen?

Dan: no

Peter: second screen is like casting. This is multiple monitors or foldable screens.

Dan: a few different hareware configurations this makes sense for. Gets very complicated if you start to hink about screens with multiple hinges. 

Peter: I'm right now sitting in front of 3 monitors. There are existing groups of things that aren't just a foldable phone. I want it to not be treated as something different from a foldable phone. I think this one API is fine for that.

Dan: design is kind of born out of that concern. Intended to address that concern, to make sure whatever we do here is forward looking. Look again at plenary.

### [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @plinss, @atanassov

Dan: someone saying it exposes hardware characteristics to the web. They've already discussed that in their responses to the S&P questionnaire. They say it's not meant to solve the problem of foldable devices with more than two screens due to iterating in CSS.

Peter: I have the concern where it's designed for two segments equal size split vertically or horizinatally and that's it

Dan: together with viewport segments the equal size thing.. I don't think it's about equal size..

Peter: this is what's detectable from CSS> The only thing is how many segments do you have. Unless you make presumptions about size and shape of segments it's somewhat useless information. Their example is map view with driving directions. An example in my mind is an email client, a message pane and list of messages - straddling fold I want one on one and one on the other, I don't care where the fold or the edge is.

Dan: that can change depending on what other things are using screen real estate. Not just about where the physical fold is. On our browser you can move the url bar from top to bottom of screen. That changes relatively speaking where the fold shows in the viewport, so you have got to adjust for that to know which is smaller.

Peter: more viewport related units to handle that sort of thing... not well thought out with multiple segments, that's for the entire viewport as a whole. My concern is what you can do with the information they expose, without script or strong presumptions about client and device.

Dan: make sense for you to leave that comment?

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Punted per Lea's request


## Breakout B

Present: Peter, Max

Regrets: Rossen, Lea


### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov

### [&lt;search> HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou

### [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov


## Breakout C

Present: Dan, Sangwhan, Max, Amy, Yves, Hadley

Regrets: Lea


### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris

Dan: they are still working on coming up with an alternative design.

**labeled - and Amy assigned**

### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion

Max: We need to wait for a response from requester

Sangwhan: did we do any technical analysis?

Dan: my comments were all about process

Sangwhan: I'll look at it

### [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @torgo, @maxpassion, @hadleybeeman

Max: I have several comments. Explainer should have more use cases from user perspective. This mechanism is more generic and should also consider how to use this mechanism in other proposals, like mini app. Related but not identical. They need to do some analysis to see whether this can be used in mini apps.

Sangwhan: can we ping the mini app people and see if it works for them?

Max: that is a good proposal

Sangwhan: their lifecycle management and window document in general is nonstandard. It's likely it's not going to work but..

Dan: it's in flux, we've been inputting, our review of miniapp lifecycle is still open

Sangwhan: everything that is how they do browsing context management is different frm what we expect it to be, and how they do origins. Maybe pass it onto them to take a look at and let us know if it doesn't work for them.

Dan: Max, do you think you can leave a comment asking about the use case descriptions, and the feedback you mentioned?

Max: okay

Dan: who can ping mini app?

Max: I can also do that, I'm also assigned to review lifecycle

Hadley: we had asked them to redo their explainer and put it in our format and make it a bit more .. it was really in the weeds and assuming a lot of knowledge already about the subject. They have done a fair amount of work in redoing the explainer, but I agree it needs more work on the use cases. Should acknowledge that they've already done some work. The other thing I'd like to do.. Lea and I had talked about the dangers of using webapp launch handler to open something that was already active and losing state. Example in the issue was if you have google maps open and you're already looking at something, or you have a music player open, and you launch something else based on that, will launching it overwrite what you were doing and how do you get that back, and what do we do about it going against what users expect. The group opened [an issue](https://github.com/WICG/sw-launch/issues/47) which has activity. I'd love to have Lea get back into that and review their issue and see whether she's happy with the progress. Be nice to say we're happy and leave it to them.

Dan: lets try and do that at the plenary. I can put that into slack.

### [`handle_links` manifest field ✨](https://github.com/w3ctag/design-reviews/issues/695) - @cynthia, @torgo, @ylafon

Dan: the one with the URL processing.. Sangwhan wrote some comments

Sangwhan: given a PWA - and the PWA indicating a specific link handling mode - there doesn't seem to be a way for the user to switch it...  User "not supposed to care" - but shouldn't the user have some level control.  That aligns with the previous one - [web app launch handler]. 

Dan: it aligns with the ethical web principles - giving users control

Yves: supposed to be a hint

Laura: if you have 3 apps that hear music - which ones do you prefer... if you have content played using only one application and not the other... There are some cases where "I always want to use xyz application for pqd" doesn't work.

Sangwhan: we haven't got a response... 

Dan: is the feedback about user choice something we mentioned? The EWP about users view content the way they want. With a PWA it can come up in full screen so you don't have access to browser controls. You can go back to the browser and use controls that way, but there's no UI affordances that help you to make a change if you wanted to change the way that something worked. I'm worried this might be a way for web app developers to constrain the user experiences to create walled gardens or stop people opening links the way they want to open links

Sangwhan: if they have a preference on the PWA shouldn't the user be offered the choice?  Given that they suggest this is just a hint - that's dodging the issue. If it's just a hint then what will UAs do? What is the user expectation?  Some browers might ignore it? I don't think we've given them that feedback. There's a philosophical question here

### [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon

Yves: sent something yesterday

### [Region Capture](https://github.com/w3ctag/design-reviews/issues/710) - @cynthia, @torgo

Sangwhan: a misunderstanding on my end, this makes sense now. I talked to the person proposing and now I understand. I think the proposal is fine, the name is unfortunate. I'll comment. It's not region capture as we expect it like draw a rectangle on your screen. It's a document region capture. Constrained to a specific tab. The application decides what inside that tab should be streamed.

Dan: I'm concerned about user expectation.. we understand region of a document, but end user is going to be looking at a rectangle on a screen

Sangwhan: what the user chooses is the tab. If I share screen, this api call will give me the share tab dialogue. The tab, the application running inside the tab, can decide to stream only a subset of what is available on that screen. 

Dan: So it might decide to only share... I understand where that might cme in handy

Sangwhan: helps with mirror effect

Dan: if that tab were a presentation tool and you wanted it to only share the presentation not the controls and editing functions

Sangwhan: right. Now that that's clear, the only thing that bothers me is the name. It looks like a generic region capture mechanism when it's not

Dan: both the things are wrong.. it's not about a region and it's not about capture. It's about sharing.

Sangwhan: it's called capture because its from webrtc

Dan: should be StuffShare. Maybe we can close at plenary.

## Plenary Session

Present: Dan, Peter, Max, Amy, Tess, Yves

Regrets: Lea

### F2F decision

**We are looking at doing a hybrid approach - Dan to work up a draft of what that would look like and share with group.**

**Officially not going to be doing Edinburgh in March.**

### Breakout B time adjust?

**discussion on rescheduling breakout B**

### Breakout Rollup

#### Breakout A

Dan: Closed UA client hints with satisfied with concerns. We need Rossen for Gamepad API, so punt to next week.

Sangwhan: can address some of the responses

Dan: do we feel like the responses on this to Ken's concerns from December are adequate?

Sangwhan: first one was an ack..

Peter: left feedback on viewport segments, no response yet

Dan: foldable CSS, same deal

Peter: was going to leave a comment, did more digging and not sure it makes sense to say. They do expose more information than what I Thought was there, just not sure if it's all useful, need to dig more. Tess do you know can you query environment vars in a media query?

Tess: I don't know

Peter: I don't think so but needt o dig in. You can do a media query are there one or two or three segments not sure you can query is the first segment 100px? I think we need that capability, just not sure if it's doable the way they're exposing it.

Dan: punted html media element

#### Breakout B

Peter: No breakout B

#### Breakout C

Dan: we created a societal impacts label and added it to raw camera access. I've been talking to group chairs about this. Sate extension for JS Self-profiling.. comments so far about process, needs technical analysis. Web app launch handler, talked about applicability of this in other contexts and weird user experiences this might cause that are not what the user might expect, Hadley felt they needed work on the explainer, Max left a comment and we got a response from a mini apps person.

Sangwhan: model is different.. don't know what we'll converge on

Dan: handle_links manifest.. asked for venue but no response. 

Sangwhan: I also asked some questions a couple of weeks ago

Dan: and discussions about user choice. Markup based client hints, Yves sent feedback and have response.

Yves: I'll try to reply today

Dan: Region capture.. can we close? 

Sangwhan: name is unfortunate, gives wrong impression of feature. Feature itself makes sense. It doesnt make tab sharing any less secure. Within the WG there's consensus.

Dan: shall we close and leave a closing comment?

Sangwhan: yes

Sangwhan: **reprises summary of the feature - capturing an element rather than a region**

Peter: currently targetted to an element.

Sangwhan: yes - and if element goes away then TAB gets shared. User doesn't have the choice - the applicationd decided which element is appropriate.

Peter: and if that is scrolled out?

Sangwhan: initial target viewport is streamed - when you target to an element - unless that elemnent is reszied you're looking at the viewport of that element where it was when you initially started sharing. 

Peter: user's expectation that they're sharing part of the Tab.... 

Sangwhan: right now it's the entire tab or nothing...

Peter: used in an application so it would need to know not to have sensitive content on...

Sangwhan: clipped to the visible part of the viewport...

Peter: what if the viewport is resized?

Sangwhan: it resizes up the point where it .. goes outside of the screen viewport...

Dan: what if you're sharing .. it's never sharing that the user who is sharing it is not seeing

Peter: sharing some component of the visible area of that tab. In worst case fall back to full tab

Sangwhan: correct. Offscreen is a potential possibility if the application chooses to do so. I don't think it works in the current proof of concept but Iw ould imagine there would be cases where you would want to have a composite view of something on an offscreen canvas. 

Dan: editing tools overlayed on top of the presentation and you wanted to show the slide.. or speaker notes.. 

Sangwhan: not supported at the moment

Dan: should give a note of caution. Any time the application might share something the user doesn't see or expect, they don't know what they're sharing

Amy: is it potentially a vector for phishing?  like a fake tech support site - it exposes something else that the web page would get?

Sangwhan: ... other ways to scam ... 

Dan: encourage them to think about ways it could be misused

Sangwhan: not significant vs what is available today. Scoped version of tab sharing. If composite canvas sharing happens then maybe. Not part of the current spec. As it stands there aren't any serious issues.

Peter: questions and concerns about if you're targeting an element ad the element moves from scrolling or window resize, and changes size/shape/anything with media queries, is it going to retarget the new area of the element. If I make my window wider and the element gets wider will it still share the full eelemtn or the original rectangle

Sangwhan: they have a demo. Does resizing up to an extent until you hit the screen boundaries

Peter: so if I move the window off the screen?

Dan: close next week?

### Issue Triage
