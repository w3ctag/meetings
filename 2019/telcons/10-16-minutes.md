## TAG Teleconference
##### 16 October 2019

Present: Lukasz, Kenneth, Peter, Tess, Alice, Sangwhan, Hadley, Yves

Regrets: David

---

Agenda:

* [Ability to customize virtual keyboard via enterkeyhint](https://github.com/w3ctag/design-reviews/issues/380) - @hober
* [Custom state pseudo class](https://github.com/w3ctag/design-reviews/issues/428) - @hober, @kenchris, @plinss
* [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @alice
* [Partition the HTTP cache](https://github.com/w3ctag/design-reviews/issues/424) - @hober, @ylafon
* [Proliferation of manifests at W3C](https://github.com/w3ctag/design-reviews/issues/423) - @kenchris
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman
* [raw clipboard access](https://github.com/w3ctag/design-reviews/issues/406) - readout from breakout with @hober @torgo @hadleybeeman & do we need to re-open [issue 222](https://github.com/w3ctag/design-reviews/issues/222)?

---

### [Ability to customize virtual keyboard via enterkeyhint](https://github.com/w3ctag/design-reviews/issues/380) - @hober

Tess: This came in in May and seems to have immediately fallen into The Abyss. I think that was my fault because I assigned it to myself.

Tess: However it also appears really straightforward and I think I'm happy to sign it off.

... Different mobile OSes/VKs will change the appearance of the enter key. E.g. it might be a search label/icon instead of enter.

... This provides a declarative way for sites to help the system pick the right label for the enter key.

... ABout the simplest thing that could work. I thought it would be a good candidate for taking something straight from The Abyss to resolved.

Kenneth: This seems pretty similar to ... Mozilla.

Peter: You put this attribute on ... each element inside the form?

Tess: Waiting for HTML standard to load...

Kenneth: We had this at Nokia, but we were looking at what type of form (element?) it is...

Peter: Looks like attribute goes on form controls. A bit weird cause enter normally submits a form.

... Should this be an attribute on the form?

Tess: Same as number keyboard..?

Peter: If the *action* of the form is submit, or go, or whatever the default enter key action is... you don't want to mess it up by forgetting to put the hint on one of the form fields.

Tess: Text and search within the same form suggest that we want the ability to customise...

... Maybe want to also allow it to be set on form?

Peter: Right, then you could override on different elements.

Tess: Perhaps you could raise that feedback as a github issue?

Kenneth: You could put this on any element?

Peter: According to the spec, anything that could be content editable.

... Other than that I have no issues with this... anyone else?

... Ok, Tess, go ahead and close it and I'll file my issue.

### [Custom state pseudo class](https://github.com/w3ctag/design-reviews/issues/428) - @hober, @kenchris, @plinss

Kenneth: Lots of comments there...

Peter: Ok, this was because existing APIs only let you specify boolean states. Got a lot of feedback...

... I'd like to see this as a general-purpose mechanism, not restricted to boolean states.

... Most existing pseudo-classes are boolean, but things like dir and lang aren't.

... state (?) has a token list, so more like the has() API

... Just adds one attribute to the ElementInternals, which is a tokenlist "state".

... Alternatives considered mentions an alternative syntax, using dash dash prefix

Kenneth: I don't know that I particularly like either syntax alternative, in a sense it makes sense...

... what other examples are there that aren't boolean?

Peter: Just :dir() and :lang() - both strings.

... token list is the set of custom states you're exposing, where each is just present or not. Would have to add something like a map.

... If we're going to use a map why not just use a map?

... Maybe we should set this as pending external feedback?

Kenneth: When might you use a non-boolean state?

Hadley: Would be nice if the explainer had some user-focused use cases...

Peter: checked state for a tri-state checkbox, you'd have to have a checked boolean and an indeterminate boolean...

... right now pretty much all you can do is set an attribute on the host attribute. So we could use attributes on custom elements which are used for styling as data to feed into this design.

### [Modal window](https://github.com/w3ctag/design-reviews/issues/427) - @hober, @alice

Tess, Alice: We didn't get to look at this yet

Sangwhan: I actually did...

... This is another WebView API, analogous to Portals. We seem to have two competing things that are trying to show a webpage from a different origin, in a browsing context that is almost but not quite an iframe.

... Reviving one of these IE specials... use case seems to be for payments. Modal dialog which is a weird pop-up iframe, you can message back and forth, on top of your current document. Sort of not great.

... significant overlap with Portals. I don't understand why they're not being developed together. API just opens a web page in a "modal dialog". 

.. IE modal dialog blocked execution of main modal opener. This one doesn't do that but inherits the same strange design. 

... Use case is valid, but ...

Hadley: Looking at the issue, looks like they're not convinced this is mature enough for tAG review. Started brainstorming at TPAC and haven't finished.

Sangwhan: I agree that this type of capability is missing, but this sdoesn't seem like the right solution.

Lukasz: Do they foresee any impact on visivble user interface (i.e. they link to showModalDialog)

Hadley: Are you suggesting we ask...?

Sangwhan: Could we suggest trying to align this effor with Portals?

Peter: Considering the feedback we gave to Kenji et al, regarding layers, it seems like there should be a common base class here if nothing else. They should definitely be talking.

Sangwhan: I'll write that down as a first response... other browser vendors aren't really fans of Portals, ... 

Peter: Tess and Alice, want to do a breakout on this?

... Sangwhan, I've added you.

... bumping it two weeks.

### [Partition the HTTP cache](https://github.com/w3ctag/design-reviews/issues/424) - @hober, @ylafon

Yves: Cache is not only for clients, but to ... on the server side. It would be good to have exemption of the partitioning for sites that are explicitly asking for public cache. ... control public... do we want a fake delay retrieval in that case?

Sangwhan: For CDN?

Yves: Not just CDN... also for sites with a lot of traffic...

... Mostly non-CDN and non-big-company websites.

... Wondering why they are ...

Tess: Worth raising the CDN, etc. question. Tension between goal of partition, namely hiding from the sites that they are both embedded in the same resource, preventing data sharing. 

... As far as eTLD+1 vs origin... this is me guessing at rationale... general desire to avoid building new platform features that depend on the public suffix list. Arguments either way. Not obvious what the better move is.

Yves: Need to be an alignment between ??? - 

Hober: prefer them to match up...

Yves: I'll write an issue on the cache control public... server-side... that's all for me on that specification

Lukasz: (copied from slack)

> Looks like a nice privacy-improving spec. Is there any way to standardise partitioning keying across implementations? Seems there is an Apple precedent and this of course opens a question: should this precedent be followed? Are there any drawbacks of having different implementations using different keying techniques?

... Would we want ... extension to this partition? 

... People might be questioning what kind of privacy or security in case an optional artificial  delay in delivery (retrieval) will be deployed so maybe not ask about this particular thing and see how it goes

Tess: we have a number of good comments here to make on the issue.

Peter: Folks want to post those comments on the issue?

Tess: sounds good to me.

Peter: so, who...

Tess: Yves is writing up the cache control one. Lukasz is adding his. I can try asking again about origin vs. registerable domain decision.

Peter: Ok, I'll mark this as pending feedback, and we can come back when we get feedback.

### [Proliferation of manifests at W3C](https://github.com/w3ctag/design-reviews/issues/423) - @kenchris

Kenneth: I got assigned to this because we have all these manifests and there is some sense in making them the same or at least similar.

... some things are similar in style but used in different ways.

... I don't know a lot about the audiobook manifest and how that works...

Sangwhan: ever seen an mp3 playlist? it's sort of like that...

Kenneth: Bit of a differen style. Some using JSON-LD as well.

Sangwhan: I believe Audiobooks has been implemented by ?? (ebook company)

Lukasz: This is a very horizontal issue.

Kenneth: We already met with publications workgroup like two years ago...

Lukasz: Not possible to design integrated manifest across all uses.... but perhaps filename or attribute based tagging?

Kenneth: .. underscores in name of manifests? I don't know why?

... Depends how worthwhile this is actually pursuing.

... already have naming advice in TAG design principles. Maybe we should link to that?

Sangwhan: We don't have a guideline for manifest formats.

Kenneth: Naming style... case rules consitent with existing APIs.

Sangwhan: That's for APIs..

Kenneth: some are underscore delimited... I'll take a screenshot and put it in the issue.

.. in WebApp manifests... can be called whatever... .manifest is because some people configure servers differently for json files and manifest files.

Sangwhan: Should we add something in the principles doc, or have a separate doc?

Kenneth: Same document would make sense...

Sangwhan: That document is getting long...

Kenneth: But it's all in one place, having multiple docs makes it harder to find the right one.

... perhaps it cou.d be spun out into a separate doc later.

Hadley: Design principles are *for client side APIs*. This seems like more than that, but also part of that.

Kenneth: ... is being separated out into a different spec. People can depend on that from other specs.

Sangwhan: Sort of falls into data. That should probably have a different principle set...

Hadley: Feels like there's two very big meta-stages:
- collecting all the existing work that includes manifests - I have a memory of Dan saying another group is creating their own manifest
- thinking and discussion what the TAG can do about it.

... I'm not sure from this discussion that we're resady for the second bit.

Kenneth: ... being split out from ... manifest ... background fetch. Splits it out into a regular API.

Peter: Might make sense to have something akin to the well-known convention, a place to store these things. Avoid naming collisions.

Kenneth: Used to have that in web app manifest...

Lukasz: I wonder what will the situation be like  in ten years? Impossible to predict but any issues if there are like five or ten different manifest files? Maybe tidy up a bit by e.g. keying (description) on some attribute? 

Kenneth: Have been trying to keep webapp manifest very minimal at all times.

... localisation...

... publication manifest, very little that's shared...

... may not be worth pursuing at this moment...

Peter: put it on the back-burner?

Kenneth: Yeah. WebApp manifest is going to evolve slowly. Maybe in the future it makes more sense to share...

... Payment is a separate thing, not an app but a method, makes sense to integrate that in the same spec.

Hadley: Makes sense to keep this open. "Deep thoughts" is accurate. Can come back to this at the next few face-to-faces, and see whether thingsa re coming out of it. Is the community helping, or is this a big, nasty piece of work that we're expected to do but may not have the resource for?

Peter: I've set the milestone to the next face to face.

### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman

Hadley: We only have 1 minute left, I would like to spend more time than that on this issue.

### Mini-apps

Sangwhan: I got one more ping about this, did we do anything about it?

Peter: Dan was going to write a blog post, I'm not sure where that ended up.





