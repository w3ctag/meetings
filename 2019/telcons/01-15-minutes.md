## TAG Teleconference
##### 15 January 2019

Present: David, Kenneth, Peter, Travis, Dan, Tess, Lukasz, Yves, Alex, Alice, Hadley

Regrets: Sangwhan


---

### next telecons : we will have next 2 calls at same time

---

## [transferable streams](https://github.com/w3ctag/design-reviews/issues/332) @torgo

Dan: Travis, you were going to provide some feedback?

Travis: I have some concerns about the user scenarios; also a concern about cross-origin bypass. I'll leave comments on the PR conversation.

## [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) @slightlyoff @dbaron

Alex: was going to have Stefan join... couln't make it. Stefan thought the problems were not what David thought they were, but actually aligned with what David wanted?

David: yes, for the v1 issue... but need to dig in. I'm happy to punt to next week (pretty busy catching up).

Alex: Will hand-off to Stefan, but I may not be able to join next week.

David: Had different concerns around v2. If motivation for v2 is click-jacking prevention, then the spec needs to be truely interoperable. Otherwise you risk cases where overlap differences could lead to a site working in one browser and not others. E.g., a site built for Chrome as anti-clickjacking, but doesn't work in Firefox due to fuzzy borders (or something), and the site denies access. So I really want to be sure Interop is rock-solid.

Alex: So, issue could be with blur? 

David: Or what constitutes what the edge of the blur is. Last time I checked, this was very unclear.

Alex: Could be result of compositor issues/bugs... I share many of the same concerns. Also, in addition to clickjacking, could be preventing monotization (which is equally bad). Recall that sites are already doing this, but using poor methods.

David: Makes sense to address the use cases--I just want more detail.

Alex: What can I tell Stefan?

David: When I gave feedback last time, Stefan made changes re: blur--but I haven't reviewed yet.

Dan: Will return next week.

## [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) @cynthia @travisleithead @plinss

Dan: What shall we do with this?

Yves: There is a discussion on Second Screen, also talked to dom about getting feedback from WebRTC as well.

Dan: Maybe should bump to next week? Give Sangwhan and Travis time to look it over.

## [Review MathML](https://github.com/w3ctag/design-reviews/issues/313) @cynthia @slightlyoff @dbaron

All: Woot!!

Alex: Since TPAC, conversation is Chrome is not generally opposed. Want to ensure good layering in platform. Also want to ensure spec is better (e.g., the rendering section). Also, we want to see tests.

Dan: We've heard this several times, have we delivered the feedback to someone that can take this and make something happen with it? If work is happening, we should let it happen.

Alex: Is there a WG?

Dan: There's a CG.

Kenneth: many folks are looking at our issue, we could give it there?

Dan: Well, we're not interested in having an "etherial" discussion, but rather "here's out guideance". 

Alex: Perhaps we can start with a series of concrete areas that we'd like to see improved. (That's really our job.). Travis you filed this...

Travis: I can start on a doc that we can all contribute to (that outlines the high-level feedback)

Dan: Might be good to collaborate on something (in private) and then paste into the issue where everyone is already looking.

Tess: I too would like to see a Rendering section that is useful for implementations ;-)

## [Vehicle Information Service Specification (VISS) CR pending external feedback](https://github.com/w3ctag/design-reviews/issues/234) @cynthia @torgo @hadleybeeman

Dan: I don't have a car.

Hadley: I haven't driven a car in ages! (But we have a fresh perspective.) Summary: They couldn't break out of the manufacturing idea; couldn't handle the constantly-updating idea. [Gives brief history of issue]
* Wanted to bundle car sensors, but there were complications... wanted to push them to HTTP to handle diverse topologies, etc.
* Clarified what a phone that plugs into the car could get access to; infotainment system capabilities.
* The web has many of the same primitives they were trying to re-invent...
* Issue on liability; if 3rd party builds a poor infotainment system, that has liability on the manufacture.

Dan: Any updates since we last looked at this?

Hadley: The crew is in CR and want more feedback/revisions before finalizing. Have pinged Yves on a different issue... May be able to close this out (process wise), but should ensure we can circle back later.

Yves: There is danger to them re-inventing the wheel--protocol-wise. I've been prompting them over time. I will communicate to Ted to have them send issues our way over time.

## [Serialization of Language Types](https://github.com/w3ctag/design-reviews/issues/178) @dbaron @travisleithead @cynthia

David: was discussed at TPAC (two years ago). We had hoped that Addison or Richard would write something, but we've lost the context... Perhaps I should take a pass at writing this.

Dan: Any way we can get this off the books? Can we try to resolve/close this at the next F2F?

## [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) @dbaron @travisleithead 

David: We put this on the agenda today as a reminder to have me look into it.

Travis: I probably won't get to this by the F2F. Anyone want to take and drive this forward?

David: I can try to make some progress by the next F2F.

## [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101) @lknik

Lukasz: We discussed in Paris; wrote some notes from our Findings. Would like to have some short findings that highlight the Privacy mode. Should we continue with creating a Finding?

Dan: Is there a "mini" finding that we could publish about having "found" Privacy modes? E.g., here's some ways in which privacy modes are different; here's how they impact specification development? We see that many specs refer to "privacy mode" as a special case to be considered; yet, there is no document that defines Privacy mode. On the other hand, no one wants to write it down...

Alex: We've also noted that brwosers that implement this are doing a "poor job" at making a session "private".

Lukasz: Does everyone have the link? I have an older doc that could be a start to the Finding we'd like to write?

Dan: Perhaps me, Lukasz, Hadley could work on this to make it a bare-minimum doc to have the TAG state what issues we see. Should be a small Finding#. If we do something small it can have an impact.

Tess: Concerned with having a referenceable definition of Privacy Mode could try to define some things in terms of that reference. Should we be encouraging this? I want Privacy mode to improve. I don't want to constrain implementations. The term in the specs could be an "attractive nuisance". 

Dan: We could say "don't reference Privacy mode in specs". [tbc i don't think we should say this]

David: We can distinguish between a feature that has a Privacy mode angle, and a set of privacy mode things that imply they are qualifications to be met.

Dan: Can we avoid falling into the trap of setting a low bar that inhibits innovation, while at the same time puts a stake in the ground? Propose bumping to the F2F and do a full break-out session on this.

Alex: Having a proposal ready at the F2F, will be great.

Dan: I could draft something up?

## [IndexedDB Transaction Explicit Commit API](https://github.com/w3ctag/design-reviews/issues/316) @cynthia @kenchris

Kenneth: Well, it's one function! Has a good explainer. Originally, IDB is auto-committing. This will allow folks to commit when folks want it to be commitment; it will still auto-commit but will be later. There is some bikeshedding on the name, since it could be misunderstood.

Alex: Does impact the conversation about retro-fitting IDB into Promise. IDB auto-close was end of micro-task or task; so I don't see this as really controversial. Does anyone have data that shows this can really increase throughput?

Kenneth: No one has brought this up with me. Folks may think that they may need to call "commit".

Alex: Can I call "commit" twice? I would like to see example code that covers the error conditions/handling? Otherwise, this is a very very good explainer!

Dan: Kenneth, you can leave some feedback on the issue?

Kenneth: Yes, and I want to sync with Sangwhan too.

## Next Week

Dan: Perhaps I should spend some time Triaging for next week.

* [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213) @slightlyoff
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) @slightlyoff
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) @torgo @hadleybeeman


---


