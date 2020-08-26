## TAG Teleconference
##### 24-25 August 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-08-24](https://www.timeanddate.com/worldclock/converter.html?iso=20200824T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @kenchris, @plinss
* [jxl Content-Encoding](https://github.com/w3ctag/design-reviews/issues/541) - @ylafon, @hadleybeeman, @plinss
* [Security Questionnaire PRs](https://github.com/w3ctag/security-questionnaire/pulls) - @torgo, @hober
* [Triage Design Review Issues with no Milestone](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+no%3Amilestone) - All

#### Breakout B (US / APAC) - [2020-08-24](https://www.timeanddate.com/worldclock/converter.html?iso=20200824T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Constant bitrate audio encoding with MediaRecorder](https://github.com/w3ctag/design-reviews/issues/540) - @hober, @cynthia
* [AB Proposal on communications](https://github.com/w3c/AB-memberonly/issues/34)

#### Breakout C (APAC / Europe) - [2020-08-25](https://www.timeanddate.com/worldclock/converter.html?iso=20200825T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo
* [Design Principles Pulls](https://github.com/w3ctag/design-principles/pulls) - @cynthia, @alice, @torgo

#### Plenary Session - [2020-08-26](https://www.timeanddate.com/worldclock/converter.html?iso=20200826T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [AB Proposal on communications](https://github.com/w3c/AB-memberonly/issues/34)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Peter, Kenneth, Dan, Tess, Yves, Rossen

Regrets: 

#### [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @kenchris, @plinss

Ken: specific issues - we gave feedback - they say they have addressed our feedback. 

Tess: issues were auto-closed? 

[looking at their issues to see if the feedback has been addressed]

Ken: I'm fine with this...  One of them they have filed an issue which hasn't been fixed yet.

Dan: are there key issues that haven't been resolved - or  can we close?

Ken: for promises they have listened, for scope they are considering, and they have combined screen enumeration and placement which also follows our feedback so I would say yes. And they filed new issues in their new repo.

Dan: Propose we close then.

Peter: my main concern is the inetraction with the foldables work.

Ken: thomas steiner filed an issue related to that issue 21 on the new repo...  Nothing there yet but the issue is filed.

Peter: my main fear is that - the foldables work is in flux - someone's going to ship something and then it will be an API we can't change and it won't work nicely with foldables...

Ken: i think that's why they asked about the scope.

Dan: we could leave that specific feedback - that this needs to play well with the developing foldables work.

Peter: i'm fine with that.

[consensus to close]

Ken: I can [leave a closing comment and close it]

#### [jxl Content-Encoding](https://github.com/w3ctag/design-reviews/issues/541) - @ylafon, @hadleybeeman, @plinss

Yves: I made a comment on the issue... It's not ideal to have a content encoding for only one media type but it has been done in the past.  Proosed close: satisfied.

Dan: propose close and we can close at the plenary.

#### [Security Questionnaire PRs](https://github.com/w3ctag/security-questionnaire/pulls) - @torgo, @hober

[PR 90](https://github.com/w3ctag/security-questionnaire/pull/90)

Merged.

[PR 91](https://github.com/w3ctag/security-questionnaire/pull/91)

Merged.

[PR 94](https://github.com/w3ctag/security-questionnaire/pull/94)

Dan: let's consider clarification between user and user-agent and how that might help to clarify the document.

[going through commits in the PR  and leaving comments there]

Tess: I will submit my review as request changes...

Dan: cool.

#### [Triage Design Review Issues with no Milestone](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+no%3Amilestone) - All

[Task scheduling](https://github.com/w3ctag/design-reviews/issues/72)

Rossen assigned

We agreed to bring it to the f2f Agenda.



### Breakout B

Present: Alice, Peter, Rossen, Tess

Regrets: Sangwhan

#### [Constant bitrate audio encoding with MediaRecorder](https://github.com/w3ctag/design-reviews/issues/540) - @hober, @cynthia

Tess: Very straightforward change to let authors request a bitrate mode, and also query what the bitrate mode is.

... Nice, straightforward proposal, good use cases.

... Only one quibble: Bitrate mode enum values are "vbr" and "cbr". I know what those mean, but it's obscure. It should be "constant" and "variable". The "bitrate" is already part of the API. I'll write that out in a comment.

Alice: Also it's hard to distinguish "v" and "b" via audio.

Tess: Right. I'll comment; Sangwhan might have additional concerns, so don't want to immediately close.

#### [AB Proposal on communications](https://github.com/w3c/AB-memberonly/issues/34)

Discussed, no objections.

#### [Triage Design Review Issues with no Milestone](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+no%3Amilestone) - All

### Breakout C

Present: Yves, Ken, Dan

Regrets:

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo

#### [Design Principles Pulls](https://github.com/w3ctag/design-principles/pulls) - @cynthia, @alice, @torgo

#### [Triage Design Review Issues with no Milestone](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+no%3Amilestone) - All

### Plenary Session

Present: Tess, Dan, Peter

Regrets: Alice, Yves, Ken, Sangwhan

#### [AB Proposal on communications](https://github.com/w3c/AB-memberonly/issues/34)

We discussed and agreed that given the feedback we have received from TAG members on this issue, we are supportive of the agreed text, with Alice's proposed amendments, as indicated here: https://github.com/w3c/AB-memberonly/issues/34#issuecomment-679948812


#### [Triage Design Review Issues with no Milestone](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+no%3Amilestone) - All

#### Mini Apps

Tess: In light of the workshop, can we close the three open design review issues?

Dan: I think we need to give feedback on the charter proposal. 

* Breakout Rollup
* Issue Triage
