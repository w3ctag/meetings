# TAG Teleconference
#### 04-06 April 2022

---

### Breakout A (Europe / US) - [2022-04-04](https://www.timeanddate.com/worldclock/converter.html?iso=20220404T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov
* [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov
* [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo
* [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov
* [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov
* [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov
* [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov
* [[CSS-Values-4] FYI review of Allow infinity, -infinity and NaN in CSS calc()](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov

### Breakout B (US / APAC) - [2022-04-05](https://www.timeanddate.com/worldclock/converter.html?iso=20220405T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion
* [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov
* [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou
* [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss
* [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov
* [&lt;search> HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss

### Breakout C (APAC / Europe) - [2022-04-05](https://www.timeanddate.com/worldclock/converter.html?iso=20220405T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
* [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion
* [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @torgo, @maxpassion, @hadleybeeman
* [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @cynthia, @rhiaro, @hadleybeeman
* [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon

### Plenary Session - [2022-04-07](https://www.timeanddate.com/worldclock/converter.html?iso=20220407T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* Issue Triage
* Revisit meeting times

-----


## Breakout A

Present: Dan, Peter, Amy, Yves, Rossen, Hadley, Tess

Regrets:


### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

Amy: doesn't seem like much has changed wrt fundamentals, only API shape

*discussed and left a comment asking if there has been any further info on implementations*

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Rossen: what is the disagreement?  Last think I see is 6 months ago...

Rossen: my proposal is to express the disagreement in the issue ... PR seems to be landed

Peter: but still open..

Rossen: I see webkit's opposition to the feature. 

Peter: two ends are allowing authors to hide controls is bad, removes platform specific controls, and is user hostile. The other half is that if we don't give them a way of filtering specific controls they turn off all controls and building their own.

Rossen: do we know if Tess or Lea are going to be around for breakout B? Let's push to B, and in the meantime try to follow the breadcrumbs and see where the discussion is.

### [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov

Amy: we looked at this in the f2f.. left feedback, proposed close, no response so far

*we agree to **close** with reservations*

### [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov

Peter: my real concern is that it's not detectable... I think this needs to be detectable. 

Dan: that's the guidance in the [design guidelines](https://www.w3.org/TR/design-principles/#feature-detect).

Peter: yes... 

Rossen: there was one suggestion from Francois but didn't go anywhere...

Rossen: The only thing remaining before we can close this is detectability. Everyone agrees the feature is needed and good.

Peter: Domenic's last comment "wait and gather more data"... implement now and wait and see and get data? would like to see a plan for how that data is gathered and loop back. Or we have consensus that it really needs to be detectable to cover all use cases, then just do it, and we can say that.

Rossen: this is only for pickers that are browser native? or any picker? some browsers invoke a platform native picker... font picker, etc... is intent for showpicker to work with those cases as well?

*discussion on types of pickers*

Tess: missed that distinction but now I get it.. UI provided by browser which may be OS or browser UI, vs picker supplied by a custom component.

Rossen: already talking about component vs browser

Peter: that's what I've been talking about. I want date input, if browser has a decent one I'll use it, if not I want to fall back to mine, which may have issues but is better than them typing text

Tess: you want to know is the one you have crap so I can use my own

Peter: or do you even have one. Whether it's OS or browser, in theory should be detectable. Is there another factor?

Rossen: if showpicker .. if the only way to detect it right now is to call showpicker and look at promise result you're potentially going to invoke something unexpected .. it's very clunky. 

Peter: totally fine with a hasPicker method. Also okay with showpicker throwing new methods.. not going to complain if a picker shows up

Rossen: maybe I like the colour picker in firefox native browser UI but I prefer to see the native fontpicker from Windows.. if they tell me they have their own font picker I want to show my library font picker because I don't have a way to invoke the OS native picker which I like.. it's three choices I'm trying to make.. I can detect between the first two (browser or OS native UI) and the third. But you're not allowing me to make the further distinction down the path. Which I'm pretty sure is important for some platforms and some browsers

Peter: similar case historically.. on one OS the date picker is really nice and on the same browser but a different OS the browser has one but it's shit. The only way to detect that is UA string... browser is going to just say yeah I've got a date picker. No feedback of if it's a good one or not. Not sure it's fair to ask for how good is your picker.

Rossen: detectibility further fine grained is needed..

Peter: has picker gives back an enum, native, OS, none.. Leave that feedback?

Rossen: [leaves feedback]

Peter: do we have consensus that we really want detectability?

Rossen: I don't see the reason why this is not needed. If you don't care about detectability just call showPicker and deal with what is there

Peter: Dominic's feedback is he thinks if showpicker throws an exception that will break code. Makes the argument we should implement it and get data. My argument is if you implement it without throwing an exception you're going to have a whole lot of code out there that will never expect an exception and we can never change it

Tess: self-fulfilling prophecy...

Peter: we can always make it not throw later without breaking any code

Rossen: on top of it you're not allowing... nicer ... [behaviour]

Peter: if we have consensus that it should throw if you don't have one we should leave that feedback

Rossen: yep [leaves comment]

### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @plinss, @atanassov

Peter: pending feedback for something minor

Dan: bump it?

### [Dark mode support for web apps](https://github.com/w3ctag/design-reviews/issues/696) - @hober, @cynthia, @LeaVerou, @torgo

Dan: comment responding to Tess's point

Peter: not sure I buy that comment. It's just JSON.. if you have multiple matching key in JSON the last one wins in a JSON parser?

Tess: yes

Peter: so if they say first one wins they write a custom JSON parser? What?

Tess: seems like completely missed the point. They even said they wanted it to be consistent with that other thing, and Peter's proposal is consistent and their proposal isn't... Someone should point out that's not how JSON works.

### [`prefers-reduced-data` CSS Media Query](https://github.com/w3ctag/design-reviews/issues/705) - @LeaVerou, @torgo, @atanassov

### [[css-values-4] The Large, Small, and Dynamic Viewport Sizes](https://github.com/w3ctag/design-reviews/issues/706) - @torgo, @atanassov

### [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468) - @hober, @atanassov

### [Modification of selection APIs to account for shadow dom](https://github.com/w3ctag/design-reviews/issues/694) - @LeaVerou, @atanassov

### [[CSS-Values-4] FYI review of Allow infinity, -infinity and NaN in CSS calc()](https://github.com/w3ctag/design-reviews/issues/708) - @LeaVerou, @atanassov


## Breakout B

Present: Peter, 

Regrets: Max

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

*bumped from A so we can get Lea and Tess*

### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov

### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia, @maxpassion

### [InteractionID in Event Timing](https://github.com/w3ctag/design-reviews/issues/670) - @plinss, @atanassov

### [renderPriority element attribute](https://github.com/w3ctag/design-reviews/issues/676) - @cynthia, @LeaVerou

### [Review Request for adding video- prefixed media features](https://github.com/w3ctag/design-reviews/issues/697) - @cynthia, @LeaVerou

### [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711) - @hober, @cynthia, @plinss

### [Review Request for CSS Subgrid](https://github.com/w3ctag/design-reviews/issues/712) - @plinss, @atanassov

### [&lt;search> HTML element](https://github.com/w3ctag/design-reviews/issues/714) - @LeaVerou, @plinss


## Breakout C

Present: Dan, Yves, Hadley, Sangwhan, Amy

Regrets:


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

Yves: ... would be good if the mini app people would look at ...

Sangwhan: how do you 'check the origin of the miniapp'?

Dan: a good indicator.. 

Sangwhan: [leaves comment]

Yves: about the webapp launch handler. In the discussion we talked about miniapp lifecycle and that they should look at it.. point them in that direction

Amy: did Max say he was going to talk to them about that?

Dan: we need to come up with what role the TAG can and should play in bringing together the miniapp community and the web app and pwa people. Appears to be something the TAG should do, but need to think about how

Sangwhan: I think the people who are working on page lifecycle are still around in chrome, I can ask

Dan: feels like there needs to be a mini workshop that focuses on lifecycle where we bring together pwa enthusiasts, webapp people and the miniapp folks. Let's bump until Max is back.

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro

Dan: recent comment from someone in the community. To my knowledge they're still working on this. This topic came up in the mini workshop we ran yesterday with the ethical ML work stream because the abuse cases we were talking about in webxr raw camera access issue are relevant to the use of ml on the web because one of the abuse cases was piping a raw camera image to some ml module doing facial recognition. How the user might not expect that.

Sangwhan: if it's running locally it's better than being sent over the wire..

### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

Dan: on 22nd feb said they'll get back in the next few weeks, haven't heard. Ping again?

Sangwhan: I don't think this has been worked on recently

### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @cynthia, @torgo, @maxpassion

Dan: comments recently.. 

Sangwhan: will re-ask my question..

Dan: they didn't respond about multistakeholder

### [Web App Launch Handler](https://github.com/w3ctag/design-reviews/issues/683) - @torgo, @maxpassion, @hadleybeeman

Dan: [response from alan](https://github.com/w3ctag/design-reviews/issues/683#issuecomment-1080253545) looks good - maybe we should close?

Hadley: explainer seems quite a bit clearer. We asked for changes twice. I feel like Max and Lea also had feedback on it. Largely looks like they have addresssed everything we put out there. And looks like Alan was saying we suggested they look at how it relates to miniapp lifecycle, filed an issue hoping they'd look at that together .. comment saying its worth considering look at how they fit together

Dan: I think it's related to what we were talking about earlier.. 

Hadley: open question of how involved we want to be.

Dan: out of scope for this particular issue.

Hadley: close with an explicit comment about the groups working together

Sangwhan: tagging Angel seems like a good way forward

Dan: [drafts comment](https://github.com/w3ctag/design-reviews/issues/683#issuecomment-1088481698)

Dan: if we close this issue, can we take the conversation to our miniapp lifecycle issue?

Sangwhan: I think so

### [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @cynthia, @rhiaro, @hadleybeeman

Hadley: we looked in Feb.. of the issues we opened looks like they've addressed.. extesnive changes on S&P

Amy: they responded to the 3rd issue but only half.  I read the S&P sections and felt they were good.

Sangwhan: they have an OCF defines layout of package. Defines format. Zip container.  Why are they stuck in zip?   Terrible for network.

Hadlety: existing implementations.

Yves: existing implementations.

Sangwhan: could there be a 2ndary container codec?  That's why we're still stuck with GIF.  We can ask. [writes comment](https://github.com/w3ctag/design-reviews/issues/684#issuecomment-1088488821).

Amy: there's probably a decade of history.

*we look through their issues*

Amy: looks like they've responded well on Privacy & Security.

Hadley: we should write our list [suggestions] down [in our issue] - also could be helpful [to them] at re-chartering time.

Amy: i'd like to check up on that issue where they'd answer half of it - before I nicely ask for a response.  Then if we think everything else is OK we can write a closing comment.

Dan: *let's discuss and hopefully close at the plenary*

### [Markup based Client Hints delegation for third-party content](https://github.com/w3ctag/design-reviews/issues/702) - @torgo, @ylafon

Dan: interesting that Ari is talking about 'sent from the first party server'. What's that about? Rather than same origin. But they are being responsive to Yves' comment.

Yves: response from Dominic saying it should be properly specified. They opened an issue in their repo. If that works then I'm fine with it.

Dan: suggest closing comment

Yves: wait for plenary? 

*we will hopefully close at plenary*

## Plenary Session

Present: Amy, Peter, Max, Yves

Regrets: Rossen, Dan, Sangwhan

### [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @cynthia, @rhiaro, @hadleybeeman

```
Thanks for the great work on the Privacy and Security sections. The threat models and mitigations now look very comprehensive, and we appreciate the effort that went into these.

I had [one question remaining around permission prompts](https://github.com/w3c/epub-specs/issues/1958), but this is not blocking.

Having completed our review, we are happy to see this move forward. Thanks!
```

### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

Yves: [markup based client hints](https://github.com/w3ctag/design-reviews/issues/702) .. okay to close.. open issue under discussion on their repo

Peter: okay with me

### Issue Triage

### Revisit meeting times

Plenary - move [this time] an hour earlier. Okay for Yves, Max and Amy, and better for Peter.
