# W3C TAG face-to-face in Reykjavík
## Day 2

Present: Hadley Beeman, Sangwhan Moon, Lukasz Olejnik, Tess O'Connor, Alice Boxhall, David Baron, Dan Appelquist, Kenneth Christiansen, Yves Lafon, Peter Linss (remote, start of am only)

Scribe: Kenneth (first half), Hadley (second half)

### Day 1 retrospective

Alice: do we want to discuss whether we want to continue doing 1 to 1 breakouts between face to faces.

Tess: Would reduce the complexity of scheduling our meetings

Dan: Feels like additional tooling can help

Yves: Does it have to be 1 to 1, or can we have more people attend

Tess: I believe 1 to 1 is very effective, we can do special one-off

David: One thought about extending this to non F2F'es, makes it easier to bring in people more often. Q? do we want to do that?

Hadley: We should encourage them to create great explainers ... 

Alice: We need to write notes and make sure that goes into the explainers etc. Hopefully not necessary.

Dan: What is clear is that a lot of people here had a lot of good to give during meetings but not a lot of time out of bands. Worrying about friction and a lots of time spend on organizing

SW: When I did this with Travis is was not a lot of overhead

Dan/Yves: We still need regular calls.

Dan: We could be biweekly calls and use every second call for 1:1s.

Alice: Still bad for the meeting times

Dan: We can do it based on time zones

Alice: We are supposed to do work outside of our meetings, so we can start scheduling that.

Tess: So every week we have our regular call, plus one 1:1 (three different time zones)

Lukasz: Do we still need the regular call?

Group: Yes, to coordinate and stay as one group

David: So we always work with the same people?

Dan: Having it at the same time every week makes a lot of sense

David: You can still cycle. For each person there should be two OK times. It is a bit complicated, but I think it can be done

Tess: Will you take the action and do that?

David: yes

SW: How do we set topics

Dan: On ad hoc basic... we could discuss at main call or just work on design issues etc.


###	Andrew Betts joining us to talk Feature Policy

Andrew joins from Tokyo.

Dan: Hallo from Iceland - lets discuss feature policy evolution

https://github.com/w3ctag/design-reviews/issues/341

Where does thsi stand from your point of view

Andrew: The points that I raised last time are still relevant. Client Hints and feature policy is great, but doesn't tell much about hte intent until you look at each policy.

Never slow mode...

Since I raised the issue, there has been a suggestion from Anne, that we split feature policy into 3 standards.

Basically there are those that are designed to sandbox document, sandbox 3rd party iframe, permission delegation (like geolocation, camera)

I would suggest taking a look at issues as https://github.com/w3c/webappsec-feature-policy/issues/282

https://github.com/w3c/webappsec-feature-policy/issues/296

There is no discussion yet about what these spec would be called or whether they would integrate and cooperate

Seems to make sense as they work differently

Dan: Where do you think, if you were trying to allocate TAG time, what should we focus on

Andrew: This latest development is good for TAG to have an opinion on - what do you want to make sure is delivered. As it is embedding dev experience into the platform, it is good to check, for instance the default size of images is 300px, where does that come from? Should these best practices be embedded into the platform?

Allows the devs to police 3rd parties/app providers - which might preventing sites going to https etc

Dan: SW and David are on this issue, what are your thoughts

SW: Need to organize my thoughts

Andrew: Good for devs to get their heads around - but naming is really bizarre - really - like allow-slow: none... doesn't make any sense

Naming is hard!

Dan: Has your feedback been well received...

Andrew: It relates to moving to 3 new standards - what do we do with what has been shipped so far - I am not seeing a consistent naming scheme

SW: Not a lot of adoption now, we can deprecate and fix it

David: We have an issue about related features like sandbox-allow and a few other things - worth thinking about that too

Need a doc to say, where do put each policy and how to name it - someone should do that

Andrew: I believe naming is important and people need more guidance

SW: I think that Anne's proposal makes sense - should we continue having this in WebAppSec? it is mostly not security

David: Makes sense there as it is related to keep close to CSP

Andrew: It is moving away from CSP like with parameterized features

In term of syntax will very unlikely remain consistent with CSP

[further discussions on where it belongs]

Andrew I want to be able to lock down a feature for 3rd parties and not just current doc

Alice: Have you talked to Ian...

Andrew: Yes, we have had video calls

Alice: I have had comments from him that stood out

Andrew for example Alex's never slow mode, turns of a lot of behaviors so maybe the UA can enable it for a slow site - not just the developer in control

Dan: Should we organize a special call for this?

Alice: Good idea, I have people from SF who wants to join

Dan: I find this important - naming matters - we should pay attention this is web arch

Dan: Alice cna you schedule

Alice: Yes

David: People here are interested due to permissions mostly

Andrew: To police your own team and 3rd parties - feature policy is cheaper than code reviews

The problem is massive - like FedEx tracks your behavior not just your package

SW: Important to police, as 3rd parties might get updated and become "evil"

Dan: AMP

Andrew: Best that I stay silent :) Might be possible to allow sites in AMP carousel if applying a set of feature policies


###	Mike West Dials in for multiple security-related issuess: [198](https://github.com/w3ctag/design-reviews/issues/198), [297](https://github.com/w3ctag/design-reviews/issues/297), [342](https://github.com/w3ctag/design-reviews/issues/342), [373](https://github.com/w3ctag/design-reviews/issues/373), [339](https://github.com/w3ctag/design-reviews/issues/339)

Hi Mike,

Dan: Just coming off break - already talked to Andrew Betts about feature policies... we have a bunch of features lined up

Dan: we have 198, 297, 342, 373, 339 lines up for you

Which one of these do you need our feedback on?

Mike: First party sets and same site=lax flows into that. Other I also want feedback on, but can be later

Dan: we start with first party sets + =lax - David you are assigned to that - speak up

David: I dont have a whole lot to say - I am curious about what feedback we should provide

Mike: See a few boundaries that we are about to create, like the origin boundary and more recently we are creating the notion of a site that fits with a cookie boundary. Like we drive site-isolation around that, but based on the origin, but your site. Site issomething in between my stuff and the internet

There is a third, that doesnt exist in dev facing way, but user facing ways, first party interaction. There is also the notion of an entity that are generally user facing and not dev facing like password management - this notion is a bit broader

Frist party sets tries to clarify this notion to avoid us building up proprietary lists of what we consider entities.

Browsers do weird things with such lists today, like amazon.com... aws.com etc...

We want to standardize this and do less weird

It is bad that every browser have different behavior, like which sites to share password completion with etc.

Also affects cookies from 1st party vs 3rd parties (Tess: storage in general)

It's difficult for us ot impose control without brekaing use cases we care about like single sign on

We want to tread different related domains as first parties

Tess: Do you want Safari to treat google.com and doubleclick.net as the same for  ITP

Mike: Yes

Hadley, makes me nervous

Mike, this brings to be same-site: lax

[Mike introducing same-site]

Mike: Cookies should be same-site: lax by default and devs should explicitly opt into cokies for cross site contexts, and those need https

Implications of that is that any cookies that needs to be accessible in cross tie contexts needs to declare it self as same-site: none.

I would love to allow YouTube to deliver cookies to google.com

Hadley: Are you trying to break same origin model because google owns multiple domains

Mike: No, check last part of document

Mike: If A embeds B, it can not access its data, but if B embeds B or A and B declare themselves as the same context, they can access the same data.

Hadley: asks for clarification

Mike: if youtube.com frames accounts.google.com then that frame should have access to its storage (scoped at accounts.google.com).  

David: so in the past that would have been the normal behaviour - but in some case there are things doing 3rd party blocking (or partisioning) that would make that not work - because it's 3rd party.

Mike: we can be more aggresive with how we deal with 3rd party content if we can can allow entities to declare themselves across domains.

Tess: if doubleclick.net and google.com are in a 1st party set together and a tracking blocking mechanism flags doubleclick.net as a tracker then you are saying that it should also block things from google com.

Mike: if the heuristics a UA has built identify a site as tracking users then...


Tracking blocking…

Mike: doubleclick.net is included on many many pages to which it is a 3rd party – e.g. cnn.com. Cnn.com including a doubleclick.net frame is exactly the case that many browsers want to attack – they want to make that embedding different. That would not be impacted. What would be impacted would be is youtube and doubleclick…

Hadley: you’re asking sites to create sites they are associated with and trying to make that scale across the web in a less proprietary way., what is to stop cnn from claiming doubleclick is a first party set. 

Mike: A registerable domain can me one and only one first party set. So only one publisher.

Hadley: how does that work?

Mike: the json file has a list of origins.. each of those origins has to make the same set of declarations… consistency in the set that’s created. A asserts that it’s in a set with b c and d. How do we guarantee a registerable domain only shows up in 1? rules in the browser. 

David: 

Tess: you were saying if doubleclick and google are in same first party set then there is a concenr about embedding doubleckicj on google.com and seeting the right data.. domains in a first party set should be treated the same for anythign where it’s a first party / third party distinction. What about google analytics. It’s in the same first party set as doubleclick so it’s a tracker and therefore gets blocked? 

Mike: google analytics sets cookies scoped to the first party.

Tess: how is it’s unaffected?

Mike: y’all would treat google analytics as a prevelant origin.. .g.a. would set a cookie on cnn.com.

Tess: the script would have to execute. But if we classify doubleckick as a tracker then it wouldn’t execute.  Doesn’t this feature encourage that?

Mike: how?

Tess: if we classify doubleckick and g.a. as same first party set then we block script execution from g.a.

Mike: allows things to load and then blocks…  if we want to start to block third party resources ...

Lukasz: in 1st party sets, let’s imagine a situation site.com and it’s in a 1st party set with evil.com. Let’s say evil.com is independently in a 1st party set with example.org.

Kenneth/Tess: cannot happen.

Lukasz: Ok.  Any abuses for identifier.

Tess: if all domains in the 1st party set have to have the domain listed and you have apopular ad service that can impose technical constraints then it can publish a list to clients to require clients be in the same 1st party set. An ad provider would have access to the.

Mike: on making things less secure by binding origins together in a way that doesn’t currently happen: my hope is that this woun’t happen. Proposal for additional same site attribute values which would scope cookie delivery based on the 1st party set as opposed to the site. When looking at the default value for the cookie, Chrome sets it to lax by default. Other option is none. No middle ground. The request between youtube and google (eg) would be allowed by the cookie delivery scope even though they are not same saite. Cookies could declare themselves to be first party lax or first party strict. Could take different actions against cookies that declare themselves to be different in scope. From a security perspective this gives developers options they don’t have to day and most would choose not-same-site. In the long term this would b ebetter for security and specifically aginst cross-site-forgery attacks.

David: the idea is that right now the default is same-site none. We migrate to where default is same-site lax, or same site-firs party lax.

Hadley: multiple local storage happening… now many block 3rd party tracking… now we are making exceptions for 3rd some 3rd parties… how to explain to users?

Mike: explain in terms of entity. People understand that entities exist. 

Dan: I don’t think this 

Hadley: people wouldn’t expect data to flow together…

Lukasz: is there a max size?

Mike: the document suggest something like 30.

Tess: is 30 big enough for the amaazon case?

Mike: some cases can be dealt with for having a carve out for the same registerable domain name but different top level domains – e.g. google.com, google.is, could be grouped together.

Lukasz: 2 large sites – 2 large user bases – and some data saved locally.. now another company acquitres another site. You could…

Dan: regulatory issues with sharing information between domains.

David: we can separate the idea of first party sets from each things that uses 1st party sets. Should there be a 1st party sets mechanism at all – then should we swhich all these things to use 1st party sets instead of what they use today. Mechanisms we have control over. E.g. Cookies, Ad blocking,

Tess: Storage partitioning.

David: Each of those things is a separate discussion.  In some sense we should mostly try to distinguish between these discussions – but “should 1st party sets exist at all” is dependent on whether some of those things are a good thing to do.

Kenneth: share service workers?

David: a lot of the things he’s talking about changing to use this mechanism are not things that use origin but things that use various hacks.

Mike: Correct.


### Breakouts

###	Signed Exchanges

special guest: Jeffrey Yasskin

[Design questions for Signed Exchanges #354](https://github.com/w3ctag/design-reviews/issues/354)

[Subresource prefetching+loading via Signed HTTP Exchange #352](https://github.com/w3ctag/design-reviews/issues/352)

dbaron introduces the issues.

dan: let's leave portals for now. 

... What's the status?

Jeffrey: we have shipped a version of this in chrome and google search is using it, to let the whole end-to-end system try it out. There are open questions on the details, and also IETF workshop ([Escape Workshop](https://www.iab.org/activities/workshops/escape-workshop/)) talking to publishers on whether we should do it at all. This issue was ... 

...A couple things you might want to look at. One idea: to prevent distriutors from helping to track users by customising the thing they ship for another origin. Maybe we should fetch the signed exchange without credentials. a new attribute on fetch. 

hadley: timbl would be happy with that. He's been asking for it for years.

jeffrey: do other people have concerns? 

hadley: yes, which is why it's been a discussion for years.

jeffrey: where should I look?

dbaron: issue 76.

yves: whatwg issue: https://github.com/whatwg/fetch/issues/517

jeffrey: I'll read that over and think about it.

...Next question: there is a possibility of checking with the original origin that the content is still up to date. The origin content culd do that on its own, or browsers could to it by default. If by default, it comprormises an anti-surveillance property. 

yves: what is the proposal? that you alwasya check fur an up to date version? or is it a propery of the package... "fetch if stale"?

Jeffrey: publishers can already write js to do this. opt in. Quesiton is: should we do this by default? we could have an opt out bit, so publishers could say they want a stonger anti-surveilance property?

yves: the security aspect is checking that the signature is still relevant, mroe than that the content is.  but fo rme, what's key is to be able to work offline as much as possible. so I'd prefer an opt-in.

jeffrey: there are several points. I'd lean to where if the liveness check fails, you can sitll use the content.

yves: yes, but there is till a delay. bad for the user experience.

hober: it's not a striaghtforward tradeoff. liveness can be used to detect personalisation of content. de-personalisation is a privacy benefit. 

david: the right thing to do might be different across different use cases for packaging. 

jeffrey: stick an enum in the package itself, saying how to revalidate it?

david: hadn't been thinking that. but the way packages are used might be different. there might be almost PDF replacements, where you want to see what's in that archive thing even if it's not up to date. in that case, the user would be aware of the package. Rather than the up to date content.

...in other cases, like syndication... there is less user presentation of the fact that there is a package underneath. so user expectation is dfferent

torgo: IETF workshop (ESCAPE)... Hadley and I were just discussing this. What is the multi-implementer commitment on this work?

jeffrey: right now, only chrome is commited. firefox is worried about the effect on the power dynamics across the web. they are also worried about the benefits, especially the signing parts, that they aren't enough to pay for the risks. 

hober: if unsigned bundled exchanges are less contentious and have broader support, why not move forward with those first?

jeffrey: we're doing both. it's quite possible that bundles will get standardised first.

...I understand that apple are worried about the tracking possibilites and the security risks

hober: I think we're broadly sympathetic to mozilla's concerns as well.

torgo: It seems reasonable to me, what Mozilla have written.

Hadley: +1

torgo: it gives the party hosting the signed exchange a lot of leverage over the party that the signed exchange is coming from. 

jeffrey: the power dynamics are something we are trying to work out. we'll get more details at the escape workshop.

torgo: that's in July, in Virginia.  so your perspective is that this will be discused then?  My thought was that this workshop was going to be more about AMP

jeffrey: regardless, I will try to write up people's worries on the effect on power dynamics. there seem to be 2 axes: ranking power and distribution power.

hadley: ranking power?

jeffrey: at google or facebook, when they order/rank content for you.... packaging has very little effect on that. 

...It does have an effect on distributions; CDNs could take you offtheir platform if you do certain bad things. It will reduce that power. and allow people to distribute around CDNs, which has come up in some discussions with people who work for CDNs.

...Mozilla are writing up their concerns on the power dynamics. I will be listening. 

dan: would it be useful for TAG to weigh in? say, through a position paper presented at this workshop?

...we were asked to co-chair and co-sponsor this workshop. there wasn't sufficient interest in the TAG to do that. It has become an issue that this is being built to allow big publishers and big aggregators and big advertisers to make money. but it is also being build to help marginalised groups evade censorship, or keep the web distributed. 

Yves: there are other user cases, like archival packaging, offline distribution in areas with low or no connectivity. it would be useful to have them in the scope for this discussion.

we recently have ISOBMFF transferring web content in MP4s... they might have an interest in this.

Jeffrey: this is in the goals. we don't have concrete users for it yet. The question of long-term signatures makes security people worried. 

hadley: that's particularly challenging b3ecause many of those users don't have the resources to spend a lot of time with you

hober: have you talked to Gogole books?

jeffrey: we should. WE've also talked to the web publishing WG. I think ebooks will be signed by the publisher, but not be able to execute as the publisher's origin.

sangwhan: do ebooks need an origin?

hober: they'd like one

yves: if you want powerful features in the book, you need an origin.

dan: We wanted the Web publications group to be represented in this too. Doesn't seem to be in scope. 

hober: there seem to be lots of constituencies not talking to each other

dan: I'm concerned about that workshop. The diversity of opinion and representation at the workshop

...Judging by this, I don't think our topics will be covered. 

...Jeffrey, do you see your proposals on credentials ... or is there something in the idea that could mitigate against these power dynamic issues?  I also read in the Mozilla paper that they thought it let info be shared with the relaying party in clear text. What's going on to address that?

Jeffrey: One way the design tries to prevent centralisation is by not allowing publishers to create an allow list of distributors. that wasn't there in response to feedback; it's justs been there and we've defendeedd it. otherwise, the worries have not been concrete enough to mitigate against.

...the question of sharing text in the clear... there have been previous attempt to do blind caches. Martin Thomson was involved. the cache couldn't see what was in it, but end users could decrypt it.  If you want to cache somehting, the same user has to be useable for multipel users, or you're just proxying it.

...If thats' the case, a cache could pretend to be a user and just decrypt it.  

...but it's a small use case. so we've been focusing on public content, where you don't care who sees it. there is a privacy risk... the only where you learn that distributor/signed_exchange holds publisher/book is by following a link to the distributor. whoever writes the a=href already knows that you clicked on it. if the person who wrote the link and the distriutor then the distributor already knows. if they are different companies than the person who writes the link has to be aware of the property. 

...That analysis is in the ietf signed exchange draft, but it's not having the impact it should. 

hadley: threat model?  what are you worried about here?

jeffrey: the distributor learning what url's people are visiting. not giving them exztra info they didn't have before.

dan: what about the content, signed and appears to hte user of the web as publisher-origin... requests special permissions, access to location, camera, etc. In that case, is the distributor also privy to that info?

jeffrey: No. ONce the contenti s loaded, it's as if a redicrect to the publisher, in the publisher's origin.

dan: okay. Becasue I think that was one of the original worries in our AMP finding. which is addressed in this particular technology. 

hadley: you are still spoofing...

jeffrey: wouldn't call it spoofing because the publisher actually did sign the content.

Yves: more a delegation of distibution...

hadley: for the purposes of question, you are spoofing the origin of the publisher - are there other messy origin things happening - 

jeffrey: one question on our issue on reporting. So should we report that a distributor...  ? and what properties should it have. Martin T wasn't sure you'd have an answer to. What we can or should reveal about hte publisher to the distributor. 

...No other issues are coming to mind. 

yves: on the first question, about the personalised content? I can't see why it wouldn't b posible to sign personalised content. it should be distirbuted... the same way as you have cache control private and cache control public... in that case, the server when it's signing might have something similar to allow or not distribution of that package.  for example, if you want to view something offline, you could use your own personal package.

jeffrey: the server should not sign cache contro private data. we dont' ahve a requirement that cache control public appear in headers; but we could. You could use an unsigned bundle... the chrome emerging markets are building that. they are currently writing mHTML. 

yves: Okay. Still working with powerful features?

jeffrey: it would not be running as that origin. 

sangwhan: yeah

jeffrey: the browser would need to be confidnt that you had saved that data and trusted it completely, in a way that if you got it to someone else, that person would not trust it. I'm not sure how to do that.

sangwhan: seems like unsigned is useful for our other use cases. maybe not books

yves: yeah, it will want origin checking

jeffrey: when you load an unsigned bundle from a file, maybe it's a secure context? possibility. it would be good to be able to grant some of the persmissions to somethign running in a bundle, so you can see where it is. Risk: an attacker can send you a file and not be sure what it is.  attackers have abused this before

sangwhan: is code signing an alternative?

jeffrey: we've been usingin origin certs because they're easy to get and the restrictions matc hteh pwers we want signed exchanges to have. the overall mechanism doens't change who is signing the cert. if it's more trusted, maybe we could trust it longer or do different things

sangwhan: that might make people happy

torgo: we're running out of time. hope we've been helpful. anything else?

jeffrey: subresource prefetching... See the explainer (issue 352). original problem: we don't have bundles implemented yet; we want a distributer to be able to send you a signed exchange of ta top level html file. it may have an image, or a style sheet, or other subresources. you need those before it'll render correctly. so those should come from publisher to avoid centralisation, so we need a way to tell the brower, "you can get those subresources from over here"

hober: isn't the obvious solution "wait for bundled exchanges?". at that point, will this go away?

jeffrey: this has 2 bnefits over bundles. Once you bundle things, client has to download the whole thing. in this system, you tel the browser to pre-fetch this, but if it ihas itin cache, it doesn't need to.

...also if a CDN is serving an unsigned html file with a cross-origin subresrource served by a CDN, the other origin could sign that, and the CDN could say "ive got a copy of that, you don't have to make a new connection"

...there is a significant privacy risk. it allows any server to ask whether any other url is cached. however, as browsers move to multi-keyed caches, the domain of that question gets smaller and becomes something our threat model is assuming the top level domain can find anyway. so it's fine. 

dan: you mentioned security and privacy issues. we're asking people to fill in the questionnaire... don't see it in your request. it helps us to be more timely with responses and we're trying. 

...what i'm hearing is that this is a request for early feedback on an idea. 

...we'd like explainers not in a google doc please, but in the relevant repo. So we can track changes, issues etc.

Hadley: in trying to optimise our time, we are seeing that a lot of our feedback when we're working with one implementor is stuff that would come out in working with others. so we'd encourage you to do that as much as possible.

dan: and please highlight the user benefit, or user need. 

jeffrey: it's in the explainers doc, I see. I'll do that.

... though I don't see a request to put it in github

dan and alice: we have an issue on that. thanks for calling it out!













