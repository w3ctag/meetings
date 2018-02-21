## TAG Teleconference
##### 21 February 2018

Present: Dan, Peter, Alex, Andrew, Hadley

Regrets: David

---

Agenda:

* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - Alex
* [Review of signature-based resource loading restrictions.](https://github.com/w3ctag/design-reviews/issues/186) - Andrew / Hadley / Sangwhan
* [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Alex / Hadley / Travis / Peter
* [OffscreenCanvas](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / David / Travis
* [Review Accessibility Object Model ](https://github.com/w3ctag/design-reviews/issues/141) - Sangwhan / Travis

Last week's agenda (try to get into these or re-assign dates):

* [Secure Contexts & TC39](https://github.com/w3ctag/design-principles/pull/75) - Sangwhan
* [&lt;link&gt; rel=modulepreload](https://github.com/w3ctag/design-reviews/issues/213) - Alex, Andrew
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/213) - Andrew
* [Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/226) - Sangwhan
* [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224) - David, Dan, Travis
* [Decentralized Identifiers](https://github.com/w3ctag/design-reviews/issues/216) - Hadley
* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) - Hadley, Travis
* [Transfrom Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David
* [import.meta.url and import.meta](https://github.com/w3ctag/design-reviews/issues/208) - Alex
* [Accept-CH header](https://github.com/w3ctag/design-reviews/issues/206) - Andrew, Alex

---

### Accept CH

Andrew: Ilya is not happy. Open to suggestions how to engage on this.

Alex: browsers in their initial request sending a hash of some vlaues

Andrew: let'sdig into his argument - he's saying "redirects happen" - part of the web - which is contadictory to

Alex: redirects happen because URLs have meaning. If the URL didn't mean something we shouldn't bother with all this web stuff. He's saying meaning of the URL couldn't be negotiated... 

Andrew: how to do that until that first slew is data is available. Vast number of requests you receive will not havea CH relationship with your origin. Evidence suggest that stored permissions don't last. People get new devices, clear their cashes, UAs might wipe them anyway... Don't know how we can usefully engage.  We said we'd like it to be reconsidered because we don't have ...

Alex: no argument for....   I can discuss with Illia tomorrow. I will do it.

Alex: there's a web performance wg meeting on Friday.  We could join the discussion there.  I see it 8am to 3pm pacific time.  

Andrew: Is it remotely attendable?

Alex: possibly.

Dan: who is the group chair?

https://www.w3.org/webperf/

Dan: let's try to get in that call

Andrew: 20 domains using accept-ch  - 2 from people I know - akamai, vogue in taiwan, jack.io, some random assortment of things... data from 2018-02-01 from Internet Archive

---

### Ads.txt

Alex: I've had 2 meetings now with the Googler involved.  This is being developed [ad hoc and not using open process].  I have a follow-up meeting on Friday.  Receptive audience to improving some of these problems.  By tightening up the question of what an origin is we can handle the TLS problem.  They are arguing for something "simple" to be "human readable" will continue to work...

Hadley: do you think they're a lost cause?

Alex: this is their first standard - they don't know what they don't know.

Dan: Standard process...

Alex: they would say they are not making a standard for the web.

Dan: they clearly are making a standard... I've seen this before in groups with lots of technical experts.   Can we help them with the process?

Alex: [...influence how IAB works...]

Andrew: I think that makes sense.  We should point out to them that their standards don't look like specs - more like marketing document.

Alex: ...and have you considered doing this work at IETF....  

Andrew: if we can convince them that the indented audience are people who will ask "where is the spec" then they will understand the benefit of doing so...

[Alex will continue to prosecute with the ads people involved]

---

### Review of signature-based resource loading restrictions

Sangwhan: I spoke to Mike at TPAC and he didn't want to bring in the whole cert chain, authorities, code signing, because it complicates things.

Peter: I owe mike a response...

Andrew: I am happy with it... One other thing - it has some inetresting crossover with signed exchanges.

Alex: Yes that is my team.

Andrew: have we looked at signed exchanges yet?

[no]

[now talking about signed exchanges]

Andrew: i had a meeting with kenji at google tokyo about signed exchanges - I had a look - it felt like a lot of crossover between signature based integrity and signed exchanges

Alex: maybe.  What if you could capture a request-response and put it in a package. It's the thing that is put inside the package and the thing that is signed.  We are proposing to sign the entire package.  All keyed to the same regular old PKI.  Very much per resource.  Also : what if you had a package of signed exchanges - could you grant it more powers if you knew none of the code in that document came from anywhere else?  The reason kenji is excited about this is to fix some of the issues that have been identified with AMP.

Andrew: I think we should be reviewing.

Dan: can we encourage kenji to request a TAG review.

[andrew to request kenji to request review]

Dan: what problem is signed exchanges trying to solve?

Alex: web packaging - gives you a way to host documents on example.com, as a package over tls - you could know they are example.com's content.  Signed exchanges put a signature on - no matter where on the network you got the content from you can run it as example.com - remember the screen shot at the TAG meeting - distributed syndicated content finding - Rt.com article with a google.com address at the top in the URL bar. What would be best if the browser understood - when it gets content from a 3rd party that it's badged as such [and linked to that origin]. It can be run in context of [the real origin].

Hadley: a massive hack on same origin?

Alex: content-addressed networking that respects the origin model.

Hadley: my head splode.  Use case makes sense. It feels like it could violate user expectaitons in other contexts. If we blow the smae origin model to smitherines.

Alex: we're not - we can respect the same origin model based on the PKI infrastructure - also can time-shift the signing. Now we are saying the content can be signed in the past and then played forward and still believe that it came from example.com.

Hadley: i'm thinking about things like - if one of our problems with implementaiton of AMP is what appears in URL bar, are we further delivering content to the user where user has no way of expecting that their interactions are with somehting not in the URL bar. Is there an exploit?

Alex: the document signed with whatever key it was signed with. we treat it exaclty as if you had issued a request and received a response from example.com.  This solves half ot that problem - the content didn't come from but didn't run as example.com.  This replicates the effect that CDNs have... Goal if all this work is a future in which you don't need [AMP] to get AMP awesomeness.

Dan: does this support re-decentralization, does it support long tail?

Alex: maybe.

Hadley: i am also thinking about whetehr the end result is that e.g. AMP content may be delivered by Google but won't be hosted by google... that this takes a step back towards decentralizing the web if we're looking at the AMP model as centralization...

Alex: I do think [that's true]  There is a mode that we should discuss further...

Peter: decentralized fail-over - where server is blocked - but you could do p2p fetch from others' browsers. what was missing was having the signed authority of that content. there is a privacy issue... but some possibilities for re-centralizing the web here

Hadley: would help with tim's pet plea

---


### AOB

Peter: Next week Ian K is joining us to talk about - Houdini custom layout... 

Alex: on Houdini - the team that has been building Animation worklet - origin trial in a few releases - it's happening in an upcoming chromium release.

### Automotive

Hadley: we have an automotive email from Ted.  

Sangwhan: yes

Hadley: i think we should move that to github....

Sangwhan: saw that on the AC list but this hasn't come to our review 

Dan: we need a new issue. We should guide to Ted to raise it.

Sanwhan: i will follow up and send that email.



