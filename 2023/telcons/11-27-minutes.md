# TAG Teleconference
#### 27-29 November 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-11-27](https://www.timeanddate.com/worldclock/converter.html?iso=20231127T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov
* [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov
* [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @atanassov
* [Animating font-palette](https://github.com/w3ctag/design-reviews/issues/915) - @hober, @atanassov
* [Verifiable Credentials Data Model v2.0](https://github.com/w3ctag/design-reviews/issues/860) - @hober, @torgo, @rhiaro, @hadleybeeman, @atanassov

### Breakout C (APAC / Europe) - [2023-11-28](https://www.timeanddate.com/worldclock/converter.html?iso=20231128T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman
* [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman
* [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman
* [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

### Plenary Session - [2023-11-30](https://www.timeanddate.com/worldclock/converter.html?iso=20231130T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Amy, Peter, Hadley, Yves, Rossen, Lea

Regrets: Tess


### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @ylafon, @atanassov

### [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov

Peter: still waiting for feedback.

### [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss

*we read [yoav's response](https://github.com/w3ctag/design-reviews/issues/879#issuecomment-1803486439)*

Lea: our issue was the heuristics didn't seem very good and the response was that they're normative and cannot be tweaked...   There are webkit and mozilla positions - just filed.  

Lea: **meta** In the explainer template - we should ask for links and whether the response was positive / negative / mixed / no response yet.

**on "contentful paint"**

Peter: something that causes rendering ....

Lea: spec points to the def of a contentful element... but they're -- not sure how ...

https://www.w3.org/TR/paint-timing/#first-contentful-paint

Peter: something that can render gets rendered due to user interaction... e.g. change a css state and it causes a render...  

Lea: I have afeeling this is the right direction... spec describes "first contentful paint" but doesn't define "contentful paint"

Peter: I think it does .. it's if it's paintable and contenful. 

Lea: it talks about a document... the document may contain many elements that are paintable and contentful - so what makes a paint contenful.

Yves: when there is a paint occuring then the element is subject to a contentful paint...

Peter: I think this is excluding things like background...

Lea: what if an element is contentful and CSS changes its background... 

Peter: don't know how they define a contentful background image...

Lea: It would be good to have answers.

Peter: It's a render that flips some pixels.

Peter: question - a contentful paint that's a direct result of user interaction. How can they tell?  What if the aninmation made the change... Comes back to original question about heuristics.

Lea: As a general UI principle you should allow opt out when introducing heuristics. We have precedent of heuristics that could not be overridden and it was pretty bad: e.g. CSS specificity, people ended up entirely not using selectors for querying to avoid specificity.

Lea: adding history elements based on a soft navigation would be a bad user experience...  So if it's just for measuring performance then...  

Peter: not being exposed anywhere other than performance observers... agree you don't want to based user interaction or behaviour on this.

<blockquote>


  
</blockquote>

**agree to post**

### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

*we review [their response](https://github.com/w3ctag/design-reviews/issues/908#issuecomment-1808802510)*

Peter: I don't see a use case described in the explainer... I see a developer need...

Dan: should we press them on this point?

Peter: I still don't get it...  

Dan: they're conflating user needs with developer needs

Peter: I can leave the feedback... 

Lea: I think view transitions are overly complex...

Peter: I don't understand the use case - my feedback is that they are pointing to a use case and it's not a use case...

Lea: how is this done today and how will this be done with what they are proposing?  I can see how this could be useful...



### [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @atanassov

Rossen: we had a response. There are standards positions.. Good that it's a really early review

Yves: they did request a position from Moz. [and webkit]

Rossen: Still concerned - we are exposing delays and overall sluggishness caused through long running scripts or animation. One of the arguments is that you can observe today cross-origin cross-frame sluggishness by composing fairly well organised rafs on the page and observing them and concluding that the delays may or may not be caused by long running animation or script.. what they're doing here is exposing them and making them even easier to observe and gather and aggregate. So the fact we have this observability cross origin for the same agent doesn't mean we should make it easier. Making it easier cross origin is taking an unwanted pattern and making it easier. Imaginging worse case scenarios, eg. trackers trying to gather information in any possible way, especially cross origin.

Amy: can we ask for threat modeling for worst-case scenarios?

Rossen: yes.

Lea: for early reviews we should focus om more on use cases - how common are they, what's the design space, have they explored  other design options, things like that... is this a problem worth solving and is this the right direction?

Amy: if they can articulate the use cases we can encourage them to look for a solution that doesn't increase the attack vectors.

Peter: are we ready to close with additional feedbadck? or do we need some more back and forth?

Rossen: i woulnd't say this is satisfied ... not ready to say unsatisfied but closer to unsatisfied.. Need concrete evidence of why the approach needs more work.. The main points are: (a) interop - how well would this work across engines (good to see they've asked moz and webkit) and (b) the overall extensibility model - for me the major benefit from this is the ability to create causality - "what is causing a chain of events that is resulting in a long running animation?" ... Final bit is : seems we're taking an unwanted pattern and making it much easier to observe... 

Peter: so what's the path forward?  We could say "we're to see this move forward but want to see work on these 3 areas" - 

Amy: based on interacitons from privacy task force with web perf feels like we should push back a little more strongly...

Amy: seems like the argument is based on "if you can get this [data] in other complicated ways then it's better to provide an easier way" which ...

Rossen: I can provide more feedback... 

Dan: the text in the [ancillary data section of privacy principles](https://w3ctag.github.io/privacy-principles/#ancillary-uses) is pretty stable and can be referenced in the feecback.

### [Animating font-palette](https://github.com/w3ctag/design-reviews/issues/915) - @hober, @atanassov

Rossen: sounds great - how are they proposing to do it?  This is a good proposal - I like the problem that they are solving.   

Lea: this doesn't add new syntax - just enables existing syntax to work - that seems like an easy win to me.  I think this should have been fast tracked?

Rossen: good explainer for a CSS feature.

Lea: shouldn't be in google docs...

Peter: close this as satisfied?

Rossen: yeah!

Lea: I can write the comment.

**agreed to close as satisfied**



## Breakout C

Present: Amy, Dan, Yves, Hadley, Sangwhan

Regrets: Max


### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Amy: feels like it's doing the same thing as TOPICS, but more granular, and for the advertisers instead of for users... a load of ad-tech jargon but they have now sent us a glossary.   ... a lot of work for advertisers on the user's device... from a privacy perspective it might be better .. but all the auction stuff is happening on the user's device... can't be good from a battery and network requests point of view

Dan: arguably not great for battery life ... power consumption ... 

Amy: and just for performance in general...

Amy: I wonder if they have tested it on not the top end phones/machines

Yves: this is the auction.... 

Amy: but they don't mention TOPICS anywhere in their explainer... 

<blockquote>
Hi @jensenpaul - We're coming back to this and re-reviewing based on the info you've provided.  We remain concerned with the processing burden that this spec proposes to place on the user's device (in terms of battery life, bandwidth, performance in general).  We recognize that that's in service of privacy – however, the question remains: are these use cases fundamental enough the functioning of the web to justify adding such a complex subsystem.  
  
We recognize that this does more than the [Topics API proposal](https://github.com/w3ctag/design-reviews/issues/726).  However considering the Topics API proposal also proposes subject-related groups and this proposes "interest groups", is there scope to reuse Topics for that part of this API?

Also - interest groups are a group of people with a common interest - but we don't understand how such a group would "bid" (first bullet point in the explainer summary). It seems like as a user you would not have control over what interest group you are part of - as this is set by the "owner" of the group.  Even if the user has the ability to opt out of being part of such a group, given the number of possible groups sthey could be part of, this could constitute unreasonable [privacy labor](https://w3ctag.github.io/privacy-principles/#dfn-privacy-labor).  We've already highlighted some [concerns](https://github.com/w3ctag/design-reviews/issues/726#issuecomment-1612522047) regarding this approach in Topics – particularly when it comes to protected characteristics / marginalized groups.  It appears that Protected Audience would suffer from the same issues.
  
You've stated that relaxing the network access constraints of Fenced Frames for this API is "temporary" - what is needed to reinstate this constraint? Do you have a planned path for this? Is there a risk that adding this constraint back will be difficult once this API is in use?
</blockquote>

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/723#issuecomment-1829374317)

### [Specification review request for Verifiable Credential Data Integrity](https://github.com/w3ctag/design-reviews/issues/850) - @torgo, @rhiaro, @hadleybeeman

Yves: only about defining some usable cryptographic capabilities. I think this one should be OK. 

Hadley: the spec link they gave us was to a CR snapshot...

Yves: there are CR snaps and CR snapshots...  It's been through the CR "gate".

<blockquote>
Thanks for your extensive replies, @msporny.   

We note that your process allowing a "verifier to select from a variety of cryptosuite signatures on a single payload" does improve interop, and we are happy to see that. 

We have no further feedback on this particular review.  
</blockquote>

### [VC JSON Schema](https://github.com/w3ctag/design-reviews/issues/859) - @rhiaro, @hadleybeeman

```
Sorry for the delay on getting back to you on this. We have no architectural concerns with the JSON Schema.
```

Dan: Seems fine.

Hadley: that works.

**agree to close this review as satisfied**

### [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman

```
Sorry for the delay on following up. Have you had chance to find pointers to any work on [mitigations to the risks of malicious issuers and an answer to the suggested security question about dependencies](https://github.com/w3ctag/design-reviews/issues/874#issuecomment-1709584748)?
```

Amy: they have loads of open issues a lot of them to do with privacy... 

### [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

Hadley: being defined at the IETF... 

Amy: I think this just a bridge - extensibility for how the VC stuff can interoperate with [JOSE and COSE]... 

### General discussion on VC Specs...

Amy: we could leave feedback on these "fine"... 

Hadley: we had concerns about the ecosystem from our vc data model 1.0 review... We were concerned about inerop being defined by the proof mechanisms. .. left the whole spec open so as an implementer you can use any proof mechanism - but there is no interop between proof mechanisms... they've said thats out of scope - we said to us it's not out of scope... see [here](https://github.com/w3ctag/design-reviews/issues/343#issuecomment-531625467). I'm concerned that our initial concerns are still standing...

Dan: what's changed since then?

Hadley: not enough has changed in their model... in what they're proposing...

Yves: relies on canonicalization.. 

## Plenary Session

Present: Dan, Peter, Tess, Amy, Hadley

Regrets: Sangwhan


### [Verifiable Credentials Data Model v2.0](https://github.com/w3ctag/design-reviews/issues/860) - @hober, @torgo, @rhiaro, @hadleybeeman, @atanassov

Dan: could we alert the group to possible objections ... ?

Hadley: are the objections likely to be architectural in nature?

Tess: when they originally did the VC data model... it's supposed to be JSON-LD - you can't feed it arbitrary JSON-LD - it will choke on certain cases... a compliant with the spec VC data model processor would "choke".

Amy: I've seen that before - I don't think it's necessary for the processor to process all JSON-LD - you can pick one "expanded, etc..." 

Tess: suppose you have a non-vc-data model and you ... 

Amy: you could tell the tool to serialize it in compact form...

Tess: I don't think that would be enough...

Amy: the prefixes are set in a context...

Hadley: sounds right but need to double-check...  I'm wondering how much has already been covered in our [discussion on data model 1.0](https://github.com/w3ctag/design-reviews/issues/343)?   We closed that unsatisfied - that our concerns were not addressed...

Tess: we could see if the things we wanted addressed have been addressed...

Amy: the explainer for 2.0 has a [summary of the changes made](https://github.com/w3c/vc-data-model/blob/main/VCDMExplainer.md#important-design-choices) in "Important Design Choices".

Hadley: IIRC Dbaron had concerns about earlier versions supporting json-ld and json.. in Syntax Agility - they demonstrated that a JSON-LD processor is nor necessary.

Tess: I have concerns with that...  the way they subset JSON-LD means you can't reliably use JSON-LD tooling and have the output remain compatible with VC... you have to write a VC specific serializer... But also - most implementations are JSON  but it's weird JSON... context... If your tool chain and your partner's tool chain are just treating it as plain JSON and not checking it with a jsonld processor at some point there is likely to be bitrot, mistakes that get copied around... 

Amy: since vc data model 1.0 has been out for 5 years... presumably the justification for 2.0 is that there are changes from 1.0.  Could we ask about that that bitrot problem? They should have seen it in the wild by now?

Tess: it's a positive sign that they're moving away from implicitly polyglotting to explicit polyglot.. talking about how it can be processed as json rather than just assuming it can... 

Amy: I think it would be useful to have this list of things that make it challenging to use with JSON-LD tooling... then they could respond to that list...

Tess: you could imagine running a no-op json-ld processor that reads and writes json-ld - and randomizes prefix.. changes the pp ... for fuzzing ... all within the bounds of JSON-LD.  If you have a toolchain where you have some VC tools into some JSON-lD tool into a VC tool... you'd have to be lucky for it not to break. The Non-VC aware tool should be able.

Amy: That's a thing to ask them - maybe that's not a goal.

Tess: Then it seems weird to me ... [for interop]

Amy: Maybe but I'm not sure if that round-tripping is a goal...

Tess: But a data model - has to have keys of these names and values of these types - that would round-trip... But the json-ld stuff - e.g. prefixes - 

Amy: I see what you mean - we had similar issues with activity streams...

Tess: I'm used to formats like html ... you serialize a dom you parse the output of that and you get an equiv dom... 

Dan: postel's law?

Tess: I feel like using JSON-lD is pretty cool.  But I feel like what they've done is not using any of the benefits of it - the benefit is the ecosystem - pulling in other tools that are used to transform data - if you break round-tripping through those tools then you [don't have the advantage of using JSON-LD].  

Amy: there is a bit in json-ld - authors "are urged not to use" ... "features that are not easily detected"

> In order to increase interoperability, conforming document authors are urged to not use JSON-LD features that are not easily detected when performing credential type-specific processing. These features include: ... 

Amy: I think it's worth asking about this... presumably this language came out of not having consensus on normative language

Tess: I did have conversations at TPAC  ... Jeffrey opened issues on their repo...   

Tess: I think a lot of the things I would have raised have already been raised...  I'm happy to find what he filed and add a comment...

Amy: We can highlight that there are issues that have raised that have not been resolved if that's the case... There's a PR to address them, not yet merged https://github.com/w3c/vc-data-model/issues/1347 - remains to be seen if this will resolve the concerns

Dan: Looks like they feel they've addressed Jeffrey's concerns, there are PRs merged which link to Jeffrey's issues

Amy: any other general concerns than jsonld tooling?

Tess: steps in algorithms assumed json or json-ld last time I read it, polyglot transition wasn't clean, but that might have been fixed.. having a look to see if any are still pending

Tess: [this issue](https://github.com/w3c/vc-data-model/issues/1337) seems like it might be an issue.. doesn't sound like the PR addresses it

<blockquote>
Something something interoperability with JSON-LD tool chain. We note the language in the JSON-LD spec that discouages use of features that are not detectable. "urged to" language is weird
  
We also note that there are multiple issues that have been raised, whose concerns we share... [Do VCs still need Media Types with Multiple Suffixes?](https://github.com/w3c/vc-data-model/issues/1364) We also note that there have eeb 
</blockquote>

*Amy to draft a comment to leave on the issue*

### Sustainability of Bundling & Caching Finding

### Web Is Not Versioned Finding

### Breakout Rollup

#### Breakout A

#### Breakout C

### Issue Triage
