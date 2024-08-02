# TAG Minutes Doc - week-of 29 July 2024

## Agendas

## Breakout B (California / Europe)  - [2024-07-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240729T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou
* [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss
* [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss
* [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo
* [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

### Breakout C (California / Australia) - [2024-07-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240729T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

**special plenary session**

* Discuss call schedule. Proposal on the table:
  * we move from 5 to 4 weekly breakouts
  * we designate one of these breakouts each week to be the "plenary" breakout
  * We still need to move one of the brekouts to be a good time for Europe and California - could breakout B be adjusted approprietly?
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
* Outcomes of Seattle f2f
* Impact of Google Cookie Announcement

### Breakout D (California / Australia) - [2024-07-30](https://www.timeanddate.com/worldclock/converter.html?iso=20240730T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss
* [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* What do we do with FedCM reviews?
  * [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
  * [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
  * [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
  * [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss

### Breakout E (Europe / China) - [2024-07-31](https://www.timeanddate.com/worldclock/converter.html?iso=20240731T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk
* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion
* [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon
* [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @LeaVerou
* [Timing Info for ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/958) - @martinthomson, @torgo, @maxpassion
* [`noopener-allow-popups` value in COOP](https://github.com/w3ctag/design-reviews/issues/964) - @martinthomson, @torgo

## Minutes

## Breakout B (California / Europe)  - [2024-07-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240729T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Matthew, Dan, Tess, Hadley


#### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @LeaVerou

#### [Specification review for CSS Anchor Positioning](https://github.com/w3ctag/design-reviews/issues/848) - @LeaVerou, @plinss

#### [text-wrap: pretty](https://github.com/w3ctag/design-reviews/issues/864) - @LeaVerou, @plinss

#### [Speculation rules: target_hint field](https://github.com/w3ctag/design-reviews/issues/931) - @hober, @torgo

#### [Web Translation API](https://github.com/w3ctag/design-reviews/issues/948) - @LeaVerou, @matatk

Matthew: we need Lea's input on API shape... however I have several thoughts...

* First one is they did talk about a potential extension - running on **device only or going to the cloud**. That could be important. I think that's important. They haven't done research with developers - would be good for them to **see what developers think**. It strikes me in some use cases that would need to be controlled.
* Don't know if they've **talked with I18N WG** - specifically about their [issue 11](https://github.com/WICG/translation-api/issues/11) on specificity - BCP codes, etc... I18N would have thoughts on that. Also [streaming input support](https://github.com/WICG/translation-api?tab=readme-ov-file#streaming-input-support).
* They're **namespacing** all the functions under `ai`
* I have a general concern around efficiency and accuracy. Concerned that **developers would rely on this rather than doing translation** for static assets as part of their development process. Some non-normative encouragement to not do that maybe?
* Donwload **progress reporting** ... downloading the language support .. they think the web app should display the progress for that. Shouldn't that be part of the UA's UI?
* Also the API used [**signals**](https://github.com/WICG/translation-api?tab=readme-ov-file#destruction-and-aborting). Using signals to see if download has been aborted, etc...  

Peter: I think the signal - abort signal - is ok.

Lea: yes.

Dan: cloud vs on device...

Matthew: at the moment it's how the browser wants to implement it.  so it could be cloud based or on-device.

Lea: the author should be able to say "if you can translate this without going out to the network, fine"

Tess: it's about fetching language models...  The translation still might be fast or slow...

Matthew: i think in some cases they are talking about it going out to the cloud to do the translation...  I think we need to check up on that. So we could have: fast-local; slow-local; or remote.

Tess: the slow-local case could also be a privacy issue...

Lea: what's to prevent a web page from iterating over all the languages?

Tess: throttling in the implementaiton...

Lea: also to be clear: the need is there and I'm excited to see this. would be nice if there were an actual list of use cases...

Dan: UI elements or content or both?

Lea: both...

- Why a whole different object to construct instances? A static method on `ATTranslator` would also have the advantage of making it clear what objects are constructed. Same for `capabilities()`
- I wonder if it would make sense to have a single object, rather than a language detector and a translator, as the functionality seems quite related and often language detection is the first step.

<blockquote>

We agree with and support the user need. Here are our thoughts...
  
1. It would be good to have a list of use cases. We could think of some from our own experience, but they may be different than the ones you had in mind. Having an explicit list of use cases ensures that everyone is on the same page.

2. Please continue chatting with the I18N WG folks about [issue 11](https://github.com/WICG/translation-api/issues/11), and [streaming input support](https://github.com/WICG/translation-api?tab=readme-ov-file#streaming-input-support).
  
3. We're concerned about the use of the network. Specifically, use of the network to download a model, or use of the network to actually perform the translation, could introduce both delay and privacy issues. Is it possible for the developer to specify: "only do this if network access is not required"? We feel that differentiation between fast-local, slow-local (i.e. with downlaod), and remote/cloud-based cases is important for MVP.
  
4. We loved the approach you propose to partitioning, and using a fake download, to mitigate fingerprinting!
  
5. We recommend a translation-specific namespace instead of `ai`.
  
6. Why is a separate namespace needed at all? We understand these objects are not constructible due to the asynchronicity, but since they are creating instances of the same class, making this obvious by adding the factory as a static method of this class seems more consistent with precedent. Same for the `capabilities()` method, we don't understand why this needs to live in a different namespace, and we think that the more objects this API is spread across, the harder it will be for authors to understand how the different parts fit together.
  
6. We think there should be a prominent note encouraging developers to make use of professional translation of pre-existing content rather than doing automatic translation wherever they can - for both accuracy and efficiency reasons.
    
7. It seems to make more sense, and help simplify the API and alleviate some privacy concerns if the UA renders the download progress bar.
  
8. We did wonder if it would make sense to have a single object for the detection and translation, since they are so related (and often detection is the first step to translation). Was this direction explored?

</blockquote>

#### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @matatk, @plinss

Matthew: in a recent breakout, we agreed that it makes sense for APA to file a comment to ask how media queries such as `prefers-reduced-motion` (and contrast) would be handled across documents, where one document responds to the query and the other doesn't... and potentially ask for a clarifying note ...  Not really architectural level feedback. There was a thread in slack where TAG were talking about parallel classes... but didn't sound like a show-stopper.

Dan: anything in our conversations mean we should not have a resolution:satisfied result?

*agree to bump to **C** to see if we can collect Martin's thoughts*

#### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou

#### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou


### Breakout C (California / Australia) - [2024-07-29](https://www.timeanddate.com/worldclock/converter.html?iso=20240729T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

**special plenary session**

#### Discuss call schedule. Proposal on the table:
  * we move from 5 to 4 weekly breakouts
  * we designate one of these breakouts each week to be the "plenary" breakout
  * We still need to move one of the breakouts to be a good time for Europe and California - could breakout B be adjusted appropriately?
  
We refine the proposal to:

1. Get rid of A, get rid of C
2. Moving Breakout B to an hour later (18:00 UK time)
3. Keep the plenaries and move to a weekly plenary, rotating between 2 times (22:00 UK time Wednesday, 07:00 UK time Thursday)
4. Rotating read-out - where we spend 5 minutes at the beginning of each call recounting what happened in the previous call - we also want to continue to do readouts in the plenary
5. We need to do better at declining / abstaining / etc... 
6. Chairs try to move agenda setting to earlier in the week

note 1: expectation is that everyone should attend 2 breakouts each week every plenary - and give regrets if you have to miss one.

note 2: should we slip everything one day later?

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
#### Outcomes of Seattle f2f
#### Impact of Google Cookie Announcement

### Breakout D (California / Australia) - [2024-07-30](https://www.timeanddate.com/worldclock/converter.html?iso=20240730T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss


The core problem we're concerned about is that the use cases are in some ways also abuse cases.

The [Google Pay example](https://developers.googleblog.com/en/updated-google-pay-button-increases-click-through-rates/) is a great example here.
No doubt the Google Pay team believes that this is an unqualified improvement to their product.
They show that more people buy things if they show the last four digits of the card number in the Google Pay button.
If we think of the feature from the perspective of making shopping more pleasant and streamlined,
by showing people that payment through this button uses a service that is known to them, that has real upsides.
People presented with information from an actor they trust
(if they do in fact trust Google Pay services, which seems likely, at least to some extent, if they've already added their card info to it)
might then feel reassured about the handling of their information.

However, that example also demonstrates the use of a subtle misrepresentation.
People might reasonably believe that they have made a purchase on this website before, because the site appears to already have their payment information, when this is not necessarily true.
In the case where the user *has not* bought anything from the site before, pressing the pay button and proceeding through the payment flow reveals lots of information about the user to the site which the site did not previously have. Yet the appearance of the button makes the user believe that the site already has this information, and that the net increase of information about themselves that the site possesses is zero.
That increases the perception that the site is trustworthy in their eyes.
Using that misrepresentation to nudge behavior is the very definition of a deceptive design pattern ([Privacy Zuckering](https://en.wikipedia.org/wiki/Dark_pattern#Privacy_Zuckering), as it happens).

The same arguments might be used for federated login buttons.
Google accounts also presented similar UX for logins, showing a user icon and account name on sites that people had not visited before.
Blocking third-party cookies disabled that feature; this use of fenced frames would re-enable it.
The effect is the same sort of misrepresentation, and may result in users revealing information to sites that they otherwise would not have.

We are also concerned that the abuse scenarios here have not been given due consideration.
The potential for abuse from a good actor here seems pretty strong,
but the potential for this capability to be exploited by a bad actor is potentially far worse.



#### [Web Install API - Same Origin](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
#### What do we do with FedCM reviews?
  * [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
  * [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
  * [FedCM API extension: Button Mode and User Other Account API](https://github.com/w3ctag/design-reviews/issues/935) - @rhiaro, @plinss
  * [FedCM bundle: Continuation API, account labels, custom parameters, scopes](https://github.com/w3ctag/design-reviews/issues/945) - @rhiaro, @plinss

### Breakout E (Europe / China) - [2024-07-31](https://www.timeanddate.com/worldclock/converter.html?iso=20240731T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

#### Recap 

discussion on **fenced frames**

Matthew: mentions issue: [Are ad interactions in the threat model?](https://github.com/WICG/turtledove/issues/990) - has there been any progress on this?

Dan: also noting **alex russel's post** about our cookies finding: https://infrequently.org/2024/07/misfire/ As usual, if you get past the inflamatory language there is some good and useful feedback in here.

Matthew: there aren't alternatives for some things, for others we are working on it... for a lot of the things that work, browsers are punching holes... which is 

Dan: maybe we should ask him for suggested text?

Martin: there are a few things worth drawing on - e.g. tracking moving into requests for people's phone numbers and email addresses... Looking at his post, he says: actionable principles that people could follow, which we don't necessarily have outside of this...  We ask people to use http to connect to web sites - we don't give them access to raw tcp sockets... There's an open debate about e.g. webusb... 

#### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

#### [HTMLSelectElement showPicker()](https://github.com/w3ctag/design-reviews/issues/900) - @LeaVerou, @matatk

Matthew: last things that happened were - we asked for more info on the TAG thread... looking at more use cases... desire for consistency... we didn't get any response... then I posted on the whatwg thread paraphrasing our concerns on there.. No input on that thread at all except for a comment from a web developer... So I don't know if we're missing some other place where this is being discussed... so not much progress. The concern is that the longer it goes on the longer the current behaviour is entrenched.  We might propose to put a note in the spec to expand on any a11y issues. 

Dan: what was the feedback from the web developer?

Matthew: it's about what they think the typical use case is... mostly coming down on one side of that...  The thing we're concerned about is... we've had time to think about use cases one way or the other way but we are concerned with the default...

Matthew: [posted a comment to check on status](https://github.com/whatwg/html/issues/9757#issuecomment-2259862856)

#### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @LeaVerou, @ylafon, @maxpassion

Martin: not a whole lot of discussion since we gave the feedback...

*IETF vs W3C*

Dan: *leaves a note asking Anssi for any update*

#### [JS String Builtins for WebAssembly](https://github.com/w3ctag/design-reviews/issues/940) - @hober, @ylafon

Martin: it's a big one and also not a big one...  really interesting. there was some discussion in Seattle.  But not enough time to get into it...

Dan: is there something that could be brought to our issue?

Martin: not right now... We need help. We need someone who has more context but is not directly connected to the work. It could be that this is non-contraversial in TC39...

#### [Conversion to RGB in VideoFrame.copyTo()](https://github.com/w3ctag/design-reviews/issues/951) - @LeaVerou

#### [Timing Info for ServiceWorker static routing API](https://github.com/w3ctag/design-reviews/issues/958) - @martinthomson, @torgo, @maxpassion

Dan: should we abstain on this one?

Martin: I think saying "pass" would be a reasonable thing... the explainer is pretty good as far as i can see.

> Thanks for raising this issue.  We discussed this proposal in a breakout session and decided that we would decline to review in this case.  This work looks broadly reasonable, but the best course of action we can recommend is to continue to work on having the Web Performance Working Group take up this work.

#### [`noopener-allow-popups` value in COOP](https://github.com/w3ctag/design-reviews/issues/964) - @martinthomson, @torgo

Dan: could this be another *decline*?

Martin: I think it could be ... last I looked, it has a good explainer.. it looks like this sparking conversation in the webappsec working group, That's a good thing.   Really what you need to do is take this to the right working group.

Martin: *writes some text*


> Thanks for highlighting this problem Yoav.  A small breakout group looked at this today and it seems like you have started an interesting discussion with a few people about the topic.  We encourage you to continue that discussion.  The Web Application Security Working Group seems like a pretty natural place to take this work.  For now, we'd suggest that our input to that discussion would not be as useful as that of the people you are already discussing this with, so we're going to decline this review.

