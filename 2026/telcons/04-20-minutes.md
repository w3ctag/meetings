# TAG Minutes - Week of 20 April 2026

This agenda can be viewed on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/04-20-agenda.md).


## Plenary Session - [2026-04-21](https://www.timeanddate.com/worldclock/converter.html?iso=20260421T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### RDF-1.2 versioning story: https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161 / https://github.com/w3ctag/design-reviews/issues/1161

JY: the issue or question is around the RDF 12. versioning could work
it's unclear from the document how it works
There is no description for how the ecosystem system should adjust and how servers and clients should deal with that
how do you expect the ecosystem to handle updating to the new version 

PC: RDF 1.2 is an incremental change with two new features 
the data model is not unchanged
it is still expected that the new RDF 1.2 data should still work with old clients
There was consensus in the WG that this is ok.  There was question in the goup about whether we should create a new media type, but we decided not to..
Because the new version is still backwards compatible so server can still signal they are 1.2 
So clients can still keep processing "RDF" even if they don't know about the new features
As the media type does not distiguish between the two should still continue to work on old clients
So the old client may signal an erros even though they don't know what to do with the new format
RDF doesnt define what to do when a feature is unknown by the client
RDF's fallback model is not the same as HTML in that sense. The behavior is undefined.

BK: You said that the WG chose not to create a new media type, but I didn't understand that you'd articulated why - I'm interested as to hearing the rationale for the choice

PC: Imagine the ?? format that is based on RDF. This format could sever the 1.2 media type 
Content media is not always an option
Some clients will use the new feature but others won't 
There are situations where the server will serve the new media type, but that would cut off the old clients
So the rationale is to not to damage the ecosystem, as we don't want old clients to fail on the new media type

OL: This is somewhat polical, but I wonder what will happen if we split the world between RDF 1..1 and 1.2 
There is going to be significant cost and we don't know what that is going to be

JY: We are trying to understand the implications in the range of options: will it drop the unknown properties? Will it just work? will it ignore the whole file? 
We would like for you to document what will happen, as the WG knows the ecosystem best

SC: the TAG feels the right solution is to send a new media type. Given the capabilities, it's can be a new media type because of the new constructs in 1.2. So there's a bit of a mismatch, because if the old clients can't parse the 1.2 then that could be a problem since it is a different format. So, what's acceptable to keep and throw out. In 1.1 it was ok to igore it... it might cause the client to crash. But that's not defined in the spec. If the media type is text/turtle, then there's an expectations for clients for what they are going to get. 

SC: the working group is in the best postions to guide the TAG here because we (TAG) don't know what the impacts are going to be. So we are wondering form the group. For the TAG, the new media type is the logical solution here, but maybe the WG is in the best position to make a call here. If the concepts explain the landscape well enough, but we didn't get that from reading the spec - that's why we find ourselves here to resolve that. 
  
Marcos: There are hard lessons to be learned about ... HTML used to be very loose, and that lead to security issues, which is why you see strict enforcement of contect types. Need to watch out. Ora mentioned that we don't know what's going to happen to the clients. The documents don't say what will happen. Something bad could happen, and making the breaking change is important to consider. If clients start behaving differently, could be a problem. If there's something semantically important, and the new properties change the semantics, and trhe clients don't understand that. There's not defined fallback model, while in HTML there's a very defined fallback model. Core part of HTML is that the user comes first. Different from XML approach, where a broken tag makes parsing fail. In web platform ecosystem we moved away from that for HTML, while JS breaks entirely with bad syntax. For the end user, who suffers when they can't read the 1.2 syntax?

Ted: Not *one* new media type; *~ten* new media types, one per existing serialization. Note that this problem was largely created by the hubris of previous Working Groups (and their reviewers) who were encouraged to think, "this will be the only version of this, ever."

Ted: The previous editors thought there wil only ever be a single version of RDF. This WG was not chartered to make breaking changes. So there is a risk of blowing the scope of the WG.

Ora: my worry is about the adopting. It's taken a long time RDF getting adopted and I don't want to put up new hurdles for adoption. RDF is used in a lot of enviromments where media types don't always pay a role, so that's not clear to me. So I'm unsure about the forward compatabilty story. So we are unsure what the original editors were thinking about when it comes to future compatibity. We don't know what the damage is going to be if we add the new media type. 

Pierre: to answer some of the questions. Sarven, I would call back to the damage to the ecosystem, and I hear you acknowledge that. To Jeffrey, we try to address the server concerns in the spec itself. In some cases the server won't care. There are cases where server does care where it uiltimately what goes to the client so we do have a way to provide an alternative way to encode the new properties  so it's 1.1 compatbile. So servers that care can downgrade the data to be 1.1 compatible. To Marcos' point, there are very generic syntaxes, with a generally very low level of semantcs. For things like digital identity, when RDF is used, it is used with a media type and that's a good thing. The ideal model is that RDF is processor neutral, but people people point out that is not the case. But the spec say that it is. 

JY: You could require new clients to send 1.2 parameters. That would mean that servers are supposed to send 1.2 things in response. 

PC: we did some testing and we found it wasn't an issue. 

JY: If they define how clients behave when they see an undefined triple or if they should drop the whole client, then at least future clients will have a specified behavior model. 

YL: I was going to say the same thing. If you define the breaking change model now, then future version of the spec will be covered as new clients are implementing the breaking change. So that gives you an out in the future. 

OL: I like what Yves said. It might be good to be the people that fix it now for the future WG. People are supposed to upgrade things for security reasons. 

JY: are we TAG ok with keeping the old media type? 

Andy: one of the justifications for putting the breaking change behavior is to protect ourselves to the future. In turtle, it's a parser error. So there they can cope by erroring. So turtle doing error recovering is non-conforming. So, it can behave like HTTP error correction might, what do you do with junk data, etc. 

JY: If you say the whole file must be dropped, that reasonable. I didn't see that in the spec. 

Andy: it might be a "sin" so you might end up dropping data. 
 
Marcos: I'm ok with it if there's evidence about the error recovery. You've described the fallback model: if someone sends a 1.1 request and you're a 1.2 server, you can jiggle the values to make it work. Has to be explicit. Hope we've convinced you it's needed going forward. Appreciate minimizing damage to the ecosystem. Specify the behavior so there's protections for later. Is the Turtle representation ... the Turtle one gives an error on new data? XML? Do they do the same error recovery?

Sarven: Think they're all different. 

Andy: Not specified. Think the behavior is complete failure. Might have been a recovery attempt for N-Triples. For XML, structural errors will come from XML being wrong. XML parsers tend to be very picky. Could specify that.

Sarven: I want to acknoledge that the situation is not ideal. With the cost of a new media type being well understood... whether this sets a precedence for other specs, that sets a bad precedence. We, TAG, need to look at the example here / lessons / considerations and document that for our understanding so that we are clear on tradeoffs vs. correctness. I agree with Marcos that the behavior should have something specified. Here we seems to be weighing things. We seem to be agreement that the current solutions is not the most idea situation. 

Yves: to talk about existing infrastructure, we still have HTTP 1.0 servers that are potentially buggy. So its good to understand what is happening in the RDF ecosystem, so if changing the media type is right and what the impact will be. 

Marcos: Lesson from old IE 6: The Great Reverse Engineering Effort at the WHATWG. Given that these implementations are open source and freely available, throw lots of things at these servers [clients?] and see what happens. tHat might give you a story to put in the spec. Jsut document what programs actually do. Might find that servers in the ecosystem have aligned on a certain behavior. If 90% do error recovery in a certain way, can go with that. Lots of ways to recover. It's painful archaeology, but it's doable. Test suites. See what comes out from the servers&clients. Might answer the question. Re Ted, don't know how concerned you should be about taking time. RDF has been around a long time, ok to take a bit longer. Charter extensions are cheap.

Ted: Working group members are not encouraged to consider charter extensions as cheap or easy. 

### AI in design review process

Reviews that have been pending external action for at least 6 months

Lola: Let's talk about the AI review. There have been siloed discussions having in various places. But would be good to have discussions here. 

Lola: we have consensus from the TAG that we won't publish AI written design reviews (https://github.com/w3ctag/process/blob/main/guide-for-tag-members.md#using-ai). Other things that happened was from the AB (https://www.w3.org/TR/llms-standards/), where they said that using AI tools are helpful in spec writing process. 

Lola: in hong kong last year we talked about potentially having some kind of prompt to pre-check submitted explainers. Would like to hear form the TAG about the above? 

JY: I wanted to share these research papers (https://c3.unu.edu/blog/the-echo-chamber-in-your-pocket) that models often just validate what one proposes. AIs will be useful potentially if we can give people a prompt to run, but we should be careful when using it on our own reviews.   

Christian: We have to be careful, of course. But it happens. Code is being written and reviewed by AI. Is did lots of reviews with AI, but also did it myself, and I also compared. It caught things I didn't see, and I caught things it didn't. Wouldn't ban the tools. See what makes sense. But for our own reviews, need to be very sure that it's human-reviewed and matches what we think.

Ehsan: Following Christian, what I've seen in papers, is that using AI for reviewing is fine, but seen a recent trend to do prompt-injection inside the papers to forge the reviews. Sure if we do the same, proponents might use that, leading to some forged reviews for their benefit. No protection, just need to be careful.

Marcos: There are protections: tell the AI to watch for prompt injections. There are peer-reviewed articles that show how to do hallucination detection, and how to verify every claim. Can use multiple simultaneous agents to run over same question. Whole things about "can get injected". A lot of people don't know how to use AI, and that's true. But if you're skilled, you can write self-protecting prompts. Doing it naively can be bad. Worries are real but also overblown. In naive hands, sure, but not in skilled hands. Could have copilot do checks if Github brings it back. Doesn't have to suggest things, can just ask questions.

Sarven: Think it's a tool at the end of the day. Worry about recycled content, and pattern matching from previous stuff. Bar for TAG and other groups should be higher to create new thinking. Shouldn't just solve a puzzle based on previous knowledge, or pigeon-hole it into the example of previous reviews. People look to the TAG for deeper knowledge. They also have access, so we don't need to re-run the script to come to the same conclusion. We may use the tools to help us think through and put content out. I'm trying to put the bar higher for myself to produce something people haven't already read.

To be continued...

### [design-reviews#1153: WG New Spec: Direction feature for `scroll-state()` query](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1153) ([Github](https://github.com/w3ctag/design-reviews/issues/1153)) - @matatk, @xiaochengh

## Pacific Breakout (Asia / Australia / West America) - [2026-04-22](https://www.timeanddate.com/worldclock/converter.html?iso=20260422T000000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

### [user-agents#47: Can we cite user agents in normative specs?](https://github.com/w3ctag/user-agents/issues/47) - @jyasskin


### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36) - @martinthomson, @jyasskin, @imsenyu

### [user-agents#43: Webview: avoid multiple permissions at once](https://github.com/w3ctag/user-agents/pull/43) - @imsenyu

### [user-agents#40: Webview: risky navigation warning](https://github.com/w3ctag/user-agents/pull/40) - @imsenyu

### [user-agents#41: Webview: embedded area indicators](https://github.com/w3ctag/user-agents/pull/41) - @imsenyu

### [design-reviews#1210: WG New Spec: Programmatic Scroll Promise](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1210) ([Github](https://github.com/w3ctag/design-reviews/issues/1210)) - @xiaochengh

### [design-reviews#1213: Question: Capability Delegation stalled -- specs are implementing local workarounds](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1213) ([Github](https://github.com/w3ctag/design-reviews/issues/1213)) - @jyasskin, @hlflanagan

HF: updated brainstorming w/ comment. Please review. 

### [design-reviews#1192: Incubation: speculation rules `form_submission` field for prerendering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1192) ([Github](https://github.com/w3ctag/design-reviews/issues/1192)) - @dandclark, @xiaochengh

### [design-reviews#1196: [wg/webperf] Web Performance Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1196) ([Github](https://github.com/w3ctag/design-reviews/issues/1196)) - @jyasskin, @marcoscaceres

### [design-reviews#1194: WG New Spec: HDR on the web (CSS, Canvas, WebGL, WebGPU)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1194) ([Github](https://github.com/w3ctag/design-reviews/issues/1194)) - @jyasskin, @xiaochengh

### [design-reviews#1207: Incubation: Prerendering cross-origin iframes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1207) ([Github](https://github.com/w3ctag/design-reviews/issues/1207)) - @marcoscaceres, @hlflanagan

HF: updated brainstorming w/ comment. Please review. 

### [design-reviews#1205: WG Revision: MathML 4](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1205) ([Github](https://github.com/w3ctag/design-reviews/issues/1205)) - @jyasskin, @matatk

### [design-reviews#1211: [wg/webauthn] Web Authentication Working Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1211) ([Github](https://github.com/w3ctag/design-reviews/issues/1211)) - @marcoscaceres, @hlflanagan

HF: Question sent on Slack about AI and accessibility tools

### [design-reviews#1198: Incubation: CPU Performance API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1198) ([Github](https://github.com/w3ctag/design-reviews/issues/1198)) - @jyasskin, @marcoscaceres

### [design-reviews#1195: Question: should `shadowrootadoptedstylesheets` perform a fetch?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1195) ([Github](https://github.com/w3ctag/design-reviews/issues/1195)) - @jyasskin, @bkardell, @dandclark

### [design-reviews#1215: [wg/wot] Web of Things Working Group rechartering](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1215) ([Github](https://github.com/w3ctag/design-reviews/issues/1215)) - @jyasskin

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Eurasia Breakout (Europe / Asia / Australia) - [2026-04-23](://www.timeanddate.com/worldclock/converter.html?iso=20260423T080000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Ehsan, Matthew, Luke, Yves, Marcos, Christian, Hadley

Regrets: Sarven

Scribe: Christian, Hadley

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

Matthew: No update.

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

(Skipped.)

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: Two questions (???/dynamic handling of content) open, not sure if we should probe on it. Had a big discussion about animation speed. Speed UA-controlled or author-controlled? Big discussions about UA responsibilities.

… Side note: Really good accessibility considerations section. APA started to draft one, but theirs is really good. Acknowledging their work.

… Put in the comment for review. Happy to do it now or async.

Lola: Can review this async.

Luke: On UA controlling the speed, came up with Interest Target. Problem we had there that this would end up being observable that the UA has done this intervention. Would that be the case here?

Matthew: We advise against making the use of accessibile technology detectable, but the benefits may outweigh this (think dark mode). We should get together CSS and a11y people together at some point and have a talk about these trade-offs. Should we consider them more on a case-by-case basis?

Luke: Wider discussion than just a11y/privacy. Comes up a lot. Personally think that a11y features should be implemented with privacy trade-off. Some should be on by default (e.g., dark mode), others opt-in.

Lola: It's good to review specific things at a time, but we also need to consider the combination of the technologies. Dark mode by itself may not be problematic, but the combination with other add-on devices may be. There are valid reasons why we want to be careful. While acknowleding not to decline everything.

Ehsan: Luke, when you say privacy trade-off: I'm a bit concerned that the threshold for the decision is a person with a disability whose privacy would be put at risk. Has this been discussed?

Luke: Re Interest Target, idea was to have keywords, and user agents would be able to increase or decrease that based on user needs or timing-related things. Authors can specifcy a concrete value now, but I believe the spec still allows UAs to intervene and change them. (?) Size of the bucket is quite important, and inferring further information.

Matthew: Appreciate the concern how this may affect people that may be vulnerable. People that alter related preferences may not consider themselves vulnerable. The bucket is maybe bigger than you think. For example, you can't tell if features are used for a11y or purely aesthetic reasons (e.g., dark mode). So we may relax some of the proposals as needed.

Lola: I'm going to review Matthew's draft comment, encourage others to do it as well.

### [design-reviews#1187: [wg/das] Devices and Sensors Working Group 2026 Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187) ([Github](https://github.com/w3ctag/design-reviews/issues/1187)) - @jyasskin, @marcoscaceres, @christianliebel

christian: Not much to say on this. We do have a deadline, end of May. The issue needs to be resolved then. The working mode we envision is a deputy one: where I will talk to the TAG internal side, and to the at least DAS working group chairs (Anssi and Riley), we'll do the talking back and forth regarding our suggestions on the agenda.

We did that for one of the first points already, and we will continue doing that. 

Lola: Understandable. 

Marcos: The deputy should be meeting ideally with the working group. We are asking the working group to make these decisions. Failing that, meeting with the chairs and the team contact. ultimately, the implementation experience is defined by the team, so they need to be part of that process. Check what the W3C Process says.

Luke: This may already be noted, but one fo the tentative deliverabes is the web serial API. WhatWG seems to have that plus the WebUSB APIs, a proposal for a whole set of device APIs to put them under WhatWG instead.

Marcos: Mozilla has taken the APIs the propose to DAS and proposed to do them as a workstream at the WhatWG. From the TAG perspective, if that happens, then those problems go away. But it's confusing that there is a proposal to send them both to the W3C and the WhatWG. 

Hadley: TAG's focus is the entire web platform, so this would still be our focus even if it should be moved to WHATWG. TC39 too. We may not have the same mechanisms, but we can still have opinions, and it's our responsibility to consider it in scope.

Christian: Ok. I'm on it. I will report back. 

Lola: this is the first time we're doing this process of having a deputy type person. once this is done, it woudl be great to hear from you how it went, as the person who has to navigate all these voices.

Marcos: Any notes from our previous meeting with Anssi?

Christian: it was 1:1. so no.

Marcos: so we'll build that in, so there is some kind of record. 

### [design-reviews#1206: Other Spec Review: OpaqueRange](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1206) ([Github](https://github.com/w3ctag/design-reviews/issues/1206)) - @matatk, @lukewarlow

Luke: Seems like a worthwhile API. For some use cases, I wonder if CSS would be an alternative.

### [design-reviews#1208: Other Spec Review: [css-text] `text-fit` property](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1208) ([Github](https://github.com/w3ctag/design-reviews/issues/1208)) - @matatk, @xiaochengh

Matthew: Already looked at this in APA. There are several interesting discussions going in within the CSS WG regarding what the limits of this should be. Combining this with a screen magnifier may also render it too big. Know that they have a similar discussion about the <meta> text-scale feature. APA is working with them. Try to put together a TAG comment as soon as possible. There's a lot of caveats to consider.

### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven

(Skipped.)

### [design-reviews#1190: Incubation: Cryptography usage in Web Standards](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1190) ([Github](https://github.com/w3ctag/design-reviews/issues/1190)) - @toreini, @lolaodelola

Lola: How did we want to post this?

Ehsan: Was wondering as well. Post this as the comment for proponents, but then parts of it as issues in their GitHub repositories, or both.

Lola: Think we should open an issue at their GitHub. This issue was opened proactively by us. Feels better to do it by opening an issue.

Ehsan: Makes sense.

Lola: Ok, then there's some editing to do on the proposed comment, so that we are opening an issue in their repository.

(Ehsan and Lola agree to send in the issue.)

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: It's complicated, working on my comment.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk, @lukewarlow

Matthew: There were some updates. Checking standards positions. Mozilla thinks the problem is worth solving, so basically positive. WebKit position is that they have concerns about the interaction on some platforms. Proponent said that this will be addressed by WPT. Think there is no official position yet, but seems they are going towards that.

Luke: WPTs have been updated. On the feedback comment, would like to push back on the WebDriver part. Tab problem exists across the web platform. Don't think it makes sense to block this specific feature because of this.

Marcos: Will ping internally regarding the WebKit position.

Lola: What's next?

Matthew: If we just wanted to post a comment, we could do it, but I guess we are waiting on the position. We could post the comment, but say: "We would like to know what the positions are." Mozilla's positive, but we would like to wait on WebKit's perspective. If people are happy with the comment, with that part added, we could post it today.

Lola: Suggest to wait until we hear from WebKit. We might say yes even if a vendor position is no, but we should consider their arguments.

Matthew: Could we post comments related to this, unrelated to the position?

(Matthew to coordinate with Luke.)

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Ehsan: Comment is almost ready, hope to have it in the next couple of days.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Lola: Has two thumbs up, so will post it today.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Trying to bring the TAG perspective into a comment. There is a breakout day presentation that is tangentially related. Concerns about how to do this across different form factors. Plan is to draft a comment why we haven't got consensus.

Luke: Haven’t read through the existing discussion. This is the long-press for the touchscreen modality. I worked on this. There might be a separate UI to initiate that instead of a long-press.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Ehsan: Jeffrey and Yves had a discussion about this. Agree with Jeffrey that exfiltration may not be a specific case, but good to have it pointed out. There is a conflict between CSP and Connection Allowlist regarding the reporting. Typing/serialization of violations are different between CSP and Allowlists, may be an issue for the reporting server.

Yves: (Reasoning for inconsistencies.)

Ehsan: Ok, will update the comment.

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh, @lukewarlow



### [design-reviews#1035: CSS Gap Decorations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1035) ([Github](https://github.com/w3ctag/design-reviews/issues/1035)) - @matatk, @xiaochengh



### [design-reviews#1189: Incubation: Web Speech API: On-Device Recognition Quality](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1189) ([Github](https://github.com/w3ctag/design-reviews/issues/1189)) - @marcoscaceres, @matatk, @christianliebel



### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel, @xiaochengh



### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel



### [design-reviews#1204: Incubation: [HTML] html-in-canvas](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1204) ([Github](https://github.com/w3ctag/design-reviews/issues/1204)) - @matatk, @xiaochengh



### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)

## Atlantic Breakout (America / Europe) - [2026-04-24](https://www.timeanddate.com/worldclock/converter.html?iso=20260424T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Lola: *rearranges agenda due to quorum*

### [design-reviews#1209: [wg/ag] Accessibility Guidelines Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1209) ([Github](https://github.com/w3ctag/design-reviews/issues/1209)) - @jyasskin, @matatk, @hlflanagan

Heather: I had a query which I posted in Slack. We were hesitant to take this on becuase we know it will go through the process and raise formal objections so I didn't put any official comments anywhere but I've was wondering about AI and Agentic browsers potetntially expands UA definition, is there a similar thread to pull when talking about AI enabled accessibility tools? Who is responsible for accessibility? e.g. if they're not only reading the screen but also filling out information and doing stuff with the content?

Yves: Also for the conformace rule, it might be linked. Is a site conformant if instead of following WCAG, it relies on AI to make it conformant.

Heather: I'm hearing about website written for AI not for humans. This would be the accessiblity side of that.

Lola: Your question about AI accessibility tools and who is responsible is definitely worth bringing up to the group if it's not in the charter. It may be something we think they should think about. They might say it's not in their remit. I vaguely remember that WCAG 3.0 is going to be thinking about the role of AI. Maybe they are already thinking about it, but they aren't ready to formalize it in the charter. But it is valid to raise regardless. 

### [design-reviews#1197: Incubation: Autofill Event](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1197) ([Github](https://github.com/w3ctag/design-reviews/issues/1197)) - @marcoscaceres, @matatk, @hlflanagan, @christianliebel

Heather: This one has quite a bit of commentary. Marcos and I met on Tuesday and I don't know that we're any closer to a final statement but there's quite a bit to consider. I'm not sure how to take it to next steps without having him around to discuss.

Lola: There may be enough for a draft comment, do you feel like there is?

Heather: I'm unsure.

Lola: *identifies comments from GH which can be pulled into draft comment* Does that sound actionable?

Heather: Yes!

### [explainer-explainer#34: Structure alternatives as: Alternative → Pros → Cons → Reason for rejection.](https://github.com/w3ctag/explainer-explainer/issues/34) - @jyasskin, @matatk

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

### [user-agents#20: Meta: Make progress 12on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

### [explainer-explainer#38: Recommend two structures for organizing alternatives considered.]
(https://github.com/w3ctag/explainer-explainer/pull/38) - @jyasskin, @matatk

### [design-reviews#1187: [wg/das] Devices and Sensors Working Group 2026 Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1187) ([Github](https://github.com/w3ctag/design-reviews/issues/1187)) - @jyasskin, @marcoscaceres, @christianliebel

### [design-reviews#1217: Question: How to reduce apex domain modifications for IDPs using FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1217) ([Github](https://github.com/w3ctag/design-reviews/issues/1217)) - @ylafon

Yves: Need to dig more into discussion before commenting

### [design-reviews#1218: <usermedia> Capability Element  (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1218) ([Github](https://github.com/w3ctag/design-reviews/issues/1218)) - @jugglinmike, @toreini

### [design-reviews#1212: WG Revision: WebTransport](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1212) ([Github](https://github.com/w3ctag/design-reviews/issues/1212)) - @toreini

### [design-reviews#1219: Incubation: Platform-provided behaviors for custom elements](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1219) ([Github](https://github.com/w3ctag/design-reviews/issues/1219)) - @bkardell, @lukewarlow

### [design-reviews#1202: Question: Could the TAG help define "The Web Platform" vs "The Web" or some other useful distinctions?](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1202) ([Github](https://github.com/w3ctag/design-reviews/issues/1202)) - @jyasskin, @ylafon, @bkardell, @hadleybeeman

### [design-reviews#1164: Incubation: PWA (same-site) Origin Migration](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1164) ([Github](https://github.com/w3ctag/design-reviews/issues/1164)) - @ylafon, @hadleybeeman, @christianliebel

### [design-reviews#1214: [wg/math] Math Group Charter](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1214) ([Github](https://github.com/w3ctag/design-reviews/issues/1214)) - @christianliebel


### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
