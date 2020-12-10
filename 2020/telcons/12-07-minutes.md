## TAG Teleconference
##### 07-09 December 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-12-07](https://www.timeanddate.com/worldclock/converter.html?iso=20201207T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov
* [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman
* [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564) - @hober, @ylafon
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss
* [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

#### Breakout B (US / APAC) - [2020-12-07](https://www.timeanddate.com/worldclock/converter.html?iso=20201207T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Review of CSS Sizing 3](https://github.com/w3ctag/design-reviews/issues/565) - @cynthia
* [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @torgo, @kenchris
* [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311) - @cynthia, @dbaron, @plinss
* [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia
* [WebRTC Priority Control API](https://github.com/w3ctag/design-reviews/issues/560) - @cynthia, @dbaron

#### Breakout C (APAC / Europe) - [2020-12-08](https://www.timeanddate.com/worldclock/converter.html?iso=20201208T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris
* [Byte Streams ](https://github.com/w3ctag/design-reviews/issues/567) - @cynthia, @ylafon
* [WebXR Hand Input API Specification](https://github.com/w3ctag/design-reviews/issues/568) - @alice, @torgo, @hadleybeeman

### Plenary Session - [2020-12-09](https://www.timeanddate.com/worldclock/converter.html?iso=20201209T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage


-----


### Breakout A

Present: Dan, Peter, Hadley, Rossen, Tess, Yves, Kenneth, Alice

Regrets: 


#### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov

Rossen: My take-away is that everything we asked for has been thought of... They are building closely on top of WebXR... There is essentially nothing new that's been added that's been concerning from API exposure. on scale factor - .. he got back to us ... he's saying it's the value of scale factor in consutruction...  not what we were thinking.  

... a few questions around security & Privacy - he did fill out the questionnaire... 

... we asked him to possibly split it.  He cited a heavy dependency on webXR to push back.  I agree for the spec, I'm not sure about the explainer... 

... they may want to break it down to new capabilities... 

... the spec itself is split into 6 different logical submodules... lifetime, initialization, type system, event model, rendering model...  

... it's marked as "early" but maybe not so early...

Dan: what are you suggesting?

Rossen: the explainer does a good job of reflecting concepts from the spec, but doesn't answer some key questions - goals and non-goals, other potential solutions considered, ... which parts of the examples are newly added capabilities vs new functionality... 

... meta-question is do we "hold them back" ?

[taking a look at explainer, s&p questionnaire, etc...]

[left comment](https://github.com/w3ctag/design-reviews/issues/528#issuecomment-740063337)

#### [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman

Tess: we talked this a couple weeks ago - we had a joint meeting during TPAC. Productive. We gave advice. We didn't reflect the discussion in the issue. I found the minutes and linked them in the comments. We propose close.

Rossen: let's close in plnary to give Alice a chance to be in on this one.

[agreed]

#### [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564) - @hober, @ylafon



#### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

Tess: we talked about this a week or 2 ago... We went back to them with some questions about using the payment request API... Basically they think we should have known the answer... 

Hadley: my question still stands as to whether this gives you a blank check -... will look at it before we discuss again.

Tess: first non-design principles week of the new year...

#### [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss

#### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

Tess: we wanted them to provide us a summary of the API - and they have done so - in IDL.  We could look at it now.  

Ken: [on API](https://github.com/WICG/storage-buckets/blob/gh-pages/API.md) I'm not a big fan of  APIs with Open or Create... I don't understand - all storage buckets have a name and also a title - metadata you can set. You can go into settings and see a descriptive name. You run into issues of a11y, i18n.. 

Tess: we've been reluctant to expose author-provided strings in security UI like that...

Ken: I think it should just be called open.  Also - i don't know about the expiration thing - takes a DOM timestamp. Will this work with summer time, etc... 

Tess: DOM timestamps are always UTC.

Ken: ok. 

Tess: the rest of it is "what hangs off of a storage bucket"

Ken: ...name of `persist`...

Tess: our naming advice would suggest a simpler name - like "save". Depends on what `persist` does.

... durability concept - durability relax - is the UA free to delete things things? But even in strict if the UA is under storage pressure it's gonna get rid of your stuff. So - don't like APIs that imply to the author that this is durable.

Ken: maybe "something i care about" / "something I don't care about"

Tess: The service worker integration is complex but it needs to be... 

Ken: file API thing... 

Tess: these APIs are straight from the file api... so consistency.

Ken: set expires -- doesn't it make sense to set expiration date?  set expires sounds like a boolean.

Tess: to summarize: we have some naming concerns and other similar concerns... but overall it seems fine.

Dan: why is this better for user privacy?

Tess: the explainer covers this reasonably well.. Currently browsers have an all-or-nothing choice about storage.  This API would allow browsers to be a little more intelligent.  For example, an email client could put mailboxes in 1 bucket - and say that the durability is relaxed - and a 2nd bucket for draft messages you haven't sent yet - and put that under "strict" durability.  So UA can delete the "relaxed" stuff first.  This doesn't change partitioning of storage - it just makes it more convenient about how to selectively purge storage.  Theoretically the privacy story is "no change" - there could be some fingerprintability - you could create different buckets but it's really hard to do...

Dan: expiration date could allow the developer to set expration on data that isn't needed anymore - aids in data minimization. Good for sustainability.

Tess: Yes.

... you could imaging user agents to want a default expiration. That would be a huge win compared to existing APIs.

... controling the expiration of the default bucket...

Ken: you can't get access...

Tess: in the S&P they talk about exposing the default bucket... could be good because it encourages sites to set a 

[discussed possibly closing in the plenary call this week - otherwise 2nd week of jan]

### Breakout B

Present: Rossen, Peter, Alice, Elika

Regrets:

#### Late CSS reviews

Rossen: Summarized planery discussion about late CSS transition reviews.

Elika: All CSS specs can benefit from having someone who is not the editor (not necessary from TAG) read it from top to bottom. Having TAG read through the specs can also be very beneficial. 
Summarizing the top level of work that is happening into a spec is going to be also beneficial. I am also perfectly happy to come and present/defend the theses here but writing an explaniner will take a huge amount of work to little benefit. 

... CSS sizing probably doesn't have a lot for TAG to look at, doesn't require TAG specifically, but we have to get horizontal review.

Alice: until we read all of the spec, we don't know if we need to review.

Elika: Would need to figure out how to ask about important topics, or read all our specs.

... Don't necessarily need in-depth review, but need sign-off and any feedback you can give.

... Can answer questions, provide information when asked.

... Sizing might be one that doesn't need full TAG review; doesn't really affect web architecture.

.... 2 different kinds of specs - module, describes a system; others which are a collection of small features.

... Text module is more of a "pile of different features"; we added 3 features, most of the text is how they interact with other CSS specs. This is the foundation of all the other layout specs; they depend on definitions in the [Sizing module](https://www.w3.org/TR/css-sizing-3/).

... For design review template, could point to what sections to look at and what to skip.

#### [Review of CSS Sizing 3](https://github.com/w3ctag/design-reviews/issues/565) - @cynthia

Elika:

... CSS3 text is like a collection of separate side dishes...

... From the CSS system point of view, terminology section is most interesting. Features listed in the review are the most interesting

.. Terminology gives names to a bunch of concepts which have always existed in CSS.

... the features mentioned in the comment are what's changing in this version.

... They are shipping in several implementations (some with prefixes), definitions of what they mean is pretty clear to CSSWG, just giving names to behaviour you could access in CSS2; previously height access didn't have any varying behaviour. TAG would be unlikely to be interested in that. Probably only interested in interaction between replaced elements and these things.

... replaced elements are external to the document, transferring info to doc about themselves (e.g. sizing info); that's the interface between CSS and other tech. Most of the spec doesn't need TAG review, but TAG is in the loop on everything.

... Some questions that might go into a CSS-specific review template:

* Why did you write this spec (what prompted the features in it)?
* If you were the TAG, which sections would you focus on?

Peter: Explanations like this one are helpful not only for TAG, but also for other horizontal reviews and newcomers to CSSWG. 

Elika: [Snapshot](https://www.w3.org/TR/CSS/) gives an overview. ...

Peter: Web developer is better served by the snapshot. Someone joining CSSWG needs more context ...

Elika: If people want to get involved, they can start filing issues... then we can provide context on the issue. Pre-emptively generating that context isn't scalable.

Peter: Could we on CSSWG have some process going forward to make this process easier, without Elika needing to personally write explainers for every single feature?

Elika: Issues also linked to commit logs... you do have to go dig, though. Alternative is to have us write continuous status reports... and we already give more context on commits than most WGs. 


#### [Formal Review Request for CSS Text Level 3](https://github.com/w3ctag/design-reviews/issues/581)

Elika: Internationalisation and accessibility implications.

... text transformation may have accessibility implications. Accessibility group signed off. Transformed text to AT or not?

... Justification may make things hard to read; CSS3 adds a new value to turn it off, without affecting ability to align text left and right.

... [how we handle whitespace and control characters](https://drafts.csswg.org/css-text-3/#white-space-processing) may be of interest here, as well as [privacy and security](https://drafts.csswg.org/css-text-3/#priv-sec)

... whitespace processing and control codes probably most relevant for TAG in terms of interactions 

Peter: none of the properties and values make sense, for historical reasons :( 

Elika: It's taken a lot of effort to make it makes sense. Florian's video, linked from the issue, goes into it.

... TAG's review is the last step before CR transition.

#### [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583)

Elika: This one might warrant a full TAG review. It was also drafted more recently, and only has 3 major features, so much easier to pull out the relevant points.

... grid would be a much taller order to explain, for example.

#### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @torgo, @kenchris

#### [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311) - @cynthia, @dbaron, @plinss

#### [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia

#### [WebRTC Priority Control API](https://github.com/w3ctag/design-reviews/issues/560) - @cynthia, @dbaron


### Breakout C

Present: Alice, Sangwhan, Ken, Yves, Dan, Hadley

Regrets:

#### Reading out Breakout B a bit

Alice: very positive discussion - leading to progress on CSS color adjust and CSS sizing 3. 

... some CSS topics are long-standing historical work - different buckets of CSS work - some require more TAG review than others...  Accomodating their workmode...

Yves: Also - we have people in the TAG involved in CSS - they can help to inform our reviews.

[discussion about whatwg - can we do somehting better with them to encourage reviews to come from whatwg when appropriate?]

#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris

Dan: looking for specific feedback on 4 points listed in issue.. let's see if we can get them feedback on those points.

... Not shipped negotiation mechanism... naming issue. Ossifying.

[reviewing last comment](https://github.com/w3ctag/design-reviews/issues/408#issuecomment-728994329)

Dan: regarding the use of the term "policy" - I agree it's confusing. 

Hadley: also not very descriptive... if you came across this on its own it's not clear what it does...

Sangwhan: might suggest "features" - but that's also confusing...

Dan: the first 2 examples are about performance.  Others are about security.

Sangwhan: feature policy got split up between document policy and permission policy... 

Dan: it's very complex...  How do you explain this to a regular web developer.

Sangwhan: don't see average web developers using this -  There will be "silver bullet" policies.  This is opt in as well..

Dan: maybe we don't have any useful feedback on the naming other than that the current name is not so developer-friendly (self-descriptive).

[on the API]

Sangwhan: we have a permissions API...  It should be unified...

Alice: on naming: the name fits together with the use of document policy header.

Sangwhan: on the 4th point (enum) I would lean towards waiting until we see an actual consumer.

Dan: let's try to close this in plenary after leaving this feedback.

#### [Byte Streams ](https://github.com/w3ctag/design-reviews/issues/567) - @cynthia, @ylafon

Yves: still trying to figure out how it differs from regular streams. For example "bring your own buffer" is already in the streams spec.

Dan: there has been an update to the explainer after Rossen's feedback.

Hadley: kind of missing user needs...  End user...

Dan: Agree - we should ask them to be clear about what the user benefit is...

[hadley leaves comment]

#### [WebXR Hand Input API Specification](https://github.com/w3ctag/design-reviews/issues/568) - @alice, @torgo, @hadleybeeman

Sangwhan: it's very medical.

Alice: that is kind of the main point of feedback - asking people to memorize the bone names...

Hadley: but if we need a vocab, that's a good one to use...

Sangwhan: could use index numbers...

Alice: i suggested that... referencing the unity API... easier to understand...  The response made some sense. Different platforms expose different amounts of information - if you're using a numbered system you still want to be able to see which parts of the hand are included in that number system... It's a subset of possible bones. 

Sangwhan: if you extend it - you have this weird situation where you have 1,2,3,4,.... when you add something in it could become 25.  

Alice: the last commetn said it's changing the constants to enums... which avoids this problem.

Alice: nobody has come up with a plain english set of names for every bone in the hand... 

Hadley: there are lots of resources out thee [to help developers know these names]

Hadley: I can imagine a future need to name other bones in the body and we've already used this special thing for hands...

Alice: it's about detecting a gesture... based on image recognition...   If there were some other vocab to use we should use that but there isn't. 

... I gave some feedback to ask if they could consider a richer data structure...  

Dan: performance issue... something something uncanny valley

Sangwhan: isn't this API just exposing a network of vertices in a semantic OO form...

Alice: I would like to see the updated examples... They talked about it being iteratable..  Don't understand how that helps...

#### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @torgo, @kenchris

### Plenary Session

Present: Peter, Tess, Dan, Hadley, Yves, Rossen, Alice
 
Regrets: 


#### Breakout Rollup

##### WebXR layers

Dan: we had a response from Rick, editing as per our suggestions. 

Rossen: This is a reasonable addition on top of webxr. Ovverall functionality is a commodity in games and games engines, for performance and responsiveness. So they're bringing that capability to the web as well.

...API surface looks reasonable, and fits into the rest of webxr.

...Everything else is more detailed.

Dan: Are we happy with security and privacy angles? Not much in their questionnaire answers. This is such a big spec... Are we missing something?

...If there's nothing else for us to do, should we close? Or should we look at it in more detail? 

Tess: I'll take a look

Hadley: can they wait til the new year for us to get back to them?

Dan: we can give them an interim response now, and final comments in the new year.

[agreed]

##### APA pronunciation explainer

Hadley: we wanted to ask Alice if she's okay with closing this.

Dan: I'll put a note on slack

...I'll put it to the first design review meeting in the new year, but maybe we can close it earlier if Alice is happy. 

[alice joins]

[discussion of what feedback we gave]

Tess: we asked them to talk to stakeholders.  

Alice: yes I'm happy closing it.

##### Digital goods API

Hadley: we need to look at it more. Milestone set.

##### Storage buckets API

Dan: possibly to close now, or maybe in Jan. Been a lot of feedback on the API surface from Ken. It's an early review, so we might say "this looks good to us, can we rereview when this is more advanced."

...But we haven't heard back from Ken's latest comments. So... let's bump it to January.

##### CSS Reviews

Peter: Elika (@fantasai) joined us. She and Alice led discussion on how to get explainer info from CSS, without docunenting 20 years of history.

...We want to write a couple of new issue templates from this.

...Elika gave some pointers for the specific specs as well.

Rossen: I caught up with Elika afterwards, to see what we can do better for discussions with guests.

...She was comfortable, knows all of us. She definitekly sympathises with the challenges that we have. CR transitions and horizontal reviews — groups are doing hard work to make sure these specs are the best they can be, but some of the specs are huge, like CSS Text 3.

...She appreciates the challenges to that, but hopes we find the middleground where these horizontal reviews can go smoother 

##### CSS text level 3

Rossen: This has been going on for literally 20 years, since Elika joined the WG. So I was curious: what might we find, as the TAG, that would set this spec back. It's been through i18n and a11y. I didn't have a good answer to that. 

...So, the question to us: besides templates and speeding up the process — what can we do? How can we sign off this one before the end of 2020?

Dan: we discussed in breakout C some of this, and mentioned that we have people in TAG who are involved with CSS, and help to inform our views. We talked about whether we should have special cases... we do treat reviews differently depending on where they come from. it's necessary to manage our workload. I'm comfortable with the idea that we have a high-bandwidth communication with CSS, and our reviews are informed by what they say we need to look at.

Yves: and for a long-running spec like CSS text 3, I feel like it's okay to say "this spec has received enough review and you're free to go", without delving deeply into the details.

Rossen: I agree.

Tess: Considering the breadth of hte consortium, we have a disproproritate amoubnt of CSS expertise on the TAG. No guarantee that will always be the case. 

Hadley: I worry that this is a precedent - I worry about setting the expectation of what the TAG doesn't engage with - I think this should be on a spec by spec basis and continue to be our decision.

Rossen: I agree. Reminder: we started this by wanting to put non-CSS TAG members on this.

Yves: and I hope in the future that CSS will involve us at early stages, so we don't have 20-year-old specs to look at.

Dan: What is the action then, re CSS text level 3? How do we answer Elika's question: if we want to do this on a spec-by-spec basis, and not set the expectation (as Hadley was saying), what do we ask of these working groups for us? Elika didn't want to do a full explainer.

Tess: This is also a culture clash of groups. I think it woudl be great if the CSS working group wrote more explainers. We've encountered confusion, that explainers are for TAG review. It's not. It's for a much broader audience, including the CSS working group. There are parts of CSS I would love explainers for, that groups taking a first look at something would work for. I get that Elika edits a lot, but i'm not sure working groups see how steep the cliff is that you have to climb to join and become a productive member.

Alice: Elika said she's dealing with the new process and was not keen to do more work. We're keen to do this so we don't have to do loads of work too. We did mention that it's helpful for people trying to join CSS WG. And whether there is scope for others to write them, like implementors. She said people will ship based on an editors draft, so there isn't a forcing function here. Apart from going to CR, which no one else seems to care about.

Peter: different issues templates?  early review / mature spec (only for the diff) / the mature spec that has been languishing - it may not be reasonable to ask for an expaliner.  Most of those specs when they come to the TAG don't need a thorough TAG review.

Tess: i think it's percisely the specs that have been languishing that need to get new people involved - the explainer can just be an overview of "here is where this module is right now" maybe we need a new explainer template. Real problem: we shouldn't say 'that spec is too big to fail' so we shouldn't do the review work. Don't like the idea of saying to CSS "we're not going to bother reviewing things that are too big".

Peter: i don't think too big is the criteria - maybe some things that are big we can break apart into multiple reviews - but there are some specs that are done and implemented and used everywhere - but are stuck because people haven't written tests... No one right response.

Hadley: a process point - we shouldn't have specs that are that big.

[discussion...]

Rossen: on the here and now - what should we do with these specs?  Yves proposal - we fall back on the 20 years of work and say that this has had enough review. 

Peter: she did point out a couple of areas of text 3 that might need TAG review - white space, security & privacy, control codes, character handling... I think it's worth us takng a deeper look.

Dan: let's open up a specific issue on those topics.  In #581.  

Peter: we can update that issue to clarify that we're going to look at these few topics.

[new issue templates]

Alice:  3 different kinds of reviews... **(1)** long-standing specs - text falls into that bucket - even with that we have a few things to review. **(2)** delta reviews - an existing spec with new things - here is what the new things are and why they were added **(3)** here is a very self-contained module that has a clear set of user needs and features that address those user needs. 3rd is a regular kind of review. for color adjust module for example - we could we could reformat their comment as an explainer. Don't know what to do for 1st one.  We don't have the resources to read entire spec from top to bottom. 

Peter: I don't propose we block the CR transition - we can review even after it goes to CR - e.g. HTML.

Alice: our path is to read the table of context and file issues ourselves - and not let it block them.

Peter: I don't think we want to present this type of review in an issue template...  maybe it's a state we can knock the spec into...

Alice: but our regular issue template requires an explainer...  

#### Issue Triage

