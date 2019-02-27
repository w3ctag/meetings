## TAG Teleconference
##### 26 February 2019

Present: Kenneth, Dan, Sangwhan, Peter, Lukasz, Yves

Special Guest Star: Alex Russell

Regrets: Hadley, David, Tess

Scribe: Dan

---

Agenda:


* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) @torgo @hadleybeeman
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) @cynthia @hadleybeeman @travisleithead @plinss
* [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241) @dbaron @ylafon @hadleybeeman @lknik
* [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321) @alice @dbaron @kenchris 
* [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) @dbaron @torgo
* [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) @cynthia @alice @lknik
* [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) @hober @cynthia @torgo
* [Serialization of natural language in data formats such as JSON [I18N]](https://github.com/w3ctag/design-reviews/issues/178) @cynthia @dbaron
* Triage of new issues

---

### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - have to defer

### [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198)

Some feedback from 19 days ago. 

Dan: Travis left feedback 20 days ago and there was a reply.

Sangwhan: i had one piece of feedback. David also had feedback.  My main issue was this was only exposed to window.  

Peter: they gave feedback on that point.

Sanghan: not entirely convinced so will have to write back on this one.

Peter: how about the rest of it?

Sangwhan: i think we wantt to get david's feeedback as well.

Dan: Agreed.

Sangwhan: everyone needs to comment back who have raised issues here.

Peter: actions on us to continue to leave feedback  - 

Sangwhan: let's bump to next week.

### [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241) 

Yves: we filed an issue concerning ads network abusing this  - don't know what the response has been.

Alex: anyone can [abuse it] like that

Yves: maybe a way to lower the priority to lower the priority 

Alex: there is already a priority system - certain media types...   Priority hint - a way to hint to the server to treat this as high priority. It's possible already gain this...  this doesn't create a new space. it does allow things that were low but should be high priority to be properly marked. Browser has full leeway to depriotitize. It's all suggestions.

Yves: you presented that - it's clear - the issue is to avoid gaming the system in anyway. is it possible to have 3rd party script like ad blockers that would be able to lower the priority of things instead of blocking.  

Alex: yes it will allow them to repriotitize content. 

Yves: the concern was - we know there is a priority ststem but is this safe enough to be wideley news

Alex: any advertiser who wants to game the system can already do it.  i can reflect that in the comment here.

Yves: we are just pending resolution of those issies in the wicg.

Dan: could this be a tool that an extension uses to help customize your experience of a partocularl web site

Alex: yes I think it is - hasn't been mentioned here.

Dan: I can file something about the use by e.g. extensions.

Peter: How long?  Maybe a few weeks.

Yves: let's follow up in 2 weeks.

### [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321) 

Alice: i took a look at this - the big PDF.  last we heard is that the PDF is stale and needs and update.

Peter: LittleDan's comment about not exposing GC - do we have feelings about that?

Alice: Perhaps we should ask whether the new API (referred to in an issue comment which littledan linked to from the review request) is ready for feedback?

Kenneth: other specs also expose GC

Sanwgan: clearly they haven't looked at our design principles doc ...
... for this particular case it's exposing necessary mechanism ... explicitly exposing
GC or by accident seems to be the thing we're aagainst.

Alex: it's whether or not .. if you read the value out of an object you will continue to perceive it. That's the bar we've tried to defend. Problem with WebAudio api prior to atomics and shared array buffers... always a case that if you posted another task and came back later ... question is here: does this violate consistency. I think answer is no. - but needs formal analysis.  

Peter: anything more?

Alice: I'll update the issue.

Peter: GC observability - should that be caputred in the design guidelines document?

Alex: I think it's worth it.

Peter: There is an issue filed - issue 100 https://github.com/w3ctag/design-principles/issues/100

Peter: 2 weeks? 3 weeks?

Alice: nothing has happened since f2f - so 

Peter: 2 weeks

## [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339)

Dan: let's wait for david

[bump]

##  [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336)

Sangwhan: still pending external feedback.  At f2f we requested clarification whether it's only accessible from top level frame and have not heard back. 

Dan: pinging?

Peter: we have pinging

Lukasz: wondering whether there is a risk of ... not limited to web browsers .. is it limited to the browser or ... operating systems. OS have lock screens. 

Sangwhan: it does - if you grant this permission to multiple origins then you can use it for cross origin tracking - if the user goes idle on multiple origins at the samne time you could  use it for tracking

Lukasz: usage patterns - conjunction with other APIs e.g. sensors

Alex: this is expressed as a permission - where browsers can decide what policy to apply - fuzziness is available. if the origins are currently running are collaborating with eachother in the same browser process they could build a wormhold scripting relationship in some browsers. e.g. iframe -> relationship -> different window (e.g. through serviceworker). Question here about what else is being exposed and how it's exposed to users is important.

Kanneth: would it idle immediately if the screen turns off?

Sangwhan: OS dependentent?

Lukasz: or use the keyboard or mouse for 1ms - is it idle. 

Alex: it's user agent defined.

Lukasz: so different for each UA.

Alex: potentially different for each UA and for each OS - in some it's most approriate to use screen lock as a signal of idleness.

Lukasz: a link betwen browser and OS

Kenneth: browser knows that if there are 5 sites open looking for idle it doesn't have to tell them at the same time.

Alex: we should look at this and make sure that idleness is only being delivered to top level documents, only in secure contexts and documents withough visibility are not having the event delivered.

Kenneth: but if I have an app running int he background i may want people to know I am idle...

Alex: what is the visibility state of tab?

Kenneth: often not visible - not opened - 

Alex: there's a question for the services if visibility is strong enough correlation with idleness

Sangwhan: I think it's 2 different flags.


Dan: ... tabs ... I' have notifications in another tab but should people there see me as idle

Kenneth: lot of people want to know if you're available. if you're in a meeting - that's a kind of idling - it's more like "im busy" - whether you're going ot answer an IM or not.

Peter: an "active idle" like a do not disturb or "distracted"

Lukasz: how should this work in private browsing modes and should user be able to disable it. Let's say slack asks for permission to use "idle"...

Alex: question we're being asked - if web platform exposes this, does it expose what develoeprs would need and does it fit with the rest of the platform.

Peter: looks like this is modeled on mution observer / interaction observer. is that right? .. you can pass in a theshold

Lukasz: what's the granularity of updates.... 

Alice: mutution observers vs. events trade-off: we suggest observers vs events. How would someone know when to use which.

Alex: observers tend ot be about the rate you're going to fire things. it's a good way to do complex configuration. Multiple parties to take a different view of the event stream. for lf stuff an observer is probably not great - event tends to be cleaner and easier. visibility state event vs intersection observers.

Peter: bunch of feedback - can someone(s) summarize?

Alex: i can summarize pieces I recall

Kenneth: I can do some 

### [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285)

Sangwhan: we need to set up a call with David. 

### Triage of unassigned issues

https://github.com/w3ctag/design-reviews/issues/341 - feature policy evolution - sangwhan 

https://github.com/w3ctag/design-reviews/issues/342 - first party sets - david & dan

https://github.com/w3ctag/design-reviews/issues/343 - Verifiable Credentials Data Model 1.0  - hadley

https://github.com/w3ctag/design-reviews/issues/344 - Web Publications - dan

https://github.com/w3ctag/design-reviews/issues/345 - Audio books - david


