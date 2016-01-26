# Melbourne F2F  Minutes

Present: Peter, Alex, Mark, Hadley, David, Travis, Yves  
via Teleconference: Dan, Andrew Betts (Welcome!)  
Regrets: Tim (in Italy)  

Of note: W3C announcing move to https on their site: \url{https://lists.w3.org/Archives/Member/w3c-ac-forum/2016JanMar/0028.html} (references our securing the web finding).

## Wednesday

- 9:00-10:00  agenda bashing
- 10:00 - 11:00 Spec reviews
- 11:00 - 12:30 

- Revisiting deliverables: 

   *  Packaging on the Web
   *  Design Principles
   *  Security Questionnaire
   *  Promises Guide (does it need any update?)
   *  Report Card (update? close it and declare success?)
   *  Private Mode
   *  Privileged Contexts ...

- lunch 12:30 - 13:30

- 13:30 - 14:30 Revisiting deliverables (cont)

   *  Packaging on the Web
   *  Design Principles
   *  Security Questionnaire
   *  Promises Guide (does it need any update?)
   *  Report Card (update? close it and declare success?)
   *  Private Mode
   *  Privileged Contexts ...

- 14:30 - 17:0 Spec reviews

## Thursday

- Mike West update: 9:00 - 10:00
 * CORS...
 * Tim's questions about certain kinds of fetches...  (slightlylate to find URL)
 *  status of secure contexts document https://github.com/w3ctag/spec-reviews/issues/75
 *  https://github.com/w3ctag/spec-reviews/issues/74

- 10:00 - 10:30 

- Debrief from the Extensible Web Summit
- New name?

- 10:30 - 12:30 Spec reviews

- lunch 12:00 - 13:00

- 13:00 - 14:00 Fido (+ Keygen bonus discussion)

- 14:00 - 15:00 Web Payments Discussion

- 15:00 - 15:15 Break

- 15:15 - 15;30 [EME Secure Release](https://github.com/w3ctag/spec-reviews/issues/73)

- 15:30 - 17:00 Brainstorm IA for the TAG's web site(s) https://github.com/w3ctag/spec-reviews/issues/53

*  Stuff we haven't fit in anywhere else

## Friday

- 9:00 - 9:15 Schedule next meetings

- 9:15 - 11:15 Spec reviews

- 11:45 - 12:30

* What role should TAG take in charter development
* Role of TAG in guiding expermental features in browsers?

- lunch 12:30 - 13:30

- 13:30 - 14:30 Accessibliity with Chaals

- 14:30 - 16:00

* Web components update
* IETF update, Captive portals
* Houdini Update
* EME and the non-sue covenant... (Cory discussion) -Yves gave an update on that and the proposed extension to the HTML Media Extensions group
* Policy interest group

- 16:00 - 17:00 Stuff we haven't fit in anywhere else

# Topic: Spec Reviews

## Issue 14: WebRTC: https://github.com/w3ctag/spec-reviews/issues/14  
mnot: this was to track the privacy issues in webrtc I believe.   
... ekr, martin thompson, fluffy, etc., might know...  
andrew: this is about leaking internal IP. I did this last week!  
... I was looking into implementing a self-discovery system... and indeed, you can get the IP addresses.  
Travis: In edge, we have a config flag for this (the 'about:config' UI).  
mnot: ekr says there's ongoing research into whether the exposure of IP could be more limited.  
... in short order we can get updates from either martin or ekr.  
Andrew: I have a demo I can paste into the issue.  
mnot: it's slow-going. It's a hard problem.  
Alex: q for the tag, do we need to disable this for the health of the ecosystem?  
mnot: are you talking about disabling webrtc  
hadley: I like that UX options are also being explored  
mnot: I'm not sure we're qualified to jump into the discussion  
alex: We could make a recommendation that if/when this info could/is about to be exposed, the user agent to interceed and alert the user.  
... you could imagine this gives the platform a bad name, and may need to be addressed.  
hadley: this is serious when users are decieved.  
alex: we know people are using this in the wild for fingerprinting  
mnot: I know all identifiers that are being generated are ephemeral.  
... rather than displaying all possible routes, they could just show the single route.  
... in IPv6 it's game over. In IPv4 the IP is exposed. Current discussion is around questions about implied consent or positive consent. Lots of folks start to get nervious about the privacy implications.  
... could potentially expose less information than is presently being exposed.  
firefox gave some APIs for this to extensions for experimentation.  
hadley: I'm wondering if I'm underestimating the impact to current users.  
alex: Apparently your current IP address is already "leaked" to web servers.  
... if this is already available through another side-channel then this is probably a moot point.  
mnot: I started with lots of concerns. Users should have reasonable expectations. But most users still have Flash (a side channel).  
david: I've seen setups with timers and image requests that try to expose more information.   
mnot: We've kept this issue open for tracking and to follow along.  
  
## Issue 18: Navigation Timing 2: https://github.com/w3ctag/spec-reviews/issues/18  
mnot: milestone is out of date, will clear it.  
alex: performance observer hasn't made much progress--lots of issues.  
... ilya and I will have time to chat about this next week.  
alex: nav timing 2 was a proposal. We said: there's a bunch of weird stuff going on.  
... nav timing + resource timing are a package.  
... safari implement some but not other. (yes http://caniuse.com/#feat=nav-timing vs. no http://caniuse.com/#feat=resource-timing )  
... a series of different styles were used (getEntriesByType). Sometimes you have to go through other means. It's unfortunate and historical.  
... WG is moving a lot of the stuff from nav timing into performance observer.  
... when I read it in TPAC 2015, there still seemed to have a lot of issues. It's still early. Latest draft is at: http://w3c.github.io/performance-timeline/#the-performance-observer-interface. Implementation status on Chromium tracker shows it as early days: https://www.chromestatus.com/feature/5945504202489856  
Travis: might be good to update the title. [Done]  
We should come back to this, but don't need to do so in the short term.  
  
## Issue 38: Browser Fingerprinting Document: https://github.com/w3ctag/spec-reviews/issues/38  
mnot: saw that an update was published, but it didn't incorporate alex's feedback.  
david: nick doty should be CC'd?  
alex: wondering if we would use this doc in our guideance?  
hadley: says that the TAG has reviewed  
alex: perhaps we should ask them to remove our name?  
mnot: [reads that there was concensus in email and draft NOTE was published following TPAC]  
dan: they seem to think they've addressed our issue--perhaps we should just send them a note.  
hadley: one of our points was the title seems to imply we're teaching folks how to fingerprint.  
... this is not the W3C telling you how to do it.  
Andrew: yeah, something like "fingerprinting risks guidance?"  
hadley: did they talk about publication when we sat with them  
dan: I seem to think so. We asked them to move forward rather than wait. Could be my fault :-)  
alex: So we should get to consensus...  
hadley: It's hard to get work done in an interest group. I recall nick getting to the point where he'd done all he could and asked to publish.  
Travis: Alex you will comment on this issue?  
Alex: yeah, just need to review and see what changed.  
Alex: looks like it's mostly identical; have pinged our review thread and opened an issue on their repo to plead for discussion at an upcoming telecon: https://github.com/w3c/fingerprinting-guidance/issues/9  
  
## Issue 42: CSP: https://github.com/w3ctag/spec-reviews/issues/42  
Travis: Looks like we just need to do a review?  
mnot: yep, is a refactor in terms of Fetch and modularization.  
... also reducing the verbosity of responses.  
alex: would this these be breaking syntax?  
mnot: possibly.  
alex: in the past we've talked about other options for setting capability limits for actors.  
... e.g., x-frame-options or sandbox for iframes, limit the set of things that sites can do. This is odd that it has nothing to do with CSP  
... makes it hard, 'cause you have to use multiple syntaxes which use different terminology.  
alex: Can keep assigned to me, would be good to have Mike to discuss as well.  
Travis: This should be added to required reading?  
[agreement]  
  
## Issue 49: Credential Management API: https://github.com/w3ctag/spec-reviews/issues/49  
Mnot: travis said he'd get to it... we should discuss at this f2f.  
travis: right.  
mnot: when Mike is around.  
Travis: I should be in a position to chat about this later.  
Alex: any cannonical example of how FIDO works with Credentials?  
Travis: Not that I've seen.  
  
=====================================  
  
# Topic: Revisiting deliverables:   
  
## Packaging on the Web https://github.com/w3ctag/packaging-on-the-web  
dan: not sure I have much to add, except I haven't documented the new requirements  
... new probject in Gov. Digital Services: called [censored]  
... services for canonical list of things (like list of country codes)  
... list of Schools in the UK + some info about those schools. Data that can change and possibly change often, but it would be one unified list shared amongst agencies.  
... idea: to provide the data, and allow multible agencies to download it, you want to be able to optimize for speed, etc., but in the face of an update, they can reference the changes/diffs.  
... seemed like something we talked about (partially?) in packaging on the web.  
... wondered if POTW would fill this need.  
mnot: about to be frank: POTW seems like a solution looking for a problem  
alex: the signing use case is useful.  
dan: I'd like to make an official statement and shelf the work, rather than let it just sit out there.  
... it's a pretty completely constructed document. Appears legit, promotes a lot of questions.  
... we need to be clear that it's shelved.  
alex: devil's advocate: the reason my team hasn't pushed harder is to only work on feature that don't have to have an alternate origin model.  
... aside from some version of sub-resource integrity with a manifest sub-module, this might be useful?  
... we have at least one implementation. This will continue to come up.  
... we can say there aren't more than one interoperable implementation. This might be enough to defer folks.  
mnot: we can say that the time's not right for it.  
alex: we can't say that.  
mnot: it would be bad to fish around for a justification for its existance.  
yves: one of the original use-cases was for optimizing delivery, but with HTTP2 we've moved away from that.  
hadley: signing, as a use case, isn't in the doc...?  
alex: we didn't include it, but planned for it originally (so that it could be added).  
mnot: are there any concrete next steps for it?  
yves: was published as FPWD, then that's it.  
alex: I'm don't want to see it get kicked away yet, since there's one implementation.  
yves: it's not a big issue to keep as it.  
.. I can update editor's use case, to say that the perf aspect is not relevant anymore, but that the signing aspect is something we're looking into.  
mnot: I want to have a conversatoin with marcos about it. Otherwise, we can defer this discussion to later.  
yves: digi-pub group looked at it, considered it, but given lack of stability assurance on the doc, they weren't confident to use it.  
  
   *   
  
   *   
## Design Principles https://github.com/w3ctag/design-principles  
Travis: We've seen some good mileage from this document.  
mnot: someone on the current TAG should own and drive it forward.  
Travis: I believe I volunteered to drive it, though I haven't made any progress on it.  
Mnot: question is how much do we need to do to publish a first edition.  
plinss: should we publish as a note in TR?  
yves: like the security-questionnaire.  
mnot: let's look through the issues and decide which ones should be addressed before publishing first-edition Note.  
Travis: Sounds good, I can bring the results to the group at a following telco. I'll create an issue.  
  
<scribe name and shame: slightlyoff should have been scribing>  
  
## Security Questionaire: https://github.com/w3ctag/spec-reviews/issues/77  
https://www.w3.org/TR/2015/NOTE-security-privacy-questionnaire-20151210/  
alex: do we have consensus on if we should use this in our reviews?  
hadley: no, I don't think we did...I'm concerned about applicability to some of the features I work on  
alex: security and privacy are things we have to look after. A doc that allows us to say "here's how you do it" is useful. You can still use the questionare as a starting point for discussion. If there are specifics of the questionare, then we should address those.  
alex: I can think of a could of specs where this security questionare might be useful. Counter-examples?  
hadley: data on the web, spatial data on the web and semantics? They're... content.  
... Where this questionnaire uses the term "data", it's focusing on data describing the user's behavior--which isn't always relevant for some of our specs. We should be as helpful as possible.  
... Though I'm all in favour of using this kind of questionnaire for the kinds of specs it's expecting.  Checking you aren't compromising user data is important.  
alex: this is a tool to apply to browser APIs, but not suitable for client implemention.  
... I could support something that says: "if you're building a feature that's not a browser API, then feel free to skip this, but tell us why."  
... Might also be helpful to treat this as a pattern for future self-assessments.  
... next steps? Go back and add language at the top for applicability.  
hadley: secondarily: the doc hasn't been updated since April of 2015, and I have a vague memory that we had some issues about the content?  
alex: who's going to follow up with Mike?  
mnot: we'll talk to him tomorrow.  
... I can take this on to ensure we don't drop it.  
<and there was much celebration>  
  
Alex: we need a doc for "how to work with the TAG" that we can wordsmith together  
hadley: plus our selection of tools/forms for self-assessment.  
plinss: we have a few things already on the home page.  
[interlude while we nit-pick the various TAG web sites and their relationship to each other]  
  
Scribe: hadley  
  
## Promises Guide: https://github.com/w3ctag/promises-guide (does it need any update?)  
  
Alex: Promises haven't changed in the past year.  We may need to update this when async and await support ships.  
... There are many proposals for taskQueues and the ability to order work in those queues.  
Travis: If we're going to take that one, we'll need to do that soon.  
Alex: Everyeone uses the queueTask language from HTML  
David: and there is stuff there that's known to be wrong.  
Travis: is the nanoTask timing from custom elements in that?  
Alex: NanoTask is a new time. This happens a lot; we get a capability, and ti wants to carve out a new time. So we look closely and establish a new time, or we pile it into something already there.   
...In most casese that works fine.  
Hadley: context?  
...setTimeout is the traditional DOM API for creating a way for the browser to call you back in the future. in milliseconds.  
Travis: so the conceptual model is that the setTimeout API puts something into a task.  
Alex: Beause this is a single threaded environment... the main thread...   
Hadley: Why does it have to be single threaded?  
Travis: legacy heritage from original JS decisions...  
Alex: and browsers are single threaded. But worker can have their own thread... and they can only interact with the main thread when breaks exist.  
Alex:  It's like the Streams thing; no one else really has the view on this.  In this case, which timing to use. We haven't given them a contructive way to think about ordering work that's in the queue.  
dbaron: Ojan (?) and others brought proposal to Houdini in Paris in August to define a bunch of the rendering pieces.  
dbaron: but also business of everybody adding their own queueing mechanism  
alex: and people want to prioritize the things they put in the queue  
dbaron: e.g., requestIdleCallback  
Travis: Let's create an issue and assign it to me. I'll start by gathering information on it. [Created: https://github.com/w3ctag/spec-reviews/issues/100]  
  
  
======Lunch=====  
  
  
  
   * ##Report Card (update? close it and declare success?)  
   *   
https://github.com/w3ctag/extensible-web-report-card  
https://github.com/w3ctag/extensible-web-report-card/issues  
Hadley: I remember dka asking what we wanted to do with this in a previous f2f...  
Travis: It's kind of fun... is it adding value?  I had not heard of it before joining the TAG.  
Mnot: It gets... pretty minimal attention  
dbaron: we could make it get more, but do we want to...?  
Hadley: what are the user needs?  
Travis: Who's the user?  Spec editors/authors? People reviewing what they want to support in their browser? People wondering which spec to go to, within the W3C's collection?  
...I go to canIuse when I need to find that out.  
plinss: Yeah  
Travis: It seems like it could be the archive of our spec review decisions. So we have them, but with closed issues to look at.   
...Do we need to rewrite those issues in another place?  
mnot: We have enough trouble keeping our current documentation up to date  
Hadley: So it sounds like this is a solution looking for a problem...  
mnot: How do we gracefully retire it?  
Travis: Is there good value we need to extract from it? hadley:  
hadley; Since we were talking about tools for spec authors to self-assess, when they come to us... is there content here that would be useful for that?  
Travis: Maybe. But i almost don't want to over constrain their possibilities.  
alex: The TAG tries to be on the record about good practice...  Has those efforts been effective?  
Hadley: Do we have spec editors coming back to us with the same questions, acros different documents?  
alex: We give a lot of the same advice  
hadley: It feels like we don't have a sense of the user needs. What we're trying to accomplish, for whom.  What was the catalys for it to be written originally?  
alex: We wanted a "state of the extensible web". Since then, many things are improving.  Not all. It's been useful to track where to have conversations... but I don't know if we've done it in a structured way.  
...We've talked about using upcoming specs to trakck what we should pay attention to.  
...It's a pull model, right now -- people come to us and ask.  
...As opposed to us being more proactive.  
...Hard to tell if that's effective?  
Travis: There is certainly a heavy emphasis on the extensible web manifesto, in this. Grading specs against it.  
...It's a good design principle, that should be talked about in the Design Principles doc.    
...I feel like we could condense it down to one screen of data...?  
alex: I think if we're not enthusiastic about it, then we shouldn't continue to do it.  
mnot: I think it's served its purpose. We're past the Extensible Web being new.  
hadley: Does anyone disagree with these views, that his has largely passed its utility?  
all: no  
mnot: What's the next step?  If this disappeared tomorrow, would anyone notice? Do we have usage stats?  
plinss: <checking> Excluding bots, probably <1 person per day on average.  
Hadley: that's pretty clear. What do we do... put a "no longer maintained" label on it?  
Travis: shall we ask Dan to briefly voice his thoughts before we unplug it...?  
Alex: I think some TAG members have been surprised at the state of some of these features... Perhaps we should pull out some issues and track them in github.  
...I'll do that.   
  
  
dbaron: Interestingly, if you search for "extensible web report card" on google, you get the github repo, not the actual site.  
  
   *   
  
   * ##Private Mode  
   *   
Travis: We have 15 issues.  
mnot: I think I owe everyone a pretty substantial revision of this doc... and I'm in a good place to do that now.  Will be ready for review before London.  
...It'll be lightweight, a target to point to for other specs to work with.    
...The key will be the guidance we give to spec authors.  
...Last we checked, all the browsers consider an on-machine attacker (person using the machine after you) to be a good threat model for privacy mode.    
...But they don't agree on protection from server attacks... Browser fingerprinting makes that one hard.  
  
  
  
  
   * ##Privileged Contexts   
   *   
alex: The draft has been working its way through. There have been changes landing in Chrome, at least, to remove iFrame capabilities.   
...Restricting powerful capabilities to things like secure connections only. And making sure you can't abuse a securely connected iFrame from an insecure context.  
hadley: So what do we need to do?  
alex: let's ask Mike West when we speak to him tomorrow.  
<added to the agenda>  
  
  
# Spec reviews (cont)  
  
## Credential management  
  
https://github.com/w3ctag/spec-reviews/issues/49  
  
travis: I'd like to fill this out more tomorrow, when we talk about FIDO.  I propose skipping for now.  
  
## CSSOM View document.scrollingElement #51  
  
https://github.com/w3ctag/spec-reviews/issues/51  
  
dbaron: My memory is that some browsers scroll the document when you change the HTML elements scrollTop or offsetY.  Some browsers reflect that on the HTML element; some do the body element. No one can change because all the code on the web accommodates that.  
Travis: Also, browsers all this quirks mode in addition to this rendering behaviour...  
dbaron: legacy as in pre-2001 content  
plinss: Netscape 4 content.  
  
alex: The blink proposal seemed like a reasonable endpoint  
...  
plinss: The main problem is we don't have a common understanding of what a viewPort is  
travis: Still today? Fullscreen has had to deal with this.  
plinss: CSS took an action at TPAC to try to refine this.  
travis: will that be a prereq to any layout boxes, coordinate representations, stuff like that?  
plinss: i'ts part of the Houdini work to explain the route of the presentation.  
travis: are you designing for the idea that presetnatiosn may be different, separate or split -- in houdini?  
plinss: Houdini should be exposing the full presentation model, as a presentation model -- eventually  
..But that wil lbe disconnected from these DOM APIs.  
travis: it's a ship that has sailed for me.  
plinss: And there are all sorts of DOM APIs that are presentational, and shouldn't be in the DOM.  
  
travis: The blink team has already shipped this. And Edge copied it and shipped it.  
plinss: So this issue is just overtaken by events.  
alex: I'll write comments and close the issue.  
  
## contributing.md document needed for tag reviews #53  
  
https://github.com/w3ctag/spec-reviews/issues/53  
  
travis: didn't we say earlier we want to work on this?  
...Where would this go? on our homepage?  
hadley: We deferred that discussion to later in the week.  
  
<deferred>  
  
## Presentation API Request for Feedback #61  
  
https://github.com/w3ctag/spec-reviews/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-asc  
  
Travis: I need to respond to them.  
... They are one of the potential consumers of the Private Mode spec, if/when we have one.  
...For instance, "I need to start up this second screen, and I want it to start -- clean."  
...So in Dec, we agreed to ask them for specific requirements for Private Mode, to put that in their document.  
...Will contact them today and close the issue.  If needed, we'll open a new one.  
  
## Sketch out proposals for event synthesis/flow and reusable a11y behavior #63  
  
https://github.com/w3ctag/spec-reviews/issues/63  
  
alex: This comes from Berlin.  #  
...We should try to get Cynthia and Alice/Domenic in this... try to get a sense of the state of the art.  
Travis: Our feedback would be, at this point, extensible web-related.   
alex: Maybe we should try to reformulate this in terms of talking through WAPA maybe? The goal is to understand how events flow through the system and end up at high-level a11y stuff, so WAPA proably overlaps.  
Travis: Initially this was an opportunity to brainstorm. Perhaps we don't need to proactively seek those out, just start with the WAPA proposal.  
...So this becomes the spec review issue for reviewing the Web Script-based Accessibility Spec: https://github.com/cyns/wapa  
...I'll write the notes and change the issue name.  
  
  
## Cross-spec device identification \& association #64  
  
https://github.com/w3ctag/spec-reviews/issues/64  
  
alex: The thoughts in the issue thread are a good start... on things to think through. Not a "here's how to do it".    
travis: Yesterday, I heard all our connected devices should be web servers, have origins and names.... Sounds counter to the guidance we've written here.  
alex:  We don't have a problem with that.  There are specific APIs being proposed which don't take a RESTy approach to their API access; they're much more direct access. We expose them to script directly.  
...In some cases we are grandfathering them into the origin model.   
...For example, bluetooth.  You don't automatically pair things; you have to choose what you pair to which website.  
...With USB and the service discovery... They're not speaking HTTP.    
dbaron: You're passing origins around as strings to say who can access something?  
travis: it's like you've got local storage but it's on the USB device, so you have to have an origin model to protect that data.  
dbaron: so grandfathering/shoehorning isn't derogatory?  
alex: No.   
...Bluetooth doesn't do this, but it does explose this device ID.  Device ID is a separate issue to the origin question -- but we should find a way to find/expose these device IDs as they come and go.  
...in WebRTC, if you clear your cookies, your devices apparently get new IDs.  
Travis: I recall this coming up in webRTC and Media Capture groups. You have two competing use cases: those building RTC protocols into devices, and it's a fix ed reltionship between the software and the hardware on that device. There isn't a reason not to just know the ID for, for example, the camera, and use it every time.  Versus for example, a web browser, where you want to reduce a fingerprinting opportunity, so knowing a device ID b etween sessions or between two web pages in the same session... is a threat.  
...So I know how this applies to a fixed hardware or pluggable device. If it's now applied to bluetooth ("give me all the bluetooth devices", and you get a list of identifiers) -- same with NFC -- or local web server devices  
Alex: or MDNS devices  
travis: Do we feel this is a good idea? having al lthese apis for asking for devices?  
alex: yes. I do  
hadley: I do see the vulnerabilities.    
alex: what common properties should they have?  
...You were talking about "session".  If that ID isn't valid across sessions...  
travis: that breaks the persistence.  
...If you derive an ID, which takes into account the origin... For example, if I go to Facebook and it enumerates a list of the devices, and I come back a week later -- those IDs are still cached and relevant for Facebook.  But they're not relevant if I'm accessing it through a different device, or for another web site wanting to know what devices I have.  
dbaron: So if I clear cookies, will they reset?  
travis: We want to keep the user in control.  
dbaron: Agree.  So need to be careful it's something random that a user agent stores per-origin, rather than, say, something computed with a hash function.  
Travis:  And they need to be relatively unguessable.  
...They start to sound like the crypto properties we need for strong hashes.  
...So, this list of guidance points...   
...Should we integrate this with our design principles document?  
...And that could basically end this issue?  
peter: We should put a reference to it in the security questionnaire too.  
travis: in the security questionnaire?  
hadley: prefer leaving the security questionnaire as a set of links to things maintain elsewhere.  (Assuming those pieces ARE maintained elsewhere)  
  
Travis:  I'll take this action then.  
  
<Gelato break (temperature outside is 40C)>  
Scribe: dbaron  
  
## Motion path spec  
  
https://github.com/w3ctag/spec-reviews/issues/66  
peterl: I think we had feedback, and I was to take it back to FX task force.  We're meeting in Sydney in a couple weeks, so I'll bring this up there.  
  
## requestIdleCallback  
https://github.com/w3ctag/spec-reviews/issues/70  
dbaron: I gave some feedback; I should probably go through the responses  
alex: a little concerned about your first comment  
dbaron: probably more about spec wording than concept, so probably not a big deal  
alex: multicore shouldn't be issue; javascript is single threaded  
dbaron: what if enough workers to saturate cores, might want to not run idle callbacks then  
dbaron: and some of my concern that just things were a little overspecified  
dbaron: also a little concerned about a different set of long timer IDs  
dbaron: https://html.spec.whatwg.org/multipage/webappapis.html#dom-window-requestanimationframe does sequential IDs different from setTimeout  
alex: chromium code does that  
dbaron: I guess this is something we're stuck with, probably, though not crazy about it.  
travis: would these APIs have been written as promises today?  
alex: distinction here is that promise resolution has a defined timing  
dbaron: did some spec define promises that resolve at a different time?  
dbaron: I guess I should read rmcilroy's comments more closely, and then maybe close it?  
dbaron: only other question is whether we want issue #100 to affect this?  
travis: wrap up into issue #100  
  
# CSS font-display  
https://github.com/w3ctag/spec-reviews/issues/71  
dbaron: currently lack of interop and lack of interest in interop  
plinss: but willingness to have a property to let author override.  
plinss: Is this one just done?  Editors commented on feedback in our issue.  
alex: did they add the examples we were looking for?  
alex: I see text examples, not code.  And don't see an explainer.  
travis: section 1 not bad as an explainer.  
plinss: Hasn't been edited to reflect our feedback.  
alex: mark it for a future ? for followup  
  
## task scheduling  
https://github.com/w3ctag/spec-reviews/issues/72  
travis: oops, looks like we just created a dupe of this at #100  
  
## Secure Stop  
https://github.com/w3ctag/spec-reviews/issues/73  
already on agenda for later (as "Secure Release")  
alex: would rather talk about it on Thursday  
  
## Unblocking HTTPS transitions  
https://github.com/w3ctag/spec-reviews/issues/74  
mnot: Brad had his proposal; had spec drawn up.  
mnot: failed to get implementor interest.  
plinss: had discussion at TPAC  
mnot: some hopeful noises  
mnot: doesn't seem to have momentum; also doesn't seem to have a venue; WebAppSec doesn't seem to want to do it  
mnot: from TPAC, next steps maybe to decompose mechanisms being proposed so they weren't necessarily used at the same time  
mnot: Brad doesn't have a lot of time to work on it.  
mnot: mkwst suggested we get Brad as well; have them both tomorrow 9am  
dbaron: not sure how well understood proposal is; seemed clearer to me verbally in joint WebAppSec/TAG meeting Berlin than in the write-up  
mnot: Making a fairly complete proposal; new ALPN token that creates a new security context.  
mnot: I'd be willing to do more work, but not without serious consideration for implementation  
plinss: so discuss tomorrow morning when they're on the phone  
  
## Secure Contexts / Powerful features  
https://github.com/w3ctag/spec-reviews/issues/75  
also talk tomorrow morning  
  
  
## With Credentials flag  
https://github.com/w3ctag/spec-reviews/issues/76  
mnot: TimBL's issue, he discussed a bit with annevk; I discussed with annevk as well.  
mnot: Tim needs to justify a little more  
Yves: If you can't figure out whether it's ??? then you can't figure out whether the server is .... then you have to link to not just URI but URI plus credentials.  
mnot: ... saying not consistent with Web architecture to have fetch have a flag (with credentials) for whether it's cross-origin; wants it to be calculated automatically  
Yves: ... a bit like an API  
mnot: you didn't have to do that  
mnot: so why is this architecturally bad?  Strength of URI is that stick URI into application.  But application does know context.  Maybe Tim misunderstands nature of fetch; not really and end-user-facing API.  
Yves: different from regular web page, running in specific .??? context  
plinss: the with credentials flag is about how the url is used  
mnot: legitimate to have something about how URL is being used  
mnot: but we can't resolve this without Tim in the room  
Yves: .... is it to hide the fact that it's security through obscurity?  
alex: ???  
Yves: would it be possibe to have 2 different kinds of errors:  unknown not-transport-level error, vs. could reach server  
Travis: sounds like layering violation  
alex: if I'm trying to provide a UI, I'd like to say what might be going wrong  
travis: at that level, you know what you need  
alex: I mean Web site ui, not browser ui.  
Yves: Is it good to have didnt-reach-server vs. didnt-get-what-wanted exception?  
alex: to be clear, we're talking about special case of cross-origin non-CORS requests  
travis: Tim would say that with-credentials part not included ...  
Yves: If not able to figure out whether real network error, then libraries would ... having proper error miht avoid leaking that information  
travis: scenario is I request resource and get denied -- then maybe I need to do a CORS request?  
Yves: You don't need to know if it was denied or not found -- just reach server and there was an error.  
Yves: You have a core interaction that failed -- at fetch level coul djust report that getting what you wanted failed  
mnot: would anything but CORS produce this kind of error?  
Yves: you don't need to know if it's a CORS error to hide the fact that it was really denied,   Goal of fetch is to hide that info; everything is a network error.  
alex: XHR has same behavior.  Scenario:  trying to cross-origin request, with with-credentials flag.  Even if sets allow-access...: *, still won't get response or know what happened.  
travis: not what I understood  
alex: that's what Tim says in the issue  
mnot: I wonder if tim knows it's not an end-user-facing flag  
alex: it's exposed through XHR and fetch  
alex: that's how this came up.  
travis: XHR was not a networking-level problem, ... application layer policy that said you're only allowed to talk to your origin  
travis: so application layer created other thing that says unless you provide exception and handshake and right headers...  
alex: a couple oddities here.  Starts at which requests get CORS and which don't.  
alex: some implicitly or explicitly invoke CORS, some don't.  It's defined, but may not be reasonable if you're trying to programmatically access things.  
alex: I think issues bottoms out at:  some requests can be made to use CORS, some use by default, some can't be made to use CORS, even if you want them to.  And that is probably the original sin here, but it's fallen off the stack for me which is which.  
travis: example of something that needs CORS and will implicitly have CORS enabled is module loading.  
Alex: fonts always use CORS  
alex: images never use CORS  
travis: script is configurable  
alex: how?  
travis: user can supply the attribute that says to use CORS?  Or maybe not?  Maybe only DOM and not markup.  
alex: crossorigin attribute  
alex: do images have crossorigin attribute?  
travis: link, script, media, import  
plinss: crossorigin images and tainted canvases  
alex: possible to invoke for images  
alex: always for fonts, possible to invoke for script  
travis: sounds like we're retrofitting most things that use resources to have the option of using CORS  
alex: can't tell from issue whether CORS values Access-control-allow-credentials vs. access-control-allow-origin are part of the debate  
alex: would love to see network trace and code snippet that's not working for tim  
mnot: as I understand it, he just doesn't want to have to send the with-credentials flag when he'se requesting data from a different site  
mnot: I think he wants to not have to know.  
alex: I think what's going on here -- if he sets credentials for every request, some will be automatically denied -- don't recall which is which.  
alex: maybe we should ask annevk  
plinss: get tim and anne on a call at the same time??  
alex: would be nice to have an enumeration somelpace of the states, and odd to me that this fetch spec doesn't have anything like that  
mnot: spaghetti  
travis: cross-origin for anchors?  
mnot: we need a fetch explainer doc  
alex: I don't think it exists.  
mnot: I've thought about it, but worry it'll change on me.  
dbaron: what does crossorigin on script do  
travis: lets you get script error messages  
  
Adjourned for the day, cooler weather tomorrow.  













