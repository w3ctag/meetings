### TAG Cals week-of Jan 17 2002

## Agenda

### Breakout A (Europe / US) - [2022-01-17](https://www.timeanddate.com/worldclock/converter.html?iso=20220117T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Explain how to decide an interface's Exposed value](https://github.com/w3ctag/design-principles/issues/35) - @kenchris
* [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou
* ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov
* [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober
* [incorporate some of CSS2's design principles](https://github.com/w3ctag/design-principles/issues/188) - @LeaVerou
* [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris
* [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo  
Should we close?

### Breakout B (US / APAC) - [2022-01-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220118T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebGPU](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia  
Planning for how to do review so we can schedule it in for next week.
* [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober
* [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober
* [should provide advice on when it's good to return the same object again](https://github.com/w3ctag/design-principles/issues/46) - @cynthia
* [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober

### Breakout C (APAC / Europe) - [2022-01-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220118T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Special Guest: Léonie Watson

* Accessibility Chesklist / Questionnaire
* [DOM Wide Review](https://github.com/w3c/htmlwg/issues/19)

### Plenary Session - [2022-01-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220119T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

## Minutes

### Breakout A (Europe / US) - [2022-01-17](https://www.timeanddate.com/worldclock/converter.html?iso=20220117T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Kenneth, Yves, Peter, Lea
Regrets: Rossen, Amy

#### [Explain how to decide an interface's Exposed value](https://github.com/w3ctag/design-principles/issues/35) - @kenchris

Ken: don't we have something "always expose things on dedicated worker"?   Some comments from Anne about worklet and service worker - that they are also specialized.

Ken: [325](https://github.com/w3ctag/design-principles/issues/325) is the issue... 

Dan: should we close 35?

Ken: I think the guidance should be "consider exposing things on dedicated worjer"  I also have this feeling - with permission dialogs and selectors just to put something on a worker then maybe it's not worth it.

Ken: with the conclusion and feedbackn 35 it becomes the same issue. 

**closed 35**

Ken: just some guidance that people should consider exposing things in a worker.  There are startup time issues.

Dan: so can you write that into a comment on the issue and get some community feedback?

Ken: I will look at this tomorrow.

#### [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou

Ken: could rewrite what anne said ...

Lea: this is specifcially about the kind of overloading where the argument depends on a previous argument?

Ken: i think any kind of overloading...

Lea: we asked ..  Anne said it's excludes optional arguments.  I'm a bit unconvinced that we should be discouraging this...

Ken: I think i understand - no types in JS - some patterns ...

Lea: the API design should be for the API users... if theres' a problem that should be solved in the JS side.

Ken: confusing for [developers] - where you think you have a string but it's been converted... weird or subtle bugs. You could have a booleon and it turns into a string because it autoconvers values.  Say I have a function that takes a string but i'm giving it a boolean - it works because it's autoconverting. But now I have a function that type-checks.. now my code is working differently. 

Ken: *promoting type checking* .. 

Lea: there are many cases where this kind of overloading has improved the platform - e.g. eventListner. 

Ken: yes. in that case ...  use options and dictionaries... that's the modern way ... that's backwards compatible.  They had [the discussion in TC39](https://github.com/tc39/proposal-operator-overloading) about operator overloading proposal and there were a lot of people arguing against that.  

Lea: can we identify specific types of overloading that are dangerous?

Ken: another option: dictionaries.

Lea: we already have a principle for that. for positional arguments I'm not sure it's universally bad.

Ken: Maybe "be careful with overloading" .. 

Lea: I think the solution is to make overloading easier! 

Dan: overloading: be cautios around these particular areas?

Lea: is this an active

Ken: the tc39 proposal is [not really active](https://github.com/tc39/proposals) now...

Ken: what might make sense is to reach out to tc39... get their opinions...

Lea: useful to get more opinions....   Will add people to the isusue.

#### ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov

**marked as "write me"**

#### [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober

Dan: open issues 175 174 169 remain...

Re: [174](https://github.com/w3ctag/design-principles/issues/174) (backwards compat) / support existing content.

Lea: I think a lot of the [HTML principle](https://www.w3.org/TR/html-design-principles/#support-existing-content) could be re-used. It should be expanded to cover CSS and JS as well.

Lea: this would be in "principles behind the design of Web APIs"


**working on this**
```
Support Existing Content

Existing content often relies upon expected user agent processing and behavior to function as intended. Processing requirements should be specified to ensure that user agents implementing this specification will be able to handle most existing content. In particular, it should be possible to process existing web content in current user agents and get results that are compatible with the existing expectations of users and authors, based on the behavior of existing browsers.

Content relying on existing browser behavior can take many forms. It may rely on elements, attributes or APIs that are part of earlier  specifications, or on features that are entirely proprietary. It may depend on specific error handling rules. It may depend on certain method names not being defined. In rare cases, it may even depend on a feature from earlier specifications not being implemented as specified.

When considering changes to legacy features or behavior, relative to current implementations and author expectations, the following questions should be considered:

* Does a significant quantity of existing content depend on the feature or behavior?
* Does any of the dependent content occur on particularly popular websites?
* Is the dependent content genuinely intended for consumption, rather than occurring solely in test cases or examples?
* Is the dependent content on the public web, rather than found solely on internal sites with a controlled user environment?
* Does the dependent content currently work as intended in multiple popular user agents, rather than explicitly targeting only one particular user agent? 

The benefit of the proposed change should be weighed against the likely cost of breaking content, as measured by these criteria. In some cases, it may be desirable to make a nonstandard feature or behavior part of the web platform, if it satisfies a valid use case. However, the fact that something is part of the web platform does not by itself mean that relying on it is condoned or encouraged.
```

Lea: *opens a PR*. [354](https://github.com/w3ctag/design-principles/pull/354)

Dan: let's try to land at the plenary.

#### [incorporate some of CSS2's design principles](https://github.com/w3ctag/design-principles/issues/188) - @LeaVerou

**We go through the CSS design principles**

Lea: fwd and bkwd compat we have that; accessibility we have that; 

Dan: nothing jumps out at me.

Peter: not much to add...

Dan: I think we're good - i think we should close.

Lea: **leaves closing comment**

#### [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris

**punt to plenary**

#### [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo  
Should we close?

Dan: is this worth writing.

Lea: yes - this was a cause of developer pain.

Dan: could we do a sentence or two?

Lea: a sentence or two with a few examples.

Dan: ok we need someone to take this.  We can try to assign at the penary.  

### Breakout B (US / APAC) - [2022-01-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220118T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Max
Regrets: Rossen

#### [WebGPU](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia  
Planning for how to do review so we can schedule it in for next week.

Added Max to issue

#### [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober
#### [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober
#### [should provide advice on when it's good to return the same object again](https://github.com/w3ctag/design-principles/issues/46) - @cynthia
#### [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober

### Breakout C (APAC / Europe) - [2022-01-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220118T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Special Guest: Léonie Watson

Present: Dan, Max, Sangwhan, Léonie
Regrets: Hadley

#### Accessibility Chesklist / Questionnaire

**reviewing state of current early draft for Léonie**

Sangwhan: idea is a basic questionnaire to ask 7 questions.  

L: should get james falkner, steve... get a few people that the a11y community know to endorse... this will have to go to APA - accessible platforms architecture group.  Position it to alleviate the pressure on horizontal review.  Emphasizing that it's had input from people in the a11y community.

Dan: Note or more informal document?

L: suggest keeping it informal.

Sangwhan: my thoughts were to pilot it as an informal document... does this solve any problems - does it reduce the workload of APA?  If there are positive signals we can make a path to make it more official.... make it more exhaustive. 

L: keep this about the TAG design review process but "we'd welcome your comments and input" (message to APA).

Dan: we could put it in GitHub ... invite issues and PRs.

L: Yes. I also suggest having a meeting with APA group co-chairs.

Sangwhan: i think it would be best in a separate repo - makes it easier to isolate issues and PRs.

L: but make it clear that it's part of the TAG review process.

Sangwhan: it will be part of the issue template.

L: other good reason to keep it in TAG space - more traction [with wider community].

#### [DOM Wide Review](https://github.com/w3c/htmlwg/issues/19)

**need for more security /privacy review of DOM / HTML**

L: In 2019 PING said they would like a security section added to DOM spec... whatwg editors said no.  They called on HTML co-chairs to facilitate.  I said "with your best judgement does anything in DOM spec impact privacy / secuirty" he said no and that was that. But now we've raised it again. Nobody is raising privacy issues but they'd like a section added that says that. There may need to be a more detailed security review.  WhatWG has a backlog.  question of who's responsibility it is to raise such a PR... reached a bit of an impasse.  Not officially escalating to the TAG just seeking opinion.

Sangwhan: certain parts of HTML spec we might want to do security review - workers come to mind. Some concerns abiut security especially about shared workers.  Storage warrants a security review.  Specific sections.  But not the whole thing.  

L: we could do what we did when HTML5 was going to be released.. with implementation experience we assume that everythung already existing has implementation experience.. Look at new features.. named date range.

L: in a11y they've gone though the commit logs between one review and the next.

Ken: Tess filed some issues ... 

Sangwhan: it's easy if there's an isolated feature and an intent to implement. 

L: With HTML there's another problem.  A concern about the reporting API...  A number of privacy / security issues opened against it. Security / PING asked Whatwg editors to put a warning in. They've said they won't do that. That's blocking HTML. 

Dan: noting that we did a [review on reporting](https://github.com/w3ctag/design-reviews/issues/585) and we were satisfied including security & privacy concerns. We could hold a special session if warranted.



### Plenary Session - [2022-01-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220119T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Dapeng(Max), Rossen, Peter, Hadley, Lea, Yves


#### Breakout Rollup

##### Breakout A

Dan:

Issue 35: closed. Became redundant to 325. Ken was going to write some stuff — which [he did](https://github.com/w3ctag/design-principles/issues/325#issuecomment-1015374609). We need to look at it and see if we like it enoug hto make a PR. Had feedback from Chris Needham from the BBC. We can circle back to that.

Discourage overloading: Was Lea's issue. We discussed is overloading that bad? In somce cases, it can make syntax easier, can mean good things for the developer. We agreed to each out topeople at TC39 on this, haven't heard back.

154, cheat sheet: This needs to be done, and is marked as write me. I forget who said they would do that. Lea, I think? It's in the issue.

160, incorporating a generationalisation of the HTML design principles into our design principles. We iterated on backward compatibility, and thought it was in our doc but it isn't. We all assumed it was there.

We drafted proposed text, and Lea opened [PR 354](https://github.com/w3ctag/design-principles/pull/354). We can look at that... let's circle back to it after the readouts.

We talked about incorporating CSS2 design principles, but a lot of it is already accounted for. Lea closed the issue.

WE didn't talk aobut the monkey patch issue. We can discuss today.

Avoid non-deterministic behavour: we didn't have time.

##### Breakout B:

Max got assigned to the WebGPU issue, correct?

Max: yes, I'll talk to Sangwhan offline to discuss the detail.

Peter: neither Tess nor Sangwhan was on the call.

[discussion of conflicts to meetings this week]

##### Breakout C:
We had a guest, Léonie Watson. Discussed the accessibility checklist, came up with a plan: not going to write a full secuirty and privacy questionnaire style TR-space document. WE'll keep it informal, as a markdownw documet in TAG space for now.

Léonie suggested we reach out to the Accessible Paltforms Architectures chairs for their input. She would introduce us, and that would be smoothest way to make this part of our issue templates for when people open design reviews.

DOM-wide review: a lot of issues bubbling between W3C HTML WG and WHAT Wg. No need for TAG to get involve dat this point. Isseu on the reporting API: some people in the W3C community wanted an issue marked in the WHAT WG document and the WHAT WG people were pushign back. WE had reviewed it and were satisfied with secuirty/privacy.

##### [PR 354](https://github.com/w3ctag/design-principles/pull/354)

Lea: this is close to the oroiginal text in the HTML design principles, but we made it bit broader for the web platform.

Dan: we need to get more feedback from others. 

Peter: 'This specification' wording doesn't make sense here.

Hadley: balance against the evergreen web finding - this could be constued as "the way it works is the way it should always work".  the evergreen web discussion - the web is continually improving - UAs should continue to evolve.  This PR should be balanced with discussion of evergreen web.  There are times when we need to say it's really important for things to move on. 

Torgo: yes. This is taking text from the HTML principles, and it does not include that nuance. Maybe it should? 

Hadley, can you suggest text?

Hadley: I feel like I haven't been involved in the discussion. I'd like to catch up a bit more.

Torgo: And Tess should be involved. We don't want to undermine the original intent, to demonstrate how valuable backward compatibility is. You're right, other people might assuem there is a contradition there.

I'll put it on the agenda for next week.

Hadley: that would be great.

##### [Guidance about exposing on Window vs Worker only (and other contexts)
](https://github.com/w3ctag/design-principles/issues/325#issuecomment-1015374609)

Torgo: Ken wrote up a principle for this. What do we think about this? And should we ask Ken to put it into a PR that we can try and land next week?

Peter: we talked about feature detect in a worker even functionality isn't available in the worker... good for workers to know it's evailable in the main thread...   Method would be present but it would be [non functional]... 


#### Next week

Torgo: We have unfinished issues from B. And I'll put webGPU on for next week.

#### Issue Triage

