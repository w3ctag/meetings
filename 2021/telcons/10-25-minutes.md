# TAG Teleconference
#### 25-27 October 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-10-25](https://www.timeanddate.com/worldclock/converter.html?iso=20211025T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris

### Breakout B (US / APAC) - [2021-10-26](https://www.timeanddate.com/worldclock/converter.html?iso=20211026T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov
* [Back/Forward Cache](https://github.com/w3ctag/design-reviews/issues/628) - @hober, @cynthia
* [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @cynthia, @atanassov
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

### Breakout C (APAC / Europe) - [2021-10-26](https://www.timeanddate.com/worldclock/converter.html?iso=20211026T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo


### Plenary Session - [2021-10-27](https://www.timeanddate.com/worldclock/converter.html?iso=20211027T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss
* [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss
* [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov
* [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* [HTMLPopupElement](https://github.com/w3ctag/design-reviews/issues/680) - @hober, @LeaVerou, @kenchris, @atanassov
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Dan, Peter, Rossen, Yves, Amy, 

Guests: Chris Wilson, Dominique Hazael-Massieux, Alex Cooper, Piotr Bialecki, Klaus Weidner

Regrets: Kenneth, Tess, Sangwhan,

### [Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652)

[intros]

Dan: the overarching question with the raw camera access api is, looking at the existing AR module of the webxr api set, it feels to me and I have come to understand that it's built in a way intended to preserve user privacy. Specifically so the web app does not get access to the camear image - that it gets access to room geometry. Yet there is still a warning because you're allowing access to a sensor so we want to be able to provide the end user with some kind of permission prompt, however the stumbling block of this review was that we were looking at this and saying now there's another api that is similar to the ar api but also provides direct access to the camera view and that also has a permission prompt associated with it. So one of thet hings I was trying to bring across in my review comment was why would I s a developer choose to use the less potetn version of the ar api if I could get a version that grants access to the camera image, so therefore when ar is deployed in the wild, eg. I'm sitting at a restaurant and I scan a qr code and I'm jumped into a fun web ar experience, why wouldn't the developer just choose to use the raw camera accss version of that and potentially open themselves up to additional privacy threats that they would not have had if the weba pp was using the non raw camera access of the ar spec. That's the discssion we had and we got into a conversation on the issue about additional mitigations that could steer developers towards the use ofo the standard augmented realtiy api unlesst hey absolutely needed ther aw camera access power. The thinking is eve if you provide a more scary warning if you're a regular web user and youre sitting down and you want to put the funny hats on your friends you're not going to pay attention to the prompt - it's necessary but not sufficient in order to protect the user from the privacy threats and end users ight not have the mental model to understand what those privacy threats are, like that this means that everyone is around me in cluding strangers oculd have their faces recognised using some web assembly code and I've given access to that and there's no additional privacy informatin available, but because I'm already authetnicated to facebook (for instance) that information can be correlated with other information and all of this creates additional privacy risks for the end user. Maybe we can come up with some ways to think about this that can move us in the right direction.

Rossen: let's go from here

Piotr: what I asked in the TAG review is do we think the changes we are thinking about to increase privacy of this api, would those mean we need to tweak the api shape itself or do we think we can keep all the mitigations in the less normative but still important privacy sections? What I'm trying to get out is do you think the api shape has good standing, can we defend it the way it is, or do we need to redo some of the work to introduce some privacy perserving mechanisms? I'm worried about how do we introduce them without crippling the api so it becomes unusable. If we are okay with the api shape itself and it's a matter of making sure the browsers make correct ui choices that becomes trickier because we usually stay away from having normative text around browser UI, but I do agree there has to be something that incentivises the users at least to pay attention to what we say to them. That's the only mechanism we have to tell them about potential issues that they might encounter by accepting the permission prompt. How do we communicate in a way that is clear to the user and says everything we want to say, but at the same time I know even webxr itself already has a lot of text around inferring intent, eg. text that says if an experience is a pwa that serves as inferring that the user intent is present because the user installed the app and we want them to feel the same way as native apps where you would get the prompt when you install the app from the store and maybe when you launch for the first time.

Dan: I think this is exactly the issue. We really want people to use this api rather than the laternative which is simply hacking it on top of getusermeda. But Iw ould challenge you to think about are there normative things that you could do that would - not cripple the api - that would .. eg. in other cases with powerful apis with privacy infringing information the people working on those apis decided to introduce fuzzing on values. If you're worried about specific threats like facial recognition is there something we could do that would mitigate against that. Facial recognition may be one of the use cases and it's very useful, however are there other kinds of fuzzing that could be enabled?

Dom: in terms of normative reqs on UI the getUserMedia spec has normative requirements on privacy indicators for usage of cameras and ability of launch camera. In a way getUserMedia is a bad guide here, it provides access, once you have it you have access to everything, but it comes with fairly highly normative degree of guideance on what needs to be displayed to the user. You asked is this a conersation in the webrtc wg - it has been quite a bit of a conversation to get to this level of specificity on UI. Anther evolution on getUserMedia in the context of realtime comms is we are now building the bricks for e2e encryption which will ultimately mean you can have something like what you are doing today without webar getting access to the camera feed with the browser reamining in control. Doesn't work if you want to do processing of the media. tHe conversations exist with regard to what you can achieve when you want to do media processing

Klaus: one alternative here is the getUserMedia based apps which bypass xr. Users have an all or nothing choice, either they grant camera access or nexperience at all. With webxr we want to support this as an optional feature so the site can say if you grant rawcamera access but without it the experience will still work but with some features unavailable. Applications can see if it's a required feature.. the goal would be to support this middle ground so people have an actual choice. They can say 'do webxr yes/no' and if they say yes they get another choice with raw camera or not. And we want to uspport apps making the rquest later whne they need the feature instead of upfront but that's still under active discussion. We want to give people the choice which is not a choice they have if the application doesn't use XR.

Piotr: with different permission prompts - if we assume people dn't read them there is not much we can do about it. And also to touch upon what Klaus mentioned this api is still not .. we still haven't gone through eg. UX review. I'm not the only stakeholder. It's hard for me to say what Chrome will say I'm allowed to do or not. It's also hard for me to mandate what Chrome UX team tells us to do in the spec. There are conversations that need to happen but I would be really cautious abut saying exactly how things need to look or behave in terms of UX as that also differentiates browsers. I looked at the indicators for getUserMedia, that's something I want to explore. How we can bring into Chrome. As I've said I'm not the only one making those calls. Additionally there might be some tweaks in the implementation, but those should be fine. So we'll see how things go, I'd like to be really careful about mandating UX.

Rossen: Generally speaking your question was is the api on a technical level okay or are we worried about privacy and what does that mean for the user? My view is that the shape of the api is more or less fine. I don't see a reason why if I was a user I wouldn't use that api comfortably. The elephant here - privacy is the problem. The conversation can go two ways. The basica feedback is when you work with audio/visual sensors, especially if the bytes can pipe back to who knows what, we're not talking about user privacy alone. We're talking about the privacy of everyone around them. As soon as I turn my camear n and I want to demonstrate on someone how funny a particular object will be on top of a table in a restaurant, I'm infringing on the privacy of everyone around me who is part of those frames. I don't think that we have UX solutions today that are resolving this. Not on native let alone on web. This is the biggest hurdle I have had with this particular review. Are there other APIs that are today just as faulty? Yes. Should we make it that much easier? Let's not. If there's a technical grind that people have to go through in order to get something very similar to what you're proposing to allow, for the time being, if this is what it takes to preserve some public privacy as much as possible then perhaps this is how we go. I'm trying to approach yoru question in the most straightforward way. In the past we've discussed mapping, object identification, this is already a step to mapping someone's building inside without them knowing, and perhaps this is leaking someone else's information without their consent. There's no way today that we're approaching public consent in the form of this capability. That's where I'm at with this.

Amy: +1 what Rossen said

Chris: The intent is definitely not to make it easier to expose that information. That is a non-goal. Everyone understands that when you turn on your native app camera on your cellphone that is potentially an invasion of privacy of everyone around you. Any AR real world geometry API is already doing some additioanl disclosure. We want to make sure this is underscored. this is raw camera access, you are giving potential access to everything, this isn't any easier than giving access to all the camear. Shouldn't be made any easier than accessing the camera becuase it's exactly the same thing. we're not trying to skate past that point, we're trying to make it clear that this is an extremely powerful api and the main reason behind doing this in my opinion is basically to figure out what things we can make easier that are safer, but that's going to be a long journey to figure out.

Piotr: to make sure I understand - let's say that we take the privacy section out of getUserMedia and copypaste it into this api would that be a satisfying solution? Mandate the indicators that the camera is in use? I think tha'ts the only gap we have right now between the behaviour of getUserMedia on android and our implementaiton. The permission prompt is displayed, with always the discussion of whether it's informed consent, which is something I'd like to improve. Let's say we do display the indicator when the camera is being used would that be something that would be sufficient for this API to meet the privacy bar? Or do we want to tweak it even higher? We already have cases where apps built on top of getUserMedia that do the same thing that native apps can do through ar core, because they run their own algorithms on the frames as they come on. This is something we right now want to reduce the nubmer of apps like this in the world becuase we have a company that asks us to expose the pixesl so they can build features on top of them, but it willa llow them to switch over the webxr and hpefully it'll allow them for the experiences that don't need camera access to not ask for it. I'm worried that if we don't have something like this in webxr people that are motivated enough wills till have access to the camera and they'll present the same experiences but they'll get no benefits that webxr would give them. THat's something we have to take into consideration

Dan: understood. 

Dom: one thing that is very different with webxr in ar mode is it's very much expected it will be looking around you which isn't the case with getUserMedia which is usually looking at your own face. You can reasonably understand what it means to have camear recording you, undrstanding the fact that whichever company you've opened your camear to have fun putting pokemons around you can now figure out where you are at that time. That's not something any user would create a good mental model.. I'd love if we can have this firtual camear that can fuzz faces by default and you have to have another nudge to unfuzz faces, but where do you start

Dan: a lot is based on research that has gone on in varoius places that hasn't been really stitched together. We do have a lot of received wisdom regarding things like how useful prompts are, depending on who you ask you get a different answer. I think it is clear intuitively that I odn't think end users will understand the difference between you're giving me ar access so I'm seeing my camear image so I know it's on, vs *raw* camera access, which from my perspective will be a very similar user eperience, but also the web application has access to the camear access, that requires a sophisticated understanding of how the web works and how computers work, but most people don't have that understanding. To Dom's point about when you're using getUserMedia you expect that you're sending your camear image, but if you're using it for an AR session you may not understand the other people you're putting at risk. Are there other mitigation factors that could be put in place that oculd steer the developer towards using ther egular ar unless they absolutely need raw camera access.

Klaus: hypothetically the browser could detect faces and autoblur - the flip side is people might be looking at browser source code and seeing it's permanently doing facial recognition while ar is active, what is the evil company doing with that. And a difference between facial recognition and facial detecting. Be nice to fuzz things that are concerning, but how feasible? If you blur pixesl enough to make face recognition impossible it would likely make the use cases impossible. It's a hard question. About getUserMedia, as far as the api shape is concerned there wouldn't be anything stopping people from making a getUserMedia request during an AR session, not in Chrome's implementation, but if we really want to not use the camera in an AR session it would not be enoguh to say no raw camera access, you would also need to say you can't have getUserMedia during an ar session, nothing that forbids that

Peter: I'm hearing this doesn't enable a specific features for XR but it's a layer that allows the building of other features. In many casse we have that these other features could be built in a privacy perserving way, it's this raw part that's the dangerous bit. We've said the low level raw access does not belong on the web. Eg. custom shaders. Just becaus we need this to experiment doesn't mean this is something we need to expoes to the entire world / entire web. Maybe we want to develop the higher level features and ship those instead. That is an option here. We don't have to do this just to enable the experimentation.

Dan: I think they would say yeah but you can do it already with getUserMedia

Peter: I know it's not that simple. The low level not good enough excuse to open the privacy door.

Piotr: what I'm hearing - it seems that we might be able to proceed assuming we make the api more painful to use from the users perspective so developers will be disincentivsed to ask for raw camera access. Two prompts in a row, users will not be okay with answering without thinking. I just said yes, why are you asking a second time? Might be something we can lean n to say that this is now becoming a more informed consent. Maybe throwing in the indicators that the camera is in use. What kind of mitigations can we put in place for this api to be okay from the privacy standpoint? Assumign we compare to getUserMedia, the developers can always fall back to that if there is something here they cannot accept. To answer Peter - the use case that I've seen that I was impressed by is if we were thinking about introducing image tracking and I see... some ways of doing object tracking. Ther eis a use case that was shoe detection. The point was we don't know what people will want to do with it so it's hard for us to write a privacy perserving api in such a way that it's extensible to allow for all those use cases. I dont think we want a brand new shoe detection feature built into webxr. But it is possible with raw camera access. The other example I've seen is we are thinking about image detection, but now someone is saying cylindrical image detection, eg. an image printed on a bottle label that allows experiences when you're holding a product from some company and you can interact with it. THe point is we might not be able to standardise everything in a privacy perserving way, but it might give us ideas n what is good t stadardise to have this feature out there and see what people do with it. Maybe there are things we can make work in aprivacy perserving manner.

Dan: in the discussions in getUserMedia context, have there been discussion about additional privacy features which might be added in future?

Dom: lots of discussions about device selection to reduce fingerprinting. And about media streams in the context of webrtc, at least give primitives to allow transmit streams instead of bytes. Exposing object recognition detection.. in context of webrtc but it's built on top of getUserMedia medai streams. Maybe there another hook for additional privacy protections or scary prompts, I'm not sure what yet. That may be another place for exploration and experimentation. 

Peter: maybe possibilities for adding extension points for doing additional types of object detection that don't require exposing the entire full media stream. An API that gives you snippets or a lower framework or something to a specific api that allows you to use a worker to return some object information that's isolated or sandbox. Has that been considered?

Dom: that's kind of what was discsussed at a session, only kind of. 

Alex: I would caution against making it that much harder to do raw camera access than doing get user media. It's not speculative - there are concerete examplels of developers that do ar with getUserMedia right now. In a typical get user media session you're not doing xyz... developers use it and users are doing the exact thing they're doing in ar. You're incentivising users to move to built in ar apis, better power usage etc, and still improving user experience at the same level as if they're using getUserMedia. On object recognition, I have int he past looked into doing face detection, as I was talking to some devs about that, it wasn't something we pursued, one of the hard issues with standardising osmething like that is differnet people expect different things they can do. Expect the face mesh to look a certain way, more points, less points, more generic regions. Once you start looking at object recognition the field of what people want explodes. There are existing wasm modules and js apis that can do this detection but also you can do the shoe detection but because you can't do this other thing they still would just use their full pipeline.

Dan: it sounds to me there's the possibily there might be additional locking down of getUserMedia. It was designed at a time when web assembly didnt exist and it wasn't possible to do al ot of this image deteciton in the browser, these privcay doors weren't opened up. We can't divorce it entirely but you need to split apart what you can do with getUserMedia from what you want to do here. 

Piotr: the sandboxing part, we have been thinking about previously and based on the feedback I got from eg. editor of core webxr spec, he's saying there have been ideas around sandboxing but there's no real good way to avoid the side channel leaking of the information. Even if you have a locked down sandbox with access to camear pixels there are still ways to get information out of that sandbox by inspecting how long things take for example. I don't have a good way to answer is there a way to extend it in a privacy perserving manner

Peter: not to design the sandbox, we do have things coming out to create more locked down environments. My concern was more has this been considered. Maybe should be explored before we just expose the camera. If yu're worried abut side channel there are ways to mitigate - adding stuttering, delays. Has that been explored? Maybe we should take time to explore that before we just expose everyting to everyone. I understand you can already do a lot of this with getUserMedia but it's not permissiont o just keep doing it - maybe means we need to lock down or get rid of getUserMedia because it's too dangerous. We can look at what is getUserMedia used for and support higher level apis that support that without giving access to media. Higher level principle of just cos we can do something doesn't mean we should continue to do that and use it as an excuse to do it more so somewhere else.

Dan: I have appreciated that you've all joined us today. I hope that's what's coming through is that you're understanding we're trying to be constructuve and it is an extremely difficult.. this is the most difficult kind of design choice from an architectural standpoing for the web that we have going right now. This is the point between new features and privcay and danger and tha's exactly why we're spenidng time and energy on it. What I'm hoping... maybe you all could brainstorm and come back with additional ideas about normative privacy mitigations that might when taken together. That has to be more than an additional prompt. I agree that it will be noise to people. There has to be something additionally that.. could the webxr folks agree to talk about this more and bring additional thoughts back to the issue?

Piotr: I want to fllow up with the UX team to see what they think. Let's go back to the discussion then. I think the way forward might be, I'll try to figure out if we can hae the same ways to bring this proposal to parity with getUserMedia, maybe it'll become easier to talk about to see what we can do above what getUserMedia does. Maybe there are ways to lock it down a bit further. I also want to say this api is strictly weaker than getUserMedia. You odn't get the choice of the camera. We dn't give you the same field of view that the camera actually can do. What the user sees on their screen is exactly what the site gets. Not the case with getUserMedia

Dan: documenting all that in your mitigations is really important

Piotr: if we got rid of getUserMedia we'd still have the tag meeting using webxr... We have to figure out how to live with this feature and how to make it work.

Dan: I hope that we can.


## Breakout B

Present: Peter, Rossen

Regrets: Sangwhan, Tess

### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov

Discussed, propose closing as dissatisfied. While useful for google.com, this feature is a foot-gun for the long-tail. We don't see why this shouldn't remain a proprietary feature.

### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov

Propose closing at plenary

### [Back/Forward Cache](https://github.com/w3ctag/design-reviews/issues/628) - @hober, @cynthia

### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @cynthia, @atanassov

### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov


## Breakout C

Present: Amy, Dan, Yves, Hadley, Special Guest Dom Hazael-Massieux

Regrets:

### [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo

Dan: don't know what the latest is [reaches out to Dom]

Dan: let's discuss more at the plenary.. Dom has closed it?

[a wild Dom appears]

Dan: what's the situation? Competing issues 609 and 625.. it looks like there's an agreed proposal for the future but an interim thing that Chrome is doing. We closed 625 saying we have concerns with an interim thing and we encourage them to do work in web rtc.. they said they intend to

Dom: for 609, a specific set of questions on the security properties, I closed because I think we've got convergance on the approach we need to take is one that requires opt in by websites to be captured, that's what's going to emerge hopefully soon in this new repo where this getViewportMedia spec is going to be developed. My sense, I will wait to see, but my sense is that there is now convergence in the web rtc wg in that direction. I'm not entirely clear whether the interim proposal is still going ahead. Their concern is that they don't think websites are going to adopt this new opt in mechanism in a short timeframe so they want to use this capture tab from google presentation that's going to fail in a large number of cases in a way that is obscure to developers and users. That was the motivation, how they intend to deal with that problem I'm not clear. I think the TAG pushback was extremely useful in getting more convergence in the wg, but I'm not sure where they've landed yet.

Dan: sounds positive. We shouldn't worry until a new review request comes our way?

Dom: yes

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris

[recap of joint session]

Amy: should raw camera access make a loud noise to alert everyone around you that you're using it?

Hadley: like camera shutter sound being mandated on phones in certain countries

Dan: what does Dom think of monday's session?

Dom: very complicated.. lots of useful things to explore and lessons to learn. Bringing more friction to devs or users so they gone way or the other.. the amount of fuzzing and preprocessing that a browser should do for privacy protections that are potentially very performance impacting, fuzzing realtime video streams would take a lot of resources. It's a balance between performance and privacy for the end user. Some of the work in terms of annotating video frames might have useful impact on this but it's so fuzzy at this stage it's hard to say it's a workable path. I agree it's an interesting issues and one that is worth further digging into, there are for sure lessons and patterns to be extracted. I didn't feel like we were yet in a position to identify these patterns.

Dan: anything else regarding prompts / permission requests we're missing? Is there a nuance about permission requests we should be thinking about more?

Dom: one aspect, not a clear picture, part of what has made the landscape evolve is that we are now exposing more compute intensive apis to browsers with webassembly, webgpu, soon webml, thsi changes the risk of what happens with data that can be collected. Handwavey discussions about the fact that these apis themselves should be gated one way or another. Don't know if it's a permission prompt, hard to understand, but making clear that they bring greater power so greater responsibility, so need greater gating. That was compunded by the fact that there was some research a couple of years ago showing that web assembly was mostly used for bitcoin mining. Not that i have a clear proposal in mind but there is a risk that we've been exposing end users to without them necessarily realising or understanding it, and whether there is things we could do to eithe rreduce that risk or augment the exposure of the risk to those who suffer from it. 

Dan: the idea of privacy budget has been floated.. part of the privacy sandbox thing.. but a general .. if you allow access to some very privacy infringing thing then you should be shutting down access to other things. That's a thing I've been trying to prompt webxr raw camera access folks in the issue but I don't feel like it's getting through. Should we be canonicalising that notion somehow better? Is that a ua specific thing?

Dom: my sense is that, gropus have their own ideas of constraints, the problem is that sometimes when you put all those things together they don't fit the way you want them to fit. In the privacy picture you might be designing great privacy mitigations in the very specific context of your api, but if you bring other apis together, maybe they mitigations don't work, or even if they all work tgoether they still leave huge gaps open because they were not designed as a whole. I feel like the TAG could come up with ways of exposing these holes that emerge from combining things together and proposing migitations that are not per spec or per domain. The privacy budget is one way. In general looking at how taking several specs together create..

Dan: unintended consequences

Dom: yes. Something like a budget sounds like a good way of managing this diverse set.. like how you manage a budget of several departments. Not sure which proposal is the right one. But the TAG looking ath the privacy budget of the platform is intersting

Hadley: been bouncing around in my head too. The idea of a privacy budget .. it's hard to think of it as a limited budget when you think about how much time and different ways we all interact with the web over such a long period of time. If I don't go outside that often I still go out lets' say once a day and over my lifetime that's a lot of exposure. It's hard to empower the user. 

Dan: not just the session, over all use

Hadley: not just in the silo of a specific feature, but in an artificial asusmption of constrained time..

Dom: feels to me like the TAG driving a conversation on this with UX and privacy people of various vendors

Dan: we do have privacy taskforce, we could push this into privacy principles. With webxr raw camera access, the question is if you have ideas on specific.. we haven't got past the handwavey thing of what other things could be turned off if this api is turned on. Is that a real thing? Are there other things that would dissuade without crippling developers from always requesting this api when they want to do AR

Dom: one reason developers wouldn't do it is if they get better perf out of the browser based version. They get a better service to their end users. In general doing live video processing in js or webassembly is always going to be worse in terms of perf. If the browser does the work and just gives you events or frames you need to do your..

Dan: or special marker detection api

Dom: that's already one aspect of the friction. The question becomes what are the use cases where what the browser provides is too limited but still valuable enough that developers and end users are willing to pay the performance and privacy cost. We'd need more information from who is doing game based ar and why they wouldn't transition.

### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss

Dan: something [new for us to review](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-942443043). Should bring this to attention of privacy tf

Hadley: confused about how site and ua are interacting. Is limit imposed by the spec or by the ua? How does the ua get to change the site's limit?

Dan: reference to privacy principles that is in a private repo that I haven't seen before..

Hadley: this goes through first part identity which ties into FPS.. but says third parties can be allowed access to a first party identity.. first party gets to decide with which third parties to share the identities of the user.. user should be in control of that rather than the first party.. concerned there may be some assumptions underpinning the broader issue that we would like to discuss.

Dan: i want to understand the standing of that document, the people working on trust token obviously think it has some standing. I think it may be superceded by the work Jeffrey did on the privacy threat model which has now become part of the privacy princples doc in the task force. If that's the case we should be getting those folks in trust token to reference our document. Even though it's hardly done it feels more comprehensive. 

## Plenary Session

Present: Dan, Hadley, Peter, Yves, Rossen, Lea, 

Regrets: Amy, Tess

### Some further discussion on WebXR Raw 

Peter: thinking more about the sandbox option... 

Rossen: are we too late?

Peter: not worth spending a lot of time locking the sandbox down


### [Media features client hints](https://github.com/w3ctag/design-reviews/issues/632)

Rossen: already in chrome, already shipping in stable. This feature allows you to pipe media features through client hints.  Through CH you can discover about the client via the headers.  You can save bytes on the wire.  Bigger players like this - this is cost reduction.  Media features - well understood, used and deployed capability.  Authors can figure out things like dark mode, reduced motion, etc... Client hints promoters say they can reduce CSS sending down the wire by using client hints. A dark mode CH for example.  Having bytes. Sounds great.  And along the way we've shifted a client-side capality to the server side. Round-tripping model of CSS through the server. The server has to be able to track and respond to user state. 

Dan: happens to me all the time with twitter in the morning as my device changes from dark to light mode. This is a real thing.

Rossen: Right. Some discussions on this... They say "this feature is only for larger web sites like google and only for power user".  Our position therefore is to close this as unsatisfied and move on.  I consider this to be an anti-pattern. Regardless of how it's massaged right now - regardless of small benefit to performance it doesn't justify changing the model to have to round-trip to the server.  It gets messay very quickly.  I'd like to close this as unsatisfied on the basis that changing the media feature handling and style sheet loading from the client side to the server side is not good. Should be kept on the client side. Also: narrowing the use to big players is also not great.

Peter: this can be used correctly and it will save bytes - only large companies that are in complete control can use this correctly.  

Rossen: the bytes saved are really tiny. 

Peter: for a site as big as google.com saving 5 bytes off the wire will be signifigant. If Google want this as a proprietay feature that they've already shipped, fine. But we don't think it should be exposed to the web.

Hadley: We have an etical web principle on this. 

Yves: it only matters for big companies.

Dan: fine with me.

Rossen: lea anything you heard that doesn't make sense?

Lea: No.

Hadley: [finds relevant ethical principle](
https://www.w3.org/2001/tag/doc/ethical-web-principles-20191204#control): 
"We will also build Web technologies for individual developers as well for developers at large companies and organizations. The web should enable do-it-yourself developers."
(It's under 'The web must enhance individuals' control and power')

Rossen: ok I will close with a closing comment.

**consensus recorded**

### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655)

Peter: this one we're happy with.

Rossen: right. here the thing is you want to be able to grab a capability and propogate it down to an iframe... the way you do this is for any nested iframe you can request to have a capability delegated.  For example giving it the ability to handle payments.  Making e.g. Stripe work in an iframe as a payment handler. Removing friction in payment is a key factor. Great use case.  This delegates down feature capabilities.  All the privacy control features as part of webappsec permissions policy.  Feature wise it makes sense.  By delegating the capability you delegate it to anything inside that iframe. They can further delegate it to someone else. Don't know if it's preventable.  The other thing that jumped out: as you read their doc - the privacy & security section - they're claiming that the capability doesn't allow provisions to sensors. Not true - it does allow camera, gyroscope, etc... you can delegate device access through that feature. I've asked them to document that in their security & privacy section. 

Peter: some background - the capabilities includes the user activation state... they did delegate the capability of user activation... that way we're not baking in the user activation.

Hadley: what's the difference?

Peter: not just the permission. some things require user activation.  You could delegate the permission but not have the user activation state.  becuase the parent frame got the user activation state.

Hadley: is it possible for a webapp with access to camera and microphone and had an iframe for advertisers - is it possible the advertiser would get access without me being aware?

Rossen: yes although they could that today.... 

Dan: some possibility here - getusermedia for example in a peer to peer webrtc session..

Peter: we could restrict the capability to delegate to a subset of capabilities.  

Rossen: i would be more worried about webusb or webshare...

Peter: parent frame...  Payment processing...

Rossen: the exploit path is to impersonate myfavstore.com - i fool you into thinking you're buying a new headset. ... if I already fooled you on the top level document if I give it to a subframe it doesn't really matter.  The payment capability is decent. the scenario is defendable.  When it comes to device capability we need to tighten down. Maybe we can tighten the allow list to only a subset of what's listed in [permissions policy](https://github.com/w3c/webappsec-permissions-policy/blob/main/features.md). 

Dan: i think that makes sense - don't open the floodgates to all the capabilities... 

Hadley: i second that.

Rossen: I like that. In that case my proposal is to keep the issue open and feed that back and see if they're ok with that.

Peter: their explainer mentions a few use cases - i don't think they want to expose everything.

Rossen: it's in the spec itself. [in Section 3](https://wicg.github.io/user-preference-media-features-headers/#feature-registry). 

Hadley: Adding that comment sounds good to me.

### [trust token]

Dan: [recaps breakout C]

Peter: [Punts to next week.]

### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss

### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov

Dan: very fundamental CSS issue about side effects...

Lea: they do make a good point about scrollbars.

[reviewing last comment](https://github.com/w3ctag/design-reviews/issues/624#issuecomment-923142901)

Rossen: christian basically says you can do this already with scrolling?

Lea: well we can't say if it's a fundamental rule of css if scrollbars also have a similar behaviour.

Rossen: I see christian's point. he's technically correct but the side effects we're talking about here that have the negative behaviour to users - 

Lea: element has style that is not a function of the current state.

Dan: [use of the word magic...]

Lea: magic - when behaviour cannot be explained with code or complex heuristics...

Hadley: It usually means we don't understand it. Or there are people who aren't good enough to understand it.

Rossen: or when it's too big to fit in a paragraph...

Rossen: not sure ... I am very familiar with where they're coming from ... it's something we did many years ago in IE9 - predict sizes of media - doing your layout.  Approx size, don't have to do a lot of compute .. saved a ton of battery and CPU - and then when you load them and you're close then the user sees no [movement].  From that PoV I sympathize.. and it's generalized.  So you can create a wireframe of layout that can then be filled in... Does it have side effetcs? it could if you get it wrong. glitches of re-layout.  I convinced myself that this is OK.

Peter: in general that style or layout state is left over from a previous algo is confusing - on the other hand I can think of some situations where we have to go there eventually. I'm OK with this.

Rossen: was curious if this has side effects to transitions in animations... 

Dan: set to *proposed closed*?

Rossen: sounds ok.

Rossen: I will leave the comment.



### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo

### [HTMLPopupElement](https://github.com/w3ctag/design-reviews/issues/680) - @hober, @LeaVerou, @kenchris, @atanassov

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

### Issue Triage
