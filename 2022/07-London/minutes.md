# TAG F2F Minutes - 26-28 July 2022

[Agenda here](https://github.com/w3ctag/meetings/tree/gh-pages/2022/07-London)

## 01a

Present: Amy, Dan, Hadley

### [Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758)

Amy: would be good if the explainer gave more context.

Hadley: we can ask them.  We could also say "it looks sensible enough - no architectural problems" and [close the review].

Amy: I don't see any architectural problems.

Hadley: [channeling Danbri] interest in series - being able to represent a series - diff says they've done it. But not sure how well it's done.

Dan: [alignment with schema.org](https://www.w3.org/TR/2022/WD-vocab-dcat-3-20220510/#dcat-sdo)... 

Amy: I'm going to look at their [open issues](https://github.com/w3c/dxwg/issues/)...

Amy: Status?

Dan: "The Working Group plans to request Candidate Recommendation no sooner than 10 August 2022"

Amy: some [privacy tracker issues](https://github.com/w3c/dxwg/issues?q=is%3Aopen+is%3Aissue+label%3Aprivacy-tracker)... 

Dan: [reviewing Nick's issue on authenticity of data](https://github.com/w3c/dxwg/issues/1526) - it's a good point but is it in scpoe?

Hadley: i don't think it's in scope for what they want to do - feels like work for another working group - a substantial piece of work, but worth doing.

Dan: .. overspecialised for just clean dataset use case ...

Hadley: librarian world where everything is organised ... vs the search engine world where ...

Amy: balance between flexibility and interopability.  No way to reliably combine data... Fine with the goal of starting with clean data - and that is what this is for.  Should be clear.

Hadley: messy data not in scope - or wasn't in scope for first ...

Amy: organisations exist to help make messy data better...  As long as it's obvious what part of the pipeline this is for ... But in the grand scheme of things there's a lot more messy data.

Hadley: I'm aware of use cases... when DCAT 1.0 became a Rec, there was a lot more momentum behind data cataloges but now there's less.. more data being surfaced via non-web APIs... stand-along websites without a catalog... I feel it would be interesting to mention in our comments it would be great to hear their thoughts on how this should evolve.  Can they look more to the horizon?

Amy: they're coming at from a "data in the lab" perspective vs "data in the wild".

Hadley: rdf itself has first/next/last 

they could have used rdf lists, https://www.w3.org/TR/rdf-schema/#ch_collectionvocab but choose dataset specific terms instead. Perhaps we should ask if it's worth creating new terms (dcat:first, dcat:prev and dcat:last)?

```
Thanks for your review request. It would be really helpful for us if the explainer could go into a bit of detail about the "more pressing use cases and requests among those left unaddressed in the previous standardization round" that version 3 is addressing. It would help us to understand if/how you've accomplished what you set out to do with DCAT 3.0.

We also try to join up work across working groups and W3C specs. We see that you've created new terms (such as dcat:first, dcat:prev and dcat:last) which could instead be covered by something like [RDF lists](rdf lists, https://www.w3.org/TR/rdf-schema/#ch_collectionvocab) - could you tell us why you made that choice? Are there any other opportunities to reuse existing work in DCAT 3.0?
```

**agreed to paste and wait for response**

## 01b, spilled into 02x

Present: Lea, Sangwhan, Tess, Yves

Opened PRs: 

- https://github.com/w3ctag/design-principles/pull/379 (merged)
- https://github.com/w3ctag/design-principles/pull/380 (merged)
- https://github.com/w3ctag/design-principles/pull/381 (merged)
- https://github.com/w3ctag/design-principles/pull/382 (merged)

## Slot: 02a

Participants: Max, Dan, Yves, Hadley

#### [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/752)

Max: I have reviewed - understand it's an extension of webapp manifest - so the basic proposal to add metadata ... e.g, name of miniapp, description....

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/752#issuecomment-1195311034)

#### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523)

Max: Sangwhan wanted to have more exploration of this - we can ask his opinion when he's back. 

Dan: issue of concept or origin

Max: answer regarding it breaks the same origin principle or not... from the explanation from their answers they believe that it will not break the same origin principle. What it says in the spec - the miniapp platform 

Dan: the miniapp UA .. the miniapp comes from the origin (e.g. starbucks.com) and operates under that origin - so operates under the web security mdoel.

Max: yes that's what the authors explained.

## Slot: 03b

Participants: Dan, Hadley, Max, Yves

### [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716)

Hadley: we did our piece on this - I think we're done.

Dan: I agree - 

Yves: especially last comment - the clarification we think this is an important issue.

**agreed to close**

 [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744)

Max: I sent a comment but no response... 

Hadley: another way to get their attn.

Max: I also sent email to them.

**agreed to close**

### [Private Network Access (aka CORS-RFC1918) permission to relax mixed content](https://github.com/w3ctag/design-reviews/issues/751)

Max: a proposed mechanism for the UA to have a security role -- for example a request to access the local IP address - policy to have restriction on that but option for the UA to set that - ok for this kind of request it's allowed.  In summary it's trying to solve security issues... e.g. an attacker which could access to local IP address could change the config of the home router.  Comment: they only focus on IPv4 -- they don't have IPv6... 

Yves: IPv6 local network more identifiable - even easier than knowing the ranges for IPv4. Link local addresses.. I think the IPv6 case is simpler. Otherwise this looks good to me as well.  when you want to create something secure you need to sign something to look legit. Allowing plain http request on the local network ... to be considered secure - should be valid option. Provided your wifi is secure and noone has access to your local network. It solves issues around key management and signatures.  

Dan: Clearly. I've seen this with my printer. You have to acess by HTTP, if you want to use HTTPS, you have to self-sign a cert, and install it on the printer, and nobody does that. And then you have to install it on every machine.

Yves: Other way to do this: devices on your local network talking to a remote place to manage signatures, and... it's bad.

It will solve lots of issues. IF your local network is properly secured, it should be fine.

Dan: we close?

Yves: with ipv6 comment.

Hadley: Also - most local networks are delivered by a router form your ISP - it just works, turn it on. 

Yves: and usually proper security?

Hadley: how much existing install base breaks?

Yves: it won't break existing things... only in the sense that if you rely on something being broken it won't be the case.  

Dan: so for this to work, does anything of the newtork need to change? You could have the same wifi router with no updates to its firmware, and you get a new printer...

Yves: it's the browser that needs to know that it can do this. Nothing changes in the underlying network. 

Yves: a prompt will warn users ... in the explainer it says it's behind a prompt.

**agreed to close, Yves to wrote closing comment**

## 02b

Present: Amy, Dan, Hadley

### [Missing word in §2.5](https://github.com/w3ctag/ethical-web-principles/issues/81)

Amy: this has already been fixed. I'll close it.

### [Protect vs Control](https://github.com/w3ctag/ethical-web-principles/issues/80)

Hadley: i like the idea of control but once the data leaves your device it's difficult to control...

Amy: in the context of the sentence... "people to control their personal data"...

Dan: would "control how their personal data is used"?

Hadley: if I send personal data - i fill out a form - and the spec changes the server side processing of that form. I have the same amount of control. It may be more accessible to more people... struggling to find a way that control fits here.

Dan: is this a legal-related thing?

Hadley: maybe - legal control even if you don't have practical control - e.g. GDPR. - uses the word control but in practice it isn't control.  Just a statement that processor will comply with the law and a corresponding action the user can take if the law isn't followed...

Dan: is there something between protect and control? or if this is 'control' from a legal perspective, then it doesn't make snese to use another word. Maybe we don't want to tie too much to legal definitions.

Amy: other readings of the document may not make the connection to legal context and have an issue with 'control'

Amy: because this is in the security & privacy principles, *protect* makes sense in this context.  Mark's reason for change is that 'protect' does not cover everything, but Security & privacy is about protecting.

Hadley: I think so. If I know that this form is going over a http vs https connection then I'm going to protect myself by not using it or by putting less info into it.

Amy: "safeguard"?

Hadley: government association.. in health & social care it's about children or people who can't necessarily make decisions on their own. It's about making the decision for them, in their best interest. Which isn't the dynamic we're after in this.

### [Translation](https://github.com/w3ctag/ethical-web-principles/issues/78)

Dan: maybe not the right time for translations

Amy: Maybe more when we are further along the Statement process..

Hadley: brazillian web community very keen to have translations... we translated data on the web best practices

Amy: what process?

Hadley: someone just sat down and wrote it

Dan: other consideration is we are so wordsmithy about this doc in english. difficult to imagine how to maintain that in translation, with nuance

### [Not using principles in isolation](https://github.com/w3ctag/ethical-web-principles/issues/76)

Hadley: in response to something?

Amy: yeah the whole sustainability debate and people weaponizing principles...  A few more words just to make it clear you're not supposed to pick one issue... 



### [Sustainability Principle is anticompetitive](https://github.com/w3ctag/ethical-web-principles/issues/66)

Dan: Maybe can be closed...

**closed**


### [Relationship with Design Principles](https://github.com/w3ctag/ethical-web-principles/issues/37)
### [Suggested principles: user data freedom portability](https://github.com/w3ctag/ethical-web-principles/issues/5)

Dan: I think it's out of scope.

Hadley: I agree. We said it in 2019 too.

```
Revisited and discussed today.  While we agree with the motivations for wanting data portability, we think this is too low level a point for this particular document. Data portability may certainly be one way to help towards the "enhance individuals' control and power" principle and the "must not cause harm to society" principle, but as a general concept does not mean the same thing to all groups. Also it is not the only thing underlying these principles, and not necessarily sufficient by itself, but we are keeping each principle as concise as possible and prefer not to go into too much depth about specific aspects here. 

We note that "individuals' control and power" does mention enabling DIY developers and minimizing single points of control, which are related concepts which implicitly support some notions of data portability that have come up in this thread.
```

**posted and closed**

## 03c

Present: Amy, Sangwhan, Tess

### [File Handling](https://github.com/w3ctag/design-reviews/issues/371)

Sangwhan: should check if this already launched.. it's shipped.

Amy: there's no s&p considerations.. a single privacy consideration.. points to [File Access for lots of security stuff](https://github.com/WICG/file-system-access/blob/main/EXPLAINER.md#proposed-security-models), which says "The API provides a lot of scary power to websites that could be abused in many terrible ways". [Google doc for file handling security](https://docs.google.com/document/d/1pTTO5MTSlxuqxpWL3pFblKB8y8SR0jPao8uAjJSUTp4/edit).

```
We apologize for the delay in getting to this review request. We note that it has [shipped in Chromium](https://groups.google.com/a/chromium.org/g/blink-dev/c/Wxuo4lZi4vM) but that there are so far no other implementations. Please let us know if you expect to progress this along the recommendation track at any point, and if/when other implementer interest emerges.

While the security and privacy questionnaire has responses, there are no security and privacy considerations sections in the spec itself. The responses to the questionnaire indicate how potentially private/sensitive data may be exposed, but there is little discussion of threat models or mitigations. We see this discussed extensively in [this document](https://docs.google.com/document/d/1pTTO5MTSlxuqxpWL3pFblKB8y8SR0jPao8uAjJSUTp4/edit) and it would be reassuring to see actionable considerations / tradeoffs for implementers succinctly documented in the specification itself, or at least references to other documents if that's more appropriate.

We will be happy to review further changes and additions in a new review request in future.
```

Amy: suggest closing satisfied with concerns

## 04a  Privacy Sandbox

Present: Yves, Lea, Hadley, Dan, Amy, Tess, Sangwhan, 

Guests: Johann Hofmann (Google), Josh Karlin (Google)

**round of intros**

**johann presents slides overview of Privacy Sandbox**

Johann: I want to overview the ecosystem. Try to represent views wider than google, but not always.


... Privacy Model. Everyone has tried to define privacy in various ways. There have been some good attempts. There are various properties that are not as much looked at right now. We're focussing most on tracking. Cross-site recognition, linkability. This is practicaly what we are most concerned with. Partitioned identity between different contexts - Michael Kleber. Central privacy threat is joining these identities across first parties. Eg. NYTimes.com should not be able to recognise me as the user who also visited cnn.com. Not just NYTimes.com, but any embedded content. That's something we can't guarantee right now on the web. That's the central threat we're talking about.


... Michael Kleber is a principal engineer at google defining a lot of ways we're thinking about privacy in the context of privacy sandbox. https://github.com/michaelkleber/privacy-model


... Tracking can happen in different ways. There are various attempts at categorising. Some may split this into different subcategories. I mostly agree with these four general types. **Stateful tracking**, the most common, mostly focussed on with browser interventions. Eg. cookies, cross-site storage. Sometimes unintentional storage types. There is **stateless tracking** - fingerprinting. **Navigational tracking** - used to transfer identifiers through other means across sites. A query param on a URL. Some social media sites do this - transfer an id in the URL bar so an embedded script can recognise you. Then the least explored is **PII based tracking**. Some tracker will either directly ask you for personal info or try to extract it from the top level site, eg. you entered your email address in the DOM.


... These are important to understand.


Dan: question about how this relates to some of the definitional stuff we've been working on in [privacy principles doc](https://w3ctag.github.io/privacy-principles/). Eg. we minimise the term PII because there's a legal definition... doesn't need to be a long discussion. Want to make sure you are synced internally.


Johann: I can talk about how we define this.. I can take this to Shubhie. This is the simplest way to define it. Whether that's how we want to formalise it is a different question. Sensitive topic we need to be careful about. 


Tess: I noticed you are restricting your definition to tracking to cross-site tracking. If you look at webkit's tracking protection policy, there is a distinction - cross-site tracking is a subset of tracking. Stateful tracking, there are two kinds. Using storage mechanisms for their intended purpose. But also covert - using hsts or things like that. So in th ewebkit policy we try to say cross-site tracking or covert stateful tracking, even if it's same site, we try to event both


Johann: evading cookie clearing? I agree that's important to add. Looking at the problem at scale, I'd claim that the larger problem is cross-site tracking. Trying to evade cookie clearing is something we should fix, but maybe not what the larger ecosystem is trying to fix right now.


Tess: I'm recommending that you do.


Johann: I'd say this is more of an edge case vs the larger problem of cross-site tracking. But I agree.


Hadley: in th econtext of PII based tracking, are you thinking about.. you've talked about PII that is in this browsing context, in this interaction with this particular site, are you thinking about PII that isn't necessarily a part of that discussion? Eg. if you are an advertiser that has managed to work out that i have a subscription to a magazine and therefore my address is i nthe mix, is that in scope? Or ..


Johann: this is not a roadmap. We're not saying we're fixing all these. just an overview of things on the web. This is something everyone should have on their plate if they want to be working on fixing tracking. But with different orders of priorities, they have various difficulties attached to them. We can definitely make other categories.


... The big problem that everyone has is that they are used everywhere. Not just some fringe API we can turn off. The whoel web relies on these technologies. For intentional tracking and data collection for advertising use cases. Anti-fraud, is considered as tracking. There's an entire flourishing web ecocystem supporting creators and authors by using technologies and techniques that we don't necessarily want or would like to see on the web in the future. That's definitely a problem. Related ot that problem are the compat challenges when deprecating the apis that enable this tracking. It's not just chrome, anyone who has shipped interventions, reduction of privacy invasive apis has seen this kind of impact on their browser. Everyone is looking into ways to minimise that impact, otherwise we can't move becuase too many sites are breaking.


... Even Tor who is on the stricter side of privacy has been thinking about breakage a lot. Something on everyone's mind.


... Leaning from that is another problem - cat and mouse game. As browsers restrict, developers shift their strategies to something else. They want to address a business need. They're going to keep doing what they do and find som epath to it. That affects both developers who use tracking, and developers of non-tracking use cases who happen to use these apis, as browser vendors step up their interventions. There is some path of least resistence mechanics. Trackers and non-trackers, when taken away some api there will go another path of least resistence to do their business. Maybe we can show th eecosystem a path of least resistence that is better and does not involve privacy invading, under certain limits and guarantees that we are comfortable with. 


... that's why it' simportant to develop privacy interventions as well as privayc preserving apis. That's the privcay sandbox vision. Strong restrictions to apis that are being abused by tracking. But also give sensible and good alternatives fo rthe web ecosystem that defends sustainability of the web and also preservers other use cases for technologies that look similar to tracking.


... Browser interventions. Things we ship in order to prevent sites from tracking users. Involves lists of a lot of things. Challenges. Unshipping is hard. Preventing someone form using something they were using is very hard. These things are highly used / popuplar. We can design interventions in a way that compat issues are reduced. Design in a precise way so that only the tracking use cases are affected, or in a way that the functionality is preserved but tracking is impossible. Takes time and is complicated. COnsider this when we think about decisions browsers are making.


... Stateful tracking has seen the most progress, and browsers are aligning pretty well. two general approches - first is blocking. If you have some iframe or third party resource in a first party context that wants to access a 1p cookie, it's not allowed. Safari shipped some time ago. Other approach, eg. by firefox, is partitioning. Instead of saying no cookies, you say yes you can access some cookies but these are in their own separate cookie jar. Own jar at the top level, if the user browsers to that site in the url bar. a separate one if you're embedded in some other context, and another one in a different context. That is thought to have better web compat. iframes and 3p resources can still use cookies, but they can't invade privacy. But reality is it's not actually the case, developers may be more confused about the properties of partitioned cookies than outright blocking. Looks like ecosystem might be converging on blocking 3p cookies by default, and partitioning 3p storage. Seems to be where people are going. Internal plans from Chrome, and verbal committments form firefox.


Tess: [CHIPS](https://github.com/w3ctag/design-reviews/issues/654) allows you to opt in, so websites who understand partitioned cookies can use them if they want, but you don't get them if you're not expecting them.


Johann: right. That's something browsers also seem to be aligning on. I think it's good. 


... Stateless tracking is a bit fractured. Nobody has converged on a single strategy. UA string.. Non major browers adopt UA string from major browsers, helping to reduce exposure. IP address.. No standard or agreed solution - proxies, vpns; [Gnatcatcher](https://developer.chrome.com/en/docs/privacy-sandbox/gnatcatcher/) -?]. Fonts, language. Tons of other fingerprinting surfaces - individual browsers experimenting. 


Dan: this is something the TAG often feeds back to people when we get a review request - did you think about fingerprinting surface area? 


Yves: recent one about fontpicker


Johann: Navigational tracking is pretty unexplored. Query parameters are sometimes stripped based on blocklists. Safari detects them and caps the writeable storage. Bouncetracking often also uses query params and there are some mitigations. Space where browsers are starting to ramp up efforts and get effective. Right now doing navigational tracking is not that hard. Referrer string a lot of browsers already restrict to the origin.


... How are we standardizing those? There are a few efforts we are successfully standardizing. For stateful tracking we have been doing a lot of work with different browsers to improve the cookie RFC. That is not necesarily anti tracking work but paves the way for improvements we want to make. RFC2625bis is being finalsied and that will help with interop problems between browsers, and then we hope we can converge on a few changes such as CHIPS and specifying how cookie blocking works. Proposal from Anne about cookie layering in IETF, which would involve pulling cookie stuff into w3c. Would help to bridge some gaps, but very early right now. 


... CHIPS is something we are aligning on. Storage and network partitioning have been successfully integrated into html and fetch specs.


... Stateless tracking, a few efforts. Documents and guidance to help new apis protect against fingerprinting service. Some Chrome folks working on UA reduction from all browsers standardised. The compat spec.


Yves: about sotrage partitioning and network partitioning - we discussed recently that partitioning had an adverse effect on sustainability becuase of the extra download and space used. I remember we discussed that in the case of storage partitioning, cache information about timing and some fuzzing random timing around that would be a way to avoid spending too much resources while keeping privacy in a better way, to simulate partioning without doing it explicitly.


Johann: Agree. Chrome hasn't shipped that yet. There are some perf and sustainability components which increase the number of requests. The mitigation, I'm not sure I can speak to that, not familiar. Other browsers have shipped it. There are things to fix. Proposals such as being more generous with network partitioning. in FPS you could share a network partitioning key, so the effect is reduced. If you kno wthese sites have embedded resources that are shared you could utilise that and lessen impact. How do we ensure privacy without making the tradeoff with perf and sustainability, is something to work on.


Sangwhan: this mitigation in the draft finding - there wa sa positive signal and inviestigations going on in the chrome team. They did comment. The reason why double keyed caching was introduced as a privacy feature was becuase you could ook at the fetch timings and determine whether this user has visited. The mitigation was keep the fetch timings, add some random noise, and then the site won't know if it came from the disc or the network


Johann: that's why we have triple keying.. with the mitigation you could just have double. Now I understand, that sounds good.


Josh: My team wound up doing the work of partitioning Chrome's cache. Safari was there 5 or 6 years before us. We did wind up triple keying. That was largely for security reasons as opposed to privacy. We found very little impact on perf between double and triple keying for the main frame. The third party iframes were slowed down. I talked to Anne vk, there's an issue on it in privacy cg about the right thing to do. unload is the timing leak. We discussed maybe we fix that in general, it's a huge cross site origin leak. I agree, that is a thing we could do. I don't think it's a trivial thing to fix. For now the network keying seems more straightforward. I'm definitely interested.


Dan: on UA reduction, which has kicked up some controversy, is there anything going on at the standardisation level? a CG or anything? 


Tess: some discussion in privacy cg. Mostly each browser doing what they think is best with little coordination. And Mike Taylor's work on compat spec to write down what everyone is doing and harmonise after


Dan: enough coordination?


Johann: folks know each other, but not talking about doing the same thing. Compat spec has a section for what each browser does, and documents that. ideally we'd have..


Tess: an effort to drive delta to zero


Dan: I do think there is something to the point of this work on harmonising the UA should be done in the clear subject to public comment. 


Tess: the work Mike is doing is public. In the WHATWG compat workstream. And privacy cg is public. Even if we drive the delta down I'm guessing it won't end up at zero. there are some disgremeents about to what extent it's okay to break UA detection.


https://compat.spec.whatwg.org/#ua-string-section


https://github.com/whatwg/compat/issues?q=is%3Aissue+is%3Aopen+uastring


Dan: yeah. 


Johann: I'll mention that to Mike. We can increase that effort.


... The well lit path. Alternative APIs browsers are developing to privacy invasive technologies. We're taking a lot of things away as we progress. We need to keep websites working. And enable sustainable business models, but should not come at the expense of privacy.


... There are a lot of APIs. Hard to have a complete overview. **Use cases specific**  - eg. FedCM, with user stories, and **general purpose APIs** - eg. Storage Access API, more designed for developer use cases. That enables APIs to make different tradeoffs. Use case specific ones can reduce the information, use privacy preserving techniques like differential privacy, to tailor/reduce/rate limit information. general purpose apis don't do that, but are the privacy boundary. The user gives consent and that lifts the privacy boundary.


Tess: yes, and.. you want the use case specific things because you can make assumptions about what is happening. You want also the escape hatch of a general mechanism for when you didn't anticipate the site's needs.


Johann: looking at general purpose apis that are out there right now in the chrome case. Eg. fenced frames, shared storage, are underlying mechanisms to the workstreams being developed. They could be used for other things but are primitives that power higher level use cases for ads.


... Also [UA client hints](https://github.com/w3ctag/design-reviews/issues/640) [nb review was closed with concerns by TAG], which is Chrome's proposed solution to the UA reduction problems. For those folks who are affected by reduced UA strings, which should be a minority, but how can they ask for that information from user agents. Interesting idea behind this - passive and active fingerprinting. If you just the UA string as a server then you're participating in passive fingerprinting. You get this information whether you request it or not. Active is you actively asking for the information. The advantage from turning passive fingerprinting into active is browsers can react to the request better. Privacy budget proposals says if we turn all passive fingerprinting into active we can rate limit so it's no longer privacy invasive. 


... Storage access api - you have an async request saying I want sotrage access, th ebrowser can decide what to do. Often gated on a few restrictions, the final one being user consent.


... [FPS](https://github.com/w3ctag/design-reviews/issues/342)** is another privacy gate, gate**d on sites preregistering a group owned by the same entity that are related to each other and have predefined trust.


... Use case specific areas, there are a lot. Work streams - Identity - discussing how to preserve federated identity, logins; Fraud detection - anti-fraud cg and wicg, trust tokens, how do we enable the fraud detection industry, which is a giant problem on the web, without privacy invasive techniques; Ads Relevance - showing better adds, and Measurement and attribution. A lot in the ads workstream.


Josh: there are a number of use cases. nice to see a picture of how they come together. When you're serving an ad, you wind up using all of them. When you want to display an ad to a user the first step is selecting an ad. You want it to be personalised to be more effective. We need a private way to select and personalise an ad. You can use the topics api to get topics relevant to the context, or you can use **[FLEDGE](https://github.com/w3ctag/design-reviews/issues/723)** which helps you to find marketing sorts of ads. So you get a couple of ads, or a list, and then from there we have a way to filter them down - **[shared storage](https://github.com/w3ctag/design-reviews/issues/747)** is a mechanism for that. Given a list of 8 ads, which is the best? Shared storage has lots of cross site information about the user, but all it's allowed ot say is: show this one. It can take into account information like how many times it has already shown a particular ad - frequency capping. Or it can say a user is in an AB test and show them one with a different colour background. Shared storage can say this is the experiment group the user is in. Shared storage used to filter down. Then to display the ad. But it's personalized, so it used cross site information to choose it. We don't want the embedding page to actually know what ad was selected, because then they learn something about the user - so we stick it inside the **[fenced frame](https://github.com/w3ctag/design-reviews/issues/735)**. It's an iframe that can't talk to the embedding page. That's a way for us to compose two sorts of partitions into a single page. Where normally we would not allow two partitions together, and we can do this without a prompt because they weren't allowed to talk to each other.


... So we've displayed an ad. The two other components are measuring performance. Digital advertising compared to a billboard is valuable because you can measure your RoI. I showed it to 2000 users and 1000 bought the product. It's very exciting for marketers. They can see they are getting their money back. You also want to be able to detect fraud. And to register the fact the user saw the ad so you don't show it again. Bumping the count of user saw this ad. Also want to measure how long it was visible to the user. 


... From within the fenced frame you can record things - impression. That's useful for measuring. You record that they saw it so you don't show it too many times. Upload a trust token to say yes this wa sa user that has bene verified by the ad tech in question so they are less likely to be fraudulent.


**[attributtion reporting API](https://github.com/w3ctag/design-reviews/issues/724)**


... Page navigates in a new tab when the user clicks. The user buys the thing, so more measurement needs to happen. Combine impression with conversion to register this ad was effective. That's the general flow. I know there are a lot of apis, there are a lot of steps involved in serving an ad in a personalsied way.


Dan: how does FLEDGE and TURTLEDOVE relate? TURTLEDOVE is the old name for FLEDGE?


Josh: you can think of it that way. Turtledove is a general client-side auction strategy, fledge is the first go at that.


Hadley: this is really helpful for all the context. It's clear from what you've said that you are intending to create an ecosystem that is more privacy preserving, that we can evolve to, in which advertisers can still make money and sites can still be funded. But as we looked at a number of these apis initially, without that context, I was concerned about adding new additional forms of tracking. So all of that concern goes away if we say this is where we're going and we just go there. How can we be confident that we are going to make this migration, rather than end up introduction a bunch of additional tracking tech?


Johann: Having 3p cookies on the web is exposing capabilities that I don't think we should exceed in any of the new apis. The fact that you already have these capabilities, you just need to custom build your solutions. You could do topics - it's a slightly worse version of what you can do with 3p cookies. I get that adding these apis are adding more. But from a threat model perspective it's not adding additional capabilities. The capabilities are already there in the form of 3p cookies. One principle behind topics is thsi observaibility principle. Sites have to have observed a specific topic somewhere in order to obtain it. If we didn't have thta it would add additional capabilities that go beyond 3p cookies.


Josh: a funky part of the apis. Diffecne between floc and topics. We were uncomfortable with the fact that sites could observe things that they could not have using cookies. In general we want to make forward progress for privacy. we realise and accept there are a lot of apis and each are leaking something. we're building up these partitions and these apis are poking holes in some of that. we understand that. From our perspective it's going to take time but we're making incremental progress toward a more privacy safe browsing experience.


Hadley: helpful, but still leaves me unconvinced that I won't have to cope with worrying about both third party cookes and everything you have laid out.


Josh: 3p cookies are going away


Johann: some browser vendors will say lets first unship 3p cookies then poke the holes back in. Chrome is taking the approach that we have to work with the ecosystem, work with devs, before we take things away from them. I get that aspect that the timing will be very close. A lot of these apis will be available before chrome deprecates 3p cookies. For a certain amount of time you'll have that situation that you're uncomfortable. From a rational threat model perspective, not thinking about how I feel as a user, we're focussed on not adding additional capabilities that 3p cookies are already giving sites. I can understand, but if you look at it rationally that thread does not exist.


Dan: to build on what Hadley was saying. If we look at fenced frames, one of the questions that came up in our review is [what will motivate developers to move to frenced frames](https://github.com/w3ctag/design-reviews/issues/735#issuecomment-1154890182). If you already have an ad network out there telling publishers use this thing to dembed our ad, why would they choose to move to a lesser capable mechanism, unless they are forced? If we think about it form that perspectiv,e why would they ever be pushed? Will the pushback on the push be such that they are never pushed.


Johann: how will we push developers to use the new apis before 3p cookies are removed? I can't talk in terms of precise dates, but I can confidently say that it won't be a scenario where we wait for every single developer to have converted. The stick and the carrot is important. There ill be a deadline, and a date that is communicated. Hopefully that announcement is enough to convince folks to switch. If they don't, from a privacy perspective that's a win, beause they can't use 3p cookies.


Hadley: that deadline is when you  stop 3p cookies


Josh: the incenvitve to use fecned frames is that fledge and shared storage both select an opaque url - you can't just embed it in an iframe. At the moment you can for debugging. But in some short amount of time it will no longer be possible to have this ad displayed in anything but a fenced frame because only a fenced frame can show that URL. [DKA: this seems important]


Tess: From a very high level - strategy is to address the use cases and then drop 3p cookies. One question is are there any use cases that you're willing to not address. Like to say we got these, but this one, although legitimate, we have to ship this at some point. The 3p cookie removal deadline has already shifted by two years at least once. I think it's easy from the outside to get the impression you'll just shift that 2 years every time becuase you'll never have all the use cases addressed, and effecitvely never drop 3p cookies.


Johann: hard to speak deifnitively


Tess: are there must haves and nice to haves? or is everything a must have?


Josh: Not every use case has to be met. But the APIs we’re currently proposing support some of the most important ones. For the things we can't make apis for, we’re considering escape hatches for.


Johann: things you can see on the privacy sandbox website today are things that are locked in and weill be at a reasonable state before 3p cookie deprectation. What comes additionally or after is a question fo how does chrome evaluate whether a feature is needed o rnot. There may be the case where some developers make a convincing use case that we haven't considered yet. Then certainly some apis added to the list. But there's always a bar. There are features we have in the past not considered 'worthy' of being solved in the browser. 


Hadley: in the context of ethical web principles, about users being empowered to manage their experience on the web, and protect themselves. We also talk about keeping the web simple and barrier low for new developers. What you've got here is reasonably complex. Have you done user reasearch with those groups? Any sense of how this is going to be received?


Johann: for ads specifically... the general purpose apis, ua client hints or fps, are reasonably simple to use for less experienced developers. 


Josh: we are making this more difficult, no question. FLEDGE in particular is a whole new can of worms for a lot of ad tech. But we are seeing a number of companies interested


Hadley: ad companies?


Josh: yes. There is some amount of technical expertise required. The number of what we'd call adtechs that sit on the users page and run js is relatively small. They are pretty tech savvy. We have not come across a problem with people just throwing up their hands. it is challenging to do this. It's all new. The clientside auctions are completely new. Adtech hasn't actually tried doing it and seeing if we get the performance we're expecting, how does the fraud side change and all that. A lot of where we are now with our origin trial is does this have any chance? Does it work? Can tech companies use it? that's the feedback we're looking for.


Johann: FedCM I think does make it easier for small devs to integrate with id providers. Not sure if it's just copypasting a lot of code in a lot of cases. Should give the option to integrate with several providers more easily than using custom code for every single one. Fraud detection is very early.. and trust tokens.. also a very specialised industry.


Hadley: complicated concept, rather than complicated api. one thing to say here is an api, another to get an entire ecosystem to depend on 


Johann: good thing about anti fraud is it's really driven by those in the anti fraud space as well as web browsers.


Sangwhan: in attribution there are three different competing things?


Dan: we got a review request, #724, for attribution reporting api - looks like there are a bunch of different things. Is there any effort going on to bring these together? Is there multi party consensus? Multiple implementations? Looking at this slide, it's worrying when we're talking about things developed by different browsers


Tess: i get where you're coming from. At least in the attribution measurments stuff, the PATCG has this reason for existing. Making that go down to one or two consesnus solutions is the whole reason people go there.


Dan: in which case is it premature for us to be reviewing the attribution reporting api? When in fact there migth be work going on in patcg to converge that with some other things, which would be great, but maybe then better for us to review.. a matter of formal review proess vs tag feedback. The feedback is you should converge thse things. Deep dive review would be better after convergence.


Sangwhan: this is one case where the blink launch process, we should focus on convergence rather than unblocking blink launch process


Tess: when will you bring PCM to tag for review? I think it's too early. Judgement call. I don't expect what PATCG ends up with to look like any of these.


Dan: a technology you mentioned - and why we might be reluctant to say it looks great, please let us know what the results of the experiment are - that's what we said when we got initial review on fps. Our feedback was 'interesting concept', and the next we heard about it was we're building these other things on top of FPS. That was an example of where we felt the review process wasn't fitting in well with how you all think about it.


Johann: I appreciate you saying that. Helps to have that context. What you're describing we still see as experimentation with FPS. There's part in the blink launch process that says you have to have TAG review. People are happy when they have an easy path forward. They don't see the positive inital feedback as they don't have work to do. We are still experimenting with FPS. It's still unshipped. Same-party is probably what you're referring to? FPS is a concept, that alone doesn't give the browser anything if you can't use it in some way. So the experimentation is how can we use it? Same-party cookies is one approach - a drastic appoach - we use it by unblocking privacy boundaries between those. That conveniently solves a lot of problems. We get the concerns people have. 


Dan: on the positive side, where things have gone well is with CHIPS. CHIPS was initially 'entangled' with FPS and based partly on our feedback maybe the work is going on to disentangle it, and that unblocks the positive feedback we can give. That's a good example, espeically when we can see aspects of multi stakeholder support.


Sanghwan: also good to see multiple stakeholders considering this a problem.


Hadley: existence of those three community groups is a good thing. Surprised we don't have a WG.. but maybe best it incubates elsewhere, because of the membership.


Johann: I think because it's early. Will be something eventually.


... Point about CHIPS - generally so far has gone well. The FPS integration, it was minor, but we're experimenting, that hasn't stopped. CHIPS+FPS was super convenient for some use cases. but seeing that the ecosystem isn't positively adopting it, doesn't see it the way that we do, there's certainly the mindset with some folks at chrome that it's not good developer experience if it's not interoperable between browsers. We consider that going into the future.


Dan: Feedback that could help us is about where we should be spending our time? What is prioritisation of reviews? What can we be expecting? Where do you think we are misinformed? Are there areas where.. eg. already I feel I know a lot more about context of attribution reporting. I understand much more about this opaque URL thing that I didn't understand before. Are there other things like that?


Johann: fenced frames was one thing we wanted to mention for sure?


Sangwhan: Private Aggreation is missing


Johann: very very early


Josh: it is a way of sending encrypted reports that can only be read in an aggregate manner. You get a histogram of this many users saw this many ads of this nature, as opposed to individual user responses. Instead of an event level user saw this thing, as a group we counted this many ad impressions. Uses in the backend multiparty computation or some trusted environment to do aggreagation of encrypted reports, and you get back ahistorgram.


Hadley: so you need a third party to collect the data?


Josh: the adtech collects them, encrypted, you can't read them, and send them on to get aggregate results


Johann: that's howh the mozilla and attribution reporting proposals also work. Underlying idea that you have trusted server that participates in a positive scheme where data is divided up and multi party computation anonymised aggregated and in chrome you have these trusted execution environments for running aggreagation servers. The Safari one is the only one that has event level maesuing that does not involve a third party. SEnds out events that contain small peices of entropy.


Josh: Chrome's also has an event level, but we'd like to focus on the aggregate in the long term.


Dan: in fenced frames. The opaque url thing - where is that concept enshrined besides in the fenced frames spec? There's a separate explainer about opaque source. I'm wondering is this a primitive that might be useful elsewhere on the platform?


Josh: We had originally in our minds this was a js object that you could return. The browser knows what's behind the object but the js doesn't. Instead we wound up using something preexisting, a urn uuid. You have this URN, it's meaningless, but there's alookup table in the browser ot map that into a url. We don't have other use cases yet other than fenced frames for this sort of thing. I don't know what the approach that the team is planning on taking for specifying this part of it is.


Johann: we can take the question back


Dan: we can leave this as part of our feedback. 


... Can you tell us about topics vs fledge? Are they for two different sets of users needs? Or will they converge?


Josh: Topics is about high level general interests of the user. You can show up on a page you've never been to before, it has its own contextual information. We also know this user is interested in high end shoes or something so we can show a shoe ad that is more valuable. There are 350 topics in the taxonomy. That taxonomy was a first stab at something. Tried to make sure it is not google centric. Took an intersection of the IAB taxonomy. We had to include google's taxonomy because that's all the data we have for training. It doesn't make the most sense yet. We'll improve. The API maps user browisng history to topics and provides different subsets to different sites, so we can advertise to something a bit more personal to the user.


Hadley: subsets of what?


Josh: subsets of the topics. The user went to these pages in the last week, we map those pages to topics, then calculate the top topics visited in the last week and come up with 5. Every site you go to if they call the api they will get one of those topics from the past week. In total they can get three. 
 One is chosen and it's sticky to that site. CNN.com will always get the same topic for that week, but Apple.com might get a different topic for that week. Different data makes it hard to link the user. 
 
.. That's topics. High level information. FLEDGE is about re-targeting. Imagine going to a site, almost buy an item, but you don't hit the purchase button. They want to show you again this thing you almost bought. A particular product they want to show to this user again in the future. You add this interest group - a group of users, not just one user in this group - that are interested in this item. I would like to in the future when someone with this nterest goes on this page, show them an ad for this thing. Every user winds up in a list of interest groups. This list is very user identifiable. It's kept on the client. The browser has this list of interest groups. WHen it comes time to show an ad in the future based on these interest group syou call fledge, run an auction and let the advertisers that are interested figure out how much they are willing to pay, and let the winner be displayed in a fenced frame. Much more targeted towards this particular user, does not leave the browser, and you wind up covering the retargeting use case. You could theorietically, in the long term, have a topics like thing suported in fledge. Would take a lot of tweaking. You could say the user is interested in the general category of cars rather than this car they almost bought. This interest group represents tens of thousands of possible ads and fledge would be able to handle that - not feasible at the moment, but maybe long term.


Hadley: why not at the moment?


Josh: huge swathe of advertising.. ten million possible car ads, let me choose one.. that much data on the client is not something we currently have support for.


Sangwhan: why so many competing proposals for this particular thing?


Josh: the server can have way more data and is faster. Microsoft is looking at it from the perspective - PARAKEET - that the auction needs to run on the server. They want to upload all th einterst groups th euser has in a way that is private, let the server figure out the ad, and return it to the client. W'ere interested in them doing this, and they're going to have an experiment of their own, and we're going forward with fledge, thinking it needs to remain clientside to retain privacy. Not aware of other retargeting apis other than those two. at TPAC both Microsoft and Chrome will be talking about their approaches. Not at a point of convergence yet, but see the potential in the ideas.


Hadley: which part of tpac?


Josh: WICG meeting.


Johann: I said PATCG though some still live in WICG. Plans to move them?


Josh: First thing is to get them out of personal repos. WICG is step one. Topics is kinda sorta in PATCG, they have not endorsed it. Not much gain by being in PATCG vs WICG until PATCG decides to take it up. They are focussing on one issue at a time to try to make progress. Hard for CG to handle all the use cases. At the moment we have others in WICG. 


Dan: to reinforce - we really encourage things to be not in a private repo. Sure WICG is a good first step, but we encourage to think about the trajectory. If you're going to go into the standardisation process, with better IP protections, it really needs to have all the.. multi stakeholder stuff.


Josh: an issue is we're not getting a ton of multi browser support for these. Topics is a chrome initiative. I don't know how that plays for you. I'd like to think we've had a good interaction. We got a lot of great feedback on FLoC and have iterated since into topics which is a far better approach. I feel like that's been fruitful, but still one browser.


Dan: we like to see things in places where there is strong multi stakeholder participating. If there's a privacy realted thing I'm much more comfortable hearing that it's in the privacy cg vs in WICG. Seems to indicate more stakeholder interest. In general, TAG doesn't say we're not going to review something unless there are multiple stakeholders, but we want to be a force to try and promote multistakeholder, because of the requirement for the standardisation track. There are a lot of things in WICG and no weekly calls.


Johann: yes. WICG has a low bar to participation so it's where a lot of those proposals end up, and so google has big representation in the group. There are proposals in WICG that have multi implementer participation. In the privacy space we arrived on CHIPS which has moved to privacy CG. Doesn't speak to the quality of the proposal. Sanitizer API is in WICG.. You're right, trend is clear..


Dan: we're reviewing stuff in WICG, that's the case.


Hadley: has a wide variety of stuff at varying levels of maturity


Lea: we do plenty of early reviews


Dan: we want to get earlier reviews


Lea: much easier to change things. Sometimes a problem people don't come early enough. 


Johann: We really do appreciate TAG review. Sometimes some time can pass, and even if it doesn't seem like it we are making progress in terms of taking feedback into account in terms of cross browser implementation.


Josh: a takeaway for me which was useful is that I understand now the concern about putting the APIs out there while 3p cookies are still there, increasing fingerprinting surface. I can see it's less clear. These APIs are less capable. The fingerprinting surface is less capable than 3p cookies. I'd strongly argue there is not much purpose at all to these apis if 3p cookies exist. We are introducing them first to see if they could do the job, but they would go away if 3p cookies didn't go away. We're introducing them first to make sure we can cover the use cases.




## 06a

- Closed https://github.com/w3ctag/design-reviews/issues/741

## 06c

### [Review request for HTTP Status Code in Resource Timing #757](https://github.com/w3ctag/design-reviews/issues/757)

Yves wonders how this fits in with Fetch's hiding of this information

[Tess & Yves read explainer & related docs]

Yves: this allows you to distinguish between a CORS check failure and some other server-side failure

... for things not using CORS (images etc.), you can kind of figure this out, coarsely, by detecting if the resource was loaded

... would be nice to have mike west's read on this, or anne's. it opens the can of worms of differentating errors

[Tess & Yves each leave comments on the issue]

### [ContentVisibilityAutoStateChanged event #756](https://github.com/w3ctag/design-reviews/issues/756)

Yves: can't you do this already

Tess: yes, with IntersectionObserver etc., but it would be clunky & error-prone

[... discussion of what would happen if you had old code doing this the hacky way and new code doing this the new way on the same page ... we eventually concluded that they've covered the relevant concerns, at least as far as we can tell.]

## 07a Privacy sandbox ctd. & TPAC planning

Present: Peter, Dan, Hadley, Sangwhan, Rossen, Tess, Lea, Yves, Amy

### [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742)

**peter leaving additional comment**

Peter: ads to detect they are in a less restrictive env.

Tess: It's not much of a stretch - we know there are actors out there who will get away with whatever they can get away with.

Peter: making it easier to do the bad behaviour - is the jist.

### TPAC

Dan: Dom is organising an ethics session. Tentatively thursday so Dan can attend.

Who is going: everyone except Amy is 'probably'

Dan: should we request a room?

Tess: be nice if we can find a space but they don't need to drop everything to find us one.

Lea: easier for me to get funding for a formally scheduled meeting

Dan: **writes email to Alexandra**

Dan: which other [groups](https://www.w3.org/calendar/tpac2022/group-meetings/) should we meet with?

Hadley: suspect it would be useful to drop into every wg to reestablish relationships. Some will have a specific issue they want our time on.

Dan: last time at tpac we did an issue template in our meetings repo where we asked people if they wanted TAG to join a meeting, and got poor response. Better way?

* WoT - Amy ()
* WebApps - Tess ()
* WebAuth - Dan ()
* Payments - Tess ()
* Web Performance - x PING? Tess ()
* WebRTC - Sangwhan ()
* Fed ID - Tess () 
* Privacy CG - Tess ()
* WebAppSec - Dan (Yves)
*  Cognitive and Learning Disabilities Accessibility Task Force including the joint meeting with Accessible Platform Architectures Working Group and Accessibility Guidelines Working Group - Hadley ()
* WebFonts - Tess ()
* PAT CG - Tess (Amy)
* Web ML - Sangwhan (Sangwhan)
* Devices & Sensors - Dan (Sangwhan)
* Immersive Web x WebRTC - Dan, Hadley ()
* Anti-Fraud - Rossen (Rossen)
* Web Editing - Rossen (Rossen, Sangwhan)
* TTML - Hadley ()
* RDF* - Hadley ()
* WebExtensions - Tess (Sangwhan)
* SecondScreen - Sangwhan (Hadley)
* WebView CG - Rossen (Rossen, Sangwhan)
* RDF Can. & Verifiable Credentials - Hadley ()

### Privacy Sandbox debrief

Open Privacy Sandobx issues: https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Provenance%3A+Privacy+Sandbox%22

Dan: we should progress the review of CHIPS. The main question we asked about fenced frames seems to have been answered. About opaque URLs. That answers the question of why anyone would use it.

Hadley: tangent - I searched, and it turns out RFC3986 URI generic syntax deprecates the term opaque URLs but it means a URL that is just alphanumeric and doesn't say anything about the directory hierarchy

Dan: that's a different meaning. 

Tess: opaque origin

Dan: browser knows and can dereference, but the parent page context can't know about it

Rossen: overloading without realising

Sangwhan: didn't realise

Tess: the use in 3986 is archaic. The thing I thought of was the same traditioanl feedback that peter and I have given to every new frame thing which is how does this relate to iframe, and are they speccing in a way that they are abstracting a common model. like fetch, common model for resource loading, and redefined xhr in terms of that same model. It is worrisome that this is now the third or fourth proposal of a new frame thingie and it's not rigorously clear how it's the same and how it's different from iframe becuase they're not defined in terms of a common model.

Dan: has that been left?

Tess: not sure about this time

Dan: Peter left feedback.. [Dominic says in progress](https://github.com/w3ctag/design-reviews/issues/735#issuecomment-1157641639) in WHATWG issue.. 

Tess: cool

Dan: I feel this is one that warrants a positive review, assuming that work is going on.

Tess: do they identify use cases other than personalised advertising?

Sanghwan: no. They wrote in one of the explainers that they have no other use cases for the opaque urls, so probably the same for fenced frames

Tess: so why not call it an ad element?

Peter: +1

Sangwhan: we could ask about other similar things..

Tess: if advertising is the only use case then call it something obvious. If there is another use case the name is probably fine.

Dan: is there something privacy preserving that could be a good use case for opaque urls? If I wanted to send you a url to something ...

Sangwhan: embedding eg. an instagram frame.. 

Amy: social widget type thing

Tess: youtube embed. The whole point is to take content that is available on one of those services and put it on another website, I don't think opaque urls have anything to do with that..

Sangwhan: the fencing might help

Amy: any use cases about sharing don't work because the lookup table is local to your browser

Tess: obvious argument to calling it the ad element, besides the other use case, is that it's going to be really easy for people to write ad blockers

Sangwhan: well the selector is fenced-frame vs ad...

Tess: people are just going to block it anyway. Element name hinges on whether they have other use cases.

Dan: I feel like our engagement is helping somehow.

Sangwhan: Main purpose was to understand what this is all about

Dan: that did help

Amy: It is still clear that they are trying to preserve the status quo around targeted advertising after 3p cookies are gone, but we don't necessarily agree that this is a status quo we want to preserve

Dan: their perspective right now with 3p cookies you can do personalised advertising. If they can come up with ways to enable personalised advertising with additional privacy controls on top of it then that's better for user privacy than what we have now. Their perpsective is that they are leaving the web better than what they found. However, I think that other browsers are already deprecating 3p cookies wouldn't agree with that, as they view the web as better when 3p cookies and an equivalent don't exist.

Peter: is there such a thing as privacy preserving targeted ads even possible? I'm doubtful. I'm not saying it can't be done better, but I don't think it's a goal that is really achieveable.

Sangwhan: worth experimenting

Dan: not just google people working on this in PATCG. Be helpful to have perspective from a publisher point of view, who can talk to us about what they're doing to preserve privacy

Tess: here are their use cases https://github.com/WICG/fenced-frame/blob/master/explainer/modes.md

Amy: SameParty cookie still stuck? Dependency on FPS unresolveable?

**agree to close SameParty cookie unsatisfied**

## Breakout 6b

Present: Dan, Rossen

### [Multi-Screen Window Placement API](https://github.com/w3ctag/design-reviews/issues/602)

Dan: [reviewing response on our concerns](https://github.com/w3ctag/design-reviews/issues/602#issuecomment-1154265904) it seems to address our issues

Rossen: reviewing [Mozilla's standards position](https://github.com/mozilla/standards-positions/issues/542)... The issue with taking over a monitor that users doesn't pay attention to is not as fringe as it's being presented. Often, people use laptops with a large screen monitor (at the office for example) and aren't paying any attention to the main, laptop's screen. 

Rossen: [leaves comment](https://github.com/w3ctag/design-reviews/issues/602#issuecomment-1195596347)


## 09a 

Present: Dan, Amy

### Retro Topics

Part 1 (15:15 - 16:00):

5 min round of topics to discuss. Write topics on white board.

Round of: each person says a thing that **went well** (or is generally positive); 
Round of: each person does one thing that **went badly** (or needs improvement); 
Round of: **additional comments**

[keep comments to 1-2 sentences / ideas to give everyone chance to speak]

Example topics: 

* call schedule - but not trying to set a new schedule today
* how do we work with browsers / other stakeholders / key open source projects?
* logistics of meetings / scribing / minutes / tooling - searchable minutes
* TAG membership / what's missing from TAG skill-set? -> recruitment
* review requests - when/how/response to our feedback
* how we respond to review requests
* non design review work
* 

Part 2 (16:15 - 17:00):

1. Highlight main / top things from part 1
2. Next steps / actions / followup

## 9b

### [review HTML event loop and how things fit into it #489](https://github.com/w3ctag/design-reviews/issues/489)

Rossen & Tess came up with a possible compromise and floated it to the CSS WG in [their issue](https://github.com/w3c/csswg-drafts/issues/5115). Rossen will try to get the WG to take this up next week in New York.


## 10a

Present: Amy, Hadley, Dan

### [Protect vs control](https://github.com/w3ctag/ethical-web-principles/issues/80)

Clarification from mark. Still pondering

### [Is this a mission statement](https://github.com/w3ctag/ethical-web-principles/issues/58)

Overtaken by https://github.com/w3ctag/ethical-web-principles/issues/79

### [Grammatical](https://github.com/w3ctag/ethical-web-principles/issues/75)

Dan: harm to society one needs to be "should", but maybe others we can change. Render web content is overstating.

Amy: and same about environmental sustainability

Dan: but control and power, verify information, and enables freedom of expression, and supports healthy community, we can change those

Hadley: does it change the spec author experience? does it influence your thinking as much as "should"?

Dan: yeah, stronger from perspective of someone wanting to know what they should be doing

Hadley: is there a place for this aspiration list? An end goal that we care about, worded this way. They are all active voice except security and privacy

Dan: we coudl say the web should be secure and private

Hadley: I like that, more concrete

Amy: *redrafts with imperatives for all*. Worried 'shoulds' weaken the 'musts'

Dan: some should stay declarative..

Hadley: shoulds make sense for some that are not very binary/testable things, as opposed to 'verify information' - I can't imagine when that shouldn't be a must. That's harder, more decisive that is testable. Shouldn't be debatable, no exceptions.

Dan: using should and must trigger people in standards.. 

Hadley: not sure how else to write them

Dan: not sure about 'should be privacy-respecting' - weakens 'essential'. Web technologies should be designed with privacy in mind. At the very beginning.

Hadley: 'privacy preserving'?

Amy: stronger than respecting. "The web must be secure and privacy-preserving". "The web must be secure, and preserve peoples' privacy" **will do a PR**

### [Find a voice](https://github.com/w3ctag/ethical-web-principles/issues/79)

Hadley: we want everyone who reads it to be part of the 'us'. 

Dan: Join our movement. Not imposing our views

Hadley: much easier to sideline as someone else's views

Dan: how does that relate to w3c statement. Can we keep manifesto thinking, while also saying this has the stamp of w3c community?

Hadley: I think it fits all the better, coming from everyone, rather than just us. Same problem if we say "w3c community thinks that.." - separates us from whatwg, ietf, rest of the web

Dan: we want w3c to say "we are w3c community and we approve this message"

Amy: can we be clear about who has written and approved it, without being exclusive about who can support it

```
Just talking about this in our f2f with @hadleybeeman and @rhiaro. We think we need to not state it as "this is what we, a small group, think" but more of "join our movement" - more manifesto-ish rather than "this is a consensus view of *this* particular group." We also want the Statement process to make it clear that the doc has W3C community support while also not limiting its applicability to that community. We're trying to think of a way to make it more clear who has written and approved this document while also not limiting its scope.
```

### [Algorithms](https://github.com/w3ctag/ethical-web-principles/issues/42)

Dan: the Web Machine learning ethics document probably covers this.

**agreed to close**

### [Decentralization](https://github.com/w3ctag/ethical-web-principles/issues/54)

```
As part of this, we aim to reduce centralization in web architecture,
minimizing single points of failure and single points of control.
```

Dan: 'decentralization' and 'federation' are both very evocative terms for some people

Amy: thought about removing 'centralization' altogether too, but including it could be useful as it's a key word

Dan: works for me.

Hadley: agree

[PR](https://github.com/w3ctag/ethical-web-principles/pull/87)


## 11b

https://github.com/w3ctag/design-principles/issues/370

Consensus from today's breakout:

- If we were to design `<input>` today, text fields would still be grouped under the same element (`<text>` or `<textfield>` or the like), but radios, checkboxes, color inputs, file inputs would have likely been separate elements.
- `<object>` is a total mess: can cause plugin execution, or subresource loading & rendering, or some other behavior. 
- `<link rel>`: some things should have been grouped together, others should have been separate elements, because some `rel` values cause subresource loads and others don't
- `<button>` is a positive example of overloading where `type` differentiates different purposes, but they are all similar enough and have the same API.
- `<textarea>` possible it *should* have been overloaded together with single line text fields, as some kind of `<text multiline>`. we've seen cases where people have wanted to grow `<textarea>` to have features like `pattern=""`, which suggests it should have been the same element as single-line text input.


Closed https://github.com/w3ctag/design-principles/issues/266

## 12a Discussion of https://github.com/w3c/w3process/pull/611

Do we support this PR or should there be a different approach to appointments?

Tess: in the current system, it's worrisome that the same three people keep getting reappointed. Seems clear that the appointed seats are not being used to balance the needs of the TAG after election results reveal gaps in expertise / background / demographics / etc.

Amy: how about team makes the appointment seeking the opinion of these constituencies? In the draft, it alway sfalls back to team if consensus cannot be reached. This could be simplified by formalising that the team makes the final call, but explicitly taking input from a specific set of constituencies, weighing it, and then making a call based on it.

Rossen: *purpose of appointments* continuance of chairs is a plus... also losing something with continuous reappointment; appointments also help to balance diversity .. in capabilities & background...

Yves: I think it's simpler than the nom com thing... in IETF there are no general elections so it's different than the TAG case... to avoid having the nom com being just another kind of member election... 

Tess: it's good that most of the seats are elected - the appointed seats should be a counter to that. After the election it should be "here are the obvious gaps" - e.g. if there is a gap in accessibility then bring in an accessibility person.

Amy: we also talked about encouraging people to run...

Yves: *suggesting incumbants maybe shouldn't be required to get a nomination in order to stand*

Hadley: one reason for appointments is to be able to appoint people from outside of the membership... so membership doesn't have a monopoly on control over the architecure of the web. So does requiring ... an AC nomination make sense in that context?

Tess: someome who has been appointed [and been there for a term]...  If someone is an employee of a member company then their member company should nominate them.

```
Just discussing this in today's TAG f2f. Even though this proposal has come out of a TAG session originally, we think it can be improved. 

Firstly, yes the TAG agrees that we should be able to pick our own chair(s).

Thinking of the purpose of appointments, they are intended to fill a gap - in expertise, background,  experience, or demographics - that may exist after an election. There is also a value to having continuity - which is arguably what the appointed TAG members have more been used for historically. On the flip side, continuity should be balanced by fresh perspectives as needed. We strongly feel this needs to be preserved.

We think it might be more effective to formalize that it's the Team that appoints the seat but that the Team is charged with reaching out to the W3C community (including the TAG), to come to these decisions on appointments. The Team will have a mandate to seek input from an explicit set of constituencies, and weigh it, in order to make a decision.

This saves the need to convene a large group that potentially changes each year, who then have to spend time meeting and seeking consensus. It also reduces the risk of the nomination process becoming a shadow election, if the nomination committee is composed primarily of member representatives.

Further to this, we should explore the idea that appointed members put themselves forward for election during the election periods that coincide with their appointments expiring.  This will encourage appointed members to go through the same process as elected members on the TAG.

In summary, we think more discussion is needed before we make a process change here. Maybe we can discuss at TPAC and come to a clearer consensus?
```

## 13a - Societal Impacts Questionnaire - https://w3ctag.github.io/societal-impact-questionnaire/

### [Measuring](https://github.com/w3ctag/societal-impact-questionnaire/issues/7)

Amy: I agree with Rick's feedback...

Tess: a worrying thing - I worry about reducing things to quantifiable items. Quantifiably there aren't that many victims of domestic abuse - that doesn't mean that we can ignore victims of domestic abuse.

Amy: also data can be used to make a point, but be from a not-well-designed study.  

Tess: a lot of people use s&p questionnaire as a box-ticking excercise... how can we design this so that people don't engage with it in that way?

Amy: it's more about how we design it - I'd like to see it earlier in the TAG process than TAG review.

Dan: we can only give people every opportunity to engage with these documents. We have to go out an advocate / evangelize these documents as well.

Amy: good feedback from the AC and at the AC panel - ... There is an appetite in the AC.  What I said was "when you're telling employees to make specs you need to allow them time for this"...

Dan: actionable response to Rick?

Amy: I can add text about measuring things, with various caveats about not everything being measurable...

### [Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2)

Amy: this is where I could most use help.

Hadley: for cookies I would go to logging vs. tracking / advertising "this was a good idea, but"

### What's missing?

Hadley: something about financial incentives? Spam is dangerous because of scale and financial incentives

Tess: what behaviour are you incentivizing or disincentivizing by changing the web platform in this way. Eg. - disincentivizing people sharing their opinion if there is a real name policy. 

Hadley: I think they're separate. Talking about something that is now possible and incentivized fully to do with what happens on the web platform, but the financial motivators are outside. We didn't build the infrastructure that makes spam a successful form of advertising. It's separate but parallel

Tess: don't build the new spam thing. If your new thing can be used at very low cost to get low likelihood payout outcomes it's going to be a spam vector. Don't do that.

Dan: we need to be clear in this document that we are targeting people that are building new specs vs people building websites or services. It's meaningless for us to tell people don't build an evil web thing. But it's meaningful for us to tell people who are building the building blocks to do so in a way that doesn't enable these bad behaviours. Feedback should be couched in that way. 

Tess: you can financially disincentivize bad behaviour. You might not be able to prevent it, but you might be able ot make it economoically too expensive to do at scale. Breaking crypto is prohibitaviely expensive so people don't. 

Hadley: and important to remember in that example that what is too expensive now may not be in the future

Amy: or depending on who is doing it

Dan: encryption adds a bar. Can be pierced in a targeted way, but unlikely eg. a govt could unencrypt all https traffic at scale, so it's an effective deterrant

Amy: **raises issue**

## 13c
Present: Yves and Rossen

### [Review request on Render Blocking Status in Resource Timing](https://github.com/w3ctag/design-reviews/issues/753)

## 14a Retro

[ notes kept seperately ]

## Breakout 17a : BF Cache

Present: Sangwhan, Lea, Yves, Dan, Tess, Amy

Guests: Rakina Zata Amni (Google), Fergal Daly (Google), Dominic Denicola (Google)

Sangwhan: how do we make new proposals more BF Cache friendly.

Rakina: *presents slides* BF cache a way for the browser to save documents the user has navigated away from in a frozen state until the user goes back to it - then it gets restored from the BF Cache... then same document reused and restored. Shipped in chrome in 2020. Been in Safari / Firefox since ~2009... Current state: been on the web platform for more than a decade but APIs didn't handle it well.  E.g. if there's an open indexdb transaction what happens?  That's what the chrome team found when we shipped BFCache...  so we blocked some APIs - meaning those pages couldn't used BF cache..  We want to bf cache more pages.  If new API don't support BF Cache it should be like they don't support iframes.  Chrome  BF cache team noticed there were lots of improvements to be made... when we found differences between implementations we filed issues.   Added some stuff to S&P questionnaire and design principles doc...   Some APIs approved by TAG but still unresolved issues for BF Cache support.   So we talked to Sangwhan - sounds like the design review doesn't have a checklist for this...  At this point we still believe TAG design review is the right space to enforce this because it covers the whole web platform rather than just Blink.  TAG the right place to put this... At the point of Intent to Ship in Blink is too late to block shipping..

Tess: we can't block shipping either

Dominic: exposing this to the whole web ecosystem is the stronger point

Tess: seems like the majority of design reviews coming from the blink team... 

Fergal: we tend to do TAG before a blink review - TAG first point of call.

Rakina: mostly talked to sangwhan... still parts of this to make the guides better... more actionable...  other part is : better enforcement from the TAG side...  Part of TAG review checklist...  Security & privacy questionnaire... 

Dan: I note that very often the TAG design principles and the S&P questionnaire etc are .. if somebody doesn't have a good response or has decided to make a different choice, the TAG doesn't block things based on that. We dn't have the power to block things. Also we don't have that kind of authority. Very often stuff comes through TAG review and we leave feedback, and we have to make a judgement call - our feedback hasn't been listened to, is it enough of an issue that we have to issue a 'not satisfied'? Eg. 'with concerns' says we're okay but they haven't listened to something, or 'unsatisfied'. There are things that have shipped that we have marked we are not happy with. But we can't stop things from shipping. Just to be clear. However, if there's something we can do to strengthen the information we give to spec authors about BFCache through the design process to make it clearer we make sure people pay attention to it let's talk about that, that is valuable. In the design review template we provide links to a lot of idfferent documents - DPs, S&P - if this is as much of a high priority maybe we should be including additional information in the template itself about BFCache, becuase it's of particular importance.

Lea: in the DPs we do have something about supporting non-fully active documents, it's not very actionable. If there's a set of things that new APIs could do to not break BFCache.. .Also not breaking other web platform APIs is one of our existing goals anyway. So regardless o fwhere it is coming from we already have a princinple. So obviously new APIs should not break BFCache, obviously we should check for that. This is one thing out of a sea of things we should check for. If API designers had more clear guidence of how to do that, which maybe exists?

Dominic: enforcement - not about enforcement or blocking shipping. As a spec reviewer, on or off the TAG, there are things you read and think 'oh that's wrong'. We've all developed that sense for naming things, and point to DPs. Similarly, it's harder, but we've developed a sense of this part of a spec leaks information across origins, let's take a look. The ask is try and develop that something is wrong sense where you can be like 'they haven't though about how it works when the document is in the background' and point to DPs. Getting it to the level of thos eother things.

Tess: Agree with Dominic. The TAG is mostly elected, at any given time in the TAG's history we have this lumpy set of skills, where we might have some weak areas and some stronger areas. One of the things that our DPs and questionnaire is there for is to help be a smoothing function. If the person doing the review might not be terribly strong in this area, the fact that the S&P questionnaire is prompting the spec authors to think about that, helps us to remember about these things we sholud care about. The other thing - going back to - Fergal said things go to the TAG before they've doen any kind of internal Blink gatekeeper thing. It's worrisome to me that if BFCache mistakes are such a concern, which they should be (this is spot on), there sounds like there should be an internal soundness check before you flood us with design review requests and .. I would ask the same thing of the other browsers, but in terms of workload if you're concerned that things are getting passed to us, try to not send us those things in the first place, try to catch them first.

Fergal: we have our own recommendations internally for people to pay attention to BFCache, but the structure or the way the shipping process in Chrome is set up there is a field in our intent to experiment and prototype to ask whether you've had a TAG review yet. So .. 

Tess: we should be looking for this. But also if you look for it first, the problem wouldn't be at the scale it's currently at

Sangwhan: maybe we want to work with a different audience for this? This session is about BFCache. Blink shipping process issue needs other people.

Tess: Sure.. maybe you folks could back us up when we want this to be improved..

Sangwhan: question whether to have two gates.. will have that discussion later. Too much Blink work coming into TAG is a general problem we here don't have an answer for

Tess: Sure. If we're seeing this is a problem, you're coming to us becuase there's an inconsistent level of reivew of BFCache issues in design reviews, it seems like we can improve things and you can improve things.

Dan: The other thing that comes to mind is do we need to - sometimes when we ask people do you have a S&P considerations section, should we be levelling this up to that level?

Sangwhan: it's in there, DPs and S&P

Dominic: Rakina has some good suggestions on how to make that better. There's a lot of questions that aren't relevant in S&P. Then I get to this one about fully active documents like, 'no'. She has a rephrasing, which is 'tell me how your feature will be have'. I can't just write 'no'. I can write "it will not be usable".

Tess: that's exactly the kind of rewording I'd love for us to do. PLease file specific issues and we'll change the names. Great feedback.

Rakina: and to actually pull out the BFCache guide into some doc, it is quite big. The doc that Dominic wrote about how to write specs .. pull out how to write features affected by BFCache

Sangwhan: a problem is that people know it exists but not that tdesigns can affect it in a negative way. Too much for DPs. The suggestion with Rakina is to split that out into a separate doc like we did with promises. BFCache should be the next case for this. One section with high level checklist about considering non fully active documents. If you're unsure please refer to gigantic document.

Tess: who's gonna write it?

Sangwhan: Rakina volunteered

Tess: fantastic

Dominic: Lea's comment about what is currently there is actionable is helpful. I'd love Lea to review Rakina's document and say if it's actionable enough?

Lea: sure

Dan: I think Sangwhan misunderstood me. Should we encourage people to put in a separate section of their spec for BFCache considerations? Or should we say when you are writing your S&P.. write now we ask for security and privacy considerations sections - should we say there do you have a subsection that is BFCache considerations?

Sangwhan: legitimate proposal. It does require that guideline document to be in place.

Dan: so proposal is to split the BFCache related stuff otu of DPs and put it in a separate document

Lea: with a link

Dan: I'm slightly worried about givign people too many documents. It's already a lot of things.

Sangwhan: it's long already. There's more stuff to be added. Putting it into DPs is going to make DPs more difficult to read. Especially for cases where y

Amy: a short section in design principles and should link to the larger document... 

Tess: enough text to cue whether people think it's relevant to them....  

Amy: and the link in S&P as well will prompt people to know if they are not understanding it should be enough

Sangwhan: might be pushback on spec boilerplate

Dominic: I'd volunteer to preemptively create a BFCache considerations and say how that felt like, and see if it worked or not

Dan: yeah. Would be a good experiment. To see if it makes sense. And sounds like there's cross browser consensus as well.

Sangwhan: retroactively revisting mistakes. STuff that is shipping.

Tess: hard to unship..

Sangwhan: how to make minor changes to existing stuff so BFCache works. There's a lot of things that make BFCache disabled.

Lea: is there a list?

Sangwhan: there's a couldn't bfcache for these reasons list in our review queue

Fergal: two things. The things that Chrome or some browser blocks for, and the things that you must block for. We block on lots of things that are not necessary, we just have to go back and make chrome work properly with this or that. The API is fine but our implementation of it is not. The number of things that ar efundamentally blockers of bfcache that have shipped is kind of low, 5 or 6 things

Rakina: yeah

Dominic: there are some recent ones

Lea: I imagine there must be some recent ones that prompted this meeting?

Fergal: yeah

Rakina: Gamepad was one. We filed an issue in the gamepad repo and I think there was no resolution for that yet. We notcied the api got approved after that. There were also some apis that we managed to talk to the people like webtransport, we discussed with them, but they didn't put it in the spec yet. But they're shipping.

Dan: did you have any discussions with the immersive web folks? Imagine webxr and AR scenarios where there's a lot of realtime interaction would be especially problematic, is that true?

Fergal: I'm not sure how they work. I think we had.. I see webxr on our list of blocked things but I don't think i'ts something fundamental

Domninic: nothing in their spec about fully active. I suspect it's very common - th eobvious behaviour is pretty clear. If the user is in xr and they navigate away you sholud take them out of xr, and i fthey go back probably you shouldn't put them right back into xr. Everyone figured that out but it's not in any spec, would be my guess

Dan: would be something to open up with them. Active work going on.

Fergal: we're tackling these in a priority order based on how often we see them being blocked. We blocked everything then tried to fix the biggest. WebXR I have no idea where it appears on our chart of blocking features, imagine it's low. A bunch of things we haven't studied.

Dan: what's the work plan? The idea is the same folks who worked on the additions to S&P and DPs will work on splitting that stuff out and seeding this new document?

Sangwhan: correct.

Dan: who else should we bring in from the community? Another rep from another engine who is also working on bfcache related stuff?

Tess: good idea. Just have to figure out who knows enoguh about implementation

Dan: that's work for us to do.

Dominic: outdated security and privacy qs being copied around - we had an idea. You could put a date at the top that people have to copy and paste. Refuse to review it if there's no date at the top.

Dan: sounds like an issue we need to look at

Sangwhan: I'll take an action to figure out what to do

Dan: use a form?

Yves: look at what i18n did. Check things and write things and copy it and put it elsewhere

Sangwhan: or another repo with an issue template and have that link back or something.

Dan: create a workflow instead of the way it is currently


