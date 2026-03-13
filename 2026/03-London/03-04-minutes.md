# TAG Minutes - Wed, 4 Mar 2026 - London F2F

Present: Yu Sen, Xiaocheng, Jeffrey, Matthew, Brian, Christian, Martin, Sarven, Yves, Marcos, Hadley, Lola

Scribe: Jeffrey, Sarven

## Global Component Design Principle: downloads, computation (where), etc

Christian: Global components arrived recently. We see this principle in many on-device APIs. As it occurs more often, do we want to develop a design principle on this? If so, what should it say?

Christian: Several APIs including but not only AI APIs have a local mode. Including Web Speech. Either the data goes to the model, or the model comes to you. Could mean many things. Model could be downloaded to webpage storage. That's out of scope for today. Today we're talking about the model downloading to the browser's store, which is shared among websites.

Lola: Even if it's on-device, device might not be the physical device; it's the user agent. Downloading a model to a browser.

Christian: Could also be the OS level, but that's also out of scope. Talking about the UA's storage. Could also send both data and model to a cloud server.

Christian: Ehsan has described the problem space. Components downloaded after the UA itself, which are shared among web apps. UA could use the same model to provide UA functionality. Dealing with large binary models and artifacts. Motivation of using browser storage is that these are quite big. Don't want to download the same model over and over, cluttering hard disk.

Yves: Model is read-only?

Christian: Yes.

Yves: No learning and no exchange.

Ehsan: In translation, no training, but it could depend on the API.

Christian: Prompt API also.

Yu Sen: Is it executable? As in you can download scripts? When we talk about downloading and storing across boundaries, I'm afraid about whether it's executable.

Christian: On the next slide.

Christian: Model can be versioned independently of browser release. Either saved across releases or updating between releases. Can be hardware accelerated. Was a satisfied TAG review of Web Speech. Translator, Language Detector, Proofreader, Summarizer. All use the same principle. Want to make a design principle.

Christian: To use the Prompt API, 1 website has to trigger it. Once you do that, it downloads 2.4GB. This is small for a model. Different browsers download different models. Could run this using the Onnx runtime.

Martin: The executable nature: it's not software. It's a big matrix. The unsafe part might be with the outputs.

Christian: Came up again, with Web Speech. On-device was satisfied-with-concerns. Now adding an extension, to describe the "quality" of the model.

Brian: Different use cases. "Do you need something conversational, or is it commands?"

Martin: It's about cost/benefit. Big models are more expensive to run and acquire.

Christian: However, when Marcos and I reviewed this.

Hadley: Backing up, should the model be constrained by the same origin policy, or is it like a browser extension that apply for any website?

Christian: It can be applied anywhere.

Christian: The presence of the model can be a fingerprint. Can download multiple language packs, for speech recognition, translation etc. in theory, you as a developer can check for the availability of the language packs on the device, and you can install them as well. As a malicious actor, can install random language packs, and the combination could be unique.

Martin: The number of qualities provides 2 bits per language. There are enough languages in the world to uniquely identify everyone this way. My website can put a bunch of different languages on your computer, to create a unique profile.

Yves: Depends how you process language tags. All the subtags are even worse. And with translation, you get pairs of two language types.

Martin: Firefox does everything through English, so you don't get the square.

Ehsan: does it return the confidence too? If you have US-english, accents might be in different confidence areas.

Martin: My understanding is that if you have an English recognition system, it recognizes all English equally. No specialized recognition for different accents.

Brian: Doesn't seem like a single website would install lots, since they're big. Easy enough to identify and prevent. Stop a single site from loading multiple languages. But if it's identifiable whether you've installed this or not, could tell an awful lot about you based on which you've installed from anywhere. Say a particular adult site installs a particular language.

Christian: Installing multiple languages at once was part of the review in May 2025, and we appreciated that installs could be requested in the same call.

Jeffrey: Note that we could still restrict the number of languages requested at once, even though it's good that the shape allows it.

Sarven: Is this in the context of the user agent? What new fingerprinting attack does this introduce? Over the HTTP Accept-Language header? Since browser already exposes that.
I'm not aware of browsers making arbitrary decisions on Accept-Language, usually based on whatever is installed?

Jeffrey: Safari limits it to ~2.

Sarven: In Firefox, you can set multiple, and order them, and the header is based on the order. Does this introduce something more scary?

Christian: This is different because Accept-Language is user-defined. This case is different because the website can set the list. And can check. Developer defined instead of user-defined.

Marcos: It's the user who dictates what languages are exposed, and Safari limits to 2. In this case, website's initiate which languages are downloaded. Conglomerate owns several properties and download these packs to create a unique fingerprint. Website could also hide information. A principle could be that you'd never automatically download a language in the background. Always prompt to download a language. Brian's point about going to different websites to download a pack, to develop a fingerprint collaboratively over time.

Sarven: That clarifies. If it's not automatically downloaded, that's great. If it is automatically, if any website can install, would dilute the fingerprint. Malicious actors couldn't easily identify their subset of the list.

Brian: You'd use obscure languages.

Marcos: Availability would need to be origin-bound. So origin would request, and prompt user, for each language.

Matthew: Very interesting. Didn't realize how bad the fingerprinting might be. Agenda was 2 things, and I have a proposal on a different aspect, and want to reserve enough time for that. Jeffrey also mentioned it's useful to think of global components in a general sense.

Hadley: I was thinking about what patterns in this are familiar. Permission prompts and installing web apps already have some patterns. Have they come up?

Christian: Depends on the exact proposal. Prompt API proposal has no permission prompt. Installable web apps are different because it's UA-global. If you install a web app, it's executed by some engine, and if the installed app uses this API, it would use the shared component.

Jeffrey: A website can't query if another website is installed.

Hadley: User chooses to install a particular website. Would a user choose to install these models? Can we shift it to a model where the user gets something. I hear that the dangers are different.

Ehsan: Hadley's point was interesting. Is it correct to assume the global components are part of UA, and web apps will be part of the origin, but in a separate context?

Christian: We approved of languages; they're adding a second dimension of qualities. In this kind of API, we always see this pair of create() and availability(). We see that pattern repeatedly.

Christian: We worried about fingerprinting and excessive disk usage in the Prompt API review. Do we need to download languages that the user can't speak?

Brian: Did they reply about teaching?

Christian: They created a lot of issues and are working on them.

Yves: We had an issue with fonts a while ago. Solution was to limit how many you get. In this case, could restrict the number of calls. Don't want to list everything in one go.

Christian: Ehsan drafted a document. (https://docs.google.com/document/d/1eXgTEmyR-M-1y50bCeDdH4yvvm8wZYSRWTrrqz0dM6Q/edit?usp=sharing) Do you believe this is a problem space worth a design principle?

Marcos: There's a long history of this kind of thing. Web Fonts. Web Speech is old. Downloadable bits have a long history of issues and concerns and mitigations. For Web Fonts, could download independently of the browser. In the oldendays, you could call getVoices(). In FF and Safari, get an empty array. In Chrome, you get a list; don't know if Chrome does anything to prevent fingerprinting on that. The idea of downloading system components is questionable at best. I'm not convinced that this will become a thing. It's just from one implementer.

Lola: Understanding that we want a draft of something, what does this document contribute? Ehsan, Marcos, and I would work on the principle.

Jeffrey: Multiple implementers here. This area covers fonts and web shared libraries.

Xiaocheng: Is privacy the only issue we want to address? Or other aspects?

Christian: Not necessarily. Lifecycle, Discovery, Installation.

Hadley: Per Marcos' and Jeffrey's points, including the historical examples makes the principle stronger, and increases the importance of landing it. Helps new people see that it's not just a reactionary anti-AI thing; it's part of how the web works.

Marcos: Fun examples: There was once a proposal to Bundle jquery with browers. Similarly, SQLlite as the underlying store of IDB, with multiple versions. Shows what can happen when you bundle different versions of different things. Point in Ehsan's principle includes versioning.

Matthew: Overlapping proposal, which might not be global components. There are important lifecycle problems around installation and fingerprinting. We have a lot of these APIs coming up. Want to look at the question of where computation is being done. People might want things done in a particular place, or not a particular place. Can we enumerate the possible places? Simple proposal for how APIs take that into consideration.

Marcos: Personally, and if user research were done, don't think people would understand on-device vs cloud. If you get the same assurances from the cloud as devices, distinguishing is harmful.

Matthew: Enumeration of where things might take place. Don't think end-users would understand the distinction, but might have a privacy tolerance, and could agree on different zones. Might also be legal mandates. Jeffrey suggested "Personal devices in secure enclave", "On your personal devices not enclave", "remote with a technological guarantee of security", "remote with a promise", "remote not private". Secondarily and handshake between the app's request and what the user will tolerate. Use cases range from the UA calling things provided by OS. Sites using an API provided by the UA. Sites providing their own model. Should we do this consistently across APIs? Make it easier for the UA to ensure the user's preferences are respected. Some platforms provide in the platform a switch to ask to do things on the device. If a platform provides it, UA shoudl be able to do the same.

Jeffrey: Secure enclaves aren't secure against local attackers. Cloud can't be as private as local.

Marcos: Site can be the attacker. Could do the processing on the local device and then upload the data. Who do you trust?

Hadley: Matthew thought it could be helpful to ask the user ,even though it's reasonably technical. Most browser have a "block 3p cookies" option. Maybe users don't get that, but those of us who do, appreciate it.

Ehsan: A benefit of this enumeration is the privacy analysis of other specs. Lets us clearly state what the API does. https://github.com/webmachinelearning/translation-api/issues/72. This could be more helpful for specs than users or developers.

Matthew: Helpful and interesting. Please look at the document. Will digest.

Martin: Think this is a useful taxonomy. Online someone mentioned that you might use other devices you control, so that's another item for the list. I think the "personal-secure" one is a mistake. TPM is usually to assure other people that you're not doing certain things. It's less personal control over the computation.

Hadley: What are we goign to do with this discussion? Design principle. Have the bones of the discussion. If we get TAG consensus, what will be do?

Lola: Add to the Design Principles.

Hadley: Write a Finding too.

[general agreement]

Hadley: Can we do that this week?

Matthew: Maybe an outline next week. Not sure the computation location and downloading is the same thing.

Hadley: When does this need to be done?

Martin: Already shipped.

Christian: Things are still in progress, but close to shipping.

Hadley: Aim to publish by the end of March? Have a draft the week before? Aim for March 24th? I'm imagining this doesn't need to be more than 3-4 paragraphs, but could be longer.

Marcos: Reminded me of Do Not Track; maybe some parallels.

##  Web User Agents

Slides: https://csarven.ca/presentations/web-user-agents-tag-f2f

Sarven: Overview of current state, and questions. Hoping we get some next steps to move the work forward. Have a Draft Note. Next step is Group Note. Want to figure out when this is a Group Note. Can continue with more updates after that. Overview of current document:

Sarven: Duties: Protection, Honesty, Loyalty. Expectations from a web user agent are both what we see in practice and how they're aligned with privacy & design principles.

Sarven: Document is intended for technical authors, UA developers. Those were original target, and introduced web developers, regulators and policymakers. Added people who could look at the document and say "we expected UAs to behave this way, but they're behaving this other way." Other groups could refer to this in their own processes.

Sarven: Duties come from the Privacy Principles.

Jeffrey: And were Robin Berjon's in the first place.

Sarven: They have a more constrained description in the Privacy Principles. This document elaborates some. Could collaborate with other groups.

Marcos: Realized that a Note prevents us from citing these normatively. "These Notes must not be cited as W3C standards and may not become statements". Might need to publish this somewhere it can be a normative reference.

Hadley: I'm not reading this the same way. In 2.5.2, ... This it's a question for the spec author of how stable a note is. No reason not to cite them.

Lola: Direction is to eventually make it a Statement.

Jeffrey: Agree with Hadley for Notes, but we also should progress this to Statements.

Sarven: Web User Agents doesn't have anything normative. Other specs would refer to things browsers implement. Web User Agents isn't strictly technical; also specifies duties, which aren't normative.

Jeffrey: I think this is fine, but it's reasonable to ask the Team and adjust (publish it as a REC) if necessary.

Hadley: It's useful for the TAG to say what we think a User Agent is. If a WG wants to use a different definition, they can, and it's outside the scope of what we need to do.

Marcos: Hadley's right. Every web spec that names a user agent points to Infra's definition. Bikeshed and respec check and complain if you include an informative reference in a normative statement. Multiple people are defining multiple things. Defining the term, but also trying to replace the Infra definition. Want to be able to reference it.

Yves: To echo Marcos, you're allowed to do informative references to anything, but normative references only to Rec-track documents, or to Statements. Can't do a normative reference to a Note. "User agent" was defined in Architecture of the WWW. Use another term to avoid clashes?

Hadley: Presumably we can update the WebArch definition? Might not want to.

Sarven: Most of these definitions are brief. Whether it's a Note or Rec, document should exist.

Sarven:
* If at all, which external developments, e.g., governance, regulations, should this work explicitly address or be aligned with?
* What concrete implementation barriers exist for user agent developers?
* What measurable risks or harms could arise from misaligned duties?
* Does the significance of duties differ across diverse (web) user agents?
* How to take into account user agent's internal decisions or rationale towards the duties (which may not strictly align with the individual's expectations of user agent's duties)?


Marcos: Implementation barriers question goes to where it belongs on the Rec track. If this makes normative requirements, it would need to be on the Rec track.

Yves: If it's a Note, it can become a Statement that could be normatively referenced.

YuSen: When we talk about barriers, there are many duties in the document. Want to know what duty is MUST and what is SHOULD. Only the MUSTs will prevent the UA developer to implement it. If it's optional, it's not a barrier.

Xiaocheng: Who is this document speaking on behalf of? Users, UA developers, regulators.

Jeffrey: This document is speaking on our behalf, to all of those groups.

Xiaocheng: Conflicts of interest. Document says UA developers need to put users' interests over the company's interests. Companies make business decisions, and don't work on users' behalf.

Lola: The priority of constituencies says to put users before ... before implementers. Nobody's going to put them in jail if they don't.

Jeffrey: Regulators might.

Hadley: We talked a lot about this when we wrote the Ethical Web Principles. There are lots of reasons for people in the web community to have other priorities. We were writing down what we, the TAG, thought, and we wrote it down because we kept putting those principles in our design reviews.  Wanted to write it down in one place instead of over and over. Company might decide to ignore this and act in the company's interest, and then they'll see why they get resistance from the rest of the community. If we have consensus.

Jeffrey: the world is better when companies don't just act in their own short-term interest. Part of the web being a commons is that everyone pitches in and helps other people, and by working together we get better outcomes for everyone. These duties are about how user agent developers can do that.

Xiaocheng: Summarizing, "this is how the TAG thinks the web should work to maximise user's interest"

Jeffrey: maximise everyone's interest. There are positive sum games. By looking to users first, we improve things for everyone. WE need to be looking for ways for companies not to do that. Regulations are one way, community norms or another. This document helps to set the community norms.

Lola: There's a benefit to having documentation on the expected behavior, even if the audience doesn't do the expected or ideal behavior, because it's a way to hold companies accountable. Some companies have changed their mottos because it doesn't align with the ethos anymore. There's a benefit to have documentation even if we wonder why business would do this.

Brian: This is all interesting, and want more time to look. Lots of interesting open issues that are worth discussing. Priority-wise, looking at the CRA (EU Cyber Resilience Spec) browser spec. They're looking for definitions of some things that are in some of the questions. Embedded browsers. Headless browsers. What defines a browser. Where do responsibilities lie? Is anyone attending the CRA discussions?

Jeffrey: ETSI put together a browser spec, generated by Claude. Simone said they have just accepted that they need to re-do it.

Lola: Seen some emails. More in the SWAG group, organized by Simone.

Brian: I've gotten liaison/observer thing that'll get me into 3 meetings. We can join in several capacities. Eligible for liaison as TAG. Answering these questions makes sense, and it would be good to answer regulators who are asking right now.

Hadley: I'd love to help, time permitting.

Sarven: We need to identify these questions, and what needs to be fleshed out. It's written from an internal W3C view. Don't think we've heard much from external people. Would stand better if it was more holistic.

Lola: Do you know other communities or organizations that might give feedback?

Jeffrey: ETSI?

Hadley: WHATWG?

Jeffrey: I think I've shown this to Anne, can double-check

Brian: Put it on a WHATNOT agenda.



## Age Workshop Report

https://www.ietf.org/archive/id/draft-iab-agews-report-02.html

Martin: Is the Report from IAB/W3C Workshop on Age-Based Restrictuions on Content Access asking the right questions?

There are takeaways from the conversation - some are interpretive / based on what we heard from people.

The broader conversation on the topic seems necessary.

We made progress on identifying key roles, some of the architectural work during the workshop. We mentioned everyone agreeing on the language used. It references the ISO-IEC doing most of the ground work.

Interesting takeways: trust and privacy has different expectations on people's minds. It shows different angles.

The common thing that was pointed is different mechanisms have different application domains and characteristics, and not necessarily applicable everywhere. May need multiple tools.

The balance between sure that someone is old enough and some of the consequences that come out of that. The more definitive you need to be about an outcome, but if I wanted to be more sure, then I stand in a higher risk of excluding you. Gets interesting when they're deployed.

Discussed different deployment models, e.g., parental control deployment model.

Lola: is there a preference to the models?

Martin: Neutral because they were contested. Some nice properties in some, e.g., website liability if certain things end up being available to a child. Then again, circumstantial and errors are possible. Is the system fundamentally flawed that a child gets access?

Xiaocheng: In this model, who owns the content?

Martin: Typically the website, the distributer of the content.

Xiaocheng: What's the relationship between?

Martin/Brian: Role.

Martin: The entity that decides some content is shown to only to an 18 year old or older. Understanding that this content is restricted in some jurisdiction but not in another.

Hadley: Did we choose a best model is a question? Different participants in the ecosystem put a lot of money in a solution. It was more useful to have descriptive than answer the question.

Marcos: WebAuthn for example has a token for age verification ... the wider discussion on DC API doing age verification, but can't do it.

Martin: My perspective on this is limited.

Brian: We had a podcast with people from W3C and saying that DC being used for age verification is common.

Marcos: Its intended purpose is for other things. But becomes a proxy for age verification. Workshop output being that it can be used for a range of things. IMO, DC API is bad for age verification. Why the DC as a primitive is a thing but ??? bad for API.

Hadley: Is this something we should say as the TAG as a statement? Easiest way to get it out there b/c the WG won't.

Martin: Important to get all the context here. The use of ZKP, acquired drivers license matched with DC for age verification, deployed in this country (UK).

Brian: How can I understand what's bad about it?

Marcos: Given this report, as the TAG we need to look at what's alreayd out there, the principles achieve with the thing. It is used and how does it sit with the web? We want to have a solution but encourage people to ??? Ideally as the TAG we should encourage ... yes, DC is a solution but there are other. Not a solved problem. ZKP is fantastic / has potential issues as well.

Lola: It'd be good to have some kind of session that Marcos can give on what makes DC inappropriate for age verification - it seems like for different parts / understanding of DC at W3C, and we should be on that understanding.

Martin: The report doesn't capture these nuances. But to start talking about these type of things.

Hadley: If we are going to write something: who are we writing for and what are we trying to say? I'd recommend we don't have one document to say both, but want to be clear on the message we send.

Marcos: DC is a solution among others. These are the bits that need to come together for a hollistic solution. DC primitive which we may not have, are needed for an overall solution but alone DC doesn't, and perhaps even introduces some.

Martin: One of the biggest conclusions for this problem domain is: Safety Requires More than a Technical Solution. If your goal is to safeguard the wellfare of children, then age verification is not going to cut it. Technical solution will be blunt and fail to capture things that are very difficult. Making sure that people are able to access various important topics / concepts, when making a transition to adulthood. And so they don't accidentally get caught by the system. For example, sexuality, or body dysmorphia, and they might not be caught by filters and profiliterated on social media. They effectivelly check for patterns of behaviour, like surveillance. It is not just blocking content but more than that. Blunt force is never going ot be able to give you. Supporting children towards adulthood, these are not magical solutions.

Marcos: Examples with kids lying to use a service. There is a worse effect. They'll be targeted as ???

Matthew: Quite helpful to see that you came back after the wrokshop, decouples age verification from id verification. DC couples so obviously not a good way to solve the problem. Not sure if that's too explicit in the report. Can you give us some good news?

Martin: Follow-up will do that. If the TAG wants to say something that would be a good thing to say. If your goal is age gating, then maybe find a separate path.

Hadley: +1 to the examples on different kinds of harms. If it is not too late to pull that out into its own section to help people.

Martin: Section on Safety Requires may be a good place for that.. with concrete examples.

Hadley: Or maybe in a table or something to make it jump out.

Brian: All these examples are protecting kids from "protecting kids". Everyone doesn't agree on what to protect them from or until when or how. There are some clear things in our podcast, there are traditional things that are age gated, cigarettes or alcohol, or rent a car, where we have gating already.

Martin: Common one is online gambling. Different from restricting access to adult content. For gambling, by law you need to identify the people. That also true for a lot of other ones. Like car rental company, need to know who is driving for liability and other htings. Not necessarily the same for cigs and alcohol. Website doesn't actually care at the moment the money changes hands. At the door they'd expect an adult at the door to hand over the things.

Brian: Could leave cigs at the porch.

Martin: Shouldn't. Isn't actually effective. If anyone taking the law seriously, they wouldn't.

Jeffrey: If someone uses for cig restriction, it'd be at the point of giving.

Christian: another use case, in DE, making real-names mandatory, and DC is a solution as it enables all of that. The nature of that is that this is super controversial but could we publish sometihng that says all this stuff on impacts...

Martin: Appendices cover... potential impacts. Collected various things to consider when designing the system. very hollistically. List of impacts is quite long. Desirable properties for any resulting would have. A lof things to take into consideration.

Christian: ... social media ban, age verification, ... they all come back to the same point. It is not the DC API itself, it is the issue of tryin to do all that stuff.

Martin: There is a lot of backgournd on real-names online. Unsurprising but disappointing to see politicians still talk that way.

Marcos:


## Technical Strategy Task Force

https://w3ctag.slack.com/archives/C08F69VR1MJ/p1772561644278599

Lola: A bunch of TFs started last year-ish. They're all about on how to implement the W3C Vision. Current state of Technical Strategy (TS) TF. This isn't what the BoD expected :( Thought we could discuss here on some of the questions that came up.

One BoDirector suggested to ditch the funding on investigating games unless Members want to prioritise them. What should be the focus for the next 2-3 years? Also risks/opportunities for AI.

So, what should be our focus for the next years? Are there any technologies / architectural things that need our focus, attention, prioritisation? Bear in mind that we'll talk about AI. If AI si the only one, that's okay too.

Matthew: W3C is a doacracy, we incubate, develop - bottom up. The TFs seem top down.

Lola: The outcome is still to be determined. I don' tthink we wan tto get into the habit of telling WGs what to do. re gaps, it is about looking for places, e.g., MathML would've been something good to invest in but people need to money behind it so it can get done. Other things like with W3C, can look at how the web is moving and putting energy behind it instead of responding to it.

Marcos: Stuff like in Devices/Sensors and AI, .. all these things like Bluetooth,.. bunch of APIs, good ideas/use cases but never really got adopted. So, architectural question despite being interesting didn't get taken up. ... In order to get there is fragmentation.

Jeffrey: It sonded you're saying, get lagging implementers to do stuff from these groups.

Marcos: What I'm saying that'd be the ideal outcome. For instance, Apple did WebPush, we first need to install the webApp and these capabilities. There is sometihng there, that I haven't quite got it right.

Jeffrey: If we're not allowed ot fund anyhting and coarse certain players to work on things, then what's the point?

Brian: By that do you mean the TAG specifically or the TF?

Lola: The TF.

Brian: A lot of what Marcos says resonates with. Also what's adjacent, WebViews, MiniApps, .. there is a lot of stuff that's not quite standard but trying to. Good to step back and assess those. Maybe we can't make it all of them happen. How to get all the cats go in the same direction?

Hadley: If we are going to fund things - not sure if we're - that's an open question. No one wants to obsolete stuff. There is work there to do. It is not exciting. No company wants to. It'd be a good thing though to be funded collectively.

Yves: Clarification on what Marcos and Brian asking. Identifying what didn't work: ... finding the missing piece that people didn't realise the need.

Xiaocheng: Is the TS supposed to identify the technical areas to focus on or - b/c I remember setting up groups to identify these areas.

Lola: From the BoD, the TS TF.

Jeffrey: Hesitant to say to focus, the WG should do what they do. I liked Brian's point on novel UAs, that needs some unification. There is some interest there from a lot of groups. The other question about disfavourites - and instead of letting them drift how to make them work together.

Lola: These don't have to be specific. AI might not be a good example. Areas more input or research. We should also prioritise.

Matthew: Echoed a few times, this is a TS, and this is technical debt, and understanding that. Re next 2-3 years, I'm still trying to undertsand why this is being asked. Unclarity on communication. They've given some clear feedback but do we actually understand what they're expecting or what prompted them. So, not sure what BoD is expecting.

Hadley: We have a clash of community operating bottom-up, individuals coming up with ideas, and building stuff. BoD is thinking we should do top-down. I don't know how to solve that.

Sarven: Suggest workshop series b/c they're focused on problem spaces. W3C should do more of those to inform the community on direction / next steps.

Brian: If we've been working on x,y,z - if all these things are trying to happen but not happening - we have a lot of work and expertise on it already, it'd be good W3C to use the critical mass and expertise to make something happen. We have a lot of investment already. Continuing to do sometihng but not succeeding.

Lola: Talking about AI, 2 questions: based on the design reviews we've done, what risks or issues do we forsee? e.g. downloading system components.

Hadley: One risk is that a lot of the work is being by companies outside the W3C.

Martin: AI Interoperability Forum; Agentic AI Foundation (in Linux Foundation), doing MCP

Christian: Very new.

Hadley: Moving so fast that traditional standardization isn't working.

Martin: A lot of interoperability is being defined by software rather than standards.

Jeffrey: Hard to test: "Is this a good translation" is something only a human or maybe another LLM can judge.

Christian: There are tests, but you get a percentage for the success rate.

Martin: Need a subjective analysis, which itself will be wrong sometimes.

Brian: Risks are difficult because there are probably privacy and security risks, but those migth be outside what we're able to do. Worry about models being private and safe. Don't know that models have a concept of secrets. If they can be shared across sites, and you give it secret data, can probably convince it to give it back to you somewhere else.

Jeffrey: When apps are embedded in chatbots, can the chatbot keep one app's data private from another app? Power dynamics when users come through another app.

Christian: Where do models come from? Vendors with their own models can do it, but what about browsers that don't train their own models? Hardware compatibility: users with incapable hardware might have to go to the cloud. Ethical AI document.

Xiaocheng: Permission management for AI agent: We think there are 2 kinds of actors: user and script. We trust user actions more than script actions. With agents, I imagine something in between.

Yves: Brian's point about exchanging information between sites that are using the same model. Linked to my question about read-only vs learning. If they're not learning, it's fine. Otherwise a huge issue. Subliminal learning in models is interesting. 2) A main danger is that you go one place, download a model like translation. Model might be trained to give inaccurate translations of certain topics. Relates to UA-should-be-truthful. Actively deceptive models.

Brian: Isn't that also true of today's speech systems? Could purposefully train Azure/Google/etc or the OS to break trust in the same way. Most browsers delegate speech to another system. Have to trust. Is the AI version different?

Yves: Not if the browser can only download models that the browser vetted. Otherwise there's a risk.

Hadley: We'll have to update the priority of constituencies if we have agents as users of some type. We shoudl be explicit what it means.

Brian: We should say the user is a human. e.g. Google is not a user.

Hadley: If you're designing for needs, might design for an agent over a human.

YuSen: As a model, we can talk about browser being wrong "in the browser" or "in JS". If the model runs outside the browser, and performs an action to the browser or page. Re Xiaocheng, the action should be trusted. Action performed by model is equal to action performed by user.

Hadley: Are you suggesting the model be in the OS?

YuSen: In the browser. Chrome published a chatting tool to chat with user and help user to operate the page.

Jeffrey: Heather has thought about this a lot, so we might talk about this more when she’s here. A current problem is that the browser runs an agent on behalf of the user, the browser can’t distinguish between the user and the agent. If the agent makes a mistake, it’s on the user. This is a problem.

Christian: I expect both things to happen. You'll have AI models/agents controlling the browser. But currently this is too slow. Like with aria tags, model tries to understand the page as a human, but it's more precise if the page can declare its tools, so WebMCP. And it can happen that the page is _only_ understandable by the agent.

Martin: It's like lowering a ladder so the agent doesn't have to climb all the way.

Martin: We've been discussing the possibility that treating agents just like humans is a category mistake. With WebMCP, you have the opportunity to treat them differently. Positive and risk: Positive: you can build systems like purchasing systems that always have an undo. In the human decides the agent went rogue, human can cancel. Web page needs ot understand that if the agent makes a mistake, need to be able to cancel. Risk is that you can present something different to human from agent. Deceive agent, maybe to charge too much, and then present different audit to human. And don't know how to manage those risks.

Matthew: Weird that all of a sudden everyone cares about contrast ratios. And depressing. Doing things more semantically is good. +1 to Martin. And there's a fine line. Some things we're proposing to help humans which will also help machines. There seem to be proposals where things that were supposed to help humans are being primarily used to help machines. Like stuffing things into ARIA. Discussion at TPAC, and the fact of the question was concerning. Won't say we shouldn't design specs to make machines' lives easier, but we should design the web to make things better for humans. Maybe less fragmentation is needed than you'd think. Semantics can help both.

Brian: There are a number of browsers that aren't doing things with APIs, but are building agents into the browser itself. Would the TAG like to say anything about that? Need to sandbox appropriately.

Martin: Or YOLO browser.

Hadley: Stuffing things into ARIA to tell agents about the website. That goes against ethical web principle on keeping the web from getting too complex.

Martin: Normal people can't build accessibility features?

Hadley: An additional layer for instructing agents makes the web more complicated.

Matthew: Distinction between what we actually need to add to allow experimentation.

Lola: What opportunities do we see from design reviews we've seen.

Christian: I'm generally AI-positive, despite risks. Can build great user experiences. Natural language can describe a solution. Other end is OpenClaw where it just sends emails. Sweet spot is to let me review. Can do a lot of work for us.

Hadley: Remove a lot of friction. Talking to Sam about how difficult forms can be, and the basics of web interations being klunky. Leonie presented at GS1's global forum about how she went through the shopping experience as a blind person. Put up a product page that showed a black jumper. Alt text said "this is a black sweater". She wanted to know if it was itchy, how far it went down, texture. Switched to Innosearch AI. Could ask questions and get feedback and dig into the photos. "Does it look more comfy?" Accessibility case is strong.

Matthew: It's so profound. Leonie has done the same talk where it makes up loads of stuff, and it gets it wrong. It's tantalizing, but you can't know if it's saying the right thing. If it works, it's phenomenal.

Martin: Dual problem: people ask chatbots and search engines for answers to questions, and get answers. Web was very bad at answering questions because people are making people watch ads before answering questions. Basic facts and knowledge become accessible. That's a fundamental change. Comes with the risk of destroying livelihoods.



## Powerful Web Platform TF

Christian: Wasn't my idea. Was from Dan Appelquist, Lea, and Sangwhan, 3 years ago. During TPAC 2023. I try to represent web developers. There are basic capabilities on native platforms that aren't fulfilled by the web platform. Want to bridge the gap between native and web. Also have platforms that bridge the gap, like Cordova/Capacitor, Electron/Tauri. Isolated Web Apps effort, which requires packaging and installing apps. MiniApps, Project Fugu.

Christian: TF wasn't started. Situation hasn't really changed. Web apps are now installable on all engines and platforms. There are regular conflicts along this line. During DAS review, Prompt API. I believe it would be a good idea to relaunch this TF.

Christian: TF speculated about an additional "powerful" context. Like Cordova does. Marcos' catchphrase is "why does my bank website need Web MIDI?"

Martin: Because it wants to fingerprint you. Chrome didn't have a prompt, so bank could enumerate devices, which provided more fingerpriting.

Christian: There are countermeasures. Should installing the app grant more power?

Hadley: You're proposing reopening the TF. Are you proposing that we product these deliverables?

Christian: This is context. Hoping for consensus positions.

Jeffrey: Good luck.

Christian: Not promoting any particular vision of the future. When this was presented, reception was in factions. I'd love to install fewer electron apps. Priority of Constituencies implies the task force should promote user needs. Current actions: conversations in WebApps about installation of web apps. TPAC discussion about proposals to let a website suggest its own installation. Came together to discuss various proposals. We touched the question of whether installation is a signal for getting more capabilities. E.g. in Safari need to install to get push notifications and badging.

Lola: When you install an app in iOS through the App Store, you get a notification to say that installing this app has these implications. If that happened on the web ... for users, if I install the app, I assume I'm giving permission to do a set of things. Issue is that those things aren't necessarily the things the app needs to do. Assuming that install gives permissions goes down a slippery slope. But permissions prompt as part of installation, maybe that's not horrible.

Martin: People's expectations vs reality. Apple's approach is pretty reasonable: if you have something on the homescreen it can get a badge. But installation doesn't imply the filesystem, Bluetooth, etc. General theory on permissions is that the up front ask-for-everything model doesn't work. You ask in context. Not just the prompt that carries information, but the context in which the prompt appears. If you ask for geolocation, that prompt should happen when you interact to require geolocation. It's better, even though the apps don't always do it well.

Lola: One thing on the other slide was permission fatigue. If you download a map application, as a user i assume it needs my geolocation because it's a map, and I'm downloading it to do map stuff. I don't think a prompt is necessary. Good, but can assume downloading the map implies consent.

MArtin: System can't know it's a map application.

Lola: Having the permissions up front, when it's specific like that, is fine.

Jeffrey: This conversation is about specific questions that the TF would be trying to answer. The question should be, do we want a TF on that?

Sarven: Lola's point is sensible, but there's an assumption that the store, or whatever can install the app, assumes the app is only asking for what it really needs and not extra things. If the app limits itself, that makes sense, but if the app isn't trustworthy, need to ask.

Xiaocheng: Wondering what are the arguments against making the web more powerful?

Jeffrey: Often disagree with these arguments, but it is dangerous. When you can connect to a device via Bluetooth, you can hack the device back. Chromium has decided to take that risk, while the other vendors have not.

Martin: Another aspect is the distinction between capabilities. e.g. want web app to make a TCP connection to an arbitrary host. The use case might be "I want to access my email or the light switch". TCP capability presumes that there's nothing that can happen on the other end to facilitate using a web app. Email can definitely change. Most people use web mail. That's a better outcome. Should focus on the use case. E.g. if you want to load firmware, can provide a dedicated UI for that. Tension on the web between building high level or low level APIs. USB is interesting because you can connect to a lot of devices through over other APIs.

Christian: Trying to gather with vendors to see if there's a path forward for an install API to let an app install itself. Might be design reviews from that.

Martin: Microsoft had a proposal a while ago. What's new?

Christian: We have beforeinstallprompt. Microsoft proposal in various forms. navigator.install(). During TPAC last year, there was an "install button" PEPC proposal. Can we make that declarative button? beforeinstallprompt is widely implemented. Trying to standardize. This discussion might shift to ask about what apps are able to do once they're installed.

Christian: Is there consensus to bring back the Powerful Web Task Force, with all vendors on board? Multi-year effort.

Hadley: Process & procedure: What part needs to be done in the TAG vs elsewhere? What deliverables do you want out of the task force? e.g. document of what apps should be able to do, signed the TAG?

Christian: Formalized process. We're discussing in Web Apps for many years. It gets forgotten. Declaring capabilities on install. Looking for a more formalized process. Task Force promises that.

Hadley: Could do a joint task force with WebApps. Deliverables?

Christian: Document we could point to. No continually improving document so far.

Hadley: Warning that it would be a shame to use TAG time because a WG can't prioritize like people would like. That said, there are quite a few architectural angles, and could use TAG time to discuss those. Want to keep the focus on which parts belong where. Don't know where the answer is.

Brian: https://github.com/w3c/miniapp/issues/215#issuecomment-3823712994 at TPAC last year, there was a joint session between miniapps, web views, others. A relevant topic is that miniapps is rechartering and is frustrated about where they're at. Should get those people together. Interest from IWA folks, miniapps folks, Cordova, Microsoft. Not currently in webapps, but spread in a lot of places. Task force seems useful to lay out guidelines. See whether it should ultimately be taken up in any particular place.

YuSen: Re miniapps rechartering. The different miniapp vendors in China, there are 2-5. Difficult to reach consensus. We don't make decisions about lifecycle or APIs. Especially WeChat doesn't participate in any standards or community. They are the standard and don't care about others.

Martin: Procedurally, interesting. What does the TAG contribute? At the high level, looks like what WebApps is doing. I'm not sure it should be anything. If it were me, it would be an answer you don't want. I think one of the core strengths of the web is that you don't install. It's nice browser feature, but it's fundamentally still just a website. Good to be able to follow a link in and out. It's very different to want installation. If you use the installation ceremony to bridge into a different experience, you're not talking about the Web anymore. It's fine that Electron, etc, can do extra amazing things, but not a lot of interest in bridging that. That said, we want the web to be more capable. We want the capabilities that make the web more able to do rich experiences. If you want AR capabilities, or interaction with physical devices, but they need to be designed along the Web's principles. Security model, interaction model. Preserve the casual nature of the web. Sometimes that's hard. Requires creativity. Means you get WebTransport instead of TCP. Maybe TAG can help with some of that.

Jeffrey: I have a similar answer to Martin. On 1), installation is inappropriate to gate most permissions. For most permissions, it will not help users to install something in order to grant certain permissions. I also doubt that we can get consensus on "we should add capabilities in this way." I’m most attached to the device APIs, and believe that WebUSB should be allowed for these reasons, or disallowed for these. Didn’t reach consensus on this, different opinions on what the trade-off should be. Also think that your idea of writing a document is good, but don’t feel like a TAG TF is going to accomplish anything in this area.

Sarven: I'm interested from the point of Web apps. Would this initiative cover the discoverability and description of application capabilities and needs? Strangely I started some work on this but wasn't sure where to take the draft. For instance, features and CSP. There is a lot of related work. But think there is a gap. Should this be covered by existing things like App Manifest? To be self-describing. App could communicate its needs to its hosting server.

Christian: Probably outside the scope I'm thinking of. We discussed what should be installable. e.g. "does it need a manifest ID"? Consensus answer: doesn't need a manifest.

Sarven: Focused on native apps?

Martin: No, just saying you can install any website.

Lola: At Boucoup, Google wanted to contract us to do some Web Bluetooth stuff. Some members were uncomfortable. Read the postmortem of those discussions. Do think this is worth exploring. Think it's an issue that you can do things in native that you can't do on the web. Sign of illness that people are going non-web places to do things that, with a little time, could be done on the web. I support exploring options, coming up with potential solutions. Don't know that the TAG has active involvement beyond reviewing things. I support forwarding this work. Don't know about the name. Don't know if I know enough to contribute meaningfully.

Christian: Vendors have expressed interest to run beforeinstallprompt through TAG review. I'm not sure this TF would be successful in Webapps: we need an independent set of people. WG has mostly people from the 4 vendors. Neutral perspective would be helpful. But could also continue the install API things in the WG, see what the result is, then come back.

Hadley: In our repo, there was a discussion on the concept of PWAs from 2017.

Brian: You'd said it's fine that Electron, Cordova, etc. But there's a lot of those in our lives. Billions of devices running web tech. Dozens of glorified web views. They share nothing. work differently w.r.t. trust and permissions. Maybe they're not a browser, and you don't install them like the web, but we should care about them.  People follow a link, download a .dmg, install, and it's using web technology. It's an abdication to say that's not our problem.

Hadley: It could get dramatically worse if excluded.

Brian: Worth doing what we can to get all the people who feel their needs aren't being met, and see how we can do something. Install prompt, or something different? Or spec of something that's not a UA.

Sarven: On the name, suggest a new name. "Powerful Web" didn't mean anything to me.

Hadley: Agree.

Yves: Don't see a huge need for a Task Force. TAG will review it anyway. But if it's a way to get people from the WebView CG, would be good to involve them. Everyone from the TAG is welcome to comment within the WebApps WG.

Brian: And MiniApps, IWAs, etc.

Yves: WebView CG came to mind as a good source of input.

Matthew: Roller coaster of a discussion. Installation step being the gate is perhaps an indication that it's less safe. But if we want to preserve what makes the web the web, and just use things, then we need APIs that fit the Web's security model. If this is accessible via the web, then raw sockets will never be acceptable. So bounds on what's not acceptable? Some of what this group is doing is highlighting and spinning out work on APIs that represent missing features. Other aspects that cover webview apps that we still want to take some responsibility for. 2 streams of work. Could use this work to do developer research. Not convinced there needs to be an API to install these apps. But lack of sharing is vexatious. Seems like this needs ot be a CG because it straddles too much. Name is confusing. "Powerful features" definition is circular, based on the permission prompt.

Jeffrey: The powerful features definition is my fault. Needed a term for a feature that needs permissions. This confused TAG.

… Feels like we have three different topics: 1) Installation, which has an API, a button, … there will be a TAG review for that. But installation should only affect a couple of capabilities.

Martin: Yes.

Jeffrey: 2) We have capabilities, that should match native, and there is disagreement about what is acceptable. 3) There is web views, MiniApps, many things. Electron apps exist to give more powerful capabilities to things that are otherwise using web technology. That space needs coherence, but I think this is distinct from the capabilities question.

Christian: Yes.

Jeffrey: Don't think we should stuff the two together artificially. Don’t think that the TAG has a role or will find much consensus on capabilities. The MiniApps WG, probably renamed, would be the appropriate place to discuss this. Want to make sure that we charter any task force cleary. I’m ambivalent whether someone works on the capabilities thing. Been there, done that.

Hadley: Not as chair, I was thinking you have the option of a WebApps Task Force, wher eyou could chair, drive to a conclusion, and not be derailed by other things happening in WebApps. At some point in this discussion, I want the TAG to agree on whether or not to make a task force.

Xiaocheng: An example of why excluding Electron/MiniApps is causing harm. They're not in the community. We make some breaking changes. When I was on Chrome, we were very careful about making breaking changes, but we have no idea how things are being used in non-browser scenarios. No way to correct things if it's broken. Information on breaking changes takes a long time to propagate to non-browser scenarios. Latency can be 6 months to get from Chrome to a miniapp.

Christian: I will continue install discussion in Webapps. If we need a task force, I'll get back to the group. Otherwise will do it in webapps.

Hadley: If you reach decisions that the TF or WG can't make, the TAG can help with smaller pieces.

Brian: I was hoping that a first step for the TAG would be to see if we could articulate (a Note?) about how the problem breaks down. Jeffrey wanted to cleave it this way. Martin and Xiaocheng pointed out other angles. Can be get a high-level description of how the problem breaks down. That could guide wider efforts.

Hadley: 2 thoughts. 1) If you're up for it, write a draft. 2) We can do that in a lightweight way with an issue and a closing comment, through to a Note or other document. Christian, what would you find helpful?

Christian: I'll have to think about that. We'll continue and then come back.

Jeffrey: this may not be entirely up to Christian. MiniApps and that space are a distinct problem from what MiniApps are working on. I endorse Brian's suggestion to write a draft of the problem space. Anything we can do to help those groups work together is good.

Christian: I come from a WebApps direction, but Brian's angle is also important.


## Associates selection

Jeffrey: Nominated x and y. One limit per company.

Brian: Do you typically talk to a person first and feel out they're able or bring them here? It is awkward, if I talk to someone and TAG doesn't...

Jeffrey: We do it itteratively.

Brian: Same as regular TAG. Funding.

Jeffrey: Time. Time commitment for associates is less than regular.

Martin: Significantly.

Lola: I dot want to acknowledge there may be a social pressure. Although we try to make it so that you can say no.

Brian: I might throw Mozilla under the bus but they're paying for me to be here and hard for others.

Martin: I can possibly suggest z.

Jeffrey: Another thing we can do is to use the associates program to make ourselves more diverse.

Brian: ??? I could convince someone who is already spending the time that they could but just as an example.

Yves: To also help them understand how the TAG works and whether to run for election or not.

Jeffrey: Also to raise their visibility so they can win an election.

Matthew: We'd probably priotise IEs, and funding possibilities so that more people can particiapte. You mentioned time commitment. The page tells you 4h of commitment, where do we PR for it.

Jeffrey: Let's come back to that.

Brian: a, b, c.

Sarven: Limit to how many we can have?

Jeffrey: Only resources to keep an eye / support for them.

Lola: d

Yves: Remember TAG associates need to be sponsor by another TAG member. Limitation is also based on that.

Xiaocheng: Do we nominate first or let them know? Are they aware?

Lola: No, just internal consideration for us.

Xiaocheng: e. Remember talking last year but declined.

Jeffrey: They're an option.

Sarven: I see potential individuals from major orgs. We should really look into more IEs.

Jeffrey: Difficult re funding.

Lola: +1 to Sarven. Also more diversity is needed. People from different regions. We should be intentional to reach out to minoritised.

Martin: If you want more gender diversity, g, perhaps. They're doing a bunch of web platform stuff.

Jeffrey: No deadline. We can have a target. Let's narrow down one per company at least.

Lola: h. Not sure how active in W3C, but they have supported others at W3C.

Matthew: They're active in Foo.

Hadley: We're a bit far from VC. Any of you actively involved in VC? Perhaps they have suggestions.

Sarven: I'd be fully supportive of m but I doubt they'd be interested in the associates program. If they were interested in TAG, they'd run as a normal member.

Sarven: Are we looking for new skills? Any reason not to re-invite?

Hadley: Another criteria to rank, the TAG member to mentor/support is on board with that. They should have a slightly stronger say on that.

Brian: I had been here for a whole week.. honestly thinking they're all very competent.

Sarven: Comments about a-Z.

Jeffrey: I do think we should be a little bit about the individuals rather than neutral.

Brian: I'd be excited about q.

Christian: Like the limit per company to not necessarily steer things in a particular way.

Sarven: Should there be a limit to being an associate?

Hadley: No need to put more rules until we actually need to address that.

Lola: Different skills would be really helpful. Also we're supposed to leave our affiliations at the door.

Martin: IETF has a rule that one represents themselves and not their org. It is largely recognised as fiction.

Jeffrey: Am in favour of dropping the limit per company. I understand why we have it. We also have it for TAG members but I think we can manage it. It doesn't need a strict rule. If we relax that, I'd like to allow more time for thought. Propose it for next plenary. Let people think about it. Ratify then.

Brian: It does seem strange that you can wind up with two people any org that has an actual TAG member and only one if not. If no one from org X, then two from that seems fine.

Brian: Do we have an estimate for time commitment.

Jeffrey: Two hour long and another for plenary, and reviews time. Associates are not expected to do that much.

Matthew: The reason why I suggested two terms is because we were presented with dilema and because we like someone and then we'd like them continue. I don t like the idea of removin the cap on number of people. If we do increase cap, should we have a way to dismiss associates?

Jeffrey: Yes, already do.

Hadley: I'd like to keep cap on companies. Not only some companies may lean on their people... and not necessarily evil, culturally a lot of us are coming from orgs, and are subject to group think from within that org. That can provide momentum or a sense of inevitability toward what that org is expecting to happen, distorting the TAG's work.

Jeffrey: Opposed or okay with some limit?

Hadley: Concerned, but willing to talk about it.

Martin: Adding more detail on expectations would be good.

Jeffrey: I like Brian's point even with current cap probably should be up to two per company, rather than... we can also say the TAG SHOULD limit to two per company, but in exceptional cases it could override that.

Lola: Martin spoke about work expectation, one review / month or less than that, but I think it really depends on the associate and what they want from their term. Defining the floor is good... if you can help them understand their goals for the program and look for opportunities to further that.

Brian: Two pieces to this. One may spend a lot of time on this. We have to tell our peers as to what they're willing to fund.

Yves: I tihnk the limit should be kept for W3C members on the TAG operates. Members don't see a way to see the bypass. Another point: we should also notify / thanks the departing associates.

Hadley: Maybe like a certificate?

Sarven: We're talking about changing the cap because we haven't broadened our view of potentials. 3/400 members.. and so many IEs. We ought to be able to find  And if there is already 1 from an org as normal member, and adding 2 more may be too much. And that's out of total TAG participants.

Hadley: Right, 1 member + 2 associates = 3

Lola: good point. To complicate things further - I'd like to add h to the list.
