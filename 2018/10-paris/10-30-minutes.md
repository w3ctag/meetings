## TAG F2F Paris
##### 30 October 2018

Present: Lukasz Olejnik, Kenneth Rohde Christiansen, David Baron, Travis Leithead, Alex Russell, Sangwhan Moon, Daniel Appelquist, Yves Lafon, Peter Linss, Hadley Beeman

Regrets: **(this space intentionally left blank)**

---

Agenda:

### Privacy & Security Questionnaire

https://w3ctag.github.io/security-questionnaire/

([diff for the past 6 months](https://github.com/w3ctag/security-questionnaire/compare/61520b7d65ebf0404097a82164add05e7fdf83f1..HEAD))

Lukasz: recap: we looked over the document in february. /january. We started to work on this document over the summer, then collaborated with Ben. Ben was able to have a look and see the spirit of it.

My main concern based on my research and all that, was that we did not have adequate details.

It doesn't really provide a context.

Dan: People are not thinking deeply enough about the answeres when answering.

Lukasz: right. The main spirit was to reformulate the questions and give some context and promote the thinking of the privacy and sec at the beginning.

People could then update answers later, more like a process than a checkbox excerercise.

Almost gone through all the items and worked together with Ben. Chapter 3 is almost functional now - about ethics. This document now is also useful for web app developers.

They will probably find it useful too.  

All questiosn are being reformulated and each would have an example  . We are looking for things that went wrong or could be improved and how. it is used in different specs.

Dan: I have a question about the intro - 4th paragraph, this consideration is mandatory. I don't think we can say that.

Lukasz: Well we can ...

Dan: Not from process perspective, but we can make it a strong case for a TAG review.

Alex: What document is being edited.. the markdown file hasn't been changed in a while

[People looking]

Lukasz, OK so we cannot say that??

Dan: We [TAG] cannot say, no. But we can use strong wording about our own ATAG review process - if you want a good TAG review. Can someone suggest wording for that?

Lukasz: I want to use the strongest wordingding 

[discussion around strong wording - take the word mandatory out]

Dan: Other than that, I reviewed and was happy with the result. What is the level of discussion between you and the PING group.

Lukasz: We are collaborating quite nicely.

Dan: We think PING is happy about how this work is going and the working mode?

Lukasz: I don't know - I don't participate in the internal PING discussions around that. That could be rediculous (be in 2 at the same time). I'm communicating with Jason as the PING's envoy.

Lukasz: They are suggesting changes and we don't always agree ... but generally I think there is progress. Requires some negotiations.

Alex: The doc got quite large - my concern is that many of the additions are not in the right section. I suggest that we remove all those additions - they don't seem to add much.

Lukasz: We are not finished, only past half. You can look at it when it is done.

Alex: We have created a tool for our users to navigate a tricky area and we ask them to get them to take what is in their head to share that with us. I believe the value is that this is a tool.

Sangwhan: These should be tripwires and we should not add more process overhead.

Alex: strongly agree with that

Hadley: we have been using this as a document to help prompt developers to think about the security and privacy implications of their features. rather than what we're asking them to tell us. If we're going to use it in both ways, we should be conscious of it

Sangwhan: I believe that if we want this to be part of our review process then we might want to split into two questionnaires. I've been told from many spec authors that filling it in is quite a lot of work

Dan: I've been told by many people in the W3C that the questionnaire is very useful. That was the Mike West document that was already pretty long. We're getting good feedback from that

Alex: but Lukasz's point is that we aren't

Peter: We should split the intro out into an explainer

Dan: What do you think about that?

Travis: +1

Lukasz: Explainer of each of the points?

Dan/Peter: No... the intro

Lukasz: So the context should go into the explainer?

Dan: Yes. Let's make it as simple as possible

Lukasz: Most of the context is in the questions anyway. I won't say this is a problem because it is quite short - the intro is not that much longer than int he Mike West version - the questions have much more context. A lot has happened since then - we found a lot of security issues etc. The context is for the authors to understand these issues and stop repeating them same issues.

Hadley: If we disagree what our users need, let's ask them?

Dan: Are you opposed to move the thread section and intro to a new document.

Lukasz: Yes until the doc is all finished. The core value is in section 4. That is the core issue. I do not feel that it is a problem having section 1-3 there. We might remove theory sections.

Hadley: I might be inclided to scroll over intro etc to get to what I need - but I might not be like most of our users, let's ask them.

Lukasz: Do we have indications that it might be too long?
Travis: I wonder if we could support the goal of streamlining the document by using summary/details to hide the details for each question and just present the question summaries...?

Lukaz: I want a self-contained document, as short as possible.

Hadley: Point 4 doesn't reference the other pars of the doc... we can split the other parts out. It won't be confusing to work with.

Lukasz: Then you assume the reader already knows all this.

Sangwhan: I have some concerns about the list of references/blog post. I'm not sure that has the durability requirement that will last a while... Should probably reference a finding, but personal blog post maybe doesn't belong.

Alex: we shoudl be referencing the most authoritative sources...

SM: There is open research on this matter; esp. related so shader exploints.

Lukasz: value (e.g., mixed-blend) is that we are presenting relevant case-studies and examples. I'm not aware of these case studies you mention...

SM: See ACM-link, archive, etc...

Dan: Some of your linked resources have been referenced in the Tech press. We have a history of referencing these...

Lukasz: tech press don't provide details. The idea is providing examples that show how one can look at misusages. To promote a way of thinking and also how some work in development was found to contain a security issue.

Dan: PING might be able to help with that

SM: Is there a peer reviewed paper? like in a journal

Lukasz: Yes/no... no one is accepting these in conferences. Want to provide value, post a blog post. Top tier conferences don't care about many of these cases - not clever or important enough.

Lukasz: the document is not just about filling in forms, it is about identifying issues and considering them

Dan: I also agree with SM that ths s s needs to be easy to fill out or people will ignore it.

Dan: What do people think?

[discussion about time boxing this issue]

Dan: Can we get to consensus on how to move forward. The TAG consensus is that YES/NO questions are better.

Hadley: That means we are deciding this is about getting people to start thinking about these issues -- instead of surfacing a lot of information for us to use in our TAG review. Yes?

Alex: Good to catalogue these things for ourselves. We can point people to these

Dan: Good ideas: Splitting out intro to explainer. Making the questions as simple as possible to read (expand for more details), reluctance to move away from a yes/no model. Asking our users (spec authors) what they think is most useful.

Dan: Let's go to the friendly voices who has been positive over the questionare - as well as other chairs etc.

Lukasz: We can wait until doc is finished:

Dan: No, it is time to ask now and get feedback and share out thinkings. just getting informal feedback.

Lukasz: Yes, let's reach out and ask. I need to repeat that I am very sceptical in splitting up the doc - no one will read the explainer.

Hadley : We can speculate a lot and that is not useful

Lukasz: I'm concerned users feel this is just boilerplate.  Rather than inspire thinking - that they just finish this excercise.

Hadley: We can ask them about that.

--


### Design Review Effectiveness

Sangwhan: We dont have a list of what we should review. A lot could be extracted from design guidelines. but it is written in a way that is not so easy to do

Travis: So meta - are we above the review process

Dan: Yes :::;-) 

Peter: Who reviews the reviewers

SM: I am happy to do the work - it is like a list.

Alex: I like this plan - I am a fan.

Dan: So shall we, we have ... we have 82 open issues! We could go through these all and just check their status - ie pending external feedback, might not have milestores tones associated -- timeboxed 5 min at the time

Travis: I would like to do them in groups - like pending external feedback etc.


Dan: 16 pending ex feedback... let's do that.

[starting now]

#### [#62 Clear site data](https://github.com/w3ctag/design-reviews/issues/62)

Alex: Issues raised at TPAC in SW WG. Let's see. There is an explainer

Dan: Not our issue to close. Writing that in issue.

Alex: IOne issue by Andrew still not closed.

Dan: Alex can I assign this to you.

Alex: Yes, please

#### [#76 "With Credentials" flag possibly inconsistent with web architecture](https://github.com/w3ctag/design-reviews/issues/76)

Yves: Surfacing another error and having something different than a network error, ?? AnneVK noted that surfacing a different event for when ACAO: * is used with credentials is dangerous, but this is exactly what we are looking to do. 

Hadley: Got a rant about this from Tim at MozFest as it is getting in his way, with regard to Solid.

Alex: You believe Anne will trust Mike West more than the TAG saying what way to go.

Yves: That is basically waht Mike said in our last call.

Alex: If we can page hand confirm what he said in the meeting, that would be a good next step.

Travis: Maybe a real time chat between Anne and Mike would be helpful.

Yves: We did that (??)

### 11am RTC ICE Transport with Martin Thompson

Dan: Hi Martin, thanks you for joining us

Martin: The API changed a lot since that I commented on the issue.

Dan: You are the one coming in at an odd time, let's minimize the inconvenience and let you drive this conversation.

Martin: Peter brough the discussion down to a few comments. Your issue #296  https://github.com/w3ctag/design-reviews/issues/296#issuecomment-427528486

Martin: Problem was unidirectional streams - I disagree on the first part. Let's have a look at that.

[martin explaining how it works]

We use this to upgrade and not having that facility for this API limits its use. 

I have already fixed the 4th point. I haven't reviewed this in details and I am not that familiar with streams. but I believe there is something stream related here.

David: they are now moving to integrate with WHATWG streams

Alex: It is unclear how much focus that has, but I am hopeful.

Martin: What do we believe the role of QUIC is. It is just a replacement for TCP/IP for the channel stuff.

It occurs to me that because QUIC is an entirely new protocol, there is potentially a role for this in the infidelities we suffer from in UDP etc to go away. Hard to expose TCP etc because of its usage - thus security.

Alex: What does QUIC add to address these abilities. Like to know what is internal vs external host.

Martin: I don't think there is anything inherently in quic that solves this, except that it is a green field - thus no expectations that you get these kinds of protections.

There is a middle ground thre that we can build something simple into QUIC, like I am willing to talk to eg. other browsers. Maybe as part of the handshake. Like I understand as a server that if someone wants to talk to me, I can do that.

Alex: So the argument here is that since QUIC will come with an implicit contract we don't need to worry about ?? ..

Martin: You will have a clear signal during the handshake ... Hey I am a browser, yeah,I recognize that.

Alex: We have strong interest in not having to deal with CORS - it is a very flimsy point of defence - too easy to get wrong. If this pans out this will be HU-U-U-GE

Martin: Yes, we have ideas that get rid of all this mess.

Martin: Ambient auth will not exist when speaking QUIC

David: So speaking QUIC means not sending cookies?

Martin: I wouldn't say that.. .. no. .. but http over QUIC would do all the http things they do currently and we would have to live with all the legacy built into QUIC.

Yves, You want to get rid of Web Sockets that way

Martin: I always wanted that it is an abomination 

Alex: The idea is that the security model gets reset. If you start in a world as a top level document, then for most cases CORS goes away, only participating content will participate. Content build for the old world will have to learn how to live in the new world. A lot of things go away and we have to rebuild all that.

David: that is not what I heard Martin say.

Martin: Yes, I wouldn't go that far. We need to think of the transport as a capability we will expose to the platform in some cases.

Martin: HTTP over QUIC is DIFFERENT.

Dan: What contents get to open up these new super QUIC sockets?

Martin: No permission is my default position

Alex: Whether you gotta need it, still add in permissions prompts so that we can fix it later if we actually do need it.

Martin: I was talking about how the different end points would identify themselves and then we have the the potential to put client certs into the mix and then we have the very different model used in Web RTC now a system that sits on top of the P2P connection (normal RTC flow)

... WebRTC's DTLS is not PKI - use as glorified containers... 

Yves: so the central ser ver become the one responsible for 

Martin: then we come to the next problem that we dont have a strong auth 

Hadley: will the upcoming strong authentication and identity workshop help with that

Martin: No comment - a coworker will join, with different focus - anything is possible.

Dan: Are you completely throwing web rtc under the bus?

Martin: Great question... haven't worked that out yet.

Martin: One view of  this, we have an API contract that says that you can exchange data between two peers, but not how. What we have now is very complicated and have no other use within the browser.

Seamlessly replacing with QUIC might be nice... but doesn;;'t do exactly all the same... a bit less and a bit more. Would be nice.

David: Does that tie back to the ALPN (app layer protocol negotiation https://tools.ietf.org/html/rfc7301.) comment before?

Martin: No.

Dan: How can we be useful?

Martin: There is one more thing? connection management. One of the things we have done with HTTP2 and QUIC - made it a lot simpler - fold different connections - lots of new features coming up making that better for perf and privacy.

But if we expose that as API we cannot do all these things.

Hadly: when is that useful?

Martin: for CDNs, often images and javascript etc going to the same IP, so better to do over the same connection.

Dan: But you might want to disallow that ewith two tabs one in incognito mode... web app sec wants more formalized def around private browsing mode - we want to preserve all that even with all this new feats at the network layer.

Martin: Once the browser has this view and can see that tab A and B are from the same origin and needs to be isolated, having all that done by the browser has advantages.

Alex: header or flag - all storage isolated from the main container... e.g. banks... shiuldn't have ambient authority shared with toehrs....

Martin: that paralyzes in to the discussions about feature policies.

Travis: catching up - if I am server and there is a quic transport API that allows me to type in any IP address and port what do I need to do to secure the gateway into my network? how do I stay safe?

Martin: How do you auth normally, ie say you are using cookies... you are operating this server and you receive a new connection and a request comes in, how do you determine that it is good or not with with a new API or not..,

Travis: I have to roll my own, you say?

Martin: It is built in. HTTP would use the mechs from HTTP.

Travis: but I am not a smart server guy, so my server might be vunerable.

Martin: yes, ... during the handshake you would say that I am a browser and it will ack that or fail..

Travis: The case of web sockets is that you need to  .... now we can just use a signal during handshake.

David: So the browser HTTP stack doesnt need to say it is a browser?

Martin: No

SM: This field you mentioned is it binary..

Martin: That would be whatever the contract would be. (something simple not totally defined yet)

David: What does RTC QUIC transport spec say about anything of this new negotiation that would expose les sor more stuff

Martin:  Nothing. They have taken the web rtc stack and broken it down into a number of new small components one of the lowest level components is the ICE components. All I want to do, with this quic thing is to put it on top and reuse 

David: The current RTCQuicTransport is only on top of RTCIceTransport and not generic QUIC?

Martin: yes

Travis: we've been talking about having a generic low-level quic transport API... replacing data channels with something similar based on quic

Travis: Have you gotten your thoughts written down in some docs about this QUIC API.

Martin: No, not apart from comments in issue.

Travis: Seems cool, would have to have it written down.

Martin The push back you get is that people want to finish speccing QUIC... reluctant to work on new things

Dan: Do you understand it from the other side, why WebRTC are reluctant in engaging. I dont know if I can see a QUIC'er way forward :)

Dan: Would it be OK if they did something simpler in the interem, and then replace later / refactor.

Martin: Depends on whether the user-visible parts of QUIC are stable enough.

SaSM: RTC seems this more like an experiment for now and see how it can be adopted

Martin: Hard to know what is going on - we want to be consistent with the design condsiderations

SM: Can we strongly push for this to be behind a flag/origin trial until later? I can leave a comment

Travis: Seems we got fetch, web sockets, XHR we got a lot of baggage... this will just be the 5th standard for doing sommcomm

Martin: We dont want to create a new CORS that is what I am most concerned about. Maybe seperaring only ICE out might be good... but needs due diligence 

Travis: You mean the Web RTC proposal?

Martin: Right - maybe we avoid any risk of this leaking out if we always use ??

Dan: Does it makes sense to orchestrate more talks between stakeholders ?

SM: Yes

Martin: This wont allow us to get rid of legacy in the short term

SM: Most people just care about the perf benefit

Martin: Connection setup is much better - 1 roundtrip vs 4.  SCTP+DTLS does a few things better, mostly around partial reliability.  QUIC doesn't have unreliable communication mechanisms -- fully reliable.


MArtin: the end goal for web rtc is to have the one quic tunnel talking to the peers all unin the same channel, data, video, ec...c...tc... in one congestion control context, with right prioritization.

Dan: Searching for actions from us.

Martin: Give us another 4-5 months to get QUIC ready.

Dan: Does the WG know this opinion?

David: is the stuff you said about adding a bit into the QUIC handshake, something you would bring up into that forum

Martin: Yes, we have people cramming to get this thing deployed. Some fear that if it doesnt happen in 2 mntonths it wil never happen

Yves: who are the implemented who will be providing implementations

Martin: All major browsers, FB,  have deployed early version, Google is still in the process of taking the proprietary stuff they have to make it work, MS has all there stuff on track... every single major CDN is encolves with multiple implementations... around 15-17 implementations

[Thanks Martin]

SM: How do we talk to you? 

Martin: Send email...

Dan joking: We only use Web RTC



# **food**

## Design reviews that were marked pending external feedback

### TTML 2

https://github.com/w3ctag/design-reviews/issues/138

?: Where are we?
Peter: CSS and TTML are talking and getting along now.

looking at [style attribute derivation](https://w3c.github.io/ttml2/#style-attribute-derivation)


### string-meta

https://github.com/w3ctag/design-reviews/issues/178

pending external feedback

### WebVR

https://github.com/w3ctag/design-reviews/issues/185

### ResizeObserver

https://github.com/w3ctag/design-reviews/issues/187

Peter: I had a brief conversation at TPAC about not ignoring fragmentation.

Peter: I think we're awaiting another draft here.

Travis: Proposing to close this and hope for a new review of the later additions, but shouldn't wait around with this issue.

### IntersectionObserver

https://github.com/w3ctag/design-reviews/issues/197

Peter: Alex was going to discuss some open issues.

Peter: waiting for feedback, push later

David: There was one set of complicated issues I needed to look into -- may not be interoperable today.

### Gesture Delegation

https://github.com/w3ctag/design-reviews/issues/199

SM: Is this superceded by user activation spec? Adding comment

Peter: If response ins superseded, then just close the issue

### ads.txt

https://github.com/w3ctag/design-reviews/issues/201

Alex: This may have been dropped after update of concerns in February.  I'll ping that PM.

Alex: Let me find some text to put here.

Alex will update issue.

### Sensor APIs

https://github.com/w3ctag/design-reviews/issues/207

Sangwhan: I'll try to get this done by end of Face-to-Face.  I eed to check through proposed changes.

### link rel=modulepreload

https://github.com/w3ctag/design-reviews/issues/213

Travis: new idea from Domenic for named package maps.

Kenneth: You don't need to preload them, though.  Can defer.  Could get a huge map pretty quickly, where not all of them need to be fetched.  Maybe we should ask how they relate to each other.

Travis: I can comment...

Dan: So still pending external feedback?

Alex: ... input to toolchain ...

### WebRTC secure context?

https://github.com/w3ctag/design-reviews/issues/228

Alex: getUserMedia should be SecureContext.  That's camera, mic, other input.

Sangwhan: Were supposed to discuss at TPAC 2018, not sure if they discussed.

Dan: What's the status of the doc that defines secure contexts?  Is that doc stable?

David: Seems like it's being baked into the web.

Hadley: Why is it only CR?

Dan: We should make sure this stuff is tied up.

Dan: Should we ask Mike to ask us to do a review of this document?

Alex: What's left to do?  Can we adjudicate without pulling in Mike?

Dan: I want us to push it along.

Alex: So can we just ask the question?

Hadley: File an issue on their repo.

Dan: I can do that.

https://github.com/w3c/webappsec-secure-contexts/issues/62

_(scribe missed a little, the reason was not food)_

Dan: ... back to WebRTC and #228... can we close it?

David: There are a bunch of issues... but I don't see one about RTCPeerConnection.

Alex: Someone should open an issue.

Dan: OK, so pending feedback on that issue.

### Vehicle Information Service Specification

https://github.com/w3ctag/design-reviews/issues/234

Hadley: This should have been suprseded by Yves visiting them at TPAC last week.

Yves: v1 is what they're shipping right now.  I think we already gave feedback.

(group reads https://github.com/w3c/automotive/blob/gh-pages/services-explainer.md)

Hadley: spec still in CR; maybe ping to ask where in process?

Alex: how possible to model this as generic sensors?

Hadley: They looked and rejected - not sure why.

Yves: Current state is not really webby, but it's what is implemented right now.  We were dealing more about the future version -- wanted to figure out how to make it better.  We already made our concerns.  I asked them to share early design.

Alex: What would be most helpful for them?  Anything current?  Or still figureing out what next version should look like.

Yves: still in early design phase

### HTML Styling

https://github.com/w3ctag/design-reviews/issues/246

Dan: Added pending external feedback, regarding async and defer for style.

Dan: pending external feedback seems in error.  Will deal with in main triage.

### Web Sockets

https://github.com/w3ctag/design-reviews/issues/268

Travis: I think that was all the feedback.

Travis will file issues for all the feedback and then close the issue

TrvaTravis will add a comment with the plan.

### ISOBMFF

https://github.com/w3ctag/design-reviews/issues/285

Sangwhan: Reviewed the packaging aspect, still need to review advance time signalling aspects; thta's a separate spec.

Dan: dsinger wanted a workshop on things related to this.

Sangwhan: I'll come up with a review before next f2f.

(coffee break)

## Design reviews

Dan and Alex discuss logistics about how to triage and break out on issues.

(subgroups break off)


### MathML

Travis: We believe web components is a way to incubate what the next better model for math on the web should be.



### Design Guidelines
### Design Reviews


---












