# TAG Teleconference
#### 16-18 September 2024

---

## Agenda:

### Breakout B (California / Europe) - [2024-09-16](https://www.timeanddate.com/worldclock/converter.html?iso=20240916T163000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk
* [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou
* [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman
* [Early Design Review: Lightweight FedCM](https://github.com/w3ctag/design-reviews/issues/986) - @rhiaro, @plinss
* [FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @torgo, @hadleybeeman, @plinss

### Breakout D (California / Australia) - [2024-09-17](https://www.timeanddate.com/worldclock/converter.html?iso=20240917T220000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @hober, @martinthomson
* [Entering IPv6 Zone Identifiers in User Interfaces](https://github.com/w3ctag/design-reviews/issues/989) - @martinthomson, @jyasskin
* [Call stacks in crash reports from unresponsive web pages](https://github.com/w3ctag/design-reviews/issues/981)

### Breakout E (Europe / China) - [2024-09-18](https://www.timeanddate.com/worldclock/converter.html?iso=20240918T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk
* [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou, @nitot
* [WebXR Device API (delta/aiming 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/983) - @torgo, @matatk

-----


## Breakout B

Present: Dan, Peter, Yves, Matthew, Jeffrey, Amy, Hadley, Tess, Lea

Regrets: 

### TPAC Planning?



### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

Matthew: they replied to our questions.. added 2 questions to the explainer... I fully read them. The main thing we were concerned was relationship to RenderCapacity API...  It's slightly moot because that one has been shelved... They did say how it compares. Both of these proposals will tell you about audio glitches but only this one will tell you about load issues with audio pipeline as a whole...  THis makes it more secure (they say). They are aware of the side-channel attack and have proposed some mitigations... Proposed to use some kind of rate limiting thing. It seems reasonable to me - but Tess might have a more expert opinion.

Peter: ... side channel being audible to the user ... not necessarily true...  I don't think it changes much. Mitigation is probably still fine.

Dan: Multi-implementer story?

Jeffrey: they haven't requested reviews from other engines... still early...

Dan: think this should be part of our feedback...

Matthew: do we think it's solid enough to take the audio wg? Seems like our answer is yes.  I just am not sure on whether the mitigations are sufficient... They've descried in the explainer... they want to use something *similar* to compute pressure... 

Jeffrey: I think we should send them to the PING.

Dan: +1

Matthew: agree. they did fill in the privacy & security questionnaire.. They did it as a google doc... https://docs.google.com/document/d/1wGv_mr7Lgg2w-6PuKDrcScoa8IvYAOW3PMTFW85O3Gw/edit#heading=h.d6giaiodx3q3

Peter: I think it's fine to close... as **satisfied** and take to WA wg and loop in PING.

Tess: +1 

<blockquote>
Thanks for the extra info you added to the explainer. We don't see any architectural problems with this. This should go to the web audio working group for further work. Please also talk to the PING group regarding the risk mitigation.
</blockquote>

*Matthew leaves the closing comment*

### [Web Install API - Cross-Origin](https://github.com/w3ctag/design-reviews/issues/946) - @hober, @LeaVerou

Jeffrey: I think there's nothing to discuss this week... 

Peter: Ok let's punt...

Jeffrey: to talk to the WICG folks about including it in the discussion at TPAC

### [Controller Documents v1.0](https://github.com/w3ctag/design-reviews/issues/960) - @jyasskin, @rhiaro, @hadleybeeman

Discussion at https://github.com/w3c/controller-document/issues/94#issuecomment-2332584962

Jeffrey: some feedback from them... I'm waiting for the wg to talk about it...

Hadley: if we do decide to drop in on them we should do some coordination...

Peter: marks as *pending external feedback*.

### [Early Design Review: Lightweight FedCM](https://github.com/w3ctag/design-reviews/issues/986) - @rhiaro, @plinss

Peter: any with more context?

Jeffrey: if this could replace fedcm that would be great.. but not evidence either way that it's going to... so swe should support experimenting with it...

*This was discussed in our recent plenary too: https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/09-02-minutes.md#plenary*

Tess: it sounds like the complexity missing is in the "we're not going to need it" category.. if in practice nobody is using it then why do it?

Jeffrey: Sam feels that some IDPs have (legal) requirements...  e.g. changing your name would propagate to all places immediately... remains to be see... 

Hadley: which legal requirements?

Peter: right to be forgotten laws?

Hadley: most legal restrictions are reactive to the work we do, rather than creating boundaries within which we have to operate...

Tess: seems unnecessary to anticipate a regulatory...

Jeffrey: regulators have already said *some* things...  E.g. opt out links... I can ask Sam for more details... I don't know if it changes much about our review of this API...

Hadley: can we more specific about outstanding questions? Outstanding questions in the working/community group?

Peter: In general I feel a bit lost on FedCM, given all the little reviews on it... This to me seems to be "throw all that out and start over" - and leads me even more confused...

Hadley: I also felt that way with next issue - 992.

Peter: that issue talks about fedcm as a trust signal for shared storage... I don't want to see that... Pushes us back to 3p cookie world.

Hadley: seconded (for issue 992)

Peter: other thing that occured: I think one of the biggest problem is lack of consistent support of single sign-**off**. Leads to user confusion about where you're logged in... Feels like leaving it as option means people won'd do it. I wonder if FedCM should require the background comms to make that work.  I'm wondering if making it slightly more complicated to require comms between the IDPs should be a hard requirement from day 1?

Jeffrey: that's a concrete question - lightweight one doesn't allow for single sign-off..

Peter: I think that would be bad.

Hadley: comment looks good.

Peter: do we want to go farther and recommend that single sign-off shouldn't be optional.

Tess: i think not having it is an argument for it not being a total replacement for the heavy-weight one...

Peter: should we close?

Tess: yes I think we should - as it's an early review request...

Peter: I'm fine with closing it.

Dan: +1

<blockquote>

We're happy to see this sort of experimentation with the FedCM problem space. It looks like there are outstanding questions in the Community Group about whether the Lightweight API will be enough to completely replace the existing proposal. We wondered whether this approach can enable single sign-*out*, and if it can't, that's a strong argument against it completely replacing the existing API. We look forward to the outcome of the testing you have planned.

</blockquote>

*amy to leave the feedback and close*

### [FedCM as a trust signal for the Storage Access API](https://github.com/w3ctag/design-reviews/issues/992) - @torgo, @hadleybeeman, @plinss

Tess: This probably isn't the worst idea... but taking some steps back... peoiple use fedcm because they don't want to create an account on every single thing. Why? They don't use a password manager and don't use passkeys? FedCM is fixing "the wrong problem"...   It's ok - you use fedcm, google knows you have an account there... we shouldn't have got to that place where this is a necessary change...  We should push them towards technologies they can create accounts they don't have to care about... If we're trying to move the web to something more private we shouldn't be encouraging people to use fedcm...

Dan: I use federated identity because there's a relationship... e.g. github to dev.to....

Jeffrey: you're weird. ;-)

Tess: yes. 

Dan: accepted.

Peter: i do agree with your point... the counter-argument is some Fedcm use cases... I also use it as Dan does... Other counter-argument... for some places there is a strong bias for using SSO because it's phishing resistant... That's also mitigated by passkeys, etc... I also question if fedcm is addressing that use case properly...

Jeffrey: Yes we should be pushing people away from fedcm... but none of those impact the answer for this particular issue... Once you've connected identities in some way the 2 sites can be connected. So we should not object to this suggestion...

Peter: One thing I would like to see: FedCM not tied to speciic IDPs. I'd love to run my own personal IDP and use that to log in everywhere... Scared of a FedCM world where only a few top IDPs are used...

Dan: you're weird.

Hadley: I'm with you but if I'm a RP don't I choose who I'm going to trust?

Peter: yes - not sure how to reconcile... FedCM allows you to "bring your own IDP".. but RP cant just trust any old IDP...  

Matthew: +1 to both Peter and Hadley... Just to say that we both briefly touch on this in discussion with Sam ... we did touch on that in this meeting...  [minutes from last f2f](https://github.com/w3ctag/meetings/blob/gh-pages/2024/07-seattle/minutes.md)

Peter: adding friction to log into another IDP...

Dan: should we be encouraging a pattern where web sites don't need people to log in unless necessary...  Thinking of the multiple web experiences I've had recently using web payment where I haven't had to create an account...

Peter: can we decouple that the IDP... similar to trust tokens...

Jeffrey: VCs can do something similar where the issuer doesn't know who you've logged into - except with cooperation you can...

Pater: we can't prevent a back-channel but maybe we shouldn't allow storage access...

Jeffrey: ... for fingerprinting ...  moving to active...

Tess: we don't have a general agreement to change passive to active fingerprinting.. some should do away...

Jeffrey: if we want to take this away, what does it give us?

Peter: I would argue that any valid use case for giving an IDP storage access.. should be given to fedcm itself...

Tess: we want developers to call the storage access API if they want access ... this is saying that in the case where they use fedcm, it resolves faster...

Peter: the valid use cases should be 

*some discussion*

Peter: it should be mediated by the fedcm ... 

Jeffrey: this is in conflict with the frustration with being sent extensions to fedcm...

Peter: I'm also pushing back on all the three dozen extensions... giving them storage access is giving them all of it... 

Dan: what's the use case? the user need that we're trying to solve? 

Peter: yeah - what uses for storage... 


## Breakout D

Present: Peter, Jeffrey, Tess, 

Regrets:


### Writing Assistance APIs](https://github.com/w3ctag/design-reviews/issues/991) - @hober, @martinthomson

Tess: Don't call it "ai". If "ai" is meant to imply something that the developer needs to be aware of, put that "something" into the name or API shape.

Tess: 3 cases that are interesting: Happens right away; takes an expensive network transfer; won't succeed.

Jeffrey: ensureModelFetched(), which could take a long time, followed by useModel(), which is always fairly quick.

Jeffrey: Could pass "not if metered" into ensureFetched()

Tess: Is metered-ness exposed?

Jeffrey: I think so, at least in Chromium.

Tess: As a page author, I can imagine these features as nice-to-have. And then, maybe I don't want to cause a download.

Tess: We can encourage developers to do things by shaping APIs in particular ways, so providing the "only if downloaded" option could encourage developers to be more respectful.

Peter: There is the "readily" vs "after-download" option.

Tess: If you initiate the download in one tab, and then start in a second tab, is its first progress event 27%? Do you pretend it's a smaller download?

Peter: Or you make it take the time, but don't actually download anything.

Tess: In which case "readily" doesn't mean much.

Peter: Stepping back, I don't like the whole API. Attributes too much ability to LLMs, they're not good at doing these things. Takes too many resources. Don't think this should be in the browser, at least not yet.

Tess: Partitioned storage means that if 10 websites use large models, you download it 10 times. Also if the browser vendor has its own model, why not provide that as a shared resource?

Peter: Centralization of models + market dominance.

Tess: It's nice UI to make model output visually distinct from human-written text. This generic API won't make sites create a visually distinct appearance for it. Could imagine a declarative approach, with an HTML element that takes text as input and provides default- or mandatory-styled output text. But if you like LLMS, you might object that this makes their output second-class.

Jeffrey: I hear 3 levels of feedback here, and we should provide all of them.

Tess: General skepticism; opportunistically using features without triggering downloads; visual distinctions.

Tess: Imagine extending form features. E.g. input, textarea, and contenteditable could say they're input to one of these things. Think any declarative approach will get rejected, but rule of least power says if we can get the 80% case easily, we should do that.

Tess to draft a comment.

<blockquote>

1. general skepticism (def. want peter's review of this bit)

At a high level, we wonder if these sort of features belong at the platform level at all, and (assuming they do) we worry it may be premature to bake them in.
  
This is a very active area of innovation in the industry, and there are many players buidling <abbr title="large language models">LLMs</abbr> and other such tools. Shouldn't we be sitting back to see if/how web developers incorporate such things into their sites first?

Also, browser vendors are not the only players in this space. Is an architecture that does not allow page authors to select from many possible models the right thing here? For some authors, the built-in/browser-provided models may be good enough. If they find the built-in model(s) limiting, it'd be a shame if there's a huge <abbr title="application programming interface">API</abbr> cliff when they go to switch to a third-party one.

2. well-lit path for "i want to use these features on my page iff model is already downloaded" / "i do not want to cause download"

Consider an author who wants to integrate one of these features as a "nice to have"—if the browser's already downloaded a model, they'd like to take advantage of it, but if the browser hasn't, they don't want to be the cause of a large download on what may be a metered connection. While that's technically possible with your current <abbr>API</abbr> shape, it's not the easiest, most well-lit path. It feels like the extra effort case should be the one that causes the download, and the easier-to-code case should not.

3. visual affordance for users to understand "this text was hallucinated by an LLM", declarative v. imperative tradeoff, Baby Steps

On other platforms which integrate these kinds of intelligence features, there's a clear visual affordance that a chunk of content is the product of a model and not something human-authored. Adding these features purely as JavaScript API means that there's no opportunit for interested User Agents to do the same. A declarative approach which the <abbr>UA</abbr>

</blockquote>


### [Entering IPv6 Zone Identifiers in User Interfaces](https://github.com/w3ctag/design-reviews/issues/989) - @martinthomson, @jyasskin

From last week: `satisfied` with

<blockquote>
  
  Thank you for running this past us. We think you've made the right call in undoing the URI syntax changes from RFC 6874 and excluding web browsers from your UI recommendations.
  
  </blockquote>

### [Call stacks in crash reports from unresponsive web pages](https://github.com/w3ctag/design-reviews/issues/981)


https://github.com/w3ctag/design-reviews-private-brainstorming/issues/1

Jeffrey: I'm generally favorable.

Peter: Will the browser pop up a request?

Jeffrey: I think the developers expect that not, but it could.

Tess: In the extension case, website users probably won't notice what it's revealing. But the UI could just say "these 5 extensions injected code and might be revealed." Don't rely solely on displaying the stack trace.

Peter: There's room for the UA to be smart. Don't want any crash report sent without my consent. Page should say "page requested a crash report", and let me say yes/no.

Tess: Good to let UAs compete on providing the most user-protecting interface. Spec should be clear enough about these concerns that a new naive engineer does something decent.

`satisfied with concerns`:

<blockquote>
  
This looks like a worthwhile piece of information to show to developers. We agree with the privacy worries that these uploads might expose what extensions a user is running. We suspect this privacy risk is avoidable in two ways: First, you could automatically omit stacks if any extensions have injected content scripts. Second, you could prompt the user about whether they want to send the report, with a user-comprehensible explanation of what sensitive information's likely to be sent; for example the list of extensions that injected script.
  
Please continue discussing this in the WebPerf working group and the PING.
  
</blockquote>

### Getting outside design review

Jeffrey: I propose that we make a list of people we're inviting to help with reviews; open the private-brainstorming Github repo to that list; and invite those people to the TAG Slack and open our #design-reviews channel to the TAG Slack.

Peter: Let's discuss in Plenary.

## Breakout E

Present: Matthew, Max, Amy, Tristan, Yves

Regrets: Dan


### [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk

Matthew: there was a reply - there are other implementers than Chrome (Gecko). and BBC have chimed in to say a more generic one would be good. Do we close this?

Yves: do we block closing on the resolution of the issue, or say they've seen our feedback?

Matthew: plenary?

Yves: we expressed concerns - raised as an issue - so closing satisfied with concerns would be good for me. The question is do we want to block on the resolution of that issue. Should ask Martin as well.

Matthew: I agree satisfied with concerns

**discuss at plenary**

### [A layer attribute for layering of linked CSS style sheets in HTML](https://github.com/w3ctag/design-reviews/issues/970) - @LeaVerou, @nitot

Tristan: haven't had chance to look

Matthew: seems like a really big change

Yves: needs careful thinking

**plenary with Lea**

### [WebXR Device API (delta/aiming 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/983) - @torgo, @matatk

Matthew: most of the way through this, PRs are well explained, most not architectural. One is to do harmonization with other specs and I believe them, so that sounds good - feature detection related - found a different way to do parameters so feature detection is the same across specs. I'd sense check that with others. A few small clarifications. A couple of bigger ones which I don't see any concerns with but need more time to look into. One was originally about conveying user intents derived from the OS or the UA in the XR space and it would take into account what the user is looking at at the time, and quite a bit of discussion about how that should work and what it should be called. And one about on screen keyboards that's important and interesting. I might be able to leave some notes this week.

### Review process

Matthew [this in APA](https://www.w3.org/WAI/APA/wiki/Category:Spec_Review) gives us long term tracking over every spec, not per issue. And [eg. this](https://www.w3.org/WAI/APA/wiki/ARIA_in_HTML) lets us see all the times we've looked at a spec, what we thought over time. Be good to see if we could link issues together and get a summary of what we thought last time.

Amy: is that automated?

Matthew: no, that's a downside

Yves: plh is working on labels for spec

Matthew: labels for spec and venue separately would be better if we're getting that. Good opportunity for us to ask next week

Matthew: if in doubt copy what i18n does - I wonder how they track longditudinally. We can ask at TPAC.

### [Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

* Accessibility conformance testing rules - APA review ongoing; could be a small delta but APA didn't review 1.0; worth doing a reasonably thorough review; doesn't say what's changed
* CSS reading flow property - looks a11y related; might relate to some epub stuff; we want a css person on?
* 

## Plenary Session

Present: Tess, Peter, Matthew, Jeffrey

Regrets: Amy, Tristan, Yves, Dan



### Breakout Rollup

#### Breakout B

#### Breakout D

#### Breakout E

##### [Add Skip-Ad media session action](https://github.com/w3ctag/design-reviews/issues/957) - @torgo, @matatk

*general agreement to close satisfied with concerns*

<blockquote>

Thanks for the review request. As this is shipping in multiple engines, and our concerns have been raised in an issue to be addressed in future, we'll close this review.

</blockquote>

##### [WebXR Device API (delta/aiming 2nd CRS)](https://github.com/w3ctag/design-reviews/issues/983) - @torgo, @matatk

Matthew: Coming back to this, I completed my review, and took some input from a colleague; here is a proposed closing (satisfied) comment:

<blockquote>
 
Thanks for your review request&mdash;and for highlighting the changes since last time. Here are a few comments on these changes.

HT @m-alkalbani for assisting with the review.

1. Expose XRSession&rsquo;s granted features ([GitHub \#1296](https://github.com/immersive-web/webxr/pull/1296))

   Looks good!

2. Add support for the isSystemKeyboardSupported attribute ([GitHub \#1314](https://github.com/immersive-web/webxr/pull/1314))

   This Boolean's name starts with 'is' whereas others' names don't seem to. Is there a reason for this, such as consistency with other specs? It seems inconsistent with other parts of WebXR Device API.

3. Clarify getPose behavior with visibile-blurred ([GitHub \#1332](https://github.com/immersive-web/webxr/pull/1332))

   Looks good!

4. Transient intent addition ([GitHub \#1343](https://github.com/immersive-web/webxr/pull/1343))

   This looks good &mdash; but gave rise to a question about an instance of one of the terms used in the [definition of `targetRayMode` enum values](https://www.w3.org/TR/2024/CRD-webxr-20240805/#dom-xrinputsource-targetraymode)...

   Assuming that the `gaze` enum variant is talking about getting input from the direction someone's head is facing...

   The [definition for the `transient-pointer` enum variant](https://www.w3.org/TR/2024/CRD-webxr-20240805/#dom-xrtargetraymode-transient-pointer) states: "Some examples are user intents based on information too sensitive to expose directly such as gaze..." &mdash; however in this phrase, is "gaze" actually referring to input that comes from _eye_ gaze (i.e. eye tracking)? If so, the word "gaze" is referring to two differnet things; would you be able to re-phrase this to make that clear?

5. First draft for adding a property to XRInputSource to say it&rsquo;s visible elsewhere ([GitHub \#1353](https://github.com/immersive-web/webxr/pull/1353))

   This looks good &mdash; but the PR referenced here should be 1352, so the Changes section should be updated.

6. Clarify rgb vs srgb behavior ([GitHub \#1359](https://github.com/immersive-web/webxr/pull/1359))

   We want to keep reminding people to try to align colors between CSS, canvas, and the other drawing surfaces in the platform. That said, that's a long-term project, and we don't expect this incremental change to solve it. Otherwise looks good!

Also...

7. [The definition for `transient-pointer`](https://www.w3.org/TR/2024/CRD-webxr-20240805/#dom-xrtargetraymode-transient-pointer) has a typo; it mentions "W3C design principals" &mdash; I think you mean to reference [Web Design Principle 2.9: Don’t reveal that assistive technologies are being used](https://www.w3.org/TR/design-principles/#do-not-expose-use-of-assistive-tech); if so, perhaps you could include this link.

   That you made the reference, and read the principles, is appreciated!

</blockquote>

#### [DOM state-preserving move](https://github.com/w3ctag/design-reviews/issues/976)

Lea and Jeffrey settled on `satisfied with concerns`:

<blockquote>
  
We consider it a mistake in the platform that element movement is handled by removing and then re-inserting nodes. We would prefer if this effort fixed the existing methods rather than adding new methods. Could the designers invest in some more thorough testing to see if this breaks a significant number of pages, rather than just [assuming](https://github.com/noamr/dom/blob/spm-explainer/moveBefore-explainer.md#changing-the-default-behavior) that it will? If changing all of the element-movement methods does break things, perhaps it would be compatible to change only the newer ones that are methods on `ParentNode` and `ChildNode`. In that case, we think the slight inconsistency between, e.g., `append()` and `appendChild()` is worth the more intuitive behavior on the newer method.

Thank you for bringing this to us. The WHATWG discussion seems like the right place to dig into the compatibility question, so we're happy to let them take it from here.
  
</blockquote>

### External design-review contributors

Jeffrey: Overall proposal:
 1. Give selected people access to https://github.com/w3ctag/design-reviews-private-brainstorming.
 2. Create a new `#design-reviews` channel that's open to members of the TAG Slack. (And deprecate or rename the current private channel.)

Tess: Purposes:
 1. Help with the firehose.
 2. Give people a taste of being on the TAG, so they can decide whether to run.
 3. Give us a taste of their reviews so we know whether to endorse them or ask the Team to appoint them.
 
Tess: Name should be straightforward. People will be wondering if this is a good career move, and the name should sell it.

### Issue Triage
