## TAG Teleconference
##### 27-29 April 2020

---

### Agenda:

### Breakout A (Europe / US) - [2020-04-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200427T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov
* [HTML Horizontal Review: User interaction, user activation, focus, tabbing, etc.](https://github.com/w3ctag/design-reviews/issues/501) - @torgo, @atanassov
* [HTML Horizontal Review: Windows, navigation, agents and agent clusters](https://github.com/w3ctag/design-reviews/issues/502) - @hober, @dbaron
* [HTML Horizontal Review: Event Loop, task queues, etc.](https://github.com/w3ctag/design-reviews/issues/504) - @dbaron, @kenchris
* [HTML Horizontal Review: misc / reorg / cleanup](https://github.com/w3ctag/design-reviews/issues/505) - @hober, @torgo

### Breakout B (US / APAC) - [2020-04-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200427T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [isInputPending](https://github.com/w3ctag/design-reviews/issues/475) - @cynthia, @dbaron
* [SM series algorithms in Web Cryptography](https://github.com/w3ctag/design-reviews/issues/491) - @hober, @dbaron
* [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss
* [HTML Horizontal Review: the img element](https://github.com/w3ctag/design-reviews/issues/500) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2020-04-28](https://www.timeanddate.com/worldclock/converter.html?iso=20200428T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris
* [AVIF Decode](https://github.com/w3ctag/design-reviews/issues/495) - @cynthia, @torgo, @kenchris
* [Content Indexing API](https://github.com/w3ctag/design-reviews/issues/496) - @cynthia, @torgo, @kenchris
* [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris
* [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris
* [HTML Horizontal Review: Documents, DocumentOrShadowRoot, etc.](https://github.com/w3ctag/design-reviews/issues/503) - @alice, @kenchris
* [Scheme-bound Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon
* [Schemeful Same-Site](https://github.com/w3ctag/design-reviews/issues/497) - @torgo, @ylafon

### Plenary Session - [2020-04-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200429T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

-----

### Breakout A

Present: Ken, Tess, David, Dan, Yves, Peter, Rossen

Regrets:  Hadley

#### [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov

David: 3 threads of discussion in this issue - one was the one we talked about last week - useful for contrast ratio - we have settled. The other is someone who says lab ^ lch aren't very good. A bunch of people disagree.  The third thread is what other parts of the web platform need to be adjusted.  Maybe we should bump it...

Dan: maybe close off the first 2...

David: [bumps 2 weeks and leaves a comment]

#### [HTML Horizontal Review: User interaction, user activation, focus, tabbing, etc.](https://github.com/w3ctag/design-reviews/issues/501) - @torgo, @atanassov

Rossen: it has to do with timing and update of autofocussable elements.  The important discussion is happening in issue 4992 in whatwg...  Has to do with how the browsing context gets updated... if you look a the diff in terms of what this change is doing - it changes when style and layout gets flushed. Previous to this chang it's defined as flush after update to style - at least style has happened. The problem is that some autofocus elements could depend on styling... The argument is you shouldn't have to update layout or style to make this observable.  so... with that in mind.. 

... I looked at the patch that was landed in blink - it's a straightforward change that moves the update style and layout... 

Dan: any contraversy?

Rossen: my take on this is that ... if you want to allow focusability of generated content ... e.g. focusing into list items... desirable feature... not sure how you can compute... does seem like a good change.

Peter: nothing in the style that affects whether it's focusable?

Rossen: yes.

Peter: if something is display: none it's not going to be focusable

Rossen: another reason why you need style computed... 

... previously it was doing it before style and  now it's doing it after style.

Dan: so shall we say it looks good to us? Anything for us to do here?

Rossen: I don't think so. it's a relatively important change for a focusability and accessibility PoV but only improving things.

Rossen: the other items in this issue addressed by Tess....

Peter: design review on User Activation V2.

Tess: i think that would be reasonable - to reference the previous design review. I'm comfortable with not double checking.

[rossen to summarize discussion and close the issue]

#### [HTML Horizontal Review: Windows, navigation, agents and agent clusters](https://github.com/w3ctag/design-reviews/issues/502) - @hober, @dbaron

Tess: there are uncontraversial changes ... david & I to schedule 121?

[decide to do it here]

[HTML issue 4617](https://github.com/whatwg/html/pull/4617)

Tess: this change to HTML - ties together browsing contexts and associated agent cluster. [gives 50k foot overview of agent clusters - agents are thread - clusters are process boundary]. In HTML there is a browsing context - a browsing context group are contexts able to reach eachother - e.g. access to eachothers globals. Therefore they have to be in the same agent cluster.  This change tries to tie together the ecmascript notion of agent usters with html notion of browsing contexts.  You can also have dedicated workers. A browsing context group and an agent cluster are roughly 1:1 but an agent and a browsing context are not 1:1.

... If you look at the actual diff.. what's interesting ... this adds the text that says every browsing context group has an associated agent cluster map.  If you consider a browser tab with some iframes and popup windows.. relationship between these things becomes fuzzy. the process boundary tends to be at a site rather than an origin.  A big chunk got removed - a hand-wavey description of how these things related and they've added in something that's much more detailed.   This is a better description of how browsers work today that ties html concepts more closely to ecmascript concepts.

Dan: are there still areas where things fall through the cracks?

Tess: the followup work has covered all these cases - as of today.  One of the things that this changes - it adds several algoritms that tie things together. Every agent cluster has one agent in it that corresponds to a ... window. A window has an agent but a window can also spin off things...  but aeach anegt cluster has only one agent that is a window. this change has the algo that specifies that... 

... good example of a change to html that is dififcult to do but not contrarsial. 

David: how much is this a thing that .. given that there is variance in implentation .. how much room does it leave?

Tess: leaves as much as ecmascript leaves... there is leeway to have different process of models. It just clarifies the wiggle room.  The idea is we 

#### [HTML Horizontal Review: Event Loop, task queues, etc.](https://github.com/w3ctag/design-reviews/issues/504) - @dbaron, @kenchris

Ken: specifies which event loop... clarifies ...

David: it clarifies the structure of the spec - moves text from one place to another...  new text puts the text "where you have to make the decision"

Ken: 2nd one is bigger - raised concerns of lack of formal definition of a task document. It seems to be in the same domain as agent clusters, etc...   The rest of updating everythng to be correct with this definition.

Tess: it's follow-on.

David: it looks sensible but one thing that is weird is the small number of things that use the new algo.  

Ken: if you look at but #4980 - a "ton of work"

David: if you look at 4980 there are a large number of commits. A pile of other PRs

Tess: 5342 is still open ...  leaves the spec in a hybrid state. A good change.

David: this seems fine.

Ken: last one is regarding forms..  submit event object... Adds who submitted the event.   ``requestSubmit`` funnction ...

Tess: does it relate to form validation?  If validation fails then submit doesn't happen.

David: this seems fine.

Peter: check them off and close it.

[consensus to close]

#### [HTML Horizontal Review: misc / reorg / cleanup](https://github.com/w3ctag/design-reviews/issues/505) - @hober, @torgo

Tess: a ... collection of [small] changes.

... it ends up being a huge diff as it impacts every constructor, but the actual meat of the change is fairly boring. the interesting change is the html constructor change itself... 

... next one 5190 - there's a separate DOM parsing spec - this change moves that defintiion into the HTML spec. Results in some changes to the DOM parser. Mostly nits.  This fixes defining what the URL of the document is. It fixes something that the previous DOM parser spec didn't do clearly. ... when there's an error what happens?  This is also [uncontraversial].

... lastly:  "Cleanups to "execute a script block” Signpost the debate on some script mismatches" - when we chunk out work for people to review.. this last one is an example - there was another, bigger changes that got split into 2 - the other change is the interesting one and this is the editorial stuff that got pulled out to clean up review of the interesting one.

th..th..that's all folks.

### Breakout B

Present: Alice, Peter, Tess, Rossen, David

Regrets: David, Rossen, Sangwhan, Hadley

#### [isInputPending](https://github.com/w3ctag/design-reviews/issues/475) - @cynthia, @dbaron

David: People seem to be ok with the run-to-completion violation... need to look at the response in more detail. We may be able to close this at the plenary.

... Will mark as propose close.

#### [SM series algorithms in Web Cryptography](https://github.com/w3ctag/design-reviews/issues/491) - @hober, @dbaron

Tess: This is a request to add a specific set of algorithms to the WebCrypto API... we asked them to fill out the missing bits of our issue template, and their answer left a lot of fields N/A or `unknown`.

... We got a response 4 days ago, from the person who filed the request, explaining that they are from the 360 browser. They mentioned the QQ browser also support the proposal.

... In the past the Web Cryptography WG have been reluctant to add this type of algorithm. If that WG still existed, they would be the right people to make this call, but they don't.

David: There has been some discussion about chartering a new Web Crypto WG; still uncertain about whether that will go ahead. 

Tess: Is there something we can cite about best practices? It would be nice to be able to point to some kind of industry consensus.

(brief discussion of whether there's any IETF stuff written down)

David: In general, the consensus seems to be that we want fewer cryptography algorithm options, with a high bar for inclusion.

Tess: Let's come back to this in two weeks.

#### [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

David: Examples in the explainer look like they're non-reusable, i.e. it's less a template for components than an entire DOM tree some of which happens to be in shadow roots.

Tess: Right, this is intended as a very narrow feature to handle this sever-side rendering case, where they're serializing a server-side representation of the DOM, and it doesn't matter that they're repeating DOM.

... This isn't a general purpose solution for custom elements.

David: When I saw the title, I was hoping for something more...

... Reminds me of writing XBL and linking to it from CSS (though the linking to it from CSS was not great).. there were some nice things about that, I guess.

Tess: I need to read up and refresh my memory on this discussion, don't have time in this breakout so let's bump it a couple of weeks.

#### [HTML Horizontal Review: the img element](https://github.com/w3ctag/design-reviews/issues/500) - @hober, @cynthia

Tess: Happy for anyone else to have thoughts on this... interesting one is pull #4952. This came up in the CSSWG over the years, wanting to specify an aspect ratio for generating a placeholder. I think Jen Simmons did a bunch of work.

... What ended up landing in HTML is to calculate an aspect ratio based on the content width/height attributes.

... Seems like a clean solution to the problem, reusing existing markup without making things more complicated. Fairly small change.

Rossen: Don't want to revisit the discussion we had about this previously... I don't recall this having been the favourite path forward in the past... we didn't like this solution due to potential impact on existing content. Has anything changed since then?

Tess: I don't recall if anyone did compat analysis. Multiple engines are now shipping this change... 

David: I think the way this ended up ... it has fewer compat problems but it's also a little harder for a site to go back and use it effectively. 

... Wanted to be able to upgrade CMS software to provide correct aspect ratio for images... by adding a new feature rather than reusing existing feature, means that you could opt in.

Rossen: I recall discussions where this particular method wasn't the most favoured one, so I was curious what changed.

David: I think this was where the most recent discussion ended up. This is the most we can do without adding new syntax to the web. Isn't everything everyone wanted to do with it, but it is a reasonable change.

Tess: I agree. Is there data to suggest that this change was a bad one? Has gecko gotten bug reports from people seeing site breakage?

David: I think the proposal was refined a number of times as a result of bug reports. Hopefully what got merged into the spec was the end result of that process.

Rossen: From the TAG point of view, I don't have any objections or pushback in terms of solving the use case.

... recalling the discussions that happened around working groups, trying to see if this may have been controversial.

... I'll write a comment linking to some of the earlier discussion from CSSWG.

Tess: Removing progress events... people didn't implement them. Firefox implemented, there is a bug for them to remove. Just removing a feature that didn't get traction.

... Spec text around loading completion, making it match reality a bit better. It's not terribly exciting.

... I think we can check off both of these and move on with our lives.

Peter: On the aspect ratio thing... this is using width and height to set the aspect ratio until the image is loaded, but the width and height overload the intrinsic size of the image. 

David: But they don't override the aspect ratio once the image is loaded... I guess.

Rossen: I am assuming that the right discussions took place.

Peter: Looks like this will be discussed at the CSSWG F2F, so we can revisit after that.

### Breakout C

Present: Dan, Ken, Yves

Regrets: Sangwhan, Hadley

#### [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

Ken: i have progressed this..  We have an explainer now... it's pretty OK.  You will get a dialog... up to implementation whether nor not if you deny permission the app will still get regular camera access.

... you will get video permission... then you (app dev) will have to check if you have access to pan/tilt... 

Dan: that's to mitigate the fingerprinting...?

Ken: yes but also not to force users to accept a powerful permission. It's a specific other set of permissions that you will be shown in the permission prompt.  Needs to work if you do or don't have the camera plugged in...  Seems to be fulfilled.

... other thing... when a web site is not in focus (when you are not looking at the screen) then these capabilities will be disabled.  Not yet in the explainer but they said they would consider it.

Dan: how much of what you just said is in the spec vs the implementation?

Ken: Not sure.  They [chromium] are doing the implementation now.

Dan: [left a comment and bumped to next call]


#### [AVIF Decode](https://github.com/w3ctag/design-reviews/issues/495) - @cynthia, @torgo, @kenchris

Ken: No update yet.

Yves: mark as pending external feedback...

Ken: if we're not getting answers ... we should ping them...

Yves: I askec Chris Lily to look into it.

[bumped]

#### [Content Indexing API](https://github.com/w3ctag/design-reviews/issues/496) - @cynthia, @torgo, @kenchris

Ken: intent to ship is happening in chrome?

Dan: [leaves comment asking about venue](https://github.com/w3ctag/design-reviews/issues/496#issuecomment-620457974)

Ken: is this about content being shown in other places in the UI - then people will be aggressively caching things in order to get shown...

Dan: if something shows up in the notification tray, that is big money.  This requires scrutiny.

... "sites to increase user engagement" - that makes me concerned.

Yves: they want to use periodic background sync to refresh and that part is contraversial for privacy reasons.

Ken: [leaves comment](https://github.com/w3ctag/design-reviews/issues/496#issuecomment-620461255)

[bumped]

#### [VirtualKeyboard API - show/hide policy](https://github.com/w3ctag/design-reviews/issues/498) - @cynthia, @kenchris

Ken: they are saying this is different [from the WHATWG issue]...

... asking for more comments.. not there yet...

Yves: let's let people try ot get consensus first - in the end they may decide to do somehting different.

[set status and bumped]

#### [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris

Ken: good, sensible idea...

Dan: should we do something different here to #498 - like maybe close this issue off?

Ken: it's a javascript api and you can only opt in via javascript... we have css environmental varialbes - why can't i do this from CSS?   Instead of having to force people to use javascript?  Very specific use case...

#### [HTML Horizontal Review: Documents, DocumentOrShadowRoot, etc.](https://github.com/w3ctag/design-reviews/issues/503) - @alice, @kenchris

Ken: [on first item](https://github.com/whatwg/html/pull/4837)... already implemeted.. totally for it... no issues.  What we are missing is the "why" the use case.  Especially when we come to wide review. I don't have that info here...

Dan: maybe we should wait for Alice 

Ken: same with other APIs - we don't have enough of the context.

... [this](https://github.com/whatwg/html/pull/4907) seems like a bug fix... seems sensible.

Dan: check that one off?

[done]

Ken: [the svg one](https://github.com/whatwg/html/pull/5109) - sounds like a bug fix.  

Dan: Agin we are missing the context... 

Dan: let's bump this to the plenary.


* [Scheme-bound Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon

Yves: [cites AWWW]

Dan: let's bump to plenary

Yves: to discuss implementation status

### Plenary Session

Present: Dan, Ken, Alice, Tess, Rossen, David, Peter

Regrets: Sangwhan, Hadley

Scribe: Dan, David

* [Scheme-bound Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon
* [Schemeful Same-Site](https://github.com/w3ctag/design-reviews/issues/497) - @torgo, @ylafon

#### Breakout A Rollup

David: **Lab & LCH colors**... 3 different threads - one to keep open. I emailed Chris Lilley. He got back to me last night. Need to look through that.

Rossen: computed values?

David: what other parts of the web need to be changed...

Rossen: anyone else follow up with computed values issue?

Alice: i haven't.

David: 4th thing - I'll add a comment.

Rossen: On **user interaction [horizontal review]** - flushing autofocus candidates.  Overall this is the right approach.  With that and the 2nd issue having been discussed we reslved htis. 

Tess: agent clusters... like the other onese, we took at look at the pull requests and we found we didn't have any concerns.  We've closed all but 1 of the HR issues.

#### Breakout B Rollup

Peter:  **[isInputPending](https://github.com/w3ctag/design-reviews/issues/475)** marked as proposed closed.  David proposed we close it at the plenary. 

David: one thing in their comments I wanted to look at and it seems fine. The idea is they want to say certain events are not the kind of things you want to interuupt for - but an option.  Seemed reesponsive to the feedback. I'm happy with closing it.

[resolved to close]

Peter: **SM Series Algos**: decided to come back to it in a couple weeks.

David: nothing from IETF contacts

Peter: I did some research - some of it was starting to look scary with key escrow - but sm9 does not use key escrow. 

Peter: **[declarative shadow dom](https://github.com/w3ctag/design-reviews/issues/494)**  - we did get some feedback on that 2 hours ago

Alice: the feedback doesn't really answer my questions - some more answers came from elsewhere. It seems to me that it's style encapsulation - Pixel-correct output.  So I'll respond ... Does that answer the use case?

David: it explains why they are doing it .. but I think there might be a lot of other reasons people want such a mechanism... The thing I'm most worried about is making it harder to do something that's more generally useful.

Peter: valid concern.

Alice: beyond the rendering case...

Ken: without using JS

Peter: yeah.

David: there has been a ton of discussion on the web components world about this... 

Alice: alternatives considered section - and the prior discussion do cover that fairly well. The WC issue was very long.  It seems like - there was [pushback] around adding another element.  We can bump this to another breakout.

Peter: this feels like a layering violation.

Alice: why?

Peter: you're exposing the shadow root - it's taking what's supposed to be encapsulated in a custom element and exposing.

Ken: but the CSS is still scoped to that shadowroot.

Alice: the style encapsulation thing gives me the most unease.  We should have a thing for style encapsulation.

Ken: we have shadow root -

Alice: that's not what it's for...

Ken: when I'm doing something with WC - style encapsulation is one of the reasons people use shadow root.

Rossen: horrible reason for it to exist.

Alice: best answer - for hiding language style - not a bubble for CSS

Peter: this puts it in the dom of the parent document..

Alice: 2 responses - style encapsulation and rendering the things on the server side.. 

Alice: the reason I am excited about using it for CSS encapsulation - is that it breaks other things e.g. Aria references. 

Peter: [**image element horiz review**](https://github.com/w3ctag/design-reviews/issues/500)

Tess: same as before - nothing of arch concern.

Rossen: some discussion took place today in CSS working group - - the current proposal in the HTML repo is sane. This is the agreed upon way.  No additional reservation.

[closed]

#### Breakout C Rollup

Ken: on **pan/tilt/zoom**: they did an explainer but some stuff to still work out...

Ken: the privacy issues are being accepted ...

Ken: **AVIF Decode** - no update yet

Ken: **Content Indexing API**:  intent to ship - 

Dan: [response from rayan](https://github.com/w3ctag/design-reviews/issues/496#issuecomment-621329634) i may respond about the abuse section regarding mitigations.

Ken: [**virtual keyboard api show/hide**](https://github.com/w3ctag/design-reviews/issues/498) - we get back to it when they have consensus

Ken: next **virtual keyboard API** - seems like sensible idea but all based on JS - no reason why they couldn't use CSS env variables... left comment

Ken: [on **html HR documents, etc.**](https://github.com/w3ctag/design-reviews/issues/503) we checked  - we'd like Alice's comment.  SVG seems like a bug fix.  We bumped to plenary.

Tess: it's fine.  a bunch of machinery about how ths spec talkes about browsing contexts changed in this timeframe and i think this change is related to that. I think it's cleaning up.

Alice: looking at [the active-element](https://github.com/whatwg/html/pull/4837) sub-issue. it's about getting - defining a chain of active elements - if you request active element for dociemnt.shadowroot ... it maakes sense.

Ken: this is adding something to shadow root which was already existing...

Alie: this is catching up 

[issue closed]

Tess: I will report back to the html wg that they have been cleared.

#### Rollup of breakout from Friday last week

Dan: We had a breakout on **Scheme-bound cookies**, minuted in last week's call.  Nothing added to [issue](https://github.com/w3ctag/design-reviews/issues//483) yet, though.  Need to figure out next steps.

Dan: Idea is moving to cookies not crossing scheme boundaries.  More secure.  But some of the web relies on old pattern of http website with https sign-in page.  Peter's point is that a lot of websites don't have people working for them that can update them in a timely fashion.  So some mechanism to mitigate against that if this change goes through.

Dan: Other question is finding out what multi-browser engine appetite for implementing is.  Mike was reaching out to someone from Apple.  mozilla standards position [was supportive](https://mozilla.github.io/standards-positions/#scheming-cookies).  Was consensus on this in an HTTP workshop as well with broad attendance.

Dan: Mike was concerned that mitigations would make this less effective.

Dan: Would be worth you reading the minutes from last week and Mike's description.

Dan: We could keep this open or close it off with concerns about existing content and unintended consequences.  Doesn't help anyone to leave it open unless there's something to be worked on that we need to keep tabs on.

Peter: I'm OK with closing it.  Mike is aware of concerns and has good ideas about potential mitigations.  If that becomes a huge factor it'll be pretty readily apparent when this is deployed; would lead to fix or revert if needed.

Dan: We could also reiterate about multi-engine support.

Dan: Peter, you write about unintended conequences, I'll write about multi-engine support, and then we'll close it.

Tess: I'm happy to close it.

Dan: What about **schemeful same-site**?

Tess: I'm cofmortable closing it.  Brings IETF notion of same-site in line with HTML's.

Peter: Less concerned about thi.  I think most people will thnink about same-site as being scheme based.

Dan: So consensus to close both things?  Or Tess, do you want to write something in 497?

Tess: Sure, though I don't have that much to say.

Dan: What you just said.


Tess: sure, I can capture that.  Already in minutes from last week.

Dan: "look forward to hearing more." etc.

### Triage

#### [navigation to unsigned web bundles](https://github.com/w3ctag/design-reviews/issues/509)

kenneth, tess, and david volunteer, milestone set for 2 weeks

#### [shortcuts member of web App manifest](https://github.com/w3ctag/design-reviews/issues/510)

Kenneth: already gave a lot of feedback

Dan: I should be on it too.

### Design principles next week

Tess: Alice and I will try to set up a breakout to  finish our 2 PRs.

Dan: Getting more HTML design principles in?

Tess: I'll try to get more issues filed to do that.

Alice: I'd suggest looking at other non-design-reviews repos.

Dan: Agree.  I'll try when putting together agenda.  Send me particular things if they're on your mind.  We could look at security & privacy questionnaire document.  Plenary or breakouts?

Alice: breakouts seem good.

Peter: In Wellington we talked about being able to set milestones in any repo and fix the agenda generator script.  Haven't done it yet, but feel free to start doing that and I'll update the script.  Milestones should be for Mondays.

Alice: At some point I'd love to look through our processes.  We could start to automate some things if we sat down and wrote down what they were.

Dan: how will we whiteboard in Face-to-Face?

Peter: cryptpad has it

(discussion of tablet-like devices and pens)
