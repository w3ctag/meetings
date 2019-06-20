## TAG Teleconference
##### 19 June 2019

Present: Kenneth, David, Tess, Lukasz, Alice, Dan, Peter, Sangwhan, Hadley

Regrets:

Scribe: Alice

---

Agenda:

* Findings - Privacy & updating ethical web principles
* TPAC Session
* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober
* [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @kenchris
* [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris
* [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @cynthia, @alice, @lknik
* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris
* [Element Timing API (images and text)](https://github.com/w3ctag/design-reviews/issues/326) - @dbaron, @kenchris
* [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @dbaron, @kenchris
* [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321) - @alice, @dbaron, @kenchris
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [FetchEvent.resultingClientId](https://github.com/w3ctag/design-reviews/issues/307) - @ylafon, @travisleithead
* [Display Locking](https://github.com/w3ctag/design-reviews/issues/306) - @cynthia, @dbaron, @kenchris
* [Form Participation API](https://github.com/w3ctag/design-reviews/issues/305) - @plinss, @lknik
* [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) - @cynthia, @dbaron
* [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) - @cynthia, @dbaron
* [Feature Policy JS introspection API](https://github.com/w3ctag/design-reviews/issues/292) - @cynthia, @kenchris
* [Spatial Navigation](https://github.com/w3ctag/design-reviews/issues/287) - @cynthia, @dbaron, @hadleybeeman


---

## Findings

Torgo: There was feedback from PING that they were working on a parallel doc and that they may not be in sync. Perhaps we should refer to it from our document.

Lukasz: I'm not sure there is a clear link...

Torgo: We could make readers aware that PING have also published a document on private browsing.

Lukasz: Ok, sure.

Lukasz: I'm not sure if their document is about private browsing mode, or about adding features to the web.

Dan: Link to document Sam indicated: https://github.com/w3cping/privacy-mode/blob/master/private-browsing.md

Lukasz: ? sent them an email.   This is the document that was published ? the blog note; I suggest we link to the blog note.

Lukasz: They speak about private browsing mode and not only adding fetaures in the context of it.  So I'll think about how to link to it.

Dan: I think that's best.

Lukasz: Specific request?  Just provide a link in the text?

Dan: I'll try to think about it and provide a link in the Slack.

Lukasz: So I'll read the 2 documents and think how to link.

## TPAC Session

Dan: I dropped a link into the slack about how new features are brought to the web...

Tess: Is this about toast?

Dan: ``<toast>`` brought this to a boil... cooking metaphors... 
  
Dan: TPAC session is intended to flesh this out a little bit. I'm unhappy with the mud-slinging online, I think if we're sitting in a room it'll be a more productive discussion. Chris Wilson said he's goign to try and get a session slot, somewhere. Going to work on that with Chris.

Dan: My concept is that we think about it as a joint TAG and WICG session, I feel that we should be trying to drive things into WICG earlier.

Kenneth: May also overlap with WHATWG. We need a whole big graph/flowchart about how it works.

Dan: I would like to produce a graph about how it _currently_ works to demonstrate the problem.

## Badging API

Tess: Essentially a way to set the text for the various badging UIs on varios platforms.

... This was talked about at TPAC on one of the days ... I had a bunch of questions at the time, that was the first time I'd heard of it. I self-assigned cause I wanted to revisit.

... There was an ownership change on the blink side that meant the TAG review request slipped through the crack and would like feedback before then, so I'm hoping to get to it soon.

Dan: There is an explainer...

Kenneth: this has existed for a while.

Tess: I'm happy to share my initial impressions here or in the issue...

Dan: One thing that occurs to me is that ... the OS already does this .... 

Tess: they want to enable it for add to home screen, you haven't launched that site in a while, the server wants to push some notification that contains some hint about unread notifications.

Kenneth: Yes, actual OS-level notifications will trigger this, but you may not always want to 

Sangwhan: Twitter app might be an example, unread @-mentions etc.

Tess: Trying to think about this API from a more device-independent angle. We have widespread behaviours on the web that fit this type of pattern. If you navigate to twitter, window.title gets updated as unread tweets come in, which is the same thing really. It's a hacky way of doing that because the browser doesn't have dedicated UI. 

... So, why is this assigned to a service worker when it doesn't technically require it?

... Seems like they are solving the narrow problem of the OS badging problem but ended up with a much more complicated API.

Alice: might make sense as an element?

Tess: Elements that when parsed would not cause the `<head>` to end and `<body>` to start, might need to be a `<meta>` element.

... But may also need to be set from a service worker so might need an API for that...

Kenneth: Need to contact serviceworker to get those details, so might be seen as more straightforward to do it there for those cases.

Dan: Tess, you're planning to address this offline - let's leave it there for today and move on.

All: Agreed.

## [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @kenchris

Kenneth: There's a lot of meta things about this. This also ties into `switch`. A lot of discussion has happened already. This one was controversial not least because of the name

Dan: Yeah I don't get why it needs to be a standard component, why not just write JS to do it.

Kenneth: the explainer covers this... one reason is having multiple toast libraries on the page ... accessibility

_discussion of name, inevitably_

David: There is more to discuss here about how we introduce new elements to HTML. There's a lot going on with that plan that I think we should look at.

... Web components did this thing where you need a dash in the name, and now we're making the new elements have dashes in their name. What's the theory behind this, when do you use it? Why do we need to use an import? Is that syntax real TC39 Syntax?

Tess: Each of these proposals build on and depend on a bunch of other pieces that are either not there or don't have clear consensus or aren't fleshed out. It's a little hard to do specific reviews when so many underlying assumptions are not clearly going to eventuate.

... it feels a little futile to debate this one element if those things may not come to fruition.

Kenneth: Well the same UI may be surfaced a slightly different way...

Dan: What happened to incubation? This is why I want to have this discussion at TPAC. The Extensible Web Manifesto ... marketplace of ideas ... this seems to assume that that discussion doesn't need to happen in public.

Alice: There is a bit of a misunderstanding of the weight that intent to implement carries.


Tess: these elements don't strike me as a fait accompli, but the underlying assumptions do.

... Domenic asked questions about whether new elements should be fully polyfillable? The HTML community can address these issues at that issue, but I wish those issues had been filed first. I'm happy to see that he agrees that we haven't come to that conclusion either

Kenneth: I think the intent was to drive that precise discussion. I agree that this should have gone to WICG *before* coming to i2i and TAG review.

Sangwhan: It seems a bit dangerous that they're going straight to the standard namespace.

Tess: It's not even that, it has a `js-` prefix in the JS library and the element has an `<std-` prefix. My understanding is that Domenic intends this to be owned by HTML.

Sangwhan: If we decided on `std` as the new standard namespace - why are these going straight into that namespace without incubation? (e.g. why is there no TR1?)

Tess: I think there is a third question... Domenic raised an issue on whether ... DOM level stuff. My understanding is that it (?) wasn't. My understanding of the JS standard library is that it should be equally usable in non-web contexts. So it felt weird to use that mechanism for adding DOM API.

Kenneth: I think it was intended for web stuff as well, like the KV store.

Tess: That one surprised me as well.

... My impression from msaboff was that it was for things usable across all javascript contexts.

Dan: Can somebody take some time to boil down this discussion into an issue comment?

... Domenic mentioned they're hoping to bring it to WICG... extending notifications ....

... What can we do right now besides summarising our discussion here, to push this along?

Kenneth: I'm not clear on whether they are interested in review on the actual element, rather than the underlying things?

Dan: Are you interested to do that?

Kenneth: other than the name... 

Alice: Name is a bikehed honeytrap.  I have a11y thoughts.  I think it's an antipattern; it's difficult to make accessible complete sense.  I spent time working on this with a colleague (Chrome UI bookmarks page).  We wished it wasn't there but did our best.  You can make an accessible version of an inaccessible pattern, but the pattern is not great.

Kenneth: but people are using the pattern all over; otherwise just not accessiible by default.

Alice: so what kind of sad bargain do we need to strike there?

Kenneth: I'd love to have an a11y expert look at this.

Alice: It's not, but you can fudge it to be kind of accessible for some people.

Kenneth: ... if you give it focus ...

Tess: focus seems like an obvious case of its inaccessibility.  Does it popping up change where the screenreader is focused?

Alice: screenreader isn't the worst of it; worst part is zoom.

Alice: I've been waiting for the rush of attention around process issues before getting into it.

Sangwhan: I have technical feedback on ...

Tess: Seems like it should be a mode in the notifications api; then you can rely on system a11y.

Kenneth: these notifications are much more tied to the content; when you've surfed to something else they don't matter anymore.

Dan: We're ratholing into designing the feature.  I think we ought to end the timebox here.

Sangwhan: I don't think we can summarize without agreement on what we want to say.

Dan: We've brought up different issues; they can be asked.

Kenneth: I think a11y should be raised.

Alice: Issue has been snarky so far; we should try to be extra kind.

Kenneth: I can make a comment ...

Dan: I think we should continue this discussion in comments. We have 15 minutes left, I'd like a two minute discussion on each of the other agenda issues.




##  [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

Sangwhan: Waiting on feedback on this one.

Dan: It says review complete...

Sangwhan: we reviewed everything they brought us...

... milestone empty for now, I'll add it to an agenda when they get back to us.

##  [Pointerevent extension](https://github.com/w3ctag/design-reviews/issues/346) - @cynthia, @alice, @lknik

Sangwhan: This was one of the "why is TAG so slow" complaints.

Sangwhan: I need another week on this.

Dan: Will revisit on the 26th.

Lukasz: Asked about privacy/security considerations. Got reply they're waiting for PointerEvents 3 (not entirely sure they intend to tackle it in the e. Are we removing privacy label from the current issue?

## [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris

Sangwhan: Kenneth and I should discuss in a separate call. Long discussion ahead.

## [Element Timing API (images and text)](https://github.com/w3ctag/design-reviews/issues/326) - @dbaron, @kenchris
## [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @dbaron, @kenchris

David: Kenneth and I looked at both of these in Reykjavik. They responded, we should read and evaluate their responses. Good thing to do in our regular breakout next week, or maybe asynchronously.

Dan: Should I set the milestone to the 3rd of July? I'm going to do that. Both set to breakout. You two can caucus on this one.

## [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321) - @alice, dbaron, @kenchris

Kenneth: Gave a bunch of feedback, they changed the explainer and filed an issue about the name. Seems like our work is done here.

Dan: Think we can close it?

Kenneth: Yeah, it's starting to ship as well.

Dan: Consensus on closing issue?

Kenneth: _thanks for flying TAG!_

Dan: *is very excited*

Dan: Can you add the happy label? We reduced entropy in the universe.

## [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron

Dan: This one seems a little stalled.

David: CSS WG still thinks it's a think, but maybe it's not progressing super rapidly...

Tess: David and I were at the HOudini meeting a couple of weeks ago, not much progress was made there on the spec.

Dan: How should we be treating this, from a delivery of value to our stakeholders POV?

David: I think it's still worth reviewing, I think the discussion isn't happening in CSSWG because people think the discussion has already happened. The filer was going to implement it in Chrome, I think.

Tess: Sounds like they need feedback from other implementers, rather than us.

Dan: adding a `Houdini` label. Should we put this on for next week?

Tess: can we do two weeks?

Dan: Ok. Do we need a breakout?

Tess: might be useful.

## [FetchEvent.resultingClientId](https://github.com/w3ctag/design-reviews/issues/307) - @ylafon, @travisleithead

Dan: needs eplainer.. been sitting around for a while.

Sangwhan: needs new assignees.

## [Display Locking](https://github.com/w3ctag/design-reviews/issues/306) - @cynthia, @dbaron, @kenchris

Sangwhan: Being redesigned, waiting for editor updates.

David: Some mozilla folks wrote a position paper.

Dan: Should we set a milestone to come back and look at it again?

Sangwhan: No, let's wait till they come back to us.

## [Form Participation API](https://github.com/w3ctag/design-reviews/issues/305) - @plinss, @lknik
## [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) - @cynthia, @dbaron
## [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) - @cynthia, @dbaron

Sangwhan: Being redesigned, WIP spec draft disappeared. Need to chase down editor.




















