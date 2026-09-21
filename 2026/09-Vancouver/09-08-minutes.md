# TAG Minutes - 8 Sep 2026 - Vancouver F2F

Present: Marcos, Jeffrey, Christian, Heather, Brian, Yves, Matthew, Sarven

## Notes

### [GitHub resolution labels](https://github.com/w3ctag/process/issues/50)

Heather: Came up in a recent breakout. Brian had thoughts. We aren't happy with our existing labels. I put Google Doc contents into this issue. I'm not invested in any of it. Brian was most concerned with "satisfied with concerns" being ambiguous. 

Brian: Matthew had the thoughts. I was concerned that it's not clear. People can interpret it as "we're satisfied with the concerns, so we're fully happy". 

Heather: Change the label or the description?

Brian: The label.

Yves: In some WG, they clearly received "with concerns" as just "satisfied" and didn't address our concerns.

Marcos: Just drop "satisfied": "with concerns".

Yves: Also the color of green is misleading.

Matthew: Google Doc: https://docs.google.com/document/d/1xNBe8H_mbeiMlp3hFtrKgb7gp7FyYPvVKv-yFbsT1Is/. I don't disagree with the concerns so far. Was trying to come up with consistent steps and outcomes. A number of different axes. Just fix the one thing first?

Heather: Anyone have suggestions? Understand the color coding, and I loathe putting semantics in color. Not going to balk if others want it.

Jeffrey: Color can be additional, but can't be the only way we communicate something.

Brian: Whether or not it's meant for the traffic light pattern, if it's green, people will interpret it that way. Fuchsia would be acceptable.

Brian: Matthew made the point that there are slightly different statuses for early vs wide review. Possible those should be clearly different. 

Lola: At the moment, all resolutions are green. Changing colors of resolutions isn't going to have much impact, even if it's in addition to something else. People don't take the color to mean anything. Need to be more communicative in our closing comment. There's miscommunication if we rely solely on the label. Maybe templates for each resolution? Put a description of what the comment means at the top. Labels are also very succint, which might not help non-native speakers.

Yves: Being too verbose can also trick non-native speakers. On renaming the labels: "Concerns, non-blocking" and "Concerns, blocking".

Heather: I like that better than my suggestions.

Brian: Can TAG technically block? But the intent would be blocking.

Yves: They can do whatever they want, but in a transition review, the staff handling transition will ask the WG why they didn't follow the TAG's advice.

Jeffrey: Like Brian's suggestion of clearly separating Early Resolution from (late) Resolutions.

Christian: Would use just "concerns", and keep "unsatisfied".

Lola: Even the suggestion of just "concerns" can lead to confusion. We might disagree here about what "satisfied with concerns" means. I think it means "you can move forward". We'd say "unsatisfied" or "object" if the concerns are blocking. In CSS, sometimes comes down to a naming thing. Don't know if "concerns" by itself communicates that well enough.

Marcos: On the WebKit positions side, we have extensive labels, which covers everything. "Concerns: internationalization", "Concerns: ...". Can frame the feedback around the concerns. Agree with Lola that the tri-state thing isn't great. Maybe just 2 would be ideal. That would put more weight on us. DAS case, where "satisfied with concerns" led to the chair ignoring our feedback. More inclined to drop the third state. Forcing us to limit the number of things, and to see things through.

Matthew: I liked Yves' suggestion because it's very clear, but it gets us into whether this is the type of review where we can block things. If we're a horizontal review group, we can block things. Like Jeffrey's point of being consistent across early/non-early reviews. I suggested 
* resolution: satisfied
resolution: concerns
resolution: unsatisfied
early resolution: satisfied
early resolution: concerns
early resolution: unsatisfied

Matthew: If we dropped "concerns", we might have to be unsatisfied with a lot more things. See Marcos' point, but we use "with concerns" a lot. Marcos, can you give us an example of the WebKit labels?

Jeffrey: We do need three states. I like renaming "Satisfied with concerns" to "Concerns - non blocking" or "non-blocking concerns". We also have an Object state which is almost the same as Unsatisfied. It would be clearer if we used "object" instead of "unsatisfied". 

Lola: I want to understand what "concerns" means. Does it mean "you can move forward, but we have concerns"? Does it mean "We don't want you to move forward until concerns are addressed"? Marcos shared the WebMCP WebKit review.  That's very precise. Just "concerns" doesn't solve the issue. We want to be clearer.

Christian: Alex Russell warned us against "positive vs negative", and suggested that we think about community guidance. "What can you do to improve the proposal?" 

Yves: Use case was ... concern was in another issue, about privacy and something like 3p cookies. Privacy issue was ignored because the label was a bit misleading, and it wasn't in a comment by itself. Was caught because Privacy raised the same issue. Need to be clear also in the text of the comment.

Jeffrey: Think "Concerns" means "we want you to think about this list of things, and try to address them, but if you can't address one, it's ok to proceed anyway." We _should_ have a template for each kind of resolution, that explains the meaning at the top and gives us a list of things to address.

Marcos: Disagree with Alex's framing. Raises a question that goes back to our charter. Are we a horizontal review group? We pretty clearly are. On the tri-state, Jeffrey has convinced me that we need the third state. We should have a template. Re Alex, we need to set some standards for architecture and making sure the whole thing is coherent.

Lola: Jeffrey's explanation sounds like "concerns" and "satisfied" mean the same thing, in that we're happy for you to progress. "Concerns" means "try to address these things before moving forward". We don't have a feedback loop for them to come back to us and get it upgraded to satisfied. They go on their merry way, and later we might or might not see a result. I don't think the "concerns" label adds anything, but it does lead to more confusion. Think the cons outweigh the pros.

Jeffrey: Concerns says to any downstream reviewers, which include the Blink API editors and the Team when doing status advancement, flags that the group has read our comment and has a response to concerns. Whereas Satisfied indicates no comments to respond to. 

Brian: I have a problem with the word "satisfied". Can be interpreted as "non-blocking", or as "we bless this". If we had concerns, we're not satisfied. Would rather not use the word at all. Would say "Support" as our strongest possible thing. Or "Object" or "concerns". Don't need to use the word.

Lola: Sounds like the label "concerns" is not for the proponents. It's for the downstream reviewers. If that's the case, we should make it clearer. If it's for both, I don't think it's quite right. Happy to replace "satisfied" with "support". Mixing the positive indicator with the negative indicator, where ultimately we're saying something positive. Seems like we're communicating "we're happy for you to move forward" regardless of whether they address the concerns. But then we're saying something different to the downstream reviewers? That's confusing.

Yves: Matthew's aware that HR groups have 2 kinds of labels when they open issues: "needs resolution" and "tracker". If we use "needs resolution", it's blocking, and the WG can't remove it by themselves. TAG reviews not only WG specifications and CG proposals that are outside the W3C itself. Can't rely only on that to express that we're blocking on non-blocking. It's one way to really block things if we need to. What we have now is already very useful to the whole panel of review that we do.

Matthew: Here's our HR 'tracking issues' list: https://github.com/w3ctag/tracking-issues/issues - this includes HR stuff plus any time someone on any issue in W3C or related space has pinged TAG for a response on any issue thread. Tracks any thread where we're asked for input, and also lets us raise issue. We're not sure if concerns are blocking, since the group can decide they're not. 2 conversations here: how do we make the existing labels clearer, and are we happy with the semantics of the existing labels? Would be good to look at some example recent reviews, and see how they were labeled, and see if we think it was confusing, and whether it was useful to indicate whatever we indicated. Concrete examples might help.

Heather: Think I used this in the thing I closed. I had questions, but I didn't feel like the questions were things where they needed to stop doing what they were doing. "Just clarify these things."

Marcos: On the WebKit side, we do have a neutral designation. A position, and then also concerns that are independent of the position. Don't think everyone has been confused. I'll paste a screenshot.

Brian: Doesn't Mozilla have a similar structure?

Jeffrey: They don't have the "concerns" list.

Christian: Consensus to add the "Early" prefix for early reviews. Need to keep discussing having the tri-state. Calling the mid-state "Concerns" has some support. Heather and Matthew will iterate, and we'll discuss at a future plenary.

Lola: [Expresses agreement with doing it the webkit way.]

Brian: I also like the WebKit idea.

Sarven: Have you covered whether the concepts need to be coupled, instead of keeping them exclusive. Group may have a neutral position and have concerns. Doesn't imply we're supporting it. Can have concerns, and separately that discussion may come out with us wanting the work to go through, or we don't want it to happen, or we have a divided opinion. They seem orthogonal.

Christian: Think that was Brian's proposed resolution.


### Timeboxing design and charter reviews

Marcos: Challenge we had with interesttarget was that we started and stopped over a whole year, which meant that getting context again, remembering what we were discussing, meant I forgot a lot of things. That dragged a long time and frustrated people. A lot of people didn't have much context. Having spoken to the proponents 1:1, they didn't imagine how the Vision Pro worked. There was a button discussion. To force ourselves to finish things more quickly, we could timebox. There are times that the discussion is ongoing. With WebMCP, some things will take longer. If something doesn't have attention in 6-8 weeks, we might defer or close. Some are more critical. E.g. charter reviews and horizontal review deadlines, we should prioritize those over "review my random API". That's the struggle. Try to help us get through more reviews in a more timely manner.

Lola: https://github.com/w3ctag/design-reviews/issues/1058 is the interesttarget issue. From here, we didn't take a year to go through it from start to finish. Opened Feb 2025, closed June 2026. We had a bunch of back-and-forth in private-brainstorming. Then replied in May. Even if we didn't have anything to say, we should have told them we were still working on it. Don't think we can really put timeboxes on design reviews.

Yves: Different issues have different priorities. Charter reviews, we know it's an early review, and it'll be reviewed in refinement and AC. Plenty of opportunities to catch issues. Not really an issue if we time out a charter review. If there are concerns, we need to treat it as fast as possible, but most of the time, we don't need to review. For horizontal review, we need to not let the WG hang many months before reviewing. Put it higher on the priority to give feedback because it blocks the WG. For general reviews, there's no solution that works in every case. We could be better at indicating in the issue that we're still considering it despite not touching it in 6 weeks. Showing it's not forgotten. Some issues require time. Sometimes it takes a long time to get responses. Apart from charter and HR, which have timing issues, we shouldn't do something automatic.

Jeffrey: For picking up reviews and waiting for responses from proponents, makes sense to have automatic time limits. If no one has assigned an issue to themselves in 2 months, we should drop it. If something waits for proponents to apply, it's currently a 6 month limit in current sittings. But if we decide something is worth reviewing, we shouldn't automatically close it or have pressure to close it because we are still discussing it. In the case of interesttarget, TAG members weren't giving it full attention which meant lots of repitition. But that doesn't mean it should have been closed sooner.

Brian: Huge problem in standards. You sink your effort into wrapping your head around the issue. There's sometimes a lot of history. You sink effort, write a response, nobody reads for 3 weeks, and it's gone from brainRAM. Never know how much to invest. Especially for interesttarget, I've been involved in discussions for 7 years. Definitely people lose patience. People want to say something timely, and direct in a helpful direction. Don't just object, give "if not this then what". Like timing things out: what's the position? "Abstain"? We pick less things, but pick things that at least one of us thinks are important to discuss.

Marcos: interesttarget: Feb 2025, we got an initial resolution in June 2025, then reopened and kept going until we re-resolved in June 2026. I forgot things, and then to understand it, I have to build it. I learn by doing more than my conceptualizing. With other members, have different experiences in different areas. Brian comes in for WebMCP comparing it to services. There need to be some respect and understanding that people process information in different ways. On timeboxing, the point is to have the intensity and mental focus. To limit things so we can get things done. Given TAG mission and goals, let's give feedback, and it's ok to get things wrong.

Lola: I did get the years wrong. Wondering if Yves' suggestion addresses the concern. Even though there were big gaps, we were talking consistently. There were a few gaps, but for the most part, even though it took a long time, we were actually discussing. Yves suggestion of noticing things that need prioritization. In addition to difficult things (interesttarget), we're also doing lighter things. Focus most of our attention on the meaty things. Regardless of anything, it'll take as long as it takes. Even if there's a limit, if it takes 5 days for a person to understand it, it'll take that time. Support prioritization instead. Maybe the people working on it have extra sessions to think things through.

Christian: Decided yesterday to automatically close issues that aren't picked up. We have priority labels already. That might address the point here. Just use them?

Yves: We might want to put priorities on the private-brainstorming repo. Could be used to set the agenda. 

Jeffrey: I need a more precise definition of those priorities and how they'll impact the agenda. 

Yves: I set up a bot for the formal-objection tracker with timeouts. We could define something that identifies the things with some time-urgency. 

Jeffrey: If we can parse a deadline out of the issue, that can go into the agenda.

Yves: We can identify charter and HR issues.

Christian: Can parse priority out of private-brainstorming. Noting for us that we need to figure out how it works exactly. Priority affects the order. Consensus to pursue deadlines and priorities.


### [Defining "The Web Platform" vs "The Web"](https://github.com/w3ctag/design-reviews/issues/1202)

Brian: Dan Applequist wrote a post a while back, "Yes but is it the Web?" (https://www.torgo.com/blog/2026/03/yes-but-is-it-the-web.html) It's very hard to nail down what exactly is the Web. Dan said that anything you can do in a browser is the web, and anything outside the browser is not-web. But that line isn't solid. But if everyone has their own interpretation of what the web is, then we're not all caring about the same things when it matters. When you mix in extensions, protocol handlers, webviews, miniapps, etc, are they part of the Web? Interesting fact: 317 standards have reached REC, and only ~23% are things implemented by browsers. So, meta question is: does it belong in the W3C? How does it affect TAG review? It seems difficult to write good legislation with limited terminology. It's also difficult to do something in a browser what you can easily do in an extension (e.g., cross-origin storage). What about other protocols? For TAG reviews, maybe we could design different models for different parts of things. Example: WebGPU is designed to be shared.

Marcos: WebGPU is not part of the standard web platform. There are opinions even here as to what should be considered. 

Brian: These are the lines that we need to have words for to discuss. Can we reserve "web platform" for manufactured materials that fit together in the general sense for use in the browser? We would have to consider them based on what they are being used for. PWAs are another interesting example. 

Jeffrey: You said something about how the W3C chooses to take work; that's not in our remit. But it is our job to be the W3C's architectural governing body and so we should have an opinion on the coherent body of work the W3C should be doing. My answer would include non-browser things. The web is things that link to each other; browsers don't have to understand all the things that link to each other. It's worth standardizing it even if browsers aren't involved. 

Yves: The web is everything which is reachable via URL, and that potentially may link to something else. That's what create the web - following all those strands. It doesn't have to be an HTTP URL. A web browser is one interface into the web. It has limitations in that it cannot process things (e.g., there may be a new file format that isn't readable by the web browser, but it can be fetched and used by a separate tool using web techniques). A text-based browser can't process images. A printer might print an HTML page, but it can't do animation. The web platform, if you link that only to the web browser, you still have weird definitions that make one question whether a text-based browser or a braille-based browser are real browsers.

Brian: Where that gets tricky is the characteristics of privacy and security. Some of these things are very different in the drive-by web browser world. So we need a word for this to say "these are things that apply this way to drive-by web but may not apply to embedded web."

Yves: The regular web browser needs to be able to run code from everywhere. That's why the security model of the web browser is very specific. You probably can't do that for isolated case where you know the interaction is with a URL that you control and that you won't cross boundaries. Within that context, you might say "I want to relax some of the general web browser things."

Marcos: These are great questions, but maybe they are too big. What do we want to do with them? 

Brian: The biggest thing is whether the answers inform the way we think about the advice we give to working groups about their specs and whether it's possible to think about these in different ways (e.g., different models about how you approach your spec depending on what you think it will be used for).

Marcos: What's not already covered by the design principles in our other documents? As a concrete example, yesterday we talked about how the Solid WG has overlap with the Digital Credentials work. Why is there this duplication happening? That's something for the TAG to step in and discuss. 

Brian: We don't really have one web, depending on how you define the web. Which means you'll have different answers to security or what you think breaks the web.

Marcos: It will be difficult, but we could start with the same-origin model as the foundation. That's already mostly defined in HTML and other specs. It's flawed in several ways, but overall it's pretty good. Where do we document that?

Jeffrey: We should think about profiles of the overall architecture when we think about each of these spaces. We need to define the core specification so they can be profiled; that might be the guidance we're missing. For example, extensions and AI browsing agent can violate same-origin policy. We (the W3C or WHATWG) should write something about the range of acceptable variation, then there can be a browser profile taht restricts in certain ways, but extensions, miniApps, etc, can do things differently. The IWA specs allow additional security rights because the apps are signed and presumably vetted by enterprise security, so there are things that would be allowed that wouldn't in a regular browser. We need the constituents to show up and tell us what knobs they need to support this change.

Brian: Yes, but we'd start by making a statement that this is worth doing. We could kick off a taskforce to discuss, as one option.

Yves: One starting point was the removal of XSLT from browsers. It is a decision from browsers that may not make sense, but it's balanced between what's available on the web, security considerations, and other points. Doesn't mean XSLT is not part of the web. It doesn't preclude a new browser from using it. 

Christian: It's really hard to define what the web is. I like the profile idea as it would help us segregate things a bit more clearly. The Web of Things demos at last TPAC further expands what might be considered the Web. 

Brian: We can talk about profiles and say "those things have different privacy/security models to them." The design of some of these has the user put their trust in more than just the domain; you're also placing faith in the whole trust framework. 

Yves: Maybe it's linked to the duties of the user agent.

Matthew: This is super interesting. I like the profiles idea and maybe different profiles come with different levels of responsibilities to different parties. Reminds me of the discussion in Hong Kong. We asked the question, if anything fundamentally changes the web, what would we want to keep? We had some good answers but they weren't technical things. 

Marcos: I am traumitized by the word "profile" given past history. They can fundamentally break the "one web" principle. Several items we're questioning now (e.g., Miniapps, TVs) have issues already in their architecture and what they break.

Jeffrey: We have WinterTC and it defines how the web and things like Node can use the same API and what needs to be variable (i.e., what the profiles need to be). Also, profiles are dangerous. Whenever we allow a profile to exist, we fragment who can view certain content. So, we need to define them very carefully, but it's still important to be able to define some set. The fact that Miniapps is merging into the web view space is progress because it reduces the number of profiles we need to dfine.

Brian: Then do we say everything is a web view?

Jeffre: No. IWAs and Nodes are different and would need their own box.

Yves: Profiles are the reason we have the evergreen finding. It was a strong reaction against profiles. But profiling on duties might be an interesting idea to differentiate between the things we see here. It would be good to have a task force for that.

Matthew: +1 to Yves. We have talked about how people struggle with what is the web and what is the browser, and which part of the UI you can trust (see https://emilymstark.com/2022/12/18/death-to-the-line-of-death.html). If a user doesn't know who is driving the UI, then it's hard to assign the duties. Also, in a practical sense, we talked about wanting things to run and work as long as they are plugged into the web. But sometimes we have security issues with patches or solutions that aren't supported by anyone. 

Sarven:  https://www.w3.org/2007/09/map/main.jpg - that was a map of the web back in the day. It has more of a view as to how it all comes together. It doesn't have a start/end. There are some expected behaviors and interactions. It's hard to say whether something is part of the web. I like the question but I think it's impossible to answer. The web is a thing to cause social change and enable society to move forward. Looking for a technical answer to that is hard. I'd rather more targeted questions.

Brian: My interest is in how we think about what we're willing to accept as work, and what we're willing to discuss and break it down in terms of security and privacy. There are many useful things people show they're doing by installing something, and those things don't cleanly fit the web model, but they don't seem unreasonable. It would be good if we could look at them to come up with some advice to guide them. 

Christian: The word Taskforce has come up a few times. What are the rules for creating one of those? It seems like an interesting path forward. 

Marcos: A taskforce is a nominated group of people. Where do we feel this would fit in our list of priorities? 

Lola: That will depend on the people who want to participate in the taskforce. Us as TAG shouldn't be defining priorities that limit what people want to work on. There should be an expectation of TAG responsibilities that have their own priorities, and then with that in mind whether they have capacity to work on this additional thing. So, answer the question when we know who wants to work on the taskforce.

Brian: I don't think that the priority of a TAG taskforce is any different from the priority of a finding. I would be interested in helping organize the taskforce, but I'm not going to allocate another 4 hours a week to do it. It would be part of the work I do for TAG. 

Christian: Do you (Brian) want to look for people interested in working on this?

Brian: Does anyone here want to work on this? 

Marcos: I'm interested in this area; I've been looking at this from a different angle. We'd need to determine how to tackle the problem. Is it new work, or is something missing in the design principles? Maybe we can have a breakout about that.

Brian: Maybe it's design principles. Maybe it's something missing in the user agent doc. I don't know yet. Maybe a breakout at TPAC? It would be good for TAG people to attend one already on the schedule from the different groups we've talked about here. 


### Service Discovery (including something better than .well-known)

https://github.com/w3ctag/design-reviews/issues/1243

Heather shares a few links: https://mnot.net/blog/2026/well_known_uris and https://github.com/w3c-fedid/identity-handler/blob/main/fedcm-827-vendor-lock-in-report.md

Matthew:  SERVICE DISCOVERY (title slide :)) - some background to start with... From my perspective the background was that we have seen a number of proposals which relate to facilitating service discovery - there is not exactly a 1:1 mapping beterrn the subdimain and the website (or app).  Approaches that use /.well-known ahve come up with their own solutions.. .Some use cases - identification and lookup.  Subsites can be located at diffferent parts of the domain tree.  There isn't a 1:1 mapping because you have logical subsites without their own subdomains.  It would be nice if we could classify the use cases, collect related proposals and see if there are related design principles we could come up with (more than what is there already) - finally - can we harmonize routing? So there are at least 4 proposals that this might apply to.  There was a big discussion on IETF DNSOP, there was the IDPs using fedCM, there's the at:// stuff offerss a few.  "discoverable destinations" is a thing going on by the adapt TF providing a mechanical way for the site to state the popular pages they offer, so that for example "login" "sign-on" "sign in" "log on" etc all "mean" the same thing.  In that we switched away from well-known and used link/rel and it means you have to repeat it. Maybe we could use linksets?  IETF (https://www.rfc-editor.org/rfc/rfc9264.html) - it is semantically equivalent to links and rel - so it's just one link you have to repeat.  Well-known url for changing passwords.  a well known uri for accessibility reporting.  You could use link rel types instead - if there are two ways, you have to try both and one has to be repeated.

Jeffrey: I feel like we don't have any particular expertise in this area. Our use is primarily in knowning who to talk to and pulling oon the cords - I also feel like we are not the right space to publish a document like this - this is a HTTP thing, it should be an IETF thing.  We could/should contribute to it - it would be useful for there to be a document that said here is how to make these desicions - when to limit it to subdomains or whatever - I doubt we can say "always do this" or "don't do this" - but maybe don't assume there is one controller in some of these cases.  

Marcos: I agree with Jeffrey.  Us proposing solutions is probably not the best - but I do think we have some precedent in some of the reporting APIs. The people who have expertise are logging things.

Jeffrey: If we aare excited about doing this we could develop something in the TAG space, we could propose an RFC happens.

Heather: If that is something of interest to more than just me, I would be happy to contribute.

Jeffrey: I would be happy to contribute 

Matthew: I put a link in to the reporting API... I think my main question for the TAG was whether we see a direction of travel here that we the community need to do something? Do we see more proposals, or am I just biased in becomming aware of them?  How big of a problem is this?   I think I am picking up that people aren't _worried_ about it, but think it is a good idea to remind people of the considerations they need to make.  Is there anything sufficiently big in that the reporting accessibility one, for example, the way it is specified allows you to do it two ways - it means you will have to send a request to a thing that doesn't exist?  It says you can do it two ways. I wouldn't want us to encourage someone to do something that was wasteful - I don't know. 

Jeffrey: I do feel like there is a consistent, though low level, stream of people confused about how to do this... .And I think Mark has seen this too or else he would not have written that post - I think there is value in writing it down.  I don't see a performance issue there - I am not worried about that... I don't understand what you meant with routing?

Matthew: If you the user are on a domain with a hotel site, and the hotel also has a spa and a gym and a restaurant, they might have sepate sub-sites - or some multitenanted sites like that, you have completely separate sites you can log into with entirely separate credentials - but they share a domain, so the .well-known doesn't work.  

Jeffrey: I would use this as an example in the document, and say something like "if this is your situation, you should probably use link relations"

Lola: I don't know if I understood your explanation matthew - are you saying it is possible to have example.com/gym and example.com/restaurant and they would have their own login flows?

Matthew: It's unlikely in those specific examples, but possible. There are sites that exist that do effectively that.  You find this sometimes when you go through a login flow, for example, you are redirected for one bit of housekeeping service, but they do it all on one domain.  

{General agreement that we don't like it but it's common}

Matthew: We gave them the tools to do it, and we have to somehow accept the organic nature of the evolution of the web.  Maybe we can come up with a flow chart and examples about how to decide, kind of like Jeffrey said earlier.  It seems like we are not trying to head anything off particularly - so that's good. It seems like there are bunch of us who want to do more on this - so that's cool.

Christian: There are a number of people who are interested, so if you want to coordinate the effort - whatever that is in the end - the action item is for the ... three? of you?  Jeffrey, Heather and Matthew

{ General applause }


### Docs / Explainer Skill
