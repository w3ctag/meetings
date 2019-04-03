## TAG Teleconference
##### 03 April 2019

Present: Kenneth, Lukasz, Dan, Hadley, Peter, Sangwhan, Lukasz, Alice, Yves

Regrets: Tess, David

---

Agenda:

### [Audiobooks](https://github.com/w3ctag/design-reviews/issues/345) - @hober, @cynthia, @dbaron

Sangwan: I've looked into this. It's a playlist format, with a bit more. An M3u file plus more. Specificially type 2 audio, while it seems liek it would be related to the ISO BFF web resource packaging would be interested in as well. There is no synchronisation, and there is no 'web' in here. So... it feels like this is a very specific fetaure, but it could fit in to a lot more use cases that they don't seem to be interested in.  

I commented: if you do a regex from MP3 to MP4, you've basically just defined the DVD chapter format. A bit weird.

And just no web stuff in here.

Hadley: How did it come to us?

Sangwhan: they used the manifest format they defined for web publications. Subset of publishing... the manifest can have arbitrary resources, including web content. Audiobook part is publishing packages, but only for mp3 files.

I feel like this is a bit short-sighted. 

Dan: Is there anything un-web here? Different identifiers besides URLs, etc? HOw is this different to RSS?

Sangwhan: It's JSON instead of XML

Dan: I@m not sure that the criticism that it's not webby... Is there a more webby approach that we can suggfest they take?

Sangwhan: Not criticising that, just a basic remark. There is the entry page which is hte bare minimum.  Looks like this would have to be repeated for video, and other formats too. That concerns me.

Hadley: So you'd rather it be done in a generaliseable way?

Sangwhan: Yeah, the publications part is general, and the audio files is a specific use case. But video will have to reinvent their own thing, which is currently ISOBFF, and I'm not convinced that's the best way to do this. 

So I'd like to see these two efforts merged. 

Hadley: Makes sense to me. 

Dan: It does seem like... in their considered alternatives, they have this one thing about ePub 3 audiobooks, and they don't explain why they're not doing that.

Sangwhan: Agreed. I'll add that to the issue. 

Dan: Do we need a really specific... It's great to have a teasing-out-the-requirements-of-audiobooks... but do we need something specific to them?

Sangwhan: this is a subset of functionality that they're doing.

Dan: I'm going to be in really cold Canada next week, and I might try to chat to Tsviya... and get a bit more context.

Sangwhan: This is a valid use case for video, so I'd like to explore that. 

Kenneth: Who would be using this?  Apps like netflix for audiobooks? Audible?

Sangwhan: Basically Americans. I think they use their own thing, (probably some variant of) the pocket mobi format. 

Dan: What is the use of audiobooks worldwide?

Sangwhan: They're more common in America because of the drives.

Peter: agreed

Kenneth: and then they need HTML at that point?

Sangwhan: You'd use HTML to push a button to say "play chapter 2"

...I will write feedback; Dan you talk to Tsviya -- and let's talk after that.

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @dbaron, @torgo

Dan: Comments from mkwst. David (who is not here today) had some comments. Does anyone have feedback? Or should we wait?

(Hears silence)

Alice: Looks like mkwst had some plans to do work on the explainer, might take some time.

Dan: Any time sensitivity?

Alice: Probably not.

...Punt for two weeks (when David is back)

JUMPBACK:

Lukasz: I will write feedback about this on the issue.

Dan: Might be useful to mention the use cases. With the new restrictions of 3p cookies on the platform, there are considerations that should be taken when designing features like this.

GOTO PORTALS;

### [Portals](https://github.com/w3ctag/design-reviews/issues/331) - @hober, @cynthia, @dbaron, @kenchris, @travisleithead, @plinss

Ken: David summarized a bit. 

GOTO JUMPBACK;

PORTALS:

Ken: Two big issues, why is this not an iframe, tried on Chrome but didn't work out well. FP didn't work well for Portals. The explainer needs to be clarified why it can't be an iframe, also there was the part about double keyed cookies. Some comments on the 

Sangwhan: When you jump into the portal by throwing out the existing state it won't work..

Ken: kind of the point...

Sangwhan: i don't know about others but I feel like this is rather inellegant.  We've done so much work - one weird element iFrame that we've spent a lot of time making it work. 

Ken: they are trying to work around restrictions with iframe but ...  really really good explanation of why this is not an iframe. and how they are going to solve these points of different specs refering to iFrames.

Sangwhan: Wonder if there will be other cases aside from AMP that would benefit from this.

Kenneth: Commerce might, Denmark has a bunch of third party payment handlers running on different origins.

Sangwhan: That feels like web payments would be the solution, doesn't feel like the right tool for this.

Dan: Parenthetically: there is an advisory council about AMP which some signers of the AMP letter  have been a part of. If anyone is interested I can explain later. 

Kenneth: Explainer could use a bit more detail on use cases. Should ask for a update.

Alice: There is a key scenarios link from the original request.

Ken: "nice transition" \[as a key feature]

Alice: use case down at the bottom is interesting - making a multi-page application look like a single-page application.

Ken: you might not need all these things for same originl - so you could make a simnpler solution that works for same origin.

Dan: The provenance of the content has been a constant issue, and a smooth transition could actually obstruct that there is a change of the origin.

Hadley: It feels like a feature to work around SOP.

Peter: If you embed a third party origin as yourself, and then switching over without a transition doesn't seem right.

ylafon: https://github.com/jakearchibald/navigation-transitions

Dan: We have provided feedback, whether or not that is enough and whether this is addressable is something we should follow up on.

### [Verifiable Credentials Data Model 1.0](https://github.com/w3ctag/design-reviews/issues/343) - @hadleybeeman

Hadley: There are a bunch of issues here; the scope of the WG's charter suggests a pure data model, but there is nothing about how the rest of the infrastructure works. I'm curious how this fits into the web. Travis had a bunch of questions, and especially in particular about the benefits over a widely deployed DID infrastructure. Whether or not this is something we need to deal with.

There are some use cases that make sense; a claim which is verifiable. Not sure if this solves a bunch of unsolved problems that exist. Would require market traction for this to work.

The issues Travis raised are quite valid, the group suggests it is out of scope. Would like to discuss this a bit more next week though. They have a list of implementors, none of which are browser vendors.

### [Carriage of Web Resource in ISOBMFF](https://github.com/w3ctag/design-reviews/issues/285) - @hober, @cynthia, @torgo


Dan: I'll (hopefully) discuss with next week during the AC meeting.


* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-
reviews/issues/318) - @hober, @alice, @dbaron
* [IndexedDB Transaction Explicit Commit API](https://github.com/w3ctag/design-reviews/issues/316) - @cynthia, @kenchris
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @torgo, @hadleybeeman
* [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240) - @cynthia, @hadleybeeman, @plinss
* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) - @cynthia, @travisleithead, @plinss
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @slightlyoff, @torgo, @ylafon
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @slightlyoff, @hadleybeeman, @travisleithead, @plinss
* [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) - @dbaron
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) - @hober


---



