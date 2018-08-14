## TAG Teleconference
##### 14 August 2018

Present: Dan, Hadley, Lukasz, David, Peter

Regrets: Travis, Yves, Kenneth

---

Agenda:

### Proposed TAG role in W3C-WHATWG relationship - Dan

#### Proposed Conflict Resolution Paragraphs

>The Cooperation Process above addresses the common case, in which the WHATWG Review Draft meets W3C REC criteria and there are no objections. But we propose an exception process to deal with conflicts and lack of agreement.
>
>If there are features that were marked “at-risk” by the W3C because they don’t have multiple implementer support, the HTML working group will file those as issues with the Steering Group for clarification.
>
>When there is an unresolved objection, due to the large cost of having normative differences between the W3C REC and the WHATWG Review Draft, we all make substantial effort to resolve the conflict so that W3C can publish a REC with zero normative differences from the WHATWG Review Draft. If the HTML WG has no consensus to bring the document forward on the REC track, it must ensure that an issue is raised or encourage the editor to re-open issues in the WHATWG GitHub repository.
>
>Conflict-resolution procedure:
>
>* The HTML WG tries to resolve the objection, working to elucidate [concern with use of this word - hadley] the concern to the WHATWG editors and other Workstream participants (through their GitHub repository) and to explain the decision of the WHATWG to those raising the concerns; if this does not achieve consensus then
>
>* The HTML WG escalates the disagreement to the WHATWG Steering Group to help resolve the issue; if this does not achieve consensus then
>
>* The HTML WG explores techniques other than having a spec with normative differences such as an extension spec; or as non-normative advice; if this does not achieve consensus then
>
>* The HTML WG, WHATWG Steering Group, an individual objector, or W3C Groups with dependencies on WHATWG specifications, including horizontal review responsibilities, may request technical counsel from the TAG. The TAG may be able to find some consensus or explain to one side or the other any negative impacts of their position; [*suggested addition:* The TAG may consult other experts if they require some expertise not currently available on the TAG; ] if this does not achieve consensus then 
>
>* The issue goes to the Director, who examines the arguments using the record of the tracked issue, the WG analysis, and the TAG analysis. If the Director overrules the objections of the HTML WG then W3C publishes the Review Draft as a REC.
>
>* If the Director sustains the objection, the Director and/or the TAG may choose to re-open the appeal to the WHATWG Steering Group with any new data or rationale; if this does not achieve consensus then
>
>The W3C may choose to a) decline to endorse a particular Review Draft as a Recommendation and continue the discussion for the next Review Draft; b) if the differences are not too entangled with the rest of the spec, the REC might be issued as the Review Draft plus a companion document; c) If W3C management and the WHATWG Steering Group cannot reach agreement on a single standard through direct negotiations, W3C may (under the CC-BY copyright) publish a Recommendation with differences, and WHATWG may terminate this agreement.

Hadley: last para section c: does that mean both have to happen?  

David: i think that's whats intended 

Dan: this is the nuclear option

Dan : are we OK ?

Alex: this would not pass a plain language contract test. -  how does this happen?

David: the intent is that the work happens upstream at whatwg - but that htere will be [w3c facilitation....]

[consensus yes - though our feedback is that the text itself is unnecisarilly complex]

### Proposed workflow for privacy & security questionnaire - Lukasz

Plan? 

1. Merge Lukasz's changes asap, write issues close to some
2. ask PING and possibly merge ASAP
3. Wait for PING feedback/edits
4. If done by 10 September or so - TPAC preso possible


Dan: We need to jointly edit the document with the Privacy Interest Group.  However, I think we need to review it every so often in the TAG and approve any changes or inputs that PING makes.  We should be accepting of changes but making sure they work for spec developers who use the questionnaire.  Best to do through Github, but don't think we need to force PING to make Pull Requests.  What do you think?

Hadley: My understanding is that PING has forked the document, so there's stuff that we need to review.  And they're talking now about making more changes over the next 5 weeks.

Dan: And we need to fold Lukasz's changes into their version so we have a single version.  If we've diverged really far, then we may need some working sessions between us and them to try to try to fold those parts together.

Hadley: I like that as a way to proceed.

Lukasz: Tentative plans should be to preferably ... make changes as soon as possible.  Issues combining some pulls, descriptions I will provide.   Then give heads up to Jason Novak and PING, and I will be quite prepared to merge my changes soon.  If I'm supposed to present at TPAC, should be stable by mid September.

Dan: Do the work now, see where we are in September and then make decision about whether to present at TPAC.

Lukasz: Want to get my stuff out of Google Docs ASAP, then I review my proposed edits and their proposed edits.  Advantage of including changes soon, and maybe forking, is that PING could view the two documents and adapt their changes.  Maybe a fork that is a completely new document.

Hadley: I'm concerned that if we present PING with a separate document and they've put work into refining current document, they'll feel we pulled rug out from under them.

Lukasz: I think it will be ??? for PING to review our proposed changes in advance.

Hadley: Advantage of PRs in github is that people can talk about each change separately and discuss each one.

Dan: I think I agree that doing a set of PRs against the current document, even if we have write permission, that we can then discuss in each PR, would make a lot of sense.

Dan: But if it's completely reorganizing the document, it's more difficult to do that wa.

Hadley: It's hard because it's not just our document; it's a collaboration.

Lukasz: I'd favor some initiative spearheading ...

Dan: Absolutely.

Lukasz: ... providing some comprehensive changes to what we already have.

Dan: Doing that by pull request would probably be the best way to do that.

Lukasz: Should I wait for you?

Hadley: It sounds like you want to make a series of changes, and it will be easier to discuss them separately.

Lukasz: By sections... per question.  So about 20-something pulls.  If each pull needs a separate issue, that's a lot of writing.

Dan: The issues are automatically generated when you make the pull request.  I'd be happy to do some of the work.  Hadley, you said you had some time next week, although nextweek is bad for me; maybe I could help after the 23rd.

Dan: I think best option is for Lukasz to start plotting out the pull requests, and Hadley can help review next week.

Hadley: late on Monday

Dan: And we can discuss on next week's call.

Hadley: Can 3 of us discuss on Thursday the 23rd?  Afternoon?  3pm UK time on the 23rd?

Dan: Lukasz, what other time would you suggest?


* [queueMicrotask](https://github.com/w3ctag/design-reviews/issues/294) - @dbaron @travisleithead
* [Page Lifecycle for system initiated Discarding & Freezing](https://github.com/w3ctag/design-reviews/issues/283) - @kenchris
* [CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - @dbaron @travisleithead @plinss
* [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - @slightlyoff @dbaron @hadleybeeman

David:R I met with Rouslan few weeks ago - talked about it ... I don't have a good sense of when we want to close these issues.

Dan: Can we close it?

David: probably fine at ths point.

Hadley: We don't have in our template "has this shipped"... 

Alex: I would suppor tthtat change.

Hadley: we could close it and ask them to inform us if they have problems.

Alex: few things raised here- 

[consensus to close and ask them to come back to use when they have something new]

* [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223) - @dbaron

David: bit thorny issue - we could just close it.

Hadley: we won't do anything about it?

David: it's open in their repo and they need to define stuff [do work]

Dan: I'm happy to close it based on that feedback.

[consensus to close]

### AOB

Other thing we should look at: https://github.com/mikewest/http-state-tokens

Alex: is every resource allowed to set a header like this?

Hadley: i'd be very in favour of restricting it to top level documents - off the top of my head

Alex: igimages that can set cookies is somethng used in advertising



F2F Backlog
* [CSP feature 'unsafe-hashes'](https://github.com/w3ctag/design-reviews/issues/291) - @cynthia @dbaron @travisleithead
* [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288) - @slightlyoff @dbaron @travisleithead
* [HTML General Review: Custom Elements](https://github.com/w3ctag/design-reviews/issues/244) - @torgo @kenchris @travisleithead @plinss
* [Deprecating nonsecure cookie delivery](https://github.com/w3ctag/design-reviews/issues/239) - ??
* [DOM](https://github.com/w3ctag/design-reviews/issues/229) - @cynthia @dbaron @travisleithead
* [Web Components Guidelines Doc](https://github.com/w3ctag/design-reviews/issues/227) - @kenchris @travisleithead @plinss
* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff @dbaron
* [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @travisleithead



---



