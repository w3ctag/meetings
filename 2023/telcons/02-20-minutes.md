# TAG Teleconference
#### 20-22 February 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-02-20](https://www.timeanddate.com/worldclock/converter.html?iso=20230220T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
* [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @atanassov
* [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

### Breakout C (APAC / Europe) - [2023-02-21](https://www.timeanddate.com/worldclock/converter.html?iso=20230221T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) in context of FPS review - @torgo, @hadleybeeman, @rhiaro

...or...

* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon
* [Skip no-op service worker fetch handler](https://github.com/w3ctag/design-reviews/issues/815) - @cynthia, @ylafon
* [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman

### Plenary Session - [2023-02-23](https://www.timeanddate.com/worldclock/converter.html?iso=20230223T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Hadley, Amy, Lea

Regrets: Yves


### [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

Peter: sangwhan had concerns about handling of CJK fonts... blocking would not be good. CSS already has controls over web fonts loading.. so I was pushing "why this"....

... response doesn't make a lot of sense to me ... 

Lea: I don't understand why they say "We are indeed pursuing CSS-based approaches to for rendering control with web fonts" - I think these solutions are out there and working for a while now.

Peter: agree.  They do link to a CSS issue. Maybe looking to tweak it...

Dan: looks like this has been stuck since August...

Lea: we should look at the CSS working group thread... 

Peter: it was [discussed in CSS wg](https://github.com/w3c/csswg-drafts/issues/7271)... 

Peter: my understanding... won't block on "critical subresources" - my understanding is a style tag with an inline style sheet then that becomes blocking... 

Lea: I believe so.  Do they want to block for subresources as well?

Peter: only "critical" - only other import stylesheets.  Doesn't sound like it's a change in behaviour.

Lea: seems like this is already happening...?

Peter: mainly the ability to add the blocking to the link tag which is currently not blocking.

...

Lea: looking at the explainer... "The user agent will not render any pixels ..."   They are adding blocking=render to an async script...

Peter: Sangwhan amd I discussed the script use case and we were OK with it.

... remaining concerns were about style sheets... but if they are already blocking in all cases then ... ?

Lea: clearly it's not because people involved in this are not new to this whole thing. 

Lea: suggest: "As currently written your explainer doesn't answer the question... "

Peter: in explainer they're talking about a script tag that injects a link tag and they want that to be blocking.

... so it's mostly about when tags get injected later.

Dan: if it's about when tags get injected that sounds useful. If it's mimicking existing behaviour but covering that case, can we close and say it looks good?

Peter: slightly concerned that adding more mechanisms to block rendering will increase time to first paint.

Lea: it's in the developer's interest to have fast loading pages...  But there are now multiple subtly different mechanisms for blocking different things and that's difficult for developers.

Peter: use case of letting script inject style tags - will be used for feature detection e.g. - i would argue that should be handled by pure CSS. So this seems like doing CSS in JS in some cases...

Dan: can we raise these points - developer complexity and duplicating a functionality that CSS ought to be doing anyway - as part of our review?  Satisfied with concerns?

Peter: that works for me.

Lea: yeah.

Peter: after the meeting I'll **close** it.

### [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Peter: ... main thing I recall being contentious here was the control over top layer ... are we ok with everything else?

Lea: there were some pushback on adding this on random HTML elements... Maybe that ship has sailed.

Peter: my thoughts - maybe close this as satisfied with concerns and say we think CSS should control the top layer and we will ask CSS wg to discuss this?

Lea: agree.

*notes Rossen off this week*

Peter: should we punt to next week? 

Peter: would want some commitment that CSS wg will working on that.

**punted to next week**

### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

Amy: Mozilla  says no... It's more than storage - there are worklets involved... Even it was unparitioned storage...

Hadley:  we left this ... do we want to change that?

Lea: what kind of storage?

Amy: replacement for cookies? Most of the use cases are ad related.  The goal is a general purpose low level APi that can serve a number of use cases. We've been explcitly advising against that for replacement of 3rd party cookies..

Lea: how do web sites opt in? You have 2 cross origin web sites that want to use the same storage? what's the handshake / the opt in?

Amy: writing to the storage is open but reading is restricted by output gates.

Lea: I see what you mean about all the use cases being [targetted] ads.  I don't have a problem with ads and I don't have a problem with targetted advertising with the user's consent.

*discussion on what consent means*

*back to the API itself*

Lea: it's complicated.

Amy: it's complicated.

Lea: maybe it needs this complexity?  We definitely don't want a mechanism just to do 3rd party cookies in a more complicated way.

Peter: ..."privacy budget"...

Lea: we also should not be turning down things that come from privacy sandbox...

Amy: it mentions fenced frames a lot - and we've positively reviewed fenced frames.

Lea: nothing wrong with ads a general concept but not sure we should be adding features to the web platform just for that.

Amy: ..."single sign on as a use case" - but we have FedCM for that.

Peter: analagous to people want to open up general sockets instead of specific APIs... if anyone can write to the shared storage - that's still basically 3rd party cookies.

Dan: any relation to FPS?

Amy: not mentioned.

Amy: a reasonable comment might be "can you update us with how this proposal fits into the other proposals such as fedcm, fenced frames, storage access, topics API"? Also we could advise to not address general use cases...

Hadley: is that in the design principles?

Amy: it's [2.2. Consider tradeoffs between high level and low level APIs](https://www.w3.org/TR/design-principles/#high-level-low-level)

Hadley: i think we should link out to it...

Dan: support asking them for an update and linking them to our relevant design principles.

Amy: Will draft a commment*

Peter: "prevent cross-site tracking of users" ... "over time we hope to add additional gates"... worrying.

Amy: also says "this is a privacy improvement over third party cookies" but we are comparing to the web without third party cookies.

Dan: Agree.

Peter: Agree.

Peter: we should tread carefully.

Hadley: I also think this.


### [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

Lea: long thread... I had a breakout with Jake Archibald. Still had some concerns that I outlined in a comment.  Had a [response](https://github.com/w3ctag/design-reviews/issues/748#issuecomment-1379517669) but not fully digested.

Lea: at this point we're going into the weeds.  We've gone back and forth extensively.

Dan: have they been responsive to our feedback?

Lea: Yes.

Dan: Maybe it is a good point to close and ask them to keep us updated. We've already raised complexity concern. "We are particularly concerned about the complexity and ergonomics of this API." Can we give them a challenge to work to explain this API to developers, especially considering the complexity factor? 

Lea: I don't think the problem is documentaiton. I think the explainer makes a lot of sense. I think the explainer does a good job of explaining how the API works. The latest [feedback on jan 10](https://github.com/w3ctag/design-reviews/issues/748#issuecomment-1377872365) was about other issues. 

Lea: i'm thinking we should say "we have some concerns - we like overall that you've been working on this - thank you for being receptive to our feecback - please keep us updated."

Dan: agree. What's the issue outcome? "with concerns"?

Lea: the fact that you have to write js for things that don't otherwise require js is an antipattern. That you can't write transitions fo rthings triggered by 3p libarries you're not controlling. Fairly complex to hook into that. Wrap the entire transition into a callback. also understand the rationale, but it's a concern. Would like them to look at our feedback and try to address it - I think they are doing that, trying to think about it and filing issues.

Peter: agree "satisfied with concerns". Looks like there is work to do and it is being done



### [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

### [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @atanassov

### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

Hadley: [leaves comment about lack of explainer]

Amy: I think this is too early.. still going back and forth with group members on this in [an issue](https://github.com/fedidcg/FedCM/issues/429). There's no privacy & security questionnaire.

## Breakout C

Present: Dan, Hadley, Max, Amy, Sangwhan, Guest: Johann Hofmann

Regrets: Yves

### [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) in context of FPS review - @torgo, @hadleybeeman, @rhiaro

*abbreviated rSA and rSAfor*

Dan: recaps [previous discussion](https://github.com/w3ctag/meetings/blob/gh-pages/2023/01-moonbase-alpha/minutes.md#slot-06a)

Hadley: we had a good look at the spec and explainer and security & privacy questionnaire... We put the questions in our issue 808.

Johann: saw those.

Amy: that's it - we also reviewed the FPS proposal on the morning of the same day.

Hadley: use cases... what are you trying to accomplish here?

*belated intros*

Johann: context of use cases... how the proposal developed. we were thinking about how to evolve fps based on feedback from browser vendors and the TAG.  We had to change the synchronous same party cookie model.  Storage access APi was the natural choice there - already being put forward by other browsers.  FPS was meant for things like SSO... Use case for Nintendo - you log in for nintendo.de it forwards you to nintendo.com - they share info - and that's how the login works...It's a classic ccTLD use case. That sort of thing is SSO based... one of the things we want to solve. Using iframes is inconvenient ... also made more difficult based on changes to storage access API...  

[doc](https://docs.google.com/document/d/1AsrETl-7XvnZNbG81Zy9BcZfKbqACQYBSrjM3VsIpjY/edit#heading=h.vb3ujl8dnk4q)

... bunch of security attacks on the web - currently possible but would be prevented with 3rd party cookie deprecation. However if we have a really easy lever [for info sharing] then that opens up security vulnerabilities.  Essentially the idea is - iframe restriction for rSA. 

... There are non iframe flows that are enabled by passing images and setting cookies - not to be confused with a tracking pixel, it's on behalf of the user - but it's set through other than cookies. Eg. logging into wikipedia.org also set cookies for wikimedia org, all set in pixel images that would log you on everywhere. Whether that is the perfect programming pattern to use or not is another situation but it's something we see on the web and it's something we want to support.

Hadley: helpful background. Would be useful to have a concrete set of how you're going to measure your success? what's on the list of things it can do and it's done?

Johann: 1) adoption that we see from the ecosystem, if it's needed. 2) technical functionality - it's not that complicated for us, it's enable top level resource credentialed resource access, cross site resources with credentials, that aren't based on an iframe user flow. Seen these things in the wild. At Mozilla we built this into the browser .. saw that need

Amy: you said "this is not a tracking pixel" - so is that use case explicitly excluded or will there be a side effect of enabling tracking pixel case.

Johann: we have to look at this for all APIs.  with rSA you still need a user action... So I'm pretty sure we made it explicit - not intended to be auto-granted on all sites. Silent auto-grant all the time should be discouraged. We see FPS as user-supplementing  - for the cases where the user would clealry make the assocation between two sites.. 

Amy: worth digging into the threat model where users think they are consenting to one thing but there is still a tracking pixel going on - which is not what they consented to.

Johann: FedCM is the long term..

Amy: That was my next question - is this a temporary solution [in advance of fedCM]?

Johann: FedCM is one social sign-on use case... Mozilla really [likes] FedCM... and are concerned about FPS.  FedCM - the way it's currently built - isn't meant to solve SSO cases... There are proposals to make it more ergonomic for SSO.. the reality is that browsers now do it with a mix of heuristics and ???. Some sites are broken, some sites work in chrome, some are covered by heuristics... I personally agree on the long term outlook that FedCM is the way forward...  So I think extending FedCM is in our interest. But for the nintendo use cases - showing a prompt for those is not something we would not feel super comfortable with... Prompt spam is a problem on the web. We want to protect users from large scale tracking and put up theoretical barriers that are only in place to support theoretical concerns. We want to be practical.

Dan: good articulation.

Sangwhan: .cc tld case would be unscalable for a lot of companies - list so long that users would not read it and press okay anyawy. That dialog is not going to help anybody

Johann: we still have to find convergence there. Our way of thinking is not necessarily the correct one. Will turn out over time. Back to rsafor ..

... we want to stay on a path that has a chance of converging... sameParty cookie would have factured the ecosystem for a long time, this is better. We're talking about details that are convergable betwen brwosers

Dan: Can we talk about the specific functionality of requestStorageAccessForOrigin which is different from requeststorageaccess and why that's necessary to support these use cases. In the discussion between Amy and Hadley you uncovered that these were functionality that other browser vendors had specifically discounted from request storage access. That seemed to be concerning. Diddn't seem like that was related to antipathy for FPS but more at a general level.

Johann: the functionality in rsafor was explicitly thrown out of rsa - we led the effort, everyone agreed to it. We discsused at TPAC, all browser vendors agreed to reduce the scope of rsa mostly because of security concerns. rsa as an api really doesn't work that well with per page storage access. It's really complicated. 

...Previously rsa worked in the way that you had to as a third party embed it inside in an iframe in a top level document. You had to get user gesture and call the code to request storage access yourself. However that storage access was then expanded onto all resources you had loaded on a page. If you were in an iframe and then the top level page tried to load an image fo ryou that would also work. Google docs in an iframe on example.com, and googledocs called the storage access api in the iframe, if example.com then loaded an image from google photos accounts.google.com that would also load with credentials. Two big problems - developer understanding and sameness.. it's hard to work with for developers when they don't know when something is going to happen because it happens in a separate iframe - always a concern. Then what tipped us over to restricting to the iframe was security concerns. We realised that when .. that can be a problem, you have an iframe that loads google docs, but as a top level you can make requests to google accounts - that is potentially bad. Google docs wanted to have this one iframe and load credential and do something with it. The user wanted to load the document in a personalised state, but it just opens google as a whole up to an attack from the top level example.com. That was the initial concern. That applies to google and also everyone else. Unless you  narrowly scope down in terms of security, the top level can arbitrarily attack all your endpoints. See more in the doc. 

...Originally Martin Thompson suggested scoping back to iframe. We had a bunch of creative solutions to work around that, but none really worked, to preserve that per page state. So back to iframe grants. Only get storage access for that iframe, it doesn't escape. It has great security properties, you can't be attacked by framing, you have to opt in to this potentially dangerous behaviour, and it only works on documents that really need it. if google docs calls it, the attacker can't forward to google accounts, because it wouldn't cal the api. So we threw out the per page behaviour. 

...Both mozilla and google at the time said we are not comforetable with losing that top level ability to load credentialled images and scripts. We had at the time proposed rsafor we felt it was needed, and it was a prefect fit for that. So sitll security concerns for rsafor - we fixed it by adding a CORS requirement on any resources loaded on rsafor. if example.com now calls rsafor on google accounts, it can make credentialled requests, but the requests always send an origin header, and google accounts always has to respond with the correct cors response, or the resource wouldn't be loaded. That is protecting against access leaks. There a few edge cases, which we considered out of scope and not solveable. We're losing some cross site developer functionality 

Hadley: what's the cross browser participation, different between rsa and rsafor

Johann: ...we hope that rsafor takes the same path as rsa had. rsa is older, has a lot more history. We think we have a really nice solution with rsa. rsafor is a very early proposal, still gathering feedback from other browser vendors. it was developed together with mozilla at tpac, and google went on to formalise it. I feel like we've hit a few points o fdisagreement with mozilla that we have to work through that weren't clear at the time we developed it together. I'm hopeful that we can.. it might take a while.. it look a long time for rsa, but I'm hopeful we can converge on something together. There are concerns, but it doesn't rise to the point of FPS 

Dan: question in the breakout about images - credential images - to focus on that - tracking pixels.. 

Johann: images are .. pixels is the right word. Has a bad connotation, tracking pixels embedded everywhere. Definitely possible on browsers that don't block 3p cookies by default. They're a technology you can use but it doesn't stop there. If you took away the ability for people to do credentialled images they would do fetch requests, or they'd embed iframes. Pixels and images are so frequently called out and used because they're so convenient. People like embedding 0x0 images which set cookies. We need to ensure that these cookies can't be used for the purpose of cross site tracking. But it doesn't make sense to say a lot of people use tracking pixels, let's not allow people to laod images across sites with credentials. That doesn't really fix anything because people would move onto the next technology. That whole space means it could be fetch requests, script loads. A bunch of things that carry credentials across sites that are used by 3p resources on the top level site. loading iframes is complicated. fetch credentails, post message up. We're not talking about cookie theft - if you send around your credentials via js apis you run a much greater risk of having them intercepted. Eg. Sony and Playstation - sony wants to authenticate on playstation, you visit playstation.com, open a popup window with sony, login with sony, sony embeds an image, a credentailled pixel, carries a cookie that has your login information. Sets that, could either be an image that has the origin playstation com, or has the origin sony.com. Say it has a pixel of sony.com itself embedded, you go back to playstation.com and then that cross site flow happens, where playstation.com has to receive the same information somehow. Actually sony.com embeds the pixel for playlsation com, then you reload the document and it loads without js being involved, portecting against cookie theft. Iframe is much less conveneint. Could we not possibly put this restriction in place on the web? Not impossible. If you were to rewrite all cases from scratch you could do it. But given there are so many sites that use images and scripts with credentials, it doesn't seem feasible for us to ask the entire web to rewrite, at least not in the short to mid term.

Hadley: thus far it sounds like you've talked about SSO and tracking. Are there other examples or situations in which you're finding somebody would to be able to use it in this way?

Johann: a lot of 3p cookie deprecation, cross-site use cases that are non-tracking, are in some way about authentication. They reduce to authentication and login to some extent. That's why people say FedCM is the long term future. I think for FPS it's really about finding that set of authentication use cases or recognition of the user identity use cases that are both non-privacy invasive and also not something that the user should be confronted with a prompt about. Another example for FPS is the service domains where we have something like githubusercontent or an experiment domain separated for security concerns in jsfill but the content needs to load in a credentialled fashion if it loads on the top level. For me it wouldn't make sense to ask the user if you want to connect jsfill with jsfill. That is speaking to FPS. Important to say for rsafor a lot of what it does and its long term future is to provide that technological underpinning, the capability to load these images, do these requests in a safe manner, gated on other things. Could be a good prompt design, could be FPS, or whatever we end up converging on on the 'front end' as brwosers. Both requeststorageaccess and rsafor provide the technological underpinnings to allow us to restore safe cross site cookie access. Long term, eventually browsers have converged on this way ...

Hadley: in S&P it says "...risk of abuse.. to not undermine the gains of cross site cookie deprecation". Sounds like a fantastic ambition, what does it mean in practice? Will it depend per browser? And in Chrome FPS will be the limitation for who will be allowed to use this technology with each other?

Johann: I think that was a good summary of the current status. A lot of this is due to necessity becuase of different opinions on what the end user flow should be. Browser choice. A bunch of baseline anti abuse mechanisms in the api right now. User interaction requirements, security retaliation(?), security restrictions etc.. we have a bunch of baseline protections. I agree the big privacy gate is something that we still have to converge on. The point of the sepc is that it requires this sort of gate. At the very least by saying the user agent has to ask the user for permission, which includes for FPS or heuristics, taking steps to not ask if you are confident that' it's fine, but generally the UA is required to ask for permission at the last step. They need to make there is some sort of privacy check, privacy gate. That's how we consider the design to be protecting the user.

Hadley: as a developer wouldn't that make for really different user experience on each browser?

Johann: yes, agree that's a problem. SOmething we have to work towards. But we can't ignore the reality. I'd love to be in charge of all browsers and find this common way of gating user consent for all sites. But we have a couple of really great approaches, like FedCM.. can see not everyone is on board with FPS. Some browsers have prompts. I'm more worried about the developer experience than about the remergence of widespread cross site tracking. All the methods we have put in browsers right now are very private and in the intersts of the user, but I agree the developer experience suffers, that's a task for us.

Hadley: helpful. And the user experience is potentially very different and confusing.

Johann: true, fair concern. Both rsa and rsafor are designed in a way that tolerates.. two edged sword.. on one hand by being so open to the browser can dow hatever it wants to ensure user consents, it creats a diverging ux.. but also ensure we're future compatible with whatever hopefully better solution we can converge on at some point. That's the problem with sameParty cookie - was closely married to FPS. Couldn't rip FPS out. But you can rip prompt or FPS out of storageaccess and put something better in front of it. We'll see, maybe FedCM. You still have the technological capabilities.

Dan: what you said about CORS being the thing that helps you mitigate the issue that was raised with the forOrigin part.. is that something that .. how do you think mozilla and other browser engines feel about that. Is it a consensus view that having CORS sufficiently mitigates the risk?

Johann: I wouldn't expect that to be contentious. May be discussions over details. One aspect of CORS where it doesn't prevent CSRF (cross-site resource forgery), you can still make the requests, but hoepfully it prevents leaks becuase the server has to respond. But CSRF we consider somewhat out of scope because it's possible in other ways. You can open a top level URL, new tab with that url you want to attack. Other way stop do it so out of scope, and also would be hard to completely solve. We won't have a lot of issues on the CORS question. Seems fine to me.

Dan: what's the pathway for standardisation for rsafor?

Johann: we've made good progress at tpac last year, leading up to the point where we are now. There are a few points of contention that we have right now, mostly around this frontend question. How do we really expose this to users? We are generally aligned with technology.. that this would at the very least not be harmful. Varying degrees of people saying it would also be useful among browser vendors. Big question is how do we expose this ot users - chrome has a clear answer, FPS. Also looking into prompts and developing a prompt strategy. Other browser vendors don't. They need time to look into it and figure out how comfortable they feel. And needs further discussion to ensure their concerns are heard, what does this look like if chrome uses FPS and we prompt, what does that look like for us.

Hadley: ..about double keying?

Johann: not an oversight, we just didn't make it clear enough. They way it's keye on rsafor is it's in the permission descriptor. Added a nonnormative note to the spec in response to your comment.

Hadley: thanks for clarifying in the spec.

---

dan: the prompt spam point is a good one

Hadley: fragmentaiton is concerning... want to spend more time - conversation was really helpful.

Amy: a piece of positive feedback: separating each of these compontents out and making them pluggable is good - gives a space to improve different bits separately...



### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

### [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon

### [Skip no-op service worker fetch handler](https://github.com/w3ctag/design-reviews/issues/815) - @cynthia, @ylafon

### [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman


## Plenary Session

Present: Dan, Peter, Amy, Max

Regrets: Rossen, Yves

### Breakout Rollup

#### Breakout A

Response to Shared Storage:

```
Hi there, sorry for the delay in getting back to you on this.

We are concerned about exposing such a complex low level API to authors (see [Design Principles: high vs low level API tradeoffs](https://www.w3.org/TR/design-principles/#high-level-low-level)). This proposal is about much more powerful functionality than only sharing access to storage. In particular, with regards to accommodating use cases that are no longer met once third-party cookies are deprecated, we strongly encourage addressing these in a focused, case-by-case way, rather than in the general sense. For example, you mention single sign-on as a use case, but we understand that FedCM is being worked on specifcally to address this case.

Could you provide us with a summary of how Shared Storage fits in with the other Privacy Sandbox proposals (such as Fenced Frames, Topics, First Party Sets)? Are there any duplicated functionality / use cases among them? Where are the overlaps?

We appreciate that you see this proposal as providing a privacy improvement compared to the status quo of third-party cookies on the web, however would you be able to give us an analysis of the privacy implications in comparison with the web _without_ third-party cookies as the baseline?
```

#### Breakout C

#### [ Open
Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences
](https://github.com/w3ctag/design-reviews/issues/767)

Left [comment](https://github.com/w3c/window-placement/issues/110#issuecomment-1441319407)

#### Privacy Principles

Yesterday in the Privacy TF call we agreed to sent out the privacy principles for a round of wide review. (There is one PR left to merge but Jeffrey Yaskin is going to merge that based on the output of our call today and I will then ask  Yves to shuttle the document over to /TR space - hopefully by Friday). My plan is to send that update the AC and Chairs list about the TAG’s last virtual f2f and include in that email a note about the privacy principles requesting wide review. https://w3ctag.github.io/privacy-principles/

### Issue Triage
