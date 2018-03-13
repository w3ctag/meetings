## TAG Teleconference
##### 13 March 2018

Present: Dan, David, Peter, Alex, Yves, Sangwhan, Hadley

Regrets: Lukasz

---

Agenda:
* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) David

David: sorry, last week meant to set up time to talk to Matt, but didn't.

Dan: punt to next week

* [Img decoding attribute](https://github.com/w3ctag/design-reviews/issues/220) David, Sangwhan

Sangwhan: this seem to be shipping?

Alex: we're seeing cases (e.g., map tile loading on a fling) where it can have a big impact

Sangwhan: it feels like a quick-and-dirty hack that we might regret at some point...

Alex: can we recommend something better?

Sangwhan: that's the problem. Can we have another week on this?

* [Review of signature-based resource loading restrictions](https://github.com/w3ctag/design-reviews/issues/186) Peter, Hadley, Sangwhan

(connection issues)

Dan: Peter, do you need help with the feedback?

Peter, no ,just need time.

(we punt the issue)

* [HTML General Review](https://github.com/w3ctag/design-reviews/issues/174) Travis

(missing a Travis)

Moving to next week.

Backlog:

* [Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/226) - Sangwhan

Sanghwan: we did review this at last F2F...provided a bit of feedback. They got back to us on how to deal with the <canvas> case; streaming the canvas to a video. ROundabout but good enough for experimentation. What's missing is user-interaction, but that's out-of-scope by design for security reasons.
  
Dan: can we thank them and close this?

Sanghwan: was going to suggest that.

(Sanghwan to close the issue)

* [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Alex / Hadley / Travis / Peter
* [OffscreenCanvas](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / David / Travis
* [Review Accessibility Object Model ](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / Travis
* [Secure Contexts & TC39](https://github.com/w3ctag/design-principles/pull/75) - Sangwhan

Sanghwan: in our design principles doc, we note that new features should use secure contexts. This has become a problem at TC39 where some folks are unhappy because JavaScript runtime != web browser.

(we stare at a very long thread)

Dan: there's a pull request?

David: it's mine, still need to revise it.

Dan: is the debate "should new features in JS only work in Secure Contexts?"

David: a lot of folks on TC39 don't want Secure Context forking within ECMAScript

Alex: every implementing team has exactly the same feedback. ECMAScript isn't special.

Dan: but it's a language...right?

Alex: so is HTML. So is CSS...so what?

Dan: I'm sympathetic to the notion that JS runs outside web contexts

Alex: seems fine for us to say "secure contexts are only about the web...if you aren't in a web context, the origin model can't help you and you need to bring your own security model. Secure Contexts aren't a solution to a problem you have there"

Dan: this is at a lower level, right? This isn't about camera access...you woulndn't get an operator.

Sanghwan: there are some capabilities you get from the language, right? Can't think of any.

Alex: how will this play with Mozilla's new restriction on all new features behind secure contexts?

David: if we did this a few years ago, async functions would have been restricted. Would have been an interesting debate.

Alex: so what's likely to happen here for new JS features in FF?

David: I don't know yet.

Sanghwan: we should have a position here.

Dan: yes. Suggest we address at F2F.

* [&lt;link&gt; rel=modulepreload](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/213) - Andrew
* [Decentralized Identifiers](https://github.com/w3ctag/design-reviews/issues/216) - Hadley
* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) - Hadley, Travis
* [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David
* [import.meta.url and import.meta](https://github.com/w3ctag/design-reviews/issues/208) - Alex

Triage List: 

* [W3C DOM](https://github.com/w3ctag/design-reviews/issues/229)

Alex: what's the delta? ... also this appears to be for CR ... quite late ...

Dan: I'll assign myself and we can try to do something here.

Alex: looks like an update to whatwg. E.g, WHATWG has ctors for EventTarget whereas the 4.1 draft doesn't:

https://dom.spec.whatwg.org/#interface-eventtarget
https://www.w3.org/TR/dom41/#interface-eventtarget

Dave: another question - how much do we want to review vs. whatwg doc. The diffs might be worth reviewing

(general agreement)
  
Assigned to next week, pending external feedback.

* [Should WebRTC be Secure Context](https://github.com/w3ctag/design-reviews/issues/228)

David: filed while we were at our last F2F. Scheduled for TOK

Dan: nobody's assigned? Travis assigned now.

Alex: what's the current state of `getUserMedia` in secure contexts in various runtimes? We know Chrome limits it...others?

Peter: unsure about firefox

Sangwhan: Safari might allow over HTTP? Testing now. Only allows in Secure Contexts.

David: the issue doesn't list browsers other than Chrome.

Sangwhan: Safari and Firefox only allows on secure contexts based on a quick test.

* [CSS ::part and ::theme pseudo elements](https://github.com/w3ctag/design-reviews/issues/230)

David: we've had a bunch of discussion here. I'm mostly happy with this except for the names.

Dan: should we put a milestone on it?

David: depends on how much other folks on the tag want to weigh in?

Dan: next week?

David: sure.

* [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231)

David: this is bigger than part/theme.

Dan: who can we assign to? Perhaps Travis?

Alex: filed late, I2S going out =(

Alex: reviewed the I2S thread...this is the one where Marcos begged Chrome not to ship. Doesn't have 3 LGTMs, so didn't make 66 branch.

Dan: assign to David for now, maybe Travis can take baton when he's here.  Assign for telecon in 2 weeks.

Alex: re: Tantek's feedback, I would like to make sure that the icon styles line up with what we do in Web Manifests

* [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232)

Dan: I'll triage and do something with it for the 20th.

* [CSS Selectors 4, :focus-visible.](https://github.com/w3ctag/design-reviews/issues/233)

David: I'm happy to take it.

Alex: shipped in Mozilla behind a prefix, right?

David: yep (`:-moz-focusring`), a11y folks asking for it, I think

Assigned to the 20th.

* [Request Formal Review of Vehicle Information Service Specification (VISS) CR](https://github.com/w3ctag/design-reviews/issues/234)

Dan: Hadley?

Hadley: sure.

Alex: going to CR...🤦‍

Moved to the 20th.

* [Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/235)

Alex: there will be an IETF next week.

Dan: should we wait until after that?

Alex: if we think it's important, we might want to say as much going into the IETF.

Dan: I think we're on record saying we support the packaging work...does anyone disagree?

(silence)

Dan: Alex, if your going to be part of that conversation at IETF, it'd be fine for you to say the TAG supports packaging. Related question: does this support re-decentralization? Peer-to-peer or resiliant to centralized outages/blocking/disruptions?

Peter: the ability to sign something and treat it as coming from the original origin is crucial to that. Open question if this is the right way to do it, but we need that capability.

---



