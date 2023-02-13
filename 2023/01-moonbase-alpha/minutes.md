## TAG VF2F "Moon Base Alpha" (DRAFT)
#### 2023-02-06 - 2023-02-08

### Slot: 01a

Participants: Rossen, Sangwhan

1. [Add "Supporting BFCached Documents" standalone guide](https://github.com/w3ctag/bfcache-guide/pull/1)
2. [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809)
3. [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786)
4. [Rewrite the BFCache question](https://github.com/w3ctag/security-questionnaire/pull/144)

See comments in spreadsheet

### Slot: 02a

Participants: Lea, Max, Peter, Rossen, Sangwhan

Present: Sangwhan, Lea, Peter, Rossen, Max

1. [Fix lint issues](https://github.com/w3ctag/design-principles/pull/413)

In which the TAG spends 20 minutes dicsussing spaces vs tabs and does not come to a conclusion.

2. [Make HTML attribute sections consecutive](https://github.com/w3ctag/design-principles/pull/412)
3. [Group "don't reveal {assistive tech,private browsing}" under a common heading](https://github.com/w3ctag/design-principles/pull/411)
4. [Editorial tweaks](https://github.com/w3ctag/design-principles/pull/409)
5. [Warn against getter throwing exception since it is a side effect](https://github.com/w3ctag/design-principles/pull/408)

Discussion about exceptions and side effects in getters and setters. Consensus is that both getters and setters should act like regular properties and avoid exceptions and side effects. When exceptions or side effects are possible a method should be used instead.

6. [Fixing markup](https://github.com/w3ctag/design-principles/pull/405)
7. [New principle: Some APIs should only be exposed to dedicated workers](https://github.com/w3ctag/design-principles/pull/404)
8. [First pass at #11, lots of TBDs](https://github.com/w3ctag/design-principles/pull/403)
9. [New principle: Identity on the web](https://github.com/w3ctag/design-principles/pull/396)
10. [Start developer version](https://github.com/w3ctag/design-principles/pull/386)
11. [New principle: on overloading, for #131](https://github.com/w3ctag/design-principles/pull/372)
12. [Guidance about serialization](https://github.com/w3ctag/design-principles/pull/367)
13. [Restrictions](https://github.com/w3ctag/design-principles/pull/363)
14. [Describe what to do when a feature is temporarily only available on some platforms.](https://github.com/w3ctag/design-principles/pull/357)
15. [First pass on backwards compatibility principle](https://github.com/w3ctag/design-principles/pull/354)
16. [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)


### Slot: 03a

Participants: Amy, Dan, Hadley

1. [Find a voice](https://github.com/w3ctag/ethical-web-principles/issues/79)

Dan: can we close this? 

Amy: we discussed making it a w3c statement so we didn't want to make "from the TAG". 

Hadley: we want them to sign up...

Amy: I agree with some of mark points - speaks to the styleguide issue of passive vs. active voice.

Dan: Maybe we need to be more focusing on "as we, the community, develop and evaluate evaluate new web technology proposals"... That could encapsulate TAG review but also just general activity in the web standards community.

Amy: bit of rephrasing in the intro also in the purpose?

Hadley: next sentence is "to inform wide review" which captures both sides of what you were saying.

Amy: it is a different voice... purpose to principles... incongruous... 

Dan: focusing on purpose... guide "thoughtful development" - very passive. Rather than saying "used by" or "applied by"

Amy: it would help - but it's different from saying "this is a set of things we think should apply to the web platform" - subtly different.  It's a statement of what the w3c community believes about the web platform.  "This is a statement of the ethical principles of the w3c community. Spec developers and authors can use it to guide their development."

Dan: so instead of first sentence of purpose..

Hadley: in favour of the sentiment, but have a memory of wanting to hold off on switching it to a w3c community thing

Dan: we could say it's a statement of the TAG's view of the ethical principles of the w3c community. 

Hadley: embodied knowledge

Dan: I can do a [PR](https://github.com/w3ctag/ethical-web-principles/pull/90)

2. [Say something about resisting interpersonal abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)
3. [Back up each principle with references to previous TAG decisions/experiences](https://github.com/w3ctag/ethical-web-principles/issues/19)
4. [Control & power: change decentralized to not centralized for #54](https://github.com/w3ctag/ethical-web-principles/pull/87)

[we rehassh the exact conversation from last July then find a PR we already made and agree to merge it]

Dan: Lgtm

Amy: i think this is a good middle ground solution

**merged abd closed issue**

5. [Security & Privacy: make principle imperative, for #75](https://github.com/w3ctag/ethical-web-principles/pull/85)
6. [Purpose: Note link with Design Principles, for #37](https://github.com/w3ctag/ethical-web-principles/pull/84)
7. [Complexity as an ethical issue](https://github.com/w3ctag/ethical-web-principles/issues/83)

Hadley: good point from mnot and dbaron... I thouhgt we had some lines in there to encourage simplicity... 

Amy: Web is transparent aludes to it...

Amy: they might acknowledge it's a design principle but there should be soemthing in the ethical principles about it...

Hadley: we [make the case](https://w3ctag.github.io/design-principles/#simplicity) in the design principles from a technical perspective rather than from an ethical perspective... All true but... barries to entry also a factor.

Amy: mark is also talking about the complexity for end users rather than developers... High level covered by control & power...

Hadley: we talked about specific examples.. that would be a way to do that..

Amy: in *transparent* and *control & power* we have stuff.. we could add something to *all people* to address the complexity to end users... 

Dan: what comesm to mind are discussions around prompting, dark patterns, things like what is the UI around web bluetooth.How do you makethat understandable.. or what local storage means 

Amy: "people should not need a high level of technological literacy to engage meaningfully with the web platform."

Amy: *prepares PR*

8. [Honouring expectations](https://github.com/w3ctag/ethical-web-principles/issues/82)

Hadley: also looking at 82... do not surprise users...   Could we wrap that into the PR for #83?

Amy: different people have different expectations...

Hadley: remember a lot of our early pushback on FPS - rationale was that this is not how users understand the web works... Rightfully people don't understand how the web works.  

Amy: consistently, intuitively, and not surprisingly.

Hadley: we sayd "do not introduce breaking changes" - focusing on the change rather than the user...

9. [Protect vs Control](https://github.com/w3ctag/ethical-web-principles/issues/80)
10. [Translation](https://github.com/w3ctag/ethical-web-principles/issues/78)
11. [Not using principles in isolation](https://github.com/w3ctag/ethical-web-principles/issues/76)
12. [Grammatical consistency of principles](https://github.com/w3ctag/ethical-web-principles/issues/75)
13. [Consider the relationship between rights and responsibilities](https://github.com/w3ctag/ethical-web-principles/issues/71)
14. [Consider adding a new principle about providing undiscriminating economic opportunity](https://github.com/w3ctag/ethical-web-principles/issues/68)
15. [Should we talk about interoperability vs "evolution-ability" as a tension / design goal for the web?](https://github.com/w3ctag/ethical-web-principles/issues/61)
16. [Strengthen transparency principle?](https://github.com/w3ctag/ethical-web-principles/issues/60)
17. [Be more specific on stakeholders](https://github.com/w3ctag/ethical-web-principles/issues/59)
18. [clarify status of document](https://github.com/w3ctag/ethical-web-principles/issues/57)
19. [Decentralization vs federation](https://github.com/w3ctag/ethical-web-principles/issues/54)
20. [Publish a built form of the principles](https://github.com/w3ctag/ethical-web-principles/issues/45)
21. [Relationship with Design Principles](https://github.com/w3ctag/ethical-web-principles/issues/37)

### Slot: 03b

Participants: Max, Sangwhan, Yves

1. [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523)
2. [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762)


```
For clarity, we'd like to separate the concerns we have in terms of priority.

1. BLOCKER: Origin model

Looking at https://github.com/w3c/miniapp-lifecycle/blob/main/docs/explainer.md#miniapp-origin the definition of Origin is crucial for following the same-origin policy, to ensure that the page is in a secure context to enable APIs that are only available in such context.

On the Web, it is done cryptographically via TLS and OCSP. In app stores, native applications are using validation done by the app store (like universal link), but this is not a first-hand verification (see the point below about responsabilities of the intermediary).

Note that files contained in the package act as a local cache for content relative to the origin, and as such should be verifiable to ensure that the origin-model is applicable here, even if no HTTP request will ever reach the network but would always be dereferenced to the content of the mini app package.

2. BLOCKER: Package can be modified by the intermediary

As there is no end-to-end cryptographically guaranteed scheme for validating the integrity of the package compared to what the content distributor originally shipped, the current proposal puts the users at the mercy of the app store to guarantee package integrity. We think this goes against the fundamental principles of the web and is a risk. A zero-trust model, such as what was introduced in signed exchanges would mitigate this.

There are notions about digital signatures in the response, but without knowing exactly when the signing happens by who, there isn't a guarantee that the content is as it came from the origin. If there is strong enforcement to guarantee that the signing is done at the point where it leaves the origin (or an equivalent first-party), this would be a way forward.

3. ZIP

Just to be clear on this, this is more of an issue with regards to random traversal of the underlying content of a given payload. For smaller payloads, the codec used for packaging is not as critical, but for something as content-heavy as a game (which can easily grow up to hundreds of megabytes), requiring full download (due to the layout of a ZIP file) would result in a less-than-optimal user experience.

We are empathetic to the choice made here, but if there is a possibility for swapping this out to something that is friendlier to low-bandwidth environments (e.g. following the game example - you don't need stage 2 content of a game unless you actually reach stage 2, and there are no guarantees that the user will play that long) as saving on transmission is beneficial to the user. (It also allows for faster loading, even for users on performant networks.)

An alternative design would be to use Service Workers as a delivery mechanism, and keep the packages light - but this comes at a cost of complicating the developer experience. Alternatively one could argue this is doable with fetch(), but these are high-level alternative approaches one could take to move away from a monolithic package which is suboptimal with ZIP.


```

### Slot: 04a

Participants: Amy, Dan, Hadley, Sangwhan

1. [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726)

*we agreed we need to defer discussion until there us an update or reply to our comment*

2. [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724)
3. [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723)
4. [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342)

[last response explaining updates](https://github.com/w3ctag/design-reviews/issues/342#issuecomment-1355093008)

Amy: the argunment "We think that this is not a departure from how the web has worked for years from a user perspective." - Yes however the point of deprecating third party cookies is to move away from this approach.

Dan: ... and improve conditions fot users... However - they have said that they're moving away from the cookie cases. Still local storage information sharing across origin boundaries..

Hadley: how could that not be used in the same attacks that shared cookies enable?

Dan: there are additional hoops the developer needs to go through to make use of it

Amy: that could be in principle a reasonable mitigation but depends what the hoops are

Dan: storage access api provides cross origin access.. 

> We think that this is not a departure from how the web has worked for years from a user perspective. For many years, third-party cookies have allowed sites to share data with other sites; this experience is not new to web users. The First-Party Sets proposal preserves this data-sharing ability but only in specific non-pervasive-tracking cases, which users may easily audit on the public list or perhaps in browser UI. 

Amy: also I don't think "users may easily audit a public list" is realistic.

Amy: starting to think of FPS as a registry - an open, consumable registry that browsers can make use of or not... 

[reviewing storage access]

[how does FPS play a role in storage access use cases]

Hadley: looking for reasons to override the default storage access block.. eg. you've been there before. So FPS is another reason your browser might choose to ignore blocking and both access the same local storage.

Amy: if that's what they're doing then it's *fine*.... better than doing it behind closed doors only in one browser. But what are advertisers going to use this for - for tracking. How can it be used for tracking?  Let's make sure it can't be used for *pervasive* tracking use cases.

Hadley: also I'm concerned explaining this to [non technical web users]... difference in user experience between user agents... difference in how the web works is substantial...

Dan: I think their point - is that many user agents have something like this and what they're propising a standard approach... 

Hadley: we need to delve into why it's not vulnerable to the same issues as cookies...

Amy: what's the difference between the [spec](https://wicg.github.io/first-party-sets/) and the proposal...   We can say "yes we'll turn this review into a review of the specific spec"...  "User Agent Interaction with First Party Sets"...   

Dan: *discussion of governance issues* - it would need to be multi-stakeholder governance - i.e. not in the GoogleChrome github identity - maybe w3c could play a role?

Amy: There is a w3c registry track...

Hadley: *centralized vs decentralized*

Amy: [a json file](https://github.com/GoogleChrome/first-party-sets/blob/main/first_party_sets.JSON).. the canonical fps list... 

Hadley: evil browses could use their own list...

Amy: yes... 

Dan: but they can do that anyway.

Amy: this being an open standard for the list is ok that browers can consume if they want to. Has a decentralized vibe to it. If registry were run thoruhg w3c it would give more longevity assurance...

Hadley: Let me do a deep dive into what they are proposing...

5. [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747)


6. [web without 3rd party cookies draft](https://github.com/w3ctag/design-reviews/blob/main/reviews/web_without_3p_cookies.md)

Amy: took the feedback from the privacy task force... not to include text on advertising... 

Dan: I think we should be explicit...  "Business models, such as advertising-funded content and services, are generally outside of the TAG's scope."

**some discussion on this and whether we already go into this in EWP**

Hadley: we don't care about the advertising funded content - we care about the tracking and the technologies that compromise the user

**discussion of tracking and unsanctioned tracking*

Amy: actual meaningful consent ... [to be tracked.]

Amy: more complex than "do I want to share xyz to pdq.co (e.g.)"  - how will the data be used, what jurisdictions, how long, etc...

Hadley: all the stuff that GDRP addresses.  Who has it, how long, what penalties, etc... 

Amy: the consent of turning it on and off only scratches the surface...

### Slot: 04b

Participants: Max, Yves

Questions about the use of Get/PostPendingBeacon, why not using the method in a dictionary instead of having two instances? How about ensuring that a PostPB isn't sent twice (like if there is a crash).
Issues about crash recovery, should it be done after a network and/or location change, as it can have privacy implications? after a time limit? Do having a pending beacon impact how bfcache work?
What is the point of forcing a PendingBeacon to be sent, if it is supposed to be sent at the end of the interaction, why not using fetch or a normal beacon in that case?

Why existing mechanism is not reliable and how this new proposed mechnisam solve the not reliable issue? Should the HTML unload event be fixed instead? Could this be solved at the Page Lifecycle level instead of having a new specification?

1. [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776)

### Slot 05a

Participants: Lea, Peter

1. [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289)
2. [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725)

CLsoed as timed-out, no response from submitter.

3. [FYI - Add optional submitter parameter to the FormData constructor](https://github.com/w3ctag/design-reviews/issues/812)

<blockquote>
  
@plinss and I looked at this during a breakout today.

Our thoughts were:
1. We think a positional argument for `submitter` is unintuitive. There is nothing that would indicate that this is a submitter argument when looking at calls to this constructor in the wild.
2. We do agree that a dictionary replacing the first argument would be confusing, though a dictionary for the second argument does not have this issue. 
3. As the SO post, npm module etc indicate, authors often want to convert arbitrary objects to form data. We want to urge the API owners to explore supporting this use case, either by extending the constructor or through a factory method.
  
We do not see any architectural issues with adding the argument however, and do not have any other concerns beyond this API design issue, so we will go ahead and close this.
  
</blockquote>


### Slot: 06a

Participants: Amy, Hadley

1. [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808)
2. [Storage Access API](https://github.com/w3ctag/design-reviews/issues/807)
3. [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798)

[discussion about how Storage Access API and FPS are linked]

Making decisions about whether or not to grant access being left to browsers has advantages of extensibility / pluggableness, but weakens privacy guarantee. Could be a worthwhile tradeoff. Obviously well thought through by SA API.. seems clear how they got to this compromise.

Hadley: looking at the acceptance process for FPS.. 3 sites, tld checking.. does that by default give away rights to all country code tlds? Eg. something local like coop.co.uk .. is that lumped in with coop.de which is unrelated?

Amy: there must be loads of words that exist at many country codes that are completely unrelated. That would be a terrible heuristic to automatically link them. I own amy.gy ..

[Reading this issue](https://github.com/privacycg/storage-access/issues/122) about making it per-page and then reverting back to iframe only. 

Hadley: why is this access *for origin* and how does it apply to the origin? What's different? Oh - requests access to unpartitioned data _on behalf of_ another origin.

Concerns about "legacy" use cases.

> Like the [STORAGE-ACCESS], requestStorageAccessForOrigin(origin) is intended to enable removal of cross-site cookies. It enables developers to re-gain cross-site cookies with additional constraints.

What are the constraints? Are they sufficient?

The CORS restriction doesn't mitigate risks to the user caused by collusion between embedder and embedee, or coercion of embedder by embedee.

[Issues..](https://github.com/privacycg/requestStorageAccessForOrigin/issues)

Where is "user interaction" defined? ... gestures... activation.. defined in HTML5

double keying access is mentioned in S&P but not in spec

Questions to ask about the (requestStorageAccessForOrigin)[https://privacycg.github.io/requestStorageAccessForOrigin/]:

1. What use cases are we explicitly designing for? Why is just using iframes and Storage access API insufficient?
2. What abuse scenarios have you considered, and what are the mitigations for them? [S&P questionnaire](https://github.com/privacycg/requestStorageAccessForOrigin/blob/main/tag-security-questionnaire.md) says, "While this functionality comes with a risk of abuse by third parties for tracking purposes, it is an explicit goal of the API and a key to its design to not undermine the gains of cross-site cookie deprecation." -- how does that work?
3. "Permission grants for storage access are double-keyed" (also from S&P questionnaire) -- but this isn't in the spec?
4. Why do images need access to storage? (Use case seems to be for cookies, images and scripts)

Also, re new first party sets

a) is first party sets now essentially a registry?

### Slot: 07b

Participants: Max, Rossen

1. [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767)

Max: we aer still waiting for the author's feedback. Me and Rossen think we should wait for them to respond, to see if the security concerns have been addressed. 


### Slot: 08a

Participants: Lea, Max, Peter, Rossen, Sangwhan

1. [Try to briefly state the difference between fulfill and resolve](https://github.com/w3ctag/promises-guide/issues/42)
2. [Add links to promise related terms](https://github.com/w3ctag/promises-guide/issues/67)
3. [Add more advice on when not to use Promises](https://github.com/w3ctag/promises-guide/issues/65)
4. [guidance on what error to specify is used when a promise is rejected](https://github.com/w3ctag/promises-guide/issues/60)
5. ["A promise resolved with" can unexpectedly run JavaScript](https://github.com/w3ctag/promises-guide/issues/56)
6. [Are unresolved promises rejected prior to a window.unload event?](https://github.com/w3ctag/promises-guide/issues/44)
7. [The `addBookmark()` example violates this guide's own advice](https://github.com/w3ctag/promises-guide/issues/41)
8. [Provide some terms to block in parallel steps.](https://github.com/w3ctag/promises-guide/issues/36)
9. [Give guidance on how to migrate void-returning callback APIs to promise-returning](https://github.com/w3ctag/promises-guide/issues/24)
10. [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791)


### Slot: 09a

Participants: Dan, Hadley, Max

1. [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760)



2. [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744)

Max: they have a number of explainer documents now... Some extensions of the current API... to improve the user expeirence. I spent some time looking at this. First one is about displaying media - used to avoid when the user has video conferencing - sometimes they accidentally capture their own image which causes a problems - this one address this case.

Dan: the documented multi-stakeholder response is positive across the board.  Great to see that and great to see that this is documented well.

Sangwhan: all of this is stuff I use on a daily basis... Contextually all of these features are "work from home" specials... lot of WebRTC screensharing capabilities expedited because there was a gap. Package of little features. Make Work from home more doable from webrtc... E.g. sharing a youtube video in another tab.  Switching between different tabs when you're sharing your tabs... "hall of mirrors"

Dan: but I love the "hall of mirrors" thing.

Sangwhan: it's expensive, CPU wise.

Dan: fair enough.

Hadley: I'm not hearing any architectural things to worry about.

Dan: doesn't look there are any privacy considerations.

Sangwhan: it has made the web a better platform for real time collaboration.

**consensus to close**

3. [Two changes to Secure Payment Confirmation prior to CR](https://github.com/w3ctag/design-reviews/issues/802)

Dan: UA Activiation requirement change: https://github.com/w3c/secure-payment-confirmation/issues/216 - I can understand it from a user experience PoV.

Sangwhan: double activation requirement - not necessary... 

Dan: How double?

Sangwhan: there's a modal activation dialog - that triggers a user activation...  A lot of payments have redirection based mechanism... You click pay button, something navigates... but what navigates is not the user activation... but security wise i don't think it's a huge issue.. I think this change is fine.

Dan: *reviews security & privacy considerations in their issue*

Sangwhan: I don't have 100% confidence but 90% confident.

Hadley: why?

Sangwhan: the payment ui for confirmation goes outside of the browser window.. difficult to spoof. I don't see a signifigant added benefit by adding activation requirement.

Hadley: they're getting rid of web activiation requiremnet because native ui effectively replaces it.

Sangwhan: the current browsing context whre the activation was initiated - not a new browsing context...  About duration I'm indifferent.  User activation is a low bar.

Dan: true.  It's useful for a lot of scenerios - like malicious permissions requests.

Sangwhan: auto-play videos.

Sangwhan: but in this case it's fine. if there is an activation you don't want to penalize - so you don't want to have that "cooldown" dialog making the user wait to pay.

Hadley: what about GDPR?

Sangwhan: a GDPR requirement to allow users to opt out of storing credit cards. Compliance issues. Don't have anythng to add to that.

Sangwhan: [back to activation] because the activation requirement is gone - if there's a hover - when you hover on this thing you could have a fake payment UI with a low number and then do a switch-a-roo for a larger amount. If you time it really well -  with the delay the user would have an ability to see the change before clicking. Removing the activation requirement would allow bad actors to do this specific thing... 

Dan: feels like they could make the verify button move around...

Sangwhan: bad for accessibility... 

Hadley: something in the UK open banking standard - requires delays so the user takes the transaction seriously...

Dan: I suggest we give this a pass - and that they should incorporate these changes into the explainer including the security & privacy considerations.  Including further guidance to UA developers about the risks. 

<blockquote>
Hi @ianjacobs - this change looks good to us. Thanks for running this by us and thanks to the group for documenting this so well [in the issue](https://github.com/w3c/secure-payment-confirmation/issues/216) including the security & privacy considerations and potential abuse cases.  We would encourage you to document this in the explainer and in the spec as well and to provide some additional guidance to UA developers about the risks and mitigations. 
  
In particular, we were very happy to see the group ask for us to weigh in on last minute changes; given that there isn't anything mandating this in the process.
  
We wish you luck with this. Please let us know if we can help with anything else.
</blockquote>

Dan: [shipped](https://github.com/w3ctag/design-reviews/issues/802#issuecomment-1422225875)

**consensus to close**

### Slot: 11a

Participants: Lea, Rossen

1. [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811)
2. [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748)
3. [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743)

### Slot: 11b

Participants: Amy, Peter, Rossen

1. [WebAuthn PRF extension](https://github.com/w3ctag/design-reviews/issues/806)

Amy: S&P responses are in the issue and they have only answered 4 questions

[discussion that this is probably fine, doesn't add anything to privacy risks]

Peter: if they're talking about e2e encryption and both sides knwo the key have they considered a PKI solution.. but I guess it doesn't matter.. they already have PKI in WebAuthn

[closed satisfied]

2. [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803)

Amy: Still in a CG. Would be nice to know what the path to standardisation for this is. Seems like a good use case.

Peter:I like the idea of user choosing their own IDP. In SAML and OIDC the RP has to trust the IDP that you are who you claim to be. How does it work if you can choose your own IDP that the site has never heard about. Handled elsewhere in FedCM? Worst case scenario I build my own IDP and can claim to be anyone I want to be. Does the site still have to pre-trust the IDP?

Amy: my reading is still that the site is choosing what IDPs to list

Peter: that's not obvious from the explainer

Amy: if that's all this is it was a big deficiency they didn't have this before

Peter: Yeah. To do the sign in you do a call on the browser to get credentials and you provide a list of providers you trust. Looks good to me. Would be nice for a user to choose their own IDP but baby steps. Would be nice to see a diff. What other API changes?

Amy: they do ask for suggestions for better alternatives than onload.

Peter: long discussion in [their issue](https://github.com/fedidcg/FedCM/issues/319)

Rossen: any suggestion as to how you set an order of preference?

Peter: it's up to the UA, the UA knows if you're already signed in or which IDPs you have accounts with. It's the same call to sign in or sign up, would just sign you in automatically. Otherwise it'll prefer ones it knows you have an account with.

[discussion about how browser choice of which IDP to show impacts user preference, and potential viscious circle of use consolidating around a few popular IDPs]

Rossen: how does the UA know the user's preferences?

Peter: "ordered by which benefits the user"

Rossen: so just down to the UA

Peter: Seems open/undecided by the group. How is this going to interact with the proliferation of sites offering to "sign in with Google" that already exists? Without user even clicking login button? No way to query what the browser would choose .. site can already filter which IDPs they prefer when they make the call.. so maybe okay.. just interested in abuse cases

Rossen: next step.. auto sign you in because you're already signed in with your browser profile

Peter: FedCM doesn't let you do that currently

Amy: there is good multistakeholder support so far

Peter: happy to sign off on this. I think they've worked through the onload question themselves.

Amy: discussion about IDP ordering in the [Mozilla issue](https://github.com/mozilla/standards-positions/issues/730). Some options, but UI may not be in scope for the spec. Open conversation they are having, I think this is fine.

[closing satisfied]


### Slot: 12a

Participants: Dan, Yves

1. [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805)
2. [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616)

*nb we had to re-schedule these to next week due to conflicts*


### Slot: 12b

Participants: Amy, Hadley, Peter

1. [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780)

Peter: looks like they are thinking about what I asked about

Amy: looks like the IETF part of this should be progressing soon. Mozilla standards position is still defer.

Hadley: in the explainer there's an extension iframe activation. There's nothing in all of the new iframe stuff we've been talking about.. about impact on how this works?

Amy: there's a bit of potential scope creep coming through in the explainer.. a slippery slope just a little bit more tracing..?

Hadley: we had a discussion with them about hwo damanging creating sets could be, and they came back with reassuring answers. I remember discussing this at length with Tess in 2019.

Amy: earlier review was satisfied with concerns, where concenrs were multistakeholder and dependency on privacy pass. Not moved far on multistakeholder front

Hadley: if the issuer is malicious, they say having an allow or blocklist that the user agent supports can mitigate - the UA can decide not to engage with token issuers not doing nice things

Peter: also a limitation on how many keys a provider can use. At most it can divide people into five buckets. Otherwise the issuer could use a different serverside key for every individual person.

Hadley: I thought they were all unique because they're all one use?

Peter: I don't think so. The client generates a unique random number, runs it through a twist algo, sends to the signer, the signer signs the token and sends it back, theclient untwists it so you still have a valid signature of the nonce that you generated but the server didn't see the number you generated. Later you can redeem this token to another 3p, they can verify it was signed by this server, but the server doesn't have any record of having signed that number

Hadley: they're using blinded an unblinded

Peter: yes, it used to be known as twist. I don't knwo if the APIs restrict how many times a user can redeem a token

Hadley: every redemption is sent to the same token issuer, so they run out over time

Peter: whoever receives the token can tell the issuer the token got used

Hadley: might be able to do a timing attack, but that's about it

PeteR: that presumes a backchannel between the issuer and the site having the token redeemed

Hadley: I think this has come on quite a bit since 2019. I see no reason to hold this up. Worth noting dependency on privacy pass?

[propose closing, check in with others especially Tess]

```
We are looking at this at our W3CTAG face-to-face (Moon Base Alpha).

We see no reason not to go ahead with this, since you have helpfully answered our questions. We note that we have only reviewed the API, not the crypto primitive (which is out of scope), and that this still doesn't seem to have interest from Safari or Firefox.

Thanks, and let us know if we can help further.
```

2. [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240)

Hadley: we talked about how to get this going in w3c process. How do we make this happen?

Peter: various things have been attempted.. 

Amy: do we just need to find a WG?

Peter: I Think so

Hadley: I don't know who that would be. A charter for a new group? 

Peter: not sure it's worth a whole new group, but not sure who else to give it to.

Hadley: any other related work?

Peter: or start a CG

Hadley: there are a number of people on this issue

Peter: I'll do that.

3. [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788)

Amy: no response yet to feedback

[discussion of whether this should be a NOTE]

Hadley: [leaves comment]


### Slot: 14a

Participants: Peter, Sangwhan

1. [FileSystemHandle.remove() for the File System Access API](https://github.com/w3ctag/design-reviews/issues/773)
2. [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772)
3. [Element.checkVisibility review](https://github.com/w3ctag/design-reviews/issues/734)
4. [Review request on `blocking=render` attribute for scripts and stylesheets](https://github.com/w3ctag/design-reviews/issues/727)
5. [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711)


### Slot: 15a

Participants: Dan, Sangwhan

1. [Gamepad Extensions API touch input](https://github.com/w3ctag/design-reviews/issues/799)
2. [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795)
3. [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738)

*we had to re-schedule these to next week due to conflicts*


### Slot: 15b

Participants: Amy, Yves, Dan

1. [No-Vary-Search HTTP header](https://github.com/w3ctag/design-reviews/issues/797)

Yves: making assumption for things that are different resources... Precedent for that with information put in .well-known.  If the goal is not putting too much in the network then it should be fine. THings can be cached if a specific parameter is different - key order being different. that should be OK. I didn't see anythng bad for privacy here.

... has to be discussed in the HTTP working group anwyay.

Dan: Does this increase likely hood that 2 users of same browser might get results mixed up - i.e. user2 sees user1's cachad page

Yves: no-vary search - you can specify which parameter to be ignored... So for example a userid should not be in that list.

Dan: about specifying which parameter can be ignored... is my point irrelevant to this spec? A general threat?

Yves: the only scenario where it could work would be user A logs in, it has a parameter with userid, a subset of people trying to log in will hit the cache, and they'll have user a information and not user b

Dan: you have a computer with a shared browser and you've got people logging into a medical service for instance, you don't want user a seeing user b's results... assuming the user's involved are logging in and logging out and have an expectation that if they log out or quit the browser their credentials are not going to be there, but the browser itself might have cached that page.. worst case

Yves: it means in that case someone at the serverside has to set up that header. Which would be difficult for a user trying to con other people to do. If you get access to the server to put those headers you can get all the information you want anyway from the server directly

Dan: does it make sense to close and ask to let us know how it goes in the http wg? or something with more caution regarding user privacy? S&P section seems light

Yves: if you avoid going too much on the network and giving information about the number of hits as it's served from the cache.. saving bytes and metrics as well.. not bad for privacy. Impact will be limited. For caches, CDNs etc, they are not doing conneg very well if at all so I'm not sure they will use that anyway unless they start to implement conneg properly and vary caches. The other point where you can save bandwidth is between the load balancer like cloudflare and the backend servers. You can send your cached copy in that case.

[will close]

2. [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765)

Yves: we are still waiting for them. Still have one month. Ping in April.

### Slot: 16a

Participants: Amy, Hadley, Max

1. [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768)

Amy: as far as I can see they haven't addressed our requests to improve the exlpainer or fill out P&S yet. There was an addition to the explainer but it doesn't add anything we require.

Max: vehicle information is sensitive, related to privacy as well as safety. The comments we left need to be addressed

Amy: [will leave a nudge]

### Slot: 17a

Participants: Amy, Lea, Sangwhan

1. [Autoplay Policy Detection API](https://github.com/w3ctag/design-reviews/issues/810)

Sangwhan: I think this is fine and useful

Amy: me too

Sangwhan: at least one implementation said there's no way it can be synchronous, it must be async. It was a big deal. I saw the positive signals, so curious about that.

```
@leaverou @cynthia and I reviewed this in our virtual face-to-face breakout today. We agreed that this will be a beneficial addition to the web platform, and delighted to see that there are multiple implementers interested. 

We recall that [in the past](https://github.com/w3ctag/design-reviews/issues/439) there was a disagreement about whether this API should be sync or async. Could you share how that was resolved in the end, or if there are any outstanding issues related to this?

We appreciate the quality of your explainer, and plan to add it to our list of examples of exemplary explainers. Thanks for the review request, and we look forward to seeing how you proceed with this work.

```

2. [Pre-CR review: DOM Review Draft — Published 21 June 2021](https://github.com/w3ctag/design-reviews/issues/658)

Lea: This is the same.

Amy: Anne seems to agree with Lea's earlier feedback. Not blocking feedback.

Lea: Linking to a diff is not an explainer. They could write an explainer for this.

[discussion of of how WHATWG process interacts with W3C process]

Amy: we could bring this to Dan and Peter and they might be able to arrange something more sensible with WHATWG if it seems useful.

Lea: [writes comment]

3. [Pre-CR review: HTML Review Draft — Published 18 January 2021](https://github.com/w3ctag/design-reviews/issues/657)

Lea: there is no point to us reviewing this. It's widely implemented by now. The wide review is closed. It was difficult to review via raw HTML PRs. Could have been more readable.

Amy: we can apologise for the late reply, say we have confidence in the WG, but ask that they present something of this size with more notice and in smaller deltas rather than one giant changelog review before CR.

Sangwhan: this is not the first time this has happened. We could insist they do HTML delta early reviews

Lea: [writes comment]

4. [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721)

### Slot: 17b

Participants: Dan, Peter, Yves

0. Council stuff

Tzviya wants to have a chat with group chairs ...

1. [Add something from design principles to each week's agenda](https://github.com/w3ctag/process/issues/24)
2. [Document design review lifecycle](https://github.com/w3ctag/process/issues/22)

Dan: [Makes PR](https://github.com/w3ctag/tag.w3.org/pull/36)
  
3. [This repo needs the standard set of TAG milestones](https://github.com/w3ctag/process/issues/11)

Peter: will work on a script (tooling) to automatically manage milestones across TAG repos.

4. [Look into skynetting the TAG assignment/triage process](https://github.com/w3ctag/process/issues/4)

*closed*

5. [Tooling to link to issues in minutes docs](https://github.com/w3ctag/process/issues/27)

Dan: do we need tooling?  could we make this process instead and a bit of manual work?

*yves to work on this*

6. [Ensure all specs & standards have published user research?](https://github.com/w3ctag/process/issues/26)

*closed as we feel we added material on this*

7. [www-tag@w3.org list vs Github - suggest updating mailing list blurb](https://github.com/w3ctag/process/issues/25)

*Yves to update the [mailing list archive page](https://lists.w3.org/Archives/Public/www-tag/) to reflect the new reality.

8. [Integrating with the WICG process](https://github.com/w3ctag/process/issues/23)
9. [Publications on TR](https://github.com/w3ctag/process/issues/21)
10. [Add documentation for starting a new ReSpec document.](https://github.com/w3ctag/process/issues/17)
11. [TAG GitHub repo spring cleaning](https://github.com/w3ctag/process/issues/10)
12. [Document face to face breakout planning process](https://github.com/w3ctag/process/issues/18)
13. [Create a checklist for initial pass of design review request](https://github.com/w3ctag/process/issues/19)
14. [Create a new design review issue template for internal-to-TAG followup tasks](https://github.com/w3ctag/process/issues/3)
15. [Architectural Decision Records for spec development](https://github.com/w3ctag/process/issues/2)
16. [When do we close "stale" issues?](https://github.com/w3ctag/process/issues/1)
17. [Document the phases of a design review](https://github.com/w3ctag/process/issues/9)
18. [Add an explanation for each label in the design reviews repo](https://github.com/w3ctag/process/issues/8)
19. [Labels: "pending external feedback" needs to be more granular.](https://github.com/w3ctag/process/issues/7)

### Slot: 18a

Participants: Amy, Dan, Hadley

0. Meta - what are we doing?

Amy: list of groups we'd like to hear from and get feedback. Check our blindspots and anything we've missed or phrased badly

* PWE
* PING
* (Some CGs)
* I18N
* A11Y

Dan: going to talk about this at the AC meeting - we should also have a session at TPAC - but ideally we should have done more on this.

Amy: challenge of getting others in the TAG to review...

1. [Consider encouraging investment in evidence over speculation](https://github.com/w3ctag/societal-impact-questionnaire/issues/7)

Dan: Subsection in Introduction?

Something like:

<blockquote>
### Measurability

When answering the questions in this document, we encourage you to discuss the data or feedback you are collecting about the impact of your technologies, and how you can use this to improve benefits to users or mitigate harms caused. Consider what you would measure in order to evaluate the impact your technology is having, and what you would change if the results were not desirable. If you already have processes for measuring impact, summarise these here as well. Note that not everything can (or should) be quantified, and that data collection itself can have a negative societal impact; ensure that in measuring your impact, you are not putting people at risk.

Example: if a local government decides to add separated bicycle lanes and signalling then they should expect fewer bicycle accidents and more use of bicycles.  They can measure that by collecting automated non-identified traffic data and by monitoring published statistics about bicycle accidents.
</blockquote>
  
2. [Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4)
3. [Surveillance](https://github.com/w3ctag/societal-impact-questionnaire/issues/3)

<blockquote>
## How does your new technology open up ways in which people might be surveilled?

How can people using the web be aware of surveillence and tracking risks associated with features of your technology? Can you be explicit about how they know and how they are able to choose?  Does your technology encourage self-censorship, or a chilling effect on society? How are bystanders (people who are not directly using the technology) affected? What societal factors might increase the risk of surveillance?  Who else might be interested in the data you're collecting?
  
Example: before https was widely deployed governments were documented to be pervasively monitoring individuals' web usage.  (Todo: refer to https://www.w3.org/2014/strint/)
  
</blockquote>
  
4. [Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2)
5. [Link to EWP](https://github.com/w3ctag/societal-impact-questionnaire/issues/1)

### Slot: 18b

Participants: Lea, Peter, Rossen

1. [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)
2. [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)

