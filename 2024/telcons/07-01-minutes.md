# TAG Minutes Doc - week-of 1 July 2024

## Agendas

### Breakout A (Europe / China) - [2024-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240701T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman

### Breakout B (California / Europe)  - [2024-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240701T153000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* F2F Agenda Planning

### Breakout C (California / Australia) - [2024-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240701T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober
* [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

### Breakout D (California / Australia) - [2024-07-02](https://www.timeanddate.com/worldclock/converter.html?iso=20240702T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson, @LeaVerou
* [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @hadleybeeman, @plinss
* [Constructors for RTC encoded frames with custom metadata](https://github.com/w3ctag/design-reviews/issues/942) - @martinthomson
* [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon
* [`noopener-allow-popups` value in COOP](https://github.com/w3ctag/design-reviews/issues/964) - @martinthomson, @torgo
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* F2F Agenda Planning

### Breakout E (Europe / China) - [2024-07-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240703T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo
* [Timing Info for ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/958) - @martinthomson, @torgo, @maxpassion
* [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk
* [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @LeaVerou
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou
* [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk
* scheduling a human rights assessment discussion - @riharo, @hadleybeeman, @torgo

## Minutes

### Breakout A (Europe / China) - [2024-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240701T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Matthew, Hadley, Max, Yves, Amy (2nd half)

Regrets:

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

Matthew: Seems like Peter has seen it and doesn't have objections... Tess said "it’s a weird layering violation if the spec mandates the use of a specific class name"... Lea said *There is precedent for using classes that way (as a pseudo argument), e.g. `::slotted()`, `:host()` etc. *  ... sounds like there is a bit of concern from the chat.. 

Matthew: it seems several have come out with soem minor to moderate concerns ... 

Dan: let's punt this to C where both Tess and Martin will be present.

#### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

Matthew: we got info from how it's different to RenderCapacity... I left a note about the side channel thing.  With respect to how related the APIs are we didn't comment. Web Audio working group said.

Yves: [from chat] *I was told it was not controversial in the Audio WG, it is linked to several (closed) issues in the WG, and they are just incubing it in WICG, see
https://github.com/WebAudio/web-audio-api/issues/2563 , https://github.com/WebAudio/web-audio-api/issues/2444 and https://github.com/WebAudio/web-audio-api/issues/373* They are probably OK with it. The draft is being worked on in WICG prior to bringing to the working group.

Matthew: So it comes back to does TAG think this is different?

Dan: worth noting that this is a good use of WICG considering that the working group is aware of it and it's being *incubated* in WICG in advance of being added to the charter...

*we review [discussion](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/06-24-minutes.md#breakout-a-1) in last week's plenary*

Matthew: we could ask them about the idea that one could be built on the other...  for anyone reading the explainer it would be helpful to contrast ... I can put something along those lines...



#### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou



#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: planned as a future extention but we are discussing doing it now...

Dan: looks like a productive discussion... Martin needs to be involved in moving this forward...

#### [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman




### Breakout B (California / Europe)  - [2024-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240701T153000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Matthew, Amy, Dan (2nd half)

Regrets: Lea

#### F2F Agenda Planning

What do we want from Johann? (Who's overseeing SAA, RWS, CHIPS, FedCM)

* high level overview of non-ad apis
* how they relate to fedcm
* privacy threat modelling of all of the things together, how they interact with each other, what architectural decisions lead to what outcomes? What levers are available to pull to improve things? How much coordination on this do the teams working on these tools actually do?

For reference, these seem to be the two most recent teleconfs with Johann:

* https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/02-20-minutes.md#breakout-c
* https://github.com/w3ctag/meetings/blob/gh-pages/2022/07-London/minutes.md#04a--privacy-sandbox

#### View transition classes ctd..

Matthew: thread in slack wasn't conclusive about disposition. Where is this thread going?

Peter: don't know yet


### Breakout C (California / Australia) - [2024-07-01](https://www.timeanddate.com/worldclock/converter.html?iso=20240701T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Martin

Regrets: Tess

#### [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo

Closing #819 after a few additional days.

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss (punted from A)


<blockquote>
  
The explainer mentions the use of classes as a considered alternative that was rejected.  This does not seem very convincing.

There's a way of conceiving this problem that looks somewhat different to what is described.  Think of `::view-transition-group` as a way of selecting elements by their name (like `div` or `p`, not an assigned name).  That is too imprecise in general.  There might be many `div` elements on a page and you don't want to animate all of them.  So `view-transition-name` is a way to assign a name to elements that overrides its natural name.

Similarly, you could use classes (as in <code>&lt;div class="foo"></code>) here.  We aren't convinced that an override for classes is necessary.  The example in the explainer uses:

```css
.list-item { view-transition-class: vt-list-item; }
```

In that model, `::view-transition-group()` contains an ordinary selector that applies to both new and old trees.  You can (and probably should) use `view-transition-name` to pick specific elements for transitions if you are using element selectors.  But you could also use `::view-transtion-group(.list-item)`, `::view-transtion-group(#foo)` (ignoring that the combined new and old trees will have duplicates), or `::view-transition-group(h1 + p:first-letter)` (even if this is not a great example).

That is, just use regular selectors.  People who need new labels because existing classes don't align with their view transition needs can add new classes.  There is precedent for using selectors that way (as a pseudo argument), e.g., ::slotted() and :host().

Maybe the feature here is a different one entirely.  In CSS, you often have a bunch of selectors that receive the same rule:

```css
.list-item, #foo, h1+p:first-letter { some-rule: 42px; }
```

This feature is adding a way to replace that list of selectors with a new class, like so:

```css
.list-item, #foo, h1+p:first-letter { extra-class: shortcut; }
.shortcut { some-rule: 42px; }
```

Which is a novel feature, but maybe not one that is necessary.  The second example there is simply more verbose and maybe use of `:is` and nesting is sufficient for most use cases.
</blockquote>

#### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) (punted from A - and maybe it can be closed)

@matatk probably needs to close this one, in case we missed something.

#### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk

Pinged proponents.

#### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

#### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

Still paused.

#### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

#### [Support Video Chapter in MediaMetadata](https://github.com/w3ctag/design-reviews/issues/952) - @hober

Tess is on point.

#### [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou



### Breakout D (California / Australia) - [2024-07-02](https://www.timeanddate.com/worldclock/converter.html?iso=20240702T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Tess, Martin

Regrets:


#### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson, @LeaVerou

Still pending external feedback. Have been waiting for 4 months.

#### [systemEntropy addition to PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @hadleybeeman, @plinss

Still pending external feedback. Have been waiting for 7 months.

#### [Constructors for RTC encoded frames with custom metadata](https://github.com/w3ctag/design-reviews/issues/942) - @martinthomson

Asked for information.  The explainer lacks key pieces of detail, like motivation.  WebKit marked this "invalid".  Hold, but expect to close.

#### [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon

Looking to enlist some external expertise in this area.  To review, get on a call, or find someone else.

stringref is a competing-ish proposal, but:

> What I describe is what the stringref proposal gives you. We don’t yet have consensus on this proposal in the Wasm standardization group, and we may never reach there, although I think it’s still possible. As I understand them, the objections are two-fold:
>
> 1. WebAssembly is an instruction set, like AArch64 or x86. Strings are too high-level, and should be built on top, for example with (array i8).
>
> 2. The requirement to support fast WTF-16 code unit access will mean that we are effectively standardizing JavaScript strings.

That suggests that there are bodies buried in the vicinity.

#### [`noopener-allow-popups` value in COOP](https://github.com/w3ctag/design-reviews/issues/964) - @martinthomson, @torgo

Discussion ongoing in the WG.  Having the TAG weigh in might help.

#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

#### F2F Agenda Planning

### Breakout E (Europe / China) - [2024-07-03](https://www.timeanddate.com/worldclock/converter.html?iso=20240703T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan

Regrets: Hadley, Yves, Max


#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou

#### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

#### [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo

#### [Timing Info for ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/958) - @martinthomson, @torgo, @maxpassion

#### [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk

#### [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @LeaVerou

#### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou

#### [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk
