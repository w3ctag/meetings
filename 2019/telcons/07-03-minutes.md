# TAG Telecon 3 July 2019

Present: Dan, Alice, Tess, David, Yves, Lukasz
Regrets: Sangwhan, Kenneth, Hadley, Peter

Chair: Dan
Scribe: Alice

## Agenda

Updates to questionnaire - @lknik
Privacy Mode Finding - @lknik
WebTransport - @cynthia, @dbaron, @ylafon
Badging API - @hober, @torgo
JSON modules - @hober, @cynthia, @dbaron, @kenchris
Import maps - @cynthia, @kenchris
Element Timing API (images and text) - @dbaron, @kenchris
Event Timing API - @dbaron, @kenchris
CSS Properties and Values API Level 1 - @hober, @alice, @dbaron
Feature Policy JS introspection API - @cynthia, @kenchris

### [Updates to questionnaire](https://w3ctag.github.io/security-questionnaire/) - @lknik 

A few lexicographic changes, markup changes, and that's it.

Do we want to close the issue?

https://github.com/w3ctag/security-questionnaire/issues/48

Dan: Sangwhan had some thoughts on this, so let's wait to get his perspective.

David: I comment during the May meeting but I can't remember what I commented.

Dan: It should be ok to republish an update if the only changes were editorial, but we might wait to actually close the issue.

Lukasz: I have been (thinking) on a blog post... ??? asked if he should be a co-author...

Dan: Ok. CC sam (?) on that email so we have good communication.

Lukasz: I' already in touch with Jason...

### [Privacy Mode Finding](https://w3ctag.github.io/private-browsing-modes/) - @lknik

https://github.com/w3ctag/private-browsing-modes/issues/2#issuecomment-507602956

Dan: This seems fine to publish.

Lukasz: Ok, I'll update this.

Dan: We already resolved to publish this at the Reykjavik meeting. I think we should publish this and then move forward together with PING.

... Yves said that he would help get this published. I'll try and follow up with him and you later today.

Lukasz: In the meantime I will up (?) this link.

~ yves appears ~

Dan: Yves, I just committed you to getting the privacy finding published after lukasz adds a little bit of text editorial.

### [Badging API](https://github.com/w3ctag/design-reviews/issues/387)

Tess: Alice & I met on this. Alice posted our feedback on the issue 3 hours ago. feedback on the issue 3 hours ago.

Alice: ...some more worked through code examples. .. notes in comment... didn't answer is it possible to have different instances one one app... proliferation of libraries... In the navigator issue - issue 14 - I brought it up again... 

Tess: Part of what confuses me about that is they are putting off using this from a service worker until the future, but in the wild the common "per-app" case they seem to want to address right now is the add-to-home-screen scenario, where you may reasonably expect there to be a service worker (and it may want to update the bage number when the app isn't active).

Dan: is the feedback being taken on board?

Alice: the navigator feedback yes.  I will talk to them about other feedback.  ​​​​​​​

### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon​​​​​​​

David: I started...

... to look at this this afternoon. It's pretty substantive. They're working on two specs, one defining protocol in IETF and one defining web APIs in WICG. And an explainer and three email threads. The first chunk of my comment was noting that the explainer felt a little short and asking if they could go deeper and explain how the parts fit together. 

... Seems like this is still somewhat in flux, e.g. integration with Streams. In flux, "early review" status.

... Did yves get a chance to look?

Yves: I haven't had a chance.

Dan: Should I bump it? Organise a breakout?

David: Yes a breakout would be good. I was supposed to do that last week and I failed. It's across three continents.

Dan: I'll bump this to the 17th.

Dan: Good luck organising a breakout! l o l

### [JSON modules](https://github.com/w3ctag/design-reviews/issues/375) - @hober, @cynthia, @dbaron, @kenchris

Dan: This didn't have a milestone associated with it, but I was looking around to see if there was anything here... I was talking to Jory about TC39 earlier this week, and this was marked as TC39, so it seemed like we should take al ook at it.

Dan: Jory [Burson] and I were talking about doing a TAG/TC39 confab at TPAC to look at issues like this one. 

... Tess WDYT

Tess: I have only looked at it far enough to triage & add some labels.

Dan: David, you're also assigned.

David: As of 90 seconds ago, yes.

Dan: Ok. Seems like we need to bump this but start thinking about it. This kind of spans different venues.

Tess: Similar to CSS modules, but JSON can't import so they would all be leaf nodes in the graph.

Dan: Seems like something that Sangwhan and Kenneth might have a particular interest in. Will bump it a week.

... And I'll follow up with them and see if they want to add anything.

### [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris

Dan: Neither of them are here so we should bumpp this one too.

### [Element Timing API (images and text)](https://github.com/w3ctag/design-reviews/issues/326) - @dbaron, @kenchris​​​​​​​

(And [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324))

Dan: Was there a breakout..?

David: I was supposed to and I didn't :(

... I have been being productive and ignoring my to-do list.

Dan: Will you be able to get one organised?

David: Let's bump this two weeks because I suspect holidays will interfere this week.

... Same goes for the next topic (Event Timing API - @dbaron, @kenchris)

Dan: Are they blocked on us?

David: Not that I'm aware of

### [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron

[we examine the state of the issue]

Alice: we could follow up asking for the new proposal....

Tess: i can get feedback from colleagues

David: this spec is about css property extensibility - turn custom properties into something that looks more like a real css property. Some of the discussion regarding scripting... could be scary.

[discussion of Alex's comment]

Tess : lots of concerns...

David: a thing that might be interesting to explore int the future...

Alice: issue with the (lack of) explainer...

Dan: user need needs to be better documented...

David: easier to polyfill css properties with higher fidelity.

Alice: has the ship sailed?

[Alice took action to find out implementation status and leave comment if appropriate - we will circle back in a week]