#
#TAG Teleconference - 20 May 2015
##
Present: Dan A., Mike West, Travis, Hadley, Alex Russell, Yves, Mark, David Baron
Chair: Dan
Scribe: The Awesome Travis

Topics: 

   * Review F2F Minutes from SFO
   * Credentials API review
   * Browser Fingerprinting
   * Next Call: CSV review : \url{https://github.com/w3ctag/spec-reviews/issues/55}
Agenda: \url{https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/05-20-credentials\&fingerprinting-agenda.md}

**Call for review** - F2F minutes from San Francisco:
\url{https://github.com/w3ctag/meetings/tree/gh-pages/2015/04-sfo}

**Credentials Review**: \url{https://github.com/w3ctag/spec-reviews/issues/49}
**Spec**: \url{https://w3c.github.io/webappsec/specs/credentialmanagement/}
mnot: I've taken a look, and am happy with it at this point.
... one issue: the friendly name on end-user credential. If this is edited, is it visible to the site? 
[This is the thread: \url{https://lists.w3.org/Archives/Public/www-tag/2015May/0020.html}]
mike: for user/pass sites, you'd have a "name" that is not a username. The user agent can do a reasonably good job showing the friendly name. 
... currently all the info is dumped back to the site. 
... for user/pass, name+icon are both exposed on the credential object when given back.
... password is only exposed for same-origin post.
... there's no reason why we have to expose this info (in case of privacy concerns)
mnot: I can see folks wanting to edit that. I would be "surprised" if that info was disclosed to the sites. Might be nice to have it write-only to not surprise users.
mike: Current chrome implementation isn't settable.
... if we do make it editable, then it opens up some questions as described above.
mnot: that's all I had.
travis: I saw something related to FIDO, could it be related.
mike: Yes, I heard about this. They wanted an API extensible enough to handle their cases, but nothing there is in the doc.
DBaron: No comments, but thanks for the welcome!!!!
All: WELCOME DAVID!!
Alex: I don't think so. Mike and I chatted about the API shape. Seems good. Using promises... the various types being somewhat 'baked in' are unavoidable. I've reviewed a lot of the decisions and they seem reasonable.
Hadley: haven't reviwed yet.
dka: I thought there was some work going on within UK gov on a related thing...?
... If you do review, can you please share your feedback from that perspective?
Hadley: sure.
Alex: Structured Clone is used in the doc. There's an open issue on defining structured clone algorithm.
Mike: SCA is not there for any existing requirement, but "folks" want to be able to store credentials locally (IndexedDB).
... I've had trouble trying to explain how it fits. Would love to see the FIDO folks join W3C.
Alex: Credientials seem to have an origin. SCA can pass credentials across origins. Is this a problem?
Mike: There are several options.
1. The Cred has an origin baked in. We either neuter it so it's not usable, or allow access.
The FIDO folks always seem to want these same-origin. Therefore SCA should somehow neuter the object (make it unusable). I haven't talked through the use-cases.
Travis: I can follow up on any cross-origin use cases.
Mike: Mmm. They may have them, not sure I like them.
dka: Is there any process blockage between W3C/FIDO (wrt intellectual property) or is this cultural differences.
Mike: I heard the word "Laywers" and backed off (didn't really want to pursue that, and I'm not sure what's going on there).
dka: Might be some kind of IP then.
Mike: Had a question for you: One of the main areas of contention was brought up by credentials and web payment. They see a lot of overlap with this API and their goals. In particular, for cross-origin creds (government ID, Driver Licenses, Age verification, passport, etc.). They have a broader view of creds than this spec embodies. We've discussed what extensibilily points might be useful to them. Personally, I'm not very interested in them, but wanted the TAG to look it over, and have a review. 
... To what extent is the API in the doc 'extensible enough' to support uses cases that matter (according to TAG)?
mnot: Automatic disclosure of my digital drivers license sounds scary, hopefully appropriate measures would be taken.
Hadley: I need to take a close look. A lot depends on who owns the data.
... in the UK, our position is that the users own the data.
... When a user visits a service, the user would disclose just want is necessary to validate and nothing else.
dka: Perhaps we should review the thread mike referred to (\url{https://lists.w3.org/Archives/Public/public-webappsec/2015May/0101.html)} and then come back and discuss on a future call?
Others: +1.
Alex: I want to understand what is going on with the Credentials CG.
mnot: The name attribute privacy issue--Mike was going to address. I think the rest of the feedback is done.
dka: I propose closing the issue in GitHub (for the feedback). I can open a new issue for a more general credentials discussion and use cases. We can bring that up as an agenda topic for Berlin. (RESOLVED)

Credentials CG use cases: \url{http://opencreds.org/specs/source/use-cases/}
Web Payments IG use cases: \url{http://www.w3.org/blog/wpig/2015/04/16/web-payments-use-cases-fpwd/}

Topic: Browser Fingerprinting \url{https://github.com/w3ctag/spec-reviews/issues/38} 
(Ways of identifying user's personal information)
mnot: A document from the privacy IG. Gives guidance on how to avoid fingerprinting
Here's the doc: \url{https://w3c.github.io/fingerprinting-guidance/}
mnot: after first read, I thought it was not terribly well aligned with browsers POV and folks in WGs -- how they address the issue. On a closer read, it does seem more closely aligned. There are best practices that make sense. My view: it's pretty reasonable. It could be improved with a few more examples and some grammar edits.
... It's trying to avoid letting fingerpriting run rampant. Some amount of fingerprinting has already happened (and the doc calls this out: is it a lot cause?)
... Specific feedback: 
... the do not track link could probably be dropped.
1. It makes a distinction between active/passive fingerprinting. The difference is whether "code is run"
Another way of thinking about it is if the server is doing something custom (sending specific content)
2. Do we need some kind of "hook" for browsers/extensions, etc., to disable fingerprinting?
Canvas has a property (origin clean?) turns off some fingerprinting access.
E.g., if I was designing a new platform feature, and had a way of turning it off via some spec mechanism, that would be nice. Same goes for privacy features also.
Alex: Some
1. What are we meant to do with/about it?
2. What is its trajectory? Going to REC?
mnot: status says its going to be an IG Note (with very little impact).
Alex: Was the TAG asked for feedback?
mnot: yes
Alex: Ok. At the limit, fingerprinting is about being able to detect the "real operations" of the system. Did it do what you expected it to do. This comes through CPU, timing, memory, etc., It's very difficult to clamp down on the amount of security leakage.
... A privacy mode does really involve "turning things off" to really be effective.
[cf the work going on in the TOR project \url{https://blog.torproject.org/blog/tor-browser-50a1-released} to reduce the fingerprinting space]
E.g., my collegue Dimitri created: \url{https://github.com/dglazkov/nope-js} to turn off features that are slow. When this runs on the web, so much of the web doesn't work at all. :-(
Alex: If there's something meaningful for us to do, I'm not sure what it is? What does this aim to accomplish?
mnot: Well, they're going to publish it as an IG note? A lot of what you said was covered in the section "is this a lot cause"?
Alex: I'm not sure if this doc really captures the state of the art. There is so much more that is there...
dka: You mean related to timing, etc.
Alex: Let's create a single VM. Everything will render though a particular browser with carefully controlled CPU, memory, timing, etc.... then maybe you've go something. Till then?
dka: Can we add feedback that the doc's contents are not the only way that users can be fingerprinting?
... Can we recommend a larger scope for this document? Should it become a TAG finding?
Hadley: that would be my suggestion.
... There is value is having someone declare: "fingerprinting is bad" as a stance.
mnot: I'm not sure it would do much good.
dka: It's a subversion of the intended use of the platform. It's just so widely done...
... I'm more concerned about the folks that say fingerprinting is a lot cause. Just because there's so much, doesn't make it a lost cause.
mnot: To Alex's point. I thought it wasn't well aligned in my first reading. I gave that feedback. I read it again, and found a lot more subtle.
... We should raise the bar so that everyday websites have more work to get your data.
... I'd like to avoid it being 'normal' to fingerprint the user.
... My interest was more for putting hooks in the platform so that folks like TOR have the right hooks. The TOR folks could really benefit from these hooks that coudl turn off or control these features. They understand the realities of this space.
dbaron: I concerned that I hear lots of convention wisdom about fingerprinting is a lost cause, and I hear different WG with differing opinions on the subject. Where one group might be strictly avoiding it, another group might be adding lots of entropy over different viewpoints on fingerprinting.
... There are a bunch of interesting mitigations that might be possible, and even they won't prevent getting model of laptop and OS version,  but in a lot of cases this might not come "down to a single user".
Hadley: We/TOR may not have the answer. With so many views out there, anyone trying to solve this gets stuck. At least if TAG put out a finding, then some folks could be encouraged to make progress.
Alex: Agree with Dan: at the level of a policy statement for you should do/not do something... I absolutely support doing this for people who are asking. Policy makers, etc. At the technical level, I'm reacting to the idea that there's a technical fix that can be done.
dka: This might be a really great topic for Berlin?
mnot: several TOR folks will be at a workshop, might be convinced to come to our meeting in Berlin.
dka: TOR team is the state-of-the-art, and might have some good, specific feedback.
[now is the winter of our fingerprinting discontent]
:)

Agenda for next week: feedback for CSV on the web. This is assigned to Hadley.
Might be nice to chat directly with Jenni before our next call, and have her join us next week.
Also looking for a second topic for next week.

mnot: Would it help to start writing up a doc on the fingerprinting issue?
dka: Wondering out loud about who the audience would be... but go for it, by all means!



