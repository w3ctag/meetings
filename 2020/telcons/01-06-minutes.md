## TAG Teleconference
##### 06-08 January 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-01-06](https://www.timeanddate.com/worldclock/converter.html?iso=20200106T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris
* [Event-Level Click Conversion Measurement API](https://github.com/w3ctag/design-reviews/issues/418) - @hober, @torgo, @hadleybeeman, @lknik

#### Breakout B (US / Asiana) - [2020-01-06](https://www.timeanddate.com/worldclock/converter.html?iso=20200106T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon
* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

#### Breakout C (Asiana / Europe) - [2020-01-07](https://www.timeanddate.com/worldclock/converter.html?iso=20200107T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* n/a

#### Plenary Session - [2020-01-08](https://www.timeanddate.com/worldclock/converter.html?iso=20200108T210000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage


-----


### Breakout A

Present: Dan, Kenneth, David

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461)

Dan: I'd like to see more disucssions of user stories in the explainer

David: I filed 2 issues on their repo... #478 & #482 - detailed algorithm thing about use of promises... other one was interaction with permissions stuff - changes required to permissions API spec... There is an example in the explainer that encourages bad practices... referenced 2 issues in permissions API spec - #189 

Dan: reviewing the privacy & security self check response & privacy considerations section - they are really comprehensive. I'd like to see Lukasz's comments.

David: NFC seems less scary than USB - much simpler tech...

Ken: It's a way to store and read data -- there are other lower level commands, more in line with USB, but those aren't supported in WebNFC... Could be used for passports and things...

Dan: opportunities for unintentional use... - leakage of PII?

Ken: there are a lot of mitigations in the spec about that. If you want to make sure that people are not changing content - e.g. smart posters... people put a nother sticker on top...   could send you to a malacious web site...  apps should use some signatures...

Dan: is that discussed in the spec?

Ken: yes it's discussed in the spec though no special APi for adding the signatures...

Dan: any other implementations planned?

[...not at this time...]

Dan: there is in Safari a FIDO -related use cases for NFC... But currently orthagonal to this... 

Ken: you could do a polyfill on top of webnfc potentially...  One of things we're not exposing is access to the secure elements... 

Dan: we should get some feedback from Tess maybe... just to see if there is any overlapping set of concerns that could be brought together.

#### [Payments -  shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) 

Ken: we got some feedback...

David: my initial cocnern is what the user consent mechanism is... it's not clear to me how the user knows what they are consenting to... how the process may reveal my address.

Ken: this is for payment apps - the payment app knows your address and whether it should share that with ther web site.

David: I'm not sure I trust all the payment handlers to have as much of a focus on privacy as say web browser makers...

Ken: maybe you want to get a trusted UI of what has been shared...

David: the entire reason for this API is to reduce the complexity of the API flow... but do we trust the payment handler. Or does the browser need to add additional UI?

Dan: is that feedback registered with them?

[reviewing responses to comments]

[david to write some more int he issue and we will bump...]

#### [Event-Level Click Conversion Measurement API](https://github.com/w3ctag/design-reviews/issues/418) 

[bumped as others need to be part of this discussion]



### Breakout B

Canceled due to regrets

### Breakout C

n/a

### Plenary Session

Present: Kenneth, Peter, David

Regrets: Alice, Tess, Lukasz, Hadley, Sangwhan, Yves


#### Breakout Rollup 

Kenneth: [Summary of Breakout A]

David: someone from Mozilla will be looking at NFC

#### Issue Triage

Lack of quorum to make any progress

---



