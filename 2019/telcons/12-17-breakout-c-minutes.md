### TAG Breakouts - 16 Dec 2019

https://github.com/w3ctag/meetings/blob/gh-pages/2019/telcons/WO-16-december.md

* MathML Core - @alice, @torgo, @hadleybeeman
* Serial API - @cynthia, @kenchris
* [Payments] shipping and contact info delegation - @dbaron, @torgo, @kenchris
* CompressStream - @cynthia, @ylafon, @plinss
* WebTransport - @cynthia, @dbaron, @ylafon
* WebHID API (Human Interface Device) - @cynthia


#### [Serial API](https://github.com/w3ctag/design-reviews/issues/431) - @cynthia, @kenchris

Sangwhan: posted an internal review...  checked the baud rate issue that has been resolved... don't understand buffer size .. don't udnerstand flow control. Even common term emulators don't support...

Ken: they are not updating the draft... they are pointing us to chromium.org version...

Sangwhan: I am also not entirely sure if getinfo bit should expose the raw serial number. that makes me uncomfortable.

Dan: is that a fingerprinting issue?

Sangwhan: yes, clear-cut...  exposure of raw serial nmbesers...

Ken: maybe ask what is the use case for knowing the serial number...

Sangwhan: yes I don't see the use case.  They could do an origin hashed serial number that are not cross-origin trackable...  It is written down. How to hash it is unclear to me...  I did write that per-origin unique would be acceptable. [Last commnent](https://github.com/w3ctag/design-reviews/issues/431#issuecomment-566419859) on 431.  This brings up a meta question of extremely unique high entropy identifiers... 

Dan: Design principles issues?

Ken: a bit like private / private key.. public one is the address...

Sangwhan: we don't want to implement this multiple times... but with the fugu stuff coming in we do want something like this.

[opens up design principle issues]

[discussion on web serial open topics]

Dan: what status?

Sangwhan: i will re-enforce my comments but not ready to close...

#### [MathML](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

Alice: when I spoke to Brian - he said he didn't know what Hadley is missing. I agree with her comment. I need to talk to Brian again about what is missing.  I want it to explain what the core of MathML is and why I would use it.  I get the basic idea of what is the bare minimum. 

Ken: does it say what they are removing exactly?  This is the core, but what are examples of what is not included in the core? Removing useless things? Or things you can accomplish in other ways?

Alice: Was going to build on that... i don't know about mathML - a couple of examples liket hat would be useful, but also : what would be more useful - a building up - all of these math elements in the XML part of the MathML specification - it might be possible to buildit up from a worked example.

Ken: like figure 1 in the explainer... 

Alice: no context given for the figure.  Explaining the figures, providing more context for the figures.. also, how to use the core features ot build up to these complex examples.  What are the new CSS features that they are proposing?  This is a very meaty, complex proposal.  I want like a tutorial on mathml core. At one point do we say "this is too complex to review as a stand-alone thing"?

Dan: what has helped is to ask for feedback on prioties...  also focusing in on the dependencies between this and other specs, eg. CSS.

Ken: already have browsers implementing all of MathML.

Sangwhan: this spec touches on stuff that's not interoerable.  

Alice: we could specifically ask for feedback on ... that.  We can clarify Hadley's comment. I can have a go with that.  Dan you wanted to clarify the CSS properties they are asking for...  Sangwhan wanted to ask about interop.

Sangwhan: in an ideal world you would be able to design custom elements and not have special magical new tags to define math...  

Ken: actually a lot of sites using mathML... 

Sangwhan: many using Katx or MathJax.

Ken: we are supposed to review...

Sangwhan: feels contradictory to what the XWM says .. at least in this c

Alice: i think it's a false dichotomy.  I've seen some of the commentary you're refering to...

[discussion of extensible web manifesto and whetehr it means everything should be built up...]

Alice: we need both.

Dan: do we need a clarify extensible web manifesto?

Sangwhan: it's low level and high level...

Alice: a lot of accessibility tools consume mathML directly.

[discussion on accessibility & mathml]

Ken: by the way all of this is implemented in chromium... [by igalia]. (fork)

Dan: does MathML core address the issues raised in the initial review?

Sangwhan: i have mixed feelings.

[discussion of LaTeX math ...]

Alice: we want the DOM version of a MathML thing to 

Sanfwhan: this is a box layout model defines as a markup language. I don't know what this improves.

Alice: the horse has bolted a bit.  It would be nice if we could get the features of stylability, extensibility.. without having to have all of this markup which is difficult to deal with...

#### [CompressStream](https://github.com/w3ctag/design-reviews/issues/410)

[discussion of IANA registration]

Ken: Intent to ship... has got approved... 

Dan: can we close this?

Yves: i can comment... on the IANA issue... and clarify things in their repo as well.

Dan: and then close?

[consensus to close]