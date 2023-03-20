## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/03-13-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-03-13](https://www.timeanddate.com/worldclock/converter.html?iso=20230313T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov
* [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss
* [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @atanassov
* [(Document Subtitle): Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @torgo
* [text-wrap: balance](https://github.com/w3ctag/design-reviews/issues/822) - @LeaVerou

### Breakout C (APAC / Europe) - [2023-03-14](https://www.timeanddate.com/worldclock/converter.html?iso=20230314T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman
* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @torgo, @rhiaro
* [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon
* [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman
* [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman
* [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro
* [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-03-15](https://www.timeanddate.com/worldclock/converter.html?iso=20230315T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

### Call Minutes


### Breakout A (Europe / US) - [2023-03-13](https://www.timeanddate.com/worldclock/converter.html?iso=20230313T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Tess, Lea, Dan, Peter, Yves, Hadley
Regrets: Rossen, Amy

#### [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776) - @hober, @cynthia, @maxpassion

Tess: looks like Yves had questions and they were answered...

Yves: ...

Tess: linked moz and webkit standards positions.. some interesting discussion. There is already a "beacon" spec - this is different. It's on purpose. But seems unfortunate that you have 2 similar sounding things with similar purposes. Feels like we should try to merge these things or find a way to integrate them.

Dan: that sounds architectural.

Tess: beyond that ... the basic issue 

Dan: no user needs...

Tess: sites want to reliably know if something bad happened. But if something sufficiently bad happens then site can't reliably know.  E.g. device crashes; browser crashes.  There is a tension bwteen having a reliable signal and the reality of software in the wild.

Dan: state and the web being stateless...

Yves: you have local state with cookies -- local storage... so this is not about giving state.

Dan: can we push back and ask for some user needs?

Tess: right now the explainer only has dev needs - you can infer user needs. But I'd rather them to be explicit.

Peter: also there should be a user benefit aside from analytics and tracking.

Dan: leaves comment on user needs

Tess: will read the discussions and follow up.

#### [FedCM Auto Re-authentication API](https://github.com/w3ctag/design-reviews/issues/813) - @rhiaro, @hadleybeeman, @plinss

Hadley: we weren't happy with explainer - asked them for a proper explainer - they have not responded.

#### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

Hadley: this is the one we were happy with ...

Dan: i think Amy was going to leave a followup comment - let's 

*bumped to plenary*

#### [text-wrap: balance](https://github.com/w3ctag/design-reviews/issues/822) - @LeaVerou

Lea: process should be if there's no objection in channel - rather... People should be more active on slack...

Lea: things should not be accepted and closed summarilly without people looking at it.

Lea: a lot of excitement in the open community about this.

*we leave to async process to close*

```
Hi - just a quick request hopefully - we noticed that the explainer is a google doc, not in a markdown next to the spec.  There doesn't appear to be an answer to the security & privacy questionnaire. The chrome status also doesn't reflect the reality as shown by the web platform tests info. We recognise that this is already in the spec and there's significant developer support but can you please update the request info so we can progress?
```

Dan: *leaves comment*

#### [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811) - @LeaVerou, @atanassov

Dan: [changes since previous CR](https://www.w3.org/TR/2023/CRD-WCAG22-20230125/#substantive-changes-since-the-6-september-2022-candidate-recommendation)

Dan: suggest we close and give a positive review based on these 5 items .. I don't see any issues here.

Hadley: 3 of them are editorial. 5th one is renaming a session to "enhanced" 

Dan: on 2.5.8 I don't see anything worrying ..

Hadley: only one that seems consequential is the parsing... Says "This criterion was originally adopted to address problems that Assistive Technology had directly parsing HTML. Assistive Technology no longer has any need to directly parse HTML and, consequently, these problems no longer exists." I presume that is the case... 

Dan: this is in their wheelhouse...

Hadley: slightly architectural... But I think it's fine.

Lea: nothing seems worrying to me.

```
Hi @michael-n-cooper - thanks again for bringing this to our attention as part of wide review.  We've reviewed and we're happy to see this go forward.   Can you clarify regarding the parsing issue (4.1.1) - just for our benefit so we understand why AT is no longer parsing HTML? Are you confident that there aren't any remaining edge cases where that would still be needed?
```

Dan: comment left let's close at the plenary.

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Dan: I asked them to provide some user needs

Tess: but they provided you developer needs instead

Tess: left a comment to that effect

#### [(Document Subtitle): Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @torgo

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

#### [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767) - @maxpassion, @atanassov


### Breakout C (APAC / Europe) - [2023-03-14](https://www.timeanddate.com/worldclock/converter.html?iso=20230314T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

#### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

#### [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman

#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @torgo, @rhiaro

#### [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799) - @cynthia, @torgo

Sangwhan: it's the best that can be done right now... a few weird things with gamepad - deterministic.. the group should re-visit.

```
We are late getting to this so apologies. We're largely happy with this proposal given the constraints proposed and in particular the integration into Gamepad API itself and the documented non-goals. I would like to suggest that you amend the explainer with some explicit (example) user needs - "the user wants to do xxx..." rather than starting right away with "Enable applications to consume inputs ...". However we're happy to close this.
```

Dan: **leaves comment and closes**

#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

Yves: [negative standards position from Mozilla](https://github.com/mozilla/standards-positions/issues/732) on this one.

Dan: explainer and spec points to PRs which is making things difficult.

Yves: this is local file system...

Yves: Webkit position is negative as well...

*discussion on whether this is OPFS or not*

Sangwhan: the use cases are in [explainer](https://github.com/a-sully/fs/pull/2/files)

Dan: Security Consideration - how does a site gain explicit write access to a file?  I'm very concerned about security mitigations...

Yves: it's not only ststem files... directories in home directory that set environemntal variables etc...  Lots of data writable in user directory. Once you know you're in a safe environment then move() is a no-brainer but ...

Sangwhan: There is [this](https://wicg.github.io/file-system-access/#privacy-wide-access)

Dan: "might want restrict" is loosey-goosey

Yves: "default download" is difficult - you may have sensitive info such as statements from your bank...

Sangwhan: move can be a destructive operation... 

Dan: we previously reviewed https://github.com/w3ctag/design-reviews/issues/390 and this became native filesystem?

Sangwhan: yes.  Positive. There were multiple iterations... we arised issues. they addressed our feedback. Not everyone in TAG was happy. But we discussed it as a group and decided it was probably OK.

Dan: concerns about mitigations in file system access...

Yves: having user agent showing you files in your directory... but doing the same from javascript is very different because you're already leaking some information.  Unless there are good security requirements -enforceable security aspects in the spec. Move() is not really the issue...

```
Hi @a-sully - thanks for this. We're reviewing today and noting that this is built on top of File System Access which we previously [reviewed positively](https://github.com/w3ctag/design-reviews/issues/390).  Can we set up a session where y'all join us to discuss the security issues, abuse cases, and potential mitigations?
```

Sangwhan: is there a way to have secure file access besides OPFS? It seems to me the answer is no.  Philosophical question ... 

... for this API to enable malware then the malware would have to access on the disk. Even OPFS if you have a file handle you can push malware.  

Yves: recommendation of multi-stakeholder support and that includes security aspects because that's where apple and mozilla have issues as well...  If we fix the security aspect - won't be easy but it's doable - then it will provide lots of benefit.

Sangwahn: *Expresses concerns about this pushback...* I don't see how the issues can be mitigated... 

#### [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

#### [WebAssembly Garbage Collection extensions](https://github.com/w3ctag/design-reviews/issues/814) - @cynthia, @ylafon

#### [CR Snapshot Review for EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/816) - @cynthia, @rhiaro, @hadleybeeman

#### [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

#### [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro

#### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @rhiaro, @hadleybeeman

#### Plenary Session - [2023-03-15](https://www.timeanddate.com/worldclock/converter.html?iso=20230315T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Dan: [comment from Amy from 9 feb](https://github.com/w3ctag/design-reviews/issues/768#issuecomment-1423895622)

Hadley: we're waiting form them to write an explainer...

Yves: they are working on it...

#### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @rhiaro, @hadleybeeman

Hadley: not written from the perspective of the user...

Dan: really good answers to the [security & privacy questionnaire](https://github.com/patcg-individual-drafts/ipa/blob/main/sec-priv-q.md)... 

Dan: https://github.com/w3ctag/design-reviews/issues/724 we said "multiple approaches..." do we want a different thing on each browser?

Hadley: IPA is set up with a multi-party computation model - makes tracking someone against their will a lot harder.  This differentiates this proposal...  will be better for user?

Dan: also points back to the user PoV.. 

Peter: do any of these benefit the user or just better ways of doing what advertisers want to do?

Hadley: conditional level of validation that the person has been validated somewhere else...

Peter: ...trust tokens...

Hadley: yes but trust tokens are completely anonymous...  IPA protocol is an aggregate report... measure performance of use of adverising... (Reading from the security and privacy questionnaire) a lot can be said about the relative virtues of advertising .. not all will say advertising is necessary ... however you can't do advertising without being able to measure it.  Alternatives involve tracking or surveys & panels ... expensive & slow and too inefficient for general use.  

Dan: this is what Apple also say that they do...   They have not requested a review yet even ...

#### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

Dan: *reprises the convo in breakout C*

Lea: this is important - parity with native platforms - 

Yves: we didn't say rule it out - but trying to get others (even apple and mozilla) to figure out a way to make acceptable for the user... how to design it properly?

Lea: maybe a different level of permission dialog... shouldn't be on the same level of notifications 

Dan: or geolocation...

Lea: although i'm not sure that "show file picker" needs to be behind that... 

Peter: i think you have to have a picker... file or directory...

Lea: then there is very clear user action...

Peter: moving talks about origin file system ... 

Lea: this model of having APIs live on the general web and trying to get web apps to compete with native apps... clearly not working.  Maybe this needs to be solved on the architectural level. Explicit user action "I want to "

Dan: i think it's explicit. .. but maybe worth revisiting.

Peter: i don't ever want a web app to have unfettered access to my entire filesystem... even native apps are getting locked out by OSs in some cases... this is somewhat scoped... there are things like file pickers... once the user has picked a file or directory then the app can inetract with that directory. If the move api can only access directories that the user has previously allowed then that's OK.

Hadley: user need?

Dan: one of the documented user needs is moving or renaming a big video file... 

Hadley: i can see about renaming... don't know about moving files though.

Yves: during the call we discussed if renaming could restrict to same directory only... 

Lea: i think web apps should be able to do things that other apps do.. right no the arch doesn't allow for this.

Peter: I agree - and - I think native apps have too much freedom.  The web is a different conetxt. There is the guarantee of the UA providing a sandbox. 

*debate on the nature of the web and the nature of nature*

Hadley: I agree with Peter's point, but also.. *example of google doc* on a native word processor, saving a document to local disk is trivial... on a web based word processor it's not, since you have to download the file to downloads folder and then move to the right directory in the OS (outside of the web).. as a user that's frustrating... 

Lea: input type=file... hack... it's bad for accessibility... 

Peter: there is a show open picker API .. what does that not give you that that hack does?

