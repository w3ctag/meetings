# TAG Minutes - Week of 16 June 2025

## Breakout A (Asia / Australia / West America) - [2025-06-17](https://www.timeanddate.com/worldclock/converter.html?iso=20250617T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Xiaocheng, Jeffrey, Marcos, Max, Martin

Regrets:

Scribe: Me

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

Jeffrey: Martin and the proponents have a considered disagreement.

Martin: They're overstating their case, and I'm probably overstating mine. I didn't find their arguments persuasive.


...

Jeffrey: Maybe we can ask them which other services they're working with, besides Google, to justify the need to reduce server complexity.

Martin: Previous attempts were at the TLS layer, which required a lot more infrastructure change.  Not sure if there are lessons that carry over.

Jeffrey: Maybe the conclusion is just that they need ot operate at the HTTP layer, but that doesn't decide between the proponents' and Martin's suggestion.

Martin: I realize that perhaps Google people, who have already shipped on both ends, would have some attachment to what they shipped and so might be biased.  Perhaps we can find someone else who operates a service to offer their insights into how this might work for them.

...: The proposed architecture would not be acceptable for Mozilla to ship (too high a complexity cost for the value) unless we could be convinced that there was a significant benefit for server operators.

Jeffrey: Let's ask that.

Martin: Don't want selection bias.

Jeffrey: Google people are supposed to gather feedback during origin trials.

Martin: But they won't get feedback on alternatives.

Jeffrey: Maybe this is something for the webappsec agenda and gather alternatives.

### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

Xiaocheng: Maybe we could add a new worker type.

Martin: Could work.

Jeffrey: Worried about a new worker type.  Would be dedicated, but live longer than the page.

Martin: Cross of two types.  Would have some properties like SW, but simpler.

Jeffrey: Recaptulates proposed feedback.  They did suggest a worklet.

Xiaocheng: Worklets live in the page context, not quite the same.  

Martin: Audio worklets do not.

Jeffrey: Worklets don't have an event loop, which this needs.

Martin: Xiaocheng's feedback seems right.

Jeffrey: Good to send.

### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Jeffrey: chair hat off
...: marcos, have you read the points about why this isn't long press?

Marcos: maaaaybe

Jeffrey: Looking for the semantic meaning of "hover".  Long press showed up because they needed a proposal.  They overdid it perhaps.  The original proposal was a context menu option that you selected.

Marcos: Interest is a bit more difficult as a thing. On the vision pro, if I look at an item, then it potentially looks like interest, similar to having that behavior, but it's a bit more vague, but it doesn't fit the patterns of other things.  That's why I ended up with long press.  "Interest" is a bit vague.  There is no interest concept that applies everywhere.  On a tablet, is a long press really showing interest?

Jeffrey: Samsung tablets with pens have a gesture where you hover the pen over the surface.

Marcos: iPads with pens also have the same sort of hover.

Jeffrey: Only works with pen.

Marcos: Hover is already covered then, with pointing devices.  This would conflict with that, given that it is supported in those cases.

Jeffrey: This would also work with keyboard input or eye tracking.

Marcos: If you tab to the thing, you can ...

Jeffrey: That requires separate code, whereas this is unified across input modality.

Marcos: This is the part that isn't clearly right.  It overgeneralizes the interaction model.  This is a larger discussion, with a11y.  If I tab around a page, that doesn't mean I'm interested, unless I do something specific.

Jeffrey: They have done some work on that.  We could ask them to validate some of these things with a11y people.

Marcos: Without it being wrapped in the interest part, but is what we have in the platform enough or do we need this extra event?

Jeffrey: You can polyfill, except perhaps for long press.

Marcos: If you can polyfill... I disagree iwth the other arguments in the explainer around complexity of implementation.  Sure implementation is hard, but I'd like to see this broken down.  Does hover fail?  Even if you need two events for the same thing.

Jeffrey: OpenUI is working on the higher-level stuff, but they are working to put the common patterns into the platform, so that you don't need to reimplement controls themselves (and get a11y wrong).

Xiaocheng: Should we suggest first step.  Can we split how to trigger the state from the specific user actions.  So rather than defining the default behavior on every platform - hard work - keyboard, touch screen, pens, VR, ... It is infeasible for them to make a complete proposal.  How about we define the interest event and default actions for that event.  The triggering is decided by the browsers.

Marcos: I would sstrongly disagree with that.  We might get there, but the thing that this improves is in identifying the problem.  e.g., Popover gives you the right context while you jump around and manages keyboard focus.  That's a clear solution to a real problem.  Prove that it is too hard to do something in particular, if we can't fix those, then we should end up with a solution.  They haven't made a case for why this is broken.  It's hard to implement, sure, but why is it broken?  From that agreement, we could potentially end up at interest.  We will get a bunch of new problems if we do this without understanding what this is fixing.  New things have significant costs, people will get excited, and we might realize that it creates new problems or doesn't address the problems we have.  Not convinced that we need it.  Sufficient primitives that we have had for some time.  Was of the view that this is already something we have.

Jeffrey: Point is that you can polyfill, but developers don't.  Are you looking for sites getting it wrong?

Marcos: Just want clear examples of where the current system falls apart and why.  if this is polyfillable, why are developers fouling things up? If we did that, this is super over-engineered, is that too much?

Jeffrey: It links elements.  Not sure if it does too much.

Marcos: I got the impression this was more complicated.  Let's get together with them, so that they can convince us of the problem.

Martin: Challenges Marcos on the point of explainer vs. high bandwidth discussions.

...

Xiaocheng: Can we split the proposal by platform or input device?  Can we make progress on hoverable interactions?  According to [their study](https://open-ui.org/components/interest-invokers.explainer/#survey-of-use-cases), triggering interest is very common across the web.  This might be low risk.

Jeffrey: Doing mouse-like triggering?

X: Y

Jeffrey: They would like to do keyboard, because it covers a lot of users and is easy.

Martin/Marcos: is it really?

Jeffrey: Tab to focus, keypress to show interest. https://open-ui.org/components/interest-invokers.explainer/#keyboard

Marcos: not sure how this addresses the a11y use case.  You tab around and then the thing that pops up is inaccessible.  Would be interested in using an iPad with hover.

Martin: What about loss of hover?  When the pen leaves proximity to move it.

Jeffrey: Maybe you don't lose hover if you don't hover something else.  By having this semantic thing, you can adjust for these differences.  And you might also get it to work on alternative interaction modes where things are different.
...: Time to consider asking the proponents to come in and have a conversation.  They are west coast.  Might want this group involved, plus Matthew.


Jeffrey: I'll find a plenary time to invite everyone.

### [design-principles#567: Add 'Choose the Appropriate WebIDL Construct for Data and Behavior'](https://github.com/w3ctag/design-principles/pull/567) - @marcoscaceres

Marcos: Updated today.

Martin: Take the .toJSON() paragraph into another PR and another principle.

Jeffrey: The section for .toJSON() could be a "don't forget to implement this set of methods"

Martin: And constructors.

Jeffrey: Temporal is interesting for constructors, where the constructors take the natural/simple form of the object, and .from() takes a bunch of other formats.

Martin: So conversion.

Marcos to do another iteration.

### [design-principles#501: Guidance about reflecting state in HTML attributes](https://github.com/w3ctag/design-principles/pull/501) - @LeaVerou, @martinthomson, @xiaochengh

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @matatk, @dandclark

Jeffrey: Probably ready to post; any objections?

Martin: Looked fine.

### [design-reviews#1051: Web Install API](https://github.com/w3ctag/design-reviews/issues/1051)

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson

Martin: Wrote this proposal two weeks back, would appreciate input: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/152#issuecomment-2933339292

Marcos: Why did they ask us instead of handling it in the WG?

Martin: Maybe it's done there?

Jeffrey: PR is still open.

Martin: TAG review exists to get feedback.

Marcos: If it affects Credential Management might be worth reviewing?

Jeffrey: Martin's feedback was important, especially if the WG is done with this. I think Martin's comment is ready to post.


### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman


## Breakout B (America / Europe) - [2025-06-18](https://www.timeanddate.com/worldclock/converter.html?iso=20250618T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Yves, Jeffrey, Lola, Christian, Dan, Serena, Hadley

Regrets: Matthew

Scribe: Serena

### Brief discussion on chairing

- No consensus yet, concern was the elected person would only serve for a few months

### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @torgo, @lolaodelola

torgo: Last time, did we challenge them on the use cases in some way?

Jeffrey: They replied with updated use cases. Now waiting on closing comment

torgo: On it! Will get this done today/tomorrow, will be out next week

Lola: On my todo list is filing a issue, will do this week, will be out next two weeks

### [explainer-explainer#23: Auto-publish the explainer explainer to TR space.](https://github.com/w3ctag/explainer-explainer/pull/23) - @jyasskin

- Yves reviewing
- Jeffrey has addressed the comments, waiting on double checking

### [explainer-explainer#25: Say that explainer contents should move into specifications.](https://github.com/w3ctag/explainer-explainer/pull/25) - @jyasskin, @torgo, @matatk

torgo: suggested "may" instead of "should" move into specifications. I like encouraging people to moce stuff into the spec, espeically if that mean that they're going to keep it up to date. However, I also feel like some people may want to include info in the explainer.

... We should encourage people to keep the explainer up to date, and if they're going to move stuff from the explain into the spec, then remove it from the explain so that it doesn't get out of sync. Better to be clearer than more concise in this case, we want people to understand what we want them to do

Jeffrey: Alice's wording isn't quite right because it opens the possibility of having duplicate text in the explainer and spec. Will do another pass to incorporate her ideas. Is there consensus that this is the right direction? To say that people can either move stuff into the spec or leace it in the explainer but we want to reinforce the idea that they both should be kept up to date

Lola: I think it's good but walk us through the process of brand new spec vs revision? whats the process

Jeffrey: The assumption is for new features, maybe changes to existing featuers, alkthough that's fuzzier if you write a separate explainer for a new feature

torgo: we've had both. New explainers and amending exisiting explainers. We could open the door to either approach.

Jeffrey: we could, but maybe we shouldn't. When people add a new feature to an existing explainer, we often get side tracked critisizing older stuff

torgo: I was thinking of the case when they add a new section and deeplink to that section. But your point stands because it's not obvious what has changed since the last version. You have to go to a diff. It could also point to a PR or a commit? It might be better to say, **if you're adding a feature to an exisiting spec, write a new mini explainer that links to the previous one**? Do we need a new issue for this?

Jeffrey: yes

torgo: I can do that: https://github.com/w3ctag/explainer-explainer/issues/27

### [design-reviews#1102: Rethink the TAG's review intake process.](https://github.com/w3ctag/design-reviews/pull/1102) - @jyasskin

Jeffrey: This is a big change. Martin asked about the arrangement of the forms, that I'm only half-using the github form areas. Because the form migration leads to a lot of subheadings that feel like they disrupt acctually reading the review request. _[shows demo](https://github.com/jyasskin/test-design-reviews/issues/7)_

Lola: What's the difference in issue #13 between -- what is an introduction to the feature aimed at ___ audiences?

Jeffrey: That's mean to be the explainers' introduction, but if you moved your explainer into the spec, you could link to the spec's introduction/ But since you aren't sure, I'll need to add more explanaation

torgo: 13 looks better to me because it's not everyhting. In 7 it's just kind of presented at the same level and it's not very readable. But it's my aesthetic preference

Jeffrey: unless I hear that people like the heading version, I'll stick with what I proposed

Lola: I prefer #13

Jeffrey: The rest of the changes:

- Overall added 2 new template types, refactored everything so that there's one script that =generates all 4. Easier to rever what's different between them and keep things that are supposed to be the same.
- intake.yaml is that generation script

torgo: what are the categories

jeffrey: renamed early design review to incubation reivew. Soec review got split into working roup that has made an ew spec, and a working group that has made a revision of a spec, both of which we assume are going through horizontal review and se accessibility interationalization are getting asked on the 

torgo: do you make it clear to the person choosing the templates, that it's about horizontal review

jeffrey: that we assume the working grouyp is doing horizontal review?

torgo: concern that i'm a spec author, I'm in a working group working on something not to do with horiziontal review, I'm asking for TAG review with full knowledge of the editor. Plenty of reasons why you might want to ask for a TAG review during the development before horizontal review. if we point them to the template we should be very clear that we only want them to use those other ones. 

jeffrey: I'm undecided about which one I prefer. I think in precious spec reviews we weren't sure if the working group endorsed it. having the distinction here might help even if the working group hasn't asked for horizontal review. Not super clear in the template. It could be ok to leave it ambiguous for now and see what bugs pop up

torgo: I want to make it clear which template they're supposed to use

jeffrey: it's pretty clear if a working group endorsed asking the TAG, then you use this

torgo: that's an argument for not mentioning horizontal review in the intake, because it's possible that the working group had a meeting and said, we should ask for a TAG review on this. Whether or not it's horizontal review is irrelevant,question is has the group endorsed

Lola: If you're considering shipping a feature that hasn't had WG wide review, please consider one. Are there any other consequeces if working group hasn't taking it to TAG review?

Jeffrey: There's 3 states you could be in, only two options on the form. Browser feature that hasn't gotten into a WG, WG doesn't endorse it, and WG endorses but has't gotten to the wide reviews stage. We are discussing where the middle one goes

torgo: I think it should be (sorry I missed this part)

--

torgo: any other thoughts?

Christian: in general this all seems fine

torgo: want to make sure we're capturing 

Yves: There was a comment from Martin about the security and privacy questionaire , 

Christian: same

torgo: having a more concise version that people can read through

Yves: Especially now at the time there was a lack of securiy and privacy review that was filled bu creating working groups and having people doing a great job at that, So it's something we might even want to ditch in the future, because it's covered by other people

torgo: we should def. refactor it. Considering the publication of the privacy principles

jeffrey: I'd like to do that in a separate PR, because that's another change. Does the rest look good, ready to merge?

torgo: something wonky in the bulleted list under links, as far as #13 goes

Hadley: Re: 4 tracks: how do we account for working groups bringing a technical question that they can't solve themselves

Jeffrey: we still have the other two templates: Dispute resolution and question (?)


### [design-principles#575: Add Criteria for Design Principles to README](https://github.com/w3ctag/design-principles/pull/575) - @csarven

torgo: will try and catch up with Sarven

### [IP Protection in Incognito](https://github.com/w3ctag/design-reviews/issues/1083) - @lolaodelola, @hadleybeeman

Hadley: this is limited to one implementer

Lola: unsure what the next step is. This is very early, is the next step to say this is fine/not fine, are we trying to encourage cross platform adoption?

hadley: Given it's limited to one implementer, it's not unreasonable to decline to review it

Jeffrey: There's also https://github.com/w3ctag/design-reviews/issues/1114 where there is a draft comment to decline to review, can reference that

torgo: Wanted to not that we have a doc in 2019 about TAG observations on private browsing modes. Doc was written because specs were starting to be written with notes saying implementers started mentioning it, but there's no specifications on private mode. This document was written to roll that up, or at least just observe what was happening. Is a think other specs can point to when they say "private mode". Unsure how successful it has been, don't know if people have been linking to it. Is there anything that we should be thinking about in revising this, maybe new doc, or an update, maybe pushing on this more to say there ought to be a spec on private modes. - https://www.w3.org/2001/tag/doc/private-browsing-modes/

Christian: That's our feedback for script blocking issue -- suggest we decline this -- basically a single engine feature, encourgae them to create a specification write a a document so that it can be implemendted across engines, and this is the same feedback for IP protection

torgo: let's add a link to our document to that comment, to reinforce that we've done some thinking about this already

Lola: Mike's last message talks about how it's still very early days for this thing, vote to decline similar to Hadley and Christian, becuase they are acknowledging it's not ready for our review. Happy to use Christian's comment

Christian: everything is missing, e.g. security and privacy review, so it's not ready to review

Hadley: Fine with declinging it. Am a little concerned with Christian's suggest that we turn the challenge back to them for standardisation. IIRC in 2019 the problem was there was siginifant divergence between different browsers. Can't turn to just one specific browser. Issue is we need to bring them all together

torgo: agreed

Jeffrey: there's 2 separate questions here. There's standardising private browsing mode. But there's also standardising IP protection and script blocking that Chrome only wants to turn on in private browsing mode

torgo: If you look at the doc that Lucas wrote, it tries to make the point that there are certain things in common to private browsing mode, question should be what web features from a web developement standpoint, web devs should be thinking about how things behave in private mode, because all these browsers have a private mode. I think it's a valuable thing for people to think about. It's valuable to have it on the books. maybe we need to strengthen it in some way. I take Jeffrey's point that the reviews aren't about this. but maybe something to push to privacy WG

Jeffrey: I think there's a caution here for these features, also [in the design principles](https://www.w3.org/TR/design-principles/#do-not-expose-use-of-private-browsing-mode). Doing something different in incognito increases risk that websites will identify users in incognito mode and increases risk that things will break in these modes. Chrome is aware if these concerns, but it's worth reiterating them. We should ask the privacy WG/CG to think about what parts of private mode can be standardised. But also I think the request for the IP protection and script blocking folks is the try and standardise those features whether or not they're in private borwsing mode or other modes

lola: I can write closing comment for IP

Christian: will take other one

torgo: Design principle 2.10 is basically a shorter version of this finding. Funny that we don't link to this finding in that principle. Maybe we should just point to the design principle instead of this finding. It's the living principle we are asking people to adhere to.  https://www.w3.org/TR/design-principles/#private-browsing-mode

*we agree to add both*

### [explainer-explainer#19: Explainers are an anti-pattern](https://github.com/w3ctag/explainer-explainer/issues/19) - @jyasskin, @torgo

torgo: can we close this?

Jeffrey: not yet, we need to merge the two PRs. Afterwards we should close it

Lola: It seems the issue isn't so much people writing or not writing explainers well, it's about where the information _is_. The Docs CG WG we discussed this in last two meetings. Explainers are helpful for technical writers, and in yesterday's meeting were toying with idea of having an explainer writing sessino on TPAC, but TAG owns this work. Don't want to encroach on TAG if they want to keep this work. Issue Eric and I bring up is that if we move explainer into the spec in runs into using technical spec speak. 

torgo: Maybe we should move the explainer explainer to the Docs CG

Jeffrey: once the 2 PRs are landed, we should run the result by the Docs CG to see if they're comfortable with it in general

torgo: let's put this on the backburner for now

Request by CL:

### [design-reviews#1114: Script Blocking (in Incognito mode)](https://github.com/w3ctag/design-reviews/issues/1114) - @christianliebel

*we resolved above*

### [design-reviews#1110: windowAudio for getDisplayMedia](https://github.com/w3ctag/design-reviews/issues/1110) - @christianliebel

Christian: We want to ask questions back to the proponents, fine for me but Martin thinks the naming isn't goof. We will ask questions, wait for responses

### [design-reviews#1109: restrictOwnAudio for getDisplayMedia](https://github.com/w3ctag/design-reviews/issues/1109) - @christianliebel

Christian: Similar thing, Web RTC features. Here we are statisfied. Fine for Martin and I. We can mark as satisfied if it's ok with everyone else. It excludes audio from the same tab being shared back to the user.

### [design-reviews#1101: env(preferred-text-scale)](https://github.com/w3ctag/design-reviews/issues/1101) - @christianliebel, @xiaochengh

Christian: Jeffrey and I have looked here, we would make as satisfied with concerns regarding accessibility. 

torgo: Don't suggest to keep this open but punt to APA?

Christian: it is on the agenda for tomorrow, if everyone is happen then you could just post a comment

torgo: If we want to do it this week, Matthew has already given regrets for this week so we should just make a call

Jeffrey: I think this is ready to post and ready to close. The feature is an improvement even from an accessibility standard, the concern is that there's maybe a better way to do all od this that needs to be designed. But it's not this feature, there's no tweaks to this feature to accomplish what they need to actually do. This is fine. Given the big fix won't happen soon this is a good short term fix

torgo: I think we should close this in the interest of moving ahead

#### Hong Kong meetup

Lola: are there updates on budget?

Jeffrey: There's no update on funding, questino came up briefly during AC meeting uesterday. Still need to write email to Seth. W3C budgeting is halfway done

torgo: W3C has Past Submitter Status, W3C feeds into the more traditional international standards ecosystem like ISO standards. Also feeds into EU stuff

## Breakout C (Europe / Asia / Australia) - [2025-06-19](https://www.timeanddate.com/worldclock/converter.html?iso=20250619T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Yoav, Xiaocheng, Lola, Yves, Marcos, Hadley, Martin, Max

Regrets: Christian, Matthew, Dan

Scribe: Martin, Hadley

### [design-reviews#1097: Browser Bound Keys for Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/1097) - @torgo, @marcoscaceres

Marcos: Haven't looked at this one.  Not familiar with the device-bound stuff.  Will need to learn more about this feature.

Hadley: We'll need to replace Dan on this one.

Yoav: Could help out.

### [design-reviews#1101: env(preferred-text-scale)](https://github.com/w3ctag/design-reviews/issues/1101) - @christianliebel, @xiaochengh

Xiaocheng: Christian already closed this out.  Happy with the outcome.

### [design-reviews#878: confidence reporting for PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878)

Yoav: Saw comments from Martin and a bit surprised by them.  It would be good to hash out those concerns.  I was involved in guiding the folks that championed this through the privacy principles. We were explicitly going with a fuzzy/DP approach in order to avoid exposing information about the user and their browser/environment.

... At a high level, this allows browsers to tell developers about why the site was slow.  Either because the browser was under stress or it was busy doing a lot of other things, such as might happen at startup.  This enables aggregated results to be adjusted at scale to ignore those cases, from those browsers.  The goal is to avoid revealing whether a particular user was under stress or not.  This allows for individual users.  I thought that this was in line with privacy principles; we didn't want to reveal new auxiliary information.  Was surprised by the comment; if we take that to the extreme, we are saying that performance measurements are a fingerprinting vector, everything related to timers is.  Anything could be.

Martin: I was looking at this from an information ?? perspective. The addition is fine. In the greater view, there is a problem here. I don't know that that means we don't do the feature, just that we acknolwedge there is exposure here. I don't know if we can even block performance monitoring without extreme isolation. There are designs for systems that operate without clocks, but if you have a web connection, that's not good. The realisation that this isn't as big a problem as at seems to be -- that's what caused me to make these comments. I don't think it affects this API. The question is: what do we do on the larger scale to make measurements more useful and more private?

Yoav: I think that's fair, but -- If we are again going by the Privacy Principles, there is some auxiliary data we are exposing related to performance, but to a large extent, it's already exposed through functional APIs, that no one is intending to remove and the performance APIs make the collection of this data either easier or cheaper for users. We know that people who care about these things or malicious folks who care about the fingerprinting aspects -- I'm not sure I'm fully buying the fingerprinting aspects -- but they can all gather this information outside of these APIs. So we made sure through differential privacy, it's not exposing anything about a specific user. If you were trying to guess, 50% of your assumptions would be incorrect in either direction.

On the broader topic of fingerprinting, if we assume that people who are slow on site A will also be slow on site B, we can break that down into network connection, the download time...

Martin: there are multiple metrics there. End to end latency from a network perspective, from a CPU perspective, and download speeds. And those are useful info for people using websites. Recognising that someone who is slow on one website is slow on another -- that's useful info.

This one has an unbound sensistivity, so adding info is not much good.

Yoav: for some of these things, we could go the route of aggregated reporting across users. For very specific things, for things where we know we can avoid the exposure through functional APIs. Here, they are all exposed.

Martin: the best I think we have there is to add a little noise, but that noise doesn't give us any value.

Yves: noise can only save some time

Martin: Having thought about this, I think the only thing we can do here is acknowledge that this is a fingerprinting risk. But there is too much compatibility risk to disable those. This one escaped, and anyone looking to build a browser that's more private may be interested in the ways. But it's not going to be perfect.

Yoav: not convinced that any of this can be mitigated in functional browser.  Maybe with full application integrity, you could do some preloading and processing, but that's not the web.  It might use web tech, but it's not the web.  

Lola: My question has been answered already, I think.  From what I'm hearing, it sounds like this is something that we want to weigh the risk of.  The data that is exposed as a fingerprinting vector vs. the use to developers.  It sounds like there is a risk, but it's OK if we add noise.

Yoav: the risk is inherent to the web platform: timers, network requests, and events.  We have to accept that risk.  If all other fingerprinting bits are solved, this is not what will expose identity.  I don't know how many bits this is in practice.  For the 10% slowest users, this might have correlation.  We should definitely mention this in the various APIs' privacy and security considerations, but I don't think this is something we can solve without fundamental changes to how websites work.

Hadley: Sounds like we are converging on something.  Can someone jump in and start drafting some text that we can agree on?

Martin: I think we're better aligned than it seemed. I think Yoav and I are aligned. We cannot fix this problem, not worth trying. But acknolwedging the fingerprinting risk is a worthwhile exercise. 

Separately, I'm comfortable with this API. The value of epsilon is flexible ,no?

Yoav: I think so, they can increase or decrease the value of this... true info vs false info... by default, the value in Chromium is 50/50

Martin: which is a pretty low epsilon. I'm comfortable with that. If we can agree with an epsilon across browsers, that's helpful.

Yoav: if I remember correctly, the API reports the epsilon used. So you can de-bias the data. 

Martin: It's just annoying because you need to de-bias on a per-browser/per-epsilon basis.

Hadley: [some discussion on process and issues and stuff]

Yves: resolution: satisfied with concerns?

Yoav and Martin: No, this API is good! 

[Yoav to draft text for a comment, to agree with Martin and Lola. Then they will close the issue, resolution: satisfied]


### [design-reviews#1079: Page-Embedded Permission Controls](https://github.com/w3ctag/design-reviews/issues/1079) - @martinthomson, @marcoscaceres, @matatk, @heisenburger

Martin: I looked at this from a Mozilla perspective... we thought the single purpose try-to-solve-everything-with-one-element is not going to work. The variety of use cases was diverse enough that we'd like to see permission-specific elements for each thing. A camera element, a microphone element, etc, but not repeat the mistake we made with ???.

Very enthusiastic about the idea, but it's a big project. Happy with what the google team have done around clickjacking etc, but overall this is a good project. Been running for a while now, I first saw this at TPAC in Seville. 

Marcos: Similar to Mozilla on the WebKit side.  We've looked at this long and hard ... because the motivation was following what Apple did with the geolocation button in some platform version \[?]. With that design, the constraints are so limiting that it kinda becomes useless, which is what we concluded.  The mitigations were good, but it was very complicated and kludgy that it added a lot of complexity.  The thing that really took this down was that we have N number of APIs that need permission, we would need to move things.  Either all new APIs use this model, but we can never get rid of existing APIs.  You always need the original API.  If you have the API, the developers will use the API anyway.  So you are still back.  If it is annoying to include this in the page, without being able to style it, you will use the API.  Maybe this works for new APIs, or we move all APIs to use this, which could be a thing.  Finally, this seemed to be a rehash of what we had with navigator.permissions; we got rid of that because it didn't align with the way the APIs are used.  This could be another means of asking for permission, which we didn't feel was a great thing.

Martin: Yeah, we talked through a bunch of this with the team at google, and we agreed with your point Marcos with permission.request. We don't want to build an API with the grant-permissions disconnected from the use. We're enthusiastic about this API because we can closely connect it to the use in a number of cases. There is no time of grant or time of use grant for notifications because you always have to ask ahead of time. But for cameras and microphones, you could imagine an in-page element that you click on, which activates the permission request. We can let the website authors style that however they choose: icon, text, colors, etc. The only thing that matters is the thing that pops up to ask permission. Giving site authors control of the placement of that, without all the controls, seems good to us at Mozilla. If you click the button again, it face mutes. You can turn it on and off in a way the browser understands and is in control of. Don't need JS, the default browser behaviour will just work.  We thought through the concerns you had, and thought if we do this well, there is enough upside to this. But it has to be done well. 

Otherwise, we share your concerns. The line of death... that's a red herring.

Marcos: the other thing that we concluded was that this was a self-created problem that chrome created for themselves, because Safari... Chrome are doing the door hanger. If you are doing a model request, then people wouldn't miss the permission... The incentives were "people were not understanding that the door hanger up here relates to the button down here", but when you do it in safari, it does it in the middle of the window

Martin: we disagree for good reasons. I think the UX philosophy that we're using is not to allow sites to force people to decide. We decided that in 2008 (before my time). 

Marcos: right, and that is following Apple platform conventions. On macOS and ios, that is consistent on the webkit side. Firefox made a different decision,

That's not to say that we don't have to do the same affordances... but there is no way like in firefox where you can dismiss it without having made an explicit choice. 

Martin: I do think that problem of people noticing the permissions is solved neatly by this one. But that doesn't foreclose on the choice of a modal prompt. Or maybe, the site would be happy with the chosen placement. That's up to you to work out. There are a lot of competing concerns here.

Marcos: there is some overlap in agreement, but there are difficult problems to overcome here. If we all had concensus that this is the way to go for new APIs, that would give us a path forward. I'm still not convinced that this is the right solution.

Martin: from our [Mozilla's] perspective, we are going to invest time into working out the camera and microphone pieces more fully. I wouldn't expect you to do more... It will be a ways off before we conclude what we think is the right design for just those two pieces.

Marcos: and there is accompanying APIs for those.

Martin: and we can't take them away. 

Marcos: even if chrome and gecko end up supporting the pepC thing, you still ...

Hadley: is it too early for the TAG to review? Do we have consensus on anything to say?

Martin: we can comment on the idea that you can do a single element to cover everything. We have established design principles here. 

The other thing: we can point out Marcos's point of the relative value of adding yet another way to do something on the platform. 

Hadley: the second one weighs in to developer complexity

Martin: yes, but then you don't need to build the UX, you just put the element on the page. Could be less complexity, in the end.

Problems that need to be solved... if you have a camera button and a microphone button, and I unmute one, does it make sense to ask about the other? 

### [web-no-papers#3: Add some text about email addresses](https://github.com/w3ctag/web-no-papers/pull/3) - @martinthomson

Martin: I'd hoped to discuss with Torgo

Marcos: there has been a lot of work with privacy... Should we wait for those? And now that Apple has announced at WWDC that some of the privacy aspects of the DC APIs as implemented by Apple's platforms. It's interesting to see what Google has done vs our implementation, and how we've addressed some of the issues with the APIs... Where the TAG may weigh in... Mozilla hasn't done an API. Google has decided to do a thing where anyone can ask for credentials, any native app can participate even if they implement a crappy insecure credential request protocol... Apple have said "no, we're not allowing anything unless standardised and very well sanctioned". It will be interesting to see that all play out.

We can add value to say on the web, maybe Google can recheck their assumptions. They may be looking at that. 

interesting discussions are happening now, because now we have different, distinct approaches. Fascinating to think about how we bring them together.

Yves: I looked at Martin's PR before the meeting. the text on phone nunbers is too soft, they are almost-unique identifiers, like email addresses, more unique than IP addresses. Recommending against using them in the text would be better.

Martin: you're right. Phone numbers are the worst, IP addresses, then email addresses (sometimes swapped for second)

Hadley: let's move this to A next week. (In fact, it was covered in the plenary.)

### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres

Marcos: \[reviews progress on this, agrees to start on a draft comment]

## Plenary Session - [2025-06-19](https://www.timeanddate.com/worldclock/converter.html?iso=20250619T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Dan, Xiaocheng, Yves, Martin, Lola, Hadley, Matthew, Marcos

Regrets: 

Scribe: 

### accessibility questionnaire - @matatk

Torgo: Where do we stand?

Matt: We've got a proposed version. We've got a questionaire to discover if people need extended accessibility review. We've been thinking to deploy that in the \[something] repo. It's more visible to them and they can use tracker labels to surface with other groups.

Using an HTML form makes it easier for people to fill in. We have a form of the TAG's questionaire that automatically makes a GH issue, we have the same for the APA's fast checklist. I've arranged for Ananya to have repo access, we can then test the form from accessibility perspective, once that's done we'll merge if everyone is happy.

Torgo: It opens an issue in their repo?

Matt: Yes

Torgo: Who is shown as opening the issue, the person filling out the form?

Matt: Yes

Torgo: It references the design review they're filling out?

Matt: Not at the moment, my idea was that they'd link the form in the design review

Torgo: That's fine

Matt: Nothing has changed here, the content hasn't changed. However I've been looking at horizontal reviews across groups, most groups have short and long questionaires so there are things I think we could do to make it easier for end users. We have two questionaires -- TAG & APA -- which aren't connected, we should connect them as some questions can be used. This would help with consistency.

The problem with the current TAG approach has issues going into repos that are unmannaged.

Torgo: This is a great approach. In the repsonse, if you say "yes" to many of these things, it should nudge to look at the APA checklist

Matt: It sort of does: "you should seek advice from relevant domain experts", I'd like that to more explicitly link to APA as we can catch things earlier. APA doesn't always have expertise applicable to design reviews, but still helpful to get involved to point people in the right direction much earlier.

We'd have to do this in a way that's sensitive to the fact that this isn't...

Xiaocheng: What does this mean for people asking for a design review

Matt: This was developed when Sangwhan was in the TAG. I don't have the full answer on this but the way I understand it is, completing the questionaire with "no" doesn't mean you've covered accessibility. Looking at the short checklist won't give you full details. The short checklist is to assess if the design needs immediate accessibility review or can it wait. Low level APIs with no user interface usually don't need accessibility reviews.

Torgo: We wanted something that could nudge people to think about accessibility because they were coming to us early with ideas. We wanted to be able to do it in such a way that didn't give the impression that the TAG was giving a review, rather just to get people thinking about accessibility earlier in the spec authoring process.

Xiaocheng: I'm trying to imagine my user experience when asking for design revieiw. Is this used for early or later reviews?

Matt: I think it's intended for any request to the TAG, some will be earlier than others. This will be useful for APA reviews too.

Xiaocheng: So if I use this, it doesn't mean I don't need to fill out the accessibility self review.

Matt: We need to clear up terminology. Looking at process for different groups, it's unclear where "self-review" comes from. Some people would refer to both as "self-review". We should harmonise the term in the way that security and privacy does. "sefl-review" has many meanings. If it's an early design review from TAG and they say no to all questions in this questionaire, they probably don't need additional review. If everything is working, fine, if not this will surface issues.

Torgo: We should avoid saying "if you select no, you don't need additional accessibility", it should be the other way around. We should be encouraging more thinking rather than less thinking. I think you've got an action item which is to circulate the test URL then a PR on the design review issue templates. There's still an open discussion around issue templates but once changes land, we can incorporate this.

Matt: Will do tomorrow or monday.

### digital credentials finding - @torgo, @martinthomson

Torgo: We changed the title to "Preventing Abuse for Digital Identities".

Hadley: We talked about PR 3 in C and I thought I pasted it to the agenda but didn't, that'd be helpful for this conversation. [web-no-papers#3: Add some text about email addresses](https://github.com/w3ctag/web-no-papers/pull/3)

Torgo: Ok

Marcos: We should change the shortname. I had a chance to read it, I don't hate it. Everything there are well known, valid concerns. A lot of them haven't been addressed by policy or govenernment/regulatory systems. It makes enough of a case without need for adding in phone numbers and email part, there's enough there to give jolt about potential abuses about this technology.

Martin: You made a point about phoning home when we spoke about it earlier.

\[discussion about ISO standard ISO18013-5]

Marcos: we should add something that talks about the phone-home case.

Martin: there should be no interactions with the issuer when you present a credential... I think we've missed that so far.

As webkit, we aren't implementing openID for VP because it involves phoning home.

Re revocation, especially checking with the issuer... 

Torgo: let's focus on what should be in the finding

Marcos: this is important because of the way the architecture works. It's not the user agent that handles this stuff. when you make a request into the system, with the ISO format, we split it. We take hte dnagerous stuff and find the presentation stuff and certificate and send them to the OS, which takes over. The UA doesn't do much.  The user then consents to the wallet they want to use, and then the site for example wants to know my age, we hand that the wallet that finds the age from the drivers license. That's webkit, and I believe it's the same on the Chrome side. 

\[shows example]

Date and time of issuance is precise (down to the second).  Postal codes can be (ZIP+4, UK postal codes).  But there is no phone number or email.

Torgo: is there a PR you could raise on the document to include this advice?

Marcos: the problem is these things are implemented by wallets, which are serving as user agents themselves, they are supposed to show the consent sheet. 

Martin: the user agents on the web, we can consider them part of our moral turf. And we can say things about what they should/shouldn't be doing, and we can refuse to implement parts of the spec.

Torgo: I would enlalrge that footprint to include the interface between UA and the wallet. 

Martin: that feature isn't implemented in the API, it's the wallet that would implement that. the wallet could take the parts of the request that are benign, but not implement a URL for example.

Torgo: This is like EME, where the CDM was a black box that could do anything.  The browser had no real control.  Much like the wallet here.  Still worthwhile having a cautionary note on this and challenging the group to consider these abuse cases as being in scope for the work they do.  Consider how they integrate and mitigate against these.

Marcos: the working group is doing this by creating a registry, and if you aren't in the registry, you can't participate. There are criteria to be on the registry

Martin: but the criteria aren't written down, are they?

Torgo: We should put stuff in our specs that empowers people to say that whatever protocol isn't good enough.  Want to get to "done" on this document, so that we can issue the finding.

Martin: I'll take email stuff out and focus on other use cases. We should release at end of the month

Torgo: Will be talking informally with people at the open wallet foundation event at the start of July. 



### [design-reviews#1080: [wg/payments] Web Payments Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1080) - @marcoscaceres, @maxpassion

Torgo: Marcos, this is you.

Marcos: I wrote a bunch of stuff

Torgo: Martin said looks good, Jeffrey had some points. Marcos do you want to add anything?

Marcos: I need to catch up

Torgo: What you wrote is great, Jeffery and Martin had suggestions that we could fold in.

Marcos: Yeah. I'm just looking at Martin's comment. It's complicated because there's the working group and interest group, and this feels like an interest group thing.

Martin: The issue seemed like it was hanging, I don't know about Jeffery's comments

Marcos: It looks like we need a bit of redrafting here. 

Torgo: I'm just looking at Jeffery's points too.

Marcos: I can try to address all this tomorrow and get something out

Torgo: I think you should work on combining the comments, and if you don't feel like you need to ask Jeffery anything, feel free to post and close the issue. The basic stuff you've written, we're happy with.

Marcos: Sounds good



### An Update on Age-Verification Workshop @martinthomson

Martin: the IAB have questions. Hadley at some point we'll be able to meet with them. If anyone else would like to join, let me know. My position is that we do the workshop without them.

Torgo: Which IAB?

Martin: Internet Architecture

Torgo: Why are they not interested?

Martin: The only thing I've heard so far is that they want certain people to be on the program comittee. But I don't think that's necessary. Some people could leverage their employer to gain access, but there's a process.

The message to them would largely be "no" if they want major changes but I expect the changes they want to be minor. I hope to be able to announce that next week.


### TPAC Explainer Workshop w/ Web Docs CG

Lola: the web docs cg want to do an explainer workshop at TPAC - we wanted to make sure that's OK with this group because TAG owns the explainer explainer.

Martin: I think we have a lot of people who have a stake in explainers - so please go ahead - the docs people are a stakeholder so we value their work on making explainers better.

Hadley: seconded - thanks for doing this - thanks for asking the TAG... Once you have it scheduled please ask if other TAG members want to host it or participate, etc... Equally that doesn't mean you need to change anything as a result.

Matthew: I or one of my team would like to attend, possibly help.  Breakout?  \[yes]

Lola: There is a session on documentation in general, plus this.  That topic is still up in the air.  Not sure whether this is how to write a good explainer, or whether it is how to integrate explainer text in specs.  Either way, we want to hold a session on explainers.

Torgo: We're not talking about getting rid of explainers.  It's more nuanced, explaining \[heh] when to use them, for what, when to move text, how to maintain things better.  This is compatible with a session on how to write a good explainer.
...The second is that turning this into a spec was intended to get things out of the mode where people assume that explainers are only for the TAG, but to instead have them useful for more than that (wide review for starters)

Marcos: An example this week, was people quoting explainers as if it were the spec.  This horrified me. That needs to be captured somewhere.  The explainer is not the spec.  Someone was doing something because it was not in the explainer (it was in the spec).  Horrifying.

Torgo: Explainer anti-pattern, needs to be quashed.

Conclusion: Lola should be empowered.

### Breakout Rollup

No time.

#### A
#### B
#### C


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


## Backlog
* [design-reviews#1109: restrictOwnAudio for getDisplayMedia](https://github.com/w3ctag/design-reviews/issues/1109) - @christianliebel
* [design-reviews#1110: windowAudio for getDisplayMedia](https://github.com/w3ctag/design-reviews/issues/1110) - @christianliebel
* [design-reviews#1105: ScrollIntoViewOptions container attribute](https://github.com/w3ctag/design-reviews/issues/1105) - @zcorpan, @dandclark
* [design-reviews#878: confidence reporting for PerformanceNavigationTiming](https://github.com/w3ctag/design-reviews/issues/878) - @jyasskin, @yoavweiss
* [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @torgo, @matatk
* [design-reviews#1050: Permissions Policy reports for iframes](https://github.com/w3ctag/design-reviews/issues/1050) - @torgo, @yoavweiss, @hadleybeeman
* [design-reviews#945: FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @torgo, @hadleybeeman
* [design-reviews#974: FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974) - @torgo, @hadleybeeman
* [design-reviews#935: FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @torgo, @hadleybeeman
* [design-reviews#803: FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @torgo, @hadleybeeman
* [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres
* [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres
* [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @torgo, @ylafon
* [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh
* [design-reviews#992: FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @martinthomson, @torgo, @hadleybeeman


