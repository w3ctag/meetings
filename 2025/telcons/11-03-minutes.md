# W3C TAG Minutes - Week of 3 Nov 2025


## Breakout A (Asia / Australia / West America) - [2025-11-04](https://www.timeanddate.com/worldclock/converter.html?iso=20251104T030000&p1=43&p2=136&p3=195&p4=33&p5=248&p6=240)

Cancelled due to low expected attendance.

Present:
    
Regrets: Martin
    
Scribe: 

<!-- Agenda+ -->


<!-- PRs -->

### [user-agents#30: Don't export "web user agent".](https://github.com/w3ctag/user-agents/pull/30) - @jyasskin
### [user-agents#27: Rework Honesty section](https://github.com/w3ctag/user-agents/pull/27) - @marcoscaceres


<!-- Design Reviews -->

### [design-reviews#1093: Prompt API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1093) ([Github](https://github.com/w3ctag/design-reviews/issues/1093)) - @martinthomson, @jyasskin, @marcoscaceres

<!-- Other business --> 

### Find and assign TPAC sessions

### Make progress on documents

## Breakout B (America / Europe) - [2025-11-03](https://www.timeanddate.com/worldclock/converter.html?iso=20251031T150000&p1=43&p2=136&p3=195&p4=33&p5=248&p6=240)

Present: Jeffrey, Ehsan, Matthew, Serena, Christian, Lola, Yves, Sarven
    
Regrets: Hadley 
    
Scribe: Matthew

<!-- Agenda+ -->

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

*bump*

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

Yves: Is it OK to publish now, or is there anything that needs merging first?

Lola: OK to publish now; open PRs are still in discussion.

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

*noop*

<!-- PRs -->

### [user-agents#21: Describe how pieces of an application can be user agents.](https://github.com/w3ctag/user-agents/pull/21) - @jyasskin, @lolaodelola, @csarven, @xiaochengh

Lola: Waiting on my review.

Jeffrey: possibly also Sarven; he left comments.

### [user-agents#31: Publish the Draft Note](https://github.com/w3ctag/user-agents/pull/31) - @jyasskin, @ylafon

Jeffrey: Marcos left a comment on [PR #30](https://github.com/w3ctag/user-agents/pull/30) asking if we should export 'web user agent' at all, or just 'user agent' - does anyone have an opinion on that? (Both of those terms link to the same definition of this document - in web specs it makes sense to just use 'user agent'; we re-titled the document and realised that we needed to be more specific.)

Lola: I think we should use 'web user agent' in this doc. Eg.. some accessibility docs talk about user agents but are not referring to browsers.

Jeffrey: They've been extended to mobile OSes etc.

Lola: Even PDF readers.

...so I think we should be specific here. Does anyone else have any strong opinions either way?

Yves: I think it would be good to define 'user agent' in general.

Ehsan: From our conversations on the online harm doc, we discussed identity wallets as user agents as well. Are they 'web user agents' or just 'user agents'.

Jeffrey: 'user agents' becuase they're not browsing web documents.

Ehsan: I think there may be some confusion amgonst readers around 'user agents' and agentic AI.

Yves: Just the fact that we're discussing if we need to do clarification means we need to do clarfiication.

Jeffrey: Do we need to block publication as a Draft Note until we have the definition? I would say 'no', but wanted to check.

Yves: A Draft Note is a draft - so it is OK.

### [societal-impact-questionnaire#26: Exclusion Example](https://github.com/w3ctag/societal-impact-questionnaire/pull/26) - @lolaodelola, @csarven, @jyasskin

*bump*

### [design-principles#596: Recommend registries, and give some guidance on how to define them.](https://github.com/w3ctag/design-principles/pull/596) - @jyasskin

Jeffrey: Got back to this and Martin's comments - please review. Sketching what's different:

* Defined 'extension point' - there's no definition in anything in specref
* Broke out what extension points ought to do - mostly from an RFC that Martin pointed to, and I consolidated another part of this expectation and said:
    - if you can, require a spec; if you can't be that disciplined, first-come, first-served may be sufficient. Maybe URLs could be OK, but they present extra risks compared to a registry.
    - You should have some defined in the spec.

...once we're happy with it, we should run it past the DID group, as they requested it.

Sarven: What sorts of registries do we have?

Jeffrey: DIDs have several documents that aren't called registries, but are registering extensions. There are some other W3C documetns that link to IANA registrations; they may come across as registries. Then there's the whole question of: when is JSON-LD correct vs. doing registries of names? It's not to say 'be sceptical of JSON-LD' but rather 'when you're doing registries, an extension is often better than a URL'.

<!-- Design Reviews -->

### [design-reviews#1128: Other Spec Review: Extend CSP script-src hashes](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1128) ([Github](https://github.com/w3ctag/design-reviews/issues/1128)) - @toreini

Pending external feedback (Ehsan posted comment).

### [design-reviews#1136: Incubation: FedCM: Support showing third-party iframe origins in the UI](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1136) ([Github](https://github.com/w3ctag/design-reviews/issues/1136)) - @toreini, @lolaodelola

Lola: recapping prior discussion: we wanted to ask them for an explainer, and ask them for more concrete examples.

Ehsan: can draft something in private repo. Could you check out their last response? They seem to conflict somewhat with each other. I'll draft somethihng based on what we discussed.

Jeffrey: Is it clear they're asking about _adding_ an extra domain?

Ehsan: Having 3 helps, but not clear on why in some cases they're going to make it 2. Despite the confusing title, I think the text is clear they want to add something, but in some cases they're proposing not to add the third. I don't think the branch with only 2 will help users.

Jeffrey: I'm not sure that question has come through - the question of 'why not always show all 3'.

Ehsan: I mentioned it in one comment

Lola: point 2 - but I don't think, from their responses, that they've picked up on that. I think it's worth emphasizing why 2 rather than 3 origins is an issue. Looks like they're not clear on what's important to us, and vice-versa. Clarifying would be good in next tommend.

Ehsan: I think Jeffrey's point about confusing title should be emphasized too. I'll draft something.

Lola: I'll check what you mentioend about their last two comments.

### [design-reviews#1157: WG New Spec: DID Resolution](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1157) ([Github](https://github.com/w3ctag/design-reviews/issues/1157)) - @jyasskin, @lolaodelola

Jeffrey: waiting for me to review the second half, and for them to respond to the review comments (which they opened up into separate issues).

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Matthew: Last thing here is me saying I would write a comment, so I will do that.

### Other business

#### Publishing things

Sarven: Can we publish societal-impact, web-user-agents, prevent-credential-abuse?

Lola: web UAs and societal impact will be published this week (as drafts).

Jeffrey: We didn't discuss prevent-credential-abuse, but if this group is happy with it, then let's tee it up and double-check with Martin.

Lola: Last time we talked Martin thought he'd addressed all the concerns.

Yves: I need to have consensus recorded for web-user-agent. For prevent-credential-abuse it's a Finding - we just have to ensure that it's publishable (from Martin). Can even publish it during TPAC.

Jeffrey: For web-user-agents we have consensus recorded in Hong Kong, with the caveat that we wouldn't export the term.

Sarven:  https://github.com/w3ctag/user-agents/pull/31 , https://github.com/w3ctag/societal-impact-questionnaire/pull/30

Sarven: I did something similar for societal impact.

...Do you take the changes happening to index.bs/index.html and create a static version out of that? In societal-impact I made a minor update that links to the Editors' Draft and mentions the shortname.

Yves: I'll manually pull that change to my local version for publication. Then we can merge your PR after that.

#### TPAC scheduling

Matthew: *gives update on tool; ask about announcement*

Jeffrey: Coul;d annoucne via chairs' list.

Matthew: will draft comment

#### prevent-credential-abuse

##### [Separation between privately issued credentials vs govt issued identity credentials · Issue #53 · w3ctag/prevent-credential-abuse](https://github.com/w3ctag/prevent-credential-abuse/issues/53)

Lola: high-level vs low-level of assurance (gov-issued ID and cinema ticket). Martin argues the same issues are present with both, and the more important is the government one, but as they're the same issues, we don't need to make a distinction.

Jeffrey: I feel like because someone was confused about it, we should mention it, even if the mention says 'this applies to both'

Lola: Agree. I see someone raised an issue.

Yves: For private identiies you might provide fake info when registering. That might be the limit that makes them different.

Ehsan: I agree with both comments. I thihnk the baseline should be the weaker/less-assured identity wallet (private); then the government wallet will be more protected than that. But we could all agree that the bsaseline has certain characteristics. If we all agree on the baseline, then more secure than that is better, but not important to discuss.

Jeffrey: The EU is requiring that wallets attest to their app identiy. Usually something we don't like on the web, but this is required by regulation. We could split the two levels based on this.

Sarven: Why do we not like this?

Jeffrey: It puts the web site in charge of which user agent the user can choose.

Sarven: ACK - but wondering if we have links to prior discussions on this?

Jefferey: There's something about attesting WebAuthn keys, which is narrower than attesting UAs. Web Environment Integrity (WEI) proposal from Google was received negatively. Don't know if TAG or W3C has a document on this.

* https://en.wikipedia.org/wiki/Web_Environment_Integrity
* https://www.imperialviolet.org/2018/03/27/webauthn.html#attestation

Ehsan: One more thing for the private identity wallets. There is some legal aspect to privately-owned identities; they can be representing private businesses as well; they're not restricted to individuals. Not sure if it will create confusion if we discuss this.

Lola: Do private companies' identities face the same issues as individuals' in the context of this document? Can they be affected by the same issues?

Ehsan: In the EUID it's explicitly mentioned that business identities should be part of digital identity as well. I don't know if they're using a different wallet for that purpose, with different expectations, or not.

Lola: What are we suggesting to Martin? Listing all the types of IDs?

Jeffrey: I don't think we should; we should mention government-issued and not.

##### [Discuss tradeoffs of using W3C-specified vs. implementation-define approaches for digital credentials
](https://github.com/w3ctag/prevent-credential-abuse/issues/54)

Jeffrey: The argument is that, from Chrome, the browser API needs to be loose to capture the market, but others like Martin are saying that we should make the browser API do the right thing, regardless as to whether it hampers adoption. I think I agree with Martin that we don't need to - we haven't said how to come down on any of the questions about concrete API - we are saying what the goals are. So I don't think we need to mention it.

Lola: I am wondering if we do need to mention it somewhere - if not this document, then another. The things that Rick is speaking to, are they already addresed or defined in principles documents.

Jeffrey: One of the arguments is whether the W3C spec says what's going on, or defers to the OpenID spec, e.g. with respect to the registry being loosely defined. With the registries design principle, we're pushing that such a registry should exist, which would have strict requirements. So we do address things in some places, but it's scattered.

We're also going to have disagreement in the TAG because I think we (W3C, browsers) should compete with native apps, and Martin and Marcos thing we should not.

I'll bring it up in Breakout A.

## Breakout C (Europe / Asia / Australia) - [2025-11-06](https://www.timeanddate.com/worldclock/converter.html?iso=20251106T090000&p1=43&p2=136&p3=195&p4=33&p5=248&p6=240)

Present: Lola, Marcos, Ehsan, Matthew
    
Regrets: Martin, Hadley 
    
Scribe: Ehsan


<!-- Agenda+ -->


### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola
 Skip for now

<!-- PRs -->

### [user-agents#28: Add loyalty guidance for facilitating users switching UAs](https://github.com/w3ctag/user-agents/pull/28) - @csarven
Skip for now

### [societal-impact-questionnaire#24: Misuse example](https://github.com/w3ctag/societal-impact-questionnaire/pull/24) - @lolaodelola

Skip for now
### [design-principles#597: Handle non-fully-active documents (and destroyed execution contexts)](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon

Marcos: not got a chance to update yet.
Lola: since the turn-out is not a lot, the best is to look at the list and check if there is anything required to update.


<!-- Design Reviews -->

### [design-reviews#1041: Signature-Based Integrity.](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1041) ([Github](https://github.com/w3ctag/design-reviews/issues/1041)) - @martinthomson, @csarven
### [design-reviews#1158: ViewTransitions: waitUntil() method](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1158) ([Github](https://github.com/w3ctag/design-reviews/issues/1158)) - @christianliebel, @lolaodelola
### [design-reviews#1149: [ig/webai] Web&AI Interest Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1149) ([Github](https://github.com/w3ctag/design-reviews/issues/1149)) - @hadleybeeman, @christianliebel
### [design-reviews#1140: `<geolocation>` element (part of PEPC)](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1140) ([Github]

Matthew: we need to have a discsssion on that during TAG. I have put it on the GitHub. Let me have a look at my calendar.

Marcos: this is going to be on Thursday (?)

Matthew: can anyone check?

Marcos: where was it?

Matthew: W3CTAG/TPAC-meetings

Matthew: it is issue #5, there might be an issue with the calendar. We got Martin, Jeffrey, Marcos, Hadly, Lola assigned to it.

Lola: I need to figure out my TPAC aim.

MAtthew: will do that on Monday.

Marcos: will do geolocation in general and then discuss the geolocation element.

Matthew: WebApps and DAS are good in providing agenda. This agenda is good so thanks.

Lola: sounds like there is not much to discuss. Anything to discuss?

Marcos: The permission model to the geolocation is my concern but I don't feel too strongly about it

Lola: do you want to post your comment? Considering Martin's comment.

Marcos: not sure, Mark West wanted us to post something. Let me check.... I can do that.

Lola: Thank you.


(https://github.com/w3ctag/design-reviews/issues/1140)) - @martinthomson, @marcoscaceres, @matatk, @lolaodelola
### [design-reviews#1161: WG New Spec: RDF 1.2 N-Triples](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1161) ([Github](https://github.com/w3ctag/design-reviews/issues/1161)) - @csarven
### [design-reviews#1160: WG New Spec: RDF 1.2 Semantics](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1160) ([Github](https://github.com/w3ctag/design-reviews/issues/1160)) - @csarven
### [design-reviews#1159: WG New Spec: RDF 1.2 Concepts and Abstract Data Model](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1159) ([Github](https://github.com/w3ctag/design-reviews/issues/1159)) - @csarven


FedCM update (1136):

Matthew: Discussed in Plenary last night, decided to have it in the agenda for today.

Lola: I remember I had to look at the comment.

Ehsan: I submitted my review last night, Jeffrey got some questions. So not ready yet.

Lola: Let me have a look.

Lola: They seem to they talk past you. They are not realising your concern about the three URLs. I do wonder about the top-level FedCM directly, if this is the case, what is the point of all of this?

Ehsan: My issue is the permission claim from the RP and then matching from the IdP. I believe there is a chance of injection or being malicious so all three items should be shown. This is authentication ceremony so better be crticial on all detail, show everything to the user and let the user decide.

Lola: It is healthy to be cautios as it is authentication. Let me look at your draft response.

Lola: I think Jeffrey's question is particularely potenant(??) on the attack is possible. Are you saying that the attack is possible?

Ehsan: ???

Lola: I think we need to frame that serious example, I think the attack likelihood is low so maybe opt in for accept with concern. 

Ehsan: Maybe Serena can help?

Lola: Maybe phrase the question. "What instances show two URL's are shown? and why is that the case and why all three should be shown? anyone has problem?

Matthew: no othing from me. It would be a good idea to talk at TPAC with the people there. Will try to do that.



## Plenary Session - [2025-11-05](https://www.timeanddate.com/worldclock/converter.html?iso=20251105T220000&p1=43&p2=136&p3=195&p4=33&p5=248&p6=240)

Present: Jeffrey, Matthew, Yves, Ehsan
    
Regrets: Martin, Hadley, Christian
    
Scribe: 


<!-- Agenda+ -->

### [obsoletion#10: Reconsider W3C Recommendation status of XSLT 2.0 and XSLT 3.0](https://github.com/w3ctag/obsoletion/issues/10) - @jyasskin, @csarven

Yves: It's normal that we're in the loop here.

Jeffrey: We should decline to Obsolete these RECs.

Matthew: The person said there's 1 implementation?

Jeffrey: He's wrong.

Yves: And the security issue is in all XML.

Jeffrey: I'll draft a closing comment in Slack. We can approve and post it at the start of TPAC.

### [design-reviews#1138: [wg/webextensions] Web Extensions Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1138) ([Github](https://github.com/w3ctag/design-reviews/issues/1138)) - @csarven, @matatk, @toreini, @christianliebel

Needs Sarven.

Jeffrey: I don't think the TAG should take a position on https://github.com/w3c/charter-drafts/pull/711#discussion_r2455480993, but we need Sarven to really decide that.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Needs Marcos.

### [design-reviews#1015: Payment link type in HTML](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1015) ([Github](https://github.com/w3ctag/design-reviews/issues/1015)) - @jyasskin, @csarven, @maxpassion

Has a TPAC session: https://github.com/w3ctag/tpac-meetings/issues/16

### [design-reviews#1092: Web Authentication Immediate Mediation](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1092) ([Github](https://github.com/w3ctag/design-reviews/issues/1092)) - @martinthomson, @jyasskin, @marcoscaceres, @toreini
### [design-reviews#1119: Digital Credentials API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1119) ([Github](https://github.com/w3ctag/design-reviews/issues/1119)) - @martinthomson, @matatk, @toreini, @lolaodelola

### [design-reviews#1093: Prompt API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1093) ([Github](https://github.com/w3ctag/design-reviews/issues/1093)) - @martinthomson, @jyasskin, @marcoscaceres

Draft comment: https://docs.google.com/document/d/1gqgMj_gQdk23_AaIYRlQ1nIYYQgOdVzvsDhJjJpTfMQ/edit?tab=t.0

Jeffrey: We're close to consensus on this. I have a few tweaks, but nothing big. Need Martin to also review before we post.

### [user-agents#30: Don't export "web user agent".](https://github.com/w3ctag/user-agents/pull/30) - @jyasskin

Need Marcos to verify that this is what he wanted in Hong Kong.

Jeffrey: We could decide to merge this, since none of its discussion is about the change itself.

Consensus to merge this.


