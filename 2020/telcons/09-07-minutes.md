## TAG Teleconference
##### 07-09 September 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-09-07](https://www.timeanddate.com/worldclock/converter.html?iso=20200907T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111) - @hober, @kenchris
* [Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112) - @dbaron, @kenchris
* [guidance on use of JSON-LD?](https://github.com/w3ctag/design-principles/issues/128) - @hober, @dbaron, @hadleybeeman
* [Best practices for feature detection of DOM API](https://github.com/w3ctag/design-principles/issues/137) - @torgo, @ylafon, @kenchris
* [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov
* [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron

#### Breakout B (US / APAC) - [2020-09-07](https://www.timeanddate.com/worldclock/converter.html?iso=20200907T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron
* [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov
* [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron
* [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron
* [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron

#### Breakout C (APAC / Europe) - [2020-09-08](https://www.timeanddate.com/worldclock/converter.html?iso=20200908T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia
* [discussed sync/async](https://github.com/w3ctag/design-principles/pull/218) PR



* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice

* [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia


* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo

* [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon

* [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185) - @torgo

### Plenary Session - [2020-09-09](https://www.timeanddate.com/worldclock/converter.html?iso=20200909T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Review Requests:
    * [Writing good specifications](https://github.com/w3ctag/design-principles/pull/227)
    * [Event design](https://github.com/w3ctag/design-principles/pull/223)
    * [When to use synchronous](https://github.com/w3ctag/design-principles/pull/218)

* Breakout Rollup
* Merge approved pull requests
* Issue Triage

-----


### Breakout A

Present: Dan, Peter, Yves

Regrets: Rossen, Kenneth


#### [PR 236](https://github.com/w3ctag/design-principles/pull/236) 

we think it can be merged.

#### [guidance on inheritance between contexts](https://github.com/w3ctag/design-principles/issues/111) - @hober, @kenchris

#### [Create advice for how to handover access to sensors and devices on dedicated workers](https://github.com/w3ctag/design-principles/issues/112) - @dbaron, @kenchris

#### [guidance on use of JSON-LD?](https://github.com/w3ctag/design-principles/issues/128) - @hober, @dbaron, @hadleybeeman

#### [Best practices for feature detection of DOM API](https://github.com/w3ctag/design-principles/issues/137) - @torgo, @ylafon, @kenchris

#### [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov

#### [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron


### Breakout B

Present: Peter

Regrets: Alice


#### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron

#### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov

#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron

#### [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

#### [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron


### Breakout C

Present: Dan, Yves, Sangwhan, Ken

Regrets: Dbaron

#### [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia


Sangwhan: I'm gonna change the bit about failure modes.

[updated - will review and hopefully merge in the plenary]

[... continued with Kenneth when he joined...]

[...discussion about currnet vs future...]

[discussion on the fact that it's not only permissions but also pickers... do we need to say "permissions or similar"]

#### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice

#### [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia

Sangwhan: "does the object require preprocessing to a form that is more usable..." 

Sanghwan [wrote on writing some text](https://github.com/w3ctag/design-principles/issues/70#issuecomment-688715810)

#### [user agent PR on S&P Questionnaire](https://github.com/w3ctag/security-questionnaire/pull/94)

We discussed the point about "other parties" vs "origins" - and I added [a comment](https://github.com/w3ctag/security-questionnaire/pull/94#discussion_r484751070).

#### [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo

#### [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon

#### [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185) - @torgo

## Plenary Session

Present: Peter, Alice, Dan, Sangwhan, Tess, 

Regrets: Rossen

### Readouts

#### PR 236

Tess will merge when addressing Alice's feedback


#### Issue 145 - sangwhan wrote some text

[Sync vs Async]

[Ready to merge 218](https://github.com/w3ctag/design-principles/pull/218)

Peter: my point is don't be async unless there's a reason to be async

Sangwhan: Somewhat agree but it's a radical change from what we've been advocating...

Peter: not advocating to change any advice on what should be async... long running process, user interaction, permission prompt... Rather than do it the other way...  Things that can be synchronous is a broad spectrum of things.  There is a cost.  Not just performance.

Sangwhan: I agree. 

Peter: i think it's a matter of phrasing it properly... Good to enumerate those reasons vs enumerating why sync is good... CHoose apropriate one for the task.

Dan: Balanced

Peter: and guidelines where there's a grey area.

Peter: Not opposed to landing this but we can iterate on it.

Sangwhan: there are some nuanced messages scattered around the doc which advocate async.  If you read the design principles it feels like we recommend async.

Dan: suggestion: let's land this PR and then *not* close 145 but instead use 145 as a way to go through the doc and find these points and rebalance.

[agreed] - PR #218 merged.


####

[pull 94 on s&p questionnaire](https://github.com/w3ctag/security-questionnaire/pull/94) -

Tess: yes user agent implementation varries...  I will look at this again...

#### Review Requests:
    
##### [API Design Across Languages section](https://github.com/w3ctag/design-principles/pull/220)
    
[...reviewing...]  

Tess: timing attack... could reveal if you're in private browsing mode...  (specific to payment example) - I feel it's a follow-up bug that can be tackled separately.

Tess: [approves]

Sangwhan: [added some comments]

Alice: good to land?

Tess: Yes

Dan: Yes

[agreement to land]

Alice: have to dismiss David's review in order to do this.

[Squashed and merged]

##### [javascript language](https://github.com/w3ctag/design-principles/pull/222/)

[resolving Sangwhwan's comment]


    
##### [Writing good specifications](https://github.com/w3ctag/design-principles/pull/227)

##### [Event design](https://github.com/w3ctag/design-principles/pull/223)

##### [When to use synchronous](https://github.com/w3ctag/design-principles/pull/218)

#### Breakout Rollup

#### Merge approved pull requests

#### Issue Triage


