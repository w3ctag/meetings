# TAG Teleconference
#### 06-08 March 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-03-06](https://www.timeanddate.com/worldclock/converter.html?iso=20230306T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Superseded by the FO Council Meeting

### Breakout C (APAC / Europe) - [2023-03-07](https://www.timeanddate.com/worldclock/converter.html?iso=20230307T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @torgo, @rhiaro
* [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon

### Plenary Session - [2023-03-09](https://www.timeanddate.com/worldclock/converter.html?iso=20230309T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FileSystemHandle.remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro
* [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----

## Breakout C

Present: Dan, Max, Amy, Yves, Sangwhan

Regrets:

### [epub](https://github.com/w3ctag/design-reviews/issues/816)

Amy: no response back yet

### [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman

*some recap of the Council discussion*

### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @torgo, @rhiaro

Amy: CSS question - one action is to rope in a CSS person.

Dan: Ask Lea to take a look?

Amy: use cases are written as "the web site wants to" no the web site doesn't want anything... 

Dan: they need to rephrase as user needs.

Max: describe the use case from the user's perspective. In the goals they only mention web site... "always non top window" but didn't give details. In the about paragraph it lists many cases but in goals secion it only lists one... 

Yves: what is the relationship with popover?  It's sharing some visual elements of a window that pops on top of something else. There are some a11y issues with popups. Does the same thing apply here?

Dan: reviewing the S&P responses.  

Yves: video has subtitles... what happens in that case if you have an a11y tool that displays subtitles in a separate window.

Dan: https://wicg.github.io/document-picture-in-picture/#spoofing don't understand

Amy: you cna have a little bubble in the PiP that has the URL (the origin)... 

Yves: it's always possible to fake what is not in the browser chrome.  difficult to ensure what is displayed is correct info.

Sangwhan: in past review I brought up the fact that picture in picture was very limited. Original proposal was a media proposal - fits into media working group. This is a general thing ... so best to go in webapps .. predecessor was media working group.

Amy: this is useful context. Review request makes it all seem like very early work. I didn't know this has been worked on on and off for five years. Changes the perspective about multi stakeholder interest.

Previous reviews:
* https://github.com/w3ctag/design-reviews/issues/374
* https://github.com/w3ctag/design-reviews/issues/226

Also related:
* https://github.com/w3ctag/design-reviews/issues/767

Sangwham: PiP not a window - it's a quasi-window...  You'd want to have the content authors cutomize and I don't see that possiblw 

*conversation on phishing*

Amy: general feature is useful... it's explicit the lack of customization is on purpose...

Sangwhan: aspect ratio... does that follow an existing pattern?

<blockquote>
@steimelchrome have you updated the explainer to clarify these issues? (And by the way, thanks @slightlyoff!) 
  
From our review in today's TAG breakout, this looks like a generally useful feature.

A few other questions:

* what is the planned route for standardizaion for this? Right now it just lists WICG.
* we noted that while the explainer is well written, it doesn't start with user needs as we've been encouraging. Can you add some material documenting the use cases from a user's perspective?
* is there any relationship with Popover #743 - considering these are both to do with layering of content
* we discussed a potential issue around accessibility... for example if there are subtitles in the PiP "window" ensuring those can be picked up by assistive technology appropriately. What other accessibility considerations have you discussed?
* we're slightly concerned with the proposed mitigation to the [spoofing issue](https://wicg.github.io/document-picture-in-picture/#spoofing) - although it's good that this consideration is called out. Can you strengthen this wording maybe with an example?
* we'd like to encourage you to use normative language in the security and privacy considerations sections, as you develop those further
* has there been any feedback from other browsers?  Have you opened up issues in Mozilla or Webkit standards positions?
* how would this feature work with multiple screens? Would it be up to implementations to decide which screen the PIP window shows up in? It seems like it would be useful to factor in multiple screens, given that proposals like [this](https://github.com/w3c/window-placement/blob/main/EXPLAINER_initiating_multi_screen_experiences.md) have come forward.
* Is the aspect ratio (width/height vs height/width) following a common pattern? If so, we might want to document this as a design principle.

Also just noting: we're going to bring more CSS expertise to bear on this review so expect some further questions.
  
Thanks!
</blockquote>

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/798#issuecomment-1457785020)



### [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo

### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

### [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

**bumped to plenary**

### [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon


## Plenary Session

Present: Dan, Peter, Hadley, Amy

Regrets: Lea

### [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

Amy: it would be useful to talk to some of the people who were around when this functionality was originally excluded from StorageAccess API.  Are there other stakeholders who agree / disagree with this? 

Hadley: Definitely

Amy: Yes.

Dan: totally reasonable to ask other editors of StorageAccessAPI to comment on this issue. Especially Anne who is ex-TAG.

Peter: question on the sso use case.

Dan: I think it's reasonable ... sso use case.

Hadley: we're asking users to fundamentally shift their understanding of the security boundaries of the web, from a url to a brand

Peter: .. sometiems I have the opposite experience, I want to be using two different accounts on two related tlds for reasons. Shouldn't be automatica and transparent and seamless, user should be able opt out. The other thing - part of the SSO answer is to get some other behaviours.. FedCM will get there as the right way to do it and they want to do it as a workaround in the meanwhile. New capability with potential for abuse as a temporary patch to do something in a way that isn't as good as the way to do it as the right way

Hadley: seconded

Dan: yes, and... they might say browsers already do this. To Hadley's point about changing the user expectation... you could argue it's already set the other way, because of the exceptions that browsers have put in place. That is the arguement being made. It's highly contextual. The [gaming brand] case that Johann made is quite clear that the intention would be .. especially with the audience of a gaming domain .. they would expect minimum fuss to get to content. However if you starta pplying this to things like google and youtube that's where it gets fuzzy. We all know that google owns youtube, but a lot of people don't know that and don't necessarily make the connection and wouldn't be okay with their google account details being shared with youtube without there being some kind of authentication

Peter: side note -there are implications, if I'm in EUrope and go to [gaming brand].de, I'm expecting european data protections vs [gaming brand].com. Conflating those two has legal ramifications. I understand the user expectation

Hadley: not just data protection. Also shopping, where they'll only use local addresses or credit cards. TWo amazon accounts for shipping to different places. 

Peter: content restricted to regions for licensing purposes..

Hadley: If the goal is to embrace the way people think it should work ([gaming brand].de is part of the same user journey as [gaming brand].com]) -- then I think it's worth saying that this isn't the status quo all around. The data protections and payments and regional content restrictions we just discussed show that.

Peter: And that goal may not be welcome.

Amy: discomfort about "legacy use cases" .. fine line between backward compat and advancing the technology in a beneficial way



```
Hi @annevk @bvandersloot-mozilla as co-editors with @johannhof of [StorageAccess API](https://github.com/w3ctag/design-reviews/issues/807) could either/both of you let us know your perspective on this proposal? We understand that requestStorageAccessForOrigin was a [departure from StorageAccessAPI](https://github.com/privacycg/storage-access/issues/113). Is this direction likely to gain your support?
```

Dan: [pastes comment](https://github.com/w3ctag/design-reviews/issues/808#issuecomment-1461483398)

Peter: [I will also leave a comment on the SSO issue we discussed]



### [FileSystemHandle.remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773) - @hober, @cynthia, @rhiaro

Amy: will write closing comment.

```
Hi there. We discussed this in our call a couple of weeks ago. We understand that this has already shipped so there probably isn't any more feedback we can usefully give here. We remain concerned about the multi-stakeholder engagement, and what happens if support for this is inconsistent between UAs. We also don't see an answer in the explainer to the questions I left in December, or information in the explainer about the impact this proposal has from a web user's perspective (rather than a site author).
```

### [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov


Dan: michael [responded](https://github.com/w3ctag/design-reviews/issues/767#issuecomment-1452505572) to our request and has indicated many things being worked on - responsive to TAG feedback.

```
Hi @michaelwasserman I see your virtual meeting happened yesterday - sorry we didn't get you feedback prior to that.  Based on your comments it looks like the issues TAG has raised are being considered.  On this basis we're happy to close this review as "satisfied".  

Regarding opening up a new review request for the entire spec, I think we already had some signifigant discussion in [issue 602](https://github.com/w3ctag/design-reviews/issues/602).  I think it may be appropriate to open up a new issue as part of wide review when the spec goes to CR.
```

### Breakout Rollup

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Breakout Rollup

#### Breakout C

Discussed history of picture-in-picture

### Issue Triage


https://github.com/w3ctag/design-reviews/issues/821

Hadley: as long as the people involved are happy... should be fairly staightforward.
