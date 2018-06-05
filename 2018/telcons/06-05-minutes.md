## TAG Teleconference
##### 05 June 2018

Present: Peter, Kenneth, Dan, Travis, David, Yves, Alex, Lukasz

Regrets: Hadley
Scribe: Travis
---

Agenda:

* [CSS Selectors 4, :focus-visible.](https://github.com/w3ctag/design-reviews/issues/233) - @plinss @dbaron @travisleithead 

Peter: So.... where are we at? Pending external Feedback.

David: waiting for proposed text to make it into the spec. Still hasn't happened yet.

Peter: moving this out a couple of weeks.

Alex: status check: Mozilla says it works, we're fine with it--still the case?

Peter: Yes.

David: Let's loop back--we want to make sure the spec gets an update to be clearer.

Travis: and notify the PR author that we're waiting on it.

Peter: I'll notify.

* [Payment Handler pending external feedback](https://github.com/w3ctag/design-reviews/issues/231) - @slightlyoff @dbaron @hadleybeeman

David: Need to bump out again--till next week?

* [Web Components Guidelines Doc?](https://github.com/w3ctag/design-reviews/issues/227) - @kenchris

Kenneth: Postponed to F2F - agreement in last meeting

Daniel: My bad :-)

* [Permission Delegation In Progress](https://github.com/w3ctag/design-reviews/issues/225) - @dbaron @torgo @lknik

Peter: where did we leave off on this?

Lucasz: I had a look at the issue. Agree with David: sometimes permission are granted indirectly; question of delegation. In my opinion, not really. I'm not sure whether it makes sense to extrapolate the file-picker examples... Not sure about screen capture or others. Should be formulated... 178? No consensus or path to integrate [that]. Do we expect more permissions to be added? Granularity is good. Will permissions need to be asked for with a prompt.

Alex: Yes, we can expect to add lots of new permission types in the future.

Lucasz: it must be extendable. Other devices/subsystems will want to be protected with permissions. Should not be a deal-breaker.

David: I think my issue on the Permissions API is not the central issue. We want to settle on the earlier discussion.

Lucasz: what was the earlier discussion? Delegation?

David: Maybe there's not that much more to do. We disagreed on the question of limiting further delegation (to sub-frames).

Travis: Iframes can work around delegation "further" when permission has been delegated to them.

Lucasz: Can issue call to reconsider the model. I don't think limiting delegations would be actively harmful.

Alex: Seems we are struggling for a capability delegation model. Would be nice to put permissions on delegation.

Lucasz: Not certain whether this would be the right thing to do.

Peter: how to move forward.

Lucasz: we can forbid delegation for delegated iframes.

Alex: Don't think that will be effective.

David: sub-frames can invoke the API that invoke permissions. Some folks want that to go away, and associate all the prompts with top-level page. That's part of the motivation for this issue.

Alex: so it's also a question of what capabilities would be removed.

Travis: I'm pro-prompts being associated with top-level origins (solves a lot of potential security concerns). Not sure we have a good delegation model in place yet.

Peter: How to move this forward?

Travis: Can we ask for the folks responsible to consider a capabilities model; since we're not enamoured with the existing delegation model.

Alex: To David--what would help asuage your opinion.

David: subsequently limiting iframes (preventing iframe creation). Permission delegation gives folks an easy path to fix (with this API). With iframe restrictions, it causes a bigger refactoring to take place to accomplish the goal. If Chrome want's to try, it seems reasonable.

Alex: Other Mozilla opinions?

Travis: is the capabilities model change too much to ask?

Alex: Yes. We can't even make certain progress on other permissions issues. In interest of moving forward (don't want to hold things up). If we can see a better path forward, we'd suggest it. I can draft something and propose it to the group on Slack.

Lukasz: would be great.


* [ReportingObserver pending external feedback](https://github.com/w3ctag/design-reviews/issues/195) - @cynthia @slightlyoff

Alex: This is the one with structured values. Mnot had feedback. It was in JSON, MNot had alternate structured value proposal--that kinda killed the momentum.

Peter: How do we unblock this? Alex, you were

Alex: some background--this was the author's first go-round on this Intent. Has now transitioned to a new owner in Chromium, who is going to try and drive this forward. Looking for guideance on how to do the structured header. (Reporting observer is one, accept-ch is another (server timing is a third.)) We will be setting some precident. Server signing was a one-off. If we give a thumbs-up on JSON, we at least know all its badness. We can go with IETF's structured headers proposal, or we can say we don't have an opinion.

Travis: Notes limitation on structured headers (can't seem to have nested types). Are they going to be generally suitable for purpose? Might want to get some more info about their intent, and whether it would make a good (general) recommendation? Should we review structured headers before deciding on this issue?

(connection problems)

Alex: I'd like for us to make progress.

Travis: I want to have a more-informed opinion before deciding.

Alex: This would be precedent-setting for Structured headers too. We get to recommend a way forward.

Kenneth: link to structured headers: https://github.com/httpwg/wiki/wiki/Structured-Headers
https://httpwg.org/http-extensions/draft-ietf-httpbis-header-structure.html

Kenneth: Chrome is using for Web Packaging

Alex: I can get Jeff a chance to tell us why he's using it (why he chose it). We can circle back next week to hear from Jeff?

Kenneth: Agreement

* [LIFECYCLE API](https://github.com/w3ctag/design-reviews/issues/283)

Alex: folks want to have this API sooner (than later)--to support an intervention support. This is the beginning of an effort to end up with... You told me you were going to kill this page on my document, but I probably want to hear that in my Service Worker where I have more context. The ServiceWorker manages state for the app, and might be a better spot for this.

Kenneth: I can add some additional feedback on the issue.

Alex: We'd like to note that we want to be notified as this feature continues to roll-out.

Addendum: [HTML 5.3 Review Request?](https://github.com/w3ctag/design-reviews/issues/275)

Travis: Left a note on Slack--Leonie asking about whether we will provide any feedback.

Dan: Spoke with Leonie--told her we were focused on the whole spec (not just parts). 

Alex: I'd like to let them know that if they have specific topics they'd like to get in front of the TAG, this is their opportunity.

Travis: We need to write our feedback into 275. I can do that after checking with Sangwhan.

--Adjourned--

The following were not discussed due to time:

* [`sec-metadata`](https://github.com/w3ctag/design-reviews/issues/280) - @dbaron, @lknik

Lukasz: relevant (https://lists.w3.org/Archives/Public/public-webappsec/2018May/0015.html)

Lukasz: Case in point (From-Origin; WebKit) https://github.com/whatwg/fetch/issues/687

* [TV-Specific Web Subsetting](https://github.com/w3ctag/design-reviews/issues/105) - @torgo

---



