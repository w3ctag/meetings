## TAG Teleconference
##### 26 June 2018

Present: Lukasz, Kenneth, Peter, Travis, Dan, Hadley, David, Yves, Sangwhan, Alex

Regrets:

---

Agenda:

* [Reporting Observer](https://github.com/w3ctag/design-reviews/issues/195) - @cynthia @slightlyoff @dbaron @travisleithead @plinss
* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - @plinss @dbaron @slightlyoff @travisleithead @cynthia
* [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - @slightlyoff @dbaron @hadleybeeman
* [CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - @dbaron @travisleithead @plinss
* [Carriage of Web Resource in ISOBMFF ](https://github.com/w3ctag/design-reviews/issues/285) - @cynthia
* [CSS Logical Properties and Values](https://github.com/w3ctag/design-reviews/issues/286) - @dbaron
* [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288) - @slightlyoff @travisleithead
* [Request.isReloadNavigation and Request.isHistoryNavigation](https://github.com/w3ctag/design-reviews/issues/289) - @cynthia @travisleithead
* [Cookie Store API ](https://github.com/w3ctag/design-reviews/issues/290) - @hadleybeeman @travisleithead

---

* [Reporting Observer](https://github.com/w3ctag/design-reviews/issues/195) - @cynthia @slightlyoff @dbaron @travisleithead @plinss 

Travis: the argument was made that structured headers can't do the nesting that is needed.

Yves: one issue from httpbis repo - they consiered json and said they couldn't use it (comma issue)

Travis: I believe Alex was pushing this to give the green light to use json - Alex wants to get this moving forward to wih json. I'm concered this is precendent setting (first time json in a header)

Yves: http community struggled with cookies because of .. probably don't want to repeat that mistake by allowing [unencoded] json in a heading. an array of values ...  Structured headers don't have that problem but they avoid the nesting part (which is hardest part). From what I read from the discussion from Mark they were wndering if the nesting int he spec was the connnanonical one...  Be good to get a follow-up.

Travis: that's where Yasskin's last comment was  --- asking if we can change the format.  

Peter: 3 options - use json,  remove nested structure, change structured headers to allow nesting (or make something else that can), [or....]

Yves: base-64 json, http-escaped json...

Travis: what action to move it forward?

Sangwhan: q: does structured headers have wide enough adotption to make it in impossible to change? I don't think so. More things will use this.

Ken: they are using it in web packagaging - has anyone asked if they can support nesting?

Peter: it's not unreasonable to ask- doesn't look like part of their design.  

Sangwhan: we make it ietf's problem

Hadley: Mark says [unhappy] - memory limitations - "it's necessary to limit the nesting.." - he seems to have thought about nesting that found it's a bad idea.

Sangwhan: throwing json in the header won't reduce the memory usage...

Travis: there could be an arbitrarily huge structured header...

Alex: do we have any reason to hold this up? is thee new data?

Travis: no

Alex: then let's unblock it.

Hadley: there could be ramifications

Alex: we've got structured headers [web packaging] - there will be decoders for both that and json... the [right thing for this seems to be json]. Doesn't appear to be a clear mapping for this into strtcyred headers.

David: someone should make the point about proxies and concatenation of headers - otherwise I am happy to unblock it.

Travis: what's the encoding we would use? what encoding to avoid comma issue etc...

Alex: I don't think we have to raise the issue - what are they gonna do about it.

Dan: can we do that and close this then?

Peter: let's make sure we capture the feedback - have we opened an issue in their repo?

[sounds of searching]

Hadley: on the subj of encoding - the spec has a reference to "json encoding for http header values" - https://greenbytes.de/tech/webdav/draft-reschke-http-jfv-02.html

Alex: there is some question of how pervasive are structured headers going to be - but ..

Travis: but can't support he use casing 

Alex: you could fully denormalise everything... but it does seem unfit for purpose. If we strand them by saying json is ok - that could happen if stryctured headers comes back with a solution...

Hadley: I'd agree with the fact that neither option looks good.

Peter: what do we do

Yves: we can get mwest to follow-up we can unblock some things.

Travis: i think t's fine to say "we're uneasy with json but given that they'd like to move forward - we are ok"

Yves: for the tag review - the only issue is this and it's not really about the spec in general.

Travis: i don't think we are gonna fix the problem.

Dan: 

Alex: I'll summarize and close?

Yves: will summarize

Alex: we'll leave it open for next week.

Peter: we'll set a milestone - 2 weeks

* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - @plinss @dbaron @slightlyoff @travisleithead @cynthia

David: I took a look yesterday - Alex & I had had a discussion 2 momths ago - I didn't see anything too major. The new design seems [good] -I looked at the wrong version

Ken : I also looked tat that version - it was the one they shared with us

David: the up-to-date version lives in a PR - once the PR is merged it would be good to have a look. Someone should look at the newwest version before I close.

Peter: wait until they merge it?

David: I'd be happy to see it merged.

Sangwhan: i think the comment is dealt with.

David: in the very last comment there is a link to [the latest version](https://pr-preview.s3.amazonaws.com/ewilligers/web-share-target/pull/40.html)

[agreed to come back to it in 2 weeks]

* [Payment Handler](https://github.com/w3ctag/design-reviews/issues/231) - @slightlyoff @dbaron @hadleybeeman

David: where we were - there was along list of feedback - and responses - need to reconcile

[agreed to bump 3 weeks]

* [CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - @dbaron @travisleithead @plinss

Peter: they were going to update the spec..  

Travis: closed 11 days ago...  Alice saying "for now we're gonna close this while we figure out..." So maybe not closed conclusively here.   Let's loop back in a few weeks.

[bumping]

* [Carriage of Web Resource in ISOBMFF ](https://github.com/w3ctag/design-reviews/issues/285) - @cynthia

Sangwhan: can we do a call with the people behind this? 

Dan: we can do that in one of the next 2 calls

Sangwhan: so having cleared that up... it allows web content to be embedded in video, and within a video via fragments - and video fragments to load time-domain resources within a video package... this has many issues. They are reinventing a pseudo file system in the packaging format. Also using fragments to ... breaks fetch compatability. No notion of what the origin is. Nothing about secure contexts. Many issues. 

Dan: Isn't this trying to solve some of the same problems TTML is addressing?

Sangwhan: possibly ... lots of questions of how the ... mime types...

Alex: should we ask them to look at the web packaging work?

Sangwhan: Yes, that sounds like a good idea.

Alex: that seems like the easy way to easily address their use cases.

Sangwhan: (Given that it's ready) packaging solves 80% of what they want.

Hadley: some other concerns in mind?

Dan: Can we tell them before the call that we're thinking about packaging?

Sangwhan: i do have a list - im planning to write that in the github issue.. what is going to do when it recurses, etc... also a question about a technical detail...

David: it's worth focusing on the parts of the web that don't work [along with their design]

Hadley: [evergreen](https://www.w3.org/2001/tag/doc/evergreen-web/) concerns as well?  We wrote a finding - updadable user agents - response to hbbtv subsetting html.

Sangwhan: there is nothing about subsetting in there though effectively it's about subsetting

Hadley: we should make that explicit

Sangwhan: i will write up a helpful and friendly tag review & circulate. and will set up a call.

* [CSS Logical Properties and Values](https://github.com/w3ctag/design-reviews/issues/286) - @dbaron

David: I went through and filed 6-8 issues in their spec.  I am capable of following up on these issues. we could close...

David: a few pieces missing in the spec. .. i'm happy with where the spec is going in general.

Peter: close?  anyone else want to take?  We do have the problem of the css members on the tag doing ht review of css work...

Peter: [so mote it be]

* [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288) - @slightlyoff @travisleithead

Travis: haven't reviewed yet 

Dan: bump?

Travis: yeah 

* [Request.isReloadNavigation and Request.isHistoryNavigation](https://github.com/w3ctag/design-reviews/issues/289) - @cynthia @travisleithead

Travis: I did review - not a whole lot to it - i don't have any objections

Lukasz: The user has previously .. the result

Alex: the site can already know whether the user has visited it.. they times when you can see this data - the user in the same session - there is a moment here for user agents whether or not to send this session.. an amnesiac browser might never set these flags to true. It is telling you something new about how the user got to the site. .. 

Lukasz: information about how the user got to the site - in this case - navigating from... 

Alex; yes:

Lukasz: per site - there 

Alex: yes, it's limited to site - no additional info available except...

Sangwhan: there has been discussion on the backlog of developers want to know if it's back or forward navigation... this has changed.  Developers want to know back navigation (history or back). Html histroy algo doesn't differentiate this. If developers want specifically back and forward, this isn't addressed here.

Alex: that is the new data provided - are you going back or forward - some larger systems will already discern this data via heuristics (a side channel).

Dan: is anyone from Tor browser or other people focused on privacy-focused browsers involved? 

Alex: Yan at Brave would be the person to reach out to.  However : this is data that the sites already get.

Lukasz: how would that work in ...incogtonito mode

Alex: chrome creates an in-memory profile - and when you leave incognito mode we just throw that info out - it should work transparently. 

Lukasz: ...

Alex: we don't neuter APIs in incognito mode in chrome  - we don't attempt to reduce what APIs deliver

Hadley: Safari sandboxes per tab in private mode...

Alex: that would aloo work - whatever your storage lifetime is that it .. if you sandbos more fully you will reduce the frequency - never delivered on first navigation. 

Hadley: really useful.  are there other browsers?

Alex: this was designed in the service worker working group -  and all service worker implementors are aligned.

Peter: if you had a service worker in regular mode and then you go into incognito mode, then there is no carry-over.

Alex: yes it woudl be a new registration.

Peter: you wouldn't leak the service worker information between service workers..

Alex: that's correct.

Lukasz: api works exactly the same whether youre in incognito or not

Peter: yes - just that the info is scoped only in that session

Travos: suggesting we drop a note about his privacy related discussion.

Lukasz: yes

Dan: I'll do that (and close the issue)

* [Cookie Store API ](https://github.com/w3ctag/design-reviews/issues/290) - @hadleybeeman @travisleithead

Hadley: they haven't got back to us

Alex: I can nudge them

Peter: bumped to next week.

[adjourned]