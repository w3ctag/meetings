
### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/11-02-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2020-11-02](https://www.timeanddate.com/worldclock/converter.html?iso=20201102T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112) - @dbaron, @kenchris
* [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111) - @hober, @kenchris
* [triage additional design principles issues](https://github.com/w3ctag/design-principles/issues) - all

### Breakout B (US / APAC) - [2020-11-02](https://www.timeanddate.com/worldclock/converter.html?iso=20201102T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [PR: when to use sync](https://github.com/w3ctag/design-principles/pull/218) - @cynthia
* [Preserving content visibility by default](https://github.com/w3ctag/design-principles/pull/240) - rossen, alice, tess
* [triage additional design principles issues](https://github.com/w3ctag/design-principles/issues) - all

### Breakout C (APAC / Europe) - [2020-11-03](https://www.timeanddate.com/worldclock/converter.html?iso=20201103T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Readability edits: Writing good specifications section](https://github.com/w3ctag/design-principles/pull/227) - alice, dan
* [triage additional design principles issues](https://github.com/w3ctag/design-principles/issues) - all

### Plenary Session - [2020-11-04](https://www.timeanddate.com/worldclock/meetingdetails.html?year=2020&month=11&day=4&hour=21&min=0&sec=0&p1=136&p2=195&p3=240&p4=248&p5=224)

* TPAC fall-out
* Breakout Rollup
* Issue Triage


### Breakout A Minutes

Present: Dan, Ken, Peter, Hadley, Yves, Rossen, David

#### TPAC download

Ken: **second screen / folding UI** convergence; virtual keyboard session... some progress there - some feedback putting the focus on **keyboard** (as opposed to PiP, etc...)... 

... **install API** - 2 use cases : (1) promoting a few apps... e.g. workspace, microsoft office... promoting related apps. (2) you're trying to make a "store" ; token-based roll out - like an origin trial.

... **storage buckets**... a lot of co's find it difficult to deal with cookies and storage. some storage will have a to have an expiration date. With "right to be forgotten" you need this - especially in the EU. Storage buckets will give different policies for different buckets.

... **ads in the world of no 3rd party cookies** ... a wicg thing.  click measurement.  and turtledove.  has to cover the use cases the ad industry really cares about. 

Dan: attended privacy baseline...

Hadley: I attended the secure **data storage breakout**.  Not much take up from browser vendors.  Working for data models for storage, transport, protection, etc... They are trying to get support for a wg. 

Dan: Can we connect them to the storage bucket people?

Hadley: use cases include "i want to store my info in a safe location"... "want to replicate data across multiple places"... "virtual safety deposit box"...  "perisable food recall" "electronic medical records".. detailed use case doc on that.  They are planning to have all of this compatible with decentralized ids and verifiable claims.  they have some test implementations... are these use cases "load bearing"?

Dan: something something user needs

Yves: **web transport** - we will see what happens there.  next meeting next week.

Dan: **ethics** and **webxr API**.. 

Hadley: found the creativity and ethics inspiring - one one thing that surprised me - from people who aren't as part of their community as they could be - an artist in online medium - was frustrated the web wouldn't do what she wanted to do.  Comparison to Second Life - as an "old school" ... we've excluded valuable people to hear from.

Dan: we can draw some feedback into the tag ethics doc - Boaz from Bocoup working on that...

Yves: some sessions were in 2 languages - but accessing zoom by the browser didn't allow access to the translation channel.

#### Call Time Discussion

[agenda creator updated]

#### [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111) - @hober, @kenchris

Ken: We're waiting for external feedback.

#### [triage additional design principles issues](https://github.com/w3ctag/design-principles/issues) - all

#### [Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112) - @dbaron, @kenchris

Ken: kind of requires Sangwhan.

### Breakout B Minutes

Present: Peter, Alice

Regrets:


#### [PR: when to use sync](https://github.com/w3ctag/design-principles/pull/218) - @cynthia

Reviewed, discussed, added comments.

#### [Preserving content visibility by default](https://github.com/w3ctag/design-principles/pull/240) - rossen, alice, tess

Reviewed, discussed, added comments.

#### [triage additional design principles issues](https://github.com/w3ctag/design-principles/issues) - all


### Breakout C Minutes

Present: Hadley, Dan, Ken, Sangwhan, Alice

Regrets:

#### [Readability edits: Writing good specifications section](https://github.com/w3ctag/design-principles/pull/227) - alice, dan

discussed, reviewed, approved, squashed, merged...

#### [PR: when to use sync](https://github.com/w3ctag/design-principles/pull/218) - @cynthia

dealt with more comments.... 

reviewed, approved, squashed, merged...

#### [triage additional design principles issues](https://github.com/w3ctag/design-principles/issues) - all



### Plenary Session Minutes

Present: Dan, Alice, Peter, Hadley
Regrets: Sangwhan, Ken

#### Fixing the build and



#### Discussing the Council

Peter: First meeting of the combined TAG/AB 16:00 London time Friday - Jeff to chair this session. Second session will be sometime next week. 

Dan: kind of a bad time for APAC

Peter: the arguments have been sent 

Dan: I will declare an interest as one of the proposed specs on the disputed DAS charter was authored by someone on my team

#### Publication of TAG stuff in TR space

Dan: What do we want?  I feel like Design Principles should be published as a note along side of security & privacy questionnaire.

Hadley: don't think it matters. Note is probably fine.

Peter: I think the current draft should be on w3ctag.org domain - and the canaonical version should be in TR space. We should also ask the AB for an official document type for Finding and republish old findings under TR.

RESOLVED: We should request to publish the design principles as a Note (with the ability to update as needed). As well, we should request from the AB a formal TR document type of "TAG Finding".

Dan: I'll ask to get this on the AB agenda.

#### TPAC fall-out
#### Breakout Rollup
#### Issue Triage


