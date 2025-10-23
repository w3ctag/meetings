# W3C TAG Minutes - Week of 20 Oct 2025

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/10-20-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

## Breakout A (Asia / Australia / West America) - [2025-10-21](https://www.timeanddate.com/worldclock/converter.html?iso=20251021T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Marcos, Xiaocheng, Jeffrey
    
Regrets:
    
Scribe: Martin

### [design-principles#600: Avoid abbreviations for strings and enums](https://github.com/w3ctag/design-principles/pull/600) - @marcoscaceres

Jeffrey: The only remaining question is whether we move it down a little.

Martin: Agree.

Marcos: Got it.

...: Should I add "Intl..." as a counter-example?

Jeffrey: The mistake was to have a namespace at all.  Might not be the best example.

Marcos: Looked for examples, but found none.

Jeffrey: What was the example that caused the PR?

Marcos: Something in DC API.  "cm-..." (the "cm" means nothing).

Jeffrey: We could use that.

Marcos: Didn't want to call someone out.  I'll look for something and use that if I find something or do nothing or use a contrived example.

### [design-principles#590: Add principles for task sources](https://github.com/w3ctag/design-principles/pull/590) - @marcoscaceres

Marcos: Looked at feedback.

Martin: We resolved my comments, which were superficial.

Marcos: Don't remember why I resolved the comment about performance and complexity costs. Ah, I added it above.

Martin: It reads well.

Marcos: Jeffrey, did you want to check?
Jeffrey: Have no opinions here.

Resolution: Merged.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @jyasskin, @ylafon

Marcos: The basic idea here is that a developer has an iframe, but you remove that with intent, but that has consequences.  That won't get into the bfcache.  As opposed to loading images, where the user hits the back button, where the image ends up in the bfcache.  Removing an iframe is not recoverable because reinserting it reloads everything.  The principle is to say that if the developer makes a destructive action, that's intentional.

Jeffrey: If a developer takes an iframe out, the document stops being fully-active.

Marcos: When the iframe is removed, the document just goes.  There's no fully-active state. Where a document is not fully-active is if you have a reference to the object.  You can never put a document back into a fully-active state through editing the page, only through navigation (?)

Xiaocheng: Why?

Marcos: If you have a UI and you reference promises that relate to a thing.  If you mix things across documents, those promises never resolve.  Unless you say that promises abort in certain cases.  You want to tear down UI.

Xiaocheng: I am familiar with these bugs in Blink.  Is this just about technical completeness.

Marcos: Those bugs you fixed in Blink are because this isn't properly specified in specifications.  There is a concept in HTML about this.  There is a promise queue where things are aborted when things get destroyed.  This is trying to get spec authors to think about documents going away.  Back buttons affect UI, for instance.  Consider webauthn/payment request. Even abortcontrollers could do something silly with timeouts (not a good example). 

Jeffrey: There are privacy implications, the document should stop doing stuff if you navigate away.  Background stuff might not be good.

Marcos: geolocation can do that, with iframe documents being navigated away but the page holding references to objects.  Difficulty here is in deciding how many examples to include.

Jeffrey: How much can we merge this with the bfcache section?

Marcos: These are related, but bfcache is a red herring. It's part of browsers, so you can't rely on it.  You should consider it, but you can't rely on it.  Think about it, but these cases are much more important.  This is about scripts doing silly things rather than the browser and user controlling what happens.

Jeffrey: If spec authors have to use the same terms to cover both, they will check for fully-active, we should talk about them in the same section, even if ...

Marcos: We might revise what is in the bfcache, say that it is just for users.  Specs need to consider it, but don't depend on it.  Vs. when the developer that takes an explicit action with implications across all APIs.

Jeffrey: I doesn't matter whether the developer can trigger the action, as long as it can happen.  
Marcos: Caution against what web developers might do.
Jeffrey: It can happen because of user action or developers.
Marcos: Hypothetical: payment sheet open, but user hits back button.  The payment sheet should go away and promises should reject.
Jeffrey: The page could also call back().
Marcos: But if it navigates back, then it destroys itself.  That enters the cleanup situation.
Jeffrey: The distinction is about things becoming non-fully-active vs. destroying the execution context.
Marcos:Bit of a misnomer, but also not.
Jeffrey: Being non-fully-active is what you check at entry; being destroyed is what you check during async operations.
Marcos: If the document becomes non-fully-active because of what the developer did, that has different implications.
Jeffrey: Enough to do another round of updates.
Martin: How do you write code that has asynchronous components with only a check at the entry? If there's constantly the possibility that the things you're touching will go away? Classic async code problem. E.g. assumptions about UX being displayed. Sequence of operations, and between any operations, the UI might disappear.

Marcos: As a result of this, I think HTML needs to add a context observer, which Gecko and WebKit have. WebKit has an observer for Script Execution Context being destroyed.

Martin: And scripts that depend on something continuing to exist, stop executing.

Marcos: Yes, cleanup and then stop executing.

Xiaocheng: We need to expose the context destroyed event to APIs.

Marcos: Yes.  There should be something in the infra spec. If the execution context is destroyed, do this: kill promises, abort errors, etc...

Jeffrey: AbortError is probably sufficient for the userland piece.  Spec tools might be needed to manage that.

Marcos: Might need to see how many specs have missed this.

Jeffrey: all of them {?}

...: we need a round of updates for this PR, but then there might be something to do in HTML (maybe WebIDL)




### [design-principles#584: Replace asking for users for consent with designing for user intent](https://github.com/w3ctag/design-principles/pull/584) - @mharbach, @marcoscaceres, @hober

Jeffrey: Just waiting on Marcos.  ... and to resolve conflicts.

Marcos: Lots of changes.

... worried that we're adding exceptional capabilities with "powerful features".

Jeffrey: Maybe this should talk about ["powerful features"](https://www.w3.org/TR/permissions/#powerful-features).

Marcos: Does that have the same semantics.  A bit of a value-judgment involved.

Martin: Always a value-judgment which is why browsers have discretion in their UX for this.

Jeffrey: PF is about consent.  This is about something else, which might not involve consent.  File input is an exceptional capability but doesn't involve consent.

Marcos: Should we `<dfn>` exceptional capability and note that opinions might vary.

Jeffrey: Maybe we can avoid the definition and look for other words, like "potentially|maybe unsafe".

Resolution: Marcos to make a few comments. 

### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Marcos: This seemed close.

Jeffrey: just nits from me, I think; no big changes

Marcos: The indicators was ...

Jeffrey: Like the camera active light or icon.

Jeffrey: This doesn't have to be in a specification, it could be in other sources (academic papers).

Jeffrey: also not clear about what a preview is in this context

...

Marcos: WebEx will activate the camera when you aren't on a call.  That seems to suggest that you are on a call, when you aren't.

### [design-reviews-private-brainstorming#211: WebMCP Review](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/211) - @xiaochengh

Xiaocheng: Lots of disagreement.

Jeffrey: We agree about the nature of the disagreement.

Martin: This might make things worse, but I think the Prompt API solves the problems that WebMCP claims to address.

Xiaocheng: Prompt API is initiated by the web page, and simply connects to a non-specific external agent. Not possible for a scenario where you have an agent and want it to work with 2 different pages.

Martin: Oh, 2 pages!

Xiaocheng: That's typical for MCP, where a client app has an agent, and you want it to work with different services.

Martin: Agent hosted in one context, making calls into another context.

Xiaocheng: Want the same agent to be able to initiate a number of connections to many MCP services.

Martin: If you look at Prompt API, if you're in the context where you're running an arbitrary agent, you can give it tools taht can postmessage or whatever. Or could do a fetch to an MCP server. This is all about glue. How much does the browser do vs the website? Different frames or windows ... model needs to poke those things.

Martin: So WebMCP is more Web Intents: publishing capability, and arbitrary clients can connect.

Marcos: Prompt API defines inputs through english prose, which is kinda nuts. This one is more static integration into OS. Considerations about whether it'll work with the intent system across operating systems. May or may not use Javascript. Do we want to get into the whole situation of booting a Service Worker.

Jeffrey: They are just testing a bunch of ideas,  We should encourage experiments.  All scary.  Bunch of open research problems.  People outside this community are exploring this aggressively.  Important that we explore it.
Marcos: This plays into the prompt API.  Are the models the same.  

Martin: I realized that MCP, the one thing it has contributed is picking a winner. Picked JSON Schema as its description language. There were thousands available, and it picked on. Effectively said JSON Schema will win. That's interesting. Shoud link to [Cloudflare's alternative](https://blog.cloudflare.com/code-mode/). That's effectively what we're saying we can't do right now, but they demonstrated they can.

Jeffrey: Anthropic isn't the biggest player, but they picked a design to converge on.

Xiaocheng: I'm also concerned about that, since if we introduce WebMCP to be similar to MCP, we've picked MCP as the winner.

Jeffrey: As experiments proceed, we might discover what options are best.

Martin: Schema question isn't as important as the question of the basic capabilities. We have websites that are looking to expose capabilities. How do they enumerate and publish capabilities? How do they authenticate themselves and others so capabilities are exposed to the right clients. Other web pages, or things sitting on same host outside the browser.

Jeffrey: Think it's things on the host.

... prompt injection doesn't have a defense.  That is one thing this experiment is supposed to deal with.

Xiaocheng: Lots of time on this topic, but we haven't been able to send a message.  What can we send?

Jeffrey: You want lower-level, I'm not sure about what that might look like.

Xiaocheng: Can we say that we publish the range of opinions on the topic.

Jeffrey: Good answer.

Xiaocheng: Will publish the last comment.  Maybe add something on security/authentication and ask them to explore that.

Jeffrey: Good plan.  Separately, you should look at the [ChatGPT apps SDK](https://developers.openai.com/apps-sdk).  A little scary.  A new platform that might be trying to replace the web.  Influential player.  Reminds me of AMP

... They are trying to build a super-app in ChatGPT, embedding webpages, but not as webpages, but MCP responses.  With some extra APIs to do extra things.  Opinions vary about how to think of it.  iPhone app store, AMP, or super-apps are the best analogies.

Xiaocheng: Information silo?

Jeffrey: Yes, but it's evolving.  They want it to be open.  In theory, many chatbots would interact with it.  There are no links into these things.  I'm worried about having a closed ecosystem and the loss of linking.

Xiaocheng: Closed ecosystems are attractive.  The excuse would be that everything is generated by an LLM, so you can't index or reproduce.


### [design-reviews#1092: Web Authentication Immediate Mediation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1092) ([Github](https://github.com/w3ctag/design-reviews/issues/1092)) - @martinthomson, @jyasskin, @marcoscaceres, @toreini
### [design-reviews#1093: Prompt API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1093) ([Github](https://github.com/w3ctag/design-reviews/issues/1093)) - @martinthomson, @jyasskin, @marcoscaceres
### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1140) ([Github](https://github.com/w3ctag/design-reviews/issues/1140)) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola
### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

## Breakout B (America / Europe) - [2025-10-22](https://www.timeanddate.com/worldclock/converter.html?iso=20251022T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Jeffrey, Yves, Serena
    
Regrets: Matthew, Ehsan, Christian
    
Scribe: Yves

Impact TF: working with people from the Team , working on Objective and Communication. Some Community outreach will likely happen at TPAC. There will be cross-over with Technical Strategy and other related TFs.

### [design-reviews#1138: [wg/webextensions] Web Extensions Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1138) ([Github](https://github.com/w3ctag/design-reviews/issues/1138)) - @csarven, @matatk, @toreini, @christianliebel
### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk
### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola
### [user-agents#28: Add loyalty guidance for facilitating users switching UAs](https://github.com/w3ctag/user-agents/pull/28) - @csarven
### [design-principles#588: Rewrite the "removing features" section, incorporating "Support Existing Content" from the HTTP Design Principles](https://github.com/w3ctag/design-principles/pull/588) - @jyasskin, @csarven, @lolaodelola
### [societal-impact-questionnaire#24: Misuse example](https://github.com/w3ctag/societal-impact-questionnaire/pull/24) - @lolaodelola, @csarven, @christianliebel
### [societal-impact-questionnaire#26: Exclusion Example](https://github.com/w3ctag/societal-impact-questionnaire/pull/26) - @lolaodelola, @csarven, @jyasskin
### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin, @lolaodelola, @csarven

Design Reviews:

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github]
(https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin

Jeffrey: Did a review and drafted some comments, need someone to review those.

Lola: many comments are clarifications

Yves will review over the next day

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

### TAG "Job Description"

Working with the TAG: https://tag.w3.org/workmode/

Old charter: https://www.w3.org/2004/10/27-tag-charter.html
> Participant Qualifications
> 
> W3C Members are encouraged to nominate individuals who:
> * Demonstrate depth of experience in broad areas of Web development; deep understanding of the architectural issues surrounding the Web and related technologies.
> * Are available to spend approximately 25% percent of their time writing and resolving issues.
> * Demonstrate the ability to resolve disputed technical issues and to build consensus.
> * Demonstrate the ability to put the common good above proprietary considerations. TAG participants must be willing, when circumstances require, to recuse themselves from decisions where proprietary interests might interfere with their judgment.
>
> Other key qualifications include experience with W3C process and Working Groups, experience in other related organizations, experience implementing Web technologies, and good writing skills.

Jeffrey: 2 separate sub-roles: We should add something about technical understanding and ability to dive into it, skill in reading specs outside of niche. We also work on policy, we need folks who can drive policy and recruit ppl to work

Yves: not policy, higher level docs

Lola: Worried that we need to avoid scaring people away by insisting on too much technical expertise.

Jeffrey: Want to be clear that the second sub-role _doesn't_ need the wide+deep technical understanding. Driving consensus and adoption requires confidence, we should emphasise need for confidence.

Yves: Associates can also help fill in technical gaps if necessary. In Paris we discussed producing  more higher level docs, technical requirements matter less here.

```
Participant Qualifications
W3C Members are encouraged to nominate individuals who:
* Demonstrate expertise in at least one area of the W3C's work.
* Note: Individuals are notoriously bad at identifying their own expertise, if you are nominated, trust that you are qualified for the role.
* Be eager to learn the other parts of the W3C's work.
* Are available to spend approximately 8 hours per week of their time writing and resolving issues.
* Are available to meet at times that work for participants around the world. We sometimes meet as early as 6am and end as late as midnight in any given timezone.
* Demonstrate the ability to resolve disputed technical issues and to build consensus.
 * Demonstrate the ability to put the common good above proprietary considerations. TAG participants must be willing, when circumstances require, to recuse themselves from decisions where proprietary interests might interfere with their judgment.

Be qualified for *one* of two sub-roles:

1) Design reviewer: Members should have a detailed understanding of a wide (though not complete) swath of work that the W3C does. Members should be able to read a specification or explainer in an area they're not directly familiar with, develop an understanding of how that area relates to the rest of the W3C's work, and produce useful comments.
2) Higher-level document author/initiative driver: Members should have the confidence and energy to drive the TAG to produce a document in some area of interest.

> Other key qualifications include experience with W3C process and Working Groups, experience in other related organizations, experience implementing Web technologies, and good writing skills.

What to Expect on the TAG:
* TAG participants will be members of councils
* Conduct design reviews
* Contribute to TAG documents e.g. Findings, Notes, Statements
* Meet F2F twice a year (Funding for Invited Experts is usually available for travel and accomodation)
* Participation in public events e.g. Meet the TAG events, Developer Meetups
```

## Breakout C (Europe / Asia / Australia) - [2025-10-23](https://www.timeanddate.com/worldclock/converter.html?iso=20251023T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Ehsan, Matthew, Marcos, Lola, Martin, Yves, Sarven
    
Regrets: Xiaocheng
    
Scribe: Matthew

### [prevent-credential-abuse#52: Add discrimination based on certain fields under Exclusion](https://github.com/w3ctag/prevent-credential-abuse/pull/52) - @csarven, @martinthomson

It's merged.

Martin: does this match your expectations Sarven?

Sarven: Wasn't clear to me about whether we were looking at specific cases or general examples. Seemed to change, but happy to defer to you as editor.

Martin: Appreciated; aiming to generalise.

### [societal-impact-questionnaire#25: Make Tristan former editor](https://github.com/w3ctag/societal-impact-questionnaire/pull/25) - @lolaodelola, @hadleybeeman

Martin: 👍

### [design-principles#585: Clarify when details should go on events vs targets](https://github.com/w3ctag/design-principles/pull/585) - @jakearchibald, @marcoscaceres

Martin: Merged 🐿️

Design Reviews:

### [design-reviews#1147: WG New Spec: FedCMâ€”Support Structured JSON Responses from IdPs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1147) ([Github](https://github.com/w3ctag/design-reviews/issues/1147)) - @lolaodelola

Lola: Jeffrey's OK'd my proposed comment - any other thoughts? It's a minor update to support structured datatypes as well as strings. Suggestion made that we should decline to review; that's where my comment's leaning.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: This is really neat.  Like so many things I've seen in previous career would be fixed with this.  That was the general consensus in APA.  We discussed yesterday and we have some questions.  Or some things that could be mentioned, possibly as future work.  I might put them in the thread.  I will probably post directly.  I plan to do that today.

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Lola: +1 to your comment Ehsan

Ehsan: In general I'm in favor; have a couple of qustions about social engineering attacks that apply to the way they're doing it (in proposed comment).

Lola: You can just post - if any of us think of more questions we can add them.

### [design-reviews#1135: Incubation: Inline Integrity](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1135) ([Github](https://github.com/w3ctag/design-reviews/issues/1135)) - @toreini

Ehsan: That one is closed and resolved.

### [design-reviews#1146: Incubation: Proofreader API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1146) ([Github](https://github.com/w3ctag/design-reviews/issues/1146)) - @matatk, @toreini, @christianliebel

Christian is not here...

Matthew: I need a bit more time.

Ehsan: Also still reading it.  Will post it hopefully next week.

### [design-reviews#1139: WG Revision: Dubbing and Audio description Profiles of TTML2 (for 2nd CRS)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1139) ([Github](https://github.com/w3ctag/design-reviews/issues/1139)) - @matatk

Matthew: was I supposed to close this?

Lola: There was another one.. You were supposed to close this with the comment you proposed.

Posted. Closed.

### [design-reviews#1119: Digital Credentials API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1119) ([Github](https://github.com/w3ctag/design-reviews/issues/1119)) - @martinthomson, @matatk, @toreini, @lolaodelola

Lola: We needed Martin to discuss this further (post workshop).

Martin: Workshop may not have significant impact on this, but that's OK.

Marcos: We landed the coordinator part, but not the algorithms yet (still drafting). It was suggested we post our comments (high-level) as questions. One thing I've learned is there's going to be a free-as-in-beer version of the mDoc spec, which is intersting. So there's potentially a path to having a complete specification at no cost.

Lola: So OK to post our questions, whilst we wait for algorithms part of the spec?

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1128) ([Github](https://github.com/w3ctag/design-reviews/issues/1128)) - @toreini

Ehsan: Got feedback from Jeffrey; asked for a revision of comment; this was done, so waiting for Jeffrey's view on it.

### [design-reviews#1041: Signature-Based Integrity.](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1041) ([Github](https://github.com/w3ctag/design-reviews/issues/1041)) - @martinthomson, @csarven

Martin: Waiting for some Mozilla feedback on this. What I'd say is that the integrity you get from this one is pretty weak if you're allowed to swap resources. There's nothign that binds the signature to the resource in the design. So you can say 'I accept this particular resource' or, if attacker is CDN, they could deliver a completely different resource as long as they share the same signing key.

...The fix for that is to say that we put the path of the resource under the signature, and then you have to do some extra stuff if there are redirects involved - but then you have the binding. If you have hashes, it doesn't matter where the content comes from, but if you have a signature, this problem applies. Seems there's an optional allowance for server signing extra properties, like the URL, but it's optional, and client may not check.

Sarven: Sounds good - there needs to be provenance.

Martin: The existing SRI is hashes, whcih is content identity, which is very strong. If you get a hash, then it has to be this content (modulo the chance that someone creates content that hashes to the same thing - astronomically unlikely unless they break the hashing algorithm). With a signature, there's a set of things that could've been signed with the same key, and they're intergchangeable. E.g. you could sign an updated verison of a script.

Sarven: Is there a reference to the source of the content, i.e. a URL. Even if you have that though, it doesn't necessarily address this fully.

Martin: Having the reference allows the client to check it's code from the same provider, but it still allows for different content to be served. Concerned about this one.

Ehsan: Can they simply hmac for it? Makes the provenance less complicated?

Martin: You can't use hmac because the key has to be distributed to thousands of clients.

Ehsan: ACK, of course.

Sarven: Concern about which instance of the content is being signed.

Lola: Suggest you post your question Martin, and look out for Mozilla's position.

## *Stuff from Breakout B...*

### [design-reviews#1138: [wg/webextensions] Web Extensions Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1138) ([Github](https://github.com/w3ctag/design-reviews/issues/1138)) - @csarven, @matatk, @toreini, @christianliebel

Sarven: We reviewed; sent feedback; not sure if 'out of scope' section was originally included in the PR wehre they made changes to the charter: https://github.com/w3c/charter-drafts/pull/711#discussion_r2434955131

... I made a suggestion on the PR that the packaging format and signing mechanism for extensions should not be out of scope. In my review, I said these seem like things that should be in scope - or at least not excluded - becuase standardising this would allow decentralized distribution of extensions. This seems like a laudable goal. There was some pushback on this from the group. I think browsers prefer to package extensions in their own way, for distribution via their own stores.

Ehsan: If you're a good actor, signing it is fine. If you're a malicious actor, and sign it, wouldn't it make the decentralized distribution of extensions easier? As there's no way to verify the reputation of the distributor. Might signing legitimize distribution of malicious code?

Sarven: Two things: (1) signing, and (2) packaging format. Anyone can self-sign and distribute right now. We could move that aside. Main thing is about format. Is there a reason why these formats need to be unique to the browser?

Lola: Struggling to see a reaosn why the format woudl/should be unique to the browser.

Martin: It's only specific to the browser to the extent that it has things that the extensions model demands (e.g. manifest, permissions) - it's a zip file otherwise.

Marcos: +1 to Martin

Sarven: E.g. you can't take an .xpi (Mozilla) and import it into Chrome. I should be able to import any extension into any browser. Trying to understand the pushback. There should be interop - better for consumers, implementers, publishers.

Martin: It's a shame that they specify almost everything you need, other than the very last thing that pulls it all together. This is useful input to the folks in this area, but it doesn't have to be in the charter.

Sarven: But they put it out of scope.

Martin: Agree it should not be explicitly put out of scope.

Sarven: Re misuse: to be able to install an extension you need to go to the store. To put it in the store, you need to sign in. So there's tracking. It then knows which devices are using extensions. Blatant centralization.

Martin: It is true; the folks doing it are doing so because they believe it's in the interests of users. There have been abusive extensions that do things like cryptojacking or other nasty things, as they have access to cookies and passwords. Browsers want to have the ability to yank extensions. Without that control system, people would self-sign. I understand it's a centralization problem, but it exists for a good reason, and that's hard to resolve. Firefox does allow sideloading, so it's not necessarily true that the extension store is the only place you can get them.

Sarven: Majority of users however aren't going to do temporary sideloading. Not concerned about stores having additional requirements on who can put things into their stores, or additional security measures. But an independent developer would have to publish multiple packages. Reminds me of 'this web page works best under IE'

Martin: We're slowly getting there.

Marcos: If you did have self-sovereign model, you'd have to strip out the powerful APIs. They see into everything and can read into your cookies and do all the things. They're literally acting as a UA.

Martin: If you stripped the capabilities out of the extensions, they'd be called web sites.

Lola: Sounds like we do want to consider asking them to add the packaging format in scope.

Martin: or at least not making it explicitly out of scope

Lola: I think they won't do it, if it's not mentioned. If it's in scope, maybe they can be held to some account.

Sarven: Agree it must not be listed in 'out of scope'. Peferably it would be listed as 'in scope'. I'd like to know if/what we should get back to them with here and wehether I or others should join one of their calls. I think they have one today.

Marcos: Packaging must've been part of the initial discussion going back many years. There must be good reasons why they left it out. They should state it, as it's such a glaring hole.

Lola: There is some discussion about this (in the PR thread linked above) - reasons given (paraphrasing the thread) around the prevelance of stores (re the CG charter), and lack of implementer interest (or actual opposition).

Sarven: So we should ask them to be clear on the reasons why these things were made 'out of scope'

Lola: May be worth doign that on the PR, or joining a discussion of theirs.

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

(mentioend about closing this in slack; will close)

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola
### [user-agents#28: Add loyalty guidance for facilitating users switching UAs](https://github.com/w3ctag/user-agents/pull/28) - @csarven
### [design-principles#588: Rewrite the "removing features" section, incorporating "Support Existing Content" from the HTTP Design Principles](https://github.com/w3ctag/design-principles/pull/588) - @jyasskin, @csarven, @lolaodelola

### [societal-impact-questionnaire#24: Misuse example](https://github.com/w3ctag/societal-impact-questionnaire/pull/24) - @lolaodelola, @csarven, @christianliebel

Lola: See also: https://github.com/w3ctag/societal-impact-questionnaire/issues/21#issuecomment-3435840151

Sarven: Trying to clarify in-spec vs out-of-spec. Misuse of gathered info. The particular point here is to think through the risks and mitigations. Some mitigations could be handled by implementations, some not.

Lola: Struggling to think of mitigations that could be handled by implementation. E.g. spec used appropriately, but info gathered, and then later that info being used to undesirable things. Not sure how the spec could mitigate against that. E.g. service provider doing things user doesn't want with their data - can close and delete account. But a third party basing e.g. news stories on info found on service provider site - not sure how to mitigate.

Sarven: Cookies are a good example - even when implemented per spec, they can be used to surveil users. Another example, if you use speech to text, you have a voiceprint for the user. What else are you going to do with that? Not concerned about in-spec behaviors so much - we have good ways to deal with these to minimize the harm. There are things that go beyond the specs, and the point of the questionnaire is to think them through.

Lola: I think cookies is a good example, but not to that point - as you're intentionally using 3pc to do something wrong (track and surveil users). The reason we're having such difficulty in replacing 3pc is that they made that tracking easy. 3pc is an example of misuse - in-spec misuses, even. Jeffrey mentioned this before, but in the spec they also mentioned that it could be used for such thigns, and warned against doing so, but it still is. I agree this is something spec authors should think about. Struggling to see that not being addressed in the text that already exists.

We are out of time so should continue the conversation in the issue or next meeting.

## Plenary Session - [2025-10-22](https://www.timeanddate.com/worldclock/converter.html?iso=20251022T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Martin, Christian, Matthew, Jeffrey, Max, Yves
    
Regrets: Xiaocheng
    
Scribe: Christian

### Consider publishing https://github.com/w3ctag/prevent-credential-abuse/

Jeffrey: What do we need to do before publishing?

Martin: PR is present, sitting open for three weeks.
https://github.com/w3ctag/prevent-credential-abuse/issues/40
I don’t know what specific discussion you meant there, Jeffrey.

Jeffrey: (connection issues)

Martin: I think it’s a lot of text, and I think it’s distracting. Don’t quite know how to compress that into something more direct.
https://github.com/w3ctag/prevent-credential-abuse/pull/52

Want feedback from at least Sarven.

Matthew: … Any reason why we can’t put both in?

Martin: Think it’s mostly the same meaning. Sarven’s concern was that certain passports don’t contain all required info (e.g., birthdate).

Matthew: "Absence of information can’t be withheld" isn’t clear to me. That’s the only thing.

Martin: I don’t like Sarven‘s example very much in support of that particular message.

Lola: If you are unhappy with the example in general, maybe it’s worth that you and Sarven figure out another example that works for both of you?

Martin: Think Sarven is quite attached to this, which I don’t quite understand.

Lola: Let Sarven review this. I remember we talked about that example during the F2F.

Jeffrey: On issue #40, I don’t mean to block publication on this. If folks don’t think this needs to go in there, that’s okay with me.

Martin: It’s one of those diminishing returns cases for me.
Only other thing I’m aware of is the text on age verification. Think the answer is that we still don’t know the answer, even after the workshop. There’s a report forthcoming, and I think the resolution is that we need more discussion between stakeholders. I might need to tweak the language there.

Yves: When is the report scheduled?

Martin: It’s not scheduled right now, still in discussion. Intent was to get something to circulate between the people that attended within the next month or two.

Yves: Will be easy to update as soon as we get the link?

Martin: Yes. We might update the finding based on what we put out. Might publish something from the W3C side (e.g., a note) at the same time. Working it out.

Jeffrey: Everything for this topic?

Martin: Yes.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Jeffrey: We didn’t manage to discuss this in A. Worried about making an actual decision on this. Want the proponents to talk to Marcos. Posted comments in the private brainstorming (https://github.com/w3ctag/design-reviews-private-brainstorming/issues/118#issuecomment-3413063870). Basic thought is that this is not implementable on touchscreens or VR systems. The proponents describe how to implement it on touchscreens, and Apple shows to implement it on VR. interesttarget cannot quite do on VR what Apple does. It’s worth to investigate this further.

Matthew: Catching up with this. Question on the previous part of the discussion. Wondering if the reason why they are concerned about it is to do with privacy, because they don’t know websites to know where people are looking.

Jeffrey: We can’t fire the interest event on gaze, because that would tell the website where people are looking. Apple has a super elaborate system that allows the app the define what happens in the event, without telling the app where the user is looking. If Apple were interested, they were the best people to design this. In its absence, the basic approach seems fine.

Matthew: Other thing I was wondering, we had a discussion with the proponents, and Marco was in there, and during or after the discussion, it seemed that we were all on the same page, they would override certain things, and that might give Apple the neccessary reassurance … Wondering if someone else remembered that.

Lola: Don’t know much about this, have a question regarding gaze. That relay pattern works well on visionOS, one of the reasons being that Apple wants to let consumers know that they care about privacy. What happens with companies that try to step into similar spaces but don’t have the same priorities? Would this feature be in danger of being abused?

Jeffrey: This must be addressed in the spec. "It’s not appropriate to fire this event when the user looks at an element." You need some layer of built-in privacy, the spec leaves it unspecified for now. Gaze should be more private.
… Found the discussion where Marcos said he wouldn’t object to the satisfied response (https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/07-28-minutes.md#design-reviews1058-the-interesttarget-attribute---matatk-xiaochengh). The other part is, we can make decisions without consensus. I’m not going to insist on that, but people should consider that.

Martin: Don’t we have ambivalent? I would rather signal that than insisting on coming to a solution.

Lola: I agree.

Jeffrey: Think TAG should tell browser engines if people make mistakes, even by not shipping something. Think "no consensus" may be more appropriate then.

Martin: Not really sure if it is a mistake, more a missed opportunity. That happens on the web, and doesn’t make it bad necessarily.

Jeffrey: Nothing to do now, let’s talk to Marcos and bring it to the next plenary.

### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1140) ([Github](https://github.com/w3ctag/design-reviews/issues/1140)) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Jeffrey: Marcos posted concerns to the issue that there would be discussions at TPAC, maybe we should come back to this after TPAC.

### [design-reviews#1093: Prompt API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1093) ([Github](https://github.com/w3ctag/design-reviews/issues/1093)) - @martinthomson, @jyasskin, @marcoscaceres

Jeffrey: Another place where Marcos and I are disagreeing. Copied Marcos’s response to a Google Doc and left a bunch of comments to it. (https://docs.google.com/document/d/1gqgMj_gQdk23_AaIYRlQ1nIYYQgOdVzvsDhJjJpTfMQ/edit?tab=t.0)

Martin: Had a look, but it’s a vast amount of text.

Jeffrey: Made a suggestion of what we want to write. There are pieces where Marcos is overly critical, or where I am okay with it. Christian offered to write a comment, maybe that would be better.

Christian: I can do this. I'll also look at the comments document. I'll do it after this meeting. Would be good to release the comment soonish, because it's been a while. I'll read through the comments and say if I'm ok with it, or if I'll write something new. I agree it sounded overly critical, and lots of problems have been resolved. Important to have a balanced response.

Jeffrey: Marcos is right that it doesn’t have to be balanced, we can take a strong opinion, but I don’t agree with it.

Martin: Think it would be good if you come down to a stack ranking of the feedback: What is the top 3 concerns that you have. A bunch of things come around the use of LLMs in browsers. I would like to see more normalization with this and the work on WebMCP. Seems like this is consistent with what MCP does, but it doesn’t explicitly say that. The description of tools, etc. If you look at the spec, there’s nothing there. We should say: Be a little bit more … about this architecturally. Don’t agree with Marcos’s response regarding the delivery of models.

Jeffrey: Think Marcos is right that they should be more clear around the cloud models. The API is build around local models.

Martin: That is confusing, and this could be a high-level point you could make.

Jeffrey: Next steps, Christian will read this and potentially write another comment, and we will check back with Marcos what the top points are.

### AC presentation - lola

Lola: Deadline is today, what should we tell the AC, what we should brag about? Was going to put our F2Fs there, and the things we discussed. We have made considerable progress on two documents, but we haven’t published them yet. Should I include documents that are WIP? Thinking prevents credential abuse, thinking user agents. Should we include the age verification workshop?

Martin: It’s a TAG workshop.

Martin (chat): And Hadley helped on the program committee for the WS.

Matthew: Agree with the workshop, developer meetups in particular at the F2F, we are doing this again. Some findings that we’ve published. Breakdown of the design reviews we did, number of them. Maybe controversial, but we could say something about trends. Intake process, accessibility screener, TAG bot.

Jeffrey (chat): https://tag-github-bot.w3.org/metrics ?, associates, election

Matthew: And I think that’s seven slides.

Jeffrey: Wanted to +1 user agents, explainer explainer, credential abuse

Lola: Anything specific about the election we want to mention?

Jeffrey: Think it’s just nominate people, the kinds of skills people need, people how know how to drive a project, have opinions about the web architecture. We could point ot the "job description" we haven’t written yet.

Yves: We need to work on that job description. Specify how much work it is. Definitely mention the WIP things. People really want the credential finding to be out.

Lola: That’s enough! Thank you.

### TPAC Planning - https://github.com/matatk/tpac-scheduling-helper

Jeffrey: Matthew put together the scheduling helper. We want to identify sessions to attend together. We have a room for 1.5 hrs at the beginning of TPAC, but we should put together most of the pleaning ahead of time. Let’s start thinking about what we should look at.
… Question: Team is scheduling the breakouts. Some seem duplicate, some just seem to identify new work. Should it be a TAG job to merge similar breakouts?

Martin: Can we do this, given the remaining time?

Jeffrey: Think there is enough time, should be at least 2 weeks.

Lola: Also, it seems like scheduling similar workshops (e.g., on accessibility) at the same time is a problem, because people may want to go to both. Maybe conflict of interest, because I have a breakout on my own.

Matthew: Good news, breakouts won’t clash with group meetings. There are some outside the Wednesday slot, but only when groups don’t meet.
… Is it worth for us to do some coordination on this? Lola and I could coordinate the accessibility breakouts.

Jeffrey: Seems Matthew, Lola and I are interested in this, we could reach out to the team.

Lola: Are there similar collisions?

Jeffrey: I think we don’t know, but they would certainly tell us.

### [Incubation: FedCM: Support showing third-party iframe origins in the UI #1136](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136)

Lola: Issue by Ehsan that is open and should be closed. It’s about the UI, different URLs.

Matthew: The IFrame in FedCM.

Lola: Matthew, please check this back with Ehsan.

Matthew: I’ll pass it on.

### Breakout Rollup

Nothing to discuss.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

Jeffrey: Who wants to do them, should we decline some? It’s View Transitions and three RDF 1.2 specs.

Lola: You can assing me to view transitions.

Jeffrey: Are they planning to publish these or is this the first working draft?

Yves: Looks like it’s publishing in CR

Martin: Didn’t they just charter?

Jeffrey: They did, but they also incubated a lot.

Yves: First public working draft is from 2023, so it’s likely for publication as CR.

Jeffrey: We could decline it, but we should check with Sarven.

Martin: Not inclined to spend any time on this.

Jeffrey: Think the changes are not huge. Would like to avoid reviewing this, let’s check with Sarven.
