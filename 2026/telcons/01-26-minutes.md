# TAG Minutes - Week of 2026-01-26

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2026/telcons/01-26-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.


## Atlantic Breakout (America / Europe) - [2026-01-26](https://www.timeanddate.com/worldclock/converter.html?iso=20260126T140000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Matthew, Ehsan, Christian, Lola, Dan, Jeffrey, Yves, Hadley
    
Regrets:
    
Scribe: Matthew

### [process#49: Review Associates program](https://github.com/w3ctag/process/issues/49) - @jyasskin, @hadleybeeman, @lolaodelola

Matthew: I have an increasingly small PR as the pieces of it have been addressed. In good shape.

### [explainer-explainer#3: Terminology: "Non-goals" meaning](https://github.com/w3ctag/explainer-explainer/issues/3) - @matatk

Matthew: Saw that Martin replied, and I hadn't read his reply. We'll address it async.

### [design-reviews#1167: WG New Spec: Scroll-Triggered Animations](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1167) ([Github](https://github.com/w3ctag/design-reviews/issues/1167)) - @matatk, @heisenburger, @lolaodelola

Matthew: Same as last week: APA and my feedback will be coming soon.

### [societal-impact-questionnaire#18: Simplification of Intro Material](https://github.com/w3ctag/societal-impact-questionnaire/issues/18) - @csarven, @lolaodelola

bump

### [user-agents#29: Write an introduction](https://github.com/w3ctag/user-agents/issues/29) - @csarven

bump

### [user-agents#20: Meta: Make progress on this document.](https://github.com/w3ctag/user-agents/issues/20) - @jyasskin, @csarven

Jeffrey: We have one issue on the agenda - would anyone like to consider any of the others?

Lola: WebViews (issue 36)

Jeffrey: This might be covered by the UAs as software components section - will make that comment and agenda+ it so we can check async.

Hadley: Sounds like we don't have consensus on this.

### [societal-impact-questionnaire#2: Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2) - @lolaodelola

bump

### [societal-impact-questionnaire#20: Meta: Make progress on this document](https://github.com/w3ctag/societal-impact-questionnaire/issues/20) - @csarven, @lolaodelola

bump

### [explainer-explainer#31: Meta: Make progress on this document](https://github.com/w3ctag/explainer-explainer/issues/31) - @jyasskin, @matatk

bump

### [design-reviews#1146: Incubation: Proofreader API](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1146) ([Github](https://github.com/w3ctag/design-reviews/issues/1146)) - @matatk, @toreini, @christianliebel

Christian: This is unblocked now because it was depending on the Prompt API review. We concluded that review with lack of consensus. The question is what do we want to do with this one? We discussed before and said we're not experts in that domain. We could continue with that approach, or bring it bak for more discussion.

Lola: What was the reason on Prompt API?

Christian: It was regarding the issues around downloading the model.

Hadley: Another option is to find an expert we know, maybe a former TAG member, or someome who is an expert.

Lola, Christian: ACK.

Ehsan: The download issue was previously discussed in TAG and we had given positive feedback - in the Translation API.

Christian: That's true and also shares API shape with Prompt API. I might give that a read and come back next week.

Ehsan: I have a review for proofreader but haven't shared it yet as it was on pause, will share it by end of week (private thread).

Lola: I think the API was Web Speech (Translation was 2024). Jeffrey praised that they had removed the cloud only requirement.

Christian: We can review your text, and also ask a domain expert, or former TAG member.

### [design-reviews#1176: Incubation: @supports at-rule](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1176) ([Github](https://github.com/w3ctag/design-reviews/issues/1176)) - @christianliebel, @lolaodelola

Lola: Both comments (for this and 1186) LGTM.

Christian: Thanks; will post.

### [design-reviews#1186: Other Spec Review: named-feature() function for CSS @supports](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1186) ([Github](https://github.com/w3ctag/design-reviews/issues/1186)) - @christianliebel, @lolaodelola

(see above)

### [design-reviews#1181: WG New Spec: Web Sustainability Guidelines](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1181) ([Github](https://github.com/w3ctag/design-reviews/issues/1181)) - @jyasskin, @csarven

Jeffrey: In addition to my detailed comments I was wondering if we wanted to say something about regulation being an appropriate way to push the community towards sustainability, to avoid the situation where individuals opt to be more sustainable, at some cost, but others do not, and do not experience the cost.

Lola: I think there are concerns about talking about regulation because of the risks this poses.

Hadley: TAG sometimes talks about current regulation, which is more than other parts of the W3C can do. Talking about areas where regulation may be helpful is an easier thing to do - e.g. if email spam was foreseen, raising the concern that that area may need regulation would've helped.

Jeffrey: Will work on something. Think it's worth sending the bulk of it. Need to know if this is a TAG position or not before I post it - please review.

*Returning to this after completing the agenda...*

Jeffrey: Main thing is to check that TAG agrees (or not). It is unclear as to whether the current set of guidelines are the most imporatnt ones. Some seem to be too low-impact to include.

Hadley: Sounds like this has been a long-running conversation.

Jeffrey: They have been talking about it for a while, and I've been reviewing it for a while.

*Discussing the point on monopolies specifically...*

Hadley: Ultimately monopolies end up with no competition and thus a lack of improvements. But up until that point, they may be investing more than others in their services.

Jeffrey: They hadn't really discussed this when I brought it up.

Lola: I agree with Hadley that a lot of the comments in your review are editorial. The document they've given us to reiew is quite long - I don't think we should be doing their editorial review, but we should let them know that they'll need to do that.

... I do think it's worth asking them how they got to this list. I am not sure what we'd be looking for as TAG.

Hadley: I was wondering that too. Relation to architecture of the web. I would've said what Lola just said before you did the copy editing. For what you've done, fine to share it with them. But it doesn't need to be our role in reviewing documents.

Lola: I wonder if they brought it to us because of the relationships with documents we've written, such as societal impact.

Matthew: I think we have consensus that it's a good thing that the web is human-editable (plain text formats etc.) but that represents an architectural choice with sustainability consequences (of some amount). Last year we talked about adding zstd to the platform, which was a no-brainer due to the improvements it brings vs. the overhead on UAs to ship it etc. We make lots of trade-offs around formats. I read that the web needs to become both vastly more resliiant, and consume far less power in future. We make decisions that have ramifications here too. I think we're all making architectural decisions with sustainability implications a lot of the time.

Lola: As the TAG, what feeedback would we be giving - do we know enough to know how resources are used in the networking of things. Do we know enough to comment on some of the specific things that they are advising, good or bad. Should we be asking sustainability experts to chime in and review this document (similar to the AI APIs above).

Jeffrey: This is the group of sustainability experts. We could go outside of W3C to people who aren't participatinog to make sure they asked for review on the appropriate set of things.

... To Matthew's comment: when designing the architecture of the web, we have to think about the goals we have. This group is adding a new set of goals. So this is a bit different to what we usually review.

Hadley: My concern re architecture was to find the parts that are relevant to architecture (of which I expect several). Also we added [2.9: The web is an environmentally sustainable platform]
(https://www.w3.org/TR/ethical-web-principles/#sustainable) to the Ethical Web Principles.

Matthew: Sometimes our architectural goals will conflict. A sustainability goal might conflict with an accessibility or security goal. Do we need a priority-of-constituencies-type thing to prioritize? Is it the priority of constituencies itself? We should consider how to arbitrate when these conflict.

Hadley: re efficiency, a lot of what we put in Ethical Web Principles, and what we ask for in our design reviews, etc. is to go against efficiency. It's very efficient to ignore accessibility, or internationalisation, or to create a feature by yourself and not bother with standardisation at all. We often strive to go against efficiency to build a better web.

Ehsan: Usability is at the centre of that, if you've got the most efficient system but nobody uses it, you have not got an efficient system. Similar with security - the most secure system that nobody uses isn't secure. We have a balance.

Lola: Agree we are pushing for the balance. I'm still stuck on the question of, as TAG, what can we advise? I think the experts are coming to the wrong group with this question. With charters, we're not reviewing them in the same way as the Team or other groups will review it. We're reviewing it in ways that we know about, e.g. we can connect groups that are solving similar problems but don't know about each other. I feel like we're not the right people.

Jeffrey: On the one hand, they're coming to us because they're doing wide review, and we're part of the process. The question that I'm trying to answer is: 'can I use this in design reviews?' and my current answer is 'no' - so I'm giving them feedback on those lines.

Lola: That contextualisation helps. I'm wondering if they consider this document as one that can be used in design processes. We want people to think of these things as they're developing this technology. Who's the audience for this document? Is it spec authors? How can we use this document to hold the spec authors to account?

Hadley: That makes sense. If their plan is to make this a W3C Statement, then whether we are doing the enforcement, or it's being done through charter reviews... It will be done one way or another. 

Jeffrey: They're thinking about becoming a horizontal group eventually. Like the others, they need to prove themselves first, but that's a long-term goal.

Lola: Trying to understand how this document could be used in design reviews... I'd like to know if that's something they're comfortable with, or intend.

Hadley: I agree that it might change their editorial slant. But even if they don't intend us to use it, if they're planning to make it a statement, the outcome is the same. Flipping it around, if someone was going to write a key technical document for the community and we didn't have any input into it, how would we feel? We need to be involved even if we won't be enforcing it.

Jeffrey: Been trying to summarize this part of the converastion into a couple of paragraphs at the start of the Google Doc - does that capture what we are saying?

Hadley: I'm not sure if this group would be aware of the design review process and thus not fully understand the meaning behind the additions.

Jeffrey: Tzviya is in the group, so understands the process.

Lola: ____ opened this issue and is a staff member.

Yves: HIdde (AB member) is involved too.

Lola: We could ask if they need clarification on this. Do you feel like you have enough?

Jeffrey: Need review from TAG of the detailed comments. Then I can post.

Hadley: would it help to put the paragraphs at the top in as TAG and the rest as you?

Jeffrey: I'd like to check the TAG agrees with all the comments.

Lola: I can get feedback to you

Jeffrey: We may want to let people read this for 5min

*group works on the google doc*

Lola: Re Greenwashing, it's described as a threat - does it make sense to connect this to threat modelling work going on in W3C?

Jeffrey: It's a threat to the authors of this document, so not something spec authors need to be worrying about very much.

... I'll apply the comments to the doc and then ping the Slack.

Lola: Reminder that Nick Doty is joining us this week for plenary. We will probably be talking about f2f topics at Plenary as well. If there are docs that you want to spend time working on, or topics we haven't spent enough time on between Hong Kong and now, let us know.

Jeffrey: Plenary specifically is about age verification and requriements, and how that should affect the architecture of the web _____ will also be there.

Lola: ISO just made their age verification stuff public.

### [design-reviews#1095: Canvas Text Metrics for Editing, Art and Design](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1095) ([Github](https://github.com/w3ctag/design-reviews/issues/1095)) - @jyasskin, @matatk, @dandclark

Jeffrey: Seems that adding a new path to the info would result in adequate performance, so we would not change our stance on this.

Jeffrey/Matthew/Dan to draft a new comment.

## Pacific Breakout (Asia / Australia / West America) - [2026-01-27](https://www.timeanddate.com/worldclock/converter.html?iso=20260127T040000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Jeffrey, Dan, Marcos, Martin

Regrets: Xiaocheng

Scribe:

### [design-principles#597: Handle non-fully-active documents](https://github.com/w3ctag/design-principles/pull/597) - @marcoscaceres, @ylafon, @jyasskin

Dan: https://w3ctag.github.io/bfcache-guide/ covers the same area as Marcos' new section, but in some ways does a worse job of saying how to "do nothing" on bfcached documents. Should we merge the sections?

Marcos: There's no way to distinguish destroyed from bfcached documents. My sense is that the first is developer-initiated, and the second is user-initiated. BFCached cases are generally not observable. They're basically the same with slight differences. If you're watching media, you hit back and forward, the media pauses but shouldn't reset. Common case with accidental back clicks or navigations. Can get weird. BFCache model is extremely fragile vs the model where the developer deliberately destroys the document. e.g. in Apple Pay's payment sheet, it works as a modal, where the user can't go back, but the underlying document can navigate itself, which aborts the sheet. There are subtle differences. A spec author can't say "if the page is in the bfcache."

Dan: Makes sense. I was thinking of an alternative way of framing it: one section for non-fully-active documents. Then at the end, "here are the ways you might end up with such a document."

Jeffrey: Think it'll be fine to merge Marcos' change, and maybe later come back and revise the BFCache section.

Jeffrey: There's a question for Rakina, but I think we can merge this and update it in another PR if Rakina comes back wanting a change.

Marcos: I've merged the changes.

Jeffrey: I think this is ready to merge then.

### [design-principles#610: chore: fix bikeshed warnings](https://github.com/w3ctag/design-principles/pull/610) - @marcoscaceres, @jyasskin

Jeffrey: I merged this as an editorial change.

### [user-agents#36: Web views](https://github.com/w3ctag/user-agents/issues/36)

Jeffrey: I think we agree, and my text just wasn't direct enough. What words would help?

Martin: You're saying you can build web-platform-like things with WebView libraries. Sometimes it's just used to render stuff. Other times it's used to make something that can browse. Then the application becomes a UA.

Marcos: Example of Facebook ... Instagram one is very user-agent-y. Does autocomplete of forms through stuff it knows through FB. 

Martin: Can do payments, etc. Full-fledged user agent.

Jeffrey: Question is just how to say that.

Marcos: "However, if they do stuff on behalf of the user, they become a user agent" ... the software wrapping the webview. 

Martin: In some cases, if it just lets the webview be a webview. They have a lot of capabilities.

Jeffrey: Think payments just trigger a callback to the embedder. But you don't have to implement that to allow the WebView to browse 3p content.

Marcos: In WebKit, there's a main thread concept, and that's the app view. To invoke WebAuthn and so on, you have to tie them to the network process. So "network process" gets entitled to do UI stuff. WKWebView has a bug to support WebAuthn through the network process. So you can drop in Facebook, etc, and be able to do WebAuthn without an entitlement. Just by embedding it, you get the powerful APIs. Can do payments just with the webview.

Jeffrey: I think I still think that you need 3p content to be a user agent. Just autofilling or paying into 1p content isn't enough.

Marcos: There are powerful features available on the web.

Jeffrey: True for native apps too.

Martin: Your line is that once you cross outside the domain of control of the application developer, that's the line. Perhaps it's limited, but there is user agency in interacting with the one service through its own application. E.g. the insurer, the app acts as your agent by changing your insurance for you. But it's narrower, so maybe it's a reasonable dividing line. If the insurer does what a lot of sites do and embeds 3p content, like how you embed a payment processor, does that cross the line? But then where is the line?

Jeffrey: Good point that there are cases where an app embeds its service provider as a web page, and it shouldn't become a UA because of that.

...

Martin: Good to be frank about the bounds and limitations in what we're saying.

Jeffrey: How can we write a PR for this?

Martin: Point is clear enough ont he libraries not being responsible, but need to expand on embedding app being responsible. 
1. Sometimes just embedding one of these libraries causes the app to become a user agent, even if that wasn't their intent. That's a warning.
2. The bright line, about external content being one way that embedding the capability taking on the responsibilities. Might not be the only way. Accessing powerful capabilities like payment might cause it to cross the line.

Martin: Power capabilities might cause the application to take user agency, but might not be a "web user agent."



## Plenary Session - [2026-01-28](https://www.timeanddate.com/worldclock/converter.html?iso=20260128T060000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Martin, Matthew, Christian, Marcos, Yves, Jeffrey, Ehsan, Tara Whalen, Nick Doty, Rick Byers, Ben VanderSloot

Regrets: Hadley, Sarven

Scribe: Martin

### Age restrictions on the Web

Nick Doty, Ben VanderSloot, Tara Whalen, and Rick Byers joining us

Nick introduces self and concept.  Lots of policy-maker proposals that seek to verify identity and age and restrict content based on age.  A lot of those are harmful for privacy and free expression.  We would like to explore the space.  Maybe consider technology that is less invasive and more effective.  Trying to get help.
...We had a workshop with this recently.  Report draft is out.  Wanted to talk about one specific solution: age range signaling.  That has been mandated in some jurisdictions.  Platforms have implemented some version of that technology.  Hopefully the TAG can provide input on the design and maybe where this can go if it is worthwhile.
...Parents and guardians want to help children avoid unwanted content (this is a privacy goal)
...Policy makers want to protect children from abuse, but this includes targeted ads, age-inappropriate content (often adult), prevent messaging with adults, and protection from design approaches (endless scrolling, late-night messages, many thing).  So this is also behavior.
...Users want to access content on the web, privately.  Don't want to be tracked everywhere.
...Unstated goals might be involved.  I won't go into those into much detail, but there are going to be some abusive guardians who seek to repress certain content.  Governments who want to limit free expression.  Commercial competion might seek to use controls.

...One option is to include an age hint (client hint?), volunteered, configured by the admin of the device.  This might be the choice of the adult owner.  Includes some discretion.  Parents can set ranges based on their understanding of children.  Similar to Apple's Age Range API proposal.  Google might have something deployed in some jurisdictions (?).  California has passed a bill requiring this, and some others.
...Volunteering an age range.  We should not send this promiscuously.  Not appropriate for most interactions.  Won't know which sites will need it.  Sites should be able to ask for the information.  We could go beyond that to get affirmative declarations from sites that they are going to use the information, what information, and include not selling the information. Some sites want to be proactive about this.  They might only care about one range and so can declare that.  Sites can adapt their content to age ranges so might want richer information.  A public declaration can identify what ranges are relevant and what promises they make about how they use that inforamtion.  Public accountability, not something that we can enforce technically.

Yves: Is it 18+ or adult per local rules?

Nick: Early discussion.  Feel free to propose answers and challenges.  One situation is that even though jurisdicitons have a desire to have age ranges, they won't agree on what the brackets will be.  Not likely to have all agree.  Different rules will happen.  It is likely that jurisdictions using this will use numbers, not labels.

...There are different architectures and trade-offs.  Talked about some at the workshop.  From most to least: biometrics and pictures of credentials.  Digital credentials can reveal all or some identifying information.  Age range signaling is middling.  Site labeling has been pursued in the past.  CDT once worked on Platform for Internet Content Selection (PICS), which partly helped convince a Supreme Court not to ban adult content.  These options might be used in different ways.
...THere are privacy risks and exclusion, discrimination, and censorship.  Age ranges might not have as much identification and gives guardians control, which could be advantageous.
...Timelines are rather urgent.  Lots of quick movement.  Workshop in DC today with a goal of broadening this.  Potential for a less harmful approach needs to be a real alternative soon.  Before we end up with a biometrics/credentials to access all sites. 
...Looking for feedback on where we are in the design space and what venues we should use.  This will require standardization, so where?

Lola: You mentioned parents being able to set age ranges for kids.  Have you thought about mechanisms to prevent children from overriding that.  Why can't the child set a different value.

Nick: Circumvention by children comes up a lot.  Applies differently in different situations.  Young children might not be likely to change a setting.  Others are more concerned about a 17 year-old.  17 year-olds will circumvent virtually any solution being talked about.  Platforms like this are willing to have some sort of control.  It is non-trivial to change parental controls.  Not just a field or a toggle.  You have to get administrator access, switch profiles, or something else.  To the extent that platforms have some controls, that might be relevant and useful.  Obviously, it is not guaranteed for a website: they won't know what is in place.

Rick: There is a spectrum of assurance levels.  Two clear points in deployment.  Browsers have content filtering features.  Safari might be best-developed.  Device owner can ask to filter out content.  Jurisdictions are requiring wallets with government credentials, that is hard to circumvent.  Do you have evidence that policymakers want another option?  Not sure if what you propose is more or less circumventable than content filtering.  What you have might be trivially circumventable by a browser extension (maybe).  Or do we risk offering them some false hope.  My personal greatest fear is that there is miscommunication with policymakers but then we are asked to constrain the openness of the web to meet the stronger requirements that policymakers really want.  If we find that another open source browser doesn't have the controls, do policymakers react by constraining what people can install?  What evidence is there that there is a demand for this.

Nick: A real concern, yes.  VPNs are very popular in the UK.  Clearly the next step is to restrict access to VPNs.  Maybe they haven't seen that the next step is DRM and total software control, but this is not hypothetical.  In terms of appetite, policymakers are not uniform.  No consensus position.  Reason for this is that there is evidence for demand, like California.  Lots of bills were discussed, but the one they passed was about age ranges, not identity collection.  AB1043 for those following.  They are also talking about other means.  They want an age-range signal, they also want to require other signals be used where those are available.  The site might know that the profile they have has extra information they can use.  They understand that this is imperfect and accept that.  Other proposals include stronger guarantees.  There is reason to believe that policymakers have some interest in this.  Yes, share concerns about circumvention risk.

Rick: Google's position on this is that the wallet-based approach is least-harmful.  My opinion on why is that it mirrors some of what we learned from DRM.  The hard stuff is isolated to a separate application.  Wallets are not open source.  They use attestations.  Those are high-level why that approach is generally least-risky.  For myself, not Google, there are mutliple points in the space and it is worth discussing those.

Marcos: Not including children in this discussion is terrible.  In Australia, we discussed the social media ban.  Most children get around the ban.  A range of hilarious things.  Instagram warn people first.  So they just change their age.  Some got caught out, so they did a face check.  Duck lips worked for some.  Makeup (frown lines) for others.  All of them are on social media.  THe site thinks they are all 20.  Parents helped them.  Zero impact because no child was excluded.  Very easy to get around the ban.  A lot of parents are annoyed at the government interfering with what kids want.  Need to consider that too.

Rick: We should expect parents who install identity documents on their kids phones, which might have far more harms than something like what Nick is describing.

Nick: We are obviously talking about more than just children.  This is affecting teenages and parents and we should include them in discussions.  We care about policymakers' stake as well. We need more active engagements.  Tara is tasked with doing more of that.  On parental involvement in circumvention, one way we can involve teenagers is to do empirical research.  Interview research with both teenagers and parents.  Both have talked about each helping the other circumvent.  Helps to have parents talk to kids about what is safe and this is a good opportunity to discuss.  Installing dodgy software or adult credentials on kids' phones is not good.  Age range signals might be helpful there.

Jeffrey: Want to talk about architecture.  The DC API allows sites to get cryptographic assurances.  That might be that the parent's credential is on the kids device.  The age range thing is an intermediate spot.  The device-owner and site cooperate to restrict what the user of the device sees.  Parental software has a way to do that.  I have 7&9 year-old kids.  We tried to sign up for music streaming and I said that they could be 16 for that service.  DC API couldn't help.  Regulators will need to decide what to accept.  Having more options available might allow them to make better choices.

Nick: I think that the point of different options is that regulators will want different options for use cases.  Alcohol, gambling, car rental and whatnot might not be satisfied by age range options.  There might not be a single API that will address all cases.  ID-based options will exist.  This might be useful where there are discretionary choices where parents have a role.

Marcos: Because teenagers lie.  If they get into trouble... They put themselves in harms way by lying, because that lie has ramifications.  So the kids are not worried about that.  Also, they can access more harmful content as well.  Now they live in fear of being banned or other consequences.

Rick: Wanted to challenge DC API claim.  Credentials allow cross-device.  So you could sign up and you could have the adult use their credential to attest adult status.  The application won't know that it was on another device and they don't get a name.  Then that would be cached by the service.  At some point they might challenge again.  In practice, they might ask again.  But you might not need to install the credential on the  child device.

Lola: I am concerned.  I don't think that this is wrong, it should be developed further.  Regulators seem to be on a one-track.  British government is fixated on particular goals.  Similar to Australia and its social media ban.  Talk of extra surveillance.  I would like to see more regulatory input.  This is an area where we have a set of privacy principles, while also meeting the needs of concerned parents and other users of the web.  That might read on what these governments really want.  They might not have anything in place legally to recognize some of these alternative solutions.  That might mean that sites won't adopt it.  It's a good signal that Apple/Google have an age range API.  So we have evidence it works.

Jeffrey: I want to talk about design details.  One aspect is that age is not the only kind of restriction that people might want to express.  Addictions might be nice to include.  Needs to be some negotiation there.  Well-known is not the right way because it involves an extra fetch.

Martin said something: not high-performance use cases of content negotiation, more like a first visit to a website, or one time account creation. definitely need to push back on potentially bad and harmful policy.

Ben VDS: I was going to address Jeffrey's comments.  The shaped sketched out here matches what the platforms do.  Four ranges of age.  When I saw this, something that is nice is that users can voluntarily opt into a more restrictive option than their actual age allows.  Much like Prefer:safe does.  Adding more categories is interesting, to allow optional protection. 

Jeffrey: Wanted to respond to some of Martin's comments.  Lot of regulators are doing this in bad faith.  That can be true.  At least California is trying to manage this responsibly.  Even while we mitigate harms from those who are less responsible.

Rick: In terms of how the TAG looks at this.  Might be some principles.  One I would propose is that APIs should be explicit in their assurance level.  We should not encourage APIs that are likely to get implemented in both low- and moderate- assurance levels.  Encouraging an API where a browser extension can override it, because the API might be misleading.  It might be hard to deal with the consequences that come from a lack of trust.  Low assurance APIs need to be clear.  Personally, I like that this is HTTP-level.  Browsers might make that not customizable.  We need to address not running a different browser.  Maybe only use these in places where those alternatives are not available.

Nick: Useful feedback.  The other generalizable part is for sites to make public promises about how they use data.  We should have this for age-range information. That should be useful for credentials as well.  Out-of-band accountability is a possibility to deal with abuse.  That helps them be held accountable.
..What the TAG thinks about declarations and whether we are willing to consider them for different classes of use.  Or whether other things work.

Jeffrey: Privacy Sandbox tried some of this public attestation, but it was never really tested.  Question for lawyers.

Nick: I would be happy to consult with lawyers and policy people.  Seems to be interest in this as part of a menu of options.  Thinking about taking this somewhere.  Unless you have other suggestions.

Marcos: Might be worth having a range of solutions in place.  DC API use is an option.  Need to understand different approaches.  Won't be stuck on one.  From that maybe new ideas come out.

Martin: I will be that voice. There needs to be more clarity on the range of requirements. Nick has done some good work. It would be good to have better agreement about the space, its problems, requirements, and solutions. Gambling has different requirements than what people think at first glance.

Marcos: We do have a great list of requirements, but we could do some analysis to line ideas with those.  Obviously we need to do something, contrasting proposals.

Nick: Consistent feedback is that there is a menu of approaches being attached to different use cases.  Self-labeling is another approach that can work.  

Marcos: Is Google's option being used?

Rick: We've announced that the ZKP solution is live with a few providers.  Some in UK and US.  It's the main usage of DC in Chrome.

### Chair selection

### F2F Topics


## Eurasia Breakout (Europe / Asia / Australia) - [2026-01-29](https://www.timeanddate.com/worldclock/converter.html?iso=20260129T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Martin, Hadley, Sarven, Marcos, Yves, Matthew, Christian

Regrets:

Scribe: Matthew

### [design-reviews#1013: Paint/presentation timestamps in performance APIs](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1013) ([Github](https://github.com/w3ctag/design-reviews/issues/1013)) - @matatk, @xiaochengh

Matthew: Xiaocheng was driving this one. last week, he published a comment after our breakout and they have replied. Seems detailed. We'll have to look at this and come back on it. 

### [design-reviews#1174: WG Revision: SHACL 1.2 SPARQL](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1174) ([Github](https://github.com/w3ctag/design-reviews/issues/1174)) - @csarven

Sarven: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/229#issuecomment-3797145530

Sarven: They're splitting the core part from the extensions (SHACL). The changelog didn't show anything new, so looks like it is just a re-org. SHACL will be an optional extension. In and of itself there don't seem to be any new normative requirements.

Martin: Did you confirm with them?

Sarven: Not yet

Martin: May be worth making that the review - doesn't look like any changes, but checking with them.

Hadley: If that is the sum-total of what they have done, I don't have an opinion.

Sarven: Will add a sentence as suggested, but will go ahead.

Hadley: Think so, but maybe don't conclude the review until they've come back to confirm. You could just put the question in first.

Sarven: Will check on the re-shuflling and open up the question for them.

### [design-reviews#1179: [wg/vc] Verifiable Credentials Working Group](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1179) ([Github](https://github.com/w3ctag/design-reviews/issues/1179)) - @csarven

Sarven: https://github.com/w3ctag/design-reviews-private-brainstorming/issues/234#issuecomment-3816374234

Sarven: There a lot of new deliverables, lots of maintenance deliverables. It looks like it's in AC review now? Is the TAG response relevant now? I can't assess all of the new deliverables they're putting forward, but it looks like they're all incubated in some form in the Credentials CG, or adopted from a WG.

... They're extending the core work. How they're doing this looks good. Can't say whether that extension is useful. They have things such as verifier confidence that came out of known use cases, and seem sensible to me.

Hadley: Procedurally, we have until 2026-02-01. Sounds like none of us are into the architecture of VCs enough to have an opinion on what they're proposing.

Sarven: What they have seems to be cutting edge. My assessment would be that there aren't any issues. Was looking for an appropraite label.

Hadley: Does anyone have any further thoughts on the conclusion? Do we have consensus there?

Martin: Looks fine. The quantum safe thing is dangerous, but it's tentative, so they may not take it on. Relates to digital signatures. I have opinions on the rest of it. Concerned about multi-@@@. Interop is more important than that, though, and they are working on it.

Sarven: How do we approach whether this is helping or advancing the web? A lot of this is plumbing, low-level. They're using a more advanced encryption model. If that's the latest standard out there then fine. But what is our role in assessing that? Is there some higher-level thing we should be looking at? I don't know how to assess this as it's in the weeds of how VC works. If a form of VC is a generally useful thing for the web, then the rest of it is effectively implementation. From the TAG's perspective, what can we say that's really useful here? I'm not sure how to give useful feedback.

Yves: In general it's quite difficult to assess if the product of a WG will be used or useful in the long run. E.g. ActivityPub - many people were against it, and now it's used in many places. Can be difficult to assess this based on the spec itself.

Martin: What Yves said is true. ActivityPub was not as well adopted until outside events occurred. For this at a high level we can look at the model they are using and the positives and negatives. The three-party model, someone who can make claims about a person and then someone who can take those credentials and @@@@. In the past I would go to Hadley's IdP to get info about her, for example, and Hadley would not have control over this; action at a distance.

... VC has the basis of some of the things that we're talking about in the Credential Abuse finding. There are potential downsides. Thinking about those may help. Hard to anticipate how things could be used. ActivityPub may not have worked out. We can try to anticipate where things might be used. Ultimately the low-level things are hard to reason about.

Hadley: Second that. Would add that as the TAG we're building our own library of resources and authoritiaive documents (that members feel are authorititve at the time). We have the credential abuse finding, and EWP, to point to later on. Both came from us reacting to design proposals and activities that were happening and made us think 'this can cause trouble; let's explain why'. Some of it is stuff there may not be a method for, but if it feels wrong to you, let's check we have consensus, and then see if we can use something we have, or write something new, to offer opinion to spec/charter authors. We never really sat down and wrote out all of how we are going to review the things we review, and how we think about the low-level stuff - it's constantly evolving. I think it's better we were not too prescriptive.

Sarven: This helps. I think we should dive deeper into what use cases led to their proposal. TAG could pershap more look at it, not so much from the minute details from the spec, but whether those use cases are aligned with the direction we want to see. Did they pick the right use cases?

Matthew: +1

Hadley: Can we work on this in the next couple of days?

Sarven: I saw them for the VCs doc, but not for the new proposals. What are the next steps?

Hadley: Sounds like you're not confident you have enough info to say this is great, whcih is fair. Procedural concern: if they're able to produce more use cases, we don't have time to have a TAG discussion about it before 2026-02-01. Yves, is it a hard deadline?

Yves: I think so. It can be done later as an FYI.

Sarven: Could we write a response that makes our concerns more apparent to them? 'If you can share a use cases document when you go for FPWD, and when the TAG reviews again we can probably come up with a better assessment'

Hadley: Makes sense

Sarven: Then a short review can be put out there. It's not going to change the charter much.

Yves: It makes more sense to send feedback on the document rather than the charter.

Sarven: For the charter itself then, let it pass by?

Yves, Hadley: Yes.

Hadley: You're responding in such a way as to say that we want to see the document when it's done but we have not had the capacity to review the whole thing. It's also helpful for future reference regarding what the TAG said.

### [design-reviews#1120: CSS find-in-page highlight pseudos](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1120) ([Github](https://github.com/w3ctag/design-reviews/issues/1120)) - @matatk, @xiaochengh

Matthew: we had a discussion a couple weeks ago, resulted in a different framing of the situation. I wrote a comment, Lola and Xiocheng reviewed it, I posted it and am waiting response.

### [design-reviews#1152: Incubation: Scoped Focusgroup](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1152) ([Github](https://github.com/w3ctag/design-reviews/issues/1152)) - @matatk

Matthew: The last on this was that we asked about implementation and... they replied and... no position from gecko/webkit.  Also talking with OpenUI/WHATWG/other browsers.  No commitments to implement, but only feedback is from Mozilla on the pull request on HTML. nice question about modifier keys.  Will look at this closely.  Not seeing any feedback from other engine that indicates it is too hard to implement.  Might look at discussions. No red flags.

Hadley: Lean toward satisfied with concerns and list lack of interest from other implementors as a concern.

Matthew: Lack of information is a big one.

### [design-reviews#1175: Other Spec Review: trigger-scope](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1175) ([Github](https://github.com/w3ctag/design-reviews/issues/1175)) - @matatk, @lolaodelola

Matthew: Checking if this is horizontal review.  Linked to scroll-triggered animations (?).  Have been looking at the other sections of this spec for APA.  Will take up layer.

### [design-reviews#1173: Incubation: Connection Allowlists](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1173) ([Github](https://github.com/w3ctag/design-reviews/issues/1173)) - @ylafon, @toreini

Yves: IIRC Ehsan had feedback too. Mike West announced they're going on origin trial soon, so we need to send it soon.

Ehsan: I liked Jeffrey's and Martin's commemts. Wanted to ask Martin... I am leaning towards satisfied with concerns, but wondering about the justification as to why this is necessary. I find it a good spec. But before that, wanted to see what Martin thinks.

Martin: We talked about it at Mozilla, people were asking where this comes from, why is it relevant? The conclusion is that it is unclear why it's necessary to have another policy for managing connections. Mike has an explanation, but others didn't find it compelling. Mike is deeper into CSP than most. But the conclusion was maybe we didn't try hard enough to shape CSP, rather than adding something new that does the same thing with slight modifications.

Yves: Perhaps we should say that one of the concerns is a lack of apparent consensus from other vendors. There's no comment in WebKit or Mozilla standardisation. Martin, it'd be good if someone from Mozilla could add such a comment. I agree with Ehsan that we should have satisfied with concerns, based on that and the potential abuse cases. It's an early review anyway.

Ehsan: I agree with Yves, but I agree with Martin as well. I think it's a very good idea to ask more about the justifications. I can see the logic behind it, can see why from my view, but from the spec authors' and devs' point of view... I think it will address Martin's team's concerns if we address this concern explicitly.

Martin: Mike has 3 reasons for doing an entirely new thing.

1. CSP is too granular, which I am not sure I agree with. It's not if you're dealing with high-level cross API stuff syntax (fixable within CSP).

2. Not granular enough.

3. Gaps in what CSP applies to (prefetch, RTC). The answer there is the work has been done.

It doesn't seem like a good idea to invent something entirely new here.

Hadley: So what do we need to do with this?

Ehsan: A position from Mozilla would be very helpful. After hearing Martin's point, I need to give it a little more thought. Right now it seems like satisfied with concerns.

Hadley: Even before a comment from Mozilla, we know there's not multi stakeholder support.

Yves: That's why I propsed, as there's no answer from WebKit nor Mozilla, that one of our concerns is lack of browser support on top of the other things we've discussed. Giving the feedback we have now would be timely.

Ehsan: I can draft something for Yves, Martin, and Jeffrey to review.

### [design-reviews#1058: The `interesttarget` attribute](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1058) ([Github](https://github.com/w3ctag/design-reviews/issues/1058)) - @matatk, @xiaochengh

Matthew: Spoke to the Pointer Events editor I know.

Hadley: It’s been a year.

Matthew: Other option is, we could say “lack of consensus.”

Hadley: Is that something you could feel you could do?

Matthew: If we have consensus, that’s fine.

Hadley: Less concerned getting off of our plate, more concerned we are timing them out.

Matthew: Will prepare a comment lining out the various opinions by different TAG members.

### [design-reviews#1177: Incubation: seamless page transition with deferred commit](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1177) ([Github](https://github.com/w3ctag/design-reviews/issues/1177)) - @matatk, @christianliebel

Christian: We wanted Tess' feedback. Haven't been able to reach her yet. I will review.

### [design-reviews#1184: Incubation: IdP-Initiated FedCM](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1184) ([Github](https://github.com/w3ctag/design-reviews/issues/1184)) - @hadleybeeman, @toreini

Ehsan: Still reading.

Hadley: How are we on deadlines? Looks like no obvious deadline. We are missing multi stakeholder support.

### [design-reviews#1172: Other Spec Review: <meta name="text-scale" content="scale" />](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1172) ([Github](https://github.com/w3ctag/design-reviews/issues/1172)) - @matatk

Matthew: this got to the point where I'm happy with it. Jeffrey said it's likely to ship soon. I had suggested some stuff that wasn't closed, but those things were not a show-stopper for what they want to ship. It was about something they might want to add in future, and I was asking them not to add that. I explained that on the GitHub thread, and acknowledged their updates. We haven't heard back. If we don't hear in a few weeks, we should ping them or contact directly. Because it's important, but not right now if they're focused on shipping. 

### [design-reviews#1182: WG Revision: CSS Anchor Positioning Level 1](https://tag-github-bot.w3.org/gh/w3ctag/design-reviews/1182) ([Github](https://github.com/w3ctag/design-reviews/issues/1182)) - @matatk, @xiaochengh

Matthew: I had mentioned that APA was providing feedback on accessibiliyt considerations. I wasn't concerned about most of it. Overall it seems like a good trend, moving stuff out of javascript into CSS, more declarative etc. So, no pure CSS concerns. But from APA's view, it crates a trap for developers, because it removes boilerplate code but you stil have to do the js if you're doing this with custom elements, you have to do the keyboard handling and ARIA etc. So how much does it save developers? It's probably a net positive, but smaller than it might have been. 

APA worry that people will think "we just do this and it's accessible", but it isn't. APA will be emphasising that. 

So this is moving in a positive direction, but we do need to make developers aware it's not a "get out of javascript free" card. 

I don't know if Xiaocheng has extra thoughts? He was involved in writing the spec. It's due on the 30 January, which is the last day of their face to face. The next one is April. 

Hadley: so the TAG view on this is that it's fine, assuming the accessibility issues get sorted with APA?

Matthew: yes. We need to set those expectations with developers. Guidance, not normative. 

## Face to face

Matthew: The Meet the TAG event is set for the 4th. Next to sort: ticketing and catering. 

* Breakout Rollup
### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+%28label%3A%22Progress%3A+untriaged%22+OR+no%3Aassignee%29)
