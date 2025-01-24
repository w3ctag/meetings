# TAG Teleconference
#### 20-22 January 2025

---

## Agenda:

### Breakout B (California / Australia) - [2025-01-21](https://www.timeanddate.com/worldclock/converter.html?iso=20250121T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss
* [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou
* [On-device Web Speech API](https://github.com/w3ctag/design-reviews/issues/1038) - @jyasskin

### Breakout C (Europe / China) - [2025-01-22](https://www.timeanddate.com/worldclock/converter.html?iso=20250122T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman
* [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk
* [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @hadleybeeman

### Plenary Session - [2025-01-23](https://www.timeanddate.com/worldclock/converter.html?iso=20250123T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Appointees discussion with team [30 mins] 
* [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)
* [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)
* [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014)
* [FYI - Web Authentication API: PublicKeyCredential’s getClientCapabilities() method](https://github.com/w3ctag/design-reviews/issues/1016)
* [Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039)
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout B

Present: Peter, Jeffrey, Tess

Regrets:

### Issue closing-palooza

All closed (we proposed closing last week, and received no objections):

* [CSS calc-size() function](https://github.com/w3ctag/design-reviews/issues/955) - @LeaVerou
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

### [On-device Web Speech API](https://github.com/w3ctag/design-reviews/issues/1038) - @jyasskin

None of us have done the homework on this one; we'll read up on it and take another pass next week.

### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

Deferring until Lea's here.

### [View Transition Classes](https://github.com/w3ctag/design-reviews/issues/938) - @martinthomson, @LeaVerou, @plinss

In the [last comment](https://github.com/w3ctag/design-reviews/issues/938#issuecomment-2442312817) on this issue back in October, Lea said we planned to file a CSSWG issue, but there's no link to the issue and we can't find one.

### <abbr title="Any Other Business">AOB</abbr>

#### [Explainer explainer](https://github.com/w3ctag/tag.w3.org/pull/57)

We merge https://github.com/w3ctag/tag.w3.org/pull/57 and https://github.com/w3ctag/tag.w3.org/pull/58.

## Breakout C

Present: Dan, Matthew, Xiaocheng, Tristan, Yves, Hadley, Amy, Sarven (2nd half)

Regrets: Max

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: they've implemented most of our feedback... I want to check what's in the explainer... If we close it we should ask them to have a proper security review...  Threat models e.g. an oversized window with a transparent background could ... [fool the user]..  Having security people look at this would be great. 

*we will look again at the plenary call*

### [Payment link type in HTML](https://github.com/w3ctag/design-reviews/issues/1015) - @torgo, @maxpassion, @hadleybeeman

*we review the feedback*

Hadley: it sounds like this is an individual effort... they've approached the web payments group but not really working with them - not ideal from our PoV.

Sarven: I've noticed there are some other related works out there, e.g., ODRL. I'm trying to understand what we have elsewhere and if that was on their radar or not. Some examples in the [ODRL Information Model](https://www.w3.org/TR/odrl-model/) for payment, e.g., amount. I've asked in https://github.com/w3c/odrl/issues/94 about the possibility for specifying payment location and method. Partly spec'd but not quite speced out. Nothing concrete for payment location. That's primarily what I was trying to investigate from the ODRL community.

Matthew: +1 to Sarven's comments... We were talking about sections we expect in explaienrs earlier.. Alternatives is one of them - this would fit. In the standards position threads they said they were going to add prior art considerations... https://github.com/WICG/paymentlink/blob/main/README.md#prior-art-considerations - links to something else but that's gone... We need to ask them to fix that link...

Matthew: we could say "could you add an alternatives considered section and fix the `<link>` and did you consider 'xxx' as one of the alternatives..."

Hadley: +1 to Sarven's general point... All for including that.  Concerned about single-browser solution...

Sarven: other concern I have ... it's about discovery of the payment location .. it's just a URI... unless there is a structured description behind it, it's going to be hard coded to whatever they want. Not sure sniffing or looking into these URI schemes are sufficient because majority of the web is using HTTP URLs for payment pages. So, besides using custom URI schemes not sure how it'd work.

Matthew: excellent point.

Hadley: +1

Matthew: maybe appropriate for the plenary ... or private brainstorming ... I can draft early feedback...

*some discussion on WICG and what we want to talk about at the f2f*

### [ClipboardChange event API](https://github.com/w3ctag/design-reviews/issues/1017) - @torgo, @matatk

Matthew: we're saying "privacy beats convenience for remote desktop users" and they say the other way around.  They want it to be a seamless experience.  We want the user to have control over their clipboard.

Dan: And I still feel that we need to look outside of the remote desktop case.. There is no argument that in that case, the seamless experience is greatly aided by their approach. However, the issue is with other developers who might seek to take advantage of this ... "bad actors" - but there is also a grey area...   Everyone thinks their application is the only application people are using and everyone thinks their application is the most important application.

Matthew: I like Dan's approach - let's look at the general abuse cases, and how they could be mitigated. This will allow us to make some progress. We're not against remote access apps, but we are _for_ preventing abuse cases. I think this will help us reach some common ground on where the risks are.

Xiaocheng: who's responsibility is it to raise abuse scenarios?  

Dan: we have prompted scenarios ...

Matthew: they don't have an explicit privacy & security section in their explainer, but they do talk about privacy & security in each sub-proposal section, and aligning with existing clipboard API. Our concern is partly with the existing clipboard API too. We have some abuse scenarios from recent minutes here. Has W3C done any thread modelling on this?

Hadley: something about remote desktop as a use cases .. crosses out of the browser and out of the web... not just looking at the browser but looking at what is going on in another OS, which crosses out of the privacy/security boundaries of the web... We keep having this problem when we look at remote desktop use cases. I don't see a way around it.

<blockquote>
First a bit of context: The TAG feels the whole clipboard API platform is more permissive regarding permission than it should be. And we have fed back and will feed back on this in more detail in due course.  Also to be clear, we understand that your position is that this is required for the remote desktop scenario in order to allow for seamless clipboard access. The concern we have is about abuse of this API in *other* scenarios. Remember that web users will also be using other web applications, visiting other web sites, and will be subject to the same risks and attacks as any other web users.

For example: user receives a text message from a scammer purporting to be their bank; user clicks on the URL in the text message; now they are interacting with a web page that looks like their bank but it's really a scam web site; the web site uses this API to scrape any info off the user's clipboard.  
  
  ...
  
</blockquote>

*we agree to come back to this after Matthew looks through our minutes for other abuse cases we've talked about*

### [Final Review Request of seven (7) W3C VCWG Specifications](https://github.com/w3ctag/design-reviews/issues/1029) - @torgo, @hadleybeeman

Matthew: there are change logs for some of them... most of them small changes... appreciate the sentiment about whether we are an HR group or not. We could I guess not comment... 

Amy: they did list change log links in the original question... but high level summary would be more useful

Matthew: JOSE and COSE one is just commits but the other ones all have a revision history...

Hadley: wanted the architectural highlights ... different than a change log having the diff between versions...

Matthew: APA was asked the same thing (in HR) we do have an expert... I can ping them to see if they've looked at it... because APA is looking into it I can see if I can figure out what out of the revision notes if there are architectural items...

*we discuss TAG's role in HR - fodder for Dan's preparing a PR against the HR page*

Amy: We've not really socialised widely that we're not a HR group...  this group has felt blocked by TAG review before so declining might be confusing

Dan: it's appropriate for us to be involved in HR in some situations

Yves: HR better at the early design stage than at the verification / CR stage

Hadley: Jeffrey and I met with this group in TPAC and I told them that this has been an issue for us - getting large specs at the end of the process is less helpful for us and we can be less helpful. Ivan said that's not what the process says. If we decline to review we can do it in a way that says it doesn't make sense for us to get involved in this stage

Sarven: presume it's not all or nothing? If there's even one spec that would benefit from a review we can do it?

Dan: this is why they need to give us a better prompt about what might be architecturally significant for the TAG to review. We don't have the bandwidth to review all the changes to every single spec. We should not be considered part of the exhaustive horizontal review category. We tend to like to do reviews at the beginning of work where we can have more impact.

## Plenary Session

Present: Dan, Peter, Jeffrey, Matthew, Xiaocheng, Tristan, Amy, Yves, Hadley, Sarven

Regrets: 

### Appointees discussion with team [30 mins] 

### Clipboard Feedback

*on 1017*

Jeffrey: I talked to MS and some of the Google clipboard people on Tuesday. Encouraged them to update the explainer with more explanation... and how clipboard change improves things in Firefox & Safari... I think this event still helps things if you assume user doing a paste ... 

Matthew: (on abuse cases) we need to come up with some others...  We're not happy with the current state... 

*on general topic*

Jeffrey: feedback was .. maybe limit to IWAs... or just installed PWAs... somewhat open to restricting the permission.  Also: part of Blink's decision process is that when other browsers "catch up" then we have to change... As they start to ship this in Blink, we have to look at how to make a change (in Blink) because other browsers behave differently...   They need to make sure they're not encouraging web pages to be written in a way that works only in one browser... 

Jeffrey: the other use case they are looking at - company that's doing "streaming apps" - e.g. use a word processor in another server .. and you interact with an image of it in another window... like remote desktop but not...

Peter: one of the things they were talking about was only in installed apps... last time we talked about it, consensus of TAG was that installed apps shouldn't have special permissions...

Torgo: Agreed. We should revisit that every so often to see if the landscape has changed, especially since installation can be gamed. IWA option sounds more promising to me. Not sure how the UX differs for the user from PWA, but it sounds like they have more scary installation steps. Like Slack, built in Electron, which is chromium-based -- basically a big web app. I think IWA is meant to standardise that approach. I'm still not okay with an installed app being able to sniff my clipboard, but it could be more palatable than a web app being able to sniff my clipboard. I still feel like the OS should be providing me a permission. MacOS, you can say, "I'm ok with zoom recording my screen so I can present", but you can't say, "I'm ok with Chrome being able to access my clipboard". No nuance for that action.

Let's edit and agree on our proposed comment asychronously later today. 

Xiaocheng: More context on the previous discussion?

Torgo: A lot of it is from issue 1017. https://github.com/w3ctag/design-reviews/issues/1017

Xiaocheng: I meant previous discussion on permissions and IWA.

Torgo: absolutely. We also have a design review issue on IWA https://github.com/w3ctag/design-reviews/issues/842

Jeffrey: Also: https://github.com/w3c/clipboard-apis/issues/52#issuecomment-875709431

Torgo: Also also, one of these where we discussed (2020) user gesture requirement for clipboard access. https://github.com/w3ctag/design-reviews/issues/406

It's still an unresolved issue in some ways.

### [User-defined script "entry points" for performance timing](https://github.com/w3ctag/design-reviews/issues/1012)

### [Paint/presentation timestamps in performance APIs](https://github.com/w3ctag/design-reviews/issues/1013)

### [Document-Policy: expect-no-linked-resources](https://github.com/w3ctag/design-reviews/issues/1014)

### [FYI - Web Authentication API: PublicKeyCredential’s getClientCapabilities() method](https://github.com/w3ctag/design-reviews/issues/1016)

### [Delegation-oriented FedCM](https://github.com/w3ctag/design-reviews/issues/1039)

### Breakout Rollup

#### Breakout B

#### Breakout C

*web payment link*

Jeffrey: It's part of the (Chrome) payment team...

Hadley: That's helpful info

Jeffrey: It's not likely to be links that go to web sites... apps as well...

Matthew: we had 2 stages of comment... Sarven had some detailed feedback ... some things missing in the explainers...  Shall we post the initial one...

*we agree to post the initial comment - Matthew to post*

Matthew: we need to talk about opaqueness issue with the URL...

Sarven: summarize - it's about link relation - the target resource is where it would be useul for the user. the question is : is the functionality just about discovering that link, or whether there is something more to it.  Unless there is pre-determined URI schemes that the consuming agent understands... e.g. paypal URI scheme... bitcoin URI scheme... they're covering various areas... but majority of web is relying on http...  With this proposal there is nothing coupled with the destination having any structured info ... e.g. amount. In http cas you don't have info. just a page. Should this provide a URI scheme to show something useful to the user?  ODRL is an example... how to express policies and constraints... 

Jeffrey: that sounds like good concerns... I think there is not intended to be any browser-understandable structure to these URLs... It seems like they are looking at user research ... we could ask for more info about the user flow and links to the user research...  UPI scheme seems to be a big driver - an Indian payment method...

Dan: shouldn't this happen through web payment?

Jeffrey: it's the same people... 

Dan: seems like this should be part of a coherent program of work for payment on the web...

Jeffrey: it feels like they want to use this an experiment and then propose it to the working group.

Peter: or at least ask where do they expect it be standardized...

Sarven: The registration of the link relation ... if they go through WHATWG it's just a detail there.. I know that the HTML spec ... rather than IANA - typically people go through IANA but WHATWG doesn't rely on IANA... as long as it's written down somewhere. As opposed to taking what's defined and going to IANA to register it.  

Torgo: considering payments/money is a highly regulated enviroment, it does feel appropriate to go for IANA registration.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
