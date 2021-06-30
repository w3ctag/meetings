# TAG Teleconference
#### 28-30 June 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-06-28](https://www.timeanddate.com/worldclock/converter.html?iso=20210628T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Device Posture API [formerly Screen Fold API]](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov
* [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @hadleybeeman, @atanassov
* [Capture Handle](https://github.com/w3ctag/design-reviews/issues/645) - @rhiaro

### Breakout B (US / APAC) - [2021-06-29](https://www.timeanddate.com/worldclock/converter.html?iso=20210629T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober
* [MediaStream Image Capture (wide review)](https://github.com/w3ctag/design-reviews/issues/651) - @plinss, @atanassov
* [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov

### Breakout C (APAC / Europe) - [2021-06-29](https://www.timeanddate.com/worldclock/converter.html?iso=20210629T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon
* [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524) - @cynthia, @torgo
* [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo
* [Resource Timing](https://github.com/w3ctag/design-reviews/issues/641) - @cynthia, @kenchris
* [User Timing ](https://github.com/w3ctag/design-reviews/issues/642) - @cynthia, @kenchris
* [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman

### Plenary Session - [2021-06-30](https://www.timeanddate.com/worldclock/converter.html?iso=20210630T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [research in specs](https://github.com/w3ctag/process/issues/26) issue from Terence Eden
* Breakout Rollup
* High level vs low level design principle PR
* Issue Triage

-----


## Breakout A

Present: Peter, Kenneth, Amy, Rossen, Yves, Lea

Regrets: Dan


### [Device Posture API [formerly Screen Fold API]](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov

Peter: Dan asked if anyone else had anything on this

Ken: some is implemented in chrome by samsung, something something windows implementation. Has been interest from google..

Peter: last comment from alexis is that they significantly reshaped the api, do we have anything to add to that?

Rossen: trying to piece together..

Ken: used to be more like fold angle, used to be a way when the fold was changing to do animations, that's removed/postponed due to privacy. Other devices came up that didnt' necessarily depend on an angle so posture had to be made more generic, now called device posture not fold angle. Now it's basically exposed the name for the posture, and a way to query it. It's a big change

Peter: is that documented?

Rossen: explainer is now different... min and max angle, spanning. Is this spanning something harmonising with the spanning apis in css?

Ken: definitely harmonise but I don't think spanning is supposed to be part of this... using spanning from CSS yeah..

Rossen: High level feedback to explainer is that I'd like to see actual use cases here and examples instead of declaring the media. How people would use it would be interesting. Question about postures - one of the statements made by alexis is that the new proposed api doesn't have any type of problems if there's more than one fold. I wanted to know more about that. What does that mean? 

Ken: that is becuase it doesn't talk about actual folds any longer it talks about postures

Rossen: if I have two folds and I fold the first one at 90deg what do I get at min angle?

Ken: it's not the angle any more. Exposing a posture which is a name.. that would just be flat posture

Rossen: Not what I'm seeing in the explainer

Ken: someone redid the explainer, it might be out of date

Rossen: go down to proposal: new css media query min angle and max angle... and an example. Then screen media posture, screen fold posture

Ken: is this sthe right explainer?

Rossen: maybe i'm looking at something else

Ken: explainer didn't get updated, I'll fix that. Also checking privacy review... I will tell alexis to fix this.

Rossen: okay so basically only the posture but not a whole bunch you can do outside of that? how do you target the rest of the functionality? with the spanning api or what?

Ken: the animation thing is maybe.. initial interest from samsung, when we tried to go over what they're doing in native apps no-one could find me examples. Everything else is with spanning

Rossen: so the span apis will give you the ability to know where the fold is, layouts and all of this stuff, but you still don't have the angle

Ken: you do't have the angle

Rossen: does that matter?

Ken: use case from angle is if you have a childrens popup book, things turn around when you open it, seems to be minor use cases.. and if it has to be exposed we have to make sure it works across if you have multiple folds and where. May have to be a javascript api. Then you get into privacy issues if you can query the angle all the time. With all of that together we decided not to pursue that at the moment. Unless people come up with real useful use cases for it. Also discussions around if you have multiple displays, how the displays are positioned toward each other.. some changes have happened with the multiple display spec.. the window segments is being integrated with that. We decided with this to do the bare minimum until everything falls into place, then maybe that will have to be combined with something like that

Rossen: I'd love to see examples that are real examples

Ken: someone did this new explainer and it's very short

Rossen: other point is the first motivation example on the very top has two folds, and none of the device postures is talking about this so it's very confusing for someone looking at the first time. Either change that, or..

Peter: how do you describe something that has two folds? add more postures?

Ken: yeah, additional or more descriptive postures, if it makes sense ot design for those

Rossen: this is a really great start, a great example of describing your feature and capabilities at the highest possible level and not exposing any additional lower level apis like angles or where things are, how they came about, velocity of closing/opening. If you really look at all of the possibilities for this set of functionality there are tons of them. on the native api we have in windows at least a ton of capabilities that are available that are a lot lower level extensibility of these models. Starting with this and going after feedback and more studies and more signals from both devices and end users of the api is the best path forward. I'm good with where this is going and how it's starting. Adding additional angles or whatever comes about later on is fine. I don't have any specific feedback on the postures themselves, they seem pretty straightforward although the only thing I'm questioning is how is flat different than no fold?

Ken: no fold here is supposed to be if you have a device that doesn't have any fold. Maybe that would be flat. But sometimes you want to differentiate.

Rossen: you can always add stuff. Removing stuff is harder. no fold vs flat I'm not sure which is better. Prefer single word values, so flat is better

Ken: questioning curved display... is that then flat?

Rossen: Crescent or watermelon...

Lea: mobius strip

Ken: It'd be great if you can give the comments on explainer, and file an issue with no-fold vs flat

Rossen: will add in issue

Peter: is this giving enough information to be useful? how would i actually change my webpage?

Rossen: if you go from a flat to a tent what you do know is that you now from a user pov have the intent to have only half of the screen visible.

Ken: useful for games

Rossen: you can split your webpage in two and flip them so one is facing one way and one the other way. This is where design should come and lead in terms of use cases. I wouldn't lead from the api to inform design decisions. Should be the other way around.

Ken: alexis did a battleship game like that with the tent mode. If it's flat you can see the opponant. Definitely games where tent mode makes sense

Peter: I'd like to see this driven by what uses it's enabling, how, and is it giving enoguh information to do that. If tent presumes split horizontally down the middle every time that may not be reality on all devices. I'd like to see actual use cases and how this enables those uses cases. I don't see it. Lacking context.

Rossen: yeah. Different types of fold and what use case they're motivating and codifying those in additional examples that are real examples is useful. I prefer this now because it is high enough level that allows quite a bit of extensibility late.r We're not pinning ourselves down to specific device capabilities. What if i have devices that can go into these folds but cannot provide angles? The lower level extension model here needs to be approached carefully.

Peter: agree. Not sure that this is solving a problem at this point. I'd like to see examples.

Ken: I'll get pepole to add examples. Not like every device will have to support all posture.s YOu might have one with a very small fold at the end, doesn't mean it's tent mode, that is up to manufacturer.

Peter: different ways things fold, I get that.

### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov

Rossen: I want to spend more time with this one.. move to B?

### [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo

Rossen: not ready to close on this, I think we have other open  discussions..

Peter: we don't have Tess or Dan, we have feedback

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Lea: this is about a controlsList attribute that provides a blocklist of controls not to display in media elements. It was proposed by Chrome a few years back, strong opposition from webkit, Chrome implemented anyway. Their motivating use case was that they had added a download button to serve users that needed to dwonload content, particularly in countries with slow internet connections where people cannot stream. A lot of content authors wanted to remove the download button and implemented controls from scratch which has accessibility problems. So the pushback from webkit was we don't offer a download button and we'd be forced to implement this nodownload keyword and we shouldn't have to implement stuff for features we don't support. Was supposed to be a DOMTokenList. If webkit did not implement nodownload authors could do does controlList support no download and if it doesn't they could just not display. But it's now in shipped Chrome. Also a side debate about if this is about removing controls from the toolbar or about disabling capabilities altogher. Proposed feature is to remove the control but it's still in the context menu. Authors might still want to disable the context menu which is not idea. So may point towards disabling capabilities instead of this controls list attribute. Also debate about why a separate attribute, why not turn controls list into this blocklist in the same way the download attribute works, either as a boolean or have a value, since this list only makes sense if controls are enabled. Arguement against is you need to be able to toggle controls on and off individually. Setting controls to false would throw away your controls list. Proposed instead that chrome could implement a vendor specific attribute, x-no-download, but there was pushback because we don't want more vendor prefixed attributes. A lot of suggestions about an idividual nodownload attr, standardise, but then a cornucopia of no-whatever attributes. Chrome said at the time they are implementing more features authors might want to disable in the controls. if we can't do that it prevents improving the default controls over just pointing authors to implement custom controls.

... personally the chrome arguements make more sense to me. Worse for the web to push authors to implement custom controls, avoid that at all costs. I would not want them to have to implement a vendor prefixed attirbute. Then if gecko implements a download button next? then we have a different one? Having a nodownload attribute doesn't make sense because we end up with a bunch of no-whatever attributes instead of a single feature that authors learn once, and a clear path for disabling any new features.

Rossen: do we know where webkit stands at this point? This conversation is a while ago

Lea: multiple conversations, as far as I know they're still opposed

Peter: who are we helping by disabling the ability to download video? a lot of sites go to greath lengths to do things to make videos non downloadable, but it's always to the disservice of the users. They should serve user needs, and let people download a video if that helps their experience. Arguments about not wanting to encourage people to make custom controls, and the UA always has a clean way of downloading video..

Lea: with the feature they're proposing it's only the control on the toolbar, the download capability is still there

Peter: seems even more useless, just making it harder for a user to do something they can still do

Lea: implemented for 3 years, would be interesting to see how it's used in the wild

Rossen: that should be queryable pretty easily.. 

Lea: don't want to disable the capability altogether, but content authors complained they were making that visible

Rossen: 4.8%, that's quite a bit

Lea: it is

Rossen: if all of it is youtube... no, quite a lot of random websites. Yeah, it's used a lot.

Lea: a bunch of libraries for adding custom controls. Not such a huge deterrent for authors. there was the argument that if we don't add this attribute authors will just allow the download button to exist over the burden of implementing custom controls, but given they can easily drop in a library, it's not such a hurdle to them. No library can match the localisiation and accessibility of the browser.

Peter: agree, but concerned that overriding user controls over media is a dark pattern. Just because lots of people do it doesn't mean it's good. I don't know if baking a dark platform into the pattern is a good idea.

Rossen: you should add this to the design review and see what the authors come back with

Peter: just questioning higher level.. should we do this?

Lea: I agree with that. I'm torn. There's a tension. If you say users should be able to download content then you push authors to implement an even worse user experience. It's like saying no you can't customise scrollbars because the scrollbars might be hard to use, then authors end up implementing even worse scrollbars. We see this over and over.

Peter: agree there is a tension. Lots of websites do things that are bad for UX, and should we be helping them do that?

Lea: Meta point - we were asked for a tag review by chrome becuase of this dispute with apple. Is a TAG review the right place for this?

Rossen: not a bad place

Lea: tess last week said it shouldn't work that way

Peter: we can be asked to settle disputes. If that's what this is it's fair to ask our opinion. They didn't use that template. We dont' have the authority to say what they must or must not implement. Want to know higher level user needs, what benefits?

### [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @hadleybeeman, @atanassov

Rossen: started reading through this... First issue was that the explainer that they provided is none.. with the comment that it seems like overkill. Here's discussion, here's the spec. An opportunity to explain why we need explainers.. then start from there.

### [Capture Handle](https://github.com/w3ctag/design-reviews/issues/645) - @rhiaro

Amy: haven't had chance to look, defer

Peter: more people assigned to this?

Amy: ask in plenary?

## Breakout B

Present: Rossen, Peter

Regrets: Sangwhan


### [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober

Punted

### [MediaStream Image Capture (wide review)](https://github.com/w3ctag/design-reviews/issues/651) - @plinss, @atanassov

Reviewed briefly. Have some questions about PhotoSettings, posted to issue.

### [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov

Punted

### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov

Punted


## Breakout C

Present: Ken, Dan, Amy, Yves, Sangwhan

Regrets: 


### [MiniApp URI Scheme](https://github.com/w3ctag/design-reviews/issues/478) - @cynthia, @ylafon

Yves: think we should close them and review when things are going out of the WG

Sangwhan: agree

Dan: [leaves note]

### [MiniApp Manifest](https://github.com/w3ctag/design-reviews/issues/524) - @cynthia, @torgo

as above

### [MediaStreamTrack Insertable Media Processing using Streams](https://github.com/w3ctag/design-reviews/issues/603) - @cynthia, @torgo

Sangwhan: I think we did review this

Yves: missing internal discussion in the WG about details, everything else is fine on our side

Dan: already proposed close, close it now

Sangwhan: *closing noise*

### [Resource Timing](https://github.com/w3ctag/design-reviews/issues/641) - @cynthia, @kenchris

Ken: one is an update to an existing spec, do we have a list of changes?

Dan: we don't really have a list of things to review..

### [User Timing ](https://github.com/w3ctag/design-reviews/issues/642) - @cynthia, @kenchris

### [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - @rhiaro, @hadleybeeman

Yves: interesting [discussion on mozilla position repo](https://github.com/mozilla/standards-positions/issues/539)

Dan: sympathetic to Anne's point about being wary of adding functionality to popups

Ken; I don't think this is adding new feature.. popups as a communicatin channel are disabled if using sharedarraybuffer. This is about with an opt in renabling that communication channel so people can continue working and still use shared arraybuffer because additional protection was put in place

Dan: not clear on user need

Ken: sites working today with payment via the window object, former popup, that's how a lot of payments work in Denmark.. that works toyda. These sites might be using that feature ands hared array buffer and want to use shared array buffer but at some point that's going to stop working because to use shared array buffer they need changes which will disable the features.. There's going to be a solution to this which is changes to web payments and Web ID..

Dan: webid is not about payment it's about id flows.. red herring.. I see people saying webid fixes this but that's not to do with payments

Ken: argument is it'll be fixed in the future, but it's way in the in future so we need something now. I'd like a security expert to be able to evaluate whether it's secure, I'm not sure. Ongoing discussion, how much we should get involved? Except who has looked at this for security.

Yves: would be good to have apple's input

Dan: need user needs.. why do these sites need sharedarraybuffer? In service of what? Need clear statement of user needs in the explainer. [writes comment] .. looks like a patch

Amy: scope of problem is confusing because it's tied up with all of these other secs, credentiallless, anonymous iframes

Dan: discussion in Mozilla thread about how webid addresses this, but webid is a set of ideas, which don't seem to address the payment case.. a lot left unsaid..

### [webxr camera RAW!!](https://github.com/w3ctag/design-reviews/issues/652)

[triaged]

Dan: [Left comment](https://github.com/w3ctag/design-reviews/issues/652#issuecomment-870408043)

## Plenary Session

Present: Tess, Dan, Peter, Yves, Rossen, Lea, Amy,

Regrets: Kenneth, Sangwhan

### Breakout Rollup

#### New Computer for Peter

#### Breakout A

Dan: you all talked about device posture API... explain yourselves

Rossen: new API is great. Simple. that was the main feedback. Can't be any simpler, now is that useful. If it's useful is it something we can take forward and build upon to extend it, add additional folds, etc. 

Dan: Samsung hat on - we already have an implementation shipping in our beta of the previous version and now we're going to be updating it for a version shipping in august. Doing a whole bunch of testing with devs trying to answer that question, is it useful, to make sure we provide user research

Rossen: perfect

Peter: Rossen posted feedback, I added a followup. I think we can get where we need by tightening definitions of what they mean. 'book' posture gives me some sense but doesn't tell me what i do with my page design. If it's defined as folded in the middle, fold is vertical, pages oriented towards user, that tells me what I need but I don't see that in the spec

Dan: I'll feed that back

Peter: talked about media element controls list

Tess: i have lots of thoughts about that. Fair amount of behind the scenes stuff relevant to that..

Yves: would be good to have apple's feedback on anonymous iframe and communication between iframes security thing that is going on. There is a discussion on the mozilla position that can be interesting for other people to read.

Peter: Lea gave a good breakdown on media controls of the position of giving authors control vs forcing them down a path of implementing all their own controls which makes it worse. I pushed back on if this is really an antipattern, a dark pattern that we want to expose, are we doing a disservce

Tess: part of the webkit position is related to that. The browser is the UA, the default set of controls are chosen by the user agent because it believes they are the kinds of controls that users want. Each browser can make different decisions depenedng on their user needs. If sites want to author their pages in a way that is hostile to user needs which I think is a fair retelling of wanting to disable certain default controls, then the site should have to do some work to dothat. I'ts not impossible, you can build your own controls. But it's harder than just using the default controls. That friction is serving a purpose. That is discouraging sites from doing this thing. Discouraging sites from being user hostile. They can still do it, there's lots of terrible antipattern content. We don't need to be encouraging sites to do it, dont' need to make it easy for sites to do it. In particular this issue acme about because of UA specific native controls. that the other uas don't even have. Which makes it especially challenging to have any kind of standard feature to enable or disable that. But to get deeper into it I have to dig into history, there's a lot of history there, sutff proposed to HTML years ago, then it had a zombie life in WICG after it got shot down and has come back for roundtwo. As far as I can tell the multi implementer opposition was still there. 

Peter: another sublty - I've built an app taht where we hid the controls and built our own, but not because of being hostile to user, but fitting a style or asthetic. Also a use case for exposing the controls in a way that they can be styled like form elements.

Tess: trick there is display none, visibility hidden, translate -5000px.. I agree that having some ability to control the look and feel of native controls is valuable, I do think there's a tension between customisablbility and meeting user need. As far as I can tell there's active work there. there are media enegineers on multiple engines who expose different kinds of stylability. We should converge that so it's spec'd somewhere, what you an tweak and how much. Having a general mechansim for here's a giant pile of css to apply to controls is probably too risky given the chance of abues

Peter: sure, I know there's work on stylability of form controls and you mention stylability of media, are they talking to each other?

Tess: i think so, I think it's the open ui people, but I don't know for sure, my impression it's on their list of things to get to. They're working through a list in a particular order, they might not get to it for a while, but afaik something they're aware of and want to get to.

Lea: stepping back, want to reply to one of Tess' points - of course a UA is an agent for the user, and therefore if there's a download button that serves the user we should encourage authors to have it. A tension - if autors implement custom control that doesn not serve the user, the more we push them ot implement custom controls the less the user is esrved. It's not a deterrant, they just include a library. It's the end user that gets harmed, now in addition to not having a download button they have worse accessibility, worse localisation, worse everything

TesS: worse platform integration

Lea: I think the user loses on both sides. I don't think it's that simple.

Tess: I agree that due to user hostile desires of sites the user loses either way. That's true. I don't think we need to condone that. The web platform should be designed with user needs first. If sites want to circumvent that they already do a hundred thousand different ways. Doesn't mean we should capitulate. 

Lea: I don't think it's capitulating if they can remove a download button. Part of the reason of not styling form controls and scrollbars was to protect the users, but we ended up in a situation that was worse for users

Tess: give and take over time, you find some kind of equilibirium that tries to square the circle. 

Lea: we have data on this now. Rossen look it up. 5% of sites that use controlsList. 5% that will us custom controls instead

Tess: 5% using a chrome-only feature. Chrome can ship features and get adopion on a giant swathe. I don't see anything the TAG saying changing the market reality of browsers. 

Lea: my point is people are using custom controls in that 5% of sites because controlList exists. If webkit or gecko implemented a download button tomorrow and people realise it doesn't work any more, they won't just accept the download button. They'll implement custom controls.

Tess: not sure about that. Videos on iOS on a phone is fullscreen and you only get the default controls, you don't get custom controls.  UAs are free to make sure video playback is user friendly. 

Peter: put this issue back on agenda and get into it more

#### Breakout B

Peter: Rossen and I looked at image capture, gave some feedback

#### Breakout C

Dan: we closed a number of issues. Miniapp URI scheme, miniapp manifest, mediastreamtrack, all propsoed closed. They were waiting on Sangwhan. Resource timing and user timing - both we need a lot more detail. Asked for more, we do have a response. They didn't include an explainer, saying it's a tiny change to an existing spec. Talked about COOP same origin allow popups thing.. it's complicated. Asked for more about user need.. and clarify relation to discussion in mozilla and whatwg, there's more stuff to talk about here.

#### Kick-off of [Privacy Taskforce](https://github.com/w3ctag/privacy-principles/)

Dan: [summarizes what happened with the kick off call]

#### [research in specs](https://github.com/w3ctag/process/issues/26) issue from Terence Eden

Lea: a lot of time private research that is not disclosed. The results should be disclosed publcly. I think it woudl be great if we could require user rsearch but not feasible. But it could be feasible.

Tess: Raised this on the TAG process repo - this feels like an idea for the w3c process.

Dan: this issue came out of a discussion between Terence and myself. Originally it was Terence saying W3C should have this thing as part of its process. I said yes, it makes sense, big issue, but a thing we could do - I suggested raised in TAG - maybe we could put something in our issue template that encourages people that are .. in the spirit of what we can do as TAG, we could encourage this way of thinking by saying in our issue template or in the explainer explainer

Tess: if there's research, link to the public

Dan: yeah, if the reasoning of your explainer is based on research can it be made public, to encourage people to think that way

Tess: great idea, we should do that in both places, explainer explainer, have a section for research and in the design review issue templates to ask for research. I stil think it's a good point that should be talked about for W3C process, we should move it. I'm happy to file follow ups for the explainer explainer and issue templates, but this itself is an issue with W3C process itself and should be considered by the whole community

Dan: process CG?

Tess: yes

Dan: don't want to kick it to there but maybe open a duplicate?

Tess: Terence filed it, ,if he wants to move it that's fine. We should file followup issues for our changes

Lea: agree we should open an issue in process CG. If we want to encourage this kind of thinking there's an extra step, we could also ask why if they say there's no research ,we could ask why, which would og further to encourage user research without preventing anything from happening.

Yves: Process CG or AB involved here?

Tess: Process CG is the right place because the conversation is generally public so Terence can participate. The AB is generally present there. They also have their own AB-only conversations about things. If they want to have a private follup they'll know about it, they'll see it in the CG. Actions? I'll take issue templates.

Lea: I'll take explainer explainer

Dan: I can [file issue in Process CG](https://github.com/w3c/w3process/issues/551).

Lea: timeframe?

Tess: no rush.. get to it when you do

Dan: we have a non design review week next week, we can merge then if simple

Lea: aim for that

#### [High level vs low level design principle PR](https://github.com/w3ctag/design-principles/pull/291)

Rossen: this was on the PR that has been hanging.. My main feedback was that when we initially discussed the issue we had a general consensus around making advice that API design should come with ideally layering, think of components composed in different layers, and when you go to expose the new features you start by exposing high level API surface which is usually minimal, while allowing all of the broader functionality inside of it. As well as at that point you have a solid support from the rest of the platform in terms of privacy, security, etc. Once you ship your feature if it proves useful and whatever your users were asking for then you continue going down the line of figuring out how to further extend it by exposing lower and lower layers as part of the api set for that feature. Not to say that there are no features that emerge on the web or patterns that are composition sof many different already available lower level apis. And such features usually make it back into the platform as this higher level construct that is adtoped and adapted by engines and made available through ?? api. The last piece there is whether or not we have examples of the opposite where we have something higher level and we want to expose lower level. This is the normal pattern we usually use. The biggest of those examples and the easiest to point to is the efforts with css houdini where we have an entire system that proves very capable and useful, the layout and style in the platform, over time the usefulness and popularity outgrew its api surface so we're going further down by breaking it into lower level primitives that people can take forward, we can learn and figure out what's in libraries and what is in platform. That' sthe summary. We had a really good chat with Lea last week where we didn't come to consensus on that point. I dunno if you want to take a minute to explain your point of view? And how it was supposed to go into the PR.

Lea: that was a reasonable summary. From my pov I thought our consensus was that the guidence needs to be nuanced becuase there's no one size fits all. we can't blanket recommend that everyone starts from a high level api. Works for some features especially with privacy and security considerations. For others it may make sense to start from lower level primitives and add higher level features later as patterns emerge. There are a lot of examples on the web platform where things started from lower level, sometimes without even knowing use cases that were going to emerge they weren't designed based on these use cases. Certain use cases and patterns emerged organically and we added higher level apis afterwards, eg. reseize observer could be done with polling, but it was done often enough by authors that eventually it was added. Or all the new HTML input types, or details and summary, or querySelectorAll we started from lower level querying functions because this emerged in libraries time and time again. If we started higher we would probably have ended up with xpath at the time given how XML obsessed everyone was! AppCache tried to start high level and failed. Both approaches have their merits and my impression was when we discussed this the consensus was guidence needs to be nuanced. It seems that Rossen's impression was the guidence needs to be to strongly recommend high level APIs first. Which one was it?

Tess: there's an aspect which is related to the rule of least power. We want to encourage people to use the least powerful tech that fits the need. I do think that exposing the highest level api which allows users to do what you watn them to do is a good thing. I do think that the ultimate advice has to be more nuanced beause hpart of the point of thinking about this at all is how do we reduce the cost of cliffs. I do think people should expoes the higher level version of the thing if they can first. 

Rossen: that was my point. I want them to expose highest level possible *if they can*. Not insisting that they expose higher level or nothing at all. Also interesting that ll of the examples Lea gave were examples fo the second point I was making which is enoough patterns emerge and we recognise those as useful features and bring them back as a higher level thing. So it's the thing that we're talking about that we're bringing back to the platform. My initial issue was that the current PR was written the other way around. Written starting with lower level and as you build it up you add higher level features/api.

Lea: as long as I'm clear on group's consensus I can rewrite as needed. Wasn't clear on which. Looks like Rossen and Tess are in agreement. What do the others think?

Peter: feelings are mixed. There are examples of where in the past we've recommended starting with low level things, that's where web componants came from. On the other hand, the view of expose highest level api that you can makes sense. But doesn't mean what you're exposing is a high level api... highest of the low level maybe. Maybe that's where the nuance is missed

Rossen: good clarification. Not all features are going to be an HTML element. Probably part of the confusion.

Peter: there's often times we do want to expose and build something that is a low level feature. Doesn't mean we start at the bottom. Expose the highest version of that low level feature that makes sense.

Lea: yeah. The way I see it is more in line with how Peter sees it. 

Peter: I don't think we're disagreeing, just a matter of how we express this. Lea you have what you need?

Yves: if you look at the history of how good apis are designed, it really depends. There is not a perfect recipe. Some people make ideal high level apis for some use cases and bad ones for others. Depending on how people will ultimately use them. It's quite difficult to say it should always be done that way. Mixed feelings about that. Good to define very high level but still being able to provide more complex low level api that have more controls so you can do things that are not the 90% use case in a friendly way. 

Lea: ties into other PR about common cases should be easy and complex cases should be possible.

Yves: yep

Rossen: we have enough to move forward here?

Lea: still unclear on recommending against starting with lower level primitives? is that an antipattern?

Tess: I'm inclined to say yes, at least weakly. It shouldn't be worded as an absolute prohibition, but we shoudl be encouraging peopel to start higher. One of the things I find .. background.. I'm not a signatory of the extensible web manifesto. It's something I agree mostly with but disagreed enough to not put my name on it. Specifically I think that the thinking around it often conflates the model that a thing is built on and API that is exposed. It's important as you design something that's high level that you think about the underlying model that makes that higher thing possible. May make sense in the future to expose some of that model as API but not necessarily the case, and there are cases where we don't want to. Starting with low level it's easy to make the mistake of exposing things you shouldn't. If I have to expose everything I need to build this high level thing. Needs to be possible in the future if there's a concrete use case that it nees the lower level thing then there's part of the model that can be turned into API. Need to do the conceputal work of designing the high level thing in terms of lower level pieces. Just don't think they have to be API. If they're API or not depends on author and user need.

Peter: that tracks with past discussions. The guidene should be start your design from the low level primitives and build a coherant model, then what you expose is you start at the top down of the model and figure out how far down you're exposing.

Lea: I think that's basically what's in the PR now... something about building blocks that you may or may not want to expose

Rossen: with the exception of talking about starting with the highest level

Lea: I can add more explicit encouragement, although I still have reservations, sometimes starting at high level gives you higher chance of getting it wrong. But fine to edit if there's consensus.

Dan: Focussing on encouraging positive behaviour rather than scolding negative behaviour is where we ought to put the attention, that will have the effect we're looking for. That's partially trying to address the question of should we say xyz is an antipattern

Lea: not if we say that in PR, just asking for my own clarity. I think we have what we need.





### Issue Triage
