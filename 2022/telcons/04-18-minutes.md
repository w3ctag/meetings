# TAG Teleconference
#### 18-20 April 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-04-18](https://www.timeanddate.com/worldclock/converter.html?iso=20220418T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [Cookie Expires/Max-Age attribute upper limit](https://github.com/w3ctag/design-reviews/issues/729) - @ylafon, @hadleybeeman
* [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

### Breakout B (US / APAC) - [2022-04-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220419T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou
* [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [FYI Review of CSS Fonts 4 `font-palette`and `@font-palette-values`](https://github.com/w3ctag/design-reviews/issues/719) - @LeaVerou, @plinss

### Breakout C (APAC / Europe) - [2022-04-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220419T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion
* [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman
* [FYI - MediaCapabilities API for WebRTC](https://github.com/w3ctag/design-reviews/issues/720) - @cynthia

### Plenary Session - [2022-04-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220421T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Amy, Peter, Dan, Lea,

Regrets: Hadley, Yves, Rossen

### [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov

Peter: browser mediated take on SAML...  trying to fix the things that will break when we lose third party cookies... It smells like an early review.  They have a manifest - browser calls an identity provider for basic information like branding.  They should add light and dark color modes and follow some of the examples of the webapp manifest. Concern: they have an accounts endpoint which could be abused... Not sure how to get around.  The browser can hit an IDP and ask "does this user have an account on this service" - not sure how they identify this.  A nonce?   They say many places they haven't worked out the details...  Needs to be designed so crawlers can't just scrape all your accounts.   Renamed evolutiuon of WebID...  

Dan: **todo: link to WebID discussion with Sam Goto**... 

Dan: I felt quite positive about the initial WebID propsoal.  

Peter: overall the direction is good the approach is good.. reusing as much as you can... you won't have to rewrite everything if you're building an IDP...   We need more data.

Peter: SAML and OIDC require public key crypto ... don't see anything here doing that.  They do also have section on privacy.. will look at that more and leave some feedback.

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Lea: generalisation of the prefetch/prerender attributes.. using json blob to define these rules in a sript element. Weird. There is precedent. Unclear .. syntax is confusing. source list / source document.. things to be said about syntax. Score is unclear how it's used. Question of do we want this logic to lie in a script element as json or should it be an html based syntax. Motivation - I am convinced, mentioned example of quicklink library that determins which links to prefetch automatically. Whole process is explicit, authors need to duplicate links to prefetch in the head. This allows the to handle this en masse to some degree. More extensible because its json, can add more properties. Main point is do we agree that this is a problem that needs to be solved, and is json in a script element a good way to solve it? Low level stuff we can talk about another time, or just leave a comment. I don't know any history about this.. seen speculation rules in our agenda a few times.. some background?

Dan: based on speculation rules? Leave comments and questions..

Lea: [will leave comment]

### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Dan: thoughts on turtledove: it's in WICG. Why isn't it in Privacy CG?  Where is this going for **standardization after WICG**?  Says "unknown" but what is the thinking?  Its not clear from the link provided on **multi-stakeholder** descussion whether there is any interest from additional implementers or stakeholders in this API.  Can they please be more specific?  It's not immediately clear how this relates to the **topics API** since it looks like this is trying to achieve the same aims but there's no reference to the topics API in the review request or the explainer.  It looks like this proposes each ad request be doubled - one request for a contextual ad and one request for an ad "indicating an advertiser-identified interest" - at a minimum this would would double bandwidth requirements for ads which would be problematic from a power consumption / network usage PoV.  As I understand it, the *contextual* request and the *interest-group* request are sent at the same time (and the browser decides which one to display). However the *interest-group* request does not contain contextual data such as the URL the person is visiting.  This is claimed to be a privacy benefit but couldn't the ad network easily correlate these requests considering all the additional metadata they might have access to including timing and IP?  (They have some mitigations listed... )  The idea of an **on-device auction** is worrying from a power consumption perspective especially when the user is likely on a smartphone.   It seems like they are thinking through some of the privacy issues - however the proposal is rooted in "how do we support the existing ad ecosystem".

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/723#issuecomment-1101573160)

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

"the API’s utility isn’t yet clear"

Amy: they have pre-empted our FLoC questions for Topics

.... loads of issues probably worth reading

... Ad topics eventually sourced from a third party (todo: who?)

... Browser classifies sites.. sites providing their own topics is an "open question".. interesting to think about variation in ads across browsers then?

... 5% random noise, for plausible deniability. Attempts to avoid cross-correlating user between sites. 

... Story about sites accumulating topics? Even if only one per week. Aggregating topic data with existing user data (from fingerprinting, cookies, etc)?

... Can sites opt out of being included in the mapping to topics? (Other than by havin an 'opaque' host name) - yes (header, and also have to call the API). How many topics can map to a single site?

... Definite improvement over floc.. more transparent

... Risks with colluding sites (documented). Risks with unintended correlations of topics to sensitive topics.

... "better for user privacy than cookies"

... Lots of open questions under discussion

Amy: definitely better than FLOC.  It's in the private advertising group.  Tons of discussion on the privacy stuff.   It's comletely different to FLOC.  No cohorts.  Ways it can be abused but it's documented and discussed.  It seems better. Ton of open issues. I'd like to look through a bit more.  The direction this is going is saying there's no privacy-preserving way to do targeted advertising ... so maybe they should stop trying?

Amy: up front there are a lot of mitigations - like 5% random noise (less of a fingerprinting vector) - list of topics is human-curated and transparent and would ship with chrome.  

Peter: a lot of evidence that targeted advertising can be used for political purposes... to negative effect. Also questions on effectiveness in general for commercial purposes.

Amy: question about multi-stakeholder.  

Peter: i'm wondering if we shouldn't have a finding "stop targeted advertising."  

[discussion about legal future of surveillence for advertising, collection & sale of user data]

Lea: what about websites that can't afford another business model?

Peter: not saying ban advertising altogether

Dan: whether or not it's correct that targeting affects the real value of an ad, whether it influences someone's behaviour, it is the case that targeted ads make more money. Still an economic issue. If targeted ads went away tmorrow there would be a certain number of websites that have a big income drop. It's a concern. Publishers would not aagree with the statement that we should ban targeted advertising. Robin Berjon's take would be interesting.

Lea: unpopular opinion - if targeted ads could be done in a privacy preserving way, it could be better for users - as long as it's opt in, users can see ads that are relevant

### [Cookie Expires/Max-Age attribute upper limit](https://github.com/w3ctag/design-reviews/issues/729) - @ylafon, @hadleybeeman

### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

**bumped 3 weeks** as Elad got back to us and said it was still in the pipeline.


## Breakout B

Present:

Regrets:


### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou

### [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

### [FYI Review of CSS Fonts 4 `font-palette`and `@font-palette-values`](https://github.com/w3ctag/design-reviews/issues/719) - @LeaVerou, @plinss


## Breakout C

Present:

Regrets:


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion

### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion

### [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman

### [FYI - MediaCapabilities API for WebRTC](https://github.com/w3ctag/design-reviews/issues/720) - @cynthia


## Plenary Session

Present:

Regrets: 

### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

### Issue Triage
