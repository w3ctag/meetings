# TAG Teleconference
#### 13-15 January 2025

---

## Agenda:

### Breakout A (California / Europe)  - [2025-01-13](https://www.timeanddate.com/worldclock/converter.html?iso=20250113T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss
* [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014)
* [FYI - Web Authentication API: PublicKeyCredential’s getClientCapabilities() method](https://github.com/w3ctag/design-reviews/issues/1016)


### Breakout B (California / Australia) - [2025-01-14](https://www.timeanddate.com/worldclock/converter.html?iso=20250114T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou


### Breakout C (Europe / China) - [2025-01-15](https://www.timeanddate.com/worldclock/converter.html?iso=20250115T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)
* [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)


### Plenary Session - [2025-01-15](https://www.timeanddate.com/worldclock/converter.html?iso=20250115T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Meet with appointment committee
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


-----


## Breakout A

Present: Dan, Tess, Peter, Matthew, Jeffrey, Amy, Yves, Tristan, Lea

Regrets: 


### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

Matthew: we asked for additional use cases...  we did get a reply with one additional use case: web apps that are embedded in cross-origin iframes... Not a long list.

Jeffrey: it's kind of fundamental that it's storage will be partitioned... if you have a partitioned iframe then the popup would be partitioned...

Jeffrey: what does safari do if an iframe opens a popup?  I can poke them to add this to the explainer...

Dan: they don't appear to have answered the UI questions we've raised...

Jeffrey: an early review ...

Dan: could we say "this looks good ... needs more use cases ... needs UI issues and abuse cases delt with ... please come back to us when you have a more fleshed out design" ?

Jeffrey: the iframe issue is in there...  I don't object to that...

Peter: the response of .. it does seem reasonable... i'm concerned about the abuse cases... if it's gated by a permission then how do you explain it to a user? I don't think users in general understand the concept of partitioned storage...  

Jeffrey: I think it doesn't require a permission... they are using framework... but no user permission.

Matthew: https://github.com/explainers-by-googlers/partitioned-popins/blob/main/README.md#ux from the user's perspective.. the domain/subdomain will be shown in the pop-in. From their spective what are we trying to cue them to check?  Seeing a pop-in with an address in it ... should that cue them that this is privelidged in some way ... we want to avoid specifying UI but that's my concern...

Peter: no indication to the user that the popin is related... 

Jeffrey: mobile UI is spoofable... as popin is drawing in the content frame...

Jeffrey: I think they need a story about what users are supposed to trust...  Security UX folks aren't convinced we have trustworthy UI: https://emilymstark.com/2022/12/18/death-to-the-line-of-death.html 

Dan: e.g. Web Payment uses trustworthy UI... so if there is no trustworthy UI then why are we doing Web Payment?

Peter: shrinking the chrome so much to give more screen real estate .. puts us in the position where the browser content can be spoofing that chrome.

Dan: i think we need to operate from the position that there is trustworthy UI.

Jeffrey: https://www.w3.org/TR/design-principles/#trusted-ui

Dan: i think from a TAG pov we need to stick to our guns.

Peter: I also respect the problem that on mobile there's a trend of behavours that makes that less the case...

Dan: also for full screen webapps... 

Peter: but in that case there has been an action the user has taken... 

<blockquote>
  
This looks like a good problem space to investigate. We'd like to see more use cases fleshed out, especially cross-site iframes opening popups on their own origin. We think the UI question is critical to a full analysis of this proposal: please let us know when you have a proposed design for that. We're also hoping to see a full description of what parts of that [UI users are expected to learn to trust](https://www.w3.org/TR/design-principles/#trusted-ui), and how various combinations of malicious top-level, embedded, and popup sites could take advantage of that user trust (that is, explain the "abuse cases" and how they're mitigated).

Please reopen this issue when we can look at that analysis.
  
</blockquote>

*general support*

*we agree to close it as "satisfied with concerns" - jeffrey to post the comment*

Peter: I still have questions... if they can address the concerns then fine... if not, then ... 

### [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss

*we review [response](https://github.com/w3ctag/design-reviews/issues/1005#issuecomment-2577396759) from Keith*

Peter: i think this is a good enumeration of inconsistencies and proposals to fix them...  We looked this last week that we're concerned with the inconsistency...

Lea: open event... on dialog.

Peter: keith talks about the open attribute...

Lea: I think harmonizing dialog and details is a good thing... Even if it's not perfect.  And popovers as well...  Harmonizing all of these would be a good thing...  

Peter: my concern: is this going far enough... and also so many issues in different places.

Peter: but if even nothing else gets done, toggle is a step in the right direction.

Jeffrey: this toggle event is trying to make dialog match... events will be consistent across the platform with this change

Lea: popover is an attribute that can be added ... to anything ... 

Jeffrey: there is an issue on HTML for doing that: https://github.com/whatwg/html/issues/10171.  

Lea: open=details ... seems like a footgun?  tends to create usability problems if you add noops like that.

Peter: i wonder about situations like where something is opened differently... 

Lea: i don't think we need to figure that out in this issue.

Peter: I think all the rest of these that have issues are steps in the right direction... but we need to make sure they all stay related... Most are in WHATWG but some are in OpenUI... people considering each issue should be considering them as part of harmonizing...  Willing to close this issue as satisfied...

Lea: close event ... should apply to all of these...

Peter: you're saying we should add close event to other things?

Lea: seems like it

Jeffrey: I'm worried about redundant events in the platforn... I'm worried about performance cost of firing extra events... 

Lea: should we deprecate `close` then?

Jeffrey: ideally yet.

Peter: worried about the next *thing*...

Tess: we have "aim for consistency"...

Peter: one way forward is to let developers choose, other way forward is to pick one.  I see both sides... 

Dan: *developer complexity*

Tess: the obvious concern ... you have a web site maintained by more than one person... developers stepping on each others toes... and they have to figure out that there are 2 events firing...  Not great.

Dan: +1

Jeffrey: we could give them the choice: either deprecate one of the events or add all of them everywhere.

Peter: have they even specified... and in what order?

Peter: I think Tess raises a valid point... it's important to specify what order you're firing them in... even if one of them is deprecated... 

Jeffrey: it *does* specify that the toggle stuff happens before the close event... 

Peter: bottom line? 

Dan: what do we say along with the **satisfied**?

Peter: I think we should say .. do we deprecate the open/close or recommend they add open/close to everything?

<blockquote>
  
Thanks for listing all those issues. It looks like work is being done to start harmonizing these.

We're satisfied with this work.  The directions you outlined look good.
  
Regarding your questions: we're concerned with adding multiple redundant events in the platform from a developer complexity and performance perspective. Furthermore, having some elements with both types of events raises another inconsistency, we recommend that either all elements get both event types or the open/close events become deprecated.

</blockquote>

**We agree to close as satisfied with the above comment, Peter to post.**

### [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014)

### [FYI - Web Authentication API: PublicKeyCredential’s getClientCapabilities() method](https://github.com/w3ctag/design-reviews/issues/1016)


## Breakout B

Present: Jeffrey. Peter, Tess, 

Regrets:


### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou

Closing as `decline` with

> It looks like this merged to HTML and shipped most of a year ago, so we're happy to get out of your way. Thanks for sending us this review.

### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

Checking with Lea, then closing as `satisfied` with:

> Thank you for pursuing the discussion with TC39. We hope you can make sure nothing the the API precludes them eventually adopting it, but we're happy for you to proceed through WHATWG until that happens. Good luck!

### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou

Jeffrey: We should close this.

Peter: And they did what we asked: they added an explicit opt-in, after which the keywords are interpolable.

`satisfied` with

> It looks like all our concerns are taken care of in the latest spec. Thanks for working through this with us!


### If there's time

* [Remove two duplicate links from the list of Findings.](https://github.com/w3ctag/tag.w3.org/pull/54)

Approved

* [Merge the HTTP guidance into the "consult other specs" section.](https://github.com/w3ctag/design-principles/pull/546)

Tess: Preserve ALL the IDs!

Jeffrey: Will do.

* [Fix markup mistakes caught by bikeshed's new parser.](https://github.com/w3ctag/design-principles/pull/547)

Approved

* [Remove obsolete parts of the privacy principles SOTD.](https://github.com/w3ctag/privacy-principles/pull/453)

Approved

* [Update links now that this repo has moved from the w3ctag org to the w3c org.](https://github.com/w3c/security-questionnaire/pull/184)

Approved

## Breakout C

Present: Amy, Matthew, Xiaocheng, Yves, Hadley

Regrets: Dan, Max


### [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman

Hadley: we've got some stuff here to process. I believe they've answered part of our question in how they think their proposal fits in with web payments. The other part of the question is whether they've talked to the web payments group and if so what their response has been. We should encourage them to make that link explicitly with the people as well as the concepts.

Matthew: it also seems to be labelled as missing multistakeholder support.. don't know if they answered that. Should we ask about that?

Hadley: they did open issues in Mozilla and Webkit standards positiosn repos linked at the top, no reply yet. Will drop a comment in the meantime.

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: they updated their explainer to incorporate our feedback. We also wanted to also have exclusions and have pass inside the scope and not just in the origin. We might add a comment about having a consistent UI experience when you're switching from one origin to another, because it's not there yet, but apart from that, should be okay. Would be better to have Martin to agree on that as well, but okay for me.

Matthew: if Martin or Dan are at the plenary we could bump it and chcek on it there. Or async.

### [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)

Amy: (End) user needs are not explicitly stated.

*[Matthew left a comment](https://github.com/w3ctag/design-reviews/issues/1012#issuecomment-2594023351)*

### [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)

Amy: Both of these aren't very user needs forward. Talks about use cases but not end user experience. Probably implicit because it's performance, but it's useful to have them state that explicitly so we can weigh up tradeoffs

Matthew: second one missing "alternatives considered"

*[Matthew left a comment](https://github.com/w3ctag/design-reviews/issues/1013#issuecomment-2594024970)*

## Plenary Session

Present: Matthew, PLH, Tess, Yves, Sarven, Peter, Coralie, Amy, Ralph, Jeffrey

Regrets: Dan, Hadley

### Meet with appointment committee 

Philippe: we haven't made decisions yet, we want to first listen. We may need a second meeting to explain our suggestion. Last year we made the mistake of saying minimum to the TAG about why we're picking individuals. That backfired. This year we'll explain more. The Team is mandated to appoint individuals 2+1, we are in the period of appointing 1. Our goal is outlined by the process - to fill the gaps from the TAG as much as we can to support diverse and well balanced TAG. Technical background, knowledge and skillsets. We don't hesitate to appoint new names. If it someone you don't know don't be afraid. We want to have new people working on web stuff we need to be welcoming to them. We cannot appoint someone with the same affiliation as someone already on the TAG. We do allow people who potentially lost the TAG election. We see those appointments as part of making a diverse and well balanced TAG. People who lost the elections are valid appointees. We'll communicate the name to you and the AB. We might have a second meeting to help understand the choice. After that you will need to ratify the name. 2/3 support from the TAG, and 2/3 from the AB. AB is less hands-on. Ballot is secret (except for Ralph). This is not a political game. We expect to represent the web. Our goal for the 4 of us being here is to represent the Team.

Yves: I'm representing the Team and the TAG to each other.

PLH: yes, we rely on Yves a lot to communicate with the TAG.

Coralie: Last year we wanted to be neutral, not seen as unduly influencing you. This time we're going to tell you why.

PLH: we have a list of 25 names right now. We include names of people submitted to us. Any questions about process?

... The TAG is moving forward with TAG associates. We don't have to worry as much as we used to about TAG reviews as associates will help on that front. Previously we had some technical areas in mind. At this point we don't have a specific technical area in mind. We think you guys need more help on statements. In Seville Hadley asked me how we're going to make decisions about WGs. We don't have a director to tell you what the web should look like or be driven by. We're going to need statements for that. We want all groups to be aligned with the statements. We'll need help as much as you can. If there are statements you want to work on, we can try to find you someone who can help with that as well. Please tell us what you believe you need and any other considerations?

Peter: As of our last f2f we have shifted our focus more towards doing findings and statements, and defocus design reviews. We still do design reviews, but we want to put a lot more energy into the statement and finding type work, and push design review off more towards associates. When we were discussing earlier this week we want to be clear that associates will not be participating in TAG consensus - giving input, but when it comes to forming a consensus opinion on something that's the seated members - appointees and elected people. Your'e correct we don't need as much help with design reviews for appointess, but we do want the balance for finding consensus.

Tess: In this election,  Hadley who was the holder of an appointed seat, got elected. Everyone else was new. It's a bigger turnover than normal. The encumbants didn't run. We'll have less institutional continuity than we usually do. Not necessarily a bad thing. In the past I'd be reluctant to see people who have been around for a long time or who have been on the TAG before. But in this case, anyone with experience on bodies like the TAG or the TAG itself feels like fair game. One area notably we're losing Peter - one of the two chairs. Dan will need a co-chair. There are people on continuing or new TAG who are up to the task. But chairing seems like a skill that could be selected for in appointments. 

... Lea, Peter and I are all leaving the TAG. All CSS WG and have done the bulk of design reviews around CSS stuff. I don't think that means you should prioritise someone with CSS WG experience over somebody else, especially with TAG associates, maybe that can be addressed in a different way.

Jeffrey: Agree with Tess. Want to mention a philosophy for appointments, and 3 skill gaps. One is that your'e trying to balance the values of the TAG. We're missing expertise in certain areas, which implies valuing those areas. That could be a reason to appoint from a subject area even if we could in theory invite that subject area as an associate. We may still not find consensus valuing that subject area like we should. Three areas I think we're missing are: 1) people who know about Africa, South Asia, South America, for a very long time. Would be great to find someone who could represent the entire global south. 2) We're also down to one woman on the TAG, which measn we might be systematically undervaluing things that are important to women. 3) We don't have people who do much DevRel or outreach. 3) We don't have anyone who does UI or UX research. We all have opinions about UI design but it would be nice to have someone with exerptise. Would like an associate for that, but might be valuable to have in the TAG

Tess: often discuss CSS. With me Peter and Lea all trying to do CSS design reviews, we sometimes felt reluctant even though we have domain expertise, because we didn't like the optics of getting our way via a TAG review if there was a disagreement. Perhaps there are people who have experience in the area of CSS but who are not specifically WG participants. Experience hacking on layout engines in browsers, but not at the same level in standards work.

PLH: those CSS conversations, were they because of review or a broader discussion?

Tess: generally design reviews. Sometimes dispute escalation.

Jeffrey: I think it would be important to think about whether people will need a lot of mentoring to get up to speed with the TAG

Tess: Jeffrey you might be the outlier here.. you're the first person to have ever hit the ground running.

Jeffrey: and consideration is how much time people have to devote to TAG work. Squeezing in TAG work on the side may not be enough time.

Peter: 1 day, currently spread out over multiple days

Jeffrey: We can optimise that

Peter: having the meetings spread out over multiple days had significant impact.

Sarven: appreciate there are a lot of factors. What kind of things W3C is expecting to work on for the next while? The kind of direction that it wants to take? And how that would align with the type of things TAG can support?

PLH: Think about the web, not W3C. Fingerprinting remains a total nightmare on the web. Another area is data space.. digital wallet, identity, it's an area becoming active and tricky to manage. Less coordination between different SDOs. Social Web aspect is interesting. Hoping for a charter. We dont' know how much it might interact with linked web storage. Performance could be relevant.

Jeffrey: Wondered what the team thinks we're missing.

PLH: we don't have a particular area we think you are missing. Just trying to tease your brain.

Jeffrey: it's a good list. Meeting values, and meeting technical areas. A bunch of people already value privacy. We'll notice things and send them to the privacy WG for technical reviews. For data and social web, I'm hoping Sarven will make sure we care about it and send it to appropriate experts or associates for review/details. I feel like for some of those areas we have the right values already.

Matthew: Completely agree with what everyone has said. The order it was said was important as well. Definitely certain areas of subject matter expertise we know we need. But we have contacts among associates or internal or external group. Using the lens that Jeffrey did, about values, is a really good one. That will help us distinguish between someone who can be an assciate or someone we need in a decision making capacity. All of this takes precedence over what I'm going on to. Question for the Team - the digital identity stuff. I'm nto an expert on this. What I have seen about it at AC meetings and TPAC is that it's so early and such an organic mess.. there's so much lack of consensus over basic things like how many identity providers there even are.. an dfor some people the browser is part of the threat and for some it's part of the solution. It's really important, could be a foundational area. I'm not sure that it's developed such that we need someone on the TAG to make decisions about it. What we need to do first is liaise with other organisations and try and get on the same page with some of this stuff.

Tess: Marcos does this kind of thing

Matthew:  ... cryptad lost my minutes of the very insightful things Matthew said about digital identity :( :( :(

PLH: digital identity, we reported on this last year. Simone and Seth are going to a workshop. Going to come down to balancing the various principles we have, rather than specific expertise. Trying to balance a set of principles and use cases.

Tess: one thing that hasn't come up is, I think it's extra important that the TAG be composed of people who are more likely to bring light than heat to fires. People who have a track record of helping people at loggerheads find some kind of consensus. We haven't necessarily prioritised that before. Especially with councils. Even keeled diplomat type folks.

Peter: agree with Tess, Jeffrey and Matthew. One thing Tess brought up is the skills we're losing with Tess, Lea and myself leaving the TAG. Also Amy has brought a lot of get off my lawn energy which has been valuable, and been a strong advocate for standing against the abuses of advertises and others. While there are other people who care about privacy and protecting users. I'd love to see someone to help carry that banner.

Tess: also helped us look at how we work. A lot of the improvements to our work mode and the routine of day to day TAG operations is better. Somebody with great oragnisational skills and the ability to herd cats should be on the list.

Matthew: I appreciate what the Team was aiming for last time. It's laudable to have a principle of being neutral wherever possible. But your job is to balance the TAG to fulfil the values that apply to the web. The way youv'e approached it this time feels like the right way. Hopefully your efforts will pay off and it will go smoother. It's much appreciated. Great to have this type of forum.

Coralie: timeline... 

PLH: lots of input to get. Old and new TAG.

Amy: remind of f2f meeting

Jeffrey: we have 2 weeks before Feb 1st. Can we get a shortlist or a nominee next week?

PLH: we are going to give you 1 name to ratify. Do you want a meeting once you have a name?

Jeffrey: I think that would be helpful. We want you to pitch the person. 

Peter: or in writing if we can't all attend a meeting

