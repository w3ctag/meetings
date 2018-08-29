## TAG Teleconference
##### 28 August 2018

Present: Kenneth, Dan, Peter, Yves, David, Sangwhan, Hadley, Travis, Alex

Guests: Chris Needham, Ali C. Begen, Cyril Concolato, David Singer

Regrets:

---

Agenda:

* [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @cynthia and guests
* Followup - Proposed TAG role in W3C-WHATWG relationship - Dan
* Followup - Proposed workflow for privacy & security questionnaire - Lukasz


F2F Backlog
* [DOM](https://github.com/w3ctag/design-reviews/issues/229) - @cynthia @dbaron @travisleithead
* [Web Components Guidelines Doc](https://github.com/w3ctag/design-reviews/issues/227) - @kenchris @travisleithead @plinss https://kenchris.github.io/web-components-guidelines/
* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff @dbaron
* [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @travisleithead


---

TOPIC: [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285)

_introductions and connection issues_

Sangwhan: looks like you're trying to solve a particular problem, perhaps you can describe the problem and we can discuss potential solutions from there?

_more connection issues_

Cyril: previously we were only able to synchronize events through <a message bus?>. We should be able to synchronize through a single event system. We didn't wnat every system to need to register their own type of event. We ended up with a carrier-agnostic way of providing htis metadata in an MP4 file because that's what ATSC is using.

Cyril: one approach, instead of having folks build their own JSON/XML/etc. formats, the idea was to have the format carry web-style events. So we started drafting the document you've seen that envisage 3 or 4 types of HTML events. One type of event is the display of the event over the video. <scribe missed second>. A third type of eent was VTT content. A 4th was a text-content event; in the context of a web page, the ==page would decide waht to do with it. AThe idea is that a piece of text would be given in the file to allow synchronization between audio and video and cctext content.
  
Cyril: because you might need to synchronize with non-timed content, we're using a feature of the MP4 feature to carry non-timed metadata. We're solving a problem for ATSC. We had some feeddback from several people about security issues related to JS in MP4 files. We've restricted that so much now that we're considering removing it.

Sangwhan: the propopsal we saw has perhaps been updated since we first reviewed it?

Cyril: when was that?

Sanghwan: a few months ago

Cyril: then yes, it was updated. We update them at every cycle (for every meeting)

Sanghwan: we should probably look at the latest

Dan: are there updates that address any of the issues we raised



?

Cyril: not sure who sent it, but someone mentioned a few points and we tried to address them. O fne was the security aspect. The processing of the track to fitput them in their own browser context.

Dan: based on an origin model?

Cyril: we have put the JS in a separate context. You also mentioned origin. We have a way for the MP4 file to contain metadata indicating that it came from a location other than the server that provided it. So we've made those URLs now relative URLs.
Sangwhan: butbut only over the internet?

Cyril: or ATSC broadcast. I don't know what the origin would be, but all of the resources will be relative to that origin. My understanding of ATSC is that they use Dash and the origin would be the base URL of the Dash document

Sangwhan: another question; one of the drafts I've seen puts web resource s into MP4 "fragments"...

Cyril: Mthese can be both fragmented and unfragmented. the new track format is agnotic to fragmentation

Sangwhan: the resources you can contain feel very restricted...what's the plan for scaling? It feels very much like a filesystem

Cyril: this is untimed data. HTML, JS, CSS, PNG, etc. Whnen it should be processed at a given time in a timed resources, we'll put a them in a track and they'll be pulled/evented when the time passes. The other data is untimed. That data has naems and paths, and looks very much like a filesystem

_trying to get access to a shared, non-public document  ; discuss "brand"_

Cyril: there are many contexts., and every file has a brand. The brand may be exposed in the mimetype. We're defining them in the document to indicate out of all possible files you can create, a restricted type. E.g. "HTMI"

Sangwhan: "HTMT"?

Cyril: "HTMT" signals the presence of an HTML track, "HVTT" for VTT,  (etc. etc.).

Sangwhan: what about Web Assembly?

Cyril: this would go in the 4th bucket; general text

Sangwhan: but WASM isn't text?  I have concerns about how this will scale.

Kenneth: It is binary, MIME type is application/wasm - https://webassembly.org/docs/web/

Cyril: it can carry formats that aren't text as well

_philisophical outline of how/when ISOBMFF adds newpab capabilities_

Sangwhan: if this was done with web packaging, the browser can handle the unpackaging

Alex: having timed resources is a new thing for us on the Web. We generally come from a untimed background, so this is a different format from how we originally work.

._questions about what the two different contexts are attempting to do_

Cyril: there are 2 ways of perhaps framing this iand we're trying to define a second method rather than time being encoded in the HTML document.

_connection issues for David Singer_

Cyril: if David were able to connect, he'd be able to talk about his favourite use-case, the presentation. YOu'd have 3 tracks, one for the HTML slides, one for the audio, and one for the video.

Sangwhan: imagine you have an untimed application that gets events 

Cyril: at most, there are 4 time-update events per second (scribe missed the context)

Travis: I have concerns about how a media engine will run the wwlifecycle of a web page in practice. Not all web pages are created equal. Pages go through complex phases when they start, fetch resources, process them, etc. You could perhaps miss every single timed queue if fetchign a resource takes too long

Cyril: we have that conern too, similar to audio/video processing. Audio/video frame decoding is bounded, but variable. So we have to do some work ahead.

Travis: I agree, audio/video arououe bounded. THe web case isn't.

Cyril: limiting the complexity of the page to be loaded would have to be done inith side the application, e.g. an ATSC profile for this sort of content.

Travis: so you'd need a policy or a change to the HTML engine to enforce those limits

Cyril: defining that is out of scope for us, butsd dsstandards bodies will have to take it up. PCs, phones, etc. will all have different profiles

Kenneth: those things change over time, though?

David: (scribe missed)

Cyril: in a Dash session, there's no cheating in the URL, but when you're receiving it overan ATSC broadcast there's no URL. SO the manifest can provide a base URL or an alternative base URL. That's out of scope for MPEG, though.

Sangwhan: _secure context point_

Cyril: if you're considering an MP4 track with HTML in it, you should consider secure context about the path where the file came from. If you're getting it over the network, if it has TLS

_discussion of definition of secure contexts_

Dan: if we don't define the secure context container, this content won't have access to expanded capabilities over time

Alex: perhaps these could be lieke `<iframe sandbox>` content toside-step the problroblem?

S_time check_

Sangwhan: Question is also when a video is shared via Netflix but not created by Netflix, should that video content have access to Netflix's cookies?

Sangwhan: what'll happen here if we don't define secure contexts is that someone will taka  ae Chromium or WebKit and tressat _everythign_ like a secure context, which will endanger user privacy and security. We'd like to help if we can.


_discussion of HBBTV and embedding contexts_

Sanghwan: HBBTV lets you inject a web application, which is quite scate scarry.

_discussion of how to follow up_

Hadley: I was wonderring about the motivation to not do this work in the open?

David Singer: that's an ISO issue. We've been as open as we can, but it's an org-wide issue.

