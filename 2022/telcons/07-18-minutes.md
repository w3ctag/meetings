
## Agenda

### Breakout A (Europe / US) - [2022-07-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220718T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Could be closed:
* [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov
* [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss

Other:
* [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov
* [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
* [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-07-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220718T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Could be closed:
* [Edit Context](https://github.com/w3ctag/design-reviews/issues/416) - @atanassov, @cynthia

Other:
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @torgo, @plinss, @atanassov
* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss
* [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744) - @torgo, @maxpassion, @atanassov
* [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss
* [CSS property object-view-box review](https://github.com/w3ctag/design-reviews/issues/740) - @LeaVerou, @atanassov
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss


### Breakout C (APAC / Europe) - [2022-07-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220719T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Could be closed:
* [Site-initiated mirroring](https://github.com/w3ctag/design-reviews/issues/745) - @ylafon, @maxpassion
* [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman
* [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman
* [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Other:
* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo



### Plenary Session - [2022-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20220720T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)



* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes


### Breakout A (Europe / US) - [2022-07-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220718T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Lea, Peter, Yves, Rossen, Tess
Regrets:

Could be closed:
#### [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov

Dan: do we think this is going in the right direction?

Rossen: check of directionality.

Tess: I'm fine with it as long as it's understood that it's an early review and there's no enormous red flags.  

Rossen: Not a license to ship.

Rossen: maybe mark as preliminary OK label?

Dan: could we ask them to file subsequent reviews when they get further?

Rossen: all the API I assume they will bring back to us when they are more solid.

Dan: propose: "Thanks for the opportunity to review this work. We largely think it's going in the right direction. this is not a full endorsement of the current API or architecture as specified in the CG report.  As this is a big piece of work with multiple moving pieces, we'd like to suggest you come back to us to request indivdual reviews of these components once they reach an appropriate stage of maturity / consensus."?

**agreement to close with the above comment**

#### [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss

Peter: similar situation - comment I left has had no response but comment is broaded scoped.  Maybe we should just open an issue against HTML - need a mechanism for declaratively making elements with this type of behaviour that don't require parser changes.

Dan: I think that makes sense.

Peter: I will file the issue in their repo and **close** our issue.

Rossen: there will be an update soon.

Other:
#### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

Lea: this is substantial.  Defer to the f2f?

Dan: I set it for next week.

#### [Early design review of the **updated** Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602) - @torgo, @atanassov
#### [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov

Dan: [response from Mike West](https://github.com/w3ctag/design-reviews/issues/742#issuecomment-1184104009).

Peter: we're concerned about the primary use case.  I can leave a comment.

#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
#### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

Sangwhan [via chat]: I don't understand [OP's comment](https://github.com/w3ctag/design-reviews/issues/725#issuecomment-1138032023).

Lea: will ask Sangwhan to comment on the issue.

#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
#### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
#### [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss

Peter: We think we can close it as satisfied.

Sangwhan [via chat]: mechanism to remove signal seems missing, what if one signal source (that one doesn't have full control over) doesn't matter any more?

Lea: other things are similar... 

**Provisionally based on Sangwhan's feedback agreed to close with positive review**

#### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-07-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220718T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Peter, Lea, 
Regrets: Sangwhan

Could be closed:
#### [Edit Context](https://github.com/w3ctag/design-reviews/issues/416) - @atanassov, @cynthia

Rossen: status?

Dan: a comment from Peter in April - no response yet.

Rossen: proposed API has a very strict scope on text.  We can debate that further .. if the topic needs to expand .. to elements .. reinvent entire DOM inside... Not interested.

Peter: I just think there's under-specified behaviour...  Within the scope of this proposal...

Peter: if you call this on an element that has children what happens to the children?  The answer could be "throw them out" - just want to have consistent implementations..

Rossen: ok that's fair.

Peter: there's a question of why not use DOMrange... just an API shape question... just about making it more consistent with other APIs already in the platform.  No answer to that either.

Dan: we just need an answer to the questions being asked here... 

Sangwhan [via chat]: we should close.

Rossen: I will follow up.



Other:
#### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
#### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @torgo, @plinss, @atanassov
#### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
#### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
#### [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss

Lea: one of my concerns here - a static method that has the same name as an instance method and does something completely different. Response.prototype.json (the instance method) converts the response to json - this one takes an object and converts it to a response, i.e. the inverse.   Should it be a concern? I think it's a bit confusing.  In general i expect when instance methods and static methods have the same name then they are related.  Feels like an antipattern?

Dan: would it be better to have 'fromJson'?

Lea: then inconsistent with the other method which is also 

Lea: e.g. `Response.json(response.json())` would be confusing... I wonder if there's a precedent on the web platform... single words for names - in general a good thing - because we don't want extremely verbose names - but breaks down in cases like this. We could use toJSON and fromJSON... Also don't know if it makes sense to hold it up on naming. We should decide what pattern what should be followed... when you invert that type of function. 

Peter: fromJSON wouldn't apply because you're not passing JSON into it... toJSON doesn't apply either... 

Lea: the existing instance method gives you an object and this does the reverse.

Peter: at the end of the day it's a factory method

Lea: and nothing indicates this.

Peter: agree the naming is ambiguous - but I would name it something that indicates it's a factory.

**let's go to the bat-design-principles**

**nothing there right now**

Lea: "create" is the dominant convention in other platforms.  Should we have a principle that factory metods should have a "create"?

Dan: can we ask them to comment on this?

Lea: i will leave a comment.


#### [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744) - @torgo, @maxpassion, @atanassov

Max: waiting for answers...   Will email Elad.

#### [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss

Lea: seems very incremental - something developers do frequently - pretty small feature, small abstraction.  

Peter: Looking at the "[sync vs async](https://gist.github.com/domenic/f2a0a9cb62d499bcc4d12aebd1c255ab#sync-vs-async)" discussion in the explainer.   Whether import maps are loaded or not.

Lea: supposed to be syntactic sugar for what devs are doing already which *is* sync. So tending to agree with Domenic.

Peter: wonder if import maps haven't loaded yet what's the behavior? would you get an answer that's wrong?

Dan: leave that as a comment / question?

Peter: i can leave the comment.

Peter: [in the issue] a lot of background to the sync vs async decision. Seems like a lot of other dependencies on this.  Not sure it's a simple thing.  

#### [CSS property object-view-box review](https://github.com/w3ctag/design-reviews/issues/740) - @LeaVerou, @atanassov

Peter: i am not sure this requires TAG review - not an architectural thing. Fine with just closing it.

Lea: fine by me.

**agreed to close with positive review**

#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

Lea: Dan left a comment... 

Dan: I don't think this should be blocking progress...  Did Tab [address](https://github.com/w3ctag/design-reviews/issues/730#issuecomment-1124298690) the issues you raised?

Lea: one of the main concerns was about cycles... 

Dan: Should we close it?

Lea: I think so.

Peter: a little concerned that this is just managing state. We've had discussions about where state should live.  This puts state entirely on the presentational layer. 

Lea: realistically it will be used for all kinds of state.

Peter: if i want to send you a link to something how is the state preserved?

Lea: this is the kind of state that is similar to details and summary.. you're not meant to see the same thing.  presentational local state.

Peter: linking to a specific tab ... 

Peter: i think the css wg can work this out. I think there's a larger arch issue about managing state... it's come up in other issues as well.

Dan: concerned that developers misuse it... (to save other kinds of state than intended) can devs be encouraged to not do that?

Lea: maybe give devs tools to read, save and restore state... 

Peter: that's what I'm thinking...

Lea: that's a huge need in the web platform. I think this is intended as a stop-gap solution.

Peyer: this should be layerd on top... we need a model that *explains* this feature. 

Lea: a javascript API for managing state that has a CSS counterpart?

Peter: possibly - a system for managing state - general purpose - CSS toggles could be explained using that... later, a JS API... 

Lea: there's a section about a JS API for CSS toggles but not sure it's the right framing.. it should be for managing state.

Peter: **leaves comment**

### Breakout C (APAC / Europe) - [2022-07-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220719T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Sangwhan, Yves, Hadley, Max
Regrets:

Could be closed:
#### [Site-initiated mirroring](https://github.com/w3ctag/design-reviews/issues/745) - @ylafon, @maxpassion

Yves: seems okay as long as it's local network that's fine for me. We can close and let the WG decide.

#### [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman

Amy: still working on breaking up my comments into issues in their repo. There was a response about a security thing.

[bump to f2f]

#### [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman
#### [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman

Hadley: waiting for a response

Dan: we got a [response](https://github.com/w3ctag/design-reviews/issues/716#issuecomment-1185621379)

Hadley: we're not *against* it... but compared to what?    Who do we know at TC-39?

Sangwhan:  Dan E. is on TC39... 

[Sangwhan & Hadley leave comments]

Dan: set milestone for next week and we can close then.

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Amy: they've taken into account our feedback, we can close

#### [Edit Context](https://github.com/w3ctag/design-reviews/issues/416) - @atanassov, @cynthia

Dan: still pending answers to questions Peter raised. Sangwhan said let's close it. Got a response that they're updating the explainer and then update the thread. Sounds like we should wait for the update.

Other:
#### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou


#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Dan: confused about motivation.. some browsers make it reliable.. is this a point of contention? Cache people vs browser people? Effectively a new entry to fight back against browsers that want to do a certain thing? Or misundersatnding?

Sangwhan: more like if a website sets this it's a guarantee that you can use BFCache. Without having this permission policy opt in the browser cannot safely enable BFCache is what this is tryint to solve. It's a bit indirect, might be unclear.

Dan: the page will set this policy?

Sangwhan: correct

Dan: "hey, I want to be BFCacheable"

Sangwhan: yes. This is one of the many flags that will guarantee you get BFCache

Dan: why do there have to be many flags? Not one flag?

Sangwhan: there are multiple problems when it comes to enabling BFCache for the entire web. a lot of theAPs we have minted in the past do not take into consideration in a document that is not fully active it is unclear what to do about script context frozen holding onto a resource, a hardware device or a file handle, the document is not technically fully deactivated. it can be partially holding on to the file handle for example, it's basically a lock on that file. you can't take a fully deactive.. you cannot use the BFCache. A lot of the FUGU APIs have this problem. That's why it's multiple flags. The condition is it must not use a certain set of APIs, not have an unload handler, and optimally have this opt in to be able to trigger bfcache. It's damage control. The team behind bfcache want us to consider this. They have some design principles they're trying to pull goether. A lot of the APIs are being minted and reviewed without consideration of allowing documents to be not fully active. So they're trying to add extra mechanisms so documents that state that they're okay with not being fully active can explicitly state it. They want to talk to us if we have time during the f2f.

Dan: sounds like a good idea.

Sangwhan: they're in Tokyo so it'll be early for us but can arrange that.

Dan: do we hold off to f2f?

Sangwhan: yes

Dan: not sure what's behind the statement about "browsers have chosen"... doesn't seem very holistic.

Sangwhan: that's a different problem, this is opting out of on unload. Ohh.. maybe could be problematic. Talk about this next week. Unload handler problems has been long standing on all browsers. Architectural issues. Multiple weird mitigations like html ping attribute.. ?? api that is also very limited.. so offer a feature to disable it.. but architectural discussion is is there any way to fix this?

```
So we're just discussing in our breakout this morning. And @cynthia has given some further detail and how it fits into bfcache. I was a bit confused by this "Some browsers, like Desktop Chrome and Desktop Firefox, have chosen to keep the unload event reliable, so the existence of unload handlers makes a page ineligible for BFCache, hurting performance. In others like Android Chrome & Android [Firefox](https://groups.google.com/a/mozilla.org/g/dev-platform/c/3pQRLPZnQgQ/m/dsA1w4iiAwAJ), and WebKit-based browsers (Desktop Safari & all iOS browsers), if the page is eligible for BFCache, the unload handlers will not run, further increasing the unreliability of unload handlers." because it sounds like part of the motivation here is to patch a problem with current implementations? Can you clairfy?
```

#### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

Dan: I like their explainer. This is about telemetry

Sangwhan: to some extent

Dan: tread carefully.. talking about information that could be used to expose personal data

Sangwhan: how many states are available? [Spreadsheet](https://docs.google.com/spreadsheets/d/1li0po_ETJAIybpaSX5rW_lUN62upQhY0tH4pR5UPt60/edit#gid=0)..

Dan: 128 entries..

Sangwhan: would this potentially leak information about if the user is using an extension that in anyway modifies the document? I don't think they call that out. In the vanilla browser setup it would not lead any extra information about the user. I guess it might... no it won't. To the origin it won't. If there's an extension that modifies the website or runs any extra scripts on the website that will trigger.. potentailly leak some information about a particular user. One extra bit of entropy to identify the user. I don't know if that's serious but they should call that out.

Dan: I don't think they have privacy and security considerations... They've answered our questions but that's not the considerations section. Where's the actual spec? 

Sangwhan: I think this is early. 

Dan: so in their response to the s&p questionnaire they've said yes it has a privacy considerations section now, but I think they just mean they have answered our questionnaire. The kind of potential privacy risk Sangwhan is talking about is something that should fit into a privacy considerations section which still appears to be missing.

Sangwhan: do we require that..?

Dan: they have said they have one. Does look like something where it's sent back to the server out of band to aid the developer. We had a whole discussion about telemetry in the PrivacyTF as well and the fact that ideally browsers should be asking maybe as a first time use asking users are you okay with this browser enabling websites to gather telemetry in order to aid the development of the websites? That's something most applications ask. And we should give users an opportunity to answer no if they don't want telemetry to be shared. This would seem to fit under that category. This is something in the proposed privacy principles.. feels like it fits in the same category. I can leave a comment.

Sangwhan: imagine normally not restored would not happen but you have an extension that messes with the scripting context of the website, eg. tamper monkey, which will trigger not restored to happen for a reason. That will correlate the user with extra information. Invalidates some of their s&p responses, I wonder if they're aware of this.

```
hi @rubberyuzu thanks for this. We're picking it up now and discussing in the context of other bfcache-related reviews. One thing that came to my attention: since this is telemetry there should probably be additional scrutiny about the privacy-related aspects of this proposal. You've indicated that there's a privacy & security section but I think we'd like to see more detail here. 

From @cynthia : If there's an extension that modifies the website or runs any extra scripts on the website that will trigger a potential leak of some information about the user. 
```

### Plenary Session - [2022-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20220720T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Lea, Yves, Hadley, Max, Rossen
Regrets: Sangwhan, Amy


#### Breakout Rollup

Dan: we didn't get to multiscreen window placement; likewise prefers-reduced-data; likewise focusgroup; likewise popup API

Lea: on focusgroup - 

Dan: [`aboutsignal.any()`](https://github.com/w3ctag/design-reviews/issues/737) 

Lea & Peter: can close

**lea to leave closing comment**


Other things we didn't discuss this week:

https://github.com/w3ctag/design-reviews/issues/670

https://github.com/w3ctag/design-reviews/issues/712

Lea: It's implemented in firefox, it's in chrome... Web developers are desperate for it.  

Dan: Although we haven't had a chance to do a thorough review we all know something about it.  

Rossen: those in CSS group know a lot about it.  We wanted someone who isn't in CSS to review it. To lea's point this is a huge feature and builds on grid which is bigger - part of the core layout system.  If you want go deep and validate the use cases & solution it's a good excercise. Not the deep dive.

Dan: no body is aware of arch issues with it - we know developers are keen on it. I think we should close this one off and prioritize our time elsewhere.

Lea: Yes!

Rossen: we have good understanding of what the use cases are and that they are addressed by subgrid.

Lea: *i will leave the comment* I don't think we're not reviewing it. A lot of us have looked at subgrid and don't see anything wrong with it. no architectural concerns. No contra-indication.

Dan: I haven't seen any evidence that there are any issues.

Lea: it would have been nice to have an explainer instead of just pointing to MDN. I don't think it's sufficient to keep the issue open.

Dan: I saw we close. Any opposed?

**consensus to close**

```
Hi there,

We looked at this today during our plenary and we have no objection to moving this feature forward. Some of us are very familiar with the work, and some of us are very familiar with the strong developer need for this feature and its multi-stakeholder support. While we did not do a deep dive on it in the TAG itself, we do not see any architectural concerns and are happy to see this move forward.

In the future, please include explainers with review requests. While better than nothing, an MDN article is not a substitute for an exaplainer, as it doesn't satisfy all requirements for what an explainer needs to contain. E.g. not every MDN article includes use cases, and this one does not.
```

**reviewed and agreed**

https://github.com/w3ctag/design-reviews/issues/727

Dan: Yoav has pinged us. we need to do this. I put it on for the f2f.

https://github.com/w3ctag/design-reviews/issues/734

Rossen: I felt like this one is ready to go.

Peter: still the question of whether it should be async. 

Rossen: will put on the agenda for CSS call.

##### [`response.json()`](https://github.com/w3ctag/design-reviews/issues/741)

Lea: we can wait for external feedback.

Dan: WebXRraw camera access <- closed and a good example where we have had an impact.

Rossen: seconded. 



#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
