## TAG Teleconference
##### 10 July 2018

Chair: Dan

Scribbler: Sangwhan

Present: Kenneth, Daniel, Lukasz, Travis, Sangwhan, Hadley

Regrets: Peter, David

---

Agenda:

## [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288) - @slightlyoff @travisleithead

TL: The latest proposal looks like they have integrated a lot of our feedback.
The explainer shows many things that were discussed at TPAC 2 years ago. Progress seems to be good. There is this thing called an Offscreen Canvas which is a proxy object that routes to another element in an actual document. It allows offscreen control to a dedicated worker. From there you can issue drawing commands to the context within the worker. You were expected to create an ImageBitmap, which is an opaque object.

KC: Is this like ImageData?

TL: No. This is different. It's sort of a blob. What has changed is that 1) they have figured out how to sync better, and 2) more proactively push frames from a dedicated worker to the actual document without jumping through too many hoops. There is also a PR which seemed a bit incomplete.

KC: Why would this not use SharedArrayBuffer? I assume it is because this is a specific case? Seems costly with copying.

TL: That's the point of ImageBitmap. It's a pointer to video memory.

KC: Is it possible to implement double buffering?

TL: Probably. You can create a bunch of these, although there is the risk of backpressure. There is an explainer, which isn't quite a spec.

KC: This is driven by WebXR?

DKA: Should note that there are no privacy considerations in the explainer.

TL: Does anyone know who raised this?

SM: What would be the actual privacy concern surface?

DKA: Well, there were specific measures from the TOR browser around &lt;canvas&gt;. (https://en.wikipedia.org/wiki/Canvas_fingerprinting)

Hadley: +1. It would be good to make the situation explicit in the explainer.

KC: Since this ties very closely into the GPU it would be possible to do timing attacks.

TL: The new proposal discusses batching the blit operations from the OSC to the placeholder &lt;canvas&gt; with commit. Second use case is for multiple views of the 3D scene, which requires the scene state to be in the same worker. The third is for WebVR. And so forth. The explainer could use a bit more detail, along with the PR. The rAF timing should be synchronized with the original context. (Scribe brainfart. Might have missed some details.) rAF in the worker is global, which is tied to the main window where the actual display canvas is.

KC: There is a possibility of rate changes with GPU changes or VR contexts.

TL: In the future the spec might accomodate this. One might use a WebVR rAF which runs at a higher framerate. The main purpose of this would be to run game engines built with WebASM from a worker.

KC: So commit() is blit.

TL: Yes. It's a method on a offscreen canvas, and it is a blocking operation. (previously it was not)

KC: Why is that not an option? (as in, a parameter)

TL: I believe this is because rAF serves a different purpose.

KC: So commit() is not something you'd always use.

TL: This seems specific to cases where you need to do blocking blit calls. Now that the background has been convered, the feedback is: The spec would currently only allow dedicated worker - since the other types don't have a strong binding with a specific window. The PR seems to suggest dedicated workers, but seems to be implicit about this. Will raise this. Curious about composition - are there cases where you want to draw parts in a worker and the rest in the main window. Not sure if this is a common use case that needs to be covered - should be worth bringing up. It's unclear what would happen when you call commit when you are in a rAF loop. commit seems to overlap the use cases that ImageBitmap covers. Code samples would be useful. Couple issues on the PR - text that has changed from async to sync, mentions about the user agents deciding specifics. Would like to see more work on this before it ships.

## [Cookie Store API](https://github.com/w3ctag/design-reviews/issues/290) - @hadleybeeman @travisleithead

TL: I like it. Has privacy and security covered too.

HB: I think it's fine too.  Answers my initial questions with the new use case section. 

TL: I reviewed this with another proposal, and think this is a better API. We should only have one API that does this in the platform, so hopefully we'll have that fade away.

KC: Seems to be only an explainer, and not a spec?

HB: Looks like it's too early.

DKA: Let's close this for now, and revisit when the spec is out.

## [Notification Inline Replies](https://github.com/w3ctag/design-reviews/issues/284) - @torgo @hadleybeeman

HB: We looked at this last week, the spec should be clear on the provenance of the notification and the destination of the reply. Commented on this. Should mark as PEF.

HB: The security/privacy answers seem to be missing. But the explainer does have a potential for abuse section. https://github.com/anitawoodruff/inline-notification-replies#potential-for-abuse

She has linked to the pull request. She doesn't have a spec as a standalone thing: https://whatpr.org/notifications/132.html

## [ReportingObserver](https://github.com/w3ctag/design-reviews/issues/195) - @travisleithead @cynthia @slightlyoff

TL: Closed. To use JSON.

DKA: Close and move to F2F?

TL: Sounds good. It didn't look like a great fit for structured headers, so not much we can do here.

## Permissions Workshop

LO: The call of papers should be out today. As soon as it's out I will &lt;something&gt;. (Audio trouble again)

## AOB

TL: Asked around about upcoming F2F and dev meetup. Wonder what we might have in terms of lightning talks.

DKA: Reached out to TC39. Might be interesting to have someone representing npm since that just joined TC39. We have one confirmed talk from them.

KC: Topic is TBD though.

TL: Do we have registration count?

DKA: Yes.



