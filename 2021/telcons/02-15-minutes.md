## TAG Teleconference
##### 15-17 February 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-02-15](https://www.timeanddate.com/worldclock/converter.html?iso=20210215T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo, @atanassov
* [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov
* [Pointer Events Azimuth Angle and Altitude Angle](https://github.com/w3ctag/design-reviews/issues/537) - @hober, @hadleybeeman
* [Review for CSS property "aspect-ratio"](https://github.com/w3ctag/design-reviews/issues/559) - @hober, @torgo
* [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou
* [Early design review of CSS Container Queries proposal](https://github.com/w3ctag/design-reviews/issues/592) - @LeaVerou, @kenchris, @plinss
* [Early design review for the FLoC API](https://github.com/w3ctag/design-reviews/issues/601) - @torgo, @rhiaro, @plinss
* [Reporting](https://github.com/w3ctag/design-reviews/issues/585) - @ylafon, @plinss
* [Review request: Partitioning Network State](https://github.com/w3ctag/design-reviews/issues/596) - @hober, @ylafon

#### Breakout B (US / APAC) - [2021-02-16](https://www.timeanddate.com/worldclock/converter.html?iso=20210216T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober
* [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @atanassov
* [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov
* [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov
* [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss

#### Breakout C (APAC / Europe) - [2021-02-16](https://www.timeanddate.com/worldclock/converter.html?iso=20210216T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @torgo, @kenchris
* [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @kenchris, @hadleybeeman
* [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo
* [Support seeking past the end of a file in the File System Access API](https://github.com/w3ctag/design-reviews/issues/600) - @torgo, @kenchris
* [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

#### Plenary Session - [2021-02-17](https://www.timeanddate.com/worldclock/converter.html?iso=20210217T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Lea, Dan, Amy, Tess, Peter, Yves, Rossen, Ken

Regrets: Hadley


#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo, @atanassov

Tess: when we last left it - after we marked it as proposed closed - we noted the non-use of dom matrix. This was due to consistency with WebXR. So I [filed that issue](https://github.com/immersive-web/webxr/issues/1174) - I don't think that should hold this up however.  

[discussion on closing]

Dan: +1

Tess: yes I think we can

Tess: lack of use cases & examples...  was Rossen's comment.

Rossen: yes.  

Tess: I think it would improve the document.

Rossen: we can leave the feedback.  I will write the closing comment.

Yves: I will TAG track the issue in WebXR.

Rossen: [noting previous comment from David](https://github.com/w3ctag/design-reviews/issues/463#issuecomment-635440090)...  Mounir [answered](https://github.com/w3ctag/design-reviews/issues/463#issuecomment-769256508) this doesn't answer the question.  Eric suggests a rename to clarify it's real world only.  But Mounir replies it's up to the implementer.... So let's push it for another week and I will prompt to answer the question and clairify Eric's point.

[so bumped]

#### [WebXR Layers](https://github.com/w3ctag/design-reviews/issues/528) - @torgo, @atanassov
 
Rossen: ... asking Rick to add his explanation / concerns to the actual spec or questionnaire...

Dan: I do see [the change](https://github.com/immersive-web/layers/commit/5639438ddd470ac13cd2428af0189847756e0c5f) but not 

[realized it's a branching issue]

Dan: [updates the links in the issue]

Rossen: OK I'll write the closing comment.

**resolved to close**

#### [Pointer Events Azimuth Angle and Altitude Angle](https://github.com/w3ctag/design-reviews/issues/537) - @hober, @hadleybeeman

Tess: we talked about closin this and I agreed to write a closing comment.  Comment almost done. If we all agree then I'l close.

Tess: to re-cap, this is a develoeper ergonomics win.  The old values required developers to do math and the new values skip that step and are directly useful to apps such as painting apps where you need to know the orientation of the stylus to do certain effects.

**resolved to close**

#### [Review for CSS property "aspect-ratio"](https://github.com/w3ctag/design-reviews/issues/559) - @hober, @torgo

Lea: Tess & I discussed at vf2f. Some issues with the explaienr but in terms of the CSS property we are happy. SO maybe we should close this? 

Tess: more general meta issue with explainers coming from CSS.  Not unique to this issue. Don't think it's worth delaying this issue on that bigger question.

Lea: should I close?

**resolved to close**

#### [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou

Lea: there haven't been any updates since discussion with Alice.  Alice opened a bunch of issues in CSS wg repo which are still open. Most have not received comments. No responses in the TAG issue. 

Lea: **adding labels to issue to indicated pending external feedback**

[bumped 3 weeks]

#### [Early design review of CSS Container Queries proposal](https://github.com/w3ctag/design-reviews/issues/592) - @LeaVerou, @kenchris, @plinss

Lea: Ken & I posted some feedback - and requestor said they would work on it... 

Rossen: CSS accepted it as part of "contain" - new module.  Starting work as part of CSS wg charter.

Peter: are we ready to close this then?

Ken: from TAG pov we have given our feedback and blessing... 

Dan: feels to me like we should close it and ask them to open up a new issue when appropriate.

Lea: I will close.

**resolved to close**

#### [Early design review for the FLoC API](https://github.com/w3ctag/design-reviews/issues/601) - @torgo, @rhiaro, @plinss

Dan: bump it a week?

[bumped]

#### [Reporting](https://github.com/w3ctag/design-reviews/issues/585) - @ylafon, @plinss

[new reply from requestor](https://github.com/w3ctag/design-reviews/issues/585#issuecomment-768563886)

Rossen: some feedback since last time.  

Rossen: exposing info to 3rd party by design... cross-origin 3rd party servers are included by design according to their feedback.  

Peter: it's true you do need to send errors to 3rd parties... you have to be able to identify what sites have the issue... 

Dan: maybe we should drill down on this privacy issue specifically?

[discussion on what to do with this]

Rossen: knowing how much scrutiny goes into reporting APIs in general in the lower parts of the OS... there is a ton of scrutiny and documentation if you want to set up a reporting system. You have to be good at tracing the reports, adhering to log requirements, privacy, compliance... 

Dan: this could be used for tracking through a back-channel by unscrupulous people...

Rossen: has this come through ping or privacy CG?

Tess: not in privacy CG...

[discussion on privacy review]

Rossen: maybe we can dedicate an entire breakout for this?  It's a large spec - we need an agenda.  I want to have 3 or 4 large ticket items we want to dive deep on : privacy is one of them. And then draw a large outcome and path forward from that.

Dan: should we invite the spec authors?

Rossen: yes.

#### [Review request: Partitioning Network State](https://github.com/w3ctag/design-reviews/issues/596) - @hober, @ylafon



### Breakout B

Present: Peter, Tess

Regrets: Rossen

#### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober

Skipped.

Tess: I should schedule a breakout with someone to take another look at this one with me. I'll ask for a volunteer at the plenary.

#### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525) - @hober, @atanassov

Skipped.

#### [CSS overflow: clip and overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579) - @hober, @atanassov

Peter: why wouldn't you also want the overflow-clip-margin to work in `overflow: hidden`? Maybe it doesn't make sense for `scroll` or `auto`, but it does seem useful in `hidden` as well as `clip`.

Peter: The only difference between `hidden` and `clip` is that one causes a scroll container. Two high-level knobs that switch a low-level value which isn't exposed. We should expose the low-level knob "turn this thing into a scoll container". Or "look, just make me a stacking context" or "just make me a containing block."

Peter to write up a comment on this issue.

#### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov

Skipped.

#### [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss

Tess to write up a comment on the issue summarizing our previous discussion on this.

### Breakout C

Present: Lea, Ken, Amy, Dan, Yves, Hadley (for part)

Regrets: Sangwhan


#### [CSS Scrollbars: scrollbar-color, scrollbar-width](https://github.com/w3ctag/design-reviews/issues/563) - @torgo, @kenchris

Lea: filipe [replied](https://github.com/w3ctag/design-reviews/issues/563#issuecomment-774053100) and opened an issue - and replied to some of our issues.  Also one point lack of consensus.  ... Also `scrollbar_gutter` ...

Dan: Can we close?

Ken: concerned about scroll indicators...

Lea: does `scrollbar_gutter` ...

Ken: allows you to reserve the space.  

Lea: it looks like this property should go through TAG review independently.

Dan: What's the status of `scrollbar_gutter` ? 

Ken: Draft.

Lea: as a general comment - it's kind of a shame that the use cases are lost in the process of making it into the spec - you can't find the use cases.

Ken: scroll bars are everywhere on the web - and we want people to make good experiences that look like native.  why not just go the last mile ... why not hear the use cases for not doing your own scrolling solution?  "strong reason why people want their own scrolling solution" - ok let's hear the use cases.

[Ken posts comment]

#### [Web Neural Network API](https://github.com/w3ctag/design-reviews/issues/570) - @cynthia, @torgo, @kenchris, @hadleybeeman

[bumped to plenary - possibly we can close]

#### [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo

Dan: bumped and also I will take a look before the plenary.

#### [Support seeking past the end of a file in the File System Access API](https://github.com/w3ctag/design-reviews/issues/600) - @torgo, @kenchris

[discussion on how this behaves if exploited with very large values]

Ken: [linked to blink dev discussion]

Dan: left a comment and bumped to next week.

#### [Storage Buckets API](https://github.com/w3ctag/design-reviews/issues/562) - @hober, @cynthia, @torgo, @kenchris

Yves: is there an issue with partitioning? 

Ken: we discussed this but don't recall the answer.

Yves: [leaves comment asking this]

#### Meta-point on Process

Lea: it would be good to document some of the process that is in people's heads.

Dan: agreed let's bring that to the plenary.

Lea: document lifecycle of a design review

#### Triage

[608](https://github.com/w3ctag/design-reviews/issues/608)

Ken: no explainer...

Dan: Mounir says it's a small delta.

Ken: 10 new methods... Also someone is asking for use cases of the feature. Seems like there should be a proper explainer.

[609](https://github.com/w3ctag/design-reviews/issues/609)

Ken: why is this new?

Lea: supposed to be privacy preserving...

Ken: this happens today... 

Dan: i think that's browser specific - and they are trying to specify it...

Lea: use cases are not clear... 

Ken: we need to ask for an explainer.. a real explainer?



### Plenary Session

Present: Ken, Dan, Peter, Amy, Rossen, Yves, Lea, Tess, Hadley

Regrets: 

#### Breakout Rollup

##### Breakout A

[we were all in breakout A so we just briefly reprised this]

##### Breakout B

[discussion on whether to reschedule breakout B- consensus not to]

[discussion on whether to reschedule the plenary - we will take it to slack]

Tess: our agenda was long - 

Peter: one issue we discussed previously - that 

Tess: we talked about [overflow-clip-margin](https://github.com/w3ctag/design-reviews/issues/579), peter wrote a comment.

Tess: we need to find volunteers for a review of HTML [focus](https://github.com/w3ctag/design-reviews/issues/468) - we need a 1:1 breakout on this issue.

Peter: a lot of discussion on that in CSS this morning.

Rossen: [volunteers]

##### Breakout C

Ken: left [comment on scrollbar issue](https://github.com/w3ctag/design-reviews/issues/563#issuecomment-779666841).

Rossen: in OpenUI scrollbars always treated at UI control. repurcussions to many parts of the presentational subsystem.  Scrollbar gutters already discussed in CSS wg.  0 width scrollbar gutter - important and interesting from authors' point of view and UA itself.  Lot of reasons to have scroll bars which appear [when needed]. 

Ken: They mentioned there is not consensus around that.  We think it's worth looking int...  If we can avoid people building their own solutions all the time that would be quite nice.

Dan: on [seeking past end of file](https://github.com/w3ctag/design-reviews/issues/600) they replied they took our feedback on board. Can we close it?

Ken: yes. good with me.

**Resolved to close**



#### Issue Triage

#### Additional documentation of TAG process

