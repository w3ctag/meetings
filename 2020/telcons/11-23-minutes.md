## TAG Teleconference
##### 23-25 November 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-11-23](https://www.timeanddate.com/worldclock/converter.html?iso=20201123T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @hober, @torgo, @plinss
* [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman
* [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564) - @hober, @ylafon
* [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

#### Breakout B (US / APAC) - [2020-11-23](https://www.timeanddate.com/worldclock/converter.html?iso=20201123T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov
* [Review of CSS Sizing 3](https://github.com/w3ctag/design-reviews/issues/565) - @cynthia

#### Breakout C (APAC / Europe) - [2020-11-24](https://www.timeanddate.com/worldclock/converter.html?iso=20201124T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @torgo, @kenchris
* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris
* [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @torgo, @kenchris
* [Review of NativeIO](https://github.com/w3ctag/design-reviews/issues/566) - @cynthia, @kenchris
* [Byte Streams ](https://github.com/w3ctag/design-reviews/issues/567) - @cynthia, @ylafon
* [WebXR Hand Input API Specification](https://github.com/w3ctag/design-reviews/issues/568) - @alice, @torgo, @hadleybeeman
* [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @hadleybeeman

#### Plenary Session - [2020-11-25](https://www.timeanddate.com/worldclock/converter.html?iso=20201125T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo with Guest Chris Wilson

* Breakout Rollup
* Issue Triage



-----


### Breakout A

Present: Peter, Dan, Rossen, Ken, Yves

Regrets: 

#### discussion on fast-track non-blocking review

Rossen: proposal by alex for light-weight reviews

[some discussion on this]

#### [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @hober, @torgo, @plinss

[some new comments]

Rossen: some folks have engaged from the HTML side.

Peter: good to get good feedback

Peter: we talked about maybe starting a community group or taking it to WICG

Rossen: I think what is being discussed here is great - in terms of how this might work. Ways to incorporate this back into form control management. Main point raised by Anne which still stands - we need the protocol underneath. I don't see anyone answering those question.

Peter: the proposal presumes trust tokens or something like it.

Rossen: Have you considered any other than trust token solutions? Any other identity solutions that might work?

Peter: something that a browser can send to  asite.. ideally doesn't provide additional PII. Trust tokens fit the bill. 

[discussion on who is in trust token work]

Dan: need for a workshop maybe?  Engage with Wendy Seltzer to see if there is w3c "strategy" interest? [emails wendy]

Peter: we should let it percolate for a while... 

#### [APA Pronunciation Explainer](https://github.com/w3ctag/design-reviews/issues/561) - @hober, @hadleybeeman

#### [Deprecating `document.domain`.](https://github.com/w3ctag/design-reviews/issues/564) - @hober, @ylafon

Yves: the idea makes sense - but aparently there is dissagreement of how to meet that goal.  There is a [WICG proposal](https://github.com/WICG/origin-isolation) ... need to check that.

... needs more time on our side.

[bumped]

#### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

[]

#### possibly we can close user idle detection?

Dan: Asked Sangwhan.

#### talked a bit about byte streams

Dan: do we need a better explainer?

Rossen: there should be "non goals" and explaining some of the decision points.

Ken: I was wondering if it's a light-weight review

Rossen: not sure.  There could be security / privacy issues... 

Dan: Maybe prompt them to give some better asnwers?

### Breakout B

Present:

Regrets:

#### [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov

#### [Review of CSS Sizing 3](https://github.com/w3ctag/design-reviews/issues/565) - @cynthia


### Breakout C

Present: Ken, Dan

Regrets: Sangwhan


#### [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @torgo, @kenchris



#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris

[reviewing last comment](https://github.com/w3ctag/design-reviews/issues/408#issuecomment-728994329)

[considering Ian's bullet points]

Ken: not sure I can think of a better name [than policy]....

Dan: I think we need to take these questions to plenary and maybe close the issue if appropriate.

Ken: worried about wide review from other browsers.  Seems to be a very core thing, an architectural thing.

#### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @torgo, @kenchris

Alice: appreciate that the explainer links out to use cases which link to bugs asking for this feature. Great example.

Ken: I appreciate the security & privacy section though 

Dan: on the self-review... they answered yes to point 11, but can it "affect securtity & privacy controls"? 

Alice: Is the scroll bar privacy & security critical in any way?  it doesn't allow anything you couldn't already do... you could already make a fake scroll bar

Ken: and remove the scroll bar...

Alice: I can't see a security or privacy implication. I can see an accessibility implication. Users could use a user style sheet.

Yves: it's using the system scrollbar. if you have a system that redefines the system scrollbar instead, it's better to use the system one as it can be linked to external tools.

Dan: prefers color scheme?

Alice: right now the browser doesn't do anything with prefers color scheme...

Ken: auto?

Ken: if the browser does dark mode for your website then it could do the same for your website.

[discussion of dark mode]

Alice: prefers color scheme is orthoginal

Ken: some compoents in material web compoents support dark mode... 

Alice: assuming they considered having seaprate properties for the thumb and the track...  Things that cascade together.  Can be auto, dark, light or 2 colors. 

Dan: Maybe one feedback point could be asking them to be clearer about the interaction betwee this and prefers-color-scheme ?

Alice: specifically the interaction between the light and dark properties and prefers-color-scheme...  Do we want a shortcut to say "match what the colorscheme wants"?

Dan: any a11y issues?

ALice: anytime you can override color you can do so to make it less accessible.  If you do a super-light-grey-on-white scrollbar that can't be easily seen - it would be nice to have users have a way to unmatch the styles.  More of a UA question but it might be nice to highlight that.



#### [Review of NativeIO](https://github.com/w3ctag/design-reviews/issues/566) - @cynthia, @kenchris

Ken: if you want to implement a db in webassembly - implementing it on top of indexdb not good for performance. Alternative might be to use filesystem access API. You kind of want a big blob of data to read from and write to.  Filesystem API has a lot of permissions issues... This is a different API - similar in shape to filesystem access but no bloat - because security is different.   Can it be abused?  Very nice place with file access - it's mutable.

Dan: [left comment](https://github.com/w3ctag/design-reviews/issues/566#issuecomment-732749514) asking for implementer info and more info on use cases...

Ken: need to look closer at this.

[disvcussion of this vs. filesystem access]

Ken: video editing use case...  other cases where performance is required.. 

Dan: we're back to primitives vs not-primitives

Ken: a native app will use a bit of the hard drive...

Ken: I don't think it will work for a db like mysql because the binary file for the webassembly will just be too big.

Ken: ... other cases like video editing or machine learning ... 

#### [Byte Streams ](https://github.com/w3ctag/design-reviews/issues/567) - @cynthia, @ylafon

#### [WebXR Hand Input API Specification](https://github.com/w3ctag/design-reviews/issues/568) - @alice, @torgo, @hadleybeeman

[some discussion on this and especially questions around what happens when the user's hands differ - e.g. if they are missing a part of their finger...]

Alice: what are the extra joints for... how does it work for missing joings, missing fingers?

Yves: each hand is one imput source...

Alice: medical names is kind of a no-no from our naming principles....

#### [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @hadleybeeman


### Plenary Session

Present: Dan, Peter, Chris Wilson, Rossen, Alice, Yves

Regrets: Kenneth, Tess

#### [Blink Shipping Process](https://github.com/w3ctag/design-reviews/issues/516) - @torgo with Guest Chris Wilson

Peter: welcome, chris...

Chris: issue in design reviews...  some good back-and-forth... first message is: the blink shipping process is continuing to be refined.  

... we want to have TAG reviews be useful. not rubber stanps, but not delaying product schedules... 

... we have early notices when incubation starts... we then send an email to public-review-announce@w3.org - PING uses this to pick up notification of new incubations...  The developer trial - built enough code to be useful but under a flag - not in an origin trial. That's going to become a notification point to the dev community.

Dan: [lays out some of the questions]

Chris: not everyone who goes through this process is a long term standards participant -they might not understand what value TAG review gives. We don't want to give an easy out to skip TAG review....  A lot of the immersive features for example - get incunated in a community group - one of the vendors wants to implement and then goes for TAG review.  WebRTC feaures - "do we need to get a TAG review on this" - maybe, because there haven't been a review in that area recently.

Dan: design principles, s&p questionnaire, explainer... how do we make sure these are being worked on early...

Chris: S&P questionnaire a good way to get useful guidance to people... people need to understand right points to ask for TAG review - and how to structure that ask as well.  Early notiication of "we're gonna look at this problem space" and notification of dev trial - ... makes it more clear when to ask for a review... 

Rossen: couple of points - some of the additional process being added - how do you guide engineers who have less experience in standards...  Nobody reads the design guidelines... making engineers go 

Dan: how do we make them more palatable? Seires of tik toks?

Rossen: yes people don't read those - they add value - people don't have the time to dig into them - creating summaries can help a lot.  entertaining the idea of a check-list that is random. Gamify the system....   The reason why the security questionnaire works well is that it's short and it prompts people to think.   Effort to create a questionnaire for the design principles would go a long way.

... is there an opportunity for early binding so the reviews don't turn into "looking backwards" and fixing lack of knowledge of the design doc, etc...

Chris: we have beefed up the standards mentor - any feature that you create you should get someone as a mentor to help you.   Iterating on the chrome status tool ... walking people through that.  One challenge is : varried amount of standards experience in the team working on chromium...

... what guidance can we give people about when to ask to TAG review and what expectation should you have about response?  

... how to structure the guidance....

Rossen: my take is- the earlier the engagement the better.  I've seen a lot of reviews marked as "early review" from the PoV of the enginner but these are not designs that are early.   Sometimes the idea might not be a good fit.  Ideation level of engagement - could be super-low-binding - not a design review but an ideation review... 

Alice: explainers that are like a paragraph... might be good in some cases.  moving the initial contact with TAG to step 1 ... there's a tension between "nothing to review" .. before they've done all the work... and writing a 2000 line ...  Could make people defensive.

Rossen: also allows people to make connections early on... 

Chris: dovetails well with revamp of the [blink] process... initial announcement is sometimes at the end of the feature design phase... 

[discussion of development of toast]

"don't fall in love with your first good idea" <- attributed to dimitry glazkov

[raising issue of incubation... ideation level engagement...]

Chris: if we had a signal of incubation - TAG could pay attention to that...

... maybe we need a 2-stage review.  New API design idea... the one-paragraph explainer. 

... example of web bluetooth ... 

Alice: chrome status is organized around features...  we want to hear from folks who don't have a feature.  in AOM we started with one idea, we refactored after feedback, now we have 5 separate things...   Your first instinct would be "what API do I want to interact with" vs thinking the underlying need.

Alice: not asking the "what is th need" question is not good

Dan: we could hook into whatever incubation process when we are putting our own agendas together...

Peter: i would like to see **something** that triggers us to look at things... It should have a sniff test beforehand. Also we should not be blocking people.  One of the ideas of the FYI review would be to look at them at a higher priority on the triage pass.  Sometimes we want to give a signal : go ahead, but don't take it as "passes tag review".

Rossen: is the time that WICG repos get opened  - those were not early ideation...  

Chris: i'd prefer to get a little earlier - but they need to be structured enough so people think it's an interesting problem to solve... 

... filing issues in a proposals repo to get new repos started...

Rossen: we need to make sure we're not going to be flooded with a firehose...    Incubation/ideation; features that are new but not revolutionary; catch-up features. Catching up on features already shipped by others... the last one should be a no-op from a TAG PoV.  

Dan: sometimes things get stalled... sometimes there is an impasse... how do we deal with that...

Alice: could there be an intergation with chrome status to the TAG review...  to highlight that there is a stalled review?

Chris: we're revamping chrome status... not as obvious as it should be... 

Rossen: how are "closed - not satisfied" reviews perceived?  Does it change anything?

Chris: yeah - TAG review and it's oucome is one of the strong signals that API owners look at before deciding whether to ship a feature.  Review from the TAG; partner feedback; otheer browser vendors; security & privacy review... a negative review from the TAG should result in it not shipping. 

Alice: you can hook into our labels ... labels should give more insight.

Peter: wrap-up - consensus on 2 new types of reviews - **fyi review** for something small. **Ideation review** where we get in early... may be triggered on WICG repo being created or email to incubation mailing list... 

Chris: we should have the early ideation engagement not only in TAG review... 

Peter: we can use labels.... and pick it up with a bot.

Dan: we also took an action to work on a simplified / questionnaire version of the design principles... make it more accessible.





#### Breakout Rollup

#### Issue Triage
