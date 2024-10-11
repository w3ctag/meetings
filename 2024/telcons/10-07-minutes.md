# TAG Minutes Doc - week of 7 October 2024

## Call Agenda

### Breakout B (California / Europe)  - [2024-10-07](https://www.timeanddate.com/worldclock/converter.html?iso=20241007T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
* [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss
* [FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974) - @rhiaro, @plinss
* [FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @torgo, @hadleybeeman, @plinss
* [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

### Breakout D (California / Australia) - [2024-10-08](https://www.timeanddate.com/worldclock/converter.html?iso=20241008T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @plinss
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion
* [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin
* [Early design review: Future browsing context group dependency hint](https://github.com/w3ctag/design-reviews/issues/979) - @hober, @martinthomson
* [Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @hober, @martinthomson

### Breakout E (Europe / China) - [2024-10-09](https://www.timeanddate.com/worldclock/converter.html?iso=20241009T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion
* [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk
* [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman
* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman
* [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk
* [Vibration API](https://github.com/w3ctag/design-reviews/issues/971) - @martinthomson, @torgo, @matatk
* [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk

### Plenary Session - [2024-10-09](https://www.timeanddate.com/worldclock/converter.html?iso=20241009T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

2024-10-07-week

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Call Minutes

### Breakout B (California / Europe)  - [2024-10-07](https://www.timeanddate.com/worldclock/converter.html?iso=20241007T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present:

Regrets: Amy, Lea, Hadley, Jeffrey

#### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
#### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
#### [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
#### [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss
#### [FedCM's IdP Registration API](https://github.com/w3ctag/design-reviews/issues/974) - @rhiaro, @plinss
#### [FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @torgo, @hadleybeeman, @plinss
#### [CSS reading-flow property](https://github.com/w3ctag/design-reviews/issues/978) - @hober, @nitot, @matatk

Matthew: i'm researching - we discussed at TPAC - a fundamental question is : we did talk about this in CSS but the minutes haven't appeared yet. 

Yves: [finds minutes](https://www.w3.org/2024/09/23-css-minutes.html) and [minutes](https://www.w3.org/2024/09/24-css-minutes.html)

Matthew: will look more into it and see if question I had was answered... A question I had around the whole conversation of reading order. Talking about focus navigation and not how the DOM order is exposed - virtual cursor navigation. That follows the DOM order. There's been discussion on whether that needs to change as well.

... tables or things that look like tables... 

... the current stuff, good progress is being made...

### Breakout D (California / Australia) - [2024-10-08](https://www.timeanddate.com/worldclock/converter.html?iso=20241008T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: 

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @plinss

Peter will talk with Noam or do a writeup to clarify the disconnect about use of selectors.

#### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

Waiting on proponents.

#### [Captured Surface Control](https://github.com/w3ctag/design-reviews/issues/962) - @martinthomson, @maxpassion

Waiting on proponents.

#### [Fenced frames with local unpartitioned data access](https://github.com/w3ctag/design-reviews/issues/975) - @martinthomson, @jyasskin

\[mt] This is a terrible idea.

#### [Early design review: Future browsing context group dependency hint](https://github.com/w3ctag/design-reviews/issues/979) - @hober, @martinthomson

Why is this the right change to ask websites to make?

Why is it that we ask sites to make this change in order to have things work as they expected.
That is, if a site sets target=foo, why would that window end up in a new BCG?
Why is rel=opener the right way to address this, rather than target=foo?

<blockquote>
Hi @kjmcnee, we were discussing this and we're not following the reasoning.

Why do you see rel=opener as the right approach, rather than by keying on target=anything?
That a new window with target= will not be discoverable is surprising.
That navigations will end up in a different process is similarly surprising.
Obviously rel=noopener breaks that link and enables moving to a new process,
but an explicit rel=opener as an explicit request to stay in the same BCG seems like it has some awkward consequences.

Concretely, what do we stand to lose if we insist that new windows stay in the same group?
Are there performance numbers that motivate having a process switch?
Maybe WebKit's behavior is evidence that the costs are acceptable.
That might trade-off back-forward performance for straight-up loading performance,
but I'm curious about what the real cost would be.
</blockquote>

#### [Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @hober, @martinthomson

Discussed and with the upcoming work on AI, it seems premature to say anything right now.  We might add a note about that to the issue.

### Breakout E (Europe / China) - [2024-10-09](https://www.timeanddate.com/worldclock/converter.html?iso=20241009T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Martin, Yves, Tristan, Matthew, Amy

Regrets: Lea, Hadley, Jeffrey

#### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

Dan: anything at TPAC

*generally no*

Matthew: there was a breakout with a similar title... local https...

Martin: no details yet on that... 

Yves: anything on local TLS in ietf?

Martin: there is mutual TLS .. but that was a little controversial.

#### [Element Capture](https://github.com/w3ctag/design-reviews/issues/954) - @LeaVerou, @matatk

Matthew: we had a load of questions and it turned out that most of the questions were addressed in the article. We asked them to put it in the explainer. A couple of the q's we had were not answered... we [asked them](https://github.com/w3ctag/design-reviews/issues/954#issuecomment-2344584220). No feedback. I think most of our concerns were addressed. It feels a little weird - but they are doing compositing properly - removing transparency... but it would be good to have this alternatives considered section... ball's in their court.

*we ping the issue to get feedback*

#### [Early Design Review: Partitioned Popins](https://github.com/w3ctag/design-reviews/issues/956) - @LeaVerou, @matatk, @hadleybeeman

*no updates*

#### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman

*no update let's discuss it at plenary*

#### [Reference Target](https://github.com/w3ctag/design-reviews/issues/961) - @LeaVerou, @matatk

Matthew: still catching up with discussion from TPAC

#### [Vibration API](https://github.com/w3ctag/design-reviews/issues/971) - @martinthomson, @torgo, @matatk

\[mt] Initial thoughts after reviewing the specification...
There are a few problems that seem fairly evident to me:

1. The specification relies on [sticky activation](https://html.spec.whatwg.org/multipage/interaction.html#sticky-activation),
   which is true if the user has ever interacted with a page.
   That makes this less about interactive feedback (as you might get with a gamepad) and more like a notification.
   That is more the case when you consider that there is nothing preventing a background window/tab from engaging the API.
   If the intent of the API is to act like a notification, then the notification API is more appropriate.
   Requiring transient activation would seem to be more in line with expectations and be less likely to annoy.
   If the goal is to enable notifications, 
   which seems to be one of the main use cases,
   then adding vibration capabilities to the notifications API might be better.
   
2. The privacy/security considerations don't consider annoyance as a major factor.
   This was part of why this was disabled.
   That might be partly mitigated by a transient activation requirement,
   which puts vibration much closer to playing audio.
   That seems like a good fit to me.
   Browsers have a bunch of ways of managing annoyance from unwanted noises.
   Reusing those techniques for vibration might make it less objectionable overall.

3. If activating vibration is observable cross-origin,
   perhaps the right thing to do is
   suppress things like accelerometer events for the duration of a shake.

4. I seem to recall that gamepads have different vibration strengths and frequencies.
   Why is this not a consideration here?

Martin: the primary privacy concern is annoyance. It's not too dissimilar from sound being annoying.  If we were able to have a similar sort of approach to playing of sounds then that would be fine. Sounds relies with activation. I don't think that's appropriate for vibration.

Dan: what's the current spec say about permission requests?

Martin: current spec says nothing.  It says the UA should inform the user when it's being used.  I think that's garbage.

Dan: I kind of agree. Vibrations are interruptive.

Martin: notifications - have a notifications API.  If you want to provide haptic feedback like in a form, then activation is appropriate. I would turn the feature off, but... 

Yves: I think it's restricted to when screen is on.

Martin: ah... it's only available for foreground... 

Dan: it should only be the active tab...

Martin: yes - it's only if it's in the foreground and visible.

Dan: then "activation" seems sufficient.

Martin: transient or sticky...  Sticky is if you interact with the web site it stays ... you've interacted.  Transient is .. you've touched the screen or hit a key and it's active for some short period of time.

*discussion of transient vs. sticky*

Martin: currently specified as sticky...

Dan: let's ask them to justify that...

Matthew: do UAs that support this offer an option to disable it?

Martin: no idea.. only implementation is chrome...   Spec says "SHOULD" provide a mechanism to disable...

Matthew: every OS has a volume control on it... but maybe not similar controls for a vibration... 

Martin: privacy principle on abusive behaviour... or notifications and interruptions

Martin: if you vibrate a device and another webpage has access to the accelerometer it can send coded messages. Require that the browser turns off the accelerometer while activiting vibration. I believe it's a physical requirement anyway.

Martin: satisfied with concerns?

Matthew: how strongly do we feel about sticky and turning it off?

Martin: it's a MUST. But does it make the whole api a bad idea?

Matthew: if our concerns were addressed we'd be satisfied. Then I agree.

Max: use case with two browsers active at the same time - and both use the api - what happens since the hardware only has one device? Does the API consider this situation? What's the user experience?

Martin: if you have two visible tabs on the device, if one requests vibration and the other one requests, it should just vibrate as much as both of them combined, the union of the two. I don't think that's necessarily problematic. If the patterns interact it'll just be solid vibration..

<blockquote>
We're concerned about the abuse of this API to divert attention in inappropriate situations.  We note that you're specifying sticky activation.  Are there use cases that support this - rather than transient activation?
  
For the difference in activation types, we think that sticky activation might not be a good justification for the notification-style use case.  If someone isn't engaging with the site, having it vibrate could be annoying.  If the goal is to generate a notification, the notification API seems like a much better fit for that.  At least with notifications, people are in control of how they are notified (sound, visual, vibration, or combinations).
  
There is a good analogy between this and audio, in that both might be engaged in a similar way and disabled with similar controls. However, have you considered adding a stronger normative requirement that UAs should be able to turn it off? It's not as easy to turn off a vibration with physical controls as it is with sound.
  
Security/privacy considerations don't treat annoyance as a problem.  [Interruptions](https://w3ctag.github.io/privacy-principles/#interruptions) is a privacy issue you should consider addressing.  We like that the vibrations only activate when the page is visible, but that seems like something that should be directly addressed as a mitigation for that issue.
  
Security considerations should require that accelerometers and gyroscopes are disabled for other origins when vibrating.
</blockquote>

#### [Accessibility conformance Testing (ACT) Rules Format 1.1](https://github.com/w3ctag/design-reviews/issues/977) - @rhiaro, @matatk

Matthew: APA is looking into this, haven't finished yet. No concerns so far.

### Plenary Session - [2024-10-09](https://www.timeanddate.com/worldclock/converter.html?iso=20241009T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Martin, Amy, Matthew, Tess,

Regrets: Lea, Hadley, Jeffrey

2024-10-07-week

#### Breakout Rollup

##### Breakout B

* [CSS Reading Flow Property](https://github.com/w3ctag/design-reviews/issues/978)

Matthew: still working ...

##### Breakout D

*browsing context groups... and AI*

*jeffrey offered to help triage on view transition classes...*

##### Brekout E

*we discuss vibration and how "sticky" the activation should be*

##### Controller Documents
*we defer*

##### Next week's call schedule

*dan to put it into the W3C calendar - will be "early morning thursday uk time" plenary call time*

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

##### [css values](https://github.com/w3ctag/design-reviews/issues/993)

Dan: can we give this one a pass?

Peter: I'm of the opinion we can give it a pass.

Dan: let's give it an "decline"

Martin: agree.

*general agreement*

Dan: *closed*

#### [animation progress](https://github.com/w3ctag/design-reviews/issues/994)

*discussion on why this isn't in "explainers by google"*

Dan: *assigns jeffrey & lea*

#### [document isolation policy](https://github.com/w3ctag/design-reviews/issues/995)

#### [canvas place element](https://github.com/w3ctag/design-reviews/issues/997)
