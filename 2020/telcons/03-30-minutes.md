## W3C TAG Call & Breakout Minutes
Week of 30 March 2020 

### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/03-30-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2020-03-30 16:00 UTC](https://www.timeanddate.com/worldclock/converter.html?iso=20200330T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Peter, Tess, Dan, David, Rossen, Yves

Chair: Dan

Scribe: David

#### Triage out *6* [unassigned issues](https://github.com/w3ctag/design-principles/issues?q=is%3Aopen+is%3Aissue+no%3Aassignee)

##### Triage of [#95](https://github.com/w3ctag/design-principles/issues/95)

comparison to [#148](https://github.com/w3ctag/design-principles/issues/148) - doesn't seem like an issue that belongs in this repo

mention of issue david wrote in comment

assigned to Dan and Kenneth

##### Triage of [#97](https://github.com/w3ctag/design-principles/issues/97)

David: Don't we have 2 documents (maybe unpublished) about private browsing?

Tess: [Lukasz's document](https://w3ctag.github.io/private-browsing-modes/) claims to be a draft TAG finding

David: Also Mark's earlier document, I think.

Dan: Let's put reviewing this document onto the plenary session agenda.

Yves: Approved as a TAG finding in July.

David: but not in [one of our two lists](https://tag.w3.org/findings/) or [the other](https://www.w3.org/2001/tag/findings)

Dan: Should we reference the finding in some way

David: yes

Dan: happy to assign myself

Tess: I think something like (quotes from doc about features being indistinguishable between normal and private browsing modes) should be in the design principles doc.

Dan: leave that comment on 97?

Tess: sure, also happy to assign to myself

##### Triage of [#99](https://github.com/w3ctag/design-principles/issues/99)

Assigned David.

Dan: for next time we do design principles

##### Triage of [#100](https://github.com/w3ctag/design-principles/issues/100) GC observability

David: I thought littledan also had a PR about this that landed.

Dan: finds [#129](https://github.com/w3ctag/design-principles/pull/129)

(group reviews the text during the call)

Dan: I'll close and comment

##### Triage of [#101](https://github.com/w3ctag/design-principles/issues/101) time units and temporal proposal

Dan: ...

Tess: Still at stage 2, so Ken's point still applies.  I think don't do anything now.

Dan: Will assign Ken, so it's assigned.

##### Triage of [#102](https://github.com/w3ctag/design-principles/issues/102) GC changes and user-visible changes in state

David: seems like it's covered by existing advice

Dan: Can I close this?

David: yes

#### [Discourage device enumeration, prefer less powerful alternatives](https://github.com/w3ctag/design-principles/issues/152)

Dan: This was assigned to the previous week that we did this, has been some activity, where do we stand?

Tess: I still have an action to write up a PR, just haven't done it yet.

Dan: I'll bump it to next session.

#### [Proliferation of manifests at W3C](https://github.com/w3ctag/design-principles/issues/148)

Tess: I think we made a good argument earlier to close this.  Seems like the sort of closure message that should come from a chair.

Tess: Though one argument is that the language we end up with from previous issue #95 -- maybe that will include language that lists the known manifest types -- preserves the notion that there should be a list, and accomplishes advice of the first.

Dan: how to structure?

Tess: 2 issues should have same assignee, same PR should resolve both, don't need to dupe, resolve both at once.

Dan: (comments in issue)

Dan: (wishes about github being able to link or merge issues)

#### [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144)

Dan: Has a lot of people on it.

Rossen: I thought Tess has an action to come up with a list of how these would go into the principles doc?  Or was that a different issue?

(later) ... oh, I was thinking about the device enumeration one.

Tess: I don't remember that. I thought Peter had taken this, but vague memory from long ago.

Peter: I don't remember that...

Dan: Mike West asked us if we want help.

Dan: We could ask Mike if he has ideas in his head to bring to the table

#### [input.valueAsDate violate "obj.attribute === obj.attribute must always hold"](https://github.com/w3ctag/design-principles/issues/139)

Dan: Maybe we can wrap this up?

David: Need to figure out if it needs a PR or already covered by the doc.

David: I'll make a small PR.

### Breakout B (US / APAC) - [2020-03-30 23:00 UTC](https://www.timeanddate.com/worldclock/converter.html?iso=20200330T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Alice, Tess, Peter, David, Rossen, Sangwhan

#### Triage out *6* [unassigned issues](https://github.com/w3ctag/design-principles/issues?q=is%3Aopen+is%3Aissue+no%3Aassignee)

##### [#104 Prefixing particularly dangerous operations with "unsafe"](https://github.com/w3ctag/design-principles/issues/104)

Rossen: So the intent here is to annotate API that invoke native code such as webasm and mark them as 'unsafe', right? 

David: Yes

Rossen: We had this pattern in .NET CLR for marking unsafe calls into native c++ code during pinvoke and later moved away from it. 

David: This is not necessary for native code only but anything which is unsafe. Example, web locks... stealing somebody else's lock is unsafe. CSP started by naming a number of things as "unsafe".

Peter: Also this is common in a lot of crypto code

Sangwhan: seen some of this pattern when thread safety is a concern.

Rossen: Should we take on that and add it to design principles then?

David: yes, but problem will be defining what's unsafe. 

Peter: David, do you volunteer?

David: I guess

Rossen: I'll help too

Peter: OK, let's set it for next month


##### [#111 guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111)

Peter: Who's goign sign up for this one?

Tess: Maybe me.

Peter: Good, thanks. Let's add Kenneth too.

##### [#112 Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112)

Tess: It was raised by Kenneth, let's assign it to him.

Rossen, Sangwhan: This is very specific guidance..

Sangwhan: We don't have general guidance about specific device access and/or patterns. This proposal is very specific in its use case..

David: General case could be - sharing something through a worker that both sides have access to, define how do you act past that point. Sharing open network connect through a worker for ex. What happens when worker and main thread write to it. 

Peter: OK, let's assign David too.

##### [#113 Create advise on when to use built-in decorators in specs](https://github.com/w3ctag/design-principles/issues/113)

Peter: This looks a bit too early to do anything before TC39 is ready. Let's leave it for now.

##### [#116 How should the toJSON method be used?](https://github.com/w3ctag/design-principles/issues/116)

Sangwhan: Do you want toJSON or not, and what best practices on cerialization could be... no clear idea of how to define it clearly.

Peter: Deserializing is completely missing at the moment too.

Sangwhan: +1, and how is it supposed to be done so it's not lossy etc. I'll try and do something with this one.

##### [#117 High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117)

Alice: I'm interested and add myself

... adding David, Rossen and Tess as well :)

#### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41)

David: There's a lot of comments and points behind Dominic's comment. What used to be 5 back in 2017 is probably 9 by now. At some point in the past I think I tried to get someone from webapps sec to write it but unsuccessfully.
This could be one of the more useful things causing a pile of inconsistency in the platform. Perhaps it is a good time to define it. 

Sangwhan: I recall some discussions with Kenneth about it, will try to dig out minutes.

Peter: It's probably good time to pull off Travis off this. 
Should we try and write it or reach out to others?

David: I will but might end up having to reach out to others for details.

#### [expand on consistency of naming](https://github.com/w3ctag/design-principles/issues/149)

Alice: There's a PR that's already up for this issue by Tess and myself.

Rossen: This is a great PR! :) Some issues to be addressed and that should be that.

Alice: Tess, lets setup some time and address these so we can close.

Peter: SGTM

#### [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145)

Rossen: Seems like Sangwhan is going to draft PR for it.

Sangwhan: ack, I'll give it a go soon and send the PR for review.
Any opinions on abort controllers?

Peter: It is a good idea in general for things that are abortable... 

Sangwhan: There's another issue #138 that is about abort controllers... I'll link to the promisses spec with this PR

Peter: SGTM

#### [How do we track implementability concerns?](https://github.com/w3ctag/design-principles/issues/143)

Rossen: It seems like #142 is very closely related, do we need both issues open?

Alice: The were oppened at the same time. Difference is about having impls that are kind of interoperable (close engough such as the backdrop filter)... where #143 is about having a feature that is super useful but not everybody can implement.

Sangwhan: Different problem is for a given impl having different behaviors on different platforms.

Rossen: So perhaps close #143 and move everything to #142?

Peter, Alice: SGTM

#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142)

Peter: Metaquestion - is the goal to give advice to WG's when these situations occur?

Tess: Yes! We want to give creative ways for groups to get themselves out of such situations.

Peter: There's always the tool in CSSWG that is to use RFC6919 language.

Rossen: It seems like the comments in the issue are capturing the ideas pretty well. Are next steps simply turning this into spec text?

Alice: Where would said text live?

Peter: Under writing good specs section? Or "other considerations"? "Implementability concerns" sections is also a good candidate. Could be a new section.

Alice: OK, so add this into design principles?

Peter: yes.

Alice: SGTM... I'll take it since I already wrote the comments.

### Breakout C (APAC / Europe) - [2020-03-31 08:00 UTC](https://www.timeanddate.com/worldclock/converter.html?iso=20200331T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Discussion on manifest files issue. We produced text for a new proposed section 2.5 in the design principles.  

Also issue with using _ in manifest files for names as it's inconsistent with other approaches to naming. Maybe we should have some wording in the principles that reflect this.

Triaging unassigned issues.

Closed #113

Discussed #112 - put it on the back burner.

Discussion on #137 (feature detection)

Ken: there are different kinds of feature detection - does the device have it, does the browser have access... This is a really important case.  Some people have said "don't expose nfc if there is no nfc chip" but then you get into the questions about fingerprinting.  This is almost a separate finding.  What kind of ways do we do feature detection on the platform and can we turn that into specific guidelines?

Ken: we need to look at a lot of specs...

#### Triage out *6* [unassigned issues](https://github.com/w3ctag/design-principles/issues?q=is%3Aopen+is%3Aissue+no%3Aassignee)
#### work on some of the newly assigned issues

### Plenary Session - [2020-04-01 05:00 UTC](https://www.timeanddate.com/worldclock/converter.html?iso=20200401T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### Breakout Rollup
#### Review and merge [pull requests](https://github.com/w3ctag/design-principles/pulls)
#### Issue an update of the principles document if possible
#### Additional triage

### Logistics

Chair: Dan

Scribe: Alice

Present: Alice, David, Dan, Kenneth, Tess, Peter (2nd-half)

Dan: Main objective is to review and merge pull requests on the design principles.

... Might be the first thing we want to do, might do a breakout roll-up after that.

... Three PRs on design principles.

... Tess, can you give us an update on #132?

Tess: I'll start with #163...

... Alice and I had taken a look at several issues related to naming, wrote some text that we thought cleaned up the naming sections and tried to address some of those issues. Several comments since I last looked at it. Not sure what is left to be done, but it's all in there.

Dan: Could we do that now?

... One change requested from Rossen...

Tess: Probably not. Second one is #164... first of hopefully many PRs incorporating HTML design principles.

... Priority of constituencies seems unambiguously popular, we cite it a lot.

... There are some comments from Anne VK and David Baron... I think we could land it as-is but I'd want to hear from David.

... Anne approved...

... David is proposing some additional text.

Dan: I think we can land it, and add David's proposed text as a follow-up.

Tess: doing it.

Dan: Second one is David's small fix (#165), Tess is listed as a reviewer.

Tess: It looks good to me.

Dan: Another bit of text...

... Kenneth and I were talking on breakout C about manifests... out of that came a discussion, need to add a new subsection into section 2, about manifests.

... [We wrote some proposed text](https://docs.google.com/document/d/1Jr_L_b4tbYOs76bQ49AwAHHt_pbcDcwh3O7miFpqvgk/edit#heading=h.w9azv2tv714x)

... Some stuff in here about naming

Kenneth: For legacy reasons, ... chose to use underscores, this is now what's in the web app manifest and payments manifest... people want to reuse dictionaries into the DOM... you end up with issues since the casing is different between manifest files and DOM APIs.

Dan: Be aware that there are other types of manifest files out there... Yves suggested enumerating types of manifest files and what they're used for.

Kenneth: Payment Handler Manifest, Publication Manifest

Dan: I'll probably turn it into a PR... 

Alice: "Be careful" isn't that actionable

Dan: Changed to "try to avoid".

... Some cases might be inevitable to add a manifest file. But there are so many it complicates the platform.

Dan: People should be encouraged to think of manifests as extensible, but understand that they will need to work with the team involved.

Alice: Does this come back to monkeypatching?

David: Yes.

... A bunch of these differences come down to scope...

... Often the scope is wrong for the existing manifests. WebApp manifest is a think that covers a specific scope, covers this set of URLs and not that set of URLs.

.. Trying to remember if Web App Manifest scope is different from service worker scope. Somebody said theyw ere trying to fix it, but it wasn't quite the same. Payment Manifest is different partly because they needed a different scope.

Dan: Can we go back to monkeypatching? 🐒🐒🐒🐒

... We need a new finding about monkeypatching.

Tess: I think I had my hand up for that.

... I might even still do that! I still think it's a good idea!

Kenneth: Web Share Target is extending Web App Menifest.

Dan: Should we move on? And by on, I mean back to the previous PR?

... I will try and write up a PR for the Manifest file issue.

... PR #163 https://github.com/w3ctag/design-principles/pull/163

... Rossen had requested changes.

Tess: I pushed an update...

David: Uh...

Tess: Oh. I'll fix that later.

... Rossen's first comment was regarding a section simply saying "Please consult widely on names in your APIs". He suggested adding specific suggestions of forums of feedback.

Dan: Something like "consulting widely means in the appropriate forum for the particular technology involved...?" We can't really give an exhaustive list. But I take Rossen's point. We could say something like "in the appropriate open forum".. people might say "well I talked to every expert in my company".

Tess: I agree we could do better...

Alice: This advice seems to be asking people to invite a bikeshed.

David: Perhaps people would be more likely to take advice that falls along the lines of the Design Principles advice?

Dan: If you're applying advice we gave you.. we've got your back.

David: Perhaps it's "consult widely but pay attention to what the underlying principles are"

Kenneth: Try to be like existing things on the platform... not always easy.

Dan: Tess, would you be able to try and come up with something?

Tess: Ok.

Dan: Shall we go through breakout notes?

... Breakout A... 

... Talked about manifests, which is what prompted the later discussion inC.

... Closed 102, 100... left nothing unassigned.

... Talked about #97, Add notes to consider private browsing/incognito mode.

... Tess commented on this issue, we need to create some text that references the private browsing modes finding that Lukasz published last year. I think I took the action? Some confusion. 

Tess: Let's schedule a breakout to do that.

✨ breakout scheduling ensues ✨

Dan: Discourage device enumeration.. bumped... manifests we talked about... harmonize permissions we asked Mike West for feedback, David said he would make a PR and he did, on #139

... And we closed it. YAY.

... Breakout B...

David: Triaged a bunch

- Prefixing things with unsafe, bumped
- inheritance between contexts was assigned
- handover access to sensors.. about threading?
- Decorators, too early
- toJSON, can't remember
- High level/low level APIs, added Alice, David, Rossen and Tess

Then went on to assigned issues

- allow- attributes
- Naming, we have a PR - can close once the PR lands
- Synchronous/asynchronous, Sangwhan is goig to draft a PR
- Implementability concerns ... couldn't remember what that was

Alice: Oh I think that might have been about the synchonous/asynchronous thing in the media WG.

Tess: Maybe.

David: And Alice took the interoperability/implementability write-up

David: When we do the triage in breakouts, we can focus on issues relevant to people in the breakout.

Dan: Are we ok to issue an update to the doc?

Alice: I'd like to wait for Tess' and my change to go in.

Dan: I'll put that on the agenda for next week's plenary.

David: I'm not aware of it being in w3c space previously. So we'll need to figure that out.

Dan: All the other findings are in w3c space.

David: We could upgrade it to a draft TAG finding, or something.

Dan: Let's discuss that next plenary.

... Breakout times... for this week I used the glitch script ...

... generated the plenary for 10pm UK time (today)... 

... for next week, should we switch to a different time? Should we alternate weeks?

David: I'm up for trying it? We previously vowed never to do that again...

... People forgot about them and missed the calls.

Dan: Yves can't make this time, so if we want Yves on at least half the plenaries..

David: Rossen also can't make this time.

Dan: For next week, we can do the 10pm UK time...

✨ plenary scheduling ensues ✨

### Brekaout to talk about Private Browsing Modes

Tess & Dan

possible things we can say to API developers about private browsing modes

0. private browsing modes are a thing, see this finding -->

carefully consider how your api should behave in PBM

1. do not reveal that te user is in private mode

section 2.3 should reference whatever we are adding

2. do not reveal that te user is using AT

section 8 should reference principles elsehere inthe document that pertain to its topics
