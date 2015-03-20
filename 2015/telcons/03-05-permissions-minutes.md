#TAG Teleconference March 5, 2015

##Topic : Permissions API (with Mounir)

slightlyoff: Would love to get an overview

mounir: Most web APIs today have a way of asking for permissions, but they vary from API to API

mounir: Many of these APIs don't know if UI is going to pop or not when called.

mounir: Cite: Geolocation, and getUserMedia

mounir: Web apps work around this. Call and then see if a callback was issued, if not, then assume UI and tell user to approve the UI.

mounir: We want to solve this in a good way.

mounir: Permissions API defines some primitives for checking. 

mounir: We want to be able to adapt existing APIs to use with Permissions API.

mounir: Goal (long term) that APIs will delegate to Permissions API instead of doing it locally.

slightlyoff: I wanted to hear current status so that we can have more eyes on this API -- since it's pretty broadly applicable

slightlyoff: goal of early reveiw to ensure smooth sailing.

slightlyoff: Mounir how has this been recieved and what's the timelines?

mounir: Query, Request and Revoke permissions are the three basic aspects of the API

mounir: Mozilla feedback: they didn't like request/revoke part of the API.

mounir: Today the API is only about querying for permissions. Some folks liked others not.

mounir: Having a central place to set permissions is compelling, in addition to just querying.

mounir: Mozilla didn't like the idea of setting permissions before hand

slightlyoff: What was Mozilla's concern about requesting before hand? Help me understand...

mounir: It's challenging in the API world to talk about the UI part... hard to have those discussions.

mounir: Instead of wasting time there--just dropped the request/revoke parts from the spec.

mounir: Noted in the spec that those bits have been removed on purpose.

slightlyoff: Anyone else other than those at Mozilla that are interested?

mounir: Google search wanted permissions to get geolocation permission

mounir: Hangouts: wanted to know if the user had permissions before using it.

mounir: I see various properties at Google that 

mounir: No one from Apple seems interested (no one participated so far)

mounir: At Microsoft (those at TPAC) seemed interested; haven't heard back from them.

travis: Had a discussion about integrating time into the permission equation; I liked where that was going.

plinss: Did Mozilla give reasons why they didn't like it?

mounir: They believed that users knew what was happening when the request is made (through UI)

mounir: It's really easy to request Geoloc before hand, and then doesn't do anything, and later you use it for real.

mounir: You could very easly apply for permission in a similar way with Permissions API

slightlyoff: Current spec addresses the problem of certain APIs want to request the permission before hand,but seems closely tied to that.

slightlyoff: When would you be interested in having the TAG take a closer look at this; I know this is pretty early for you.

mounir: In terms of the Spec, if you looked today, you'd see what we want the v1 specification to be. (It's ready.)

mounir: I would like to add Requests later. It's easier to talk about requests alone.

mounir: Once we have a query for requests in place, it'll be easier to see how to integrate.

plinss: Seems pretty well designed API at this point. Anything else the TAG can do for you?

mounir: Would love to see new APIs integrate with Permissions API.

mounir: I think there is some kind of permission registry. Would love to see this used broadly across new specs/features.

slightlyoff: I wold love to see more extensibiliyt in the current API.

slightlyoff: Would be nice to enable cross-app collaboration (one app wants permission to use another); Inttroduced storage and lifetime of the permissions. I think those things would 
eventually need to be considered.

mounir: Clarify cross-app collaboration?

slightlyoff: Question of who's providing capabilities to whom. App may want to grant access; specifically things that the platform knows (built-in). Wonder if we could facilitate more general contracts between actors.

slightlyoff: How would I share between facebook? Could permissions API helps me out?

Travis: thinking about existing means for access control (e.g., document.domain, CORS, etc.)

plinss: Thinking about 3rd party services might replaces platform caps (e.g., replace geoloc, etc.) and plug-in more user services.

plinss: May want to think about extensibility and not paint yourself into a corner.

slightlyoff: Anything else to cover?

mounir: not really. What's the first steps on API review?

slightlyoff: More a question of when. What's the best time for you. This is the honeymoon period :) 

mounir: Spec is ready for FPWD.

slightlyoff: don't block on us. But now might be a good time for review.

mounir: If there are big issue we want to raise, please do so right away (Chrome implementation starting soon--next few weeks.)


plinss: Shall we start former review

slightlyoff: Yep.

plinss: And you will own?

yan: I'm happy to own that reivew.

slightlyoff: we can get something started on Github then.

slightlyoff: there's another review there we can copy/paste

##Topic: Security/Privacy Review Guide

plinss: Yan, you were interested in that?

plinss: Discussion about using the guide for editors to self-check their status.

yan: written by Mike West

yan: Someone asked why we didn't have a security/privacy guide (like we do for accessibility, etc.)

yan: Rather than wait for webappsec, just have folks self-review.

yan: I looked at this, and I think this looks pretty good.

plinss: does this eliminate the need for a security group?

yan: groups can do a review and post a survey of results, then someone can look it over and see if it looks reasonable.

plinss: anyone else have any thoughts.

travis: seems similar to what we do internally

plinss: Is Mike doing this independently, or as part of another group?

yan: he posted to webappsec, but I'm not sure. I'll check with Mike

plinss: It would be good to know--I'd like to see it move forward.

plinss: We need to get a process set up. Is this a job for the TAG or for someone else?

yves: If there is a process, then the AB should be involved.

plinss: Maybe the TAG can help Mike by presenting to the AB for him.

**yan: take action to chat with Mike.**

plinss: Anyone have anything else.

plinss: Let's adjourn!


