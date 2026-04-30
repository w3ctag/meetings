# TAG Minutes - Week of 27 April 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/04-27-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

## Pacific Breakout (Asia / Australia / West America) - [2026-04-29](https://www.timeanddate.com/worldclock/converter.html?iso=20260429T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Brian, Xiaocheng, Jeffrey, Philip Rogers

Regrets:

Scribe:

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh; Proponent attending

Philip: Responding to the [minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/03-30-minutes.md#design-reviews1204-incubation-html-html-in-canvas-github---matatk-xiaochengh). When you use canvas, you opt out of all the default web platform features, like accessibility, selection, zoom, translate, agents. HTML in Canvas enables authors to use the web platform in canvas. So they don't need to reinvent them. Comment around privacy implications. Unfortunately, there's not a high-level design to use here. Case-by-case. e.g. forced-colors mode. Could choose to expose it or not-expose it. Is the new information and fingerprinting worth the benefit to users. In none of the cases is it an easy decision. For forced-colors, it's already available in canvas, and we expose it. But others are case-by-case. How we got where we are. Started with the design engines use for drawing SVG. Can hack using SVG foreign objects. Browsers have had to deal with it. I did it in chrome and WebKit. Built up knowledge. Have to re-evaluate, but can start there. Looked at how things rendered in different engines. Thought about everything with this tradeoff: privacy, cors, revealing themes, etc. Made a decision for each one, and iterated. Internally, with Google security team, spec process, and with AI. Ended up with the list in the explainer and spec. Not perfect, but that's how we got there. What do you think?

Xiaocheng: That sounds very nice. You mentioned a high-level principle of the tradeoff between benefit to users and privacy risk. This is reasonable. 

Philip: History wasn't available when you reviewed, and it's been changing. Current ability to draw with SVG foreign objects is widely used. Doesn't allow drawing interactive content. So interactive privacy issues are all new. Another small note: we filed a spec issue to take the findings from this, and use this for the foreign-object security model to improve interoperability for SVG foreign objects.

Xiaocheng: Think the foreign object hack was mentioned in the explainer. Very important, and we want to do better.

Philip: Some people wanted to take it away after we learned about it, but the use counters say it's too popular.

Marcos: Isn't that somethingw e should fix at the web platform level? Should be uses for canvas for certain things, and sometimes you want buttons, but if there are other cases where we should push up the chain, due to interop issues and rendering text. Shoudln't be in the domain of canvas.

Philip: If you draw foreign-object into canvas, there are browser differences around, e.g. scroll bars. We should all agree about thre tradeoffs for that case. Kind of thing we want to bring back around foreign-object. If we agree on html-in-canvas tradeoffs, we can tighten interop  for foreign-object too.

Marcos: They'll look different regardless due to platform differences. Want to keep those. Having those cases pointed out ... e.g. draw whatever you want as a scroll bar but make sure it's at least this size. Interop: have to weigh against privacy implications. Fingerprint pretty heavily with this. Might be enough motivation to shut it down. Hopefully not.

Philip: Fingerprinting issue is top of mind. Pragmatic issue: it's easy to jam a bunch of stuff in canvas, and hash the pixel data. We shoudl be careful. Most of the issues here are already available. You have text drawing in canvas, so you already get fonts. Shaping. Exactly how glyphs look, font fallbacks. Not to say we should stop here. Those are out of the bag. Design principle for html-in-canvas is that we should be able to lock things down on a case-by-case basis. If, e.g. ligatures aren't ok, we can disable that for rendering html-in-canvas.

Xiaocheng: How bad is the privacy issue for foreign-object?

Philip: Not a lot of information from foreign-object that you can't get from drawText(). I'm not authoritative, but drawText() API is the primary fingerprinting issue. New information like buttons isn't bit. 

Xiaocheng: visited colors?

Philip: We lock them down in foreign objects and HTML-in-canvas.

Jeffrey: The ability to lock things down one at a time makes this feature align with https://www.w3.org/TR/privacy-principles/#unavoidable-information-exposure.

Philip: Interactivity: If you expose HTML in canvas without interactivity, it's dangerous in a lot of ways. E.g. accessibility. If you draw a button that's live in DOM, accessibility tree thinks it's live, so it should be live in canvas. Text selection also needs to work end-to-end. Overall issue is top request from people prototyping this early. Drawing forms into canvas is extremely hard. Tracking typing, backspace, arrows, needs building a whole browser. 

Xiaocheng: Understand the motivation. Is this really achievable, or do we need more restrictions to make it feasible? E.g. interactivity is tricky ..

Marcos: Poor PEPC people want to render browser-secure UI, and it wouldn't work with this. When you drop it, it reveals permission state. Can't render it. Assume they've come to you. On WebKit we can't use PEPC buttons in canvas since it circumvents whole PEPC thing.

Philip: We have an answer for that class. There are similar issues with, in a normal <select>, with the popup drawn by the OS. Popups don't draw into HTML-in-canvas. Text IME doesn't draw into canvas. Browser security popups. Nothing cross-origin.

Xiaocheng: Another canvas?

Philip: Another canvas is ok, but we lock down nested html-in-canvas.

Xiaocheng: Interactivity: apply transform matrix to element. Feels hacky. Wondering in general if interactivity is feasible. What if we draw it twice? Canvas has multiple child nodes, drawn in non-DOM order?

Philip: Today, if you draw an element twice, and we return a transform from the drawElement API, and there are equivalent ways to do it in WebGL and WebGPU. Then we update the DOM's transform to match. Only 1 DOM, so only the last is hit-testable. It's an anti-pattern. 

Xiaocheng: In one of the demos, something is drawn ...

Philip: We have a cube demo, which we should remove. Antipattern. That breaks the whole idea of accessibility. Which is accessible/live? This API has grown, and this example is carried over from an old version. Another issue was the ordering issue. That's tricky since you need to sync the DOM order with what you've drawn. Have a proposal in the issue to make that easier. When you're drawing an element into canvas, you can make the decision about the transform, but can't decide about the DOM ordering. Doing this nicely requires a follow-up change. Have a pretty clear, but it's a problem now. Another issue was that transform sync'ing seems hacky. Frameworks: if we automatically set the transform, can break virtual DOM. Need author to be in the loop for the transform setting. Also trying to build the lowest-level primitive. Possible today with filters. Also can draw 0 times with opacity:0, which is hit-testable but not visible. Not good, but worse to try to lock down the API super hard. E.g. drawing element twice: if someone's trying to make a sprite-sheet, it would break the use case. Not locking things down until we see problems and what authors are doing. There is a footgun. Even if you lock it down fully, you can draw to canvas, read, and then write it again.

Xiaocheng: IIUC, goal here is to maintain interactivity under "correct" usage. 

Philip: Interactivity by default. Another example: browser can translate. Without interactivity, if the user clicks 'translate', text won't translate. Need to have the whole thing hooked up to have a real web platform in the canvas.

Xiaocheng: Good answer. More hypothetical: we restrict interactivity to correct usage. Will this lead to, in the future, people say this isn't interactive enough, and let's add a new version? E.g. HTML in canvas is interactive only if it's used correctly. In the future, people find incorrect usage important and also want to support interativity. How likely?

Philip: Very possible. E.g. a game uses a sprite-sheet to stamp out buttons. Now they want to make the buttons live? Encourage author to update the DOM and have multiple buttons in the DOM. When authors can make DOM match, that's ideal.

Brian: Things you're saying aren't drawn to canvas, are htye not drawn period, or are they potentially layered above the canvas and not read-back-able? Things you've marked sensitive, like pseudoclass spelling/grammar error aren't read-back-able even in CSS. I can imagine still drawing them, because the use cases you're describing, editing+selecting text, if you don't have those, people will recreate the universe to get them.

Philip: Get that. If you can't draw spellcheck markers, that's clearly useful. Each of these has to be considered case-by-case. When they're drawn into canvas, they're fully exposed. Can't use tainting that's sometimes used for cross-origin things. Spell check reveals the user's dictionary.

Brian: Only if you draw it to the canvas. Can you provide those things on another layer, tied to the canvas, but not written into image?

Philip: Autofill: Browsers when you click a form element, you get a dropdown with, say, your name and your alter-ego. When you hover and it previews, that's super sensitive and not visible to Javascript. So you draw those previews on top, like you draw selects. So that's a way out.

Brian: That's the answer. Suggetion is you can draw them, but only above the canvas.

Philip: Spell check markers would probably break layering, so I've chosen not to drawn them, but autofill is already drawn above the DOM. Tooltips too.

Xiaocheng: Timing of paint event: Explainer is pretty vague: says if anything changes. Some changes can be processed completely off the main thread. Wondering if these have to trigger paint, would this be not implementable in a UA that processes such changes entirely off the main thread?

Philip: Canvas is inherently main-thread, so everything drawn in html-in-canvas has to be tied to the main thread. Canvas apps are 100% main thread, and html-in-canvas can't fix that, so drawing there ties things to the main thread. We talked with other engines about whether they could implement this. Have a proposal and a follow-on to support threaded effects. Could go into detail. Current API shape is 100% main thread, like canvas.

Xiaocheng: Are off-main-thread APIs supported? E.g. Video playing in canvas, shoudl I fire a paint event every frame?

Philip: Yes. 

Xiaocheng: Have to hook changes from different thread to main thread.

Philip: Also need this hook if you're drawing video into WebGL.

Dan: Confidential information: why can't the developer opt into tainting, e.g. no read-back?

Philip: Can't do it because in the interactive case, need to draw into canvas and be able to tell JS when to redraw. Invalidation. And that can't support tainting. If we draw an input box and draw squiggles. Can't tell JS to redraw without revealing the thing we don't want to tell them. Interactivity blocks tainting. What if we allow cross-origin iframes but didn't have onpaint? They'd change but wouldn't appear changed.

Jeffrey: If canvas acquired someday an async interface, could this start supporting off-main-thread html-in-canvas?

Philip: Spent so much time for threaded scrolling; sucks to throw that away. Say the 2d canvas recorded everything it drew, and when you get to a scroller, it could replay the canvas on another thread. We think there's a path, but it's vaporware.

Xiaocheng: Thank you for coming. I'm very excited about the proposal, but have to play adversary here. 

Philip: Thanks for looking closely.

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu
* [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu
* [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu
* [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu



### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan

jyasskin: bkardell had asked some questions on slack - I'm honestly not sure how people discover or expect to discover skills

marcosc: I like some of the voice, don't answer questions - it probably needs a broader scope like who should they concsider working with in terms of working groups or some of our other prinicples or design refs. I think we could put in some more robust anti-hallucination things. The interesting thing is who bears the cost for actually running it. In the AC mailing list there is "how do wesupport open source projects". GitHub blesses me with free access- I didn't realize everyone didn't get it. If the W3C could throw some money to support that or something, that would be helpful.. I am excited to try it out though.

jyasskin: In response to who pays to run it - a lot of the people creating explainers work for MS or Google - they can definitely afford to ... anyone who is independent could probably ask someone else to run it...

marcosc: We could automatically run it on submission... 

jyasskin: I don't know that that wont be noisy I don't want people to go back and forth with a bot...

marcosc: I don't think they can do that...

jyasskin: I prefer to not do that onthe thread.

Brian: This is what I was getting at on Slack. How do we envision this working, if I'm making an explainer, I do it in Igalia Explainers. Webkit has one, WICG. There's no "this is where you do explainer" place. Some are by big companies. Some by small. End of the day, you submit it somewhere. I was thinking it's mixed. You'd like to give them the opportunity to run it and get feedback offline before submission. Would be useful. But running it on submission. Maybe we run it on the private one. I like not making people feel like they're getting AI feedback. So would be great it whatever this comes up with, we can quickly edit and approve to send.

Marcos: It's not for us. Having a preliminary check; the bot just points things out. It's pre-commit. Will be commonplace that this is the thing, but it's a cultural adjustment. I'm used to it, and I expect the bot to yell at me before I submit real work. It's for us to be comfortable with its feedback, with enough warnings. "This is a bot giving you feedback; did you think about these things?"

Brian: As someone with an explainer, I can take this and reference it in my own igalia-explainers skills. If we merge this, I can put it as a precommit hook on my own explainer in my own repository. 

Marcos: This is the processing we haven't set up properly. What's the right way to 

Xiaocheng: good idea to ask them to run this on their own, instead of worrying about our own infrastructure. This is a good starting point. It avoids infrastructure issues and controversies like whether the bot represents the TAG. Can add more disclaimers or instructions. "Do this on your own to improve your explainer, but it's totally optional. And it won't affect our review process."

Marcos: Drawback is that we don't get to see what the bot wrote. 

Brian: Igalia could use this for our explainers, and I'll guinea-pig it. Can iterate a few times before we recommend anything.

Marcos: Brian and I and Jeffrey can iterate. I'll send an updated proposal that covers more areas.


### [design-reviews#1213: Question: Capability Delegation stalled -- specs are implementing local workarounds](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1213) ([Github](https://github.com/w3ctag/design-reviews/issues/1213)) - @jyasskin, @hlflanagan

jyasskin: Updates, or do we just go talk to specs?  
<crickets>
jyasskin: Ok, I guess we need to go talk to them

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

jyasskin: Marcos, did you have any updates
marcoscaceres: <looks>... I cannot recall where I was in this. I had opinions but I can't find them at themoment, I will try to come back to them

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

jyasskin: I captured a proposed feedback that I thought distilled them - does it work?

marcoscaceres: I think the intention is there, but let me have another read and I think it will probably be ok

jyasskin: If you approve, go ahead and post it.


### [design-reviews#1196: [wg/webperf] Web Performance Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1196) ([Github](https://github.com/w3ctag/design-reviews/issues/1196)) - @jyasskin, @marcoscaceres

jyasskin: You had proposed a draft, I had a minor nit - if it is ok, can you please go ahead and post

marcoscaceres: Yep


### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @dandclark, @xiaochengh

jyasskin: dandclark just commented on this right before the meeting, are we ok with that?

xiaochengh: That looks good to me

jyasskin: Marcos did you have concerns?

Marcos: No
 
jyasskin: Ok, go ahead and post...


### [design-reviews#1211: [wg/webauthn] Web Authentication Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1211) ([Github](https://github.com/w3ctag/design-reviews/issues/1211)) - @marcoscaceres, @hlflanagan

jyasskin: I see there is discussion with marcos and heather - do you need more time?

marcoscaceres:Yes, we'll keep discussing.

### [design-reviews#1194: WG New Spec: HDR on the web (CSS, Canvas, WebGL, WebGPU)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1194) ([Github](https://github.com/w3ctag/design-reviews/issues/1194)) - @jyasskin, @xiaochengh

jyasskin: I will go ahead and post what is drafted there unless someone hollers, because I was supposed to post it before... no objections, sorry for the delay.
    

### [design-reviews#1210: WG New Spec: Programmatic Scroll Promise](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1210) ([Github](https://github.com/w3ctag/design-reviews/issues/1210)) - @xiaochengh

jyasskin: I see xiaochengh and I were going back and forth on theprivate thread - how are people feeling about this?

marcoscaceres: 
    
xiochengh: I think that's ok, I was a bit nitpicking. Maybe we can say we discussed whether this should be a promise or a callback and here's what we decided.

jyasskin: sounds good, go ahead.


## Atlantic Breakout (America / Europe) - [2026-04-29](https://www.timeanddate.com/worldclock/converter.html?iso=20260429T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Lola, Matthew, Brian, Yves, Luke (partial)

Regrets: Hadley, Heather, Christian, Ehsan

Scribe: Matthew

### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin

Jeffrey: I filed the Infra issue. Anne would prefer to keep the primary definition in Infra as he wants to reduce the number of documents people have to cite to get their basics. That seems reasonable to me, but means we'll have to send PRs to Infra as we update this doc. Posing to the group: does that make sense?

Lola: Why wouldn't it make sense?

Jeffrey: It's a little extra work for us. I think it does make sense, but wanted to check with the group.

Lola: Any concerns?

Brian: Makes sense, but the primary idea of creating this doc was to define this here.

Jeffrey: Anne was happy with Infra pointing to this doc - so short definition in Infra, and we elaborate with all the duties and everything here. If people think we shouldn't work on it given that constraint, speak up.

Brian: It's an interesting document, but it's a little less critical to me. I would prefer to not abandon it, but maybe we can bump the priority down. It seems interesting and useful to the ETSI work though. Simone and the WebViews people may have input to it? So maybe that contradicts what I said about priority.

Yves: The document we have currently is far too long to be included entirely in the Infra spec. Having a short, crisp, definition in Infra, we can work with Anne, and then this document with the background is beneficial.

Lola: There's precedent for such pointers to other specs for more details. I think this is a good idea.

Jeffrey: Also wanted to point out [Mark Nottingham's blog post](https://mnot.net/blog/2026/agents_as_collective_bargains) about UAs being mechanisms for collective bargaining. We had a section about this in the doc which was not sufficiently fleshed out, so we [deleted it](https://github.com/w3ctag/user-agents/pull/24), but I think it'd be useful. I am not sure if I'll find time to incorporate it.

Lola: Are there any dates we need to be aware of?

Jeffrey: Don't think anything is time-critical.

Lola: Are we de-prioritizing the document?

Jeffrey: Let's make changes as we make changes. Other documents may well be more urgent.

Yves: We asked around for definitions, and we should. We should check if anyone is waiting on us, and ask if they want to contribute.

Brian: When we're talking about priorities. If you look at TAG Findings historically, they don't come out at a fast and furious rate. We're working on a number of them, and in order to finish any of them, I think we need to focus a little bit. UAs Finding is interesting but we should focus on less things.

Lola: Agree in general. However since I've been on TAG we've only pubished 2 things, so not that much, and have had a lot of work in progress that it'd be good to finalize and publish. Would be good to publish more stuff.

### [explainer-explainer#38: Recommend two structures for organizing alternatives considered.](https://github.com/w3ctag/explainer-explainer/pull/38) - @jyasskin, @matatk
* [explainer-explainer#34: Structure alternatives as: Alternative → Pros → Cons → Reason for rejection.](https://github.com/w3ctag/explainer-explainer/issues/34) - @jyasskin, @matatk

Jeffrey: Matthew was happy with the PR. I made a change after David Baron's review to say that if one alternative is clearly worse than another one, you don't need to go through all the subsections again. I also noticed 'pro' and 'con' may be obscure language and we should use 'advantages' and 'disatvantages'.

*Group agrees*

Jeffrey: Will make that change and merge.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Lola: At the f2f I agreed to chair the group as an experiment, but I don't think I'm going to have capacity to do that, as things have changed. If someone else is up for doing that that'd be great.

Matthew: I made a couple changes in line with our discussion about the name of the group. In the Readme. Haven't renamed the repository. It's long, and I couldn't find a way to shorten it. Happy to rename repo if we want. More substantially, we needed to clarify the charter to explain more about how it works. Are there obvious issues? Will look in F2F minutes. I volunteered to co-chair, but we do need another co-chair. Do think it's a good idea, but we need to clarify.

Lola: At F2F, we decided to go ahead as an experiement; next step was to finalize a charter and start inviting people.

Matthew: "Finalize charter" needed us to explain some things.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Lola: Any further issues to add to the agenda?

*not at the mo*

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Jeffrey: if we notice anything, let's post to blink-dev, as the API owner has just approved it to ship. We asked them to make the element, but acted as if we'd approved the design of it, which is not the case - I pointed that out, but if we have comments we should make them on blink-dev first.

### [design-reviews#1209: [wg/ag] Accessibility Guidelines Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1209) ([Github](https://github.com/w3ctag/design-reviews/issues/1209)) - @jyasskin, @matatk, @hlflanagan

Jeffrey: I've been interacting with this a lot from the Google side, but I think TAG doesn't need to make a comment; they are not architectural issues.

Lola: Some of the issues I've heard are around the work they're committing to and the timeframe they're committing to, to do it. It's not architectural, but if they don't deliver, that could have impact. There are a number of people who don't think they're going to deliver to this timescale.

Jeffrey: What could we say about the charter that would help them move faster?

Lola: I think we could encourage them to do less, but I'd have to think about it.

Matthew: I noticed one significant thing that they are commiting to doing less of: 2.x maintenance. This has been a tough balancing act for them: there's a lot of work for 2.x, but 3 is going well. They've said, "We're not going to do anything on 2.x in this charter period, but if we learn that there is more work needed there, then we will invest time for that in the future." I think it's great that they've scoped it in that way.

Jeffrey: Another aspect that reassured me: some people have said it won't be ready until 2030, but the charter says CR in 2028. But a few experienced people talked about how the group tends to spend time in CR to get wide feedback, so that reassures me that the two timescales are compatible.

Lola: So seems not much for TAG to say here. Other avenues for other comments.

Jeffrey: We should decline this perhaps - will draft a comment and run it by Heather.

### [design-reviews#1187: [wg/das] Devices and Sensors Working Group 2026 Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187) ([Github](https://github.com/w3ctag/design-reviews/issues/1187)) - @jyasskin, @marcoscaceres, @christianliebel

*bump*

### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Brian: I think this feature is always going to feel a bit off to me - would be slightly better if it did, as we suggested.

Jeffrey: And I think we suggested, use a `<link>` tag to configure everything.

Lola: The last comment seems to indicate that someone should be drafting a closing comment.

Dan: This was a review, then closed, then re-opened for the question, so does that mean a resolution is needed?

Jeffrey: I think in this case it makes sense.

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Brian: I've continued to have some discussions on this and had a look at the W3C's current catalog of WGs and things, to see if I can figure that out. No updates yet.

Yves: There was a comment from Heather talking about layering things. I'm not sure the originally proposed layers match the definition that we had, but worth exploring.

Brian: Beyond architecture, I think this is relevant to W3C itself (thinking as an AC rep) - it's a little bit like 'Why are we here? Why are we doing this work in this venue, and in this way? Who is "we"?' - but I don't have anything meaninful at this time.

### [design-reviews#1205: WG Revision: MathML 4](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1205) ([Github](https://github.com/w3ctag/design-reviews/issues/1205)) - @jyasskin, @matatk

Jeffrey: This `intent` attribute overlaps with the semantic MathML elements. The explainer says that the semantic elements haven't been adopted in the past 10 years. But they need to say why they think that, rather than proposing a new thing, which we don't know the changes of being adopted.

Brian: Effectively, there was a tool with "presentational MathML" to do what this is trying to do: more or less, to read it correctly. It's unclear how to read some math formulas. Everyone uses the presentational one. The semantic one is alittle deeper in the weeds. It's a little more "semantic web-y" as opposed to light annotation to clarify. The tools that have been used all sort of do heuristic matching. This is used by JAWS and other plugins. The idea with the "intent" is to ust be able to add some clarification with some light annotation. It's more like a presentational hint than a required thing. You *can* make it better. It is currently being used; there is a tool, MathCad [sp?], from Microsoft. I think it definitely stands a better chance of success. That said, I'm not a part of it. We've said "these things are real and in the browser, and these are the speculative things." They have focused almost exclusively on this "intent" attribute, and I get it. The idea, though, is that if it takes off, then maybe we can get it into MathML core in the next version. We have even reserved it as an attribute that could be introduced later.

Luke: My question was going to be which of the designs seems more in-keeping with MathML 4 and the wider web platform, rather than the XSLT version of the web. If `intent` is what is being used in real MathML in the wild, and may be included in MathML Core, maybe that answers the question of what's different between the semantics stuff specified before and what's proposed here. Haven't looked into the detiails but concern about the HTML design - maybe an attribute is OK.

Brian: it's a hint, like ARIA, though it has its own format.

Luke: If you were designing this from scratch, would you make it accessibility-specific i.e. part of ARIA, or does it have wider uses?

Brian: Its primary use is accessibility. It's very well thought-out in a lot of ways. But semantics are semantics. Being able to understand them makes it a better target for AI and other applications. If you can convey semantics, then others can use them.

Jeffrey: It looks like this is not useful for evaluating the math, but this is for presenting it to people. It does seem like they should at least talk to the ARIA WG about how this will integreate with the rest of the accessibility annotation systems. I think you said that MathCat has implemented this; have other screen readers implemented it?

Brian: I know he is working with people from those other groups. He has attended some ARIA meetings. He was at CSUN recently. He's working with a lot of groups. I think they're generealaly on-board. We tried to bring them together when the proposal for HTML was a thing. (It does some wild emedding of SSML in HTML. It's interesting, but it's complicated to serialize.) That was mostly the pronounciation task force. Matthew was involved in that. We tried to bring that to the same group. I encouraged Neil to attend, and we even tried to link them with James Craig who had similar ideas--maybe we do an IPA attribute or something liek that. There are a lot of related questions and problems. They're all a little bit different...

Matthew: https://w3c.github.io/mathml-docs/notes-on-mathml/#notes-on-mathml-accessibility
https://w3c.github.io/mathml-aam/ I was going to ask about how widely-used and widely-supported "intent" was. I have a sense it hasn't been implemented yet. I found somethings outside the scope of this document. They propose to have a "note track" document. It will include a number of things, including a section on accessibility (linked above). It will evolve to include best-practices. There is an AAM document being proposed; Neil and James are involved in it. I don't know how well-supported this is, but they're definitely talking with the right groups.

Brian: the AAMs are more for MathML Core. It's not in MathML core, nbut it could be in the future. I guess the AAMs would work regardless. Probably? The AAMs are generally for binding in HTML.

Jeffrey: I like the syntax they've come up with. Sounds like they've been and are talking to the right people. One tweak with how they're arranging these documents: they have these side documents that talk about the terms they're defining. These should probably be W3C Registries, rather than general side documents.

Brian: So we can say 'continue talking to the right people'

Lola: Leaving it with Jeffrey.

### [design-reviews#1215: [wg/wot] Web of Things Working Group rechartering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1215) ([Github](https://github.com/w3ctag/design-reviews/issues/1215)) - @jyasskin

*bump* 

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

Luke: Need to look in more detail. I think this is one in which the TAG has an important role to play in trying to steer them. This is the third or fourth attempt to try to solve in this problem area. They tend to focus on very scoped use cases, like a submit button, because someone has requested it, and I don't think they're thinking holistically. I think we need to step in and ask them to think wider.

Brian: We're not the first to mention that it's focused on a couple of very specific use cases. What happened to the other use cases? Do you know why, Dan?

Dan: We've had similar feedback coming from WHATNOT calls. The explainer discusses what may happen to resolution when you have a couple of behaviors attached. Most of the behaviors people are interested in shouldn't really be mixed, so they are not expected use cases. The API has been designed with the idea that we _could_ support combined behaviors in future if we find several that make sense to combine. But things like submitting a form, or triggering a pop-up, wouldn't need to be combined. So we are thinking about the future, but catering for what people are asking for.

Brian: It feels like there's a lot in there about 'a submit button' as a use case. There are lots of simple use cases, but I'm not sure they're the most valuable. If we never got that, the web wouldn't end. How does that help me if there are other use cases? I'd like to see some more on that. It may've changed recently.

Dan: Submit is the focus at the moment. There are two goals: (1) create a framework for adding these behaviors generally; and (2) use submit as the first case. I agree maybe the example isn't the best one - maybe triggering pop-ups is a bigger use case. Those would be coming after this. Maybe this proposal should lay out the roadmap, paint what the endgame would look like. At the same time, we have to do something first.

Luke: There's a middle ground between designing every conceivable behavior, than laying out something concrete like just the submit button. Buttons are an interesting one to start with, as there are many overloaded ways to trigger it. Even taking a button element, thinking about the button element and its behaviors more completely (submit vs reset vs commandfor vs toggle, ...) could be useful. What about those future behaviors? Also somethihng that is not a button element. If we had 2 different elements' behaviors it'd make it a lot easier to explain. And explain how those would and wouldn't go together.

Dan: Most of the complex behaviors and interactions you mention apply to a submit button as well as a generic button. Including keyboard activation etc. I'm not sure switching to a generic button makes too much of a difference. I do like the point that something else, like <label>, is quite different, and would prove out the idea that behaviors could work.

Brian: Just having a list of other things you think people would use, like label, and moderately thinking through them, would help demosntrate that they will work. We risk building a solution that is built very much for that weird case.

Dan: The explainer does have a list - might be worth looking there.

Brian: I'd move those from 'future work' to into the design considerations. And show some kind of thought to them that shows we are not painting ourselves into a corner. I'm curious as to why this is the first case, too.

Lola: Encourage you to continue async and devise a comment.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow

Matthew: All I have to do is post a coment. Luke said 3.1 was "okay". There was a recent update, but I don't htink it changes our comment.

Dan: The API owners (one of them being me) just approved this to ship. If we have feedback, it should be shared in Blink-dev.

Luke: The proposed comment doesn't materially change what's shipping. We asked for an update to the explainer. And I think the spatial-navigation thing is important, but it doesn't actually affect the implemented behavior.

Luke: I don't think this needs to go to Blink-dev; I don't think it changes the numbers in terms of shipping. I think it's more about "dotting the I's and crossing the T's", though if we want to post it to Blink-dev, that should be fine.

Lola: Usually we post to Blink-dev in this case. Nothing we comment is going to materially change. If this is just documentation, then I syuppose we don't need to post to Blink-dev. But point #2, involving spatial navigation mode--it might be worth asking that in Blink-dev.

Jeffrey: Posting to Blink-dev is probably a good idea just to make sure that the right people are aware of any question.

Lola: Dan, if you could share that on the private brainstorming just so folks have access to it just in case.

Luke: LGTM aren't conditional on PRs landing, and that seems odd to me. Is there a reason for thats?

Jeffrey: I haven't been paying attention to this one, but that's a decision they make on a case-by-case basis.

Dan: If it might block on feedback from another implenmenter that wasn't addressed, then that might block. In this case, I felt it was good to move forward.

Matthew: I've posted the public comment on the TAG design review thread. I think the only part we would want to ask on Blink-dev is about integration with upcoming spatial-navigation. I don't think that's imminent, though. And I also don't think the documentation part needs to be posted to Blink-dev.

### [design-reviews#1206: Other Spec Review: OpaqueRange](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1206) ([Github](https://github.com/w3ctag/design-reviews/issues/1206)) - @matatk, @lukewarlow



### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

Ehsan has opened issue in Security Group: https://github.com/w3c/security-guidelines-cryptography/issues/20


### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini



### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

*closed*

### Time change for Atlantic

Atlantic meeting will only happen on a weds starting from next week.

## Eurasia Breakout (Europe / Asia / Australia) - [2026-04-30](https://www.timeanddate.com/worldclock/converter.html?iso=20260430T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Ehsan, Matthew, Luke, Marcos, Christian, Yves, Luke, Hadley

Regrets: 

Scribe: Christian

### [design-reviews#1153: WG New Spec: Direction feature for `scroll-state()` query](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1153) ([Github](https://github.com/w3ctag/design-reviews/issues/1153)) - @matatk, @xiaochengh (Pending for 6 months)

Lola: Should we send out a message to say "we are awaiting a reply on this, we are closing this, if you have updates, please reopen?"

Matthew: Sounds good, will do that.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Lola: Had a look at Matthew’s comment, looks fine to me.

Matthew: Wanted to ask if the content being animated would be in the DOM and in the a11y tree. They said that's their expectation. To be able to be animated, it has to be in the DOM, but in would come in there from the outside into the viewport. But they didn't guarantee it. Reason we asked was we were concerned the content should be there. Not sure if we need to press any further on this, unless I'm missing something.

Lola: Ok, we can drop that question (no. 2). Happy with the changes you made regarding the first suggestion.

Matthew: Ok, will post without point 2.

Lola: Yes, consider this a thumbs-up.

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

(Skipped.)

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

(Skipped.)

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: This is a thing that stays on the agenda because we want to add examples for all of the things, but there's nothing to add for this week.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: I would like to add: https://github.com/w3ctag/societal-impact-questionnaire/issues/17

### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel

CL: everything is clear. We have a draft response ready. We just need to post it. So I will post it. 🎉

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

Matthew: I proposed a draft comment. This is about changing the height of a font so that the text is more justified in the container that it’s in, to make sure lines start and end properly. I have some concerns about edge cases. There is cross-engine commitment. Jeffrey put up a comment that seems to be in agreement with my points.

Ehsan: Had a brief look, but didn’t see any privacy section for this. Skimming through the explainer, I believe it can have potential for fingerprinting, given it’s adaptive to various screen sizes. Would love to see their point on this.

Matthew: Agree that’s worth asking.

Lola: They have an issue about a11y open, and it’s still open. What are your thoughts?

Matthew: Largely good, they have done serious work on it.

Lola: So you would draft a comment related to WCAG, baseline mechanics, …?

Matthew: Yes.

Ehsan: Happy to help.

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

Christian: Heather is on this, and was collecting concerns.

Marcos: Think we are waiting for Matthew for a11y considerations. We think it’s quite problematic from that standpoint.

Matthew: I’ve been following this. I think there were good a11y questions to raise. Acknowledge the concerns around interoperability. Don’t have any additional/specific concerns to add.

Luke: (Comment on a11y/interoperability).

Lola: Would encourage you to post that comment. (https://github.com/w3ctag/design-reviews-private-brainstorming/issues/252)

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: Working on a comment. Number of points raised on this. Whatever the default is, it should be accessbile. Had a big discussion whether this is a page feature or UA feature. Wonder if TAG has consensus which of it it is. If it’s a page feature, it falls under the responsibility of authors, considering all factors (dark/light mode, …). And if this is exclusively a UA feature, the proposal isn’t needed. One of the justifications for this was for example :has where table stylings weren’t possible on UA level. So is it page/UA or should they co-exist?

Luke: Think pseudo-elements are allowed in :has. Potential problem with that is not all are allowed and it can go in cycles. What if you display: none the container, and the text can no longer be found on the page? Not sure if that can be worked around.

Lola: Opinions on Matthew’s question?

Luke: It’s a "both" from my perspective. It's a UA-originated feature, but it operates on the page, so I believe it’s ok to allow page authors to have some influence. Obviously we shouldn’t allow it for everything.

Lola: Dark mode is also a UA feature, but also page-controllable.

Christian: Agree to Luke. If engines decide not to support it, that’s also fine. Also feels like a niche feature.

Lola: So I guess "both" is what TAG feels. UAs could also decide to override the author’s choices.

Matthew: Concerned that if this is such a niche feature, developers won’t actually consider that colors work in all the different permutations. There's a risk that this might be broken.

Lola: From a developer POV, this seems like a "nice to have" feature. I feel the color question comes up more frequently. Contrast issues etc. come up really often. Would an extension to WCAG make sense? UAs can always decide to override. Up for the UA to decide whether they want to implement this.

Matthew: Will write a comment, then we can follow up.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Have a proposed draft comment (https://github.com/w3ctag/design-reviews-private-brainstorming/issues/118#issuecomment-4351092299). IT says that we don’t have consensus on this yet. I think I need some more input. Feels similar to popover. Main objection is privacy, usage on XR platforms.

Marcos: Native apps go through an app store review that have privacy gates. Things they can do are restricted by policies. Not possible on the web. Use case is real and we see it on lots of places, but expression of interest is very different between device categories (VisionOS vs phones etc). For example, long press was never standardized. Abstraction of interest might be impossible. Also consider tables that have pen hover support.

Luke: As someone who worked on this at OpenUI. Reason for the design behind popoverhint/interestfor was that it can work on all of those devices. One of the original designs was "popoverhover". It was deliberately changed so UAs can decide what this means for them. We can’t design for platforms in 20 years time. On Android, Long Press is fairly established, secondary buttons. Mainly a thing where UAs have to device what’s right for them.

Marcos: Not getting concrete examples how this would work on VisionOS.

(Discussion about hand tracking, pointers, … on various platforms.)

Marcos: Also, context menus on mobile (usually triggered via long press) which you would take away from users. Users have accustomed to that.

Matthew: Think on desktop-style platforms with context menus, this could be added to the context menu. Other platforms could decide to implement it. Also on iOS, you get a link preview. I hear it’s possible to do on immersive systems, but maybe not on all systems.

Hadley: Enjoyed the discussion. Issue was filed 1.5 years ago. Believe we need to do something. What can we do in the short term?

Matthew: Would like to add some more options. I think I got what we agree on and what not. Looking at the intent vs. looking at the concrete actions seems like a separate discussion. Will take out popover stuff. Will work on the comment and get back to you.

Hadley: Can we get it posted this week?

Matthew: Will do my best.

Lola: Also remember, we can say there is no consensus, given this is open for over a year now.

Hadley: Do we know if there’s any deadlines?

Luke: This is already shipped.

Matthew: Ok, so will post it on Monday at latest.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel, @xiaochengh



### [design-reviews#1187: [wg/das] Devices and Sensors Working Group 2026 Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187) ([Github](https://github.com/w3ctag/design-reviews/issues/1187)) - @jyasskin, @marcoscaceres, @christianliebel



### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow



### [design-reviews#1035: CSS Gap Decorations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1035) ([Github](https://github.com/w3ctag/design-reviews/issues/1035)) - @matatk, @xiaochengh



### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon



### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini



### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Hadley: Had a look at the conversation. My thoughts are: Manifest ID does not have x-vendor support. Believe changing the wording would help. Believe we are not supportive of it, because of SOP. Suggest closing it as unsatisfied.

Yves: Was leaning for unsatisfied because of the exchange part. Thought it was pretty clear in my last message. Use case is good, execution is not good.

(More people supporting going with unsatisfied.)

Christian: Will merge the comments, and if you think its unsatisfied, we can go with that.

### [design-reviews#1214: [wg/math] Math Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1214) ([Github](https://github.com/w3ctag/design-reviews/issues/1214)) - @christianliebel



### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini



## Plenary Session - None

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
