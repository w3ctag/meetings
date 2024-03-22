# TAG Meeting Minutes - Week-of 18 March 2024

## Agendas

### Breakout A (Europe / China) - [2024-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20240318T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

### Breakout B (California / Europe)  - [2024-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20240318T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @torgo, @rhiaro, @hadleybeeman, @plinss
* [Side Panel](https://github.com/w3ctag/design-reviews/issues/903) - @matatk, @plinss
* [DeviceOrientation Event Specification](https://github.com/w3ctag/design-reviews/issues/928) - @torgo, @matatk

### Breakout C (California / Australia) - [2024-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20240318T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

### Breakout D (California / Australia) - [2024-03-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240318T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson, @LeaVerou
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

### Breakout E (Europe / China) - [2024-03-20](https://www.timeanddate.com/worldclock/converter.html?iso=20240318T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @torgo, @maxpassion

### Plenary Session - [2024-03-21](https://www.timeanddate.com/worldclock/converter.html?iso=20240321T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk
* [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A 

Present: Dan, Yves, Matthew, Max
Regrets: Amy

#### [DeviceOrientation Event Specification](https://github.com/w3ctag/design-reviews/issues/928) - @torgo, @matatk

Dan: Anssi got back to us... DAS WG believes the spec is compliant with the Permissions guidance, however in response to our concern they opened an issue https://github.com/w3c/deviceorientation/issues/148

Matthew: there's a typo in the permissions spec in /TR ... also I'm wondering if the permissions spec Anssi linked to ... I'm wondering if our advice is compatible?

Matthew: I don't think we can say no to them since this is in agreement with Anssi's approach.. We're saying we don't want to block devices & sensors wg work...

<blockquote>

Hi @anssiko & @reillyeon - First of all, thanks for raising the issue in your repo in response to our feedback. We're happy to close the review on that basis.  
  
...and... It's clear we need some harmonisation between the TAG guidance on devices and powerful features and what the WebAppSec group has developed around this topic. Thanks for bringing that to our attention. We've opened up an issue on our design principles doc https://github.com/w3ctag/design-principles/issues/481 to track.

</blockquote>

Matthew: APA WG [suggested an Accessibility Considerations section](https://github.com/w3c/a11y-request/issues/71#issuecomment-2000387571) (also, it's been great working with this group, as ever).

**closed as satisfied**

#### [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760) - @hober, @torgo, @maxpassion

Max: they have indicated they will modify their proposal. https://github.com/w3ctag/design-reviews/issues/760#issuecomment-1934474449

Dan: *leaves a comment acking their response.* https://github.com/w3ctag/design-reviews/issues/760#issuecomment-2003485944


#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Dan: no response to our feecback from last week.

#### [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @torgo, @maxpassion

Dan: I think we should close on this basis. 

Matthew: yes.

Max: yes.

**closed as satisfied**

#### Attribution Reporting 

Matthew: https://github.com/w3ctag/design-reviews/issues/823#issuecomment-1942431311 .. when we looked at IPA, we discussed the fact that ARA, IPA, Private Attribute Reporting... there's a comment from ... that the merging is happening. So not sure what the timescale is... Not sure of the details here.  We closed the design review for IPA on the grounds that the 3 will be merged... One is still open for ARA ..  If google is still intending to go ahead with their API then it might be worth us reviewing... Do we know whether everyone is involved in this merging... 

*we agree to discuss async*

#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
#### [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

### Breakout B 

Present: Peter, Matthew, Yves
Regrets: Amy

#### [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798) - @LeaVerou, @torgo, @rhiaro

Matthew: They've provided us with several updates, but doesn't look like we have any pointers to [options 2 and 3 from Lea's comment](https://github.com/w3ctag/design-reviews/issues/798#issuecomment-1892583836) having been considered.

Peter: window.open() could be modified to restrict PiP window numbers. Should we ping them to answer that question?

<blockquote>
  
Hi @steimelchrome, thank you for your recent updates. We are still unclear as to whether [options 2 and 3 from Lea's comment](https://github.com/w3ctag/design-reviews/issues/798#issuecomment-1892583836) have been considered - could you point us to the outcome of any discussions on those?
  
</blockquote>

Matthew: *left the comment*

#### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

Peter: I think we were OK closing this on the basis that it's no more harmful - though I have concerns about clarity to the user, when logging into/out of an IDP, exactly what they're logging into/out of. They will get logged into multiple sites, and may not log out of the IDP. This is a big risk. This issue brought it up, but it's a general concern.

Matthew: :-O

Peter: Some providers don't support single sign-out - lots of users don't realise they're not fully logged out.

Matthew: Whom should we go to about fixing this?

Peter: it's a FedCM issue, but also about user intent - on a private machine, users may not want to fully sign out each time, but it needs to be made clear to them what they're doing, and the consequences.

Matthew: Should we file a tracking issue (on us or elsewhere)?

Peter: *checks for an existing similar issue in FedCM repo*

Peter: We were wondering if all of this UI/UX should be handled by the UA instead. This is something that could be solved in that scenario, in a standard way, with the UA as a situational observer. Prior feedback on this was that it's not on the roadmap.

Matthew: That sound good! How can we track it? Is there an issue already filed on that?

Matthew: *takes action to figure out how to track this*

Peter: With respect to this issue, I think we can close it, but would want Amy's buy-in on that.

Peter: *adds propose close*

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

#### [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @torgo, @rhiaro, @hadleybeeman, @plinss

Peter: We pinged Dan ([as previously discussed](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/03-11-minutes.md#tag-review-request-for-the-idp-signin-status-api---rhiaro-hadleybeeman-plinss)); he's OK with us closing this.

<blockquote>

Hi @cbiesinger, we discussed this on our call today; we're happy with the direction the work is going, so we're closing this review. Thanks for flying TAG.

</blockquote>

#### [Side Panel](https://github.com/w3ctag/design-reviews/issues/903) - @matatk, @plins

Matthew: Sounds like they're saying that Side Panel detection is needed becuase the content is philosophically different (per the stated example).

Peter: This still feels like a UA feature (like split tabs). Let's see which other browsers want to do this (if any) before we figure out how to standardize it.

Matthew: ACK.

Yves: Do they link to positions from other browsers?

Peter: No response from WebKit. There is a WICG proposal; doesn't seem to be active.

<blockquote>
  
Thanks @benjycui for your request, and to you and @novac42 for your answers to our questions. It looks like there isn't active community engagement with this proposal at the moment (please point us in the right direction if we've missed anything) - so we are closing this for now. However, if the community picks up on this work in future, please feel free to re-open. 
  
</blockquote>

### Breakout C 

Present: Tess, Peter
Regrets: Lea, Amy

#### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

[Talked about several issues probably explained in the explainer]

Tess: Explainer has gone missing—it 404s.

#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou

[We talked about the general lack of WASM expertise currently on the TAG]

Tess: could be a good example to bring up in this week's AB/TAG joint meeting re: how to fill the appointed TAG seats

#### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

Best to wait for Lea to talk about this one.

#### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

[Discussed the two trigger moments for @starting-style. Peter to ask a question about the display:none case.]

### Breakout D 

Present: Peter, Tess, 
Regrets:

#### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson, @LeaVerou

#### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

#### [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo

Tess to write a comment summarizing the conversation we had with mt about this the other day.

#### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou

[Peter & Tess read some linked issues and spec changes for a while]

#### [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

#### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

#### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou


### Breakout E (Europe / China) - [2024-03-20](https://www.timeanddate.com/worldclock/converter.html?iso=20240318T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Max, Yves
Regrets:

#### Discussion on Appointments



### Plenary Session - [2024-03-21](https://www.timeanddate.com/worldclock/converter.html?iso=20240321T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Matthew, Max, Peter, Yves
Regrets: Tess, Amy

#### Review Breakouts Day [timebox 15 minutes]

Matthew: generative AI one - overall document references TAG document - references ethical principles for web machine learning (which in turn references EWP).  The [AI and the web document](https://www.w3.org/reports/ai-web-impact/) has some interesting points.  Systemic impact.  Comparison with search engines... We've been in this place before with the rise of search engines... Balance between going to the site to get the information vs. not going to the site... At TPAC in Seville there was also a good conversation if ML is an existential threat to a web... many people concerned that responses from LLMs don't have links... Seems search stuff points you to the original site where this doesn't...

Dan: [bing etc..]

Max: I agree ... the link published by Dom - I read it - I started thinking about what's our role in this activity... since we don't have a big impact in generative AI.. As TAG what can we do? Don't have a clear answer. The doc has pointed out interesting perspective. ex how too use web standards technology for example to let users know what part are generated by AI and which part are not. 

Dan: c2pa - reported here https://www.nytimes.com/2024/02/08/business/media/google-ai.html also https://www.bbc.com/rd/blog/2024-03-c2pa-verification-news-journalism-credentials ...

Matthew: last workshop on machine learning was 2020 so probably time for another...

Dan: real world identities ... I am skeptical...

Peter: RealID in some US states - enhance driving licenses -- it's a federal thing...

Dan: i think we need to know what is proposed to be added to the web...

Matthew: Also stuff going on in the EU about IDs... I think understanding it is important...  There was also one about how the web is funded. Interesting use of micropayments proposed in that breakouts. Has big architectural considerations... Brian and Robin ... Robin said a good use of micropayments was from the browser perspective... could lead to "netflix for the web" - subscribe to a whole bunch of web sites and then you don't get ads on them... Seperate ads from sites.. allow the browser to take a slice to fund the engine development.  Concern that the whole web is funded by search deals and all the funding eggs are in one basket..  There's an independent fund for chromium development being set up... https://github.com/w3c/breakouts-day-2024/issues/20



#### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk

Matthew: i've done some work here.. but there's a new review request that came in 2 weeks ago - [play-out statistics](https://github.com/w3ctag/design-reviews/issues/939) - that looks similar ... 

Yves: would say 

#### [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo

#### Breakout Rollup

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

https://github.com/w3ctag/design-reviews/issues/933

https://github.com/w3ctag/design-reviews/issues/934

Matthew: relates to haptics... 

https://github.com/w3ctag/design-reviews/issues/935

