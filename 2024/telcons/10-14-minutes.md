# TAG Teleconference
#### 14-16 October 2024

---

## Agenda:

### Breakout A (California / Europe)  - [2024-10-14](https://www.timeanddate.com/worldclock/converter.html?iso=20241014T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk
* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou, @nitot
* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk
* [FYI Private State Token API Permissions Policy Default Allowlist Wildcard](https://github.com/w3ctag/design-reviews/issues/990) - @jyasskin
* [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou
* [[HTML] Canvas place element](https://github.com/w3ctag/design-reviews/issues/997) - @hober, @matatk
* [CSS Scoping; :has-slotted](https://github.com/w3ctag/design-reviews/issues/999) - @hober, @LeaVerou, @plinss
* [Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @hober, @LeaVerou

### Breakout B (California / Australia) - [2024-10-15](https://www.timeanddate.com/worldclock/converter.html?iso=20241015T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @plinss
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [Early design review: Future browsing context group dependency hint](https://github.com/w3ctag/design-reviews/issues/979) - @hober, @martinthomson
* [Multiple import maps](https://github.com/w3ctag/design-reviews/issues/980) - @jyasskin, @LeaVerou
* [Realms Initialization Control](https://github.com/w3ctag/design-reviews/issues/985) - @jyasskin, @plinss
* [Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @hober, @martinthomson
* [CSS Selectors 4; :local-link](https://github.com/w3ctag/design-reviews/issues/998) - @hober, @jyasskin, @LeaVerou

### Breakout C (Europe / China) - [2024-10-16](https://www.timeanddate.com/worldclock/converter.html?iso=20241016T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion
* [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk
* [Document-Isolation-Policy](https://github.com/w3ctag/design-reviews/issues/995) - @martinthomson, @torgo
* [Review for CR transition of WebAssembly specifications for version 2.0 features ](https://github.com/w3ctag/design-reviews/issues/1002) - @torgo, @matatk

### Plenary Session - [2024-10-17](https://www.timeanddate.com/worldclock/converter.html?iso=20241017T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Tristan, Peter, Yves, Matthew, Jeffrey, Lea

Regrets: Dan


### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk

Still waiting for a reply from proponents.

### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman

They've sent a bunch of PRs, and we (Jeffrey) need to review those.

### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Jeffrey: [summarizes the TPAC discussion from https://www.w3.org/2024/09/25-webcomponents-minutes.html#da4f] We should endorse the first phase, and maybe we can help with the design for the second phase where they have some open questions.

Matthew: +1. Thinking about prior art for phase 2.

Jeffrey: I was surprised that we don't want to follow the `data-*` pattern, but there seems to be consensus against using hyphens. I'll also find the minutes from TPAC.

Matthew: Think about how this affects the general gap on IDREF in shadow trees.


Peter: Is it right to put the property on the shadow root, or better to put it on the target element inside the shadow root? Seems like it might be better ergonomics if the right target inside the shadow tree needs to change, since you'll probably be updating that element's attributs anyway. Could expose the map at the root as readonly.

Matthew: This might be consistent with the rest of ARIA, where relations are sometimes backwards from HTML.

Peter: That's a mistake in ARIA.

Matthew: Doesn't make this comment invalid; it might just apply more generally. Although it has helped implementation for assistive technology.

Peter: If the browser is helping out, it can expose the right accessibility tree.

Matthew: Should we file a more general issue?

Peter: Start with posting the comment here.

Peter to draft the comment.

<blockquote>
Have you considered reversing the relationship of the shadow root to the target node? For example, rather than having the developer set the `referenceTarget` on the shadow node, introduce a `aria-referencetarget` (or some equivalent) attribute which is set on the target node? The shadow root can still have a `referenceTarget` attribute but it's read-only and can be a reference to the actual node.

I'm thinking of the developer ergonomics, for instance if I'm building a select-type control, in the current model I have to set some attribute (probably a class) on the currently selected node to indicate its selected state and trigger style changes, and then I have to also add an id and set the `aria-activedescendant` in the reference map on the shadow root. In my proposal, the developer would only need to set the `aria-activedescendant` attribute on the active node (which can also be used as the style trigger) and the reference map can update automatically. This also eliminates the need for ids on everything. 
</blockquote>

Posted to https://github.com/w3ctag/design-reviews/issues/961#issuecomment-2411812056

### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou, @nitot

Lea: I have some qualms. `<link>` does a variety of things, some of which are CSS. It worries me that we keep adding things to this element that are only relevant to CSS. Not just `layer`. `supports`, `scope`, etc. Would these be better served by having an attribute that passes attributes to particular technologies. But the use cases are pervasive, and I don't want to block them. Not sure it's a great design, but it can move forward.

Jeffrey: I get the sense from WHATWG discussions that it's better to just add the attribute with a short name rather than inventing a microsyntax to scope it exactly right.

Peter: It also works on the `<style>` element, and we'd like `<link>` to be consistent. But maybe we want to do it in the linked thing?

Lea: Problem is that we've overloaded `<link>` too much, which we now have a design principle against. Should have been `<style src>`

Peter: How about the Link header?

Lea: Don't think it works for new things.

Jeffrey: Good comment to leave, that this should also work in the Link header.

<blockquote>
We like this, and we're happy for the WHATWG to figure out the exact name and details. Our one concern is that the `Link` header should behave the same as the `<link>` element.
</blockquote>

[After the meeting, Jeffrey discovered that `Link: <>;rel=stylesheet` isn't actually specified to work at all (https://html.spec.whatwg.org/multipage/links.html#table-link-relations), so there's no need to make it work for `layer` attributes.]


`Resolution: satisfied`:
<blockquote>
We like this, and we're happy for the WHATWG to figure out the exact name and details. Thanks for working on it!
</blockquote>

### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

Matthew: Haven't reviewed this yet.

### [FYI Private State Token API Permissions Policy Default Allowlist Wildcard](https://github.com/w3ctag/design-reviews/issues/990) - @jyasskin

Postponed to Breakout B.

### [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou

Jeffrey: It seems confusing that Animation.progress would be the overall progress over all iterations, while getComputedTiming().progress would only return progress over the current iteration. They should have different names.

Jeffrey: https://github.com/DavMila/explainer-animation.progress?tab=readme-ov-file#time-driven-animation doesn't look compelling to me: you need some trigger to call updateInfo(), but a progresschanged event defeats a lot of the purpose of putting animations into CSS in the first place, that they can run more efficiently and off-the-main-thread.

Jeffrey: Similarly, https://github.com/DavMila/explainer-animation.progress?tab=readme-ov-file#scroll-driven-animation seems roundabout and should show the code an author would use to show a scroll percentage without using animations. IIRC, it's possible to use animations to set an element's contents, although it's a bit tricky and breaks copy/paste. Maybe the proponents should work on that instead?

<blockquote>

The explainer doesn't justify this feature well enough. It presents two use cases: one for showing a percentage through a time-based animation, and another for showing a scroll percentage.
  
The time-based animation has two issues:
1. It doesn't say why the developer is writing code like this in the first place.
2. It doesn't show how `updateInfo` would get called.  A big reason to do animations with CSS is to get them off the main thread, but this seems to require interrupting the main thread periodically to change the text.

The scroll percentage code doesn't show the "before" state? What would the code look like if you only used `scrollTop` to measure progress and draw the meter? Is using animations simpler or more performant here?

It's possible but complicated to render text directly from an animated property: https://dev.to/madsstoumann/clocks-countdowns-timing-in-css-and-javascript-554n. Maybe the use cases for `Animation.progress` would be better served by making that easier to use?

Finally, if you do need a property for this, it seems confusing to have two `.progress` properties with different meanings (within-iteration for `getComputedTiming().progress` vs overall for `Animation.progress`). Please find a different name for the new meaning.

</blockquote>


### [[HTML] Canvas place element](https://github.com/w3ctag/design-reviews/issues/997) - @hober, @matatk

Matthew: This is really interesting. Could be pretty helpful. People use `<canvas>` to render a whole webapp. Instead of using HTML elements, they draw pixels, so it's not accessible, but they want exact control over appearance. Can put fallback elements inside the canvas. They don't get rendered, but they're available to AT. This allows you to put those elements on the canvas in a particular place. They say it's great because it'll be good for accessibility. That aspect does sound good. Concerned that use cases aren't explained well enough, because if you're using canvas to avoid native elements, why would you use this?

Jeffrey: We should ask them to explain the use cases, if they're not clear enough in the explainer. I'm pretty sure they'd have a partner who's interested in using this, but they might not have _enough_ partners.

Matthew: It's sometimes not enough to show a particular element for example if the focus indicator actually lives on one of its ancestors. They said you could use this for a menu in a game. But if you're placing things at particular pixel locations, you're doing a lot of the layout yourself, and what if the user has changed the base font size? They talked about "and its children", so maybe you wouldn't place menu items. That should be made very clear to developers.

Jeffrey: Can we point them to a particular accessibility group?

Matthew: Point them to APA. We might point them toward the ARIA people. We have the TAG question about use cases, in addition to the accessibility question. I'll post a comment this evening.

### [CSS Scoping; :has-slotted](https://github.com/w3ctag/design-reviews/issues/999) - @hober, @LeaVerou, @plinss

Lea: Think this is ready. It's a pseudo-class that applies to `<slot>` elements when they have assigned nodes. We ought to make `:slotted` a combinator so you can use `:has()` for similar things, but we still need something that catches text nodes. Didn't call it `:fallback-displayed` because there's no guarantee that it has a fallback.

Peter: Seems like an no-brainer. My only "hmm" is a vague memory of doing this without the pseudo-element. 

Lea: You posted the original proposal: https://github.com/w3c/csswg-drafts/issues/6867.

[`satisfied` with](https://github.com/w3ctag/design-reviews/issues/999#issuecomment-2411841675):

<blockquote>
We discussed this in a breakout today and we don't see any architectural concerns with this, so we're happy for this to move forwards.
</blockquote>

Lea: Side-note: I don't like when the CSSWG uses pseudo-elements to address real DOM elements. It introduces a host of ergonomics problems that would not otherwise exist.

Peter: I'd like `::part()` to be replaced by a way for the shadow tree to define its own pseudo-elements.

Lea: I'd like `::part()` and `::slotted()` to be replaced by ways to target real elements, e.g. special combinators to expose other elements. But that's a very big conversation that we cannot have in 5 minutes. 

### [Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @hober, @LeaVerou


## Breakout B

Present: Peter, Tess, Martin, Jeffrey

Regrets:


### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @plinss

Punting that.  Call on Monday.

### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

We spoke at TPAC and there is no new information.

### [Early design review: Future browsing context group dependency hint](https://github.com/w3ctag/design-reviews/issues/979) - @hober, @martinthomson

They got back to us; the end of [their comment](https://github.com/w3ctag/design-reviews/issues/979#issuecomment-2403549065) says the following:

> WebKit's bfcache implementation does not require BCG changes. While this would be ideal for all bfcache implementations, it is unfortunately infeasible (at least for the chromium implementation).

Tess: If this is a Chrome-only problem, shouldn't they simply pursue a Chrome-only solution? Why standardize something at all here?

Jeffrey: If we do nothing, Chrome might ship this.  Does this matter?

Martin: Firefox does this too.

Peter: This might pollute the web with unnecessary API surface.  Sites might become locked into depending on this implementation quirk.

Tess: Sites can come to depend on Chrome's behavior.  No obvious risk from this, but that might lead to issues.

Action on Martin to check with Gecko.

### [Multiple import maps](https://github.com/w3ctag/design-reviews/issues/980) - @jyasskin, @LeaVerou

<blockquote>

We looked at this today, and it seems like a very nice improvement to the platform. The devil will be in the details, of course. It looks like you're working those out in the right place. Please keep doing that, and good luck.

</blockquote>

Then a question:

If querying the map causes the queried mapping to be fixed (otherwise, the introduction of a new mapping will result in a change to the already-retrieved mapping) then does that not potentially lead to non-deterministic outcomes?  The value of mappings will depend on the order of import map availability and queries to the import map.  This is partly addressed by the fact that a module graph uses a consistent mapping, but that doesn't help at the top level where the loading order of modules might not be deterministic.  Also, why should a miss (a mapping that a module graph attempts to resolve, but fails) be treated differently, as it appears to be?

Jeffrey: This and https://github.com/w3c/tpac2024-breakouts/issues/31 / https://github.com/WICG/webcomponents/blob/gh-pages/proposals/css-modules-v1-explainer.md seem related, unless I'm mixing up module maps and import maps.

<blockquote>

At first glance, this looks great. We had a few questions:
  
* As we understand it, the requirement to ensure that a mapping cannot change is hard to meet.  It looks like a resolved mapping has the effect of fixing that mapping so that new additions to the map don't change it.  How do you avoid nondeterminism?  We see that you require the mapping to be stable while loading a module graph, but what about between different graphs?  We're thinking about top-level async module loading here and we're not clear on how this might interact with that.
* If a mapping is used, but does not resolve successfully (perhaps because no mapping exists) is that a state that needs to persist?  Why is that safe?
* The discussion in https://github.com/w3c/tpac2024-breakouts/issues/31#issuecomment-2387141476 seemed to indicate that server-rendered custom elements would want to add inlined CSS modules to the module map as they're sent to the client. Does that need support from this proposal, and if so does this proposal support it? cc/ @justinfagnani @rniwa
  
</blockquote>

### [Realms Initialization Control](https://github.com/w3ctag/design-reviews/issues/985) - @jyasskin, @plinss

https://github.com/mozilla/standards-positions/issues/1062#issuecomment-2412451522 is fun

<blockquote>

We're very concerned about a belief that one can make Javascript secure against hostile Javascript by running first. We think WebAppSec and TC39 have relevant experience in this space, and you should make sure they're both happy with this before going forward.
  
</blockquote>

### [Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @hober, @martinthomson

In theory we're starting a finding on that, but not all of us are making progress.

Lots of new developments, perhaps we can continue to wait on that basis.

### [CSS Selectors 4; :local-link](https://github.com/w3ctag/design-reviews/issues/998) - @hober, @jyasskin, @LeaVerou

This name is confusing, but apparently not everyone thinks that.

We'll discuss in Plenary: should Jeffrey's issue be "promoted" to coming from the TAG and not just himself? (Everyone present in this breakout believes we should.)

### [FYI Private State Token API Permissions Policy Default Allowlist Wildcard](https://github.com/w3ctag/design-reviews/issues/990) - @jyasskin

Not clear that this is OK, but the problems are likely inherent, rather than a result of this change.

Consider asking for privacy review to validate the claim that calling this API doesn't have a significant privacy cost.

## Breakout C

Present: Hadley, Martin, Tristan, Liu, Dan, Yves

Regrets: 

### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Still waiting on proponents to respond/etc.  Time to ask monseigneur Yasskin to apply the obligatory amount of force to colleagues.

Dan: *pings Jeffrey to ping colleagues* let's revisit at the plenary.

### [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk



### [Document-Isolation-Policy](https://github.com/w3ctag/design-reviews/issues/995) - @martinthomson, @torgo

Martin: the goal is to allow access to shared array buffers - 

Dan: the risks are to do with cross-proccess attacks with high-resolution timers... 

Martin: timing attack related stuff ...

Dan: what is the user need?

Martin: being able to deploy your wasm code... you've got a popup with some code, some of the code is wasm, you want to use shared array buffers... but you can't use it because ... The user benefit here would be that the app would use less of the battery, cpu, etc... because it's able to use the more efficient version of the code...  There's a lot of work here .. and a lot of use of mechisms that maybe shouldn't exist... 

Dan: example?

Martin: like not partitioning popups... 

Martin: key example - cross origin isolation breaks the communication ... you have an iframe, that opens a popup window, then that window is able to communicate back.

Yves: payment is one use case.

Martin: ... use cases that involve cryptography ...

Yves: this could always be misused for [advertising]...  Reading the explainer - it's possible to do this but they want to remove it for security reasons...

Martin: but wouldn't be able to access coi restricted APIs...

Yves: allowing this capability... you open up another process to avoid timing attacks... 

Martin: i don't like these things without going through the negatives...

Yves: all efforts around restricting sharedarraybuffer... it's done by patching and patching and patching ... 

Martin: they want to restore the ability to do cross-origin communication... if you isolate something then you want to be able to communicate it still... but question on whether that should be allowed - the reasonable one is : if you COEP something it can't embed something... it would be seem reasonable to loosen the restrictions on COEP if you isolate...

Dan: we could get them along to a call...

Martin: first thing to do might be ask something... In the explainer (though it's a lot) there is no discussion of the trade-off. They want to change the way cross-origin isolation works so...


> Questions:
>
> We're still struggling a little bit with the explainer here, but there are a few things you might add to help us a little.
>
> 1. What is the user need that this addresses?  There is some mention of performance benefits in your writeup here (~40%! \[citation-needed]), but that isn't really substantiated.  Can you give us some examples of real-world scenarios in which this would be used and provide material end-user benefit.  In particular, why do these applications need to jointly use popups and this sort of arrangement? In "use cases" you list "App with cross-origin popup" and state "The user would like some of their compute heavy web apps to be faster" - but there is no discussion of why these applications must exist cross-origin.
>
> 2. What are the trade-offs taken for this?  Or, what are the risks that we'd be taking on by allowing this loosening of cross-origin isolation?  The explainer focuses exclusively on arguing *for* the proposal, but if we're going to make a reasoned decision, we need to understand the cost of the change.   Are there any safeguards that might be needed to mitigate these risks?
>
> 3. Are there cases where applications might want to use SharedArrayBuffer, but are unable to employ a fallback method, such that enabling easier access to the capability would dramatically simplify the deployment/development of those applications?

*we agree on the above comment and Martin posts it*

### [Review for CR transition of WebAssembly specifications for version 2.0 features ](https://github.com/w3ctag/design-reviews/issues/1002) - @torgo, @matatk

*punted*

### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

Martin: concluded that needed more time - we gave Anssi & co info to consider. we expect a major update before we re-engage on that one.



## Plenary Session

Present: Jeffrey, Martin, Dan, Tristan

Regrets: 


### Breakout Rollup

https://github.com/w3ctag/design-reviews/issues/979

Martin: a concern... some feedback pending.



#### Breakout A

#### Breakout B

Martin: we talked about https://github.com/w3ctag/design-reviews/issues/985 

Jeffrey: Mark claims that under some constraints you can run untrusted script... and yes maybe, but it's not clear that it's useful to anyone... 

Dan: what's the user need?

Jeffrey: it could enable a bunch of nifty web sites... e.g. run stuff without putting it in an iframe... in fact nobody has made it work... On the other hand it might be. So I think what we said : go talk to TC39 and webappsec is the right statement.

Martin: totally agree...

Jeffrey: we need Lea to talk about 998 local link.. seems like everyone things it should be renamed but Lea might disagree.

Dan: private state tokens?

Jeffrey: the idea is that there is skepticism about private state tokens overall... the change is justified on the idea that there's not a privacy leak with private state tokens... the ask is for them to run it by PiNG... turns out it's not adopted by anti-fraud group .. it should got to a working group.

Martin: considerable skepticism about this line of investigation... but it's deployed and shipping... so it should be in a working group with IPR protections...

Jeffrey: private access tokens ?

*discussion of use cases*

*agree we should probably focus on encouraging creation of a working group rather than trying to solve the problem in TAG*


#### Breakout C

### Issue Triage



### TAG Associates

https://docs.google.com/document/d/1DcN1IkdxKPbTZFa2vzqEaYgyP9LTqQEjjIBY3PXLbV0/edit?tab=t.0#heading=h.4q0a341xlnl1

Jeffrey: this makes sense.. question is limit one per person...

Martin: I'd rather just have a pool of people.. I like the idea that the people each have a TAG mentor... but doesn't have to be one person...

Dan: *defence of the one-per-member idea*

Jeffrey: i suggest anyone can nominate anyone they want and these people get approved by TAG consensus

Martin: i agree with that...  We could have 2 or 3 per organization.

Martin: this is a leg-up... We should have an announcement. I suggest we work on developing that announcement. And how to communicate it to the larger community. And try to get a list of names for the initial list that we can approach...  List of people we wish were on the TAG.

### Gaps

https://docs.google.com/spreadsheets/d/1kct5cZQnWsgIF2K4UfOSMbZpo4eiT2xpekM-knPYBug/edit?gid=0#gid=0
