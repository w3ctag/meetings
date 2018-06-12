## TAG Teleconference
##### 12 June 2018

Present: Kenneth, Hadley, Travis, David, Daniel, Yves, Peter, Alex, Sangwhan

Regrets:

---

Agenda:

* [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - @slightlyoff @dbaron @hadleybeeman

David: I still didn't get a chance to go through the feedback. Sorry.

Kenneth: there's a lot of feedback

David: lots of feedback, lots of responses...haven't had time.

Dan: should we bump it to next week?

Alex: is there a timeliness constraint? Are we blocking them?

Dan: they wanted feedback by March 1st

Alex: should we find a new owner?

Dan: we just need to understand what they said.

Kenneth: they filed a few issues due to the feedback

Dan: I'll bump to 2 weeks from now. If folks want to drop in and leave thoughts, that would be valuable too.

* [Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225) - @dbaron @torgo @lknik

Lukasz: there was a talk to organize Permissions workshop (presentations/etc but also some brainstorming/work), but somewhat stalled now.

Dan: we covered this last week, but is there something else we can do on this right now?

Lukasz: We aren't tasked to design the "right" solution. Travis provided feedback from Edge in the issues

Travis: I asked about transitivity about delegation after giving it a thought, and that seemed like a non-starter; if we're going to block transitivity, the iframes thing seems the way to go

Dan: what can we do?

Lukasz: we can wait or provide some initial feedback

Dan: I propose that we close the issue but note that we're interested in the topic and would like to see it improve

Lukasz: my concern is that we might see developments that create implied (or not) permissions, like sec-metadata that might create leaks, and I'd like to keep an eye on the potential evolutions of the architecture

Dan: so maybe we keep this in mind and perhaps reach back out to Mike. I think we should close this one rather than having it linger on. 

Lukasz: I agree. I will also reach out to folks doing the permission workshop to understand the current state.

Dan: I'm going to close-and-comment. Would be nice if someone else could also add the URL to the workshop in the GH issue

Lukasz: workshop is not yet public, but when it is, I'll include the link


* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - @plinss @dbaron @slightlyoff @travisleighead @cynthia

David: there's a new version of the spec that includes some of the feedback that Alex and I provided a few months ago. It looks like we need to re-review this.

Travis: added myself to the issue

Alex: looks like the explainer hasn't been updated with the changes to the spec

Dan: will reassign to next week.

* [ReportingObserver](https://github.com/w3ctag/design-reviews/issues/195) - @cynthia @slightlyoff

(long conversation about the utility of Structured Headers)

Alex/Travis: big open question for SH is if it can do nesting. BNF suggests not.

Alex: ok, having undrestood the nesting question, are we ok with telling the RO folks to go forward with JSON but note that something better might come down the pike?

Travis: do you think RO data will need nesting?

Alex: very likely

Travis/Dan: ok

{Alex to provide feedback}

* [Triage Newly Added Issues](https://github.com/w3ctag/design-reviews/issues)
* Talk about developer meetup in Seattle

Issue 284: Alex outlines the feature, Kenneth notes the diagrams

Dan: I might volunteer for this one. I'm worried about spam prompting.

Alex: would like to separate those

(Dan and Hadley to reply, on next week's agenda)

[Issue 285: Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285)

Sanghwan: this might be a bad idea; stuffing web apps into video files

(Questions about where the referred email resides.)

Dan: Sanghwan, do you want to take this?

Sanghwan: they're re-inventing a packaging format.

Kenneth: We are already getting Web Packaging, can they use that?

(conversation about MPEG; is this an open spec? Horror from Hadley)

Sanghwan: I'll take this; their use-cases seem simpler than Web Packaging. Video is the main actor in their model, web content is there to support it. From our perspective, they'll still need use Web Packaging and stick it inside BMFF.

Alex: does this have any way to denote origins?

Sanghwan: no; the content could come from a DTV stream which doesn't have an origin. So that's a bit weird.

Dan: sounds like a use-case for signed Web Packages

[Issue 286: CSS Logical Properties and Values](https://github.com/w3ctag/design-reviews/issues/286)

David: I'm pretty happy with this; I've reviewed it with my other hats on.

Alex: this came up in the Blink API OWNERS conversation recently. Was Gecko OK with the size of this change and it's serializations?

David: this doesn't change any of the serializations. You're now stroing both, but they have the same serialization.

David: I'll have another look to see if residual issues are resolved. I can try and take a look.

Dan: the 19th? 26th?

David: the 26th

---



