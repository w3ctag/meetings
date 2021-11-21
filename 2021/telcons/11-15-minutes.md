# TAG Minutes - week-of 15 November 2021

## Call Agenda

### Breakout A (Europe / US) - [2021-11-15](https://www.timeanddate.com/worldclock/converter.html?iso=20211115T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

NB: Guests will join us for first party sets discussion which will start at the halfway mark.

* [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @torgo, @hadleybeeman, @atanassov
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov
* [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @kenchris, @hadleybeeman

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

### Breakout B (US / APAC) - [2021-11-16](https://www.timeanddate.com/worldclock/converter.html?iso=20211116T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [WebTransport review request](https://github.com/w3ctag/design-reviews/issues/669) - @plinss, @atanassov

### Breakout C (APAC / Europe) - [2021-11-16](https://www.timeanddate.com/worldclock/converter.html?iso=20211116T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @torgo, @kenchris
* DIDs - should/can the TAG formulate a response to the formal objections or the issues raised in the formal objections?

### Plenary Session - [2021-11-17](https://www.timeanddate.com/worldclock/converter.html?iso=20211117T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

### Logistics

Chair: Dan

Scribe:

Bridge: https://whereby.com/w3ctag first then going to https://meet.jit.si/w3ctag as a back-up

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/11-15-minutes.md

Raw minutes: ...

## Call Minutes

### Breakout A 

Present: Dan, Ken, Amy, Peter, Yves, Hadley, Rossen
Guests: Kaustubha Govind, Harneet Sidhana

Regrets: Lea

NB: Guests will join us for first party sets discussion which will start at the halfway mark.

#### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @torgo, @hadleybeeman, @atanassov

Dan: waiting for response to questions

Amy: explainer has an update

Dan: close at plenary?

#### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

Ken: people are already doing this today, about sending metadata with your distributed tracing. As I understand the resposne to Hadley, clearly people are implementing custom headers which makes it harder to control, so they expect switching to this unified approach which is better from compatibility. Yyou can already do this today, so this is about standardising how people are doing it, sending this custom data, so that it will work across different libraries. That sounds like the right thing to do. This is not allowing anything new. Was wondering how this ties together with structured headers.

Dan: looks like they are being quite responsive. If this is just a way to standardise a thing people are doing already and there is some consensus around it it doesn't feel like it opens privacy issues. But is it a good design?

Ken: structured headers allows structured data, not just key value pairs and properties. [writes comment]

Ken: subset of structured headers? Make sure it's an actual subset and doesn't have confusing additional features

Peter: we have guidence in design principles about structured headers

Yves: that would be good

Peter: don't want to see yet another header form that requires another parser

Yves: or even worse, intermediaries, like what happened for cookies in the past

Dan: also missing info on multistakeholder support

Hadley: Why is it called baggage and not tracing id?

Ken: this is an extension tracing api?

Dan: language idiom issue?

Hadley: yes. Makes it harder to understand

Dan: is there anything in the responses that should be in the explainer?

Hadley: didn't get the use case until I went to the charter. Makes sense to standardise what they're already doing in other ways. Standardising a few different headers, of which baggage is the 'everything else' header. Still not convinced or understanding how this can't be hijacked for stronger user tracking. Am I missing something?

Ken: not worse than it is today. Going to standardise how you store the data, not what data you store. If people start using the same data you could use it for additional tracking, but you could always use it today with the telemetry thing. If it becomes standardised you might learn what something means you could use as additional entropy. But it's the same as today, if specific data is common, that would be the same case. Maybe slightly more entropy... if they continue today people are not collaborating well, but something becomes common enough that it's a de-facto standard. With the new thing if people just use their own data it's not going to give you more but if they use the same... it's the same.. not going to give you more entropy. Not standardising the values, just the format to store values, that's not very useful. You oculd argue there's a larger chance of de facto values and key pairs on top that could be used

Hadley: if it's standardised is it more useful to intercept?

Ken: already part of the telemetry thing.. this is just the custom data part. The non custom data part is much more valuable for tracking purposes.

Hadley: right, rather than just the baggage part. Not sure what that means we should do.

Dan: should it behave differently in private browsing?

Hadley: that's tricky. Depends on what you want to do in private browsing. You might want this kind of functionality to work. Whether it gets disrupted or cleared.. doesn't the spec say when you reload the page you get a new id?

Peter: id is provided by the service, the browser doesn't have control of that. Nothing stopping the service generating the same trace id or something they could deanonymise

Hadley: or with your IP address or somethign else identifiable or consistent

Peter: means private browser has no recourse than dropping the trace id entirely and not sending any telemetry

#### [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @kenchris, @hadleybeeman



#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

Dan: From the perspective of the TAG review issue, Amy left some comments, and I've been rereading our original review, and trying to understand where we've got to. Maybe you could give us an update on where you are, especially wrt the governance part of it, and any other updates?

Kaustubha: It's a hard problem from the policy and application aspects. Use cases for a single org creating disjoint sets - I can't say anybody has come to use with use cases asking for that. It's the answer I've given to folks who say if there's a size limit on a set, I have 300 domains which seems too large to me for a fps. I say I get there are 300 domains but do all of them have a common user flow through them? They might own a fastfood business and also an insurance business. THe user probably doesn't think of them as being thes ame thing, so there's no reason for them to be in the same fps. You don't have to think of every single one of yoru domains in the same set.

Dan: is that wording about user journesy centered in the... how do you define.. how do you ensure that the sets are being used for user journeys? I guess that is a core issue that we're wrestling with. User journeys as opposed to backchannel data journeys

Kaustubha: the original intent was to support these common user journeys, whether its consent management or login, use cases in the explainer. if you look at the policy document, we talk about common user journeys being one of the things we considered as a policy requirement and eliminated it. I've brought this up in privacy cg, if folks could think of a way to enforce it we'd be happy to reconsider. The challenge when we were analysing this in google was unless you had someone auditing all of your server code for the same journey it's harder to do that. It's a recommendation to the site owner rather than a requirement. Only form a first party set where you need to create this common user journey across these domains.

Amy: wrapping my head around org having disjoint sets but still sharing data that's come through both of those sets internally.  

Kaustubha: when we talk generally about 3p cookies or any interventions, we assume sites are using clinetside state to share data across those domains, they don't have to use clientside, they could do backend joins on the server. I'd say that's out of scope for fps. We're specifically talkinga bout what clientside mechanisms or state you could have to share across those domains and how we can organise that and restrict that.

Harneet: about making it hard for us to technically implement the user journey aspect. We're using disconnect on Edge and we have the same cncept of an org having multiple different site and the ability to audit what sites belong to which org and identifying org boundaries.. not having an easy technical way of establishing user journey across different sites.

Kaustubha: disconnect is also the list firefox uses. The UI surface and normative language - I've been talking to colleagues in chrome as well, the sentiment I've heard was that because we want to allow uas to have the means to innovate on UI,  having normative text around you must show this in a UI surface - an eg. is in chrome efor instance the origin info bubble or page info bubble is what pops up when you click on the lock for https, but perhaps there's a browser vendor that odesn't have that. the UI is important for FPS because that's the primary means the user agent can convey to the user that sites are related, in a world where other clientside mechanisms don't exist like 3p cookies. Where you can have the expectation that no two sites can share data without your permission, in that world, .. what I'm thinking is use SHOULD language to say user agents should inform users about how sites in the same fps have access to cross site data, instead of saying MUST use page info bubble to communicate the entire list of domains and MUST have a link to the privacy policy. Also wanted to ask how your thinking about normative language about UI generally in specs. And also the point of testing, in web platform tests there are no automated UI tests, but wanted to see if that's what you meant by testing.

Amy: I mean in terms of testing comnformance to the spec - so if you have SHOULD then how do you test?

Kaustubha: I think it's gonna have to be a manual test... Get current position ... all it say. Need to do some homework. A test that describes the goals rather than where the UI is placed...

Amy: Yeah from my perspective it's not about what the UI looks like (also because of non-visual UIs). Important to get it into the spec.

Kaustubha: The third issue [about corporate structures]... Amy you refered to [UA policy document](https://github.com/privacycg/first-party-sets/blob/main/ua_policy_proposal.md) .. we have 4 diff bullet points - when there is an independent enforcement entity they will do work to enforce thos. When it comes to the actual enforcement we will need to talk to folks like Disconnect.me - to operationalize enforcement.  We were trying to navigate that balance... listed 4 different options - how to bubble up group identity to users.  Parent company just one of them. Co-branding slighlty different.  We use parent company loosely... intent to 

Dan: feedback rooted in discussion of the ways that different countries think about corporate structures that may or may not relate to data ownership. I have a concern about how it works across borders. How does this work in a country where there are frosty relationships with say the enforcement agency is a US nonprofit - what if now I as an Iranian media company want to use fps? There are laws in the US that forbid US orgs fromw working with Iranian orgs. This came up a couple of years ago because there were people of IRanian background and Slack was banning their accounts because they seemed to have been connecting to Slack from Iranian IP addresses when they were Iranian expats possibly in the UK who happened t have been visiting their families. That incident resonated with me. How does it work in these international scenarios?

Hadley: if we play that out, countries under embargo or under a trade dispute, would they set up their own enforcement entities? And if so, how does that split the web? How do we deal with mismatch between global geography of web and political geography?

Dan: right now the country based authority for the name registry owns that registry and there's a certain enshrinement of that approach. We continue in theory to have one web and ..

K: I don't know how it works in the pki world, the CAs are different from the registry entries.. how is it handled in web pki? The other thing.. if you're not part of a fps it doesn't mean that your site is going to be inaccessible. It's not as dire as saying your tls cert is revoked. It potentially means you have to build in things like some sort of login api or something.. whatever constraints browsers are going to place on third party interactions, Do you see that as too high a bar for sites? Sometimes there can be business implications, ads measurements across domains. If you can't measure you can't pay the publisher the money cos a user saw the ad on their site. That's the other thing brewing. I haven't figured out how to articulate it yet.

Dan: I do feel .. what we build.. we have this One Web principle, and we're also trying to make sure what we build is applicable to small web providers as well as large web providers. FPS should work for a chain of barbershops in manchester as much as it works for facebook and all the facebook properties. It should work across international borders. Anything we build should be applicable to small web as well as large web.

K: stuff to think about - will find out about PKI.  I did want to dig on the question on the random spot checks.  If someomne abuses that - then originally - when we proposed the policy a site would submit a list of domains and someone would check - including checking ownership.  Some of the TAG feedback was that it doesn't seem scalable.  In the dieconnect case it's not the entire web - they first have a blocklist and then an allowlist on top of it - and so we talked to some lawyers and .. common privacy policy common identity... were discussed. We could perceive tech checks but ownership is the hard one. Legal counsel says: if a company misrepresents the ownership structure that's in the pervue of the regulatory body they operate under - there are implications. We should make the definition crisper - and an org asserts that this is correct then the legal implications are a deterrent. We have built in abuse reporting as well - revoking - block list for misuers... 

Dan: is that documented in the explainer?

K: in the UA policy document

Hadley: hihgly likely to be country specific and location specific. Presumably you have lawyers in a lot of different countries - be great to ask all of them for universally applicable wording

Rossen: interested to figure out controllorship and ownership respnsibilities and how that applies to .. curious how much will transfer into UA and how you're thinking through this. If I'm a German citizen in Germany my GDPR policy applies that all of my data goes to Germany even if I take my computer and I'm in Brazil on vacation. Now by me taking physical  device out of geo boundaries I'm still having gdpr enforcement and my data goes back to the data controller and owner in this case. Controller and owner is the service in this case. When the browser enters this space I'm still trying to wrap my head around where do we stand as a UA.

K: a balance here is to make the policy as lightweight as possible. THe policy is to prevent abuse. As a brwoser we don't need to get too much into regulatory aspects - that'sr esponsibility of the site owner. If the regulatory agency requires them to get consent we should do that, not just ..

Dan: Can I encourage you write something?

#### [SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

### Breakout B 

Present: Peter, Rossen

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov


#### [WebTransport review request](https://github.com/w3ctag/design-reviews/issues/669) - @plinss, @atanassov


### Breakout C

Present: Yves, Sangwhan, Lea, Amy, Dan
Regrets: Ken

#### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @torgo, @kenchris

### DIDs - should/can the TAG formulate a response to the formal objections or the issues raised in the formal objections?

[discussion]

Amy: suggesting a "dystopia avoidance" questionnaire which also includes environmental considerations along with other things like centralisation, affect on minority groups, widening divides, power imbalances ("societal impact questionnaire")

Sangwhan: possible for inclusiuon in this doc: Anything should not have an exponential increase of energy as you use it.  Toxic pattern: Bundling of JS applications ; How do we fix this? Https has higher overhead because of these inefficiencies and how do we address this?  https is here to stay but how do we make it better?

Dan: steers the conversation in a more positive direction. 

Yves: many cahce ineffeciences are not due to secure contexts, but timing

Dan: is that part of the same societal impact work?

Sangwhan: more like trying to address an existing practical problem. I've been thinking about this for a long time.

Dan: sounds like a Finding

Sangwhan: it is a Finding. Key takeaways we can bring to people and ask for solutions. Makes the web experience better.

Yves: reusing the cache but with a random delay..

Sangwhan: has anyone looked into browser level package managers?

Yves: I'd be happy to be part of the discussion

Dan: I'm hearing two documents coming out of this discussion. Finding about cacheing issues on the web platform, and societal impact questionnaire

### Plenary Session

Present: Dan, Peter, Yves, Sangwhan Lea, Hadley, Amy

#### https://github.com/w3ctag/design-reviews/issues/414 Trust Token

Dan: there was a response to us - left comment and we'll talk about it next week.

#### https://github.com/w3ctag/design-reviews/issues/632 media features client hints

Dan: We will discuss next week.

#### Breakout Rollup

##### Breakout A

Amy: discussion with FPS. Felt like K went through the points left in my feedback but still some doubts. Also left a comment on more things we'd like to hear from them on. 

Dan: response about international applicability was something like not everyone has to use this. But aren't we building stuff everyone wants to use? Eg. if you had an org in a particular country repsonsible for curating fps and judging whether certain parties are part of the same party how is that going to work when certain countries bar commerce with other countries, vs dns where yes there are questionsa bout centralisation but at least individual countries control their own name registries so you don't have that issue. That was one thing they were going to come back to us on.

... proposed closing anonymous iframes. I asked a question, got a response.. point by point addition to explainer to address the issues. Point 3 about ephemeral storage.. I feel like Tess would have feedback on that. Not sure whether to close. We've gone back and forth and they've tried to address the feedback. Just close?

Sangwhan: not against closing

Dan: [closes]

Dan: we talked about baggage api, hadley and yves left feedback

Yves: was looking because of question about structured headers, abnf was a bit weird, outdated definitions

Dan: schedule for next week. Secure payment confirmation... had a response

##### Breakout B

Peter: [on editcontext API](https://github.com/w3ctag/design-reviews/issues/416) - concerned about the model - whole API seems to be built around plain text rather than DOM.  Using indexes for start and range ... have to standardize behaviours. Not sure if that's part of this API or not...

Sangwhan: what's the concern?

Peter: use case is - people trying to build editors - being able to edit on top of a plain text buffer... this API falls down if there are children... why don't wwe just build it around the DOM?  Rossen's argument is if you're building something like word you're building your own model. I think that's fine but what if you want to edit HTML? Why are we ignoring a fundamental part of the platform. Seems like a reasonable use case for the web.  We didn't get it right with contenteditable - this is one attempt to improve that but takes it in a diff direction. [will write up comments and leave them on the issue]

[Web Transport](https://github.com/w3ctag/design-reviews/issues/669)...

##### Breakout C

[Possible new findings https://github.com/rhiaro/societal-impact-questionnaire (Amy) and something about bundling (Sangwhan)]

#### Issue Triage

### Logistics

Chair: Dan

Scribe:
