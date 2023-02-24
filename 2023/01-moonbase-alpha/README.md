# Virtual F2F: Moonbase Alpha

The TAG held a virtual face-to-face the week starting 30-Jan-2023.

The schedule consisted of 18 scheduled break-outs (and 9 read-out sessions) across 3 time zone groups.

* Full **[minutes](minutes.md)**.

The TAG closed 12 design reviews in this meeting:

* [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780)
* [Autoplay Policy Detection AP](https://github.com/w3ctag/design-reviews/issues/810)
* [Storage Access API](https://github.com/w3ctag/design-reviews/issues/807)
* [No-Vary-Search HTTP header](https://github.com/w3ctag/design-reviews/issues/797)
* [Pre-CR review: DOM Review Draft](https://github.com/w3ctag/design-reviews/issues/658)
* [AbortSignal.timeout()](https://github.com/w3ctag/design-reviews/issues/711)
* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803)
* [WebAuthn PRF extension](https://github.com/w3ctag/design-reviews/issues/806)
* [Two changes to Secure Payment Confirmation prior to CR](https://github.com/w3ctag/design-reviews/issues/802)
* [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744)
* [FYI - Add optional submitter parameter to the FormData constructor](https://github.com/w3ctag/design-reviews/issues/812)
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725)

In addition, the TAG made updates to the design principles document:

* [Change guidance about dictionaries to cover all optional arguments](https://github.com/w3ctag/design-principles/pull/416)
* [Add new principle for sync() vs async()](https://github.com/w3ctag/design-principles/pull/417)
* [Fix more lint issues](https://github.com/w3ctag/design-principles/pull/418)

The TAG inaugurated a new guide document on **Back/Forwards** Cache (thanks to contributor Rakina Zata Amni from Google and thanks also to Domenic Denicola from Google and Anne van Kesteren from Apple for their reviews of this material).  We welcome community feedback in this area.

* [BF Cache Guide](https://w3ctag.github.io/bfcache-guide/)
* [Updated material in Security & Privacy Questionnaire on BF Cache](https://github.com/w3ctag/security-questionnaire/pull/144)

The TAG also left substantive feedback on a number of ongoing design reviews, notably the review for [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523#issuecomment-1427697804).

We also updated our [TAG work mode](https://tag.w3.org/workmode/) document to provide more transparency about how the design review process works, including how we “triage” new reviews and how we use labels and milestones during the course of reviews.

## 24 breakouts and 233 issues

### Slot: 01a

Participants: Rossen, Sangwhan

1. [Add "Supporting BFCached Documents" standalone guide](https://github.com/w3ctag/bfcache-guide/pull/1)
2. [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809)
3. [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786)
4. [Rewrite the BFCache question](https://github.com/w3ctag/security-questionnaire/pull/144)
### Slot: 02a

Participants: Lea, Max, Peter, Rossen, Sangwhan

1. [Fix lint issues](https://github.com/w3ctag/design-principles/pull/413)
2. [Make HTML attribute sections consecutive](https://github.com/w3ctag/design-principles/pull/412)
3. [Group "don't reveal {assistive tech,private browsing}" under a common heading](https://github.com/w3ctag/design-principles/pull/411)
4. [Editorial tweaks](https://github.com/w3ctag/design-principles/pull/409)
5. [Warn against getter throwing exception since it is a side effect](https://github.com/w3ctag/design-principles/pull/408)
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
2. [Say something about resisting interpersonal abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)
3. [Back up each principle with references to previous TAG decisions/experiences](https://github.com/w3ctag/ethical-web-principles/issues/19)
4. [Control & power: change decentralized to not centralized for #54](https://github.com/w3ctag/ethical-web-principles/pull/87)
5. [Security & Privacy: make principle imperative, for #75](https://github.com/w3ctag/ethical-web-principles/pull/85)
6. [Purpose: Note link with Design Principles, for #37](https://github.com/w3ctag/ethical-web-principles/pull/84)
7. [Complexity as an ethical issue](https://github.com/w3ctag/ethical-web-principles/issues/83)
8. [Honouring expectations](https://github.com/w3ctag/ethical-web-principles/issues/82)
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
### Slot: 04a

Participants: Amy, Dan, Hadley, Sangwhan

1. [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726)
2. [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724)
3. [Review request for TURTLEDOVE](https://github.com/w3ctag/design-reviews/issues/723)
4. [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342)
5. [Shared Storage API](https://github.com/w3ctag/design-reviews/issues/747)
### Slot: 04b

Participants: Max, Yves

1. [Early Design Review: Pending Beacon API](https://github.com/w3ctag/design-reviews/issues/776)
### Slot: 05a

Participants: Lea, Peter

1. [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289)
2. [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725)
3. [Spec review for CSS Nesting](https://github.com/w3ctag/design-reviews/issues/791)
### Slot: 06a

Participants: Amy, Dan

1. [requestStorageAccessForOrigin](https://github.com/w3ctag/design-reviews/issues/808)
2. [Storage Access API](https://github.com/w3ctag/design-reviews/issues/807)
3. [Early design review: Document Picture-in-Picture](https://github.com/w3ctag/design-reviews/issues/798)
### Slot: 07b

Participants: Max, Rossen

1. [Multi-Screen Window Placement on the Web - Initiating Multi-Screen Experiences](https://github.com/w3ctag/design-reviews/issues/767)
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
### Slot: 09a

Participants: Dan, Hadley, Max

1. [COOP: restrict-properties early review](https://github.com/w3ctag/design-reviews/issues/760)
2. [Collection of Screensharing-related UX Hints](https://github.com/w3ctag/design-reviews/issues/744)
3. [Two changes to Secure Payment Confirmation prior to CR](https://github.com/w3ctag/design-reviews/issues/802)
### Slot: 11a

Participants: Lea, Rossen

1. [Web Content Accessibility Guidelines (WCAG) 2.2 2023-01-30 > 2023-02-24](https://github.com/w3ctag/design-reviews/issues/811)
2. [View Transitions API](https://github.com/w3ctag/design-reviews/issues/748)
3. [The Popover API (previously Popup)](https://github.com/w3ctag/design-reviews/issues/743)
### Slot: 11b

Participants: Amy, Peter

1. [WebAuthn PRF extension](https://github.com/w3ctag/design-reviews/issues/806)
2. [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803)
### Slot: 12a

Participants: Dan, Yves

1. [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805)
2. [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616)
### Slot: 12b

Participants: Amy, Hadley, Peter

1. [Private State Tokens (formerly Trust Tokens)](https://github.com/w3ctag/design-reviews/issues/780)
2. [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240)
3. [Review of IMSC-HRM](https://github.com/w3ctag/design-reviews/issues/788)
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
### Slot: 15b

Participants: Amy, Yves

1. [No-Vary-Search HTTP header](https://github.com/w3ctag/design-reviews/issues/797)
2. [Wildcards in Permissions Policy Origins](https://github.com/w3ctag/design-reviews/issues/765)
### Slot: 16a

Participants: Amy, Hadley, Max

1. [VISS (Vehicle Information Service Specification) 2 Core and VISS 2 Transport](https://github.com/w3ctag/design-reviews/issues/768)
### Slot: 17a

Participants: Amy, Lea

1. [Autoplay Policy Detection API](https://github.com/w3ctag/design-reviews/issues/810)
2. [Pre-CR review: DOM Review Draft — Published 21 June 2021](https://github.com/w3ctag/design-reviews/issues/658)
3. [Pre-CR review: HTML Review Draft — Published 18 January 2021](https://github.com/w3ctag/design-reviews/issues/657)
4. [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721)
### Slot: 17b

Participants: Dan, Peter, Yves

1. [Add something from design principles to each week's agenda](https://github.com/w3ctag/process/issues/24)
2. [Document design review lifecycle](https://github.com/w3ctag/process/issues/22)
3. [This repo needs the standard set of TAG milestones](https://github.com/w3ctag/process/issues/11)
4. [Look into skynetting the TAG assignment/triage process](https://github.com/w3ctag/process/issues/4)
5. [Tooling to link to issues in minutes docs](https://github.com/w3ctag/process/issues/27)
6. [Ensure all specs & standards have published user research?](https://github.com/w3ctag/process/issues/26)
7. [www-tag@w3.org list vs Github - suggest updating mailing list blurb](https://github.com/w3ctag/process/issues/25)
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

1. [Consider encouraging investment in evidence over speculation](https://github.com/w3ctag/societal-impact-questionnaire/issues/7)
2. [Responsible AI / algorithmic bias](https://github.com/w3ctag/societal-impact-questionnaire/issues/4)
3. [Surveillance](https://github.com/w3ctag/societal-impact-questionnaire/issues/3)
4. [Examples](https://github.com/w3ctag/societal-impact-questionnaire/issues/2)
5. [Link to EWP](https://github.com/w3ctag/societal-impact-questionnaire/issues/1)
### Slot: 18b

Participants: Lea, Peter, Rossen

1. [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)
2. [Review the HTML spec's treatment of focus](https://github.com/w3ctag/design-reviews/issues/468)
