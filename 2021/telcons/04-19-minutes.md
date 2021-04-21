# TAG Teleconferences week-of 19 April 2021

## Call Agendas


### Breakout A (Europe / US) - [2021-04-19](https://www.timeanddate.com/worldclock/converter.html?iso=20210419T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou, @kenchris
* [WebXR Plane Detection Module](https://github.com/w3ctag/design-reviews/issues/620) - @torgo, @atanassov
* [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549) - @hober, @ylafon

### Breakout B (US / APAC) - [2021-04-20](https://www.timeanddate.com/worldclock/converter.html?iso=20210420T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [ARIA in HTML review](https://github.com/w3ctag/design-reviews/issues/614) - @hober, @atanassov
* [CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @LeaVerou
* [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou
* [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @plinss

### Breakout C (APAC / Europe) - [2021-04-20](https://www.timeanddate.com/worldclock/converter.html?iso=20210420T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris

### Plenary Session - [2021-04-21](https://www.timeanddate.com/worldclock/converter.html?iso=20210421T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

## Minutes

### Breakout A (Europe / US) 

Present: Amy, Dan, Peter, Lea, Tess, Hadley,

Regrets: Kenneth, Yves

#### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou, @kenchris

Lea: my primary concern is it might be too low level. All the use cases are about an app resonding to high CPU load. What constitutes high CPU? Two kinds: utilisaiton threshold and clock speed and they need to provide thresholds for both. This would make more sense as an observer for.. there's high load right now, or no high load any more. All the use cases they listed don't depend on specific thresholds, but on apps lowering use of resources when there's high load. Tying it to hardware makes it less futureproof. I'd like someone else to review security and privacy if they stay with this current design. Because they aggregate these numbers across all CPUs they're not exposing sensitive information, but would be good if someone else could review the questionnaire responses. Minor feedback - using an observer but the method to start observing is not called observe, but start, so should be harmonized with other observers.

Dan: [reviewing S&P questionnaire responses]

Peter: the test modes seems kind of weird. And GPU as well? Would that be part of this?

Lea: I had mixed thoughts about the test mode. It's good they thought of debugging, but it is kind of weird and not consistent with anything else.

Peter: I have no problem with debug mode, but weird as part of API surface, maybe a browser switch or something.

Dan: current spec is too specific? A binary switch of high cpu or not high cpu, or is the proposal to have more granular?

Lea: I worry it's too granular and too hardware specific, but I might be wrong.

Peter: agree that a simple high usage mode or throttled would be better than the number they're exposing now. Felt odd. Pinning base CPU to 0.5 and max to 1 seemed weird. You're going to have a different range between 0 and .5 as you are between .5 and 1. They talk about linearizing it but I don't think the math works out.

Dan: for keeping it simple, having it be one single thing makes more sense and then we'll see if developers take advantage of that, vs building a whole complex thing and it turns out it doesn't get much use.

Lea: sounds like we're in agreement, I could leave a comment.


**Proposed comment:**

We reviewed this during a breakout today. Since all use cases listed relate to web applications responding to high load, we are wondering if a simpler, less granular, more high level API would address these use cases equally well, without the added complexity of specific thresholds, different for CPU utilization and CPU speed. See [Prefer Simple Solutions](https://w3ctag.github.io/design-principles/#simplicity).

If not, it would be good to show use-cases where this is not the case. We assume the reason might be to know well ahead whether you are about to get throttled and it is less interesting knowing when you are being throttled. Is that correct?

We understand that all speeds are being rescaled to a percentages, instead of revealing actual top speeds etc which really helps with privacy, so we welcome that.

In terms of the proposed API, please note that all other observers on the Web Platform today use `observer.observe()` instead of `observer.start()`. Also, while it's good that debugging use cases were considered, we think that a test mode would be more appropriate as a browser dev tools switch instead of part of the API surface. 

The spec has to handle heterogenous computing where the CPU has different kinds of cores (ARM BIG.little, Intel Alder Lake). The software/hardware scheduler can move workloads (such as browser process) to another core with different characteristics, like you might be about to max out the little cores, then you are moved to another core with plenty of performance budget left. This may lead to confusing numbers when it is expressed as a single scalar.

#### [WebXR Plane Detection Module](https://github.com/w3ctag/design-reviews/issues/620) - @torgo, @atanassov

Dan: Proposed feedback...

`Hi! I'm just having a look at the ex-*plane*r and coming up with a few questions. First of all, I think it could go into a bit more detail on the user need.  Can you give a few examples of where plane detection becomes important in the context of a WebXR application?   The answers to the security & privacy questionnaire look good but do not seem to be fully reflected in the explainer of the spec itself? For example, the quantization of planes is mentioned as a mitigation strategy against privacy attacks in the questionnaire response but this is not mentioned in the spec itself. I think this would be a lot stronger (and less prone to fingerprinting) if the quantization and other mitigation strategies were spelled out in the spec. Finally, you mention synchronous hit-test but it's not clear from the explainer how this fits together with the [hit testing](https://immersive-web.github.io/hit-test/) specification itself? What does this technology provide over and above what WebXR hit testing?  We may also have feedback on the API to share - but I wanted to get this out to you quickly.`

Dan: [posts comment](https://github.com/w3ctag/design-reviews/issues/620#issuecomment-822615550)

#### [Client Hint Reliability mechanisms](https://github.com/w3ctag/design-reviews/issues/549) - @hober, @ylafon

Tess: this is a network protocol level optimisation of client hints, under the assumption client hints is a thing and works as it was designed. Say a client requests a website for the first time, send a GET request, with no client hints becuase you don't know what the server wants yet. In the 200 reply it can say here are the client hints I'm interested in. Right now if a browser spports client hints it might retry and send client hints for maybe a better website. So it tries again and gets a different result. But that roundtrip sucks performance wise so they were trying to figure out how to optimise that away most of the time. Combation of TSL level change and HTTP/2 and 3 level change that accomplish that. New Header called critical-ch that say which client hints would result in very different responses. Mechanism to expose than in the initial TLS handshake. When client first connects to server it can say it wants an ecrypted connection the server says right aware here are client hints, before the first HTTP request has been made. In the initial http GET it can include the client ints it would have asked for, removing the round trip. It's very sensible as an optimisation mechanism. Fundamentally questions about client hints in general as a mechanism, and any specific client hint may or may not have concerns related to it. I don't think that's relevant here. if you presume client hints are a thing, this is a straightforward optimisation to make them less costly in the common case. I don't remember TAG's position on client hints in general, but as optimisation it seems fine. I don't want to say it looks fine without Yves saying he's okay with it. Plenary? Proposed closed and getting Yves confirmation in plenary?
... They want to ship some of it and it's been a while. 

Dan: we don't have a general position on client hints. In Feb 2019 we had a proposal about migrating high entropy http request headers to client hints which we [responded positively](https://github.com/w3ctag/design-reviews/issues/320) to. 

Tess: we don't necessarily need a position on underlying mechanism to be positive on it

Hadley: do we need to take a position on client hints?

Tess: we probably should. There are specific client hints being proposed I'm not okay with, but some that are fine. General mechanism seems fine. there's been a lot of back and forth.. people working on it are responsive. Biggest concerns have been / are being fixed.

Dan: what's the current implementation status on client hints itself?

Tess: probably out of date - I understand it's still a single engine thing. Mozilla's position overall was "non-harmful". We were initially opposed but they've been very responsive on specific feedback. No implementation in Safari.

Dan: would it make sense to say if the implementation s ory is okay to say it makes sense as a mechanism but there should be some rule about things shouldn't be implemented as a client hint if they can be x or are intended to be y. Adds complexity, not something developers expect, not easily configurable in servers. Finding? Design principle?

Tess: one of the advantages of client hints as infrastructure is the shift of passive fingerprinting into active fingerprinting. One arguement is that it's a good idea because it improves the stuation fingerprinting-wise. Specific client hints that make things worse fingerprinting-wise subvert the entire mechanism and probably shouldn't be done.  Ultimately it doesn't come into this specific design review.

Dan: in the spirit of spinning things into design principles, we might want to open a design principle issue

Tess: makes sense as a design principle for i fyou're thinking about adding a new client hint we can offer guidence about when it is or isn't appropriate. That's the case for many other mechanisms... http header? Propose close and I'll file a design principles issue

Dan: I'm doing it.

Lea: when I was reviewing the compute pressure we were discussing adding a principle about designing APIs in a low level way so we're stuck on hardware, do we have that?

Tess: we should have that

#### First Party Sets

Hadley: read through the additional comments - discussion of the difference between an origin and a privacy boundary.  The privacy boundary concept is probably helpful. Conceretely I don't think it changes our approach which is to wait for the changes in the explainer.

### Breakout B (US / APAC) 

Present: Peter, Lea

Regrets: Sangwhan

#### [ARIA in HTML review](https://github.com/w3ctag/design-reviews/issues/614) - @hober, @atanassov

#### [CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @LeaVerou

#### [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou

#### [Font Enumeration API](https://github.com/w3ctag/design-reviews/issues/399) - @hober, @plinss


### Breakout C (APAC / Europe) 

Present: Dan, Amy, Sangwhan, Ken, Yves

Regrets: 

#### [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris

Sangwhan: curious about traction from other implementers. I like the idea. 

Ken: I thimk it's for single page applications - which do work in every browser....

Dan: can this be used to spoof the url bar because we're talking about modifying history? Dominic clarified that and made a change to the privacy & security to indicate that. That was the main issue I saw. Felt inherantly worrying when you talk about something that is an API onto the browsing history. The word "app" is unfortunate in the name. Looked to me like that had been thought through in the spec.

Sangwhan: I wasn't particularly concerned about that. 

Dan: Ken asked framework authors to look at it

Ken: posted links to feedback

Dan: what next? They're asking to close up the review, is there more to do? 

Ken: they have good questions in [issues](https://github.com/WICG/app-history/issues), whether we have comments on those instead. Dominic filed a lot himself. NavigateState option... something we have some opinion about? 

Dan: key things they asked from us are about when [url bar updates](https://github.com/WICG/app-history/issues/66), [reporting navigation duration](https://github.com/WICG/app-history/issues/33), [replace window history and window.location](https://github.com/WICG/app-history/issues/67), and [should apphistory events be fired on page load](https://github.com/WICG/app-history/issues/31)?

Sangwhan: usually the origin that matters for users?

Ken: sharing a URL, then it matters. Regular users don't look at the URL but they do share it

Sangwhan: share goes to another view, the share view

Ken: but you have the full URL, eg. with a tweet so the twitter view inside the SPA.. the tweet not the whole thread
... Normally framework around history API, updates the URLs..

Sangwhan: feels somewhat random from a users perspective

Ken: lots of SPAs do it really well so they update the URL when you're changing the view, especially so you can copy the URL and it makes sense. Or refresh you stay the same place

Sangwhan: I've seen a lot of SPAs do that extremely wrong

Ken: if you don't know/think about URL and state...

Dan: it's about giving control to the developer, so they could use it to do something that doesn't make any sense. But ideally it's about servicing a user need which is that what happens in the history and in the URL bar makes sense wrt what the user's expectation is about that appication. Sharing/refreshing/copying are all things that give the user agency. 

Ken: today it's quite bad. All those routing framework have to hack around the existing API, so once in a while it breaks in unexpected ways

Sanghwan: that's what I meant about random

Ken: new API makes it easier to do this the right way. I have dealt with this in SPAs and it's a pain. Don't like pulling in these huge router frameworks that I don't understand.. I want to do it without relying on a framework and know what's going on.

Sangwhan: even if it's not super friendly to handroll everything being able to do it at a framework level in a way that doesn't look random is progress enough to justify this work. Right now it's not work. Would be great to use from the get go though

Ken: i think you can, that's what they're trying, it's not just for frameworks. They want to make an API because people are using frameworks so they can subsittute this API and have less bugs. But also an API for develoeprs who want to knwo what's going on. That's the problem with those routing frameworks, t ey expect your app to work in a specific way and sometimes that's not what you want. Having an easy to use low level API is realy progress.

Hadley: I don't mean to throw a spanner in the works.. Agree with what Ken and Sangwhan and Dan are saying that ultimately this makes things make more sense to users. We are spending a lot of energy in FPS saying users have built up an understanding of how the web works that hinges on some basics like having a vague sense of what an origin is... we're not too far away from all that stuff. In letting developers redefine the back button we are in redefining what back goes to, rather than going to the previous page ..

Ken: you can do this already

Sangwhan: it just sucks

Ken: not changing anything. People are doing this today.

Sangwhan: it's not great and this is why we're happy to see this

Dan: I have the same visceral reaction to this which is wait you're mssing with the history. But on the other hand, many web applications are built using this design pattern and 

Sangwhan: damage is already done, harder to find an application that doesn't do this these days..

Hadley: As a user this makes sense, that's really important, we should focus on that. May be logically inconsistent.

Dan: What does multi engine support look like? I was going to leave a note about that. Otherfeedback on the points Dominic has specifically asked about?

Ken: they're getting feedback from developers...  [on #66]

Dan: they're asking for feedback on the user experience of when URL bar updates.. 

Ken: if it's moving to another domain ti should update immediately

Hadley: I agree

Dan: that's feedback we can give from a how the web works perspective, reinforcing importance of origin. 

Sangwhan: you can't change the origin with this API can you?

Dan: no

Hadley: having an accurate URL seems pretty important

Ken: people have use cases like...

Hadley: Dominic says some people might want to use it if it changes the URL sooner.. but I don't understand why

Dan: the point is if you have the URL bar update you can make use of it. You go to a single viwe of a tweet you want the URL bar to be the tweet not the previous thing

Ken: angular and vue router work the same way.....

Sangwhan: youtube updates with time, but not the history...

Ken: same as google maps, stores coords if you move map.. copy it you get the local one but probably replacing the entry in the history

Sangwhan: cases like that they won't use this API..

Ken: it's the same, your'e just replacing, so you go back and forward you go around the map..

Sangwhan: makes sense for map, not for video..

Ken: why not? updates timestamp.. you press forward and want to go to the same place in video if you clicked back by mistake, or clicked a video you didn't mean to.. don't want to start from beginning..

Dan: could we say updating immediately makes the most sense from a web ux point of view?

Ken: vue and angular routers don't do that

Hadley: useful to ask Dominic what use cases where this would be bad

Ken: or ask them to explain how that works.. should there be a timeout? how long can you defer it? a few milliseconds? I'm going to ask.

Dan: will ask on our issue and reference their issue

Ken: #33 .. for performance? Seems reasonable to reuse performance entry if that's being used for everything else.

Sangwhan: there is no way to measure as of today? Agree performance entry.

Dan: if it's already being used in a similar way elsewhere then yes

Sangwhan: not the same but close enough that it makes sense. Likely it will fetch.. navigation pulls in new data in a lot of cases.. not the same computational complexity as loading a new page from scratch

Ken: [leaves comment on issue]

Dan: #67 should this API replace window.history and window.location ?

Ken: would be nice..

Sangwhan: would be very nicei but we can't get rid of window.history...

Dan: what's the decision point? Can't we let this be organic? If developers embrace this API then eventually window.history could be deprecated?

Ken: that's why it would be nice. Question is a few things with the API you cannot do? or will people stop doing it, or so important they cannot use this API?

Sangwhan: one thing is restoring scroll. I can see how that doesn't fit into the current design

Ken: you also want that for bfcache navigations right?

Sangwhan: it's not done thorugh an API, the user agent does that for you. If it's not a proper page it will probably put you in a weird state.. I don't know how that should work here

Ken: no counterpart to push state or replace state.. issue for youtube and maps? [leaves comment]

Dan: what other decisions are gated on this question? Do we need to decide as a platform right now? is he saying they need changes to API now?

Sangwhan: to take into account stuff like scrolling you might have to redesign certain parts of the API surface which would be difficult once you ship. I'm not entirely sure how pushState and replaceState would be replaceable with this. It covers most use cases but I don't know them all to comment on whether it would work.  There's also the frames problem. window.history supports frames. If you do iframe navigation it goes onto window.history. If you press back a couple of times and you've navigated within the iframe it navigates the iframe then to the parent document. This API does not account for that. We might want a separate breakout on this.. 

Dan: plenary? We could ask Dominic to join us for a discussion? See if you can schedule a time Sangwhan?

Sangwhan: I'll reach out to him and read up on all of their other issues.

#### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) (revist from Breakout A) - @LeaVerou, @kenchris

Ken: I looked at the comment - but the idea is that people want to know before they're being throttled. that's why it's a scale. And because of privacy they are not exposing the top speed of the cpu / gpu...

Sangwhan: there's a thing called BigLittle in ARM - you're running your device with the slower cores and as you saturate your CPU capacity you switch to powerful cores - good for power consumption. The M1 macs do this as well. The opposite version - hyperthreading - logical cores that have half the capcity of actual cores. It might look confusing [in this API] if you say "go further" but it plateaus because of hyperthreading.  

Ken: heterogeneous compuuting... 

[debate on CPU architecture]

Dan: we talked about this and said better to post feedback than hold off

Ken: Lea pinged me. I'll add something.

Dan: bring to plenary

Sangwhan: I'm sure they thought about this I just want to know how they plan to do it. Usually applications are not supposed to be aware of the switch.

Ken: good to point out, it's complicated.

Sangwhan: fingerprinting surface could be scary

Yves: you don't know what triggered the fact you are in slow consuption mode, heating / battery .. cpu is used by other things in the background. As long as you are nt aware of why you're being throttled it should be fine

Sangwhan: if you're being throttled or turbo'd if you send an event to the web app multiple origins can listen to the event and say at this very specific time we noticed this user got turbo'd on all of these tabs, probably a trackable surface, feels like it.

Yves: same issue with timings in general, that you can infer what's going on elsewhere basedon what's going on in your own sandbox

Sangwhan: and you only have one cpu in general so it'll be easier

#### [Random UUID](https://github.com/w3ctag/design-reviews/issues/623)

Sangwhan: I like it. Left comments.

Ken: I'm fine with it.

Sangwhan: new API, new capability, delta to crypto. Something people have been doing crappily, getting good random data using web APIs is not straightforward. This makes it easier.

Ken: that's great.

Sangwhan: perfectly fine, many valid use cases. They have a way to evolve the API moving forward as needed, eg. change algorithm or change entropy. 

Dan: what does the multi engine support look like? This will go in the web crypto WG which is closed.. so where after WICG? [leaving comment]. Important to go through W3C process for IPR.

Sangwhan: they asked if this should be in secure contexts only or allowed in insecure contexts? if you only allow it in secure contexts frameworks will use an insecure polyfill. We have a policy for new features in secure contexts only. But I think it's okay in insecure contexts.

Ken: I agree. We want people to use it. 

Dan: [triaged]

### Plenary Session 

Present: Ken, Dan, Amy, Peter, Hadley, Yves, Sangwhan, Tess
Regrets: Lea

#### Breakout Rollup

##### Breakout A

**Compute pressure API**

Dan: we need to come up with text for feedback

Ken: doing it

Tess: at least on apple platforms you don't get a chance to cut it out first.. I don't know if they have any text.. just because these events exist doesn't mean you won't be summmarily killed. It's a nice thing for the browser to give you a chance but ultimately the browser might make the decision to not give you a heads up first and that's okay. I don't know if that's something they acknowledge.

Ken: before you're getting killed, but throttled, so experience is bad. Not out of memory or anything like that.

Tess: a bunch of other place where we throttle websites/apps which we may or many not expose. page visibility api tells you things like whether you're a background tab

Ken: I think this is supposed to be focussed

Tess: if you're a foreground tab and browser window is backgrounded, you might not know in that case

Ken: will add something about that

Peter: vector for abuse, can something discover there's not a lot of cpu usage, let's go mine some bitcoin

Tess: it's the other way around, this is hinting that there isn't much cpu available. One way of abusing it would be to do something even more computationally expensive if you get the signal, but what happens is you get killed

Peter: the spec as it is right now it's saying you're using x% of the CPU. I could throw an observer and say whenever the threshold falls below 30% mine bitcoin and I won't get noticed, if it goes up, then stop mining.

Ken: we can add more comments, this is early

Dan: do they have anything about abuse scenarios in the spec or explainer?

Peter: don't remember seeing anything

Ken: they filled out the questionnaire

Tess: overall good comment

**WebXR Plane**

Dan: there was a reply with additional info about use cases. [responding]

**Client hint reliability mechanism**

Dan: opened an issue in design principles for text about client hints. Tess is writing feedback.

Tess: we talked about in breakout A. Where we ended up is it's a proposed closed but we wanted to talk to Yves first. My read is as an optimization mechanism it seems fine - given a world where client hints are a thing.  A lot of the conv in breakout A was how do we feel about CHs in general - but that doesn't change this mechanism. I know Yves had some back and forth about how they are using the 200 response...  How do you feel about closing this?

Yves: i took a look -one thing that bothers me is that you're mixing layers - mixing tls layer and http layer. If you see them as hints - such as SNI - that can be used to select the proper cert but notification of the host header - then it's borderline OK. 

Tess: draft closing statement...?  

[consensus to close]

##### Breakout B

[discussion of time of breakout B... doodle poll required]

**ARIA in HTML**

Tess: they want feedback by this week. I can try to block out time tomorrow. Can ping Rossen.

##### Breakout C

**App history API**

Dan: lots of discussion, pretty good, argument to be made that this API fulfils a user need because it is helping to create a coherant system and user experience for SPAs. Still questions which came up, we tried to address specific issues. One is should the API update the URL bar immediately or should there be delay? Not clear on use cases for delay, but framework devs seem to be in favour, so asked about that. Bump a week? Shouldn't be long running.

Sangwhan: we agreed to set up a call including Dominic and I'm supposed to reach out about that

**Random UUID**

Dan: triaged and Sangwhan has good things to say about it. Asked about multi implementer support and venue - got a response - no reply from webkit, ongoing with mozilla (standards position still open). Issue is it belongs in web crypto but web crypto isn't an open group; suggesting webappsec or whatwg. 

Tess: ongoing problem with things.. webcrypto doesn't have a home. This is not the first time since that group closed that people have wanted to add things to it. 

Dan: API, so could sit in webappsec

Tess: it could, but the fact we've seen multiple of these and there's no maintenance story for webcrypto makes me think should we (the TAG) go to the AC or Team and say this seems untenable? Should create a maintenance WG? This is going to happen again. 

Dan: I can email to wendy and ralph

Tess: as a stopgap webappsec would be fine. Folks in webappsec either are the right people or know who to pull in to review.

Sangwhan: one bit I'd like feedback on - about whether it should be secure contexts only. Hairy because we've been saying all new features should be

Tess: not all of us. We ended up with a lack of consensus, but in design principles: if a feature has a clear security or privacy implications it should be secure context only.

Sangwhan: this API I don't think should be restricted to secure contexts because it promotes frameworks that rely on this to throw in a polyfil that may not be cryptographically safe. In C we agreed that in this case it doens't seem like it would be harmful to allow in nonsecure contexts, but harmful if it was secure contexts only

Tess: I agree, polyfillable and people will polyfil it. Is the life of that polyfil bounded or unbounded? We shouldn't be encouraging people to roll their own crypto..

Sangwhan: yes

Dan: leave feedback?

Sangwhan: I left feedback, said partial consensus, I can update that. Okay to close?

Tess: Reasonable. Incredibly common and browser is already capable of doing it. 

Sangwhan: will leave closing comment

[resolution: satisfied]

#### Issue Triage

#### Meta

Dan: we need to be more clear with people that for specs in W3C groups they need to check with chairs and editors before kicking off a TAG review. This has happened multiple times. Editors and chairs might not feel spec is ready.
