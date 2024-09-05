# TAG Minutes - week-of 2-September 2024

## Agendas:

### Breakout B (California / Europe)  - [2024-09-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240903T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [Vibration API](https://github.com/w3ctag/design-reviews/issues/971) - @martinthomson, @torgo, @matatk

### Breakout D (California / Australia) - [2024-09-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240903T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober
* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion
* [Spec review for scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/966) - @hober, @martinthomson
* [Design Review: Prioritized Task Scheduling (big picture)](https://github.com/w3ctag/design-reviews/issues/967) - @hober, @martinthomson
* [Explainer explainer: Ask people to list non-consensus dependencies in their explainers](https://github.com/w3ctag/tag.w3.org/pull/40/files) - @jyasskin

### Breakout E (Europe / China) - [2024-09-04](https://www.timeanddate.com/worldclock/converter.html?iso=20240904T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @martinthomson, @LeaVerou
* [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk
* [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou, @nitot

### Plenary Session - [2024-09-04](https://www.timeanddate.com/worldclock/converter.html?iso=20240904T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
  * Actions taken
    * https://github.com/w3ctag/tag.w3.org/pull/40 merged.
    * Support Video Chapter in MediaMetadata closed.
    * Spec review for scheduler.yield() closed.
    * Commented on Captured Surface Control
    * Commented on Add Skip-Ad media session action.
  * Draft consensus comments
    * Controller documents
    * text-wrap: pretty
    * Vibration
    * Explicit JavaScript Compile Hints
* [Private discussion repo](https://github.com/w3ctag/design-reviews/pull/987)
* Breakout scheduling: avoid Monday morning & help Max attend Breakout D?
* TPAC breakout(s)
  * [The future of TAG reviews](https://docs.google.com/document/d/1ZlqM1W5HIkF2rNsnXE5MY7v8cSMRwAMkz2p6KyMVZRA/edit)
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout B

Present: Jeffrey, Amy, Lea

Regrets: Dan, Yves, Matthew

#### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman

Draft comment by @jyasskin

<blockquote>

We appreciate this effort to make the bag-of-keys functionality that Verifiable Credentials use more independent from the did: URL scheme. Beyond that, we're not confident that other systems will find much use in it, since the effort of profiling it is likely to be larger than the effort in defining a bespoke format. There is also a risk that defining a generic format will introduce security vulnerabilities into specific applications when libraries implement the generic format and fail to enforce the restrictions that those specific applications need. We've seen this in the past when generic JWT libraries allowed alg=none or symmetric keys in applications that were designed for asymmetric keys. While those specific flaws don't exist here, analogous ones might.

We were happy to see that this document doesn't try to define a format that can be interpreted as JSON and JSON-LD at the same time. Some of the [discussion in issues](https://github.com/w3c/controller-document/pull/43#pullrequestreview-2261617341) has been worrying on that front — it sounds like some implementers might be intending to include `@context` properties, parse documents as JSON-LD using hash-pinned values for those `@context` URLs (which is better than not pinning them), and then interpret the result using an unspecified (though logical) mapping from URLs to the terms that this specification defines. We are concerned about such an implicit interoperability requirement that isn't captured in the format's specification, and we're concerned that attackers will find ways to exploit the complexity of JSON-LD context processing. We're also skeptical that JSON-LD provides benefits for a format designed for grouping cryptographic keys: interoperable extensibility can be achieved through IANA registries at least as well as through individually-owned URL prefixes.  (We recognize that the DID WG sees registries as too-centralized, but we disagree.)

Some of us are concerned about the inclusion of multihash and multibase. We all think it's best to mandate that all implementations of this specification align on a single cryptographic digest algorithm and a single base encoding, to improve interoperability. We're split on whether it's a good idea to use the multihash and multibase formats to make those strings self-describing.

We don't see some security considerations that we were expecting to see:

* It seems risky, at least in some cases, to say "https://some.url/ defines the keys that can approve changes to this document" without pinning the content of https://some.url/ either by hash or signature, and we don't see any facility in this specification to do that pinning. Where would that be defined?

* If one controller document creates a "verification relationship" to "https://actor1.example/key1", can a hostile actor include a verification method in their controller document with "id": "https://actor1.example/key1" and cause their key to be trusted? https://www.w3.org/TR/2024/WD-controller-document-20240817/#retrieve-verification-method does say to fetch every verification method URL with no caching at all, but it seems unlikely that implementations will actually omit all caching.

</blockquote>
  
#### Tooling for drafting comments

Mirrored github thread for async review work is a good idea.

We need to ask Peter where the agenda generating script is so we can make sure the link to the mirror thread goes into the minutes.


#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

Jeffrey: filed an issue with CSSWG. Tess suggested a more obvious name. Chrome said it's too late to change the name. Close to closing last week. Should we argue more?

Amy: would arguing more make a difference?

Jeffrey: only if other engines agree but they haven't weighed in. Name comment was a year after the issue was opened, so a bit late.

Lea: all we had are concerns..

Jeffrey: Lea left a comment last year... 

Lea: they said pretty has orphan control plus this niche thing that only applies when you're doing justification

Jeffrey: I don't know if they shipped the rivers control. It changes how hyphenation works, and they did ship that (and got a complaint in the CSS discussion). An author wanted to do just orphans and not change hyphenations

Lea: that's what I was saying! They can't just ship this bag of things without shipping the individual knobs as well. People end up using pretty as a proxy for them. 

Jeffrey: and now they can't, but also don't have the individiual knobs. Florian didn't like the idea of the individual knobs

Lea: I don't understand the problem with the individual knobs. it can't be that tricky to implement, just syntax

Jeffrey: I think Florian's worry was they then have to specify how the knobs interact with each other and authors will want control over how much do we sacrifice hyphenation in order to get a better last line, balancing the various things. Pretty just asks the UA to do something sensible.

Lea: this is a solved problem. There are already typesetting problems... how dothey do it? No checkbox in indesign called Pretty. There is control over the individual knobs but it's not a problem

Jeffrey: indesign is generating a page, doesn't have to be responsive to widths... not an expert in typesetting

Lea: anything that does the typesetting once is not a great example for perf, but in terms of exposing the knobs we can look ... prioritisation between different knobs and how conflicts are resolved. Does that affect perf?

Jeffrey: I don't know. I'd guess not.

Lea: if it doesn't, I don't see why we can't look at how existing software has solved this with a lot more years of experience into what people want from typesetting

Jeffrey: CSSWG should have this discussion. We should close on our end.

Lea: true. Satisfied is that we agree there's a pain point, concerns are we don't like how this is being solved. Pretty sure we haven't used satisfied with concerns for this in the past

Jeffrey: I don't feel strongly

Lea: eg. picture in picture. 

Jeffrey: [Florian's objection](https://github.com/w3c/csswg-drafts/issues/3473#issuecomment-1744086855)

Lea: balance seems like a low level knob, not sure how you'd decompose that. We didn't say _only_ do the individual knobs.

Jeffrey: it actually doesn't sound like they're firmly opposed to adding the individual knobs, just not ready yet. So shipping pretty was dangerous as long as it just controls one thing. But now it controls two it's less dangerous. people who only want to control orphans will run into problems.

Lea: the second thing it controls only applies in a very specific case?

Jeffrey: I think hyphenation shows up not only when you're justifying text

Lea: I suppose there's a lot of correlation between hyphenating text and using this property. There's a design principle about high and low level features. Here they've shipped the high level feature first and I'm not convinced there is enough knowledge of what authors want, so I suspect pretty is going to end up changing over time and we'll run into web compat issues.

Jeffrey: so we're worried this is going to change in the future because we don't know what authors need, and that will cause web compat issues, and we'd like the CSSWG to revisit this.

Lea: yeah. Good line breaking is about a lot more than limiting hyphenated lines in a row and avoiding orphans. It would be an excellent name for a whole algorithm with smart line breaking.

Lea: We don't have a good sense of how intensive the final performance will be

Jeffrey: will continue to work on this comment after the call

Draft comment:

<blockquote>
  
While we recognize that the author pain points this is designed to solve are real and prominent, we still have several concerns about this solution, both in terms of its current definition, and its timing.
  
In general, shipping high level features is a good idea when 
a) we have a good idea of what a good solution to author needs would be (either by first shipping low level features and observing how they are used OR because the solution is so obvious that this step is not needed) or
b) the corresponding low-level features would be very tedious to use to produce the same result.
  
In this case, neither of these appear to be true: we do *not* have a good sense of what `text-wrap: pretty` should end up doing in the end, and it currently only corresponds to two very specific features, that would not be tedious to set individually.
  
[One author's reaction](https://github.com/w3c/csswg-drafts/issues/3473#issuecomment-2032718416) to this feature appears to validate this concern: they wanted control over orphans and are frustrated they have to accept re-hyphenation to get it.

Given this, we are concerned that the behavior of this feature will need to change a lot over time, and that after a certain amount of adoption, those changes will either break web compatibility, or will require a high enough performance cost that browsers won't be able to ship them. We encourage the CSSWG to:
  
1. keep working to expose the lower-level features so authors can request them directly (e.g. if their intent is to avoid orphans, they should be able to express this without having to resort to a feature that combines it with other things).
2. work on a plan to ensure that implementations can eventually ship a truly-pretty line-wrapping algorithm even if that turns out to be expensive.
3. consider whether the completely open-ended specification for `text-wrap: pretty` ("[Specifies the UA should bias for better layout over speed, and is expected to consider multiple lines](https://drafts.csswg.org/css-text-4/#valdef-text-wrap-style-pretty)") was the right way to get engines to ship evolvable and eventually-compatible implementations.

We think the CSSWG is the right place to pursue those goals and that parallel discussion within the TAG won't help anyone. Thus, we're closing this as `Resolution: unsatisfied` with the acknowledgement that solving the above problems would likely turn this into a `satisfied` resolution.

</blockquote>

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Jeffrey: meant as an accessibility thing... 

Lea: had some concerns about the design.. but also saw excitement from webcomponents people

Jeffrey: it's incredibly needed, my worry is it's across more things than just accessibility... problems with shadow dom and links to #foo not scrolling.. CSS has some similar problems.. deal with in a different way, might not be IDs

Lea: the whole syntax of using id refs of linking elements to other elements is broken and we want a better way to link to other elements, it's not just about aria, it's also about developer ergonomics. Web components authors don't have a good precedent to follow. Assigning ids to everything produces very poor experiences for authors. One one hand this is solving a very prominent pain point, on the other hand my sense is that it's solving it with a bandaid. Also something that needs to be solved asap. Waiting to solve the bigger problem is also suboptimal

Jeffrey: yes. Should generally support this, but describe the overall problem and ask people to keep thinking about how to solve the general problem. Gaps repo!

Lea: exactly! I wrote a [post in whatwg](https://github.com/whatwg/html/issues/10143) about this, I need to edit and post there. [Narrator: It was already posted: https://github.com/w3ctag/gaps/issues/2]

Lea: we also don't have standardised api about how this corresponds to idl attributes. Value, or reference to element... or two idl attributes for value and element.

Jeffrey: accessibility folks using that setter as a way to cross shadow boundaries ... ?? is opposed to crossing the shadow boundary ... to be continued.

Lea: hes' going to have to revise his perspective because there's a ton of use cases

### Breakout D

Present: Martin, Jeffrey, Tess

Martin merged https://github.com/w3ctag/tag.w3.org/pull/40.

Should we move this breakout an hour later so Max has a chance of attending? [No conclusion]

* [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober

Tess says this is ok, and closes it.

Martin: This might subsume the need for a "Skip Ad" API.

* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Martin: Security considerations doesn't include "why we excluded click". In one world, the captured application might know it's being captured, so it could guide the process. Then you could pass through the fact that there's a scroll request, or even clicks. The problem is that that shouldn't be the only mode since some applications might decide not to cooperate. That could be considered a good thing.... So the design you have here where the events are indistinguishable. 

Jeffrey: Telling the page can remove the user's control.

Jeffrey: Could get both, but you'd have to ask the user, which is hard to build UI for.

Martin: Having the page decide can be seen as a good thing.

Posted comment:

<blockquote>

Thank you for bringing this to us. We think this seems like a generally useful feature, but we have some questions and suggestions for the explainer:

The explainer should discuss the alternative design of having the page cooperate, and accept dedicated events from the capturing process. We think there are both upsides and downsides to that option that deserve exploration.

The two interactions that are considered are scrolling and zooming.  Is that list exhaustive?  Are these uniformly safe to do?  Are there not occasions where scrolling results in changes to things like form elements?  That could require a change of focus before sending the events in, maybe, though with precise X and Y on events, that might still engage the element that is targeted.  We're inferring that this is limited to those two actions because "spoofing" those events is safe, but the explainer doesn't give enough details to show that that's true.
  
There seems to be some heightened permissions UX being contemplated here.  It's not clear to us what would be different from a regular screen capture.  It would be helpful if the explainer could show a proof of concept that highlights those differences.
  
</blockquote>

Posted: https://github.com/w3ctag/design-reviews/issues/962#issuecomment-2327555698

* [Spec review for scheduler.yield()](https://github.com/w3ctag/design-reviews/issues/966) - @hober, @martinthomson
* [Design Review: Prioritized Task Scheduling (big picture)](https://github.com/w3ctag/design-reviews/issues/967) - @hober, @martinthomson

The interaction with requestAnimationFrame and render (bad name) needs to be better resolved.  That is, do these functions belong in the scheduler or do they belong on the thing responsible for the handling (which calls into the scheduler underneath)?

yield is fine.  Are we OK with how it fits into the broader picture?

Draft [yield](https://github.com/w3ctag/design-reviews/issues/966) comment, with `Resolution: satisfied`:

<blockquote>

The `yield` piece of the scheduling project looks good to us, with the caveat that if the rest of the scheduling project doesn't pan out, or if the different scheduler bits end up hanging off of other objects, we'll need to come back and rename `scheduler.yield()` to avoid having it hang off of an otherwise-empty object.

</blockquote>

* [Vibration](https://github.com/w3ctag/design-reviews/issues/971)

Maybe we should have a full Haptics API instead.  However, browsers have given the advice that APIs should not be fully generic, making this a bit weird. Though vibration is really a weaker version of haptics.  Haptics being more powerful and general.

Maybe the security/privacy thing should recommend disabling sensors that might be affected by vibration while vibrations are active.


Draft comment (not posted yet):

<blockquote>
  
Given the proposal to obsolete the Vibration REC and 2 browser engines' reluctance to implement it, we wonder if there's another direction that could attract more interoperability. For example, would enough use cases be served if browsers could treat the device they're running on as a gamepad (https://w3c.github.io/gamepad/#gamepadhapticactuator-interface)? We think it would help everyone evaluate this API if the WG would write an explainer for their current direction, including a list of use cases and alternatives that you've considered.
  
</blockquote>


### Breakout E

Present: Tristan, Martin, Yves, Matthew, Amy

#### [TAG review for web app scope_extensions](https://github.com/w3ctag/design-reviews/issues/875)

No progress to report.

#### [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951)

Question open to Lea about color spaces stuff in CSS.  Architectural desire to ensure that color is treated consistently across the platform.

This really needs to be taken to the Media WG.  A gist is not really good enough.

Is the name "copyTo" the right name?  Or is this a color space transform?  Are there other transforms that the platform should support?  See [The Design Principle issue on naming](https://github.com/w3ctag/design-principles/issues/507).

#### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954)

Tweaked the labels, but this is waiting on authors/proponents.

#### [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957)

Martin: we talked about this this morning... parallels to chapter metadata... could be more generic feature to skip _something_ when the concept of chapters is added. This may fit with Peter's earlier feedback.

Tristan: Like the idea of being generic and useful for multiple purposes.

Martin: could have a `skippable` attr with a cause, which could provide the string for the button. This oculd improve consistency with UA controls.

Matthew: from an accessibility perspective my biggest concern is how people reach the buttons and how they are rendered.  I realized that this is a much deeper issue.  I'll check the review of the spec as a whole and the TAG doesn't appear to have reviewed the whole thing (MediaSession, that is).  (Wrong history?)  This is pretty old, but it has only ever been a working draft.  We should have seen it in APA, but we don't seem to have.  Correction: APA did look at it a long time ago and it probably needs another look.

<blockquote>

Firstly, we need to ask whether this was implemented in browsers *other than* Chrome.  If it wasn't, this presents an opportunity to improve it.

One desire we have is to make this feature generic, rather than being specific to skipping ads.
  
We observe that the [Media Chapter](https://github.com/w3ctag/design-reviews/issues/952) information (that we recently reviewed) might provide a useful hook for this sort of control.  "Chapters" that are skippable can be marked as such in that metadata.  The type of thing to skip might be included in that information.  Consider `{ ..., skippable: "ad" }`.  That would allow for skipping of intro sequences and credits in addition to ads.

For accessibility purposes, this sort of thing might need to be given a symbol so that non-textual users are able to more readily access the function. Please consult an accessibility expert about this (@matatk indicated that APA is likely to want to take another look; it's been a while since they reviewed the original MediaSession proposal).

</blockquote>

#### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970)

No progress to report.

#### [Early review request for "Explicit JavaScript Compile Hints" #947]

> Thanks for bringing this to us.  The TAG doesn't have a ton of experience in this area, so we're not in a great position to help.  The question of venue is a critical one here.  We disagree with your assessment that this doesn't belong in TC39.  This seems pretty firmly in that domain.

Propose to decline with something like that in the comment.


### Plenary

Present: Jeffrey, Dan, Martin, Matthew, Tess

Regrets: Peter, Hadley

#### Rollups - 

From B:

Jeffrey: wrote a draft comment on controller documents... 

Martin: I like it...  maybe not far enough on multibase but that's ok...

Tess:  on tontroller docs I think we should post it.

Dan: let's post it.

Jeffrey: I checked it with Amy and they did not object.

From D:

Jeffrey: text.pretty, also javascript compilers...

Tess: I also think the text pretty comment looks good- I am happy to close as satisfied...

*agree to ship text.pretty comment [above] and close as 'unsatisfied'*

*we agree to post the draft comment [above] on vibration API*

From E:

Martin: we did some triage … a bunch of things where nothing has happened … we talked about skip ad … we looked at new issues. We tried to triage *explicit javascript compile hints* and sort of concluded we should decline this one. It's  big and we may not be qualified.... 

Matthew: we propose to direct them to the web performance wg.

Jeffrey: consistency question - optimisation structure via comments - it's a little weird... 

*we wordsmith the closing comment; will continue wordsmithing offline and then post*

Matthew: about explainers and about triaging for fedcm reviews... For explainers - we agree to change something in the issue review template... adding a link to the explainer documentation there as well... I think our explainer page is good but the key link is to the template... Nitpicky things... we could change the way the review request is worded - url rather than markdown with text [url]. 

Martin: we talked about in E... A PR on the repo... 

Matthew: let's make the link to the explainer more prominent ...

*Matthew to work on a PR on explainers*

Matthew: to triage thing... We looked at a few things to triage... 

##### FedCM Discussion

* FedCM early review request (following our meeting with Sam Goto): https://github.com/w3ctag/design-reviews/issues/974
* Newer lightweight FedCM issue (which I sense TAG may prefer): https://github.com/w3ctag/design-reviews/issues/986

... Note at the top of 974... my suggestion was to ... if we want to close 974 ... that this was htem building the bridge...

Martin: the point of the discussion was... if we do conclude that the lightweight one was good.. lightweight one be used... then point to all of them in the set... "we have thought of these things.. we think this one is better because xyz"... 

Martin: lightweight approach not as fully featured and requires a different style of integration... so some view it as complementary and some view it as a replacement.

Jeffrey: ... not sure... reluctant to close the heavyweight FedCM reviews ...

Martin: ... rrelated to issues like IDP not wanting to present a deadname ... since it's been cached in the browser... we discussed this and there is a solution...  It may not be totally acceptable to the IDPs but it may be sufficient...

Martin: lightweight one says the IDP can register an identity... the full version gives the IDP the ability to do cross-site cookies but there is a whole protocol --- IDP needs to stand up http endpoints... more complex.  User manifestation is essentially the same... web site has button "log in with IDP" - you press a button and bunch of identities pop up... 

#### Idea of parallel discussion repositories...

*we agree to trial this*

#### TPAC breakout

Let's what should TAG review look like in the future draft... 

#### Brekout scheduling...

Breakout D is too early in the morning... So should we move that one later... current time might not work for Beijing...

Breakout B timings ... if we move that breakout a day later it would be easier ... 
