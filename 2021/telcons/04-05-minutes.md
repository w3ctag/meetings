## TAG Teleconference
##### 5-7 April 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-04-05](https://www.timeanddate.com/worldclock/converter.html?iso=20210405T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
  * agree the feecback we want to give, pick times for a special breakout
* [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris
* [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
* [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299)
* [New principle: APIs should allow introspection](https://github.com/w3ctag/design-principles/issues/300)
* [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286) - @LeaVerou, @kenchris
* [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @hadleybeeman
* [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - @LeaVerou, @kenchris
* [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon

#### Breakout B (US / APAC) - [2021-04-06](https://www.timeanddate.com/worldclock/converter.html?iso=20210406T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [High Level vs Low Level](https://github.com/w3ctag/design-principles/pull/291/files)
* [Added some text for "Attributes vs Methods"](https://github.com/w3ctag/design-principles/pull/262) - @cynthia
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou
* [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281) - @hober, @LeaVerou
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [[Meta] HTML Design Principles section](https://github.com/w3ctag/design-principles/issues/269) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

#### Breakout C (APAC / Europe) - [2021-04-06](https://www.timeanddate.com/worldclock/converter.html?iso=20210406T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282) - @torgo, @rhiaro, @hadleybeeman
* Detectability of AF - Sangwhan

#### Plenary Session - [2021-04-07](https://www.timeanddate.com/worldclock/converter.html?iso=20210407T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage


**NB: We largely focused on *first party sets* this week to the exclusion of this agenda.**

------

### Breakout A (Europe / US) - [2021-04-05](https://www.timeanddate.com/worldclock/converter.html?iso=20210405T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Peter, Amy, Dan, Tess, Lea, Rossen

Regrets: Ken

##### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
  * agree the feecback we want to give, pick times for a special breakout
  
Tess: if we tightened up same origin policy somehow.. if we slowly changed the default for cookies to be same origin only slowly over time we might not object to that architecturally, maybe for compatibility, but not philosophically. Making same origin policy more consistent and faithfully applied. That this is loosening it is the concern. Good to word it as change is scary to an important piece.

Dan: FPS expands the scope of origin. Maybe better to rephrase to be more dispassionate.

Tess: you could use loosen instead of expand, weakening instead of attack. Be more specific when talking about being cautious about change, about weakening the policy. Example - if someone were trying to fix holes in the same origin policy that exist now like same origin cookies, our concern with that kind of change would not be philosophical it would be pragmatic. That would be strengthening the same origin policy. Not that all change is concerning. 

Amy: I can't find actual concrete use cases for why they want sites to be able to declare sets

Tess: some browers have hard coded lists for tying domains together, for authentication and autofill stuff. 

Tess: crawling all of the .well-known to build a comprehensive set might be challening....

Tess: inject js needs to be softened.. there are user centered features that rely on browsers doing script injection, eg. reader modes. can be at the users behest, that isn't invasive.

Dan: makes things more complicated for web devs. We have a principle about not having too many manifest type things.

Tess: we're correct in saying hold off on building stuff on a rickety foundation... but if we say there's not evidence for the additional complexity..

Dan: we also need to talk about scope for us to be comfortable with this architectural change

Tess: be specific, make a list of use cases. We can say "in its current form".

Tess: we don't know what all the problems are, we don't know what they're trying to solve. To the extent we've identified concrete use cases we believe they can be addressed in other ways. We need them to show their work.

Tess: is there something we can cite about not building new things on top of new things. Add on top of stable things. Incremental things. I'll look around.

Dan: it needs to be implemented by multiple browsers to be viable.

### Breakout B (US / APAC) - [2021-04-06](https://www.timeanddate.com/worldclock/converter.html?iso=20210406T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Rossen, Peter, Lea, Sangwhan, 

Regrets:

[More First Pary Sets feedback work.]

### Breakout C (APAC / Europe) - [2021-04-06](https://www.timeanddate.com/worldclock/converter.html?iso=20210406T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Ken, Dan, Amy, Yves, Sangwhan

Regrets:

##### First party sets again

Dan: Call for consensus at plenary on feedback doc

[NB: consensus was recorded on the TAG's slack channel]

##### [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282) - @torgo, @rhiaro, @hadleybeeman

##### Detectability of AF - Sangwhan

### Plenary Session - [2021-04-07](https://www.timeanddate.com/worldclock/converter.html?iso=20210407T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Hadley, Kenneth, Peter, Dan, Amy, Rossen, Tess, Yves

Regrets: 

##### First Party Sets Feedback Final Edit

Working on [feedback doc](https://github.com/w3ctag/design-reviews/blob/main/reviews/first_party_sets_feedback.md) on First Party Sets.

[Discussion on the layering paragraph...  How can we indicate we don't want to see stuff built on 1st party sets until it's more stable and also still encourage layering?]

Dan: Looking at [pr 291](https://github.com/w3ctag/design-principles/pull/291)

Amy: kind of related but doesn't make the exact point we want to make.

Dan: Ok final version is [here](https://github.com/w3ctag/design-reviews/blob/main/reviews/first_party_sets_feedback.md). I will send to requestor, I will link to the issue. We will discuss with them on Thursday.

[Recording consensus.] - multiple thumbs up.

##### Breakout Rollup

##### Issue Triage

### Special Session for First Party Sets - [2021-04-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210408T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Tess, Peter, Amy, Sangwhan, Rossen, Yves, Hadley, Chris Wilson, Chris Harrelson, Kaustubha Govind, brad, Jade Kessler

(Everyone doing self-introductions)

Dan: the TAG, as part of a new... 2013 TAG.. Alex Russell was involved in that, as a TAG member, helped us put in place what we now have as the spec review process, design review process, emphasise the idea that the TAG can be helpful during the design process. We encourage anybody who is writing new specs, new technologies for the web to participate in the TAG review process. All managed through github. Different issues depending on what you want to do. The other thing the TAG does is write documents like findings, a document that addresses one particular issue that the TAG has an opinion on, e.g. Securing the Web from 2015. We have lots in the pipeline. Also things like security and privacy self check document which was contributed to the TAG by Mike West and has since been iterated on and continues to be iterated on and is something that we ask spec developers to read before they request a review or during the design review process, it's supposed to prompt discussion and thinking about privacy and security issues. We have our design principles document which is referenced a number of times in the review response that I circulated. That as well is intended to be a living document that accumulates material, design guidelines for APIs and new web tech. Over time as we participate in the design review process we continually add new items to our design principles and that steers our overall direction and is something that we encourage .. has brought in some of the original HTML design principles stuff such as the priority of constituencies which is work that Tess was involved in. That leads us to where we are with the .. normally when we are asked for a review the process is that aa lot of the activity goes on in our issue or is activity that happens in somebody elses issue or issue list and is normally resolved through discussion in the issue and we close our issue and say we're done and move on. In that process we're working through a lot of different things up and down the stack in different parts of the web platform. Everything from devices and sesnsors to new CSS to HTTP sometimes stuff outside w3c in terms of ECMAScript features such as those from TC39, protocol level stuff, definitely involved in WHATWG. I should mention that we a couple of years ago we wrote some ethical principles which are also referenced. The idea behind that is to give the design principles more ethical footing. That's been very well received within the W3C community. We're not just developing technology, collectively, we're here developing technology platform that's meant to serve .. for the benefit of society. The web has an ethical design at its root. That thinking tends to permeate our design princples and also the work we do on design reviews. We're constantly referring back to that and it gives us direction in the work we're doing. Wanted to make surep eople are aware of that.

... That brings us to the review document. With First Party Sets originally we received the review request in 2019. We had initial feedback, something along the lines of it looks like there are issues people ahve raised .. you might take a look at the review request and say it's been sitting there since 2019.. we did respond and at the time saw it as more of an experimental idea, raised some issues, closed our issue, and then we received another review request for Same Party Cookies, and noticed that it referenced FPS. So that prompted us to re-open FPS because part of our review feedback on Same Party Cookies was that we didn't know that FPS was stable enough to start building stuff on top of. That is why we included the last paragraph of our review feedback.

... I've been sitting in on PrivacyCG calls. This document is in formed by some of that experience s well. It's a consensus document, it's gone through multiple review rounds this week with the TAG. The three major points at the top can be seen as the core of the feedback. The concern we have about the same origin policy and therefore the security model of the web. The scope issue which we would like to see.. more well defined scope. And governance issues, especially around the lists, blocklists/allowlists, and UA Policy. Some of the other concerns that are underneath that are stll important, but more things that buttress the previous issues. The one other thing that .. we talk about redefining third party cookies and that's where we mention the privacy sandbox initiative. If we're changing.. our perception is that this changes the definition of what it means to be a third or first party cookie so in that context we have ot be really careful because people already know what it means to be a third party cookie so we have to be careful with changing that. if we are talking about limiting third party cookie access we have to not change the definition of third party cookie.

... The web user agents thing is talking about priority of constituencies, that it should be safe to visit a page, this security guarantee is underpinned by the web security model. We talk about permission and consent, and adding to complexity of the web. The question is are we adding a lot of work for web developers here when it comes to adding a new configuration layer and is that justified? So our .. One of the things we'd like to hear .. we'd like to hear your feedback and one of the things we're hoping to prompt is how much could you imagine reframing the proposal in a way that does not have the issues that we've raised, especially around same origin policy and is that possible? Is that something we could come up with an action plan between us that would help move things in that direction? 

Brad: we designed FPS with a layered approach which is generally a useful paradigm. FPS itself maybe doesn't make a ton of sense to talk about in isolation but the first thing built on it is same party cookies. It has other applicaitons but the right thing to talk about is how it applies to cookies and therefore same party cookies. Off the bat it does not change the same origin policy or affect origins at all, that's the intent. We've seen with most major browsers that have intervened against third party cookies have had to have some solution for multi domain sites. i spent 10 years at Mozilla when we introduced enhanced trakcing proteciton we had to have entities.json to make that work, that's been in gecko for nine years. Same party cookies in today's world along with FPS is purely restrictive. It's saying that cookies marked same party are vailable in a similar sense as third party cookies within the set but not outside of the set. It's purely a restriction on today's world. Moving forward or looking forward to when we remove the ability to have generalised third party cookies the idea is that within a set same party cookies would be treated similar to how third party cookies are today within a set.

Tess: when you say that the status quo today, it is a restriction today, it might be true for chrome but not for other browsers which already prevent third party cookies. It's a loosening in other browsers.

Brad: equivalent in firefox and edge which use entities.json

krgovind: Tess made a good point about other browsers restricting. One key thing, as reading the feedback, there's a lot of context and layers to the problem that we may not have called out in the explainer. We're focussing on the technical mechanism. We want to add some background... differences with the way chrome and privacy sandbox is trying to solve vs how mozilla and safari have done it. Mozilla default tracking eTP mode today is a blocklist of trackers. They only drop third party cookies on requests to those trackers. And they have an allowlist that applies to those trackers which own other domains that are first party to them. So let's not drop third party cookies as long as the requests are happening within the conext of the entity sets. Safari today has heuristics in a lot of cases, blocklists every time there's a new version of safari, and always a disclaimer saying this might change, only temporary. Different browsers, there's a problem with the use of heuristics and allowlists, there's a problem today yet everyone is trying to solve it a different way. With Chrome we are going to when we turn off third party cookies, no heuristics or blocklists, everyone is getting it turned off, but we recognise there are multi domain sites, it's the nature of the web today, we need a way for the domains to say they are a collection and for sites' functionality to keep working we need our own cookies avialable in that context.

... Also a lot of prior art in this area. It's existed as a problem for a while. I responded in the review with a short response. for instance back to prior art, the DNT spec in w3c tries to define this notion of party. In the .well-known file there is a property called sameparty which is an array of domains. The server can say here are all the domains I own. The spec says brwosers might apply different rules to these domains. that's what we're trying to do. Firefox has the allowlist with some differences, an exception to a blocklist of trackers. in the IETF there was the dbound working group which was formed when Mike West published FPS. In Oct 2020 they published something. Not exactly the same thing but they're saying that we want orgs to define policy boundaries. Different levels of access to cookies, not redrawing same origin policy but trying to define what first party means for those domains. Other applications, not just cookies. This is a problem that has existed on the web for a while. There have been other attempts but we're hoping with FPS that a) the site author has agency to tell us what the collection of domains is, that's how there are no mistakes. The disconnect list is mainted is really ad hoc. How domains get added, someone in firefox will file a bug, the site author is never involved. very obvious mistakes. Of course its not exhaustive, its an allowlist that's an exception to a blocklist. That's why this is an important problem to solve. We recognise its a foundational change. We're trying to define what first party vs third party means.

Dan: Thanks. A lot of what you're saying is related to the feedback we had in our very last paragraph which is about the thing that raised our alarm bells was same party cookies. It wasn't because we're against the ideas that are being put forward, but because we didn't understand the layering in this case. To address the layering issue. The TAG is on record as supporting rigourous layering when it comes to specs. I mentioned the 2013 reinvention of the TAG, that was happening by the same group of people that also put together the extensibel web manifesto which talks about layering, we were involved in a lot of stuff. We're pro layering. The issue was that we saw when we're talking about such a fundamental layer that the scope is left open quite a bit as with FPS that was the thing that gave us some feeling of discomfort. Whereas in this case if .. I don't want to force you to pick a solution, but in this case maybe if we'd seen the proposal come through in the same breath, same party cookies an din order to do that we want to put in place FPS which will have a scope limited to supporting same party cookies. That makes a lot more sense to me. 

Brad: On governance, when we first proposed first party sets in a privacyCG face to face, we asked does firefox or edge have a policy they apply for entities.json because we wanted to start from that? They didn't have a policy that was in place. The desire, governance wise is to have a common policy and a common set of sets. The other bit on the layering.. layering is helpful but it primarily is driven by the cookies issue and the communication that provides. To point to another proposal which is still in incubation is privacy budget. One thing privacy budget mentions is that it needs to be applied to a set of communicable domains. Today that's the internet, it's not really a plausible solution. As long as third party cookies exist the set of communicable domains is all domains on the internet. If we eliminate thid party cookies it's one domain. In the presence of first party sets a budget needs to be applied across the whole set. A limitation applied to the whole set. Having the layering of an easy to consume version of what is this set of domains is useful for other specs to take into consideration. Another spec we've propsed further along with a similar issue is conversion measnurement. One of the things conversaion measurement is trying to do is limit the amount of information leakage between pairs of domains. There are limits in place to make sure you can't leak too much deata between a publisher and an advertiser over a certain amount of time. If there is commnication between two advertisers or two publishers it doubles and doubles again that communitcation channel so that limit neesd to be applied across the set of communicable domains. That's where being able to consume FPS as a primitive is useful outside of cookies but it hinges on the fact the domains in that set can communicate through cookies.

krgovind: the feedback about better use cases is great, i'll add a few more. When we wrote the explainer a lot of thsese other proposals were in early stages, we knew roughly the role of FPS but were still formulating all of that and writing these explainers. Now some of these are defined it is time to revisit. The intention is.. this is why we use the phrase privacy boundary, i know it is vague, trying to say these sets of sites are one thing, one site, any leakage of information across those sites is what 'tracking' means. We're talking about tracking across those blobs. Today for the most part the way safari does it, registerable domain is the blob, but we know based on the background i gave earlier, registerable domain doesn't serve well as a privacy boundary. The origin remains, if a domain sets a cookie, only a request to that domain will have that cookie set. You won't send it to gstatic.com, that is what the same origin policy means. We're not saying that with FPS gstatic and google.com are in the same set, we're not saying a cookie bound to accounts.google.com is not going to be sent. That seems like a common misunderstanding of the proposal. 

Brad: A way that has helped communicate the concept is maintaining third party relationships but only within the set is the core concept. Restricting outside of these is the core concept of what this is trying to accomplish.

Dan: some of the issues that have been raised around scope, eg. what about permission requests? I've given this origin permission to get my location or to listen to my mic so if you imagine .. You're facebook (who are positive about the proposal) and you own instagram and whatsapp then if I want to use instagram and give it access to my camera, facebook might say we really want ot use FPS .. instagram and facebook and whatsapp are thes ame company, same organisation, if somebody gives access to camera  in one place we should be able to get access in all of our other properties, that would go against the user promise that the web has you are incontrol of who has access to your data. I understand the feedback was no this doesn't apply to permission equests, however coming back to the scope creep issue I can imagin ea future in which the people would want to push that kind of thing into the scope or would want to redo the permission model for things like get user media so it now respects a different privacy boundary as you're talking about.

Brad: that's where the framing of maintaining existing third party relationships is useful. When we facebook gets permission today it isn't automatically granted to instagram just as it isn't automatically granted to every third party on facebook. Perhaps that framing would be useful to make more explicit in the exlpainer. That is the limitation of scope here, maintaining *existing* third party relationships within the set, on things we would be intervening or restricting going forward.

Rossen; what would prevent dan's scenario and how? If FPS is in market today what would prevent facebook realising this scenario through FPS? Maybe I didn't get your explanation as to why technically it's not possible

Brad: technically they aren't capable of it today. We're not looking to expand any capabilities with this. 

Chris H: another way to say it is that the browser just wouldn't allow that. It wouldn't use FPS to share camera permissions. Therefore facebook woudl be unable even if they wanted to do it.

Tess: to riff of what Dan and Rossen are saying ,maybe the concern is the browser wouldn't do that as a matter of policy. Policies can change. If the capacity exists then there's no guarantee that policy change doesnt' happen in the future. The way to restate the concern is adding this like pandora's box. We're inviting through policy changes in the future. Whereasi if we did not introduce the capacity a policy change alone wouldn't cause those kind of negative effects.

Dan: To buttress what Tess is saying this come sback to the question of yes we understand that this replaces something that is being done now in a more adhoc way that is not standardised but one of the outcomes is that people aren't building stuff on top of it, it can't be referenced by new specifications, so when we are talking about adding this a s a new layer it opens up that pandora's box not because we now will be able to do all of those things but Im concerned there will become pressure to add those other capabilities, as we add capabilities to the web. we're in this period of history where we're adding capabilities to the web at such a rapid pace, espeically with a privacy implication, so much of our review process over the past 7 years has been focussing on privacy and specs that have a potential to infringe users privacy. In that context that's the concern that we have and that's why your'e hearing an incosnstent message regarding the layering issue.

Brad: that already exists with entities.json and we're not seeing that pressure now. Maybe you see that as a difference of it being specified or not.

Dan: yes because it's something that if it's sepcified and part of the architecture it can be somethign that people can write a dependency to. Like we came across this issue when we realised that some specs were writing in things specific requirements about how they'd operate under privacy mode but there's no specification that talks about what a privacy mode is. 

Brad: isn't that proof that being a standard doesn't actually mean folks won't try to..

Dan: in that case we pushed back, said would it help for the TAG to write what privacy mode is and we did that .. there was a need for that document so we wrote it.

Tess: as an existence proof of mechanisms in this general area, when they exist coming under pressure in this area this is a recent thing is the flood of requests to alter the public suffix list that have come in recently due to some advice facebook is giving lots of advertising companies and the PSL is a volunteer project that doesn't have resourcing to handle that incoming set of requests. That demonstrates that if you have a capability there's going to be pressure to expand its use in ways that maybe you didn't envision.

Kaustubha: the PSL and facebook and the PCM... the reason this is happening is because we have these new apis which are making this assumption that the domain is the boundary. Not the same thing as in the context of FPS but highlights the fact that all of these privacy mechanisms that are replacing.. PCM wants to limit 8 bits that can be sent to the site, facebook's contention is we have sites like shopify that hosts thousands of businesses... 8 bits won't do.. we're putting pressure on the registrable domain defining the site. We have all this new privacy work we here we're trying to apply limits to blobs of things which we think are sites and today we're using the registrable domain and putting pressure on that thing and that's not good enough.

Rossen: thank you for the clarification Chris that helped. If you're an evil browser today you can enable third party cookies for everyone anyway and you can do the same thing for FPS. What are the next steps here? 

Dan: we need to start talking about where we go from here

Chris H: I'd like to ask if not FPS, what do you think is a ecommended solution for.. do you have a solution for removing third party cookies and avoiding this problem? Do you think you'd recommend Chrome adopt a similar approach to what firefox and safari are doing with an adhoc allowlist?

Dan: we don't have a consensus view on a good solution. One of the things we resonated with feedback we saw from Mozilla, that it looks like it's trying to codify and calcify a technology or an approach or pattern that is there because cookies are a mess. People have used them in this way and they're being abused and let's build that into the browser now and make it a standard. That felt a little inflammatory, sorry, not intended to be.

Chris H: we all agree there's a problem. The other brwosers also have mechanism sto try to address this immediate need. You recommend that one possible approach is FPS.. do you recommend something like what other browsers are doing?

Dan: No. We would like to see.. the web would benefit that these allowlists and blocklists that are intransparent in nature are not part of the web architecture at all, they're diminished rather than reinforced. The question I have is: is there another technology that could come into play that could play a replacement role or mitigate against the removal of third party cookies

Tess: the storage access API is one

Dan: http state tokens as well have been talked about as another proposal. There are multiple things out there that are trying to replace cookies or trying to make a better cookie. Could those be .. that's more our thinking

Kaustubha: two technologies mentioned, state tokens is easy to respond to, we're also interested, its a replacement for cookies but doesn't do anything to define what these blobs of sites we talked about. I'm on board, that's one of my pet projects to replace cookies with state tokens. Tess talkeda about storage access api, we've considered it, but as the TAG pointed out in the FPS feedback, how can we expect users to meaningfully answer questions like would you like google.com to get access to storage on youtube.com, or facebook.com access storage on nytimes.com. we have thse highly composable sites, like microsoft has sharepoint which embeds previews from excel.live.com ... a very common pattern today. you're asking questions of the user where the question they read is "click yes or the site does not work"

Dan: that's an antipattern, absolutely

Brad: similar to what Kaustubha was saying, we're skeptical of the ability for users to answer questions for request storage access, I don't think putting that onus on users to make those decisions is a pattern we want to get into. the other bit is delving back to data limits with privacy budget and measurement apis.. with request storage access api it is most probably that you're going to get sets of domains that get access such that they can join user identity across them commonly. googl eand youtube will have a high yes rate to that question, or icloud and apple, or instagram and facebook. We then can't necessarily reason about enforcing those limits across domains since it is an ad hoc issue. 

Dan: this has been a really productive discussion. We need to close up. Would we benefit from having a part 2? I do. Next week? Same time?

Chris W: I would not but I'm not required

Tess: not next week either

Dan: if we hare happy to do this again I'll try and schedule part 2.. then we can take further discussion on to the issue

Kaustubha: we should probably tighten up and add use cases and examples and expand motivation. That's one takeaway for me.

Dan: use cases which is part of definition of scope. To me that's one of the major issues. We didn't really get into the governance stuff enough today but that's another area. THe use cases and scope is really one of the things that is causing the most anxiety in the group. 

Rossen: action item with a proposed agenda of what we didnt' get to?

Dan: I'm doing that














