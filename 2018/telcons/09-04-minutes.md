## TAG Teleconference
##### 04 September 2018

Present: Dan, Peter, Kenneth, Lukasz, Hadley, Alex, Yves

Regrets: Travis?

Scribebot: Dan

---

Agenda:

* Followup - Proposed TAG role in W3C-WHATWG relationship - Dan

Dan:...I'm not sure there is anything more to talk about... at this time.
  
* Followup - Proposed workflow for privacy & security questionnaire - Lukasz

Lukasz: i pasted to slack the latest committ.... no feedback from PInG yet.  Mike has confirmed that he's out.  I will put Mike as previous editor in acknowledgement.  Have transfered most of my proposals to the document right now.  

Dan:
i think we shoould review
I feel like you (lukasz) and someone from PInG should be co-editors?
i mean we all take an action to review the link you send - offline from this meeting and come back with comments next week.
(I need a chance to review in depth)

Lukaz: i can put myself as editor for now - ... Suggest a version number. I also propose - suggest that every TAG review or transition should require filling out the questionnaire. Suggest it to be madatory.

Hadley: not sure if we can do that withough putting it into the process. Domain of the AB. We can encourage.  We the w3c can't mandate anything; we are the venue where everyone comes together to agree things. We can encourage loudly but not mandate.

Dan: I am not sure we want to do version numbers. Aren't we post version numbers now? This might be toxic to some people. 

Hadley: I would agree - i think we handle version control through github committs - and by version of notes. And links to previous versions...

Lukasz: one thing I notice is that it doesn't help there is no central ... for such questionnaire...  Wonder if there would be a good idea for a standard place.  As for version numbers... Problem is we would still benefit from some facilcilities for people to compare between changes.

Hadley: you're thinking about a particular user need - eg researchers?

Lukasz: not insisting any particular way of versioning. But an option for easy comparison between changes.   I I advocate for filling the questionnaire in early. Why

David: it sounded like one of your cocnerns was to know which version people filled out. The alernative way to do that is to identify by gihthashes. I also don't thinl a version nunber would be that toxic as long as version number was in the context of suggesting ththe response say to the version nunber.

Lukasz: i don't have a concern about using githashes. We need to document it. We need to document in the security & privacy quesetionnaire - ich which version is filled out. Not insisting on any way of versioning. Only desire other people understand what has been filled.

* [OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame](https://github.com/w3ctag/design-reviews/issues/288) -  @slightlyoff @dbaron @travisleithead

Alex: travis wrote up our feedback from last time...  I haven't seen any serious update here.  Looks like some progress in the discussion from the commit side of this - suggestion commit be async and non-blocking. Interesting but no consensus. But nothing else to talk about.

Hadley: american or english Interesting?

Alex: if they're saying that commit may be totally async from perspective of application that is also (good?) interesting. That's gonna drive this design and what browsers do under the hood.  T 

Peter: Post some of those questions into the issue?

Alex: will do.

Peter: loop back in a couple weeks.

* [CSP feature 'unsafe-hashes'](https://github.com/w3ctag/design-reviews/issues/291) - @cynthia @dbaron @travisleithead

Sangwhan: they replied back ...   

[we haven't reviewed their reply yet]

Peter: we need more time. A week.

* [CSS Selectors 4, :focus-visible](https://github.com/w3ctag/design-reviews/issues/233) - @dbaron @travisleithead @plinss

Kenneth: no updates

Alex: has that PR been closed yet?

Peter: looks like it's still open.

Alex: we shouldn't be blocked for this long...

David: Floorian or I could review it... I could look.

Peter: come back in a week?

Alex: yes I will also ping Tab again.

* [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240) - @cynthia @hadleybeeman @plinss

Peter: I need to do something. I haven't had a chance. Kicked.

Sangwh abo aboan: online breakout on this?  Separate call?  Talk about a prototype?

Peteyesr: yes.

### F2F Backlog
#### [DOM](https://github.com/w3ctag/design-reviews/issues/229) - @cynthia @dbaron @travisleithead

Hadley: we agreed we would review the whatwg spec.

hhK: there is a wide review tracker for dom4.1 - the w3c one.  Missing the TAG feedback.

Hadley: we've explicitly said we won't be giving any. 

Kenneth: so what are we doing?

Peter: wide review period ended march 12.

Peter: we should still do our review of the whatwg sP
Ppec.

Sangwhan: we schedkued it during the f2f but didn't find time. I will try to get a hold of travis after this call and we can do a separate call.

Peter: reset milestone...

akeDavid: I expect a bunch of whatwg folks to be there.

Peter: we'llc heck u next week.

#### [Web Components Guidelines Doc](https://github.com/w3ctag/design-reviews/issues/227) - @kenchris @travisleithead @plinss

Kenneth: i want to move this to a more proper place.  

Hadley: mdn artifcle?

Hey:Kenneth: it's a spec like thing - rather than an article.

Hadley: turn it into a note?

Peter: we have other things like the API design guidelines document - which we are just publishing on github [ta\g]
 We can host it on tag.w3.org - we can publish a finding or note.

Kenneth: Relative difference in standing between them?

Dan: I think a finding has more weight because TAG publishes findings, but NOTEs generally don't.  But NOTEs have more process around them than finding so maybe has more standing.  I think should be more like promises guide or API design guidelines -- something that's more fluid.  We could then decide to takesnapshots.  I think we should publish like we published the promises guide.

Kenneth: repo?

Dan: I think youshould beaould be able to make a repo on TAG github yourself; if cannot ping Peter.

Peter: OK, Kenneth will make a repo, and people need to start reviewing and giving feedback.

Kenneth: People read at face-to-fcae, but more review is good.  Name web components guidelines ok for repo?

Alex: Web Components design guidelines?

Peter: sounds fine

Peter: Everyone can review, come back in 2 weeks?

#### [Intersection Observer](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff @dbaron

David: I think one of the problems was that they were inserting stuff into a list that different people interpreted this differently. The issue I believe is attempting to specify this better.

Alex: Probably worth checking across implementations...turns out there are several; Edge, Gecko, Blink.

David: The details that I mentioned might not be interoperable but not many may notice; but it would be good to have this interoperable

Peter: Next steps?

David: I'll look into this this week and revisit next week

#### [Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134) - @cynthia @travisleithead

Sangwhan: Haven't looked for bit... I think should be able to look quickly and have something to revisit next week.

### Triage
* [User Activation v2](https://github.com/w3ctag/design-reviews/issues/295)
* [User Activation API](https://github.com/w3ctag/design-reviews/issues/300)

David: Standardizing popuopup blocking algorithm which has been used in a bunch of other places in the platform.

Hadley: would help if they explained use cases better

Sangwhan: There's also a "User Activation API" issue, #300, below.  Should have same people on it.

Hadley will post requests for further explanation.


* [RTCIceTransport & RTCQuicTransport ](https://github.com/w3ctag/design-reviews/issues/296)
* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297)
* [Support codec and container switching with MSE using SourceBuffer.changeType() ](https://github.com/w3ctag/design-reviews/issues/298)
* [WebAssembly Threads ](https://github.com/w3ctag/design-reviews/issues/299)
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301)
* [Canvas TextMetrics](https://github.com/w3ctag/design-reviews/issues/302)


---



