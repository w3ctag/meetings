## TAG Teleconference
##### 10 October 2019

Present: Lukasz, Peter, Hadley, David, Yves, Alice

Regrets: Kenneth, Dan, Tess

Scribe: David

---

Agenda:

* [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @cynthia, @alice
* [Service Worker Scope Pattern Matching explainer](https://github.com/w3ctag/design-reviews/issues/417) - @cynthia, @torgo, @kenchris
* [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394) - @dbaron, @kenchris
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman

---

### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

David: looked at issue, not sure whether it's worth more now or waiting (per Adam's comment)

Hadley: How are they doing an origin trial if there's no draft spec?

(some discussion of origin trials and continued changes to specs)

Peter: could close and ask to reopen when they have more

David: or alternatively maybe I should look a little more now... 2 weeks?

### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301)

Hadley: discussed recently?

(looks like we discussed it 4 weeks ago)

Hadley: (reads chrishtr's [last comment](https://github.com/w3ctag/design-reviews/issues/301#issuecomment-537765252))  Still seems like it's changing relationships: putting the referring site in the position of being the user agent.  I feel like we keep going in circles on this.

Hadley: Also 4 comments up... misses that what we meant by "one browser" is that the only browser team involved is Google.

Hadley: Fundamentally I think this is from the ethical principles -- just not the way we think things work.

Alice: curious what you thought of chrishtr's answers to the second quoted question in [this comment](https://github.com/w3ctag/design-reviews/issues/301#issuecomment-537741688)

Hadley: As someone who cares about Privacy, it frightens me that we would transfer responsibility for knowing my preferences to the website.  He says relying on the UA only is too limiting to know what preferences are, works against openness, decentralization, and choice.  It doesn't in the way I think about those terms.  I feel like his last sentence about "smart sites" is useful but very different from offering suggestions to the next site.

Hadley: I'm stuck -- we already closed this "unsatisfied"; that's what I keep coming back to.  I think we're fundamentally on different pages here about how the web works.

Peter: I'm also consider the explanier suggests it would influence the `Accept-Language` HTTP header... which it really shouldn't be doing.  

Hadley: Have we written that down?

Peter: Not sure.

Hadley: We had in our feedback a year ago, from Paris... we talked about `Accept-Language` from the UA as an alternative.  So I don't think it was in the explainer then.

Peter: I agree it's the wrong design; I don't see anything convincing me otherwise.

Alice: how convinced are you about the use cases they've explained?

Hadley: not convinced because the way I'm reading the use cases, they're use cases about developer of one website wanting more control about what happens on another website.

Peter: Only thoughts are either (a) close again or (b) invite Dave to a call to try to explain to us what we're missing?

Hadley: I'm up for that.

Alice: I could...

Hadley: Did we have a call with him before?

David: I think so.

Peter: I'm happy to if we think it would make progress.  Make the offer... leave it up to him?

Hadley: I don't remember chrishtr being in the discussion then -- maybe a conversation with both would be useful?

Alice: I'm happy to ask if they could join us.

### [Modal window](https://github.com/w3ctag/design-reviews/issues/427)

Peter: Alice, Anything we should talk about here?

Lukasz: Security questionnaire looks very interesting.  I think it's not finished yet.  Look at the answer to parts 2, for example.  Still .5 -- in progress.  Not sure what long term implication of introducing this new context.

Alice: I see that Marcos had commented that he intended to have a look and needed a few days.  Over to WICG discourse... I guess involved in that?

Alice: ? and Sangwhan also wanted to have a look... bump this for next week, and capture Lukasz's comments?

Alice: Comment if they want to finish filling out the security questionnaire?

Alice: ... I can do that if Lukasz isn't.  Lukasz, did you want to comment about the security and privacy questionnaire, or shall I?

Lukasz: I can comment!!

Peter: Bump this to next week, when hopefully rest of the folks are here.

### Call time

We're continuing with this call time, although next week it will be 1 hour earlier for Americans since they end summer time this weekend.
