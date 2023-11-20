# TAG Teleconference
#### 13-15 November 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-11-13](https://www.timeanddate.com/worldclock/converter.html?iso=20231113T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov
* [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov
* [CSS `text-spacing` property and its longhands](https://github.com/w3ctag/design-reviews/issues/907) - @ylafon, @plinss
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Web Printing API](https://github.com/w3ctag/design-reviews/issues/910) - @hadleybeeman, @plinss
* [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @atanassov
* [Dubbing and Audio description profiles of TTML2](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman
* [Partioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @rhiaro, @plinss

### Breakout C (APAC / Europe) - [2023-11-14](https://www.timeanddate.com/worldclock/converter.html?iso=20231114T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Pending findings
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @torgo, @rhiaro
* [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman
* [WebCodecs support for AV1 screen content coding tools](https://github.com/w3ctag/design-reviews/issues/912) - @cynthia, @torgo

### Plenary Session - [2023-11-16](https://www.timeanddate.com/worldclock/converter.html?iso=20231116T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


-----


## Breakout A

Present: Peter, Dan, Yves, Amy, Hadley, Rossen, Lea

Regrets:

*Discussion on next F2F we zero in on late Jan in London*

### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

Rossen: ... since pause, there has been at least one breakout on this that did bring alignment... Not sure if other onese since... Not aware of large disagreements.  If that's the case, can we unpause?  Could we say "we like this, developers want it, belongs in the CSS layer and we think CSS wg should work on it."

Lea: we don't need to do a review to say this.

Peter: apple came up with a new design... 

Lea: valid reasons for the new design...  we paused the review to review the end proposal...  we don't even need an explainer to say that... j

Rossen: path forward is pretty well aligned... syntax difference will be resolved by the working group.  

Peter: question is: do we have something to review?

Lea: I don't think we do.

Peter: it's worth waiting until the wg resolves on something... maybe that's happened but I don't see it written down.  Let's kick it down the road.  We already left positive feedback.

*bumped*

### [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov

Peter: should we defer?

Rossen: yes i think we should wait for feedback.

### [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov

Rossen: the explainer is an issue...

Lea: we could ask forn an explainer and move on...

Dan: [leaves reply]

### [CSS `text-spacing` property and its longhands](https://github.com/w3ctag/design-reviews/issues/907) - @ylafon, @plinss

Yves: I don't have an issue with this - the main issue might be "why are we reviewing this now" - it's not early or horizontal so feels weird.

Peter: it's a CSS thing that isn't architectural...

Yves: syntax could be - part of the syntax could impact parsers...

Lea: one concern I have - often features added that only work in a single language... the name doesn't indicate that.  It's a CJK specific thing... but sounds like a  more genral thing.  Maybe just that the explainer is focused on CJK?

Peter: that's useful feedback... 

Dan: does [florian think](https://github.com/w3ctag/design-reviews/issues/907#issuecomment-1774248318) it's premature to review it or not..?

Yves: a bit premature becasue it's not stable enough to reach cr... but still it's pretty stable

Peter: at least one feature that also applies to french..

Rossen: and arabic

Peter: so not ideographic specific. Okay to close?

Rossen: i'm happy to close.

**agreed to close 907, Yves to write closing comment**

### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

Lea: seemes to be adding syntax to do something that is already possible. Adding syntax to work around a performance issue in implementations, rather than focusing efforts on fixing the perf issue. Then again, being realistic might mean we need this sort of thing.

Peter: is it just a perf issue?

Lea: if you look at the linked issue, the only reason this is needed is that using has very high up the tree is slow. Explainer is minimal. Use case is a link to an issue.

Dan: no alternatives considered. Developer complexity?

Lea: [leaves feedback]

### [Web Printing API](https://github.com/w3ctag/design-reviews/issues/910) - @hadleybeeman, @plinss

Hadley: lots of concerns about this. it's a thorougly written explainer including a good security & privacy section explaining about the fingerprinting risk. Mitigiation listed to put it behind a permission prompt. Proposal to not allow the user to choose the printer.  

Peter: I can see the app wanting to filter down a list of printers... but ... i agree.

Hadley: my biggest concern is that it feels like the same discussion we've had with access to files & directories and the OS - crossing the line between what is the web and what isn't the web. Authors say it's based on internet printing protocol...  I'm concerned that this is sacificing a lot of security / privacy for a slightly smoother user experience.

Peter: I share your concerns... It looks like the main motivating use case is for remote desktop applications, like Citrix... I'm sitting at home on my mac, i'm remote piloting a windows machine.. and i want to print to my local printer... not sure how that would work... 

Torgo: this seems similar to [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852), which was all about remote driving someone else's application, or a different computer, but instead of viewing the whole screen, but every single window is cast to you in a different browser window, which would be borderless.

...It was a conflation between the web and virtual desktop kind of thing. 

...We said it shouldn't be standardised in its current form.

Peter: it's a really narrow use case to be adding a feature to the browser, especialy one with such big risks. Feels like this should be handled with a browser plug-in

Hadley: seconded.

...Also, no standardisation pathway for this, and no multi-stakeholder buy-in or collaboration. 

Lea: I'm missing the discusion on the use cases. Remote printing is the main one.

Peter: that's the only one. Says "we acknolwedge there might be other use cases", which sounds like they don't know of any either.

...At A higher level... you're taking capabilities of the client's environment and handing them off to the server.

...I can see the utility with things other than printing, but it's really dangerous.

Lea: Yes, it doesn't see like the problems/pain points are worth the risks. Opens a significant vector and the pain point is niche

Peter: the workaround is that you print to pdf and then print locally. It's not like there's no way to do this.

Hadley: the price for this is too high

<blockquote>
  
Hi @GrapeGreen. We are looking at this in our W3C TAG breakout session today.

We have a lot of concerns about this, and don't think it should be added to the web platform in its current form.

The web has always been separate from the operating system, and implementing this proposal would take capabilities of the client's environment and hand them off to the server. Not only does this pose a large privacy risk, some of which you've outlined in your explainer, but it also moves the boundary of where the web ends and the user/client's environment takes over.

But most importantly, the use case seems rather niche, so the privacy risk is not balanced by a comensurate gain in user experience. Therefore, we are not convinced that the trade-off is worth it. We wondered if this might be better tackled with a browser plug-in.

We are proposing to close this review issue. You are welcome to come back to us with questions, or with a substantial re-architecture.

</blockquote>


### [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @atanassov

### [Dubbing and Audio description profiles of TTML2](https://github.com/w3ctag/design-reviews/issues/897) - @rhiaro, @hadleybeeman

Amy: slight elevated fingerprinting risk - ack'd in S&P questionnaire. Seems worth the tradeoff for accessibility gains, and they've obviously thought about this. Oddly not explicitly mentioned in the Privacy Considerations though.

```
Sorry for the delay. We have no architectural concerns and are happy to see this work move forward.
```

Amy: I think the answer is "carry on, satisfed"...

Hadley: mitigation for the fingerprinting risk?

Amy: if you do the processing sever side ... but then the user doesn't have the option to switch audio tracks...

Peter: i'm fine closing this satisfied.

**amy to leave the comment**

### [Partioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @rhiaro, @plinss

Amy: seems good, what's the catch?

Peter: I know there are other mitigations to using visited links as fingerprinting. i wonder if this is necessary if those other mitigations are used. this has impact to the user. not sure this is a benefit to the user.

Amy: it's a trade-off... but there is a citation that we don't understand how people feel about links being styled differently.

Peter: I rely on it.

Lea: we've learned not to rely on it but when it is there it can be quite useful.

Lea: this partitions history based on origin... if we wanted to implement this using JS  we could do it...  If you can have the union of these 2 then there are few visited links tyou would miss having...

Peter: i remember years ago David Baron had a proposal letting the style of visited links happen but relying on JS...  

Lea: very restricted styling that can be done - only colors really...  The point of this proposal is that it's a normal pseudoclass...

... tbc ...

## Breakout C

Present: Dan, Max, Sangwhan, Yves
Regrets: Amy, Hadley

### Pending findings

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: the fact that app links are using something similar to what is done for letsencrypt - requesting a hash to be put somewhere... different than putting something into .well-known ... verification stage. If you don't have that - the verification - then I think it's dangerous. 

Dan: We need to feed back that they need some kind of cryptographic proof... 

Yves: it can be many things - cryptographic verification - in that case it's about the manifest... in that case you need to ensure that the verification is done off-line. Or if it's online then you need something similar to what exists in the acme protocol... It's prettty similar to what we have in miniapps... 

Yves: their answer is more "how can we do that?"

*yves to leave feedback in that regard*

Yves: you can do it but only in this case - and look at what acme has done for online use case, look at what miniapp is working on for off-line case.

### [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @torgo, @rhiaro

Dan: Not sure I understand [Motivation](https://arichiv.github.io/saa-non-cookie-storage/#motivation) since it's saying devs will use [3rd party?] cookies but in the intro it says 3rd party cookies are being deprecated.

Yves: they imply that there is a mechanism to request accesss to stored cookies... To me if you have a shared storage like that then it's quite dangerous.

Dan: [reviews what we said about storage access api](https://github.com/w3ctag/design-reviews/issues/807) Let's take it as read that Storage Access doesn't open the door to reinventing 3p cookies.

Yves: it's already there in the previous proposal...  Anne / webkit has an issue with this one though https://github.com/WebKit/standards-positions/issues/262#issuecomment-1743104792

Dan: we could ask how they are going to respond to Anne's comment.

Yves: they mean using cookies as a storage mechanism that they can access through the storage api - and those can be 3rd parties... they just want to extend that to plain storage and not using cookies as a storage access mechanism...

Dan: in which case - i'm not sure I understand Anne's issue... what are the additional privacy & security concerns that they feel are unresolved?

Max: what they are trying to say is that this proposal don't introduce more security issues than using cookies... 

Dan: it's clear the proposers think that. But webkit people seem to disagree.

Sangwhan: ...trying to untangle...  I don't think it's a security & privacy concern.. 

Yves: i think it's an API issue...

Sangwhan: doesn't seem like a disagreement on the developer / user need. More the shape of the API...

Dan: feedback we could offer?

Sangwhan: only part where we could weigh in is .. is where the storagebucket API is considered a wrapper... to enable to enable (gate) storageaccess in different ways. that's an API philosophy issue and maybe an architectural issue.  That's where the lack of consensus sits.  I'd have to think about it...  Really the question is - you have to look at 2 places to access the storage in different ways - maybe that's not a good thing.

...We could respond: we would have to think about the implications of the pattern - there's a pattern to be defined here regarding gating storage access...  we could weigh in. if we suggest going down the sotagebucket route that would have worse ergonimics... supposed to be used to have more deterministic behavour under pressure... but it does have the right kind of abstratcions - but as of today i don't think its the right tool ... I can see both sides.

<blockquote>
Hi @archiv - thanks for this - we appreciate the cross-implementer consensus that seems to be developing around the user needs of this feature. We understand the user need and appreciate the effort to not add any additional security or privacy issues.  We've been discussing the "API shape" issue in today's breakout. We're going to discuss further in our plenary call and we hope to leave further feedback.
</blockquote>

### [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman

### [WebCodecs support for AV1 screen content coding tools](https://github.com/w3ctag/design-reviews/issues/912) - @cynthia, @torgo

Sangwhan: the codec is there - this adds a feature config dictionary that's specific to AV1... 

Yves: secreen content tools...

Sangwhan: screen content coding... and extension for av1?

Yves: if the wg is ok with this then there is no reason to say no.

Sangwhan: only part where we might have comments is ... screen content coding is also available on H.265. What if at some point that were to be supported? That's the point I'm not getting.

Yves: adding a dictionary as paremeters seems good to me...

Yves: also - if you're not supporing screen content tools are you supposed to default to the regular settings or should you "bail out"? It should be the first one - graceful degradation.  If you leave the next comment - 

*sangwhan to leave comment and we'll come back to it at the plenary*

## Plenary Session

Present: Amy, Dan, Peter, Yves, Hadley

Regrets: Sangwhan, Max

### Breakout Rollup

#### Breakout A

#### Breakout C

##### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

Hadley: my comment was referencing a discussion on plenary ... rick had called them attack vectors... I was looking at the attack vectors that rick had linked to in their explainer... In the context of this feature and the documents rather than users and user activities... If I remember correctly we particularly wanted them to think through how this could be used on malicious ways... Maybe we should just say "thanks".  

Dan: I think it's the first thing and I think we need to ask them to frame it as Abuse Scenarios rather than attack vectors.

<blockquote>
Hi @rbyers - we just discussed in TAG plenary today and I think what we're asking for is more the first thing - expansion on the existing attack vectors discusion - although in my view "attack vectors" may be too narrow a framing. What we're concerned about is general abuse scenarios of this new proposal: given that this new proposal is in place, what are the abuse scenarios, including by actors who may be "legitimate actors", and what are the mitigations against those? In other words, how may this be mis-used by players in the web ecosystem?
</blockquote>



### Issue Triage

#### [CSS Spelling and Grammar Customization](https://github.com/w3ctag/design-reviews/issues/913)

Peter: maybe we can fast-track.

#### [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916)

<blockquote>

Hi @arichiv @johannhof. We are looking at this to triage it in today's W3C TAG meeting.

We appreciate the careful diagrams in the explainer, since they help us understand WHAT you're focusing on, but can you help us with the WHY? Specifically, when would a user encounter this, and how would it change their experience on the web?  Something that starts like "a user is visiting *xyz* type of site and trying to do *abc* type of action and this can put them at risk to *pdq* type of attack..."

</blockquote>
