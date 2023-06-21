# TAG Teleconference
#### 12-15 June 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-06-12](https://www.timeanddate.com/worldclock/converter.html?iso=20230612T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss
* [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman
* [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2023-06-13](https://www.timeanddate.com/worldclock/converter.html?iso=20230613T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [[FYI] Report Critical-CH caused restart in NavigationTiming](https://github.com/w3ctag/design-reviews/issues/833) - @cynthia, @torgo
* [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

### Plenary Session - [2023-06-14](https://www.timeanddate.com/worldclock/converter.html?iso=20230614T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Privacy Sandbox Special Session


-----


## Breakout A

Present: Dan, Peter, Hadley, Amy, Lea, Yves, Rossen, Tess

Regrets: Max


### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

Dan: we've had external feedback, responding to mine and Yves' message in April. Privacy/security concerns. They were claiming it doesn't make the situation worse, but we want to leave the web better. They replied it makes the web better. They've modified the spec about spoofing prevention from Yves' feedback. Mozilla standards position is not resolved yet. Don't think it's clear how they think this can be... theiri point is any ui element can be misused by advertisers.

Amy: no further comments

Yves: we discussed in Tokyo. Agreed it wasn't worse, but good to say there are issues in the spec. Looks like that is what they did.

Dan: [change to spec](https://wicg.github.io/document-picture-in-picture/#spoofing) addresses phishing topic. What about the API?

Rossen: given the fact we can't dictate/require UI I agree the normative language is good. But worry there are UAs where the UI is minimal or customiseable, and it becomes a vector for exploits. Especially things designed to harvest user data without their consent. Not that there's something different for us to do, but still concerned.

Dan: what if they added normative language around those requirements for those kinds of UAs?

Rossen: e.g. a webview - a PWA (full screen) could be abused. Not sure that this language is sufficient. Having said that I don't have something more strong to offer without getting into territory of specifying UI expectations - which we don't do.

Peter: "if the user clicks the window's close button" but doesn't mandate that the window has a close button. Would be nice if there was a standard consistent way to dismiss something. 

Lea: this is basically very similar to window.open except the window's always on top....

Peter: ...with a lot more constraints.  E.g. you can't position it.  

Lea: they address this a question under [detailed design discussion](https://github.com/WICG/document-picture-in-picture#detailed-design-discussion)...  but wasn't there discussion of creating a better window.open - couldn't this plug into that?

Lea: they've discussed many use cases - maybe it shouldn't be named this way - since it's not just about pictures...  Does this name space have anything else?  or is it only this one method?  Would another namespace be more suitable?  If the only reason this isn't part of window.open ... I'd love this to become part of the efforts to improve window.open...   Would be better - would fix both problems in one swoop. Wish the use cases for integrating into window.open were explored more.

-Rossen

Lea: why don't we fix window.open so the options it supports are feature detectible?

Peter: it does strike me we have other things that are difficult to feature detect... 

Peter: why is this an API and not an element... they talked about "requiring the overhead of a separate doc" - not sure that's necesarily true...  wondering if that's not a better approach. tie it into frame behaviour?

Dan: good feedback, a bit late. Multistakeholder is an issue.

+Tess

Peter: it's not too late if there is no multistakeholder support

Dan: Picture in picture has multistakeholder support as part of WebRTC

<blockquote>
Hi - first of all we know we're late getting back to you on this. Thank you for bearing with us. We appreciate the addition of normative language around spoofing. We remain concerned about the lack of multi-stakeholder support - particularly the lack of support from other browsers - unlike picture in picture itself which enjoys strong support across engines. We're also concerned that this feature could be used to enable surprising and disruptive advertising experiences. We also remain concerned about the browser chrome around this picture-in-picture window. E.g. the documentation presumes there will be a close button but this is highly dependent on platform.

In terms of API design, we did see a lot of commonalities between this functionality and an "always on top" option in `window.open()`. Integrating it in `window.open()` would also fix a lot of issues around it (guaranteed prominent window chrome, guaranteed close button, existing ways to interact with said windows, naming, namespacing etc) and it also reduces the new API surface that authors need to learn. We do [see](https://github.com/WICG/document-picture-in-picture#since-this-is-pretty-close-to-windowopen-why-not-just-add-an-alwaysontop-flag-to-windowopen) that this was considered as an alternative, but rejected due to lack of feature detectibility for `window.open()` options and some functional differences (never outliving the opener). There are [discussions](https://github.com/whatwg/html/issues/7485) around creating a new method that fixes the various issues of `window.open()`, it may be a good idea to collaborate with the folks working on this effort. The functional differences between this and `window.open()` may be useful more broadly too, never outliving the opener certainly would be!


</blockquote>


### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

Hadley: looked at in the tokyo face to face. I'm not sure their reply addresses Peter's question. My main concern.. prevent silent access.. the site calling the browser after the user clicks sign out... sounds like credentials are still in the browser.. could there be ways to override that? On the other hand the browser as the UA is the place we've decided to trust for all this stuff anyway. So I think it's okay.

Peter: in saml in a lot of implementations you can sign out of the RP without signing out of the IDP. You're just closing the session. So if you revisit the same app it autorelogs you in.

Hadley: so you have multiple steps to sign out, that don't necessarily feel intuitive? That's not good for the user

Peter: in saml there's the possibility that when you sign out of an app you can feed it upstream and sign it out of the idp as well. And that can kill sessions of other RPs, but that's very rarely implemented. I don't know if this flow is an issue in FedCM. In my experiecne most users don't undrestand the difference between signing into an RP vs an IDP. If you're on a computer that isn't yours, most cases people will think they have signed out but haven't. Concerned about people walking away from active sessions that they don't realise they're walking away form.

Hadley: I think that's worth making explicit

Peter: this might be addressed elsewhere in FedCM, don't want to add noise. Need more time - plenary.

### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman

Hadley: long discussion... api changed

### [WebRTC Codec selection API](https://github.com/w3ctag/design-reviews/issues/836) - @torgo, @maxpassion, @plinss

### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

### [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia


## Breakout C

Present: Dan, Sangwhan, Amy, Yves, Hadley

Regrets: Max


### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Dan: they have indicated a change - i've asked them to update this review and let's keep going in this one rather than opening a new review.

### [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon

Yves: we should close it as "satisfied" - it got multi-stakeholder support and they documented user needs. 

Sangwhan: yes I'm OK with this.

Dan: Yves can you leave a closing comment?

Yves: sure.

**closed**

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

Dan: They [responded](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1517032595) to feedback that we left.  Comments adddressed. Question raised by Tess about suitability for standardisation. They make a compelling argument that it is appropriate.

Sangwhan: user expectations.. could argue that the behaviour of autofill should be consistent between implementation. Or it could be entirely implementation dependent. Currently lots of heuristics and magic logic. Even in standard forms.  In payments there is a thing called *PCI* -- payment processor has to be the recipient of the card information. You can't take care info into an input field on your site and post it over.  If e-commerce site wants to customise the style... you can't really style an iframe. So, each of these input boxes are small little iframes: credit card number, name, etc. And the iframes are sitting on the payment provider, and the style is on the e-commerce site.

Dan: how does this overlap with eligibilty for autofil?

Sangwhan: You want to double-key autofill, for this payment provider WITH this e-commerce site. E-commerce site delegates to payment provider to let this through.

Dan: sounds reasonable. Shouldn't they be using web payment, etc.

Sangwhan: I'm sure they've had numerous discussions with the payment providers about what is possible. 

Look at the example code... It's [difficult.]

Hadley: as a user how do I know that the cc number goes to payment provider as opposed to e-commerc provider. 

Sangwhan: as a user you're sabving it on e-commerce site but it's double keyed.

Hadley: but e-commerce site doesn't see the data.

Sangwhan: as a user you don't see that?

Dan: it's covered by the e-commeerce site saying this is PCI compliant. 

Hadley: still the user doens't know who they're giving this information to...

Sangwhan: they want it to auto-fill all fields at once...

Hadley: I am concerned we're breaking some rules of the web to satisfy this one use case.

Sangwhan: it already happens... but just for one iframe not for individual iframes.

Hadley: what if an ecommerce site uses a payment provider that I don't want to use... I've lost my ability to make an informed decisiom...

Sangwhan: if ecommerc site is in a country that requires it to be compliant then...

Hadley: what if the field is for something else...

Sangwhan: you wouldn't use it for something else...

Hadley: I think what you're saying makes sense... 

Dan: could the browser prompt the user with both the ecommerc site identity and the payment provider site identity?

Hadley: I think that would help with my concerns, of users not knowing who they are giving their info to...

Sangwhan: defining UI in spec...

Hadley: could be non-normative rather than designing specific UI...

*discussion of if it's a UA UI thing*

Sangwhan: underlying complexity - but at the end of the day user's just want autofill to work.

Dan: users want to pay for stuff in an easy seamless way.

Dan: if other UAs think this is a UI issue and not to be specified then it's up to the proposers to convince them.

Dan: I still think it's worth saying "let's take some of this energy and push people to web payment"

Sangwhan: we said that already.

<blockquote>
We remain concerned with the level of information available to the user about what they have agreed to share with whom via auto-fill. Is it possible to advise UA providers to surface this information to the user in some way "are you OK with sharing your cc number with *ecommerce site* who uses *payment provider* as a payment provider?"
  
We also remain concerned about the multi-stakeholder buy in. If this is going to be adopted by the industry then we'd like to make sure it's widely adopted across browsers.
</blockquote>

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/831#issuecomment-1592430767)

### [[FYI] Report Critical-CH caused restart in NavigationTiming](https://github.com/w3ctag/design-reviews/issues/833) - @cynthia, @torgo

Sangwhan: lgtm

**closed**

### [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro

*we begin looking at the explainer*

**bumped to next week**

### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

## Plenary Session

Present: Peter, Tess, Dan, Amy, Hadley

Regrets: Max, Yves, Sangwhan


### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

Peter: [on autofill issue] this sounds like a hybrid solution - piecemeal - seems like the worst of both worlds. Why are we adding a feature to the web to support that way of doing it when there are 3 other viable good options.  It's not either this or web payment.

Dan: I think we're all in agreement that this is not a nice thing – so if there are alternative options we can articulate, let's do that.

*Peter to post something*

### Issue Triage


## Privacy Sandbox Special Session [Friday the 16th at 15:00 UK time]

Present: Hadley, Dan, Sanghwan, Amy, Yves and guest Michael Kleber from Google

### Agenda

Torgo: [introduces TAG work mode and findings and 3p cookies finding](https://www.w3.org/2001/tag/doc/web-without-3p-cookies/)

Hadley: we looked at specs that focussed on a particular use case, and were trying to recreate functionality for a single use case, without considering the effect of all of these things coming together. This was to help take a step back from the one problem we were trying to solve, and to look at the whole web, and look at the impacts as a whole

#### W3CTAG [Web Without 3rd Party Cookies](https://w3ctag.github.io/web-without-3p-cookies/) draft 

Dan: we've talked a lot about - we hear "we need these thing because 3p cookies are going away". My reaction is wait a second - do you really need that thing? Is that thing more important than... (restating Hadley..?)

Sangwhan: there's a nuance here. There seems to be a need to provide some sort of replacement due to legal complications. Seeing the perspective from both sides, is that there needs to be an alternative  in order to deprecate 3p cookies

Michael: the privacy sandbox goals are aligned with what you said. To make the web much more private, getting rid of third party cookies is shorthand for doing that. Practically, there are other ways to track people.

Dan: we also have a finding on unsanctioned tracking, fingerprinting

Michael: "unsanctioned" is a good word, but there are some surprises about what falls into that category. Some people think if someone gives you an email address they have sanctioned using their email address for tracking, so hash of email easily becomes a replacement for third party cookies. This is why all the people who care about anti tracking bring up single use per domain email addresses, so you can be contacted but not joined up. Happy to talk more about ulterior motives and real world ecosystem pressures. Goal is let's get rid of the tracking techniques, and what is the range of use cases that is going to break as a result, and figure out which are essential. Harm to the web is substantial if there's no replacement. And figure out / provide a way to acocomplish the goal without enabling pervasive tracking. Unfortunately often, especially for advertising use cases, the amount of work and change requred from people who depend on 3p cookies to migrate to a new way of doing things is really large. Things developers have built are complex. Anything is hard to change once there are billions of $ riding on it. 3p cookies are used in so many different ways. We're trying to create a minimal set of apis to make getting rid of 3p cookies feasible, and won't result in an alternative that is worse. Worse could be along a lot of different axes. Privacy axis right now is bad. A lot of damange that could be done depending on how you go about fixing the privacy one.

Dan: generally the TAG is looking at things from the end user perspective. Are 3p cookies really necessary to do the thing? We're thinking about end user cases, not the advertiser cases.

Michael: Privacy Sandbox is on the same page. The first question we try to answer is what would happen if we just got rid of tracking. What would the impact be? A rise in rampant fingerprinting, email collection, hashed pii, paywalls. If hypothetically you've prevented all of those bad things from happening, what happens? Extremely painful result that we got is that most sites on the web lose somewhere between 50 and 70% of their revenue. Garrett Johnson did a meta analysis, that shows all the different papers on the subject. 6 papers try different techniques. One outlier, but well substantiated. A lot of websites would lose a lot of money, not a recipe for the web continuing to thrive. Damage ability of the web supporting people to be able to access it. Testament to how strong the motivation is to do all of those other unsanctioned things. If you can track with fingerprinting and tell websites that their income will go up by 2 to 3x if they use it, that's a strong motivation. Hoping people won't do these nefarious tracking things seems unlikely to come to fruitiion. Cost-benefit analysis for everybody on the web. Privacy sandbox is focussed on both sides of the tradeoff. How much can we shrink the revenue benefit of fingerprinting? Can we make 90% of the money without doing any of the tracking. If so, not nearly as much incentive. And if there's regulatory pressure against tracking, that makes the cost of tracking even higher. Goal is a well lit path of no tracking as the most attractive option.

Dan: what about the anti fingerprinting technologies increasingly built into the browser and seem to be on the rise?

Michael: indeed, half of privacy sandbox is anti fingerprinting work

Dan: ...lots of fingerprinting surface area...

Michael: CMA / competition - they raised the concern that the rev loss is not nearly as large of a problem with ads on google.com   

Amy: does "most sites on the web will lose.." mean "sites which earn revenue via advertising"?

Michael: yes, and most sites on the web earn revenue via advertising

Hadley: google adsense?

Michael: google plays a big role in putting adverts on many sites on the web, and earns a share of the revenue from this, but much smaller than from ads on google.com.


#### W3CTAG [Privacy Principles](https://w3ctag.github.io/privacy-principles/) 

Dan: [introduces doc]. Encourage looking at principles dispassionately. We want people to consider these things when developing a technology which has privacy implications. We use ethical web principles to think about what differentiates it. Not about the user expectation necesssarily, but our expectations of what it should be for the user. Some people say "but users don't care" - I care that what we are producing as an organisation, needs to be held to higher standards than apps or other platforms. I think that largely is the goal of a lot of people who are working on the web. Feedback would be appreciated on these principles. That they make sense from the perspective of people on the privacy sandbox team working on something. That it's additive, that the work complies to these principles.

Michael: I have engaged through Jeffrey. Brought up perhaps a dozen different things. Has moved in a very good direction. The right sort of guidance. We're aligned.

Dan: trying to help level up the web one api at a time. Feeds back into our design review process. The point is not to make grandiose statements, it's to have something we can point to next time someone asks for a design review - can they please adjust it in this way. This is where design principles came from.

Michael: for every api we're producing, we are happy to talk about why each one is in line with these principles. They're designed with this goal in mind. At the beginning of Privacy Sandbox I wrote our proposed new privacy model for the web. That also is aligned with these goals. Those are the principles we're working from. There's a lot of stuff about competition stuff we can talk about, that ends up getting into some of the stuff that shows up in the privacy principles. It's clear there are some people who believe our actions are self-interested, in a way we disagree with. Because of complaints from parties who are claiming this, we have spent an enormous amount of effort engaging with regulators who are worried about the same thing. Making it clear that if we were acting in a self-interested way they would shut us down, and we need to justify why a lot of decisions we make are not motivated by preferring google over competitors. Any document focussed on motivations has this risk of one party trying to make guesses about what a different parties motivations are that makes it hard to turn into action because you have to make assumptions about somebody else's motivations. Area where there's room for pitfalls we would like to avoid.

Sangwhan: it's easier for google to not deprecate 3p cookies, if I understand correctly? less friction, less engineering cost?

Michael: less engineering cost and easier for otherh parts of google. Chrome is a browser though and all of the browser engineers know that all the browsers need to steer to the same destination eventually. It will take a while to get there but we all have the painful memories of "this site best viewed on..". Nobody wants to be back in that world. Chrome is the only major browser that has unrestricted 3p cookies, certainly cannot be stable in the long term.

Dan: that's one of the things that keeps coming up in the context of our reviews. You've got this new thing.. eg. topics is meant to replace some of the functionality of 3p cookies. What if you have a browser that doesn't support it because they fundamentally disagree. What stops that bad experience of being denied use of a website?

Michael: without trying to tell other browsers what they should do: our designs all have considerations for the question how is this going to work in incognito modoe, or if the user has turned off the api? We don't want the website to be able to say you can't use it in incognito mode. We try to prevent this. Everyone API gracefully degrades. topics in incog mode or turned off works the same as if the topics api does for a regular user who has only recently started browsing, etc. there's no way to tell. Website just has to accept there are no topics for a particular user. If sites really want to call topics, other brwoser can implement it to say there are no topics all the time. That's a functional shim to prevent sites from saying you have to use chrome instead.

Sangwhan: user does seem to have control over topics so they can go in and delete stuff.

#### Updates from Privacy Sandbox

Michael: we haven't had much opportunity to talk about goals and motivations. perhaps should have talked about this years earlier.

Sangwhan: the ultimate goal of deprecation is something everyone wants. The how is where we're disagreeing. How chrome is approaching it as a way to sneakily reenable 3p cookies - not the intent.

Dan: i think it's possible for an engineering effort to mitigate against a particular thing to reintorduce some of the problems without there being nefarious intent.

Michael: judge outcomes not goals

Dan: we had a lot of discussions about requeststorageaccessfor. What is the use case? For some things where the motivation is to replace something that went away because 3p cookies went a way. Do we really need a replacement? Is there another way? Or maybe the web shouldn't work like that in the first place. 

Michael: concerns expressed in world without 3p cookies, about shipping things that get you back to the same state, is similar to some of the feedback we gave safari in response to their introduction about request storage access. Makes things bad again, joins a local and global identifier, and while you can pretend it's only on this page, pretend it's a temporary join, but actually it gets you back to that state.

Dan: I don't think they would agree with that...

Michael: I know, they're not trying to sneakily reenable things. But request storageacccess exists in every non chrome browser already. we can't not implement it. For other browsers there's this hacks file that says "on this site automatically call request storage access for this party on behalf of this party" without the sites having to do anything. Requeststorageaccessfor is to add something to the platform that other brwosers had to do in a nondocumente dcustom hacks file in order to keep thing working without 3p cookies. We'r etrying to do that in a more above board way that does not involve a proprietary hacks file.

Dan: there were multiple different opinions being expressed on that. I'm not as deep into that. But there are people I know are operating in good faith that do not agree. Maybe the TAG can help to facilitate that discussion. Should be happening in the privacy cg. 

Michael: happy to have discussions that try to avoid degenerating into finger pointing

Dan: if there's a fundamental disagremeent about something, like this, sometimes it helps when the TAG runs a session to bring peopel together with different opinions and try to hash it out

Michael: I'd love to see that work. Similar to some discussion about public suffix list. How to move that into something people like? Our attempt to do that is part of what led to FPS. Has moved in a good direction. But a lot of vitriol against the current version of 3p sets which is highlighting a lot of things wrong with the PSL from people who use it and agree there should be a better replacement, but oppose the FPS way to solve the problem. It's easy to not like solutions because they're bad, and be living with bad solutions at the same time. It can be frustrating. We're attempting to make something better. Incremental progress. We're trying to be genuine and out in the open. This is going to be a long process.

Hadley: important to not put ourselves in positions of laying blame. That's not helpful. Even if we all do agree on motivations and fundamentals of what the web is, we're not the only players in this field. Incremental steps can open the door to someone else using that incremental step to make things much worse. to create another ecosystem full of money and incentives to keep the status quo the way it is.

Michael: a lot of our designs have been careful to avoid that hazard in particular. Everything we're doing you could write a shim on top of existing web platform .. we're not adding any new capability for a brwoser that has 3p cookies. If 3p cookies are gone, everything is fine. But if you're talking about today's chrome, you could implement everything we've done with js and local storage - we did that. We're not creating new bad things, but highlighting things that were already the case and were bad before.

Hadley: standardising something that is bad behaviour and a hack can bring it to a level fo prominence and a level of usage that it wouldn't have had before.

Michael: I agree we don't want to put forward apis that standardise something we wouldn't be happy with people using them.  some work one way now and as we write them we say this thing in the api is only temporary and will go away but it's a bridge to get to a new better state in the future. in cases wer'e doing things we don't like, we're flagging this.

... for Topics API it's only things we can stand behind... some people don't stand by it and some of those conversations make the API better... 

... Regulatory and commercial pressure - not able to remove third party cookies unless there are some kind of ads replacement technologies.  If we just took third party cookies away it would make ads revenue on google.com much more valuable than 3rd party web sites... 

Dan: will privacy sandbox APIs like topics work?  will they be good enough?

Michael: Two answers. First: CMA in last official statement for Q1 2023 they indicated that they want at the end of the evaluation period that cookies can go away and they don't need to delay things -- their goal is to say yes.  Second thing : timeline and process by which they can get to saying yes - involves Chrome shipping the "replacement technologies" to general availability (100% of chrome instances, not an origin trial) - and then many different companies engaging in 2 different types of experimentation to evaluate the new APIs compared to the old way of doing things. We need to run A/B experiments, taking the data and submitting it to the CMA and having their people perform their own analysis as well - and listen to Ad Tech industy feedback. That's spelled out on privacysandbox.com/timeline. Right now discussion ongoing about how to do that experimentation.  That's what the next 14-or-so months is all about. Whole timeline spelled out.  

Michael: We talk to a lot of regulators around the world including EU countries. In the UK - when we began our regulatory engagement, we were talking to both the privacy regulators (ICO) and competition regulators (CMA)... In the UK regulatory establishment - after talking to each of them individually those 2 regulatory offices came together and instead took the official position was to give unified guidance becan ICO and CMA. Much of that guidance - not UK specific...  CMA's transparency and description of what they've done is an outstanding example of transparency in regulatory engagement. 

Sangwhan: what happens if there is no satisfactory solution matching the timeline?

Michael: offical answer is at some time we will say we want to get rid of 3p cookies in 60 days - CMA can say yes/no or request 60 more days. If they still say no then regulatory could sue google in court for anticompetitive activity.

Sangwhan: is there another jurisdiction where 3p cookie deprecation is blocked?

Michael: the CMA's opportunity to say "no" - is not a special right we gave them. I'm not a lawyer, but it seems like any jurisdiction's competition regulator could decide to sue a company for anticompetitive actions.  No other public info available.

Sangwhan: on API surface - would you entertain the idea of wrapping some of those capabilities behind a policy, so could be turned off?

Michael: I think everything we've shipped has its own permissions policy. Turns out that's important for publishers who want to he ability to control what 3ps on their sites are able to do. 

Dan: user prompting - what's the current thinking about this?

Michael: some of the answer is more heavily reluctance in Chrome to rely on user prompts.  GDPR style cookie prompts on every site you go to seemes like a UI failure.  We ARE prompting the user for permission to turn on TOPICS API in EU or GDPR countries.  I don't think a site by site permission seems appealing... 

Dan: there are things like getusermedia, where it's clear. We haven't had a lot of of blanket permissions, like "as a user, are you okay with sending telemetry data to third parties" (rather than site-by-site permissions)

Michael: Interesting conversation but I don't have a chrome-wide position on that.

Sangwhan: it's a wider permissions problem than how we approach it on the web. Taking away permission from websites... problem at the moment. Not sure privacy sandbox is the right place to fix this. All these super-powered APIs, hard to retract permission once you've granted it. Sometimes you don't know what permission you're really granting.

Michael: these are UX research questions.I can tell you my intuition, but I don't think it's good compared to UX research. A huge part of the answer has to be how much the user understands what they are saying yes to. Hard question to get at. 

Dan: It's a complex problem, I agree. And there are a lot of dark patterns, deceptive user experiences around this. Example: the permission dialogue comes down from top of screen to ask for notifications permission, and there is a screen asking you to click it if you are not a robot... Happens all the time. Approval for geolocation, etc.

Michael: I am all about ecosystem motivations. Moving the web to HTTPS, my story: I was on the make-the-web-fast team at Google, that meant that I turned out to be the person in the position to make your javascript put the "s" on the end of the ad request URL so that ads would be loaded/rendered over https. So I ran the experiment of websites loading of https instead of https. answer: websites lost on average 38% of revenue. Very few websites were secure, so the adverting infrastructre didn't bother to serve over https. They would just drop out, and so the auction price/value dropped. Chicken-or-egg problem, neither publishers nor ad tech would move to https first.

So, I spent 2 years as the engineer who changed google ads so that we eventually requested ads over https on every page, whether the underlying publisher page was secure or insecure. We did that by slowly ramping up the traffic fraction and working with every ad tech company in the world to do this. Told them, "we are monitoring it, and this is how much ad traffic you are missing out on, we are removing your ads from the auction because you're not doing the right thing yet". Strong ecocystem related incentives. And then publishers wouldn't see a revenue hit. 

Dan: just wanted to reemphasise: re other browsers and engines... we HAVE to look at the web as a multi stakeholder enviroment. Market share is not something we take into account. When I hear someone levelling accuasions at other browsers about bad motivations or doing things that don't make sense, I get worried. I don't think it's functional. We have to take that approach in the TAG, because we're already getting yelled at by people who say we are in everyone else's back pocket. And then "why do you hate us so much?"

We're not in the business of trying to destroy anybody. 
In our design reviews, we have commonly used TAG phrases, among them: "is there multistakeholder support?"

So when RequestStorageAccessFor comes to us, we go to the other stakeholders and ask what they think. So if we are getting opposite messaging back, maybe we can help play a role in squaring that circle.

Michael: Do you take into account how other browsers solve the problem: one answer, we don't. or we have a different solution. or: here's what actually happens in practice and we don't like it.

Dan: we'd like to have that discussion in as much an open way as possible. We've tried to do that with First Party Sets. We get that browsers are using Disconnect.me or other lists, and this is trying to do things in a more standardised way, but... 

And we have got to a much better place through working with the FPS team. 

*discussion on the TAG working mode*
