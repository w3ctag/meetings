# W3C TAG Minutes - Week of Mon, 25 April 2022

## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/04-25-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2022-04-25](https://www.timeanddate.com/worldclock/converter.html?iso=20220425T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [CSS Variables](https://github.com/w3ctag/design-reviews/issues/731) - @leaverou
* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
* [FYI Review of CSS Fonts 4 `font-palette`and `@font-palette-values`](https://github.com/w3ctag/design-reviews/issues/719) - @LeaVerou, @plinss
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss


### Breakout B (US / APAC) - [2022-04-26](https://www.timeanddate.com/worldclock/converter.html?iso=20220426T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss
* [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

### Breakout C (APAC / Europe) - [2022-04-26](https://www.timeanddate.com/worldclock/converter.html?iso=20220426T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman



* [Cookie Expires/Max-Age attribute upper limit](https://github.com/w3ctag/design-reviews/issues/729) - @ylafon, @hadleybeeman


### Plenary Session - [2022-04-27](https://www.timeanddate.com/worldclock/converter.html?iso=20220427T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)


* Breakout Rollup
* Issue Triage



## Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2022/telcons/04-25-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2022-04-25](https://www.timeanddate.com/worldclock/converter.html?iso=20220425T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Hadley, Lea, Yves, Tess, Amy

Regrets: Rossen

[Some discussion on the AC]

#### [CSS Variables](https://github.com/w3ctag/design-reviews/issues/731) - @leaverou

Lea: they want to publish an updated CR... it's being used - mature - nothing we can say here.

Tess: are they things that merit review?

Lea: 2015...

Tess: is there a high level summary of changes?

Lea: no easy link to show what was ..

Peter: [changes since 2015 cr](https://drafts.csswg.org/css-variables/#changes-20151203) .. section 5. 5.1 looks like mostly clarifications and editorial... Don't think there's anything strongly architectural. Also very clearly used in the wild.

Dan: empower lea to write a closing comment?

Tess: works for me.

Peter: yes.

**recording consensus**

#### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

Tess: Pete Snyder asks [does this belong in privacy CG](https://github.com/privacycg/first-party-sets/issues/88)...?  Active for a year... relatively frequently actively working on it in privacy CG... some members of the CG shared feeling that they feel feedback is not resulting in substantive changes...  As far as how far along it is ... will it graduate from the CG?  Due to the lack of multi-implementer inetrest it's unlikely to move to a working group soon.  

Dan: What is the level of implementer interest? Is MS engaged? What other Chromium implementers?

Tess: some interest from MSFT... public signal-wise... for webkit have been mixed so far... beyond that mozilla have been consistent in lack of enthusiasm.  

Dan: have the international governance questions we asked been answered...

They are engaging with us. But I haven't seen anything that addresses the core issues that we raised. No movement.

Hober: Given what's there, it's hard to see how we end up with something ohter than resolution:unsatisfied.

Dan: Yeah. I don't want to blindside them with that, and I think they're acting in good faith. But it doesn't change the situation on the ground.

Hober: there is a perception among a lot of people that this is something Google will do anyway. Full steam ahead. I agree that the editors are acting in good faith and doing their best to move this along, but I think they need to at minimum do more to help the public image problem. It doesn't matter if they are substantively changing things based on feedback if the perception is that they are ignoring everyone and proceeding at speed. It would help to put more time/energy into making it clear to observers that they're willing to make some fundamental changes.

Dan: Issues: lack of implementer support and that many of the issues we've brought up haven't been dealt with.

Hadley: can we list those, so we have a clear closing comment for us as well?

Torgo: these: 
https://github.com/w3ctag/design-reviews/blob/main/reviews/first_party_sets_feedback.md

Origin and the security model of the web: 

We have a philosphical or maybe technical difference on this? They don't feel this changes the definition of 'origin', but in practice it does change the security boundaries built aorund origin.

Tess: existing security boundary is origin and privacy boundary is site. it loosenes the site boundary. On its own it doesn't, but what do you do with it? First party sets define the sets, but don't say how you use it. But other specs, like same party cookie — that's hwere the weakining is happening.

so they're correct that they aren't...

torgo: except that, re vagueness of scope. This seemed to indicate taht the scope of first party sets would be enlarged to things like cookies that are currently bound by origin. Everyone talking about this spec were saying 'security model based on DNS is old and we need something new for the web', which is also talking about weakening the origin boundary. So I feel this is valid. 

Hober: I think we agree. the question is: what is this for? What will you use this for? We shouldn't add fundamental new primitives to the platform without knowing why we're going to use them. Ideally, we'd have a relatively complete model of where we're going to use them. If there is only one use case, we wouldn't add something ot the web. You'd want three r four use cases, and they'd have to be very concrete.

So if there isn't consensus around those use cases, it doesn't make sense to add those primitives.

This review is putting the cart before the horse. If we can't agree the purposes of first party sets are worth pursuing, then...

Dan: On the last call, we suggested focusing in on same party cookies. But we got pushback on that, since we'd said we awanted to do layering.

But I agree ith you, that we need to look at each of htese thigs in situ, because they all have different security and priacy issues.

Hober: it's impossible to review something in the abstract. We need know what they want to do with it.

Dan: maybe we shoudl revise this document

Hadley: I think that would be helpful, for us in future and for the community. 

Dan: Include the first doc, then links to calls and issues and disucssions, and after all of this, we still feel that these issues have not been resolved.

Tess: I'll take a look and start to think about the new doc.


#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Dan: There have been some discussions on this at the Immersive Web WG f2f last week, and minutes aren't published yet. But some discussion about lowering the permission barrier on webXR AR in the first place (doesn't provide the application access to the raw camera image) and the Raw Camera Access API, which does.

I worried why would anyone use the lower, more privacy preserving one, if the user has to agree to a permission request either way? Same amount of effort either way.

I don't know the output of that. Discuss at plenary. 

#### [FYI Review of CSS Fonts 4 `font-palette`and `@font-palette-values`](https://github.com/w3ctag/design-reviews/issues/719) - @LeaVerou, @plinss

Lea: override colors does/does not support var references... discussion in CSS WG  ... no consensus.  Some [clunky syntax](https://github.com/w3ctag/design-reviews/issues/719#issuecomment-1101480840)...  but reasonable response.  Happy with that reasoning... the issues with references will be solved in a diffferent spec... 

Peter: microsoft did somehting with --color ... custom properties?

Lea: no they are not defining custom properties... author defined...

Dan: Implementation status?  Looks good from chrome status...  Shipping in 101.

Lea: shipped in 15.4 Safari 

Dan: looks good from a multi-stakeholder pov.

Dan: Shall we give it a thumbs up?

Peter: in the explainer ... custom colors ... multiple fonts being used within an element... can you reuse that overridden colors identifier?    font palette value... keyed to the font?

Peter I can raise this issue in CSS wg - don't think it's architectural.

Dan: then I suggest we close with satisfied.

**so mote it be**

Peter: *will write comment*

(dug more throught the spec and answered my question, no issue)

#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

[reading response](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1105786277)

Hadley: using a lot of bandwidth in connections that are not able to handle it?

Amy: i think we did bring this up and privacy stuff for [prerender](https://github.com/w3ctag/design-reviews/issues/667).. but don't think most of the privacy concerns apply to prefetch....   assume it would take note of the user's context and not prefetch or prerender stuff on low bandwidth

Dan: **left comment we will revisit at plenary**

[update - bumped to 9th May]

#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

**bring to plenary**


### Breakout B (US / APAC) - [2022-04-26](https://www.timeanddate.com/worldclock/converter.html?iso=20220426T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Max, Peter

Regrets: Sangwhan, Lea, Rossen


#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

**left some comments**

#### [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss

**left comment channeling Sangwhan's comments**

#### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

**punted**

### Breakout C (APAC / Europe) - [2022-04-26](https://www.timeanddate.com/worldclock/converter.html?iso=20220426T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Yves, Amy, Max, Sangwhan, Yves, Hadley

Regrets: Rossen


#### [Web of Things (WoT) Thing Description 1.1: TAG and Security Review](https://github.com/w3ctag/design-reviews/issues/715) - @torgo, @maxpassion, @hadleybeeman

Max: responded to my question. Seems it's not meant for general web service, but often web services associated with them. This proposal is focussed on IP based as we assumed. Sangwhan had security concerns.

Sangwhan: was curious how the security model works in conjunction with CORS.

Amy: I think that's a question for another spec in the suite of specs - it's orthogonal to the data model

Dan: We have previously reviewed [Thing Description](/357).. at that time we were not recording resolution with labels. Hadley closed it in december 2019. We said we don't hvae any relevant feedback on the description language itself - feedback was primarily in the [architecture](/355). Unless we think there are major issues in the data model that are architecutral..

Hadley: [diff since last version](https://github.com/w3c/wot-thing-description/blob/main/explainer/Explainer11.md#differentiation-to-thing-description-10-and-backward-compatibility). Looks lightweight. They've added in Thing Model Concept which was an appendix of the previous document. I'm guessing it hasn't changed substantively, but if it has we might need to care.

Dan: I remember David had some issues with the use of JSON-LD..

Sangwhan: I think that's a preference..

Hadley: abstract says JSON format that allows JSON-LD processing

Dan: back in time, David's concern was it should not require a JSON-LD parser in order to be part of the WoT architecture. But something that simply parses json should be able to participate. Suggest we close sastisfied based on already having reviewed previous version. Any other comments we could make?

Hadley: they say in their request for review that their Architecutre is being submitted at the same time, I don't see it yet.

Amy: and they have two other things listed saying they'll be in for review soon. We could wait until the other things come in?

Hadley: I'd prefer to do that

Dan: I can say we'll keep this open until we get the others.. [leaves comment]

#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Amy: how does it related to topics API?  Also could be an OK way to add targeted ads but maybe we shouldn't have a specific API for targeted ads for the web platform?  

Dan: not sure of the provenance - and why it doesn't reference TOPICS...

Amy: In WICG.

Dan: Two technical issues.. one is doesn't this mean every ad request will now be two ad requests? One request for untargeted and one for targeted, doubles the amount of energy/bandwidth/etc being used. The other thing is what's to stop .. I'm not convinced that these requests cannot be correlated on the backend in an ad network. They claim that there are mitigations against the network being able to correlate the requests so you wouldn't be able to tell which page you're on or who you are, but the contextual ad mechanism would know which page you're on. What's to stop the ad network correlating those by ip address or other fingerprinting information available through http headers etc?

Amy: no - i don't have an answer... they say there are mitigations in the privacy & security questionnaire.. it would be nice to know if they are concrete technical mitigations...  The stuff about the double requests... the concept of running an ad auction on the user's device seems quite heavy..

Dan: yes.

Amy: in the goals of the API there is a lot of stuff about opting out -- possibly having this stuff more in the browser gives the end user more control.  A browser of a company that sells ads might not be motivated to surface that UI in a useful way necesarilly.  

Dan: the wording seemed weird about that stuff.. talking about how users can turn off targeted ads if they don't want to see them.. but wouldn't the ad network still be correlating the information about them? It's not about the user not *seeing* the ads, it's about the .. the user seeing targeted ads is a symptom of the ad networks holding a bunch of data.. but I understand they think there are technical mitigations against correlation but I feel like they need to ask more. They haven't responded to th equestion from 8 days ago

Amy: will leave a comment

Hadley: was wondering about the browsers joining interest groups part of the process.. the user or the browser is opted into a set of groups that can be used to advertise against .. would be good to find out how they think that will work and not run wildly out of control.

#### [Media Capture Region](https://github.com/w3ctag/design-reviews/issues/710)

Sangwhan: there are disputes happening within the group again. Elad reached out to discuss. I said I'll write my thoughts and bring it to TAG. We did a review on this and we were fine with this, there were some things I didn't like that much

Sangwhan: we reviewed it and were satisfied... Then there was some disputes in the working group... 

##### [What makes CropTarget special to require an asynchronous creation? #17 ](https://github.com/w3c/mediacapture-region/issues/17)

> Background is that the factory function for CropTarget is async - and other implementors disagree. Implementing it as a sync method in Chromium seemingly would require blocking the main thread, which is undesirable. The other implementors have not done the investigation and it is rather unclear what the gains are to make this API synchronous.

Sangwhan: I have looked at this discusison and think the developer ergonomic gains would be minimal, unlike the autoplay API.

Sangwhan: based on example code I've seen I don't see a signifigant gain in terms of ergonomics for developers with sync.  You do this once.  You don't have to issue multiple crop targets.  In this case I think it's fine to be async.  Would like to hear from others.

##### [Is CropTarget name too generic? #18 ](https://github.com/w3c/mediacapture-region/issues/18)

> CropTarget name is too generic. Multiple proposals, none of them seem significantly better over another.

Sangwhan: None of them seem to be significantly beneficial over another, but prefixing it so that CropTarget contains more context on *what* kind of CropTarget this is might be useful. Indifferent on what it should be called, but the “Element” notions are probably only going to add confusion. 

Sangwhan: not namespaced to a specific context.

##### [Why expose produceCropTarget at MediaDevices level? #11 ](https://github.com/w3c/mediacapture-region/issues/11)

> produceCropTarget() is only available at MediaDevices, why not layer it as a member function of an element? Counter argument is that there is already too much stuff on element.

Sangwhan: Initially was indifferent, but after thinking about this for a bit layering it at an element seems like it might have some issues -  for some elements this wouldn’t make sense. (e.g. you don’t want to cast a `<style>` element, for example) Agree on the “there is too much on element already”

Sangwhan: a little bizarre if you stick it to an element - a lot of elements not visible... these make no sense to set a crop target on... makes more sense to have it layered elsewhere... 

##### General discussion

*These are the sorts of things that the WG should be able to come to consensus on. Not the TAG's job to pick a winner.*

Yves: if WG can't come to consensus they can pick one and if it goes to FO there can be a council. If they're are both architecturally equal, we don't have to take a position.

Dan: we can feed back that interoperability is an imperative. That should be what should be driving them, not what is most technically pure. Priority of constituents?

Sangwhan: that was referenced

Dan: we know as webrtc users that the issues of interop are many. This is something that should be guiding the WGs work. That should be the primary goal of anything. Not the most elegant or correct API. Is it going to be implemented in as many places as possible. Do they have consensus? That should be the feedback that we give.

Sangwhan: I've given that feedback...

Hadley: reasonable

Sangwhan: we can say we don't regularly resolve disputes for WGs. 

Hadley: I think we would jump in where there's an unresolveable issue that is architectural. That feels appropriate. The issue here is not architectural, we are happy whatever they choose, so we're not the final arbitrator.

#### [Cookie Expires/Max-Age attribute upper limit](https://github.com/w3ctag/design-reviews/issues/729) - @ylafon, @hadleybeeman

Yves: still a huge amount of long expiring cookies. Wondering about impact. Expiring current old cookies, .. avoid issue where people are losing whatever state they have in that case. Small comment. otherwise looks decent. Some cookies are used for authn, good to not have them there for too long.

Dan: sounds fine. I noted there was a new version of the [cookie spec](https://datatracker.ietf.org/doc/draft-ietf-httpbis-rfc6265bis/) from ietf that just came out, right?

Yves: not aware of that..

Dan: Should we be prompting the http wg to ask us for review of the cookie spec?

Yves: the spec itself is in the http wg. I expect they reviewed it. New cookies can't be more than 400 days, in the rfc. Question here is just what happens to existing cookies

Hadley: webkit's position, linked from the issue, is they're generally in favour but also wanted to say there are use cases for cookies outside of browsers where no limits still makes sense - machine to machine communication over http. So if they end up with something more nuanced than a hard 400 day rule that might accommodate or affect the cookies you're looking at

Yves: also looked at webkit position. 

Hadley: can leave comment.. but concerned about having that exception to then be exploitable..

Yves: machine to machine, there is probably a way to replace the cookie once it has expired. they just need to modify a bit for new cookies.. the issue is really about old cookies that are in use in systems that may not be updateable.

Hadley: if we do want to get into the discussion, I particularly like that that max age is the maximum and the UA can adjust the limit to be less. So presumably there would be a situation in which you could set your UA to blanket limit all cookies to 20 days or whatever works for you. Might there then be ways to handle exceptions, have behind permission prompts? But then could that be exploited to innundate users with requests to agree to a permanent cookie?

Yves: a regular UA doing set cookie with date in the future for every hit. At worst if you have one hit per year you're safe. Old things, eg. machine to machine where the cookie is set in stone somewhere. The server might forget it because it's expired, that can lead to some issues. Really edge cases.

Dan: close with comment?

Yves: Yeah I think so

Hadley: yes. Good to be supportive of overall aim. [will leave comment] [close satisfied]

Yves: Mozilla and webkit are roughly the same. Having a limit is good, and figure out some details for edge cases

Dan: multistakeholder ftw




### Plenary Session - [2022-04-27](https://www.timeanddate.com/worldclock/converter.html?iso=20220427T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Peter, Yves, Amy, Hadley

Regrets: Sangwhan, Lea




#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

Lea: can we punt?

Peter: 

#### Discussion on advancing EWP to "Statement" 

Dan: release EWP to Statement track (along side of Privacy Principles which will be going directly to Statement track)

**Recording consensus, priviso that we need to get other non-present TAG members' agreement as well - Dan to do so in chat and will record here**

*recorded +1 from Lea*

*recorded +1 from Tess*

**recording resolution to allow the Privacy Task Force to publish a fpwd to Statement track**


#### Breakout Rollup
#### Issue Triage

