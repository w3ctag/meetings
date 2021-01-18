### Call Agenda

[Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/01-11-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20210111T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov
* [Review Request - Decentralized Identifiers (DIDs) v1.0](https://github.com/w3ctag/design-reviews/issues/556) - @hadleybeeman, @atanassov
* [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman
* [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564) - @hober, @ylafon
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss
* [WebXR Lighting Estimation](https://github.com/w3ctag/design-reviews/issues/574) - @torgo, @atanassov
* [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov

### Breakout B (US / APAC) - [2021-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20210111T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman
* [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @dbaron, @plinss
* [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris
* [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @alice
* [Requesting a TAG review of CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @alice
* [ARIA 1.2](https://github.com/w3ctag/design-reviews/issues/586) - @alice, @atanassov
* [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @atanassov

### Breakout C (APAC / Europe) - [2021-01-12](https://www.timeanddate.com/worldclock/converter.html?iso=20210112T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @torgo, @kenchris
* [Review of NativeIO](https://github.com/w3ctag/design-reviews/issues/566) - @cynthia, @kenchris
* [Byte Streams ](https://github.com/w3ctag/design-reviews/issues/567) - @cynthia, @ylafon
* [WebXR Hand Input API Specification](https://github.com/w3ctag/design-reviews/issues/568) - @alice, @torgo, @hadleybeeman

### Plenary Session - [2021-01-13](https://www.timeanddate.com/worldclock/converter.html?iso=20210113T060000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage


## Minutes:

### Breakout A (Europe / US) - [2021-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20210111T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)


Present: Kenneth, Dan, Lea, Amy, Tess, Peter, Rossen, David, Yves, Hadley

Regrets: Sangwhan




#### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov

Rossen: ability to create layers - which allows for optimisations etc.. in applications such as gaming, whatever... tons of details here. Huge spec. Extension to XR. APIs being added for construction, lifestyle, etc... It's a great addition to the platform but devil in the details. One question was whether they can break into pieces. They prefer not to. We asked if it's an eraly review - from our PoV early - may already be shipping in some places - where we are today is we asked for privacy & security review.  We felt the overall direction is good and we are ready to close.  We were going to spend more time on security & privacy.

... they have [a doc](https://github.com/immersive-web/layers/blob/master/security-considerations.md) ... They are falling back on "this is an extension of webxr".. so not so much added. Not 100% agree on security because they are adding new object lifetime management - if t's tied to the GPU then I can speculate that the security part is more complex. 

Dan: Yeah in their response they didn't go into too much detail.

Rossen: i did post a question about malicious actors - mostly around the privacy side. which was a long way to say - can I obtain visuals from the hosting document and capture what you're seeing?  They said "this is not possible".  I have confidence in the response.  

Dan: it should be in the security & privacy considerations section.

Rossen: I will ask for a bit more detail on lifecycle management of objects and primitives in the compositor. And we can propose closing after that.  We're happy with what they're doing. 

Ken: they should spell out the mitigations.

#### [Review Request - Decentralized Identifiers (DIDs) v1.0](https://github.com/w3ctag/design-reviews/issues/556) - @hadleybeeman, @atanassov

Hadley: we're still missing - the explainer not phrased in the context of user needs.  Lukash brought up security issues - they have now filled out the s&p questionnaire. They've done a good job - thoughtful response.  Also highlights how the s&p questionnaire is browser centric. They have left feedback on what we "should have asked." Amy what do you think?

Amy: There are a lot of people in the group who care deeply about security & privacy. They are hoping to get to CR by end of the month. Ths spec has had a bunch more editorial restructuring. A couple of concentious issues about privacy in the group. That said it is just a data model. The issues people raise are at other levels in the spec.  Thet group is trying to cover as many bases as possible.

Hadley: Having the data model in front us ...  Any other issues from a TAG PoV.

Amy: I can take the feedback on the explainer back to the group.

Rossen: I'd like to complete the proces...

Lea: I'm worried the action separated by a colon.  There is alot of JS code that assumes - incorrectly - that it parses a URL that way. Wondering if that would break existing code.  Using another character instead of a colon would solve the drawbacks.

Hadley: sounds reasonable. 

Rossen: a break-out of the breakout. For one more end-to-end. 

#### [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman

[some discussion on should we close]

[bumped to B]

#### [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564) - @hober, @ylafon

[mike west response to Lea](https://github.com/w3ctag/design-reviews/issues/564#issuecomment-757440835)

Tess: it sounds like a 3x above the "removeal" threshold.  If we could do this it would be great but we're skeptical for compat reasons. The numnbers are promising since its usage is declining. I think Mike has done a really good job of designing the process ... This sounds like a pretty sensible way to about it.

Dan: so what can we do with this issue?

Hadley: we should write up some kind of response "this seems risky but the approach seems good considering the risk" and propose close.

Yves: `document.domain` as Anne said is a way to do more isolation... isolation is done doing multiple other tweaks... there is still an issue of figuring out all the ways to do isolation here and explain them to developers so they can figure it out. While I agree it would be good, we need to get better understanding of isolation...

Dan: that could be a part of our feedback - that there should be a clea docuemntation of how to do isolation - e.g. on MDN - for developers.



#### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

#### [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss

#### [WebXR Lighting Estimation](https://github.com/w3ctag/design-reviews/issues/574) - @torgo, @atanassov

#### [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov




### Breakout B (US / APAC) - [2021-01-11](https://www.timeanddate.com/worldclock/converter.html?iso=20210111T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Alice, Peter, Lea, Tess, Rossen

Regrets: Sangwhan, David


#### [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman

[can we close?]

#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @dbaron, @plinss

Tess: Want an in-page picker where each font is a live preview of itself.

... I understand the desire for that, once you get all of them (?) it's a can of worms that a picker would avoid

Lea: Seems like very limited use cases beyond an in-page picker.

Tess: Can accomplish most of those use cases in other ways. Would prefer a font picker to this API.

Rossen: There's a reason we have the file picker as a file picker... 

Tess: `<input type=file>` is probably one of the best features in terms of how it implicitly grants permissions without showing a permission prompt: you grant permission to the single file when you pick it from the picker.


... Users don't think about fonts the same way they think about files. A lot of systems have native font picker dialogs, which you could imagine this would invoke.

Lea: That would also be a lot more [developer friendly] than a font API.

Tess: Geared towards complex, enterprise tools rather than middle-of-the-road web developers. Most developers aren't working on Google Docs, they're working on a rich text editor in something like WordPress. Bit of a smell when an API is really only for big tools, and overkill for little ones. If you're really dedicated to having that custom, in-page picker, input type=font wouldn't do the job for you, but you could still do it. Full Font Enumeration API is overkill.

Lea: Once pickers are more extensible and stleable they could cover more of those use cases as well.

Rossen: This goes back to the design principle we were talking about last week about high vs. low levels: enumerate your use cases, potential levels, ship the highest level API you can to begin with. 

Tess: Also least power principle: font picker has less power than a font enumeration API.

... what's the status of the review?

... filed a bunch of issues previously, at least one was "why not use a picker"

Peter: Explainer lists goals, but the goals don't really shed any light on user needs.

Tess: They combined two proposals, more or less because we told them to.

Peter: One use case I can think of where you'd want low-level access... grouping similar types of fonts so users can pick types of fonts (with similar metrics, e.g)... font picker wouldn't provide that functionality, but not clear to me that S&P risks are worth it.

Lea: Any kind of font tool also... but very niche use cases.

Tess: This is being pursued precisely for the Google Docs kind of use case, where they would see it as more of a showstopper that we can't get the extra 10%, IIRC.

Rossen: Is it fair to suggest re-opening the conversation about the [font] picker, and have an additional conversation as warranted... what are we *missing* if we have the font picker only? Then becomes a conversation about how to extend the font picker to get the use cases they need.

Peter: We did leave a comment in this issue https://github.com/w3ctag/design-reviews/issues/399#issuecomment-561387155 in December 2019 saying a picker style API would be better... don't see a reply to that. 

... can we ask again for their reasoning on that, as well as what are the *user* use cases, as opposed to the goals listed in the explainer? 

... got a summary of changes, but not how they addressed the feedback.

Tess: https://github.com/WICG/local-font-access/issues/62 was opened by someone else very recently which is very relevant to our feedback.

... also one from Anne https://github.com/WICG/local-font-access/issues/36 which is also very similar. From July... "the website invokes query() and the user then gets a browser-driven dialog with which they can select zero or more fonts to expose to the website." Also still open, there has been some discussion on that.

Tess: I can try and write something up... along the lines of enumerating the points of feedback and issues that are yet to be addressed, particularly around the API being more powerful than needed for the 90% use case, and whether it could start from a picker model and be extended from there to address any gaps in functionality.

#### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

Tess: Quick summary: Ken and I looked at it, liked the general idea, wanted some kind of summary IDL to understand what the API is.

... they provided that, Ken and I haven't managed to do a second review on it since then.

... We talked about doing a 1:1 breakout to do that, but we haven't yet scheduled that. Other folks are also assigned to this... but doing a breakout between Tess, Ken and Sangwhan is near-impossible timezone-wise.

Peter: Should we push this to the f2f?

Alice: still overconstrained.

Peter: I would simply have multiple breakouts... 

#### [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @alice

Rossen: I'm deeply involved in this spec... need to recuse from reviewing but I can provide context.

... looking at the call here and basically everyone on the call is close to this issue one way or another.

Alice: ...

Rossen: color-scheme... light or dark currently, few different ways authored content can fall into a color scheme. Might come directly from OS setting, has a global application of color scheme, forced or opt-in comes down to OS implementation. 

... Windows supports both forced color scheme from a11y settings, colour reduced down to a few system colours, improving readability and cognitive load.

... other one is preferred scheme such as dark and light, which are deliberately undefined; dark may be dark blue, dark brown ...

... looked at color scheme property, convinced ourselves that dark and light are the only color schemes we really need to support to accommodate modern OSes and browsers.

Alice: already a MQ for dark mode, right?

Rossen: that will evaluate whenever color-scheme is dark.

Alice: What does the property add on top of the MQ?

Rossen: Can be in dark mode, but then force colours that are light... force-colors MQ will be true, color-scheme light... dark mode will go away.

Lea: Are the use cases more like I don't want dark mode on this part of the document, or more like I do want light mode... more opt in or opt out?

... Examples in the spec say you should list out all the idents... not future-proof. If a new color scheme is listed, it's assumed I want to opt out of it.

Alice: Examples in spec also use the exact same code snippet for two different scenarios, and it's not clear what is consuming the property.

... color-adjust...

Lea: There is an open issue (#2) about whether these properties should be merged... color-adjust basically mainly applies to printing... seems like an overly generic name for a specific thing. What about making it a shorthand, of perhaps `color-adjust-forced` and `color-adjust-economy`?

Peter: May want these things to cascade differently... `forced-color-adjust` more likely to apply to specific elements.

Rossen: color-adjust is a legacy property for printers, has existed for many years. Ideally wouldn't be generic at this point. `forced-color-adjust` is quite a different use case, applies to an element and its subtree.

... since `color-adjust` was already there, we decided to reuse and combine it (with `forced-color-adjust`.

Peter: historically browsers would not print backgrounds; color-adjust allows you to opt in to printing backgrounds (for example).

Rossen: drifted away from color-scheme topic.

Alice: I'm going to leave a comment on that one.

Lea: does forced-color-adjust and color-adjust have the same basic use case (albeit in different context)? Could they be something like color-preserve?

Rossen: Opt in vs. opt out behaviour... opt-out is forced-color-adjust, you can opt out of the forcing 

Alice: you revert to the non-forced colors...

Lea: it's an opt-out in both cases?

Rossen: color-adjust is an opt in (`exact` value)

Peter: use color-adjust when you have a background on something that really needs to be printed. e.g. you're printing a list of driving directions and need zebra striping.

... forced-color-adjust, the browser is flipping the color of the scrollbars

Lea: significant intersection in the use cases, e.g. color swatches you would want to both display and print them.

Alice: seems like color-adjust and forced-color-adjust have the same effects?

Peter: economy mode is going to suppress backgrounds. forced-color-adjust affects default colors.

... If we were going to combine, UA stylesheet would need to specify the default behaviour in each context.

#### [Requesting a TAG review of CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @alice

#### [ARIA 1.2](https://github.com/w3ctag/design-reviews/issues/586) - @alice, @atanassov

#### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @atanassov


### Breakout C (APAC / Europe) - [2021-01-12](https://www.timeanddate.com/worldclock/converter.html?iso=20210112T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Amy, Dan, Ken, Yves, Sangwhan, Alice

Regrets: Hadley

#### [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @torgo, @kenchris

Ken: Only big difference is they adopted my API suggestions and added an idle detection permission.

Sangwhan: We discussed this earlier...

Dan: So they respoded to all your feedback...

Ken: Yes, looks like they took it all on and made all the changes we asked for.

Dan: Last comment from Reilly was in response to my question about venue/destination. Intended venue beyond WICG. "We don't have a particular destination in mind" as of Nov. 10.

... Could leave a closing comment saying we're happy you've addressed our feedback, and suggest a venue...

Ken: Seems like WebApps.

Sangwhan: I can leave that feedback.

Dan: Propose close, we can officially close it in plenary.

#### [Review of NativeIO](https://github.com/w3ctag/design-reviews/issues/566) - @cynthia, @kenchris

Dan: Previously left a bunch of feedback saying given the characteristics of what ??? a file, how can I share this file with my web application... how can these files be accessed from the OS, how does it relate to storage buckets, should there be ephemeral mode... and what's the venue

... They [responded](https://github.com/w3ctag/design-reviews/issues/566#issuecomment-736883333) saying it should be in WebApps...

Sangwhan: did we ever ask about fsync? Flush to disk. I don't remember seeing that, seeing any guarantees.

Ken: This is a performance thing ...

Sangwhan: There are times when you would definitely want to flush.

... say you put a flush on close...  (missed)

Ken: Talking about having a delete on close, could have a flush on close.

Sangwhan: If execution context is destroyed... want something like Beacon?

Ken: There is a flush function actually, looking at the API..

Sangwhan: Doesn't come with guarantees

Ken: (quoting from explaiener)

Sangwhan: Reliable as long as flush finishes before execution context is destroyed.

Ken: It's a good question.

Sangwhan: A lot of things don't guarantee anything once you lose the execution context. All bets are off.

Dan: Same problem we've encountered elsewhere, API being introduced into the platform, a capability that is overlapping with similar capabilities with some significant differences, being introduced as a completely different technology that creates bloat.

Ken: I left feedback to that effect... for a start the name is important, they have decided to change the name to highlight the main use cases.

Dan: It's still using its own concept of a filesystem. 

Ken: ... bloat in the implementation ... stay secure... this is for e.g. BYO database, like doing MySQL from WebAssembly. They def know about the filesystem access API, but you can't base one on the other for performance reasons...

Dan: That's an implementation detail; from a dev perspective feels like it should be the same thing, I want to open a file, how do I know which one to use? UAs should be abstracting that implementation difference away, making the dev experience more straightforward

Sangwhan: We have the abstractions, but not the unabstracted version, which this provides. This is the lower level.

Dan: So you think they've adequately addressed our questions?

Ken: Haven't finished designing yet so hard to say, but they're aware of the feedback..

Sangwhan: Not seeing solutions yet to the problems we raised

Ken: But they're still working on it.

Dan: If we've left the feedback we want to leave and they've taken it on, we should probably close with some directions... consider the dev experience of filesystem-like APIs overall when coming up with their final design

Ken: Try to keep the APIs as similar as possible... happy with (?), happy with the name - doesn't sound like how I access a file... 

... not access to local files, more like a cache kind of thing...

... you don't have those files, you can't access them from the OS in general.

Sangwhan: This is not for "common" developers, this is for not having to reimplement the whole storage part when you're porting an app to webassembly.

Ken: Or ... people could use the FS access API and emulate this, but then an external application could modify those files and potentially even trigger browser bugs taht way. 

Dan: Still feels like why isn't this an optional feature... or an option on FS access API?

Ken: It's not a filesystem

Sangwhan: If you get a handle from the FS API you might be able to ??? these APIs, but it's nto directly related.

Ken: It's like a virtual filesystem.

Sangwhan: This is like libc level.

Dan: Think we should close this and leave the feedback we've left. Propose close, close in plenary. Should be encouraging them to consider the complexity they're adding, thinking about ways to simplify.

Sangwhan: Would like folks to consider the use cases and concerns that we've noted above.

... Oh, and a flush guarantee.

Ken: I think I'm ok with the name. It doesn't say filesystem.

Dan: We've talked about how this is origin-bound and that's the web security model, but also asked about access across origins... kind of conflicting feedback. Intention was just to ask if there's a use case for cross-origin access. If there were that access, it would be problematic... unless we're talking about a first party sets scenario. 

Ken: I assume it would have to be... don't want to transfer my database to another site

Sangwhan: You've got CAD, or Eagle... generating PCBs... want to be able to transfer that data from one app to another. Audio editor to video editor.

Ken: Write it to a file?

Sangwhan: It's possible by binding the FS access API... if a FS access API has these handles you can flush a file to disk, then load it up from the other app.

Ken: This is a pretty big use case... a lot of native apps today are looking at doing this kind of thing.

Sangwhan: It's not an imaginary use case. If these files are trapped in virtual FS land, it's inaccessible to the user. You can make SQL Lite easier to use, but that's just one use case...

Ken: Would you use this API for this instead of the FS Access API? When would I use this API instead.

Dan: [leaves comment on developer complexity](https://github.com/w3ctag/design-reviews/issues/566#issuecomment-758494304)

Sangwhan: Legacy CAD format that's implemented in C, for example... don't want to port it all over to JS... 


Ken: If we can write to a non-virtual file, that would solve this concern...

Sangwhan: If there were a connection, yes. That connection is currently missing.

... Will try and leave a comment around this.

Ken: Writing it to a different file mitigates Dan's concern

Sangwhan: Yes

Ken: It's like saving a file.. ... delegating access to storage from one origin to another origin... that's a can of worms.


#### [Byte Streams ](https://github.com/w3ctag/design-reviews/issues/567) - @cynthia, @ylafon

Dan: Maybe the lowest-level API we've tackled. 

.. December 8, Hadley asked the requester ... user benefits/user needs.

... responded, "increase speed and lower memory usage for sites that take advantage of it. Specifically, sites that handle streaming binary data will see improved performance."

Ken: How would developers figure that out?

Sangwhan: People who need this will use this.

Yves: It says it's there to avoid multiple copies in memory for the same buffer.

... Another example of very low-level optimisation in a higher level API, not that great. Would rather have other ways of achieving that optimsation like ??? in Linux, a view of data that is streamed in memory space, don't need a copy but can take a pointer at a given location. Not sure something analogous is possible in JS

... A bit ugly, but could be useful for something like a node application for example.

Ken: what is the alternative today?

Yves: Copy.

Ken: This is just about trying to avoid having several copies... 

Yves: Reducing copies. Copying between buffer and stream.

Sangwhan: Can byo buffer, don't need to worry about GC

Yves: Also controlling size of buffer.

Ken: I had assumed the BYO buffer thing already existed...

Dan: Two WHATWG bugs on streams that they point to in service of answering question about multi-stakeholder review. e.g. bytestream bug 300... where does this indicate multi-stakeholder review? Lot of stuff around Chromium.... developed by Google engineers, being pushed into WHATWG, we're being asked to review because of blink process. Trying to figure out what the multi-stakeholder story.

Sangwhan: Doesn't look like Anne has looked at it, which is worrying.

Dan: I don't see anything in either of these bugs that talk about multi-stakeholder review.

Ken: Jake Archibald should have a look at this. Should we @-mention Anne and Jake?

... I can do that.

Dan: I'll leave a comment asking about multi-stakeholder feedback.

Yves: Other than the low-level optimisation in a high-level API, it looks ok. I can add that comment.

Ken: I wonder what the actual use case that triggers people to work on this feature.



#### [WebXR Hand Input API Specification](https://github.com/w3ctag/design-reviews/issues/568) - @alice, @torgo, @hadleybeeman

Alice: I think we are actually done with this one. I should respond to the last comment that says I have been spending effort imaginging a more inclusive system. it's very hardcoded that everyone hasa got two hands and five fingers.. well any number of hands. Any given hand has 5 fingers, any given finger has the expected joints. Which obviously doesn't bear up to reality. We talked about this is the baseline API until someone ships an API that takes that into account, but they've got to do the classic thing, it's hardware, so the superset of what all the underlying things do. I was posing the question of whose responsibility is it to come up with the more inclusive version, so the answers are quite good, they have ideas, have been working with some of the WGs including device manufacturers, but they don't hae time yet. That seems pretty good. The one outstanding issue that another commenter raised right up in the second comment about privacy, the fact that it returns real metrics about peoples finger lengths etc and this is the one where the explainer starts talking about hand phrenology. It's really wild. It might be worth reiterating that point. They ask for elaboration on anonymity - we don't have a clear idea of this.

Dan: it says implementations are required to employ strategies to mitigate, reduce precision of sampling data, adding noise

Alice: I guess that's fine. I suggested could it be a richer data structure and a bunch of enums and they said no not right now. They did change it to enums instead of constants but other than that. It looks pretty good. I'm happy to comment and propose closing.

Dan: I think we should do that, we've gone around and around and they've been responsive to our feedback. I support that.


#### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

Ken: I read the feedback, it's really good. Some of the comments about names, it's consistent with existing things so I think that's okay. Consistency is very important even though the names might not be perfect.

Dan: propose close?

Ken: yeah this is early review. We like the feature, they are listening to our feedback, we have given some comments and we look forward to a late review.

Dan: did they say what the venue is?

Sangwhan: feels like webapps

Ken: they haven't said. Probably same as cookie store API. I'll write that the feedback sounds sensible.

Sangwhan: use cases and goals I'm happy with, detailed API I'm not up to date

Dan: and multi stakeholder, I don't see

Ken: done

Sangwhan: the multi stakeholder thing is at the bottom of the explainer

Ken: it's definitely there, I'll remove that

Dan: there are some words here.. when they say Gecko positive, what does that mean? I would like to see a link to the Mozilla standards position. Web developers - positive? I'd like to see more.. be good to see some evidence. Some blog posts?

Ken: I'm a web developer and I like it

Sangwhan: it takes away the problem of namespacing so you can scope storage from the developer to the browser, so that's useful

Dan: I'm in no way making the arguement that it's not useful. I'd just like to see more evidence when they make these assertions.

Ken: maybe we should change our issue template to point out please send the standards position

Dan: I might add an additional comment asking for more detail on the developer feedback.


### Plenary Session - [2021-01-13](https://www.timeanddate.com/worldclock/converter.html?iso=20210113T060000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Tess, Lea, Peter, Alice, Sangwhan

Regrets: Hadley, Amy

#### Breakout Rollup

Lack of quorum

#### Issue Triage

Assigned all unassigned design review issues, closed a few "propose closing" issues.

