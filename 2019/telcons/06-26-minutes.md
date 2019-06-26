## TAG Teleconference
##### 26 June 2019

Present: Tess, David, Peter, Dan, Alice, Sangwhan, Yves, Lukasz

Regrets: Kenneth

---

Agenda:

### Breakouts organization

Sangwhan: Are we actually using this?

Dan: Sort of, Hadley and I met last week to discuss matters.

Dan: suggest that we take 5 mins at end of meeting to organise breakouts

Alice: re calendar - if we use google calendar then you can rsvp and get reminders....

Peter: you can invite people and rsvp and all that using the caldav feed... - there is a web UI...

Sangwhan: for me, i the caldav feed always has the times wrong...

Peter: Fine with switching over if more people prefer Google.

Dan: Okay, let's do that.

[...discussion of calendars...]

### questionnaire update - lukasz



### Update on [Ethical Principles issues](https://github.com/w3ctag/ethical-web-principles/issues) triage - @hadleybeeman, @torgo

Dan: Hadley and I met and triaged issues on ethical principles document.

Dan: 3 categories: editorial (need to be clearer, e.g., in intro), people have proposed new principles (e.g., minimal change, paving cowpaths, data freedom portability), and clarifications to existing principles.

Dan: Hadley and I thought we shouldn't be too quick to change the document.  Maybe having an update ready to go for TAG meeting prior to TPAC.  Reluctant to add new princples, but certain things we should listen to regarding updates to text (e.g., wording around accessibility; jbrewer said wording too focused around website accessibility; we're discussing in issue).

Dan: If we continue to work on these, could have proposed updates around that meeting.

Dan: Also, appears to be a philosophical discussion in one of the issues (["should this document also consider data on the web"](https://github.com/w3ctag/ethical-web-principles/issues/4)).  danbri left a comment about the role of the TAG; others have weighed in.  People may wish to read it and weigh in if moved to do so.

### Web of Things is waiting on us [357](https://github.com/w3ctag/design-reviews/issues/357), [355](https://github.com/w3ctag/design-reviews/issues/355) - @torgo

Dan: WoT group blocked on our lack of feedback... 

Tess: why do they think they are blocked

Dan: I will ask the group chairs why they think they are blocked

David: I wrote a long comment on 355.  There is related Mozilla work.  They are building a mozilla web of things implementation.  They are half aligned with the WoT specs.  I wrote a comment that called out the big issues. MNOT also made a comment in the issue - they are building something that is very complicated and not likely to lead to interop.  The fundamental disagreement is that there are people in the group that want to build a w3c web of things specs that can interop with the existing IoT devices out there - so it has to be able to map existing device capabilities (e.g. turning lights on and off) so you need a full description language. The alternative that Mozilla is pushing : here is the rest protocol, here is the web sockets protocol so if you want to be a web thing you need to speak these protocols. MNOT is sort of coming from same perspective.  

Sangwhan: I took a quick look at this and had some issues trying to figure out what they are trying to do - seems like an infrastructural framework.  There is very little scope defined here.  

Dan: We have some experience with the web of things (mozilla) framework...

Sangwhan: scope is an issue and also security model - and CORS-like functionality to restrict access....

Peter: they have a deadline (today)... Don't know if that charter is being renewed or what...

David: there was a workshop a month or 2 ago - one of the goals was development of a new charter...

Yves: they asked about moving to CR, w3m say it would be better to get validation from the TAG first...

Dan: there are some issues that have been raised by sangwhan and david... 

Yves: should we ask about the consensus state of the specification, considering David's feedback... 

Dan: suggest Yves and I get on a call thursday to discuss more and come back to group next week with an output.

* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @torgo

Tess: we talked about this last week and I took an action to search TPAC minutes and write up some comments. Not done yet. 

[finding breakout time to discuss..., Tess & Alice]

* [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @hober, @kenchris

Tess: lots of discussions since last week...  Giant chunk 

David: 2 issues on whatwg HTML [4696](https://github.com/whatwg/html/issues/4696) and [4697](https://github.com/whatwg/html/issues/4697) that are substantive. A bunch of the discussion has moved there.

Tess: this seems to be a moving target. I'd like to see the HTML issues progress to consensus. 

Alice: TAG reviews for those 2 things?

Tess: personally no - i think we should personally weigh in on those issues.

Peter: I think we should be keeping an eye on those discussions...

Tess: maybe we should let this one cool off for a couple weeks...

### [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @cynthia, @alice, @lknik

Alice: we discussed this - sangwhan and I - an explainer did come in and fleshes [things] out reasonably well. We thought we are done.

Sangwhan: i had issues with the naming.  

Alice: that coalesce is a tricky name for non-english-proficient...  Spelling bee word. But might not be a frequently used API...  I can't think of any good alternative.

Dan: bundled?  Doesn't feel like we should block on that though.

Alice: a LGTM with suggestions.

Sangwhan: yes - i'm ok with that but I'd like to be on record about the english-language issue raised.  When reading somneone else's code this won't read nicely.

Alice: I will write the feedback.

[consensus to close]

### [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris



### [FetchEvent.resultingClientId](https://github.com/w3ctag/design-reviews/issues/307) - @cynthia, @ylafon

Sangwhan: we need to close this as well as we haven't provided feedback and it has shipped in the meanwhile.

Peter: "overtaken by events"

Peter: how many implementations?

Sangwhan: as of today it's 2.

[conesnsus to close]

### [Form Participation API](https://github.com/w3ctag/design-reviews/issues/305) - @hober, @plinss, @lknik

Tess: suggest we close the issue "thanks for flying". 

[consensus to close]

### [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) - @cynthia, @dbaron & [Feature Policy JS introspection API](https://github.com/w3ctag/design-reviews/issues/292) - @cynthia, @kenchris

Dave: [reads tea-leaves] I think this needs a breakout. 
304/303/389

... cors-like bit... 

Sangwhan: happy to do a breakout.  

Dave: we can figure it out time-zone wise.

Sangwhan: this could change how you substrate protocols - layered protocols - http3 runs on top of quic - quic runs on UDP. Also we have DNS over http - a protocol that has been pulled up. CHanges the dynamics... 

Hadley: so you would say dns over http is a substrate of http?

Sangwhan: yes.

Peter: Breakout on this?  Milestone on breakout session - a generic one... 

Hadley: label?

Dan: feels more like a label 

Peter: ok but then set a milestone when you are done with the breakout...

Alice: there is also a new TAG review to web transfer API - which is 389 so you may want to pull that into the breakout as well.

Peter: should we close 303?

Alice & Sangwhan: no

Alice: 2 separate things.

Dave: possible it's 304 and 389 but we can sort it out in the breakout...

[set for breakouts]

### [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) - @cynthia, @dbaron

[bumped]

### [Spatial Navigation](https://github.com/w3ctag/design-reviews/issues/287) - @cynthia, @dbaron, @hadleybeeman

Sangwhan: i have provided review feedback. I know some external to the TAG have expressed concerns. that's not something I can speak to.  Suggest we close.  In terms of tech review we have done what we can do.

Peter: discussion ongoing...

Sangwhan: for the feature policy bit 

Dan: what is implementation status?

Dan: vivaldi had one...

Sangwhan: they are 95% conformant... Definitely does not have feature policy... Other than that, none.

Peter: so close this for now?

Alice: nothing additional to say...

[consensus to close]



---
