
## W3C TAG Breakouts & Plenary - 17 Feb 2020

### Agenda

#### Breakout A (Europe / US) - [2020-02-18]

#### Breakout C (APAC / Europe) - [2020-02-18](https://www.timeanddate.com/worldclock/converter.html?iso=20200218T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Gamepad Light Indicator extension API](https://github.com/w3ctag/design-reviews/issues/362) - @cynthia
* [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia
* [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris
* [Native File System API](https://github.com/w3ctag/design-reviews/issues/390) - @cynthia, @kenchris, @lknik

#### Breakout A (Europe / US) - [2020-02-18](https://www.timeanddate.com/worldclock/converter.html?iso=20200218T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471) - @torgo, @plinss
* [Foldables CSS](https://github.com/w3ctag/design-reviews/issues/472) - @hober, @torgo, @kenchris

#### Plenary Session - [2020-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20200219T210000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

### Minutes Breakout C

Present: Kenneth, Hadley, Alice, Sanghwan, Dan, Yves¡¡

#### [Gamepad Light Indicator extension API](https://github.com/w3ctag/design-reviews/issues/362) - @cynthia

Ken: this is old...

Sangwhan: I'm OK with this.  Last update was 11 months ago...

Dan: what's the status & venue for this work?

Sangwhan: no this looks like it 

#### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370) - @cynthia

Sangwhan: I finished a review...

[discussion on whether this applies to bluetooth...]

Sangwhan: browser doesn't care... it's an implementation detail...

Sangwhan: 2 issues - 1 is that HID devices are 2-way. You can write to a HID device. You can read from a HID device.  Given that the user has said "you can use HID devices on these 2 origins running in 2 different tabs" they could communicate with each other. That breaks the [web security model].  Leak cross origin information...  They are aware of one device..

Ken: you could make that not possible.

Sangwhan: block writes? that might be problematic.

Dan: couldn't the spec mandate that one context could have a connection to a single device (exclusivity)

Sangwhan: i mentioned that - also in the context of race conditions.   They said it needs to be implemented carefully...  They don't have a proposal to address this.

Ken: also with Native apps to and from webapps..

Sangwhan: yes you could leak between web and native. This can be a side channel...  I mentioned that. they did suggest it might make sense to restrict write access to a single tab.  Also: they expose serial numbers which is problematic.

Dan: maybe ping them and see what the current state is and mention these issues?

Sangwhan: OK i will do.  One architectural question - unique identifiers that come from the system... 

Dan: we need to put that into https://github.com/w3ctag/design-principles/issues/152

Hadley: done

#### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338) - @cynthia, @dbaron, @kenchris

Dan: [reviews status of issue](https://github.com/w3ctag/design-reviews/issues/338#issuecomment-580970955) 

Dan: feels like we need to re-review it with the new design

Sangwhan: pick this up at the f2f?

Dan: new proposal here: https://github.com/WICG/main-thread-scheduling/blob/master/PrioritizedPostTask.md

Ken: this is one of 3 proposals in the issue. Maybe this should be split into 3 reviews?

Dan: Maybe their priorities are changing?

Hadley: they do have separate explainers for each...

Dan: I will bump this to the f2f and Ken can you please leave a note in the issue asking them what their current priorities are and how we can be most useful?

#### [Native File System API](https://github.com/w3ctag/design-reviews/issues/390) - @cynthia, @kenchris, @lknik

[some discussions on covid-19 and impact on next f2f]

Sangwhan: general binary blob access - a filesystem - is useful. or do developers want access to "the" filesystem - which is a can of worms.

Dan: agreed it's a can of worms - interested to see what this proposed design is...

[bumped to f2f and dan will try to get more info about the mdn survey]

### Minutes Breakout A

#### Present: David, Kenneth, Dan, Rossen

redux on scheduling API...

#### [Foldable CSS](https://github.com/w3ctag/design-reviews/issues/472)

Rossen: the proposal came around a month ago - a response to new devices announced last year - by Microsoft and before that by Samsung. Idea is to have capability to decide if something spans multiple screens (1) and then - if it does where is the hinge? The API has a number of iterations - final one they came up with in MS is that it provides a media query. One discussion that came is - address second screen or multiple screen.  Yes we can extend for multiple screens... ... not sufficient use cases... in windows we introduce APIs that can give you an idea of where the hinges are... bottom line the current proposal doesn't preclude multiple / second screen scenarios...  CSS group favourable to it...

Ken: i think it's fine ...

Dan: some Samsung stuff.. around folding continuous screens vs separate screens...

Rossen: triggering animations with environment variable that changes...  position of the fold could trigger animations... Multiple different scenarios - where the hinge is - would grow... we have scenarios where you have a super bar ... (area that is used for something else - e.g. buttons). Very aligned...

Ken: on the Samsung phone you still have a display on the hinge..¢. 

Rossen: on our devices the hinge is physical but we also have software that extends the area where the app thinks the hinge is... 

Kenneth: i think this is the right approach - right direction in my opinion...

[discussion on angle]

Ken: wouldn't angle be a separate API?  

Rossen: there could be many folds by the way... not just one.

Dan: there is at least one out there with 2 folds...

Rossen: many prototypes out there... 

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

[bump to plenary for now]

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

David: [referring to mozilla standards position disucssion...](https://github.com/mozilla/standards-positions/issues/238) different mental models of what is going on here (and what a good analogy is).. 

Dan: the use cases in the explainer are pretty clear...

David: what risks are there and how do you explain permissions to users?

Ken: the way I see it... everything is unencrypted... if you have access to the camera it's similar. the whole problem came up because yubico is exposing passwords..

David: passwords or one time codes?

Ken: by default it's one time codes but there is an advanced mode where you can create static password

David: one concern is that yubikey exposes one time codes which could be read by the web site.. other set of concerns are what the permissions around writing should be and whether it's possible to explain them to users...  3rd piece was : does it need some kind of permission around reading and how do you explain that?

Ken: there is a permission of using NFC as a whole... No specific permissions for writing... You can make it read only...

David: there are going to be some devices that aren't read only and therefore the page would have permission to write with them...

Ken: It needs to be focused, it needs to be unlocked (the phone), the user needs to be on the web page, it needs to be...

Dan: (raises scenarios about user touching an NFC tag which then loads a web app)

Dan: what are the abuse cases?

Dan: devices have NFC buttons and advertise NFC as a function --- users will begin to have some understanding of what NFC is similar to Bluetooth...

Dan: i guess the question is... we could close it and acknowledge that the debate is still going on elsewhere...

Dan: I will note that the MDN Developer Needs Assessment did indicate that web developers do want APIs that allow them to access device features.

Dan: propose closed?

David: i think it's reasonable. Tess may have opinions as well.

#### [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471) - @torgo, @plinss

### Plenary

Present: Kenneth, Hadley, David, Peter, Tess, Alice, Yves

Regrets: Sangwhan, Dan, Rossen

Scribe: David

#### Breakout Rollup

##### Breakout C

###### [Gamepad Light Indicator extension API](https://github.com/w3ctag/design-reviews/issues/362)

Kenneth: Trying to remember... we were proposing to close the issue.  Sangwhan seems happy with it.  If no other comments, we should close it, unless anyone else wants to look.

Peter: This is the one where he was initially worried about the lights being a communication channel between origins, but turned out that wasn't a problem.

Peter: OK, I'll close the issue.

###### [WebHID API (Human Interface Device)](https://github.com/w3ctag/design-reviews/issues/370)

Hadley: looked like we had question about whether communication was possible across origins

Kenneth: Also question about whether works over bluetooth classic, or only constrained to USB.

Hadley: Said we'd put it in our device enumeration issue on design principles but doesn't look like we did ... I'll do that now.

Peter: Looks like Dan set milestone to face-to-face.  Maybe more to discuss then?

###### [Scheduling APIs](https://github.com/w3ctag/design-reviews/issues/338)

David: there was brief followup in breakout C about this -- and it's now split into a bunch of separate issues.

Kenneth: I think the thing we discussed was having multiple APIs in one issue -- I think they filed the `isInputPending` review.  We were confused about priority and what to look at first.

David: @shaseley asked to have this cover `postTask`, so perhaps we should do that?

Peter: yes

Kenneth: Should also fix explainer link.

###### [Native File System API](https://github.com/w3ctag/design-reviews/issues/390)

Peter: has face-to-face milestone as well.

##### Breakout A

###### [Badging API](https://github.com/w3ctag/design-reviews/issues/387)

Kenneth: ?

David: I think we had neither Tess nor Alice so wanted to bump to plenary.

Peter: now or face-to-face.

Alice: Should we wait for Dan?  Not sure how good videoconferencing option at face-to-face will be?  Tess and I probably most active on issue.

Alice: If we were to talk about it now... Tess and I talked a couple weeks ago.  We disagreed on whether there should be 2 APIs.  I'm reasonably convinced there should, Tess is not.  I'm uncomfortable with 2 APIs looking so similar; Tess thinks they should be more similar and in fact the same.

Tess: That's a fair summary.

Alice: I think the fact that there are 2 APIs that look exactly the same will create confusion.  `navigator.setClientBadge` versus `navigator.setAppBadge`.  I'd want the APIs to look different.  `setAppBadge` is where there's only one surface (icon/bookmark); I think setClientBadge should perhaps live on document, very different because they're different things.

Tess: I'm comfortable with you providing that naming feedback on the issue.  I'm with you on the naming.  Could be comfortable with `navigator.?.setBadge` and `document.?.setBadge`. Or maybe one of them isn't called badge at all?

Alice: I can talk to Matt.

Tess: Maybe Dan will have a third set of thoughts.

Alice: I'll give feedback, and we'll check in again at face-to-face.

###### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461)

David: We discussed possibly closing, and how we all have different analogies for it.

...And what happens if a user touches a web app and that web app wants to use webnfc, and what that looks like.

Kenneth: If the nfc tag triggers loading a web page, no special data passed through.  Would then need to touch again to read the NFC tag.

Tess: Subsequent to breakout I commented on the issue, raising concerns about not knowing how to word the permission prompts for this to get meaningful consent from users.  Subsequent conversation about that.  A bit of pushback from one person who wants a rigorous description.  I don't want to design a user study for him; I think we should be describing the relevant principles, ask people to do the work, and show their work.  Though I'm not sure what to do with the thread at this point.

Hadley: I'm scanning the conversation -- looks reasonable.  I think we can say thanks, we've done the bit under our remit, it's now up to you to design the thing.  Perhaps we've been in loops where it wasn't clear what the role of the TAG was -- people feeling they need to iterate on the design with us until we can rubber-stamp it.

Tess: That's useful, still not quite sure how to get out of conversation.  But I think you're right that confusion over role of TAG is involved here.

Alice: Worth thinking about which parts are meaningful -- I think motivated by unhappiness with the feedback -- but what can we do to be clearer -- are there other resources we can point to to explain when the prompt isn't good enough?

Hadley: design principles?

Tess: Some text (a little) in David's PR.  Tried to link to resources I had at hand.  I linked to workshop report from San Diego on permissions and one of the other artifacts from that (checklist).

Tess: I think we should add to design principles.  I don't offhand have all the resources to point them at.

Alice: Can you describe why it's a bad prompt?

Tess: "The Website wants to send and receive info when you tap your phone on an NFC device".  First, not clear that it's sending to/from the NFC device.  What's the nature of the info?  The yubikey example is interesting.  Given the general nature of API, I don't know how to write text that makes threat/tradeoffs clear.  I work in the space and understand the technology, so I think I could make an informed decision with a specific NFC device in my hand and I knew what was on it.  But not knowing much about the device I wouldn't know what to do.  But I"d want less knowledgeable users to understand this.

Hadley: Can we pull something out of ethical web principles? Ex: 

> [Security and privacy are essential](https://www.w3.org/2001/tag/doc/ethical-web-principles/#privacy)
>   
> We will write specs and build platforms in line with our responsibility to our users, knowing that we are making decisions that change their ability to protect their personal data. This data includes their conversations, their financial transactions and how they live their lives. We will start by creating web technologies that create as few risks as possible, and will make sure our users understand what they are risking in using our services.

Kenneth: Same problem with camera -- might pick up text.

Tess: Camera and microphone are interesting -- I think it's much clearer to an average user that camera takes in scene around you.  Though might not realize how easy it is to find the location.  But 

Tess: I think Camera is a case where permissions well, there's a lot of nuance about what you're granting, but I think users can get the gist of it.  Though I think David used geolocation as an example.

Kenneth: Yubikey is a special case; shouldn't have used NDEF for this.

Tess: Web is meant to be secure, though.

Peter: Sensitive stuff like credit cards and passports.

Kenneth: Those aren't over NDEF, though.

Tess: But Yubikey thing is the existence proof that hardware developers might expose that kind of information.  I don't think it's fair to dismiss that as "they shouldn't have done that".  If there's a fatal flaw like that, we should clearly identify it.

Kenneth: Also I think it's not exposed by all Yubikeys.  Security issue here is with Yubikey; can already get this with any native app.

Hadley: (question)

Kenneth: If I tap my Android phone on an NFC tag that an app can't handle, Android will show the data in a native UI.

Tess: I don't think we should make that mistake on the web.

Peter: Difference between exposing info to person holding both devices versus to a website halfway round the world.

Tess: How to respond?

Alice: In terms of responding... might be worth raising the point about yubikey as an existence proof since I didn't see that there.

Hadley: Also something potentially ... might be jumping to conclusions based on previous examples... but we've run into cases where developers haven't thought about the difference between the web and the feature in the browser... Difference between not being able to specify UI makes this more complicated?  If they feel comfortable with the risks in Chrome; it's another thing to say to other browsers that you'll feel comfortable with it as well.  I think that dividing line isn't fully divided in this conversation.

Tess: Agree it's a useful line of questioning.  Also, a more general concern, this is a specific case of it.  More general concern is that hiding powerful features behind permission prompts is often not a good enough mitigation.  There are tradeoffs not often looked at.  Scary?   Put it behind a permission prompt.  But what you say when you prompt, how informed when say Allow, is relevant.  But also permission fatigue, but if we keep prompting users, they're just trying to use the site, they'll just hit allow a bunch until it lets them do the thing.  We should be careful adding permissions prompts because adding more increases chances of permissions fatigue.  When I see new spec say "just put it behind a permission prompt".  Given the cost of permission fatigue and the difficulty of designing a prompt, why do you think this in adequate mitigation?  I think that conversation should happen more in other reviews as well.  Sometimes there's pushback on how to word a permission prompt to do this that "UI is out of scope" ... some browsers may prompt, some may use engagement metric.  True, but as a smell test... if you can't figure out what to say, that's a smell.

Tess: David, you and Dan had the conversation in the breakout, could you raise that example.

David: sure

Peter: OK, and I'll set a milestone for face-to-face and we can loop back and review

###### [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471)

Peter: was just bumped due to lack of people

###### [Foldables CSS](https://github.com/w3ctag/design-reviews/issues/472)

Peter: looks like a bunch of discussion on that one.

David: I think mostly Rossen and Dan.

Peter: I also want it to cover things like desktops and multiple monitors.

Hadley: If that's the case, does the name need to change?

David: I think some (Dan, Rossen?) didn't want this to be multi-monitor.

Ken: I also had that position: multi-monitor is very generic.  Monitor positions can be arbitrary.  Google had 2 proposals for finance use cases: window enumeration API.  This is really for things that are connected with a possible seam with no display.  This should be as simple as possible for existing content, treated as one viewport.  I think that's the right approach.  Treating this as different screens you'll get few developers optimizing app for those use cases.

Peter: I'm not saying different screens in the sense of multiple viewports.

Kenneth: Approach here is one viewport.

Peter: I know people with multiple monitors that are still one viewport, a window dragged across, with some gaps in the middle.

Kenneth: I think that's a minority use case.  Even if you create the API that could work with these cases, developers won't test on those cases, it will break on other devices.  All thees other configurations that people would have to test as well.

Peter: Also half a dozen configurations of foldable screens and people won't test on those either.  Microsoft has an emulator.  Mac historically had UI where you can tell OS what monitor configuration is.

Kenneth: I'm worried this would make API much more complex.  At least API should be designed so it wouldn't break if configuration is a bit nonstandard... opt in to supporting an unusual configuration, e.g., with media queries.

Peter: Certain things like aligning grid column widths or row to these screen gaps.

Peter: The future heading to foldable screens.  Microsoft heading short term solution with a physical hinge because foldable screens aren't there yet; I think that's a stopgap measure that won't be there in 3-5 years.  Or foldable screens will fall out of fashion entirely.  Multi-screen desktop has been around for use, more likely to be around longer in the future.

Kenneth: More likely tablet/laptop than phones, but support phones too.

Peter: I've seen laptops with 3 screens that fold out.

Kenneth: Intel has done it, a lot of different prototypes.

Kenneth: I think Microsoft hinge way will stay for a while; issues with foldable screens.

Kenneth: I think API should definitely work whether a visible hinge or not -- should work with both cases.  I'm told this does.  Dan has other point that even if you have screen above the fold, still want to know where the fold is, reflection and animations etc.  Maybe a different environment variable similar to the other one.  Still fine if you have ideas to make this more generic, but don't want to make it too complicated for the simple cases.

Peter: I saw yesterday video made with a foldable flip phone.  When they folded the phone it stopped crossing the ???.  So adapted when the angle of the hinge change.

Kenneth: I hope Dan can bring Samsung devices to face-to-face.

#### Issue Triage

out of time, didn't get to it

