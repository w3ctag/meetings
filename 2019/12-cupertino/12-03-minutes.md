## TAG F2F Cupertino
##### 03 December 2019

Present: Dan, Yves, Tess, Hadley, Peter, David

Regrets: Sangwhan, Kenneth, Alice (morning only)

Scribe: David (start of morning), Yves (end of afternoon)

---

Agenda:
* 9:10 - 10:10 - Plenary - Triage; agenda plan for Thursday (Fugu)
* 10:30 - 11:30 - Slot #1
* 11:30 - 12:30 Lunch
* 12:30 - 13:30 Slot #2
* 13:50 - 14:50 Slot #3
* 15:10 - 16:10 Slot #4
* 16:30 - 17:00 Readouts

---

### Agenda and scribing

Scribes: David (Tues am), Yves (Tues pm), Tess (Wed am), ? (Wed pm), Hadley (Thu am), ? (Thu pm)

### Issue triage

#### [Screen Capture API (2019)](https://github.com/w3ctag/design-reviews/issues/440)

Examination of [previous issue](https://github.com/w3ctag/design-reviews/issues/309).

Assigned Dan, Hadley, Lukasz.  Set tags.

Assigned to breakout session 2b.

#### [WebRTC playoutDelayHint](https://github.com/w3ctag/design-reviews/issues/441)

Assigned Yves and Tess.

Failed to find appropriate breakout slot.

#### [Browser-assisted performance ablation studies](https://github.com/w3ctag/design-reviews/issues/442)

Hadley: Seems to be about being able to better perform tests to measure site performance.  Specifically stop certain things in order to avoid having the UA stop them because it's overloaded??

?: We're... interested in the use of the term "ablation".

Dan: I'll assign myself and comment.  (Dan writes comment.)  This looks like it might be too early; does it need to be suggested to WICG?

Peter: I think this should go to WICG first, not come straight to us.

Dan writes comments to close issue.

### Other issues not assigned to breakouts

Dan: There are some others where we didn't assign to a space:  raw clipboard #406 (Thu AM with Alex), carriage of web resources in ISO BMFF #285 (chat with dsinger at a break)

#### Periodic Background Sync #367

Yves: Periodic Background Sync

Tess & David: We know some people with opinions.

Dan: Maybe Yves can look at Periodic Background Sync in breakout time 3.

Yves: Apart from the privacy issues?  Some folks pushed back, so it's not in charter for Service Workers WG.

Assigned Yves, Tess, David.  Added to breakout 04a.

#### Other

Dan: Other issues not assigned to breakouts that we want to pull out?

Dan: Assigned #350 to a Sangwhan & Kenneth breakout

### Agenda plan for Thursday (Fugu)

(defer topic to when Alice is here)

### Other agenda topics?

Peter: Tim emailed www-tag about CORS and HTTP2.

Dan: Do you want to introduce topic tomorrow morning?

David: design-principles doc, maybe other repos?

Tess: Question for a breakout of whether we should revive the HTML Design Principles doc -- likely wants to come back to plenary.

Dan: We should file issues against our design principles document when we're in breakouts.

Tess: One piece of feedback from Media WG at TPAC was that they'd like us to update our design principles doc.

Dan: If we put some focus on closing issues over the next 3 days, helps us to dig out, and then next time we can organize focused work on design principles later.

-----

Dan: another meta point, maybe for the meetings schedule topic on Thursday.

Dan: Should we try to reduce the number of meetings we have, from a green web flying everybody around the earth perspective?  Is theer an alternative?  Could we experiemnt with a remote TAG meeting tht's not just an hour, but a couple of days.

Hadley: I think it's a good idea... but we get so much done in those concentrated periods of time.

multiple: time zone issues

Dan: We could do breakouts organization thing that takes into account timezone.

Tess: Related but distinct thought:  People's travel budgets are different.  Budgeting over course of year is different.  Some people almost had funding issues coming to end-of-year face-to-face.  Should think bout things from perspective of self-funded folks.

Yves: In a meeting like that we know whole day is devoted to TAG work -- in the middle of a workday more difficult to get focused on TAG things.

David: Should we do a 5 or 6 hour chunk?

Dan: Maybe for one day, not for three.

Tess: Suppose we remove one face-to-face and replace with three of those spread over three months.

Dan: Do we need the plenary?  Could we organize it as breakouts.  Keep the plenaries as they are but an hour every week.  Be more systematic about scheduling breakouts.  Build an algorithm and schedule the breakouts.

David: I think we used the breakouts well for a few weeks, and then not...


## Breakout 1A (David and Peter)

### #405	[CSS Modules](https://github.com/w3ctag/design-reviews/issues/405)

Discussed issue; recorded notes in comment on issue.

### #422	[Microtransaction payment handlers](https://github.com/w3ctag/design-reviews/issues/422)

Closed issue.

### #395	[Element Timing API for text](https://github.com/w3ctag/design-reviews/issues/395)

Briefly discussed, added one comment to the issue, and closed it.

### #425	[[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425)

### #366	[JS Self-Profiling API](https://github.com/w3ctag/design-reviews/issues/366)

## Breakout 1B (Hadley and Tess)

https://github.com/w3ctag/design-reviews/issues/414


Hadley: Use case: advertising. 

Hadley: who will be the trust token issuers? 

Hadley: Risks: issuer compromise

...If they don’t genuinely anonymise…

Tess : This is based on an architecture from cloud flare. Privacy pass. 

Hadley: Presumption of the model: reputable sites that want to rely on this kind of info will only rely on trustworthy issuers.

...If they’re issuing me identifiable tokens, then they can track me. 
And it’s the publisher’s choice, the user doesn’t get to choose.

Tess: My worries are similar. The potentially dodgy issues are concurrent with the existing web architecture: ads and captchas work like this. 

...So my worries: 1. We've not done this well in the past; can we do it better now?

...Consider web payment request. Browser has a set of payment methods. Shopping site has a list of payment methods it supports. At purchase time the site supplies its options; the browser picks. Nice quality: the UA has a role in choosing.

Hadley: so we could do this in the same way. The user has a list of issuers and the site does. And if they have an overlap, great. Then if not: you have to work out how this could work.

Tess: Consider a use case where a government is the issuer. They know a lot about you, and then have your browsing history...

...The issuer can correlate to a user on their issuance

Hadley: They could fingerprint you when they issue?

Tess: yes. and then could they attach that to the SRR process and identify you?

...I can imagine a keylogger or something being hidden in software to help users get rid of these annyoing captchas.

Hadley: This sounds like this works perfrectly when everyone is playing nicely.

Tess: Yeah. Privacy Pass is used by Tor users, since they can't pass captchas. Hinges on the fact that cloudflare is a hig-trust service. Generalising it to any issuer loses that aspect. 

...Obviously, if this ships -- day one, cloudflare is ready. 

...So the privacy and security considerations aren't looking at the attackes from the perspective of humans. WE are looking at it from the perspective of users. And what are risks.

Hadley: I agree. 

Tess: It's unclear to me what is in the trust token. How many bits? If it's 33 -- you have a globally unique identifier for every human being on the planet. 

Hadley: assuming you only have one issuer

Tess: Sure, but I'm assuming the surveillance case. A hostile government that requires sites to use them. 

...You could categorise users.  Say it's 4 bits, 16 buckets. You could categorise your users. And if the site is required to use them... 

Hadley: And then you're just adding an identifier to your users. 


## Breakout 1C (Dan and Yves)

#### #354 [Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/354)

[We asked for an update and proposed closing the issue]

Yves: The purge mechanism issue - in the design questions for signed exchanges might have a mechanism similar to the stalte state in HTTP caches. 

Yves: i am pointing them to that...

[yves leaves comment on issue](https://github.com/w3ctag/design-reviews/issues/354#issuecomment-561306127)

#### #352 [Subresource Prefetching](https://github.com/w3ctag/design-reviews/issues/352)


## Breakout 2a (Hadley, Dan and Peter)

### #438 [MathML Core](https://github.com/w3ctag/design-reviews/issues/438)

Plus special guest Brian Kardell

Brian:  MathML hasn’t gone far because in the blink split, chromium decided they weren’t interested yet. It hasn’t been a priority because it doesn’t help sell ads or monetise videos.
It just helps people share math and research. So it’s ethically important

Torgo: What's the current status? And what's different about this than previous? And which implementations? What venue?

Brian: It had a working group, it is a rec. It has an implementation in Firefox, in the 2000s. In webkit, which was also redone after the blink split. Igalia has an implementation in chromium which answers questions google had, like how does this fit into the platform? And is this existing or new?

... We think there is a core wihich is interoperable. Benefits of getting everyoen to agree and making this well specified -- this is the thing to do.

... So MathML is the things from MathML3 implemented in the other browsers and have proven use on the web.  MathML3 had lots that wasn't implemented, and maybe didn't fit with the web.

...We're looking at the weirdness as issues in this implementation. 

...The creation of a normalised DOM, so that it can move forward like everything else: this is shipping in firefox and webkit. There are now 2000 platform tests for mathML. Scores of both engines have gone up in the past 4 months because they're doing work to align with the spec.

Torgo: What do you want us to focus on?

Hadley: why were there features in mathml 3 that weren't fitting with the web?

brian: basicaly yes. We had a forked co-evolution where mathml, html, and CSS were solving the same problems in parallel. But mathml did things differently because it had a need. And the others did things on their own.

...There is also a branch from its xml past. has the cnocept of math being in an error state if there is invalid markup -- and we had to resolve that.

hadley: so how much does Core conflict with html and css?

brian: hopefully not at all. That's our goal, to show how this IS html and css and DOM. Our goal has been to make them less special.

hadley: that sounds great!

brian: We need:

...1. It's part of the process, to ask you for a review

...2. Especially because of this history -- it was removed from blink, and in the same 6 month period, the Extensible Web Manifesto  explained what to do with new stuff. So we're proposing some pretty specific answers, and it feels relevant to me to get TAG feedback.

...3. Also, does the TAG agree with our ethical argument. I personallly think it's not good to fundamentally disadvantage this kind of text. It's what the web does. It's an important part of text, and our society benefits from sharing mathematical information. 

dan: Are there chrome people who are participating?

brian: yes, a lot. Rick Byers, Ian Kilpatrick, and others have worked with us along the way. They want to see this solved -- it's just that it's nobody's priority. 

hadley: what are the chances of this being implemented in chromium?

brian: it's implemented already, under a flag. I'd guess high chance of being fully implemented.

...We've left ourselves a year to finish answering questions. TAG are part of the checks and balances.

torgo: I haven't seen any alarm bells. It's a shame sangwhan isn't here; he'd have thoughts. 

...I would ask for more specificity about what's changed since 3, what areas you want us to focus on.

hadley: is anyone unhappy with this?

brian: None that I'm aware of. Anything that isn't what people were hoping for is inevitably going to be disappointing, which is common in web standards. There are people who want essentially LaTEX, and they'll be disappointed. But it shouldn't be super disappointing because we can show you a custom element that does that, and it fits with the platform, etc. 

...But that is actually the goal. From this moment forward, this is what will be interoperable. if we need additional semantics, we do that through ARIA. CSS stuff goes to CSS working group. Etc

torgo: Should we focus on your Applying Extensible Web Principles section in your explainer?

Brian: yes

torgo: I think we can move forward on that basis. 

hadley: you're talking about how to move forward. What are the choices?

brian: Options include:

...1. We start over. The people who want LaTEX in the browser want this.

...2. There are people who say we have these libaries. this is fine, with a few more primitives.

...3. And there is this group, who recognise that we have mathML. Currently to render text, we have to load a Js library, turn it into images or svgs, ... it's a huge ask for text.

torgo: looking at the previous TAG review (issues/313). It feels to me like you're accomodating all of our feedback.

brian: the challenge is: there was a different community group already. the person leading that was an advocate for mathml. just before that TAG review, they wanted to work with an alternative.

...It's important to keep everyone on side and recognise the good work that's being done. 

torgo: I think we have what we need to move forward. I'm also receptive to the ethical concerns here. In light of climate change, and scientific research that benefits humanity -- 

hadley: or medical research

torgo: this stuff matters. 



## Breakout 2C (dbaron, yves)

### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

discussed briefly, added one comment to issue

### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389)

discussed and added comment to issue

## Breakout 3B (Alice, David)

### [Launch events](https://github.com/w3ctag/design-reviews/issues/372)

Refreshed our memory of the issue, made a few comments, and decided to close.

### [CSS Intrinsic Size](https://github.com/w3ctag/design-reviews/issues/437)

Quick ping and set to pending external feedback given recent discussions.

### [File Handling](https://github.com/w3ctag/design-reviews/issues/371)

Alice filed one issue, left as pending external feedback since it looks like theree's current activity.

## Breakout 3C (Hadley, Dan)

## Ethical Web Principles finding

We reviewed the [pull request](https://github.com/w3ctag/ethical-web-principles/pull/15) and made some additional changes based on discussions and comments.

We have also reviewed the [open issues](https://github.com/w3ctag/ethical-web-principles/issues).

We will review the PR in plenary session later in this f2f and hope to merge them before we close. 

## Readouts

Going through the list of issues.

#421 #384 and #385 issues seems stuck, so possible 'close' for them.

For WebSocketStreams and WebTransport, it would be good to have explainers that are not targeted at specialists of those specification.

Ethics: completed PR that will be reviewd in plenary tomorrow.

partial enums defined in multiple specifications, talk about that in plenary tomorrow.

rescheduling unprocessed issue of today's breakouts to other sessions.

