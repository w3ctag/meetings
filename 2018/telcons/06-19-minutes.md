## TAG Teleconference
##### 19 June 2018

Present: Dan, Lukasz, Peter, Travis, Sangwhan, Hadley, Alex, Yves

Regrets: David

---

Agenda:
* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - @plinss @dbaron @slightlyoff @travisleithead @cynthia
* [Notification Inline Replies](https://github.com/w3ctag/design-reviews/issues/284) - @torgo @hadleybeeman
* [Triage Newly Added Issues](https://github.com/w3ctag/design-reviews/issues)
* Talk about developer meetup in Seattle


---

* [HTML 5.3](https://github.com/w3ctag/design-reviews/issues/275)

Travis: a response from charles in our issue 275 which is the request for the 5.3 tag review
... if there's something specific to look at...
... chaals replied with 2 things - [ping attribute](https://w3c.github.io/html/links.html#element-attrdef-a-ping) ... 

Sangwhan : privacy concerns related to this. we should be looking into it. official privcacy concerns
... 

Peter: sends a message back to let you know that you clikced a link - link tracking feature

Travis: w3c spec has removed it on pricacy concerns and whatwg has not

hadley: are there situations where this is good for the user other than for tracking?

... gives user the ability to block whern uses redirects....

Sanwghan: you can't block redirects...

Dan: blocking redirects happens in firefox

sanwhan: we should spend some extra time later on - we need to get educated on the use cases.
... the other issue was ruby notation - chaals is trying to ut something at risk which I am against.
... i'd like to spend some more time on this as well.

`<rb>A<rb>B<rb>C<rt>a<rt>b<rt>c`
  
we can tackle it in our html general review.

Travis: agree

Peter: what do we do with 275?  

Dan: f2f?

Sangwhan: yes.

Travis: i think we should take this feedback and drop it into existing issues and then close it. I'll take that ACTION.

Peter: ok.

Travis: we received one other comment on 244 - custom elements portion of general review. question there was to review the question about attribute names.

Peter: what should we do with it?

Sanghwhan: on ruby by f2f.

Peter: and 244?

Travis: let's put it on the f2f.

* [Web Share Target API](https://github.com/w3ctag/design-reviews/issues/221) - @plinss @dbaron @slightlyoff @travisleithead @cynthia

Travis: I read the thread...

Peter: Alex and david are working on this...

* [Notification Inline Replies](https://github.com/w3ctag/design-reviews/issues/284) - @torgo @hadleybeeman

Hadley: dan & i talked about it earlier - we were concerned at abuse cases and for the notification api itself to be abused. because inline replies allow you to erespond to a notificaiton in the OS rather than in the brwoser, the spoofing potential is higher. Some considerations would be nice to see in the explainer and the spec. We also talked about permission delegation. I can't think of a situation where [delegation] would be appropriate. in this case. I understand why they want to have inline replies but they need to think about the broader implications.

Peter: especially - ripe for fishing attacks - if it comes from an iframe.

Sangwhan: possible?

Hadley: we'd like to make sure it's not.

Peter: any indication of ...

Sanwhan: no mention of origin

Travis: lots up to the user agent but I agree spec should note more of it.

Hadley: there is a line between spec and implementation but it shoudl be laid out int he spec...

Lukasz: my initial view here https://github.com/w3ctag/design-reviews/issues/284#issuecomment-398437072

Alex: everything about notifications is advisory - it can choose not to display the interaction - always best effort. No guarantee something will be displayed. the UA is in its rights to ignore.  The chrome team is specifically looking at downpriortizing [something] notifification. But agree these should be outlined.

Hadley: we shoould build the web for users - and not for web developers... down to user control.

Alex: requests for permission - one fo the things we are starting to look at so that when you navigate around you don't see requests - by not allowing requests in certain situations.

Travis: window.alert - and it's abuse over time.

Hadley: I rememebr that.

Travis: user agents have changed the approach to that and I would expect the same.

Alex: the ability to know whether a request for permission will generate UI - we don't have a handle on it right now - gated request surface - i'd love to see a uniform answer to this via the permissions API. We don't have that today. It would be useful for all of those things.

Travis: i wonder how that would work in the abstract - user would evaluate ...

Hadley: has anyone looked into the process for revoking permission -

Alex: we (chrome) think it should be possible programmatically to drop permissions... Mozilla disagree

Travis: i'm a fan of an approach that decays permissions over time.

Hadley: a site you've never been to before - uninformed decision

Alex: in chrome - a complex collection of "points" for different actions in origins - as a gate for certain things. It's a heuristic. Knowing when you pass a threshold...

Hadley: no plan to standardize that?

Alex: i think it would be standartized via an event - e.g. on the permissions API. 

Lukasz: i agree permissions should decline over time - why not at least allow the web site to include some kind of ... browser configuration should have a preference. 

Peter: i get abusing notifications - but sometimes it's a feature user really wants.

Dan: yes - high user apps notifications are vital 

Hadley: sthen some site smight only make sense through a certain browser... 

Alex: we should have browsers implementing their own policy.    With install prompting we do require some inetraction - it's async and gated.  [notification permission should be similar]  This is a place where having uniform request for permissions (permission API) woudl make things easier.  If we had a uniform APi then adding time limitation would be easier.

Lukasz: interripting a user outside of a web browser.

Alex: you can create a notification and show buttons - so you can interact with notifications with yes and no buttons... without opening the web page.

Lukasz: yes but at the moment you are unable to paste someting or type your password.

Hadley: Are you worried about something?

Lukasz: worried about abuses - next level of ... [risk]

Travis: a limit set of options to offer to the web site developers and a broader set of options to offer to users.

Hadley: takes it back to flagging it up clearly.

Dan: other considerations?  I will ping the requestor ...

Lukasz: other considerations - what happens now?

Alex: permissions are orthogonal - notification permissions - has been there for a while.  we should probably have that conversation witht he permossions API.  

Hadley: we were talking about a workshop - permissions workshop. Can we discuss some of it then?

Lukasz: the cfp is not finalized yet. 

Dan: I will ping the requestors.

* [Triage Newly Added Issues](https://github.com/w3ctag/design-reviews/issues)
* Talk about developer meetup in Seattle

Peter we've got triage stuff - and old issues.

[OffscreenCanvas new commit() and DedicatedWorker.requestAnimationFrame ](https://github.com/w3ctag/design-reviews/issues/288)


[Request.isReloadNavigation and Request.isHistoryNavigation](https://github.com/w3ctag/design-reviews/issues/289)

Alex: these are service worker APIs - addressing some analytics and monetisation problems - these were agreed in serviceworker working group - 3 of them - 

Travis, Sangwhan

[cookie store API](https://github.com/w3ctag/design-reviews/issues/290)

Alex: this is the async cookie API ... cookie gets and sets...  synchronous --- create slowness. 

Travis: is this the spec that integrates with service worker?

Alex: yes - we don't have any sync IO APIs right now in service workers. having an async API for cookie access gets us what we need there.

Dan: we need to treat cookies with a lot of care.

Alex: it donsn't change the cookie model.

Sangwhan: didn't MS havea related proposal?

Travis: yes i will sync with MS people.

Dan: does it mess with blockers?

Alex: in this case the request goes out and the cookies are stapled to the requests outside of the user control. 

Hadley: it would be good if their explainer included use cases. would love to see these cases be written out.  [will feed that back]  

Alex: it would be useful to see a set of considered alnernatives here.

Peter: what milestone?

Hadley: have they talked to the IETF?

Alex: not sure - there was a conversation about how this interacts with secure cookies and siteness vs. originness - decision was made not to change anything about that.

Hadley: it would be good to join up with them...

Sanwhan: we couldn't use web locks why?

Alex: didn't have web locks

Alex: if a cookie changes behind your back - you can ... a notification.. i don't know whether web locks do that.

Peter: what milestone?

Hadley: 2 weeks?

Travis: i think we will need a couple of discussions to close it.

Peter: i set this for next week

Hadley: +1 

