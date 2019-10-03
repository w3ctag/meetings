# TAG Teleconference
##### 02 October 2019

Present: Kenneth, Alice, Peter, David, Tess, Yves, Hadley

Regrets: Sangwhan, Lukasz

---

Agenda:

* [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @hadleybeeman
* [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris
* [File Handling](https://github.com/w3ctag/design-reviews/issues/371) - @alice, @dbaron, @kenchris
* [JS Self-Profiling API](https://github.com/w3ctag/design-reviews/issues/366) - @dbaron, @kenchris
* [how to decide if workers are subresources or separate contexts](https://github.com/w3ctag/design-reviews/issues/310) - @dbaron
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman
* [Reviving the HTML Design Principles](https://github.com/w3ctag/design-reviews/issues/426) - @hober
* Issue Triage

---

## [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris

Ken: Nothing much on our feedback; at TPAC some feedback on security issues...

Tess: I raised this in the web components meeting. 
... import foo from whatever.css. No indication that the author knows that it's CSS, may not be expecting it to execute. Coordination problem as server may decide to serve some JS instead and that may execute.
... Came up in the context of JSON modules. Common to load things cross-origin, eg. a weather widget. Fetch JSON, then parse it, so you know it won't be executed. JSON modules may be immediately executed.
... Server controls what is served, so it's not under the author's control.
... Advocating for a change to import ... some kind of special syntax. That is being pursued.

Ken: Could you add a link to that discussion into our issue?

Tess: I will dig up [the minutes from the web components meeting at TPAC](https://www.w3.org/2019/09/17-components-minutes.html#item18), and the [associated issue](https://github.com/w3c/webcomponents/issues/839) and [PR on HTML removing JSON modules](https://github.com/whatwg/html/pull/4943).

Peter: I see the concerns David raised about ... did we get any feedback on that?

David: No, no feedback on that. Felt a little weird to defer... they were waiting on a decision.

Kenneth: Should also mention that they are changing the name because there is a popular module... will be called CSS Module scripts potentially.

Peter: What should we do on this issue? Wait for things to shake out at ECMAScript? Anything else?

Kenneth: Not much we can do at this point.

Peter: Should we set this to pnding external feedback and come back to it? Ok. Will do.

## [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @hadleybeeman

Tess: Not much has happened on our review. Hadley and I had a breakout on this at our F2F in Tokyo... this was a big topic on Friday at TPAC. Haven't seen the minutes from that; I believe it was an interesting discussion that ran late. I'd like to understand the outcome from that discussion.

... Never had a time to talk to Sam about this... just met him very briefly at lunch in Tokyo.

Hadley: I didn't get a chance to talk to anyone atbout this at TPAC either. Would be useful to find out what happened. This was still going on after I left.

Tess: I will [try to dig up the minutes](https://www.w3.org/mid/m2a7ajlo3f.fsf@toconnor-mb10-1.lan) on this one.

Peter: Shall we bump this by a week?

Tess: A week sounds good.

Peter: Done.

## [File Handling](https://github.com/w3ctag/design-reviews/issues/371) - @alice, @dbaron, @kenchris

Kenneth: Didn't get any feedback on this one either.

David: We might need to open some issues in their github repo, per their request.

All: good point.

David: Some of these are more discussion points than issues, might be hard to frame as issues.

Peter: I'll leave this one as pending feedback for now.

## [JS Self-Profiling API](https://github.com/w3ctag/design-reviews/issues/366) - @dbaron, @kenchris

Kenneth: We gave a lot of comments here but haven't heard back yet.

David: My co-workers had some more feedback, should probably revise my comments.

## [how to decide if workers are subresources or separate contexts](https://github.com/w3ctag/design-reviews/issues/310) - @dbaron

Peter: David, you're the only one on this issue and it's marked as stalled.

David: Anne thinks it can be closed based on that summary... we should probably read that summary. Closing it is likely to be fine.

Peter: ... design principles

David: I think closing this one in favour of the design principles issue makes sense.

Peter: I'll put a note.

## [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman

Hadley: I had another look at this. Looks like dtapuska opened it again... didn't know that was possible. 

Peter: I re-opened it after he asked.

Hadley: Looks like he has taken feedback on board, but hasn't resolved my fundamental issue that the UA doesn't determine the language of the page... 

... User agent is there for the user to express their preference to a website. Breaks that model for the preference to come from the referring website. We already have lots of discussion of this on the issue.

Peter: Ironic that Google.com is notoriously bad at selecting the language for the user when you change locations, on google.com anyway.

Hadley: So what should we do? David?

David: Maybe we should figure out what has changed with the request. I agree with your concern about the outgoing page choosing the language.

Hadley: Let's bump this week.. you're right, we should look at the changes that have been made. We still have the same underlying concern, though, and it doesn't seem to have been addressed.

David: It's not clear what changes have been made; the PR hasn't changed as far as I can tell.

Hadley: Great, we can just ask what has changed.

## [Reviving the HTML Design Principles](https://github.com/w3ctag/design-reviews/issues/426) - @hober

Tess: this was brought up by Anne... suggested that the document be revised and worked on, and thought it might fit with the TAG. Some kind of joint work between TAG and WHATWG, or at least something produced in collaboration to document shared principles.

... I think this is a great idea. Several of the HTML design principles are cited when considering various features for the web. Cited in our own reviews, and in the ethical web principles, specifically priority of consituencies. Makes sense to be a living document, not an ageing note.

... Idea would be to take old ED and revise it as a draft finding, and go from there.

Hadley: Content-wise it seems to have a lot in common with the ethical web principles and TAG Client API design principles... can we find logic to explain why this is different?

... Can imagine later asking why we have all these separate docs.

Tess: Right. These principles were never just about HTML; they happened to be worked on alongside HTML5 but they apply to all web APIs. First thing to change woul dbe the name, to generalise it.

... Would be distinct frmo the two existing documents. Sits next to the ethical web principles; pretty high level.

... Client API design doc gets a lot more specific. Would expect Client API document to reference the other documents.

... ???

Hadley: If the purpose of this doc is to explain the design principles, why not merge them? Also looking at universal access, which we have also covered in the ethical principles, so those are parallel logic with different explanations. 

... In my experience the HTML doc carries a lot of respect, and that is valuable; would love to make the context of everything else we're working on.

(hadley disappears in a puff of smoke)

David: Echoing Hadley's question of whether this needs to be a separate doc...

Kenneth: First we need to have a look to see whether we agree with those principles in the first place.

Peter: Agreed, should make sure there isn't something coming in that's out of date or inaccurate or flat-out wrong...

Alice: Noting that Tess has commented on Baby Steps... what was that referring to?

Tess: .. referring to Anne's comment "add a late proposed addition that never made it in, encouraging folks to start small and evolve features slowly".

Kenneth: Could pick it up at the face to face?

Tess: This would be a valuable use of ...?

.. Like the idea of spending time on longer-term time horizon things rather than just always doing design reviews, so would like to dedicate some time to that.

Yves: We might cherry-pick some items to put in our global design guide, and keep html-specific ones in the HTML specific document.

Peter: Hearing some broad support for this idea... wasn't clear if Tess wanted to start working on it before the face to face, but I would say go ahead.

Tess: agree ... sure.

Alice: And my axe

Peter: Adding Alice to the issue.

## Issue triage.

[Microtransaction payment handlers #422](https://github.com/w3ctag/design-reviews/issues/422)

Peter: This idea keeps coming up every decade or so...

Kenneth: I can be on this but I don't know much about microtransactions.

David: I suppose I should given I've reviewed a lot of the other payment specs, though I will be away the next two weeks.

Peter: Will set a milestone for a month out.

[Proliferation of manifests at W3C #423](https://github.com/w3ctag/design-reviews/issues/423)

Kenneth: I will take a look given I work on some of those manifests...

Peter: Setting a milestone for a couple of weeks out

[Partition the HTTP cache #424](https://github.com/w3ctag/design-reviews/issues/424)

Tess, Yves: 🙋

Peter: Milestone? 

Tess: Couple of weeks sounds fine. Feel free to move it, push it.

[shipping and contact info delegation #425](https://github.com/w3ctag/design-reviews/issues/425)

Kenneth: Also payments.

Peter: Same assignees then? You and David?

Kenneth: [reluctantly] I guess that makes sense.

Kenneth: The last one is modal dialog, apparently also payments.

[Modal window #427](https://github.com/w3ctag/design-reviews/issues/427)

Tess: I'll take that one.

Peter: Milestone: two weeks.





