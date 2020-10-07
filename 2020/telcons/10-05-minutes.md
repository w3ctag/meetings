## TAG Minutes

### Breakout A (Europe / US) - [2020-10-05](https://www.timeanddate.com/worldclock/converter.html?iso=20201005T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* PR: [Internet is for End Users](https://github.com/w3ctag/design-principles/pull/236) - @hober
* PR: [Change APIs to features](https://github.com/w3ctag/design-principles/pull/207) - @plinss
* [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron
* [Can we use `media` in WebNFC?](https://github.com/w3ctag/design-principles/issues/140) - @atanassov
* [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov
* [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron
* [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185)

### Breakout B (US / APAC) - [2020-10-05](https://www.timeanddate.com/worldclock/converter.html?iso=20201005T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Readability Edit PRs: [readability edits](https://github.com/w3ctag/design-principles/pull/223), [readability edits](https://github.com/w3ctag/design-principles/pull/224), [readability edits](https://github.com/w3ctag/design-principles/pull/226), [readability edits](https://github.com/w3ctag/design-principles/pull/227), [readability edits](https://github.com/w3ctag/design-principles/pull/228) - @alice
* PR: [web consistent naming principle](https://github.com/w3ctag/design-principles/pull/217) - @atanassov
* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron
* [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov
* [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron
* [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

### Breakout C (APAC / Europe) - [2020-10-06](https://www.timeanddate.com/worldclock/converter.html?iso=20201006T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* PR: [when to use sync](https://github.com/w3ctag/design-principles/pull/218) - @cynthia
* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice
* [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia
* [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia
* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo
* [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon

### Plenary Session - [2020-10-07](https://www.timeanddate.com/worldclock/converter.html?iso=20201007T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Security & Privacy Questionnaire: publish a new snapshot, and adopt continuous publication in the future
* TC39 interaction?
* Breakout Rollup
* Issue Triage

## Minutes

### Breakout A (Europe / US) - [2020-10-05](https://www.timeanddate.com/worldclock/converter.html?iso=20201005T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Tess, Peter, Yves

#### PR: [Internet is for End Users](https://github.com/w3ctag/design-principles/pull/236) - @hober

[Tess working on it...]

Tess: [made changes]

Dan: Positive review.

Tess: [merges.]

#### PR: [Change APIs to features](https://github.com/w3ctag/design-principles/pull/207) - @plinss

[On hold until readability edits land...]

#### [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron

[punt to plenary]

#### [Can we use `media` in WebNFC?](https://github.com/w3ctag/design-principles/issues/140) - @atanassov

Rossen: issue around naming.. the name webnfc is using is one thing. We opened a PR against design pinciples. [PR 217](https://github.com/w3ctag/design-principles/pull/217)

Tess: I like it.

Rossen: Literally 2 sentences.

Dan: ken's comment

Rossen: merge after the fix?

[agreed to merge PR 217](https://github.com/w3ctag/design-principles/pull/217) and closed issue 140.

#### [Harmonize permissions and similar mechanisms](https://github.com/w3ctag/design-principles/issues/144) - @dbaron, @hadleybeeman, @plinss, @atanassov

Dan: we reached out to Nick Doty but no response yet.

Tess: I can ping him again.

Peter: I am happy for it to be a separate document. My goal on the original issue was - when you do use permissions, make it consistent.  Standard API patterns... Places to look for permissions to see which are active... 

Dan: dependency on work such as the permissions API..   Maybe this should be a finding to encourage more work on this topic - there is still no consensus about what the right approach is even after the permissions workshop.  

Tess: "please fix this mess"

Tess: Nick got back to me - positive on incorporating the permission doc into design principles - either way.

#### [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron

Dan: [david wrote some content at the f2f](https://github.com/w3ctag/design-principles/issues/172#issuecomment-698023655)

Dan: Can someone create a PR with this content?

Rossen: David's text is pretty good.

Peter: It's fine.

Rossen: I will put it in a PR.

Dan: We can review and hopefully merge in the plenary and then close this issue.

Rossen: [making a PR](https://github.com/w3ctag/design-principles/pull/240) 

Dan: let's merge at the plenary

#### [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185)

Tess: this came out of the web crypto review... adding altorithms... 

Dan: Anything can be done here?

Dan: Suggested some [text](https://github.com/w3ctag/design-principles/issues/185#issuecomment-703751333) "new crypto algorithms that are proposed to be added to the web platform should be rigorously review by international security experts..."  I think we need to define that a little more - what review means, what rigorously means, etc...  But also I think we need to say that the TAG is not and does not seek to be a cryptography design authority.

Rossen: where should we point them?

Yves: the security IG?

Rossen: that sounds reasonable.

Dan: also IETF 

Tess: and IAB

Dan: maybe we can write some more in the plenary if we all agree this would be useful to put into the document.

Yves: network security should be IETF - but web applications security it should be webappsec wg.

### Breakout B (US / APAC) - [2020-10-05](https://www.timeanddate.com/worldclock/converter.html?iso=20201005T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### Readability Edit PRs: [readability edits](https://github.com/w3ctag/design-principles/pull/223), [readability edits](https://github.com/w3ctag/design-principles/pull/224), [readability edits](https://github.com/w3ctag/design-principles/pull/226), [readability edits](https://github.com/w3ctag/design-principles/pull/227), [readability edits](https://github.com/w3ctag/design-principles/pull/228) - @alice
#### PR: [web consistent naming principle](https://github.com/w3ctag/design-principles/pull/217) - @atanassov
#### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron
#### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117) - @hober, @alice, @dbaron, @atanassov
#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron
#### [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

### Breakout C (APAC / Europe) - [2020-10-06](https://www.timeanddate.com/worldclock/converter.html?iso=20201006T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### PR: [when to use sync](https://github.com/w3ctag/design-principles/pull/218) - @cynthia
#### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia, @alice
#### [Improve guidance for using attributes vs methods](https://github.com/w3ctag/design-principles/issues/70) - @cynthia
#### [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia
#### [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @cynthia, @alice, @torgo
#### [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @cynthia, @torgo, @ylafon

Yves: comment from anne - sniffing may be necessary - might need to be added to the text.  For image formats there's pretty much an equiv between media type and data format but for video formats it's more difficult because the media type is about the package not about the encoding.

Yves: is there way to advertise properly the encoding.   Need to discuss with Sangwhan.

#### [pervasive monitoring link pr in ethics](https://github.com/w3ctag/ethical-web-principles/pull/27)

[reviewed, squashed and merged

#### [looking at marcos's PR](https://github.com/w3ctag/ethical-web-principles/pull/30)

Dan: looks good

Hadley: looks good

[squashed and merged]

### Plenary Session - [2020-10-07](https://www.timeanddate.com/worldclock/converter.html?iso=20201007T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Tess, Dan, Peter, Alice, Hadley, 

Regrets: Sangwhan

#### TPAC Organization

APA - 
https://github.com/w3ctag/meetings/issues/45
https://github.com/w3ctag/meetings/issues/46

Alice: ...

Hadley: At TPAC session last year they were talking about personalization -- cutting out everything but the main text... Distraction.  & I have a general interest in semantics.

Alice: you may be interested to look at [comment Rossen & I left](https://github.com/w3ctag/design-reviews/issues/476#issuecomment-698641238)

DID -
https://github.com/w3ctag/meetings/issues/47



#### Security & Privacy Questionnaire: publish a new snapshot, and adopt continuous publication in the future
#### Interaction with TC39?
- What features would be interesting to us?
- What guidelines can we give as to what we would like to look at, rather than every single proposal?
#### Breakout Rollup

Alice: in breakout B - we debugged the build process for the design principles.

#### Design Principles PRs

Looking at https://github.com/w3ctag/design-principles/pull/224 - 

[discussing long long vs unsigned long long in webidl and javascript]

Peter: Bug in WebIDL?

[merged]

Looking at https://github.com/w3ctag/design-principles/pull/223

[debugging the markup]

[merged]

Looking at https://github.com/w3ctag/design-principles/pull/226

Tess: maybe a simple bulleted list on reasonable justifications for a manifest file - one would be the fetch timing and one would be the domain being different.

####  Security & Privacy Questionnaire

Tess: Can we publish the latest version fo TR space?

Dan: I'm happy with that.

Tess: PING are happy with it.

Tess: can we set it up for continuous publication?

Dan: I also think it's a good idea

Hadley: do we need a resolution for new drafts into TR space

Tess: not if we have a resolution for continuous drafts to TR space...

Dan: I think it makese sense to move to continuous

Hadley: makes sense to me.

Peter: +1

Dan: Can you ask Yves to do that?

Tess: will do

#### Issue Triage

## Chat with Brian Kardell on Extensible Web/High level vs low level APIs - 2020-10-07

Dan: We've been revising the design principles... just recorded a talk for TPAC to get the word out a little more.

... We have a separate [extensible-web.md](https://github.com/w3ctag/design-principles/blob/master/extensible-web.md) document - should we just incorporate that?

... Have we already incorporated that guidance? Do we still agree with it?

... To what extent has your (Brian) thinking evolved since the Extensible Web Manifesto was written? How might we better articulate the advice there?

Alice: extenible web design principle says ... new features to be designed via primitives and the composed to high-level capabilities...  

Brian: I [responded](https://github.com/w3ctag/design-principles/issues/182#issuecomment-627621773) to issue 182 that my hope had been that the TAG would think carefully about how to word this in a way that is not a manifesto.. myself and other co-authors of the manifesto have written a number of times about the follow-on questions and nuance it begs. The EWM says "should priotitize" - there hadn;t been any prioritization of that except for the DOM API up to that point - there was a huge backlog of things that needed to be done. Fetch and "explaining" things in terms of Fetch.. Promises that lead to Stream.  CSS was a giant magic box - no esecape hatches. When I think about prioritization, tech debt is a good analogy. You don't stop everything while paying down some tech debt - you just give it some priority. When you're talking about new features it makes sense to think of the lowest level you can start with but most things are looking for the advantageous middle. Inert and FocusVisible are examples of that.

Alice: You had that talk about finding the middle (https://www.youtube.com/watch?v=HgcLYIj05DI). 

Brian: I dom't feel the extensibleweb.md adds anything. There is a polyfill finding - a feedback loop is important... 

David: Was thinking about things in this space recently... came to the conclusion that one of the conerns I have with the EWM is that it doesn't describe a particular trade-off: a lot of the useful stuff that browsers do on behalf of users can only be done because of high-level features; those are the points where browsers can usefully intervene. E.g. some of the display stuff around making rendering usable on mobile, or to people who don't or can't look at things the designer designed them, or interventions at the networking level for privacy reasons

... A lot of those interventions depend on high-level features, so there is value for users in pushing towards high-level features.

... EWM talks about the escape hatch problem, developers want to do a little thing differently, so they need to throw away the whole thing and re-write it in canvas, for example. Some of the value of exposing low-level primitives is to fix that escape hatch problem, and that could influence more use of high-levle features because they can use those escape hatches.

Brian: EWM specifically says "we want people to write high-level, declarative code". It has a lot of authors, which led to different emphases. Need to deliver partial value, meet developers where they are.

Dan: Another reason this came to the fore was that we were getting some feedback on design reviews to indicate folks were taking a fundamentalist approach to primitives. Should we have some guidance in the DP doc which talks more about that "middle ground" area. Seems like that would be a good idea.

Brian: seems like a necessary idea.

... The "Bruce Lee" document was a year after the original document because I had similar concerns then. That says "nothing is holy including EWM". The EWM is an observation fixed in time that lacked a lot of details and nuance.

Alice: Can we remember any specific examples in design reviews?

Dan: Not immediately, sorry.

Brian: Something else relevant around being very clear in communication. I didn't realise until very recently that there isn't consensus on what "high level" and "low level" are, which seemed wild to me because I thought it was very clear.

... For example, was talking to someone about how vendors prioritise... I held out for them `inert` and `focus-visible` as reasonably high level features... `inert` juggles a lot of low level things in one coarse-grained switch, for example. They cited `async/await` as high-level, which was confusing...

... they refer to something which is transformative in how you write code is high-level.  I mention this because Travis also brings it up in #117

David: One piece of a definition I have used... low-level features are features you'd find in a general purpose language or it's stdlib... high-level features are more specific/peculiar to the web. 

Brian: Also plenty of stuff in the middle (between those) which are "higher" or "lower"...

David: It would be useful to talk about what the definition is.

Dan: I'm looking at this through the lens of what we should include in the design principles... does it makes sense to have some additional text around this. High level/low level seems to vague, it's more like a spectrum. 

Alice: not only not a dichotomy, but we don't agree on the endpoints.

Dan: could at least agree on endpoints, give some examples.  Maybe a separate finding?

Alice: David gave one option of definition of specific-to-the-web.  Examples that aren't HTML elements?

David: 2D Canvas API.... that is pretty similar to something you'd find in other stdlibs.

Tess: In fact it was based on core graphics

David: CSS text rendering on the other hand, is unique to the web.

... not a perfect definition, but might give some alignment with what we imagine these to be.

Brian: So by that definition everything in the JavaScript language is low-level,... everything that comes out of TC39 would be "low level".

... I think of this as a series of thought exercise questions... how big is this problem, how can we break it down, what is already shipped? Look at that differently from something that is fundamentally new... if something is fundamentally new, what is the lowest *practical* level we could offer it first. That also needs to be taken into account with security questions. That's the one that I'm the least sure on.

... People are asking for Maps ... week-long event (https://www.w3.org/2020/maps/call-for-participation) where we were talking about map-related elements, representing millions of dollars and many years worth of engineering effort, where you have to define "what is a map" where they don't even agree on that fundamental term... instead we could look at what maps need, e.g. panning and zooming.

... crosses video games, e-commerce, technical drawings, ... and maps. 

Tess: David said some of the things I would say  there is a disconnect between what it said and how people are interpreting.  David made a good point that user agents act on the user's behalf and declarative features typically have "wiggle room" that imperative features don't. UAs can perform the hinted activity or not... e.g. ; if you have a lower level (imperative) feature it's harder for the browser to intervene on the user's behalf.  `inert` is a good example where consolidation prevents a class of error.  Lower level than that would be bad. 

Brian: i think the design principles should not say "extensible web manifesto"...

Tess: the EWM was written and signed and in the intervening time it was associated with the TAG though was never issued as a finding. Given that what we want to say is more nuanced I think we have to reference it and say "here is the bit that needs some updating."  

Brian: no opposition. 

Alice: what advice should we give today?  Do we want to contradict the EWM, or some interpretations of it?

Dan: ... pre-question: what do we lose if we get rid of `extensible-web.md`.  Seems like an orphan document that lives in the design principles repo?  Have we incorporated it?  And as Brian said, already a polyfill finding.  Remove document, maybe no value left?  But then go on to Alice's question.

Brian: delete; shouldn't have an `extensible-web.md`.  But would love to see the third paragraph expanded and explained, with more nuance (safe, secure).  I'd say something about how this helps:  creates achievable goals, more likely to ship, and give us another building block on which to build next steps, meet developers where they live, let them show us paths and explore the space.  But I feel it has to be well nuanced.  I'd like y'all to do that.

Alice: I'd like to ? into that explainable concept.  If we take that into an extreme, which features hould be explainable in terms of which other features and why?

Tess: e.g., should `inert` be explained in terms of lower level things, or should it be the lower-level thing that explains `dialog`.

Brian: We're given the thing that we have... we have tech-debt ... maybe those other things shouldn't exist?  (responding to Alice's question) e.g., `pointer-events`, bolt-on ARIA.

Alice: what value do we get from things being explainable?

Brian: The thing David was talking about -- if you want to exlpore an adjacent space, you shouldn't have to throw out most of the web platfrm to do it.

Tess: e.g., explore new style line layout,

Brian: put something in CSS, parser isn't exposed, object model throws away what it doesn't recognize, then when is the rule applied, you have to understand how to sort applicable rules by specificity and origins, etc.  And that's before the complexity of "now it's your turn to lay out a run of text".  I think there are a lot of good examples of thing that happened because of this effort to connect and dig down. I think fetch is great.  I think having to spec url was unfortunate but necessary; great that we have it.  I think fetch api lifecycle with request/response makes so much sense, serves as where we define things for the platform.

Tess: Makes things like web bundles or unsigned exchanges possible; those are made up of request and response objects that fetch api defines, or something like that.

Brian: I guess -- makes service workers possible.  Allows you to explore -- there are custom elements out there that allow you to embed fragments of something.  Can guarantee it shares the web's qualities of same-origin-ness, and to greatest extest possible shares fundamental qualities of fetching on the web.  Tess, do you have concerns about those?

Tess: I think fetch is great.  Fetch is an nteresting example too; we already had XHR, which n terms of functionality it did almost everything.  They can still both do things that the other can't; a little weird.  But the reason I bring XHR up -- I tend to be averse to adding reduncancy to the platform (maintenance, testing, attack surface).  But in fetch's case I think it was worth it.  Common model that both could be defined in terms of enabled building things.

... back to question Alice started with:  one of the things I"d want to push back on that's at least in the standard interpretation of EWM is:  I think it's usually a mistake to build low-level feature before even trying to do a high-level feature.  I think it usually makes sense to do a high-level feature and find out why it's too hard, and fill in the lowel-level features.

Brian: Example?  I might agree with you.  e.g., I think a map element might be too much.

Tess: I think it makes sense to work on low-level and high-level stuff at the same time.  So you design the low-level pieces to serve an actual developer need.  If you just build low-level stuff, it's hard to know if it's fit for purpose.  Need constant validation from working on high-level stuff at the same time.

Brian: Example of where you saw that?  (I think I agree.)

Tess: I feel like most cases where people invoke EWM, they're arguing to not do a high-level thing and do the low-level thing first.  It's a stop-energy thing to say not do the high-level thing and do low-level things.  I think that's majority of my experience in venues like HTML and WebApps when people cite the EWM.

Dan: I think right approach is to add this nuance and reference it where appropriate.  Adding the nuance... can push back on people who wield the EWM like a stone tablet.  I think that should help solve Tess's issue.

Alice: key phrases I've heard: "escape hatches", "user needs", "common needs among different use cases", "middle ground".  Peter had an excellent point last time we talked about this about defining the lower levels in spec, but not meaning you have to put an API on it.

Tess: Yes, been making that argument a bunch.  Model is not equal to API.  Great to define an underlying model, but doesn't mean it should be 1:1 mapping to API that's exposed to script.

... I think that's standard for EWM afficionados to assume that model should equal API.

Alice: Maybe explicitly counter that?

Tess: Case I'd use as example there is probably `inert` as well.  Touches a lot of things.  Underlying description of behavior it controls is complacitade.  But as we said before `inert` should be the lowest exposed bit, since exposing lower bits would cause people to get it wrong.

Alice: guiding principle (with inert as example): what's the lowest level avoiding risk of developers getting it wrong.  Also goes back to David's earlier point about browser intervention.

Tess: grayer example: styling of form controls, e.g., select element.  Not enough escape hatches for fiddling with bits of select element.  But not enough in-between other than `appearance: none`.  So people build their own select elements.  And avoiding builtin ones means they get different behavior on iOS that doesn't fit platform conventions.  There is an escape hatch but it's a blunt instrument.  Hammer, used to make adjustments to fine china.

Dan: A quick note: we don't define escape hatches anywhere.  Maybe we should add that too.  If document is defining common terminology... we should talk about it.

Tess: select doesn't have enough nuanced of an escape hatch.  So developers go to the big hammer.  So the browser can't do the right thing when a new class of device comes out (like iPhone) that changes how inputs work, can't improve.  Example of what David was talking about -- matching platform convention is kind of an intervention on the user's behalf.  Using a thing on your phone should feel like other things on your phone.

Tess: Another example from recent-ish design review in the past year was `portal`.  Peter and I spent a lot of time with them in Tokyo, trying to convince them that `iframe` is XHR and what they neeed to do is `fetch`.  They were trying to define a new iframe-like thing, but weren't redifining iframe and this new thing in terms of a common substrate.  If this isn't the only one of these we want to do.... and in fact later the media team at Google proposed another iframe-like thing.  So seemed to walk away with a better understanding of our position, but seemed like they weren't happy about the amount of work we were asking them to do... seems unfortunate.  How do we help people do the design work the right way without discouraging them from doing it at all.

Brian: I think Andrew had an earlier take on that -- promotable iframe.  Try to reuse existing iframe.

Dan: I need to drop -- thanks for having this discussion.

Alice: I'm interested with the form control styling -- an example that came to mind for me as well.  EWM came out, all about shipping primitives.  Web Components stuff probably worthwhile, but with the amount of focus and time put into that, never got around to looking into form control styling until now.  What might it have looked like if we'd spent time on that earlier, went from top down instead of from bottom up?

Tess: To go back to something Alice says, what's the user need here?  Should work on things closer to this question.  Sometimes need to do foundational work several steps removed, but in terms of prioritization have a point.  But could have had more wins quicker on that question.

Brian: I want to go back and stress a few things:
1. prioritization for me means it needs some priority where it previously had none.  We're giving some priority to lots of things, e.g., parts of Houdini.  Happy about that, and conversations it generated.  I feel like we're adding priority but want to stress that I don't think this is exclusive priority ...I look at it like what do we do with tech debt, and how do we create big new things pragmatically somehow.  I literally proposed a new element the next year.

Brian: Features needn't start at the bottom... plenty in the platform has this "tech debt" where there's nothing "beneath" it - e.g. some way to do more with `<select>` than you can do today, is entirely in keeping with the EWM. 

... it's important that we look at the system, rather than point out what you "should" do as philosophical points, it would be helpful to look at things that exist in the platform as examples. We need concrete examples.

... EWM has no examples which leave too much to interpretation.

... the `<select>` thing is a good example, as is `fetch()`. You avoid duplication... `fetch` and `xHR` are two interfaces to the same underlying thing

Tess: I often find myself at odds with people who propose adding an alias to a CSS feature. If we're not changing the feature set at all but just adding a name alias, not enough to justify the increase in maintenance surface. Doesn't seem to be consensus on that principle, not sure what position the TAG should take on that. 

Brian: Could we document things that we think took a wrong turn, and how we might be better? CSS has some mistakes... 

Tess: there's that wiki page

Brian: Right, we don't want to do those things again. Maybe this document should include something like that.

Tess: One of my fav. examples is that cookies are scoped to schemeless same-site... new privacy features are going to be site-bound not origin-bound. That is a mistake that continues to affect new features beyond cookies. 

Brian: It's fine to start with a high-level thing and then figure out what parts can be broken off?

... Don't focus on this fundamental primitives thing, that's a red herring. Aim for the middle.

Tess: The slow, use case-based web manifesto.

Brian: I expect you'll find things ... this is a necessary element, no reason we shouldn't tackle this. Pan and zoom... no reason we shouldn't tackle this. 

Tess: When trying to figure out what feature to add.. look at developer pain points. Things where there is a lot of complexity, shows that there is a problem - too low level, too many things to juggle, or too high level because there's no escape hatch. Complexity is a smell.

Brian: We agree more than we disagree.

Tess: I took an action item to write a PR for the high level/low level APIs issue. Still need to do that. This discussion will help on that. This will be better the more of us that contribute...

Brian: Portals... I think portal is a neat idea, I appreciate the issue with duplication with IFrame. Feels like there is a common, lower-level thing that's missing. I don't know that I would block on that... there was stop energy there...

Tess: They understood our point, but ultimately we were asking them to quadruple the amount of work they would need to do to achieve their use case. Haven't heard from them since.

Brian: Would you do it differently?

Tess: Would do something similar, but emphasise that they don't need to do it all themselves. WebXR people came to us about hit testing, which is cool but we don't even have a hit testing spec for the web. Was worried they would design something for hit testing in the VR space which wouldn't match what we do for regular web sites. Asked if they could think about how hit testing works on the web, and specialise that for XR. But the XR folks don't want to pay down others' tech debt... the lack of hit testing spec has been a problem for a long time. However, they risk incompatibility since it doesn't exist.

... IFrame has a similar problem. frame/frameset and iframe are two existing elements that have a similar behaviour... they're adding a new one, so they need to figure out what the difference is between the models. Whatever the difference is between iframe and portal are parameters on iframe... need to at least add the scaffolding, so that iframe could be remodeled on top of the new model. Could have done it in a way which was less intimidating.

Brian: These are almost counter-examples... different problem sets that you come to, that have similarities and differences. Here you have stop energy ... some substrate where you need to do excavation and that work isn't as fun/rewarding. Things like hit testing... want to introduce this thing for XR but we need it everywhere else too. This is an opportunity for you to not make all the effort, but find allies to work together. Here are a million use cases and we're working together on something that's important to all of us. 

... Not "now you should go do this work for the general platform" but an introduction to other people who are working in a similar space. 

Tess: That sounds sensible. Lot of things on people's plates, things they could be working on. May decide to put something aside for easier wins. Should emphasise collaborative nature of standards work - you don't have to go it alone, this is an opportunity to find collaborators and have an impact outside of your domain.

Brian: The commons wins when we all contribute to it.












































































