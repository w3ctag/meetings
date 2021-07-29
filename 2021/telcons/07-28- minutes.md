# TAG Teleconference
#### 26-29 July 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-07-26](https://www.timeanddate.com/worldclock/converter.html?iso=20210726T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Private Network Access (fka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss
* [HTTP 103 Early Hints](https://github.com/w3ctag/design-reviews/issues/638) - @torgo, @ylafon, @plinss
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov
* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov
* [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro, @hadleybeeman
* [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman

### Breakout B (US / APAC) - [2021-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20210727T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov
* [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober
* [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov

### Breakout C (APAC / Europe) - [2021-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20210727T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon
* [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov
* [Request for review: CSS tree-scoped at-rule names and references (for @font-face, @keyframes, etc.)](https://github.com/w3ctag/design-reviews/issues/659) - @torgo
* [Shared Element Transitions - Early Review](https://github.com/w3ctag/design-reviews/issues/631) - @cynthia, @LeaVerou, @plinss
* [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2021-07-28](https://www.timeanddate.com/worldclock/converter.html?iso=20210728T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage
-----


## Breakout A

Present: Dan, Lea, Tess, Rossen, Amy, Peter, Yves, Hadley

Regrets:


### [Private Network Access (fka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @ylafon, @hadleybeeman, @plinss

Yves: won't be here for 3 weeks

Dan: generally supportive but they need to engage with ietf feedback.. they want us to see how they've engaged with the ietf feedback.. re-review because they rewrote the fetch integration section to be "less handwavey". [leaves comment]

### [HTTP 103 Early Hints](https://github.com/w3ctag/design-reviews/issues/638) - @torgo, @ylafon, @plinss

Yves: they need validation before implementing.  This is an IETF document... it's been reviewed... So sure go ahead.



### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Lea: we need more input. Only one comment...

Tess: we @-mentioned many people on the thread and we'd like more comments first...

Dan: punted to second week in august

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

Peter: a bunch of activity not from us..

Peter's cat: MEOOWW

Dan: they don't have a S&P questionnaire response... [writes comment]

Yves: ask if their header can be [???] ... [RFC8941](https://datatracker.ietf.org/doc/html/rfc8941)

Dan: ..user identifiable data..

[dan & yves leave some comments]

Peter: lot of privacy concerns that are glossed over... 

### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

Tess: to the extent that third parties still exist in most browsers, they are partitioned. So what does having an opt in to partioning accomplish? Chrome is the only holdout on this. This API seems not useful for other browsers.

Dan: does that include Edge?

Rossen: not necessarily

Dan: the proposal talks about safari and firefox's partitioning of cookie jar as prior art

Tess: safari tried it then backed out

Rossen: experimentation ran by maybe google folks? Is this the result? A better path forward?

Tess: we just block them now which seems to work fine. All cookies used to be unpartitioned. If you have a facebook widget on newyorktimes.com, if a facebook user visits newyorktimes.com facebook then knows the user visited newyorktimes.com. In a world with partioned cookies, facebook in an iframe on newyorktimes.com only gets the cookies for facebook when its embedded on newyork times. Doesn't get facebook if you visited as a first party. It doesn't know who you are unless you log in using that like widget. Explicitly telling facebook you'r eon that page. Facebook can't track you across unrelated sites, so better. So trying to explicitly set a cookie as an opt in.. but also unpartioned cookies

Dan: who is opting in and how?

Tess: the facebook like widget sets a partitioned cookie using this new opt in. If it doesn't then I don't know what happens

Dan: in which case facebook does get to know which article? just passively if a like button appears?

Tess: no. If a like button appears, facebook with this api can set two kinds of cookies. Partiioned or unpartitioned. In a browser that supports both, facebook will know every time you go which page you're going to because its current session cookie is unpartioned. But if facebook were to opt in to using this partioning feature then t hey wouldn't be able to. But we assume they wouldn't opt in to that..

Dan: what's the incentive for them to opt in?

Tess: this is why the other browsers just did it for them

Dan: by..?

Tess: Safari initially tried to partion cookies by default, but ended up with a couple of thorny web compat problems. There are third party widgets that anticipate having first party cookies set, and when they don't they recreate them and then .. there was a weird flow that broke. We ended up just blocking them altogether in Safari. What happens in safari is you don't get cookies or any storage, have to use the storage access api. Facebook.com on newyorktimes.com calls the storage access a pi saying please user i would like to kno wthat you read nyt articles. User says no and moveson, or says yess and you're logged in and can press like button

Dan: looks like a permission prompt?

Tess: yes, "facebook would like to know that you're browsing nyt.com"

Dan: isn't that the right approach...?

Tess: yes. Prompting the user for permission sucks for so many well known reasons. Users get a barrage of prompts and say whatever sure. There's a real concern here that the storage access api is too in your face and too frequent. I tend to disagree, unsurprisingly I'm biased, the kind of access that you're getting via the storage access api is very powerful and creepy and i think users should get enough of an understanding of that for an informed decision. Currently I can't speak to rates of saying allow or deny but it seems like users are able to make an informed decision.

Dan: is this supporting a kind of user basic function of the web that is problematic anyway? Your description of how facebook can get information out of like buttons reminded me of a famous occassion from 10 years ago [where the nhs put facebook like buttons](https://www.theregister.com/2010/11/24/nhs_connect_facebook_privacy_fears/) all over their pages including lists of symptoms, the kinds of pages that you might... privacy advocates cried foul, now I have a potentially embarassing disease and search and facebook already knows I'm looking at this page and that gets factored into advertising. they had to back that out. That's what comes to my mind. Maybe we can find a reference to that. This is not a great thing to have on the web in the first place - push back on that basis?

Tess: my understanding is they're assuming unpartiioned third party cookies are going away.  A lower friction way to get partioned cookies than using the storage access api. In safari that gets you access to unpartioned cookies. In current safari if the nhs still had those facebook like buttons, and I was searching symptoms, I go to the nhs website, there's a fecebook like button, facebook has no idea that i'm there because there are no unpartioned third party cookies in this world, but it could do partioned cookies. In this proposal doing partiioned cookies is frictionless, they can just do it. But those cookies are partitioned. They could know that there's some user who visited these five nhs pages because they get the same partitioned storage for nhs.uk. So they could know somebody thinks they have these five diseases. They can't associate that with a facebook account without you logging in using the like button widget. In that sense, it's better than the status quo in chrome. The status quo in chrome is you have access to your unpartioned third party cookies. I don't know what to do with this. It's an improvement for them. A step in the right direction for them. A regression for everybody else.

Rossen: who?

Tess: gecko and webkit

Rossen: reading issue 75 in storage access privacy repo and following johan hoffman's logic I'm not sure I agree with you. A little bit above there there was support for this expressed by eric anderson on behalf of Edge. I'm not sure it's as heavy sided as you're positioning it

Tess: talking about the status quo, not future. The deployed reality in other browsers. Experience Safari had that was backed out would be alleviated by this. The site would know about partioning and wrote code to know about it. Bugs we had were because sites didn't know about it and had issues about state being preserved across sites. This could be used to enable people to do partioned cookies .. 

Dan: coming back to the case we've been talking about with facebook like buttons on pages and some pages may tell facebook stuff that I don't want facebook to know about what articles I read, etc, would in a world where third part cookies have gone, and there is this CHIPS proposal in place, what's to stop facebook now seeing me visit pages without me having to say yes that's okay?

Tess: gets information that somebody.. it has your IP address

Dan: it can correlate that information quite easily

Tess: can probably correlate things easily already.. but this does make it easier. THey might have additional partion information that with the IP address tells them somethin ginteresting

Dan: feels like there should be an additional *user* optin. Not a site opt in.. this is why I keep asking about the term opt in. We had this discussion last week with Mike... *who* is opting in? Opt in to me means a user.

Tess: issue 75 on storage access api is exactly that. What if there was a param to request storage access that says I'm okay if my cookies are partitioned. I would like partioned access. The user would get a prompt or the UA would have some kind of preference to say I don't care about partioned cookies. Good luck with a meaningful way to tel lthe user that. But this would allow a less potentially friction experience, but still with the user opt in. That requires this in tandem with storage access api. WHich the proposers have said they don't like and don't want to do

Hadley: what's their arguement?

Tess: comprehensibility of prompt and permission fatigue.. probably other argumenets

Dan: not that they don't like that api, but the idea of asking the user for permission? because it's happening again and again? Maybe their research shows people won't answer reliably?

Tess: yeah

Peter: not following a few key points... my understanding is with embedded iframes in safari and gecko, all cookies are double keyed?

Tess: that is sometimes true

Peter: sometimes..

Tess: double keying storage generally is that's true but cookies are a weird special case. Local storage, indexeddb are double keyed in gecko and webkit. Cookies are double keyed in gecko I think. a little fuzzy. Storage access api gets you.. I can't speak to gecko's behaviour. In webkit's case you just don't get cookies, cookies are blocked.

Peter: you just don't get them at all

Tess: then you can use storage access api to say prety please user let me have cookies. If the user says yes you get your unpartioned cookies

Peter: you get unpartitioned storage? cookies also?

Tess: the storage access api when it was initially released was only applied to cookies. Didn't apply to other storages. I don't remember the current implementation state. If you get user permission you get storage that's unpartioned. I don't know what the matchup is between what' sshipping and where that will go

Peter: in theory with user permission you get access to all storage including cookies and other storage too, that would have been double keyed, but that's okay becuase user opted in. So this proposal is saying I now this cookie is partion and I'm cool with that and the browser can not block it where before it would block it?

Tess: yeah..?

Peter: If I have a facebook frame in the nyt, and facebook sets a cookie now they won't get anything under any circumstances

Tess: without calling storage access api, yeah

Peter: not even on a subsequent visit to the same site? without this flag? a normal cookie in the frame in nyt?

Tess: they never get it at all

Peter: but the theory here is they set that cookie the first time with the partioned flag, i come back next week, they will get it? but only that cookie set on nyt page?

Tess: yeah

Peter: what new behaviour is this enabling?

Tess: also hard to say too becuase the current behaviour in chrome is that there is no blocking of ordinary cookies, so the behaviour you see ends up being the same, regardless of whether you set this bit or not. When you go back you see the cookies

Peter: this proposal only makes sense when you're blocking 3p cookies. Scary where the browser isn't blocking 3p cookies and lets facebook sets a cookie that has all your user identifiable information

Tess: I'd hope they wouldn't ship this without having blocked, but I don't know what their current plan is.

Peter: there's a lot of detail in here.. I get lost trying to track what happens in every scenario reading this explainer

Dan: [writes feedback]. Should we talk about the fact that other browsers are going further? Safari and gecko seem to be blocking third party cookies.

Tess: safari is the only one blocking completely right now. Gecko does partioning by default.

Peter: safari tried double keying and that broke stuff but blocking is not?

Tess: Yep. Might be a quirk of the fact safari has always had a strictor 3p cookie policy, from the first version. The first version of the cookie policy was something like a site can only set cookies if it's been visited in a first party context. If you're a pure third party widget co and the user only ever sees you as a third party widget you never get to set cookies, even in safari 1.0. Sites were able to make assumptions like I don't have cookies, I'll never have them in safari, or I have my cookies so I have unfettered use of cookies. So we enabled partioning of cookies in embedded frames they were able to set cookies. So they assumed those cookies would be available in a first party context or another third party context, and they weren't. If they cleared cookies.. the most common case was you visit a thing as a first party, you hit "clear my cookies", and then you go to a site where it's embedded, it gets an inconsistent state. Where it either sets a cookie in a 3p cookies that it expects to see in 1p but it doesn't so it breaks. First party and thid party things were inconsistent. code paths trying to make sense of this were basically a UA check. The compat concern is probably primarily safari's. It was bad enough we had to roll it out. I don't now if we have public list of sites that broke but it was not fun for a year.

Peter: seems this is delivering a mechanism where safari could say set this cookie but double key it. I understand this is only a double keyed cookie. Which seems like an improvement? becuase it alllows you to double key all your cookies if everyone is opting into this

Tess: if it's used in conjunction with some kind of user agreement then maybe that's the case. Without a user agreement, without consent, you can't set them at all. So it would be a regression, I think, from ..

peter: Safari tried to do something to tighten up cookies, double keyed them, that broke because sites were making assumptions, so blocked them entirely

Tess: which had less of a compat impact becuase sites assume dthey weren't getting cookies in safari

Peter: if you'd had this in the beginning this would have let you double key the cookies

Tess: only for sites that opt in and nobody would have opted in. No reason to at the time. 

Peter: wouldn't have opted in for you because they were still getting them everyone else.

Tess: yeah. If this was gated on the storage access api then it wouldn't be a regression. It would be an improvement. But if nit's not gated on storage access or a similar prompt its' a regression for us so it doesn't make sense.

Peter: anecdotal reports saying these sites will correlate you anyway so double keyig doesn't really help in the real world

Tess: IP address is a very high source of entropy

Peter: guessing there are other things they can do to correlate

Tess: fingerprinting, IP address..

Peter: consensus to invite someone to a call as best way forward?

Dan: yep

`Hi @DCtheTall. We have been talking about this in [today's TAG call](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/07-26-agenda.md). We're a bit concerned that this proposal is reinforcing or enabling a web feature that we might want to be deprecating in the first place?  We discussed some negative outcomes of data leakage to a 3rd party without user interaction / consent which are enabled by the current regime and which would continue to be enabled in a CHIPS world. We're also concerned about the roll-out plan. If partitioned and unpartitioned cookies are intended to be supported simultaneously for some period of time then that could enable 3rd parties to work around the privacy protections. Also we discussed how this could/should fit together with the storage access API. Could we bring one of you in to a TAG call at some point to discuss further?`

### [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro, @hadleybeeman

### [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman


## Breakout B

Present:

Regrets:


### [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov

### [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober

### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov


## Breakout C

Present: Dan, Amy, Hadley, Yves, Lea, Sangwhan

Regrets: 

### [Request for review: CSS tree-scoped at-rule names and references (for @font-face, @keyframes, etc.)](https://github.com/w3ctag/design-reviews/issues/659) - @torgo

Sangwhan: this is a [long discussion](https://github.com/w3c/csswg-drafts/issues/1995) for a small delta

Dan: but it is a reslolved change to CSS. Possibly not a small delta. Discuss at plenary where we have more CSS voices?

Sangwhan: don't think it's controversial..?

Dan: multi stakeholder? [leaves comment]

[punted to the plenary]

### ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon

Yves: looks good to me - would like to see in caches differentiation between what is retreived with and without credentials - eg. service worker and native cache of the browser. If everyone is happy with that, i can send that comment.

### [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov

Sangwhan: we wanted to ask for the delta between spec they are pushing and one in CR... We have no idea where to find the delta.  [leaves comment]

### [Shared Element Transitions - Early Review](https://github.com/w3ctag/design-reviews/issues/631) - @cynthia, @LeaVerou, @plinss

[some responses to Lea's comments](https://github.com/w3ctag/design-reviews/issues/631#issuecomment-856265760)

Lea: sounds like multipage transitions are ones this is useful for but not speced yet. Seems like it's an essential part of this API.. 

Dan: not clear from the feedback if they are going to refactor to layer based on existing APIs or not...?

Lea: i will take a closer look let's revisit at the plenary.

[punted to plenary]

### [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro, @hadleybeeman

Amy: they have a para in their spec and they want out opinion ...  They say "top level browsing context" and they may be refering to an SVG which isn't techically a top level browsing context so they want feedback. They have decided on behaviour, just want feedback on how to communicate it.

Yves: what is the origin when you navigate to a data URL? And do you use whether the document was sent using https to infer whether it can access powerful features, etc?

Dan: trying to figure out if the [WHATWG PR](https://github.com/whatwg/html/pull/5279) is consistent with what Ivan is asking about

Hadley: MDN [page](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs) says this already happens.  

Amy: it is consistent with what the epub spec is asking for...

Yves: their spec says must prevent data url from opening in a top level browsing context.  They say "browsing context" doesn't apply to SVG - only HTML.  Something something Transcluded references - resources that are automatically downloaded like images and style? 

Dan: could we just advise them to say "top level context"?  Should they specify it in their doc?

Amy: or they could just say "in this context SVG also counts" [when referring].

Dan: I think that would be sufficient.  But I'm not implementing epub readers...

Yves: should be secure contexts as well... there was [an issue about if data URL is a secure context](https://github.com/w3c/webappsec-secure-contexts/issues/69) and the resolution was no ... do they require secure contexts or not?  If they do then instead of using top level context you can say only for secure context documents - in that case it prevents Data URLs to be used.

Dan: let's leave those comments and maybe we can close it at the plenary if we get a response.

## Plenary Session

Present: Peter, Dan, Rossen, Sangwhan, Lea, Yves, Tess, Amy, Hadley

Regrets: 

### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

Dan: back and forth with Kaustuba.. should we get her on one of our calls to talk this through?

[general agreement - invite for second half hour of breakout A]

Peter: taking the minutes literally re: like button

Dan: they are really focussing on the 3p cookies thing. K's intention, if we are saying that a permission prompt should be required for a partitioned cookie, then we should also be requiring a permission prompt for partitioned js storage. Her view is that this isn't what safari is doing.

Tess: the website doesn't have to do something to get that storage

Dan: can you untangle that? I said we're talking about cookies, not js storage. Yes the requirements for prompting on js storage may need to be stronger if we want to push for a more privacy sensitive web. That is possible. However just becuase they're not as strong as we want them to be doesn't mean we shouldn't be trying to strengthen them on cookie based storage.

Tess: I'll try to catch up

Sangwhan: can you gate a http header behind a permission?

Tess: no. In this case what you'd have to do is [??] access to it after the fact in js. For other storage mechanisms where you can only get them from js it's because you might have serverside state that relies on them and the reason to need them at that earlier stage.. there's a number of things about cookies that make them weird compared to other clientside storage. That's how we ended up [??] in safari with permission by default and cookies are blocked by default

Dan: I'll reach out to K about breakout A

### [Request for review: CSS tree-scoped at-rule names and references (for @font-face, @keyframes, etc.)](https://github.com/w3ctag/design-reviews/issues/659) - @torgo

[is this a small delta?]

Lea: seems very reasonable to me, but not sure what the delta is.

Dan: I'm on it because Chris H pinged. If it is a small delta we want to move it quickly. But it looks like maybe it isn't a small delta. But not a CSS expert.

Tess: been a long time since I looked at this issue. 

Peter: seems reasonable to me.. I've relied on things with @font-face propagating down ..

Tess: it's the right direction.. shadow tree gets to know about its context

Peter: nothing leaks upwards

Tess: I think i'ts good. Can't remember specifics from the discussion which happened over several years. A ton of gotchas. This is probably how it should work.

Peter: I agree

Sangwhan: prsumably CSS variables have scoping

Lea: they inherit down shadow trees  - this was influenced by how variables behave.

Rossen: this looks pretty good

Peter: **close** this as satisfied?

Lea: I'm in favour of that. [writes closing comment]

Rossen: only thing I see - closing argument - don't recall we had resolution over email.  Not a showstopper just an FYI.  I have no evidence of an email resolution.

### [Shared Element Transitions - Early Review](https://github.com/w3ctag/design-reviews/issues/631)

(Punted from breakout C)

Lea: I asked if this could punted to plenary. I did take a closer look today.  It does seem like something that needs solving and there is a need for it.  But I am not quite sure how this proposed API is supposed to work.  Seems that the primary need is for MPAs which is not specified here. Not sure this can be designed without that.  Even the SPA case - there is a [code example in the explainer](). Not sure how this is suppsosed to work.

Rossen: on Tuesday during our [CSS]() call - what was the overall outcome?

Lea: in general they were positive. I posted a [link to Jake's talk](https://www.youtube.com/watch?v=UIWZFXwAPxE). which talks about the problem statement but not about the API. So the working group was positive. 

Tess: yes I think everyone understands the problem statement - the devil is in the details. 

Lea: The review does show an API sketch.

Tess: why isn't this going to the CSS working group?

Rossen: procedurally - I think this is a case where they are engageing in an early preview- we have encouraged that in the past.  This is the idea stage.  At that altitude this is a good review to have - to justify the use cases and technical path forward.  This feels like they are a bit more off-shore - they have already designed it and implemented - so this not an idea review.  In which case I would expect a technical proposal.

Tess: at the beginning they say similar to material design principles -- there are other things that come to mind - e.g. in IOS. What about powerpoint?  Transitions between slides... I would think they would look at slide to slide transitions in powerpoint and keynote...

Lea: The primary complexity is they are not just interested in transitions between pages - but also where specific elements in one page morph into specific elements in another page.

Tess: powerpoint (e.g.) does that.

Sangwhan: I don't see how the SPA version can evolve into an MPA version... based on the current design.  Agree with the problem statement though.

Peter: I get the MP issue - but with a SP what does this do you can't do with CSS transitions?

Lea: more high level - this takes care of things that are hard with CSS transitions.

Sangwhan: the MP thing sounds like a complex problem.

Rossen: intended to work between pages that know eachother?  

Lea: an open problem - an opt in where both pages could declare or maybe a limited set of transitions? 

Sangwhan: would have to have a preload feature if you want to support MP...

Peter: unless both pages opt in and collaborate you'd have to clamp down on transitions - otherwise security issues

### Breakout Rollup

#### Breakout A

Dan: private networks - I left a comment

Hadley: generally supportive but need to engage with ietf

Dan: http 103 early hints - closed

Yves: closed as something already implemented

Dan: html media element control list - punted to 2nd week in august. Distributed tracing WG baggage stuff - privacy concerns. Just talked about CHIPS. Co-op same origin allow popups - still open

Hadley: don't think we got to that, carried on with CHIPS

[tangent about chocolate chips]

#### Breakout B

n/a

#### Breakout C

Dan: Talked about CSS tree scoped thing. Credentiallless embedder policy - closed?

Yves: wanted to wait until plenary to close. I will have to comment on Artur's reply. I can comment and close.

Dan: performance timeline...

Sangwhan: pending external feedback

Dan: shared element transitions talked about. Restricting use of data URLs

Amy: said I'd comment, forgot, will do..

Dan: set for 2 weeks time

### Schedule for August

Dan away w/c 16
Hadley away w/c 9th and w/c 23rd
Rossen maybe away 2nd and 3rd weeks of august

Virtual f2f - sept 13-15
