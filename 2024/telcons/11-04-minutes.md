# TAG Teleconference
#### 04-06 November 2024

---

## Agenda:

### Breakout A (California / Europe)  - [2024-11-04](https://www.timeanddate.com/worldclock/converter.html?iso=20241104T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)


* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk
* [Review for Protected Audiences Bidding and Auction Services API](https://github.com/w3ctag/design-reviews/issues/1009) - @jyasskin
* [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin
* [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss


### Breakout B (California / Australia) - [2024-11-05](https://www.timeanddate.com/worldclock/converter.html?iso=20241105T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [CSS :open pseudo-class](https://github.com/w3ctag/design-reviews/issues/1010) - @LeaVerou
* [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou
* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

### Breakout C (Europe / China) - [2024-11-06](https://www.timeanddate.com/worldclock/converter.html?iso=20241106T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early review request for "Explicit JavaScript Compile Hints"](https://github.com/w3ctag/design-reviews/issues/947)
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996)

### Plenary Session - [2024-11-06](https://www.timeanddate.com/worldclock/converter.html?iso=20241106T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Matthew, Peter, Jeffrey, Yves, Lea, Tess, Amy

Regrets:

### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

Matthew: a few thoughts... some general issues - and specific a11y discussions. I haven't seen anything in this proposal that's concerning. But a couple of things - reading the spec from the CSS WHATWG side... About reading flow in general ... Specific words & phrases might have an a11y implication - e.g. sequential navigation order is clear, but "speech order" is being referred to in the spec... https://drafts.csswg.org/css-display-4/#order-accessibility CSS WG is capable... But APA and CSS might need to get together to understand these common terms... So no specific concerns about *this* review but I think APA needs to talk to CSS... Action on me. ... when I read the spec it's more focused on the order of interactive elements... could supersede tab index.

Jeffrey: my sense is that this should affect the a11y tree.  No definition of how html turns into an a11y tree...

Matthew: one interesting thing - talks about the difference between source order and display order. If it does effect a11y tree then why not just reorder source?

Tess: The a11y tree comes from the render tree.  But different ATs are different.

*some discussion on this point*

Peter: would be good to have a reference in the CSS spec.

Matthew: also the explainer is in a personal repo.

Jeffrey: Will poke. It should be in "explainers by googlers"...

Matthew: "render to speech" different from the "focus order". 

Jeffrey: it's the wrong term, regardless... Seems like a good issue to file with CSS.

Peter: just go ahead and post your points to the public thread.

### [Review for Protected Audiences Bidding and Auction Services API](https://github.com/w3ctag/design-reviews/issues/1009) - @jyasskin

Jeffrey: I [posted a comment](https://github.com/w3ctag/design-reviews/issues/1009#issuecomment-2453858089)... said "explainer is bad"... It's possible they think they are fixing some of the issues. I think it's in their court.  

*discussion on how we should treat this...*

Peter: let's wait for feedback...

### [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin

Jeffrey: Martin wrote a draft comment... 

Peter: we did discuss at the Seattle f2f...

Yves: we concluded that it was a potentially deceptive pattern - you may feel you have done business with these people...

Jeffrey: the core use case is telling the user that clicking this button will do something for them - prefilling credit card number, for example. 

Peter: how do you enable a feature like that in a way that is not deceptive.

Tess: put the info that is cross-site outside of the viewport.  People don't have a mental model that includes iframes...

Jeffrey: I'll propose some new text...

Dan: would an alert in the browser chrome make sense?

Jeffrey: we can ask the proposers for user research that indicates why there has been a change of behaviour (e.g. increase in "conversion")

### [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss

Jeffrey: I had a useful discussion with them this morning... About idea... The objection that it's more typing for authors came up.... 

Lea: is the idea that open and close would still exist?  or phase it out?  

Jeffrey: for elements that already have open/close it would stick around but for new things it would be *toggle*.  New state.

Lea: I like this.

Tess: this feels like one of those cases where we are chasing API design fads... Ideally the web's API surface moves more slowly than trends in JavaScript libraries?  When we hadd things to the web platform that doesn't look like the web but looks like popular JS libraries, then I would like to see some justification for that... There's no such things as adding web features in a vaccuum.  My knee-jerk worry.

Jeffrey: It looks like the precedent that Domenic was following was the *details* element which has toggle....

Lea: besides what Jeffrey mentioned about *details* it seems that on the web platform we use a single event for state changes... So that seems to be on par... More than an open and close event...

Yves: as we already have open/close it's easy to have another state. In the case of a toggle it might be more difficult... Especially if you have 2 ways of doing the same thing... something about not doing the same thing 2 different ways in the design principles?  There might be dragons.

Dan: https://www.w3.org/TR/design-principles/#consistency ?

*discussion on toggle vs state change?*

Peter: like a light switch - 2 positions.

Lea: state change is way to generic.

Jeffrey: things are open and closed - not much prospect to add another state...  Following precednet - they were right to extend toggle to dialog.

Lea: What about popover?

Peter: uses toggle.

Jeffrey: the event is called toggle but the actions are show and hide.

Peter: having open / close events would be more consistent with CSS... Checkboxes... that pattern comes from other input elements that definitely have more than 2 states.  In my mind having open/close event feels more proper.  Having them as separate event handlers might be more convenient. Consistency is my main concern. Popover is the odd one out... Not sure that's the pattern to follow.  At least "pick a lane and stick to it."  

Jeffrey: *writes proposal comment*

Dan: noting positive review from Mozilla: https://github.com/mozilla/standards-positions/issues/1101

Peter: details has a boolean open attribute... I'd love us to be consistent between CSS, properties, and events... right now it's inconsistent.

Lea: a shared toggle event class?  Then you could also do isevent instance of toggleevent...

Peter: a common base class named toggle is fine but more concerned with the event names...  I think there's value to developers (DX) to get some consistency...  Suggest we leave the comment and not close... but get feedback from the broader community...

`satisfied with concerns`:

<blockquote>

We want to emphasize the goal of [consistency](https://www.w3.org/TR/design-principles/#consistency) across the platform, between CSS properties, attributes, methods, and events. Unfortunately, none of these are consistent. Based on the history of `details` having a `toggle` event and `dialog` only having a `close` event, we think `popover` was correct to use `toggle`, and then this change is correct to extend that to `dialog`. There's an argument that `open`/`close` would be more consistent with the CSS `:open` and `:closed` selectors, but we think it's worth keeping consistency with the events.
  
</blockquote>

Or `unsatisfied`:

<blockquote>

We want to emphasize the goal of [consistency](https://www.w3.org/TR/design-principles/#consistency) across the platform, between CSS properties, attributes, methods, and events. Unfortunately, none of these are consistent. Because the elements have `open` attributes, and CSS added `:open` and `:closed` properties, we think the better path forward would be to use "open" and "close" everywhere, across event names and method names. This implies that it would be ideal to retrofit `open` and `close` events onto `popover` too, and we'll file an issue with HTML to ask to do that.
  
</blockquote>

## Breakout B

Present: Jeffrey, Matthew, Peter, Lea, Tess

Guests: Dan Clark, Alice Boxhall, Westbrook Johnson

Regrets: Martin


### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Peter: People have a bunch of opinions.

Dan: Steve Orvell has summarized the tradeoffs: https://github.com/w3ctag/design-reviews/issues/961#issuecomment-2457667230. Somewhat aesthetic. Main concern is about re-ordering, for example for aria-labelledby. We lose that if we push the information down to elements. I don't have a good sense how much developers would miss this.

Alice: Comes down to ordering. Steve's table was useful, but ordering is the only place where it's not just convenience. TL;DR comment: https://github.com/w3ctag/design-reviews/issues/961#issuecomment-2456465629. When is this actually going to be used in practice? For what attributes? We're designing a general solution without understanding the specific problems it's trying to solve. Looking through the problems in my comment, if we can solve the naming problem, the ordering question doesn't seem to actually mention. There are lots of attributes that do take lists of id references. Do we need to support those use cases?

Lea: One of the considerations to keep in mind is that this is not just about ARIA or labels. It's about anything that takes element references. The list of things like that keeps increasing. popovers, invokerrs, input lists. Anchor attribute. These have very different characteristics w.r.t. which shadow dom element you need to refer to?

Alice: Specific examples?

Lea: Not off the top of my head. Do you ever need a datalist inside a component? Need to think more to find specific examples. 

Dan: I've written tests where you have a popup inside a shadow dom, and want to trigger it from outside. Don't know if people actually want this?

Westbrook: The idea that it's growing, regardless of the use cases, is a reason not to use new attributes. Every time another group wants to add an ID reference, they'll need a reflected attribute. We'd be setting everyone up to fall into gaps. With popover, we know the context, but the next one won't have it. Want to solve the general problem.

Lea: I don't have a strong opinion. Slightly favor attribute approach. I think the id approach is reasonable, and it has many things going for it. Much easier than the general idref problem. In shadow roots, you assign a fair number of IDs anyway. There are arguments for both. If we have an attribute on the shadow root, want to iterate a bit more on the syntax. Also want to make it work with direct element references. Whatever solution should allow web components to extend the set of idref attributes.

Alice: I want to understand the specific problems we're trying to solve. Think if you scope the problem to just referenceTarget (after bikeshedding), a lot of the distinctions between the two syntaxes disappear, because you lose the ordering problem. Really depends on whether we can justify not doing any kind of mapping.

Dan: I have that feedback. "Please solve the basic referenceTarget problem; dont' get delayed by the mapping problem."

Alice: Would be really nice to know what the more problems are.

Dan: Want to do an origin trial of the basic referenceTarget case. Haven't implemented referenceTargetMap yet. One option is to move forward with that, and we can prod the partners to ask if they'd be happier with the attribute on the elements. You get better responses if people can ship this in production.

Alice: Element references: I think that's explicitly scoped out, having an element reference version of referenceTarget. Not sure if the explainer says anything about an  element reference from shadow dom pointing [?] For activedescendant, you have to change things all the time, so an element reference might be nice to have. Solve the basic "there's an input inside the root that needs to substitute for the root". activedescendant is important, but it's niche. I liked Jeffrey's suggestion to let aria-labeledby work when it's on a shadow root. The problem with daisy-chaining might be that you want an input to have a value, but the value becomes part of the label. And the input has its own label, but you want its value to act as the label for something else.

Jeffrey: And that problem doesn't happen if you only allow labeledby to recurse only when it's set on the shadow root.

Peter: Main concern is the mechanics of using IDs to reference everything. When you're dynamically generating component content, assigning IDs is hard. ARIA requires IDs for almost everything. Want to see a path to fix that. Try to reverse the relationship and let the browser help out. Want to improve the DX.

Lea: +1 to Peter. IDs are painful, but this might not be the place to solve it. I wrote an essay about this. But wouldn't want to block referenceTarget on this. What if we don't do either. Specify stuff on shadow root. Instead of just specifying IDs, use selectors that are scoped to shadow root.

Westbrook: Interesting to avoid needing IDs, even if it's hard to manage or keep track of them. Web Components community wants to keep ARIA working. But I'm also excited to share thoughts on how we can expand on those relationships in the future. Wouldn't want to invent new selectors to let web components devs catch up to non-components development.

Peter: In general I'm sympathetic. We see proposals that are inconsistent with some othe rthings, but it matches years of precedent. "Chart a new path" makes people boil the ocean. Counterpoint is that we have an established path that we're trying to get away from, and we keep adding to that path, we create more inertia.

Jeffrey: We don't yet have a plan. The plan isn't just "selectors" since we also need to be able to go up the tree. We should make a plan and then we'll need to upgrade the existing aria-* attributes anyway. `referenceTarget` and `referenceTargetMap` (spelled however) will probably be able to upgrade the same way. So I'm leaning toward saying to go ahead with referenceTarget as it's currently designed, with IDs, and then we fix everything at once.

Dan: Use an id on the shadow

Alice: +100 to Jeffrey. When it comes to designing the new system, you need to be able to go up or sideways. Collect specific use cases. It's a different things to get aria-labeledby where maybe you want to reverse a name. You need to think about the cases you need. 1 thing vs multiple things. Collect the cases of the attributes we have currently. As opposed to thinking of them as a general problem.

Lea: I like the idea of "let's solve this problem now, and pave the way for solving the general problem later." What makes that easier? Microsyntax of referenceTargetMap -> separate attributes. Attribute for each mapping. Then the attributes have the same syntax as the bound attirubtes, and upgrading them works the same as upgradinng ARIA.

Jeffrey: Think that came up at TPAC. 

Dan: People were wary of microsyntax at TPAC. (https://github.com/WICG/webcomponents/blob/gh-pages/proposals/reference-target-explainer.md#use-separate-attributes-for-each-forwarded-attribute) Still wanted to put it on the shadow root.

Lea: Pending TAG principle against inventing microsyntaxes. Maybe helps forwarding for certain attributes work before others. Huge disparity. Want to delegate `for` the most. Maybe that could advance independently.

Westbrook: I heard also the feedback on microsyntaxes. Anything specific about the microsyntax that would stop it from working like attributes. [Link](https://github.com/WICG/aom/pull/204/files) about crawling up and down DOM. It was frowned upon by lots of people.

Lea: Not about browser internals. More syntax implies that new syntax is hard to introduce w/o introducing parsing ambiguity. w.r.t. #204, maybe this particular naming scheme isn't the only possible one?

Alice: To clarify one thing about `exportid`: the syntax is noisy, but when you have a substitute element within the shadow root, the syntax was horrible. Every time you want to refer to the real input, you have to use `hostid::realid`. This wasn't meant to stand on its own. It was a stepping stone toward a better coordination thing; would let you prototype.

Jeffrey: I think we've converged on saying "go ahead with referenceTarget, and we'll work on fixing ARIA in parallel."

Peter: Let's just be careful not to paint ourselves into a corner. Don't want to fix all of ARIA before shipping this. But do think about what the future shoul dlook like and avoid preemptin ghtat. Maybe we delay parts of this, but get the most important parts out.

Lea: Re "delegatesReferences" looks good, not a good use of call time to bikeshed, but if we use multiple attributes, we need a short base name plus suffixes. So the base needs to be very short.

Tess: "delegates" might be an ok name since it copies `delegatesFocus`.

Peter: Not a fan of over-abbreviating things. Spell it out. But if it shows up 1000 times in a document, that's bad too. As we think about the future, I'd like to be able to take references to DOM nodes. And have that expressible as attributes, so it can be serialized. But as a developer I don't want to think about all the attributes. Think of DX first.

Matthew: To clarify, my understanding is that phase 1 seems good, but phase 2 we want to keep thinking? 

Peter: And about it being dynamically generated by the browser.

Lea: Ergonomics is important, but since time is finite, let's make things possible now and easy later. e.g. imperative API later. As a data point, don't know if it reflects the broader set of use cases. My engineers said they were happy with just `referenceTarget`.

Alice: That is the most common case. The 2 other cases from my post are real cases. Maybe not having a map, but solutions to specific problems. e.g. computed name and some potential ideas for activedescendent. Maybe those cases can be solved in a better way than a map.

Jeffrey: Who's going to work on fixing ARIA?

Alice: That sounds like something to talk to ARIA about. They have a lot of work.

Lea: I would frame it as fixing IDREFs, rather than fixing ARIA.

Peter: Browser vendors care more now, so maybe we can get things that we couldn't have gotten 10 years ago. Would like someone to step up and go think about these things. We shouldn't say "someone should fix things" without following it up.

Jeffrey: Task force? We need to identify a person who will lead the taskforce, and they can recruit people from the right communities. But nothing happens without that leader, and we need to avoid blocking things if we can't volunteer someone to run the task force.

Peter: AI for the TAG.

Dan: We'll go ahead with the origin trial. I'll ask about better names, if they prefer putting it on an element, what other use cases this doesn't cover.

Lea: Westbrook's explainer document has some use cases.

Westbrook: It almost always goes back to the combobox pattern. We have to write web components the hard way, so we don't even run into this wall. Not sure an OT will be enough to get us to the use cases we want to see. As soon as production systems can use this, we'll find use cases.

Dan: Very interested in the ID problem. Reluctant to sign up to drive it today, but want to think about driving it.

Task force members but not leaders: Dan Clark + Alice + Matthew


### [CSS :open pseudo-class](https://github.com/w3ctag/design-reviews/issues/1010) - @LeaVerou

### [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou

Jeffrey: [sketches explainer update]. My sense is to say to keep trying to find a clearer name, but otherwise that this looks good.

Jeffrey to draft a closing comment.

### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Jeffrey: I think this is probably ready to close as either satisfied or satisfied-with-concerns, but it's assigned to Martin so should probably wait until he's back.

Peter: Assigning it to the Nov 18 milestone.

Matthew: I'll also reply to the accessibility question.


## Breakout C

Present:

Regrets: Martin, Dan, Matthew


### [Early review request for "Explicit JavaScript Compile Hints"](https://github.com/w3ctag/design-reviews/issues/947)

### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

### [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996)


## Plenary Session

Present: Peter, Jeffrey, Matthew, Tess, Amy,

Regrets: Martin, Dan, Tristan


### [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin

Jeffrey: close to closing, comments from me and Martin

Tess: wasn't super enthused about the start of your comment. What is the use case we agree with? Having pay buttons on the web at all?

Jeffrey: the idea that having a pay button that you click on then there's no information to help you with paying is a bad experience

Tess: right now you get to a checkout page and there's paypal and apple pay and google pay etc and you click on one of the buttons. And it works or doesn't.  The use case they're trying to solve specifically is I don't remember offhand as a user if I provisioned a card yet in apple pay and the button on the page doesn't suggest to me whether I have or not so I don't know if clicking on that button will be faster or slower than filling out the form myself

Jeffrey: you click apple pay, it didn't work, you click paypal, that's another part. It didn't tell you you should use paypal not apple pay

Tess: it couldn't have known that beforehand. I'm wary of describing the use case of anything vaguer than trying to make that button look like you've already configured google pay so you can trust that you can be faster to click on it than not. That's the actual use case. We already have payment request. It has to be more specific than an api that already exists.

Jeffrey: Right. That was meant as context for the rest. Shortening that makes sense. My goal is to identiy a reasonable use case.

Tess: i suspect I could get behind some description of the use case

Matthew: I've read both comments, Jeffrey's is more dispassionate. It can't be misinterpreted as us saying they're bad. The bit I had most concern with was the very start in much the same way. The approach is constructive. We talked about how much work we want to give them. Not sure we have consensus on the use case.

Jeffrey: happy to redraft first paragraph

Matthew: the fedid people want to pull login providers out of the webpage and into the browser. Is this a stepping stone to that?

Jeffrey: the way fedcm works in chrome is it sticks this sort of information inside of the content area in a way that we should dislike. The shape of the api would allow a browser to pull it out of the content area, but the implementation hasn't done that. We should say something about fedcm, connected to this issue. But it's also separate, it's a UI choice chrome has made not required by the api shape.

Peter: if the use case is knowing you've provisioned google pay or apple pay, isn't that provided by th epayment request api?

Tess: there's a query method to ask if a payment method is supported. That will not say is a card provisioned at apple pay or not. Don't think there's api to tell you there's a card provisioned. Fingerprinting risk.

Peter: is there a way to provide functionality to the user without exposing it to the webpage

Tess: payment request.. you get the UI.. at that point when you see that screen you'll know if you've provisioned a card or not, because it'll be filled out or it won't. They're trying to shortcut that.

Peter: have you already selected the payment provider at that point?

Tess: depends on the browser. In Safari Apple Pay is the only payment provider supported. In a browser that supports others you'd have to have a way of selecting them.

Peter: presuming there's multiple if the browser is going to present the ui to choose the payment method, the browser can tell the user which is provisioned..

Tess: depends on the relationship between the browser and the payment method and the apis available, it might not have any way of knowing

Jeffrey: Shopify wants this and are not a payment provider

Peter: in general we tend to recommend instead of a broad api that exposes user information in js, just use this platform api and let the browser handle all of it. I'd like to have that response here. Just use payment request api, solve them in payment request. If there's a problem why you can't use payment request, let's fix payment request

Jeffrey: that has not been convincing to the payment providers. My impression is they don't want to outsource their UI to the browsers. When we force them to they have specific requests about what exactly the UI should look like becuase of their legal teams.

Peter: this is the payment providers

Jeffrey: Stripe and friends

Peter: that would be handling the transiaction.. are not wanting to work with the browsers?

Jeffrey: they did work with us in the context of the webauthn integration. They had to. They insisted in precise language in the opt outs inside the browser UI. That was for one piece of their authn flow. Getting the entire payment flow into the browser will be even more of that.

Peter: disappointing but understandable. That would be the better direction, rather than opening up other weird escape hatches.

Jeffrey: we are suggesting this might be attainable by sticking some UI into the browser chrome rather than the page. Of course it's a security problem if the page controls what's in the browser chrome

Peter: not the content, but the page can influence what gets to show up by opting into different providers 

Jeffrey: folks also wondered if the actual attack we're worried about is reasonable for payment. If we stick the credit card number in the page is that likely to trick users into thinking the've given the page their credit card number already and will that change their behaviour?

Tess: we know it does because they're justifying this api on that basis

Jeffrey: but is it because it's tricking the user? they can do research to answer that and they should. Not obvious which way it comes out.

Peter: even if you say overwhelmingly it's just a confidence thing, there will be some people who think they've been there before and it's saved their card

Jeffrey: what fraction of tricked users is acceptable

### [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss

Jeffrey: two comments to choose from..

Matthew: both about consistency

Peter: two different things to be consistent with

Amy: what if we gave them both paths to consistency and handed the decision back

Peter: ask for a broader conversation among stakeholders

Jeffrey: they're likely to pick the one they've already gone with. We're only going to get a change for using open and close if we really push for it

Peter: push harder on the fact that we have established precedent with the open pseudoclass and property and that wasn't taken into consideration properly in the past and should be rethought

Matthew: any explainer about where they considered the alternatives and discussed it

Jeffrey: it's in the issue discussion: https://github.com/openui/open-ui/issues/607#issuecomment-1309330785.

Matthew: also discussion about how things might expand in future.. open and close might be all we need. Is there another aspect for which we could say this is likely to be better.

Peter: I can redraft to blend them

Jeffrey: the :`open` pseudoclass is newer than all of this. CSS can't do toggle there, they have to do open and close.

Peter: a resting state, not a transition.


New draft for the second option, from Slack:

<blockquote>
  
We want to emphasize the goal of [consistency](https://www.w3.org/TR/design-principles/#consistency) across the platform, between CSS properties, HTML attributes, and JS methods and events. Unfortunately, none of these are consistent in the current platform, so this change needs to instead chart a plausibly-consistent path forward.
  
Because `<details>` and `<dialog>` have `open` attributes, CSS added `:open` and `:closed` properties, and the event handlers seem likely to be more different than similar, we're inclined to think that the better path forward is to use "open" and "close" everywhere. That implies that it would be best for popover to also migrate from show/hide to open/close. (It doesn't imply that we should try to get rid of the various `toggle*()` methods.) We recognize that retrofitting new names onto shipped features is a big project, so it would be acceptable to just apply this pattern in the future, but if the community generally approves of this path, we'll file issues in HTML to suggest the retrofit.
  
</blockquote>

### [Spec review for Animation.progress](https://github.com/w3ctag/design-reviews/issues/994) - @jyasskin, @LeaVerou


### Breakout Rollup

#### Breakout A
  
See above

#### Breakout B

Peter: Long conversation about reference target

Matthew: kind of resolved. Should we close it? or are they going to do a separate one for phase two?
  
Peter: we may be able to close this. We have the action of trying to create a task force or something

Matthew: really interesting problem
  
Peter: we're better off to start with a mental model of an object model of the DOM and relationships. Imperiative apis create those relationships directly, and use the attributes to serialise those reslationships. Now we're using attributes to define those relationships. That's the main disconnect.
  
Jeffrey: interesting trying to serialize those paths into attributes. we don't want to embed xpath. 
  
Peter: Serialization could get interesting and could be impossible in some cases. BUt it's the model, the starting point. Define the relationships in terms o fthe object model and create apis around the object model and figure out how to serialize them into attributes.

Jeffrey: there's a bunch to talk about in the closing comment
  
Matthew: how far do we want to go into the discussion? I'd be confident to say phase 1 go for it
  
Peter: dont' think we need to restate everything we talked about in the meeting. More just summarising the conclusions. Go for the initial phase, we're going to look at improving ways of defining relationships, keep that broad and vague.
  
Matthew: do we really have critical mass for a task force?
  
Peter: don't know. Consensus to try.
  
Matthew: do you think they've seen the gaps issue Lea and Jeffrey filed?
  
Jeffrey: worth mentioning it
  
#### Breakout C

### Issue Triage
