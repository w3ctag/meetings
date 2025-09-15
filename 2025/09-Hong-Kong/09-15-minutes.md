# TAG Minutes - 15 Sept 2025 - Hong Kong F2F

Present: Lola, Jeffrey, Xiaocheng, Yves, Marcos, Martin, Matthew, Sarven, Max

Scribe: Matthew

## Expectations + Hopes for the week

Lola: We're going to do the round robin exercise that we did in Paris.

Note: start person and order varying.

### How are you feeling?

* Quite tired, excited, happy to be here.
* Nervous, but we will pull through.
* Excited, looking forward to productive week.
* Tired. Travel-stressed. Nice to meet people yesterday, and at breakfast. Our work is important.
* Not tired! Not sure where this is going, so apprehensive on that front.
* Adjusting to the climate; good.
* Tired but excited to be here. Looking forward to the meet-up - great to be doing these sorts of events again. Making progress on the finding.

### What do you need from the group to have a productive and joyful time together?

* Engagement. Ideas. What do _you_ want to achieve?
* +1
* Ideas and in particular vision. We're standing at a crossroad, and I don't know where we are going.
* I'd like people to chime in with organisational ideas. If you see a session that could be done a different way, chime in. E.g. if you have ideas for how to discuss something that the group isn't already doing.
* Mindfulness. Especially if you're not the person leading the session. Bear in mind that someone is. No cross-talking. General respect for the person who's leading a session. And mindfulness of the people joining from Zoom.
* Add mindfulness for people who're not native English speakers.
* Engagement and ideas.
* Repeating an idea I've heard in multiple workshops - if you tend to speak a lot, try to hold back a bit; if you are quiet generally, please chime in.
* Actively ask people about their thoughts.

### What do you need from the chairs?

* Help figure out the feeling of the room regarding topics and emerging work that will pop out from the discussion.
* Chairs to chair (as they are)

### What are you most looking forward to?

* Publishing Findings or Notes (if we can). Not for the sake of it, but for having something ready. Plans for the future: new topics; new people to bring in, as elections and appointments coming soon. Producing things and planning ahead.
* Particularly Wednesday afternoon - web-no-papers and User Agents - this work is progressing well. Looking forward to the developer meet-up.
* Making progress on our draft Findings. Maybe even more important: thinking about the future of the web, and documenting what we come up with. We have a whole day scheduled for the impact AI is going to have. We are here for the bigger picture topics.
* Impact of AI; Technology Strategy TF - whether/how it will bring a difference.
* Moving findings forward toward publication so they can have a positive impact. Talking about what's happening next, and the developer meetup.
* Not sure about looking _forward_ to AI topic, but it's an important discussion for us to have, and the Findings. And to having a break.
* The AI stuff, new technology discussions. No papers, hopefully we can get that out. Geoloation stuff - there are some quick wins there. Revising what Findings we have on the go, in the limited time we have.

## What is a Standard?

Yves: What 'standard' means varies based on where you are. W3C has recommendations. Standards could be requirements-driven, or research-driven, have a test suite, or be more exploratory rather than being based on wide implememtation experience.

IETF RFCs (their standards) - takes a long time to get to RFC, so there are many drafts and relatively fewer standards. The process here is based almost entirely on implementation. The bar is higher. Could take 10 years of careful debugging and implementation. Email may be a standard now. HTTP is, recently.

Martin: IETF standards need to meet a very very very high bar. Lots of interoperability reports. The higher you go up the stack, there's a lot of discretionary stuff, so nobody knows how to solve for this. BGP is relatively lower-level and simple, so has an easier path to being a standard. Lots of documentation.

... WHATWG has a view that is based on implementations.

Yves: WHATWG are standards that are evolving over time, based on implementation reports, the needs of browsers changing over time. Different goal. Driven mostly around implementation and test reaults.

... So there are 3 different kinds of standards, moving at different paces, that interact with the Web platform. So as W3C TAG, how can we make things better? Better for W3C RECs, and what co-ordination to do we need to ensure standards are interoparable and evolving at compatible rates?

... E.g. if you're a W3C WG, making a standard based on on RFC, what's the right way to interact?

Marcos: There's a legal side, and a practical side. 'Standard' in the ISO side, to have an international standard, there are legal requirements for implementing it. W3C doesn't wnat to get involved in this.

Yves: In a way, we did because web services became a US @@@@@ standard. But it's not our role to decide which standards get adopted (e.g. WCAG)

Marcos: Some members view this as inherently dangerous. Even though there is an IP framework which we operate under, the W3C makes its recommendations, but there's no implication to not implement them, or wilfully violte them at times. Otherwise we'd be forced to do things we may not want to do.

Yves: Whole story around privacy here.

Marcos: Framing around why they're called Recommendations at the W3C is valuable. The ratoinale for that is important. These are recommendations, rather than standards. Some specs have standards attached to them, which may become legally enforceable if someone like ISO takes them up.

Marcos: Voluntary adoption is key in this area.

Jeffrey: https://open-stand.org/about-us/principles/

... One of the principles for web standards is that they're voluntary.

Yves: There's no possibility for W3C to force implementers to adopt recommendation to the letter, as Marcos mentioned.

Lola: What are the holes in this process? What does W3C want us to do to make it better?

Yves: To me it's more keeping in the same voluntary standards, so W3C and IETF are in the same basket. The goal is what can the TAG recommend to W3C or even to IETF or WHATWG around specifications that are developed in those 3 groups. How can those specs be developed better for the consumers of those specs.

Jeffrey: What questions do we want to answer in this session? e.g. how we make the various standards bodies work togetehr? What makes a good W3C standard?

Yves: This relates to how to make things usuable by the other bodies, need a high bar. Need a good Explainer to help others who are not in the space understand what the spec is about, rather than trying to infer it.

Jeffrey: ... so there's that question, and then: how does the TAG want to guide that? Do we need a separate group? Like the QA group spin-off again. We could have views about what makes good standards without being the arbiters.

Yves: TAG has good experience due to reviews. Sometimes IETF asks for details on certain things, also WHATWG, even TC39. We're in a position where we can talk to those different people and co-ordination. We can start something, even if we're not doing the work, TAG ist he right place to think about that.

Martin: re voluntary adoption. A number of reasons it's good. It prevents drawing sharp lines of responsibilities across SDOs. So if one SDO does duplicative work of another SDO, the test of who's turf it is doesn't become a problem, beause what succeeds in the marketplace determines what becomes the reality, rather than saying 'this is the area of W3C' for example. Re Identity work, there's duplicative work going on in different groups. Partly becuase some people don't get on. Partly because there are different perspectives. We're doing the whole capitalism thing where we have 5 different products and seeing which does well in the marketplace.

... One thing I added: if you look at the DID Methods tal Credentials work: the 'standard' as it were, is being developed as a framework with a hole in the middle. The real standards work is being done outside of W3C. These specs defined a framework, and a rough hole in it, but didn't define the things that go in the hole. Do we have a standard at this point? I still have this question about the URI: what a scheme means is undefined. The concrete schemes we tend to use on a daily basis are understood, but the new ones... why would you need some of those?

Yves: There's the question about what even is a URI? (differing defintions)

Martion: Some maintain WHATWG's version is an abomination, but WHATWG would say this is what is shipping and what people are writing code to. They're both right though IETF not quite right. There are community uses of URIs that don't intersect with WHATWG's version.

Yves: Some people want to have hard distinctions, URI, IRI, ...

... The question about holes in a framework may be more related to strategy. Highlighting things that are not properly defined. What we can do to make standardisation better.

Martin: Maybe should be asking more what we should be doing to standardise an _API_. The DID Methods hole is a fundamentally different one to the Digital Credentials hole in the framework.

Yves: IIRC there were FOs around the DID Methods work.

Martin: Indeed; how can it possibly be interoperable?

Matthew: Agree with the "hole in the framework" issue.

Marcos: What motivated this session? E.g. concrete issues.

Jeffre: One thing was we got a design review about 'should the DCs API spec have a registry in it?' - some thought everyone should define the approaches they want, and use UUIDs and search engines can find them, but I think this is foolish.

Yves: the registry is a search engine.

Martin: At what point do you determine that those processes are an essential part of the spec. You could build the alternatives into the spec. Ultimately: what does it mean to standardise once you give away that capabilty? There's an amount of responsibiltiy when you take on the work of others to fill the hole.

Marcos: Makes sense as to how we got here, but wonder if we should narrow it.

Yves: The other discussion that raised this was whether the Explainer be part of the spec at some pont - does it halp make it a better standard? The W3C process evolves all the time, e.g. with testing being included; the recent work by Dom & Francois about making sure the JS and IDL align; constraints on types. Many things done to make W3C RECs better, but can we do more?

Jeffrey: Short answer to Marcos is: a lot of questions have come across our desk about spec quality, so it's looking at if there's anything we can generalise from these. What do we think about spec quality.

Marcos: We know the tooling, and the things we can check. This is broad - Explainers, what can we check, legal stuff, pressure from external groups. Doing the DCs spec... people ask things that are not tightly specified ('why can't you have a list' when we need an algorithm with defined steps, failure modes). Defined formats falls into this.  3 kinds of standards:

1. Data formats. There's processing in web manifest you can do. 
2. Browser features. WebApps & WHATWG are very algorithmic, which is good. 
3. Network protocols.

Martin: They're processing standards, so fits their model.

Marcos: THere are pocesses in the spec that interat with the OS/platform. Network protocols.

Martin: fetch relates. Networking standards are a mix: you define the fields, and also how you expect entities to react to them.

Yves: WebTransport work at W3C and IETF.

Martin: Not enough to define just the fields, but what you have to do when you receive one. Not the same as defining an API. IETF has HTTP and Structured Headers that adopted this method. It's a good idea, but the challenge is you forclose on some implementation strategies. QUIC affected by this despite being right in the middle.

Marcos: 3 types: data formats    ; browser API/feature; network protocol.

Lola: What determines which group would be good to develop a particular standard? E.g. if you require an API? Guidance for groups: 'if you're doing a proto/networking standard, here's what you need to include'

Martin: When developing for a platform like POSIX or a programming language stdlib, insturctions like 'when you get this, you raise this error' is needed; need preciseness about algorithmic processing. In W3C specs about a format, more important to be precise about the semantics rather than the algorithm.

Yves: I've seen some W3C stuff that ran into problems with the threading model; was not forward-looking.

Marcos: We got it wrong in credential management.

Jeffrey: Everything in HTML is written as if on a single thread, but you can implement it differently as long as it behaves the same. There's a good example of this in @@@@@@ [ 'you just busy loop' ]

Martin: Fast, Comprehensible, Correct. We need Comprehensible and Correct.

Jeffrey: One guideline that migth go into what is a good web spec document.

Xiaocheng: Specs written without threading may be difficult to implement multi-threaded. You raise the parallel queue example. It's extremely difficult to parallelize in CSS, because so many things block layout, which is very bad. We need to have principles on good performance.

Jeffrey: Write the algorithm to be comprehensible, but pay attention to what the potential implementations will be, so they can be made performant.

... May be useful to move on to registry question.

Xiaocheng: Can I add a subtopic about implementations. Martin mentioned competing standards. It's a very monopolised capitalism. When we have conficts, it's up to the choices of a few implementers as to which one we adopt.

Martin: Important question: When it comes to making decisoins, the market is not a health one. Some players have a veto over other options.  ALternatives therefore have no hope of success.

Jeffrey: True: but what's the question the TAG can answer that addresses that?

Xiaocheng: We still need to be aware of different alterntives.

Jeffrey: Like 'how can the TAG enocourage more alternatives?'

Xiaocheng: From TAG's perspective, we probably want to decrease the influence of powerful implementers, and focus on the best approach for a problem.

Martin: We're substituting our judgement for that of the market - is that any better?

Xiaocheng: There is no judgment of a market.

MT (agree)

Lola: True that there's an unfair market, specifically in the W3C, a few companies make big decisions. Howvever, as TAG, we do have quite a few systems and levers we're not shy about pulling when we notice these things. Beyond that, not sure how we can influence. If we're thinking of what's best for web architecutre, it's up to spec authors to bring us suggestions. When we notice they're all from the same company, we ask them to show they covered alternatives.

Jeffrey: Not sure if we would be good at this, but one way to decrease the influence of browsers is to create new ones.

MT, X: difficult

Jeffrey: We could coordinate between the groups?

Lola: I'm contributing to Servo at the moment. Igalia is too. We're all in W3C, but what can we do to make this better?

Marcos: Having an engine is no use if nobody uses it. Need a browser. Also finding a balance with DCs work. Brave made some valuable points. They're using a modified version of Chromium. Others, like Ladybird, need users.

Lola: Brave has a user base. Vivaldi too. Not in comprison to other browsers though.

Martin: Opera has quite a few users.

Lola: How do we get them more involved?

Marcos: Complicated, and contentious, as there are browsers, and engines, and many browsers use the same engine.

Jeffrey: The debate club can't really do anything, but the W3C could.  It could fund work on Servo, for instance.

Lola: This came up at Web engines hackfest earlier this year. Didn't see W3C participation.

Jeffrey: It's not doing that yet, but it could. We could work on a more solid plan and then convince the W3C to do it.

Marcos: What budget would this have?

Jeffrey: W3C would have to raise more money. But if it has a use for it, that's something to go to the members on. 'We'd like to coordinate you to produce some output' Personally I don't think we can be effective doing this.

... What should we discuss for the rest of the session? I think we can make progress on when Registires are the right thing to do, and make progress on documenting that decision.




Questions to answer this session:
* How can we help SDOs work together?
* What makes a good W3C standard? E.g. what the QAWG published in 2005
* What group should guide standards quality? TAG? new QAWG? Something else?
* How do registries fit in? E.g. DIDs vs DID Methods. Digital Credental protocol field. Etc.
* How can the TAG decrease the power of centralized implementers?
* What is Implementation Experience?


### When and how are registries appropriate?

Sarven joined the call.

Matthew: I remember we have had similar conversations before, if you have choice of formats, everyone has to implement everything, so it can be a bad idea.   This can relate to the framework hole issue.  Not sure what we could or should do.
...Never got around to documenting the polyglot format.

Martin: I think this is a scenario where we're talking about options in specs, anticipating that we don't know all the situations that may need to be addressed. So we build in an optionality mechanism, and add some way to select options, including negotiation. When talking about the spectrum of choices you may present for giving people choice, there's 'parameters in the spec' to 'I don't know what may fit into this hole in the future' so providing an extension mechanism, or as in the DCs work, which is s still being worked through (registry)

Jeffrey: ["Have one joint and keep it oiled"](https://www.imperialviolet.org/2016/05/16/agility.html)

Marcos: Issues around JS, quality, defence of the W3C's mission, all these things come up as criterea for inclusion in the registry. The WG accepted the criteria. There is good intent there. Could talk about registries in general - what are their roles, and how they are governed by the W3C's mission.

Martin: Good 'blog post, was based on TLS.

Yves: Re extension points, issues around referecing, etc.

Martin: Issue with URI schemes, you have to go back to first princpiles. All the infrastructure needed, rather than just having specific points for optionality/extension. There are specific pathologies in this domain that don't apply to others.

Presenting: https://www.w3.org/TR/digital-credentials/#protocol-registry

Marcos: With DCs API, the API itself tries to be agnostic of the protocols, which define formats, for which we have a registry. So we had to come up with a set of criterea for inclusion. Motivations included: practicality of how we work with other orgs; how these things can go awry; knowing that a lot of SDOs, like OpenID, they don't work within web browsers, so don't have a full understanding of how UAs work. Given that poast experience, we made it clear that: (1) there needs to be a formal liaison arrangement with W3C to cover IPR/legal issues; (2) it must be defined in a freely-available spec; (3) have a stable URL.

... Practicallity of implementing: other SDOs weren't familiar with WebIDL or JSON. Needed to explain why these are important to the development of the spec - and the need to develop validation rules. OpenID had URLs and parsers a lot. Need to understand these are vectors for attack. Weren't considering e.g. what happens when you have a fragment identifier. Assumption that these are opaque and will be handed over as strings to wallets etc. Can let UA check this.

... Referred these defintions to HR groups such as privacy.

... (4) implementation commitment: this one was a bit loose.

Martin: Not a great one @@@@@@@

Marcos: (5) agreed by WG; (6) response must be encrypted, in particular any response containing PII. We also defined a change process.

... Lots of this is trying to improve cross-organization understanding on how things on the web work.

Martin: All of those are problematic; some are actively harmful.

Jeffrey: would it help to list some other registry strategies?

Martin: Experience with TLS, has a registry for cipher suites. Narrow defintion. Everyone understands the limits of that. With one exception, most fit that form, e.g. 'I want to use AES 128 with ...'

... We found poeople defining code points without using the registry, because going to the registry was difficult. They had to ship code. Or they had legal reasons to use the cipher suite they used (e.g. mandated to be used); happens in different countries. So code points were getting used, and not published anywhere. We had at least one occasion where 3 TLS extensions used the same code points (16-bit integers).

Jeffrey: We've had the problem in MIME types also.

Martin: The collisions were more of a problem, so we thought about controlling what goes into the registry. Other parts of IETF don't have the same problems, so are not doing this, but TLS decided that registries had to be more permissive so we could get away from the idea that you can place stipulations around access, because it doesn't work. This is especially true for string-based registries. This works better - unless you're defining a standard, whcih we'll get to.

Lola: if we acknowledge that part of the problem is the bar is too high, and now different countries etc have different ciphers, how has TLS addressed this?

Martin: With TLS, as long as you have something in common, it'll work. Whether there is an overlap is generally something the market resolves. TLS mandates that you implement at least one cipher, which means everyone has a fallback. Problem is with 1.2 that the fallback is not something you would want to use.

Lola: Is there an incentive to implemeneters to have a fallback? What about the fact the mandated fallback isn't usable?

Martin: Over time, new de facto fallbacks have come about, and it works out.

Jeffrey: 2 things we need to write down: (1) do we have a registry that is easy to put things in, so that everyone has a definition and code points don't colldie and (2) do you need a high bar so that only things that meet those high requirements go in.

... E.g. DID Methods and VCs define extension points. Some specs like these define registires and then put nothing in them. We should endorse a principle that there must be at least one.

Martin: For WebRTC we decided too early. (64-bit uncompressed audio)

Jeffrey: Registires: Permissions (I think it's been successful in that people have provided a lot of strings for them, but there's no registry yet); URL schemes (successful, but registry has not been).

Martin: Dave Taylor at Microsoft went through an exercise of getting them together and registering them once, but nobody registers them.

Jeffrey: Not aware of collision.

Martin: I think there has been one.

Yves: The problem is that these should've been based on MIME type and not URL scheme.

Jeffrey: Which brings the quality question to mind: if people tried to register schemes we culd find these. Another one is MIME types.

Martin: I suspect again that the compliance rate is much lower, so the registry is only a subset.

Jeffrey: Anything else to add?

Martin: The DCs one is an intersting one. The rules reflects the political reality of the WG when they were written, but the don't reflect what you'd have if you wanted to ensure interop. I would ask: what is the shape of the hole? And what is required to fill that hole directly? So there's a 'create' or 'isssue' and the retrieval operation. The definition of what activates each, and the nature of the response, isn't specified. I would expect these things to be written down, not whether the Privacy group has looked at it. 'Have some people looked at it' isn't a standard.

Marcos: There are HR requirements.

Martin: Which should be checked for whether they've been met - not whether it's been looked at. Currently you don't have a 'how this meets this hole'. My expectation is that if you manage to register something, that'll lead to refining the criteara.

... So we have registries for things like QUIC parameters or frame types (for which you don't need a registry, because you can't use frame types without negotiating them, so you can use the transprot parameter registry as a proxy).

Jeffrey: I divided DCs registry reqs: 'is this an adequate standard for the code point' and 'is this specification a good idea (does it meet W3C goodness requirements, as wella s just promoting interoperability)'. We shouldn't just have 'I claimed this code point but won't tell you what it means'

Sarven: There may be more than one registry for URIs. Who gets to make the call/have governance over the web community. Mostly done through IETF/IANA, W3C and GS1 had one. The point is: if you have multiple registries operating, and different specs overalapping, registring at different places, that sort of fragementation may not be what people ware looking for. Parallel in my mind: URI spec - original at IETF, WHATWG has one that is reflected in the browser. Not overall great for the web community, but solving these problems. Some aspect of dagner.

Jeffrey: Not aware of parallel URI schemes.

Martin: There's one in the HTTP spec about what web apps can answer.

Jeffrey: Forking a spec is a serious escalation, and should only happen in extreme circumstances. Though it's good there is that escape valve.

... Question: do you do a registry of code points/defined strings _or_ just say put a URI in this field; doesn't need central agreement. Need to write down the cases where it makes sense. W3C has a community that over-uses URIs for that purpose.

Martin: When you define JSON-LD and the schema link points to something, that's a great example of the open flexibiltiy that system provides without coordination; that's great. In other contexts, the application you're interested in has to behavie within a certain envelope. For something like DCs, it has to behave in a particular way, it has to have the 'get' and 'create' and follow a particular structure. So then you need to know it is going to behave a certain way. At this point, we are not building a standard?

Jeffrey: How to write this down? Start a doc about how to write standards? Re-start the QA work? Design Principles?

Lola: Design Principles.

Martin: A statement in the form of what TAG expects people to do when defining a registry. When you have a registry in a document, understand what it is that you're doing, there are multiple reaosns you may be doing this. What is needed in each case (of which I don't think there are more than 2).

Jeffrey: Makes sense to start, especially with registries, in Design Principles, as you're doing that sort of design. If we have too much we can split it into a separate document.

Martin: +1. Though there are 2 subsetions to it. I think we should duck the issue about defining new URI schemes.

Jeffrey: I'll file an issue. In fact, Wendy filed the issue!

Martin: https://github.com/w3ctag/design-principles/issues/583

... You put a registry in when you need to make a choice, but don't know what fits there at the time. So you're punting on a choice, which can be a cop-out, but it may be that you know _one_ way to do it, and then you define that, and it becomes the template. That is healthy, but I think what DID has is not, because there are thousands, and they don't share things in common. Would've been better as a MIME type.

Matthew: ADAPT has a registry that acts as a coordination point with Bliss Symbolics. It's not "anyone can put anything in." We need the registry because when you are writing a web page, you want the author to pick the concept. The concepts are keyed by unicode codepoints. Some can be 1-N codepoints to create a concept. Only a subset of Bliss is going into Unicode, so to make all the concepts, you need sequences that are "spelled correctly". 

Jeffrey: This is appropriate. Unicode is a registry, you're doing a dictionary. You can't make it open-access because the space is dense...

Matthew: You can make up any English word by inventing sequences of code points. Bliss is a language, and new "words" could come into the registry by being invented. Makes sense for people to invent, and W3C will reflect the Bliss organization's dictionary writing.




## Technology Strategy

Scribe: Martin

https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/09-08-minutes.md#plenary-session---2025-09-11 and https://www.w3.org/2025/06/w3c-2025-roadmap-to-develop-a-strategy/index.html#5-5-technology-strategy


Jeffrey: THe W3C is trying to set a technology strategy.  Looking for 2 volunteers.  Wanted to hold a session here for us as a group to choose who to send to the task force and then to open discussion in this group on the questions that the group might address.  I suggest we do names at the end.
... Let's start by brainstorming questions that we want to address.  Doing this as a round.

Matthew: Was on the call.  Should we summarize the output?

Jeffrey: We have got this document that has text:

Ensuring that we are able to navigate emerging technology.  Looking for what to engage with and what to ignore.  And how to effect change.

https://www.w3.org/2025/06/w3c-2025-roadmap-to-develop-a-strategy/index.html#5-5-technology-strategy

Marcos: Does the W3C even have expertise in this area?  Should we even do a tech strategy?  What part would we be evaluating?  Companies do this to plot paths for their work, requires foresight and research.  Not a lot of innovation in standards.  if we are looking at this from a societal impact, we need sociologists and those who are critical of the technology.  Not in the W3C.

Lola: Even in this group, there isn't a clear idea on what a technology strategy is.  We should have an idea of what we expect in developing one.  How is the TAG defining technology strategy?  What are our expectations from one?

Jeffrey: Should the W3C Strategy be bottom up?  defined by members.  Or top-down?  decided by a body like the TAG.  Or some mix?

Xiaocheng: WHat are we going to do with the output?  How does that affect working groups?

Matthew: Looking at discussion with PLH, I asked on the call about reacting to change.  THere is the CG process improvements.  I was wondering if W3C expectations are about being more outward facing and who to collaborate with.  I also got the impression it is about what technologies to focus on.  I really liked Martin's suggestion to make the W3C a really good place to do standards.  Struggling to come up with questions other than what Lola said.

Sarven: Touching on top-down vs bottom-up: identifying gaps and biases and dealing with them.  Whoever is providing some guidance will come to that table with views and their experience.  Worried about how that will influence the direction vs. community perspective (CGs or members).

... Short-term and long-term guidance.  One is seeing active trends and deciding about how to act.  Immediate, like AI.  The longer term consideration is more like 30 years out.  If that is important then how does the group balance those time horizons.  Foundational work like HTTP, HTML, URIs are understood to be what drives the web.  Will W3C be picking from technology that will become such key components and evolve the web?  Might be different than looking at AI.

Lola: Xiaocheng mentioned output.  Who is the audience of the work this group produces?

Matthew: Would this be a group in which you would discuss a plurality of user agents and engines?  Do we want to do something about the more novel user agents?  like wallets or AI



### What does the TAG think a technology strategy is? 

* Audience
* Short-term vs long-term

Martin: I hear very clearly that this was 3 years, not 30.
...
Martin: So in the short term, we can only focus on the components that are ahead of us. Some might accidentally be foundational. To some extent, the web stumbled on foundational things like URIs by accident. Don't want to go in expecting to find something with that lifespan.

Marcos: A more worthwhile exercise might be to look hollistically at what things need more resources vs. not.  Make a case for investing in areas that are underserved.

Jeffrey: A tech strategy is a list of stuff and priorities with each.

Lola: But we don't have priority?  Is that the strategy?

Jeffrey: Is strategy the priorities or the principles you use to determine the priorities

Marcos: We might have a good platform that has some potential unrealized in some areas.  Maybe we could add more resources to AI.  Only to use that as an AI.  Determine what we have, what is the state of things.

Jeffrey: What would the output look like.  It would be a survey of all the work the consortium is doing.  A big list.

Marcos: Automotive was there a while ago.  Maybe that might be deprioritized.  Identify new trends.

Martin: THe W3C is not a corporation. Doesn't have resources to marshal. Membership dedicates resources based on each member's determination of importance.

Marcos: But W3C can influence priorities.

Martin: Corporation would look at resources, threats, etc. and try to align them. Slightly different here, since influence is indirect.

Sarven: What the W3C is seeking to do is differentiate itself against other SDOs.  And hoping that one of these groups will help to influence some of that to be a key driver in standards.  THat has a lot to do with purpose.  GLobal credentials condeference in Geneva, you can really see in that room where there is a whole lot of things happening around wallets and credentials.  In some ways these are competing and collaborating.  W3C is setting out principles and visions, some of that work is not being taken seriously (even by some states/govs).  They might use some W3C work, but not always.  The task for needs to find a way to navigate that.  Identify how the W3C can take a role.  Big question is not about specific technology, but how the W3C maintains relevance.

Jeffrey: does that imply that a strategy is not a list of priorities?

Sarven: Maybe whether this is short or long term matters.

Jeffrey: what is the shape of the answer?

Sarven: Context.

Jeffrey: A description of the environment we are operating within.

Xiaocheng: Comparing to corporate strategy planning.  Planning should have how do we evaluate how an investment in something is successful or not.  THere is a goal.  For a corp, the goal is to make money.  For W3C, it might be keeping relevance.  A company can switch business focus, but W3C dies if the web is no longer relevant.

Lola: Sarven said that strategy defines context. Agree with that. On Xiaocheng, disagree because the W3C moves slowly.  I don't know what could be measured in three years considering how slowly things move.

(confusion)

... At the end of three years, what would we measure?

Marcos: So.... what do you think you do here?

Lola: How I interpret things at 3 years.  THe time is maybe too short a time to measure.  If there is a different measure, what would that be?

Lola: A potential audience is governments.  It might be helpful to tap into what their strategies are in order to help define our technical strategy.  For example, HMgov has priority technologies that it lists.  If we have an opportunity to inform that work or collaborate in those areas, that's positive.  Advances goals of working closer with government and other SDOs.

Jeffrey: Note about policy engagement task force.

Matthew: Focus on what it is.  I like the priorities and the comments made by Sarven and Xiaocheng.  It says in PLH's report, how we identify what to pursue or not.  There are two deliverables: one is the technology choices and the other is measuring success.  A lot of stuff is changing today and we need to figure out how we understand that and make the change positive. A lot of people see the user agent as a threat.  A vector of attack rather than a trusted part of the system.  Might need to address that.

Martin: Strategy needs to list risks and has plans to mitigate those risks.  Matthew identified on such risk.

Xiaocheng: Measurement of success.  A strategy is successful doesn't mean that we have produced a REC.  It means that, for example, significant portion of our audience agrees with direction.  We don't command people we influence.

Yves: Yes, because of voluntary adoption.

Sarven: To elaborate on context.  Points are touching on that, like risk.  Influence is another thing mentioned.  Accepting and being realistic about the W3C situation.  To determine whether a tech is worthy of investment, knowing that others are likely doing similar things.  Strategy needs to draw a line sometimes and say "too late for this" or decide to pursue something.  Need to assess whether we get buy in from the broader community.

Matthew: Some things are small: cross-site data, mimization of heuristics, those might be too small for a tech strategy.  Large scale quality of life changes might be something that could be useful.

Sarven: Attention of dev community and making sure they are interested in the developments at W3C, and retaining. They play an important rule in shopping around and finding cool tech they can implement for their needs, or even convincing / making the argument to their orgs in which direction to move to.

Lola: PLH mentioned a developer survey as well as other surveys.

Jeffrey: We didn't mention which inputs go into this effort.

Matthew: We've mentioned other strategy arms.  Process, policy, etc...  (Five of them)  THe other one is about the W3C processes need constantly need improvement to ensure that we don't exclude parts of the community.

Rough TAG answer:
* 3-year scope, per PLH
* Audiences:
  * Governments
  * Other SDOs (this is where we intend to operate)
  * W3C Membership
  * Web Developer community
  * Spec Developer community
  * ...
* A Technology Strategy is a list of potential areas for standardization investment, with priorities for each.
  * "Areas" could be cross-cutting like "drive down cross-site data".
* A Technology Strategy defines a goal for the strategy. E.g. "W3C will stay relevant" or "Web will evolve in good directions"
* A Technology Strategy defines a way to measure the strategy's success, not necessarily at a particular point in time. E.g. "significant portion of audience agrees with direction"
* A Technology Strategy lists risks to achieving the goal, with mitigation plans.
* A Technology Strategy is realistic about the W3C's ability to effect change.


### Should the W3C Strategy be bottom up?  Or decided by a top-down body like the TAG? Or some mix?

Jeffrey: My perspective: I think we should start by describing what the membership is already doing.  Describe the emergent, bottom-up strategy and then notice and describe any problems with what has emerged.

Martin: Like that.  They might find there is not a lot wrong with that, so no need to develop a top-down.

Sarven: WHether is top-down or whatever, the bias there is that people are interested in developing certain tech.  Look at what people have already bought into.  We need to look at who we havent' been able to attract and the gap there.  Look at reduction in membership.  Other governments taking other technologies.  Need a more hollistic assessment than what the membership or CGS are doing.  Need to do both.

Jeffrey: Good point.  On the other hand, a thing that people outside the W3C do is screw threads.  Maybe this points to something else, which is decide what is conceptually in the W3c scope.  Look for what things are in that scope, but are happening else where.

Yves: We are already as TAG doing some top-down, by producing EWP, privacy principles, design principles.  Defining characteristics.  We probably need both looking at what membership is doing, but giving long-term direction.  Might miss things if you only focus on what people are working on.

Xiaocheng: This will be dominantly bottom-up.  We don't command resources.  I like the idea that the TF might set up a venue for others to discuss what will be the important areas.  Eventually the output will be consensus of the TF.  If there is a top-down aspect, the TF might be acting like a chair.

Yves: There's an exploration working group looking at new tech.

Max: Regarding top-down or bottom-up.  I don't think that W3C has a top-down system.  Most new proposals are in WGs and CGs and incubation.  Those seek to build consensus.  That is all bottom-up.  Bottom up might be more fitting with the system we have.

Matthew: really like recent efforts on the process side to help us figure out when something is starting to attract interest.  That is really good. Re-reading the description of strategy, do a similar thing but to look outwards instead.  To then have some way to decide whether this is something that might need our efforts.  We haven't talked about that.  Maybe that's the work of the TF.  Model this on recent process work in W3C?  How far outside should we be looking for things?

Sarven: I mentioned something in the plenary.  A mix is the right approach.  To assess from a broader perspective.  Mentioned a council for FOs.  Similar de-biasing needed.  The danger of a small task force is that there is an increase in bias.  And there is also a time issue.  Whether the small group will be able to get the work done.

Jeffrey: The TF is chartered to come up with guidance on how to decide (positive or negative).  Our answer might be that we don't want to develop a rubric for assessing new things.  That might be a process, rather than a set of guidelines.  That might answer the concern.  Instead o the TF defining that, it might be to define a process so that others can make decisions at the time.

Matthew: We asked how do things get into the strategy repo right now? The Team does that and we might want to ask them how they get there.



General sense:
* Describe/summarize what is happening in the W3C.
* Describe/summarize what is happening outside the W3C ... in areas where the W3C might operate.
* Point out problems.
* Concern about the size of the group and the time scale.  Might not be possible to develop a set of guiding principles, but might be able to define processes instead.

### Task force composition

* Lola
* Jeffrey
* Xiaocheng (depending on time)
* Sarven
* (Dan Appelquist from PLH's previous conversation)
* Hadley (remove if the list is too long)
* Matthew (remove if the list is too long)
* Jory Burson (VP of standards at Linux Foundation)
* Nick Doty or someone he suggests from the civil society area
* Someone from the IETF side (Talk to Jay Daley)

### Questions for the task force to consider

We didn't discuss these at any length, but the task force might

* Should the W3C develop a strategy at all?
* How does a Technology Strategy affect WGs?
* Identifying gaps and biases of the Task Force?
* Does it cover "How to encourage more browser engines?"
* What inputs should the task force take?




