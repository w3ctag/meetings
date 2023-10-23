# TAG Teleconference
#### 16-18 October 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-10-16](https://www.timeanddate.com/worldclock/converter.html?iso=20231016T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Extending the PointerEvent with Unique DeviceId Attribute](https://github.com/w3ctag/design-reviews/issues/880) - @torgo, @atanassov
* [`form-sizing` CSS property](https://github.com/w3ctag/design-reviews/issues/890) - @LeaVerou, @rhiaro
* [The CSS `word-break: auto-phrase` property](https://github.com/w3ctag/design-reviews/issues/891) - @rhiaro, @atanassov
* [FedCM API extension: Error API, AccountAutoSelectedFlag, HostedDomain and Revocation API](https://github.com/w3ctag/design-reviews/issues/893) - @hadleybeeman, @plinss
* [Relative Color Syntax (RCS)](https://github.com/w3ctag/design-reviews/issues/894) - @LeaVerou, @torgo, @rhiaro
* [Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @rhiaro, @plinss
* [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman
* [Feature detection for supported clipboard formats](https://github.com/w3ctag/design-reviews/issues/901) - @LeaVerou, @torgo, @rhiaro
* [Side Panel](https://github.com/w3ctag/design-reviews/issues/903) - @plinss, @atanassov
* [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov
* [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @cynthia, @LeaVerou

### Breakout C (APAC / Europe) - [2023-10-17](https://www.timeanddate.com/worldclock/converter.html?iso=20231017T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman
* [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @cynthia, @torgo
* [DisplayMediaStreamOptions monitorTypeSurfaces](https://github.com/w3ctag/design-reviews/issues/892) - @cynthia, @hadleybeeman
* [Web Audio API: User-Selectable Render Quantum Size](https://github.com/w3ctag/design-reviews/issues/895) - @ylafon, @maxpassion
* [Tag review request for the "Dubbing and Audio description Profiles of TTML2"](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman
* [Standardizing Security Semantics of Cross-Site Cookies](https://github.com/w3ctag/design-reviews/issues/904) - @torgo, @ylafon, @hadleybeeman
* [CSS `text-spacing` property and its longhands](https://github.com/w3ctag/design-reviews/issues/907) - @ylafon
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

### Plenary Session - [2023-10-18](https://www.timeanddate.com/worldclock/converter.html?iso=20231018T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Yves, Hadley, Dan, Rossen

Regrets: Amy


### [Extending the PointerEvent with Unique DeviceId Attribute](https://github.com/w3ctag/design-reviews/issues/880) - @torgo, @atanassov

Dan: not concerned about persistent device IDs... because it's session scoped.

Rossen: is this part of webapps?  Why are they starting with WICG?

Peter: explainer says the expected venue is WICG... 

Rossen: pointer events - where is it?

Peter: not sure where current status is....

Peter: pointer events wg still exists and charter expires end of this month... 

Dan: the design?

Rossen: the motivation makes total sense –being able to recognize multiple input devices in a session - makes a lot of sense.  Pen... gaze... other ways of interacting... The thing that I'm trying to get from the use case... 

*we look at the [example](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/PointerEventDeviceId/explainer.md#usage) provided in the explainer*

Rossen: so it's really just a device id and nothing else - no additional context - you can't treat the input differently... 

Dan: you wouldn't be able to determine if a given device is a pen, etc...

Rossen: no - so if you resume editing of the same document you wouldn't get the same context... 

Dan: IDs are ephemeral...

Rossen: so if session restarts your colors assigned might swap...

Rossen: in your session - in this use cases - you would have a device and a color ... mapping. That's all the context you have. 1 = blue, 2 = red. No guarantee when you resume your session that device 1 will be the same device you had before... 

Peter: minor concern - on difference between pointer ID and device ID. "if the device doesn't support hardware ID then you have a new ID for every event..." And we also have interfaces on element... Just curious about how those values interact. Wondering about the difference between device ID and pointer ID... in the cases where the device does not have a hardware ID... then device ID would always be -1 and pointer ID would be incrementing value... But if it does have a hardware ID then PointerID would be stable... So (a) is pointer ID and device ID ever going to be the same and (b) why is't pointer ID just a flag saying the device ID is stable? So if you have multiple pens (e.g.) with no hardware IDs then they would all be listed as -1 ... so would this even be useful for devices without a hardware ID?

<blockquote>
Hi @sahirv - thanks for sending this our way. We discussed in our call today 

The motiviation (user need) seems to make sense.
  
We wanted to clarify - it seems there is no way to persist device IDs across sessions with the current design.  In your example, if your session is interupted your color assigned to each device might swap. Is that the intention?

We're also concerned about the usefulness of this for devices that don't have a hardware ID - since it seems they wouldn't be able to be differentiated within a session?
  
For devices with a hardware ID, would the deviceId be the same as the pointerId? If so, maybe this could just be a flag indicating that the pointerId is stable? If not, why not?
  
Also can you clarify where this work will end up for standardization. It seems that this belongs in the Pointer Events Working Group - but that group is due to close off in a month. Is the intention to open up this group again for further updates, or do you envision bringing this to WebApps or some other working group?
</blockquote>


### [`form-sizing` CSS property](https://github.com/w3ctag/design-reviews/issues/890) - @LeaVerou, @rhiaro

### [The CSS `word-break: auto-phrase` property](https://github.com/w3ctag/design-reviews/issues/891) - @rhiaro, @atanassov

### [FedCM API extension: Error API, AccountAutoSelectedFlag, HostedDomain and Revocation API](https://github.com/w3ctag/design-reviews/issues/893) - @hadleybeeman, @plinss

Hadley: it's 4 features - new additions to the FedCM API... the first 3 I don't think are architectural...
* when sign-in fails there's no notification - they want to fix - and sounds sensible - maybe we want to ask them if they want to reuse HTTP error codes? but it seems some of the errors are out of scope for http.
* make it easier for developers to see if you're on the reauthentication pathway - auto-reauth may be unable for reasons only the browser knows... developer might find they're on this pathway - they want to make that more obvious to devs. sounds sensible.
* for some FedCM instances a relying party might restrict to a particular domain - e.g. a corporate portal for employees of a certain company - they want to make it possible to bake that in. Part of what they are trying to do is make the failure case clearer to the user. Sounds like some of that might be taken care of by the first feature - but thus-far don't think it matters from an arch perspective.
* allow revocation... when as a user you're signed into a number of IDPs... and you want to revoke one of them - the revocation flow. difficult if you have multiple IDs with a single IDP linked to a given RP...

Peter: So far agree with everything you've said... 

Hadley: will let them know none of the changes seem architectural and we will close.

**agreed resolution satisfied**

Peter: I agree - there are a number of small issues with FedCM but in general seems they are doing a good job.

### [Relative Color Syntax (RCS)](https://github.com/w3ctag/design-reviews/issues/894) - @LeaVerou, @torgo, @rhiaro

### [Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @rhiaro, @plinss

### [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

### [Feature detection for supported clipboard formats](https://github.com/w3ctag/design-reviews/issues/901) - @LeaVerou, @torgo, @rhiaro

### [Side Panel](https://github.com/w3ctag/design-reviews/issues/903) - @plinss, @atanassov

Peter: i've seen it... 

Yves: is it related to document picture-in-picture?

Rossen: I think it's fairly different - intent is to allow you to have context between different apps... 

Dan: this seems like a browser feature...

Peter: being able to detect you're in a side panel.. maybe makes sense... Not sure how you would get into a side panel...

Rossen: any pwa that wants to do this... how do you do it? this is the propoosal they have to achive that capability in a pwa...

Peter: if I put in my manifest that yes I can go into a side panel - how would I then be put into a side panel? how would i request to be put into a side panel? I don't see that in the explainer...

Dan: they say in Non-goals that it's not from different origins- but the example they have shown appear to show 2 different origins...

Peter: the intention .. e.g. you click on an email link and email app appears in a side panel - those are 2 different origins...  I can see a need to target a side panel but I don't see that in the proposal...

<blockquote>
Hi! Thank you for sending this our way. We're not sure exactly about the use cases? You've listed a non-goal of displaying content from different origins but the example seems to show content from different origins. Also there's no specified way to target content to a side panel or to trigger content coming up in a side panel. Basically can you elaborate on the use cases a bit?
</blockquote>

### [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov

### [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @cynthia, @LeaVerou

### [EditContext](https://github.com/w3ctag/design-reviews/issues/416)

Peter: the listed issues don't seem to be addressing my concerns.. i will follow up with this and I will leave a comment.



## Breakout C

Present: Yves, Sangwhan, Dan, Amy

Regrets: Hadley, Max, Lea


### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman

Sangwhan: I met with the developers - they have heard our concerns but unlikely to be addressed.  Concerns were mainly about user agent controls being completely removed when the permission has been granted.  Dragability and resizeability goes away... No way for user to claw that back - except by going into browser settings and revoking the permission... That's not great - one particular thing - unmovable modal dialogs - accessibility issues. How they plan to use this - have the virtualized desktop environments - a super fancy remote desktop.  Idea is that all the windows from your remote desktop brought over to your local desktoip as separate windows... Like parallels or vmware - remote applications casted to your local OS as if they are local applications...  Dragability is determined by the OS on the other side... e.g. Photoshop on remote desktop - it will say "you cannot drag that window" and native dragability should not be able to usurp.

Dan: comparable to.. in the powerful apis breakout.. where yes there's a native capability but does it make sense for that native capability to be translated directly to the web. I kind of agree but I feel like the argument that comes back to us from people who are promoting the web as a competitor to native is that well native has it so we have to have it. This is a very good example of something that disproves that.

Sangwhan: ultimately I think this is an implementer decision. I don't see this proposal having any feature being standardised becuase there are so many unknowns when it comes to normative text. On top of that, the questions you have to ask about.. the reason for this powerful capability being a thing is because it's in a trusted environment - which is not a well defined paradigm. The application is from a vetted vendor, a managed browser.. none of these concepts exist on the web platform today

Dan: therefore it's chrome only, like the mangaged device api, or capture all the screens, not okay to standardise

Sangwhan: I suggested there's likely no future for this on the web platform unless a lot of boilerplate work is done to do with formalising the "trusted" browser or application concept

Yves: is it related to web apps can provide the fact you trust them?

Sangwhan: yes, hard dependency on that. How do they define what is a trusted application? It's a business decision, up in the air. What's on the table today, we can't support it. Consider this as a non web platform feature, or a proprietary api. Probably wouldn't cause serious harm from one implementer with the surface it has today, it's very specifically carved out. We wouldn't support, but not harmful.

Yves: "ambivalent" - we see the use cases, but they need to iron out details. Not something that should not be implemented, but needs more work. We don't want to see it on the web right now, but it's useful in the case of installable web apps

Sanwhan: depends on isolated web apps. Without that context it doesn't work. Also introduces new accessibility issues.

<blockquote>
Hi @sonkkeli we discussed today in our TAG breakout. We don't think this should be standardized in it's current form on the web platform. We understand the use case. However there is a dependency on the idea of "trusted" applications - and this is an area that is in development - e.g. [isolated webapps](https://github.com/w3ctag/design-reviews/issues/842) which we're also concerned with and is currently not stable enough for other things to be built on top of it. In any case, we are concerned with the lack of agency of the user - e.g. with dragability and accessibility issues.  We're going to close this review for now.
</blockquote>

**closed as ambivalent*

### [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman

**bumped**

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: they [responded](https://github.com/w3ctag/design-reviews/issues/875#issuecomment-1756356220).. 

Yves: the fact that app links are verified by apple to be able to reach the store, and we don't have that here. There is a verification step that you don't see in the end product but that happened by going to the store. So it has to be replaced in another way in the case of a regular web app [leaves feedback]. No response on webkit and mozilla standards positions.

### [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @cynthia, @torgo

### [DisplayMediaStreamOptions monitorTypeSurfaces](https://github.com/w3ctag/design-reviews/issues/892) - @cynthia, @hadleybeeman

### [Web Audio API: User-Selectable Render Quantum Size](https://github.com/w3ctag/design-reviews/issues/895) - @ylafon, @maxpassion

**bumped**

### [Tag review request for the "Dubbing and Audio description Profiles of TTML2"](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman

**bumped**

### [Standardizing Security Semantics of Cross-Site Cookies](https://github.com/w3ctag/design-reviews/issues/904) - @torgo, @ylafon, @hadleybeeman

Dan: sounds like they're trying to put some definition around what it means..

Yves: a way to standardise the behaviour between the different browsers. Sounds good to me.

Dan: apple and mozilla don't want to comment until it goes to webappsec

Amy: is this related to ~First Party~ Related Web Sets?

Amy: should they be starting the most restrictive definition instead?

Amy: we can say we support the fact that you want to do this - come back to us when there is multi-stakeholder support.

<blockquote>
Hi @johannhof - We're supportive of the effort to develop concrete definitions around cross-site cookies.  We think it's vital that this work reflect multi-stakeholder consensus.
  
You mention that Apple and Mozilla have declined to comment until this moves to WebAppSec - and you've noted that it will be a working group Note.  However, a Note doesn't connote consensus of the working group and won't include normative content (testable).  So we're a little concerned that the intention is to deliver it as a note - as this might not represent multi-stakeholder consensus.
  
Has this work been shared with the Privacy Community Group? If so, can you share the feedback?
</blockquote>

### [CSS `text-spacing` property and its longhands](https://github.com/w3ctag/design-reviews/issues/907) - @ylafon

Yves: explainer is a google doc... needs i18n review more than anything else. Syntax seems okay, painful to parse but should be deterministic

<blockquote>
Hi @kojiishi thanks for that – we're reviewing this morning and largely happy with the proposed syntax. Can you also let us know more about the status of this work in the CSS working group and multi-browser support. Are there webkit and Mozilla standards positions on this? Can you also let us know about any W3C internationalization review if this has happened?
</blockquote>

### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

Amy: new information is that it's gated on this attestation mechanism - so google is the gatekeeper on who gets to use it... which seems problematic...

**draft - to be completed at plenary**

<blockquote>
Hi folks - We're planning to close this as the concerns raised by us and in the [Mozilla standards position](https://github.com/mozilla/standards-positions/issues/646) have not been addressed. We're also noting that there is lack of multi-stakeholder feedback/support. We are sympathetic to the need to replace some of the functionality lost with the removal of third-party cookies; in this case we think it'd be better to address the use cases individually, with designed-for-purpose approaches, rather than adding a single underlying mechanism which has the potential to re-introduce the risks that the removal of third-party cookies were intended to mitigate in the first place.
   
We're a little concerned by the addition of the attestation mechanism [mentioned](https://github.com/w3ctag/design-reviews/issues/747#issuecomment-1690156498). Registering in order to use an API is not something we see having a place in the web platform. 

Please let us know if there are any significant changes in the design going forward that would mitigate the issues raised.
</blockquote>

**agree to close as unsatisfied**

## Plenary Session

Present: Peter, Dan, Amy, Max, Sangwhan

Regrets: Yves


### Breakout Rollup

#### Breakout A

##### [EditContext]()

Peter: i'm ok with their responses ---  Most of my feeedback to them was - how does this work if something with a DOM with ... the answered that. For the use case, it's fine.

Dan: so close?

Peter: I can leave a closing comment.

Dan: I agree to close.

#### Breakout C

##### Shared Storage

*we wordsmith the closing comment, above*

**agree to close**

##### Cross-site cookies

Dan: they got back from us.. it's a NOTE because the normative content will have to land in html fetch. Trying to build consensus early, so note is compromise. Had early discussions in privacy-cg. Positive verbal sentiment from browser reps in meetings.

Dan: has to be consensus to publish something as a note, but definitely seen WGs publish notes that don't have consensus for the content. I'll mention that.

<blockquote>
Hi @mikewest I take your point. I have definitely seen examples where working groups have published Notes that contain content that some working group members would have objected to had it been in a Rec. But I think it depends on how the wg operates. 

@johannhof thanks for the explanation and the pointer.

We're generally OK with the approach (and the effort to agree this fundamental definition across browser engines) and we'd like to see this work move forward. Please come back to us for a re-review when this is further along and the consensus-blocking issues have been resolved.
</blockquote>

**closed with satisfied-with-concerns**

##### [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889)

Dan: media wg.. because it has to do with codecs. They have listed firefox and safari as n/a.. not clear why from the minutes they linked to

Amy: they are asking a specific question they want guidence on

Dan: need to research more into web codecs..

Sangwhan: this is not about a proposal, this is asking us for an opinion on a particular pattern. A missing principle. 

Dan: presumably they will need to deal with multistakeholder.. just found it weird to see n/a.. if they think it doesn't require consensus.. feel we should ask about that even if it's tangential

Sangwhan: disagree in this case. It's not a proposal yet. They want our guidance then go back to the WG, iterate, then the multistakeholder discussion will happen.

Dan: okay

Sangwhan: the problem is around trying to be consistent vs usable. have to think about this. Transferrable objects... we don't have a recommendation for how to approach these things. I believe they copied existing patterns and what they're asking is it doesn't quite work well for them. Related to concept of [transferable objects](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Transferable_objects) - transfering objects across process boundaries... 

Peter: saying they don't really need the full pattern but maybe it's okay?

Sangwhan: something for us to think about. The transferrable objects paradigm is designed around being able to transfer objects across process boundaries, underlying implementation wise. For web codecs you're not crossing process boundraies, just thread boundaries. Which has a completely different implication.

Dan: they talk about transferring objets that can only be accessed from one thread at a time.. are they really talking about transferring objects between processes?

Sangwhan: the initial concept was created for processes boundraies, created for workers. When you transfer an object from the main thread over to a worker that crosses an entire boundarie of a process, tricky to do lock/unlock. Execution context is on thw orker side. Unless you do something like shared memory to sync across two processes, which is a nightmare.. you want to just hand it over. What they're seeing here.. will have to check.. I think webcodecs is just a thread transfer, so you don't need the compelxities surrounded around transferrable objects because it's not as complicated.

Peter: that's an implementation detail right? Couldn't it be a process boundary at some point in the future in someimplementation?

Sangwhan: right.. coudl be.. but we don't have a pattern that distinguishes process and thread boundaries or provide the ergonomics that are necssary. Transferrables are not nice. 

Peter: also think we shouldn't be exposing the fact you're crossing a thread or process boundary in a web api. Can explain this as nothing more complicated than... you don't need the data any more so we'll clear out your reference to it and you don't have to worry about copying the data. Whether it's process boundary or something else the consumer shouldn't have to care. Agree we don't have a good way fo doing that in a way.. this isn't a Rust API where we're handing ownership of this object. 

Sangwhan: not something the language supports well. We're retrofitting this mechanism through api surface, it's sort of ugly

Peter: yeah. I see maybe inventing some wrapper object instead of the array buffer, make a transferrable object, give the array buffer to that, pass the object..

Sangwhan: right

Peter: I don't think adding an extra boolean saying we're transferring this as a separate flag is any better ergonomically than the array. The array is clumsy but the boolean is not extensible or obvious what's being transferred

Sangwhan: the boolean itself.. depends on the api might not be adequate

Peter: yeah. And if they ever extend the api ..

Sangwhan: if you have a constructor where you're talking an object initially, the boolean at the top level is it inside the dictionary that goes into the constructor..

Peter: never used this but in post message.. you're sending one object then an array of trnasferrable objects. Presume they could be things referred to by the original object? I could be passing an object that has 3 properties, two of them are in the transferrable list. Deep copy of the whole thing exceopt whatever is in the transferrable list is going to get moved instead of copied

Sangwhan: yeah. Array approach is also not nice

Peter: it's not, but it's what we have

Sangwhan: I think they're okay with following that pattern but I suppose they reached out to us because it smelled funny. When the ergonomics of an existing pattern is sort of off. I think it's something we should think about and possibly provide architectural guidence on how to improve this going forward. It's very hacky.

Peter: my thoughts. If their question is should we use a boolean or a transfer list, betweent hose, use a transfer list. But even better would be .. not their problem to solve, but us and/or a task force to come up with a better design for how to do this in the future.

Sangwhan: realistically us and TC-39 kind of problem

Peter: yeah

Sangwhan: you would want to encode.. ultimately move syntax into a language without pointers or memory managers

Peter: who is our current liason with tc39?

Sangwhan: Dan Erinberg(?)

Dan: I can raise this with Dan tomorrow

Sangwhan: I will also message him privately. I think this should be a larger group discussion. It is a problem. We and tc39 should come up with a problem statement and straw proposal. For the time being my recommendation would be to use transferrables for now. [will leave comment]

Peter: +1 we don't ask them to invent a better mechanism, but we should try to get one designed

Sangwhan: We definitely don't want a one off case for this


### Solid charter review

### Issue Triage
