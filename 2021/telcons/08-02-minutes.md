## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/08-02-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-08-02](https://www.timeanddate.com/worldclock/converter.html?iso=20210802T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Triage [Security & Privacy Questionnaire Issues](https://github.com/w3ctag/security-questionnaire/issues)
* S&P PR [Add non-"fully active" document question](https://github.com/w3ctag/security-questionnaire/pull/128)
* [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286) - @hober, @LeaVerou, @kenchris
* [APIs should allow introspection](https://github.com/w3ctag/design-principles/issues/300) - @LeaVerou
* [New principle: When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - @hober, @torgo
* [New principle: Guidance on User Activation](https://github.com/w3ctag/design-principles/issues/314) - @hober, @torgo, @rhiaro
* [CHIPS](https://github.com/w3ctag/design-reviews/issues/654) with special guest @krgovind (2nd half hour)


### Breakout B (US / APAC) - [2021-08-03](https://www.timeanddate.com/worldclock/converter.html?iso=20210803T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Whether or not the web inspector / dev tools are open should not be detectable by the webpage](https://github.com/w3ctag/design-principles/issues/209) - @hober
* [New principle: Web IDL is for APIs exposed to the web by browser engines](https://github.com/w3ctag/design-principles/issues/216) - @hober
* [New principle: New features must not break existing ones](https://github.com/w3ctag/design-principles/issues/297) - @hober, @atanassov
* [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)

### Breakout C (APAC / Europe) - [2021-08-03](https://www.timeanddate.com/worldclock/converter.html?iso=20210803T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Triage [Ethical Principles Issues](https://github.com/w3ctag/ethical-web-principles/issues)
* Ethical PR [Environmental sustainability](https://github.com/w3ctag/ethical-web-principles/pull/31)
* Ethical PR [Editorial: fixup links](https://github.com/w3ctag/ethical-web-principles/pull/43)
* [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou
* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @kenchris
* [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @torgo, @hadleybeeman
* [Principle against tying APIs too closely to hardware](https://github.com/w3ctag/design-principles/issues/308) - @cynthia
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281) - @hober, @LeaVerou


### Plenary Session - [2021-08-04](https://www.timeanddate.com/worldclock/converter.html?iso=20210804T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)



* Breakout Rollup
* Issue Triage


## Call Minutes


### Breakout A (Europe / US) - [2021-08-02](https://www.timeanddate.com/worldclock/converter.html?iso=20210802T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Peter, Lea, Ken, Rossen, Tess, Amy, Hadley

Regrets: Yves

#### Triage [Security & Privacy Questionnaire Issues](https://github.com/w3ctag/security-questionnaire/issues)

#### S&P PR [Add non-"fully active" document question](https://github.com/w3ctag/security-questionnaire/pull/128)

Tess: [PR for this on design principles too](https://github.com/w3ctag/design-principles/pull/317) - should merge both or neither

[reviewing 317]...

Tess: an [argument about syntax](https://github.com/w3ctag/design-principles/pull/317/files#r651522960) ... 

Dan: this is not substantive.. 

Tess: we know the TR isn't stale in this case because of semi automatic publication

Dan: overrule and go with marcos

[we agree to drop the two lines]

Peter: it's really a tooling issue. 

Dan: [postpone decision on merging to the plenary]

#### [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281) - @hober, @LeaVerou

Looking at [PR](https://github.com/w3ctag/design-principles/pull/326)

Lea: should we include SVG and other MLs?

Tess: it should be about HTML - if there are principles common to other MLs that we need to talk about we can do that.

Dan: Agree.

Dan: positive review.

Ken: me too.

Tess: merge.

Peter: guidance on the opposite?  Existing attribute with same name?  

Ken: yes - behaviour should be similar.

Tess: not incredibly clear line... example: open dialog.open has weirder behavior than details.open - same name but behaviour wise it's different. It's about unexpectedness. If the auhthor is used to using it in one way one place...

Lea: An example from a design review?

Peter: let's land this but then do a separate PR.

Lea: we could generalize the title to "same attribute names for similar things" and... That could be a separate PR.

Dan: agreed let's merge... and create a new issue.

#### [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286) - @hober, @LeaVerou, @kenchris

#### [New principle: When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - @hober, @torgo

#### [New principle: Guidance on User Activation](https://github.com/w3ctag/design-principles/issues/314) - @hober, @torgo, @rhiaro

#### [CHIPS](https://github.com/w3ctag/design-reviews/issues/654) with special guest @krgovind (2nd half hour)

Present+ Kaustubha

Dan: back and forth around the user needs.. And we wanted to delve into.. we were talking about a higher level of informed consent for that kind of information sharing. We posted about the scenario that happened with the NHS putting facebook like buttons on their pages which unintentionally leaked information to facebook which could have been damaging to users which could have shown up in ads or been leaked to insurers. The question came up are there other mechanisms where third parties might be able to do this anyway so does adding an additional consent step make sense. We had back and forth about cookies vs js storage. Does it make sense to add a consent req on cookies if it's already available without consent through js storage? That's the essence. We're trying to look at it from a user needs and ethical principles perspective and moving the web in general in a more privacy focussed way has been one of the things the TAG has been looking at. It is our role to ask these questions and say if the web is doing this thing should there be some additional consent barrier. If this capability is available with js storage in some browsers - maybe it shouldn't be. That doesn't necessarily mean we should link those two issues. 

Kaustubha: the uses targeted with this proposal - in the explainer we talk about resource CDNs often will serve subresources on sites. CDNs like to use cookies for load balancing, it's available in the http request and they'll read a hash of the cookie for matching it to a server and the user ends up on the same server. The other use case is SAAS embeds. You have store locator widgets. The only service some businesses provide is store locator widgets. They don't need full unpartitioned 3p cookies (unpartitioned cookies, third parties get the same cookie no matter what top level site they're embedded on). The web is composable, a lot of sites delegate services to third parties. A business doesn't have to have everything, it is okay to outsource pieces of the experience. Eg. chat embeds and maps. Those are the ones where they don't intend to track across top level sites, just need some notion of session state, and fine with partitioned state. More the SAAS and CDN use cases we're targeting here.

... Wrt to the facebook like button, that's a harm I studied a year or so ago. Yes 3p cookies make that possible, but an easier thing to fix at the time was change the default referrer policy where you cap the referrer. In every subresource request there's a referrer header. It used to be a full url by default. Then on the NHS site the symptoms or diseseas would be part of the full URL. That was the intention of that change - the 3p shouldn't get access to this. THe top level site can opt in to send the full URL. We talked at the time should we cap the referrer so in no situation can a cross site embed get access. There might be a discussion going on in privacy cg about this..


Tess: there is

Kaustubha: ruling out the default change wa shelpful from chrome's perspective becuase we learned about use cases that used it. In github you have the heroku run button - they look at the repo path and it navigates you to heroku and knows what repo to run the action on. There are payment merchants that look at the path and do anti fraud checks. SO for now we have to set the referrer policy and have the merchant top leve lsite opt in to send the full referrer header. Just to explain there are other mechanisms to improve privacy - the NHS case would have been avoided today becaues the NHS would have had to opt in to send the full referrer.

... The other thing was the permissions prompt. When we think about state in the browser there's js storage, cookies, and also httpcache - there are ways for devs to leverage httpcache as storage. It could be a couple of bits at a time, but there are ways. Generally we've been thinking of partitioning everything by the top level site. THat is what prevents the cross site tracking risk. When we created the issue we felt like the other browsers were aligned. Firefox rolled out this totall cookie protection enabled in private browsing and everything is partitioned by default, no permission prompts. Safari's storage is partitioned by default and John had an issue on the reuqest storage access repo about adding an optional param where without permission the site could request partitioned cookies - could be opt in becuase safari saw breakage with partitioned cookies by default, but not sure.

... From chrome's perspective we think we should have an opt in, that's why were proposing the attribute. 3p cookies today are used for different things. We're introducing different apis. In the ad space a big use case is conversion measurements or click attributions. In that case if we simply partition developers won't even know something broke becuase they're just seeing the cookie for that partition. Federated auth is the other one, IDPs typically use 3p cookieis, what they want is unpartitioned cookies. If we were to partition all 3p cookies by default here would be these silent failures. We're hoping to force a path of you need to opt into these new apis or partitioning so you can prepare your system sfor when chrome wants to deprecate

Tess: with safari we saw two classes of breakage - one you mentioned where they were safari specific code paths that assumed the original safari cookie policy that weren't ready to get cookies at all, and assumed they were in another browser and broke. The second is sites that would set a cookie in a partitioned state and then try to clear it as a first party. You'd visit it later and they'd cleared tehir cookies, then get into an inconsistent state where they are a third party again and see a stale cookie because they weren't clearing in a partitioned state. Some are specific to safari becuase of the historical cookie policy, some are endemic to the case at large

Kaustubha: the clear site data is an important one. If the site invokes clear site data in the partition we want to make sure we only clear the partition otherwise it's a side channel. That's another reason developers should opt in so they are aware when we call clear site data it's happening in apartition

... going back to permissions - does this need to be gated behind a permission prompt? And what is the actual syntax? Firefox is doing the partitioning by default. I think safari is nterested in opt in. Our preference is a cookie attribute becuase we don't want to force people to load js to get access to http cookies. If you have cookiies marked http only it's going to add roundtrips so we thought having a cookie attribute might be easier, everyone just deals with the set cookie header. 

Dan: a cognitive dissonacne for me is a discussion of "opt-in" - in my mindset it's the user opting in and when we're talking about opt in in this and other contexts it's about the top level site opting in. I also feel like the permissions when they exist should be understandable by the end user. SO when yo'ure talking about data potentially privacy infringing data being shared with a 3p that is something that should be gated potentially behind a permission, but some of the use cases like CDNs that is something entirely in the realm of how the service is architected in the backend, it doesn't have to do with the flow of information or privacy infringing information. I'm trying to think about this from the end user perspective.

... And question about multi browser / multi engine consensus. What's mozilla's view, what's the webkit view? We don't want to see further fragmentation when it comes to cookies, any privacy related web technologies. Fragmentation can result in worse situation for user privacy becuase developers make certain assumptions that match all browsers, or different code paths for different browsers.

Kaustubha: from a survey of things that use cross site cookies, i'd wager most could use partitioned cookies. Advertisers, federated login, payments, are use cases that need unpartitioned cookies. I suspect a majority could do with partitioned cookies. So nice to have a good cross browser story for partitioned stuff.

Dan: is there something we are asking the user permission for that makes sense to them? What does the permission and user flow look like in a world where this is gated behind a permission vs not gated behind a permission?

Kaustubha: I'm trying to understand the privacy leak wrt the permission. We think of unpartitioned state as what enables that cross site privacy leak. With partitioned cookies all facebook knows is that there is a user visiting the NHS site, top level url, but can't correlate that with their logged in state on facebook. For that they would need access to unpartitioned cookies. On safari those are gated behind request access api. Something like webid also has some kind of permission. If we think there is a risk of that cross site joining that warrants a permission. Is that what the TAG is thinking? What is the threat we're worried about here wrt user privacy?

Dan: that is the kind of threat. I don't know that th emitigate you described of making the referrer only top level is necessarily... I need to udnerstand if tha tfully mitigates the risk

Tess: it doesnt' fully but does partially. In the NHS example it does prevent the 3p from learning the specific medical conditions. But for others simply the origin is enoguh to share information about the user

Kaustubha: there are two mitigatiosn we are talking about. The referrer as well as the fact this is partitioned cookies only, and no unpartitioned cookie access

Tess: do you envision there being a period of time in which chrome would simultaneously support unpartitioned 3p cookies and opt-in partition 3p cookies at the same time?

Kaustubha: yeah, we want to make sure sites have enough tiem to migrate

Tess: so sites that are migrating can simultaneously get their unpartitione duser id and set a partitioned user id cookie and set themselves up in the future for when 3p cookies are turned off

Kaustubha: we're thinking about that... what if we do a one time clearing of all 3p state? partitioned and unpartitioned at the time that chrome rolls out 3p cookie blocking

Tess: are you willing to take the user hit of logging everyone out from everywhere and having everyone think chrome is broken?

Kaustubha: losing third party cookies is going to be pretty disruptive anyway. the one loop hole is that a lot of including ad tech companies have script embedded on top leve lsite, so access ot the top level site cookie jar. What's to preven tthem from doing the same there? We clear out all state including first party? I'm unclear. I was considering putting in a section for that, but wanted to think about how to prevent that. A one time clearing of all third party state is what i had in mind. Not perfect but dissuades people form trying to do stuff like that.

Tess: Relatedly there's also link decoration protection might have to come along with that in the same time frame for the same reason. The script embedded in the firs tparty that creates the iframe can pass informaation with link decoration as well as other means. Any plans there? 

Kaustubha: we're thinking about it. And talked in privacy cg. There are a whole ton of use cases, federated auth, payments, does it mean cross site POSTs should go away? It's a wide range of things, we're going to have those discussions.

Dan: you're on a website where being on the website tells the third party a lot about you. Is that something that dserves to be behind a prompt? Is it okay for diquss.com (if we're talking about embedded chat) to know that you're on a website that may be sensitive. what other additional mitigations could we imagine to mitigate against that data leakage against the users expectations? or is there another thing in the proposal which wouldn't allow for that in the first place?

Kaustubha: are you thinking more about an ad script embedded on the sensitive site?

Dan: could be a chat widget or maps or location finder or any kind of third party content

Kaustubha: if you're not signed into to disquss and they don't know who you are would you still consider.. all they kno at this point is there is a user and they are visiting that site, they don't know you your email, or that you're the same user who visited sensitivesite2.com. In a world where you only have partitioned state by default, and no unpartitoined cookies, that cross site correlation isn't possible any more. If you signed in or gave storage access then they could do that if they wanted to. But that is going to be gated behind some kind of permisson. Is it sufficient that we have a permission gated to when that site requests access to unpartitioned? but as long as they can't do that sort of cross site correlation, only have partitioned state, is it fine to give them without user permission?

Dan: we are talking about the right issues here. How do we take this forward?

Tess: we should continue this conversation

Dan: schedule a special session

Kaustubha: if you have specific questions in the meantime I can help answer them.

Dan: I feel like we're talking about problems difficult to talk about, or using terminology differently... there's value to trying to write down some of these scenarios eg. where third party content is embedded in a website where we understand what privacy infriging data might flow to that third party, and how the CHIPS proposal mitigates against that kind of harm or whether it does or whether it needs to. i feel like that's missing from the current explainer. Maybe we could work on that together.

Kaustubha: yeah. And the privacy threat model - chrome  had put out a privacy threat model. Partitioned identity is okay, as soon as you have identity travelling across parititons we need guard rails in place. This is based on that principle. If there is a paralell discussion going on that might be a good place ot have it in the task force

Dan: maybe there's an issue that could be raised in that repo. 

### Breakout B (US / APAC) - [2021-08-03](https://www.timeanddate.com/worldclock/converter.html?iso=20210803T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Peter, Rossen

Regrets: Sangwhan

#### [Whether or not the web inspector / dev tools are open should not be detectable by the webpage](https://github.com/w3ctag/design-principles/issues/209) - @hober
Peter: This is just a write me. Let's do it offline.

#### [New principle: Web IDL is for APIs exposed to the web by browser engines](https://github.com/w3ctag/design-principles/issues/216) - @hober
Peter: This is just a write me. Let's do it offline.

#### [New principle: New features must not break existing ones](https://github.com/w3ctag/design-principles/issues/297) - @hober, @atanassov
Peter: This is just a write me. Let's do it offline.

#### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)

#### [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)
(Peter and Rossen read the issue and linked discussions)

Peter: The main point being raised is do we enable any API to Workers only and if so, to what benefit? It seems like the best argument being made for this is to teach people to use Workers, as a mechanism to offload work off the main thread.
... At the same time, if they just expose these as async functions you should get the same performance benefit.

Rossen: To that end, spinning up a Worker comes at a much greater cost than simply making an async call off the main. 
... One benefit of Workers we can argue is having a bit stronger security sandbox where execution takes place. That being said, in the case of WebCodecs I'm not sure that holds true since we're not considering exposing lower OS API for decoding itself.

Peter: one argument for exposing on Window is feature detection from the main thread. If there's a compelling reason for functionality to be worker only, the feature should still exist on Window, maybe just not function there. e.g. A constructor exists, but throws if not called from a worker.

Rossen: Agree completely. Feature detection is a must and should be part of any API.

Peter: The consensus we're arriving at is to have a very high bar about having something in Worker only, small performance gains are not enough, security features might be. At the very least, the API must be available on Window for feature detection.
... Similarly, we need guidance about what API must never be part of Workers - functionality that depends on Document, Window and Screen are obvious cases when the API must not be part of a Worker.



### Breakout C (APAC / Europe) - [2021-08-03](https://www.timeanddate.com/worldclock/converter.html?iso=20210803T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Ken, Amy, Hadley, Lea

Regrets: Yves

#### CHIPS

[recap discussion from breakout A]

Amy: rollout plan with unpartitioned and partitioned at the same time is still a concern.. what does that look like for users, especially cross browser? Very chrome focussed solution. Also cross browser story in general..

Ken: explainer gets very technical very quick.. would be better to outline other browser solutions, point out issues, and then explain why this proposal

Hadley: NHS/facebook scenario - response about referrers but not cookies..?

Dan: leaving comment; i will have further discussions with Kaustubha.

#### Triage [Ethical Principles Issues](https://github.com/w3ctag/ethical-web-principles/issues)

...we worked on triaging issues and we merged [links from design principles to ethics doc](https://github.com/w3ctag/design-principles/pull/327)

#### [The role of the user agent, to serve the user first](https://github.com/w3ctag/ethical-web-principles/issues/38)

Hadley: we need to call out that users come before advertisers.  [PR32 clarifying priority of constituencies](https://github.com/w3ctag/ethical-web-principles/pull/32). 

Dan: I think it addressed issue, maybe we can close

Hadley: agreed

#### [The danger of prioritising algorithmic relevance over human needs](https://github.com/w3ctag/ethical-web-principles/issues/42)

Hadley: from a breakout discussion

Dan: huge problem.. is it a problem with the web?

Hadley: these are web services. Needs in depth discussion.

Dan: keep it open.. I can have a go at writing something

Amy: another one that is implicit throughout several principles... eg. web is for all people. Maybe worth calling out explicitly as a bad thing

#### [Say something about resisting interpersonal abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)

Dan: agree

Hadley: me too, might be multiple issues. When we talk about surveillence it's easy to broaden beyond govts and cover other parts of the network. Employers, ISPs etc. Parents and children might be a separate issue.. really hard to draw that line. Partners spying on each other or abusing the fact one controls the network is definitely a problem. SOmething we design when we think about the fact my machine can see other things on my home network. That's why encryption is good. Can try to write something.

Dan: could be incorporated into existing principles. Clarification.

#### Ethical PR [Environmental sustainability](https://github.com/w3ctag/ethical-web-principles/pull/31)

Amy: on my list

#### Ethical PR [Editorial: fixup links](https://github.com/w3ctag/ethical-web-principles/pull/43)

MERGED

#### [Dark patterns](https://github.com/w3ctag/ethical-web-principles/issues/25)

Hadley: spawned issues in design principles and s&p questionnaire

Dan: we agreed not to have a principle on this in EWP...  it's implicit in the whole document not to enablel dark pattern

Hadley: would it help if we mentioned them explicitly?

Dan: in intro. Comment from mnot - not sure I agree enhancing control and power does conflate things with centralisation

Amy: not doing dark patterns and not doing centralisation are both things that enhance individuals control and power. A more specific subset. Agree that EWP is more high level than mentioning specific dark patterns - makes sense to offer guidence in s&p and design principles instead - but we could mention dark patterns somewhere in EWP as one of the various things that are relevant. I can do that.

Dan: [leaves comment]

#### [PR Link to ethical web from design principles](https://github.com/w3ctag/design-principles/pull/327)

Dan & Amy: [live suggestion mode]

Hadley: looks great

[merged]

Agree to close corresponding issue #282 on design principles

#### [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou

#### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @kenchris



#### [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @torgo, @hadleybeeman

#### [Principle against tying APIs too closely to hardware](https://github.com/w3ctag/design-principles/issues/308) - @cynthia



### Plenary Session - [2021-08-04](https://www.timeanddate.com/worldclock/converter.html?iso=20210804T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Peter, Dan, Amy, Kenneth, Lea, Rossen

Regrets: Tess, Sangwhan

#### Breakout Rollup

Dan : A- Chips... the none fully active document stuff... some things we didn't talk about... Back to CHIPS... asked for more clarity on defining partitioned and unpartitioned and also being specific about what opt in means and why that's important for end user privacy. Still feels disconnected to me. Ken also wrote a comment. Waiting for response.

Peter: B - bunch of the issues in write-me state.  We talked about exposing features - only [exposing in workers](https://github.com/w3ctag/design-principles/issues/325)  - trying to get people to use workers.  We're not sure there's a benefit to doing that.  The only real benefit you get is more security isolation - no performance benefit. Also it breaks feature detection if not available on `Window`. The guideance should be not to expose something just on Worker, but you could expose a feature on `Window` and make it non-functional. But should be a high bar - just encouraging use of workers isn't good enough.  Thing we didn't get a feel on is - is there a good reason to not expose things to worker.  There is stuff not exposed to workers that probably should be.  E.g. legacy.

Ken: e.g. webusb is exposed to workers but you have dialogs that pop up like prompts selecting devices - you don't want it popping up out of context.

Peter: makes sense for some things to not be in the worker - but why can't i construct dom nodes in a worker?  We don't have strong consensus on this point.  

Dan: enough consensus to write text?

Ken: sounds good to me

Peter: wanted to get agreement from the rest of the TAG on general principles, not to expose based on worker only

Dan: agree with this philosophy that we shouldn't just be exposing things on worker to try to encourage the use of workers, it's not an intrinsically good thing. Workers are great, but..

Peter: they have their uses

Dan: Breakout C - CHIPS again.. did some work on ethical principals. Landed some PRs in EWP and on Design Principles that was links to the EWP. Editorial / non-substantive. Talked about dark patterns - probably don't want to have a separate ethical principle abut it but we should mention it in the intro, Amy's going to write some text. Likewise on environmental sustainability. Hadley is going to write something on resisting interpersonal abuse from jyasskin. Closed something about the priority of constituency, had been addressed. 
 
#### [APIs should allow introspection](https://github.com/w3ctag/design-principles/issues/300) - @LeaVerou

Lea: I opened. Tension between usability and in some ways privacy. We need to figure out how to phrase it so if we do want to adopt a principle on this so that APIs allow introspection only in cases where it doesn't pose a security and privacy risk. I think when we discussed before that was the main concern. How do we word this? So we don't push API designers to allowing mor efingerprinting by exposing more info. If we can figure out a way to do this properly I think it's important because it does increase usability of apis if you can inspect their state and information that the browser has instead of predefining it yourself.

Dan: issue would be how unique is that set of information? Things like the list of fonts available has been highlighted very often as something used for fingerprinting. If there are similar sets of information that the browser has access to that create a unique fingerprint that should be something not exposed, but only puts you in a set of .. depends on how big a set

Lea: fonts are different, system information not api information. The kind of info i was thinking of was either information that can be deduced from browser version and locale - already there - or information about the state of particular objects, like for example a case I ran into yesterday - a mutation observer object doesn't expose anything. You can't read it's callback or its options object. No way to create another object based on it or to figure out what it does or anything, it's just a black box. Not sure if that's intentional or nobody thought of adding these properties. A few examples in the first post of the issue as well.

Dan: is it enough to say what you said about as long as it doesn't aid fingerprinting. Are there counterexamples of things that should not be exposed becuase they're going to be used by scammers and bots (oh my)?

Lea: counterexamples listed so far are system information, not to do with API. Ken mentioned available cameras which is different. List of fonts is also not part of an api. 

Dan: I think we need a counterexample in the text which is something that wouldn't make sense to expose, if we're going to say apis should allow introspection except for information that would infringe privacy

Lea: beyond security and privacy do we have consensus it's a good idea?

Dan: what are the performance characteristics? Are there downsides to allowing introspection? Does it create bloat or additional complexity?

Ken: I don't think it's a performance issue. But it's more code in the engine so of course some overhead

Lea: any overhead beyond the overhead of any code being written?

Ken: I don't think so

Dan: just trying to think of any issues. Sounds reasonable to me. Trying to think from a browser developer perspective. Does it increase the overall footprint of the browser itself? Memory usage?

Ken: like any api it needs to be standardised and implemented... but if you're not using the api it's probably ver minimal overhead. Same for dev tools - adding introspection. It's the same engine work.

Lea: would also make it easier for dev tools

Ken: probably yeah

Lea: we should consider the footprint not jusut of the api surface but also the footprint of all these developers reimplementing these things or including thing sin their code that the browser already has. If almost every website is linking to something that has a list o fmonths in a certain locale even though the browser already has this information there is a footprint there as well

Peter: I've advocated for exposing that kind of information, timezones, calendar. Aside from fingerprinting concerns is generally not controversial

Peter's cat: begs to differ

Dan: sounds like we have consensus that it's a good thing

Lea: I think consensus is it's a good idea as long as it doesn't raise fingerprinting concerns / add fingerprinting vectors

Rossen: is this for dev tools alone or in general?

Lea: also author code. Any tool designed to work on code. In-browser editors.

Rossen: is this a sign of missing an incomplete api?

Lea: you could say so.. the whole principle is about making sure that apis include some way of getting this kind of information that the browser has and authors also need access to

Rossen: in the case of dev tools you do have pretty different code path that data is being aggregated and provided so that you can have things like history and actual view of how a particular value was inherited and where it came from. This is very compute intensive information that is stored only on demand. SOmetimes we rerun processes in order to provide that information. To say that i have element A that had a property B with a value C and I want to know where C came from as a developer..

Lea: I don't think that applies

Rossen: you can do that through dev tools. What am I missing?

Lea: so far the issue is about exposing certain types of data, not history or stack traces.

Rossen: the type of data that you might sometime sneed to expose could be very heavily dependant on the context in which you computed it. A lot of time for optimisation purposes contexts are being rehashed, reused, dropped, in order to move forward quickly. If you require to expose a functionality right then and there you will start requiring all that context to be recomputed. sometimes that would mean gooing back quite a bit

Lea: I'm hearin gin additional to fingerprinting we should add a disclaimer that something like this needs to be performantly implemented

Rossen: is this principle supposed to attract implementors or have them ignore it..?

Lea: I'm trying to avoid apis hiding information fo rno good reason just because nobody thought of exposing information

Rossen: i would agree, that's why we have all the reviews that an api goes through.. 

Lea: can't htis point be made for any principle?

PeteR: the point of the principle is to inform the reviews, and to inform the editors before we get to review, what we expect

Rossen: agree..

Ken: you can also add something later but removing something is difficult. Don't want people adding things for completeness sake. Wait for cases come up that really need it for debugability, then add it

Peter: not always about debugability. The point was raised that it may help enable a developer experience, more about giving authors the exposure to things that they may need that the browser has. That's what Houdini is for. Not runtime information, API surface. This isn't about exposing everything to everyone. This principle is about introspection of API surface

Rossen: that's fair. Sounds like let's expose everything ot everyone but let's see what the wording looks like

Peter: no, more about just making the api surface introspectable. Lea has a bunch of examples in the issue.

Ken: that's true, you can't iterate events

Peter: or find out what events a DOM node could fire. Finding all the element types.

Ken: a lot os in dev toosl though

Peter: Why shouldn't it be available to author? Calendar and timezone info

Lea: Currency

Dan: I see it. Lea is going to write some text? We'll discuss the text

Lea: okay

Rossen: sounds great. The examples here are all great. The seem to me to fall closer to missing functionality rather than introspection. Difficult to straddle that line.

Lea: devil is in the details. A negative example would be very useful

Ken: listing all of the events could be expensive. If it is too expensive it would be abused, apps become slower. Issue with other languages like Java and C++. People turn off runtime time information because it slows down everything. That would be the fear, that you expose useful functionality and it's in frameworks and libraries and will slow things down.

Dan: [notes that in issue]


#### [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou

Lea: I think that makes sense. Not sure about webidl implications, but as api design advice it's really good

Dan: been sitting here since 2014

Lea: nice if people mention examples they have in mind... comments like classes defined with just functions or just data.. which ones?

Dan: Sanghwan added writeme asap on 13th May but to my knowledge nothing has been written yet. Is this something you could add Lea? Someone can help?

Lea: good api design advice but a webidl tangent that I'm not following. Maybe someone more versed in webidl?

Peter: happy to advise.. Don't think webidl is the key point. My understanding is just using webidl terminology to define dictionaries namespaces vs a webidl interface.. 

Dan: we could write something, we could drop it.. 

Lea: let's write something.

Dan: sounds fairly small.. Would like to know what Sangwhan's thoughts are

Lea: recall we added the writeme asap label during our breakout.. 

Peter: Sangwhan also self-assigned the issue.. him volunteering to write this?

Lea: principle is not about webidl.. don't want to have to add webidl for every js principle

Peter: agree, better using plain terminology and note eg. "in webidl use a dictionary"

Lea: I'm fine taking it up but don't know when that will be

Rossen: I can help

#### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @kenchris

#### [New design principle: Consistency](https://github.com/w3ctag/design-principles/issues/285) - @LeaVerou, @torgo, @hadleybeeman

Dan: consistency is mentioned in naming 

Lea: we had a PR.. what happened? It's not linked.

Peter: was PR 313 but apparently got merged but didn't do everything, needs additional examples

Dan: considering workload and issues maybe we should just close it? Not high priority?

Lea: fine with that

Peter: yep

Dan: [does so]. Only open a new issue if we get feedback that it's unclear.

#### [Principle against tying APIs too closely to hardware](https://github.com/w3ctag/design-principles/issues/308) - @cynthia



#### Issue Triage
