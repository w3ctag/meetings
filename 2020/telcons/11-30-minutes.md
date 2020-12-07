## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/11-30-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2020-11-30](https://www.timeanddate.com/worldclock/converter.html?iso=20201130T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris
* [review security & privacy issues](https://github.com/w3ctag/security-questionnaire/issues) - @hober
* clean up design review issues

### Breakout B (US / APAC) - [2020-11-30](https://www.timeanddate.com/worldclock/converter.html?iso=20201130T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311) - @cynthia, @dbaron, @plinss
* [triage design principles issues](https://github.com/w3ctag/design-principles/issues)
* clean up design review issues

### Breakout C (APAC / Europe) - [2020-12-01](https://www.timeanddate.com/worldclock/converter.html?iso=20201201T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Review of NativeIO](https://github.com/w3ctag/design-reviews/issues/566) - @cynthia, @kenchris
* [review current state of ethics issues](https://github.com/w3ctag/ethical-web-principles/issues) - hadley, dan
* clean up design review issues

### Plenary Session - [2020-12-02](https://www.timeanddate.com/worldclock/converter.html?iso=20201202T060000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* assign actions our of our discussion with Chris Wilson last week
* [triage design review issues](https://github.com/w3ctag/design-reviews/issues)


--

## Minutes

### Breakout A (Europe / US) - [2020-11-30](https://www.timeanddate.com/worldclock/converter.html?iso=20201130T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Tess, Kenneth, Peter, Yves, Hadley, Rossen (2nd half)

Regrets:


#### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

[discussion on the API]

Ken: there is no API spec yet...

ken: [leaves commet]

Dan: I will look at the privacy & security response - briefly looking it looks reasonable.

[bumped a week]

#### [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman

Tess: we had a meeting ... I can capture the results in a comment in the issue. They took our feedback into consideation...

.... [about pronounciation semantics]...

#### [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564) - @hober, @ylafon

Dan: we had a brief discussion last week...

Tess: reading through most recent comments... I'm cautious about the compat stuff.  Some good comments from Domenic & Anne. I like swapping the ... a way to get back to the old behavior if you need it. Doesn't help sites that aren't being actively maintained.  We have to be careful of breaking sites that have no plausable path to being fixed...  .. but this seems like a reasonable way to do it if you're gonna do it.

Tess: will leave a comment.

#### [review security & privacy issues](https://github.com/w3ctag/security-questionnaire/issues) - @hober

Tess: I'd rather look at the [PRs](https://github.com/w3ctag/security-questionnaire/pulls).

... [109](https://github.com/w3ctag/security-questionnaire/pull/109) - make use of spec and feature more consistent.  Happy to approve & merge.

... clarifies between features and specs... also has some grammar and language fixes.

Hadley: looks fine - but [finds typo] - [fixes typo]

Dan: Ok happy to merge.

**MERGED**

Tess: 100 there are pending edits

Tess: 99 - we can skip - need to address comments by Martin Thompson

Tess: [94](https://github.com/w3ctag/security-questionnaire/pull/94) I requested some changes from the requestor but the changes haven't been made. 

Hadley: I can write the comment back. 

Tess: issues - 2 or 3 that will be closed by open PRs.  Some issues from Sam - that are in sections I haven't got to yet.  There are a couple of questions later on in the questionnaire - are disjointed bullet points instead of explanatory text.  Legit issues...

Dan: new issues?

Tess: no, we did a full triage at TPAC. And Pete Snyder and I have a call on Wednesday to do some pair editing.

Tess: Re- automatic publishing...  Sam mentioned that he would like the /tr version to be automated.

Yves: there is a tools issue... because it's cc0.  The fact that the TAG is involved generates some issues. We'll do Design Principles first and then put S&P questionnaire in auto. 

Yves: I will update the latest version - ping the webmaster.

#### clean up design review issues

**triaging untriaged issues**

[571 - digital goods API](https://github.com/w3ctag/design-reviews/issues/571)

Hadley: feels dangerous... 

Ken: app store use cases... if you want to ship a PWA in the play store - you have to wrap it in a TWA... 

Rossen: what is the purpose of this API on the web?

Ken: MS want something for their store, Google want something for their store...

Tess: I would prefer we just expose the API in web views in apps ... seems weird to require a separate Web API for that.

Hadley: good to get more use cases...   - other APIs

Tess: simplest thing would be to use the payment request API - and for the store to use a payment method...

Tess: the way the payment request API works is everything hinges on payment method - the payment method is a black box.  The most straightforward way to do this is for the store to define a payment method - and the payment request would fit a profile.

### Breakout B (US / APAC) - [2020-11-30](https://www.timeanddate.com/worldclock/converter.html?iso=20201130T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)


Present:

Regrets:


#### [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311) - @cynthia, @dbaron, @plinss
#### [triage design principles issues](https://github.com/w3ctag/design-principles/issues)
#### clean up design review issues

### Breakout C (APAC / Europe) - [2020-12-01](https://www.timeanddate.com/worldclock/converter.html?iso=20201201T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Ken, Sangwhan, Alice, Yves

Regrets: 


#### [Review of NativeIO](https://github.com/w3ctag/design-reviews/issues/566) - @cynthia, @kenchris

Ken: seems to be orign-bound filesystem.  Different to filesystem - you can open directory. Different sites can use the same directory.

Dan: So it might better be called "orgin bound virtual filesystem"... the current name is quite scary.

Ken: of course with this they don't need the same kinds of dialogs. I'm still worried about quota.  Video editing, etc... needs lots of disk space. How is that managed?  Handled with usual quota things.

Dan: [left a comment](https://github.com/w3ctag/design-reviews/issues/566#issuecomment-736297259)

Sangwhan: let's imaging a scenerio where you use something like this to implemnt a PCB CAD webapp - you'd have multiple files... if you bind it to an origin you can't take it to another tool... 

Dan: you'd need to export.

Ken: if you want to bring a video to another tool to say add special effects.

Sangwhan: moving between different CAD applications is a pretty common case.  The filesystem API does do this.

Dan: trade-off between privacy ....

Sangwhan: what if you want to share between native app and this?

Ken: you'd need to use filesystem API

Sangwhan: these APIs don't acknowledge eachother... 

Ken: yes could it be an option on the other API? Give me sandboxed filesystem?

Sangwhan: yes it's a sandboxed filesytem where you can't access the files...  I don't see why you would use this over IndexDB...  Except for porting legacy application...

Ken: music editing, video editing....

Sangwhan: yeah but this design doesn't make sense for music editing... You have to bring in small pieces of video / audio, assets...

Ken: You could use this in combination with filesystem access... or you get them from a cloud system...

[crafting comment](https://github.com/w3ctag/design-reviews/issues/566#issuecomment-736308119)

Yves: could you add a few things to make Cache API use Native API... immutable flag... persistence... store until this freshness expires... 

Sangwhan: something you can mark as ephemeral...

Yves: it would be good if instead of creating a new system, create a lower-level system that you could build something on top of...

Dan: ... and what about storage buckets?

#### [triage design principles issues](https://github.com/w3ctag/design-principles/issues)

Discussing organizing pair-wise breakouts for next week on the design principles...

We agreed to do design princples first week of the new year.

#### [review current state of ethics issues](https://github.com/w3ctag/ethical-web-principles/issues) - hadley, dan

did not discuss

#### clean up design review issues



### Plenary Session - [2020-12-02](https://www.timeanddate.com/worldclock/converter.html?iso=20201202T060000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### Breakout Rollup

Present: Dan, Rossen, Alice, Peter, Hadley

Regrets:

#### Roll-ups from breakouts

#### assign actions our of our discussion with Chris Wilson last week

Peter: actions were to make a couple of new issue templates...

Alice: the FYI - things that want to ship that don't need a full TAG review... things we agree are an FYI, close, thank you...

Peter: the other part was having an automated feed... or early knowledge of ideation of things before they go to WICG... so people don't have to submit them... There's already a process of creating a WICG repo ... we  could have a bot pick it up... 

Alice: we do have an early design review template...  this would auto-file it?

Peter: different from an early review?  it's more of a guidance for new ideas... an opportunity to give them a nudge... 

Alice: under what conditions would we spin up such an issue?

Peter: when they get a repo in WICG....

Dan: but sometimes, don't they arrive in WICG fully formed and maybe shipped?

Peter: true. if that happens, we should change it into a different kind of review. When we triage it.

Dan: We have discussed with Chris that we should make it a criteria for getting a response to a review request that you are not in a private repo, that you're in WICG. But then, others see it as not a proper standardization route (it's not, it's incubation), which is why we ask where it's going after WICG. Sometimes that's a surprise to the people working on it.

Hadley: one of the roles we play is as a router or a switch.. 

Peter: primary output of these ideation reviews... "look at these previous attempts" "go talk to these other people" "think about what working group this will end up in"...

Rossen: also paying it forward for ...



#### Going through large spec reviews as part of TAG reviews

Rossen: [are we going to be expected to be doing deep dives into large docs... e.g. CSS]  if so what are the ways to make this easier?  One idea is to have a quick summary of what we are being asked to review.  Contrasting with HTML horizontal reviews - they are pointed at PRS... CSS modules are similar - a collection of changes that are moving forward. I think we do a decent job of collecting the change list - but this doesn't give you the big picture if you're not deeply familiar with CSS. So what do we do with these types of reviews?  CSS group is getting ready to progress a bunch of specs to PR - and TAG is on the checklist. I18N will be similar.

... concepts deeply rooted in CSS ... 

Dan: So maybe there shoud be a new issue template, for tag review? This is a big chunk of work... we can leave off questions like 'what's the target for this?'. But we can ask, in your explainer, write what the substantive changes are; explain like a new API developer would explain their ideas, for someone who isn't enmeshed in the domain, what this change is and how it meets user needs.

We're changing CSS in this way... Okay, why? How is that going to meet user needs? Users are clamoring for this, help us understand why. It should be explainable.

Rossen: We could have an editor come in and give us the 5 minute download...   In CSS there is so much work .. by the time we're ready with something I have a hard time thinking where TAG might say "no"... Have we had any cases where TAG has said "no" to CSS - in PR or CR - no. 

Peter: we have overlap between CSS and TAG which helps

Alice: one thing that comes to mind is displaycontent - had I reviewed that at the time - if they had written down "we want this thing so we can get the semantics of this thing in the a11n tree without having a layout object" ... it would have been better for TAG review.  But if you just dump the CSS spec there's not the context.

Rossen: I don't think we should be rubber-stamping.  

Hadley: is CSS special?

Rossen: it's the biggest thing happening in W3C...

Alice: why?

dan: Let's look at the web platform. e have html, javascript, and CSS. of those three, W3C has CSS. Webapps is also a big group.

Rossen: in general, regardless of the working group - do we have cases where we are saying NO to transitions...?  There have been some.

Hadley: should we do earlier CSS reviews?

Rossen: we do that. A lot of proposals coming through design reviews come through CSS.  Some WICG stuff ends up in CSS.

Hadley: I agree we're in an awkward position. Fundamentaly uncomfortable with declaring CSS proceduraly different and special. Haven't heard a good reason why we should inetract diffeently with CSS.

Rossen: don't want to put CSS in a special bucket.  More - as we start ramping up reviewing docs that are going to be coming to PR - how to make that easier for everyone... One proposal made by Elika : why don't you have an editor on one of the TAG calls to discuss - that will allow us to move it more quickly.  Will allow us to zoom in...

Hadley: I think that makes a lot of sense.  In the past we have invited groups into a call when we want to have a discussion about explainer or are having comms problems. It would be great to do this in a way that doesn't require the same documentation... i don't want to have discussion replace that step.

Rossen: you want to have a paper trail.

Hadley: we have set the expectation with the community - e.g. a11y, i18n... we talked about what explainers are how they're used etc... 

Dan: So, a new issue template? pointers to the material, the PRs? Why we think the TAG might be interested... And then, absolutely we can have an editor join a call.

...We haven't had a good policy about how we do guests on breakout calls. Is it okay to join a breakout call? or does it have to be a plenary call? We should sort that out.

Peter: we could do that.

Alice: If you invite a guest, you will spend the entire hour talking about their issue.

Peter: not always, in the past

Dan: It is up to us to timebox the discusssion. Otherwise I agree — it will fill the time available.

Peter: It's more likely we'll give a guest more time during plenary, since it's a bigger deal to get them in.

Alice: we cannot possibly invite every single person who requests a review. 

... regarding CSS - it's often difficult to understand how to use CSS features... MDN is the place for writing these up but people need to write those articles.  CSS wg process is extremely contextual.  "the way things work in CSS is you have to have been there"..   no on-ramp.

Dan: Agree.

Rossen: yes.

Rossen: explainers...  not sure they will help...

[discussion of how things work in CSS ville]

Rossen: many many different considerations - e.g. i18n, a11y -- features baloon because there are so many considerations...

Hadley: an explainer could document where you make these trade-offs.

Peter: a lot of times when that's a point like that it turns into a note in a spec.

Rossen: usually it will also be backed up by an issue - and a discussion that is happening in an issue.  We have (currently) 1935 open issues right now in CSS.  All of these are being discussed across the 60+ specs we have at the moment.  We are rigorous about using tags, cross-linking, etc... 

Peter: agree that that data is there but it's not linked from the specs... 

Alice: I don't want to read a whole thread - i want to read what the decision was and why.

Rossen: i don't quite agree with what Peter said - disposition of comments always has the issues... each issue discussed by WG have WG resolutions that are captured by our bot.  It's not easy ...

Peter: an explainer would help to say what the main points are - for outside reviewers... 

Rossen: could be part of the [new] template... For people preparing a doc for ...

Alice: the template would have links to the important issue and where the decision was summarized?

Rossen: all of our specs have a change list... for each of these changes we can ask for the links back to the discussions...

Alice: I think that's a good start...

Hadley: looking at CSS... we reviewed aspect ratio... fine ... review includes a link back to the applicable repo ... review doesn't point to the specific issues that are relevant...

Alice: could be something we do as an iteration... it might be worthwhile doing a discussion with Tab and Elika to brainstorm ways we can do this in a lightweight way... 

[discussed inviting Tab & Elika to Breakout B for next week]
 
#### [triage design review issues](https://github.com/w3ctag/design-reviews/issues)
