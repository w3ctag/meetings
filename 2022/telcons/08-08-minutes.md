# TAG Teleconference
#### 08-10 August 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-08-08](https://www.timeanddate.com/worldclock/converter.html?iso=20220808T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
* [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov

### Breakout C (APAC / Europe) - [2022-08-09](https://www.timeanddate.com/worldclock/converter.html?iso=20220809T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

### Plenary Session - [2022-08-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220811T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Hadley, Lea, Tess, Rossen

Regrets: Amy


### [Shared Element Transitions](https://github.com/w3ctag/design-reviews/issues/748)

*brief discussions*

Lea: totally new thing...  Work happened to improve it.  Looked at explainer - well written - we need to go through it.

Peter: I had a brief look.

Tess: also a thing where there have been lots of attempts in the broader space... to what extent are people aware of this familar with those prior attempts...?  

*put on the agenda for next week*

Peter: homework assignment to read through the explainer.



### [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov

Peter: google shipped the prompt... 

Lea: they shipped enumeration... this is access to font tables.

Dan: good to see they've added an [issue on incognito mode](https://github.com/WICG/local-font-access/issues/97) behavior in response to our feedback. 

### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov


### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Lea: This is exposing a system setting

Tess: that system setting can change during the life of a page... 

Dan: I think the device could change it without the user's express action as the user and their device moves from areas of low connectivity to high connectivity, back again, etc... e.g. on a train and using a webapp.  E.g. a whereby call... 

Tess: webrtc already does some of that for you - in the webrtc context...  Using this media query for that might not be the best approach.

Dan: you're right webrtc might not be the best example.

Peter: according to the article - the article is talking about a user setting, not an automatic detection... 

Lea: a lot of comments we got is that there is no OS that currently does that. But I wonder if it would make sense to say "this media query is evaluated on page load and never changes.." that would prevent the concern if it flips halfway through the session.

Peter: don't like the argument that nobody has done it that way so we don't have to support that.

Tess: in this case, I'm not so worried - because the setting can change web devs can code to that ...

Peter: i think they need to specify it one way or another...

Tess: reminds me of page visibility API... you want to specify a floor.  Don't want to over-constrain browsers ability in the future to do this in additional cases where they see a performance benefit... I suspec in this case you need leave some wiggle room.  With page visibility developers started to use it in contexts where spec authors didn't expect...   Metered connectionc case in this case - maybe if the browser knows you're international data roaming - maybe it should say "prefers reduced data" regardless.

Peter: what triggers it is probably outside the scope... 

Tess: you need a floor - minimally it's a user setting.

Peter: even when they say "user not likely to flip" - what about long-running apps like PWAs... I'm still using the same app a month later...

Lea: so only examining it under page load is problematic...

Lea: what's the solution....?

Peter: I don't think locking it is the worst case scenario...

Tess: locking it on pageload kind of sucks... if you're on e.g. youtube... it keeps churning through bandwidth...  If it's gonna fail you want it to fail towards using less data.

Peter: you could lock it one way and let it degrade but never let it go the other way... until you reload.  we don't have to design it - we should just detail the issue and let them [the working group] work it out.

Lea: [writes comment]()...

<blockquote>

We understand that it's a user setting. However, our concern was that the user's device may try improving their experience by changing that setting when the user is in areas of low connectivity, effectively making this work like a bandwidth MQ. 
  
Simply making it evaluated only on page load is not a solution, because for long-running apps this can end up being user hostile when the app loads in high data mode, then the setting flips (either due to user action, or other reasons). One solution might be that it can only go from high to low data mode during the lifetime of the page, and never the other way. 

We would like to see this issue addressed in some way.
  
</blockquote>

(Dan, Peter, Tess): +1

### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss

Peter: My biggest concern - on the innertext and hidden stuff it's just that it was under-specified... my biggest concern was that sync ... they're pushing back on that... 

... they have an answer on the other issue.

... sync forces a style computation.

... several times we've raised this... the prior art is broken.  Not much if any lot of prior art doing it the wrong way. we'd like to fix this... 

Tess: did Range.innerText not exist before?   I understand the temptation.. but why propogate a [antipattern]?

Rossen: are you proposing to keep this from progressing until they figure out async?

... pushing for something - from expected behaviour and pattern - makes sense - but doesn't exist anywhere... we don't have good guidance.. we reviewed the event loop at the f2f - my expectation from the TAG pov - solid guidance - this is what causes flushes, this is what causes batches... this doesn't exist.  Brings us.. we can continue to ask and be ignored or ... no alternative.

Tess: I think the alternative ... TAG vigilence...  not suggesging we do the rigorous def.

Peter: we could guuide people to look at a better alternative... 

Rossen: I think we can engage in a more meaningful way.

Peter: they can make it async.. they can turn it into an observer... there are paths forward... there's the issue of "leave it better than you found it" - just because someone else made the mistake before ...

Rossen: we're not steering them on how to move from the sync API...

Lea: we don't have a design principle don't trigger synchronous layout?

*we look back through the design principles*

Dan: open a design principle issue and get some debate going in the design principle?

Peter: What should our feedback be?

Rossen: [i will open the issue]()

Peter: I will take a stab at writing the feedback...

<blockquote>

@dlibby unfortunately there's not a lot of prior art of code not triggering synchronous layout and style computation. But this is something we're trying to fix. Existing cases tend to be bad for user experience and overall performance. We do have a general [principle](https://w3ctag.github.io/design-principles/#leave-the-web-better) about not using the existence of less than ideal designs as license to repeat the mistake.

We understand that making the proposed `adjust()` method async raises further complications, but we would like to invite your group to discuss our concern and offer possible alternatives.
  
We've also opened a [new issue](https://github.com/w3ctag/design-principles/issues/388) about the general problem of synchronous layout and style and welcome your group's input there.
  
</blockquote>

### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss

### [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov



## Breakout C

Present: Dan, Max, Lea, Sangwhan, Amy, Hadley

Regrets:


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

Dan: we closed manifest?

Sangwhan: yeah that one is satisfactory. There's package as well..

Dan: we [discussed at f2f](). The question was is the origin of the miniapp.. is the miniapp retreived from the origin, or from an intermediary that tells the client that it is the origin in some way? If that is the case, is that a strong enough indication? But the indication we got from the miniapp group is that it is actually retreived from the origin. 

Sangwhan: there is also a packaging proposal that just hit us..

Sangwhan: I still disagree with the fact that this is about the last comment in lifecycle... there's a fundamental flaw in the security model. Seems like we're talking past each other.

Dan: we can close it with unsatisfied or satisfied with concerns. Security model seems like a fundamental thing. If we can't square that it doesn't make sense to close satisfied. Other approach would be to try to have a more high bandwidth discussion with the mini apps folks. Maybe we should try to facilitate that, maybe Yves could help bring in some w3t who are working on this to help bridge the gap? I think some of it is a communications issue.

Max: that would be better than just closing unsatisfied

Dan: I'll take the action to talk to Yves to set something up

### [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762)

Amy: do we need to look at this to resolve lifecycle..?

Dan: I think we do. It's about the role of the intermediary in the lifecycle. I think the packaging seems to indicate that... zip based.. can be delieved through an intermediary.. web or offline..

Sangwhan: explanation about it all being bound to origin doesn't make sense

Dan: unless there is some kind of web packaging-like cryptographically secure approach to being able to claim that it is that origin? That's what web packaging is all about

Sangwhan: this is a competing proposal to web packaging. There's a comparison here. All of this aside, why are they using zip? Goes back to.. if it's executable by super app (web runtime) or a browser this would mean that there must be some level of origin guarantees bound into this. Web packaging has that sorted out because everything has to originate from the origin. one of the problems with web packaging is becuase of that limitationa nd certain constraints put in for security reasons it is not a very adequate vessel for shipping offline apps in specific cases, not fully addressed yet, in the works.

Dan: this did seem to be coming at it more from that perspective, where offline is ..

Sangwhan: first use case... digital signatures?

Dan: PKCS7 (?).. would it be appropriate to feed back and ask how this fits together with the web security model in terms of guaranteeing origin provenance?

Sangwhan: some level of guarantee about provenance. Other problematic parts is that there is .. this kind of approach has a problem where there is no way to deal with scenarios such as certificate revocation in a nice way. Digital signatures, the certificate chain is likely to be outside of the browser root store. That was a problem found in the context of widgets - made the same mistake. They used an app signing mechanism. Digital signatures don't fit in with the model of the web, in particular when it comes to secure delivery and provenance. You put yourself at the mercy of whatever digital signature mechanism and the trust chain that issues this. May not be as rigorously validated as the root stores brwosers are shipping. Other part is .. technical.. zip  is terrible for online resource package addressing. The reason is the header of the zip file - table of contents - is at the end. So you need to download the whole thing before you know what's in it. Cna't do random addressing easily. Can't parallelise loading of resources, that's not possible. If you want to address certain subresources wihin the package, zip makes it very difficult as you are downloading the whole thing anyway, which is why it was not chosen for web packages.

Dan: am I thinking correctly that there's a dependency between webapp lifecycle review and this review? THis seems to be a vital part of the lifecycle.

Sangwhan: i believe so

Max: the explainer suggested, I'm not sure whether miniapp packaging needs to have the dependency on lifecycle. There is a section explains the relationship of the proposals. 

Dan: that might simplify things. THe main issue we seem to be having around miniapp lifecycle proposal.. was this origin issue. If the origin issue is more oriented around the packaging proposal maybe we ought to think about closing lifecycle and putting our focus on the discussion within packaging

Max: yes

Sangwhan: indifferent. 

Dan: [notes we will set up call to discuss]

### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

Amy: I was looking at these this morning trying to figure out what to do individually (for privacy sandbox). We could write something collectively about them.  All seems to be at enabling targetted advertising... 

Dan: could be scope for a general document. Maybe about framing the issue as the tension between targeted advertising and privacy

Amy: some other thoughts on topics: as you read through the mitigations to make it more privacy preserving - it makes it less and less useful. Lots of people from the Ad tech industustry in their repo asking how useful it would be. So the question is - does it make it completely ineffective for the use case..?  Might be worth asking what's changed in Topics in particular.

Dan: maybe if privacy advocates are complaining and ad tech people are complaining maybe it is actually hitting that middle ground.. maybe it's a compromise. But no good if both groups reject it. What we did not get into in the London session is the wider ad industry feedback, besides google.

Sangwhan: within the scope of Topics related stuff, the new way of doing retargeting, I've seen other companies chime in and have written their version of the proposals - they are actively engaging, so the approach may not be that contentious. The technical details and the amount of data held where is a point of contention. Advertisers, especially the ones that are very data driven don't want to give up.. they want to give up  as little control as possible. There is a middle gorund. But definite engagement. About finding a path where the ad companies with a dependency on this look for a plan B where 3p cookies are not a thing. There are people who are not willing to accept that compromise.

Dan: maybe try to get TAG consensus on some of the issues across the board, and documenting the tension between targeted advertising and user privacy?

Sangwhan: we could make a statement about 3p cookie tracking being bad...

Dan: pretty sure we can get consensus on that. We could also talk about the fact that some new proposals are trying to mitigate or to preserve mechanisms for 3p tracking and there is a danger that in doing so we .. that the move towards deprecating 3p cookies is positive and we have to be careful as we develop new advertising enabling tech that is a replacement that we're not just replacing one bad thing with another bad thing. Something measured.

Amy: "what's the point of replacing 3rd party cookies with another set of tech that just mimics the status quo?" but more polite.

Sangwhan: definitely limits the amount of tracking. A step in the right direction. I don't have the expertise to say whether or not this will be a level playing field. It might end up being beneficial to advertisers that do not require significant targeting, who have a lot of volume, compared to those who do small amounts heavily targeted. Can't say if that's good or bad. Definitely the landscape will change. Another thing we want to mention is that 3p cookies do have a legitimate use case - single sign on. That is 99.9% is creepy tracking, but 0.1% is single sign on, we want to preserve that from not completely breaking - we want that in the statement.

Dan: we can point to things like fedcm.

[tangent discussion about single sign on in absence of 3p cookies]

Amy: I'm happy to kick it off by creating a doc and get feedback from others.

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

Sangwhan: we were upset about their "!!!" in security and privacy.. 

Dan: they removed them

Sangwhan: I'm okay with this proposal

### [Early design review: Back/forward cache NotRestoredReasons API](https://github.com/w3ctag/design-reviews/issues/739) - @cynthia, @torgo

Sangwhan: what I saw as a potential issue - same for everybody - info is already available to website. If you have extensions involved that can change the bfcache.notresotred reason. That has the potential to leak what kind of extension this user has. They did address... I think it's OK that websites know that an extension triggered it - they won't know what extension.

Dan: in the priv tf we're talking about telemetry and what kind of consent browsers should have from users before allowing telemetry-gathering APIs to function...  we should be tracking functions that are about collecting telemetry.

Sangwhan: telemetry should be a permission - an origin-level permission..?

## Plenary Session

Present: Dan, Amy, Peter, Sangwhan, Max, 

Regrets: 

### FO prep

*some discussion on the upcoming FO council*

### Breakout Rollup

#### Breakout A

Peter: drafted a comment about Range API improvements. Not a lot of prior art but it doesn't mean we shouldn't be fixing this. Also seems like something we need ?? looking at. Comes from WHATWG.. I know a lot of work in Houdini about layout algorithm.. folks involved that would have better insight into where the appropriate hooks would be. Shall I post this comment?

Sangwhan: yes, should post and do another round to wait to see what they say

Dan: for prefers reduced data.. 

Peter: lea left a comment, we got some feedback saying yeah.. 

Dan: suggest closing. Sounds like we're getting good traction, they understood the issue

Peter: yes. Get Lea's eyes on the response, mark as proposed close

Dan: will put in slack, Lea can close if she's happy

Dan: we didn't get to interaction id and event timing 670. Has been kicking around for a year. Not clear status.

Peter: discussed with Rossen, who wanted to think about it.

Dan: will put something on slack

#### Breakout C

Dan: we talked about the need to have a focussed discussion about mini app lifecycle and mini app packaging. Waiting for Yves. Hoping to set up a separate discussion. Maybe with some W3T to bridge the question about packaging and where packaging fits in to lifecycle. There are innovations in web packaging we could be taking advantage of here - need to talk about with miniapp folks. 

Sangwhan: mini app maniffest?

Dan: that's closed? oh it's still open. I left a message asking for them to confirm they discussed something with webapp group

Sangwhan: they have

Dan: we can close based on that

Dan: **closes [minapp manifest](https://github.com/w3ctag/design-reviews/issues/752)**

Sangwhan: what are the reasons to use zip?

Peter: years ago epub had something that evolved into zip that evolved into something else... 

Sangwhan: bundling thing lets you do random access better than zip

Peter: be nice to not have 3 or 4 ways of bundling packaging

Amy: we also talked about the privacy sandbox stuff, and I started a document to collate our notes about the higher level issues

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
