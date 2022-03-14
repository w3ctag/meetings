# TAG Teleconference
#### 07-09 March 2021

---

## Agenda:

### Breakout A (Europe / US) - [2022-03-07](https://www.timeanddate.com/worldclock/converter.html?iso=20220307T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348)

### Breakout B (US / APAC) - [2022-03-08](https://www.timeanddate.com/worldclock/converter.html?iso=20220308T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia, @atanassov
* [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou
* [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou
* [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342)

### Breakout C (APAC / Europe) - [2022-03-08](https://www.timeanddate.com/worldclock/converter.html?iso=20220308T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)



* [Sustainability](https://github.com/w3ctag/ethical-web-principles/issues/66) 



* [Economic Opportunity](https://github.com/w3ctag/ethical-web-principles/issues/68)
* [Abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)
* [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro
* [New principle: all new headers shall be structured headers](https://github.com/w3ctag/design-principles/issues/252) - @ylafon
* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344)
* [New principle: Just because you can do xyz bad thing using another API doesn't mean it's OK to design a new API tha can also to xyz bad thing](https://github.com/w3ctag/design-principles/issues/340)

### Plenary Session - [2022-03-10](https://www.timeanddate.com/worldclock/converter.html?iso=20220310T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Dan, Lea, Peter, Rossen, Yves, 

Regrets: Hadley, Amy


### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon

[looking at status]

Yves: not sure we need one - since all the ones in HTML are correct

Lea: this isn't from HTML design principles

Yves: I think people aware of HTML are aware of this...

Lea: Might apply to all principles...

[discussion of the fact that this isnot only for the html wg]

Lea: authors create html syntax whenever they define a web component...  We should be documenting this knowledge... 

Peter: I agree we need this.

Lea: I think it should be a  HTML principle.

Peter: Sangwhan made a point this should be tied to APIs ...

Lea: I think it's a separate...

Peter: I agree but we should have the same principle for APIs and CSS...  CSS substitute attribute for property...

Peter: I agree they should be separate principles...

Lea: we should assign to people who don't have too many assignments already... 

Dan: take it to the **plenary** and find an author?

### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

Rossen: anything remaining besides having to write it?

**Rossen to write**

### [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris

Lea: makes HTML less powerful - forces people to use JS for things they shouldn't... Implying that `<details open>` is a mistake? not behind that. There's a weird interaction between the methods and the HTML attribute. Makes me sad if the take-away is that `<details open>` is a mistake - that's very widely used. Sad if people need to use JS in this case...

Peter: typically state for styling purposes is in pseudoclasses not attributes...

Lea: we could add specific pseudoclass for this and for dialoges... 

Peter:  There's syntax for ...

Lea: adding a property doesn't ...

Peter: an issue with web components being able to expose state to CSS... i'd like wc's to be able to add custom pseudoclasses...

Lea: agree

Peter: today in custom elements you widnd up exposing your state as attribute - better pattern is to expose custom pseudoclasses...

Lea: Trying to imagine a world without `<details open>`... 

Peter: an IDL attribute in sync with your HTML attribute ... a CSS pseudoclass called **open**.  

Peter: e.g. if you're hovering should a hover attribute appear on the element? should all state be reflected as attributes? We should have a universal principle that informs all of this.

Lea: what the guidance should be isn't clear - even among us - should we let this ferment longer?

Peter: if we say not all IDL attributes should be reflected as HTML attributes - then why - wat guides reflected vs. not?

Lea: some guidance in the [web components guidelines](https://www.w3.org/2001/tag/doc/webcomponents-design-guidelines/#native-html-elements) on this? ["use attributes to reflect non-complex data"]

... The fact that the IDL attribute has a different state than the HTML attribute but they have the same name has been a source of confusion for years...  I was thinking of 279 and [289](https://github.com/w3ctag/design-principles/issues/289) - related issues. Also related to [348]().

Peter: *If they're not being synced then they probably shouldn't have the same name.* 

[...more debate...]

Lea: there's a lot of IDL properties on existing elements - the ones authors primarily know about are the ones with attributes...  If certain aspects of an API are exposed through HTML syntax - you can interact using existing APIs existing selectors.. otherwise you need to add new (e.g. pseudoclasses) for it. increases the size of the API surface...

Peter: what would be the guidance for adding a pseudoclass as opposed to an attribute?

Lea: an attribute needs to make sense as something you set as well.. *hover* is a read only state...  Don't know if that's the whole story.  Similarly for focus - you can set what has autofocused but not what is focused...  Doesn't make sense to set it with an attribute.  Because HTML is reactive and declarative...

Peter: list of CSS pseudoclasses... a bunch that could be trivially derived from attributes.. e.g. *checked*.

Lea: I think *checked* was a mistake - ... it should have been *initially checked*... i don't think *checked* and *value* would be good examples... IDL properties having same name of attributes and not being in sync.

Peter: wondering if the pattern of having an attribute for setting initial state and reflecting that as a pseudoclass.

Lea: less powerful pattern...

Peter: how do you change the attribute without script?

Lea: means libraries can't use HTML elements generically ... 

Peter: if the pattern is in the intial -foo and pseudoclass is foo - how is that harder to learn?

Peter: pseudoclasses and attribute slectors have diff specificity?

Lea: no.  same specificity... 

Dan: not the same name if they're not synced...

Lea: yes - we can agree on that.  So actually that could resolve 279... 

Peter: talking about serialization... serialization needs to reflect attributes...

Peter: ... definitely a notion of state thst's out side of the document - reflective of the env -like hover, focus...

Lea: ...Target...

Peter: examples of state like form controls that should be part of the DOM.... if a box is checked.

Lea: what about visited link status? 

Peter: external to the document...

Lea: what about enabled, disabled...  That should be preserved...

Lea: **document state** and **external state**.... as two categories.

Peter: yes.

Peter: the fact that you are autofilled ... 

Lea: if you could copy HTML to another document...  if inputs were autofilled i would expect them to preserve their value but not necesarilly that they had been autofilled...

Dan: the document should be able to know if it's autofilled

Peter: reflected as a pseudoclas rather than an attribute.

Peter: we have to define what falls into what category.

Lea: I like those two categories - a moment of clarity.

Dan: set 279 to write-me?

Peter: we have an answer to "if they aren't kept in sync then they shouldn't have the same name"...

Lea: I think that's what the attribute is about...

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

### [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348)


## Breakout B

Present: Peter, Lea, Rossen, Max

Regrets: Sangwhan


### [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia, @atanassov

General agreement, assigned to Sangwhan to write

### [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou

Lea to write a PR

### [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou

Pending feedback, pinged mentioned people

### [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342)


## Breakout C

Present: Dan, Amy, Sangwhan, Max, Yves, Hadley, 

Regrets:

### [Sustainability](https://github.com/w3ctag/ethical-web-principles/issues/66) 

Dan: more to do here? agenda+ f2f

Amy: said I'd write something more nuanced

Sangwhan: something like doubled keyed caching does increase the carbon emissions... don't provide enough benefit...

Dan: requires additional downloading...

Sangwhan: worse environmental footprint...

Dan: Agenda+ that (new finding) for the f2f.

### [framework for balance](https://github.com/w3ctag/ethical-web-principles/issues/63)

Dan: I think it's not necessary

Amy: this issue wants to build on the work in intro already done about balancing - but I think out of scope for this document. Maybe a valid thing to do in another document.

Dan: point of diminishing return. Close to say out of scope for this document, but we accept submissions of ideas

### [Economic Opportunity](https://github.com/w3ctag/ethical-web-principles/issues/68)

Dan: I'm resistant to adding stuff if there are existing principles we can add wording too. We have a principle on enhancing peoples power and control. I'm wondering whether we could add text here which says 

Hadley: could also be relevant to multi browser/device .. about no one company have ultimate control, fits with undiscriminating economic opportunity, no bottleneck where someone can limit someone esles opportunities... sketchy though, same argument that ?? were making about rights of advertisers

Dan: you could frame it as..

Amy: priority of constituents is still a factor

Hadley: agreed. Maybe we should feed those points back and say we think these sections are relevant, can you have a look and suggest edits

Dan: looking at UDHR to see anything about economic rights.. right to work, free choice of employment, equal pay for equal work. Those kinds of economic rights the web should be supporting but I'm not sure we need to.. if we were going to put something in here it should be about individuals rights rather than something about anti competitive or companies competing. It's about something that usports individuals economic rights

Amy: i think it fits into power and control - a sentence in there...  [something somneting anticapitalism]

Hadley: the point [Larry makes](https://github.com/w3ctag/ethical-web-principles/issues/68#issuecomment-985977568) ... rules about consensus, etc... economies of scale.. is important enough statement about w3c that it would be helpful to have it officially enshrined somewhere. Not sure if here.

Dan: I think it's overkill for this. We're nt trying to write what w3c should be.. kind of.. but more applying .. not guide w3c process from this document

Hadley: true

Dan: only so much as it applies to the technologies we're producing

Hadley: still a ProcessCG? Can we tag them in?

Sangwhan: Tess is in the ProcessCG

Dan: we can get Tess' opinion on whether it can be passed over

Yves: Chair is dsinger. And Wendy is in it.

Dan: [leaves comment](https://github.com/w3ctag/ethical-web-principles/issues/68#issuecomment-1061578321)

### [Abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)

Dan: discuss at f2f?

Hadley: yeah. Can draft something

Amy: +1

### Other Ethics Stuff?

### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro

**agenda plussed -- amy to look out output from TPAC**

Amy: the tpac breakout doesn't appear to have happened

### [New principle: all new headers shall be structured headers](https://github.com/w3ctag/design-principles/issues/252) - @ylafon

Sangwhan: i think we can close this

Yves: I think we can close this.

**closed**

### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344)

Sangwhan: assign me

**agenda plussed for f2f**

### [New principle: Just because you can do xyz bad thing using another API doesn't mean it's OK to design a new API tha can also to xyz bad thing](https://github.com/w3ctag/design-principles/issues/340)

Dan: I like "leave it better than you found it"

Amy: don't magnify harms, don't duplicate harms

Dan: not increasing surface area of vulnerabilities. Maybe for 1 - leave the web better tahn you found it, for example don't increase vulnerabilities, try to fix existing problems while you're building

Hadley: also sounds ethical as well as design

Amy: lots of real world examples we could think of

Dan: I'll draft something before the face to face that we can talk about

## Plenary Session

Present: Peter, Dan, Max, Yves, Hadley, Tess, Sangwhan

Regrets: Lea


### Breakout Rollup

#### Breakout A

Peter: on 278 - we need an author... Tess to write.

Peter: on 279 - clear principle on naming of attributes vs properties - 289 and 348 related

Tess: when we designed the dialog eleement part of why we didn't add a pseudo was because we had the attribute.. selecting on the dom attribute would always work.  This may be regrettable.

Peter: i think for details it makes sense - not sure it makes sense for dialog.  Counter examples of everything.

Tess: the media elemtent in particular- if you're used to using other elements they're behavior is quirky.  Given context - it makes sense.

Peter: we didn't discuss media elements...

Tess: volume... muted... one or both reflects to an IDL attribute called "default muted" etc..

Dan: we can close 279 if we write this basic thing - lea is signed up as an author.

#### Breakout B

Peter: Sangwhan assigned to 266. 277 Lea to write. 131 pinged people. 342 question as whether it should be in design principle or promises guide... 

#### Breakout C

Dan: we discussed a "leave the web better than you found it" top line principle. (340)

[discussion on structured headers - 252]

Yves: don't recall a place we're ok about not using structured headers... 

Peter: Found the issue: [baggage](https://github.com/w3ctag/design-reviews/issues/650) ... using cookies instead of structrued headers... 

### Issue Triage
