## TAG F2F - Wellington
##### 04 March 2020

---

Present: Ken, Tess, Alice, Peter, Yves, Rossen, David, Hadley (Remote), Dan (Remote), Sangwhan (Remote)

### Agenda:

* 14:00 (UK) - 16:00 (UK) - Breakout UK2
* 08:30 - 09:00 Arrive
* 09:00 - 09:45 DIDs and Verifiable Credentials (45m)
* 09:45 - 10:30 Plenary (45m)
* 10:30 - 10:50 Tea (20m)
* 10:50 - 11:30 Breakout 07 (40m)
* 11:30 - 11:50 Break (20m)
* 11:50 - 12:30 Breakout 08 (40m)
* 12:30 - 14:00 Lunch (90m)
* 14:00 - 15:00 Breakout 09 (60m)
* 15:00 - 15:20 Tea (20m)
* 15:20 - 16:20 Breakout 10 (60m)
* 16:20 - 17:00 Readouts (40m)

### UK2 Breakout

Present: Hadley & Dan

[trust token api](https://github.com/w3ctag/design-reviews/issues/414)

Hadley: concerns if the issuer is a bad actor.. user doesn't have control.

...reviewing current status of issue & minutes from [Cupertino f2f](https://github.com/w3ctag/meetings/tree/gh-pages/2019/12-cupertino)

https://github.com/w3ctag/meetings/blob/gh-pages/2019/12-cupertino/12-03-minutes.md

in this: https://github.com/WICG/trust-token-api/issues/10 
https://github.com/cfrg/draft-irtf-cfrg-voprf/blob/master/draft-irtf-cfrg-voprf.md

Hadley: the way i understand it is: you go to the issuer, the issuer says : i trust you. it then issues you with a series of blind tokens.

Dan: which are signed from the issuer?

Hadley: the user agent takes them out of a sec trust token response header, unblinds them, and associates them with an.. the issuer signs the trust token. when the user browses another site, publisher.com, that site can redeem tokens from another site.

Dan: this feels like it's based around unitary identity. One citizenship, one bank, etc. Hence: it would be important to have a permission mechanism involved. 

Hadley: we have that already; twitter.com has you log in with one account at time

Dan: Okay, but if I'm logging in to Medium, I have to go through an OAuth dance so that Twitter can assert that I am me, to Medium. I can choose to use a different twitter account in that, if I want. What I'm concerned about here is that I go to a website, and that website will know that all these other trust issuers have vouched for me. I may or may not want that publisher to know about that. Even the fact that someone vouched for me may count against me, as far as publisher.com is concerned. If a hostile government vouches for me, then a non-hostile government might hold that against. If [an lgbt website] authenticates me, and I'm in a country that persecutes homosexuality, then I [may be putting myself in physical danger]. It implies that every trust toke that I receive would be seen as positive information. 

Hadley: would it make sense to users?

Dan: If not, should we have it on the web? 

[similar to how governments deal with identity]

Hadley: we could explore for the EWS - should there be discrimination against someone new? Should we build into the web the assumption "you've been around so we trust you..."

Dan: which could have an implication for private browsing as well. If you want to browse privately... and websites have the tools to disallow you access based on other signals like a lack of trust tokens, then it makes it more complicated to use the web anonymously. 

...Funny, because if Tor browser are using this already, they must have some thoughts on this. Given their focus on privacy and anonymity, and resisting fingerprinting attacks. So is there an inherent design. 

Hadley: can I steal someone else's tokens?  from wapo perspective why am i bothering...  if the tokens getting presented back to the issuer to say "is this really one of yours" - it's going to end up with a random number that comes from the issuer. what if that number's not random? have i just been handed a unique id? that means the issuer who created the random number... etc... Once we get past the edges of the protocol, what if people do bad things?

Dan: yes, I'm trying to think about how people interact. The risks of breaking the anonymity are high. In the case of cloudflare, the user is trusting that cloudflare isn't passing any correlateable info to a third party, publisher.com. And publisher.com is trusting cloudflare to keep spammy traffic out. 

...I need to understand better how these abuse cases are dealt with, and why there is no need for a user UI when this stuff happens. This is info passed across origin boundaries. 

Hadley: we could also talk to Cloudflare.

#### [Raw Clipboard access](https://github.com/w3ctag/design-reviews/issues/406)

... no visible progress in the issue since 18 Dec ...

Dan: looks like the reference clipboard-api issues (52, 51 and 78) are still open...

Dan: also there is an open issue in raw clipboard access - https://github.com/WICG/raw-clipboard-access/issues/3, "not acceptable for privacy & security"

#### DIDs and Verifiable Claims (in Plenary)

Present: Alice, Tess, Kenneth, David, Yves, Peter, Rossen, Dan (remote), Hadley (remote)

(with guests from NZ Gov)

Introductions:

Alan Bell, director of digital identity
Decentralised model - new approaches
Looking at standards
Digital ID, Verified Credentials
Joanne Knight, Standards Expert - writes standards
Emma O'Connell, Policy Lead Digital Identity Trust Framework

Joanne:

In our ecosystem, looking at the ability for people to choose any (ID) provider, add multiple sets of information and combine bits of different sources and credentials to make a useful set of information for the provider.

... Currently need name and date of birth, but invariably need other attributes. Working on a system to allow flexible assertions.

... Verifiable credentials is a valuable standard for this.

... Spoke yesterday with Mattr who are working in this space. Bringing in a few other requirements that we have... currently credentials require both sides to understand credential. Credential provider could understand level of credential.

... Looking at multiple sources... provides us with a mechanism to tie things together.

... These two standards are the only ones that have been brought to our attention, were there any others that might be helpful?

Alan:

Connected with UK Verify, DTA Australia, Crown Canadian Trust. Working together on this.

Hadley: What use cases are you focusing on? 

Emma: Broader economy, not just about identity - proving eligibility, capability (qualifications etc) - enable you to share your information across the economy.

Hadley: Getting everybody who checks credentials to be able to receive as well as send credentials

Emma: About setting up trusted credential providers... if you're a service provider you know who you can go to in a trusted way.

Hadley: sounds exciting.

Joanne: moving away from the form of credentials... info not always in existing credentials e.g. income. Putting this information into a structure where we can then share this information.

Hadley: We've been looking at this for the NHS in the UK. Something we're interested in doing, need to double check this... vision behind verified credential was "self sovereign" identity, individuals in control of their own identity. Maintaining identity in blockchain to ascribe credentials to.

... Situation in NHS was that we'd have doctors and nurses who want to pick up shifts in other hospitals on a locum basis, that hospital or trust needs to verify their qualifications to practice, that they are allowed to work in UK. Right now that is a laborious process. Verified credentials process of not having a unique authority doesn't really apply - general medical council will always be the central authority there. There are parts we are finding very useful, parts less so due to existing legal structures. 

Alan: What is the status of the standards?

Tess: Verified credentials data model is a recommendation, which is the final state for a specification at the w3c. To reach this state there are requirements from w3c including implementation.

Joanne: Is it published who has done these implementations?

Tess: I don't know offhand what has happened in this case. Typically that kind of technical work is done in public in the w3c...

David: It's linked from the top of the specification, in the list of 12 things one is a link to the implementation.

Tess: DIDs is a Working Draft, more like a work in progress, it's being worked on in a working group with people from multiple vendors. It might move on and it might not. Working Draft doesn't guarantee any particular end state in the process.

Alan: No scheduling or timing for that?

Tess: DID spec is being produced by the DID working group

... Charter says timeline for use cases and requirements is to be finished in August of 2021.

... Data model and syntax is scheduled to hit candidate recommendation in Nov 2020. 

... This is a fairly mature step, this is when they think they're done and ready for implementation and implementer feedback.

... They believe they'll hit Rec in August 2021, but November 2020 is when they expect to be ready for people to start building on it.

Alan: How do you interact with (other orgs)?

Tess: W3C is one of the orgs that has a fast track with ISO

Yves: We have a few set of specifications that became recommended by ISO... 

Joanne: Which working group?

... Don't know of any W3C standard in ??? 

Yves: ... web services

Joanne: ... different area of ISO...

Emma: Would we expect this to be fast tracked through ISO?

Tess: It's fairly rare... if there was interest it could be done, but folks would have to express interest

Yves: Some other documents like WCAG are standardised through other processes 

Joanne: And through ITU?

Yves: I don't think so, see the list of liaisons2 https://www.w3.org/2001/11/StdLiaison

Alan: Want to know whether these things are going to become mainstream... interested in process, might be able to chat about this later on.

... For our advice to ministers we need to understand the process.

Joanne: DIDs and VCs are based on JSON(-LD) schemas.. might they be based on another schema type? Same principles written in any other schema?

Tess: If it did, it would be supplementary material and not in the specification...

Joanne: Principles are solid but tying in to one schema type could be limiting.

Tess: A lot of the linked data work is serialization agnostic. Could be using JSON-LD examples because it's current.

Joanne: Want to be able to capture it at a generic level that will be future proof

Tess: I suspect that for signing, particular signing statements have to be tied to the serialisation because you need a canonical form to do the encryption. I know signing statements are a big part of it.

Hadley: Looking at the spec, it looks like it's expressible in JSON or JSON-LD. JSON gives you more popular takeup since JSON-LD does but it would be less expressive.

Tess: Does it forbid other serializations? Could use RDF-XML or equiv

Hadley: Right... that would take you away from what's in the spec, but a government would have access to a number of suppliers 

... "Although syntactic mappings are provided only for JSON-LD... may use any other syntactic mappings such as YAML... "

Joanne: Need to specify the principle and not the schema.

Tess: VC group is still open... would be valuable for them to get this feedback from you, that the spec says that it's allowed, but it would be nice to have supplementary material demonstrating that it's possible.

Joanne: Same problem with OASIS (?), embedding XML into requirements. Would rather have principle, then a break, then example encodings. People could add examples. Top bit remains stable even though examples may change over time. Syntaxes may evolve over time.

... Having issues with standards being superseded, trying to get standards to be written to be more enduring and allow technology change at a rapid rate without destabilising.

Tess: this sounds like fantastic feedback for them.

Joanne: We can connect with them. We can have a good conversation with the ideas we've tested.

Rossen: Given the maturity of VCs, should be able to engage productively with them.

Hadley: Current working group charter (and activities): https://www.w3.org/2020/01/vc-wg-charter.html

Dan: Discussion about standardisation, relationship of W3C to ISO. I sit on the Open Standards Board in the UK govt, in the cabinet office. Pasted a link into our chat to UK government open standards principles process. Intended to allow UK government to bless certain standards that are specifically in the IT space that are not going through ISO or our national standards body... many standards such as this one or IETF standards that aren't going through more traditional standards. 

https://www.gov.uk/government/publications/open-standards-principles/open-standards-principles

https://www.w3.org/2001/11/StdLiaison

... Don't know if NZ has something similar, worth thinking about a parallel process to approve a standard for use that hasn't gone through ISO or other Standards process.

## Readouts

### Trust Token API

Dan: We looked at [trust token API, #414](https://github.com/w3ctag/design-reviews/issues/414).  Discussion minuted above in UK2 breakout.  We were concerned that current state of this review.

Hadley: Tess and I looked at it in Cupertino, had serious concerns.  Dan and I went through similar process today.  Do we think it's good for the web that we discriminate against sites that are new, without a built-up reputation.  It's a concept we use in identity.  Governments use identity indicators from university, bank, utility bill.  Governments trying to solve a different problem, looking for people masquerading as someone else or violating immigration rules.  We weren't clear that's how the web should work.  Trust tokens builds expectation that you're brand new.... do we trust whoever issues the trust tokens to know whether you should be brand new?

Dan: Also doesn't seem to be a verification step, or permission request step, for whether user chooses to share trust tokens with third party.  Assumptions is all trust tokens must be good -- but what if trust tokens that receiving party reveals something considered negative, e.g., past travel to a certain country.  Wasn't clear to me those things had been thought through, especially w.r.t the permissions model.

Dan: Requester on issue has responded.  Need a wider discussion in the TAG.

David: Mozilla position at https://mozilla.github.io/standards-positions/#privacy-pass and https://mozilla.github.io/standards-positions/#trust-token (may need to click to expand).

Dan: Should we continue talking about trust token, or go on to clipboard access

Peter: continue

Tess: My main interest in this has been in context of private click measurement proposal, for privacy-preserving ad conversion measurement.  Trust tokens could provide a useful mechanism for verifying origin of clicks for that, but can't speak to particulars.

Dan: How does it let you do that anonymously?  How does it both allow trustworthiness to be vouched for and that you can't be correlated with whoever the voucher is?

Tess: By carefully choosing a voucher you could maybe help that problem.  In our case, if you're getting PCM reports from Safari, it's OK for that to consume a trust token that says nothing more about the user than that they use Safari.  If we're careful about how we pick an issuer then we don't learn anything more.

Hadley: But then the conversation we had about how the user needs to have control over the issuer.  Not somebody who benefits the site but not the issue.  Potential for bad behavior, e.g, comments after last discussion about bad behavior on the part of the issuer.  Need to trust issuer to not assign different groups with different keys that indicate something.

Dan: Any browser currently implementing?

Rossen: it looks like it is being [prototyped in blink](https://cs.chromium.org/chromium/src/services/network/trust_tokens/README.md)

Dan: Hadley said in our breakout that she'd heard something about TOR browser and cloudflare.

Tess: Correct.

Dan: Is TOR browser implementing?

Tess: No, it's a plugin.  This proposal is proposing to move that plugin into the browser implementation and provide a JS api.  Cloudflare has a privacy pass plugin that it provides to TOR.

Dan: Good resources online for relearning about zero knowledge proofs?  I'm still worried about the abuse cases.  E.g., signals that person is part of marginalized group.

Hadley: https://hackernoon.com/eli5-zero-knowledge-proof-78a276db9eff

Peter: My recollection:  I can create a nonce, run it through an algorithm called a twist, ..., other party can sign, I can run signature through twist... other people can verify signature of my nonce, but other party never saw the nonce.  That's my understanding of what they're using in the trust token stuff.  But they could theoretically use a different key for signing each person and then know who each was.  They wanted to limit producers to maybe 5 keys.

Hadley: How can you technically limit the producer.

Peter: Other people can choose to trust only N keys... but then could producer still use more as long as nobody sees more than 5.

Tess: An observation for this discussion -- cloudflare built this specific solution to problem of Tor users being indistinguishable from botnets for certain kinds of browser.  Tor users typically don't want to log in to site.  Goal was to demonstrate human rather than bot.  I think they did that reasonably well for sites that trust cloudflare to handle that pipeline.  But fundamentally this is a generalization of that in a decentralized way, and there are tons of concerning scenarios when decentralized because issuers are of unknown trustworthiness.  Unclear, at least from first pass, how to overcome that.  Abuse potential seems moderate to high.  So what now?

Hadley: We started to lay it out before...  (impactful?) ... I think we can continue to explore further.  Privacy pass at IETF, could have conversation with them.

Tess: One aspect of associating with a specific person -- you issue a whole batch at a time....  So right now a bunch of sites have CAPTCHAs provided by Recaptcha.  Sites are saying they trust Recaptcha.  User who's being challenged to solve them is never given a choice about whether they want to use Recaptcha to demonstrate humannness.  Is the intention to let users choose from multiple services for demonstrating humanness, or do sites just delegate to one and nothing fundamentally changes for the user?

Hadley: We brought that up last time, got [reply](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-561325890) (reads middle paragraph in that comment).

### [Raw Clipboard Access, #406](https://github.com/w3ctag/design-reviews/issues/406)

Dan: This and the related issue on clipboard access -- last time we looked it looked like the requester was saying re-evaluating security and privacy issues.  (from 17 Dec).  Since then it doesn't look like anything happened.  That led to comment 8 hours ago.  We looked in their issues and in Clipboard API repo issues.  It looks like 3 issues I highlighted in my response on 15 October are still open.  Issue on raw clipboard access (their #3) not acceptable for privacy and security reasons is still open.  Not clear that work is going on to mitigate.  Not clear anything changing in spec/explainer.  Uncomfortable, don't know what's going on.  Is there work that's not visible to us?  Does anyone know?

Tess: I share your concerns.

Rossen: Any chatter on blink-dev?

Dan: Would be great to get feedback in issue

Rossen: Nothing in blink-dev since October.

Alice: intent to implement.

Dan: We had discussion with Alex Russell in Cupertino, frustrating but seemed to help.  Would be good to verify that.

Alice: https://crbug.com/897289 and https://docs.google.com/document/d/1XDOtTv8DtwTi4GaszwRFIJCOuzAEA4g9Tk0HrasQAdE/edit

Rossen: Active development happening but communication stalled.

Dan: Communication to the wider community has stalled.  Not just to the TAG.  Not to harp, but people in blink community point to WICG as wider review of spec work, but here that doesn't seem to be functional.  If that's true then these issues should be being updated.

## Breakout 7b

Present: Tess, Alice, Hadley, Dan

Tess: [intro'ing topic]

https://github.com/w3ctag/design-reviews/issues/426

In https://github.com/w3ctag/design-reviews/issues/426 David adds a new section to the top of the document, principles ...

Tess: I'd like to put HTML design principles here...

Hadley: it's felt like the design principles are a rallying point for the html community. If they are removed from the html will they have less impact?

Tess: definitely not. [some history:] in '06 or '07 w3c decided to get back into the game.. started html wg. Invited the whatwg people to collaborate. For several years after Ian published the spec at both orgs. At the beginning of that there was the clash of different communities. A lot of whatwg decisions questioned. Same questions asked again and again.. Some of the folks who had been involved in the whatwg effort started the design principles document to make explicit what some of the implicit principles had been. Was collaborated on in html wg. It was a distillation of the early learnings of whatwg.  HTML wg never got consensus in this. We parked it as a note. It's been a note for 13 years...

... most of it is about web technology as a whole...

... for the most part i think it captures web platform design principles. 

... it's worth resurrecting them and putting them in a living doc the group like the TAG is maintaining. 

Hadley: I think that's really useful.

Dan: yes yes and yes... and it should reference and inform the ethical web principles ...

Tess: why don't I take an action to write a pull request to add the HTML design principles en masse to the design principles document. We can iterate on them in PR> Some of them maybe shouldn't make the cut. E.g one of them is a principle of XML and HTML serialization.. doesn't impact the modern world.. 

Hadley: there is something about serializations that is worth keeping...

Tess: we start with the html principles and iterate on them...  Tie in more modern approaches from things like origin trials...

[decided to go through the principles now....](https://www.w3.org/TR/html-design-principles/)

Tess: from the introduction.. really important to distinguish between requirements on implementations vs. requirements on authors.   Fairly valuable.  Wording needs to be updated. also cf: [Postel's law.](https://en.wikipedia.org/wiki/Robustness_principle)

Hadley: we should make sure the language is clear that it's not just "the browser"

[Tess leading conversation on current principles]

for anything "kept" assume modernize wording...

1.1 - **requirements on implementations vs authors** - keep (see above)

2.1 - **support existing content** - i.e. don't break the web - keep

2.2 - **degrade gracefully** - keep

Alice: depends on if you're focusing on authoring or API design... 

Tess: this document needs to provide spec authors to provide advice to authors

2.3 - **do not reinvent the wheel** - keep

Alice: without idiomatic phrases would be nice

Hadley: if we want new people to understand then...

Alice: i think including the phrase int he text is legit but naming it an idiomatic phrase

Dan: totally agree with getting rid

2.4 - **cowpaths** - keep

2.5 - **evolution vs revolution**

Hadley: how is it different from not breaking the web...  

Tess: this is about when you're adding a new API try to make it fit in with other APIs rather then a whole new thing.

Rossen: incremental improvement 

3.1 - **solve real problems**

Alice: that sounds snarky

Dan: we talk about user needs ... in the tag reviews .

Rossen: you have to have a good supported set of use cases that solve real problems 

Tess: i think this principle isn't about use cases but - there is something you can point to in the world that is a problem - in terms of user needs. 

Rossen: don't solve 

Tess: i think it's a keep

3.2. **priority of constituencies** - keep

Hadley: can you take a look at what we said in the ethical web principles

Tess: yes and also the IETF IAB draft

3.3 **is secure by design**

Tess: I would like to add private by design 

Rossen: yes

Hadley: i suggest going for both as separate principles.

Rossen: privacy 

Dan: suggest a data minimization wording in privacy principle (reference my [data min draft](https://www.w3.org/2001/tag/doc/APIMinimization) )

3.4 **separation of concerns**

Alice: feelings on this - people have used this to justify misreadings on semantics on accessibility. E.g. people surprised by display:none removing something from accessibility tree. I think this one needs a rethink of what it's trying to do.


3.5 **DOM consistency**

Tess: i don't think it belongs here - it belongs in the DOM spec 

4.1 - **well defined behavior**

Tess: i think this is great.  Prefer to write down a single behavior that everyone should converge on.

Hadley: is this where we should make it explicit that we don't do UI?

Tess: interesting point.. Right, we don't do UI but there is a relationship between APIs and the kind of UIs you can build or the way UI can work. e.g. permission prompts.

Dan: Permission prompts do come to mind here. It also came up in discussion about the Screen Capture API spec which is so vague, trying not to define UI, it's impossible to understand what they're talking about.

Alice: references [PR 155](https://github.com/w3ctag/design-principles/pull/155/files/2708c83e5ec8f4f260bd5952fe29fa4f68e870af#r376828483) - would be nice to rephrase that ...

Tess: try to figure out how to improve based on that.

4.2 - **avoid needless complexity**

Tess: i keep citing this and 

Alice: needs to be rephrased

Tess: related to a TAG finding that captures the role of least power

Hadley: when you cite this - i would imagine people don't think something is needlessly complex. how do you convince them it's overly complicated.

Tess: by describing an alternative

Alice: "look for minimal solutions" 

Tess: yes agreed.

Hadley: use verbs  in the titles

4.3 **handle errors** - keeper

5.1 keep and possibly re-word

### Breakout 8A

?

### Breakout 8B

Present: Peter, Tess

#### [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342)

Tess: I saw this on twitter the other day: https://twitter.com/pes10k/status/1232478095333937152

... Edge seems to have an internal mechanism for grouping domains as being the same organization, and appears to use this internal, FPS-like thing for its engagement metric, so doubleclick tracking cookies don't get blocked because everyone uses google search

... I worry that FPS could turn out to be an attractive nuisance: by having this feature in the platform, implementers will tend to build features on top of this that will have the kind of bad behavior Pete called out in that tweet.

Peter: It also could take agency away from folks who, say, use a different user account on google.com & google.co.uk.

Tess: it seems like there's only one use case identified here, and I think it's a use case already solved by the storage access api. Both Firefox and safari ship it, and Edge is implementing it in blink.

Tess: [leaves comment on issue](https://github.com/w3ctag/design-reviews/issues/342#issuecomment-594222861)

### Breakout 8C

Present: Ken, Rossen

Spent some time trying to find out how the document policies were supposed to work and added some comments to help clarify.

### Breakout 9A

Present: Tess, Rossen, Yves

#### [WebRTC playoutDelayHint](https://github.com/w3ctag/design-reviews/issues/441)

Yves: it is only a hint, avoiding issues like having a too big delay resulting in abusive memory consumption, so it is pretty safe. Only issue is that it is expressed in second instead of ms

Tess: It is in the design document https://w3ctag.github.io/design-principles/#milliseconds

Rossen: Nothing wrong in that specification, sending feedback about the time unit.

#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142)

Tess and Rossen discussed at length, but did not minute the discussion. We talked about the limits of feature detection especially in cases where authors write feature detection code that assumes the current browser landscape and rough feature set are static, and/or features are mutually exclusive. In the case where a browser starts supporting some popular feature in a different way, sites that check for that feature will have often assumed that browser to have its previous behavior. These sites can break. Can we improve feature detection API shape to help such cases?

### Breakout 9B

Present: Peter, Sangwhan

#### [Service Discovery](https://github.com/w3ctag/design-reviews/issues/240)

Peter: What happened since we last looked at this?

Sangwhan: Probably nothing. (looks) - yep, nothing.

Peter: So services like Matrix use SRV records to allow service discovery on a given domain. It would be nice to have this feature exposed to the web. Could probably do this with DoH.

Sangwhan: That would solve the global (internet) service discovery problem, but won't solve local service discovery. That has popped up a lot more on the web under the context of media playback than global service discovery

Peter: Indeed

Sangwhan: Current specs don't define "how" you discover, that's sort of up to the implementer so obviously there is no common API. mDNS is a common mechanism but IIRC does not provide SRV

Peter: That use case probably is not solvable through DoH.

Sangwhan: With DoH might be polyfillable?

Peter: Yes, if someone had time... I'll try to do a prototype and possibly roll it through WICG

Sangwhan: Sounds good

#### [Media Capabilities]()

Sangwhan: I suggest we close this.

## Readouts 
### Breakout 7a 

#### [Contact API](https://github.com/w3ctag/design-reviews/issues/337) 

Kenneth: They only had a JS API and we had some comments on that. Not sure how to proceed on this.

David: It's one of those issues where we aren't completely satisfied, but not sure what to do from this point on

Rossen: When should we revisit this? 

Peter: This is the question... One of my previous feedbacks was that this could be done by simply exposing a picker. The pushback was that there is a need for feature detection.

David: I challenged this by writing a non-js feature detection

Ken: The feature is currently approved to ship with M81 of Chrome (currently in two weeks of now).

Peter: Again, shipping out of a WICG draft that's not affiliated with any WG...
... are there any signals from other UAs?

Tess: Mozilla position is Deffer (reading from issue). Apple has no public position as of yet.

Peter: Don't know what to do with the issue... Not because of the feature itself but using TAG as an excuse to sidestep going through the standards process.

Rossen: This is a good example of why we have to improve the process of TAG reviews. There must be an explicit way to associate work with a given WG that will govern the long term progress of the proposal. 

#### [Payment Handler](https://github.com/w3ctag/design-reviews/issues/425) 
David: Closed by replying to comments.

#### [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/338) 
Ken: Went over and verified some of the changes on the Explainer but didn't get far (summarizing the explainer).


### Breakout 7b
#### [Revitalizing HTML guidelines](https://github.com/w3ctag/design-reviews/issues/426) 
Tess: There was general agreement that we should resurrect the old HTML design principles and merge them with TAG design principles. We went over all principles and agreed what/how should be ported. I have been working on a PR to do that.

### Breakout 7c
#### [HTTPS and CORS](https://github.com/w3ctag/design-reviews/issues/443)
Peter: This was filed by Tim and turned out to be a bug in Blink that was since then fixed. Firefox has similar bug and is tracked. Closed as external.

#### [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471)
Peter: Extending sec ctx restrictions, CSP policies etc. in order of things to work. In general we like the idea of proposal but concerned how the restrictions are going to be turned on/off and gated. Should try to minimize complexity. CSP1 is a good example to follow. Feedback provided.

### Breakout 8a
#### [File Handler](https://github.com/w3ctag/design-reviews/issues/371)
Alice: David had good points about overlap/dependency of functionality with native file system... Links, files and mime handling. The main concern is that it depends on the native file system API that may not be implemented everywhere. Also, what would the permission flow look like. Informed consent from the user can be confusing and granted without too much care allowing access to private data.

#### [Pay For What You USE](https://github.com/w3ctag/design-reviews/issues/421)
Alice: Read and agreed with Dominic's long comment, thus, closed the issue.

### Breakout 8b
#### [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342)


