## TAG Teleconference
##### 24 April 2018

Present: Hadley, Dan, Lukasz, David, Yves, Sangwhan, Kenneth, Travis, Alex

Regrets: Peter

---

Agenda:

* [CSS Selectors 4, :focus-visible.](https://github.com/w3ctag/design-reviews/issues/233) - David, Travis, Peter
* [CSS ::part and ::theme pseudo elements](https://github.com/w3ctag/design-reviews/issues/230) - David
* [Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225) - Lukasz, Dan, David
* [The always lovely HTML General Review](https://github.com/w3ctag/design-reviews/issues/174)
* [Keyboard Map](https://github.com/w3ctag/design-reviews/issues/238) - Travis, Sangwhan
* [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232) - Dan, Yves
* [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224) - Travis, Dan, David
* [Async Clipboard API](https://github.com/w3ctag/design-reviews/issues/222) - Travis, Alex
* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - David
* [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Peter, Travis, Hadley, Alex
* [Offscreen Canvas](https://github.com/w3ctag/design-reviews/issues/141) - Travis, David, Alex, Sangwhan
* [With Credentials](https://github.com/w3ctag/design-reviews/issues/76) - David

Followup:

* [Deprecating nonsecure cookie delivery](https://github.com/w3ctag/design-reviews/issues/239)


---

## Private Mode

Hadley: We need more detail. We need something about threat models in this document and about what privacy mode means in different browsers.

Lukasz: it's difficult to forsee the theat models - different vendors ship different things.... Describing some commonalities..

Hadley: i agree we don't do specifications in the TAG. 

Dan: To clarify: threat model each browser has in their minds when they are implementing private browsing? Which threats each mode each implementation has in mind?

Hadley: Yes. Whether it's the network snooping, someone else using your computer after you, or the site knowing more about your browsing.

Lukasz: There are differences. Brave use TOR tabs in private browsing modes. But I'm not sure a finding is good for discussing this. This is an area of active competition and frequent changes. Findings aren't subject to update, yes?

Dan: I agree that a finding shouldn't list the features of each browser. But I don't think it's bad to mention specific implementations. but it feels more like this could be the start of looking at the commonalities. every one of these implementations does X, Y and Z. Therefore, that might be interesting on its own. and I do think mentioning the network side and that some implementations — not just TOR browser — are bundling VPNs or some TOR-like functions.  That does seem to be useful information. 

Hadley: I agree

Lukasz: I agree too, but these are areas of frequent changes. But I'm not sure if there is a path for an update to Findings documents? There are for specifications. But we are not talking about specifications.

Dan:  I agree that we need to get something out there that might not be a finding, but a document that surveys the current state. We can then start talking about it. 

Hadley: I agree, most of the interest I'm hearing is in the patterns in the ways implementations think about private browsing. Feature interaction does change constantly.

kenneth: What are we hoping for an outcome?

dan: Perhaps to work out what is useful to have in common. We even ask in our security and privacy questionnaire "how shoudl this feature behave in incognito mode?" But there is no spec for that, since every browser is different.

Kenneth: So the point is to evaluate this against a spec?

dan: there is no spec. 

lukasz: My understanding in London was that we aren't sure if this should to a spec. And that we have some scepticism in the TAG. The issue was that we do not have a browser in W3C to explain what it is, so we write a finding to recognise their existance but not write a spec. To achieve this I wrote this draft, with previous findings in mind. 

Hadley: yes, but I am still concerned that the current variety in implementation disadvantages users and developers, most of whom (as far as I'm aware) don't understand the difference between the implementations. I don't have enough data to know if I think some form of standardisation is an answer, or UX improvements in implementations, etc.

Lukasz: So what is our aim? Specification? That's different to a finding.  There is a case for specification, but I'm not sure that vendors would be happy with that.

David: More intersting question: not whether users understand what private browsing is, but whether spec authors know?

Kenneth: I agree. Maybe not a spec, but an explainer or a set of ideas?

Dan: I agree. And what Lukasz said: having a TAG doc talking about private browsing mode is better than nothing. 

Sangwhan: The point that David brings up should be in our design principles document. Do we have an issue to track that? (Now we do: https://github.com/w3ctag/design-principles/issues/97)

Dan: let's add that.

...Let's keep working on this, track it for publication at the face-to-face in Seattle. 

Hadley: Sounds good

Lukasz: I'm happy we agree we need a doc, but we need to figure out whether it should be long or speak of concepts. I think concepts would be better.

dan: If you share what you've written already, and you can write the stated goals of the document. We can comment on and collaborate on what those goals can be? 



## [The always lovely HTML General Review](https://github.com/w3ctag/design-reviews/issues/174)

Travis: I propose we close this issue. I've created issues for each of the section. Action for everyone: Look over issues: 242-274.  Assign yourself to one of these reviews. 

Dan: When you created these issues, have you linked them to specific issues in the HTML repo? Or have you stayed away from which vrsion of HTML we're reviewing?

Travis: I've been specific: these are all sections in the WHATWG document. That's a superset of what's in the W3C document.  I"ve also tried to be specific on what parts of the spec to look at. 

... For example... https://github.com/w3ctag/design-reviews/issues/242

...I'm not sure what milestones to set; each person claiming an issue should put in their own milestones. 

dan: This is a lot of work; amazing that you've done this, Travis. 

...Now we need to triage these and assign them out to people. Once everyone has claimed the ones they want, then we'll allocate the rest next week. 

...Does the HTML community know we're doing this?

Travis: Domenic has commented on this issue. I can reach out to him and Anne. 

Dan: The reason I was asking which version of HTML we're commenting on — AC meeting is coming up. The future of W3C in HTML and DOM will be on the table. the TAG will be asked to weigh in. I think we're doing the riht thing in referencing the WHATWG version, but it's bound to be controversial.

...If you're watching the AC list, the TAG's name is coming up a lot in questions about the future. 

Hadley: I think we should discuss that before the AC meeting.


## [CSS Selectors 4, :focus-visible.](https://github.com/w3ctag/design-reviews/issues/233) - David, Travis, Peter

Travis: I looked at this last week. Added some commentary. Otherwise, this review is done. My comments have been responded to.

David: I agree, as long as that PR they had is merged.  We reviewed the PR... but it's not merged yet.

Alex: Travis wanted to close the issue?

Dan: Yes, but if the PR isn't merged... 

David: I'll check with the editors. 

## [CSS ::part and ::theme pseudo elements](https://github.com/w3ctag/design-reviews/issues/230) - David

David: No comment at this time.

Dan: Will move milestone to next week.

## [Permission Delegation](https://github.com/w3ctag/design-reviews/issues/225) - Lukasz, Dan, David

Dan: We need Lukasz.



## [Keyboard Map](https://github.com/w3ctag/design-reviews/issues/238) - Travis, Sangwhan

Travis: I looked at this, added a few comments. I think our review is done. Sangwhan?

Sangwhan: They haven't fully responded yet; it would be good to hear their views.

Dan: Can we close it and ask them to come back at the next stage? Or do we need to keep it open and ask them to reply?

Sangwhan: I'd like us to get to a point of agreement, and then we can close our issue.

Travis: I agree.

Dan: How are we going to get that feedback?  I'll ping Gary. 

Travis: on their repo, issues 7, 8, 9, 14 and 15 are the ones we're looking at. 

## [BCP56bis](https://github.com/w3ctag/design-reviews/issues/232) - Dan, Yves

Yves: nothing to report. 

## [CSS Layout API](https://github.com/w3ctag/design-reviews/issues/224) - Travis, Dan, David

Travis: I still have an action to file issues on their repo.  

Dan: I'll move the milestone. 

## [Async Clipboard API](https://github.com/w3ctag/design-reviews/issues/222) - Travis, Alex

Travis: I looked at this this AM. We have filed our issues on their repo — same editor as the keyboard map API.  Not sure we've heard back. I commented on a few issues. In Tokyo we discussed — is it enough to gate this clipboard access on a user gesture? We have semantic events in the platform for when the user wants to perform a copy or paste. We can map the gesture to that event. 

Kenneth: If you are online in google docs, you'll have it in the menu (like "paste content"). Helpful

Alex: In Tokyo, we wanted to see language on user gestures. the language around semantics is hard, becasue you delegate your UI

...I'd love to see security and privacy section in the doc, and non-normative notes for implementations.

Dan: do they not have an issue on this?

...On both this and the keyboard map issue, we don't have specific links from our issue to the issue that we're interested in. I'm happy to do that legwork. 

Travis: We could track their issue 52, on user gestures. 


  ## [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - David

David: Alex and I met with Eric and Matt before our last f2f. I need to understand what the current state is.

Alex: I spoke with Matt last week. I understand he's busy with other stuff right now, but will come back to this.

David: Let's revisit after the AC meeting? 

## [WebVR](https://github.com/w3ctag/design-reviews/issues/185) - Peter, Travis, Hadley, Alex

Travis: We've met them several times, did a thorough review. Not apparent what the next steps are, but followup from a comment on 31st. this AM I filed these points on their issue list. Should we close it and ask them to come back at a later stage?

Dan: I'd like to close it

Alex: I'd like us to invest more time on this. Specifically, I'm concenred they'll ship something that hasn't progressed enough. The changes we requested were large. 

Dan: Should we invite them to a call? if so then we need to have an agenda for that discussion.

Alex: Just an update on our previous conversations. 

Dan: Travis, can you invite them to our 8 May call?

Travis: sure



* [Offscreen Canvas](https://github.com/w3ctag/design-reviews/issues/141) - Travis, David, Alex, Sangwhan
* [With Credentials](https://github.com/w3ctag/design-reviews/issues/76) - David

Followup:

* [Deprecating nonsecure cookie delivery](https://github.com/w3ctag/design-reviews/issues/239)
