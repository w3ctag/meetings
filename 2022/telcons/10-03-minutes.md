# TAG Teleconference
#### 03-05 October 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-10-03](https://www.timeanddate.com/worldclock/converter.html?iso=20221003T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Fix monkey patching link](https://github.com/w3ctag/design-principles/pull/394)
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober
* [Guidance in exposing some APIs only off the main thread](https://github.com/w3ctag/design-principles/issues/360) - @hober
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [Describe what to do when a feature is temporarily only available on some platforms.](https://github.com/w3ctag/design-principles/pull/357)
* [Guidance about serialization](https://github.com/w3ctag/design-principles/pull/367)
* [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366) - @LeaVerou


### Breakout C (APAC / Europe) - [2022-10-04](https://www.timeanddate.com/worldclock/converter.html?iso=20221004T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
  * [Start developer version](https://github.com/w3ctag/design-principles/pull/386)
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo
* [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)
* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia
* [Restrictions](https://github.com/w3ctag/design-principles/pull/363)
* Check in on [Ethical Web Principles PRs](https://github.com/w3ctag/ethical-web-principles/pulls)
* Discuss post-3rd-party-cookie-world draft

### Plenary Session - [2022-10-05](https://www.timeanddate.com/worldclock/converter.html?iso=20221005T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)
* [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)
* [New principle: on overloading, for #131](https://github.com/w3ctag/design-principles/pull/372)
* [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378)
* [Meta: How do we work with other WGs?](https://github.com/w3ctag/design-principles/issues/387)
* [New principle: Avoid exposing API that result in synchronous flushing of CSS or layout](https://github.com/w3ctag/design-principles/issues/388)
* [New principle: Guidance on options disctionaries and default values](https://github.com/w3ctag/design-principles/issues/391)
* [Move out most of "non-fully active" handling guide](https://github.com/w3ctag/design-principles/pull/392)
* Discuss new schedule for after the time change

-----


## Breakout A

Present: Lea, Amy, Peter, Yves, Rossen

Regrets: Dan, Hadley


### [Fix monkey patching link](https://github.com/w3ctag/design-principles/pull/394)

Yves: just fixing a link, seems okay

Peter: *merges*

### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

Lea: we had a breakout on this in the f2f

Peter: anything to do besides write it?

Lea: we did a lot of brainstorming about examples, just needs someone to write it

Peter: assigned to Tess but anyone else wants to take a stab?

Lea: tempted but busy

### [Guidance in exposing some APIs only off the main thread](https://github.com/w3ctag/design-principles/issues/360) - @hober

Lea: Sangwhan would be helpful

Amy: any discussion by TAG members? Issue by non-TAG members

Peter: not that I know

Amy: Next step: post in slack for async work by those with the right expertise to see if and what needs to be written?

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

Peter: had a discussion with folks about toggles

Rossen: what would that mean for ARIA? where you have a lot of state exposed as attributes

Lea: these attributes are not dynamically updated by the browser

Rossen: I'm not sure about that

Lea: any cases in mind?

Rossen: looking... especially for landmarks and things that come in and out of view. When you say updated by the browser what do you mean?

Lea: following interaction

Rossen: all of them.. aria selected..

Lea: usually the author that has to write js to update them

Rossen: sure they are, through form controls. ARIA checked..

Lea: is automatically updated by the browser?

Rossen: I'm pretty sure that's what the AAM asks you to do

Lea: you're not meant to use ARIA checked on a checkbox

Rossen: you can use it however you want

Peter: are these attributes creating or defining state, or just reflecting state that's managed elsewhere?

Rossen: they mostly reflect an abstract state. But tehy'rea ll about state. It sounds like a decent intent, but heavy handed. 

Lea: ARIA attributes are not updated by the browser.. try that out in a codepen. I think you're thinking of an accessibility tree? They're updated there. The browser doesn't add or remove or change values for ARIA checks unless you do it as a develoepr. Even IDL isn't updated. Remains unchanged regardless of whether you check the checkbox or not.

Rossen: *tries it*

Lea: the issue is if you have an IDL attribute, when should there also be an html attribute for it? It seems obvious that for most primmitives there should be. It seems obvious that for certain complex objects there shouldn't be. There's some confusion about where the threshold is. At what point is it a bad idea to have attributes for a state property?

Amy: maybe draft a PR with a suggestion and discuss that concretely? Or find someone in the community who might have a good idea?

Lea: I have opinions.. there is not consensus..

Peter: start by writing that down, then we can see

Rossen: if you take the opening section of the issue.. Conversation at the end with Peter, around state which is preserved through clipboard and what that means, if this could be used as an evaluation criteria. 

### [Describe what to do when a feature is temporarily only available on some platforms.](https://github.com/w3ctag/design-principles/pull/357)

Amy: PR by Jeffery Y who has been off for most of the summer but is back now. May need a nudge to respond to feedback?

Peter: pinged

### [Guidance about serialization](https://github.com/w3ctag/design-principles/pull/367)

Rossen: Started as something basic to build on. Took comments from a discussion and spec-ified them a bit. Needs examples. I think one of the places I was going was.. I hinted serialisation of CSS grid templates and what that would mean from the pov of serialisation expectations. It's CSS specific but so what.. it's a decent example that I can expand on. 

Lea: what about serialising CSS colors?

Rossen: yeah. Broad serialisation problem. I guess a little more scoped. Good example.

Lea: not trivial, needs decisions, but something most people are familiar with. 

Rossen: right. A simpler example could be starting with a keyword and getting back values

Lea: mm, I like that better

Rossen: having that sustain consistency through roundtripping.

Lea: be nice to have something like in these cases you use a keyword and get back a value; in other cases it's important that the keyword is preserved.

Rossen: current color for specified value is definitely preserved. Computed value for current colour I believe is going to give you current colour. We certainly cascade it as current colour. 



### [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366) - @LeaVerou

Lea: straightforward. Do we have consensus?

Peter: what is meant by primitive arguments? A simple argument?

Lea: for example.. canvas elements take a series of positional arguments.. whereas if it took a dictionary you'd know what's the radius, what's the x, what's the y. A trend in APIs the last few years to use named args through dicts, unless the positional arguement is very very obvious what it means. We already have a principle saying primitive arguments should use a dict so you don't have boolean traps or nonobvious random numbers. I opened this to exapnd this guidence from primitive to any argument that is either optional or not obvious from its value and position. I guess there is some vaguness about what obvious means. It's a judgement call. Eg. I think toLocaleString is a good example. The locale is a string and positional but everything else is a dict. It's very obvious when you look at a function call that the first arg is a locale from its value. Booleans or numbers are not as obvious. I think often objects are also not obvious. Using the example of fetch. We have a dict arg for headers. Imagine if that was positional just because its an object not a primitive. It's a good design that it's a dict arg. Otherwise it would be confusing.

Peter: i get the basic point about using a dict to get named args. Ideal in the case of optional args. Pushing back as it's written now, talks about dicts over primitive arguemtns, but not clear what constitutes a primitive argument?

Lea: numbers, strings, booleans

Peter: simple literals?

Lea: I do think that strings are often different that numbers and bools when ti comes to this

Peter: it would be very easy to push this to the extreme and say dictionaries for everything so it's named and obvous. BUt I think that would be also bad to do that. 

Lea: yeah.

Peter: the goal here is what's the clear advice for when something should not be a dictionary.

Lea: rule of thumb is if you look at a function call, can you tell what each arguement is? ToLocaleString with locale is an example. AddEventListener is an example. Pretty obvious what the event name is and what the callback is. But everything else lives in a dict and that's great. When capture was a boolean it didn't make any sense. You'd see true at the end and ask what is true?

Peter: how do we distill that into practical advice? Is it fine when it's positional because its described by the name of the function? Or is it a judgement call over time? Something we can distill down to make this easier for people?

Lea: strings I don't think we could codify. Strings can represent two things. An enum in the web platform is a string often. In those cases it's usually pretty obvious what the arg means. i the string can be one of a finite number of strings. Or when the string is a freeform arg of any text. It can be more difficult to tell what it's supposed to represent. I don't think we can have a hard and fast rule that string either is or isn't self-explanatory. That's a judgement call.

Peter: Trying to get something more concrete. If we tell people it has to be a judgement call it's nice to say the metrics used to judge this.

Lea: even callbacks. Usually .. I'm thinking in addeventlistener callbacks are obvious. Promisethen..

Peter: described by the name of the function. Function is describing thething being passed.

Lea: then isn't descriptive, but is central to the purpose..

Peter: do a gree that anything optional should be in a dict. Should have some guidence over what is obvious and what isn't obvious. We need to drill down on what makes something obvious.

## Breakout C

Present: Dan, Amy, Yves

Regrets: Sangwhan


### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
  * [Start developer version](https://github.com/w3ctag/design-principles/pull/386)

### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

### [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo

### [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)

Amy: needs shortening. I'll have a look then ping in slack for TAG review.

### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia

### [Restrictions](https://github.com/w3ctag/design-principles/pull/363)

### Check in on [Ethical Web Principles PRs](https://github.com/w3ctag/ethical-web-principles/pulls)

### Discuss post-3rd-party-cookie-world draft

[drafting]

## Plenary Session

Present: Dan, Lea, Yves, Tess, Peter

Regrets: 

### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

Lea: not particularly actionable and maybe we should axe it?  Do we need this?


### [New principle: on overloading, for #131](https://github.com/w3ctag/design-principles/pull/372)

### [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378)

### [Meta: How do we work with other WGs?](https://github.com/w3ctag/design-principles/issues/387)

Lea: concern raised by Elika... 

Tess: if CSS wg wants to have a CSS design principles that would be great - we're not stopping them.  Feels like stop energy.  If it's work CSS wg wants to take up then let's move over portions of our documents to them. Absent that they are welcome to pitch in on our doc.

Yves: If any wg wants to do a design principles for their domain that's good.

Lea: So what can we do to encourge them to contribute?

Dan: anyone can send a PR...

Lea: doesn't privelidge the CSS wg... And in practice they're not contributing...

Lea: CSS wg shoould "co-own" these principles...

Dan: suggest: establish a joint effort; we could ask CSS to review our CSS-related principles; agree that we will seek CSS wg consensus support for CSS-related design principles we introduce in the future; maybe have co-branding?

Dan: example of privacy task force...

Lea: the fact that we have CSS wg members in the TAG is a coincidence... we should have a process that doesn't assume that.

Dan: i think it should be one doc... 

Lea: agreed.  Wouldn't want to have to go to different repo for each design principles...

Peter: there was a separate HTML design doc and we are folding those in... we do ping WhatWG ...

Lea: the results of reaching out may be the same ... they feel CSS principles something that happens to them.  Can we do something more structure that would have the same effect but they feel more in control.

Dan: we could put a tracker label on our design principles issues that are specific to CSS as an invitation to get our issues into their agendas - explicit invitation for CSS wg ...

Lea: would ne nice to have a process that is not specific to the CSS wg.

Lea: They (CSS) should also discuss how this should work...  We need to ask CSS who would participate / who would be interested.

**Next steps**: Lea to start the dicussion in CSS wg ... and come back with feedback.

### [New principle: Avoid exposing API that result in synchronous flushing of CSS or layout](https://github.com/w3ctag/design-principles/issues/388)

### [New principle: Guidance on options disctionaries and default values](https://github.com/w3ctag/design-principles/issues/391)

### [Move out most of "non-fully active" handling guide](https://github.com/w3ctag/design-principles/pull/392)

Lea: maybe we should merge this when the new guide isn't to do any more...



### Discuss new schedule for after the time change

### Breakout Rollup

**Note:** list issues talked about this week to mention in commit message so issues are linked to the minutes

#### Breakout A

#### Breakout B

#### Breakout C

### Issue Triage
