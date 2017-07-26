Present: Dan Appelquist, Yan Zhu, Tim Berners-Lee, Peter Linss, Alex Russell, Charles McCathieNevile, Hadley Beeman, David Baron, Mark Nottingham, Travis Leithead, Yves Lafon
Special guests: Nick Doty (for discussion on fingerprinting), Wendy Seltzer, Domenic (for discussion on API design)

Scribe: Wendy, Yves
in which we look forward to the arrival of our absent colleagues
guten Morgen

Mark: I updated the document to draw a bit more distinction between legitimate tracking and illegitimate. not just fingerprinting and supercookies, but also header enrichment 
More examples would still be helpful
Rearranged the findings. 
" Believes that while browser fingerprinting surface area introduced by new Web specifications should be minimized where possible, on its own it is not sufficient reason to deny new features. We will work with the Privacy Interest Group on a document detailing guidelines for this. "
Mark: purpose is to flag how theW3C thinks about fingerprinting; details to go into Nick's document. Educator and call to arms for policy-makers. Not to completely define the space
Travis: Illegitimate thus implies a Legitimate tracking?
Mark: "on the reservation" I have todo to define better
even legitimate means can be used in non-benign ways, 
DKA: I like it for framing the issue. e.g. when I say "private browsing protects you from xyz" and people say "why doesn't the web always work that way." 

npdoty: some danger to legit/illegit tech because it will turn off some readers, imprecise. Purpose is orthogonal. 
Types of tracking that are 1) not controlled by the user on the web platform, 2) non-transparent, 3) violates same-origin. 
not about purpose

TimBL: legitimacy can be used when you talk about policy. So you need to talk about what the data is used for. What you're using it for is more significant than how you get it. 

mnot: If I remove cookies and I am tracked, that is a surprise as a user. Note that there are many people in the general population that are clearing cookies on a regular basis.
wseltzer: two use cases (at least): ordinary user, Tor browser user. TB rips out many features from browser, because its users need privacy more than features. 
mnot: there are two threat model, the everyday use where someone don't want to be tracked but that's not the end of the world if it happens, and the case where you _really_ don't want to be tracked. This document is more about the first case. What's normal on the Web.
Wendy: How do you define things so that the current Web still work while accomodating both use cases?
let's not legitimze deep inspection as a normal part of the web, so long asit's done for good purpose
Chaals: big corporations like search engines are not sending information to third parties, as they are the third parties.

[dka draws a table on the whiteboard]
dka: primary and secondary use of information/user control v no user control


mnot: we should be careful about not expressing value judgment. For example we have to be clear that "illegitimate" was referring to standarts, not law.
npdoty: things you should care about are transparency and user-control (and same-origin violations).
dka: if you allow yourself to be tracked, then reset your browser and clear cookie, you expect not to be tracked anymore.
Chaals: This is unspecified at the moment.
TimBL: we didn't discuss about linking use of DNT with Private browsing.
mnot: Private browsing is not clearly defined...
TimBL: This may be our duty to express that we need Private browsing defined
dka: this is the topic of this afternoon

hadley: If this were to be used to inform policies, it would need to clearly define what is needed.  Otherwise it is just a nod in a direction we want to head to at the technical level.
mnot: we should have an appendix "If you intend to create a law out of this, this is what you should use".
hadley: If you make a law about technology, it's better to do it about user needs as the underlying structure, rather than technical implementations. They change too fast.

mnot: we are to the point that to avoid being tracked, you need another computer, another ISP
TimBL: and another typist.

Wendy: when you say there are legitimate use of tracking, does that mean that it should be illegal to block such tracking?
mnot: If you live in a jurisdiction that have that kind of law, then you have to live with it.
mnot: DNT has a caveat for that.

Alex: We should ensure that new systems that provide storing data, or anything allowed for tracking, it should still be under user-control if tracking data is also under user-control.
Alex: So we should reframe this document to be related to user-control.

Chaals: the technical approach is to define standards way of doing tracking, where we have clear understanding on how to opt-out, like cookies. The other aspect is to tell what authors can do to track yourself, and ways to allow users to clear their tracking information on the site.
n
dka: I think that this is out of scope, this is more about the glue used to track between the browser and the server.

TimBL: A Bank for example can allow to do different things based on multiple levels of authentication. Tracking can be defined as multiple levels as well.
TimBL: We need to distinguish between the benevolent and the malevolent case because they are so different

npdoty: applies to plugins and other technologies too. flash cookies, plugins, EME, etc.
npdoty: to avoid evercookies, we need a way to remove ephemeral cookies that can be used in EME for exemple. As stated before, it is about user-control and transparency.

wseltzer: I like Nick's definition in terms of characteristics: user control (cleared simultaneously with cookies), user transparency/visibility, and constrained by same-origin.
Alex: +1
wseltzer: are there any other shared characteristics we should add to the list? 
npdoty: those are the 3 I keep coming back to.

dka: what are the next steps for the document? Ready to be put in GH? Is it ok to be published as a finding today?
mnot: The document should also give a heads-up for legislators, while being useful for developers. But we can decide on the audience.
Alex: we should say that there is a role for policy that technology can't fill.

Wendy: we should point regulators to the part of tracking that is defined by standards, and what is not defined by standards and could be the source of policies.
Yves: It is the use of standard-defined technologies for tracking (which was not defined for that in the standard) that is the issue.
Chaals: It would be nice if tracking could be done by standard-defined tracking, but regulators should be very careful.

[BREAK]
[during the break, edits to the doc defined "unsanctioned tracking" in contrast to "standards-defined tracking"; removing the illegitimate/legitimate distinction]
=> 
Topic: letsencrypt

Yan:letsencrypt is a new CA, launching sept. 14. ACME (Automated Certificate Management Environment) protocol is now at IETF.
dka: will letsencrypt companies work with small hosting companies? What would be the strategy for that?
Yan: hosting companies could use it. 
mnot: have you talked about distros about integrating letsencrypt scripts for setting up SSL
Yan: The linux foundation is a sponsor, but not directly with distros I think.

Topic: Extensible Report Card

dka: live edit, or enumerate TODOs/file issues, work offline ?
Alex: wondering if the current structure is "actionable". It might be useful to have a kind of chart defining layers in the platform and where specs fit.
Chaals: Various things has been sent back to school (AppCache,WebSQL, ...), in the same vein, we need to define what needs more work, what is good etc...
Travis: what is the audience for this?
Chaals: an audience is spec developers, to see what bricks they can build from (or not if not well defined).
Yves: for that audience, the layering is quite important.

[working on the issue list, see https://github.com/w3ctag/extensible-web-report-card/issues

[lunch - which was yummy in our tummies]

PROPOSED RESOLUTION: publish the "unsanctioned tracking" document as a finding: https://w3ctag.github.io/unsanctioned-tracking/
DKA: +1
hadley: +1
mnot: +1
plinss: +1
yan: +1
dbaron: +1
yves: +1
tbl: +1
travil: +1
slightlyoff: +1

RESOLVED, by swing of the chair's gavel.
www.w3.org/2001/tag/doc/unsanctioned-tracking/

Remaining agenda items: Accessibility, API design.

Topic: Accessibility

Chaals: Travis is the guy
In the last meeting, I talked about keyboard events. We should be moving toward intentions, as IndieUI, not "what the user did physically on the computer"
User-contract with the developer. 
General principle that that seems like a smart way to be heading would be helpful. 

Alex: I strongly dissent

Chaals: ARIA currently provides special magic to a special API that only special tools can use. 

DKA: They're using UAs that don't know anything about ARIA meta-information?

Chaals: right. that seems like a bad design approach. 
There's no reason for someone to have to install a bunch of special software just to reach the accessibility API
current thinking, that ARIA is only for screenreaders, doesn't help solve all users' problems .

Alex: it's purely one-way reflection

Chaals: ARIA role=button doesn't make the button activate by normal "button" means
imagine if ARIA made things actually behave as they claim
- simplify life of developers. Unless they want special handling, no special handling required
Do you break things or make it inherently more complicated? Testing suggests No.

Travis: what are you suggesting? 

Chaals: the behavior of the button, 
pull apart the pieces
the states that can be changed

Travis: envision an ARIA tab-index, instead of tab-index. You'd propose extending that to other types of features. 
Worth exploring. I imagine some of the interactions become complex. 
Early-gen accessibility interfaces had a primitive interaction model. Identification of the thing, simple action to trigger. 
Every control had one response type.  
More recent accessibility interfaces more closely map roles and states .Set up a range of actions.
Trying to bridge between what those intefaces provided and what a js dev needs to do to make it work. 

Dbaron: presumably because that's a native control

Alex: I feel that what you're describing is the right set of goals, but the form is confused. 
instead of adding an ARIA element and imbuing it with magic, create a series of mixins about what it does. 
I see ARIA as a communication channel out. It shouldn't take on side effects. That would be like drawing on a canvas re-starting the draw. 
Consumer-Producer model. 
I'd like to avoid doing this in a way that's not pluggable and in-script. 
You're right that people like to use high-level, but history shows that when you need to, you'll take side effects, 
HTML inputs conjoin typing, synthesizing key events, changing data model, display, range. Munging in a crazy single object.

Chaals: I think I share that goal. 

[Domenic gets eaten by cylons, or at least his phone does]

dbaron: It seems some of the goals are to supplant some aspect of the platform. 
Because the platform didn't let them take out pieces, they end up rewriting and not getting the capabilities of the element that they didn't want to remove. 

Chaals: We start throwing away bits of ARIA. 
You might start out having ARIA work, and as you get elements pulled apart, you drop the ARIA. 
Transition period will involve black magic, but my hope is that ARIA will become irrelevant, if web components works. 

Alex: What is the comm channel to assistive tech?
There's a big table of role and state mappings in ARIA

Chaals: if you set a given role, accessibility tree expects you to populate mappings

Alex: I could imagine if you had an API, doing more self-hosting of roles and states in script. 
[return to this discussion later]

Topic: API Design
 https://w3ctag.github.io/design-principles/

Domenic: There's been some good discussion on the issue tracker re naming issue

Id? 
https://github.com/w3ctag/design-principles/issues?q=is%3Aopen
Issues 13, 17 

Domenic: Fingerprinting, privacy, and API design
mnot: you may be interested...
Travis: We just put out a finding 
Domenic: could be interesting to look at how it applies to API design. 
Alex: Read the finding we just spent the day discussing 

Domenic: Should we put somethign into the doc?
Chaals: "go look over here"

#17 Warning on high precision and timing attacks

Domenic: "fingerprinting is a lost cause"? 
Chaals: Look at what your API does, be responsible

DKA: refer to previous finding. We just finished talking about it. 

Travis: I want to close 17, covered by 13. 

DKA: data minimization. This takes more thought. Close the issue. 

Domenic: #3, avoid nondeterministic behavior. 
[domenic drops, then rejoins]
if enumerating devices always starts with front camera, specify it

Issue #10 https://github.com/w3ctag/design-principles/issues/10
Travis: when I talk to my dev manager, he says we're doing it backwards. Specs for developers rather than for implementers

Alex: that's why we've started explainer docs

Travis: blended approach: algorithmic section intended for implementers, explaining what the algo is supposed to accomplish, before jumping into step 1.

Domenic: That's complicated because they get out of sync
We always bury somewhere "all the algos in this spec can be accomplished in any way with no observable difference"

dbaron: flipside. Sometimes there are multiple ways to write the algo that produces the same results. That scares me because of edge cases. 
You end up with a situation where implementers need to follow the precise algo in the spec to get the edge cases right. 

Travis: e.g. in DOM spec. If you take it literally, want to introduce sync events, you've introduced an observable change

Domenic: I like outlining explicitly why it's bad: prevents optimization, requiring 
Algo specs are perfect if you know exactly all the test cases and edge cases
If you don't, you might get in trouble by overspecifying

Travis: there's a degree of specificity in algos staged by how mature the spec is?? 
not sure I buy that

Domenic: unanticipated consequences

Travis: important to keep the goals of the algo in mind, edit that first. 
might be a good opportunity to get feedback in spec development

timbl: I don't know if the TAG wants to take up methods of writing specs
procedural, grammars, 
there's been lots of scorn poured on grammars and declarative specs
I think that cultural revolution has left us poorer.
Without machine-readable grammars, and with detailed procedures, we're in an appalling state 

Domenic: grammars have fallen out of style for lack of error recovery behavior. 
I could see a place for them, e.g. author conformance requirements,

Timbl: you could have multiple grammars, URL with reserved character properly used, improperly
but the actual grammars used in browsers can't be expressed that way

Domenic: even if we started from scratch, we'd end up with fall-back to a parser for "any character, any number of times" eventually for error-recovery

dbaron: CSS tried to do this in Level 1 and Level 2, trying to represent forward-compatible parsing
making the grammar represent any string, split up into parts. 
but 10 years later, we were still finding strings it wouldn't accept. 
finding a string the grammar didn't accept meant undefined error handling for that string. 

That was addressed by moving to a more algorithmic approach

Travis: can you talk more about the invariants?

dbaron: in CSS parsing, we knew roughly the invariants. 
then we found we wanted to do things the grammar didn't cover. 
Goal was to have points where old implementations knew what they could skip.
What was more important or less important depended on which extension pads the group decided to use later on. 

dbaron: algorithms, like code, need to be well-written to be understandable, maintainable. 

dka: should that go into the doc?

Domenic: yes. you have to go through code review.

dka: "this is a good way to do it", and here are some techniques. (Not "this is the only way to do it"). 
from the positive perspective: here are the advantages we've found. 

Domenic: I'll try to do a first draft. 

Travis: Anthing else you'd like us to look at as a group? 

Domenic: what next? do we want to make this a finding? 

dka: it's a few API design principles, not a comprehensive list. 

alex: let's let this document live. Promote it not as a finding. 

dka: document we keep updating as needed, like the Extensible Web Report Card. TAG Experiment
we should publish it once we figure out what it is. 

Domenic: abstract says "small but growing set", Findings aren't dead. 

Alex: but harder to republish, requires the whole TAG

dka: there's still more to do; 

Alex: when people come to us for review, I'd like to send this to them. 
"What to expect when you're expecting to design an API"

dka: Extensible Web Report Card needs more eyes. 
https://bocoup.com/weblog/extensible-web-manifesto/

Domenic: finding community members and adding them to github can produce good results. 

[Domenic leaves]

dka: we need to give that a milestone. 
Should we aim to publish something at next F2F? 

yes. 

Topic: Accessiblity 

Alex: @@ High level is good, also low-level mechanism should be available to the developer. [scribe was returning to the pad, apologies]

Chaals: Having a high-level event, 

Alex: My view is colored by experience, JS devs wil try to synthesize new high-level things, with a pile of code. I don;t understand the alternative

Chaals: alternative is painful but generic mechanism to find out things. You can make a generic controller, not particularly friendly, to read the list. 

Alex: I'd like to see the closed vocabs opened to APIs. 
ARIA is a closed vocab, not even 100% overlap with HTML. 
If you want to write something new, ARIA doesn't help. it has no API that lets you help yourself. 
When you're building something new, the system might not have a name for it, pile of divs styled to look like a calendar. 

Chaals: pile of divs to make a color picker. That's a horrendous UI, but amazingly generic. 
This is not an ARIA quesiton, how you talk to an object and figure out its primitives, what you can do with it

Alex: what was I objecting to? My concern, more closed vocabs without ability to extend don't seem to match how I see people makng new things in the platform. 
If the proposal is that every browser has to agree on a new semantic, implement, before making it avialable to anyone, then what are we doing new? 
How do we get incremental progress, see the gains then solidify them? 
I'd love ot see some code. 

Chaals: It should probably just be done. 

Alex: let's sit down and work through code together. 

Travis: New accessibility work? 

Chaals: proposal, ARIA keyboards. I don't see how it helps. 
It looks like access key, but worse. 

Travis: I thought it improved the ARIA situation, though it doesn't change the way ARIA works.

dka: I heard that Alex and Chaals would work through code together
Travis: I'd like to participate in that
Alex: I'd like to have Domenic join us. 

dka: can we put that into the spec reviews issues list? 
Alex: done




topic: New charters
wseltzer: Should we run through the ones in my list?
dbaron: sounds useful
wseltzer: I'll start with the ones in Technology & Society: Web Payments and 1-2 web authentication charters.

Wseltzer: We have a Web Payments IG, which has good participation. They're currently drafting a charter for a working group, which then goes to W3C for consideration and then AC review.
 http://w3c.github.io/webpayments-ig/latest/charters/payments-wg-charter.html
 ...Thinking about Payment architecture; what does the Web need to do transaction flows handling.
 ...Now has diagams of what a payments flow looks like.  Deliverables are web payment vocabularies; messages requests and responses around payment transactions (wallet API);  lots in it.
 ...I expect lots of interest in getting the TAG to review this, as an architecture design.  Are we biting off the right sized chunks? Achievable, extensible in the platform?
dka: what's the implementer feedback on this charter? 
dbaron: there's been a lot of back/forth recently...the feedback from browser implementers seems like rough consensus between vendors but with some non-browser participants not agreeing. In what ways is the system open to new participation? I.e., if there's going to be in-browesr payment, there are multiple ways to make a payment, how can other companies/systems participate? Is the browser offering a closed set of thigns? Not sure it's worth reviewing in detail here.
dka: I chaired an early workshop around this and co-presented with Mozilla on payment API issues and the feeling I had was "what are we asking implementers to do?" What is actually being asked? What requires standardization here? Do vendors now thing there are things to standardize?
dbaron: yes; I can say what the advantages are from a user perspective. Not having to type your credit card details into a page you dont' fully trust via tokenization is valuable. Security advantage there, particularly for small sites you might not fully trust. Another advantage is that payments that can be initiated without long-winded form input can be better for both users and merchants who want to complete a transaction.
dbaron: other browser vendors want that too
dka: are merchants interested?
dbaron: not entirely clear to me. I've only been to 1 IG mtg.
wseltzer:  Target, Merchant Advisory Group, NACS, etc.
dka: chaals? What's Yandex's view?
chaals: we have a payment system already, we see benefits of a low friction system that's good for developers. Setting up with Yandex Money is simple to set up; works with accounts denominated in rubbles. Being able to do things in a straightforward way helps make business work. We would like to see something that accomplishes this at scale.
chaals: we went folks to workshop and early meetings. Taking a back seat to see where things go. Seems like there's a reasonable chance there will be momentum. Being able to ship actual money around the web has large-scale benefits to privacy and security.
hbeeman: this could start at the level of tokenizing credentials/information or it could address payment backends...
wseltzer: all of those interests are represented in the IG, some parties are very interested in settlement, others in consumer payment transactions. First focus is the transaction between the user and the merchant (the user's payment agent to the payee's agent or processor) tokenization/input problem. Related to the regulatory system, we want to enable the parties to capture and exchange necessary data, not specify regulatory compliance.
hbeeman: lots of the regulatory stuff has been sorted out in intl money laundering treaties, no?
chaals: that does represent a lot of requirements, but local requirements are even larger
dka: these discussions always cut across all of these levels...it has always felt like a complex area. The Charter Scope looks good in that it simplifies it down to some smaller/key areas. The wallet thing is also interesting. Wonder if some of that could just be done via Service Worker?
slightlyoff: probably not?
dka: should we do charter review? How to engage?
wseltzer: interesting thought...looking at building messaging formats that encapsulate a lot of this opaquely. <scribe connection fail>
hbeeman: lots of what happens in transactions isn't something we can control, but finding places we can define APIs and put them into the web that will accelerate transactions has use and can change how these things are done (eventually).
travis: <trolls>
hbeeman: wouldn't be surprised if banking/payments industry reacts and learns from this, adapts and grows.
travis: why will they move?
hbeeman: exactly.
timbl: these APIs will keep track of wallets and credentials...will they keep track of transactions?
hbeeman: the goal is input/output formats for wallets, not how they actually work
timbl: if I have a wallet and want to send someone money...can I go to my browser and ask "what's the history of my transactions"?
wseltzer: that's not in charter but can enable that behavior in user agents. Not constraining agents at this point.
travis: what does Apple Pay do?
wseltzer: it could work with this flow
dka: so credentials in this wallet could work with a web transaction (e.g. if Safari/iOS implemented)
wseltzer: unclear if Apple would open that up to the web, but they are participating in the IG; hopeful
hbeeman: is anyone against it?
dka: paypal?
chaals: cc issuers?
dka: no, this allows those instruments to be used
chaals: but this could allow more efficient payment if user/site route around certain method
wseltzer: that discussion is sort of out of scope. Many participants.
dka: privacy, security are key elements
wseltzer: this group wants to do credentials and identity at some point as well; the "know your customer" requirements. Would prefer to work with tag to re-invention
dbaron: other charters?
wseltzer: web authentication and expected FIDO-alliance work on multi-factor author. That's waiting on their process to conclude.
(discussion of IPR roadblock)
wseltzer: HW auth/security group will spin up; secure element access, etc. The goal in splitting the groups is to keep the discussions distinct. One is about enabling multi-factor auth to the web. The other is about leveraging hardware security tokens/capabilities. Need to find ways to do that in accordance with same-origin (or has reasonable model). Not merging them is useful because they have different goals.

wseltzer to create an issue in the spec review repo. 
dka: wrap up!

thanking chaals/Yandex for outstanding hosting. Here here!

DONE.














