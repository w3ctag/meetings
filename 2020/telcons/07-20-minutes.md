## TAG Teleconference
##### 20-22 July 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20200720T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @kenchris, @plinss
* [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss
* [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris
* [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron
* [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss

#### Breakout B (US / APAC) - [2020-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20200720T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477) - @hober, @cynthia, @dbaron, @hadleybeeman
* [Behavior of the "disabled" attribute for HTMLLinkElement](https://github.com/w3ctag/design-reviews/issues/519) - @hober, @alice, @dbaron
* [CSS Overflow: scrollbar-gutter](https://github.com/w3ctag/design-reviews/issues/520) - @alice, @dbaron, @atanassov
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov
* [Storage Pressure Event](https://github.com/w3ctag/design-reviews/issues/533) - @dbaron, @plinss

#### Breakout C (APAC / Europe) - [2020-07-21](https://www.timeanddate.com/worldclock/converter.html?iso=20200721T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo


* [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris



* ["display_override" field addition to the Web Manifest](https://github.com/w3ctag/design-reviews/issues/530) - @alice, @dbaron, @torgo, @kenchris
* [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris
* [WebRTC Insertable Streams](https://github.com/w3ctag/design-reviews/issues/531) - @hober, @cynthia, @ylafon

#### Plenary Session - [2020-07-22](https://www.timeanddate.com/worldclock/converter.html?iso=20200722T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Voice our approval for new text in [AB issue on communication](https://github.com/w3c/AB-memberonly/issues/34#issuecomment-647021744)
* Issue Triage


-----


### Breakout A

Present: Peter, David, Dan, Yves, Rossen

Regrets: Kenneth, Tess, Hadley

#### [Screen Enumeration API](https://github.com/w3ctag/design-reviews/issues/413) - @hober, @kenchris, @plinss

Bumped to next week.

#### [Window Controls Overlay for Installed Desktop Web Apps](https://github.com/w3ctag/design-reviews/issues/481) - @torgo, @kenchris, @plinss

Dan: requested access to the s&p document...

Rossen: I explained some of the concerns - Amanda did say that the spec and proposal are being worked on. They are definitely addressing the privacy & security concerns. As a result the doc has info... I'll ping.

[bumped to next week]

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris

[bumped to next week, David to take a look at it]

#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @dbaron

David: smaller breakout with Tess required?

Yves: I sent mail to webappsec working group to ask if they were interested in helping but have not heard anything back.

Peter: schedule breakout time for tomorrow?

David: Will try sometime this week.

#### [WebAssembly js-types API](https://github.com/w3ctag/design-reviews/issues/532) - @hober, @kenchris, @plinss

[bumped to next week]


### Breakout B

Present: Alice, Peter, David, Rossen

Regrets: Tess, Sangwhan

#### [Media Feeds API](https://github.com/w3ctag/design-reviews/issues/477) - @hober, @cynthia, @dbaron, @hadleybeeman

Peter: What is the browser meant to do with the feed?

David: there were some links... seems like it's to show e.g. recommended YouTubes?

Rossen: Interesting that audio-only feeds are explicitly a non-goal...

Peter: Are any other browsers interested in implementing this?

David: Mozilla is probably unlikely to be interested.

Peter: Who else is participating in WICG? Looks like Marcos has made a few comments..?

Alice: There was a comment from Chris Needham...

Peter: I would agree with that feedback... especially the comment about restricting a site to a single feed, not everyone has control over the site (?)

... Also, yet another feed format when we already have RSS, Atom etc.

Alice: I think that was the gist of the [issue](https://github.com/beccahughes/media-feeds/issues/10) Tess filed.

... danbri commented that JSON would indeed be preferable, with lengthy reasoning.

... Intent to ship was sent, although not clear whether it will actually ship.

Peter: What should we do with this?

Dan: ... I should respond to this from Mozilla Standards Positions, but that's not a TAG thing...

Peter: A high-level concern with this being a whole new thing... pushback on "why not use X" where X already exists... would like to see a richer feed format which works for everything, if existing feed formats don't.

... I also share Chris Needham's concerns.

... Would be good to understand whether there has been significant participation outside of Chromium.

David: Does this affect privacy-related UI in browser? Browsers have UI to show users what's going on with their information, how does using cookie information in a context that's not obviously a web page influence that UI?

Rossen: What use case do you have in mind for this?

David: Browser goes and starts fetching the feed on its own, not associated with any particular tab. Browser making cookie requests outside the context of a tab feels a little weird to me.

Rossen: Could this be done for push instead?

David: (missed)

Rossen: The security and privacy questionnaire... what information is exposed? Answer is "no information exposed to the website", data flow is the other way around... 

Peter: So, what do we want to do with this?

Rossen: Comments have been fairly reserved, no strong push-back. This is getting ready for shipping, seems like the shipping ship has sailed... only remaining question is whether this is truly a standard.

Peter: So, do we raise yet another issue about this being a one-off feed format?

Rossen: Doesn't hurt...

Peter: Is there an open issue for Chris' privacy concerns? I don't see one...

... I'll file an issue and ask Chris to share his concerns...

#### [Behavior of the "disabled" attribute for HTMLLinkElement](https://github.com/w3ctag/design-reviews/issues/519) - @hober, @alice, @dbaron

David: Much smaller feature in an existing, interoperable spec.

... I replied to Emilio's comment, the status quo after the change in question seems like a reasonable compromise given the constraints.


... We should look at the specific issues Mason called attention to?

... I'm inclined to think we should close this issue... the reason things are ugly is compat, and people have tried to make it better and done what they could get away with compat-wise.

Peter: Propose closing, close at plenary?

David: sure.

#### [CSS Overflow: scrollbar-gutter](https://github.com/w3ctag/design-reviews/issues/520) - @alice, @dbaron, @atanassov

Rossen: Propose closing?

Alice: Sounds good.

Rossen: I'll comment and update the label.

#### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521) - @hober, @alice, @dbaron, @atanassov

Rossen: Main hiccup is between things that want to interact with timers/capabilities such as prefers-reduced-motion. 

Alice: It's a tricky one. 

Rossen: I don't believe we have a good answer based on discussions in CSSWG so far.

Peter: There's an issue on CSSWG - should we make this pending feedback?

#### [Storage Pressure Event](https://github.com/w3ctag/design-reviews/issues/533) - @dbaron, @plinss

### Breakout C


Present: Hadley, Alice, Dan, Sangwhan

Regrets: Kenneth


#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo


Alice: they haven't responded to questions yet...

Alice: if you've got something on a table and you create an anchor from a hit test result and you move the table around then the object on the anchor moves around...

... And then there's XR Frame ...  Each returns a promise.  I asked in my feedback why it was a promise.  The answer is it might need to ask hardware for it.   The API is minimal. The API seems fine. 

Yves: Can an anchor be shared?

Alice: Is it serializable?  Based on the explainer I would say no.

Yves: wouldn't it be better if it was serializable and have a URL for it?

Dan: I think it only makes sense for one AR session?

Yves: use case would be for sharing a place with someone else... Might be out of scope.

Alice: `XRframCreateAnchor` takes a reference space and a pose. I imagine what you'd need to create a duplicate anchor would be the pose, assuming the same reference space. 

Dan: it's worth asking.

Alice: can we give them feedback - investigage what the thought process is when people are writing explainers. We get a lot of explainers that are writing with us as an audience.  In this case the explainer doesn't seem to be written with us as an audience because it's written with knowledge of XR assumed.  It would be interesting to understand - what do they understand the purpose / audience to be?

Dan: we could be more direct. The purpose of the explainer is $this, and the audience is $that. it's in the explainer explainer, as I said to the AC. The audience should be web devs, but those who may not be knowledgeable about your thing. It starts with the user need. This doc could then be adapted to material for this API, like an MDN article. 

...We've seen this issue, of assuming domain knowledge, with a lot of other reviews. 

Alice: yeah.. with some nuance.. a lot of people have been forced to write explainers because of our process. We have an audience we can encourage to write explainers before they come to TAG.  When they ask for a design review it could be too late.  We're getting explainers out of the XR group.  They're a group that wants to do the right thing.   So what's their process given that the intentions are good?  Also with this issue I filed about IDL - what can we  do to make that process less confusing.

Dan: I'll chat with Ada [group co-chair] about it today.

Alice: Now that I've had it explained multiple times by people - other than Yves's comment... My other question would be are there any other members on XR anchor other than Anchor Space? It seems like it's a holder for the anchor space... In which case why have the `XRAnchor` at all? Why not have a subclass of `XRSpace` which would get us out of this naming collision as well.


#### [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris

Sangwhan: multiple things that describe a viewport... one is generic .. not enough..

... 2 viewport APIs...

... one or the other should be deprecated ...

... two parties pushing similar things - one by MS and one by Goog - similar technologies...

... visual viewport work hasn't been updated...

... at least one implementer (Apple) has strongly come out against this proposal...

Dan: could we encourage the parties to come together?  Maybe reference SMS receive API as a  good example of this hapening and creating something better and more widely implemented?

Sangwhan: will get in touch with Kenneth as well to discuss....



#### ["display_override" field addition to the Web Manifest](https://github.com/w3ctag/design-reviews/issues/530) - @alice, @dbaron, @torgo, @kenchris

Dan: I wonder if David would be happy to close this based on their updates to the explainer? Let's bump to the plenary?

Alice: for accessiblity - it would be interesting if something is stand-alone or full screen thwn you don't have access to the browser UI.

Dan: that's general.

Sangwhan: yes - a general issue that hasn't been touched on.

Alice: it cuts both ways.  I've heard from some screen reader using that thye don't like focus moving nto browser chrome... needs more thought.

Sangwhan: it effects people.  Payments had explicit stuff on what browsers should be able to do.

Dan: note - as part of the work on updating the docs in MDN https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps I've asked for Leonie's input. 

Alice: I'd be surprised if the result came back as something other than "the web doesn't have as rich accessibility support as native apps". My day job is trying to fix that.  It's difficult because of privacy.

Hadley & Dan: [express alarm]



#### [IndexedDB putAll](https://github.com/w3ctag/design-reviews/issues/536) - @torgo, @kenchris

[reviewing]

Sangwhan: indexdb has this thing called put - people have been asking for "put many things" - so you have to have a for loop, which blocks. If you have a huge amount of stuff you want to put in and then get an event at the end there is no solution for that. This is one of many things like this. Because of legacy reasons they don't want to move away from an event based architecture (vs async). So I brought that up. The original IDB editor commented. There was an atteempt to try that but it didn't succeed.  

Dan: so more to do ... on our side. 

Sangwhan: some archeology.  The naming issue isn't so much of an issue.

Dan: sounds like a reasonable request...

Sangwhan: yes, it doesn't seem nice [the way it is]. 

[bump]

#### [WebRTC Insertable Streams](https://github.com/w3ctag/design-reviews/issues/531) - @hober, @cynthia, @ylafon

Dan: [reviewing explainer]

Yves: they are using transform streams.. semems good.

Sangwhan: the pattern stuff is fine, the use cases are fine... does it interact with anything other than WebRTC?  The answer would seem to be no.

Yves: possibility to hide computation-intensive processing here... bitcoin mining.

Sangwhan: why do we not have video/media worklets?  Audio has audio worklets.  WebRTC has their own thing.  If you want to do video preprocessing in a worker or service worker there's no nice way to do it except at bitstream level...   

Dan: Where could it be?

Sangwhan: HTML media...

Yves: transform streams... 

Sangwhan: latency requirement was a real problem.  you don't get the latency guarantee.  

[bumped]

### Plenary Session

Present: Peter, David, Rossen, Alice, Tess, Yves, Hadley

Regrets: Kenneth, Dan

#### Voice our approval for new text in [AB issue on communication](https://github.com/w3c/AB-memberonly/issues/34#issuecomment-647021744)

Peter: Dan asked us to sign off on the comms document. (all looking at the doc)

Alice: What does "role models for the CEPC" mean?

Tess: Ppl in leadership positions are expected to be excellent examplars and howld themselved to higher standards.

Peter: ... don't want us to be an example for unexpected behavior "so and so did that on TAG/AB etc."

Alice: CEPC guidelines (new version) look a bit vague.

Peter: Feel free to file issues against it.

Alice: quoting paragraph 3 "As a member of an elected body". 
... LGTM modulo what it means to be a role model of the CEPC

Peter: Want to leave feedback?

Alice: Sure but someone else should since I have no access

Peter: I'll leave it for you.

#### Breakout Rollup

##### Breakout A

Rossen: It was short due to lots of deffering. 

David: The one we didn't defer (#525) needs a dedicated meeting.

Tess: Next week is csswg vf2f, so that means past August.

David: Sept if you want me for it.

Peter: David, given you'll be out in August, want us to push anything else?

David: Not really

Rossen: I'll help with #525

##### Breakout B

Rossen: **Media feeds API**... pretty lengthy discussion. 

... Issue raised by Chris Needham. Feeling during the discussion that this feature is targeting a somewhat narrow use case. At the same time, it's opening a new capability that wasn't exposed previously. Potential impact to security & privacy, mostly driven by the fact that the user agent has the capability to fetch media lists from a given service using user auth, and drive that feature.

... Could we make that more of a push instead of a pull? This was likely discussed on one of the issues on their repo. WE'll raise another issue on github.

... Feed doesn't accommodate audio-only feeds...

Peter: I think I filed an issue on that...

Tess: I think I filed an issue ages ago?

Rossen: **disabled attribute for HTMLLinkElement** - feature is fairly well worked through, couple of issues that were addressed by Emilio and Mason. General improvement to compat here that is going to be the ultimate effect of the [?], proposing to close this one.

David: I wrote a comment during the meeting.

Peter: Are we good to close this?

Rossen: **scrollbar-gutter** - previous comments had been addressed, happy to close.

... **Scroll-linked animations** - what do we do WRT prefers-reduced-motion? Broader issue is currently being worked on at CSSWG.

... Need to work out how to thread the needle of what animations to support, how to define what types of animations to suspend.

.. e.g. animating focus rings is very useful, and can be in line with reduced motion needs.

Peter: didn't get to the **storage pressure event** issue.

Tess: I can jump in on that.



##### Breakout C

Alice: Started out talking about **Web Anchors module**.

...You can get a frame of reference relative to an opbject so you can put something in front of or next to an object and have the things move together. I'd asked for examples. The response: You've got this anchor, and the explainer doesn't seem to think it can be shared.

Yves: I left that feedback

Alice: Long chat about the explainer. And my follow-up feedback: This XR anchor object is just XR space... wondering why we needed anchor objects.  Haven't heard back yet. 

...**Virtual keyboard API**: Initially they wanted an event, and we asked whhy not make it a CSS environment variable. So they added one. But Sanghwan pointed out that visual viewport seems like it would be a more generic solution to that problem. But it hasn't been updated in a while... So the plan was to try at get both teams to talk to one another and figure out if there is a common solution possible.

...**"display_override" field addition to the Web Manifest**: We talked about how this might impact accessibility. Doesn't directly. Purpose of the API is for stand-alone web apps with a manifest. Display types fall back one to the next, but order becomes unclear so they want authors to be able to set the order in the manifest. The accessibility impact is orthogonal, like the impacts of using an web app for full-screen vs in the browser. It can go both ways. Recently heard from a screenreader user re focus moving... which isn't covered in a spec right now. Writing a spec would be tricky. Sanghan pointed out the Payment API had some language on this. Even though we didn't come to consensus on this because we got distracted, it seems like a good candidate for closing. Unless there are objections to the concept?

dbaron: Yeah, there was a lot that wasn't clear to me. They've improved the explainer, which is substantially better now. Clearer how they intend this to be used. I'm okay with closing this. 

Peter: So we close?

Alice: Yes.

David: I'll write a closing comment.

Peter: should we track the discussion from C?

Alice: Dan is starting a discussion with Léonie about that. 

Peter: Let's ask him what comes of it and how to document the issue(s).

Alice: **IndexedDB putAll**: Bumped to next week.

Yves: **WebRTC Insertable Streams**: We discussed the options in their explainer. We noted they are using transform streams, which is a good thing. Discussion about how audio worklets are the same thing...maybe due to history? Latency? Would be good to investigate that.

...For Insertable Streams, there was a issue on how it could be used to hide big computations like mining. But otherwise it seemed interesting.

...And we bumped it two weeks.



#### Issue Triage

* [Pointer Events Azimuth Angle and Altitude Angle](https://github.com/w3ctag/design-reviews/issues/537)

Hadley: I'm intrigued...

Tess: Add me please.

* [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538)

Tess: Add me and Rossen.

Hadley: Me too please.

#### Scheduling our next F2F

Please reply to the doodle (see slack)