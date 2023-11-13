# TAG Minutes DOC - Week-of Mon, 6 November 2023

## Agenda

### Breakout A (Europe / US) - [2023-11-06](https://www.timeanddate.com/worldclock/converter.html?iso=20231106T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Charter Reviews
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

### Breakout C (APAC / Europe) - [2023-11-07](https://www.timeanddate.com/worldclock/converter.html?iso=20231107T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Findings: sustainability of bundling & caching; no versioning of the web
* [Ethical Web Principles PRs](https://github.com/w3ctag/ethical-web-principles/pulls)
* [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov
* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
* [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia


### Plenary Session - [2023-11-08](https://www.timeanddate.com/worldclock/converter.html?iso=20231108T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss
* [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)
* [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou
* [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)
* [Make 6.1 more inclusive of non-Web JS APIs](https://github.com/w3ctag/design-principles/pull/435)
* [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453)
* [Add info to device apis section about privacy](https://github.com/w3ctag/design-principles/issues/398) - @torgo
* [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo


* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2023-11-06](https://www.timeanddate.com/worldclock/converter.html?iso=20231106T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Tess, Peter, Rossen, Lea

Regrets: Amy

#### Charter Reviews

Yves: we need to better organize...

Dan: Design review template for charters?

Tess: new repo?

Yves: I think a new repo would be easier.  We would need to have a time out for it because it's time sensitive... and if no comment then OK to not do anything.

Dan: what I said to PLH at TPAC was ... that we didn't want to be in the ciritcal path.. 

Yves: in strategy repo that is public there is a call for horizontal review for charters.. currently nothing added into TAG repo because of that...   To track it would be easier to have our own repo...  Depends what level of involvement we want to have from the TAG... Ones wwhere we know we need external feedback... others where it's straightforward...

Dan: in that case, we should be asking Team to open up a charter review us when the Team thinks it's warranted?

Peter: ... don't want us to get too off into process - if we want to review things it should be about the work that's being done.

Tess: as long as we do it in a way that isn't burdensome... Both design reviews and charter reviews are retrospective... someone's written the charter / spec and then we review it... If the Team comes to us ahead of time maybe that could shortcut...  But not necesarilly a hook.

Tess: one of the things I hear is - gee the folks on the TAG are missing the forrest for the trees - so busy doing design reviews, aren't setting architectural direction. Chartering new work is part of that...

Tess: I don't care for stop energy... we should catch things at the beginning... "is this the best fit for W3C?"

Rossen: wasn't this part of "directorless"?

Tess: i do think getting involved in the wide review stage is good...  We could do more to exert influence...

Lea: I would go even further... Any cases where TAG review was particularly useful when done at a very late stage?  The most value is early reviews...  

Peter: several times we've had impacts late - web audio, automotive...

Lea: where someone asked for an early review and then we still had impact at the late review stage... 

Yves: Strategy funnel https://github.com/w3c/strategy/projects/2 could be one place to look...

Peter: the TAG taking on the role of identifying new work and setting direction.. There are examples where we've done that but nobody has listened... could we fix that?
 
Tess: the Team writes charters - sometimes that happens and nobody sees it coming... the Team doesn't do that in a vaccum.  Usually someone comes to them and asks...  We can ask the Team - tell the Team - we can be part of where those ideas come from...

Yves: Team needs to ask community what they want to see as charters...

Dan: plan - I'll create a repo and an issue template.

*agreed*

#### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)

Dan: we tried to do the [Discussions](https://github.com/w3ctag/design-reviews/discussions) section

Lea: yeah but we haven't done enough to promote that... so no posts... Still think it's a good idea but it needs more work.

Lea: some action items - rossen to reach out to blinkdev and tess to post to webkit...

#### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

Tess: we already have a princple... the existing open issue is overloading HTML. I'd like to pull the "user overloading wisely" into.... from 6 into 2 and add some xamples.

Les: huge +1.

Tess: I'll put a PR in to fold it into section 2 and make it clear...  Could be a small PR... I like adding examples as well.

### Breakout C (APAC / Europe) - [2023-11-07](https://www.timeanddate.com/worldclock/converter.html?iso=20231107T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Hadley, Dan, Max, Yves
Regrets: Sangwhan

#### Findings: sustainability of bundling & caching; no versioning of the web
#### [Ethical Web Principles PRs](https://github.com/w3ctag/ethical-web-principles/pulls)

*Discussion on [#84](https://github.com/w3ctag/ethical-web-principles/pull/84)*

Hadley: does this solve the problem? … more concrete "to get concrete actions, we have fed these principles into the design principles" to make it really clear.  Or we say it's good enough for now.

Amy: having re-read it it's extra words that don't say a lot...

Dan: other thing that occurs to me is that it doesn't flow very well if the document is a W3C statement...

Dan: These are intended to be high level guiding principles. For actionable advice that stems from these principles, look to the Design Principles, Security & Privacy Questionnaire, Privacy Principles, etc...

Amy: Do we need to spoonfeed?  Some people are coming at this with spec editor hats on and being pedantic.

Hadley: Seconded.

Dan: so maybe close?

Amy: [updated PR](https://github.com/w3ctag/ethical-web-principles/pull/101)



Dan: [#85](https://github.com/w3ctag/ethical-web-principles/pull/85) has already been reviewed... let's merge!

Hadley: Agree.

Amy: Yes.

**merged**

#### [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov
#### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
#### [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia

### Plenary Session - [2023-11-08](https://www.timeanddate.com/worldclock/converter.html?iso=20231108T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Peter, Yves, Amy,

Regrets: Sangwhan, Lea

#### [eIDAS issue](https://last-chance-for-eidas.org/)

Yves: a request to control the root certs in different browser s- from the EU - this is a contentious issue. If you let some actors to force browsers to use specific CA then it's a problem.

Dan: in 2015 - we said https://www.w3.org/2001/tag/doc/encryption-finding/ - tag supports strong encryption...  but we don't talk about this issue...

Dan: is this policy or tech?  Personally I am supportive but should TAG support it?

Yves: to me it's policy that has implications at the tech level... maybe we should talk to AB...  

Peter: If there's gonna be a general statement by w3c then we should coodinate. But I think this falls within the scope of the TAG because of the encryption implications - it's legislation that breaks the encryption of the web. No less so than DOA thing... And we already have a finding in this space.

Dan: I agree fwiw that it's in the TAG's scope. And I agree that it's legislation that breaks encryption.

Yves: usually you download your browser from a mirror - that might have a different CA list... if it's not the case then a govenrment might fine companies that have financial activities in those countries.  But on the technical side it's possible - for example a browser might accept another CA and display a warning to the user that it's potentially insecure.

Peter: this screams we need better controls for sites to pin their CA ...

Yves: not only the CA but the whole chain.

Peter: if I can have my site say "I use letsencrypt as my CA" ... 

Yves: there is something in DNS for that...

Peter: DANE, which no browser supports, and all browsers deprecate3d HPKP. Another thing - it's fixable but Safari doesn't use its own cert store it uses a system store - now you've opened up MITM for every single app on the device.

Dan: Yves could you reach out to see if there will be a coordinated W3C response?

Yves: yes I will.

Hadley: best of both worlds might be w3c signing the letter and a public blog post from TAG.

Peter: if W3C is going to put one out then we should coordinate but we can wait to see what the w3c statement is first.

#### [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391) - @LeaVerou
#### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou
#### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss
#### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)
#### [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou
#### [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)
#### [Make 6.1 more inclusive of non-Web JS APIs](https://github.com/w3ctag/design-principles/pull/435)
#### [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453)
#### [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo
#### [Add info to device apis section about privacy](https://github.com/w3ctag/design-principles/issues/398) - @torgo


#### Breakout Rollup
#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
