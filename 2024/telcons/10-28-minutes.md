# TAG Minutes Doc - Mon 28 October 2024

## Call Agenda

### Breakout A (California / Europe)  - [2024-10-28](https://www.timeanddate.com/worldclock/converter.html?iso=20241028T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk
* [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996)
* [HTML Canvas place element](https://github.com/w3ctag/design-reviews/issues/997) - @hober, @matatk
* [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk

### Breakout B (California / Australia) - [2024-10-29](https://www.timeanddate.com/worldclock/converter.html?iso=20241029T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin
* [Multiple import maps](https://github.com/w3ctag/design-reviews/issues/980) - @jyasskin, @LeaVerou
* [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou
* [Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @hober, @LeaVerou
* [CSS view transition auto name generation](https://github.com/w3ctag/design-reviews/issues/1001) - @martinthomson, @jyasskin, @plinss
* [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005)

### Breakout C (Europe / China) - [2024-10-30](https://www.timeanddate.com/worldclock/converter.html?iso=20241030T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion
* [Review for CR transition of WebAssembly specifications for version 2.0 features ](https://github.com/w3ctag/design-reviews/issues/1002) - @torgo, @matatk

### Plenary Session - [2024-10-30](https://www.timeanddate.com/worldclock/converter.html?iso=20241030T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* ["With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76)
* [Adjust TimBL's TAG status](https://github.com/w3c/process/pull/791)
* incoming masonry design review request
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Call Agenda

### Breakout A (California / Europe)  - [2024-10-28](https://www.timeanddate.com/worldclock/converter.html?iso=20241028T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Lea, Jeffrey, Matt, Peter

Regrets:

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss

Dan: who's getting what on the CSS agenda?

*no action thus-far*

Jeffrey: they are doing a breakout for some view transitions issues next week [?] if we want to be engaged that's a good time to engage.

Lea: either October 30th or nov 6, but doesn't look like it's decided.

Jeffrey: should we close our issues as satisfied-with-concerns?

Peter: don't feel like we're satisfied?

Lea: if we're satisfied with the use case and not the solution then it's not satisfied.

Dan: so who's gonna do what?

Lea: maybe someone who is not part of CSS wg should post? I can write it though... Let's summarize our concerns:

Dan: Key point I was hearing was developer confusion arising for the overloading of the term "Class" in the CSS context.

Lea: if they don't use the class syntax and they don't call it class, then are we OK with it?

Peter: i'm ok-ish. The conflation with class is my primary concern... but also concerned with using something like class ... where there could be competivie solutions. One of the solitions we discussed briefly on the call would be allow multiple names... 

Matthew: from minutes from last week - https://github.com/w3c/csswg-drafts/issues/8319 - where they told us it had already been discussed.

Lea: looking at that thread, I think Peter suggested repetitive code... he reasonably suggested why can't authors use selectors .. answer was that selector isn't valid at that time. But could this be an internal implementation detail...  What if it's the browser generating these rules? Then the experience for authors is just specifying selectors.

Jeffrey: I think we need someone to write that down...

Draft proposal:

> Summary of feedback, following our discussion on [last week's TAG breakout call](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/10-21-minutes.md):
> - If you're really set for this:
>   - don't use syntax around classes 
>   - support multiple comma-separated arguments to improve ergonomics
> - We'd prefer to eliminate the repetition in the first place, e.g. by having the UA generate these rules as an implementation detail

*we agree on above, Lea to augment and post both to CSSwg and our issue*

#### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

Jeffrey: altetnatives mentioned FedCM, Storage acces, Exemption Heuristics... The question is is there a way to do UI that is clear enough?

Yves: to make sure that people are not tricked.

Jeffrey: that it's not the main origin but that it has access the identity of the origin if there is communicaiton.  Not clear that there is any UI that can communicate that.  We can ask for solid UX studies that users understand the right thing from some plausable UI... 

Dan: user need.

Yves: SSO was listed .. but if fedCM is here then maybe it's not needed?

Peter: the user need is a need for business to maintain their current product... current business model. and i don't think this actually serves... users. It's a dangerous weakening of the web security model and user protections to support a dangerous use case that never should have existed in the use case.

Matthew: they have some UX proposals.. you end up with 2 URL bars ... which is a really really big change... Setting aside the issues they might have about understanding the URL anyway, but having 2 URL bars that would cause implementation pushback... 

Dan: the URL is important.

Lea: (1) cookie partitioning and (2) the UI component ... still unclear what that UI is... not sure how these mockups differ from ...

Jeffrey: there's a "please note"... 

Lea: what I was going to say is that the most contraversial of the 2 is the whole cookie thing... but not sure why that's needed.  None of these address post messages... So why not just use post message?  If this is a differnt way to open a popup... 

Jeffrey: security benefits to using cookies ... we can make it more secure ... that's some of the motivation here. 

Lea: but post message is just used when the popup communicates...

Jeffrey: yes but post message has to go through javascript...  This would work without javascript. Core idea is that the authentication token is never exposed to javascript... The context here is that people hire companies to do their login for them - like Octa - so if your site is foo.example, it goes to foo.octa.com ... so it blocks cookies. There have been proposals to use CNAMES and some browsers have taken action to block use of CNAMES for this purpose...  Authentication companies are worried about using CNAMEs for this purpose...

Lea: cost / benefit question is open but assuming they are useful - could we layer them differently?  What if the different popup UI was a different component? 

Jeffrey: example of this in the Arc browser today...

Dan: I've used Octa... I think the use case is valid...

Peter: but the reliance on 3p cookies - which was a bug ... what I'm opposed to is adding features to the web ... that exist purely to support someone's business needs... I have mixed feelings about the CNAME thing... there has been abuse of CNAMEs...   fundamentally I get that user authentication is hard - and some people want to outsource that. fine with building a mechanism into the web platform to allow for that. Happy with a dedicated API to do user authentication.

Dan: yes - i agree if we 

Lea: I agree it's a common flow - but fedcm us way down the line...  Also wondering if the main advantage is the cookie partition thing is to do post message without JS then why not just do that... and the browser takes care of communicating it to those origins...  Maybe instead of extending cookies or extending the security model of cookies... 

Yves: what you described sounds like first party sets though... so might not be the perfect model... If you're defining what you want to export to another site... content of a header...  Also re: fedcm not being implemented... therefore there should be a clear path to deprecating...

Jeffrey: another aspect - it's partitioned - it's not intened to share identities across the 2 sites - it's trying to be like an iframe... a general popup with post message would be too powerful.

Matthew: we discussed when we talked about document PiP that maybe there is a fundamental problem. I like the idea of decoupling UI but in this case since it's privacy maybe not... They compare themselves to fedcm - what about lightweight fedcm?

**dan to draft a comment based on above**

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Jeffrey: the comments gives some reason to give it the way they did - and that it aligns with ARIA... Is that convincing?

Lea: to some degree... We have a principle about consistency... and precedent... no right answer... that's what we have here.  Being consistent with a precedent is reasonable. However this isn't just about ARIA .. but any id ref in HTNL... we want this to work down the line... e.g. through slectors or names... Should this just be ID focused?  I won't push back if we think we're fine with it.  It's an important issue to solve that is holding WC back.

Peter: generally agree - i do want to push back on "ARIA works this way" - ARIA could be improved.

Jefrey: let's invite them to come talk to us?

Dan: breakout A the next week?

*jeffrey to reach out*

#### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

#### [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996)

#### [HTML Canvas place element](https://github.com/w3ctag/design-reviews/issues/997) - @hober, @matatk

#### [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk

Matthew: Jeffrey & I were discussing... we do think there might be something worth talking about here... Automatable?  I've just seen some additional comments.

Jeffrey: this specification is not a technical spec.. It's a guide for how to write specs. I feel like this should not be on the REC track... They don't have a format... 

Dan: a guidelines doc...

Yves: WCAG is on rec...

Jeffrey: it's saying "here's how you write a rule to test a web page against"

Matthew: Some parts of WCAG can be tested mechanically .. we have a plurality of different rule sets ... some proprietary. This is an attempt to harmonize...  This document is a tech specification for writing those rules... Perhaps it's a novel sort of document for the REC track though it does have MUST, SHOULD, MAY... but you couldn't write code to lint these rules as they are allowed to be written in file formats that lack structure (though in practice, many seem to be written in Markdown, which opens the possibility for linting and migration between rule format versions)... I do understand why it's rec track... but also it could be done in a different way. It's a good piece of work.

*we discuss potential comment - Matthew to work with Jeffrey*

### Breakout B (California / Australia) - [2024-10-29](https://www.timeanddate.com/worldclock/converter.html?iso=20241029T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Jeffrey, Peter, Martin, Tess

Regrets:


#### [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin

Looking to close with unsatisfied.  Martin will draft something that will likely be very spicy.  Jeffrey will help make that less overtly offensive.

#### [Multiple import maps](https://github.com/w3ctag/design-reviews/issues/980) - @jyasskin, @LeaVerou

Closed after previously saying we're OK.

#### [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou

Jeffrey owes this a re-review.

#### [Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @hober, @LeaVerou

A long discussion about the nature of stylesheets and whether adoption results in (logically) a clean copy of the sheet or a reference to a sheet.  This matters because encapsulation is enhanced by making a copy.  Having a reference means spooky action at a distance.


<blockquote>

A concern about whatever mechanism is used here is that there is an existing behavior of copy-on-write behavior when the same stylesheet is loaded from multiple places. e.g. if I `<link>` a.css twice, there's one instanace in RAM, but if it's modified via CSSOM, it splits into two instances so page authors can't tell it was shared in the first place.
  
However, with stylesheets that are adopted via JS API, the same instance is re-used and changes to that instance are reflected in each place they are referenced.
  
At the least we need to be clear what the expected behavior will be when declaratively adopting a stylesheet. It's also worth thinking about either reconciling the behavior or giving authors explicit mechanisms to opt-in to the behavior they desire.
  
</blockquote>

<blockquote>
We're happy to see this feature progress.  There are a few things that we've identified in the comments above that need to be considered by the working group as you continue to develop the feature.  Closing the early review as "satisfied with concerns" to reflect that.
</blockquote>

#### [CSS view transition auto name generation](https://github.com/w3ctag/design-reviews/issues/1001) - @martinthomson, @jyasskin, @plinss

This seems fine.  There is a web-compat risk "self" and "auto" were not previous proscribed, but now have new meaning.

#### [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005)

<blockquote>

The two types ("before" and "on") of event seem very useful things to have.

Why is this "toggle" and not separate "open" and "close" events?  The platform is not entirely consistent here, but these elements likely need distinct actions for the two cases.  We can't see a reason for this being a single event type.  (We'd like to see a path toward harmonization of events across the platform, but that's a larger project.)

We also agree with Dan about `&lt;details>` and the opportunity for future work.  That's not in scope here, but we encourage you to look into it.

</blockquote>
  
### Breakout C (Europe / China) - [2024-10-30](https://www.timeanddate.com/worldclock/converter.html?iso=20241030T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tristan, Matthew, Yves, Max, Martin

Regrets:


#### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Dan: We have a [response from Elad](https://github.com/w3ctag/design-reviews/issues/962#issuecomment-2429483359)

Martin: ... it's fine ... the discussion of alternatives I think we covered off well ... risk mitigation is a bit soft ... maybe should push more on that.

Dan: security & privacy section is small and does not talk about abuse cases

Matthew: looks like this would work OK if someone viewing the share is already zoomed in - but this is about controlling the remote viewport. So this could improve a11y in that sense. But... is there any provision for the people on the call being able to control?

Martin: unclear - I think it's only local playback. No protocol that exists ... 

Matthew: it's just "you are the person sharing this tab and it allows you to control scolling or zoom from there"

Martin: yes...

Matthew: from a cursory look - looks fine - but in something like this that has profound UX implications we should be asking for an a11y considerations section in the explainer. But they need to demonstrate that they thought about it.

Dan: Should we recommend that they get an a11y review from APA?

Yves: also an attack surface analysis.

Matthew: maybe something that could be good for a11y. 

Dan: a11y checklist

Martin: ... not sure it's enough

Matthew: if you're sharing  a web site...

Martin: ways in which different browsers render things differently... 

Matthew: in some cases like collaborative editing ... 

Martin: a lot you miss with the screen shot... in some cases that's a feature. 

Matthew: re: checklist - APA does theirs as a questionnaire that allows you to open an issue somewhere else - whereas ours opens an issue in our repo.

> Thank you for your reply and all the info in the Explainer. We discussed this on our breakout today.
> We still feel the explainer needs more information on possible abuse cases and a bit more discussion of attack surface. The security considerations talks about potential confusion, but doesn't talk about how the API could be abused by bad actors. So we recommend a security analysis (and there is a W3C process spinning up for this) but in the mean time if you could bolster the current security considerations doc with some discussion of abuse cases and mitigations that would great.
> As there's a lot going on UI-wise here, we'd really like to see an 'Accessibility considerations' section in the Explainer (it's totally fine to use this section to show what the positives are) - please could you add one?
> Please also consider requesting a review from the APA WG: https://github.com/w3c/a11y-request/issues/new/choose

**we agree to [post this](https://github.com/w3ctag/design-reviews/issues/962#issuecomment-2446195385)**

#### [Review for CR transition of WebAssembly specifications for version 2.0 features ](https://github.com/w3ctag/design-reviews/issues/1002) - @torgo, @matatk

Dan: we got a [response](https://github.com/w3ctag/design-reviews/issues/1002#issuecomment-2433783456).

Matthew: they said "yes it's part of our work mode" ... but they did point out that there is a [design rationale](https://github.com/WebAssembly/design/blob/main/Rationale.md) docs posted publicly... 

*Martin has suggested that we close. We have +1's on that from Jeffrey, Tess, Yves, Matthew, Dan*

> Hi and thank you for your response, @dschuff. We agree that making those design rationale docs more discoverable, as you suggested, would be a good idea. Other than that we are **satisfied** with the proposal. Thanks for allowing us to review.

**closed**

### Plenary Session - [2024-10-30](https://www.timeanddate.com/worldclock/converter.html?iso=20241030T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Martin, Jeffrey, Dan, Tess, 

Regrets:

#### Breakout Rollup

* View transitions - CSS issue to be progressed 

* Popins - Dan to write a draft response based on discussion in A.

* Reference target - some discussion in the issue - Jeffrey working on getting Alice to breakout B, maybe

* A11Y rules format - Matthew has an almost complete comment

* Fenced frames - Martin wrote [a long feedback *in draft*](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/41#issuecomment-2445927267)

  Martin: I would advocate for an *object* position

  Peter: I support



#### ["With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76)

Peter: we've had a proposed close on it for 3 years. I think we can close it.

Martin: I think we can just close it.

*we agree to close*

#### [Adjust TimBL's TAG status](https://github.com/w3c/process/pull/791)

3 options:
1. Just lower the short-circuit threshold to 80%
2. That and [Remove Tim from the TAG, but extend a permanent invitation to participate](https://github.com/w3c/process/pull/791)
3. That and [Remove Tim from Councils](https://github.com/w3c/process/pull/792)


#### TAG Associate program status

#### [incoming masonry design review request](https://github.com/w3ctag/design-reviews/issues/1003)

Tess: we're going to get a design review request for "masonry" - it's not a dispute escalation. They are not asking us to solve their problem. The chairs of the css-wg want the Tag to weigh in on this before they make the decision. We should not treat it like a dispute ...

Martin: we should call a spade a spade

Tess: they want our input by **mid-November**... 

Jeffrey: asked them to talk to each other - Elika and Rachel will do that in the next week.

Tess: masonry layout is (like pinterest) - is it a new kind of thing or is it a flavour of grid? Good arguments on both sides... Not a clear right answer.  There is 2 and a half implementations... mozilla, webkit, chrome in progress... 

Peter: I'm aware of the issue ... at the end of the day are their behavioural changes? 

Tess: basic functionality, use cases, are the same ; all addressable by either. It's not just bikeshedding. It's about extensibility of css over time... That architectural question is non-obvious.

Dan: clear developer complexity thing?

Tess: one of the arguments that's being made - you're doing a responsive layout - if you want to sometimes be doing grid and sometimes be doing masonry then that makes an argument one way... But do people actually want to do that? Don't know because they're not doing it now...

Peter: you could still switch display types - but it might have extra complexity.

Tess: some scenarios might be more complex than the other... 

Peter: is there a fundamental arch principle? 

Jeffrey: both sides are claiming arch principles support their side.

Tess: they're both right. I don't want to push CSS wg one way or the other... 

Martin: only thing we can contribute is being the detached [view]

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

