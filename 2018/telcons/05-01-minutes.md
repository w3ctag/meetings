## TAG Teleconference
##### 01 May 2018

Present: Peter, Kenneth, Travis, David, Alex, Hadley, Lukasz

Regrets: Sangwhan, Dan, Yves

---

Agenda:

* [Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225) - Lukasz, Dan, David

Lukasz: We had a discussion on this on Github; whether is makes sense to limit transitivity of permsission. If we give iframe access to geoloc, can it delegate to another iframe? Could be possible to limit adding iframes-in-iframes (which would limit delegation). My position: we should limit transitivity of permissions.

David: At risk of restating what's been put in github and minutes: Why not do this? These are easily defeated; and the workarounds are usually worse. Usage will come from Libraries, e.g., thing for inserting a Google Map. If these couldn't delegate further, they would have to include script into their own origin (rather than use an iframe), which has worse security principles. Or they might make a postMessage protocol, which is worse for performance. We can offer an API, but can't force it to be used a certain way. We shouldn't offer a security property that we can't guarantee.

Lukasz: comes down to the business logic of what is being nested in the iframe.

Alex: Yes, I see you can build a postMessage protocol... Yes, Google Map is a good example. They put a script from another origin into their origin (implicitly trusting it). I'm focused on the extend that a content develoepr does want to delegate--what are their tools? Delegation as currently designed is a very blunt instrument (it's all or nothing). Since it could be constrained, there no way to ensure it can't be abused. I'm "pro" limiting transitivity, but I get hung-up on feature detection.

Alex: Also, we will try to meet with Raimes Cory (spelling?) next week.

David: If it's clearly documented as "not doing what you think it does"... If we're saying here's what it actually does, you must depend on these invariants... then maybe OK?

Alex: I'll point out today that nearly all this happens with full trust. 

Peter: Is it possible to envision a way to further restrict it to make it more useful? Should we start down this path without making it

Travis: Would be nice if there was a way to provide a two-way handshake (so that both parties have to agree)? Or that delegated permissions flow upstream to the original delegator(s) for approval?

Alex: Would like to be able to revoke a permission. There's no way to do that in any direction today. 

Lukasz: Is there no way to have selective delegation? (what happend if top document looses permission, are the iframes/sub-iframes loosing access immediately?)

David: Could be interesting to delegate and then revoke your own permission as a way of least-priveledge.

Alex: A real capability model would be useful (like an object-based capability), that could be granted, and transferrable.

Peter: bumping to next week for follow-up

* [Keyboard Map](https://github.com/w3ctag/design-reviews/issues/238) - Travis, Sangwhan

Hadley: Reviewed [the issue on Incognito mode](https://github.com/WICG/keyboard-map/issues/16), and seem satisfied with the responses. Gary's analysis seems sensible; I'm not aware of a better fallback mode than keeping the feature consistent. I also like the idea of letting a UA override that if they choose (presumably with the user); that lets a particularly privacy-conscious browser offer the user different choices ("You are in Germany; do you want your keyboard to return DE-QWERTZ in incognito mode?")

...Also worth noting that "not revealing info about the user" isn't the only purpose for privacy modes. It's useful that Gary makes it clear that's what he has in mind.

* [CSS Selectors 4, :focus-visible.](https://github.com/w3ctag/design-reviews/issues/233) - David, Travis, Peter

David: As of yesterday, no edits yet--let's skip.

* [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232) - Dan, Yves
* [CSS ::part and ::theme pseudo elements](https://github.com/w3ctag/design-reviews/issues/230) - David

David: See previous comment about no edits yet.

* [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224) - Travis, Dan, David

Travis: Waiting for me to file additional issues (from my big comment).

David: Discussion happened about Promises/Generators. Nervous that the change to Promise timing and microtasks might be necessary in the Layout worklet.

Kenneth: The folks writing layouts may be able to live with using Generators. I don't think that Promises are going to fix the issue (of being easier to use).

Peter: Issue is still open; I expect future discussion.

Alex: We want to make sure the spec delivers on its goals
* Developer ergonomics
* Object types vs property bags
* Text shaping (is not included but should [eventually] be possible)

* [Web Components Guidelines](https://github.com/w3ctag/design-reviews/issues/227) - Kenneth

https://docs.google.com/document/d/1mT5xD3kDQURKy5CYTackQDxvRhGMCcn-EfBR6zATX1k/edit#heading=h.6noqmk1wlqtv

Kenneth: Was asked to prepare a doc (see above). I focused on components that could be standardized. Pleast take a look; will then discuss what we want to do next.

Kenneth: You'd create a component that *could* be integrated if it became popular.

Alex: This could give us enough info that the component could be upgraded into the standard.

Peter: (on #5) Question on that? Is it worth telling people not to do that? It's not necessarily visible on the outside.

Kenneth: Specific part of light DOM would go into different places in the parent's DOM

Peter: We have wanted to do that with native elements and now that we can do it with custom elements we might be able to bring that back into native HTML elements

* [Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/235) - Alex, Peter, Travis, David
* [Async Clipboard](https://github.com/w3ctag/design-reviews/issues/222) - Travis, Alex

Peter: Still hope to see some movement on the issues...

Alex: Can ask Gary to follow-up.

* [Web Speech](https://github.com/w3ctag/design-reviews/issues/214) - Hadley, Travis

Travis: Do we still want to move into WICG to try to drum-up interest?

Hadley: We can move our thoughts into Wendy's strategy funnel...

David: There's an issue in the strategy funnel: https://github.com/w3c/strategy/issues/71

Travis: I can copy our architectural thoughts there, and then close the issue.

* [task scheduling](https://github.com/w3ctag/design-reviews/issues/72) - Travis, David


---



