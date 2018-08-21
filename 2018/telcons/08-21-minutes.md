## TAG Teleconference
##### 21 August 2018

Present: Peter, Sangwhan, Kenneth, David, Travis, Yves, Lukasz, Alex, Hadley

Regrets: Dan
Scribe: Travis
---

Agenda:

* Followup - Proposed TAG role in W3C-WHATWG relationship - Dan

(waiting for folks to show...)

* Followup - Proposed workflow for privacy & security questionnaire - Lukasz

## Followup - Iceland F2F date finalization - Sangwhan

SM: Hosting if fine, but they would prefer us to come in eearly May  (they have an all-hands in late-May, early June).

M(Discussion of availability)

KC: Maybe this is when Google I/O will take place?

PL: Week of 13th or week of 20th?

SM: Maybe aim for Mid-May? Tell our Iceland friends sometime between 13th and 20th, and see what they can do?

(Alex has arrived)

AR: I don't have insight, but I would expect to have dates soon. I'll follow-up and talk to some people...

## [Followup - ISO-BMFF call with MPEG folks - Sangwhan](https://github.com/w3ctag/design-reviews/issues/285)

SM: These folks asked if they could join our call either 28th or 11th of Sept?

PL: Either date is OK with me.

SM: The esteemed chair can decide!

## [queueMicrotask](https://github.com/w3ctag/design-reviews/issues/294) - @dbaron @travisleithead

TL: I'm pretty satisfied with how this has shaped up.

PL: Do we want to raise anything else
?

TL: Don't think so.

## [Page Lifecycle for system initiated Discarding & Freezing](https://github.com/w3ctag/design-reviews/issues/283) - @kenchris

KC: Seems that everything has been resolved. There was one nit (a rendering issue in the spec--it's OK.)

PL: We are OK to close. KC to write a closing statement.

## [CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - @dbaron @travisleithead @plinss

DB: I've pinged folks yesterday to discover status of the PR. No response. Maybe push this out again?

PL: Two more weeks?.

# F2F Backlog:

## [CSP feature 'unsafe-hashes'](https://github.com/w3ctag/design-reviews/issues/291) - @cynthia @dbaron @travisleithead

TL: Sadly, I haven't looked at this yet...

DB: We put in some feedback, and haven't heard any responses to that yet...

PL: Shall we mark this Pending Etxternal Feedback?

DB: Are we done giving feedback?

PL: We didn't get to it during the F2F.

SM: I don't think we're done with the feedback.

AR: Will bping the issue filer to try and get a response.

PL: Will revisit in a few weeks.

## [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288) - @slightlyoff @dbaron @travisleithead

AR: I'm increasing uncomfortable with the `commit` method...

TL: They're subbing out the old `commit` method for a new (blocking) one...

AR: Would having them on a call help?

TL: They've responded to some previous comments of which I haven't read the responses yet. Would like to look those over... Promppose we come back to this next week?

## [Web Components Guidelines Doc](https://github.com/w3ctag/design-reviews/issues/227) - @kenchris @travisleithead @plinss

KC: I have some new text, just need to put it back into the doc.

## [HTML General Review: Custom Elements](https://github.com/w3ctag/design-reviews/issues/244) - @torgo @kenchris @travisleithead @plinss

KC: It's shipping... Some feedback around the term `callback` suffix on all the APIs.

AR: Additional areas of feedback:
* Lack of integration with forms (prevents ability to have custom input type)--we can encourage them to address this in the future.
* Synchronous upgrades
* Sub-registries - large apps would like to scope custom-elements to certain parts of the tree.

PL: Q from chaals about what attribute names should be valid for CE?

DB: WHATWG and W3C specs disagree.

AR: How do they differ?

DB: particular attribute names.

SM: Might be WHATWG has restriction on what names are allowed, but implementations don't follow that? (W3C doesn't have the restriction?)

AR: I wouldn't use CE if I had to prefix. Yuck. CE authors define their attributes locally (to the element).

TL: Is there a conflict with a future "custom attribute"?

AR: Potential issue is whether some new global attribute creates a new processing model for something that wasn't defined before.

PL: Imagine a new 'class' or 'id' global attribute that gets introduced later... the system for processing this might override or have a side effect that is unexpected.
Only safe path here is to prefix custom element's attributes.

AR: ...or you have to exembpt custom elements from the processing logic.

PL: like providing a way for the system to query for a custom attribute without conflict.

AR: or have a way of opt-ing the attributes in/out of the global processing. We probably can't have a opt-in, but maybe and opt-out?

AR: Prefixing is a pain and probably web-incompatible at this point. So, we can't recommend this, but we can recommend a way to add defensiveness to the custom-element iatnstead.

## [Deprecating nonsecure cookie delivery](`https://github.com/w3ctag/design-reviews/issues/239`) - Hadley, Lukasz

Hadley: We need to sort out how to respond to this and Mike's new proposal. We have two parallel proposals here. Which one do we like? How to de-dup?

LO: Is it possible to coordinate this change among all the browsers at the same time? What would the impact be otherwise?

TL: I haven't floated this by anyone yet :(

AR: On track to ship in Chrome 70

HB: Big picture: this would be a good intermediate step on the road to deprecating cookies. But it could be too easy to holdon to this stage for a long time...

LO: If deprecating cookies will happen...

AR: I expect it (deprecation of insecure cookies) will happen (eventually) given people are pushing on it. Re shipping, we should say something sooner as 70 forks really soon.

HB: Let's do this (and not stop here)

RAR: OK. Let's be sure we communicate that.

LO: All cookies, or just insecure cookies?

AR: Affects a small percentage of cookies today.

LO: Would like to have Mike clarify what would happen  under various conditions... web apps.

AR: Much of the requested context is in the blink intent-thread.

* [DOM](https://github.com/w3ctag/design-reviews/issues/229) - @cynthia @dbaron @travisleithead
* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff @dbaron
* [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @travisleithead

* Permissiomnsmnsns workshop progress -- Lukasz
* Security/privacy questionnaire progress -- Lukasz
 
---



