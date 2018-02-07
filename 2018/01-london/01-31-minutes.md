## TAG F2F - London
##### 31 Jan 2018

Present: Dan, Peter, David, Andrew, Alex, Lukasz, Travis, Hadley, Yves (remote), Sangwhan (remote)

Regrets: Tim

---

Agenda topics:
* special election update (Wed AM)
* [Design review issues](https://github.com/w3ctag/design-reviews/issues) (49 open issues) (Wed AM)
* [Privacy and security checklist](https://www.w3.org/TR/security-privacy-questionnaire/) (Thu PM?)
* Lukasz intro to the TAG
* Remote web objects
* Fake news (Thu PM?; not Friday)
* [Whatwg working mode/structure/IPR](https://blog.whatwg.org/working-mode-changes)
* EU GDPR/ePrivacy Regulation and browsers (Thu PM?)
* [CSS Typed OM](https://github.com/w3ctag/design-reviews/issues/223)
* [Accept-CH](https://github.com/w3ctag/design-reviews/issues/206)
* [Web Audio](https://github.com/w3ctag/design-reviews/issues/212)
* Web Components "tipping point"
* next meeting, etc.
* [with credentials](https://github.com/w3ctag/design-reviews/issues/76)
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201)
---

Scribes:
 * Wed AM: Travis
 * Wed PM: Andrew
 * Thu AM: David
 * Thu PM: Alex
 * Fri AM: Hadley
 * Fri PM: ?

### Morning Session - Dan chairing

### Special Election Update

Yves: special TAG election announcement will be very soon now...

...Election will be a 2 year term, and go through Jan 31 2020.

...Nomination will start right after the Process 2018 announcement.

Lucasz: Good! I'm aware that TAG has expanded the scope of their work during the last few years. Will be handy. 

Dan: When the announcement goes out, Dan will blog about it.

### Un-assigned issue Triage

[unassigned issues](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+no%3Aassignee+sort%3Acreated-asc)

#### [Dusting Off Web Speech API (#214)](https://github.com/w3ctag/design-reviews/issues/214)

Travis: I raiseed issue. Happy to be assigned.

Alex: Nigel makes a good comment about having Web Audio + Speech. The folks at Google who drove this forward have since [probably] moved on.

Peter: There's also a CSS Speech Module (for output). Untouched in years!

Hadley: Use cases? Reviews the [ones listed](https://w3c.github.io/speech-api/webspeechapi.html#use_cases).

Alex: "Hot wording" (e.g., Alexa/OK Google). This is offloading to special processing.

Dan: Is there any group currently working on this? What would the outcome be? (Should we ask for a Working Group to be chartered for this?)

[could we do a blog post? A wicg post?]

Alex: Might be worth reaching out to implementors to see who might be ramping up on this.

* [behind a flag in Firefox](https://hacks.mozilla.org/2016/01/firefox-and-the-web-speech-api/)

Hadley: wondering if tipping off Wendy might help to get something started in WICG?

Travis: Will follow-up with figuring out what the outcome is about this.

#### [Media Capabilities (#218)](https://github.com/w3ctag/design-reviews/issues/218)

(sangwhan volunteers)

#### [CSS Selectors 4 (#219)](https://github.com/w3ctag/design-reviews/issues/219)

[Discussion on at what stage this work is in and whether a TAG review is appropriate at this stage]

[Issue assigned to David Baron]

Alex: notes there is no explainer!

Dan: Yes, we should ask for that...

Alex: We'd like to know the use cases around the newly added stuff.

#### [(text only) Async Clipboard API (#222)](https://github.com/w3ctag/design-reviews/issues/222) 

[assigned Alex & Travis]

Dan: Shall we revisit this week?

All: yes!

#### [CSS Typed OM (#223)](https://github.com/w3ctag/design-reviews/issues/223)

David: I've been reviewing over the last week--it's a bit of a large spec. (I'll assign myself). A few interesting bits:

(Background: This is a new version of the CSS OM)

Alex: where is the explainer?(tm)

David: Much of my feedback was about the vagueness of the spec (hey, two implementors may not read this the same way.)

Issue 564 of that repo is interesting--that have range-restricted properties (that result in parse error). Typed OM is trying to take the more 'lax' approach.

E.g., in Gecko, properties that serialize and then are re-parsed should be round-trippable. This may introduce complications given the way the spec is going...

Tab is in Syndey this week to work on issues; if we can get issues filed today, then that would be much more actionable.

Suggest: Extra time for this issue after lunch.

#### [CSS Layout API (#224)](https://github.com/w3ctag/design-reviews/issues/224)

Alex: Houdini API for custom layout modes. Traditionally there ahave been a fixed set of modes - hasn't been possible to add your own layout mode. This is about creating efficient hooks for doing custom layout.

David: spec in flux. Allows a subset of what is possible with layout (constrained to block level-layout).

Peter: previously missed the ability to handle floats.
 
David: Traditional hard part is what parts of the layout happen by the parent and hwich happen by the child. This API might be constraining that which codifies how this might work--will be tricky to get interoperable implementations.

Alex: Sechedule for a future call? Feb 13th?

#### [Permission Delegation (#225)](https://github.com/w3ctag/design-reviews/issues/225)

Lukasz: delegates permission to iframes but it needs to be included in the iframe

LAlex: there's an attribute

Lukasz: if you delegate to a 3rd party there is transitivity.  iFrame can delegate this permission further.  The origin is losing control. It will need to trust iframe not to delegate it further. Potentially this might escalate.  This needs to be clearified in the specification and include some directive if transitivity is possible. Or oppose this idea. I oppose it. Architectural risk.

Lukasz: May also just oppose it. Wondering if Developers might always use the transitivity feature.

Dan: Can we ask Raymes?

Alex: And ask if the specific question is a weight/limit delegation further?

Dan: The question is: can I delegate permissions but not allow them to be delegated further.

David: So what happens as a result?  Often the alternative to delegating permissions to an iframe is including js code in your origin from some other origin. It's basically a security loss. if you're a mapping site and a business wants to have an iframe with a map in it, and it has delegated geoloation to you so you can make a map for the user — if you need to delegate that permission for some reason and you can't, the workaround will be to do it through included JS. Which is worse. 

Lukasz: That's often the case. But this proposal sanctions this kind of approach. While it has merits, we should look at the potential problems. For the clarification, whether there will be any options to limit the delegation — we should ask.

Alex: agreed.

Travis: Similar pattern with document.domain, where you want the origin to be included in another origin but isn't hte same. The paralell is that both sides need to agree; one side asserting it isn't sufficient. So in this model, maybe both the parent and the child must agree?

Alex: If it's a bad actor, the child will greedily accept and and all permissions.
...Similar: We see a cause for a limit to the number of frames you can nest. iFrame depth. 

Alex: In Chrome's treatment, there's an independent permission for the iframe (separate than the parent). The permission is to ask for delegation (not for the specific thing delegated). There's generally a "permission to ask" which can be locked down for certain HTTP pages (they may not be allowed to ask by default).

Peter: if user is browsing example.com and they embed google maps and permission is granted. If user goes to another site that also embeds google maps then is permission already granted?

Lukasz: (hopes not)

David: my understanding (though not sure) was tied just to top level origin

Dan: Lukasz, please copy some of your notes/thoughts into the issue.

Lukasz: https://github.com/w3ctag/design-reviews/issues/225#issuecomment-361900867

#### [Picture-in-Picture (PiP) (#226)](https://github.com/w3ctag/design-reviews/issues/226)

Alex: do we know/ what is the reason why this isn't available for general web content?

?: Use cases: video playing on mobile

David: Also use cases of video chat apps or google maps navigation doing that on Android.

Travis: Seems a lot like allow-fullscreen (but not quite fullscreen)

Alex: Why is it video-only rather than general web content?

David: might be a phishing/security UI concern?

Sangwhan: maybe could also be a canvas API?

Travis: Might also be similar to media control playback (e.g., let the OS host your video content)

Sangwhan: Also whether controls should be shown.

Lukasz: wondering about creative ways of misusing ;)

## Coffee Break

#### [internationalization of natural language in json strings (#178)](https://github.com/w3ctag/design-reviews/issues/178)

Timeboxed to 12pm; Lunch at 12:00

David: new information - sangwhan & i should read it...

#### [ttml](https://github.com/w3ctag/design-reviews/issues/138)

Peter: there was a meeting at tpac [that went well]. ttml meeting with css folks in the room.

Alex: outcomes?

David: ended with a reasonably coherent outcome, I think, but don't recall entirely.

Hadley: found [it!](https://www.w3.org/2017/11/09-tt-minutes.html#item35) (Continue through to "Break for Lunch")

#### [webvr](https://github.com/w3ctag/design-reviews/issues/185)

Travis : is there much left to do here? The feedback has been received by the group.

Dan: notable that they've rebadged the group as webxr.

Alex: most substantive changes are to change in design for RAF as it correlates to vr devices. ...

... hopefully they will come back to another proposal.

Hadley: were RAF changes what we wanted?

Alex: In the direction of what we wanted.  They have aligned the style of API - for VR objects and main document RAF.

Travis: they wanted a way to extend it to specific cases.

Alex: related concern around FPS of different subdocuments...  They have built a set of APIs that work at that higher framerate. Unclear how APIs like offscreen canvas will work with that.   So closer and hopeful.

[discussion on gamepad]

Sangwhan: Sony and google people are looking at it. (within Web Platform.)

Dan: Can we suggest that WebXR folks work with gamepad folks rather than duplicating effort?

Travis: I don't think it's in conflict, but gamepad is getting restarted.

Dan: my team is working with gamepad api

[discussion about quality of the API]

Dan: We run into this assuption that everyone using VR has an amazing console with extensive controllers. I think we're designing for simple equipement too — a phone and a cardboard headset.

Travis:  I think the vision of great VR experience includes controllers. They don't want to invent all that, but they watn to include the possibilities. I've told them to make the most of existing work.  re gamepad, they have discussed in v1 how to extend the existing gamepad to get some of these controller functions. then re the gamepad API not being great for ecxtending: is there something better to be done?  Is it just VR specific, or general purpose?  Open question.
...I agree that these inputs should not be VR specific.

dan: We did some work with BBC late last year on a [WebVR game](https://vrscout.com/news/doctor-vr-game-pilot-tardis/), the whole point of which is to make sure it could be used on as many handsets and things as possible.  That didn't take advantage of a game controller.  Ideally if you were doing that, you'd want to take advantage of existing ones as well as more sophisticated options. See also [case study](https://www.goodboydigital.com/case-study/doctor-who-time-vortex-360o) published by the developer.

Travis: To use a gamepad on the web requires mapping to mouse events.

Sangwhan: I don't think it's bad that gamepad API is being reinvented like touch events vs pointer events. The only way to do it right is to start over 

Lukasz: I think this would deliver a lot of info about the user.  

Hadley: fingerprinting?

Lukasz: Yes plus — you can get inter-pupilar distance, between the eyes, if I remember correctly from an older spec. There will be some biometric information. Possibly also behavioural mapping.  Less worries on fingerprinting at the moment. 

Travis: I'm putting a comment in the webVR issue. 
1. Framerate per RAF, offscreen canvas 
2. input and how it relates to gamepad
3. Decorating an iFrame as high-performance content

Dan: I get frustrated that some spec authors don't realilse that there are impelmentations already of v1.1.  This BBC Dr Who example is a good one.  It has gaps, sure — but it's in use. There is enormous appetite for using this stuff.

Travis: The group has been focused on the next generation.

Dan: Exactly. When HTML shipped it didn't have images.

...Milestone of 20 Feb to see what feedback we get. 

## Lunch Break

## Afternoon session - Peter chairing

### Lukasz intro

Lukasz: hi!  

### Meet the TAG 

Lukasz: What is Meet the TAG?

Dan: TAG was accused of not being open, understandable or relevant to 'real' developers.  In 2013 we started to do dev meetups.  Sometimes we do panel. Questions.  Open discussion.  Sometimes longer event, breakouts.  Occasionally half or full day unconf.

https://ti.to/w3c-tag/meet-the-tag-london

L: how many coming?

D: 30ish?  Have had max 100 at previous events.  Min 1.  Pub.

L: Any spaces left?

D: Yes but with some special action needed because it is too late for general registration.

### [Remote web objects](https://github.com/plinss/remote-web-objects)

Peter: I introduced this.  Homepage for HTTP API endpoints. Instead of adding new JS APIs in browsers, we can advertise HTTP APIs and express them in JS land.

Andrew: So WDSL?

Peter: But... good.  You can bind functions to endpoints, include state information to modify objects and return derivative information.  Also event bindings, becomes eventTarget.

Andrew: Sounds magic

Peter: Yes it's all magic.  I'm using it in production.  I have a polyfill.  Originates NextStep.

Hadley: Anyone else working on this?

Peter: No, just me and you folks have now seen it.

Andrew: would like to see examples of the JS code interacting with an example defined API.

Alex: params coercion?

Peter: Everything is JSON encoded.  URL params templates.  Anything not in the URL template is a PUT or POST payload.

Travis: How to bootstrap it?

Peter: window.fetchRemoteObject

Andrew: Why a loader rather than a new type of script tag. We have scriptType module; why not scriptType remoteObject?

Peter: You're getting back an instance.

Andrew: So you get back a reference to an object that you need to assing somewhere?

Peter: Yes. This isn't sending you JS code. All implementations are at the server and marshalled over HTTP.

Travis: JSON-LD?

Alex: Does schema.org data

David: patch mechanism?

Peter: allows the server to patch the object that called the server method

David: network errors?  Server might not know if the object got patched?

Peter: throws on network errors

Travis: serviceworker?

Peter: SW could be the 'server' side of the implementation

Andrew: in the automotive example, if you didn't want to create a server. Currently the JS would need to connect out through the browser/run time through to the various objects in the car — there currently isn't a network protocol for that. Would you see this being a sw-powered thing that pretends to enable this?

Peter: yes, that's possible.

Alex: proxies?

Travis: WebIDL generator in the browser

Peter: I built this on top of the JSON home work that Mark Nottingham has done

Andrew: goal?

Peter: Is this a good idea?

Alex: Seen Comlink (by Surma) library? (No)

Peter: I haven't done anything about serialising objects once queried?

Travis: I can't just feed you JSON and have you construct objects?

Peter: No, it has to be HTTP.  This doesn't provide any functionality

Andrew: Do we know enough about this to say whether it's a good idea?

<Consensus is it's a good idea>

### WHATWG working mode

David: As of mid Dec 2017 WHATWG now has a steering group.  Overlap with TAG and AB.  Has patent policy, IPR commitments.  Patent policy is around snapshots instead of recommendations, in line with the living standards. 

Dan: Is there a policy for exclusions? Or potential abuses of the patent policy?

Travis: There's a period of time around the publication of the snapshot when things can be pulled out / redacted

David: We can build new policies.  I don't think there's a definition of Patent Advisory Groups.  It has similar concepts to 'last call CR'.  MSFT is participating.

Dan: I think patent [exclusions] are going to come up

Travis: it's designed to be low impact, in line with their original work mode.

Sangwhan: How do you call calls for exceptions/exclusions for living stuff?

David: snapshots

Hadley: How does this work in practice? If living specs are supposed to be implementable ASAP and snapshots are around every six months...

Travis: even in W3C many things are built and shipped before CR or rec.

David: Hopefully in 6 months you haven't shipped in all browsers

Andrew: goal?

Travis: We are a review body used by WHATWG and W3C

David: It doesn't change the relationship

### Web components tipping point

Travis: Is this an opportunity to do a blog post?  My view is still 'not yet'.  What is there to say other than "the tag recommends that you consider web components".  Do using web components change your initial model of how to architect the app.

Peter: Yes, I build a page, not an app, and then I build components that fill in the missing pieces.

Travis: There's no app platform for the web

Peter: That might be something that's missing.  But web is designed for docs.  Over time we need to add more parts to the platform that are more about modelling apps.

Dan: I don't think we should say anything, not our responsibility

Alex: There's a hoped for future where we can see web components.  We'll use that as a way to collect evidence on use cases and guide future development.

Sangwhan: We should only say something when WC replaces something that already exists

Alex: There are areas of the platform that are hostile to WC, forms.

Peter: No lore in the ether about how best to use web components.  People make up random things.  Cargo culting older patterns.  Not necessarily giving us anything new.  May not hurt for us to have a document saying this is how you leverage this technology.

Andrew: Isn't that basically a tutorial?

Peter: Yes

Andrew: Great idea, not a TAG thing.

Travis: I was asked to do a WC demo a year ago.  I struggled to find a good use case.

Alex: Everyone wants a component system.  WCs are maybe not the best one, but they're in the platform.  Good for upgrades in frameworks.

Travis: Those companies maintain large sites where reuse is a major thing

Alex: Yes. Also lots of legacy systems, desire for common design system.

Dan: suggestion: I create an issue in design principles repo: do we need a WCs document?  We can get community feedback.  What should be in it?

Alex: Jan Miksovsky has written a thing that has been very useful for our teams. (The [Gold Standard Checklist for Web Components](https://github.com/webcomponents/gold-standard/wiki))

### Next meeting

David: Room is confirmed

Sangwhan: We have the room for 3 days.  Room comes with projector and big screen.  Mita campus.

Dan: (concerns about toilets)

### Future meetings

David: We have tentative Boston in July, no location

Peter: After that would be TPAC

Alex: week of 23rd?

Dan: I will email Amy (about Tim's availability)

Travis: come to Seattle!

Hadley: before TPAC.  1-3 October in Seattle then?

Sangwhan: I'd prefer London to Boston. (But Seattle is fine too.)

## Coffee Break

### [Clear-Site-Data (#62)](https://github.com/w3ctag/design-reviews/issues/62)

Andrew: \[summarizes\] Basically we need to poke this...
... this has shipped in Chromium - not in other engines.
... all the questions still need answers.
... we need to re-ping.
... my concerns are around the syntax (double quoted strings), interaction with set-data headers (set-cookie etc) and lack of explainer.

Alex: figuring out who the implementer is... Will try to raise...

### [Task Scheduling (#72)](https://github.com/w3ctag/design-reviews/issues/72)

Alex: there are a lot of things that are ordered and serialised.  Some are not specified well.  Eg when are mutationobservers, promises etc delivered?

David: If you flush layout and style, when do these things happen? etc. This was an effort to write a better spec, it hasn't gone anywhere really.

Travis: I'd like to make progress on it, but...

David: Postpone to next F2F.

### [With Credentials](https://github.com/w3ctag/design-reviews/issues/76)

David: I'm still dealing with feedback on the statement of the problem that I wrote, and an attempt to describe the proposals that have been discussed.  Yves has some substantive comments on this which I need to process.

David: Tim is concerned about a case where he has creds for a foreign origin, and wants them to be used.

Yves: Tim is concerned about having to know if creds are needed or not in advance.

### [Streams General]

Moving to extra time and will schedule for discussion on Friday.
(Sangwhan: Happy to join as long as it is before 16:00 London time)

### [Privacy Mode](https://github.com/w3ctag/design-reviews/issues/101)

L: Probably a good idea to have a common framework and common guarantees - but impossible describe every possible way a browser wants to provide privacy guarantees.  Is there anything already?

Hadley: we're trying to work out if there is a problem, and if so, where?

Dan: In 2016, mnot opened the issue.  Hadley's been working on it.

Lukasz: So you're potentially going to publish something?  What do you need?

Dan: consensus!

Andrew: Were we going to do some work to compare different browsers definitions of privacy mode?

Hadley: Yes!  https://docs.google.com/spreadsheets/d/10kulKoA6b_EWXDjzlg2DXS2vKL1NbW0NvPbcnWo5v0s/edit?usp=sheets_home&ths=true

Hadley: We don't have power to tell browsers what to do.  We can make recommendations, do work as individuals.

Dan: we can blog.

Andrew: Is there a summary of the differences?

Hadley: No, but there's a summary of the threat models.  I feel that users are confused by the different options.

Lukasz: document would be for implementors or users?

Hadley: Both.  Impleentors could make things clearer.

Dan: Also other specs make reference to private mode.

Andrew: options:

1. do nothing (privacy mode remains without definition)
2. some guidance issued in a casual form (blog post, note, finding eg) that makes some important point
3. there is a standard that defines what privacy mode is

Hadley: eliminate option 3, competition is good, there's not enough value in defining (comprehensively) what privacy mode is.

Lukasz: an idea - some standards reference privacy mode but no w3c docs define this - maybe we issue a finding - that we are a variety of features. 

dka: it may be useful to give clarity to spec authors that they can reference privacy modes. We know there are differences, but they should think about how their feature should behave in such a mode. 

Lukasz: OK. So if we aren't sure which options are the best maybe let's go for issuing findings? Wins: (1) W3C-issued document that can be referenced, (2) acknowledge that there are now two modes of web browsing, (3) not going into implementation difference, and actually even note this in Findings, (3)  etc.

### [TV Specific Web Subsetting](https://github.com/w3ctag/design-reviews/issues/105)

Dan: There's some new stuff percolating through HBBTV that I haven't gotten up to date with.  I'll follow up on this.

### [Web USB](https://github.com/w3ctag/design-reviews/issues/108)

Alex: CORS and permissions were the last things discussed here.

--reviews status--

Alex: OK, I'm happy.

**Resolution:** Close issue

### [Review Accessibility Object Model](https://github.com/w3ctag/design-reviews/issues/134)

--> extra time

### [Spec/Style Checklist](https://github.com/w3ctag/design-reviews/issues/136)

Pushed the explainer explainer to https://github.com/WICG/starter-kit/pull/10 and closed the issue.

### [TTML](https://github.com/w3ctag/design-reviews/issues/138)

waiting feedback.

### [OffScreen Canvas](https://github.com/w3ctag/design-reviews/issues/141)

Pending external feedback.  we discussed and looked like minimal value we can add at this point. We'll continue to monitor and come back to it on 2-20.

### [WebRTC Stats](https://github.com/w3ctag/design-reviews/issues/148)

Comment from Anne about secure contexts, but stats seems to be just dictionaries.  We're opening a new issue and will close the review.

### [WebPayment Method Manifest](https://github.com/w3ctag/design-reviews/issues/162)

Closing the review, noting some unresolved concerns.

### [Input Events Level 2](https://github.com/w3ctag/design-reviews/issues/173)

Travis to write up.

### [HTML General](https://github.com/w3ctag/design-reviews/issues/174)

Situation with `<main>`.

Discussion of the value of setting rules on limits on number of elements.

Andrew: I don't think we can realistically attack this from top down.

Travis: thinking about how we will split things up at MS, which may be relevant.

[ will continue discussion tomorrow when we have Sangwhan ]

### [Serialization of National Language in JSON](https://github.com/w3ctag/design-reviews/issues/178)

Return to this tomorrow.

### [Image Decode](https://github.com/w3ctag/design-reviews/issues/182)

(Sangwhan: I can volunteer to get this ball rolling again)

Andrew: i have thoughts

\[agreed to discuss tomorrow\]

### [Review of signature-based resource loading restrictions](https://github.com/w3ctag/design-reviews/issues/186)

\[discussion\]

Travis: "i don't have to trust the content explicitly"... 

Peter: the consumer is putting the trust in the public key of the publisher... 

Andrew: anyone who has the ability to create something signed with this key, I trust

Peter: instead of the consumer specifying a hash... the consumer says whatever you get has to have a signature and that needs to be verified against the content and a public key.  there is a signature algorithm. 

Travis: web author includes the public key.

Peter: the server sends the signature (in a header) and the content... the public key is included instead of a hash...

Andrew: I was concerned about the practical incentives.. that this gives to CDNs..  Theoretical purity argument going on here that publishers need to do their own signing..  

Peter: the whole point here is to not trust the CDN...

Hadley: Isn't this just a fundamental difference in viewing hte role of the CDN? Either the CDN is a trusted agent you can delegate key management to, or the CDN is on your list of adversaries. If we don't agree on that, how do we go forward?

Andrew: I'm not sure it will work out the way they expect. But I won't stop it; I think it is a good thing.

Peter: I'm concerned about making sure you can use multiple signature headers. I'm not sure this spec allows that

Andrew: The header won't allow it, but you could have multiple headers.

Peter: I have filed the question.
...Alos I'm concerned about using bare public keys. You have to distribute the public key out of band... how do you validate that you got the right public key?  Potential for fraud. You relaly want certificates there, not just a bare public key.  
...Mike's response: next version.  I'm concerned it might not last long without being broken; maybe we should add that extra level of complexity now. 

Andrew: Posted an update on our remaining concerns to the github issue.

**END OF DAY ONE**

**THE TAG WILL RETURN IN "DAY TWO"**















