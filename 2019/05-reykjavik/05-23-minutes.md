# W3C TAG face-to-face in Reykjavík

## Day 3 (Thursday, May 23)

* Present: Yves Lafon, Kenneth Christiansen, Dan Appelquist, David Baron, Alice Boxhall, Tess O'Connor, Lukasz Olejnik, Sangwhan Moon
* Scribes: Tess, backup: David

### Readouts from yesterday's breakouts

#### WebRTC DSCP Control API

Dan: Did anyone look at this

Sangwhan: no

Dan: OK, so we need to move this to the Sangwhan/Tess breakout this afternoon

Tess, Sangwhan: OK

#### Event Timing API #324 (David, Kenneth)

David: I posted a bunch of comments a few days ago; when Kenneth and I looked at it we didn't see much more, and we agreed we should wait for their response, which has since come in but I haven't had a chance to read it

Dan: Can we re-file this into today's schedule?

Alice: Slot 8 this afternoon (David, Alice)

Dan: OK

#### Element Timing API (David, Kenneth)

David: Travis gave them a bunch of feedback at our last F2F in Tokyo

David: Kenneth and I looked again yesterday and it had changed a bit

David: Anne was discussing shadow dom encapsulation violations with them

Kenneth: Yes, in a separate issue filed in w3c/webcomponents

David: There's also some replies from @npm1 I need to look at

David: Should I stick this in the same session for this afternoon?

Dan: Yes

Dan: Meta point for the Explainer Explainer "We prefer you to have your explainer in GitHub"

Dan/Kenneth: Another meta point: the issue template should ask the filer for their organizational affiliation & what's your relation to the spec which you are requesting review on

[Aside on how to frame that question]

#### VISS (Sangwhan, Hadley)

Sangwhan: We closed it. We provided feedback

Hadley: and they said they were happy with our feedback, so we closed it.

#### Trusted Types (Sangwhan, Hadley)

Sangwhan: We need to go through this again as the spec has probably changed

Sangwhan: Should this be an isomorphic JavaScript feature, but trusted types are tied to an origin, which makes it hard for Node to use these in templates on the server side

Sangwhan: Also a problem if you try to use these from a service worker

Tess: But service workers are tied to an origin

Sangwhan: Also tied to the document object somehow

Hadley: Only Google appears to be working on this, are we the only non-Google people talking to them about this?

Sangwhan: mwest passed this issue on to someone else

Dan: I think the npm interop point is really important. Is there someone from TC39 we can rope in?

Sangwhan: Yes, I can do that

Lukasz: Google security are very interested in this feature

Dan: Can we change the milestone?

Lukasz: What is lacking in our review?

Dan: We need to give feedback and get a response to it

Dan: We don't have to set a new milestone now

Lukasz: It massively changes how JavaScript works

Kenneth: Not really

Dan: This is a good candidate issue for a secondary (1:1) call

Kenneth: Myles Borins from Node.js would be good to bring in

Dan: I can talk about this with folks at JSConfEU in Berlin soon

#### Service Discovery Mechanism #240

Hadley: We discussed this, and came to a resolution to have a breakout at TPAC with plinss, sangwhan, anssi, and anyone else who's interested (in particular, we think the media people may be interested)

Dan: OK, can we close this or put it in a dormant state?

[Discussion of what the label or milesstone for dormant issues should be]

Dan: I'll make a "TPAC" milesstone and put this in it

### Breakout slot 7

### Security & Privacy Questionnaire

Dan: Can we replace the stale version that people still use with the current draft that Lukasz and PING have been working on?

[General agreement]

Dan: In the issue list for this document, Sangwhan filed ["Drop this feature is not really an option"](https://github.com/w3ctag/security-questionnaire/issues/48). Many people discussed this. Is this issue resolved?

Sangwhan: "Your feature is terrible and should not be used" is not something we shoudl say

Dan: Is that in the questionnaire

Sangwhan: "Drop the feature" is that

Tess: All for less inflamatory wording, but it is absolutely a general principle that we should have.

Sangwhan: That's in the review process:  that's pre-shipping.

Dan: This is the review process questionnaire.  If a privacy issue comes up in a new feature, reasonable to say one of the options is not to ship.

Tess: This came up a lot at the permissions workshop last fall.  Maybe I can link to relevant bit from report.  A theme throughout the workshop is that we're doing a bad job of asking that question up front.  There are definitiely cases where we should have dropped work as a web community.  There was broad symathy that we need to be better at this.

Sangwhan: I think we're talking about slightly different cases.  I was thinking about where feature is necesary bit for entire set of APIS.  Rather than make half-baked version of API by removing a bunch of features -- find a way to reduce the granulatiy.  Bad when competing with native parity.  Why are features not as nice as native?

Tess: Feature of the web that browsing to a website is safe.

Sangwhan: We do have permissions to mitigate these things.

Dan: I still don't understand your objection in this context.

Sangwhan: Shouldn't the first option be to see if you can make the functionality exist but in a mor eprivacy preserving way.

Alice: Look at the end user need.  You're trading off one end user need (need for API) with another (privacy).

Sangwhan: I'm having issues with the sudden jump.  Nothing in between that says "could we please make this work".  It seems to say "if ???, then remove it"

Dan: That's not how I interpreted it.  If you see a security/privacy issue, you should *consider* dropping the feature.  Maybe that's the right thing -- but you look at the impact on the rest of the spec.  But if it's intrinsic to the rest of the spec, go on to other things.  I don't see it as inflamatory in same way.  Maybe different cultural interpretation?

Hadley: I see how Sangwhan got there from what's there... but reading it as last in list of mitigations, I see it as one of seven possible responses... but may not be the best.

Tess: Always tradeoffs between the things.  I do think it should be considered first, but order less important than keeping it in the list.

Lukasz: ???.  Also common in research papers.  We also provide examples of UAs that actually followed with this.  Not saying that everything should be purged.  Happens rarely.

Dan: Sangwhan, Is there a wording change that would make you happier?  E.g., "In some cases"
.
Sangwhan: "If there are no other viable options"

Tess/Dan: no

Lukasz: IMO, current phrasing is not offensive.  We explicitly provide examples of past behavior of UAs.

Dan: Could we come up with wording that makes both Sangwhan and Tess happy.

Tess: I think there's a separate question of ordering:  I think it should be first, Sangwhan thinks it should be last.  Compromise:  put it in the middle, unordered list.  I don't think this is a last resort; I don't think it should be frontloaded.  I can compromise, but just don't want it as last thing to end.

Sangwhan: I'm channeling feedback from people designing powerful features.

Hadley: How many people have you heard from?

Sangwhan: 3 or 4?

Hadley: IT sounds like we're worried about how it will be interpreted.  I think we agree on what it should say and how it works, and worried that others will read it in a way we don't expect.  So I think whatever we decide today we should leave this issue open and we may discover we've misled peolpe.

Dan: Sholud we make a note about this in the document itself and say it's still an open issue?

Lukasz: Then people reading doc will come here and object to that.  They'll use this one issue pointed to from doc to express their range.

Hadley: Agree it de-legitimizes the document.  I'd suggest publish anyway, leave as is or small changes, and leave issue open.

Lukasz: feedback on mailing list

Tess: If we're leaving this open, when are we going to close it.

Dan: It's a living document, we can continue to update it.  I'd like to get to a decision today on replacing the TR version of the document with this document.

Sangwhan: I'm not against that.

Dan: Let's continue to gather feedback.  Find out what views on this, see if people are reacting badly.

Dan: Yves, I think we have consensus view that we should take this document.

Lukasz: (writes reply in issue)

Dan: The URL https://w3ctag.github.io/security-questionnaire/ should replace https://www.w3.org/TR/security-privacy-questionnaire/ which is what we point to in issue template.

RESOLVED: ^

Yves: sounds fine to update

Hadley: I think updating the TR space document should solve Coralie's issue.

David: one minor question: do you mind if I file a pull request to fix spelling errors in this document before publishing?

[General agreement]

RESOLVED: Update TR to match latest ED once David's PR goes in

### Ethical Web Principles

Dan: This started last year. I presented a checklist and got the feedback that it should be a list of principles instead. Iterated, including our last Tokyo F2F. Published [a blog post](https://medium.com/samsung-internet-dev/we-need-a-more-ethical-web-382ba6142632) and got a lot of interest and support from the developer community

Dan: Then I turned the blog post into a talk that I gave at the AC meeting in Quebec City. Got mostly good feedback and some skepticism. I then talked to the AB about it, and got generally good feedback from them. They're mostly happy with this. The one bit of feedback I got is that they didn't want it couched as a set of W3C principles, and wanted us to instead call them TAG principles.

Dan: I've discussed this with several ethicists and have incorporated some of the feedback from them into a draft

Dan: Some scepticism about the use of the word "ethics" within the TAG.

Hadley: These are technical principles and I worry that using the word "ethical" would result in people ignoring it or thinking these concerns are optional

Hadley: I think these principles underly a lot of the concerns we frequently raise on specs

Hadley: [provides numerous examples of these]

Hadley: I worry the term undermines our shared goal in putting these principles out there.

Dan: I see it as something that's increasingly not seen as a "nice to have"

Sangwhan: This feels like just "web principles" or even "internet principles"

Dan: We need to scope this to the thing we have remit over, so "web" is essential here

Dan: [provides "there is one web" as motivating example]

Dan: We don't have authority over things like routers

Tess: That would fall on the IAB

Hadley: is the goal to publish a finding?

Dan: Yes

Hadley: Under each of the principles, we should include a technical justification for the principle. Without that, this is more like an activist call to action

Dan: Those are more examples than specific technical justification

Dan: By putting in examples, people may be confused that the examples exhaustively cover what our concerns are

Hadley: That's an editorial challenge

Tess: Hadley is concerned that not providing these examples would result in people misinterpreting the principles.

Hadley: No, more that people wouldn't engage constructively.

Tess: Dan raised the point that by providing examples we risk people thinking that list of examples is exhaustive, and they won't realize that they're open ended principles that apply to many circumstances.  The Bill of Rights has explicit language (9th and 10th amendments) says it's not an exhaustive list, but that hasn't gone very well.  There's a very real risk that providing examples really limits what people see it as.

Hadley: Yesterday we talked about where privacy policy and local storage may differ from country to country because data protection laws vary.  The web needs to be built to accomodate.  That doesn't undervalue what I think you're trying to say, but I think it does clash with the words you have here.

Sangwhan: How widely do you want this to be understandable?  How wide of an audience do you want?  General web standards audience.

Alice: As low a reading level as possible is a good principle.

Dan: A question Lukasz and I were looking at yesterday and coming up with wording.  veracity vs. truthfulness.  Better to have plainer language, but also needs to be succinct.  If they're too long and have too many explaining words, then that removes ???.

Lukasz: If we give more technical examples, we cut audience significantly.  I'd opt for high level wording.  If you speak of technical examples for each principles, which would you use?  I'm not aware of examples for all -- would need to be articficial.  Similary examples years ago with privacy.  Now this kind of impact assessment is just starting up.

Dan: Please file these as github issues now that Yves has created the github repo

Sangwhan: Some wording can be changed to help these make more sense to a wider audience

[Example of "detriment" as confusing word]

Alice: Lowering the reading level often makes things more clear

Hadley: Are we clear that the audience is spec authors and editors?

Dan: It should also generally be people in the web community, and us as we're working on our various findings and design reviews

Hadley: I think a lot of our confusion would be solved by changing them from the passive voice into active, and to be clear about who we expect to perform the action

[further example: "non-optional"]

Dan: So "we will do this" or "we will do that"

Dan: it sounds to me that we can't publish this as a finding today. I want to incorporate this feedback

Hadley: I'm willing to spend some breakout time on this later today

[scheduling discussion]

<br type="lunch">

### [Autoplay Detection API #356](https://github.com/w3ctag/design-reviews/issues/356)

Scribe: Alice

hober: This got escalated to us a couple of months ago via an unofficial face-to-face.

... unofficial because there was at that point no official working group.

... One of the issues was the autoplay detection API which was being worked on in WICG.

... We had a fundamental disagreement on async vs. sync, and agreed as a group to escalate it to the TAG.

... When the review got filed, it used our issue review template, which made it less clear that it was intended to be an escalation of the disagreement rather than a regular design review.

... We had a later phonecall with them where we raised some tactical concerns.

... I drafted a response, got some feedback from TAG members, and had intended to update the TAG review with my response.

... The Media WG got chartered this morning and they now own this document.

... The venue and the process have now both changed, from WICG to the regular W3C process.

... The rules are significantly different under this process, which has clear rules about managing dissent if consensus cannot be found.

... Let me explain why I would like to punt.

... This got escalated to us because WICG is "kinda weird". The WICG chairs are really lightweight facilitators, there is an on-paper dispute resolution process but I don't know that it has been invoked.

... Now that this document is owned by a group with a more official dispute resolution process, I would like to invoke that process.

ylafon: Our role is to help arbitrarion in case of disagreement that couldn't be solved in the working group.

hober: It is now our role to ...

... I have updated my draft response to reflect the fact that this is now owned by the new venue and should go through their resolution process.

... I don't want to step on the toes of this new group.

hadley: I'm very happy saying "this is not the right time for us to provide feedback".

torgo: Yes, and I don't think that any of this actually conflicts with Hadley's earlier feedback. I think that they should still be taking feedback around user needs on board in their discussion.

... Tess may like to add a note to that effect, that her feedback doesn't contradict Hadley's.

hober: The Media WG have a charter, a mailing list, chairs...

torgo: We can use the "migration proposed" label for this.

hober: Is the delay, followed by punting, going to be taken badly?  My draft text does apologize...

(review of proposed text for comment in the issue)

[Comment](https://github.com/w3ctag/design-reviews/issues/356#issuecomment-495246562) made in issue.

## Privacy

(we did a lot on private browsing modes)
















