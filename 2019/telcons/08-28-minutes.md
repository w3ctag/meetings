## TAG Teleconference
##### 28 August 2019

Present: Kenneth, Tess, Peter, Lukasz, Dan, David, Hadley

Regrets: Alice, Sangwhan

Scribe: Kenneth

---

Agenda:

* Tokyo Logistics / Discussion of Meeting Format for Tokyo

Dan: Talks about 1:1 breakouts - do people want to do that again?

Kenneth + Tess: Yes, it was great

David: I also liked it, but I am fine with 3 people as well.

Dan: Yes small sized breakouts worked out well but it requires a bit of prework and I need to find out when to do that and wanted to hear Alice if we have access to the venue on Monday. Iceland felt productive as we didnd't do all that work during the meetings.

Dan: Feel free to join at the hotel and help me out.

* [Review request: DOM Standard Review Draft](https://github.com/w3ctag/design-reviews/issues/404) - @hober

Tess: As a result of the the W3C/WHATWG memorandum we will review drafts from the WHATWG group - so this is such a request.

Tess: Plenty of changes, we ew already have our existing review tasks of HTML and we can treat this as one of them.

Tess: This hope is that going forward - on a yearly basis - this won't be much of a task (saying with my WHATWG hat on)

Tess: (hat off)

Dan: Does it makes sense for the TAG to concentrate on particular changes.

Tess: As we will do every year, this will be easier next year and forward

Dan: we need to make sure it doesn't take a year :-)

Tess: We are kind of trying to find out how to do this. Would help with a list of major changes recently

Ken: I think there have been changes in the area of Web components - like form participation

Tess: We can ask the WHATWG to help us so that we can prioritize etc

David: Makes sense to review in units of feature instead of specification

Hadley: How do we trunk up something massive, like HTML

Dan: Ye	s this would really help us, adding that as feedback.

Dan: Do we want to add this to the agenda of the F2F? Let's do it

Dan: Who are we giving the feedback to? Are the WHATWG interested in receiving, or mostlyh partly of a W3C boiletplate process. That informs the amount of effort we put into this.

Hadley: Looking at the review draft, no introduction that explains what the DOM is, and I don't see a DOM explainer :-) What is the user need etc - depending on how we get this, we might respond in different ways

Tess: I hope we would generate the feedback that the WHATWG editors would be interested in - the WHATWG published review drafts every 6 months and we don't envision these docs changing much. We can mark as at-risk potentially.

Tess: Feedback that there is no explainer/introduction explaining what it is - is actually good feedback long term. But I dont expect that for this process that that would be added to the review draft

Hadley: how does the whatwg deal with at-risk features?

Tess: WHATWG doesn't have the notion of at-risk but the W3C does. There are annotation in specs about like feature implemnetation (from MDN etc) so this could be an additional annotation like that. Like at-risk/non-normative from W3C side of things

Tess: Worth saying that the tooling doesn't exis. So we haven't solved problems like: Do we want to be granular with at-risk or can be mark a whole section at risk?

Hadley: Got it. thanks

Dan: we come back to is at the F2F


* [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @alice, @torgo

Dan: Skip for today as Alice is not on the call - bumping it


* [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394) - @kenchris

Ken: Looks like a really early review.  My suggestion is to do this together with ...transforms.

Dan: I've been hearing people using web sockets where webRTC is too heavyweight. Relevant here?

Kenneth: This is a temporary improvement of websockets, with backpressure.

Dan: Next step? 

Kenneth: let's talk at face to face. We have feedback from Martin Thomson: suggesting we discuss with webtransport. So maybe wait for a reply on that?

David: Let's cluster those in a f2f breakout

* [Layout Instability Metric](https://github.com/w3ctag/design-reviews/issues/393) - @alice, @dbaron, @lknik

Lukasz: we should wait for the replies - we opened issues in their repo.

David: There are also Florian's comments, but I didn't feel obligated to file Florian's issues


* [Native File System API](https://github.com/w3ctag/design-reviews/issues/390) - @cynthia, @kenchris, @lknik

Lukasz: It appears that they do not want to restrict the access to specific files/folders. Big flashing warning in red?

Kenneth: I believe they didn't want to spec that, but browsers should be able to restrict access

Dan: Looks like their issue 74 on this is still an open issue. on the other hand, that is going to vary by architecture to architecture. So it can't be normatively... 

Kenneth: like a phone OS has a very different file system to  say a desktop (Windows or Chrome OS) 

Dan: yes, or a television. Well, they're all unix.... 

lukasz: sooner or later, this will get abused. Don't know precisely how or what intent. This is powerful so will be useful.

kenneth: not that different from uploading a file etc. will be more interesting in serialising those file handles

lukasz: assuming permissions to permission/access a file are kept

kenneth: yeah, they're thinking that for installed web apps. But they're not to that in the spec yet. 

lukasz: so for that, would be useful to understand the use of the web/PWAs in like 5 years or something

David: also worth saying that chromium-based browsers are the only ones showing interest in implementing this.

Dan: Let's put this into the face to face

lukasz: why are only chromium-based browsers the only one interested?

david: I think other implementations have concerns about the security model.

tess: I agree

Dan: I think we should highlight the lack of implemeneter interest, makinging it difficult to think about.

kenneth: I think i'd like a list of ... some of these features are already available.

lukasz: we should pu that in the issue tracker

kenneth: what feedback would we expect? "currently this is only happenning in chrome." Then what?

...they're syaing they want to roll this out in pieces, and it would be good to see more on that.

lukasz: I saw that in a document somewhere, yes.

dan: I want to mention with Lukasz's comment on "the drive-by web will only have enough state...." what do we mean?

Tess/Kenneth: the web

Dan: this is another example of inventing terminology, but it confuses the issue

lukasz: "drive by" has very strong Grand Theft Auto connotations

Dan: I've moved it to the face to face, and Kenneth you've put your comments in; let's come back to it then


* [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392) - @hober, @alice, @dbaron

Tess: I dont know if anything happened since we last looked at this - was on vacation

David: a breakout did not occur

Dan: Move to F2F? or any burning need?

Hadley: There have been replies, was the breakout to discuss the replies?

Dan: David can you schedule a breakout?

David: I can try yes

* [WebTransport](https://github.com/w3ctag/design-reviews/issues/389) - @cynthia, @dbaron, @ylafon

Dan: Postpone? David you added alot of comments, but a while back - there is an open issue on WebSocketStreams.

David: I had wanted to do a breakout after Yves is back from vacation.

Dan: bumping it, also considering that Sangwhan is not here.

* [A toast UI element](https://github.com/w3ctag/design-reviews/issues/385) - @hober, @alice, @kenchris

Dan: I expect that Alice has a lot of new info, but he is not here today.

David: I actually wanted to schedule a breakout on this one

Dan: Let's bump it!

* [Import maps](https://github.com/w3ctag/design-reviews/issues/340) - @cynthia, @kenchris

Dan: Bump

* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron

Dan: any comments? 

David: I believe we did a breakout. July 19th - long ago so I don't recall the details.

David: They split it out into two reviews, but I need to have a look at it.

Dan: Would be good if we could close it... but looks like we need to wait until Alice is back. Tess do you have any feedback

Tess: I may have had but also don't remember :-) Need to look for the notes in the slack channel

David: some unfortunate things in the draft, not clear if anything can be done about them though

Dan: This is a tought one, don't want to leave dangling like a zombie - let's consider closing it on the next call.

[Talking about hotels in Tokyo]

---



