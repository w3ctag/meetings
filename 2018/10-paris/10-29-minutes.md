## TAG F2F Paris
##### 29 October 2018

Present: Lukasz Olejnik, Kenneth Rohde Christiansen, David Baron, Travis Leithead, Alex Russell, Sangwhan Moon, Daniel Appelquist, Yves Lafon, Peter Linss, Hadley Beeman

Regrets: **(this space intentionally left blank)**

---

Agenda:

## Escape workshop

alex: {putting document to review in the slack}

hadley: very big picture is that AMP has renewed a lot of interest in packaging. Publishers sign content and UX and origins and the like work, even if the content comes from somewhere else. We're looking at a workshop in January to discuss the bits nd pieces. Came up in other WG contexts. Meta point: my worry is that we need to address this in the context of "I am the Guardian and I want my pages to load faster", there are additional use-cases and we should make sure they're included

yves: Terence Eden talked about the need for archiving of Web Packages and the issues associated with signatures. That case is different from what's in the din the din the draft today

dan: I made a comment that I thought the anti-censorship/civil-society/privacy part of this wasn't well represented in the description. If we're going to discuss packaging, and SgneGX and who it benefits, getting those constituents in the room feels important to me.

Alex: are we ok with participants list? (review folks slated to attend). 

Hadley: would like more use cases.

Dan: my high level idea: it's good to have a joint workshow between IAB + W3C to drive coordination.

Alex: We've agreed tahtahthat Mark and I lewill be program chairs.

Dan: Let's make sure we have an inclusive paragraph as noted above. 

(agreement that we should have Tzviya Siegman from DPUB involved, perhaps on the PC)

yves: publishing WG is also looking at an alternative for their packaging format

(discussion of how that community can remain involved)

dan: so should we have mark join us, or are we doing with this discussion?

hadley: I don't know if we've answered what the point of the workshop is

Alex: we're probably not going to redesign signed-exchanges (it's already quite far along). Looking for: have we captured all the design questions? Is the design sound? If it's not, that will require a redesign, but that won't be sorted out on the day. Channelling mark: IEFT folks are looking for signs from publishers that they support. Part of goal is to show the folks who willl benefit are folks who are attending.

Hadley: is the above content just a single discussion, or are there larger decisions that nneed to be made?

Dan: Can mark dial in? He's ready...

(through the magic of science, we have mark on the line)

mnot: do you have a view as to what the workshop _is_?

dan: lemmie start; we'd only like to add that a paragraph about inviting civil society and privacy folks to the room is encouraged.

mnot: first of all, I should say that the purpose of a workshop in the IAB is a little different than a W3C workshop; for the IAB it's a way to get folks together who have a common interest in a problem but it's not a way to start a standards effort. That happens in BOFs. In this case, the idea is to have a much more targeted discussion with one potentially affected community because, as the description says, we don't have a lot of exposure to that world and would like to get more before we dive more into it.

mnot: have heard disinterest from other browsers, but when I talk to publishers, I hear very strong opinions. We want to hear them from the IETF perspective before we move forward. The workshop is about gathering that input. Having the discussion, seeing where it takes us. Lots of folks in publishing are keenly interested to see something more neutral technically.

mnot: if we broaden it much more, it'll be hard to get much done in a day and a half. The workshop is about getting specific feedback

hadley: what would you expect the output of the workshop to be?

mnot: the output is a report which is used as input ta stan  dards effort. Jeffery has done a lot of work a, but there's some concern about taking some of this work wholesale. Some people, and I feel this way, it would be difficult to standardize this without giving them a hearing.

dan: my pushback on your pushback is that I don't think we need to bring in general anti-censorship activists, per sae, but I more think that we should be talking with people in the publishing field who are focused on anti-censorship.

alex: we got some feedback that people wanted this for anti-censorship. If that's not in scope, why not?

mnot: (scribe missed)...

hadley: one specific use case you're designing the workshop around gathering more information about?

mnot: tehre's one elephant-in-the-room case (AMP replacement) and others that we aren't sure if they'll ship. So we want to get more out of that.

hadley: so if we have more use-cases, why not bring them all in?

mnot: I've heard representations that people are frustrated that we're being presented with a solution that solves the AMP approach, but if we took a community approach, would we not end up with a different technology that meets the needs in a difin a different way??

Alex: Multiple use cases in this -- from PWA side, publishing (rePublishing WG interest in replacing one-off thing), potential use cases around component distribution, .  Those haven't been part of this conversation because whenever we open this conversation around other use cases, seems like other folks want to scope it back down to the elephant in the room.  If goal is to gather info on whether this solves broader use cases, seems worth having those use cases in the room.  If not, what will we solve by having only folks addressed by AMP replacement use case in rthe room?

mnot: many use cases for the tech.  Purpose for workshop is that we have one thread that keeps on being controversial.  Give it a hearing now, understand  why it's controversial, if we do that we have a better chance to characterize the community's input... now we have other pieces, other communities, other use cases, and we can take the synthesis of that.  Then we have the work being proposed.  If we try to have the decision about how it affects publishing in ??? then it's less likely to be successful.

hadley: not clear why to do a deep dive on the one use case we understand the best. 

Does this meet a social need, bringing in someone who otherwise might not get involved...?
(missed a little here)

mnot: give people a chance to be heard.  Dispel concerns from publishers that they haven't been heard in prior Web packaging discussions. What exact capabilities will be exposed in the browser.

Alex: The TAG is on record suggesting packaging as a way to repair some of worst damage from AMP, specifically origin model breakage which hurts everyone.  

mnot: for context, major focus area for IAB is consolidation of power on the Internet.  How do mechanisms we standardize encourage consolidation of power?

Dan: Feels like we need to (cut off)

Alex: ???

Dan: can we enlarge the scope a bit so we hear from publishers not just thinking about using packaging for the AMP case, but also for other kinds of distribution, or publishers interesting in using packaging for anti-censorship cases.

mnot: if it's use cases for publishers, fine, as long as it's a proportional part of hthe workshop.  Concerned about dpub focus.

hadley: why?

mnot: Is ePub really part of the advertiser/publisher ecosystem.

hadley: Feel my best contribution is on the technical side and not redoing the ecosystem.  I we're coming from a technical perspective and just looking at the AMP use case, seems to tell other use cases they're not important.

alex: Can we acknowledge other use cases in invitation/summary, but still let people know the focus is on syndicated content...

mnot: ... and advertising/publishing online.

alex: welcome participation from other groups who have those interests and recognize those are use cases for packaging but by noting the focus

dan: could reinforce with a timeboxed discussion of those topics on the agenda.

mnot: happy for jeffrey or someone from packaging team to have discussion about how those would work.  Concerned about ePub focus.

dan: I am talking about that... it's an important constitutency.

alex: question is if they can replace their one-off packaging fgormat with something standards-based.

dan: one of the key areas for the TAG -- can we get ePub to closer align with the rest of the web stack by encouraging adoption of ...

mnot: Understand why that's a motivation for the TAG -- but as organizer of a workshop I want to have the right conversations in a day and a half.  Not convinced about ePub focus on the program committee.

dan: what do we want to put our energy and time into?  Big advertising, or better web?

mnot: purpose of workshop is we're considering standardizing something that may have massive effect on that ecosystem.  Want to understand its impact.

hadley: Have trouble making sense of that without equivalent for other use cases.

alex: if ePub adopts this it has a big effect on the way content ?? industry as well.

dan: longer workshop?

mnot: would ePub adopting this be controversial?

alex: yes, large toolchans to replace.

Yves: ???

alex: then maybe not so controversial

dan: maybe 2 days rather than day-and-a-half.  At least a day on advertising-specific cases, but time on other cases.

mnot: half a day intro/overview/background, half day on other use cases, day on advertising.

alex, dan: yes

alex: suggest text to invite other groups but note limited time.

alex: and hopefully you have more context on my other comments.

mnot: core of my feedback on most recent comment -- previously tried to have 2 sections on percevied positives and negatives.  Edits seem to change it to both positives.

alex: Happy to reframe and to suggest other text.

mnot: On program committee?

alex: if we have a half day on other use cases non-syndicated content, one sixth of pc rerepresenting outside group.

## TPAC Debrief

[Assignments](https://docs.google.com/spreadsheets/d/1xhG8KNdg5njJUH-H6V1zcIKjJgmFRIOUFL5U4cCWqVU/edit#gid=0)

### Day 1:

#### Morning

Anything notable from the morning?

dbaron: nothing is ever finished. As tantek says, "specs are either being maintained or they're not being used".

plinss: we tried to kill off GCPM. The pie-in-the-sky stuff fell off. Should perhaps kills what's on /TR/

Alex: I went to APA in the morning, 60-90 minutes, fascinating -- they had Math on the Web CG visiting -- needs for better accessibility hooks -- what I noticed was that accessibility representatives were asking "tell us what you need and we'll design it" and Math community really wanted an extensibility hook because a11y folks couldn't possibly couldn't cover everything.  They'd just do things wit hthe hooks they already have, otherwise.  Mantra has gotten through to some folks.  We went to interesting things 

#### Afternoon

Sangwhan: Was a proposal to stream WebRTC by "stream all the things" everything. Move everything to the Streams API. Part of the "WebRTC NV" proposal. 

Sanghwan: because things would be converted to a Streams API, not everything 1.0 provides would be polyfillable.

Travis: because the bits will be different?

Sanghwan: they have some weird features about non-streamy data formats that can't be accommidated. Not much of this is interoperable, so it might not matter much.

Travis: because you can't do much with it anyway?

sanghwan: these features might not be usable from the live web anyhow

alex: poor interop, IIRC: https://wpt.fyi/results/webrtc?aligned&label=stable

dbaron: so there's also 3 versions, roughly, in the same 1.0 spec. If you use this bit of v2 with this bit of v3, who knws what'll happen!??!

sanghwan: almost no interop.

yves: they also need to update their tests

alex: There are folks who are looking to make this better layered, which seems promising given how poorly it's layered today. You can't *just* use the data-channel.  Can we as the TAG encourage them to do that. How can we provide them with support?

sangwhan: streams is a step, chopping up monolithic interfaces is a second step.  Would be interested in following up if reelected. For the next version work, we could perhaps provide more useful feedback. Getting to a more layered spec.

travis: so instead of 3 ways of doing things, there will now be 4?

(GO STANDARDS!!!!)

sanghwan: I met with the Math folks. ; mathjax maintainers, etc. They're doing a lot of this in userspace. They want to know when Houdini Layout will happen.

plinss: some hope to help them with Houdini

alex: they'll also need font metrics API, right?

plinss: right. They need to stretch glyphs

sanghwan: integral and ral and ral and ral and ral and parens need stretching, e.g... I was expecting much worse when I walked in and they were sensible people with sensible requests. Want to supporthethethet them
sangwhan: they asked "what's the TAG's position on MathML?"

travis: we tried to address that in the plenary panel

alex: so we were asked for a position?

sanghwan: not just mathml, math in general

kenneth: people have a lot of problems with mathml

sangwhan: you lose a lot of semantics in mathml; layout language, data model, and equation defintion. It tries to be all 3 but you can't be all 3 at once, so it's suboptimal.

travis: is there a way they should be? is data-model the way to go?

sangwhan: equation definition would be fine with a way to split out data

plinss: worked with some of these folks in the 90s to do a separation based on CSS. Never got that far

sanghwan: authoring is also painful because it's not the sort of language that people who write math equations use.

travis: perhaps we should open a design review on MathML?

alex: is there a community to engage with?

sangwhan: everyone supports some version of it

alex: we removed it from Blink

dbaron: we've supported it for a long time

alex: does Edge have MathML?

travis: it does not.

lelealetravis: I'll open up a design review for this

alex: let's make sure we're talking with whoever is working on it

(discussion of how we can help identify common custom elements)

plinss: this brings up the general problem of how we re-integrate these other languages: MathML, music markup languages, etc.


AlexelexaTravis: I went to Publishing and Web Platform. Publishing had a long conversation about strings wth directionality and language tags. An overlap of what we discussed.

dbaron: we didn't ever get them to write up what we discussed with them.

travis: I think we needed them to have that discussion in the coconversation. The practical folks eventually ended up at "we use a subset of HTML beeverywhere, so why not that?". The JSON-LD folks said "fine, but we're not happy. If you can bring us a proposal for whawt it should shshlook like in HTML, we'll take a look at it"

travis: all the right i18n folks were in the room.

travis: it wasn't the conversation I was hoping to hear, but it's what we got. I was hoping to hear about publishing and packaging, but that wasn't what we needed.

hadley: TPAC is hard like this. We end up novisiting when gorups are in the weeds when we want an overview

sangwhan: there's a controversy over Web Packaging vs. EPUB. A split on how to move forward. In particular they have issues about pagination and search in web packages. Isn't clear how to do that. Search isn't something we provide in the we provide in the platform.

alex: what does EPUB do?

sanghwan: not sure; you can search the HTML

alex: can't we do that with web packages too?

sangwhan: some discussion about how this might work with Invisible DOM

travis: dovetailing into searchable and invisible DOM; had a breif conersations wiwith Alice Boxhall around how to do this in the context of AOM. Providing an accessible way to do this without opening up fingerprinting or privacy concerns.

alex: I'm really concerned about this thread of argument; turning on the a11y tree usually leaks usage through timing. Browsers don't protect against this

travis: the hope was that doing this through something like invisible DOM would allow a11y to piggyback on a general purpose mechanism; fold a11y tech users into the mainstream.

plinss: I had a side-channel request that we do a general review of epub 3.2 vs 4.0

kenneth: first day at DAS there was discussion of permissions. Not much progress from that workshop.

plinss: has the workshop produced a report yet?

kenneth: it's not out yet

kenneth: geolocation generic sensor; thomas leading that work. Discussion about how to allow that to work in the background, particularly re: geofencing. Can't depend on SWs being alive

alex: right. Need to signal those as events that can wake up the SW

kenneth: discusion of how to test with webdriver extensions.

travisL: the group behind that has been amazing.

kenneth: a bit about WebNFC. May be removing peer-to-peer because it's not supported on iOS and will require changes to Android to support. So removing that. Also moving to be more modern -- abort controller and abort signal. Also, instead of a weird `watch` thing, moving to an event to be more in line with DOM and Web Bluetooth

alex: anything to follow up from us?

kenneth: nope; going well


#### Tuesday

hadley: went to Spatial Data on the web who are now an IG (were a WG). Produced a "best practices" document draft. Were a WG with OGC. They took advantage of TPAC to meet with the Web of THings group and one of the OGC SensorThings group because Spatial Data had been working on a way to describe the location of sensors and OGC has a way to describe sensors. I think they're fine.

hadley: sanghwan and I went to localization. We ended up with a big conversation about how to format rtl/ltr for the lefthand side of an email address (the "mailbox"). 

sanghwan: Mailboxes are not very unicode compatible. RHS isn't a problem because punyode.

plinss: some new standards

travis: i've been trying to track this down inside MSFT

(discussion of state of MTA compat for unicode)

sangwhan: `<input tpe=pe=ype="email">` seems to be dead....

alex: is it?

travis: the validation kills it. Nothing that's not ascii charachters won't pass validation.

(discussion of how to relax the restrictions)

alex: should this be noted for our HTML review?

travis: yep.

(discussion of form extensibility; particularly validation)

RESOLVED: we all hate how forms are welded closed. "forms are bad and they should feel bad"

hadley: I went to webappsec and we had a conversation about private browsing

alex: ...did we get them to give us a CORS Mode that just lets you freaking fetch the resource?

hadley: no

alex: it's been another year! What are they doing!

hadley: I had to hear about this from Tim again yesterday.

alex: and he's not wrong!

hadley: webappsec was asked by Web Platform for a definition of private browsing.

dan: what did you input to the conversation?

hadley: cheerleading. Brave's research that a lack of uniformity among the modes confuses users.

alex: I'd like for us to note how poor the current modes are. Whhenn we studied htis last, it was clear they were pretty deficient. These folks need to start bringing VM technology to the table if they're going to do what they say on the tin. We could define a strong form, and demonstrate that some current implementations aren't as strong as that.

dka: We should get the Tor browser folks involved.  Notable that Brave were ata TPAC this year too.

(discussion of where to host this work and WebAppSec charter scope)

alex: pe: perhaps a good role for a CG; less lawyer ovehead (potentially)

dan/hadley: DNT formally closed

hadley: AC meeting and decentralized identifers. We obligingly did not review Manu's spec. At the same time, they're campaigning for a WG. 

(we resolve to open the issue and review)

hadley: Manu has an SBRI grant from the US DHS to create an ecosystem in which identity solutions can grow. There's a press release on that.

**blockchain blockchain blockchain blockchain**

blockchain blockchain?

blockchain!\

Hadley: verifiable claims - they are still figuring this out. they are in the incubation stage. they plan on feature freezing in first wek eek of november. Use case was parent traveling internationally with a child, and upgrading to first class. 

Dan: I've had this problem, the parent part.

Hadley: i am unsure for these use cases whether they need to be in the web platform. We should come up with an opinion to share with the AB and the community.

hadley: the question is in front of us and there will be a case for a WG

(discussion)

[lunch]

TPAC debrief continued

Sangwhan: clipboard now adding caps for images. Big debate about how to do that. WHATWG annavk notes we could break back-compat for security. Folks from Microsoft objected. Spec defines a way to 'pickle' the thing into a binary blob... if you don't know the format, you can't descipher the data. Gary and Chrome team had a proposal:

Initial proposal used DataTransfer, but

SM: Any feedback on this particular item?

Alex: What would we like to weigh in on? Will come to us through Blink process, right?

SM: Assume so.

##### AC

Hadley: decentralized Identifiers was the main concern.

Dan: Collaborative WHATWG proposal. Went much better than Berlin. (e.g., no comment about terrorists) So, that was positive! Chaals had a few negative comments, glazman said (in other direction): its lost, give up W3C. Otherwise, very positive comments, esp. Terence Eden who seems positive. Leonie asked if WHATWG would allow full access to W3C editors.

Travis: session on WHATWG/W3C apparently went really well.

Hadley: WHATWG represents largely American companies. Is that a problem?

Travis: Response was largely that it just happens that is where the engines are developed. ?

Alex: largely all engines (e.g., in Asia) are Chromium based.

TPAC Debrief Continued

---
There was a complaint that WHATWG can’t be reflected of the world since they’re just American browser companies.

Hadley: we want to avoid an HTML that is biased to Europe/USA and not good for the global community.

Dan: other AC things?

Dan: Ada on Immersive web was the best talk ever!! 

Hadley: talk on web packaging as well (from Kinuko Yasuda of Google). Included signed exchanges. Slides are [here](https://www.w3.org/2018/10/TPAC/slides/TPAC2018-Lightning-talk-Web-Packaging.pdf). 

##### Wednesday (Plenary)

### TC39

Kenneth: TC39 was very interested in any collaboration with W3C. Was some concern with how proposals that might reviewed by the TAG could results in “this is bad”. 

Dan: And why ask for feedback if the feedback is only positive? There was a proposal to put in front of TC39, that they could raise review issues with TAG. Four potential items raised that would be coming our way. 

Kenneth: Daniel was going to return and check with the authors of the proposals before raising them with us:
*temporal
*decorators
*weakrefs

Alex: I think it’s important for us to ask TC39 for Stage 3/4 efforts, and working with them to drive consistency (e.g., they don’t see DOM). They also don’t want TAG to send related feedback on other W3C specs (they have their own process). (This will apparently not lead to quality feedback.)

Kenneth: Our design doc has text about not exposing the GC. Yet, weakRef does expose it.

Alex: Well, we’ve been more specific about “read consistency” vs. not exposing GC. No other guarantee is really possible. If you keep polling in a turn and you get a different result sometime during that turn--it’s bad. But if you yield and then return, it could be a thing. Sorry.

Dan: We need to bring this up a level--we’re getting too bogged down here…

David: r12n did a “what’s up in i118n? Was poorly attended, but interesting to me. I18n wanted to get (long languages of the web) better supported on the web. Did some work for Japanese, and realized it took a lot longer than hoped. R12n working now on gathering a set of experts that can divide up the questions and sent to right experts. (e.g., How does Lao work in ?? case.)

David: Living standards and registries. Didn’t like the conflation of LS and registries.

Dan: how are they the same?

David: both require an update process that is different from a standards process. With registry there’s just a small piece that needs to be update. For a standard, you just want to use a different process rather than drive the whole document to Rec..it’s just a different way of working.

Dan: with Registries, we last kicked the issue back to AB.

David: I don’t think this was the same conversation about registries. Living Standards is the Process WG’s new focus area. May want to do a LS trial with a11y mappings. Seems well-suited for it (somewhere between a registry and standard), but also different than a lot of other docs (came up because of conversations about charter review). Mozilla was unhappy about weakening the two implementation requirements.

Dan: DNT?

Travis: Meeting was a retrospective on how the effort went, resolving to take the current spec to Note, and brainstorm how to continue the discussion (e.g., in community group). 

Dan: Now may not be the time to kill DNT?


Travis: the session thought that the conversation should continue, but perhaps in a community group.

Dan: Lukasz, were you there?

Lukasz: I was not. I don’t feel that DNT should be cut because it might be useful in the concept of how GDPR and ePrivacy evolve. There is work in the EU Article 29 Working Party that says there should be some consent mechanism. I know that some vendors are interested in maintaining it, on the security and privacy side and the policy side. 

Travis: attending were Mike West (Google), Tobie Langel, Travis, David Singer (Apple), and others from the WG.

Dan: yes that is my sense as well.

Lukasz: ...So I would keep that and see how it goes. There is also the idea that Tobie shared, that there are lots of sites with different consents these days, due to GDPR. So maybe it would make sense to standardise cookie boxes and consent boxes on websites. Maybe this is too premature? What GDPR requires is some of those pop-ups… and what would change if ePrivacy is adopted? Or maybe ePrivacy gets killed?

Dan: isn’t that the same as having an API? Instead of a cookie popup in the website, the web app could trigger something for the browser to say “no, don’t track me”.

Travis: Some sites are using DNT: 0 flag to assume that tracking consent is granted.

Lukasz: my understanding is that browsers haven’t fully implemented the spec.

Also, on Monday I was in Devices and Sensors working group. Nothing remarkable there except shape detection. I will look into that. 

I was also at WebAppSec. Some updates on web vulnerabilities, some proposals… And that’s it.  

Hadley: I feel like the journey DNT has taken has burned the brand. I think we still need users -- and user agents for them -- to be able to express their preferences around tracking. But I’m not sure the web standards community will get as much done there under the name “Do not track”.

Dan: Don’t particularly agree. I think we have that opinion, but others in the eco are more supportive. (Cites data from Robin Berjon for the New York Times) Can’t we get some advertisers to start using it?

Alex: related to unsanctioned tracking finding.. We said countering active fingerprinting is hard. But we put some guidelines in to help developers making standards do the right thing. Browsers could use this flag to enforce stronger interventions on blocking known bad ads.

Hadley: and fingerprinting? Other forms of tracking?

Dan: what Alex is thinking is valuable because it reinforces the user’s choice. Helps build an eco that respects user choice.

Lucasz: lots of research on DNT. But then nothing happened. Conversation turned from DNT signal to active ad blocking/tracking prevention. Conversation already moved. So, maybe browser could signal to developer that more active prevention is happening.

Hadley: my worry about the name was about standards activity in W3C. For a finding, I’m happy to use DNT explicitly (the term). The value is in the term that everyone understands. If we were starting a new effort, we could be more generic.

Alex: While discussing next steps, the brand could be salvaged in a way to encourage allternative uses for it?

Hadley: So, a finding here could be useful?

Yves: At Automotive, they're investing a complicated thing that reminded me of Web Services. Asked if they couldn't scope down their work... (seemed like it was overengineering for an area that is changing). They want it all! (Protocols over web sockets, etc.) My message: keep it as simple as possible (as 'webby' as possible).

Kenneth: WoT, they have many conflicting solutions,,,, not clear on use-cases. Now are targetting smart cities. Are adding Scripting llayer, using observerables? Sounds like a can of worms.

Yves: I wanted ted them to ask TAG fofor reviewtheir  of  their work as early as possible.

Alex: how can we repair our poor reputation with them?

Yves: Working with Ted from the WG... so he has a direct contact if neededd. When they have something for us to review, I hope they reach out.

Travis: Do they not have "something" yet?

Yves: no. Use cases, but nothing concrete.

Travis: the Distributed Tracing group met with Web Performance on Thursday to see if there was an existing mechnaism from WebPerf to help them get data through the client in a round-trip'd way. A good discussion and both sides learned more about the scenarios. In the end, the Web Perf WG suggested that most everything they wanted was already possible via Server Timing. They also said that the set of things that weren't already possible wouldn't be due to privacy concerns.

yves: they also discussed header formats, including JSON as a serialization.

hadley: does this discussion mean that performance tracing are packing up, going home?

traivs: no, but it means they can use some existing client-side API to complete their scenario. So they don't have to invent something else, they can use what's there.

hadley: so is there more to standardize?

travis: yes, but not on the client.

David: this was a question I had for their charter. Got my answer (apparently not).

#### Web GPU

Sangwhan: WebGL but less crappy. Vulcan/Metal bindings for the web. Should create the same performance improvement. 

Kenneth: HLSL and ?? shader languages?

SM: Someone at Apple is working on WHLSL (web version). Middle ground between High-level or low-level pre-baked language.

Alex: Is this being quarentined to a Worker?

SM: Well, can probably be used in either place. Also, there's this new thing compute-shaders for massivelyy-parallel compute(ML anyone?). Lots of open questions around potential security/privacy here.

#### Machine Learning

SM: The WebML binding I saw was a bit too early for useful technical feedback. Looked like they took the Android neural network API and created javascript bindings. I Couldn't tell whether it was for training or inference, or both? Until they figure this out, I don't think the design is clear.

Kenneth: Saw some demos.

SM: Poorly named--only does Neural Networks. Web ML CG is proposing WebNN?

#### Second Screen

David: dropped in on SS. Randomly dropped in during disc. on what they're planning for next year! Was very useful! They had useful questions about when to ask for TAG review. We like reviewing things early, but make it co-herent.

SM: They arere working on Open Screen Protocol. 

David: We previously looked at the higher level API, but they've since started developing the lower-level communication protocol.

SM: Yes, started out as binary thing, switched to CBOR. They've been listening to our feedback.

Hadley: what do we do about the protocol?

SM: That's a question for the group: should we review, or will it come to us, like WebSockets was developed?

#### AOM

Travis: Part of the WICG discussion... there were several venues where parts of the AOM were discussed. T Editing taskforce.. new events.. piggybacking off of the input event. 20 or 30 new input events - they would like to extend this with semantic actions that accessibility technologies might want to use. PgUp, PgDn, Increment, Decrement and Dismiss. All oost ther semantic events they rnneeded were already covered. That got warm reception. Alice met with the WICG - gave overview of where they are. Rteflecting properties for ARIA so you can read them through DOM APIs... has made it into accessibilities spec 1.2. They want to allow direct assignment - ARIA properties labbeled by ID ref ... 

Lukasz: did they discuss permissions?

Travis: they went to the security & privacy interest group and talked about the sec & priv aaspects of these...

Lukasz:  Is AOM closer to finalizing how this works?

Travis: the expliner and the spec are rapidly changing. Portion Leonie has concerns with is final stage which is stil being designed. I feel that group has taken Leonie's feedback to heart. 

Lukasz: still very changing...

Travis: mmonths away from updated document.

Alex: Confused with some of this - I've heard this cocnern in the past. Not wanting users who are using assitive tech to be profiled. But is there a principled line we can hold technically? A lot of these things are detectable - e.g. using high-res images... 

Travis: there was a comment about oft"often you need to enter an accessible mode" of a complex webapp that caters to spacial nav, keyboard support, etc...  that is a necessary thing for some scenarios.  

Alex: I don't understand how we're going to make it so that users of assistive tech are not distinguishable.

Travis: maybe there is a difference between prefs like larger font size, vs... a thing that clearly indicates you needing greater accessibility (e.g. an accessibility mode).
  
Alex: don't disagree. but we are positing a version of this that adds no fingerprinting surface area and I don't see how that's possible. is tthat doesn't seem reasonable.

Travis; It's not that's not supportable but we want to create the solution that is serving the accessiblity need and the general need.  

Lukasz: not sure what the relationship of fingeripring and profiling here. If you assume that something is operating after a permission prompt then it's not fingerpringing. Hp  For example incrementing ...

Travis: for something like increment and decrement the event would be fired for regular usage (of an input) as well as from an AT.

Lukasz: make it seamless... don't think that security & privacy vs. accessibility ...

Lukasz: difficult to make research in this region.

Alex: the last time I loooked the way AOM is constructed is - it's designed to give you the ability to provide data about a separate layer to anyone who asks - e.g. aria roles - es - will heop you understand focus and tab index... pieces of the assistive tech tree that all users may eventually want or need.  

... have we had progress wuth the ARIA focus on ARIA extensibility?  anything on that?

Travis: I don't think so; didn't hear anything about extensibility; although Alice mentioned that the AccisibilityNode idea is far away , and maybe not even feasable. (She'll cross that road when she comes to it.)

Alex: this demo enables and alternative input mode...

David: I agree with Alex's idea that it's hard to block on not detecting accessibilty in general. There are CSS animations thand prefers-reduced-motion that are a11y touch-points that can't really be avoided if the developer wants to leverage them.

Sangwhan: +1

##### Package name map

Kenneth: Imports? In Node land, you can import a URL. On web, you have a JSON description to map the module names to known identifiers. The page's map affects all the names imported by the page and recursively. Adds the ability to have native and fallback to polyfill. aaCan work for CDNs too. Lots of +1s. QQuestions about how to implement. Currently it's a script tag with a new type. Suggestions that this could be a header?. But headers are not too good for local development.

## Plans for Dinner

(TAG discuss all-important topic of "food")



## Ethics doc

Dan: Last night at dinner, was talking about movement in this area in global tech. Need to incor=orporate ethics into more of what we do. Tantec hightlhtlhtlhlighted mozilla manifesto which is pushing the company in this direction. At conference, say Project Maven -- A.I. division of Google that was using tech for drone targetting; had a link between drone and civian deaths; some googlers dqurevolted.--this is all in public press. Google produced a set of ethical guidelines for use of A.A.I. In essenace "we won't use our tech (or profit from it) in ways that can cause harm, etc." [Summary here](https://docs.google.com/document/d/1tGQOFo-d849sagYDvgGzmSpPFDd_Nf47qb0FT6UjQKc/edit). 

..Thinking about human rights. Was at Mozfest and attended session about thinking about human rights while designing tech. We've been thinking about this already though Sec. and Privacy self-check, etc. Idea of ethical design is not in W3C's DNA. I would like to alter W3C's mission statement to really graft ethial policies in. Tantec then challenged me to bring this to TAG; maybe our docs could help trigger the right discussions.

..Alex suggested we might need a CG?

Alex: If we want to build a community, it probably has to happen from within. the TAG has been successful by being a technical advice body, not a social proclaimer.

Dan: We've weighed in on EME's sheilding privacy researchers, unsactioned tracking...

Hadley: and how browsers should be for the people, not at the whim of implementors?

Dan: We should be asking also, what the users need?

Lucasz: I'm quite thinking along the lines of humanitarian needs, with some experience here. Disagree that this needs to be started by social circles. We've already involved privacy people, and we of coursew think of privacy thru tech lens. We can imangine digital ethics on a quite similar level. Even if we wanted to bring to a CG, then fine, but the TAG is already involved, as evidenced by this discussion here, and actually starting here. Now we need to look forward. To consider: which principles mentinoed would be applying to W3C, and which would be under their mandate and control. (I have edits to suggest there.). But in general, I'm supportive of this, and would like to be involved in some way. However, I'd like to point that might end up with 3 questionares; should consider how/if to merge them?

Dan: It should be one question, then please refer to...

Lucasz: On what level should we speak about digital ethics impact? Is it simply considering it in the design? Like David said: "if a disabled user want so use the web, he should be using it even if AOM would be designed in as way disclosing disability: (rephrasing; sorry David for using this). IfBut if it's not designed considering the risks/etc, then of course no choice.

Dan: Like the a11y mode discussion.

Hadley: Agree that there's work to be done in this area. Not sure a questionare is the way to do this work. Meta: who's our audience? Is it spec author at design time? Is it the AC at charter review time? Is it for companies/individuals for fututrutrure membership to help destablish the boundaries?

Dan: When thinking of bringing work to W3C, this could help inform your decision to e.g., bring my survielance tech to W3C... Something we could add to design doc.

Hadley: feel like there's a hole in the broader space of web standards, where no one has said "user is more important" or "a11y must be considered".

Sangwhan: Should this be in our charter scope ???? GGGSpec editors or implementers may not be aware of implications (or they may be very indirect). E.g., you could right missile guidance in HTML, so does that take HTML out of scope?

Dan: My emotional argument: if not us then who? If not now, then when?

SM: While working in this field that requires this (computer vision), that seems harder here because of the set of low-level features we're using. Web Components ethical? Who knows.

Dan: We can't say for a computer language whether its ethical, etc., (Less obvious/measurable). Some things may register on this scale...

Alex: What changes would you like to see made?

Dan: I would like to see spec author consider ethical designs in spec design.

Alex: Do you think there's a gap here?

Dan: I do see a gap.

Alex: And what you have them done differently?

Dan: (thinking).

Yves: Folks working on battery API assumed good intent, later it was found to be misused. Code of ethics in positive work env. is focusing on how we worku, not what we build.

Dan: Agree PWE might be a good venue, but we should consider it part of our remit. It's a tech topic (and a social topic).

Hadley: we need to empower people to make this into a technological decision as a result.e this

David: when dealing with S&P questionare, answers are relatively simple and short answers. Should be the case here. Our questions should be designed to encourage folks to consider what they haven't thought of before. I think this could be something that is good for us. Not keen on conflating it with PWE group. Seems different, and folks can pick where to participate. There's a risk to putting it into CG by make it take more process--bikeshedding, etc. You end up with a process sekewed to those who have lots of time to participate.

Dan: This represents 30 mintues of me typing. We should refine this together. I want to provoke thoughts and discussion in the WG. 

David: I don't think the list is too long, as long as a user can easily say no to half. As long as the others provoke thoughts.

Lucasz: on S&P questionare, maybe many of the answers are not informative, needs to be addressed.

Dan: David's comment fills his heart with warmth.

Hadley: would love to run this through a series of use cases. Existing tech/tenants probably can't be pulled (e.g., DNS used for nefarious purposes).

Dan: Considering freedom of expression (is great goal).. Many twitter tweeters are trying to wear you down so that you...?? It's information warefare tactic. Not trying to stop freedom of speech.

Peter: Folks using freedom of epression to advocate taking away other folks freedom of expression.

Hadley: ??

Dan: It's about mitigation. I don't know if we could build something that could stop EME. .. :-) Id'd just like to incrementally encourage folks to start considering these. And I want W3C to incorporate into a larger effort.

Hadley: not against the idea, but can image lots of ways of doing it badly. Would like to help.

Dan: maybe do more of a survey of what other groups are doing? as Alex suggested.
 There's an IETF, ACM series of guidelines.

Alex: Could be that the TAG recomments to AC/AB what to consider looking at/incorporating.

Travis: Are the questions concrete?

(read off a few of the questions...)

Hadley: many of these questions are eaasy to give BS answers...

Peter: love the idea; are we stepping stragiight into policy (out of our scope). Maybe we can recommend the AB look into this.... But can we bring this back to a tech issue? Are there guidelines we need to give that bring the W3C back to it's technical moorings... TAG needs to issue technical policy, not policy policy.

Hadley: there are some fundamental ethical things we act within. When considering these question, I wonder what the spec author is supposed to get out of it... am not sure a socially-grounded document is the right way to do this.

Dan: I jumped right into some of the questions... but maybe could frame this better: here's a set of technical/ethical considerations of which the following questions are pre
sented? 
"Is this tech restricted to certain types (like those in Silicon Valley, or for kid in basement)?"

Travis: ...well if the kid is bbpretty smart...?

Lucasz: Should this be done in CG? Who would want to be involved? oFolks with spare time? Tech vendors?

Dan: I have PASSION for this; would love to be an editor. Need to do more research. Will put a draft together and socialize with TAG. Then shop the draft around to AB, PWE, etc., see if we get good feedback. Then see where it goes.

Hadley: seems sensible.

Dan: Just working on this might be controversial. 
D
Alex: Just work on principles, not checklist PLEASE. We can later work backwards from the principles to potential concrete deliverables.

Hadley: encourage to tjhink carefully about using "ethics" in title. Wil have polarizing effect on folks (similarly to "human rights"). Don't want to have this fail because it triggers people.

Yves: SSCould also collaborate with Corallie.

Peter: We've set "priorities of constituences" (so not true that we haven't said anything about users come first...)

## Accessibility

The TAG finds that... the web should be accessible.

Adding a11y to our reviews?

Lukasz: I spoke to Leonie. We discussed if it would be helpful to make an accessiblity review in some form. Since we are already covering Ethics & co today ... this is broader than our previous discssion on AOM. Whether it's been considered? Whether issues were filed or fallbacks included? What safe fallback features were considered? E.g., if someone has motor movement issues, features dependent on accelerator might be hard to use.

Dan: what was Leonie's request for the TAG?

Lucasz? : No request in particular, area to discuss.

SM: Discussed this with APA. We're not the ones to wris to write this. 5-6 short questions, anything that triggers, then we could look into it. Keep it short, not 200 questions.

Dan: Sounds great. A11y folks might have trouble distilling down their great knowledge. Yet, we can't expect spec authors to give a11y due consideration (in general).

SM: Will make sure it gets simpler.

Hadley: I don't want the TAG to be: Our review is held up because you have a11y outstanding issues.

SM: Right. This can be deferred.

Lucasz: wait, what?? 200 questions? Can I see them?

SM: Lots, WICG?

David: guidelines groups are for content creators... APA is for reviewing specs. (Silver is new a11y guidelines). 

Lucasz: If its possible to create features and make the experience seamless even if user has a disability.

_Lukasz gives an example of impassable captcha without a fallback method_

## IETF Update

Defered until after IETF meeting.

## Teleconference Schedule

DKA: We agreed to move to a rolling 3-week model after this f2f. We may or may not have to move again after the election.

David: Reveals the crazyness of new timezone regulation... 

Peter: I will update the TAG calendar.

## Web Components Doc

Dan: What's remaining to publish this?

Kenneth: Nothing, let's do it.

Dan: but it's a draft!!?

https://w3ctag.github.io/webcomponents-design-guidelines/

Dan: Shall we spend 15 mintues to re-review?

RESOLUTION: let's publish this as a finding and put it to w3c space.

Alex: Domenic can make a streams guide.

## Joint Meeting with AB

Peter: AB is proposing joing meeting with AB. 

## Meeting dates

Tokyo in february



## Design Guidelines
## Priv & Sec Questionnaire
## Design Review Effectiveness
## Design Reviews

---












