# TAG Minutes - Week-of Mon, 15 January 2024

## Agenda

### Breakout A (Europe / US) - [2024-01-15](https://www.timeanddate.com/worldclock/converter.html?iso=20240115T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov
* [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou, @torgo
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hadleybeeman, @atanassov
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [Adding a close event to MessagePort API](https://github.com/w3ctag/design-reviews/issues/923) - @hober, @torgo
* [New attribute to control UA-provided writing assistance](https://github.com/w3ctag/design-reviews/issues/924) - @hober, @matatk
* [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @hadleybeeman, @plinss


### Breakout C (APAC / Europe) - [2024-01-16](https://www.timeanddate.com/worldclock/converter.html?iso=20240116T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman
* [TAG spec review of Storage Access Heuristics](https://github.com/w3ctag/design-reviews/issues/919) - @torgo, @rhiaro, @hadleybeeman
* [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman
* F2F Planning

### Plenary Session - [2024-01-17](https://www.timeanddate.com/worldclock/converter.html?iso=20240117T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* F2F Planning
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2024-01-15](https://www.timeanddate.com/worldclock/converter.html?iso=20240115T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Matthew, Amy, Hadley, Yves, Lea

Regrets: 

#### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

*plenary*

#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

Lea: Dominic got back to me and I asked a question... 

Dan: he did clarify

Lea: yes.  There could still be a way to do this as window.open... *or* it still may make sense to base it on that - additional additional functionalty - and 3rd design option which is orthogonal to window.open what they're doing...  Want to make sure they've all been considered and whether they're all feasible. Do they mean the top level window not including any iframes when they say top level traversable? That's my interpretation.

Dan: leave it a couple more days?

Lea: should I add another comment to explain why I'm asking?

Dan: yeah

Matthew: I think it's right for us to ask about the current issue of the overall design first; we did also ask about spoofing and accessibility so we need to make sure we get answers on those eventually.

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

Hadley: we asked for more more use cases... user-gen content, payments, process... the reply from Shavini said they would update their explainer... then a series of updates on the spec... 

Amy: we also asked for user needs and code examples in the explaienr and I asked a specific question about the api and there has been no response to that...

Matthew: i don't think the last updates are included in the explainer...

Amy: 

Peter: concerned about all of the workarounds for ads..

Amy: the first review was for something for private ads. Now looks like poking holes in what they originally built to benefit advertises

Peter: exfiltration budget.. convoluted.. 

Yves: we really need to look at leaks and exfiltration

Peter: fence interface.. buyer/seller, etc. Isn't this just a mechanism for sending data between frames?

Dan: isn't that auction stuff?

Peter: what they say it's for is frames that can't talk to the outer document... why build the rest of this, to give the communication mechanisms you need for running ad auctions? This is an ad element. It's isn't a fenced frame.

Amy: Appreciate the surface level effort that the keep updating the issue, but it's not helpful that they are just links to PRs with no explanation 

Dan: Well they do say what they've added

Amy: We should ask them to update the explainer each time they add a new feature.

Peter: we've asked before for use cases that aren't adtech.. If it's just an ad element, call it an ad element.

<blockquote>
  
Hi folks -
  
We're noting that there have been many spec changes since our last comment but no changes to the explainer. Can you please explain what has changed since our [previous review](https://github.com/w3ctag/design-reviews/issues/735) and a short explanation of why you made these changes?
  
Thanks for updating this thread with links each time you make updates to the spec, however could you also update the explainer with this new information as you go as well? It's good for an explainer to be a living document.

We're concerned about the direction this is headed since our last review. Concepts such as "exfiltration budget" which seem to be at odds with the stated goals of the fenced frames proposal itself?
  
We've previously asked for use cases and user needs and we haven't really seen anything back. These should be added to the explainer as well. 

</blockquote>

#### [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov

Hadley: I was concerned we not spend too much time if this is one proposal among many in the WG, which seems to be the case

Dan: it seems like some of the feedback we've raised could benefit from hearing what happens with the origin trial. Should we just say that?

Hadley: never a bad thing to have more information, but how much do we want to invest in something that the WG hasn't selected?

Amy: it'd benefit everyone if there are multiple proposals for them to explain to us what the sticking points for consenus are and see if we have architectural advice, rather than us just looking at one proposal at a time with nothing to compare it to

Dan: do we have this because it's part of the Blink process? 

Peter: OT information should feed into the TAG

Matthew: +1 to the idea of seeing what the lay of the land is if there are multiple proposals, so we're looking at them together (or the differences). Expecting some non-zero likelihood that focus management is going to come into this. There isn't specific mention of focus management or accessibility int he explainer. Not sure if it's because it's the same as the normal fullscreen api. Seems like it's worth them being more explicit about any accessibility concerns in the explainers.

Peter: small concern about their api, but not sure if we should give them feedback without looking at other options. Their example, you have to pass in the four coordinates of the other screen.. seems redundant. A window in fullscreen mode vs a window taking up the entire screen? pass identifier screen not coordinates - not sure if there is an identifier.

Matthew: sounds like the coordinates are optional?

Peter: coordinates to target a different screen... if they have a label why can't I just say fullscreen on screen with this label

Matthew: Agree. Says they could also include window bounds features. Implies its optional but not explicit

Peter: their example shows using all the coordinates to target screen. Not thrilled with feature detection.

<blockquote>
  
Thanks for the reply, @Anssiko. Are there alternative proposals for similar functionality that the WG is also considering? Is there is a particular architectural question we can help with, or are you having trouble achieving consensus in a way that we can help with?
  
At this stage, we would recommend that, as a working group, you all work towards consensus and come back to us when you have a single proposal for us to review. 
  
Having said all that, we have looked at what you are proposing here and are recording a couple of thoughts as well.

We noticed that there isn't specific mention of focus management or accessibility in the explainer. Can you make accessibility considerations explicit in the explainer / spec?
  
Another specific question that came up in our discussion: do you require passing in 4 coordinates of the other screen when targeting a different screen? Passing a screen's label may have better developer ergonomics.

Considering the early stage here, we don't think it's appropriate to give a final review at this time. You can re-open the issue if you have any specific questions, or feel free to open a new issue if the proposal changes significantly.

</blockquote>

*proposed close*


#### [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou, @torgo
#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

*bumped to f2f*

#### [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hadleybeeman, @atanassov
  
Hadley: stalled.. needs to be reassigned. Tess was in the discussion at last f2f
  
#### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

*bump to f2f*

#### [Adding a close event to MessagePort API](https://github.com/w3ctag/design-reviews/issues/923) - @hober, @torgo

Dan: can we close this? It's small. It's about adding one specific piece of functionality, related to bfcache. Wanted to make sure Tess has visibility. Propose close?

Peter: okay with that

*agreed to revisit at the plenary*

#### [New attribute to control UA-provided writing assistance](https://github.com/w3ctag/design-reviews/issues/924) - @hober, @matatk

*bump to f2f*

#### [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @hadleybeeman, @plinss

Dan: this is an early review. They've said no considerable privacy concerns expected. 

Yves: there is a contentious issue regarding privacy.. contradictory. 

Dan: [privacy issues for custom web formats](https://github.com/w3c/editing/issues/439). Should be drawn out in the explainer. Positive feedback from safari = still open standards position, neutral from firefox = open but not replied to standards position. You paste something, it causes the original application that copied it to do some work. Doesn't that feel like a potential security issue?

Peter: when dyou do the initial copying the source application puts data on the clipboard - it just doesn't have to put all of the formats it could potentially rpovode, just one and a list of other formats. At paste time, the receiving application says I want it in this format. Then the browser can go back to the original application and say convert this blob of data on the clipboard to this format.

Dan: what happenes when content is pasted from another tab?

Peter: you should be going back to the tab it was copied from

Dan: feels like two situations - copied from another application, and one copied from another tab in the same browser

Hadley: I'm reading that they're not paying attention to cross application use case

Peter: only copying from a web app, to anywhere

Hadley: given the clipboard is generally an operating system thing I think it has the potential to really confuse things for users. A use case is excel in the browser - when you copy an excel cell you can get a whole bunch of formatting and formula to go with the copying. Why that would work from excel in the browser and not excel the application would be really confusing

Peter: this should only impact things copied from a web app. Excel the app already behaves this way. If I have an excel app open and I copy the cells, the only thing on the clipboard is some excel native binary data. It's at paste time that the browser goes back and asks for the format to change..

Dan: scenario says user copies cells from native excel app and pastes it into a web based..

Hadley: in the last sentence of that section with delayed clipboard rendering excel online app is looking to handle custom formats

Peter: if you're copying from a native app, then the OS goes back to the native app to translate the clipboard, this API is not involved. This API is only involved with copying from a webapp. Concerned about - if I copied from an excel online source, and paste into something else, then I'm going to take that data and send it back to the excel online server to translate. You have extra network overhead and serverside processing. I don't think it's extra, if you didn't do this the server would have had to generate all the different formats at a copy time - still saving bandwidth, just delaying and filtering down to the one you need, if you even need it. You can copy things and never paste them. You'd never paste most of the formats that excel can translate into.

Hadley: true

Peter: conceptually I think it's fine. Not sure I see the privacy issue.

Dan: *writes comment*

### Breakout C (APAC / Europe) - [2024-01-16](https://www.timeanddate.com/worldclock/converter.html?iso=20240116T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Matthew, Yves, Hadley, Amy

Regrets: 

#### [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman

Dan: doesn't look like there has been a reply to us. Should this be with concerns? We need to probe more about what Mozilla's views are on this proposal, and their approach to permission policy

Hadley: agree

#### [TAG spec review of Storage Access Heuristics](https://github.com/w3ctag/design-reviews/issues/919) - @torgo, @rhiaro, @hadleybeeman

Dan: this is about mitigation against removal of third party cookies... "unintended impacts" - authentication flows.

Hadley: isn't this trying to solve the same problem as FedCM

Dan: I think so when it comes to authentication.. there's a lot of authentication flows out there already and not all of them are going to immediately embrace fedcm, so it's about making sure things don't break that people are relying on, maybe

Hadley: so we need to be concerned about not settling for the interim solution when people should be moving to the permanent solution. That's a pattern we see often.

Dan: we see the nintendo case pop up as use case 1, which we've already heard about with another proposal.. requestStorageAccessFor?

Amy: is there a path to deprecation, if this is a temporary thing?

Dan: let's ask.. and ask if the design principle for this that they should be implementing the most minimal heuristics possible. I don't see that overriding design goal in this doc. They talk about minimising user facing breakage, and avoiding a solution that is too leniant or cna be manipulated, but they dn't talk about minimal set of heuristics - I feel that should be a design goal. They'd say all browsers have heuristics..

Amy: we talked about one where chrome brought a proposal to standardise on the heuristics, but knowing all implementers do this, didn't we ought to start from a place of all implementers bringing what they are currently doing to standardise, rather than start on what chrome is doing?

Hadley: they're already in a multistakeholder forum in webcompat and privacycg

Dan: slightly concerned about what they list as key pieces of multistakeholder review or discussion - safari docs for this feature, are they pointing to something that is for webkit and is their heuristics? it's documentation of webkit's heuristics, but not a documentation of or indication that webkit is happy to work on standardising these heuristics?

Hadley: looks like it might be that

Matthew: the safari docs say it's a temporary compatibility fix.. interesting sign that they expect to remove it

Hadley: also the intelligent tracking 2.0 document is from 2018.. I'd be shocked if they haven't done any work on it in 5 years

Matthew: there's a link to a recent blog post to talk about improvements..

Amy: in chrome status it mentions users turning heuristics off - does that mean 3p cookies are renabled, or the breaking cases are present? Also, just checking, this exists as an alternative to 3p cookie access right? Not in conjunction with 3p cookies still being on

Hadley: yes

<blockquote>
Hi @amaliev, @wanderview - thanks for sending this our way.

It appears that for this effort to work there needs to be cross-implementer consensus. You've highlighted multi-stakeholder review/discussion - however it looks like these are documenting the heuristics of other engines - establishing that these other engines have heuristics, yes, but is there a consensus on agreeing common heuristics in the Privacy CG and WebCompat efforts? 
  
It seems like a design goal for this work should be to implement the most minimal set of heuristics possible in order to achieve the other goals. Would you agree?
  
Is there a deprecation plan for the heuristics? In the case of authentication, for example, there could be a stated goal to remove heuristics as sites move to FedCM.
  
In the intent to ship, you state that users can turn off heuristics in settings - does that mean that third party cookies would be re-enabled, or would that mean heuristics off and third party cookies off as well? It would be helpful to have language about that in the explainer.

</blockquote>

*posted*

#### [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman

Hadley: assuming the algo is sensible - it's a way of signing and verifying signatures of whoever issued a verifiable credentials..   They've been algo-agnostic... 

Amy: is it's because they're doing cryptosuites for several different algos?  E.g. Jose & Cose?

Hadley: data integrity spec does contain BBS, elliptic curve, edwards.. So yes.  That being the case - miltiple crypto-suites as options for same use case - that seems good...

Amy: they've indicated "17 implementers" demonstrating interop...

Matthew: we had a look at this in APA... One of our members spotted something interesting.  We did an a11y self-review... date formats... they allowed people to specify dates in different formats - we asked about it - they have [replied](https://github.com/w3c/vc-di-bbs/issues/102)... 

Hadley: all VC? 

Matthew: specific to BBS cryptosuite... 

Yves: many protocols are using plain text dates... more readable...   Lots of libraries process those strings... 

Matthew: it seems weird... it seeems like there has been a mistake ...  

Dan: seems like this is in hand

Matthew: yes doesn't seem architectural in nature... part of horizontal review.

Yves: the discussion before is about interop and what would be mandated...

Hadley: i don't see any reason to hold it up

Amy: it's following the pattern they're using for other cryptosuites - i don't have any concerns.

<blockquote>
  
Hi all, Thanks for sending this our way. We are explicitly not reviewing the BBS Digital Signature Algorithm itself (for avoidance of doubt), but your cryptosuite using it seems fine to us.
  
We note that verifiable credentials signed with BBS aren't likely to be interoperable with those signed with other algorithms. (We recognise this is probably unavoidable, given the architecture you're using.)
  
Let us know if you have any specific questions or issues for us. Otherwise, we are happy to close it.
</blockquote>

#### F2F Planning

### Plenary Session - [2024-01-17](https://www.timeanddate.com/worldclock/converter.html?iso=20240117T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Matthew, Dan, Peter, Yves. Hadley, Sangwhan
Regrets: Amy, Lea

#### Appointments Update

*Yves updates us - the proposed candidates from the team will be ratified by the AB and TAG*

#### Breakout Rollup

##### BBS Cryptosuite in VC

Hadley; they want [more feedback](https://github.com/w3ctag/design-reviews/issues/922#issuecomment-1894408455) from us

*bumped to plenary*

#### Things we didn't get to

##### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

Dan: suggest we close

Sangwhan: sounds fine

Sangwhan: *closes with satisfied*

#### F2F Planning

*dan presents current draft agenda for comment*

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

