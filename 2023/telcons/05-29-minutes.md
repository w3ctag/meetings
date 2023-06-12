# TAG Teleconference
#### 29-31 May 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-05-29](https://www.timeanddate.com/worldclock/converter.html?iso=20230529T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [Detect UA Transitions on Same-Document Navigations](https://github.com/w3ctag/design-reviews/issues/834) - @hober
* [Disabling UA transitions for same-document navigations](https://github.com/w3ctag/design-reviews/issues/835) - @hober, @LeaVerou
* [WebRTC-SVC (Scalable Video Coding) ](https://github.com/w3ctag/design-reviews/issues/837) - @hober, @torgo
* [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov
* [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

### Breakout C (APAC / Europe) - [2023-05-30](https://www.timeanddate.com/worldclock/converter.html?iso=20230530T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

### Plenary Session - [2023-06-01](https://www.timeanddate.com/worldclock/converter.html?iso=20230601T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Hadley, Dan

Regrets:

Lack of quorum due to holidays

### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

### [Detect UA Transitions on Same-Document Navigations](https://github.com/w3ctag/design-reviews/issues/834) - @hober

### [Disabling UA transitions for same-document navigations](https://github.com/w3ctag/design-reviews/issues/835) - @hober, @LeaVerou

### [WebRTC-SVC (Scalable Video Coding) ](https://github.com/w3ctag/design-reviews/issues/837) - @hober, @torgo

### [Fullscreen Popup Windows](https://github.com/w3ctag/design-reviews/issues/840) - @hadleybeeman, @atanassov

### [Tabbed web apps](https://github.com/w3ctag/design-reviews/issues/841) - @hober, @LeaVerou

### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman


## Breakout C

Present:

Regrets:


### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion


Max: they have not answered the multi-stakeholder question

Dan: I raised this with Chris Harrelson at Google last week.

Max: the user need is important - we've spent a lot of time in discussion with the authors regarding the user need.  Regarding the solution: if there is this kind of complexity it needs some very strong user requirement as justification. That is my feeling.  It's an optimization regarding the current cross-origin policy... For the user needs section we've asked authors to clarify. They gave some examples from the developer perspective. From the user needs perspective.. not as clear. I agree with the previous comment. If there are some more concrete user needs it would be good. And multi-stakeholder is very important.

Dan: yes - what is holding back other implementers from embracing this approach? So far no signals in WebKit or Mozilla standards positions.


### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo


Dan: also related to https://github.com/w3ctag/design-reviews/issues/805

Sangwhan: I will write an async review and we can take it from there.


### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo

Dan: Related to more powerful APIs.

Sangwhan: I have context.  This effort is driven by needs of ChromeOS.   PWAs are good but from an app vendor perspective not good enough.  There to fill the gap.  But we need some level of alignment from different browser vendors.  Related to Electron, etc... Clear business need from different operating systems. If there was parity compared to native apps.  Potential to have more adoption.  Even with the risk of bring too powerful.  We have to balance this well.  The PWA rollout has been fairly sueccessful but there are gaps. Like you can't have Netflix offline on a PWA. The WICG way of doing this would be one way.  The middle ground could be an icubation chamber.  Without being able to buld an experimental applicatiomn you can't do much... This effort would have merrit in that regard. But I want to have one other browser interested in this.  It could be powerful for the future of the web.

*discussion of a potential task force on powerful webapps*

Dan: could we develop a model that has multi-stakeholder buy-in?

Sangwhan: we could have a model for isolated webapps that could be stricter - like communicating with only one origin.  The user has opted into a particular constraint - via installation... A trade-off could be "you get all this power but you lose a bunch of capabilities."  A new, fundamentally different thing for powerful APIs... 

Dan: also related to packaging and bundling...

Sangewhan: in some cases you can't have cross-origin communicaiton functionality and powerful functionality at the same tine... I feel like if you get both superpowers in one package... people could abuse...

Dan: A new permissions model?

Sangwhan: is installation an implicit grant for a set of permissions?  That's not well defined.  When it comes to installation, how the permission model should work would be different. We should have a different model for weak permissions -- in the web every permission is equal. There's an upside of having in-context permission requests - but if you have too many permission requests in an installed app then that doesn't work. Tiered permission?

Sangwhan: this issue is focused on ChromeOS business needs. I'll review - standard type review - but also expanding...

### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov

### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro



## Plenary Session

Present: Peter, Amy, Max, Dan

Regrets: 

### Privacy Principles

Dan: *Discussed the [Privacy Principles doc](https://w3ctag.github.io/privacy-principles/) and the fact that wide review is winding down - we should be seeking TAG consensus*

### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) / Powerful API Task Force

Dan: *talks through discussion on Isolated webapps*. *push notification on IOS requiring installation*

Peter: installing to homescreen vs. saving a bookmark.. distinction of a user opt-in...

Dan: we could document that as a pattern that makes sense... 

Peter: given such a model there are other things we can turn off by default...

Peter: in their explainer they talk about prior art - firefoxos - signed archive... would be nice if there were signed in some way...  Bundling and signed exchanges may not be the answer but there are other mechansisms... that people don't usually buy into..  Subresrouce integrity...


### Issue Triage

*triaged 849, 850, 851*
