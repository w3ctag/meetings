# TAG Teleconference
#### 26-29 June 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-06-26](https://www.timeanddate.com/worldclock/converter.html?iso=20230626T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Verifiable Credentials Dara Model v2.0](https://github.com/w3ctag/design-reviews/issues/860)
* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman
* [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo

### Breakout C (APAC / Europe) - [2023-06-27](https://www.timeanddate.com/worldclock/converter.html?iso=20230627T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman
* [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman

### Plenary Session - [2023-06-29](https://www.timeanddate.com/worldclock/converter.html?iso=20230629T060000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Peter, Yves, Rossen

Regrets: Lea


### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

*discussion on what happened last week in the privacy sandbox related call*

Rossen: they have their third LGTM [in BlinkDev](https://groups.google.com/a/chromium.org/g/blink-dev/c/PN_aE-X-f9U) so from an API owners pov they are good to go.  Suggest going to review.  

Yves: from my recollection - we're not against it but there are issues needing to be fixed - like being able to exclude topics for all sites - e.g. "I don't want health topics". not well enough defined.  They have to say that topics will be a better replacement than shared storage, etc.. which replicate mechanism of third party cookies. 

Dan: trials?

Rossen: they have done the trials.

Peter: There's a header - there's a lot of dicussions on setting topics to empty. If you send the header that opts out of FLOC that apparently opts you out of TOPICS as well.

Dan: is it a FLOC-specific header? 

Peter: It's a permission policy setting- a lot of apps e.g. gitlab, wordpress, mastodon, set that to NO by default. Apparently TOPICS respects that header.

Rossen: there's a feature detection for topics API - as a developer at a site - I'm providing a new feature - as a developer I can segregate our customers - and thereby tell people to come back with a browser that supports it.. 

Dan: see [here](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/06-12-minutes.md) for discussion with m. kleber on topcis...  Michael said "topics in incog mode or turned off works the same as if the topics api does for a regular user who has only recently started browsing". So according to him it's not detectable.

Peter: it's true for a browser that supports topics incog mode is not detectable. But what if I'm using a browser that doesn't support it at all that is detectable.

Rossen: right.

Dan: the browser could return "yes" but return false data.

Rossen: that assumes browsers will do extra work.

Yves: you can use introspection to see if it's been implemented or not...

Peter: still forces other browsers to do work.  They can do this but it still puts an onus on them to do something to prevent losing market share.

Dan: agree this a key issue - we need to make sure  we do not end up in a "works best in chrome" scenario for other browsers. 

*discussion on Chromium-based vs. non-chromium based browsers*

Peter: I'm presuming it'll be there by default for browsers using chromium... 

Dan: this is an interop issue, as Rick Byers [asked us to comment on](https://github.com/w3ctag/design-reviews/issues/726#issuecomment-1604275069).

### [Verifiable Credentials Data Model v2.0](https://github.com/w3ctag/design-reviews/issues/860)

Rossen: they are asking us for horizontal review. - Data model V2. Not triaged yet. 

### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @rhiaro, @hadleybeeman

### [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747) - @torgo, @rhiaro, @hadleybeeman, @atanassov

### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss

### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @cynthia, @LeaVerou, @torgo


## Breakout C

Present: Dan (first half), Sangwhan (second half), Yves, Amy, Max

Regrets:


### [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

*reviewing [Martin's comment](https://github.com/w3ctag/design-reviews/issues/726#issuecomment-1608499746)* 

Amy: from one of Martin's [linked papers](https://arxiv.org/pdf/2306.03825.pdf): "any replacement of third-party cookies may have to seek other avenues to achieve privacy for the web". This paper is specifically about Topics.

Dan: *lack of multi-stakeholder*

Dan: Topics impacts every single user of the web, everyone who uses a browser other than chrome. That's a big group. Micahel says: "Any UA that wants to pass feature detection but not give out information could implement the API to return an empty set of topics every time." - this means other browsers still need to implement. Forcing webkit and mozilla to implement the api in order to avert the situation where websites say "best viewed in chrome".

Yves: good summary. The fact you need to force others who don't want that api to implement it so you avoid having two different web, a chrome web and other browsers.

Yves: is site classification local in the browser, or sent to google?

Sangwhan: it's entirely local. [Demonstrates current build]

Amy: I understood that sites also need to opt in to being included in the topic categorisation for users. But seeing this, it's determining topics from sites which have not called the API. Did I misunderstand this?

Sangwhan: maybe that is just about sites having access to topics by using the topics?

Amy: this is problematic. Sites who know they serve a vulnerable population may not want to be used for this to protect their users.

Sangwhan: this version in the I2S does not provide the opt out for the topic as far as I can see it. Strange, because it's normative in the spec. That's a definite problem. Shipping something non-conformant is bizarre.

Sangwhan: imagine a website is misclassified by the web browser, so there is unexpected classification of cohorts that there is no way to opt out from. The fact that my personal website and 4chan are in the same cohort ("online communities" in this case) is not very comforting, and there is no way for me to. or if I want to change topics. Seems like a design issue. Seems user hostile.

Sangwhan: thoughts on document vs window? If you want to persist topics .. if you put it on window there's a possibility of you being able to use it in service worker process, if it's on document you have to use it in document. For extensibility, window makes more sense, or worker global scope.

<blockquote>
The following comment has come out of TAG discussions this week:
  
First of all, thanks to @martinthomson for those pointers to two relevant papers. 
  
We've continued to discuss this API across several calls this week. @cynthia also demonstrated the current implementation.
  
We remain concerned about the points recently raised about interop. Especially given the lack of multi-stakeholder buy-in for this API, how can we really protect against a future where advertising based sites tell users they must switch to a browser that implements Topics? @michaelkleber you've said "Any UA that wants to pass feature detection but not give out information could implement the API to return an empty set of topics every time" however that still implies other UAs would be required to implement the API (at least minimally) when they might not otherwise do so, in order to mitigate privacy harms for their users - so there is a risk here.
  
We remain concerned about the ability of users to give meaningful consent for their interests to be calculated and tracked from their browsing activity. The spec says:
  
>  suggestion that user agents provide UX to give users choice in which Topics are returned
  
and refers to a "user preference setting" in several places.

We have inferred from this that users are able to disable particular topics in the settings, or the API as a whole, but we don't think that either of these potential configuration options are good enough to protect against potential privacy harms, particularly for marginalised groups. A person's status as vulnerable, at-risk, or marginalised can change over time, and this isn't something most people are necessarily aware of or paying attention to in their day-to-day web use, and nor is it reasonable to expect people to regularly review their browser settings with this in mind. Thus, "opt out of individual topics" is not sufficient to offer meaningful consent to being tracked in this way. Further, from what we have seen of the API as implemented so far, there are no user preference settings relating to specific individual topics. We raised this in our initial review, and don't feel it has yet been considered with the depth warranted.
  
This issue intersects with others, for example, as [pointed out in the Webkit review](https://github.com/WebKit/standards-positions/issues/111#issuecomment-1359609317) that the topics list represents a western cultural context, and that the mechanism for sites being classified according to these categories is unclear. We [understand from the spec](https://patcg-individual-drafts.github.io/topics/#determine-topics-calculation-input-data-header) that site classification is automated, based on the domain, but the mechanism for doing this remains opaque, and it is not clear there is any recourse for sites which are misclassified.
  
We saw in the current implementation that sites in a user's browsing history which do not call the Topics API were being classified under particular topics. We had been led to believe that sites _opt-in_ to being classified by calling the API ("Sites opt in via using the API. If the API is not used, the site will not be included." in the initial review request), but perhaps we misunderstood, or this has changed. The [spec refers to "site opt outs"](https://patcg-individual-drafts.github.io/topics/#privacy-considerations-header), although we weren't able to find how they do this in the spec (please could you point us to the right place if we missed it?). 
  
Questions:

* Do you have a response to the points raised in [Webkit's review](https://github.com/WebKit/standards-positions/issues/111#issuecomment-1359609317)?
* Do you have any analysis or response to the papers that Martin pointed to?
* Please could you elaborate if it is in fact the case that all sites browsed by a user are included by default as input data for generating a user's topics list?
  * If this is the case, what recourse is there for sites which are misclassified?
* Can you clarify the situation with regard to definition of user preference / opt out?
* Have you considered dropping the part where topics are calculated from browsing history, and instead entirely configured by the user in their browser settings? This would be much closer to people being able to meaningfully opt in to targeted advertising, and would make several of the other concerns raised moot.
</blockquote>



### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

### [Borderless mode](https://github.com/w3ctag/design-reviews/issues/852) - @cynthia, @ylafon, @hadleybeeman


## Plenary Session

Present: Peter, Amy, Dan, Yves, Max, Hadley, Sangwhan

Regrets: 

### Breakout Rollup

#### Breakout A

#### Breakout C

##### More Discussion on TOPICS

*reviewing proposed comment text, above*

Peter: could the user be asked to opt in to each topic?

Sangwhan: sessions last for a couple of hours... 

*document vs window*

Yves: Seems cleaner to have it on document... 

Sangwhan: if you put it on document how does it function when it comes to service worker?  The context is the document but is it really that important for it to be attached to the document?  Is the entire session the same set of topics?

Yves: I see the point. If it's attached to window it can also have issues with delegation to other sites.

Sangwhan: if you have it on document - contextual gating...  I can see benefits either way. If the auction is going to happen in a service worker then - real time takes CPU time away from the user... 

Peter: browsing through open questions list... in explainer... thing that worries me open question #2 - does mislabeling cause harm?  What if for example a user browses a lot of LGBTQ sites and their browser advertises LGBTQ topics and they visit a gov site .. and in their country being gay is illegal..

Sangwhan: if sites content is gated behind a log in... domain can be classified - pinend to a topic - if the user visits that domain they get assigned that.  That exposes info about the web site that the web site might not prefer.  The user in the sense of the content provider might not want that. Might want to be dissasociated from a topic.

Peter: example: say I'm running a site and somebody's engine misclasifies my site as being a nazi site - now I'm misclassified as being a nazi - and anyone who visits my site gets nazi adds...

Sangwhan: topic list has been washed by US tech - comes from the IAB certified list... So that particular use case cannot happen.

Amy: this is still a very western context list... can cause problems in different part of the world...

Peter: so many dog whistles and other associations... right wing companies that advertise on certain things - you're going to see right wing advertising pop up on a site that has nothing to do with it...

Sangwhan: we need a better example... 

Peter: I think it's nuanced - more so than having a small list of IAB topics.

Sangwhan: **childcare** is a good topic...

Peter: inferences from a collection of topics - this combination of topics can mean X or Y.

Amy: I feel like we've given a lot of this feedback.  Hence what I wrote: I feel like these issues have not been addressed.

Dan: the issue is with the topics design, and fundamental decisions taken around how to allow for user choice

Sangwhan: the lack of opt out on behalf of the content provider is one issue we have to loop back.

Dan: I don't see it's possible to leave a reslution satisified without some kind of multistakeholder buy-in. We've left satisfied with concerns on APIss that we're generally happy with but lack of multistakeholder. If we could get to a point where we're generally happy we could leave that. But currently we're not. We need these issues to be addressed.

Amy: one option is to ask for user's to define their own topics. They don't need to be extracted from browser history at all. Standardise a data model 

Dan: it's not completely out of the question that when I open my browser I'm asked for an opt in order to participate in this ecosystem, or as a website I opt in to participate. It doesn't need to be I need to opt in every single time I'm targeted for an ad. Could be a first time use opt in, and an occasional reminder, with here are the topcics we think you're associated with. Can we be pushing on that?

Sangwhan: pre-filtering of a topic... but not proscribing what presention is...

Peter: we don't have to specify the exact UI...

Amy: I'm suggesting browser presents a list of options and user chooses using their brain.

Peter: personally I'd be OK with the browser popping up and offering "looks like you're interested in these topics would you like to add them to your list?"

Amy: would be fine with that.

Peter: user should be asked to opt in before they're assigned a topic that's going to be broadcast.

Amy: language of topic assignment is jarring - topic suggestion would be more appropriate.

Peter: I agree - leaking info to third parties. that user might not be want leaked. We don't need to entrench or rubber stamp a certain amount of leaking as being okay.

Dan: what specific feedback? This is that. If you are browsing the web and suddenly a UI comes up and says "hey we've noticed you've been browsing these different topics" you might not want that to happen in this specific time and place. Context-oblivious popups about this could be sensitive.

Amy: we've had the response that this already happens

Peter: ads seem a lot more random today, even if they come from more detail today

Sangwhan: I don't have a better solution. They should have the chance to experiment. What's happening right now [with current ad networks and tracking] is disturbing. I don't know if it's good enough, but its in a better direction

Peter: it's a step in the right direction. Concern is that there's other steps that could be taken, bigger steps, and if we rubber stamp this they'll take this step and then never another step.

Sangwhan: if the extreme direction causes too much friction the whole effort might stop

Amy: we're hypothesising about what might or might not happen if this one API proceeds or not. There are a lot of forces at play - regulatory, economic - not only web platform apis. We can't predict the outcome. I don't feel comfortable entrenching this model just because something bad "might" happen if we don't.

Peter: **[posts comment](https://github.com/w3ctag/design-reviews/issues/726#issuecomment-1612522047)**

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

