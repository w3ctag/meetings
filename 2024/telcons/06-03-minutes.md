# TAG Minutes Doc - Mon, 3 June 2024

## Call Agendas

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/06-03-agenda.md).

### Breakout A (Europe / China) - [2024-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240603T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [triage new design principles issues](https://github.com/w3ctag/design-principles/issues) 
* [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion
* ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456) - @torgo, @matatk
* [Terminology jumps away from principle's subject ("Use care when exposing identifying information about devices")](https://github.com/w3ctag/design-principles/issues/479)

### Breakout B (California / Europe)  - [2024-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240603T153000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [triage new design principles issues](https://github.com/w3ctag/design-principles/issues)
* [PR 476](https://github.com/w3ctag/design-principles/pull/476)
* [PR 485: Attempt to split attribute by type](https://github.com/w3ctag/design-principles/pull/485)
* [New principle: Incremental user effort should result in incremental value (or more)](https://github.com/w3ctag/design-principles/issues/473)
* [New: Avoid revealing that consent was denied](https://github.com/w3ctag/design-principles/issues/475)
* [New principle: HTML attributes can affect semantics](https://github.com/w3ctag/design-principles/issues/478)
* [New principle: Events should only fire during actual state transitions](https://github.com/w3ctag/design-principles/issues/483)
* Design Principles Abyss Clearing
  * [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov
  * [New principle: Avoid exposing API that result in synchronous flushing of CSS or layout](https://github.com/w3ctag/design-principles/issues/388)


### Breakout C (California / Australia) - [2024-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240603T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [[WIP] add forwards compatibility / graceful degradation principle.](https://github.com/w3ctag/design-principles/pull/468) - @hober
* [First pass at #453 (text-based syntaxes should be designed for humans)](https://github.com/w3ctag/design-principles/pull/472)
  * [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453) - @LeaVerou, @torgo, @hadleybeeman
  * [New principle: when to use permissions, when to use user activation, and what if neither are adequate](https://github.com/w3ctag/design-principles/issues/341)
* [HTML: Receive complex data via JS or element subtrees?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober
* [New principle: The value of HTML boolean attributes doesn't matter](https://github.com/w3ctag/design-principles/issues/451)
* [New principle: When introducing heuristics or "magic", also include a way to override them](https://github.com/w3ctag/design-principles/issues/455)

### Breakout D (California / Australia) - [2024-06-04](https://www.timeanddate.com/worldclock/converter.html?iso=20240604T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369) - @torgo
* [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391) - @LeaVerou
* [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou
* [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)
* [New principle: Document whether to add things to Document, Navigator, Window, or SomeOtherInterface](https://github.com/w3ctag/design-principles/issues/448)
* [New principle: Consider many & diverse use cases to avoid overfitting](https://github.com/w3ctag/design-principles/issues/450)

### Breakout E (Europe / China) - [2024-06-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240605T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Abyss clearing
  * [New principle: Remove deprecated functionality responsibly](https://github.com/w3ctag/design-principles/issues/361) - @torgo
  * [New principle: Deployability and Monitoring](https://github.com/w3ctag/design-principles/issues/368) - @torgo
* [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454) - @ylafon
* [Harmonize with WebAppSec Powerful Features Draft](https://github.com/w3ctag/design-principles/issues/481)
* EWP transition status / additional work

### Plenary Session - [2024-06-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240605T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Add principle on use of delta seconds](https://github.com/w3ctag/design-principles/pull/467) (close?)
  * [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
* [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457) - @hober
* [Proposed charter: Linked Web Storage (née Solid) Working Group](https://github.com/w3ctag/tracking-issues/issues/79)
  * [the new charter](https://www.w3.org/2024/05/proposed-linked-web-storage-wg-charter.html)
  * [a summary of the changes that were made (or not made), with our rationale](https://www.w3.org/2024/05/solid-new-charter-changes.html)
  * [the old charter](https://www.w3.org/2023/09/proposed-solid-wg-charter.html)
  * [diff (old vs. new)](https://services.w3.org/htmldiff?doc1=https%3A%2F%2Fwww.w3.org%2F2023%2F09%2Fproposed-solid-wg-charter.html&doc2=https%3A%2F%2Fwww.w3.org%2F2024%2F05%2Fproposed-linked-web-storage-wg-charter.html)
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Call Minutes

### Breakout A (Europe / China) - [2024-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240603T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: rhiaro, matthew, yves, dan

#### EWP transition status / additional work

Yves: I published a new version - and there were a few issues we were wondering if they were blocking or not? https://www.w3.org/TR/2024/DNOTE-ethical-web-principles-20240531/

Dan: Only changes were [119](https://github.com/w3ctag/ethical-web-principles/pull/119) 

Amy: and [mitigating harm](https://github.com/w3ctag/ethical-web-principles/pull/118) - just about mitigating threats that we can avoid... 

Amy: I don't think [either] have substantive impact on the other horizontal reviews.

Dan: Agree.

Dan: so the [31 may draft](https://www.w3.org/TR/2024/DNOTE-ethical-web-principles-20240531/) can be considered validated as having incorporated horizontal review feedback.

*consensus on this point*

#### Charter Reviews

* [Adding Digital Credentials to the FedID WG](https://github.com/w3c/strategy/issues/450)

Dan: upshot of our discussion was that this concept of a government-linked credential that's exposed to the web platform is incredibly controversial and therefore we're concerned about how it might impact the rest of the work of the group.  

.. Does the government linked credentials thing belong in the same WG as the other bits? We raised issues with that in the past. Is there other feedback we could give?

Matthew: I remember some of us being quite excited about the browser helpiing the user in this very security sensitive area. Since then I've become aware of the various concerns people have. It could be abused, and it could be abused by governments. I wouldn't say we have consensus about whether this kind of work should even be done. On the issue of does it fit in the WG - not an expert caveat - it seems quite different in spirit. Kind of by definition the government one is a monolithic centralised form of digital identity, and the federated one is more light weight and web of trust. Even without the controversity, they seem very different.

Dan: it seems like a whole bunch of people who aren't involved in the lightweight web of trust thing would need to be involved in the discussion about the government centralised one. Civil society, governments, other standards bodies. None of that needs to happen for the use cases like sign me into dev.to with my github account.

Yves: use case was more around ensuring people visiting some sites are adults and things like that. Of course you don't want to have the government knowing you're visiting certain sites. To be a way of doing that without... discussed the browser acting as..

Dan: the browser making sure the requesting party doesn't get anything besides the information that they need. The other problem I have with this is.. the work item is not age verification. It's government supplied credentials. So yes the age verification might be one of the use cases, but it has to work for others as well like presenting your passport at the border. It's easy to trivialise age verification as only applicable in certain cases... Uncomfortable scoping it only age verification.

Yves: it's just an example. One of the main examples with the difference between ensuring you are someone, and ensuring you have some property

Amy: How does it fit together with verifiable credentials? That is also supposed to support the privacy preserving age verification use case. Seems weird that this should be tied up with the fedcm stuff... Just from this conversation I agree with Matthew. I wonder if the government credentials thing... has it already been in a CG... should it have incubation somewhere else, more consensus building needed? Seems a bit left field for it to be tacked on to FedCM. Would be dispapointed to see fedcm stuff bogged down in centralized government credentials debates. 

Dan: we need an open dialog about this before we start shoehorning government credentials into the web. I'm concerned about that.

Matthew: how it relates to DIDs and stuff... Heather did a presentation at the AC meeting about identity that was really good. 

Matthew: Context on Identity (not digital passports/driving licences) discussion from AC meeting: Heather Flanagan's presentation on Tuesday: https://www.w3.org/2024/04/AC/ac-agenda.html#tuesday - really good.

* [Sustainability](https://github.com/w3c/strategy/issues/420)

Dan: We discussed the fact that the current CG report is quite long and parts of it may not be testable... So some concerns there about introducing a document that is not implementable... whereas what we have tried to do with Privacy Principles and Design Principles is to have actionable advice... I think the overall feedback should be something like: we support sustainability as a goal - however there is a lot of work to do to take the current CG report and make it into something actionable... 

Amy: I think I agree...

Matthew: one of the concerns we had - depending on the task trying to be solved, some of this stuff might not be possible. I agree with the overall feedback. We want to support... we could work with them more closely to result in more actionable stuff. Lot of peripheral discussions about serialization formats, etc... we should encourage but they need that feedback to help them focus.

Yves: I can look at the minutes from last month and find the previous discussion.

#### [triage new design principles issues](https://github.com/w3ctag/design-principles/issues) 
#### [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion

Needs Max.

#### ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456) - @torgo, @matatk

Matthew: can work on this tomorrow

#### [Terminology jumps away from principle's subject ("Use care when exposing identifying information about devices")](https://github.com/w3ctag/design-principles/issues/479)

punt to tomorrow

### Breakout B (California / Europe)  - [2024-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240603T153000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Martin, Peter, Yves, Amy

Regrets: 

#### [triage new design principles issues](https://github.com/w3ctag/design-principles/issues)

*assigning some old issues*

#### [PR 476](https://github.com/w3ctag/design-principles/pull/476)

Reviewed and merged. Related issue opened on Privacy Principles.

#### [PR 485: Attempt to split attribute by type](https://github.com/w3ctag/design-principles/pull/485)

Martin: we have a suggestion from Anne but I don't think "content attributes" is helpful terminology.

Yves: we should check with Lea on this one

Amy: ultimately this is editorial and an improvement on what's there. Maybe not get hung up on further changes?

Peter: they do raise a point that HTML attributes rules out SVG and MathML

Amy: could we add a dfn of HTML attributes that notes it also includes SVG and MathML?

Peter: we do use the term HTML attribute in a lot of other places. Would be hesitant to add a PR that adds a new term and doesn't change the other uses of HTML attribute.

Martin: I only changed one section which was the most ambiguous. In some cases HTML attributes is reasonable... the getter ones stops using attribute entirely for the most part, besides an IDL attributes.

Peter: fine with merging, and opening another issue about relpacing HTML attribute

Marin: I'll open it

Peter: my suggestion for a replacement would be DOM attribute

*merged*

#### [New principle: Incremental user effort should result in incremental value (or more)](https://github.com/w3ctag/design-principles/issues/473)

Amy: sounds reasonable... add "write me"?

*assigned to Lea for now*

#### [New: Avoid revealing that consent was denied](https://github.com/w3ctag/design-principles/issues/475)

Closed by earlier PR 476

#### [New principle: HTML attributes can affect semantics](https://github.com/w3ctag/design-principles/issues/478)

Amy: couldn't figure out if there's consensus or what on in the thread

Has been triaged earlier, leave it to assignees..

#### [New principle: Events should only fire during actual state transitions](https://github.com/w3ctag/design-principles/issues/483)

Martin: this seems reasonable, just needs someone to do the work. Lea is assigned.

Yves: examples of antipatterns?

Martin: an update thing.. an event fired on every update in one of these proposals and I don't think it stayed that way because the feedback was received.

Yves: Render capacity api.. is linked.

Martin: don't send an event when the state doesn't change, only when it does

#### Design Principles Abyss Clearing
  * [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov
  
Martin: there's a list of things that would all be broken as a result of someone requiring that a particular piece of behaviour runs to completion... the potential for two discrete apis to ahve a dependency between each other that creates an expectation for people calling those apis that it's atomic.. I think the request is reasonable. Don't break peoples expectations about how things are implemented by requiring constraints that are not guaranteed.
  
Peter: ready to write?

Martin: unclear. Anne's framing is interesting. People need to be able to treat promises like values and not have any expectation that when the code that might fulfil that promise runs, whether it be colocated or not ... but I'm not sure I could say anything confident about this.. with all the state .. micromanagement tasks that we have..

Peter: is this a design principle or the promise guide? Not sure if it has an active editor. Not sure that moving it over there would result in anything happening

Martin: might still be better than leaving it where it is, given how many of us necessarily have the expertise needed

Peter: Rossen did ask that in 2022...

Martin: perphas the principle is that if an object is restricted in that way it must not escape out into other execution contexts. Eg. if you are making a call to something you expect to be synchronous or time limited, you have an object, and some task of your own that runs at some point in the future that invalidates that object... I wouldn't do that, but. Something to do with audio and video.

Peter: could we ask jan ivar to write a PR? Assign to Marin to shepherd?

Martin: *nods* I think there's disagreement. Maybe a PR will elicit some reactions.

  * [New principle: Avoid exposing API that result in synchronous flushing of CSS or layout](https://github.com/w3ctag/design-principles/issues/388)
  
Peter: ties into a long standing thing about describing the html loop. I don't know that anything has ever happened. CSS WG agreed to take that up... but looks like it's in CSS's abyss.

Amy: is there a minimum viable principle here based on the feedback we gave the Range API?

Peter: the original sin is getelementwidth as a sync method which requies you flush all of style and layout in order to compute that. We're saying don't do that any more. If you need to flush style and layout do it asynchronously. I still think there's a dependecy on ... we need to have something to point to to say don't break this.

*assign Peter*

### Breakout C (California / Australia) - [2024-06-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240603T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [[WIP] add forwards compatibility / graceful degradation principle.](https://github.com/w3ctag/design-principles/pull/468) - @hober
* [First pass at #453 (text-based syntaxes should be designed for humans####https://github.com/w3ctag/design-principles/pull/472)
  * [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453) - @LeaVerou, @torgo, @hadleybeeman
  * [New principle: when to use permissions, when to use user activation, and what if neither are adequate](https://github.com/w3ctag/design-principles/issues/341)
#### [HTML: Receive complex data via JS or element subtrees?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou
#### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober
#### [New principle: The value of HTML boolean attributes doesn't matter](https://github.com/w3ctag/design-principles/issues/451)
#### [New principle: When introducing heuristics or "magic", also include a way to override them](https://github.com/w3ctag/design-principles/issues/455)

### Breakout D (California / Australia) - [2024-06-04](https://www.timeanddate.com/worldclock/converter.html?iso=20240604T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369) - @torgo
#### [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391) - @LeaVerou
#### [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou
#### [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)
#### [New principle: Document whether to add things to Document, Navigator, Window, or SomeOtherInterface](https://github.com/w3ctag/design-principles/issues/448)
#### [New principle: Consider many & diverse use cases to avoid overfitting](https://github.com/w3ctag/design-principles/issues/450)

### Breakout E (Europe / China) - [2024-06-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240605T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [Restrictions](https://github.com/w3ctag/design-principles/pull/363) - @maxpassion

Max: content of the PR - examples and refernece policy link need to be updated... as well as remove... I have made these changes and submitted a PR...

Dan: [requested change from Sangwhan](https://github.com/w3ctag/design-principles/pull/363/files#r831947583) - We agree to accept this change though GitHub UI is not working to do this right now...

Dan: removes [ref to document policy](https://github.com/w3ctag/design-principles/pull/363/files#r1627128051)...

Dan: adds Lea to reviewer list... 

Dan: let's revisit at the plenary...

#### Abyss clearing
  * [New principle: Remove deprecated functionality responsibly](https://github.com/w3ctag/design-principles/issues/361) - @torgo
  
Dan: I'm wondering if we should close this... rationale being: if we introduce a new principle which is at odds with an existing spec or implementation we don't want to appear that we are "gandparenting" that in... e.g. geolocation spec was not requiring https... then we had "securing the web" finding... we didn't say "ok except for geolocation"... 

Matthew: if something is a security risk than it can be chanked... https was a massive security improvement... also Martin mentioned we switched to newer versions of ssl etc... that doesn't change the API.. but when we were in London for the f2f - we had a discussion about removing stuff... 

https://www.w3.org/TR/design-principles/#removing-features

Dan: [leaves comment](https://github.com/w3ctag/design-principles/issues/361)
  
  * [New principle: Deployability and Monitoring](https://github.com/w3ctag/design-principles/issues/368) - @torgo
  
Dan: [anne has good comments](https://github.com/w3ctag/design-principles/issues/368#issuecomment-1144690252) 

Matthew: what has happened in the last couple of years... 

Dan: we do have a [privacy principles](https://github.com/w3ctag/privacy-principles/issues/150) issue that we closed... and about monitoring and telemetry .. a lot of it is in [ancilary uses](https://www.w3.org/TR/privacy-principles/#ancillary-uses)...

*we agree we need to re-read what we put into privacy principles and maybe we can close this issue on that basis .. punt to plenary*
 
#### [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454) - @ylafon

Yves: I think it's putting some text to reference another document - I will check and make a PR.


#### [Harmonize with WebAppSec Powerful Features Draft](https://github.com/w3ctag/design-principles/issues/481)

Dan: I did some work on this yesterday ... and I'm still working on it...

Dan: we need to haromonise ...

Matthew: what do we think about the definition?  As I recall one group had a definition that powerful features are gated behind permissions and we said "powerful features should be gated behind permissions"...

Dan: they say "A powerful feature is a web platform feature (usually an API) for which a user gives express permission before the feature can be used."" and in fact I think this is a bit circular... We [say](https://www.w3.org/TR/design-principles/#require-user-activation) that "Some powerful APIs can produce intrusive UI (eg. auto-playing audio), expose user data (eg. interacting with the clipboard), perform a background activity without an obvious indicator to the user (eg. accessing local storage), or prompt the user to interact with trusted UI (eg. permission prompts, device hardware features)." 

Dan: [opens issue](https://github.com/w3c/permissions/issues/451) in their repo.

### Plenary Session - [2024-06-05](https://www.timeanddate.com/worldclock/converter.html?iso=20240605T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Tess, Yves, Matthew, Amy (1st half)

#### Appointments Brouhaha

Dan: I feel we should develop some TAG consensus about what changes we would like to see (small tweaks) that we could discuss at the joint meeting coming up in July.

Matthew: as it is a ratification, changing the threshold to reflect this fact could be a really simple thing to do... so people *really* have to be concerned to stop it from passing...  We should go with solutions not just problems. (Others suggested this before me; I agree though, and maybe that has consensus within TAG?)

Tess: I feel that time should be talking about changes... 

#### Joint meeting at Seattle

Peter: TAG related stuff is currently scheduled for afternoon...

#### [Add principle on use of delta seconds](https://github.com/w3ctag/design-principles/pull/467) (close?)
  * [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
#### [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457) - @hober
#### [Proposed charter: Linked Web Storage (née Solid) Working Group](https://github.com/w3ctag/tracking-issues/issues/79)
  * [the new charter](https://www.w3.org/2024/05/proposed-linked-web-storage-wg-charter.html)
  * [a summary of the changes that were made (or not made), with our rationale](https://www.w3.org/2024/05/solid-new-charter-changes.html)
  * [the old charter](https://www.w3.org/2023/09/proposed-solid-wg-charter.html)
  * [diff (old vs. new)](https://services.w3.org/htmldiff?doc1=https%3A%2F%2Fwww.w3.org%2F2023%2F09%2Fproposed-solid-wg-charter.html&doc2=https%3A%2F%2Fwww.w3.org%2F2024%2F05%2Fproposed-linked-web-storage-wg-charter.html)
  
Logged in, I don't have permission to access [the summary](https://www.w3.org/2024/05/solid-new-charter-changes.html) - Amy  
  
#### Breakout Rollup

##### [New principle: Deployability and Monitoring](https://github.com/w3ctag/design-principles/issues/368) - @torgo

Dan: Can we close on the basis that we already talk about this in https://www.w3.org/TR/privacy-principles/#ancillary-uses?

Tess: they're kind of both right and both wrong... there is a real privacy concern about software that phones home and also there's a real need to find out info when software crashes...  You can tailor the information sent... 

Tess: i feel with [the privacy principles text] that is suffciient.

<blockquote>
In the time since this issue was opened, some [new text](https://www.w3.org/TR/privacy-principles/#ancillary-uses) has been added on this topic to the Privacy Principles document which feel covers these cases.  Hence we're going to close this.  If people feel there is need for additional text in the Design Principles doc for this issue, please raise a PR. 
</blockquote>

**closed with comment**

##### [powerful features](https://github.com/w3ctag/design-principles/issues/481)

Tess: we could "squat" on the dfn... Anne is not wrong when he's talking about shared array buffer... 

Dan: Maybe "dangerous" is better...

Matthew: re: geolocation ... we have a design principle – says "the web app should not be able to distinguish between a capability not being available and a user declining permission" but the geolocation suff - an app knows when you've pressed cancel...  so that seems to violate that principle... Do we all agree on that?  

https://www.w3.org/TR/design-principles/#device-ids 
also
https://w3ctag.github.io/design-principles/#consent

*matthew to open issue on geolocation API repo*

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


