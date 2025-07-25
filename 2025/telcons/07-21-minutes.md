# TAG Minutes - Week of 21 July 2025

### Breakout A (Asia / Australia / West America) - [2025-07-22](https://www.timeanddate.com/worldclock/converter.html?iso=20250722T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Regrets: Martin, Marcos, Max

**Cancelled due to low expected attendance.**

<!-- Agenda+ -->
#### [process#43: GH issue forms might not be right for design reviews](https://github.com/w3ctag/process/issues/43)

<!-- PRs -->
#### **Callout for reviewers** [accessibility-screener#8: Update repo name in README.md](https://github.com/w3ctag/accessibility-screener/pull/8) - @matatk
#### [w3ctagbot#64: Bump @eslint/plugin-kit from 0.3.1 to 0.3.3 in the npm_and_yarn group](https://github.com/w3ctag/w3ctagbot/pull/64) - @dependabot, @jyasskin

<!-- Design Reviews -->
#### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola
#### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark
#### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion
#### [design-reviews#1043: CSS.highlights.highlightsFromPoint API](https://github.com/w3ctag/design-reviews/issues/1043) - @torgo, @xiaochengh
#### [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres
#### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh
#### [design-reviews#1115: Expose unprintable areas via CSS](https://github.com/w3ctag/design-reviews/issues/1115) - @xiaochengh
#### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres
#### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres


### Breakout B (America / Europe) - [2025-07-23](https://www.timeanddate.com/worldclock/converter.html?iso=20250723T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola

Scribe: Matthew

Present: Matthew, DanC, Lola, Jeffrey, Yves

Regrets: Christian, Hadley

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/07-21-minutes.md

Raw minutes: ...

<!-- Agenda+ -->
#### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Jeffrey: Will complete my review within 1.5 weeks.

<!-- PRs -->
#### **Call out for reviewers** [accessibility-screener#8: Update repo name in README.md](https://github.com/w3ctag/accessibility-screener/pull/8) - @matatk

Jeffrey: Merged.

Matthew: We'll un-draft Ananya's PR converting it to HTML soon - getting some final testing from APA members on it.

<!-- Design Reviews -->
#### [design-reviews#838: Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola

Lola: Happy to resolve as unsatisfied - largely due to the tight coupling with Protected Audience - will draft comment if so. I can draft a comment - Jeffrey, can you review?

Jeffrey: Yes.

Lola: I am planning to link to malicious ads, and the open issue that's been open for some time.

Jeffrey: It'd be good to acknowledge the other use cases - https://github.com/WICG/fenced-frame/blob/master/explainer/use_cases.md

Lola: Individually?

Jeffrey: I think so - fenced frames would be useful if others of these use cases were useful.

#### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @matatk, @dandclark

Jeffrey: I talked to the proponents and there's some interest from Flutter on this, so need to figure out if our proposal works at all, but overall there's some positivity. (Separating the visual presentation from the semantics.) Flutter has some accessibility challenges; looking forward to hearing from them with my Google hat on. On hold for now.

#### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @torgo, @matatk, @toreini

*group discussion* Result: Awaiting Martin's input on direction in this review; no more to add from Ehsan.

Jeffrey: We could see the related sites issue here as a security boundary, rather than privacy. Encourage UI similar to Storage Access, and then they can remove the 5-site limit.

Jeffrey: We haven't had the discussion about Cross-origin iframe registration with the right people yet.

Lola: *assigned Martin*

#### [design-reviews#1066: 'focus-without-user-activation' permissions policy](https://github.com/w3ctag/design-reviews/issues/1066) - @matatk, @heisenburger

Matthew: They updated the explainer as we asked; all seems comprehensive and reasonable; can we close satisfied?

Dan: I am happy with this approach (I had some involvement in it too).

Matthew *to close as satisfied*

#### Torgo's Issues

We should have an update on what to do with these by today

#### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @torgo, @lolaodelola

Lola: We'll un-assign Dan from this one. I can write the closing comment. I think we had some concerns.

Yves: IIRC we had concerns but ultimately were OK because it's not extending what's possible already, but making it safer in some ways. The main concern was that it should be temporary - when other features allow for this to be done in a safer way.

Lola: This was about extending to Shared Workers. This is opt in for users, which is positive.

Jeffrey: So that's either satsified because it doesn't make things worse, or with concerns, beause it depends on SAA about which we have concerns.

Yves: Yes, that was largely what the discussion was about.

Lola: I don't think we came to a conclusion; now we need to decide. I'm hearing 'satisfied with concerns' - the reasoning behind the concerns being it's no worse than what exists.

Jeffrey: The Storage Access API is concerning and we want to get rid of it, but we recognise the need to not break things.

Yves: and that it should be temporary.

Previous discussion: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/06-02-minutes.md#design-reviews906-extending-storage-access-api-saa-to-non-cookie-storage---zcorpan-torgo-lolaodelola-1

#### [explainer-explainer#7: Explain why to focus on the end-user's need, and/or moderate that advice](https://github.com/w3ctag/explainer-explainer/issues/7) - @torgo

Lola: We'll un-assign Dan from this one. I think his input can help us. I assigned myself.

Jeffrey: Happy to take this one. Was planning to ask what the group wants to do here.

Jeffrey: Often when it's a feature aimed at developers, Dan's wanted to focus on the end-user need. This has caused friction. I understand and appreciate the reasoning, but I think we should rethink this. I think we should say it's fine to have the explainer for developer-focused features to concentrate on those use cases, as long as they explain how they are not harming users.

Lola: I'm of two minds. I agree with you, but my concern is that there'll be a shift in how spec authors think about users. They may feel more empowered to place developer needs above user needs. I do agree there are some things that are just developer needs and improve DX, which is important. I wonder how we can clarify that whilst also showing that we are respecting user needs. E.g. what if a proposal makes it easier for developers to get user data?

Matthew: I feel similarly to Lola. Understand that there are some purely-technical things, but everything we do is ultimately for the benefit of people. Know it's hard -- like getting into Test-driven development -- but it's important for spec authors to really consider how it will affect users. In a really technical explainer, maybe the end-user bit is very short. "We're doing this developer feature so users get websites faster." Don't want to make people spend loads of time when it's not that related. But ultimately we do this for people. Could we give some examples from explainers we've looked at? Somewhere we said "this is very technical". Examples of explainers that handled this well.

Jeffrey: We cited Mike West's explaienr as a good example, but also criticsed it and said it could focus more on the end user. He asked us for more details on what we'd change - what would that be? Is it good enough as it is?

Lola: A lot of the stuff we try to catch with user needs is to make sure that users aren't being exploited in some way (privacy, security, accessibility, ...) - I wonder if we can rely more heavily on those questionnaires and systems? I wonder if re-framing might help, in terms of, instead of explainng user needs, explain how users may be negatively impacted. And if not, then OK - but if there are negative impacts, we want to weigh up the risks. There are technologies we know can have negative impacts in some cases, so we put mitigations in place. Even if they came in today, we may say 'yeah' but with caveats/mitigations. I think it's important we communicate the importance of user needs and UX. There are some technologies that don't directly impact the user, and I think it's unfair to make spec authors go into the indirect impacts in more detail.

Jeffrey: I'm planning to write a PR and put it up for review - this discussion was helpful. I'm thinking of: say if your feature is primarily for developers. If so, discuss any negative impacts for users. In order for it to be developer-focused, it should have almost no negative impacts on users. I would push spec authors to put these in the explainer.

#### [web-no-papers#10: Adding a conclusion](https://github.com/w3ctag/web-no-papers/pull/10) - @torgo

Lola: Have asked Dan to implement Martin's suggestion; then it seems good to go.

Jeffrey: I can implement Martin's suggestion, and merge in today - want to have that in before we review it.

##### URL templates: https://github.com/w3ctag/design-reviews/discussions/1123

Jeffrey: MapML needs templates. They're using IETF's URI templates, which mostly work but have some issues: they don't define a good way to escape braces, and don't say if they generate upper- or lower-case URL encodings. These are fixable but there's also an argument that we should be able to match URLs with the same syntax. Client-side routing could benefit from doing both matching and generation with the same syntax.

... Lea's question was how we rename the attributes. MapML proposes attributes such as 't*' e.g. 'tsrc' - eventually there should be a principle about this, but this is the first time we're doing this, so we should expect that we will get it wrong, and the second use case will teach us something else and we should define the principle.

Yves: Could it be empty `src` or `href` and a template attribute?

Jeffrey: The element that has a template is going to cause multiple fetches, especially in the case of tiles. Nothing's going to set its href attribute to an instantiation of the template. 

Yves: It's more like a factory. In that case, using 'tref' may be confusing as it's close to 'href' - something like 'linktemplate' might be better.

Lola: I agree that it would be confusing.

Jeffrey: 'tref' would be a template for generating addresses.

Lola: Next steps?

Yves: I'd like to look at it in more detail. Could say 'tref' is confusing as it's not a src or href; it's something else. Trying to find another name that doesn't have the implied semantic of using 'ref' or 'src' would be better. We know they're using this for doing fetches, but it's indirect, so don't use a name that implies a direct use of it.

Lola: In their draft report, they're saying 'tref' is a URL template. Are we saying they should not use that; and use something else? Or are we saying we want them to change how they're using 'tref' in Lea's example?

Yves: It's more about changing the name to avoid confusion with 'href' or 'src'

Lola: I.e. changing the spec, or just Lea's example? Lea's asking if it should be 'src' or something else in the example.

Yves: The spec.

Lola: +1

Jeffrey: I'm concerned about other things - e.g. should they be 'link' elements - but am informed the spec isn't ready for TAG review yet, so we'll look into those later. So Yves is saying pick a name that's further away, more spelled-out, not just indicated with a 't', e.g. 'srctemplate' (i.e. spell out the word 'template').

... The other question here is: should the URL pattern people be working on generation, or should they just fix URI templates? I think they should work on generation and we should have one syntax instead of the two pretty different ones.

Lola: If they don't work on it, would the MapML people?

Jeffrey: Or they may work on URI template - tightening the spec, and creating a JS class that could be used for it.

... We don't need to come up with an answer now, but am curious as to whether people have a sense on this.

Lola: I think the URLPattern people should be working on generation.

Jeffrey: I'll post into the discussion.

### Breakout C (Europe / Asia / Australia) - [2025-07-24](https://www.timeanddate.com/worldclock/converter.html?iso=20250724T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola

Scribe: Christian

Present: Christian, Hadley, Matthew, Ehsan, Xiaocheng, Lola, Yves

Bridge: https://meet.google.com/vvu-apdo-hrj

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

Archived minutes: https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/07-21-minutes.md

<!-- Design Reviews -->
#### [design-reviews#1071: Private Proof API](https://github.com/w3ctag/design-reviews/issues/1071) - @martinthomson, @hadleybeeman

Hadley: Nudged them for follow-up to our comments, came back saying they would revisit it, but it would take some time. Suggested to close it as timed out, and let them reopen it later.

Ehsan: Just sent a comment to the private brainstorming. We could post it to the public repository before closing it.

Hadley: We've given them a lot of comments, do you think it is important to put those comments in or can we hold on to them and post them later?

Ehsan: I consider this an important issue, my understanding is that it can protect users to proof they are not a fraud. Think this would need a clarification.

Hadley: If the TAG agrees, I think this would be important.

Matthew: We can chat with Martin if he agrees with Ehsan's comment and then post it over.

Lola: Ok, we'll wait for Martin before we proceed.

_Hadley to ping Martin in the private brainstorming._

#### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Matthew: Can we bump this to next week?

Lola: Yes.

#### [design-reviews#1121: WG New Spec: Web Speech API contextual biasing](https://github.com/w3ctag/design-reviews/issues/1121) - @lolaodelola

Lola: I'm just reviewing it, something that just need to be looked over.

Yves: Issue of poisoning things, so you need to be careful where you declare it. Apart from that, it seems okay.

#### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @toreini

Ehsan: There's no update from Martin's side yet, there is a lack of multi-stakeholder support, which I don't think is important though. Needs final say from Martin. Still waiting for them to review on our comment.

Lola: Think if there is no multi-stakeholder support, we need to call it out in our closing comment. This should be one of the concerns.

Matthew: As far as I'm aware, there's no negative expression of support.

Ehsan: Think Safari mentioned that they are supporting it, but that wasn't official, so it's uncertain. It's pointed out in the private brainstorming.

#### [design-reviews#1037: CSS Overflow Navigation Controls (Carousels)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Matthew: Found out a couple of things. There is a few things that we were discussing that I related to this one.

… Recap: We were pleased that the implementor's reflected the HTML inertion behavior

… but we still have several concerns, these include issues around whether the CSS is going to apply semantics on the page

… concerns me that it applies semantics to pseudo elements

… there's a change in HTML to harmonize HTML and CSS, and they've agreed on that you can't uninert

… we've talked about Cascading Attribute Sheets as an alternative solution

… for the other one, I don't see a solution. If you do inerts (i.e., hide from a11y tree), there is no way to explore them using the virtual cursor, which is a very important navigation mechanism, which is especially useful on mobile (rotor in VoiceOver), which allows you to skip between segments like headlines, landmarks etc.

… One potential way around that would be that the user agent would be aware of this, but this would take a lot of effort

… Lot of related things are going on at the same time, think we should have a comment that combines all these

… I think we are concerned about this more than we were before. I'm happy to draft the comment, so we have it available next week.

Lola: Totally fine. Jeffrey also mentioned that we can link to Scott O'Hara's blogpost. If there are things in the blogpost, you can refer to them. Let's talk about this next week.

Matthew: Xiaocheng, you are also on this issue. Thoughts?

Xiaocheng: Don't have anything to add. Waiting for you to finish the comment.

#### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @matatk, @xiaochengh

Xiaocheng: Discussed this two weeks ago, I was supposed to draft a comment, but didn't do it yet.

… There is a point that Martin raised earlier about the indirection of element names. Could you explain this to me?

https://szager-chromium.github.io/declarative-interactions/#solution-sketch

Matthew: There seems to be a layer of indirection, where you give the animation trigger a name, but we don't understand why. Why not simply selectors? What is the advantage of introducing the name?

… Looked at the spec, and had an idea. Maybe they give them a name, so they can skip the shadow tree, but that doesn't seem necessary. But it comes back to why do we need the name?

Xiaocheng: I think anchor positioning should have the same issue, did we discuss it before?

Matthew: We should check back on that, good point.

… Other concern is that they don't specify where the name for the trigger functions come from, very underspecified.

Xiaocheng: Will check anchor positioning and then draft a comment.

Lola: We will come back to this next week.

Xiaocheng: If we've discussed this before, we could send out the comment this week already.

#### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Matthew: We're seeing the proponents of this issue next week, we've invited them to the plenary call.

… Long discussion in the private brainstorming, we're uncertain about what the attribute tries to solve

… We struggle to agree on the questions we want to ask

… Maybe we should discuss this asynchronously with Martin and Marcos before we talk about it here

… There's much disagreement in the TAG about what the underlying problem is, and how to solve it.

#### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @ylafon, @marcoscaceres

Yves: Marcos wasn't there, so we need to move this.

#### [design-reviews#1117: Add IndexedDB getAllRecords() method and update getAll()/getAllKeys() to support direction option](https://github.com/w3ctag/design-reviews/issues/1117) - @martinthomson, @christianliebel

Christian: Didn't have time yet, will take care of it until next week.

_End of official agenda, bringing over issues from Breakout A._

#### [design-reviews#1043: CSS.highlights.highlightsFromPoint API](https://github.com/w3ctag/design-reviews/issues/1043) - @torgo, @xiaochengh

Xiaocheng: They've introduced another JavaScript API that requires synchronous updates of the layout and performing a hittest if the current layout is not up-to-date. This was the major concern last time, and we closed it as unsatisfied.

… Three weeks ago, they came back and added more arguments why asynchronous updated are difficult and offered a more holistic solution.

… Thinking about closing this as satisfied with concerns. This is a long standing issue, and asking them to fix it is probably out-of-scope.

Matthew: Is there some kind of guidance that we could offer?

Xiaocheng: How would we approach this?

Lola: Would say we shouldn't do that, closing as satisfied with concerns seems fine, if they want suggestions, we can talk about it. Unless you have in-depth suggestions?

Xiaocheng: Probably not. I'll post a comment with satisfied with concerns. Still concerned with adding an API that can cause layout refreshing. Happy to see explorations of holistic solutions to that problem.

#### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

Xiaocheng: Wanted to post a comment, but didn't do it yet. Will have a look.

Lola: Do you want someone else to look at this review or are you fine?

Xiaocheng: Unless someone else wants to join?

#### [design-reviews#1115: Expose unprintable areas via CSS](https://github.com/w3ctag/design-reviews/issues/1115) - @xiaochengh

Xiaocheng: Posted a comment, and they immediately replied.

… Posted that we are generally positive, provided an alternative, they've responded with why the alternative doesn't work

… Since it's an early review, we could close it as satisfied. I believe we're on the right track.

… We want to see more alternatives explored while they are developing this.

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

_Xiaocheng and Matthew to take [design-reviews#1120](https://github.com/w3ctag/design-reviews/issues/1120)._
