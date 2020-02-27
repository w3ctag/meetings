## TAG Teleconference
##### 24-26 February 2020

---

### Agenda:

### Breakout A (Europe / US) - [2020-02-24](https://www.timeanddate.com/worldclock/converter.html?iso=20200224T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Screen Capture API (2019)](https://github.com/w3ctag/design-reviews/issues/440) - @torgo, @hadleybeeman, @lknik
* [WebXR Augmented Reality Module](https://github.com/w3ctag/design-reviews/issues/462) - @dbaron, @torgo, @hadleybeeman, @atanassov
* [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @dbaron, @torgo
* [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov

### Breakout B (US / APAC) - [2020-02-24](https://www.timeanddate.com/worldclock/converter.html?iso=20200224T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [WebRTC playoutDelayHint](https://github.com/w3ctag/design-reviews/issues/441) - @hober, @ylafon
* [[WebComponents] Custom state pseudo class](https://github.com/w3ctag/design-reviews/issues/428) - @hober, @alice, @kenchris, @plinss
* [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-reviews/issues/446) - @hober, @cynthia

### Breakout C (APAC / Europe) - [2020-02-25](https://www.timeanddate.com/worldclock/converter.html?iso=20200225T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo
* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @alice
* [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

### Plenary Session - [2020-02-26](https://www.timeanddate.com/worldclock/converter.html?iso=20200226T210000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage



-----


### Breakout A

Present: Ken, Tess, Rossen, Dan

Regrets: ?

#### [WebRTC playoutDelayHint](https://github.com/w3ctag/design-reviews/issues/441) - @hober, @ylafon

Bumped to B

#### [WebXR Augmented Reality Module](https://github.com/w3ctag/design-reviews/issues/462) - @dbaron, @torgo, @hadleybeeman, @atanassov

Dan: this includes some additional features to WebXR to bring AR functionality...

Dan: trade-off between functionality and privacy...

Dan: I will review the s&p self check answers this week.

#### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @dbaron, @torgo

Tess: I linked to the mozilla standards position issue which raised some good concerns... security & privacy in particualry. Has not been prototyped... Basic worry I had a month ago - I am concerned we define hit testing for webxr before we define it for the rest of the platform. Adding additional concepts on top of the current model.  I don't want to say " you can't work on this until we do xyz".  but what are the common concepts? If there were to be general work, how could this work inform it so it could be architecturally aligned in the future? 

Dan: security & privacy issues need to be addressed. 

#### [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov

Tess: no thoughts off-hand right now.

Rossen: some movement on this one - enaggement on Moz's position on this topic. 

David: I think Anne has been involved in this.

[discussion on Moz's position]

Ken: [difficut to explain it to developers]

David: I think developers understand what a process boundary is...

Rossen: ...

Ken: some of these. .. difficult to understand...

Dan: concerns about overcomplicating the platform

David: prompted by Spectre mitigation

Ken: we need to come up with better names... make it easier to understand...

David: at some level the explanation is : if you want feature x you need to enable this flag and then you lose features y and z...

Ken: better documentation needed - e.g. on MDN...

Tess: sympathetic to the concern of making things easier for developers...

Ken: dev tools... to help developers...

Dan: can someone leave this feedback on the issue about simplification? I will see if I can raise that feedback in an informed way.

### Breakout B

Present: Peter, Rossen, Alice, Tess, David

Regrets:

#### [WebRTC playoutDelayHint](https://github.com/w3ctag/design-reviews/issues/441)

bumped to face-to-face

*
(lots of unminuted discussion before we realized there was no scribe)

Discussion of whether booleans are sufficient (they are certainly sufficient in theory but that doesn't make a nice API) for pseudo classes.

Discussion of getting feedback from CSS working group.

#### [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-reviews/issues/446)

Tess: This is a request from Tantek.  Quotes "analyze and provide clarity on the exact security model or models and hopefully some degree of consistency and explicit architectural design across these mechanisms."  I think it should go to design-principles document.

Tess: Should I make a PR to design-principles?

Rossen: sounds reasonable.

Tess: The interesting thing last year here was when JSON modules and CSS modules got paused due to security concern Apple raised about unexpected code execution.  Try to import a JSON module that in the past the server served as a JSON file so itwouldn't lead to code execution.  If changed on the server to JS, gets executed as a module.  The fallout of that conversation is that we require some measure of textual opt-in at import time, so the author doing the importing says "I expect this to be JSON" or "I do not expect code execution", so the browser can fail when needed.  That's being pursued in TC39.  Kenneth left link to proposal.  Seems like the general design principle is something that falls out of the rule of least power: when an author wants to do something less powerful we shouldn't surprise them by doing something more powerful. That's roughly what I wanted to capture here.  It's a good thing for APIs to say "I'm expecting this safe thing to happen, I want failure if that invariant doesn't hold".

David: Sounds like a good principle to document... wondering if there are other principles to document out of that request.

Tess: OK, I hope to write a PR when I have time.


### Breakout C

Present: Dan, Ken, Yves, Alice

Regrets:

#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo

Dan: what is the user need?  Feels like it needs to be better documented... Feels very overly complex...

Ken: Document policy enforced?  Required document policy / etc... how do these relate?  Policies split into 3 different groups- this is part of it.  A bit confused between the different types...

[comments in issue]

Ken: How are we gonna make sure these features are consistent... consistency needed...  if presentation lock, shouldn't there be one for orientation lock?  Need consistency...  same names... 

Dan: is that a design principles thing?

Dan: reached out to Andrew Betts for additional comment.

Ken: an overview...  requires acklnwoledgement flag... What is an associated flag?  

Dan: added more comments... let's move on for now.

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @alice

[discussing and analyzing the explainer]

Alice: does Rossen know about this?

Alice: a thing to capture events that may allow you to edit text...

Alice: explainer could have more images...

Ken: typing into an input field and you get feedback while typing like typing "icecream" and getting a prompt for an emoji...

Alice: is it the auhtor telling the page about the editing ...

Ken: both ways.  If it replaces "ice cream" with the emoji it needs to know where ice cream is...

Ken: names / selection...

Ken: seems sensible... the API seems sensible.  [internationalization cases ...]

Dan: I'm concerned about the responses to the security & privacy questionnaire

Ken: I assume this will only work with input methods shipped with the browser, like emoji picker and accessibility helpers. This is an API for the web site author to integrate with these, and not a way for developers to create their own input methods that will then get access to sensible information such as selected text/passwords etc. Maybe this could be made more clear.

Dan: let's review the assignment of this in plenary

* [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

[...discussion of where we're at now...]

[alice composes comments and pastes into issue]

### Plenary Session

Present: Dan, Rossen, David, Tess, Alice, Peter, Yves, Sangwhan, Hadley

Chair: Dan 

Scribe: Rossen

Regrets: Ken

#### Agenda setting etc. during f2f

We will most likely have a room to do it on Monday afternoon. The timing is bad for Dan and Hadley, thus, we might have to do it without them. Another proposal is for Dan and Hadley to get on a VC and decide the issues they will work on so we don't need to consider them.

Remote participation for breakouts - this could be tricky for such sessions that require Dan, Hadley or Sangwhan, so keep that in mind when scheduling breakout topics.

#### Breakout recaps

##### Screen capture 
Bumped to f2f

##### WebXR issues 
Waiting for response by Ada
[some discussion of tag issue process ... ]

##### Origin issues 
Bumped to f2f

##### [[WebComponents] Custom state pseudo class](https://github.com/w3ctag/design-reviews/issues/428)

Rossen: we discussed with CSS wg.  There were some people working on it. More disucssion encouraged. 

... some challenges by Peter to current design ...

... accepted by the group ...

... related to design of the JS API

Peter: Happy that my feedback received. I feel the TAG side of this is in good shape. Maybe mark as "pending external review" - and loop back on it .. Not for the f2f.

##### [Review different cross-domain import mechanisms and their security models](https://github.com/w3ctag/design-reviews/issues/446)

Tess: agreed this was mostly design principles issues. She has the action item to write something about it.

##### Feature policy document policies

Dan: COmment from Ian https://github.com/w3ctag/design-reviews/issues/408#issuecomment-591013926 based on Ken and my questions...

Asked Andrew Betts for comments, who had positive things to say and should comment back to the issue.

##### Edit context

Dan: lots of things to say... Sengwhan should be involved in this. Some concenrns about privacy of the feature.

response from bo : https://github.com/w3ctag/design-reviews/issues/416#issuecomment-591024638

##### MathML

Dan: responded with comments but haven't heard back from Brian yet... will ping him to get a response 

#### New issues triage

##### Delegated ink trail 
Hadley: need better (or any) motivational examples. 
Will looking into it during f2f

##### HR review
Issue from TTML WG. Assigned to Tess.
https://www.w3.org/TR/ttml-imsc1.0.1/

##### Is input pending
WICG issue related to Perf WG. 

##### Personalization semantics
Hadley: This is about a11y related inhancements. Assigned to Alice, Hadley and Rossen

##### Media Feed API
Tess: I self-assigned because I'm interested in media







