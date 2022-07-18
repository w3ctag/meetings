# TAG Teleconference
#### 11-13 July 2022

---

## Agenda:

### Breakout B (US / APAC) - [2022-07-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220711T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou
* [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss
* [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov

### Breakout A (Europe / US) - [2022-07-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220711T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov
* [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov
* [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

### Breakout C (APAC / Europe) - [2022-07-12](https://www.timeanddate.com/worldclock/converter.html?iso=20220712T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman
* [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman
* [Site-initiated mirroring](https://github.com/w3ctag/design-reviews/issues/745) - @ylafon, @maxpassion
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman

### Plenary Session - [2022-07-14](https://www.timeanddate.com/worldclock/converter.html?iso=20220714T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout B

Present: Dan, Peter, Max, Rossen

Regrets: 

### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

Peter: related to 737.

Peter: primary feedback was that it's weird to create as signal. Why not an abort controller?  

Rossen: are you talking about the abort controller itself?

Peter: it's a factory method on abort signal. we thought : construct a regular abort controller and pass in a timeout parameter.  Times out after a given time. 

Peter: I don't understand the motivation... but it looks like it's been implemented by Firefox and Safari.  

Dan: resolution: satisfied with concerns?

Peter: you want the ability to time out on a fetch. If all you want is a timeout then you pass that into the fetch.. but if you want the ability to timeout and abort... then you have to go through girations... 

Dan: worth leaving that feedback?

Peter: yeah - if you want a timeout and the ability to abort then I think they made it more complicated than it needs to be.  [Could be a middle way.]

Rossen: agree to leave that feedback.

Peter: ok will leave it.



### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

### [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss

### [Font Table Access API](https://github.com/w3ctag/design-reviews/issues/400) - @hober, @plinss, @atanassov

Dan: Re-opened in March due to [new information](https://github.com/w3ctag/design-reviews/issues/400#issuecomment-1051070031).

Rossen: **reviewing new info**

Dan: they think they've resolved the issues we raised in 2020.

Peter: a lot closed without explanation of how they were addressed.

Rossen: **reviews status of linked issues**

Peter: Joshua Bell is now main editor for the spec.

Rossen: I'd ask - what the actual resolutions to these issues?

Peter: I seem to recall that we didn't want to see 399 happen - TAG consensus was that we'd rather see a chooser than enumeration API.  They still have an enumeration.  

Rossen: I want to see where these issues are resolved - i looked through some of the commits they have - they added [fingerprinting](https://github.com/WICG/local-font-access/issues/25) - but no clue what answer to ToC in explainer means... 

Peter: older vers of API was only exposing one font format - now it looks like their API just returns a blob of bytes.   Their response is "here's bytes parse it yourself" - which seems the exact opposite of what we're asking for which was "parse it but don't just to opentype".  

Peter: regarding fingerprinting - no mitigation suggestions just some info - for example "in incognito mode, don't expose the fonts" or something similar.

Dan: it doesn't really look like they've resolved the issues we've raised.

Peter: they did add a "prompt the user to choose" step.  

Dan: not mentioned - that should be listed under mitigations in the privacy & security section - and highlighted in their comment on our issue.

Peter: yeah it's not mentioned anywhere...   They did throw in a choose but their mechanism is still "give me all the fonts" and then allow user to choose which fonts to expose - we asked for "let the user choose a font and then you get back a font". Users will just hit "select all" and move on.

Peter: they say users of this API will want to provide data to libraries that expect all the fonts... justification for blob approach.  Curious what libraries they are talking about. Seems the goal of this API should be to replace those libraries.

Rossen: agree.

Rossen: will leave feedback accordingly.  

Dan: LGTM

Peter: yeah.

Rossen: [posts comment](https://github.com/w3ctag/design-reviews/issues/400#issuecomment-1180572491)

## Breakout A

Present: Peter, Rossen, Dan, Hadley, Amy, Yves

Regrets:

### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

Dan: disentangled from FPS.... new explainer merged. The issue before was too dependant on FPS. Now we can rereview.

Amy: changes are mostly removals of paragraphs...

Dan: partitioned means...

Hadley: cookies double keyed to both sites involved...

Dan: I think that's good.. Does it suffer from the same problem of why would people use this?

Hadley: I think we asked them that

Amy: 'when 3rd party cookies go away...'

Yves: opt in (by the developer) - a system could keep some state.  But with the restriction that cross site tracking won't be available.

Hadley: I think we're on board with the aim  - disrupting the model of an ad in an iframe being able to track you is a good thing for the user.  I think we're fairly happy with how this is written out... However some info on CDN / load balancing that i haven't revived. But I haven't seen any red flags.

Rossen: last time I looked it I was positive.

Peter: in a world without first party sets what's the benefit?

Hadley: standardizes the double keying...

Yves: with demise of 3rd party cookies - its a way to not entirely get rid of them but to limit their invasiveness...

Peter: so it's a way for authors to opt in to what they get by default in Safari & Firefox.

Hadley: I read it as a half step by Chrome towards where the other browers are.

Yves: opt in per site.

Dan: they envision need for developer opt in even after the phase in.. sounds up in the air, we could ask about that

Hadley: we could encourage moving towards not being opt-in. [Example](https://github.com/privacycg/CHIPS#third-party-locator-service)

### [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov

Hadley: Amy are you happy with [sam's response](https://github.com/w3ctag/design-reviews/issues/718#issuecomment-1171734451) ?

Amy: yes - although "web identity API" is not my favourite naming...  could be "web identification API"... identity is a controversial word.. invites potential scope creep or general confusion or upset..

Hadley: I think it would be useful to tell them that. 

Amy: I'll leave a comment to say "thanks looks good" and leave that comment.

Hadley: name and picture always involved? Sam says it's an undersirable shortcoming.  If we're going to sign off on the review can we say something like that?

Amy: At this stage of early review - just that they know it's an issue is good enough.  

**discussion on venue**

Peter: It would be nice if a working group had this on their radar...

Amy: have they liaised with web app sec?  I will leave a comment and set it to *proposed close*.

**plenary**

### [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov

Peter: already a ?? cross origin embedder policy

Peter: maybe instead of ... put them all in the window object - makes sense to me.

... if they create a policy object would you expect to see all the other policies there?

Rossen: in their S&P... there is a costly and polyfillable thing and this is an API to let you do it

Dan: jumps right into talking about solution and assumes a whole ton of knowledge without bringing up to speed on the problem and the space. 

Peter: There's a PR against the HTML spec... the motivation here is for ads... to know if they will be effected by this policy...

Hadley: this isn't even in WICG...  Opening comment - "this is a simple PR" on HTML...

```
@ArthurSonzogni, 

We will be able to review this if you can provide [an explainer](https://github.com/w3ctag/tag.w3.org/blob/main/explainers/index.md) that puts this in a bit more context.  Please remember that although we are often reviewing security-related proposals, we do not share all the back story of this proposal and how it fits together with other technologies.  What is the user need that is being serviced here?  What kinds of threats does this protect the user from?  How can the developer employ this technique?  Etc... 

Lacking use cases we can follow and review, we encourage use of our explainer template in order to capture all the other important bits in a single place - other considerations, code examples, privacy, security and a11y considerations etc. Can you please write one?

Also: in your response to question 2 of the s&p questionnaire it's a little confusing: do you expose or do you not expose the info specified?

```

Rossen: [leaves feedack](https://github.com/w3ctag/design-reviews/issues/742#issuecomment-1180650940)

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman


## Breakout C

Present: Dan, Amy, Max, Yves, Sangwhan, Hadley

Regrets:

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Amy: [PR that talks about loads of the stuff we care about](https://github.com/immersive-web/raw-camera-access/pull/12)

Dan: I chimed in on [this issue](https://github.com/immersive-web/webxr/issues/1269) - I said I wanted to close but we're blocked on how powerful the API is. Saying that with regular AR functionality WebXR is already privacy preserving so mabye it doesn't require the level of prompt, but for rawcameraaccess because it allows the raw camera image it would reqauire a prompt, so that would be a nudge that would encourage developers to use the regular AR functionality when they don't need the full power of the camera image. 

Amy: a bit about the permission prompt having 2 options - fine access, course access.. Not exactly the same...  It's helpful.  That example of what it could look like is good. Gives good info to the user on what they're agreeing to. 

Dan: yeah I agree it looks really good.  Prompt on regular AR access is already optional in the spec, eg. to enable experience with a headset and your expectation is not that you're going to have to answer a prompt to say yes I want AR when I put on AR glasses. UA should make the decision based on context.

**looking at privacy indicators section**

Amy: it's a should not a must ... "should attempt" is a bit weak. I'd accept "must attempt."

Sangwhan: it should be "should"

Amy: I wonder why it can't be a "must" 

Dan: I agree i think it should be a must to allow access to the raw camera.

Amy: I'd like to hear what their really good reasons are for it to not be a must.  Maybe it's "because goggles" - but I'd like to be spelled out.

Dan: agree, that's why you have access to the less privacy invasive version of the API

### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Hadley: similar position to attribute reporting.

### [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman

Hadley: we have feedback to Addision P - guideded by developer ergonimics... tc39 consensus and then to webidl. And we left with a question is there anything we should do and no reply. So will nudge. I think our work is done.

Yves: i already talked to Richard Ishida @r12a and @Xfq... it was done already last week.  Also ping on the issue.

Hadley: [leaves comment]

### [Web of Things (WoT) Architecture 1.1](https://github.com/w3ctag/design-reviews/issues/736) - @torgo, @rhiaro, @maxpassion, @hadleybeeman

### [Web of Things (WoT) Discovery](https://github.com/w3ctag/design-reviews/issues/733) - @torgo, @rhiaro, @hadleybeeman

Amy: I left the massive esseay on the architecture issue - they asked for github issues feedback. I will file a bunch of issues instead... 

### [Site-initiated mirroring](https://github.com/w3ctag/design-reviews/issues/745) - @ylafon, @maxpassion

Max: [answer](https://github.com/w3ctag/design-reviews/issues/745#issuecomment-1171748040) to question I raised looks fine.   

Yves: looking if it's outside of the local network - or limit it without prompt to local network access.. Seems OK otherwise if the work goes to a working group.

Sangwhan: Web screens - overlaps between IETF and second screen WG.

Ybes: As long as it goes to second screen working group then it's ok.  I think there should be differentiation of inside and outside of local network.

Dan: feed back and set as proposed closed?

Sangwhan: I think this looks fine... generalization of 2nd screen video - raw playback API.  Basically "airplay for tabs". 

Dan: their s&p self review is [in a PR](https://github.com/webscreens/site-initiated-mirroring/pull/3/files).

Yves: I'll ask them to land that PR.

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

Hadley: no comments back yet on our feedback. 

Dan: will talk to Chris H

Sangwhan: I think these things are best discussed with the folks working on it... We could invite them for a session during London.

Dan: can you find out when they can do it and we can work our schedule around it?

Sangwhan: yes. Also they are part of privacy sandbox. 

Dan: part of this session should be prioritising our time wrt to things that are provenance privacy sandbox

Hadley: [leaves comment about f2f london]

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

Hadley: [leaves comment about f2f london]

### Discussion on Trusted Computing

https://nordprojects.co/projects/oak/

## Plenary Session

Present: Dan, Peter, Tess, Amy, Sangwhan, Hadley, Max

Regrets: 

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Amy: They've [changed SHOULD to MUST](https://github.com/immersive-web/raw-camera-access/pull/12) when it comes to privacy indicator.

Dan: really good.

Sangwhan: this looks good to me.

Dan: the only thing that stops me from saying lets just close it is I know Rossen had some strong feelings about it regarding privacy implications, and he's not here.. wait for feedback

Peter: privacy indicator.. just going to be a camera icon or something?

Dan: they strengthened wording around prompting as well. They have [an issue](https://github.com/immersive-web/webxr/issues/1269) about lowering the prompting requirements for webxr AR which would then provide greater differential for raw camera access. Part of the issue is that we were requiring the same level of prompting for both, and I think that has been resolved in that the prompting for webxr ar without raw camera access is optional and that is based on the fact that it has to be up to the UA because some UAs might be specialised, eg. headset, where you're obviously entering into an AR session because it's an AR headset, so based on context. Leaves it slightly up to the UA but the prmpting in raw camera access has strong wording. Their PR also strengthens language around prompting, and talks about a prompt that would ask the user if they want coarse or fine camera access. A differential and explaining to the user a bit more what is going on.

Amy: concerned we've lowered the bar but it does feel like progress.  They've not reduced the prompting for AR - it was always optional. 

Peter: is it about the resolution? or fingerprinting surface as well?

Dan: about access to the camera image itself via the web api, whereas AR just gives you room geometry.

Peter: wasn't there something more privacy concerning about this than getUserMedia?

Dan: only the context in which people are using it, and you're feeding even more metadata, because in addition you're giving all the room geometry stuff.

Peter: seems like the hard part is educating the user about what the privacy implications are when you're asking for permission. Saying 'coarse' vs 'fine' doesn't sound like it's covering all of the issues here. Sounds like the resolution.

Dan: it's not exactly precise. 'coarse' in this case means ... it's suggested wording, it would be up to the UA

Amy: they have a few examples of how to do the prompt, and language about the UA introducing friction to discourage unnecessary use

Dan: I feel like our work here is done. Just waiting for Rossen's comment.

### Breakout Rollup

#### Breakout B

Peter: left a comment on abort signal timeout. Almost ready to close.  Weird they're making a factory method on abort signal... awkward to use the signal.  we argued a timeout on the constructor. feedback on why not both. no response. Also already shipped in firefox and safari. already merged in html.

Tess: fair comment... 

Peter: it's all sugar. 

Sangwhan: i'm indifferent.

Peter: close?

Tess: give them a week or 2?

Peter: move it to the f2f.

Peter: we didn't get to nav API or abort signal... 

Sangwhan: Nav API we wanted to close as well. I asked a question but not very important.  We can close.

Peter: Ok can you respond to D but close the issue?

Sangwhan: yes.

Peter: font table access... strong opnions... They addressed some of our concerns but in other ways made it worse.  it was re-opened.  They haven't responded to our questions yet.

Tess: will take a look.

#### Breakout A

Dan: talked about CHIPS.. 

Hadley: we decided to invite all of privacy sandbox to a session in the f2f.. but not *all* of privacy sandbox.

Dan: and FedCM

Amy: left a comment, let's leave it open to hear back...

Peter: coep reflection.. they made a real explainer

Dan: still jumps right in and assumes you know

Hadley: use cases are passive voice or from the perspective of the document

Dan: we explicitly asked for user need - what kinds of threats it protects user from.. doesn't say

Peter: my understanding is it's the opposite. It services the needs of advertisers and exposes the user to more threat

Hadley: the goal of getting them to write the user needs is so we can have that conversation

Dan: if it is solely for the benefit of advertisers, then write that.. the user will see better targeted ads

Peter: in general I'm not opposed to exposing the information. It's something a site can discover without this API. This makes it slightly more convenient for a site to be a bad actor

Hadley: don't we have a design principle for that?

Amy: leave the web better than you found it

Peter: my main concern is: is there any utility here other than being able to abuse the user? If not, maybe we shouldn't have this feature. The other part of the question they asked was about the shape of the API. Mike West made the suggestion of whether it should be a top level property, or a policy object. Similar comments - having a policy object is a good thing if this is goin to exist. But begs the question fo what else will be in the policy container and are those things that have any utility other than being able to abuse the user better.

Dan: if it's security related it should be protecting the users' security, not harming it.

Peter: as far as I can tell this is telling the site when the security features are turned off. It's not enhancing the user's security. It's like putting a sign on the front door saying your front door is unlocked.

Hadley: [leaves comment]

```
Hi @ArthurSonzogni, this is a good start. What's still missing is a discussion of the user need. For example: *as a user, I need [___] so that I can [___], and then how this API accomplishes that.*

As far as we can tell, this is telling the site when the security features are turned off. Can you help us to understand the user benefit? And who are the expected users of this feature?

```

#### Breakout C

Dan: proposed close i18n string meta

Hadley: gave them a week

Amy: on WoT - saw there was a recent issue in their repo and they asked me to split up the comment and leave feedback that way. Will do.

Dan: talked about Turtledove..

Hadley: ended up wanting to invite to f2f discussion


### Issue Triage
