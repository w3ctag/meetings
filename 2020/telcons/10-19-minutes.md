## TAG Teleconference
##### 19-21 October 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20201019T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @dbaron, @torgo
* [HR review of IMSC 1.2 FPWD](https://github.com/w3ctag/design-reviews/issues/474) - @hober, @hadleybeeman
* [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris, @atanassov
* [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov

#### Breakout B (US / APAC) - [2020-10-19](https://www.timeanddate.com/worldclock/converter.html?iso=20201019T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Permissions policy (formerly feature policy) evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @alice
* [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov

#### Breakout C (APAC / Europe) - [2020-10-20](https://www.timeanddate.com/worldclock/converter.html?iso=20201020T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris
* [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron, @atanassov
* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon

#### Plenary Session - [2020-10-21](https://www.timeanddate.com/worldclock/converter.html?iso=20201021T050000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Hadley, Peter, Kenneth, Tess, Rossen

Regrets: Yves, Dan

Scribe: None
 
#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @dbaron, @torgo

#### [HR review of IMSC 1.2 FPWD](https://github.com/w3ctag/design-reviews/issues/474) - @hober, @hadleybeeman

https://www.w3.org/TR/ttml-imsc1.0.1/
https://www.w3.org/TR/ttml-imsc1.2/

Propose close

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris, @atanassov

Rossen: We had few rounds of review for this proposal. The main feedback to the authors was that if they were to separate cross vs same origin unsigned bundles the progress will be faster. Furhter, none of the concerns we raised as of Aug 17 were addressed.
... Propose marking as Waiting for Author Feedback and moving on.

All: Agreed.

#### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov


### Breakout B

Present:

Regrets:

#### [Permissions policy (formerly feature policy) evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @alice

#### [Personalization Semantics Explainer and  Module 1](https://github.com/w3ctag/design-reviews/issues/476) - @alice, @hadleybeeman, @atanassov

### Breakout C

Present: Dan, Alice

Regrets: Kenneth

#### Discussed APA joint meeting

Dan: We discussed with APA about pronounciation - integrating SSML into HTML - we opined that a ligheter touch way might be better 

Alice: what you want is some kind of decorator pattern - what CSS does. A little bit of markup in the HTML that something else can go in and attach extra data to.  Difference with MathML and SVG is that they will always be presented.  It's part of the document. Whereas this is metadata. 

Dan: adding attributes rather than adding elements

Alice: Data-ssml - converts the SSML to JSON.  What I would want is something that - you could have a separate doc - an SSML doc that you could link into via well-known attribute. Pull in the SSML doc as a resource.  Similar to CSS but instead of classes & selectors it's just one doc - give each pronounciation an ID.

Dan: And use a meta tag

Alice: like a "link" tag.  But don't know if that's close to feasible.  Could you annotate with a `speak` attribute that matches the IDs?  Then the ask is a single attribute and a new link type.... you might want a template format...  SSML+templates.... 

Alice: *writes an example of what it might look like*

```xml
<speak id="digits"><say-as interpret-as="digits">{}</say-as></speak>
```
```html
<link rel="ssml" href="my.ssml">
<p>
  According to the 2010 US Census, the population of <span speak="digits">90274</span>
  increased to 25209 from 24976 over the past 10 years.
</p>
```

Alice: could you do it as a web component?  You do it as a component - the component replaces the span ... then you're back to square 1 because what interprets the ssml.

Dan: let's feed this back and encourage them to open up a design review issue and keep us in the loop.

#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @dbaron, @torgo

We discussed Mounir's feedback..

Alice: yes, agreed that this type of hit testing is different from document hit testing.  

Dan: yes - 

Dan: and agreed on Mozilla's feedback as well as the feedback on use of this API in the VR enviroment.

#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @cynthia, @torgo, @kenchris

#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron, @atanassov

#### [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon


### Plenary Session

Present: Alice, Sangwhan, Tess, Peter, Dan

Regrets: Kenneth

#### Roll-ups

PEter: what can we close?  474 IMSC

Tess: They've gone to Rec.

[agreed to close]

#### APA Joint meeting

Tess: they have identified a real problem - the intent is to make changes to standards and browsers to work with voice agaents - but no participation from voice agents. I tried to encouage them to talk to the voice agent people first - to validate the design. They need to get buy-in from people who would use this.

Alice: My thoughts were around - itirtating on their solution could we come up with a solution that doesn't invovle adding extra XML into the main document. Could we come up with a way to have the SSML in a separate resource that you refer to?  It kind of depends on how it's gonna be consumed. 

Rossen: Also: you can build pretty awesome read aloud experiences right now in the browser just using HTML and the accessibility tree. What is the thing we're trying to fix?  For example, our [Edge's] built in read aloud is working the way I described - using the accessibiltity tree and including the speach API - and had good feedback on.

Alice: What about the example - where you have a zip code and you want to be able to annotate as "speak as digits" rather than number? 

Rossen: You can build models around recognizing this type of content without augmenting the content layer. Without additing additional metadata and micro-formats.

Alice: so it's not necessary to give the author control over that - what is doing the speaking could be responsible.

Rossen: in other words, if you're looking for something to work by default... when you get into permutations - this logic sits on a higher layer than inside the construct itself... I don't think this needs to involve another language and using that as a microformat on top of HTML.

#### Formal Objection Experiment

... is happening ...

#### TPAC

Sangwhan: TAG x DAS meeting on Friday at 6am - privacy & security of HID

