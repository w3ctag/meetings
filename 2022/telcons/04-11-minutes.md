# TAG Call Minutes - Week-of 11 April 2022

## Agenda

### Breakout A (Europe / US) - [2022-04-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220411T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [``<search>`` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @rhiaro, @hadleybeeman
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov
* [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov
* [`[css-values-4]` The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov
* [`[CSS-Values-4]` FYI review of Allow infinity, -infinity and NaN in CSS `calc()`](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-04-12](https://www.timeanddate.com/worldclock/converter.html?iso=20220412T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov
* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @atanassov
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov

### Breakout C (APAC / Europe) - [2022-04-12](https://www.timeanddate.com/worldclock/converter.html?iso=20220412T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion
* [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* AC Sustainability Panel

### Plenary Session - [2022-04-13](https://www.timeanddate.com/worldclock/converter.html?iso=20220413T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion




* [Privacy Principles](https://w3ctag.github.io/privacy-principles/)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22) (14 untriaged)

## Minutes

## Breakout A (Europe / US) - [2022-04-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220411T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy, Peter, Tess, Lea

Regrets: Sangwhan, Yves, Hadley

### [``<search>`` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss

Tess: it's one of the only remaning cases where there's an aria landmark role that doesn't have a corresponding html element.... that's it - search element - container for searchy things. 

.. reasons why `<search>` may be better without forms functionality.

Tess: element not backwards compat - also more complex to specify. Goes beyond the original ask which is to make an element for each ARIA landmark role...  

... WHATWG SG ruled there was no code of conduct violation ...

Dan: So from a design perspective - what is there to do?  Pretty simple.

```
Hi folks - just FYI we've been asked to review the proposal. We're now moving forward with the review of the proposal as outlined in the initial request. Can we please limit discussion here to that context? Thanks!
```

Peter: call out specifically reviewing on technical merits, not process

Tess: most elements have some kind of default styling that aren't div or span. I don't remember offhand if this has any. 

Dan: [left comment](https://github.com/w3ctag/design-reviews/issues/714#issuecomment-1095263315)

Lea: doesn't make sense to duplicate form element functionality. Troubles me that it's an element that doesn't do anything and its only purpose is to have role="search". I worry authors will not be motivated enough to use it if it doesn't do anything else

Tess: fair. Lets you write selectors simply, like section or article - just aria landmarks, and make landmark look cleaner.

Lea: article and section are things you use multiple times on a website, so benefit from having them multiple times is more

Tess: ``<nav>`` you have once.. next to nav, search.. kind of nice

Lea: not saying it shouldn't exist..

Tess: it's a weak argument

Lea: anything useful it could actually do?

Tess: agree. Argument is basically completionism. 

Lea: where is that discussion?
  
Tess: aria and html people have always seen aria as a way to override semantics, not a way to set the semantics it should have had anyway. If you're using html correctly you souldn't have to decorate lots of things with aria. These days you do because people build their own custom form controls and you have to use aria on all of that stuff. But assuming you're using all of the pieces of html you shouldn't have to reach for the hacks.. aria is a hack, is the philosophy. The primary use case for aria that I find compelling is when you are a frontend developer and you come into a project afer it's been built, and someone says hey this is inaccessible please fix it. You have this refactoring challenge - do you fix all the markup to be good? you might break it. Might be complex selectors. Refactoring that kind of stuff can be risky. So the much lower risk is aria. Surgical tool for someone to make something accessible without screwing it up too much.

Lea: plans to add elements like grid cell, menu item, list box ..?
  
Tess: probably depends. Table is seen as the markup solution to tabular stuff. I doubt the aria stuff will get new elements as wel. But anything where there isn't any kind of equivalent, then probably. As far as I know for sectioning element stuff this is the last one. There might be some early aria design doc that talks about that philosophy that talks about it being an override and you should just use the html elements

Lea: I'm aware in general if you use html correctly you shouldn't need aria, but not about the pupsh to have html elements. Seems a cheat to invent html elements for the sole purpose of being aria roles. 

Tess: sure.. one of the nice things about adding it as an element that doesn't do anything is you're not overconstraining the future. If we wanted to add an api that hangs off this in future there's nothing to stop us. If we had it inherit from html form suddenly you've got this whole can of worms in terms of the stuff that hangs off it. I feel like the argument for adding it is pretty mild. Against is mild too. It seems fine. No real red flags.

Peter: I thought in the html5 parsing algorithm unknown elements are parsed as spans not block level?

Tess: this does not require parser changes, but there was an argument about whether it should autoclose `<p>` and don't remember how that ended up. I think it should. But there might be good arguments against. Obvious arguemnt is please don't ever change parser again

Peter: according to explainer it does close p tags, which does require a parser change. That's frightening, older browsers will parse a different DOM.

Tess: backwards compat story isn't that bad.. delivering markup to old implementations you can close the p yourself

Peter: with well formed you can always achieved the same DOM. That's not the point. Should acehive the same DOM regardless of how clean your markup is. So concerned if this does require.. I agree it's logical ot close the p tags, but breaking parsing algo is a concern

Tess: valid concern

Dan: leave a comment?

Peter: want to confirm I'm remembering this right. Always thought it was a mistake when they refined html5 parsing algorithm they should have defined self closing tags and defined a way to say this is block level... but this is th eworld we have, I'd like to not break it.

Dan: Lea's quesiton about additional functionality was answered by Tess?

Tess: still think i'ts worth bringing up. If you're going to convince someone to use an element there has to be some benefit. I'm okay with either outcome. I want to see they thought about it. You can make an argument either way.

Dan: that's what we should be doing, prompting people to think and write it up

[various comments]

Lea: [looks up stats]
  
### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @rhiaro, @hadleybeeman

Dan: I asked a question after last week's call. Didn't look like it's moved on from being a product specific API. That's the basis on which we closed the issue previously. We were requested to reopen it because of API changes. But the reason we closed it was the one vendor issue.

Tess: and that's still the case

Dan: so close it again?

Tess: assuming our original rationale was valid I don't see why it doesn't apply now. Could argue we should review it more closely because if chrome ships it and if everyone else decides to do it they will have to implement it that way. But not inclined to spend time reviewing a google only thing.

Dan: [leaves comment]

**closed**

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Tess: where we left off.. we both felt fairly strongly about this, and Peter was in between us.

Peter: agree strongly with both sides

Lea: might be good to recap.

Tess: proposal from google to add a controls list attribute to html media element which will control which of the native controls show up are are hidden. There were one off things for specific controls and they wanted to generalise it. [recaps history] There are arguments that aren't about ads. One argument is if you don't give them a way to do this they'll not use native controls at all, but will use custom controls that are more bloated and less accessible, buggy. Good arguments for encouraging websites to go down the virtuous path of using the built in contorls which we believe are already accessible etc. You can see the argument that if we don't give them this feature they're going to do it anyway in possibly a worse way. There's a harm reduction argument for it. Argument against that is paving the cowpaths of user-hostile behaviour. This has been argued about for years. The tiebreaker between the two sides is the question of multi-vendor-ness. We don't have multiple vendors on board with this attribute. That's a blocker for it ever landing in the html spec. Unfortunate to give a thumbs up to something that isn't going anywhere. 

... I have another idea. We could agree to disagree. There are really good arguemnts both ways. I sympathise a lot with Peter's position directly in the middle. Maybe the right thing at the TAG is for us to say we understand it's complex and there are good pros and cons. We haven't been able to come to consensus ourselves. Our understanding of pros and cons so you're informeda bout trandeoffs, though I'm sure thye've heard it.

Lea: I don't recall the picture in picture case.. a lot of the discussion centered around chrome offering a download functionality for vidoes which made some content providers uncomfortable so they wanted to hide it so it's less prominent. The functionality is still there. Using controlsist to hid the download button, authors can still download the videos by right clicking. Whereas telling them we will not provide this functionality would mean they switch to another element. If it's more effort for the author so they ahve more incentive to use the native element... these days using a custom element is a oneliner, not extra effort. There are several legit use cases for customising the gui. Right now it's no controls at all, or all the controls the browser has to offer. With something like thhis they can display controls appropriate to use case - not all require every control. And if there is a way to customise what is displayed browsers have incentive to make new functionality available to authors, who can choose whether to use it, rather than browsers weighing whether it clutteres the control ui or not. My udnerstanding is push back comes from apple who do not implement a download functionality anyway. Not sure what the best approach is here.

Peter: a lot of sites will mask the right click behaviour to prevent people from doing a right click download> That feels like a sense of drm that is not a use case we should enable. There are cases with platform specific controls that may or may not show that web devs may not be thinking about - like air play. When I pull up a video I can't air play it to my tv

Tess: webkit default controls on apple platforms have an airplay button, we also expoes a js api, which ended up contributing designwise to a standardised api. We expose a js api so if you're building custom controls you can build your own airplay, so you have the ability to do that too. 

Peter: very user hostile to hide controls that developers may not be aware of or thinking about that a user may find valuable. Developers are hiding them for aesthetic reasons

Tess: or capitalism reasons

Peter: I've turend of all controls and built my own because designer wanted a different look and feel

Lea: even though controls list is only supported in chrome, when we looked at actual usage ther ewas fairly significant useage on the web today, which does indicate user need

Tess: youtube may have adopted it

Lea: in terms of % of websites. Not just youtube.

Peter: that shows a developer need, not an end user need. Developer may be scratching an itch that is end-user hostile

Lea: sometimes you want a very small player and control which are the absolutely most important ones to display

Tes: yeah. Look at native controls in many browsers you might have a reduce set of controls visible depending on a bunch of factors

Lea: but browser doesnt know your use case - can only display what would work for some average

Dan: More what we need to do is write a document that captures this information, and post, or post a comment that says the essence of TAG discussion. We don't have consensus. We can see both sides. Sometimes it's okay to not have consensus. We can still point out issues like multi stakeholder. 

Tess: yeah. Lay out pros and cons. 

Dan: start a document? Progress it by plenary this week?

**we agree to 

### [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov

Peter: needs to be feature detectable

Dan: close based on feedback from Dominic? Satisfied with concerns? Or unsatisfied?

Peter: somewhere in between.. I want the feature but I think this is a huge mistake and really needs to be detectable in a way that will be backward compatible. The path Dominic is going down we cannot add detectability in a reasonable way. Unsatisfied.

Lea: agree with Peter

Dan: to plenary..

### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov
### [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov
### [`[css-values-4]` The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov
### [`[CSS-Values-4]` FYI review of Allow infinity, -infinity and NaN in CSS `calc()`](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov

## Breakout B (US / APAC) - [2022-04-12](https://www.timeanddate.com/worldclock/converter.html?iso=20220412T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Max, 

Regrets:

### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov

### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @atanassov

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion

### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov


## Breakout C (APAC / Europe) - [2022-04-12](https://www.timeanddate.com/worldclock/converter.html?iso=20220412T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Dan, 

Regrets: Sangwhan, Yves

### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou

### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion

Dan: Sangwhan left a comment. Looks like not much update since then.

Max: We had a discussion, the authors didn't respond yet

Dan: Plenary? Wait to next week for Sangwhan

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion

Dan: we are late on this one

Max: a couple of weeks ago Sangwhan and I had a discussion, and had a summary with further questions to ask, but didn't see Sangwhan send the questions. Probably we can discuss in plenary? My suggestion is to send the further questions.

Dan: yes. Do you have the questions? You can post them

Max: we wrote them in a google doc, I can't access it

Dan: let's see if we can get him to post those.. they're waiting. Left a note for Sangwhan.

### [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou
### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

## Plenary Session - [2022-04-13](https://www.timeanddate.com/worldclock/converter.html?iso=20220413T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Max, Dan, Hadley, Sangwhan, Amy

Regrets: Lea, Yves

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion

Dan: closing comment?

Sangwhan: questions and a closing comment. Will share questions. API design itself looks fine but there should be some safety nets. If you're on a single GPU system you can use any amount of GPU resources on the tab. Something you can do with WebGL but that's a bug not a feature.

.. My comments:

```
Higher granularity for selecting devices? For example, for cases where one wants to select a high-VRAM device (e.g. for machine learning workloads) or the non-dominant (e.g. secondary device which hopefully will not jank the current compositor) device.
Power consumption - while there is a mechanism to allow applications to request a high power vs low power device, wondering if the choice should be initiated by the user, and not the application
e.g. if the user is on the go, let them choose integrated GPU instead of discrete to save power
Revisiting position on permissions based on this data - and some informal asking around non-technical folks. Graphics is too generic and users will likely be confused - e.g. “yes, I guess the website needs graphics” when it is actually trying to mine Ethereum.
Instead of a permission, should this be something else..?
e.g. big fat warning suggesting “this will use lots of power”
Re: USVString vs DOMString - saw discussion LGTM.

```

Dan: proposed close?

Sangwhan: yes [will leave comment]

### [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo

Dan: Pending feedback, Peter left a comment..

Sangwhan: can nudge

### [Privacy Principles](https://w3ctag.github.io/privacy-principles/)

Dan: we're inching closer to issuing a fpwd of this document. I don't think it's done. But ready for fpwd. It's being developed by a task force with some TAG members in, and some ex-TAG. Preference would be.. the last time we did something from a task force it was the polyglot thing ages ago. We don't have a process. My impression was that the task force would issue a fpwd from the perspective of letting the AC know what we're doing and widening the feedback circle, rather than .. this becomes a finding. In order for it to become a finding it needs to be signed off on by the rest of the TAG but I dont' think it needs to go through that filter before we start getting wider feedback from the comunity. Is that okay?

Peter: status of the document is pretty clear. Does not yet have consensus. 

Hadley: Process makes sense. Might want to ask Jeni T for her opinion earlier than later. Spent a lot of time at ODI and current work on that.

### Plenary time

Peter: I'd like to move it an hour earlier

Dan: 7am UK.. is fine

Amy & Hadley: +1

### Face-to-Face June

* Pick a week
* Edinburgh or Nice?

### AC Sustainability Panel

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22) (14 untriaged)
