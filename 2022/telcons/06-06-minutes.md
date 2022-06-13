# TAG teleconferences week-of-6 June 2022

## Agenda

### Breakout A (Europe / US) - [2022-06-06](https://www.timeanddate.com/worldclock/converter.html?iso=20220606T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov
* [[CSS-Values-4] FYI review of Allow infinity, -infinity and NaN in CSS calc()](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov
* [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @torgo, @plinss, @atanassov
* [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
* [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss
* [CSS property object-view-box review](https://github.com/w3ctag/design-reviews/issues/740) - @LeaVerou, @atanassov


### Breakout B (US / APAC) - [2022-06-07](https://www.timeanddate.com/worldclock/converter.html?iso=20220607T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss
* *things we didn't get to in breakout A*

### Breakout C (APAC / Europe) - [2022-06-07](https://www.timeanddate.com/worldclock/converter.html?iso=20220607T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
* [first party sets](https://github.com/w3ctag/design-reviews/issues/342) - should we close this?
* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov
* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

* [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou
* [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman
* [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou

### Plenary Session - [2022-06-08](https://www.timeanddate.com/worldclock/converter.html?iso=20220608T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2022-06-06](https://www.timeanddate.com/worldclock/converter.html?iso=20220606T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Tess: we should distill the tradeoffs ... however don't know if it would be useful.  We could just say "we didn't come to consensus".   "We're happy to see the complexity of the tradeoffs has been considered."  I'm worried about them taking our output as a red light or green light.  Something generic and short.

Tess: I will take the action to figure out that statement.

Dan: let's plan to review at the plenary and close if possible with that text.

#### [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov

Rossen: closing as unsatisfied.

**closed**

#### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov

Dan: happy to "pass" this.

Rossen: I am too.  

```
Thanks folks - on the basis of this feedback we're happy to close this and we're happy to see this work move forward.  Looking forward to a foldable future.
```

**closed**

#### [[CSS-Values-4] FYI review of Allow infinity, -infinity and NaN in CSS calc()](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov

Lea: in CSS wg we have a resolution that this will be treated as 0.

Rossen: yes. Resolution is in the linked issue.  We should close as satisfied.

**closed**

#### [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov

Dan: does [Mason's comment](https://github.com/w3ctag/design-reviews/issues/694#issuecomment-1082211834) from 29th answer your question?

Lea: i think it makes sense.

Dan: can we close this issue?

Lea: I'd be fine closing.

Rossen: reading his last reply - he acknowledges the proposal started with closed shadow roots.  .. after some discussions added ..  "we added the selection root argument" ... so.. if I'm within a component, and I call the selection.getcomposedrange and pass my root as the selection root argument by default - that guarantees I don't get out of my component.

Lea: I think so.

Rossen: so.. what's the expected behavior if I have a sibling container as the shadow root?  Something iffy here... I think we need to revisit it further..  This is one of those APIs I don't want to mess it up..

*we take 5 minutes to review*

Rossen: I think this will work well... Not caught up on all the issues but the proposed API for the use cases they stated - is a good approach.  The consideration of the `getRangeAt` and changes to `getRangeAt` ... 'The primary selection API use cases SHOULD not be adversely effected"... it's a loose statement.  This is the part where I don't have a strong opinion.... If they're willing to go and try it out it would be great to see how it works in reality. Otherwise from the API shape... it's what I would expect.  A lot of use cases they show is where selection crosses into an open component.. you start selection in the div and the selection ends in the middle of that component... The end is the other shadow root... it's going to work... not sure what that means when you cross many roots..  

Lea: have the roots been passed in?

Rossen: no this is when you call `getComposedRange`.. 

Lea: it cannot return offsets ... that's my understanding...  

Lea: points to [here](https://github.com/mfreed7/shadow-dom-selection#part-1-add-selectiongetcomposedrange-and-selectiondirection)

Rossen: to me that means you're going to start selecting and the selection will run forward...

Lea: the use cases they study don't want to span shadow roots...

Rossen: puts the work to the author... but as long as that's the case that's OK.

Lea: also this new `getComposedRange` becomes a replacement for `getRangeAt`... if you don't pass any shadow roots then it does the same job...  so i wonder if it would make sense to give it a more generic name?  Should it have a more generic name like `getRange`. 

Dan: impact of the authoring of content in the future...

Rossen: to me it feels more constructy...

Dan: Maybe makes sense to leave this feedback in the context of a closing comment.

Rossen: I'm happy to close it.

Lea: *writes closing comment*

**closed**

#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

Lea: we told them to add an explainer..

Dan: good to see this.

Lea: since this basically a boolean - when is it supposed to be true?  When you're on cellular data?

Rossen: it's the UA being in "data saver" mode.

Lea: the example is a signifigantly reduced user experience... 

Rossen: anything that puts the user agent into data saver mode...

Lea: I wonder if 2 scenarios is granular enough...  but maybe the boolean is the easiest way to go... but as a developer I wouldn't know what kind of experience to serve with this boolean. Remove images?

Rossen: all of it... Because it's binary it allows you to as an author reduce anything you want to reduce. You may want to completely restyle... loading no fonts, less images... we've had a back-and-forth about this API - what happens when you go back and forth in the consiumption capabilities... roaming case.. 

Dan: 2g to 5g connectivity just in the course of a half hour trainrride... happens to me all the time in London.

Rossen: the answer is a little vague.. don't want to rush this one... From TAG pov the use case makes sense,.. the way it's being approached makes sense...   We need to consider more the implementation...

Lea: for me the main concern is lack of granularity...

**discuss more at plenary**

#### [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov



#### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @torgo, @plinss, @atanassov
#### [`<search>` HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss
#### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
#### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss
#### [Design review: AbortSignal.any()](https://github.com/w3ctag/design-reviews/issues/737) - @cynthia, @LeaVerou, @plinss
#### [CSS property object-view-box review](https://github.com/w3ctag/design-reviews/issues/740) - @LeaVerou, @atanassov
#### ...some discussion on FPS...

### Breakout B (US / APAC) - [2022-06-07](https://www.timeanddate.com/worldclock/converter.html?iso=20220607T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
#### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
#### [Response.json()](https://github.com/w3ctag/design-reviews/issues/741) - @cynthia, @plinss
#### *things we didn't get to in breakout A*

### Breakout C (APAC / Europe) - [2022-06-07](https://www.timeanddate.com/worldclock/converter.html?iso=20220607T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
#### [first party sets](https://github.com/w3ctag/design-reviews/issues/342) - should we close this?

Dan: dropped from the Privacy CG... 

Dan: my proposal is to close our review.  We issued [a document](https://github.com/w3ctag/design-reviews/blob/main/reviews/first_party_sets_feedback.md) which said we're unsatisfied.  We then had a number of rounds with the proposers. We monitored ths work as it progressed in PrivacyCG. We fed back a number of times.  It doesn't seem like our issues were addressed.  And the fact of it leaving Privacy CG due to lack of consensus is a bad sign for implementation.  So I think we should close and say something like "please re-open after this has incubated"... 

Hadley: more mature or more stakeholders involved?

Dan: I think both...

Hadley: we should spell this out.

Dan: I also feel like we should say : we look forward to additional privacy-related specs that are decoupled from FPS... 

Hadley: i suggest we spell it more clearly... These concerns extend to any spec or feature reliance on first party sets, though we look forward to additional privacy-related specs that are decoupled from FPS.

````
Hi all. We have revisited this again in our W3C TAG meetings this week.

The TAG has agreed to close this review. We began our review buy writing this [statement](https://github.com/w3ctag/design-reviews/blob/main/reviews/first_party_sets_feedback.md), and we have since dedicated extensive time to providing feedback and engaging with the spec authors to improve this design, and do not feel that our suggestions are resulting in evolution of the feature.

We remain concerned about a number of issues, including the privacy implications of this design, and the problems that could be created with any of the proposed governance models for first party sets. Equally, we haven't been able to come up with a governance model that would avoid the same problems. 

These concerns extend to any spec or feature with a dependency on first party sets, though we look forward to seeing additional privacy-related specs that are decoupled from FPS.

We understand that this work is moving to WICG, and will be happy to review future documents that address the necessary use cases after further incubation and demonstrated support from other stakeholders in the W3C community.
````
[nb: text now includes edits from Amy from the plenary.]


Dan: Ok let's discuss and move forward at the **plenary** call.

Hadley: agreed - want to get Tess's feedback.

#### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov
#### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman



#### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

Dan: Isn't there a competing Apple proposal? Where is this work now? https://webkit.org/blog/8943/privacy-preserving-ad-click-attribution-for-the-web/

Dan: is this the same thing? https://privacycg.github.io/private-click-measurement/

Dan: they have listed private click measurement in the reporting API's explainer...

Hadley: should we do a deep dive or encourage them all to converge?

Dan: I feel like there is a standards war happening here... We should be encouraging these different camps to conerge on a solution.

...There seems to be implementer support beyond Apple for Private click measurement. So why is google seeking our review?

Hadley: is it just the Blink process point, sending it to us?

Dan: and they have [negative feedback](https://chromestatus.com/feature/6412002824028160) from Safari

Hadley: given that i don't think it would be helpful for us to dig into the details... Where is a good venue for them all to collaborate? Perhaps the Privacy Preserving Ads CG... 

**determined that this is in WICG**

Dan: so... what can we say?

```
Given that there are other competing specs from other entities that already enjoy implementation (as indicated in your Related Work section of explainers) and that at least one browser has signalled that they do not support this proposal, it seems to us that there is additional work to be done here to converge these proposals and push for a consensus approach.  Is there any effort under way to move in this direction?  Considering the numerous efforts underway by different parties, it feels like this should be headed towards a proper working group. @wseltzer
```

Hadley: also wondering if this should be headed for a working group.

#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
#### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro
#### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
#### [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou

#### [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman

Max: we requested them to provide some code example... he has promised to add a code example in the explainer but it hasn't been done yet.

Dan: Can we close then?

Max: that's one comment... from TAG.  We need another round of review after they provide the example. They have multiple choices - one option is to do the standardization in webidl but webidl people don't like it. - another option is to do it in emaca - that will take too long.  Another alternative, possibly acting as a shim for eventual standardization by ECMA TC39, would be for I18N to define a dictionary and ask specifications to adopt it generally for natural language string values.

Yves: last time we talked about this - the data and meta-data close together so it's not lost...  To me the easiest option for implementers - either in unicode encoding (currently deprecated because of lack of usage - which means all string libraries) - or have ecma work on a specific type that can be a regular string plus indication.  If we don't have that then it means we would always use structures that would be lost at some point.

Hadley: we were going to circle back to them...

Yves: https://github.com/w3c/mediacapture-main/issues/665 and https://github.com/w3c/miniapp-lifecycle/issues/25 are discussions ongoing...

Dan: ecma solution possibly best?

Hadley: found in [previous minutes](https://github.com/w3ctag/meetings/blob/8e1aa24feb0497374cc72b8aaa7dea4e5adb0f71/2022/telcons/05-09-minutes.md): "draft tag view might be - "be guided by developer ergonomics; data and metadata closely bound; should follow from TC39 consensus on what the right approach is and then adjust WebIDl accordingly..."

Dan: so we should post this.

Hadley: *rewrites in full sentences*

Dan: and then?

Hadley: ...ask them if there is anything we can do to help.

Yves: keep it open until we find a place for this...

Dan: we should revisit at the plenary and then push it out a few weeks to revisit again.

Hadley: [posts comment](https://github.com/w3ctag/design-reviews/issues/716#issuecomment-1148353130)

#### [Navigation API (formerly app history API)](https://github.com/w3ctag/design-reviews/issues/717) - @cynthia, @LeaVerou


### Plenary Session - [2022-06-08](https://www.timeanddate.com/worldclock/converter.html?
iso=20220608T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Max, Dan, Hadley, Yves, Rossen

#### Discussion on Closing First Party Sets Review

**we amended the text for the closing comment and agreed we need Tess to review and approve before we close the issue.**

Tess: (from chat) The text looks good to me!

**AMY CLOSES and POSTS COMMENT**

#### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

*...on from Breakout A.*

Rossen: binary or a scale.. My feedback is starting with a binary and then extending is good... All in all it's a decent feature.  I can see how it would be useful. It's being addressed by the right folks. I think we're close to closing.  

Dan: there's no indication of consensus with any other party besides google / chromium, ?? and microsoft. Design sounds fine but is there any indication that anybody else is paying attention? No indication about web developer support, or from Safari. Where is this coming from? I feel like it's a good thing, but that's my anecdotal feeling.

Rossen: Great question.. ask?

Dan: okay

```
Ok thanks @argyleink that's great. We're generally positive on the feature and the design. Can you let us know any information about multi-stakeholder support? Right now Chrome Status shows "no data" for Firefox, Safari and "Web Developer" support (although there is some info provided under user research - thanks for that). Is there any further info in this area?
```

#### [Review request for Fenced Frames](https://github.com/w3ctag/design-reviews/issues/735) - @hober, @torgo, @rhiaro, @atanassov

*punted*

#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

[latest comment from requestor](https://github.com/w3ctag/design-reviews/issues/721#issuecomment-1113605601)

Amy: lea left a review - not sure if the answers are satisfactory - I also did a related review. 

Dan: let's maybe organise a special session on this?  I can reach out to Chris H at Google.

Amy: it's interesting to know why they're not getting interest from other vendors...  But *doesn't* feel like the sort of thing that if only rolled out in Chrome it would break web sites across other browsers.

#### [FedCM (was WebID)](https://github.com/w3ctag/design-reviews/issues/718) - @hober, @rhiaro, @hadleybeeman, @atanassov

#### [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov

Dan: Tab left an update, purely within CSS, looks like it has multi stakeholder support, I saw it's being implemented in Safari. Anything left for us to do that is valuable? Or we say CSS WG has done their work and to please continue? (See https://twitter.com/jensimmons/status/1534255159282368513 for indication of support from Safari.)

```
Hi @andruud thanks for this review and apologies it's taken so long to get you feedback. Thanks aloso to @tab for the further info and explanation. We're happy to see this work move forward and we note positively the multi-stakeholder support.  
```

Dan: **sets to porposed close**

Rossen: will **close**

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Amy: a bit of an impasse...   Idea of blocking access to other APIs to make it inconvenient.. 

Dan: https://github.com/immersive-web/webxr/issues/1269 - if you can remove the need for privacy prompt, you would require it for raw camera access, would be a mitigation, and encourage people to use the non-prompting, more privacy preserving version

Amy: yes that does sound interesting. There needs to be a clear advantage. Not having a permission prompt is a step in the right direction.  Could we ask for a list of APIs that are essential for these use cases and turn everything else off?

Dan: Makes sense but they're not very receiptive to this kind of approach because they think people will just work around it. The reason I like the non prompted version is it gives more convience to the developers who are using the privacy perserving one

Amy: any other positive reinforcement we could give alongside that?

Dan: I'll liase with Ada about this

#### Breakout Rollup
#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
