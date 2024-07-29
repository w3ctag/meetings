# TAG Teleconference
#### 08-10 July 2024

---

## Agenda:


### Breakout A (Europe / China) - [2024-07-08](https://www.timeanddate.com/worldclock/converter.html?iso=20240708T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Agenda Bashing

### Breakout B (California / Europe)  - [2024-07-08](https://www.timeanddate.com/worldclock/converter.html?iso=20240708T153000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Matthew, Yves, Lea, Hadley
Guests: Sam Goto & guests from Google team working on FedCM: Michael Knowles, Christian, Yi Gu, Johann Hofmann
Scribe: Matthew

Dan: We're keen to make progress on the various reviews we have, but need some metadata on how the pieces fit together, and what the relative sizes of the different proposals are (in terms of issues they're addressing). I.e. context with FedCM would help us out.

Sam: Hearing that you're asking for clarity on FedCM from a long-term/big picture perspective so you can get a sense of which work is long-/short-term?

Peter: I'm getting the impression of conflicting goals in terms of the direction the work has taken, sò looking for clarity on that.

Sam: Thank you - we appreciate your help and feedback. There is tension in this area, which we seek to resolve. End goal: there's a lot of value in composition on the web. Web is composed of many services. One component is identity. It's useful to take accounts from web sites and bring them to other sites. Sometimes the same primitives that enable that also enable tracking, which for the most part people agree is not good for the web. That's the tension that we're in. A lot of things that make federation possible also enable bad things (i.e. tracking). We want to block third-party cookies in a way that removes the bad parts, and allows us to keep the good parts. Therefore, 3pc deprecation caused us to think about what would break, and what we'd like to not break. Federated identity is one of those. Federation, OAuth, SAML, have been constructed as top-level redirects.

Sam: There's an opportunity to make the browser a first-class citizen in terms of federation. Overeall strategy has been (1) do no harm; and (2) leave it better than we started. Inserting the browser allows us to do new things. Some of the tension comes from the desire to not break the web (e.g. blocking 3pc without breaking things); also we want to construct a system that propells us to where we want to be.

Dan: *references TAG design principle <https://www.w3.org/TR/design-principles/#leave-the-web-better>*

Sam: +1 to the design principles

Sam: Right now, you can sign into a site using multiple things (user/pass, passkeys, Facebook, Googlke, ...) - this is all down to the site's UI, not the browser. You can only pull this out of the content area if the browser knows how to mediate those things. Browser can mediate user/pass, and passkeys, also SMS OTPs. One of the last pieces is to mediate federated accounts. When the browser can, you can offer a UX that can't be offered right now. We can aggregate them. A lot of this presupposes that identity providers and web sites have motivation to change. Blocking 3pc / iframes provides that pressure.

Sam: The tension you mentioned comes from this.

Sam: Passkeys are super-exciting; we're trying to figure out the right framing with Passkeys and federation. Goal is FedCM gets used once, when switching device, e.g., but then is traded for passkeys.

Sam: There's an overall trend for the emergence of identity wallets, largely due to regulation coming from Europe. This has privacy implications. Real-world identity challenges.

Sam: It's a challenge to move an industry based on 3pc and iframes for decades, to bring them along the way.

Sam: Any questions?

Peter: My understanding is there are multiple goals; not just replacing 3pc; replacing SAML for SSO?

Sam: Yes (more details below)

Peter: I'd like to see more of a fully federated identity, where I'm not logging in with e.g. Facebook, but with an identity provider of my chosing. Concern is that if it's a handful of major providers, we're centralizing, rather than distributing.

Sam: *references GitHub issue <https://github.com/fedidcg/FedCM/issues/240>*

Sam: Is this intended for social login, or SAML and enterprises? Also see the question about bringing one's own identity provider. The framing so far isn't FedCM vs SAML/OpenID - rather FedCM replaces 3pc and iframes. If we succeed, SAML et al will still exist, but they'll bind to something that's higher-level than 3pc and iframes.

Peter: In my day job, we can use things like SAML with no 3pc necessary. I would like to be able to plug into a federated identity method without having to support many different ones.

Sam: I think in the end this is where we will get to, but we haven't yet because the browser hasn't been as involved in the process. Tracking with 3pc is easier to orchestrate than link decoration. But blocking 3pc can provide pressure to get people to move. FedCM could help with addresing bounce tracking. I don't think people move to FedCM without some pressure.

Peter: Agree people won't move to a new solution just because it's there.

Sam: I think the TAG can contribute by providing reviews and form opinions on how to architecturally handle bounce tracking etc.

Sam: We have an IDP registration API - allows sites to identify themselves as identity providers, and thus allows other sites to bring their own (see above issue). This is in Chrome Canary, behind a flag. Still early. I agree and empathize with the case of being able to express one's own prefernces re provider - chimes with the IndieWeb community, and people from the fediverse.

Peter: We weren't aware of there being motion in this direction.

Sam: I may file an early design review - still some details to work out.

Johann: In the enterprise space, a lot of vendors we've talked to use 3pc and iframes (taking what they have in a first-party context, and applying it to a widget in a third-party context) - this is where a lot of our motivation is coming from. For a long time we've had the view that enterprise will have their own separate policies etc., but they don't relaly want that - they want to use open standards, as it's better for their users, and simpler for everyone.

Peter: Moving things to cloud infrastructure is perhaps a big part of this.

Christian: Coming back to registration API, we also have the Multi-IDP API. This allows sites to specify multiple IDPs. We think this will be helpful with smaller IDPs.

Peter: It's helpful, but if the RP is to pick the IDPs then it'll still be biased towards bigger IDPs.

Peter: The other concern we keep running into: direction. I hear the goal of browser UI being used to orchestrate the process. But a lot of the proposals we look at involve providing more info to the content area. We're concerned how much effort is being put on preserving the status quo - just without 3pc - vs getting people to move to a better approach?

Sam: *Shows mock-up of ID management UI anchored into the browser's URL bar*

Peter: I know this is part of the direction for the future. But we keep seeing more and more FedCM features being implemented in the content area - hopefully shortlived. I would like to see more effort going into the browser UX.

Sam: Looking at this problem, there are many prior attempts at solutions (c.100). One of the common themse was an adversarial relationship with identity providers. We're trying to make IDPs first-class citizens in the browser, whilst understanding the way they are operating currently.

Sam: Having a partnership with Sign in with Google (the largest IDP) allows us to improve our relationship with all IDPs. We want to adopt a constructive approach to migrating away from 3pc - we think this differentiates our approach.

Johann: Peter, can you clarify your concern wrt in-browser vs in-content?

Peter: I understand the need to not be adversarial with IDPs. Not referring to Sign in with Google. Some IDPs use their position to track the user. Want to make sure we're not enabling the abuse cases. IDPs are going to have to lose some capabilities they had in order to protect users in future. In future, I hope only a bit of content will be needed in the page (e.g. if additional providers are available). Want to limit the ability to inject content into a third-party site.

Sam: *shows the widget that's currently in Chrome stable - this looks like it's within the content area*

Peter: ACK that sometimes it appears to be within the content area, but concern is around e.g. the buttons being injected into the site.

Johann: Right now, the IDPs have SDKs the site uses to add buttons, or the site writes one - I am not aware of any functionality that injects content.

Peter: **SCRIBE MISSED THIS: referencing something you had read previously?**

Sam: The [multi-IDP API is under TAG review](https://github.com/w3ctag/design-reviews/issues/803); behind a flag in Chrome; allows Facebook accounts and Google accounts to be embedded into the same account chooser.

Peter: +1 to this use case

Sam: Another extension is to allow the user to bring their own IDP. *shows example*

Peter: ACK.

Sam: Once these things are mediated by the browser, the browser can render them anywhere. Because it's rendered by the browser, we can take it out of the content area, into the browser UI. This is not a web platform change, but a browser change. Does this order of steps make sense? Do we arrive at where you want to arrive?

Peter: I believe we will - but part of the problem we're having is we get a review for a feature in isolation. But as part of the bigger picture, does it still make sense? We can get lost in the details.

Sam: Does the overall strategy info presented here help?

Peter: Yes. You're driving towards the end goal I'd like to see. The concerns are about the steps along the way - how many are preserving the status-quo vs striving for the better FedCM future?

Sam: We can aim to be clearer on this.

Johann: We don't want to break privacy or security. We are interested in extending the web, whilst not breaking things that exist (as long as they support privacy and security).

Peter: I understand there has to be a migration path; there has to be a transitionary step. I want to make sure we're not adding features in the transition that we'll never be able to get rid of. Does that make sense? Seen this happen before, in other areas.

Sam: ACK.

Peter: Maybe in explainers or reviews, you could highlight if a feature is more geared towards the end goal, or is transitionary.

Sam: We are partially finding a way to work with IDPs such that they want to work with us - so it's building trust. We are not fully sure of the end state. We are trying to find ways to help each-other. We expect this will converge into something better.

Dan: You mentioned a spec earlier that hadn't been sent to TAG review (multi-IDP) - is that somethign that's incubated in a CG? Are you thinking of sending it to us?

Sam: Multi-IDP has a review in progress. IDP Registration API ("bring your own IDP") is the latest one.

Dan: I'm hoping we can progress the multi IDP review - this context has helped. Is there anything we should be concentrating on/thinking about so we can get meaningful feedback to you soon? We can also talk about this at our upcoming f2f.

Sam: We appreciate the work you're doing, and aim to be clearer in explainers. We'd like to focus on the higher-level architectural issues. So far we have been looking at the low-level stuff, but there's not an existing review that we have at a high level.

Dan: We do have something we'll be talking about at our f2f regarding digital wallets. Specifically government-supplied IDs.

Sam: Re principles... we devleoped some as part of this. I could use a higher-level discussion about e.g. how does federated ID fit into the larger picture.

Hadley: +1

Lea: +1

Peter: It helps us to give advice when getting the higher-level issues.

Lea: Early design reviews should be higher-level

Sam: Ideally, TAG input would come at the beginning and the end - would be happy to work together more, earlier.

Peter: +1; we also like to hear about approaches that were discarded and why.

Sam: by the time we ask for TAG review, we've already been through Chrome's, and discussed with other engines. If you dropped the lower-level reviews, and reviewed FedCM strategy overall, then that would be really helpful for us.

Hadley: We want to have that conversation in general, and specific on FedCM. If there's anything in our issues template that puts you off and makes you feel like we want to talk too much about specifics, please let us know as this is helpful feedback for us.

Sam: ACK.

Lea: +1 to what Hadley said. You mentioned that these have gone through reviews for the low-level details. Usually, you can't have the low-level reviews without settling on the high-level picture. Then flesh out the low-level details. How do you have low-level and high-level reivews happen at the same time?

Sam: Early reviews may be verbose (as we don't know the problem space fully) but very helpful for providing guidance. Later reviews (i.e. spec reviews) are concise; overall they provide less input.

Sam: We'd like to have our _goals_ and _direction_ reviewed primarily.

Dan: This has given us a lot to talk about - discussion with Johann upcoming on Monday.

Peter: Thanks for joining us - good to get the high-level context, and direction.

Lea: There seems to be a frequent mismatch (in both directions) between whether a high or low level review request.

Peter: We appreciate that TAG reviews are part of the shipping process. Sometimes though this results in rushed reviews/timelines.

Sam: This suggests that we should ask more for early reviews, and not block shipping on later reviews.

Lea: We would like to have earlier input; a lot of times it's too late for us to provide useful input.

Peter: We want to be engaged early enough that our feedback can have positive impact.

Sam: I think we should move TAG review process back from intent-to-ship to earlier design process. The earlier things are, the less clear they are.

Peter: If the outcome is 'run an experiment, and report back' that can still help; we can follow up on it after the results.

Lea: If a feature is already being shipped as an experiment, that can be too late. For low-level details about how an API actually works, the relevant WG is probably best.

Sam: We have prototype; internal dev trials; origin trials; ...

Dan: This is a great discussion that we need to have - evolving our relationship with the Chromium project. Would like to include others too. Maybe we can start that discussion at the f2f in Seattle.

Lea: we should have a session on it.

* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
* [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss


### Breakout C (California / Australia) - [2024-07-08](https://www.timeanddate.com/worldclock/converter.html?iso=20240708T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Agenda Bashing

### Breakout D (California / Australia) - [2024-07-09](https://www.timeanddate.com/worldclock/converter.html?iso=20240709T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Agenda Bashing

### Breakout E (Europe / China) - [2024-07-10](https://www.timeanddate.com/worldclock/converter.html?iso=20240710T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Agenda Bashing

### Plenary Session - [2024-07-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240711T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Agenda Bashing
* F2F Planning

-----


## Breakout A

Present: Yves, Dan, Max, Matthew

Regrets:


### Agenda bashing


## Breakout B

Present: Dan, Peter, Matthew, Yves, Lea, Hadley, Sam Goto, Michael Knowles, Yi Gu, Christian Biesinger, Ashima ?, Johann Hofmann

Regrets: Amy


### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

### [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss

### [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss


## Breakout C

Present:

Regrets:


### Agenda bashing


## Breakout D

Present:

Regrets:


### Agenda bashing


## Breakout E

Present: Max, Hadley, Dan

Regrets:


### Agenda bashing


## Plenary Session

Present:

Regrets: 

### Agenda bashing

### F2F Planning
