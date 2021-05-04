## TAG Teleconference
##### 26-28 April 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-04-26](https://www.timeanddate.com/worldclock/converter.html?iso=20210426T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris
* [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @LeaVerou, @torgo, @kenchris, @atanassov
* [Partitioning Network State](https://github.com/w3ctag/design-reviews/issues/596) - @hober, @ylafon
* [WebXR Plane Detection Module](https://github.com/w3ctag/design-reviews/issues/620) - @torgo, @atanassov
* [WebID](https://github.com/w3ctag/design-reviews/issues/622) - @hober, @rhiaro

#### Breakout B (US / APAC) - [2021-04-27](https://www.timeanddate.com/worldclock/converter.html?iso=20210427T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov
* [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov
* [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss
* [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov

#### Breakout C (APAC / Europe) - [2021-04-27](https://www.timeanddate.com/worldclock/converter.html?iso=20210427T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews)
* [Declarative Link Capturing](https://github.com/w3ctag/design-reviews/issues/589) - @cynthia, @kenchris, @plinss
* [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo
* [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris
* [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris
* [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

#### Plenary Session - [2021-04-28](https://www.timeanddate.com/worldclock/converter.html?iso=20210428T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Dan, Lea, Hadley, Peter, Amy, Tess, Yves, Rossen

Regrets: Kenneth

##### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

Peter: domenic's feedback encorporated... 

Tess: wording of challenge global names... not clear on "new list" vs. "shortening it".  Not sure what relationship to other list is... some shared context is missing.  

Dan: any other items from [Leo's last comment](https://github.com/w3ctag/design-reviews/issues/542#issuecomment-825314747) that we could express an opinion on?

[group re-reading issue and re-digesting]

Peter: I'd like to take a deeper dive into it...

Lea: This is very big.

Peter: No direct access objects between realms.  Significant change to capabilities.  

Dan: punt it to the f2f?

Tess: not unreasonable.  It's a meaty enough thing.

Peter: [punted]

##### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @LeaVerou, @torgo, @kenchris, @atanassov

Lea: looked at filipe's response - i'm happy - but Ken might have thoughts. After filipe's response, some responses from ruben. Should this discussion be happening in our design review?

Rossen: maybe suggest to them that they take the discussion to [their repo].

Peter: let's move to breakout C?

Dan: meta point - at some point people discussing a specific technical issue should open an issue on the spec repo and continue the discussion there

Rossen: [leaves comment requesting this]

##### [Partitioning Network State](https://github.com/w3ctag/design-reviews/issues/596) - @hober, @ylafon

Tess: i want to investigate : to what extent does ths proposed spec match the partitioning that other ... already do. And whow can we find interop?  There's a storage partitioning discussion in privacyCG group... That may include networking state stuff.

Yves: knowing if the partitioning of network state.. different process, thread for each tab then it's likely that they will be partitioned by default... 

Tess: different browsers have different process architectures. Webkit has a network process that is distinct - so you could theoretically share network state between different browser parts.

Yves: ... many things that require buy-in from vebdors.

Tess: lots of moving parts.

Yves: goal is to avoid timing attacks - it's a good thing - but the question is : is there a consensus amongst browsers that it's a good way to do it?

Tess: will do more reading... 

Yves: we can leave feedback asking for evidence of interop and vendor buy-in...

Peter: foundation key... everything else is based on - should be talking to the people working on storage partition keys.  

Tess: some browsers double-key and some browsers triple-key...

Yves: having current partioning policies depending on caches, network state, etc...

Peter: confusing in their explainer: they propose using the 2-value key as a triple key. 

Tess: THERE ARE 4 LIGHTS!!!

Dan: 😂

Hadley: additional network partition key?

Peter: top level site plus the iframe site.  Network partition key is where you're using the key.  Http cache partitioning ... [in some parts] double keying seems like single-keying...

Tess: I'll do it. 

##### [WebXR Plane Detection Module](https://github.com/w3ctag/design-reviews/issues/620) - @torgo, @atanassov

Dan: I left feedback, asked how it fits with HIT testing and for more examples and use cases. The requester has responded well. Not HIT testing, but did respond on additional use cases and quantization issue. Still more we're waiting for.

Rossen: since last time we talked, nothing much has changed. Discussion last time was around privacy and what that means for users. Through such API you can pretty quickly and easily map out somebody's physical environment. What does that mean from a privacy point of view? If I use this does company x all of a sudden have a map of my office or bedroom? Don't believe this was addressed.

Dan: one way they say they're addressing that is through quantization of planes. Could make it less possible to fingerprint you based on how high your desk is..

Rossen: might make it slightly harder. The actual API set they are bringing in is pretty straightforward. 

Dan: note that the phrase quantization still does not appear in the spec. [leaves comment](https://github.com/w3ctag/design-reviews/issues/620#issuecomment-826989516)

Proposed comment:
`Hi @bialpio - we're just taking another look at this this week... Still missing the connection to hit testing and some additional info regarding the privacy & security. Do you want to ping us again when you're ready for us to re-review?`

Rossen: re-read paragraph 6 in the spec which is on privacy and security, still not addressing it. Recognising the issue but not necessarily proposing concrete ways of why this is a non-issue or how it will be mitigated. Instead just saying general XR concerns apply. Look at general XR anchors module.

Hadley: is it possible to do all of that on device or in the user agent? To keep the information from leaking out of the users control. If we can keep it within the user agent as opposed to expose it throug the API such that the application can work with it rather than....

Dan: part of the idea of the API but they don't do enough to explain how that happens. That's part of the issue with the security and privacy thing, not really going in to detail on the abuse cases so its' not clear how the design doesn't allow for the information to be misused. 

Rossen: we had similar concerns with hit test but they said at the time hit test is completely contained in the user agent and the only thing you get back is the object that you hit tested, not anything identifying about it. This one goes one level further, or more. 

##### [WebID](https://github.com/w3ctag/design-reviews/issues/622) - @hober, @rhiaro

Amy: really big - one thing to note is that they didn't do the s&p questionnaire yet but they do have a threat model document. Probably a good idea to fill it out?

Tess: yes - it's to prod them to have those thoughts.  so if they've already done the work then filling out the questionnnaire should be easy for them.

Amy: i couldn't map the things they've comment into the s&p questionnaire... They also said they want our feedback on the problem space more than the solution... 

Tess: it's kind of tricky... part of the design reviews is an implicit assumption that the problem you're trying to sovle is worth solving... so we tend to focus on the how. this is a bigger picture question.

Tess: the web is littered with previous attempts to solve things in this space.  some of them are reasonably successful and some of them less so.  given the fact that there is so much prior art - it does seem prudent that someone who is trying to do this tell us why this is going to be different this timne. why previous solutions didn't work...

Peter: they are looking at how existing systems are breaking given changes in the browsers...

Peter: someone should look at the history.

Dan: I'm not sure the is a right way. "identity" is a very philosphical concept, very slippery notion. What do people mean.. there are so many edge cases, it's such a complicated topic, and a human thing.. mapping this ill defined social construct onto technology is not very .. possible. 

Peter: scope of this issue is there are existing systems, openID, SAML, and with other changes with third party cookies and whatnot some of the capabilities of these systems are breaking More specifically how do we continue with the improvements in privacy without breaking existing identity systems.

Amy: by inserting the browser into the flow..

Peter: some examples of monkeypatching other things.. fenced frames

Rossen: a good one to take to a dedicated discussion with additional prep ahead of time. Either as a separate breakout or f2f. Aligned with Peter. It has a great summary of a lot of the pain points, it is doing a good job of staying as neutral as possible and focussing on technical challenge and solution. We should give it time and provide additional feedback. 

Dan: I'm up for a separate breakout

Peter: figure out next week and invite sam

Rossen: we should probably have a session ahead of time that will focus and get us on the same page, so if we want Sam as part of the discussion we will be ready. That can be during the face to face.

Dan: that sounds different than one of our two person breakouts

### Breakout B

Present: 🦗🦗🦗

Regrets:

##### [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov

##### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov

##### [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss

##### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov


### Breakout C

Present: Amy, Ken, Dan, Yves

Regrets:

##### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @LeaVerou, @torgo, @kenchris, @atanassov

Lea: wanted to get Ken's opinion - personally I'm satisfied with [filipe's response](https://github.com/w3ctag/design-reviews/issues/563#issuecomment-782994485).

[replaying Breakout A discussion on this...]

Ken: I think this is good enough. They seem to have thought about it. I'm good with this.

Dan: "propose close" then?

Proposed comment: `We took another look at this during this week's meetings, and we are happy with the direction this proposal is going, so we are going to go ahead and close this. If/when there are substantive changes, feel free to open another review request. `


##### [Declarative Link Capturing](https://github.com/w3ctag/design-reviews/issues/589) - @cynthia, @kenchris, @plinss

Amy: privacy & security questionnaire in a google doc.

Ken: I also get access denied.

Dan: it should be a markdown file in the WICG repo along with the spec

Ken: about to ship? I think they already made changes based on my comments.

Dan: looks good to me

Hadley: makes me uneasy in the same way that changing forward and back behaviour makes me uneasy

Ken: which they're not changing

Hadley: we did talk about that at the time, uneasy rather than full on problem

Dan: one thing I like is that it's not proposing a new JS API, the declarative aspect. It's extensions to the manifest file. 

Yves: I'm sure this is a use cases in miniapps, some coordination here would be good. Especially as there is a WG on that.

Dan: this goes to the manifest file...

Ken: this is going to go into incubation, Marcos does not want to add anything to manifest that isn't implemented in browsers

Hadley: just for navigating to URLs within the applications navigation scope?

Ken: if you have installed a PWA it will focus instead of opening another window.. give you control to reuse existing tabs

Hadley: one reason I use web apps vs native apps, eg. twitter, if I'm clicking on a link I'd prefer to read the article in the brower rather than in twitter's web view

Ken: this is the same origin. Twitter would create another window that would embed in iframe, it should open in a separate window. You can always right click and say open in new tab/window. I understood you could change the default on ChromeOS.  Right click > always open in new window. You can control it yourself, that's nice.

Hadley: I like the scope of this.

Dan: in an ideal case this spec provides a more web like experience for web apps that make use of the manifest. What you said about twitter is why I use twitter as a PWA as opposed to the app, because I want everything I do on twitter to be in the same context as my other web browsing. I'm asking a question about visibility of browser engines.

Sangwhan: I vaguely remember seeing something analogous to this in a miniapps spec

Ken: developers and people we're talking with doing PWAs all want this

Sangwhan: I'm sure this is useful for many people

Ken: for creating app like experiences on the web it's very useful. Flexible way is to use service worker and give you full control of windows inside your domain so youc an focus them and do whatever you want. But that's not coming now, this is in between, 80% or more use cases.

Dan: wait to hear back about S&P questionnaire and check back in plenary.

##### [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo

Sangwhan: the API itself is similar to the webrtc.. I don't see an issue with the design itself

Dan: could be better at articulating user need... but they do say funny hats in the spec.

Yves: they say in the issue that a major concern is are they using real streams JS level or webRTC streams that are different? Issue of homogenisation of the web platform by avoiding using too many kind of things doing the same thing.

Sangwhan: ongoing problem with webRTC in general. A bunch of stream-like thingies but due to interoperability they can't change it. Early effort to transition over to streams at some point but that project sort of died off. 

Yves: Apple arguing that they should use transform streams from the javascript streams. Makes sense. In 'further details' it's the major [unresolved issue](https://github.com/w3c/mediacapture-transform/issues/4).

Dan: having multiple things which do the same thing is complicated and creates bloat

Sangwhan: the problem inside webrtc is that the damage has already been done and it's hard to unship these streamlike thingies

Dan: we could say 'ideally we could see convergence happen over time' rather than change this thing now

Yves: they may provide an API that would be compatible with regular streams

Sangwhan: aside from that i don't see why we would keep this open ... I can comment but I have to digest this discussion

##### [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris

Dan: Dominic [commented](https://github.com/w3ctag/design-reviews/issues/605#issuecomment-824291002) 6 days ago on the topic of whether the URL bar should update immediately... sites today delay updating URL until after data is fetched and DOM updated..

Ken: they are waiting to hear from authors

Dan: should we keep this open?

Sangwhan: last week we suggested we might want to have a separate call? I was supposed to arrange

Dan: if we've got something really helpful it's worth having a separate session but looks to me like they've got it in hand. He's spoken to people at Mozilla.

Ken: I don't have anything else

Sangwhan: I don't have anything at the moment

Dan: let's talk about closing in the plenary or maybe waiting on updates and rereview at some point

##### [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris

Sangwhan: contentious.. get serial number... for corporate things.. when it's not your computer. you list origins where this API is enabled and it's propagated down to the browser. Your enterprise administrator allows that. 

Ken: internal sites. Can they go and do that for like youtube? why would they?

Sangwhan: nothing that blocks you, that's an implementation detail

Lea: what are the use cases?

Ken: IT managed laptops. We have specific sites that can do something. is it about limiting or enabling what sites are allowed to do?

Sangwhan: I've seen one case which has the software license portal and it gives the serial numbers that you're supposed to use for your installations. If you don't have access based on the serial number of your device it won't let you download it. 

Hadley: would that have to happen in the browser?

Dan: they're moving all of their intranet applications to the browser

Sangwhan: alternative is as a native app

Hadley: that might be safer

Sangwhan: this is uncomfortable in many ways. Undefined aspect is centralized management - probably an implementation detail.

Dan: the people in adtech space are agitating for unique IDs for everyone.. what's to stop them taking advantage of this so that ...

Ken: knowing enterprise it would be opposite, they're never going to do that

Hadley: there are some abuse cases

Ken: I'm sure there are abuse cases

Sangwhan: another use case is the device is preauthenticated to automatically log into certain tools, no ID or password. Knows serial number or host name

Dan: feels like we should say this is not really the web... this is the enterprise software stack. Enterprise specific features for enterprise customers with special APIs can be shipped in Chrome, it's not the web

Hadley: I hear what you're saying.. a lot of it I'm not sure I'm okay with it. If they are fundamentally making changes to the UA and how other parts of the web are working w'eve got to have an opinion. 

Amy: last time we talked about this we talked about if only Chrome ships it then it constrains what browser people in corporate settings can use

Sangwhan: either everyone implements this exact API that Chrome ships or we let it become a standard

Lea: interest from other browsers?

Sangwhan: pretty sure Mozilla would not

Ken: pretty sure Edge would

Hadley: MS target market..

Ken: if I want to do something at work I use my IT laptop and it says 'managed by your organisation' and there are a lot of settings you can't even change

Hadley: I wonder if we're in a minority, rebelling against enterprise control...

Sangwhan: should it be a standard?

Ken: is MS interested in this API? Same across edge and chrome makes sense. or do they have any concerns.

Dan: are there certain elements we would like to question? What is really necessary? A more webby approach?

Lea: I was missing a list of use cases for the particular bits of information. What use cases are enabled by returning the serial number? there is nothing in the explainer.

Sangwhan: there are ways to do similar things to the use cases they need for enterprise but I think it's for convenience

Lea: we need to know what problems they're solving

Hadley: it lists two but implies others, buried in detailed description [reads] .. what worries me about these is that they deliberately break the sandboxy nature of the user agent.

Sangwhan: not sure I buy the configuration, that's more convenience.. you could preinstall a client cert on the root of every device which would allow you to uniquely identify each device. There are different ways to do this. It's just more work.

Hadley: worth saying. Good alternate solution.

Sangwhan: same applies for personalisation.. 

[discussion of certs at OS / browser level]

Hadley: why does this need to go through the web?

Lea: what's the alternative? Don't we want web to compete with native?

Sangwhan: visualbasic.NET?

Amy: we don't want the web to compete on the field of creepy corporate spy-ware. That's not the future we want.

Dan: +1

Sangwhan: instead a fetch on localhost...

Ken: everyone does that at some point

Hadley: feels this really belongs in the OS and at the network level, and push it to IETF

Sangwhan: I don't have a solution

Lea: mixed feelings as well

Dan: resonate with not wanting web to compete on field of spyware.. when you're an employee and your machine is provisioned by taht company, and you oepn your web browser, you still have ane xpectation of privacy - visit your bank website, check on your dentist appointment, perform functions related to your daily life, use your computer during your offtime even if you're in a job where your time is managed.. you still have an expectation of privacy when it comes to use of the web. We need to be aware of that.

Ken: even today people install extensions on my IT laptop, on edge and firefox, that will monitor whatever site I visit, whatever I do, because there are web extensions APIs and I cannot remove them or turn them off. It's the same at other companies.

Dan: I would not be okay with that.

Ken: its unfortunately very common.

[dystopia discussion]

Dan: it might be the right thing to say why do you want to do that with the web

Sangwhan: I could ask.. the main thing seems to be to uniquely identify the device, solvable with client cert. Ask the reason they chose this design?

Hadley: sounds good. Add that it brings up some concerns if you want. 

[discuss more at plenary]

##### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

Hadley: I'm not sure they answered Yves' question. diff between storage buckets and partitioning?

Yves: organise buckets by yourself rather than by each file and resource..

Ken: control your own storage inside your own application. Like caching. You can say which is privacy sensitive..

Yves: or a bucket you pin in your cache.

Ken: per user per site. Site is in control. UI that says you can delete cache but have a bucket you don't want to delete. Site has more control over how caches are stored. Good with regulation, some data needs to be stored and treated in a specific way. Eg. right to be forgotten.. want to remove private info but not necessarily cached images.

Dan: positive from firefox, no signal from edge or safari

Yves: fine to close

### Plenary Session

Present: Amy, Peter, Ken, Dan, Lea, Yves, Tess, Rossen

Regrets: 


##### Breakout Rollup

Breakout A: Realms, punted; css scrollbars - left a draft comment; Lea wrote in breakout C [consensus to close with lea's comment]; partitioning network state - tess to leave a comment; webxr plane detection - we left a comment and no reply yet; webid - we will focus in on it at the plenary; 

Breakout B: 

Breakout C: 

**Declarative Link Capturing** proposed feedback:

'Hi <>. Ok thanks for that. For the security & privacy questionnaire, can we understand that the answers to the other questions is 'no'?  Also just to note: you list WebApps as a destination (presumably because this will become part of webapp manifest) however in order for that to happen there need to be multiple implementations. So I would encourage you to have those discussions with other browsers and try to generate some additional support if you want to take this out of incubation.  We also think this activity needs to be coordinated with the parallel work going in in this area in the MiniApp working group. However in general we're very supportive of this feature and would like to see this move forward.'

**Managed Device Web API**

Dan: [summarizes]

Rossen: will chat with folks... 

Tess: I will also chat with folks...

**Storage Buckets**

Yves: will close now.

#### Discussion of AC meeting outcomes


