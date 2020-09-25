## 09c (Peter and Rossen)

### [Web Share API](https://github.com/w3ctag/design-reviews/issues/554)

Discussed the overall share API and how it fits into the platform. In order to get the larger picture we also looked at how the Web Share Target API and provided the following comments.

In review with @plinss during our Cork virtual f2f, we are assume that this is the respective explainer that goes with that design review. 

In general we like the concept and approach to it. The following is a summary of some concerns we have.  We will also open as individual issues in your repo.

The current API exposes a single global share promise and it is unclear why this is needed. This global appears to clutter the navigator space while also being exposed as a return parameter. Can we remove it?

Is the share method better exposed as an interface between navigator and the share method (e.g. Share interface) making it easier to integrate with the share target API or any other share capabilities. From extensibility and future-proofing point of view, having such interface will save us from having to add more methods to navigator in the future. 

The contents of the ShareData dictionary is tied to the File API. This makes it a requirement to implement File API before you can have Share API. A user might want to share an image directly from their camera feed which is still a blob. It would be good to explore exposing lower level block in addition to a file.

One more observation close to the file vs blob comment is about exposing capability to share different formats. Examples of such extinsibility could sharing a Calendar, vCard, and other structured data that can be useful to users - JSON of user contact info for example.

## Breakout 11c (Peter and David)

### ["With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76)

Reading issue 76 and https://w3ctag.github.io/with-credentials/ and https://github.com/whatwg/fetch/issues/517

David: My memory from 3 years ago is perhaps that I thought `public-deauth` was the one that seemed possible and I thought `public-auth` was too risky, which is the reverse of what 517 suggests.

We can't figure out how to make progress here; changing from "pending external feedback" to "stalled".

### [IntersectionObserver](https://github.com/w3ctag/design-reviews/issues/197)

David: added [comment](https://github.com/w3ctag/design-reviews/issues/197#issuecomment-698013370); we should probably close this

### [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172)

...looking at previous minutes and fantasai's blog post...

David: We don't have principles on layout system design now -- is this the one principle we want here, or should we hold off on adding it?

Peter: How was this meant to be extended to HTML?  Is it just presentational aspects of HTML?  Does `<details>` defaulting to being closed violate this principle?  Not sure we want to assert that.

David: Could go in the existing CSS section, I guess.

Peter: We don't have an HTML section, do we?

David: No, but I was thinking we would.

(David drafts a little bit of text in the issue)


## Breakout 17c (Alice and Rossen)

### Personalisation

Alice: Analogy with CSS?

How are these annotations intended to be consumed? Browser extensions?

`purpose` attribute seems to largely share a vocabulary with `autocomplete` - why not just use that attribute for whatever personalisation purpose `purpose` is intended for?

Rossen: this is getting into microformats territory?

Overlaps with several existing technologies.

Alice: Recipe microformat example: http://microformats.org/wiki/hrecipe

... uses the `class` attribute.

Rossen: The meta-language they're adding is targeting many scenarios in an inconsistent way... content descriptors such as destination are intended for the user agent to enhance the experience... `symbol` is intended for use by AAC tools.

... More generic ones like `action`...

Alice: `action` seems semantically close to `role` - kind of a secondary role?

Rossen: The inconsistency bothers me... say I'm writing a tool, do I need to pay attention to all of these attributes? Use case seems to be mainly for writing browser extensions.

Alice: destination : link :: action : button

... `purpose` is redundant with autocomplete

Rossen: What does `destination=phone` do? Does it pop up a dialer?

Alice: Could use a usage example for each vocab value.

... seems like `email-recipient` and `phone` are redundant with `contact` in this context - when would someone put them on separate pages?

... `distraction` property has an overlap with reduced motion preferences

... Many of the values for `distraction` - `messages`, `offer` and `overlay` - seem to be patterns that are aimed at generating revenue, so it seems unlikely that sites would voluntarily allow the user to easily disable them.

... `sensory` is the remaining one, which seems to have a strong overlap with `prefers-reduced-motion` preferences.

Alice:

- The research here is very thorough, and there are very real user needs addressed.
- It would be good to see some examples of how the proposed vocabulary would be consumed, particularly for some of the less obvious values.
   - Specifically, what types of tools would consume these values, and how? Extensions? AAC tools? Specialised user agents?
- It seems like this proposal is aimed at overlapping but distinct sets of users - it might be helpful to separate these out a bit, and explain how each set of users would be served by what subset of these vocabularies, and where the intersections are. It might make sense to have a few different technologies instead of one single standard.
- We wonder if you've researched [microformats](microformats.org) as a potential avenue for providing the hints described in the vocabulary of the content module. That seems to be a potentially good fit for the types of annotations we're seeing here, and would avoid needing to reserve an attribute prefix in HTML.
- We note that `purpose` seems to have a near 100% overlap with the [`autocomplete` attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete) - could whatever is intended to consume `purpose` use `autocomplete` instead?
- `distraction` unfortunately seems largely geared at allowing users to remove content which is intended to generate revenue for the site - why would a site voluntarily make it easy for users to hide that content?
    - `distraction=sensory` is a slight exception to this, but has strong overlap with the [`prefers-reduced-motion` media query](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion) - could its intended uses be covered by that existing technology?
 


Rossen: There is a mix of intended users of the data that is proposed here. UA, AAC, AT, extensions.

Alice: Might be worth addressing this on a per-need basis, and then also noting the intersections.

Rossen: "... provides web content authors ... persons with various cognitive and learning disabilities ..."












