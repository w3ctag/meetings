## TAG F2F
##### 07 February 2019

Present: Dan, Alex, Travis, David, Kenneth, Yves, Alice, Tess, Andrew Betts (guest for feature policy discussion), Peter, Hadley, Lukasz

Regrets: 

Scribes: Alice, Tess

---

Agenda:


---


### Feature policy

DKA: Kicking off with Feature Policy, Andrew Betts is joining us from Lisbon

AB: Feature Policy is a brilliant idea, and I would like to help in trying to evangelise it.

AB: However, I am concerned that some policies are semantically hard to understand.

AB: *shares a demo*

AB: This works really well, sort of the hello world - geolocation.

AB: If the policy allows geolocation it works; if I turn off the policy, it geolocates me to 0,0 which is in the ocean

DKA: Did you have to reload the page to apply the policy?

AB: Admittely I am using an iframe attribute. Generally yes, a reload is needed.

AB: I would like to draw your attention to the lazy-load policy. If I set a policy of lazy-load: none, you'd think my page can't lazy load. But in practice every single element is lazy loaded. The chromium implementation is broken, so my test thinks that it works.

AB: If the policy is disabled, unexpectedly then the spec implies that the image should load immediately (rather than lazily).

AB: Second point is in relation to parameterized policies. This has been thought of as a second phase, bolted on in a way that doesn't take existing policies into account.

AB: This is what prompted me to gett into tthis.

https://github.com/w3c/webappsec-feature-policy/issues/163

AB: This is really difficult to understand. In a world where we don't have parameterized policy, what happens if you specify allowed-image-formats without specifying any specific image formats? ....? Are we at all concerned about this?

AB: All policies currently exist without parameters. Parameterized policies are not yet implemented. Proposal for param policies suggest names like allowed-image-formats which suggests a parameter is necessary. However, existing policy such as lazy-load have suggestions for how they mnight behave in a parameterized world. oversized-images have optional parameter hints, but fall back to a boolean. For lazy-load, the behaviour when it's not parameterized vs when it is parameteried is quite difficult to define.

TL: What might lazy load with parameters look like?

TL: Like, the first N things might lazy load?

AB: https://github.com/w3c/webappsec-feature-policy/blob/master/policies/lazyload.md

AB: "The extra mile" section...

```Feature Policy: lazyload 'self'(off) https://example.com(force)```

AB: So you could force lazyload for other origins. This possibly prompted the development of parameterised policies.

AB: Example: https://github.com/w3c/webappsec-feature-policy/issues/163#issuecomment-459975413

AB: This implies very strongly that all image formats are allowed, but in fact applies the `allowed-image-formats` policy, with no parameter value, to all origins, with... undefined (?) results.

AB: I've gotten feedback that ... too specific.

DKA: Have you submitted these comments to the webappsec group?

AB: I have... 

DKA: I have been promoting the idea that when we're building web technologies we should be thinking about indiv web developers and not solely big web providers and developer astronauts. If we're building things that way things should be understandable in human language.

AB: Singing to the choir. I agree. https://github.com/w3c/webappsec-feature-policy/issues/193

AB: I proposed preload-offscreen as an alternative name for lazyload, because that's what it actually does.

AB: Most policies are *permissive*, they describe a thing you can do. Turning a policy off means I get to do less.

TL: There should be a consistent policy about what a feature policy does. Feature policy should be about taking something which is usually allowed and restricting it.

AB: It's about taking something which is historically allowed, and drawing a boundary around it. It can be explicitly allowed or denied, where previously it was always allowed. 

DKA: This might be intuitive to people who think about policies all day, but it's not intuitive to web developers.

AB: The name eager-loading was proposed, I'm not wild about it. Someone else didn't get the problem.

TL: So the feature policy model is not broken, but some of the naming implies the opposite expectation of what it does.

AB: I also have an issue with parameterised policies.

TL: You don't think that providing more input is good?

AB: I think it's worth having a conversation aboutt the value that parameters provide vs the added confusion..

AB: I am worried about making tthis feature so complicated that we lose the massive benefits we stand to gain, because nobody will want to use it.

DB: I had a chat with Anne that was along these lines. Anne had some concerns around complexitty that were slighly different. He was concerned about confusion around inherittance and how developers can introspect. I can't really represent his concerns. 

DB: I agree that feature policy is imprtant and that we should be looking more into this.

TL: Parameterisattion seems really powerful. You could provide lots of fine grained detail. Struggling to find examples where that is valuable.

TO'C: Geolocation granularity. Country level vs. local.

TL: So what if we just had two feature policies: geolocattion-coarse and geolocation-fine.

TO'C: I could allow my contentt fine access but my advertisers coarse access.

DB: Payment processing needs to know country, but you want to make sure it doesn't know more than that.

AB: Sure. These do seem kind of niche use cases on top of something that's really valuable - the ability to turn geolocation off completely. 3rd party prompts invoking user permission prompts. Tthe parameterisation on these properties are ill thought through and adding unnecessary complexity.

AB: I agree that use case is complettely valid and does make sense, I am not convinced it is worthwhile to add the extra layer of complexity. 

TO'C: I agree it's a trade-off: complexity is a cost. There is at least one benefit. Weighing tha tis hard.

AR: We've been asking this team to unify these features a bitt. We may have helped create this tension.

AB: The range of different media in which feature policies are defined is spectacular. google docs, pull requests, various spec formats.

DB: ..value of asking nott just for an explainer but also a spec doc ...

AB: Framework specification is well defined, but then they can use the mechnism of their choosing to define policies, and sometimes they are defined in a single paragraph

TO'C: Someone asked "Are you expecting TAG vigilance to be the mechanism of sanity".

AR: If we're going to be put on the beat, someone should let us know.

DKA: Andrew, could you write a finding?

AR: A design principle contribution.

TO'C: TAG could ask webappsec to ... a finding seems overkill. We, the TAG, could file an issue with webappsec to say here are some issues. A finding feels like an escalation path.

AR: Feels like a distraction.

DKA: How can we best action this?

AB: To briefly explore a finding... the relationship of framework specifications with ttheir individual elementts/policies/items, framework items, to define the undefined: if you are writing a framework specification you need some kind of process, registry, around the items that your framework wraps. We don't need to solve this problem.

DKA: that could be a valuable addition to design principles.

TO'C: I could imagine asking in a questionnaire about a cambrian explosion of poor quality exttensions.

DB: We had a discussion about registries about two years ago, punted itt to the AB.

TL: Question was around.... 

TO'C: Historically, registries have not worked well. CSS snapshots. Has anyone ever looked at them?

AR: Keeping up with CSS is a different issue..

DKA: How can we help. If we want to encourage adoption of feature policy, make it more usable to individual developers, we can maybe help ... 

TL: TTwo actionable things: get the design guidelines issue filed. Explore how to collect framework items. Second, inventory of feature policies and review for consistency.

AB: If I may raise this issue to a higher level of abstractions: Client Hints.

All: Yes.

AB: Opens the floodgates of whatever you want to add to the spec. Similar problem.

DKA: Outputs of that discussion?

TL: *** Will raise an issue ***

DKA: How do we action a review of feature policy policies? Open a design review? Sounds like a design review thing. Maybe Andrew could open up the issue in our design review repo.

AB: *** Will file a design review mentioning TAG request ***

*laughter*

DKA: *** Will whatsapp AB re above ***

AB: We didn't get far on parameterised policies.

AR: You've raised big issues. Seems compelling to me.

AB: Naming inversion?

AR: Yep.

AB: That feels clear cut to me. The parameterisation seems like something we should tthink about. Do we devalue the ... didn't seem clear cut to me.

DKA: What else can we discuss...

DKA: We have something to focus on, we have some work to do here. Andrew, anything else on your mind?

AB: Primary issues - it's a really important spec that we should make sure to get right.

### Privacy and Security self-check

DKA: Reviewing document at https://w3ctag.github.io/security-questionnaire/

### Never-Slow Mode

AR summarizes some recent work on time-to-interactive perfomance analysis

AR: Alex Russell was wrong.

DA: Question re: your TLS analogy. We had multivendor consensus that something needed to happen. How do your ideas here become a multi-browser thing? How can we promote these ideas across browsers and across the web?

AR: The TAG can help with this. It's difficult to make this case.

DA: What about the Web Perf WG? Are they working on performance budget?

AR: ... (could someone summarize?)

TL: We don't want to put up a barrier that disincentivies content authors from publishing on the web

AR: The TLS effort had a motivating event (the Snowden incident); it's unclear what the motivating event would be here.

DB: How much of a problem is on the people with primary responsibility for the site, or how much of it is on external business factors etc.?

AR: Lots of work happening for ad attribution. First-party code also very bad (large number of unnecessary polyfills etc.)

DB: (Example of a news site that dropped 3rd party content for GDPR reasons, huge performace win)

DA: It's interesting that NSM is a defacto ad blocker. What about applything these restrictions only to 3rd party code

AR: Most of the weight is first-party

SM: You need 3rd party code for things like federated login, etc.

KRC: Is this people not conditionally loading polyfills?

AR: Yes.

KRC: Isn't this also a problem with frameworks? (That load polyfills)

AR: Those are usually conditional loads

DA: Do we need a "use polyfill.io" TAG finding?

SM: Maybe a finding about bloat on the web?

KRC: How would a finding make a difference?

DA: The Securing the Web finding made one.

DA soliticts volunteers to edit such a finding

KRC and SM volunteer; AR may help as external contributor

## Breakout Team AWESOME:

### Scroll-linked Animations #330

Satisfied with repsonse to our review comment. Scheduled for deeper review in mid-March.

### [Wide gamut support for Canvas/OffscreenCanvas/ImageBitmap](https://github.com/w3ctag/design-reviews/issues/315)

DB: SRGB is a limited color space that doesn't include *all* that we can see.

DB: Colors are in 3 dimensions. If you ignore limenance (taking one dimension from the equation), you can model colors on a two-dimensional space.

<DB draws a circle from Red (Infra-red) to Violet (UV), and shows how RGB fits inside the triangle>

DB: RGB primaries didn't often fit close to the edge of the circle.

DB: Web likes to pretend that sRGB is *the way*, but some web devs want to run new colors through other features like Canvas, etc.

TO: As first step in a UA, you might support images in wide-gamut, but then when you paste that into Canvas (which assumes RGB data), how is that translated?

TO: Also size concerns about wasteful 32-bit packing...

TL: So, like encoding, we're wanting a UTF-8 that can handle the range, but need conversions?

DB: Except that encodings are a defined space, we're talking about the limits of human vision.

DB: Basic problem, we need to pass data around what color scheme you're in, and sometimes convert between them.

### [Temporal](https://github.com/w3ctag/design-reviews/issues/311)



## Breakout Team Modest:

### Form Participation API https://github.com/w3ctag/design-reviews/issues/305

Discussion on whether there is any privacy issue - consensus that the checklist filled out is accurate (no to most)

Dan: I think the user need / benefit should be more adaquately explained in the explainer

Alex: how do I get access to the internals of form elements? this proposal does not do that side of things. only gives you access to check validity and reporting validity.

### [User Activation API](https://github.com/w3ctag/design-reviews/issues/300)

Alice: keyboard users are only implicitly supported - this is a broader issue

### [Priority Hints API](https://github.com/w3ctag/design-reviews/issues/241)

[Hadley and Lukasz re-join]

Lukasz: looked at the included security/privacy section, provisionally ok. Thought not exactly what I thought of. Maybe I should write a separate post.




## Back to Plenary

### [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198)

DA: Is anyone present familiar with the changes since we looked at this before?

( The room takes 10min to review the revised explainer : https://github.com/WICG/trusted-types )

Lukasz: pretty radical change but probably among the most promising for fixing web application security these years....  

TL: Seems like they have reduced the scope in terms of number of types. I like the feature policy type - you can say you require trusted types for the system to execute your code.

TL: I'm kind of curious how you get a trusted type.

DB: Seems like there is a race to register policies because you can land-grab the policy names.

Lukasz: ...problem (refering to david's comment)... when you assume security is based on registration of policy...

1.3 use cases ... only one use case now, the templating system -  looks like it would scale well... in case of megasize web applications

DA: meta-level concern: "trust" is such an overloaded word

HB: (reads previous TAG feedback on naming this)

TL: "brokered"

DA: it should say "this is what we mean and don't mean by trust in this case"

DA: this is similar to the usability of feature policy as discussed earlier today

DB: "policy-checked types"

HB & TO like "policy-checked types".

HB: My worry with "trusted" is that implies having evaluated and decided something is okay. It may make sense with our current ways of doing things, but in the future might not-- but the name would still say "trusted." I'd rather the name explain what has been done (like policy checking), allowing the developer to make an informed decision about how to understand/use it. 

TO: It (policy-checked types) surfaces that you still need to provide the sanitizer code yourself

Lukasz: things that your webapp can digest well...

... "This document defines Trusted Types - an API that allows applications to lock down DOM XSS injection sinks to only accept non-spoofable, typed values in place of strings"

... "We introduce the following list of Trusted Types indicating that a given value is trusted by the authors to be used with an injection sink in a certain context"

DA: captures this in a comment on the issue - https://github.com/w3ctag/design-reviews/issues/198#issuecomment-461313122

TO: I think the problem space is complicated. Large site engineers may benefit from this...

David: Library writers will use this.

Alice: WPT tests don't function well as example code/documentation, and that makes me sad.

Travis: there should be sample code and less webidl

TO: XSS attacks succeed against poorly-written sanitizers. This proposal is about how to hook your sanitizers up, not how to write better sanitizers

AB: It's not about providing a guarantee, it's about reasoning. In a world where each sink is locked down to just trusted types, security folk can just review the policy impl, and not every call site.

[Lots of positive vibe.]

(Discussion: do we need a call on this?)

### Privacy & Security Questionnaire

TO'C: Issue with two distinct issue trackers. 

DKA: PiNG repo, file a bug goes to our (w3ctag) version. Also, all agreed too much introductory material. I sent a PR which reduces the amount of detail and simplifies the language. It could also be a lot more friendly. mkwst tends to write short, to the point, clear language and we need a similar style here.

DKA: I'm going to do another PR on the intro doc and edit down again. We felt that the threat model section ...

TO'C: The threat model section is super useful to understand as you're going through, but including it as front matter makes it take longer to get to the first question, and we need to make it as easy as possible to incentivize people to fill in the questionnaire. Can still have internal links to this information.

AR: Could be in a separate document?

DKA: Would rather not a separate document.

TO'C: More of a glossary.

HB: I keep going back to what the user needs are. They will want threat modelling as reference material, but they will want to start with the questions.

TO'C: When I hit the first question that I don't understand, I will be wanting to click a link to find out what I don't understand.

DKA: Other issue is that there is no question about how the user will experience the permission request, and how it will interact with other permission requests. There was a permission workshop, but no report has been produced. I asked Jo Franchetti from my team to weigh in...

YL: Sam said he will do it.

DA: expect more PRs on the document. should we have a separate, more focused call in the next few weeks?

LO: some of these concerns are the same as were raised in paris. we planned to take these concerns back to the community. i still believe we should do this. i've worked against inflating the document more. i wonder if we want to reduce the length of this document, or split it into two

DA: i think we should have one document. we or others could create a separate tool that presents the material in a friendlier way, for spec authors or web developers.

LO: Please be light on content reduction

LO: should we seek feedback from the community before making these changes?

DA: edits first, then solicit wider feedback. we'll iterate from there.

LO: should we merge § 1 (intro) and 2 (how to use ...)?

DA: also swap §3&4

Lukasz: merge section 1/2 (and simplify a bit) kind of. Swap 3 & 4.

Tess / DKA: +1

LO: re: "drop the feature", this dates from the mwest era of the document

AR: i object to the antagonistic nature of the language, not the sentiment (that feature removal may be the right thing to do in some circumstances). our goal is to help people make this risk assessment.

DA: how would you reword this to be less antagonistic?

LO: what is the objection?

AR: the current working treats the reader like they are stupid

DA: Tess, will you take an action item to revisit this wording?

TO: Yes. (I'll wordsmith with Jason.)

LO notes that multiple user agents have dropped features for such reasons

DA returns to the question of having a followup call in february with a more focused group including PING representatives, say in 2 weeks

∎













