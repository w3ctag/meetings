# W3C TAG Minutes - Week of 6 Oct 2025

## Breakout A (Asia / Australia / West America) - [2025-10-07](https://www.timeanddate.com/worldclock/converter.html?iso=20251007T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Dan, Marcos, Serena
    
Regrets: Max, Xiaocheng
    
Scribe: Jeffrey

<!-- Agenda+ -->

<!-- PRs -->

### [design-principles#600: Avoid abbreviations for strings and enums](https://github.com/w3ctag/design-principles/pull/600) - @marcoscaceres

Jeffrey: Do enums need this specifically?

Marcos: Might be useful to be redundant. CSS ones say to avoid abbreviations. Can put it in the naming section.

Jeffrey: Send the more general one.

Marcos: In https://w3ctag.github.io/design-principles/#naming-common-words

Dan: Yes.

### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres

Jeffrey: I left a bunch of comments, too recently for you to have done anything about them.

Marcos: Re "worried that "mediate" is less clear than "explain".", it is actually a mediation. You present UI to explain, but the UA is acting as the mediator.

Jeffrey: If you still like the word, I don't object.

Marcos: For example, in PaymentRequest, it does a true mediation, where the user does something in the UI, and it gets sent to JS, and the page might not accept the value. Permissions also just ask.

Marcos: For links to "text, permission prompts, indicators, previews, placement and emphasis, and other cues.", these can't be links to specs since we don't specify UI like this. Inline the examples? Screenshots?

Jeffrey: That's probably clearest, with alt text.

Serena: Is this a new section?

Jeffrey: Replacing an existing section. The issue asked whether "honesty" was the right word.

Serena: Maybe "transparency"? "of state, behavior"?

Marcos: I like honesty because it's serving on behalf of the user. It's not just being transparent. It's not neutral.

Jeffrey: I want to use "forthrightness", but nobody will get the point if we use that.

Marcos: Other comments look reasonable.


### [design-principles#584: Replace asking for users for consent with designing for user intent](https://github.com/w3ctag/design-principles/pull/584) - @martinthomson

Marcos: I believe both user intent and consent have a role. I'd advocate strongly for intent, but historically we've asked for consent, and that's worked reasonably well for a long time.

Jeffrey: [1.4.1](https://pr-preview.s3.amazonaws.com/mharbach/design-principles/pull/584.html#user-decisions) tries to explain "how" to ask for consent, and to capture the content of the old section, but you should definitely review this.

Marcos: I'll review this.

### [design-principles#585: Clarify when details should go on events vs targets](https://github.com/w3ctag/design-principles/pull/585) - @marthinthomson, @xiaochengh

Marcos: I want to review this too.

### [design-principles#594: Clean up link-defaults.](https://github.com/w3ctag/design-principles/pull/594) - @jyasskin

Marcos: Approved

Jeffrey: Merged.

### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin

### [design-principles#588: Rewrite the "removing features" section, incorporating "Support Existing Content" from the HTTP Design Principles](https://github.com/w3ctag/design-principles/pull/588) - @jyasskin

Marcos: I'll look again. 

Jeffrey: I'll also move this to B.




<!-- Design Reviews -->

### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Jeffrey: Think the explainer should discuss the choice of local or remote in more detail.

Marcos: Think it shouldn't discuss it at all. So many attacks. Anne was unhappy that it exposed the download progress. It affects the whole browser. And language packs are a fingerprinting vector. Major design flaw with the API is that it goes into memory management. Presumptions about sessions that might be large. Could be true, but not for the developerr to decide or manage the memory. No indication in the session about the available size. Want it to move away from talking about that at all.

Jeffrey: All models have a token limit?

Marcos: Model quota is fine, but local vs remote shouldn't matter. Results should be transparent. Developer shouldn't need to manage things they don't know. Even if it's downloaded, they shouldn't be able to know that. If I'm roaming, the browser might ask, but the website shouldn't be able to monitor that.

Jeffrey: We had a discussion around Web Speech, where developers wanted to ensure the data stayed local. 

Marcos: That's a different problem. EULA governing the browser would cover that. The website would need to avoid using the API at all, since it can't govern the data once it goes into the platform. Another example: geolocation: Firefox uses Skyhook, and that's part of the bargain when you download Firefox. Your data goes to a company, and you can't do anything about it.

Jeffrey: Your point is that the API should be transparent between cloud and local process. Don't know if the browser is willing to pay for cloud processing. AI models are more expensive than location services.

Marcos: Might not be true forever. Quantum comuting might make this very cheap.

Serena: Would be good to plan for what we know is real now.

Marcos: Some browser companies have a relationship with good model companies. What about smaller browsers?

Jeffrey: The proponents argued that there are good-enough free models. Don't think that's in the explainer, and they should substantiate it.

Marcos: Model quality matters. 

Jeffrey: Maybe we ask the proponents to substantiate that free models are good enough that sites don't need to UA-sniff.

Marcos: Users are the ones who need to decide if it's good enough.

Jeffrey: Users could plug in their own models.

Marcos: Developer tests with Chrome. Opera has a low-quality model. Developer doesn't test and doesn't want to run on the server. Real chance to exclude people based on their browser choice. Web developers should care about users, but often they don't.

Serena: Summarizing: saying that because this proposal means that each browser chooses their own model. Because the cost of creating a good model differs so much between mid-range and good. Cost might be prohibitive, and user experience could be drastically different between browsers. And that's bad for users and developers because they can't guarantee quality.

Jeffrey: I question the quality of even the best models, but users can pick their browsers.

Marcos: Some governments will only design for Chrome and Firefox. User doesn't have choice.

Jeffrey: If it's the site picking the browser, presumably the site has tested that browser's model. So users at least won't be hurt by having to use a worse model than the site has tested.

Marcos: We should require that all browsers have a certain quality, and no other API has such varying performance.

Serena: I wonder how we even define the quality bar. Output is so non-deterministic.

Marcos: "Reasonable person".

Serena: What if 10% of the time it's not good enough, but 90% of the time it is. Don't know how someone proposing a model, would they just cherry-pick? How does one prove that the open-source model will be good enough?

Marcos: That's the debate.

Dan: Changing quickly. People's expectation of a "good" model is evolving rapidly.

Jeffrey: I'm wondering how we give actionable feedback. If we just say "don't do this", we'll get ignored. If we say "do this in this other way".

Marcos: We can say "consider this".

Jeffrey: I think if our feedback says "please discuss this, this, this in the explainer", that'll have an effect. Especially if that's the opening of the comment.

We'll iterate more on the draft comment.


### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Marcos: This is very complicated, especially once visionOS is involved.

Jeffrey: Wanted to ask if Apple has looked at exposing visionOS's custom hover effects in any way to the web. E.g. by using the custom-select `<selectedoption>` behavior of copying the DOM tree, and styling the two options differently.

Marcos/Jeffrey discussion of what that might look like.

Serena: What does interest target do that we can't do with hover?

Jeffrey: Hover is mouse-only, and this wants to expose this to other input modalities, like keyboard, touch, XR, etc. Currently specifies behavior for mouse+keyboard, maybe suggests it for touch, leaves it up to the OS for other modalities.

Marcos: In visionOS, if we exposed hover, apps would know where you're looking all the time. It does react, but doesn't expose where it's reacting.

Serena: Not proposing that this replaces hover?

Marcos: Expression of interest is a gesture that I'm interested. E.g. you mouse-hover on github. Or you long-press on some native apps.

Serena: We're worried about leaking more information?

Marcos: That's 1, and you might mess with a platform convention.

Jeffrey: We discussed the touchscreen affordance, and thought the proposal was a good idea anyway. Apple raised the visionOS issue 1.5 years ago, but Anne brought our attention to it a couple weeks ago, so we're asking if we still think it's a good idea given that.
    
Marcos: Definitely not a bad idea, but is it doable? Who takes on the burden to prove it's doable and safe without fundamentally changing how a platform works? There are existing affordances that users are used to, and if we mess with them, there could be unintended consequences. Like with being able to cancel right-click or not being able to paste.

## Breakout B (America / Europe) - [2025-10-08](https://www.timeanddate.com/worldclock/converter.html?iso=20251008T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Jeffrey, Yves
    
Regrets: Hadley, Sarven, Christian
    
Scribe: Jeffrey

<!-- Agenda+ -->

### Double-check JSON-LD charter PR
https://github.com/w3c/json-ld-charter-2025/pull/17 with proposed comment in https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1150.

Jeffrey: Sarven and I are happy with the changes, but wanted to double-check before saying the TAG's happy.

Lola: These comments all look reasonable. They're just being more specific.

Yves: I agree with the changes too.

Matthew: Me too.

Lola: Jeffrey+Sarven are good to reply.

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

Matthew: Happy to write a PR if I knew what to write. In discussion, I think we couldn't find a better definition than is in the document. We could just say the definition we have is fine. Only related thing I don't have an answer to, is the deffinition for assistive technology and whether they're UAs. Doesn't matter from this document's perspective. WCAG and Aria use slightly different definitions of AT, which is out of this document's scope.

Jeffrey: I want to ensure that our definition implies that AT or UA+AT is also a UA.

Matthew: Some people think AT could be a UA on its own. Depends on what kind of AT.

Jeffrey: Sounds like we're ready to close this with "no change necessary".

Lola: Wait for Sarven.

Matthew: Slack?

Jeffrey: Prefer commenting on the issue.

Lola: Do both.

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven
### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk


<!-- PRs -->

### [user-agents#25: Add Audience section](https://github.com/w3ctag/user-agents/pull/25) - @csarven, @csarven
### [prevent-credential-abuse#52: Add discrimination based on certain fields under Exclusion](https://github.com/w3ctag/prevent-credential-abuse/pull/52) - @csarven

Jeffrey: I've assigned the issue to Martin, who had the comments last week.

### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin

Jeffrey: There are comments I have to incorporate.

### [design-principles#588: Rewrite the "removing features" section, incorporating "Support Existing Content" from the HTTP Design Principles](https://github.com/w3ctag/design-principles/pull/588) - @jyasskin

Jeffrey: I need re-reviews from a bunch of people who've made comments.

<!-- Design Reviews -->

### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://github.com/w3ctag/design-reviews/issues/1134) - @jyasskin, @dandclark

Jeffrey: Proponents replied. I'll reply `satisfied` and encourage them to keep iterating with the HTML group.



### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @matatk, @dandclark

Jeffrey: They updated the explainer. 

Matthew: Question is, what kinds of problems will be caused by delaying this feature in favor of doing it "properly" by waiting for html-in-canvas. The explainer updates say performance is affected by doing it the right way, but they haven't put numbers to it. Last time we discussed it, we sympathized with the desire to transpile to the Web, but the Web is high-level, and we don't want to add inaccessible stuff. Some of this stuff is additions to an existing low-level API. But don't necessarily think that means we should carry on down that path. "Better and more efficient" would be great. Question from last time was "we need them to prove that they need the low-level API". They produced the game-over example, which is cool, but you explained how it could be done. Don't know what to do. We're not happy; want to find a better way; HTML-in-canvas is a proposal, but it's some way off. Right now, people are doing loads of stuff in canvas for Reasons. Anything that we're stopping from being possible that you can't do another way? Or can they polyfill.

Jeffrey: They do probably improve Internationalization by using this.

Lola: Sounds like you're not satisfied.

Matthew: They haven't made any changes other than updating the explainer. They did say HTML-in-canvas won't do something. We should agree among ourselves if there's a way to do it. Specifically, they say HTML-in-canvas doesn't address text-shaping use cases. 

Jeffrey: It does, with an appropriate API option. Does take a change to the proposal, but it's straightforward.

Matthew: Then we should pursue HTML-in-canvas until it proves unworkable.

Jeffrey: Do want to include the consideration that we should ship the accessible thing first, so that everyone who can use it, does. We could ship the low-level thing second, and then only people who really need it will move to it.



### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://github.com/w3ctag/design-reviews/issues/1136) - @toreini, @lolaodelola

Matthew: Bump to Breakout C. We thought the picture would be a mock-up of the UI, and it's just a flowchart. They want to minimize the number of domains you need to show. Ehsan has concerns about that. Death of the line of death. They say that sometimes they don't need to show all 3 domains. Where are they proposing to show 3 domains? Address bar, iframe, 3rd???

Lola: They're talking more about implementation than presentation.

Matthew: Get that we avoid talking about UI design, but want some illustration. Even some text.

### [design-reviews#1139: WG Revision: Dubbing and Audio description Profiles of TTML2 (for 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/1139) - @matatk

Matthew: Talked about this last week. Maybe I was just supposed to close it. "They're the experts." I said I'd post it "next week". I'll close it.

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://github.com/w3ctag/design-reviews/issues/1128) - @toreini

Jeffrey: The point is solid, but we need another iteration on the comment.


### Docs CG & Explainer Explainer

Lola: Docs CG is hosting a session at TPAC, which wants to include Matthew and Jeffrey. I proposed https://github.com/w3c-cg/webdocs/issues/21 to explain how Docs CG should review explainers. They want to know how they should review explainers, and how it would be incorporated into the existing process. Don't want to give developers another step. CG is hesitant to commit to the time it takes to do horizontal reviews.

Jeffrey: Looking forward to session. Have ideas.

### On `unsatisfied`

Lola: Do we actively encourage spec authors to write WPTs?

Jeffrey: We do not; other parts of the process do.

Lola: For carousels, if they'd written WPTs, would it have highlighted some issues we found?

Yves: When people writing specs also write the tests, they put in their reading of the spec that they wrote, including things that aren't written in the spec. Main issue is finding people.

Jeffrey: Think traditional WPTs don't cover accessibiility, so if they'd written those, they wouldn't have caught accessibility problems.
    
Lola: One issue we complained about was the pseudo-elements not changing the accessible-name.

Matthew: My issue was that CSS was giving roles to elements, which isn't appropriate. But WPTs couldn't catch that.

Lola: WPTs do include accessible-name and role. Assume Google implemented this in canary, so WPT uses it. Think you'd write a test for the role to be what you expect, but it wouldn't because you're using CSS to change it.

Jeffrey: But they'd just implement the CSS to change the role, so it'd pass.

Jeffrey: I'll challenge the idea that it's inappropriate for CSS to change roles, but not in the last 5 minutes. APA should own the question, really.

Matthew: APA did discuss it, and thought as long as it comes out accessible, it's fine. But I don't agree.


### TPAC planning

Matthew has a draft tool for coordinating who goes where and notifying about conflicts.


## Breakout C (Europe / Asia / Australia) - [2025-10-09](https://www.timeanddate.com/worldclock/converter.html?iso=20251009T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Marcos, Matthew, Ehsan, Lola, Christian
    
Regrets: 
    
Scribe: Ehsan

<!-- Agenda+ -->

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

Lola: 2 PR open, one for misuse example and another for exclusion. Asked for Sarven review but he is out this week. Anyone else? 

PRs:
    
* Misues examples: https://github.com/w3ctag/societal-impact-questionnaire/pull/24
* Exclusions examples: https://github.com/w3ctag/societal-impact-questionnaire/pull/26

They just add example texts for each item. Anyone review? I don't think it is going to be a heavy one but could use a hand.

Noone? Let's discuss it in plenary.

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Lola: will discuss it later

<!-- PRs -->

### [user-agents#28: Add loyalty guidance for facilitating users switching UAs](https://github.com/w3ctag/user-agents/pull/28) - @csarven, @csarven

Lola: I don't think they are here to do the review. Let's leave it for now.

### [design-principles#590: Add principles for task sources](https://github.com/w3ctag/design-principles/pull/590) - @marcoscaceres

Lola: any update Marcos?

Marcos: anyone wants to review this one? I think anyone else might be helpful.

Lola: any takers?

Lola: let's discuss it in plenary. Martin is the main reviewer on this.

### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres

Lola: any update?

Marcos: there is no review on it. 

Lola: can you give an update?

Marcos: when there is iframe, you get execution context that can steal content. This can be harmful. For example in the payment process. It is about what happens if the iframe goes away?
Lola: any review for this?

Yves: I can do that. This is about race condition.

Lola: I will add JEffrey and Yves then.


<!-- Design Reviews -->

### [design-reviews#1144: WG Revision: Geolocation](https://github.com/w3ctag/design-reviews/issues/1144) - @christianliebel

Lola: Chritian, any update?

Christian: This was a review for Geolocation API. I have small review draft and it is ready to be posted.

Lola: any concerns or questions on that?

Christian: three thumbs up. 

Lola: Good to post that then.

### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://github.com/w3ctag/design-reviews/issues/1140) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Lola: any update?

Matthew: I need more time on this.

Lola: was it discussed last week? there seems to some discussions

Matthew: yes.

### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Lola: any update?

Matthew: just checking the history as we discussed it before.

Xiancheng: I have checked it, it was posted on ????

Matthew: Anne has given a list of concerns that webkit has about it. I think it comes to slightly wider discussion about how this going to work on different platforms (such as vision OS). We can have a look and check where we are?

Lola: sounds good to me.

### [design-reviews#1135: Incubation: Inline Integrity](https://github.com/w3ctag/design-reviews/issues/1135) - @toreini

Ehsan: I did a review of this; have two suggestions for the explainer which we have discussed with Jeffrey and the spec writers. Drafted a review and posted with Jeffrey's approval. Need to decide if we have consensus on it. If we do we could close this today. Any questions/concerns?

(none raised)

Lola: Should we ask again in plenary?

Ehsan: my suggestions are basically cosmetic on the explainer; don't have any architectural concens. Happy either way.

Lola: I think you should post your comment - looks good to go based on the discussion so far. The status should be 'validated'.

### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Lola: we need MArtin to discuss. We discussed in B that we need Martin and Sarven to approve. Am I right Matthew?

Matthew: I don't think we have anything other than what we discussed. MArtin's points were more fundamental and our were not, so I would priotrise MArtin's. 

Lola: I want to ask for an update on the algorithms, Marcos?

Marcos: we have concensus between google and apple on the fundamental model. We are waiting for one more approval. On the related topic, the age related topic will have significant impact on Martin's questions and we can revise before he is back. I am excited about the outcome of the age workshop as there are innovative solutions there that can be used and helped for universal application. Eventhough, the wider concerns remain, the proposed solutions are more grounded now with input from regulators and industry. I am very excited about the solutions.

lola: This is really exciting.

Matthew: first, this is really encouraging given the situation. when are we going to find out about this? Some will see Martin tomorrow and we might find out something. We need to have a meeting for update on this, maybe planary is a good place to do that?

Marcos: Martin is the best person to make that call.

Matthew: fantastic.

Lola: great!

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://github.com/w3ctag/design-reviews/issues/1136) - @toreini, @lolaodelola

Ehsan: Review almost ready to post. Main concern is that removing one of the URLs (shwoing 2 instead of 3) may increase the chance of phishing/social engineering attacks. This is becuase they're delegating the task of specifying the iframe to the developer and trusting that they will act in good faith. This seems to be a fundamental question: it seems to reduce user confusion perhaps, but increase the chance of phishing and privacy leakages. I am slightly inclined to oppose it due to that. Whilst the likelihood isn't huge, it does present some risk. (That's a summary of what I'm about to post.)

Lola: Can you post that in the private thread and folks can review it? I have questions but would like to read it.

Ehsan: Yes, sure.

Lola: To Matthew's question yesterday about whether they have any mock-ups. I was looking at the web speech API today and they have a screenshot of what the UI could look like if you're using Web Speech APi - so I dont' think it's out of our remit to ask for something similar on this. Whislt it's up to the UA to decide on the UI, the spec authors could give us an idea.

Ehsan: My main issue is they're removing one of the URLs. If they can find a way to include all 3 It hink it would help.

### [design-reviews-private-brainstorming#211: Draft WebMCP review](https://github.com/w3ctag/design-reviews-private-brainstorming/issues/211) - @xiaochengh

Lola: any update on this?

Xiaocheng: last week I drafted a review to send to webML WG. just wondering if anyone had a look an dok to send it out?

Christian: I had a look. I am interested to know how this can be implemented as JS library. I don't think it is possible.

Xiaocheng: I think we had an agreement in F2F on we should not introduce something like MCP at this moment. Then, if we want to introduce MCP to web, but not as a built-in feature, then we need to introduce something lower-level and general.

Christian: I mean it is possible if that is the concensus. I am surprised as I wonder if anyone asked for this review yet? Are we going to say please stop working on this?

Xiaocheng: we will say consider focusing on something else. The F2F had a discussion on this.

Christian: I don't think it is still doable in JS.

Xiaocheng: Do you want to have a look? ####

Lola: Do you need time to think about it more?

Christian: No, this is the early proposal and it is still being developed so I don't think.

Lola: are there any questions on this? if anyone interested to knwo more on the discussions, the meeting notes are available.

Lola: that concludes the agenda, let's do the triage. Before that, any business needs to be discussed? If not, let's go to the roll-out. Let's start from the button.

Matthew: Can you ping a link to that?

Lola: sure.

Lola: 1134 (already assigned)

Matthew: It has Dan on it, do we want to delegate it to Jeffrey or reassign Dan?

Lola: we need to discuss it with Jeffrey. I won't reassign Dan yet but let's move it to plenary to discuss.

Lola: 1145

Matthew: there was a duplicate on that (1136). This one we talked about it definately. There should be a mistake.

Lola: I close this then.

Lola: 1146? This is writing assistance APIs, we had a couple of those recently. Any takers?

Christian: I was not involved in the specification phase but certainly can have a look.

Ehsan: I am interested.

Matthew: This is interesting. Add me in too.

Lola: Is it pending an accessibility review?

Matthew: not sure, not came across yet.

Lola: I'll add labels to it. What is the difference between Web Architecture and API design?

Matthew: it is the scope. Web Architecture is wider. API design is about if the API name is fine or things like that.

Lola: 1147?

Lola: This is not an explainer format. This is a comment.

Matthew: It happened recently a couple of times.

Lola: It makes reviewing hard. I assign myself to this to remind them to a proper explainer.

Matthew: maybe refer them to the explainer explainer?

Lola: yes, I need to do that.

Lola: 1148
    
Xiaocheng: I can do it.

Matthew: sounds interesting... I don't know how I can contribute. 

Lola: Does it mean you are assigning yourself?

Matthew: I probably I shouldn't do it as I have many thing now.

Yves: I can

Lola: great!

Lola: 1151

Lola: is it security/privacy related? I say yes.

Yves: I can take a look.

Lola: Ehsan do you want to have a look?

Ehsan: yes, it is intresting.

Lola: you seem to be very busy on the reviews. Let's have another one added to review. Anyone?

Lola: I will add myself.

Lola: 1152?

Matthew: I assign myself as APA is already looking at this.

Lola: anyone else?

Matthew: it is trying to provide more declarative ways to do focus-management. It is trynig to avoid the need for JS to do that. It is used on custom selective items (like grid or radiobutton) and gives users the opportunity to do that with JS. They are trying to remove that need. It looks very cool. We have some discussions, liked the overall idea but I think we might some concerns.

Lola: anyone else?

Lola: noone, Matthew you are the only one. send something to Slack so other can comment. Anything related to Privacy or Security?

Matthew: I don't think so.

Lola: 1153?

Matthew: it seems relevant to accessibility. I don't think I can contribute but maybe Xiaocheng can be really good fit.

Xiaocheng: yes, I can take a look.

Lola: anyone else?

Matthew: I will assign myself so I can ask others in APA on this.

Lola: 1155?

Matthew: I assigned myself as APA is looking to it.

Christian: I can.

Marcos: I wrote this spec so if anyone inetertsed can ask questions.

Matthew: I remenber you had accesibility review on this and thanks!

Lola: I will add Marcos to the private-brainsotmring so everyone remembers Marcos has written this.

Matthew: It seems like related to web architecture too, like device orientation API and we might find some items that needs looking into other specs related to this.

Lola: 1156

Matthew: We discussed it in the APA.

Lola: I will add you then so if there is anything related to APA so you can contribute here too.

Lola: Matthew, you have many reviews on your plate. I will make a note on the private-brainstorming so it is only for your opinion.

Xiaocheng: I am very busy at the moment, I like to contribute but I am afraid maybe not.
    
Matthew: What about Lea?

Lola: we should ask svjesus or Lea to review? I put them in the private-brainsotrming. I gonna leave the remaining ones for later.


## Plenary Session - [2025-10-09](https://www.timeanddate.com/worldclock/converter.html?iso=20251009T130000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Hadley, Martin, Jeffrey, Christian, Lola, Xiaocheng, Matthew, Marcos, Yves, Ehsan
    
Regrets:
    
Scribe: Jeffrey

### Age Restrictions Workshop

Hadley: The Program Committee will create a report about consensus. Martin+Mark Nottingham will take steps back to the TAG and IAB to figure out what we can say that's more opinionated.

Martin: In the short term, we should discuss the report. I heard a lot of things that will be hard to summarize right now. The workshop helped understand the complexity of the problem space. Censorship, privacy to getting stuff deployed. Report will try to make sense and rationalize it. Then discussions about constructive ways to proceed and things to point people away from. Could be a Finding and could be joint with IAB or independent.

Hadley: Breadth of attendees was impressive. Web, Internet, Civil Society, academics, implementers, governments. Great for collaboration, less for looking for consensus in the room.

Jeffrey: How should this affect the prevent-credential-abuse finding?

Martin: Identity and identity-online plays into it. Some of the credential-abuse finding is right on point. But right thing might be to try to insulate the two topics.

Hadley: Topic came up in the workshop. Participants are concerned about every website wanting to know invasive things before reading their newsletter. 

Martin: Maybe we change the tense on the workshop.

Marcos: Workshop was clear about the distinction between identity and age verification. Community's working assumption was that identity is age verification, and it's not. That's a success of the workshop. prevent-credential-abuse holds very strongly for identity. Says government documents shouldn't be used willy-nilly. Potentially a happy path.

Marcos: Question about availability of list of requirements. Want to see that as a draft early. Would let engineers start looking for solutions.

Martin: Might be able to share that more widely, at least with TAG. Not more broadly before a discussion with attendees.

Hadley: On identity: I had been worried that everyone would be confused, and they weren't.

Lola: Difference between identity and age verification, is there a difference between saying "Lola is 33" vs "this person is 33"?

Martin: More or less. Recognition from several sectors that having just one mechanism (e.g. tying to government id or facial recognition) doesn't solve the problem broadly enough. E.g. not everyone has a government id that's recognized by the website. Privacy properties also vary.

Marcos: This also just deals with adult content, so it's just "is Lola an adult". Jurisdictions don't vary too much, so you can prove adultness without revealing age at all.

Martin: Other use cases are about age-appropriate design, where you get a different design for very-young, and another for the next up, and another for adults. That was particularly challenging. I'm not even sure the adult-or-not signal vs age-appropriate design takes the same solutions.

Hadley: Also keeping adults _out_ of children's spaces. One participant who works in schools: sexual content is least likely to cause harm, but body dysmorphia can cause more harm. Violent content. Not just porn.

Martin: Not clear that the same solutions that work for adult-or-not (e.g. alcohol) apply in all scenarios. Other aspects of safety, like child-safety is not just preventing them from seeing things they're not prepared for. Additional support mechanisms are out of scope for us, but there are other mechanisms. Folks involved with parental control software have a surveillance apparatus, so you know if a particular child is trying to break through the blocks so teachers and parents can have a word with them. Building a surveillance apparatus at web scale might not be a good choice. There were like 60 design criteria.

Hadley: There's a lot to synthesize. 

Marcos: There were some key papers that were very relevant. 

Jeffrey: Can you make a list of the best papers for us?

Martin: Can share the PC's sense of what were the most interesting. Marcos was highlighting great ones.

Xiaocheng: Do we have a collection of cases of age verification. Feel like we spent a lot of time on raising examples, but lots of discussion is on alcohol or porn. Use cases?

Hadley: Dont' know we have a formal collection, but talked about a lot.

Martinn: Legal landscape is all porn or extremist/terrorist-grooming content. But lots more things are potentially important. Differential ad and profiling purposes. Safe spaces for children who are free from unauthorized/non-guardian adults. Dieting, LGBT, etc. We tried to focus on the technical mechanisms.

Hadley: We ran into but didn't flesh out that the use case is often that people <18 won't have a government ID yet, so what do they do to prove, say, they're over 13.

Martin: Even the child's documents (e.g. birth certificates) often don't have biometrics.

Marcos: If you just turned 18 might not have an identity card. Traveling. Lots of interesting edge cases. Respecting that people have different documents. Credit cards. This wasn't just about the Web, but about all internet use. E.g. Telegram channels might need age verification.

Martin: We recognized pretty quickly that the set of things that might need restrictions has a cultural basis. Any system needs to be flexible to accommodate differing society's differing needs. E.g. China, NA, Europe might all differ.

Marcos: Lots of cherry-picking w.r.t. what's considered harmful vs not. Body image: social media is harmful to some degree of the population, and young people have issues, but a larger percentage have positive experiences. So by excluding the small group, it impacts the large group. Always check who's making statements and their rationale.

Hadley: Variety of participants meant a variety of appetite for risk. Excluding people, further-disadvantaging people. We know nothing's perfect, so how do we cope with problems? No consensus on appropriate level of not-perfect-ness.

Matthew: Marcos reminded me of trigger warnings, and COGA has looked at it. Trigger warnings are triggering, so we've been thinking about enabling people to by themselves stop from being exposed to certain things. Could have that discussion separately.

<!-- Agenda+ -->

### Time change
- Unable to schedule plenary due to no overlap - lola

Lola: Appreciate Jeffrey doing this last year. Times will be changing from 1st week of November. Have times for the 3 weekly meetings, but the plenary has no overlap including inconvenient times. Want to give folks an opportunity to add times to your range for plenaries. Please expand your ranges a bit for plenaries. Currently floated times are UTC 7am and UTC 10pm. Those are good for Asia/Australia, and Europe. Neither is good for North America.

Hadley: This is for the next 6 months.

Lola: Yes, until March.


<!-- PRs -->

<!-- Design Reviews -->

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @jyasskin, @marcoscaceres, @toreini

Ehsan: Concerned about sacrificing privacy for usability. I remember being against it because the privacy sacrifice wasn't justified enough. I'm still on that decision. On the historical discussion, was meant to let them know.

Jeffrey: We have discussed some with them, we could potentially invite them to talk to us. They've added comparison with additional UI, I think the privacy change is small enough that the benefit to useability could justify it. Martin made a suggestion that people design a log in element similar to PEPC that might remove the privacy loss bc the browser would be rendering stuff. It would be plausible to sketch out a design before we say "do this instead."

Martin: That's not our responsibility

Jeffrey: If we give an alternative, we should show that it's possible. At least have a sketch about how to overcome difficulties

Martin: I disagree. I think we can say that if it's going to have this problem, you should consider a solution

Jeffrey: They're happy to say that if you clear cookies, this stops saying that you've logged in the past. The permission associated is that you logged into the site

Martin: what's the point?

Jeffrey: The use cases are unclear but most interested in the case of propogation across devices with syncing pass keys. There's flexibilty for UAs to do what's right.

Martin: have to duck

Hadley: Further discussion needed?

Martin: Yes

Jeffrey: Move to A

Hadley:  Ehsan is that ok?

Ehsan: Yes


### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @csarven, @maxpassion

https://github.com/w3ctag/design-reviews/issues/1015#issuecomment-3348599823

Jeffrey: they'd like at least soem of us to attend their TPAC meeting. We should send the people who are concerned and let them try to convince those people.

Most active on the issue are Martin, Sarven and Marcos.

Marcos: I can possibly attend but need to check my schedule. Tentatively yes.

I'll reply on the issue.


### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @martinthomson, @jyasskin, @csarven

Jeffrey: Martin said Mozilla were going to comment. we were going to wait for that so we could consider it.

Signature based integrity has different properties from SRI, but the proposal is to use the SRI terminology and attributes. they should consider using different names to make clear that the properties are different. 

The overall use case seemed fine, but it's just about confusing names. 

Let's look at it next week and make sure we still want to wait. Let's put it in breakout C. I don't have strong opinions about this. 

### [Incubation: patching (interleaved out-of-order streaming)](https://github.com/w3ctag/design-reviews/issues/1134)

Lola: Should we reassign Dan?

Jeffrey: Yes. And we can leave him assigned to the patching one because that's about ready to close.

### [WG Revision: CSS Color Adjust Level 1] (https://github.com/w3ctag/design-reviews-private-brainstorming/issues/212)

Lola: We need reviewers.

Hadley: Should we review it?

Lola: it was suggested that Lea and SVGeesus should?

Jeffrey: they will be highly involved. 

And I think we should decline this. 

Hadley: Can say "Do you know of any particular architectural concerns?"

Xiaocheng: Does that mean we can decline a lot of design reviews?

Hadley: Maybe not most, but definitely more than we have been. We're often interested and not good at saying 'no'.

Xiaocheng: I'm still interested, but worried about time. I'll assign myself.

Jeffrey: I do think we should be more eager to decline things.

### Breakout Rollup



### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


### [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh

Jeffrey: we had closed this as satisfied, having discussed some concerns on how touchscreens deal with things. Anne from Apple said that VisionOS had privacy conerns if you do this by gaze tracking. there are workarounds, you can have the gaze show a button and you tap the button to show an interest (similar to the touchscreen solution where you long press, and tap one of the menu items. That shows interest). 

Question is: are we still satisfied with the feature, given the extra concerns about a gaze-based interaction mode?

Hadley: Did Anne have other solutions to propose, or only concerns to share?

Jeffrey: Anne had only concerns. This was raised over a year ago, with no attempt to suggest a way around it. I don't think we should endorse that kind of blocking things without suggesting a way forward.

Marcos: Don't think they're just privacy concerns; they're concerrns that it might not be implementable. I've discussed inside Apple. Concerened that it's not implementable. There's a class of applications that by policy can have access to some of this, in a general purpose platform like the web, it might not be possible to do it. In visionOS, doesn't exactly solve the mobile case where it interferes with long-press. Not privacy at that point, just about a platform implementer having to fundamentally change the way their OS works.

Matthew: Really want to look into the concerns before we do anything, even though status quo is that we'd stay satisfied. Last time it was easy once we discussed it. I'm very in favor of finding a way to make this work, but concerned. I'll look.

