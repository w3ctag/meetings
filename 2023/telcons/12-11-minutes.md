# TAG Teleconference
#### 11-13 December 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-12-11](https://www.timeanddate.com/worldclock/converter.html?iso=20231211T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Privacy Principles](https://w3ctag.github.io/privacy-principles/) - Ready to publish?
* [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov
* [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss
* [Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @rhiaro, @plinss
* [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [@page margin boxes](https://github.com/w3ctag/design-reviews/issues/918) - @LeaVerou, @atanassov

### Breakout C (APAC / Europe) - [2023-12-12](https://www.timeanddate.com/worldclock/converter.html?iso=20231212T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Protected Audience with guest Martin Thomson
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @cynthia, @torgo
* [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @cynthia, @torgo, @rhiaro
* [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman
* [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @hadleybeeman

### Plenary Session - [2023-12-14](https://www.timeanddate.com/worldclock/converter.html?iso=20231214T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Amy, Yves, Hadley, Rossen,

Regrets: Lea


### [Privacy Principles](https://w3ctag.github.io/privacy-principles/) - Ready to publish?

Peter: Any objections to publishing?

Dan: to be clear, the call is for TAG consensus on the principles of the document - proviso that some editorial is yet to happen. 

Dan: unless someone comes up with objections between now and the plenary then we will declare TAG consensus.

Peter: agreed.

### [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @plinss, @atanassov

Peter: we haven't heard back from them on the last reply to their response... 

Rossen: let me ping internally and see what's happening with this. They're still interested in moving forward and are going to update soon.

*punted for now*

### [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss

Peter: holes in their heuristics. Lea's primary point which I agree with is just relying on heuristics seems fragile. Not being able to override is problematic

Dan: looks like Yoav was agreeing with you .. future iteration..

Peter: makes the point they've experimented for a year and haven't seen a lot of instances of these other ways of navigating being doing. Question what he's looking at. Not seeing CSS only navigations is not surprising because that's a new feature, but it's going to become more popular over time. The bigger issue is not having any author control over the heuristics, or augment or override the heuristics. Not harmful. But just a performance thing... bigger issue if it ever gets folded into something else, a higher level detection of navigation, other concepts of navigation. Would still like Lea's feedback.

Dan: does it make sense to set this to proposed closed and get Lea's feedback async?

Peter: currently satisfied with concerns, not sure if Lea is willing to do that.

Dan: bump it

### [Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) - @rhiaro, @plinss

Amy: we definitely discussed this... can't find minutes

Peter: i remember being concerned about : don't we already do this? but it looks like they are taking that into account and going beyond the protections we have...

Amy: was Lea's concern that this would make visited links useless to end users?

Peter: concerns about ... most visited links would not show up as visited..   Triple keying - target, domain and top level domain... 

Amy: my perspective is that's probably a reasonable trade-off for not leaking your history... but don't have a good sense of how useful visited links state is for most other people

Peter: personally - search results - visited links are useful - that would not break.  Similar a wikipedia site - that would not break.  It does break if it's cross-site. If I visit a site where I've never clicked on a link 

Dan: Say you visit a link on a social media site to an article in a blog.

Peter: and then you visit another social media site has a link to the same article - it would not show as visited.  Users will lose some utility and some may be confused but it won't be the most common cases where we expect visited links to work.

Dan: what do other browsers think of this? No signals. We could say it looks good, we understand the tradeoffs, what feedback is there from other browsers?

Peter: agree we should ask for feedback from other browsers. Not sure we should say it looks good yet, some concerns about user expectations

*Peter to leave feedback*

### [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov

Rossen: it's important to have this ability as a further optimisation, trying to express and capture the ened user behaviour from something deep in the layout pipeline like this is difficult and maybe the author has found a challenge.. I'm fine with moving forward with this one

Peter: close satisfied?

Rossen: yep

*Rossen to leave feedback and close as `satisfied`*

### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

### [CSS ::selection Inheritance Model]() - @LeaVerou, @torgo

*bumped to plenary*

### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

Dan: I feel like Lea had opinions on this..

*bumped*

### [@page margin boxes](https://github.com/w3ctag/design-reviews/issues/918) - @LeaVerou, @atanassov

Rossen: great addition. Bridging technology that already exists for some of the printing renderers. Suggesting that this capability should be able to target different parts of a page when the content of a given document is printed. If you want to add additional content and target specific areas of the page with it. The additional granularity of targeting the margin areas allows for higher and higher quality print scenarios that are already possible to some of the industry standard renderers that are not necessarily browsers.  I'd say we can close satisfied

Peter: this is just talking about page margin boxes that have been defined for the last 15-20 years and chrome wants to implement it?

Rossen: right. Princexml is already doing it

Peter: so not adding anything new? Just implementing?

Rossen: yeah, it's basically what's in the spec

*Rossen to leave feedback and close*

### Meeting schedules for holiday season

*We agree to hold meetings week of the 18th and we agree to cancel breaks A and C on the first week of the new year.*

### Appointments

Yves: think about who should be appointed.

### [F2F](https://github.com/w3ctag/meetings/tree/gh-pages/2024/01-london)

### VC Review

Amy: We need to get consensus on this review comment... 

*working towards consensus at the plenary*

## Breakout C

Present: Dan, Max, Yves, Hadley, Amy, Sangwhan, guest: Martin Thompson

Regrets:


### [Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) with guest Martin Thomson

Martin: contextualize the whole thing... overall context is - number of people want to make sure ads continue to work - the ways it currently works are terrible for privacy... Google are looking at ways in which they can make small trade (privacy loss) for huge utility for advertisers. First area is attribution measurement (PatCG) - you put an ad on one website, measure it somewhere else. That allows advertisers to get a lot of value in a context where they get good strong privacy protections

Dan: that's an area where there are 3+ proposals in flight.. different types of measurement and they don't seem to be synced up, and this is frustrating

Martin: the PATCG's primary task right now is sorting out the three aggregator proposals. Two are starting to look like they're getting closer together, but we have a major question to resolve between those two and the other one. We can talk about that another time.

... The second thing is Topics. The idea is take some information about your browsing activity and give it to every website you visit so they can enrich their contextual targeting with information about you. I don't like it, the design isn't very compelling, but different perspectives might come to a different conclusion based on the same research.

... And the third thing is protected audience is convoluted. It doesn't have good privacy properties. If the baseline is a web which respects contextual integrity to some degree, it breaks down all of those barriers in a lot of different ways. The system of patches to cover up the holes are interesting, complicated, and oftimes not actually very effective. 

There are multiple states to think about this proposal - the ultimate end state they're aiming towards, and all of the intermediate states with respect to their strategy for getting towards that end state. Currents tate - 3p cookies are a thing, and protected audience provides zero privacy protections relative to 3p cookies. That's the baseline right now. As google roles out the 3p cookies deprectation, the plan is to remove the very worst of the privacy holes in the proposal - intermediate stage. Lots of things on the roadmap for 2025-6 that are features related to that that they'll keep for some amount of time then introduce some amount of time and remove from 2026. Sometime in a two year timeframe they're going to start implementing stricter controls, and that's not the final state they're aiming towards. 

The basic goal they're trying to achieve is to have sites build up information in the browser about you based on their observations of your activity. Then to use that information for ad targeting, without necessarily reveleaing what they've recorded about you or what the results of the ad targeting where. You'll browse and do some things of interest to advertisers - look at a product or read an article - and the advertisers will record that as an item of interest, which goes into a db in the browser. At a later point you'll go to another website, and that site will want to do remarketing or advertising based on that db. It sets up an auction, which is essentially a series of isolated js realms which run snippets of code from people who registered these interests. They can access cross site information in these js realms and use this information to make bids. you'll have multiple annotations across the web owned by a particular advertising business. The ad business will enter the auction, get ... look at items of interest, and decide what to bid on in the context. Fed information from the context, from the person setting up the auction, and the annotation they made, will go into this js realm. The person running the auction gets a set of js realms - they'll see each bid in an isolated context, with private information that has been accrued. They ask does this meet my standards for a bid in this auction? I might discount it or eliminate it. The ad might not be appropriate in the context. The browser will take the winning bid after bidding and screening, then show the ad. It can't just show the ad.. it has been derived from private information. It has to show it in an isolated context, so the webpage doesn't know what ad has been placed. Idea is some aggregated reporting system that will report on what ads were shown and hook into the attribution measurement that we were talking about earlier, so people who placed these ads know whether or not they were working.

Dan: what stops the ad network from knowing more information about the user's browsing history in this scenario? Why is it not possible for the ad network or some 3p to simply query and exfiltrate that data back out of the browser?

Martin: currently nothing. Currently deployed as it all runs and the URL is spat out the other end, you can just ask for it. Throughout the bidding process, the person making the bid can insert whatever information they want into the url, the screening person can add something extra, then at the end you can harvest that information. But the idea is that the js realms will be isolated completely and they won't be able to communicate with the outside world. This is an information flow control system where you have elevated privileges in terms of access to information, but lower priviligeds for exfiltrating that information. I have my reservations about the way in which that is possible, but that's the idea.

Dan: what's mozilla doing relating to this?

Martin: I'm engaged for communicating with regulators and folks like you. Mozilla doesn't see any prospect for implementing anything this elaborate, and with these privacy prospects. We think the prospects of it being sufficiently private in the near to medium term are basically zero. The amount of effort required to get it sufficiently private is phenomenal. We don't believe the current design is capable of maintaining the isolation required.

Dan: how this impacts marginalised communities more than other web users?

Martin: my primary focus is does it provide the properties that google claims it provides. Might want to consider whether it has good effects on equity or creates interesting power imbalances in the way the web is structured. From that perspective I've not spent a lot of time on that. I don't think it changes the situation significantly from what we see today. I'd say the overriding goal for this project is to preserve the status quo.

Dan: we in the TAG are taking a fairly strong view on deprecation of 3p cookies. 

The other question.. isn't that what Topics is doing? How is it related? It's also collecting interests related to users browsing history. Why would I be implementing both topics and this?

Martin: I can't make firm statements about this. The way google talks about it is that they're complementary technologies. Topics provides a small amount of information about a person, it integrates well into existing targeting sysstem without too much work. This one is more complicated, difficult to set up and operate, vast amount of effort required just to get bootstrapped. They've got to set up servers and domains and they don't know what's going on because of reporting mechanisms. Topics is a small subsidy in light of the lack of cross site information coming into your ad targeting system. A very weak signal about someone's interests, and this would allow delivery of more specialised advertising experiences but at a much higher cost.

Amy: thanks for that - very helpful - we heart about why mozilla is following this. Do you know about other implementers?

Martin: I know MS are implementing.  They're doing their own implementations - not just picking up the chromium code - with their own opinions... server infrastructure side...  Haven't seen any other browser engine demonstrate interest... 

Yves: on top of the companies themselves, there is the pressure of regulators that want to chime in on what is required or not. That may impact what different companies will implement in the end. It's a difficult question.

Martin: one of the reasons I think google are very much interested in this stuff is that they see the regulatory pressure from eg. the CMA is relevant here. They want to make sure that when 3p cookies go away then people whose business depeend on advertising, particularly small publishers, don't have significant reduction in the efficacy of their advertising. I don't know how to assess those claims and I don't know if anyone has a good graps of that. Research presented under constraints and conditions that are very unclear. Hard to know what the volume of the impact is on a news publisher. The research helps us understand there is going to be some amount of inmpact, but not how much, when they're competing with folks with a similar disadvantage.

Sangwhan: I don't knwo the full context of the limitations of claims google is working on, but the response I've received from the privacy sandbox folks is that the advertising industry that is not google thinks that the fact that google as a big ad company plus a big browser company having access to all this information even when 3p cookies are disabled gives them an unfair advantage, so they should have some level of information they need to serve ads, and that is what makes 3p cookie deprecation in chrome very complicated

Martin: small publisher industry folks are concerned about their advertising efficiacy relative to big players like googles. Removal of 3p cookies makes the value of 1p information that much greater. That skews the market in favour of big players like google. Some people claim that gives them an unfair advantage

Dan: we had a [session with michael kleber](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/06-12-minutes.md#privacy-sandbox-special-session-friday-the-16th-at-1500-uk-time) where we go through this.

Martin: the CMA is interested in what everyone thinks, and taking this project very seriously. They understand the technical characteristcs of what's going on. The primary remit is the competition aspects, but understand that the privacy impact is important.

Hadley: we've talked about, with both this proposal and tpics, shifting the role of the UA from representing and protecting the user to representing and acting on behalf of the advertisers

Martin: more in relation to Topics.. uninformed legal opinion... if the UA truly is acting on behalf of the user and collecting information about their interests and giving it to other, that's the user acting to give information to people, which means they're far less constrained in how they use it. I don't subscribe to the absolute view that the UA has no obligation to anyone other than the users. There are interesting collective governance questions. Robin gave a talk on governance and responsibility. There is a role for the UA to act on behalf of users in the aggregate. Their interests might be represented 100% to the exclusion of all other actors, but the quities of all other actors in the system are so dramatically affected by the loss of 3p cookies, making some small allowance on the part of users for a significant gain for advertisers has a big effect for allowing the system to continue to operate. If the UA makes decisions in the aggregate with opt outs etc, such that people are able to support their business througha dvertising more effectively, then people will have access to content without subscriptions, and the net benefit to users outweighs the use of those APIs. I don't think that's a good trade with protected audience or topics. I think it's a good trade for the attribution work. Finger in the air analysis, will depend on things like the parameters chosen.

Hadley: helpful.. why is this more in relation to topics than protected audience?

Martin: there's a useful distinction. If you look at the ultimate goal of something like protected audience, the structure is such that advertisers get to use private information but they don't get to collect it, so the uses are tightly constrained and limited. The effectiveness of limitations on a technical level are something to examine. But the idea behind the whole thing is the uses are clearly constrained and concretely if protected audience works as intended, the only thing that advertisers will learn is aggregated information about the efficacy about particular advertising strategies - that's the goal that's being set. In theory that's attainable, in practice, a good number of years worth of R&D to go into that.

Sangwhan: there are many proposals being put forward .. some are competing, some are different ways of approaching a similar goal. What it boils down to and what we've been hearing at google is google's proposals are the ones that advertisers seem to be excited about therefore that's why they want to do it. I imagine there are other concerns and proposals also getting traction. We want the PATCG to sort out a winning solution. But finding consensus on a topic with no right answer is really hard.

Martin: at least on the attribution front we have a process in place now where we can make a decision. There are clear tradeoffs being made. Some prospect of reaching a conclusion sometime next year. The harder questions are wrt to topics and protected audience. A number of people believe this is not worth doing. Meta don't think this is a good idea. One of the properties of protected audience is that you don't get to know what ads are being displayed - that's a dealbreaker. MS say they can make this work, can implement the correct brand safety controls. But we haven't started on that conversation. 

Sangwhan: on the non-google proposals, what reaction have we heard from smaller ad companies like criteo?

Martin: criteo have been constructively engaged. They're investing to some degree, and this is their jobs and they're taking it seriously. Not a clear signal about preferences. We've talked about optimisation for ad placements etc. They've done some work. There's a huge market out there, so there's a spectrum.

Dan: hIt feels like there are certain browsers who just don't want to use 3p cookies, and others who don't. We hear a lot of different arguments about why 3p cookies can't be deprecated, but browsers that don't use them are still use-able... Thoughts?

Martin: On those disabled 3p cookies, the storage drives an enormous hole. There are user engagement gestures and things in heuristics, but they have a massive play. At the same time, there is a desire to wind down those exceptions and find ways to put poeple in control of what's going on. I was an early proponent of FedCM work, but implementation has gone down a pretty bad path, but we're still broadly supportive. We have an implementation but haven't turned it on.

Dan: let's have a separate discussion about that

Martin: Yes. Also, all the anti-fraud and stuff.... it's languishing in a CG, and needs far more weight put behind it. WE've looked at the various proposals, like Web environment integrity. It's dead. The team were distressed at the reaction from teh community, didn't understand that. I've got a blog post coming this week on Privacy Pass, which is related. We don't think that works either. That leave s us with a hole... Areas with prospects: real world ID, gov ID, etc. Huge risk on other side, but yes. That will be something to take very slowly. One of the problems with Google's approach is they wanted to get everything in place before deprecating 3p cookies, a 10 year project in 3 years. Not worked well

Sangwhan: a lot of these hiccups are related to that. Not all of the team are browser people, they solve the problem they're given. Web environment integrity is a good example. Some people in Chrome think it's a bad idea.

Martin: there were a number of people who reviewed it. The folks who presented it to me said, "we thought this was in a bad place when we first saw it, but we now think it's better." One of my colleagues found it risky. And then it blew up.

Amy: We discussed user opt-outs... I couldn't find anything on that. With topics, we found a mitigation where user can opt out of a topic, one by one. (Privacy labour there isn't reasonable.) But with protected audience, there deosn't seem to be a limit.

And it seems like most of the work is happening on the users device. Seems excessive.

Martin: primarily, yes. But there is a mode where the auction is executed in a trusted environment in the cloud somewhere. Ends up costing more in networking and less in processing, but I think not. We'd like opt outs to be indistinguishable from regular user behaviour. the api continues to look like it's working... we don't have a convincing solution for protected audience. 

Amy: That's well as a principle, but there shold be a way to enable the user to opt out.

Martin: it's possible to opt out... you could turn the whole thing off... you can still have the API accept interest groups... store info on what groups are there.. then you can "fake it" and pretend that the auction failed every time.. Will look like a new user, etc... but ultimitately the advertiser won't know.

Amy: we've heard that it's reasonable to look at each topic and opt out of each one... i don't think it's reasonable.

Martin: haven't looked at this.

Max: proposal says shifting from server side to browser side will have stronger privacy guarantees - any analysis or data to support this?

Martin: no. Isolation properties of the system - information goes into browser and websites can ask you to perform queries, run auctions, and ads are shown. There's so much leakage out of this system that I don't think claims about being able to maintain isolation are reasonable at this point. Maybe there's a future version that have privacy properites we can stand behind, but the current system is not reasonable.

...I think the TAG is in a position to decline reviews. This one is a signifiant amount of work, is a proprietary proposal. You could say something on whether the system should exist or not, like looking at whether opt-out is possible -- but I would not go into any significant detail.

## Plenary Session

Present: Peter, Max, Dan, Sangwhan, Hadley, Amy

Regrets: Yves

### Privacy Principles

Sangwhan: still needs editorial work, language is too complex

Dan: we're still working on that, we want to know if the TAG has consensus, with concerns remaining about language and editorial work

Sangwhan: I can try to write some actionable feedback. Not blocking.

*discussion of how to make the document more accessible to spec developers*

Sangwhan: the style guide says to get to the point... Being able to skim through the ToC and knowing that the section is relevant to yourself.  Right now this would be unusable for htis purpose.  Anything over 15 pages then this document should have a better ToC.  This is 53 pages.

Peter: I don't disagree... I haven't heard anyone arguing that you're wrong. Let's back up a sec. Anything about the principles themselves that you'd object to?

Sangwhan: Principles themselves I don't see anything that stuck out.

Peter: Are the problems with the structure and readability sufficient to block publication at this point?

Sangwhan: Structurally I would say yes - not ready for "prime time" - but iteration post-release is possible.  If we want to finish and deal with the editorial later then I'm fine with it.

Amy: What if we put something in the status of the document that it's still undergoing editorial revision.

Dan: the point of the resolution is that the TAG is happy with the substance, and editorial work continues

Sangwhan: I will look at the principles summary and provide feedback on that.

Sangwhan: I don't want to block.

Amy: flag your concerns as they come up.

Peter: not discounting your concerns - if there's something that needs to be removed we can still do this.  But is there sufficient concern to block publication?  I'm hearing no.  I am hearing that there is a lack of objection to publish. 

Amy: we have a bunch of issues on the "back burner" as well that we will address after this draft.

Peter: I haven't find anything that is objectionable.

[discussion about language and audience and how document is used]

**RESOLUTION: we agree to publish Privacy Principles as a draft note. We note that there is significant editorial work to be done, including making the document more accessible to spec developers - a key audience.  However the TAG does not object to any of the core privacy principles at this time. The TAG will continue to provide editorial feedback. Update the doc to say to the effect 'the substance of the document reflects TAG consensus...'.**

### [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo

### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

### [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @cynthia, @torgo

### [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @cynthia, @torgo, @rhiaro

### [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman

### [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @hadleybeeman


### VC Comment

Amy: Can I post the VC comment to move this forward?

Peter: Happy with you posting it.

### Breakout Rollup

#### Breakout A

#### Breakout C

*we discuss the discussion on protected audience with Martin*


Amy: will TOPICS get deprecated if Protected Audience goes ahead?

Amy: Martin said that work is ongoing in attribution reporting specs... Sounds like we should wait for PATCG...?

### Issue Triage

### Peter's new Finding

Peter: New Finding? The purpose of the web is to connect users - not to monetize people. You're not supposed to be monetizing and surveilling.  Not anti-capitalism but anti abuse.  No problem with businesses being on the web.  Huge problem with businesses monetizing the web itself and monetizing the users of the web.

Amy: there's often a false dichotomy of either surveillance capitalism or you have to pay for stuff. There are other ways to do things.

Dan: I like piercing false dichotomies. Be great to do something that highlights the positive aspects of commerce. Scenarios that involve commerce and money that are also good about privacy. I'm at a cafe, scan a qr code, pay for something with web payment, but because of the privacy aspects of the browser and web payment the cafe doesn't know anything about me.

Amy: and the 3p menu provider also isn't collecting your data..
