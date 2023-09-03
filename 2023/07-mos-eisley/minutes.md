# W3CTAG VF2F "Mos Eisley"

### Session 01 A

Present: Tess, Peter, Sangwhan
Regrets:

#### [Missing guidance for handling steps that are run "in parallel"](https://github.com/w3ctag/bfcache-guide/issues/2)

See PR #3

#### [Add guide for "in parallel"](https://github.com/w3ctag/bfcache-guide/pull/3)

Tess: looks ready to merge except for merge conflicts. Will ask submitter to fix.

#### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786)

```
We've discussed and looked at this during our vF2F. The API surface/design, use cases this attempts to solve seem valid - and is articulated through a well-written explainer. 

The part that we *are* concerned about this proposal is more philosophical - the question that remains to be asked is whether exposing cache control going to work this time. If it doesn't this will potentially end up with a widely-used antipattern which eventually makes everyone's life difficult. This has happened in the past, and given how cache is a complex problem - there is a non-zero chance this will happen in the future. If the risks of (unintentional, e.g. "preventing cache on everything fixes a simple problem I have!" pattern for example.) misuse is higher than the gains of exposing this, then maybe this shouldn't be exposed. 
```


#### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776)

Sangwhan to post asking them to close, design has changed.

#### Triage of unscheduled issues assigned to at least two of us

##### [w3ctag/design-principles#101](https://github.com/w3ctag/design-principles/issues/101)

Too big for today

##### [w3ctag/design-principles#154](https://github.com/w3ctag/design-principles/issues/154)

Propose close?
Closed.

##### [w3ctag/design-principles#231](https://github.com/w3ctag/design-principles/issues/231)

Too big for the remaining time in this breakout

##### [w3ctag/design-principles#254](https://github.com/w3ctag/design-principles/issues/254)

Editorial

##### [w3ctag/design-principles#289](https://github.com/w3ctag/design-principles/issues/289)

Waiting for Lea's PR


### Session 02 A

#### [Sustainability of bundling & caching finding](https://github.com/w3ctag/caching-bundling-sustainability)

Tess and Peter agreed to to review and file issues offline


### Session 03 A

Present: Dan, Amy, Sangwhan, Max. 
Regrets: 

#### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831)

Dan: Ian has said web payments wg will be discussing in their 3-august call. Maybe we bump this to next week.

*bumped*

#### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845)

Dan: good to see notes on stakeholder feedback in the Explainer.  Also good to see that there is positive feedback on the basic concept. It's not clear how well this meshes with filesystems that aren't how chromium thinks about filesystems.. maybe android/chromeos.. It would be good to see webkit and mozilla standards positions on this.

Sangwhan: ...modern filesystems... 

Sangwhan: bfcache ... being put into the cache could break your lock... no way to do a lock override. You'd have to manually override but no API for that.

Dan: comment from [Fergal on bfcache](https://github.com/w3ctag/design-reviews/issues/845)...

Sangwhan: and what happens if you crash? API seems fine.

Dan: in the explainer they've mentioned positive signals from mozilla and webkit but the links provided are to a whatwg thread. No standards positions.

Sangwhan: I will add to my feedback.

#### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854)

Sangwhan: unclear what hardware they want to support with this

Amy: they list negative signals from Gecko and Webkit

Sangwhan: hareware that uses is is either industrial or 20 years old

Dan: often eg. if you talk to people at Intel they're talking about industrial things like tractors. Is this an industrial use case, or a maker community use case? Would be interesting to know. They're not talking about specific platforms or devices in their motivation.

Sangwhan: I have a multimeter that uses RFCOMM. It would be cool if that worked, but seems like a lot of overhead for the web platform.

Dan: why isn't this happening in the web bluetooth cg?

[digging into history]

Sangwhan: HID makes sense because webusb can't see it unless you kick it into a special mode, disconnect and reconnect. Serial makes sense because of how OS treats it. Web bluetooth for same reasons will not really make sense, if the device is paired it's paired as a serial port. I don't know how it would work if you did the pairing from the browser. Still would be OS pairing. Ultimately I'm unconcinced about use cases

Dan: we could ask them to be concrete about devices they propose need to be connected to the web.

Amy: there are a lot of use cases in the various standards position threads from people in the community

Sangwhan: very specific use cases with a lot of baggage for the web platform

Dan: sympathetic to use cases from maker community

Amy: [tantek's comment](https://github.com/mozilla/standards-positions/issues/336#issuecomment-678387813)

#### [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820)

Dan: good multi-stakeholder signals - it's shipped - although Chromestatus doesn't reflect the multistakeholder support.  We left feedback in Tokyo - no response.

Amy: they may need a nudge? [leaves comment]


    
### Session 04 A

Present: Dan, Max, Amy
Regrets:

#### [API for capturing all screens](https://github.com/w3ctag/design-reviews/issues/856)

*reviewing the [comments from Elad](https://github.com/w3ctag/design-reviews/issues/856#issuecomment-1639735184)*

Amy: the fact that it's constrained by admin allowlist suggets it needn't be on the web

Dan: like managed device api

Sangwhan: if another implmeenter is interested, they could converge and figure it out and maybe there's a path to standardisation. But probably recommend we say it's not part of the web

Dan: we said unsatisfied on managed device because of the use cases - not in users best interests, contravenes best interests of the user. Reasonable for us to give the same view. Unsatisfied. Adding as a configuration option on enterprise deployments for chrome, that's their business. 

Amy: +1

Dan: we can reinforce the user can't "just walk away", and making these policies harder to implement differentiates the web platform from other platforms 
[close and comment](https://github.com/w3ctag/design-reviews/issues/856#issuecomment-1659835130)

#### [WebUSB exclusionFilters option in requestDevice()](https://github.com/w3ctag/design-reviews/issues/865)

Sangwhan: This is one line of code - you set a filter "i want all the USB devices by this vendor... " - there's nothing to remove stuff - this functionality lets you do it. "All the google devices that are pixel phones" - looking for a specific port... Doesn't cause harm. Actually helpful.  Convenience feature...

Dan: previous concerns to do with interoperability and multistakeholder support, because there's lack of multistakeholder support for webusb. The best we can do on a webusb extension/change is satisfied with concerns. The one thing I find worrying is that they haven't really put together an explainer, just a github comment on the wicg thread, it's already merged. Agree with what you're saying and having worked with webusb I get what this is doing and it would be useful. Would have been nice if there was an explainer with the use cases. Is it worth asking for this?

Sangwhan: need a lightweight explainer template for them of some form... bullet point list of bare minimum to proceed

[discussion of explainer template for small deltas]

Dan: I would say this is:
* user needs
* brief explanation of what the delta is
* ...

Amy: can work on a "small delta" explainer template

Sangwhan: expectation that TAG is expert in many things... 

**closed satistifed-with-concerns**

#### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795)

Dan: no activity on multistakeholder. Some concerns from mozilla. Webkit negative from 2021. 

Sangwhan: on an old version

Dan: We reviewed and gave positive feedback on the fact they were referencing data minimisation principle in april.

Sangwhan: previous proposal was polling based, had a high granularity, not great usability. Privacy risks due to granularity - that's why webkit says it's a side channel. CPU architectures with a heterogenous setups (big and small clusters, modern intel cpus, atom cores, core cores, common). THe compute pressure, % aggregated, doesn't mean anything, in these kinds of configurations. But you can use those readings to create artificial workloads to create a side channel. A lot of that was saddressed by making it more coarse - high pressure, medium or low pressure, three levels or so. If you're in a high pressure situation a web application can choose to do things to improve the situation within their control, eg. blackground blur is a very expensive feature that video conferencing supports and uses a lot of cpu cycles - could black it out instead. Apps can reactively deal with this. Also reduces the side channel attack surface, but doesn't completely eliminate it. You can sync things - two origins. There are other ways to do this, not overly concerned.

... In low power mode, tell the application to use less energy, you can signal to the application. 

... It's a huge gap. If we want applications to be more advanced and considerate about resource consumption this kind of mechanism lets them do that. It benefits good actors. On the other hand, it benefits bad actors.. if a bitcoin minor is sitting in the background and sees 'idle' they can crank it up to medium and not get noticed too much. There's a tradeoff.

Dan: the other signals that are coming through.. the work is happening in devices and sensors. There's multistakeholder with intel and google. Privacy and security considerations section is good. Concerns around lack of multi browser support. But webkit's position was on the old version, so need to review the new version. No information from mozilla. We don't have current information about negative feedback on this version.

Sangwhan: good use cases in video conferencing

Dan: and in web gaming [proposed close satisfied with concerns] - concerns purely based on multiple browser support

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738)

Dan: fergal's [latest comment](https://github.com/w3ctag/design-reviews/issues/738#issuecomment-1621288141)

Sangwhan: fergal wants to have a consistent developer story with bfcache.  he's trying to find common ground and not getting support...  As a developer right now you have every motivation to avoid being bfcached because of the inconsistencies in implementations.  Similarly if we give developers control over bfcache - developers might choose not to cache... 

Dan: can we intervene to bring people together? ask for consistency. We want developers to use bfcache, it is good to have consistent behaviour from a developer perspective. What can we do to encourage that?

Sangwhan: reinforcing that it's good for the web to have consistency

Dan: there's not controversy about whether bfcache should exist, just the behaviour. For functionality where there's consensus that it should exist, it should behave similarly. An example is private browsing modes.

Sangwhan: bfcache is more impactful when it's user facing, and inconsistencies do more harm. Web application is half broken or reloads when you switch to a tab. Affects users a lot - should be a priority for the web.

Dan: what about adding material to the bfcache principle to reinforce this?

Sangwhan: that's easier than a finding

### Session 4 Wrap-Up

Dan: **on 738** what can we do to move this ahead?

Sangwhan: there is some misalignment on gloals for bfcache.. 

Dan: we don't say "ensure the web platform supports bfcache concistently"

Sangwhan: I don't think it should go in the principles...

Sangwhan: maybe a little blurb of text... in the principle... "consistency of non-fully active documents is crucial to user experience.  Consistency guanrantees a healthy where users won't be motivated to switch browsers..." If we have consistency that means there is a clear user & developer expectaion of what to expect when the document goes into non-fully active... Multiple implementations being the same will be beneficial to all implementations.

Sangwhan: hixie ended up documenting features... it's bfcache's turn.

Sangwhan: maybe a PR - & I will draft a short finding.

**we work on the "web is not versioned" finding draft from Sangwhan**

### Session 05 A

Present: Amy, Tess, Peter, Max
Regrets:

#### [New question on hidden metadata.](https://github.com/w3ctag/security-questionnaire/pull/138)

#### [Hidden' data question needed?](https://github.com/w3ctag/security-questionnaire/issues/130)

#### [Mention (capability) negotiation?](https://github.com/w3ctag/security-questionnaire/issues/122)

Tess: reocurring finterprinting debate. Might be a place to reference privacy principles. Prefers reduced motion; media capabilities. The job of putting text in the questionnaire is to be a prompt for thought. So the text here can be short. Also a capability negotiation review on the finterprinting guide.

#### [Add a section for preventing behaviours that are abusive toward users](https://github.com/w3ctag/security-questionnaire/issues/106)

Overtaken by Privacy Principles and/or Societal Impacts Questionnaire

#### ['mode' PR](https://github.com/w3ctag/security-questionnaire/pull/150)

Closing, not an appropriate change
    
#### [fix wide review link](https://github.com/w3ctag/security-questionnaire/pull/143)

merged

#### [error handling question](https://github.com/w3ctag/security-questionnaire/pull/140)

nudged
### Session 05 B

Present: Peter, Max, Amy, Hadley
Regrets:

#### [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818)

Profiles no longer a priority but they'd like input for the next charter. Asked if it's useful for one of us to join their meeting at tpac

#### [WebDriver BiDi](https://github.com/w3ctag/design-reviews/issues/869)

Peter: Not web facing, cross vendor support. Concern about patching html.

Amy: understand S&P doesn't apply necessarily but can't find any other kind of security assessment

Peter: does give the driver in the browser a lot more capabilities to know what's going on.. okay with that in this context

Amy: no use cases, only "customer scenarios". Even their ["end-to-end user scenarios" doc](https://github.com/w3c/webdriver-bidi/blob/main/roadmap.md) doesn't seem to involve actual users. Is there an accessibility angle?

Peter: I don't think I've seen use cases for building accessibility tools in the browser. Out of scope, but would be interesting.

Amy: thinking out loud about abuse cases

Peter: all already possible. Web Driver has been around a long time. Happy to close as satisfied.

Hadley: +1

Peter: curious about their modified version of json rpc

Hadley: should be in the explainer    
### Session 06 A

Present: Dan, Tess 
Regrets:

#### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

*working on finalizing this text*

#### [The `FileSystemObserver` interface](https://github.com/w3ctag/design-reviews/issues/868)

#### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616)
    
*changed to proposed closing*

Dan: propose resolution of ambivalent - somehting like "Since this has shipped but also it looks like additional work isn't going to happen, we're going to close this for now. We've left previous feedback - particularly around ad blockers - which has been listened to - thanks.  We don't have a definitive outcome. Lack of signifigant multistakeholder interest remains a concern."

**closed**

### Wrap-up Session

Present: Dan, Tess, Peter, Hadley, Amy

Dan: *recounting 616 proposa*

### Issue 839 - [FedCM](https://github.com/w3ctag/design-reviews/issues/839)

Peter: fine by me.

Peter: we talked about FedCM... some possibility of information leakage... and if the idp calls the api from an iframe and has to already know the id of the rp... how do they get that?

Peter: we need to find more info from them... i need to get better understanding...

Hadley: agree - also the both shipped in june in Chrome...

Dan: Shipping 116 - positive signals from Firefox.

Tess: nobody else shipping though...

Dan: should we get them on a call?

Peter: I will do some more research on it...  will leave some feedback on the issue.

#### [PR 290 on design principles](https://github.com/w3ctag/design-principles/pull/290) 

Tess: we're trying to talk about the failure scenario...  Been working on this for a while since breakout with Alice in Iceland.  Tension between implementability and interop.  Presumption of this text is "plan A failed" - weren't able to come up with a solution that worked for everyhone.  Describing the alternatives and their downsides...   So it's weird.  We've had tons of feedback.  We've addressed the feedback... 

Dan: I think we should merge.

Peter: I'm ok with merging *proviso one minor typo in markup*

**merged**

### Session 06 B

Present: Hadley, Amy, Peter, Tess, Dan
Regrets:

	
#### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839)

Tess: login status api integration into fedcm. Login status api is from apple. Need to see if it's..

Hadley: no status from safari..

Tess: Sam from google reached out recently about integrating login status api into fedcm. I don't know if anyone has had a chance to look at it yet. The use case should be solved. Devil in the details.

Hadley: having read the userinfo api I'm concerned about .. the general idea is that once you've already signed in it wants to be able to prompt you to continue on that site with what you already sign in with because the browser is going to remember.. 

...

... Looking at [invisible tracking problem](https://github.com/fedidcg/FedCM/issues/230) - says they're mitigating but can't see anything that stops a site using it

Peter: talking about the login button as a cross origin iframe controlled by the IDP but depends on 3p cookies.. so instead of having to rely on a cookie you can ask the browser directly. RP doesn't necessarily know that you've logged in.. and doesn't know who you are until you've logged in. But IDP knows you're visiting this RP even before you log in.

Hadley: that's the invisible tracking attack

PeteR: they're saying they mitigate by making it visible. But nothing saying it has to be visible. Ask for the information andthen just not present it to the user.

Hadley: true. Or user is supposed to click continue in order to proceed?

Peter: yeah but if the IDP is just rendering an iframe they could render anything they want. It's still going to track you, you've got all your user info, name, avatar, and not present it. Is there something in the browser to surface this information, or are we relying on the IDP to surface this information?

Hadley: looking at the fedcm explainer it looks like we're relying on the idp to issue a token that goes to the user agent. The ua has to check that

Peter: browser gets the token when you're logged in?

Hadley: so not whether you've been logged in previously?

Peter: I Think the browser only has the token once you have logged in. So in this case you don't have a token yet. I guess you're still logged into the idp but not logged into the rp

Amy: there's a lot of detail in their S&P questionnaire. I'm inclined to say these additions are fine.

Peter: they're aware of the tracking problem and they think they're mitigating it but I'm not sure if their mitigation is as effective as they think it is. Maybe I'm missing a detail.

Amy: worth leaving that comment to ask for clarification

Peter: reading that.. the idp already has this information.. if they fetch the information but don't surface it they haven't found anything they don't already know. Still seems weird.

Hadley: that's how I understand it. Fundamentally the RP should know that you've already been able to log in there..? although I guess it would know that through tracking which is not ideal

Peter: are theyt alking about the idp and the rp have collaborated out of band to track? Feel like I'm missing something [will ask the question]


### Session 07 A

Present:
Regrets:

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760)

### Session 07 B

Present: Peter, Rossen, Tess
Regrets:

#### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858)
Tess: First obvious feedback is that there are more than one type of cache. The opening paragraph is even explicit about that and at the same time it's hard to know how you would target a specific cache. It's unclear how you can use the capability to improve performance 

Rossen: left commet pointing the authors to the https://w3ctag.github.io/caching-bundling-sustainability/ effort for considering how it might affect their proposal.

#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)

### Session 08 B

Present: Peter, Rossen, Tess
Regrets:

#### [Early design review: scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/827)

Tess and Peter left feedback in April and have received no response. Closed as satisfied with concerns.

#### [Portable Network Graphics (PNG), Third Edition.](https://github.com/w3ctag/design-reviews/issues/873)

Closing as satisfied. 

Rossen: `We really like the proposed changes and overall direction of the spec. The details are somewhat out of our technical depth but we trust you and the WG to have captured the current state of implementations. Having spec text for APNG is particuraly great to see. Thanks for you working with us and we're excited to see how the spec matures.`

#### [Exclusive accordion (&lt;details name=""&gt;)](https://github.com/w3ctag/design-reviews/issues/866)

Tess: `@plinss, @atanassov, and I took a look at this during the TAG's vF2F this week. See their comments above for specific bits of feedback. Overall, we're really happy with the simple, incremental approach you've taken here to add this feature to HTML. It fits right in with the existing use of `name=""` for radio buttons and checkboxes, and it doesn't require authors to change the existing structure of their documents. Thanks for bringing this to us for review!`
	
#### [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840)

#### [ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/863)

### Session 9 A

Present: Dan, Amy, Max, Hadley
Regrets:

#### some discussion of [Web Integrity](https://github.com/RupertBenWiser/Web-Environment-Integrity/blob/main/explainer.md) proposal.

Dan: just noting this has not yet been submitted for TAG review yet.

#### [TAG spec review of Bounce Tracking Mitigations](https://github.com/w3ctag/design-reviews/issues/862)

*we spend some time reviewing the explainer*

Dan: good to see no dependency on FPS.

Dan: interesting to ✨ that - in ack section - lists other browser behaviour that is "aligned" with this proposal. So it's aligned but no specific feedback from those stakeholders... what do they think of this proposal?  

Dan: this is happening in the privacy CG...

Amy: I think this looks good and we should ask them to ensure other browsers are aligned on this approach.  I presume they looked at what other browsers have done..

Hadley: that's what they've said in the intro.

Amy: this looks like things that are what a user agent should be doing, as an agent for the user

```
Hi @wanderview @amaliev @jyasskin. We (@torgo @hadleybeeman @maxpassion and I) reviewed this in our virtual face-to-face this week. We're really happy to see this being worked on! The design looks good and well aligned with the [privacy principles](https://www.w3.org/TR/privacy-principles/). 

What feedback have you had from other browsers in the PrivacyCG? It's great to see that you feel the proposal is aligned with what other implementers have done, and we would be even happier to see other implementers collaborating with you on documenting this behaviour – which would give clear guidance to web developers. ✨

We're looking forward to hearing more about your progress going forward. What are your thoughts about your next steps?
```

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342)

Dan: not sure if there are recent updates to the spec

Hadley: looking at the [I2S thread in Chromium](https://groups.google.com/a/chromium.org/g/blink-dev/c/7_6JDIfE1as/m/wModmpcaAgAJ)... they stopped at the end of June - their metrics analysis identified an issue in "core web vitals" - pausing the roll-out.  Problem for them but .. hard to tell.

Amy: so should we give feedback on FPS specifically - looking OK as a standardized registry - but with warnings of what you use it for?

Hadley: fps rsa4 dependency?

Amy: for rsa4 they have gates... and fps can be used as one of those

Hadley: they do also say you could gate on user prompts... leaving the door open for other possibilities...  

Amy: We asked these questions... about rsa4 - i'm wondering if there's something we can do to move fps on from our pov...

Hadley: we can ask why it's stalled and what they're learning.

```
Hi, we are looking at this at our TAG f2f. We're noting a pause in the I2S -- can you tell us more context about this and how any consequences might impact the design of FPS, especially any of the aspects we've discussed in this review?
```

Amy: also noting [their issue 167](https://github.com/WICG/first-party-sets/issues/167) - feedback from people working with early implementations... so they've shipped something.

#### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808)

We're waiting to hear back from them in September.

```
Hi all. We've looked at this during our W3CTAG f2f. We are still hoping for replies to our previous two comments from @plinss and @cynthia. Any thoughts?

```

#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726)

#### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747)
    
    
### Session 10 A

Present: Amy Hadley Dan Max
Regrets:

(See 12A for EWP issues)

#### [Add an acknoledgements section](https://github.com/w3ctag/ethical-web-principles/issues/96)

Dan: reached out to people who have us early feedback. Some are happy to be named in acknowledgements section. Haven't had responses from some. 

*we reach out to Olu and Chris*

#### [centralisation is bad PR](https://github.com/w3ctag/ethical-web-principles/pull/95)

*We agree that this is already covered in [2.8 The web must enhance individuals' control and power](https://www.w3.org/TR/ethical-web-principles/#control) and no additional principle is called for, however we will ask the Pete if he has requested wording changes to that principle.*

*We agree to close this PR but leave the issue open for now.*

#### [information integrity pr](https://github.com/w3ctag/ethical-web-principles/pull/93)

Amy: I like additions about determining trustworthyness, but this is more words than necessary

Dan: removes "origin". I like the rewording of the principle

Amy: but not the change from must to should. Verifying information and determining trust are two different things. Can we have both?

Hadley: they are two different things. And we need to keep origin and source, we refer to them often.

[worked on refining the PR - almost ready to merge]

#### [Link to EWP](https://github.com/w3ctag/societal-impact-questionnaire/issues/1)

### Wrap-up

Present: Hadley, Dan

#### [ewp decentralization text](https://github.com/w3ctag/ethical-web-principles/issues/94)

```
Hi all. We thought carefully about this topic when we wrote the first draft of the EWP, and — as you can imagine — it has come up a lot in the ensuing revisions.

We have written each principle to be about the ethics, with the technologies in the explaining text. The ethical issue that underpins centralisation is the power imbalance: when pieces of the web are centralised, it means that individuals or small parties lose power in comparison with the centralising power. 

We wrote that up in [2.8 The web must enhance individuals' control and power](https://www.w3.org/TR/ethical-web-principles/#control):

> We recognize that web technologies can be used to manipulate and deceive people, complicate isolation, and encourage addictive behaviors. We seek to mitigate against these potential abuses and [patterns](https://en.wikipedia.org/wiki/Dark_pattern) when creating new technologies and platforms, and avoid introducing technologies that increase the chance of people being harmed in this way. **As part of this, we favor a decentralized web architecture that minimizes single points of failure and single points of control.** We will also build web technologies for individual developers as well for developers at large companies and organizations. The web should enable do-it-yourself developers.

We also wrote that we *favor* a decentralised web architecture, instead of saying that we will only accept one, because — as @mnot points out on the PR — DNS is relatively centralized and yet is a pretty functional part of how things work right now. We aren't intending to condemn it.

@pes10k, with all that in mind, if you would like to try to strengthen the text in principle 2.8, we would appreciate any suggestions. 

In the meantime, we are closing PR 95. 
```


#### [find a voice](https://github.com/w3ctag/ethical-web-principles/issues/79)


    
### Session 11 A

Present: Hadley, Tess, Dan (second half)

Regrets:

(Overflow from 9A)

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838)

Tess: this feels like it should have more use cases. 

Hadley: payments? The shopping site needs to know that the transaction has gone through. And 

Tess: yes. what about an ebook reader. Contents of the epub are web content. I don't think there is a need for the ebook to communicate with the reader app/website -- Js in the book does not need to talk to the website. Although, it could be the same site... though it could be google.com and googleusercontent.com, where they isolate untrusted content that they didn't write. The site wants to pritect itself from the book. What breaks there? Scrolling, pagination. Can you read the book? Most are a document per chapter, so multiple documents. So how would you read the book? Not the book in a frame, i'ts a content document in the frame.

So the ebook reader needs too know that the reader has scrolled to the end, or pagination, etc.

Just thinking out loud about other use cases.

I suspect that the containing page needs to know info about the enclosed page, where it might be ableto get the info from the zip file, but not all. The metadata in the zip file doesn't know the screen size, the font size, etc. 

So I guess you can't use a fenced frame, because there is some info that needs to go back and forth.

The use case they're envisioning is adversarial, to prevent the adtech from learning info the shouldn't learn. Isn't the case in other use cases. In the books case, it's sort of adversarial -- I might purposely upload a malicious book --

Is there scripting, (which you could turn off). Maybe there is werid stuff you can do in CSS, which you could prevent with cross document loads 

Hadley: payments isn't adversarial in the same way... it's not that the sites don't trust each other, it's that I as the user don't want them to talk more than I want.

Tess: right. Stripe, as a white labelled service, are going for seamlessly embedding themselves in the page the user is using. The user shouldn't care. They offer multiple payment methods (apple pay, paypal, etc etc). As a user, I know that paypal knows stuff about me. I want to be able to tell by looking at my browser that paypal is in a different enviroment from the page, and I want to belive that that different visual means something about who has access to what.

But in fact, the paypal popup needs to know something about the thing you're buying

Hadley: or just the total?

[discussion about how these work]

Tess: Both of these cases show that the user expectation is coming out of...

[Enter torgo]

Dan: we could ask them about use cases in payment... 

Tess: We should ask "Are there use cases outside of ad tech?" - should be relevant to other cases ...

Hadley: and having it just for ads means developer complexity...

Tess: an `<ad>` element has always been rejected by the ad community bceacuse it would make ad blockers easier...  Carrots and sticks...  The carrot would be "if you don't use fenced frames, you don't get the data from your partition that allows you to do the targeting." that's a pretty enticing carrot.  If you're just designing for the ad case we might be missing opportunities... e-book also an interesting one.  e-reader needs to be able to inject style - impose user preferences like dark mode or font... so maybe not.

Tess: back when payments people working on payment handler they wanted payment handler to present a "sheet" that would be a payment flow... different from iFrame but similar to it... would this be sufficient for that?


```
Hi all. We are looking at this at our W3CTAG f2f. We had a long discussion about how the shape of this, changing the relationship between an iFrame and its embedding page — it must not be unique to the advertising use cases you've listed.

We brainstormed along the lines of a site presenting user-generated content in an iFrame, and the payments processes. Have you explored use cases out side the ones you're citing? And if so, what overlaps are you finding?
```

#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723)

```
hi @JensenPaul - we [understand](https://github.com/w3ctag/design-reviews/issues/838#issuecomment-1634120833) that this proposal has been renamed **protected audience** - can you confirm and let us know status? Should we keep this item open, or has the design changed so significantly that we should be opening up a new review?  If should keep this open, should we re-name this?  Can you update us on any dependencies we should be aware of?  Many thanks!
```

#### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846)

Tess: there's 2 approaches - event level and aggregate level - in both cases there are 2 or 3 competing proposals right now. I am hoping all the event level stuff coaleces into one approach and all the aggregate level stuff coalesces into another.  There is some skepticism from some PatCG participants about event level as a whole.  The "event" is the conversion - you click on an ad.  Does the ad provider get a report of the conversion or just an aggregate report?  Mozilla's pretty convinced that it's impossible to do event level with privacy preserving... Other people attempted to demonstrate with a mathematical proof that the amount of info exposed was riskier.

Dan: where does pcm fit?

Tess: PCM is one of the proposals for an event level solution?  It shares a bunch of API surface with google's thing. Possibly attribution reporting API?

Dan: yes, [that is where I left the feedback](https://github.com/w3ctag/design-reviews/issues/724#issuecomment-1148391588) a year ago about the different names of different things and asking if there is convergence.

In Feb Charlie Harrison from Google asked us to look at it again.

So this (the attribution reporting API) is Google's overall level proposal.

Private aggregation is also from Google, but we haven't commented on it yet. They are spliiting out the aggregation of the attribution reporting api and making it a new thing.

#### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823)

Tess: I think something along these lines is probably the right thing for aggregated reporting... 

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724)

### Session 12 A

Present:  Tess, Dan
Regrets:

(Overflow from 10 EWP)

#### [EWP PR 93](https://github.com/w3ctag/ethical-web-principles/pull/93)

Tess: *approved*

#### [voice](https://github.com/w3ctag/ethical-web-principles/issues/79)

Tess: we're beting put in a contradictory position - this doc from the TAG and it's just TAG's opinion but also elevated to a statement...

Dan: I think it's kind of "what the w3c community feels is an important aspect pertaining to the whole web" <- and wide review, plus acknolwledgements section that shows we have had early engagement with wider community should buttress this. 

Tess: the text of the doc itself should be broad, should focus on the web... we can add some status words "currently the TAG is working on this the intention is to develop into a w3c statement with wider community consensus."  

*we agree to leave the issue for now*

#### [relationship to design principles](https://github.com/w3ctag/ethical-web-principles/issues/37)

*looking at [https://github.com/w3ctag/ethical-web-principles/pull/84/files]*

Dan: [leaves comment on the PR](https://github.com/w3ctag/ethical-web-principles/pull/84#issuecomment-1662520019)

#### [be more specific on stakeholders](https://github.com/w3ctag/ethical-web-principles/issues/59)

Dan: is this actionable?

Tess: target audience is anyone working on anything at w3c... but people outside - e.g. people who work on frameworks - should read it too...

Dan: maybe we need an "audience of this document" that says that... concentric audiences - members of the w3c community, the wider web standards community, and the web development ecosystem at large.

Dan: [left a comment](https://github.com/w3ctag/ethical-web-principles/issues/59#issuecomment-1662531429)

Dan: I will do a PR...

#### [isolation](https://github.com/w3ctag/ethical-web-principles/issues/76)

Tess: rhetorically people opposed to improving privacy on the web have created false or misleading tension between privacy and other societal goods. The goal for that line is stop energy - stop improving privacy.  People shouldn't weaponize a single principle... e.g. improving privacy is bad for the environment.  So "sustainability" could be set up against privacy.   We need to not inadvertantly grant legitimacy to that kind of bad engagement.  

Dan: we could tell people it's inappropriate to pick out a principle alone to help in your argument.

Tess: but someone else could make the counter argument that you shoulnd't use privacy to harm the environment... We could inadvertantly encourage a certain kind of bad faith behaviour... 

#### [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851)

#### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843)

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809)

#### [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872)

### Session 13 and 14 A

Present: Rossen, Tess
Regrets:

#### [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851)

Propose close. draft text:

`Looking at the issue @hober during our virtual f2f and following all threads, we agree with @LeaVerou and are happy to resolve it. Looking forward to seeing this feature adopted and in use. Thank you for flying TAG.

@LeaVerou please close once you have a chance to confirm your concerns are addressed.`

#### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843)

Overall looks good. Unsure what "load" means in this case; do they mean Unix loadavg? If so, that doesn't work on Windows. Tess commented to this effect.

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809)

Tess to read & make comments.

#### [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872)

Rossen: to implement on windows, would require plumbing deep into the OS...
Tess: and what would this even mean on iOS?
etc.

Rossen commented with our concerns.

Hi @eladalon1983, looking at the proposal with @hober during our Aug 23 f2f, we have the following questions:

1. What is the expected behavior for OSs that have no cursor - iOS, Android etc.?
2. The intended effect assumes that the receiving UA will have the ability to change the lower layer OS cursors effects - is this possible? (For instance, we suspect this would be very diffcult on Windows.)
3. It is unclear how this feature will be available in different pixel densities, DPI, frame sizes etc.
4. What other alternatives have you considered? 
5. How does this featuere interact with the a11y stack given they usually have thier own virutal cursor?
6. Not a question but suggestion - we assumed that the spec is your explainer given the little information provided in the README that is linked as an explainer. Can you consolidate please?

#### [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853)

Neither of us is the right person to look at this; skipping.

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416)

Rossen to read & generate comments.

### Session 15 A

Present: Lea, Dan, Sangwhan
Regrets:

#### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842)

Lea: we have looked at it and replied to them... 


#### Possible Powerful Webapps Task Force

*discussion on possible charter - and ensuring composition of the taskforce is balanced*

Sangwhan: what are the missing gaps to make the web application platform appealing for developers and users?

Lea: "the web plaform needs xxx it should look like this..."  

Sangwhan: common demoninator of things that are missing on the web platform...

Dan: outputs?

Lea: right now we see explainers as something after the spec is written... what if this group writes the explainer... or proposals... for new API - requirements, user needs, high level sketch... Should be more concrete than "the web platform needs an API for this thing"... something at the level of an explainer.

Sangwhan: I've seen this kind of process used for web platform features - the product manager writes the problem statement...

Sangwhan: one important thing we want to get out of this - agreeing how to deal with state. File systems, interactions with the actual operating system... we should agree that it's a gap.  We should look at the usage of popular electron apps out there and understand why they're on electron instead of web... that should give us a list of things that should be supported by the web platform...  Isolated web apps is one way to do that - but how to provide the capabilities but not in as way where you have dangerous situations...

Dan: installability / trustability...

Lea: discoverability for users.. making the install process designed in a way that it's a clear process of trust. Right now the process is not discoverable. Also one reason people create native apps is that they can be in app stores and be paid for.

Dan: problem with WebAPK...

Lea: this discussion should be item number 1... don't see it as part of planning... 

Dan: I think "installability" should be one of the bulleted list of topics that are in scope...

Lea: something around app stores, etc...  Also more powerful APIs... file access, sensor access... 

Sangwhan: networking.

Lea: better hardware access...

Sangwhan: list of potential specs that people should be writing as deliverables that come out of this group...

Dan: Something that helps TAG [with reviews]...

Lea: Why do we need principles specific to this? Wouldn't any principles that come out of this fit better in e.g. Ethical Principles? I think there’s usually an underlying bigger picture principle. Let's take installability as an example. The underlying principle is that the user needs to give a strong enough signal of trust for an app to have access more powerful capabilities -- that fits better in the Ethical Princples. But also, you mention a laundry list of APIs, however  I think this kind of gap analysis is really important and not done right now. Specs are developed by the groups that will write them, in an ad hoc way, not as a coordinated effort. This results in the web platform not being cohesive enough to compete with native.

Sangwhan: we should have rough guidance on what to do about "secure-er" context... have to be distilled out after a list of things we agree to work on.

Dan: also noting prior work: https://github.com/mikewest/securer-contexts/ and https://www.w3.org/TR/secure-contexts/

Lea: being able to do cross-origin requests - should be something for the bulleted list.

Sangwhan: first set of deliverables... 

Dan: *yammering on about installability*

Lea: also backwards compat... 

Dan: I will propose a plenary thingy...

Lea: native apps for specific platform - you can take advantage to specific platform tech... 

### Session 15 B

Present: Amy, Hadley
Regrets:

Further work on EWP PR #93

### Session 16 A

Present: Hadley, Dan, Lea
Regrets:

#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848)

Lea: we've replied - there's nothing to reply... there's a new proposal... 

#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864)

Lea: Been looking at it - and pinged spec editor - who was not in agreement that a TAG review should be requested and had concerns about the Chrome implementation.  This has a generic name for a reason: it's supposed to be a way for UAs to use a mix of heuristics to maximise line breaking aesthetics. Develoeprs were evangelizing it as a way to avoid orphans because that's all this implementation did, and there was no way to control orphans specifically... If you ship something that is supposed to employ a mix of heuristics with only one heuristic, authors will learn to depend on that to control this one thing and you can never change it. There's a CSS WG resolution for a separate property for orphans, and also they are open to shipping pretty with more than one heuristic.

Lea: i've given this feedback - they've replied, they're receptive.. don't know what else there is to do here...

Dan: *issue of people asking for TAG review ... they should know that it's part of wide review ... also they should ensure that other editors and group chair have visibility / approval of that review request*

Dan: "are you in the group? did the group produce the document?  then you're proposing it."

Lea: *to write comment* I will direct that the CSS WG more appropriate for specific heurtistics...

Comments posted:
- https://github.com/w3ctag/design-reviews/issues/864#issuecomment-1663539298
- https://github.com/w3c/csswg-drafts/issues/3473#issuecomment-1663560448

#### [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791)

#### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852)


Hadley: we discussed [this](https://github.com/w3ctag/meetings/blob/847eafb9fe3e5453ad553a57a079f225b5f5a1d3/2023/telcons/07-03-minutes.md#borderless-mode---cynthia-ylafon-hadleybeeman
), since it had a strong dependency on isolated web apps, we were going to join them up with miniapps.

Sangwhan: miniapps is primarily about mobile. If they want to go to desktop, they'll have this problem. you want the user to have control over application sizing.

...Sounds like IE6

Hadley: also sounds like kiosk mode, but without the restrictions from getting into the operating system

Lea: what's the use case?

Hadley: It's for IWAs, which want to look like they're not in the web. Like native apps.

Lea: what happens if the app doesn't iclude a close button? Most users don't know the keyboard shortcuts.

Sanghwan: I'm against using the webkit prefix style.  There are efforts to remove this, but given the speed of how things work, i'm not convinced it's a good way of doing this.

Lea: I have concerns. A big use case is adding controls to the existing title bar, see their example of Excel. They've added controls but still need the regular controls... However, here the common case is not easy and there is a cliff: the moment you need to add anything to the title bar, you have to recreate the whole thing, including the regular windowing controls. I can easily see lazy implementations that look like OSX or Windows in every platform, rather than preserving the platform conventions. 

Sangwhan: is there an enforcement of draggable? No. Guarantees of draggability is probably required. What is the accessibility story for this?

Hadley and Lea: +1

Sangwhan: the semantics of close are very important. There is no discussion of that.

Hadley: we should ask them to talk to the Second Screen WG, re [Fullscreen popup windows](https://github.com/w3ctag/design-reviews/issues/840). 

```
We discussed this during our vF2F. While we see potential use cases which could benefit from this functionality, we'd like to discuss a couple things that are points of concern.

First of all, this depends on a feature that no other implementation has provided any signal on - which somewhat jeapordizes its future path on the web platform. We'd probably want to hear some level of feedback from other implementors on the dependency proposal (IWA) as it is a architecturally complex topic which we should carefully approach.

Even if this is gated behind a protected context of some form (IWAs?) - draggability should be a key consideration, especially the guarantees of having the user to be able to do so. The proposal as it stands does not seem to have mitigations from applications (be it malicious or not) breaking usability by making undraggable windows - and we believe that is not a positive pattern. Similar situation with the window controls. Reading the IWA explainer, we had a hard time understanding how that as a mechanism can prevent bad patterns coming from user-experience degrading applications.

We are also concerned that the feature introduces a [sharp cliff](https://www.w3.org/TR/design-principles/#high-level-low-level) in terms of usability: While many use cases are as simple as adding a control to the title bar, there is no way to do this without recreating the entire title bar, windowing controls and all. It would be better to introduce a layered solution, that makes [simple cases easy and complex cases possible](https://www.w3.org/TR/design-principles/#simplicity:~:text=As%20Alan%20Kay%20said%2C%20%22simple%20things%20should%20be%20simple%2C%20complex%20things%20should%20be%20possible.%22.

The drag feature being coupled to a webkit-prefix style is definitely not a recommended pattern, and unless this is a prototype/trial, having yet another feature depend on a webkit prefixed feature is a pattern we should avoid.

And we would recommend you have a conversation with the Second Screen working group, who are working on [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840). Their use case is slightly different, but it would be good if you could align your approaches and attributes. @bradtriebwasser, @michaelwasserman, @inexorabletash, and @anssiko are your main contacts for that.

Finally, we see there is no discussion about the accessibility risks associated with removing the window controls from the user interface. This can have detrimental effects on the usability in the context of AT needs.

```

### Session 16 B

Present: Amy, Dan
Regrets:

#### [EWP integrity changes](https://github.com/w3ctag/ethical-web-principles/pull/93)

**Discussed and... added link to Distributed Content finding -- and merged**

### Session 18 B

Present: Tess, Les, Dan
Regrets:

#### [[FYI] Clear Client Hints via Clear-Site-Data header](https://github.com/w3ctag/design-reviews/issues/871)

Tess: all things being equal it seens like clear site data header... user feedback of building on quicksand.. proposals that don't have consensus built on top of proposals that also don't have consensus..

```
Hi – the proposal itself seems fine, when taken in the context of client hints.

A meta comment regarding client hints:  In 2018, the TAG gave an initially positive review to the [client hints design](https://github.com/w3ctag/design-reviews/issues/320).  However subseuqntly client hints has failed to garner multi-stakeholder support, specifically from other browsers.  In more recent reviews, we have been flagging this and trying to advocate for multi-browser support (multiple implementations) as a key aspect of new features we want to add to the web.  The TAG remains concerned that we are building new features and technologies on top of other features that do not enjoy multiple implementations and are not supported across multiple platforms.
```

Dan: Satisfied with concerns?

Tess: OK.

Lea: OK.

**closed and commented**

#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805)

`mv *.zig # for great justice
chown us:us *.base`

Dan: Still pending...

**bumped 2 weeks**

#### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849)

Lea: lots of stakeholder feedback.. design looks good.. I'm generally positive... 

Dan: noting [mark's comment](https://github.com/w3ctag/design-reviews/issues/849#issuecomment-1569372457) and the subsequent response - that the issues that Mark is alluding to are actually not in scope for this review. 

Tess: no server-side requirement?

Lea: there are 2 methods -- range request - there's a detailed explainer... 

Dan: patch subset and range request...

Tess: the thing I'm worried about - safari positive signals - 

Lea: there's a design discussion about why both are needed... 

Tess: the other proposal further consolidates large server...

Lea: both of them are in the spec?

Tess: I will talk to myles about it today.

Lea: so there is group consensus and no formal objection... ?  If there's no objection then 

Tess: there's another play from Adobe in this space...

Lea: before we do anything let Tess followup with colleague...

*bumped to next week*


#### [Disabling UA transitions for same-document navigations](https://github.com/w3ctag/design-reviews/issues/835)

Tess: disabling worries me - pretty core to the UX of Safari (e.g.)... 

Dan: [response](https://github.com/w3ctag/design-reviews/issues/835#issuecomment-1638874530)

> Easiest example would be clicking the back button on a desktop browser. It makes sense for the custom transition on the site to win instead of overriding it with a UA transition.

Tess: it's an interesting assertion .. in the swiping case... wouldn't want to override.. so it's counterintuitive to me...  but let's close for now.

**clsoed with resolution too early**

#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798)

Dan: I'll ping google folks about this to see if we can get movement.

### Wrap-up for 16

Present: Dan, Lea, Hadley

### PR 85 https://github.com/w3ctag/ethical-web-principles/pull/85/files

**discussed but agreed not to merge yet**

Lea: *reviews Text wrap pretty situation*

Lea: left proposals - linked to comments in minutes.

Lea: *reviews borderless mode - builds on Isolated Web Apps* recreate the entire title bar - Sangwhan's concerns - its dependency on IWA - also a "cliff" - this could lead to windows looking like a specific platform - we recommended a more layered solution - simple cases should not have to recreate everything. Coupled to a webkit prefix property... A11Y risks.. 

Hadley: concerns about dragability... 

Lea: lots of concerns around developer experience, user experience, security & privacy..

Hadley: also suggested aligning with 2nd screen wg.

### Session 17 A

Present: Torgo, Hadley, Lea, Tess
Regrets:

#### [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841)

Tess: Feels like not considering mobile in this design is ... bad?  Every time we design a web API that's only for one platform we don't consider things that would apply on other platforms... Feels like it should be designed from the get-go...

Dan: majority of web usage is mobile ...

Tess: modern browsers... have lots of features that are not available to installed webapps because the browser provides all this functionality - ui - that is not intended to apply to installed webapps... intentional that the installed webapp doesn't have the browser chrome, complexity that comes with full browser tabs...  If you're supposed to refactor your browser to pull out the stuff that does tabbing and apply to whatever does installed webapps... 

Dan: I'm a fan of installed webapps but ...

Tess: *implementation issues*.  In the abstract, I like the idea... they don't seem to want it to make sense on mobile... and worried about implementation... 

Tess: assumption is that the tabs have certain functionality -- do the installed webapp tabs get all those functions?  Because those features may not be in the installed webapp container... 

Dan: on android you have multiple ... 

Tess: on IOS... same installed webapp engine for other browsers that install... so what are the tabs supposed to look like?  This is why it's a problem they're only thinking anout desktop... 

Tess: I'll write something up later

Dan: see  https://hachyderm.io/@TheRealNooshu/109947378812496228 as an example of some stats indicating majority of web usage being mobile - in this case 58.26% mobile, 39.82% desktop for gov.uk usage...

Lea: I think it benefits web apps to have this functionality... I see this as one of the things that could bring the best parts of apps into PWAs... bridging the gap with native...

It would be good to see more work on the use cases that exist. I think there are more here than it says, and I'm concerned about over-fitting and constraining if they're only focused on productivity apps.

Tess: is wikipedia a productivity app?I would like it to work so that when I open a new wikipedia page, i don't lose the other ones I have open and haven't read yet.

Lea: Use case? why not web tab?

Tess: access from teh home screen?

Lea: I see two use cases: adding shortcut from home screen, and "installing" a web app

Torgo: say I have a web app i want people to install, and I set up a manifest file, and I say it could have multiple tabs, so I ask for that... and now, suddenly, there is a lot mroe complexity to manage. Say i'm using mastodon web app, and someone drops a link in their toot, which I then tap on. Do I want that to come up in a tab in the mastodon web app? Or whats the right thing to do in that case?

Tess: on ios we have several different behaviours in that situation. A ommon thing native apps use is `ssSafariViewController`, which isn't shady. most of the time that's what i want. can open in safari if i want. That's different than this thing with tabs.

Hadley: is the new tab an iframe? does it inheret any permissions? can it track my activity? compromise my privacy or security? 

Tess: it wouldn't be an iframe... you'd open the new webapp and there would be a tab strip with one 

Dan: tIs there any thing in this about origin? would it use the same origin as the web app?

Hadley: you'd want it to be same origin becasue you already have decided what this origin can know, how to behave... but if you want to be the mastodon example, you'd be clickin on external links. Which one do we want here?

Dan: maybe it's an assumption to restrict it to one origin. but it's not stated.

Tess: you're going to want some tab management API for the app. It will want the list of tabs, and in the web extensions API, there is a tab ... to manipulate and manage tabs in the browser. Google maps, if you've opened a tab for a specific naviation and then completed that trip, and it uses the geolocation api to know that you've reached that destination, and you haven't opened that tab in 24 hours, and you haven't closed it... It could close the tab for you. But how would it know that stuff? 

Or you could give a service worker more api space than it currently gets... that feels weird.

for ios, installing a web app doesn't give that site any more permissions. maybe mroe resouorces, but no more power than just clicking on a link to a web page in a browser. Doing tab management would require more power.

Lea filed https://github.com/w3ctag/design-principles/issues/450

```
Hi there @loubrett,

We're discussing in today's TAG virtual f2f session – we're concerned about "desktop only".  Most available statistics indicate that the majority of web usage is on mobile devices - e.g. see [this run-down of recent access stats for gov.uk web sites](https://hachyderm.io/@TheRealNooshu/109947378812496228) - indicating 58.26% mobile, 39.82% desktop. Also since the web is [multi-browser, multi-OS and multi-device](https://www.w3.org/TR/ethical-web-principles/#multi), we'd like to encourage you to consider mobile and other platforms. We're also concerned about implementation issues across different OSs, @hober will follow up with more details.

We'd like to see more use cases & more discussion of user needs. Even in our short vF2F discussion several different use cases were brought up (Google Maps, microblogging client, Wikipedia etc). We would hate to see a web feature designed for just one thing when it could help meet a lot of different needs. See our relevant [Design Principles discussion](https://github.com/w3ctag/design-principles/issues/450). Also, have you considered the user experience when URLs to this web app are clicked across the OS? (e.g. in a Google Maps PWA, what happens when I click on the pin a friend sent me on Messenger?)

Are you thinking that tabs would only be allowed from the same origin that is the origin of the webapp itself? We're concerned about the user experience of a web app that includes links to other external sites which might then be opened as tabs in the tabbed webapp vs being opened in the user's default browser / browser experience. Equally, saying "you can only open links from the same origin" would be a very different feature, from a user's point of view. What was your intention on this? 
```

Lea: *leaves comment*


    
    
### Session 18 A

Present: Amy, Hadley
Regrets:

discussion of links between this set of specs.

#### [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850)

Hadley: are the cryptosuites normative dependencies?

Amy: the cryptosuite specs depend on the Data Integrity spec, but not the other way around

discussion of how RDF canonicalization fits in

Hadley: there's a json canonicalization process for plain json, and rdf canonicalization can be used if you have rdf

Amy: looks like they've considered complexity tradeoffs against the use cases they want to solve

looking at how cryptosuite specs fit with the data integrity spec.. data integrity specifies how to write a cryptosuite spec. Any cryptosuite can then be plugged in

> The following language was deemed to be contentious: The specification MUST provide a link to an interoperability test report to document which implementations are conformant with the cryptographic suite specification.
>
> The Working Group is seeking feedback on whether or not this is desired given the important role that cryptographic suite specifications play in ensuring data integrity. 

Interested to hear more about both sides of that argument..

discussion about how this could be used as a general mechanism, and why it might be focussed on VCs (because it's impossible to charter a group for a general data integrity mechanism?). In the spec:

>  While this specification primarily focuses on Verifiable Credentials, the design of this technology is generalized, such that it can be used for non-Verifiable Credential use cases. In these instances, implementers are expected to perform their own due diligence and expert review as to the applicability of the technology to their use case. 

```
We (@rhiaro and I) reviewed this in our virtual face-to-face this week.

First of all, we'd like to thank you for the clarity and conciseness of your explainer. Thanks!

The architecture which enables use of different cryptosuites depending on needs seems sensible. How does this affect interoperability? Is a verifiable claim from an implementation using one cryptosuite readable by an implementation using another?

We noted the contentious issue around requiring interoperability reports for cryptosuite specifications, and wondered what the different sides of the argument are for that.

We also see that you're not rolling your own crypto in this architecture and want to applaud that. Sensible choice. 

Also noting that the specification could be put to general use, rather than being suitable only for VCs. Have you considered how to expand this work for other use cases?  And have you thought about preceding work like XML signatures? If so, how does it feed into your thinking now?

```
    
#### [RDF Canonicalization](https://github.com/w3ctag/design-reviews/issues/855)

Hadley: use cases are making sense. 

Amy: the explainer reads as 'this is the work we will do' rather than 'this is the work we have done', as the explainer was originally written for the charter (noted by phila). Would be useful to have it updated to what was actually done. But assume they would have mentioned if they'd done anything radically different. They haven't filled out S&P questionnaire, but have S&P in the spec. We should ask them to fill the questionnaire.

Hadley: using quads as a triple with the graph name. Sounds complicated and repetitive. If you're hashing you should just be able to do that once

Amy: could ask the rationale for that. There's a 'todo' in privacy considerations in the spec.

Hadley: what if the hashing algorithm is no longer secure? SHA256 is okay for now.

Amy: be good to see mention of that in security considerations

```
We (@hadleybeeman and I) reviewed this in our virtual face-to-face this week. We like the direction of the work, and the design is sensible.

We noticed you haven't yet filled out the privacy and security questionnaire. Understanding that not all of the questions may be relevant, please could you do this?

Also, we see that you are using quads instead of triples and adding in the graph name once? It sounds more complex — but we suspect you have considered this at length. We are just interested in your thought process here. (This is the sort of thing we normally expect to see in an [explainer](https://github.com/w3ctag/tag.w3.org/blob/main/explainers/template.md).) 

Also, we'd love to see the explainer when you've updated your explainer to bring it in line with the spec. 

And finally, what happens if the hashing algorithm becomes insecure? It might be helpful to put a comment in the security considerations section to advise implementers in the future to consider that possiblity.
```

#### [VC-JWT](https://github.com/w3ctag/design-reviews/issues/857)

#### [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859)

#### [Verifiable Credentials Data Model v2.0](https://github.com/w3ctag/design-reviews/issues/860)

