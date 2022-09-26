
Regrets: Amy, Rossen, Lea

## Plenary Session - [2022-09-21](https://www.timeanddate.com/worldclock/converter.html?iso=20220921T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
### [Element.isVisible review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

Peter: sync vs async... Last we talked we wanted to get Rossen's input.  I feel this is a design mistake across the platform....

Tess: Intersection observer v2 ... what does this do that intersection observer doesn't? It adds convenience.  

Peter: this doesn't take the viewport into consideration

Tess: the default ... they can specify the container... 

Peter: their argument against makint it async is that it's inconvenient - and it's only inconvenient because developers are used to sync - which isn't good for performance. 

Tess: yes.

Dan: Do we need a finding?

Peter: maybe - it's unfair to push back on individual things...   But we also have the principle of "just because something's bad don't keep making things bad in the same manner"...   May be worth making a concerted effort to find these tings and raise issues in working groups.

Tess: dbaron and I had a discussion about what it means to flush layout... some issues... in medium term we will not have a definition [in CSS wg] of flushing that is something we can cite. If we want such a list to exist we'll have to do it ourselves.

Tess: Hard to say "don't do this" without a definiton of "this".  We have to say what we mean by "flush layout."

Peter: we could create a **task force**.  It's within our scope to make a list of APIs... 

Tess: we already have a task force...

Dan: should we push this to Houdini?

Peter: Houdini hasn't been active...  One of the chairs needs to do this.

**agreed to assign this to Rossen**

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov
### [CSS Overflow for replaced elements](https://github.com/w3ctag/design-reviews/issues/750) - @plinss, @atanassov
### [TAG review of Data Catalog Vocabulary (DCAT) - Version 3](https://github.com/w3ctag/design-reviews/issues/758) - @rhiaro, @hadleybeeman

Hadley: still in progress - we put some comments in our issues. Amy opened an issue in their repo which got a response but they haven't fully answered our question... why they are not reusing RDF lists...  They came back and sayd DCAT is hierarchical. Danbri has responded and they haven't replied...  Hopefully we can get a response from them and wind this up.  Also they have done some edits on their explainer that I need to review.

### [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765) - @rhiaro, @ylafon

Yves: I sent some comments and got a reply - some things not defined. Based on what Nick Doty added as well... will check if basic use case is enough... or should we mandate other ways of doing matching.  Amy is looking at it as well..

### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro

### TPAC 

Tess: How was the hybrid format? 

