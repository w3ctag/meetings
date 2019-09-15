## TAG F2F Tokyo - Day 2
##### 11 September 2019

Present: David, Peter, Sangwhan, Dan, Alice, Tess, Yves, Hadley

Regrets: Lukasz

Scribe (afternoon plenary session): Tess (& Alice)

---

Agenda: 

## Meeting scheduling

[discussion on future schedule]

## Breakouts

### [Scroll To Text](https://github.com/w3ctag/design-reviews/issues/392)

Alice: Good update from Dave, issues filed on various repos for the URL parsing issue.

Alice: Maybe we can suggest the review change venue for that topic?

Tess: Still the issue of word boundaries.

Alice: Could you give an example of how that would play out?

Tess: Suppose a page sent you a link to a scroll-to-text fragment like "your password is xyz" in a browser which had a poor dictionary implementation - you're then vulnerable to the attack described in the explainer.

Alice: Makes sense. So the spec absolutely needs some language to describe what attributes the dictionary needs in order to mitigate the security risk.

Tess: Let's leave it to David whether he's comfortable closing the issue pending discussion of the URL parsing questions in other venues.

[David would prefer to leave this open]

### [Backdrop Filter](https://github.com/w3ctag/design-reviews/issues/353)

Tess: This is shipped... should we close it as overtaken by events?

Alice: Not sure. We were talking about the question of implementability (Blink and WebKit are unable to implement fully compatible versions of this feature due to existing constraints).

Tess: Right, which is the bigger question of what do we do when different implementors have mutual implementability concerns with competing proposals

Tess: This API makes the authoring experience more complicated, and has the potential to be a worse user experience. 

Tess: There's spooky action-at-a-distance (changing of backdrop root) caused by seemingly unrelated properties.

### Breakout on Process

We took minutes in [this document](https://cryptpad.w3ctag.org/code/#/2/code/edit/vLpYC3TbDmULXJMwSyeGhMf0/).

---

## [Project Fugu](https://www.chromium.org/teams/web-capabilities-fugu) update (Alex)

Alex: Next door is a meeting of 40+ engineers (microsoft, google, intel), the work of which is arriving for TAG review as a set of disjoint explainers

Alex: [Explains a bit of the prehistory of Fugu]

Dan: Are the proposals going to WICG?

Alex: Yes, mostly, though some of them have pre-existing homes (e.g. NFC)

Hadley: what's the logic behind doing this all in one big og?

Alex: Great question. These are not one big project, but independent projects with similar goal, prioritised by partner feedback.

Alex: We don't do rendering, layout, networking... 

Hadley: I still don't followWy toh

Alex: The shared goal is to build trust in the web platform by ensuring the gap between what most platforms deliver and what the web delivers that people can't trust the web ...

Alex: Near competitors to the web, like Electron, or WebView on Android, have capabilities that are missing on the web, so that's our TODO list.

... Another close competitor is Chrome Apps, which was our (Google/Chrome) mistake.

... What are the APIs people most frequently need?

... Next door is an open meeting, so there is an opportunity for you to influence their/my thinking.

Yves: Are all of the new APIs that come to the TAG coming from Fugu

Alex: No, some (e.g. toast) are separate. Fugu is going to mostly ... there is a public tracker that lists the things we're working on.

DAN: You were instrumental in setting up the process of design review on the TAG, and embedding it within the TAG's processes. We're continuing on that tradition. Our stakeholders feel that it has been good. We're continuing to evolve it but we are sticking with the core idea.

.... When we get a design review we don't know if it's associated with that project. Would it make sense to track that? We track things like CSS, ...

Alex: Would you like to know that?

Dan: Might help us figure out who to talk to... i.e. if we can call you to ask for more context.

... We shouldn't treat Fugu requests any differently from other reviews

Alex: We don't differentiate between Fugu and other Blink APIs.

Tess: It's difficult to review a lot of trees when you don't see the forest. Having that context is helpful.

Kenneth: A lot of Fugu features depend on other features - file API..?

Sangwhan: Would make sense to review networks of interdependent features.

Alex: We'll do what you tell us to do re: what to provide in explainer / review requests

Kenneth: Would be good to know what is being actively worked on.

Alex projects the [Fugu project tracker](https://goo.gle/fugu-api-tracker)

Alex: This is our prioritized list of deliverables with timelines. you can search this list to figure out if a review is from us, and to figure out who is working on it

... spreadsheet is updated frequently

... Green bars indicate origin trials, meaning it is launched but only available with a key, which partners have to apply for.

... (Chequered) flags indicate that it is available behind a flag (get it) for developers to experiment/prototype with.

Dan: Where is the information about which standards venue the API is being worked on

Alex: We'll add it

Hadley: Web is a cross-browser project. How does this interface with non-Chrome implementations?

Alex: the standards process [... scribe missed...]

Hadley: We've had a number of design review requests come in on things that haven't even been socialized to other browsers, much less taken to WICG or another multivendor venue

Dan: When we document features in MDN, we look at where something is implemented and worked on...

Alex: One of the challenges we had over the years with the Blink launch process is that the TAG review was quite late. We would have hoped that ideas would have been socialized earlier, and lots of reviews came in after the implementers were willing to change their proposal based on external feedback

... we request TAG review much earlier now, [scribe missed]

... When review comes in really early, you wouldn't expect other vendors to be on board

Dan: TAG could prioritize reviewing requests that have multiple implementor interest

Alex: Lots of the Fugu work is multi-browser (e.g. Microsoft) but single-engine (Chromium)

... We've heard people from other vendors have trouble getting bandwidth to review our work

... Process is run in the open so anyone who wants to participate and has the time to participate can

Dan: When we're looking at incoming requests, we're trying to answer the question: is there multi-implementor interest? e.g. the WebXR request that came in recently. We know there are multiple implementors & implementation commitment from engines.

Dan: So then when we get a request that seems really Chrome specific, we ask the question if it's been socialized with other vendors. Reply "didn't know that was a requirement"

Peter: requirement for standardisation

Alex: Yes, that is well understood.

Kenneth: We could have something in the template about this...

Dan: We decided not to do that, because we don't want to discourage review requests from people working on standards targeted to one engine.

Alex: Everything that happens in this project, we have a goal to work with other vendors. If other vendors want to show up and work with us on these things in WICG they can.

... it's challenging to get enough engineers at other engines to do review

... the TAG ends up as a substitute for that

Dan: We're often the first port of call; we're usually the first people to whom they're showing their work

... it's great to see those requests happening, and we want to be able to help. it would be great if there had already been some public socialization with other vendors before it hits TAG review. One option would be @ wicg ...

Hadley: you can "clear" wicg without having multiple implementations

Alex: WICG doesn't produce standards.

Hadley: do you expect to push these things through the REC track?

Alex: yes

Hadley: it's seemed to me that some stop at wicg

Alex: in some cases you need to recharter a wg to add a deliverable, so it's hard for them to accept new work from wicg

Ken: (e.g. device & sensors wg)

Alex: doing as much of the design at wicg as possible helps clear the deck for moving the work to w3c wgs when ready

Hadley: is there still room for the proposal to adapt after it graduates from wicg?

Alex: by the time you've chartered a wg, you already know roughly what the feature is, use cases are, etc.

... missed ...

Alex: the TAG is getting a crack at things earlier, so you can change it

Peter: My concern is that you go through wicg, tag review, then ship, and only then it arrives at a wg who want to change things and the answer is "no"

Alex: That can happen

Tess: That seems like the likely outcome in this process

Alex: Blink launch process prioritizes solving developer needs. Interest from other vendors can be a proxy for that, prefer origin trials. I don't view it as the highest goal of the process that folks who work on other engines think it's a good idea

Petetr: ??

Alex: We run this process in the open and ask people to collaborate. 

Peter: I'm not criticising... but you do end up shipping ahead of the standards process.

... This has happened on CSS... things ossify.

Alex: We could look at extending Origin Trials ... like with WebVR, we ran a very long origin trial process. Other vendors wanted to ship things they didn't want to standardise.

... We put WebVR behind an origin trial for around 2 years, with 8 or 9 (users?)

... This did effectively prevent burn-in of that API. 

... We viewed that length of origin trial as a failure, we would prefer to facilitate iteration...

Peter: You have a much larger team, and you can iterate on so many things at once... other vendors/groups have a smaller team and can't keep up (?)

Alex: I don't view under-funding of other teams as a reason to slow down.

Dan: You don't have to have everyone in lock step with you, there is a middle ground; other vendors may agree on design without committing to prioritising engineering work for it.

Tess: Seems from the outside like you're throwing spaghetti at the wall to see what sticks, but you're asking us to review all the mid-air spaghetti.

Alex: One of the best benefits we've gotten from TAG review is the negative feedback. TAG has technical and moral authority for teams to revisit theri design.

Dan: That's good feedback.

Alex: Web Audio was reshaped. Web Share Target was another example. 

Tess: Let me try to rephrase that.

... It's not clear how much buy-in or support a proposal from a Blink engineer has when it comes in for TAG review. How do we distinguish one engineer's opinion from something which has significant manager support, etc.?

Alex: List of Fugu APIs has priorities - P1 has a third party support. Not all these APIs are equal. P2, P3 are places where we don't have that level of engagement and support...

Dan: Does it make sense to revive the notion of a priority bit? We've avoided that because we feel like everyone would say their thing is urgent. You could say "use this only if you are a P1".

Tess: That wouldn't generalise outside of Fugu.

Dan: We could map that to other projects. Ask people in our guidance to be judicious.

Alex: Hopefully we've reduced the incidence of urgent.

Alice: I have been getting fewer pings.

Hadley: Where does Fugu fit in to the whole ecosystem?

... We have developers, we have users who are even more important.

... But the web is powered by the decisions by (in the early days) Google, Mozilla, Opera, Microsoft, W3C.

Alex: In the early days people shipped what they thought was right, and then fought over what the standard should be.

Hadley: That's a good point.

Alex: There's a mistaken idea from people in working groups around immaculate conception for features when their working group's idea didn't start that way. There is a survivorship bias. They demand *everyone else* use a process that they didn't. 

Hadley: That is helpful... has Chromium's perspective shifted away from this idea of working with other browsers and engines, to working within the Chromium family?

Alex: We continue to spend at least 2x what any other engine spends, so we've flooded the zone We're trying to work out how to get [the web] competitive on mobile. We have to compete with native apps, or the web doesn't have a path to continue existence. It won't get carried along to the next form factor, or device. We see this already playing out in China.

Hadley: How does that play out in who you work with?

Alex: We need to do work now to give developers what they are going to need in the near future. Fugu engineers are walking through mud in hopes that someone will reach out and offer to help.

Kenneth: People at some orgs have difficulty working on projects... Fugu is easier? More like a partnership...

Dan: We came up with some ideas just now that could help to send signals to help us prioritise and understand the context for reviews, to get you earlier feedback. I thinkn that would be valuable to you... we'd like to see more discussion of early implementer interest even if that's informal. Would like to see priority. Tags and labels.

Alex: there's a challenge that a lot of these APIs are aprtner driven, i.e. an application that can't move to the web until this API is available, which we can't disclose.

... can you help me figure out how to get you the information that you need?

Dan: we will allocate a breakout to have that discussion and come back to you with a process proposal.

Alice: A lot of explainers come in without a clear explanation of the user need. It would be nice to clarify them when explainers come in.

Alex: Okay. I'll send out an email to the team to make sure they use the new issue template, etc.

## Breakouts

### [Wide review request: the HTML Standard Review Draft](https://github.com/w3ctag/design-reviews/issues/412)

Tess: HTML WG wants a review by October. Given the size of the spec that seems tight. What can we do in that timeframe that would be valuable?

... This is 150-200 commits, doesn't seem like we have the bandwidth to do all of that.

... I'm happy to take an action item to go through all the commits since 1/1/19 and generate a set of features in HTML that we should do architectural review of.

### [Scroll-linked Animations](https://github.com/w3ctag/design-reviews/issues/330)

Tess: Last comment was from Travis on Feb 17.

... "dbaron will take a look and circle back at the milestone" where the milestone has been bumped a bunch of times...

Alice: Was assigned to the June 12 milestone, missed out on being discussed at that telcon and wasn't bumped to a later one so it fell off our radar.

Tess: I found their public team minutes doc. 

Alice: Right, last time it was discussed with them was in May. Linked to https://github.com/WICG/scroll-animations/issues/48

✨closed issue✨

## [CSS Animation Worklet API](https://github.com/w3ctag/design-reviews/issues/349)

Alice: This rings a bell... we discussed this in Reykjavik.

... I had some questions about prefers-reduced-motion, you had some concerns about implementability, and a meta-issue about how to track those types of concerns.

... [Intent to ship](https://groups.google.com/a/chromium.org/forum/?utm_medium=email&utm_source=footer#!msg/blink-dev/aRKT0BkrF-8/G-KuTnMBBgAJ) seems to suggest that it hasn't yet shipped...

... We probably don't have much more to add here, though.

Tess: &lt;comments re implementability concerns&gt;

Alice: &lt;closes issue&gt;

✨closed issue✨

