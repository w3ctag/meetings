## TAG Teleconference
##### 11 September 2018

Present: Dan, Peter, Hadley, David, Yves, Travis, Lukasz, Alex

Regrets: Sangwhan

Scribe: Hadley

---

Agenda:

* [CSP feature 'unsafe-hashes'](https://github.com/w3ctag/design-reviews/issues/291) - @cynthia @dbaron @travisleithead

(Notes Sangwhan's absence)

(Notes Github complications. Gremlins.)

David: It's a new thing in CSP.  Link to an explainer (google doc). 

...CSP has a thing called unsafe-inline. Even though inline script has some risk of xss attacks, unsafe-inline says "I want to use inline script anyway". unsafe-hashes is a more linmited version; not all, but only the script with these SHA256 hashes. And nothing else. It seems not that complicated if you do it right. It's a small feature. We had a dicsusussion about character encoding... turns out you need to understand that to do this. 

Travis: We had a question on what was supposed to be hashed, in the user's content to compare against the CSP directive.

David: Just the attibute value.  Maybe extraneous white space; needs to be defined.  

...Otherwise this seems fine.

Travis: Concur. The UA will eventually need to check every one of these markup defined event handlers. and hash them all l... it's more work that before

Lukasz: It's not a performance problem, when you see how much computation blockchain does.  Also remember that HTTP header limits the number of hashes that one can include in a header. 100 hashes; header limit is 8KB -- or something like that.

Travis: So there may be some practical limits due to what you can include in a CSP file. Not just in a header, right?

alex: I don't think it's 8KB. 

Lukasz: Okay, but there is a limit.

alex: there are pracitcal limits that proxies set, for example, You couldn't hae a URL > 4k in length.  Mozilla at oen point had a similar restriction, to prevent buffer overflows. But I'm not aw aware of a fixed size limit.

peter: apache has a default limit of 8K, but you can overr override tthat.

Travis: David, what more should we get from Andy P?

david: Main this is going to be interoperable spec text. Whic hshould be a prerequisite for shipping it, at least. 

alex: it's still early; it's at intent to implement. So we have time.   ...right?

Lukasz: Apache has a limit of 8000 bytes.  If this is the case, it should be in the specification.

Travis: Should we close this? Have them come back when they're further along?

alex: I'd like that. Do we have structural critiques beyond interoperability and char encoding, and think harder about across attacking document types?

lukasz: I like this, it improves security. So we can close it. This is somethign we want.

Travis: works for me.

(Github is playing more nicely. California is clearly awake)

(consensus for closing this issue and asking for them to come back when close to shipping)



* [CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - @dbaron @travisleithead @plinss

dka: I had notes on this from last week

Travis: We did a good review in Tokyo. We've been waiting for the PR that we reviewed to get merged into hte spec. Happened last week. I've reviewed the spec, looks great. I'm happy.

...Let's close it.

David: I'm fine with that.

Travis: I'll do that.

* [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240) - separate call arranged? - @cynthia @hadleybeeman @plinss 

dka: was a separate call arranged?

Hadley: I thought we left it with Peter.

Peter: I recall I was going to write up a blog post. Still will do that.


* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff @dbaron

Hadley: We left this open so that David could monitor progress in the W3C spec and the WHATWG spec.

alex: Do we need external feedback? I'll ping the owner and get an update... I'll move the milestone o 2 weeks from now.

* [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @travisleithead

Hadley: progress from Alice

Travis: I've looked this over thoroughly. She has since responded to my comments.

dka: Will Alice be at TPAC? 

alex: I'll check. -- that's a yes, she will.

Travis: Let's come back to this next week. She has retsome urned some questions to us.

dka: Where will AOM be discussed at TPAC? In an accessibility working group? 

Alex: Guessing it will at least get an overview at one of them, as it has in years past. There hasn't been deep technical debate on merits in those groups. Normally she gets feedback at TPAC on hallway track and at TAG meetings.

Travis: web incubator group meeting on Tuesday and Thursday. They might review it there. 

dka: that could be an opportuitynity for us to engage.

Lukasz: question whether the permissions model might apply to that. 

travis: that has come up in the notes I've read .Privacy around the permission prompt and that any customised events they may fire could raise a signal that this is an accessible user.

Lukasz: This may be an issue for further down the road. Permissions model might not be efficiently applied in that case. If not then there is a more broad issue.

dka: Let's bump this a week, and note that we'll revisit it at TPAC.  No, just discuss it at TPAC.?

Travis: I'd like to see it again next week first.

(Pause to blame TAG alums andrew and mnot for CDN failures)


* [User Activation v2](https://github.com/w3ctag/design-reviews/issues/295) - @dbaron @hadleybeeman

Alex: they're trying to come up wit ha simpler mod usel for user activation. 

Hadley: We are waiting for clearer explainer info from them.

Alex: Let's reemphasise that and come back to this.

dka: Speaking of explainers, I will note that Alex and I originally collaborated on this "What is an explainer?" doc.  I put it on the TAG website, so it lives in a few different places. We should make sure we aren't editing it in the wrong place. 

Hadley: [Github version](https://github.com/w3ctag/w3ctag.github.io/blob/9d3531b15e92c928ae5fd21a5cb9bfc32fdacc6f/explainers.md) 

David: ...or is it [this github version](https://w3ctag.github.io/explainers) ?

Hadley: Looks better to me

David: I recently changed our ["TAG, Please review" template](https://github.com/w3ctag/design-reviews/blob/master/ISSUE_TEMPLATE.md) to include this document. 

dka: let's reconcile these via slack before next meeting.

...Let's bump this. 

alex: I looked to see if there was a reasonable polyfill.

(Pause for disambiguation between issue 295 and 300)

travis: I'll comment here. 

* [User Activation API ](https://github.com/w3ctag/design-reviews/issues/300) - @dbaron @hadleybeeman

alex: i'll take care of this one, in light of previous issue.

* [HTML General Review: Custom Elements](https://github.com/w3ctag/design-reviews/issues/244) - @travisleithead @plinss @slightlyoff @kenchris

Travis: This began with chaals asking if we should recommend prefixing in attribute names. Discussion on a previous call; Alex wrote down a bunch of content that doesn't use prefixes. Our advice was .... not going to be breakage. We can't enforce prefixisinsinng. Anne vk said he got to the same conclusions, with the caveat that it still might be worthwhile to encourage prefixing. Potential future feature called custom global attibutes that might require having a prefix

alex: I think that mahink hink that matcheshat matchesches what we did with global elements, preventing leakage into hte global namese. e. e. pace. Still the case that without prefixing.. you can get into trouble. That's a problem; we don't have a solution. Can we leave this comment thread as something to be cited adn movdn movnd move on?

Travis: I think we can close this. WE WE WE We've done it justice. Post conclusion for chaals.

alex: Yves, Hadley, Lukasz - thoughts?

Hadley: I'm happy with that.

Peter: I keep writing elements and forgetting what's global.

ale: We discussed that here could be a way for custom element authors... you could imagine a version where author says "I'm going to use these, disable global behaviour on these."  I'm of two minds; it'll help people locally, but won't prevent this problem at scale. But if we think it's important... we could have 2 flags: no global attributes, don't apply any global behaviour to me.

travis: accessibility folks wouldn't like that

alex: right; thats the second option. "These can never be overriden"

peter: If we did that, we'd have to do it in an attribute.

alex: no easy way to do that, since things can load asynchronomusly.

...At registration time, earliest moment possible. A class-level property that allows you to enumerate owned proattributes.

peter: If you have a flag of opt out of all global attributes, that could be an attribute itself.

alex: I could imagine that breaking a lot. At page level?

travis: I don't feel comfortable recommendating that

alex: or you have a fight over the prototype of html unknown-element. So when it gets parsed, ... the browser creates an element. 

dan: it would be a good idea to close this (while we're ahead) :)

* [RTCIceTransport & RTCQuicTransport ](https://github.com/w3ctag/design-reviews/issues/296) - @cynthia

(skipped for =now)

Triage

dan: since I don't have access to Github issues, maybe we can do issue triage at a later date?

(all agreed. ajourn.)



* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297)

* [Support codec and container switching with MSE using SourceBuffer.changeType() ](https://github.com/w3ctag/design-reviews/issues/298)

* [WebAssembly Threads ](https://github.com/w3ctag/design-reviews/issues/299)

* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301)

* [Canvas TextMetrics](https://github.com/w3ctag/design-reviews/issues/302)

---



