# TAG Teleconference
#### 09-13 January 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-01-09](https://www.timeanddate.com/worldclock/converter.html?iso=20230109T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [View Transitions](https://github.com/w3ctag/design-reviews/issues/748)
* [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744) - @torgo, @maxpassion, @atanassov
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia, @rhiaro
* [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman
* [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791) - @LeaVerou, @plinss
* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2023-01-10](https://www.timeanddate.com/worldclock/converter.html?iso=20230110T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion
* [UI Events Keyboard Events Code Values review request](https://github.com/w3ctag/design-reviews/issues/790) - @rhiaro, @ylafon
* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo
* [No-Vary-Search HTTP header](https://github.com/w3ctag/design-reviews/issues/797) - @rhiaro, @ylafon
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @torgo, @rhiaro

### Plenary Session - [2023-01-12](https://www.timeanddate.com/worldclock/converter.html?iso=20230112T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* IRL F2F Dates - AC/AB/BoD monkeywrench
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


-----


## Breakout A

Present: Dan, Amy, Lea, Peter, Rossen, Yves

Regrets:

### Spaces vs. Tabs

Amy: *strong thoughts about why spaces are better*

Lea: *also strong thoughts and opinions*

Dan: Are we really doing this?

### [View Transitions](https://github.com/w3ctag/design-reviews/issues/748) - @lea @rossen

Lea: I had a call with Jake Archibald - we went through some demos - it's more clear to me how this API works...  My concerns were - there's a lot that has to be done with JS. There's a declarative version - same API for multip page and single page apps. For SPA it requires JS.  For MP there's a declarative version. A way to solve the declarative problem... use JS for the transition as well..(?) Transition itself is specified in CSS.  View transition name needs to be unique... Failure mode inconsistent with web platform... No way to specify if you want a different transition depending on pages or elements... unless you hack together with more JS. Biggest take-away: I do think it's usable as is. I would like simple cases to be possible to do declaratively. You still do some wrangling with JS. Say you're animating from a list of things with images to a full page showing the image. The way you use the API - you add a class to the thing you clicked and then remove that class and add it elsewhere... Still more simple than with CSS, where you have to wrangle a lot more things...

... You can enable flags in Chrome Canary... if you want to play with it...

*deep thought ensues*

Peter: where do we go?

Lea: Satisfied with concerns?  There is a strong user need.  As long as you're willing to write JS it's OK. my main concern is you have to write JS in some cases where you don't have to otherwise. Other concern: you must [...] the DOM manipulation (in SP version) ... if you want to add a transition you depend on the library firing the right event... 

Peter: how would you do it declaratively?  If you're going to wind up making changes to the DOM.

Lea: when you click an element and it gives you more detail - how do you declare which element is the staring one since CSS doesn't give you a mechanism for that?  It would be nice if there was a way to say. Since the browser knows when the DOM has been manipulated. 

Peter: my concern: is there anything about the design that preculdes declarative - probably not.  The point about not being able to have different transitions depending on what the elements are is concerning.

Lea: also what the pages are in multi-page. Transitions are supposed to communicate meaning, not be only decorative. If it doesn't matter where you're coming from and going, they are just decorative. 

Peter: should be addressed in future.

Lea: it could be worked around... 

Peter: give feedback to ask if they've thought about that... Let's not paint ourselves into a box... with an API design that makes it difficult to add later.

Lea: I can give that feedback.

Rossen: I have thoughts.

Lea: my questions were answered today... They are already thinking about transitions dependant on elements

Rossen: so not precluded by the current design?

Lea: Correct. Concern about.. if you use a view transition name that is a duplicate you get a warning, is that consistent with the rest of the web platform?

Peter: if it just goes and spits out a warning that seems odd

Lea: you lose the transition altogether, and it spits out a warning

Rossen: you can't even handle it easily?

Lea: you can't because its CSS.

Peter: is the case where you have multiple things with the same name.. in CSS specificity wins

Lea: right, in most things in CSS. With this new css property that's not how it works. If you have a duplicate view transition name.. if you specify the same view transition name on two elements - and the way css selectors work makes this very easy - you're supposed to manually make sure you only apply this to one element in the entire tree. If you have duplicate ones, no transition happens, you just get a warning. The reasoning being maybe in the future they might want to do something clever with multiple elements that have the same view transition name. So that might make it easier. Seems to me CSS printing out a warning is nto very consistent. We even have a principle about declarative syntax shouldn't throw warnings somewhere, at least to html. Maybe should expand to CSS.

Peter: the issue is when you have the same transition declared for multiple elements? Not multiple transitions with the same name?

Lea: you use the same transition name on the start and end state,s which could be different or same elements. Same property with an identifier. If you use that on multiple elements at the same time that is a problem. When you use it to specify the start and end state you're supposed to add the name on the starting element and at some point you move it to the end state element. Unclear to me at what point that happens.

Peter: warning if multiple elements have the view transition name at the same time?

Lea: yes. Then you don't get a transition at all.

Peter: does seem weird

Lea: I wonder if a better design might be to explicitly say what is the start and end state, instead of a property that does both at once. But haven't thought about it as much as they have, maybe there's a reason not to do it that way.

Peter: could ask

Rossen: and ask if using root as the name would ever work? If you look at the clarification they have about using the view transition name custom ident it's defined as the element can participate.. as either a node or new element with view transition name equal to custom ident value.. [reads] ... so now if I go and add a transition called root, what happens? Do I get a warning and the document elements one doesn't work?

Lea: [will ask]

<blockquote>

@jakearchibald and I had a call about this yesterday, and I think I now understand how this works and how the different pieces come together a lot better. We later discussed this again with other TAG members in a breakout.

We are aware that you have all been thinking about this for a lot longer than we have, and it's entirely possible that you've already explored all this and concluded the current API shape is a necessary compromise, but in case it helps, these were our thoughts:

- We like that MPA transitions are declarative, and would love to see a declarative syntax for SPA transitions too, as right now the two APIs feel a bit disconnected. It's also an antipattern if an author needs to write JS to animate a DOM manipulation or navigation that was not fired through JS. A declarative way to transition hash navigations within the same document could address some of that. Perhaps also a declarative way to filter view transitions by container and types of DOM mutations? This would also facilitate enhancing behavior from third party scripts with view transitions, as these often use their own events, which makes it hard to time the JS call. 
- It looks like CSS would be a more appropriate place for the declarative opt-in, rather than an HTML `<meta>` element which cannot be customized by media queries or scoped to elements in the future.
- We think it's **essential** to be able to customize the transition easily based on the elements or pages that are participating in it. Good transitions communicate, they are not just decorative. If the API makes it simple to have the same transition regardless of what is transitioning to what, but tricky to customize it, it facilitates transitions which are merely decorative.
- We think that skipping the transition and showing a warning when there is a duplicate `view-transition-name` is not Web Platform compatible. Typically in the declarative languages of the Web Platform, when something needs to be unique but isn't, is still handled gracefully (e.g. by using the first or the last one). Especially this being a CSS property, it's very easy to accidentally specify it on multiple elements, simply because it's very easy to specify selectors that match multiple elements. Also, since the root has `view-transition-name: root` anyway, how do you use that without having duplicate transition names? 

We wondered if it could prevent some of these issues and allow more room for future expansion if `view-transition-name` distinguished between the start and end state (e.g. through `old` and `new` keywords, possibly used together if the same element is both). That also prevents the user having to time when `view-transition-name: foo` will be removed from the start state and added to the end state: both can happen at once, at the same time as the event that kicks off the transition.

In general, we'd like to see a layered, gradual approach, where a small amount of declarative CSS syntax can address common use cases, more CSS can customize the transitions further, and JS is needed to customize behavior even further than that.  This is also in line with how existing CSS transitions and animations work, where syntax is gradually added to customize further, but very little syntax is needed to produce an initial result. 

We also think tighter collaboration between the designers of this API and the CSS WG could help address some of these issues.
  
</blockquote>

### [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744) - @torgo, @maxpassion, @atanassov

Dan: it's a bunch of different things

Rossen: how do we review many things.... Looks like they have at least five different APIs all under one review.

Dan: as Elad said, he feels like they're too far apart to be part of the same explainer, but close enough for review as a group, because they're all screensharing related UX hints. Looking at display media stream... There are security considerations, a description of the use case

Rossen: hard to tell what it is from the explainer. What is being proposed?

Dan: a spec change, which is a [PR](https://github.com/w3c/mediacapture-screen-share/pull/216/files) that has already been merged, into media screenshare ... They've all been merged. I would like to ask what they're asking us for. Are there issues with this? Privacy and security it says covered by existing questionnaire - small delta.

Rossen: looking at [this](https://groups.google.com/a/chromium.org/g/blink-dev/c/bIGZVdkZ4OE/m/G1C2aXcIAAAJ?utm_medium=email&utm_source=footer) .. says it would benefit from a joint explainer. Combined outline with pros and cons, what's in and out of scope.

Amy: there's back and forth in that thread that says one overall explainer might be confusing, so maybe that wouldn't help us?

Rossen: [will respond asking how we should approach review and asking for one explainer]


### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia

*bumped to C*

### [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman

Peter: conversations between them and the CSS WG

Amy: this spec was mentioned in the FO report - because this was the main reason they wanted to change the wording in the TTML charter... They talked me through it on a call so i understand the gist.  A way to share info on what devices can render for subtitles - so not too much information is provided.  It's a complicated spec to read.

Rossen: explainer highlights and does explain what they're doing and why.  Based on the design they're proposing - the brief overview is - a level of capability categorization - allow them to understand what the time to render a subtitle is - so subtitles don't overlap.  Fairly well scoped and well intended capability.  Question I'm not understanding : as the author what will you do about it?  If you have font specific ... as an author you should be able to switch and use something less expensive.

Amy: Also note: I understand none of the substance is new - it all existed as part of [another spec](https://www.w3.org/TR/ttml-imsc/) before.

Dan: so there are presumably already implementations. Is there any revision? What's changed?

Rossen: visually there is change, but hard to see what

Peter: are they asking us to review the delta, the refactoring, or all of HRM? I don't recall that we've ever reviewed this in its entirety

Dan: could we ask... what the specific ask is. What should we be focussing on? What answers do you want from the TAG? Given it's already existing rec, is there anything architectural that you're concerned about that we should weigh in on?

Peter: are they really asking for a full TAG review of the HRM?

Amy: [will leave a comment](https://github.com/w3ctag/design-reviews/issues/788#issuecomment-1376192275)

### [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791) - @LeaVerou, @plinss



### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

Amy: negative signals from Mozilla and Webkit

Dan: *move to breakout C*

### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia


## Breakout C

Present: Max, Amy, Dan, Yves

Regrets:

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

```
The intention of the Topics API is to enable high level interests of web users to be shared with third parties in a privacy-preserving way in order to enable targeted advertising, while also protecting users from unwanted tracking and profiling. The TAG's initial view is that this API does not achieve these goals as specified.

The Topics API as proposed puts the browser in a position of sharing information about the user, derived from their browsing history, with any site that can call the API. This is done in such a way that the user has no fine-grained control over what is revealed, and in what context, or to which parties. It also seems likely that a user would struggle to understand what is even happening; data is gathered and sent behind the scenes, quite opaquely. This goes against the principle of [enhancing the user's control](https://w3ctag.github.io/ethical-web-principles/#control), and we believe is not appropriate behaviour for any software purporting to be an agent of a web user.

The responses to the proposal from [Webkit](https://github.com/WebKit/standards-positions/issues/111#issuecomment-1359609317) and [Mozilla](https://github.com/mozilla/standards-positions/issues/622#issuecomment-1372979100) highlight the tradeoffs between serving a diverse global population, and adequately protecting the identities of individuals in a given population. Shortcomings on neither side of these tradeoffs are acceptable for web platform technologies. 

It's also clear from the positions shared by Mozilla and Webkit that there is a lack of multi-stakeholder support. We remain concerned about fragmentation of the user experience if the Topics API is implemented in a limited number of browsers, and sites that wish to use it prevent access to users of browsers without it (a different scenario from the user having disabled it in settings).

We are particularly concerned by the opportunities for sites to use additional data gathered over time by the Topics API in conjunction with other data gathered about a site visitor, either via other APIs, via out of band means, and/or via existing tracking technologies in place at the same time, such as fingerprinting.

We appreciate the in-depth privacy analyses of the API that have been done so far [by Google](https://github.com/jkarlin/topics/blob/main/topics_analysis.pdf) and [by Mozilla](https://mozilla.github.io/ppa-docs/topics.pdf). If work on this API is to proceed, it would benefit from further analysis by one or more independant (non-browser engine or adtech) parties.

Further, if the API were both effective and privacy-preserving, it could nonetheless be used to customise content in a discriminatory manner, using stereotypes, inferences or assumptions based on the topics revealed (eg. a topic could be used - accurately or not - to infer a [protected characteristic](https://w3ctag.github.io/privacy-principles/#hl-sensitive-information), which is thereby used in selecting an advert to show). Relatedly, there is no binary assessment that can be made over whether a topic is "sensitive" or not. This can vary depending on context, the circumstances of the person it relates to, as well as change over time for the same person.

Giving the web user access to browser settings to configure which topics can be observed and sent, and from/to which parties, would be a necessary addition to an API such as this, and go some way towards restoring agency of the user, but is by no means sufficient. People can become vulnerable in ways they do not expect, and without notice. People cannot be expected to have a full understanding of every possible topic in the taxonomy as it relates to their personal circumstances, nor of the immediate or knock-on effects of sharing this data with sites and advertisers, and nor can they be expected to continually revise their browser settings as their personal or global circumstances change.

A portion of topics returned by the API are proposed to be randomised, in part to enable plausible deniability of the results. The usefulness of this mitigation may be limited in practice; an individual who wants to explain away an inappropriate ad served on a shared computer cannot be expected to understand the low level workings of a specific browser API in a contentious, dangerous or embarrassing situation (assuming a general cultural awareness of the idea of targeted ads being served based on your online activities or even being "listened to" by your devices, which does not exist everywhere, but is certainly pervasive in some places/communities).

While we appreciate the efforts that have gone into this proposal aiming to iteratively improve the privacy-preserving possibilities of targeted advertising, ultimately it falls short. In summary, the proposed API appears to maintain the status quo of inappropriate surveillence on the web, and we do not want to see it proceed further.
```

Sangwhan: the state with 3p cookies is worse.. this is a counter proposal

Yves: change Amy proposes about filtering on the set of topics you're willing to share is a good way to make it better.

Amy: I agree it would be an improvement..  But still possible to identify individuals from a set.

Dan: it's presented as a way to do privacy preserving targeted advertising but it doesn't actually acheive that goal. Jumping through a lot of hoops and doesn't do it anyway. Something we should call out. If a lot of people say 'we use the Topics API that means we preserve your privacy' and that's not the case, that's a bad thing for the web

Sangwhan: the information theory perspective.. if what was presented is wrong that's a concern .... 

Amy: Not necessarily that it's wrong. Moz analysis is from a different perspective.  Google analysis doesn't cover the worst case scenario.  The google paper is correct but just not the whole picture.

Sangwhan: please add the user opt-out story into [this comment]. Users should be able to opt out from certain topics. It could be something culturatly sensitive. 

Amy: lots of reasons...  Also shared computers.

Dan: only one user of the browser.

Amy: plausibile deniabolity - random topics sometimes selected - that doesn't help. If we have a collective idea that the web is spying on you then ... given that "it was a randomy selected ad" won't cut it.  

Sangwhan: Also because it's so low ... 

Amy: Martin's paper goes into it - you get the same set of topics in the period of a week - in the worst csase it would be 3 weeks before you'd find a topic is of legit interest.

Sangwhan: the more origins involved ... 

Amy: you can spin up subdomains - game it in this way.

Sangwhan: using sampling to get the topics...

Amy: on the point of saying "i want to opt out" - it's a good setting - but you can't possibly know what things are going to get you into trouble in a given moment. You don't make time in your week to curate your ad topics for sensitive topics.

Dan: Don Marti sometimes makes the point thath people who don't think t hey're in a protected class or that they've vulnerable people could suddenly become a vulnerable person, if they're in an abusive situation, or the law changes .. eg. someone who suffers a miscarriage isn't going to immediately sit down and curate their ad preferences

Amy: and if they're in a particular jurisisdiction, suddenly it's dangerous if 'baby stuff' is no longer an interest overnight

Sangwhan: the more efforts like this get delayed the more the current state continues.

Amy: I don't think that needs to be true.

*discussion on dynamics of advertising and browsers*

Amy: I don't think it's about 3rd party cookies - it's about surveillance on the web and tracking.  if we take away 3rd party cookies and replace it with something that has the same problems then that's not OK.

Sangwhan: I'd like [us] to give actionable feedback.  I think what webkit and mozilla raised are all valid concerns.

Amy: also getting feedback from an independent third party.  I think we're getting iteratively closer. We're moving slowly in the right direction.

Dan: +1

*amy to do some edits and check with group before posting*

### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

### [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion

Yves: conversation started with the Google folks.  The choice of packaging format depends on solution they take for insuring origin is a proper origin.

Dan: as far as we kno there's not additional need for our time right now?

Sangwhan: our concerns were heard, so we can wait.. it's a solveable problem. Technical debt on the packaging end. Bundles did not solve the use case that mini apps needs

Yves: yep. It has some mechanisms that will help, but doens't solve everything

Sangwhan: and something that bundles really needs to address. Eg. epub wasn't able to use bundles becuase of these limitations. Indefinite offline web apps should be a thing.

### [UI Events Keyboard Events Code Values review request](https://github.com/w3ctag/design-reviews/issues/790) - @rhiaro, @ylafon

Yves: looked in the past.. a registry more or less. Hasn't changed in a long time. Looks good to me. Very stable, this is just for CR

Sangwhan: we can sign off on this, it's been around for a long time

Dan: I'm happy for us to .. 

Yves: [will leave closing comment]

### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo

Sangwhan: I have looked at this.  Was reviewed by us - this is a re-design. The other API was a polling mechanism. This changes that into an observer based pattern. I'm happy about that change. That said I have some concerns - some gaps in this. The compute pressure - trigger could be cases where it's artificial. Not because you're busy but because you're constraining the system because of power saving. It's one bit of entropy. If you take the browser process and constrain the cores it can access... you will be able to mine this information out by heuristics.  Functionality wise it seems sensible. Other thing I'm a little worried about is sample rate - will it cause problems - certain ways of sampling this info can be high CPU consumption - not sure if sampling rate is too high?  Overall other question that remains to be answered : do we think this is a good thing?  I know Mozilla has been negative about this - it's info that a compute heavy applicaiton would make use of - but it makes more informnation - intimite platform info - to an origin. Do we want to expose this to the web platform?

Dan: will move to devices and sensors wg. You mentioned multistakeholder - any others besides chromium?

Sangwhan: nothing from webkit. Mozilla is against it.

Dan: what is an example of a compute heavy application that we'd expect people to..

Sangwhan: cryptpad plus google meet on a low end machine... if one or the other application can acknowledge that they can't use the whole cpu they can do something about it. Right now there's no information that lets them take action. Now a video conf app can reduce resolution or disable certain streams to reduce data needed to process. Cryptpad could reduce the amount of worker threads to reduce the footprint.

Dan: I think we should raise the issues, in particular the privacy related issue.. they've done a security and privacy.. minimising information exposure.. they are talkinga bout some of these issues [in the document itself](https://w3c.github.io/compute-pressure/#security-and-privacy-considerations).


Sangwhan: they reduced the granularity of the information to make it a bit more safe

Amy: is there a UX improvement that could help with the privacy issues? off by default, and you can turn it on if you're doing something compute heavy?

Dan: or the browser can use a heuristic to prompt the user to enable it if it's struggling, with a warning?

Sangwhan: gated behind a permission - but problem because of how observer kicks in ... the user doesn't see it when there are problems, but before... 

Dan: can they share additional information about multistakeholder?

Sangwhan: [will leave comment]

### [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo

### [No-Vary-Search HTTP header](https://github.com/w3ctag/design-reviews/issues/797) - @rhiaro, @ylafon

### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @torgo, @rhiaro

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia



## Plenary Session

Present: Dan, Amy, Peter, Yves, Sangwhan

Regrets: Hadley

### IRL F2F Dates - AC/AB/BoD monkeywrench

AC/AB/BoD meeting in south of france end of april/early may - should we colocate?

Tentative booking in Tokyo w/c 17th April

### [Should charters link to TAG Design Prionciples](https://github.com/w3ctag/design-principles/issues/407)

### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

### Issue Triage

## Async

- Closed https://github.com/w3ctag/design-reviews/issues/789
