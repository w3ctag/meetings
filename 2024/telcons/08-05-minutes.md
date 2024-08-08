# TAG Teleconference
#### 05-07 August 2024

---

## Agenda:

### Breakout B (California / Europe)  - [2024-08-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240805T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk

### Breakout D (California / Australia) - [2024-08-06](https://www.timeanddate.com/worldclock/converter.html?iso=20240806T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @LeaVerou
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou

### Breakout E (Europe / China) - [2024-08-07](https://www.timeanddate.com/worldclock/converter.html?iso=20240807T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

-----


## Breakout B

Present: Dan, Matthew, Peter
Regrets: Yves


### Cookies Finding and Feedback

Dan: I openend up some issues to reflect Alex's feedback - or some of his feedback points

Mattew: I'd like to merge Martin's PR

Dan: I'd like that, but I'd like Hadley to review. Also it doesn't cover anything we want to say with use cases.

Matthew: I'd like to see a bulleted list...


### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

### [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss

### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

### [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss

### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

### [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon

### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

Matthew: we need to decide if we're OK with closing it... Nobody has said "this is bad"... 

Peter: if you're designing a transition that you're expecting multiple pages to use that transition... so that's an argument for it. But is having this layer of indirection useful?

<blockquote>

Thanks for bearing with us. After reviewing and discussing internally, we have one question which is: did you discuss the option of using selectors and if so could you document in the explainer the reasoning for not using that approach?

We see the extra layer of indirection as being useful if view transitions can be used with multiple arbitrary pages, but it's unclear if the transitions will be generic enough in general to be reused. If the transitions need to be tailored to the specific page content then an extra layer of indirection doesn't seem useful.

</blockquote>

*comment left https://github.com/w3ctag/design-reviews/issues/938#issuecomment-2269500378*

### [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk

Matthew: some additional feedback I've been catching up with... especially about the AI namespace...  But there is other stuff they want to put in this AI namespace... the concern is : if they're going to put something in a namespace shouldn't it be problem oriented rather than technology used to solve the problem...

Dan: I'm not anti-LLMs in the browser. Say a browser used a different technology besides AI based to do translation? Then it wouldn't make sense anymore?

Peter: if they want to expose an LLM at a low level then call it an LLM... 

Peter: if they are making a new common API pattern then let's make sure it makes sense for everyone... and put it in our Design Principles document...

Dan: propose we say something like

<blockquote>

Hi Domenic - Our feedback that we sent above stands, particularly regarding the name space of this API. We don't think it belongs in a `.ai` namespace. We think that the name spaces should be funciton-led rather than technology-used-to-deliver-the-function-led.  
  
</blockquote>

Matthew: a little more discussion to go...  I'm really concerned about point 7 from our [original feedback](https://github.com/w3ctag/design-reviews/issues/948#issuecomment-2256555364). But I'd like to see if we have consensus about this. It's related to what I've seen in Accessibility. The one thing we can do is set the tone for the discussion here...  W3C is also working on this AI and the web document...

Dan: I agree.

Dan: should we bring up the AI and web document in this dicussion?

Matthew: they have been requesting feedback since the AC meeting...

Matthew: we should keep an eye on it and see if Lea can respond...

## Breakout D

Present: Peter, Martin

Regrets: Tess


### [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

This is waiting on proponents still.

### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

Peter and Martin are inclined to close this issue as unsatisfied.  Thoughts follow...

This whole ID business is distracting.  Can we focus on the use case and legitimacy of it, or not?

A site can provide a link to another website.  With a same-origin install, a website can initiate an installation.  Enough?

The ID of a manifest is a URL.  However, that URL is not expected to be resolved, which is weird (note: ask Marcos Caceres why).  If it resolved to a manifest, a lot of things would be easier.  If it resolves to nothing, that's fine too.  The manifest is what is provided to navigator.install() as options.

The presumption here is that trust is a finite resource.  People trust a limited number of sites.  So in deciding what sites to trust or not, they end up picking just a few.  Having an app store as a trusted sites is convenient, because it enables people to broker that trust into multiple app installations from multiple sources.  But what power does that confer to the app store over those installations?  A mobile app store has a considerable level of control over what apps can or cannot do.  They can withdraw an app that violates those terms.  This is antithetical to a web that rejects the notion of centralized control.

https://github.com/w3ctag/ethical-web-principles/issues/120 --> https://github.com/w3ctag/ethical-web-principles/issues/120#issuecomment-2272278572

### [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @LeaVerou

### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou


## Breakout E

Present: Dan, Matthew, Tristan, Martin

Regrets:


### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

No info... 

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Martin: feedback was let the web site in the scope have something to say about it... they wanted to do this on an origin-wide basis...  Idea is that you have a webapp that includes stuff from outside the origin of that webapp - so the webapp declares please include this other stuff in my scope. The request from the feedback we gave is to give the other origin fine-grained control of what resources are in the app vs. not in the app... Reilly suggests a "CORS" mechanism - and trust but verify...  Potentially too late at the point you've started to make requests though...

Martin: opt-in suggested in original explainer - at the target origin you would host a resource that says "these apps are ok on this site for all origins"... 

Dan: a new type of resource that would be at a well-known location...

Martin: It's a reasonable thing to be able to do... Reilly is suggesting that the manifest sets the scope and that when you navigate, that navigation request uses a cors-like protocol that says "the following app has asked me to navigate to this resource" then the resource itself says "ok" (in a header). Don't know if it's reasonable to do this in the navigation and loading algs... 

Martin: a file can be relatively straightforward... 

Dan: `https://example.co.uk/.well-known/web-app-origin-association` (from explainer)

Dan: can we leave feedback to the tune of 

<blockquote>
  
Hi @LuHuangMSFT - as noted we are fine with the user need and we are generally fine with the design. @reillyeon has suggested a CORS or CORS-like approach. Whilst that has some advantages (in particular, not requiring a new well-known located file) it also has the disadvantage of requiring complex server configuration. Our main concern stands, however, that the Association file should allow for more specifying resources in a more fine-grained way. This could include wildcards to make it easy to create a very permissive Association file, but it should be possible to lock down the resources that are OK to share.  Would you be OK with modifying the design to allow for such an approach? If so, we're happy to close this review as `satisfied`.

</blockquote>

Matthew: urlpattern as also brought up

Martin: I think it's a secondary issue... 

*some discussion on [install cross-origin](https://github.com/w3ctag/design-reviews/issues/946)*

Dan: Leaves [comment](https://github.com/w3ctag/design-reviews/issues/875#issuecomment-2272811044)

## Meta issue on centralization

Martin: one of the trends we see with app-stores - it's a centralizing force in some ways - that's a natural result of people having a limited set of things they can "trust". An app store has an opportunity to have a central place to judge trustworthiness. A search engine also plays this role. But when you create an API that encourages the use of delegation or centralized trust in this way then you're creating a force towards centralization. Principle I was thinking of was "don't have someone delegate something when they can do it themselves" or similar... E.g. for web install API - the target website has a PWA and can install itself... all it requires is that your appstore link to a page on the target... 

Dan: I agree but not sure how we phrase it exactly...

Dan: *thinking about multiple appstore use case*

Martin: does the web even need an app store? couldn't a central location just link to "apps". Also an app store general has control - they can kill the app. They have a kill switch. They can control what an app can and can't do. That's not possible on the web... So the extent to which you're able to instill trust in a web app store is greatly reduced...

## Plenary Session

Present: Peter, Dan, Matthew, Martin, 

Regrets: Max, Tess, Hadley, Lea

### Breakout Rollup

#### Breakout B

##### Discussing [Translation API... ](https://github.com/w3ctag/design-reviews/issues/948)

<blockquote>

Hi Domenic - Our feedback that we sent above stands, particularly regarding the name space of this API. We don't think it belongs in a `.ai` namespace. We think that the name spaces should be funciton-led rather than technology-used-to-deliver-the-function-led. Your proposal under [point 6](https://github.com/w3ctag/design-reviews/issues/948#issuecomment-2257382202) (`AITranslatorCapabilities`) is a step forward but we would prefer `Translator.capabilities()`. We also think your response to point 3 of our feedback is fine. We also would strongly encourage that the spec include a non-normative note encouraging the use of professional translation services where possible (point 7 of our original feedback). Please consider this. We're going to close as `satisfied with concerns` due to these concerns. Given the current state of the spec, and lack of venue, we understand this to be an early review. We expect that addressing the points above will be important for further standardization. ✨
  
</blockquote>

Issue closed with sparkles.

#### Breakout D

#### Breakout E

Dan: we left feedback to scope extensions - no feedback so far

*discussion on scope extension*

Martin: i keep thinking if we could be creating a way where this could be misleading or abusive... 

#### Finding on Why the Web Doesn't have an App Store

Martin: *suggesting a new finding* - power I'm most interested in is that that protects from bad apps and that is built into the platform on the web.

Peter: counter-argument is that installed apps might get elevated permissions by default but current consensus is that this isn't a good idea.

and Dan comes up with an idea for this that should never be implemented.

We discussed whether scope extensions is potentially harmful and conclude that with an origin being able to control what resources are included, it is broadly reasonable. It exists to ensure that navigation warnings don't occur for things that aren't really navigation.

### Issue Triage

https://github.com/w3ctag/design-reviews/issues/957

Matthew: they are proposing to add a facility to add a button in pip... 
