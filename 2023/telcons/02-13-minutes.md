# TAG Calls Week-of 13 Feb

## Agenda

### Breakout A (Europe / US) - [2023-02-13](https://www.timeanddate.com/worldclock/converter.html?iso=20230213T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* New Issue Triage

### Breakout C (APAC / Europe) - [2023-02-14](https://www.timeanddate.com/worldclock/converter.html?iso=20230214T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [FileSystemHandle.remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [Storage Access API](https://github.com/w3ctag/design-reviews/issues/807) - @torgo, @rhiaro
* Merge EWP PRs
* Review Social Impacts Issues

### Plenary Session - [2023-02-15](https://www.timeanddate.com/worldclock/converter.html?iso=20230215T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Autoplay Policy Detection API](https://github.com/w3ctag/design-reviews/issues/810) - @cynthia, @LeaVerou, @rhiaro

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2023-02-13](https://www.timeanddate.com/worldclock/converter.html?iso=20230213T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Amy, Hadley, Yves, Lea

#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

<blockquote>
Hi @domenic - Sorry for the mixed messages. Lea was asking specifically about the [new proposal](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1344814699) from @kjmcnee and I was referring to general updates of the original subject of the review.  So yes, we would very much like to see a separate review opened when there is a new proposal. However the explainer link Kevin provided is to a document fragment, not to a [separate explainer doc](https://tag.w3.org/explainers/). Could you please clarify what we're being asked to review? To be clear: if it's a new piece of functionality that can be written up in an explainer doc, with the specific user needs being addressed, then please open up a new review (with a new explainer). If it's a delta to something we're already reviewing, then please update the current review text/explainer and let us know specifically what changed and why in a comment.
</blockquote>
  
#### [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

#### New Issue Triage

[WCAG 2.2](https://github.com/w3ctag/design-reviews/issues/811) ... requested explainer..

[FedCM auto-reauthentication API](https://github.com/w3ctag/design-reviews/issues/813).. 

[Web Assembly Garbage Collection](https://github.com/w3ctag/design-reviews/issues/814)

[Skip no op service worker fetch handler](https://github.com/w3ctag/design-reviews/issues/815)

#### Epub 3

Yves: we did a review of epub - during the CR phase - they are requesting a review as they go to PR... Demonstate the changes they've done have been reviewed...

Yves: diff link https://services.w3.org/htmldiff?doc1=https%3A%2F%2Fwww.w3.org%2FTR%2F2022%2FCR-epub-33-20220512%2F&doc2=https%3A%2F%2Fwww.w3.org%2FTR%2Fepub-33

Yves: change log: https://w3c.github.io/epub-specs/epub33/core/#change-log

... seems pretty straightforward from TAG perspective... 

Amy: finding it hard to parse ... have they got a sumamry or micro-explainer of what they are actually asking us?

Dan: +1

Yves: fixed OPUS media type is substantive but not from an architectural perspective... 

Amy: [our review](https://github.com/w3ctag/design-reviews/issues/684) is from last April ... 

Dan: we'll defer until they can open up an issue in our design-reviews repo.

#### [JavaScript Symboll.dispose](https://github.com/w3ctag/design-reviews/discussions/800) discussion

Dan: good conversation.. ... anything we can take out of this?

Lea: I don't know about the protocol. They've linked to something.

Dan: what should web developers do?

Lea: Sangwhan?

Dan: I'll ask him in breakout C

### Breakout C (APAC / Europe) - [2023-02-14](https://www.timeanddate.com/worldclock/converter.html?iso=20230214T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Sangwhan, Amy, Hadley

Regrets: Rossen, Yves

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman
#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
#### [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

Dan: anything we can do right now on these 3 things?

Amy: Hadley & I reviewed this - conjunction of FPS and this one... Change to FPS itself made sense. But this additional feature seemed to undo the benefits... We need to dig into it a bit more.

... Hadley also made a list of questions to ask them...

Dan: suggest getting the questions to them ahead of time.

Amy: I'll draft something for the plenary... 

<blockquote>
Thank you for the update and the detailed explanation of the changes. We discussed this in our virtual f2f last week and we agreed we like the direction this is going in. We're still formulating some questions to ask - and the same regarding [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808). 
</blockquote>

#### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Dan: we have new information about [webkit position](https://github.com/WebKit/standards-positions/issues/127)..

Sangwhan: I see pushback about the layering, not the feature itself

Dan: [Mozilla position discussion](https://github.com/mozilla/standards-positions/issues/691) also notes "worryisome" concerns.

Dan: people in this issue are posting without name or affiliation - in this case from Mozilla - assuming that people know who they are - which is a problem across the web community. I wish people would put their name and affiliation in their githib profile when they are acting on behalf of their employer.

Sangwhan: I'm okay with this. There are concerns, it's not mutual in a sense of an iframe that is legitimate and the parent is bad. Permission policy enabled and the nested browsing context, the iframe, doesn't get to have an unload handler. That means that if the parent decides to nix it unload handler will never kick in and if for some particular case the nested context requires to saves state it wouldn't have a change to do that, so it would break. The concern is that there's no mechanism for the nested context to say no I don't want that please let me have my unload handlers

Dan: is there a mechanism for the nested context to know its unload handler won't kick in?

Sangwhan: no, not until we unload. You would still have a slot in the document level as a function.. if you define a handler for it it will still register. If you look it up the function will be there, it will just do nothing.

Dan: is there a chance for the child document to do something to gracefully fail at that point? Can it tell my unload handler didn't run?

Sanwhan: probably not

Dan: I think this is problematic. Just in terms of.. if you've got a child doc that's expecting some kind of behaviour and we're encouraging some kind of fail gracefully approach and you can't feature detect whether something has been disabled by the top level context that kind of defeats that feature. Or it's only used by "evil" child docs so we don't care?

Sangwhan: most cases are to prevent users from navigating away. There are legimitate cases. I don't know how permission policy propagates down and if it's available to the nested context - I'll take a look at that - but if that's not available..

Dan: we could leave a comment about that. Feels like the nested context should be aware that this is not going to work. I don't think tht will create an unfair advantage for the nested context. If anything it will discourage the nested context from using the pattern of doing something to distract the user on unload?

Sangwhan: yes and no..  For malicious cases they would probably find alternative ways to work around. So whether or not exposing that information is useful remains to be answered. Legitmiate cases, fi we don't provide a way for the nested context to beg for permission there's no point in providing this information

Amy: surely the middle ground is just so they know to gracefully fail ... still seems useful to me.

Sangwhan: having context so graceful failure is possible is useful. If you're a text editor... timer that kicks in... if you don't have an unload handler to hint the user they need to press the "send" button then this could have bad consequences.  Concerns might be less of an issue than Moz and Apple are saying.

Amy: an opportunity for that form to present a warning at the top of that frame...

Sangwhan: most of the time the parent is goign to be aware of what is embedded and isn't going to block it with permission policy

Amy: if there's composed web pages... arbitrary services... wouldn't rule that out

Sangwhan: "ad doesn't let the user navigate away from the ad" use cases -- malicious patterns used aggressively. I don't think this will solve all the problems but will solve that problem. Corner case is also valid... [will leave a comment]



#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Max: still waiting for updates since last week.

#### [FileSystemHandle.remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro

Amy: the material at the end of the explainer link is not an explainer from the user needs perspective. 

Dan: yes - no separate explainer and no user needs stated. 

Amy: it's from the site's perspective - i don't think the "site" can be said to want anything.

Sangwhan: it shipped in 110 - last month.

Amy: says "positive signals" from firefox and the the comment was not clearly positive. Positive signals from developers was also less than clear.  In my comment I had 2 questions and I don't think they've been answered in the explainer.  No mitigations against the risk of recursive directory removal specified... 

Dan: should we say "we're concerned - you've shipped but not engaged with our feedback"

Amy: I can leave a comment...

Sangwhan: I think we should put it to resolution timed out... 

Dan: suggest we close the issue - amy to leave comment, sangwhan to close issue.

*consensus reached to close*

```

```

#### Third Party Cookies Draft

*discussion on how to leave comments*

Amy: comments also coming from Amy and Jeffrey Yaskin. Tess and Rossen haven't had feedback.

Dan: I'd like to get this converted into a finding and ship it as soon as possible.

Sangwhan: timeline?

Amy: still need feedback from Tess and Rossen, can wait until next week



#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
#### [Storage Access API](https://github.com/w3ctag/design-reviews/issues/807) - @torgo, @rhiaro

Amy: the conclusion was this is good but we wanted to spend some time going through the detail.

Hadley: we looked at it and we didn't comment ... We're pretty happy with it.  Work is being done in the Privacy CG... They are happy with it. It's got lots of multi-stakeholder support.

Dan: can we close it?

Hadley: we were happy to greenlight it - but do we keep it open for "storage access for origin"

Dan: that's a separate review anyway...

Hadley: will leave a closing comment.

#### Merge EWP PRs

[pr90](https://github.com/w3ctag/ethical-web-principles/pull/90)

Hadley: it says "the community"

Dan: I think it's a statement of what we think this doc is.

Hadley: it's fine - 

#### Review Social Impacts Issues

### Plenary Session - [2023-02-15](https://www.timeanddate.com/worldclock/converter.html?iso=20230215T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Hadley, Amy, Lea, Yves

#### [closing storage access API?](https://github.com/w3ctag/design-reviews/issues/807)

**agreed to close**

#### [sharedStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808)


```
We have done an initial review, and have a few questions to begin the conversation:

1. What use cases are you explicitly designing for? Can you elaborate on "legacy use cases"? Why is just using iframes and the Storage Access API insufficient? 
2. What abuse scenarios have you considered, and what are the mitigations for them? The S&P questionnaire says, "While this functionality comes with a risk of abuse by third parties for tracking purposes, it is an explicit goal of the API and a key to its design to not undermine the gains of cross-site cookie deprecation." -- how does that work?
3. We see "Permission grants for storage access are double-keyed" in the S&P questionnaire, but this isn't in the spec - is there something to add here?
4. Why do images need access to storage? (The explainer alludes to uses for cookies, images and scripts).
```

#### [Autoplay Policy Detection API](https://github.com/w3ctag/design-reviews/issues/810) - @cynthia, @LeaVerou, @rhiaro

Amy: Lea and I reviewed at the f2f... left a comment.

Dan: Sangwhan set it to proposed closed.

Amy: I think we can close this as satisfied.


#### 3rd parties cookie draft

Amy: sangwhan going to review next week.

Hadley: sending comments to you Amy.

Yves: looked ok to me.

Peter: looks ok to me.

#### Sustainability of Bundling and Caching

Lea: Sangwhan & I worked on a doc for this

#### Findings

Dan: I'll go ahead and create new repos for 3rd party cookie finding and for the caching finding.

#### [Private State Tokens](https://github.com/w3ctag/design-reviews/issues/780)

Dan: we set it to proposed closed last week...

Hadley: i think we wanted Tess to have a look.

Dan: suggest we close and let Tess know.



#### Breakout Rollup




#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
