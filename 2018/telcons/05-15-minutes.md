## TAG Teleconference
##### 15 May 2018

Present: Peter, Hadley, Alex, Sangwhan, Gary Kacmarcik (guest), Yves

Regrets: Dan, David

---

Agenda:

* [Async Clipboard API](https://github.com/w3ctag/design-reviews/issues/222)

Alex: summary of conversation about reading system clipboard contents w/o user consent
Gary: this is one of the reason that most password managers have a timeout feature. LastPass, e.g., uses a 20 second timeout
Hadley: oh! Will look into that
Gary: reading is more sensitive than writing (which is a security, but not a privacy, issue)
Gary: the permission allows us to decide to auto-grant or not...were there other issues?
Alex: I had recalled Hadley being concerned about notifying users when the clipboard was being read back out
Gary: right. In the past, we used to have a hackey user-gesture standard, an any user-gesture would trigger it. Now we have real permissions. The API is set up so that UAs can impose gesture requirements if they want to -- the API allows UAs to also require a user gesture -- but Chrome doesn't use these.
Alex: is there a concept of foreground vs. background use?
Gary: Chrome limits this API. Only the top-level tab can use it if Chrome is in the foreground.
... that said, we do probably allow cross origin iframes given that it is in a top-level tab. This should probably be addressed.
Alex: there's a way to do iframe delegation.
[_discussion of this attribute system_](https://docs.google.com/document/d/1x5QejvpyQ71LPWhMLsaM1lWCfSsBsSQ8Dap9kJ6uLv0/edit#heading=h.ib6rctasbt3y)

[TAG Review of Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225)

Gary: for the clipboard, it should say top-level browser context, will follow up on that
Hadley: there was something that was non-normative but not in the algorithm...
Gary: I didn't put something in the spec because I didn't want to add something in the spec w/o checking w/ other browser vendors
Gary: agree that it should be in the algorithm. Should specify which exception to throw and that it should be limited to top-level browsing context.
Sanghwan: it's there in section 11.2
**group discussion of where this exists in the spec**

Gary: there are non-normative approaches mentioned about expiring the permission, e.g.
Alex: what's shipping?
Gary: Chrome 66 -- for text -- auto-grants the permission to write, and the read-permission puts up a permission request per-site; it's persisted

**discussion of user visible indicator**

**we verify on https://permission.site that Chrome shows a usage indicator**

Gary: per previous comments on this, we split the TAG review into a few sections because there are many open issues on the spec. The Text API is what we pushed through because it ididn't have those issues. Once we get those other issues resolve, we'll file another TAG review for those areas.
Gary: we know text is both easy to use widely requested
Gary: there was a question about `DataTransfer`, but we're pretty sure we won't be able to use it -- e.g., via Delay Loading and images in multiple file formats -- we'll probably be moving to specify a new object type
Sangwhan: good to hear. I assumed it was being used because it was there
Gary: also, we thought it was adequate. It's *mostly* adequate, but we'll need to make serious changes to use it. There's another issue -- once we change it, all the Drag and Drop issues show up on our doorstep.
Alex: sounds like we should have another conversation about that when you get closer to making a decision?
Gary: absolutely. My plan is to come up with proposals before TPAC, present there, and come to some consensus after TPAC

Sangwhan: has anyone raised the concept of stack-like clipboards?
Gary: most people are asking to access the system clipboard. What we're mostly hearing a request for is custom data types on the system clipboard.
Alex: is prefixing or read-barrier usage possible?
Gary: Chrome does something similar with a funky name. APple does something similar with a different interpretation. If it's useful, we might want to specify that so we can get agreement.
Alex: I'd expect people to stuff things in images until we get custom data types
**conversation about content munging and EXIF content exfiltration**
Gary: I think Chrome will strip EXIF data incidentally
**sangwhan files issues**

**hadley is muted =( **

Sangwhan: one question about text vs. other formats...you're shipping `readText` but not `read`?
Gary: we don't have the signature locked down for `read`, which would have perhaps required us to nail down usage of `DataTransfer`.
Sanghwhan: but that wouldn't be required for, e.g., a rich-text editor?
Gary: right. We think text is very much the most common case.

Hadley returns!

Hadley: I'm thinking through vulns about persistent origin-wide permission. What brought you to that conclusion?
Gary: which conclusion? A permission that doesn't timeout?
Hadley: yeah
Gary: we ran it through our privacy/security team and they requested having many of the mitigations we've discussed in place
Gary: I'll point out that you may have heard about WebAudio over hte past week or so...there have been many conversations about autoplay which raises the idea of permissions that apply based on use

**conversation about execcommand and various workarounds to be able to update the clipboard**

Gary: until we had permissions, there was no realistic way to implement this API. Having the permission pop up a grant request was what allowed us to unblock this work.
Hadley: I still have the concerns, but now I understand why this problem is so important to solve
Gary: having this conversation has helped me understand why so many of these mitigations need to be listed in the spec

* [Keyboard Lock](https://github.com/w3ctag/design-reviews/issues/192)

**agreement that it's closed and looks good**

* [Keyboard Map](https://github.com/w3ctag/design-reviews/issues/238) - Travis, Sangwhan

Gary: some concerns about privacy on this one; e.g., providing information about the user's setup. I updated that spec to include a privacy mitigations section (section 6.1). Is this in a better shape?
Hadley: it is in a better state. Might be useful to say why we care about this. I.e., noting that someone's keyboard is unusual in their country
Sanghwan: that's been noted in the spec.
**we all agree update was made recently**

Alex: Will this ever be available to workers? Maybe a question for the WebXR group.

Gary: I thought they were content to move everything off the main thread.

Sangwhan: I thought at least one of the inputs they tried to move off, because the sampling was too low.

Alex: I like the design of this API and the examples in your explainer.

Alex: ...Questions for us?

Gary: not really. Have been trying to proactively apply previous TAG review learnings to this. Was initially concerned w/ the promise-based design, but that allows permissions.
Gary: is it recommended that every API be a promise?

Alex: Every API that could be user-mediated; i.e., prompting the user for permission.

Gary: I don't have specific questions with this. I'm working on a definition on what "ASCII-capable layout" means, but that's the only outstanding issue.

Sangwhan: wanted to say that I'm happy with the latest changes. Thank you!

* [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232) - Dan, Yves


---



