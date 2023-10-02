# TAG Teleconference
#### 25-27 September 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-09-25](https://www.timeanddate.com/worldclock/converter.html?iso=20230925T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss
* [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss
* [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @cynthia, @LeaVerou

### Breakout C (APAC / Europe) - [2023-09-26](https://www.timeanddate.com/worldclock/converter.html?iso=20230926T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
* [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman
* [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo, @maxpassion
* [Specification Review: FetchLater API](https://github.com/w3ctag/design-reviews/issues/887) - @cynthia, @ylafon
* [Tag review for Compression Dictionary Transport](https://github.com/w3ctag/design-reviews/issues/877) - @cynthia, @ylafon, @plinss

### Plenary Session - [2023-09-27](https://www.timeanddate.com/worldclock/converter.html?iso=20230927T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Yves, Lea, Peter, Tess

Regrets: Rossen, Amy, 


### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Dan: they got back to us just now with some additional clarity and info - will review and hope we can discuss in breakout C this week.

### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

Dan: Shares [doc from patcg](https://github.com/patcg/docs-and-reports/tree/main/design-dimensions)

Tess: we asked the patcg to help us understand the difference between different proposal. In patcg we used this spreadsheet to drive some discussions in TPAC as well.. 

Dan: where does Privacte Aggregation API fit in?

Tess: actually there is [another spreadsheet](https://docs.google.com/document/d/1oMe3Q7DMG3xzl-peIdq6voVD4PKD822-W4nf4ak7s2E/edit#heading=h.yfjr802w1q8t)... 

Dan: [asks for further clarity](https://github.com/patcg/private-measurement/issues/22)

### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

Tess: [lots of activity here]

Lea: I think they asked us to wait..  The message is still "please wait"... Just reached out to Chris Lilly to ask if we should look or wait - and he said "please wait."

Dan: [leaves comment indicating it's blocked](https://github.com/w3ctag/design-reviews/issues/849#issuecomment-1734085777)

### [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss

Dan: Yoav [got back to us](https://github.com/w3ctag/design-reviews/issues/879#issuecomment-1707991589).... 

Peter: he updated the explainer to answer some of our questions...

Lea: are the heuristics normative?

Peter: looks like they are still figuring them out....

Lea: we should review independent of the heuristics... ?

Peter: curious about multi-stakeholder.  

<blockquote>

If the heuristics are still being worked on, is the purpose of this review to review the rest of the API, assuming the heuristics are good?
Are the heuristics meant to be normative? Will there be ways for the developers to tweak this in either direction (both opt out of a detected soft navigation as well as be able to declare something as a soft navigation that was not caught by the heuristics).
We also wondered about multi-stakeholder interest. https://chromestatus.com/feature/5144837209194496 lists "No signal" for both Firefox and Safari. Have standards positions been requested? If so, including the links to these would be useful (we plan to make this part of our explainer template very soon).
  
</blockquote>


### [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss

### [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @cynthia, @LeaVerou

Tess: there was a breakout at TPAC that I attended - I gave the authors a lot for feedback.  tl;dr  the core idea navigator.install being an API that would invoke the UA's install flow - is a good idea - we should do something like that. Everything else is fuzzy - lots of additional complexity - they are imagining a fairly complex future where you have a web app that's an app store for other webapps..  I get why but it feels like a lot more complexity... If there's a user gesture restriction on navigator.install and same origin only - this seems sensible. It's easier to envision that flow as something browsers might be willing to expose to users. The indirect case ... might enable malicious actors... 

Dan: there does need to be a permission granted from the webapp manifest file to which origins are allowed to install it...

Peter: they want to know if it's been installed... 

Tess: they want to know if'ts already installed  - but a malicious opt in ...

Dan: it would be interesting to see if we could get broad consensus for a same-origin only navigator.install - and then build from there...?  

Tess: we shouldn't block the simple case that we already have consensus on ...

Lea: makes sense.

Peter: they say "the biggest risk is installation spam" - i don't think that's the biggest risk...

Tess: open question in browser land about PWAs and capabilities - because the user installed the thing do you give it more capabilities or not. Mozilla has held the line that you shouldn't.  One concern here - if you trick a user into installing a thing - it's a PWA - but if the browser / OS platform gives additional capabilities to installed webapps then this now has those capabilities... Do PWAs get certain capabilities for free - this makes that attack more concerning.  There's a coupling - the easier you make it to install a thing, the woser it is to allow PWAs to have additional capabilities...

<blockquote>
Hi @diekus - thanks for this and thanks also for the TPAC session on this topic which was really interesting!

Some initial feedback form our TAG breakout today:
  
We're concerned about potential abuse of the "Web app installation from associated domain" use case, especially in a world where installed webapps might be auto-granted additional permissions.
  
We're generally happy with the same-origin-bound use case of `navigator.install()`. We're wondering if you might consider a phased approach to this where phase 1 tackles the same origin case and phase 2 works on the more complex use cases - as this will give some opportunity to explore how the installation function itself works and will give time to explore and design mitigations for potential abuse cases for associated domain installation.
  
We think the expected venue should probably be Web Applications working group (after this graduates from WICG) and/or the WHATWG HTML workstream. 
</blockquote>

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/888#issuecomment-1734131209)

## Breakout C

Present: Dan, Sangwhan

Regrets: Amy


### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo

### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman

### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo, @maxpassion

Dan: considering this is building on top of web serial, which we did not have negative feedback on, and that they have documented use cases and user needs - specifically in the education space - it feels like this should get a "satisified with concerns" from us - the concerns being the multi-stakeholder support which is really the underlying web serial and web bluetooth.

Sangwhan: OK with that. No concerns with the design.

Dan: will set to proposed closing and we can close at the **plenary**.

### [Specification Review: FetchLater API](https://github.com/w3ctag/design-reviews/issues/887) - @cynthia, @ylafon

### [Tag review for Compression Dictionary Transport](https://github.com/w3ctag/design-reviews/issues/877) - @cynthia, @ylafon, @plinss

### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

## Plenary Session

Present: Peter, Yves, Max, Sangwhan,

Regrets: Dan, Amy, Rossen

### Breakout Rollup

#### Breakout A

#### Breakout C


### [Tag review for Compression Dictionary Transport](https://github.com/w3ctag/design-reviews/issues/877) - @cynthia, @ylafon, @plinss

Discussion about CRIME attack, closing as asatisfied.

### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo, @maxpassion

Sangwhan to write closing comment as satisfied with concerns

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
