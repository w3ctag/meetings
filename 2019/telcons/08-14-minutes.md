## TAG Teleconference
##### 14 August 2019

Present: Peter, Tess, David, Alice, Dan

Regrets: Kenneth, Sangwhan, Hadley, Yves

---

Agenda:

From last week:
* [SMS Receiver API](https://github.com/w3ctag/design-reviews/issues/391) - @hober, @dbaron, @torgo, @lknik
* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [JavaScript Memory API](https://github.com/w3ctag/design-reviews/issues/386) - @cynthia, @kenchris
* [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @hober, @alice, @kenchris

This week:
* [Review request: DOM Standard Review Draft](https://github.com/w3ctag/design-reviews/issues/404) - @hober
* [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @torgo
* [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393) - @alice, @dbaron, @lknik
* [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392) - @hober, @alice, @dbaron
* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [Web Authentication Feature Detection](https://github.com/w3ctag/design-reviews/issues/383) - @dbaron, @torgo, @hadleybeeman
* [Web of Things (WoT) Thing Description](https://github.com/w3ctag/design-reviews/issues/357) - @torgo
* [Web of Things (WoT) Architecture](https://github.com/w3ctag/design-reviews/issues/355) - @torgo


---
### Web of Things ([Thing Description](https://github.com/w3ctag/design-reviews/issues/357), [Architecture](https://github.com/w3ctag/design-reviews/issues/355))

Dan: We had a call last week, Dan, David, Kenneth, Yves, Hadley?, and Web of Things folks.  They were under misimpression that we were going to do a security and privacy review for them.  They took our feedback on explainer (being more user-centric, being for consumption of broader audience than the TAG).

Dan: Discussed JSON-LD issue; David said he'd provide some additional explanation.

David: I did [that](https://github.com/w3c/wot-architecture/issues/371#issuecomment-519707518).

Dan: Other issue was about privacy and security self-review.  Weren't actions out of that.

Dan: Other thing underlying discussion was the sense that they needed TAG blessing to move forward; I said it doesn't work like that.

Dan: My sense: we should monitor responses to things like David's comment, and then close these issues fairly quickly.  Reaching the limit of return on investment on this issue.

David: Seems reasonable.

### [SMS Receiver API](https://github.com/w3ctag/design-reviews/issues/391)

David: Didn't get to this in breakout, should schedule one for this week.

### [Badging API](https://github.com/w3ctag/design-reviews/issues/387)

Alice: Breakout last week.  This has gotten into an interestesting state.  Marcos has been (reasonably) insisting on having some Tab badging.  If something is a PWA it must work in a load-from-URL-in-a-tab context as well.  It would be great if you didn't have to know which context you're in and badge tab with classic favicon/title munging.  That's quite sensible.  This kind of goes outside scope of what API authors originally intended.  They've been trying to figure that out.  And trying to figure out the difference between what is a "installed web app" and what's a page in a tab, and what the differences in the API surfaces in those cases.  So they went in a direction of being able to set a badge on a Scope (a URL).  Matt has been working on explainer to clarify a lot of these things.  Matt was working on it originally, then others for  bit, now Matt is back.  To accomodate this in the API you can set the badge for a particular scope.  This allows different tabs on the same origin to have different badges, for a start.

Alice: Tess raised the question... I brought up that Chrome may not immeditaley implement the UI side of this.  Tess raised the question of progressive enhancement.  No way to know, if you set the badge on a scope, whether that's worked.

Dan: Leave that up to a polyfill?

Alice: You could use the genuine badging API, and it may not set the tab badge.  It may only set the PWA badge.  If support for badging tabs not yet implemented.

Alice: API doesn't rule it out, but may not ship it all at once.

Dan: But API editors have listened to marcos's feedback.

Alice: yes

Dan: As someone with interest in PWA story, I tend to agree with that reasoning.  Shouldn't be a depnedency on installation.  Has there been discussion of dependency on manifest?

Alice: We discussed that a bit in breakout -- think it was a misunderstanding.  I don't believe it does depend on a manifest.

Dan: It strikes me that mention of scoping it at a certain URL -- manifest also defines that scope.

Dan: PWA in manifest - could say, should sit in a tab, not full screen.  Appears to be a little redundant to have another way of setting scope, when you already have manifests that set scope.

Alice: Badge is associated with a scope, not setting a scope.

David: also service workers have a scope

Alice: Note in the explianer -- scope may need to be in its own spec since referenced by service workers, app manifests, and badging.

Dan: What is a scope?  Slightly more than an origin?

Alice: Seems to be a URL.

Alice: In the explainer: https://github.com/WICG/badging/blob/master/explainer.md#badging-for-multiple-apps-on-the-same-origin-as-in-the-case-of-multiple-github-pages-pwas

Dan: I wonder if we should add something about scope to the design principles.

Alice: I wonder.

Dan: Sounds like going in a positive direction.

Alice: Yes, I think it is.  Helps that I've been able to have multiple in-person conversations with Matt and others.

Alice: To finish up the fallback thing -- Matt put the last comment on, and suggested that it needs some indication as a developer of whether `Badge.set()` worked, so you can do a fallback action.  Not sure if that's in the explainer yet.

Dan: Does TAG need to continue to engage, or are we done?

Alice: Are we happy with `set` for a scope?

Tess: I think so.

Alice: So basically LGTM with a way to check that the badging API has worked.

Tess: I'm glad Matt agrees about ?? to effectively use this API.

Dan: So I think we should leave that feedback on our issue-- what Alice just said.  And thank and close the issue from our side.

Alice to do that.

### [JavaScript Memory API](https://github.com/w3ctag/design-reviews/issues/386)

Postpone to next week.

### [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385)

Alice: Feels like there's a lot to unpack; not sure where to start.

Alice: For sure there's the namespace issue.  There's the naming issue.  There's the import thing -- importing a module in `std` namespace -- discussed elsewhere on builtin modules -- has that come to the TAG?

Alice: The link text says "builtin module" under proposed API.

Alice: There's pay-for-what-you-use HTML elements, related to builtin modules.

Alice: There's the question (dearest to me) about the process for adding a new HTML element with UI implications.  How do we think this should work?  What are the requirements?

Alice: Then you get into specifics of design of this specific element and the design pattern.

Dan: Where has the conversation gone on this specific element, since June?

Alice: There's a document -- let me check.  They've been working on accessibility.  Adding a `type` attribute to the element, implies the default style and ARIA role.

Dan: A lot of emotive language in this thread...

Dan: Can we de-link the meta issues you described, e.g., adding UI elements to HTML.  We previously had discussion about badging.  That's not HTML, but another rather similar (in concept) to what we're talking about here.  Something that alerts the user to something that's happening.  What is the difference in terms of how easily that discussion seems to be going versus the `toast` discussion?

Alice: Also an interesting question.

Dan: Scope of it?  For badging we're talking about very specific API.  Maybe has a smaller community of practice around it.  Once we start talking about HTML it's the entire WHATWG community of practice.  All the people who are engaged in it -- all the stakeholders.  Group of stakeholders is bigger.

Tess (writing, audio problems): (trying to paraphrase something IIRC dbaron said the last time we talked about std-toast) it makes me nervous that this proposal is built on top of so many other proposals that also haven’t shipped in multiple browsers / been around for a while (JS Standard Library, Import Maps, Builtin Modules, and the open HTML issues about polyfillability & “pay for what you use”ness, etc)

Tess: like, as a general engineering principle, you’re more likely to succeed in adding a new thing if it builds on more stable underlying parts

Alice: ??? we begin addressing the various issues that this brings up?

Dan: We could assign some time at the face-to-face for a toast meta-retrospective.  And try to tease out the meta-issues that have come up and discuss each as a separate thing.  Could try to time-box that, to try to come to some reasonable conclusion or action on those.  Make sense?

Alice: Yes.

Alice: Dan, would you like to leave feedback on issue about identifying subissues, and needing a face-to-face discussion?  So that we're not leaving the issue silent.

Dan writes.

Dan: On this issue itself, what do we do?

David: Seems like some of the stuff in this issue depends on the meta-issues.

Dan: Specifically some of the dependencies that Tess brought up.

Dan: Do we need to put this on ice until face-to-face discussion?

David: Maybe worth identifying and opening issues to open before them?

Dan: schedule a breakout to do that?

Alice: I'm happy to go.  Also happy to not go if it helps scheduling.

Dan: Australia+California timeslot might make sense.

Tess and David also interested.  Maybe Peter, if the time works for him.

### WebXR

Dan: A bunch of untriaged new issues.  We need to triage next week.  Some of us have done some proactive triaging.

Dan: One that came in last week was WebXR device API.  That's 403.  (I'm sitting next to Ada.)  One motivation was to try to make this review request a good example; see if you think it is, in terms of level of information in a review request.  We also need to figure out what we want to do with this.  Maybe we need to schedule a breakout on this one as well. I'll put it on the agenda for next week.

Dan: And try to put time for triaging in next week's agenda.
