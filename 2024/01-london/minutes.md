# W3C TAG - Breakouts A & Plenary Sessions - Tue, 23 January 2024

## 1a 

Present: Sangwhan, Yves, Tess, Dan, Matthew, Max, Martin, Lea

[web install](https://github.com/w3ctag/design-reviews/issues/888)

*assigned to Tess & Lea - noting that we got feedback from Diego and should therefor discuss this week assigned to 7b*


[HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900)

*reassigned and we decided not to talk about it this week*

[clipboard formats feature detection](https://github.com/w3ctag/design-reviews/issues/901)

*assigned to 2a*

[DisplayMediaStreamOptions monitorTypeSurfaces](https://github.com/w3ctag/design-reviews/issues/892)

https://github.com/w3ctag/design-reviews/issues/762

*not assigned to today*

https://github.com/w3ctag/design-reviews/issues/776

*closed*

https://github.com/w3ctag/design-reviews/issues/843

Dan: we need to re-assign ...

*reassigned to Tess & Matthew*

https://github.com/w3ctag/design-reviews/issues/334

*reassigned to Lea & Tess*

https://github.com/w3ctag/design-reviews/issues/911



https://github.com/w3ctag/design-reviews/issues/902

*reassigned to Lea & Tess*

https://github.com/w3ctag/design-reviews/issues/525

*we discuss closing this since we haven't made progress*

Lea: could it be a principle?

Tess: we are the right group to do this -- 

Sangwhan: it would take an entire f2f...

Dan: topic for TAG future?

Sangwhan: We have to go through all that's currently available - requires a focussed issue.

Tess: 468 is also similar.....

https://github.com/w3ctag/design-reviews/issues/468

*reassigned to Matthew & Tess*

**Both 525 & 468 assigned to TAG future discussion - added "deep thoughts" TAG**

https://github.com/w3ctag/design-reviews/pull/844

*merged & closed*

https://github.com/w3ctag/design-reviews/pull/898

*sangwhan merges & closes*

## Signals of Support

Sangwhan: we ask for a lot of signals for reviews - signals for implementer interest can be misniterpered.  There are cases where we see a negative signal - doesn't belong in our browser but is it OK for another implementer, or it will cause proper harm to the web platform....   Other part is that the TAG-side signal is not well conveyed...  Not well aligned...  Also I want Google to have a standards position repository....  Implementers see a new proposal and TAG sees radio silence - is it no support or negative?  That causes delays.. There should be a way for implementers to say "i don't care" ...

Martin: I don't think a useful signal. The TAG should get a formal signal and should get no info because they're not interested... It doesn't mean there's an obligation on the part of every implementer to respond to every proposal...  What's the material difference from the TAG's perspective?

Sangwhan: if there's not enough time then we could delay the review... if others are not interested we can say "satisfied with concerns" ... being able to distinguish would be helpful.

Martin: I would say "the TAG is looking for as much info as possible for any given proposal - the implementers work is useful input but the TAG can make it up its own mind...  if we lack the info then we can ask for it... "... Radio silence - you can infer lack of interest... Don't create a dependency....

Sangwhan: cases where ... there's a niche use case .,.. we ask for multi-implementer support ... there's no response .. then we say "we have serious concerns." 

*discussion on what we're asking about*

Sangwhan: try to make it easier for other implementers to say "we're not interested, case closed"... And when there's a signal "this is a bad idea" we should know how bad it is...  I would like better signals from us... and potentially also the implementers... 

Martin: I hear this complaint from new participants in IETF - it's no-one's obligation to pay attention to your proposal... if you're unable to get ...

## Findings Plenary

### Bundling & Caching Finding - possible mitigations - emulating security without having bandwidth...

Tess: I'm concerned .. the first time you go to a site that embeds from tracker.example ... In a world where you're emulating partitioning ... you're vending the personalized resource... now you have a cross-site tracking vector.

Yves: one signal could be cache-control public ... or allow-list of sites... 

Tess: or you load the resource multiple times... and only if you've loaded it multiple times and it's the same every time... a heuristics...

Sangwhan: with enough duplication....

Tess: load it partitioned... on like 15 page loads it comes back with the same bytes...

Sangwhhan: wouldn't SRI mitigate this?   If you have a hash then there's no way to inject an identifier...

Dan: is there any wording about possible mitigations? 

Tess: we're trying to invite someone to investigate this for us

Yves: we just want to give out a naive example of things that might work, but not a definitive solution - a call for research in the area to address the issue we are raising about the cost of partioning

Dan: how much do we need to do here?

Tess: not saying we should design it for them. If we do throw out a straw idea for an avenue of investigation, we should be up front about the issues with it. On the face of it this naive approach doesn't work but..

Yves: maybe it's a start

Tess: without saying that we can't put what we have now

Dan: can we agree that wording now?

Sangwhan: The other part is that we could polish more after publishing the initial draft

Tess: would love to get Martin's thoughts

Lea: what if we slot it in tomorrow? We could get it to a place we're happy with

### Merging PRs

**we agree to merge PRs 13, 14, and 15*

*We agree to ask Martin for feedback on this version of the document so we can potentially publish tomorrow*

# W3C TAG - Breakouts A & Plenary Sessions - Wed, 24 January 2024

## The web is unversioned finding

We got some feedback from Jeffrey and Coralie.

[general agreement]: Web 2.0 part needs to be more nuanced - web 2.0 was good, but it shouldn't have been called web 2.0, that was harmful in retrospect. It's always been the same web. Rolling release with a very long deprecation pathway. 

Martin: please don't rush out versioning finding...

# 05a - Design principles discussion

### [Add Lea as editor. #462](https://github.com/w3ctag/design-principles/pull/462)

Merged - thanks for volunteering Lea

### [More detail on why events should fire before promises #460](https://github.com/w3ctag/design-principles/pull/460)

Consensus that this leaves the spec better than before - some questions about definitions and examples.

Approved Jake's PR

### [Developer version of design principles #386](https://github.com/w3ctag/design-principles/pull/386)

Closed PR.

Discussion about the use cases for developer (app/library/...)-specific version.

It's a subset of the full document. The differences are not section-level, but more granular (e.g. skipping paragraphs about IDL). The full document is for implementers.

Comparison to HTML developer version - which provides a precedent.

**Action:** How has the HTML developer version been received? Is it maintained?

Lea: There is a gap in terms of this sort of documentation for developers.

**Action:** Peter is checking out if this could be done with Python.

Lea: Think we should close the current PR, as a different technical approach will be used.

General question that GitHub Actions may be usable for this.  Apparently we use actions already, but we might need to do some more work to avoid manual labour.

Discussion about using some sort of JS/CSS-based approach vs. a preprocessor for Bikeshed (ref the PR comments).

Lea: This would allow us to have different attribute valeus, as well as element content.

Martin: could we establish two documents and then use "include"s? If it's just the metadata that is different, then the two sperate files would only contain that, and reference a common principles.md file.

Sangwhan/Lea: Let's explore having just one source file with conditionals to start with.

TAG has faced several challenges in getting the principles adopted. In the long run, they'll help with design reviews, and help with scalability.

Sangwhan: We don't have a checklist of things to look for in reviews, based on the principles.

Lea: the principles provide a tool for TAG to improve consistency, both amongst the TAG at any given time, and over time.

General consensus that this document is the most important document TAG produces.  The primary purpose design reviews is to inform the development of design principles, so that what the TAG does is not disconnected from reality.

### [Data minimisation principle #465](https://github.com/w3ctag/design-principles/pull/465/)

Discussion of relation to Privacy Principles

Martin: this ties in with purpose in the other document.

### Discoverability of the principles documents (also web site updates)

Matthew: We have a lot of principles documents (across W3C), e.g. Design, Privacy, Ethics, also Ethics and Machine Learning. Need a way to signpost them all? A page that lists all the docs.

Lea: We do need some updates to the TAG site - please update if you can.

### [First pass on backwards compatibility principle #354](https://github.com/w3ctag/design-principles/pull/354)

Discussion about some of the wording; pointers to other specs. This started as an HTML design principle; could cover JS, but needs to be widened.

General desire to include examples of good/bad outcomes.

Martin: "New features should add capabilities; not change existing ones" (then some more nuanced discussion)

Lea: Wouldn't necessarily want that to be a blanket statemnt. Sometime we do need to change things. E.g. CSS `:visited`. Underlining rendering in CSS changed. Some people angry, but in almost every case, it was a win. Current thing changed in spec is about changing default color interpretation to OKLab from sRGB - do some people "depend on"/expect it?

Martin: if you're going to make changes that will affect content, the onus is on you to do your research.

Tess/Martin: We need to be very clear about this in the doc, as we get a lot of requests for potentially breaking changes.

Further discussion on phrasing/structure of the PR content.



## 06a

Present: Dan, Yves, Martin, Sangwhan, Lea, Tess, Amy, Matthew, Max

*discussion on graceful degredation principle*

*consensus that we do need a principle on this*

### [Add some discussion on adding removing features](https://github.com/w3ctag/design-principles/pull/469)

Martin: forwards/backwards compat but I am light on the forward in this...

Tess: Backwards and forwards should be kept separate... 

Sangwhan: actions that have to be taken are very different

Martin: 2 is right 

Sangwhan: fold this into martin's PR?

*we discuss Lea's proposed changes*

Lea: I think adding a list makes it more concrete. 

Martin: I was hoping to make it an inline list... 

Lea: I just want it to be more concrete.

Tess: Let's link to 1.7.3 in the HTML spec... We don't need ot list all of them here.

Sangwhan: My concern - we don't have any guidancce...  What am I supposed to do as a spec author?

Amy: Most of these sentences can be flipped around to make them [action oriented].

Tess: there's a feature - you want to remove it - if lots of web content depends on it you can't remove it so you do research and if you find nobody uses it

Lea: don't just assume, verify with research that changes would actually break the web.

Max: [on adding new feature] .. is that on all new features .. 

Sangwhan: adding or changes...

*we noodle on this a lot and then agree to squash and merge it*

We agree to close 354 and potentially lift some of the examples ... into a further PR that adds examples...

### Bundling and caching finding

Martin: we spent an inordinate amount of time on the topic of bundling content. 

Dan: we have a long history with packaging

Yves: we've had discussion and a draft finding about addressing parts of a bundle. Lots of related work.

Martin: I'm struggling with what this document is seeking to achieve. That's not particularly clear on what it's message is. There's a potential implied statement being made which I think is the wrong one. Tess tempered some of that with the recent pr. From a privacy perspective, the fact that interactions with sites are kept separate is important enough to spend real resources on. I know some people may disagree, but I hold that firmly. The document seems to be saying something approximating the opposite of that, and it's quite confusing. I'd like more clarity on what it is the document is trying to accomplish before I get into the next layer of discussion.

Sangwhan: putting the bundling part aside, and focus on the site isolation and partitioning. Partioning solves a real problem, we're in total agreement of the benefit it brings. THe document is trying to highlight is that there are some costs associated with having partitioning. THis gets amplified a lot more in places where network bandwidth is limited. On top of that, there's associated costs in terms of client device storage memory, which is not something we can easily neglect for the sake of privacy. What we would like to get to is there's probably a different way... there is single keyed caching which is scary and not great, we don't want that for security and privacy reasons. The extreme opposite end which is double tripled keying has an expensive cost. THis document is seeking to ask from the main experts is to find a middle ground where we could get some of these guarantees without having to pay so much in terms of cost

Martin: that's not the message I get from having read this. It's my view that the finding says we've learned something here's what we've learned, rather than asking a quesiton. If this is phrased as a question that's a different thing than a finding.

Dan: a finding is our word for an opinion. An opinion can be we think there's something broken and some people oughta fix it

Martin: it needs to say that more clearly if that's what it's saying, and I"ll probably disagree with that. The next layer of things is that we think there are .. there's something to be explored in terms of opportunities for resource reuse on the web. 

Sangwhan: correct

Martin: that's a fine aspirational statement, but it's not a finding. I"m struggling.

Dan: let's forget about the word finding and focus on what we're trying to say

Sangwhan: could folks with the right expertise get together and propose somehthing less expensive than double and triple keyed cahcing. Can we figure out a way to make the ecosystem do less bundling which is incredibly horrible

Yves: the issue is not to replace double or triple key caching, it has some values in the wild. But there may be specific cases where you know what you are caching and the status of it, or you can have heuristics which define that. In that case you can more aggressivley reuse what has been cached locally to avoid spending too many resources. THat's basicaly the message. It's not to say let's replace it with something else. It may be optimised in some way

Martin: two things... I read this as something of an attack on the privacy protections that were put in, where that's clearly not the intent

Tess: that's how I read it before I did the PR, that was my motivation

Martin: want to concentrate on the positive things -I'm not seeing those either. NOt concrete enough for the TAG to be saying it. Potential for people to be doing some work, but that's not TAG work necessarily. Unless it's the case that the TAG has a unique insight into the problem derived from being exposed to the broad spectrum of things. THis is a huge discussion over and over in the http world. We talk a lot about content granularity and the overheads associated with requests so we might encourage people to make smaller requests, and all of those sorts of questions, all the time. We don't have a good answer for that. Saying we don't have a good answer is perhaps a reasonable thing to be saying, but a lot of people who work in the space already understand that.

Sangwhan: ..thinking... Could be reworded.

Dan: we hear you. We need to address the issues you're raising.

Sangwhan: Maybe we could get a round of feedback on how the intent reads from somebody that doesn't have as much background as Martin does. It's not specifically for the people in that particular domain

Yves: it's also for people who want to develop things and say we have a privacy problem, lets double key that to avoid that problem, and there might be other ways of doing it with less cost. Also for that audience

Martin: where would that occur where that is not part of the web where we've already made that decision? AGree in the general application you might look at the web and say the web just double keys everything we can too. BUt you'd be outside of the web at that point. It's just how it is. There may be cases where we can loosen that behavoiur under tight constraints, and we should be exploring those, but not soething the TAG should have a say on

Dan: I feel that's where we could be saying something - what are the constraints under which double keying could be loosened usefully in order to acheive..?

Martin: I don't know the answer, it's discussed in http

Sangwhan: I suppose if we had an answer we wouldn't be doing blind double keying

Martin: extends into other topics. THe http wg talked a lot about the ability to do cross resource compression, which is to say you have two resources and rather than serving the individually compressed you use compression that spans the two resources

Tess: we've talked about ..

Yves: this is the work that was tempted to the TAG with the shared dictionary thing

Martin: it's now being worked on by Patrick ? and it looks promising. But we still don't have a concrete solution for the cross resource thing, because it rquires what is effectively a publication of a common resource that is referenceable by multiple things. Leads to a number of complexities within the protocol, and the effect it would have when exposed to the web. We'd not be able to have something like this operate across double keying partition boundaries.

Dan: given Martin's feedback we need to go back and take a look at that. We need to make a decision on what to do next.

## 7a

Matthew: does Topics and Protected Audience overlap?

Amy: yes. All of our feedback on Topics applies to Protected Audience, but PA does more stuff.

### Delayed clipboard rendered

Tess: ... paste the representation that makes sense. At the time you hit cut or copy you don't know where the thing is going to get pasted and theremight be some representations that could be useful to generate that are computationally expensive to generate so you don't want to compute that representation until it turns out you need it. So you want to put a promise into the clipboard saying if youc ome back to me and tell me to produce one of these expensive thingsI'll do it then, but I don't want to do it upfront.

Matthew: they've answered our query and updated the explainer. Only applicable if copy, not paste, is being performend in a webapp. 

Tess: the website where you hit cut or copy doesn't get to know about what app ro website is receiving the paste. All it gets to know the preferred format

Amy: could it infer where it's going because of the format?

Tess: it's a concern. Eg. a web app that's an image store, pasting it into photoshop. If there's a photoshop format, you've eseentially told the website you're using photoshop. THat could be mitigated in a couple of ways - you could do a data minimization step. Typically a format string talking about a video format will have the mime type that identifies the container and the codecs to use inside the container. The browser could discard some or all of that, and say you wanta video but not a specific kind of fancy hdr video in a specific codec. There's a risk that a very specialised tool might ony support the narrow version and not the wider 'any video'. That would mitigate the backchannel.

Matthew: they have made a pr to update the explainer to update in line with what they've told us, but it's not merged and there's an image that might be good for us to see but we can't see it

Tess: their exampleof excel is a great example of this

Matthew: in this proposal they are presumably doing things like proposing an event which the webapp will receive when the user has pasted to say what format was requested?

Tess: yeah

Matthew: so this is how that gets through the browser to the webapp so the webapp can respond

Tess: they have a callback so they pass in... it's a callback per format. The page isn't getting a callback saying hey I want this format, on a per format basis, only what it can return..

Amy: that seems less risky... but is there an attackwhere the site could offer ot return some formats that would reveal something?

Tess: a generic tool.. if someone requests WordPerfect... that's fingerprinting, you're learning something interesting

Amy: could you identify protected characteristics if for example the paste format is to some specialist software, eg. for accessibility purposes

Matthew: good example. There is software that will read back something that is pasted in. But no custom mime types. Can users opt out? The app would have to be coded quite differently

Tess: the version of the explainer says there are no privacy considerations, but they have added stuff in their PR. One of them is that the web custom formats are specific to particular ecosystems so that's conveying information. They have a couple of possible mitigations which are not great. THe first is browser triggers all the callbacks, which is the exact opposite of what this api is designed to do,it's very expensive. The second one is support a generic web custom format that isn't specific so it's saying nothing. I don't understand that.

Matthew: sounds like the developer of the app decides the most appropriate default format and they just get that. You'd have to declare what that default format was, and they're not doing that

Tess: that's why I don't understand it

Matthew: we can comment that

### Captured Mouse events

Tess: had a concern about non-cursor based input... they say it's out of scope. But they could just send an array and future proof it. Rossen phrased the question in terms of no visible cursor, but there are cases where the cursor is visible but only transiently, eg. a trackpad connected to an ipad.

Matthew: seems like there might be an opportunity for accessibility improvements

Tess: like making the cursor more prominent in a screen sharing context

Matthew: want to make sure they're considering that. Will suggest they include accessibility considerations and APA can help them write it. Kind of covered in the spec, but not...

### [Writing assistance](https://github.com/w3ctag/design-reviews/issues/924)

Matthew: the UI for suggestions already exists. 

Tess: this is giving the page the ability to opt in or out depending on where in the page. Cynicism aside, this is a good idea we should do it. Similar scenario with different input methods. If you have a complex IME it may or may not interact with the page well. The page may provide its own IME, which might be more specialised. The values of on or off are not good. Feels like it should be boolean. THe downside would be there's no explicit opt out in that case. It's presence or absence. If it were boolean you couldn't be saying outright don't do, only defnitely do it. If the default is do it there's no way to turn it off

Amy: would there be other values in the future?

Matthew: like system default. Could this turn into a an attribute with a list of values? Like 'on' and the subject area is...

Tess: i think this design is roughly right, and there are use cases that aren't LLMs, existing use cases for autocomplete etc

Matthew: if we're saying subject domain should be a different attribute, is writing suggestions the right name for the one we've got?

Tess: I don't think we need to bikeshed that. They talk about calling it text prediction instead of writing suggestions, but that's too narrow. I don't have a better suggestion.

Matthew: also, we've talked about IMEs and i18n issues, should we ask them? For example how does it know what language the writing suggestions are going to be in? We have a lang attribute, how does that interact with custom elements?

Tess: it works fine, it's already well specified. The system at the OS level either there's some kind of keyboard or input method selection, and your language preference, the system has a really good guess. The page can use lang attributes to help that along. All of that is able to be fed into the thing that decides what to do. Do we need a separate predictive-lang? Probably not

Matthew: not asking that. Do we think we should run it past i18n

Tess: I'll write a comment. Also remind them to talk to i18n.

Amy: is it just to control llm provided suggestions or are there other options?

Tess: other options. Eg. in iOS it can suggest next words. BUt what they're actually doing is using an LLM

Amy: their solution is good, our reality is bad

Lea: Is this only on contenteditable?

Tess: no, all form controls

Matthew: what if in future they want to fine grain control it - so autocomplete or predictive text as we know it is differentiated from gpt style stuff?

Tess: right, like you said if you want to drop a hint for domain expertise. If we need additional controls we can add additional elements

Matthew: originally I thought ths has a11y considerations, but actually it doesn't because the browser is already shipping controls for this. But those are all for single or few word things. But if you could actually invite a whole paragraph or essay, there isn't a control that exists to do that.

Dan: sounds fine

Lea: is the idea that authors will opt into this, or that they will opt out?

Tess: both. Browsers might have it on for some areas and some off

Amy: so it's up to the browsers

Sanghwan: implementer defined, gives authors control over it. Better than now

Tess: scenario is the samea s disabling the system IME, maybe the site itself is doing it

Matthew: there is not a widget in OSs and browsers which would allow you to pick a writing assistant result

Tess: I wouldn't say that

Matthew: in that case maybe there are accessibility considerations. If this could be used to control the variety of different types of writing assistants, don't we want to say the user should be given that control? OS or browser setting

Tess: the attribute is a hint. the page is saying I'm doing something such that the system feature, if present, would interfer with the function of the page. It's just a hint. THe UA could decide to do it anyway, for the user.

Matthew: we can't tell the ua what options to have, but don't we want to use this opportunity to suggest the ua affords the user that choice? I want all these forms of autocompletion, except that one. Is that something we should suggest they consider including?

Tess: we could try to say something, but worried about giving advice that makes it less likely that their PR lands. Might be reluctance to add advice about user interfaces.

Sangwhan: and might be a much larger change to do it right. 

Tess: you end up with a potential explosion of the site wanting to say these but not this one, and the user the same.. gets hairy. The opt out is probably sufficient.

Tess: *drafts closing comment*

<blockquote>

Hi @sanketj!
  
@matatk, @rhiaro, and I took a look at this during a breakout at the TAG F2F today, and we're overall supportive of where you've ended up with the proposal. Have you run this by the i18n folk? We suspect they'll have relevant thoughts.

Thanks for bringing this to us. Please don't hesitate to ask us to take another look should things substantively change. 
  
Incidentally, we asked Google Bard to draft a supportive closing comment for us and here's what it came up with:

> **Strong support for writingsuggestions! Granular control & user/developer focus are excellent. Looking forward to implementation! @sanketj **
  
</blockquote>

## Bundling and caching again

Dan: Tess suggested splitting up bundling and caching and donig them one at a time

Tess: Dan suggested something similar to secure the web forward - the bundling case, we can make a stronger recommendation, which is now we're in a world with h3 and all these other things, bundling really is thoroughly obsolete and here's what to do instead. Maybe stronger than if it's paired with the partioning one, which is muddling. 

Yves: they have an implication on resource usage

Tess: I understand why they're together, butw e might be able to get consensus faster if we focus on bundling

Dan: and then we're making an impact. For https, there was a move to https already, and us putting out that we supported the move and why helped to move things in the direction they were already moving. If there is something similar we can do here to help the sustainability story by putting some momentum behind something that's already happening...

Sangwhan: I don't think it will help with the sustainability story, these are not validated ideas yet today, we don't have clear data.

Yves: it's at the point as when people were alerting that there were privacy issues by doing cookies, but still at the beginning, then work started later. We are at the point of alerting - that there are sustainability issues and maybe we can do better. But there's no driving forece in sustainability that would support that. SO I Don't think we're in a rush.

Dan: let's consider this in plenary, how to take it forward after Sangwhan's term ends

## Retro

### Topics

Suggested topics that were not chosen for discussion:

* Meeting times 
* "The firehose" - relationship with the blink project
* Meeting attendence *
* Agenda Creation & Tooling
* Scaling workload 👍＊*
* How we make best use of call time
* TAG red tape
* How we influence the technical direction of the W3C ***
* Communication responsiveness (async, seeing/responding to messages)
* FO councils *
* Commitments (time) ***
* Code of Conduct enforcement
* Is it TAG's responsibility to identify gaps in the web platform, and, if not, whose is it?
* TAG associates/interns/... **
* TAG's relationship to chartering
* Succession planning 
* Standings / enforcement 
* Prioritization *

Topics chosen for discussion from those suggested:

* TAG's relationship to the AC, and other governance bodies at W3C *** (influence technical direction, FOs)
* Review turn-around **＊ (scaling workload, firehose)
* Additional TAG responsibilities **👍 (charters)
* Candidate pools and the one-member rule 👍＊*

Rules for preventing round robin rabbit holes:

* 1~2 sentences per topic
* Don't repeat something someone else said
* CAn pass

### TAG's relationship to the AC, and other governance bodies at W3C (influence technical direction, FOs)

#### Went well

* Happy that Dan & Peter ran for and won election. That's improved the TAG's relationship with the AC and the team.
* Relationship with the AB in tokyo that allowed us to have more seats
* Most of the feedback from the AC on our work has been positive, including the latest member meeting where the privacy principles were raised. Positive feedback from AC members that we're doing the right thing.
* That there are calls for us to influence the technical direction of the web.
* Work done outside of TAG's usual comfort zone (e.g. ethical web principles) triggered the will for some of our bodies to work on the Vision document, and vision for the organization

#### Not so well

* The positive meeting mentioned was the exception; we don't put ourselves in the position to meet with the AB and AC often enough.
* That we didn't get the appointed seat we asked for, which resulted in confusion over should the appointed people run, and related rules 
* Getting involved in FO councils. Makes TAG political.
* There's still no mechanism for us to influence the technical direction of the W3C
* Nobody is identifying gaps in the web platform right now.
* Lack of concrete authority.
* We haven't met the new CEO.
* Poor election turnout (?)
* Conflicting opinions in governance bodies about what the TAG should be doing; TAG has not been engaged.
* Both chairs being forced to run in this election; could've lead to a catastrophic lack of chairing experience.

#### Solutionising

* We should be at the spring AC meeting every year; have a TAG f2f there (and commit to that).
* Explore the possibility of being looped in to FO councils only when the FO is technical.
* Prioritise our work to be mostly technical (relative to new responsibilities that the board and AB assign to us) - this will keep us as a technical body.
* We should have a plan for each AB-lead member meeting, for who's going to attend, and what they're going to present. We have experience of great feedback, and positive engagement. This will help us build better relationships with both the AB and AC.
* Identifying gaps should be an explicit work stream - even if the implementation interest is not there right now. (And trying to garner implementation interest.)
* Maintaining a living document detailing the skills and expertise of TAG members - this will help us clarify the responsibilities, and be more clear about what we can do, at any given point in time, and know what/when we need to outsource.
* We should attend the AB-lead member meeting each month. Not everyone on all call, but TAG should be present. Makes us visible to the body that elects us. Just that we should be on the call (not necessarily asking for agenda each time).
* We should dedicate some time to speak with the CEO regularly (dedicate time at f2f meetings).
* It should be part of the CEO's responsibility to speak regularly with the elected bodies.
* We should be involved with setting technical strategy for W3C.
* One of the ways gaps are filled is chartering new groups. It's opaque as to where they come from. Proposing that certain groups get chartered would help with both addressing gaps, and setting direction.

### Review turn-around (scaling workload, firehose)

#### Went well

* We resolved some reviews.
* That we have a large workload is a good sign of engagement - that people care about our opinion.
* Low plenary turnaround can help us close issues quicker.
* We managed to fast-track a few things.
* In general, we have a good trust culture within the TAG that has enabled us to close things in breakout sessions with fairly little controversy, because we all have a respect, and we know when to _not_ close something, and seek others' opinions.
* When we do fast-track something successfully, it reduces turnaround time by 88% on average.
* We make good use of the tooling, labelling, milestones, issue assignments, and mostly not dropping things into the abyss.

#### Not so well

* We don't turn them around. There are many that we don't turn around in a timely manner. Some get triaged; some don't; some fall into the abyss.
* We're often stalled on getting feedback/responses to our queries.
* We don't give up soon enough.
* We don't refuse to review things that might be a time sink for no gain.
* We don't like to say "no" - we don't like to say "we don't like this", so we keep padding things out.
* Most people ignore requetss for fast-tracking things. In most cases, it doesn't work because most people ignore the fast-track channel.
* We don't do a good job of differentiating between different types of review in terms of size, complexity, expertise, WG input requried, etc. at triage time, which impacts our ability to turn around reviews. The labels we have don't seem to make a difference to the action.
* One downside to having a firehose is that we're receiving so many design review requests that we spend all of our time on them, and don't do other work.
* We don't do enough homework before we start the review. Maybe one person has read the Explainer, maybe not. Often there's an early reason to reject. Our reviews end up shallow, which damages our credibility.
* We aren't good at timeboxing horizontal review requests.
* No way of scaling our ability to do reviews within our current process (response times posted on Slack). Our average closing time is very slow.
* We don't time-box discussions in calls so not all issues get covered.
* Several problems we have identified are in conflict with each other (review time to long; reviews too shallow; firehose is overwhelming) - solving for one may adversely affect others.
* We've become fairly beauraucratic. E.g. if there's something missing, like standards positions. Not giving the Explainer any credance because a different box wasn't ticked is easy.
* We can't really collaborate async. Had many attempts; it doesn't work.
* Some, perhaps many, design review requests are done as a box-ticking excercise, but there is not an intention to act on what we say.
* Sometimes the design review requester hasn't asked the WG that's incubating the thing about requesting a review.
* Our reviews are not balanced - because we are so pressed for time, we fail at the first error. E.g. if we spot a security/privacy issue, we don't perform an API design review.
* Other browser vendors don't send us reviews.
* The design review requests we get are disproportionately from one vendor (due to their process) and have not been vetted.
* We go into the weeds about miniscule details that are not high-impact.

#### Solutionising

* More formal system of pairing of reviewers per issue. Incl consideration of mentoring/sharing knowledge, and load balancing.
* From time to time it's good to have more than two people reviewing an issue.
* Letting go earlier. We have concenrs, but no concrete solutions, but we hold on to issues for a long time sometimes.
* Could we engage the other W3C horizontal review groups to free up some of our bandwidth for overarching architecture.
* We've tried a lot of things....
* We can have a standard procedure/perspective on certain requests. We already have some of them, and can continue building/maturing these template responses.
* If for a certain review request, we have no expertise, we can invite experts from W3C community (e.g. the WG chairs/other experts). Could have an invited experts team / consulting team / pool.
* We could not do as many reviews / ask for organisations to internally vet their review requests before they come to us.
* Do more work at triage time to understand the work required for a review. We often discovere in a meeting that it's missing some critical info, or we are missing some expertise.
* We could suggest implementers have an "everything that needs to be interoperable should go through the TAG" rather than "everything should go through the TAG" (alternate related suggestion: "experiments").
* Having a more formal way to bring the requester into interactive discussion with the TAG. (E.g. joining call; being on slack; ???)
* We should try again with fast-tracking things. Do more work at triage time (as above) and turn around in a week.
* We shouldn't be reading Explainers during triage time - we should read them in advance. (I.e. there should be an obligation on members to put this time in.)
* Some of the long turnaround times are fine (some of those are not design reviews; some are difficult problems that required time to solve). Some 2-5mo ones may be problematic - and for some of those, saying "no" may've been apt. Additional observation: the backlog is not increasing - so whilst there's a problem, it's not a crisis.
* Make multiple versions of the design principles document - and distill them/it down into a self-review checklist.
* More work on classification of review requests - e.g. we could create standardised categories for all the requested reviews. Need to carefully discuss those categories. The external experts (above) can be grouped by category.
* We should use our meeting time with more discipline - timebox agenda. A lot drop off/get punted and that causes delays that aren't carefully considered - they're because we didn't look at the issues. If something will take a long time, schedule that explicitly.
* Especially for specs going through HR, we've done a lot of security review because it's been missing. Privacy and security should be starting again soon, freeing up some time for us.
* We don't communicate well that "this one will take some time". This is a reputational issue too.
* Deadlines/priorities for reviews.
* More retrospectives about how to work better - more vigilance about execution of these plans.
* Accept that reviews will be be done synchronously and plan arround it by allocating fewer reviews per call and aggressively prioritizing. Mandate shorter explainers/explainers with suitable summaries to begin with.
* We've tried processs to do stuff async, so that we can spend time better in meetings. But people don't follow slack etc. so it doesn't work. Enforce "notifications on" time.
* Create a process where we train community members to do an initial pass over the reviews, and we do QA on those. Investigate use of ML as a tool to help us (nothing facing the requester).
* wrt failing early on reviews (aborting review before API design if privacy issue found) Rate APIs on different factors - e.g. privacy, API design, etc. (i.e. a scorecard)
* Understand the difference between a showstopper for a _review_ and a showstopper for a _spec_.

### Additional TAG responsibilities (charter review, FO council, ...)

#### Went well

* We reviewed a charter.
* It was possible to avoid the need to go to a FO council on some occasions.
* TAG's assistance in resolving FOs helped with making resolutions.
* The council dismissal process has been shown to have positive elements (short-circuit, delegation).
* Every single council that we've sat on since first one has gone well - the contributions from TAG participants helped with a good decision.
* Design Principles week has gone well - been very helpful in carving out time.
* Taking on the council work has improved our relationship with the AB, and improved awareness of us and our expertise, and improved our abiltiy to chime in on cross-W3C things.

#### Not so well

* It feels like there are too many people on the councils - from an effective time management perspective.
* Only looking at Design Principles once per month lacks continunity. Isn't frequent enough. Can't catch up with reviews.
* We get blocked on councils because we can't find a chair for the council.
* Too much red tape for councils.
* Much council discussion is political, not technical - we don't have a lot to add.
* Tension between taking out additional responsibilities, and our existing responsibilities - including design reviews.
* There's not consistency about how and when we do charter review.
* We don't have TAG consensus about what our primary deliverables are. E.g. some think it's the Design Principles (which are informed by reviews), but some don't. Without reaching consensus on this, we will not be able to make progress. (We don't have consensus on what is an additional, and what is a main, responsibility.)
* Charter creation is an opaque process. Conflicts with our need to be transparent.
* Tension between TAG not having time to do its own work, the council work, adding reviews for charters, potentially other things, and the size of the TAG and mythical man month.
* For a technical architecture group, we spend little time on technical architecture. We spend a lot of time on tactical, rather than strategic, work.
* When a TAG participant is also an AC rep - in combination with council - is distorting decision making. Conflict of interest from TAG members who want to make FOs.
* The trend is for more being expected of the TAG. Funding the time / recognising our commitment - can be challenging.
* If we are to be in a critical role in charter review, the consensus of the TAG must be respected.

#### Solutionising

* We need to reach out to W3C management to figure out a better way to get the TAG engaged in charter creation - e.g. give the TAG a heads up that a charter is in development. (Additional: some tooling options may be available.)
* Investigate delegation of council duties to a subset of TAG with interest/expertise in the particular issue.
* Consider abstaining/recusing ourselves from councils if there's nothing we can add - especially if political. (Addition: council time is a personal burden)
* Could discuss FOs in the TAG and then delegate one member to join the council.
* When we signed up, we committed to a certain number of hours per week. We cannot get more. When being asked to do more things, we need to ask W3C management/governance what to drop.
* For councils, it would be better to be framed as a request for input from the TAG (with details provided for async consideration) - rather than an obligation.
* Investigate improving the council process, so that finding chairs is easier. (Additional: some people may be willing to say yes if asked.)
* Investigate how to reduce the number of councils. Discourage use of councils generally. Focus on resolving conflicts in WGs, leave responsibility with chairs and staff contacts as much as possible.
* Investigate having councils chaired by a neutral party (from the team, or external to W3C).
* Attending councils presents significant barriers for some people (including those for whom English is a second language), depending on where they are (time zones). Investigate running councils async.
* Use a random subset of the TAG, AB (etc) to form councils, like jury duty.
* Investigate making councils f2f - e.g. having scheduled slots during the year.
* Investigate funding of any f2f councils (or parts thereof) by objectors.
* Only invite TAG to councils that are technical in nature.
* Streamline the recusal process. Particular problem point is the collecting of rationale from one group, and how it's presented to another.
* reduce the number of people involved... we're not obliged to participate... we can opt out... AB needs to be on the same page. Action: write these suggestions up and bring them back to the AB/TAG...
* Recognise that a council is a totally separate entity to the TAG/AB - it's a group that is formed from individuals from these other groups. Make this clear to everyone, so they understand it. E.g. councils can cross TAG/AB terms.
* W3C should create budget for AB and TAG (likely separately). (Context: The extra responsibilities being asked towards elected bodies for are effectively "free labor" as far as W3C goes.)

### Candidate pools and the one-member rule 👍＊*

#### Went well

* Not flooded by people from a single company / Prevents big companies from having multiple seats.
* Enforces diversity of point of view; reduces bias; more solutions considered.
* Enforces us to expand our search radius for candidates.
* The single affiliation limits helps us to prevent even the appearance of bias towards one single entity - especially to regulatory bodies, etc...

#### Not so well

* Very hard to find people who both have the right expertise (breadth and depth), the time & willingness to contribute it, and the funds and ability to travel, and they tend to disproportionally congregate in specific companies, so in practice while well-intentioned, this ends up depriving the TAG from a lot of talent.
* Can be detrimental to the diversity of the TAG (under-represented groups etc.)
* We didn't spend enough time reaching out to people from different areas, who may have the knowledge to contribute to the TAG.
* Sometimes our search fails.
* Sometimes the constraint causes individuals difficulties in finding jobs.
* The affiliation limit, when combined with STV as the election method, can produce negative outcomes. E.g. it can be hard to get two similarly-qualified people in any given election cycle. This can impact diversity too.
* The appointee process is difficult as it's unclear what role the TAG members should be playing with regard to the appointees (the Team is to make the appointments, but not clear what TAG input is possible). The affiliation limit can affect this. Are TAG members engaging enough with the web community?
* Certain members have a stigma associated with them such that increasing the limit even to 2 is not considered acceptable.
* We're not getting people running for TAG because there's already someone from that employer - instead of the AC making that choice, the employer is a priori.
* W3C isn't willing to support qualified people who are willing to put in the time and do the work - on an activity that's on the critical path.
* TAG members aren't supposed to represent their employer, but we also have the rule that there can't be multiple people from one employer - these may contradict each other, one dilutes the other.
* There isn't any effort to nurture a candidate pool.
* Candidates aren't necessarily voted in on their expertise. The process is prone to tactical voting.
* The lack of support and incentive structure for participating inherantly excludes people who are already disadvantaged, which creates a vicious cycle.
* Geographical and cultural diversity is not considered enough.

#### Solutionising

* TAG needs to engage better in wider web community to find potential candidates (restart Meet the TAG events?)
* Make it clear we can have nominees from multiple companies?
* Make the affiliation limit only apply to elected seats, so that the pool of possible candidates for appointment is larger. (or apply the affiliation limit within the elected seats and a separate limit within the appointed seats, etc.)

### Actions

* Discuss chartering involvement further in TAG future session
* Plan for getting us to do less security/privacy review? (by other horizontal review groups doing it)
* Dan and Peter take suggestions for council improvements, feed back to the AB, then back to whoever is in charge of the process for this

## TAG Future

Present: Dan, Amy, Tess, Peter, Max, Martin, Matthew, Sangwhan, Yves, Hadley, Lea

### Meeting times

Dan: intro on current status...
Used to do 1h30 a week.  Was terrible.
We moved to 1h a week, planned to do ad hoc breakouts, but didn't.
We then scheduled breakouts.
We have dropped some breakouts, where we have breakout A and C and a plenary call every other week.
The problem is that we still don't have consistent participation in calls and often have an agenda that has items for one person and they don't turn up.

How do we make it better?

* Use modern calendar tool rsvps
* Maybe there's no way to have a plenary that everyone will join? Anything that requires resolution from the entire tag should be done async or f2f, and we have only breakouts for two timezones to get together: US/EU, EU/APAC, APAC/US. Our plenaries at the moment are breakouts.
* Fewer plenaries and more emphasis on rotating breakouts
* Find a better way to work async
* One-on-one sessions betwen specific people at more convenient times
* How to accommodate different work modes of different people (sync vs async especially) - no one size fits all
* Be more reactive when we see something is not working
* Regional f2f coworking more frequently
* Survey what times people are available - general times/range
* If mandatory attendance was one breakout and one breakout, and time to do homework - allocate the other breakout time to homework?
* Shared understanding of expectation of hours?
* Plan around the fact that some people won't make meetings
* Pick set times to meet and do work, if you can't make it at that time you shouldn't be on the TAG
* Find better tools for async working.
* ONly use calls for things that cannot be done async
* async parts of different reviews could be done separately rather than waiting to be all together - one person does privacy, then hands off to next person for api design, and so on (needs to be clear to requester what is happening)
* quorum - lower barrier for individual or pair reviews
* call times oriented around timezone groups and make the into invites that people respond to, to help chairs make agendas
* tailored agenda to people who can attend
* get rid of daylight savings
* figure out which reviews we can progress in smaller groups or individually, even if it's not all of them
* have more breakouts than we need and people attend what they can and keep track of attendance as one data point
* downsides to smaller groups - fewer perspectives; fewer opportunities to share information. Opportunity to share more information.
* could do each facet of the 'score card' in small groups or async, and they have a whole review when the score card is filled in
* knowledge sharing == capacity building
* plenaries with a theme: "this is what I learned from..."
* dashboard with due dates / deadlines / milestones / etc

Summary:

* Improve async working
* Fewer people in more breakouts for sync working (determine how much is needed)
* Less frequent but better attended everyone plenary - not design reviews, but making decisions, educating each other
* RSVP to breakouts ahead of time so agenda can make sense

## 10a

Present: Dan, Yves, Sangwhan, Lea

### [Web Audio API: User-Selectable Render Quantum Size](https://github.com/w3ctag/design-reviews/issues/895)

Yves: it looks like it makes sense... I looked at it before and felt it looked OK.

Sangwhan: there is a user need.  This is well thought-through.

Yves: It's mostly hints so there is an implicit graceful degredation....

Sangwhan: agreed... the application should have a right to request... I'm an LGTM.

Yves: Same.

### [coop restrict properties](https://github.com/w3ctag/design-reviews/issues/760)

*dan leaves a comment since it looks like this may have been overtaken by another proposal*

### [webapp scope extensions](https://github.com/w3ctag/design-reviews/issues/875)

Yves: i view this as having the same security problem - trusting the origin - as miniapp...

Sangwhan: *[leaves comment](https://github.com/w3ctag/design-reviews/issues/875#issuecomment-1909989403)*

### [The FileSystemObserver interface](https://github.com/w3ctag/design-reviews/issues/868)

Sangwhan: I am OK with this

Yves: use case is OK....

Yves: it says on the local file system... def of local file system may be Origin-controlled.  Looks OK but depeneds on whether other stakeholders... 

Dan: does it have a dependency on local filesystem?

Yves: no.

Sangwhan: no.

Sangwhan: I'm looking at the API to see if it makes sense... API looks good to me.

Dan: please add some wording to encourage continued engagement with additional implementers...

Sangwhan: *closes*

### [supported clipboard formats redux](https://github.com/w3ctag/design-reviews/issues/868)

*lea shares comment*

### [naming factory methods](https://github.com/w3ctag/design-principles/issues/378)

<blockquote>

Start factory method names with `create` or `from`
=================================================

When defining a new factory method, prefix its name with either `create` or `from`.

If a factory method constructs a new empty object,
prefix the method name with `create`.
However, if your factory method creates an object from existing data,
prefix the method name with `from`.

Factory methods should be the exception, and not the norm.
An example of valid usage of a factory method is
when an object is being created it also requires association
with the parent object.
`document.createXXX()` is an example of this.
The prefix `from` is expected to be used
when there is a source object expected to be
converted to a target object.
For example, `Foo.fromBar()` would imply
that a `Foo` object will be created using a `Bar` object.
 
Inventing other prefixes
and usage of legacy prefixes should be avoided
unless there is a strong reason to do so.
Consistency with existing factory methods under the same object,
such as `document.initXXX()` would be an example of an exemption.
New factory methods should not follow this convention.

</blockquote>

## 12a Design Principles

### [Guidance for Factory Method Naming](https://github.com/w3ctag/design-principles/pull/471)

*we work on this and agree to land*

### [data minimization](github.com/w3ctag/design-principles/pulls/465)

*we work on this and agree to land*

### [identity & the web](https://github.com/w3ctag/design-principles/pull/396)

*we review Amy's latest revisioms*

Consensus that we should add this but we agree it needs one more round of tightening...

Matthew: Not entirely sure if this is relevant: https://blog.mozilla.org/netpolicy/2021/11/04/mozilla-publishes-position-paper-on-the-eu-digital-identity-framework/

## Fin.

RESOLVED: Gratitude to Tess for hosting us abounds.







