# TAG Minutes Doc - Week of 24-July-2023

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/07-24-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

## Agenda

### Breakout A (Europe / US) - [2023-07-24](https://www.timeanddate.com/worldclock/converter.html?iso=20230724T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov
* [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss
* F2F Agenda Building

### Breakout C (APAC / Europe) - [2023-07-25](https://www.timeanddate.com/worldclock/converter.html?iso=20230725T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
* [Sustainabiloty of Bundling & Caching](https://w3ctag.github.io/caching-bundling-sustainability/)
* F2F Agenda Building

### Plenary Session - [2023-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20230727T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* Update on any upcoming councils
* F2F Agenda Building

## Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/07-24-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-07-24](https://www.timeanddate.com/worldclock/converter.html?iso=20230724T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Lea, Rossen, Peter
Regrets: Hadley, Amy

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

Lea: looks like there was another proposal presented at the CSS wg... don't know if there's a point in doing a TAG review right now.  I asked in the CSS meeting whether we should review - and I was told that there is.  

Rossen: My take - is that there is a proposal on the table - the spec has been worked on - there are additional considerations... The new proposal is a simplification ... very little new functionality.  People working on this were caught off-guard.  Should we review or not?  I would put to back to the authors... I don't have a strong reason why we shouldn't.

Lea: seems almost certain it will change signifigantly.  Ideally they should update us and let us know.

Lea: i did review - and posted feedback... My main points are: developers want this - but main concern is that (tho it's nice fall back can be specified) fallbacks are opt in - and if you don't do anything then popups stay... which seems undesirable. it seems to me the common case should be the one that requires least amount of code. "i want this popup to be visible in visible part of the viewport" - that should be default behaviour.  With new proposal that behaviour is more possible.  

Rossen: could we feed back 

Lea: "Givenhow the position is specified here it's hard for the browser to figure out what the fallback should be automatically - without the author having to specify explicit fallbacks." Counter-arg from Tab was that there are cases where you don't want a fallback. I suspect the percentage of these cases would be very small.  Bigggest painpoint that this solves is positioning menus, etc... 

... other question was - "it seems difficult to do a pointer... with popups and menus you sometimes want a pointer arrow."

... new API is very well designed and solves these issues.

Peter: i don't think we should review this without incorporating our information about the new proposal.  Maybe put this on hold?

Rossen: i think they are gonna take this back to the whiteboard.

Rossen: we should ask - should we wait for a new proposal?

Peter: not sure we need to be quite so formal...

Lea: we could also establish that these are TAG concerns.. 

Peter: +1

Dan: +1

Rossen: Yes that's fine. I support. 

Peter: if wg ships this as level 1 and something else as level 2... 

Peter: i think the comments stand as they are - I don't think we need to clarify anything.

Rossen: let's just ask Tab explicitly - with the propisal of new additions an enhancements to this, how should we proceed?  

Peter: "givem that we know of propisals to enahance this, we're gonna pause this review." **I can post that**



#### [Cross-document View Transitions API](https://github.com/w3ctag/design-reviews/issues/851) - @LeaVerou, @atanassov

Dan: Looking at [new draft spec](https://drafts.csswg.org/css-view-transitions-2/)

Lea: Cross-fade? what happens?

Lea: "the transition happens" - what happens? [see comment(https://github.com/w3ctag/design-reviews/issues/851#issuecomment-1618916752)

Lea: what happens in slow connection... timeouts... not an ideal user experience.  Response is "because it's same origin it shouldn't take that long" - not a given that it's tested for slow connections and wifi...

Dan: +1

Rossen: i think most of the questions are answered OK... Even for the slow connection.. I think it's a valid point. You control the to and from experience - you can have whatever logic you want as a developer... You can do all of this because it's the same origin... 

Lea: still unclear - how do you prevent a pause after clicking on a link?  Are you able to detect if the user is on a slow connection?  Proposed media query... 

Rossen: maybe start a timer and...? would the browser UX be engaged in this case? so the browser has a spinner... That's not gonna be engaged at all...

Lea: I would expect the browser spinner would start when you click on the link. Maybe that's enough signal that something's happening.  Just want to make sure users on slow connections don't sit there with no feedback.

Rossen: I think that wouldn't happen.

Dan: agree this should be in the spec - right now it doesn't mention "slow"... 

**lea to leave feedback**

Rossen: a section on security considerations -- "concern around safety of 3rd party css - however as a general rule 3rd party css should come from trusted sources" -- that's ... nothing happens as a general rule on the web.  We need a threat model to understand timing-related attack vectors that weren't previously exposed.

Dan: could we ask them to do a more rigorous security review?

Rossen: same origin nav could happen between a 3rd party re-direct... This can cause a (minor) situation... unexpected transition... I think this section needs to be ... strengthened ...  Same origin without cross-origin re-directs.. that's fine.  Other 2 places this is spelled out - in the algo for setting up cross origin view transition...

Rossen: I'm luke-warm.  They did spell it out and call it out.

#### [HTTPS Upgrades](https://github.com/w3ctag/design-reviews/issues/853) - @torgo, @plinss
#### F2F Agenda Building



### Breakout C (APAC / Europe) - [2023-07-25](https://www.timeanddate.com/worldclock/converter.html?iso=20230725T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Dan
Regrets: Max, Sangwhan

#### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
#### [Multiple Readers and Writers in File System Access API](https://github.com/w3ctag/design-reviews/issues/845) - @cynthia, @torgo
#### [Sustainability of Bundling & Caching](https://w3ctag.github.io/caching-bundling-sustainability/)

Sangwhan: will follow up polish on document in the markdown - 

#### F2F Agenda Building

### Plenary Session - [2023-07-27](https://www.timeanddate.com/worldclock/converter.html?iso=20230727T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Amy, Dan, Hadley
Regrets:

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

#### Update on any upcoming councils

#### F2F Agenda Building


