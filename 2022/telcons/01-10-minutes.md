# TAG Teleconference
#### 10-13 January 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-01-10](https://www.timeanddate.com/worldclock/converter.html?iso=20220110T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306) - @hober
* [Issue with our guidance of use of custom properties](https://github.com/w3ctag/design-principles/issues/251) - @LeaVerou
* [New principle: all new headers shall be structured headers](https://github.com/w3ctag/design-principles/issues/252) - @ylafon
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

### Breakout B (US / APAC) - [2022-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220111T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: Avoid introducing new parser-blocking features, fixes #329](https://github.com/w3ctag/design-principles/pull/347) - @cynthia
* [Add guidance for attributes vs methods. Resolves #70.](https://github.com/w3ctag/design-principles/pull/350) - @cynthia
* [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia, @atanassov


### Breakout C (APAC / Europe) - [2022-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220111T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)



* [Decentralization vs federation](https://github.com/w3ctag/ethical-web-principles/issues/54)
* [Less Hedging & Add Subheadings](https://github.com/w3ctag/ethical-web-principles/issues/51)
* [Say something about resisting interpersonal abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)
* [The danger of prioritising algorithmic relevance over human needs](https://github.com/w3ctag/ethical-web-principles/issues/42)

### Plenary Session - [2022-01-13](https://www.timeanddate.com/worldclock/converter.html?iso=20220113T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Peter, Dan, Hadley, Lea, Yves, Rossen

Regrets:


### [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306) - @hober

Lea: Still blocked... we need to reword something... 

**we go through proposed changes to the text in the PR**

[we find reference to alan kay's principle](https://www.quora.com/What-is-the-story-behind-Alan-Kay-s-adage-Simple-things-should-be-simple-complex-things-should-be-possible?share=1)

**wordsmithed and agreed to squash & merge**

### [Issue with our guidance of use of custom properties](https://github.com/w3ctag/design-principles/issues/251) - @LeaVerou

Lea: maybe close? container queries cover a lot of it...  we have a finding that targets web component authors -- but with current tools web platform provides authors not possible ... so today's web components use .. can't use custom properties. However there is this new spec - container queries - also allows for querying the values of custom properties. So that will allow a lot of use cases not previously possible.  So this is a smaller problem.

Peter: question is - are custom elements inherently containers?

Lea: you have to declare but .. 

Peter: isn't that implicit?  

Lea: It seems to be it addresses this problem.

Peter: I think it does address the issue - but if custom elements don't explicitly contain style... but that's a bug on container queries. orthogonal.  I agree we can close this.

Rossen: Is there still text we should write?  I think the issue and reason for guidance is valid.  If we just close the issue - but if nobody knows about it or how to use it, then we know it but community doesn't know it.  Also agree with the guidance .. it is relatively not baked ... still super early.  Things needs to be finalized around container queries. But leary of providing guidance to authors right now.

Lea: the guidance is a finding... 

Dan: [transfers issue](https://github.com/w3ctag/webcomponents-design-guidelines/issues/8) to the finding.

Peter: leave it until container queries is a little more baked.  So mark it as blocked for now...?

Rossen: as a finding i think it's fine.  

Peter: I think it's fine to update the finding ... 

Lea: sounds strange but defer...

Dan: at this point on hold, in the future maybe update finding. maybe add material to design principles.

Rossen: if we're saying this is still early on what's our guidance in the meantime.  

Lea: Add "whenever possible" ..?

Rossen: yeah.

Dan: we can talk about a finding PR at the plenary?

Lea: OK.

### [New principle: all new headers shall be structured headers](https://github.com/w3ctag/design-principles/issues/252) - @ylafon


### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss


## Breakout B

Present: Max, Rossen, Peter

Regrets:


### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

Discussion and suggested edits to the PR

### [New principle: Avoid introducing new parser-blocking features, fixes #329](https://github.com/w3ctag/design-principles/pull/347) - @cynthia

### [Add guidance for attributes vs methods. Resolves #70.](https://github.com/w3ctag/design-principles/pull/350) - @cynthia

### [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia, @atanassov


## Breakout C

Present: Dan, Kenneth, Sangwhan, Dapeng(Max), Hadley, Yves

Regrets:


### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

Sangwhan: language about single implenter - not a design principles issues. It's a w3c process issue.

**discussion on whether this is a design principles issue or if it's a process issue**

Dan: shall we scrap?

Sangwhan: I'm ok scrapping or doing a complete re-write on this.

Hadley: one question we got into in breakout A - who will do a rewrite?

Sangwhan: I can try.

Dan: looks like we have consensus that this is more of a process issue but as Hadley as pointed out it's not enitely out of our wheelhouse - just not part of the design principles.

Sangwhan: I can try to to write alternative text.

**so resolved**

### [Decentralization vs federation](https://github.com/w3ctag/ethical-web-principles/issues/54)

Sangwhan: meaning of decentralized....  Web is tied to root DNS, cert authorities... centralized... You have a dependency on certain things... 

Hadley: i think we accomodate that in the original text by saying "we favour decentralized"

Sangwhan: that's why i favour federated... BGP is also not decentralized... 

Yves: for TLS you also have nonrepudiation check which is quite centralized...  but those centralization points are not the worst... There are articles explaining that blockchains are not as decentralized as people think...

**discussion on crypto stuff**

Yves: "decentralization is in the eye of the believer"

### [Less Hedging & Add Subheadings](https://github.com/w3ctag/ethical-web-principles/issues/51)

**we agreed to close**

### [Say something about resisting interpersonal abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)

Hadley: the issue is on me - the issue is around power imbalances - particularly e.g. Tobie said "boundaries of common security practices are that your employer knows about your ativity" - inherent power imbalance.

### [The danger of prioritising algorithmic relevance over human needs](https://github.com/w3ctag/ethical-web-principles/issues/42)

Sangwhan: there is a machine learning ethical principles [document](https://webmachinelearning.github.io/ethical-webmachinelearning/)... we could potentially take a look that. 

Hadley: this is good but very specific

Sangwhan: if we are to add something about ethical use of AI in there what would be the TL;DR?  There are a lot of subtltys about ethical use of AI?

Hadley: the original discussion was where algorithm is acutate but due to biases in training data the results become dangerous or inhumane.  There's something about not just accuracy but it having a damage to users that makes it ethica to me... Something that just results at misleading statistics...

Max: machine learning ... new priciple?

Sangwhan: I don't think machine learning should be brougt up... Altgorithmic bias can happen even without ML

Max: we should emphasize the relationship with web

Dan: review of webxr raw camera access API... nto to do with AI or machine learning, but there is an untended consenquence that if you let web applications have access to the raw camera feed, it could be piped into an AI or ML facial recognicion alggorithm could be sitting inside a WASM blob . That presents risks to the end user that they may not have been aware of when they agreed to open a fun VR program.

That feels like the right thing to consider here. The interaction between different APIs and technologies on the web. Doesn't address algorithmic bias, but is more of a general... Since AI/ML is now part of the web, when you are designing an API, you have to think about how your technology might fit togehter with something that fit together with AI/ML.

Sangwhan: it does feel captured by "web should not cause harm to society" and "web is for all people" -- algorithmic bias tends to cause problems because it's not "for all people". Maybe we can add a sentence in there?

Hadley: that makes sense to me.

Dan: I agree.  I also think the more detailed work on this should be folded into the "societal impacts questionnaire" which Amy is working on.

Sangwhan: AI ethical principles also not well defined

Dan: considering there is a CG working on this I think we should defer to them

Sangwhan: and reference their doc.

Hadley: I can take it.

Sangwhan: see also https://en.wikipedia.org/wiki/Algorithmic_bias and https://ai.google/principles/ https://www.microsoft.com/en-us/ai/responsible-ai

**so resolved**

Hadley: there is a way to mention it while leaving space for the more detailed work.

## Plenary Session

Present: Max, Peter, Dan, Sangwhan, Yves

Regrets: Hadley, Amy


### A11y checklist

Sangwhan: the idea is to be a quick check whether a more comprehensive A11y review might be necessary. Series of yes/no qustions. List of yesses and nos will let people from a11y know which partds of the exposed design they should be focusing on.  A UI elemeent, a dialog... If you have a UI element that can disapear... If it's making noise (sound-only delivery mechanism)... API-only spec... Some sort of mechanism for the delivery of equiv of alt-text... specific kinds of user input (touch events, pen events) - need for fallback scenario.  Occational specs have authoring advice.  Authoring advice should promote accessible content and best practices.  2 other ideas we were incubating... 

Yves: a way to help people think about accessibility in their document rather than a pre-review. 

Sangwhan: We make it clear : we are not going to review accessibility.

Max: How is this document supposed to be used?  Published as a TAG document for spec authors to reference?  Or mandatory?

Sangwhan: mandatory in review process

Yves: S&P Questionnaire is a Note.  

Dan: we can add this a11y checklist as part of the review process...

Sangwhan: I can take this, snapshot it and send it to Silver...   Silver writes the guidelines... Invite Leonie to a breakout?

Dan: Breakout C next week?  I will send an email.

Peter: I'm happy to start linking to it... I think it might be good to not publish it as a TAG doc - better if it's owned by some a11y group. We could publish it some place temporarily with the expectation that it is transfered to them at some point.  The existence of the doc is good - to act as a quick sanity check. Happy to have that as our gatekeeping. Ultimately the doc should be owned by the a11y folks.

### Breakout Rollup

#### Breakout A

Peter: we landed a PR on design principles.

#### Breakout B

#### Breakout C

Dan: we closed one issue on EWP. 

### Issue Triage

Sanwhan: bunch of untriaged issues.

Peter: 36 issues with no milestones in design principles.

Dan: Shall we assign some of that to next week?

Peter: a bunch of lefover ones from this week as well.  

#### WebGPU Review

Dan: WebGPU in breakout B next week?

Sangwhan: Tess. 
