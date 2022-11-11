# TAG Teleconference
#### 07-09 November 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-11-07](https://www.timeanddate.com/worldclock/converter.html?iso=20221107T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [Guidance in exposing some APIs only off the main thread](https://github.com/w3ctag/design-principles/issues/360) - @hober
* [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366) - @LeaVerou
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober
* [New principle: Guidance on options disctionaries and default values](https://github.com/w3ctag/design-principles/issues/391)

### Breakout C (APAC / Europe) - [2022-11-08](https://www.timeanddate.com/worldclock/converter.html?iso=20221108T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia
* [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo
* [New principle: Patterns for x() vs xSync()](https://github.com/w3ctag/design-principles/issues/402) - @cynthia
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378)
* [Meta: How do we work with other WGs?](https://github.com/w3ctag/design-principles/issues/387)
* [Request for design principle clarification: Warn explicitly against getters throwing exceptions](https://github.com/w3ctag/design-principles/issues/400)

### Plenary Session - [2022-11-10](https://www.timeanddate.com/worldclock/converter.html?iso=20221110T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Dan, Hadley, Lea, Yves, Rossen, Tess

Regrets: Amy


### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou

Lea: not much progress will will ping Tab ...  we ran into a bikeshed issue. Need to work on this with Sangwhan.

*agreed to take off agemda+*

### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

*question on why this was agenda+*

Peter: what is the status?  Do we have consensus on this principle?

Lea: we agreed we should pick it up...

Rossen: this is about web developers.

Lea: it's about HTML

Peter: Design of HTML. 

Lea: we agreed not to have issues only for web developers - they have to apply to spec developers.  Some will be helpful to web developers and even primarily web developers but still help spec developers.

Peter: do we have guidance on this point?

Rossen: it would be fantastic

Peter: somewhat related - new configuration syntax - I have the same kind of concerns - when should something be a child vs an attribite.

Lea: harder to internationalize an attribute 

Rossen: also accessibility.

Tess: any time you find yourself designing a microsyntax for an attribute you probably want to use child elements.

Peter: a single attribute has structure. If it's a simple thing then... 

Lea: so the microsyntax argument is a good one - doesn't apply to i18n..

Tess: yes it does - 

Lea: cases where you don't have structure in the attribute - it might sitll make sense as a seperate element.

Tess: tooltips is a mistake.  Classic example: you have a word in a foreign language in middle of text in another language - so use title attribute. lang attribute on element that contains the foreign word doesn't apply ...

Lea: should alt have been a seperate element?

Tess: alt is an interesting case - distinct case from ... we want to have fallback content that is rich.. you want a similar situation for img element.  

Lea: fig and fig caption...

Tess: fallback content different from accessible description... 

Tess: one example is a simple value and one might be simple space seperated values. Another example might be style attribute. Not a novel syntax but rather CSS.  Still raises concerns about scope.  

Tess: when the microsyntax comes from somewhere else....  If it's use facing text then better as a child element.

<blockquote>
Principle: favor use of child elements unless the information is super simple.

If user facing text then better as a child element.  [exception of alt tag because ...]
  
Use of a novel microsynatax indicates it should be a child element.
</blockquote>

Tess: I can do it.

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

*question on why this was agenda+*

*punted*

### [Guidance in exposing some APIs only off the main thread](https://github.com/w3ctag/design-principles/issues/360) - @hober

Tess: it's come up in a number of working groups - e.g. webrtc - some disagreements around it.  Maybe not ready to write text. Dom's comment is interesting.  Can be used on the main thread doesn't make any claim about likelihood - if the common case is to be blocking then we don't want the well lit path to be blocking.  If you've never made a worker on your path...  If it fails then the developer can figure out how to do the right things if it succeeeds it might still be a disaster.  I think this kind of API shouldn't be on the main thread period.  Just because you *can* do something doesn't mean you're likely to... With A18n we ask how do you make it accessible by default. So to me we do web developers a disservice by making the easier coding path the bad one.

Peter: i agree in principle - my question is - is there a valid use case?  Is there a good reason?

Tess: i think that's the right question to ask... 

Peter: Is it possible to use it on the main thread vs. "people must use this on the main thread" - maybe jump through some extra hoops to use it on the main thread... 

Tess: mayne you know it's user triggered.  I can see an argument there.  If you can identify a use case where it has to be done on the main thread then OK - but think about the common cases. 

**Tess to write**

### [New principle: Prefer dictionary arguments for all optional parameters (and non-obvious parameters?)](https://github.com/w3ctag/design-principles/issues/366) - @LeaVerou

Lea: spent some time coming up with examples - posted to [my comment](https://github.com/w3ctag/design-principles/issues/366#issuecomment-1265778771). 

Peter: concerned about 'obvious'

Lea: we need a different word

Peter: what's obvious to one person may not be obvious to someone else...  I agree with the point. 

Lea: maybe talking about it in terms of arguments essential to the function's purpose vs arguments that parameterize what the function does.

Peter: extensibility - what if we add additional arguments later on?

Lea: that would have to be a dictionary.

Peter: so if you have one optional argument and then add a dictionary?

Lea: we have examples of both in the web platform... for `padStart` it would have made more sense as dictionary. 

Peter: argues for there's no time we want optional arguments that are not dictionaries?

Dan: doesn't that impact developer complexity?

Tess: tempting to say "sometimes we really know we won't need an extension point" but difficult to say with confidence...

Peter: if there's more than one optional argument then use a dictionary. that's clear. Is there an argument for use of a dictionary with a signal optional argument.

Tess: yes because in the future you might need another optional arg.  If the previous primitive was a string or a number and now you're passing a dictionary then it can cause problems [for compat].

Lea: booleans are the prime case that should always be in a dictionary.

Peter: comes back to "all optional arguments are dictioanries".

Tess: I would prefer "in almost every case it should be dictionaries and not optional arguments."

Lea: we more or less have consensus that optional arguments should be dictionaries - but no consensus on mandatory arguments. Consensus on all optional arguemnts and not just primitives.

**conesneus achieved**

### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

Tess: we had a breakout in london... we added a writeme label. We can remove agenda+.  (also links to https://github.com/w3ctag/design-principles/issues/270#issuecomment-933786019)

**tess to keep**

### [New principle: Guidance on options disctionaries and default values](https://github.com/w3ctag/design-principles/issues/391)

Lea: context - there are multiple points of guidance on how to name boolean arguments. 1. don't name them negatively. 2. don't make the default true 3. have sensible defaults that are the common case. Sometimes these guidelines are at odds.  Difficult to decide how to weigh these against eachother.

**heavy cogitation**

Lea: we don't have guidance that API designers should take into account now common things are... to compare numbers as mumners you have to use numeric=true which is the common case. 

Dan: part of "simple things should be easy?"

Lea: sometimes you can't satisfy them all you have to pick one to violate.

Tess: I don't think there's a global precedence rule sometimes it's a judgement call. We have to learn to live with that.

Lea: Overall I agree - but sometimes there is an overall priority between specific principles.

Tess: yes in specific cases.  When it's clear we should write it down.

Peter: in this case I would lean towards false being default is more important than the name. Which is kind of odd because usually the name is more important. but if you end up with a dictionary with a bunch of optional arguments you want to be able to make it easy for the common case (defaults). I also tend to do - if you have an optional argument where the behaviour isn't clearly biases - make a different method that clearly specifies what they're trying to do.  

Lea: do we agree that naming positively is less important then false being the default.

Dan: makes sense to me.

Peter: more discussion... 

Lea: i will leave a comment with what we discussed today.

Peter: take to plenary take to breakout c...


## Breakout C

Present: Dan, Amy, Sangwhan, Max, Yves

Regrets:

### Celebrating ActivityPub

Dan: well done Amy for your work on the activity pub spec... Getting a lot of use this week with migration ot users to Mastodon...

Sangwhan: why isn't w3c using this?

Amy: there is w3c.social - it's not official

### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia

Sangwhan: need a breakout - maybe next week.

Dan: can co-ordinate with you on this.

**scheduled**

### [New principle: Data Minimization](https://github.com/w3ctag/design-principles/issues/399) - @torgo

Sangwhan: I think we have something on this. A thing from Intel on this.. 

### [New principle: Patterns for x() vs xSync()](https://github.com/w3ctag/design-principles/issues/402) - @cynthia

Sangwhan: 2 converging issues that are antipatterns. All we need to do is say... there are specific cases where a synchronous api is warranted becuase of say web assembly bindings. There's a gap in how webassembly connects to the web world. Because of that there have been patterns emerging where people are creating sync apis, and we don't have the work finished by ecma so we can't recommend people to use that pattern because it's not done. For thetime being the recommendaton is x is always async and if it's going to be sync attach sync to it and think about a deprecation pattern too. The platform will evolve. Webassembly will get a mechanism to address this. Some people have chimed in on [#771](https://github.com/w3ctag/design-reviews/issues/771) - js promise integration with consensus but nobody is shipping yet. We can't ask people to start using it becuase it's not there

Dan: We need a temporary design principle? It's a living document but we haven't marked anything as explicitly temporary. How should we do that?

Sangwhan: right after the first sentence would be "this only applies given that web assembly promise is not implemented" 

Dan: with a link to the evidence that it's being worked on. We should file an issue to ousrelves to rewrite that text to say don't sync any more there's no reason to sync.

Sangwhan: **to do PR**



### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)

Dan: So we have discussions https://github.com/w3ctag/design-principles/discussions but we haven't advertised...

Sangwhan: why not defer this to the w3c community slack - there is a TAG channel there?

Dan: I would be fine but not at a stable URL...

Sangwhan: it's a matter of do we have time to look at this...  we need more than 1 person...

Dan: I will take an action to see if we can addo some automation to notify us when new discussions topics / questions are posted... let's keep it where it is for now... 

Sangwhan: I know there's a need...

### [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378)

Sangwhan: Dominic wrote a good summary...

Dan: dominic suggested adding it to https://w3ctag.github.io/design-principles/#constructors - do we agree?

Sangwhan: I agree. It's patterns on creating objects...  We say you shouldn't use factories in 

Dan: we say a lot about factories but...

Sangwhan: no guidance on when to use one or the other...

Sangwhan: patterns when this makes sense... we could say "sometimes it makes sense to use a factory"

Dan: we already say [some things about this].. is there really more we need to add here? Looking at text in 6.7. Are we adding value by adding more complexity to this?

Sangwhan: write ...use this naming pattern, don't use this naming pattern, would make this easier to address. I'll take a look.

Dan: continue discussion in the issue

### [Meta: How do we work with other WGs?](https://github.com/w3ctag/design-principles/issues/387)

Dan: specifically about CSS, more of a plenary thing. What happened? An issue opened in CSS that hasn't had a response.

**agree to wait for feedback from CSS group**

### [Request for design principle clarification: Warn explicitly against getters throwing exceptions](https://github.com/w3ctag/design-principles/issues/400)

Dan: is this a js best practice, or something for specs?

Sangwhan: probably an antipattern we should point out

Dan: are there specific apis that have done this the wrong way? Can we challenge Matt [issue opener] to write us a PR? Where do we think this would go in the principles doc?

Sangwhan: 6.3 [will respond]

## Plenary Session

Present: Dan, Peter, Amy, Tess, Yves

Regrets: Rossen, Lea, 


### Breakout Rollup

#### Breakout A

Peter: dictionaries and default values.. talk about more in plenary

#### Breakout C

Sangwhan will write things.

Meta discussions - using gh discussions?

CSS best practices - ball in CSS WG court, they have an issue.

Peter: there was a discussion of that in today's meeting. Issue was following the i18n wg's model - file css design principles in our repo but have issues in the css repo to track them so the css wg can be aware and give their input. And discussion of spinning up a task force. 

Amy: CSS WG don't want to own their own document?

Peter: no discussion of that, happy contributing to ours. More discussion at some point.

### [New principle: Guidance on options disctionaries and default values](https://github.com/w3ctag/design-principles/issues/391)

Dan: Lea left a comment, agreeing with Anne. Let's take to slack.

### Issue Triage
