

## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/10-17-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2022-10-17](https://www.timeanddate.com/worldclock/converter.html?iso=20221017T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro
* [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro
* [Early Design Review: Page Unload Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia
* [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

### Breakout C (APAC / Europe) - [2022-10-18](https://www.timeanddate.com/worldclock/converter.html?iso=20221018T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Privacy Draft
* [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon
* [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon
* [Output Device Selection in Web Audio API: AudioContext.setSinkId()](https://github.com/w3ctag/design-reviews/issues/766) - @torgo, @maxpassion
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion
* [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon

### Plenary Session - [2022-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20221019T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Minutes

Present: Dan, Lea, Amy, Yves, Peter, Rossen, Tess

Regrets: Hadley, Sangwhan

### Breakout A (Europe / US) - [2022-10-17](https://www.timeanddate.com/worldclock/converter.html?iso=20221017T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Lea: no updates - no responses... Someone said they'd ping Yoav?

Dan: i will send a note to Yoav

#### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Lea: last time they pointed to a document saying why they made this an attirubte... 

Rossen: I will set it up.

#### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @rhiaro

#### [FileSystemHandle::remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @rhiaro

*punt until we can discuss with Tess*

#### [Early Design Review: Page Unload Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia

*punt to next week*

#### [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov


### Breakout C (APAC / Europe) - [2022-10-18](https://www.timeanddate.com/worldclock/converter.html?iso=20221018T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Max, Yves, Rossen

Regrets: 

#### Privacy Draft



#### [Fetch streaming upload](https://github.com/w3ctag/design-reviews/issues/754) - @torgo, @maxpassion, @hadleybeeman

Max: they responded - in the explainer they've added a section talking about the benefits. Some end user benefits. 

Dan: I think the discussion is editorial. Do you have concerns about the api?

Max: I don't have other concerns

Dan: we could close this **closes with comment**

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Dan: Previous review: https://github.com/w3ctag/design-reviews/issues/649 - lots of issues raised regarding complexity. What has changed? No signal about multi stakeholder. Not clear how they've addressed feedback from our first request. *leaves comment*

#### [FileSystemHandle Unique ID](https://github.com/w3ctag/design-reviews/issues/764) - @ylafon

Amy: is this releated to the other FileSystemHandle issues?

Yves: sent a comment saying it looks like UUID-URNs and didn't hear back. It's different from the other issues.

#### [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon

Dan: left feedback last week.

Yves: we gave them a pointer to the minutes. Waiting for the feedback. The issue was about opening too much.. using unrestricted * and only that. I can reping at the end of the week.

#### [Output Device Selection in Web Audio API: AudioContext.setSinkId()](https://github.com/w3ctag/design-reviews/issues/766) - @torgo, @maxpassion

Max: the author responded to last week's comment and provided information

Dan: it's a compelling argument. Worrying that they're saying there's another feature of another api that would partially solve the problem but it isn't implemented in browsers so that's why they need this. Why isn't in implemented? Maybe it should be deprecated.

Amy: and why would this be implemented in browsers instead?

Dan: they're working on web audio. There's this other thing that's happened in a different WG. That's media capture which is part of webrtc

Max: they also mention in the last sentence - *even with* that .. 

Dan: generally we were happy with this other than that. There is the fact that it has multiple stakeholders..  It does talk about a user need. Privacy review.

<blockquote>
  Thanks for this review request. We're happy to see this move forward and we're espeicially glad to see it do so with multiple stakeholder support and the attention to privacy considerations. We are slightly concerned that some of the functionality is duplicated elsewhere in the platform, however we undertand the different context.  Can you please move the explainer into a markdown file in the appropriate repo?  
</blockquote>

**agreed to close**

#### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Amy: user need not specified... explainer also doesn't really say how it works

Max: agree to add this to the explainer

Yves: do they have list of differences between VISS 1 and 2?

Amy: I'll look over what we've reviewed in the past and leave a comment

**comments to be left asking for clarity**

#### [Delta review (to CR) of Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/771) - @cynthia, @maxpassion

Max: first, the naming of synchornised and async method. They had a discussion in their WG and it seemed they were unable to reach consensus, that's why they asked us. Two naming proposals. The second part is to ask the TAG to review about the design choices they restrict the sync api to worker only. Rare exception design on the web platform, that's why they want to confirm with us. 

Dan: they're really looking for a response on naming in particular.. 

Max: after looking at WG discussions, maybe first naming is more suitable. They summarized: in the future the api will be async so it's not necessary to .. the default behaviour should be async in the future. So the first..

Dan: Sangwhan should also weigh in. Could you have that discussion with Sangwhan to get feedback, then if you have consensus you could leave that comment.

[come back to this at plenary]

#### [updated URI syntax for IPv6 link-local zone identifiers](https://github.com/w3ctag/design-reviews/issues/774) - @torgo, @ylafon

Yves: looks okay, but need to understand more

### Plenary Session - [2022-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20221019T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### Privacy Draft

Amy: did an edit pass....

**discussion on privacy and advertising**

Peter: if people are going to claim that advertising can be targetted in a privacy prserving way then they need to prove that.  So far we haven't seen that proof.   Som studies have shown that targeted advertising doesn't work ... 


#### [Early Design Review of Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

Dan: I note it's shipping in Chrome 104. 

Dan: the work they've done [addresses concerns](https://github.com/w3ctag/design-reviews/issues/767#issuecomment-1233369118) that were raised by the TAG previously...

#### Breakout Rollup

Rossen: on Popup - organizing a joint call...  we don't have responders to the doodle yet.  Next session "a" slot 2nd half.  

Amy: on Vehicle Service Spec I left a [comment](https://github.com/w3ctag/design-reviews/issues/768#issuecomment-1283597164) asking them for more information... 

Yves: https://github.com/w3ctag/design-reviews/issues/774 still looking at it.

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
