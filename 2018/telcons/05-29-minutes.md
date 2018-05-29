## TAG Teleconference
##### 29 May 2018

Present: Kenneth, Daniel, Travis, Trevor (WebXR), Kearwood Gilbert (WebXR), Alex, Hadley, Yves, David

Regrets: Peter, Sangwhan

---

Agenda:

* [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - @slightlyoff @hadleybeeman @travisleithead @plinss

Q: Has the TAG feedback been useful?
Q: What's the current state of things?
Q: What's up with Gamepad? Old gamepad vs. new gamepad?

Kip: My first time (excuse any ignorance). Gamepad was blocked on certain parts of WebXR were not opened up yet, but that's now unblocked. Gamepad spec will build on new XR objects. XR is changing the inheritance model in a way that doesn't really work with the old Gamepad spec.
There would be some form of configuration on the user's machine, and Content will express how things will be mapped.
XR will not depend on it enough.

Dan: Concerned about there being two gamepad..

Alex: XR didn't use gamepad for the past. Enumeration has been a major sticking point. I asked Brandon for why there would be a diversion (if necessary). Brandon reported that retrofitting Gamepad for 6 degree-of-freedom input would not be a good fit. Because coordinates are head-relative, it didn't really work for the existing infra.

Kip: Gamepad extensions also exist (primarily for desktop). Enumeration of gamepad identifiers--is that consistent between various specs? Would love TAG feedback on that.

Alex: Had a similar question around Bluetooth/USB about device id. We wanted to avoid shared identifiers which can be used as supercookies. We might have had a recommendation about.

Hadley: Yeah, I was particularly concerned about expanding the fingerprinting surface area.

Travis: leaking device id outside of origins is fingerprinting concern.

Kip: Poses as unique identifiers (if you leave a controller in one spot) two requests to access a controller can collaborate to identify a controller, which is a fingerprinting concern.

Alex: https://github.com/w3ctag/design-reviews/issues/64 was our earler issue.

Dan: Should we be focusing on the existing Gamepad review if its not fit for purpose?

Kip: would be nice to share some IDL so that Gamepad gains some of the same features that are useful outside of VR, like touchpad and vibration.

Alex: if gamepad could inherit from interfaces you're defining, that could be good harmonization.

Kip: Noticed one item... framerate and subframe timing. Might relate to iframe/perf topic. We purposely avoided disclosing framerate of the device, and encourage use of existing rAF. One difference of rAF in XR is rate can be variable--what matters is how long the frame took. Sub-frame
timing is important and should be submitted early. Ex: Occulus desktop framework can go from 90 FPS to 45 depending on factors--even change several times per minute.

Travis: how is frame timing identified

Kip: timestamp is passed in, since perf.now is not reliable (cite quantization mitigation from Spectre/Meltdown).

Alex: Trying to repair the damage re: quantization and SharedArrayBuffer since we have Process Isolation.

Kip: WebXR in Workers (which is necessary to maintain perf benefits).

Dan: How WebXR interacts with other web content? 

Kip: What should other content do when in XR? Considerations for Perf and Security. In Security, want to avoid ... Perf: would expect browsers to prioritize XR exclusive content over other background content. Curious how this would be done?

Alex: Lots of content (generally) wants to be in high-performance mode. Content that wants to ramp-up perf, run on GPU, ensure other content goes to background. This is "exclusive" content. XR content scenarios where you are 'co-presenting' 

Kip: multi-tasking scenarios might be exception. Simple ex: open spotify playlist in background tab, then switch to VR content. Maybe fewer scenarios where framerate is critical.

Trevor: page is presenting tethered VR headset: has content for headset and content for the rest of the folks to see the 2D content.

Alex: Looking for a way to provide a hint at a frame level, for the platform to enter high-performance mode. Is this useful? 

Kip: for XR, we can be sure exclusive content is wanted. Like Gamepad, are we just solving this for ourselves, or more generally?

Alex: in the past, we've had various fast-paths, and there is some concern around having a flag. Browser might have to disagree with the flag...

Kip: concern is that we might have different heuristics that we have to depend on. For XR, this is explicit, so we don't have to solve this for the whole web. Don't see the added benefit for "we need more performance" flag. Exceptions (possibly): GPU context selection. Web page might be 2d until user interaction turns it 3d--would have liked to have been on the right GPU from the beginning. Would have liked to see "anticipation" for future high-performance mode.

Alex: Interesting! Wondering what the urgency is for this? Should continue to discuss? Due to time: are there any specific concerns we can help with?

Trevor: Any other issues where TAG has issues about not getting enough performance.

Kip: asking about whether we're giving the users enough choice on how to [not] drain their battery?

Trevor: there was some concern about isolation...

Alex: chatted with Brandon... might have to give-up on idea of [...]. Maybe a feature-policy concept?

Alex: input routing? Go from one document to another. If you want isolation, it must be at a document-level. At the time, we were wondering if XR is embedded in a document (a part), or is it bounded by the document. Seems the only rational way of doing this is by document-level (iframe) isolation.

Kip: might be true that XR content will be more of a "part" of a document--but I would expect this content to be using isolation via iframes.

Trevor: would like feedback on how navigation in XR is done (staying in XR).

Daniel: Is there is a link capturing cross origin VR linking. We have some architectural considerations here regarding origins etc. Thanks to the Web XR members for their participation.

* [Web Components Guidelines Doc?](https://github.com/w3ctag/design-reviews/issues/227) - @kenchris

Daniel: lets do a workshop at the F2F

Kenneth: Incorporated the feedback that I have got, but would like more.

-- meeting ending --


* [CSS Selectors 4, :focus-visible.](https://github.com/w3ctag/design-reviews/issues/233) - @plinss @dbaron @travisleithead 
* [Payment Handler pending external feedback](https://github.com/w3ctag/design-reviews/issues/231) - @slightlyoff @dbaron @hadleybeeman
* [Permission Delegation In Progress](https://github.com/w3ctag/design-reviews/issues/225) - @dbaron @torgo @lknik
* [ReportingObserver pending external feedback](https://github.com/w3ctag/design-reviews/issues/195) - @cynthia @slightlyoff
* [`sec-metadata`](https://github.com/w3ctag/design-reviews/issues/280) - @dbaron
* [TV-Specific Web Subsetting](https://github.com/w3ctag/design-reviews/issues/105) - @torgo


---