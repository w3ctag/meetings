# W3C TAG face-to-face in Seattle
## Day 2

Present: Kenneth, Sangwhan, Hadley, Travis, Peter, David, Daniel, Yves, Lukasz (remote)

Guests: Sam Weiler, Wendy Seltzer, Christine Runnegar (Privacy IG co-chair) for the Privacy and security questionnaire discussion; ; Ojan Vafai for Async Local Storage & Layered APIs discussion

Scribe (AM): Hadley

Scribe (PM): Alex

### Triaging Non-HTML Issues

#### [294 - queueMicrotask](https://github.com/w3ctag/design-reviews/issues/294)

Travis: I'd like to be on this

Peter: Anyone else?

Travis: This is a convenient shortcut for quining work to run at the end of your task but before the next painting/rendering cycle. We now do this with promises, but this is more convenient.

David Is this the first time we're using the name 'microtask'? Might not be ideal.

#### [291 - TAG review request of the CSP feature 'unsafe-hashes'](https://github.com/w3ctag/design-reviews/issues/291)

Peter: We pushed this to the f2f to discuss. I'll mark it with extra time.


#### [288 - OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame ](https://github.com/w3ctag/design-reviews/issues/288)

Travis: We need to review to review the feedback

David: I'll join


#### [285 - Carriage of Web Resource in ISOBMFF ](https://github.com/w3ctag/design-reviews/issues/285)

Sangwhan: We're waiting for the group to arrange a call with us. I'll nudge again.

#### [283 - Page Lifecycle for system initiated Discarding & Freezing](https://github.com/w3ctag/design-reviews/issues/283)

Kenneth: This is shipping in Chrome, yes?

Travis: yes.

Peter: Does this need breakout time this week?

Kenneth: We looked at it before. .

Alex: They didn't ship the one event we provided feedback on. But they had that larger vision.

Travis: Microsoft looked at it throughouly. We liked it.

Alex: Doesn't look like the they've responded to our issues. Ping them?    Kenneth is now on it.

Peter: will push it 2 weeks

#### [293 - TAG Review Request: Stale-While-Revalidate handling in browser](https://github.com/w3ctag/design-reviews/issues/293)

Hadley: What is this about?

travis: (reads from the [explainer](https://github.com/dtapuska/stale-while-revalidate):  'The motivation for implementing stale-while-revalidate inside the browser is to allow fast update lifecycles of resources while allowing these resources to be used as stale for a limited number of times. These properties allow pages to load quickly using stale content but having the cached resource be update shortly thereafter.'

david: Feels like this is different for different resource types. For an image or font, you know how to replace it. For a script, you can't just execute a script and replace it and act as though you executed the second not the first.  Is that the idea here?

Travis: I get the sense it's supposed to revalidate in the same session, after.

DDSangwhan: Yeah, scripts would be trickier

Yves: Wants to have some guarantee that the requesting resource would be served stale only once.

Alex: Yeah, you would get it from the cache.

Yves: Depending on the origin of the request (preload, regular fetch, etc) it should behave differently. Design decision of the implementation.

Peter: So... extra time?

Travis: We have some immediate feedback.

Yves: Would be good to get feedback from other browser vendors. The definition of stale-while-revalidate aaacame out of IETF, from the HTTP working group.


#### [292TAG review requested: Feature Policy JS introspection API](https://github.com/w3ctag/design-reviews/issues/292)

Travis: I like the sound of this one

Hadley: I found a nit. In 7.1.1. there is a typo 'To retreive'.

Kenneth: I'l'll join this. Wondering about 'allowList feature... in different origins'.  Why even 'list'? It's an array

Travis: it semantically matches classlist.



#### [282 - TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282)

Sangwhan: I'm on this

Travis: I'm interested. 

Kenneth: me too

#### [287 - spatial navigation](https://github.com/w3ctag/design-reviews/issues/287)

Hadley: I'm interested in this

Kenneth: like with a tv remote control... which direction to focus

travis: seems like an accessibility feature

alex: or a feature phone

...This is cool, the polyfill. Use your keyboard to try to get round it.



#### [281 - gamepad](https://github.com/w3ctag/design-reviews/issues/281)

yves: This isn't about the future of gamepad; it's the current spec.

kenneth: I know this works differently across browsers.

Travis: Do they have conformance tests?

Sangwhan: Tests agains the APIs existence are easy, but 'hey does this key actually do that...?'

Break-out: Sangwhan, Kenneth, Yves, Hadley

Dan: blog post on this topic from Samsung:
https://medium.com/samsung-internet-dev/the-gamepad-reloaded-5ba866770003



#### [280 - `sec-metadata`](https://github.com/w3ctag/design-reviews/issues/280)

Peter: there is some feedback here

david: it'd be good to bring in others 

...(Read Mike's third comment) 'I'd actually appreciate y'all spending a little more time on this in the somewhat near future, as it's something that turned out to be trivial to implement, and that doesn't seem controversial from the (few) conversations I've had with other vendors. It's feasible that we could ship it in the somewhat near future, and your feedback would be really helpful in ensuring that we do that in the right way.'



Peter: who else?

Hadley: I'm interested

Alex: me too

david: the idea is that this is adding metadata so that servers can do mitigations on cross site requests based on that metadata.


#### [279 - Background fetch](https://github.com/w3ctag/design-reviews/issues/279)

Kenneth: yeah, this is mine. Updating now. 

Peter  : discussion during f2f?

Travis: I think so

#### [278 - Async local storage](https://github.com/w3ctag/design-reviews/issues/278)

David/Kenneth: this is part of layered apis

David: I could join this

Travis: I've looked at this and have no issues with it.

#### [277 - WebUSB on Dedicated and Shared Workers](https://github.com/w3ctag/design-reviews/issues/277)

kenneth: the idea is that you do it all on the main thread and then transfer to the other side. 

sangwhan: Apparently they did an update

kenneth: we should follow up on that.

...So, extra time in our f2 

sangwhan: I'll join.  Add travis too. 

#### [276 - layered APIs](https://github.com/w3ctag/design-reviews/issues/276)

Peter: nothing to discuss right now

#### [241 Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241)

Hadley: What is this?  (reads from explainer)
 'This specification describes a browser API enabling developers to signal the priority of each resource they need to download. It introduces the importance attribute that may be used with elements such as img, link, script and iframe.'
 
 Kenneth: want your ads to load faster?
 
Travis: Feed into HTTP/2?

Alex: Last time this came around, Yoav was proposing 12 values (4 buckets with 3 values each). This has 3.

...I would like to see a way to rationalise the implicit priorities of various resource types. A way from fetch in a service worker to change the priority.

Travis:: isn't it too late?

Alex: It hasn't been dispatched to the network yet.

Yves: You hwant to have priorty or dependency trees?

Alex: Haven't dependency trees been a disaster in http/2?

Travis: I want to leave that to the module resolution algorithm

Alex: Question: how long are you going to wait?

Yves: Every time I saw priority defined like that, everything ended up at top priority. So it isn't helpful.

Alex: But dependency trees require more info. 

Alex: add me

Hadley: me too

David: I could be interested too, but I'm stretched thin.

#### [240- The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240)

sangwhan: this isn't a review; we're missing this.

hadley: what kind of services?

peter: for example, connecting to a calendar feed.  I ca type into my email address into a calendar find and it can look up a calendar service associated with my email address, etc. But I can't do DNS lookup in javascript. Calendar, XMPP, caldav, matrix, etc.

travis: do you want to expose that to the web app?

peter: yes. Now a lot use well-known URLs be3cause that's possible. It would be nice to have an API to do a higher-lever service discovery 

sangwhan: also, mDNS for local service discovery. broadcasting and TV industry.

alex: We looked at this for university networks: a local cache of content you can say is from the origin.  Not raw mDNS, but cors style the packets ssay they represent example.com. Discovery is consensual.

hadley: Also we have a big problem for discove䁲y of data on the web. wondering if there are overlaps. 

sangwhan: Depends on the format. If you eethe data as caldav, then it makes sense. But if it's CSV -- that's more of a well-known kind of thing. I believe mnot was unhappy about imposoing to much on well-known.

travis: smells like there's a registry in the future.

peter: taking to extra time.

[may be worthwhile looking for overlap with https://datatracker.ietf.org/doc/draft-hoffman-dispatch-dns-over-https/]

#### [239 - Deprecating nonsecure cookies](https://github.com/w3ctag/design-reviews/issues/239)

hadley: Wasn't Mike West nudging us about this?

dka: We'll be discussing that with him tomorrow.

david: this and 280



#### [237 - Changing requirements for Well-Known URIs](https://github.com/w3ctag/design-reviews/issues/237)

Peter: we were just discussing this for 240.

Sangwhan: we can probably disucuss them together


#### [236- Find-in-page API(s)](https://github.com/w3ctag/design-reviews/issues/236)

Sanghwan: I'm thinking this is not great.

Peter: we discussed this in Tokyo.

Travis: I don't have good feelings about this one either.

Kenneth: The publishers are interested. ePbuub. 

Travis: full text search

dan: there is an open find-in-page HTML issue too. Anne put it in the thread.

Sangwhan: that one seems a bit less dangerous.

Hadley: what's dangerous about this?

Sangwhan: command-F could become anything.  Like command-phish. with a p.  Replacing the browserser UI is concerning.

...Find-in-page as an API doesn't add security concerns, the one Anne referenced.

Hadley: add me too 

Break-out: Sangwhn, an, an, aan, Yves, Kenneth, Hadley

JKenneth: there are multiple things here.. the UI, etc...

Sangwhan: some of this is possible by other means

Kenneth: on PWAs you don't have a menu ... on android you have a menu item... 

Sangwhan: customozed ui, defining data outside of the dom tree, reflecting realtime data loading in find results, reretreating multiple pages as one ...

Dan: I don't understand the problem youre trying to solve..

Sangwhan: in android for example the search intent isn't an event you have access to... e.g. in cryptpad... I can see its uses.

Kenneth: it's used - people are doing it. Twitter have their own search  - they have virtulaised... not all data on the screen... so c-f searchdoesbot work.

Sangwhan: user should always have the ioption to go back to default in-document search behaviour. 

Kenneth: in PWAs you don't have a search UI - so I don't want to implement search ...

Hadley: what's the benefit for standadtizizing that?

Kenneth: common need
... I want to rely on what is in the browse.r in PWA I want to build my own search thing so it looks integrated. 

Hadley: when we talk about consistent UX implementers don't like it...

  We do standards not UX or UI

[reading some of some of the backlog]



#### [235 - Signed Exchanges](https://github.com/w3ctag/design-reviews/issues/235)

Peter: We wanted to bring Jeffrey into a call. Still need to do that.

Hadley: I'd also be curious to see what the HTTP WG's response to this was. 

#### [234 - Request Formal Review of Vehicle Information Service Specification ((VISS) CR](https://github.com/w3ctag/design-reviews/issues/234)

Sangwhan: are we okay with their wwwivi magical domain?

David: they said in section 7 that that is an example

Sangwhan: They said that it was because they didn't have a service discovery mechanism. 

Alex: So that would help?

Sangwhan: That part, yes.

David: wouldn't prevent security attacks on the vehicle

Hadley: Yes, but I think they wanted to minimise connections on the outside world. (which I'm not sure was going to work)

...Also,  a lot of this approach/feedback will be relevant for airplanes too

#### [233 - CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233)

Peter: postpone a few weeks


#### [232 - BCP56bis](https://github.com/w3ctag/design-reviews/issues/232)

Hadley: looks like we need to reenergise this discussion

David: And there is some info for the explainer in the answers here. 

Peter: break-out or no break-out?

#### [231 - Payment Handler](https://github.com/w3ctag/design-reviews/issues/231)

David: I did go through and respond to responses … I don't think we need breaktiout time but I will follow up on it. **ACTION**

Peter [bumps 2 weeks]


#### [229 - W3C DOM](https://github.com/w3ctag/design-reviews/issues/229)

Travis: there is a toggle API newly added to the DOM

... You pass in a second parameter which is a boolean, of how you want it to end up.  It semantically matches the toggle API of the DOM token list. So you can use it on boolean attributes like checked.

Kenneth: so what does that bring me?

Travis: it's convenient. They're playing with range... static range on one side and abstract range on the other. And sharing methods between them.

Sangwhan: Breakout on this one?

... I heard chaals is unhappy with this. There are intentional differences with WHATWG DOM?

...We should also review WHATWG DOM

Peter: Sangwhan and Travis, who else?

David: me

#### [228 - WebRTC Secure Context](https://github.com/w3ctag/design-reviews/issues/228)

David: this involves a bunch of different pieces, which are easier/harder to restrict depending on what it is.

Peter: Do we need feedback from someone?

Hadley: looks like they want us [to raise it on the webrtc-pc spec.](https://github.com/w3c/webrtc-stats/issues/347)

Yves: I'm doing that now... Done, see [w3c/webrtc-pc#1945](https://github.com/w3c/webrtc-pc/issues/1945)

#### [227 - Web Components Guide](https://github.com/w3ctag/design-reviews/issues/227)

Peter: I think we need a break out on this.

Kenneth: Add me


#### [224 - CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224)

Peter: we decided in houdini to switch back to promises

David: yes

dan: so do we close this?

travis: I didn't yet break this into individual issues. Should I still?

... it would probably be just as valuable to re-review this when they're ready to ship. None of the feedback was as critical as that promises/gnerators issue

...I'm satisfied with this result. Happy to close this and see another iteration in due course.

Peter: done

#### [223 - TAG review for CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223)

David: a few of my issues from this are still open.

Peter: so should we bump the milestone to later?

Alex: What can we do to resolve them?

David: one of the issues is fundamental - it's missing a big chunk of stuff if this is going to be interoperable. [718 in their repo](https://github.com/w3c/css-houdini-drafts/issues/718). 

Dan: can we link these from our issue, so we can trace them better?

David: sure

...I'm not as worried about the range restrictions ones. Needs to be sorted out though. 

...I don't feel the need for a breakout now though

Peter: Will move this milestone forward then



[221 - Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221)

Alex: I'm inclined we close this and ask if there are detail they want us to pay attention to. This is a clear success case; the design has changed a lot.

Kenneth: there are a few comments from Matt that need a response

Peter: so no breakout time then?

Kenneth: is this being implemented now?

Alex: yes

Travis: File support?

Alex: it's coming. Look at the bottom...  Oh no, you're right.

Kenneth: not in the initial version. 

Alex: You should be able to get file data, but it's not clearly described in the examples.

Hadley: they do say that the examples in the explainer are out of date.

Alex: I'll leave that feedback. Are we still happy to close it?

All: yes.


---

10 minute break, back at 11:00

---


## Privacy and security questionnaire & user consent workshop

Guest: Wendy Seltzer, Sam Weiler (w3c staff), Christine Runnegar (Privacy IG co-chair)

dka: This ties into the User Permission and Consent workshop. Lukasz is on the program committee for that. 

[connectivity issues]

[and discussion of how webRTC doesn't work when you've disabled the privacy-invading features of the web]

dka: 2 issues to discuss: upcoming User Permission and Consent workshop and the security and privacy questionnaire.

Yves: and an IETF update please?

dka: And anything you want to raise?

wendy: I would love to follow more what you're doing. I keep losing modalities of owrk.

alex: most happens in github issues, our design-reviews repo.

hadley: I also try to tweet and post on mastadon he our minutes and the big-picture stuff of what we're up to.

dan: Let's start with IETF then. What should we be aware of?

wendy: Now that everyone's here, let's talk about the relevant updates for the Privacy questionnaire.

dka: Can you share the latest version, Christine?

Sam: We decided to use the TAG's version, so we've been submitting PRs against that version.  

dka: Are we responding? (Expecting not...)

Sam: We only did this a week ago. 

dka: Understood.  Sorry.  
[Privacy and Security Questionnaire PRs](https://github.com/w3ctag/security-questionnaire/pulls)

...Let's talk through them.

Ch
Christine: We have in PiNG a number of draft documents that deal with privacy guidance. We've worked on cleaning them up and deprecating them. Looking through the latest version of this questionnaire, it occurs to us that we'd like to pull in the relevant guidance that isn't in there. We'd like to support hte TAG in continuing to flesh out this doc to being a questionnaire with guidance.  How best to do that?

[Privacy Interest Group home](https://www.w3.org/Privacy/IG)

dka: Other complicating factor: We put Lukasz, relativekly recently joined the TAG on a platform of privacy protection, as editor of this document. Unfotuanrtunately he's not here. 

...So we're not fully supportive right now, not beause of these ideas. But because he should be working with you to make this happen.

...I'm open to other suggestions of how to do this though. Co-editorship? 

Alex: If we can talk about these, we can maybe get these merged and then talk about next steps.

Hadley: Sounds sensible to me.

Sam: Sure

#### [29](https://github.com/w3ctag/security-questionnaire/pull/29)

Sam: This is just editorial

dka: Okay, I'll merge it. 

#### [31](https://github.com/w3ctag/security-questionnaire/pull/31)

dka: In the context of additional info?

Sam: this explains why access to devices can be harmful in less-than-obvious ways.

Alex: What are we asking the designer to do? WE are obviously making them aware of the potential of attack. But can we generate a ch3ecklist to help them understand that? Or are we asking them to enumerate the set of devices they might be exposing to?

Sam: You're asking what is this editorial change. WE didn't explain: If you take the documets that you have, and we have 9, and if you consolidate the useful bits into the TAG document and deprecate the duplicative and not-relevant documents.

dka: I don't know the content of hte other documents. The feedback we've had so far on this checklist is quite good, in that working groups have been using it. I want to make sure whatever we add is useful info.

alex: I don't have a problem with this, because it enumerates what can go wrong. 

Hadley: I think there is a difference between a treatise about privacy, versus creating something that meets the user needs of a spec author in their journey of writing a spec and designing a new feature of the web platform.

Christine: We agree with that. We don't want this to be a dumping ground. We were hoping to work with all of you - and Lukasz - on this.

dka: That sounds great. And as Hadley said, we want this to be relevant to the user needs, where the users are the spec authors.

...I'm open ot what the process can be. It feels like you and Lukasz should work on evolving this document and then the TAG can go through a review process. Does that make sense?

Christine: Yes it does.

Sam: I'm going to disagree. I think that imposes a degree of process that makes things more challenging.

Hadley: can you explain?

Alex: Is the proposal that there will be a branch that folks can merge at will, and we will decide at some point to publish that? WE can do that pretty often (each face to face, for example). I want to make sure that we are not talking about everyone reivewing every change.

Hadley: agreed.

dka: I was thinking we would open this doucment on github to yourselves to work with Lukasz on iterating it, as a draft, and then at some point in the future, we do a review step as the TAG and say "we're happy to post this as an update from the TAG." Mimicking the process we have for other W3C.

Hadley: Sam, what were you concerned about?

Sam: That we submitted 4-line editorial things that didn't get merged. And we could end up with conflicting merges. It woudl be frustrating.

Alex: If we all agree that work would happen in a branch, and you had the ability to mange that branch... would that solve that issue?

Sam: Sure.

(Lukasz arrives. Dan brings him up to speed.  We are talking about how to edit this document with Sam and Christine from PiNG. The proposal on the table is that we open editing rights to the document to Sam and Christine, and that you Lukasz work with them)

Lukasz: I'm up to date from the transcript.

...I did work on the questionnaire today a bit. I think it should be reworked, modifying some questions and filling the gaps. For example, figuring out the threat model. I would ask not to work on this and maybe wait until I post what I have.  And then we can go further. The last version is from 2015.  Things have moved on in technical terms.  Again, let me just finish modifying this and I will then share it with the TAG and other interested people, if that will be fine.

...Originally I had something finished soon, though I am quite under pressure. I wanted to present something at TPAC.

Alex: I'm confused.

Sam: I need to switch connections.  Can we come back to this in a couple minutes?

Dan: Lukasz, you don't need to repeat.  Sam is having webRTC problems and suggested that we move to a different part of the discussion. But I don't know what part, since the other part of this discussion is the workshop, which we need Sam for too.

...And we have a communication problem here that isn't helped by the multpile audio and video problems.

Lukasz: To recap, I am working on the questionnaire. I want to finish that at some point and share it.  

dka: On the document: 

Alex: can we find a co-editor for this document? It would be seful to have more conversation within the TAG.

dka: Lukasz, you mentioned that you are doing edits to the document. In github or offline?

Lukasz: In google docs. That's easier for me.

dka: We need to be responsive to the request from the PiNG that they would like to have input into htat document as well. If it is a google doc, then you could share that doc with Christine and Sam? and we can collaboarte there?  HOwever we do it, we should be open to their input and expertise.

Lukasz: I'd like to do the first edits on my own, and then share it. But maybe that isn't a good idea.

Alex: This is what source control is for. I would suggest that we handle these all as pull requests to discuss each one. I think we had moved on to a separate discussion from the one about how to unblock this for PiNG, who want to make changes and we've been stopping them.

dka: That's true, the edits should be happening in Github rather than in google docs. Maybe we should set up a separate call betwen me, you Lukasz, Sam and Christine?

Alex: Can we solve it in this call?

Hadley: We can't hear Lukasz, so I can't minute it. 

Christine: I notice that Lukasz said he's working off a version from 2015. But the latest version is 2018. So I want to make sure he has the latest version.

Alex: I think we all support working off hte master in Github

Lukasz: I am working off the document in github.

David: The website was not showing master until last week when Wendy noticed and I fixed it. So if Lukasz took his version before last week, he is seven commits behind. 

Lukasz: I took this version in January. 

Dan: Yes, but as David just pointed out, there was an issue that it wasn't up to date. So some of the changes you've been making need to be worked back into hte document in GitHub. Can you do that as a series of pull requests? So we can update it to where it has your input?

Alex: I'd like for us to agree on a work mode. That will solve all of this.

Lukasz: I've changed some of the questions. My desire was to have a complete document. There is a different document now.  

Alex: Can you make your edits via pull request on github?

Lukasz: I can do that from the google doc.

Alex: I think it would be best if we do it all via pull requestrs. Is that okay?

Lukasz: It would take some time, especially the discussion. 

Hadley: It lets us have the discussion for each of the changes you want to make, and involve the PiNG community.

Lukasz: So you want me to look at Google docs and see where it has changed from the master.

dka: I can help with that. Next week.

Hadley: I can help too. 

Lukasz: What do you mean by help?

dka: going through your changes and acting as a reviewer.

lukasz: So yo uwant me to stop making changes in the google doc and start making pull requests instead?

dka: yes. And then we can all work off the same document and we can start to incorporate the changes that the PiNG group have been working on. Which I think is worthwhile. And we can keep a focus on making this the best document it can be.

Wendy: Thank you - I think it's important to have one source for the guidance and info we are giving to spec editors. Having one source for that document will improve everyone's experience in the long run.

lukasz: Some of my changes are driven by how this questionnaire has been used since 2015. 

Wendy: That sounds helpful!

Lukasz: My question: would you be open to these changes even if they are breaking changes?

alex: Yes! please file them as pull requests.

lukasz: i will provide you with an example. 

... I wrote a chunk of text in the introduction. One change that might not be incorported at all is on the threat model:



>  2.5. Legitimate Misuse
>
> Even when powerful features are made available to developers, it does not mean that all of their uses should be justified; in fact, data privacy regulations around the world may even put limits on certain uses of data. In the context of first party, a legitimate website is potentially able to interact with powerful features to learn about the user behavior or habits. For example:
> Tracking the user while browsing the website via mechanisms such as mouse move tracking
> Behavioral profiling of the user based on the usage patterns
> Accessing powerful features enabling to reason about the user system, himself or the user surrounding, such as a webcam, Web Bluetooth or sensors  
> 
> This point is admittedly different from others - and underlines that even if something may be possible, it does not mean it should always be done. When designing a specification with security and privacy in mind, all both use and misuse cases should be in scope

...I wanted to change question number one to this:

> 3.1. How does the specification deal with personal information allowing to single out the user?

...This also provides a context for the editors that the feature could be misued. Also for question one was supporting the old style. I didn't find anyone saying the answer to question #1 is "no". So it wasn't useful for us; the important information is how.

dka: That makes sense. 

lukasz: Because of that, I've been working in google doc.  Some of the changes are conceptual in nature.

dka: Okay, right. So we need to make those changes into pull requests and include the ping people in that. And then we can merge them.

hadley: one of the benefits of pull requests is that you can explain your thinking.

lukasz: how does it work?

dka: So we can have that discussion in each pull request. We should aim for having a full version for TPAC. 

hadley: the other reason to put the rationale into the pull request is that we can then involve others, and have a record of our thinking.

dka: Then at TPAC we can have a broader discussion about the whole document. And gather feedback from attendees.

lukasz: These kind of changes - make existing questionnaires obsolete.  What is also important is to write how this should be used. I think it should be mandatory. In the process document. Mandatory to become a recommendation. 

dka: That sounds good. I think we have a plan. Christine, does that sound okay to you?

Christine: Yes, thank you.

dka: will you be at TPAC?

Christine: I don't think so, but I think my co-chair Tara will be.

dka: Should we talk about the workshop on user permission and consent?

... Logistical question: Are the dates set? I'd heard that someone wanted them changed.

Wendy: I'm checking... Found out whiel at IETF tha tthe dates conflicted with a QUIC interim meeting, and the Mozilla folks were previously committed but wanted to attend our workshop. Sam has shared that with the program committee.  The idea was to sort that this week; either for the as-scheuled week or the week following.

Hadley: Peter,are you attending? Does the date change matter to you?

Peter: I will be there. Either week is fine.

dka: I won't be there but someone from my team will.

Wendy: we know people want to know ASAP.

dka: There wa a twitter discussion between Robin Berjon and Dom today, and Robin was wondering if regulatory authorities would come/be invited. Sounded like a good idea to me. Thoughts, Wendy?

Wendy: the goal of the workshop is broader than legally relevant consent. Could be a useful to have a session on that, like with GDPR. Certainly we should invite regulators to join. The broader subject is: how do we convey info to users, when do we, about features that that they might or might not want enabled. What is the connection betgween interface design, user agents, what guidance to spec authors and implementors about how to think about htis.


dka: I was co-chair of a predecessor workshop, 10 years ago.  Device APIs permission workshop in 2008 at Vodafone in London. It was intersting to reread the proceeds of that workshop as a prep for thinking about this topic.

[Security for Access to Device APIs from the Web - W3C Workshop 10-11 December 2008, London](https://www.w3.org/2008/security-ws/)

...For that workshop, my statement was: it's worth reviewing that stuff, but we have so much more knowledge now about the real use of these powerful APIs and permission-driven APIs (and the misuse of them and antipatterns that have crept up around permission promts, gaming user consent etc) - we're now at a good point to rethink all this.

...I hope it isn't too abstract. We need this to be rooted in the concrete.

wendy: Yes. In our tweets and publicity around it, we should be encouraging people to submit real world examples, user studies, etc. because we also know more about how users do and don't react to prompts. That could help us to do better for the future.

lukasz: How about the research work I did messing around with sensors?

dka: Yes, exactly.

... Are we done with this topic then?

wendy: did you talk about the potential TAG/IAB workshop on AMP and packaging?

alex: no

dka: No, it's up in the air. I've been talking to Robin Berjon about maybe them hosting in New York. It's on the back burner right now.

wendy: Okay. Another IETF conversation - Jeffrey Yasskin was talking about the web packaging work. One of the concerns in the room was, is there intrest in standardisation and is there time for it? Does it fit with what Google wants to do? This workshop was another potential piece of input on that.

dka, alex, hadley: +1

dka: We haven't discussed it in detail yet. Maybe we need to. We do have a lot to get through this week, and it didn't look like that workshop would happen until late this year or early next year.

wendy: okay. I will come back to you if I have other specific agenda points.

(Wendy, Sam and Christine leave)


(Ralph leaves)

---

lunch break

---

[278 - Async Local Storage](https://github.com/w3ctag/design-reviews/issues/278) & [Layered APIs](https://github.com/w3ctag/design-reviews/issues/276)

-With special guest star, Ojan Vafai.

plinss: discussing layered APIs and async local storage

ojan: happy to introduce them. We can asseparate layered APIs from the details of the async local storage's API

ojan: we can perhaps discuss layered APIs, the problems theyr're trying to solve, and if it's the right solution

(discussion of what to tackle first; Travis suggests layered APIs first -- including groaner joke)

ojan: we see developers pulling in way too much code. I spent a weekend trying to learn MacOS Cocoa and all the introduction examples were really simple. "set up an app, use a UITableView, etc.". Everything puts you on a happy path. Web equivalent doesn't exist. Web tutorials aren't friendly.

ojan: I recently tried to do this again with an infinite list; couldn't easily decide which one was going to be a "good one". So our goal here is to ship more high-level APIs with the browser so the out-of-box experience is good and you won't need to download tons of bytes on the wire to do relatively basic stuff.

travis: you're going to get universal agreement (in this room) that shipping fewer bytes over the wire for a good experience is good

dan: I agree with what you just said about the out of box experience. That resonates with me and everyone who does educations of web developers feels this acutely. Particularly if you're trying to convince app developers to move to the web. 

dan: what you're describing is also a characteristic of the web being crowdsourced..., er, open

alex: but it's not all crowdsourced. There's a library of built-in stuff that is browser provided.

dan: what's the review process? who's designing these new APIs? where are the APIs going to be designed?

ojan: let me talk a little bit about the constraints we have in mind, then discuss standards process

ojan: first constraint: make more of the APIs "pay as you go"; every API we add gets exposed in the JS global scope, and toots of accidental dependencies. The second issue is that we think that to make these scalable, we want them to be decoupled more than the existing platform is. The ways we want to achieve that is to make sure they're built in a layered way -- as things built only with capabilities available to web developers.

ojan: 3 options for build/standardize; all options use existing standards processes -- existing CG/WG processes. What gets produced might be different. Variants:
 
 1- exactly the same as today, specs can only use things exposed to web authors (no magic). In this case, standards process is largely unchanged
 - another variant suggested by Bobby Holley at Mozilla was a different process where there's a single implementation and everyone shares that. "Standards process  " would define what goes into this library
 - no change; no process around decoupling
 
(some discussion of history of 2nd idea)

david: what I think Bobby was pushing for was that based on the assumption that there is a single implementation, a constraint on ensuring that there wasn't any magic -- a requirement that it all designs only do what JS developers can
(see clarification below: ... that they not be privileged by browsers)

travis: I think there _are_ advantages to a layered; in-js approach. Specifically in speed; uptake could work faster. Development could allow for more fairness. Allowing things to move faster is a benefit that library and framework authors enjoy today. I don't know if that aspect is a concern?

alex: in my conversations with ojan nobody proposed relaxing the stringent backward compatibility goals we use when designing new features today

ojan: one of the difficulties I see with libraries is that they're built for today's browsers but they don't rework their implementations to be targeted at the latest versions/capabilities. They get bloated and slow (relative to a moving target)

travis: they need to cater to multiple browsers, right?

ojan: right, but they don't need to cater to legacy

ojan: versioning these things causes problems. We've analyzed several times the idea that we could "just precache popular libaries". JQuery, e.g., is used very heavily but the most popular *version* of jQuery is only used on 1-2% of pages. Authors know how to deal with browsers not having versioning.

travis: speaking as someone who built IE 9 (that included many old versions of IE), versioning is hard (scribe fail)

plinss: so folks would have to polyfill if they don't have the most modern std lib?

(yes)

alex: new high level features might need to go hand-in-hand with new lower level capabilities

plinss: can these be loaded directly from the network?

ojan: an open problem is this sort of versioning that isn't tied to the browser version. Chrome 40 with std. lib. version 50, e.g.

ojan: we've heard from develoeprs that a complex matrix of versions to support is hard

travis: can you say more about why the versioning thing didn't work?

ojan: defeats the goal of "don't download tons of stuff". With versioning, you don't get any caching benefits in practice.

travis: in terms of user habits, many users only use a small set of the web. I'm interested in pursuing better caching. You maybe need to indicate what your library "is" and what version it is.

ojan: dbaron, was interesting to hear you say that Bobby wasn't actually requesting a single implementation; we thought the mozilla position was a *request* for a single implementation

(discussion of the history; TPAC last year -> today)

ojan: we don't feel strongly in either direction regarding inumber of implementations.

dbaron: a key request from Bobby was that we not use the power of being browsers to "force" one particular set of APIs onto developers by abusing browser power.

dbaron: we don't want the browsers to force one set of things on people when any other set of people can do the same thing too.

travis: that's an interesting counterpoint to the Cocoa example

ojan: working through a compromise. There's a "Package Name Maps" proposal which is sort of a low-priority proposal, but we might use it to map a namespace to a URL. E.g., ``"amazon-infinite-list"`` -> https://amazon.com/...

ojan: what we're working through with Bobby is the idea is that there would be a default package name map to browsers. E.g. `std:...` -> https://webstandardlibrary.org/...

ojan: so there is a default and that's the benefit you get.

travis: let me see if I get this. So there's a name for an infinite list. That name is a configurable map. You can get weak/enhance it.

ojan: right. Node wants to use the general capability to map node module specifiers. Folks can use the standards stuff or pull from another namespace.

travis: ok, I think I've got it.

ojan: so there are positions on this spectrum. You could continue to spec as today, and browsers can implement however they want. Another path is a JS implementation and a map and browsers are only priviledged in shipping the map. browsers can pre-cache stuffif they want.

alex: is there any browser that *wouldn't* do this?

dbaron: depends on how many & big they are

ojan: e.g., I'd like to ship MathML but wouldn't want to precache as it won't be that popular. And what about ChemicalML and MusicML (+others) ? Can imagine not precaching for these niche things.

travis: my off-the-cuff reaction is that I like the map/name-binding proposal.

alex: nothing about it requires a browser vendor to use that implementation

ojan: everything we're discussing is an implementation details from the perspective of web developers

travis: can developers participate in the map? need to figure that out.

ojan: right, overrides.

travis: MSFT's thinking has been evolving. Were initially cautious about implementations not working as well on, e.g., Edge as Gecko. We're getting more comfortable with the idea of working on something that can produce a shared library. Adrian Bateman even suggested that there could be a more lightweight organsiation to develop this.

ojan: I've been wondering similar things. I think you still need standards and specs and tests. YOu still need a spec for the implementation surface.

dan: does this sound funny to anyone else? Over the last 10 years, we've moved from "you just need the API surface" to "you need a full algorithm". I'm extremely concerned.

ojan: it opens up the opportunity to share, but we're happy to continue to write specs (etc.)

dan: I'm concerned about this; feels like shift in the balance of power. Today you have to get buy-in from multiple implementers to move stuff forward. If we're talking about a standard library, now it's a single group that has control over that behavior.

ojan: I share that concern

travis: I had that reaction too. But then you think "today, the power is held exclusively by engine implementers...this other model expands the power to a larger group, people who are expert JS developers and framework authors". 

dan: it feels like a *really ambitious* open source project.


sanghwan: individual modules can be more scoped

ojan: emodules could have a contiuum of maturity. Shipping guidelines that browsers use today could be used; "lots of people are using this, we are comfortable shipping this".

ojan: with a single implementation, you lose the variety of implementations. As we see in design APIs, we get good feedback from other vendors about how things will/won't work in other architectures

dan: that is concerning. We've come across a few things just this week where APIs reflect different concerns. How will implementer issues get resolved (e.g. around a11y, privacy, etc.) in this world? This is where standards play a role today.

ojan: how is that handled today?

dbaron: some of that is different if it's all on the basis that things are fully layered APIs. If you're writing it on top of existing stuff that everyone has, some concerns go away. But you're left with concerns about performance differences.

ojan: continuing to get input from marginalized groups wouldn't be different

travis: we keep fgetting questions at "Meet the TAG" events about "how do I get involved in web standards?"

ojan: working with a framework team here on the infinite scroller has shown that

sangwhan: this feels like the web platform version of Boost TR1; polyfills for C++11 done in userland.

ojan: conceptually very similar

sanghwan: in the many years of the Boost experiment, there have been breaking changes and it has been easier to do versioning because it's local

alex: ... Browsers designing and shipping features before standards are finalized... what is the maturity signal that will cause a browser to expose a feature in one browser?

sangwhan: another platform which didn't have versioning just introduced it after many years of being unversioned - Go 

alex: ... origin trials can work with this... 

ojan: if we realy need we can make a breaking change we can make infinite lists 2.

ojan: if someone can come up with a way to introduce versioning in a way that works, I'd be open to it, but create as any problems as they solve

travis: if we want to enhance qSA, e.g., we have to be measure and be careful.

ojan: also need to figure out browser release process. If there's a standard name mapping, changing one could break a large % of the web. Browser vendors will want to be in control.

alex: what's the minimum set of things you want to achieve?  If single implementation was thrown out -- all traditional standards bodies, traditional design mechanisms, etc.?  deal-killer if not modules, deal killer if not always layered?  What's the minimum things you want to achieve with this effort?

ojan: layering and pay-as-you-go.  Modules seems like most straightfoward way to get pay-as-you go. Those seem like the critical bits for us. Talking to Bobby at Mozilla, he wanted to add the "unpriviledged" bit; taking layering a step further.

alex: should we talk about async local storage?

dan: I'd like to understand what the governance model?

alex; async local storage is being proposed in a way with some existing governance; maybe we can look at that?

ojan: layering is sort of nuanced. Maybe we can talk about that?

ojan: async local storage (ALS) doesn't use WebIDL. That's the big difference to a traditional web API.

travis: so you wouldn't see a WebIDL interface that hat references a bunch of steps?

ojan: you still have "when this method is called, do these 32 steps", but how the method is exposed is expressed in JS

ojan: if you look at the spec, there's a JS snippet that *is* the normative JS surface. There's also a "see below" to to to to describe behavior.

alex; a lot of our design guidance is about dealing with WebIDLisms. We talked about "JSIDL" years ago to try to work around. I'm predisposed to like this direction as a result.

ojan: that and the ssimport system are the only things that are really different

travis: (outlines exact differences to existing practice)

aaaalex: this is happening at WICG, right?

ojan: will, yes.

dbaron: regarding defining things in JS;;, are you trying to say "this is just like if it's defined in JS" when, e.g., someone messes with Prototype chains? Is that normal JS behavior a requirement? An anti-goal? Either?

ojan: one of the things we're working on -- as we implement this in JS -- is a proposal we're sharing at TC39 called `getOriginals` which gets you the "original" versions of functions so we can implement these things in a more defensible way. So we can use `Array.push` without exposing it., e.g.

ojan: the way we're planininning on doing this is to wrhhhite these things in something like TypeScript and write a compiler that consumes that. We'd want to m the library not call it's own exposed methods, so overrides wouldn't affecat behavior.

dbaron: `Array.push`???

ojan: `getOriginals` is our solution to that

dbaron: mozilla folk were concerned by `getOriginals` because we've had a lot of experience with things in Firefox frontend code that interact with page DOM and things in JS engine that are self-hosted. Boris Zbarsky has opinions/information.

ojan: our V8 team had the same feedback. hardest part is building that tooling. We are optimistic. Hand-written, this would be sort of crazy.

travis: since this is loaded by module import, can you get these original?

travis: how late can you bind those? Do you need to do it up front, or can you load it after it's been running for 10 min?

ojan: `Array.push` you need to do up front, pupubinding the ALS can happen late

sangawhan: what if a layered API depends on another one? What if you call `getOriginals` on one of those?

travis: browsers have different techniques for this sort of sasandboxing?

alex: this will have to be spec'd right?

(agreement)

kenneth: dwn to layered APIs to avoid this; what's the order re: monkey-patching?

travis: same as libraries today, but they don't do the right thing

ojan: we discussed w/ Domenic, not sure where that landed

ojan: dependencies and prototypes -- preferred solution is to expose ability call `getOriginals` on most things, including for user-land libraries. Hoping TC39 will help us come up with something.

(WebIDL: love? hate? ambivalent!)

ojan: our goal is to test all of this out with ALS.

travis: it'll be an edgecase; always is

alex: (recap what's new/different vs. what's not; this looks almost exactly like existing standards development but with modules and without WebIDL)

kenneth: will there be new things with virtual scrollers? E.g. optimisations you might make for scrolling and the compositor thread?

travis: something you didn't mention is that uncovering things in the platform to make these features run well might happen

ojan: we view that as a plus.

ojan: for scrollers, specifically, lots of existing systems don't work well with browser features. Githubs's editor defeats scfind-in-page, tab order is busted, etc. We're exploring new primitives to help developers improve these implementations; not just ours.

kenneth: even things like `position: sticky` won't work; what are you sticky to? Can't use `position: absolute` with transforms.

ojan: will need to work all of this out with virtual scrollers. Current plan is to use the existing process; very open to suggestion about how to do this in the future. wnwwLooking for feedback from other vendors about how they want to work.

ojan: please reach out! We're mostly stuck on figuring out who to work with.

[279 - Background Fetch](https://github.com/w3ctag/design-reviews/issues/279)

Spec: https://wicg.github.io/background-fetch/
Explainer: https://github.com/WICG/background-fetch/blob/gh-pages/README.md

dbaron: is this for snc w/ the SW involved? or for large file transfer when SW might be shut down?

alex: the second

(discssion of when SW is started up)

alex: (explains why API models an operation about many URLs rather than individual requests)

(discusison about spoofability)

dbaron: skeevy websites might say "deleting all the files from your HD in 120 seconds unless you pay us bitcoin" or something...maybe the UA should be in control of the upload/download wording?

alex: noting that there's no permission. Seems bad. Even if it was going to be widrrely granted by default, should probably be modeled that way. You want to detect this.

alex: isn't this jsut the Notification permission?

alex: what about partial success?

travis: MSFT's progress bars hhave changed their behaviors to late-report failure to help accmodate partial success.


[218 - Media Capabilities](https://github.com/w3ctag/design-reviews/issues/218)

[216 - Decentralized identifiers (DIDs)](https://github.com/w3ctag/design-reviews/issues/216)

[214 - Dusting off Web Speech API?](https://github.com/w3ctag/design-reviews/issues/214)

[213 - `<link rel="modulepreload">`](https://github.com/w3ctag/design-reviews/issues/213)

[208 - import.meta.url, and import.meta generally](https://github.com/w3ctag/design-reviews/issues/208)

[207 - Sensor APIs](https://github.com/w3ctag/design-reviews/issues/207)

[201 - ads.txt](https://github.com/w3ctag/design-reviews/issues/201)

[199 - Gesture Delegation ](https://github.com/w3ctag/design-reviews/issues/199)

[197 - Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197)

[187 - ResizeObserver](https://github.com/w3ctag/design-reviews/issues/187)

[185 - WebVR](https://github.com/w3ctag/design-reviews/issues/185)

[182 - Image Decode API ](https://github.com/w3ctag/design-reviews/issues/182)

[178 - Serialization of natural language in data formats such as JSON [I18N]](https://github.com/w3ctag/design-reviews/issues/178)

[141 - OffscreenCanvas, including ImageBitmapRenderingContext](https://github.com/w3ctag/design-reviews/issues/141)

[138 - Timed Text Markup Language 2 (TTML2) ](https://github.com/w3ctag/design-reviews/issues/138)

[134 - Accessibility Object Model ](https://github.com/w3ctag/design-reviews/issues/134)

[105 - TV-Specific Web Subsetting](https://github.com/w3ctag/design-reviews/issues/105)

[101 - Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101)

[76 - with credentials](https://github.com/w3ctag/design-reviews/issues/76)

[72 - Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72)

[62 - Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62)
