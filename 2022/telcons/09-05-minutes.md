# TAG Teleconference
#### 05-07 September 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-09-05](https://www.timeanddate.com/worldclock/converter.html?iso=20220905T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov
* [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober, @alice
* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov
* [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)
* [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

### Breakout C (APAC / Europe) - [2022-09-06](https://www.timeanddate.com/worldclock/converter.html?iso=20220906T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman
* [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo
* [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion
* [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
* [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
* [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou
* [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369) - @torgo

### Plenary Session - [2022-09-08](https://www.timeanddate.com/worldclock/converter.html?iso=20220908T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Amy, Lea, Yves

Regrets: Rossen, Tess, Hadley


### ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154) - @hober, @cynthia, @LeaVerou, @atanassov

### [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160) - @hober, @alice

### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou

Lea: appropriate uses for the canvas element.. we could say it's not related to what we do... we could say we have a pricniples for API designers and some apply to both API designers and web developers...  We should have consensus on what our position is.

Dan: I think it's "primary for API developers" but...

Lea: depending on what platform developers think of the canvas element that could influence the web api design... "Principles are only in scope if they affect future decisions about API [web platform?] design."

[discussion on whether there should be an intro with discussion of audience]

Lea: if we have consensus about the audience then someone leave a comment.

### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

### [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342) - @atanassov

### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

Dan: there is feedback from Alice that hasn't been addressed..

### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

Dan: I think this would benefit from having Sangwhan

### [identity on the web](https://github.com/w3ctag/design-principles/pull/396)

Amy: new PR - can get feedback ... Where in the doc should it go?



## Breakout C

Present: Dan, Max, Sangwhan, Amy, Yves

Regrets: Rossen, Tess

### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro, @hadleybeeman

Amy: I have a PR... Interested TAG members should look at it. And then we get a review 

[the PR](https://github.com/w3ctag/design-principles/pull/396)

Dan: lgtm...

Amy: straying from the scope into privacy principles land.. so maybe some of it should come out... tried to keep it architectural

Dan: I was going to say that it should be edited down a bit...

Amy: some feedback from others with that in mind would be helpful. What can be removed that is out of scope for design principles? (focusing on architectural principles)

[discussion about what in the bulleted list might be edited out]

Amy: portability is arguably an architectural principle... hesitate with blanked guidence becuase of cans of worms

Dan: what is architectural?

Amy: input from Lea and Sangwhan as people with their heads in what belongs in Design Principles and what doesn't would be helpful. Will ping on slack.

### [Avoid nondeterministic behavior](https://github.com/w3ctag/design-principles/issues/3) - @torgo

Amy: some examples from a million years ago... could be a small short thing... but has been labeled as "big"... we could close and see if it comes up again... Is it so basic that we don't need to close it?

Dan: is it high priority based on what api desginers are doing right now?  Has it come up in design reviews?

### [Avoid exotic objects (e.g. named/indexed getters/setters)](https://github.com/w3ctag/design-principles/issues/16) - @hober, @maxpassion

Max: I can read the discussion and come up with a proposal...

Sangwhan: the tricky part is getting to "tl;dr"... 

### [Discourage overloading](https://github.com/w3ctag/design-principles/issues/131) - @LeaVerou

### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

### [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris

### [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou

### [HTML: Receive data via attributes or JS?](https://github.com/w3ctag/design-principles/issues/348) - @LeaVerou

### [What should be the principles be about appropriate use cases for the canvas element?](https://github.com/w3ctag/design-principles/issues/369) - @torgo

### [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)

Sangwhan: another styleguide violation.... - and Lea also needs to weigh in on this.

Dan: doesn't start with actionable advice... 

Lea: suffers from a lot of the same problems as #290.  

Dan: [left a comment](https://github.com/w3ctag/design-principles/pull/354/files#r963434020)

Lea: usually API designers are also implementers... this is already a concern for them... should be there for completeness.. 

Dan: I think it's something that some people don't think about..

Lea: have we had any cases where people didn't take this into account? In most discussions I've been in the problem is the opposite - implementers pushing against changes in case they break an old website. Recent example - color interpolation in CSS. Pushback because what if websites depend on the broken behaviour? Should we be able to change colour contrast to something better in the future?

Dan: let's discuss async

### Miniapp

Max: we need to check status on the feedback document... they are having a meeting this week.

Amy: we need to assign someone...

Max: it may be helpful to provide additional guidence to authors

Dan: agree. We could start it now.


## Plenary Session

Present: Peter, Dan, Max, Amy,  Yves, 

Regrets: 

### Breakout Rollup

#### Breakout A

#### Breakout C

Dan: We have been working on a miniapp feedback doc... Will continue working on it today. Identity on the web principle is ongoing. Non-deterministic behaviour is proposed closed. Okay to close?

Peter: I don't think it's a burning issue, but it's a valid point. But if it's been open for 8 years and no-one has written anything it's probably not going to get written.

Dan: I feel its meaningless to have these open issues that are not getting prioritised. I think Lea made this point - has it come up in any of our design reviews? if not, maybe it's not something.. we're not seeking for principles to be completist.

Peter: fine by me

Dan: ]closes]. On avoid exotic objects, Max is going to work on something. We looked at backwards compat principle, landed proposed changes, but Lea asked if it's useful, have we had cases where people didn't take this into account? Is this something we want to land?

Peter: Lea brings up a valid point - do people actually break backwards compat? Has this come up in issues? One of the things we talk about are proprietary features. On one hand it seems like market forces will keep backwards compat except where there's a good reason not to. Good question to ask if we really need this?

Dan: can continue on slack. Going to interoperability vs implementability PR.. No resposne from Alice or Anne.

### TPAC Week Planning

Dan: what are we going to do next week?

Peter: afaik Tess and Rossen and Yves are going to be there

Dan: Yves, have you had any response about lightning talk about ethics?

Yves: not yet. I'll try to prepare something

[discussion of meeting formats]

### Issue Triage
