## TAG Teleconference
##### 06-08 July 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-07-06](https://www.timeanddate.com/worldclock/converter.html?iso=20200706T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Guide spec authors to use one manifest (web app manifest)](https://github.com/w3ctag/design-principles/issues/95) - @torgo, @kenchris & [Proliferation of manifests at W3C](https://github.com/w3ctag/design-principles/issues/148) - @torgo, @kenchris
* [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron
* [guidance on use of JSON-LD?](https://github.com/w3ctag/design-principles/issues/128) - @hober, @dbaron, @hadleybeeman
* [Can we use `media` in WebNFC?](https://github.com/w3ctag/design-principles/issues/140) - @hober
* [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron
* Security & Privacy PRs & Issues
* Promises Guide Issues


#### Breakout B (US / APAC) - [2020-07-06](https://www.timeanddate.com/worldclock/converter.html?iso=20200706T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [API v Feature PR](https://github.com/w3ctag/design-principles/pull/207) - @plinss, @alice
* [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron
* [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron
* [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron
* [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-principles/issues/157) - @hober, @cynthia
* [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron
* [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185)

#### Breakout C (APAC / Europe) - [2020-07-07](https://www.timeanddate.com/worldclock/converter.html?iso=20200707T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* MiniApp feedback
* [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia
* [How should the toJSON method be used?](https://github.com/w3ctag/design-principles/issues/116) - @cynthia, @kenchris
* [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia
* [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @torgo
* [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @torgo

#### Plenary Session - [2020-07-08](https://www.timeanddate.com/worldclock/converter.html?iso=20200708T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Dan, Rossen, Tess, Yves

Regrets: Peter, David


#### [Guide spec authors to use one manifest (web app manifest)](https://github.com/w3ctag/design-principles/issues/95) - @torgo, @kenchris & [Proliferation of manifests at W3C](https://github.com/w3ctag/design-principles/issues/148) - @torgo, @kenchris


Dan: I feel like the PR we did addresses both 148 and 95 and we can close both.

[agreement]

[issues closed]

#### [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron

[deferred to B]

#### [guidance on use of JSON-LD?](https://github.com/w3ctag/design-principles/issues/128) - @hober, @dbaron, @hadleybeeman

Tess: I think we should at least add text to the principles to say "specs should not define JSON structures that be optionally be interpreted as something else"... I think this is the core of @dbaron's concern. Saying "interpret this as either JSON-LD or as plain-old-JSON" is just asking for interoperability problems, and could easily cause a race-to-the-bottom where browsers are forced for compat reasons to implement an underspecified mix of "JSON-LD" processor that is neither compatible with plain-old-JSON processing nor JSON-LD processing.

Dan: that looks good to me.

Tess: i will write a PR

Rossen: Ship it!

#### [Can we use `media` in WebNFC?](https://github.com/w3ctag/design-principles/issues/140) - @hober

Tess: I think this is a mismatch in terminology between two different communities. In the NFC world they use the world media type for what in the web world we call a mime type. So anne's request to the webnfc people was to call it mime type instead of media type. WebNFC people are concerned NFC people wil be confused. Anne's concern is the other way around. I think it's a straightforward problem that arises in APIs that straddle communities.  I worry about the web... i would prefer it to match to the rest of the web stack. Even more, nobody should die on this hill. 

Dan: I agree with your view Tess that we should look at it from a web developer perspective.  Teh webnfc API is not for NFC developers to use the web. It's for web developers to use NFC.

Tess: yes.

Tess: analogy - web has keypress events - i think it would have been a mistake for the key events on the web to follow the PS2 or ADB naming conventions.  

Rossen: I was following their spec - they already have a good section on terminology and conventions. They could take advantage of that and define these terms. The best path forward would be to 

Dan: maybe the design principle is to say "When developing a web API interfaces with a technology stack, naming conflicts like [this] arise, the preference should be towards the web ecosystem naming convention rather than the other community" something like that...

Tess: I wrote a comment. 

Rossen: I can finish that PR.

#### [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron

Rossen: if you look at Elika said on this topic:

> Another principle is no dataloss by default. The content should always be visible by default. If you did not try to hide it, then you will see it somewhere on the page. This also means we want the content to be readable by default. Even if it “visible”, if you put everything on top of each other, it's not readable. A layout system that by default places everything in the top left corner on top of each other is not a system that we want to have. This is also why the boxes in CSS automatically grow to fit their content, unlike other design systems where you create a fixed-size box, and if there is too much content, it overflows or is clipped.

Rossen: this one is very presentation-oriented ... we have principles on CSS so this fits well. 

Tess: it says "data loss" but the description is very CSS focused and making sure the page is visible to the user. Using data loss is confusing because web has APIs where data is transfered. IndexDB e.g. Current titling of this doesn't fit for the API cases. I would prefer it to say something like "content needs to be accessible to users" that would imply something about CSS and more. The current title suggests to me that IndexedDB shouldn't have a "delete this database" call.

Rossen: I had similar reactions. This is about presentation - mostly visual presntation and layout. You can an author can make something accessible to a screen that isn't visible to a print media. So I agree with what Tess said. If we specify anything it shouldn't be worded as "data loss" - rather accessibility or something similar though that may be too narrow.  On the flipside to extrapolate beyond CSS I don't know if there's going to be an easy principle. Network, strage, etc... APis. 

Tess: as far as taking a stab at writing a PR should probably be David.

[defer to plenary]

#### Security & Privacy PRs & Issues

Tess: 2 open PRs ([w3ctag/security-questionnaire#90](https://github.com/w3ctag/security-questionnaire/pull/90) & [w3ctag/security-questionnaire#91](https://github.com/w3ctag/security-questionnaire/pull/91)) which are waiting on Dan to review.

Dan: waaaaat?

Dan: Will review and let's see if we can land them at the plenary.

Tess: there are also several open issues: https://github.com/w3ctag/security-questionnaire/issues

Tess: In particular, I'd like help with [w3ctag/security-questionnaire#83](https://github.com/w3ctag/security-questionnaire/issues/83).

[Everyone looks]

[Dan comments]

[let's bring up at plenary]

#### Promises Guide

Rossen: https://github.com/w3ctag/promises-guide/issues/29 is ready to be closed. Should we do it here or wait for plenary

Dan: let's close it now

 [Closed]

### Breakout B

Present: Alice, David, Rossen, Tess, Peter
Regrets: Sangwhan

#### [add a principle on "no dataloss by default"](https://github.com/w3ctag/design-principles/issues/172) - @dbaron

Rossen: in breakout A we talked about the no dataloss by default principle.

... Agreed it was poorly named because many APIs do allow data loss. Elika's definition is fairly narrow, left it to you to figure out if there's anything else to be defined there.

#### [API v Feature PR](https://github.com/w3ctag/design-principles/pull/207) - @plinss, @alice

[missed a bunch]

Peter: The thing I care about is having two distinct terms to represent when we're talking about JavaScript APIs or when we're talking about things that are more general, and using them consistently.

Alice: How much of that is underpinned by the history of the document?

Peter: I went through all the uses of "API" and decided what they meant.

Tess: Could also try to avoid generic terms like "API" and "feature" and talk about "HTML elements" etc.  But that only gets us so far; some sections need generic terms.  I think API is a sensible generic term for the naming section.

Alice: Maybe I can work on a PR (with Tess or Peter?), after I land my other PR that trims word count a lot.

Peter: We do need generic terms.

#### [Is `partial` a long term maintainability problem?  If so, how do we fix it?](https://github.com/w3ctag/design-principles/issues/99) - @dbaron [from A]

[missed]

Tess: Do we need more consensus on this before we make a PR?

David: Yes, I think so. Right now we don't have enough consensus for a PR. Not much to do on this today, other than encouraging others to think about it and weigh in.

Peter: Could do something with tooling. Shepherd (?) has a list of links out to all other specs. Would be possible to have bikeshed and respec annotate the spec that has the base interface with links out to all the other additional partials. Kind of a hybrid solution, depends on what the annotation looks like what those links should look like - a list of partials right in the original document, or footnotes, or...

David: Would have to be very careful about levels of maturity.

Tess: File issues on bikeshed, respec, wattsi?

David: Could propose in this issue before filing a bunch of issues.

Peter: I can add that comment.

Tess: Might be worth prototyping in one of the tools. What would it look like? Mock up a spec with a possibility of what the output might look like.

Alice: What the output might look like vs. the engineering cost of implementing it.

#### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41) - @cynthia, @dbaron

Tess: Sangwhan isn't here...

David: I haven't looked at this since last month. It's been a few months, at least.

Tess: How does this relate to the issue we filed to do an overview on mechanisms for setting policies on IFRAMEs?

David: That was part of the work I started to do on this issue, but I hadn't gotten very far.

Tess: Could we combine/dupe these issues?

David: Maybe... would need to look at both of those issues. They are in two different repos.

Tess: So you're still working on a PR on this one...

David: "working on", sure.

#### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142) - @hober, @alice, @dbaron

Tess: We made a list of options, in no particular order. Can we make a PR with these options?

Alice: Nigel's point is interesting as well.

Tess: We should add that option to the no-compromise option list.

David: Not sure about the numbering...

Alice: The numbering is silly, but it does indicate that the no compromise positions are as such.

Tess: Option "-2" is a compromise position? 

Tess: Any volunteers to write the first PR?

Alice: I'll do it. I'll include Nigel's option, and we can discuss where it should go when we have the PR.

#### [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-principles/issues/157) - @hober, @cynthia

Tess: We haven't started on this. We should set up a breakout for the two of us.

#### [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169) - @hober, @alice, @dbaron

Tess: We have this project to move the HTML design principles into our design principles doc.

.. It's popular in terms of people citing it, but there's some controversy about its value/correctness.

Alice: a problem here is that "semantic" is poorly defined.  (in "strikes a balance between semantic expressiveness and practical usefulness".)  A bunch of elements like `section` etc. that don't come with any default presentation or emantics that are useful to users.  I'm familiar with uses for assistive tech, maybe other uses for non-presentational use of HTML.  I'm not sure what "semantic" is trying to mean here.  I don't think vast majority of HTML and CSS authors understand what "semantic" means in this context.  And they don't experience semantics other than visual presentation and interactivity.

Tess: e.g., with the argument about the outline algorithm, browsers don't surface results of running the outline algorithm.  Users see that headings are a different size.  A user of AT does get to navigate by headings.

Alice: Can be a poor experience.

Alice: I'd be interested in what, other than AT (which I have a good understanding of), what "semantic" is meant to mean.

Tess: tautological?  "semantics" just means "meaning".

Tess: In an HTML tutorial, you'd say that the `p` element is for paragraphs.  Paragraph is the semantic of the `p` element.

Alice: If I use a `div`, what difference does it make?

Tess: None other than maintainability?

Alice: how does it help maintainability?

Tess: Makes the intent clear from the markup.

Tess: Example: blog whose markup is all `div`s is hard to work with; element names are not useful.

Alice: What if writing React?  Is there still value in semantic HTML?

Tess: Presumably you're using the developer tools?

David: I recently wrote a [blog post](https://dbaron.org/log/20200221-dom-identity) that's sort of related, about ...

... semantics in the context of React has more to do with the identity of objects over time than the tag names.

Alice: ...operating without javascript?  default styling, default mappings of things into CSS?  (Argued about this point for `inert`.)

Alice: I'd like to understand context of original principle and what it can be useful for before we try to rewrite it.

Tess:  What's this principle been used for?  Arguing about whether things belong in HTML or CSS?  The things that come to mind are the exceptions, like `<meta viewport>`.  People agree in abstract way that it belongs in CSS, but we finally agreed in CSS within the last few years that we couldn't do it.  Belongs in HTML despite offence to theoretical purity.

Alice: `pointer-events`, CSS `content`.

Tess: I forget if it's `dir` or `lang`...

David: ... Elika argued that `direction` shouldn't have been in CSS, just `dir` in HTML.

Tess: Can we use the exceptional cases to define a modern version of this principle?

Alice: I want something that gets to what this is trying to do, without the undefined "semantics" term in the middle.

#### [Security / Cryptography Principle?](https://github.com/w3ctag/design-principles/issues/185)

### Breakout C

Present: Ken, Sangwhan, Dan, Alice, Yves

Regrets: 

#### MiniApp feedback

Dan: there will be a miniapps call organized by w3c to discuss our feedback later this week - tba.

#### [Non privacy related design notes on device APIs](https://github.com/w3ctag/design-principles/issues/39) - @cynthia

Sangwhan: some has been addressed in section 8 of the doc but some needs to be done.

Alice: [working on general PR]

Sangwhan: will wait until Alice's PR lands to work on a PR on this.

#### [How should the toJSON method be used?](https://github.com/w3ctag/design-principles/issues/116) - @cynthia, @kenchris

...discussion on this issue... and agreement on Sheppy's comment](https://github.com/w3ctag/design-principles/issues/116#issuecomment-635401864).

Sangwhan: general object serialization is a missing featue of TC39 [ecmascript] rather than the web. JSON cannot be extended at this stage to accomodate all the new [cases]. If the object can be represented in JSON and it can be reconstructed... it uses the same serialization provided by the object.... No interface declaration... 

Dan: shall we punt this to TC39?

Sangwhan: [leaves comment summarizing the issue]

#### [clarify advice on synchronous versus asynchronous APIs](https://github.com/w3ctag/design-principles/issues/145) - @cynthia

Dan: haven't we already issued a lot of guidance on this?

Sangwhan: we've promoted promises in some cases beyond where it makes sense.  "you should prefer async" is scattered all over the design principles doc.

Dan: to the exclusion on when you should use sync?

Dangwhan: yes there is no guidance on when you should use sync - maybe there should be a small section on that?

Ken: like property [setting]? Some of these things are simple and just return a value.

Sangwhan: that's what the concern is about.  Sometimes setting up a promise might take longer than running the function itself.

Sangwhan: [writes the text live and sends PR]().

#### [Taking debugging use cases into account in W3C specifications](https://github.com/w3ctag/design-principles/issues/156) - @torgo

Sangwhan: So APIs are debuggable. But it makes sense for things like CSS.

Dan: so we could say something like "new features should be debuggable"... shoudn't that be part of the extensible web promise?  Are there good examples of this we could point to?

Alice: person who filed the issue mentioned the web animations spec as a good example.  And they go on to list flexbox as a negative example.

Sangwhan: i did notice that we don't have anything about meaningful errors. that's something we could add. 

Ken: we had people tell us not to introduce new errors and events.. then you add a lot of objects to the platform...

Sangwhan: but we don't have a principles of "meaningful error messages in an exception"... 

Alice: please add me...

#### [Considerations and pre-cautions when adding new media formats](https://github.com/w3ctag/design-principles/issues/171) - @torgo

Yves: related to http mime types... 

[discussing Dominic's comment]

Yves: in th case of AVIF do we want to do decoding in JavaScript (using `fetch`) or do you want to do it in a native way or in that case use `<video>`

Sangwhan: design principles... does it fit here? not a API surface...

Dan: We did expand the scope beyond client-side APIs...

Sangwhan: Dominic's comment is not related to this particular issue but it is somewhat related. 

Sangwhan: this  is a bigger PR...  There has been no documented history of how we added media formats to the web platform - it's been mostly on the browser implementation side. If you add support for a new image format then you need to use that for output from canvas for example. So this needs some more investigation. 

Dan: could we crowd-source the work on discovering these things to the rest of the TAG?  

Sangwhan: Github issues here...

#### readability

Alice: [ [introduces PR 219](https://github.com/w3ctag/design-principles/pull/219) ]

### Plenary Session

Present: Kenneth, Peter, Dan, Tess, Alice, David, Yves, Rossen

Regrets:

#### Breakout Rollup

##### Breakout A

Tess: We closed 2 issues related to manifests because the PR had already landed and addresses both issues. We defered talking about webidl partial. We talked about the issue around JSON-lD. I took an action to write a PR. I filed a follow-up issues. 2-3 issues tangled up here. One is that the JSON-LD specs use WEBIDL but don't expect to be used in browsers. 2nd one is that when JSON-LD is used in a spec it's unclear if browsers are supposed to manage it as JSON-LD or JSON. And the general principle might be "don't encourage polyglot". We talked about a naming conflict in webnfc. How to reconcile names when there is a naming conflict.  Rossen's PR says to match the web platform naming conventions. We also talked about a new principle - no data lost by default. Then we talked about security & privacy questionnaire issues. 

Rossen: ust to add - we did talk a little about data loss in breakout B. David has it as an action.  Also resolved some issues on promises guide.

##### Breakout B

Tess: first thing we looked at was no data loss - we also talked about the open PR on API vs feature naming. Plan is to revist after we land Alice's revisions. We talked about partial being a maintainability problem. Peter started some discusison on bikeshed changes.  We talked about how to balance interop vs implementability - Alice took an action to write a PR.  Sangwhan & I will do a breakout. We talked about the separation of concerns. Unclear how to adapt it to the modern world. No actions or next steps yet. 

Alice: Tess & I to schedule a breakout to brainstorm.

##### Breakout C

Dan: We didn't talk about miniapps because there will be a call on Monday.

Ken: Non-Privacy related notes on device APIs. Sangwhan to work on that.  We looked at toJSON.  Conclusion to punt to TC39.  

Dan: closed and commented on #116.

Ken: Async vs sync apis - when to use Sync.  Sangwhan wrote a PR.  We talked about APIs should be debugable.  COnsideration and precautions adding new media formats.

Yves: About adding consideration for new media formats.  You have to register media types - also there is a difference between data consumed at the network level vs the JavaScript level. 

Dan: Also Alice raised a bunch of PRs for changing & improving language.

Alice: There is one that goes into a full description (observer pattern vs events). The level of detail varies wildly. Naming section is long. I moved to an appendix.  We were talking a while back about how we want people to read the doc - that plays into how we write it.  I'm hoping people can read the whole thing.  

Dan: We should maybe try to make it more friendly.

Rossen: the doc has a few different things going on. it acts as design guideline and a pure API guideline doc. As a result the doc is quite lengthy.  We might make it easier to consume if there was a design guideline and an API guidelines / principles.

David: I feel it's OK if people skim sections they're not interested in.  They might be working on something very javascripty and not care about the sections on CSS, or vice versa...

Alice: yes, and I feel people should be able to skim the whole thing.  In the styleguide it says to make the main point after the heading.

Peter: I wonder if it makese sense to break the doc up - one doc that has a single bullet point for each item and one that has the details.

Rossen: like the cheat sheet.

Dan: i'd rather not split it into API and other.. (javascript and everything else...)

Alice: I will make a PR with all the changes - right not it's a list of short snappy recommendations and mini articles.

Peter: take the mini articles and put them in a separate page?

David: counter-argument. It's sometimes useful for people to see how much material there is on each topic.  If you take all the bigthigns and move them into separate docs it could give the reverse impression.

Alice: My plan is that we review each PR as it is.  I will make a not-for-review PR so you can see the whole thing.

Peter: actions for today?

Alice: Style guide.



#### Issue Triage

Triaging new issues 530, 531, 532, 533


