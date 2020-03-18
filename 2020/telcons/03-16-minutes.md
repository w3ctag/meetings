# TAG Calls for week-of 16 March 2020 

## Minutes

### Breakout A (Europe / US) - [2020-03-16](https://www.timeanddate.com/worldclock/converter.html?iso=20200316T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: David, Peter, Tess, Rossen (except from :15 to :35), Dan and Yves

Scribe: Rossen, then David

#### [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo

Dan: this goes way back and can't remember why it's lost in time.

David: last we looked someone had to write what the rules are but then it didn't happen. We should have this in one of our docs but not sure where. This comes up frequently thus we should write it.

Dan: design principles?

David: file an issue but we already have one :) keeping this open it doesn't seem to provoke further progress.

Dan: if this is guidance to devs it doesn't feel like a design review

Rossen and Tess +1

David: this is issues 41 in design principles. It is cross linked too.

Dan: agree to close this issue and move the discussion to the design principles issue. I'll schedule the design principles issue for 3/30/2020 which is our next design principles discussion.

#### [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris

David: filed an issue yesterday and we should probably wait for this or close and not wait?

Dan: should we trust the web components progress?

Tess: there is a vf2f on web components and I'll make sure to bring it there.

Dan: keep it but assign for the week after?

Tess: yes

#### [More restrictive hasEnrolledInstrument() for autofill data](https://github.com/w3ctag/design-reviews/issues/407) - @hober, @dbaron

Tess: not much has changed - the request is for a behaviour change. Most recent update is that they will add non-normative text to explain. That sounds fine to me.  I think we can close it.

David: it's a pretty small change 

Tess: we could post a comment asking for an update...

David: yeah

Dan: yeah

#### [HTML horizontal review: Browsing contexts](https://github.com/w3ctag/design-reviews/issues/452) - @hober, @torgo

Dan: a bunch of WHATWG PRs to review.

Tess:  Haven't taken a look yet. We've been pretty good at using face-to-face breakout time for these.  Should we do a one-off breakout together this week?

(will take scheduling offline)

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

David: Was hoping to provide some more specific advice here but hadn't gotten to that yet.

Dan: Bump for next week then?

#### [Title Bar Customization for PWAs](https://github.com/w3ctag/design-reviews/issues/481) - @alice, @torgo, @kenchris, @plinss

Dan: I might move this to... not sure why I put this here.  I think Alice and I should discuss in Breakout C.

#### [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482) - @dbaron, @torgo, @kenchris

Yves: Just looked at this, linked to issue we have on miniapps.  It's basically something related how to define hooks based on on the URL scheme instead of doing it using media types.  In that case... just skimmed it a bit earlier on ... seems that the ? mechanism is still http/https.  I think there's [something in webarch](https://www.w3.org/TR/webarch/#URI-scheme) for that.  What do they really want here?  Do they just want media types, or do they want a protocol to access them.

David: I think one thing that's led people to want schemes like this in the past that they want the URL and not just the contents of the resource.

Tess: Why not just use registerProtocolHandler.

Yves: It's expensive, and (missed).

Dan: I kind of had the same question.  Feels like web applications already do this.  Doesn't feel like there should be a PWA-specific thing.  The point of PWAs is that they're web applications; we can push back against technologies specific to PWAs, especially when web applications can already do this.

Tess: Restated: There could be some value in providing any web application that uses a web app manifest to have a way of saying what protocols they register from their manifest.  But I'd want to think that's syntactic sugar, 1:1 with a call to registerProtocolHandler from the web application.  Same underlying model and permissions and expectations.  If we want to change the model for the PWA case, I'd want to entertain changing the model for the non PWA case.  The manifest is convenience but not sole mechanism -- letting you know stuff that you could know anyway if you load the webapp -- it's letting you skip the loading.  I worry that redefining the feature risks bifurcating the models.  This should be by reference to `registerProtocolHandler`, or they should file bugs on `registerProtocolHandler`.

Tess: I'll take an action to review the explainer with that in mind and see if that feedback makes sense when I read it.

Dan: Bump it a week.

#### [Scheming Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon

Dan: Yves, I think this is the one I took liberty of assign you even though you weren't on the call.

Yves: I still have a few questions, need to read a bit more about the definition of session for non-secure cookies.  But I think really tying cookie to scheme used is a good thing.  Might break a few things, but worth it.  Dangerous to have cookie that's set in http and reused in https.  I still need to read the fine details, but it looks right to me.

Dan: Other people (TAG alums) who we should get opinions from on this?  e.g., mnot?

Yves: It will be discussed in IETF HTTPbis anyway.  I wonder if Mozilla or Apple has a position on it.

Tess: I don't think we have a public position yet.

David: Very cursorily I thought it seemed reasonable but possibly risky.  Didn't look in detail.

Dan: Bump a week, or to plenary?  Would be good to get input from Apple and Mozilla.

Yves: A week at minimum.  Positive but want to get more details.

#### Good example of process

Dan: There was an example of something I wanted to bring to people's attention, but now I can't find it... good example of Blink process.  Seemed to have venue, be going in good direction.  Provide positive reinforcement.

### Breakout B (US / APAC) - [2020-03-16](https://www.timeanddate.com/worldclock/converter.html?iso=20200316T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Alice (a bit late), David, Tess, Rossen (a bit later), Sangwhan (later)

Scribe: David

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

Alice: I was supposed to do something...

Tess: I've not yet read the updated explainer.

Alice: (makes reminder)

Bumping out 1 week

Alice: I had a chat with Matt.  I've been convinced for a while (though I think Tess disagrees) that tabs API and app API are significantly different and have different use case.  As such I think it would be nice if the tabs version of the API was more closely tied to the document (makes no sense on `navigator`).  Current design is a weird compromise based on lack of agreement whether they were different use cases or not.  I think we need to pick one, I would pick being different.  That's the comment I need to leave.

#### [WebXR Device API](https://github.com/w3ctag/design-reviews/issues/403) - @hober, @cynthia, @alice, @torgo

Tess: We marked this "pending external feedback" in December, and never got feedback.  So we're waiting on them?

David: do they know we are?

Alice: likely slipped off their radar

Tess: I'll [leave a comment -- poke the issue, say waiting on answers](https://github.com/w3ctag/design-reviews/issues/403#issuecomment-599799684).

Alice: Maybe bring to Dan's attention in the plenary?  I don't think anything a deal-breaker.  I still want to see evidence that accessibility is a core part of their design process rather than a to-do list item.

Tess: Agreed.

Tess: Set a new milestone?

Alice: 2 weeks?

#### [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon

Tess: Breakout in Cupertino looked at this.  As output from that, Yves filed 2 issues on their spec, which are both still open.  Marked ours as "pending external feedback" waiting for those to be closed.  But I haven't looked at this one at all.  (Not sure who else was in that breakout.)  I should look at the explainer.  Do we want to do anything in terms of the open issues?

Tess: Related to this spec monkeypatching the regular gamepad spec, which it shouldn't.  Looks like not any movement.

David: links to https://github.com/w3ctag/design-principles/issues/99

Tess: Nell's latest comment was a question to the TAG about what to do here -- Yves answered the specific question, I think it's a satisfactory answer.  Should we file an issue on design-principles to handle this case in general?  Should we do more?

David: I'm not wild about the registry idea; I guess a registry is better than partials, though.

Tess: A registry results in a central list, partials doesn't get you that. From a platform maintenance POV that's what we want. There are other problems with registries, but it's an improvement.

David: There is a question of whether it's a registry or a spec edit.

Tess: Yves is providing a specific answer for this specific problem, either answer would be fine. Any sufficiently small and bespoke registry is indistinguishable from spec editing.

David: It's whether it does/should go through a different process.

Tess: I'd probably prefer the spec editing process myself, but either works.

Tess: We should probably give some indication that this came up today and we're waiting on those issues to be resolved. [Left a comment](https://github.com/w3ctag/design-reviews/issues/430#issuecomment-599803022).

Tess: let's pick a new milestone

Alice: 3 weeks?

#### [WebXR Anchors Module](https://github.com/w3ctag/design-reviews/issues/479) - @hober, @alice, @torgo

(scribe missed a bit)

Tess: explains a bunch of the first three paragraphs of the [explainer](https://github.com/immersive-web/anchors/blob/master/explainer.md), and tries to explain it with different examples.

Rossen: commonly used in AR when you want to augment successfully and persist over time.  Naming of the concept is already overloading anchor in HTML.

Tess: I assume it's a term of art in XR.  Sort of a name clash for the Web.  That's part of the confusion.

David: feels a little like scroll anchoring

Tess: model anchoring

Tess: If they said that -- a method for anchoring XR models to the environment.  Started simple, then got more complicated, then it would be clearer.

Tess:  I'll look at these minutes and try to distill this into a comment on the design review.

Tess: Who are people writing explainers for?  We've talked about this a bunch.  I worry people write explainers for the TAG, and come to the TAG to check a box.  So they're not writing the explainer to be a useful living document, but instead this one-off thing to get a checkbox checked.

Alice: Do you think we can change this, or need to work with it?

Rossen: change what?

Alice: ... what Tess was referring to, that people write explainers as a one-off document for the TAG, rather than a living document for a general audience including for developers learning the API.  Do we need to live with that (I'm not happy to do, it's extra labor for us).  This is why I've been pushing back on this for the last year.  But if we need to accept that people are writing explainers for us, rather than writing for a more general audience, are we able to do something about this or not?

Rossen: I couldn't agree more.  People shouldn't abuse this review, and use this in lieu of standards work (as we discussed already).  I guess my point is that something that worked well for some of the previous engagements with API reviews is that we insistent that the equivalent of explainers (that we were using) were intended with the developer user in mind.  They were supposed to explain how the feature works, and give code examples that people could use to try it out.  Which is how most APIs are done on MSDN.  90% of docs on MSDN are these explainers translated into MSDN.  I'd love to see similar rigor here, where explainers would get converted into an MDN doc or into part of the spec that could be taken forward.

Alice: Agreed.  I've had this discussion with Joe Medley (tech writer on Chrome team).  We want this to feed onto MDN.  So we want it to be as close as possible to what that will end up as.  How do we get that to happen?  The explainer explainer tries to hint at that, but not very explicit.  We've tried to keep it brief; don't want people to have to read a whole essay on explainers.  Maybe we could tweak it a little. Similarly with issue template -- those are the contact points for people.  I think people are familiar with it.  I'm not sure what other contact points we have to influence that.  (Rossen asks clarifying question)  We have limited contact points with people coming to us for reviews -- where we can influence the process.  The explainer hints at that, but we also need to keep it brief.  If it's too long they'll skip straight to the template.

Rossen: Do we have good examples of explainers that have made it through the process and were used as MDN material.

Alice: Don't know offhand.  Maybe we should have a task to research that in a non-issue week.

Rossen: Might motivate people more if people knew their explainer would end up on MDN.  The way to incentivize people is to show them it's good for them.

Alice: Does point to underinvestment in communication work in the tech industry.  Maybe we can capture this as an issue on design reviews repo.  We could capture this as an issue to come back to in a non design review week.

(Alice volunteers Rossen to file the issue against the explainer explainer... and then decides Alice can file issue and assign Rossen and Sangwhan and Tess.)

(Side discussion about explainers that have separate versions in Google Docs and markdown, where the latter is out of date.)

(Alice files [the issue](https://github.com/w3ctag/w3ctag.github.io/issues/23).)

Tess will comment on this issue to give feedback on the audience for their explainer.

#### [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) - @cynthia, @dbaron

*Scribe*: Alice (with assistance)

Tess: I took a look at this earlier... not actually assigned to me but I took a look anyway. Maybe it could be a propose close? Sangwhan had one question, it's been answered, and David thought it looked fine. 

... I started looking into it a little bit... this is in the [Intent to Implement](https://groups.google.com/a/chromium.org/forum/m/#!msg/blink-dev/3oVuczJ5Ty4/b8VLNNvyEAAJ):

>  Safari: Negative signals (concerns over keeping it fingerprinting neutral)

... Should we take another look from the perspective of fingerprinting?

Sangwhan: I don't understand how this is another fingerprint. Either you'd be have (less than a handful of) silicon provided encoders or you'd have ffmpeg. The codec availability at most gives you as much entropy as knowing say, your phone model number which we happily dump on the UA string

Tess: I'm going to dig up the minutes from TPAC to find where the fingerprinting conversation happened, and what the specific concerns were, so we can follow up in our issue.

### Breakout C (APAC / Europe) - [2020-03-17](https://www.timeanddate.com/worldclock/converter.html?iso=20200317T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### [MediaStream Image Capture API (Pan/Tilt feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @kenchris

Alice: No explainer - but came in before that requirement

Ken: Pretty sure nothing has happened since (last comment). This is a powerful feature that can be abused.. It would be nice if they wrote an explainer...  Security & privacy questionnaire responses also not correct... it says "no" to everything...

Dan: on s&p, 3.2 (data) and you can use this to gain access to data that the user has not intended you to see... 3.4 (cross-origin-state) they have said no, but can you read the angle?

Ken: looks like you can read the angle...


#### [MathML Core](https://github.com/w3ctag/design-reviews/issues/438) - @alice, @torgo, @hadleybeeman

Dan: Brian has answered 7 days ago.

Alice: What Brian is saying the whole idea behind the core concept, if you are going to strip down mathml so that most of the stuff will work, then you end up with mathml core. Plus this is more consistent (CSS cascade etc).

... legacy compat things will still be parsed and worked correctly but implemented by deferring to other mathml core part or css.

... I might suggest a rewording so make it a bit more readable.

Dan: So we can close as satisfied? please work on your documentation

... This is a good response from Brian.

Alice: What is left for us to do might be looking over the spec once more.

Dan: Writing a response.


#### [Title Bar Customization for PWAs](https://github.com/w3ctag/design-reviews/issues/481) - @alice, @torgo, @kenchris, @plinss

Dan: Lets try to not creep the term PWA into specs, especially since some vendors do not like the term and because it is more a pattern than a formal term.

Ken: this is about the app getting control to draw the title bar - with trusted controls to mitigate against e.g. it mimicking your bank or some other trusted site...

Alice: I am no CSS expert, but I don't think adding classes is the right approach, why not a media query.

Dan: Adding my comment about the term PWA.

Alice: OK the class example, was in user code, sorry.


### Plenary Session - [2020-03-18](https://www.timeanddate.com/worldclock/converter.html?iso=20200318T210000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Kenneth, Alice, Peter, Rossen, Dan, David (5 min late), Tess (5 min late), Yves (15 min late)

Scribe: Alice

#### Readouts

Dan: Let's do readouts...

... **Breakout A**, **Feature Policy Control over Sandbox**

... Agreed to close, move to design principles.

... **CSS Modules**, needed more work so bumped.

... **More restrictive hasEnrolledInstrument()...** bumped and asked for update.

.. **HTML Horizontal Review**, Tess and (Dan) agreed to schedule something offline.

Alice: Could that happen in the regular breakout slot?

Dan: Maybe, we agreed we needed a special slot to look at this.

(Scheduling discussion ensues)

... **Title Bar customization for PWAs**.. moved to later breakout.

... **Protocol handler for PWAs**... why isn't this just registerProtocolHandler? Tess had an AI to check the explainer.

... **Scheming cookies**... Yves has positive comments, agreed to bump, will review next week.

... **Breakout B**

Tess: **Badging API**... Alice is going to write up a comment on that issue, bumped out one week, I'll read updated explainer.

... **WebXR device API**, looks like this might have fallen off their radar. This was marked pending feedback in December. Pushed it out two weeks, left a comment.

Alice: I wanted to bring up something with Dan on that one.  I asked about how accessibility was being addressed in their process.  (reads question asked)  I'd like to see that accessibility is being considered as part of core process and not just left to APA.  They should be working with them as much as possible.  I and Nell met with them.  They put out a [user requirements doc](https://www.w3.org/TR/2020/WD-xaur-20200213/).  But the core WebXR team should not be expecting accessibility work to be done by another group.

Dan: accessibility thing seems like a bigger kettle of fish, so do we need to keep this open?

Alice: Probably not, I don't think there were any major issues with the API other than the promise thing... though we did have a whole meeting about it so I expect it got fixed.

Dan: So I think we probably should close the issue, but say other feedback we left was really making sure you're taking accessibility seriously.  Maybe ask them to open a special review on WebXR accessibility topic.  Originally saying they shouldn't have a separate requirements document on accessibility... but maybe they should.

Alice: Was the APA that produced that document.

Dan: Oh, I thought there was work on accessibility requirements in XR.

Dan: Produced based on output of workshop in Seattle?

Alice: I checked the promise thing is updated in the explainer, though didn't check the spec.

Tess: Looked at **WebXR Gamepads Module**. Yves had been on a breakout on this in Cupertino, filed some issues, marked pending feedback.

... Compatibility of this with gamepad spec, there's some inconsistency. 

... Things getting redefined vs upstreaming. Currently monkeypatches the gamepad spec.

... Those issues are still open, haven't been addressed. Monkeypatching issue is still open. There's a question in there to us, basically looking for guidance about when do you write things monkeypatching-style vs. when to merge things upstream. If your spec is not mature but the monkeypatched spec is, probably want to wait until your spec is stable before upstreaming. Yves proposed a registry. We discussed trade-offs between registries and spec editing. Left a comment, bumped out three weeks. 

... Should file an issue on our design issues repo about monkeypatching.. we have a section on how to write good specifications. 

Dan: Is there a better term than "monkeypatching"?

Tess: Yes, we need to find a better term; the issue will probably use the term but note that we need to find a more neutral term.

... e.g. "which is sometimes called 'monkeypatching'" - people search for that term

... WebXR Anchors module. Got a bit off-topic on this, the explainer expected a lot of context that we didn't have, so we started talking about how to help folks write good explainers.

... Alice filed an [issue](https://github.com/w3ctag/w3ctag.github.io/issues/23) to track how we can improve this situation. So we didn't really get back to the WebXR Anchors issue.

Rossen: Want to ideally have explainers that could end up on MDN.

... Technical discussion, we found "anchor" super confusing, it's an overloaded term on the web. 

Tess: It's probably the standard term of art in XR, unfortunately clashing with a standard term on the web. Since they're an "amphibious" spec, we need to figure out how to resolve this.

.. Will file an issue on their explainer to ask.

... **WebCodecs**... this is a propose close. There were some concerns about fingerprinting, we hadn't asked them about that. I took an action to dig up the relevant minutes to find out what the concern is so we can ask about it productively.

Dan: **Breakout C**.. 

... **MediaStream Image Capture API** 

Ken: Took another look at this... still waiting on explainer.

Dan: They're going to get back to us in a few weeks...

... **MathML Core**.

Alice: Hadley had asked to what extent MathML core follows platform.  "The legacy situation may leave" ...

... I had a chat with Brian offline about that.  He said it will all follow the platform; that's the point of the work being done.  I suggested clarifying in spec, and he has.

...He added paragraph beginning with "MathML Core aims to always follow the platform".  Explains analogy of border being implemented always using CSS once CSS became widely adopted.  I'll follow up with him about improving the explanation.

... I suggested that now that explainer gives enough context for us, we should actually have a look at the spec itself and make sure we don't see issues there.  But it seems this work is going well.

... Sangwhan and I should look at explainer.

... I asked specifically about `mrow` as something ... Sangwhan pointed out that it looks like a layout directive, but used as a non-semantic group directive.  Wondering if something could be done around that.

... They answered around legacy compat.  We need to check in the spec.  Are things that are legacy compat marked as deprecated in the spec?  We need to check.

... Wrote comment thanking them for work, we'll take a look at the spec.

Dan: **Title Bar Customization for PWAs**..

.. Little concerned that this is PWA specific, got a few thumbs up on that. Ken left some comments, I left some comments, we'll revisit next week.

.. This is about customizing what's *in* the title bar for a full window web app is in a windowing system. Very system to desktop chromeless web-apps.

Kenneth: Like samsung DEX..

Dan: android webapps on desktop ...

Alice: Or like Electron?

Dan: Could be relevant to Electron apps.

... As written very specific to Microsoft.

Kenneth: A lot of the experiences, especially microsoft experience, e.g. microsoft tunes, puts a search field inside the title bar. In order to become PWAs instead of Electron apps they need this feature. Also things like Spotify.

Rossen: This is not specific to this, I had the same discussion with Marcos recently. I urge you to do a little more reading in the explainer ... when I worked with the team internally, I don't want anything to be tied into any particular OS experience. Using the same primitives you can allow the iOS "notch"... this is described with a CSS environment variable

Tess: safe area inset (?)

Rossen: This is "how far down is the safe area"... this feature is building off that. Adding "Inside the inset, you have something that starts here and ends here"... whether this is called the title bar or the area around/next to the "notch" is not that important... explainer started with title bar, but it's not exclusive to that in practice. As they considered more platforms where PWAs need to be successful, they realised the naming is less than perfect.

Alice: Could you leave that feedback?

Rossen: Sure. I can also go into a lot more technical details on this spec if needed.

Dan: Two new issues for triaging.

[PWA Change logs](https://github.com/w3ctag/design-reviews/issues/484) and [Layout Instability Shifted Element Surfacing](https://github.com/w3ctag/design-reviews/issues/485)

Alice: Also [Imperative Shadow DOM Distribution API. #486](https://github.com/w3ctag/design-reviews/issues/486)

Dan: Let's come back to PWA Change logs.

... **Layout Instability Shifted Element Surfacing**... does anybody know about this?

Rossen: I don't know the details but I'd like to be involved.

Explainer ... needs some work.

David: It also lists "W3C" as the intended group for work...

Dan: Leaving a comment asking for more detail in the explainer.

Alice: **Shadow DOM Distribution API**

Ken: May be discussed at the Web Components meeting next week.

Tess: I'm chairing that meeting, I can make sure it is.

Rossen: This one has an explainer so that's a good start.

Dan: Milestone? Week after next?

David: Is this w3c or WHATWG?

Tess: It's complicated.

Dan: Pete Synder from Brave reached out to me in relation to how PING could play a stronger role in the TAG review design process. A call for us to more clearly label design reviews where there's a privacy issue... we did that.

... As long as we start using that approach, if people are happy with that approach, PING can put that into their work process.

... Also discussed Pete's perception... he's channeling others as well... concern that some people think that fewer things are getting wide review as we move forward. Some people mistakenly view TAG review as wide review. TAG review should be a trigger for wide review, rather than considered wide review

... Got me thinking that it's the same topic we talked about in NZ. I don't know ... things in WICG need a trajectory, and that requires wide review. More people want to see TAG playing that role of encouraging wider review of specs.

[some discussion on WICG and how TAG could help WICG out...]

[let's have a call with WICG people]

Alice: Another related topic: TAG could help to review the Blink standards process.  

Dan: could someone file that?

Rossen: I can file that...

### AOB

One quick thank you, and apologies for failing to do a squash merge yesterday.

Tess: I had fun.

Rossen: I was embarrassed, I had to go fix it.

David: I've [adjusted](https://github.com/organizations/w3ctag/settings/audit-log) some of the settings on our Repos to change this. This is a per-repository configuration. I haven't changed the setting on all of our many repositories. Also I did slightly different things in different Repos.

Rossen: Thanks for removing Merge With Commits as an option.

David: rebase is still an option, I think squash is the default.

... Also set up branch protection rules... require administrators to go through the branch protection rules. Ticked the require linear history box. Setting up those rules is a little bit obscure but it's not too bad.

Rossen: Apologies again, especially to Tess.



