# TAG Teleconference
#### 26-28 September 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-09-26](https://www.timeanddate.com/worldclock/converter.html?iso=20220926T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

### Breakout C (APAC / Europe) - [2022-09-27](https://www.timeanddate.com/worldclock/converter.html?iso=20220927T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo
* [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman
* [Web Machine Learning Model Loader API](https://github.com/w3ctag/design-reviews/issues/759) - @cynthia, @maxpassion, @hadleybeeman
* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion
* [Secure Payment Confirmation (heading to Candidate Recommendation)](https://github.com/w3ctag/design-reviews/issues/763) - @torgo, @maxpassion
* [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman

### Plenary Session - [2022-09-29](https://www.timeanddate.com/worldclock/converter.html?iso=20220929T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Meeting schedule / workmode
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Rossen, Tess, Lea

Regrets: Yves


### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @atanassov

Tess: Rossen brought this to the CSSWG, so maybe we're done here?

... last time we looked at it, we came to the conclusion the most important thing to do was to follow up with CSS wg... Rossen brought to CSS WG. They're discussing. Not the TAG's role to do the spec work. 

Peter: Shall we close it?

Rossen: I'm fine with closing it.

Peter: how does it tie into getting Houdini task force up and running?

Tess: last week we talked about batching & flushing.. a notion that this was something Houdini could take up. Low level parts of CSS that historically not descibed in documents... actually in Houdini's wheelhouse?

Rossen: on one side I agree.. on the flip side, internal details of css ... if we don't continue to force those discussions with CSS WG.. might not be more expedient...

... some commitments by CSS WG members made. 

Tess: maybe we can just wrap up.

**agreed to close**

Peter: several new APIs where people are synchronously flushing layout / style - we kind of want to extend into a generic design principle.

Rossen: do we have a design principle that says "avoid sync api"?

Peter: we have an open issue - avoid sync apis that cause style / layout flushing. https://github.com/w3ctag/design-principles/issues/388

Rossen: I think we can write this -  we can give some examples.

Peter: we don't have a good defintion of what it means to flush layout or style. I agree we can have the principle w/o a def.

Rossen: as a path forward

**issue added to next week**

### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Lea: we gave feedback - "for example do x"... They posted some updated notes.  It's basically that idea... 

Dan: minded to close it...

Peter: share your concern Lea that they shouldn't just adopt our suggestion...

Lea: i think there is a difference between web sites that load and that's it, and continuously downloading web sites... if you have high capability you want to get the higher-capability content at that point... what is there right now serving not either of those use cases?

... "if it's in high data mode and it switches to low data mode then apply a change if other way then do nothing"

Rossen: that sounds like a poor choice - e.g. a video call if you start in the outskirts of the city then you get better connection you don't want better quality?

Peter: understand but for video streams thats a bit of a red herring because video streams are adaptive.

Dan: WebXR environments?  More connectivity e.g. web socket connections when you have a high data connection...

Rossen: we're trying to descretize the switch events... if it happens every 10 seconds that's disruptive.  if it's once a minute then .. makes more sense... 

Rossen: a timer for changing state... 

Peter: one of our original concerns -- are people who use this feature design it so their page will still work in a mixed mode?  Half-way through and it changes... will page just break? 

Lea: i think a mixed mode concern only happens when they use the JS API. With media query it will be automatic... 

Peter: if I'm on a high bandwidth mode then I switch to low data - so the page loads all the low data versions...

Lea: that was the basis of our original idea...

Peter: the other thing - we don't need to define it... so we should push back.... "Thanks for taking our feedback on board but..."  **I can write the comment.**

*no consensus to close at this point*

Rossen: the timer thing is an idea... not sure if they talked about it... 

Peter: they are saying they're not just taking what we're doing... not clear if it's a resolved decision...

Lea: problem with mixed mode, problem with having different resource if it changes, problem with...

### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Rossen: we did have a chance to talk about this during TPAC... we did talk about the evolution of the Popup API.. started as an API.. they made it into an element... they took it and went down attribute path... we raised a flag about this... tl;dr their position - they want to rescope the attribute to which elements it applies to do be closer to ARIA type button. AAM spec. mappings between HTML layer and assistive tech tools... In that table there is an actual set of elements to which that ARIA role applies.  Attribute which wires up everything else... makes good sense. One pushback I gave: go think about what it means for elements that may be in non-visible areas... one of the problems with ARIA (e.g. describedby) you can have something in a non-visible part of the doc still descibed... requires traversals of the content tree and the layout tree... that's still a concern. Their action is to go back to Mason and discuss A11Y feedback and define the subset of elements to which the attribute will apply.

... what we need to do ... if they scope it to specific set then it comes back to us to debate whether ... from a A11Y pov ...

Lea: it still makes for a less nice API... having a separate element would make markup more readable... would allow for easier use on JS side. 

... having to pick which elements would be appropriate .. in most cases you just want a simple container.

Rossen: if you want to redesign these UI behaviours then it's a primitive you need.

Lea: you'd still have a pick a DIV to put the attributes ... to create e.g. a toast.  Are there any use cases where you woulnd't use a DIV?

Peter: custom elements.

Rossen: also the fact that showPopUp and hidePopUp bound to attribute... what if element a has showpopup and element b...   they had some response to this concern...

Lea: even if you scope to specific elements they produce a global namespace.. they all need to have popup prefixes... seems less elegant than a separate element. Balancing the concerns on both sides my pref would be a separate element...

Peter: concern about poluting the namespace. There is only one attribute popop that makes something a popup.

Lea: a lot of metatdata attributes... 

Peter: i don't see anything other than popup in the current doc that goes on the popup itself.

Rossen: yes...  

Peter: others that come into play like autofocus...

Lea: in the API side there's showpopup and hidepopup methods...

Peter: they only get added to an element when it has a popup attribute.

Rossen: yes.

Peter: any examples elsewhere of attributes that add or remove methods?

Rossen: yes i was asking that as well.

Peter: seems weird.

Lea: in every other case you'd have throw or return emtpy values if they don't apply.  

Peter: methods added to element that takes the popup element. .. no comon bases class. 

Rossen: right.

Peter: just for clarity it means if DIV can take popup attribute then all DIVs will have those methods.

Lea: which leads me back to the proposal of having it be an element.  Better for A11Y.  No precedent for this.  THer's no dialog attribute hung off DIVs...

Rossen: we suggested we didn't want an element.

Lea: we had concerns but upon seeing the alternative it's worse.

Rossen: maybe we should ping Mason to have a higher bandwidth meeting?  We should invite him and others... they have subsequent proposals chaining on this.  I will reach out.

### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman


## Breakout C

Present: Max, Dan

Regrets: Sangwhan, Amy


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

### [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion

**some work on miniapp feedback doc - Max & Yves happy with it - Dan will bring over to github so we can discuss & agree at the plenary**

### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

### [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman

### [Web Machine Learning Model Loader API](https://github.com/w3ctag/design-reviews/issues/759) - @cynthia, @maxpassion, @hadleybeeman

### [Secure Payment Confirmation (heading to Candidate Recommendation)](https://github.com/w3ctag/design-reviews/issues/763) - @torgo, @maxpassion

Max: basically this proposal is to secure the playment request web webauthn proposal... extension enhancement with webauthn protocol... I looked at the explainer.. They summarized the issues this proposal has - security considerations, cross-origin auth mechanism... analysis that there may be security risks... Also from a design perspective they have analysis that this security payment confirmation - mechanism is designed ... may not be a good design choice because not a payment method... But easier way to do this...  In general looking at their explainer they summarized well.  Maybe they need our input on the design choice.

<blockquote>
Thank you for this review request and for the comprehensive information you've put together in the explainer.  As we've previously positively reviewed Payment Request and Web Authentication we're happy to see these being brought together to make the web payment user flow easier.  The use cases and user needs are well documented.  It's also great to see the results of the experiment written up here.

Regarding the [design choices you've made](https://github.com/w3c/secure-payment-confirmation/blob/main/explainer.md#why-use-the-payment-request-api) to implement this as a payment method: we're concerned that this may be confusing to developers. Would the alternative approach (`navigator.credentials.get()`) be better from a developer ergonomics PoV? If so, it may be worth the effort to coordinate with the webauthn working group.
  
Regarding the privacy risks enumerated at the end of the explainer, can you include more specific mitigation advice for implementers on how to mitigate against these potential attacks?
</blockquote>

### [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman


## Plenary Session

Present: Dan, Max, Peter, Tess, Yves

Regrets: Hadley, Lea

### Meeting schedule / workmode

### Breakout Rollup

#### Breakout A

Closed 489. 705 Peter owes comment. 

#### Breakout B

#### Breakout C

Dan: we talked about miniapp and agreed a [response document](https://github.com/w3ctag/design-reviews/blob/main/reviews/miniapp_packaging_feedback.md)

Yves: status of [universal links on IOS](https://developer.apple.com/library/archive/documentation/General/Conceptual/AppSearch/UniversalLinks.html)... [and android](https://developer.android.com/training/app-links) might be another solution if security folks are OK with it...  Ensures you're talking to the right server..  Ensuring as a person creating an app that does banking that you're not impersonating another bank... 

**we agree to ship the doc as is with another sentence making reference to other solutions in market**

Dan: Payment request

**we agree to close based on [Ian's response](https://github.com/w3ctag/design-reviews/issues/763#issuecomment-1259894033)**

#### [754](https://github.com/w3ctag/design-reviews/issues/754)

Max: I left comment and they replied - they only support half duplex mode - the full duplex mode mentioned in a note. When the full duplex streaming mode implemented... There should be more issues between compatability between different versions. 

Tess: I think I found the update... if you look in the document for "caveats" look at the para before... 

Tess: could be "currnetly web applications can't upload web data sets without knowing the data set up front..."  I feel the request [for user needs] isn't an unreasonable one.

<blockquote>
Hi @yutakahirano thanks for the updates. We'd like to see more detail on the user need and expected use cases for this. For example "Currently when users need to do xxx the situation is yyy. This creates problems because zzz. This technology solves these problems by qqq."  This should be at the top of the document explaining what the new technology proposal is.  We're also reviewing the API and we appreciate your feedback regarding the modes.  Also thank you for going through the security & privacy questionnaire and providing answers. Can you bring this document into the same repo as the explainer please (rather than a google doc)? 
</blockquote>


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

https://github.com/w3ctag/design-reviews/issues/761

Peter: do we need to review?
