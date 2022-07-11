## Call Agenda


### Breakout C (APAC / Europe) - [2022-07-05]

* [overloading](https://github.com/w3ctag/design-principles/pull/372)
* [restrictions](https://github.com/w3ctag/design-principles/pull/363)
* [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366)
* [Ethical Principles](https://github.com/w3ctag/ethical-web-principles/issues) triage issues
* [Societal Impacts](https://github.com/w3ctag/societal-impact-questionnaire) open issues including [evidence](https://github.com/w3ctag/societal-impact-questionnaire/issues/7)
* [Contributing tips missing in README](https://github.com/w3ctag/design-principles/issues/373)
* [identity](https://github.com/w3ctag/design-principles/issues/324)

### Breakout B (US / APAC) - [2022-07-05]

* [monkey patching](https://github.com/w3ctag/design-principles/pull/355)
* [Guidance about serialization](https://github.com/w3ctag/design-principles/pull/367)
* [Security & Privacy Questionnaire](https://github.com/w3ctag/security-questionnaire) open PRs and issues
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370)
* [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16)

### Breakout A (Europe / US) - [2022-07-05]

* [backwards compatibility principle #354](https://github.com/w3ctag/design-principles/pull/354)
* [what to do when a feature is temporarily only available on some platforms](https://github.com/w3ctag/design-principles/pull/357)
* [grammar suggestions](https://github.com/w3ctag/design-principles/pull/374)
* [New principle: the simple syntax should not be doing the harmful thing](https://github.com/w3ctag/design-principles/issues/375)
* [New principle: Deployability and Monitoring](https://github.com/w3ctag/design-principles/issues/368)
* [New principle: Remove deprecated functionality responsibly](https://github.com/w3ctag/design-principles/issues/361)
* [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369)

### Plenary Session - [2022-07-06]

## Minutes

### Breakout C (APAC / Europe) - [2022-07-05]

#### [grammar suggestions](https://github.com/w3ctag/design-principles/pull/374)

Reviewed and merged.

#### [overloading](https://github.com/w3ctag/design-principles/pull/372)
#### [restrictions](https://github.com/w3ctag/design-principles/pull/363)
#### [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366)
#### [Ethical Principles](https://github.com/w3ctag/ethical-web-principles/issues) triage issues

##### https://github.com/w3ctag/ethical-web-principles/issues/75 

Dan: Would like to hear from Hadley, some of the principles were crafted to be 'active voice' specifically

##### https://github.com/w3ctag/ethical-web-principles/issues/76

Amy: related to the sustainability principle being weaponised.  I will come up with some proposed change to the intro. 

Dan: a small change... 

Amy: to make it stand out a bit more than "collectively."

##### [Translations](https://github.com/w3ctag/ethical-web-principles/issues/78)

Dan: this is great!

Yves: the language is carefully crafted. Translations would have to have the same level.. a bit more difficult than a regular technical document.

*discussion on what the translation process is within w3c*

Amy: huge potential community... We could set up a transifex and invite community input.  

##### [find a voice](https://github.com/w3ctag/ethical-web-principles/issues/79)

Amy: if we say "the TAG thinks" then it may be changed to "the w3c thinks" ... if the AC does agree to it and therefore it becomes the AC's position then that's more powerful.

Dan: would we imagine that through the process we would be changing it to say the w3c thinks, or would w3c be issuing a statement that says the TAG thinks this. The process of issuing that as a statement would be a de-facto endorsement, but that we wouldn't rewrite it

Yves: the fact that statement is endorsed by w3c means that it's more than just endorsing that the TAG thinks.. it's endorsing the content.. we should say that if it reaches statement we'll change that sentence that it's not only the opinion of the TAG, but the opinion of W3C

Amy: +1

Dan: PR?

Amy: can do a PR to add more of our sense of ownership. Would like to know what Hadley thinks.

Yves: "w3c says that" instead of "tag says that" should be an ed note so that it's clear. [Statement in process](https://www.w3.org/2021/Process-20211102/#memo)

Dan: how do we advance the document? Do we notifiy w3c staff that we wish to... do what? to get AC review?

Yves: same as regular TR WD. Wide review by accessibility, security, privacy, and the TAG... Ensuring we address all the feedback from the AC and possible formal objections.

Dan: at some point it is appropriate to call for TAG consensus to get AC review?

Yves: yes

Amy: will do a PR ... is it worth setting a goal to get TAG consensus to get AC review?  Maybe at the f2f? tpac?

Yves: we need to resolve all the issues received...

##### [Voice](https://github.com/w3ctag/ethical-web-principles/issues/79)

Dan: more assertive if we identified ourselves.. we should loop Hadley in

##### [expectations](https://github.com/w3ctag/ethical-web-principles/issues/82)

Amy: agree in principle but in practice falls apart if you think about the scope of the web... "mental models" may be wrong, and "expectations" can vary a lot 

#### [Societal Impacts](https://github.com/w3ctag/societal-impact-questionnaire) open issues including [evidence](https://github.com/w3ctag/societal-impact-questionnaire/issues/7)
#### [Contributing tips missing in README](https://github.com/w3ctag/design-principles/issues/373)
#### [identity](https://github.com/w3ctag/design-principles/issues/324)

Amy: re-read [this thread](https://lists.w3.org/Archives/Public/www-tag/2021Jun/thread.html) from last year..

*we review Amy's proposed text*

```
## Identity on the web should be contextually appropriate

"Identity" is a complex concept that can be understood in many different ways. It can refer to how someone presents or sees themselves, how they relate to other people, groups, or institutions, and can determine how they behave or how they are treated by others.

On the web, we typically see systems which generate _identifiers_ and attach data about a particular person to these identifiers. This data may include simple attributes and values; claims or credentials which can be used for verification, authentication, or authorization purposes; or a compilation of choices, activities and interactions of a person in a particular system (or all of these). "Identity" is often used as a shorthand when referring to these kinds of systems, but you should note that this is unlikely to represent someone's identity in a complete or necessarily meaningful sense. 

Architecturally, identity systems are often composed of the following layers:
    
* Identifiers (strings)
* Credentials (data)
* Authentication & Authorization (protocols)

When designing, implementing or integrating an "identity" layer into a system, you should consider the following:

* Before you collect data about someone - passively or actively - and attach the data to a persistent identifier, enable them to [give appropriate consent]().
* Be transparent about the circumstances under which such data is used or shared.
* The same data is not always appropriate for different scenarios, or in different contexts, so [do not collect more than needed](link to privacy principles) for the service being provided, nor conflate or connect data collected in different situations.
* Where possible, enable people to use the same identifiers and associated data in multiple systems if they choose, but do not require this. 
* People should be able to establish multiple identifiers (and corresponding data) for different purposes within the same system, if they need to.
* Different identifiers for a particular individual should not be correlated without that person's consent. 
* It may be empowering or beneficial for people to be able to port their identifiers and associated data between different systems with similar functions.
* Identifiers may be ephemeral or long-lived.
* Using the web anonymously or pseudonymously is appropriate, sufficient, or necessary in many situations.
* Avoid mixing metadata for a system or protocol with the data connected to an identifier for a person.
```

Yves: local identifiers vs non-local identifiers... 

Dan: .. bound with authentication and authorization and credentials ... the federatedCM was originally called WebID, becaue the credentials are the identifier..

Yves: link to leaks where databases are hacked... 

Amy: something about data minimisation as well...

Yves: we should link to big data leaks

Dan: overlaps a bit with privacy principles. Could link.

Dan: as "complex"... not a concept that can be defined in the realm of technical architecture.

Dan: I think having a section on identity like this is good. I think it should be in section 1. I think it should be meaningul and accessible to people building new APIs.

Amy: I'd like to pass it by a few people before making a PR.  It should only say things that are settled concepts - not trying to break new ground. To help people who are coming at this for the first time not to fall into traps or make bad mistakes, and to come at it generally aligned.

Dan: agree.

### Breakout B (US / APAC) - [2022-07-05]

Present: Dan, Peter, Max, Lea
Regrets: Sangwhan

#### [monkey patching](https://github.com/w3ctag/design-principles/pull/355)

**Added a link to wikipedia's definition, merged.**

#### [Guidance about serialization](https://github.com/w3ctag/design-principles/pull/367)

**Seems overly broad and vauge, hard to determine what's actionable, left some feedback.**

#### [Security & Privacy Questionnaire](https://github.com/w3ctag/security-questionnaire) open PRs and issues

#### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370)

#### [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16)

Lea: we're not sure what's being proposed here. There is a def of exotic objects in the ecmascript spec - but Dominic is talking about a wider field. A lot of userland JS has this pattern. Do we want to say that all of this has bad design or is it something more speicfic?   I'm writing a comment.


### Breakout A (Europe / US) - [2022-07-05]

Present: Peter, Lea, Dan, Amy, Yves
Regrets: Hadley

#### [backwards compatibility principle #354](https://github.com/w3ctag/design-principles/pull/354)

*reviewing Ken's feedback*

Dan: makes suggestions

Dan: lines 289 and 290 extraneous?

Lea: [on 290] sometimes we standardize non-standard things because websites rely on them but that doesn't mean we can [/should] use them as precedent of API design for new features.  If it satisfies a valid use case would we standardize the badly designed thing or just build a new thing?

Dan: **commits Lea's suggestions**

Dan: let's bring this to the **plenary call**?

#### [what to do when a feature is temporarily only available on some platforms](https://github.com/w3ctag/design-principles/pull/357)

**we worked on some changes to the text and then asked Chris Harrelson for an example**

Dan: maybe we can merge this at the plenary.

#### [New principle: the simple syntax should not be doing the harmful thing](https://github.com/w3ctag/design-principles/issues/375)

Lea: it turns out there was some confusion on the issue - prefers reduced data - so we don't have an example. While the principle seems reasonable I'd be wary of adding it without an example since it's too obvious..

#### [New principle: Deployability and Monitoring](https://github.com/w3ctag/design-principles/issues/368)

Dan: related to wording bubbling around in privacy tf about telemetry data and whether browsers have a responsibilty to users about what they collect. Maybe should be on agenda for privacy tf tomorrow.

#### [New principle: Remove deprecated functionality responsibly](https://github.com/w3ctag/design-principles/issues/361)

#### [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369)

Dan: feels more like a finding?

Peter: doesn't feel like a design principle.. feels like a web developer principle.. not sure it merits a finding

Dan: is there one more about html than canvas? As we evolve the web platform we should be thinking about how we build features into html first? Architecturally thinking about the web platform as you've got html, on top of that css and js, and other things like canvas on top of it?

Lea: seems related with using images for things that shouldn't be images, like text. Canvas is dynamic images. Basically the similar reasons why this is a bad idea. Agree as DP stand right now it doesn't make sense in there. I'm not sure about publishing a new finding every time we have a DP that applies to developers rather than spec writers. We often come up with guidence for peopl ewho write web apps. For one we have a document we can edit. For the other there is a much bigger barrier - to publish a whole new document. Should we have a design principles document with principles for web developers, that we pull in the DPs.. some are fit for both. Some are only for web developers, and some only for spec editors. Maybe we should have three sources of truth and pull into two documents that we generate, or something like that. 

Dan: maybe. 

Lea: findings are kind of lost. Developers are not going to look at findings. But if there's a design principles document for developers, that is going to get a lot more attention

Peter: there is an open issue about making a version of this for developers

Lea: it's not just a subset

Peter: right, there's a venn diagram here

Dan: how to build great websites docs might not be in our scope. But there could bee architectural principles we could bullet point out that might fit in that kind of thing. Which could be fleshed out on articles on mdn etc. If we're going to do something like that, maybe we want to create a task force which includes a bunch of people from the community that are working directly with web developers

Lea: I like the idea of a task force. This is not coming up for the first time. Design principles for web component authors finding.

Peter: historically lots of examples of trends that become common in app development that are violating web arch.. not encoding state in urls, using fragments..

Dan: we have historical TAG findings that have addressed those. [E.g. capability URLs](https://www.w3.org/2001/tag/doc/capability-urls/)

Lea: right, so we have content immediately. We could link to them. 

Dan: even securing the web and unsanctioned tracking, all address website develpment rather than spec development

Lea: two part thing.. one part is to link, how are we going to manage this content. One part is editing. Needs editing work to produce such a document.

Dan: that's where a task force could come in handy. 

Lea: past tag members more prominent in the js community, we could reach out. Will update 'create subset' issue, and reference this issue.

### Plenary Session - [2022-07-06]

Present: Dan, Lea, Yves, Max, Rossen, Peter
Regrets: Sangwhan, Amy

#### 354 (backwards compat)

Dan: Did our change resolve your issue?

Max seems fine now.

Dan: is the example still good?

Lea: I don't think it's the best possible example... 

Rossen: *user agents* and *browsers* in the same sentence... 

Dan: *makes 2 suggested changes*



#### 357 - temporarily unavailable

Dan: Should we merge?

Peter: re-reading it it doesn't sound like guidance for someone writing a spec... 

Rossen: i don't think this is ready..

Dan: "build your feature so FD works"

Peter: i think it goes beyond that - it's in the engine, but doesn't work in one OS or one device because the hardware doen't support.  You need to be able to fetaure detect if it's been implemented but still doesn't work.  Geolocation as an example... it's easy to feature detect if it's implemented... but now I'm runnint it on a device that doesn't have a GPS ... so what happens?

Rossen: functional readiness vs. existence 

Peter: depends on OS support or hardware support - that may not be universal on the same version of the same engine.  Often times it's not possible to FD it.

Rossen: maybe the fruit is unripe...

Peter: I'll post a question - but regardless I think we've covered feature detection.. I think this is a subtle aspect of feature detection that is something people get wrong.

Dan: +1

Peter: guidance to spec authors.
