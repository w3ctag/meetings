# TAG Minutes — Week of 5 January 2026

## Atlantic Breakout (America / Europe) - [2026-01-05](https://www.timeanddate.com/worldclock/converter.html?iso=20260105T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Matthew, Yves, Christian

Regrets: Lola

Scribe: Jeffrey

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) - @csarven, @lolaodelola

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @csarven

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel

Christian: We talked about this just before the holidays. Hadley said the document is malformed and not really an explainer. 2 alternative proposals. We said we'd check it, and if it was still unclear, we'd ask for clarification. Still unclear today. We should ask for clarification, and for them to fix the explainer. They should also mention multi-stakeholder support.

Matthew: Please do that.

### [design-reviews#1179: [wg/vc] Verifiable Credentials Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1179) ([Github](https://github.com/w3ctag/design-reviews/issues/1179)) - @csarven

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Matthew: Jeffrey proposed edits, and I'll do that and post it. I'll put the edited version in private-brainstorming.

Jeffrey: I'll 👍🏻 that.

### [design-reviews#997: [HTML] Canvas place element](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/997) ([Github](https://github.com/w3ctag/design-reviews/issues/997)) - @matatk, @xiaochengh (pending for at least 6 months)

Matthew: This is part of html-in-canvas (https://github.com/WICG/html-in-canvas). It's been pending for some time because we asked them for information that never came. I wasn't able to determine how much this has changed. We discussed it in 2025. Only public comment is from Oct 2024, where we encouraged them to do certain things, but we didn't get anything back.

Jeffrey: I'm inclined to say we're excited about the direction, and ask them if this is ready to review. Maybe they'll withdraw the request. 

Matthew: A new review request might be appropriate. Closing comment like "we've noticed a lot of changes. Please open a new review"

Jeffrey: I might ask them to update it, but leave it open in case updating is easier than creating a new issue.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: I will ping pointerevents to see how they've dealt with it. Will do this soon.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Jeffrey: I noticed this is still in explainers-by-googlers even though it's merged to the CSS spec, so I'll encourage them to move it.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: We asked a load of questions. Got many answers. I wasn't entirely clear, so they answered a question other than what I asked, but their answer satisfies my real question anyway. Seems all good to me. I left a comment recently to explain where I think the confusion might have been, and to say it looks fine and say what I understand. They're thinking about it in some good ways in terms of not subtly changing how ARIA works and not being too dependent on it, but let developers do common-but-tricky things. Question that remained was about orientation, and they've clearly thought about it and specified it in a good way. Uses logical orientation (inline+block rather than left+right+up+down). Can constrain keyboard handling to work in a particular direction, and they have the right escape hatches.

Jeffrey: You'll post a comment to confirm your understanding, and if they confirm, close with satisfied?

[general agreement with Matthew's draft comment.]

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Yves: Not much progress over the holidays. Remember having a potential thing about link things throught he reporting URL. e.g. add a specific site to the block list with a unique url as the reporting URL, to link sites. Didn't have time to check if that's possible. Generally looks interesting to prevent things that happened in the past like poking open ports.

Ehsan: I read through it, and still working on my review. When you read the threat model, they don't consider the server to be the bad entity.

Yves: I thought they wanted to prevent people from scanning using the API, and it's good for that. Wondering about people misusing it for other purposes.

Ehsan: They mention side-channels, and I focused on that, but your threat is more sensible.

Yves: Mine is a kind of side-channel anyway.

Ehsan: I'm positive in general. Wanted to suggest that the proponents explain it through an example. They say CSP is not relevant, but they don't go through something concrete. Could improve the explainer, but that's minor.

Yves: Wonder if there's a way to differentiate between plain HTTPS, Web Transport, and Web Sockets. Having the intended protocol in there might be useful.

Matthew: Overall we sound positive, with suggestions for improving the explainer. (2 of those: protocol + example). Yves, you're still checking on the possible threats, and we should raise that concern. Either of you want to draft the comment?

Yves: I'll draft it this week, and Ehsan can review.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Matthew: We seem to have converged. Ehsan has incorporated Jeffrey's suggestions.

Jeffrey: I'll double-check this today and thumbs-up. One nit about paragraphs inside bullets.

Matthew: Ehsan will make the tweak. If we get a thumbs-up from Jeffrey, we'll post.


### AOB

Matthew: Anything people are aware of from the other agendas that we could do?

### Triage

https://github.com/w3ctag/design-reviews/issues/1181: Assigned Jeffrey. 

https://github.com/w3ctag/design-reviews/issues/1182: APA is looking, so adding Matthew. Also adding Xiaocheng. 

### Appointments

Jeffrey: I plan to invite Philippe to discuss the people the Team is appointing, at plenary next week.

Yves: We haven't figured out those people yet.

Jeffrey: Still inclined to invite him to increase the urgency.

Matthew: Next week's plenary time is awful for Philippe.

Jeffrey: Good point. I'll offer to switch it to the other time.


## Pacific Breakout (Asia / Australia / West America) - [2026-01-06](https://www.timeanddate.com/worldclock/converter.html?iso=20260106T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Martin, Xiaocheng, Dan, Marcos

Regrets:

Scribe: Martin

### [user-agents#33: Define "user agent" as distinct from "web user agent"](https://github.com/w3ctag/user-agents/issues/33) - @jyasskin

https://github.com/w3ctag/user-agents/pull/38

Jeffrey: Please review.

Martin: This is good.  Necessary to recognize that there are more than web UAs.

Jeffrey: Suggest that we give others time to review this, since it is very fresh.  Will follow up later this week and merge unless there are objections.

Xiaocheng: Is it too general to say that an OS is a UA.

Jeffrey: I'm thinking that an OS runs 3p software.

Xiaocheng: What about cloud or IoT OSs.

Jeffrey: Can qualify that.  Maybe with "many".

### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Marcos: Don't have an update on that since we last spoke.

Jeffrey: Xiaocheng has a new comment.

Marcos: Will add to the TODO list.

### [design-reviews#523: MiniApp Lifecycle](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/523) ([Github](https://github.com/w3ctag/design-reviews/issues/523)) - @maxpassion, @xiaochengh (pending for at least 6 months)

Jeffrey: The script brings pending reviews now, so this has been pending for almost 2 years.

Xiaocheng: I tried to follow the thread.  We list some blockers, but these seem related to packaging rather than lifecycle.  They have proposed solutions to those blockers.

Jeffrey: Does that mean we need to re-evaluate or just ask for a status update.

Xiaocheng: I think we should ask for an update.

Action: Xiaocheng to post a request for update.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29
)

Just two issues to review.  These were marked as assigned in the last breakout.  Confirmed both as triaged.

### This breakout

Jeffrey: This breakout has been taking fewer and fewer issues.  We've had light agendas for the last little while.

Marcos: Depends on many factors, including absences.  We should try to assign more during triage.  Hopefully some of the miniapps items can be removed.  Not a lot of things to review anyway (about 30?), so not a lot of things to assign.  Hopefully we can close stuff more actively, especially older stuff.  Getting that to around 10, we can focus on other things.

Jeffrey: We may be at the point that the review load is manageable and we can look at other things to focus on.

Martin: One thing I've been thinking of putting on the agenda. Age Workshop: further work. Nick Doty has approached me to ask whether the TAG wants to discuss some solutions in that space. I said we'd love to talk, but we aren't the place to design solutions. Might need to adjust the time to accommodate US-east.

Martin: A lot of the work I've been doing in breakouts has been with other people on the TAG. With 2 people assigned, the chance is that it'll overlap in Europe. As I leave, that might become a bigger problem.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-01-08](https://www.timeanddate.com/worldclock/converter.html?iso=20260108T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Sarven, Yves, Christian, Xiaocheng, Marcos, Ehsan

Regrets: Hadley

Scribe: Christian

### Update on appointments

Martin: Any update on the appointments?

Yves: Not yet, but the deadline is approaching. Will come back to the group once we have tentative names.

Martin: That would be perfect, given I was tasked with chair selection.

Yves: You can send me any feedback on nominations until tomorrow.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

Marcos: No updates. Waiting for feedback from Jeffrey regarding Garbage Collection (GC).

Yves: Issue was to avoid committing to things that would be too synchronous, e.g., GC. It should be weak GC instead. Seems the current wording is ok.

Martin: Next step is for Marcos to see if he can resolve some of the feedback from Jeffrey.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49)

Martin: Any feedback from this group? Not sure why Jeffrey placed this on the agenda.

… Matthew and I worked on a new proposal (directorate-style), which allows to spread the work across more people. Need more time to talk to Matthew about this before we share it.

… Probably more work to do, as the charter only says "this process is defined by the group."

… Two chairs for this group, both would have to be TAG members. More things need work to do.

Yves: If the pool would be larger, this would help TAG, but also other groups (e.g, horizontal review groups).

Martin: This is why I want to talk to Matthew, as he has more experience working with horizontal review groups.

### RDF 1.2

Martin: Are we ready to send the review?

Sarven: For N-triples, concepts and abstract data model.  They are working on some changes based on the review that we gave.

… Started on SHACL. Not a whole lot we need to say about the RDF 1.2 Semantics. Doesn’t seem like substantial changes, touches on data handling. Seems they are deprecating one feature, too. But they are saying, 1.2 is backwards-compatible. What I gather from that is 1.2 content producers, will not use that feature. But what does this mean for 1.2 consumers or parsers? They should clarify that part.

Martin: Deprecation doesn’t generally lead to throwing errors when the feature is used. It says "we prefer you not to use it." Don’t know what the reason for the deprecation is, though.

Sarven: Is this okay to send out with satisfied?

Yves: Read your comment, and I think it makes sense. Especially, web compatibility. Makes sense to close as satisfied.

Martin: Did you find major problems?

Sarven: Nothing else that stands out.

Yves: It’s not problems, it’s things they should take care of.

Sarven: Side point, some other changes they are doing in N-Triples, they are trying to get the right text. Think this will settle, they are working on it.

… Will close as satisfied, and set the labels.

Martin: Sounds good, and you can also close the entire suite.

Sarven: What’s the process for doing that?

Martin: I think you can simply close them and set the "satisfied" label. There’s no other progress label.

Sarven: Done. https://github.com/w3ctag/design-reviews/issues/1160#issuecomment-3722957770

#### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

#### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven

#### [design-reviews#1174: WG Revision: SHACL 1.2 SPARQL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1174) ([Github](https://github.com/w3ctag/design-reviews/issues/1174)) - @csarven

#### [design-reviews#1166: WG Revision: SHACL 1.2 Core](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1166) ([Github](https://github.com/w3ctag/design-reviews/issues/1166)) - @jyasskin, @csarven

#### [design-reviews#1160: WG New Spec: RDF 1.2 Semantics](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1160) ([Github](https://github.com/w3ctag/design-reviews/issues/1160)) - @csarven

Sarven: Draft review: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/216#issuecomment-3718693351

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Xiaocheng: Will look at it until next week.

### [design-reviews#1176: Incubation: @supports at-rule](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1176) ([Github](https://github.com/w3ctag/design-reviews/issues/1176)) - @christianliebel, @lolaodelola

CHristian: Had a first look.  Seems fine, but want to do another pass.  Terminology and other things.  This lets you detect @-rule support in the browser.  Elaborate.

Yves: Is it an @-rule extension?

Martin: It extends @supports, with a new syntax. My only concern is, it looks fiddly. Documentation is going to important.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Xiaocheng: No update.

### [design-reviews#762: MiniApp Packaging](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/762) ([Github](https://github.com/w3ctag/design-reviews/issues/762)) - @ylafon, @maxpassion, @xiaochengh (pending for at least 6 months)

Martin: This is one of the design reviews that is pending for more than six months.

Yves: There were questions about parsing performance. Either outcome seems okay for me.

… One of the issues was to use a way to do URL resolving to use it as a cache, to be identified as a regulr URL. Not sure if it was in packaging or somewhere else. Will take a look at the current state of it.

Xiaocheng: Need another week, will take a look at it.

Yves: We haven't looked at it in a long time, the publication is very old.

Christian: Argue for closing it.

Yves: We can put a "propose closing" label, and close it next week.

Martin: Okay for Xiaocheng to have a look until next week, and if there’s no significant update, we can close it?

(Group consensus.)

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: Looked at it. Complex.  I don't think that it is fine.  It lets you migrate a PWA from one origin to another, but only within the same site.  Elaborate.  Lots of security reviews.  Problems are that this (again) relies on a manifest present.  In webapps, you don't need a manifest.  This only works with a manifest.  That might be fine, but there is also the ID requirement again, which we had before.  It might make sense for Marcos to take a look at it for those issues.

...Also this proposal looks at the scope extensions proposal.  It shares some files with that proposal.  Not sure what we thought about that proposal, so we might need to include scope extensions in any.

...What seems problematic is that it migrates permissions across between origins (same site).  Up for debate, but also merges permissions.  You can end up with a denial once the permissions are merged.

...Interesting problem space.  Something that people want to do, but there are a lot of details.

Marcos: When you said, lots of security reviews, you mean Chromium security reviews?

Christian: Yes.

Marcos: There is a larger TAG question, where there is a stack of things depending on other things that haven’t become part of the web platform, like Scope Extensions. I’m not sure what we should do about those. I’m gonna have a look at this as well. As you’ve mentioned, there are some parts that may be contrary to the installation workflow as discussed in the WG.

Yves: Still don’t really like the fact that is uses .well-known URLs for the handshake. Would prefer a redirect with a proper media type to trigger the progress. This is a much better architectural approach than to rely on a well-known URL. If you could pass a JSON payload that defines if permissions, data, etc. should be transferred, it would be even better.

Martin (chat): 310 Moved Permanently.

Yves: I’m looking at that from a networing side, not from the PWA side.

Martin: Permissions seems problematic. It seems fine to ask for permissions again. It’s causing an unexpected prompt, but that seems easier to attempt merging permissions.

Marcos: If you've moved it and redesigned the application.  A and B might not really be equivalent.  The new thing maybe shouldn't have the permissions of the old thing.  What if you already had B installed?  What if it already has some permissions?  Sounds un-good.  Trying to be clever never works out well.  Just reset.  What do they do with cookies?

Christian: Data is not migrated, only permissions.

Xiaocheng: How big is the motivation? How strong is the demand for this?

Marcos: Twitter.com to X

Christian: But this is outside the scope, it’s only same-site.

Martin: It’s maps.google.com to google.com/maps. And that happens. The question is, how much do you want to smooth that process over? Maybe we can skip the installation step, but not move over permissions, etc.

Christian: From a dev standpoint, rebrandings happen, and losing the entire installed user base would be bad. Makes sense to solve this, but the question is how.

Xiaocheng: Feel skeptical about motivations, seems like it’s only for the big ones.

Christian: Even if the motivation is larger companies/brands, smaller ones also benefit from this.  Small companies rebrand often, too. Or personal websites, think name changes.

### [design-reviews#1171: [wg/dx] Dataset Exchange Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1171) ([Github](https://github.com/w3ctag/design-reviews/issues/1171)) - @csarven

(Skipped.)

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

(Skipped.)

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

(Skipped.)

### Issue Triage

Yves: Any issues to triage?

Martin: We had a look during the last meeting, there weren’t many.

… Inbox zero!

### MiniApps Issues

Marcos: The miniapps stuff has been sitting there for an extremely long time now.  We should decide what to do about it generally.

... A little fraught, but avoiding it isn't helping.

Martin: Xiaocheng will take a look, and then we can discuss it next week once we have a bit more context?

… If anyone has views on this? The specification hasn’t changed in a very long time. If there’s still important work going on, that would be interesting to contemplate.

… Somebody pointed me on work in the AI space, where AI can call a tool, which produces a website, that is shown in a chatbot. Uses sandboxed iframes, but sounded like MiniApps.

Xiaocheng (chat): Generative UI?

Martin: Not necessarily, as tools are (deterministic) code, if they produce the UI. Interesting thing to think about.
