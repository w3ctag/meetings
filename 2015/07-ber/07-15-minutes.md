## TAG F2F - Berlin (Day 1)
### July 15 2015

[Main Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/07-ber/agenda.md)

### Contents

* Agenda Setting
* IETF Update / Liaison Issues
* End-to-End Encryption
* Security / Joint Work with WebAppSec

*Present:* Daniel Appelquist, Hadley Beeman, Tim Berners-Lee, Yves Lafon, Travis Leithead,  Peter Linss, Mark Nottingham, Alex Russell, Yan Zhu, David Baron

*Special Guests*: Brad Hill, Wendy Seltzer, Charles McCathieNevile, Mike West

*Scribes*: Mike West, Travis

*Chairs:* Dan Appelquist, Peter Linss

[Scribe setup]  
    Wed AM - Mike West  
    Web PM - Travis  
    Thu AM - Hadley  
    Thu PM - David  
    Fri AM - Yves  
    Fri PM - Wendy  

*Topic*: IETF updates

mnot: IETF is meeting in Prague next week.  
... Haven't had a liason call in a little while.  
... Joint leadership meeting between W3C and IETF is difficult to make happen.  
... ISOC is holding a dinner that night in Yokohama, W3C folks are invited.  
... Usual sorts of meetings in Prague. No active liason issues?  
... HTTP/2 is done.

dan: WebRTC?

mnot: Loath to get involved. Self-managing relationship.  
... Rechartering issues on the W3C side.  
... IETF side is quiet.  
... Web Push: protocol part of the Push API.  
... Martin Thompson active on that.

dan: Anything to review at this point?

mnot: Protocol document could be reviewed.  
... I looked at it, gave some feedback.  
... Looks like it works.

dan: Add it to our review list?

mnot: Sure.

Hadley: How is reception/take-up for HTTP/2?

mnot: Implemented by all major browsers.  
... All require encryption.  
... Mozilla does OE, no other browser does.

tbl: Requires an "s" in the scheme?

mnot: Yup. All except for Mozilla.  
... Sat in on WebAppSec meeting yesterday. Might be other interesting formulations based on those conversations.  
... Go back to HTTP working group, see whether there are things we can do together.  
... OE: Don't check the cert, don't change the UX.  
... Might be interesting to change those properties.

brad: Interesting possibilities if we can make all the guarantees we expect without tying them to the scheme.

mnot: Not clear whether we just need to leave the door open for that in the OE spec, or if we need to do some work.

tbl: Current OE draft hasn't moved much?

mnot: https://httpwg.github.io/http-extensions/encryption.html
... Implemented by Mozilla (Fx39).  
... Only thing it helps with is passive attackers.  
... Downgrade, MITM can easily subvert.  
... Is controvercial as a mechanism. Other browsers have little interest in implementing.

tbl: If cert is available, are they checked?

mnot: Not mandated. Allows you to build something on top if you like.

tbl: How does it work?

mnot: Listen on a different port on the same hostname, send a header to do the upgrade.  
... Not a redirect, an advertisement that your origin is available on a different port with TLS.

tbl: Like HTTPS (HSTS?) from then on?

mnot: No, succeptible to downgrade attacks.  
... Best effort.  
... Was interesting enough to Firefox to implement it.

Wendy: Not a substitute for HTTPS.  
... If the W3C does the HTTPS upgrade, then everyone should just see the HTTPS version of the site.

tbl: We can use a real cert, prove OE works without changing links?

mnot: Cert isn't checked. Downgrade.

dan: We should talk about the things Brad proposed in WebAppSec.

tbl: Lots of discussion before, should chat more this afternoon.

[Noting that [Brad's document](https://github.com/w3c/webappsec/blob/master/admin/100\_percent\_https\_roadmap.md) should be on the agenda for this afternoon]

mnot: If OE isn't going to get broad adoption, we shouldn't publish the doc.

dan: HTTP/2 was presented at a websec meetup in London.  
... Good presentation, good to see folks talking about HTTP/2 who aren't mnot.  
... Lots of skepticism in the audience wrt server side implementation.  
... Performance questions.  
... Apache?

mnot: Server-side has lagged. Now seeing more adoption.  
... mod\_h2 is landing in Apache, will be backported to 2.4.  
... Varnish is rearchitecting to support H2 (EOY).  
... Nginx by EOY.  
... IIS is shipping in a few months.

dan: Push?

mnot: Server push is experimental and new.  
... All of HTTP/2 fits into the footprint of existing APIs.  
... Push is new and we need more experience with it to understand how best to use.

Travis: server-sent events?

mnot: Very different.  
... Server can push a synthetic response into the browser cache so that a later request will resolve right away.  
... Cancel the push if the resource already exists in the cache.  
... Akamai is experimenting with it. Not sure how to expose to customers yet.  
... Prioritization is more worrisome: all the browsers have different ways of serializing prioritization.  
... Talking about that in Prague, with Ilya, Alex.

alex: Adds requirement for delay in order to understand prioritization.  
... mnot pointed out that there are workarounds, but that choice creates challenges for implementers.

mnot: Also not cheap for servers.

alex: is it possible to change that mechanism?

mnot: Sure, as an extension, or by using the existing scheme in a constrained way.  
... Showing citizenfour in Prague on Sunday.  
... Will be crowded, get in early.  
... Might want to do the same thing at TPAC.

wendy: Few other bits and pieces that I'm watching.  
... dbound http://datatracker.ietf.org/wg/dbound/charter/

dan: What is that?

wendy: Formalizing the administrative boundries of domain control.  
... Include subdomains? At what level do you do the assumption that a host controls everything above it.

brad: Ambitions to make it bidirectional as well.  
... More complexity than exists in the current model.  
... Is at least being contemplated.

mnot: Better than PSL, but feels very hope-based.

wendy: ICANN SSAC report was even more hope-based. https://www.icann.org/en/system/files/files/sac-070-en.pdf

[Dan realized that we didn't actually do introductions; we're doing them now]

yves: SNI? DNS in the clear.

dan: Key topic! Middleboxes are very keen on keeping SNI unencrypted.  
... That's the one hook they have left to understand where users are going.  
... So the sooner we fix that the better.

[Cheers]

mnot: Deep topic. Right now TLS 1.3 doesn't encrypt SNI.  
... Too hard for too little gain.  
... Another key-exchange.  
... Only benefit is when many sites share a common IP address.
 ... Effectively CDNs.

tbl/dan: Not just CDNs. Hosters!

dan: Bluehost is less than awesome, but is hosting hundreds and hundreds of sites on each box.

mnot: Problems:  
... 1. Old IE (XP before SP3) and Android 2.2 don't support SNI.  
... 2. If on a unique IP address, then encrypting SNI doesn't buy you anything.

tbl: Chicken/egg problem.

mnot: Sure. If it had been introduced earlier, it would have been easier.

yves: Mandating SNI is tricky, because it is locking out people.

mnot: 2k refused connections on my blog daily.

tbl: Error message?

mnot: Nothing meaningful. Logged an issue with Apache, haven't gotten traction.  
... Still supporters in the TLS discussions.  
... Emerging discussion in IETF about supporting network management needs (QoS, UDP+NAT, etc)  
... Mechanisms being talked about add plaintext metadata to streams.  
... Might include a variety of things, ranging from network data to customer data.  
... Big concerns around transport metadata.  
... Hard problem, constrained vocabulary might be a solution.  
... Arbitrary extension would allow telcos to add arbitrary metadata.  
... Might be in the customer's interest, might not.  
... So that's fun.

alex: Fine?!

mnot: Fun.  
... Customers unaware of mechanisms that allow ISP to talk to sites on my behalf.

dan: When arbitrary data can be included?

mnot: Right.

dan: What's the reaction to the constraint proposal?

mnot: I haven't published the draft yet.  
... If you push them hard enough, they'll do backchannel communication (cookies, DNT).  
... Difficult balance.

dan: Is this mechanism going to be discussed at IETF?

mnot: Proposal called SPUD. UDP-based framework for building new protocols friendly to netboxes.  
... Various ways to do this. Packet header in UDP. TCP options. Wrapper in TCP outside SSL.

dan: Mentioned middleboxes, network operators. What about use cases around malware protection?

mnot: Firewalls?

dan: Corps want to protect their networks. Monitor the traffic that goes through the firewall.

mnot: Different topic, also contentious.  
... Seeing a lot of pressure.  
... Web browsers allow you to insert a new root into the local trust store.  
... Pressure to accomodate that in the standards.  
... Browser vendors don't want that to happen.  
... "Can do virus scanning at the endpoints."  
... But folks want to do it at the border.

mnot: BoF about captive portals. Want to see if we can do anything about them.  
... Draft for new DHCP option which advertises a URL.  
... Not proven that that's going to get implemented in OS.

tbl: At the HTTP level?

yves: Need a mechanism to say that DNS resolution was noncanonical.  
... Some folks tunnel traffic through DNS.

mnot: Things stuck in cache for days afterwards. Captive portals are terrible.  
... Pessimistic about the effort. Lots of people agree that captive portals are bad, but no implementers in the room.  
... Need the attention of the captive portal vendors and Android/iOS/Windows/OSX in the room.

tbl: Who at the IETF is repsonsible for getting folks in the room?

mnot: We don't have a staff. :/  
... Have people in the right companies who say they're talking to people.

tbl: You have to plan out to what extent deploying a custom thing will work. If it doesn't work, what do we do next?

mnot: Could maybe make this thing work by creating a funnel: if you work this way, better user experience, etc.

tbl: Two types of portals:  
... Airport type, ad supported. Want you to see the ads.  
... Other type, universities require login, T\&Cs, etc.

mnot: More and more networks don't require a captive portal. They might be getting a bad-enough rep that there's hope.

tbl: Is there hope for agreeing to let the portal remember your MAC address to tie that to permission?  
... For BA or MIT, I'd be happy to let them track me.

dan: What about MAC randomization?

mnot: What I'm finding now is that I need to change my MAC address manually to make the portal work.  
... Not sure a standard will help there yet.

dan: What about a fully-encrypted web?  
... Number of sites I can go to to trigger a redirect is dwindling.

mnot: Sure, this is where DHCP could help in a mythical future.

tbl: If DHCP, would that be encrypted?

mnot: No, DHCP is incredibly insecure, so this wouldn't make things any worse.

plinss: They should have a cert, but they don't.

dan: Let's Encrypt solves, right?

tbl: Why do portals have less security than anything else?

plinss: Usually just a turnkey solution. Dropepd in with no staff.

mnot: `file:` URI scheme.  
... Matthew Kerwin working on a draft.  
... Talking about bringing back Gopher.

hadley: Want to make sure the 'file:' work connects with URI scheme stuff in the Data on the Web BP WG

tbl: gopher\_s\_, right?

mnot: Error reporting.  
... We found that HTTP-based protocols generally defined their own error formats. Tries to standardize in order to avoid the problems that causes.

tbl: Does it nest?  
... Most important thing about errors is nesting.  
... In most cases, you should have an incoming error, produce an outgoing one, capture all the information about what happened inbetween.

mnot: Status code?  
... Multi-status status code.  
... Defined for WebDAV.  
... Poorly defined, poorly implemented.

tbl: Not surprising.  
... Important relationship is "because".  
... "500 because of TLS error" or whatever.

mnot: Right now, "root status code", details in extensions.  
... Could recurse if you wanted to.  
... Should add an example of that.  
... That it for IETF stuff, I think.

[Break until 11. Lunch at 12:30.]

[Discussion of tbl's strange, glowing box]
[He claims that it's a battery. Chaals is not convinced.]

[And we're back!]

mnot: HTTP Workshop: https://httpworkshop.github.io/

dan: Will there be a dial-in?

mnot: No. But I have stickers!

[HTTP workshop agenda](https://github.com/HTTPWorkshop/workshop/wiki/Agenda)

mnot: Folks coming who don't generally get involved in standards.  
... Looking forward to it.  
... Will release notes, but probably not detailed minutes.

hadley: Trying to get a different crowd?  
... What do you do in the case of a conflict?

mnot: Mostly a socialization event. Bring community together, put faces with email addresses.  
... Outcome will hopefully be a list of things that are interesting to talk about in a standards body, not decisions in themselves.  
... Not trying to fork the process. Still at IETF.  
... If anyone wants to come, we can probably arrange it.

dan: Do you feel that W3C will be underrepresented at this event?

alex: Do we need to care about this level of the stack?  
... Are browser folks there?

mnot: Yup. Along with CDNs, network ops folks, server folks, Tor, researchers. Etc. ~40 people at the moment.

*Topic*: End-to-end Encryption.

Intro: Some governments feel pressure to demonstrate that they're catching criminals and terrorists.  
... At the same time, their own security and much of the economy is built on encryption.  
... This can lead to confused messaging.

What's the TAG's role in this? The TAG might draw a few conclusions:  
... - Parts of the discussion are missing technical expertise. Could we be that expertise?  
... - Governents will still want to catch bad guys. Is there another way for us to help them meet that requirement?

alex: To what extent does encrypted communication actually hinder the ability of intelligence services?

mnot/wseltzer: We could throw our weight behind particular documents, e.g. http://www.cl.cam.ac.uk/~rja14/Papers/doormats.pdf

tbl: From reading reviews of it, it makes a statement that keys under doormats are a bad idea.

wseltzer: TAG could contribute a "Why this is a terrible idea" statement from a technical perspective.  
... Keys under doormats specifically calls out standards.  
... TAG could respond to that explicitly.

tbl: What was the statement?

wseltzer: "If we were to do it, it raises questions around standardization."  
... Could run with that to explain why an interoperable and yet secret backdoor would be unsuccessful.

tbl: I don't see that argument.

wseltzer: How do you standardize a `backdoor()` method?

tbl: Protocol's not the problem. Distributing the key is the problem. How do you distinguish good guys from bad guys?

mnot: Perhaps they could form a community group?

dan: possible response:  
... - Open standards are best, abd could not produce backdoors.  
... - Weakening encryption on web is incompatible with making the web "fit for purpose"

tbl: The argument should be "It's a bad idea."

mnot: This is what we do in IETF, re pervasive monitoring.

hadley: Might be useful to outline potential impacts on the various specs we care about.

alex: Fundamentally breaks the same-origin model.  
... Working to get to a place of authenticated/encrypted communication.

dan: Trustable web?  
... Not just encryption, but also trust that you're talking to a particular host.  
... In what form should this document be presented?  
... TAG Finding? "Securing the Web"? Blog post? Gist on GitHub? Instagram photo? With text in the photo?

hadley: Depends on desired audience.

brad: It would be helpful for folks to be able to cite this.

dan: Ok, so something at the same level as "Securing the Web" might make sense.

alex: We should focus the document on those areas which we're explicitly involved in.  
... We're responsible for pretty much everything from the browser on up.

brad: Trustworthy across borders.  
... Balkanizing it into snooping zones by official policy destroys the "world wide" bit of the web.

tbl: Security of the web is fragile, under attack.  
... Government needs integrity on the web for commercial and other interests.

mnot: This finding wouldn't just be about governments MitM, but also firewalls, enterprise.

mike: If you own the machine, you can do whatever you'd like with it. The distinction between governments and enterprises seems like a reasonable one.

mnot: We should have a framework for addressing the potential slippery slope.

dan: Did folks read the [UN report I sent around](http://www.ohchr.org/EN/HRBodies/HRC/RegularSessions/Session29/Documents/A.HRC.29.32\_AEV.doc)? 
... Put the onus on corporations to respect the privacy rights of the individual.  
... Argument would be that users have a reasonable expectation of privacy, even on a corporate machine.

chaals: Signed contract for employment generally obviates this kind of thing, at least in courts.

hadley: Need to identify the audience. Different people in govt have different responsibilities, so each of these topics is addressed in a different discussion.

wseltzer: If the primary value is having another voice, then the document can be quite short. We might say:  
... "As other folks have said, XXX. We agree wholeheartedly. 
Weakening encryption would undermine prior TAG finding (Securing the Web) and the Recommendations being developed to support that trust and security (WebApSec specs)"

mnot: +1. Low effort, high value.

dan: Who's going to write something?

yan: Me! I volunteer with no prodding from anyone else at all!

mnot: I'll help.
alex, wseltzer: we will too 

tbl: Important to plan for the world in which we want to live. Should be idealistic.

dan: "TAG Decries Woolly Thinking"?

alex: "TAG Supports End-To-End Encryption"

challs: Needs a backronym.

hadley: WhatsApp has been a focus of discussion. Not even on the web.

mnot: Less WhatsApp, more vendors that don't have the keys. Signal, Apple, etc.

**AI: Yan to write two paragraphs. This afternoon.**

mnot: In that spirit, I have a fingerprinting draft that I did on the airplane.  
... Wendy and Nick didn't hate it. I'll put a link in IRC to chat about it.  
... Not really ready for the list yet.

tbl: Possible to get etherpad into GitHub?

dan: I copy them out at the end of the meeting, then clean them up and dump them into GitHub.  
... Treating etherpad as nonarchival.  
... Do we backup the GitHub repository?

plinss: Yes.

[Brief interlude to wave at small children wearing bright yellow vests, standing on top of a massive fish tank]

[some live-editing happening on the e2e encryption doc]


[Lunch happened]

*Topic*: Security

Chaals: Security is good.

[all]: agree

dan: perhaps we can start by enumerating the docs that webappsec is working on.
.. brad also presented another doc we could look at.

List of security things we shoult talk about this afternoon: 100% https roadmap; subresource integrity; secure contexts (powerful features); 

In previous discussion with TAG, we talked about ways to secure all transports without search-and-replace http -> https.  
... not sure how deep to proceed as this has already been discussed at length in previous meetings.

dan: I wanted the TAG to see this because it looks architecturally to me.

brad: Try TLS first, then try requesting over TLS, and all guarantees are met, then you can treat as secure.  
... Opportunistic upgrade:  
... if starting from a secure state, what can I and can't I do. What properties must change. 

tim: Can you explain, why we can't have 
brad: there are a lot of complicated invarients that

tim: that sounds like defeat

brad: well document title is a work-in-progress  
... just renamed.
  
... [talking through each of the sections]
https://github.com/w3c/webappsec/blob/master/admin/100\_percent\_https\_roadmap.md

[on section of Starting Assumptions]

tim: any plans from Chrome to allow webapp to find what cert is being used by the client?

alex: such as exposing channel id?

tim: on login, that is your identity.

alex: oh, client cert. No, I don't think so.  
... you could imagine web crypto giving something like that back to the user on a secure channel... just brainstorming.

brad: can the DOM access the cert it was given by the server and replay it? Currently no. (but Flash can do that)

tim: axiom 3 is controversal because user agents must be in control of how the UA trusts on their behalf?  
... I might want to ask my family/organization to trust a given cert.  
... better to have the user go to a UI where they can see all the things they've trusted. It should be more visible.  
... Could then allow more easy manageability

travis: browsers don't give such UI higher importance (than camera/mic access, for example)

brad: the same action has the ability to phish or compromize user's security.  
... facebook sees attacks where website advertises some new cert and tricks users to install.  
... for ordinary users, they shouldn't have to perform certain ceremonies to get access--promoting blind click-through.

tim: just saying this stuff should be easily discoverable

brad: in enterprise, browsers have agreed not to have an arms-race over trying to showcase where globally trusted certs are used.  
... repeating arguments that I've heard from browser vendors.  
... perhaps there's some middle-ground that could be reached

tim: I tend to think that the security space gets easily polerized to only thinking about the bad guys, and not making it easy for the good guys.

[back to review of sections: The Invariants]
brad: tranquility is probably most interesting (comes in form of mixed-content)

hadley: is "open data" a common word for non-encrypted data?

brad: it's an application data term. e.g., app wants to grab data that is open (like open-source).

hadley: wondering if the terms might be confused with other uses?

dan: you're not saying open data is always http. 

tim: some folks care about data integrity of open data, but there's a tension between the person looking at open data, and the provider.

brad: the browser doesn't perform stron taint-flow analysis, etc., at the time the data being read is going to influence the control flow of the application.

hadley: that's not specific to open-data

brad: right, but its the example driving the scenario

tim: eval of JSON, ultimately due to cross-origin restrictions... it's ironic.

brad: you might be able to improve things if you could provide a safe environment, e.g., turning off eval, enabling CSP, etc. Not sure if this would be sufficient though to allow data to be treated as data.

[No Write Down]

tim: well, there's no attack there (https: to http: ). 

brad: the browser's related dialog has been removed

david: in some ways, browsers wanted to make the lock icon mean something. In mixed content, you may not want to show the lock icon.  
... the dialog was meant to catch the common mistake of https -> http -> https.  

brad: if we imagine a world where...  
... https and http are equivalently secure...  
... on server side we don't discriminate based on schemes, we expect a policy to be applied. This would be a necesary thing to add to get to this new world (no write down).
We are exploring this in our Upgrade and Secure spec: http://w3c.github.io/webappsec/specs/upgrade/

[Tranquility]
brad: means: an application does not change between secure/insecure while it is being accessed.

Dan: Google was thinking of showing you nothing as an indicator of secure...

brad: it's not a request to change the principle of tranquility.  
... this was nice to identify as a principle especially when working on the mixed content spec.

brad: webappsec is working on building strong containment models. Once you have that you can start to talk about aggregating data in interesting ways.

dan: What do you mean by how do we handle tranquility in an upgrade model.

brad: Start with `http://example`
... later through magic, it is upgraded via TLS  
... it's tranquil  
... we then load a sub-resource over http, but something causes the resource to not be upgraded, what is done?  
... given another resource loaded at the same origin, but not upgraded, can it's DOM reach-acros to the upgraded one?

dan: consider `http://news` with lots of dependencies.  
... has lots of self-references over http (ads, news, other content)  
... If I turn on https on the main page, everything breaks.  
... I have to turn on https on all my links  
... I also have to make all my dependent partners upgrade to https

dan: we can add another interesting step by signifying "no tranquil"  
... means you can upgrade any resource to TLS, but don't show a lock--e.g., this \_will\_ be mixed content.  
... Now, we solve this interesting problem:  
... an existing secure site (https) can reference an upgradable image sub-resource. If the upgrade succeeds then it's secure. If not, then it's blocked. You've broken the deadlock so that secure sites can upgrade and not be broken by external resources (that can't be https)

david: what about iframe

brad: it's more complicated

david: I feel like the "no tranquil" flag might want to be flipped the other way around.

dan: isn't this problem (of switching to secure) solving itself?

brad: yes, but slowly

brad: many sites just don't know what their insecure edges might be until the users uncover them.  
... these sites can get regular reports on how many resources are not loaded securely  
... they can drive down to steadystate.  
... they will assess what the cost to certain revenue will be when the https switchover is made.

tim: reporting will be important

brad: yes, these could be fairly easily instrumented.

mike: Mike's Documents:  
...Content Security Policy 2 http://www.w3.org/TR/CSP2/  
...Mixed Content http://www.w3.org/TR/mixed-content/  
...Definition of Secure Context http://www.w3.org/TR/powerful-features/  
...Credential Management API http://www.w3.org/TR/credential-management/  
...Clear Site Data API https://w3c.github.io/webappsec/specs/clear-site-data/  
...CSP Pinning http://www.w3.org/TR/csp-pinning/  
...Upgrade Inecure Requests http://www.w3.org/TR/upgrade-insecure-requests/  
...Sub-resource Integrity http://www.w3.org/TR/SRI/  
...Referrer Policy http://www.w3.org/TR/referrer-policy/  
...Entry-point Regulation http://www.w3.org/TR/epr/  
...Specs moving at a good clip: CSP2 (->CR), Mixed Content (->PR, level 2 including more feature creeps), Upgrade Sec. Request (in FF/Ch already, expecting CR soon - after adding a feature requested by TAG).  
... Not going anywhere: CSP Pinning, EPR is theoretical at the moment  
... Referrer Policy is being specced (has shipped for a while)  
... Sub-resource integrity (shipping or will-ship soon)  
... Secure Context (working with Yan)  
... Firefox/Chrome have implemented CSP2, IE has implemented CSP1.

mark: concerns about site-wide CSP. Looking for a well-known location.

alex: imposing CSP is difficult - adding rules makes things tricky.also composition problems for CSP.

mike: composition issues are being addressed with CSP Pinning.  
... There are basically 2 models for pinning.  
... In model 1, define a policy that is persistent for an origin (if no other policy exists) - delivered via header (could easily be app manifest, well-known-location, etc.)

mark: my specific concern was avoiding the need for a pre-flight which is expensive.

brad: that issue was CORS. Not sure what's happening with that.

mark: with options, we have to punch through.

brad: CORS has been closed for awhile. Need a volunteer?

Brad: Well, it would live in Fetch, so you work with Anne one way or another

Mark volunteers to work with Anne.

mike: Brainstorming: for CORS, you check the flag before pre-flight. 

Mark: depends on adoption.

mike: our group is trying to tackle a few things:
    ... cross-site scripting
    ... another is "what is the minimum bar" for security on the web. e.g., powerful features  
... for powerful features, we want to only allow some features in contexts that are propertly secured. These features would have sensitive features e.g., geolocation.  
... Geolocation reveals data about [me] that should be protected  
... We need to define the context that will make a feature available.  
... Then we need to decide what are the set of features that should belong to the context.  
... For WebAppSec, we will define the context, then leave up to another group (like the TAG) to decide what features go into the context.  
... We have created some suggestions, but would love for other group to decide what features to do this to (possibly TAG?)  
... Thinking of publishing as REC.  
... Or perhaps use a review procss to decide what to do.

david: during rechartering, had some conversations with EKR.  
... one of EKR's objections was the correlation between the feature's actions and data isn't so strong.

mike: I don't want to talk about the recharter, btw.

david: I think EKR's perspective was interesting. Geoloc can be sensitive, but so can the data you submit in a form.  
... the most important thing was so push the whole web to secure.

alex: I'm not sure I see that cause and effect. From point of view of those supporting powerful features, you create a place and draw in new features into that "pole".

david: then why use the word "powerful features". Why not opt-in all new features?

alex: the word "powerful" is an easy to use/describe term.

mike: powerful things are a great way to prioritize.  
... You could say "plaintext is dead". That might be too hard to do.  
... It's easier to get the ball rolling on incremental features.  
... It's much easier to argue over individual features.  
... We have the same goal (all features secured), just using this incremental method  
... We start with something easy to talk about like security features.

alex: it's an incentive mechanism

david: one other point: things that require permission grants shouldn't be permanent.

mike: http shouldn't be more persistent. Follks proposed that cookies should expire sooner over http. (I think the cookie claim may be more about privacy than security.)  
... generally we haven't had a lot of success in talking with various WGs. Geoloc WG hasn't been able to give an answer.  
... Having the TAG help, or push this direction through review process would be great.

Alex: I think the TAG should be making recommendations about "powerful features".

alex: geofencing is already considered powerful, but because it depends on service workers, it had to be :-)

chaals: spatial data should be coordinating with geolocation group.

mike: any questions about the work in webappsec?  
... any gaps we aren't filling?

wendy: are there things the web arch. needs from a security standpoint?

brad: a few things we have coming up  
... new primitives around isolation models. Such as declare arbitrary sub-space around an origin.  
... treating information flows with new labels optionally with confinement.  
... there are some hard-to-solve issues with side-channels.

dan: how can TAG specifically help with powerful features document?

mike: there's one open issue in the document.  
... some folks have hacked around by framing a secure source and post-messaging.  
... we need to consider whether we try to shut-down the leaking problems that are cropping up? Or do we just admit that there will be some hacky problems.  
... otherwise the spec is ready to go.  
... will get feedback.

dan: the TAG/WebAppSec arrangement was that the document would be jointly offered and would have more clout.  
... we need to make good on the promise by reviewing at a detailed level.  
... perhaps we need to do this tomorrow?
https://w3c.github.io/webappsec/specs/powerfulfeatures/

Yan enthusiastically volunteers to co-edit this without any prompting from anyone whatsoever

tim: folks protecting data stores are wanting to use CORS, but they can't because they are using credentials--so they are faking it...is this the way the world should work?

mike: I think yes. You do this by allowing access. The origin header is important to know.

[tim asks questions about CORS]

brad: you can't set multi-value header or use wild-cards.

brad: may have been due to fear of header-bloat. Agree this should probably have been allowed.  
... the browser doesn't know that the data you're asking for is *my* data on the server.

tim: folks are pushing for that data (that is mine) yet is stored on facebook to be granted. But right now, all CORS knows is that the server has the data and that it grants the permission to access.

brad: in terms of apps, you grant permission to the app and it has a clear boundary

wendy: we have more contexts for things to do than we have security indicators to represent.

dan: we wanted to minimize differences between installed apps and web apps.

brad: UAs aren't confident that they can present UI to the user to enable the user to make a confident choise.

tim: have you thought about using the same principals for native app installation and applying them to web apps.

brad: the confidence that folks have in an app store, involves trust in a gatekeeper that can kick off the bad folks. This doesn't exist in the web.

alex: all the technology exist in the browsers and web tech. We can do this today--the question is do we want to? We are moving into this territory with downloadable shells and server refresh.

[end of day 1]
