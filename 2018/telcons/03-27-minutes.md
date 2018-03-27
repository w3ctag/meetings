## TAG Teleconference
##### 27 March 2018

Present: Peter, Sangwhan, David, Yves, Alex, Travis, Andrew (partial), Hadley (partial)

Scribe: David

Regrets:

---
## Agenda

### [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - David

David: Alex and I met with Matt recently, and there was a lot of good discussion on this

Alex: The shape of the API we discussed got rid of the URL substitution.  It's modeled as a GET or a POST.  Substitution of named parameters.  It's an evolution from where they started out.  Doesn't get rid of text-only sharing, but still gives URL in the manifest.

Alex: One other question is whether to require Service Worker for user experience.  Discussion suggested non-normative note.  Chrome won't allow unless you're installed as a PWA.

Alex: Proposal is now treating more like a form-encoded GET or POST, could be handled by the page or by a service worker.

Peter: When to discuss again?

Alex: About a month?

### [HTML General Review](https://github.com/w3ctag/design-reviews/issues/174) - Travis

Travis: This is my proposal to break it into bite-size chunks.  Had some feedback from folks at Microsoft.  Looking for feedback from this group on how the breakout is, or whether we should drop something from the review (e.g., appcache, microdata).  Given guidance, happy to take this to the next step and open issues.

[reads]

Alex: Outline algorithm is still here?

Travis: We do use it for something in our a11y code, though simpler version than what's in the spec.

Alex: W3C or WHATWG document?

Travis: I was looking at the WHATWG document; more in it.  e.g., server-sent events, websockets, cross-document messaging, web storage.

Travis: We already have a review open for two of them (offscreen canvas, ?).

David: seems like a reasonable breakdown; will reviewing them lead to useful outcomes?

Alex: Are there large piles of legacy APIs that can be rebuilt in terms of promises, generators (?), streams, etc.  Also some things here that require permissions not currently modeled in the Permissions API.

Travis: We also talked about looking for things that aren't explained well by the platform; forms and form submission is one area we talked about.  Identifying those could be useful.

Peter: Paths forward?  You suggested breaking up into individual issues.  Then we could spend time at the face-to-face triaging and assigning from there?  Maybe add labels to categorize the sorts of things we're looking at.

### [Vehicle Information Service Specification](https://github.com/w3ctag/design-reviews/issues/234) - Hadley
### [CSS ::part and ::theme pseudo elements](https://github.com/w3ctag/design-reviews/issues/230) - David

David: We asked when the spec changes would be done - hopefully would happen next week so let's revisit during the F2F.

### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - Alex

Alex: No further interactions on this since we last talked about it.  Punt again.

Peter: Face-to-face or later?

Alex: I'll ping, and update at face-to-face.

### [ResizeObserver](https://github.com/w3ctag/design-reviews/issues/187) - Alex, David

Alex: Haven't had followup post Peter's comment about fragments vs. elements.  I can ping Aleks.

Peter: ...

Alex: I'll try to talk to Aleks this week and try to represent your view.

### [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101) - Hadley, Lukasz
### [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - David

David: By today turned out ambitious, but I'll try to look this week to have something for face-to-face.

### [W3C DOM](https://github.com/w3ctag/design-reviews/issues/229) - Sangwhan, Travis

Travis: Haven't started anything yet.

Sangwhan: Nor I.

Travis: Punt this down the road a bit.

Peter: Face-to-face, or later?

Travis: I'm thinking after.

Sangwhan: Given the backlog, yeah, I don't think we'll have time during the face-to-face.

Alex: Can we do a triage?  Can we figure out what areas deserve attention so we can chew on a smaller piece when we get there.  I expect a lot of overlap between people for HTML and DOM reviews.  (??)So punt to later if we can't figure out how to split up?(??)

Travis: OK, (?) will do a triage and see if there's anything we want to split out and bite off during the face-to-face.

### [CSS Selectors 4](https://github.com/w3ctag/design-reviews/issues/219) - David

David: Looks like there was comment and response at London, nothing since.

Peter: Where do we go from here?  Is feedback addressed?

Alex: I'll respond.  Would love if David or Peter could weight in on question of explainer or in-document.  I would like to see motivations outlined.

Peter: CSS WG hasn't generally done that, but might be useful for insertions into old documents.

Alex: And seems good to have an explainer explaining insertions into older documents to explain the constraints.

Peter: Done after this response?

Alex: Check back in next week after I write the response.

### [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) - Hadley, Travis

Travis: I finally watched one of Brian's presentations linked from the issue.  I'm both happy we can do speech synthesis on the web (it's cool) and saddened by the shape of the API we have.  It seems simple and straightforward and first, then you get into it, there's a lot of magic happening, it's very hig-level ... wild-west in terms of having consistency between browsers.  Basic controls for pitch, volume, speed, but no way to connect to the rest of the platform.

Alex: Can you take the output and pipe it into web audio.

Travis: Zero connection between this API and the rest of the platform; pipes right to the speakers.  It's a rich area for refinement that way.  Honestly if a revised version were implemented in experiment, or a new shape we could expose, it would be fantastic and I'd love to see somethhing like that move forwad.  In terms of what to do next... we have some folks in a group at MS looking at the speech APIS.  Might be they have an interest in having more expressive power or pushing a few more requireents into the existing APIS, but if that's the case it might be enough to gather some interest among rest of browser vendors and start design work in WICG, which is I think where I'd like to see anything get started if we were to pick this up again.  I don't know that there's a future for a review of the existing APIs... worthwhile to document what we'd want to see in a future API, but assuming nobody's jumping the gun to implement a new thing, that would be where this ends.

Peter: Speech is one of those things where every so often a proposal pops out, but then dies.  Is lack of implementation due to lack of a good design yet, or lack of interest in implementation?

Travis: I'd love to chat with folks I've heard are interested in this ... API seems to be meeting their needs, which aren't complicated.

Peter: shipped?

Travis: text-to-speech part is nearly universally implemented, interoperable-ish.  speech-to-text (SpeechRecognition object) not as well deployed.

Peter: data on usage?

Alex: I can try to find.

Travis: I'd love to have folks from web audio group involved in design discussions.  High correlation between their expertise and what a community group would need to think about.  Thinking about a voice node you could plug in to the audio graph.

Alex: Or a source like for media streams or media tracks like with the various audio and video elements.

Peter: No current working group looking at this?

Sangwhan: right.

Alex: tens of millions of users per day of text-to-speech feature.

...

Alex: Seems low urgency, but seems like we should do the review so somebody later has something to build off of.

Travis: I'm happy to summarize, recap the high and low level issues I've seen so far and write it down in the issue.  Reaching out to some folks and finding if this is meeting their needs, or if there's interest in design work on a v2.

Peter: Milestone farther out?

### [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David

Alex: I believe this was going through intent-to-ship in Chrome.  Has 3 LGTMs; probably will ship.

Alex: Didn't write feedback; I'll take that as an extra action item, before the face-to-face.

## Backlog (reached)

### [&lt;link&gt; rel=modulepreload](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew

Alex: There's a graph of resources you want to request off the network.  May or may not be traversable.  Want to load them as modules (with appropriate request parameters).  This is about preloading a graph of requested resources as opposed to a single resource.  There was a conversation about whether this makes sense to expand... e.g., grabbing `@import`s or fonts from a style sheet... but don't necessarily want to grab the fonts.  modulepreload sort of hints in that direction; not sure where we ended up in that conversation.

Travis: specific to module scripts?

Alex: modules of all sorts... there are puns with other features.

Andrew: The main motivation for modulepreload was that due... you mentioned the dependency thing... CSS has same situation (e.g., dependencies via `@import`s); that's the thing we were waiting for feedback on.  Anne also commented about fetch not doing recursive fetch; this isn't something you can easily layer in; not usre how to explain it.

Andrew: Theres' difficiltlty in the nuance of the semantics here.  We were unconvinced it needed a different name from preload.  If the difference is that it traverses dependency tree, maybe `deeppreload` or `recursivepreload`; `modulepreload` seems targeted towards a single use case.

Travis: That's the first thing I tripped over as well.

Travis: Does fetch get involved.. like a service worker... for the preload contents.

Alex: You sholud receive the `fetch` event.  You want the SW to get an early start at handing back those resources if they were in cache.  

Travis: And a preload request would get them naturally if they were as well.

Travis: And this would be useful for HTML modules down the road.

Alex: That's the idea.  I can write something back to Anne.

Travis: Definitely.

[ Alex leaves ]

## Tokyo Face-to-face

Andrew: see my message about Friday-evening event

Peter: Any developer event planned.

No

Sangwhan: Keio host is getting us lunch.

Sangwhan: I'll consider bringing an extra computer for videoconferencing.

David: guessing no call next week

Peter: correct

## Backlog (unreached)

* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/213) - Andrew
* [Decentralized Identifiers](https://github.com/w3ctag/design-reviews/issues/216) - Hadley
* [import.meta.url and import.meta](https://github.com/w3ctag/design-reviews/issues/208) - Alex



---



