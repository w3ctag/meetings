## TAG Teleconference
##### 10 July 2019

Present: Dan, Kenneth, Peter, Tess, Lukasz, Alice, David, Sangwhan, Yves, Hadley

Regrets: 

Chair: Peter

Scribe: Dan

Rocking: yes

---

Agenda:


* [Web of Things](https://github.com/w3ctag/design-reviews/issues/355) - @kenchris, @ylafon
* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @torgo
* [JSON modules](https://github.com/w3ctag/design-reviews/issues/375) - @hober, @cynthia, @dbaron, @kenchris
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393)
* Triaging unassigned [issues](https://github.com/w3ctag/design-reviews/)

---

### [Web of Things](https://github.com/w3ctag/design-reviews/issues/355) - @kenchris, @ylafon

Ken: I looked at the scripting API. I added a few comments. They have responded to some of my comments.  Issues with complexity of properties... There are a lot of things to understand.

Dan: my suggestion is to focus on the API (also this was what Yves suggested)

David: my impression was that the API is getting dropped?

Ken: i was told there at 9 implementations...

David: I also have info from Ben [Francis of Mozilla] which I've given it in one of these issues [355]

Dan: suggest scheduling a breakout on this for later in the week with goal of closing it off.

Peter: do we need more feedback?

Ken: [difficult to understand some of the API choices...]

David: they want to interface with tons of devices that are already out there. they have a mechanism for mapping actions onto existing things.

Ken: you need to write your own adapters.

[breakout will be organised on slack]

### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @torgo

Tess: I don't think we heard back...

Alice: I had a chat with them about the feedback. they have a PR in their repo to update the explainer. They hagd one change which was to make badge into a namespace. I went through the feedback with them.  They had some convincing answers to feedback and they are working those into the explainer - it's in PR state right now. Jay says to wait a week.

### [JSON modules](https://github.com/w3ctag/design-reviews/issues/375) - @hober, @cynthia, @dbaron, @kenchris

Sangwhan: briefly looked at it - has anyone else looked at it?

Ken: i looked a while ago...  most people seemed to be fine with the idea of json modules... 

Sangwhan: the idea seems sane

Ken: some people adding it to node.js

Sangwhan: node has had similar mechanism 

Ken: i like the idea

Sangwhan: i couldn't see anything I wanted to point out as bad...

Dan: will it ignite the inter-group ... discussion ... on json?

Sangwhan: it's not controversial. This doesn't touch on the standard. JSON itself is untouched.

Ken: done in TC39 initially but moved to whatwg. not sure why [but no issue]

Alice: there was an existing javascript module script - https://whatpr.org/html/4407/38c50c4...2aa1aad/webappapis.html 

Sangwhan: loading algo is the same 

Peter: shall we close [thanks for flying TAG]?

Sangwhan: Yes

Ken: Yes

Dan: sgtm

Ken: i will write summary

### [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris

Sangwhan: i want to do a breakout with Kenneth about this.

Ken: we have had problem scheduling time...

[scheduling a breakout and deadline pushed]

### [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron

David: i was supposed to schedule a breakout - will see if we can do that for later this week.

[following up on slack to organise breakout]

### [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393)

Alice: it's new. they are wondering if they can get an expedited review.  I can explain.

Alice: they are adding an extra interface into the perf API to get metrics on performance to send back to the server to test whether your changes have impacted performance. new performance entry type. it is aimed at measuring jank. They have a jank score.

Lukasz: measuring how far the current layout is compared to the layout that is supposed to visible...?

Alice: it's more about - what does the user perceive about how stable the layout is. E.g. ads that load that cause the page to jump when you load it.  

Lukasz: sounds engine dependent and user dependent ?  Depend on engine, network, related to the user's... this info will only be provided to the web site?

Alice: as opposed to what?

Lukasz: might be misued by web sites ... like use an adversarial layout...  not sure if it's possible to devise a blueprint of an adversarial display that ... may be overthinking.

Sangwhan: looking at the algo it looks like if there is a font that loads too late this will have a really large value.

Alice: excellent question ... to leave on the review.

David: I am generally worried both about whether we will be able to make it interoperable and also whether it's the thing that will be the best to optimise for or whether it will lead people to optimise for the wrong thing.

Alice: is optimising for the wrong thing still an imporovement?

David: often but not always.

Peter: question on how does the performance observer API work... does it fire any time layout changes?  Root question is : are we expediting this, who is doing it and when?

David: i am happy to be involved.

Alice: Lukasz do you want to be on this?

Lukasz: sure at least about the issues I mentioned. yes. put me down.

Alice: i will assign myself.

Peter: milestone?

Peter: noting 2 things on the agenda for next weeek 

David: let's try

[set for next week]

## Triaging:

### [web auth feature detection](https://github.com/w3ctag/design-reviews/issues/383) 

Hadley: i would like to join

Dan: I can join

David: yes

Hadley: we can't go go much further until they have an explainer.

[assigned 2 weeks]

### [JS memory API](https://github.com/w3ctag/design-reviews/issues/386)

Peter: no spec but there is an explainer.

[Assigned Ken and Sangwhan - and 2 weeks]

### [Native File System](https://github.com/w3ctag/design-reviews/issues/390)

Dan: danger will robinson

Hadley: [danger noises]

Dave: 5th time?

Hadley: would lukasz be interested in joining?

Dan: this might have privacy issues.

Lukasz: yes.

[milestone set for 3 weeks]

### [SMS receiver API](https://github.com/w3ctag/design-reviews/issues/391)

Tess: please assign me.

Dan: me too

David: me too...

Peter: what stops this from slurping all SMS messages

David: a few things - based on an Android API that matches based on a hash.

Dan: main use case is 2FA codes over SMS

Tess: the alternative proposal is already in the HTML spec - a one-time code autocomplete value. David linked to the moz standards  position on this. And disclosure: i wrote the PR for the alternative feature.

[milestone set for ]

### [Scroll to text](https://github.com/w3ctag/design-reviews/issues/392)

Peter: haven't there been multiple things like this:

David: an IETF thing

Tess: and an epub thing (epub-cfi). bunch of prior art.

Peter: also annotations... 

Hadley: do we have past TAG reviews we could link to?

Tess: at least in the case of the similar epub technology - it has a syntax for doing assertions... and an algorithm for figuring out what the likely correct thing is. some robustness... I guess assign me.

David: i guess I could be. i've wanted this for a long time.


