# TAG Minutes Week of 6 Jan 2025

## Agendas

### Breakout A (California / Europe)  - [2025-01-06](https://www.timeanddate.com/worldclock/converter.html?iso=20250106T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Design Principles PR on HTTP guidance](https://github.com/w3ctag/design-principles/pull/546)
* [Ethical Princioples PRs](https://github.com/w3ctag/ethical-web-principles/pulls)
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Breakout B (California / Australia) - [2025-01-07](https://www.timeanddate.com/worldclock/converter.html?iso=20250107T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [CSS advanced attr() function](https://github.com/w3ctag/design-reviews/issues/513) - @hober, @plinss
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss
* [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss

### Breakout C (Europe / China) - [2025-01-08](https://www.timeanddate.com/worldclock/converter.html?iso=20250108T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion
* [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

### Plenary Session - [2025-01-09](https://www.timeanddate.com/worldclock/converter.html?iso=20250109T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)



## Minutes

### Breakout A (California / Europe)  - [2025-01-06](https://www.timeanddate.com/worldclock/converter.html?iso=20250106T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Matthew, Jeffrey, Yves, Amy, Hadley, Tess (second half)

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

Jeffrey: we postponed it in Edinburgh...  My thought : there are not very many use cases in the explainer and we haven't liked the use cases that are there... So there's nothing left to review.

Hadley: that gets to the comment from july - the use cases are in some ways also abuse cases

Tess: it would be interesting if they could come up with use cases... But I don't know of any

~~~
Our core issue with the current specification is that the use cases it's supporting can also be "abuse" cases (as we put it above)...  Can you provide some additional use cases that make it clearer why this technology is needed? Can you also provide some suggested mitigations against the potential for abuse that we highlighted above?
~~~

Matthew: it's not just that we don't "like" the use case - but (as per previous discussion), we were concerned about why it's effective. We don't know if the user is more likely to make the transaction because they think they've transacted with this party before.

Jeffrey: we talked about that in 975.

#### [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou

#### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

Peter: users don't understand the concept of partitioned identity...

Jeffrey: the whole UI experiment is to explain to users that this is happening in the context of another site but give the same security guarantees... Can we do for a pop-up like thing what we already can do for iframe.

Jeffrey: we think it aligns with users' expectations...

Matthew: a debate .. between low level primitives you can build on top of .. vs. specific high-level focused APIs... I think we'd agree that if you're gonna do a low level API you need to make sure it's secure & private. The current impasse we have is: TAG has said a focused API in this case would be better - but Google say the lower level stuff is good and is more private than what currently exists. However the only use case they've given is the login one - which is legit - but are there additional use cases where you need short-lived pop-ups? So could we have more use cases?

Peter: I agree.



#### [Design Principles PR on HTTP guidance](https://github.com/w3ctag/design-principles/pull/546)

#### [Ethical Principles PRs](https://github.com/w3ctag/ethical-web-principles/pulls)

Dan: **Merging** https://github.com/w3ctag/ethical-web-principles/pull/139

##### https://github.com/w3ctag/ethical-web-principles/pull/142 - 

Dan: Agree to change authors to editors. We try to use specific clear language. "Any member of the w3c community" is very vague. It doesn't mean other people can't also use it if we use specific language. Puts a clearer image in peoples mind.

Jeffrey: sounds reasonable. Wanted to take that suggestion to a new PR anyway.

Dan: will resolve, and move Sarven's suggestions to another PR.

Hadley: "developers" also inconsistent. We usually use that to mean "people developing a website".

Jeffrey: qualified by spec developer here, not as confusing as authors was

Dan: spec developers includes people who are working on a spec but aren't necessarily the editor. Contributing in other ways, code examples, etc. Vs the more formal role of edinburgh.

Hadley: "contributor" is more often used for that?

**we agree to merge**

**we agree to punt 143 to chat with Sarven**

Dan: https://github.com/w3ctag/ethical-web-principles/issues/145 - *explains*

*we converge on the idea to change debate to discussion as Chris Wilson suggests*

Dan: to create a PR.

##### [clarify which websites will be well internationalized](https://github.com/w3ctag/ethical-web-principles/pull/146) trying to keep this editorial

Dan: are there other places we're using the word 'we' that we should change to the w3c? There's constructive ambiguity

Hadley: I think it was deliberate. It's a statement about what the w3c community would do. Would be concerned about taking it out.

Dan: is this getting in the way of translation?

*discussion about how to clarify connotation of 'we'*

Hadley: will continue discussion in issue

Matthew: 'we' is used all the way through the document

##### [Individual Digital Sovreignty](https://github.com/w3ctag/ethical-web-principles/issues/137)

Sarven is involved in this long thread, let's wait til Sarven is here

##### [2.12 People should be able to choose how they engage with the web #140](https://github.com/w3ctag/ethical-web-principles/issues/140)

Dan: right, web is two way

Jeffrey: sounds like authors should be able to constrain authors in certain ways?

Hadley: not how I read it

Dan: me neither

Jeffrey: rest all seems to agree with what's there, don't know what to change

Matthew: ask for clarification and an example of one thing that might be changed

##### [debate](https://github.com/w3ctag/ethical-web-principles/issues/145)

Dan: "debate" has become a bit toxic. There are some suggestions.

Amy: both suggestions good

Hadley: "discussion" captures what we were originally intending for this

Matthew: discussion seems clearest

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)



### Breakout B (California / Australia) - [2025-01-07](https://www.timeanddate.com/worldclock/converter.html?iso=20250107T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Jeffrey, Peter, Marcos (briefly)

Regrets: Tess

Quick discussion of the duplicated Findings list. Resulted in https://github.com/w3ctag/tag.w3.org/issues/59.


#### [CSS advanced attr() function](https://github.com/w3ctag/design-reviews/issues/513) - @hober, @plinss

Jeffrey: In their I2S (https://groups.google.com/a/chromium.org/g/blink-dev/c/2dNLhQN9SNs/m/VP2BPdE5AQAJ), they say #5079 is resolved by a change in CSS Values and Units Module Level 5.

Peter: The overall feature is good. Devil is in the details, and we should trust the CSSWG to get that right.

Jeffrey: So we should close this as satisfied?

Peter: Let's ping Tess, and then yes.

[Tess was pinged and said ok; Jeffrey closed the issue.]

#### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou

#### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

#### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss

#### [Dispatching Toggle Events for Dialog open/close](https://github.com/w3ctag/design-reviews/issues/1005) - @martinthomson, @jyasskin, @plinss

https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/11-04-minutes.md#dispatching-toggle-events-for-dialog-openclose---martinthomson-jyasskin-plinss: Peter was going to draft a comment.

OpenUI asked the same question in 2022 in https://github.com/openui/open-ui/issues/607#issuecomment-1309330785. They decided on toggle. Our biggest concern is consistency across the platform. So we should be filing issues to make `toggle` happen everywhere. If it turns out not to fit everywhere, that would be a sign that we need to go back and try to make `open` and `close` happen everywhere.


<blockquote>
We understand that there was a long discussion that resulted in a single 'toggle' event rather than 'open'/'close' events, 
and don't want to unnecessarily reopen that discussion. However, the platform is currently inconsistent between CSS psuedo-classes, properties, attributes, methods, and events. 
We feel having platform consistency outweighs slight improvements over DX in specific cases here.
If the path forward is a single 'toggle' event, then the CSS pseudo-classes, properties, attributes and methods should be made consistent with that pattern. For example, the pseudo-class values should match the ToggleEvent's `newState` values, which we believe they do. For properties, attributes, and methods, to what extent are they consistent with the 'toggle' pattern?
If the toggle pattern doesn't fit well with the other uses, then it may be time to rethink 'toggle' vs 'open'/'close'.
</blockquote>

### Breakout C (Europe / China) - [2025-01-08](https://www.timeanddate.com/worldclock/converter.html?iso=20250108T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tristan, Max, Matthew, Hadley


#### F2F Planning

Dan: Dates we are looking at are 3-5 of March.

Tristan: waiting for final approval for 3-5 March in Paris.  Space for 10 - we can book that.  Other than that, we have 2 cafe spaces open for us but not won't be alone.  All open spaces and can sit where we want... Benches / spaces used for hot desking... Will book one meeting room and we will use other stuff around if we need to.

Dan: Sounds good...

Dan: food... we've had catered lunches in the past... 

Tristan: place is surrounded by dozens of restaurants... takes 5 to 10 mins and we meet up in cafeteria.  

Dan: time & dietary requirements...

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: noting what I've already noted. Mid-nov, they'd asked us to close it on the basis that we'd left some feedback but it was incomplete. Now they've asked us to re-review. Needs Martin. 

#### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

Dan: no updates - let's bring it up at plenary and see what the outcomes were from any TPAC discussion? 

#### [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk

Matthew: we discussed last year and Jeffrey made a comment - the concern we had was that we don't need as much as info as they say they do to do the things they want to do... Jeffrey's proposed comment puts that across... As a separate issue it shouldn't be possible to do this by polling and that's a bug.

*we ask Jeffrey to leave his comment*

Dan: let's discuss at the plenary.

#### Partitioned popins

Matthew: I'll do another pass today.

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

*We talk about HR request https://github.com/w3ctag/design-reviews/issues/1029 - hadley leaves a comment asking for more info on changes.*


### Plenary Session - [2025-01-09](https://www.timeanddate.com/worldclock/converter.html?iso=20250109T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Tristan, Dan, Jeffrey, Matthew, Yves, Amy

#### Next F2F Plans

Confirmed: *Paris, 3-5 March*

*discussing the idea of doing a developer meet-up. 

Tristan: Octo may be able to host it. We need to find the people to invite them. We could find a local meet-up that could help with this.

Matthew: We can recycle the presentations we did in Edinburgh.

*Tristan to reach out on social media.*

#### Breakout Rollup

*partitioned popins*

Peter: on *toggle* I'm concerned about consistency.  we posted we're not going to argue but we want things to be consistent. 

Jeffrey: Keith [left a detailed reply](https://github.com/w3ctag/design-reviews/issues/1005#issuecomment-2577396759)

Peter: also we have 2 lists of findings... https://github.com/w3ctag/tag.w3.org/issues/59

Dan: we should have the authoritative version on w3.org

Peter: agreed. since w3.org has URL persistence policy...

Peter: let's get them in sync and then change the link on tag.w3.org ...


##### Clipboard access ongoing issue

Dan: *clipboard thingy ... how do we engage*

Jeffrey: in the remote desktop community .. they are worried that if you are rendering the remote desktop, the remote desktop might have a "paste" menu ... there is no way for the desktop app to know that the pixels say "paste". They are also worried about the gesture requirement.

Dan: Kind of think that it's OK that the remote desktop doesn't have access to the local clipboard ...

Matthew: want to agree with the concern.... The article just referenced is about writing the clipboard. There's also reading from the clipboard. I think reading is worse. On the reading side there is reference that you can poll for what's on the clipboard. That seems like a gaping hole that needs to be plugged. Maybe a compromise would be an API that says if something is on the clipboard or not.

Amy: It's not just about the remote desktop it's about any other application ... wider threat model than just this specific one.

Peter: Just echoing ... I'm a remote desktop user .. used to be a standard that there is a feature in the desktop client to paste .. always a special UI that .. more modern desktop clients do this action of a shared clipboard..  So if we can't figure out a way to do it securely, then we can live with that.

Jeffrey: at least 2 mitigations that could make this safer. One that's already done is that there's a permission. Another one is a "toast" that says "this thing pasted" - some OS's do this. The third is that the browser could popup UI that says "the site would like to read your clipboard - here's what's on your clipboard" - the API could made safe. I suspect that Firefox and Safari won't shop it unless it's safe. Some options there.

Peter: if a remote desktop client has to have a user opt in, then that's a really good opportunity to flag permission... 

Peter: 

Jeffrey: a bunch of activity on the clipboard API's repository... Either picking one of those or filing a new issue with a couple ways forward...  We could say "do this instead"... 

*Potential comment that we can iterate on*:

<blockquote>
Hi folks - I'm raising an issue here to draw attention to an issue that the TAG thinks is worth considering, regarding the privacy characteristics of the clipboard API surface. Specifically: the TAG still thinks there are privacy and security issues with web sites being able to access data in the clipboard. This is not abstract - we are talking about real user harms in terms of theft of private information and access to credentials. It's not just about the single remote desktop application - it's about all the ways other web site can gain access to this sensitive data. A single permission prompt doesn't do the trick because these can be easily gamed. Something more robust is required, considering the sensitive nature of data that is often stored on the user's clipboard and the security & privacy considerations of the web platform. We have raised this issue before, both in the context of [our own reviews](https://github.com/w3ctag/design-reviews/issues/636#issuecomment-857829725) and in [issue #52](https://github.com/w3c/clipboard-apis/issues/52#issuecomment-875709431) here. 
  
We would like the group to mitigate this issue via one of these avenues:
  
1. Have a normative requirement that the browser notifies the user each time a site pastes, along with an API design that encourages seamless remote desktop apps to only show that indicator when the user actually intended to paste. This could be similar to [existing OS designs](https://www.howtogeek.com/692572/why-are-iphone-apps-pasting-from-other-apps/) that show a toast each time an app pastes.
2. Have a normative requirement that the browser provide some dialog to the user that "the remote app is trying to paste this data from your clipboard, OK/Cancel" - possibly with an indication of what is on the clipboard so that they can make an informed decision.
3. Have the remote desktop apps provide a remote dedicated paste button.
4. If none of the above mitigations are acceptable, then we would seriously like to suggest not to ship this feature.
  
Thanks for your consideration.
</blockquote>

*proposed approach : dan posts the issue. we will iterate on slack and post soon.*

##### Partitioned Popins

Matthew: I revised the comment I have in line with Jeffrey's suggestions... 

*some discussion on this*

##### 

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

