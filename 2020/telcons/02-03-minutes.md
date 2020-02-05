## Minutes for week of Mon 3 Feb 2020

## Breakout A

Present: Rossen, Dan, Yves, Hadley

Regrets: Tess, David

### Design Principles

#### [Discourage Device Enumeration](https://github.com/w3ctag/design-principles/issues/152) - 

Rossen: could go in section 5...?

Dan: yes could be section 5.3?

Dan: what title?

Yves: you don't have a complete enumeration of things - means that when you don't have an enumeration available you go for a less powerful approach.  More efficient alternative - something more suited to what you really need.  We can also say that it has a value for privacy ...

Dan: Data minimisation...

Yves: argument about minimisation about hardware attached to a laptop etc... less of an issue as you don't have 1000s of devices attached - applied even to small sets for privacy reasons...

Rossen: how does it fit together with 5.1?  A scenario when you have multiple screens attached and you want to add one more...  Why would I need to know... (as the developer)

Hadley: i can imagine a scenario in which - you are trying to do something processor heavy and you want to allow the developer to run it on a GPU ... a different use case than choosing which screen... hard to create an abstraction that covers both...

Rossen: in that scenario - targeting multiple devices...  is it still the case that we encourage (in such a scenario) to have enough abstraction - so describe that you have multiple of these but not be too specific. When I read 5.1, I can get behind thise principles... What we're discussing here seems to against these. Could weaken some of the principles ahead of that.

Hadley: I see 5.1 as "things to think about" vs what Tess wrote which is more of a decision tree. It might be reasonable to swap out what is in 5.1 for what Tess wrote.

Rossen: at the end this relates to device enumeration API which sort of goes against section 5...  In Windows platform fro example we have strongly defined API bounderies and layers. Following the logic and steps of proposed in the issue one could interpret the last step as breach of a layer, meaning, exposing device ID or other identifyable data all the way up to the author.

Dan: I think we need Tess to be in this discussion to progress it.

#### [JSON-LD](https://github.com/w3ctag/design-principles/issues/128)

Dan: references the review work for webofthings

Hadley: worrisome - browsers to always interpret it as a JSON object defeats the richness of a JSON-LD data model. Browsers ignoring richness model of JSON-LD... not a good thing to do. If we say that JSON-LD is never for the browser then who or what are we expecting the be the ecosystem that parses it?  Schema.org is representable in jSON-LD and that's one of the most popular syntaxes for schema.org...   I feel if we were to make such a statement it would need to be backed up by research.

Dan: ok. Agreed, it depends on what it's meant by 'implementation'. dbaron's concerns is having a requirement for json-ld in the browser... but a use whithin the browser could be ok. ex. lightswitch app using json-ld without really requiring a built-in json-ld parser. 

Hadley: it fits with most implementations of json-ld i'm aware of. I feel uncomfortable saying: browser it's never going to be your job to cope with json-ld with a data model. There is an awful lot that isn't the browser's job.. that feels different to mek then taking the decision that that isn't going to be their thing.

Dan: [suggest something...]

[hadley to write something on the issue]

#### [Discussion of Permissions](https://github.com/w3ctag/design-principles/issues/144)

Torgo: We've been looking at this since 2014. I think a lot of the workshops on the anti-patterns around permissions... those anti-patterns haven't been addressed by the standards community. They've been addressed to some degree by engine manufacturers-- eg., one of the engines not allowing permissions on the first visit to a site.

...We even saw the anti-pattern of a permission request for push notifications as a "prove your not a robot"...  How to mitigate against that? Better UI, but also better API design? Maybe more like a requirement that takes into account... There was a design review for the clipboard API? where the security and privacy discussion centred around the fact that the API would make use of a permission request, and that therefore mitigated against hte security/privacy issue.  Without noting the fact that sometimes the permission requests are gamed, or are used to trick users into agreeing to a permission.

...So, is there something we could say to encourage API developers to think about those abuse cases?

Rossen: also the permissions [ws paper linked by mikewest](https://www.w3.org/Privacy/permissions-ws-2018/papers/thomas-nattestad.pdf) -  they are hitting some important principles... they have 4 principles they are talking about. the 2nd one seems good... "Permissions requests should be centralized on a single method to enable theintroduction of better user controls and developer consistency." - sort of like having an app manifest where you declare your permissions requests ahead of time...  As a developer you request capabilities from the user - making them part of the manifest means they are verifiable ahead of time, controllable by policy, etc... 

Dan: We learned from Android apps -- many were asking for all permissions. We the tech community. These days, both Android and iOS have more sophisticated models for their apps, where they don't allow developers to do that. You have to request permissions when you need it. And sometimes it prompts you "This app is still using your location in the background. Do you still want to do that?"

...I think this is what we need on the web. We don't want to have a permission last forever.

Rossen: It's the case, yes. We've observed that with app, and appManifest... it's verifiable through automatic detection for whether the API is used. So that you can reject it at permission time, "you're not using any of that!"  Ensuring that applications operate with least privilege....

### Breakout B (US / APAC) - [2020-02-03](https://www.timeanddate.com/worldclock/converter.html?iso=20200203T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Alice, David, Peter, Rossen, Sangwhan, Tess

Regrets: None! Perfect attendance.

#### [Discourage device enumeration, prefer less powerful alternatives](https://github.com/w3ctag/design-principles/issues/152) - @hober, @torgo, @lknik [in context of minuted discussion from breakout A]

Rossen: Quick summary of Breakout A...

... We looked at common approaches, proposed a set of changes in #152 which describes howa device capability/availability API could be designed and exposed.

... Reading current design principles, section 5, 5.1 - they're doing a great job of explaining the issues with fingerprinting, and how to avoid expsing any device information, and yet this particular thread goes more or less agains section 5.1

... the conclusions section, available style API is best, then picker style, ... then finally the device enumeration API. That goes straight against the first principle which is to never expose the devices.

Tess: Let me give some context on that. Section 5.1 does a pretty good job of covering some of these issues; it's been in the design principles doc for a long time. 

... Yet we're still requested to review APIs that do something along the lines of device enumeration.

... Obviously not everyone reads the design principles document, but we could do a better job of capturing the lessons learned.

... I had "enumerate" as the last option because... there is this tension with more powerful APIs... 5.1 says "don't do that". Authors of more powerful APIs tend to retort that they are trying to address a use case. So the options give us a framework of alternatives they could explore in preference to enumeration, with enumeration being a last resort. We are trying to help people achieve a use case, instead of just telling them "NO".

Rossen: I can sympathise.

Tess: Here is an example. 

... Sometimes there is already an API out there that does this kind of unfiltered enumeration. Sometimes when we say "don't enumerate", the issue is one of compatibility with these APIs.

Rossen: From what I've read on the issue... I couldn't find any examples of requests that were anything more than just exposing multiplicity for a particular capability.

... for example, I want to have multiple screens. It's not exposing more capabilities, just a multiplicity for something that's already available.

... Might want to do something different for single vs. multiple GPUs, but it's also about exposing multiplicity. 

... Is this a reasonable characterisation? Have I missed something?

Tess: Web Bluetooth Scanning could be another example.

... This offered a filter-style API, along the lines of "give me a list of the nearby devices which match these criteria"

Sangwhan: correct

Rossen: That's a good example. This creates a more compelling reason to have these rules in the design principles.

... In the previous breakout, this reminded me of one of the design principles that we have (at Microsoft), which is that you don't cross layers; you maintain layer separation. e.g. device information isn't propagated from kernel to user mode.

... The way this issue is summarised, you say "I'm going to jump across all these layers and use the device ID"

Tess: Right, I don't want people doing that. The way I think about design principles is that you frame the _best_ option, then you have various harm reduction exercises. 

... People are going to keep doing these things, so how do we reduce the damage as much as possible.

.. If we make it clear that an unfiltered enumeration API is the last resort, maybe that will help someone look at the alternatives.

Alice: "Harm reduction" seems like a meta design principle.

Tess: I think that's fair.

Rossen: How do we close this issue? What needs to be done?

Tess: Yeah, a PR on section 5.1.

... Need to add more API styles with their pros and cons, guiding people to do the right thing when they can.

David: This might make sense as a separate section, alongside 5.1. 

... I'm looking at this list of 5 things (in the issue) and having trouble convincing myself that this is a strict continnum. 

... For example, could you intersect a picker with some kind of filter?

Tess: You can, I actually think that's fairly common

Rossen: For example a file picker limited to one file type

David: This may fall out as you write it up.

Tess: I'll take an action to write something up.

#### [expand on consistency of naming](https://github.com/w3ctag/design-principles/issues/149) - @cynthia, @alice

Alice: started to try to capture naming-related issues in this one.  David and Tess linked to specific issues about consistency; I started pulling in all issues around naming as well.  I wanted to think about naming advice as a set; so I linked out to getter/setter naming advice, and Sangwhan filed issue on discouraging fancy words in names (plain language).

Alice: Currently a very short section.  Perhaps need to flesh out with these ideas.  I don't want to spend too long in this breakout on it.  Perhaps something I could take offline to collect ideas and start throwing text into a gist or something to look at.  Maybe Sangwhan and I could sync up.

Sangwhan: sure, outside of call.

Rossen: happy to help as well.

Tess: One recent naming issue particularly interesting:  video.`requestAnimationFrame` thing.  Name was chosen for consistency, but timing of callback is different from `Window.requestAnimationFrame` so it perhaps shouldn't be the same.  Should be captured in nuance of issue.

Alice: perhaps we should have ... could we link design-principles as tags in the design-issues repo -- make a `naming` tag for this one to call out?  Want to capture design-principles from the design reviews - would be nice to make cross-links.

Tess (in slack): like “principle: naming”, “principle: enumeration”, etc. labels?

Alice (in slack): yes

Rossen: How often does the TAG weigh in on naming?

Tess: We can weigh in on whatever we want... but people come to us asking for review.

Sangwhan: But another question is whether people will listen.

Sangwhan: Also, about cross-linking.  Travis and I thought about a checklist made from the design-principles that we should refer to when reviewing something.  (Many years ago, never happened.)

Alice: so a checklist for us?

Sangwhan: yes

Alice: I like it.  Fits in with Hadley's doc from Cupertino about how to TAG.

Sangwhan: We don't actually read the design principles when we're reviewing new APIs... hypocritical.

Alice: yes and no; we shouldn't need to read them every time.

Sangwhan: We have an issue template for people filing reviews but we don't have a template for ourselves.

Alice: Thinking about that is part of why I wanted these weeks.

#### [Don't Erode Users' Trust in the Web](https://github.com/w3ctag/design-principles/issues/146) - @hober, @alice, @dbaron

Tess: David made this comment on a different issue that I thought could be a design principle.  I think we should capture it somehow.

Tess: A little fuzzy on venue: design principles or ethical web finding?

... We should capture David's wisdom.

David: Where would this fit in the design principles document?

Tess: Perhaps it belongs in a different document, which is fine... I just thought it should go somewhere.

Sangwhan: I think this belongs in the design principles in some form.

David: I think the idea that it shoudl be safe to visit websites belongs in the design principles... perhaps we need another top-level section..

Sangwhan: Introduction?

Tess: ...

David: Sections six and seve... oh we changed that, never mind. Maybe it could go in section 6.

Tess: Some of those sections could graduate to their own sections.

Rossen: This could easily be the opening of section six, and then expand.

David: Also possible that that section should come earlier in the document.

Tess: David, would you be able to try writing something up here?

David: Yeah, I could try.

... I'm not sure what it would look like until I try writing it down...

#### [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @hober, @cynthia, @dbaron

David: Someone tried to apply our design principles to an argument and couldn't figure out how.

Sangwhan: I have some concerns that we might have over-applied async design patterns.

... Autoplay detection is an implementation detail that ended up becoming a larger argument than we anticipated.

... I've seen cases where Promises over-complicate the design.

David: I think the idea that a reasonable implementation might make it a permission might be a reason to make it a promise

Sangwhan: But equally we shouldn't just use a Promise for the sake of using a Promise

David: This came down to "fast enough to run synchronously" disputes.

Sangwhan: I consider that an implementation detail.

Tess: I think we need someone to swap this back into their head and write a PR.

Sangwhan: I can volunteer if someone volunteers to review/collaborate. I can write a first draft. 

#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron

Tess: This came out of the backdrop filter issue.

... Obviously the ideal scenario is that we figure out a way to achieve interoperability, and have the solution be implementable by all of the engines.

... What do we do when we know we can't do that?

... What kind of advice can we give working groups when they hit that wall? These are all "Plan B" at best, plan A is you don't need to look at this list.

... Something like this list should be in the design principles document.

Rossen: I was reading through this summary earlier on. Even as a guiding/staging principles, this is really good... it's not necessarily about implementability but more about timelines. There's always someone who's going to be first to market, others will follow, others will never catch up.

... The options given there where you offer feature detection and stage the feature, so long as the feature has value to the broader platform, these set of options allow good staging options to (the engines who can't implement/can't yet implement).

... Is there a particular section you had in mind?

... Seems to go to "what is a well-designed API", which might fit in "API surface concerns"

Tess: Interesting that the document lacks an introduction. We could have some front matter here ... this falls into a "general" category that this document doesn't yet address.

Rossen: Yes, that sounds good.

Tess: And this reminds me that we should resurrect the HTML design principles.

Tess: filed [w3ctag/design-principles#153](https://github.com/w3ctag/design-principles/issues/153) to capture this

David: This is also about reaching consensus, a segue into the [W3C Process Document](https://www.w3.org/Consortium/Process/) or the [guide for chairs](https://www.w3.org/Guide/).

Tess: Right: this is as much a process observation as a technical observation.

...

Alice: what he says about the end user concern is saying "the problem this is solving is not a concern to begin with".

Rossen: as part of the principles, valid to have the option of not doing something.

Peter: Getting a little beyond design principles into meta-standardization principles.  Maybe something for another document?

... We do have a few sections in the design principles about new features being detectable, and sections on writing good _specifications_.

... We still need a section on what to do when interoperability is impossible...

... advice could be don't break feature detection, how to write a spec which 

... [RFC 2119](https://tools.ietf.org/html/rfc2119) language on SHOULD and MAY, if features are optional. Don't use non-standard "weasel" words, use clear guidance.

Alice: with backdrop-filter, a lot of spec both engines concerned could implement, behavior would differ in specific edge cases.  Because of how engines worked, there was no possibility of consensus or compromise on   I don't remember how that landed in the spec.  Was it a SHOULD/MAY?

Tess: We recommended that the spec define both things.  In this particular case the API doesn't need to be different; the expectation is that the interop difference isn't a usability issue as much as an aesthetic one.  So maybe option (3) in our list?  I don't remember what's happened since then.

Peter: This sort of thing has come up a lot in CSS; elements of implementation that are beyond the browser's control.  Want to let the implementations be compliant.  Used [RFC 6919](https://tools.ietf.org/html/rfc6919) language once.

Rossen: So how do we track implementability concerns?

#### [How do we track implementability concerns?](https://github.com/w3ctag/design-principles/issues/143) - @hober, @alice, @dbaron

Alice: I filed both, don't remember why it's a separate issue. 

Rossen: About use of github so the right things surface to the TAG?

David: Might be something about wanting spec authors to document implementability concerns.  Could also look at minutes of meeting.

### Breakout C

Present: Alice, Dan, Yves

[reviewing outputs of A & B]

#### [Expand 5.1 with some "how" guidance on identifiers](https://github.com/w3ctag/design-principles/issues/150) - @cynthia, @torgo

Dan: Closed as duplicate.

#### [Proliferation of manifests at W3C](https://github.com/w3ctag/design-principles/issues/148) - @kenchris, @lknik

Yves: We had a meeting with webapps (when) to talk about duplicating manifests.

... I'm not sure it's the role of the TAG to work on this... more the work of the Team to ensure proper coordination.

Dan: Could be in the design principles to not introduce another manifest. We already have a lot of manifests.

... This also came up with mini-apps. The talk of manifests came to the fore in that discussion... it includes a manifest which overlaps a lot with the webapp manifest. I mentioned this a few times. If we're going to do work on mini-apps we don't want to duplicate the webapp manifest. So we could just say something like "don't add more manifests"

Yves: Don't make new manifests with incompatible designs. Webapp manifest is extensible.

Dan: Where might this fit in...

... Could be an additional section in 6 (Other API Considerations).

... _typing_

... This issue seems to have attracted a lot of high-profile attention. I want to make sure we address it adequately. 

#### [input.valueAsDate violate "obj.attribute === obj.attribute must always hold"](https://github.com/w3ctag/design-principles/issues/139) - @dbaron

Alice: Seems like David agreed the design was a mistake. 

Dan: Let's take this to plenary. I can't parse what the outcome of this discussion is.

... Might be able to wrap this issue up this week.

#### [Clarify appropriate and inappropriate use cases for AbortController](https://github.com/w3ctag/design-principles/issues/138) - @cynthia, @kenchris

Dan: We really need Kenneth to weigh in here.

Yves: I recall an issue of people thinking that using AbortController was more or less synchronous. This is not correct, everything is asynchronous. You can abort, and have the promise still resolve. If you are aborting using AbortController, you should not expect it to be guaranteed.

Dan: Can you write that into the issue?

Yves: It might be a bit different... 

Dan: perhaps that's a modification to 2.8?

Yves: I'll have a closer read of the thread.


### Plenary 

Present: Dan, Peter, David, Rossen, Alice, Tess

Regrets: Sangwhan

#### Design principles roll-up

[Discussion on when we do the agenda planning for the next f2f]

[roll-up of design principles issues]

Dan: What can we have "spec text" to review at the f2f to ship?

[Discourage Device Enumeration](https://github.com/w3ctag/design-principles/issues/152) 

Safe to visit web pages / permission prompts (
[Don't Erode Users' Trust in the Web](https://github.com/w3ctag/design-principles/issues/146))

PR for Travis (David to merge)

Naming one ([expand on consistency of naming](https://github.com/w3ctag/design-principles/issues/149))

Dan : On #148 ([Proliferation of manifests at W3C](https://github.com/w3ctag/design-principles/issues/148)) - we need input from Ken who will be with us from nex week.  I have a feeling we might have something to review at thef f2f on this one.

Guidance on JSON-LD #128 - Hadley said she might be able to write something.

#142, #143 - 

Alice: tess raised the issue of adding a front matter / introduction section. that would include e.g. the framework tess & I put together in Rjk. 

Dan: is there something written?

Tess: #142

Alice: yes #142 

Dan: I put myself on the "intro" issue and I could help to write that.

Dan: any other priorities between now and wellington for the design principles?

Tess: the advice about when to not use a promise - 

David: #145 - clarify advice on sync / async

Dan: [chases sangwhan for text] Anything else?

Alice: How can we capture themes from reviews better into design principles "issues"? When things come up in design reviews - any comment we make in a design review should be generalizable - here's why we made this comment and then we link it back to the design principles. Also Sangwhan mentioned - turning the design principles as a checklist for our own reviews.  Can we have a "cheat sheet" version? 

Rossen: +1 to that - a digest version or crosslinking between review templates... 

[discussion of issue templates]

Dan: a littleworried aout a cheeat sheet.

Alice: I am less worried about it drifting.

Dan: i also think we should explore the idea of a quiz

[rossen and alice and sangwhan to work on a proposal]

Dan: maybe a checklist could be appropriate?

Rossen: needs to help the review process vs. adding additional friction

#### Triage for next week?

[Curve25519 in Web Cryptography](https://github.com/w3ctag/design-reviews/issues/466)

David: this is mostly a straightforward spec change except that there is no workign group to spec it.

[UA String freezing](https://github.com/w3ctag/design-reviews/issues/467)

Dan: [summarizes]

Rossen: a couple of more propsals - randomizing the UA string - sort of encouragement I gave: how does this approach affect the different groups involved here. Inflict disadvantage on small browsers, tail-end web (which doesn't move fast), web developers/authors, 

Rossen: if you use GREASE or a key to reference a key to browser and version based on timing - that's a cute approach but it immediately you could abstract a service that does that for you...  

Rossen: i don't hink anyone has done a good enough job of what the impact this will have on the broader industry. SOme MS people engaging.

Dan: I agree with your point about coming up with a list impacts in the ecosystem. I think more data needs to be provided to support the statements being made.

Rossen: allow lists / disallow lists ... yoav's approach will work well if

Rossen: GREASING - adding random garbage around the stuff that is important... if you favour an allow list to say "if this is firefox and version > 70 then I'm happy" - the allow lists will latch on to things it recognizes. The other way that is being used - disallow lists - loooking for things that are there because people cheat and claim to be the dominant browser. the disallow approach will look for things not recognized. when you do greasing you add a token that is meaningless. so disallow approaches will fail because they will always come up positive.  

Rossen: other approach proposed - us a hash but that has a time limit on it - a speicfic browser version for a specific period of time.  Time-based key.  That will discourage and disallow UA sniffing. The downside - someone could reverse this in a service easily.  Puts the long tail web at a disadvantage.

[cookie store API](https://github.com/w3ctag/design-reviews/issues/469)



