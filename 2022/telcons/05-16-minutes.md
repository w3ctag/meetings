# TAG Teleconference
#### 16-18 May 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-05-16](https://www.timeanddate.com/worldclock/converter.html?iso=20220516T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: guidence on user activation](https://github.com/w3ctag/design-principles/pull/365)
* [New principle: Inclusive Naming Choices](https://github.com/w3ctag/design-principles/issues/253) - @hober, @rhiaro
* [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
* [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober
* [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober
* [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou
* [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober, @alice
* [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris
* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris

### Breakout B (US / APAC) - [2022-05-17](https://www.timeanddate.com/worldclock/converter.html?iso=20220517T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)
* [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)
* [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion
* ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov
* [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
* [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov
* [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou

### Breakout C (APAC / Europe) - [2022-05-17](https://www.timeanddate.com/worldclock/converter.html?iso=20220517T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo
* [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman
* [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369) - @torgo

### Plenary Session - [2022-05-19](https://www.timeanddate.com/worldclock/converter.html?iso=20220519T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* F2F Dates
* DID FO Report
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Lea, Peter, Tess, Amy,  Hadley, Rossen, Yves

Regrets:


### [New principle: guidence on user activation](https://github.com/w3ctag/design-principles/pull/365)

Tess: very concise, good. Worry.. might not be a real worry.. user activation or user gesture restrictions didn't used to have any standardized existence in the platform. It was an innovation of browser to add additional security. Arguably we've had them for a very long time because input type file, for instance, in order to get to the file picker you have to activate the form control in some way. But it's something that started to get applied to more things that just form controls in the last like 15 years. Overall I think that's an innovation that improved things, and it's great we're defining user activation in a cross browser way. The uneasiness I have is that there might be some other way to restrict powerful features that someone thinks up in the future that isn't user activation but is something else. But tha'ts equally as effective or even more effective. If there were such a thing I wouldnt' want us to require people to still have to have a user gesture restriction even if they were using the new thing. The text is great for the platform that exists, I just worry about people interpreting this as over-constraining solutions in the future where someone more clever thinks up a better way..

Amy: we can update the design principles..

Tess: worry someone would think up something cool and discard it

Dan: would it help to add ..

Tess: at a minimum? it says that already. Or equivalent

Dan: or to indicate engagement, such as..

Tess: thank you for wording it that way. An existing thing people have been trying. Chromium has this notion of user engagement with a site and over time if you're engagement score passes various thresholds there are things you get to do without bugging the user as much. If you go to youtube 3 times a day and always grant it permission to play audio, maybe after a month of that maybe the browser says it doesn't need to bother the user about whether they want youtube to make sounds. At that point on day 32 when you load youtube, does that meet the user activation requirement? Strictly no? If you had such a mechanism in your browser I don't want to tell you you can't use it

Peter: maybe instead of saying api should require activation, should require user consent. One way of indicating consent is user activation..

Dan: worried about using 'consent' .. legal..

Tess: that's even worse

Dan: these APIs should be designed to require some indication of user engagement in order to function..

Peter: intention?

Tess: better than engagement

Hadley: I agree

Dan: and such as user activation

Tess: so do we change the headline of the principle?

Dan: I don't think so. My preference would be not to. But rather to introduce user activation as a form of intention and that can always be.. [adds suggestion]

Tess: seems good, leaves enough wiggle room. I worry about if the world changes under us, we have to notice and update the text. This seems better.

Dan: some of the point of this document is to include some stuff that people have been saying or browsers have been doing, or general patterns. We all know this. The thing that came to mind was also the idea of a private browsing mode. That was never specified by anybody but was increasingly being deployed and other specs were starting to refer to it, like how an api should behave in private browsing mode, so it seeme dimportant for us to say something about it. This feels the same way. Need a thing to point to for people talking about user activation. Otherwise different people can be using it to mean different things.

Peter: concerned with the heading.. says user activation, but we mean user intent

Dan: the reason I think it's appropriate is so that when somebody is trying to figure out which part of the design principles is about user activation they're not going to see it if it's not in the heading. If it's buried..

Peter: understood

Hadley: not necessarily starting with user activation in their heads

Dan: we've had enough apis come at us that mention user activation. In peoples minds already. We're trying to say something about user activation in a way that can be extended, to Tess's point, if there are other mechanisms that develop. We can always change the name of the principle. To me this is actually about user activation. We should call it what it is.

Peter: okay

Hadley: works for me

Amy: [merges]

### [New principle: Inclusive Naming Choices](https://github.com/w3ctag/design-principles/issues/253) - @hober, @rhiaro

Amy: Sangwhan made [a commit](https://github.com/w3ctag/design-principles/commit/56f2c9609446b886178ebb8010d66e7532400fd2) that references this a while ago

Dan: I think we can close this

### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon

Lea: this has been a to-write for Tess..

Tess: ..since time began

Lea: since march 10

Tess: the idea is to push people towards not introducing new attribute names?

Lea: yeah

Peter: using href ..

Lea: don't do things like object data again

Tess: okay, will work on it

### [Guidance on re-using/creating task sources](https://github.com/w3ctag/design-principles/issues/38) - @hober

Dan: the last comment is from Travis

Tess: anyone want to tag team?

Rossen: I'll help

### [Create launching point into the Performance APIs overview doc](https://github.com/w3ctag/design-principles/issues/52) - @hober

Rossen: I'll help with that one too.

### [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou

Tess: example is html input element?

Lea: this is about JS APIs

Peter: but that's a good point about HTML. New issue?

Lea: what would overloading be in html?

Tess: I was thinking of the type attribute on the input element.  Never do that again.

Lea: we should totally have a principle on this. May already have an issue.. I'll make one if not.

Peter: meanwhile, back on JavaScript. We have feedback from Tab.

Lea: I'm a little worried.. I have some reservations about whether this is a principle to make tooling easier, or if it's better for usability. I see some arguments that it's easier on IDL authoring and tooling. But the question should be does overloading make things easier or harder for authors?

Rossen: can you tell me how you differentitate between one and the other? Between successful authoring without successful tooling?

Lea: the arguments I see are about spec editors tooling, not like VSCode

Rossen: I see, completely misunderstood.

Lea: if it's easier on tooling for authors that's definitely an argument against overloading

Peter: I'm not sure if there's a strong argument that overloading is bad for authors

Tess: strong argument it's good?

Rossen: yeah

Tess: priority of constituencies.. spec authors are important but not as important as everyone else. We shouldn't do anything that makes things hard for spec authors if everything else is a wash

Lea: argument for overloading.. api surface.. longer to document, to teach

Tess: disagree. Same amount of prose if you're overloading or not. If it has two API surfaces, or one that is overloaded, you still have to write two bits of text

Lea: you need to know whether you need to look for a different function at all as an author. Whereas it's easier to look for one function and figure out which arguments. Looking for a differnent function all together is more complicated, you don't even know what you don't know

Rossen: some thinking happening already that might make it into some kind of prose, to further the issue or close it.

Lea: there are libraries.. i know on the web platform overloading tends to be avoided, but libraries employ very heavy overloading and authors like using them. Indicates that there is something there. Why do authors like that sort of thing so much? 

Tess: also indicates argument for consistency. If some corners heavily rely on overloading but mots of it doesn't, you're not only asking people to learn a different technique, but to hold these two fairly different abstractions in their head at the same time

Lea: the whole point is that because there are parts that do overloading and people want to discourage that.. It's not used as often as in libraries, but not like it's not used at all. And confusion about kinds of overloading that is acceptable. Certain things are considered overloading by some, that are acceptable. AddEventListener has multiple signatures, which is fine. But tha'ts not what they want to discourage. It's the type where you have entirely different numbers and types of arguments. It might be hard to define this, even if we agree it's a good idea. To tease apart the kind of overloading that we like and the kind we don't. Especially since everyone who has read this issue seems to be confused. I'm not sure people understand what is discouraged.

Tess: if everyone is confused by something that is a great argument for us to add something to design principles. Clear some things up. But the opposite - if there is a bunch of places people are happy with the overloading, and a bunch where people aren't, maybe a black and white principle is not going to cut it. If we can't find a principled way to describe the difference between the cases we like and cases we don't, maybe we shouldn't have a principle.

Peter: overloading is a tool that can be used in  good ways and in bad ways. **1** A method with the same name that has different behaviour based on the types of inputs, that's bad. A method that just has optional arguments, that's fine. Acting on a single thing vs acting on an array of things, that's fine.

Lea: right now there are different methods names in most places where you want to handle a single thing vs multiple things. I don't think we want to encourage that. Would be better if we had the same methods.

Peter: that's a specific example. I've certainly done it that way in my code in other languages. If we have a lot of precedence of different names we should identify that as a case and say for consistency do this pattern this way. **2** There's a form of overloading with a dictionary of options and everyone seems happy with that. Technically not method overloading, but is in principle. I don't see anything wrong with that. The addeventlistener is a case where we've upgraded an api. Originally done with a boolean and later decided a dict of options, but that pattern wasn't in use at the time, so we fixed that.  Can we break this into patterns?

Lea: right now we have objectdefineproperty for single properties and objectdefineproperties for multipple properties. Is that good or an antipattern?

Peter: one answer is consistency. If we can find a lot more examples of one vs the other, we should direct people that way. **3** The other is, when you work with multiple things does that radically change the signiture of the method. I'm literally passing in a single thing vs an array, is that an okay use of overloading? I think so. If there are subsequent arguments that have to change radically because I'm passing in an array, that's not a good use and I should make a separate method.

Lea: all seems reasonable

Peter: anything we're missing?

Rossen: I think you stated four points. Can we prioritize? First around consistency. 

Peter: [recaps]

Rossen: so type overloading is bad?

Lea: there are good examples of type overloading

Tess: addeventlistener is a good example of type overloading. But if you have a method and pass it foo it does x and pass it a bar it does y. What do you call that?

Lea: have there been proposals like this?

Peter: not sure. Agree that optional arguements with a known default value or behaviour is fine..

Tess: not sure? part of what we learned from addeventlistener was that consolidating args in an options dict is bad?

Peter: yeah.. so no optional arguments unless they're a dict?

Tess: I think we already have a principle about using an options bag for things where the functions signature would change radically don't we? Can we reference that text?

Peter: in my mind options dict gets you the same behaviour as named args in other languages like python. You can have multiple optional args and don't have to insert default values to get to the nth one. That's an advantage.

Tess: agree. Other advantage is just labelling the arguments.

Peter: yeah.

Dan: is the current principle you're referring to Naming Optional Arguments?

Lea: [prefer dictionary elements over optional](https://w3ctag.github.io/design-principles/#prefer-dict-to-bool).. apparently generalised over time.. I found an issue to make this even more general, but we haven't discussed this yet.

Peter: Anne's kind of overloading is kinds of subsequent arguments depend on a prior argument.

Tess: example earlier of passing ``(foo, False, False, False)`` or ``(bar, 1, 2, 3)``.. an api where theyr'e booleans if it's a foo and numbers if it's a bar.. is awful

Peter: agree. Should just be independant methods. Do we have agreement on different aspects of this, or something still controversial?

Tess: so far agreement on a bunch of stuff

Dan: I'm not clear on the headlines.. how many things we've talked about?

Peter: do we have enough for someone to write this? Who will that person be?

Amy: [volunteers]

### [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober, @alice

### [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184) - @hober, @kenchris

### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou

### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

### [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris


## Breakout B

Present: Peter, Rossen, Max

Regrets:


### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

### [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion

### ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov

### [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou

### [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou

### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

### [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov

### [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou


## Breakout C
10:
Present: Dan, Max, Amy, Yves, Hadley, Sangwhan

Regrets:


### [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo

### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman

Amy: I think we should punt it until I have a proper think about it... Now I'm leaning towards writing something small.  The scope of it is scary.  Lots of citations... but nothing else in the doc is academically cited... but I feel i should make citations on identity.  

Dan: what is the small thing?

Amy: [1] separation of identifiers and identity ... [2] credentials and authorization being separate considerations.  [3] General statement about people using the web representing many facets of themselves - not good to tie them into one.  Won't use special terms of art.  General statements about "don't do this in a terrible way".  Not that I think people coming into this space are starting with the TAG design principles...

Dan: we should seek early review on this from people who have come to us recently with identity related review requests.. web ID folk? It would be good for this to be relevant to the people who are asking us for advice on identity-related stuff.

Amy: start people from a similar foundation, even if they're building different technical solutions.


### [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369) - @torgo

Dan: trying to get at something like don't use canvas to make UI when HTML would do. Not clear if that is something to address in the design principles. Doesn't apply to spec developers. I agree, but not sure if it belongs.

Sangwhan: our principles are not authoring guidelines

Dan: yeah. Unless there are specific guidelines related to this topic that would relate to the design of new web features. Maybe ask Chris if he can think of design scenarios where this would be appropriate guidence?

Sangwhan: I believe the only cases where this makes sense if you have a connection to a graphics pipeline of some form, is the only place we would recommend canvas. Otherwise canvas has clear accessibility disadvantages

Dan: right, but again that sounds like authoring guidence, something we should stay away from

Sangwhan: not in terms of authoring guidence, but for cases where your'e connecting an output of a graphics pipeline, a raster, to another component in DOM, that is directly translatable to a DOM element.. it doesn't make sense to take a media sync output and crank it into.. say it has to be DOM becuase it has to be accessible. It's going to be a video. I thas to have an auxiliary peiece of infor for an accessibility tree because you can't reason from raw pixels from the video stream. But that's fairly obvious. I do know there's a ?? happening in google docs and sheets where the whole thing is a canvas. I don't know why. I could ask.

Dan: ask, and leave some feedback on the issue, maybe others have .. maybe something else we could say. If it's worthwhile having that as a principle then or if there is something we can say to people building new web technologies or apis then I'm all for it.

Sangwhan: will leave comment

## Plenary Session

Present: Dan, Peter, Max, Tess, Amy, 

Regrets: 

### F2F Dates

**LAST WEEK OF JULY, IT'S HAPPENING**

**Google will host in London 25-28 of July**

### DID FO Report

### Breakout Rollup

#### Breakout A

Dan: we landed a principle on user activation. Closed inclusive naming choices because it was already done. Tess and Rossen volunteered to write some things. 

Amy: [overloading PR (draft)](https://github.com/w3ctag/design-principles/pull/372)

Dan: incorporate HTML into ours is a long term thing.. other things in agenda no update.

#### Breakout B

Peter: rossen, myself and Max... we spent time looking at the cheat sheet... adapting from the security questionnaire... Sangwhan did some prototyping... We took a look at what that script does... what would be in this doc other than the table of contents?  

Tess: would probably just be the ToC...

Peter: less than useful.  Sangwhan raised "these headings are weird"...

Dan: [PR for making headings consistent](https://github.com/w3ctag/design-principles/pull/371)

#### Breakout C

Dan: talked about principles for identity.. Amy enumerated some.. and will think about it more. Chris H opened an issue asking for a principle about appropriate use of canvas element (#369). I'm not clear on whether this is enough of a principle for spec editors vs authors/web devs, in which case it's out of scope for us. Sangwhan said he'd leave a comment.

Peter: is it really out of scope? Given other issue about generating a subset for web developers. If we have adice about canvas, may help shape future directions about how that element evolves. Fair for us to think about how people use the web

Dan: I do not disagree™



### Issue Triage


