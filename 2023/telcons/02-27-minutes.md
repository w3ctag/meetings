## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/02-27-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-02-27](https://www.timeanddate.com/worldclock/converter.html?iso=20230227T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Pre-empted by the TTML FO Council

### Breakout C (APAC / Europe) - [2023-02-28](https://www.timeanddate.com/worldclock/converter.html?iso=20230228T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo
* [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon
* [Skip no-op service worker fetch handler](https://github.com/w3ctag/design-reviews/issues/815) - @cynthia, @ylafon
* [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman

### Plenary Session - [2023-03-01](https://www.timeanddate.com/worldclock/converter.html?iso=20230301T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [FileSystemHandle.remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @atanassov
* [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)



## Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/02-27-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-02-27](https://www.timeanddate.com/worldclock/converter.html?iso=20230227T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Pre-empted by the TTML FO Council

### Breakout C (APAC / Europe) - [2023-02-28](https://www.timeanddate.com/worldclock/converter.html?iso=20230228T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Amy, Yves
Regrets: Hadley, Sangwhan

#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

*looks stalled - we need to have a focussed session on this*

Amy: they want to ship as an experiment... as Fledge... not sure whether we should be looking at fledge or turtledove https://github.com/WICG/turtledove

Dan: I'll leave a comment apologizing for taking so long and asking them for an update.

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/723#issuecomment-1447753590)

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

Amy: there are three explainers that all go straight into the technical solutions without user needs, and are really long. I don't know how they fit together.

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/724#issuecomment-1447762900)

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

*bumped*

#### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

Amy: have been working on this async... Johann has come back with a clarification.  I've written my comment based on the minutes. 

Dan: I don't recall - it may be that we conflated wuth storage access API.

Amy: I will leave a comment.

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Max: Some feedback from them. They updated the explainer. In the new explainer - from other browsers there is no signal... Not sure whetehr there is a concern.

Dan: comment about a new spec concept, coop group, is interesting.. trying to address developer complexity, is good

Max: there is a diagram [explaining coop group](https://github.com/hemeryar/coi-with-popups#the-coop-restrict-properties-proposal).. within this new coop group pages can have async acccess ... 

Dan: user need...? Some discussion on [user needs](https://github.com/w3ctag/design-reviews/issues/649#issuecomment-874055061) in previous issue... and [here](https://github.com/w3ctag/design-reviews/issues/649#issuecomment-880016720).

Dan: taking a look [here](https://github.com/hemeryar/coi-with-popups#why-does-crossoriginisolated-require-coop-same-origin) .. is it unreasonable to ask for a paragraph of user needs before this paragraph?

Amy: it is OK.

<blockquote>
Hi @hemeryar we're happy to help. However (and I apologize if I sound like a broken record here) but I'm still missing discussion of *user need* in this explainer. What I guess I am looking for is a paragraph before https://github.com/hemeryar/coi-with-popups#why-does-crossoriginisolated-require-coop-same-origin (before the paragraph that starts "because of Spectre") that says something along the lines of "a common web usage pattern is this: users try to accomplish xxx goals; web sites use yyy technologies to create a user experience to service these goals. ZZZ information is exchanged in the following ways.... Because of Spectre this is put at risk in the following ways..."
  
I appreciate that this work is solving an important set of security problems for the web - however part of the TAG review is necessarily to understand how it fits into the overall set of user needs of the web platform.
</blockquote>

Amy: we want to understand this at a higher level so we can see if there are conflicts or related or overlapping work going on elsewhere in another group that this group isn't aware of.. so we can link them up and make sure they're not going to get in each others way... 

#### [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov

Max: no feedback yet.

#### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo

*bump*

#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

*bump*

#### [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo

*bump*

#### [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon

Yves: looks like doing a VM inside a VM... no opinion yet.  Would be good to have Sangwhan looking into it as well.

*bump*

#### [Skip no-op service worker fetch handler](https://github.com/w3ctag/design-reviews/issues/815) - @cynthia, @ylafon

Yves: starts with assumption that it's required to have a fetch handler registered to be identified as a web app... (PWA). If that's the case then i think it's a wrong requirement. I understand this can be a current common practice... looks good as an optimization... but could be removed in the future... Premise is a long one but the solution is a good one as a temporary measure.

Dan: leave that feedback and **close**?

Yves: Ok can do.

#### [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman

Amy: the've left a list of [issues and PRs](https://github.com/w3ctag/design-reviews/issues/816#issuecomment-1430329171)... I'm asking if they can do a tiny bit more work...

```
Thanks for the summary list of changes for us to review. 

We appreciate the strengthening of the security and privacy sections.

We're finding it difficult to review the other changes based on links to PRs and issue discussions however. We'd like to be able to provide meaningful feedback that is useful to the WG. Could you put together a small explainer for the important changes, including what user needs have been addressed by them and why you ended up with the solutions you did? And if you have any specific questions or sections of the spec(s) it would be useful for us to focus on, could you let us know that as well?
```

Dan: lgtm

### Plenary Session - [2023-03-01](https://www.timeanddate.com/worldclock/converter.html?iso=20230301T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Amy. Yves, Peter, Rossen, Lea

#### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Amy: they've [replied](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1428522868) - the person who we thought was making a new proposal says they are making a delta. 

Amy: we're supposed to reviewing the explainer that they keep updating.

Dan: the [explainer](https://github.com/WICG/nav-speculation/blob/main/triggers.md)

Amy: lea left some comments as well.

Dan: [this is what we are talking about](https://github.com/WICG/nav-speculation/blob/main/triggers.md#explicit-referrer-policy)

Amy: still under active development; shipping in chrome; [noone else is interested](https://chromestatus.com/feature/5740655424831488); explainer has no user needs in it (but may be too late to tell them that)

Lea: No archietctural concerns with the actual functionality. However I don't like the syntax.  [see comment](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1101600240)

Dan: have they addressed those issues?

Lea: they opened up issues for some of them. I see one of them is resolved.  Others [in tag] should look at syntax as well.

Dan: are there other examples where the same pattern is being used, around the use of JSON?

Peter: import maps

Dan: if there are other examples then maybe it's not..

Lea: import maps are using json to define metadata, but not to essentially annotate html elements. The only precedent for using a differetn language to annotate html is css (not saying they should have used css for this)

Dan: what about web annotation?

Amy: it's only a data model.

Rossen: proposal to use an `<a>` attribute?  Do we have feedback on what can be better?

Peter: i don't understand json being used to annotate HTML elements? Isn't this one blob of json that's metadata for the document?

Lea: it's like a mini querying language about which elements it applies to.

Peter: selector matches... tagging elements. The rest is more of a map of the site.

Lea: My impression is that any anchor that meets those criteria would be (or not be) pre-rendered.

Peter: yes that example would better be on the element..

Lea: does this apply to link tag? image element?

Amy: it's about pre-rendering things the user might click on? So it would only work on href?

Lea: I think it's only about `<a>` elements.

Peter: I agree that the selector matching seems like a layering violation.

Lea: will create future features that use same syntax... precedent...

Peter: everything other than the selector matches seems like metadata about the site... that seems like it should be one blob of data somewhere. Could be a map on a site... 

Rossen: no well formed opinion.

Amy: an interesting [issue in their repo](https://github.com/WICG/nav-speculation/issues/220)... Alex says "woould have expected this to come up in TAG review"...

Lea: the syntax doesn't allow for likelyhoods to be changed. My understanding is that the json is read once. Whereas if this was an attribute on the anchor then it would be dynamic.

Peter: how does that work if you have multiple pages...

Lea: something to define in the spec... 

Amy: should we invite the requestor to come talk to us?

Peter: if this shipped in chrome and nobody else cares is this a waste of time?

Amy: the conversations are ongoing so it's at a stage where we could influence.

Lea: do they need the whole power of RegExps in href matches?

Peter: wasn't there another proposal for URL matches? 

Lea: URL pattern.

Yves: yes in service worker and they ruled out RegExp because it's not cheap.

Lea: if they don't need it then they could just use selector matching... If their entire selection ctiteria can be described with selectors then why do they need this microsyntax at all?

Dan: does seem like it adds complexity - yet another query syntax..

Peter: does look like they're referring to url pattern spec, not a regex

Peter: should this be in CSS?

Rossen: elaborate

Peter: well selector matching.. it's a language for mapping properties to random HTML .. can be referenced by multiple pages .. 

Lea: reactive

Peter: question is can you consider this presentational?

Rossen: that's my issue. 

Peter: you could start to consider this presentational?  doesn't preculde it from being in CSS.

Lea: i don't think that's a terrible idea though CSS doesn't have URL pattern matching.  Maybe CSS could add URL pattern matching...  that could be useful for CSS as well.

Points to raise:

* Have they considered using CSS?
* Concern continues about use of a novel JSON format for annotation
* Something about user needs not being clearly defined in the explainer
* Meta issue: Things that need to annotate HTML elements en masse that are not necesarilly presentational - how should they work?

Amy: explicit referer - if the user goes on to click the link - if the referer policy is different - it still uses the referer policy for pre-rendering.

Amy: if you set the referer policy in the json and in the link then the pre-renderer referer policy takes precedent. Are there consequences for this?  Maybe means if there is a link to an external site that they author doesn't trust - but pre-rendering is configured differently - then it could have possible privacy implications? could be a stretch. [posted a question]

<blockquote>
 
Hi there,
  
We looked at this again in a breakout today. 
  
The general consensus was that we agree that the functionality is useful, but we have some architectural concerns about the syntax this is introducing in the Web Platform, especially since its is introducing a novel precedent that could affect the direction of even more future Web Platform features.
  
  One thing that came up in the discussion was that this is syntax that is annotating other HTML elements en masse, and the only precedent in the Web Platform for doing so is CSS. Since it could be argued that this is presentational, we were wondering if you have explored extending CSS for this.
  
  Most of your criteria syntax is CSS selectors anyway, and while Selectors do not include matching for URL patterns, this would be more broadly useful anyway, and would make a good addition to selectors anyway. Since CSS is inherently reactive, this would also naturally afford dynamic scoring for links.  
  
  It seems that something like this could reduce the API surface of this feature to a couple of CSS properties, making it simpler to implement and test.
  
  Sorry this has been taking so long. We're trying to make a concerted effort to come back with actionable feedback so we can close this issue as the consensus is generally positive. We look forward to hearing more as the origin trials progress. If you have other specific issues you would like to ask for TAG's feedback on please let us know.
  
</blockquote>

#### [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
#### [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
#### [FileSystemHandle.remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro
#### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
#### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
#### [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
#### [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @atanassov
#### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

