# TAG Teleconference
#### 11 December 2024

---

## Agenda:

### Plenary Session - [2024-12-12](https://www.timeanddate.com/worldclock/converter.html?iso=20241212T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* EWP status
* Design Principles
* Societal Impacts
* Other f2f wrap-up topics
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996) - @jyasskin, @maxpassion
* [ Vision for W3C: request horizontal architectural review and wide TAG review](https://github.com/w3ctag/design-reviews/issues/1008) - @hober, @jyasskin, @rhiaro

* Releasing ballots?
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)



## Plenary Session

Present: Dan, Peter, Martin, Tristan, Max, Jeffrey, Amy, Matthew, Yves, 

Regrets: 


### EWP status

Dan: Will be [published today](https://lists.w3.org/Archives/Member/w3c-ac-members/2024OctDec/0072.html), blog post coming

### Design Principles

Jeffrey: Two PRs reviewed but not merged, and two that could use more review

Martin: I have a couple of trivial ones

Peter: merging

Martin: I looked at 536 and it looked okay but there are a bunch of people weighing in and it's not clear the comments are resolved. If you have can you tick them off?

Jeffrey: someone should double check with Anne and Jan Ivar ... but we can merge then follow up afterwards

Dan: let's get as many in as possible so we can move it to /TR and I can include them in the summary

Martin: I wouldn't hold on 536, we'll probably get that in within 24 hours. 501 looks very close, and then that's it. Others are blocked or draft.

Jeffrey: I can look at 501 tomorrow

Martin: Lea wrote it originally and there's some feedback to follow up on

Peter: publish as is or give it a few days?

Martin: 24 hours for 536 to settle. Don't block on 501.

*no objections*

### Societal Impacts

Dan: want to try to progress this with Amy, heads up. We've had positive feedback and think it could be useful. Want to get it in a better shape.

Amy: could meet next week, if anyone else wants to join please do

### Potential UA finding

Jeffrey: User Agents finding. PP includes a set of duties that don't really fit as privacy principle. What other findings would be useful? Definition of UA in infra is kind of the wrong place and is the only one we've got. We should find a place to define user agents that is the right place, a finding is plausible. We might take it to statement.

Martin: if it's good yeah. It's a difficult thing to define though

Jeffrey: I'm sure we need iteration and would love feedback from more people

Dan: I don't think we can totally define  ..

Jeffrey: did you look at the draft?

Dan: not yet

Jeffrey: look over it and then yay or nay

Peter: don't see anything problematic at this point, nothing to stop us putting it into a repo and getting more feedback

Martin: worth having a cover letter for it to contextualise it. That we have a bunch of things that skirt around the edges of a definition in infra and privacy principles, and trying to collect that together. We can update that over time as it gets more concrete.

Peter: if there are no objections by the end of the week in slack, go ahead.

Jeffrey: I'll draft the readme

### Commons analysis

Jeffrey: I wrote more and sent it to two academics greg bloom intro'd me to. Should I cc tag@?

### Work mode

Dan: I did a project board for the technical topics we discussed. So let’s try to start using that.

### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

Peter: doesn't look like feedback since Martin's last post

Martin: has been exchange on how much information leaks from a fenced frame under these conditions. Seems to be disagreement.

Peter: what's the resolution?

Jeffrey: seems like we're missing a use case that the TAG is happy with. If I understand there's no fundamental objection but missing a use case..

Martin: key problems we have with unpartitioned access also apply in the general case, but I may be wrong. I think you get to do the same sort of deceptive stuf except potentially worse because you don't have the same restriction on navigation out of them as the other cases. You get the k-anonymity but you don't get any other meaningful reduction. Simpler to exploit. I think it's true, is it a convincing argument? Need to think more about abuse scenarios.

Peter: follow up next week

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: there has been an update to the explainer

Yves: I can take a look again

Dan: have they addressed the issues we raised?

Peter: will put it on for next week

### [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk

Matthew: not any development since last time

Jeffrey: shipped in 121

Martin: we've provided feedback. Overtaken?

Matthew: will close as satisfied with concerns, invite to ping if something changes

### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

Jeffrey: Johan asked questions about this that we should answer. Breakout next week?

Peter: be good to get Lea involved

Matthew: would seem reasionable we don't have an opinion on UX until we get the results of the study. Sounds like they are wanting to do some actual evidence gathering so we'd want to see it wouldn't we?

Jeffrey: yeah and this is the early review so they'll file something else when they're ready to ship. Plausibly this could be esatisfied with conerns pending the UX, but worth figuring out the second half of the question

### [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996) - @jyasskin, @maxpassion

Jeffrey: posted proposed satisfied comment to the internal thread. Other things?

Max: we discussed about user experience, in the explainer they have listed some problems. They also describe some of the user experience although they didn't have a UX section, I think it answers our question. The API is used to remove the revoked credentials, otherwise the user may see some already revoked credentials and have some issues with consistency. Personally no other comments on this. Fine to close with satisfied. Maybe Dan should also look?

Martin: you raised a point about UX and having some sort of suggestion that they deal with it in their explainer. Perhaps you can draft up a note to add? Take [Jeffrey's note](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/61#issuecomment-2529922422) with a brief note about the UX stuff that will do the job?

Max: okay

### [ Vision for W3C: request horizontal architectural review and wide TAG review](https://github.com/w3ctag/design-reviews/issues/1008) - @hober, @jyasskin, @rhiaro

Jeffrey: a bunch of issues to iterate on. Question of publishers in the priority of constituencies. They have adjusted it.. Chris is going to draft text to make it a full ordering. They added publishers and removed web authors.. we should consider if we want to consider publishers.

Martin: I have draft text with a hyperlink to the design principles

Jeffrey: just to delegate to DP?

Martin: yes, much cleaner, I'll leave a comment

Jeffrey: sounds like they want to explicitly mention publishers to distinguish..

Martin: they should bring that to DP

Jeffrey: say this in issue 216 in their repo? I do think they're reasonable to say something about members. Point to priority and say members participate as whoever they are in the priority

Martin: that would be my preference. That may be the case for publishers as well.

Peter: a member can be representing any of the other categories or multiple. Probably intention was to state that members don't have any special place just by virtue of being members

Jeffrey: will figure out what to say as the TAG on the issue

Peter: Chris' last comment was taking a stab at reordering. I prefer Martin's take of just linking.

Jeffrey: I'll get something drafted tomorrow or someone else is welcome to.

> The TAG <!-- oh yeah, do we just say "TAG believes" like "W3C believes"?--> believes that the main source of conflict here is any attempt to reformulate this statement,
> which puts the AB and TAG into an unnecessary conflict
> in terms of who owns the priority of constituencies.
>
> It would be best if there is a single formulation of this important principle.
>
> If there is a place for publishers, we should discuss that in the context of the design principles.
>
> We also discussed the role of W3C members and feel that it would be OK for this document to clarify that "W3C member" has no inherent ordering, as below.
>
> Hence, we suggest:
>
>> Put users first: W3C prioritizes the interests of various stakeholders according to the [priority of constituencies](https://w3ctag.github.io/design-principles/#priority-of-constituencies).
>> W3C members are not listed in that ordering; they assume a position in the ordering according to the role they act in.

Jeffrey: we haven't heard back about any of the other issues. Chris H [proposed](https://github.com/w3c/AB-public/issues/215#issuecomment-2529827084) a positive vision for the web that we might consider, figure out if that would solve the problem

Martin: if we're going to develop a vision for the web it should be more substantial than four bullet points, a whole document.

Jeffrey: could start positive vision for web doc but don't have much content yet

Martin: Vision should not just be internally facing, which this is almost entirely. The future you'd like to see. Title is wrong.

### Releasing ballots?

Yves: it's the TAG's choice

Jeffrey: I feel like we can't decide for the current candidates. Most said they wanted ballots or didn't care. One said it felt like private data, and needs a use case.

Martin: the process doesn't require that and they didn't enter the election expecting it would be released, I don't think it's responsible to do anything now.

Jeffrey: the AB want the TAG to express an opinion

Martin: it's not a matter for current sitting members of TAG to decide if it's a procedural issue

Jeffrey: can we say this is in the AB's domain?

*nods*

Yves: TAG is not opposing it or mandating it, just a matter of asking the candidates if they agree

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
