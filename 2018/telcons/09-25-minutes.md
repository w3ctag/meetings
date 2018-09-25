## TAG Teleconference
##### 25 September 2018

Present: Dan, Kenneth, Peter, David, Travis, Hadley, Alex

Regrets: Sangwhan, Yves, Lukasz

Chair: Dan

Scribe: Kenneth

Agenda: https://github.com/w3ctag/meetings/blob/gh-pages/2018/telcons/09-25-agenda.md

---



## Agenda:

### [Canvas TextMetrics](https://github.com/w3ctag/design-reviews/issues/302) - @dbaron  

David: Minor things... APIs not designed very well for vertical texts.  It's a feature in the HTML spec... nothing that's too big a deal here.

Dan: what is your recommendation?

David: lets see a respomse and make sure these things gets filed on HTML and see if there is a reaction there. Then we can probably close this issue.

David: Any one else has an opinion?

Dan: Let's not close before another TAG member has reviewed David's feedback

Peter: I agree with David and looking at it now. Seems that a few things are missing like x cap height etc. My main concern is that work happened in Houdini which then stopped because this was more complicated than expected. I would like to make sure that we have the right expertice in the room .

Dan: I feel that we need to get feedback from them before we close this off. Can you do that Peter, write into the comment?

Peter: Sure

Dan: Bump this a week and see if we get good feedback

Travis: We need to notify Fernando

### [User Activation v2](https://github.com/w3ctag/design-reviews/issues/295) - @dbaron @hadleybeeman 

Hadley: awaiting external feedback.

David: I didnt get too far into 295. This is about trying to standardize user activation behavior which is different to what browser do today, but more close to what Edge does today. the one thing I was wondering is whether this is being used for more security/privacy minded things in contract to what it was designed for (annoyance prevention).

It seems pretty resonable to trying to standardize these, but if it touches security/privacy then we need to be more careful.

Alex: Chrome has two other use cases, muting media playback and unpausing iframes

David: None of these seems worrying from a privacy perspective

Alex: Let me look though the rest of our usages - we used it a lot

David: three groups of activations: ...

Dan: What do we think in terms of what we are being asked for? What should out response be

David: I am not perticularly concerned about anything here beyond the one question that I asked

Hadley: This is outside my area of expertise - I am converted that they spec author doesn't like creating a proper explainer. Spec author liked Web IDL better than plain English explainer -we are not convinced though.

I am concerned not just for us, for for anyone working with it - explainers are a useful part of the process

Alex: One of the use cases in blink is supressing permission requests in a lot of (i)frames the users hasnt used - annoyance mitigation

David: I understand why they want to do this is to simplify their code and improve interoperability and not necessarily a end user goal.

Hadley: Might be hard to artigulate

David: they could just say that

Dan: An explainer should start by  "User should do that, developer should do this.." not "blah blah implementation details" - I think it is not high level enought 

Dan: You should explain in plain language, what problem to solve, and use cases..

Hadley: I am missing the why, we are speculating about it as a group - not a good use of our time

Dan: Can someone sit down with Dave and help them write a few extra paragraphs

Alex: Sure I will handle this

Hadley: Everyone is busy and this is more cognitive load than necessary for us :)

Dan: Shall I bump this one, yeah, I should do that... done

### [User Activation API](https://github.com/w3ctag/design-reviews/issues/300) - @dbaron @hadleybeeman  

Dan: What about 300?

Hadley: awaiting external feedback.

DanThis is where Dave said that Web IDL is better than plain English

Alex: [laughting]

David: This is about an API that exposes the activation state.

Kenneth: Are the use-cases clear here

David: There were some use-cases that were a little interesting, but ... like I think that some of it was around iframes that wanted to post message each others, and condition an message from another iframe depending on user activation or not

Alex: Same thing with resizing iframes.

Hadley: I like that use-case

Dan: Should this not be highlighted in the security considerations. Again I think we need a little more infomation here.

Alex: We asked for sample code and didnt' get it - lets follow up with Dave again on that

Dan: What problems are we trying to solve

Alex: We would like to check the states ourselves in a layered approach, which this seems aligned with. Questions is whether this is motivated well, which I think it is

Dan: That is not really reflected in the explainer well. There are too many assumptions, but the point of the explainer is to do the opposite 

Dan: Bumped as well. Will he be at TPAC

Alex: I will check


### [DOM](https://github.com/w3ctag/design-reviews/issues/229)- @cynthia @dbaron @travisleithead  

Travis: The goal is to get this closed out today, we spend some time on this last week... thumbs up to our co-chair. I dropped in a polished comment into the issue. There we not a lot of significant feedback, mostly nits.

Lots of historical things are specced in the dom and new things, all mixed together. Would be nice to make it more clear what is old and new. No explainer like text. It sure would have been nice with a bit of intros. Sangwhan was confused about about a few things like Processing Instructions and you wont find out by reading the DOM spec.

Some questions about composed events  - what is it and why is it useful

References to mailing lists that might have gone

General feedback about abort controller vs TC39 proposal - is that over?

Alex: They chose not to do anything with Cancellable Promises but they didnt seem to care around that time, so people went ahead.

Alex: I think that there is still going to be work in TC39 around cancellable promises

Alex: Is cancellable an advice or an actual cancellation. TC39 is constrained in what they can do now due to fetch cancellation and they will probably have to come to us for advice on what to do.

Travis: We wondered whether mutation events should be written down and spec'ed. Wording around TreeWalker. Is anyone using that

Kenneth: Yes, lit-html for instance: https://github.com/Polymer/lit-html/blob/14f7e67b1a325946030aff031d4518c4a9e54ff2/src/lib/template.ts#L53

Travis: It is interesting, I just wondered whether its time had come and gone

Dan: Shall we close this off?

Travis: I think that is fine... take it or leave it feedback

Dan: Close it off! Great!

### [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @dbaron @slightlyoff

Alex: I have not discussed with Zager

Dan: Shall I bump this in that case?

Dan: It is sooo bumped! OK!


### [WebVR](https://github.com/w3ctag/design-reviews/issues/185) and other orphaned issues

Dan: In going though existing issues I noticed that a lot needs to be cleaned up. Because of the launch of the Immersive Web group, I was looking at our review of Web VR and I noticed that it was set to a milestone of May 29th and it is still open! So I didnt have the time to see if there are otehrs like this - but there probably are. Maybe worthwhile doing this the next couple of minutes... like can be close this one out?

Dan: Is there anyting left on this issue or can we close it?

Travis: Looking over the comments. Discussion around commit model, Web VR in worker.

Alex: This is what we discussed a lot - having both commit (pump data) and rAF (async model) is weird, very different models.

Hadley: Gamepad API, did we understand the differnence between the specs?

Ale: x: People hoped for Gampad to be the answer, but didn't turn out the way, added more and more info like pose, etc so added that directly to Web XR

Hadley: Makes sense. I posrpose that we keep this in our backlog

Alex: Should we talk to them at TPAC?

Dan: I think that is a good idea if we can get closure around raf and gampad

Hadley: I would like to talk at TPAC

Dan: I will attend part of their meeting at TPAC

Dan: I will assign to TPAC -then we can hopefully close it up.

















