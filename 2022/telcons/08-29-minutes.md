## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/08-29-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2022-08-29](https://www.timeanddate.com/worldclock/converter.html?iso=20220829T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [ContentVisibilityAutoStateChanged event](https://github.com/w3ctag/design-reviews/issues/756) - @hober, @ylafon **can we close?**
* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss
* [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [CSS Overflow for replaced elements](https://github.com/w3ctag/design-reviews/issues/750) - @plinss, @atanassov


### Breakout C (APAC / Europe) - [2022-08-30](https://www.timeanddate.com/worldclock/converter.html?iso=20220830T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### First Half

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo **can we close?**
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo
* [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman
* [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman
* [Web Machine Learning Model Loader API](https://github.com/w3ctag/design-reviews/issues/759) - @cynthia, @maxpassion, @hadleybeeman
* [Secure Payment Confirmation (heading to Candidate Recommendation)](https://github.com/w3ctag/design-reviews/issues/763) - @torgo, @maxpassion
* [Review request for HTTP Status Code in Resource Timing](https://github.com/w3ctag/design-reviews/issues/757) - @hober, @ylafon, @maxpassion
* [FYI review of Writable directory prompts for the File System Access API](https://github.com/w3ctag/design-reviews/issues/749) - @torgo

#### Second Half : Mini-App Discussion with Guests

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @ylafon, @maxpassion, @torgo
* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion, @torgo


### Plenary Session - [2022-08-31](https://www.timeanddate.com/worldclock/converter.html?iso=20220831T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* TTML FO
* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov
* [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Call Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/08-29-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2022-08-29](https://www.timeanddate.com/worldclock/converter.html?iso=20220829T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Yves, Peter, Tess, Dan, Rossen

#### [ContentVisibilityAutoStateChanged event](https://github.com/w3ctag/design-reviews/issues/756) - @hober, @ylafon **can we close?**

Yves: we asked about the issue of having a complex and (now) simpler way of doing the same thing and the possible bad interactions... would there be a way to mititage this issue we're raised. They've said they are aware but no way to mitigate.

Tess: at least on par with the rest of the platform... at least they are aware and thought about it.  It would be nice if we could break the cycle but in this case...  

Dan: they need a "please make sure this is documented"...

<blockquote>
  
Hi @vmpstr,
  
Thanks again for bringing this to our attention. We're happy with your design and will close this review. We are hoping that you can note (non-normative text would be fine) the possibility of cycles with related features in the spec, so that authors can be warned, but we're not blocking the review on that.
  
</blockquote>

Dan: close with satisfied?

Tess & Yves: Yes

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

Rossen: I feel everything I wanted to put forward - how I see this API and how it could be used for editing - is already stated in the minutes... Peter also stated his points.   At this point what is the benefit?

Peter: The main overall shape is OK ... the last questions are they need to specify what happens with content that has children.. needs to be specified. Questions on use of DOM range. They said they are going to update the explainer and spec... they added details to the explainer and working on changes to the spec.  SO I think we're waiting for them to update the docs.

#### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @atanassov

Rossen: we had this in the agenda for the CSS f2f ... we had a conversation and overall agreement in wg that this is important and we should specify the types of behaviours that are causing flushes in the subsystem in style layout and paint... and what are the patterns to be used to batch as many capabilities as possible.  On the back of this we tasked ... and Dbaron... to think about it.  [could take a while]. This issue can't make fwd progress before that work comes back.  We could keep this open or close it in similar state.

Dan: feel like we should close it.

Tess: Happy to close it.  When CSS group comes back we could get an update. Don't feel we need to keep tracking issue open.

Peter: yes ok.

Rossen: *can close it*

#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Dan: **marked as proposed closed based on feedback from requestor - will close when Lea can join the discussion**

#### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov

Tess: prefer to close it when they actually file the follow-up.

Dan: *added note to clarify status but left open*

#### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

Peter: last week we talked about this - it sounds like they are taking on the suggestion but not clear - we're waiting for that.

#### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss

*punt to plenary*

#### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

Peter: waiting for response - async vs sync

#### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

Peter: they removed a large part of the functionality... now this only effects scripts and stylesheets...  So curious as those are generally blocking things what does this do?

... they've added the ability to block rendering... doesn't block parsing but does run before rendering starts... I'm kind of OK with that.... opting in to async processing... don't understand what this does with stylesheets.

Dan: No signals on multi-stakeholder support.  Does that matter?

Rossen: have we discussed having the multi-stakeholder thing automated ... so it's part of the form?... standing issue...

Tess: I like that idea... 

Rossen: should be part of the template of the form.

Tess: multiple, interoperable implementations ++

Dan: *I'll take a look at what we can do in the issue template*

Peter: *back to issue* their use case still seems to be delibately blocking ... could be bad on a slow connection.  Also numerous issues in CSS wg ... related to web fonts.  We fixed that in CSS... I'm happy to let this proceed for script but not happy with it on style.

Rossen: +1

Peter: *will leave feedback accordingly*

#### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Dan: Another async / sync thing.

Peter: we want Lea's input.

*punt to plenary*

####  [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

*punt to plenary*

**see discussion below**

#### [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss

*punt to plenary*

#### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

*punt to plenary*

#### [CSS Overflow for replaced elements](https://github.com/w3ctag/design-reviews/issues/750) - @plinss, @atanassov

Dan: *let's punt to plenary*

Rossen: I remember one discussion in CSS wg.

### Breakout C (APAC / Europe) - [2022-08-30](https://www.timeanddate.com/worldclock/converter.html?iso=20220830T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### First Half

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo **can we close?**

Dan: status is - I asked for what they wrote into the issue to be reflected in the explainer... they've made some revision. Checking multistakeholder..  Negative signal from firefox.. ambiguous argument in May. [replies]

#### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo
#### [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman

Max: noticed that this is the first version and it can only support half duplex mode - but they plan to support full duplex mode. In their explainer they explain that this is the first version... we discussed full duplex in WHATWG... Will leave comment.

Yves: to me it looks like a valuable addition - they are using streams which is the "right" way of doing it.

#### [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman

Amy: we left them some feedback after the f2f and they have not replied yet.  I will leave them a nudge.  I can open an issue on their repo.

#### [Web Machine Learning Model Loader API](https://github.com/w3ctag/design-reviews/issues/759) - @cynthia, @maxpassion, @hadleybeeman

Max: I looked at explainer and spec - how do we protect the user's machine learning model - not leak it outside the browser. In the explainer they have some disucssion but no solution yet.  Is this a big concern?

Dan: what data is at risk? The model based on the training?

Max: part of web machine learning spec - proposed to prpovide an API to load the machine learning model... the ML model is - like tensorflow - a matrix - mutli-dimensional data set.  In this API they propose to load the ML data model... from URL... They also have a little discussion how to protect the data model. For some companies the ML model itself is considered as intellectual property... 

Dan: analagous to issues around DRM? 

Max: in their security considerations section... theur short answer use DRM like solution...? They don't have such considerations... 

Dan: I'd express not happy feelings about extending DRM to other realms. I think we should be trying to push back on that and saying why does .. we already know DRM on the web is problematic in that it introduces elements to the web security model that are black boxes - we have spoken on this issue before. There needs to be a real serious need and big support for this, otherwise it's my sense that we should not be adding DRM for machine learning models.

Hadley: I agree - otherwise hard to run local data through a model without having access to the model.

Amy: are they proposing a DRM like thing... Or have they not considered how to protect it and we want to make sure they don't end up in that route?

Dan: In [the explainer](https://github.com/webmachinelearning/model-loader/blob/main/explainer.md#how-can-web-developers-protect-their-proprietary-ml-models) they use the phrase "DRM-like solution". Write only.. that's different from DRM. They should not be saying DRM if what they mean is a special type of browser storage. DRM has other type of things.. we could write something about this.. 

Hadley: we can say we appreciate this being an issue - if and when they tackle it we'd love to discuss because there's a lot of nuance about how DRM works that doesn't seem to pertain to this, and a bunch of potential pitfalls with the web's security model.. leave a marker that this is messy and complicated but let's not have the conversation now unless we have to

> Hi @wacky6 we're just reviewing today and one thing that came up was your mention of the idea of a "[DRM-like solution](https://github.com/webmachinelearning/model-loader/blob/main/explainer.md#how-can-web-developers-protect-their-proprietary-ml-models)". We appreciate that you're seeing this might be an issue - protecting models - however if you're going to seriously work on this we'd appreciate being involved because there are a lot of issues and complications with DRM, the differences between its use case and this one, and the web's security model. We suggest to leaving this for future work.

#### [Secure Payment Confirmation (heading to Candidate Recommendation)](https://github.com/w3ctag/design-reviews/issues/763) - @torgo, @maxpassion
#### [Review request for HTTP Status Code in Resource Timing](https://github.com/w3ctag/design-reviews/issues/757) - @hober, @ylafon, @maxpassion
#### [FYI review of Writable directory prompts for the File System Access API](https://github.com/w3ctag/design-reviews/issues/749) - @torgo

#### Second Half : Mini-App Discussion with Guests

Dan: [summarises issues around break from web security model]. How can we best influence the work to adopt some of the alternative packaging mechanisms - some of which have been discussed in the miniapp packaging explainer - that are being developed to preserve the chain of trust of the web security model? So we can have this for miniapps in the same ways we have it for web apps which are packaged using the bundling methods. In particular there was this statement that Sangwhan highlighted that the mini app platform will have its own business policy to check validity of the domain, which is out of scope for the standard. The general view is the chain of trust for security of the mini app is not out of scope - it's part of the architecture. I'm wondering if there's some way we can find to help the group move towards that path. What is your perspective?

Fuqiao: you mentioned alternative packaging mechanisms. I think some of them haven't been discussed in the WG yet because the main vendors all use zip currently. The mini apps are downloaded ot the local device and run in a form of a package. The mini app itself is somewhat like an epub package. It does not have an origin because there is no domain. There is no cross-origin. However there is a safe list which can be configured in the hosting platform. Domain name safe list to permit scripts contained in the mini app to access URL when only when the domain name is in the safe list. There is some kind of mechanism like that. If you think it should be documented in a spec I think that is something we can discuss in the working group. It's mentioned in the whitepaper but not in the spec.

Dan: From my naive point of view, thinking about it in terms of.. you've got the mini app provider who is the middleman.. the network operator or the app store provider, and then you've got the third parties, eg. Starbucks.. It strikes me that the bundling and alternative packaging methods being discussed which preserve the chain of trust could be use din exactly the same scenario to provide exactly the same user experience as what we're talking about here. And perserve the web security model. The concern would be we're doing all of this wrok to shore up and consolidate and strengthen the web's security model so malicious applications do not have access to each other's data etc, and we know that even with the greatest intentions malicious apps can be loaded into an app store and can be executed inside of a trusted environment, so I think we do need to have provide this feedback to the mini app group that we'd like to see them embrace the web security model and to implement that so that it does have this concept of origin, rather than rely on a safe list. What would be the best way for us to provide that feedback, that would be most well received by the mini app community? How can we provide that feedback in a constructive way so we can work together to move towards that approach. A road map. Focus on web package in particular, but it also impacts lifecycle.

Fuqiao: if you think it's feasible for the web security model to be applied to mini apps, maybe the TAG can provide some relatively specific detailed proposal? Maybe have a draft explainer or something? We can invite interested TAG members to the WG meeting to discuss this. We can discuss it in an issue in the mini app packaging repo. 

Dan: that's a reasonable ask. I don't think the TAG can provide a detailed architecture document for mini app packaging. What we could do is come up with a general idea of why it's feasible. An alternative proposal. That could be possible. And we can open the issue in that group's repo. It would make sense to focus on packaging. That seems to be the crux.

Amy: can we get some info on why this hasn't been diuscussed... something about the existing solutions that hasn't worked for them?

Fuqiao: i think it's because of existing implementations are using this mechanism already...   but group is open to more ideas... Another proposal could help to improve things for mini apps.

Yves: recently a lot of discussion (in the TAG) about code injection in applications. The fact that in that case it's related to those apps not respecting the orgin model - this is a good example who they origin model should be followed propertly.  I think we should put that discussion in scope.

Max: I'm happy Miniapp wg is open for suggestions from TAG. This will benefit the whole mini app specification.

Dan: We need to write something. Maybe analagous to what we wrote in Fukuoka which amongs other things highlithed the importance of manifest file as something we wanted to make sure we didn't add an additional manifest file to thew eb, and that resulted in this very good discussion about mini app manifest being extension to the web app manifest. I know this is a bit more fundamental, but it's something we need to articulate what we think the issue is and what the roadmap could be. Important to speak about this.

Amy: is the minapp group meeting at TPAC? What date would make sense to shoot for?

Fuqiao: not meeting in TPAC but there will be a wg meeting 1 week before TPAC. But if needed we can arrange a topic-specific call. 

Dan: timeline I see - TAG works on something, get Fuqiao's feedback, then circulate it,then organise some time to discuss. Make sense?

Fuqiao: sounds good to me.

#### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @ylafon, @maxpassion, @torgo
#### [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion, @torgo


### Plenary Session - [2022-08-31](https://www.timeanddate.com/worldclock/converter.html?iso=20220831T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Max, Peter, Lea, Hadley, Amy, Rossen

Guest: Dom

#### Breakout Rollup

##### Breakout A

##### Breakout C

#### TTML FO

#### Code Injection

Dan: *summarizes... question of should TAG do a finding related to the recent [revelations](https://krausefx.com/blog/announcing-inappbrowsercom-see-what-javascript-commands-get-executed-in-an-in-app-browser) of code inkection*

Also related to webview CG open issues:

* https://github.com/WebView-CG/usage-and-challenges/issues/20
* https://github.com/WebView-CG/usage-and-challenges/issues/36

Dom: this has been brought out in the Web View CG .. we are looking at intersection of webview and other technologies. webview is used for a lot of things, some are hurting the web, some are bringing the web to new places so we're trying to make the best of the situation. Some developers need to do code injection when they used webviews. There have been good and bad examples ofthat. The bad examples are in the article. One of the active participants is DuckDuckGo who need code injection for their privacy preserving browser to protect end users. One of the early outcomes of the discussion is that code injection is not per se good or bad, it's more how transparent what is being done with this injection is to the end user. I think, personally, it has emerged that the notion of what constitues a user agent is at the core of the challenges here. If you're a browser installed by the user with an understanding of what you sign up for, it's a pretty different picture than if you're in a social network app and click a link and end up using the in-app browser realising it or not, and the in-app browser does things that we're aware of or not, that brings a very different perspective to what extend the user agent is really behaving on behalf of the user. in the speciic context of the webview community gruop we're probably going to stay away from any kind of policy discussion. If you're building browser-based web views you probably need thse types of capabilities and itw ould be useful if there was a unified approach. But it would be interesting, not sure if easy or feasiable, if the TAG could bring more of the policy view of this, if you're a user agent and sign up to be a user agent what are the committments you're expected to make, you need to make, to the end user. How transparent should they be? I know from these discussions it's a topic Robin Berjon has put thoughts, intersting to chat.

Rossen: In this context, how is code injection different in web view than in the browser?

Dom: in the browser you can't really inject code unless you're brought in by the website itself. That could be through advertising, more or less controlled, but as the website owner you control what you serve to the web user. In webviews it's controlled by yet another party, whichever one is shipping the webview, without understanding of the website owner. In some cases breaking the website itself

Dan: it reminded me of the controversy around supercookies. Which was a http header injection being proposed/done by some mobile operators, prior to the whole movement to move to https. At that point it was really easy to inject http persistent headers into web content which caused a huge privacy backlash, and was one of the things that led to the rise of https, because it was highlighted in places that call was being made. It's kind of similar in many ways as a third party that is not the one that you've chosen. Facebook or TikTok would say you have chosen them because you've chosen to load the content in their app, but you don't understand that when you've loaded the content in that app that that webvie wis making choices about how to render that content which could include injecting trackers or doing other things that you don't normally associate with a web browser

Rossen: you can side load into any process on any OS if you are able to deliver bits on the user machine with or without their willingness. What I'm hearing is you're talking about the possibility of downloading bits alongside with webview which are coming without necessarily the intent or knowledge of the user and those bits are sideloaded into the process and then you can do what you want. Did I get the threat or the concern correct? Otherwise having process injection.. yes, browsers are doing a lot of work to try and protect themselves but there are still a lot of devices that have other software inejecting into browsers all the time. What exactly is the problem that you're trying to address? is it the fact that longside these applicatinos, webview applications, users may unintentionally download additional bytes that then can be...

Dan: no, it's when you're in an application that uses a webview to load third party content. You're in TikTok, somebody has put a link into their comment, the link opens web content from elsewhere on the web, say a news article, but now it's loading inside a webview in TikTok and TikTok has decided to put additional tracking code in there, which is not what the original author of the news article wanted.

Rossen: that makes a lot of sense. And you wanted to talk about how we could wall-garden that kind of behaviour?

Dan: to say what we can say to discourage that kind of behaviour. We have done similar things in the past - unsanctioned tracking. When we see a behaviour on the web like this we can write a finding. Could call for things like platforms to provide tighter scrutiny against this kind of use

Dom: One of the things we've discussed in the webview CG is that right now you get everything or nothing. All the APIs they provide. As we were discussing the type of usages that webviews expose, we also thought the notion that platform OSs could say if you want access to that API you need to say that you intend to behave as a browser or a UA and that commits the person that does this to that level of scrutiny in terms of app store reviews or regulators or whatever. You're saying you're a UA you have to behave on behalf of the user, not just commercial interests. If you add tracking for commercial interests to a websiset hat was completely utnracked because the owner had committed to this, you may be sharing very sensitive information that the user did not expect to be shared. AS you'd expect in a browser facebook does not share your banking access with themselves or a random third party. You can say you don't want facebook tos hare that you visited this clinic with a random third party.

Rossen: is that getting traction? Especially with implementers who are part of web view capabilities and implementation?

Dom: we are so early. Getting good discussion from some ofthe implementers. In particular google and microsoft are really involved. But still very far form making any sort of recommendation. WE've alluded to some ofthis idea, but far from saying this is what we have

Dan: sounds like there are some nuances. E.g DuckDuckGo do code injection in order to... I guess the other thing .. browser extensions do code injection (or removal) and that is.. there is a nuance.

Dom: I think there is a particular bias here. Code injection is detectable beacuse it can impact the visible js. But if you are coding a native browser that would do trackign without the user knowledge it would be just as bed. It's really about the kind of expectation that users have in terms of browsers. If you're behaving like one you should accept the user expectations that come with it. Facebook is using the webview but does have the means to do an independant browser, they could do any kind of tracking. It's a good way to raise visibility of the topic but I don't think it's the main focus here.

Rossen: makes sense. once you're inside essentially the webview is your host, then the host has superpowers. If you're in the host's environment and in their own content then you already committed to that facebook or whatever experience. But once you leave etheir premise and you continue to carry them with you they do still have the same superpower even if they're not injecting code. That's a problem.

Dan: does it make sense for us to work with people in the webview CG on this?

Dom: We are meeting at TPAC. I suspect the web view cG will want to stay as far as possible from policy positions. But in terms of informing ... What a CG needs to deal with if we were to come with technical recommendations we don't want them to be blocked because of somethign we have said before.

Rossen: when do you meet?

Dom: Friday morning 0830-1030

Rossen: i can try and drop in

Dan: i can via video

Hadley: I'd love to

#### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Dan: they provided answers..

Lea: what changed from the previous attempt?

Rossen: our last one was not exhaustive right?

Dan: no signals from firefox or safari **adds multi-stakeholder label**

Max: [from request] "This is a third attempt at a TAG review for this feature. The first attempt was closed due to the lack of an Anchor Positioning proposal. That has now been proposed, and there's a draft spec. The second attempt was closed because we changed directions from a \<popup\> element to a popup content attribute. This third TAG review is for that new content-attribute-based approach."

Lea: adds on div or a?

Peter: they have examples of custom elements

Rossen: it's on element

Peter concerns me - how this interacts with other mechanisms to do the same thing. dismiss behaviour.. a close watcher type of thing.. Tess had issues.. listening to escape. one of their examples is building a date picker and that sounds like something that should be the form element and there's already an API for form elements to do popups so be nice if these things were aligned. if I'm buildng a custom element that acts as a form element maybe I should be abel to activate the popup the same way as a native form element

lea: i have a lot of rservations about extending the element api surface to that extend> I understand it's imporatnt but it adds several attributes on every single element. I'm not sure this is needed compared to having a dedicated element for htis sort of thing, which was the prvious proposal. What do others thing? Okay to add that much stuff on every element?

Peter: I think that's a valid concern. I think it's fair to be able to add this capability to custom elements, but it could be restricted to popup or custom, or have some way for the custom element inheriting from popup

Lea: or the custom element could contain a popup element in the sahdow DOM, whcih is how they inherit capabilities in other areas. We don't add to every element to become a details and summary or dialog..

Peter: their original proposal was for dedicated element

Lea: I think the pushback was that it wasn't clear what this did? I think the problem was it was an abstract class that you needed to extend to do anyting useful with

Rossen: more like an interface. Which is why, reading their explainer now, why they went odwn the path of distributing the actual abstract capabilities to the base element. Which is now taking it perhaps a step too far. I can see how that could be .. we can probably make a case fo rnumber of elements and the opposite for.. I don't see any discussion or .. reading through their goals I don't see the behaviour being intended to be so broad. I don't know what ... 

Lea: regardless of the reservations for the previous proposal, compared to this I think the previous proposal was better

Rossen: in some ways yes. I like the ease of extensibility of this one. But if they were to scope thi, and it's going to be up to them to come up with use cases and data to back up which elements they would extend it to, I can see how they can make a case to the usual suspects of elements, inputs and a div perhaps, and custom elements, and keep it there. I'm nto sure what that behaviour would do for body. But then again you might come up with a use case where that is a useful thing on body.

Lea: The API shoudl be designed to accommodate the common cases

Rossen: agreed

Lea: we are concerend that they are extending every element, doesn't look like this needs to be a global behaviour. yes it's a way to address our previous feedback it would probably be better to have a popup that does somethign by default. Any other points?

Dan: I left a note asking about stakeholders/implementers

Rossen: Re-reading the goals.. the very first, "any element and arbitrary descendents" .. that by itself suggests that the popup behaviour they're describing here is intentially applicable to any element. I do'nt know what that means for table column for example.. 

Lea: doesn't that make it harder to implement? To deal with these complications?

Peter: something like a ?? where youw ant to take random content and surface it, but a backdrop around everything else. Back to the discussion about custom elements - they did add a mechanism for a declarative popup trigger. That mechanism does make sense to apply to custom elements in addition to popup. Even if the custom element contains a popup in its shadow DOM it makes sense for the custom element to be acting like a popup. Agree that applying this to everything is scary.

Lea: any attributes on the trigger are fine as globa. Doesn't make sense for the popup to be a set of global attributes and methods. 

Peter: the thing you can trigger you want to be able to trigger custom elements in addition to popups. MySpecialPopup and trigger it with this mechanism.

Lea: extending builtins is a whole separate issue.. we're not going to fix it with popup. There are several proposals to fix this. Existing functionality for extending builtins that safari has blocked. We should nto be solving this as a one off for this use case.

Dan: focus on the scope question. Additional thing about form controls that you said Peter?

Peter: one of their examples is a datetime picker. Other form controls do popups. There's a separate proposal for how to trigger thos eprogramatically. If I build a custom element as a date picker that is a form element it would be nice if I can trigger its popup behaviour the same way as aother form elements rather than having two different APIs.

#### [Focusgroup](https://github.com/w3ctag/design-reviews/issues/732)

Lea: any movement?

Dan: not since June. A [PR](https://github.com/openui/open-ui/pull/550) merged in mid June which is about a11y.

Lea: I don't have the a11y knowledge to evaluate how serious this concern is.

Dan: did Travis's comment address your issue? Not really

Lea: don't think it should be a blocker. Just a matter of doing it. the other thing is this person who raised this concern and I'm not sure how serious it is.

Dan: we could bring in external help?

Rossen: the overall issue that Paul raised was with some of the.. one of the examples which was addressed by the api itself and the ability to navigate through focus groups. The way I read this comment is I believe he was misled by the example in believing that the tab index in combination with focusgroup is going to be an issue. Which explicitly I think somewhere in the explainer.. section 6 focusgroup concept.. talking about overall interaction between tab index and how that extends to handling of focusgroup and focus. So generally speaking focus mangaement and focus itself is a fairly loaded issue on its own. I can help if I spend some time. Distanced myself since I was involved in the initial design, a couple of years ago. I don't see the concern from Paul as being something that should block progress.

Dan: close satisfied?

Lea: [comments] - can reiterate the thing about element internals? Anything about Paul's point?

Dan: could say please engage with the accessibility community to ensure they look at this. [APA]

Rossen: pretty sure they already have. Done in part with the help of the community. Not in a vacuum. But fine to remind them.

**Agree to [close](https://github.com/w3ctag/design-reviews/issues/732#issuecomment-1233123697)**

#### [Review request for HTTP Status Code in Resource Timing](https://github.com/w3ctag/design-reviews/issues/757) - @hober, @ylafon, @maxpassion

Max: I think this is resolved

Yves: I think we can close, positive feedback

**agree to close**

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov
#### [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov
#### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
