# TAG minutes, week of 13 Jul 2026

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/07-13-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.


## Plenary Session - [2026-07-14](https://www.timeanddate.com/worldclock/converter.html?iso=20260714T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair:  Lola

Scribe: Sarven

Attendees: Heather, Lola, Sarven, Matthew, Ehsan, Luke, Brian, Hadley, Dan Applequist (guest)

### Process Stuff

#### How the AB and TAG choose chairs

Dan: https://www.w3.org/policies/process/#ABParticipation

Lola: {introduces Dan}

Lola: Dan will speak to us about how the chairing system works in AB, and changes that may be made that affects TAG, and perhaps TAG wants to adopt them as well as the ratification process.

Dan: TAG appointment process

Dan: Recently we (AB) had a meeting in Rotterdam. The AB is the elected body responsible of the "process", which includes verbage on defines what the AB is and what the TAG is. Including participation in TAG/AB, how members are chosen, chairs etc. Because the AB is responsible of the process, we are embarked on the mission, to simplify the process, make it less byzantine, ... we didn't want to take any resolution on things related to TAG without TAG's awareness. First is about chairing. The way the AB chairs are chosen is no longer desired. The Team chooses the chair and chairs choose the co-chairs, and it treats the AB differently than the TAG. There will be a public summary posted. AB wants to remove this, and move towards consolidating it to the elected body. To remove the wording that's currently under the TAG to a common section for both AB and TAG. Rough proposal doesn't change how the TAG works but the ask to TAG is how is the TAG chair choosing working.

Hadley: As I'm one of the co-chairs, I'll let others respond to that point. We have interim chairs as some folks take time off. We asked the whole TAG about what they think. We had volunteers, and there was consensus around them. It has been nice to have this flexibility to share that work and keep the work in control of how things run. And obviously the interim chairs don't have formal authority, but practically, we (the elected chairs) don't really either. So informally, I think it works out to be the same, or similar enough. 

Given the choice, my instinct would be not to put this interim chair arrangement into the process but also to not make it impossible.

Dan: One of the things with the process refactoring, where possible, swap out very specific procedural wording about how things happen with more general descriptoins that allow more flexibility. This is an example of that, right? The process doesn't contradict what you did but process doesn't need to talk about interm chairs. Likewise AB, some members of AB wanted to express their opinions in a confidential way in context of chair choosing. I think that's a cultural sensitivity that we need to listen to and be aware of. So, trying to figure out what that looks like. What element of confidential opinion we can work with. We should be able to have an informal mechanism, like confidential opinion, without it being algorithmic either.

Heather: At least when we were looking into interim chairs, when we have a problem with anyone in a chair role and not talking about it with the others, then I'd go to the Team to ask for their help. I agree we shouldn't be limited on that.

Dan: Some historical reasons why the process is written that way to take that into account.

Lola: It is not that I think it needs to be in the process, but want to flag potential pitfalls. If this is written in an official way, then we rely on AB to be consistent over different membership (AB). And there may not be a way ot point to as to who said what. For example, when AB changed last year and who is AB today is different. Some culture changed. You still work with the ghost of the past. That's (the) causing issue.

Dan: The issue isn't we don't want ot write it down or not but should it be in the process doc. Process is hard to change. AB has an internal docs in its wiki. The proposal will be to write down whatever process into that rather than being in the Process document. There isn't an AB issue on this but can send it when we do I can send. This shouldn't impact TAG so much, it is more about getting what you do right now.

#### AB proposal to remove the AB from ratifying appointments of TAG members

Dan: The second issue is 1178 in the process doc.  https://github.com/w3c/process/pull/1178 

To remove AB from the TAG ratification process. The Team appoints and there is a combination of AB and TAG to ratify those appointments. There was consensus to remove the AB itself. Secondly, the proposal to make is to remove the ratification process entirely. It caused more problems than solving. It initially sounded good but in the end, it turned out that there was some ambiguity on how involved/influential are TAG members are in the choice. If there is a problem with Team's appointment, we can use the regular objection process rather than a special ratification.

Hadley: The confusion especially came out the Team was appointing people that some TAG members didn't know them to say enough. I see the problems you'e outlined and agree. In the TAG associates process, we have had people suggest associates, upon further discussion, we decided they may not be people that we'd like to work with. Mostly for activities that were essentially code of conduct violations (even if in other forums or venues). If there is a way to solve that problem, I'm all for it.

Lola: That may raise an issue where only the Team is recommending. If someone is elected through AC, we don't ratify them. So, immediately, you are applying only that cultural fit question to maximum few people as opposed to the rest.

Brian: For the associates for the TAG, that makes sense whether to invite or not. For the ratificaftion thing, I think it'd be better to treat as Lola said Team appoint.

Dan: re Hadley's point, when we were designing the ratification step, someone may raise concerns about an individual. That was what we had in mind. The ratification process may not be best place to apply those concerns. We also had a requirement for a 2/3 majority, and not everyone voted each time, which caused other problems. 

Dan: If you have additional feedback, please ping me or another AB member. We may need a joint process CG Process regarding the second question.


### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Hadley: From the looks of it, we may be taking a strong stance on this. But instead of "we are against this" we use more like "we have serious concerns about this approach." 

The other thing is since we rarely come out this strongly, we should reach out to proponents, the CG chairs, and have a conversation with them before sharing our review so they are less surprised and understand where we are coming from. 

Luke: Agree with Hadley's point on the wording. Or some iteration.

Sarven: the type of solution they are offering, signalling at the weaknesses of how the web is working, how pages are published, how authors are making their documents available. So you've highlighted a problem, and maybe the solution is more towards fixing or improving those, as opposed to adding another technology. Accessibility of the potential actions is hard for random scripts to navigate around... why is that? We should look at improving that. "Great, you've pointed out something important. The solution to that might be different than you're proposing."

Heather: Agree with Hadley's approach, it doesn't shut the door re good / bad things. If this is going to be a TAG statement, we probably don't want to do that.

Lola: There is industry push for this and i think that complicates things a bit. Other tech proposed doesn't necessarily have that. That doesn't mean we need to agree to that but have to consider these things. And also think about the general direction of the web and how the web is moving. I haven't read the spec proposal yet, and if we are going ot be against it, and because of the context we are in, it'd be good to pull in the authors/chairs to discuss the issues and look into how to figure it out.

Matthew: Horizontal review groups have been asked "should this be part of the charter for the Web Machine Learning working group?" I agree that people want to do this, and I don't want to push them into doing it in less safe ways. At the same time, if we said we're ok with this, it would standardise a whole new set of security and privacy holes for which there is no known solution. So I agree with "let's work together, try and make it work."

Hadley: +1 to Lola.

Luke: In terms of positions, there is opposition from WebKit. I do agree with the perspective maybe wording it rather than saying this shouldn't be a thing, we could say, "here is a problem we see. There are holes in the security model here, and don't think it'll be solved appropriately."

Hadley: We had a number of situations in the past where we either published and watched the chaos, and that tends to lead to more opposition and blogposts, and our message, and then theirs, and it is not particularly collaborative. We have also talked with individuals as well, then they found that interesting/useful. So, just want to reiterate that we talk to them directly.

## Pacific Breakout (Asia / Australia / West America) - [2026-07-15](https://www.timeanddate.com/worldclock/converter.html?iso=20260715T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Heather

Scribe: 

Attendees: Brian, Dan, Marcos

### [explainer-explainer#39: Create an explainer-review skill.](https://github.com/w3ctag/explainer-explainer/pull/39) - @jyasskin, @marcoscaceres, @hlflanagan, @christianliebel

Heather: Christian had some ideas; we'll come back to this when he's back from vacation. 

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @jyasskin, @marcoscaceres, @bkardell

Brian: Marcos and I commented on some Web view issues last week. Still more work needed.  Kind of a bummer that our definition of a user agent wont match CRA

Marcos: Can one of us change?

Heather: Theirs is written in some law and they feel that they need to match and stay true to that

Brian: there's a new community group (https://www.w3.org/community/embedded-web-engines/) that will focus on embedded web engines that will overlap a lot with "web views".  Will be interesting to see. what comes out of that. 

### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu

<skip>

### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu

<skip>

### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin

Marcos: Before we can close this, we need to do something with infra (because we have overlapping definitions).

Brian: My understanding is that, based on WHATWG discussions, the basic definition would stay where it is and we would link to the TAG doc for more. But there is opportunity for us to improve the existing one in WHATWG. Suggest we finish the doc and see what can be broken out into WHATWG. 

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

Marcos: It's on my to-do list. 

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

Heather: They are still thinking about my comment re: nested iFrames. Still waiting to hear back. 

### [design-reviews#1233: WG Revision: CSSPseudoElement](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1233) ([Github](https://github.com/w3ctag/design-reviews/issues/1233)) - @bkardell, @xiaochengh

Brian: Xiaocheng and I discussed this; it is ready to post. 

### [design-reviews#1244: [wg/webappsec] Web Application Security Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1244) ([Github](https://github.com/w3ctag/design-reviews/issues/1244)) - @hlflanagan

Heather: There are no deliverable dates. Is that expected?

Marcos: Fair question to ask them now. 

Heather: Also noted they have two discovery items; we should watch that. Also, they reordered alphabetically, which makes the diff useless.

Marcos: They should hold off on reordering until after the review. Will post the questions.

### [design-reviews#1238: Incubation: WebMCP](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1238) ([Github](https://github.com/w3ctag/design-reviews/issues/1238)) - @marcoscaceres, @matatk, @toreini, @christianliebel

Marcos: What is your understanding of how WebMCP relates to the rest of our thinking about web architecture. 

Brian: Matthew pointed out this morning that this would open a whole new set of privacy and security holes for which there are no known solutions. This is a lot more like web services; it is not MCP. If you want to find a way to advertise your webservices, fine. There are many semantic things already existing for that. There is a lot of complexity and risk for something that is upside-down in terms of architecture.

Marcos: Can you say more about the web services bit?

Brian: From the presentations I've seen, the rationale for why WebMCP is necessary is that it's very complicated to operate a site. You need to emulate the whole browser and understand CSS layout and window aspects and how to understand labels and so on... But the actual operations are hidden in the code today. 

Marcos: Brian has hit on an important point. If you go to a website and it links to it's definition of where MCP is, it could in theory allow the agent to see there is a RESTful definition and I can operate the site independently of the UI, without muddying the whole thing by driving the site through WebMCP. There is a distinction between the agentic web (all RESTful, no HTML, etc) and the human web. And then there's the app side of things, and the app may advertise their own capabilities. Not necessarily to agents, but agents may leverage those capabilities. 

Heather: When I went through this I focused on what I know most about - and the amount of tricky scenarios that they just glossed over with regard to authorization - they talk about fully autonomous agents, but... it can even be an interesting continiuum along the way.  They talk about falling back, but how are they going to know - that all seemed unspecified as far as I could tell. They reached out of the web a bit - so it's like "here's all of the things that you could do on my site" but then there is also "check my email" which is a whole different thing.

Dan: I'm not directly involved in this, some of it is underspecified on purpose in order to allow for different interaction models.  So I think the idea is "how do we bolt something into the platform that allows different AI models to interact with the web" - it is definitely interesting the different authorizations that Heather was talking about. I definitely think they could go into more details on those things.  I like some of the things Marcos was saying about these sort of different levels.  It might be good to invite them here to talk about it - it might be the most time effective way to do this.

Marcos: I absolutely agree we can have them in a call - but I think the motications are clear and the intents are good, but the approach really needs to be iterated on more.

Brian: Would you propose we offer feedback then invite them, or invite them first?

Marcos: It depends on whether if others understand what they're proposing. We could send what we have then have them come chat. I don't feel strongly about it. 

Brian: We could say something like "We know people are interested in this problem; it is valid. But we don't think this is the way to go about it. Here are some questions we have." 

Marcos: I want us to have a productive architectural discussion. I'm worried people are entrenched in their solution because they were so excited to put it together. But there does seem to be other ways to solve these problems. The TAG should suggest they take a step back architecturally because it touches so many things. We don't want to segment the web into multiple parts like this. 

Dan: A lot of the security concerns raised on the thread reasonate with me. It would be interesting to hear how browsers are already managing this risk. 

Marcos: The way Safari interacts through Siri is different than how people do. Things are sandboxed in different ways, and that's still different from how other browsers do it.

Brian: It's not just about interrogating the page. To query about how to do something, you need to know about the query API; you take actions and hit URLs to get enough information to have the page in context for the AI. If it was just asking questions about the text, we wouldn't be having this conversation. 

Marcos: And that comes back to Heather's question about authorization. What happens if it hits an authentication prompt? 

Brian: Their use cases focus a lot on purchasing online, so those are relevant questions. There is a workshop coming up on this.  https://www.w3.org/2026/ecommerce-agents/cfp.html Sept 8-9.


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

No issues to triage; will spend the remaining time talking about WebMCP.

## Atlantic Breakout (America / Europe) - [2026-07-15](https://www.timeanddate.com/worldclock/converter.html?iso=20260715T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola

Scribe: Matthew

Attendees: Heather, Matthew, Lola, Mike, Dan, Sarven, Yves, Brian, Luke

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven, @bkardell

*bump*

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

*bump*

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

*bump*

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @hlflanagan, @lolaodelola

*bump*

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

*bump to tomorrow*

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

Brian: I think we put this on the f2f agenda; would be a good place to talk about it. Mentioned last night the new Embedded CG will be interesting here.

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

Mike: Ehsan drafted a comment; LGTM.

### [design-reviews#1223: Other Spec Review: Responsively-sized iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1223) ([Github](https://github.com/w3ctag/design-reviews/issues/1223)) - @dandclark, @toreini

Dan: I posted the clarifying question we had conesnsus on. Started discussion with Ehsan in Slack chat.

### [design-reviews#1229: WG New Spec: Attribution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1229) ([Github](https://github.com/w3ctag/design-reviews/issues/1229)) - @bkardell, @toreini, @hlflanagan

Heather: I'm unclear on what I'm supposed to review at this point, given we've asked for an explainer.

Brian: I think this is tied into conversations about Global Components. Talked with James Roswell about this at the Meet the TAG event. Two issues arising. One is that this really could use an Explainer. I commented on this; group is taking it into consideration. As Heather said, this is a big change to what you'd expect out of a UA.

Lola: Typically if there's no Explainer, we wait to review until there is one. This is a big spec, would be very helpful to have one, say what the user benefit is, what the impact is, who's involved, etc. If they're going to write one, we should wait.

Brian: Separate Explainer not required by the Process; they say that the first part of the doc is equivalent to the Explaienr, but I think it's not adequate. Some disagreement in the AC as to whether an Explainer is required for a spec that's undergone incubation.

Lola: If there are specific sections (like the Considerations, and Alternatives Considered) that we would not expect in the spec, that are missing, we should ask for them to be included.

Brian: I think I've put this across to them, Explainers aren't just for TAG. Lots of people across the industry will want to know about this. Especiallly for this, an Explainer would be really good. Some people have been able to use Claude to create a starting point for Explainer from the doc that was good. I tried this and gave it to them, and encouraged them to edit it to improve it without spending much time on it.

Matthew: (That's awesome, Brian--to be the change that you want to see in the world.) I don't wnt to derail this conversation too much, but an item I haven't spoken about with anyone is tied in with explainers and also the CRA. Jeffrey was probably way ahead of me on this before he went on leave. Architectural decision records (ADRs) would probably be in-line with the CRA. I'd love ot see a spreadsheet with agenda ideas, but I guess we're get there at some point. It's difficult to collect them in a GitHub issue.

Lola: Yes, we're collecting things for the F2F in a number of different ways, so we'll have to consolidate them at some point.

Luke: I think we need to push back when groups put the spec forward as the explainer. Many people need it for reviewing purposes. We shouldn't all need to burn through water and resources to generate one. Anchor Positioning for CSS was another that could have benefited from this - I'm sure there are many more specs that I would understand a lot better after reading the Explainer. Especially for Attribution. It's doing a specific thing in a specific way, but there are already around six different implementations around the web; this would be an important Alternatives Considerd section.

Lola: Likewise with DID Resolution - it's challenging to review without the Explainer. I think it's fine that you've given them a starting point, Brian, but we shouldn't have to keep doing this. May have been good to speak with Dan Appelquist about this, as IIRC he championed Explainers.

Brian: Yeah, around 2014 or so.

Lola: If there are Explainer sections that are not in the spec, we should ask for those at least. Please do ask.

Brian: Having the generated one is better than not.

Heather: I always assumed I needed both - the Explainer helps me get started, and the spec provides the detail.

Sarven: Some of the reviews I do, I make use of the Explaienr first; on others I dive into the spec first. Sometimes I don't rely on the Explainer as it's not as authorititive as the spec. For one, I sensed the Explainer was machine-generated, and I read the spec, and the issues they had for it helped me understand what the group was up to. This is just for me, nothing general for every person and spec.

Lola: They're not a replacement for a spec, but are good as a primer. Sometimes the Explainer is poorly written and needs work.

Lola: Should we wait for them to create one, or use Brian's generated one?

Brian: For me I think the comments I have are nothing that they wouldn't've heard already. This is a whole new ball of wax - responsibility for UAs - it's unusual in ways that I think are not great. It copies some design mistakes from Web Speech, to me. I don't think on purpose, but has some similarties that are not good. I have reservations about the whole thing that are not just architectural.

Lola: Should put that in a comment. Helps to know what TAG thought at a specific time. Please draft a proposed comment and we can review it.

Matthew: Ehsan's on this one, and I've looked a bit, as well. I think we might have some questions for them, but I need to sync up with Ehsan, first. I might be able to do that before tomorrow's call. I would like to review the comment (and maybe contribute to it) before it goes out.

Brian: I think questions would be a good first step. I think the comments we have are relatively shallow. Most of my questions/thoughts... need to dig more into how I think about some of these more centralised global things that we are putting in the browser. That's why I was reaching out about the Global Components discussion. Not exactly related, but one may inform the other.

Lola: Sounds like two things to me, how these things fit into the architecture of the web, however this isn't the first time when we've been in that kind of situation. I wouldn't hold off on commenting on this review until we've had that bigger discussion.

Heather: +1. I want to have that Global Components conversation because I don't see the thread that you do, Brian, so I'm interested in that. That's probably an hour or two of our f2f but I don't think this review can wait that long. Happy to push back with the questions I have, and requesting an Explainer before we dive in.

Brian: Sounds good.

### [design-reviews#1234: WG Revision:  wai-aria-1.3 20260604](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1234) ([Github](https://github.com/w3ctag/design-reviews/issues/1234)) - @matatk, @lolaodelola

*bump* (Matthew to propose closing comment as discussed)

### [design-reviews#1237: Other Spec Review: CSS Image Animation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1237) ([Github](https://github.com/w3ctag/design-reviews/issues/1237)) - @bkardell, @matatk

*bump* (Matthew to propose closing comment as discussed)

### [design-reviews#1239: Other Spec Review: CRA web browser standard](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1239) ([Github](https://github.com/w3ctag/design-reviews/issues/1239)) - @toreini, @hlflanagan

Lola: Heather asked in Slack if anyone else can review.

Heather: Ehsan has comments on the way. Is anyone else interested in chiming in? When asked what they want us to look at, they said the whole thing. I don't know enough of what's happening at the TLS level, but commented on what I could.

Matthew: That probably means waiting for Ehsan to review my review.

Lola: I think we should do this differently to a typical review. Normally we say 'these are our questions on the whole thing' and have a dialog. But in this case, I think we will be async, and can do this better as a rolling review. We're already missed the two-week deadline, so we're no longer beholden to that timeframe. It's a lot of technically challenging stuff. The people who've composed it don't have web/browser experience, so the input will probably be of help. And this is a bit harder than a normal spec review. So, rolling review; post questions as we have them. We could start opening issues in their system (GitLab).

Luke: Not a TLS expert, but if there are specific questiosn that you have, expertise that you need, it might be worth linking to those, and I can try to work on specific bits. Don't think it's going to be valuable for me to read through the whole thing.

Lola: If you have a look at Heather's comment in the brainstorming thread you'll see what she's written about places where she has questions. Brian has posted about where they've posted this (GitLab). We can figure out raising issues later.

### [design-reviews#1242: Other Spec Review: HTML menu elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1242) ([Github](https://github.com/w3ctag/design-reviews/issues/1242)) - @matatk, @christianliebel

Matthew: I'm  just seeing this now: they answered our questions about the existing review. It links back to previous discussions and Scott O'Hara's blog post. I am not an expert, but given the discussion that we had last week in TAG, and to my mind, yes it has been part of the platform for 30 years, but it has completely come full-circle in terms of how it's used. It's basically the `<ul>` element. I've never come across it being used anywhere at all, and I've audited quite a lot of websites. I'd be interested in what other people think, though, because it does seem like it would be neat if we could use it. If we look at the data and learn that we cannot, then that's fine. It links to a few different things about the scope of the review, so I'll need to think about that. (Scott's blog post was great, by the way, and I appreciate that they don't want to break things.)

Luke: One thing that might be worth asking them for is if there's a Chrome use counter for `<menu>`. I have a suspicion that this will have high usage. Some devs seem to really want to use it. I think if this change were to be made it would have to be opt-in via an attribute. But then maybe the benfits aren't as strong. I think it's worth pushing on this a little more, to get enough data to make the decision.

Dan: There's a parallel to the customizable `<select>` where we ended up using the old element, and a CSS opt-in to the new features.

Luke: I think it's similar, but the opposite decision is correct, as in the case of `<select>` it has the right semantics to start with.

Lola: Matthew, you will respond.

Matthew: Sure. I'll check out the bit about the scope of review, as well.

Sarven: Is the proposal attempting to put something in place that works similar to `<dialog>` - it would have some affordances that come with being a menu. Dialog allows you to interact with it in different ways, e.g. instead of the alert thing popping up, you are able to put HTML content in there. It's clear that there is a plethora of examples of things having a menu. Being able to escape, or use keyboard to navigate, is important. The interaction pattern is often re-invented.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

*Our work is already done!*

## Eurasia Breakout (Europe / Asia / Australia) - [2026-07-16](https://www.timeanddate.com/worldclock/converter.html?iso=20260716T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Chair: Lola

Scribe: Sarven

Attendees: Matthew, Lola, Ehsan, Luke, Yves, Marcos, Sarven

### [tag.w3.org#101: Update Yu Sen participation](https://github.com/w3ctag/tag.w3.org/pull/101) - @ylafon, @hadleybeeman

Lola: ok with PR?

Yves: Yes

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

*bump*

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

Sarven: https://github.com/w3ctag/user-agents/pull/49

Sarven: Tried to keep it aligned with parallel discussion on "user agent" definition and Note->Statement, or at least not conflict.

Matthew: First impression is awesome. Concise. In issue 29, Hadley was mentioned as someone that might have thoughts.

Lola: Marcos, myself, and Hadley can review.

### [design-principles#616: Create an "accessible by default" principle.](https://github.com/w3ctag/design-principles/pull/616) - @jyasskin, @atanassov

Matthew: Made a minor change. dbaron's comment was interesting. Brian suggested we find more scoping/detailing. Waiting on feedback.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

*Matthew still working on the comment - sorry for the delay*

### [design-reviews-private-brainstorming#217: WG New Spec: RDF 1.2 N-Triples](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/217) - @csarven

Sarven: Yves and Jeffrey have been contributing to this too. We had some concerns.

Yves: Yes, originally about the media type, and after discussion with them, trying to have a good story for the 1.2 to _next_ transition. That was the start of the discussion.

Sarven: We ended up with them needing to be more clear about what parsers should do (error handling, messages returned) in these future cases. We left a comment.

Yves: I discussed with Pierre Antoine. Not that we want to mandate a particular processing model, but that we need predictability as to what would happen in future version transitions. E.g. defining a priori what the parser should do - e.g. stop, stop but continue. Trying to pin down what the parser does when it encounters a future version that it doesn't understand. Could look at things like ordering the triples according to version so as to be sure as to how the parser will handle or ignore things.

... Another option they proposed is to have dynamic errors (returning an error, but continue processing) vs stopping completely. Could be an application layer choice. So we are looking at ways to get clarity without being strict about behaviour.

... The group's response was along the lines of not wanting to be like CSS [forwards-comp] - though that wasn't exactly what we were aiming for; we want to be sure that whatever the behaviour is, it's predictable. It's a real problem if future applications can't know what will happen.

... If the group doesn't want to move away from the current approach, we'll have to close as unsatisifed. it is a very risky approach. This isn't anything against this group, or to mandate a specific model to them. It's just to encourage them to care about predictability, as we have had problems like this before.

Lola: So, sounds like we don't think it should be happening in the way they're proposing?

Sarven: Where we started was that they need to create a new media type. It came to a point where we're kind-of letting them work around the current architectural constraints. I think the discussion with Pierre Antoine was promising, but isn't captured in the public design review. I don't know if the WG is going to make _any_ sort of a change right now. I don't think they're tracking an issue, other than that this design review is open.

Yves: I think there's a PR from Pierre Antoine, but no issue behind it. Need to check.

Sarven: [PR 107](https://github.com/w3c/rdf-n-triples/pull/107). I thought the PR was sufficient.

Yves: The issue is that in this PR they say 'the parser should raise an issue' but that's not enough, becuase it's not specified what would happen after that point.

Sarven: Isn't 'what happens after this point' out of scope for the parser, and more in the scope of the thing that's consuming the content.

Yves: The parser should say, after an error, 'I plan to continue', or 'I can't continue'. The appilcation can then know if, after that error, everything has to be dropped, _or_ whether I can flag that there's something I missed (and may enter a degraded mode), but can process the rest. If the parser can't produce any triple after that, then maybe the application should use a different way to request the stuff that was not processed. It needs to be clear which path is gonig to be followed (whichever that may be).

Sarven: I see your point on needing this clarity. In our feedback to the group, shall we ask them to specify this more clearly with respect to the signal the parser sends back.

Yves: Yes. The most important thing _isn't_ copying what CSS did; it's being predictable.

*An updated comment will be written and reviewed by Yves and Sarven*

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: It needs editting. Didn't just want to close as satisfied; wanted to raise the concern we have that we are not getting enough input from developers.

Matthew [proposed a closing comment (that really needs editing)](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/223#issuecomment-4989973806).

Matthew: We asked them to make it possible these things might be slowed down by UAs and give time people to process them. 

Related platform wishlist item: Giving users control over motion · https://github.com/w3ctag/gaps/issues/15

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow

*Pending external feedback*

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Ehsan: I can review part on components and start discussion. Should I wait for Hadley or both with Jeffrey?

Lola: Hadley. As long as Jeffrey's points are in there too.

Ehsan: I did get approval before Hadley's comment that needs to be integrated.

### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh, @lukewarlow

*Matthew still working on the comment - sorry for the delay*

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

*Matthew still working on the comment - sorry for the delay*

Regarding the discussion about accessibility, ATs, fingerprinting, that we discussed: Matthew raised this on a recent Web Accessibility Initiative (WAI) Coordination Call, and it got a good reception; working on a draft breakout proposal and will circulate to anyone who's interested in joining, so we're ready to propose it when proposals open.

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

Ehsan: Had a conversation with Martin. We're now on the same page. There were some sentences that caused misinterpretation on my end so maybe edit those and make it better. Overall I'm happy with the spec and fine to draft a response.

Yves: I already proposed a title of the change. The new version of the spec's title changed.

Ehsan: I already drafted but will check again to be up to date. The algorithm of how it work, I agree with the spec.

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

Yves: This shouldn't be there because it is part of ??? discovery.

Matthew: We discussed last time but dont' remember outcome, perhaps to discuss in Sept.

Yves: Heather is part of that WG. I can draft a comment and ask Heather to review.

Lola: Yves mentioned "there was no common approach" and perhaps that's the comment we send to them.

### [design-reviews#1222: Other Spec Review: Single-Axis Scroll Containers](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1222) ([Github](https://github.com/w3ctag/design-reviews/issues/1222)) - @xiaochengh, @lukewarlow

Luke: I don't know how many immediate concerns are jumping out at me. I thought it might impact accessibility in some way.

Matthew: I do want to look at it. Anything with scrolling on one axis is okay.

Luke: It doesn't do the new behaviour. It only uses the new behaviour if you used double key with double index.

Lola: is that enough? If you're a developer, and used key for any pari, is that going to work as extended if this is a breaking change?

Luke: A conversation to have. Worth flagging.

Lola: If it is going to be confusing for webdevs, then we'll probably not mark it as satisfied. Post initial comment.

### [design-reviews#1228: Other Spec Review: overscroll-behavior: chain](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1228) ([Github](https://github.com/w3ctag/design-reviews/issues/1228)) - @lolaodelola, @lukewarlow

Lola: I wrote a draft comment ( https://github.com/w3ctag/design-reviews-private-brainstorming/issues/283#issuecomment-4959008804 ) want others to look re satisfied with concerns. I was sure that the naming of this is confusing. I did use the AI skills thing - raised a few things I didn't feel comfortable. The diff between is one allows local and the other doesn't. If you're a webdev, it could be confusing b/c one is chain and would assume chaining of local and non-local.

Luke: When I first read your comment, it made more sense. Agree it is worth raising the naming thing. 

Lola: I knew we have design-principles on naming things. We haven't raised this before but this is something whereby the design principle .. CSS properties are usually nouns but the values are adjectives. The more I read, they are using chain as the verb, rather than a chain. We shouldn't use verbs any way. We encouraged them to consider that name the difference. Is this enough to mark satisified with concerns or something else?

Luke: I think this is ok with satisfied with concerns. It is not always ok they're ok. If we take all of the CSS properties/vlaues, how often do they meet the design principle. On the whole this is mostly correct. The word chain could be a noun or vern as you said, but some could interpret different. Fine to do satisfied with concerns.

Lola: Any objections?

Sarven: no, and +1.

### [design-reviews#1235: WG New Spec: Soft Navigations and Interaction Contentful Paint](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1235) ([Github](https://github.com/w3ctag/design-reviews/issues/1235)) - @xiaochengh, @lukewarlow

Skip.

### [design-reviews#1240: WG New Spec: Ignore Duplicate Navigations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1240) ([Github](https://github.com/w3ctag/design-reviews/issues/1240)) - @ylafon, @marcoscaceres

Yves: I didn't look at it yet.

### [design-reviews#1241: [wg/atag] Authoring Tools Accessibility Guidelines Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1241) ([Github](https://github.com/w3ctag/design-reviews/issues/1241)) - @matatk

*Closed as per previous discussion*


### MCP

Marcos: Not sure how we proceed. Give everything or have a position? There are such variety of positions and facets, and I'm worry we might loose the nuance if we have one position. But there is also the urgency.

Ehsan: Agree with Marcos. My only concern is that it might be overwhelming. Could have a discussion with them as mentioned before.

Matthew: I think I'd like to edit some of the feedback if we are going ot put it across them. Certain things are privacy/security an we can bucket them in rough areas. There are upcoming other proposals that seem similar to WebMCP; there's clearly demand for this sort of thing, so we do need to put across our concerns. Somethign struck me about this spec: it says it's about user and agent collaborating, but the agent could call *any imperative function to do anything: it's not tied to the page, or content on the page* (this itself creates a lot of risk, as the agent could be doing something totally different, or receiving content that's totally different, as @AutoSponge pointed out in APA's discussion of this). On the web, we usually develop a simple, declarative API first, and then an imperative one for any edge cases if needed later, but WebMCP is imperative first, which is concerning. The CG report actually links to a proposed Explainer for a declarative version, which _is_ tied to form filling and thus content on the page. This is much more aligned with the agent and user collaborating. They don't require it in the explainer, but I think should that the UA should ensure the user can always review a form filled in by the agent before submission. The Explainer does talk about styling forms to indicate the agent filled it in. I think we would still have significant privacy concerns, but _maybe_ the declarative version could provide a better way to experiment first?

Sarven: Is this a good lens to use for UAs to experiment with what a UA is? Matthew seems to be saying there's a potential misuse of what's being proposed - on the surface it seems like what an agent can get hold of from the web page, but could be used for something entirely different, and there's no way to constrain that. We need to make sure that whatever UAs do, it's done with an understanding of their duties (they MUST be acting on behalf of the user).

Lola: I like Marcos' suggestion of posting our thoughts. If we're posting as TAG there needs to be consensus. Not saying we should post a position, but don't want us to post something publicly whereby other members of TAG may not be comfortable. The discussion is ongoing. Consensus just means you can live with this. We don't need to spend ages.

Matthew: we could post as individuals.

Lola: Hesitant to do that. Especially for something like this raised concerns for proponents in the past. One might see one TAG and unclear if posting as individual or for the whole TAG. That question would be ongoing. In the past it unnecessarily confused things.

Luke: What do you do in a situation where multiple people TAG have things that are important but not necessarily consensus. It'd be also unfortunate if that feedback can't be provided.

Marcos: We don't have to put it directly on the issue. We can get feedback to them and clear that's informal.

Sarven: We should have a single voice on something like this but makes sense to have an informal conversation with them initially.. instead of posting something publicly which may carry more weight.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)


