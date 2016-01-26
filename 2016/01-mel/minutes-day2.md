## Thursday

- Mike West update: 9:00 - 10:00  
 - CORS...
 - Tim's questions about certain kinds of fetches...  (slightlylate to find URL)
 - CSP changes? breaking? shared vocabulary with frame options in the future?
 - status of secure contexts document \url{https://github.com/w3ctag/spec-reviews/issues/75}
 - unblocking https transitions \url{https://github.com/w3ctag/spec-reviews/issues/74}

- 10:00 - 10:30 

 - Debrief from the Extensible Web Summit
 - New name?

- 10:30 - 12:00 Spec reviews

- lunch 12:00 - 13:00

- 13:00 - 14:00 Fido (+ Keygen bonus discussion)

- 14:00 - 15:00  Web Payments Discussion
 - [EME Secure Release](https://github.com/w3ctag/spec-reviews/issues/73)

- 15:00 - 15:15 Break

- 15:15 - 15:45
  - Brainstorm IA for the TAG's web site(s)
  - https://github.com/w3ctag/spec-reviews/issues/53

- 15:45 - 17:00 Spec Reviews
  - Stuff we haven't fit in anywhere else

## Friday

- 9:00 - 9:15 Schedule next meetings
- 9:15 - 11:15
 - Spec reviews

- 11:45 - 12:30
  -What role should TAG take in charter development
  -Role of TAG in guiding expermental features in browsers?

- lunch 12:30 - 13:30

- 13:30 - 14:30 Accessibliity with Chaals

- 14:30 - 16:00

  - Web components update
  - IETF update, Captive portals
  - Houdini Update
  - EME and the non-sue covenant... (Cory discussion) -Yves gave an update on that and the proposed extension to the HTML Media Extensions group

  - Policy interest group

- 16:00 - 17:00 

  - EWS Blog Post
  - Stuff we haven't fit in anywhere else

==========================================================================
= Notes
=================

### Present: plinss, yves, dbaron, mnot, slightlyoff (aka: "alex"), bradhill, mkwst, travis  
via Teleconference: Andrew, Dan (for morning session)  
Regrets: hadley  
  
TOPIC: special guest, Mike West \& Brad Hill  
  
bhill: status is that it has been stable for years, there's a small correction in flight, but new work is happening in the Fetch spec today  
mnot: I had a conversation with Anne about an origin-wide statement so you don't need preflights; this is important because Options requests aren't cacheable. These requests tend to hit backends. He's more sympathetic but there isn't any sort of movement yet.  
bhill: didn't have agenda in advance, but webappsec has hosted conversations on tihs.  
mnot: haven't seen major activity on this recently...is now a good time to start that discussion?  
(https://lists.w3.org/Archives/Public/public-webappsec/2015Feb/0309.html maybe?)  
bhill: we're looking at other preflight options for lots of other kinds of requests (e.g. intranet/extranet)  
mkwst: I could imagine something like a manifest file and/or lots of other ways to set up this sort of policy. There are a number of features we want to build that create a policy for an origin (CSP pinning, HSTS, etc.) and some might make sense to set on an origin basis. If we could come up with a reasonable mechansim than perhaps we should explore it.  
alex: TimBL had an issue he raised where something wasn't working for him, and the request wouldn't use CORS even though the server would have done CORS.  Inconsistencies.  Each new resource type needs to set policy.  with-credentials flag in fetch and XHR; doesn't have same behaviors in all cases.  Can you explain status of that to catch us up?  
mkwst: CORS allows something to have access from another origin. CORS lets holders of information expand the same-origin policy such that other origins can have access to that data. We're relatively leanient with regards to "simple requests"; i.e. GET, OPTIONS, TRACE (others?) and requests that have "simple headers". The idea is that if you don't handle these correctly, your internet card is revoked ;-)  
[interrupt]
mkwst: my default a credential request is not considered a simple request. These are treated as dangerous requests. Non-credential requests are considered "safe", and we all them to be public with access-control-allow-origin to allow things to work x-origin. Does that answer the question?  
alex: sort of, the question then is, does sending credentials create a preflight?  
mkwst: yes; CORS creates a protocol for mediating this policy. My understanding is that including credentials doesn't always create a preflight.  
bhill: an `<img src="...">` creates a simple request with credentials. If you expect the result might be a "*" for access-control-allow-origin, you need to explicitly set cross-origin mode to "anonymous". You need to know what the resource will proabably have set.  
alex: this is the root of timbl's problem; you need to know a lot about the URL, not just the URL.  
bhill: You could make a manual preflight by doing a second request.  ...  
alex: so is it possible to make a GET, e.g., with a single set of flags to any URL, and ensure that it will always work in some way?  
bhill: haven't worked through it, but the answer is probably "no"; you can't combine "*" for ACAO and Credentials.  
mnot: oh, interesting.  
[discussion]  
bhill: server can set the Access-Control-Allow-Origin header in the response to the value of the Origin header in the request; this avoids * and will always work.  
bhill: [history lesson about abarth and annevk and parsing vs. simple string matching]  
bhill: if you go through redirects, the Origin header will end up null  
bhill: if I have a public data source and move somethign, or move it to HTTPS, you can never CORS it using the original links, which sucks  
yves: and it's seen by the library as a network error  
bhill: it's an '06-'08 design choice, it's pretty lame  
mnot: has there been any discussion about how to get to a CORS2? Seems like it'd be messy?  
mkwst: yeah, slow and painful. Something we could do if we thought it was important and worth doing.  
alex: I'm very uncomfortable about the developer ergonomics of this; that you can't "just make a request" is \_bad\_  
travis: can't we just have the user agent automatically start a new request at the redirected URL? Does that violate the user-contract (e.g., I asked for a resource at X, but the resource was actually recieved from Y.)  
bhill: yeah, the developer ergonomics and the redirect issues are painful  
dka: is there anythign we can do to help?  
mnot: a lot of this is tied up in Fetch  
[discussion about interest and TAG ability to jumpstart the discussion]  
bhill: I've talked to developers and it's sad-making; you can't just take a URL and get open-data from it, you need to know a lot more about the URL a-priori. It's frustrating.  
dka: would it be useful for the TAG to have a document describing the problems  
alex: yes!  
alex: is there a set of testcases that would help us navigate what does/doesn't work in browsers today?  And is there an implementation gap \& minefields about compatibility, or is it stable?  
bhill: relatively stable.  There was a CVE last year with Safari and Chrome not stripping origin header on redirects.  Mozilla still does not send Origin header in all cases that other browsers do, e.g., cross-origin form post.  Some inconsistencies in how outbound initial requets are sent.    
bhill: the addition of the 308 status code wasn't done correctly in all cases, but I'm encouraging folks to polish that up this year.  
alex: so we could do this as a working session, maybe at the next meeting, where we could set aside time for enumerating the issues, perhaps bring in other folks who know/care, and can start to write up a position/status document  
mnot: we could then plan to do something larger around TPAC, if that's warranted  
alex: yes, think it is  
mnot/plinss: yeah, this is about the overall architecture of the web  
[agreement that redirect situation is nutty]  
  
Sub-Topic: CSP status  
alex: mention yesterday of new syntax for CSP?  
mkwst: not that I know of.  We're talking about extracing out a reporting API as a backend for CSP, public key pinning reports, error logging, etc. as a single way to do this for all specs that need to send report. One-stop shop for security/privacy considerations/mitigations.  
mnot: [discussion about using JSON for this]  
mkwst: I'm coming around to using JSON, with the CSP stuff, we'll think about doing it if something changes  
[discussion of JSON and the term "data model"]  
  
Sub-Topic: status of Secure Contexts  
mkwst: status is that the spec is Done.  
[much rejoicing]  
mkwst: waiting on the status of an WebIDL change  
https://github.com/heycam/webidl/pull/65  
mkwst: the idea is that it would be good if an API could specify if it was linked to a secure context  
... we concluded last year that if we lock something to a secure context then we can remove it entirely from the DOM, so the feature detection would work (in the sense of it not being there at all). I don't really care which way we resolve it, just want it done. We have 2 options: don't expose it or throw on access.  Current PR takes "don't expose" option.  
Alex: throwing is insane.  
mkwst: was me, but then was talked out of it but then anne supported...  
travis: not creating is easier for Microsoft  
mkwst: there was a discussion at TPAC about allowing this to be worked around with document.domain, but it turns out that it's far too-widely used in the real-world to ignore it. We'd like to drive usage down.  
mkwst: If we get to a state where secure context can change dynamically, then we'd start throwing after the status changes if code has references to the object that would have been hidden.  
alex: sounds reasonable. Mostly unhappy about the idea that accessing the object would throw in some cases and not others. It's OK if things change and a neutered object turns into a bomb as this is an extrordinary case.  
mkwst: this is done; we just need to figure out how to polish it off  
[discussion of it being a TAG \& WebAppSec Joint and what that means for publication]  
  
RESOLUTION: we resolve to support the current draft and would like to see it move forward to publication as soon as possible  
  
Sub-Topic: unblocking HTTPS Transitions  
bhill: will attempt to relay martin thompson and richard barnes response, which was roughly that if this was going to be "purely transition" and would eventually go away, than the investment might not be worthwhile vs. HSTS, priming, and redirects.  
[crickets]  
  
[thanks to bhill and mkwst for joining]  
  
TOPIC: Extensible Web Summit Debrief  
mnot: we've published the minutes from the sessions; we had 50-55 people total and we had some substantial discussions. Not as intense as Berlin, but good  
andrew: what's the goal?  
alex: one possible goal is for us to learn from the community about what's going on outside our walls; some of the sessions were good in that respect  
mnot: ???  
dka: the first time we ran it we were starting to do developer outreach events since there were so many implementers in SF; and that was a specific community that we could draw together. Folks who work on browser engines and frameworks but who might not be directly participating in standards work but have a lot to say.  
dka: the only other one we ran was in Berlin; we also run regular developer meetups.  
mnot: for me, the EWS events are a lot more valuable than the "meet the TAG" events that sort of devolve into us having a chat  
dka: I think those are valuable in terms of at least doing our work in public.  
mnot: something that came up was that nearly every session touched on privacy in some way. Someone remarked that "it's not like you have a separate security group any more, it permeates everything you do"  
dka: I think that's another reason to have these events so we can temperature check, to make sure it helps to prioritize our agenda  
dbaron: most of the sessions I went to didn't touch on security/privacy, so some confirmation bias ;-)  
[discussion about name, planning, online presence]  
  
  
[discussion about size, frequency, length of event, etc…]  
  
Andrew: useful to have a record of the event that's more readable than live-scribed minutes.  
  
mnot: if we were to do it more than once a year, I think it'd continue in its current form, it'd continue as low-to-medium-effort, middle-of-the-road impact. If we want to accomplish more, than doing it once a year makes more sense.  
andrew: if there's less to do because the format is unconference, than it may be possible to do it more than once a year.  
dbaron: I think the geographic diversity is very useful; for the CSS session, a lot of people were talking about a library written by somebody from Melbourne (who couldn't make it that day, but had wanted to come).  But follow-through seems important.  
alex: we haven't done much to book-end things; a structured narrative around the event, intros and end-talks that set the tone, talk about where we're succeeding and how to participate  
[discussion about July/Stockholm]  
  
dka: maybe we should do a blog post about the event, talk about what happened, send out links, and summarize themes.  
  
[on agenda for tomrrow]   
  
[coffee break]  
  
[back from coffee break]  
  
Mini-Topic: TAG github organization  
Dan: Have TAG members, ex-TAG members, and some other collaborators; setting that up as 3 distinct groups.  
  
Topic: Spec Reviews!  
  
### Security Questionnaire  
https://github.com/w3ctag/spec-reviews/issues/77  
Alex: did we mean to bring this up with WebAppSec folks?  Oh well.  
  
### Advice for Spec Authors  
https://github.com/w3ctag/spec-reviews/issues/78  
mnot: we talked a bit about doing stuff to the homepage yseterday; happy to make this part of that  
mnot: if we refresh, this might be a page page rather than a wiki page  
  
### Opportunistic Security  
https://github.com/w3ctag/spec-reviews/issues/80  
mnot: that spec is still on hold.  With chair hat, not convinced it has implementor interest beyond Mozilla, and even interest at Mozilla is 1 or maybe 2 people, but has been implemented.  Could publish as experimental.  But Brad's opportunistic/transitional thing is so similar -- one of the reasons we held it.  Seemed suboptimal to have 2 floating around.  If Brad's thing doesn't get traction, then maybe publish op sec as experimental.  Issue against alternative services spec (in IESG review).  Alternative services (treat that host and port over there as though it's me) is new ish.  Response header in HTTP1, new frame type in HTTP2.  If you change hosts the alt svc needs to be strongly auth as the origin.  If www.foo.com redirects to alt.foo.com, cert needs to cover www.foo.com.  Doesn't need to be same cert, but needs to be authoritative for that host.  And maybe some experimentation with additional constraints.  If on same host, then don't need .  
alex: what definition of same host?  
mnot: will follow up  
Yves: key pinning?  
mnot: has to apply to both  
mnot: alternative (if it fails) is to just fetch as though no alt svc.  
mnot: so like DNS-based   
mnot: Some pushback, from Mike Bishop (MS), require strong auth -- worry about shared hosts, listening on port.  Current mitigation is not allowing to go from standard port to high port or vice-versa.  Feedback is that that's not a bright line anymore; many OSes don't have meaningful privilege to low ports.  
mnot: Could go 2 ways with this -- just drop it -- or instead require strong auth for same host.  And drop opportunistic security spec altogether.  
alex: why?  
mnot:  It breaks opp sec. A use case for opp sec making it easy to deploy -- scheme stays http, but things happen over https.  
mnot: ...  
mnot: For our purposes... might come to a head in the next few weeks, or at the latest at Buenos Aires IETF.  
mnot: Worried because didn't really coexist with Brad's thing.    
alex: wait a month and see what happens?  
mnot: We can probably close this issue unless someone thinks we need to track discussion we just described.  
alex: would like to be notified  
mnot: either we'll publish as experimental (RFC) or not publish at all  
mnot: and implemented in Firefox  
mnot: I'd bet slightly on publishing as experimental RFC.  
Alex: I'd want to make clear that the Web has assumptions built on secure contexts and the origin model, and concerned about things that impact relationship between content and origin model.  
mnot: If browser makers were to make statements about whether they would/wouldn't implement, that would be input into the process.  
mnot: say something as TAG, or close it?  
peterl: what would we want to say as the TAG?  
alex: welcome lower barriers to entry to TLS, but have concerns about coherence of same-origin model and would like to be informed if this receives wide adoption  
dbaron: what's the concern with this and the same origin model?  
alex: shades of gray bottom out at how opp sec relates to secure contexts  
mnot: you saying isn't opp security -- a constrained set of properties being gained  
alex: need to be clear that opp sec isn't a secure context  
dbaron: sure, but given that, is there a problem?  
alex: no  
alex: ...  
mnot: could certainly add text to opp sec  
alex: happy to just close issue  
(mnot and alex look at spec)  
mnot: so it's just the host string in the URL:  host portion of origin must match to do alt svc without strong authentication  
alex: seems really bleeeaaaghhhhhh  
alex: exception of being able to do alt svc to same host on different port seems bad  
  
### Automotive WG  
https://github.com/w3ctag/spec-reviews/issues/81  
Domenic's Design Document (DDD): http://w3ctag.github.io/design-principles/  
travis: I can dive in, and probably look towards end of February.  
peterl: Issue in automotive github repo, linked to another issue on ??? handlers, linked to another thing on generic sensor API, so may be driving towards resolution.  So probably important to take a quick look short term.  
travis: ok, slot in for January 27?  
  
### Performance API review  
https://github.com/w3ctag/spec-reviews/issues/83  
alex: didn't we talk about this yesterday?  
alex: I'd mark this as a dupe?  
travis: other is issue 18  
  
### new Indexed DB methods  
https://github.com/w3ctag/spec-reviews/issues/84  
?: who's familiar with Indexed DB?  
alex: yes  
travis: at first glance these seem like great additions  
alex: ...promises ... I'll look at this  
  
### storage persistence  
https://github.com/w3ctag/spec-reviews/issues/85  
alex: this is about ... we should probably review the storage API (not particularly happy with it), I don't think the notion of boxes/buckets.  These methods don't seem bad to me, but would like to see mapping with permissions api -- would like to see permissions state reflected.  Seems like least contentious part of storage API proposal.  If you clear coookies and cache, will still go away -- just privileges it over automatic eviction.  Will be a UA decision about ... ..   I'm tempted to:  as long as it continued to abide by guidance on unsactioned tracking and control surface for users, they seem fine.  Use promises, promises look good.  
travis: this is not a third way -- but an explainer about how storage works.  
alex: and about how long allowed to live, and relative to other origins, ...  
(Alex writes comment in issue)  
(Dan leaves; Andrew left maybe half an hour back)  
Alex: whole boxes concept is DOA.  
  
[lunch]  
  
## FIDO  
See https://www.w3.org/Submission/2015/02/   
Fido stands for Fast Identity online, not federated. In fact, it's not really about identity, not about validating identity. It's an authentication scheme.  
You can also use it anonymously. Like with a password, you are establishing a relationship with one server. With this, the server doesn't have to take risks as it does with passwords (as passwords needs to be stored in one way or another on the server (the passwd themselved are usually not stored per se, but hashes are). In the case of FIDO, the server stores only public keys, and the private key is on trusted hardware on the client side.  
When talking about an origin, you are not disclosing other information about other origins.  
FIDO is seen as replacement for a password, but it can be used as the second step in a two-factor authentication, in addition to a traditional password.  
  
https://www.w3.org/Submission/2015/SUBM-fido-web-api-20151120/  
* makeCredential looks a lot like keygen. Asking the UA to generate a key pair, storing safely the private one, and answering with the public key.  
* getAssertion is where you prove you have the private key associated to the public key used in the challenge.  
  
Yves: is there ways to ensure that the relation between the UA and the hardware is not snooped on? (like what can happen with USB tokens fo example).  
Travis: it's outside the scope of this document, but the UA still needs to provide a "safe" UI, like using pin, face recognition, etc... before talking to the hardware.  
  
David: what is the role of the hardware, just storing the keys?  
Peter: store the keys and perform cryptographic operations.  
Mnot: the devices are usually quite limited wrt storage.  
Yves: are the keys ephemeral or do you need to store them for a long time?  
Travis: not ephemeral, but the server can remove the pubkeys when it wants. Both parties have the possibility to revoke the relationship.  
David: how about multiple devices?  
Mnot: you have to authenticate using the two devices, then yo need a way to make a relationship between the two server-side, but it's outside of the scope of FIDO.  
  
Travis: now reading the page about keygen http://w3ctag.github.io/client-certificates/ Section 6 is about requirements for a keygen replacement.  
(checking bullets one by one)  
* provided by FIDO  
* User Account information is providing that.  
* "must be considered a "powerful feature" and only available under secure contexts." it's a SHOULD in FIDO.  
* "must not release the raw private key material to script at any time." by design. Note that FIDO is not about identity (last part of the bullet).  
* Async, yes.  
* "should allow the user to delegate the key persistence and generation to separate secure hardware." by design.  
  
alex: this doesn't do the thing some folks wanted -- persistent x-origin identity -- but that's a feature as far as the Unsanctioned Tracking Finding goes so ¯\\_(ツ)\_/¯   
Travis: So the conclusion is that FIDO can be a potentially good replacement to Keygen.  
Note that FIDO won't act as an identity attestation  
  
Topic: Credential management.  
Credentials, In password credential, client-side js can't access password.  
Also even if the credential manager is able to give back the credential object, it can be set to require user confirmation.  
Alex: needs more code example / explainers of FIDO to check that the integration with other specs works.  
https://www.w3.org/Submission/2015/SUBM-fido-signature-format-20151120/  
Travis: the goal was to have the same as the WebCryptoApi  
Alex: In 3.1 hashAlg is not using the same names as WebCrypto.  
Travis: we should raise an issue.  
Alex: in Credential API, things like imageURI or id are not clear.  Images should use size/etc. information like in web manifests; might need multiple sizes, etc.  
David: There are interfaces in both specs called Credential.  http://w3c.github.io/webappsec-credential-management/#credential http://www.w3.org/Submission/fido-web-api/#api  There is also a mismatch between Credentials (FIDO and credential management), 'id' and 'type' not having the same types.  
David: Issue is that we got issues with cookies are eTLD+1 rather than origin, which is believed to be a mistake, do we want the same here?  
Alex: no.  
Mnot: we should talk with FIDO people.  
Alex: say, invite them to a call, we don't need to wait on a working group  
  
TODOs:  
    - clarification on mismatch between WebCrypto, FIDO Signature Format, JWA nomenclature on hash algorithm naming  
    - clarification on some data structures  
  
   *     - Credential interface, e.g.:  
                  *  - 'type'  
           *  - id  
           *  - imageURI (align with manifest syntax for multiple sizes?) in User Account Information    - reasons for eTLD+1 rather than origin (and unclear wording in section about how the origin and RP ID are used in authenticator operations)  
    - feedback on the API design  
       - options object instead of optional params?  
       - clarify the Credential interface between Credential Management draft and FIDO drafts  
    - specs need more examples \& explainer doc, e.g. end-to-end code for Credentials + FIDO?  
    - specs need more links of terms to their definitions  
    - request time to meet at a TAG call  
  
put in https://github.com/w3ctag/spec-reviews/issues/97  
  
## Web Payments  
  
The WG doesn't have a stable proposal, will wait for their next F2F late february.  
Note that they should concact us when they have something ready for review.  
  
## [EME Secure Release](https://github.com/w3ctag/spec-reviews/issues/73)  
  
https://github.com/w3ctag/wiki/wiki/Shutdown  
  
Travis: difficult to pinpoint what should be the hooks for shutdown.  
for Beacon, sendBeacon is defined as being reliable, meaning that in case of a power shutdown it should be requeued to be retransmitted. In reality it is more 'Best Effort'  
So, the timing for close is not good, and there is no longer safe hooks in the platform like sendBeacon could have been.  
Mnot: can a sendBeacon be blocked by an adblocker?  
Alex: yes, ad blockers are more privileged than sendBeacon.  
Travis:  the percentage of times beacon is reliable could be a metric on its use here.  
  
[break]  
  
## TAG Site Design  
  
[whiteboard design/discussion]  
  
On tag.w3.org:  
- About  
  - Who  
  - Why  
  - What  
- TAG User Guide  
  - Audience Specific Info  
  - Github  
  - Mailing Lists  
  - Starting Points (link to publications, etc)  
- Events  
  - EWS  
  - Meetings  
    - Agendas  
    - Minutes  
- Publications  
  - Findings  
  - RECs  
  - Other  
- Spec Reviews  
- Old Stuff  
  
Remove redundant data from w3.org/2001/TAG  
  
## Spec Reviews  
  
[Network Information API](https://github.com/w3ctag/spec-reviews/issues/86)  
  
mnot: this is the newer version of figuring out what the network is doing  
... they talk about the underlying tech for first hop  
dbaron: from css experience, sec 4 scares me  
alex: this is a long debate with lots of alternatives, note these may be a lie (eg tethering over wifi), which is why max is important  
mnot: known this if imperfect, but for parity with ap/fetchps...  
dbaron: [discussion of flaws with css media types] (notes css moved to feature detection)  
alex: oses don't give us good information eg metered or not, downlinkMax and online/offline are mostly what you want to look at, everything else is fuzzy  
mnot: these is discussion about providers giving us this info  
plinss: possibly UA could provide UI for user to enter params  
alex: people want to detect connection changes, some providers, like youtube want much more, like rtt time, room for expansion, I support this for producing the info that isn't a lie  
dbaron: how is this diff from os  
alex: os will tell you connection change, uplink/downlink speed, wifi type, cell connection variant, which all can still be lies  
[discussion of tcp multipath]  
mnot: the api itself seems reasonable, we'd love it if more vendors participating  
  
  
[Review FormData additions in XHR](https://github.com/w3ctag/spec-reviews/issues/87)  
travis: whatwg/xhr#27 seems reasonable  
alex: other constructor types, like json serialization/deserialization would be nice, like that it's itertable  
[discussion of json]  
[discussion of set/delete with multiple entries per name]  
[discussion of usvstring vs domstring]  
plinss: concern if able to construct from elements with domstring names contining unmatched surrogate pairs, would be unaddressable via usvstring api  
  
  
[Feedback on DOMError -> DOMException in Indexed DB](https://github.com/w3ctag/spec-reviews/issues/88)  
  
alex: looks great, lets do it, make a note to ourselves to include in our doc for spec authors  
  
[Geofencing FPWG](https://github.com/w3ctag/spec-reviews/issues/89)  
  
[defer until hadley available]  
  
[Bluetooth API Security Model](https://github.com/w3ctag/spec-reviews/issues/90)  
  
mnot: some things that use bluetooth, like speakers should just use audio api, etc  
... question is how to access other random paired devices  
[discussion of bluetooth profiles]  
[defer until torgo available]  
  
  
[Streams General issue](https://github.com/w3ctag/spec-reviews/issues/92)  
  
[discussion of stream types, clock driven, btye streams, object stream]  
alex/travis: might be helpful for us to define \& classify stream types and usages  
  
[adjourned]





