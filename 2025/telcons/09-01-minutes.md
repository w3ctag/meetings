# TAG Minutes - Week of 01 September 2025

## Breakout A (Asia / Australia / West America) - [2025-09-02](https://www.timeanddate.com/worldclock/converter.html?iso=20250902T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Marcos, Martin, Xiaocheng, Jeffrey (late)

Regrets: Max

### [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion

Pass

### [design-reviews#1092: Web Authentication Immediate Mediation](https://github.com/w3ctag/design-reviews/issues/1092) - @martinthomson, @toreini

Martin to follow up on this.  General sense is that the feedback is OK, but Jeffrey has some concerns about accuracy (which I, in turn, have accuracy problems with).

### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres

Martin: Were some of those quotes in earlier versions of the explainer?

Marcos: Maybe.  The schema thing might have been added later.  Max and I went through it together and put notes.  I got ChatGPT to rewrite some of this and add links.  But it didn't invent anything.  If anything, the humans hallucinated.  The retention policy was predicated on the LLM going to a remote server.

Martin: Was this always always local?

Marcos: It was always intended to be local, but I was asking if a local model could meet quality expectations.  Lots depend on that question.  The presumption of this being on-device only holds until local models decide to hand off to a server, which is what some might/will(?) do.
...The thing about structured output.  Might need to chase history; it wasn't there when we went through originally.  Constraints with regex/schema was not there.
...The whole thing about user transparency was not hallucination.
...Computation abuse was not covered.
...Fingerprinting - can't see how that was false.  This might exploit hardware that differs between people.  That is a fingerprinting risk potentially.

Martin: That would depend on getting reliably different results for different people based on choice of model, choice of hardware, or other things like that.

Marcos: Not all hallucinations; we missed stuff, but there are a number of concerns that remain.  Resolution can be validated and we can move on.

Martin: The packaging of the message obscured the actual message. Need to make sure that the key points you highlight here are re-made, maybe in a more succint form.

Marcos: Looking for the history. Seems strange that it would have taken text that wasn't there. 

Martin: The text reads plausibly, which is a trait of a lot of LLMs.

Marcos: Didn't change the messaging of the original thing, just trying to link up the text. 2 parts: re-respond, and clarifying various things. Happy to remove the linked up text. On the TAG part, not being reactionary. We're going to annoy people, and being reactionary on this wasn't super helpful.

...

Marcos: Will look into the JSON Schema part. Re-review the rest of the review. There's an overall concern about doing queries with processing unbeknownst to the user. 

Jeffrey: Using local power to answer queries?

Marcos: Yes.

Martin: Somewhat a security vulnerability. The other party is exposed to things the user's LLM tells their systems to do.

Jeffrey: Bitcoin miners.

Marcos: Don't want to get into a back-and-forth.

Jeffrey: I'll review it and find ways to say things that won't/can't be argued with.

Marcos: I'll draft a response in the brainstorming.

Jeffrey: I plan to write a thing on how to generate review responses using LLMs.  Christian had thoughts and experience to share.  Idea was to not give the output of the LLM to people to read.  Needs more discussion once it has been proposed.


### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark

Jeffrey is waiting on Dan to look at some updated changes, but we might look also...

\[Some discussion about synchronous loading, blocking, style imports, usability, FOUC, etc...]

Will post tomorrow after checking with Dan.

### [design-reviews#1052: Early Design Review for Device Bound Session Credentials](https://github.com/w3ctag/design-reviews/issues/1052) - @martinthomson, @jyasskin, @lolaodelola

Martin: I'm ready to be finished with this. Not getting traction with proponents.

Jeffrey: We might suggest that they explore the alternative (more modular) more seriously and close unsatisfied.  Proponents are also at this point.
... Case that the proponents haven't really tried orthogonal/modular pieces.  API owners in Chromium will decide if it ships there. I can post this once Martin writes it.


### [design-reviews#1039: Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039) - @jyasskin, @marcoscaceres, @martinthomson

Jeffrey: Should time this out and let them come back when we're ready. It's potentially a big architectural change for FedCM (2-party to 3-party model) but we don't need to just wait for it.

Closed out.

Martin: Good model, but more complicated.


### [design-reviews#1120: CSS find-in-page highlight pseudos](https://github.com/w3ctag/design-reviews/issues/1120) - @matatk, @xiaochengh

Dan has been going back and forth on the [blink-dev thread](https://groups.google.com/a/chromium.org/g/blink-dev/c/U-6tIuuGtgo/m/DhstpnP6HAAJ) on this one.  

Are devs asking for this because browsers are doing the wrong thing?  If so, browsers can fix bugs.  If not, then what are the developers needing from this.

Jeffrey: I suggest we just endorse Dan's feedback.

Martin: Interoperability ... depends what you're trying to do. If you meant to highlight the line instead of just the text, Safari won't do that.

Marcos: Might be platform-wide ability to do it.

Martin: Might be things you can't do with it, like override color. You've done a find, and there's color, and you can't override that. But could be the case that there's value in having Safari implement some of this, so when you do find-in-page, the website knows what parts are found, and do other styling around it.

Jeffrey: That sounds like a recommendation that Safari look harder at certain parts of the use case, in particular "highlight things around the match".

Martin: Or draw big arrows pointing to it.

Jeffrey: I think I just volunteered to draft a comment. Argh.

### [design-reviews#1108: ServiceWorkerAutoPreload](https://github.com/w3ctag/design-reviews/issues/1108) - unassigned
### [design-reviews#1137: [wg/didmethods] DID Methods Working Group](https://github.com/w3ctag/design-reviews/issues/1137) - @jyasskin
### [accessibility-screener#9: Convert to HTML form](https://github.com/w3ctag/accessibility-screener/pull/9) - @ananya-ky
### [web-no-papers#37: Editorial pass](https://github.com/w3ctag/web-no-papers/pull/37) - @martinthomson
### [design-reviews#1134: Incubation: patching (interleaved out-of-order streaming)](https://github.com/w3ctag/design-reviews/issues/1134) - @jyasskin, @dandclark

### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Breakout B (America / Europe) - [2025-09-03](https://www.timeanddate.com/worldclock/converter.html?iso=20250903T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Jeffrey, Matthew, Dan, Yves, Sarven

Regrets: Christian

Scribe: Matthew

### [user-agents#14: Clarify the scope or definition of what constitutes web user agent](https://github.com/w3ctag/user-agents/issues/14) - @matatk

Matthew: Jeffrey replied. We have a definition of a "web user agent", and that helps us focus. JEffrey's asking if it gives us an answer that we wouldn't have consensus on? Or is there an example that could clarify it? I think the definition is reasonable. Suspect the only area where it might be less clear is in the superapps/miniapps, but even there it's not too difficult. A next step is for us to think about whether that definition filters the list sufficiently.

Lola: Thoughts?

Yves: Are AI agents in the LLM bucket? AI agents have some responsibility to present to the user the exact thing that was meant by the author.

Matthew: There's a difference between LLMs that are provided by the webapp, and an LLM in the user agent that tries to act on behalf of the user. Worth denoting that they're different.

Jeffrey: LLMs are a piece of a system, but we should avoid talking about them directly, and talk about the system as a whole - is it an agent driving a browser, or solving a more specific problem. Some may, or may not, be UAs. They will satisfy the duties of being a UA in different ways.

Yves: Should we replace LLM by AI Agents?

Jeffrey: I feel an LLM is a subset. A summarizer wouldn't count as an agent.

Yves: E.g. something that gives a description of an image for peole who can't see it.

Jeffrey: That may be a UA, but not what people think of when they talk about agentic browsers.

Lola: Sarven added https://github.com/w3ctag/user-agents/issues/14#issuecomment-3250073517 *see definition of web user aagent in the issue*

Sarven: I like the distinction that we made in Edinburgh. Emphasising the web part, and acting on behalf of the user. Question for today is: given all this background for a couple of decades, how far has that definition come, and whether the new understanding is still applicable. It would be good to stay true to that understanding - it's acting on behalf of the user, the user's agent. Anything that diverges - if the browser's going out and doing things... how opinionated should the UA be, that it is acting on behalf of the user? As opposed to acting on *knowledge* of the user. How much is the browser going to do on the user's behalf? E.g. decide to install an LLM on behalf of the user to solve a problem with them. Is that an explicit permission given to the agent by the user? Curious in exporing and understanding this, it's a bit of a vague notion. Who says it's acting on behalf of the user? Is installing it giving that permission?

Lola: How do we define acting on behalf of the user? When we get design reviews for specs doing something on behalf of the user, without the user's explicit consent, we flag this. I don't think we need to be too worried with respoect to whether somethihng is on behalf of the user, as that's when things like consent and permissions come into play. But I do have a question on top of that, which is: what instances does a software entity interact with a webiste without the user triggering that action? What current real-world situations do we find wehere software claims to be acting on behalf of the user, without being explicitly triggered by the user?

Jeffrey: There are cases where it's separated in time. RSS user fetches things, not at the same time the user asked for it. Some of this is contraverisal, but web pages that report back stats about how they were used as they're unloading/after they've unloaded. The web page asks the UA to send the stats on the user's behalf. The user's permission here is pretty implicit.

Sarven: Distinction between 1st and 3rd party (another issue) - there are extensions that I find indispensible. E.g. uMatrix extension ( https://addons.mozilla.org/en-US/firefox/addon/umatrix/ ). By default the browser fetches 3p assets (CSS, JS, etc). Here we have an extension that takes another step towards protecting the user. Starts with blocking by default, and having the user granting access to certain origins/resource formats. This flips the model around: blocking by default. This is why we have the privacy tests: https://privacytests.org/

... If you try browsers, e.g. LibreWolf etc. are more conservative on what will be fetched on behalf of the user. How do you draw the line... whether the extension is acting on user's behalf.

Jeffrey: We have an expectation that all web browsers are acting on behalf of their users, and that there will be variation in what users want, and in what browsers do, so users can pick the right browser for them. These guidelines are a lower bound. We need to be pretty conservative as they will apply to all UAs. A user shouldn't be able to pick a UA that *deson't* comply with these.

... I think we've discussed it as much as we can today - people need to read and think about it.

Lola: next steps is for people to open PRs!

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

*done by virtue of the above*

### [user-agents#7: Consider applications with both 1p and 3p sections](https://github.com/w3ctag/user-agents/issues/7) - @jyasskin

Lola: We talked abou this a bit - anything to add?

Jeffrey: This has a PR - https://github.com/w3ctag/user-agents/pull/21 - needs review.

... The idea is there are libraries like web views. There are applications that embed web views. Which parts of these are UAs and thus need to satisfy the UA duties? There are concerns in both directions and I tried to capture them in one section. Web view libraries don't want to be responsible for upholding the duties, as apps only use them to render 1p content - effectively implementing the application but nothing more. Users can expect an app to act for itself. But as soon as one of those apps starts browsing the web via a web view, then it becomes responsible for those duties.

... Also there are some libraries that take on more responsibilities - e.g. including tabs etc. so they take on more.

... On the other hand, an app that embeds custom tabs/view controller, there's two parts: (1) the part that allows the user to interact with the specific app/service (in which case it doesn't have to uphold the duties) and (2) the part where the user goes on to the open web (where the duties would need to be upheld).

Lola: Suggest people read and review the PR.

Jeffrey: Yes, please review. Check you are happy with the approach I took.

### [design-reviews#838: Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hadleybeeman, @lolaodelola

Lola: Left a note in the brainstorming thread. I brought together all the written and discussed feedback (from last week in C with Martin and Mat, included the mention of wicg/turtledove#990 - I see they're trying to address this). They're still thinking through the capture issue as of December last year.

### [societal-impact-questionnaire#11: centralization](https://github.com/w3ctag/societal-impact-questionnaire/issues/11)

Sarven: PR https://github.com/w3ctag/societal-impact-questionnaire/pull/23

Lola: Sarven opened PR today; I reviewed it. It would be good for others to review as well.

Jeffrey: It's not a published finding so you should feel free to iterate faster.

Sarven: We have to publish two things: (1) editor's draft, sans W3C label; and (2) the draft note. Right now it's only on GitHub. Maybe we need a separate cut, or two branchs?

Jeffrey: I'd avoid separate branches; can do live publishing to TR space; Yves and I can help.

Sarven: Will follow up with you.

Yves: First publication on TR will need a decision from the group (that has a URL).

Sarven: Both responsible AI and another issue touch on the dangers of centralization. I thought I could introduce a sentence about it's not that AI is the concern, but solutions around AI at the moment have a big push towards centralization, and a lot of ML being done on the client side. Thought we could mention here, and refer to Ethical Web Principles (we have a section on control). So instead of opening up a whole new section about AI / algorithmic bias, we could generally roll this into centralization and link to EWP and possibly webmachinelearning.

Lola: Makes sense. I'm still not convinced that we need to write anything about AI at all, unless we're using AI as an example for something. The AI issue meets many different points in the questionnaire - it could be an example for almost all the things we're asking about. I'm not sure we want to name specific technologies or solutions to things unless we're using it as examples.

Jeffrey: Good point. I feel like AI is not necessarily and example of centralization, as there are open source models, and models that run locally. All of the problematic aspects are topics, rather than AI specifically.

Lola: If you feel it should be included, write the sentence and make a new PR. Maybe when we see it in context it'll be easier to review.

Sarven: I think it goes in this PR, as didn't want to add a new section.

Lola: We could close the algorithmic bias issue then?

Jeffrey: I don't think we should just close it - bias and auditability are issues that could apply in other areas, but also do apply to AI. We could cover the harms without mentioning it's specific to AI. Close it with links to the paragraphs that address those harms.

Lola: We'll come back to this.

Sarven: We shouldn't hold this one up to resolve the AI part.

Lola: Yes, please do. We will merge if we don't hear anything.

### [societal-impact-questionnaire#4: Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4)

*discussed above*

### [web-no-papers#14: TAG, please review this document](https://github.com/w3ctag/web-no-papers/issues/14) - @jyasskin, @toreini

Jeffrey: Martin's still going through the rest of my comment; more to come. This will be a Hong Kong topic.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

*bump to C*

### [explainer-explainer#9: Update the WebIDL guidance for explainers](https://github.com/w3ctag/explainer-explainer/issues/9)

*bump to HK or after*

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

*done by virtue of above discussion*

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

Lola: Docs CG wants to invite you Jeffrey and Matthew to next Explainer Explainer call.

Jeffrey: May be best to do this after HK.

Lola: is there anything we want to add to agendas before/at HK?

Jeffrey: I think it'd be better to focus on UAs, WnP, things that are likely to get published. But if people have specific things they want to fix, let us know.

### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin

*discussed above - UAs 7*

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://github.com/w3ctag/design-reviews/issues/1095) - @jyasskin, @dandclark

Jeffrey: The Flutter team has been concerned about the feedback we're giving so I've been talking with them directly and encouraging them to update their explainer. They're worried that people are writing apps that are expected to be compiled to multiple platforms, and they want to use the lowest-level API to draw text, and handle accessibility at a higher level. My inkling is that Flutter doesn't do well at convincing apps to provide that accessibility info, but I don't have enough evidence - so suggest they update the explainer and let TAG review it.

Lola: accessibility info at higher level?

Jeffrey: Flutter has an API for adding accessibility info, so the component can be drawn, but then have its own accessibility tree style info added on top. I feel like this works in theory but not in practice, but I don't have the evidence/expereience with it to demonstrate this concern.

Matthew: Concern. What you said. I'm not a Flutter expert, but any time we make it not-part of the standard controls, people will miss it. I sympathize that if you want to make something truly cross-platform, this is the way you'd want to do it. But the web isn't a low-level platform.

Jeffrey: I think the Chromium team is pursuing both approaches; low-level API and a higher one that comes with accessibility info that could work on top. I asked the proponents to *prove* that if you have the higher-level API you *need* the lower-level one. E.g. performacne or similar. We should aim to go with the higher-level/more accessible API by default.

### [design-reviews#1130: Incubation: An `Origin` Object](https://github.com/w3ctag/design-reviews/issues/1130) - @csarven, @dandclark

Dan: Been looking at this; responded about a week ago. Contention was whether this should be part of the platform, or a library. The response was same-site checks are hard. I find this somewhat persuasive. I know Christian was not as keen - want to get his thoughts. I'm starting to come around to this. The interesting part is about opaque origins, and whether they are the same or not. Mike's proposal is maybe not complete there, because in order to construct the Origin objects you can only really do that from a serialized opaque origin, so that's not telling the full story, but the explaienr touches on this. It owuld be useful to flesh this out.

... I have the makings of a response; would like Christian's and Sarven's take. I'm leaning towards 'satisfied' though.

Lola: Same site difficulties?

Dan: The notion of same site is not baked into the platform. You can take the path out, and compare the origins and try it that way. There are pitfals. But 'is same site' is a different kind of check that depends on public info. You could have danclark.github.io and lola.github.io - those are not same site, but in order to know that github.io is to be treated as an origin but not a site, there's some context there. Sometimes subdomains should be treated as an origin and sometimes not. There are suffix lists that compile this info. The browser has some info on this but doesn't expose it via a platform API.

Sarven: The way you're expressing this makes sense.

Lola: so Sarven is +1 and need Christian's info.

Matthew: Are 'multi-tenated' sites (sub-paths) out of scope?

Dan: Yes. Main use case is, I recieve a message from an iframe, is it from an origin I trust? Url object and Urlpattern would be used for those.

### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @martinthomson, @jyasskin, @csarven (also added to C to give Martin opportunity to discuss)

*bump to C*

Matthew: Feature request for could we include the Tag Bot links in the agenda.

### [design-reviews#1000: Declarative CSS Modules and Declarative Shadow DOM `adoptedstylesheets` attribute](https://github.com/w3ctag/design-reviews/issues/1000) - @jyasskin, @dandclark (Added from A)

Jeffrey: We have a proposed comment. Dan has +1'd it. I want to check everyone else is happy with it. Then I will post. Then we mark as 'satisfied' - it's still early, there's work ongoing. It's a long comment; please check it by tomorrow. We agreed in A that it needs a bit more input.

Matthew: Last week, I discovered the `validated` status. Should this be validated or satisfied?

Jeffrey: We'd marked the original as 'satisfied with concenrs'; 'validated' is a fine thing to use instead; I don't feel strongly.

### [design-reviews#1137: [wg/didmethods] DID Methods Working Group](https://github.com/w3ctag/design-reviews/issues/1137) - @jyasskin (Added from A)

Jeffrey: I reviewed the charter; it looks good except for two comments which I left in brainstorming. They use the word 'ephemoral' which means a lot but it's not well defined (we should ask them to). They also use the term 'decentralized' but this is not ncessesarily the case, e.g. in blockchain example, if a few actors control most of the network (which can happen) then you can change a document with their agreement.

Lola: You also asked if we should also ask them to co-ordinate with FedID and other identity groups. Do you think this has crossover?

Jeffrey: We have two different kinds of identity groups working in parallel, so we should suggest they start talking together. I think Sarven could help in drafting this.

Sarven: I saw this and self-assigned. The issue in w3c/strategy has been hanging for a while. Would you like me to review as well, in the next week? Maybe for tomorrow?

Jeffrey: it's only 3 weeks old that they asked for a review. Everyone else has given them feedback. Security asked them to do things. It would be good to get our review out. I think you have expertise here.

Sarven: Will review. Your review looks good.

### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Breakout C (Europe / Asia / Australia) - [2025-09-04](https://www.timeanddate.com/worldclock/converter.html?iso=20250904T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Sarven, Lola, Martin, Yves, Matthew, Christian

Regrets: Max

Scribe: Martin

### [design-reviews#1: Approximate Geolocation](https://github.com/w3ctag/design-reviews/issues/1131) - @toreini, @christianliebel, @lolaodelola

Lola: Not had a chance to look.  Some feedback on the explainer, but nothing much.  No Christian here today.

Marcos: Have looked. It's interesting.
... An interesting thing that has come up with this one, for longer term consideration, is that the granularity can be so wide that it may not warrant a prompt any more because it is roughly equivalent to IP geolocation.  Putting that out there to think about.  I don't know what that means if there is a VPN active.

Lola: Is that something they need to put in the security considerations?

Yves: The VPN question is important here.  It is easy to fake location with a VPN, but not with the API.  Is there something needed to activate.

Marcos: This doesn't currently  require user activation, which is an outstanding issue on the main spec.

Yves: A permission might not be for every call.  If you request far too often, you might be able to infer the proper location instead of getting an approximated one.

Marcos: In practice, you don't query, you'll get a cached position from subsequent requests.  It's not cheap to update the location.  For this you would get something stale.

Yves: Might need to explicitly add something to avoid oversampling.

Lola: Others might have input, but it sounds like we need to give people a chance to review.

Yves: not a negative comment, just feedback.

Martin: We could put the comment in.

Lola: Not confident in drafting a comment.

Yves: I can try to draft something.

### [design-reviews#1138: [wg/webextensions] Web Extensions Working Group](https://github.com/w3ctag/design-reviews/issues/1138) - @csarven, @matatk, @toreini, @christianliebel

Sarven: Review https://github.com/w3ctag/design-reviews-private-brainstorming/issues/193#issuecomment-3244825170

Matthew: APA has looked at this.  I do think that this group seems to have been responsible for some positive change, so getting people into a working group is a good thing.  They have adopted a novel-for-w3c approach, because they have consensus around differences.  Aim to smooth those over eventually.  Not sure if the CG will be kept (might be mentioned in charter).  We might have an opinion about that, might say that keeping the CG is good.  Not sure what else APA said.

Sarven: The charter does indicate coordination with the CG.  A bit more specifically on deliverables, there were discussions from PLH (seemed uncertain?) definitely keeping the spec in CR snapshot.  They anticipate changes constantly.  They don't want to go to REC and have a final cutoff.  That was their consensus.  I didn't get much about what the coordination would look like, but presume that ...  they have a good scope and only mention two deliverables.  if the group thinks they need more specs, they will recharter to take more work on.  The CG will intubate and add work to the charter as they go.  That's based on inference from discussion and charter.
... There were concerns around manifest v3.  Didn't dig too deeply, but there are differences in views between browsers. Highlighted in the review.  If the CG has incubation experience, then whatever the version is arrived at, then the working group can take that on.  Not a TAG call so much.  What I thought was more important was to talk about threat models and trust models.  There is the idea that CR is active, so they should have a threat modeling exercise and publish that as they go.  Implementation experience shows authentication is a challenging part and it needs to be clearer how extensions are authenticated alongside other authentication methods on the platform.  Parts might be from FedCM.  They might need to iron that out.  The point is not to come up with an authentication mechanism, but clarify it in their output.

Martin: Ask for clarification about authentication.

Sarven: Depending on the authentication with remote storage, how would an extension be identified?  How might it be authorized to make requests and how would servers authorize requests from extensions?
... [Dokieli](https://dokie.li/) is an application I work on, it also works as an extension.  The feature to annotate webpages, enables the user to store annotations in their preferred storage.  users need to authenticate to the extension, so the extension knows about storage and then have the storage system know that the client is authorized to write to that space.  That depends on the authentication mechanism.  Lots of question marks there.

Matthew: I found APA minutes.  +1 to Sarven (on something).  APA we did have some things we would want to check and review in the deliverables, but the charter seemed good.  One thing is that they work closely with other groups, liaisonization, etc..  Might be good for threat modeling.  Simeon, who might be a chair, contacted APA chairs if there was anything we would like to see included.  We thought it was fine for us to do horizontal review of deliverables.   There might be other groups where that needs to be clear.  In terms of threat modeling and S&P,  Ehsan's speciality, so we  might file issues as interested individuals.  On manifest v3, I do agree with Sarven that this is such a big change that this is not going to get consensus, which will cause fragmentation.  The group has addressed this by acknowledging the issue and keeping awareness of it.  I don't know if they are going to reconcile or just document differences.  My own extension used to be a lot better, now you can't run the same code on all browsers.  This group is a positive force for fixing that.

Lola: Can we thumbs up Sarven's document, or do you want to add some stuff?
... Did you want to mention authentication.

Sarven: Want to check with Christian?  Did this capture the concerns you had?

Christian: It's fine, we could maybe just merge our comments into one.  I wrote one as well.  Combined would be good.
 
Sarven: We could merge, but I didn't feel comfortable with the text you had in the first two paragraphs.  Do we need to repeat what the charter says?

Lola: Suggest Christian and Sarven work together on a resolution.

### [design-reviews#1119: Digital Credentials API](https://github.com/w3ctag/design-reviews/issues/1119) - @martinthomson, @matatk, @toreini, @lolaodelola

Lola: Matthew and Ehsan have a nice list of questions.  I haven't given this a lot of time.  

Martin: This is not an implementable spec.

Lola: Marcos, is there time pressure on this spec?  Can we table until Hong Kong?

Marcos: There is no time crunch on the implementable question.  The pressure is with respect to sites adopting it.
... We should get the no-papers (whatever it is called) out.  WaPo put out an article on the technology, with some inaccuracies, but very interesting to see what people are saying.  The no-papers document gives a good technical foundation and explains some of the dangers from a few perspectives.
... At the same time,... With Google, they are doing ZKP stuff with adult providers.  At least they can't identify people (in theory).  Some sites see a drop in visitors when they comply, others - who are ignoring the law - see huge increases in visitors.  This doesn't change content consumption habits.  VPNs usage skyrocketed.  This is important to be out there, because it does provide a knowledgeable perspective on the technology and the possible implications.

Lola: Might agree about unimplementable.  Should we wait until after Hong Kong.  Not going to change much in the meantime.

Marcos: Lots of difficulties getting algorithms from the WG.  "Why can't we just list what it can't do?"  That's not how computers work.  Maybe we'll have more in ~two weeks.

Lola: We can discuss what to do F2F.

### [design-reviews#1143: [wg/png] PNG Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1143) - @christianliebel

Christian: charter looks OK to me.  Jeffrey is concerned that the new compression algorithm is not backwards compatible.  Should they introduce a new media type for that?

Martin: I think Jeffrey is entirely right.  If you can't consume the content without new code, it's a new format.

### [design-reviews#1142: Incubation: FormControlRange - Live ranges for `input` and `textarea`](https://github.com/w3ctag/design-reviews/issues/1142) - @csarven, @matatk

Aside: I updated the title of the issue above because Cryptpad's markdown parser messed up the rendering of the remaining text - Sarven


Sarven: Review https://github.com/w3ctag/design-reviews-private-brainstorming/issues/197#issuecomment-3248284375
... I'm satisfied with this.  The important parts, that they should cover, are OK.  They are shuffling how things work, adding an abstraction in order to add the new stuff.  All fine.  They cover what will be unavailable or do not apply to form control range.  You might get the sense of the length of a password field.  `<input type=text|password|url|tel>` won't be covered.  Understand the password thing, but the text didn't make sense to me.  The idea is that the value space should be able to find the location of terms and whatnot.  Good that passwords are not included; I don't understand "text" being excluded that way.  Seems like a mistake.  Solves a real need.  Improves on workarounds that people use.

Lola: Comments reads.

Matthew: Like Sarven's comment.  I noticed the image in the explainer is broken.  Maybe there is a mockup, because it's not there.  Couple of things: assistive tech potential benefits.  They don't mention a11y in the explainer.  Because this is so tied to user input, they should be encouraged to put that in the explainer even if there are no impacts (or only positive ones).  They should make it clearer.  If there are no privacy concerns, is there some fingerprinting surface here?  Not sure.  It would be nice if it would be more explicit about why those concerns aren't there.  One thing that we've been encouraged to ask for.  Maybe we can also ask them how their API might be abused.  (Two images are broken in fact, not just one.)

Lola: Maybe ask them to fix the images and address abuse cases.

Matthew: and a11y use cases.  Are we okay saying there are no privacy concerns.  The live one makes me think it needs more thought.

Sarven: I think there are concerns, but it looks like their design is trying to work around them by disallowing methods or disabling for passwords, that was my impression.
... A function like getBoundingClientRectangle is available, but the context is about the value space, which is disabled for passwords.  If that is the case (and I understood correctly), I can't see how this would be abused.  It won't be available.

Matthew: The privacy concerns sections says "nope".  Maybe they can reassure people there.

Sarven: They should acknowledge these concerns and point to the mitigations.
... Another example was including the textarea could include script strings.  If that is somehow exposed to the API, that could be an issue.  Whether the form is working in a way that filters all that, how the script might be exposed, but that is another example that could be mentioned.

Matthew: We've designed the platform to make it hard to detect assistive technologies.  But it is still detectable through patterns of mouse movement, key press timing, and things like that. This might open up something.  Could you infer typing speed, determine what is pasted.

Martin: Sorry to say, we already lost the ability to hide that stuff.

### [design-reviews#1140: Incubation: `<geolocation>` element (part of PEPC)](https://github.com/w3ctag/design-reviews/issues/1140) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola

Martin: Suggest that we encourage them to continue.  Apple might have reservations about duplicative work, but this is in a good shape.

Marcos: Main concern was the duplicative aspect of this.  The positive is that it lets you recover from mistakes.  Deny is difficult to unwind.  This allows you to get back from that gracefully.  The thing was that this is less of a concern in Safari, because of different choices in prompting.  It is good because it becomes a nice element, but people might continue to use other things.  The surprising was the restrictions on the element, which seem arbitrary.  And difficult to implement.  Could be wrong.  Hiding/transparency all in the document, but need to be addressed and are quite tricky because they are trying to address click-jacking.  iOS has a swift element, which is meaningless, because it can be restyled into meaninglessness.  Is this going to be flexible enough for developers to use.  Different presentation might not lead to consistent implementation and be adapted to suit every website.  My sense is that this is going to fall apart because of the competing tensions.  

Martin: I also share reservations about restrictions on styling and placement.

Marcos: Starting from a form element, which is less ambitious, this could really be a thing.  I can also see some tweaks to make as a geolocation API editor, but minor stuff.

Marcos/Martin to put a comment together.

### [design-reviews#1139: WG Revision: Dubbing and Audio description Profiles of TTML2 (for 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/1139) - @matatk
### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://github.com/w3ctag/design-reviews/issues/1136) - @toreini, @lolaodelola

### [design-reviews#1041: Signature-Based Integrity.](https://github.com/w3ctag/design-reviews/issues/1041) - @martinthomson, @jyasskin, @csarven

### [process#45: Add an AI policy that we don't use AI to generate human-read text or summarize human-written text.](https://github.com/w3ctag/process/pull/45/files) - @jyasskin

Also see [PWETF#432: Humans are responsible for machine-generated content we post, and we need to attribute it honestly](https://github.com/w3c/PWETF/issues/432).

### Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
