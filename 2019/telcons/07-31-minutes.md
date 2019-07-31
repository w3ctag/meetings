## TAG Teleconference
##### 31 July 2019

Present: Lukasz, Peter, Alice, Kenneth, David, Tess, Sangwhan, Hadley

Regrets: Dan, Yves

Scribe: David

---

Agenda:

* [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392) - @hober, @alice, @dbaron
* [Native File System API](https://github.com/w3ctag/design-reviews/issues/390) - @cynthia, @kenchris, @lknik
* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [JavaScript Memory API](https://github.com/w3ctag/design-reviews/issues/386) - @cynthia, @kenchris
* [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @hober, @alice, @kenchris

Triage:

* [WebRTC-SVC](https://github.com/w3ctag/design-reviews/issues/396)
* [Same-Origin iframe document-access limiting Feature Policy ](https://github.com/w3ctag/design-reviews/issues/397)

---


### [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392)

Alice: we were waiting for... (goes through comments and summarizes them)

David: the two hash thing may actually be interesting architecturally; part of the URL that the page doesn't have access to

Peter: there's a lot of work that's been done with media fragments; seems like this should be compatible with that

Peter: I remember Doug Schepers talking about an annotation system.

Tess: There was a whole effort -- workshop, community group of some kind, which may still exist.  Artefacts are still out there.  I want to say the folks working on scroll to text have already looked at that; at least I remember offhand seeing they'd already seen that.

Peter: how to proceed?

Tess: Two things important: (1) adding something to URL not visible to page; media fragments didn't do that.  They came up with a different syntax that is page visible.  What's important about hiding from the page?

Alice: why hidden from the page?  I recall seeing, but forgot.

Peter: I see concerns about pages that already use fragment ids for keeping navigation state, and they're worried about conflicting with that.

Tess: why more of a problem in this case than for media?

David: because it's a user feature?  Users invoke new feature that the page doesn't expect, want to share URLs?

Alice: Explanation in https://github.com/WICG/ScrollToTextFragment/issues/15#issuecomment-506347279 .   Concern about apps doing their own hash parsing.  Also causes the text search part to not appear in the URL, so it would be an odd transient thing.  So tradeoff between backwards compatibility for sites that do their own hash parsing, versus not changing the URL and consistency with media fragments etc.

Peter: Bigger than just consistency, adding a new delimiter to URLs.  Big new feature.  Something we should look at.

Alice: When would there be an actual conflict between -- when would you link to a fragment in a single page app?

David: I've seen examples... like cryptpad.

Sangwhan: Youtube for TVs.

David: Map examples -- do this with hash, not great example for text search.

Peter: How will these URL be minted?  From user doing text search in browser?  Or something page will generate?

Hadley: If the page generates it on its own, isn't it then pretty close to how anchors already work.  Looking at search use case, thinking of something like schema.org -- pages provide some semantic context, but heavy lifting done by crawler/indexer.

Peter: Search engine use case would definitely be the url being minted by something outside the page.

Peter: sounds like we have some issues to raise -- someone want to write them up?

Hadley: One more issue: internationalization.  In security section, potential threat is exfiltrating data from destination site.  One proposed mitigation to say it only matches on word boundaries.  Not all languages have visible word boundaries -- cites UAX 29 supplemeted by word dictionary, as done by ICU project's boundary analysis.

Peter: Thai example requiring dictionary; CSS doesn't have concept of word.

Tess: On the one hand, ICU is widely used in browser engines... though should we have specs that require a specific library, or should we have a spec for this so that we're not just depending on ICU.  So we could reference a spec rather than an ICU behavior.

Peter: Somebody want to write this up?

Alice: I can try.

Peter: Bump issue a few weeks?

### [Native File System API](https://github.com/w3ctag/design-reviews/issues/390)

Kenneth: Apart from contentious parts, API seems nice.  Filed a few issues; haven't gotten response yet.  Spec seems early, they want an origin trial soon.  Spec just has API, not a whole lot of other info there.

Sangwhan: The API itself is fine -- the "just a javascript API".  I'm not entirely convinced about the mitigations that are in place to prevent terrible things happening to your home directory.  The `getDirectory` method seems (missed).

Sangwhan: API surfce seems fine.  Alternative proposal from another chromium person that might change it a bit; seems like improvement, but not that significant a change.

Sangwhan: alternative is what Kenneth linked to: https://github.com/WICG/native-file-system/issues/19#issuecomment-490579093

Lukasz: Questions as well about aspects in security & privacy quesstionnaire.  Would be nice if they clarify.  They say they encourage UAs to protect access to file based sensors, i.e. special files like /dev/something, but little clear on that.  They also say API will behave differently in PWAs.  I my view this is probably among the first such approaches, if not the first. Would be reasonable to  have a close look at that.  We did not receive feedback, bump?

Alice: They also requested github issues in their repo; they might not be tracking comments in our issue.

Hadley: Naive question:  why is this useful to take out of the UA and status quo for the way things are done and put into this set of defined APIs?  That is, what's the benefit of standardizing this rather than having the UA handle things as done now.

Sangwhan: Not there now.

Kenneth: Today you can get a handle in indexed db.  Today you can't build something like Visual Studio code on the web.

Sangwhan: Supposyou wanted build a web app that handled a 100mb file-- can't do incremental updates today.

Alice: Somebody file an issue on their repo to sugest adding those examples directly to their explainer (multi-file editor, large file)

Sangwhan: It's there (multi-file editor), in the goals section.

Alice: large file isn't.

Alice: And seems like the words could be fleshed out a bit.

Hadley: I don't see a use case described in this explainer; it's a bunch of functionality.  Not written to say what the problem for the user is.

Lukasz: persistent access to filesystem -- user gives permission for persistent access to directory.  Visits site again, no permission prompt.  Streamlining access to the file system.  Yes, possible Privacy issue.   How to mark that this kind of access is actually being retained?

Peter: That you can send a handle through `postMessage` also scares me.

Kenneth: only on same origin, right?

Peter: checking

Kenneth: Other point, could only access handles in specific cases.  Not really writtten here, but was told that's the idea.

Sangwhan: One question I did have:  any way to do equivalent of `mmap` -- I think the answer is no.

Kenneth: file an issue?

Sangwhan: So what do we think about this?

Hadley: At a bare minimum would like the explainer to explain use cases more.

Lukasz: `mmap` would also access `/dev/` filesystem?

Sangwhan: `/dev/` filesystem is out of scope... says so in the spec... or maybe the explainer?

Lukasz: I asked them in the this ... not really clarified.

Sangwhan: I think "encouraged" is too weak.  I'm also uncomfortable going to a point outside of your home directory -- should be as restrictive as possible.

Lukasz: Not only too weak, but also not being written anywhere. Even that would be scary.

Kenneth: Lukasz, could you file your issue on the repo?

Lukasz: I ??? my question but received no response.

Kenneth: Yes, but you should file it in their issue tracker.

Lukasz: ??? these kinds of answers in their issue tracker.

Sangwhan: I put it in there.

Kenneth: Add "in response to" so we get a link back?

Sangwhan: done

Peter: more to discuss with this issue?

Hadley: I'm opening an issue on their repo about the explainer.

Kenneth: I already did.

David: Are browsers going to be willing to ship this given security risks?

Sangwhan: Should it be PWA-only?

Kenneth: Get a modernized API if not a PWA -- but can't store handles in IndexedDB.  How it's going to be implemented in Edge and Chromium.

Kenneth: The other thing, not implementing this all at once in Chrome, staged rollout.  Would be nice to know what's in what stages, and what we should be concentrating on.

Sangwhan: I'm also concerned about exclusive access -- multiple tabs operating on the same file at once.

Kenneth: Have ??? about that.  They're copying files unless you set specific markers "in place" etc.

Sangwhan: Does "in place" twice reject, lock, etc.?

Kenneth: How does that interact with native apps doing the same?

Sangwhan: Can use OS-level functionality.

Kenneth: file an issue.

Sangwhan: Did you already file it?

Peter: What to do with the issue?  Pending feedback at this point?  Kick it out a few weeks?

Kenneth: seems to be moving slowly.

Sangwhan: 3 weeks?

Kenneth: TPAC?

Sangwhan: Haven't followed up on issues they've filed themselves.  Downprioritized?  Vacation?

Peter: 4 weeks then?

### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389)

David: was supposed to schedule a breakout for this... for next week.

Peter: OK, bump this 2 weeks.

### [Badging API](https://github.com/w3ctag/design-reviews/issues/387)

Alice: Checking if they've updated their explainer.

Alice: One of the main sticking points was the difference between badging for a page and badging for an origin.  I asked them to give some examples of each.  They explicitly want this to be badging for an origin, since it's about badging an installed web application.

Alice: They had a PR...

Alice: reads from something -- (1) and (2) but not (3)
https://github.com/WICG/badging/blob/master/explainer.md#What-to-Badge

Alice: If you have a github issue, you'd be able to badge whether or not the PR has been approved since that state is specific to a URL.  If you have comments that have come in, the per-document case.

David: ???

Alice: distinction between any tab at that URL, versus the state of that particular tab even if multiple tabs at the same URL

Alice: That doesn't rule out badging a tab, but I understand they don't intend to flesh out the tab case anytime soon.

Alice: ? about scope.  Maybe something for me, Tess, and David to discuss as well.

Peter: next week?

Alice: sure

### [JavaScript Memory API](https://github.com/w3ctag/design-reviews/issues/386)

Kenneth: only have an explainer so far, haven't looked in detail.

Sangwhan: likewise

Peter: push out 1? 2? 3? weeks

Peter: ok, next week

### [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385)

Alice: interested in what you all think

David: still a bunch of namespace discussion in TC39

Hadley: Am I misreading gary greene's responses?  Kenneth wrote up a11y concerns.  Gary came and says he sees other concerns?  Oh... not part of team working on this?

Hadley: So have we seen response from people working on this?

Alice: A little overwhelmed, they have been active in their own repo; our issue thread got pretty noisy.

Kenneth: blink-dev too.

Hadley: what's the best way to get responses to the questions we asked in our issue?

Alice: raises question about our process -- sometimes it's helpful having external people comment on these issues, but sometimes gets very noisy.  Becomes difficult for someone to follow the conversation.  Doesn't look like we've heard back from them on this issue since we last talked over a month ago.

Alice: a11y issues are going to be difficult to overcome, I think.  I'm not convinced it's not a pattern that's inaccessible by design.  Do we standardize such a thing, just because we think we can do a better job of a11y than the 50 libraries doing it?  Is it a net win, or does it not meet the bar?

Peter: there's the argument that we can get it in front of the right people to get an answer to the a11y argument.

David: common tradeoff with adding features - adding a feature that has negatives for the user increases the use of that feature (negative) but does it in a less bad way than how developers were doing it before (positive)

Peter: push down a week or two?

Alice: would be good to have a longer discussion; a lot to unpack.

Peter: ok, next week then.




