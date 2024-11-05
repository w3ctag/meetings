# TAG Meetings Minutes - Week-of 19 February 2024

## Call Agendas

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2024/telcons/02-19-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / China) - [2024-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Verifiable Credentials Data Model v2.0](https://github.com/w3ctag/design-reviews/issues/860) - @hober, @torgo, @rhiaro, @hadleybeeman
* [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman
* [ARIA](https://github.com/w3ctag/design-reviews/issues/927) - @matatk, @maxpassion
* [ewp new issue on data harvests](https://github.com/w3ctag/ethical-web-principles/issues/109)

### Breakout B (California / Europe)  - [2024-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo
* [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hober, @hadleybeeman
* [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss
* [Side Panel](https://github.com/w3ctag/design-reviews/issues/903) - @matatk, @plinss


### Breakout C (California / Australia) - [2024-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @torgo

### Breakout D (California / Australia) - [2024-02-20](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Special guest Reilly Grant

* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @LeaVerou, @torgo
* [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou

### Breakout E (Europe / China) - [2024-02-21](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @matatk, @hadleybeeman

### Plenary Session - [2024-02-21](https://www.timeanddate.com/worldclock/converter.html?iso=20240221T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* New TAG Work Mode Proposals
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes


### Breakout A (Europe / China) - [2024-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Matthew, Amy

#### Discussion of Privacy Principles Wide Review
#### [Verifiable Credentials Data Model v2.0](https://github.com/w3ctag/design-reviews/issues/860) - @hober, @torgo, @rhiaro, @hadleybeeman

Amy: I read Manu's feedback.  I think it's fine.  The group have thought about it... However I don't havea  strong opinion about the polyglot issue. And it's clear that Tess does. https://tess.oconnor.cx/2023/09/polyglots-and-interoperability  Manu asked for an official TAG perspective. We have [this issue](https://github.com/w3ctag/design-principles/issues/239)

Dan: one outcome for this could be that we say "no consensus"...

Amy: feels like a debate that has been going on for many years without a wrong or right answer...

Yves: https://www.w3.org/TR/html-xml-tf-report/#conclusions from 2012 - "little consensus"

Dan: worth noting.. it's one of those issues that becomes circular.. the TAG isn't adding any value by getting into this argument

Amy: also vague concerns about malicious issuers, but not sure how architectural that is, not very concrete

Amy: I'll draft a comment, and put it in design reviews chat and ping Tess

<blockquote>
Thanks for your detailed reply, and patience as we work our way through our backlog. Sorry that we missed your CR deadline.

* We have a general concern about the potential harm caused by malicious issuers, but that applies to the whole ecosystem, rather than the data model spec specifically.
* We don't have a consensus position on polyglot formats, and we don't think the TAG can add anything of value by getting involved in the debate in the context of this spec. We note [an open design principles issue on the topic here](https://github.com/w3ctag/design-principles/issues/239).
</blockquote>

#### [Verifiable Credential Status List 2021](https://github.com/w3ctag/design-reviews/issues/874) - @rhiaro, @maxpassion, @hadleybeeman

Amy: feedback from ping is that this could be a cross-origin unique identifier and they should stop. https://github.com/w3cping/privacy-request/issues/127#issuecomment-1932531261  The spec acknowledges the privacy concerns...

Dan: Ok with *satisfied with concerns*

Amy: will make it clear that we're satisfied that you're thinking about this - not because we don't think it needs to be resolved - specifically the privacy issue - not that we don't think it needs to be resolved.

<blockquote>
Thanks for your comprehensive reply, and for your patience while we loaded this back into our collective heads.

We think it's important that you continue to explore and elaborate on mitigations for the privacy concerns raised in this thread, and [in the horizontal review with PING](https://github.com/w3cping/privacy-request/issues/127). We're closing this as 'satisfied with concerns' because it's clear that you intend to do so, though we think it's important that these issues are resolved before the spec goes to REC.
</blockquote>

#### [ARIA](https://github.com/w3ctag/design-reviews/issues/927) - @matatk, @maxpassion

Matthew: APA are looking at this in a slightly different way. We're looking for architectural stuff in this context. Good discussion on this last week, including helpful comments from Yves. I looked into the major features and also the substantive changes since 1.2. [My comment](https://github.com/w3c/apa/issues/341#issuecomment-1951464309). tl;dr everything is fine in my opinion. A couple of things we talked about last time, the naming of aria details, it accepts a list of id refs, but it's not called aria detailed by like the other labelled by and described by. The reason is there's no way that information is designed to fit into a flat string. It's supposed to be structured. Inconsistent but it's actually sensible, it sets the expectation that there isn't going to be a flat string version of this. Plus it was added in aria 1.1, the only thing in this version 1.3 is to change it to allow for multiple id refs, like the other two. It's been out there for some time.

Dan: is there any point in suggesting they should have both names? Concerned about developer complexity.. it's one thing to say this is how it was in 1.1.. but if someone is coming at it new.. they might see a pattern and then it doesn't work. Naive question.

Matthew: It's a good question, naming consistency is important. I think, if they were to add a synonym - they've done this for one of the roles, presentation, which actually meant there are no semantics on this element - and people didn't understand it, so they added 'none', it makes more sense that it doesn't have a role. There is a precedent for doing that. The challenge with this one is if you added detailedBy as a synonym you've also got inconsistency with label and labelledBy, you'd think it doesn't take aria refs but it does... I don't think we can make this better by changing the name. There are lots of attirbutes that accept id refs in all sorts of specs, and there isn't by on the end of them. It's not 100% optimal but I can see arguments on both sides why this was named what it was. I tried to look into it and find their discussion on this and the gh history doesn't go that far back. I can investigate...

Dan: doesn't sound like it's worth it

Matthew: agree. I don't think it can be improved by making the obvious change. I think it would end up being more confusing. Also label, labelledBy, description, describedBy map to the two most important things about an element. Name and description being consistent with each other is more important than other things are.

Matthew: Yves asked about translation wrt to the properties like description, role description and label, and the fact the attirbute value is a user facing string.

Yves: my main concern was i18n's reaction to that kind of thing - just a string with no indication of language

Matthew: good question. I didn't find any discussion around concerns raised by i18n. There have been these flat string attributes in for a very long time, so plenty of time for i18n to object if they were going to. Did want to spend more time looking at how translation works. It's not my area of expertise. I did find [a section in the spec about translatable attributes](https://www.w3.org/TR/wai-aria-1.3/#translatable-attributes) and it does talk about how that works, which attributes are expected to be localisable, and it gives a list. Minor bug - aria-description which is new isn't included in that list, which is clearly a bug, it's obviously supposed to be. I'll file an issue on the spec.

Matthew: for APA specifically - consider recommending adding slightly stronger wording against the use of things like aria label, description, role description - I've seen a lot of misuse of them. But it's valid that it's there, people need to use it right. There's pretty good guidence on how to do that. Maybe APA should add a stronger note to discourage that. We see a lot of overuse of aria label. There is a really strong note against over use of braille label and braille description.

Dan: suggest we close as satisfied with a brief closing comment. Thanks

<blockquote>

Thanks for your review request. We have no architectural concerns. There are a lot of really helpful new features, changes, and clarifications in this version, which will be of great help to users; great work!

</blockquote>

#### [ewp new issue on data harvests](https://github.com/w3ctag/ethical-web-principles/issues/109)

Amy: sounds like the finding we were discussing about the web not existing to serve an exploitative business model.. if we publish that we might be able to call it out in an existing principle

Dan: it's asking us to weigh in about copyright and licensing. of content hoovered up by generative ai. That's a matter for the courts? My personal opinion is that it's not right for ai systems to indiscriminately hoover up data and images without attribute or any understanding of the licensing of the training data.. Weighed in on this in the context of code, that's very specific, in open ssf, to try to get them to adopt guideance that systems that train themselves on source code should keep traceability of the licensing of the code, so as a user you know the code generating ai adhered to licensing in line with whatever your policy is. It's an important issue. There are court cases ongoing in different countries. Feels like a legal/policy issue.

Yves: https://www.theverge.com/24067997/robots-txt-ai-text-file-web-crawlers-spiders

Amy: I agree - weighing in on copyright and IP is too low level for the Ethical Web Principles... the higher level issue is the extractive use of labour ... which would cover that...

Yves: also copyright is not the same in all countries...

Amy: sort of covered by harm to society, freedom of expression, individual control & power... But the finding Peter suggested could be the detail.... will update the issue

### Breakout B (California / Europe)  - [2024-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Peter, Yves,
Regrets: Lea, Hadley

#### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

Amy: they've asked for our opinion but it's been 4 months so we could just ask if they've made progress

Peter: they're asking for a lot more detailed knowledge..

Amy: [posts request for more info]

#### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

Peter: three different features.. context bit looks fine to me. Gives me pause.. if I sign in from the IpD and sign out it still wants retain my identity, so I can do a 'sign in as..'. Not good for shared computers. Next person on the machine gets to see who I was.

Amy: yeah it looks like if the user grants permission for Rp-IDP communication, then signs in on a public computer, it would still apply that consent to remember them as a returning user..

Peter: other than that, not seeing any obvious issues

Amy: login hint doesn't seem to introduce any specific privacy issues

Peter: [leaves comment]

#### [Entry and Exit Animations](https://github.com/w3ctag/design-reviews/issues/829) - @LeaVerou, @torgo

#### [Captured Mouse Events](https://github.com/w3ctag/design-reviews/issues/872) - @hober, @hadleybeeman

#### [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss

Amy: they replied to Dan's questions...

Peter: it's been renamed to LoginStatus API and there's an [open issue on privacy cg](https://github.com/privacycg/is-logged-in/issues/55).. there's a pr about merging ipd sign in status to the api...

Amy: looks like they made some progress at tpac, but don't say what it is

Peter: inclination is to ask them for current status, exlpainer is 404 and things seem to be in flux. The privacy cg has an explainer in it now...

Amy: last update was 3 years ago that can't be it

Peter: Looks like is-logged-in is supposed to play with fedcm but doesnt' depend on it..

Amy: [leaves comment]


#### [Side Panel](https://github.com/w3ctag/design-reviews/issues/903) - @matatk, @plinss


### Breakout C (California / Australia) - [2024-02-19](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present:
Regrets:

#### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou

#### [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @torgo

### Breakout D (California / Australia) - [2024-02-20](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Matthew, Martin, Peter
Regrets: Lea

Special guest Reilly Grant and Robbie McElrath

#### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @LeaVerou, @torgo

Peter: We were concerned about WebSockets being allowed.

Reilly: We worked with Chrome security team. There are some apps that use non-web transports. We are trying to create an environment were the author's original code and intent is present, but alos granting access to facilities that some devs need.

... One need, as noted in the Explainer, is e2e encrypted messaging. Also applications that are completely offline. Such apps can declare all of their code, and the browser could verify. We need to allow access to these capabilities in some occasions, but in exchange the app has to adaopt a stronger security posture.

Peter: Helps to understand the use cases. Still have concerns. CSP would stop you from downloading scripts from other origins perhaps unintentionally. Doesn't stop you from connecting to anywhere else with raw sockets. Still some danger here, despte the CSP.

Reilly: There are some parts of this that depend on some kind of external vetting of applications that would allow browser vendors, or third-party auditors, to check that the application isn't doing something that intentionally subverts the protections. The goal is to force you to make it obvious that you're subverting the protections. A systme that looks at web content and detects malicious patterns could work here, as the app is more restricted.

Peter: The assurance that someone has audited the code tends not to work in the wild.

Martin: Who's signing this?

Reilly: The explainer doesn't go into some of how this could be deployed more broadly. The current prototype only includes signatures from the origin. The design is extenisble in that you could add additional signatures from an additional trusted party that would make those kinds of assertions about the checks they've done on the app.

Martin: Signatures don't provide the property of non-repudiation. If you have a chunk of code signed by your origin and you wish to disavow that fact, that's relatively straightforward to do. Signatures provide you with existential unforgeability. For a given key, you can show the content was produced under that key, but someone else could take a different key and make an assertion about the code. This does not seem to provide the desired protections.

Martin: This problem has come up before... https://dennis-jackson.uk/assets/pdfs/signatures.pdf covers some of these challenges.

Reilly: We were wondering if we could link these to DNS origins - that raised additional processes around ownership and longevity. Not sure how these concerns apply in this situation.

Peter: How would I check?

Reilly: Most browser extension systems I'm aware of use a key that represents the identity of the app across updates. The browser does the hash comparisons for you.

Peter: That would cover an update scenario, but if I get App B from Source A, this may not help. What happens if a key gets owned? Can I tell that these two apps came from the same person? We don't necessarily have to dive into all the edge cases, but we're trying to understand the broader scope here.

Reilly: There's an implementation question around the signatures. How do you do transparent updates. Good discussion in WebAppSec at TPAC around e2e messaging and binary transparency for web apps which delves into the same problem. You'd need to include a set of CSP protections. If you can load in cross-origin scripts, you don't have binary transparency anymore.

... The more interesting question to explore is: is the idea of trying to construct this environment that gives you these integrity properties (we can noodle on what they are) - is that something we want to tackle as web standards organization, rather than at the browser level.

Martin: Key question is what sort of protections are essential here - what level of assurance must we have to be able to e.g. trust the code to read our password file. Not sure these are articulated clearly in your proposal so far. I don't quite understand what you think helps you achieve that goal. Would be helpful to lay out those preconditions. I would also like to see that it's possible to achieve them; understanding them is the key.

Reilly: There's a strong correlation between the preconditions necessary for e2e messaging apps and our use cases here. The proof of that may not be immediately obvious, but the use cases are helpful, and may have consensus.

Martin: I think there are differences with the requirements to e2e messaging and the capabilities extension we worked on for this. Relies on having a way to deploy code that can't be individually targeted at people. The app you're running has to be the same as everyone else. That's a productive line of discussion (and we are pursuing it). If that's one of the preconditions we need here, this could be a good approach.

Reilly: That is the primary precondition. Looking at the platforms that provide these capabilities. Legacy native platforms have no controls. Modern native platforms are moving to app stores. With the app store model, someone is checking the app and determining it's not malware. In the legacy model, a virus scanner does this after the fact. In the modern, the app is checked before it's deployed. In the browser, we have extensions, which go through a similar review process. In Chrome, we extended the extensions platform into this app platform, which shares its security properties.

... The core properties are like those that apply to the extension framework. Properties to protect devs from themselves (e.g. CSP) and the capabilities to look at code before it goes to somoen's machine and check it's not malicious.

Martin: You're not including anything here that would suggest there's independent review.

Reilly: IIRC distribution methods in the Explainer is vague, but imples there could be a review process - I could make that clearer.

... Back to comparison with e2e messaging. That guarantee that code running on one user's machine is the same as on another's enables you to have that kind of review.

Martin: That's necessary, but not sufficient. If it's a WASM blob, which a lot of these apps end up being, the abiltiy to audit that, and understand the ways it can access the network is limited.

Reilly: I wouldn't disagree with that.

... An additional property that's useful in e2e messaging is in the reputational problem (e.g. app name can be faked) - being able to tie the app to the developer can help with copycat issues. This can't let you audit obfuscated code, but if a dev hides something malicious, their reputation would commensurately suffer, and be conveyed to users.

Martin: If your core capability is direct socket access, I don't think this is appropriate. At the moment we can guarantee that everyone has the same code that could be used to attack a network within which the browser is deployed.

Reilly: One place where we've seen a need for this bag of dangerous capabilities is any kind of desktop remoting. VDI apps deployed in enterprise situations, and others. A web-focused example of where this class of application needs something we'd never deploy on the web platform is WebAuthn. If you're remoting into a system, then using a browser, you can't remote the passkey exchange. This is bad news for remote desktop operators. One of the APIs we've been looking at for this environment is WebAuthn for remote clients. If you have a sufficiently trusted client (everyone's running it, and someone's looked at it and is happy with it) then you give it the capability to pass through the credentials. This is a feature that is provided on native remote desktop solutions.

... One school of thought is that "remote desktop apps can be left to native apps" - I think we can do better.

Peter: We could just not do direct socket access. When we first reviewed this, the primary case was IMAP. We responded "why not just build an IMAP API?" (and then same in other areas).

... How can we explain what the app is doing, to the user? Can we make a permissions prompt they could understand? A prompt like "I'd like to talk to your mail server" rather than opening up the whole world.

Reilly: This is why I like the WebAuthn example. If we had an extension to the API to allow remote tunelling, what requirements would we place on web apps that use it?

Peter: But if you devise a specific API, users have more control over these decisions.

Reilly: It's a good idea to concentrate on concrete examples. Is some kind of permission prompt that indicates you're doing more than a normal WebAuthn transaction good enough, or would you like some extra security restrictions on the app?

Peter: I get that these are not independent issues. There is such a thing as permissions prompt fatigue. But we don't necessarily have to open the doors to everything, keeing things fairly well sandboxed.

Reilly: Some of these capabilities are in the "we don't really know how to explain this to the user" camp. In cases like WebAuthn and e2e messaging, we need extra assurances to communicate to users.

... Part of the proposal includes this permissions-based system. For normal web content, policies are allowed by default, and web sites/apps can decline. In this approach, apps have to decleare which permissions they could possibly request. Anti-footgun mechanism for devs. Makes it easier for people looking at the code to understand the blast radius of the app.

... It doesn't automatically get everything becuase it has these properties.

Peter: There are apps (e.g. on native) that do just ask for everything at install time. Some devs don't play nice.

Reilly: Permissions policy isn't requesting at install time. It's saying what the app might request.

... This is why there's been a move away from asking at install time.

Peter: Though devs may still say they _might_ ask for X in future, so they'll ask for it now.

Reilly: This would cause extra scrutiny at auditing time.

Peter: This feels a lot like MiniApps.

Reilly: Yes.

Peter: Wondering about the boundary between what's a MiniApp and what's a WebApp.

Tess: Is there an attempt to converge the two?

Reilly: I'd like to converge things. I'm concerned that the MiniApp proposal is throwing a whole bunch of new technologies into the web stack - our approach is trying to add as little as possible. Convergence would be good though.

Peter: Question TH Lea. What's the difference from the user's perspective between an installed PWA and an IWA? Difference between a web app that's added to the home screen, and something that's been installed fully trusted.

Reilly: The requirement that these be installed comes from a couple of directions. Building the trust relationship requires a well-defined install event. Also desire to have them behave more like native apps. We're leaning on the idea of install as the point at which you express trust in the app because you've installed it. Users have different expectations between something they explicitly install vs something they get from any web site.

... What will user expectations be like in 10yrs from now, when users experience more apps as web installed apps, and native apps are less special? I don't have an answer to that.

Peter: Could this lead to a PWA that's been installed getting access to more things than a PWA that hasn't? This seems like a way to cross that bridge, but it's not clear that there's a path from one state to the other, nor that it's clear to the user.

Reilly: Now this has some technical teeth to the trustworthiness, but does the user understand that transition? Open question. Also it depends what the installation process looks like to a user. Today's PWA install process is seamless in Chrome. Shows off the fact that nothing changed. If you install a web app distributed via the Play store, this is a very different thing from the user's perspective, even if the web app is the same.

... We've explicitly chosen _not_ to make it super-easy to install these things from their publisher's web site, and make it obvious that you're really installing something. We don't want the web experience, that is far less of a trust decision.

Martin: Thanks for giving us all these details; very helpful.

Peter: +1 helpful to understand the developers' thoughts

#### [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou


### Breakout E (Europe / China) - [2024-02-21](https://www.timeanddate.com/worldclock/converter.html?iso=20240219T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present:  Dan, Yves, Max
Regrets:

#### [Early design review for the Topics API](https://github.com/w3ctag/design-reviews/issues/726) - @torgo, @rhiaro, @hadleybeeman

#### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Max: read this proposal... seems that we asked a question about uniqueness of the identifier -- they gave an answer abnout that...

Yves: it's not clear that IDs can't be spoofed - if it's a hash for example it's potentially fake-able. Also the scope extension is to extend the origin - the URL plus other origins... If the ID is tied to the URL then do they have multiple APP ids?  I'll look at that more closely to see how they are doing that...  If an app served from site-a,com wants to serve content rom site-b.com, site-b.com must be aware and accepting that...   Maybe we could have them on a call?

Dan: I will reach out to Diego...

#### [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @matatk, @hadleybeeman

Dan: they've updated their explainer with some additional examples... https://github.com/arichiv/opener-storage-partitioning/pull/3

Max: they have 2 proposals in their explainer... do they want both proposals reviewed?




### Plenary Session - [2024-02-21](https://www.timeanddate.com/worldclock/converter.html?iso=20240221T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Matthew, Dan, Martin, Yves, Peter, Hadley
Regrets: Lea, Max, Tess

#### New TAG Work Mode Proposal

Dan: I like proposed additions to rigour around how we triage, it's important. We don't do enough work, we just assign them. We end up with a situation where the right people might not be assigned. Different levels is good as well. Worried that we wil need special sessions dedicated to triage to do this. Would we have enough time on our schedule today to go through this process? Can we streamline it?

Martin: triage thing is daunting, looks like a lot of work. Concerned about gathering context. Formalising a bit more allows for one person or one or two people to perform the task. It becomes mechanical. Areas, people, next steps. That information gathering often requires a bit of extra knowledge of the history of things and a bit of digging. Most of the things that are difficult don't always appear to be. I don't think gathering context is a triage activity - but the first assignee.

Matthew: awesome. We discussed at the f2f about reading explainers before we start the review. Should we explicitly mention that in the process? is it worth having an explainer checklist that's a bit more explicit than the current advice on explainers. We see explainers that are missing things. Then when we do the triage we check to make sure the explainer is an explainer and if it's not we can have templated feedback.

Peter: I like more rigour in triage. Agree with Martin that maybe not all of this belongs in triage, or a second stage. It's about prioritise the important things first. Checklists like what Matthew was talking about, that it's ready for us to be working on. Main concern - a lot of areas in this process where we're gathering data. We need to be clear about what we're doing to do with that data. Distil to one of 5 levels - be nice if we had a formal way of storing the information we've collected so we have it for next steps.

Hadley: welcome the increased rigour and share expectations around triage. Will make it easier to work together. Specifically about assignments and async working - proposes empowering the subset of the TAG or individual or two people to post responses with the weight of the TAG behind them. I totally understand where this is coming from and recognise how much complication we've added by requring TAG consensus. On the other hand we've had a lot of experience of some members of the TAG weighing in with comments or concerns and the spec author responding at length to that, and another member engaging from a different perspective and the poster feeling like they had already started this process and suddenly the game had changed and someone new had arrived so what they had to do was completely different. I don't know if that's a pheneomenon specific to group dynamics in the past. Concerned we not recreate that.

Yves: not much to add. One thing missing is shortcuts that we can have - the fast track - which is not working that well at the moment. Formalising fast track and when to close issues in that case would be nice. Triaging will put things into fast track, and explain how it works. Ensuring you have at least two pairs of eyes.

Amy: we could move the conext part of triage ......

Peter:

Dan: to Yves point, fast track is accounted for in here, we're just not calling it fast track. It's roughly level 1. You could put "(fast track)" after that. Then we should have.. we've been trying to apply a fast track process, implies positive review. That could be documented further in here.

Martin: sensitive to concerns Hadley raises, but a tiny bit of process around that might help, mitigate some of the worst problems. I don't think there is such a thing as level 0. One of the larger levels in disguise. The decision not to review something needs consensus and a more dedicated discussion (unless it's spam). Basic idea of saying this is a trivial thing and whoever is assigned to this can discharge it without any more from the rest of us is almost okay, but giving people time to notice that's happened and an opportunity to escalate is a safety valve. Not always the case that someone looking at something would pick up on something. Rules around what it takes to conclude something under each of these would be good, and expectations about level of consultation necessary. And if something is at level 1 and someone wants to escalate to level 3 that's fine.

Matthew: we talked about deferring to HR reviews potentially for specific expertise.. and there's a hint about that in what's written. It could be helpful for us for bandwidth and quality reasons. Would we like to make that more explicit? If we do, two different ways.. we could say "we're happy with it but please talk with i18n" for example. Or if we think it's important that we get that review before we make our decision, it holds the review open, and we'd have to have some sort of monitoring around that process. There might be some w3c specific process around this.

Peter: when things are in level 1 and it's fast track, a lot of our experience is that it makes it fall into the abyss because they don't get scheduled for breakouts. We need to treat them as something that is scheduled, just not into a breakout. Maybe we make an async agenda for the week as well, and call that out.

Yves: same issue. You open something in fast track and there is no process of closing things. Is two people agreeing enough? Unclear. Quite clear when you're ina breakout and say we did that work and proposed closing and we'll do that at the plenary. We never had that for fast track. It led to having issues in the abyss. Despite the fact it should have been fast tracked. Process on how to close.

Hadley: nothing to add. this is a good and important discussion.

Peter: part of our issue template has been where would lyou like the feedback. We should take that out and we leave the feedback in our issue. Gets confusing to track when we do it.

Matthew: we talked about having a review score card where we look at all the different areas, which correspond to the HR strands. If we're doing async reviews and people get assigned over time for specific expertise reasons we could have a template where we fill that in - update a comment in the issue to indicate when we've ticked off a particular area. That gives the person that requested the review some visibility that we're making progress. Is this something we think we should do? I like it, but maybe it makes us seem less coherant as a group? Could be useful in some way for tracking. ...labels... tooling ... tooling goes off of labels...

Martin: any of these processes requires a degree of trust. If you have a rule that says two people are assigned to any task and they have to check with the other person that it's okay, then you have two people who have the responsibility of identifying when more people need to be involved. I think something along those lines can work with that understanding. Building that trust and that assumption into that process is not a bad thing.

Peter: we do this at f2fs. It's safe.

Amy: will take this in and revise and make a PR to work mode

Dan: in agenda creation for next week.. put the fast track things on the agenda so we close them.

#### Breakout Rollup

##### Isolated web apps

Martin: attempt to solve the app integrity problem but only to put extra capabilities in the applications .. a lot of attention applied to the capabilities but not the preconditions. I would like to encourage them to spend more time and effort on the hard part of the problem. You have a signed thing and you want a way to distribute that signed thing ... that's a hard problem that I know people are working on right now.

Dan: isn't this the same problem that miniapps folks are trying to solve?

Martin: it may be in the same kind of space... miniapps are you have an app and you want to ship it by an intermediary... in this case an intermediary may be a solution.. but that's the part where [it's vague].

Matthew: similar problem... to distribute apps via and app store .. but they are trying to do this without a designated party that everyone trusts...

Peter: i get what they're trying to do but a lot of holes in the technology...

Matthew: I got the impression that they didn't necesarilly have much agreement about the UI stuff that we talked about.  The user journey from something super powerful and something you just added to the home screen...

Matthew: They've got these use cases that represent developer needs... a different approach would be to provide specific APIs for these specific things... they cited specific examples... maybe specific APIs and specific API permissions would be more appropriate...

Martin: the use case they specifically used - a remote desktop website... the browser launches in the remote desktop... then that browser wants access to your passkey... so now that becomes  a very good phishing site...

Dan: i get the use case ... but it feels like they could work on that use case...

Martin: the other use case is raw sockets... tcp and udp directly... the answer to that is well.. don't. use the network capabilities that respect the security model...

Peter: this sort of thing has come up before and will come up again... OS's don't even get this right so where we draw the line ...

#### AOB

Dan: controversy around Apple and full screen web apps in the EU.. Should we weigh in?

Yves: would be good to know if it's a temporary measure until we figure out technical issues or if it's a way for them to leave web apps altogether. let's wait to hear more if we can?

Martin: is it about the broader thing or about the specific home screen install

Dan: the broader thing seems to be the topic of multi engine support on iOS. Regulatory has pushed them in a certain direction which is arguably good for the web. The specific problem is nerfing some of the capabilities of the web platform in response to this. Feels like we're moving towards a more expressive web platform, and this is a step backward. We've weighed in positively in the past on manifest and more advanced capabilities of web apps. We haven't specifically weihed in on PWAs because it's a controversial term, but in generally we've been supportive of adding expressivity to web apps, and full screen web apps has been one of those things, through the mechanism of the manifest file. Feels like something we ought to say something about.

Martin: encourage you to think about the core arguments you'd be making and whether or not they are web arguments or if they're outside of the web. Do they affect the web? Are they aspects of the web that are being changed by these decisions? Certainly the PWA example fits within that. If this is a question about cntrol of the platform and questions like that I'm not sure.. we'd have to be very careful

Dan: for me it's about the web.

Yves: is it related to what engine will run an installed web app?

Matthew: if yu decide to change the engine you're running all of a sudden all of your data isn't there. There are UI ways around that, but it's not an insignificant concern. If that is it, it would be possible to wrap that in a user experience. That could be wrong..

Peter: don't other platforms tie it to the engine you installed it from? I don't know what happens i fyou then uninstall that browser. I presume your apps just break. Worth us saying something. Should we wait until there are more facts about what they're doing.. or if we say something now could we stop them from breaking this. We have 2 weeks.

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
