## TAG F2F - Berlin (Day 2)
### July 16 2015

### Contents

* Dev meetup roundup
* Meeting planning
* Spec reviews
* Fingerprinting
* Extensible Web

*Present*: Dan Appelquist, Yan Zhu, Tim Berners-Lee, Peter Linss, Alex Russell, Charles McCathieNevile, Hadley Beeman, David Baron, Mark Nottingham, Travis Leithead, Yves Lafon

*Special Guests*: Brad Hill, Charles McCathieNevile, Mike West, Nick Doty (for discussion on Fingerprinting)

*Scribes*: Charles McCathieNevile, Hadley Beeman, David Baron

*Chairs:* Dan Appelquist, Peter Linss



*Topic*: Thoughts on feedback from development meetup

dan: what stood out to me was the feedback on installable apps

yan: was thinking about signing the "packaging on the web" format  
... https://github.com/w3ctag/packaging-on-the-web/issues/21

mnot:  there will probably be a signature mechanism in HTTP soon - it would be nice to align with that…

alex: when I chatted with the developers afterward, it sounded like they really wanted key continuity; old installed app wanted to veto upgrade to new version. I think we can add something for Service Workers to fill this gap--will talk about it next week at SW f2f.



dan: we also heard a bit about the extensible web. We may need to do a better job articulating what that means for web developers.

mnot: We tried to explain it at length, and then we got a question about what the idea was. So maybe we didn't succeed in explaining it very well.

dka: also lots of feedback about developer outreach, engagement, etc.

*Topic*: Meeting Planning

DKA: Do we want to revisit date for next f2f? It's pretty soon. Then next official meeting is in January. We don't have anything official at TPAC. DO we want to push the september meeting back?

MNOT: We will be at Sapporo.

DKA: But there is a lot else going on, which is why we don't have a meeting at TPAC.

MNOT: Before or after TPAC?

DKA: WfM… What about the week before, in Tokyo 21-23 October?

TimBL: no can do

DKA: Let's do what we said we would.

MNOT: what about we plan a Halloween meeting?

DKA: Let's do what we said we would do.

PLinss: 15-17?

RESOLUTION: TAG will meet 14-16

MNOT: Still good for Jan 19-21 in Melbourne? Book well in advance.

RESOLUTION: Start organising the meeting.


*Topic*: Spec reviews - issues



*Subtopic*: WebRTC - issue 14

DKA: Rechartering, interim extension.

CMN: Charter review nearly over (until 19 July) https://www.w3.org/2002/09/wbs/33280/webrtcwg2015/

TimBL: Is there an issue?

DKA: So far only the charter. What about issue of privacy of IP addresses - should we tell them off about that?

[this is a well-known issue]

MNOT: There is no meaningful way to make RTC work without sharing the extra information. You can hide it from JS, but the peer needs it to make something work.

DKA: Sounds like New York Times are using the RTC API to expose information, rather than for actual communication.

mnot: [summarises the article at https://webrtchacks.com/dear-ny-times/]

DKA: The metaissue is that some party is using WebRTC to gain information, perhaps profile the user, fingerprint them, but NOT in the context of establishing a WebRTC session.  IN that case, it's harmful.

Alex: That's the open question.

David: I've seen this before. It's widespread.

dka: these are advertising networks, attempting to use this technology like many use canvas tricks.

mnot: Notable: we have a new portion of the web platform that is changing how we can fingerprint dramatically. If I'm in activist in a country that doesn't like me, and I use a VPN to protect myself, this would expose my local IP address, which could be dangerous.

timbl:  Even if inside a NAT?

mnot: yes.  All your local IP addresses, which could be used to trangulate me (if I"m on a cell phone)

timble: And reverse-engineer the network.

dka: Shall we defer this to the fingerprinting discussion tomorrow?  How did the WebRTC working group respond to this?

mnot: They see it's an issue, but we can't do webRTC without it.

travis: "document these, and move on."

Alex: Is this being used in a top document or in an iframe?  Could this be given on a user gesture, some evidence the user made this happen?

travis: expsoing to intermediate servers, and then exposing that to javascript (which is the scariest part.)  If we hide it from that layer, you'll still see it at protocol-level, but that may help.

mnot: Any mildly determined hacker could still get to it.

dka: Re rechartering — do we want to put this feedback to them? Feedback due July 19th.

mnot: It'd be interesting to look at Nick's fingerprinting advice doc for the Privacy IG through this lens.

alex: we should try to understand this better. They've already thought about privacy, and disagreed with us, which is within their rights.

mnot: Yes — but we should get something in before the charter closes.

chaals: if you're an AC rep, you can say something that way...

dka: re permissioning, for a WebRTC app to get to your camera and take your image, it needs your permission. How is it possible to get your ip address wihtout permission?

chaals: it happens in establishing the channel to make the request.

dka: Permission there then?

yan: Peope use it for things that don't require camera/microphone; just to chat.

David: Someone on the WebRTC team was quite opposed to having a permissions dialoge aorund that, but I forgot why.

mnot: p2p caching on the data channel... makes a privacy tradeoff that the user many not understand.

timbl: if you're going to a trusted site, then the p2p connectins could enhance your privacy

mnot: yes. but how should the user make that decision? What evidence/info do we give them, without annoying them?

...I see this NY Times article as a flag that WebRTC has got it drastically wrong. Maybe we can't have nice things til we fix that. 

...May be fixable, but we shouldn't expose the functionality until we get that sorted.

alex: why are they doing this?

mnot: looks liking fingerprinting.

david: if you have the external and internal IP for someone — that's a lot

timbl: and you can establish relationships between users in a local network

alex: but it's likely to be NATted.  
... I want to understand this better, exxactly whta it means.

mnot: Sure, but there's a difference between telling everyone to reduce fingerprinting surface area (which isn't effective) and encouraging a vulnerability

timbl: And for specific people in specific situations..

Yan: Threat model: if you're using TOR, even if you change your TOR circuit, this could expose your local IP.

timbl: maybe we need a tutorial on webRTC?

alex: Here you're making a p2p connection anyway. So where is the privacy concern?

timbl: Whether the software will allow the IP address to be extracted with no warning at all.

dka: I'ts that it can leak even without choosing to set up a connection.

mnot: It's p2p across the internet.  possibly with some intermediation for firewall traversal.

alex: NYtimes has a STUN server; trying to set up a connection.

mnot: people are using this for p2p caching, and chat. No effective permissions model for this.

...At one point, this was a concrete vulnerability in the TOR browser; they disabled RTC in response.

...For users interesteding in limiting fingerprinting surface area, we should help that.

alex: Okay, but we're talking about the burdens on the developers of TOR browser.  This may be about how they consider every new feature on the Web.

timbl: Is it not true that... if somene isn't through a VPN and not NATted, then they're not losing anything, right?

mnot: Right. The worry is that the ad networks are jumping on this so quickly.

timbl: Let's categorise scenarios, to understand the threat model.  

mnot: most people on IPv4 are NATted. So this is exposing something for most.

chaals: odds are, its 192.168.0.*. What worries me is that they can map out internal networks — privacy vulnerability for organisations.

travis: there was previously no other way to see someone's local IP address. I'm surprised it's so easy to read it in the clear right now. 

timbl: How does WebRTC use the local IP addess?

mnot: if you're behind a NAT, then it has to do a NAT traversal. Usually with STUN, which is esoteric and ugly.  Sometimes you do rendez-vous on a turn server.

timbl: Is it possible STUN could be changed so this would happen?

chaals: The only way to punch through a network is to have the end destination.

timbl: If someone is forwarding packages... you could give them a long one-off key

chaals: you could set up an intermediary — external or in your own network.  Man in the middle

timbl: does the stun server handle every packet?

mnot: stun is just for discovery.  
... Use stun to get external IP address, if you have a direct way, you can p2p. If not, you use a turn server to act as a relay  
... Mozilla team and I agreed you could hide this stuff from javascript, but if attacker sets up a peer, and has you connect to that peer, then that info has to be exposed to that peer.

yan: Eric Rescorla's webrtc privacy work? Sounds like they've set up forced used of a turn relay to allow a user to hide their IP.

mnot: Yes — but you need a trusted relay, which doesn't exist in the ecosystem right now.  
... I can take an action to talk to Fluffy and co about this.

timbl: it'd be interesting to know if, looking at all protocols, whehter the user could use a random alias for each connection.  If you have two outgoing connection that turn out to be the same connection, then all you need is the external IP and the port numbers.

...It's an old form of firewall traversal.

...Each protocol protably doesn't need to know the end IP address; it was just set up that way when everyone was happy to share their addresses.

mnot: There are so many different kinds of firewalls.

timbl: There are different ways of punching through firewalls.

hadley: ipv6?

...we're not saying that every user should be able to hide their ip address from the web? This is an IPv4 issue only.

timbl: This is an ipv4.5 issue where you're being identified by 2 IP addresses.

dka:  Back to — is there anything meaningful to say to the rechartering?

timbl: separate issues.

dka: Let's pick this up again when we talk about fingerprinting.  
... mnot will put this example in as a case study on fingerprinting, attend group next week in Prague on this and report back on a future telcon: 5 August.

timbl: but if this is more than just fingerprinting, then we should be clear on that.  VPN users etc.



[Break for coffee]



*Subtopic*: CSV on the Web issue. https://github.com/w3ctag/spec-reviews/issues/55

hadley: I think this is out of our hands.

Hadley: looking at David Booth's concerns on .well-known

mnot: we have a fundamental disagreement on whether or not this is an ongoing issue. We went through a process to look at it, discuss it with him and the editors, and we all seem satisfied with it.  He may be less pleased, but I'm not sure it can be helped.

dka: Closing then, especially since JeniT said her issues brought to the TAG were resolved on the telecons.



jumping back to

*Subtopic*: webrtc

Alex: Chrome users are showing ~80% of WebRTC connections are started behind asymmetric NATs.  Majority of users on IPv4.  Ipv6 connections are at 7%

mnot: seeing ~10% of ipv6.



*Subtopic*: issue 60 webpush

assigned to mnot, and assign to a telcon (19 Aug)



*Subtopic*: CSP 

https://github.com/w3ctag/spec-reviews/issues/42

alex: I sat in on WebAppSec WG, who are formalising CSP level 2, getting it to CR. Not yet time for a chat about the API.  

...CSP 2 is renamed version of CSP 1.1.

...They're making progress on capabilities.  We should pick this up in 3-6 months.

timbl: any philosophical differences between the versions?

alex: CSP1.1 included a proposal to add an API. I helped argue it down because the API didn't add much power.

...Weird timing issues.

...Has to do with the origin story of ay given document; it applies at the origin. CSP is actually turning off the runtime's ability to set things later.  Earliest: in the HTTP header.

timbl: or you could put it statically then, if you're a normal person

alex: That's why we put it there.  
... I asked: what API would you use to configure the javascript runtime, so it wan't be interefered by HTML parsing

[more explanations on how CSP works]

travis: we talked aobut hte principle of tranquility yesterday... would an API violate the principle, allowing things to be more mutable at runtime?

alex: CSP vocab doesn't let you easily reason re whether something is stronger or weaker.

timbl: The principle is that the policy should be stronger.

travis: So... leave it assigned to Alex and move on.

DKA: I'll put it on a milestone for the next F2F



*Subtopic*: scrolling element

https://github.com/w3ctag/spec-reviews/issues/51

DKA: we've had a lot of engagement on this.  We should resolve it. 

Alex: there's a resolution in the thread, which just needs to be written up. Which I will do today.



*Subtopic*: subresource integrity

https://github.com/w3ctag/spec-reviews/issues/43

Yan: I've looked at it; it's fine

mnot: I've reviewed it too. 

dka: So we can close it.



*Subtopic*: Request for feedback on a Presentation API

https://lists.w3.org/Archives/Public/www-tag/2015Jul/0001.html

Dka: [opens an issue.  Travis volunteers to take it; sets for discussion on 29 July]    



*Subtopic*: issue 56, Frame timing API

https://github.com/w3ctag/spec-reviews/issues

David: [offers to take it; sets for discussion on 5 August]

alex: my comment: where is the example code?

travis: this ties into issue 18, navigation timing



*Subtopic*: issue 18, navigation timing

https://github.com/w3ctag/spec-reviews/issues/18

travis: both this and frame timing are by the same group

alex: I talked to the web performance WG at the last TPAC... We owe them feedback.  Though the group isn't asking; Domenic is.  We can invite them to a call and offer?  
... And they don't have a serialiser. Issue: https://github.com/w3c/navigation-timing/issues/23

dka: [assigns to 5 August, to tie in with Frame Timing API discussion.  Will send a mail to invite Ilya.]



*Subtopic*: Issue 24, navigation error logging

https://github.com/w3ctag/spec-reviews/issues/24

travis: This looks closed?

alex: Yes, we can close it. We can interact with them in their open bug, if needed.

travis: to be discussed on the 5th, with Frame Timing API.



*Subtopic*:  Issue 41, CSS variables

https://github.com/w3ctag/spec-reviews/issues/41

plinss: still open. 

travis: I've put some time into it and I think it's fine. We got some feedback on syntax, but... bikeshedding isn't our job.

alex: What were the design alternatives available for hte syntax? Did you end up with hte shortest version?

plinss: We went through a few iterations

david: there was var- .  -- was the shortest thing that wasn't in an occupied space.  
... I think Tab had other ideas on what to use $ for.  it's possible there would also be conflicts with pre-processing tools.

plinss: there were a few variations of using functional notation.

travis: some good exploits in there...

alex: I think we can close it.  We can thank them for responding to their devs' feedback.



*Subtopic*: semantic equivelence of protocols

hadley: We need to open an issue on whether http: is semantically equivalent to http:// (in data and the Semantic Web)

[initial debates ensue]

DKA: we need a discussion document.  Hadley — outline it, to present the issue to us.  
... the TAG can open that discussion and perhaps lead it? bring in others, like Jeni?  Structured disucssion in Boston/

Hadley: I'd like that. My worrry is that the communities aren't very interlinked, so we'd be in a good place to lead that. 

timbL: ge tpeople who d othe libraries; the parsers and triple strings.  capital HTTP etc.  They already do some munging.  Tying up to HSTS.   
... migh also be connection to make it easier for scripts to pick up HSTS header...?  
... There's a wider issue in running through browsers; it's hard to track follow redirects. Different ones have different semantics;

mnot: I think there's a flag in fetch to change that behaviour

alex: Active discussion. Surfacing that something is a redirect is useful, but expsoing all info re directs could use to, for example, exposing tokens that are currently hidden. Bad for security. So some limited info may be availble via fetch but...

timbl:  cookie exchanges?

mnot: you're crossing a trust boundary.

timbl: Redirects can tell the system that those URLs are equivalent. For example, if you change from HTTP to HTTPS, you redirect. People then fix their database.

alex: We can get the eventual URL, but you won't know how many.

timbl: that's not acceptable.

alex; Okay.    
... For same origin content, that's possible. same trust model. Across entities (incl HTTP to HTTPS), it's not.  HSTS is there.

Timbl: That kind of redirect is very common.  Slowly, I'll replace all the HTTP urls with HTTPS urls, in everywhere I store it.

travis: Clients want that information?

timbl: example: list of paychecks, come out every week.  Every month the list is longer. One day it gets redirected.  If you want to go back to the previous ones, the data structure isn't the same.  The program has to be explicitly told they've moved. You don't want two payslips form the past (HTTP and HTTPS), so we need to know they're the same.  The client side identifies them by the URL.  
... Or when you bookmark things.This is not done by the application; its done by the code libraries underneath.  They look at a URL as being an identifier.  When you build those libraries underneath, you don't know if everything will have been upgraded to HTTPS...

DKA: So... we need to understand some of the convergence use cases, not just semweb use cases. 

...From JeniT, it'd be useful to know where open data companies are impacted.  

...And Jonathan Rees, Creative Commons — is a license relevant to just one URI? 

...Where does this impact large user communities?

Hadley: Wikidata... Freebase...

Timbl: The TAG could say here

alex: What extent do semweb have latency issues like browsers do? It's difficult to try both.

timbl: You load the resource, and HTTP patch.

mnot: is the client a browser? Or code?

timbl: both, but normally i nthe browser, as a webapp.

mnot: wondering if we can check to see if HSTS is in place, define a new API and polyfill it.

timbl: you'd have to operate the RDF libraries; give them a new hook because they don't talk much to the HTTP system. Well, they do fetches, infer stuff from headers.

mnot: We need owl:sameOriginAs.  Check by probing for HSTS. If you probe hte HTTP site and it redirects to HTTPS; HSTS is an assertion that it will all redirect. You have access to the HSTS from XHR.

timbl: the HTTP range-14 issue was this is an object, which is a document.  That's what HTTP is saying.  Then other people said I don't like the hash character; I want to use something that looks like a document name. Taht brokethe assumptions that the code was making from HTTP.  That was very boring. It's simillar — the code will pick up link headers and remember them. Relationships: this is an earlier version of that, etc.  The main thing is the links.  Adding HSTS is a big change; saying RDF will look at HTTP headers is a massive change.

mnot: If your'e going to reason about the Web, you do need to take headers into account. Mediatypes, cache times, etc. Rich metadata.

timbl: For these guys, a name is a name.

mnot: if the semantic web is based on http, it buys into that system

timbl: they're different worlds.

dka: we need more of the use cases, to talk about this.

mnot: HSTS is the first thing we need to examine in this discussion.  Is there anything in linked data that prevents considering HSTS?



*Subtopic*: JSON form submission

https://github.com/w3ctag/spec-reviews/issues/40

travis: we can encourage robin to drop this into the new Incubation Community Group.

dka: [closes issue]





*Subtopic*: Web NFC API

https://github.com/w3ctag/spec-reviews/issues/22

[brief discussion about how we work with community groups]

dka: Anyone considering shipping an NFC API in their browser soon? I know one is part of FirefoxOS, but there was some reluctance to take it through to a standard. I don't understand that; it's growing right now and there isn't a standard way to interact with it in a web enviromennt.  Apple Pay, Google Pay, etc.  Will encourage native apps over web apps.

travis: it's a hardware disccovery problem

alex: the interesting part of the spec is registration. This API looks like it will do a reasonable job of letting you talk to an NFC endpoint, but it's unclear how it deals with hte passive, you're-in-the-environment-as-a-participant.

dka: The physical web is low energy bluetooth, but a similar use case.

travis: ??? had a similar device discovery API

alex: for user-initiated actions, this looks like a fine API. Question: what other use cases should we accommodate? Can this evolve to meet them?

dka: Worth our time commenting on those points?

alex: I'd also like to give them credit for designing an API well.  Very modern.

dka: This popped out of the SysApps WG, so may have not been expected to be on the Web. Should we bring together other people as well? Microsoft, Google, Samsung etc.

alex: could we accellerate it, if we thought it was valuable?  

travis: I'm certain we have APIs for NCF in our lower level architectural model. 

Alex: the NFC tags are outside the origin model.  Good or bad?

dka: I'll take an action to contact anssi to propose a focused discussion on this (on a call or another venue).  Offer help.  Will feedback briefly on telecon 29 July.



*Subtopic*: File URI scheme

https://github.com/w3ctag/spec-reviews/issues/59

Yan: I can take that.

Travis: I asked folks at Microsoft; thought this reflected what browsers do. Didn't answer how we handle origins in relations to the file scheme; may be OS-specific. We'd like it to be specific across browsers running on Windows.

David: We have additional security checks beyond the origin checks. Can this URL cause a load of that URL? If the second is a file URL, the answer is no. 

mnot: Sure. XHR to file should not work.

dka: [sets for discussion at telcon 29 July]



*Subtopic*: fingerprinting issue 38

mnot: we can just change the milestone to this meeting.



*Subtopic*: media capture and streams; issue 57

 doc: http://www.w3.org/TR/mediacapture-streams/

dka: last call ends may 15.  Does somebody want to contact dom?  Nobody currently assigned, no milestone assigned, no conversation.  Not clear if request still valid.

travis: specifically looking for feedback on IANA-registry based constraint system, use of promises (which looks fine to me), and handling of persistent permissions

alex: why is this on a member-confidential list?

alex: can we take 10 minutes and look at the spec?

travis: partial to the API; was involved in design

alex: methods on media stream, like removeTrack and addTrack -- do they have synchronous behavior on the other side?

travis: of a PeerConnnection?

alex: I assume you can create a MediaStream that doesn't have PeerConnection backing

travis: they queue a task to do stop or start -- removing a track...

travis: The tracks are a core piece of the design; adding to a media stream is just about synchronizing them together

alex: the web audio api has concepts of processing rate.  There's the hardware clock about audio processing, and then the "offline Web Audio Context" which is batch processing.  Is there anything like that here?

travis: These are always hardware-bound processing.  There's a separate document talking about recording of these streams.  In terms of recording there's a batching model applied:  record and give a timesliced interval, blob for that, another timeslice.  As far as this is concerned content is opaque.

alex: so say I have a media player and want to play at 0.5x

travis: I don't think you can do that b/c you're just streaming through what the video is doing.  No concept of fast-forward.

alex: If I wanted to do that I'd have to poll faster on the other side, consumer, to get frames delivered more quickly.

travis: you're talking about live content; have to record it first

alex: why live?

travis: connection to camera or microphone

alex: can't be used outside of that?

travis: it's the interface you get from a PeerConnection.  In a realtime application it's the endpoint to other hardware streaming over the web.  But you can't connect it to HTML5 audio or video tag as a source.

alex: So you'd have to push content faster to enable that.

travis: The real world would have to speed up.

alex: There's a clone method on MediaStream.  Do streams have similar clone semantics to streams api, readable stream api, where read operations are destructive unless you clone and ??? the buffers.

travis: Don't know.

travis: Trying to think what is the point of cloning, except as convenience.  Fork off to redirect to diferent places?  The MediaStream is the thing you attach to sink.  Not sure if there's a restriction of attaching stream to multiple sinks.

alex: One thing when we were looking at ??? was to make sure we didn't have implicit buffering for streams that happen to gain another consumer.  Default semantic is destructive reads.  Need to clone. This has the behavior of implicitly creating buffering.

travis: So you need to clone to have non-destructive read.

alex: This is a weird semantic difference.

travis: Why is read destructive?

alex: Not destructive, just consumes off buffer, deprivig other readers from getting that, at the byte level.  Don't want buffer to continue to bloat.

travis: In media stream bottle, no buffer on the creation side.  As soon as you hook up the source and the sink it's up to the underlying infrastructure to route frames to destinations.  Might buffer on the sink side , ut nothing accumulating on the source side.

alex: ... I'd at least like to see discussion betwen you and dom and editor; might clarify where things go in the future.  When we talked to Harald Alvestrand a year or two ago about WebRTC, he made convincing case that streams model they have isn't a series of byte streams, different sort of object.  Core semantic of fork/tee/clone in terms of what consumers see is an important thing.

alex: How do media stream tracks play with getting bytes, e.g., tofeed to processing web audio.

travis: I think Web Audio has attachment point.

travis: Recalling code review, forget if it was in web audio or this spec... script processor.

alex: script processor ... media stream sources.  Which is a hack.

alex: Media stream sources -- things that hand you stuff.

mnot: The IANA part looks fine.  I noticed they introduced device ID, which is effectively another cookie mechanism; they talk about the considerations for that.  Say that clear it too when clearing cookies.  Some people think we shouldn't let these proliferate, but we haven't addopted Nick's document.

travis: In earlier drafts, tried to make pseudo-random identifier.  Wanted to tie back to domain.  If origin A cached deviced ID, and visit or

[minute taker got disconnected briefly]

mnot: When I chat with them next week I could 

travis: ... unique to the application

mnot: I'd like to see a little more text around it.

travis: authorization part; I think when we implemented we said not to persist authorization

mnot: per-origin persistent identifier device id, but in text above it didn't make it clear that it was per-origin

mnot: looks like some information lost in edits

mnot: This will be relevant when we talk to Nick about his document; he recommends no new cookie-like methansims.  You should treat new cookie-like mechanisms as if they're cookies.

alex: If they're isomorphic to cookies, so what?

mnot: Yeah, so long as state gets cleared when cookies are cleared.  Though we shouldn't have new mechanisms that are just like cookies willy-nilly, but if there are good use cases for them.  As long as it doesn't expand the mental model of the user when dealing with the Web, so if clearing cookies clears those too, we're good.

mnot: But maybe Nick can convince us otherwise tomorrow.

travis: assignee and milestone for this issue?

travis: assign whole issue to me; let's look at it end of August.  26th.

travis: That will give me time to read up on stream stuff.



[discussion of trees in Melbourne having email addresses, not URLs]

[... city of Litchfield used URIs ... ]

Hadley: in Melbourne, new government CTO came there from UK; could arrange something when we're in Melbourne



dka: Yves contacted dom; do we have questions for him

travis: only concrete feedback so far was about device id not being clear; rest of feedback needs to become more concrete, so probably not worth talking now



mnot: Did we want to talk about March face-to-face?

dka: Were talking about South America.  I think we should rethink and meet in London.

mnot: Could we shift 2 weeks later?  Week after AC meeting (20-22 march) in Cambridge, MA.

dka: We were looking at 29-31 March.  Which is just before IETF95 in Buenos Aires.



alex: Travis, what's relationship between codecs and media streams?  Seems that media streams implicitly deal in time which means it's decoded content.  Or synchronized encoded frame notion.

travis: You get a video track and that video track will have its own encoding format, and the media stream lets you bundle potentially many different tracks, maybe with different encoding schemes, together.

travis: The tracks are the core thing.

alex: Which spec defines tracks?

travis: Same spec.  Media stream track.



dka: Paris or London.  Do we want to change dates?

TimBL: There's a Web conference in Montreal.  April.

mnot: Last time we met we talked about IETF being in South America, and last time people seemed excited about going to South America.

dka: We have Japan and Melbourne...

People seem happy with London.  March 29-31.

TimBL: Right after Easter.  Will be a lot of travel there.

dka: Would week of April 11 work for people instead?  (In London.)

mnot: Then I wouldn't go to the AC meeting, but not the end of the world.

Yves: Holidays.

dka: Suggest keeping March 29-31.



dka: Yan, saw something come through from you on Encryption thing.  Want to talk about it?

Yan: Just want to know if people are happy with where it is.

mnot: Just sent some email.  And can probably drop table of contents.



dka: I'm suggesting maybe we could all take a look at the TAG supports strong encryption thing, and if consensus around the table, actually publish.

TimBL: Maybe ???

mnot: I think this is good and we should publish it; feedback I gave was editorial.

dka: Should we say instead of "millions of businesses" (sounds a bit strange).

mnot: talked about this in securing the web

hadley: "Millions of services" instead?

dka: services a little abstract; important to root it in things that ...

alex: do we want to enumerate them at all?

alex, dka: organizations

TimBL: organizations more inclusive

various: "businesses and other organizations"

hadley: it talks about privacy violations of network operators; 

mnot: change [VERIZON] reference tag to something else, [PERMACOOKIE]

hadley: any actual criminal behavior?

mnot: well-advertized attacks on authentication tokes, FireSheep.  Could refer to FireSheep, one of early drivers of encyrption before Snowden.

Yan: wouldn't want to call it an attack because it was a demonstration..

mnot: "Likewise, attacks on credentials and other ... information, such as demonstrated by FireSheep, are prevented by ..."

Yan: I like last sentence; could change it to "any hypothetical benefits" to make it clear that we're not referring to concrete ones

chaals: mandate refers to something that's not described

dka: yes, should be more concrete

Yan: "Such capabilities"

dka: Can you publish this into w3.org space?

[ Yan pushes changes to github ]

chaals: Third paragraph belongs as third sentence of second paragraph.

mnot: Can I suggest taking first paragraph of section 1 and make it the abstract?

dbaron: Shouldn't that be in the body too?

various: no, it's fine

hadley: Did carriers get in trouble for things like permacookie.

various: Just bad PR; nothing formal.

mnot: Not much relevant law in US/Aus; different in European context.

chaals: Doesn't seem to hang together.

chaals: Abstract says what it means to say; first two paragraphs jump around.

chaals: first paragraph says a bunch of things

dka: I think it works; does what we want it to do.

...

Yan: 2 sentences at end of first graf would fit better at start of second paragraph.

mnot: and make reference [HTTPS] be [SECURING-WEB]

...

mnot: I think Keys under the Doormat is pretty authoritative, but some people may not realize how authoritative it is, so we're lending our name to it.

[discussion of reordering of sentences]

hadley: add "to the Web" after "known risks"?

dka: these risks to the Web are in fact risks to society

various: no change

[ discussion of whether the finding link to securing the web is a link to the github URL or the w3.org published finding URL ]

[ discussion of finding being published at a non-https URL ]

[ discussion of https on www.w3.org ]

dka: Can we publish the document so it's accessible on a w3c URI; people can refer to it on a github URI or a w3c URI.  But for outreach to policy people, should send around the w3.org URI.  I know it's ironic that it's http.

Yves: I will update the link to securing-the-web finding to the w3.org version as part of publishing.

Resolution: publish End-to-end encryption and the Web as a TAG finding  
... https://www.w3.org/2001/tag/doc/encryption-finding/

[ going through checking of publication ]

[ break ]

*Topic*: fingerprinting

mnot: I posted this to IRC yesterday.  After our discussions of fingerprinting and talking to Nick.  Wrote this on the airplane here.  https://etherpad.w3ctag.org/p/fingerprint  Floated it past Nick and Wendy; they were both supportive.  High-level finding about how we  feel about fingerprinting on the Web.  What I wanted to do now was let people have a quick read; let people think about whether it's worth starting work on in a repo and start a draft of a finding.

alex: finding seems premature; should discuss ...

mnot: that's what we did on the phone a month ago with Nick.  Voice of document is interesting; targeted at Web users, not sure if tthat's right.

mnot: and Brad had a look as well and put in some extra info.

mnot: Fingerprinting is a societal problem better targeted by regulators or legislators than by us.  This is to help explain it to them.

mnot: we have a session tomorrow on this, but wanted to get a sense of the room as to whether this is something we'd consider adopting.  And we should get a repo and a url if we think it is.

alex: There's a qusetion here about the findings, in the draft findings list.  It says actively harmful to the Web.  Asterisks that would need to be applied; more technical background than we should pour into this.  There's reputational harm -- when finguerprinting escapes user control.  We should distinguish between cookie-lifetime, and supercookies.  We could introduce language talking about cookies and user control, and persistent tracking.

alex: maybe we should have text defining fingerprinting as not being what cookies/localstorage/indexeddb do.

mnot: (agreement)

alex: And then great to link to everookie, panopticlick.  Ther's more theoretical grounding, like covert channels.  Theoretical ability to constrain.

mnot: Maybe we don't call this fingerprinting, but maybe supercookie or evercookie.

alex: Worth doing, maybe motherhood and apple pie, to say supercookies considered harmful.

hadley: Do we have a thesis?  That this is violating contract of Web?  Or general description so there's a common set of vocabulary around the topic? Or...?

mnot: Purpose is to document that it's considered harmful to the Web, to guide W3C.  In many WGs fingerprinting comes up and there's disagreement about policies about fingerprinting surface area.

hadley: stake in the ground for internal decisions?

mnot: Yes, and also externally to guide policymakers.

mnot: Maybe "Fingerprinting and the Web" isn't the best title.

travis: I was a little confused.  You say at the beginning that cookies are what sites use to correlate what you do.

mnot: That's the on-reservation mechanism.

travis: Then you talk about how user can control that.  Then more things, like local storage.

mnot: And that's still cool.

travis: Then sites that attempt to use fingerprinting... needs to be clear how that's different from cookies.

mnot: Yes, probably need better terminology here.

mnot: Didn't want to edit this now, but sounds like there's interest but need for scope adjustment.

mnot: I'll hack on this this afternoon/tonight and we can have better discussion tomorrow.

mnot: Challenge is finding good terminology.

Yan: I can send you a paper with good taxonomy - Mayer (2012):  supercookies, active fingerprinting, passive fingerprinting.  https://jonathanmayer.org/papers_data/trackingsurvey12.pdf

travis: tone and detail so far are good

mnot: I don't want to go away with "cookies bad" here.

TimBL: Cookies are useful; help give a real URL for an object without having to hide lots of crap in it.

alex: Also should emphasize role of policymakers in this.

mnot: Yes, without policy here it's the wild west.

mnot: Maybe it's just "Supercookies, fingerprinting, and tracking on the Web"

mnot: Abstract probably needs to change as a result.

mnot: Emphasizing duality between recognized and unrecognized mechanisms for tracking is the heart of the matter.



*Topic*: Extensible Web

alex: report card?

dka: More importantly, had blog post from Mat Marquis, https://bocoup.com/weblog/extensible-web-manifesto/  Might be useful for us all to read what Mat had to say.

dka: and also feedback from yesterday's dev meetup

dka: And think about tools we have to further extensible web, and what should we be doing more to talk about success stories.  Should we update the report card?  Do blog post?  Another TAG finding?

dka: What really triggered my worry about this was Mat's blog post, and the stuff that came out of yesterday's dev meetup reinforced my view that e need to do something here to keep momentum going.

[group reads]

alex: feel the need to write a blog post in response.  Think he's spot-on.

dka: some of the same topics from the dev meetup yesterday

travis: Some others, though -- library being so good that it prevents standardization.  To what degree do you have to write code at same quality level as browsers?

chaals: people asked about that yesterday -- how do you decide what to standardize and what not?

travis: Implementors may not be 100% aligned with the most needed thing being standardized at the moment.

alex: Standardization doesn't happen without solid (if not complete) vendor input.

chaals: There's stuff that could be valuably standardized that doesn't get standardized, because implementors are doing other stuff.

travis: Part of this document seemed to me as a question to those who write javascript libraries and polyfills - to what degree do weneed to write professional quality javascript that's not going to be throwaway stuff; don't know if your'e going to be the next popular thing that's picked up by a million users.  Same problem an implementor faces but on a smaller scale.

dka: I was trying to read this from the perspective of what the TAG can do.  So I wasn't considering that issue as much.  I was thinking more of the ...

chaals: The TAG could say "we can't solve this problem"

dka: There are a lot of problem the TAG can't solve; we don't need to point them all out.

TimBL: Issue 42 on the old tracker.

dka: Are there things we can do to address issues Mat is raising?  Or 

hadley: How much influence do we have over the w3c community socially?  He starts out in the beginning that this feels like a crappy part-time job with no pay.

chaals: it is

hadley: It could be a fun part-time job with no pay.  Do we or the AB have the power to encourage the rest of the community to welcome newcomers and not draw clear boundaries as us as a group.

chaals: ...

hadley: can't solve employment problem

chaals: whole w3c community -- AB has responsibility in saying how organization should behave -- TAG can say should give input a sympathetic hearing, then you risk developing in a technical echo-chamber and building second-rate stuff that's only good in your echo-chamber.

travis: So off-the-bat he cites a number of roadblocks: listservs, timezones (that's reality), spending nights and weekends on specs (think that's talking about tooling about writing specs)

chaals: actually the tortured pseudo-English prose

travis: And fighting with professional Web standards reps (that's us)

dka: This is all colored by Mat's experience with RICG, and their fighting with HTML.

chaals: And not unrepresentative of lots of cases.

dka: I don't want to build Mat up too much -- but particularly dogged in his determination.  And others like Yoav helped.  And we have what's now seen as a success; we talk about it as future of standardization.  But many other great ideas may have never got that far.

dka: In some ways that might be good because you do need a weeding process; can't take everybody's ideas.  But the extensible Web idea, coming down to the end, is that we want that to enable actually more small-scale, new, stuff, and that stufff is embraced organically, and eventually filters through to widespread use and is not blocked by somebody just saying "no, that's a bad idea", but rather we enable the people who think it's a good idea to get it out there and into the hands of more people, and can prove itself without having oligarcchs saying no.

alex: Or saying "I don't understand your use case", my favorite.

chaals: ???

dka: I was talking last night about the whole saga of widgets.  A lot of the same concepts in manifests were in widgets.  But I had so many conversations with people then saying users weren't asking for it, doesn't make sense.  It wasn't based on reason; just dislike.

chaals: One of things is explaining limitations of extensible Web.  The only thing it can do is to build the thing that you're trying to convince us is useful.  You've got to go out and convince the world that it's useful (which doesn't necessarily say whether it's good or not).

alex: ... 

chaals: It allows people to build their thing and play around with it and get people excited.  Not just shouting from one ivory tower to another.  But just provides building blocks you can use.  If you have a brilliant idea and don't tell anyone, the extensible Web won't solve that problem for you.

alex: What the extensible Web can do over time is to reduce the expectation that people who have a seat at the standards process will invent the answer for you.

travis: Human nature of people looking to authority to solve problems for them.

alex: learned helplessness.  It's a set of expectations we can affect, not an unchangeable feature.

chaals: Whether it's a default course of action or not, providing tools and examples lets people with ideas ...

travis: How do you provide motivation?

chaals: You don't.

chaals: It used to be that you had to argue with people at the standards table.  With extensible Web they can show how to solve the problem . If they can communicate, they may discover that other people with the same problem want the same sort of solution.

chaals: If you see the same sort of tool turn up many times independently, that's a fair idea it's a problem worth solving.  If it has 2 users, it might not be useful, or might be a communication failure, and maybe somebody will come along and build it again 4 years later.

alex: I'd like to make standards boring; way too much drama.

chaalss: developing standards should be boring.  The actual standards should be well-written and engaging.

travis: What's wrong that makes him say he wants answers

mnot: The EWM is not yet evenly distributed.

TimBL: ask him what he means by that.  "I don't want a vision, I want a concept"?

hadley: the endgame

...

travis: I get confused because sometimes the EWM is a design philosophy or contributing and making it easier to get your ideas to get your ideas into standardization; sometimes it a set of tech to make that happen.

chaals: the manifesto says we should produce the tech that enables that.  We should produce the tools that let people play on their own.

chaals: If we put it into practice, the outcome is a pile of tools people can play with.  If the thinking behind the manefsto is sound, these tools can be used, and emerging from the Web we'll see things people need that we never bothered putting in.

travis: Not new by any stretch.  AJAX, rounded corners.

chaals: How many dollars did the industry spend paying designers to shade pixels in quarter circles.

?: ... doesn't have a posse.

dka: aggressive advocacy

chaals: So what else can you do that's useful?  Say that, and repeat it when you see people making rand glorified things without figuring out what's underneath.

dka: Useful to keep updating extensible web report card and keeping pressure going from that perspective. https://extensiblewebreportcard.org/

[degrades into dns jokes]

dka: I don't even think this is up-to-date.

dka: We didn't spend time in SF updating it.  We had spent time at the last 2 TAG meetings updating it.

mnot: How many people actually look at it?

plinss: I can look.

mnot: In terms of return on investment.

alex: It's our externalized internal thinking.

dka: If it's just about moving things around in these categories or adding/removing to/from list,  then that might be something worth spending half an hour on.

chaals: Would be interesting to go out and find the things that people did with the bits of the extensible Web that play well with other children.  Show us the examples of how having put this into practice in some areas, we got benefits out of it.

dka: That's a fourth category: graduated with honors.

dka: Does it make sense to spend time on the expensible Web report card?  Do we have enough people interested in coediting document right now, or not do that?  Nobody else seems as interested in it as I am.

plinss: Site is getting about a dozen visitors per day.

dka: We could move on to the next thing.  But before we do that we should take a decision on this.  We have document out there that's out-of-date.  IT's a report card that's about things that are in a different state.  Reputational risk.

alex: Can we do it tomorrow.

dka: ok



[ 5 minute break ]



[ 25 minutes later... ]



Present+: Nick Doty (via Skype)



mnot: So, Nick, you read the document I sent?

mnot: We discussed it today.  I think the general feeling is that it's interesting to go in this direction.  But want to refocus slightly.   Think the document is really about the delineation between recognized mechanisms for tracking and are part of platform with appropriate controls (cookies, etc.), and the ones that aren't.  Trying to draw a bright line so we can make appropriate technical decisions, and can talk to legislators and regulators etc.

Nick: Guidance about capabilities rather than specific technologies.

mnot: I'm going to revise that and we'll talk about it again tomorrow.  The follow-on activity is to work with you on your document, which is much more specific advice for specification authors.

mnot: A few things have come up in the meeting already, e.g., about WebRTC and fingerprinting.  What's your feeling about that document now?  Stil privacy interest group document.

Nick: In terms of my fingerprinting guidance document.  Haven't yet incoporated comments from last time we talked.  Great comments, just haven't gotten to it.  In terms of location, opportunity for collaboration between privacy interest group and TAG; don't really care about the name at the top.

Nick: Got a response from WebRTC people in response to a review, asking whose document it was and whether it was consensus.

mnot: My personal feeling is that with some work and luck we might be able to approve finding at this meeting or shortly thereafter; that might set higher level direction, and then we can focus on your document.   Does that make sense?

Nick: Sounds great. :)

mnot: I'll try to make edits tonight or tomorrow morning; appreciate your feedback on them.

mnot: Will edit offline and paste back into etherpad for more group edtiing.

Nick: sounded from the minutes like maybe there was some ongoing debate about how much technical background we'd need to make these claims.

mnot: Alex was finding material, and have some from Brad (Hill) as well, to bolster that.  Great if you have recommendations.

[agenda timing logistics]

mnot: ... maybe even discuss by email

[ pick up 9am CEST / midnight PDT ]



[adjourned]



