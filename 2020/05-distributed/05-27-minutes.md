## W3C TAG Virtual F2F
### Day 2 - 27 May 2020

Agenda: https://github.com/w3ctag/meetings/blob/gh-pages/2020/05-distributed/README.md

### Slot C
  * Breakouts 7 **06:30 - 07:30 UTC**
    * Breakout 7a - Dan & Alice
    
    Alice & Dan discussed design principles topics, specifically what the status of the document is (Note vs living doc vs Finding) the Title and Abstract, etc.. We also discussed the cheat sheet. We created [an issue](https://github.com/w3ctag/design-principles/issues/191) for new title and abstract. Alice added material to the [cheat sheet document](https://cryptpad.w3ctag.org/pad/#/2/pad/view/MIJs8efMW1yTEQ3exik+-aKy1qyC5AH67r750mQ9LvI/).  Dan started an [introduction](https://cryptpad.w3ctag.org/pad/#/2/pad/view/G3ERqbq--2j0Amm5vCzkYgiUPNjGVm7ZU7pTolRc4do/).   

    * Breakout 7b - Ken & Sangwhan
      * <a href="https://github.com/w3ctag/design-reviews/issues/334">HTML Modules</a>
      
        Sangwhan: Just checked, not much happened here

        Kenneth: Move milestone?

        Sangwhan: Yes
      
      * <a href="https://github.com/w3ctag/design-reviews/issues/390">Native File System API</a>
      
        Ken: They asked for our feedback on two particular issues, one about different return types depending on opens given to method.
      
        San: I don't think that makes a lot of sense, very confusing for users
      
        Ken: Yes, also then if the user just selects one file, should the method then just return a file and not a sequence of 1 file - I definitely will  go for the latter. If the dev knows there is only ever going to be one file, then you can just do files[0] - and if the code is prepared for multiple files it will work for a single file too.
      
        San: Let me write a comment
      
      * <a href="https://github.com/w3ctag/design-reviews/issues/396">WebRTC-SVC (Scalable Video Coding)</a>
      
        Sangwhan: Looks like the ball is in our court, my bad
        
        Kenneth: Commenting on some stuff.
        
        (...long discussion about idiomatic patterns)
        
        Sangwhan: Will comment.
        
      * <a href="https://github.com/w3ctag/design-reviews/issues/429">HTMLVideoElement.requestVideoFrameCallback()</a>
      
        Generally looks good, and incorporated the feedback from Simon - we don't care strongly about the name. 
      
    * Breakout 7c - Alice & Yves
    
      NB we decided to move these 14b.

      * <a href="https://github.com/w3ctag/design-principles/issues/131">Discourage overloading</a>
      * <a href="https://github.com/w3ctag/design-principles/issues/133">Provide some guidance on creating new list types</a>
      * <a href="https://github.com/w3ctag/design-principles/issues/135">To fulfill or to resolve</a>

      (Yves sent apologies so no 7c)

  * Break **7:30 - 07:45 UTC**
  * Breakouts 8 **07:45 - 08:45 UTC**
    * Breakout 8a - Dan & Ken
      * <a href="https://github.com/w3ctag/design-reviews/issues/358">MediaStream Image Capture API PTZ (Pan/Tilt/Zoom feature)</a>
      
      Dan: I left a note on the issue noting that we intend to close with unsatisfied because they haven't taken the security & privacy issues seriously.
      
      * <a href="https://github.com/w3ctag/design-reviews/issues/481">Window Controls Overlay for Installed Desktop Web Apps</a>
      
      We bumped this as it's pending an editor update.
      
      * <a href="https://github.com/w3ctag/design-reviews/issues/484">PWA Change logs</a>
      
      We [left a comment](https://github.com/w3ctag/design-reviews/issues/484#issuecomment-634506831) reflecting our discussion in a previous TAG call.
      
      * <a href="https://github.com/w3ctag/design-principles/issues/95">Guide spec authors to use one manifest (web app manifest)</a>
      
       Created a [new issue](https://github.com/w3ctag/design-principles/issues/192) to reflect the fact that we need an ack section.
      
       Reviewing [the PR](https://github.com/w3ctag/design-principles/pull/189).
      
       Ken: i think we can drop JSON-LD.
       
       Dan: Agreed.
       
       We resolved some editorial comments from Tess and we still have a few more things to resolve on this PR.
      
    * Breakout 8b - Alice & Sangwhan
      * [Accessibility checklist (First draft)](https://cryptpad.w3ctag.org/code/#/2/code/view/Gr0M1nuleNUuVjn+NyDpLff0yDfOmcgJv0WwukyyjZA/)
      
      Created a repo: https://github.com/w3ctag/accessibility-questionnaire/blob/master/accessibility-questionnaire.md
      
    * Breakout 8c - *unused*
  * Break **08:45 - 09:00 UTC**
  * Readouts/Wrap-up **09:00 - 09:30 UTC**
  
    [discussion on minute taking and cryptpad...]
    
    Dan: 7a wrap-up
    
    Sangwhan: 7b wrap-up: Native filesystem - important piece of feedback on whether it should be polymorphic; webrtc-svc - some feedback; htmlvideo element - happy with current design and closed.
    
    Dan: Moving 7c to 14b
    
    Dan: 8a... talked about MediaStream Image Capture. Left some feedback. They don't seem to have paid attention to the security and privacy questionnaire. Closed as unsatisfied.
    
    ... Window Controls overlay, bumped waiting for editorial changes.
    
    ... PWA changelogs, left a comment. 
    
    ... Manifest issues, spent some time reviewing the open PR. Still some issues remaining, e.g. around JSON-LD. Tess also wrote a comment we're not sure how to address. Need to revisit, chat to Tess about it.
    
    ... Sangwhan will dial in to slot A to discuss.
    
    Alice: [accessibility checklist...](https://github.com/w3ctag/accessibility-questionnaire)
    
    ... if you're designing an API you go through this checklist and if you answer "yes" to any of the questions then it triggers that you need a deeper accessibility review.  
    
    Ken: does it apply to permission prompts?
    
    Sangwhan: no 
    
    Ken: then it should be explicit
    
    Alice: new UI...
    
    [some discussion on this]

### Slot A

### Breakouts 9 **14:30 - 15:30 UTC**
#### Breakout 9a - Dan & Tess & David & Sangwhan

##### [Manifest files PR](https://github.com/w3ctag/design-principles/pull/189) on design principles

(Dan goes through outstanding comments on the PR)

Tess: my outstanding comment is the question of whether these are good examples.  What's the point of the list?  If it's to route people who might add a thing to a manifest to wrote of them, then it needs a little more than names and links.  But second question is whether they're meant to be examples of manifests done well, or just that they exist?

Dan: I think it's the second.

Tess: Then I think I'd want a little more about each one.  Payment method and publication manifest are pretty clear; web app manifest is a kitchen sink.

Sangwhan: I raised similar question in JSON-LD discussion.  I think bigger issue is that we list these things and don't give guidance.

Tess: I think with Web App Manifest, reason it came to this document, people were deciding to create a new manifest rather than use Web App Manifest.  Often doesn't make sense, though makes sense sometimes.  Especially because in Web App Manifest, the name is narrower than its actual domain.

David: Thing this doesn't touch on much is question of whether something should be in a manifest or should be an API.

Tess: e.g., `registerProtocolHandler` equivalent review recently

Tess:
 - should it be in a manifest or an api?
 - which manifest?
 - if there are two parts, is it done in a way that the manifest part and the api part share an underlying model?
 
Dan: I think on David's point... I think it's better *not* to have a manifest and we should say that.  Web features should be self contained and self describing in context.

Tess: Lead with that!  I like the manifest section starting with "maybe you don't need a manifest at all".  (Sometimes people propose solution rather than identifying problems and miss out on other possible solutions.)

(Dan writes text into PR and reads as he types)

Tess: On "Metadata can reside inside a new manifest".  Fetch timing, and complexity/size of data being added.  "You may need to make a new manifest file if the function of the manifest file is different from existing manifest files, if the fetch timing is different, or if the complexity (or is it size?) " ... getting at don't add a new file format for one piece of metadata .  If the set of data you want in the manifest is large, if the domain of the manifest (area it pertains to) is different from existing manifest file, or if the fetch timing of the manifest file is different, those are reasons to create a new one.

(more wordsmithing)

##### <a href="https://github.com/w3ctag/design-reviews/issues/342">First-Party Sets</a>

Tess: We talked about FPS during privacy CG F2F a few weeks ago.  Latest status in that there's a discourse thread started in Jan 2019 proposing to bring FPS to WICG... still blocked from being added to WICG from lack of support from others.  Not promising.  But we had a productive conversation about it in the privacy CG.  Still very skeptical about it.

Tess: As far as design review goes, it's not clear what to do with it.

Dan: Do we need them to get back to us when there's something more concrete.  "Vague but interesting"

Tess: I'd like to see some multi-implementer buy-in.

David: Can we say something about how there are both known issues (raised here and elsewhere) and known benefits to this proposal, we don't want to weigh in heavily as the TAG, but let us know if there's something else different.

(wordsmithing)

Agree to close issue.


##### <a href="https://github.com/w3ctag/design-reviews/issues/391">WebOTP API</a>

Tess: I should mention that I'm coediting (with Sam Goto) a somewhat competing/complementary proposal to this.

Dan: Does that obsolete this?

Tess: no.

Tess: HTML has `autocomplete=one-time-code`.  Other proposal that's not in this issue is the SMS format changes (which I'm coediting with Sam Goto), which has more agreement.  And then there's this proposal which is new JS APIs, which I personally don't think are necessary given that we have `autocomplete=one-time-code`.  SMS format allows site to say "only fill it on my origin".

Dan: This is the same fugu API that we reviewed before.  Does it have multivendor support?  Mozilla position?

David: https://github.com/mozilla/standards-positions/issues/152

Dan: Can we close it?  Interop is important.  One company pushing a design approach... competing design approaches that need to be squarshed together in some way.  Sites would have to browser-sniff... there will be a polyfill.  That's... fine.

Tess: There's a bit that I'm really happy about in terms of interop:  the wire format is the same.  You don't need to know browser in order to format the SMS; that's a big win.

(Dan wordsmiths comment to close)


##### <a href="https://github.com/w3ctag/design-reviews/issues/463">WebXR Hit Test Module</a>

Ran out of time before we got to this.

#### Breakout 9b - Ken & Yves
##### <a href="https://github.com/w3ctag/design-reviews/issues/367">Periodic Background Sync</a>



### Break **15:30 - 15:45 UTC**
### Breakouts 10 **15:45 - 16:45 UTC**

#### Breakout 10a - David & Tess

##### <a href="https://github.com/w3ctag/design-reviews/issues/477">Media Feeds API</a>

David and Tess discussed the status of this review & of the issue we filed during a previous F2F.

David left [this comment](https://github.com/beccahughes/media-feeds/issues/10#issuecomment-634772011) (related to [an open design-principles issue](https://github.com/w3ctag/design-principles/issues/128)) on [the issue filed when the TAG last looked at Media Feeds](https://github.com/beccahughes/media-feeds/issues/10):

> I think whether this is true depends a lot on exactly what is specified.  Browsers all have support for JSON, but I'm not aware of any browsers currently having support for the RDF data model that JSON-LD represents or support for turning JSON-LD into that data model.  So I think the balance here on which is more complexity to add to browsers depends a lot on whether the specification requires JSON processing or JSON-LD processing of this JSON feed file.

David & Tess filed the following issues:

* [Incompatibility with JSON Feeds #29](https://github.com/WICG/media-feeds/issues/29)
* [should this be using rel=feed?](https://github.com/WICG/media-feeds/issues/30)

Tess: let's draft closing text & confirm with Sangwhan during the slot b mini-plenary? Or should we wait since we filed new issues?

##### <a href="https://github.com/w3ctag/design-reviews/issues/432">Timed Text Markup Language (TTML2) 2nd Edition</a>

(We only had a couple of minutes left in our breakout when we got to this.)

David: looking at the changes from the previous edition, it's actually a pretty small list.

##### Design principle issue lucky dip

Ran out of time before we got to this.

#### Breakout 10b - Dan & Yves
##### <a href="https://github.com/w3ctag/design-reviews/issues/483">Scheme-bound Cookies</a>

Dan: this looks good...

Yves: this needs an experiment - if apple and mozilla are fine then I am good...

Dan: we need to check it with David and Tess...

Yves: I think it should be the same for schemeful same site...


Dan: isn't there some IETF implication for schemeful same site?

Yves: revision of the RFC

Dan: I feel like we should check this with Wendy Seltzer.

Yves: already discussed internally with Wendy & Sam Weiler - should be fine.

Dan: OK

Yves: reservations about new header... but no feedback on this point.

On Schemeful same site 

Yves: basically there should be some update to the RFC.... The definition - incrementally better cookies is a draft RFC from Mike... discussing with http working group...



##### <a href="https://github.com/w3ctag/design-principles/issues/68">Best Practices for Registries (including that they should be machine readable)</a>

On Best Practices for Registries -- 

Yves: would it be good to create a task force to address this issue?  Who would be helpful in creating this kind of document? I can ask Ralph Swick & Sam about that. 

Dan: Hasn't the discussion of ever-[insert-color] registries obsoleted this discussion?

Yves: some specs will still need registries...

Dan: ever-[blank] specs can address some of the reasons we were discussing registries

Yves: some specs need machine-readable metadata ...  But these are not really technical issues...

Dan: So there may be something to write in design principles on this topic but we need someone else to design a registry system first...

Yves: yes - by people who have more experience in creating / using registries.

### Break **16:45 - 17:00 UTC**

### Readouts/Wrap-up **17:00 - 17:30 UTC**

Present: Dan, David, Kenneth, Peter, Tess, Rossen, Yves

Scribe: Rossen

#### 10b readout

Dan: (on 10b) **schemebound cookies** and **schemeful same site**. We proposed to close a number of issues. This is because we're happy with it (reads feedback provided). We didn't want to close before checking the temp for multiple implementations as well as hear from David and Tess.

David: People are reasonably happy with scheme bound cookies given this won't break too much stuff.

Tess: ack

Yves: Great, that agrees with our position. So are you OK closing both issues?

David: So my answer was about the first. What's the schemeful same site?

Tess: In WHATWG/W3C land, same site means schemeful same site; there's a separate term for schemelessly same-site. IETF is the opposite (the unmarked case is schemeless there) thus this is adding a notion of schemeful same-siteness to IETF that matches the WHATWG unmarked case.

Dan: So close both?

Everyone: ack


Dan: Next we focused on **best practices for registries**. We put this on the back burner. Doesn't the ever green/blue/teal proposal cover this..? Since we're not experts on registries we shouldn't rush in writing a proposal or best practice of how to use them.

Tess: Makes sense to defer for now. Let's wait for more examples and go from there. The AB is also trying to figure out how that works from process POV. This isn't even part of Process 2020... so it's fine to wait.

Dan: Not going to close but push on back burner. 

#### 9a readout

Tess: Super big breakout between Dan, myself, Sangwhan and David. Started talking about the PR for giving advice about manifests (Dan's PR). We looked at comments and revised some text to the point we were all happy with it. 

Dan: I'd note that Dominic still thinks that referencing image recourse is not a good idea. We should address it before landing. 

Tess: Agreed. We made significant progress but not done.

Tess: Next we talked about first party sets. Decided to close the issue. Having worked over a year there doesn't seem to be buyin from others, thus we felt it's a bit too early for us to weigh in on it. Resolved to close the issue.

Tess: Next was WebOTP API. 

Dan: Tess, said that she's working on a new document, sorry new specification of new format for WebOTP. There is some discussion about this being a JS API or an input autocomplete type? We decided to close the issue. 
There was a lot of discussion about both approaches. We don't feel that TAG should be the deciding factor and prefer to have all parties come together behind one or the other.

Dan: It seems we need a different label we can use for such issues. 

#### 9b readout

Kenneth: We didn't move the issues too much further. There weren't any updates to any of the issues. Added pings and hope to see some activity soon.

#### 10a readout

Tess: Looked at only one issue - Media Feeds API. Ended up filing a number of issues for it and responded to a previous issue from the last f2f. We feel we can/should close it but given all new issues we propose moving few weeks back and discuss again.

Dan: What about TTML?

Tess: With few mins left, the changes between the two versions suggest we can do this at a different breakout. 

Dan: Moving to 15B for myself and Hadley.

### Slot B

* Breakouts 11 **22:30 - 23:30 UTC**
* Breakouts 12 **23:45 - 00:45 UTC**

#### Breakout 11a - David & Sangwhan

##### <a href="https://github.com/w3ctag/design-principles/issues/41">Document when to use allow- attributes vs. extend the sandbox attribute value set for iframes</a>

brief look at, and addition to, the changes David started nearly 2 months ago.

Really needs work off-line rather than thinking we'll get something useful done in an hour.

##### <a href="https://github.com/w3ctag/design-principles/issues/46">should provide advice on when it's good to return the same object again</a>

Closely related to https://github.com/w3ctag/design-principles/issues/70 which we looked at as well.

David: though maybe it's really more related to the live versus static section

David: I think if it's live, you return the same object each time.

David: ... if it's static, you probably return different objects each time.

... but there's also the pattern of returning the same object until it changes, and then a different object.  That's a somewhat weird pattern.

(David adds comment to issue.)

##### <a href="https://github.com/w3ctag/design-principles/issues/55">Need guidance on returning error values vs throwing exceptions</a>

Didn't get to this at all.

##### MiniApps (generally)

Discussion trying to understand whether MiniApps want to be part of the Web.

Sangwhan: We should probably ask if it's intended to be part of the Web or not, and get a reply from the MiniApps group on what they want as a group.  We can review things where they make improvements to the web platform to benefit miniapps but that apply more generally, but our time is probably better spent reviewing things that are more broadly part of the Web.

Action to discuss during mini-plenary - possibly ask chair for a formal position (web or not) from them

#### Breakout 11b - Alice & Rossen
##### <a href="https://github.com/w3ctag/design-reviews/issues/511">Beforematch event</a>

Alice: Let's start with this one since it should be smaller.

Rossen: SGTM

Alice: This is a display locking related. I can imagine this being useful for modern editor apps such as Docs or Word online and their need to handle/provide their own find-in-page behavior.

Rossen: I'm concerned about the "Responses to DOM and style changes in the `beforematch` event handler

... `beforematch` allows re-entry into the event model by causing the target to be removed, hidden etc. Allows an entry point in the middle of the event pipeline. Potentially causes a lot of instability in the event model.

... Appreciate the fact that they call this out, but not seeing any good explanation of how to mitigate these problems.

Alice: What is the use case?

Rossen: User wants to navigate to an element for a particular reason... find in page etc.

Alice: But why do you want an event for this? You can already find display-locked (or whatever it's called now) content, right?

Rossen: Want this element to be out of view... then show it in response to it being found

Alice: My understanding of display locking is that that happens automatically...

... "allows custom styling of the matched element" smells like something which should be a pseudo-class instead, in particular.

Rossen: After reading most threads in the issue and linked issues, I am still worried about the overall instability that such event introduces. In case of the element being removed through DOM ...

Alice: Posted [a comment](https://github.com/w3ctag/design-reviews/issues/511#issuecomment-634988474) asking for clarification on the use case.

Rossen: Verbatim from the [issue](https://github.com/WICG/display-locking/issues/150) "we should continue to fire events when the element is changing, but we should limit this to, like, 10, to prevent infinite loops"

... Added [a comment](https://github.com/w3ctag/design-reviews/issues/511#issuecomment-634992651) asking about re-entrancy and instability.

##### <a href="https://github.com/w3ctag/design-reviews/issues/476">Personalization Semantics Explainer and  Module 1</a>

Rossen: Looking at [new explainer](https://github.com/w3c/personalization-semantics/wiki/Explainer-%28restructured%29) - still a little confused.

Alice: I think they are mostly looking for advice on how to move away from `data-` attributes.

... they're to model a very complex set of user needs, meaning potentially an explosion of new attributes. The explainer lays out that complex problem space.

Rossen: Seems like only 3 attributes?

Alice: That's just the content module - later in the explainer they mention `data-easylang`, `data-simplification`, `data-purpose`, `data-symbol`, `data-numberfree`.

... seems like an analogous problem to CSS, trying to add metadata to enable things to be presented differently in different contexts

Rossen: Yes and no. Extra context is kind of difficult to provide.

Alice: I mean more if you were designing CSS today - extra information about font, color etc. now lives in a separate document and can change according to context. I'm not saying that CSS would be the solution, just that it seems like a similar problem space.

Rossen: But it needs to do more than CSS can do.

Alice: Agreed. You've got to get the relevant info about the content attached to the markup at the right time, but you don't want an explosion of attributes (ARIA etc., which is already listed as alternative). Ideally there isn't a lot of noise added to the document. The data-* is the compromise they arrived at and need an advise on how to move away from such attribute once they are past prototyping.

Rossen: Reading through some of the proposed alternatives, it seems that borrowing ideas from CSS to create such personalization sheets is great. However, we don't want to overload CSS nor do we want to repeat its functionality.

Alice: I think we need to take this offline, but I can leave a comment


#### Breakout 11c - Peter & Tess

##### <a href="https://github.com/w3ctag/design-reviews/issues/413">Screen Enumeration API</a>

Tess: They requested that we file an issue in their repo per point of feedback. We filed at least one issue on them in the past, but we've also been waiting on them to reply to Lukasz's comments, which he left directly on our design review issue.

Peter: Let's @-mention them & let them know about Lukasz's comment

Tess: I don't think I have additional feedback for them.

Peter: Neither do I.

Did so, will propose close when they get back to us.

##### <a href="https://github.com/w3ctag/design-principles/issues/93">Need guidance on DOMString vs USVString</a>

Tess: the rule of thumb I use is "if it's a reflected content attribute that contains a URL, use USVString for the IDL attribute; otherwise, use DOMString."

Peter shared some background with Rust and Servo that Tess failed to minute.

Peter: Servo at one point used USVString internally, so CSSOM grew this union type allowing either string, which just leads to more confusion. 

Peter: unpaired surrogates are a mistake we made, and it would be nice to migrate APIs away from having to deal with them.

Peter: scanning for unpaired surrogates makes things more expensive

Tess: I'll try to distill all of this into a PR.

##### <a href="https://github.com/w3ctag/design-reviews/issues/414">Trust Token API</a>

We marked this `pending external feedback` and @-mentioned the folks who filed this, since there were still open questions from before.

##### <a href="https://github.com/w3ctag/design-reviews/issues/392">Scroll To Text</a>

Proposed closing comment:

> We took another look at this in this week's TAG F2F and we've decided to complete our review.
>
> We're happy that you've tightened up the normative text around word boundaries that we were concerned with, and that you reached out to several other venues to solicit feedback (e.g. uri@w3.org).
>
> We're (still) worried that this is a very significant change to URL syntax and processing that may not have gotten sufficient buy-in from the various relevant standards bodies and other stakeholders. We're also worried that this doesn't have a clear path to standardization. Where do you intend to take this after WICG?
>
> Please file a new design review issue if you end up significantly altering your plans here. Thanks!

#### Break **23:30 - 23:45 UTC**

#### Breakout 12a - Alice & Sangwhan
##### <a href="https://github.com/w3ctag/design-reviews/issues/403">WebXR Device API</a>

Alice: Looks like there's been no response for a while... they fixed the `supportsSession()` issue which I raised. I'm happy to propose closing. If they want more review they can let us know and then we won't close it.

Sangwhan: Sounds good to me.

##### <a href="https://github.com/w3ctag/design-reviews/issues/507">Virtual Keyboard API - boundaries of docked overlay keyboard</a>

...reading background and explainer, discussing why this is not declarative

Alice: I'm not sure why this can't be declarative, like the notch CSS

Sangwhan: For example, there is the maps example in their explainer, which repositions the search box based on the geometry change event

Alice: But that can be made declarative

Sangwhan: Now that I think about it, yes possibly

Alice: Seems like Kenneth proposed the event, should probably check with him.

Sangwhan: The notch itself might not work - probably has to be a new CSS thing

Alice: Posted [a comment](https://github.com/w3ctag/design-reviews/issues/507) to ask about insets.

Sangwhan: Posted [a comment](https://github.com/w3ctag/design-reviews/issues/507#issuecomment-635016277) noting that this seems like an instance of a more generic problem. 

##### <a href="https://github.com/w3ctag/design-principles/issues/70">Improve guidance for using attributes vs methods</a>

Alice: I had a brief look at this.

Sangwhan: David and I looked at this... this is a moderately deep rabbit hole.

Alice: Oh ok, let's move on then

##### <a href="https://github.com/w3ctag/design-principles/issues/73">Optional arguments</a>

Sangwhan: This looks tractable. Looks like it could go in between "dictionary parameters" and "classes should have constructors".


#### Breakout 12b - David & Rossen

##### <a href="https://github.com/w3ctag/design-reviews/issues/485">Layout Instability Shifted Element Surfacing</a>

Rossen: Steve answered the questions we raised last month.

David: proposed comment to close:

> @atanassov and I just took a look at this again in a breakout at our virtual face-to-face.  I think we're happy closing this; what we've seen seems reasonable.  We encourage you to continue to get feedback from the appropriate working groups (I suspect Web Performance is probably the right venue but that it's useful to get a bit of feedback from CSS), and to get data on whether this is a useful approach for the performance that affects users and for what developers want to measure.

##### <a href="https://github.com/w3ctag/design-reviews/issues/488">CSS Color: lab(), lch()</a>

David's comment on reasons the issue was open was at https://github.com/w3ctag/design-reviews/issues/488#issuecomment-620098626

We looked at https://github.com/w3c/css-houdini-drafts/issues/989 which was about the fourth point.  Discussed a little bit; David suggested that we may as well wait for Lea and Chris to propose what they want to propose.

David: I'd like to dig in to the Color on the Web CG issues a little bit more.

David adds https://github.com/w3ctag/design-reviews/issues/488#issuecomment-635010629

David: I'd like to at least see Chris's answer to that before closing this -- it's something I might want to help with depending on the answer.

##### <a href="https://github.com/w3ctag/design-principles/issues/104">Prefixing particularly dangerous operations with "unsafe"</a>

David: The two issues Anne linked to both cite CSP as a precedent -- maybe worth looking at CSP.

Rossen: in .NET our guidance about safe/unsafe was mostly about referential integrity.  Most pitfalls were about weak pointers in C++ being used as in or out parameters, or structs that use weak pointers.

David: The Web doesn't expose anything that's like C++ raw pointer semantics... not even (I'm pretty sure) WASM.

David goes through existing uses/suggestions of "unsafe" and summarizes them in
https://github.com/w3ctag/design-principles/issues/104#issuecomment-635016104

David: I think the common thread is that they're all weakening the guarantees that the specification itself provides.

Rossen: What can we do to move the issue forward?

David: Add some text in section 2.1 of design-principles, about naming considerations.

Perhaps something like a new bold subheading under 2.1:

> ###### Warning about dangerous features
>
> Some specifications exist to provide guarantees or invariants to developers who use them.  For example, [CSP](https://w3c.github.io/webappsec-csp/) provides protection against certain types of content injection vulnerabilities. Such specifications may also provide features that weaken their own invariants (or those of other specifications), such as CSP's `unsafe-inline` keyword, which allows inline scripts, reducing CSP's own protections.  It is useful to mark features that weaken the invariants provided to developers by making their names start with "unsafe" so that this is more noticeable.

#### Break **00:45 - 01:00 UTC**

#### Readouts/Wrap-up **01:00 - 01:30 UTC**

Sangwhan: Started out with mini-apps. 

... Last point of feedback on the URI scheme, which we criticised, is that mini-apps are "Web URL accessible" application-ish things, but they're not supposed to work in browsers. Begs the question of whether this is within scope for us. We don't have a formal position on how we draw that boundary. If something isn't going to be part of the Web Platform, should we take on that work?

David: There have been cases in the past where the Team have tried to persuade things which don't integrate well, to integrate with the web stack, and this has ended up with a compromise that makes everyone unhappy. Something which wasn't really designed for the web tends not to fit well, and the compromises to make it fit make it a poor experience for what it was originally designed for.

Rossen: Can we draw that line in the sand?

David: We should raise this with Yves and Dan.

Peter: This seems like a full plenary issue. Raises questions about our charter. Web architecture vs. everything coming out of W3C.

... added to next week's milestone.

Sangwhan: We discussed some design principles issues but didn't make significant progress.

... Has been some good discussion, some of which we minuted.

Alice: Did you comment on any of these issues?

David: I think I commented on the one about the restriction models... or I started working on a PR... 

Sangwhan: We commented on one issue and updated the branch on another.

##### Breakout 11b

Alice: started looking at the beforematch issue. Couldn't really get a good idea of what the use case that this individual proposal solves. Added comment asking for clarification on the use case and why content-visibility.

Rossen: Re-entrancy concerns... could imagine removing/re-adding DOM nodes in response to this event which could trigger another iteration of the event. This is an ongoing discussion in an issue. There was a proposal to limit the number of events that could fire in sequence. That only underlines the concern.

Alice: Next we looked at personalization. Had trouble understanding what that was all about at first. After filing an issue they came back to us with a new explainer much closer to what we expect. 
The new explainer outlines a number of use cases that can be addressed by something CSS-like allowing additional data to be provided and displayed to the user. 
Added a comment asking for clarification if this is all the help they need from us. 

##### Breakout 11c

Tess: Screen enumeration API. This had ended up in the abyss. Was stuck at pending editor feedback.. Lukasz had asked a number of questions, but we think they hadn't seen it because they had asked us to file issues in their github.

... Beyond that we felt like they had heard the rest of the feedback, we'd like to propose closing.

... We'll come back in a few weeks and see if we got a response.


... We then talked about DOMString vs USVString. This is a long-standing issue, I took an action to write some advice for the design principles.

... Trust Token API... still open questions, so we did a similar thing to the screen enumeration issue. @-mentioned folks, marked pending external feedback.

... Then we took a "bonus" issue, Scroll To Text.

... Drafted a closing comment which is in the minutes.

##### Breakout 12a

Alice: The supportsSession case that we saw as a design bug has been addressed - we're thinking about closing it. Still concerned about the group not addressing the accessibility issues here. Aside from that nothing else is outstanding from our point of view. Thoughts?

... Virtual keyboard - they added two things, first is an opt-in flag and an event that fires when the keyboard shows up, with the boundaries of the overlay. This seems like a strange design decision so I commented on that on why it is not CSS-based. Sangwhan commented on why this is assumed to be bottom anchored and also non-generic.

... We did not look at the attributes vs methods issue as David and Sangwhan discussed this and it was deemed a longer discussion than what we could do in the remaining breakout time.

... We did look at optional arguments, Sangwhan made a [PR](https://github.com/w3ctag/design-principles/pull/194).

##### Breakout 12b

Rossen: Made some good progress, closed one issue, raised a PR.

... Layout Instability Shifted Element Surfacing, proposed closing with a comment.

... Feature and specification seems fine, questions were answered. We did recommend that they continue to involve the appropriate WGs and get their input.

David: We did close it.

... LAB, LCH - thought about closing it, but there was one outstanding question for Chris (Lilley) - auditing other points on the web platform to handle the wider color space. Chris has a CG that is doing work on this... seems like the end goal should be filing issues on HTML and CSS, are they planning to do that and if so, sooner or later?

... Last issue was prefixing dangerous operations with "unsafe", where we tried to figure out what makes things unsafe. We made a PR on the naming section.





