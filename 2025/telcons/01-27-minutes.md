# TAG Teleconference
#### 27-29 January 2025

---

## Agenda:

### Breakout A (California / Europe)  - [2025-01-27](https://www.timeanddate.com/worldclock/converter.html?iso=20250127T173000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk
* [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @hadleybeeman
* [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014)
* [FYI - Web Authentication API: PublicKeyCredential’s getClientCapabilities() method](https://github.com/w3ctag/design-reviews/issues/1016)

### Breakout B (California / Australia) - [2025-01-28](https://www.timeanddate.com/worldclock/converter.html?iso=20250128T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss
* [On-device Web Speech API](https://github.com/w3ctag/design-reviews/issues/1038) - @jyasskin
* [Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039)

### Breakout C (Europe / China) - [2025-01-29](https://www.timeanddate.com/worldclock/converter.html?iso=20250129T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman
* [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)
* [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)

### Plenary Session - [2025-01-29](https://www.timeanddate.com/worldclock/converter.html?iso=20250129T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
-----


## Breakout A

Present: Matthew, Jeffrey, Dan, Peter, Tess, Hadley

Regrets: Amy

### [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk

<blockquote>
First a bit of context: The TAG feels the whole clipboard API is more permissive regarding permission than it should be. Also to be clear, we understand that your position is that this is required for the remote desktop scenario in order to allow for seamless clipboard access. The concern we have is about abuse of this API in *other* scenarios. Remember that web users will also be using other web applications, visiting other web sites, and will be subject to the same risks and attacks as any other web users. 

For example: user receives a text message from a scammer purporting to be from a trustworthy site; user clicks on the URL in the text message; now they are interacting with a web page that looks benign but it's really a scam web site; The web site convinces the user to paste something into the page; the web site shows the permission prompt, which of course the user accepts, and thereafter it's able to scrape any info off the user's clipboard any time it gets focus.
  
We also think the remote desktop use cases would work fine if it only works on paste, and without the clipboardchange event, websites don't know when a copy happens and so are incentivized to only read the clipboard on paste. With clipboardchange, they get a new incentive to be incompatible with Firefox and Safari, which [isn't good for the Web](https://www.w3.org/TR/ethical-web-principles/#multi). Before endorsing clipboardchange, we'd like to see an explanation for why that won't happen.
</blockquote>

Jeffrey: not convinced by the abuse case... They are going to update their explainer to describe why clipboard change is useful even if you don't assume chrome's UI model for clipboard... And I think the TAG is fine with the Firefox & Safari UI model.

*discussion of an explicit permission grant*

Jeffrey: in Firefox the browser pops up somehting and in Chrome there is an explicit permission grant.

Dan: [leaves comment](https://github.com/w3ctag/design-reviews/issues/1017#issuecomment-2616519376)

### [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @hadleybeeman

Matthew: some input... APA has looked at this ... and have had some opinions relating to which bits relate to accessibility. By breakout C I will have further input.

*deferred to breakout C*

### [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014)

Jeffrey: mostly for pretty large orgs creating e.g. search result pages that don't link out... you can get parsing to go a bit faster if browser knows not to look for links.

Yves: it's just links or also embedded links?  

Jeffrey: It's about the prefetch scanner... Scans the whole doc quickly and then starts doing the prefetching. If you don't prefetch you do everything a bit faster. Some entities have explicitly asked to turn off the prefetch scanner ... due to legal issues.  The designers don't want it to be used for that... 

Peter: I envision problems with preload scanner fetching links... part of me says "good idea" but another part gets annoyed at all these optimization knobs... that to me feels very implementation specific... optimization should be transparent... users (develoeprs) shouldn't have to care about them...

Dan: is this chrome specific?  

Jeffrey: I think it also helps webkit... but gecko doesn't do prefetching.

Jeffrey: arg against: you're only going to be confident about turning off preload scanner.. if you know you're not going to have these kinds of links. We shouldn't be adding complexity only to solve the largest organizations... 

Jeffrey: the use case is on the open web.  

Peter: I like the notion of not prefetching until you have consent... I don't like adding a feature that only helps ~3 companies... but if it's a lot of traffic then...

Jeffrey: our review is: there are pros and cons... not against it, but also problems. So satisfied with concerns?

Dan: is it a foot gun?

Peter: would only hurt performance... so it would stop things being fetched... Work around would be don't put the links in.

Jeffrey: this feature is explcitly not for the "don't link until consent"

Peter: should that feature be handled by a different tech?

Dan: where is this happening? 

Jeffrey: WICG

<blockquote>
Thanks for sending this our way. The explainer is clear and we understand the articulaed user need. Our overall feedback is that we don't have strong concerns about it, but we are worried about adding complexity to the web platform in order to only support a very small number of web sites. This is aligned with our "[prefer simple solutions](https://www.w3.org/TR/design-principles/#simplicity)" design principle. A question on venue: Will this work eventually go the web performance working group? This feels like a performance optimization and so should be aligned with the work there. In general you should have a plan for where this work goes after WICG (assuming you intend to take it to WICG).
</blockquote>

### [FYI - Web Authentication API: PublicKeyCredential’s getClientCapabilities() method](https://github.com/w3ctag/design-reviews/issues/1016)

Jeffrey: suggest we decline.  It's already shipped...  It's an FYI.

Peter: no explainer...

Hadley: mozilla is happy.

Jeffrey: we could look at how this matches how we want feature detection to work...

Peter: basically just booleans... 

Jeffrey: I think it matches how webgpu is doing thing...

Peter: similar to media stuff...

Peter: i'm fine with declining.





## Breakout B

Present: Peter, Tess, Jeffrey, Martin

Regrets: 


### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss

Peter: Not interested in fighting this anymore. Want to get Martin's and Lea's feedback.

Martin: Same. Seems like every response is "you don't understand this". 

Peter: We seem to be missing part of the model, but the model also doesn't match how I think it should work. Issue with View Transitions is bigger than this part. Don't think I can win the bigger fight.

### [On-device Web Speech API](https://github.com/w3ctag/design-reviews/issues/1038) - @jyasskin

[Discussion of Jeffrey's suggested comment.]

Google Meet might want to do on-device recognition iff all languages spoken are available. The proposed API doesn't support good UI for this: we'd want a single request that lists all the needed languages.

General support for having a boolean where the site requires recognition to be done locally, and then browser UI asking to download a model for any use of speech recognition.

Peter: also mention that it would be nice if users could pick their cloud recognizer.

Jeffrey's suggestion for Plenary:

<blockquote>

Being able to recognize speech on a user's local device seems like a great advance, and we strongly support it.
  
We note that this is a prefixed API with an old design that it might have been good to update in the process of unprefixing it. Unfortunately, documentation violated https://www.w3.org/2001/tag/doc/polyfills/#don-t-squat-on-proposed-names-in-speculative-polyfills and recommended assuming the prefixed and unprefixed names would behave identically, so that option is closed.

We see sites' desire to guarantee that speech isn't sent outside of the local device (for example to a cloud speech recognizer operated by the browser), especially for end-to-end-encrypted (E2EE) services. This is hard to actually guarantee: a valid browser architecture, especially for low-power devices, is to run the entire browser in the cloud and stream its UI down to the user. But with that caveat, we support giving the site a way to encourage the browser to keep the speech local.
  
We don't see a reason to let sites require the recognition to happen in the cloud if the user prefers it to happen locally. That is, `recognition.mode==cloud-only"` doesn't seem like an option that should exist. Perhaps just `recognition.localOnly = true` or `onlyOnDevice`, or have sites check the return value of the `requestLocalRecognition([lang1, lang2, ...])` function suggested below?
  
We wondered why `recognition.onDeviceWebSpeechAvailable()` and `recognition.installOnDeviceSpeechRecognition()` take a `lang` parameter when `recognition.lang` exists. @jyasskin asked you via a side-channel and heard that a video-conference system might have participants on a call speaking several languages and would want to recognize locally only if all the participants' languages are supported. We think there's a better design for this along two axes:
  
1. Having each listener spend CPU cycles to recognize audio seems wasteful compared to having either the sender or the cloud recognize the speech once. In an E2EE system, the cloud might not be able to, but putting the responsibility on the sender seems more efficient, both in terms of the number of language pack downloads and the CPU time for recognition.
2. If a site wants to know if it can recognize in multiple languages, it should request downloads of all those languages in a single permission prompt. So an API more like `SpeechRecognition.requestLocalRecognition([lang1, lang2, ...])`. This `request` function also seems to mitigate the fingerprinting risk better than a query function that can ask which languages are present without showing the user a prompt.

Browsers should also proactively offer language pack downloads to people using sites that don't know about this option. Could the spec suggest this? Would an omnibox icon be an appropriate UI in your Chromium implementation?
  
Similarly, there might be cases where a user actively wants the recognition to happen in the cloud, for example if their battery is unusually low, or (speculating) to use a particular cloud service if there are several options with privacy tradeoffs. The same UI might be appropriate for giving them that control.
  

Nits:
* `onDeviceWebSpeechAvailable` looks like it's going to be an event handler because of the initial `on`. Above, we suggested a design that doesn't need this name.
* "download over a cellular network" isn't quite the right condition for guessing that the user might prefer not to pay for the download. https://github.com/tomayac/netinfo/blob/relaunch/README.md#metered-connection suggests "metered", but that's not adopted into a working group yet.

</blockquote>



### [Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039)

Martin and Marcos should review. Jeffrey doesn't see anything to complain about.

Should ask Privacy about the zero-knowledge proofs.


## Breakout C

Present: Dan, Tristan, Matthew, Sarven

Regrets: Amy, Max, Hadley, Yves

### Discussion on Societal Impacts Questionnaire / Sustainability

Dan: *proposal to fold sustainability considerations into societal impacts...*

Sarven: Sounds good - there is a whole Web Sustainability interest group dedicated to that specific area - if they have the energy then it makes sense that anything touching sustainability can lead spec authors in that direction...

... I'm happy to work on this... I can make this as one of my primary work.  I can edit (societal impact questionnaire).  What progress do we want to do? Do we want to get a group note out this year?

Dan: Good to have a transition from Amy to new editor(s). Sarven and Tristan?

Dan: *will make a PR accordingly*

Sarven: minor note: this questionnaire has been on my radar ... I tried to integrate this into the SOLID protocol:

Sarven: https://solidproject.org/ED/protocol#societal-impact-review . SI has been in my radar but didn't get to it in the Solid Protocol. Could apply the questionnaire there as an exercise.

Yves: we can use a tentative short name... and when we publish in TR we can ask for this specific short name.

### [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) 

Matthew: I had a look at this... Summarizing: we've established that on the technical side of things we trust these people are the experts... We can go with their view that some of the changes are editorial. In their readable change log... there are several changes that need some further look or clarification... and one of the docs doesn't have a human readable change log... and I think we should ask for a human written one. The good news is - when looking across the 7 documents, there are 3 or 4 changes common to almost all of them... So actually less work than we thought.  So +1 to Hadley that it would help to have some clarification on some of these... I'll put in my comment before the plenary what those are. They have provided ... some info .. but still not clear what the implications of some of the changes are... 

*we agree to re-visit at the plenary*

*discussion on adding WCAG citation to respec bibliograpgy*

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: plan was to close it and ask them to have a proper security review....

Matthew: [Changes to the explainer](https://github.com/WICG/manifest-incubations/commit/f255162f1f6610f23c182ad7381e78f6088f0422)

Yves: as long as they do a complete security review then I'm fine with *satisfied*. Will still require buy-in from all implementers..

<blockquote>
Thanks for having updated the explainer based on our feedback. We will close the issue but would like to see a more complete security review from SING.
  
Please work with other implementers ... [something] ... and move this from WICG to another more permenent home.
</blockquote>

*we can agree at the plenary what resolution to give this*

### [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman

Matthew: [Substantive changes to explainer (re prior art)](https://github.com/WICG/paymentlink/commit/7193df1f59df3c6b4342c09ccd0d402eecb782ed) (there was also a typo fix, separately)

Sarven: I have a TODO to review this... capture what we said in prior meetings... 

*we will discuss further at the plenary*

### [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)

### [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)

Matthew: both of these (1012 and 1013) we asked for specific bits to be put in the explainer but no reply or updates on either... 

### Discussion on TAG GitHub Extension

*matthew to make changes relating to authentication and share to rest of TAG*

  
## Plenary Session

Present: Peter, Dan, Hadley, Tristan, Jeffrey, Matthew, Sarven, Yves, Tess,

Regrets: Amy, Max


Dan recognizes Peter for chairing since 2013.




### Breakout Rollup

#### Breakout A

Dan: We looked at `clipboardchange` and posted a comment. No replies yet. Didn't talk about the VCWG specs; agreed in Breakout C to talk about this in the plenary. `expect-no-linked-resources`: we posted a comment. And we declined `getClientCapabilities()`.

Peter: I think we hoped to close `expect-no-linked-resources` in the Plenary. No feedback yet, so waiting until next week.

#### Breakout B

Peter: Postponed HDR. Hoping for Lea's input. We'll need to reassign this or rope in other color experts. View Transitions: Martin and I aren't thrilled, but we're willing to close. Want to hear Lea's response, perhaps over Slack. I think we should close it.

Jeffrey: I drafted a potential comment on Web Speech in the notes above. It's long. They also want to do the same thing as the proposed LLM-based Translation API does for downloading big things, but I didn't get a chance to compare the two.

Dan: The feedback should be bolstered with links to design principles and/or privacy principles.

Jeffrey: I'll look for links after the meeting.

Dan: And put it into private brainstorming.

Peter: Delegation-oriented FedCM. Delaying to next week so new folks can look at it.

#### Breakout C

Dan: Societal impacts Questionnaire and sustainability. Fold sustainability into societal impacts? Tristan and Sarven volunteered to edit the Societal Impacts questionaire. Also talked to Tzviya who said the Team are looking for ways to incorporate human rights review into the process. They're hoping for this document to help with that. I will update the editorship.

Dan: VCWG specs. Close that today? Web app scope extensions: Want to say it's satisfied, but want Martin to approve that. They've been responsive. Made changes in November.

Jeffrey: Assign it to Martin?

Dan: Post it to #design-reviews on Slack.

Dan: Payment links in HTML: They've added some things to their explainer. 

Sarven: 
  
  
  
### [Jeffrey's explainer PRs](https://github.com/w3ctag/tag.w3.org/pulls?q=is%3Apr+is%3Aopen+label%3A%22explainer+explainer%22)

#### [Markdown](https://github.com/w3ctag/tag.w3.org/pull/61)

Peter: Not sure about the assertion that Markdown make it easy to link.

Sarven: If the explainer is on Github, Markdown is natural. If it's hosted somewhere else, there's no particular reason that Markdown would be relevant.

Dan: Explicitly say "assuming you're hosting this on Github, use Markdown". Encourage stable anchors too.

Hadley: Do we care about the source format? Probably not.

Peter: Like first sentence. Second should be about ensuring that sections are linkable. "You can do this easily by using Markdown and Github." 

Jeffrey: "Use a source format that's easy for other people to contribute to."

Hadley: Really glad we're including this.

#### [Prior Art](https://github.com/w3ctag/tag.w3.org/pull/63)

Hadley: +1

Jeffrey: [merges]

Sarven: Not sure the word "worse for the web" is the best.

Tess: "Worse" might be right. We want them to explain why they picked the option. If something's worse, great. If it's just an aesthetic choice, we want to know that too.

Jeffrey: Send a followup PR. :)

Hadley: E.g. something's worse for the web but way more complex.

#### [Alternatives Considered](https://github.com/w3ctag/tag.w3.org/pull/64)

[Lots of LGTMs]


#### [End-to-end experience](https://github.com/w3ctag/tag.w3.org/pull/66)

Matthew: Looks good, but why change "explanation" to "demonstration"?

Hadley: Don't want to imply that people need to build a whole demo.

Jeffrey: It was to imply that pure prose isn't great; we'd rather screenshots.

Hadley: We also talk about not specifying UI. And we have demos where the feature doesn't show anything to the user, but still want to know how it affects users. Loading speed, packaging. We often ask authors of those explainers to take a step back. Don't kknow the best way to convey this. Use more words?

Sarven: Is this a recommendation for what the explainer should include? Wouldn't this be included in the proposal/report itself?

Matthew: Often we get explainers before there's a spec.

Hadley: Or we get an explainer that's meant to be the abbreviated summary, coming out of a collection of 5-10 long specs.

Jeffrey: And there are some other issues that'll imply further changes in the future.

Dan: Merges.

#### [Make it a Note](https://github.com/w3ctag/tag.w3.org/issues/65)

Dan: I like this idea because it gives the document a bit more standing.

Matthew: Sure, it's kind of a de-facto standard, and it's really good, and some people aren't aware. Does it mean that explainers will end up in TR space? Also we looked at one heading wording; I have another question. [Will ask on Slack]

Peter: I'd like explainers to wind up in TR space.

Hadley: There are WGs that still start with Use Cases And Requirements, and then sketch their spec. Want to get into people's heads that this is a good place to start.

Matthew: If we go into TR space, they need to be super easy for people to edit.

Jeffrey: Moving explainers to TR space is independent of publishing this as a Note

Jeffrey: Concluding: I will migrate this to be a Note.


### VCWG Specs

Matthew summarized the changes. Some might be architectural.

Matthew: we could work out what's architectural and then ask for more info on those... 

Hadley: it's frustrating to get stuff that's this evolved... Each one of those points reflects extensive debate in the wg... for us to give feedback, it feels way too late... to be useful.

Jeffrey: I think we shouldn't ask for more detail about most of these... we should look at them and figure out if we have something to say. The one that I noticed was "context injection" which I thought was in the controller document... Processing by JSON or JSON-LD, supposed to act the same... The note says "if you're not processing it as JSON-LD then ..." so I will write a proposed comment. 

Matthew: one of the ones that stood out to me - about generalization for non-DID identfiers...

Jeffrey: we reviewed the controller document this is point to... we said it was not sure it's useful , but good that it can be non-DID. I think we've already reviewed it and we don't need to say anything else...

Matthew: the JOSE / COSE one... doesn't have a change log.

Jeffrey: this is the one that will be the foundation of the digital identty stuff in the fedid working group...

Matthew: another thing - the removal of integer error codes... 

Jeffrey: I think that we probably don't care about that... Seems like it's up to them.

*we agree that Marcos may have opinions so we should wait until next week*

### Issue Triage
