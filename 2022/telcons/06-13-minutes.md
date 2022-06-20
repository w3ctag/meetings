# TAG Teleconference
#### 13-15 June 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-06-13](https://www.timeanddate.com/worldclock/converter.html?iso=20220613T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman
* [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602#issuecomment-1121694034) - @atanassov
* [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov

### Breakout B (US / APAC) - [2022-06-14](https://www.timeanddate.com/worldclock/converter.html?iso=20220614T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss

### Breakout C (APAC / Europe) - [2022-06-14](https://www.timeanddate.com/worldclock/converter.html?iso=20220614T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman
* [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo
* [fenced frames](https://github.com/w3ctag/design-reviews/issues/735)


### Plenary Session - [2022-06-16](https://www.timeanddate.com/worldclock/converter.html?iso=20220616T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


-----


## Breakout A

Present: Peter, Amy, Dan, Lea, Rossen, Yves, 

Regrets: 

### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Dan: I left a comment. We reviewed last week. Generally positive. Asked about multistakeholder. We were hoping they'd have come back with an answer so we could close.

Lea: I could ping the requester

Dan: great

Peter: revisit in plenary. Does this change during a pageload? 

Lea: I think we concluded that it doesn't?

Dan: concluded it would be up to the UA to mediate the change to something that makes sense? Or up to the device, so the device has to .. it's a blunt instrument, designed that way. Up to the device not to flip it back and forth multiple times per second

Lea: are there any use cases of changing it throughout the life of a website or app?

Rossen: the default, you're moving. Changing cell towers. Bitrate varies.

Lea: I understand your bandwidth might change. but if you've already loaded the high bandwidth website is there any case where you might want to switch at that point? After you've already loaded all the assets.

Peter: maybe you haven't. If you've loaded them there's no pint in throwing them away

Lea: exactly

Peter: but if you're on a navigation site and you're moving it's goign to be loading new images of where you're go. Walk out the door from wifi to 3G. I have high res content, and now I start getting low res content. Or do I keep getting high res content because I initially loaded the page in a high bandwidth content?

Lea: so it can end up sending more bandwidth than either version?

Peter: if you reload assets yeah

Dan: but that would be up to the app designer

Lea; if you're writing css that loads certain background images under this media query you have no control, they just load

Rossen: my comment from March 22nd asks about that

Dan: I think it wasn't as explicitly obvious until I heard Lea articulate it. Might be worth raising separately in the issue.

Rossen: sure

Dan: I was thinking about it from the perspective of as Peter was saying, you're using a web app, scrolling and you certainly wouldn't want if the web app had already downloaded the high quality assets that it would throw them away

Lea: thinking of match media where you control through js.. but there are a lot of declaritive things that load when a media query matches. Fonts, background images, srcset.. all of that stuff is triggered automatically without any control. if the media query changes what it matches then you'll end up loading a bunch of stuff.

peter: you shouldn't reload something youv'e already loaded, but it's pretty easy to get into a state where you've got half the assets loaded under high bandwidth and some loaded under low. And maybe they don't match any more.

Lea: who is you? The app developer writes html an dcss that matches a media query, they are nto doing the loading. They migth think they're being nice and providing a low res version and end up loading both the high res version and the low res version because the user had some spike of bandwidth

Dan: that's not accounted for in their explainer

Peter: I'm concerned if it flips half way during page load. Half may not match. 

RosseN: which could be changes to layout even

Peter: I could have said under high bandwidth I load a pretty background which measn I have to have my text be white, and on low bandwidth background is white and I get white text on white. One solution is you pick one at the start of page load and stick with it, but that could leave users loading high bandwidht content later

Dan: or what's the beginning or ending of a session. I coudl go to a webpage, ptu  my phoen down, pick it up 15 minutes later and scroll on the same site. But in different network conditions.

Peter: or I start streaming a video at home, then walk out the door - switch to low bandwidth version in the middle?

Lea: valid use cases for both something that changes and something that doesn't. Maybe a media query is not the best approach here.

Peter: or the behaviour needs to be clearly defined so authors can reason about it. I remember we had these questions, was wondering if we got answers

Rossen: very wishy washy..

Peter: not so much thought through

Lea: should definitely not be up to the implementation. I think that's the worst of all worlds. Not knowing what you'll get.

Peter: agree behaviour should be clearly specified

Lea: also the simple syntax should not be doing the evil thing. I don't want to see well meaning authors wasting more bandwidth trying to do the exact opposite

DRAFT COMMENT:

```
```
Hi Adam,

We discussed this again today, and in addition to our previous question about multi-stakeholder support, we had some additional concerns related to when this MQ is expected to change (which based on your previous comment seems to be left up to the implementation right now).

If it could change every time a user's connection speed changes, then this has the potential to be the worst of all worlds: **both** the low and high bandwidth versions of any CSS or HTML assets differentiated based on this MQ would be loaded, spending **more** of the user's bandwidth than if the MQ did not exist at all. We can see many well meaning authors doing things like:

```css
.foo { background: url("4k.jpg");

@media (prefers-reduced-data) {
	.foo { background: url("hd.jpg");
}
```

Imagine a user that starts off high bandwidth when the website is loading, then gets a reduction in network speed later. Not only have they actually downloaded the high bandwidth version of the website (and potentially paid a lot for it), but won't even get to enjoy it because **once the MQ flips, it will trigger the lowres version even if nothing is actually downloading when it changes!** Not to mention how jarring it will be to experience the change.

While it's easy to address that by caching the value of the MQ when the page loads and using a corresponding root class, in general in Web Platform features, the simple syntax should not be doing the potentially harmful thing.

If assets are loaded imperatively, this is also not ideal, because you could end up with a website with mixed assets, which may not even work well together. 

Lastly, there are also use cases where you *do* want the MQ value to reflect the most recent knowledge about the user's network speed or preference, e.g. in apps that load content continuously, so redefining this to remain fixed for the entire session duration would also leave a lot of use cases out. 😕 

```
```

### [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman

Amy: there are 3 things things....  Easier to talk about them all together... 

Peter: max is on some of them...

Dan: timebox discussion here and then discuss rest in breakout C.

Amy: They have done a lot of work on security & privacy - good on many different angles. Guidelines, recommendations, answers to questionnaire... 2nd first impression - there is a LOT here.  Lots to digest.. Overall I think it's probably fine.  They have an architecture document -contains background material & examples. Doesn't feel like a normative document.

Dan: I agree ... 

Amy: the way they've broken it up makes sense but the arch document doesn't seem to be rec track material. Maybe take the normative statements here and put them somewhere else and release it as a note?

Peter: meta question - there's a standard called Matter. Does this tie into that at all?

Amy: they do mention they are not trying to do something where they are trying to create a new competing standard but more of an overarching...  We could ask them.

Peter: I thimk Matter does have an actual protocol - more IP based... works on bluetooth BLE, z-wave, etc...  Does anyone care about web of things?  is the industry going another way?

Amy: they discuss the fragmentation a lot...

Dan: to channel Sangwhan.. where does this fit into the web? There was a scripting API but saw no reference to that

Amy: it was published as a note in 2020 but I don't know why.. maybe no browsers involved?

Dan: I think that question is relevent. Doesn't invalidate the work or mean it shouldn't be happening, but is relevant to ask. Some of the demos I've seen do have an answer to this in terms of it's using browser interfaces and http

Peter: somewhat naive concern - when I look at home automation they use wifi and 

Amy: I don't think they're ignoring - lots of discussion of things not being connected all the time... I don't want my things on the web. But I felt reasonably good about this by the time I finished reading.

Dan: Anything on the abuse use casess?

Amy: no location info shared (anything to do with geo is deferred to future)... everything in terms of discovery of devices is gated bethind authorization - but what they've asked us to review is about metadata of devices, not sensor data itself.

Peter: simple protocol to intgerate home devices... 

Yves: note that some vendors use wifi-connected device but have the possibility to work only on the local network (ie: do not phone home). Also the privacy/security of BLE is... often not existant

Peter: I agree... security model is short range. 

Dan: my understanding of the arch is that it imagines a proxy where that type of situation exists

Peter: the hub that controls these things locally is a web of thing thing

Yves: ways for devices to advertise themselves .. not phoning home.. but that's pretty niche

Peter: not an ideal model...

### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602#issuecomment-1121694034) - @atanassov

Peter: ..

Dan: popping up multiple windows can be a way that bad actors try to confuse the user by ocluding bits of browser ui, making it hard for them to get back to what they were doing... but is this only in a multi screen scenario..?

Peter: when you have window placement permission already. And you've got an activation so you can place fullscreen content. And what youc an now do is let you place popups on other screens. So you won't get 100 popoups all of a sudden, but you could go to fullscreen mode and get popups on other screens. That may be what you want in some scenarios, but share the concern.. can it be abused by.. not always fullscreen on the most ethical sites.

Dan: I'd like to unerstand if they';ve really thought about the abuse scenarios

Peter: they [list mitgations in the explainer](https://github.com/w3c/window-placement/blob/main/EXPLAINER_initiating_multi_screen_experiences.md#proposal)

Dan: are they considering browsers on keyboardless devices? They talk about esc key for instance. Not available to everybody. Are we clutching at straws? Minor change.

Dan: minor change.. should we just close?

Peter: I'm ok to close it I guess. I do have concerns about how badly it can be abused...

Dan: Proposed comment on multi-stakeholder:
```
@michaelwasserman when we closed this issue last year we indicated a concern related to multi-stakeholder. I note that the API is still being developed in the Second Screen Community group and Chrome Status does not list any other engine that has expressed interest. Has this moved in any way towards the Second Screen working group and has there been any interest expressed by other implementers?
```

Rossen: Looks different from the initial ...   Now... The way I see this is that this is generally reducing friction.. not enabling something that is not possible.  Question is: is that friction really that bad?  

Peter: how can it be abused? To me the abuse could be "i am on e.g. instagram, i press full screen, i get ads popping up on all my other screens full-screen".

Rossen: If I have an app that is a fullscreen app and I launch another app that is also full screen the first app may or may not exit full screen.  With multi-screen.. with modern window management capability - i can separate by sections... launch one of those apps and my screen layout will not change on the 2ndary screen unintentionally...  I don't see where they address privacy & tracking... Taking over screens, especially multiple screens, could... 

Dan: I don't think they specifically address that in mitigations. They're not talking about privacy and tracking

Rossen: trying to see if they cover it somewhere else

Dan: indicated they're interested in moving it to the second screen wg, so want to ask about that. Would make sense for someone else to ask about the abuse scenarios?

Rossen: I want to expand the comment about privacy and abuse. Does it need to be part of this review or fork off to a different review? it's very related but it's an extension.. why are they reopining the same issue

Peter: could have been a new review request

Rossen: if we ask them to open a separate issue they'll have to go through multistakeholder etc again

Peter: we dont' need to religitate everything we already reviewed. Fair to push them on multistakeholder because that's left over.

Dan: I can also post about abuse.. but I think Rossen had it more in his head

### [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov


## Breakout B

Present:

Regrets:

### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

### [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss


## Breakout C

Present: Dan, Amy, Hadley, Yves

Regrets: Max, Sangwhan

###  [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman

Amy: they did one security & privacy review for all...  Lots of linked data in these specs.  They have been very explicit about no dependency to JSON-LD. "Just JSON"

Yves: There are plenty of JSON-LD parsers around... Shouldn't be an issue. Usually IOT hubs would require processing those.  I've run into some devices that have javascript... I have web of things devices...

Amy: one of the things thye've done in the arch document is to make security & privacy sections normative - seems like a good step. ... before plenary [call] I want to go through it and look at what the normative statements are in the arch doc - maybe see if it can be split into 2 documents. One consise normative document and one informative note...

Hadley: [explainer section](https://github.com/w3c/wot-thing-description/blob/main/explainer/Explainer11.md#differentiation-to-thing-description-10-and-backward-compatibility) describing diff to 1.0.

Dan: what is a thing model?

Amy: a generalization of a thing... rather than an instance

Dan: why did they not need that in the previous version? Before it was Thing Template... 

Dan: can we close thing description as it's a minor update and keep the reviews open for things arch and discovery...

Amy: yes makes sense.

Hadley: yes seconded - doesn't seem like it's a massive change.

Hadley: just re-reviewing the original review we did.

Dan: there are a whole bunch of issues in their repo that are linked from our [issue 355](https://github.com/w3ctag/design-reviews/issues/355) which all appear to be clsoed.

Dan: There is one [open issue](https://github.com/w3c/wot-thing-description/issues/791) from our last review of web of things description.

Amy: it's got a label "defer to 2.0"...

Hadley: we could include a mention in our closing comment.

Dan: I think thay makes sense.

Amy: deferred several times though... 

Dan: wonder if there's just a disagreement in the group with David's framing?

Hadley: looked at the issues opened against our arch review (355) - looks like they've all been considered... looking [at 178](https://github.com/w3c/wot-scripting-api/issues/178)...

Amy: if that's on the scripting APi then we're not reviewint it.

Hadley: Ok perfect. *writes closing comment for 715*

### [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman

Amy: I'll draft a comment on this for the plenary which might also cover Discovery.  Use case is that parties that want to put content side by side are being considerate and throughtful of user's privacy. So who does that?

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo



### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo


### [fenced frames](https://github.com/w3ctag/design-reviews/issues/735)

Amy: (1) what's the catch and (2) why would anyone use it?  It's tight for privacy... so why would anyone choose to use it?

Amy: it says "this can only be allowed if the documents are isolated" but allowed by whom?  Is the assumption that.

Dan: leave a comment asking this so we can probe this issue?

Amy: is it assuming 3rd party cookies going away?

Yves: don't think so...

Dan: I'll note that chrome status shows no signals from other engines... It's in WICG now but they are thinking about moving it to WHATWG.  So my question would be: do they have consensus in WHATWG-land?

```
From our initial review we think this looks great from a privacy perspective.

Regarding the use cases that Fenced Frames are meeting - how are they currently achieved? What will motivate developers to move to Fenced Frames instead?

We see you expect to move this work to WHATWG - are there positive signals from other implementers in the WHATWG community?  Because right now that is not reflected in Chromestatus. 
```

## Plenary Session

Present: Dan, Peter, Max, Amy, Yves, Sangwhan

Regrets: Hadley


### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Dan: `prefers reduced data` .. Lea left a comment. Could lead to more data being used. We have responses. Which are that it's intended it's a user choice rather than based on network conditions

Peter: until ua adds that auto setting

Dan: exactly, that's what happened with dark mode. Pretty reasonable to make that.. what's in the spec to normatively say the ua should not be making this choice?

Yves: always the same issue - trying to figure out what kind o fnetwork you're on, which is always difficult, if you have a 4G base station, and you're on wifi, and you can't figure out..

Amy: also still doesn't solve the problem of the unspecified behaviour when switching between

Peter: what happens when the switch is flipped? they have to make the call. Does it only apply to future loads, or refresh everything, or not apply at all? one way or another they all have problems, but the spec should pick one and say it so at least it's interoperable. Are they thinking through all these implications? They need to. Is there a better approach?

### Breakout Rollup

#### Breakout A

Dan: Web of Things Discovery - action on Hadley to close. Very minimal

Dan: multi screen..  Rossen left a comment. They responded. Good responses. We need Rossen to close it.

#### Breakout B

n/a

#### Breakout C

Dan: More WoT.. No progress on permission policy unload or back forward cache because we need Sangwhan. Talked about Fenced Frames. Asked why anybody would use it becuase it looks really privacy preserving

Amy: answer was because 3p cookies are going away. Want to dig into use cases properly before responding again.

Peter: years ago someone was proposing Portals.. we pushed back and wanted them to define frames properly and understand this more widely before making new kinds of frames. I don't think anyone has done that work.

*discussion on fenced frames via portals*

Amy: CG report from 2021 ... https://wicg.github.io/portals/ 

Peter: we talked about this stuff years back... We had a meeting with some Google folks in Tokyo... 

Dan: finding [the minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2019/09-tokyo/09-12-minutes.md#portals) ..

Peter: seems like the same arguments we had about portals applies to fenced frames

Amy: I would love to hear about use cases that are not adverising related... also trying to appreciate that if this really does help with privacy then we shouldn't step in front of it too much...

Peter: basic idea - it's its own first party?  Does the fenced frame have any knowledge about the document embedding it at all?

Amy: it has 0 access to sensors... anything with a permission prompt denied... etc...

Peter: embedding document could pass data via attributes?  Would it not have access to its own attributes?

Dan: what's to stop ad networks from telling publishers they must do this other thing to provide data down a side channel if they want to participate? Under the umbrella of why would people use it unless they're forced to ... 3rd party cookie answer not enough

Amy: those use cases... "that are motivating .. require cross-site user access ... reliant on cookies ... so they need a solution that doesn't require cross-site data acces..."  Not super clear.  It does say "iframes do not suit this purpose because of [comms channels]" implies fenced frames would not have those channels. In the explainer they have privacy considerations where they are still working on mitigations.. like the size attribute being limited to only a few values...

Dan: sounds like it addresses the issue peter raises.

Peter: can the document loaded in the fenced frame know it's in a fenced frame?  Don't see this spelled out anywhere. Still leads back to question: If i'm an ad network, why would I want people to do this?  Trade-off ...

Amy: it may be that the only way they achieve that now is with third party cookies...

Peter: I'd like to know what the other use cases are beyond ads.

Peter: they link to TURTLEDOVE... It's indicating other side channels that the ad has access to.

Dan: we also have an open review on that

Sangwhan: cohort hinting mechanism for ad networks

Peter: so a completely isolated frame that can tell nothing about the context it's embedded in, but browsers can give other information through this private side channel

Dan: but turtledove would give you that in a way that doesn't allow you to trace back.. it's providing this data separately so that you can't correlate

Sangwhan: trying to obstruct the provenance of the signal and the amount of entropy that can be captured, by using the browser as an agent

Peter: browser side channels are a concern

Dan: worth probing.. similar dynamic to FPS.. But having looked at turtledove and seen what people have said, discussed in privacy ad technologies cg.. getting traction, saying maybe it does address privacy issues for targeted advertising. Could leave things in a better position.

Peter: is possible. Or could make it worse wrt power dynamics.

Sangwhan: two extreme ends.. more power to big players vs allowing lots of small companies to collect this data. Seems to be little middle ground.

Peter: have mechanisms like fenced frames, and *don't* add the side channels.. focus on protecting users. Ads don't get special priviliges.

### Discussion on Breakout Timing

Sangwhan: drop B, try to increas participation in A?

Yves: issue with moving one hour earlier... 

Peter: what if we started A an hour earlier and ran it for 2 hours... 

Amy: moving B to one hour before A....  Agending them seperately.... Poll?



### [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman

### Issue Triage
