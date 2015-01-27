# TAG f2f
## 6 Jan 2015 - NYC - Google - Earth

## Present: Alex, Sergey, Yves, Domenic, Tim, Mark, Peter, Jeni, Dan
## Regrets: Yehuda

---

Chair: Dan
Scribe: Alex

Topic: Houdini Task Force

mnot: there's an effort in IETF to register .onion, there's also decentralized naming on the horizon

[marking for discussion pre-lunch]

*Topic*: Houdini Task Force

plinss: not sure what's new except the name. Meeting scheduled in Feb in SYD the 2 days before the CSS WG mtg. Some discussions about opening up CSS parsing via API.

dka: charter?

plinss: extensibility to CSS; notably:
    
    - defining the box model
    - creating APIs to the box tree
    - ways to interact with the box tree at layout time (e.g., Layout Workers that can participate in box creation, layout, etc)
    - also looking at missing extensibility points (parser, cascade/resolution)
	    related: https://github.com/glitterOrg/pipeline
	
[discussion about security/privacy implications of desugaring CSS work to JS; e.g. CSS Shaders]

plinss: opening up the CSS parser is the first thing; writing polyfills is too hard

mailing list here: http://lists.w3.org/Archives/Public/public-houdini/

dka: what's our way of helping to facilitate developer back to the TF? github? other? How do we talk about it?

plinss: discussions about that likely to happen at f2f

slightlyoff: who's attending this f2f meeting?

plinss: mozilla, google, css wg members...

alex: tool vendors such as sass and less should be involved...they're the constituency who is feeling this pain most and I'd be worried if they're not at your early f2f meetings

[how many engineers does it take to present a demo?]

[looking at glitter demos...they're neat! custom properties and drawing]

Topic: TC39 update

domenic: ES6 is going to be finalized soon...published officially in May/June. Last-minute snag about built-in subclassing from implementer feedback. Mailing lists are a-flutter. Somewhat worrying.

slightlyoff: what's your sense for timing?

domenic: schedule slippage not likley to happen.

dka: what does that mean for Joe User?

domenic: ES6 is being implemented by major browsers. The open question is if/how Joe User can subclass HTMLElement/Array/etc.. Conceptual framework still, worryingly, under debate. Parallel work is happening on ES7 proposals. That seems to still be going well.

dka: what's the intention for terminology post-ES6?

domenic: ES-2015, ES-2016, e.g.

ylaffon: discusison about streams?

domenic: streams are going to stay where they are for now (WHATWG). I'm sympathetic to only wanting a single standards body.

slightlyoff: what's the status of the patent/cc0/etc?

dka: are they openstand compatible?

domenic: no. Brian Terrelson (MSFT) is doing a lot of work on this. better-than-zero chance of changing the rules, but going slow.

domenic: copyright is still ECMA. Patent process is in process for ES6, going well.

dka: is there any area that the TAG can help with?

[jokesa about JSON. Too soon?]

domenic: there's a WebIDL patchwork of use of ES features. Probably needs and update. Something we can highlight. Also, post ES6, there's a lot of work on tooling to let the spec be edited as HTML, in plain-text (not MSWord), on github, etc.

[digression about C++]

domenic: works continues on specifying the event-loop in ES6. Currently in HTML, and I'm not sure that ES6 is doing the best job about the portions it's taking on, but will get better. Promises forced this, O.o needs it, generality ahoy. Will enable setTimeout() to be in the language, e.g.

mnot: Python did this in Python3. In PEPs.

domenic: one more thing! Modules have been split into syntax (which is stable) and loaders which are still speculative and are now in a separate spec. This allows implementers to get a start on syntax.

timbl: what's the name of a module? Is it a string? URL?

domenic: it's a string. Plan is absolute URLs and "."-* are verbatim in the URL namespace. If it's a "bare string", it gets looked up a table.

timbl: so we still have a table?

domenic: yes, you need it so you can do "import jquery"

slightlyoff: it's pretty important...lets you transpile...

timbl: is that only for table'd imports?

slighlyoff: oh, no, you're right...swapping out the loader should let you transpile for everything...

timbl: lots of systems have had these search paths. If everything's just URLs and a package system, then you get out of this problem.  Search paths are evil

domenic: the hope is that the package system would build the table for you.

timbl: what about incompatible versions of the same lib?

domenic: I'm pushing for supporting that.

timbl: what if I use the short-name in that case?  

domenic: the loader can satisfy that based on the caller.

[discussion about table population and timing of i/o]

[discussion about require()]

[discussion about agenda additions, privacy IG, etc.]

TOPIC: coffee.

TOPIC: HTTP/2

mnot: at IETF last-call, ends on Jan 14; goes to IESG on Jan 22. Will have an RFC shortly thereafter.

[discussion about treating comments with due respect]

dka: that's HTTP/2 & HPACK

mnot: yes, we have 25-30 impls. Shipping in Chrome, IE, & FF. Rumors about Safari. Akami, nginx looking at it, varnish is rearchitecting to support, IIS should support

mnot: lots of tests, partiuclarly of Japan.

timbl: why is Apache not interested?

mnot: not sure. Not a string impetus in that community to do it yet. Perf benefits are uncontroversial and that's going to create some market pressure to implement.

[discussion about how to get the benefits]

mnot: expect to see the webperf community align around experiences about this.

mnot: background discussions about HTTP/3. Lots to do; connection coalescing, security, UDP transport. IAB workshop in Jan about UDP-based transports. Feedback will filter back to IETF.

slightlyoff: what experiements besides QUIC are happening for UDP transport?

mnot: lots of these floating around. Akami has a product. MSFT research. etc.

domenic: MinimaLT was an impressive experiment in this area. Also like the HTTP/2 working mode where experiments come back to the spec over time.

mnot: encouraged that we now *have* an HTTP community. We didn't have one 5-10 years ago. Lots of new participants. Lots of focus on long-term evolution.

slightlyoff: what changed?

mnot: we started HTTP/bis to re-document HTTP 1.1 and that snowballed. Took several years to re-build the mailing list. When we started HTTP/2 we had a lot of f2f meetings and that really helps.

dka: having a metric was great.

mnot: there was an existing web-perf community that we could talk to and that helped us connect to the rest of the world.

dka: one of the other docus you were working on was about opportunistic encryption. What's going on with that?

mnot: only on impl on the client (FF), but it doesn't seem to be getting tremendous momentum yet. Lots of discussions about tradeoffs; does it make the security a tri-state (vs on/off)?

mnot: expect something to get published, but not sure if it'll actually get used on the web.

[discussion about scenarios about opportunistic encryption; problems with cert deployment, e.g. to printers]

mnot: the bit carrot is low-friction; not validating the server is part of that.

dka: what's the view to how HTTP/2 will get used inside data-centers?

mnot: HTTP versioning is hop-by-hop; lots of systems can insulate those systems with a front-end

mnot: one of the issues with HTTP/1 was connection handling; e.g. at Yahoo, a constraint was the # of the open connections supported by a switch in the middle of a system. HTTP/2 makes some of this better. Front-end/back-end conversations can *probably* benefit from encryption, but there's lots of ways ot meet that requirement.

dka: other topics that aren't encryption?

mnot: we're starting to talk about 451 again -- "you're being censored". 2 use-cases:
	- the server is being asked in a certain jurisdiction to block some content

mnot: if people have thoughts about if it's a good idea, now's the time.

[discussion about gag order vs. transparent blockage]

[note that we should talk about captive portals]

[everyone plays with their cookie- and ad-blocking settings]

[discussion of how sometimes third-party cookies are not malware]

[451 draft: https://tools.ietf.org/html/draft-tbray-http-legally-restricted-status-05]

mnot: there are upcoming IETF meetings. TLS 1.3 is coming along. RTCweb is coming along. 

TOPIC: future meetings

dka: April 20th Extensible Web Summit, with O'Rielly space that sounds suitable; April 21st-23rd F2F needs host. Possible hosts: Mozilla, Akamai, Telefonica.

dka: beyond that we don't really have a plan. Back to MIT at some point?

timbl: in the summer.

yves: Robin offered to host us in Paris

dka: usually April, June, Sept, TPAC, ...

[discussion of scheduling relative to www conference; AC meeting; hot Australian summers; ...]

Proposal:

- July 15-17 Paris (hosted by Robin or Akamai)
- Sept 14-16 MIT
- Jan 12-14 Melbourne (tentative)

Chair: Peter
Scribe: Jeni

TOPIC: Do Not Track

mnot: so what do we think?

domenic: I think it's silly, I don't see how anyone envisioned it working. If we were really protecting users we'd turn it on all the time, but if it were on all the time then it would just be ignored.

timbl: Talking to regulators in Europe...

domenic: oh yes, you said that this gave hooks for regulators to use, when I think of it that way then it's more sensible

timbl: you're trying to build a world, and they're prepared to make laws. If they make a law about what people can and can't do, they need technological hooks. The mathematical justification is that you have a whole load of use cases where you have different motivations & concerns between industry and the consumer. If you try to design a social system for only one case the tension is quite high; if you have two cases and enable toggling between them maybe the overall happiness is higher. But it's crazy to design the technical piece without the regulatory piece.

mnot: DNT is getting one thing right by having a single bit (in contrast to P3P which never turned into anything). It was deployed by Microsoft...

timbl: everyone put out P3P digital policies, because IE wouldn't browse a site unless you had one, so people put up a P3P policy but no one followed it up.

mnot: the P3P policies are just text files that say 'this is not a P3P policy'. The regulators didn't have the stomach to use that mechanism to enforce anything. I've talked to Thomas & Wendy about DNT, and to me it never made sense without regulatory support. And it seems like the working group has been captured by the industry, which has lots of resources.

domenic: there was a recent thread about this, but I don't know about the current status

timbl: there were no regulators present

dka: the original impetus was from the FTC, they were the ones that came up with the idea

mnot: they thought it would be industry self-regulation. It's a protocol that asks the participants to act against its best interests

timbl: lots of things in protocols are against their best interests, lots of people do things that are in the community interest; it would be sad if we could only design protocols that work with people's best interests

mnot: you can't have an HTTP header that stops the messages being used

dka: in the context of private browsing modes: should we add DNT: 1 to private browsing mode? it would be in the best interests to pay attention to the bit in that case because everything in private browsing mode isn't untrackable anyway, so you're not going to get paid for that anyway

[domenic suggests in that case serving porn ads]

mnot: that would give an incentive to browsers to always send DNT

dka: I'm saying that would be an alignment of concerns

mnot: but it doesn't cost them anything to do it, and the session might give information even if it's epheremal

domenic: I think it could be an interesting bit in that case

dka: isn't there legislation in eg CA that mentions DNT?

mnot: I don't know what the regulatory situation is in America & Europe; if Europe were involved in this more, it would be something stronger. It seems pessimistic to design for America

dka: Wikipedia: http://en.wikipedia.org/wiki/Do_Not_Track_legislation - not all of this is existing legislation, some is just proposed

[see california California Assembly Bill AB 370 - passed legislation which references DNT]

mnot: I brought this up because whenever I talk to technical people about DNT, it's refered to as a cautionary tale, something that is broken. As the TAG, should we try to position it, what the longer term vision is? Should we try to affect it? Is there something we could do? I feel that it's making W3C look bad.

domenic: I wouldn't even try to salvage it.

mnot: Do we try to say that we don't have any faith in it?

domenic: I don't feel confident in my opinion, I just feel we shouldn't say anything

dka: as you pointed out, it's right to have a bit. We've talked before about having the bit of 'I'm a child'.

mnot: the semantics of that were 'I prefer not to see particular types of content'

plinss: but a flag that said, 'It's illegal to show me particular types of content'

mnot: the 'safe' hint isn't about ads, it's about objectionable content, where there's a good alignment of concerns, eg porn sites are under legislation about not serving porn to children. 'Safe' hint is going out for last call now. It's in IE, Firefox, YouTube, Bing support it.

dka: I'm not sure there's anything the TAG could say that would help or hurt

timbl: maybe to draw analogy with the 'Safe' bit, to say that without regulation it's not going to be effective

mnot: in a few years it would be interesting to look at P3P, PICS, Safe, DNT, we've had stabs at policy on the web, what can we learn from it

timbl: right now we should be steering the W3C to do useful things, it's the TAG's job to make people to step back

mnot: maybe we should educate ourselves more and see what its current status is

JeniT: there's a bunch of things matching policy & technical eg robots.txt, POWDER

plinss: DNT isn't going to work because it doesn't make you untrackable, bad guys will ignore it

dka: that relates to private browsing, if you're going to be untrackable, we need to think about fingerprinting etc, which would point to having no DNT

timbl: I disagree that this is the right route; the way I think that privacy is going is building accountable systems rather than locking down what gets shared. There are lots of reasons and ways in which you are going to be held accountable, because you have a process and if you're not good someone will whistleblow. They aren't the systems that lock things down, but that track use of the information, so that the user of the information can be held accountable. I think the way we're going is tracking how data is being used, and this will be driven by companies trying to do the right thing. Or it might be companies being forced by legislation to do things. And yes there will be cases where you're in an oppressive regime and you're gay then under those circumstances the protocol is completely different. But in the friendly case of commerce in states where the law isn't dysfunctional we have a different approach.

plinss: I think we can help guide new systems & protocols and understand what gets exposed. I don't want to build new systems that make it harder to have your traces hidden

mnot: I wonder if we should tell the DNT working group to target legislation

yves: they are already working on that

slightlyoff: practically with browsers, the train has left the station. If you got to the extensible web manifesto, we're talking about being able to observe things that aren't currently observable. I feel like it's a different project than being upset that the fingerprinting train has left the station.

plinss: say there's 20 ways I can fingerprint a browser; if I add 5 more ways that enables 20 more methods, it just makes it easier and easier to be narrowly trackable; the attitude that 'it's already so bad it doesn't matter if we make it worse' bothers me

slightlyoff: I'd like to work on problems we can actually solve

mnot: there are people who are actively trying to minimise their profile (eg TOR browser) and we shouldn't make their lives harder

slightlyoff: does the TOR browser remove all persistent features?

mnot: yes, most, and they're continually working on it

slightlyoff: the question is really about the maintenance burden on them, which is the same question as we'd have about identifying the privacy preserving mode, right?

mnot: I'm not saying don't add any fingerprinting bits

slightlyoff: I'm trying to figure out how we could assess the cost

mnot: it's hard to quantify because there are so many ways in which people use the web

TOPIC: private browsing

http://w3ctag.github.io/private-mode/

mnot: I did a proto spec on private browsing mode last year; during TPAC we had a dinner on Monday night with good representation from all the browsers except Chrome, though I've had other discussions with them; also UK government; we had a good discussion about the document. I want to pare it down to get to a Recommendation that defines "private browsing mode" for other specs to reference, eg 'and when in privacy mode you do X'. It doesn't seem controversial to document what private browsing mode is right now. There's more in the document about machine, server etc. Right now it's just the on disk attacker or person using the browser next etc. So let's document that and extend the scope later. I want to think through a bit more what that roadmap would look like.

domenic: what have you found about divergence between browsers currently?

mnot: I haven't done that research but someone else has

domentic: that would be a good driver for browsers

mnot: I'd like conformant browsers to point out that people aren't being protected from particular attacks in normal mode

domenic: the incentives aren't there

mnot: the nice thing about private browsing mode is that it's a flag from the user about the expectations they have, eg if they try to navigate to an HTTP site then warn them

domenic: most of the time I use private browsing mode is not about privacy (it's about shopping for my girlfriend, obviously)

timbl: it's useful to have a single switch, but there's a difference between hiding what gift you're buying and trying to avoid the government knowing you're gay: there's a different level of warning that you want to receive if you're going to do something that isn't actually private

mnot: I don't want to make any decisions about user experience. There are 3 different types of attacks here.

timbl: I'd like to have preferences about the user interface.

mnot: the defaults are the important thing. Non-technical users are surprised that you're not really private.

dka: when I talk to them, they're surprised that it's not always like that. I make the argument that there are benefits.

domenic: part of the benefit is that it's ephemeral

dka: when we had the meeting at TPAC, we talked through some of those different scenarios and it was interesting. One of the scenarios I have is if one of my kids wants to use a site they like and I don't want to see it in my browsing history

domenic: similarly, my girlfriend checking her mail

dka: but that's not private browsing

slightlyoff: it's ephemeral browsing

dka: the other case is medical symptoms checker: you don't want it in your history. This has happened to me.

mnot: let's congeal what we know and build on that: protect against the disk-based attacker, explicitly not protecting against the networked attacker or fingerprinting

dka: I think it should protect against fingerprinting

domenic: currently private browsing mode is really about ephemeral browsing

dka: or doing a search on your name on Google and not wanting it to be adapted

domenic: if Google used supercookies instead of cookies it wouldn't give you that experience

dka: I think it should give me that experience

mnot: there's state that is in local storage and then there's fingerprinting surface from more accidental things, it's not User-Agent or fonts on the system, but state that has been purposefully set from the server

slightlyoff: from the point of view of the attacker, which is more useful?

mnot: we need a spec that others can refer to, and a separate spec about fingerprinting surface and the considerations around that

dka: +1

mnot: lumping it all into one bit is too much; browsers might make a UI decision to lump it together

dka: the other aspect is education; I talk about private browsing mode to other parents, there needs to be more education about it, from governments & NGOs. Having something independent from vendors could be useful. The other point is that the iconography is all trenchcoat & shades, but these use cases aren't that. The current private browsing mode reinforces that it's nasty. 'Low impact browsing'

mnot: maybe publish from webappsec so it can be a Rec? There's browser interest, privacy community interest. I'll take an action to rewrite.

plinss: I think there's consensus to continue work in this direction.

slightlyoff: I'd like to know what TOR does & doesn't turn off.

mnot: look at https://www.torproject.org/projects/torbrowser/design/#fingerprinting-linkability

TOPIC: "same origin"

[Related news: http://www.theverge.com/2015/1/5/7494731/gogo-in-flight-wi-fi-is-spoofing-its-own-customers]

domenic: I'd like to get to a ToC for this document. We need to discuss the target audience

slightlyoff: start from the idealised multi-agent model & build from there including all the stuff that's grandfathered in

timbl: in all this there's no concept of a trusted app

domenic: the point is that if you trust one of the actors but you don't trust the others. I can give access to my microphone to one origin and not to everyone else.

slightlyoff: you could imagine a model that provided path-based access

domenic: or a whitelist-based access or an appstore-based access

timbl: if you allowed paths you wouldn't have to have subdomains, which would mean more privacy

slightlyoff: you still have all the same problems

timbl: you may have the same problems, but the problem you solve is that having to use a domain-based system exposes what you're doing even using HTTPS, and it's a pain because a new app requires a new domain. It makes running a web server more complicated; it's not a simple space like AOL hometown used to be

slightlyoff: this is automated pretty well with wildcards

timbl: because someone has written the code, but it's a decision that's been made that prevents you from using the path, and the domain is exposed whereas the path is private

dka: the IP address is exposed

mnot: this is an important document. Through the extensible web, with fetch, you could have a different interface with a new security policy, so is the primitive something different

domenic: fetch API is only as powerful as XHR currently. The idea is to enable the primitives to support the grandfathered stuff and the idea is an opaque response that you can only push into the canvas

slightlyoff: you get a response that has an apparently unknown body, only trusted parts can actually get it

mnot: I'm just wondering if people are going to write their own security models

domenic: the point is it's baked in, with few exceptions, and fetch won't let you work around this.

plinss: a lot of this is post-facto

mnot: cookie options in Safari are interesting: block all, allow all, allow from sites I visit, allow from current website only

domenic: this stuff is about reading/executing stuff from another site, whereas cookies are about what data you send when you make the request, it's connected but I don't think it fits in

mnot: we could talk about same origin in relation to cookies

[discussion of use of cookies & origins]

slightlyoff: writing document.domain should be covered - you can write it to be a more general origin

plinss: I think I read the automotive working group is looking at using a different origin model

[digression into gun type ENUM]

topics to cover:
            
  - what is same origin policy
  - explain cross-origin canvases, why you can't access pixel information
  - scripts execute in an origin
  - CORS headers
    - they're almost always safe
    - why opt-in instead of opt-out
 - granfathered stuff: `<img>` & `<script>`
 - synchronous script access (oop iframe?)
 - abstract agent model
	 - isolated by default
	- compare with OS processes
  - isolation allows permission-granting (mic, camera, etc)
  - permission grants to HTTP = grants to all origins
  - cookies break this mostly
  - document.domain

timbl: I have an app that doesn't work at the moment because originally it just could use XHR, but now it doesn't work. It used to be that in Firefox you just had to ask for permission (universal browser read), and it would remember that you'd granted the permission. It doesn't work any more because the user isn't trusted to give permission to scripts.

domenic: it's a hard permission to grant, you're saying you trust the app to be you

timbl: the problem is ambient authority

timbl: we need to separate the model from the attacks. The jump to assume that everything on HTTP is read & available is extreme. It wouldn't be easy for me to intercept your HTTP traffic while you're sitting at home.

ToC:
    
- intro: completely separate agents
	- can't XHR to another origin by default
	- message passing
	- exceptions: `<img>` & `<script>`
		- cannot read img contents, only paint them
		- script executes in the context of effective origin (JSON-P)
	- CORS headers allowing collab [where to talk about turning these on all the time] (vs server proxy)
	- granting sensible permissions (mic etc)

A: ambient authority / CORS / credentials
B: HTTP = all origin 

domenic: I'm happy to start writing prose. I'm not sure how to frame the CORS story & make the recommendation to use it.

[timbl writes matrix of no cors / cors / wildcard cors vs origin, different origin, http vs credentials flag]

timbl: In case it isn't obvious, I feel this is terribly broken. When you're writing code that's going to do general stuff, you can't determine whether to set the credentials flag for example. We've cheated for scripts & images. It comes down to that I can't build apps with the power of a native app because of this policy.

slightlyoff: we're missing an API for privileged network access

timbl: we had that API in Firefox (and IE as well I think); what's been removed is the ability of a user to "install", to trust a web app as a user agent.

slightlyoff: we haven't got an API to bless an origin to break the origin rule. When we look at push notifications & other APIs, we've bucketed them into origin-preserving & origin-breaking. TCP socket access is an example. We haven't got the browser super power. Origin breaking things require more trust. The user agent still has to give you the ability to audit who has the powers and enable you to take them away. The DAP WG has done a TCP/UDP API.

timbl: so the most practical way of writing such an app is to rewrite the HTTP stack to use the sockets?!?

slightlyoff: it would be possible to have an HTTP stack available in user space

timbl: the reason we're not doing this is because we don't have a philosophy in which some apps have complete power, even though the browser has complete power

slightlyoff: I would like us to get there. Pretty much everyone wants to stick to origin-preserving APIs. How does the app get the power?

timbl: you could put it in an appstore which is managed

slightlyoff: CSP is an enforcement model there. CSP is a policy enforcement mechanism.

timbl: CSP can only decrease my power.

slightlyoff: we've tried the appstore thing: Chrome has had multiple appstores, Firefox too. Packages have lots of downsides. You could imagine a developer programme so you can verify the developer.

timbl: I've discussed 'beneficient app', a branding label. Meanwhile, why do we have to have CORS on everything.

slightlyoff: it's a question of balance, who is it good for

domenic: an easy example is XHR to any origin I could take over your wifi router from any web page

timbl: the browser could see you're in a local IP space. It's a heuristic, but if it turned out that helped the 99%

slightlyoff: the font foundries insisted on this. They're only just transitioning to being hosted. These ships have sailed.

timbl: these aren't good examples, they're not ancient pieces of code that no one is upgrading. We're throwing away a huge amount of power. The way people build apps is proxying servers. We don't have a web where people's computers talk to each other over the internet, they all go through these silos. The whole CORS debacle is driving everyone to make all the interaction go through the server. You build things which aren't really distributed, it's all going through the silos. What about WebRTC

slightlyoff: it does have a data channel

timbl: you can talk to other clients, but not to servers. What about writing the scenario: what would it take to dismantle CORS?

dka: do we have enough to write a document on the here & now?

domenic: yes. I want to bring up a crazy idea: what if browsers came with a proxy so you could do anonymised XHR & have browser vendors host a proxy that the traffic all runs through

[everyone: err, maybe not]

slightlyoff: there are browsers that sort of do that with an optimising proxy

dka: those proxies don't work on HTTPS content, right?

slightlyoff: that is correct

dka: doesn't that mean the proxy has an end-of-life as more of the web gets encrypted

mnot: the Google proxy may, the Opera proxy, one of them won't. Split browsers MITM TLS, and it's hard to know what they're doing. You can't test what they're doing because it's not on the network. I've been talking to people in the IETRF about this, because they're getting very very popular. You download a browser, it does whatever it wants to do.

dka: from the implementer's perspective, they're implementing TLS properly from their server

mnot: I don't know if we can say anything useful about it, there should be education around it, you need to be an informed consumer

slightlyoff: incognito tabs don't go through the Google proxy is the other exception

mnot: the one I was talking about was UC browser, which is huge in India, 23% of all usage

domenic: I like the squirrel icon

mnot: UC browser mini is a split browser. Opera mini actually say what they do & Norway is good about data protection. You just have to trust Norwegians. With Chrome you have to trust Google. You can verify software you download, but not stuff that happens in the network nearly as easily. Split browsers are accelerating pretty quickly. From an architectural standpoint we should be aware of it.

dka: I think it's specifically interesting in the context of the move to HTTPS

mnot: in terms of the pressure that it might add to that tendancy?

dka: it's one thing to consider Opera mini in the context of unencrypted sites, but something different with HTTPS where they're essentially MITMing

mnot: this is already the case. For some people that's OK. I don't think it's OK that users in general don't know that split browsers are doing this. The interesting question is when everyone moves to HTTPS and telcom companies want to relieve pressure by installing a new root CA routing everything through their proxies

dka: so who's going to do this?

domenic: I could bang this out in an afternoon

slightlyoff: I think you're optimistic, how about I volunteer instead as an "interested outsider"?

TOPIC: WebIDL

domenic: this topic was brought up on the mailing list a while ago. WebIDL has a v1 and a v2 branch, neither of which are complete or publishable. v1 is generally not maintained, whereas v2 is growing and in non-backwards-compatible ways. Someone was saying they wanted to push v1 to Rec, and that would be the wrong thing to do. WebIDL spec editor is overburdened. There are tons of open bugs on both versions. I don't know where that leads us; the discussion died down. v1 is factually incorrect, no one should use it.

dka: is there value in putting effort into bolstering v2?

yves: v2 evolved because of new types and promises, parameterised types etc. v2 is where new technologies from TC39 are put, so it can't be stable.

domenic: it's fine to have a master branch & an outdated branch, but we shouldn't be keeping them in parallel. The assumption was for v1 to go to Rec, but that's not how things have worked out

dka: so v1 should be deprecated?

domenic: yes, but it's harder because of the resource constraints. Ideally v2 would be getting more love & there would be WDs & CRs etc. We have an illusion that v1 is more stable because it's in CR, but it's been that way for 2 years; it's abandoned.

yves: it's not abandoned, there are new issues against it. There are a lot of things like sequence that are defined in ES5 rather than ES6. For those using it as documentation...

plinss: there's so much of v1 that's incompatible with v2 is the problem, it should be pared down to what's compatible

domenic: what would be left is the BNF and not all of it, and that's a waste of time. I don't know if there's an action item; we could encourage v2 but I don't see how concretely

dka: is there an action to inject some positive energy into v2?

domenic: I have 2-3 PRs merged now. Part of the issue is systemic. Someone needs to spend at least a solid week on the spec. The toolchain used is hard to work with (it's XML). It's oriented around a language-independent ideal that doesn't work. Anne has been trying to get me to do this for a long time, but I don't have time.

dka: if there's expectation that v1 is going to Rec, there's a discontinuity there, perhaps the TAG should say how we think it's going to happen, paint the future history of WebIDL

timbl: this is producing a disproportionate amount of angst from people who don't really rely on it

domenic: if we could paint that future history, the plan we see, eg having periodic snapshots of WebIDL v2

plinss: there's not even a published WD for v2. It should at least be a FPWD.

domenic: I could draft a response saying "this is what we think", and see what the TAG thinks

yves: if v1 has most of v2, maybe we could publish what's currently in v2 as Rec while still having an editor's draft

pliss: pull it out of CR, go back to WD with the v2 material in it

TOPIC: spec review planning

dka: new stuff that we're not currently reviewing: what should we be adding to our spec review queue?

domenic: there are a couple of proposals, one on media controls (early stage, not necessarily architectural)

yves: there's joint work on editing from the editing task force

domenic: DOM 3

dka: web payment?

mnot: I reviewed a number of specs because they're making amendments to HTTP. They're ambitious. They're trying to establish a new standard for identity on the web. The whole payments thing is interesting too. I'll probably track that on an ongoing basis.

dka: that seems like something we should add to our list of things we're keeping an eye on, maybe an action on mnot to add it to our Github issue list?

[discussion of potential April 1st TAG Findings]

[Bittorrent browser: http://blog.bittorrent.com/2014/12/10/project-maelstrom-the-internet-we-build-next/]

Dka: question - does anyone know anyone at Bittorrent?

dka: the TAG has often touched on what a P2P architecture for the web might look like - is this something that could be speccable? do we know what the Bittorrent folks are doing? Should we be thinking about it?

mnot: I've looked at it: Bittorrent is all poprietary. They have a P2P web caching thing now. This goes back to SRI & privacy & the tradeoffs inherent in that. If you're using a P2P model you're broadcasting everything you browse.

dka: that argument is often used to stop any line of thinking around P2P caching. When this news item came up, it struck me that there could be another approach that could allow the community to have their cake & eat it.

mnot: there's a technique called 'private information retrieval' but it's not practical at web scale (according to AT&T researchers). there are other ways to slice this, SRI seems like it's the best hope we have right now. It allows an origin to flag the content that it thinks is public for reuse. My understanding is that the browser security guys are interested in that use case, but they want more experience first.

dka: as far as we know, we think the Bittorrent thing is proprietary so we shouldn't comment on it?

mnot: yeah

Domenic: https://specs.webplatform.org/html-aria/webspecs/master/ ?
[4:57pm] Domenic: https://github.com/w3c/editing-explainer has three links
[4:59pm] Domenic: https://w3c.github.io/webappsec/specs/powerfulfeatures/ of course
[4:59pm] Domenic: http://w3c.github.io/nfc/index.html
[5:00pm] Domenic: https://w3c.github.io/frame-timing/ !!
[5:06pm] Domenic: http://research.microsoft.com/en-us/people/mickens/ToWashItAllAway.pdf

ADJOURNED

