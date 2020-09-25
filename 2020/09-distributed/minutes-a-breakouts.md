# 22 Sept 2020

## 02a

Alice: meta-PR is here: https://github.com/w3ctag/design-principles/pull/230

### Readability edits: Cascading Style Sheets section https://github.com/w3ctag/design-principles/pull/221

Alice: this one is new since I joined the TAG; I can't remember when it was added.

Sangwhan: I don't think I'm the best person to review this one.

Alice: I might bring it up with Tess.

### Readbility edits: JavaScript Language section https://github.com/w3ctag/design-principles/pull/222

Sangwhan: Some subtlety was lost from an implementer perspective in "js-rtc", but I think that part is ok.

... For js-gc, I think the summary comment might not be quite accurate to the original.

### Readability edits: Event Design section https://github.com/w3ctag/design-principles/pull/223

Sangwhan: Dropping dont-invent-event-like misses some useful guidance.

... and events-vs-observers is absurdly long.

Alice: For events-vs-observers, I wondered whether it might be its own document.

Sangwhan: I think dont-invent-event-like could be reinstated, but with some much briefer text.

... At the point where the spec author has already decided to use one or the other, they'll be looking at events-vs-observers. This is not intended for that audience.

### Readability edits: Types and Units section https://github.com/w3ctag/design-principles/pull/224

### Readability edits: Other API Design Considerations section https://github.com/w3ctag/design-principles/pull/226

### Readability edits: Writing good specifications section https://github.com/w3ctag/design-principles/pull/227

### Readability edits: JavaScript API Surface Concerns section https://github.com/w3ctag/design-principles/pull/228


## 03a (Rossen and Tess)

### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

Rossen: We already spent some time dicsussing the issue and creating a spreadsheet of all features that interact with subframe/subresource. This is a good topic to remind everyone at the planery to take a look and start engaging on the spreadsheet.

### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/521)

Rossen: This issue is already on the radar of the CSSWG. It was scheduled for a group discussion with Alice present in the first Wed of Oct.

### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509)

Tess: Little Dan started discussion on the webkit slack about unsigned bundles. Most likely as an action from TC39 discussions.

... Questions put to the room are mostly about cross-origin cases and can we separate features and concerns based on signed/unsigned?
... Ex. navigating to an unsigned same-origin bundle then there should be no problem. 

... The rest of the issues that apply to the cross-origin case, like what goes in the address bar in the case of cross-origin unsigned bundle etc. Again, repeating lots of things that have been said, if the bundles are signed you do at least have some reason to believe the publisher had a hand in creating it.

Rossen: So there has been a lot of discussion on the issue and we have commented a number of times without success (last two comments handing for over a month). How about with propose the following at the planery in order to make progress?

... 1. There seems to be a good support by use cases and some of the community about the capabilities unsigned same-origin enables.
... 2. Some concerns with cross-origin will be lessened if the budnles are at signed.

... Based on 1 and 2 we should propose splitting this design review into two parts in order to separate concerns. One for unsigned same-oring and one for unsigned cross-origin.

### [High level or low-level APIs?](https://github.com/w3ctag/design-principles/issues/117)

Tess: Looking at the minutes of our last discussion it should be rather easy to distill a PR against the principles doc. (summarizes notes). 
... Happy to take a first crack at this week between breakouts and go from there.

## 04a

Yves, Dan, Peter

### discussing miniapp work

Yves: they are exploring the differences between minuapps and regular webapps... to figure out what they shoild work on in W3C. Talked about URL scheme - we should avoid to use a miniapp URI/URL scheme. If there is another way to do it then they are fine with - it - so URI scheme may be moot.

... Packaging ... some features of budles/etc.. may not be required for niniapp.

... Manifest - the goal is to avoid creating a new manifest and to get what is needed for miniapp ion the manifest. 

... lifecycle - they want to sync as close as possible .. but may need something special for miniapps.

Dan: looks good!

### role of director

Yves: TAG taking a technical review role...

Peter: we talked as part of the blink shipping process discussion - having TAG review triggered by something moving into WICG....


# 23 Sept 2020

## 05a

### [add a section describing what should be in html versus css versus javascript (the separation of concerns) (HTML Design Principle 3.4)](https://github.com/w3ctag/design-principles/issues/169)

Tess: We've talked about this a few times in breakouts, but the minutes weren't linked. I think we had some interesting conversations.

Alice: There is a misconception that the accessibility tree is based off the "vanilla" DOM, which seems very pervasive.

... Previously talked about the capabilities, characteristics of each of those layers.

Tess: Rephrasing... there is a historical thing here, some context we could give around what the original intent was. The reality is more muddled than that, but the rough design still holds.

... e.g. when we're talking to authors, we advise avoiding `style=` on the element, but instead suggest using the class name.

... Partly this intellectual idea about what belongs in each layer... also maintainability/engineering aspect, having clean interfaces. Class attribute, class selector syntax are an interface between markup and styling. Similarly with the ID attribute, ID selector.

... less likely to run into specificity confusion if avoiding `style=`. 

... From a technical perspective, if you stick roughly to that ideology your code will be more maintainable.

... That's all author advice, though. Like using the right semantic element means you get keyboard events etc. for free. But we're in the business of giving spec authors advice, not web authors.

... Some sort of positive guidance is useful. Design overview, capability breakdown of different layers. Also some negative advice, pointing to negative examples.

... e.g. `dir` in CSS. Weird interaction between content and style. If text is right-to-left, and you change what styles are applying, you should probably still be able to read the text. 

Alice: HTML `dir`...?

Tess: Right, that's one of the ones where it's an input into the CSS property.

... What are the layers we need to describe? Markup, Styling, Accessibility, 

Alice: JavaScript for interaction, dynamic content...

Tess: What about things like replaced elements - images, media, embed/object? Markup with extra behaviour.

Alice: accessibility is more of an output, like rendering is an output.

Tess: I'd be tempted to replace markup with DOM, or Structure.

Alice: what about `hidden`? 

Tess: A lot of arguing about it has been a bit noisy. It's an attribute in markup, the reason you use it is for the default styling. If hidden didn't exist, you'd do it with a classname. It's a bit of a pave the cowpaths kind of thing.

Alice: `pointer-events` in CSS is probably a good negative example. Can we dig into why it's bad?

... the cascade has become a popular way to solve problems beyond appearance, which is beyond the original scope of CSS.

Tess: The temptation for adding features that change behavior (as opposed to appearance) to CSS was partly because selectors are a convenient way to find the things whose behavior you want to change. But these days we have `querySelector` and `querySelectorAll`; CSS and JavaScript have equivalently-convenient ways of finding the things you want to muck with.

Alice: An imperative API for animation didn't have an integration with the prefers reduced motion preference, and suggested `matchMedia` was the right solution. I disagree.

Tess: I think `matchMedia` is the right solution. `matchMedia` is the interface that scripting has to that preference. Timing matters - if CSS and JS have different views on that preference simultaneously because the underlying preference changes by style recalc hasn't happened... using `matchMedia` means you have a consistent state of the world. 

... e.g. you might have an animation in CSS, and script is checking for the preference and adding/removing the classname.

Alice: Adding the classname will trigger style recalc...

Tess: Hm. If you add something to the web platform that exposes something that's already exposed via a media query, the timing shouldn't differ.

Alice: Providing something via a string based API sends a signal that it's the wrong layer.

Tess: `matchMedia` isn't reaching into CSS, it's interacting with the same underlying data that `@media` interacts with.

... layers are structure (DOM), style (CSS), behaviour (JS).

Alice: Outputs are appearance (rendered view), accessibility, interaction.

Tess: We can write a guide that starts something like "you're trying to add a feature that does X, here's where it should go".

... layers within layers, e.g. `input` element. That involved a lot of mistakes. Attributes shouldn't fundamentally change *what* the element is. So saying "this should be in markup" isn't enough.

Alice: We talked about extensible web... our (TAG) guidance was that we should focus on primitives. That seems to essentially deprecate HTML.

Tess: ... high level vs low level features... we found an earlier discussion that we can base a PR on.

Alice: We wanted `inert` to be in HTML for 2 reasons: it should inherit via the tree rather than via the cascade, and it affects behaviour but not appearance.

Tess: Part of what we often encourage authors to do... your markup is your "default"; when you load script afterward, you can change some of those defaults depending on browser state etc. `inert` should be in HTML... before my script loads, but after my initial document has loaded, the stuff that should be inert should already be `inert`.

Alice: `display: none`?

Tess: Right, which is why we have `hidden`. I can add script that reasons about the state of the world and adds/removes those attributes.

Alice: So we're getting back to SSR/progressive enhancement. There's a reasonable argument with `inert` that for things like moving things into overflow menus when the screen size changes, that `inert` should go along with that.

Tess: My intuition is that that kind of responsive design shouldn't change the functionality of the page, but just the appearance. If I wanted some behaviour to change on some breakpoint, I'd use `matchMedia` rather than the stylesheet. Unfortunately that entails duplicating the breakpoints.

... If I'm mucking with e.g. `pointer-events` in `@media` blocks, that doesn't seem right either. But that gets back to discomfort with `pointer-events`.

Tess: Perhaps we need to acknowledge the trade-offs. If it's a sufficiently interesting feature, the result might not be perfect. I think `inert` is in the right place, even though as a result you might need to duplicate breakpoints in script.

Alice: we might also need to address the misconception that "everything" should be in CSS, and that if it requires writing JS then it's broken somehow.

Tess: Right, some places don't allow designers to write JS. That might be behind trying to cram everything into CSS... they think people don't want to write script, or can't.


### [How do we balance concerns between interoperability and implementability?](https://github.com/w3ctag/design-principles/issues/142)

Ran out of time before we got to this.

### [☂️ Incorporate a generalization of the "HTML Design Principles" document into our principles](https://github.com/w3ctag/design-principles/issues/160)

Ran out of time before we got to this.

### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)

Ran out of time before we got to this.

## 06a (Tess and David)

### [Storage Pressure Event](https://github.com/w3ctag/design-reviews/issues/533)

David: A lot of security/privacy issues already discussed in the explainer.

Tess: Example in explainer saying that `quotachange` event firing implies that there is storge pressure seems odd.  Presumably the quota could become larger too?  Especially given the name `quotachange`.  Isn't this example bad?  Should it look at some property of the event?

Tess: found issue for that already, linked it.

Tess: Seems reasonable.  I'm all for helping well-behaved sites be well-behaved, but what about less-well-behaved sites?  Often a lot of misinformation and cargo-culting around performance-related things.  What will sites do in rseponse to storage pressure?  Seems like this could help well-behaved sites.

David: There's been a lot of thought that's gone into this.

Tess: Propose close?

David: Sure, so long as we don't give them the impression that they can stop worrying about the things that they're already worrying about.

### [navigator.scheduling.isFramePending](https://github.com/w3ctag/design-reviews/issues/415)

David: We looked at this in Cupertino and it's been pending external feedback ever since.

Tess: Maybe we should close unsatisfied?

David: Let's poke them one more time.

Tess: Okay. ... Nothing has changed in the repository in 13 months. Is this abandoned?

### [IFrame Execution Pausing](https://github.com/w3ctag/design-reviews/issues/369)

Tess: This was waiting on [#397](https://github.com/w3ctag/design-reviews/issues/397), but that's closed now.  We should poke this issue.

### [Don't monkey patch](https://github.com/w3ctag/design-principles/issues/184)

Tess: maybe the positive framing of the principle is about asking for extension points and also thinking about what extension points you need to provide

David: I'm worried about premature extensibility.

Tess: agreed

David: and agree we should also include the positive framing around extension points.

David: "don't do X, do Y instead is useful"

Tess: I'll try to draft a PR for this "soon"

### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489)

Not enough time to give this one a go.







## 08a

Alice & Dan

### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438)

[reviewing state of issue]

Alice: Oh no, links. ... We had that discussion with Brian which made it clear that the links issue 
was not as straightforward... there's an existing solution for links in MathML... One implementation (Moz) supports: any mathml element can take an href.  Question is: do we be pragmatic and say it's a backwards compat issue and people expect this to work even though it messes up the semantics - once something is a link it's not allowed to take a shadow root.   If you add a href into a mthml element that makes it a link but if it's a link it can't have a shadow-root.  Maybe that's OK.  

Dan: mostly this will be an issue for existing content for which shadow root will be less of an issue?  Feels to me like not so much of an issue.

Alice: Sangwhan had a point : if you're linking a variable to a definition of the variable you might need a different approach anyway. Seems like. I can live with any of the solutions proposed.  Introducing the limnitation of not being able to attach a shadow root shouldn't be too limiting or surprising. Not sure about implementability.  If you attach a shadow-root and then put an href on everything in that shadow root will drop off.

Dan: yes that seems logical.

Alice: which should take precedence.  

Dan: So maybe we should just replay this back to the MathML folks and say we don't have a preference.

Alice: the question is: if you attach a shadow root and then you try to attach an HREF, does the HREF just not do anything or does the shadow root drop off?

Dan: Right.  Then I think we should close this in the summary section.

Alice: [left comment](https://github.com/w3ctag/design-reviews/issues/438#issuecomment-697208609)

### [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/545)

Dan: So in your [comment from a year ago](https://github.com/w3ctag/design-reviews/issues/403#issuecomment-527299905) you mention accessibility as one of the areas of concern. It seems from the spec like no work has been done in this area - there is no mention of accessibility in the spec. I seem to remember a separate accessibility requirements document being worked on but there is no mention of this or sign of this in the top level repo. Maybe we should mention this, since the group has asked us for a new review?

Alice: I think we should because it is in the previous review and Brandon specifically said "I think it would be more productive for us to outline our current thinking about accessibility in a separate doc which we'll link here." And that was a year ago and the doc hasn't been linked. And in particular I had some specific questions that weren't answered.  

- *Could the Web Audio, Vibration and Gamepad APIs make use of XRViewerPose to provide this immersive experience? How does that work with the frame-based mechanism for updating the XRViewerPose? Could the explainer (or another document) provide some example code for linking these things together?*
- *For users who require magnification, might it make sense to have an option on the viewport to perform appropriate scaling automatically?*

... Meta point. this is a new technology - the very best time to think about accessibility is when things are being designed.  Not to do so now is a missed opportunity that they maight regret later.

Dan: Agreed. They could at least have a non-normative section in the spec pointing at a requirements doc indicating where this work is ongoing. I know accessibility was one of the work items in the working group, so that work should be surfaced here.

[left a comment](https://github.com/w3ctag/design-reviews/issues/545#issuecomment-697219461)


### [WebXR Depth API](https://github.com/w3ctag/design-reviews/issues/550)


Alice: One initial bit of feedback: would be good to see some non-visual use cases, such as realistic sound effects taking the room geometry into account. This might be useful for low vision and blind people in particular. In general, it would be good to see more use cases which take disabilities into account.


## 09a 

Taking a look at Ethical Web Principles pulls, issues and "Dark Patterns"

### Issue 25

Dan: should it be here or in the design principles... etc...

Hadley: who's responsibility is where?  We have to think about how is this going to be used... we ask them to wargame out different scenarios.

Definition of a dark pattern

Hadley: example of ui elements in title bar... reason it would come to us is that this standard is being developed... we would come back to the standards author and raise those issues. Do we have something in the EWP document to back up our argument?

Hadley: in "control and power" we could put in a reference to misleading UI elements or dark patterns...  A dark pattern in the context of misleading text is complely legit in the sense of application of technology, it's just really bad for users.

Torgo: Permission requests. When we saw an example of a web developer gaming the request, asking the user to click okay to prove you're not a robot and then using that click as a permission for push notifications, when the user hasn't requested that and doesn't want it... What could we have done differently when we developed the permissions model? 

The developer can paint what ever content they want on that webpage. The request itself only says "Are you sure you want this website to send you notifications?" the develioper can make bigger text on the page below it, saying "This is to prove you're not a robot!"

Could the spec be developed in a way that doesn't lend itself to that misuse?

Maybe it's a matter for the user agent developer? 

We could add something into one of the existing statements that reinforces that point? 

Hadley: could it be something for the security & privacy questionnaire - security & privacy & abuse. Add a question : could this technology be used to trick the user?

Torgo: this is relevant: 

2.11. Does this specification allow an origin some measure of control over a user agent’s native UI?

https://www.w3.org/TR/security-privacy-questionnaire/#native-ui

Hadley: i think there should be another question in the questionnaire aout this..

### Issue 19 - explicit examples

Dan: I'd like to keep this document short and succinct. 

Dan: should we instead reference more external docs / work?  Practically, should we put more effort into the design principles?

Hadley: we in the TAG do not have that much experience in ethics but we have experience in what works well on the web and what causes trouble if it's done badly. We have the most impact when we refer to where our authority comes from.  That's the agrument for grounding it in our experience.


Torgo: When we're takling about hte misuse of web technologies, we could reference this incident that happened when web technologies were misused, as reported in the press.

...If someone tried to get an 

... so for example, in the bit about state surveilance we could refer back to the proceedings of the STRINT workshop - pervasive monitoring considered harmful. 

Dan: we could reference workshop proceedings, RFCs, academic papers, etc... but keep the text concise.

Hadley: We might need to add some additional text in the footnote, to tie it all togehter — but I'm generally in favour.

Dan: so use this issue to collect some of these references and then we can make a PR to add them...

Hadley: The distinguishing thing is : is it coming from our community?  Includes some RFCs, papers... but has to be "our community."

### The PR from Tess on pervasive monitoring

Dan: Let's wait for the summary session to merge the PR so we can discuss with Tess. Support but just want to make sure we're doing the right thing in the context of all of the other references.

Hadley: ok.

## 10a

Tess & Dan

### [geolocation](https://github.com/w3ctag/design-reviews/issues/529)

Tess: just a review of changes since last rec - change to only expose it in secure context. That's fine.

Dan: Agreed.

Tess: fixed a bug for callback interface. Adopted some updated webidl. Great.  interesting change: controlled by permissionspolicy.  That seems like a good thing.  4 changes all of which are either cleanup or incremental.

Dan: sounds good to me.  What's the implementation story?

Tess: on permission policy, chromium and gekko both to that. fixing the callbacks: everyone. Fixing the names...  

Dan: Secure contexts?  Are all UAs doing it at this point?

Dan: let's propose to close with a "satisfied" in the summary session.

Draft closing statement:

*Hi, @torgo and I looked at this during our virtual F2F this week. The four substantive changes since you last went to REC strike us as reasonable, incremental improvements. Thanks for bringing this to us for review!*

### [WebXR Hit Test](https://github.com/w3ctag/design-reviews/issues/463)

Dan: [left a comment](https://github.com/w3ctag/design-reviews/issues/463#issuecomment-697604819)

Tess: Not many changes since April...  

[we pinged to find current status]

### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470)

Tess: In July dbaron commented on the explainer...  "Given today's discussion, I think it's likely that the TAG wouldn't review this proposal with the explainer in its current state." 

... no update on the explainer yet.

... I'll write a comment. 

### [XR Anchors](https://github.com/w3ctag/design-reviews/issues/479)

Tess: we commented in may and july - and no replies.

### Ethical Web Principles

Let's talk about this in the summary session.

### Security & Privacy Questionnaire

[we progressed PRs]

## 11a (Sangwhan & Tess)

### [Constant bitrate audio encoding with MediaRecorder](https://github.com/w3ctag/design-reviews/issues/540)

Tess pinged the OP re: her comments from August

[Propose close; Sangwhan to file an issue so we don't lose track of the naming thing]

### [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-principles/issues/157)

[Tess left a comment on the issue, pointing at things that have changed since the laast time we looked at this.]

Sangwhan: We don't have enough examples, both positive and negative examples, to write a principle about.

Tess: Yeah, I agree. Propose close?

Sangwhan: Okay, I'll leave a comment.



## 12a (Alice, Sangwhan, Tess)

### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416)

[We all read the updated explainer]

Tess: re: https://github.com/w3c/editing/blob/gh-pages/docs/EditContext/explainer.md#native-selection-and-caret this seems unfortunate.

Tess: given what the explainer says [about Undo](https://github.com/w3c/editing/blob/gh-pages/docs/EditContext/explainer.md#undo), I suspect they'd benefit from integration with the [UndoManager API](https://github.com/whsieh/UndoManager) (another proposal in the Editing TF IIRC).

Alice: This looks promising, but it's a very complex API and the explainer is quite terse and seems to omit a lot of detail, so it's hard to review the details of the API.

For example: 

> Additionally, the layout bounds of selection and conceptual location of the `EditContext` in the view should be provided by calling `updateLayout`.

```js
window.requestAnimationFrame(() => {
    editContext.updateLayout(editContainer.getBoundingClientRect(), 
                             computeSelectionBoundingRect());
});
```

I'm not quite sure what this is doing. Update the layout of what? Why does it take these two rectangles?

In general, it would be helpful at least if the IDL had extensive comments explaining the purpose of each enum, object and method.

Sangwhan: It's a bit unclear how this would work with RTL languages, since it involves selection and selection behaves differently there. Do you have any thoughts on this?


### [To fulfill or to resolve](https://github.com/w3ctag/design-principles/issues/135)

Sangwhan: Background is that we don't have clear guidance... what to do when a promise successfully "completes".

Tess: This seems like it should be an issue on the promises guide.

All: Go ahead and move it...

Tess: Doing it ... there is also already a similar issue on the promises guide. I'll link the two.

Sangwhan: I'm also interested whether we're referring to the Promises guide in the right places in the design principles.

Alice: So do we pretty much want to pull [states-and-fates.md](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md), plus code examples for each of the states and fates, directly into the Promises guide, as a guide on terminology?

Tess: Sure.

[everyone makes Promise puns]

Sangwhan: I think the main cause here is confusion between all the terminologies. 

Tess: Right, it seems like there needs to be all these extra terms because of promise chaining.

### ["Cheat sheet" for reference during design reviews?](https://github.com/w3ctag/design-principles/issues/154)

Alice: Could use the first sentence of each principle once all the rewrites land.

Tess: I could take my script for the S&P questionnaire and try adapting it to the design principles to see how hard it would be.

Alice: Probably want heading, first sentence, link to design principle.

Tess: I'll take that action. Assigning myself.




## 13a 

Sangwhan & Dan

### [Miniapp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523)

[reviewing progress]

Sangwhan: not much has changed recently...

Dan: is the "Worker" a ServiceWorker?

Sanfwhan: no doesn't look like it [leaves a comment]

Dan: [asks for a general update]

### [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524)

Dan: If they are going to give input into Web App Manifest as an extension...

Sangwhan: We should say "we would like to close this - for now we have provided our feedback. When you want us to take a look at the next revision / Miniapp extension, we can re-open."

Dan: should we close or not?

Sangwhan: there's no way dor the requsster to reopen...

Dan: so maybe leave open but "pending editor update", "pending external feedback"

### [adding new media formats](https://github.com/w3ctag/design-principles/issues/171)

Sangwhan: 2 things here - [new ways of fetching](https://github.com/w3ctag/design-principles/issues/171#issuecomment-617779337) ... related to https://github.com/w3ctag/design-principles/issues/157 issue Tantek brought up...

Sangwhan: best course of action is to draft some text:

--

#### New Data Formats

Always define a corresponding MIME type and extend existing APIs to support this type for any new data format.

There are cases when a new capability on the web involves adding a new data format. This can be an image, video, audio, or any other type of data that a browser is expected to ingest. New formats should have a standardized MIME type, which are strictly validated. While legacy media formats do not always have strict enforcement for MIME types (and sometimes rely on peeking at headers, to workaround this), this is mostly for legacy compatibility reasons and should not be expected or implemented for new formats.

It is expected that spec authors also integrate the new format to existing APIs, so that they are whitelisted in both ingress (e.g. decoding from a ReadableStream) and egress (e.g. encoding to a WriteableStream) points from a browser's perspective.

For example. if you are to add an image format to the web platform, not only do you need to add a decoder (and presumably an encoder) for said image format to support HTMLImageElements, but you are also expected to add support to egress points such as HTMLCanvasElement.toBlob() and HTMLCanvasElement.toDataURL().

--

[new text written and new design principles issue created]

## 15a (Hadley & Tess)

### [guidance on use of JSON-LD?](https://github.com/w3ctag/design-principles/issues/128)

Tess: This is like polyglot HTML, where you can process it as HTML or XHTML. It leads to interop problems. Authors may test this with one kind of processor, and miss that the other one may not like it. 

In practice, neither processing model is the real one that needs to be used if you encounter these things in the wild. We end oup having to write a new processing model that says, "If you see soemthing that looks kind of like this, then do this..."

Specific worry here: processing JSON-LD as JSON or JSON-LD is htat the resolution of nanmes is different. JSON you'll get the global names, and JSON-LD you want. Clain is it's okya, but I don't think so.

A lot of people will add stuff to make it JSON-LD, use the JSON processor, and forget it. And then that boilerplate gets out of date. Downstream from them, consumers of hte document they've written will start encountering bugs. They'll report it upstream, and that person will say "still works in my software".

So I think that's what David's point boils down to. Not about JSON-LD specifically.

Hadley: That was my initial impression too. And then the issue went on to other things.

Tess: That's fine, and maybe we should talk about webIDL somewhere else. But I want to talk about polyglot formats. 

Hadley: And it's not realistic to ask a developer to keep an eye on stuff that is irrelevant to whether their site works.

Tess: I'm sympathetic with David's conclusion. You release a new browser, and that new browser has direct support for new kidn of JSON-LD document, and the new browser processes it as JSON-LD, not JSON.

The website serving those things will have to work with older browsers too.

So... you could do feature detection, see the browser doesn't ahve support for this, and you just fail. "This website works best in $namedBrowser"

Another option: write a polyfill in JS, and serve that to older browsers. Now you're doing a lot more work, maintaining that. Or keeping a 3rd party library... your site is more complex.

Third option: you could say "whatever. Older browsers still have json.parse. So I'll just write for ordinary json processing when that happens."

Agreed: move the webIDL conversation to https://github.com/w3ctag/design-principles/issues/216, so we can investigate whether we think webIDL needs updating.

We'll create a new, broader issue on to recommend not creating polyglot parsing, more broadly.

And we propose to close this issue.

### [Referrer handling - default policy and capping](https://github.com/w3ctag/design-reviews/issues/538)

Ran out of time before we got to this.

### [HR review of IMSC 1.2 FPWD](https://github.com/w3ctag/design-reviews/issues/474)

Ran out of time before we got to this.

### [Pointer Events Azimuth Angle and Altitude Angle](https://github.com/w3ctag/design-reviews/issues/537)

Ran out of time before we got to this.

## 17a (Peter, Tess, and special guest Pete Snyder from PING)

### Front-to-back revision effort

#### PR [Revise 2.6 for clarity](https://github.com/w3ctag/security-questionnaire/pull/98)

Tess: I think we can just merge this.

Pete: Yup!

[Merged]

#### PR [merge questions 2.1 and 2.8](https://github.com/w3ctag/security-questionnaire/pull/100) fixes [Consider merging or retitling questions 2.1 and 2.8](https://github.com/w3ctag/security-questionnaire/issues/97)

Pete: Isn't this the one that Sam looked at the other day? He wanted us to instead work this into the introduction.

Tess: Oh right, good point. Let's hold off on merging this.

Pete: I'll mention this on the issue.

#### PR [editorial + sec/priv sections rewrite + howto rewrite](https://github.com/w3ctag/security-questionnaire/pull/103)

Tess: Dan and I reviewed and approved; WDYT?

Pete: LGTM. Let's merge.

[Tess resolves conflicts and merges.]

#### ["feature" or "specification"?](https://github.com/w3ctag/security-questionnaire/issues/105)

Pete: I can do this while I'm working my way through the whole document anyway.

Tess: Okay, great!

#### [2.9 (script loading) needs wrapper text](https://github.com/w3ctag/security-questionnaire/issues/104)

Tess: I'll fix this when I get to it in my rewrite. Assigning to self.

#### [2.16 (relaxed-sop) what are the bullet items?](https://github.com/w3ctag/security-questionnaire/issues/102)

Tess: I'll fix this when I get to it in my rewrite. Assigning to self.

### New content

#### PR [WIP: Initial attempt at addressing issue #96](https://github.com/w3ctag/security-questionnaire/pull/99) fixes [Lessons from sharing URLs](https://github.com/w3ctag/security-questionnaire/issues/96)

Tess: Please review this PR & pay particular attention to mt's comment.

Pete: Okay!


## 18a

David & Sangwhan

### [CSS page-orientation descriptor](https://github.com/w3ctag/design-reviews/issues/515)

David explained the rationale for the feature, that it's small, etc.  I don't think this needs a bunch of TAG time; I think it's fine and we can close this issue.

### [should provide advice on when it's good to return the same object again](https://github.com/w3ctag/design-principles/issues/46)

Sangwhan: This is related to #70, which I already have some text for.  I could add some text for this to that PR.

(some discussion of the existing comments in both #46 and #70)

(editing of proposed text for addressing both of these, which Sangwhan will put in #70)

### [Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes](https://github.com/w3ctag/design-principles/issues/41)

Didn't get to this