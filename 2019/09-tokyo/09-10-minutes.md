## TAG F2F Tokyo - Day 1
##### 10 September 2019

Present: David, Peter, Sangwhan, Dan, Alice, Tess, Yves

Regrets: Lukasz, Hadley

Scribe: David

Backup scribe: Sangwhan

---

Agenda: 


---

## Triaging unassigned issues

Dan: Go through issues with a 3-minute timebox, mostly trying to just get them assigned.

### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394)

David: unreviewed, haven't looked yet

### [CompressStream](https://github.com/w3ctag/design-reviews/issues/410)

Dan: why isn't this taken care of automatically?

Peter: (describes some use cases)

Dan: assigning Sangwhan, Yves, Peter

### [Wide review request: the HTML Standard Review Draft](https://github.com/w3ctag/design-reviews/issues/412)

Tess: a small document

Alice: Ill assign myself

Tess: We have a bunch of existing open issues for reviewing the HTML spec.

Sangwhan: Because it didn't make sense in a single issue

Tess: Need to figure out how to relate issue to existing ones, figure out a reasonable time frame.

(discussion of whether to fit it into breakout 2b -- doesn't fit)

### [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413)

Dan: how many screens?

Tess: Lukasz might find this interesting

Alice: I like these use cases -- using new explainer template.

Sangwhan: Seems to be exposing stuff ChromeOS internally uses.

... internal APIs for building the shell that let you enumerate the displays.

Tess: I'd be happy to be assigned.

Peter: Ue cases about optimizing video -- codec quality.  Combined somehow?

Peter: Display capabilities / media capabilities and screen orientation should be talking to each other.

Tess: Also second screen.

Sangwhan: ?

Peter: though second screen is more about casting

Assign to Tess and Peter.

### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414)

Tess: Had interesting conversation on Thursday at browser privacy workshop.

Dan: a pointer to notes?

Alice: Wht's privacy pass?

Tess: If you're using TOR - cloudflare lets you solve a capcha and they give you a bunch of privacy passes.  Instead of doing capcha, it consumes oe of the passes.  Cloudflare the issuer, when redeemed, can know that it deffinetily issued them in the past, but can't connect redemption event to issuance event.

Dan: how stored in the client?

Tess: In case of cloudflare work, there's a Tor browser plugin.

Tess: Idea here generalizing it is that browser would be responsible for storing them and vending them when sites request them.

Tess: OK, fine, assign me to it.

Tess: cloudflare's model depends on one trusted issuer and one trusted redeemer, how do you generalize that?

Assign: Tess, Peter, ?, Dan

### [navigator.scheduling.isFramePending](https://github.com/w3ctag/design-reviews/issues/415)

David: I commented, though at time of first comment I didn't realize it wasn't the issue for `IsInputPending`.

Dan: combine?

Tess: no

David: but common issue for both is whether we're ok with violating the run-to-completion design principle

Dan: Can we request issue on IsInputPending?

David: I'm not that fussed about run-to-completion; I think it's less concerning when explicity.

Tess: My worry is we don't make a habit of exposing ??? ... can you change href of a link and then check IsFramePending again to discover link state?

Assign David, Tess.

### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416)

Sangwhan: Yet another attempt at IME (input method editor).

Assign Alice, Sangwhan

### [Service Worker Scope Pattern Matching explainer](https://github.com/w3ctag/design-reviews/issues/417)

Dan: scope different from origin?

Tess: Already the case; this is more complicated scopes.

Tess: Question of other things (e.g., Badging API) that reference service worker scopes?

Tess: Should scopes be defined lower in the platform?

Assign Dan, Kenneth (in absentia)

### [Event-Level Click Conversion Measurement API](https://github.com/w3ctag/design-reviews/issues/418)

Tess: assign to me please

Tess: This is a counterproposal to private click measurement api, a privacy-preserving way to do conversion tracking.  Very similar counterproposal.  But carries 64 bits of fingerprinting data instead of 12.

Dan: lukasz as well?  And Hadley?

Dan: I think based on our findings about data minimization and things like that we'd want to weigh in that les  fingerprinting bits is better than more, but should preparae good argument.

Tess: Concern isn't fingerprinting though bits of entropy are much higher; concern is that threat model is different.  There's one kind of tracking that they're not trying to fix here, which is probably the kind of tracking that is the main point of the original proposal.

Assign Tess, Hadley, Lukasz, Dan

### [Storage Corruption Review explainer](https://github.com/w3ctag/design-reviews/issues/419)

Sangwhan: starts to summarize explainer

Dan: Is this a WICG thing?

Tess: I'm worried about the third reason?  Why add an API to expose browser bugsif we could fix them.

David: It would make sense to actually detect the bugs that may happen


Assign: Sangwhan, David


### [Mixed content level 2](https://github.com/w3ctag/design-reviews/issues/420)

Dan: It's a W3C spec.

David summarizes

Assign David, Yves

## Unmarked issues (without progress labels)

### [Marking tracking vectors](https://github.com/w3ctag/design-reviews/issues/411)

Tess: good idea

Tess: Essentially editorial, since it's pushing stuff down from HTML to Infra so other specs can use them.

Dan: Structure this as a TAG review of that proposal and feedback on that PR

Dan: Normally we'd ask for explainer, to what level should we do that?

David: Feels like this is asking us a question, not asking us to review a thing.  It's not a new feature.

Dan: Should we have an issue template for "just want to ask us a question"?

Dan: I think it's a lot like our other design reviews.  But on the other hand I think we should encouraging more requests like this from WHATWG.  I'd like to take this to breakout, treat as a regular design review erquest.

Assign: Tess, David, Dan, Lukasz?

### [WebXR](https://github.com/w3ctag/design-reviews/issues/403)

Peter: in progress, missing label?

### SMS Recevier 391

Peter: same thing?

### [Autoplay detection](https://github.com/w3ctag/design-reviews/issues/356)

Tess: Arguably shouldn't be opene anymore.  We'd decided to ask the Media WG chairs to handle it.  At the time they didn't have a repository we could transfer the issue to.  It should go away.

Dan: You want to transfer it?

Tess: yes

Dan colors the new label

### https://github.com/w3ctag/design-reviews/issues/352

Dan: just in progress?

### 343

Tess: This has "Progress: big chunk of work" which shouldn't be a progress label.

Dan: should be a review type

### 338

Dan: Just "in progress".

### 330

Tess: stalled, I think.

### 325

Sangwhan: I'm closing it right now

### 310

Dan: Can we look at issue referencing it and see if we need to?

David: I guess if we wanted to do something here we'd explainer or someother documentation.

Dan: Can you put that into the issue

### 240

David: This is what "big chunk of work" was for -- big thing we're asking ourselves (or someone else) to do

Dan: Let's come back to this in the discussion of the retrospective of how we work.

### 360

Dan: same level of thing

# Procedural question

Alice: A bunch of Google folks around who want to know if we want to talk to them when discussing their issue

Sangwhan: Discuss on IRC?

Tess: Outside of face-to-face meetings, we should definitely solve so people can look up information themselves.

Tess: That there's a bunch of folks in Tokyo because of another meeting -- that's already a bunch of Google people.

Dan: Sometimes the discussions in these issue -- sometimes valuable to have requseter in room, sometimes not valuable.

Alice: I may be in the middle of a discussion.  How should we be able to pull people in.

Dan: But how do we know which people these are and that they're in the building.

Alice: Mention when we're starting issues in the IRC channel?

David: Sometimes we don't want to invitem them, e.g., for a 2 minute discussion.

Tess: Also don't want to let others dictate our schedule.

Alice: I'm proposing a way for you to get in touch with them.

Peter: Unusual that people asking for reviews are nextdoor.  More general issue that we don't know who the people filing the issues are.  more generic TAG chat, etc.

Peter: Should part of our issue template be about alternative forms of communication for reaching you?

# Retrospective on how we work

Dan: Peter, can you chair this?

Dan: Retrospective is the high level topic, maybe focus around triage and labels.

Dan: Documenting our process is what we need to do.  We have a lot of ad hoc stuff.  Maybe need a markdown file that says what we do?  Ideally a flowchart about issue lifecycle.

Tess: Sounds like something we could do on a whiteboard

Peter: We have a work mode document, seems out of date.

Dan: Yes out of date.

Dan: So about updating that.

Tess: Scope question: design review process, or the TAG's process?

Dan: Let's talk about the design review process.  I think it needs the most attention.  I think we know how to make findins and stuff like that.

Peter: If the output is making a document for how to work with us and what to expect from us, the design reviews are that primary interaction.

Tess: First thing people do is file an issue
.
Dan: First thing might be reading about what they can expect, even before they file an issue.  Why are they filing an issue in the first place.

Peter: "So you think you want help from the TAG?"

(whiteboarding)

Tess: Do you want TAG review?

Alice: Also the question of whether we want to review it.


(various discussions on the whiteboard)

Tess: Have a badness score that goes up when we bump the miletone?

Dan: We don't have a notion of priority.

David: tracking next action

Tess: And who has the next action.

David: lack of next action could be a problem state we need to fix

Dan: Tess, you wanted to discuss self-created issues (like 240 and 360)

Peter: Often we *want* to bring in other people, sometimes we want others to take it over.

Alice: In Reykjavik I suggested filing issues on the meetings repo for ourselves.

(discussion of whether we also want these labels/milestones in other repos)

Dan: Should self-created issues be in different repo?

Tess: technical/architectural stuff should be in design-reviews, some other stuff no.

Peter: Or another repo for overall architectural questions that aren't design reviews?


Peter:
  - create the bots
  - document the process
  - create new templates/repos
  
Tess: what expectations are wesetting?  This says what... but when?  And document how to unstick things when they're stuck?

Tess: project boards on github - can create in org-wide way.  Track things in multiple repos.  That could be thing that tracks where thinsg are in the workflow; then we wouldn't need to replicate things across multiple repos.  But I've never used them before.

Peter: I've used gitlab a lot, but haven't done this in github.

Tess: Some people *in* the CSSWG use the project boards.  https://github.com/w3c/csswg-drafts/projects

Peter: one of us should explore how these work and understand how they could help us

Tess: 3 kinds of projects: org-wide (cross-repo), repo-scoped, and user-owned.

Dan: repo scoped sounds good for design reviews, for communicating to those outside

David: but we're trying to not forget about the other repos, that calls for org-wide

Dan: Who would be interested in the bots?

Peter: I'm happy to.

bot assignees: Peter, Sangwhan, David

Dan: Ada (co-chair immerive web) has been using bots.  She'll do a talk at TPAC.

documentation (updating work mode document https://tag.w3.org/workmode/) assignees: Tess, Alice, Dan


### Break for Lunch

### Breakouts

#### [Subresource prefetching+loading via Signed HTTP Exchange](https://github.com/w3ctag/design-reviews/issues/352)

Peter, Yves, Dan

Comment left on issue requesting further info https://github.com/w3ctag/design-reviews/issues/352#issuecomment-529758324

#### [Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/354)

Peter Yves, Dan

Peter: where does signed exchanges fit into the cors model?

Yves: You'd have to have that method in the cache...

Peter: maybe every time you get something from a signed exchange it's set-credentials = false.

Yves: I believe that was discussed in the past.

Peter: should things that come out of a signed exchange always be tainted?

Yves: why? it should be the equivelent of if it comes from the origin server?

Peter: question is: what if the origin server screwed up and signed personalized content...

Yves: it makes sense to make it more fool-proof. Do we need another way of tainting it? Not saying that it's insecure but that it may potentially leak something. They want a double key cache. THat may remove that kind of issue.

Peter: what origin gets used? The signed i assume?

Yves: the distributor shouldn't be in the key cache. should be the publisher.

Yves: you don't have a way to "ensure servers don't sign personalized content"

Peter: but if they do, could you mitigate against that in some way?  We can't assure a server isn't going to sign something it shouldn't have signed.

Peter: [as an example] Your bank has a signed exchange which has a bunch of stuff someone else can server - images, script, etc... but it shouldn't have your balance info or account number in it.  Anyone can serve it - and the UA would treat it as if it came from the bank.  But what if the bank screws up and signs a page that has balances and account numbers?

Dan: shouldn't this just be explained best practice that you should never use signed exchanges for soemthing that has PII in it?

Yves: in their response to s&p questionnaire they have stated that signed exchanges should not have personali information.

Peter: is there something we can do to mitiage against the publisher including and signing a page with PII in it?  If the browser treats every fetch that comnes from a signed exchange as "tainted" and never sending credentials - it's not a panacea but maybe it prevents abuse?  If we do that to every fetch from a signed exchange then have we cripled signed exchanges?  It limits the scope of what they are useful for.

Dan: cripling it would be better than having an insecure technology...

[continued to break-out 2, with Kenji Baheux joining discussion + 2 chromium engineers]

Kenji: Prefetch ... for privacy reasons it's not easy to .. this idea of having a non-credential prefetch that's only meant to be used for the next navigation - if it's a signed exchange then it's better.

... regarding the question we had in march - we had best practices, refusing to accept a signed exchnage if it has cookies, etc...

Peter: can we mitigage some of it?  You can't pretend you are doing a fetch without credentials into a signed exchange.  The content could have private info that's generated with soneones credentials by accident. Can we treat everything out of a signed exchange as being tainted?  The page that fetched it can't extract?

Kenji: that might impact negatively a bunch of use cases...  In the whole story having bundled. Don't think that's workable.

Kenji: we still care about the subtext on the first question - "oes it make sense/help things to require that a signed exchange is fetched with credentials="omit"? This requires at least a new attribute on <a> tags to set its credentials mode and Fetch infrastructure to handle that on navigations."
  
Peter: I'm not entirely sure what that means. If you're talking about when you fetch the bundle what does it matter?  If it's from the distributor then it's an opaque bundle and what does it matter? 

Kenji: that's the case where the signed exchange is dynamically generated.   My understanding is that - the scenario you want to enable - you are on a search result page and it has links to signed exchanges - you would use credential omit on the navigation so when you navigate you don't send credentials. (when the content came from a signed exchange)

Yves: also a way to mitigate customised content.

Peter: the a tag in the scenario goes back to the origin...    you're expecting when the user clicks on the link to pull the response out of the signed exchange. 

Kenji: javascript will run so you will talk to the server...

Publisher: publisher a fetches content from b.com. I click a link in a.com origin. Now I fetch a signed exchange from b.com? 

Kenji: today only the main resource is served fromt the cache and the subresource will be fetched from the publishers....

... a tag has link to distributor's signed exchange and the sites who want to use signed exchange prefetch the signed exchange... when the user clicks the link to the signed exchange, in the current implementation chrome sends the credentials (distributor's cookie). this can be used to track.

... the page that has the links would point to the signed exchange... example.com -> example.cdn.etc..  The search portal would know. 

Peter: The browser has preloaded the signed exchange?

Kenji: The search page would rewrite the link to point to the page on the cache.

[some discussion on roles of publisher vs. distributor]

Kenji: we can at least if you use signed exchange then you have to do navigation without credentials...


Kenji: there will be 2 sessions - one for web packaging (in the palenary day) and one for the privacy theat model (priobably in web app sec).

#### Web Publications

We proposed closing our issue.

#### HTTP state tokens

We proposed closing our issue as the work is now ongoing in IETF httpg wg.

#### Web Authentication Feature Detection

We are waiting for a specific epxlainer on this feature.

#### [@property](https://github.com/w3ctag/design-reviews/issues/402)

Alice: Not sure about the order of precedence here

Tess: It's analogous to specificity with `style=""`

Alice: Is it though?

David: I am concerned about potential compatibility issues with `registerProperty` throwing more often if there are conflicts... the issues suggest that these should be two separate registries, but the spec doesn't seem to reflect this.

Tess: Right: in the spec there is only one `[[registeredPropertySet]]`, and there would need to be two.

Filed https://github.com/w3c/css-houdini-drafts/issues/942 and https://github.com/w3c/css-houdini-drafts/issues/943.

#### [CSS Properties and Values API](https://github.com/w3ctag/design-reviews/issues/318)

David: Alex wanted script-based extensibility for syntax classes 

https://drafts.css-houdini.org/css-properties-values-api-1/#parsing-definitions

Tess: Do we feel strongly about this?

David: We had previously agreed to close this, and you (Tess) was going to comment, and then I had a follow up comment. 

[Tess and David draft comment]

Tess: closed

#### [Default accessibility semantics for custom element](https://github.com/w3ctag/design-reviews/issues/401)

Tess: unclear if the outstanding disagreement in whatwg/html#4658 is blocking the PR

Tess: I suggest we assign this review to a TAG participant more removed from the issue...

Alice: I'll ask David

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387)

Tess: What is a "handle", referred to in the explainer? Why does the API refer to a "scope", when the concept used in the explainer is a "handle"?

Alice: I kind of get it - the "handle" (defined early on in the explainer as it turns out) is more like the UI treatment of the abstract concept of whatever the scope is used to refer to, e.g. the app or the website. It's used to refer to both an app icon and a bookmark icon, each of which is a "handle" to something which you use to get to that something. It is a bit quirky to invent this term, though.

Tess: Noting in the issue that we should all read the updated explainer

#### [Portals](https://github.com/w3ctag/design-reviews/issues/331)

Peter: [lots of insightful things re: portal being "iframe done right"]

Peter will write a comment on the issue with his thoughts

#### [User Activation Delegation through postMessage](https://github.com/w3ctag/design-reviews/issues/347)

Tess: closing per latest comment











