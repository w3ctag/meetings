# TAG Minutes - Week-of Mon, 5 December 2022

## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/12-05-agenda.md).

### Breakout A (Europe / US) - [2022-12-05](https://www.timeanddate.com/worldclock/converter.html?iso=20221205T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss
* [Guidance in exposing some APIs only off the main thread](https://github.com/w3ctag/design-principles/issues/360) - @hober
* [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366) - @LeaVerou
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober
* [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391)
* [New principle: Patterns for x() vs xSync()](https://github.com/w3ctag/design-principles/issues/402) - @cynthia

### Breakout C (APAC / Europe) - [2022-12-06](https://www.timeanddate.com/worldclock/converter.html?iso=20221206T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [BFCache design principles PR](https://github.com/w3ctag/design-principles/pull/392) and [s&p PR](https://github.com/w3ctag/security-questionnaire/pull/144)
* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
* [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia
* [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo
* [Request for design principle clarification: Warn explicitly against getters throwing exceptions](https://github.com/w3ctag/design-principles/issues/400)
* Take a look at EWP issues
* Post 3rd Party Cookie Doc

### Plenary Session - [2022-12-07](https://www.timeanddate.com/worldclock/converter.html?iso=20221207T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Anything bumped from Breakouts A & C
* Can we merge any additional [Design Principles PRs](https://github.com/w3ctag/design-principles/pulls)?
* Async Process - how do we close issues with consensus asynchronously?
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* Republish current Design Principles to /TR ?
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* Any ideas on timing for March/April f2f?

## Minutes

### Breakout A (Europe / US) - [2022-12-05](https://www.timeanddate.com/worldclock/converter.html?iso=20221205T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Tess, Rossen, Hadley, Yves, Lea
Regrets: Amy

### [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov

Rossen: we started this off - good discussion - [Travis's summary](https://github.com/w3ctag/design-principles/issues/11#issuecomment-318080953) of Dbaron's proposal kind of summarizes the intent here.   Lea asked for some clarification but we haven't heard back.

<blockquote>
* data-only objects => dictionary
* behavior-only objects (functions only) => namespace
* mix of behavior and data (where the object holds state) => class (interface)
</blockquote>

Dan: Where would this go in the document?

Rossne: no push back....

Lea: feels like a JS API surface concerns...

Rossne: 6.2...? Preceeding all of these ones... It's higher level... Maybe we should start with it. [before 6.1]... 

Lea: that makes sense... Could be first in this section.

Rossen: travis has summarized the points he and david were talking about. We just need to expand prose.

Lea: we need examples. Media error is listed as one.

Lea: actually not sure if that Media error one is a good one. Will start a PR.

Lea: [writes comment](https://github.com/w3ctag/design-principles/issues/11#issuecomment-1337771968)

Rossen: both of the discussions linked by Rick [link](https://github.com/w3c/reporting/issues/216) [link](https://groups.google.com/a/chromium.org/g/blink-dev/c/j7vOAkMbu_M) have interesting discussions and ideas.

### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou

Dan: Lea you left a comment.. Anne [left a reply](https://github.com/w3ctag/design-principles/issues/270#issuecomment-1308806751)... 

Lea: Tess?

Tess: I think it's a fair point.

Lea: it might be interesting to make the point in the prose that HTML and SVG decided it differently... this trade-off.

Tess: the interesting point is to consider the trade-off. Not tell people "you must always do it this way"...

Tess: I will volunteer. ✨

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss

Lea: I will write a draft.

### [Guidance in exposing some APIs only off the main thread](https://github.com/w3ctag/design-principles/issues/360) - @hober

Tess: i would very much like to take a crack at this one - came up in context of media specs...

Tess: *worked on a PR - i will have a dratf within the next 20 minutes*

### [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366) - @LeaVerou

### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

### [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391)

### [New principle: Patterns for x() vs xSync()](https://github.com/w3ctag/design-principles/issues/402) - @cynthia

### Breakout C (APAC / Europe) - [2022-12-06](https://www.timeanddate.com/worldclock/converter.html?iso=20221206T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Sangwhan
Regrets: Amy

### [BFCache design principles PR](https://github.com/w3ctag/design-principles/pull/392) and [s&p PR](https://github.com/w3ctag/security-questionnaire/pull/144)

Dan: PR 392 looks good to me...

Sangwhan: *removes index.html* 

Sangwhan: there is also a style guide issue that I need to address...

Dan: we may want to do the [new document](https://github.com/rakina/bfcache-guide) first before landing these PRs because they both contain links to the new BFcache document.

Sangwhan: [creates repo](https://github.com/w3ctag/bfcache-guide) 

Yves: bfcache - same as Promises guide... Either we put all of them in TR space or leave in TAG space.

Dan: I think this kind of doc should be in TR space.

Yves: we should figure out all the guides... and having them published at the same place...

Sangwhan: https://w3ctag.github.io/bfcache-guide/ - currently reviewing and doing a style pass.

Dan: Yves can you make a list of things that should be elevated to TR

Yves: yes can check that.

Yves: Web components design guidelines and Promise Guide.

Dan: let's discuss at **plenary** - my proposal would be to make all three of those TR space docs including new BF Cache document.

Dan: can we have a bit more into text...

Sangwhan: style guide is one line guidance and then explain....   Maybe we can do a parenthetical... We chould define it in the following sentences.

*merges 392*

Dan: On S&P PR [144](https://github.com/w3ctag/security-questionnaire/pull/144/) we need Tess to weigh in.



### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo

### [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia

### [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo

### [Request for design principle clarification: Warn explicitly against getters throwing exceptions](https://github.com/w3ctag/design-principles/issues/400)

### Take a look at EWP issues

### Post 3rd Party Cookie Doc


### Plenary Session - [2022-12-07](https://www.timeanddate.com/worldclock/converter.html?iso=20221207T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Yves, Lea
Regrets: Hadley, Max, Rossen, Amy

### Breakout Rollup

*We agree we should have /TR/ names for BFCache, Web Components and Promises guide.*

https://w3ctag.github.io/bfcache-guide/

### Anything bumped from Breakouts A & C

### Can we merge any additional [Design Principles PRs](https://github.com/w3ctag/design-principles/pulls)?

### Async Process - how do we close issues with consensus asynchronously?

Lea: we started the #design-review channel on slack but we haven't defined criteria for when action happens. So what are the clear-cut criteria for closing the issue. 

Dan: the people on the issue?

Lea: what if it's untriaged and we think it can be closed?  E.g. UI event spec - it looks good. Posted in channel. Maybe we should just fast track.  Got one response. Nothing else.

Dan: could be a reasonable use for @all ?

Lea: people could mute notifications?

Dan: I think we can let people know not to do this.

Peter: in general chairs rule that a consensus has been reached.  Little concerned that it's too arbitrary.  There should be a sens of judgement. You have to have "the right people" involved. For example - if someone who has been invovled isn't on the call then ...

Lea: The primary case where this coms up is things that are small.

Dan: So peter or myself.

Lea: plus how many?

Dan: The proposer, one of the chairs says OK and then we give it 48 hours and we close it.  Mark the thread - someone sets a reminder on the thread then closes it if there are no exceptions.  

Peter: the chairs can express support in an individual capacity and also "yes there's consensus".   My suggestion: anyone can ask for consensus and start a clock.  If everyone says "yes" then there's no reason to start a 2-day clock. If consensus isn't clear then it should be up to a chair to say "we're going to do this unless someone objects".  

Lea: from the perspective of someone not a chair. I want to fasttrack something. I @all. Then we have no objectoins. Then at some point a chair posts.  What happens if crickets?  

Peter: there's a responsibility on the chairs to close that loop - so ping one of us. Then one of us can say.

### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)

### Republish current Design Principles to /TR ?

*resolution recorded - and also for EWP*

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Any ideas on timing for March/April f2f?

### General quesitons - but not dispute resolutions - how can the TAG be engaged?

Lea: is there a process for this?

*we discuss whether and when it's appropriate to raise a dispute resolution ticket*

Peter: [or...] raise a regular TAG review - an early desgin review.  Ask for TAG input... 

Peter: we can use https://github.com/w3ctag/design-reviews/discussions 

*we have a revalation*
