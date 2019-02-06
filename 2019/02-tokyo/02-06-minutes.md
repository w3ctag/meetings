## TAG F2F
##### 06 February 2019

Present: Kenneth, Yves, David, Daniel, Alex, Tess, Travis, Alice, Sangwhan, Michael(tm) Smith, Peter Linss (remotely)

Regrets:

---

Agenda:


---

### Signed Exchanges and Bundling

Visitors present: Andrew Betts (Fastly), Mark Nottingham (Fastly), Jeffrey Yasskin (Google), Kenji Baheux (Google), Kinuko Yasuda (Google).

-introductions-

Kinuko: Quick presentation for updates. ([Slides](https://docs.google.com/presentation/d/15JtRVNNajiKeMMGEQFA25TI8GWyG3gAmkThsunQANww/edit#slide=id.p))

Jeffrey: TAG proposal from 2015.  Just a list of files, no proof of origin.  I picked it up in 2017.  Tried to make it work for P2P sharing.  HTTP WG suggested splitting into 2 pieces, became signed exchanges and bundles.  AMP and distributed content discussions.  Latest drafts have fetch (WHATWG) side spec about part, and IETF side spec about format and how you generate them.

Dan: One editorial comment:  I know the current thing is only roughly related to the 2015 web packaging proposal.  I think in your history presentation you ought to mention Jeni Tennison as editor of that.

Alex: A set of use cases aren't mentioned here, originally designed to help address: how to address multiple resources from a single file.  In that case it was CSP, where you may have many CSP files which are related as a single package of data.  Hash navigation into them as a way to address them was top of mind at the time.

Kinuko: I reviewed that proposal again when preparing for this presentation.

Jeffrey: ... contact her and see if she has comments about the new proposal.

Dan:  Sounds good.  She's currently CEO of open data institute in UK; may have requirements.

Jeffrey:  Current structure fo the specs: exchange, pair of HTTP request and response.   (bad audio) ??? similar to TLS certificate but not the same.  We can then bundle exchange ???.

Kinuko: Split the two: signed exchanges and bundled exchanges.  This spec introduces signed exchanges concept on top of exchangses (pairs of HTP request/response).  Signed exchanges are cryptographically signed.  On top of that, spec for bundled exchanges.  A bundle of exchanges, signed or not.  Could represent entire website.

Travis: Is bundle signed?

Kinuko: Individual exchanges are signed.

Yves: Are you asking if the entire bundle is signed so you can trust the party that sent the package?

Jeffrey: Right now the design says no, but I believe we'll need to; it has the important property that you pin all the versions together.

Kinuko: This proposal specifies concept of loading:  how the UA can load signed exchanges and bundled exchanges.  Later can be integrated into fetch spec.

Kinuko: Running an origin trial with Chrome, got feedback from several groups.  Positive feedback from origin trial.  Mixed feedback from other browser vendors.  Mozilla currently opposed.  Trying to ask them to reconsider.  Chrome plans to ship signed exchanges in 73, and starting to work on bundled exchanges, to bring a native package format for the web.

Jeff: Security tradeoffs: a couple reductions in security relative to TLS.  Mitigations we're proposing -- some we're not sure which direction to choose.  List of things we'd like help with.  First is that atacker can replay a personalized response.  Attacker could replay setting a cookie, could unknowingly put person into attackers login.  We block the Set-Cookie header.  But an attacker could confuse people by taking information personalized for the attacker and pretending it's personalized for the victim.  Have some advice -- We don't know how to enforce that -- and not sure it's the right advice.

Travis: Requires encoding the response in the signed exchange?

Jeff: The core mistake the site makes is signing the personalized response.

Alex: Also a few mitigations already.  A restriction on particular state-setting headers.  And you mentioned earlier in presentation, require a different certificate type.  The requirement to generate exchanges is high enough that hopefully people don't do it without foreknowledge of what they're doing.

mnot: One thing I've heard people want to build is personalized content.  e.g. ???

Jeff: I don't think it akes sense to use this to send *your* mail.  I think it makes sense to use this to send the gmail application.  You don't want to distribute the mail to anyone except the person -- you want the TLS connection, the 1-to-1 pairing.

mnot: I haven't read the document set recently -- is that use case very explicitly marked out of scope in the documents?

Jeffrey: I don't think we specifically say don't sign mail/tweets.  We talk about signing applications.  But we can make that more clear.

Mike: I wanted to ask what exactly a personalized response means.  To qualify that, I recognize you can keep state information from headers.  If you're not doing it through headers, you can have application specific stuff, query params in urls, that the server knows to store state information.

Jeffrey: The way I can see this being a problem.  Say you're logged in to your barnk .  Make a request with cookies to the bank -- and bank signs response to you.  The response includes name, balance, etc.  When they just sign your thing, you're not likely to redistributed it.  If an attacker sets up their account in a particular way, gets the bank to sign a particular URL, and gives it to the victim -- they might be able to trick the victim into paying a bank fee, or sending money to the wrong person.

...It should be public information that applies to everyone.

Mike: Are the cookies from the browser's cookie store sent back?  I heard you're not allowing Set-Cookie.  Do the cookies go back in the rpsonse I guess?

Jeffrey: It's mostly the response that is signed.  When you request the signed exchange itself you're geting it from a distributor.  When you get the original signed exchange you might send your own cookies.  When the origin server is planning to sign the result, the ??? shooulld strip out the cookies before sending it to a backend.  One thing we could do which would break things somewhat is say you can on/ly receive a signed exchange if you make a fetch without credentials.  That forcese you to know it's going to be a signed exchange before you fetch it -- makes things a little more fragile -- but it could work.  That's something the TAG might suggest we look more into if you think it's a good way to mitigate the problem.

Jeffrey:  Second tradeoff:  a signature lasts more than a minute.  Attacker can replay content.  We currently bound signature liftetimes at seven days.  It's arbitrary, could be tweaked in any direction.  If the origin signs JS with an XSS vuln, attacker could replay the JS and exploit the XSS, and take people's cookies / localStorage / etc.  The only way to block that is to make a blocking request to the origin which prevents this from fixing AMP's problem -- introduces an extra round trip right when they're trying to instantly load a page.  And it breaks offline use cases, e.g., peer to peer sharing of apps.  I think it's a necessary compromise... that an XSS stays alive for the length of the signature.

... other way to use this is, say you're a new site, you report something wrong and quickly correct it.  Attacker could replay it for a week.  We could mitigate this with a nonblocking request to the origin... and reload the page if it says it's invalid.  This compromises some of the antisurveillance properties of signed exchanges.

Alex: This is a property of the client's belief ....   client could trust for longer or shorter period than the 7 day period.

Jeffrey: Signature validity is set by the publisher.  For some offline emerging market use cases I think we'll want to let the client trust for longer than the signature if client is offline -- but not making that argument yet.  There are intreesting security implications of trusting something longer than publisher said it could be trusted.  We could say, more aggressively revalidate if signed more than 2 days ago.

Kenji:  For antisurveillance aspect, could be an opt-in feature.  Different user agents could have different defaults for different markets, and so on.

Jeffrey: 3rd way we reduce security is that we no longer require that an attacker using a misissued certificate be on path.  Normally to intercept TLS you need to intercept DNS or routing protocols.  With both signed exchanges or secondary certificates (in TLS WG) we relax that on path requirement.  We're doing things to reduce chance of misissued certificates.  We require CAA Record in DNS to allow this at all.  Require Certificate Transparency and OCSP responses.  Misissued cert can still be used for about 2 weeks before client will realize it's revoked.  One draconian thing to do that is say that certificate must be at least 2 weeks old to use for signed exchages.  Obnoxious, but available.

... if private key is stolen, how do you tell somebody is taking advantage?  Can currently watch DNS and routing tables.  With signed exchanges might be able to do it silently for a long period of time.  Want to be ble to report that signed exchanges exist for your private keys... without having users all have to tell you.

Alex: requirements from CAB forum will still exist?

Jeffrey: We require Certificate Transparency... more than for normal browsers.

Dan: Can you explain the risk case in this last bullet a little more?

Jeffrey: 2 risks here>  One is that attacker convinces a CA to issue a cert under your domain name.  That happens more than we'd like.

Dan: Then leads to someone being able to spoof that they're you.

Jeffrey: The second risk is that tey break into your system and steal private key for valid certificate that you have.  They can then spoof as you.

Jeffrey: Today if they do that they have to intercept traffic meant for you -- we're removing that interception requirement.

mnot: This is part of a larger discussion, we're designing other systems with similar properties.

Dan: Kenneth, you mentioned a case this morning.  Is that covered?

Kenneth: ... bad regimes ... hard to block ???.  I think some regimes might find a news site that they don't want to share.  People might want to distribute in other ways.

Alex: Is it fair to say Jeff and Kinuko that this is designed with anticensorship properties in mind as an explicit positive?

mnot: I've heard a lot of interest in that case as well.  Are those workflows enabled by the fetch integration?  That's kinda where the rubber meets the road.

Jeffrey: It's not specified yet.  Haven't specified how you load one of these froma file.  fetch integration is now all about how you load one of these over HTTP... not from a file.  But it should work to load these from a file.

Alex: Kinuko, I understand you added in the heading field a default entry.  A way to find the main resource in the signed excahnge.   So if you were to receive a signed exchange as a  file, there'd be a way to know how to find the primary content in the file.

Kinuko & Kenji: for a bundle

Kniuko: fallabck url could work in similar ways.

Jeffrey: In order for us to upgrade signed exchanges as the standards community tells us, we've defined a fallback url, so that if we don't understand the format we can redirect to the url.  IN a bundle that's the primary URL.

David: (assks question)

Jeffrey: In order that the fallback URL is accurate, the fallback URL is used by clients that do understand the bundle use it as the primary url of the content.

mnot: that's designed for incompatble changes.  Facilities for compatible ones?

Jeffrey: fewer than there used to be.  We could add some back as standards community gets more comfortable with it.  We've made parsing stricter because we have incompatible change, versioning designed in there.  When we rev the version the signatures all become invalid.  The version number is included in the signed string.  So you can't use a signature across 2 different versions.

mnot: semantic versioning?

Jeffrey: no, just a single number.

Dan: you mentioned anticensorship as a design goal. Is that explicit?

Jeffrey: use cases document lists that as a goal

Dan: question that comes to mind:  what if you are a small long-tail web site or service, if you're enabling a protest movement in a country that has an authoritatrian regime, and your'e dsistributing information about when and where to assemble to protest something... and the government decides to close the internet that day... but you're not a major publisher, you're not a google or a NYT ora small student protest group... how easy is it to take advantage of this techonolyg to enable those people who don't have their upstream access to the internet but they can still receive and validate this informatio against the origin it was originally signed rfom?  How can we enable the small players to use this just as easily as the big origins?  Or maybe not just as easily, but also.

Kinuko: Distributed ??? is ... addressd naturally by this specification.  The case has 2 situations.  Offline ??? being detached from the actual origin -- how to circulate the actualy.  For the latter part -- this cuts the limitation of the distribution, this can be basically transferred over any media, p2p, sd card, can bring the information inside the wall.  There should be some altrenative network.

Kenji: could imagine a couple things happening.  The website doesn't have a signed exchange, but some people could get that content -- could be a feature in the UA that lets you share the content -- but wouldn't be able to sign it since that would be wrong, but could let you share.  If the website forsees it, then they could make the content available with a signed exchange, and they could make it available in a way that people trust.

Dan: The use case comes from a specific presentation from an organizer of the tahir square protests in Egypt, where this specific thing happened, they were stymied by... this specific thing happens.

Jeffrey: If you have a distribution network that can distribute content of big players, it should also work for small players.  You need a way of sharing files around, and signed exchanges allow to validate that the file not modified by people who handed it to you.

Dan: We have topic later today on ethical technology standards.  Don't have agreement yet.  One thing I wrote as a strawman about freedom of expression.  That being an ethical standard we try to apply to new web technologies as they're developed.  That's something we could potentially play... could influence our feedback about, Jeffrey, you specifically mentioned surveillance reduction -- reduction of surveillance resistance.

Sangwhan: Two questions:  One, proxying from publishing comunity - they had a question about this beig designed for short term packages.  They want to be able to put packages on e-book reaers, which doesn't guarantee being online on the time?  Is that a consideration?

Kenji: It wasn't clear to me if they cared about content from specific origin, or integrity of the content. 

Sangwhan: I think integretiy is enough... not sure epub even does that now.

Kenji: ...

Jeffrey: There's a tension between long lived content and guarantees that it came from the origin. Signatures don't last forever.  In long term algorithms get broken, in near term fin bugs in content.  We have strong reasons to both shorten and lengthen maximum signature liftemie.  We need to keep talking about those tensions.  Mozilla and Apple have asked to shorten.  Publishing community and emergenging markets groups less directly asked to lengethen  it.  I don't want to make that decision unilatelarrly.

Kinuko: We keep hearing request -- longer term.  One thin is that UA could show different UI treatment when it shows old content.  For different use cases, different UA treatment could be possible -- but also security risks.

Sangwhan: Other thing that came up, publishing don't care about signing -- could be bundle of unsigned exchanges.

mnot: Could be the UI diference is that I'm reading it an ebook reader which has different expectations from a browser.

Sangwhan: Seems very useful for saving web pages (Ctrl+S)

Kinuko: In our use cases document -- could be an unsigned bundle.  

Travis: Is there an idea that you could load some signed exchanges and unsigned one would be like mixed content warning?

Mike Smith:  One use case from intent to implement thread -- discussion with ipfs people -- didn't have time to read through and understand it -- but I know what they do -- if it enables some use cases for them could be interesting.

Kinuko:  They could make the content of ipfs available over the web with the integrity information.

Mike Smith: The interesting thing about what they do is that the urls don't break -- it's a way of ensuring urls don't break -- but it's a lot less than ideal way.  If it could help with long term preservation of web resources, woud be interest from other areas of w3c work.

Kenji: Another set of use cases I want to learn more about -- people sharing information to chat app -- people want to know if it's fake news. People get killed over that.  Is this part of ethical technology topic?  Is there more we could do there?

Sangwhan: Not strictly technical -- as long as you can buy a certificate

Andrew: On use cases -- was the consideration given on using bundled signed exchanges in use cases where we currently use PDF as a downloadable portable document format, and as a replacement for File->Save in the browser.

Jeffrey: Definitely a repalcement of file -> save.  PDFs have some extra properties about looking the same...  not sure you'd really want to replace PDFS.  One of goals of pere-to-peer sharing group that started my involvement with this.  Say, I saw this web page, it's cool -- replacement for MHTML and Save as-complete.

Andrew: not complete replacement for PDF?

mnot: ??? an email, for exmalpe

Kenneth: there is another case for creating new derivative formats, like a next gen epub, with additional restrictions (ie. disabled JS, etc) and a different validity length for certificates (talked about exploring a replacement of epub). This way a browser and runtime can thread these files differently

David: I've talked to people who were using PDFs just for the bundling.

Yves: Last TPAC, we've talked about use case for archive.  If, say, library of congress, signed at a certain time -- could it be shown in a way that it's. trusted


Alex: Commonality about unsigned bundle -- there might be a new mode for web content -- we have incognito mode, iframe sandbox, etc.  So there's room to do this... archiving is interesting because it's a different point in the space where you'd like to get some historical notion of authenticity 

Yves: Know the original signature...

Alex: Want an out-of-band mechanism for validating with whovere signed it that it's still a signature you should trust.

Yves: Could be good for publishing industry.  Want epub book to have longer life than just a few days.

Mike: To respond to what Andrew said orignially and whatDavid reiterated -- feedback I've heard fro discussions with publishing orginazitonsiot involved in w3c is that as far as replacing PDF cases they don't care about the preserving the rendering necessarily, they care about portability.  In that sence they've positioned epub/IDPF, trying to positon it as a replacement for PDF.  Already have work looking for replacement for PDF.  Marcos Caceres and I were having discussions with them a few years ago.  They want portability.  What does portability mean?  We have a URL -- but what they want is portability off the web.  Readability systems do things offline.  Essentially at the time they wanted something that changed the web security model.  We told them at the time that we're not going to be changing the web esuciryt model.  Somebody needs to get back to those people in the publishing group and find out if this is still... maybe you've been having discussions with them?  Leonard Rosenthal  from Adobe was one of them.  Main person to communicate with more about current use cases in publishing is Tzviya who's the chair of that group.

Dan: Was tsupposed to be a workshop -- got delayed.  Theoretically that could be a forum for those discussions to happen.  Intention to socialize the work with the publishing community, not only commercial publishing community (consumer glossy magazines), but also scientific journal academic publishing community.

mnot: for the sake of clarity, the intent of the workshop was to engage the online publishing communtiy -- maybe ??? the advertiser ecosystem.  We expanded it to the paper publishing community.  Web sites that might be packaged was the scope there.  Maybe to get to the workshop we could have a discussion about next steps.

Dan: need to draw a line under the discussion and find nxt steps in general.

mnot: IETF next steps, TAG next steps, Jeffrey & co next steps

Alex: This feature was split into 2 at request of IETF.  The noly thing that will ship in near term in any browser was signed exchanges.  Almost all book use cases are bundling, which is being designed now.  Still time to influence that.

Mike Smith: concretely, what I'd like to propose the TAG consider doing, is working to get some kind of stamenet from Tzviya or whovere she wants to delegate to find out whether this (signed exchanges & bundling) address the use cases.

Alex: Bundling still being designed, so good to have a conversation about needs rather than public statements about whether it works.

Dan: You're asking us to ping Tzviya as chair of the Publishing WG within W3C?

Mike Smith: I don'tthink we have to have a workshop to find out what Tzviya thinks...   Yes, under her hat as the chair of that group.

Dan: That soudns like a  concrete step we can do.

Alex: I'll note if the workshop is going to move forward -- I'm soon to be an ex-TAG member  -- so 'd need to be deputized or find an alternate.

Dan: (signs) I did tell you you couldn't escape.

mnot: A lot of conversations in IETF land and associated places.  I think people are warming to the ideas here.  I think still needs to be some discussion.  I think people are now getting imatient to have that discussion.  Jeffrey, thinking about going to dispatch in Prague or something else?

Jeffrey: Plan we'd talked about before where I hpresentt o the HTTP WG and have a side meeting in Prague and then probably do a BoF at the next IETF still sounds good to me.

mnot: Maybe we should talk offline about whether to go back to dispatch now that time as passed and had some experience -- dispatch is one of the ways in the IETF taht new work gets started.

Jeffrey:  I'm happy to go back to dispatch in Prague if that's wht you and others think is best.

mnot:  Big question is do we still want to have the workshop, still suitable for purpose, and do we want it before or after the IETF BoF?  How to incorporation into IETF chartering discussion.  I'm kinda neutral on that now.

Jeffrey: I believe X wanted to have discussion at the workshop rather than posting comments on public mailing list -- I think we need to have the workshop to get publishers engaged.

mnot: Input on timing?  I'm talking to Area Directors.

Dan: We'd lost the thread.  I didn't even know the workshop hadn't happened as originally planned.

mnot: We could hold it in something like May... or in July right before or right after Montreal IETF -- probably still NYC to engage publishing community -- or could do after that.  On balance I think for people traveling really far, July is a bit easier, but May could happen too.

Alex: from a NYC perspective, want end of July rather than beginnning

mnot: either week of 15th or 29th of July.  May would probably be something like week of 13th or 27th.

Dan: We can take workshop planning offline.  We should be helping to figure out dates/location/host.  I'm happy to spend some time on that.  What about feedback on the issues that you have on your last slide here?  Would be useful to have TAG feedback.  What would most useful way to get you that feedback?  We have designe-reviews process -- we could start a design review and accumulating feedback and accumulate feedback in a github issue . We could accumulate feedback in our repo.

Jeffrey: We have a couple github issues that discuss some of these issue -- best form would be to comment on those -- but that would take a lot of your time.  I'm happy to summarize questions and file a design review.

Dan: If you can open a design-reviews issue that would be helpful to us -- happy to leave that feedback in other places if you want to direct us there.   And, yes, it should be a new issue rather than the exsting one.

Mike Smith: The publishing group has use case and reuirements document https://w3c.github.io/dpub-pwp-ucr/ -- that's quite thorough. THere's a requirement about authenticity.  "The publisher should be able to provide information in a packaged web publication that can be used to check the origin of the publication and its authenticity."

Jeffrey: That requirement is too vague to do anything with.  Doesn't describe what kind of signatures.  But format is able to handle anything reasonable.

Mike Smith: I think they don't know more detail.
Dan: I think that's the kind of thing that needs to come out in the context of that workshop.

Mike: I don't think we should block on the workshop to get feebcak from another part of W3C.  I'd rather you take the responsibility, but if you don't, I have to.

Dan: Help me help you.  Happy to be in the loop with you and Tzviya.

#### break

## Design reviews breakouts

### Group 1 (Awesome)

Present: Tess, Travis, Kenneth, Sangwhan, David



#### [imagesrcset and imagesizes attributes on link rel=preload](https://github.com/w3ctag/design-reviews/issues/329)

TO: Assumption that the 

DB: If you're designing a feature to preload, and have another for responsive, you proably want the same syntax.

KC: Why are the syntaxes different?

TO: sizes, hxv (link [rel=icon]), url <density|dimensions> for the srcset...

TO: We need to take a look at the whole pre-loading stuff in general (e.g., the modulepreload).

SM: Also should think about how this all works together with H2 push; preventing double loads when not necessary feels like something that needs to be coordinated

TL: Note drafted and issue closed.

#### [Element Timing API for img](https://github.com/w3ctag/design-reviews/issues/326)

TL: Assuming only elements that belong to the top-level browsing context are considered for auto-inclusion in the timings? E.g., many ad frameworks manipulate iframes to fill considerable space in the viewport and which oclude other content. Since iframes are not being considered in this spec (just img elements and maybe elements with background images), this is additional variability that would decrease reporting value. 

TL: The auto-inclusion seems nice, but will add a tremendous amount of variability to the feature that seems very hard to rationalize and get interop across user agents--thus if an origin want to compare data across user agents, the correlation may be difficult, leading to uncertainty and lack of confidence in the feature. 

TL: 'elementtiming' as an attribute on an element seems quite redundant. Perhaps something a bit shorter like 'timingname' or 'timingid'. 

TL: Would like additional clarity on the cross-origin availability of this data. E.g., is it proposed that all "hero" timings (including the auto-added items) be available in the performance entry lists for all browsing contexts of the top browsing context? This seems a bit dubious…

TO: (Side issue about issue template)

KC: Is it possible to turn this off...

SM: This could be put into lots of places...

TO: shadow trees?

#### [Querying Encryption Scheme Support Through EME](https://github.com/w3ctag/design-reviews/issues/322)

SM: Feels like MediaCap should be the superset that does this...

TO: Encrypted content is sufficiently different from other general media info that it doesn't seem like a great idea to combine.

SM: Re-reading it, I stand corrected. LGTM.


#### [Migrating some high-entropy HTTP request headers to Client Hints.](https://github.com/w3ctag/design-reviews/issues/320)

Hey Mike!

At today's Tokyo F2F, we had a great discussion about this proposal. We didn't dive too deeply into the technical proposal, but discussed the problem space at a high-level. As you might have expected, the TAG is supportive of efforts to reduce fingerprinting, especially passive fingerprinting which we think has a much smaller surface area that we can affect in the browser. Given this framing, we are actually quite happy to see this effort around the User Agent string (and Accept header) move forward. We believe it will be great to have the User Agent string (that is sent by default) ultimately have less-entropy by transitioning the entropy into opt-in client hints.

We liked the fact that, as client hints, the client can be aware of which servers are asking for the extra entropy, and potential for fingerprinting that go with it.

So... this is the official "thumbs-up" from the TAG. Please continue developing this proposal, and we look forward to being involved in future review requests!

The is TAG, signing off.

#### [Wide gamut support for Canvas\/OffscreenCanvas\/ImageBitmap](https://github.com/w3ctag/design-reviews/issues/315)

...

#### [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311)

...

#### [RTCIceTransport](https://github.com/w3ctag/design-reviews/issues/304)

...

#### [RTCQuicTransport](https://github.com/w3ctag/design-reviews/issues/303)

...

#### [Feature Policy JS introspection API](https://github.com/w3ctag/design-reviews/issues/292)

...

#### [TextEncoderStream and TextDecoderStream](https://github.com/w3ctag/design-reviews/issues/282)

...

#### [<link> rel="modulepreload"](https://github.com/w3ctag/design-reviews/issues/213)

...

#### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201)

...


### Group 2 (Modest)

Present: Dan, Alex, Alice, Yves, Mike Smith

#### [Event timing API](https://github.com/w3ctag/design-reviews/issues/324)

DA: Explainer could be in plainer language, and state problem up front

AB: This is about metrics

AR: Yes, about metrics, and the naming is misleading - it's explicitly about input events.

AB: Would be nice to see an end to end example of how developers would use this data to improve the user experience - it seems like the spec authors know the answer to this, but haven't explicitly stated it.

TO'C (outside the room): Can we push back on the occluded security/privacy review?

AB: Perhaps we just take them up on their offer to fill out tthe security and privacy questionnaire

#### [JavaScript WeakRefs](https://github.com/w3ctag/design-reviews/issues/321)

AB: "Explainer" PDF is designed to be ttalked through, not read as a stand-alone document. Makes it not function very well as an explainer.

DA: [feedback left on the issue]

AB: Can someone here explain why we want weakrefs?

AR: Want to get access to an object e.g. in a cache, which is transient. Today, a reference creates a liveness guarantee and prevents GC. No explicit memory management. This is a tool for providing developers who want access ... not to create memory leaks.

AR: ES6 added WeakMaps which don't do what you think they do (laughs). WeakMaps are a weird inversion ... the *keys* are weak. You reference an object as a key and a value like a regular map, but the difference is that the reference to the key object is weak.

AR: There is a school of thought that says WeakMaps are good, more tools. Another school of thought says weak references are bad because they don't do what you think they do.

AR: The VM community pushed back on weak references because they assert that you think you're doing memory management - but you're not. There are no guarantees about when the GC will run.

YL: If the GC runs, the weak reference may not even be removed. Depends on the strategy of the GC.

DA: Why did TC39 feel that this issue was specifically that they wanted TAG feedback on?

AR: This is a new tool for our tool chest. Weak references change the design language for DOM.

AR: TThere might be places in DOM today where this behaviour is already exhibited, butt itt's not available in userspace at all. How do we retrofit APIs to use this?

AR: THe reason this is coming up now is related to Web Assembly. wasm is looking for a way to access DOM capabilities. Part of the current proposal uses a combination of weak references and some DOM wrapping magic to allow them tto not have to go through JS every time... without creating anew GC hazard. 

AR: WeakRefs in JS could be more of a single place for these things to get sorted out. TThey will thunk through tthis weak reference thing to prevent the double access problem.

AR: Motivation is hidden by the proposal. Looking for Web Assembly proposal.

DA: Not specifically called out in the explainer. We should document why this is more important to the web platform than other TC39 proposals - we asked them to file reviews with us when they felt it was important, so we should ask them to collaborate on explaining tthat (on top of Alex's explanation earlier).

AR: My current thinking is that it looks good because it doesn't provide any new finalization mechanism. YOu don't get any destructors.

YL: ???

AR: The important part about tthat is you can only detect that att the same polling interval that you're able to today. The fact that a GC will remove that object is something you could detect with polling today, but only at the end of the microtask. This maintains the appearance of stop-the-world GC regardless of what happens underneath.

DA: Is that feedback you feel comfortable leaving on the issue?

AR: Sure... the WeakFactory feels weird, but that's really something for TC39 to sort out.

AR: the slides are relatively old...MarkM isn't at GOogle any more and hasn't been for some time

AR: <leaves feedback>

#### [FetchEvent Worker Timing](https://github.com/w3ctag/design-reviews/issues/317)

DA, AB: We like this explainer. It uses the template well.

AR: I want this. This is a good thing. This is outstanding.

DA: I'm going to leave feedback that we like the explainer.

AR: This solves a bunch of problems that I've seen teams have.

DA: Should probably have a S&P section in the explainer, even just to say "we don't think there are any".

AB: Alex, you mentioned this solves problems you've seen in practice. Are those problems outlined in the explainer?

AR: Kiiinda. I've seen teams have difficulty... There are alternative mechanisms. There are potential differences in apparent timing. One of the benefits of using the performance timeline is thatt it gives you the browser's reconciled view of global tiing. In a lot of implementation, SWs may live in a different process, so this isn't a panacea, but it will give you significantly better access for performance timing.

AR: First time you open indexeddb, can be very slow. This will let thtem quantify that - answers the question of what happened end-to-end.

DA: Any other feedback?

AR: It integrates well with the existing feature set. Performance timeline is what you'd use. I don't understand the interactions between this and the new ??? API and ... error logging? No way to get this data out to a monitoring server.

DA: Can we close this issue?

AR: I would love to. Will leave some feedback and close.

### Design principles

TL: This was started back when Dominic Denicola was part of the TAG, as a place for people to go read up on the latest... guidelines and principles.

KC: and to file issues to add new guidance

TL: it has grown, and I've been expressing interest in moving it forward; have been it's sponsor. It has been a good collaboration, allowing us ot come up with a consensus and then file PRs that get merged. We also referr to it in our design reviews. Has raised the water level for design reviews. Haven't seen a lot of "this isn't webby" because designs aren't aligned with DOM design.

TL: I won't be able to continue as sponsor, but wanted to have a chance to talk about the future of the document. Will it evolve to become more than it is, shrink, etc.?

KC: will you keep editing it, Travis?

DKA: makes some sense.

TO: makes sense

DB: Domenic has been involved in a similar way

TL: I'll continue to lurk and try to participate then. Have struggled to have the time to author the gudiance. Have allocated some time in past meetings to that and it has helped move the document forward.

KC: it's hard for one member to come up with guidance and merge. need agreement.

DB: has varied. Have been cases where we've had contentious conversations and some where it has been easy.

DB: agree it has been a valuable document that we should continue to add to.

KC: similar to other documents like the promises guide

DKA: W3C folks who are familiar with AWWW...have asked when will we do a v2?

AR: we said at TPAC that we'd continue to extract lessons from what we learn from collaborations and put them in these design-resource documents

DKA: agree we are unlikely to do another AWWW.

TO: as someone coming to us from the outside, the design-principles document seems limited to client-side API, whereas AWWW was more network/http focused. Where does everything else go?

DKA: so the question is, what is the perceived need to revise or correct things that are in AWWW that may or may not apply. 

TO: to maybe rephrase: the TAG review process is generating tons of questions about client-side API design and so those things are getting captured in the document, but if reviews end up generating other sorts of questions, perhaps those would get captured in other artifacts.

*agreement*

TL: mnot brought a networking perspective...

AR: which yves helps us understand now

DKA: we had some review requests on high-entrypy HTTP headers, reporting API format, etc.

TL: was thinking that we bumped into this a little bit when we started talking to the automotive folks. Should they do a client-side API? Or should it be modeled as HTTP because it's a micro-client-server situation. As we talked through it, we tried to parse out what we should recommend in an area that wasn't about client-side APIs. Hasn't been recorded and documented.

DKA: is that something you think should be doing more of, Tess?

TO: I think it's raosnable to be reactive. N is currently 1, so hard to extract from that.

DKA: so what can we do this week to best progress the design principles doc?

TL: ideally, having some focused time to do some authoring would help a lot. I haven't prepared, so would need to do some work there.

TL: have it on the agenda for Thurs

DKA: what's the right amount of time. Should it be a breakout?

KC: last time it was a breakout with 3-4 people.

DKA: sounds like the right approach. One group focuses on princples.

*discussion of timing*

DKA: how about we plan to schedule this for tomorrow morning at 9AM?

*embarassing high-5's all around*
(JK, your scribe is punchy)

*discussion of how/when to write streams advice*

*more scheduling discussion*

#### TOPIC: [Client Hints](https://github.com/w3ctag/design-reviews/issues/320)

TL: privacy risk to passive fingerprinting. Can be done and abused by UA string; includes a lot of entropy. System architecture, browser, version, etc. There's also data broadcast in the `accept` header. Mike West's idea is to reduce the amount of data sent over the wire by default. The idea for UA is to adopt a frozen string for the UA. Servers that want specifics, would opt into a client-hint.

YL: a similar string for all UAs? Or the same string for each individual UA?

TL: there's a different string for mobile vs. desktop, e.g. Depends on how long-term we're looking. Near-term, freeze parts. At some point, maybe everyone has one frozen UA string.

*DKA induges in press coverage future-fiction*

DKA: is everyone familiar with the EFF's Panotoclick? It tells you how identifiable your browser is. Different UAs have different levels of uniqueness.

https://panopticlick.eff.org/


DKA: if you use a particular browser exposes some features -- local fonts, GPU, etc. -- users who use TOR browser (e.g.) get put into a "bigger herd" to keep fingerprinting from being easy

TL: Mike isn't trying to solve the whole problem, he's trying to take a chip off it

DB: there's a set of things we're probably never going to obscure; e.g. major version. You can tell that through feature detection. Same for OS; too many differences to cover over. Stuff in the UA is redundant with stuff we won't fix. Passive vs. active is important, tho. With active, you have to send code over the wire to do the fingerprinting. Might be hard to pull apart the payloads, but doable. With passive, this is handed out to everyone without any work. UA is a big part of the smaller bucket of things that are in the passive fingerprinting area.

AR: while I've been hugely skeptical in the past about discussion of fingerprinting from the client-side (active) surface, I do support removing passive fingerptinging surface to the extent we can understand how muc entropy is being broadcast in general. There's still the question of network data (IP, etc.), but that's something we could do something about.

TL: ???

KC: ???

DKA: the manufacturer is something we might be able to take action on (removing Samsung Internet vs. Opera vs. Chromium-Edge vs. Chrome). We've been asking partners to split out Samsung Internet usage from other Chrome buckets because our usage wasn't being reflected correctly in the statistics. So that's a worry. We don' twant to make it more difficult to collect that level of data at a GA or statcounter level.

AR: `navigator.userAgent` could diverge from what we send over the wire; hinges on active vs. passive distinction

TL: analytics providers could be fixed. Other uses are unknown. If you get the big 6 analytics vendors to send `Accept-CH`, you could get good coverage

DKA: but that's an extra round trip

TL: but browsers cache that?

DKA: might want to feed back to Mike that these distinctions can matter; need to be considered

*discussion of Chromium-based Edge UA*

DKA: is mike still waiting for our feedback here? Is this a Mike idea?

DKA: do we have consensus that removing passive fingerprinting surface is worthwhile?

TC: wondering if I could restrict what info an ad can get

AR: ads tend to be embedded by inline `<script>`; which can pass down what it likes

*consensus: we agree that mitigating passive fingerprinting is good*

###### RESOLUTION: The TAG resolves that passive fingerprinting is *bad*, and that we should enable less of it

TL: if we want to standardize on a version nubmer, we might want a relase *date*. Folks aren't going to be releasing browsers more than once a day

KC: there are variants and channels...

TL: I like the date as a standardized way to note the version number. E.g., "this person is using a browser that's no longer than 2 years old"

AR: Can I ask a follow-up question? What happens with patches to IE11? What would the date be?

TL: Good question.

*discussion of double vs. triple digit version numbers*

DKA: there are branding considreations. Maybe some folks are attached to versions?

AR: consumer version vs. network broadcast version are separable, right?

TO: exposing a new thing seems bad? Might be intresting to someone and expose more info

AR: perhaps that's a collective action qeustion? If multiple browsers agree on an approach, maybe that makes it less bad even thouh interim has some damage?

DKA: can we feed back to mike that we support the overall goals?

#### TOPIC: [TextEncoderStream and TextDecoderStream #282](https://github.com/w3ctag/design-reviews/issues/282) & [](https://github.com/w3ctag/design-reviews/issues/332)

... subclasses ...

AR: Transform stream ??? is a class you end up using in this hierarchy. There are subclasses that end up being used. 

Adam: The only way you can gett to ??? stream is by calling tthe default constructor

The only way you can get to the constructor is by gettting object.constructor

The objects of this type are useful to you, but having tthe constructtor is not useful - one exception is to override properties for debugging. Plan is to switch streams spec to IDL; at tthat point we might expose the constructor, since that tseems tto be more webby.

Without having a ? to associatet the stream, it's not going to be usefl.

TL: tthat is typical, though.

AR: We've flagged that non-scontructible types are (an anti-pattern?)

AR: System-defined obejcts live in an other class. There is a privilege gap; the gods don't need to come back down to earth. There's generically some value about fusing those things more tightly together. Whatt is the argument here?

Adam: If you constructed one it would be useless; wouldn't be associated with a transform stream?

AR: How do I associate?

Adam: You can't, because a transform stream comes with a default controller.

AR: There's a whole part of this construction hierarchy which is not exposed in userland; that seems like a bug to me.

KC: If you inherit, can you call super()?

AR: No. There are these built-in types which we can't imagine expanding. These end up being roadblocks into creating interoperabletypes.

Adam: You polyfill by polyfilling transform stream as a whole. Classes are too tightly coupled to pylifill one but not the other.

TL: Why are they two objects?

Adam: Like promises where you want to be able to hand off one but not the other. Promise vs. Resolver/Reject functions. Similar to that... in the case of fetch, we're exposing readable stream, would be bad if someone could take that and start injecting chunks into it. 

AR: What's the optimisation ability we'd lose?

Adam: Internally it's not a sttream, it's just a fetch. We massage the data to be a stream.

AR: We do something like this for streaming rwesponses inside of fetch handlers today. Relies on extrenally observed notion of whether the response was touched. This winds up being orthogonal ... workings are available, we maintain fast path some other way.

AR: Why is this optimisation so different?

Adam: I don't know how you'd aquire the controller off a readable stream. I suppose touching that would turn off the optimisation. 

AR: You don't want to dirty it for all readable streams.

Adam: Right, you'd just dirty it for thatt particular stream. It's not just htte optimisation, it's the whole code patth tthat'd need to change.

AR: But isn't that the logical endpoint? May not be blessed by fast path but should be interoperable.

Adam: That works already, doesn't need to have transform stream type; you could subclass and give it tthat type but httat's not even neceessary.

AR: We pulled on this tthread about buffering policies which got us to this question. If you wanted to set different buffering policies, wouldn't defining your own types be the way to do that? Is there some otther mechanism?

Adam: If you create your own stream you specify the buffering policy.

AR: ???

Adam: You could have your MyTransformStream which calls the super constructor witth a particular queueing policy.

AR: Transform stream has a constructor which is callable. You can passs in a policy there.

AR: Only part which is welded shut is the controller, correct? Are there other non-constructable types.

Adam: Readable stream, Writable stream, ??? - each has a controller which is not constructable.

AR: It's just weird that it's not constructable. If you can subclass all the operations you care about then I probably don't care that much.

Adam: Hard to speculate what folks might want to do in future. Would subclass one of those streams and inject the functionality you want, I think ttat provides flexibility people need. Could polyfill whole thing, though intterferes with system ???. Again cf. promises.

AR: Promises are a bad example because you end up with a Thenable and a Promise.

Adam: I've had a lot of problems with Promises. This design with controllers was kind of copied off the Promise design.

AR: Ah, sorry.

DA: How can our feedback be most helpful?

Adam: Is tthere a tag review for streams as a whole?

DA, AR: For different aspects of streams, yes.

Adam: Maybe just file an issue against us saying that this is weird. We will Note it.

AR: Can you perhaps give us an update on the design goals?

DA: Yes, please.

Adam: My 1ary goal is you do postMessage on it and it does what you expect. The default should be you can postMessage things. You can't clone streams, they have to be transferred, which is a restriction. I'd like to live in a world where you can put anything into a postMessage and it Just Works. In the case of streams it's awkward cause you have JS running in the original scope which then needs to be proxied in the new scope.

AR: Originally couldn't be posted across the origin boundary. Will these be restricted to same origin?

Adam: Like message channel (which it is under the hood), not origin scoped. Maybe it should be. Maybe it's ok.

AR: Uh, is it?

TL: ... security reason why it might need to be scoped. You can create a message channel, take your stream, take bits out of it. By transferring you don't need to ... 

TL: so you an skip the copies, but you could already pass this data cross-origin. That's an argument against making these origin-bound.

AR: Are there opaque streams?

Adam: I've mulled it but currently no.

AR: Imagine I make a fetch to a non-CORS resource, gives me back an opaque response. I can get an image for an <img> that's cross-origin; I can't read its bytes. There's this opaque type. It potentially have abody, mheaders which I may/may not be able to read. Does this design anticipate this use case?

KC: so these would be restricted then? ...

Adam: Yes, that's something we should think about. There aren't a lot of platform streams, so there isn't a lot you could do with opaque streams - you coul dpass it to someone who can read it.

Adam: if someone puts tthis on the TAG issue we could think about it.

DB: You'd need the information of who's allowed to look at it carried along with the stream.

AR: Yves had request for making certain web APIs usable from XR environments. Image recognition, QR code API, don't want to pass world data to everybody. Would be like a media astream. Deals in frames rather than bytes.

Adam: We are intersted to provide interoperability there.

KC: shape detection works on images; would need to apply frame to canvas, apply, next frame etc.

AR: So you'd like us to provide feedback in the TAG review? 

Adam: Provide feedback in whatwg/streams repo and we'll respond there.

Adam: WebSockets?

MS: Aren't they going to be redundant with streams?

Adam: No.

DKA: so what's on yoru mind about this?

: Backpressure. Gluing backpressure into the existing API is going to be ugly, so working to fix this is going to probably require a new API

SW: so this won't be about changing the protocol?

Adam: No, this will only be about the JS API surface.

MS: this will also help with developer adoption. It has been dissapointing becuase it didn't get the level of adoption we hoped it would.

AR: I blame GFE ;-)

KB: I read that the adoption was broad?

Adam: going up on smaller sites, but services like Google and FB haven't integrated it into their infrastructure

SW: I've been hearing complaints about use in transferring large amounts of data, e.g.

DKA: some interest.

KB: we see it used on 9% of pageloads.

Adam: used to see one message and done, but in recent years, seeing more usage for longer conversations

TL: vs. `fetch()`?

KB: fetch is 19%

*discussion of github use of websockets*

(the TAG thanks Adam for joining)

#### TOPIC: [Portals](https://github.com/w3ctag/design-reviews/issues/331)

*Kenji Baheux joins to present*

KB: context: TAG recommended packaging and something like "upgradeable iframes" in finding about Distributed and Syndicated content.

KB: look at the idea of upgrading iframes, but security team say "noooooope". Took a step back and looked at what we were really tryingto achieve. In 3D Games, you end up with texture maps; instead of re-parenting, you project. Don't know much about implementation details (team is in Waterloo CA), but that' the background.

KB: this deck is from Chrome Dev SUmmit, so might be slightly non-technical. The way you experience the web to day is like going throug ha bunch of slides. A sequence of single experiences. Sort of tedious. On mobile, you go from document to document. Even if it takes a few seceonds to navigate, not as seamless as mobile apps; particularly currated experiences. Every time you click on a link, you *feel* the overhead

KB: SPAs are a lot more work, and don't work cross-origin. With mobile devices, this is an even larger concern.

*Presentation of current vs. future experience; today's navigations show you a flash of white*

KB: for a long time, we've been trying to load things instantly. Back in Chrome 13, we did background preload, but for privacy reasons, could only pre-render stuff you've already been to. Very limited and practice and hard to maintain. Page didn't know it was doing a pre-render, so page had to adapt. THings like prompts for permissions aren't good, and so we bailed out in pre-render if any of those API s were called. Big footgun.

KB: that brings us to portals: like an iframe. A DOM element called `<portal src="...">`.

*demo shows how this works*

KB: transition can be pretty eamless, even across origins

DKA: can you show again?

KB: infinite list experiencew, and that site says "I'm pretty sure you're going to click on that", and so you load the article in a portal. You can place hero images relative to where you think they're going to be. At some point the parent document tells the child that it's now the active document (and URL is updated).

TL: tricky. Code on both sides.

SW: in this example, how many portal elements are being used?

KB: you can have as many portals as you like, but there's a tradeoff.

SW: twitter example: perhaps creating tons of portals.

KB: maybe something where you go to something deeper; maybe Reddit where you want to go to an article and come back.

AR: so the hero image transition isn't automated? Not handled by the browser?

KB: no, the destination page needs to coordinate with the original page; needs to provide position information, e.g.

KC: how does this solve the permissions problem? Another event?

KB: there are lifecycle events; "am I being pre-rendered, am I activated?". Plannign a way to restrict what portal prendering pages can do. All about privacy; want to avoid providing network information ahead of activation.

SW: how about nesting?

KB: team is pulling their hair on how to spec that. Should be possible (with iframes you can do it), but explaining that in a spec is hard.

TL: the HTML spec should have that explained somehow.

DKA: what are the abuse cases?

SW: maybe mistakes will be more common...inline twitter feed, opens portal to a site that opens another tweet

DKA: moer concerned with other abuse cases; phishing, etc.

AR: the destination page actually gets teh right security indicators

KB: right; you get the security indicators set

TL: I've been thinking about this as "right-click and open-in-new-tab". Same process. It'll do loading, but page visibility is set to hidden, etc.


AR: First, the use of a separate element is strange. Why not iframe?

KB: Any reason why it should be an iframe?

AR: We spent a lot of work defininig the behavior of a iframe, feature policy and a lot of work has already gone into it. This will have to be redefined which seems like a big risk and potentially a lot of extra work. I'd like to see this converge if possible as the proposal moves forward.

TO: Adding a portal mode to an iframe

KB: Not particularly attached to the naming or element.

AR: The intent is to transition to a different document. On the question of the privacy preserving bit, I hoped to remix the features of iframe sandbox and bundle packaging to be able to pre-load content from an origin. Especially in a way that the origin won't know that the user is interested in the content. The key moment here is that in this idea it seems like it is overly pre-emptive. The user state may not make sense, which could be problematic.

KB: On the note of using web packaging for this; it makes a lot of sense from a privacy perspective. What to do when you are activated.

KB: if yo uare able to run JS in the pre-render mode, you can set data on the client (in JS) to know "i've seen this"

AR: That depends on whether or not you are running in a sandbox -- a one-off origin or not. If you try access user state in a generated origin things won't work, so you'll have to require the user to reboot into a state-enabled mode. Right now the platform doesn't have this.

*discussion of preload case and privacy*

AR: if we think about this as an `<iframe>`, maybe it clarifies what's going on. The risk of remarketing/retargeting is pretty high (as a for-exmaple). How do we prevent the web from having that content follow you around after you just scrolled page Space News?

*discussion of same-origin/x-origin restrictions*

DB: what's actually different here between iframes and portals?

TO: if the list of differences is long, that's one thing. Would like to understand this in the context of if this should be a different element.

*Kenji shows MPA transition prototype*

KC: *outlines history state transitions*

AR: two big open questions: what are the actual differences between this and `iframe`, and what *exactly* does the transition do, specifically regarding state and storage?

AR: getting some outlines of those will help us get a handle on a review

TO: a-priori, a new element is "bad" for compatibility reasons. Tons of work in iframe restrictions already. It sounded like the reason for new element was that promotable iframes were hard?

KB: the idea was that falling back more easily would be possible.

*discusson of next steps for the review*

KB: regarding ITP, is pausing exeuction on access to storage reasonable?

AR: unsure. Maybe if it's fed out of a package, can mitigate network issues around privacy. Writing back to storage seems like the biggest issue.

*logistics*

TO: so I have a portal, soemthing inside of it...because the page in the portal doesnt have a reference to the parent...who calls `portal.activate()`?

*parent document*

TO: what happens if I interact with that content?

TL: could imagine that being inert...no interaction.

*parent has to activate*

KB: started with activation from the parent as simplest thing. Can add more

TO: doesn't the AMP usecase require the content to be active?

KB: yes. AMP carousel can activate on swipe transition.

AR: *lots of problems that get introduced with adoption*

KB: swipe would trigger multiple transitions of top-level document. Document that's driving should always be clear to the user.

### Ethical Web

DKA: the idea that technologists have an ethical obligation to the platforms they produce is an idea that's gaining ground. We have an obligation not to implement dystopia. Unfortunately, folks have been operationg under the assumption that they don't have any ethical responsibility. THis disconnect can create big problems. We're in an age when we're living through some of the problems caused by this disconnect at scale.

(shorter DKA: "people should take some damned responsbility")

*DKA outlines some background from TPAC*

DKA: Tantek suggestd that the TAG work on this, so I started writing a set of ethical technology questions that could appear on a questionnaire. Those are at the bottom of the document. Presented in Paris. Feedback was "that's potentially a good idea, but we should write down the principles first and derive the questions from that"

[DKA's Draft](https://docs.google.com/document/d/1tGQOFo-d849sagYDvgGzmSpPFDd_Nf47qb0FT6UjQKc/)

DKA: in my research, I started looking for the W3C's priority of constituents. It was only ever written up by AnneVK in '08 as an editor's draft.

MS: there is a non-normative doc, in the HTML Design Principles

DKA: can't be normative

MS: wasn't on REC track

DKA: we could perhaps put that into a finding. Outline some proposed non-optional peroperties (security, privacy, i18n, etc.)

DKA: balance of power between large, wealthy teams and and individual developers. Greenness (specifically, power consumption/efficiency). Inspectability -- e.g., from our EME review experience.

AR: web was bootstrapped on closed-source implementations of sometimes-open protocols. What does inspectability mean in this context?

DKA: view-source.

*discussion of testability of principles*

HB: these are things we tend to ask folks about in our spec reviews.

HB: something to clarify: inspectability should be for the user, not the network. Would be nice to have ammunition as we explain these things.

HB: second thing to add: right for user to render things however they like. I should be able to render the web the way I like it. You can accept that or deny me access, but if you serve content, it's under user control.

HB: to that end, I can imagine using them in reviews. Questionnaire is harder.

SM: I imagine myself filling out a questionnaire coming out of this, and I'm wondering "how much of this can I assess myself?". Lots of subjective bits. How can these points be made actionable? e.g. Accessibility should probably be a separate checklist.

DKA: that's something for the translation to the questionnaire to address. Like the Security & Privacy self-check. Mike has done a good job of translating wolly principles into a framework that you can check things against.

*discussion of applicability to specific specs*

YL: I can understand a11y, security, etc, but things like freedom of expression...that's very country-specific. Hard to test.

DKA: I link out to the UN Declaration of Human Rights.

*discussion of country-level blacklists*

YL: my point is that the TAG as a technical forum should focus on technical points. Maybe ask the AB?

DKA: I don't agree with that

*discussion of history around policy debates*

*DKA mounts pile of soap boxes*

DKA: no policy CG, no policy from the AB.	

*discussion of how to impact this*

MS: the Director has weighed in on this, feels the TAG can weigh in on policy, thinks you can't separate technology from policy.

MS: the TAG can decide how to spend it's time. Director's view doesn't define that. Other point: I support this in principle, but it's much more complicated...bad social effects are hard to anticipate. Came home to me in '16 with elections. Opinionated statement to describe these as disasters, but some of the things have happened that bad actors have abused systems we've spent 25 years creating. I don't want to be naive about negative effects of what we create, e.g. propaganda. THis happens with every powerful system we create. Can't blame those folks for not anticipating spam volumes and phishing.

MS: looking at Twitter, e.g....heavily abused, but not novel. Not unique to '08, per sae. Technology choices didn't define that. Messaging and design of the web didn't define that. Bad stuff is going to happen no matter how folks think about this.

HB: email is a good exaple. Tim's rant on this is that whenver folks who were designing SMTP were doing this work, they should have reached out otp olicy makers and noted the vulnerablity.

AR: is the counterfactual that development and rollout would have paused waiting for policy feedback?

HB: the idea would have more been a release note in the direction of policy makers

YL: billions of people weren't using it at the time

DKA: STRINT workshop was done to mitigate against network-as-active-participant attacks. Some folks in that room coming with attitude that it wasn't appropriate for technologists to weigh in. Govt should define how to apply things, and technologists should be hands-off. Weight of opinion wasn't on that side. Room believed that passive monitoring was an attack on the internet.

YL: more that privacy of communication is expected; e.g., physical mail. Reasonable expectations of privacy.

DKA: an example of an area where the TAG weighed in on a policy deicision backed by an ethical principle. Used that to make actionable technical decisions that tied back.

YL: in the Secure The Web finding, which was a technical finding

DKA: W3M pushed back, asked why TAG was weighing in on a policy issue

HB: agree that there's a role for these things, but I almost wonder if we'd be doing ourselves a disservice by describing them as ethical principles and not operational principles -- e.g. end-to-end principle; basis of the whole web. Fact that the web is transmitting tons of value means it must continue to work. These are functional requirements, not ethical.

YL: I think it's better if we do it the way we did Secure the Web...not framing it as policy.

DKA: not policy, ethical principles

HB: these are technical prinpciples. Saying "ethical" sounds buzzwordy. It's about making a web that actually works.

AR: Level of debate ... if we're going to wade into ethics, it's a deep discipline with a lot of expertise.  Ethics of science has a set of experts -- we could consult them.  Having discussion without that background seems like time we could use better on other things.  Atomic weapons experience maybe not dissimilar in terms of societal discord.

DKA: I don't think bringing in set of experts should be an academic exercise.  

AR: If you'd like to make this something people can do something about, it may be help to describe these as responsibilites rather than principles.  You seem to be flagging that people making technology don't feel they have particular repsonsibilities.  Lots of ways societies give people reponsibilities.  Doesn't seem like there are easy answers here; seems like this group should seek guidance if it's going to continue doing this.

DKA: IN Paris, came witha questionnaire, you asked me to restate it as princples.  Seems like an argument for not doing anything.  I want to get to where we can do something.

AR: We haven't recounted things we haven't done before.  Securing the web finding helped to support work that was happening.

DKA: We're not the only people talking about tech ethics.

AR: I think it's worth looking at what effect our participation in that dimension has had.  Was it effective?  What's the most effective way to engage?  ...  I'd like to attack this with the longer arc of technology ethics in mind.  I'd like us to spend time on it in a way that has more grounding.

DKA: I don't want us to spin our wheels on it.  Even something analogous to the security & privacy self-check, even if it only covers subset of topics we put in.

MS: I agree with something Alex said -- maybe time to get some outside expertise.  More it's discussed, maybe not just the TAG on its own but the W3C organizationally, including the AB.  I think the AB has decided it doesn't want to do something.

DKA: the AB has decided that it didn't want to do anything on *policy*

MS: "policy" is a bit of a red flag. "Principles", ala "design princples" seems like a good thing

DKA: can agree that "policy" might be bad, using "ethics" might be a good signal to that the W3C is thinking about this

AR: to who?

DKA: the technology industry

HB: Could do a document on responsibilities with a covering blog post that ties it to ethics.

*group hug*
(JK, punchy scribe)

MS: https://tools.ietf.org/html/rfc1087

MS: we know the IAB well, we could discuss with them as we know them well. If it's not in scope for the IAB, maybe their scope should change too.

*discussion of RFC 1087*

DKA: I was thinking of RFC 7258: https://tools.ietf.org/html/rfc7258

DKA: you can link 7258 directly back 1087. 

DKA: a couple next steps:
 - socializing ideas with W3M
 - discuss with AB at their next face-to-face
 - bring in external expertise in tech ethics

#### Weekly Teleconf timing

DKA: We've previously had a rotating schedule, but this has worked poorly as people have routines.

DB: We need to adjust for summer time changes anyway.

*hilarity*

DB: Things shift a bit between summer and winter time. Also, some timezones might stop doing a time change over summer - but probably not this year.

DB: We have three intervals to think about - AU, US, EU in summer times which nest into one another.

DB: Look at a globe, fit the sleep onto the globe such that it doesn't overlap with the callers.

DB: The sleep window is either between Japan and Europe, or Europe and the west coast of the US.

DB: I proposed keeping that sleep where there is an 8 hour time gap, because that will push people the least.

DB: The time for northern hemisphere summer (July half of the year) with an 8h time gap looks something like this:

DB: 6:00 UK / 7:00 France / 14:00 Tokyo / 15:00 Sydney / 22:00 California

*cameo by a tired Andrew Betts*

DB: If we wanted to put the sleep gap in the oother place in the summer, that'd be 6am Tokyo, 11pm France (start time).

AL: It's better than early in the morning for me.

DKA: I really struggle in the evening. Early morning is much more manageable.

AL: It takes time for me to wake up enough to process a second language.

*Slack paste below*

So regarding teleconference times:  Right now, we have two time slots that are reasonably viable:  roughly 21:00 UTC (which we just used, 06:00 Tokyo / 08:00 Sydney / 13:00 California / 21:00 UK / 22:00 France) or roughly 06:00 UTC (6:00 UK / 7:00 France / 15:00 Tokyo / 17:00 Sydney / 22:00 California).

21:00 UTC becomes much less viable in northern summer because France and Japan get an hour closer together (requiring either 05:00 Tokyo or 23:00 France), whereas 05:00 UTC is fine in northern summer (6:00 UK / 7:00 France / 14:00 Tokyo / 15:00 Sydney / 22:00 California).  (Or 16:00 Sydney for the small number of weeks when both Europe and Australia are on summer time.)

In the transition period when the US is on summer time and Europe is not, however, the 06:00/05:00 UTC variant (which works in both northern summer and northern winter) *doesn't* work because Europe and the US are an hour closer together, and we want the 21:00 UTC time (06:00 Tokyo, 08:00 Sydney, 14:00 California, 21:00 UK, 22:00 France).

Or, to put it another way, I think it's the European summer time transition that's most critical with the current set of participants.

(Note that it's convenient that the date range of Australia on winter time is a subrange of Europe on summer time, which is in turn a subrange of US on summer time.)

That said, a bunch of people may have time constraints that aren't sleep related that we need to consider as well...So I guess my strawman teleconference time proposal is that we use 21:00 UTC when Europe is not on summer time, and 05:00 UTC when Europe is on summer time


21:00 UTC, January half

0600 Sangwhan
0800 Alice
1300 David, Tess, Peter
2100 Dan, Hadley
2200 Kenneth, Yves, Lukasz

06:00 UTC, January half (second option)

1500 Sangwhan
1700 Alice
2200 David, Tess, Peter
0600 Dan, Hadley
0700 Yenneth, Yves, Lukasz

05:00 UTC, July half

1400 Sangwhan
1500 (sometimes 1600) Alice
2200 David, Tess, Peter
0600 Dan, Hadley
0700 Kenneth, Yves, Lukasz

TO'C: 10pm is very problematic for me - I could listen, but would have to speak very quietly.

SM: 6am is similar for me.

DKA: Is there another option which flips Tess and Sanwhan?

DB: Will stick with current schedule (21:00 UTC) until the Europe summer time change, then switch to 05:00 UTC.

### F2F planning

DKA: Thinking of swapping London for Reykjavik

... visa issues? ...

SM: Accommodation is fairly expensive in London

PL: Bletchley? Milton Keynes?

TO'C: I could enquire about hosting in Cork.

DKA: Paris again?

KC: Sweden?

DKA: Berlin? Let's zero in on Berlin.

TO'C: Good for pulling Anne in as well.

DKA: Ok, next F2F after thatt is 10-12 September (pre-TPAC), probably in Tokyo again.

DKA: Tuesday-Thursday again, Friday off, then TPAC the next week.

TO'C: May or may not be able to host.

AR: Google office isn't going anywhere...

SM: Also the university.

DKA: Yves, can you check with W3C staff if we can host at ...?

YL: I can check.

TO'C: The week before they may be stressed about TPAC.

DKA: If we've got September, we need to think about where we do the next meeting and when. December?

DB: When is thanksgiving holiday? Late or early this year?

PL: Nov 28.

DKA: Let's look at 3rd-5th December.

TO'C: Cupertino should be possible.

DB: December 1st will be the busiest travel day of the year in the US.

TO'C: What about the week after?

HB: Bit too close to holiday time.

DB: Probably ok if you have a direct international flight into SF.

DB: Hotels are expensive in the Bay Area.

DKA: Tentatively let's say 3-5 December in Cupertino.

AB: Google can host again in Tokyo in September.

DKA: Well the lunch is pretty convenient... ok.

AB: Ok, I will plan on hosting in September.


### Security and Privacy self-check

DKA: is there soemthing you can give us to do tomorrow durring the F2F tomorrow before you join to help progress the self-check document?

Lukasz: we believe we're almost finished. There may be a need to get a holistic review...

DKA: so we can review something?

Lukasz: not sure if it's finished or not. Met last week to discuss. If you want to review you can. Most of the content is already there.

*discussion of logistics*

DKA: can you send us on slack the version you'd like us to review?

LO: yes.

https://w3ctag.github.io/security-questionnaire/

LO: I think we've done it all excpet an overall review

DKA: from Paris there was some specific feedback...

LO: I forwarded taht to Jason and took that into account. We also took into account the idea of writing the document as a way to gather feedback. We may also want something smaller on the side. I believe this document should be standalone, and perhaps we can just extract the questionnaire if we want a shorter document.

LO: there's also a "privacy mode" document, have you looked at it?

DKA: no

*logistics*

*discussion of private browsing modes doc; reading to review*


DKA: Background for this doc - spec authors were adding things to their specs about private browsing mode, e.g. web payments, but there was no definition in any document about what private browsing mode meant.

DKA: in every browser, tehre's a private browsing mode feature. They tend to operate differently. That's one of the reasons I zeroed in on that particular statement. In the security and privacy self-check, there are some statements prompting folks to consider how things work in tehse modes.

TO: this line "encourage folks to make web features work differently" is stronger than I'd like to get to. Perhaps it should be "please think about how this works in these modes". I'd like our finding to encourage folks to be thinkging about this.

DB: there's some contradiction. There's a statement that some things should behave differently in private browsing mode, and another that says "things should work the same in private browsing mode". I thin tkey could be put together in a combined statement that isn't contradictoory by saying "yes, some things will work diffrently in private browsing mode, but should be done in a way that's not detectable". E.g., storage, where you don't want things stored beyond the duration of the session.

AR: sort of a meta point, but the finding isn't going to define private browsing modes, and we probably want something that goes into the design principles that's actionable

HB: I put out some research on this last year

(which AR had blanked on)

HB: could be more complete, but welcome additions

*discussion of document format choice*

TO: this goal of this document was to solve the reference problem...right?

