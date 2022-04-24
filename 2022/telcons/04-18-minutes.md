# TAG Teleconference
#### 18-20 April 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-04-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220418T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [Cookie Expires/Max-Age attribute upper limit](https://github.com/w3ctag/design-reviews/issues/729) - @ylafon, @hadleybeeman
* [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

### Breakout B (US / APAC) - [2022-04-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220419T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou
* [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [FYI Review of CSS Fonts 4 `font-palette`and `@font-palette-values`](https://github.com/w3ctag/design-reviews/issues/719) - @LeaVerou, @plinss

### Breakout C (APAC / Europe) - [2022-04-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220419T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion
* [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman
* [FYI - MediaCapabilities API for WebRTC](https://github.com/w3ctag/design-reviews/issues/720) - @cynthia

### Plenary Session - [2022-04-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220421T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Amy, Peter, Dan, Lea,

Regrets: Hadley, Yves, Rossen

### [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov

Peter: browser mediated take on SAML...  trying to fix the things that will break when we lose third party cookies... It smells like an early review.  They have a manifest - browser calls an identity provider for basic information like branding.  They should add light and dark color modes and follow some of the examples of the webapp manifest. Concern: they have an accounts endpoint which could be abused... Not sure how to get around.  The browser can hit an IDP and ask "does this user have an account on this service" - not sure how they identify this.  A nonce?   They say many places they haven't worked out the details...  Needs to be designed so crawlers can't just scrape all your accounts.   Renamed evolutiuon of WebID...  

Dan: **todo: link to WebID discussion with Sam Goto**... 

Dan: I felt quite positive about the initial WebID propsoal.  

Peter: overall the direction is good the approach is good.. reusing as much as you can... you won't have to rewrite everything if you're building an IDP...   We need more data.

Peter: SAML and OIDC require public key crypto ... don't see anything here doing that.  They do also have section on privacy.. will look at that more and leave some feedback.

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Lea: generalisation of the prefetch/prerender attributes.. using json blob to define these rules in a sript element. Weird. There is precedent. Unclear .. syntax is confusing. source list / source document.. things to be said about syntax. Score is unclear how it's used. Question of do we want this logic to lie in a script element as json or should it be an html based syntax. Motivation - I am convinced, mentioned example of quicklink library that determins which links to prefetch automatically. Whole process is explicit, authors need to duplicate links to prefetch in the head. This allows the to handle this en masse to some degree. More extensible because its json, can add more properties. Main point is do we agree that this is a problem that needs to be solved, and is json in a script element a good way to solve it? Low level stuff we can talk about another time, or just leave a comment. I don't know any history about this.. seen speculation rules in our agenda a few times.. some background?

Dan: based on speculation rules? Leave comments and questions..

Lea: [will leave comment]

### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Dan: thoughts on turtledove: it's in WICG. Why isn't it in Privacy CG?  Where is this going for **standardization after WICG**?  Says "unknown" but what is the thinking?  Its not clear from the link provided on **multi-stakeholder** descussion whether there is any interest from additional implementers or stakeholders in this API.  Can they please be more specific?  It's not immediately clear how this relates to the **topics API** since it looks like this is trying to achieve the same aims but there's no reference to the topics API in the review request or the explainer.  It looks like this proposes each ad request be doubled - one request for a contextual ad and one request for an ad "indicating an advertiser-identified interest" - at a minimum this would would double bandwidth requirements for ads which would be problematic from a power consumption / network usage PoV.  As I understand it, the *contextual* request and the *interest-group* request are sent at the same time (and the browser decides which one to display). However the *interest-group* request does not contain contextual data such as the URL the person is visiting.  This is claimed to be a privacy benefit but couldn't the ad network easily correlate these requests considering all the additional metadata they might have access to including timing and IP?  (They have some mitigations listed... )  The idea of an **on-device auction** is worrying from a power consumption perspective especially when the user is likely on a smartphone.   It seems like they are thinking through some of the privacy issues - however the proposal is rooted in "how do we support the existing ad ecosystem".

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/723#issuecomment-1101573160)

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

"the API’s utility isn’t yet clear"

Amy: they have pre-empted our FLoC questions for Topics

.... loads of issues probably worth reading

... Ad topics eventually sourced from a third party (todo: who?)

... Browser classifies sites.. sites providing their own topics is an "open question".. interesting to think about variation in ads across browsers then?

... 5% random noise, for plausible deniability. Attempts to avoid cross-correlating user between sites. 

... Story about sites accumulating topics? Even if only one per week. Aggregating topic data with existing user data (from fingerprinting, cookies, etc)?

... Can sites opt out of being included in the mapping to topics? (Other than by havin an 'opaque' host name) - yes (header, and also have to call the API). How many topics can map to a single site?

... Definite improvement over floc.. more transparent

... Risks with colluding sites (documented). Risks with unintended correlations of topics to sensitive topics.

... "better for user privacy than cookies"

... Lots of open questions under discussion

Amy: definitely better than FLOC.  It's in the private advertising group.  Tons of discussion on the privacy stuff.   It's comletely different to FLOC.  No cohorts.  Ways it can be abused but it's documented and discussed.  It seems better. Ton of open issues. I'd like to look through a bit more.  The direction this is going is saying there's no privacy-preserving way to do targeted advertising ... so maybe they should stop trying?

Amy: up front there are a lot of mitigations - like 5% random noise (less of a fingerprinting vector) - list of topics is human-curated and transparent and would ship with chrome.  

Peter: a lot of evidence that targeted advertising can be used for political purposes... to negative effect. Also questions on effectiveness in general for commercial purposes.

Amy: question about multi-stakeholder.  

Peter: i'm wondering if we shouldn't have a finding "stop targeted advertising."  

[discussion about legal future of surveillence for advertising, collection & sale of user data]

Lea: what about websites that can't afford another business model?

Peter: not saying ban advertising altogether

Dan: whether or not it's correct that targeting affects the real value of an ad, whether it influences someone's behaviour, it is the case that targeted ads make more money. Still an economic issue. If targeted ads went away tmorrow there would be a certain number of websites that have a big income drop. It's a concern. Publishers would not aagree with the statement that we should ban targeted advertising. Robin Berjon's take would be interesting.

Lea: unpopular opinion - if targeted ads could be done in a privacy preserving way, it could be better for users - as long as it's opt in, users can see ads that are relevant

### [Cookie Expires/Max-Age attribute upper limit](https://github.com/w3ctag/design-reviews/issues/729) - @ylafon, @hadleybeeman

### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

**bumped 3 weeks** as Elad got back to us and said it was still in the pipeline.


## Breakout B

Present: Peter, Sangwhan, Max

Regrets:


### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou

Question if innerText causes style calc/reflow like Node.innerText does, if so maybe better served by an async method?

We have quesitons abou how innerText maps to the range when adjustments are made, e.g. if an end point is in a hidden node, and the enpoint is moved, does it move to the start/end of the hidden text + offset? 

### [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

Use case for font blocking is replicating controls already available in CSS: https://drafts.csswg.org/css-fonts-4/#font-rendering-controls-introduction

[Blocking is bad](https://w3ctag.github.io/design-principles/#avoid-render-blocking) do we really want to add more mechanisms to do this arbitrarily?

Discuss in plenary

### [FYI Review of CSS Fonts 4 `font-palette`and `@font-palette-values`](https://github.com/w3ctag/design-reviews/issues/719) - @LeaVerou, @plinss


## Breakout C

Present: Amy, Max, Sangwhan

Regrets: Dan


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

Max: authors have replied, regarding authentication mechanism. We can discuss whether it's clear enough.. 

Amy: do you know if they connected with the Web App Lifecycle people?

Max: had these discussions before, authors left comments to make sure they're aligned, that's the idea

Sangwhan: not good... checks the origin through an intermediary. A developer can claim an origin, and it's entirely up to the mini app platform to determine whether or not the developer is worthy of claiming that origin. That sounds scary. The problem is the verification depends on - it's not a chain of trust - it's giving the inermeidary unlimited powers on whether or not a certain developer can claim an origin or not. Let's say for example, example.com - I claim it's mine, and I claim my mini app is from that origin. The app store will say I trust Sangwhan, I'll just give him access to example.com,e ven if I shouldn't be example.com. That destroys the origin model because the mini app is effectively operating as if it is on example.com, and al the cors validation is going to be on the assumption that is example.com

Max: in the .. for example one mini app is going to apply to register itself onto the app platform, the platform should do some authentication about the authenticitiy of the claimed origin. Does that solve the concern?

Sangwhan: how does the platform do the authentication?

Max: maybe should be done by.. what we do in application store is the same problem..

Sangwhan: no it's not. If the mini app claims to be example.com and makes a request to example.com on the web it will be treated in same origin. In a native app you don't have the cors model, so it's not an issue. If you disregard cors and consider mini app non-web it's fine, but if it has to account for cors this is not good. This is why it took so much time to get bundled exchanges and signed exchanges out, it's a very hard problem to solve. Signed exchanges somehwat lets you do that, it's how it should work, but signed exchanges are ephemeral so you can't use it for a mini app. Bundled exchange you might be able to pul it off but have to talk to packaging folks. If it's delivered in that way then the authenticity of the orgin claim can be guarnateed, unless you're under a dns attack.

Max: that is probably one way.. just thinking about what if .. as one example, for the application store, the platform also needs to check the authenticity of any backend server of the application, so maybe they can use similar mechanism to do that?

Sangwhan: authenticity of the backend application?

Max: for many mobile applications they need a backend.. so when the app developer uploads their app onto the store, eg. google store or iOS store, in their applications they need to talk with their backend server. Similar in this case.

Sangwhan: there's no CORS there. It's native applications, there's no origin model. If you want to treat a mini app as not aprt of the web.. if you lift CORs and the origin model you don't have to care about it. It's a fundamental question of if the origin model exists, in which case it should follow web platform security conventions. Letting the mini app claim an origin when it's offline is in this kind of way is very risky. 

Max: former case.. more like application model, not like web model

Sangwhan: then I don't know why we should be reviewing this. Is it part of the web or not?

Max: that will depend on definition of part of the web.. 

Sangwhan: miniapps run in a browser runtime, therefore the origin model is in there. I'm trying to understand is it going to operate in conjunction with the web's origin model or not. It seems like they're saying they're checking the origin, so presumably there's an origin model, I just don't understand how it's going to work, in confjunction when the paplication is considered online. I't snot an offline application right? It makes reuests to some api service to get data and return it back? What is the origin here, is the main question. example.com makes a mini app and example.com has an api. example.com's api with cors rules only allows access from example.com. Will the mini app have access to this? Should it have access to this? if so how? If it has access is it by disregarding the cors model, or because it claims to be example.com, as with bundled exchanges for example?

Max: my understanding is the mechanism when the mini app registers onto the platform the platform will bind the mini app to certain domains they claim, and the platform will check authenticity of the domain, whether it's owned by the mini app developer or not. When this binding happens the mini app platform can follow the same origin principle to only allow the correct mini app to access the certain domain.

Sangwhan: can this be done in the same mechanism as we do exchanges? Bundled exchanges, signed exchanges?

Max: I'm not sure if they use bundled exchange mechanism or not

Sangwhan: don't need to use it, use the signing mechanism to verify authenticity. 

Max: Maybe that can improve the security. Probably useful.

Sangwhan: right now it's up to the app store to decide, and that's a scary model. it depends on whether the app store is prudent and trustworthy. 

Max: yes. That happens for other application stores also.

Sangwhan: but it's not the case for the web. That's where I'm concerned. If you disregard entire security model of the web then this is fine. Also any link you visit in the mini appp will operate under the same scary security model

Max: mini app itself follows the same origin principle, but for the authenticity check part this is done by the mini app platform. But for the application it will follow the same origin principle

Sangwhan: I don't think having the app store / platform signing off on it is a good idea

Max: maybe that part does not belong to the web standard, but for the mini app itself still follows same origin, only the mini app application can access the backend server, no other mini app can

Sangwhan: if you change the model like that, the same origin principle doesn't hold the same kind of guarantees or safety that we have in the past. That's the part where I'm concerned. Having an origin backed model like how we do signed exchanges is probably better solution than having an intermeidary. There are ways to do it.

Max: leave a comment?

Amy: is this a centralisation issue?

Sangwhan: worse - the intermeidary can act as a man in the middle to.. we have to .. mini app model puts a lot of trust on the app store. It can issue any number of apps claiming any number of domains. Has the power to issue an app claiming the origin is google.com

Max: as a developer if you have your own dns server you can also do that. This is not the problem web standards can solve.. a regulation problem. If I buy a DNS server I can put google.com..

Sangwhan: that's man in the middle. But you can't get a cert issued by a cert authority

Max: for the mini app case it will not get a certificate either. Technology cannot prevent that. That is what happens

Sangwhan: this is solveable, it's been solved. Signed exchanges and bundled exchanges is that exact mechanism. At the origin the package is signed, and it's passed through non trustworthy cdns and validated by the client.

Max: just saying for the dns examples you mentioned, that is a different case. I agree that we can suggest to the authors to consider the packaging security mechanism..

Sangwhan: I'm very concerned that this gives too much control to the app stores. I don't think 

Max: I don't understand.. app store model works in the real world. App store is not part of the standard. 

Sagnwhan: origin alidation must be part of the standard. 

Max: mini app does the authentication with the origin

Sangwhan: the end to end validation needing an intermeidary, that's the part that's..

Max: only the registration process. That is not in the mini app spec itself, that is an operational thing or business model thing. Jus tlike what application store does today.

Sangwhan: i disagree. This security model is not something that works or that we should be promoting.

Max: need to discuss concrete problems

Sangwhan: there are technical solutions to this that are not being evaluated

Max: concrete uestion first. We can ask the authors to consider the packaging security mechanism. But the whole packaging mechanism... google and ios..

Sangwhan: there's no same origin in native apps.. I'll leave a comment and we can discuss in plenary

Amy: Anything with a centralised point of deciding which apps do and don't get to exist.. raises red flags for me. And we see that in practice with native app stores today, too.

Sangwhan: and on top of that we're breaking the security model on a web browser based runtime

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion

Max: Sangwhan had questions, hasn't put them on github yet. Had a discussion and he summarised further questions to ask

Amy: did he put them in slack?

Max: ah yeah.. about the hierarchy of selecting devices and power consumption concerns and information .. 

Amy: you can post them?

Max: we can wait for Sangwhan.. I'll remind

Sangwhan: [appears] I will do that

### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion

Amy: looks like waiting for response

### [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman

Max: only questions I have, seems only to support IP based devices because it .. they can be reached by http.. assumption.. but in real world there are many IoT devices that don't have IP addresses. Not a problem, if this specs puprpose is only to work for IP addressed devices it's fine, but want to mention that in the real world there are many iot devices that don't have IP addresses. Maybe that is a question to be asekd.

Sangwhan: last time I read this it was JSON and IDL things. Is it still the same?

Max: JSON based to describe the properties of the IoT devices. How to get .. and how to control devices, how to get notifications

Sangwhan: Last time I read this document it was more like a protocol document than an API, is that still the case?

Max: I think it's not an API. Kind of a format. Data model to describe IoT devices so the developer can use that data model to automatically gather sensor data. Data format. Not a web platform API. Doesn't require the browser to implement that. Only the IoT devices developer or platform vendors.

Sangwhan: I don't have much to say on this.

Amy: security implications?

Max: they have a security mechanisms .. in the explainer has some.. and in getting started section

Sangwhan: how does the security model work?

Max: in the explainer, very simple example. JSON field with a thing description.. security measures user name and password based. Password in http header I think.

Sangwhan: no origin protection?

Sangwhan: given this device is accessible, what is the CORS equivalent mechanism here? I'm not understanding

Max: different from web platform. In this example the devices is a web server I think. It will have an IP address..

Sanwhan: this device, according to what I see here, has a web server, has https.. does this mean i'ts only accessible locally? Or can you make ..? I think the question is can an arbitrary application make a query to this device and turn off your light?

Max: in my understanding security mechanism is that the light will have password protected and only authorised applications have the password. When you send a query or certain command to the light you should provide the password. 

Sangwhan: so if you're accessing this from a weba pplicatin, you have ten lights with ten different passwords, you have to type ten different passwords?

Max: in the spec they have different options. That's one option. Basic authentication option. Also key based security model.

Sangwhan: I don't see anything about auth in the spec, we should ask that question. I don't see how you'd do any reasonable protection here. I don't understand how the interaction with the weba pplications are supposed to work here. Haven't read carefully.

Max: my understanding of how the web applications interacts with iot devices.. the devices have three.. properties, stauts is one example of properties.. the web application can send an http get on the url, status url, to get status whether the light is turned on or off. The second is action - similar, the web application sends http post to the action url. Last one is event - here the if the light has something wrong, that can send a notification to the weba pplication, using the http protocol. The iot devices in the sepc have three services. For other devices it may be different. 

Amy: also haven't read closely, but seems like the auth may be orthogonal.. possibly in another spec somewhere

Sangwhan: because it's not defined.. I don't know.. It's saying you consume a url.. no reference to cors in this entire doc, very concerning

Max: this spec doesn't require the web browser to do anything. Ony the iot devices platform vendors should implement this

Sangwhan: why is it called web of things then?

Max: I guess maybe they use semantic web or web technologies to do this.. 

Amy: looks like a small part of a bigger ecosystem.. other specs that go along with it to make it make more sense, not standalone

Sangwhan: I don't know how many specs they have. Last time I looked at at web of things specs they were more like device to device protocol, nothing to do with the web. Don't know what has changed. I will revisit when I have read the spec. 

### [FYI - MediaCapabilities API for WebRTC](https://github.com/w3ctag/design-reviews/issues/720) - @cynthia

Amy: what's with "FYI" in the subject line..?

Sangwhan: separte spec called media capabilities and they're basically just attaching this to webrtc from what I see. Looks okay. I'm just going to close it.

## Plenary Session

Present: Peter, Dan, Amy, Max, 

Regrets: Hadley, Yves

### Breakout Rollup

#### Breakout A

Posted some comments, some responses..

#### Breakout B

Peter: Navigation api has a lot to read, need to bump, but chrome is shipping soon.

Sangwhan: WebGPU - will write a closing comment and post questions

Peter: No response to questions on Range API. Weirdness with innerText attribute, gets text of range but skips anything hidden, which seems like it would force  style and layout recalc. Methods to adjust input of range and it's not clear how it will work if it touches something hidden. A bit underspecified. The blocking thing we wanted to talk about..

##### [blocking](https://github.com/w3ctag/design-reviews/issues/727)

Sangwhan: the more I think about it the more harmful I feel it is. What this tries to do is introduce a attribute to async loaded subresources to block the render. To prevent unstyled flashing. Which I an understand why they want to do it but I'm not so sure if the gains outweigh the harm. The risk is eg if a resource marked as blocking is incredibly heavy and you're on a slow network. Right now you get some progressive rendering, you can read unstyled text. Another thing is if an ad script is 'blocking', which it shouldn't, but.

Dan: who gets to say what's blocking?

Peter: on the tag

Dan: for instance publishers or websites could be compelled to set it as blocking by advertisers

Sangwhan: advertisers have every incentive to set it to blocking, because it guarantees they will have an impression. If the user quicky navigates away now they won't get an ipression. It would be in ad networks greatest interst to set it as blocking, but taht would be harmful because its a massive pile of js that is not relevant to the content.

Amy: how would that play with ad blockers? Would nothing load?

Sangwhan: the fetch fails if there's an ad blocker. If the fetch fails in their proposal then it's fine, shouldn't block it.

Peter: and they do accept you may still want to time out. Their use cases are weak. One is loading a font. Webkit used to do this with 30 second timeouts on fonts, and users were staring at blank pages while the font loaded. That was bad and you can control it with css, why add something else?

Sangwhan: if you do this with cjk fonts that's going to be fun... they're like 5mb

Peter: they can be. They give a use case of using a script to inject a stylesheet and you want it to be blocking. Seems like you're already kind of past the..

Dan: aren't all of these cases antithetical to the spirit of the web?

Sangwhan: it disobeys our previous stance on making everything async friendly. Suddenly this is adding a big block of sync in an async system. Feels like it would be abused too much.

Peter: example of wanting to block render on an async script load.. seems completely counterintuitive to me.

Sangwhan: if it's just to prevent the flashing of unstyled content, a weak story. The design should be revisited.

Dan: Sounds strong enough to leave feedback along those lines

Sangwhan: one way it could be approached with this design is the site does that but the user is presented with a dialog that indicates preference... seems like too much..

Dan: if the use cases are as weak.. who is asking for this? What's the pressure?

Peter: what user need is this serving? As far as I can tell the need is for developers to work around issues with frameworks

Sangwhan: if you have a massive SPA but a webpage that loads before that.. I guess that.. making a block and not showing the html part maybe makes sense? Still seems weak.

Dan: we should leave feedback

Peter: just wanting to make sure we have broader consensus [will leave comment]

#### Breakout C

##### Mini Apps

Amy: Miniapp lifecycle - how it plays with origin model.

Sangwhan: the current proposal lets the intermediary set it to be a certain origin... I find that design dangerous.  I don't think an intermediary validate the origin of an app makes any sense - kind of destroys the purpose of CORS.  Personally I think using a model that puts all the origin validation on a cryptographic chain - e.g. signed exchanges - makes a lot of sense.

Max: I think there is some misunderstanding - in my opinion this proposal doesn't require miniapp platform to validate origin... actually the miniapp - follows the same origin - I will ask them to clarify that.  There is no origin validation.  

Sangwhan: I don't undersdtand the response ... lets' say you install a miniapp from example.com - the origin of the miniapp is example.com

Max: yes. And not offline. Not like a PWA. 

Sangwhan: so you navigate to the web site?  

Max: you go to example.com to load the resources.  We can ask the author to clarify.  In my understanding ... follows the 

Sangwhan: miniapp package submitted to miniapp platform on domain... 

Max: that happens on the registration ... not the loading...  Maybe not in the scope of the standard. 

Sangwhan: let's imagine this is a secure context - the miniapp has been validated by a chain of trust - in this case the chain of trust - it's up to the app store to verify?

Max: the chain of trust is the same - same origin - the miniapp platform...  The checking whether the domain is permitted only happens at registration.

Dan: sounds like the actual action of the user invoking the mini app, the user agent goes to example.com..

Sangwhan: according to what I read in this response.. if you look at document.domain in that local package index.html it would be example.com. When you do an app submission.. example.app.. say the origin of example.app when it's run locally should be example.com. Correct?

Max: No. When you submit a mini app... maybe the word 'origin' in this context is not very accurate. Just checks the domain of the mini app developer to make sure that it follows the regulations. Then after the mini app is running it follows all the web principles just like a web application. That is why I said it's an administration.. not part of the standard. Just like if you are a developer of an iOS platform you need to apply for a developer account, then the platform will check whether you are a valid developer. 

Sangwhan: what does the package do here then?

Max: maybe wording confusing.. 

Sangwhan: why is validation happening by mini app platform? Seems like a risk

Max: in different areas they have different regulations. For some regions some web content is not legal. Every platform has need to make sure it follows the lawas and regulations. The platform's responsibility. In some countries it follows the law and others it doesn't. Different rules. 

Sangwhan: censorship?

Max: Not talking about censorship that is different.

Dan: in this ecosystem, the app platform, much like from a user perspective looks like the app store, that is facilitated by the developer submitting a package which includes all the resources which then might go through some kind of validation step by the app store itself. What you're saying is your understanding is when the app is invoked by the end user, the user agent goes out to example.com and grabs those resources directly?

Max: yes. To respond to Sangwhan - not talking about censorship. if you develop a web app to sell fake goods, it violates most laws. That is the responsibility of the app platform to verify that.

Sangwhan: still having trouble understanding the origin model

Max: appreciate the comments, maybe the wording is causing confusion and needs to be improved.

Amy: worth checking with Yves as well..

Sangwhan: PWAs have origin inheritence because the provenance is very clear.

Max: Daniel's summary is very accurate in my understanding...

Sangwhan: Therefore what makes the miniapp different from a bookmark?  It's like a more complicated version of a bookmark?

Max: the difference is - from technical PoV miniapp has lifecycle - similar to native app - lifecycle management...  

Sangwhan: can I get access to a runtime to test something?

Max: possible because there are commercial miniapp platforms...  Thanks for the questions and help - really appreciate efforts to improve security.

##### Web of things

Amy: we also talked about web of things thing description - which Sangwhan also had concerns about.  It's a data model - so no discussion of security - but may be out of scope.

Max: need more time to understand the detail.

Dan: things not directly in the browser.. we had this discussion earlier. There's a whole bunch of stuff that happens that is not directly related to the browser

Sangwhan: other things are at least served on the web..

Dan: demos of web of things I've seen all involve the browser as well. I wouldn't dismiss it

Sangwhan: not dismissing it. Trying to find out.. my question is where is the connection point between the browser, aside from fetch?

Dan: I think there is more. We need to go back to the original web of things review. We also had [WoT Architecture](https://github.com/w3ctag/design-reviews/issues/355) - more relevent, from 2019. You can see a lot of dbaron's concerns, around the api. Worth reviewing.

### Issue Triage
