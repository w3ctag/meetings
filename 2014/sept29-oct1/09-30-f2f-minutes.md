## W3C Technical Architecture Group face-to-face
### - DRAFT -
### September 30

---

### Attendees

*Present:* Daniel Appelquist, Tim Berners-Lee, Domenic Denicola, David Herman (afternoon), Yehuda Katz, Sergey Konstantinov, Yves Lafon (remote), Peter Linss, Mark Nottingham, Alex Russell (afternoon), Jeni Tennison

*Guests:* Dominique Hazaël-Massieux (for discussion on Permissions)

*Chairs:* Daniel Appelquist, Peter Linss
*Scribes:* Mark Nottingham, Domenic Denicola, Sergey Konstantinov

### Contents

- [EME](#eme)
- [Captive Portals](#captive-portals)
- [Tooling / Github / Etc…](#tooling)
- [Spec Reviews](#spec)
- [Permissions](#permissions)
- [Spec Reviews (continued)](#spec_cont)
- [Pricacy](#privacy)

[Agenda](https://www.w3.org/wiki/TAG/Planning/2014-09-F2F)

---

<a name="eme"/>
### Topic: EME

__Domenic:__ Spec editor came to us at the last meeting to help us understand the current state of EME and answer our questions.

__Domenic:__ I worked out a proposal to make EME more "webby" -- more conformant to shared values of privacy, platform independence

__Domenic:__ I submitted a revised version of our opinion, stating concerns rather than solutions

__Domenic:__ Sergey reviewed, accepted pull request, then sent a followup which we need to discuss

__Domenic:__ Also, we got a reply from Mark Watson (Netflix) on list, which is good. His feedback was mostly about phrasing, softening things, etc. which I think we can address and is worth doing.

__Domenic:__ It'd be great to issue this as a finding that can be referenced as a TAG opinion when closing bugs on the spec.

> **mnot** [ group looks at document ]

> **twirl** https://github.com/w3ctag/eme/blob/master/EME%20Opinion.md

__Domenic:__ Sergey has an alternative design that he'll take to the group as potential future work.

__Domenic:__ EME has momentum; it's shipping in most browsers, vendor-prefixed; we're just trying to limit the damage.

__Domenic:__ We may still get EMEv2 or DRMv2 e.g., based upon public key cryptography, but that's a multi-year effort.

__TimBL:__ I'd encourage Sergey to do that.

> **twirl** Further reading: https://github.com/w3ctag/eme/pull/8

> **twirl** And http://lists.w3.org/Archives/Public/www-tag/2014Sep/0039.html

> **mnot** [ group reviews pull request ]

__Domenic:__ Sergey proposed sections on fraud prevention, accessability, fair use, anti-circumvention

__Domenic:__ My opinion is that these are outside the scope of criminal activity

__TimBL:__ I disagree

__Peter:__ The whole point of DRM is to prevent criminal behaviour

__TimBL:__ You don't have to say "fraud"; it could be "attack"

__Domenic:__ That could be OK; "attack vector" is better

__Sergey:__ I agree with Domenic; this shouldn't be limited to criminal behaviour. I'm 100% sure that some vendors will give you a license with additional restrictions. So let's make it clear that the user has to be able to read the license.

> **JeniT** JeniT has joined #tagmem

__TimBL:__ ... or you could leave affordances for regulators so that they can make appropriate limitations.

__Domenic:__ We should be concerned about the user, and phrase it that way.

__Domenic:__ The main point is that the user should be able to inspect the license, as this helps prevent attacks.

__Domenic:__ "Fraud" is less concrete than "attacks"

__ACTION__ Domenic and Sergey to re-phrase "fraud" as "attacks"

> **trackbot** Created ACTION-876 - And sergey to re-phrase "fraud" as "attacks" [on Domenic Denicola - due 2014-10-07].

> **mnot** Next - Accessibility

__Domenic:__ I don't think this works. It's saying that in a hypothetical future when they can translate video, we should punch a hole in EME for that technology.

__Domenic:__ I would rather approach this as saying that text tracks should not be encrypted. I have feedback that this is feasible and not highly controversial.

__Domenic:__ If we want videos to be accessible, we'd need a huge societal / legal effort.

__Peter:__ There are high contrast modes, e.g., those applicable to images.

__Peter:__ The video stream shouldn't be lopped out of that, e.g., if the browser is in high-contrast mode.

__Peter:__ A solution could be that the requirements can be pushed down.

__Domenic:__ If we soften it to "The normal accessibility modes of videos should be available."

__Sergey:__ [ draws diagram CDN - CDM - Hardware with pipe between CDM and Hardware to "System Service" ]

__Domenic:__ System services could give instructions to CDMs to help accessibility

__Peter:__ It could be a filter that has to be applied

__Domenic:__ these are specific technical solutions; there could be others

__Sergey:__ So we just add a note

__Domenic:__ yes.

__ACTION__ Domenic to add a note generally encouraging accessibility in EME opinion

> **trackbot** Created ACTION-877 - Add a note generally encouraging accessibility in eme opinion [on Domenic Denicola - due 2014-10-07].

> **mnot** Next - fair use

__Sergey:__ Amazon displays books in the browser, and you can't copy it. The HTML was a complete mess of iframes, etc.

__Sergey:__ In a short time, everything will be like that.

__Domenic:__ I worked for bn.com and we did ebooks. E.g., you were granted 45 pages of copying every thirty days.

__Torgo:__ Because it's important in an academic context

__Domenic:__ yes

__Torgo:__ The thing about fair use is that it's specific to jurisdiction, and varies quite a bit.

__Torgo:__ IANAL

__Torgo:__ AIUI the EU doesn't have a concept of Fair Use

__TimBL:__ Yes they do

__JeniT:__ It was never there as far as I'm aware, at least called "fair use"

> **mnot** Torgo radiates joy

__Torgo:__ There's work going on on a EU copyright overhaul

__Torgo:__ My point was that it's not universal

__Torgo:__ DRM stops users from doing things that are legal any way; e.g., excerpt of a video, which is legal under many copyright laws

__Sergey:__ video companies think that all copying of videos is illegal

__Domenic:__ Do we want to soften this to something like "We know that DRM and Fair Use have been in conflict, and would encorage discussion"

> **mnot** [ derision erupts ]

__Torgo:__ My thinking is that it'd be useful to say something like "DRM often foils people from doing something that's legal for them to do, according to their copyright law. This issue is not addressed in this document."

__Domenic:__ That's only useful from the perspective that Tim brought up -- that future lawmakers might find it useful.

__JeniT:__ Does that even make sense as a position though? Lots of tools don't let us do things that are legal for us to do.

__Torgo:__ They restrict you from doing something that you could otherwise do on the Web, under the pretense that you can't do this because it's illegal.

__TimBL:__ We talk a lot about UI quality and principles. In a way, to say we're introducing something that restricts the UI is a UI issue.

__TimBL:__ What does the TAG think about web sites that add their own link and attribution when you copy?

__Domenic:__ I think it's horrible

__Peter:__ We can't technically restrict people from being annoying; we'd shut down the entire web.

__JeniT:__ I think the usability aspect is important

__Domenic:__ How can we say that constructively?

__Peter:__ It's breaking the whole "view source" model on the Web

__Domenic:__ That's a can of worms

__Peter:__ There's a lack of developer tools; EME could prevent them from coming about

__Domenic:__ That argument means "no CDM"

__Peter:__ Or it means that the CDM exposes the content in a trusted way

__Domenic:__ The point of DRM is that there is no trust.

__Domenic:__ That might be a good motivator for DRMv2

__Domenic:__ Kill it?

> **mnot** [ group seems to agree ]

> **mnot** Next - Anti-Cirumvention law

__Domenic:__ This is an interesting one; not sure what to do with it.

__mnot:__ what vulnerabilities would they be looking for?

__Domenic:__ Like anything that ties into the OS

__Peter:__ it has low-level access to the hardware

__mnot:__ This seems like a purely legal problem

__Domenic:__ agreed, but it's a good problem to bring up

__TimBL:__ why is this a legal problem?

> **Domenic** mnot: the problem is stated that there's legal exposure for people who try to do penetration testing. that's in the legal realm

> **Domenic** timbl: so it's a problem that should be solved by changing the law, not changing the technology?

> **Domenic** mnot: i don't see how else

> **Domenic** timbl: well, if the whole setup was different (e.g. open source DRM), it would no longer be a legal problem

> **Domenic** mnot: but that's a pretty radical thing to put into the document

> **Domenic** timbl: agreed, not at this point, although a radical re-engineering is still a good idea over a longer timescale

> **Domenic** timbl: but we should raise the concern

> **Domenic** mnot: indeed, if only to give affordances to lawymakers later

__Domenic:__ My intuition is that you couldn't design a spec to make it not possible to sue (sergey's suggestion)

__Domenic:__ However, we could have something like an equivalent to the patent policy; "I won't go after pen testers"

__Domenic:__ We'd need to talk to the AB about that

__TimBL:__ AB might not be appropriate. It's worth pointing out that there are other possible protocols; it's half legal and half engineering

__Domenic:__ I only suggest the AB because they have experience with the patent policy.

__Domenic:__ I do like this feedback and suggest we do something with it; not sure where it belongs.

__Torgo:__ I like the idea of a covenant.

__mnot:__ +1

__TimBL:__ Using SMTP as a model; suppose that the mail RFCs said that conforming use of the To: header is that it's used to give a functional address for the social entity that sends the e-mail. A conforming user is one that does these things...

__TimBL:__ You then leave it open for regulators to use that.

__Domenic:__ Making spec into certifications is a big thing

__TimBL:__ That's different

__Domenic:__ I think we should remove this from the document, but draft a communication to the AB asking for collaboration

__mnot:__ Will it do harm in this document?

__Torgo:__ Then we can point to this when we talk to the AB

__Domenic:__ I think it needs to be separated. A lot of this is about concrete restrictions on the API; this is a separate concern.

__Peter:__ This fits under the category of security concerns.

__Domenic:__ good point

__Domenic:__ We'd want to modify it into "We'll be investigating this..."

__Peter:__ Say that this is a hole that we don't want to leave open

__mnot:__ As long as we make it clear that we don't expect them to solve this problem.

__Domenic:__ I appreciate the notion that this could be built on top of web crypto, but don't think it's directly relevant

> **mnot** group resolves to rephrase, make it clear that this is an action for the TAG, not EME; make it clear that this is a security risk, put under security section ]

> **mnot** Looking at Mark Watson's feedback

__Domenic:__ There are four points.

__Domenic:__ First - phrasing of "The ability of the CDM to potentially run arbitrary code is a hole in the web platform's security model."

__Domenic:__ He has a point; e.g., Flash

__Domenic:__ OTOH it's aritrary from the standpoint of the user, and opaque to the user

__Domenic:__ We can either change from "arbitrary" to "unspecified" or add a sentence giving context

__Sergey:__ With Flash, SWF are a set of instructions. With EME, we don't know that video is just data, not code.

__Domenic:__ So restrict what data goes in and out?

__Sergey:__ Yes, so only data goes in and out

__Domenic:__ That seems to go against years of computer science

__Domenic:__ Oh, you're saying that frames shouldn't smuggle code?

__Sergey:__ Yes

__Domenic:__ There is no restriction that it is video presently?

__Sergey:__ They're talking about using standardised form of encrypted video. But the license response could contain instructions for the CDM.

__Domenic:__ I think this is worth bringing up in our reply to Mark; it may not change what we put in the document though. I haven't talked with many people about the license response.

__Domenic:__ Second concern - "As part of interoperability, EME should not provide APIs that are designed to allow restriction of content to one platform and/or key system."

__Domenic:__ We should do a more thorough investigation by what is meant by this.

__Peter:__ Isn't it the opposite, that EME is failing to provide universal APIs?

__Domenic:__ I think we covered that pretty well.

__Domenic:__ More investigation needed.

__Domenic:__ Third concern - "While certain key systems may only be supported on certain platforms, and certain content may only be available with certain key systems..."

__Domenic:__ I'm not sure what he's concerned about here.

__mnot:__ he seems to be just noting something.

__Domenic:__ Fourth concern - "We understand that designing a DRM system for the web brings along robustness requirements that are unlike those of most Web APIs..."

__Domenic:__ My take is that this is not very relevant.

__TimBL:__ He's saying "Don't focus on robustness."

__TimBL:__ Maybe he's saying that people should be allowed to think about systems that don't have robustness

__Domenic:__ I want to push back because I don't see this expressed in the EME document

__mnot:__ We're not writing a requirements document; it doesn't have to be complete

__Domenic:__ Maybe he's concerned that we're mischaracterising it

> **mnot** [ side conversation between Domenic and Sergey ]

__Domenic:__ Tim's point is that we shouldn't say "necessary for robustness" as if that were a feature for all DRM

__Domenic:__ ... but EME has chosen to address DRM in this way

__Peter:__ You could address this by removing the word "robustness" from that sentence

__Domenic:__ OK

__Domenic:__ I like this, because it addresses Tim's and mark's comments

__Domenic:__ Or say "Robustness or IPR"

__Torgo:__ I like Peter's suggestion more

__Torgo:__ Keep silent on the motivation

__Domenic:__ That's it for EME

> **timbl** http://tag.w3ctag.org

> **plinss** https://pad.w3ctag.org/

> **timbl** “

> **timbl** The web address you've requested doesn't exist

> **timbl** The web address you have requested is incorrect or does not exist. You could try amending the spelling or check the web address.

> **timbl** ”

> **timbl** Pppht

> **mnot** [ group agreed to send this as spec feedback ]

> **timbl** https://pad.w3ctag.org/p/eme

> **Domenic** { "&" : "&"} ===> <json:string name="&amp;">&amp;</json:string>


<a name="captive-portals"/>
### Topic: Captive Portals

__mnot:__ we've talked about captive portals a lot in the IETF and elsewhere

__mnot:__ if we wanted to try to do something, we could probably get the right people from places like Cisco, Microsoft, Apple, the browsers, ...

__mnot:__ where we're at now, is, "what can be realistically done?"

__mnot:__ we've had preliminary discussions mapping out the problem space, figuring out back-compat constraints

__mnot:__ big question is what is the right layer to interpose these things

__mnot:__ we have a status code in HTTP for this, but you can't intercept that when you go over HTTPS

__mnot:__ anecdotally I've been seeing fewer captive portals, just WiFi passwords

> **Domenic** (the room disagrees)

__mnot:__ a common use case is just showing some text before a user connects

> **Yves** well, ssl should show certificate issues if connected to a captive portal

> **Domenic** (discussion of various problems with bad cert errors upon connecting to a network and how this is only getting worse)

__timbl:__ i could see OS designers lying, saying "there is no network," until they can detect actual internet

__mnot:__ yes, but there is a war between the networks and the OSs, some captive portals want to overcome captive portal detection

__dka:__ this is why apple has 100 different domains to detect this...

__mnot:__ it's only getting worse because Apple is doing MAC address randomization, causing captive portals to lose their ability to remember you

__mnot:__ low hanging fruit would just be documenting what OSs do right now

__timbl:__ what would it look like to design this from scratch?

__mnot:__ we need a transition stategy

__timbl:__ no, I'm more interested in benevolent places like MIT

__mnot:__ my gut is if you wanted to do this from scratch it would be part of 802.11

__plinss:__ what about DHCP?

__mnot:__ we're trying to get away from that; inherently insecure

> **plinss** s/plinss:/timbl:/

__timbl:__ "here's your IP address; it's not going to work until you visit this web address"

> **Yves** DHCP is insecure, but still you configure your interface (and dns settings) using dhcp replies

__mnot:__ but because of how DHCP works, anyone can announce that to you, so it's a great way to phish someone in a coffeeshop

__timbl:__ are we ratholing?

__mnot:__ the problem is captive portals are full of ratholes like this because it's full-stack

__timbl:__ i'm interested in solving this for enterprises and universities...

__mnot:__ well universities have alreayd solved this with e.g. eduroam...

__plinss:__ (but it's still a crappy implementation)

> **dka** http://www.btplc.com/news/articles/showarticle.cfm?articleid=%7B2b5f7e38-2551-47d6-9d01-21f44cb25d26%7D

__plinss:__ opportunity to invite some of the other parties around TPAC?

__mnot:__ I was thinking more a full-day workshop. And TPAC is only a couple weeks away

> **mnot** https://github.com/httpwg/http-extensions/wiki/CaptivePortals

> **timbl** timbl has joined #tagmem

__plinss:__ I'd like to see an end result of "ideally, here's a spec for a good captive portal"

> **Domenic** (discussion of a "brand" for well-designed captive portals and related stuff)

__mnot:__ my gut feeling is that this is a long-term thing

__mnot:__ perhaps an event of early to mid next year

__plinss:__ perhaps adjacent to EWS in April

__mnot:__ concrete next steps---work on the wiki, talk to people to set up a meeting, maybe come up with a plan for a plan

> **Zakim** Zakim has left #tagmem

> **timbl** Hitler reacts to the HTML5 URL normative reference controversy - See more at: http://meemsy.com/v/22036#sthash.I7RqFP9V.dpuf

> **timbl** The last bit was snuck in by the site — how?

> **twirl** ScribeNick: twirl

> **dka** Starting Up Again

<a name="tooling"/>
### Topic: Tooling / Github / Etc…

> **twirl** mnot: <presented his concept of TAG homepage>

> **twirl** mnot: <shows script which uses Github API to get all issues>

> **twirl** mnot: <reviewing w3ctag repositories>

> **twirl** mnot: Markdown rules

> **twirl** mnot: The hardest decision is doing something with our home page

> **twirl** dka: I think it's a high priority task

> **twirl** dka: EME is a good example, it's actually spec review but it's not in spec reviews repo

> **twirl** mnot: Chairs should control repo creation

> **twirl** [ disagreement ]

> **twirl** [ mnot is very persuasive ]

> **twirl** [ discussion on whether github wiki is better than TAG Wiki or not ]

> **twirl** [ discussion on using wiki vs repos ]

> **twirl** mnot: Repos could be used offline

<bkardell_> bkardell_ has joined #tagmem

> **twirl** mnot: And github wiki too :)

> **twirl** mnot: github wiki is a separate repo

> **twirl** [ mnot explains how HTTP2 repos are organized ]

> **twirl** [ discussion on organizing indexes ]

> **twirl** dka: proposes (a) move to tag.w3.org -> w3tag.github.io, (b) move meeting organization to github, (c) move minutes to github

> **twirl** (d) move all current work to main page, (e) move EME to Spec Reviews repo, (f) clean up repos, (g) backup everything, (h) elaborate policy on repo creation

> **twirl** mnot: are we ok with breaking URLs?

> **twirl** timbl: I think its important to preserve URLs

> **twirl** s/its/it's

> **twirl** [ dka explains our current policy ]

> **twirl** plinss: let's proxy all URLs into W3C space

> **twirl** [ timbl explains how to convert cvs subtree ]

> **twirl** [ plinss explains how to synchronize github and w3c space ]

> **twirl** plinss: Minutes URLs MUST be preserved

> **twirl** dka: Having our documents in github, having clear repos are good ideas

> **twirl** dka: But I'm very concerned about preserving URLs history

> **twirl** [ general discussion ]

> **twirl** dka: We could put on our home page everything which changes rarely, and have a separate gh-page for current work

> **twirl** mnot: I could try to convert our old stuff

> **twirl** [ discussion on CVS -> git conversion ]

> **twirl** mnot: what about gh issue tracker?

> **twirl** mnot: two trackers are confusing

> **twirl** [ historical joke from dka ]

<bkardell_> ...But GH is very Dev friendly

> **twirl** dka: the problem is that each repo has its own tracker, so you can't see all w3c tag issues

> **twirl** mnot: let's use Arch tracker for long-living issues

> **twirl** [ discussion on confusing trackers ]

> **JeniT** all issues: https://github.com/organizations/w3ctag/dashboard/issues/repos

> **twirl** dka: let's setup a repository for "TAG" issues

> **twirl** dka: and close w3 issues

> **twirl** mnot: what to do with spec reviews wiki page? let's put in README in specreviews repo

> **twirl** [ dka tells the story about agendas in cvs ]

> **twirl** dka: let's move agendas to github

> **twirl** mnot: what's the metrics of success?

> **twirl** [ memes, videos, number of documents ... ]

<a name="spec"/>
### Topic: Spec Reviews

> **twirl** Domenic: we were asked to review WebApps specs

> **twirl** Domenic: WebCrypto is done

> **twirl** twirl: Web Animations review is done

> **twirl** mnot: HTTP2 reviewed

> **twirl** [ reviewing w3c issue tracker ]

> **twirl** mnot: Get off My Lawn: closed

> **twirl** http://lists.w3.org/Archives/Public/www-tag/2014Jun/0004.html

> **twirl** http://lists.w3.org/Archives/Public/www-tag/2014Jun/0002.html

> **twirl** mnot: CSS Regions?

> **twirl** [ plinss explains elements flows ]

> **twirl** dherman: Is there any progress with box trees?

> **twirl** plinss: yes, we are moving

<bkardell_> Was a task force set up?

> **Yves** good also to put the discussed scope in the issue description

> **twirl** [ looking at: CSP2, Mixed Content, Referrer Policy, ... ]

> **twirl** Domenic: I've reviewed Referrer spec, found some issues

> **twirl** [ mnot and Domenic take this issue ]

> **twirl** [ Domenic explains SRI problem ]

> **twirl** mnot: there severals spec related to URL metadata

> **twirl** s/spec/specs

> **twirl** s/there/there are

> **twirl** https://github.com/w3ctag/spec-reviews/issues/36#issuecomment-57311652

> **twirl** Domenic: best way to do spec reviews is talking to author directly

> **dherman** "on their turf" is a powerful point

> **dherman** "TAG is here as a service" <== good attitude

> **twirl** [ Screen Orientation is done ]

> **dherman** "come over to my house and let me tell you how you're wrong" <== bad attitude

> **dherman** TAGaaS

> **twirl** [ multipart/form-data ]

> **twirl** mnot: it's already Last Call

> **JeniT** http://www.ietf.org/rfc/rfc2388.txt

> **JeniT** (presumably the previous version)

> **twirl** Domenic: looks cool, there are tests

> **twirl** [ work suddenly stopped ]

> **twirl** https://github.com/w3ctag/spec-reviews/issues/34#issuecomment-57313078

__https:__//github.com/masinter/multipart-form-data/issues/17#issuecomment-48077041

> **twirl** [ reviewing multipart-form-data issues ]

> **twirl** [ off-topic: mnot complains about implementing HTML5 ]

> **twirl** [ agreed to propose something by TPAC ]

> **twirl** mnot: Wake Lock

> **twirl** Domenic: I'm already involved

> **twirl** I'd prefer to have a simple API

> **twirl** s/I'd prefer/Domenic: I'd prefer

> **twirl** http://w3c.github.io/wake-lock/

> **twirl** [ reviewing proposed use-cases ]

__mnot:__ Full Screen: closed

> **twirl** mnot: Manifest?

> **twirl** Domenic: It's for installable webapps; related to packaging

> **twirl** mnot: WebRTC Identity Provider Selection

> **twirl** Domenic: bizzare thing, something like invisible iframe

> **twirl** https://github.com/w3ctag/spec-reviews/issues/28#issuecomment-57316875

> **slightlyoff** OMW

> **slightlyoff** hey all

> **slightlyoff** terribly sorry

> **slightlyoff** meant to join 2 hours ago and failed = \

> **dom** dom has joined #tagmem

> **slightlyoff** worse in many, many ways = )

<a name="permissions"/>
### Topic: Permissions

> **slightlyoff** terribly sorry for how long that took

> **dka** https://gist.github.com/slightlyoff/43cd8c2f64a0719358fe

__Alex__ there are several key aspects

... you can request a permission at page load

... you may build UI using API calls results

... all these things are async

... and user can always say no

... we can imagine lighter UI than prompts if user trusts that app

... we have lots of experience with mobile apps sync permission dialogs, and its disappointing

... there is a trade of remembering webapp permissions vs. leaking this information

__twirl:__ how to revoke permissions?

__Alex:__ I separated UI from API in a document

__twirl:__ but how will webapp know its permission revoked?

__Alex:__ ask each time

__Domenic:__ but how to restyle UI?

__Alex:__ probably perission change event

__Dom:__ I like this proposal

... we discussed those questions, I think it's a good starting point

> [ discussion on requests ]

__Alex:__ the question is whether it reasonable to create separate API requests to each action

__mnot:__ there is no easy answer, in mobile APIs too

__Alex:__ you should have a freedom to change your mind

__Alex:__ we could do that in extensible way, with low-level API

__dom:__ It would be great if TAG provides more guidance on securing the Web

> **slightlyoff** I am still working on the origin post, it's much harder

> **slightlyoff** so I have an idea of where we're going here

> **slightlyoff** I can outline it briefly

__dom:__ We need a clear picture of future web security

__Alex:__ there are good success stories from OSes, we should work on browser UI

... we should think about "installation" for webapps

> **slightlyoff** I don't think WG's are the right place to be litigating these issues

__dom:__ we need even broader picture

> **slightlyoff** nearly all the important security UI is owned by the UA

> **Domenic** permissions, origins, crypto, UI

> **slightlyoff** and that's increasing over time

> **Domenic** (i really like this idea that we should lay out the landscape of how all those things interact)

__Alex:__ we now have some legacy, files, we can't ask, for example, a single contact information

> **dka** ok thanks Dom!

__timbl:__ I need to understand why app wants to have some particular access, I have to trust it completely

__Alex:__ we may think for example about manifest, so user could understand what application is

> **twirl** ... I don't believe we have answers; for example, should permissions be granted to app working in iframe, etc

> **twirl** s/answers/all answers

> **twirl** [ timbl on peculiar requests bouncing in Chrome ]

> **dka** dka has joined #tagmem

> **twirl** [ discussing the problem of sending credentials with CORS ]

__Alex:__ Credentials are the most valuable permission, more sensitive than raw socket access

__timbl:__ imagine that I'm trying to write really good calendar, I need to be able to get information from all other sources

> **twirl** ... at present moment ony Facebook could be such super application

> **twirl** ... that's reputation question

__Alex:__ my experience tells that user doesn't understand what really happens

> **twirl** [ discussion on service workers which help to solve these problems ]

__dka:__ Dom asked could we document security model beyond permissions

> **timbl** timbl has joined #tagmem

> **twirl** ... and that's an action for the TAG in my view

__Alex:__ I've been working on origins post

> **twirl** ... we need to evaluate question how much more could you trust smth, there is no answer right now

> **twirl** ... Service Worker is a thing which controls origins since it sees all requests

__mnot:__ we have same problems with proxies

> **twirl** [ Service Worker Union, we need it ]

> **timbl** http://www.seiu.org

> **timbl** clientside proxy

> **slightlyoff** timbl: we avoided that because it doesn't describe the other background stuff we can do with it, e.g. responding to Push messages

> **slightlyoff** timbl: also, I'm going to look into the XHR/fetch credentials thing and see what conditions we can relax it under

<a name="spec_cont"/>
### Topic: Spec Reviews (continued)

> **slightlyoff** thanks for bringing it up

__mnot:__ Shadow DOM

> **twirl** [ awwwww ]

__mnot:__ Closed!

__mnot:__ Navigation Error Logging

__mnot:__ They added promises

__mnot:__ I'll check implementation status

__mnot:__ Beacon

__Alex:__ API is ok, but there could be some implementation problems

__mnot:__ NFC API

> **slightlyoff** this API doesn't look half bad!

> **twirl** so many abbreviations

> **slightlyoff** questions for NFC: what about "background" NFC? integration with SW's?

__mnot:__ CSS Font Loading

__Domenic:__ nearly done

__mnot:__ Web MIDID

> **twirl** s/MIDID/MIDI

__mnot:__ Closed

__mnot:__ WebRTC

> **slightlyoff** I think we should perhps try to get the ORTC folks to present?

> **slightlyoff** maybe have them talk to us?

__dka:__ let's organize a call

> **slightlyoff** thanks

> **slightlyoff** I would also like to let both "sides" know that we're paying attention

> **slightlyoff** and would like to see resolution + interop

__mnot:__ Web Components

__Domenic:__ done!

__mnot:__ Push API

__Alex:__ already done, feedback accepted

__mnot:__ Web Audio

__Domenic:__ done

__mnot:__ Compositing and Blending

__mnot:__ Closed

> **slightlyoff** the only thing about Push that's nasty is the verbosity in the API: https://w3c.github.io/push-api/#example

> **slightlyoff** but otherwise I think it's in good shape

> **twirl** verbosity is better than letter-saving

__Domenic:__ next time we should ask authors about preferred form of communication

> **slightlyoff** the call is SUPER static-y now

> **slightlyoff** gonna re-dial

> **slightlyoff** thanks

<a name="privacy/>
### Topic: Privacy

__mnot:__ I talked with Chrome and HTTP teams, they were frustrated with Privacy mode understanded by users

> **twirl** s/understanded/understood

__mnot:__ people don't understand what Privacy Mode guarantees and what does not

__mnot:__ if we standardize definitions of privacy mode it will help

__mnot:__ users and websites will learn what it means

__mnot:__ it's probably a proper moment to act

> **slightlyoff** link?

__mnot:__ I tried to define what browser privacy mode is

__mnot:__ hiding clues from other users of the computer

> **slightlyoff** I'd LOVE for sites to get unique storage in this mode

__mnot:__ hiding from external observers

__mnot:__ hide identity from websites

> **slightlyoff** the measurement APIs are an area we can do better in a privacy mode

> **slightlyoff** also font access

__dka:__ fingerprinting is important too; I can be okay with tracking in regular mode, but I'd like to be not tracked in privacy mode

__plinss:__ but you can, in fact, identify yourself as a person-which-is-untraceable

__mnot:__ browsers should be more agressive in failing situations

__mnot:__ and last one: get user informed

__mnot:__ in privacy mode browser either should either obfuscate traffic or display an alert

__Domenic:__ browsers should compete how many privacy features they implement

__Alex:__ I think in privacy mode access to storages should be restricted

__dherman:__ how could this affect the platform?

> **slightlyoff** specifically I was saying that you might be able to partition storage

__mnot:__ spec editors will be aware of several browser modes

__dherman:__ idea itself seems fruitful, but AFAIK users use Privacy mode for hiding browser history, not to be not tracked

__dherman:__ we should not make decisions based on our view, not real people needs

__dherman:__ it's a product decision, not platform

__timbl:__ that's just a switcher saying "I will be embarassed if anyone knows"

> **timbl** s/knows/knows — it is up to the tech community t try to anctipate the attack vectors, not the user/

__dka:__ there are too less knowledge about when you'd better use privacy modes

> **twirl** s/there are too less knowledge about/people know very little

__JeniT:__ does this affect server-side?

__mnot:__ in general not; maybe in a form of profiles and cookie politics

> **dka** adjourned

> **slightlyoff** heading off

> **slightlyoff** later all!

> **dka** thx!


