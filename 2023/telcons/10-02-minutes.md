# TAG Teleconference
#### 02-04 October 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-10-02](https://www.timeanddate.com/worldclock/converter.html?iso=20231002T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Discuss new findings
* [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)
* [Start developer version](https://github.com/w3ctag/design-principles/pull/386)
* [Make 6.1 more inclusive of non-Web JS APIs](https://github.com/w3ctag/design-principles/pull/435)
* [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou
* [New principle: Avoid exposing API that result in synchronous flushing of CSS or layout](https://github.com/w3ctag/design-principles/issues/388)

### Breakout C (APAC / Europe) - [2023-10-03](https://www.timeanddate.com/worldclock/converter.html?iso=20231003T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Discuss new findings
* [Editorial tweaks](https://github.com/w3ctag/design-principles/pull/409)
* [Make HTML attribute sections consecutive](https://github.com/w3ctag/design-principles/pull/412)
* [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion
* [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)
* [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman
* [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo
* [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion

### Plenary Session - [2023-10-05](https://www.timeanddate.com/worldclock/converter.html?iso=20231005T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Yves, Amy, Lea

Regrets: Rossen, Dan, Tess

### Pre-agenda chat

Arguement about whether CSS should be versioned or not

### Discuss new findings

### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

Lea: I'm fine with Dan's suggestion, I'll commit it. Bigger picture - I don't have strong opinions about this principle (I've just ported comments from an issue). This is not something that is at risk of not being followed. We don't see people violating it very frequently. Usually the opposite is the concern, to convince browsers to make any change at all even if it's clear it benefits everyone, or if they promised they'd make the change if it became necessary later on.

Peter: shall we punt this?

Lea: we can merge Dan's other suggestion... but it's not about implementation, it's about usage. We need to consider widely used features for backwards compatibility more. Which may not necessarily even be widely implemented. Eg. a feature used by everyone that is not supported by firefox for example. [leaves comment]

### [Start developer version](https://github.com/w3ctag/design-principles/pull/386)

Lea: why does this have a milestone? There's nothing to see. Tess suggested edits to the makefile but I've never used makefiles before. It just needs more work, nothing to discuss.

Peter: what work, who does it, and when?

Lea: it's me and Sangwhan. I need to ping Tab about something bikeshed can do [does so].

Lea: if Tab is not willing to fix [bikeshed] does it make sense to introduce a pre-preprocessor for generating the two versions? Any templating language would do. Conditional inclusion is basic in any syntax, we could have a pipeline where depending on the commandline flags we output different bikeshed code, and then the bikeshed code gets processed by bikeshed. Maybe we don't need bikeshed to do this.

Peter: doable. Decent templating library called jinja that is quite powerful

[lists templating libraries]

Lea: that might be more powerful and produce a nicer syntax

Peter: gets confusing because we have a polyglot document with two different templating syntaxes which may have conflicts

Lea: that's the downside

Peter: if it uses the same syntax as bikeshed, you'll have to escape the bikeshed

Lea: we can choose one that doesn't. I think bikeshed is unique enough. I don't think it uses double braces, or single curly braces and % signs. If we use includeif as an attribute of an element, that restricts us to elements so we cannot vary text in attributes, things like that. Or we need a whole new metadata block to override things. We could do all sorts of things... The more I think about it the more I like this approach.

Peter: let's not get carried away and do weird things

[discussion of implementation details, Peter to do something with jinja]

### [Make 6.1 more inclusive of non-Web JS APIs](https://github.com/w3ctag/design-principles/pull/435)

Lea: I think this was controversial

Amy: last comment from Sangwhan saying we need a discussion

Peter: he also asked for some input from littledan and didn't get any

[push to breakout C]

### [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou

Peter: has a PR and feedback that the issue is addressed. Can close?

Amy: +1

Lea: fine to close

### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

Lea: Not sure if it's worthwhile continuing with CSS principles, the CSS WG has their own

Peter: issue also mentions higher level principles..

Lea: [this is the meta issue, unanswered](https://github.com/w3ctag/design-principles/issues/387)

Yves: [367](https://github.com/w3ctag/design-principles/pull/367) was merged as well. Perhaps this is enough generic serialization guidence and we can close this as well?

Peter: Lea, does this cover your concerns?

Lea: as someone proposing css features, I never know what to propose in these computed values or serialization dicsussions, and after reading this I still don't know what to propose. It's good advice, but not very actionable

Peter: should it be high level guidence, or should we get into css serialization? has all the other issues..

Lea: "Languages may differ..." - it's a bunch of considerations but what is the balance of these for CSS?

Peter: I think there are some principles...

Lea: and dbaron mentioned them.

Peter: in general I think a lot of that is a mistake because you're not preserving.. if you follow the css serialization guidelines you'll produce something that has the same effect but doesn't necessarily preserve the author intent. If you're trying to build an editor you can't use the browser serialization at all, it throws away a lot of information

Lea: yes. But if you're building an editor you need a ton of stuff that's not going to be preserved by any parsing mechanism like whitespace

Peter: and comments

Lea: html serialization is particularly bad, there's a ton of things that change. But you lose enough things that you cannot use that process for an editor in any language

Peter: i think that ship has sailed, I don't know that we can fix that

Lea: we could, but is it worth the effort? But the CSS concerns are not even listed here. They're not even factors. The factors listed are [reads factors]. Serialize to the shortest form or consider back compat is not even among these

Peter: I'm not sure things like serialize to the shortest form should be general guidence for all languages that could be added to the web in the future. I think tha'ts language specific guidence that css has chosen to adopt.

Lea: then maybe we should list that CSS has additionally these extra rules

Yves: [scribe missed]

Peter: should we open a new issue?

Yves: maybe Lea's comment on this issue should take into account the existing text that Rossen made

Lea: what I'm writing write now is... [this comment](https://github.com/w3ctag/design-principles/issues/284#issuecomment-1743386099)

### [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou

Peter: not a lot of discussion

Lea: guidence as it's currently written goes against html elements being usable without javascript

Peter: in the component guidelines?

Lea: yes. I think this and other guidence on the same vein is driven by the part of the community that sees web components as a shortcut for resuing JS rather than something that makes some functionality approachable to people who can't use js. Which is what html is supposed to do - doesn't expect you to assign properties through js. Having a guideline that goes against how html works but is drive by performance concerns is against the spirit of web components. If there are performance issues, fix those, to make it viable to create componenets that behave like html elements. I don't think we should be pointing more people towards the direction of having web components that do nothing without a ton of javascript behind the scenes. There was an example from google that was a single componenent in the background and everything else was done through javascript.

Peter: do we need better APIs on the DOM to make that data accessible? If I have an array of objects and pass it into a property that makes the code that I have to write for my component fairly simple. Vs if all that data were a bunch of subelements. There's not a good convenient way of extracting data from the DOM like that

Lea: yes. This is another gap in the web platform. This is exactly why I envisioned a task force that would do this gap analysis on the web platform... started as an idea between sangwhan and dan and me, around installable web applications. Proposed we should make it more broad. Powerful APIs is just one gap. There are lots. Right now nobody identifying that

Peter: there is a broad issue and a narrow issue. The broad issue is how do we do gap analysis on the web platform, the narrow how do we read/write data for things that are represented via HTML structures

[very in depth discussion of implementation]

Lea: can write this up as an issue

### [New principle: Avoid exposing API that result in synchronous flushing of CSS or layout](https://github.com/w3ctag/design-principles/issues/388)


## Breakout C

Present: Dan, Amy, Sangwhan, Yves

Regrets:


### Discuss new findings

Sangwhan: I think [sustainability and bundling](https://github.com/w3ctag/caching-bundling-sustainability) one is a week or two of work away. The no versioning of the web... one is a bit easier, but I don't think we've had enough people look at it yet.

Yves: the mention that there should be only one web is always there in w3c, and it's in EWP, so we should lean on that as well. One web is antithetical to versioning

Sangwhan: that is mentioned in the conclusion

Dan: maybe add to the beginning as well to bracket it, for structure

Sangwhan

Amy: I can do an edit pass... 

Dan: let's work on an edit that we're happy to bring to github and then we work on it from there.

Yves: https://www.w3.org/mission/ ?

Dan: feel it needs more intro.. ecosystem has developed in phases or something like that. If I add anything I'll use track changes

Sangwhan: check it doesn't already say that. Trying to keep it as short as possible

Dan: thinking from a naive reader perspective, how to order things

Sangwhan: [reshuffles text]

Dan: one thing that comes to mind is this [baseline](https://web.dev/introducing-baseline/) work going on. I want to make sure we don't contradict that... discussion about features and milestones could be interpreted as coming against the baseline concept. which is a different thing - that is developer facing. Trying to layer something on top of the platform, but it's complicated. What we're trying to achieve is more making it clear that web x.x doesn't make any sense as a concept. Which si right, however the baseline thing is trying to overlay a kind of set of baseline features which developers can be confident exist in the web and that's .. we shouldn't be undercutting that. Fine line.

Yves: should we also talk about how new apis and stuff on the web should be paired with graceful degredation, so we have a path toward implementation, so a new baseline that will have this new capability? The evolution has been done that way. You add something, a polyfill or something else, so that other people can use, and once everyone is up to date with the latest browsers and all the browsers..

Dan: worth spending a couple of sentences on that. We could reference the polyfill finding

Yves: and evergreen web?

Dan: I've left two links at the bottom. Demonstrates a good story - we're building findings on top of things we already said. Evergreen web finding from 2017 doesn't talk about versions. We are definitely saying something new here.

Sangwhan: I don't know if polyfill really fits in. It's detail on how a new feature is being rolled out

Dan: we can mention the fact that progressive enhancement is another technique to ensure we don't need versions or something like that

Yves: https://www.w3.org/wiki/Graceful_degradation_versus_progressive_enhancement .. it's originally from the Opera web standard curriculum that is no longer available. It's very linked to mobile but pretty sure it can apply more generally

Sangwhan: baseline is also a moving target, right? 

Dan: yeah

Sangwhan: we could write this is not to be confused with efforts such as baseline which is an incremental evolution and does not have anything to do with versioning

Dan: yes, to be clear. So we'll do more editing, but I don't want to wait a month to publish this, let's work async.

Yves: pretty sure Lea will have comments

### [Make 6.1 more inclusive of non-Web JS APIs](https://github.com/w3ctag/design-principles/pull/435)

Amy: we discussed yesterday... wanted to talk to Sangwhan

Sangwhan: looking... I might disagree..  I think this only make sense if the non JS web apis can't make sense of meaning of *attributes*. Ultimately if *attributes* makes sense as a concept then this doesn't improve anything...  [leaves comment]

### [Editorial tweaks](https://github.com/w3ctag/design-principles/pull/409)

Amy: more than 'editorial'

Sangwhan: we should close this

Dan: go with what you said in April. The doc has moved on, there have been multiple changes. Maybe you could ask the author to come back and make multiple prs instead of one huge one, so we can address each one in situ

Sangwhan: [closes]

### [Make HTML attribute sections consecutive](https://github.com/w3ctag/design-principles/pull/412)

Dan: this seems less of an issue

Sangwhan: also a conflict

Dan: it's just a reorder

Sangwhan: changes nesting structure as well. Closing with comment

Amy: we should aim to follow up in a week or two if we're saying that..

### [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion

Sangwhan: this is not done, I made some suggestiones, they need followup. Refers back to specs that are not standardised, and therefore is not implemented in multiple... puts a hard dependency on proposals that only chromium has implemented, which I don't think we should be doing

Dan: is it salvageable?

Yves: avoid lists treated as a definitive list... 

Sangwhan: problematic - no actionable principle. I've written this in the review

Dan: I'll ask Max if he can put some work in

### [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)

Amy: I still have work

### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman

### [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo

Dan: there's a PR pending which I think still makes sense to reflect the data minimization principle in the privacy principles document. The action is still on me.

### [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion

Dan: shall we just close it? Is there something we can turn into a principle?

Sangwhan: Yes. There are some specific examples where the members of an object where you have an object which has a set of members or attributes that expand depending on what was originally there. Eg headers. The header object can contain any amount of attributes as long as it was part of the header. Which sort of sucks because if you now try to map that back.. if you try to add other attributes specific to the js object representaton of the header - if they conflict, and you don't know if it's from the header or the object. Annoying when you're doing object serialization, you need to know which ones are object representation only vs the original. That's the thing that this principle touches on. There are at least two anitpatterns I've seen, I think it's something we should mention.

Dan: is the headline still avoid exotic objects?

Sangwhan: exotic is probably a good word, I don't know if there is better expression

Yves: I think it's an [official term from ecma](https://tc39.es/ecma262/#exotic-object)

Sangwhan: there are very clear reocmmendations we can write. Headers.headers and it's a key-value access mechanism instead of a bunch of other things to pull out..

Yves: is it related to overloading?

Sangwhan: i tcould affect that

Yves: we have discussed that

Sangwhan: I would imagine that exotic objects overload poorly. Our recommendation is don't do this, and do this through a getter setter pattern for the individual key values, instead of having it all spill out to the object space

Dan: feels like it would be low effort fo you to take what you just said and turn it into a principle? I think you're the one who needs to do it. I've assigned you.

## Plenary Session

Present: Peter, Tess, Amy, Dan, 

Regrets: 

### Breakout Rollup

#### Breakout A

Peter: web not being versioned discussion... because of CSS4 conversation. And backwards compatibility PR. Developer version... blocked by something in bikeshed... idea to make a preprocessor before bikeshed with a different templating engine. ... what is the status of the task force for finding gaps in the platform? 

Dan: there's the powerful apis taskforce which we had a session at tpac on, spirited discussion.  Idea is still to create a taskforce along the same lines as privacytf that would have multi browser support and look at powerful apis. Problem - we ratholed into what's the web arguments. Trying to bring energy to put those things aside and focus on the things we agree on. Lea is keen to push some of the things that don't have clear agreement. If we're going to do a taskforce we need to do it with all browsers represented. Still a blocker is I don't have bandwidth to spin this up, especially with privacytf. 

#### Breakout C

Dan: new findings from Sangwhan... mostly spent time on web doesn't have versioning. Not in github yet. Agreed to do some reviewing and feedback through the doc. One of the things that came up is that there has been this baseline thing that has consensus and we don't want it to look like we're against that. And the sustainability of caching.. sangwhan is also working on this, the version in gh is not up to date.

Tess: last time I reviewed the sustainability draft I think the github copy wasn't up to date

Dan: we closed some PRs that were claimed to be editorial but weren't. Well meaning but we've also made a lot of changes since the PRs were in. We asked for smaller PRs. Back to the exotic objects thing.. Sangwhan agreed there's something useful to write. Also still work on identity and data minimisation principles.

Dan: [summarises privacy tf meeting]

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
