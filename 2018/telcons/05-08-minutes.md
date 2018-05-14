## TAG Teleconference
##### 08 May 2018

Present: Dan, Travis, Alex, Sangwhan (Mr. Moon), Peter, David

Regrets: Hadley, Yves, Lukasz

---

Agenda:

* [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232) - Dan, Yves
* [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - Hadley, David, Alex
* [Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225) - Lukasz, Dan, David
* [Async Clipboard](https://github.com/w3ctag/design-reviews/issues/222) - Travis, Alex
* [Reporting Observer](https://github.com/w3ctag/design-reviews/issues/195) - Peter, Travis, David, Alex, Sangwhan
* [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Peter, Travis, Hadley, Alex
* [AOM](https://github.com/w3ctag/design-reviews/issues/134) - Travis, Sangwhan
* [TV Subsetting](https://github.com/w3ctag/design-reviews/issues/105) - Dan



---
### Issue 232

Action: Revisit later.

### Issue 104 - [TV Subsetting](https://github.com/w3ctag/design-reviews/issues/105) - Dan

Action: Revisit later.

### Issue 222 - Async Clipboard

AR: Still waiting for feedback here... 

TL: I looked over te spec and relevant issues - these last 2 are the only ones... Issue 51 privacy considerations has fantastic discussion in it. I'd love a second review of where they landed in the spec. read and write have separate position - and then each has a config flag...

- https://github.com/w3c/clipboard-apis/issues/51 - the privacy one
- https://github.com/w3c/clipboard-apis/issues/52 

... Suggestion was to move forward with a request for access, API could then be a trigger for the permission - not added to the spec yet. The P&S considerations have not been added yet either.

DKA: I'll also take a look at issue 51. Can you add a note pointing to the areas in the spec that are affcted by this?

TL: A pointer into their draft spec?

* https://w3c.github.io/clipboard-apis/#clipboard-permissions
* https://w3c.github.io/clipboard-apis/#security
* https://w3c.github.io/clipboard-apis/#privacy

DKA: Yes. About issue 51. Are we waiting on 52?

TL: Yes.

DKA: Waiting on anything?

TL: We could submit a draft as a PR.

AR: We should give them some more time. Are these for our issues or their issues?

TL: Some comments on our side should probably be moved over.

Action: Milestone pushed to 5/22.

## Issue 195 - [Reporting Observer](https://github.com/w3ctag/design-reviews/issues/195) - Peter, Travis, David, Alex, Sangwhan

TL: Last time we discussed this we ran out of time.

DKA: We need to review their issue 54? All of their issues still open?

TL: Yes. Let me dig out the minutes of the discussion. I believe we should look at 54. We had some feedback on how this report should be formatted - especially on JSON serialization. Mike addressed those questions in 53 - but I need to look at this.

DKA: Was this related to something IETF did?

TL: I believe so

AR: Structured headers should be something that IETF does, no? Is this structured? This has it's own type system.

DKA: You mean IETF's work?

AR: Yes. We should wait for Mark to comment on this.

TL: I think the point we should be looking into is if the IETF spec is good enough for the reporting requirement.

AR: (Something about JSON, choppy audio.)

Action: Leave note on their issue, potentially invite to future call? Revisit 5/22.

### Issue 185 - [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Peter, Travis, Hadley, Alex

TL: Haven't looked at it yet. Should invite them to a call.

AR: Should we reach out?

TL: Yes.

DKA: How about the 29th?

TL: SGTM.

DKA: Can someone send an invite?

TL: I can take care of this.

Action: Send WebVR folks an invite for a call on 5/29.

### Issue 134 - [AOM](https://github.com/w3ctag/design-reviews/issues/134) - Travis, Sangwhan

Action: Sangwhan to send Alice invitation for future call

### Issue 225 - [Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225) - Lukasz, Dan, David

AR: Status - this is delayed - time to sort out - in Chromium for certain users, changing whether users see a paired requests - warmings about subframe requests.  I discussedd (with the proposer) what happens in lower levels.

DKA: Any other implementors working on similar features?

AR: No idea.

DB: Some people at Moz who saw this proposal liked it. One piece of feedback - list of permissions in the API spec is the list of permissions that are requested.  There  are also permissions that are implicitly granted throuhg a user action. So a question is - if you are talking about ability to delegate permissions do we need a list of those permissions as well?

TL: in some of those cases are they all tied to user action? you'd be delegating without the need for user interaciton?

DB: The reason the spec should be able to control that is that the user might e confused [otherwise]. We have a model where you see a file picker or media picker and there is an association with a tab, but not with an origin. If we're moving to a model where we are associating witha top level page than maybe the top level should be able to restrict.

AR: we don't have a way to restrict.  I can have a [chrome] conversation about what data they do have to inform this...

### Issue 231 - [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - Hadley, David, Alex

DKA: What is the status on this? David left a comment.

DB: I think they opened a bunch of issues on their side, should check what the current progress is.

DKA: We should review the current work.

DB: They linked 5 issues, of which one has been closed.

DKA: We need to review the response and see if this can be closed.

DB: I'll get to it.

Action: Revisit 5/22.

### AOB

DKA: Next week is the AC meeting. Should we have a call?

PL: I can chair.

(Others expressing availability. Will have call.)
