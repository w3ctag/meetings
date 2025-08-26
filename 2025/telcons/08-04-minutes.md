# TAG Minutes - Week of 2025/08/04


## Breakout A (Asia / Australia / West America) - [2025-08-05](https://www.timeanddate.com/worldclock/converter.html?iso=20250805T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair:

Scribe: Dan C

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/08-04-minutes.md

Raw minutes: ...

#### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark


Dan: Jeffrey wrote response. I'll post in a couple days if no one has feedback.

Marcos: Nothing to add from me.


#### [w3ctagbot#71: Bump the minor-updates group with 9 updates](https://github.com/w3ctag/w3ctagbot/pull/71) - @dependabot, @jyasskin

Dan: Does anyone have context about what this is?
Just updates w3ctagbot dependency. Merge or wait for jyasskin?

Marcos: It's a bot thing, just merge it.

Dan: Merged.


## Breakout B (America / Europe) - [2025-08-06](https://www.timeanddate.com/worldclock/converter.html?iso=20250806T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair: Matthew

Present: Matthew, Sarven, DanC, Hadley (second half)

Scribe: DanC, ???

Regrets: Christian, Ehsan

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/08-04-minutes.md

Raw minutes: ...

#### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Sarven: Will have a review for next week.

#### [user-agents#7: Consider applications with both 1p and 3p sections](https://github.com/w3ctag/user-agents/issues/7) - Sarven, Jeffery

Sarven: Will look.

#### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - Sarven, Jeffery

Sarven: Will follow up.

Matthew: PR was merged. Should tis be closed?

Sarven: I was initially thinking of defining "web user agent" up front but in the meantime we had that mention in the PR mentioning what tools it overs. Still some distinctions to be made about what constitutes a UA (e.g., cURL?), what the document covers. I want to review the document to see if the definition needs to be elevated.

#### [explainer-explainer#9: Update the WebIDL guidance for explainers](https://github.com/w3ctag/explainer-explainer/issues/9) - Matt & Jeffery

*bump*

#### [societal-impact-questionnaire#11: centralization](https://github.com/w3ctag/societal-impact-questionnaire/issues/11)

*bump*

#### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2)

Sarven: Have started to come up with examples. We can collect some examples and then pick a good one or two that can be PRd.

*bump for 2 weeks please*

#### [societal-impact-questionnaire#4: Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4)

*bump*

#### [explainer-explainer#30: Say how to explain developer-focused features.](https://github.com/w3ctag/explainer-explainer/pull/30)- Matt & Hadley

Discussion from last week: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/07-28-minutes.md#explainer-explainer30-say-how-to-explain-developer-focused-features---jyasskin

Hadley: I've reviewed it, and commented. I think both the (proposed) deleted text about focusing on the user and the (proposed) added text about situations where the user isn't impacted positively or negatively — both are worth including. I recommend we keep them both. (Or at least, the ideas in both.)

#### [design-reviews#838: Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola

*bump*

#### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

#### Going through the queue

##### [Reduce accept language](https://github.com/w3ctag/design-reviews/issues/1078)

Sarven: Is this to reduce noise?

DanC: Fingerprinting concern. Maybe send main language only. But i18n folks had concerns.

Sarven: I find this interesting. AFAICT, the UA / web browser comes with their default locale, e.g., en, en-gb. It is possible to change the settings from the browser to include additional preferred languages and order them but I suspect this is for a certain group with the know-how as opposed to the general population. Typically people download and use a particular "pre-configured" browser.

Dan C: i18n WG looked at this, had concerns: https://github.com/explainers-by-googlers/reduce-accept-language/issues/10.

## Breakout C (Europe / Asia / Australia) - [2025-08-07](https://www.timeanddate.com/worldclock/converter.html?iso=20250807T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### Logistics

Chair: Hadley

Present: Hadley, Matthew, Ehsan, Max, Lola, Yoav, Martin, Christian, Marcos

Scribe: Christian

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/08-04-minutes.md

Raw minutes: ...

#### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

Martin: Had a meeting, progress was made. Replied to a comment. Not sure if we can do anything on the short term.

Let's give them another week.

#### [design-reviews#1125: Probabilistic Reveal Tokens (for IP Protection)](https://github.com/w3ctag/design-reviews/issues/1125) - @martinthomson, @toreini, @lolaodelola

Martin: This doesn't seem feasible. Seems like a proxy, but not really. It makes me question what the exact threat model is.

Yoav: My understanding is that we want to mask user's IP addresses for realtime traffic but still want DDoS prevention and anti-fraud measures in the longer term.

Martin: to exercise those, you need the IP address of the attack. and you're not getting that.

Yoav: a website that collects the data is now aware of... how can they act on that data from the info coming from the proxy?

Martin: IP addresses delayed by 24 hrs

Yoav: That sounds like good feedback that they could put into the explainer.

Martin: And also, what is the user need? Don't think this is the right solution. Need to understand the threat model first.

Ehsan: Concerned how trustworthy the issuer is. Core cryptographic solution is vulnerable to an active attacker.

Yoav: With my API owner hat on, I've put this back on blinkdev to get feedback. if your feedback is "this is going to get shut down..." If you can recommend they send this to mast, that would be useful.

Proposed feedback:

~~~
First, the explainer doesn't address the end-user benefits that might come from a solution like this.  For those users who reveal their IP address, this doesn't seem like a great deal, but maybe there is some indirect benefit you can point to.

Mostly, the things that we need to understand better what sort of operational model might apply here.  That starts with what sort of expectations end users have with respect to the system you are deploying.  Ordinarily, a user that engages a proxy does so to ensure that their activity cannot be traced back to their IP address.  This upends that, with a 10% chance of leak after a 24h delay.

Then there is the question of how a site might use that information.  If an IP is acting poorly, it learns about this 24h after that abuse starts.  None of the requests that pass the proxy have an IP that can be used at the time of the request.

For this to work for DoS, or any other form of abuse where the reaction needs to occur in real time, there has to be some visibility of IP addresses at the time of a request.  That rules this out for many forms of abuse mitigation.

The explainer says that this is for managing ad fraud, but we can't see how this works for many workflows related to ads.  Given the 10% reveal rate, this might give a probabilistic read on fraud rates, but the 24h delay is going to be very limited in its applicability, even to this narrow case, because many of those cases need real time action as well.  For example, it doesn't look like sites using the attribution API will be able to take advantage of this sort of information.

Finally, we recommend that you take this to the MASQUE working group in the IETF to collect feedback from the experts there.
~~~


#### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Ehsan: Raised a question in the private brainstorming, wanted to clarify if there's any kind of counterfeit document.

Marcos: That's outside of the API scope. Not something that I can answer.

Lola: Is this an early design review? Or a step before release?

Marcos: Barely baked. Not much that can be changed, Credential Management API handles most things. Pretty much set in terms of inputs and outputs. Very simple API, even though it does many things.

Hadley: Are you concerned about the API?

Marcos: I'm concerned about what happens outside the API. How it's used, or how often it's misused. but we've done what we can to mitigate that. The EU wants to use URI schemes, which is even worse. So we're trying to fight back. This is the best of worst solutions. Made it very clear in the WebKit position that this is concerning. But at least we as the web community have a say through this. 

Martin: Do you know how issuance works with this API? Does it require back-channels?

Marcos: I can issue the credentials, I'm the driving authoirty app, and I have this capability to issue. I'm a website, foo.com, and I am authorized as a website to allow the requesting of the issuance of drivers licences from state A, B, C. Then there's a wallet (native app) that is able to pick that up. But the request being signed goes to the website. Native app handles the issuance.

Martin: So it is going around to the wallet? The spec doesn't say that. Does stuff a GET method isn't allowed to do.

Marcos: We haven't implemented it in WebKit, do I don't know how it works. There is nothing in Apple's platform that allows for issuance.

Martin: Some protocols allow to interact with the TPM.

Marcos: There are some protocols that have those details, but they are not in the spec.

Hadley: Where is this going to be specified?

Marcos: Requesting part, request to create, is specified by us, but not the format, just take input of a particular type. How issuenace happens and the format of it is part of ISO. Defines all the steps needed to create a driver's licence, that is cryptographically approved by some authority.

Hadley: Seems weird to separate those, across W3C and ISO. I know some governments won't rely on non-ISO standards (which is a separate problem), but I'm concerned about that fragmentation.

Ehsan: Did you have a look at the Digital Credentials API session at W3C? If you don't have the notes, I can forward them to you. My concern is very much similar to what Hadley said. It's concerning that regulators use this pattern and don't trust browsers. What is your take on that?

Marcos: The OS doesn't issue credentials, the browser cannot do it. Only the wallet can issue credentials. And that wallet usually comes from a government or a wallet representing one. In Australia, there's a private entity (Bick Roads) that represent the driving authority in Victoria. The app has my driver's licence…

Martin: They've privatized this?

Marcos: Yes. This tells the OS, I have a credential and give that to the website. The website allows pulling in something that can be used to create a driver's licence. Only the issuing authority can create it. Cryptographic things take place to make it happen. If you watch my W3C presentation, it mentions the entire workflow.

Ehsan: Can you only use MDocs? 

Marcos: You can only use ISO/IEC 18013-5, e.g. for driver's licence.

Hadley: How to proceed?

Martin: This is not fine, until you have something in the registry that can be interoperabably implemented. Need to dig a little more. I think this can be fixed.

Lola: Do we want to add this to the F2F agenda?

Martin: Seems worthwhile.

_Martin to add this to the F2F agenda and to run the session during the F2F._

Martin: Where do we maintain the agenda?

Lola: Don't have one yet, will prepare.

Hadley: Feel it needs more than 15–20 minutes.

Martin: Rather expect this to be 1.5 hrs. Marcos should give us the nuts and bolts in 20 mins.

(Discussion if this is a good use of time.)

#### [design-reviews#1120: CSS find-in-page highlight pseudos](https://github.com/w3ctag/design-reviews/issues/1120) - @matatk, @xiaochengh

Matthew: Think Xiaocheng has a proposed comment, looks good. Think we should post it.

Hadley: Up for doing that?

Matthew: Will post it.

Hadley: Give Xiaocheng credit when posting the closing comment.

Marcos: Probably not needed, TAG should speak as one voice.

Hadley: But we also shouldn't take work from others. Let's balance that.

#### [design-reviews#1124: WG Revision: Adding document.activeViewTransition](https://github.com/w3ctag/design-reviews/issues/1124) - @christianliebel, @xiaochengh

Matthew: Very simple, let Christian post the comment.

_Christian to post the comment._

#### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @matatk, @xiaochengh

Matthew: Seems there is input missing from the TAGbot. They got back to us on the three points we raised. Includes the reason for the indirection.

… It's idiomatic CSS to invent a hyphenated name, which is correct. But there wasn't a specific reason why this is better than using selectors. Was wondering if anybody thought, we accept that. Was curious about that.

Hadley: Sounds like it's your judgement.

Matthew: Will ping Xiaocheng on the private thread and will ask if he can explain it to me.

… Other two questions were about the syntax, is this okay for an early design review? There is an ongoing discussion. Where they are getting Possible trigger functions from seems to be underspecified. Is from ui-events. Uncertain if there's a hit test needed. Sounds like they intend to be more precise.

… Overall, I think we got the answers we were looking for. Need to decide on the first question.

Lola: So, you want to ask them about the naming convention?

Matthew: Want to check back with Xiaocheng.

Lola: Don't think this is an issue that needs to block the review. Not everybody here and not everybody reading the explainer is a CSS expert. Good opportunity to gently push back on them.

Matthew: Does anybody have a problem with their answer that it is ideomatic? Are we happy with the fact this exists? Are we happy with this layer of indirection?

Lola: Think they should explain why.

Matthew: Ok. Will ask them on the public thread. Think we need to figure out where the cutoff point is. We should manage expectations if we should close this. Or set pending external feedback.

Hadley: We can also reach out to the WG chairs if needed.

#### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion

Max: I think we have drafted a comment in the private brainstorming.

Hadley: Are you ready to publish it?

Martin: Last comment in the issue itself is we would like to invite them to a TAG meeting.

Hadley: Okay for you, Max?

Max: Yes.

Hadley: Then we will organize the meeting.

#### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @martinthomson, @matatk, @toreini

Martin: Discussed this last time we met.

_(Interrupted.)_

Martin: Was assigned to this issue, but don't know what to do with it.

Hadley: Tim Cappalli asked what the progress is. We offered a TAG call.

Martin: We had that call, lots of feedback was given.

Lola: There are subissues. We wanted to mark the subissues as _unsastisfied_, but the main issue as _satisfied_. Don't remember who wanted to write the closing comment.

Ehsan: Remember that Immediate Mediation was another sub issue.

Martin: Think we're not satisfied with that one either, but that was separate.

Hadley: Two tasks: One is write the closing comment for general issue, one is to do something with the subissue. Which doesn't say what our subissue is.

Lola: Think the closing comment is for both of them. We need two, one for the main issue and one for the subissue.

Hadley: Reviewers, how would you like to split that work?

Martin: Started to write a response for the unsatisfied portion.

Lola: Whoever writes the comment for the satisfied review, if you could explain why everything is satisfied, call it out clearly, so there's no confusion.

_Lola to do this._

Hadley: If you close the big issue you don't lose the subissue?

Martin: I think you do, but I'm not sure… didn't use it yet.

Lola: Will keep the issue open. Will set the appropriate labels.

~~~
The TAG has reviewed this and finds that the mechanism here is too similar to related website sets, for which we have provided [more extensive feedback](https://github.com/w3ctag/design-reviews/blob/main/reviews/first_party_sets_feedback.md).

Overall, we're not satisfied that this is the right way to authorize cross-site communication or cross-site release of identification information.  We do want to acknowledge that there are some redeeming aspects of this that make this more manageable than RWS.  The use of prompting/choice UX that might look similar in nature to FedCM does a lot to mitigate the downsides of this approach, but we are not confident that this has been as carefully thought out as the FedCM interactions.

If those UX interactions prove to be as good as FedCM, then the method by which different sites authorize each other seems redundant in that context; a simpler approach is probably enough.
~~~

#### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

_Skipped, wait for Xiaocheng._

#### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Marcos: We have a rough idea. Challenges that arise with this API seem the same as for Writing Assistance APIs. We want to time out the Writing Assistance APIs. Think there's consensus that the issues have been captured. Anyone have any further concerns/opinions?

Ehsan: Might have a question what a prompt is. If there's a malicious web page, can they display an item with a malicious prompt in it? Still articulating the feedback and reading the spec.

Marcos: We've covered that in the feedback. You could abuse the prompt and do mining.

Martin: That's my core problem with this proposal, and I'm not sure if we will get consensus on this.

Ehsan: There are research papers with hidden prompts in them. Infusing a potential LLM to give the paper a positive review.

Marcos: That sounds like a more general societal problem. It's why we have peer review in academic contexts.

… Not sure if this is related to the prompt. Reminds me of the bias of ChatGPT etc. to be on your side. You can prompt it to be less on your side. Part of the prompt engineering part of things, but not really related to the Prompt API. Does the model sway that way? Probably. Good counter-example for this is X's Grok.

_Marcos to draft the closing comment._

#### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres

Martin: It's the same response here.

Marcos: My suggestion is to time this out.

Christian: Timeout seems wrong, if we actually have a closing comment for this? Wouldn't decline be better and refer to the other comment?

Hadley: Can't we post the same comment to this issue?

Marcos: Writing Assistance is a very specific use case, when the larger Prompt one does the same thing. Overarching concerns are the same. That's why timeout or decline seems ok. But agree it's not a great look. They would use the same models unterneath.

_Marcos to decline the review and refer to the other issue._

Hadley: Timing out means someone dropped the ball, we or them. Decline is we won't have a look.

#### [design-reviews#762: MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @xiaochengh, @maxpassion

Max: Wasn't able to check the details. Let's put this in for next week.

Christian: My suggestion is to time this out, since our last discussion on it was last week. 

Hadley: Max, after you had a look, can you give us a recommendation if we time this out?

Max: Yes.

Hadley: Would be good to know if this is useful to have.

## Plenary Session - None

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

