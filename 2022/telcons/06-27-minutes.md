# TAG Teleconference
#### 27-29 June 2022

---

## Agenda:

### Breakout A (Europe / US) - [2022-06-27](https://www.timeanddate.com/worldclock/converter.html?iso=20220627T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov
* [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov
* [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-06-28](https://www.timeanddate.com/worldclock/converter.html?iso=20220628T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744) - @torgo, @maxpassion, @atanassov
* [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov

### Breakout C (APAC / Europe) - [2022-06-28](https://www.timeanddate.com/worldclock/converter.html?iso=20220628T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman
* [Site-initiated mirroring](https://github.com/w3ctag/design-reviews/issues/745) - @ylafon, @maxpassion
* [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro
* [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou
* [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

### Plenary Session - [2022-06-30](https://www.timeanddate.com/worldclock/converter.html?iso=20220630T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


-----


## Breakout A

Present: Peter, Amy, Yves, Tess 

Regrets: Dan, Lea, Hadley,


### [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov

Amy: see the [cg report](https://docs.google.com/document/d/1D-UbhD7_d_X8h1_aEFV-nrlkMf2pQDTuf_s70ycYj20/edit). A list of existing auth scenarios - only a few small parts actually break in absence of 3p cookies. Someone who knows more about js apis than I do should review the explainer.

Peter: in OIDC or SAML the IDP signs the response so the RP knows to trust the IDP. I don't see anything about signatures, does it implicitly trust the UA

Amy: Not sure, seems so?

Peter: Hard to believe they would have just ignored that. ID token itself is maybe a JWT? Kind of vague.

Amy: Has there been much discussion in privacycg?

Tess: we've had a couple of joint meetings. Specific topics. PrivacyCG doesn't do privacy reviews, so nothing to point at. Eg. we met on the relationship between fedCM and the login status api. At least one other, generally about when 3p cookies go away.

Peter: ability to scrape accounts api? But looks like you have to have a cookie to access that, so signed in once with the IDP before you can get back the accounts.

Amy: not clear there's anything to stop IDP tracking you across sites, they need to know what you're logging into

Peter: yep, more of a feature, for session management

Peter: is it possible to spoof the logout endpoint and log people out of sites? You should be able to go to the IDP and say log me out of everywhere - that's a feature. But not for other people.

Tess: out of scope for this is logging into the IDP itself right? Reasonable to assume the IDP would gate that button.

Peter: can I go to RPs and say by the way Tess logged out? More of a DOS attack than a leakage. Apparently an API call from the UA to the RPs. Not sure what that handshake looks like. Other than that generally looks fine to me. Minor things in the fedcm.json, they have colours and branding - dark mode support?

Amy: intent to trial on chrome status..

Peter: where does it go from here? 

Peter: already an issue about light mode vs dark mode

Amy: could ask about feedback from their origin trial? and from devs?

Peter: token is a JWT, just not clear in the spec.

Amy: seems to always require name and picture... not all sites will want that. What's the bare minimum to identify an account?

Tess: username probably

### [The Popup API](https://github.com/w3ctag/design-reviews/issues/743) - @LeaVerou, @atanassov

### [import.meta.resolve()](https://github.com/w3ctag/design-reviews/issues/746) - @LeaVerou, @plinss

### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

### [Shared Element Transitions API](https://github.com/w3ctag/design-reviews/issues/748) - @LeaVerou, @atanassov


## Breakout B

Present: Peter, Max

Regrets: Rossen


### [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744) - @torgo, @maxpassion, @atanassov

Max leaving feedback re explainer format and multi-stakeholder. Overall looks ok.

### [COEP reflection](https://github.com/w3ctag/design-reviews/issues/742) - @torgo, @atanassov


## Breakout C

Present: Dan, Amy, Yves, Lea

Regrets: Max, Rossen


### Reviewing some of the pending issues from last week's breakout C to check status

### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

### [I18N String-Meta and WebIDL](https://github.com/w3https://www.selina.com/uk/camden/ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman

### [Site-initiated mirroring](https://github.com/w3ctag/design-reviews/issues/745) - @ylafon, @maxpassion

Dan: Max has comments -> plenary

### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

Amy: seems stalled by the requester

Dan: closing for now, can reopen when it's ready for review

**closed**

### [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou

Dan: we asked for an update to their explainer, nothing since. Lea do you know anything more?

Lea: I don't think so. Should we ping them again?

**we review their explainer in current form**

Dan: it *is* in the CSS working group.

Amy: would very slightly increase the fingerprinting... Also looking at their security & privacy review - Sam W points out that media queries level 5 doesn't have a security & privacy review... 

```
Hi folks - it looks like our request for some additional information in the explainer hasn't been actioned.  We've gone ahead and reviewed with the information provided.  It looks to us like this is OK.  We're slightly concerned about the additional fingerprinting surface area. We also note the lack of Security & Privacy considerations sections in the Media Queries spec - is this likely to be added in the near future?  Also it seems like this review was filed [as an afterthought](https://groups.google.com/a/chromium.org/g/blink-dev/c/OpUsOWnnN6c/m/QFfsQwmUDAAJ) rather than as a legitimate request for wide review.  
```

Sangwhan: introduces extra entropy.

Dan: satisfied with concerns?

Sangwhan: guess it has an intent to implement

Lea: wouldn't say the user needs are completely obvious. I don't think we have a problem with the feature, but they haven't responded to us after months.

Amy: what does the CSS WG think?

Sangwhan: looks like they asked for TAG review *after* they shipped it. This is an antipattern.

Dan: [closes with concerns]

### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

Sangwhan: are we happy with this api? I had a followup question. "If the frame is first-party and the content author would like to delegate history down (to the frame) and then back up, how would that work? Obviously this is a bit of an edge case, but mostly asking out of curiousity"

**Sangwhan leaves comment and we will try to close at the plenary**

### Specs we left feedback on last week

Dan: no reply on WoT

Amy: do we have a way to make sure they saw the review?

Dan: topics, attribution reporting, CHIPS, no responses. Turtledove, not sure what the status of this work is. Will email Chris H. WebXR? Proposal in [their issue 1269](https://github.com/immersive-web/webxr/issues/1269) which looked good but no activity.


## Plenary Session

Present: Dan, Amy, Max, Peter, Rossen, Yves

Regrets: Hadley

### F2F agendas...

#### Privacy Sandbox briefing (Sangwhan to arrange)

Dan: to schedule a special session at the f2f.

### Breakout B Time Slot

Everything moved to Tuesday next week, for one week only (due to Murca Day) and Breakout B one hour earlier than rearranged Breakout A.

### Breakout Rollup

#### Breakout A

Peter: FedCM.  Filed comments, issues... filed and issue talking about logout... 

Amy: no reply to my question yet - looks like it's gone to origin trials... said we're excited to hear back.

Peter: should we close this?

Amy: we should wait until we know where they take it after the CG...

Peter: they asked for comments in their repo...

Dan: multi-stakeholder?

Amy: webkit some positive indication, mozilla no indication yet but no negative report yet.

Peter: in general it's a good direction to go. Next-gen OIDC.

Peter: SAML has more implementations than OIDC but I don't think SAML is a pattern we should adopt for the future.

#### Breakout B

Peter: it was Max and me. Feedback on screensharing... we punted on coep reflection.

#### Breakout C

Dan: we closed conditional focus, stalled by requester. Video-prefixed media features also closed. Navigation API - Sangwhan left comment.

#### [Site-initiated mirroring](https://github.com/w3ctag/design-reviews/issues/745) - @ylafon, @maxpassion

Max: have comments for this, in general user scenario is valid. I have only one technical comment which is maybe related to security and privacy. Wondering whether any mechanism for developer to know whether there is an existing session of this remote mirroring of the screen. Sometimes maybe there is a network problem or the user closes the browser, but not sure if the session will be terminated. Otherwise we will have some security and privacy issues.

Dan: Worth asking. 


#### [I18N String-Meta and WebIDL](https://github.com/w3https://www.selina.com/uk/camden/ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman

Dan: we haven't had feedback from Hadley's comment on i18n string meta. Close? Wait for Hadley.

### Issue Triage
