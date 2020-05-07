k
# W3C TAG Design Principles Week
## Week-of 4-May-2020

### Call Agenda [on Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/05-04-agenda.md).

### Breakout A (Europe / US) - [2020-05-04](https://www.timeanddate.com/worldclock/converter.html?iso=20200504T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [security & privacy Self-check](https://www.w3.org/TR/security-privacy-questionnaire/)
  * [open issues](https://github.com/w3ctag/security-questionnaire/issues)
* [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron
* [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111) - @hober, @kenchris
* [Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112) - @dbaron, @kenchris

Present: Dan, Tess, David, Rossen (part), Peter

Regrets: Kenneth, Yves

Chair: Dan

Scribe: David

#### [open issues](https://github.com/w3ctag/security-questionnaire/issues) on security and privacy self-check

Dan: thought it would be worth assigning open issues

Tess: who's editing it?  Had a TAG editor and a PING editor... neither of whom are in their respective groups anymore.

Dan: Lukasz sounded willing to do additional work on this, but probably need an editor in the group

Dan: At the same time, we can get work done without knowing who the editor is.

(Tess volunteers to be editor)

Tess: PING has a call on Thursday; I'll bring it up there as well.

Dan: I'd also be happy to email PING chairs.

Dan: Doesn't appear to need major work today.

Tess: [#71](https://github.com/w3ctag/security-questionnaire/issues/71) looks like a simple edit that someone can make; I'll do that.

Dan: I should set up milestones in this repo, offline later.

Tess: [#61](https://github.com/w3ctag/security-questionnaire/issues/61) on geofencing link is not helpful... might be a simple edit, need to look.

Tess: The point of the proposal still stands... it's still tied to service workers and therefore restricted to HTTPS.

Dan: Maybe another example that could be swapped in to something not defunct?

Tess: Status quo seems fine.

(Dan adds comment to issue, assigns himself)

Tess: The remaining issue is [#48](https://github.com/w3ctag/security-questionnaire/issues/48), on whether dropping the feature should be a mitigation strategy.  From a longstanding disagreement.  Was some useful discussion.  I think there's an edit to be made that would provide some nuance, combining most recent comments from jyasskin and dbaron.  I'm happy to take a stab at it.  That said, I had a clear strong opinion on one side of this disagreement, so I'm maybe not the best person to take it.

Dan: I think that's fine, rest of TAG can review.

Dan: Peter, do you have an auto-milestone-creator?

Peter: no

Dan: OK, I'll add milestones.

Dan: Doesn't seem like major work is needed, but seems worth having an active editor from both TAG and PING sides.


#### [New principles related to private browsing mode and assistive technologies. Fixes #97.](https://github.com/w3ctag/design-principles/pull/167)

Tess: This was waiting on 1:1 between me and Alice, repeatedly rescheduled, but should happen later today.  Or we could noodle on it on this call.

Dan: Can wait, should we add to agenda for breakout B?

Tess: Yes, we're meeting right before that.

#### [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99)

David: something I have opinions on

David: there's a proposal - no consensus yet (Dominic still disagrees)

Dan: Maybe noodle on it more?  Can we get folks to agree.  Others we could bring in to conversation?  Other ideas?

Tess: broadly sympathetic to David's point

Dan: David, maybe reiterate the original idea and ask again?

#### [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111)

Tess: Assigned to Kenneth and me... but I haven't read it yet.  Should talk about it when Kenneth and I overlap... but I should read it sometime today.

Dan: Maybe pick it up in the plenary call?

#### [Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112)

(Dan reads history of issue)

Dan: We can postpone to "face-to-face".

#### Other topics?

Dan: should we pull anything in from breakout B?

#### [Discourage device enumeration, prefer less powerful alternatives](https://github.com/w3ctag/design-principles/issues/152) - @hober

Tess: I still haven't written a PR for it; would like to.  Not going to happen by breakout B, though.

#### Other topics?

Dan: HTML design principles?

Tess: David filed three new issues ([#173](https://github.com/w3ctag/design-principles/issues/173), [#174](https://github.com/w3ctag/design-principles/issues/174), [#175](https://github.com/w3ctag/design-principles/issues/175)) on HTML design principles based on conversation with fantasai.  I've added them to my to-do list.  Alice has opinions on [#169 separation of concerns](https://github.com/w3ctag/design-principles/issues/169).

Dan: Also [one on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172); should we assign it?

David: I could take it

Dan: Also [ Considerations and pre-cautions when adding new media formats #171 ](https://github.com/w3ctag/design-principles/issues/171), came out of discussion on AVIF decode.  I could potentially take it.  Though not sure if it belongs in design principles document.  Let's discuss in the plenary.

Dan: There's one more unassigned [generic advice about preferring booleans, and maybe advice on boolean versus string versus enum #170](https://github.com/w3ctag/design-principles/issues/170).

David: Not sure if there's actually something here, though, but can take it.

### Breakout B (US / APAC) - [2020-05-04](https://www.timeanddate.com/worldclock/converter.html?iso=20200504T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### Triaging [promises guide](https://github.com/w3ctag/promises-guide) [open issues](https://github.com/w3ctag/promises-guide/issues)

Tess: Who is writing the Promises guide these days?

Peter: Domenic has still been involved, but less so lately. 

##### Give guidance on how to migrate void-returning callback APIs to promise-returning #24

David: This hasn't had any comments for 5 years.

Tess: It would be nice to find someone to pick up editing so we have someone to default to...

_general agreement in principle_

_nobody rushes to volunteer_

Tess: Kenneth knows about Javascript...

Rossen: I can step up.

David: This issue is a pretty basic piece of what the guide was intending to help authors do.

Alice: There is a link out to an [issue on encrypted media](https://github.com/w3c/encrypted-media/issues/19) which looks like maybe a good working example.

Rossen: Are there any of these issues we can make progress on now?

##### Add more advice on when not to use Promises #65

Rossen: Peter and Yves were looking at this in Wellington... was there anything else you wanted to add?

Peter: We were looking at the Wake Lock API... their issue #226... looking for examples of things that shouldn't use Promises, because they don't behave Promise-like.

Rossen: Do TC39 have good guidance on this? I'll go and dig in on that. I would assume they've thought through this methodically and ideally documented something in terms of design patterns and recommendations for users.

Peter: I don't know that TC39 has a lot of guidance around Promises... if they have something we should harmonise the two.

Rossen: I plan to go through these issues and figure out what's assignable and assign them to a future breakout.

#### [New principles related to private browsing mode and assistive technologies. Fixes #97.](https://github.com/w3ctag/design-principles/pull/167) - @hober, @torgo

Tess: Alice and I had a breakout earlier today to work on this one and the next one. We landed some changes to address the outstanding comments on it. We think it's ready to merge.

Rossen: Merge it, what's the worst that could happen?

Tess: I enjoy a good YOLO merge on my own projects, but I thought I'd ask first.

Peter: Let's hold off merging until the plenary.

#### [WIP: Attempt to address some of the naming feedback in #132 and #149.](https://github.com/w3ctag/design-principles/pull/163) - @hober, @alice

Peter: Let's hold off merging until the plenary.

Tess: I'll ping Anne to see if he's happy with the latest version.

#### [Prefixing particularly dangerous operations with "unsafe"](https://github.com/w3ctag/design-principles/issues/104) - @dbaron, @atanassov

David: I agreed to write something on this back in March, and I haven't done it yet. Need to describe what it means to be "unsafe".

Mimosa (Peter's cat): *meoooow*

David: Not quite at the top of my list, seems like it will be a little involved...

Alice: Would scheduling a 1:1 with someone to work through the detail help?

David: Maybe...

Peter: New milestone? 

David: Yeah, I have about 5 PRs to review for the plenary already...

Peter: Does anyone want to do a 1:1?

David: I'd be happy to if someone wants to...

Alice: Maybe we should ask for participants at the plenary?

David: sure.

#### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov

Alice: This quote:

> The term "high level" must also be clarified. Over time, esp., with the adoption of the Extensible Web Manifesto, browser vendors have begun focusing on uncovering the "building blocks" that make other higher-level features work. Case-in-point, Web Components aim to explain how high-level markup languages work, enabling web applications to extend or create their own high-level markup languages for distribution on the web. The downside is that the code to power these experiences is not built-in to the browser, and must be downloaded by every client that visits the web site.

reminds me of declarative shadow dom, std:toast, builtin modules. Happy medium is what we want. We don't want to just continue shipping built-in elements.

David: An advantage of high-level APIs is that they allow user agents more ability to intervene in various ways on behalf of the user, e.g. for accessibility or privacy or user preference, etc.

... Low-level APIs gives you room to experiment with what you want for future high-level APIs. This is the extensible web manifesto's vision.

Peter: Also gives you an escape hatch when higher-level APIs don't behave in the way you need them to.

Tess: Worth talking about escape hatches, and also cliffs - if you don't have a well-layered solution, you fall through the escape hatch and off a cliff, e.g. "now I have to do everything in canvas because HTML can't do this thing".

Alice: makes me think about how we know what the happy medium is.  Developer research (e.g., MDN), user research (nobody doing as far as I know).  Something we can have opinions about??

... finding the happy medium is often iterative; have to overshoot and make mistakes.  Maybe a meta-principle about letting the perfect be the enemy of the good.

... I'm happy to try and write something (eventually) but I want everyone else's thoughts on this as well. Still forming my own thoughts.

Peter: Meta-question about what the intention of this issue is... outlining the difference between high and low level? Recommending where APIs target? Rather than telling people to target high-level or low-level, we should be telling people to think in layers. Better if people build a higher level feature in terms of lower level features so that you can compose new features out of lower-level features but still have the higher level features. 

Alice: Working across layers concurrently?

Peter: If designing a new set of features, better to expose lower level features and higher level features and expose both sets of APIs... then we don't end up building the single high level feature that doesn't have the "cliff" problem nor the WebRTC problem where you have to be across a range of technologies to get the feature you want..

David: Often a trade-off between that (?) and other things like security, privacy, accessibility - low-level features may risk one or more of those.

Peter: Guidance may be to design in terms of building blocks, but that the lower level building blocks may not be able to be exposed... that may guide decisions on how "high level" the API needs to be.

... If you do need to cross these lines (?), build things in a more isolated granular way that doesn't expose everything.

Alice: I'll take point on this, but would be helpful if folks can comment on the issue with concrete examples of APIs that are good and bad on this axis.


#### [add a section describing what should be in html versus css versus javascript (the separation of concerns)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

Tess: One of the principles in the HTML design principles doc is separation of concerns, I've been doing this project of taking one at a time and fitting into a modern design principles doc. David filed this, I'd love to head his summary of it. A little different than taking what was in the old doc and putting it in the new one.


David: Started to write something in the section I was adding on CSS... this was more complicated than what I'd written so I pulled it out. Not clear how well we're still able to do this. Things that happen on the web today ... sure, Gmail has html and css and JS out, but is gmail going to work if you take the CSS out?

Tess: Is separation of concerns about independently enabling and disabling those technologies, or is it about something else?

... Would gmail work if you disabled CSS, is that relevant to the question of where a feature belongs?

... Some other examples are things where we know we got it wrong...

David: The principles are more relevant for documents than they are for applications... fantasai disagreed.

Tess: Hoping for some thoughts from Alice on this.. thoughts on how this intersects with assistive technology.

Alice: This has come up a lot with CSS in particular:  there seems to be a misunderstanding of "semantic".  People expect the HTML to completely encompass the document/application semantics.  My view is that semantics don't work like that; semantics are what the user understands of the application.

Rossen: which people expect this?  (long-ish list, including people producing documents, consuming documents, working on CSS, HTML, JS, etc.)

... I agree with you; it's a large pain point for all these groups.  CSS is trying to reinvent HTML inside, add functionality that could be in JS layer.

Alice: examples?

Rossen: producing HTML elements versus boxes...   Houdini.

Alice: goes back to higher level versus lower level API thing.

Alice: I was mostly thinking... the strongest arguments I've had with CSS folks about text-transform... assistive technology users want the transformed text.  Demonstrating a gap in user research; we ask our friends.  Might get a different answer if we did actual user research.  People say CSS just meant to be for presentation, but we can't escape from presentation being semantics.  This also came up with flex ordering.  There's language in the spec that flex order is for visual order only, not logical order (but no distinction between those two things).

Rossen: Meta point that's important here is: can we have some sort of succinct recommendation or guidance for altitude of what you're trying to do and where it fits best.  What should be declarative API versus an event.  Some things are intuitive; some are awkward and could fit anywhere -- what's the best place?  That's how I understand this recommendation.

Alice: This also comes back to declarative shadow DOM issue.

Alice: schedule time to continue this discussion?  4 assignees?... and Peter

### Breakout C (APAC / Europe) - [2020-05-05](https://www.timeanddate.com/worldclock/converter.html?iso=20200505T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

####  [How should the toJSON method be used?](https://github.com/w3ctag/design-principles/issues/116) - @cynthia

Ken: usage is really mixed - seems to be a long discussion...  Very inconsistent on the web platform...

... seems to be really about serialization... 

... this is pretty big... 

Dan: if there is not a clear cut best practice we can bring into the principles doc we should drop this.

Ken: It seems to make sense...

Dan: can you ping the issue and see if the author has any further thoughts?

Ken: I will read through it...

####  [Best practices for feature detection?](https://github.com/w3ctag/design-principles/issues/137) - @torgo, @ylafon, @kenchris

Ken: we should find the ways things have been done - e.g. looking whether a namespace exists, where an object exists, sometimes has to do with permissions requests (e.g. pan/tilt/zoom)... 

Dan: media queries as well..

Ken: for CSS feature detection.  In CSS you also have `supports` 

... should we rename this to feature description in javascript / DOM.

Yves: in JavaScript

Dan: Ok

Yves: some advice comes from the promises guide - there may be some interlinking there.

Ken: we need to figure out how it's done to today, why and pros and cons.

Alice: what about HTML or DOM?

Dan: privacy

Ken: in some cases people have been arguing that the namespace should always be available so it cannot be used for fingerprinting, even if the feature is not actually available.

Ken: you should - if the feature is available in the browser it should be exposed. Don't hide anything because you don't have access. Then it should fail with a promise if you don't have access.  Not sure if that's the right approach or not.  Not sure if it avoids the fingerprinting. It makes it more complicated...

... we don't want any difference between incognito mode and normal mode whether those objects exist.

Dan: but they might fail in incognito mode...

Ken: but they might fail for certain web sites...

Dan: We should include: "Feature detection is a commonly used approach to browser fingerprinting. In order to mitigate against this, we recommend ..."

Ken: also how it should operate in incognito / privacy preserving mode...

Dan: let's agree some text in the f2f

Ken: yes but we need to gather examples...

Dan: who to ping... 

Dan: [pings andrew betts]

Ken: maybe we do need multiple ways of doing it...

#### Discussion of Promises Guide Issues

Dan: Should promises be in the principles doc?

#### Discussion of CSS Principles

Alice: some discussion of whether there should be a separate guide ....

[discussion of whether we should move the principles doc into one big doc or separate docs...]

Alice: part of API design is deciding whether it fits [from David]

Alice: the question is: how do we make the design principles doc tractable while also including a lot of detail - including tech-specific detail like promises and css principles. How do we make sure it's consistent -- having an overview would be good.  How to make sure it has enough advice... How do we apply those principles ourselves... 

Dan: we need a way to make the design principles more accessible / readable / digestible...

Alice: I will make a design principles issue on Information Architecture for the design principles document...

### Plenary Session - [2020-05-06](https://www.timeanddate.com/worldclock/converter.html?iso=20200506T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Peter, Tess, Alice, David

#### Breakout Rollup

##### Breakout A

**Open issues on security and privacy self-check**

Dan: Coming out in discussion of PRs to follow

Tess: Decided I should take over editing this for the TAG side, and ask PING who should edit from their side. They responded: Pete Snyder. Yves seems to have [added him](https://github.com/orgs/w3ctag/teams/security-questionnaire-collaborators) into the repo.

Dan: I'm glad we got that result!

**Partial a long term maintainability problem?**

David: I'm going to write something on that.

**Guidance on inheritance between contexts**

Dan: Were going to pick this up in this call..

**Handover access to sensors and devices...**

Dan: ...

**Discourage device enumeration...**

Tess: Device enumeration issue... been in my to-do list of PRs for a long time. Did start it today, made a dent in it.

**Other topics**

Dan: New issues filed on HTML design principles...

Tess: New issues that David filed incorporating HTML design principles, based on feedback on a different pull request of his. Is that roughly right, David?

David: yep

Dan: We triaged out those issues...

##### Breakout B

Tess: First thing was triaging open issues on **promises guide**. Ended up getting Rossen to agree to take over the Promises guide, and I assigned all the issues to him. Triage DONE.

... Talked about a bunch of those issues.

... Talked about two **pull requests** that Alice and I had had a breakout to look at two PRs, we didn't minute that breakout. We think the PRs are ready to merge, these are on the agenda for later.

Dan: Meta-topic in breakout A... eventually merge the promises guide into design principles? Then we have one design principles doc... comes with issues...

Tess: **Prefixing dangerous operations with `unsafe`**... this has been on David's todo list for a while. We need to schedule a dedicated break-out on this.

Dan: is that assigned to the face to face? 

Tess: I don't remember.

Dan: Let's schedule it for then.

Tess: Next talked about **high level vs low level APIs**.

... This was a long, interesting, involved conversation.

Alice: I am taking this one, but need good and bad examples.

Tess: **Separation of concerns** principle.

... Came out of David's work on CSS section. All four assignees ended up in Breakout B. Used the rest of the breakout to talk about that, ran out of time, scheduled a sequel breakout for "tomorrow".



##### Breakout C

Dan: **toJSON**.  Ken is going to read through it. Assigned to f2f.

... **Feature detection** - Ken sent out a [tweet](https://twitter.com/kennethrohde/status/1257594461728788481), it's had 22 RTs and 28 likes. Trying to gather additional feedback on how folks do feature detection in practice today.

... Ken is going to write some things out before the f2f.

... Then talked about rolling the promises guide into the principles doc.

... Alice filed [an issue](https://github.com/w3ctag/design-principles/issues/177) on the principles doc about information architecture - could pick that up at f2f. Make some decisions about multiple docs, how to find relevant information, promises guide, how to make principles doc more approachable for first-time readers... TikTok version (dan lip synching the design principles guide)

#### Design Principles: Merge any outstanding PRs as possible & issue update

Dan: Let's merge these and then we can issue an update.

##### PR: [New principles related to private browsing mode and assistive technologies](https://github.com/w3ctag/design-principles/pull/167) - @hober, @torgo

Tess: We came up with three new principles... Dan and I worked on text, David reviewed, Alice reviewed and we ended up with the current change in this PR. Dan, David and Alice have approved.

Dan: What changed since I did my review?

Tess: Only three commits, so the original commit is the one you and I worked on together, then the next two are follow-ups.

David: The middle one is more substantive

Tess: David pointed out some places where additional nuance was needed, and I used his suggested wording directly.

Tess: Third change was nits and typos.

Dan: Motion to merge. 

All: Aye

Dan: _merging noises_

##### PR: [Naming things: expand language around the use of common words, brevity, wide consultation, and future-proofing](https://github.com/w3ctag/design-principles/pull/163) - @hober, @alice

Tess: Alice and I wrote the first draft of this in Wellington and we got a lot of discussion and feedback on it from Rossen, Anne, David... 

Dan: This is a noted problem in computer science

tess: Yesterday Alice and I went through the discussion and added a couple more commits to address those comments.

... Resulting diff adds section headings inside the naming section because there are many different pieces.

... Expands on some wording Rossen had added around easily-readable names in English, given web developers don't always speak English as a first language.

...Favouring readability over brevity... over the courses of the discussion cases where there is reason to prefer shorter names, e.g. using a common term of art for a specific standard technology (JSON).

Dan: You linked out to Tantek's URLs doc?

Tess: Yeah. We expanded on "consult widely", provided tips on how to do that e.g. looking at libraries, other parts of the web platform. Tips on how to do naming research.

... Had added a point about names not being related to brands... came up with some examples.

... Parts of speech ... making sure the name is consistent with adjacent/related names. 

... Commonsensical naming advice.

Dan: I took a look while you were talking ... looks good to me. Motion to merge.

Peter: Do we want to say anything about searchability... want to name a property with some name that is not "Googleable". 

Tess: Worth saying something, but can probably happen in a follow up patch.

Peter: I'll log an issue.

Dan: SQUASH AND MERGE

David: Searchability often comes up in CSS when talking about a symbol vs. a function...

Peter: Comes up with English words too... searching on this common word...

Dan: The merge is done. I'll ask Yves to publish the document into our space and send an email to the AC list and the chairs list, talking about the update. I'll write that email. Then we can do some Twitter promotion.

#### Security & Privacy Questionnaire

##### PR: [Add some nuance to 'drop the feature'](https://github.com/w3ctag/security-questionnaire/pull/72) - @hober

Tess: Once we merge one of these PRs the other will be a pain to merge, just as a heads up, cause the generated bikeshed file is checked in (??)

.. Some wording around the "drop the feature" mitigation. This came out of [issue #48](https://github.com/w3ctag/security-questionnaire/issues/48).

.. Sangwhan suggested that this mitigation be removed, I disagreed. This was early last year. The issue produced a lot of discussion and identified some interesting nuance. What should you keep in mind when considering removing something. Lots of thoughts from people.

... I last recall looking at this in Reykjavik, some good comments from Jeffery Yasskin and David Baron which got to a lot of that nuance. This PR attempts to add that nuance.

... Diff looks a little funky because I changed the newlines while I was doing it.

... Used to say "simplest way to mitigate is to remove the feature"... now notes that security & privacy features may be added or removed by adding or removing features.

... Chunk of text which is new, saying consider the cumulative effect of feature addition. David's text about "should be safe to visit a web page", need to take the totality of user experience into account.

David: seven subsections of this section, two of them don't really belong.

Tess: Need to take a high level pass.

... David approved, but David has been the only reviewer. Lukasz and Pete Snyder approved the change in words, but not "officially" via GitHub.

Alice: Some language around being clear about the problem being solved (as a follow up)?

Tess: Something along those lines would be good, since this is typically being used as part of a dialogue - "remove the feature" is in the context of the problem the feature is intended to solve.


##### PR: [Clean up bikeshed source](https://github.com/w3ctag/security-questionnaire/pull/76) - @hober

Tess: ... _long discussion of bikeshed specifics_

Dan: In the email I'm sending, I should note the update to the security and privacy questionnaire, in particular the new joint editors.

David: Security and Privacy questionnaire is in TR space now... are we going to update it there?

Tess: Ok, so I'll squash and merge, then Dan will talk to Yves to do the TR space stuff.

Dan: Then I'll send out the email. Should be just one email about both documents. Kind of gated on squashing and merging.


#### [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171)

#### Any action on other docs?

#### Issue Triage

### Separation of Concerns [#169](https://github.com/w3ctag/design-principles/issues/169) breakout

Present: Alice, David, Peter, Tess
Scribe: Tess

Alice: fantasai's point about alternate styling is critical. For me, it's less about semantics going in HTML and styling in CSS. I need to circle around the idea a bit. David said:

> If non-visual consumers of a page (such as search engines or screenreaders)
seem likely to need the information (at least for well-designed pages),
then it probably belongs in the markup rather than in the CSS.

Alice: I think combining screen readers and search engines here doesn't work. ...scribe missed...

Peter: I don't think a screen reader that ignores CSS is doing anybody a service

Alice: very few ATs interact directly with the DOM; they interact with an accessibility tree which is built after CSS is applied. That process is still being refined. Old Edge built it off of the DOM tree instead of the layout tree. The accessibility tree is not a function of the dom tree, it's a function of the rendered page. It represents what is laid out. We don't assume any AT user can't see the page. Most can.

Peter: Sometimes presentation is semantic. The line between these things is a bit blurred. There's no simple hard line between the two. Just like in voice, tone is presentation but also conveys meaning.

David: The things we think of as semantic in HTML some other people think of as presentational.

Tess: possible strawman conclusion to disagree with:  we agree the line is hard to draw.  The naive version of this idea doesn't work.  But there is a difference.  Part of the web being a higher quality system is having each component well defined in its own sphere, interfacing with the other ones.  None of us are advocating for "put the semantics in CSS and the presentation in HTML".  There's a line, we just think it's nuanced.

Alice: Perhaps we want to guidance -- David's first paragraph on how to decide in which language a requirement should be addressed.  There isn't a hard and fast line but we can give guidance on how to make the decision.

Alice: Content in CSS pseudo-elements seems like a misfeature, an example where this has failed.

Peter: Ripe for abuse, but not necessarily wrong.

Tess: I think I agree with both of you -- if web components had existed before CSS `content`, we wouldn't have done the `content` property that way -- we would have done something where the pseudo-element is implemented using shadow dom, and the shadow dom contains the content.  CSS would have had styling information about the pseudo element and ...

Peter: probably true... but you can put semantic information in a background-image.  Or the content in the pseudo-element could be purely decorative.

Alice: Sounds like it's one of the things on the fuzzy line.

David: I think the original use cases that motivated `content` were these two:

1. the `<q>` element's automatic quoting rules - bad idea, esp. in multiple languages
2. list numbering. this is right at the fuzzy line.

Peter: also leaders (ToC entry dot dot dot page number) is commonly implemented with a pseudo-element and the `content` property.

Tess: maybe talk about some obvious examples instead of borderline ones?

Alice: The "EXAMPLE:" text in HTML text being in a pseudo-element is clearly the wrong side of the line to me.  Can't search for it.

Tess: Tangentially, maybe the non-searchability is a browser bug?  Agree that it should be in the page... but that seems like a browser bug.

Peter: There are examples where you don't want the generated content to be searchable.  Maybe `content` should have a knob that says whether it's presentational.

Tess: I think the `<font>` element was an example that shouldn't have been in HTML.  (Predated CSS.)  If you're writing HTML and want a different font, you should ask why, and use the appropriate HTML element for that reason.  On the other hand, maybe we want modern examples.

Tess: I was thinking about the directionality stuff -- there are some bidi things probably wrong between HTML and CSS.

David: I think fantasai likes that example, that a bunch of CSS stuff related to bidi shouldn't have been in CSS, but only in HTML.

Alice: `<article>`, `<main>`, etc., the structuring elements that aren't used much -- are those useful to guide this conversation.  They didn't come with any default rendering -- perhaps why nobody used them.  Default styling might be something to consider as part of this conversation.  The lack of default styling leads to underuse -- but harsh default styling for `<button>` is why nobody uses that.

Tess: Maybe that should be an HTML design principle -- new elements should have useful default styling, but it shouldn't be difficult to undo.  Then this principle (living outside of either HTML or CSS section), should point to HTML and CSS principles including this one.  But I don't think that reads directly on the separation between HTML and CSS, but rather on what makes an HTML element more likely to succeed in the wild.

Peter: I think also goes back to our talk about layering.  `<button>` is a high level thing -- you get all or none of it, can't separate the pieces.

Tess: so when you rebuild it you miss pieces.

Alice: I'm trying to gather related things together -- don't think it's the line described in original separation of concerns.

Peter: Also separation of Javascript -- declarative versus imperative.

Alice: Goes back to declarative shadow dom that we discussed earlier.  Not a good user experience to gets a page that looks interactive and isn't.  Progressive enhancement is part of this discussion.  Page loading is part of this discussion.  Progressive enhancement in the sense of creating a good experience in a range of contexts with a range of different data needs.  We've moved on from idea that screenreaders operate purely on HTML with no CSS and JS... but how do you use the fact that we have these 3 separate languages to make a better user experience, taking the user's context into account?  We don't see any of them as optional in actually using a page.

Tess: I think sometimes there are... I don't know how common disable Javascript browser features still are.

Tess: We have 3 languages comprising the API surface.  When you're developing a web site/application, you have to make decisions how to build/architect your site to best serve your users, across variety of devices/browsers/network conditions/etc.  One thing we might say is: use the best tool for the job.  Per job, which is better suited?  If you pick one of the other ones, you often end up with a lot of pain.  Modern JS libraries that avoid CSS sometimes deliver enormous library delivering a partial version of CSS that doesn't work for RTL.  Would have avoided problems if they used the appropriate tool for the job.  Helping people figure out the right tool for the job -- figuring out what are these 3 things best at.  Not what they're designed for or meant to do, but what they're best at.  Might be things that one of them is supposed to do and allegedly does but we actually do it elsewhere for practical reasons (e.g., performance).  For example, `@viewport` didn't go anywhere, probably since not available in the first network packet (unlike `<meta name=viewport>`).

Alice: A feature of HTML is that it's the first resource you get.

Peter: Maybe instead of describing as 3 separate boxes, describe as the layering that they bring to the platform.  HTML brings structure, meaning.  Relies on CSS to bring proper presentation, JS for interactivity.

Peter: I think we're going into tangents of advice to page authors, but here we're trying to give advice to spec authors.

Alice: Though whenever we have to give advice to page authors, we should question why we need to give that advice.

Peter: ...  ...  Maybe ties back into high versus low level aspects.  Maybe a better way to explain this.

Alice: I'm interested to revisit Tess's point about what the languages are good at.  Maybe path to guidance for spec authors.

Tess: Random examples:
* both CSS and JS have selectors - for styling or searching.  HTML doesn't.  (We don't have XSLT.)  Shadow DOM v1 slotting isn't powerful enough.  Does your feature need to identify arbitrary sets of elements?  If so, use selectors, thus use CSS or JS.  (But not in the value slot in CSS.)

Alice: Interactivity is interesting point -- no real interactivity without JS, except for forms (limited).

Peter: HTML forms, and CSS, have some limited interactivity.  Once upon a time we were trying to explain all of HTML's interactivity in CSS.

Alice: `inert` was an interesting one -- controversy where it could live.  Could have ended up in any of three.  Custom elements another can of worms.  `inert` ended up in HTML for ergonomic reasons.  Straightforward to add tabindex attribute -- could have ended up in CSS but would have been more granular, but didn't want it granular.  CSS already has `pointer-events`, `aria-hidden` is in ARIA -- wanted combination of those 2 things plus untabbable, bundled together.  If in CSS would have been not bundled.

Tess: I think this is a good example .  A similar but simpler case is the `hidden` attribute in HTML.  We already had `display:none` before `hidden` was proposed.  We could already make things go away visually.  The debate around the `hidden` attribute -- the argument was made -- originally argument for `irrelevant` attribute that would have the same effect.  The fact that a subtree is irrelevant right now is semantic.  So it was capturing something meaningful about the content that happened to be implemented using `display:none`.  With `inert` I think you could make a similar argument -- that the subtree is inert is semantically interesting about it.  It might contain elements that are normally interactive in some way -- but because it's inert, none of those things work.  There's something about this tree that causes all those effects.  I think `pointer-events: none` is probably an example where we did this wrong -- it is in the gray area, but it's so weird.

Alice: It's using the CSS selectors feature.

Tess: Enough of a smell -- probably not a good enough reason to add it to CSS.

Peter: But sometimes that is the right answer.  The `hidden` attribute has semantic value to the content -- the behavior you get comes from CSS (UA stylesheet).  Maybe all `inert` should be is an attribute, and the behavior comes from other aspects of the platform, maybe CSS.  Another angle on this is what's an attribute versus what's a property.  exposed to CSS this way versus Javascript that way.

Tess: Also i18n concerns:  reason for element rather than attribute is needing to tag language and directionality.  So a case where the right tool is markup -- 

David: i18n WG has guideline about not putting text presented to users in attribute values.

Tess: We should probably reference that in an HTML section.

Tess: Have we  gotten closer to understanding how to write separation of concerns for the modern world?

Alice: Yes, but not done.  I'll spend next hour rereading this and try to pull out key facets and add comment to the issue.

Alice: Point about what languages are good at, problematic and good cases that we came up with.  Those are main things we did today -- hopefully we can add to those buckets, and maybe do more of this brainstorming at face-to-face.
