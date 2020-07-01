## TAG Teleconference
##### 29-31 June 2020

### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/06-29-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2020-06-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200629T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov
* [Cross-origin opener policy reporting API](https://github.com/w3ctag/design-reviews/issues/527) - @torgo, @ylafon, @plinss, @atanassov

### Breakout B (US / APAC) - [2020-06-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200629T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman
* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
* [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov
* [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris

### Breakout C (APAC / Europe) - [2020-06-30](https://www.timeanddate.com/worldclock/converter.html?iso=20200630T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon
* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo
* [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524) - @cynthia, @torgo
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo
* [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

## Minutes

### Breakout A (Europe / US) - [2020-06-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200629T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Kenneth, Dan, Tess, David, Peter, Rossen, Yves


#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Dan: Whats the latest?

Ken: improved on the security section of the spec.

[reviewng latest comment from Zoltan]

David: I think he said "no x cannot happen" a bunch of times to things that can happen. 

Tess: I agree with david.

Dan: I agree. 

[trying to find a way forward...]

Dan: left a comment and bumped - let's try to resolve by next week.

#### [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov

Rossen: we were more or less ready to sign off but wanted Tess to take a look.  At the time we convinced ourselves this was good. Not much has changed.

Tess: I'm happy to trust that.

Rossen: David do you have additional feedback?

David: no.  Other than that definitions could be improved a little bit - they are aware.

Rossen: I'll write up a summary and propose-close it for the plenary.

**UPDATE: Wrote the following comment and closed the review**
<blockquote>
We reviewed this proposal one more time during our June 29 breakout. At this point we are happy to see it continue to evolve with the HTML community.

@dbaron issue about clarifying the concepts of cross-origin and same-site seems well handled.

@atanassov (my) issue about exposing the functionality behind an API such as document.domain has been self-answered after re-reading the explainer and your additional comments, thus, I consider it non-issue at this point.

Given all issues have been address to our satisfaction, closing the review.
</blockquote>

#### [Cross-origin opener policy reporting API](https://github.com/w3ctag/design-reviews/issues/527) - @torgo, @ylafon, @plinss, @atanassov

Yves: I was a bit concerned that there is already a CSP reporting - so many instead of creating a new header, reuse it?

Peter: there are other reporting APIs as well.  we gave them feedback - as long as it's separate, I'm Ok with it being a new header.  hpkp has the same thing.

Yves: that's just at the http level, not a JS API

Peter: true.  The point of this header isn't to generate a report...

Yves: It's reporting what will be blocked but don't block anything. Apart from the point I made about CSP - seems OK to have that kind of thing.  Good section on how not to leak private information or leak info to 3rd parties.

Peter: they went through a lot of work to figure out what can and should be reported...

Dan: Why is this whatwg and not webappsec?

Yves: cross origin opener policy is defined in Fetch...

Tess: what is the relationship between this reporting API and the reporting API defined by the web performance working group?

Yves: that also uses structured headers... so could be a good match.

Peter: it's not just the fact you want to report but you want to get a report as if the cross-origin policy is on.  You need to have a report-only mode. You could put is a switch in the one header and not haev 2 headers... Useful to have reports one way or the other... 

Yves: related to secure context as well...

David: [sumarizing] opting into a stricter model so browsers can have better guarantees about site isolation - because of SPECTRE.


### Breakout B (US / APAC) - [2020-06-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200629T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Peter, David, Rossen, Alice, Brian Kardell, Tess

Regrets:


#### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

Alice: Only remaining issue is what to do with links. Brian gave us 3 options. 
1. Punt for now
2. chose a safe list for href - more in line with the original design of mathML
3. add an `ma` element similar to link.

... we like option 1 since we don't know what the uses cases really are and that will give us time for arrive at the best solution for the long run.

Brian: My preference as well. Not the CG preference, but certainly mine. Being forward looking this seems to be the best option at hand and too many unknowns. 
... There is lots of excisting content using links and we need it for backwards compat.

Peter: Existing content is in XML?

Brian: All over the place, but yeah, mostly. MathJax too.

Alice: The MathJax stuff is not super relevant? Because it generates html?

Brian: Yes and SVG too. A lot of folks have XML and all they need to do is change their mapping and regen.

Alice: So in summary, Punt for now seems the best option and the one we all agree on?
(summarizes more unknown behavious - various modality of click etc.)

Tess: The idea behind Html.... was to fire the href on the element. 

Peter: If we consider XHTML, any element with an href can become a link. 

Alice: How feasible is it to embed HTML?

Brian: You can't

Alice: Because it breaks formatting?

Brian: Yes and it is weird. 

Tess: Is that any worse than a `tr`? The goal isn't to make any arbitrary HTML work isnide MathML, but, make MarhML as capable as HTML in terms of links at least.

Peter: Any use cases where an entire row is supposed to be a link?

Brian: Yes, not in the same was as a table row in HTML but `mrow` can be a link.
... If we have a new math-link element in the future, it will make a lot of sense as it will be as useful as HTML and SVG.

Tess: If `mrow` is supposed to be link-capable, I would expect the same effort will make `tr` the same, right?

Brian: ack

David: Does option 1 mean there aren't problems for linking individual symbols? And using HTML doesn't interfere with MathML's formatting ??

Brian: No

Alice: Why can't we have links in the middle?

Brian: The parser as it will close everything in the current context. 

Peter: ??

Tess: Use case question. I recall from school that, when you have an equation you've never seen before, the teacher used to point out particular parts of the equation - the numerator for example etc. I want such parts to be clickable and usable for such examples.

Brian: Right! This is definitely a use case that we're tracking and want to make possible. Hence the reason for links :)

Brian: What about Sangwhan's comment?

Alice: (summarizes Sanghwan's comment)

Brian: Honestly, don't understand the comment. I will ask for more details.

Peter: Just did some testing and it seems that Firefox is pretty happy with HTML links around `mrow`. 

https://software.hixie.ch/utilities/js/live-dom-viewer/?%3Cmath%3E%0A%3Cmrow%3E%0A%20%20%3Ca%20href%3D%27https%3A%2F%2Fgoogle.com%27%3E%0A%20%20%20%20%3Cmrow%3E%0A%20%20%20%20%20%20%3Cmn%3E%202%20%3C%2Fmn%3E%0A%20%20%20%20%20%20%3Cmo%3E%20%26%23x2062%3B%3C!--INVISIBLE%20TIMES--%3E%20%3C%2Fmo%3E%0A%20%20%20%20%20%20%3Cmi%3E%20x%20%3C%2Fmi%3E%0A%20%20%20%20%3C%2Fmrow%3E%0A%20%20%3C%2Fa%3E%0A%20%20%3Cmo%3E%20%2B%20%3C%2Fmo%3E%0A%20%20%3Cmi%3E%20y%20%3C%2Fmi%3E%0A%20%20%3Cmo%3E%20-%20%3C%2Fmo%3E%0A%20%20%3Cmi%3E%20z%20%3C%2Fmi%3E%0A%3C%2Fmrow%3E
...(discussion about Peter's example)

Peter: So maybe you can just throw `a`s randomly inside MathML?

Brian: Not sure what's up here. Will investigate more.

Rossen: So have we convinced ourselves that we should advice any other option than 1 at this point?

Alice: Perhaps not. We should continue working with the MathML folks and see if that'll work for them.

... (more discussion about Peter's example) Seems to work in Firefox...

Brian: I suppose the question still is - can we try to document what's happening with Firefox and seemengly Safari or go with option 1? FWIW, the CG is interested in the TAG's opinion.

Rossen: Would they be OK with Option 1?

Alice: (missed)

Brian: Sure. The CG will also be interested what the current browsers do and how to transition everyone to a compat state.

David: I'm OK with 1 as long as linking of tokens works reasonably and in interaction with other things...

Brian: For sure. 

Alice: David, is the existing FF support of links (`href`) everywhere, any thoughts?

David: Not sure.

Alice: Later if you decide you want shadow DOM, you will be OK to change?

Brian: Yes.

Peter: HTML5 dropped the ball on namespaces and made the situation confusing. There is no way to gracefully exit/enter between HTML, MathML, SVG. Transitioning between them requires closing everything and only then transition into another space.

Brian: Thank you for all the time spent on the issue. Sounds like there is agreement about use cases and the importance of linking, we just don't want to rush into the specification before we know more?

Alice: Yes, and unshipping such changes in engines will be complex.

Rossen: So recommend option 1?

Tess: Sure, we will summarize and recommend in the issue.

Brian: Having two shipping impls makes it difficult.

Alice: Yes, and unshipping is difficult. Also, we don't lose much by delaying a concrete specification.
... also, it will be imprortant whether implementers are willing to remove the existing behavior of `href`, or else we'll still have to deal with the disadvantages of it in the future.

Tess: Have we asked if unshipping the current `href` beharior is something implementers would do?

Brian: Not formally. Happy to go ask around.

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @alice, @torgo
#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
#### [Client-side video editing (MediaBlob)](https://github.com/w3ctag/design-reviews/issues/514) - @cynthia, @kenchris, @atanassov
#### [making the "total" field optional in PaymentRequest API](https://github.com/w3ctag/design-reviews/issues/512) - @hober, @cynthia, @kenchris

### Breakout C (APAC / Europe) - [2020-06-30](https://www.timeanddate.com/worldclock/converter.html?iso=20200630T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Yves, Ken, Sangwhan

Regrets:


#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

Sangwhan: Sort of OK about the spec now aside from the side channel.  HID can be anything. Means you could potentially write to and read from the device.  SO you could use it as a cross-origin communication. Exclusive access is something I suggested.  If you have 2 game tabs, switching from one to the other would involve a hand-over process.  

Dan: [nonedebug comment]

Sangwhan: I'm concerned about using it to share tracking cookie identifiers across origins.

Dan: agreed.

Sangwhan: tracking companies do whatever it takes to track you across origins.

Dan: [ref unsanctioned tracking](https://www.w3.org/2001/tag/doc/unsanctioned-tracking/)

Sangwhan: something innocent like a gamepad you leave plugged into your computer could be abused like this.

#### [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon
#### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo
#### [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524) - @cynthia, @torgo
#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo
#### [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

Ken: I think [Bo's comments](https://github.com/w3ctag/design-reviews/issues/498#issuecomment-643548255) are pretty good.  I'm OK with the idea. It's opt in. It seems usable.

Sangwhan: I'm not agreeing with the webkit position.

Ken: [giving some examples of when you want to have more control]

Sangwhan: I don't understand why they are against it. 

Yves: when we say it looks OK it doesn't preclude it being worked on in a working group or that others can disagree.

Dan: yes.

[we agree that it looks OK]


### Plenary

* Present: Dan, Tess, David, Sangwhan, Peter
* Scribe: Sangwhan

Dan: One of the things we discussed is publishing the design principles as a note. We also need to do readouts on the different breakouts.

#### Readouts

##### Breakout A Readouts

Dan: We talked about WebNFC, which led to some discussion. We bumped it to next week. Multiple people are working on additional stuff on privacy prompts. We'd like to see more progress - David wrote a very good comment two days ago. Not much further to share, aside from there is work being done. It would be good if they could respond to our feedback and move forward under consensus.

... Origin isolation, which we decided to close.

... We need to discuss Cross-origin opener policy reporting API this more in breakouts, so maybe next week.

Peter: Next week is non review week.

##### Breakout B Readouts

David: B was 100% MathML, with special guest Brian Kardell. We mostly agreed with Brian's position, personally I had some concerns but he will take the feedback back to the CG and will report back.

Dan: What is the feedback?

David: Punt on adding link-y things into MathML for now.

Dan: Can we close?

David: Not sure.  Question for Alice?

Sangwhan: Brian contacted me yesterday to clarify what I was intending, but now that that has been communicated I'm okay closing this

Tess: At the end of the call, Alice asked Peter or me to leave a comment but I didn't follow enough of the conversation to understand what the comment was supposed to say.

Dan: What about other stuff?

Tess: The entire call was about MathML.

Peter: I've bumped the ones that we didn't manage to get to.

##### Breakout C Readouts

Dan: Mostly talked about miniapps. We need to talk about the feedback document we've drafted. Before that we should probably mention WebHID. I see it as review complete, is that a mistake?

Sangwhan: No, the review is complete. We've raised our concerns.

Dan: We bumped it and left feedback. Namely around being able to use this as a side channel communication device across origins. Blink shipping process we didn't get any feedback it seems.

Tess: They still haven't given us the new version.

Dan: Virtual keyboard show-hide policy, we proposed closing this one.

Sangwhan: Our closing comments were that we as a group are fine with this, but if implementors disagree that's a WG issue.

(Sangwhan to write closing comments)

Dan: So, miniapps. We reinforced the comments we had during Fukuoka, we talked about the context and conflict/incompatibility different technologies in the web platform. The gist is to not make a parallel web; we specifically mentioned that multiple manifest files are not desirable during our statement in Fukuoka. Also there is URI, and lifecycle which have similar issues.

... As for Jeff's commments, I think the passive tone bit is something that originates from me; should we change it to be more specific?

(Discussion on Miniapp feedback)

#### Agree to publish the design principles doc as a whatever (note)

Tess: Should probably discuss this.

Dan: Where are we at with this?

Peter: There was feedback about changing APIs to features. There was some disagreement within the group, we need to spend more time on it.

Dan: Regarding referencing this, having this on w3.org might carry a bit more weight to some people.

Peter: If it's a note on TR-space we can technically just publish through echidna.

(Discussion on the deployment process)
