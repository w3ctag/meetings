## TAG Teleconference
##### 09 October 2018

Present: Peter, David, Lukasz, Sangwhan, Yves, Alex, Hadley

Regrets: Kenneth, Dan

---

Agenda:

* Security and privacy questionnaire -- quick briefing by @lknik

LO: have a look at [SP PR#39](https://github.com/w3ctag/security-questionnaire/pull/39). PING is editing my/our edits. One notable change is the inclusion of PING as a mandatory/optional step prior to a TAG review. What do we think about it? For the moment I added a small edit saying that we're also open to other external review (i.e. researchers, or so).

The particular edit I'm speaking of:

"The Privacy Interest Group (PING) recommends that a feature group review the
guidance and questionnaire when first considering their feature and meet with
PING at that time to discuss any questions they have about how the
guidance/questionnaire intersects with their feature at a conceptual level.
After the feature group has developed their feature with the
guidance/questionnaire informing their development process, the group should
bring an early draft of their feature specification with Privacy consideration
section to PING for review.  From there the feature group should iterate on
their design.


 When requesting a Technical Architecture Group review, include the filled
questionnaire, along with the description of changes or observations made
during the design and outcomes of your discussion with PING. This allows
external reviewers understand the rationale, as well as the challenges and
evolution of the feature, with respect to security and privacy."

As you'll see from the PR above, I suggested a small word change in the second paragraph

PeterPeter: (Remarks lost while trying to load Cryptpad...)

ddAlex: We haven't quite heard from PING about what is needed to move things forward.

LO: I sent my edits, now PING is editing the RPPR.

Alex: I believe Peter is talking about the vreview process. Lukasz's question was about the PR, and the other question was about the review process.

LO: I think they were suggesting the questionnaire require consulting with PING.

Peter: They can do that, but I don't think that should gate the tTAG review.

LO: I agree. I don't think it should be a pre-requisite. The second paragraph suggests this, should we remove this?

Peter: Maybe we should remove or change the wording.

Alex: We could reword it so we leave the option open.

LO: I suggested a change. Will share, although it is a bit delicate.

LO: my proposed edit

(link?)

"during the design and outcomes of your discussion with PING, or other 
  external contributors or researchers. "
  
* [Form Participation API](https://github.com/w3ctag/design-reviews/issues/305) - @travisleithead @lknik

Travis: Started looking at it, but not finished the review. This proposal allows two things:) Allowing arbitrary JS to participate and supplement a existing form submission by getting an event to modify the form data object. 2) Enable autonomous custom elements in the submission process - not necessarily limited to form elements themselves. I'm actually excited about the first part, the latter I have some concerns about. Quite a few callbacks that would need extra review - but the feature itself is interesting. Not ready for a formal review comment. The event being synchronous is concerning, triggering a form submission inside a form submission seems like trouble.

LO: looked at privacy/security as bit. 

Alex: General view is that the event is fine, having a formdata interface to add additional data seems fine - the duck taping does have problems. One part is that it is not a mixin, and requiring a subclass of a form element. My primary concern suggests that in userspace the developer is expected to build the form infrastructure, instead of providing a mixin that could be used. Decorators from TC39 might work, but then again not. I'd like to see this being idiomatic OOP rather than duck typing.

LO: From S&P I don't see any particular concerns. The new mechanisms don't seem to add significant attack surfaces (i.e. similar to hidden attribute).

Peter: I share your concerns, the fact that it only plugs into the submission process is a bit concerning.  Also validation and resetting.

Alex: There is a section called API details - element details which is handed to you, which is then expected to stored. Custom elements have a lifecycle issue regardless. It exposes a snapshot of what the system is doing, instead of allowing actual participation. I think we should try to aim for a solution that isn't a reflection based proxy interface. Attributes and values are properties - in CE there is no way to find out access the actual state - other platforms describe the lifecycle .

Peter: The explainer covers CSS selectors, would like to have this exposed to a wider scope than forms.
ACTION: Alex to follow up with review comments. Revisit next week.

* Paris F2F
 
(Checking for attendance and dietary restrictions)

* [Display Locking](https://github.com/w3ctag/design-reviews/issues/306) - @slightlyoff @dbaron

David: Have some feedback, but needs to be organized.

Peter: Punt this for a week?

David: Possibly.

Travis: Also have a few concerns about this.

Alex: The lack of functionality to bring stuff into the front buffer batched up is the reason behind this.

David: Not sure if this is the best solution for this. Adds a great deal of complexity, but might not be extremely helpful for all the usecases tehy hey would like to cover.Ne Need some more time.

ACTION: Revisit next week.

* [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) - @cynthia @dbaron @travisleithead
* [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) - @cynthia @dbaron @travisleithead

Sangwhan: Did leave feedback, but it was a bit late - so no feedback from their side yet. I raised the concerns we had from the last call ithe the nto the last review comment on each issue (although the ICE feedback is a bit sloppy. Should probably do a follow-up on this.) - I think we should probably get the stakeholders behind this and QUIickickC during TPAC and have a follow-up discussion on this.

* [Canvas TextMetrics](https://github.com/w3ctag/design-reviews/issues/302) - @dbaron

David: This one the issuissues I wanted to raise have been filed. Think we might be able to close.

* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @torgo @hadleybeeman

Hadley: Did not have time to look into this yet.

ACTION;: Revisit next week.

* [User Activation API ](https://github.com/w3ctag/design-reviews/issues/300) - @dbaron @hadleybeeman

Alex: I spoke with Dave about this. I don't think the explainer has been updated, will send a reminder.

ACTION: Revisit next week.

* [Codec and container switching with MSE](https://github.com/w3ctag/design-reviews/issues/298) - @cynthia @travisleithead
* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @hadleybeeman @travisleithead
* [User Activation v2](https://github.com/w3ctag/design-reviews/issues/295) - @dbaron @hadleybeeman

David: I believe what the proposal is suggesting is similar to what Edge does, although I'm not su sure.

Hadley: Suggests it comes from Chromium.

David: The model with 3 levels seems to be sensible. One point is that this could potentially break some sites that rely on the old pop-up blocker behavior to create pop-up windows.

Alex: I beiveivelieve the intention is convergence. Should look into the usage stats for window.open.

David: Wouddld like to look into some of the details - but given that it works out seems like a good idea.

Peter: Revisit in a week?

* [Review AOM](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @travisleithead



---
