# TAG Breakouts - 16 Dec 2019

https://github.com/w3ctag/meetings/blob/gh-pages/2019/telcons/WO-16-december.md

## TAG Breakout B (California/APAC) - 2019-12-16 23:00 UTC 

* [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) - @cynthia, @dbaron
* [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @cynthia, @alice
* [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron
* [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) - @cynthia, @dbaron
* [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) - @cynthia, @dbaron


* Present: Tess, David, Alice
* Chair: no gods, no masters!
* Scribe: Alice  

### [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @cynthia, @alice

Tess: Saw there was a comment from @danyao five days ago...

Alice: Yeah, I didn't have a chance to respond yet.

Alice & Tess: [leave comments on the issue]

Tess: Is this ready to close?

Alice: Yeah, I'll comment thanking them and asking them to re-open when/if there's more to discuss later on.

###  [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) - @cynthia, @dbaron

David: This is another early review.

Alice: I'm going to go ahead and label it as such...

Tess: There's a lot of WebIDL, how early is it really?

Alice: Hmm, I think some engineers "sketch" in WebIDL, I wouldn't read into it too much.

David: I think Sangwhan or Yves might have more to say about this.

Alice: Can we add any more labels?

Tess: Hmm, maybe fingerprinting? May give more timing information (e.g. encode/decode timing) than is currently possible from other sources.

David: Trying to read their examples to understand how this would actually work.

.. First example seems to take two streams and send them to the source of a `<video>` element.

.. Is setting the source of a `<video>` element to a media stream an existing thing you can do?

.. Yeah, looks like it is. So I assume there's already some concept of how synchronisation etc. work with this. Lot of complicated things under the hood here. I don't feel especially qualified to have a lot of comments on this right now.

Tess: Yeah, I would need to ask around about this.

David: Contacts at Microsoft, Google and Mozilla.

... Not much more we can do on this today. I should probably try and read it offline.

### [Feature policy evolution](https://github.com/w3ctag/design-reviews/issues/341) - @cynthia, @dbaron

David: I've been talking to folks inside MOzilla about features policies lately.

... We're interested in it for permissions, specifically about delegating permissions to subresources across domains. We're kind of nervous about some of the other uses of feature policy. 

... Specifically, the complexity of the header syntax, and the per-domain allow/deny syntax being not what you expect.

Tess: So you can have the top level document denying iframes... with an exception for itself...

David: You have two subframes, allow for one and deny the other, but the deny subframe can embed something from the allow domain...

Tess: Right - if the embedder denies permission to a frame, there should be no way for a frame to get that thing. Seems like it should be more like per-frame than per-domain.

Alice: My memory is that the original issue did in part concern the confusing syntax.

Tess: Right, so if I read his first point correctly, if you disallow the lazyloading feature, it forces all elements to lazy-load. That seems confusing, to put it mildly.

Alice: Following the links, it looks like `lazyload` has since been renamed `loading-frame-default-eager`.

Tess: Not as concise, but maybe better named.

Alice: Also, no movement on the parameterised feature policies issue yet.

Alice: So looks like there is some groundwork to do here - what is the current spectrum of feature policies? Are the two issues Andrew raised here still a concern? What is Mozilla's eventual public position? What design principles could we propose?

David: Working on filing an issue on our design principles repo about naming. We do have something but I think it could be expanded.

Alice: The other issue seems to be around types and consistency... changing types after the fact, and/or using union types.

David: ... what else should we do about this issue?

### [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304) - @cynthia, @dbaron
### [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303) - @cynthia, @dbaron

Punted.

