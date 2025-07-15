# TAG Minutes - Week of 7 July 2025


## Breakout A (Asia / Australia / West America) - [2025-07-08](https://www.timeanddate.com/worldclock/converter.html?iso=20250708T030000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present:

Regrets: Jeffrey, Xiaocheng

Scribe:

### Prioritize issues in https://github.com/orgs/w3ctag/projects/6/views/1. 
### [design-reviews#831: Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @jyasskin, @torgo, @marcoscaceres
### [design-reviews#1093: Prompt API](https://github.com/w3ctag/design-reviews/issues/1093) - @martinthomson, @jyasskin, @marcoscaceres
### [design-reviews#991: Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @martinthomson, @jyasskin, @marcoscaceres
### List our active Finding drafts, and look for some issues on them that ought to be prioritized in future meetings.

## Breakout B (America / Europe) - [2025-07-09](https://www.timeanddate.com/worldclock/converter.html?iso=20250709T170000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Lola, Yves, DanC, Matthew

Regrets: Jeffrey

Scribe: DanC

### Prioritize issues in https://github.com/orgs/w3ctag/projects/6/views/1. 

Matthew: Idea for https://github.com/orgs/w3ctag/projects/6/views/1 is you
look at things in the New column, can assign yourself to things, and claim
them for a particular breakout.

Lola: https://github.com/w3ctag/design-reviews/issues/1108 doesn't have anyone assigned.
It's a bit old. Doesn't seem to have been discussed.

Matthew: I'll search in the minutes if this was discussed.

Lola: It introduces new strategy for loading ServiceWorkers.

Yves: Might be interesting race conditions here. So let's add Ehsan?

Matthew: Will find his github @ and assign.

Matthew: Discussed [ServiceWorkerAutoPreload](https://github.com/w3ctag/design-reviews/issues/963) in 2024, resolved as too early.

### Canvas text metrics: https://github.com/w3ctag/design-reviews/issues/1095
Lola: This is waiting for response to Jeffrey's comment.

### https://github.com/w3ctag/design-reviews/issues/906
Lola: Messaged DanA, he was going to leave closing comment. Hasn't yet and he's
on AB now. Asked him if there's anything else he wanted to include, I will probably
write closing comment but waiting for proper response from DanA, so tabled for now.

### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085) - @torgo, @matatk, @toreini

Matthew: We discussed this, couldn't find when. We agreed to do something specific.
Does anyone know when we discussed?
<Found at https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/06-30-minutes.md#design-reviews1085-wgwebauthn-web-authentication-level-3---torgo-matatk>

Lola: Did he manage to look at this then?

Matthew: Yes, he left feedback in brainstorming thread.
Not clear what next step is. Probably not going to wait for Privacy WG.
Before last week I recall we wanted to know rationale for changes. Did we get that back?

Lola: Can you give overview of what the issue is?

Matthew: That's what we asked them to do.
Different of us had questions like is this the next logical step for level 3?
Were there issues discovered that needed fixing, or things we wanted to add?
Reply was that there was big discussion with team including Tim, but not up-to-date
with what happened in that breakout

Lola: I'm sure we have minutes

Matthew: Yes but we should talk with someone who was in that breakout.
All the stuff SM raised in the breakout has been there for a while.

Lola: In the private repo maybe we just put a note. I'll leave a comment for Jeffrey
in private brainstorm repo if we should discuss this when he's back.

Matthew: He would have been on that call.

Lola: Are we happy to wait for Jeffrey?

Matthew: Yes

Lola: Would Martin have been there? Could add to tomorrow's call.

Matthew: Suspect he might have been. But minutes say no, was from the week before:
https://github.com/w3ctag/meetings/blob/gh-pages/2025/telcons/06-23-minutes.md#special-guests-design-reviews1085-wgwebauthn-web-authentication-level-3---torgo-matatk
Don't see any agreement on next steps in there.

Lola: Adding it to tomorrow's agenda, we'll discussed with Martin.

### [design-reviews#1107: echoCancellation mode](https://github.com/w3ctag/design-reviews/issues/1107) - @matatk, @christianliebel

Matthew: Christian posted comment that everyone is happy with. Should we give him the
chance to post it? Is he away currently?

Yves: On vacation, he might be back next week.

Lola: He probably mentioned it in person.

Matthew: How about if he's on tomorrow, he can post, otherwise I'll post and credit him.

Lola: Is there urgency to this? It's been 3 weeks. If Christian is not here tomorrow,
Matt you can post.

### [CSS Overflow Navigation Controls (Carousels) #1037](https://github.com/w3ctag/design-reviews/issues/1037)

Matthew: Would be good to discuss with Lola, Jeffrey, Xiaocheng.
Don't want accidental uninterting. They decided to mirror the HTML attribute.
That seems like a good thing for accessibility. Not sure how we feel about the rest of it.
But that's the biggest change. Immediate changes for us would be, is this enough? Sufficient to make TAG happy or satisfied with concerns?
Next question would be, is this how it's going to stay? Maybe this is a pause rather than
a change of direction. On that front, want to share a link, they're discussing in HTML
and we just talked about it in APA call.
Connect HTML spec up to new CSS interactivity property #10956
 https://github.com/whatwg/html/pull/10956 does the harmonization between and HTML and CSS.
 What we want to figure out is, are they specifying this in terms of how HTML has always been in that you can't uninert stuff,
 or does this override the change we liked in the carousel space? Will this revert back to
 it being uninertable via CSS, or will it be the behavior we do want? Discussion is ongoing?
 
 Lola: First question is, is this enough. I don't think so.
 In the final comment, @flackr says we are going to explore some things.
 They've updated explainer with alternatives considered.
 There are still additional properties they're exploring.
 Not sure if you've read https://www.sarasoueidan.com/blog/css-carousels-accessibility/#update%3A-may-29th%2C-2025. Sara is a11y expert. She has written this
 post breaking down all the issues with CSS Carousel in lots of detail.
 
 Matthew: I've seen this, she's got the same concern where CSS is now in the business
 of adding roles to elements. They're already adding roles to pseudos, but adding roles
 to acutal elements is even worse.

Lola: Opens the door to mismatch of responsibilities. Things that HTML is responsible for,
that CSS is responsible for, carousels wants to step into HTML's territories.
So I'm opposed to this implementation of CSS carousel's as-is.
Don't think the fixes to inert is enough based on this.

Matthew: I agree. Need to confirm about the roles stuff, but seems wholly inappropriate
if they're doing that. Doing it with pseudos is already blurring the line. If they
start doing it with elements...
The other thing is, they're giving devs a choice between exposing as tags or links.
Not good. CSS liason mentioned that Scott O'Hara mentioned, that the thing where they
want to auto-inert slides that aren't in view, from some perspective that seems reasonable, it completely breaks virtual cursor. E.g. if you are iOS voiceover user, getting to next item , you can't do it because it's not in a11y tree anymore.
Some users it would be better for, but for significant number it's worse.

Lola: Sounds to me like this tech is not ready. Not ready to be standardized at least.

Matthew: It worries me. I appreciate the progress with moving away from JS, like anchor pos is great, grid, but they've bitten off complicated widget pattern. I wanted to be supportive of it
because devs want to do this and it gets done poorly, so if we can make it suck less and it
can be more accessible that's good. But the more we go into it it seems less like that's happening.
They've shipped so much, and in a generalized way, the parts don't add up.

Lola: My position is, regarless of what they've done and plan to do, this is TAG's position.
Doesn't mean we have to back it. My position is it's not ready.
A concern I have as well is that there don't seem to be many a11y pros in the CSSWG.
It's one of the bigger and more active WGs in the W3C. We don't want to take on too much
work and have expectation that TAG will come into your WG and personally direct things, but
there needs to be a requirement now that CSSWG needs people to participate to give a11y guidance.

Matthew: I have action points for what you suggested.
I will check up on the business of giving roles to elements from CSS.
While drafting the comment we can also show it to Alice.
On subject of getting more a11y representation in CSSWG, yes. Paul Grenier is participating and flagging stuff to APA. We need to find a way to support CSS and get that feedback ASAP.
They're attracting people who know stuff -- Scott, Sara, Paul...maybe they're attracting them too late.
APA is also struggling with this. Only finding out about it after it's shipped, only hear about it because of Paul. But too late. So part of the answer is to encourage people to 
go through a11y review sooner, through TAG or APA.

Lola: Makes sense to me. Who are the CSSWG chairs, can we reach out to them? Alan Stearns, Rossen Atanassov.
Immediate next steps: let's figure out the comment we want to leave on this.
Should discuss with more of the group. Let's put it in next plenary.

Matthew: Are we saying, by next plenary, we have draft comment on this?

Lola: Yes if it's not too much. Else we should have a position at least. I will add to agenda for next plenary.

Lola: Concern of possible antagonism between CSSWG and APA.
Worried about the feedback we’re seeing from a11y pros.

Matthew: The outcome of getting more a11y review is great.
But issue seems to be mainly with features that come to the CSSWG already largely complete. The issue is not with the CSSWG itself, who has members that care deeply about a11y.
Talking with the chairs could help alleviate this.
Process improvements about CG's is good, about stuff getting more scrutiny as it gains "traction", and defining what "traction" means.

Lola: CSSWG gets stuff as first point of access, right?

Matthew: Right, so those process changes wouldn't help here. But would they if there was a CSS CG?

Lola: Privacy CG does this well. Other people are thinking about this -- maybe we can discuss at TPAC.


### [explainer-explainer#7: Explain why to focus on the end-user's need, and/or moderate that advice](https://github.com/w3ctag/explainer-explainer/issues/7) - @torgo
### [design-reviews#906: Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @zcorpan, @torgo, @lolaodelola

### FedCM
  * [design-reviews#974: FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974) - @torgo, @hadleybeeman
  * [design-reviews#945: FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @torgo, @hadleybeeman
  * [design-reviews#935: FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @torgo, @hadleybeeman
  * [design-reviews#803: FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @torgo, @hadleybeeman
  * [design-reviews#992: FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @martinthomson, @torgo, @hadleybeeman

## Breakout C (Europe / Asia / Australia) - [2025-07-10](https://www.timeanddate.com/worldclock/converter.html?iso=20250710T090000&p1=224&p2=43&p3=136&p4=195&p5=33&p6=248&p7=240)

Present: Christian, Xiaocheng, Matthew, Ehsan, Marcos, Martin, Yves, Lola, Hadley

Regrets:

Scribe: Christian

### [design-reviews#1085: [wg/webauthn] Web Authentication Level 3](https://github.com/w3ctag/design-reviews/issues/1085)

Lola: Were there any next steps from the meeting?

Martin: Need to check. Don't think it's resolved, some things were misunderstandings. Don't know to do with that one.

Lola: Wait for Jeffrey.

### Prioritize issues in https://github.com/orgs/w3ctag/projects/6/views/1.

(skipped)

### [web-no-papers#10: Adding a conclusion](https://github.com/w3ctag/web-no-papers/pull/10) - @torgo

Lola: DanA wanted to…

Martin: Would like to drive it to completion, travelling over the next weeks, can talk about personally in London next week, not set up yet.

Lola: Will get reacquanited with that and reach out.

Matthew: Sounds good.

Martin: Will send a note in Slack.

### [web-no-papers#9: Add passport use case](https://github.com/w3ctag/web-no-papers/pull/9) - @torgo

(see above)

### [accessibility-questionnaire#7: Clarify title, and scope](https://github.com/w3ctag/accessibility-questionnaire/pull/7) - @matatk, @matatk

Matthew: Finally figured out GitHub web UI for changes, found wording for Martin's proposed approach. Liked the collaborative angle. @Martin: Would you be ok with us adopting the type of framing and adding the tracker label for APA?

Martin: This is reasonable.

Matthew: Rationale for having this in APA is being helpful for spec authors.

### [design-reviews#1084: media-playback-while-not-visible Permission Policy](https://github.com/w3ctag/design-reviews/issues/1084) - @ylafon, @marcoscaceres

Marcos: Didn't have the time yet.

### [design-reviews#1117: Add IndexedDB getAllRecords() method and update getAll()/getAllKeys() to support direction option](https://github.com/w3ctag/design-reviews/issues/1117) - @christianliebel

Christian: Only halfway through, getAllRecords() seems fine, but the changing the existing methods needs a deeper look.

Lola: Do people want to join this issue?

Martin: I would love to join. Also think that the changes to existing methods need a deeper look.

### [design-reviews#1118: [wg/webapps] Web Applications Working Group Charter](https://github.com/w3ctag/design-reviews/issues/1118) - @christianliebel

Christian: I'm a participant of this WG, but happy with it. Only a small change, and it makes sense.

Hadley: No need for anyone else to look; maybe ask if you think others need to look at it.

Yves: Fine process-wise.

Christian to close the issue as satisfied.

### [design-reviews#1116: TAG review for Local Network Access(LNA)](https://github.com/w3ctag/design-reviews/issues/1116) - @martinthomson, @ylafon

Yves: Martin made a proposal last week that demonstrates the concerns with the user prompt. Comment is perfect, we should close satisfied with concerns as proposed by Martin.

Martin: Will do, just processing Jeffrey's comment.

Lola: Inclined to defer to the both of you, or do you want to wait until Jeffrey is back?

Yves: Don't think Jeffrey would mind, but we could wait.

Martin: Think Jeffrey was fine with posting.

Yves: Think it is more an experiment at this stage.

### [design-reviews#1037: CSS Overflow Navigation Controls (
els)](https://github.com/w3ctag/design-reviews/issues/1037) - @matatk, @lolaodelola, @xiaochengh

Lola: Matthew and I spoke about this yesterday, want to include Xiaocheng. Essentially, the question was: Is this enough? There is another issue somewhere else (https://github.com/whatwg/html/pull/10956), but haven't linked that. Don't think this is enough. There are other significant issues.

Xiaocheng: Also went through the minutes, what you discussed makes sense. Are we ready to post a response? What should be our position? Keep working with them? Satisfied with concerns?

Matthew: +1 to what Lola said. Think Alice is not happy with it. Problem of uninerting in CSS. 

…Yesterday we discussed that we should draft a comment for the plenary next week. Want to clarify some things first.

…Cascading attribute sheets could solve problems like this in the future. Might be that we ask them to not do carousels and refer to the attribute proposal.

Lola: Having more information or a proposal to review would be great.

Xiaocheng: Fine for me, don't have additional ideas.

### [design-reviews#1089: Extended lifetime shared workers](https://github.com/w3ctag/design-reviews/issues/1089) - @xiaochengh

Xiaocheng: Didn't have time to look at this. I'm aware that Martin and Jeffrey proposed another alternative.

Martin: Might be very close to what they're proposing, may not actually be an alternative.

Xiaocheng: Fine if we post a response with the alternative. Another question: For this review we have been proposing a lot of alternatives. Looks like we're showing a strong opinion that we don't like the approach.

Martin: Don't really agree. Questions: What do you do at creation time?

… uses an extendable Event to keep the worker live, just like SW?

… Difference is extension by default in their proposal and not in the alternative …

Lola: Worth asking if they've considered a secondary API?

Martin: Think we can just ask the question if they've considered that. We should respect their position here: they are the experts in this area.

Xiaocheng: Still have a doubt about proposing yet another alternative.

Lola: Think it's fine to ask for alternatives. If they haven't documented that alternative, it's not wrong to ask.

Xiaocheng: Need to think about it, think there should be a boundary between thinking about alternatives and finetuning the API shape.

Lola: Can Xiaocheng and Martin discuss this offline?

Martin: Yes. I'll defer to Xiaocheng on this one.  We should not engage in an unhealthy interaction mode.

### [design-reviews#1115: Expose unprintable areas via CSS](https://github.com/w3ctag/design-reviews/issues/1115) - @xiaochengh

Xiaocheng: This is an early design review. Motivation is that, when printing a page, we want to avoid areas that are not printable due to restrictions by the printer. Think their use case is solid. Adding this new API seems reasonable. Slightly increases fingerprinting surface.

Martin: Can sites really read back the value when it goes to a printer? Expect the answer to be no. All the interactions after printing are happening between the browser and the printer. Don't think that happens… do we know the format? The amount of pages?

Lola: If you are on a site that is about printing, maybe they have to give them the information.

Martin: That is in the page setup instructions in CSS, but it's all static between HTML and CSS.

Christian: Think there's a beforeprint event which you can use to change stuff before the site is printed, need to check.

Xiaocheng: Discussion may be a bit off-topic. Is this really a privacy threat? Don't think so. Comparable to safe-area-inset. Would also be part of the fingerprinting surface.

Martin: You can read this back, but I'm not sure if it's entirely reliable. The rules for which stylesheet applies only gives you one shot per print, so it may not be worthwhile.

Lola: Propose Xiaocheng leaves a comment. It's worth asking them about potential alternatives. Think we can resolve this as satisfied if everyone's happy.

Martin: Think they've discussed multi-page prints. … Think that's a good sign.

Xiaocheng to post a comment that we're positive with their direction.

### [design-reviews#1111: Declarative Interactions](https://github.com/w3ctag/design-reviews/issues/1111) - @xiaochengh

Xiaocheng: Motivation is they want to play animations … very common pattern when you interact with certain parts of the page that they show animations. When you click a button, some element nearby is rotated by a certain angle that indicates the element has been clicked.

… Currently, events and JavaScript have to be added, which isn't great. They are proposing a declarative syntax in CSS to allow triggering such animations completely off the main thread. 

… Regarding their direction, I think this is good, like it a lot. Like when offloading work from the main thread. Starting/stopping an animation is a very traditional topic in CSS.

Martin: What's your view on the name? Right now, it has an animation trigger. One element triggers the animation of another element. Name here seems to add another layer of indirection. May be appropriate? You can have multiple elements to trigger the elements, and multiple elements to respond to the same name… many-to-many relationship.

Xiaocheng: Think they are proposing a many-to-one relationship…?

Martin: They are using ID selectors, but they could be class selectors.

Xiaocheng: Not following what you meant by using a selector? Does this change the relationship?

Martin: No, doesn't change the relationship. … (Can name be replaced with selector?)

Xiaocheng: Replacing the name with a selector? Think they follow the design of anchor positioning. Think they want the trigger element to be unique. Selector might match multiple elements.

Martin: But that could happen with the name as well, as it has a selector attached to it. Right now, they have an ID selector, that's probably only one thing. But if it was a class selector, it could match more elements than one.

Lola: But shouldn't that be left to the developer to decide? What's the impact?

Martin: Is the extra layer of indirection adding value in some way? Not sure what the value of adding the indirection is.

Matthew: See what you're asking, Martin. Should ask what the rationale is. Related question: Struggling to find the bit where they allow other triggers than just click. Can't find where this is specified. Explainer doesn't mention it either.

Xiaocheng: This is where I want to raise a concern. Didn't find it at first as well. Assume that the trigger functions should match the event names in UI Events. Don't think every UI event qualifies as a trigger. Think this part is underspecified.

… Related concern is this is adding coupling between CSS and UI events spec. Not sure if that's a good thing. Wondering if there's a way to define the trigger functions to not couple with UI events spec.

Martin: Can we replace this behavior with existing capabilities? For example, when clicking something, it gains focus, that could change the DOM, activate different CSS, and thereby trigger an animation.

Xiaocheng: Can this avoid the main thread?

Martin: Think so! There'a brief hit on the main thread, as for any action. But the event doesn't necessarily have to invoke JS, but the DOM instead.

Xiaocheng: Think they're trying to trigger UI events in the compositor thread without redefining UI events.

Lola: In terms of next steps, I think we cannot close this yet. Sounds like there's concerns around the design of trigger functions. You can write a comment to put that back to them.

Martin: Just trying to help out… They have drafted some specs, but they didn't incude links in the explainer. Needs more clarity. Looks like someone had an idea. Might need more discussions.

Lola: Is this an early review?

Martin: If it isn't, it should be one.

Xiaocheng: Is not marked as an early review.

Lola: Doesn't look like other browser vendors were involved. Wait for what they respond. Don't think we can close this for now.

### F2F Clarifications

Lola: 15–18 September, don't have any information on accomodation etc. @Xiaocheng: Would it be possible to get a list of hotels near the venue? Public transportation etc.

Martin: There's a hotel 10 mins by bus. Cluster of hotels. Buses seem to be very good.

Xiaocheng: Will contact our teams to get some information. Please reply in the F2F thread so we know the number of people coming.

Hadley: Creating a page in our meetings repo would be great.

## Plenary Session - None


Design reviews for which we're inviting guests in a future meeting:
* [design-reviews#1058: The `interesttarget` attribute](https://github.com/w3ctag/design-reviews/issues/1058) - @matatk, @xiaochengh
* [design-reviews#1015: Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @jyasskin, @torgo, @csarven, @maxpassion, @hadleybeeman

