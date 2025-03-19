# TAG Minutes - Week-of 17 March 2025

## Agendas

### Breakout A (California / Europe)  - [2025-03-17](https://www.timeanddate.com/worldclock/converter.html?iso=20250317T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @jyasskin, @matatk
* [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012) - @matatk
* [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013) - @matatk
* [Suggest talking about "people" rather than "users"](https://github.com/w3ctag/process/pull/40) - @jyasskin, @martinthomson, @csarven, @torgo
* [Use "Web user agent" in title and intro](https://github.com/w3ctag/user-agents/pull/10) - @csarven, @jyasskin
* [Revise common web user agents, add command-line and web crawlers](https://github.com/w3ctag/user-agents/pull/11) - @csarven, @jyasskin
* [add entry about communication guideline](https://github.com/w3ctag/process/pull/38) - @ylafon, @martinthomson, @torgo


### Breakout B (California / Australia) - [2025-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20250318T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [CSS Inline `text-box`, `text-box-trim`, and `text-box-edge` properties](https://github.com/w3ctag/design-reviews/issues/1021) - @xiaochengh
* [CSS Overflow Navigation Controls](https://github.com/w3ctag/design-reviews/issues/1037) - @xiaochengh (with guest joining)
* [CSS if() function](https://github.com/w3ctag/design-reviews/issues/1045) - @xiaochengh
* [CSS Scroll Buttons](https://github.com/w3ctag/design-reviews/issues/1054) - @xiaochengh
* [CSS inert](https://github.com/w3ctag/design-reviews/issues/1055) - @xiaochengh
* [Start a guide to chairing the TAG.](https://github.com/w3ctag/process/pull/39) - @csarven, @martinthomson, @torgo, @hadleybeeman, @jyasskin

### Breakout C (Europe / China) - [2025-03-19](https://www.timeanddate.com/worldclock/converter.html?iso=20250319T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola
* [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @marcoscaceres, @hadleybeeman
* [Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @lolaodelola, @martinthomson, @jyasskin
* [Clarify which websites will be well internationalized.](https://github.com/w3ctag/ethical-web-principles/issues/146) - @torgo, @hadleybeeman, @jyasskin
* [Improve Baseline text](https://github.com/w3ctag/the-web-is-not-versioned/pull/9) - @martinthomson, @jyasskin

### Plenary Session - [2025-03-19](https://www.timeanddate.com/worldclock/converter.html?iso=20250319T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk
* [Unicode MessageFormat 2.0](https://github.com/w3ctag/design-reviews/issues/1042) - @jyasskin, @torgo
* [(brand new ✨) Web Install API](https://github.com/w3ctag/design-reviews/issues/1051) - @torgo
* Privacy principles consensus: [Rework retaliation text](https://github.com/w3ctag/privacy-principles/pull/458) and [Ancillary definition](https://github.com/w3ctag/privacy-principles/pull/459)
* [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @hadleybeeman, @csarven, @martinthomson, @jyasskin,
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (California / Europe)  - [2025-03-17](https://www.timeanddate.com/worldclock/converter.html?iso=20250317T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Matthew, Yves, Jeffrey, Sarven, Lola

Regrets: Torgo

Scribe: Sarven

#### [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @jyasskin, @matatk

Matthew: If the rules of themselves are implementations of this document, then our recommendations about how to make the format more precise would kick in?

Jeffrey: A lint to some rules to comply with the spec.

Matthew: I can comment. We knew in general it wasn't precisely defined.

Jeffrey: We should recommend to pick one but perhaps don't need to object. All of the rules are in one format so no reason not to standardise on that.

Matthew: IIRC, the headings/values weren't specified. Can pick out some of those examples. They can ask APA for input and we (TAG) can help out.

Jeffrey: Sounds reasonable.

Matthew: They're looking at WPT. Work on manual rules as well. Some are not objective. All seem reasonable.

Matthew: Is our preference to close this? Mention examples of things to be more precise?

Jeffrey: Do you think we'd be unsatisfied because the spec isn't tight enough?

Matthew: Technically I think we are?

Jeffrey: Ask to iterate.

Matthew: Ack.

Jeffrey: I'm happy to review. Anyone else can review too if they like.

*[Matthew posted comment](https://github.com/w3ctag/design-reviews/issues/977#issuecomment-2730535113)*

#### [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012) - @matatk

Matthew: Wrote a comment about this in internal thread. Lots of technical stuff. Needs more eyes. Some considerations: the Explainer talks about two ways to do this on the platform but we kind of don't because both are only in Chromium. In the alternative section: it also mentions why it isn't suitable. That's sounsd about right. Then why not fix that API in the WG instead of proposing it here in the Explainer. Wasn't quite sure.

Jeffrey: Is user timing more widely implemented?

Matthew: It's Baseline.

Jeffrey: It'd be nice if the Explainer would say that. Probably worth posting the questions to the discussion thread.

Matthew: Will mention if they have considered it in the WG. Fix/Augment/Replace to address the needs they got. Will draft.

Matthew: We asked some things to be added to the Explainer. Specifically end-user needs. And less specific about alternatives considered.

*[Matthew posted comment](https://github.com/w3ctag/design-reviews/issues/1012#issuecomment-2730568703)*

#### [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013) - @matatk

Matthew: Don't enough. It is interesting, and agree it should be more interoperable. Firefox is doing it. Not sure about WebKit. Signs are good. Curiousity is interoperable and implementation-metric. They give an explanation on why interoperable-metric is one or two things. Not sure how interoperable it is. Perhaps @xiaochengh could look into it.

Jeffrey: We should post something about direction looks good. Agree re having xiaochengh a look.

Jeffrey: Hope to post something in plenary.


#### [Suggest talking about "people" rather than "users"](https://github.com/w3ctag/process/pull/40) - @jyasskin, @martinthomson, @csarven, @torgo

Jeffrey: Martin had a suggestion.

Sarven: WFM. Simpler. System covers program.

Lola: I think it is fine.

Jeffrey: Took Martin's change and Merged: https://github.com/w3ctag/process/pull/40


#### [Use "Web user agent" in title and intro](https://github.com/w3ctag/user-agents/pull/10) - @csarven, @jyasskin

Jeffrey: I think we have consensus on this. Sarven can you review since you have change requests.

Sarven: Merges.

#### [Revise common web user agents, add command-line and web crawlers](https://github.com/w3ctag/user-agents/pull/11) - @csarven, @jyasskin

Jeffrey: Okay with the current state.

Lola: I think it is fine.

Jeffrey: Will merge.


#### [add entry about communication guideline](https://github.com/w3ctag/process/pull/38) - @ylafon, @martinthomson, @torgo

Jeffrey: Merged.


#### [WebRTC Encoded Transform Timestamps #1049](https://github.com/w3ctag/design-reviews/issues/1049)

Lola: I'm the only one assigned to it.

Jeffrey: I can also review. Will put it on the plenary.

[General sense that Martin would actually be the right reviewer.]

#### Misc

https://tag-github-bot.w3.org/ with source at https://github.com/w3ctag/w3ctagbot, for any of our automation needs.


### Breakout B (California / Australia) - [2025-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20250318T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Jeffrey, Matthew, Marcos

Guests: Robert Flack, Vladimir Levin, Tab Atkins

Regrets: Torgo

Scribe: Jeffrey

#### [CSS Overflow Navigation Controls](https://github.com/w3ctag/design-reviews/issues/1037) - @xiaochengh (with guest joining)

Matthew: Several issues split out. Inert is the juciest from my perspective. APA had some questions about the scrolling stuff, some of which were answered by the fact that it fits into the overall proposal. Where else do you see this being used? It would be a good idea to start with an idea of what the current status is. Short term availability. And I have some other questions.

Robert: In Chrome 135, scroll markers, scroll buttons, columns, `interactivity` are available. Element-based scroll markers aren't.

Matthew: Inert will be an in-depth discussion. Some questions about scroll buttons.

Matthew: There's a lot of good stuff that's come out of this trend to avoid needing Javascript. Generally we're supportive, but we also have some concerns, particularly about inert. But also when you're doing a big thing, wouldn't create a single primitive just like ordering in support of masonry. Makes sense to look at what can be split out to solve other problems.

##### [CSS Scroll Buttons](https://github.com/w3ctag/design-reviews/issues/1054) - @xiaochengh

Matthew: TAG had an understanding that the scroll markers and buttons: is that intended to be used for something wider than carousels? Roadmap for where that's going to be used?

Robert: Intention for scroll markers is that they're very similar to a table of contents. Authors could use this for other use cases where a list of anchor points would be useful. For scroll buttons, they're equivalent to having a JS-based button to scroll an associated area. Many ARIA authoring guidelines suggest this for carousels. It sometimes shows up in other contexts, like with a 'view more' button to scroll the page down. Adds this automatically without needing script.

Matthew: Might it be used in a 'back to top' situation? Or 'back to top of section'?

Robert: Could. Scroll buttons don't provide that specific thing, but we could add it as a value. The intention is for that kind of thing for any scrollable region.

Matthew: APA got looped in on this through a CSSWG member labling the issue. It was a discussion of scroll buttons, and we couldn't find the overall explainer. Nobody's fault. We're looking at tweaking the process so the TAG sends us explainers. One issue we had, and it sounds like these are separate, but just to ask. You say "scrollable regions". In a Terms & Conditions, that's a scrollable area. Could they be applied in that case? Or just to scroll the viewport? Merge this with the browser's scrolling controls?

Robert: Can be associated with any scrollable region, so Ts&Cs woudl work. Haven't spec'ed how these would be attached for the root scroller, but they should work there too. This isn't the browser's affordance for scolling though; it's the developer's affordance. We wouldn't add scroll buttons by default.

Matthew: Would you end up with both?

Robert: This has nothing to do with the scroll bar.

Matthew: There was a lot of concern about focus order. We thought that if this were applied to scrolling in general, it might result in extremely different keyboard interaction. Now you press up or down, and there was a concern that this might need focus. But this is a button going to a particular place.

Robert: And adding the button doesn't prevent normal scrolling. It's the same as if the author wrote a `<button>`.

Matthew: Describing the problem is the most difficult part. ...

##### [CSS inert](https://github.com/w3ctag/design-reviews/issues/1055) - @xiaochengh

Matthew: APA left a comment on the TAG review. This is doing much more than CSS often does.  How many of you have seen the APA-specific feedback? Robert replied. Going through APA's still-current comments.

Matthew: Why wasn't the original proposal sufficient? Overflow interactivity. It's not mentioned much in the explainer.

Robert: For the specific case of making a carousel, it's perfectly sufficient. When we discussed this in CSSWG, people were concerned that cases weren't handled by this. Scott raised concerns that while we're making it possible to automatically handle some use cases, we should handle some other ones. For carousels, it doesn't require the per-element interactivity thing, in most cases. There are experiences where authors will have animations as things scroll, so they're technically in the scroll port even though they're not visible yet. Maybe we could work around it.

Matthew: So, to make it more generally applicable. Some of Alice and Scott's cases, you couldn't do with that properrty, but don't know how effectively you can do them with `inert`. There are still some things you can't do. In the explainer, it cites the ARIA authoring practides, and I know Open-UI worked on a range of carousels, but for specifically accessible carousels, the APG one was the main cited one. There are different ways you can do it, and I've cited a few. Paul who's also in CSSWG. Some don't make the out-of-view content inert because it's part of a navigation. Some don't do it and still provide alternate means of navigation, and make `inert` a progressive enhancement using HTML with some JS. Some are like tab panels. When you were looking at this, did you look at other keyboard navigation patterns.

Robert: APG one doesn't even handle arrow keys. I looked at several. Cited APG as the authoritative one, but I thought abuot other experiences. That's why it's not just a default thing, but it depends on the experienc eyou're building. A list of contents probably makes sense to have the offscreen content in the tab order. When you have 100s of items, and many focusable things in each item, (e.g. the APG one with slides), it's a better epxerience for accessibility and keyboard navigation to have the separate controls, and make just the current pane interactive. Support both of those, with developer guidance.

Matthew: There are lots of types of carousels, including where cards have interactive and non-interactive content. What's insufficient about HTML's `inert` attribute?

Robert: You have to manage that in script, and tracking what's in view is non-trivial. One bit advantage over the APG example is that the carousels we're advocating are scolling containers. They advertise as having more content in the direction they pan. When you do that, it's complicated to get the events correct to update the `inert` attribute as you scroll.

Matthew: Looking at the discussion on this thread, your approach looked entirely reasonable. My worry, and APA's, were the implications of following this approach. We have a lot of experience of mistakes like this. People who accidentally use this even though they shouldn't. Accessibility consultants see so many instances of using ARIA when you shouldn't. This is something with no visual effects which could render a whole site useless to someone using AT. Can see it getting copy+pasted all over the place. Mitigations against things like that? Devtools could highlight inert parts of the page?

Robert: Unlike accessible-name, inert affects interactivity for all users, not just AT users.

Matthew: That helps.

Robert: Having some visual indication of this in devtools would be a good idea. I liked on the CSS discussion, Scott suggested something very similar, to have a visual treatment of those elements to make it obvious. Fits in devtools.

Matthew: Would have to be by-default until the user turns it off.

Matthew: Possibility of escaping the inertness, maybe unintentionally. Alice's comment about limiting it to the top layer. And if you have the ability to un-inert stuff, that's quite different from the HTML one, which is absolute. They're both called `inert`, which is confusing.

Robert: HTML attribute only has a value to make something `inert`. No opposite value. CSS has that, plus a new value that's not present in HTML. Not that confusing. HTML has a hidden attribute, while CSS has `visibility: hidden|visible`.

Matthew: The effect of this one is invisible. If you inert a subtree, you might test by clicking it, but if other things get un-inerted, you wouldn't know. Developer education. It's different because you can't see the effect. Asking you to limit the un-inerting to teh top layer might go against how CSS works. Limiting risk.

Robert: One thing we did, if you have content in the otp layer, you cant un-inert content outside it. That makes sure that if you have top-layer-modal UIs, you can't make deep content interactive. I understand the concerns: this doen't feel akin to other CSS properties. But today I added that a requirement to use the top layer eliminates some use cases like component modals. Must interact with part before you can use the rest of the component, but don't want that to prevent interaction with the rest of the page. Don't want it to pop above things outside the component. That's why it's generally useful to provide un-inerting. Good use cases where the top layer doesn't provide needed capabilities.

Matthew: Interesting. An ask on the comment thread was "couldn't we do a more thorough study of these mechanisms". You might say "we did that; here's a pointer". If we'd like to support some use cases, right now they're supported by frameworks and libraries. Might use the `inert` attribute or other mechanisms. How much JS code are we going to save by having this extra feature?

Robert: Doing this today, you have to change the structure of your DOM so the interactive content is outside the `inert` content. Or you can modify the tabindexes, but that's much worse for accessibility, because that content is still present. Either the libraries carefully ensure the interactive content is at the top of the DOM, which has structural and layout limitations. Or tricks with tabindex, which provides very different experiences between regular and AT users.


Matthew: Sounds like you're expecting that you can eliminate all the scripting. Is there anything left for JS to manage?

Robert: Goal is that you shouldn't need to use script, especially in support of users who disable script in their browser, it should be fully functional. There's probably always edge cases where it doesn't do exactly what you want, so you have to reach for script.

Matthew: For accessibility stuff, there's this view that to make it accessible it must not have JS. For a long time that was true. It's been such a long time since we gave up on the notion that there would be no-script browsers. Know why you want to move things out of the main thread. Anchor positioning is so good for accessibility. Carousels suck for accessiblity and usability: users often miss everything except the first slide. But designers want to use them, so you're making them better. If there was something devtools could do, fairly aggressively, that would be good. We have some things to think about, and maybe we can make suggestions.

----

Matthew: We didn't talk much about stylable columns because we didn't review it as extensively. Anything we should be aware of?

Robert: column-boxes that we lay things into. Styling is quite limited. Most properties don't apply; no full layout boxes. No font-size. Lets authors add things to physical locations of column boxes. It's the combination of features that make it really powerful. Scroll markers on columns makes an automatically-paginated carousel, but it uses existing primitives rather than inventing new things.

Matthew: Was there ever a stage where people researched whether there should be an element to handle this?

Robert: Yes. We started from elements, 5 years ago from an element perspective. Through the research of the ways developers want to create these experiences. It was going to be extremely difficult to pick a particular element behavior. Would be best to provide the features that authors could combine. It's possibel to revisit an element with the features in mind. Build an element from these features, which matches the `<selectlist>` approach.

Matthew: Yes, would be surprised if people could come to consensus on an element.

Matthew: Just before this call, there were some issues with customizable select. Didn't review the PR.

Robert: Saw it but haven't looked into it.

Tab: Same.

Matthew: Comments from Scott and Sarah Higgley. On carousels, everything makes sense, but I'm concerned about how people will use this in other places. Use cases that you've mentioned sound really good, and like a hassle to support now. There are tradeoffs in everything: if you have to structure your DOM in a certain way; people have tech debt which prevents them from making things accessible. Making people structure their DOM in a certain way might be far too restrictive. But with great power comes great responsibility. Undersatnd much more about motivations and tradeoffs. You're into the possibility of providing more help for developers. Wise for us to check out the latest comments on the actual PR. The worry about it having effects without being visible is my biggest concern.

Matthew: I still need to dig into the concern around un-inerting and live regions. Certain things we might be able to have added for developer education. Still some technical concerns that I'd like to ensure we understand. But that was very helpful. We'll see if we can offer anything constructive.

Matthew: What should we weight differently?

Robert: Inerting affects all users, not just AT users. Important to emphasize to authors that they've made authors inert, but it'll still affect regular users.


#### [CSS if() function](https://github.com/w3ctag/design-reviews/issues/1045) - @xiaochengh

#### [CSS Inline `text-box`, `text-box-trim`, and `text-box-edge` properties](https://github.com/w3ctag/design-reviews/issues/1021) - @xiaochengh

#### [Start a guide to chairing the TAG.](https://github.com/w3ctag/process/pull/39) - @csarven, @martinthomson, @torgo, @hadleybeeman, @jyasskin



### Breakout C (Europe / China) - [2025-03-19](https://www.timeanddate.com/worldclock/converter.html?iso=20250319T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Lola, Marcos, Xiaocheng, Yves

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola
Lola: Comment received yesterday, need more time.

#### [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @marcoscaceres, @hadleybeeman
Marcos: closing it, and close [#899 Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) as well

#### [Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @lolaodelola, @martinthomson, @jyasskin

#### [Clarify which websites will be well internationalized.](https://github.com/w3ctag/ethical-web-principles/issues/146) - @torgo, @hadleybeeman, @jyasskin

#### [Improve Baseline text](https://github.com/w3ctag/the-web-is-not-versioned/pull/9) - @martinthomson, @jyasskin

#### [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013) - @matatk

#### Issues cleanup
[Constructors for RTC encoded frames with custom metadata](https://github.com/w3ctag/design-reviews/issues/942) closed with resolution timed-out, as no information was received in nearly one year.
[Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) no progress, propose closing?




### Plenary Session - [2025-03-19](https://www.timeanddate.com/worldclock/converter.html?iso=20250319T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Matthew, Christian, Sarven, DanC, Jeffrey, Lola, Yves

Scribe: Sarven

#### [Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) -
During Breakout C, Marcos figured out this issue was reopened but the resolution label is still there.
Should it be closed and a new issue be created?

Jeffrey: Agree with Marcos. How do others feel about this?

Dan: It seemed liked a good change.

Jeffrey: Shall we suggest satisfied? Earlier it was satisfied with concerns. Looks like they got through the concerns. Hearing no objections, I'd say we're satisfied.

#### [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk

Jeffrey: Dan Clark and I are too close to the contributors. DanA has concerns.

Yves: It'd be good to know how the browsers ???

Jeffrey: {explains background on the issue / explainer} This matches what iOS does. Gets a toast sayin the webapp is being sketchy but with ??? you don't get it. Firefox / Safari are okay with this design. Am excited about this because it'd enough to get remote desktop apps. Because it opens the use case for Firefox/Safari.. we could push Chromium to not read the clipboard all the time.

Sarven: Piecing together from a couple meetings. I thought the concern was that there's a permission being given to the app, that once they have it, there's no way the user can know when to revoke that permission. So the app/site has continuous access to the clipboard. Also, the original issue was giving read access to RAM. What precautions are being taken? Or reasoning? There's a lot the user is asked about accessing hardware; can understand the argument that this falls into that category, and the UX can be designed so the user is aware, and you have the right to revoke it. Is just making that a possibility, good in itself? Laptops have an indicator that the camera is on, via a light. Clipboard: is there such an indicator? Understand the concerns that are raised. What steps are taken to ensure that it's safe and/or even if the user is tricked into granting permission, they have ways of backtracking.

Jeffrey: This particular API doesn't fix any of those problems. Chromium permission model for clipboard allows persistent access. I think there are ways for Chromium to indicate those but they haven't implemented the mitigations. So that bad state is still ther.e The reason I'm still excited about this is that it give a route to fixing that. Doesn't make it better or worse. Firefox/Safari have shipped nearly the same API without a problem, without a permission. This allows the use cases for Chromium where they have permission quality ... We should scope our review to this API and what it enables. Chromium has the status quo but this at least gives a process to improving that situation.

Matthew: For context, we've discussed this before and realised that the status quo isn't acceptable but this is narrow in scope. Why do we need to know the types on the clipboard on copy as opposed to paste.

Jeffrey: 1) there is a lot of spreadsheed apps, they give you the kind of things you can paste (value, formula, format etc.) And in order to what to enable you have to know what's on the clipboard. Need to know that when the user enables, before pasting.

Matthew: Native apps similar?

Jeffrey: This is why iOS allows type-x without warning.

Matthew: re Sarven's permissions, you said iOS popup with toast before permission, if you give permission, how long is the permission?

Jeffrey: Safari, or at least iOS doesn't. So what they did was to pop up a toast. The UI they have for the async API, thwn then wesite asks to read the clipboard, one item with paste item in it. If you trigger it with keyboard, it'd be under the mouse - bad accessibility / UI problems - kind of works.

Matthew: This clearly is an improvement over the status quo but some TAG's understanding is that the status quo is already really bad. Ack improving things for the future. What can we do if we say go for this? e.g., To encourage Chromium's model to change.

Jeffrey: https://github.com/w3ctag/design-principles/pull/563 . Directly relevant. Don't improve API unless mitigating problems. A path toward fixing them. I don't know how we can push Chrome to fix this. The sketch I had in mind is all three browsers ship this API. Remote desktop app that uses this could use all three. Maybe we take a page from iOS to show the toast. Right now it shows if you pasted in current sessions - that can be louder. Don't know for sure which way would have traction.

Dan: UI more aggressive to push those measures if we have this as off ramp.

Matthew: We don't say how their UI should be. I guess once we okay this as TAG, then need to push on it hoping that it changes.

Jeffrey: We can file Chromium bugs for example. Suggest a UI along the lines of x,y,z.

Matthew: We also talked about this is writing to the clipboard. That seems also free for all. Perhaps of the lesser of the two evils.

Jeffrey: We could toast on write. Same paste surfaces do this. They warn you like finger-pasting can do bad stuff for you. Windows-command ought to be doing that. We should be telling people the stuff in the clipboard is not necessarily safe.

Matthew: Good example of annoying but not malicious and user doesn't know until pasting.

Jeffrey: They immitate recaptcha.

Jeffrey: So what's next? Sarven's been most skeptical on the call, so what do you think?

Sarven: You mentioned Dan A has a concern, so from my end, I'd like to catch up. Everything said has been sensible, but I don't understand it well enough.

Dan: I can write a draft proposal. Can write a summary based on today in the private brainstorming.

Matthew: Yes, and, like Sarven want to check out the edges. Mention the direction and also file bugs that needs to be followed up to address the root problem.


#### [Unicode MessageFormat 2.0](https://github.com/w3ctag/design-reviews/issues/1042) - @jyasskin, @torgo

Jeffrey: I'm basically happy with it. We should get overall TAG to agree that this is a sensible review.

Jeffrey: Close as satisfied? OK.

#### Privacy principles consensus: [Rework retaliation text](https://github.com/w3ctag/privacy-principles/pull/458) and [Ancillary definition](https://github.com/w3ctag/privacy-principles/pull/459)

Jeffrey: They've been available for a couple of weeks. Any objections to merging them?

Sarven: Approved 459.

Jeffrey: Sounds like no objections. Merging.


#### Breakout Rollup

##### Breakout A

* Hoping to post a comment on [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013) once Xiaocheng has a chance to look at it.
* Merged https://github.com/w3ctag/process/pull/40.
* Merged https://github.com/w3ctag/user-agents/pull/10.
* Merged https://github.com/w3ctag/process/pull/38/.

##### Breakout B

Jeffrey: {Summarises}

Jeffrey: `interactivity` is the most contentious piece. What should we do about it?

Lola: seems like CSS carousel is something the CSS community wants. How important is inert to the rest of the CSS carousels package?

Matthew: re What could we do before they ship someting ? They could ship without this property, or with JS enhancement. Next level / more towards their position would be, what about that initial proposal from Robert, it might / might no be sufficient. It wasn't attracting a concern from the CSS accessibility community. Most of it could be shipped still. Accessibility concerns are along th elines, this could alter / remote content from the page, from the kb or AT perspective, or all sorts of interaction. The risk is that people missing content or it could do the opposite making up content. There is a consistency argument here. One of the proposed solutions was: un-inerting only works in the top layer, but that doesn't fit the CSS model. Un-inert'ing everywhere doesn't fit the existing HTML model. If this ships, there'll be inconsistency any way since we have an established way to do this in HTML. Silverlining: dev tools could at least highlight stuff inert. I'm concerned about the risk of this. To build consensus here on how to get most of way.

Lola: Trying to get consensus now in this call?

Matthew: Would be nice but people making proposal and have accesibility concerns. I don't know how to help bridge that gap - besides the limited ways that we could, e.g., partial shipping of it.

Jeffrey: Chrome is making the argument hat accessibility team is being too cautious here. Preferring to get it in front of the developers and accept the fact that some people will misuse it.

Lola: Writing a talk for AC about accessibility team being cautious, we don't have to rely on independent browsers how they are goin gto fix it in their browsers. That makes the web more distorted, and it doesn't have to be that way now. I do think that more work needs to be done - consensus on the middle ground. I guess this is what Matthew is saying. Perhaps that's what we can focus on re what the issues are.

Jeffrey: Chrome is scheduled to ship this April 1. TAG might have a consensus on having an opinion on it. It'd be worth to write it down. Perhaps Matthew and Lola could collaborate?

Matthew: re move fast but make it better, as long as willing to change. But once people start using it... Gave an example of ARIA labels. From a TAG's perspective and our job is to be consistent.

##### Breakout C

Yves: We didn't have most of the people involved in the issues in the meeting. Did close several issues and forward [Partitioning :visited links history](https://github.com/w3ctag/design-reviews/issues/896) to this plenary.


#### [(brand new ✨) Web Install API](https://github.com/w3ctag/design-reviews/issues/1051) - @torgo

#### [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @hadleybeeman, @csarven, @martinthomson, @jyasskin,

#### [WebRTC Encoded Transform Timestamps #1049](https://github.com/w3ctag/design-reviews/issues/1049)


#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
