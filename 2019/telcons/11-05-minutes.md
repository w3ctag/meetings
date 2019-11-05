## TAG Teleconference
##### 05 November 2019

Chair: Dan

Present: Hadley, Kenneth, Dan, David, Sangwhan, Lukasz, Alice, Peter, Yves

Regrets: 

Scribe: Hadley + others

---

Agenda:


* [Triage Parade](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22) 

Triaged, assigned to TAG members and set milestones for [issues 429 - 439](https://github.com/w3ctag/design-reviews/issues/).

* [Raw Clipboard Access API](https://github.com/w3ctag/design-reviews/issues/406) - @hober, @torgo, @hadleybeeman

Torgo: (Reviews progress)

... How can we escalate this? Shall we invite (tech lead) Alex Russell to a call?

Hadley: that works. it's important we have this discussion on the record. We have a responsibility here, since we're talking about trading off user privacy against functionality.

David: I'm concerned about this too. Another important use case is users having passwords on the clipboard, and we don't want sites to get access to those.

Torgo: Are there other mitigations we can suggest? 

David: agree about user activation.  Need something that gets user consent each time.

Tess: webkit gates the async clipboard api on user activation

Torgo: I'll take an action to invite Alex to come join us on the 26th

* [[WebComponents] Custom state pseudo class](https://github.com/w3ctag/design-reviews/issues/428) - @hober, @kenchris, @plinss

Kenneth: boolean only - most people using web components are not so interested in looking at other use cases...

Peter: it's true that the vast majority of these pseudoclass state things are boolean. No problem with that. My issue is that their API is geared towards only boolean state and it would be awkward to extend. and there are use cases for expanding it. Would like to see API surface that is future friendly.

Alice: he's saying : don't think non-boolean should be considered as an extension.  ... each one would be a custom function rather than a non-boolean value.

Peter: the custom function thing is a nonsequitor to me. ... nowhere am I talking about extending this to cover that use cases.

Alice: isn't this being able to extend it?

Peter: if they're not state related then you might just hook a function at selector matching time - ...

Kenneth: he says "we don't need to support non-boolean states".. but "a state change event could be added."

Peter: a state change event doesn't help CSS authors...  E.g. paper slide exposing the state of the slider...  for example, in a thermostat with a "sweet spot" and danger bands - so multiple states...  I will reply with that ... 

Alice: not a map but implemented as a map... that might also be worth mentioning.

Peter: if it's a map then let's make it a map.

Alice: if they've considered that and not done it, it would be good to understand their reasoning for it.

Torgo: There is a point of limited return, where the TAG, having no formal power, needs to say "you heard us, we're on the record,"

Kenneth: "...we agree to disagree"

* [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @cynthia, @alice

[bumped to 19th]

* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @kenchris

[bumped to 19th]

* [Microtransaction payment handlers](https://github.com/w3ctag/design-reviews/issues/422) - @dbaron, @kenchris

Torgo: let's organise a breakout on this.

...[creates label for breakouts]

* [Default accessibility semantics for custom elements](https://github.com/w3ctag/design-reviews/issues/401) - @hober, @dbaron

Dan: any reason why we should not just close this?

Tess: it seems fine but that is not a thorough review

Alice: [recusing]

David: i am fine to close it

[agreed to close]

* [Translate Attribute](https://github.com/w3ctag/design-reviews/issues/301) - @hadleybeeman, @dbaron, @torgo

Hadley: we need to discuss this with him (Dave).  Alice is organising it for next week - for the call.

---



