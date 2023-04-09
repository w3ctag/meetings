# TAG Teleconference
#### 03-05 April 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-04-03](https://www.timeanddate.com/worldclock/converter.html?iso=20230403T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423)
* [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391)

### Breakout C (APAC / Europe) - [2023-04-04](https://www.timeanddate.com/worldclock/converter.html?iso=20230404T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
* [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia
* [Request for design principle clarification: Warn explicitly against getters throwing exceptions](https://github.com/w3ctag/design-principles/issues/400)
* [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)
* [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo
* [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov

### Plenary Session - [2023-04-06](https://www.timeanddate.com/worldclock/converter.html?iso=20230406T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Yves, Rossen, Amy, Lea

Regrets: Dan


### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss

### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)

Peter: do we have enough seeded questions to publicize it?

Rossen: everyoen engaged so far is either TAG or ex-TAG

Amy: we can tweet about it, and give people 'permission' to share it with eg. developers

Lea: *arrives at a helpful moment*

Lea: I think we can just close this. There's no point in reaching developers, we want to reach API designers. What is the best way to reach them?

Rossen: email blink-dev?

[discussed where / who to publicize it to]

### [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423)

[long and inconclusive discussion]

[further discussion at f2f]

### [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391)

Enough conclusion to draft a PR?

Lea: maybe could happen in the f2f

## Breakout C

Present: Amy, Yves

Regrets: Dan, Max

[cancelled lack of quorum]


### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo

### [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia

### [Request for design principle clarification: Warn explicitly against getters throwing exceptions](https://github.com/w3ctag/design-principles/issues/400)

### [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)

### [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo

### [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov


## Plenary Session

Present: Dan, Peter, Max, Amy, Yves

Regrets: Hadley

### Breakout Rollup

#### Breakout A

#### Breakout C

#### https://github.com/w3ctag/design-principles/pull/290

Dan: lots of comments from me.

Amy: last comment from you Dan suggests throwing it out and starting again - maybe focus on that at the f2f.

Dan: punted to Tokyo where we can give it some dedicated love.

Dan: goal for f2f: **clear the PRs in design principles**

#### https://github.com/w3ctag/design-principles/pull/354

Dan: I suggested to remove a bullet point.. Lea asked why, and I don't remember..

Dan: merge?

Peter: David makes some good points about legacy terminology that needs to be addressed...

Dan: Adds comment suggestion....

Peter: this is talking a lot about content relying on non-standard behaviour.  Nothing talking about changes to standardized behaviour... 

Peter: that bulleted list... -- what about changing specified behaviour.  We're not speaking about that anywhere... 

Dan: we could remove "legacy" and just say "when considering changes to features", and add to the bulleted list there about does this change the standardised behaviour of this capability

Dan: not sure how to address https://github.com/w3ctag/design-principles/pull/354/files#r963683513.

Dan: we can punt the rest to the f2f.

#### https://github.com/w3ctag/design-principles/pull/357

Dan: can we merge this?

Peter: implementations vs. platforms... both cases relevant... 

Dan: Adds as suggestion...

Dan: Sangwhan already approved - proviso of having an example which we don't have so let's move it forward and add an issue.

Peter: available vs. implented

Peter: going going....

**merged and closed**

#### https://github.com/w3ctag/design-principles/pull/363

Follow up at f2f

#### https://github.com/w3ctag/design-principles/pull/367

Dan: [rephrases to make simpler]

Yves: intent might be that if you're using a parser to consume things that are minified

Dan: what impact does that have on the text? That this principle applies to parsers?

Yves: parsers are generating only in-memory structures so it's not relevant for serialisation

Peter: should probably change the second half.. "adding or extending.."

Dan: ..should consider their effect on parsers? Consumers.

Peter: run changes by Rossen

Peter: one additional [comment](https://github.com/w3ctag/design-principles/pull/367#issuecomment-1175216706) from Lea. I would be ok with merging an opening up a new issue around that comment.

#### https://github.com/w3ctag/design-principles/pull/372

Amy: Lea has left a load of feedback - whatever everyone thinks best [at the f2f]i is fine with me.

#### https://github.com/w3ctag/design-principles/pull/396

Amy: I will review and respond to feedback in time for discussions at the f2f...

#### https://github.com/w3ctag/design-principles/pull/405

*Tabs vs. spaces: fight!*

Amy: iterative improvement: merge it.

Peter: personally I like intenting... we are doing it other places...

Dan: I say merge it.

Peter: and add another issue about identing practice...

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
