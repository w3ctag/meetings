# TAG Minutes Doc - Week-of 4-March-2024

## Agendas

### Breakout A (Europe / China) - [2024-03-04](https://www.timeanddate.com/worldclock/converter.html?iso=20240304T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion
* ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456) - @cynthia, @torgo
* [Add info to 9.1 & change link](https://github.com/w3ctag/design-principles/pull/470)

### Breakout B (California / Europe)  - [2024-03-04](https://www.timeanddate.com/worldclock/converter.html?iso=20240304T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454) - @ylafon
* [New principle: Incremental user effort should result in incremental value (or more)](https://github.com/w3ctag/design-principles/issues/473)

### Breakout C (California / Australia) - [2024-03-04](https://www.timeanddate.com/worldclock/converter.html?iso=20240304T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou
* [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453) - @LeaVerou, @torgo, @hadleybeeman
* [First pass at #453 (text-based syntaxes should be designed for humans)](https://github.com/w3ctag/design-principles/pull/472)
* [New principle: When introducing heuristics, also include a way to override the heuristic](https://github.com/w3ctag/design-principles/issues/455)
* [More detail on why events should fire before promises](https://github.com/w3ctag/design-principles/pull/460)
* [Add principle on use of delta seconds](https://github.com/w3ctag/design-principles/pull/467)

### Breakout D (California / Australia) - [2024-03-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240304T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)
* [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457) - @hober
* [New principle: APIs which vend byte buffers should return a Uint8Array](https://github.com/w3ctag/design-principles/issues/463)
* [[WIP] add forwards compatibility / graceful degradation principle.](https://github.com/w3ctag/design-principles/pull/468) - @hober
* [Short is often better](https://github.com/w3ctag/design-principles/pull/474)

### Breakout E (Europe / China) - [2024-03-06](https://www.timeanddate.com/worldclock/converter.html?iso=20240304T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)


* [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396) - @rhiaro
* Work on Ethical Web Principles Pull Requests and Issues - put forward for wide revview?

### Plenary Session - [2024-03-06](https://www.timeanddate.com/worldclock/converter.html?iso=20240306T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* New TAG Process Discussion
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / China) 

Present: Dan, Max
Regrets: Yves

#### [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion

*we review Sangwhan's comments on the current draft*

Max: Document policy is considered a group report so... https://wicg.github.io/document-policy/  Also there are notes in the draft... separate out features that are not yet interoperable into their own category...  One category of features could be "already interoperable" and 2nd category "at lesast 2 vendors interoperable".

Dan: so first of all all things that have a /TR version should be pointing to those and also there should be 2 categories as you say.

*Max to do another revision based on these comments*

#### ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456) - @cynthia, @torgo

Dan: to do with this part of the doc: https://w3ctag.github.io/design-principles/#js-rtc

Dan: reading jake's comment and I'm still not clear on how to translate this into an actionable principle... 

Max: Jake suggests in his earlier comment "This should probably be reworded in terms of running scripts and callback invoking."

Dan: Maybe "Avoid altering data retrieved through JavaScript APIs when scripts are executing"?

Max: maybe also add "...or callbacks are being invoked."

#### [Add info to 9.1 & change link](https://github.com/w3ctag/design-principles/pull/470)

Dan: *taking a look first at Amy's suggest re-word*

Dan: *accepts Amy's re-word*

Dan: *considering Sangwhan's comment*

Dan: Maybe it should be using the language of data minimization... 

Dan: something like "In line with [Data Minimization](https://w3ctag.github.io/design-principles/#data-minimization), only expose the minimal amount of data necessary in order to for the web app to accomplish its goals. The guidelines below can help..."

Dan: I will edit the PR... and maybe we can land it later this week.

Dan: [makes suggested change to PR](https://github.com/w3ctag/design-principles/pull/470/files#r1510954074)

### Breakout B (California / Europe) 

Present: Peter, Matthew,
Regrets: Yves

#### [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454) - @ylafon

#### [New principle: Incremental user effort should result in incremental value (or more)](https://github.com/w3ctag/design-principles/issues/473)


### Breakout C (California / Australia) 

Present: Martin, Peter, Tess, Lea
Regrets:


#### [Web platform features that augment HTML elements en masse](https://
github.com/w3ctag/design-principles/issues/423) - @LeaVerou

Some general consensus that CSS selectors are a powerful tool that can replace the "Selector" part of this proposal.  That might require some new selector capabilities, but those might be generically useful (like @moz-document...)

Open debate about whether using the CSS grammar or using JSON is better.  Then we ratholed on things like the media type +json (or +css) suffix and its utility, CSS parsing more generally, polyfills for CSS-like things, and more.

In order for the CSS base syntax to be reusable and polyfillable, we need the CSS parser (or a more abstract CSS syntax parser) to produce a generic object model for things it doesn't understand, rather then throw them away as it does now (also would help for CSS polyfills). 

#### [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453) - @LeaVerou, @torgo, @hadleybeeman

#### [First pass at #453 (text-based syntaxes should be designed for humans)](https://github.com/w3ctag/design-principles/pull/472)

Discussed during the breakout B.  Missed the discussion on the issue.  Not updated since the last discussion on the topic where a bunch of points were captured.

More discussion, captured in issue, Lea to update PR.


#### [New principle: When introducing heuristics, also include a way to override the heuristic](https://github.com/w3ctag/design-principles/issues/455)

#### [More detail on why events should fire before promises](https://github.com/w3ctag/design-principles/pull/460)

#### [Add principle on use of delta seconds](https://github.com/w3ctag/design-principles/pull/467)


### Breakout D (California / Australia) 

Present: Peter, Tess, Amy, Lea
Regrets:


#### [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)

Lea: there was some opposition which surprised me

Tess: Anne and Dominic are opposed. I don't have a strong opinion. Seems likely if we did provide such guidance it would not be followed.

Lea: what do you think about the issue? Seems if you're throwing functions into the global scope you're essentially namespacing them without namespacing them. you have to pick names that are uinuqe and don't clash. There's nothing tying them together. No way for authors to explore them all together. To understand that they're part of the same API. More likely to conflict with author functions. I don't understand what the benefit is. I see drawbacks. What do you gain by adding a bunch of global functions?

Peter: I kind of agree with Anne a little bit and maybe Domenic, but I think they're overreading what you're saying - you're not saying never add them, just avoid it. It can be appropriate to add them..

Lea: every design principle is a rule of thumb. That is implicit. There is no design principle that applies all the time regardless of anything else. These are just considerations.

Peter: in general I'd lean towards not putting them int he global space unless it truly is something that makes sense as a global function. We shouldn't say don't do it - and we're not - we should say think carefully and these are the reasons you'd want to make it a global function vs a namespaced function. Articulate the guidence as to when you'd choose one vs the other

Lea: true. Makes sense. Having trouble thinking of methods that should have always been global.

Tess: [Domenic's comment from a year ago](https://github.com/w3ctag/design-principles/issues/426#issuecomment-1472928048) is interesting. Second bullet is interesting. If advice like this produced a proliferation of non constructable classes that would be a bad thing. If it's enough of a bad thing I don't know. The first bullet I don't find compelling. The third one feels like a taste thing..

Lea: don't like this divergence that is happening between tc39 and whatwg js apis

Tess: Fair. If your goal is to reduce divergence between whatwg and tc39, putting something in the design principles is not going to achieve that, practically.

Lea: goal is to reduce divergence... perhaps we should add something. It's more important to reach some kind of consensus.

Tess: agree. Currently no consensus among stakeholders in this issue.

Lea: that's the consensus that matters. The second point about being against other design principles.. objects should be constructable; classes should only be used .. that's not an existing principle without consensus... do we think math for examlpe was a mistake?

Tess: I don't know

Peter: mixed feelings. Regardless, I think we have examples in the platform that fall on both sides of this issue, and probably got it wrong, and examples that have got it right. More important than coming up with a principle saying tend to do this, we'd be better served to explain why you'd choose one over the other

Lea: definitely think you could go too far... dom.node and dom.element.. that would go too far. You only need one object to get the benefits of having a namespace. Beyond that it's pointless verbosity

Peter: other languages that do namespace things (C++ and Python) there are mechanisms to say Iwant to use this namespace by default and not have to repeat yourself all over the place. Being more aggressive on namespacing everything wouldn't be a bad thing if js had the ability to opt into a namespace

Tess: it does with ecmascript modules... gets back to arguement from years ago about built in modules that went nowhere

Peter: existence of namespaces as a concept negates some of domenic's arguements

Tess: the point about document and navigator is interesting. Window document and navigator, all three are treated as grab bags by people

Lea: that's true, but it doesn't mean namespaces are bad

Tess: I don't think it's unique to window that they're being treated as grab bags. All three are a mess. His point is if we discourage people from putting stuff on window they're more likely to put it on document or navigator... so haven't shifted behaviour much... but maybe it will shift things that belong on document and navigator

Lea: maybe we need a principle about when we add something on document or navigator. Also a consistency arguement - there are more apis that use namespaces than don't... 

Tess: I don't have an intuitiion about that... is that true? that more apis are namespaced vs not? 

Peter: just because something is more common doesn't make it right

Tess: can see the arguement either way

Peter: in the case of filesystem api it seems weird they're adding multiple functions to the global scope. That's an example - a whole bunch of related functions is a good reason to namespace them

Lea: Exactly. And createimagebitmap when you already have an image bitmap class

Tess: it is not constructable?

Lea: probably not otherwise why would you have a factory. But you could add it as a static method. I think we have a principle about that.

Peter: Lea has a good point here... structured clone as a global when we have all these other object doc methods... why isn't it an object doc method...

Tess: good point... tc39 has a way of doing things and whatwg has a way of doing things... they proceed with doing things. Platform is funny because of this divergence..

Peter: where this an established pattern follow that pattern - is the guidence?

Tess: for instance.. suppose we invented a new kind of DOM node, the right thing to do would be to create a new global element and ..

Lea: that's why the title says non constructor functions

Tess: a differnt thing seems relevent - the new invoker feature. Where does that live? There are other places tc39 is doing things differently than whatwg that are higher priority than the shape of the names. The intelsegementer(?) api.. for breaking up strings into words. There are more consumers of ecmascript than the web, node ecosystem. When we design apis in tc39 we overindex on designing an api that needs to be useful in a web and non web context.. so we dont' integrate well into the web. Most common case of intelsegementer ont he web would be segmenting the DOM.. get a bunch of ranges for sentences in a paragraph elment. Might not even be easy to make a string for the thing you want to segmenet. intelsegmenter assumes you're serverside and you have a string, known to be only in one language. Weirdnesses to the shape of the api that don't match js in a browser. It's unfortunate. That should have been caught early enough in that design for them to be able to change it

Lea: so in browser contexts it would have an additional dom signature?

Tess: I odn't know what the shape should be. What you typically have is a DOM.. most html/xml have some notion of a lang attribute. So it's weird that the intelsegementer call requires you to pass in a language. It's already present or can be inferred from the DOM. I'd expect it to produce ranges instead of indexes into a string. It's not a string that you necessarily have in the case of a DOM

Lea: my weakly had opinion is that it seems like these are different levels architecturally. DOM is part of the view, whereas this deals with the data. Good point that there should be a DOM api that uses intlsegment under the hood, but doesn't sound like intlsegmenter is the right place for that

Tess: i think you'll find intlsegmeneter isn't well suited to that - I tried it. If it's necessary to have two apis - oen that knows about web stuff like the dom, and one that just operates on strings, this reminds of me of fetch where you want these apis to rely on some shared underlying architecture. I don't think it would make sense to build the dom api on top of intlsegement in its current shape. You'd want them both to be defined on some kind of shared context

Tess: the point is the disconnect is bigger than how we name things

Lea: seems to go both ways. All our specs are using webidl which is using synonyms.. different terms for js concepts. Everybody reading these needs to mentally convert these to js concepts

Tess: I wish the ecmascript spec used idl terms..

Lea: I wish browser specs used js terms since they are defining js apis.. we can agree to disagree. 

Tess: "Overall, I'd prefer the TAG position on how to organize APIs to remain neutral. Some APIs may have material benefit from an "all static" object, but I don't think there's a clear default."

Lea: against having a principle at all... remaining neutral about how apis are organised..

Tess: I don't think it's that

Lea: you don't think we should have guidence on something like this. What do others think?

Tess: not that I don't thin we should have guidence. Sometimes it should be one way and sometimes it should be another way

Peter: right, there are times when we want to go one way vs the other. We need to dive into it more and figure out what criteria do you use to choose

Lea: that is the whole point of fleshing out the design principle. What are the edge cases? Thought of an example... fetch was obviously a good decision. We definitely don't want to say all functions should live under a namespace

#### [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457) - @hober

Peter: sometimes we mean DOM attribute, sometimes IDL attribute

Tess: funny one. Question of audience. Who are we trying to reach with design principles? Spec authors primarily. All for doing that in a way that is unambiguous. Some ways of alleviating ambiguity might be better or worse suited to the audience. If we were targeting web developers I'd be less inclined to presume familiarity with web IDL. Do we have a PR? Sounds like we should writeme.

Peter: there are two proposals in the issue. Replace every issue with either DOM attribute or IDL attribute everywhere. Or use attribute to mean DOM attribute and use another term like property for IDL. You had a strong preference for 1 in the past and opposition for 2. Brian Kardell also chimed in with a preference for 1. Straightforward writeme, just need to agree on resolution. 

Tess: add the write me label, I'll do it

#### [New principle: APIs which vend byte buffers should return a Uint8Array](https://github.com/w3ctag/design-principles/issues/463)

Peter: what's the difference between an arraybuffer and a uint8 array?

Tess: arraybuffer is somewhat indirect

Peter: tell it what the underlying type is?

Tess: have to make it a view to get the date in it. Already seems to be a principle... this person who filed it offered a PR. I'm happy to let them send us a PR. I suspect we agree. I'd be surprised if someone felt strongly in the other direction..

Peter: you can get a view of other types..  I'm not sure if that's an advantage in some cases. If I'm looking at a canvas I dont know if that gives me an arraybuffer or .. the underlying storage ... ergonomically to go from a uint array to a ..32 array would be a lot less ergonomic than just getting a view on a buffer. But don't have a strong problem with it. Comments where they decided use a uint8 array... if the underlying type really is just bytes, then no problem with it being a uint8 array. If it's more of an abstract bunch of data to interpret in different ways then an array buffer seem smore appropriate

Tess: maybe that's what the principle should say. In most cases uint8 array is sufficient, but if your underlying data can be used for different purposes then use array buffer. Do you think we need to lead with that and say to write a PR and capture this nuance? Or ask for a PR and add a comment?

Peter: if we agree on that nuance we should tell them

Tess: sure. Raise that in a comment and see if people agree? The link is to a comment from Anne, should we @mention Anne to see if the nuance is appropriate?

Peter: I can do that, see where it goes

#### [[WIP] add forwards compatibility / graceful degradation principle.](https://github.com/w3ctag/design-principles/pull/468) - @hober

Tess: still a work in progress... wasn't ready for review.. just needs some time

#### [Short is often better](https://github.com/w3ctag/design-principles/pull/474)

Amy: ship it

Tess: editorial change...

Merged


### Breakout E (Europe / China) 

Present:
Regrets:


#### [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396) - @rhiaro

*we discuss https://github.com/w3ctag/design-principles/pull/396/files#r1466639387 and agree to resolve that this is active and brief enough*

Amy: Martin left a comment "a missing point..." but would have prefered a suggested change?  Not reading this as something that would block merging.

Dan: if we think we should merge then let's merge.

Matthew: I agree. I think the changes you made in the f2f are compatible with that - it's going in the right direction. Does talk about identifiers and links to EWP as well.. ... Anything else can be done after.

**RESOLVE TO MERGE**

#### Work on Ethical Web Principles Pull Requests and Issues - put forward for wide revview?

https://github.com/w3ctag/ethical-web-principles/pull/108

*we discuss whether we should change the CEPC link to "code of conduct" proactively and decide not to*

Dan: *leaves a positive review*

Matthew: I see a lot of nom-user-visible odd line breaking... *discuss line breaking*

*discussion on what needs to happen before we put it forward fot Statement - looking at issues that are marked `pre-statement`*

**We agree to merge**

https://github.com/w3ctag/ethical-web-principles/issues/37

Amy: we were planning to cross link specific ethical principles to specific deesign principles. Do we still think we need to do that? I don't feel strongly. We have the link in the intro.

Dan: one of the things that makes it valuable is that it's brief and not complex. Value of adding more links is offset by making it less readable. But we've had feedback that they wish there was more actionable advice, which is why we added the link in the purpose statement.

**agree to close**

https://github.com/w3ctag/ethical-web-principles/issues/59

Dan: I think we've done this

Amy: do we need to mention the wider web community?

Dan: not explicitly. It's the case that other people can read this document to understand how we are informing our design decisions with ethical considerations

Amy: write that

**commence editing by committee**

https://github.com/w3ctag/ethical-web-principles/pull/110

**merged**

https://github.com/w3ctag/ethical-web-principles/issues/79

Dan: i think we've addressed this through incremental improvements

Matthew: I think this has been addressed... this is now going to wider discussion which is more appropriate for the wide review stage...

Amy: *nods sagely*  Suggest we draw the line.

Matthew: we've addressed the root of this issue and we appreciate the wider discussion but we feel this is something that should come up as part of the wide review process

**close**

**RESOLVE to put this forward for wide review as part of Statement track**

### Plenary Session - [2024-03-06](https://www.timeanddate.com/worldclock/converter.html?iso=20240306T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Tess, Dan, Peter, Matt, Martin, Amy
Regrets: Yves


#### New TAG Process Discussion

[PR for discussion](https://github.com/w3ctag/tag.w3.org/pull/48)

* generally okay with proposed process, we can refine as we use it
* gap about handing off between areas - can we use an initial response with assignees and checkboxes for areas?


##### Need to integrate horizontal review repo

Matthew: any other group can loop us in on an issue thread by adding a label which creates a tracking issue for us in [our repo](https://github.com/w3ctag/tracking-issues) with meaningful labels. I have a CLI for this.

Dan: we haven't been tracking it. We need to put this into the agenda creation script

Peter: possibly. Our work is driven by design review issues. Do we need tooling that creates a design review issue on this?

Matthew: that's something we'd have to make. The tool I have can help with prioritising - possible on the web but takes longer - filter for issues that have a status which means they're important. Some issues with statues they shouldn't get... that conflict with each other, eg. 'pending' and 'needing resolution'. There's a status about the other group closing their issue. A combination of pending and closed is really urgent. Good news is they aren't coming in at that big a rate. A few per week.

Peter: Even fewer. Some are dups of design reviews. We need to either stop ignoring it or shut it down

Dan: we should stop ignoring it

Peter: should we add this in the triage process?

Matthew: they're not all at the level of design reviews

...

Dan: also github discussions board .. not much traction... another way to think about being able to do that? it's a place for people to ask for clarifications

Matthew: depends where discussion originated - our discussions is about something we've made, but if it's in a wg repo it's something they want to pull us into

**discussion of levels and criteria for assigning them**

Peter: Mode instead of levels

Matthew: we can change them as we go. Also - is fastrack orthogonal? Can fasttrack happen in a breakout?

Dan: fast track is not high priority, it's for things that are not controversial

Amy: I'll revise

#### Breakout Rollup

##### Breakout E

resolved a bunch of issues on EWP with intention of putting it forward for statement

Dan: intention to put this fwd for statement... 

Tess: +1

Amy: +1

Martin: any opportunities missed in coverage and scope? 12 principles.... all look broadly fine... it's useful to do a bit of work to look at other things in this general space and see if there are gaps...  It doesn't have to be perfect...  Happy to do that along side...

Peter: ship it

Dan: Takes that as an action to inform the AC about wide review.

Amy: identity on the web - we merged.

Martin: I will look at it.

##### Breakout A

Dan: PR 363 on design principles about restricting features. Feature policy. A list of methods that allow restricting features. Varying support. Discussed having two categories - widely supported and not. Max is going to revise the PR.

... 456 is an issue from jake archibald about wording.. I'd like to land this. Jake suggested new wording for the body, but not the principle. Can people take a look?

... PR 470 which is close - about identifying information about devices. Review from Martin please? Linked to data minimization principle. 

Martin: I'm okay to land this. I don't like "use care" - could be more targeted

Tess: definite improvement

Peter: weird grammar - swap order of first two paragraphs

Dan: **will edit further then merge**

##### Breakout D

Peter: merged a PR... we had discussion about array vs. array buffer... left comments; came to consensus about term attribute- Tess to write PR; had long discussion about adding non-constructor functions to global scope.

Tess: meta point vs. clear disagreement...  ... but I don't feel like it's worth adding a principle that we know WhatWG won't follow.

Peter: we should offer guidance on when to use a namespace and when not to use a namespace...

Tess: I think writing guidance is a good idea... validating guidance with relevant stakeholders also vital. 

Peter: I think these issues should be merged in some form...

Amy: #448 is more specific...

Peter: #426 came first...

##### https://github.com/w3ctag/tag.w3.org/pull/48

*we discuss*

Tess: in the new guidance we don't give people that choice...

Peter: we talked about taking that out of the template.... (a) we often forget to read that and leave feedback in our repo and (b) we don't have the paper trail.

Amy: also when I was editing that line i felt was ambiguous...   Also I don't think they need to block eachtoher...

Tess: other than that I think it looks great.

Amy: quite a substantial process change on labels and areas... 

Lea: any rules on american english vs international english?

Tess: w3c styleguide on specs is American english but in other materials it's whatever is comfortable.

Martin: *going through and making typo corrections*

Lea: I'm leaving some nitpicky type of things...

Amy: if we're sharing a review across more people.... e.g. lea for API review vs Martin for privacy... making sure what bit each person is responsible for ...

Lea: are we Ok with a single person for each area?

Peter: it does say 2 people per area... which raises a question if you're assigned to it how do we know what area you're assigned to?

Amy: one thing we can do - first comment - a list of the areas and who's assigned and checkboxes...

Martin: do we have 2 people who are compatent in every single area?

Amy: we don't need 2 domaon experts... one person is the sense-checker...

Peter: just because you're assigned to a specific area of focus and you have comments in another area, it's not out of bounds...

Amy: this already gives us more coverage...

Peter: no reason to expect a single person wouldn't be assigned to multiple areas...

Lea: one of the complaints that came up in the retro - design reviews that don't make a difference... is that something (a) we want to caputre in this and (b) where do we want to capture... maybd under prioritization section.. predicted impact of the review.


##### Horizontal Review

Peter: in breakut B we discussed horizontal review tracker... we need to fold that into our process somehow... 

Matthew: one of the types of HR thing we need to do - any other group can loop us in on a conversation - by adding a label tag-review - which should create a tracking issue in our repository - w3c-tag-tracking-issues - and that creates these pointers for us... that is a very nice system but it takes a bit to get head around... 

Dan: should these go into the agendas?

Peter: we could use them as tracking issues... and have tooling that creates a design review issue...

Matthew: the tool I have could help with filtering out and priortizing... it could filter for issues that ... some statuses that conflict with eachother... shouldn't be both pending and awaiting a resolution... some in particular that we might want to prioritize based on date... also if the other group closed their issue we need to look at it to see if we agree it should be closed... some stuff we can do to help with triage... The good news is that they aren't coming in at that big a rate... easily could be picked up and inserted into the agenda...

Peter: the incoming rate is low - 4 in 2023 - many are "we filed a tag review rquest" it's largelly a matter of getting it into our triage queue....   Should we add to the triage process...   We need to be explicit of what it means for people to add this label to their repo...

Matthew: from APA's perspective, ... (1) for a spec review we get engaged... late in the game... (2) where you can get looped in on specific issues...   One of the reasons why it's not being used is because design review is more formal... but it could be as simple as changing one attribute value... design reviews having broad range of sizes... quickly questions... what's your feeling on this particular issue... rather than a spec review...  we can add the label to other issues ourselves...

Dan: discussion were spun up to try to capture...


#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

