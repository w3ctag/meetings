# TAG Teleconference
#### 18-20 November 2024

---

## Agenda:

### Breakout A (California / Europe)  - [2024-11-18](https://www.timeanddate.com/worldclock/converter.html?iso=20241118T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk
* [Customizable select element](https://github.com/w3ctag/design-reviews/issues/1007) - @LeaVerou, @matatk
* [Review for Protected Audiences Bidding and Auction Services API](https://github.com/w3ctag/design-reviews/issues/1009) - @jyasskin

### Breakout B (California / Australia) - [2024-11-19](https://www.timeanddate.com/worldclock/converter.html?iso=20241119T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin
* [CSS Masonry Layout](https://github.com/w3ctag/design-reviews/issues/1003) - @jyasskin, @LeaVerou
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

### Breakout C (Europe / China) - [2024-11-20](https://www.timeanddate.com/worldclock/converter.html?iso=20241120T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion
* [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996) - @maxpassion
* [EPUB 3.3 Recommendation with Candidate Corrections  2024-10-17 > 2024-12-19](https://github.com/w3ctag/design-reviews/issues/1006) - @rhiaro, @hadleybeeman

### Plenary Session - [2024-11-20](https://www.timeanddate.com/worldclock/converter.html?iso=20241120T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [ Vision for W3C: request horizontal architectural review and wide TAG review](https://github.com/w3ctag/design-reviews/issues/1008) - @hober, @jyasskin, @rhiaro
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Matthew, Tristan, Jeffrey, Amy, Tess

Regrets: 


### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk

Matthew: Martin had a [question to ask](https://github.com/w3ctag/design-reviews/issues/954#issuecomment-2475591666)... We didn't know what resolution to use.  Martin says "satisfied" is OK. Jeffrey would said "Satisfied with concerns" seems ok. 

Jeffrey: happy with either. Closing is the most important.

*Matthew to post comment and close.*

Dan: satisfied with concerns might be more appropriate to nudge them

Peter: sounds good

**closed**

### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Matthew: lea had the question... *looks at [answer we got](https://github.com/w3ctag/design-reviews/issues/961#issuecomment-2481735961) to lea's previous question from Alice* - satisfied. Looks like now is the time to post the comment we had drafted.

*consensus to close with Matthew's draft comment*

Peter: we talked about spinning up some kind of task force .. on ID ref. What are next steps?

Matthew: I think it's an important problem

Jeffrey: we need someone to lead the effort - and so far we don't have the time...

Peter: indicates we wait for the result of the election .. or look for someone outside the TAG - neither of which we have to do today.  But we should track this. Maybe open an issue...

Matthew: there's [an issue in the gaps repository](https://github.com/w3ctag/gaps/issues/2).  We can put a comment on there.

Matthew: [posts closing comment](https://github.com/w3ctag/design-reviews/issues/961#issuecomment-2483716803)

**closed**

### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

Matthew: I need to reply with a comment... 

Peter: we were happy to close it last week... had your question on the a11y order... 

Matthew: we were wondering if they were aware of / work with AT vendors...  APA is asking our contacts... Will post later today and then we can close it.

Peter: is there a defined eventing system for a11y tools that aren't js?

Matthew: it's outside of the viewport... There are several different APIs that these tools use to talk to the browser. It's something we're (APA) looking into separately.  From the spec perspective it maybe shouldn't be in the spec - or it might be an editor's note.

Peter: there should be a spec for all of that - standardized behaviour across all browsers.

### [Customizable select element](https://github.com/w3ctag/design-reviews/issues/1007) - @LeaVerou, @matatk

Matthew: some questions after reading the explainer... one that caught my attention - there are interactive elements allowed inside the list box - really want to dive into that in more detail.  [Need to do more work.]

Peter: punt to brekout C?

Matthew: one naming issue... if you want to make a custom style-able select box widget you use base-select - which sounds like the default one to me. Is there a precedent?

Jeffrey: the default is AUTO which feels right. NONE means no appearance. BASE seems reasonable. They are worried that people styling it by accident with * so it's this way so they opt into one element in a time 

Tess: this is a route to get to...

Peter: base to me didn't imply this is the style-able version.

Tess: appearance none should be called appearance cliff...?  The name base is coming from "this is a base you can build on".

Peter: makes sense when you think about it. A lot of people spent a lot of time thinking about this so don't want to jump in. But it seems weird, but there are probably reasons for the weirdness.

Tess: select is unique in that it's really really weird. More weird than other form controls. There are three pieces of it. The normal select is a drop down, a control in the page you activate, and there's the thingie that shows up that you can pick stuff in. This concept of a picker. There are other controls that when you activate it something comes up - the picker. Select is unique in you can style it in a way that instead of having an element on the page that casues the thing to come up, it inlines the thing that would have come up. Eg. for multiple selection, a list box in the page.

Peter: that's done by attribute not by style

Tess: you want to be able to apply styles to the thing that pops up that are the same as the thing embedded in the page. It gets messy. It's great they're tackling select first because it's the most complex one and they have to work through all of that. The subsequent ones will be easier. But initially seems weird.

Peter: layering violation? appilcation of the css here changes the html parser algorithm

jeffrey: I talked to them about that. I thought that was a request from the aria folks, but the answer was they do it by adjusting the display .. they generate all three possible html structures and then the css says display:none on two of them. Which is gross.

Peter: I wonder if.. because when we start styling older controls we have to do something strange for compat reasons, would we be better off by making a new element that is a stylable select

Tess: OpenUI people started with a new element. That wasn't very palatable to a bunch of other constituents. The eventual consensus after a lot of head bashing on that is to try to augment the existing select element as much as possible. A strong reluctance to introduce redundancy in html elements. Generally a mistake in the past. Sometimes understandable, eg. input and button. Bemoans lack of time machine.

Peter: should that be revisted? Don't want to throw a wrench in, but curious..

Tess: they've already gone in these circles. On balance, consesnus was to augment the existing element. There are still people who would prefer the new element approach.

Peter: I've seen this happen in other technologies.. a decision like that, you settle on rough consensus, then you go down that path and you find out more information, maybe then worth revising original decision.

Tess: that's exactly what happened

Peter: I wonder if the parser change was fully considered when they made that decision, and should go back. But also understand the desire not to do that.

Tess: I don't think there is significant new information that would cause them to revisit. 

Jeffrey: they knew they would have to adjust the structure based on the css attribute.

### [Review for Protected Audiences Bidding and Auction Services API](https://github.com/w3ctag/design-reviews/issues/1009) - @jyasskin

Jeffrey: suggest we close as 'decline' or 'timed out' and say if they have a reason for us to re-open then ping us.

Peter: timed out doesn't seem right since it's only 3 weeks old.

Jeffrey: declined is fine with me. I'll draft a comment and we can close at or before plenary.

Peter: should we object?

Jeffrey: we object to the overall structure but this piece ... doesn't make it worse.  I  think there is a possibility that this improves one of the objections to protected audience. But don't think this makes it worse.

Peter: could decline be interpreted as a positive signal to keep building?

Dan: don't we already have a negative review of protected audience? We can point them at that. We can say we've already raised serious concerns about protected audience

Jeffrey: we could say we only think you should extend this if you're fixing problems we identified over there

Dan: we can channel all of that.. in general we don't think you ought to be building on top of stuff that doesn't have broad consensus. If any of these changes are meant to mitigate the issues that we raised then please let us know that.

Peter: I'm happy with that phrasing. We're not really approving unless they've fixed all the fundamental problems.

Jeffrey: I'll draft something

### Chat with Greg Bloom

Jeffrey: we had a chat about the web as a commons... there is a meeting of commons people coming up in Amherst Mass - there might be a good opportunity to run a workshop.



## Breakout B

Present: Hadley, Tess, Peter, Jeffrey, Martin

Regrets:


### [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin

Jeffrey: Martin, I'd like to know more about what you think are the use cases? What do you hate about tbe nascar thing?

Martin: nothing in the soultion allows us to distinguish between that use case and the abuse cases. This seems to enable abuse and doesn't enable the things I think I care about. Nascar: you ahve to log in with one of the 500 different id providers, and you have to find it out of this giant grid. We have a solution for that: FedCM, and the browser knows which of those identities you have.

Then we don't have all the abuse and deception.

Jeffrey: so the idea is represent all the payment and this provider has some info to fill in treat those login cases?

Martin: or similar. Different flow for payments, but yes.

Jeffrey: I can put in suggested comment.

Martin: whether or not this is so bad we object? I would. Not sure if we have consensus there

Jeffrey: I don't think there's a problem with saying this solution is objectionable. I was trying to phrase it effectively.

Martin: there is a piece of the problem that is useful. We should focus on that.

Talking about web payments and fedCM -- examples of where the browser can mediate these things. constructive way to do it.



### [CSS Masonry Layout](https://github.com/w3ctag/design-reviews/issues/1003) - @jyasskin, @LeaVerou

See the rough draft and suggested changes in https://docs.google.com/document/d/1hC4l_9PkhMhvd1J_KRpN8WXlvrOeGq53eLESsyYzC38/edit?tab=t.0.

Martin: I liked these comments

tess: Yes. I fed in my comments.

[discussion of edits into the google doc] 

Was hoping that Lea could've been here to review. But we should not make them delay another week.

Martin: yeah, this is important enough to give a good anount of feedback to

Hadley: are we set?

Jeffrey: let's go through the comments.

Tess: I'm concerned about lumping this in with multicall. multicall is about fragmentation. I'm concerned it will cause confusion.

Jeffrey: yes, and we don't want to say "deal with fragmentation and all the others stuff".

Tess: wrapping flexbox is sufficient to cover the other things. It's a good one, as part of a  non-exhaustive list. Are we trying to be exhaustive? If not, then including multicall causes more trouble than good.

Jeffrey: [makes relevant edits]

Peter: the pdf [?] wasn't necessarily an example, just what we could do back in the 90s

Jeffrey: got it, but it was good to have some example.

Peter: everyone will know where that example came from.

Tess: Could someone explain why the flicker-style grid can't be implemented using masonry?

Jeffrey: it's about hte trailing end for both flexbox and masonry. You stack elements and they end some where

and flicker is not,

Elika thinks we should deal with that with a keyword on the flex property. I largely agree, but this is one of the layouts they should be thinking about.

Martin: how are those layouts achieved?

Jeffrey: they lay them out so it's jagged, and then they scale the whole row so that it's the right width.

Martin. Ah. Wonderful.

[nostalgia for LaTek]

[consensus on the proposed comment]

Jeffrey: I will post to github

### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

Jeffrey: we posted our comments, slightlyoff objected, and we had a good discussion at TPAC

tess: no record of that in the issue though?

Martin: I think we should close unsatisfied

Jeffrey: we can do that.

Tess: can we link to the conversation at TPAC?

Jeffrey: we could, but the most useful conversation was at lunch afterwards

Martin: the minuted discussion focused on one of the minor issues. I wasn't at lunch.

Jeffrey: it was mostly explaining our comment.

Hadley: so what do we do with this issue?

Tess: we close it. 

Jeffrey: yes.

Peter: without comment?

Jeffrey: no, say "when there are answers to the questions we asked above,..."

Peter: sounds good.

### AOB

tess: I won't be able to be there for agenda bashing session at the f2f. the ongoing tag election is none of the incumbents are running

Jeffrey: except for Hadley

Hadley: yes, but I was appointed. Not re-election.

Tess: I know we usually set aside a session for improving how we do our work. Is it more important now to get people's unfettered opinions of how things work? Or is it the other way around?

Martin: I want that unvarnished opinion, and a sanitized artifact that we can share with the incoming people. 

Hadley: we do have a document for new TAG members that could be edited.

Martin: I meant a "this is what works well, this is what doesn't" from the people leaving. 

Tess: what I'm wondering: in any organization when you see attrition rates spike, you have to ask if this smoke suggests there is fire? Unusually high rate should prompt a discussion. 

[Agreed]

Peter: personally I find it too hard to task switch. too many meetings. (But not the conversation for today.)

Hadley: when are the election results in? We could invite them to discuss

Martin: the 10th. So, after our f2f

Peter: we always invite incomning members before they start, and outgoing ones after they finish. To transfer some institutional memory.

Tess: for us outgoing, I feel like we should provide information. I worry about prematurely shooting down ... just because we couldn't make something work doesn't mean they wouldn't.

Peter: definitely. But "this is what happened for us" could be helpful. Stepping down as chair means it's not my problem anymore.

Hadley: well someone will be chair, and they'll want to hear what you have to say.



## Breakout C

Present: Dan, Max, Matthew

Regrets: Amy (belated)

### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954)

Matthew: I closed and documented...

**closed**

### [Cuztomizable Select](https://github.com/w3ctag/design-reviews/issues/1007)

Matthew: Still looking into that...

### [Reading flow](https://github.com/w3ctag/design-reviews/issues/978)

Matthew: Will post comment soon (before plenary)

### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Matthew: if we close, I can leave a comment after on my UI point.

Matthew: when I say there is a lot going on UI wise, Elad was thinking I was talking about the UI of the user agent, not the UI of the app, I think...  I get it... this is interesting to me, because the spec is not specifying how you should do UI either within the UA or within the WebApp - it's up to the WebApp. From an A11Y pov both are covered by WCAG... But if the API is able to do things that are user-visible then that still counts as UI...

Matthew: I need to clarify what I meant by "UI-wise".  If you give me until the plenary - I'll leave a comment and then we can close at the plenary.

*Matthew to leave a comment on UI and A11Y and we can close at the plenary.*

### [Web Authentication's PublicKeyCredential signal methods](https://github.com/w3ctag/design-reviews/issues/996) - @maxpassion

Max: there is an answer from Jeffrey...  But no response from the requestor yet so we should wait.

Dan: OK I will bump.

### [EPUB 3.3 Recommendation with Candidate Corrections  2024-10-17 > 2024-12-19](https://github.com/w3ctag/design-reviews/issues/1006) - @rhiaro, @hadleybeeman

Matthew from an A11Y perspective we are happy with it so no additional input.

## Plenary Session

Present: Dan, Tess, Jeffrey, Peter, Martin, Amy

Guests: Tantek

Regrets: 

### Breakout Rollup

#### Breakout A

* Element capture [closed](https://github.com/w3ctag/design-reviews/issues/954#issuecomment-2485496049).
* Reference target [closed](https://github.com/w3ctag/design-reviews/issues/961#issuecomment-2483716803). We still seem to have concerns about Phase 2, and we have nobody to lead the effort to fix IDs.
* Reading flow ready to close without proposed text.
* [Customizable select](https://github.com/w3ctag/design-reviews/issues/1007) ready to close with proposed text.

*we review a draft comment from Jeffrey and agree to post and close with **satisfied***.

* [PA Bidding & Auction](https://github.com/w3ctag/design-reviews/issues/1009) ready to close with proposed text.

*we review a draft comment from Jeffrey and agree to **close**.*

#### Breakout B

* [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) ready for comment, with proposed text.

*Martin to review the draft reply that Jeffrey wrote*

*we agree that if Martin is happy with Jeffrey's comment then we can close as **objecting**.*

* [Masonry](https://github.com/w3ctag/design-reviews/issues/1003) ready to close with proposed text.

*discussion on whether we can send this feedback and close*

*we agree to post the draft comment and **close***

Peter: what is the resolution.

Jeffrey: "[validated](https://github.com/w3ctag/design-reviews/issues?q=label%3A%22Resolution%3A+validated%22+is%3Aclosed)"

Tess: yes let's do that.

Peter: that works.

* [Cross-origin install](https://github.com/w3ctag/design-reviews/issues/946) ready to close with proposed text.

*we review draft text and agree to close with 'unsatsified'*

#### Breakout C

### [ Vision for W3C: request horizontal architectural review and wide TAG review](https://github.com/w3ctag/design-reviews/issues/1008) - @hober, @jyasskin, @rhiaro

*we go through potential TAG feedback to the proposed W3C Vision with Tantek*

*we make progress on our consolidated feedback and agree with Tantek to file some issues and leave additional feedback soon*

Drafting a comment in https://docs.google.com/document/d/1bqQ1vSO2NP94mF43Pj_MSMD20OJcdHhV5rgz5w3ihXs/edit?tab=t.0

### Issue Triage
