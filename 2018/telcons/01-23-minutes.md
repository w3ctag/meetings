## TAG Teleconference
##### 23 January 2018

Present: Peter, Lukasz, David, Dan, Andrew, Yves, Travis, Hadley

Regrets: Sangwhan, Alex

---

Agenda:

* [Files and Directory Entries API with webkit prefixes](https://github.com/w3ctag/design-reviews/issues/215) - Andrew

Andrew: I put some comments on this. It seems fine to me. It's been around for quite a long time. There is some undefined behaviour... it allows you to select a directory or you can select multiple. Undefined behaviour if it's combo of directories & files. It doesn't use Promises. There has been a reluctance to change the API instead of making a new one (a redesign). Generally it seems fine. Seems like there isn't convenient to convert the existing API to remove the prefix and add promises.

Peter: Close the issue?

Andrew: There's no impetus to spec someting different. Yet low appetite to just use this. I think we should say if the design substantially changes we'd like to see it again. And then close it.

Peter: OK seems fair.

Travis: This is the legacy …

Andrew: doesn't specify upload behaviour.  If your web browser were running on a device which had a restricted file system like a camera / smartphone it could preesent [something appropriate].

Travis: from what I recall we implemented this [reluctantly] so even though we hated it we did it for cross browser interop. At the same time there was another proposal - in the WICG - which is superior and promise based. But it's stalled. [link?]  The webkit prefix is bad. There's no appetite to map everything to a concept of a file/ directory structure.

David: there might have been some security concerns... How users understand what they're being asked - when you pick a directory for example.

Travis: it was a while ago.

Andrew: from a developer perspective, the argument in favor of a generic abstraction layer - you do have that low level model on desktop machines and many other devices. The danger of going with something more simplistic is that it doesn't match.  So it seems fine to me [besides the prefix and the promise]. Can you comment on it, Travis?

Travis: yes I will do that or delegate.

Peter: so leave it open...

Andrew: yes.

---

* [Serialization of natural language in data formats](https://github.com/w3ctag/design-reviews/issues/178) - Sangwhan, David, Travis

Peter: nothing.

David: punt to f2f.

Hadley: should we nudge?

David: we just need to review the thing.

Travis: maybe a poke to Addison would be worth it.

David: I can do that.

---

* [Web Locks API](https://github.com/w3ctag/design-reviews/issues/217) - Andrew

Andrew: I did have a look at this. Alex has had some input. The thing I find weird - it's a combination of callbacks and promises. From a developer perspective it's confusing and a barrier. If you click through to [the explainer](https://github.com/inexorabletash/web-locks#api-proposal)…  Promise doesn't resolve when the lock is acquired (despite the method being called `acquire`) - it's when it's released. So confusing. The 2nd argument is a function so the Promises resolves when the lock is complete. The explicit lock and release API would be more what I would expect. So I fed that back. The response is that was considered but they went with this one. Not sure I agree with the response.

Travis: my gut reaction is "what?" 2nd reaction is: if they want to extend this for storage meachanisms then maybe we need a general mechanism for locks?

Andrew: yes - I suggest you make that point. They say the test framework for weblocks actually does implement the explicity release mechanism. They've got some test harness.. that .. [describes current test case scenarios].  This is a really good indicator that people will want to do it like that.

Travis: We all just pulled shared array buffers because of Meltdown - so we don't have the same set of scenarios - which is referenced in the FAQ. I will add a response.

Lukasz: [security & privacy] Security and Privacy has been considered during the development of the API. As for taking and releasing locks - not clear if resolution granularity would be similar to Meltdown/etc timings (re: shared array buffers). Some links: https://github.com/w3c/wake-lock/issues/78 https://github.com/w3c/wake-lock/issues/89 - considerations speak about detection of system/performance patterns (e.g. battery level).

David: I haven't had a chance to write something substantial with async / await.

Andrew: I have - it's nice - most JS developers have shifted to use it for Promise based code. The idea of mixing in a call back feels like the wrong design.  It's misleading.

Peter: "with" statement?

Travis: …unscopeables…

Andrew: I suggest we have some input from Travis on the issue and we could - if we want to resolve something stronger than I think that would be a good idea. [recounts feedback already given] Remaining issues are the name, shape and likely behaviour when developers don't use it correctly.

Peter: potential for deadlocks concerns me as well.

Lucasz: Agreed with Andrew (1) async/await is cool, mixing promise/callback doesn't look good. 

Peter: bring someone in?

[discussion of who to bring in]

Andrew: we can ask Josh Bell.  I can ask him in the github thread.

---

* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221)

David: I looked at this a bit last week.  There are 2 separate APIs. WebShareTarget and WebShare. Can be used together or independently.  Web app can be the recipient of a share... limited to things with webapp manifests.  Could be a native share or from the use of the web share API.  …  This is related to registerProtocolHandler and registerContentHandler.  Latter is dead [due to lack of popularity].  This doesn't have type specific stuff...  One of the issues they asked was about URL parsing. The thing they did seemed fine to me. The other question they asked was - if the share subsitutes things into a URL and pass it off to a site - they asked about concerns with path segments and path escaping - should they limit the substitutions to be in the query & hash parts of the URL. I can't work up a strong opinion about this. I'm not crazy about imposing URL restrictions but maybe it's OK due to security issues.

One thing I'm not crazy about - this spec adds to the webapp manifest partial dictionary and not having a registry. Especially if we want to make sure that webapp manifest and origin policy don't have duplicate keys.

Travis: similar feedback from Boris for web performance wg. Valid feedback.

David: Boris likes to call them "come from" statements - you can't follow it. (As opposed to a go-to statement.) I'm worried - we don't have a mechanism to make sure specs don't use the same name to extend an interface in different things. Worrying.

Travis: ...something something registries...

Dan: We did ask the AB to take on a work item on registries...

Travis: maybe what is needed is a go-to statement.

David: conflicts may only be discovered after both specs have shipped.

Peter: [back to issue at hand]

David: should there be a broader solution or is this a good first step?

Travis: it has a higher chance of success than registerContentHandler had. It seems like a good start to me.

Peter: they are reinventing URL templates and there is already a RFC - [RFC-6570](https://tools.ietf.org/html/rfc6570) - for this. I've written 2 different implementations. They should look at this instead of inventing their own.

Peter: so - let them respond... milestone set for the f2f. Can you comment with that RFC link?

Peter: OK.

---

* [Transform Streams](https://github.com/w3ctag/design-reviews/issues/211) - Sangwhan, Alex, David

---

* [General storage observer](https://github.com/w3ctag/design-reviews/issues/210) - Travis

---

* [Web Lifecycle](https://github.com/w3ctag/design-reviews/issues/205) - Travis


---

Followups:
* [import.meta.url, and import.meta generally ](https://github.com/w3ctag/design-reviews/issues/208) - Alex

---

* [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - David, Alex


---

Triage:
* [Web Speech API](https://github.com/w3ctag/design-reviews/issues/214) 

---

* [Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218) 

---

* [CSS Selectors 4](https://github.com/w3ctag/design-reviews/issues/219)

---

* [Async Clipboard Text API](https://github.com/w3ctag/design-reviews/issues/222)

---

* [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223)

---

* [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224)

---



