# TAG Teleconference
#### 22-24 August 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-08-22](https://www.timeanddate.com/worldclock/converter.html?iso=20220822T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
* [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss
* [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

#### Second Half - With Guests

* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss


### Breakout C (APAC / Europe) - [2022-08-23](https://www.timeanddate.com/worldclock/converter.html?iso=20220823T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo
* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion


### Plenary Session - [2022-08-25](https://www.timeanddate.com/worldclock/converter.html?iso=20220825T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Amy, Rossen, Yves,

Regrets: Lea, Hadley, Tess

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Peter: marked pending feedback - we got some... 

Rossen: says "we'll work on it, thanks for the ping"... i think it's safe to push it back ...

Peter: *bumps*

### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss

Dan: we've had feedback - added material around a11y in explainer. This is in response to Lea's feedback and could be addressed. Lea should review.

Dan: [their PR 550](https://github.com/openui/open-ui/pull/550)



### [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov

Amy: reading through conversation that's happebed.. 

Dan: there was discussion of the frame-like things.. Dominic answered the question in June about work going on on this.. their issue 6315.. doesn't necessarily.. 

Rossen: one question Peter asked was answered.. you would know whether you're being fenced ...  Having ads that are running inside of a fence vs non-fenced frame I can see them behave differently. Would that matter?

Dan: comes back to the question of what will motivate developers to move to fenced frames instead. I think the answer is they will be compelled to 

Amy: there will be functionality they will need that will go away with deprecation of 3rd party cookies... but share concern about what an ad will do if it knows it's in a fenced frame. but if we assume 3rd party cookies are gone then there's nothing they can do that would be harmful because theu wouldn't have acces... but in the period of transition time it could be an issue with ads taking the opportunity to collect extra data from cookies when they know they are embedded by a publisher using a fenced frame... but that might be out of scope...

Peter: is it similar to the COEP thing where ads can tell if they're *not* in a fenced frame...

Amy: that would depend on presence of 3rd party cookies...

Amy: .. use cases other than ads ..

Rossen: shopify and other shopping scenarios .. could be a decent use case. 

Amy: also some feedback from Lukasz - wasn't well responded to - he suggested removing access to a clock - they said they considered it but won't do that... but I also think they're discussing in the group. Something to keep an eye on.

Dan: multi-stakeholder issue in that there is none.

Peter: main concern in the past was additional side channels between document and fenced frame. 

Amy: close with concerns - slightly suspicious concerns - would like to understand better in future, in the context of when 3rd party cookies go away or other things in privacy sandbox.  But satisfied with direction of travel.

Peter: makes sense to me. Corresponds with previous discussion. It's a good thing but worried about other privacy sandbox things that open up side channels.  This by itself is OK.  Maybe closing satisfied with concerns makes sense here and keep track of other things?

Rossen: *nods sagely while petting dog*

Amy: [will write comment]

### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

Rossen: third attempt at a TAG review..

Dan: [bump to plenary]

Rossen: explainer is nice and exhaustive

Dan: what do they mean by having a [2] but nothing that it's referencing.. in s&p.. 

### [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss

### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

## Second Half - With Guests

### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

Guests joining: Tab, David Baron, Miriam

Peter: our biggest concern was the fact that this was dealing with state - and managing state somewhere other than the DOM itself... how does that fit?

Tab: it is stored int he Dom - there is a DOM interface...  I assume you mean about preserved...

Peter: when I say stored in the DOM i mean serialized .. preserved... loaded back in.  If I'm in a web app that is in an inetresting state and I send the link to you then you won't see the same state because it's not recoverable ...

Tab: yes - that's true but also the current state of thing. so this doesn't change anything... 

Peter: wasn't a criticism but - exposes a hole in web arch - creates another way for authors to use this - could there be a better way to manage this?  Not necisarilly putting this all on you but...

Tab: we haven't thought about it because this isn't a new problem.... this seems like a pretty big project - and fully seperable from this in concept...

Peter: don't think it has to be solved as part of this issue - but the more we expose this to developers the more it will become a problem... may be something that needs to be solved in parallel with this...  that we have a strong arch model ... that this isn't doing something new and weird...

Tab: my initial thoughts are : this shouldn't be doing anything that makes that harder... the fact that this is the case... suggests that something as relatively simple as .. toggles .. falls into the same realm of stuff..

Lea: assuming someone does want to serialize the state somehow - can you do that?  I see there's a toggle pseudoclass but that's for matching.

Tab: walk the DOM... Everyonce in a while if you need to know that then it's not a bad solution but it could be exposed [in a better way]... 

David: one other related question we've had discusion of - how does this relate to session history... do we want toggle state to be restored in session history? i think the answer is "yes". 2nd question: can the APIs involved in Toggles be connected to a push state mechanism.

Tab: yes... I think.  There's an issue open on this.  Similarly being able to opt into session history.. things that would be a good idea.  It's purely stylistic.. 

David: I'd add that if we add a mechanism to some push state mechanism then we might want to do the same for form controls.

Tab: Yes. that would be connected to auto-serializing it into the URL? 

David: not fully thought out... i'm envisioning something that would allow you to save and restore state to some kind of thing in a fragment identifier...  Some question as to how much belongs in the implementation.

Tab: i think the serialization issue could benefit from iteration in libraries first.  See what feels right - produces URLs that people want to share that are meaninfgully deserializable back into application state... Even ignoring that the session history issue I am inetrest in... remember some info that it would be complicated from an implementer PoV. 

Peter: do we know of anyone actively working in this space?

Tab: we have implementers with experience in this area - can ask Chris H.... 

Peter: is there any work going on in w3c ...?

Tab: to my knowledge, no... some text in HTML but not very prescriptive. 

Tab: can you elaborate on ..... document..

Peter: come up several times in other reviews - multiple things that act on state - coming up with this idea of document state vs. presentaitonal state. Nothing written down anywhere. If you copy a doc and paste it soemwhere else what goes with that?

Tab: Yes currently an inconsistent ... that said, toggles have this property that you can restore a toggle state using style properties.. even if you can't manipulate... you can go through an element with a toggle, serialize and emit that as an element .. that will result in the same toggles/states.  Some manual work. I don't think we want to autoreflect ... but make it easy as possible to do this seralization.. I will record it as an issue and record it in the document that it's an explicit goals.

Peter: bigger picture - beyond toggles there's state reflect back that probably shouldn' tbe... as the TAG our concern is that there's a hole int he architecture here... before we add yet another type of state... maybe important that someone does this work ... rather than building something else that's bolted onto the side... Not putting the onus on boiling the ocean ... but this work shoul be done somewhere...

Lea: relevant to that - any plans to explain via toggles other things like checkboxes?

Tab: it's not as an explict goals because the legacy requirements of existing form controls... maybe not worthwhile.. but at the least making things parallel would be good.

Rossen & Lea: observability & accessibility ARIA roles?

Tab: I'm working with A11Y people on this... we want to make sure the toggles are reflected into the A11Y tree... from our investigation we can't do it automatically but can record the role.. (radio group, tab, etc...) and from there set up the appropriate role patterns. 

Lea: you can figure from these heuristics..... 

Tab: this working well with A11Y is an explicit requirement for this. Pretty important.

Peter: toggles looks and acts like a checkbox... if something is acting as a form element maybe it should be managed as form state rather than presentational state.

Tab: Yes... i think we can do some auto-assigning.  Some way to say "here's a toggle - add this to my form data" would be good. 

Peter: or "here's some form state - reflect as a toggle"...

Peter: is the advice to the authors good so authors know how to use this in the right situation...?

Tab: given that Toggles ... whatever we do in this space is integrateable... 


## Breakout C

Present: Dan, Sangwhan, Amy, Yves

Regrets: Lea

### FTC Response Proposal

### Do we need a finding about the code injection thing?

Dan: ... https://krausefx.com/blog/announcing-inappbrowsercom-see-what-javascript-commands-get-executed-in-an-in-app-browser

Sangwhan: if a page declares itself as doesn't want to be in an in-app web view then it can escape.  Worst offendors are facebook & co... 

Dan: we wrote unsanctioned tracking...  we should say "it is harmful to the web to inject code"

Sangwhan: between user agent and user is the most vulnerable path...

Amy: some of the companies doing it are w3c members... we could reach out via their AC reps...



### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion & [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion

*can we organise a special session?*

Yves: re: security model - i think the security model is given by the app store - that's why there is no need to have cryptography. The fact that it's through an app store and should have a review before entering the appstore.

Sangwhan: bundles and signed exchanges have been trying to solve this... they need to find the missing cases for their use cases.  Push back from the mini-app community. Also exchanges still have issues. But I would like them to work with the people on Exchanges to have a common solution because it does solve the provenance problem and origin problem.  Using the app store as a gating mechanism to filter out bad actors ... doesn't work.

Dan: +1

Yves: there are automated checks that can verify a few things but not filter out all the bad actors..  what's at stake is ensuing you can act as an origin.

Sangwhan: if you treat the app store as a CDN then you can get a lot of that for free.

Yves: will try to arrabnge discussion...

### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou

### Privacy Document

#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

#### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

Amy: framing it as "TAG finding on deprecation of 3rd party cookies" - express suppport for deprecation and then concern for preserving the bad parts of current status quo... and also champion work to preserve non-tracking use cases like single sign on etc


## Plenary Session

Present: Dan, Peter, Max, Amy, Tess, Hadley

Regrets: Sangwhan, Lea, Yves

### Proposed Draft Findings

Dan: third party cookie one and code injection one. Title for the latter should be 'we can't believe we need to say this but code injection is harmful'

Tess: most web extensions work by code injection.. we need to not throw them out

Dan: agreed. We need specific examples. Feeling we ought to reach back to securing the web - one of the reasosn we wrote that was that a lot of network intermediaries were doing code injection and this was an issue. Besides the pervasive monitoring thing. Wifi hotspots and mobile networks. The current things in the recent news are equivalent, we need to help make that clear.

Dan: discussion on third party cookie finding was to frame it around 3p cookies going away, TAG thinks that's good, so now what - let's make sure we don't replace 3p cookies with something that's just as bad

Peter: or worse

Hadley: or more complicated, which could become worse

### Proposed FTC Reponse doc

https://www.ftc.gov/news-events/news/press-releases/2022/08/ftc-explores-rules-cracking-down-commercial-surveillance-lax-data-security-practices

Hadley: they've published a long list of questions under 10 or 12 subheadings... on all things realted to commercial surveilance and data ... everything from tracking with cookies through to companies holding data and securing it properly... big range from very technical through the GDPR type discussions.  Trying to pick out what is in the TAG's wheelhouse ... vs what is out of scope..  First pass - proposing a scope in which we can respond to each of them...  will run through it with interested ... Robin also wrote something that we can pull some items from but much of it may be out of scope for the TAG.

Amy: We can encourage Robin to submit his thing separately.

Hadley: Agreed.

Peter: we shouldn't get too far towards policy but this sounds like a good approach.

Dan: +

### [Element.isVisible](https://github.com/w3ctag/design-reviews/issues/734)

Dan: back with us

Peter: inclined to keep pushing back.. other things being broken is not an excuse to introduce one more broken thing. I'd like to hear from Rossen and Lea.

[next week]

### [Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735)

close satisfied with concerns

```
Thanks again for requesting a review. We're happy with the goals of this work, and think it will be a positive addition to the web platform in the absence of third-party cookies.

We have general concerns about negative impacts if/when it is implemented before third-party cookies are completely phased out. We also remain concerned about how the threat model is changed (eg. introducing new side-channels) when it is used in combination with other work that is emerging to meet use cases which previously needed third-party cookies, in particular the other work coming out of the Privacy Sandbox initiative. We look forward to your ongoing work on ensuring Fenced Frames is sufficiently secure and privacy preserving in the context of the wider ecosystem, and will appreciate another review request when the work has progressed further and with input from other stakeholders.
```

Peter: LGTM

Dan: LGTM

Tess: Looks fine

Hadley: if we look at this again in 6 months will we remember what "other work" means?

Amy: it's in reference to the vague potential issues about privacy sandbox introducing side channnels...

Hadley: more concrete?  can we say "used in other combination with other privacy sandbox work"?  

Amy: when we draft this finding about deprecation of 3rd party cookies that could address some of those concerns.

**some additional wordsmithing**

Peter: ship it! 🐿

### [Render Blocking Status in Resource Timing](https://github.com/w3ctag/design-reviews/issues/753)

*can close?*

Dan: they [opened a PR](https://github.com/w3c/resource-timing/pull/327) that makes the change Yves had suggested.

Peter: looks ready to close.

**closed**

### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676)

*closed on feedback from chris H. at Google*

*marked as "withdrawn"*

### [AbortSignal.timeout()](   )

Peter: sounds like he's supportive but will they take this feedback on? 

Dan: no PR...

Peter: or at least an issue for discussion?  Maybe we should file an issue with them?

Peter: I'll ping them.

### [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746)

*can we progress it this week?*

Peter: another sync vs. async feedback...  To me this feels like - it makes sense to have it sync now but we'll probably regret it at some point.  

Dan: is it satisfied with concerns? Or not resolved?

Peter: I don't know. Need Lea's feedback as well.

**bumped to next week**

### TPAC

Peter: not going to be there

Dan: maybe we don't have enough people to have a slot on the agenda

Peter: so far only Tess and Yves

Hadley: I won't know until the end of next week - hoping to but don't know yet. I did get a bunch of respones from WG saying it'll be great for us to join them. Need to decide if I can figure out how to join remotely or if other TAG members can go instead

Tess: I'm oversubscribed with meetings there already, not sure how much I can do.

### [Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748)

Dan: noting [jake responded](https://github.com/w3ctag/design-reviews/issues/748#issuecomment-1225922770) to Lea's comment.  Great!

Peter: I have some other concerns on the CSS side of this - will dig into it and formulate my thoughts... structure of pseudo-elements feels weird to me...  Let's bump to next week.



### Breakout Rollup

#### Breakout A

Dan: Yves said he will arrange a discussion with w3t for miniapps. Not sure when yet.

#### Breakout C

### Issue Triage
