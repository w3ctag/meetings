# TAG Teleconference
#### 15-17 May 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-05-15](https://www.timeanddate.com/worldclock/converter.html?iso=20230515T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @LeaVerou, @rhiaro, @atanassov
* [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov
* [Spec review for Scroll-driven Animations](https://github.com/w3ctag/design-reviews/issues/828) - @hober, @LeaVerou
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2023-05-16](https://www.timeanddate.com/worldclock/converter.html?iso=20230516T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon
* [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman
* [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788) - @rhiaro, @hadleybeeman
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-05-17](https://www.timeanddate.com/worldclock/converter.html?iso=20230517T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Dan, Lea, Hadley, Amy

Regrets: Rossen


### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @LeaVerou, @rhiaro, @atanassov

Peter: looks like we got some [feedback](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1520658230).

Dan: aside - we push back a lot about developer complexity. But we don't really have it documented as a design principle. Should we?

Lea: we do have something... consider tradeoffs? [Prefer simple solutions](https://w3ctag.github.io/design-principles/#simplicity)

Hadley: and a reference in EWP, about keeping it possible for everyone to make a webpage, not needing a team of hundreds.

Lea: it's about the tradeoff, developer complexity needs to be justified by the benefit. In this case, when we looked at the big picture, they're adding this complex feature and a different syntax, and the benefit seems rather small - automating something you can do with js anyway

Dan: even Prefer Simple Solutions, it doesn't lay it out as the issue is when you add developer complexity you're giving developers a lot more work to do. The point about is it justified. Maybe there's just an addition to 2.1

Lea: something that clarifies, talks about tradeoffs.

Peter: agree it could be stronger, this keeps happening

Lea: what to reply here? I don't think it's justified... Ading an entire block of json with its own syntax with a filter scheme that combines url patterns and css selectors... I'm not sure it's worth it. Neither did Sangwhan or Tess when we looked at it

Dan: It would be one thing if this was the only way to do it and it had support from additional implementers. Given the lack of support for additional implementers... already an issue with multistakeholder

Amy: We could say "please go find more stakeholders and work together to make this less complex"

Peter: It's just in WICG right now...

Lea: I think the bar for adding a new type of json blob that gets added to html, the bar for that should be pretty high. Compared to adding an html attribute or a css property. We've done this for importmaps which is way more of an important feature than this. I could argue that this is also in the same category as linking to a manifest, sort of extension to the web platform. The benefit should be of that magnitude. If it's not, they should work with existing web platform technologies instead of adding new ones. Add html syntax or a css property.

Lea: also it limits resusability. You have to include inline json on every page, you can't link out to it.

Peter: do we have a principle about locality of data? The further apart you keep related information the more likely it is to get out of sync

Lea: that's really good, please file an issue

Peter: this has that issue as well. By centralising the prefetch rules you're taking it away from the things that trigger these rules. As you edit the document it's more likely to get out of sync. 



<blockquote>

We understand the arguments for a separate syntax; we did not argue that this is not useful. However, we think that the increase in complexity that adding an entirely separate JSON-based syntax adds to the Web Platform should be comensurate with the benefit developers get from it. Similar cases in the past that warranted this kind of increase in complexity have been JS import maps, or PWA manifests. We don't feel the benefit developers get from this is in the same ballpark, to justify this increase in complexity. Furthermore, considering the lack of multi-stakeholder support, it seems like the resulting fragmentation could create additional developer complexity and confusion.
  
We would like to suggest that you work with additional stakeholders to see if you can both garner additional support and find a less complex design.
  
See also:
  
* [2.1 Prefer simple solutions](https://www.w3.org/TR/design-principles/#simplicity) (TAG Design Principles)
</blockquote>

Lea: [leaves comment](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1548181078)

### [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734) - @cynthia, @plinss, @atanassov

### [Spec review for Scroll-driven Animations](https://github.com/w3ctag/design-reviews/issues/828) - @hober, @LeaVerou

### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia

### [IMSC HRM](https://github.com/w3ctag/design-reviews/issues/788)

Hadley: did we not conclude that this doesn't have an impact on the architecture?

Amy: the issue is... this will get challenegd at CR by the AC... Is that our problem?

Hadley: we can say we've reviewed it and it doesn't have an arch impact- it doesn't say we can support.

Amy: no harm here.

<blockquote>
  
  Thanks for this request. We've looked at the spec and had several conversations with you and the working group through the past few months. We don't see that this proposal has any impact on the architecture of the web, so we won't hold you up any further. We are really sorry this has taken so long!

</blockquote>

### [Web of Things (WoT) Profile - Review Requested](https://github.com/w3ctag/design-reviews/issues/818) - @rhiaro, @hadleybeeman

Hadley: I see the need for a profile...  It could aid adoption - this allows it to be more specific - doesn't have to do as much comfig.

Peter: there is the new "matter" solution for home automation that seems to be gaining traciton.

Dan: some iot vendors have been announcing support for this.. it's not on the web.

Peter: IP based.. 

https://en.wikipedia.org/wiki/Matter_(standard)

Peter: I think Matter is at a lower level - doesn't require http.. There should be an answer to how it plays with other standards...

Hadley: [leaves comment]

### [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768) - @rhiaro, @maxpassion, @hadleybeeman

Hadley: still stalled.

## Breakout C

Present: Dan, Max, Amy

Regrets: Hadley


### [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion

### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

Dan: back and forth on security concerns. Maybe worth putting this into the issue. In the explainer it says user agents are recommended to perform checks on files moved. There's no spec, only an explainer. S&P considerations is in another spec somewhere else.

<blockquote>
Hi - One thing that is still blocking this from our perspective is that the Spec is not self-contained so it's difficult to understand what we're reviewing - especially the privacy & security considerations.  In the explainer it says "User agents are recommended to perform security checks on files moved within the local file system" but that isn't in the linked PR. And one issue we're concerned about is the strength of this "recommendation" and whether it's appropriate to the power of this API - especially when it comes to security.  If there's a self-contained spec, can you please amend the review to point to that?
</blockquote>

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/805#issuecomment-1549120074)

### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

Amy: it's good that Johan took Anne's feedback and spun up 2 issues on that...  These security issues are pending... If you look at their [issue 29](https://github.com/privacycg/requestStorageAccessFor/issues/29) .. it's too bound to FPS.  So at this point I feel it's *unsatisfied* based on lack of multi-stakeholder support, open security issues and dependency on FPS.

Amy: FPS stands on its own as a registry function - by itself - is harmless.  But if it's used for automatically granting access to storage without the user's permission then that's problematic.  But it's not dependent on RequestStorageAccessFor ... 

Amy: comment from Alex in April - I2S.. 

Dan: [leaves comment pinging the issue](https://github.com/w3ctag/design-reviews/issues/808#issuecomment-1549145367)

## Plenary Session

Present: Hadley. Lea, Peter, Dan, Max, Rossen,

Regrets: Amy

*From breakout A: shall we re-label "ambivalent" to "lack of consensus"?*

### Breakout Rollup

#### Breakout A

* Design Review: [Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @LeaVerou, @rhiaro, @atanassov

Lea and Torgo: [explain the comment we left]

Rossen: I agree the having multistakeholder support strengthens the value proposition. But now, there is no multistakeholder support and that's why there is no developer support.

Torgo: wording says "could"

Peter: rossen, I agree with your point.

Torgo: we could add to the comment

Rossen: is there a strong community asking for something like this?

Lea: [checks chrome status]. No signals from developers. Maybe we shoudl make it more explicit that multi-stakeholder review should include stakeholders from the community.

Hadley: I agree with the intention, but don't want us to get into procedural debates that could be messy

Rossen: I agree with that, but the fact that we're only seeing one vendor doesn't mean that developers aren't asking for something.

Torgo: [reviews our issue template]. We could add "multstakeholder: impelementers, developers, etc."

Hadley: that sounds great

Rossen: +1

Peter: tied to the priority of constituencies.

...Also, we did an early review of this, closed with satisfied with concerns: lack of multistakeholder. So we're not contradicting ourselves.

Lea: we didn't mention the complexity concerns in the earlier review. It's unfortunate, because it was still useing custom sytax, was still a JSON island in the middle of the page. We could've given them that feedback earlier, and it's unfortunate that we didn't. That's the whole point of an early review.

Peter: I agree it's unfortunate. Not sure what we can do about it now though.

Dan: [creates PR to the issue template](https://github.com/w3ctag/design-reviews/pull/844)

Rossen: Let's close it.

Would this result in an additional microsyntax that they're adding here? This new JSON format... I think this could be another principle they're going against.

Lea: I hear you on the principle. Not sure this qualifies.

Rossen and Lea: agree there is nothing micro about the syntax.

Peter: Also, I'm not sure it was as complex in the earlier review. Looking back at the earlier explainer.

Lea: how do these JSON islands interact with CSP?

Rossen: inherit?

Peter: they talk about CSP in the explainer.

Rossen: I'm trying to understand the headline whten this is launched, the big user benefits. I get the reduced payload benefit, which will most likely affect some of hte bigger properties out there.

Torgo: It's 2 or 3 picoseconds faster

Rossen: I get that. Less compute is less power, less power is less pollution.

Peter: will it not just cause more bandwidth use? I think there is also a cost to the end user.

Rossen: you're making my point. I don't know what this is giving me!

Rossen: [drafts a closing comment]

<blockquote>
Thank you for the continued persistance in working with us on this review. Based on all of the above feedback from our earlier breakout session and [early review concerns](#611), we're closing this for now.  
  
We note the continuation of our concerns that started in the early review. They weren't addressed, but were instead made more complicated by the added/extended syntax.
  
We think a new feature must pass a high bar of end-user benefit to compensate for that added developer complexity. We don't see enough benefit. Right now there is some discussion of the user need in the explainer, but given the web developer pull for this is not documented and additional stakeholders have not been supportive, we're unconvinced that this proposal passes this bar.
  
Again, thank you for working with TAG and please feel free to bring this back when it evolves significantly to address our concerns. 
</blockquote>

* Web of Things (WoT) Profile - Review Requested - @rhiaro, @hadleybeeman

[discussion about the WoT approach and the layers in the stack it touches]



#### Breakout C

### Issue Triage















































