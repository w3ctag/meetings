## Agenda

### Breakout A (Europe / US) - [2020-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200727T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @kenchris, @plinss
* [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss
* [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris
* [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss
* [Storage Pressure Event](https://github.com/w3ctag/design-reviews/issues/533) - @hober, @dbaron, @plinss
* [Import Conditions](https://github.com/w3ctag/design-reviews/issues/535) - @hober, @kenchris

### Breakout B (US / APAC) - [2020-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200727T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
* [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss
* [VisibilityStateEntry](https://github.com/w3ctag/design-reviews/issues/534) - @dbaron, @atanassov

### Breakout C (APAC / Europe) - [2020-07-28](https://www.timeanddate.com/worldclock/converter.html?iso=20200728T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Miniapps doc - ready for publication?
* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris
* [WebRTC Insertable Streams](https://github.com/w3ctag/design-reviews/issues/531) - @hober, @cynthia, @ylafon
* [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris

### Plenary Session - [2020-07-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200729T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Miniapps feedback doc
* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo - what do we do with this?
* Breakout Rollup
* Issue Triage


## Minutes

### Breakout A (Europe / US) - [2020-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200727T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Kenneth, Peter, David, Tess, Yves

Regrets: Dan, Rossen


#### [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @kenchris, @plinss


Ken: They are asking for feedback on 5 things (last comment in issue). Like should we add to existing screen in addition to getScreens() or should we just add the new props to the screen objects returned by getScreens().

Ken: navigator.screen is the main screen. they want to add additional things (beyond what's already defined in CSSOM View). [list of many features] They want getScreens() in addition because you may have more than one; should the new things just be added to the new objects or should they also get added to navigator.screen

Tess: shouldn't they be the same type of Screen object?

Ken: the new things are async, and they want a static snapshot instead of having a live object. Also the current object is sync and permissionless.

Peter: my initial reaction was similar to yours. But now I think navigator.screen is a mistake. We should deprecate it over time. Maybe the new Screen object should have a similar API surface, but be distinct. I think we should pretend navigator.screen doesn't exist and start over.

David: Do all of the things on the existing screen object even make sense for all screens, or just the main screen? [examples] [spec](https://drafts.csswg.org/cssom-view/#the-screen-interface), [Gecko IDL](https://searchfox.org/mozilla-central/source/dom/webidl/Screen.webidl), [Blink IDL](https://source.chromium.org/chromium/chromium/src/+/master:third_party/blink/renderer/core/frame/screen.idl)

Tess: should we file CSSOM View issues to ask them to deprecate the main screen object, and cut its properties down to just what is necessary for web compat?

Ken: That sounds good

Peter: `availTop` and `availLeft` make sense if you have `top` and `left`, but those only make sense if the geometric relationship between all the screen is known. (I suppose it is, but can change over time.)

Ken: [takes action to leave comment to that effect]

David: we shouldn't weigh in too strongly, in case they have good reason to do something different.

Ken: the next one is whether getScreens() should support filtering, perhaps with media queries

Tess: We have [some advice in our design principles document about this kind of device enumeration](https://w3ctag.github.io/design-principles/#device-enumeration
). We recommend providing the ability to filter or constrain the devices that get returned.

Tess: They shouldn't rely on a list that provides all the screens.

Peter: not sure the multiscreen boolean makes sense.

Tess: They should also rigourously spec the order in which screens are returned (per our design principles)

Ken: [leaves comment summarizing the above]

Tess: [time check]

Peter: third issue is #34 combining screen enumeration and window placement proposals

Tess: argument for is that they need to be used together to solve the use cases, and argument against is theoretical purity? they're logically distinct?

Peter: relationship between screens can change over time, but that's not related to this issue. this is the relationship between windows and screens.

Tess: on the one hand, I like reviewing short specs that define one, self-contained feature. On the other hand, I tend to prefer kitchen sink specs (like HTML) over lots of little specs (like CSS). I think it makes editors think through how things are interrelated more. All that said, I think this question is ultimately one of editorial discretion. My quirky preferences shouldn't outweigh the preferences of the people actually doing the work.

Tess: I will take the action item to give the feedback

Tess: issue #29 now, reject promise with permission denial

David: Seems reasonable to reject the promise.

Ken: As we suggested deprecating navigator.screen it would be bad if you can not get the main screen without a rejection/permission

David: Not sure this should be behind a permission and instead be browsers settings etc.

David: I will leave some feedback. [Done.](https://github.com/webscreens/screen-enumeration/issues/29#issuecomment-664511183)

Ken: last question is [about scope](https://github.com/webscreens/window-placement/issues/15)

David: seems complicated; different OSes and different browsers do different things here.

Tess: regarding #15 scope, I encourage them to take baby steps - I will leave feedback. 


#### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss


#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris


#### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss


#### [Storage Pressure Event](https://github.com/w3ctag/design-reviews/issues/533) - @hober, @dbaron, @plinss


#### [Import Conditions](https://github.com/w3ctag/design-reviews/issues/535) - @hober, @kenchris

### Breakout B (US / APAC) - [2020-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200727T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Alice, Tess

Regrets: David, Peter, Sangwhan

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov

Alice: They filed an [issue](https://github.com/w3c/csswg-drafts/issues/5321).

Tess: Analogy with forced-colors is good. But not all user preferences are created equal - this is "I prefer not to have seizures/motion sickness", not "I prefer dark mode".

... Could map the "reduce motion" preference to "forced-reduced-motion" MQ instead of "prefers-reduced-motion".

Alice: A lot of animations aren't problematic, and are useful.

Tess: Need some way of distinguishing parallax from...

Alice: e.g. flying focus rings

... Here is the WebKit blog post with the list of problematic animation types: https://webkit.org/blog/7551/responsive-design-for-motion/#zoom

Tess: If you ask authors to denote what their animation is doing... they're not going to do that. Hard to even get people to add alt text. People don't tend to notice things that don't affect them directly. 

... Would need to be some heuristic but what? Number of elements impacted? Number of properties changed at once?

... If I was some very knowledgeable author with a very complicated site, and I wanted to handle prefers-reduced-motion by selectively disabling animations on my site but without fore-knowledge of what they are.. I could use the web animations API to figure out what animations are running... what would the risk factors be?

- Total number of animations e.g. 20 animations is probably too many?

Alice: The article lists the following triggers:

- Scaling and zooming, e.g. giving the illusion that the viewer is moving forward and backward in physical space
  - example is a subtle zoom effect on a background image which is played on mouse hover. Fix is to simply turn off the zooming effect when prefers-reduced-motion matches
- Spinning and Vortex Effects - visual elements moving in circular motions around a large portion of the page, behind still elements.
  - fix is to disable the spinning effects
- Multi-speed/multi directional movement (often parallax effects)
  - fix is to turn off parallax effects and just scroll normally
- Dimensionality or Plane Shifting
  - example is a solar array that tilts as the page scrolls.
  - Fix is to disable the tilting animation and scroll normally
- Peripheral motion, specifically horizontal movement
  - Example is an animation of leaves gently swaying near text
  
Tess: It's interesting that most of these examples are scroll-linked

Alice: What examples have the scroll-linked animation authors given us other than problematic ones?

- Progress bar animations... probably

... I think every other example is problematic per the WebKit blog post.

... Scaling and/or translating animations in all of the problematic examples

Tess: Rotating would be another problematic transform

... blur was in one case in the WebKit blog post - that would be a filter, rather than a transform

... scaling and translating are often "hacked" using width/height, left/top etc.

... blur could be simulated in other ways. 

... 3D transforms are directly messing with perspective

Alice: I'm really tempted to say that there are so few unproblematic cases for scroll-linked animations that scroll-linked animations should need to opt-in rather than opt-out of running if the user prefers reduced motion.

Tess: There would be push-back because of the inconsistency. Not really a backwards compat issue because it's not shipping yet. Argument about inconsistency is primarily theoretical purity, also partly a learnability thing. But the user need is very clear. Still gives the author to opt-in. Sweet spot of meeting user needs and powerful enough to allow authors to do what they need to do...

... Would like opt-in to explicitly mention the risk, somehow. Would be kind of cool if the word "vestibular" were in the property value. Like you have to type out "this animation is not going to harm people with vestibular disorders", basically.

Alice: Can always copy-paste your animation into the prefers-reduced-motion block.

Tess: Would be good to give people something easily Googleable where we can attach an explanation about the harm that can be done to users. Not having that risks authors blithely copy/pasting code into prefers-reduced-motion blocks without understanding why that might harm users.

... I'm happy to try and comment to this effect.

1) The default needs to be off
2) We should have an opt-in syntax which is clear about the potential user impact

#### [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

Alice: It would be good to get Peter's thoughts on the `do-not-stream=""` attribute.

... I'd probably call it `no-streaming`

... when would you use the attribute?

Tess: Code will be written assuming the attribute is a no-op, because it is in the only known implementation.

Alice: Do we want to say the attribute must be provided if only a non-streaming implementation is available?

Tess: Would be better to say that without that attribute it's just a plain `<template>` that never gets instantiated, if there is no streaming and the `no-streaming` attribute is not provided.

... What would a browser that *only* supports streaming do when it encounters this marker?

... Other browsers will probably need to support non-streaming since there is this precedent, anyway.

Alice: I think we would prefer that `shadowroot` not have any effect on its own if streaming is not available, *unless* the `do-not-stream`/`no-streaming` attribute is present.

... Let's discuss this in the plenary with Peter.

#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

Alice: No update on their end yet.

#### [VisibilityStateEntry](https://github.com/w3ctag/design-reviews/issues/534) - @dbaron, @atanassov

### Breakout C (APAC / Europe) - [2020-07-28](https://www.timeanddate.com/worldclock/converter.html?iso=20200728T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Kenneth, Alice, Sangwhan, Dan, Yves

Regrets: Hadley


#### Miniapps doc - ready for publication?

[discussing content of document]

Dan: I will export this to markdown and we can send the URL to the w3c people.

Dan: the virtual meeting is happening this week: https://www.w3.org/2020/07/miniapp-virtual-meeting/index.html

#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

Sangwhan: commenting and bumping

#### [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris

Ken: [updating explainers in issue]

Ken: they added some content to the explainer. Support for CSS environmental variables that we suggested. 

Alice: Sangwhan [had commented] it wasn't using visual viewport.  We talked about getting visual viewport and virtual keyboard folks talking to each other.  [reviews latest comments]  The overlaysContentProperty seems like a good thing to have.  Less clear on what the geometry change event is for.  With the example of the env variable setting the position of the search box and then the event repositions the search box but why would you bother with the code when you could use the env variable.

Ken: if you're using a canvas based approach then you would need the API.  At lot of MS Office for example is using Canvas. That should be clarified. 

Alice: Sangwhan's comment is asking for a more general solution - the response has been that they don't expect there to be a general API.  This is a suite of features that all work together... Whether there should be a more general solution.. if there's not then an env variable is good to have... They are adding a virtual keyboard event in navigator.  virtual keyboard namespace... now also an event target.  Any other types of events?

Dan: does this fit together with "events are for notifications"? [in design principles](https://w3ctag.github.io/design-principles/#events-are-for-notification)

Alice: I think this isn't violating that. 

Alice: `navigator.virtualkeyboard` has one property which is an event listener that gets geometry change events ... why not just have the geometry available on that instead of having to get it from this event?  I should be able to get the dimensions every time.

Ken: I think it should have. That is also how we did generic sensor API. The event just notifies that there is new data.  

Sangwhan: [demos a virtual keyboard]

Alice: I think the event makes sense but the data should be available without the event.

Alice: Feedback: it would be nice if we could get the bounding rect of the virtual keyboard at any time.

Alice: you've got the virtual keyboard showing and you want to change the search box... you've got to store a copy of the width and height...

Ken: yes - if you want update it in every request animation frame because you're doing something with canvas then those dimensions might have been changed...

Alice: seems like it might be good to have a generic solution but probably shouldn't be their problem. Who's problem is it? 

Sangwhan: picture-in-picture has a similar problem. Payment request as well. 

Dan: Some browsers have a "scroll to top" button that brings user to the top of a page - which is overlaid on top of content.

Alice: So it's conceivable we need a general solution. Say we were to generalize this- the geometrychange event would make sense to generalize. So that would be a collection of "obstruction" rectangles. For each of those you would want to know when it changes... Then would you also want a CSS environment variable for each one?  And would you want to generalize ...

Dan: could we push this to an existing working group?

Sangwhan: CSS might be interested... not sure how to make this work in CSS.

Alice: It's worth noting that there are specific examples that Sangwhan gave - a set of things that all have these properties of occluding the page.  We feel like there should be a general solution - which means it's tricky to say "go ahead and ship this". 

Sangwhan: my main concern is that there is a bunch of one-off geometry obstruction notifications. Also one last meta question about API surface. Keyboard is a member of `navigator` but should that be `window`? If you're in one tab and you switch to another then you won't have keyboard open any more...  `navigator` feels overly global. 

Ken: you have it on multiple screens then how's that gonna work?  How does this tie together with screen enumeration API?

Alice: in the last example they give - it has 2 window segments - they keyboard pops up and they move the search box without checking which segment the window is on. So even their own example is weird. How could we help them?

Sangwhan: we could suggest - visual viewport.

Ken: with dual screens it's considered one viewport.   If you have a different screen..  

Sangwhan: or something completely new...   Maybe this should be 2 specs rather than one. The obstructions should be a separate spec from keyboard.

Alice: yes - what is keyboard only?

Sangwhan: i think just geometry change should be generalised.

Alice: Not sure I agree. We've got a bunch of CSS variables that give you the same info as the bounding rect on the event that we think should be in it.  In any case environment variables are going to be useful. You're going to need to get the bounds and when the geometry has changed. The only thing that doesn't need to be generalised is when the virtual keyboard changes the viewport height?

Dan: Could we just recommend they call it "interface overlay" instead of keyboard?

Ken: that makes it difficult to do with CSS variables... If you just want to position something where the keyboard is ... 

Sangwhan: if you have a keyboard and PiP window and another payment request API popping up then the content should know about these.  The separating of the keyboard into 2 is less important.

Alice: the nice thing about the API is that it does help with the split keyboard case... for example the map content appearing between keyboard areas... page content can flow behind.

Dan: next steps?

Alice: I think we can say that it does seem this is going to be a general problem. Shipping a specific solution to a general problem could cause problems down the road. They've identified the elements of a general solution.  You need ways to know the geometry of the obstruction and you need to know when that changes. We think this will apply in other cases.  

Sangwhan: anything that's browser chromish that could obstruct qualify.

Alice: they might want to reach out to visual viewport. Reach out to PiP to generalize this. Only challenge to generalize would be CSS properties. Could be a collection of objects that work the same as virtual keyboard. Final bit of feedback would be to be able to get the bounds at any time without having to save them from the event.

Alice: it's suspect to have it on navigator ... we're talking about generalizing this - could we generalize this as a pattern. For example `window.virtualkeyboard.boundingrect` `window.virtualkeyboard.overlayscontent` could we make that a pattern e.g. `window.pictureinpicture.boundingrect` etc... And get `window.obstructions` and it returns a list.

Sangwhan: [looks at PiP spec] PiP also has a [resize event](https://googlechrome.github.io/samples/picture-in-picture/). 

Alice: it's on us to go to the PiP folks and say 'you should give enough info as virtual keyboard does'.

Sangwhan: they don't have this.  

#### [WebRTC Insertable Streams](https://github.com/w3ctag/design-reviews/issues/531) - @hober, @cynthia, @ylafon

[punt to plenary]

#### [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris

[punt to plenary]

### Plenary Session - [2020-07-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200729T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan, Peter, Tess, Sangwhan, David, Alice

Regrets: Hadley


#### [Miniapps feedback doc](https://github.com/w3ctag/design-reviews/blob/master/reviews/miniapps_feedback.md)
#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo - what do we do with this?
#### Breakout Rollup

Tess: Breakout A: **Screen enumeration API**.  Was the entire breakout.  We got through the issues. We spread out actions to each of us to comment on each issue. If those 5 issues go satisfactorily we can close this.

... For B, we looked at **Scroll-linked animations**.  Should scrolling animations animate by default when `prefers-reduced-motion` is on. This question hinges on : currently `prefers-reduced-motion` doesn't by default reduce any animations.  Sites need to affirmatively follow that pref.  Question is : should these animations follow default or.. argument for a change like that is that if you look at the kinds of animations that trigger vestibular disorders, the kinds of animations that scrolling triggers are these. Second question: should there be a "i really mean it" option for scroll-linked animations.  And should the syntax be `i-promise-my-animation-doesn't-trigger-vestibular-disorders` to help make people aware?

Tess: **Declarative Shadow DOM** issue - Mason's proposal of a do-not-stream attribute... 

Peter: I was pleased he likes the idea but it still seems to be operating in the same mode. Don't know why we need an opt in to explicitly turn off streaming.  I need to go back and review.

Dan: Breakout C: Talked about **miniapps**..

... agreed to publish the document we've been hashing out. Now checked in to design review repo; abolished dated URI scheme for future reviews. Sent the link to Wendy. Haven't heard back yet.

... Miniapps Virtual Meeting later this week.

... **Virtual keyboard API** is where we spent most of our time. Think we made some good progress.

... question is, is this just for keyboards or is this applicable to other types of screen overlays that can occlude web content? We think the latter, e.g. picture-in-picture, payment sheets, scroll-to-top overlay button, video controls potentially. Would be nice to signal to content that this is happening. Would be nice to have a generalised approach. Sangwhan was going to look into PIP.

Alice: feedback I was going to leave - they have a solution that has a couple of components - an object that hangs off of window.navigator. Property - boolean - also an event target.  When there is a geometry change event it includes the new geometry on the event. We think the geometry should be available at all times. The other aspect is the CSS env variables that allow you to style things to not go behind the keyboard if it's in "overlay the content" mode. Seems like most of those functions would be needed by anything that occludes the screen. Furthermore you could call it a pattern.  You could also list the CSS variables on the object... seems like there might be a nice solution where we're not requiring the authors of this proposal to boil the ocean to ship what they want to ship - but also provide a pattern that others can use.

Peter: I think it's a great idea in general. I'd also like to see the API so you don't have to go look for things explicitly but get a list of things that are overlaying the screen in general.

Alice: you'd be able to get `window.virtualkeyboard` but also `window.obstructions` - all of those objects would have the same pattern. But difficult to know what to do about the env variables.

Peter: it would be fair to through this problem at the CSS working group.

Alice: My action is still to leave a comment and note the problem - 

Peter: and one of us will file the issue in CSS.

David: some of these types of things need to behave differently from others - keyboards vs other types of obstructions have different characteristics.  

Peter: one example - if you get focus on an 

David: keyboard - you do want to let the page know that it's smaller...  But some other example where you don't.

Dan: Suggest that Alice still leave the feedback as above, and we can try and recall those exceptions.

... Reviewed feedback on **[virtual keyboard show-hide policy](https://github.com/w3ctag/meetings/blob/gh-pages/2020/telcons/06-29-minutes.md)** from Bo Cupp and we were happy with the change made to the explainer.

Sangwhan: I had recalled that there was an implementer (Safari) that had objections. I don't personally have objections, however.

Dan: Do we need an end state/label for a review where the TAG doesn't have consensus?

Sangwhan: I think we do have consensus on this one.

Peter: not all screens are rectangular, when we consider split-screen devices. Can't shrink a screen in an "L-shaped" way.

Sangwhan: Web Machine Learning community asked me to submit a talk on ML on the web. Plan to submit on an individual basis, would folks be interested to read slides?


#### Issue Triage
