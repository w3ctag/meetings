# TAG Teleconference
#### 21-23 October 2024

---

## Agenda:

### Breakout A (California / Europe)  - [2024-10-21](https://www.timeanddate.com/worldclock/converter.html?iso=20241021T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @plinss

* [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou
* [Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @hober, @LeaVerou
* [[HTML] Canvas place element](https://github.com/w3ctag/design-reviews/issues/997) - @hober, @matatk
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

### Breakout B (California / Australia) - [2024-10-22](https://www.timeanddate.com/worldclock/converter.html?iso=20241022T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk
* [Early design review: Future browsing context group dependency hint](https://github.com/w3ctag/design-reviews/issues/979) - @hober, @martinthomson
* [Multiple import maps](https://github.com/w3ctag/design-reviews/issues/980) - @jyasskin, @LeaVerou
* [FYI Private State Token API Permissions Policy Default Allowlist Wildcard](https://github.com/w3ctag/design-reviews/issues/990) - @martinthomson, @jyasskin

### Breakout C (Europe / China) - [2024-10-23](https://www.timeanddate.com/worldclock/converter.html?iso=20241023T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk
* [Review for CR transition of WebAssembly specifications for version 2.0 features ](https://github.com/w3ctag/design-reviews/issues/1002) - @torgo, @matatk

### Plenary Session - [2024-10-23](https://www.timeanddate.com/worldclock/converter.html?iso=20241023T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* [Election Transparency](https://github.com/w3c/AB-memberonly/issues/240)
* ["With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76)

-----


## Breakout A

Present: Jeffrey, Dan, Matthew, Tess, Tristan, Peter, Lea
Guests: Noam Rosenthal (google), Vladimir Levin (google)

Regrets:

### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @plinss

[with special guests]

Peter: view transition classes... some disconnect... mechanism for adding classes... seems to be recreating what selectors is doing...  Taking a view transition and binding it to an element... that's what selectors do... So I don't see the point of it...

Vladimir: our model is not so much that it binds ... but uses element info to create a new pseudo tree... configures the pseudo-tree to act like... Regular slectors would targer the dom... 

Peter: I don't quite fully get the point of the pseudo-elemnt tree... fundamentally the notion is ... 

Noam: the whole concept of view transitions is .. when the transition happens, the dom that generated it is no longer applied... it creates a snapshot... all those things can be changed... the only thing that's left is the transition itself .. it's outside - a child of HTML - the only thing that exists there is pseudo-elements and their names...  Separating it from topology of the dom allows for flexibility... Dom is rigid... One of the problems we have is .. when using unique name for everything you have to do a lot of repetition... Every element that is being animated you need to give it a unique name. So we wanted to style many at a time.

Peter: similar things like grid lines... why do the names for view transition elements need to be unique?

Noam: this was an alternative that was discussed...  It was copied from known idiom from the web... also the unque name is how to grab ele,ment

Vladimir: the uniqueness point - it maps one element on the old dom state to an element in the new dom state... so it can't be reused - it's an ID in the page.

Noam: I see how it creates a weird thing... it's an underworld that copies the real world ... I see it as a feature...

Peter: to me - the problem is that re-using the concept of classes... it generates confusion for authors... sort of like classes, but not classes, but uses the class syntax... 

Dan: *developer complexity blah blah*

Jeffrey: I wonder if the thing to do here is to ask the CSS wg to look at this issue again... and schedule some time where Peter and Martin could come to ... and discuss further...?

Peter: certainly a possibility...

Matthew: i can understand the desire ... I'm wondering: when the name viewtransitionclasses was developed were there alternative proposals?

Noam: yes - this duplicates the discussion in the CSS wg... all of this is in the minutes... hesitant to repeat without new information?

*noam to send link to this minutes*

Noam: a few names were suggested ... [this was all discussed in CSS]...  I think it's 90% like classes... regular dom tree provides the names and classes... regular css tree provides names and classes for view transition tree. something less complex about this then inventing new names... 

*Matthew: I think this was the link given re the prior discussion: <https://github.com/w3c/csswg-drafts/issues/8319>*

Vladimir: ... there is a desire to target "not one but not everything" - which is the function classes play in regular HTML... which is why we ...

Lea: *also querying about selectors*

Lea: there's 2 states - what's there when you start and when they finish ... couldn't you set a class on an ancestor?

Noam: with cross-page the new stare is what decides on things...

Lea: ... you could do the same thing with selectors... 

*more discussion on selectors*

Lea: the pseudo-element is on something... 

Vladimir: not clear to me what the proposal to target multiple...

Noam: you could implement a subset of this feature with [hostcontext]? You would probably be able to have some aspects of the feature but not everything - you'd lose exit transitions...

Lea: targeting elements based on a property ... has come up multiple times .. perhaps there is something that can benefit all of CSS ... concerned about introducing something that's different to other ways CSS works...

Vladimir: this property effects how pseudotrees are constructed...

Lea: looking at these code examples, I'm worried about the DX... everything under a selector would have a certain view transition class.. 

Vladimir: on the exit transitions it would need to preserve that topology... we are currently just naming it... whatever it was, give it a name... what you're proposing you would need to remember ...

Jeffrey: so where do we go from here... CSS wg would need to agree.. seems like we should be trying to continue... 

Noam: there has to be a counter proposal to CSS to bring it up in the wg again... or an enhancement... 

Lea: if something like this design goes forward could we make it less like class... to make it clear this is a custom thing... similar to animations, font palette..  Similarly if the naming cannot used class ... that might be more consistent.. 

Peter: Lea mentioned .. the problem here is that classes themselves are assigned by selectors... when old DOM goes away you have to have memorized those classes.. if you're doing that why can't you just have used regular selectors to target the transitions and then captured that at the same time?

Vladimir: the answer is... what you're proposing is - at the time of targeting, remember a particular selector... not clear what the selector is ... right now our answer is "give that whole thing a name"... 

Lea: you could argue that the selector matches the end state... but sometimes needs to match the begin state. CSS is a reactive language. This introduces an ordering effect... 

Vladimir: in terms of reopening ... right now the state of the world is that as far as CSS wg is concerned this is added... so to re-litigate it would need to be opened as an issue?

Peter: i'm not opposed... I think where it landed is not idea... i think it creates developer confusion... i think it would be good to see if there is a better answer. Allowing multiple names; capturing information; etc... also I accept there's something I don't fully grok.  We should push back from the TAG to the CSS wg on developer confusion issue...

### [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou

*we discuss draft comment from Jeffrey*

*we agree to post*

Posted to https://github.com/w3ctag/design-reviews/issues/994#issuecomment-2427287323.


### [Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @hober, @LeaVerou

Lea: why would style be written ... also the fact that we're recreating filenames that don't exist

... feels like this solving problems ... inventing API surface to solve a problem that could be solved by saying "they should not trigger additional network requests"

Tess: It is a big pile of stuff... but the number of cases they are trying to cover is big enough that it might be justified... similar reaction... some of the naming hoops I need to jump through... attribute names ... get unwieldy really quickly...   Given the constraints I think they ended up somewhere reasonable. I wonder how it works for closed shadow roots? The whole big debate of "what the default mode" - wasn't resolved... but de dactor there has been an assumption of "open"...

Lea: 2 problems this is trying to solve - sharing styles between components or between host page and components... if you use existing mechanisms, it triggers additional network requests...

Tess: i think the problem is encapsulation...

Lea: they are saying it's a problem... javascript actually defines when you import a ESM across multiple modules it's not requested multiple times. why not just define that that is how CSS works?  2nd thing tis is trying to do: importing parts of a style sheet... why not having a mechanism that allows for this using existing mechanisms?  Feels non-ideal and introduces new API surface? ... fixing the problem outside of web components... there have been a lot of opponents to web components based on complexity...

Jeffrey: they're argument about the @sheet alternative considered is "not implemented" which isn't great... 

Peter: i'm also curious about "may cause network requests" - i've implemented code to not load style sheets multiple times... what are the conditions that WOULD coause a network request? 

Lea: seems like this could be specified...

Tess: it's a question of data .. does the web ...

Peter: behaviour that is 20+ years old to not do extra requests... maybe if there is a clearly defined condition...?

Tess: asking for data to back up their assertions...

Jeffrey: maybe @sheet and then a link rel pointing at that named sheet .. would be a better way to do this if it's web compatible...

Peter: yeah

Lea: yeah

Fodder:
> We're concerned about the developer complexity ... Do you have data to back up the assertions you're making?  Compat analysis

*we will draft a comment and discuss further before leaving it*

*discussion of whether this is a chrome bug or a general issue*

Lea drafted a comment here: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/65#issuecomment-2427387664

### [[HTML] Canvas place element](https://github.com/w3ctag/design-reviews/issues/997) - @hober, @matatk

*we discuss and agree Matthew's comment*

Tess: I think this has been tried before.... in ancient whatwg mailing list issues...

*[Matthew posted a comment, including a couple of edits suggested by Jeffrey](https://github.com/w3ctag/design-reviews/issues/997#issuecomment-2427376698)*


## Breakout B

Present: Martin, Jeffrey, Peter,  

Regrets:


### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Not enough information and not the right people.

### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

Ditto

### [Early design review: Future browsing context group dependency hint](https://github.com/w3ctag/design-reviews/issues/979) - @hober, @martinthomson

Martin: Mozilla folk's conclusion is that the target= thing is a bug. Browser context group switches should not be visible to content, so if content gives a window a name, and you switch back, and the name is still used in the back-forward cache, then it's a bug. Mozilla will fix the bug: if someone opens a named window, that invalidates the back/forward cache. Apple doesn't switch browser context groups, so they can keep that. 

Jeffrey: So if Chrome has data showing it's important to keep the bf cache, Mozilla might reconsider.

Martin: Yes, but that probably won't happen.


`unsatisfied`:

<blockquote>
  
We discussed this in a breakout and with some Mozilla engineers, and we think it's probably best to drop the bf-cache optimization in the case that's driving the proposal here. If Chrome has data showing that it's important to keep the optimization in this case, we're open to reconsidering.

</blockquote>

### [Multiple import maps](https://github.com/w3ctag/design-reviews/issues/980) - @jyasskin, @LeaVerou

`satisfied`:
<blockquote>

Thank you for the discussion. We're happy to see this proceed through the HTML review process.
  
</blockquote>

### [FYI Private State Token API Permissions Policy Default Allowlist Wildcard](https://github.com/w3ctag/design-reviews/issues/990) - @martinthomson, @jyasskin


Martin: the race on picking the 2 issuers gets worse with this change, so this would be a good time to insist on finding a better way for the top-level page to pick its issuers.

There is a set of entities that can run script.  That set is probably smaller than the set of entities that might get framed in.  Therefore, this change increases the by-default exposure of a page to entities that might "use up" its limit of 2 token-issuing origins.

Jeffrey: Last week we said we should ask them to get a privacy review.

`satisfied with concerns`:
<blockquote>

We discussed this in a breakout and have a couple concerns:
  
* This change increases the by-default exposure of the page to entities that might "use up" its limit of 2 issuers. You've suggested that the top-level page should call the API to explicitly pick its issuers, before allowing 3p script to run. We're skeptical that that's a practical defense. You're right that it's a pre-existing issue with the API, but because this change makes the risk worse, it would be good to improve the defense before making this change.
  
* We're not the right body to judge whether the privacy implications are reasonable. Could you ask the Privacy WG to review this system?
  
</blockquote>

### Sundry

Discussed voting transparency.



## Breakout C

Present: Dan, Martin, Matthew, Tristan, Max

Regrets:

### Outcomes of A, B

Martin: we skipped 961, 978. We talked future browsing context ... we told them not a great idea and fix the bug.  Told import maps we're happy with it. Private state tokens we said "satisfied with concerns" - they think they can punt on the basis that problem already exists... it's already possible for cross origin content to "steal" the limited number of token issuers ... this is allowing them in iframes... a significant expansion in scope... so we said "it's not enough"... you might say top level site has control over who executes script but not the same for iframes. PiNG to also have look. Re voting transparency - for TAG election.

Dan: feels like we should not change things so close to the election...

Martin: I'd like to change from STV to approval voting... 

### [Accessibility Conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk

Matthew: this is an fpwd of 1.1... changes highlighted from 1.0.  APA is looking at this. from an Architectural perspective I don't think we should be concerned about it. Parts do raise interesting questions... one thing some in the TAG might have experience with. A few small questions that APA will ask for clarifications on.  A number of people from different a11y consultancies and other places - good mix of people involved. I think from a TAG PoV it's good. 

... One thing that is related: got me thinking about - a lot of a11y is subjectine and dependent on context. But some is very mechanical. All of these rules are plain language rules... but e.g. some custom control has been implemented correctly, there are ways to express that .. Could we represent those by patterns?  Just wondering is there anything people have come across that expresses the relationship between DOM structures ... 

Martin: I think **selectors** would do it...   `:has()` is a big change.

Matthew: I think the question is how applicable ... sort of tangential to what ACT is doing...

*Matthew to draft a closing comment and we close by end of week*

### [Review for CR transition of WebAssembly specifications for version 2.0 features](https://github.com/w3ctag/design-reviews/issues/1002) - @torgo, @matatk

Martin: I don't think this is a problem. the reference types explainer has not been updated... maybe the spec is up to date, but the explainer is not ready. there is a naming problem... Otherwise it would be keep up the good work.

Matthew: the repo is officially abandoned... 

Martin: the question is where is the material?

Martin: *writes proposed comment:*

---
Hi @dschuff, we're looking at these and for the most part these seem reasonable, but we noted that the reference types explainer is full of questions and has a big TODO.  Then we realized that most of the explainers are old and no longer being updated.

It seems like the WG work mode involves forking the spec for a feature and then archiving the fork once the changes are merged.  However, this means that the explainers are sometimes not updated to include the sort of stuff the TAG likes to see, little things like user benefit (see [our explainer explainer](https://tag.w3.org/explainers/) for more).  Is there anywhere that we can get up-to-date information in that form?  None of us are particularly expert at reading WASM specs, so it's hard to find these features, let alone find a discussion about benefits and trade-offs.

## Plenary Session

Present: Peter, Matthew, Martin, Jeffrey

Regrets: Dan, Yves


### Breakout Rollup

#### Breakout A

* Adopted stylesheets: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/65#issuecomment-2427692540

[Posted](https://github.com/w3ctag/design-reviews/issues/1000#issuecomment-2433471327)

#### Breakout B

#### Breakout C

#### ["With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76)

Can we make this go away?  https://github.com/w3ctag/design-reviews/issues/76#issuecomment-767710822 proposed closing it 3 years ago.

#### [Election Transparency](https://github.com/w3c/AB-memberonly/issues/240)


### Issue Triage
