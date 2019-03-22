## TAG Teleconference
##### 19 March 2019

Present: Dan, Peter, Sangwhan, David, Tess, Alice, Yves

Regrets: Kenneth, Lukasz

---

Agenda:

* [IETF Liaison](https://datatracker.ietf.org/liaison/1614/) - @ylafon
* [Audiobooks](https://github.com/w3ctag/design-reviews/issues/345) - @dbaron
* [Web Publications review](https://github.com/w3ctag/design-reviews/issues/344) - @dbaron, @torgo, @hadleybeeman
* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @dbaron, @torgo
* [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @alice, @kenchris, @lknik
* [User Activation Delegation through postMessages](https://github.com/w3ctag/design-reviews/issues/347) - @alice
* [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice, @dbaron
* [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241) - @dbaron, @ylafon, @hadleybeeman, @lknik
* [Serialization of natural language in data formats such as JSON [I18N]](https://github.com/w3ctag/design-reviews/issues/178) - @cynthia, @dbaron


---

## [Audiobooks](https://github.com/w3ctag/design-reviews/issues/345) - @dbaron

hober: like that it's simple

hober: wanted more from explainer; seems to be missing relevant technology such as podcasts. 

hober: audiobooks get very long & large, using a zip file seems maybe suboptimal, the audio is already compressed..?

hober: I assume they have thought of all these things, but I don't see documentation in the explainer of why they were not used

dbaron: did you see the use cases doc for web publications? It seems relevant

hober: I was reminder of torgo's doc on ethical technology principles - having a living document on priority of contituencies. This seems like a case of don't reinvent the wheel - the explainer should make a case as to why this isn't doing that.

cynthia: Right, none of the considered alternatives explain why those were decided against

hober: agreed; it's missing both obvious alternatives and rationales

dbaron: not sure what ePub had for audiobooks in the past.

torgo: do we want them to think about web packaging? We've talked to the ePub people about that before. There's some kind of workshop coming up on this. Is there an obvious, more "webby" approach not listed in the considered alternative that we could encourage them to use?

dbaron: seems possible. I made some notes on the web publications review - audiobooks is the first "sub-spec" of web publications. A bunch of the issues here are related to packaging and how packaging relates to origins and URLs, there were some interesting things in the requirements doc but I haven't gotten to look at how they address those in the spec yet.

torgo: Should we provide this feedback and then bump this two weeks?

hober: Sure, I can try and capture my thoughts on the issue.

dbaron: I won't be here then

torgo: Let's do one week then.

## [IETF Liaison](https://datatracker.ietf.org/liaison/1614/) - @ylafon

yves: Don't have anything yet.

torgo: I found this very hard to decode. There seems to be something brewing where webRTC group is doing something ietf doesn't like...?

yves: I don't have any more information than that.

torgo: Should we invite Mark to come in and give us an update?

dbaron: This may be a game of telegram. 

torgo: yves, can you talk to Wendy about it?

yves: that's my plan.

torgo: Do we have an issue for this?

yves: that doesn't seem necessary.

torgo: I'm going to put it on the agenda for next week; if Wendy can join the call then, that would be helpful. If she tells us we don't need to get involved, I'm happy to take that advice.

## [Web Publications review](https://github.com/w3ctag/design-reviews/issues/344) - @dbaron, @torgo, @hadleybeeman

torgo: Should we bump this one to next week as well?

dbaron: I did a quick review, added a comment in the issue. So far I've read the requirements and explainer, not the spec. Interested in how the spec deals with issue around URLs and origins and packaging. Another week seems good.

torgo: I will also try and read the spec before the next call.

## [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @dbaron, @torgo

dbaron: I think the implications are pretty interesting. I've forgotten more than I knew about it, somehow. 

dbaron: there are various browsers that treat more than an origin as "lumped together" - this would gives sites some control over that grouping.

hober: I have a concern. Say I'm a nefarious actor, and I go to companies and say "please put this thing on your web server that says I'm part of your first party set". Seems like a way to subvert the understanding of the first party/third party distinction.

dbaron: Mike has some mitigations for this. For example, you can ask one party to do this, but if you ask two they have to put each other in their first party sets *and*  they have to do it in a synchronised way. 

hober: That's probably good enough? Though I'm hesitant to ever say "good enough" in relation to security. I can ask colleagues for feedback. Google homepage has like 100 different domains, this is a difficult problem to solve without everyone having to maintain whitelists.

torgo: Good idea to ask for feedback; please ask your colleagues to weigh in on the issue directly. How about we bump this a few weeks... I'm going to put it on 4/2, we can come back and see if we have any substantive feedback. Do any other implementers have any feedback on this? Microsoft? 

hober: I assume Mike and John (Wilander) are already talking about this, I don't think I have a lot to add...

## [User Idle Detection](https://github.com/w3ctag/design-reviews/issues/336) - @cynthia, @alice, @kenchris, @lknik

alice: I took myself off because it seemed like there were enough people on it.  Was a good discussion on there already.

sangwhan: My main concern has been addressed... Ken added a bunch of feedback, I haven't read that yet.

*sounds of reading*
  
sangwhan: This is about events vs. observers. That hasn't been resolved yet. This is still waiting on external feedback.

torgo: Should we bump this a week or two to wait for feedback? Ken may also not be able to make next week's call, so let's bump two weeks.

## [User Activation Delegation through postMessages](https://github.com/w3ctag/design-reviews/issues/347) - @alice

alice: This came in 25 days ago, not quite my area but seem reasonable. Useful when you want to know if the user has interacted, let's you transfer to the frame.

tess: Worried about the browser limiting some activity in iframes/subframes to a user gesture and this is a way for the main frame to hand off that user gesture. This makes sense going upward, but not downward. Media policies are different in different browsers; would this allow arbitrary hand-off of user gesture state? You have an iframe that has a video in it, user taps to make a comment and that causes the iframe to start playing a video.

alice: Wouldn't the video stop when the user interacted with the top frame again?

hober: I think that would depend on the browser's policy.

torgo: There are some security considerations in the design doc; not very privacy focused. Does seem that there's a missing privacy consideration... any time you're dealing with activation you're dealing with something that is personal to the user. That feels dangerous when it comes to privacy... doesn't seem that there's enough in this doc that deals with this issue. This is a little vague..

dbaron: I'm concerned that there are things that set the user activation state; often you'll get more than one of those in rapid succession. If you have the ability to transfer that to another frame, you can take what's conceptually one user action and "spread" it around, e.g. mousedown transfers state and then mouseup keeps the state locally.

hober: or you run into an issue where the transfer recipient loses user activation.

torgo: Let's try and solidify our feedback and come back to this next week.

## [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330) - @hober, @alice, @dbaron

everyone: We haven't managed to look at this.

hober, alice: We'll ask around among our colleagues and cycle back to this next week.

## [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241) - @dbaron, @ylafon, @hadleybeeman, @lknik

dbaron: This was another case of being over-optimistic.

torgo: Haven't heard back since November; has this been dropped?

dbaron: One of the other primary contacts may know.

torgo: Going to bump to the 26th and bug the WICG chairs and other contacts.

## [Serialization of natural language in data formats such as JSON [I18N]](https://github.com/w3ctag/design-reviews/issues/178) - @cynthia, @dbaron

torgo: Can we close this one?

sangwhan: Yes, actually!

sangwhan: I don't know that I have anything to add here, I think they're doing some work on it...

torgo: We have precedent for closing issues when there's ongoing work but no open questions as such. Let's close this off.

sangwhan: I volunteer.

## AOB

torgo: I will be at the AC meeting in two weeks, as will David. We'll probably talk about the usual stuff that we talk about.

torgo: I'm hoping to informally talk to people about the ethical web thing. I posted a blog post recently which refined some of the things we talked about in Tokyo. I'm hoping to talk to more people in the W3C community about this. Jeff asked us to come and join part of the AB meeting that'll happen on the 10th; David will also be there, we'll talk about this there as well.

torgo: The AB also wanted to hear from us about the new web features coming - well, more trends and issues, things like the securing the web activity. If anyone else wants me to carry a message ... will anyone else be there?

hober: Unlikely.

dbaron: May also be a discussion of the role of the director.

torgo: I'm not going to attempt to be the voice of the TAG on those issues; if people have questions for us I can bring them back for us to discuss.


