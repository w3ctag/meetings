`# TAG Minutes - Thur, 5 Mar 2026 - London F2F

Present: Yu Sen, Xiaocheng, Jeffrey, Matthew, Brian, Christian, Martin, Sarven, Yves, Marcos, Hadley, Lola, Heather

Scribe: Sarven

## Intros part 2

TAG should be
* a connector of ideas and efforts
* broadly aware - beyond the browser... what even is a browser
* Thinking about what should a good web look like?
* ensuring that the web moves forward and remains a place for everyone. Maybe we should pay more attention to the priority of constituencies
* helpful in awareness raising, getting people from very different backgrounds talking from the same place of reference. Not sure it is our place to make the connections, but it's worth applying the breadth of connections we have towards it.  There are a lot of ways people want to move the platform forward, it's good that we've been able to experiment, but we need to be very careful also to not bake answers in too early.
* A neutral voice of reason, we are able to speak as individuals here.
* an orchestrator, to help lead the changes and keep the tempo
* relevant.  I am pleased that we started the meet the tag events again, I think it helps us connect
* advocates and leaders for a vision of what the web should be
* build connections and build concensus about how to build the web and maybe more than the web
* thinking about things with a longer time horizon than most people
* aware that we are trying to build a socially aware and meaningful web.
* trying to hang on to what the web should be in the face of many real world pressures
* A balance of leadership and practicality, looking for middle ground


What do we need?
* No side conversations
* Clear communication of expectations/targets +1
* Good scribing, to help non-native speakers catch up +1
* Tell me if I'm not doing the right thing.
* Understanding of neurodiversity
* Patience with misunderstandings
* Appreciation of timezone differences (for example, it's hard to scribe at 2am)
* Tell me when I assume everyone has my advantages
* Pateince with verbal communication


What do we need from our chairs?
* Make sure that mentoring happens. (We resolved to start by encouraging questions to any of us, and if we want to create named mentors in due course, we can revisit the topic.)
*




## AI

Heather: First I looked at what conversations happened so far. One was Web & AI at TPAC 2025. And the AI & the Web - understanding and managing the impact of machine learning models on the web.

Heather: WebML, WebGPU, WebML, ... but don't touch much on what happens outside of W3C.

Heather: IETF has some interesting work that's relevant to the Web. AI Preferences (aipref), Web Bot Auth (webbotauth).

Hadley: is webbotauth so that bots need to auth befor ethey can scrape?

Martin: No. It is so that they can get better treatment. Currently bots identify thsemvesl with teh user-agent string but that's not verified.

Hadley: So, auth in the literal sense and not as logging in.

Martin: Getting spicier.

Heather: This is a hard topic everywhere.

Heather: Do the existing web principles need to be adapted to AI or does AI need to adapt to existing web principles? Ethical Principles for Web Machine Learning, Web User Agents. Also wondering about open source software, and LLM efforts. I've seen the phrase "agentic web" and whether that's good for the web.

Hadley: We could define it. I'm not sure I'm advocating that, but it's the sort of thing the TAG could do.

Brian: I feel like it'd be like defining web3.

Matthew: How do you know what's a bot?

Jeffrey: Cloudflare and other DOS protection systems are working on it already (effectively finger printing), and the argument for WebAuthBot is that the bots would be able to say to them "I am really this bot and maybe you will let me through because you like me?".

Matthew: It'd be great if we can get to a place where you have to authenticate if you're a bot. But how do you know.

Heather: Part of the problem is why are you asking? What's the purpose of making that determination. If to control behaviour, is it worth for the entities to actually allow it? One side may want to know but the other may ask why do we need to tell you.

Hadley: For principles, I think we put agents or bots into priority of constituncies. If we don't do it now, we might have to do it retroactively. If we can bottom the discussion to consensus that'd help with discussions and community.

Jeffrey: Disagree. we need to ask why the bot is doing what it is doing. If embedded in the browser and asking the user. If a search engine asking, then that's not just a bot. PoC is about kind of thing driving the agent. I think that's the kind of thing what the "agentic web" is. when I use the term, the users asking the computer to do a bunch of actions, rather than clicking actions. That leads to a bunch of questions. We need to make sure when someone's computer to do a bunch of actions at once. Or understanding the page. To see whether that's actually helpful.

Hadley: So we could do that work, break those things down, and then to see whether PoC needs updating? That makes sense. You've convinced me.

Martin: Jeffrey is right. We should not treat all these tools as actors. The way I've been thinking about distinguishing between bot and human, for a long time websites sort of had no firm understanding of what it is to serve a human or bounds on that. Bots slipped behind on all that. As a result, they can make 100s of requests / second. A shift a much more towards for every visitor coming and if you want to serve humans there are bounds to what they can do. There are also ways to just serve bots. A world there are humans and similar cost to humans, and that necessarily includes agentic representation for humans. If you don't understand the diff between crawling and scraping... Google operates on crawling and tries to be a good citizen. Definition being following links. Scrapers take stuff. Some of the use cases is where they build profiles on people.

Ehsan: My comment maybe more counter or philosophical. I can now see shift towards welcoming bots. It might be a good idea to discuss what is a "good bot" or "bad bot". The capabilities has changed a lot. There were protections against them.

Marcos: To Ehsan's thing, when I'm using my bot it is good but others may be "bad". Re PoC, what's interesting there is that we have a responsibility within W3C there are sources of truth on what's being served. If I'm writing a spec, I can ask it to do quality assurance of type of thing. The specs need to be rock solid for humans and the bots.

Jeffrey: Ehsan was talking about what is a good bot. It is one that serves the goals of whoever is making that determination. User might think a good one gets what it wants from the webpage and the website thinks what it gets from the users. We had tension. Reader mode is not something a website might exist. I think we need to look at it from a commons sense. Is there an action undermining the health of the commons. The users need to be able to experience websites, and should have a way to experience the way website wants. There is a continual conversation. Maybe our job is to facilitate that discussion. The other thought re websites, making changes to support bots. It's similarly to the accessibility question. Humans want to interact with webpages. Webpages need to be supported to help these different types. Sometimes it is impossible.

Xiaocheng: What does the Priority of Constituencies mean in this context?

Jeffrey: It comes from HTML5 design principles but we adopted.

Martin: Different people have a stake. There are way more users than authors, way more authors than spec editors, etc.

Hadley: Often used to settle disagreements. If there are multiple ways to achieve a thing, the PoC may help.

Xiaocheng: I disagree with Jeffrey on we need to ask what the bot is doing. It reminds me of the UA string where every browser claims they are Mozilla. That's the same reason why it is not good to ask what is the bot is doing. They can disguise. They find disguising as a shortcut.

Jeffrey: I don't mean ask the bot what it is doing, we think about what the bot is and doing. We shouldn't expect bots what the bot is doing.

Hadley: We should effectively ask ourselves what the bot is doing before the priorities and carrying out the conversation.

Sarven: I'm on the fence re the questions/actions. I worry about what (philosophical) assumptions we are building on or taking for granted. Acknowledging, and are we trying to take an authoritative stance on what is sentience. Web architecture and infrastructure (socially and technically behind).

… Build for humans first, then for machines. Infrastructure is not currently able to handle it. Network is not advanced enough, authentication mechanisms, data models. Whether they interpret human language, etc. There is a lot of assumptions here. If we pick any of them, we can answer the question very easily. If the TAG is in a position to adress them in a fair way (?)

… Notion of self-describing web/documents. They get a sense of a full understanding of what a human has intended for a URI. The architecture of the web talks about the ownership of the URI, and that the owner of the URI gives meaning to it. The self-describing web says that the resource explains whatever you need to know. Even there, it serves both humans and machines. If we agree that the infrastructure is not equipped well enough (HTTP, URI, …) is not good enough for machines, we should have a look at how machines communicate with the infrastructure that we have. I think the current infrastructure isn't good enough, and this is why we are behind on how the machines can navigate the web.

Heather: If a bot or agent acting on behalf of doesn't make it the person. There is a lot of work in the identity space for that (onBehalfOf) but we havne't come to a conclusion on that. In response to making value judgements about value, I'm not comfortable, unless generalised. I want to think about that.

Hadley: One thing we can do is to amend HTTP so that a bot can say "I need an answer now" vs. "in the 10 minutes, it's not urgent" or whatever. That not only lets bots who are behaving well communicate that, it also lets servers manage their load and do things like treat all bots they don't like or who aren't authenticated as an "it's not urgent".

Martin: HTTP API WG working on something like this. It creates patterns on "ask later". You can respond with a 202 and that becomes an off. Example is Acme: "I'd like a certificate", "ok, come ask later, because it takes some time to do that".

Jeffrey: Sarven talked about self-describing web, and vision of semantic web has been that. I think SW failed. I think people were designing metadata for systems that didn't exist. Now we do have the meaning of documents, so maybe it is the time to start, and people have started with agentic web. When there was no implementation to use the data. Heather talked about value judgements on good/bad. I think you're right that we shouldn't make value judgements, and we need a societal discussion on. Someting not sustainable is bad. We need to figure out what behaviours are not sustainable. I don't know how to structure that but I think it needs to be. Community being everyone using the web. I don't know how to structure that. We make societies and decide that when you walk around do certain things, we say it is not acceptable, and we need same kind of judgements for the web.

Sarven: Don't want to go on a tangent or make strong statements about the Semantic Web failing or succeeding. But we're already swimming in the Semantic Web.  Hard to draw a line and say "this is not the semantic web" or "this is ...". There are many things deployed on the web, including schema.org, that's there. There are efforts in MCP work that smell like reinventing Semantic Web ideas. We know LLMs and natural language processing have made great advancements. But it's top-down, and there's room for bottom up, where authors and creators describe what they mean. As opposed to a third party interpreting. Communication goes both ways. One person says something, other interprets. It's a dance. Part of the Semantic Web isn't just grey metadata for machines only. There's work at the W3C that tries to capture what's intended for humans in a way that's meaningful also for machines. If anything, these things help machines get a better sense of the existing content, beyond a blob of text. Ways of connecting human knowledge within the person's mind, as well as what has been said by others across the web or in the past. There are ways to structure the semantics; has been available for decades. Helps the machine get a better sense. There's a limit to natural language processing, so if machines can encode structure, it helps.

Hadley: Work at the W3C trying to capture what's meaningful for machines... can you give examples?

Sarven: RDF formats. Don't want to say RDF is the solution, but there's an understanding, also at the WHATWG, to make it more meaningful for the machine. RDF and RDFa encode a differently layer of knowledge. Offshoots like JSON-LD and microformats, but there's a similar sense of making the content meaningful for both.

Brian: We have a tendency to think about what the world we have and want the ways ignore practical bits even when we got to where cellphones having browsers, people making links out of telephone numbres, and most of the world was not on telephone numbres, and my mom would click the link... and also if you pay or have mic or speakers.. which we didn't, and so built something, and trying to know what it'd be useful for and without knowing. What OS did was detecting what looks like a phone number and making a link and so you can dial. It is not detectable it is a link, from the UA you can't but it is presented. No one is doing this anymore but if you're writing your thing on a terminal and no UI at all, and you can type it. Don't need markup but no big deal, send an email. It is just text. That is the most content authored. Semantics is more difficult. We have to think abotu that in the PoC, people who author the content, we have to understand offering something simple, and designing for specific assumptions.

Lola: Do we know of the major AI vendors as participants at W3C?

Google, Microsoft.

Lola: Even if they're and (un)forunately they're not the major AI vendors when people think of AI. There are x,y,z. And if they're not participating in web standards and so can't expect they'd want to.

Jeffrey: There is engagement from Google Agentic AI folks talking to MCP. Spread the things we think should happen differently. It does sound like x,y,z want to do the right thing. MCP and MCP-UI are standardized at AAIF (Linux Foundation). Although you could also be right.

Hadley: Some of have huge number of users because of search results.

Jeffrey: re agentic authoring, people are writing pages in text and if someone is going to experience tha tthrough AI or tel detection, then authoring system ought to tell them how it'd be interpret. There could be assistance on interpretation, by adding (meta)data. For example, if this translated to Chinese, maybe you should another word.

Marcos: Apple Intelligence (AI). On a serious note, there is a tonne of AI going on in mobile devices. We can't just think that LLMs are it. Yes, LLM is cool/useful but just one small part of large part of capabilities and features of AI.

Heather: Observing that some of the more visible AI companies have said they want to do the right thing and they create a new stanards organisation.

Matthew: I like the idea of "light semantic web" to pave the way. I'm skeptical about someone checking before going out. If navigation is where it has helped, there are benefits that people got. I wonder if your initial push is for SEO, markups. The navigation being probably being the time sink. Navigation in/outside of pages. We're working on discoverable navigations, and also machines will benefit. That leads us to the concern - we should make sure people are talking to each other. One other cool use of AIs is, autoCHEMplete looks at legacy chemical diagrams, the human guides it to hone in on what it is. When you hone in, it is marked up semantically. so you can produce braille, haptic versions, etc. of this diagram.

Hadley: So, what do we do about all this.

Heather: Concretely, we should dive into that existing issue on Web User Agents.

Matthew: Is this the sort of thing that we spin up a TF.

Lola: Not sure if we need a TF just yet. If we want to stay in the loop, we should connect with Dominique.

Jeffrey: Yes, and Web & AI IG we should coordinate with.

Hadley: Yes, and if we write something, that's the time for a TF to see the work through. What do we want to say and to whom?

Lola: If we want to write something we should read x (link in the slide).

Jeffrey: re to design someting that should be accessible and it should be in the design principles.

Hadley: We could say effectively who are using the word "agentic web" it is more complicated than you're using it.

Marcos: Given that "agentic web" has "web" in it, there is the web as we know it component there.

Matthew: We can provide leadership on how things are, so this is like a Finding. Ehsan and I have some work on this.

Hadley: deadlines / goals / targets?

Matthew: In the next couple of weeks?

Hadley: 2026-03-23. If we can get TAG consensus we can get it out at the end of the month.

Matthew: We should make sure that we are not stepping on other people's toes. We can seek others input.


## OSS, OSS Communities, and Web Specifications

Heather: Does the TAG think W3C should be more attractive to Open Source SoftwarE? Then how do we see this interacting with our work?

Lola: Yes to both. There are quite a number of examples .The Soverign Tech Fund also doing a survey on how to support maintainers in standards. I don't know if W3C has contacts htere. If they don't, there are people that have contacts. It'd be good to liase with them. In terms of ideas/projects, baseline technically owned by private companies but work happens at W3C. But not W3C thing. I'm working on assistive technologies. There are security things.

Heather: Why didn't MCP come here? MCP doesn't belong in W3C but might belong in IETF.

Brian: Also like HTML eventually ending up at WHATWG. Or JS ending up at ECMA. There's been evolution in looking at practical aspects on what needs to be achieved, what's good about standards orgs or not. Lightweight things to startup and foundations.

Brian: At TPAC 2019? we led a session on breakout days, several people from W3C. We talked about polyfills, they get linked from documents, and no longer maintained or die out and how do we know they have license policies. We want to make sure they are covered properly. There are some sense on they should be maintained.

Jeffrey: MCP didn't even try or consider the standards bodies, as opposed to deciding that it wasn't a good fit. One of the things they got from Linux Foundation, they agreed with their existent governance model. It is not going terribly but that is not a standards based model. We would insist that they are. There is also WebRTC only kind of a standard because it has one open source implementation that everyone uses. I think the W3C should write down that it is okay.

Sarven: Concretely, one way of attracting OSS communities and developments is by incorporating to the charters to require open source implementations and test suites, and that works toward demonstrating adequate implementation experience in the W3C Process. Speaks to an assurace that OSS work is welcome, and what makes a verifiable impelmentation — something is verifiable if you can see its source. The web is built on view-source. One way to demonstrate sometime is interoperable is an open source implementation.

Hadley: Am I the only one thinking of https://xkcd.com/2347/ ?

Heather: I wrote a blog about MCP (https://sphericalcowconsulting.com/2025/06/17/the-mcp-bandwagon/) which was kind of a rage post against people calling it a standard, because it isn't. That sort of feeds my concern that they're necessarily here. Implementations are important but I do see a separation from implementation their own workflows, and the specifications are informed by that. I'm not convinced that I want open source intimitately.

Martin: Part of the standards is diff'ing.... Going to disagree with Jeffrey, IndexDB also doesn't qualify. There is a significant part of the spec implemented differently in browser. Arguably there is single library shared. THe primary concern is we need to draw a line re OS and collaboration and picking winners on implementation front, and the latter is someting I dont' want to see. One gold implementation is like with Mastodon, and bunch of others effectively trying to define it.

Christian: Was is also WebSQL?

Christian: on the Agentic AI Foundation (AAIF), we looked, and however you need to buy your own vote, which is expensive.

Christian: The gov structure of that group is concerning. However I also agree that it is not for W3C-land. Same for OSS.

Sarven: Privilege to participate in standardisation.

Xiaocheng: There are defacto standard implementations that lacks maintenance. There might not be a clear boundary on what we want to host or partner with. It is definitely not how significant it is to web. Otherwise we should be hosting Chromium. The reason they're not at W3C as I understand is b/c it doesn't align with their goals / governance.

Lola: Similar to Xiaocheng, I disagree that we shouldn't host. We are speaking a lot of implementations but those are not the only kinds. I was thinking of MDN Web Docs. I don't think it is a good idea that Mozilla hosts MDN and have to go through them. All the web stndards that are created should end up there? Mozilla let go of many a few years ago. A lot of the things are for the benefit of these companies. Web Platform Tests is a core infrastructure, and if anyone changes their minds, then WPT ... re Sovereign Tech Fund, they run a survey, who had worked for agencies, and found that engagement was wide-spread. A lot of these open source maintainers rely on standards and should be involved in discussions, or necessarily rely on the implementation.

Brian: Mostly Google donated infra, where does code even live? What org it lives under or charge of that. I think it should be part of W3C, where W3C to define its own test suite. Chronos does that. It is even part of a lot of stuff, and this is how you know you can form. Mostly links to WPT. One is defining the test and the other is hosting, and latter is more expensive. Re MDN docs, way before the other docs, Microsoft donated a lot of their docs - WebPlatform docs, hosted by W3C - and Mozilla.

Hadley: We have this careful line between standards — the bare minimum that needs to be agreed so that things can be interoperable, work together — and implementations, which are then free to serve the needs of different users, to be creative in what they do, to innovate and create better ways to implement, new user journeys, etc etc. And I haven't seen anything in this discusssion to change my mind.

Also, having looked at MCP's github, their website and documentation, etc. — it's effectivectively standards. A protocol. Why does it come up in conversations about open source?

Jeffrey: I think because it's effectively governed as an open source project, using a governance model common in open source projects. Not a standards process.

Jeffrey: Bloomberg mentioned they are the only funder of Test262.

Matthew: Why isn't ECMA funding?

Jeffrey: I don't know if they did but needed money, and raised all to fund 262. So, we are in a bad situation and can imagine some ways out of it but didn't happen. Connects to WPT, and Google is funding it, and to give governance is a good thing but then there needs to be more funders. Some things W3C could host it'd be cheap but continuous integration or running of the code is not cheap. We need to look for ways to fund tests.

Brian: There is who is in charge of code. The process of how you get things in there. In theory it should be reviewed but in practice we don't have to. Tons of false positives there.

Jeffrey: We don't need to get into problems with WPT but how to structure a system that could fix them. I don't think hosting and control over can be separated. We need a system that motivates companies to fund the hosting. And a lot of times they want control in the system. It is a social problem.

Matthew: It seems like we're asking, if we bring things to W3C it'd be like how we do things? Otherwise I would say no.  If we bring people in is one thing, and that would have to be without governance. Hugely in favour of open source. I'd love it but not convinced we're the right place for it. Managing the test suites seems like a good idea.

Christian: On AAIF, we asked about working groups, workmode and so on. The response was that they don't know, and that they are currently figuring it out. +1 to Heather that setup seems questionable.

Sarven: Concerns around how groups are not aligned with our work mode. W3C is behind OpenStand. To build bridges, first can we agree on OpenStand? Right now they have their own governance, but fundamental parts are missing.

Xiaocheng: There are some software even critical for W3C, and I'm not sure how it is governed. Then what do we talk about these open-source projects in community groups?

Brian: Until a few years ago WebIDL was in someone's personal repo.

Hadley: There is a big difference between our own tooling and open source projects for the web. It doesn't make sense in the same way of how we look after them.

Martin: If primary source of cost of platform tests, all the companies that make the browsers have the infra and money to make it work.

Brian: For Servo and Ladybird and... the cost could be made manageable.

Martin: Thinking more creatively is important. For bikeshed, I maintain something that's used by IETF. Should the org take over that work? If ain't broke, don't fix. But being aware that the main maintainer might disappear. If public domain, someone can fork it, so not particularly complicated.

Lola: re Why is MDN considered open source software?

Heather: I thought W3C was looking at is the software bit.

Brian: It is the documentation of the web, and without it kind of screwed.

Martin: Could get by.

Jeffrey: I think the next steps are figure out testing and funding and hosting, but figure out what the rules are and what kind of governance, and start figuring out funding, and the incentives.

Hadley: Happy to answer but prefer to pass it on.

Jeffrey: re bikeshed example, I pushed something to speced for community org planning. People disappear sometimes or not responsive, and in order to get a more responsible owner.

Brian: Sometimes the tool is not the right tool or bit rot or do something with it.

Brian: Wattsi, a spec processing tool, written in Pascal was made by Ian Hickson (HTML 5 editor) for processing HTML, it's part of the WHATWG org - at least they do own their tools.
