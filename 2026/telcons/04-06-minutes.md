# TAG Minutes - Week of 6 April 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/04-06-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

## Plenary Session - [2026-04-07](https://www.timeanddate.com/worldclock/converter.html?iso=20260407T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Heather, Christian, Marcos, Jeffrey, Matthew, Ehsan, Yves, Brian, François Daoust, Atsushi Shimono, Anssi Kostiainen

Regrets: Lola, Hadley

Scribe: Heather

### [design-reviews#1187: Devices and Sensors WG charter](https://github.com/w3ctag/design-reviews/issues/1187) — with guests from the WG
* Can we categorize the issues into buckets?
  1. The charter needs particular text before going to AC review.
  2. The WG and Team need to make a deliberate decision before going to AC review.
  3. The TAG is merely interested in the outcome.
* One significant issue is the extent to which a browser-focused WG can adopt documents that only 1 browser engine seems likely to implement.
  Can we find any TAG consensus or near-consensus on this topic?

Jeffrey: We're trying to figure out what has TAG consensus, what needs to change, and what we need WG actions on. Marcos has identified the issues we need to discuss in issue 1187.

Marcos: We have consensus on what the concerns are; we don't have consensus on how to solve them. As a start for https://github.com/w3c/charter-drafts/issues/780, read for the proposal. What might be a suitable action in response to the concerns that the use of the wiki and the verifier result is insufficient?

Jeffrey: pointing back to the actual TAG comment, there's not necessarily consensus that these implementations need to support these in these particular ways, but we are more concerned about what support the group will supply to the spec and where it's headed. For the TAG: do we want just these categories, or do we want the spec to say these engines support these in the following ways? I want to hear from the WG what you're thinking about how to signal your spec's support levels. I want to hear from the TAG as to what direction you want the WG to go.

Anssi: What was the key problem the TAG wanted to solve here? 

Christian: Developers could confuse the docs there with formal standards. They might not be happy with current implementation support and draw the wrong conclusions. If the spec authors could clarify that, perhaps by displaying the status more prominantly, that might help.

Anssi: Does the TAG have this type of boilerplate that you generalize across all WGs, or is this WG being treated differently?

Jeffrey: It is a problem that has shown up in a few places. The importance seems to have been higher for this WG. Once we figure it out, we need it shared across WGs and become part of the charter template, once we figure out what should be there. We are asking for the WG's help to figure out what the change to the template needs to be.

Anssi: I would prefer to see a general boilerplate for the charter template that I will see applied across all WG. What was proposed to be added to the text creates more confusion. There is a PR for the charter that is a good solution at this stage when we don't have general boilerplate. 

Jeffrey: The charter text doesn't address the problem that people reading the spec don't know where the spec is going. People don't click over to the charter when they are reading the spec, so something in the spec seems useful. We should put it in the status of the doc via respec or bikeshed eventually, but we need to try it out first. The TAG needs to figure out what to ask you for, too. Using Marcos' suggestion of specifying the engine and their position gives too much weight to the browser engines. The categories listed in the charter content are more general.

Anssi: You are familiar with the MDN data project - it documents support across features. I expect our tools would use that data as a source. 

Marcos: My feeling from what Christian said, a developer might ask why something has not been implemented. It might be nice to have answers to that, which is why I included the standards positions (which MDN cannot answer). If we have standards positions that are clear, these are ultimately web APIs that are supposed to be implemented in browser engines.

Anssi: I think that's an interesting proposal. Would like to lean on François on this. Marcos feels that it is important to have in the spec direct link to standards position. But the spec is fixed and the positions may change over time. Is that ok if that's dynamically fetched? But if the specs are static until the next commit arrives, that might be a problem.

François: I don't have an answer for WG deliverables. Dom and I are working on an update to community grou preports for the same reasons, trying to make clear that these are CG reports, drafts not supported by anyone, and provide more useful info. Part of that info would be in the front matter and would include links to standards positions. But that's easier for CG drafts because they get updated and have no official standing. For a WG deliverable, it will be harder to come up with the right rules, which standard position to link to, and how to present things. We need to get some experience with the CG before we can apply further to the WG. 

Marcos: The challenge with the specs to become standards is that they need to have multiple implementations to exit CR. The underlying intent to having these non-normative boxes is to signal that these are not expected to progress on the REC track due to the positions of the potential implementers. Anssi is right, those positions can change, but we are aware of when that happens and can update the docs when ready.

Jeffrey: This might bring us to the web architectural question. This WG has been operating to push the boundaries of what's possible on the web. It has been doing that when one engine is willing to push boundaries and the other engines thought that was a bad idea. We have the ethical web principle that the web is multiimplementation/multibrowser, but these are not as multi as we would like. A website might be written to use these APIs but would not work on the user's choice of browser engine. We can either remove the feature from the implementing engine, or get the other engines to implement it. A warning at the top of the spec that it's hopeless to complain sabotages the goal of giving developers a path to complain to the browser engines. Do we hold the web back until the engines are convinced intellectually rather than by developer pressure?

Anssi: I think what you described is the essence between WHATWG and W3C work mode. WHATWG mostly works on infrastructure, so it's probably easier to reach consensus across all browsers. But W3C works differently than that, which is not necessarily a bad thing. Someone needs to be the first mover. We are making a disservice for the web platform if we expect all browser to make the investments at the same time. It would be like saying companies cannot roll out 4G phones until all companies support 4G.

Christian: I also believe that single vendors should be allowed to push forward and that normative text is ok. My personal opinion is that we should add the SotD box, it should not be a scary warning, but some kind of fair hint of the status would be good. Anssi had fair points, so the common ground is adding that box with wording we agree on.

Marcos: I don't think it's so binary. The boundary pushing is good but it presupposes that the architectures being put forward area lso good, and the use cases are being addressed in the appropriate way and are valid. For example, with the generic sensors examples, those didn't catch on and we have alternative ones that serve similar purposes. These aren't things taken wholesale. We shouldn't be scaring people with these boxes, but we should be clear about what's being tried and if we can put a timeframe on that. Maybe the use cases we thought about ten years ago when the work started might not fit anymore. 

Brian: I object a little that these are scaring people. We shouldn't think of it that way as much as these are informing people. To the example of 4G, we want people to lead and do early implementations, and we want to let developers know the status. When the status is "we actively oppose 4 G for xyz" that's good to know. I don't think that scares people away from commenting. It might put more scrutiny on the rationale. It gives people a concrete thing to dispute. It should be as clear as possible as to what the status is, and if that includes a particular engine that is actively opposed, we should let people know.

Jeffrey: I hear a suggestion that we have a few categories, and we're focused most on the first two. When there is a spec where, in general, people should use the other spec, people should put that in the document. "If you're thinking of using this spec, you should use that one, this one is just being maintained." Or "This spec is pushing the boundaries; other engines are opposed to it." We need the WG's suggestion on how to put that in.

Anssi: A link to standards positions - I'd like to avoid something that has to be maintained. Will talk to François as to what might be appropriate. I don't want to leave any implementers out, so who should I include? 

Jeffrey: If a browser or engine wants to be in this section and says "please include my position here" there's probably some threshold here where some browsers are too small to matter, but if there's a reasoned explanation as to why even the small browsers won't implement, that's useful. I do want to question how mucha problem it will be in the spec. Yes, when it's a REC, it's static, but CRs are still dynamic.

Atsushi: Can we tie this to spec metadata rather than human readable in the SotD? There is no place in the process to talk about the SotD. Most working drafts don't show status like this. 

François: In the WebDX CG, we maintain mappings between web features and standards positions. We also have a side project collecting developer signals. We got pushback on adding features to the dev signals project about including negative standards positions; they wanted to avoid that push from developers when they feel the tech is not good. We are reconsidering that in the CG so rules may change. Also, links to standards positions seem good, but maybe we can summarize those positions. We did get pushback on that as well; the positions are phrased very carefully and summarization might change that language. I'm superpositive to add info in the spec, but I'm wary of adding this to the charters until we know how to do that and how acceptible it will be to everyone. That's why I want to start with CG then move on to WG. 

Anssi: I'm surprised that developers are reading the specs. The ones I talk to are reading MDN. Why are developers interested in reading W3C specs? My developers don't do that.

Brian: Some developers do that, even if you go to MDN, the spec is linked from there. People give talks or write blogs and link to the specs. That's not how developers learn it or reference it day to day, but they still look at the spec. If it's confusing what the spec is saying, and there aren't good signals, it's confusing for developers. It may also cause unnecessary division in the community.

Anssi: The developers I talk to know where to find positions for browsers. That's why I think this is not a problem. So what really is the audience for this? is it a regulator? This kind of box may discourage people from trying features that are new. 

Brian: MDN itself flags things as experimental or risky. This is the other side of your same argument. Its relevant, and it does not scare them away. 

Anssi: MDN is where developers go, and we'd just be duplicating info. Does MDN link the standards positions? That's where I think developers should go; implementers will go to the specs.

Jeffrey: People writing the MDN read the spec. So this would be sending a signal to people writing that documentation. It is possible that we can stick the info in the doc metadata that can be automatically read by MDN. But I want to get back to next steps for the charter. Sounds like we don't have a full answer before we send the charter to the AC, but maybe the charter can include having the WG figure this out. Suggested text: "The WG will work to add a description of browsers' positions in the SotD of each specificiation"

Marcos: People do read the specs, and this is not new. I worry that leaving it to the WG means it will not get done, which will prevent the charter from progressing because various members will object. 

Anssi: It's up to the members to read and cast their votes.

Jeffrey: I think we should consider as to whether we want our problem. Formal Objections are not always a failure; they allow the council to make a binding position. The TAG needs to figure out if a strong majority feels that we should hold the charter on this or allow it to go ahead with the statement the WG will work on this. 

Heather: For myself, this feels like an area with such history and passion, that I'm hesitant to try to dive in. With no prior views, as long as it's still a dynamic document, in CR, not REC, having a note at the top saying "here's what's what", I don't understand why that's contentious. If that's already in MDN, great. If it's in both, great. Some people look in each place. Belt and suspenders to have it in both places. Don't know why it's a problem.

Christian: I personally would like us to find consensus here. I believe it is possible and not too far away.

Brian: Agree with Christian and Heather. I feel like I don't want to block this forever, but I do feel like there are a number of bullets in here that seem reasonable and we can do better. It's worth taking the time to see how much better we can do. 

Jeffrey: I will re-open this charter review so it doesn't look finished. Anssi, can you organize a WG discussion on this topic? When that's done, we'll re-add to the TAG agenda and we will see what we think of the WG direction here.

Anssi: What is the schedule for the start of the AC review? We can try to do it asynch if we can't find a good time. 

Atsushi: I don't have a strict date right now. Current charter period is extended until end of May. We can think about AC review then. 

Jeffrey: Let's figure this out asynch.

Marcos: We are asking the WG if we're proposing text. Christian can take over as lead person to suggest the text.

Anssi: Let's try with Christian.


### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman



### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh



### Breakout Rollup



## Pacific Breakout (Asia / Australia / West America) - [2026-04-08](https://www.timeanddate.com/worldclock/converter.html?iso=20260408T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Heather, Jeffrey, Marcos, Dan; guest Phillip Robers

Regrets:

Scribe: Heather, Jeffrey

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu

Will come back to this when Yu Sen is available.

### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu



### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu



### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu


### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh
(With Philip Rogers calling in.)

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Jeffrey: there is a lot of discussion on the design reviews that could use clarification. What points from Marcos and Jeffrey make sense? We have problems with their use cases (video sites and AI stuff where cpu measurements wont' be measuring the relevant stuff). They think that its still useful to have this, even though load may slow a computer down; it lets you serve the correct content then use compute pressure to adapt to the current load. Maybe we should ask about whether that actually works and what evidence they have that this does the right thing for sites. 

Marcos: The architecture is not correct. The static model they propose, that they adjust performance dynamically based on a static snapshot is completely flawed. The use cases should be taken to the appropriate groups. For example, the media one should be taken to the media group because it may duplicate things they are already working on. So, refining all the use cases would be good. At this point, very skeptical that this is useful in its current form.

Jeffrey: Should they refine the use cases and come back?

Marcos: And reach out to the working groups, too. 

Heather: What's the point of clarifying use cases if the architecture is broken?

Marcos: If they change to a dynamic measurement, and there are legit use cases, it could be useful.

Heather: Sounds like it would need to be both. Have to fix static vs dynamic architecture.

Marcos: Change wouldn't be dramatic. Field is similar, but gets events or a media query, so it can change every so often.

Jeffrey: Is the a pointer to the chrome/webkit feature? 

Marcos: Will try to find where that is. 

Jeffrey: I'd be happy to draft a comment and run it by Marcos.

Marcos: should we start with the questions to get them moving so they don't have to wait for the formal position?

Jeffrey: Yes. Please make sure the use cases need a CPU measurement and talk to the working groups that work on those use cases. We don't need to close or set a resolution; we'll wait for an answer to that first. 

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @xiaochengh

Dan: Had a chance to look at this this afternoon. I'll work with xiaochengh async. There is precedent for what they're trying to do, but I'm not a fan. Would like to push them to see if this is something that could be removed. 

### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1134) ([Github](https://github.com/w3ctag/design-reviews/issues/1134)) - @jyasskin, @dandclark

Jeffrey: I think we're ok with this?

Dan: Yes. The big ask was to justify the processing thing a bit more. I wasn't totally satisfied with the response, but I do know they have been talking to developers and getting feedback that this si the right thing. I would have liked to see more of that in the explainer, but they are doing the right thing. Will draft a comment closing the explainer.

### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

Jeffrey: I think we're waiting for Brian to have a comment. 

### [design-reviews#1196: [wg/webperf] Web Performance Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1196) ([Github](https://github.com/w3ctag/design-reviews/issues/1196)) - @jyasskin, @marcoscaceres

Jeffrey: the chairs wouuld like to add lines to the spec and mark them as experimental to the spec before they have multiple implementations. Can say some of the TAG has concerns, but we want to indicate leaning one way or the other. 

Marcos: Clarifying, They basically want to include incubations in the specification. That may be ok if they have multiple implementers backing the thing. Problem they were having was that they weren't getting enough participation from various implementers, but want to land things in the spec. I think that's risky because implementer might come back and wonder what it's doing there. They need to fix the WG process for getting conensus, rather than landing without consensus. But it's for them to decide what's best, and if fits all members, they should add things.

Heather: I don't have a problem with an experimental tag. Making it clear in a draft spec that this part is more drafty, by clearly labeling it, is perfectly reasonable. But I'd want the WG to agree that an experimental tag is something they're willing to have. If 1 editor wants it, but the others don't, the no. But if the WG says 'yes', I have no problem.

Jeffrey: 

Marcos: The process document has an explicit mechanism to mark things "at risk" at CR.  But the framing sounds different. Covered by the same thing, but maybe they want to make it more explicit. My reading was that they wanted to put the incubations into the spec rather than having them "at risk". Could be both?



### [design-reviews#1194: WG New Spec: HDR on the web (CSS, Canvas, WebGL, WebGPU)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1194) ([Github](https://github.com/w3ctag/design-reviews/issues/1194)) - @jyasskin, @xiaochengh

Jeffrey: I have a draft comment. See https://github.com/w3ctag/design-reviews-private-brainstorming/issues/249#issuecomment-4180738881. Please read and see if we have consensus to post. Will ping xiaochengh over Slack as well before posting. 

Heather: If they've got the right experts in the room, all I'm looking for is consistency. Good with the text.

Jeffrey: 

### AOB

Marcos: Around DAS, we might have a finding around browsers vs engines. When WGs write specs, it hands off functionality to 1 of 3 entities: browser itself, e.g. WebKit hands it off to an OS API (IdentityServicesFramework), which handles UI. Chrome does some more things itself. Gecko on Mac uses IdentityServicesFramework. Spec is written, they handle JS realms, SecureContext, Permissions Policy, User activation. All those things are across engines. Then a point of departure as an implementer to use a 3p, give it to the browser, or leverage OS. Boundary, I think. Could discuss. Another example is Brave, which leverages Chromium but turns off some APIs. E.g. because privacy or security issues. They pick and choose, but implementation is the same. Finding here might settle some debates. 

Jeffrey: Think you're right that there's a finding. Worth writing down where we agree, disagree, and what to think about.

Marcos: In DC, some people thought WebKit shoudl implement CTAP. Rec became that it "should" use CTAP. There are interesting cases around the boundaries.

Heather: Feels like what Marcos is describing is what I was trying to capture in the brainstorm document about web platform vs web, and how you get there from here. https://github.com/w3ctag/design-reviews-private-brainstorming/issues/257

Marcos: Web vs Platform felt more broad.

Jeffrey: it's worth writing a finding about how all this acts, and we may have to collaborate with the AB on this. Sometimes browsers have multiple implementations internally. 

Marcos: We can point to a lot of concrete things to point to. The BLE case is one example and how it is/isn't used with the DC API depending on which browser engine you're talking to. 

Jeffrey: Might also need to look at non-browser implementation like polyfills. 
    


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
- https://github.com/w3ctag/design-reviews/issues/1203 - accept, decline, or skip (i.e., bring up in another breakout) - pass to the security interest group or webappsec and decline as the TAG. Marcos agrees.

- https://github.com/w3ctag/design-reviews/issues/1205 - accept, decline, or skip? - Accept and suggest we ask Matthew to look at it. Jeffrey has some concerns about intent; will also look at it.

- https://github.com/w3ctag/design-reviews/issues/1206 - accept, decline, or skip? Dan worked on this so shouldn't be part of the review. If I have input text area, there are two main use cases: custom highlights and getting the bounding rect. This lets you get a range object that lets you refer to a specific block. Jeffrey feels we should decline this; WHATWG reviews covers what we would normally look at. 

- https://github.com/w3ctag/design-reviews/issues/1207 - accept, decline, or skip? Heather: raising some potential privacy flags for me since x-origin iframes can be mighty sensitive. Marcos: ads? Assign to Heather and Marcos

- https://github.com/w3ctag/design-reviews/issues/1208 - accept, decline or skip? Matthew self-assigned last week. Jeffrey will suggest that xiaochengh also look since it's CSS.

- https://github.com/w3ctag/design-reviews/issues/1209 - accept, decline or skip? Jeffrey: concerns about the progress of WCAG; can the TAG help? Marcos: Give them a Working Mode. Examples of other groups with good modes. Heather: What should the TAG focus on in doing charter reviews? Will assign to Heather, Jeffrey, and Matthew

- https://github.com/w3ctag/design-reviews/issues/1210 - Dan looked that this as blink owner. Jeffrey notes it might be something xiaochengh would be interested in. It's small and simple; might be best to decline it. Jeffreey will comment in brainstorming and ask xiaochengh if he wants it and if not, decline it.

- https://github.com/w3ctag/design-reviews/issues/1211 - Heather and Marcos to be assigned

- https://github.com/w3ctag/design-reviews/issues/1212 - this is a general primitive; websockets over QUIC. Maybe Ehsan and Luke? Hand over to another breakout to discuss.



## Eurasia Breakout (Europe / Asia / Australia) - [2026-04-09](https://www.timeanddate.com/worldclock/converter.html?iso=20260409T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Luke, Matthew, Ehsan, Yves

Regrets: Lola, Hadley

Scribe: Matthew

### Consider breakout time — 0800 or 0900 UTC? This may need to wait until more members are present.

Christian: Breakout time is 9 UTC. Do we want to move it 1 hour earlier, now the time vortex is over?

Marcos: I can't do one hour earlier or later due to other meetings.

Luke: This does conflict once every 4 weeks with the WHATWG call.

Marcos: Same - gives opportunity to talk with WHATWG if needed.

Yves: This slot was chosen to synch up better with Asian countries, who don't observe DST.

Christian: Looks like we're fine with the time as it is.

Ehsan: +1

Matthew: +1

Christian: We should consider the opinion of Xiaocheng and Yu Sen.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: Need to come up with a comment, will do it today.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

(Skipped.)

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

(Skipped.)

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk

Matthew: This is interesting. Assigned myself to this during triage, seems nobody else assigned. This is new, haven’t looked at it yet. Will have a look early next week.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel, @xiaochengh

Christian: Discussed during the f2f. Sent response; proponents replied. I haven't had a detailed look yet, but would ask Xiaochengh to do this, as he's the expert.

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

Christian: Drafted a comment based on our discussion last meeting. We said we'd like to close 'unsatisfied' but I believe this is a bit strong. i understand where they are coming from, their rationale. The solution is not nice, but I understand their reasons. Suggest 'ambivolent' but that we highlight the problems with the approach. Could Yves and Marcos look at my proposed comment?

Yves: Even if they want to use redirects, they can use a link header, instead of using site-wide metadata such as well-known, which should be the last resort. Let's merge comments.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh

Matthew: Still looking at this.

Luke: I think it's a problem worth solving; solution seems to have been thoroughly reviewd to ensure it's implementable. I think the main thing is nailing down whether the accessibility works as intended. And getting the privacy stuff nailed down so that all the engines are on board with what they consider worth redacting, and what's OK to leak. There was discussion on the WHATWG calls that some things are leaked becuase they are _already_ leaked, but there was some disagreement that that's a reasonable approach to take.

Christian: To be continued. Feels pretty big. So we are not at the point to say 'yes' or 'no'

### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel

Christian: Last time we weren't sure what to do about the fingerprinting risks. It tends to make fingreprinting worse. The proponents ignored our request to add a S&P section. The alterntive was that we create an issue in their repo to track it there.

Marcos: S&P is a requirement for any W3C spec.

Matthew: Could show you how to track issues, if somebody is interested. Reach out to me if you want to learn how tracking works.

Ehsan: Curious to know if they have communicated the reason for not adding S&P section? The choice of on-device processign reflects an interest in privacy.

Christian: Their argument is that having a local model means their S&P considerations are already there.

Marcos: They mention mitigations; they've not landed.

Ref https://github.com/w3ctag/design-reviews/issues/1189#issuecomment-4000423542

There's a larger concern around Web Speech that contributions are Chrome-only, and lack of implementation commitments. Though I see some from Mozilla.

Yves: It would fail the TR '2+ implementations' test if that was a problem at transition time.

Marcos: This is confusing as it seems to be incubation work, but being done within a WG. *Checks charter.* Will file a bug.

... They're saying they think they solved it through un-merged PRs on the spec. We could push back and say it'd be helpful to give people a summary in the explainer, as it's confusing.

Christian: We could conclude the review here, and ask them to add a link in the explainer at that time.

Matthew: Question is, we would be happy if the PRs are merged. "Assuming the PRs are merged, and the link is added…"

(Consensus.)

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Matthew: Agreed on this one that we are happy, need to write the comment.

Luke: Did we have a detailed look into visibility? Seems counter-intuitive to what I as a developer expect.

Matthew: Just searched the minutes… in the review request, it introduced position area and properties. It doesn’t come up later. What I suggest is to leave a comment in the private brainstorming thread so Xiaocheng can have a look.

(Luke to post that comment.)

### [design-reviews#1035: CSS Gap Decorations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1035) ([Github](https://github.com/w3ctag/design-reviews/issues/1035)) - @matatk, @xiaochengh

Matthew: We are happy with this, can close it. No requirements. Will write a very brief closing comment.

(Consensus.)

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: Working on a comment. Trying to cover everything that was raised in the last discussion.

### AOB

Marcos: Wanted to pitch a finding. Did it in the US one before. With relation to DAS and what constitutes an implementation. 

Essentially there are 3 engines that can go into a browser. When we write standards, we generally target the engines to implement the things that we want. At some point the engine reaches a boundary point where we hand off some functionality - e.g. in Digital Credentials there is an OS-level service (on Apple platforms) to do this. Similar with Geolocation. So it's not necessarily something the browser implements. Geolocation is interesting. In WebKit it calls out to an OS library. In Gecko it was using a third party to do a geolocation look-up. With DCs, Chrome on Mac doesn't use the OS library. They've implemented it themselves in the browser. But if you look at the spec, there's a very clear boundary where this is handed off.

... All engines generally run the same code and that will be a policy enforcement point e.g. for secure context; permissions policy; has user activation happened; etc. Eventually we hit that limit, the boundary of the spec. The OS doesn't know about JS realms. But these things can come from OS, third party, or engine-specific code.

... E.g. Gecko uses Necko [spelling?] networking stack instead of using the OS one. But WebKit uses the OS-provided one.

... I would like a finding to clearly define the boundaries of what an implementation is, and talk about the boundary.

One more example. Brave uses the Chromium engine, but they have removed things that they think annoy or could harm the user's privacy, e.g. they disabled Vibration API. They pref'd it off. But if it was turned on, something would be called (in the brower or otherwise) to cause the effect.

In the case with DAS the Team didn't seem to have a way to determine whether things were implemented per spec. This could apply to any WG. This would bypass discussions we've had e.g. with Chromium people about implementations across platforms.

E.g. for Gamepads - there are only so many ways of talking to the OS.

Would love to collaborate with people as we investigate the boundaries of browsers and specs.

Luke: I'd be interested in reading and critiquing anything you write. I believe WebKit uses HID and Chrome probably uses IOKit on Mac.

Marcos: Yes, there are alternative ways of implementing the same thing.

Christian: +1 to being interested. Currently have a lot on, but would be interested in following and contributing if possible.

Ehsan: Similar to the work we (Marcos, Christian) are working on. I am interested, would like to join.

Macros: Let's record that we believe this is worthwhile.
 
Matthew: Does that mean that this is a study of looking at engine source code? Is that what it is?

Marcos: A situation we've had with recent TAG reviews is disagreement about what is an implementation. What is a single-engine implementation. E.g. the difference between 7 implementations, but they're all Chrome. There could be differences with e.g. Edge on Windows - but these could be outside of the boundary of the spec. And Microsoft may/may not have changed the code that is within the boundary of the spec.

... So we set out to find out if we can ascertain that there is a boundary of a given spec, and what that means for whether there are differences in the implementations.

... We are not entirely sure what we'll find, but I think it's important becuase we keep running into this issue. But once we have the definition, then there will be concrete outcomes for the W3C process, as to what counts as an implementation, and the spec defines the boundaries for it. And when it leaves the spec, that isn't part (and shouldn't be counted as) an implementation.

Luke: Makes sense, but if we define the boundary of the implementation as what's in the spec, how does this relate to the code that does what the user expects in terms of functionality?

Marcos: E.g. Vibration API - Mozilla ripped it out, but left a stub. So in the implementation report, it looks like it is supported and is interoperable, but it doesn't do anything. These are the cases that I want to document. I think something good can come out of this.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

#### Question: Using Cross-Origin-Resource-Policy to enable compression dictionary support for opaque responses (https://github.com/w3ctag/design-reviews/issues/1203)

Skipped.

#### Other Spec Review: OpaqueRange (https://github.com/w3ctag/design-reviews/issues/1206)

Luke, Matthew assigned

#### WG New Spec: Programmatic Scroll Promise (https://github.com/w3ctag/design-reviews/issues/1210)

Luke: Maybe decline, seems trivial.

Yves: Xiaocheng might have an opinion on?

#### WG Revision: WebTransport (https://github.com/w3ctag/design-reviews/issues/1212)

Ehsan assigned.

#### Question: Capability Delegation stalled -- specs are implementing local workarounds
 (https://github.com/w3ctag/design-reviews/issues/1213)

Marcos: This is similar to permissions policy in that it's delegating a super-power of a transient activation down to an iframe. It doesn't propogate into 3p iframes. 3p iframes are running in the wrong thread potentially so there are all sorts of threading problems. So capability delegation uses postMessage - it's more like 'I grant you the ability to take part in transient activation'.

... This allows a transient activation to be passed along _but only for a specific API_ such as payments, for example.

Christian: Who wants to take part?

Marcos: Warning, DC and WebPayments people are trying to bypass it. There is real privacy and security risk here if we don't get this right. Bad solutions have been proposed like having a 'freebie' (any API) on first request per iframe - so people are just creating more iframes.

## Atlantic Breakout (America / Europe) - [2026-04-10](https://www.timeanddate.com/worldclock/converter.html?iso=20260410T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Christian, Heather, Matthew, Ehsan, Jeffrey

Regrets: Lola, Hadley, Yves

Scribe: Ehsan

### [explainer-explainer#34: Structure alternatives as: Alternative → Pros → Cons → Reason for rejection.](https://github.com/w3ctag/explainer-explainer/issues/34) - @jyasskin, @matatk

Jeffrey: Sent https://github.com/w3ctag/explainer-explainer/pull/38 to improve the situation here.

Jeffrey: posted PR last night, ahs anyone looked?

Matthew: looks good to me, skimming but I will look more into it. Doesn't seem I have an issue.

Jeffrey: I can update it, let me know async (or here)

Heather: you mentioned about the structure

Jeffrey: we have the template where people copy and then instruction son how to get stuff in.

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Jeffrey: any progress?

Matthew: not reviewed yet

Jeffrey: there was a bigger issue in f2f about what this program will do, this is not urgent but we need to work on that

Matthew: Lola had some points, I will work with her on this.

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk


Jeffrey: anything?

Matthew: I started to look into it, I am not sure where to put it. I need more time here, especially about the thing as a whole... some places are relevat but not sure yet. I will look more.

Jeffret: you probably need to add a tip (https://w3ctag.github.io/explainer-explainer/#tips). It is mentioned in the introduction, but not the tips.




### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

Jeffrey: Sarven is not here.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Jefrrey:  I feel like meta items will be more next week.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Jefrrey: no progress yet.


### [design-reviews#1214: [wg/math] Math Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1214) ([Github](https://github.com/w3ctag/design-reviews/issues/1214)) - @christianliebel

Christian: No update.

### [design-reviews#1215: [wg/wot] Web of Things Working Group rechartering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1215) ([Github](https://github.com/w3ctag/design-reviews/issues/1215)) - @jyasskin

Jeffrey: No progress yet.

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

Heather: not finished the review yet. 

Heather: I wrote down my points and fed them to chatGPT to make them coherent. Is everyone ok with that?

Jeffrey: not sure as previous experiences were not ideal. I prefer to have another look from humans to ensure hallucinating or redundant content. There is a policy for it.

Matthew: I read through it and it does not seem odd (there are some pieces)

Heather: I had some issues about the race condition that could happen if there are conflicting items. I also have some points on the security and privacy. It needs expert review.

Jeffrey: the race condition already exists becsause browser autofill and this react to this in parallel. We are trying to make it better, but I can't say it is successfull.

Heather: I am not an implementor, but it seems like an issue to me.

Christian: I am very busy and I want to support heather but it is not possible in two weeks.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Jeffrey: Ehsan what do you think about the conversation?

Ehsan: I agree with the discussion, but I am not sure which one is correct. What do you think Yves?

Yves: the CORS is the problem, is it possible to replicate this behaviour using crafted messages? I don't know if it makes sense or not, Ehsan need to look

Jeffrey: my sense is this is only allowed if there is only third-party involved. If the credential is requested, this is not good but I am not sure about it.

Ehsan: I will have a look and let you know.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: I proposed a comment, I have not seen reaction.

Brian: I know that  Luke has been involved and tracking this - but is on holiday today. Perhaps we can co-assign him.

Matthew: We can ping him on slack.

Jeffrey: should do it. 


### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Ehasn: I agree with Jeffrey's points. Working on finalising a draft, ETA early next week.

... I think the overall feedback seems OK, but there needs to be some change on the bounce tracking aspects. My sense is we have agreement on the other parts. I'll iterate on the comment.

Jeffrey: Others: the last two comments are the ones to skim in order to get up to speed on the proposed comment here.

Heather: a note on questioning the stakeholders. who is the stakeholder.

Jeffrey: It is basically asking Ehsan about it, it is for internal use. Anymore comment?

JEffrey: feel free to post more comments in the week and Ehsan will post a final comment.



### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Matthew: Lola was supposed to put a comment on it. I think we were pretty much gonna say "this is fine". Jeffrey you pointed something about other browsers, but lola wanted to put some more comments (concerened about the level of support from other browsers). Is that ok to propose "satisfied" regardless?

Jeffrey: I think if her comment doesn't get out by Tuesday, you should ping her.

Matthew: OK

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

#### [WG New Spec: Programmatic Scroll Promise]{https://github.com/w3ctag/design-reviews/issues/1210)

Jeffrey: I think there was a decision to reject 
    
Brian: Luke is assigned to the custom elements, I will put myself on this too.

#### [WebTransport](https://github.com/w3ctag/design-reviews/issues/1212)

Jeffrey: WebTransport, Ehsan is already assigned. anyone else?

Yves: we already reviewed this 4 years ago. 

Jeffrey: They made a summary of the changes since then... probably not much to say but will be good to have a second person in the review.

#### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/1213)

Jeffrey: Capability delegation... 
it is discussed in Eurasia breakout. What should we do with it? Marcos was complaining people are not doing work but it is not much we can do as TAG. It seems we all agree to have a consistent design for this problem.

Heather: I am motivated to see the results. Do we have any relation with WhatWG chairs?

JEffrey: there are now WHATWG chairs. ??? is the person working on this. We can say we think it should continue.

Heather: Yes

Jeffrey: I think we can comment that in the review.

Matthew: I was very itnerested into the decribtion by Marcos yesterday. He was saying there are some solutions for this, and most of it was not ideal. We don't want to see many of those solutions got accepted.

JEffrey: we can say freebe for new iframes is bad.

Matthew: ???

Heather: I have no objection for that. It will have some issue with the webAuthn. This might mean if there is no here, then it will be no to WebAuthn either.

Jeffrey: Draft comment:

> We discussed this in two breakouts, and the TAG agrees that we'd like work to continue on Capability Delegation to act as infrastructure for these several related areas.
>
> We agree with @marcoscaceres that we see potential abuse if each new iframe gets a call without activation. We think that WebAuthn needs to reconsider its design if it's open to this abuse.

Jeffrey: no objection to it so I will put it. Also, we need volunteer to refer to the specs affected. Marcos?

Heather: Maybe not Marcos.

Jeffrey: HEather do you want to be there? 

#### [WG Revision: EPUB 3.4](https://github.com/w3ctag/design-reviews/issues/1216)

Mattthew: I can do as many APA people are already involved in it.

JEffrey: I think APA should do that, it might include some security items that can relate to architecture but not sure yet.

Matthew: I wonder if there has been many changes to that?

Heather: It says there are some changes

Matthew: I found it. thanks.

Jeffrey: I suggest we decline it and refer to APA as appropriate review target. We can say we see no architeture issues with it. Here is my draft comment:

Draft comment:

> Thank you for sending us this review. We don't see any likely architectural implications from the changes you've summarized, so we're going to decline to do a detailed review. We think the other horizontal groups will cover the topics they focus on.

then close the review.

#### [Question: How to reduce apex domain modifications for IDPs using FedCM](https://github.com/w3ctag/design-reviews/issues/1217)

Jeffrey: this is very interesting.

Heather: and frustrating. This has already been in the group in 2021. It seems to be a very hard problem for several organisations. The group that work on Stanford uni commented that can we put the information somewhere and then the conversation started that what would be the right approach. Microsoft proposed this comming to the ???, we basically reached the point that we are not sure what to do and we are asking for help.

Jeffrey: maybe we should offer help to Mark Nottingham to help. This is part of the web architecture. 

Heather: It seemed easy problem but the university and Microsoft are pointing it as a hard problem and it is intiating discussions.

Jeffrey: the biggest risk is we give two answers and then they disagree. The best is to have an answer that make sense to developers.

Yves: if many people failed, then I am not sure how we can make it.

Heather: as I am too invested in this already, I will nto put my name. 

Jeffrey: I will post to offer with that to Mark Nottingham. We will come back to this one later.

#### [<usermedia> Capability Element (part of PEPC)](https://github.com/w3ctag/design-reviews/issues/1218)

Jeffrey: maybe Mike here?

Christian: sounds reasonable.

Ehsan: I might be interested, let me have a look.

Jeffrey: ok.

