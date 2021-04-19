## TAG Teleconference
##### 12-14 April 2021

---

### Agenda:

#### Special First Party Sets Session Part Deux

Present: Dan, Amy, Tess, Yves, Hadley, Peter (2nd half), Lea, Kaustubha, Brad Lassey, Chris Wilson, Yoav, Chris Harrelson, Alex Russell

Kaustubha: (Presents [slides](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/First-Party%20Sets%20TAG%20Discussion.pdf))

Kaustubha: What we're trying to do is not modify same-origin policy (SOP), not seeking to redefine origin, not redefine hoow existing security features work. Trying to define "party" in third party contexts. Party is not a concept that exists on the web today. The best alternative is registrable domain, whcih as a dependency on the public suffix list, which has its own set of issues. Use cases where that's not enough. Existing security features that rely on SOP are unchanged. New privacy mechanisms may use FPS instead of registrable domains to determine what is first party and what is third party.

Dan: I don't think what you're saying is necessarily that you're not redefining same origin policy.. maybe a matter of semantics. We can get into that later.

Kaustubha: it's not clear how we're not trying to redefine SOP?

Dan: I think we need to go into more discussion on that.

Kaustubha: maybe helpful to think about one specific security feature?

Brad: it is not our goal with this to redefine SOP. If there was any way in whch this did affect same origin policy that would be a bug in what we've tried to propose. It'd be great to identify that so we can resolve that.

Dan: you're saying you don't want to redefine/change same origin policy, but what I'm reading here is for future mechanisms which may have been tied to SOP in the absence of FPS they might be based on FPS as a way to define the security and privacy boundary instead of SOP. That to me is a change to the way we think about SOP.

Brad: I do not think that things that would have been defined by SOP in the future would be affected by FPS at all. But where that decision might come up is things that might be defined by eTLD+1 we might reconsider as would they be better as FPS. There's a spectrum. Things that apply to origins, leave alone. A group of things where the boundary is the eTLD+1, and another set where we might put a line between eTLD+1 and FPS. Where today we have.. the other thing of the entire internet, and saying that should go away and we want to itghten that up. There's something in between eTLD+1 and the entire internet. But all things defined by origin relationships should be completely left alone.

Kaustubha: new privacy mechanisms may use this. We have SameParty Cookies, when when we deprecate third party cookies that blocking which would normally be applied to cookies that are being sent in cross domain contexts would apply across first party set contexts. Other features being specd right now (a bit early to talk about them) in context of new privacy mechanisms. Cookies and storage are being double keyed, so thinking about using FPS as the top level key. Eg. a SaaS provider with chat widgets, that provider would get the same partition across multiple sites that you own. We've had businesses with multiple domains and users expect to see the same session. if they had a chat widget embedded it would get access to the same partition state across those top level domains. If that same chat provider was being used by another company it would get a different copy of the partitioned state. We touched on WebID which is a new federated login mechanisms that we hope would issue directed identifiers on different state. Eg. uber.com and ubereats.com are different domains but the same business. If you used any social logins to sign in you'd get the same account across both, instead of .. a different hashed identifier for a different business. And privacy budget for limiting fingerprinting entropy would be applied accross an entire collection of domains in a FPS. This is a few of the features, what we mean when we say privacy mechanism.

Alex: In all of these cases either it's a new feature, or in browsers that don't already have strict double keying of identity as a way to rationalise what that would mean in a relaxed world, similar to the storage access api at a conceptual level. access to multiple parties to mix state across double keyed buckets. interesting in that what you also see here is that nothing is really trying to say we're going to share session storage or local storage or idb or serviceworker kept state automatically across these contexts without some level of user interaction. Is that a fair way of characterising that?

Brad: one way I'd put it is this is the stuff where the scope is the entire internet and we're reducing that scope to the FPS boundary where an eTLD+1 boundary would have deliterious effects about how users are interacting with these entities

Alex: what in practice would prevent these from being buckets per user rather than more internet sized buckets?

Brad: the original proposal would allow it to be dynamic, where that has led us up to now is to ship a list.. that's more about a mechanism .. something we want to disallow

Alex: is that the public suffix list where the browser is informed about what these are?

Brad: exactly

Tess: one of the things that came up in our feedback was ... do you think this is a relatively complete list? We can't predict the future, and there might be some as yet unimagined mechanism that relies on this, but with your present knowledge is this a comprehensive list of use cases? One of our concerns is the use cases were not clear. The expected scope of how often or how much it would be used in different features was unclear. Hard to evaluate on its own as a mechanism without knowing what all the purposes are.

Brad: This is a reasonably comprehensive list as we understand it now. Hard to predict the future. The other way I'd go about it is these are all things that naturally fall out from the first party sets interaction with same party cookies that allows these sites to communicate. Eg. with the privacy budget that needs to be applied to be across the constellation of sites that need to communicate. With WebID and direct identifiers you're probably going to have account information between ubereats and uber that you want to share, that's why you should have the same login, directed identifier. The keying for double keyed storage, the point of double keying storage is to prvent cross site communications so if it exists already than we can relax that, we saw from microsoft's issue they were interested in the potential performance improvements of relaxing that when it's not providing any meaningful privacy when they can communicate anyway with FPS. 

Chris H: Do any of the specific features listed in this list.. do you think any of them trigger your concern you stated before about same origin policy?

Dan: the webID for directed identities, the use cases you gave about uber and uber eats is slightly concerning to me. uber and ubereats share thes ame branding, its fairly clear to people who are using those services that its the same company. When yout talk about something like instagram, facebook, whatsapp, most people are not aware even though facebook puts wording. People are not aware of that. Do we .. are we building something in that puts the owner of multiple large services at an advantage over the expectations of the end user is what I'm worried about there. I think it does have to do with the expectation of the end user about if I visit instagram.com and I see something and visit whatsapp.com and see something and facebook.com and see something.. those are separate services [from a uer's PoV]. 

Hadley: As we were formulating our response, we, the web community/developers have trained users that they need to log into things differently when they're different origins. We've got this expectation of how everything works in our users and as a result empowered them with laws and policies and UX to help them understand who they're interacting with and what they're doing on a particular site. I'm also concerned that stretching a cookie across multiple sites/origins/domains has the potential to dramatically disadvantage users. 

Brad: on the WebID front this is something we're having the presence of the FPS could allow browsers to be helpful. Using ubereats and instagram as examples .. I land on ubereats.com, I already have an account with uber, as I go through the webID flow the browser can stop at some point and say ubereats is part of uber would you like to use your uber identity or have a different identity? as I log into insagram it can say do you want ot use your fb login or have a separate login? if we didn't have the set on every login we'd have ot say is there another site you think is associated that youw ant to have a shared experience? by having that smaller cluser of sites with the same data controller or ownership we can reduce that set of choicecs that we can present to users. 

Hadley: I'm trying to think this through on the fly... I can appreciate how that flow can work and that makes sense. Are we designing a feature that relies on the developer to build in that flow and that makes it possible for the developer to ignore it and to just crack on with these sites being a part of the same set that the user doesnt' get a choice? Are we designing in such a way that malicious site developers/content owners/whoever could take advantage of users?

Alex: [in chat] WebID UI, e.g., would also be mostly browser-presented; UI can present the relationship from a trusted position

Kaustubha: a key thing is .. can develeopers take advantage? that's where the policy comes in, we are going to talk about governance. there will be policy enforcement that checks that these domains are related. It's up to us to define that policy. THe chrome team has made a proposal but we're inviting the ecosystem to help us, so the policy is one aspect. The other is UX - being able to surface this in the browser UI. Mozilla has this disconnect.me entities list that does the same grouping today. When you have enhanced tracking protection on in firefox they do make exceptiosn for domains in the same entities list, hwich is equivalent to FPS. Edge also ships this. They made the exception and have a third party entitty that manages this. No UI today, the ETP today would provide a report and say these trackers were blocked. Those trackers get omitted if you happen to go to a site that are owned by the same organisaiton. In other browsers because there is no coherant policy or governance model they havent' surfaced that information. With FPS with a common policiy everywhere there's predictability and a governace model behind it. Considering site authors are involved and are giving us that informatin that allows more rigor. Browsers are doing it already but its' adhoc. We're saying lets add more rigour and mroe transparency, and surface this inforamation to the user which is a better solution.

Hadley: makes sense, although If eel like disconnect.me is a hack on the status quo. I'm not sure what we want to enshrine into web standards. Also concern our job on the standards side as opposed to part of the job on the user agent side, tend not to specify anything that is UI specific. I'm trying to focus on the part of the discussion that essentially doesn't rely on specifying UI in the user agent. But it sounds like more of what I'm thinking about is going to come out i nthe governance part.

Alex: we're trying to strike anything privacy/security sensitive not to specify specific UI, but give users more confidennce than in the content of the page. This presents an opportunity for the browser to present those relationships. in the webid context with two parties the browser can present those origins in the regular origin centered way from UI that is trusted by the user rather than relying on thes ites, who we don't have much faith in their ability to tell us who they are. We have the aiblity to reprsent that and createa bility for the uers to understand who those parties are, to the extent they understand origins.

Tess: meta point - wer'e over half way and a big part of the TAG's concern is around governance. Want to make sure we look at that. In response to Alex - I think you made an argument about getting meaningful user consent requires UI that a user can understand. one of the advantages of .. the PSL (Public Suffix List) has many disadvantages, but one advantage is people understand domain names, sites, the average web user doesnt understand an origin. In the storage access api if you say do you want facebook.com to get access to data on instagram.com.. people understand what facebook and instagram are. introducing a new mechanism requires some kidn of label? Some metadata.. a first party set that is facebook/instagram/whatsapp/others there's a column in that database entry that is "human readable name of this FPS". Who is providing that? i assume that isn't going to be like the ?? text stuff? PSL does match up with meaningful user consent pretty decently.

Alex: to the extent you ahve two parties as with webid you'll be able to present that choice. See other people who can participate in that conversation UI.. which will come down to browsers having ood UI, we're not specifying that here but making it possible to help which comes to governance.

Brad: Chrome is not planning on shipping request storage access api, we dont' think that's a question we can meaningfully ask users. I don't think that's really an alternative.

Kaustubha: We've talked to a bunch of developers and people on the github repo with use cases. There's app domains.. applications are complex deployed over multiple domains, they often embed each other. microsoft, lucid software.. users interacta cross and expect thes ame session. Branded domains like amazon, audible. Country specific domains. Interesting use case with gov.co.uk on the PLS because they love the security properties.. if we compelled them to take thesmelves off the PLS it would be a security question. Agencies with subdomains get treated as different registered domains. That's consent management, with third party cookie blocking you're forcing our users to give consent each time in different government agencies, adds a lot of friction to their sites.
.. Service domain like github, utilities.. CDNS
.. sandbox domains where sites have chosen to separate user uploaded content for security reasons. Smaller sites like codepen, they have a cdpn.io which has developer uploaded content, and codepen with login cookies. Broad spectrum of use cases.
.. this problem has existed for quite a long tim eon the web. Not radically new, a lot of prior art. DNT with same party property. IETF DBOUND uses DNS as a mechanism to query boundaries. Firefox entities list, same purpose. John Wilander from Safari proposed Affiliated domains in 2017.
.. [quotes from safari devs in support].. some issues in PrivacyCG under discussion, we're seeking feedback.

Tess: a quick aside - the Chrome featuresets page says signals from safari are positive and I think that's inaccurate. What you're seeing here is we think the problem should be solved, but our on the record statement from Maciej is "I don't think we'd implement the proposal in its current state", interpreting that as positive is incorrect.

Kaustubha: supportive of incubation
.. Edge has also exprssed support
.. Governance.. hoping for more ecosystem input. Generally we are very interested in developing a common poliy. At the time we wrote the explainer we left a lot of flexibility because we were talking to safari at the time,t hey had the static entities list that they liked. If firefox likes the entities list perhaps they can continue to use it, but for the prupose of site developers they can assume.. chrome might have its own list, firefox might have its own, but they're getting the same sort of behaviour. Since then we've been in the privacycg and browsers have said they prefer a common policy. They don't want to see different lists across different browsers. That's the ideal end state for chrome as well, interested in developing a standard policy and verified by an independant entity. We're interested inw orking with the ecosystem. Issues on github about that. the DNT spec cals out what party means - common data controlle ris the terminology they use. Not sure if that's right. That's the key thing that we've also saidc ommonly owned and operated, we'd have to consult with policy experts. This might be a fraught example, we do have the webPKI baseline requirements that offer precedence for a common set of rules between browsers. Special certs.. have an organisation field. Verifying domains are owned by that org. There are issues today with webPKI, want to offer that as precedence, it has been done on the web today.
... It's kind of early, we're trying to define what this is, we're figuring out from the ecosystem.

Dan: sounsd like we're talking about governance of an allowlist that would be based on some policy and that policy needs to map to some of those use cases. however you mentioned common data controller. that's exacty the problematic use case that I tried to reference in one of my previous comments about amazon.com and amazon.co.uk are the same org but from a data policy perspective they're subject to different data controllers, if one of the goals is that governance tries to demtermine what are thes ame organisations so we can make sure FPS members are all in thes ame org we need to be really clear about what is an organisation? that is a different definition depending on which way you slice the problem. That is another thing that's causing me concern.

Hadley: if we get into legal orgs, amazon.co.uk and amazon.de are different companies. Then we're splitting hairs about which belongs to whom and the countries themselves have a tax interest in having them be different companies.. gets messy

Tess: and plenty of use cases for nonlegal groupings as well. Direct action efforts where poeople dont' have 5013c status, but it is the same org informally.. it's hard to ground this in the legal notion of organisation, but also cases where you wouldn't want to do that. Seems really hard.

hadley: another area would be interesting to explore is whether countries that have a very strong role in their economy could argue that every company in that country is part of the same group. Which could put us in a situation where this had a bunch of unexpected knock on effects.

Alex: interesting question about where governance might happen. At the end of the day browsers ship what they ship. Browers should do the right thing by users.. certificate governance works today, everyone involved considers it to be painful but it has done a good job of ensuring that users are safe. who would be the entity that that responsibility that is delegated to? If these lists are transmitted out of band... an earlier proposal gave the browser agency over how these things are recognised. Is there technical feedback about mechanism to prefer, better than live or browser provided that can be joined up? And how might that governance quesiton be answered?

Hadley: depends on the use cases

Alex: is that per feature then? Eg. shared origin cookies or webID maybe those would be different governance questions?

Hadley: my intuition had been more in thinking specifically about cookies.. very difficult conversation to ahve in the abstract.

Dan: differs dependingon what the use case i. Thinking about what this could be put to.. if you have a sandbox domain where w'ere talking about different domains that the user really doesn't see but its convenient to be able to host things in these different domains, that's one thing. Then you're talking the common eTLD thing is different.. country specific then we're back to the question of in what sense the same organisation? BBC is a really good example. I know from talking to people that they view bbc worldwide as a completely different organisation from BBC UK. From a regulatory perspective they have to be different. When I was working in UK gov there was a strong value placed on not sharing data between eg. the immigration authority and the ministry of justice. Somebody's immigratin status should not be by law pertinent to whether or not they pay a parking ticket. In some cases even in the common eTLD case it may be by design that its not a good idea to share data. The question becomes what are we trying to accomplish through this governance, and that is still not clear to me.

Hadley: GDPR and the data protection act that says those departments are not allowed to share data exxcept for explicit laws for specific use caes

Dan: while they might complain users have to click the cookie warning each time, from a regulatory perspective it might be that they need to each time.

Brad: one key point Dan and Hadley have made is that this is a great argument for making sure thes ecompanies/entities can have control of how these relationships are expressed, as opposed to today's third party cookie world (interent) and entities.json with no policy and one or two engineers who stick domains on a list as they think they should be, not how the companies think they should be related or legal entities want to be related. FPS is trying to help the situation that you both described.

Hadley: does muddy the waters for users if we're trying to help them understand that amazon.com and amazon.co.uk are thes ame but bbc.co.uk and bbc.com are not. 

Kaustubha: because site develoeprs have the agency to define what their first party set looks like if bbc.com and bbc.co.uk were required to not share that data or be treated as separate sets that would be up to them. Companies are still required to conform to whatever laws of the region they operate within. As opposed to something like the entities list with obvious mistakes today. 

Dan: would that mean that the primary reason for having governance is to stop bad actors from abusing this capability?

Kaustubha: exactly

Chris H: the legal and regulatory examples raised are great examples of how we shouldn't be designing features as a mechanism for enforcing these legal constraints. It's a different thing. To the extent that site is subject to gdpr or have a different company for tax reasons they are expected for mechanisms outside of the scope of standards to conform to those things. If bbc.co.uk and bbc.com need to be separate need to be separate they should just be separate. I don't think it has direct bearing on this proposal. What you said is the main thing we should focus on with governance which is avoiding situations where users may be harmed or abused.

Dan: that's a really good thing to focus on. The questison had to do with the feedback so far.. a lot of discussion bout how do we determine whether or not a FPS are part of the same organisation which leads to the question what is an organisation... but if we're focussing the governacne around combatting abuse or using FPS in an unintended way then I think it totally changes the discussion about governance. i'd love to understand more about that.

Chris H: I guess I meant potential for user harm or doing things that the user didn't think was reasonable. I'm sure we can come up wtih scenarios where there are sites trying to phish you or be evil. Cases like instagram.com vs facebook.com is one that's hard because it has to do with .. the're not really the same but they're the same company and maybe the user knows and some would want things to be shared and other users might not. That one is a grey area. Other cases with large conglomerates that happen to own a bunch of random companies. Probably we agree their companies shouldn't be in the same set because it doesn't make sense at all.

Yoav: user confusion where amazon.com and amazon.co.uk are different organisations and bbc.com and bbc.co.uk are not.. the other way around.. the current situation today with the entities.json does bring to that if we were to make a different obscure decisiosn on those two fronts that would lead to confusion, but giving FPS give the browser a UI opportunity here to express that to the user and to tell them that these two sites are related where these two sites are not. That could potentially require some education but FPS gives us an education opportunity here. 

Hadley: Given .. as somebody who helped to define GDPR, I think that our role as the TAG and what I presume is your role as Chrome engineers, is not to necessarily respond to international regulation but to inform it, or to make the world work and then regulation responds. In Creating GPDR we didn't sit down and say how do we want the world to work based on what tech could be uilt. We looked at current risks, and looked at current context, and responded. The regulatory examples I brought up in this context not as regulations constrains us but it constrains the organisations we're takling about which can affect the use cases. Sepearate to that I had a quick look at DBOUND fro IETF and see they didn't produce any docs and thw orkign group has conclued. Would be useful to know what happened with that and what we can learn.

Kaustubha: i can share a link, they produced rdbd

Dan: Positive discussion.. maybe we can continue in the issue for further deliberation? I think it would be useful to see some elaboration in the proposal about.. tighten up use cases and specifically say what you're not trying to do. Understanding not how the governance would work but what the governance is for would be very useful because then we understand what wer'e talking about here. The point about mitigating against misuse by bad actors or using it for something unintended, that would be .. the rqeuirements of governance vs the mechanisms of governance. If it's been documented I haven't seen it yet. Could be part of the explainer.

Brad: next steps - defintiely interested in updating the explainer to clarify points especially around same origin policy. The concerns raised about SOP we don't want to be a concern with FPS. Someone we can work with to run edits by and make sure they're clarifying this in the way you're looking for so we can resolve the issues? 

Dan: I'm happy to be a point of contact for that. Maybe we can figure out a more transparent way to do it as well. 

Brad: we'll work on edits and run them by you to make sure they're addressing the concerns y'all have.

#### Breakout A (Europe / US) - [2021-04-12](https://www.timeanddate.com/worldclock/converter.html?iso=20210412T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
* [HTML: Guidance about 
-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
* [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris
* [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - @LeaVerou, @kenchris
* [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @hadleybeeman
* [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286) - @LeaVerou, @kenchris
* [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299)
* [New principle: APIs should allow introspection](https://github.com/w3ctag/design-principles/issues/300)

#### Breakout B (US / APAC) - [2021-04-13](https://www.timeanddate.com/worldclock/converter.html?iso=20210413T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Added some text for "Attributes vs Methods"](https://github.com/w3ctag/design-principles/pull/262) - @cynthia
* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [[Meta] HTML Design Principles section](https://github.com/w3ctag/design-principles/issues/269) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
* [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou
* [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
* [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281) - @hober, @LeaVerou
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [High Level vs Low Level](https://github.com/w3ctag/design-principles/pull/291/files)


#### Breakout C (APAC / Europe) - [2021-04-13](https://www.timeanddate.com/worldclock/converter.html?iso=20210413T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282) - @torgo, @rhiaro, @hadleybeeman
* Detectability of AF - Sangwhan

#### Plenary Session - [2021-04-14](https://www.timeanddate.com/worldclock/converter.html?iso=20210414T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Tess, Peter, Dan, Yves, Amy, Ken

Regrets:

##### [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris

Lea: there's a TAG document on creating components - some of these apply to HTML in general... I was wondering if we could fold some of these in...  Pointed out in the issue some of this.  Some specific to web components some specific HTML design advice.

Tess: there's an ongoing effort to move the rest of the HTML design principles into this doc - most of those are very general. 

Lea: unrelated - a lot of the issues are related to that.

Ken: Should they be duplicated?

Lea: I don't think duplication is good.

Tess: in CSS working group as in here we don't have to wait for an official resolution. 

Peter: true.

Peter: looking back at web platform component document - it's still draft.  If we've been socializing it then it makes sense but if we haven't published 

Dan: when we were writing this we thought they were not appropriate for design principles because they were about using html rather than writing new html features.

Tess: same issues apply to component design to feature design in some ways... they maybe should be reformulated as opposed to using the web components APIs.  We're telling people how to do a good web component. A lot of similarity to how to make good new Web features.

Hadley: would same audience come to both docs?

Tess: it needs to be - the bits that apply to html - bring those over ...

Lea: web components guideline should link to the design principles.

Peter: So I think it makes sense to not gut this document.

Tess: we need a heading.

Ken: I can do it.

Dan: rewrite certain parts of web components to make the appropriate to include in design principles, and include bidirectional links

Lea: maybe not bi-directional?

Peter: whatever makes sense in the case.

##### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon

Lea: there are certain patterns in HTML - should we formalize?  Sangwhan said it could be expanded... 

[bump to breakout B or C?]

##### [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris

Lea: about keeping IDL and HTML attributes the same when they are the same thing... When they are not in sync it confuses authors to no end.  In more recent elements this is avoided but there's no prnciple about it.

Tess: have you asked Anne or Domenic? Should it be enshrined?

Lea: will ping them explicitly.

Peter: I remember we talked about this years ago - there may be examples where an attribute sets initial state - doesn't reflect live state - don't have any good examples.

Lea: `input value` is an example...

Peter: not sure if it's a feature or a bug.

Lea: having seen how confusing this is for authors I'm pretty convinced it's a bug.

Peter: don't disagree - but how much of the web would it break if we changed?

Lea: I don't think we can change it for existing form elements - just for future ones.

Dan: I'm sympathetic to voicing the developer pain. We should listen if things are especially confusing we should mitigate

Peter: even if there is some reason to not always do it, maybe the principle should be : *keep them in sync unless there is a really good reason not to.*

##### [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - @LeaVerou, @kenchris

Lea: Basically the web platform is a mess when it comes to naming events - some patterns have emerged. Maybe we should have some guidance so it's less of a mess when new events are added. I've recorded some patterns I've noticed.  

Peter: I recently went through something similar to this - ordering words ... mousemove vs movemouse. Might make sense to have all mouse events start with *mouse*.  Not sure if that's something we want generalized. I agree it's a mess and we should have recommendations. Sometimes it's a matter of style or choice.

Dan: design an api for community of practice of domain, or to fit together with Web

Lea: Fits with next issue - which consistency is important? 

Tess: all things being equal the web should be consistent with itself - but sometimes specific domains mean it's important to be consistent in with that domain.  I don't think you can write a hard and fast rule.

Lea: everything has exceptions but the prevailing rule is not apparent. 

Tess: I don't think it can rigid. It can say "we try to keep the web names consistent within itself..."

Peter: sometimes the inconsistency is on purpose sometimes by accident. we should avoid the accidents.

... past tense vs present tense - all new events should be present tense but if you're adding a new event to a set of 12 that are the other way then you should add it in the other way for consistency.  I agree we should have some principles here.  When there's a common name across a set of events the common name should probably be first.

Peter: someone want to take a stab at a straw man proposal here?

Tess: I can give it a try.

##### [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @hadleybeeman

Lea: this is - when features are designed there's no obvious way to consistency - with the web platform or with the concept that the API's about... or sometimes there is tension between API ergonomics and consistently. Should you try to design something more usable?  The improvement should be significant.

Dan: this came up in web neural networks api. Sangwhan was suggesting current proposals was mapping on android api as opposed to being something that web developers would expect. We should have language here. I can start something if people are happy...

Tess: 👍 

Ken: happy.

Lea: happy.

Dan: [assigned to write something]

##### [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286) - @LeaVerou, @kenchris

Lea: api ergonomics vs precedent ... there are a lot of ... in the developer community it's seen as - should these functions return something or void ...

Tess: i have an opinion - the promise that we return from `.play` - play was a void function - we had the ability to return a value if there was something to return - but if we had a return value specified we wouldn't have had that flexibility. All things being equal I'd prefer to keep degrees of freedom. I think the web platform will exist longer than any particular library.  So I think our design for the API surface should not track current trends or fads - we can be more conservative. 

Ken: some of this is done in JavaScript itself - like if you have an object and you modify it - in that case it makes sense to get that object back.  This is not a broad thing... It's mostly for collections and small objects you want to modify.

Peter: similar. I've seen consistently in both directions.  In Objective C you never returned void.  We don't have that precedent here.  We'd have to have a really good reason as it'd be a fundamental shift. 

Ken: we'd have to go and look through those cases... 

Peter: is there something we can extract ... 

Yves: elements vs attributes ... difficult to define a general principle in this case.  support tess : forbidding the use of void would be bad because it would resrict the future overload of void.

Tess: unless you can concretely identify a return value - then don't return something. Better to lock it down at first and then expand. 

Lea: I wonder if "start with small and expand later" could be a design principle.

Tess: see also "baby steps".

Peter: I agree we should.

Tess: [takes actions]

##### [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299)

Lea: made an edit it should be "common things should be easy."

Tess: I think this is a general software engineering principle - and can find citations - happy to do this one.

Dan: can I suggest we include a few examples from web platform. Could be misinterpreted.

Tess: doesn't mean every idea no matter how simple should be easy....

##### [New principle: APIs should allow introspection](https://github.com/w3ctag/design-principles/issues/300)

Lea: this about exposing certain data structures so authors can build - e.g. a long default config that wasn't exposed ...  lot of offenders here.  intl object in JS for example - authors need to define their own data structures... All the color libraries have huge data structure of existing colors which they could get from the browser... 

Yves: WebIDL is allowing introspection and we found it's not properly implemented - difficult to rely on that.  2-3 years ago most of the webIDL automatic tests were failing. Introspection was not working - nor able to detect from JS.

Lea: I think there are APIs that are doing it right but can't think of them.

Peter: we should define how the introspection is exposed.

Tess: fingerprinting concerns... some examples - e.g. i18n data - could be used for fingerprinting... tz info might expose information that wasn't otherwise availabile. In some cases it might be best to not provide this data.

Peter: another way to mitigate that is to define a standard set for the web platform.

Tess: e.g. rgb.txt - single set of colors the web supports.  You wouldn't want to say that about TZs though because they are political categories... 

Peter: we don't have to bake them into the browser ... but use a canonical source. 

Tess: odds are exposing ICU version isn't so bad from a fingerprinting perspective ... there is some text in the Mozilla standards positions repo on this.

Dan: more thorny

Tess: just more nuanced.

Peter: web should be fully introspectible. 

Ken: we should make it clear that this is about the API being introspectable. 

Tess: in some cases we recommend a picker style API - cause the browser to ask you - there are examples where the API is intentionally not fully introspectible 

Ken: we should make it clear it's an API thing....

### Breakout B

Present: Peter, Lea, Sangwhan

Regrets:

##### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon

Lea: Your comment, not sure what you are intending, can you clarify?

Sangwhan: If we define URL like input into objects in the web, I figured it should probably not be limited to objects that have a DOM binding - there are objects that do not necessarily have a DOM representation that juggle URL-likes - e.g. WebRTC

Lea: Can you open a new ticket?

Sangwhan: Sure

Lea: So we have src and href which are common patterns, and one-offs like video poster etc that are not necessarily antipatterns. And then there are things like object data, applet code that feel like antipatterns. Then there is form action, which is an outlier - should that be href or src if we designed it now?

Peter: When object data and applet was made there were no patterns to work with so that's probably why we ended up with the antipattern

Sangwhan: Not so sure if form should be src at least, src implies load semantics

Peter: If we had the URL object back then we probably would have used that


##### [Added some text for "Attributes vs Methods"](https://github.com/w3ctag/design-principles/pull/262) - @cynthia

(Long discussion which I forgot to minute)

Peter: We should distinct between a conceptual getter and a getSomething() getter.

##### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou

##### [[Meta] HTML Design Principles section](https://github.com/w3ctag/design-principles/issues/269) - @LeaVerou

##### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

##### [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou

##### [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou

##### [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281) - @hober, @LeaVerou

##### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

##### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

##### [High Level vs Low Level](https://github.com/w3ctag/design-principles/pull/291/files)

### Breakout C

Present: Ken, Amy, Dan, Yves, Sangwhan, Hadley

Regrets: 


##### Translations of Web App Manifest

Ken: translations to the web app manifest - so a separate file that would override some of the fields... In the Twitter.com Manifest it would go to the local language one... the problem is keeping all of those up to date.  So [I suggested reporting API](https://github.com/w3c/manifest/issues/676#issuecomment-818488036) ... it be a use of the reporting API... Feedback was that this was just for CSP violations but I think it's for wider use cases... I think people should start adopting reporting API more - get feedback when things break.

Dan: sounds like something we should weigh in on if there's a question about what the reporting api is for and the scope - do we need a dispute resolution issue here?

Ken: it does say it's generic if you read the spec. I think it's useful for other things than violations. Maybe we have other use cases.

Dan: isn't it already internationalised? why do you need a separate manifest?

Ken: long dispute... doesn't really support languages.. JSON doesn't have this ability.. don't want to add languages inside and grow these huge files. Separate manifests from the server. 

Dan: you would request webapp manifest and server sees your language accept in the request..

Ken: yeah but doesn't scale. Can add lang to link and media, but pushback.. same thing with dark mode, should be in the manifest. Keeping manifests in sync if ou're not generating them is a pain. Danish manifest for google is 2 years old, but US is always up to date... the solution aaron(?) had is substitute certain fields, mitigates some issues with it being a different experience in a different language. Maybe translate icons. Issue that you have a manifest that links to translation maniffest and how are these getting tested? I know how developers are... you check your own language and english and maybe others aren't tested. Very easy to break JSON. Developer doesn't get notified and don't know it's broken for weeks or people know where to report it. My experience with translation tells me this is just going to happen.

Dan: plenary?

Ken: reporting api shouldn't be that difficult.. this file failed. Similar for storage.

Dan: sounds like the dispute resolution template was designed for this kind of thing



##### [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282) - @torgo, @rhiaro, @hadleybeeman

Amy: I made [a PR](https://github.com/w3ctag/design-principles/pull/295)!

Dan: use reference instead of direct link to ewp in abstract

Dan: left a review comment - other than the [[reference]] we are good to go - let's review and merge at plenary.

Rathole: weigh in on [capitalisation of web platform](https://github.com/w3ctag/design-principles/issues/294) ... this is a thing.

Dan: [left a comment](https://github.com/w3ctag/design-principles/issues/294#issuecomment-818548017)

##### [Detectability of AT](https://github.com/w3ctag/design-principles/issues/293) - Sangwhan

Sangwhan: brought to my attention - [issue in ARIA](https://github.com/w3c/aria/issues/1371) - we have a blrub in the design principles about not making AT detectable. Currently there are numerous ways to detect AT. It's unclear from the [design principles](https://w3ctag.github.io/design-principles/#do-not-expose-use-of-assistive-tech) whether we are suggesting they should go in and fix everything. Not clear whether possible. From a user activity PoV it's easy to detect AT. Should we make it clear that this is only for new technology and if unavoidable?  Thoughts?

Dan: that sounds reasonable to me.

Yves: I wonder how it relates to the introspection issue we discussed yesterday. Detectability can be done through introspection as well. 

Sangwhan: a lot of things on the page are changed by enabling AT... things differ.. I don't think it's 100% perventable. 

Dan: be good to get Alice's input if she's been involved

Sangwhan: Alice split the problem in two - one is not preventable: if certain things change in user behaviour you can be pretty certain a person is using AT. The other kind is APIs that only show up if you're using AT. What she thinks is that our principle is about the latter. But since there's already stuff that allows web pages to detect use of AT with the former mechanism, does it make sense to enforce 2? We're not exposing extra entropy here. Exposing specifics about the underlying AT would be very bad. 

Dan: when we determine something related to accessibility we bring people from that community in. Do that for this issue?

Sangwhan: wendy said PING is interested as well

Hadley: sounds helpful

Sangwhan: Alice's intent was that APIs should not explicitly allow detection. But since it's already detectable is there a point in enforcing it?

Hadley: is this similar to the more broad fingerprinting? Yes it's possible but we still remind everyone to think through the implicaitons and minimise fingerprinting surface

Sangwhan: the fingerprinting surface is this person uses AT and what kind of screenreader possibly. 

Dan: issue is current wording is strong. If we weaken the wording or give an out then does it make sense to have the thing in here at all? Because if somebody designs a new API and explicitly don't allow for introspection of AT but it can still be easily detected what are we really asking them to do? I don't know. We should have a discussion with PING and people in accessibility community.

Hadley: makes sense. Wonder whether moving away from a hard and fast principle to a nuanced questionnaire exploration of the possibilities might be more useful.

Sangwhan: Alice and I have a draft checklist for a11y which we were hoping to bring in as part of the process for TAG reviews. We hadn't managed to release it because its sensitive. It's for content not for specs. 

Dan: what Alice said in the issue response is consistent with the text in design principles. Maybe this is a smaller wording issue like adding a phrase .. nothing in this document says go back and redesign the web where it doesn't match this ideal, it's already about for new technologies.

Sangwhan: I can add specifics on what kind of cases we're expecting it to be covered by

Dan: having the wording about safe to visit a webpage and justification about exposing sensitive information is important because people might not be thinking about that when they're designing an API. That's part of the whole point, to get people thinking about not just the people they know and the conditions they are familiar with.

Sangwhan: should still look at meta issue of de-facto detectability. Third thing is should we have an accessibility review questionnaire in our process. Will contact Wendy about arranging a meeting.

https://www.w3.org/WAI/test-evaluate/preliminary/

http://w3c.github.io/apa/fast/checklist.html

### Plenary Session

Present: Ken, Dan, Peter, Tess, Amy, Sangwhan, Lea, Yves

Regrets: Hadley

#### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon

#### Breakout A Rollup

Tess: Design principles issues ... we assigned them to write PRs... merging some of the guidelines for components into the design principles doc.  Some of the advice is applicable to adding elements to HTML... We can port some over.  Attributes in HTML that contain URLs.  HTML & IDL attributes out of sync.  Lea took an action to summarise the discussion - that has sparked a good discussion on the topic.  Guidance for naming events - and self-consistency vs consistency with prior art (a domain).

Peter: On the IDL attributes - a lot of web component frameworks have an option to do this which you can opt in or out... 

Tess: "foo attributes reflects the attribute of the same name..."

Peter: we should be consistent... 

Tess: Then: what to do with functions that return `void`.  We decided that's an important degree of freedom. General software eng principle: simple things should be easy; complex things should be possible.  We finished with question of - APIs should allow introspection.

#### Breakout B Rollup

Lea: URL-containing attributes - Sangwhan started a new issue related; we had consensus about the bulk of the issue - but something to the plenary.  Long discussion on attributes vs methods.  We also resolved we should have a HTML design principles section in the design principles.

#### Breakout C Rollup

Ken: translation in webapp manifests... from a manifest you link to other translated manifest files.  Fear is very few developers will test all languages.  So I suggested using reporting API.  Marcos disagreed.  Brought this up for discussion.  Link to ethical web principles.  Also capitalization of "web plartform." 

Amy: there is a PR on the design principles we can merge. [PR](https://github.com/w3ctag/design-principles/pull/295#pullrequestreview-635753823)

Sangwhan: **squashed and merged**.

Sangwhan: Detectability of AT.  We have a principle that AT should not be detected. Current state is that it is detectible.  I took an action to imporove the text...  Meta arch issue is - what should we do about the detectiblity right now?  we had no conclusion.  I left a comment for Wendy to follow up on. Hopefully we can have a 3-way call between accessibility folks PING and us.

Tess: In some cases - the detectiblity is a quality of implementation issue. E.g. voiceover clicks the exact center of the button. Solution is to fuzz... for some features.

Sangwhan: for some things.

Tess: it might be that for some for compat reasons we can't get everything.

Tess: this gives people reviewing specs a leg to stand on.

Sangwhan: that approach was brought up in the original ARIA issue... other cases - ARIA hidden - which is a blatent hint. 

#### On Reporting API (ref the Manifest file translations issue)

Ken: issue of whether this is an appropriate use for the reporting API... 

Dan: what do the people who reported the API say?

Ken: generic reporting framework ... variious platform features can use ... 

Peter: don't see why it couldn't be used for reporting manifest installation failures.  Could argue about which endpoint it goes to...  Seems reasonable.

Dan: we could open a TAG issue - like a dispute resolution issue. 

Ken: storage pressure event seems to have created their own thing https://github.com/jarryd999/Storage-Pressure-Event 

Dan: do we need a new design principle?

Ken: currently reporting API used for .. things such as CSP violations; deprecated feature usage...

Peter: i'm not sure that storage pressure makes sense to go back to the server. The reporting API is about reporting things you can't detect easily.

Sangwwhan: i think it's application-level failures... 

Peter: agreement that it makes sense for Manifest errors - storage is more of a pressure event. 

Sangwhan: or it could be that the user declines....

Sangwhan: reporting API not very widely implemented... Believe Chrome is only one that supports whole thing.  so might not be good for a principle yet.

#### URL-containing attributes

Lea: issue 278.. we're not sure about : (A) shold attribute be called href (B) regarding things like ping attribute in A - are there emerging patterns there?

Yves: Form action ... the fact that it's not a get or a head - unsafe - makes it different by default. 

Tess: in a form where the submission is a get it may ... but most forms are post.

Lea: So what can we distill?

Tess: Not sure there's much to distill... form is the declarative mechanism for doing Http requests that aren't get.

Lea: it's appropriate to standards groups designing new web standards --

Yves: might be more important for people designing web components 

Lea: applies to every naming principle.

Yves: we can keep in design principles. 

Lea: one additional issue - there should be a subset of the design principles for web content authors - and generate the subset. Some of these things are not relevant to web authors but a lot of them are.

Peter: agree that makes sense.  we could have bikeshed generate it for us automatically .

Lea: my opinion: any principles that apply to designing web technologies should be in the design principles doc.  We can't predict what may or may not come up again in the future in design reviews

Tess: the design principles doc is something distilled from what we observe over time - it's not comprehensive. I think it's a mistake to include things that haven't come up.   We should wait for the situation to occur.

Sangwhan: I agree. Also it reduces the burden on the people refering to the design principles.

Dan: I agree with having a profile of the document that is relevant to web developers. It should be relevant to web devs as well even if its to help understand guiding princples of web platform design. Sympathetic to what Tess was saying, it should be based on lived experiences of web and spec developers and the TAG, that will help to ground it in reality.

Lea: agree, makes sense. But web developers will not come to us for review, these are things devs get wrong in the wild, not sure if standards groups get them wrong as well. Value in recording patterns somewhere, right now they're not.

Sangwhan: some of the stuff has been recorded in our backlog - if I see the same pattern twice I'll open an issue on it. For example 234, 238... (in design principles repo). Those were spun out of reviews where we didn't have a principle to cover it.  Keeping track of repeating patterns. 

Lea: if we write principles that are obvious to but haven't come up yet - could help the people ahead of us.

Sangwhan: there are things we should have put in that we missed...

Lea: we should prioritise ones that came up in design reviews.  

[we create labels]

Peter: anything else on URL-containing attributes ?

Lea: for HTML it's harder to wait for design reviews to bring up new principles.

Tess: might be a good thing.

Peter: if there are patterns not written down it's worth documenting, but not trying to predict too much

Lea: there are already features that violate principles

Tess: web platform is really big.. not sure it's a good use of time to go into weird bits to try to extract principles that may or may not be relevant in the future.. primarily about our own limited time and energy. If you want to write PRs about this then go ahead. Document is more relevant when we focus on things we learn from the design review process.

Peter: agree with both. Documenting existing architecture isn't outside of our scope, but isn't necessarily priority one.

Lea: agree on prioritisation. Hard to send PRs when not sure of group consensus. I have energy to work on them but I don't know group consensus.. don't want to do work then discover the group doesn't agree.

Tess: typically file an issue, then try to fix it with a PR.. not a prerequisite to have agreement of the group to do either. Group decides whether to merge. Understand your caution.. PRs get revised repeatedly before merging because of feedback. Here it's a do-ocracy.. if you think it's worth doing do it. PR text can be most convincing. Highly recommend writing PRs when you have time and energy, don't need TAG consensus.

Lea: difference between agreeing work should be done and assigning the work.. just going off and writing PR for something we never discussed has higher odds of never getting merged. 

Tess: in practice I don't see much of a difference in this group with these documents. In general I see your point. 

Dan: it depends..

Tess: I wrote a PR to add a better readme to ethical web principles.. we didn't talk about it beforehand, I happened to look at the repo and see it should have more

Peter: don't be discouraged about writing a speculative PR. Fair to write something and try to build consensus around it. Or to raise the idea. If you have bigger scope issues and you don't want to spend effort on PRs, write an issue to spark discussion. Or write a handwavey PR and we can discuss see about fleshing it out. Use your judgement about how much effort to spend. There's no order of how things have to be done. Even unmerged PRs leave something for the future.

##### Issue Triage
