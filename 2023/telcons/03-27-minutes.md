# TAG Teleconference
#### 27-29 March 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-03-27](https://www.timeanddate.com/worldclock/converter.html?iso=20230327T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @hadleybeeman, @atanassov
* [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss
* [Background Blur API](https://github.com/w3ctag/design-reviews/issues/826) - @torgo

### Breakout C (APAC / Europe) - [2023-03-28](https://www.timeanddate.com/worldclock/converter.html?iso=20230328T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon
* [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman

### Plenary Session - [2023-03-29](https://www.timeanddate.com/worldclock/converter.html?iso=20230329T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Yves

Regrets: Hadley, Dan, Lea, Rossen

Lack of quorum

### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

### [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @hadleybeeman, @atanassov

### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

### [Background Blur API](https://github.com/w3ctag/design-reviews/issues/826) - @torgo


## Breakout C

Present: Dan, Max, Yves, Hadley

Regrets: Sangwhan


### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Hadley: did they check back?

Max: not yet.

Dan: *puts on agenda for 10-april week* if we haven't heard back by then maybe we close.

### [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman



### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

Dan: I think Sangwhan was going to talk to the developers about strengthening the language around threats and abuse cases so let's wait until he updates us on that.

### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

### [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon

Yves: seems like they want to create a VM on top of a VM... So a bit weird but seems OK.  Would be good to have Sangwhan's input.

Dan: so why would you want to create

Max: in the last paragraph - VM implementers - webkit and v8 and firefox 

Yves: *drafts comment*

### [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman

Dan: wendy [got back to us](https://github.com/w3ctag/design-reviews/issues/816#issuecomment-1472362763) - we could take this at face value and close.

Hadley: if we do that we could say "we don't have enough info".

Dan: can you leave that comment and set to "out of scope"? And close.

Hadley: OK.

**closed**

### [Background Blur API](https://github.com/w3ctag/design-reviews/issues/826) - @torgo

Dan: Multi-stakeholder looks good - apple, google, intel.... and mozilla.

Yves: it's a transform stream - which is good - and they exclude detected faces - so easy to implement. 

Dan: in their security & privacy questionnaire response they said there's no security & privacy considerations section currently in the spec. We should for one.]

Yves: fact that they are using transform streams looks good so looks good to me.

Dan: i suggest we set to proposed close and close at the plenary.  

Dan: *leaves comment and sets to proposed close*

## Plenary Session

Present: Dan, Yves, Tess, Rossen, Lea, Peter

Regrets: Hadley

### Breakout Rollup

#### Breakout A

#### Breakout C

Background blur...

Peter: it's a boolean - is a boolean the right choice?

Rossen: it's a good start.  They do talk about adding a blur mode. 

Tess: i think it's fine - boolean will be backwards compatible... to more complicated. This is simple.

Peter: Boolean is just awkward...

Dan: **leaves comment on boolean and bumps 2 weeks**

### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

Tess: Some feedback I've heard: insufficient integratoion with sendbeacon... Entirely new API that is in similar space to existing APIs... and maybe a better API shape would have been to add an argument to an existing API?  [Webkit's position](https://github.com/WebKit/standards-positions/issues/85) - 

Dan: Support but with concerns.

Yves: supposedly it's to save a state server side from the client. The fact that it can be done using GET is not really nice.  Should be a *post*. Using a *get* is not ideal.  *will leave comment*

Tess: Agree.  I can leave a comment.

### [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @hadleybeeman, @atanassov

Lea: can we rubberstamp. 

Rossen: no substantive changes. 

Dan: AT parsing removed https://www.w3.org/TR/2023/CR-WCAG22-20230124/#parsing 

Rossen: this is good news.

Peter: data comes directly from 

Yves: i would say OK to close:

Tess: yes.

Dan: **closes and leaves comment**

### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

Dan: will ping Chris H and put on the agenda for the 10th.

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

### [WebAssembly JS Promise Integration](https://github.com/w3ctag/design-reviews/issues/809)

Rossen: this is big. They ticke the boxes - multistakeholder - questionnaire, etc... however there are some differences between WASM and JS promises... interop between the two is unclear...  They say JS already has promise...


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


**we triage**
