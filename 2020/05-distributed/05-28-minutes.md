## W3C TAG Virtual F2F
### Day 3 - 28 May 2020

Agenda: https://github.com/w3ctag/meetings/blob/gh-pages/2020/05-distributed/README.md

### Slot C

#### Breakouts 13 **06:30 - 07:30 UTC**

##### Breakout 13a - Alice & Dan

###### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479)

Dan: Came in 29 Feb, early review, we haven't really looked at it yet.

... Anchor is an overloaded term, between XR and Web. Unfortunately terminology is already well established in each domain here. Need to make sure to communicate clearly to developers that this is a completely different concept from `<a>`.

... Would also like some worked/visual examples of what "pose" and "anchor" refer to - there is a lot of description, but it's hard to follow for anyone not already familiar.

Alice: API details section doesn't list out the arguments for each of the methods...

Dan: Responses to security and privacy self-check look ok to me.

[Discussion of permission prompts for AR sessions] [example from Samsung internet](https://twitter.com/torgo/status/1263820803310747653)

Dan: notes that this is in the proposed charter for the upcoming charter renewal.

###### [Re-think information architecture for the design principles doc](https://github.com/w3ctag/design-principles/issues/177)

Dan: how do we want developers to read this doc? You (Alice) felt that developers should read the whole doc, I thought maybe they should read the first section and then refer to the rest as necessary.

... Perhaps we can approach from the point of view of what does someone see the first time they open this doc? Could be entirely boilerplate.

Alice: Does w3c publishing require this front matter? Could that come at the end?

Dan: One thing we could easily do is put some more content in the abstract.

Sangwhan: we need more plain language

Dan: on naming -  section 2 needs an intro

Alice: could use an intro before jumping into 2.1...

Sangwhan: front-load the tl;dr summary in every section

Alice: yes!  The point should come first - with an explanation after it.

Sangwhan: could we use "expanding" sections with a "read more"

Dan: I suggest 

###### Design principle issue lucky dip

##### Breakout 13b - *unused*

##### Breakout 13c - *unused*

#### Break **7:30 - 07:45 UTC**

##### Breakouts 14 **07:45 - 08:45 UTC**

##### Breakout 14a - Dan & Sangwhan

* <a href="https://github.com/w3ctag/design-reviews/issues/465">WebRTC DSCP Control API</a>

Sangwhan: we don't really have meaningful feedback...  Underlying stuff is more or less IETF...  We did provide some level of feedback and we said we don't have further feedback. They haven't replied back. My proposal would be to close.

[agreed to close]

* <a href="https://github.com/w3ctag/design-reviews/issues/495">AVIF Decode</a>

Dan: should we do something here? image formats come and go.

Sangwhan: they do not come and go. they come and stay.  Given that AVIF does become a thing, it may replace GIF - it has animations, there will be hardware implementations -- it could be a game changer.  

Dan: [Sends email to AB Chair.]

Dan: What should we do with this in the mean time?

Sangwhan: for this, nothing.  But they haven't addressed the implications for adding a new image format to the web platform. Any form of I/O into the web platform that takes or spits out an image will need to be considered when a new image format is introduced.  Things need to be added to APIs to support new image formats. I have an action to deal with that.  Another TAG action would be to make suggestions of where web platform needs to be patched up to support multiple image formats...



##### Breakout 14b - *unused*
#### Breakout 14c - *unused*#
#### Break **08:45 - 09:00 UTC**
#### Readouts/Wrap-up **09:00 - 09:30 UTC**

Alice: 13a - we talked about WebXR anchors...  we noted about use of term anchor.  we left some comments and filed an issue on the API details.

Dan: then we talked about IA for design principles.

Alice: we made a diagram...

Dan: we also talked about use of plain language - renaming priority of constituents - and putting a tl;dr at the front of each section.

Dan: 14a - Sangwhan & i closed DSCP control API - and then we talked about AVIF decode.  

Sangwhan: I have an action to figure out how to add a new image to the web platform and maybe publish a finding on that.

Alice: I edited during 14 and reviewed Sangwhan's PR.




### Slot A

* Breakouts 15 **14:30 - 15:30 UTC**

#### Breakout 15a - Ken & Tess
##### <a href="https://github.com/w3ctag/design-reviews/issues/486">Imperative Shadow DOM Distribution API.</a>

Propose close.

Draft closing comment:

> @kenchris and I looked at this again during the TAG F2F this week, and we're wrapping up our review. Overall we think this looks great, and while we would have preferred some default slot sugar, we understand why you're reluctant to add it. Thanks! Please open a new design review if your approach significantly changes in the future.

##### <a href="https://github.com/w3ctag/design-reviews/issues/487">WebAssembly SIMD review</a>

There's a new explainer they're prepping to send to us, so we'll hold off on this review until we get it.

##### <a href="https://github.com/w3ctag/design-principles/issues/111">guidance on inheritance between contexts</a>

We'll wait for the corresponding HTML change to land before writing a PR.

##### <a href="https://github.com/w3ctag/design-reviews/issues/472">Foldables CSS</a>

Propose close.

Draft closing comment:

> @hober and I took a look at this during our TAG F2F this week and your answer sounds sensible to us, so let's go ahead and close this. Thanks for flying TAG.

#### Breakout 15b - Dan & Hadley
##### <a href="https://github.com/w3ctag/design-reviews/issues/440">Screen Capture API (2019)</a>

Dan: Looks like they have responded well to our concerns and comments. Suggest closing.

##### TTML2

*not addressed*

##### Ethical Web Principles    
      
Dan: Tantek has proposed a new ethical web principle - [avoiding dark patterns](https://github.com/w3ctag/ethical-web-principles/issues/25). I'm not sure whether this should be an ethical web principle or maybe something in the design principles doc itself - referring back to one of the existing principles? [New design principle](https://github.com/w3ctag/design-principles/issues/196) issue opened. 

#### Worked on DR Intro 

Did a [design principles PR](https://github.com/w3ctag/design-principles/pull/197) for the revised title and intro.  Also closed Issue 153 as it was redundant.
      
#### Breakout 15c - David & Peter
    
##### <a href="https://github.com/w3ctag/design-principles/issues/173">add principle on media independence</a>

> <h3 id="devices-platforms">Support the full range of devices and platforms</h3>
> 
> Features on the web should work across different input and output devices,
> different platforms, and different media,
> as much as this is reasonably possible.
> For example, they should not be specific to a particular screen size, 
> a particular operating system or browser engine,
> or assume the user is using a mouse.
> Some features don't reasonably work across all of these cases:
> for example, hyperlinks don't work when printed on paper,
> and '':hover'' doesn't work on touch input devices where there isn't a mouse pointer position,
> but these features are still valuable across a range of devices,
> and could be adapted to devices that don't support their original intent
> (for example, hyperlink targets could be converted to footnotes when printing).
>
> Features should also be designed so that the easiest way to use them
> works across devices as well.
> For example, the simplest way of using a feature for positioning of content
> should encourage doing so based on where the other content is
> rather than using pixel positions,
> so that it works across devices of various sizes,
> across browsers and operating systems that have different fonts available,
> and across different user settings for default text size.

Made [a PR](https://github.com/w3ctag/design-principles/pull/198).

##### <a href="https://github.com/w3ctag/design-principles/issues/174">add principle on backwards compatibility / supporting existing content</a>

didn't get to this

##### <a href="https://github.com/w3ctag/design-principles/issues/175">add principle on forwards compatibility / graceful degradation</a>

didn't get to this

##### <a href="https://github.com/w3ctag/design-principles/issues/186">Link to the CSSWG's FAQ</a>

Closed with comment:

> @plinss and I looked at this during a breakout in the TAG's virtual face-to-face today.
>
> We're not sure how useful this link would be; we're trying to link to things that people designing new features would find generally useful.  We think this FAQ probably doesn't fall into that category, at least partly because it's targeted more at the audience of developers using CSS rather than those designing new CSS features.
>
> (We're also a little unsure how *frequently* some of these frequently asked questions are; perhaps it's the obscurity of the first one that threw us, though.)
>
> We'd be happy to link to a set of CSS principles that fills the role of advice for designers of new features.

#### Break **15:30 - 15:45 UTC**

#### Breakouts **15:45 - 16:45 UTC**
#### Breakout 16a - Dan & Tess
##### Security & Privacy Questionnaire
###### [Geofencing link is not helpful](https://github.com/w3ctag/security-questionnaire/issues/61)

Tess: i don't think we should change the reference because: the TR space doc is gutted.  So it doesn't contain any text to help the reader who might follow that link.  So I would be OK to using that link in addition, but not replacing.

Dan: and I don't think it makes sense to link to another obsolete doc.. so let's keep it.

###### [should we further mitigate threats of identifiers in local storage because some mechanisms won't clear all local storage?](https://github.com/w3ctag/security-questionnaire/issues/80)

Tess: there is work going on in Web Priv CG and WHATWG which could obviate the need for this - so we should wait until that work progresses and then add something to address this issue if appropriate.

##### <a href="https://github.com/w3ctag/design-principles/issues/180">Add principle discouraging device enumeration.</a>

Dan reviewed and approved this PR. It's blocked on a change to tobie/specref.

##### <a href="https://github.com/w3ctag/design-principles/issues/197">Changed Name and added expanded Abstract</a>

Tess reviewed and approved this. We spent some time bikeshedding.

##### <a href="https://github.com/w3ctag/design-principles/issues/199">Add guidance on when to use which Web IDL string type</a>

We talked through the change and some of the complexity around it. Dan reviewed and approved the PR.

#### Breakout 16b - David & Ken & Rossen

##### <a href="https://github.com/w3ctag/design-reviews/issues/306">CSS content-visibility property</a>

Rossen: The work is ongoing and getting traction with the CSSWG at this point. Since its opening the issue has moved away from Display Locking and into content-visibility. There isn't a dedicated explainer anymore. 

Kenneth: Where did `hidden-matchable` go; it looks like it was needed to address use case (2).

Kenneth: So CSS WG is working on this now?

Rossen: definitely

Rossen: display locking parts are split into 3 design reviews now, right?

Kenneth: core idea was to solve efficient performance of list views / virtual scrollers.

Rossen: also a lot of feedback on a11y.

Rossen: how much of original display locking effort covered by these 3 specs?  What happens if one of them gets dropped?

Kenneth: ?

Rossen: We had a long thread about a11y and the 4/5 different values.

Rossen: do you see a reason to keep this issue open?

David: I'm ok with closing it.

<blockquote>
  
@dbaron @kenchris and myself took another look this issue, now scoped to content-visibility only. It would be good to update the explainer to match the CSS Containment module, ex. the value `hidden-matchable` is no longer part of the spec. 

We advise you to continue working with the CSSWG in completing the rest of the spec.

</blockquote>

##### <a href="https://github.com/w3ctag/design-reviews/issues/371">File Handling</a>

(reading through old review comments)

Proposed comment for closing issue:

<blockquote>

@kenchris, @atanassov, and I just discussed this in a breakout at the TAG's virtual face-to-face meeting.
  
I think we're happy with closing this issue at this point.  We've provided a good bit of feedback, which you've been responsive to, although I think some of it probably still needs to be incorporated into the explainer.
  
As an early-stage review, we're not expecting a full spec at this point.  But we would encourage you to continue to solicit feedback from relevant parties, and if the specification continues to make progress, to try to find an appropriate standardization venue for it.

</blockquote>



##### <a href="https://github.com/w3ctag/design-principles/issues/137">Best practices for feature detection in JavaScript</a>

David: Some pages might care if a feature is supported vs is a given hardware available. Such detection isn't adding entropy in general is useful.

David made [a PR](https://github.com/w3ctag/design-principles/pull/201) to clarify that but there's still more to do on this issue.

##### <a href="https://github.com/w3ctag/design-principles/issues/112">Create advice for how to handover access to sensors and devices on dedicated workers    </a>

didn't get to this

#### Breakout 16c - Hadley & Yves
##### <a href="https://github.com/w3ctag/design-reviews/issues/240">The web platform needs a service discovery mechanism</a>
##### Design principle issue triage
#### Break **16:45 - 17:00 UTC**
#### Readouts/Wrap-up **17:00 - 17:30 UTC**

Present: Rossen, Tess, Peter, Dan, Kenneth, David, Yves

15a:

Tess: we look at the imperative shadow dom dist api - we think it's good to go. \

[consensus recorded]

... SIMD review - they asked us to hold off

... guidance on inheritance between contexts - interesting - policies inherit between contexts differently. Spec authors have to come up with their own way to do it each time- how do we encourage people to converge. There was a path forward written up based on session at TPAC last year. so... ken & I think what makes sense is to wait for change to HTML - then we can add some simple guidance that points to that.

... Foldables CSS - we are proposing to close it. 

[consensus recorded]

15b:

Dan: Screen capture API - propose close or could bump to future call...

Tess: reasonable [to close]


Dan: PR on Design Principles - new title "Web Platform Design Principles" - [consensus on this] - 

15c:

David: all design-principles breakout - we spent most of the time on media independence - I have [a PR up](https://github.com/w3ctag/design-principles/pull/198) to add that principle. 

... we closed Design Principles issue #186.

16a: 

Tess: all of the open issues on S&P questionnaire - we closed geofencing issue - triaged rest of them. One we should hold off on until some related work happens.  We then looked at 3 different PRs on the design principles document. [Device enumeration](https://cryptpad.w3ctag.org/bounce/#https%3A%2F%2Fgithub.com%2Fw3ctag%2Fdesign-principles%2Fissues%2F180) - Dan reviewed and approved.  Can we land it?

[consensus to approve]

... Dan's change to name and abstract - we fixed a syntax - will wait for Sangwhan.

... [Adding guidance on when to use which IDL string type](https://github.com/w3ctag/design-principles/issues/199)...  Anne made a comment I should address.  I will try to address his issue and we can land it in slot B mini plenary.  

16b: 

Rossen: we looked at 3 issues - we closed 2 of them. CSS content visibility - this is part 1 of 3 of which used to be display locking.  The work is healthy and ongoing with CSS working group.  Healthy discussion for this feature. In closing comments we suggested this work continues there and they update the explainer to match the spec. **closed**

... other one we looked at was file handling... similarly as an early draft all the issues raised were addressed - we want it to be out of WICG. **closed**

... best practices for feature detection - David made [a PR](https://github.com/w3ctag/design-principles/pull/201) that differentiates ... don't think it's complete yet but this PR will move us closer to the end goal.  We may want to link this to the device enumeration section - if your detection is about hardware then look at this other section...  [Rossen adds issue].  

... We didn't get to last one which was about handing device / sensor to dedicated workers...

##### PRs to land

<a href="https://github.com/w3ctag/design-principles/issues/180">Add principle discouraging device enumeration.</a>

Landed.

<a href="https://github.com/w3ctag/design-principles/issues/197">Changed Name and added expanded Abstract</a>

Will land in Slot B's breakout after Sangwhan approves.

<a href="https://github.com/w3ctag/design-principles/issues/199">Add guidance on when to use which Web IDL string type</a>

Probably shouldn't close this until Tess adjusts based on Anne's review comments.

### Slot B
  * Breakouts 17 **22:30 - 23:30 UTC**
#### Breakout 17a - Alice & Tess

##### <a href="https://github.com/w3ctag/design-principles/issues/160">Incorporate a generalization of the "HTML Design Principles" document into our principles</a>

Alice reviewed two open PRs which each fall under this umbrella issue, and Tess iterated on one of them with her. We will hopefully be able to land them in the mini-plenary:

* <a href="https://github.com/w3ctag/design-principles/issues/190">add several HTML Design Principles related to interoperability</a>
* <a href="https://github.com/w3ctag/design-principles/issues/198">Add section on supporting the range of devices and platforms.</a>

##### <a href="https://github.com/w3ctag/design-principles/issues/169">add a section describing what should be in HTML versus CSS versus JavaScript (the separation of concerns)</a>

Ran out of time and didn't get to this.

##### <a href="https://github.com/w3ctag/design-reviews/issues/468">Review the HTML spec's treatment of focus</a>

Ran out of time and didn't get to this.

#### Breakout 17b - David & Rossen
##### <a href="https://github.com/w3ctag/design-principles/issues/170">generic advice about preferring booleans, and maybe advice on boolean versus string versus enum</a>

David: This is about seeing if there's something more generic we could say about booleans to combine https://w3ctag.github.io/design-principles/#prefer-dict-to-bool and the boolean bit of https://w3ctag.github.io/design-principles/#css-naming .

David: I think we should just close this; I think they're sufficiently different that there isn't a generic version of them.

Rossen: Looking through both sections CSS and JS, it seems we have pretty good coverage and advise already. It is worth underlying that for CSS our recommendation is pretty firm, don't use booleans. For JS on the other hand is softer, preferred not using them though return parameters for synchronous functions that are boolean in nature don't necessary need to avoid being boolean...

##### <a href="https://github.com/w3ctag/design-principles/issues/172">add a principle on "no dataloss by default"</a>

David: maybe others are higher priority; this is about layout systems which we don't cover yet

(skipped for now to go on to the others)

##### <a href="https://github.com/w3ctag/design-principles/issues/50">give advice on read-only lists</a>

(reading of issue and things linked from it)

David: I added [a comment](https://github.com/w3ctag/design-principles/issues/50#issuecomment-635655173).

##### <a href="https://github.com/w3ctag/design-principles/issues/99">Is `partial` a long term maintainability problem? If so, how do we fix it?    </a>

##### [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464)

(spent a while reading the explainer)

David added a comment about one thing that was confusing

#### Breakout 17c - Peter & Sangwhan

##### <a href="https://github.com/w3ctag/design-reviews/issues/370">WebHID API (Human Interface Device)</a>

Pending feedback, but we didn't comment in their repo or @ them, Sangwhan is opening issues in their repo, and we'll revisit in one month.

Still have concerns about API layering here, this in principle builds on WebUSB and Bluetooth and is related to gamepad, but all are unrelated interfaces.

##### <a href="https://github.com/w3ctag/design-principles/issues/39">Non privacy related design notes on device APIs</a>

Needs a PR, Sangwhan will work on it offline.

##### <a href="https://github.com/w3ctag/design-principles/issues/56">Guidelines for binary stream-likes should be added</a>

##### <a href="https://github.com/w3ctag/design-principles/issues/85">describe principles for naming of locking/unlocking APIs</a>

#### Break **23:30 - 23:45 UTC**
* Breakouts 18 **23:45 - 00:45 UTC**

#### Breakout 18a - Sangwhan & Tess

##### <a href="https://github.com/w3ctag/design-reviews/issues/285">Carriage of Web Resource in ISOBMFF</a>

Draft closing comment:

Hi,

@cynthia and I took another look at this during the TAG F2F this week, and we think we can close this review. We encourage all of the interested parties to attend the upcoming related W3C workshop, which we hope will be an excellent opportunity for media people and web people to collaborate in this area.

##### <a href="https://github.com/w3ctag/design-reviews/issues/512">making the "total" field optional in PaymentRequest API</a>

Tess: You and Ken looked at this in a breakout and wanted to close, but then I noticed a couple of things and started a discussion. The most recent comment is from a colleague of mine, who makes the excellent point that having both a pending total and optional total would be really confusing for authors. Doesn't look like the person who filed this review issue has replied to that point yet.

Sangwhan: let's ping the OP to see what they think of the recent discussion, and put the milestone out a couple of weeks.

##### <a href="https://github.com/w3ctag/design-principles/issues/157">Review different cross-domain import mechanisms and their security models  </a>

Sangwhan: Not sure what we should be doing here

Tess: So this was initially in design reviews, and the issue at hand was about JSON modules being executable when the importer intends to only use it as data. TC39 is working on a proposal to fix this problem, but it may take some time.

Sangwhan: Would this be a problem if we ever get any mechanisms that have eval() like behavior upon fetching a foreign resource that is not import? (Question with no answer atm...) e.g. importer specifies that they intend this to be data only

Tess: Think we'll have to see the TC39 proposal and see if this warrants a principle or if the infrastructure will just magically deal with this for you. We should probably revisit when the proposal have advanced a bit more

Sangwhan: SGTM. Let's set a future milestone.

##### Design Principles PR merge-fest

We merged several of the less-controversial Design Review PRs that have been written recently.

#### Breakout 18b - David & Alice

##### <a href="https://github.com/w3ctag/design-reviews/issues/72">Task Scheduling</a>

skipped

##### <a href="https://github.com/w3ctag/design-reviews/issues/338">scheduler.postTask() API</a>

skipped

##### <a href="https://github.com/w3ctag/design-principles/issues/168">Further clarify the priority of constituencies principle</a>

discussed and Alice wrote https://github.com/w3ctag/design-principles/pull/204 which we discussed and refined

#### Breakout 18c - Rossen & Peter

##### <a href="https://github.com/w3ctag/design-principles/issues/55">Need guidance on returning error values vs throwing exceptions</a>

Peter: We have some good recommendations about rejecting vs error in the promises guide. However, we should have something in the design principles that's a bit more general and still captures the idea and main difference between errors and exceptions.

Rossen: Execution failure or exception occurs whenever a member cannot do what it was designed to do (what the member name implies). Everything else should be an error and communicated as such.

Peter: Yes, for example if I was making a network request and I'm not connected I would expect that to be an exception since the function is not capable doing what it was intended to do. Now, if the network is connected and the server returns 500 or 400 etc. hmmm debatable but probably still an exception.

...Similarly if I call a method with the wrong type of argument, and it can never work, throw an exception, or if the system is in a state where the function will never work.

Rossen: Yes, everything else is an error.

Peter: other general statements: exceptions should not be used for 'normal' control flow, but rather reserved for exceptional situations.

Rossen: Agreed. Given that exceptions are way smaller subset of failure modes, we should try and define what they are and suggest that everything else is most likely an error.

... Anything that prevents a member to complete its intended functionality with a normal failure mode is an exception. Examples are invalid input or invalid context.

Peter: It is unfortunate that the recommendation will not be backwards consistent but it is a good start and hopefully will help future API.

Rossen: OK, I'll start a PR most likely against section 5 or 7.4 in the design principles and let y'all poke holes in it.

Post breakout notes from Peter: 
1) we should also give some advice about how to return errors,  e.g. it the API is expected to return an object and there's a single failure mode, return `null`, if there are multiple failure modes that the caller needs to know about, either return an array with multiple values, or a single object that contains the successful result and/or error information (we should probably favor a pattern, personally I find APIs that return `null` and then have other methods to fetch error data annoying). An example of the latter approach is Fetch.
2) We should give examples of APIs that follow our guidance, and historical APIs that don't, and how they 'should' have been designed following this advice. An example of something that throws which should have returned `null` is getUserMedia() (return null when camera unavailable, throw if invalid constraints were passed).

### Break **00:45 - 01:00 UTC**

### Readouts/Wrap-up **01:00 - 01:30 UTC**

#### 17a readout - Alice and Tess

Tess: Looked at the "HTML Design Principles" umbrella issue - used time to review Tess' PR and David's PR under that umbrella. Think both PRs are ready to go. That took the whole breakout.

#### 17b readout - Rossen & David

David: We had a list of design principles issues... Domenic had been skeptical on one of them, we agreed and decided to close without change.

... Skipped the "no dataloss by default" issues, seems too in the weeds for now.

... Thought about "read-only lists", David realised didn't understand the situation well enough and asked some questions on the issue.

... Pulled in an issue on Origin isolation. Didn't make that much progress. Added a comment about sites that are cross-origin but same-site, which is inherently confusing. Or maybe it's cross-site but same-origin.

Tess: I think it's the former.

David: I couldn't even follow all the definitions in the spec.

#### 17c readout - Sangwhan & Peter

Sangwhan: One design review and three design principles.

... Web HID API. Some comments and some concerns. Have escalated those. Spec author replied back an hour ago, we should probably review their response.

... We're ok with the spec, with a question about privacy and about ???

... Didn't do a lot on the design principle issues. Non-privacy design guidance on device APIs. Sangwhan will make a PR.

... Binary stream-likes, didn't do much on that.

... Principle for naming of locking/unlocking APIs. Not just about locks/unlocks but also about pattern. Did a very early draft of "how to name things when you are using X pattern". Started with locks and streams.

... Will add a small section inside the naming section to give guidance on this case. Guidance on a more idiomatic pattern. No PR yet.

#### 18a readout - Tess & Sangwhan

Tess: Carriage of Web Resource in ISOBMFF. ISO spec has been published, so somewhat overtaken by events. W3C trying to organise a workshop, figure out what next steps are. We commented saying we plan to close it and that we hope everyone goes to the workshop. Thanks for flying TAG.

... Making "total" field optional in PaymentRequest API. Some comments that the OP hadn't seen. Bumped.

... Design principles: cross-domain import mechanisms. Really looking at modules. We looked at this, got the impression that TC39 is handling this well. There is an early-stage proposal which we hope to see progress. Makes sense to wait for that to progress.

... Went to merge a bunch of design principles PRs.

#### 18b readout - Alice & David

Alice: went straight to design principle on clarifying priority of constituencies design principle.  Did some iteration, but should probably wait for wider review before merging.

#### 18c readout - Rossen & Peter

Rossen: I pulled Peter into an 18c breakout.

Rossen: We spent entire time on the first issue - getting proposed guidance on returning error values versus throwing exceptions.  We looked at promises guide, which has some language on error handling and discouraging use of exceptions except for exceptional cases, but without a good definition of what that means.  We spent the entire time talking about what this should be.  We arrived at -- since in JS, exceptions are a tiny subset of the normal errors, we're trying to define exceptions -- anything that prevents a function from completing its intended functionality.  For example, invalid inputs or invalid context.  Everything else is recommended to be a normal error.

Rossen: Action for me to make a PR, most likely section 7.4, and then let others add to it.

Rossen: We went through some bigger specs to see how accurate guidance will be -- found that to some degree it will be ok, but some examples where this isn't true.

#### PRs to land if we can

##### [Changed Name and added expanded Abstract](https://github.com/w3ctag/design-principles/pull/197)

Dan authored, Tess reviewed.

Tess summarizes.

Peter: I suggested change in title... but there are some other places where we're using API inappropriately.  I think we should probably fix those before merging, although if we merge this we could open a followup issue, but make sure to do that.

Alice: What do people think about last sentence?  Controversial for me.

Tess: We shouldn't really be telling people to skip the rest.

Consensus to delete the last sentence.

##### [Add paragraph about device detection to clarify advice on feature detection](https://github.com/w3ctag/design-principles/pull/201)

David authored, Rossen and Tess reviewed.

merged.

##### [add several HTML Design Principles related to interoperability](https://github.com/w3ctag/design-principles/issues/190)

Tess authored, Alice and Anne reviewed.

Merged

##### [Add section on supporting the range of devices and platforms](https://github.com/w3ctag/design-principles/issues/198)

David authored, Alice and Tess reviewed.

Still need to address review comments.

##### [Add a subsection about using "unsafe" in names](https://github.com/w3ctag/design-principles/pull/193)

David authored, Anne reviewed.


































































