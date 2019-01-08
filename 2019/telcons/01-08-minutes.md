## TAG Teleconference
##### 08 January 2019

Present: Dan, Kenneth, Peter, Travis, Yves, Hadley, Alex, Tess

Regrets: David, Sangwhan, Lukasz

---

Agenda:

* [transferable streams](https://github.com/w3ctag/design-reviews/issues/332) @torgo
* [Background fetch](https://github.com/w3ctag/design-reviews/issues/279) @slightlyoff @kenchris @travisleithead
* [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) @slightlyoff @dbaron
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) @cynthia @travisleithead @plinss
* [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282) @cynthia @kenchris @travisleithead
* [HTML General Review: Web Sockets HTML](https://github.com/w3ctag/design-reviews/issues/268) @slightlyoff @ylafon
* [Review MathML](https://github.com/w3ctag/design-reviews/issues/313) @cynthia @slightlyoff @dbaron
* [Vehicle Information Service Specification (VISS) CR pending external feedback](https://github.com/w3ctag/design-reviews/issues/234) @cynthia @torgo @hadleybeeman
* [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101) @lknik
* [IndexedDB Transaction Explicit Commit API](https://github.com/w3ctag/design-reviews/issues/316) @cynthia @kenchris
* [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) @slightlyoff14
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) @slightlyoff
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) @torgo @hadleybeeman

---

Resolved: next week we will hold the call at this same time (21:00 GMT) - in order to facilitate Tess and Alice both joining hopefully.

Resolved: we will invite both new members to both Slack and keep Riot as an experme.

Dan: [outlines the Slack situation]

Peter: Riot is open source, disttributed and has a IRC bridge... and there is a Slack bridge.

Resolved: we love Travis and Alex. 

--- 

### [transferable streams](https://github.com/w3ctag/design-reviews/issues/332) @torgo

bumped 1 week

### [Background fetch](https://github.com/w3ctag/design-reviews/issues/279) @slightlyoff @kenchris @travisleithead

Travis: I read through the material and was ok with the responses on our open issues.  Trusted UI - when you make a background fetch you provide info that can be displayed in the download manager - a string passed through to the UI. UAs should be careful about this... spammy or phishy messages, or deceptive ones, could be an issue.

Alex: could be non-normative text...

Travis: i'm looking for a note on the potential veunerability in the security & privacy section

Alex: makes sense.

Dan: +1

Peter: what's the issue? 

Travis: yes i will open 1.

Peter: can we close this off?

Kenneth: I move to close it off.

Dan: +1

Kenneth: there are some remaining open issues but they are being tracked & i think it's fine.

Peter: closed.

### [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) @slightlyoff @dbaron

Peter: bump until David joining?

Alex: I did have a conversation with Stefan (the engineer working on this). In the timing thing it appears as though it's specified the way David wanted. There is a separate question about other documents that are cooperating - but that's not the root of David's question. I want to get Stefan & David talking about this. Let's punt and maybe invite Stefan.

Peter: Ok - reach out to stefan?

Alex: Ok.

punted to next week.

### [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) @cynthia @travisleithead @plinss

Kenneth: comment 21 days ago that they updated the PR but we haven't followed up.

Travis: I'm skeptical of how useful this is going to be in practice.  A UA might be able to tell you whether it could play smoothly or be battery efficient but there are a lot of factors...  

Hadley: re battery efficiency -- could be important for older devices and developing/less wealthy countries.

Alex: this is one of those trade-offs where it's highly invested eng teams vs the common case.  Big media companies would need this.

Kenneth: but it is bad for the user if you're draining their battery - bad for the web. This seems like something we need to have but is it done the right way? Could be especially useful for VR media...

Dan: is this in fact useful in other domains besides high volume video?  Maybe get feedback from VR people?

Alex: there might be some but [it's a different medium]... Potential benefits might be different. we could ask them if they are paying attention to power at all.

Dan: XR folks will be requesting a review soon so..

Kenneth: what about amazon / hulu / netflix?  Also BBC.

Dan: we could reach out to talk to Mark... (AC rep for netflix).  

Kenneth: we could get feedback from 2nd screen working group.... 

Alex: And Web & TV folks

Yves to work w3c contacts.

Kenneth: let's get feedback and from that feedback we figure out what we do.

### [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282) @cynthia @kenchris @travisleithead

Kenneth: alex's comment about subclassing / not subclassing. They say you should subclass...

Alex: I'll provide feedback today.

### [HTML General Review: Web Sockets HTML](https://github.com/w3ctag/design-reviews/issues/268) @slightlyoff @ylafon

Travis: ... one remaining issue, but otherwise ready to close...

### [Review MathML](https://github.com/w3ctag/design-reviews/issues/313) @cynthia @slightlyoff @dbaron

Alex: within cr community there have been further discussions.... on mathml... idea here now is if folks want to implement it we [Chrome] need e.g. full test suite, etc...

Alex: no layering story - no way to plyg in - maybe this is solved  by custom elements. we have an opportunity to raise that as an issue from the TAG.

Hadley: +1 from me - someone said "we can get rid of it" and that has spawned a signfigant set of discussions refuting that. We can bring the communities together - which would be great for the web.

Alex: math on the web CG - not pusing mathml - looking for accessibility hooks and can't do it with mathml. ohealing that rift and gettign both sides what they want...

Hadley: do we have what we need?

Peter: next steps?

Alex: let's talk about the quality, explainer, users, motivation, quality in terms of modernization (extensibility)... rendering section.

Alex: I'll draft something.

---

Resolved: we all love Alex and Travis and want them to stick around.

Peter: you never the TAG.


