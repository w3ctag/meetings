## TAG Teleconference
##### 06 March 2018

Present: Dan, Peter, David, Alex, Hadley, Travis

Regrets: Lukasz, Andrew, Sangwhan

---

Agenda:

## Teleconference time starting next week

David: Daylight saving time coming up! Maybe next week swap to new schedule:
8am CA / midnight TOK.

Dan: Slightly leaning toward going back to regular call schedule (though existing rotating schedule hasn't been too bad).

David: If we start that next week, Europe will be an hour earlier for two week (then return to regular time.)

## [Sensor APIs](https://github.com/w3ctag/design-reviews/issues/207) - Sangwhan
## [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - Alex, David

David: Wanted to follow-up on an rather involved issue--but haven't followed up yet.

Alex: fine with kicking down the road.

Peter: how long?

David: perhaps move to the F2F.

## [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223) - David

David: I have reviewed some of this (about half the spec). It's a pretty big spec--attempt to replace CSSOM with something we like better. Some other Mozilla folks have also reviewed due to vendor opinion requests... A couple of issues seemed to rise to the top:
1. Reason was for better performance/ergo for CSS manipulation than working with strings. Wins on ergonomics, but not winning on perf by the evidence.
2. Spec is not yet solid-enough to lead to two interoperable implementations.
3. Few other things maybe not worth discussing.

Alex: we left a lot of feedback from our last F2F... Have recieved some responses already. HAve you processed these?

David: Some were design issues... 23-30 issues + Anne/Boris a similar amount. Spec has had huge changes since the F2F--probably Tab's full-time effort.

Issue: Lots of undefined--what's the underlying model, how is it defined. Spec defines the object model API, but not the model that is being defined. Doesn't say what happens to the model when you change things.

Alex: To a certain extend, browsers don't open up their CSS...

David: More like... complex properties (like transform) have parts, what's the model for how the underlying model for the transform is manipulated, and how the string version is affected, etc.

Alex: We've seen that ambiguity in other parts of the DOM (Attributes/properties). Interop testing has ironed this out... Perhaps implementations have to figure out how that works themselves?

David: Some needs to be fixed in Typed OM, others may need to be distributed to other specs where applicable. Probably other parts need to be defined in CSSOM where serialization is defiend. There's an existing mess, we dont' want to add to the mess without making it better.

Alex: I'm concerned about holding this up for some undetermined long time. I'm also concerned about the lack of definition of a model.

Travis: We should be sure there is clear application of a model.

David: If Chrome implements out ahead, we could get stuck with Chrome's interpretation of 

Hadley: Perhaps "OM" is not reflecting the nature of the spec very well... add "API" suffix?

Alex: Worried that Anne's concern is theoretical... 

Peter: looks like there are actual side-effects.

Alex: Think we should get to resolutions by writing tests.

Peter: any given property needs to have definition of how they are represented in the object model... we do not want to hold up the rest of this spec until that happens.

Alex: Do we need to channel this feedback to the CSS WG?

Peter: there was a question about needing Proxies to effect this (as it may be slow).

Alex: Chrome doesn't use a proxy.

Peter: Houdini meeting coming up. We can relay the feedback about seeing a consistent OM defined for what parts get set when properties (parts of properties) are changed. David?

David: Nothing else I want to raise here; brought some other issues up to the CSS WG as a whole. Should I write-up the feedback?

Peter: I can do it.

(Note that https://github.com/w3c/css-houdini-drafts/issues/718 may also cover some of this.)

## [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - David

David: Was pending-external-feedback from London F2f.. some discussion since then. M's comment did respond to Alex's question.

Dan: Noted the Twitter uses is... has there been feedback.

Alex: Yes they want it yesterday, but they want it to share photos--which it doesn't do today. Leads back to a service-worker style event.

Peter: I share concerns about shipping something that doesn't fill all the user-cases. But changing to a new URL template syntax annoys me as well. Is there a path forward to engage here?

Alex: think we need to invite **@mgiuca** to a call. David can you meet with Matt? We can have a direct communication about this.

David: yes, but Alex should be there too--it's your Service Worker idea.

## [Img decoding attribute](https://github.com/w3ctag/design-reviews/issues/220) - David, Sangwhan

Travis: we hit deadlock on this right?

Dan: might wait until Sangwhan is back?

Peter: kick it to next week.

## [Web Locks API](https://github.com/w3ctag/design-reviews/issues/217) - Andrew, David

David: still looks to be pending external feedback. 

Alex: Josh mentioned that he's making some progress on this...

Will come back to this at the face-to-face.

## [Accept-CH header](https://github.com/w3ctag/design-reviews/issues/206) - Andrew, Alex

Peter: Google was going to go talk to some people...

Alex: I did. I now understand that the reason the hints are not being sent on the initial nav is that some folks who represent the net team are resistent to sending this data. (For reasons not privacy related.) These folks haven't seen the compelling argument yet... Concerns about size (how much can afford to send). Pretty extrodinarily that this will be resolved soon. Plan is to show effectivness on sub-resources first, then use that data to convince the team to put it on the initial request. Politics. We shold note in our review that the inital request should send the data and inquire who can take the feedback.

Peter: Andrew had some strong feedback--please sync with him first.

## [ResizeObserver](https://github.com/w3ctag/design-reviews/issues/187) - Alex, David

Peter: Had some feedback about adding yet another 'single box' idea to the platform, not accounting for fragmentation; there was some pushback on implementation constraints.

Hadley: Also Alex noted timing of feedback--is it too late for feedback?

Peter: Only in Chrome?

Alex: TAG design review is not moved to early in the design process (Intent to Implement).

Peter: TSLC<1wk (time since last comment), move out and revisit?

Peter: 2 weeks out.

## [HTML General Review](https://github.com/w3ctag/design-reviews/issues/174) - Alex, David, Hadley, Sangwhan, Travis

Travis: Started looking into what a breakout would be, but didn't get far.

Alex: How do we structure this to come away with a lot of progress?

Travis: Perhaps divide-and-conquer? Assign homework? Maybe work to a goal?

Dan: We could use a checklist? What could we do while at the face-to-face? Create some sort of document to split things up? One thing we keep talking about is how big of a rock this is--and need to de-compose the problem. We can break-up the one issue into smaller issues.

Travis: Yes, and I can have next steps ready for next week.

## [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101) - Hadley, Lukasz

Hadley: not too much progress. Lukasz put a draft of our conversation together. Covers the variety of privacy modes and notes the diversity involved. Have some feedback that I'd like to generate for the doc and can relay to Lukasz.

Dan: I'd love to help; let's get together and provide the feedback jointly; can return to the group with an updated document.

Peter: will revisit in a few weeks.

## ["With Credentials"](https://github.com/w3ctag/design-reviews/issues/76) - David

Dan: can we close it?

Alex: Can you say "please fetch, if you can do it, just do it".

Travis: We still believe there's an issue to be addressed :) So much for Tim's on Sabattical, close the issue...

Peter: Come back to it in... 2 weeks?

## Election and candidates for TAG seats

* [Candidates](https://www.w3.org/2018/03/05-tag-nominations) are: Andrew Betts, Tess O'Connor, Kenneth Christensen
* May the odds be ever in their favor

Dan: we should encourage all AC reps to get out the vote! Ridiculous how few AC reps voted in the last election.

## Call it a day

Backlog:

* [Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/226) - Sangwhan
* [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Alex / Hadley / Travis / Peter
* [OffscreenCanvas](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / David / Travis
* [Review Accessibility Object Model ](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / Travis
* [Secure Contexts & TC39](https://github.com/w3ctag/design-principles/pull/75) - Sangwhan
* [&lt;link&gt; rel=modulepreload](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/213) - Andrew
* [Decentralized Identifiers](https://github.com/w3ctag/design-reviews/issues/216) - Hadley
* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) - Hadley, Travis
* [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David
* [import.meta.url and import.meta](https://github.com/w3ctag/design-reviews/issues/208) - Alex


---



