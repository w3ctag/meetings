## W3C Technical Architecture Group face-to-face
### - DRAFT -
### April 22 2015

### Contents

* General public policy advice from the TAG
* Storage
* Future of the future of the TAG
* Powerful Features, Security & Privacy review process
* Priviledged Contexts (née: powerful features)
* Packaging!
* Web Performance 
* HTTP to HTTPS

[#tagmem IRC Log from this day](http://www.w3.org/2015/04/22-tagmem-irc)  
[Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/04-sfo/agenda.md)

*Present:* Daniel Appelquist, Hadley Beeman, Tim Berners-Lee, Yves Lafon, Travis Leithead,  Peter Linss, Mark Nottingham, Alex Russell, Yan Zhu

*Special Guests:* Mike Smith, Tantek Çelik, Nick Doty, Mike West, Ilya Grigorik

*Chairs:* Dan Appelquist, Peter Linss

*Scribes:* Travis Leithead, Yan Zhu

### General public policy advice from the TAG

mnot: We should publish docs that talk about how the web works and how certain legislation might contradict that direction  
… and fostering direct interaction and a resource for policy makers

Related link: [publishing & linking draft](http://www.w3.org/TR/publishing-linking/), which was intended in some way as a response to some  

dka: context: were discussing "linking" and its affect on copyright infringement.  
… part of the idea for the doc was to establish common terminology.  
… perhaps we should review/revisit some of that terminology  
… web vs. traditional publishing  

mnot: we need to careful tailor the language to our audience.

dka: we created a glossary of terms for understanding and with explanation  
… "embedding" vs. "copying"

hadley: very useful for the press too.  

dka: there was some pushback: "hey, you're not lawers and are weighing on a subject you're not part of"... (original request was for an "amicus brief")

timbl: we stopped short of saying "you *should* do this"  
… if you're just linking to legal content, you should be safe.

Spam: the great inbox-filler

timbl: folks get major benefit by contributing to the common open relay (smtp); if I get a message I should read it.  
… it was successful.  
… If the explosion of spam were anticipated, policy could have been created to regulate what mail was acceptable to contributed into the network.  
… There is human duplicity in the system which leads to things like PGP...  
… however over the years SMTP is still the same  

mnot: DKIM, spf, etc. were also specified

timbl: every single protocol we create has a social aspect.  
… Google works because people have created links from their sites, because they find value in those links, and because sharing that information in ingrained in them.  
… We must be aware of these implicit social assumptions present around a protocol.  
… Sometimes we should say what the implications are for breaking the social contract around the protocol.  
… as in TCP, you can cheat the exponential backoff. There are implications for subverting the system.  

mnot: I'm comfortable explaining the technical details and interactions between various mechanisms  
… we can describe: if you take advantage of these things, here's what happens.  

timbl: that's what the TAG should do (should have done) since the beginning.

hadley: government's power is in regulating behavior; W3C'sp ower is in building things.  
… when we see spam/captive portals, we can consider building something else.  
… we usually don't take a stand on the behavioral issue: e.g., "you should not send spam"  
… do folks agree?

mnot: folks establish metaphors for understanding various systems, then governments establish laws and regs based on those metaphores...  
… but these metaphors can break down.

timbl: the distinction is what I'm pushing back against  
… Separate social pieces and technical piece. When considered together, they work together because both constituent systems are designed together.  
… These things are coupled (say a "microscopic relationship--two people exchanging an email)  
… Then you couple these microscopic interactions together and you have "facebook" and "twitter"  
… This leads to more complex issues when in turn geminates new ideas which results in social+technical issues (it's a closed-loop cycle)  
… So... when we create new tech, we should also state the social expectations that are considered in the design  
… So, government policy makers create an arc from "issue" to "social", while TAG creates new tech (and the cycle continues)  

dka: considering geoloc as we discussed at ExWebSummit.  
… the geoloc technology has circled around the loop once, so that now we're once again considering the issues with the original development.

alex: What did we improve with geoloc?  

dka: Uh.. not sure we have. My point is that the model is a frame of reference for understanding the model that tim described.

hadley: that's important context, thanks.  
… it's helping me shape my thoughts on social networking.  
… such things like distribution of child porn, while a polarizing topic, has some social aspects.

dka: so... obviously it would not be appropriate for the TAG to take a stand on gambling (example). I think it is appropriate to say: the web is a tool for free speech.

yves: "free speech" is not accepted in all countries

timbl: there are lots of other folks talking the social/moral issues.  
… if considering captive portals, and you brand the issue as a human rights topic, then it may not be accepted everywhere.

timbl: If you say: don't inject JS advertising into the page at the captive portal because it's a social statement, I say perhaps we should say that.

hadley: that sounds "functional" not a social statement...

timbl: we're bikeshedding.
… another example, if you talk JSON and say it must translate to RDF, then that's clearly technical...  

alex: If you bring the social/political assumptions to the room then we have a clear ability to make progress. When folks in the interaction don't share the same assumptions, then it's not so easy...

timbl: maybe we shouldn't be so concerned about splitting hairs here, since the social+technical are so intertwined.

alex: I'm concerned about our effecitiveness if we start down advising the social issues, then it might detract from our cred to make technical progress

alex: We should adopt a principle of "conservation of effectiveness"

hadley: +1

dka: I want to frame this a bit more  
… we're talking about how to frame social/policy advice from the TAG  
… we had:
- subversion of intended function
- fit for use
- break of trust (this and the above point are characterized by the "securing the web" finding)
- bringing tech clarity to policy debate (publishing and linking)
- positive reinforcement to policies "we like" (e.g., the white house proposal)
- what breaks the web (the web's "social contract")
- encouraging public discourse and transparency

dka: any other frames for policy statements? Yan?

yan: I think a lot of what EFF does is not appropriate for the TAG unless we adopt some kind of free speech policy...  
… not sure how much of EFF applies

timbl: can you say: "hey, you shouldn't inject javascript"

travis: not sure you can just say that as-is. Need to add context.

timbl: it would belong to a "play book" with the scenario defined. You can say that this and that is not appropriate.  
… there's the social argument; to say: hey, you're cheating, that shouldn't be allowed.

hadley: yes, agree, and you're breaking the web... but...  
… we've setup lots of expectations with the web architecture, whey they put in and what they get out.  
… some things mess with that, js injection, pervasive monitoring  
… for us (TAG) to say: those things are not part of the expected usage of the system.  
… the other arguments sound like human-rights arguments.

dka: should we then pursue a document "js injection is considered harmful"

alex: Who's the audience?  
.. If there was a group that would benefit from it, then OK.

timbl: example of wanting to expand the internet in Africa by using injected ads. Would we be OK saying, no, that not an appropriate business model.

alex: I personally agree... just want an answer to who's the customer?

timbl: I think the customers are ISPs and software companies...  
… we don't have to talk about "human rights", but perhaps "social contract" is OK.

dka: any other policy debates that we could potentially add to our [above] list?

mnot: What forms will these deliverables have? "Finding", "blog post"  
… Social networking, net neutrality, metadata (which is just data :-)  
(brief refresher on order of formality: Tweet < Blog < Finding < REC).

### Storage

Different Storage Technologies in web standards:
* cookies - simple strings + expiration date
* local storage - string/value pairs (strings only?), persistent
* session storage - string/value pairs, temporary
* indexed db - transaction-based (thread-safe) key/object pairs
* web sql - (obsolete? yet folks still asking for it at #extwebsummit)
* File system API
* Caching API (fetch) [Cache objects (from Service Workers spec)](https://github.com/slightlyoff/ServiceWorker/blob/master/explainer.md#the-cache)
* HTTP Caching - no API :(

[FYI, Mozilla Device Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Device\_Storage\_API) (non-standard, only for privileged apps)
[Minutes from Extensible Web Summit sesssion on storage](https://pad.w3ctag.org/p/EWS-20April2015-Breakout1.1.md)
[An early Durable Storage proposal](https://github.com/slightlyoff/StorageDurability/blob/master/explainer.md)
[AnneVK’s concrete proposal for unified architecture for storage on the web](https://wiki.whatwg.org/wiki/Storage)
[navigator.connect API proposal](http://mkruisselbrink.github.io/navigator-connect/)
[navigator.connect explainer](https://github.com/mkruisselbrink/navigator-connect/blob/gh-pages/explainer.md)

Alex: There are many storage systems in browsers, with various guarantees.  I can give the lay of the land, and then we can talk about the architectural concerns? Question about what user agents are going to do, which is what prompted this.  
…Those storage technologies (list above) have some nice properties: they are origin-bound. The storage used by origins is attributable, from the user's perspective. Challenges on the semantics of them.  IndexDB tries not to have locking between threads; local storage and session storage weren't so lucky.  
… This gives rise to the crazy behaviour where reading from IndexDB looks slow. Local storage looks fast or slow.

TimBL: can an app find out what it's waiting for?

Alex: No.

TimBL: Thinking of the XKCD cartoon where it looks like it's locked up, but it's opened another modal window behind the screen.  
…If you're waiting for another application that happens to run on the same origin.... could be any of the same LibreOffice suite, or Office 365 — your spreadsheet could be waiting for your calendar or whatever.

Travis: Browsers have this assumption that storage is boxed into an origin. Origin is a representation of an app or a suite of apps, but is restrictive about granting storage to other origins. In non-sandboxed, you have a storage layer that is common to all applications.  My question: Is that view of origin-tied storage — do we want to explore sharing storage, to allow it to be more of a substrate than it is today?  There are use cases, but... security?

TimBL: Totally. For example, in cloud storage, — what about interoperability of data formats?  Eg: .ODT file.  I want to share with other people (access control), but also, ' I want to say this can go to LibreOffice'.

Travis: Thinking about XHR and now Fetch... people want to grab that content from different origins, so we created Cross Origin Resource Sharing (CORS). I as the creator of the content might put that same intent on my storage block, "this is shareable, readable by anybody."

TimBL: in read-write linked data apps, people are fed up with CORS getting in the way. So, rule is: just put that stupid CORS header on it.  Use HTTP (or HTTPS) consistently throughout.

Yan: I see why that's useful if you want everyone to access your data, but security people freak out when they see that.  If your website is a bank, and you see a wildcard CORS header, it's probably really bad.

Tim: If I have my data somewhere on the Web, and I want a cool web service to use it — like Mint — which i trust... but my bank hasn't said they approve it.  I'm never going to think of the list of all the apps I want to use this.  Then I have to turn CORS off.

Yan: In your model, the user has to make the decision of "I trust mint.com with my data."  In the CORS model, the bank says "Yes, I trust mint.com".

Travis; Or they give you your data in a portable format to send to mint.

Tim: Yes, but that's not sharing.  That's downloading.

DKA: This is theoretical though, but in the real world — if I go to TurboTax and ask it to get my data from eTrade, it can do that because i give it my eTrade password.

Yan: I think it would be more wrong for eTrade to allow access through CORS.  In that case the user has no idea that a malicious party might have access to their data.

Tim: So what should happen is that the user shoudl authenticate to both services.  Delegate access.

Travis: In that case, every piece of data should have an access policy, integrated.

DKA: back to the initial discussion. Perhaps a separate discussion about problems with CORS?  But here, let's talk about using the CORS model to let some piece of local storage be accessed by different applications.  
…If you have two web apps in the service worker world, that are executing locally on your device, and you wnat them both to access data on your device and you're not online, then you're screwed.  We don't enable that.  
… Example:  A photo retouching application as a web app.  I want it to access photos in a photo storage app (which is a web app).  
… On mobile OSes, a dialog box asks you for permission.  Is there something similar we ned to do for local storage to make this work?

Travis: That prompt in an installed app? Then the API isn't one of ours; it's at the OS level.

DKA: I'm thinking about the user model.  Has this been discussed?  Alex?

Alex: It's hard for me to unpack all the roles I'm playing here.  What's likely to happen, and what's reasonable, and what the opportunities are:

* It's likely we'll struggle with the storage mechanisms we have right now, because they're not integrated. Re the locking problem: IndexDB has a similar problem. The Cache API has to preserve opacity for non-CORS cross-origin content. 
* It's attributed to your origin storage.  You can set whatever mode for the Fetch that you would like (CORS, no CORS). You'll receive a different type in return: a regular response, or an opaque response (which doesn't allow you to see hte content).

Tim: I have an outstanding issue on the Fetch spec. The credentials flag.  Will we get rid of that?

Alex: Not sure.

Tim: Good issue for the TAG. With the credentials flag is a different space, produces different results. If you mistakently set/don't set it, you can't go back.

Alex: Dont' have an easy answer for that.  
… We have two classes of content: the image element and the CSS link rel system and sciptSource= allow you to fetch and execute third party content without CORS, and without being able to see the content.  
… You can't read back the pixels from a third party image fetched with CORS.  
… It is a little incoherent. How do we get to a place where applications can collaborate re their storage. One option: allow apps to install services that other apps can consult. 

Travis: vs allowing them to have direct access.

Alex: Both are available.

Tim: If one option to the data is ID reference and the other is a fetch to a service on the machine, and get back the data, parse it, and instatiate it — the first option is preferable (when I'm writing code)

DKA: Are you suggesting this is an elaboration to service worker?

Alex: Yes, and there are proposals out.  You can do most of this with appcache and iframes. But that doesn't work from workers, which can't talk to documents they haven't created or create new sub-documents.  
… There are interesting protocol-level considerations... does this happen transparently when you make a fetch? Explicitly when you call out over an RPC? Who owns that data? Can we preserve the opacity of an opaque response? postmessage doesn't have an opaque object type.  
… Another option would be a shared storage pool. Assuming you had  asynchronous APIs only.  

Travis: Simplest solution: I write something to a shared file system, with a given key (hard for anyone else to randomly discover), and then I give you that key and you can read that file.  
…And you can put that into local storage.

DKA: Running out of time for this discussion.  Any proposals on the table in Web Apps or Web Apps Sec to deal with this? Could we prompt a discussion?

Tim: LDP group are looking at access control.  Adding in origins as priniciples is interesting. If somebody is accesing something using a script from a different place, you have to trust both.

Travis: There's a security prinipcle for granting cross-origin scriptability between frames: both domains have to say "I'm willing to cooperate." There's no concept of user.

Yan: My concern is that persistent storage to be very sensitive — I'm one of them. I block third party storage in all of my browsers, local storage and cookies. Tor will clear everything after each session. Needs to require user consent for cross-origin local storage sharing.

DKA: Part of my mental model: FirefoxOS, where the Web environment is the OS, you need local storage.

Mike: Alex, when you were talking about cache, you meant objects from service worker?

Alex: Yes. They happen as a side effect of the service worker design. In next release of Chrome, we're making cached objects available as well.  
… How do we deal with storage locking? Now, IndexDB has a nasty way of daling with this: it closes transactions at the end of the task.  You could extend the life of the transaction (artificially), — but it's there to keep developers from getting themselves into an inconsistent state.  
… This goes badly with other apps wanting access to the storage and trying to coordinate about the transaction lifetime.

Travis: Transaction closes when there are no more pending events on the transaction.  
… There shouldn't be any race conditions... The design was to avoid introducing a javascript locking primitive.

Alex: But now, It isn't possible to coordinate your rights to a cached storage area with a indexDB transaction.  We're clearly missing a locking system.

Travis: Such a mechanism could be safe, same properties that indexdb guarantees, but less complexities.

Alex: Upside: Indexdb could provide an extended lifetime for transactions without extra I/O.  
… For the cache API, allowing transactional behaviour that isn't implicit or underspecified.  
… Jonas Proposed ordered locks: if you guarantee the order of your locks, you can take them out and use them to coordinate with other storage features and avoid bad patterns today (using I/O to extend transaction lifetimes)  
… Clearly, we haven't fixed this yet.  Needs to be done.

### Future of the future of the TAG

To include: 

* Composition of the TAG
  * AB proposal to expand the TAG. (Chaals) expand to 13 members - https://lists.w3.org/Archives/Public/public-w3process/2015Mar/0029.html
* Additional roles that we may/may not want the TAG to take in W3C Process:
  * (Mark) charter reviews, 
  * creation of WGs, 

Mark: Once we had the problem of Alex leaving the TAG because Dominic was hired by Google (and we couldn't have two Google employees)

DKA: This was the second time I've seen this.

Tim:  This is separate rule to the number of people in the TAG.

Mark: This was discussed in the process group, the AC and the AB. Lots of proposals.  Most reasonable: if there's a change of employment, those people can serve out their terms but to be rebalanced at next elections.  
… Others said limits re company representation weren't reasonable.  
… In that, Chaals as one of the chairs proposed that we change the rules as above — AND expand the TAG to 13 people. To me, that second bit seemd out of left field.  
… If you grow a body like this too large, it can become unweidly.  

Yves: it can expand by creating task forces. We did this with HTML.  
… There is no need to expand the size of the TAG to an abritrary number.

Peter: Chaals wasn't proposing loosening the restriction to TAG members per company.  He's in favour of keeping that.

Mark: Several other AC reps, including David Singer, were concerned about expanding the size of the TAG.  
… Also, the TAG didn't ask for that. Maybe we should ask the TAG  
… The TAG has a roving focus/purview of work, but we don't have a role in the process with specific responsiblity (beyond advising the Director).   
… If we have more, then I can see the case for expanding.  

Alex: I'm more concerned the rules create disruption in the TAG (having people leave, special elections)

DKA: Agreed.  
… We have a hard enough time finding good people for the TAG; this can turn them off.

Mark: I think this will be fixed: everyone knows this is a problem.  There are lots of people who want to remove the limitations on employee representation.

DKA:  If we can get it to not trigger a special election — then I think it's better.

DKA: Should the TAG play a formal role in chartering new working groups?  No one has asked us to.

Tim: What would be our goal in doing that?

Mark: Speaking as an AC rep: I'm concerned that chartering happens with lots of control to the W3C; opaque to the membership.  Others have remarked that they expect the TAG to have input on that.  That seems odd.  
… I come from an IETF background; the people making those decisions are technical and have a view on the architecture.

DKA: This is when charters are initially crafted, before they get to the AC?

Mark: Yes.

Tim: I'd like to point out that W3C staff ARE technical people.

Mark: Yes — some W3C team are.

DKA: Not sure this is relevant. Even if we posit (as I believe) the people buildling these charters are appropriately technical

Tim: And they don't just do it in a vacuum!

Alex: to Mark: If the problem is the AC having issues with the W3C staff, is that our issue?

Tim: Why should the TAG be involved?  To what view/activity?  To have an opinion about the technical architecture?   
… Also need to know who will be in the working group; does the membership want it? The staff know these things, and the TAG won't.

Mark:  Yes — so run new charters through the TAG.

Tim: Another process: the headlights

Mark: and the workshop process.

Tim: Perhasp we should have the TAG in the headlights process of new things we ought to be working on and haven't thought of yet.

Mark: yes. I don't want to take the team out of the equation, or 

Peter: I don't think the TAG should be affected by concerns of who may be a new member

Alex: My concern is that, should the TAG be asked to contribute in areas where we don't have much expertise, that may impact our work in other areas.  
… What is the situation in which we can provide valuable feedback that wouldn't be caught in any other way?  
… As we discussed in the proposed HTML process yesterday, there are moments when we could be involved.  

Mark: This is hard because we have a dual process now.

DKA: Mark, do you mean: When I talk about the TAG having a role in chartering, I mean before the AC sees the charter.

Mark: Yes

DKA: I like the idea of the TAG playing a greater role in workshops.  I don't see much of the headlights process — but we have taken a role in informing the team.

Tim: We used to have the Noah Mendelson/Jeff Jaffe interview.

DKA: We had that recently, Jeff joined our meeting.  We tried to have that discussion — a CTO-to-CEO conversation.  
… Re workshops: if TAG wants to play a role, I don't think we need change in W3C process.

Mark: Just a notification?  Some of us get them as AC reps.

DKA: It'd be useful to have as a standing agenda item: what's coming, and what do we want to prompt. 

Hadley: And to make sure the right topic connections are made, cfps end up in right hands.

Tim: It does go out to chairs, etc.

DKA: So: earlier in the process. Before cfp.

Peter: Sometimes we've spawned new working groups.

Tim: Can you think of a time when that HASN'T happened?

Peter: Not right now.

Tim:  Guess it's also the staff contact's responsibility.

Mike: Offering a viewpoint as someone who has written a number of charters... I'd welcome TAG feedback. Never been a possibility before. I don't see anything in the process that would prevent me from doing it.  I will bring the next charter to the TAG.

DKA: The process generally is that this doc is shared around between a select group of people (previous chairs, a few interested parties, influential companies who are interested) — not that that's bad — and then at some point it's shoved out into the light for comment.  Mike, I think you're talking about including the TAG in that closed group for comment?

Mike: Yes

DKA: Issue there is that the TAG is doing much of its work in public.  
… We have to decide if that's going against this, on our private mailing list, or...?

Mike: If we need people to talk freely, then the member list is good for that. For this, we'd need a TAG-only mailing list for "TAG team"

Tim: I'm wary.  For those of you who've drawn up charters, how important is that quiet early on?

Mike: From my experience — I'd be fine with it. But I'm not sure the other team members would agree.

Tim: Some charters come from Committees.  

Mike: The process of making things public has made things better.

Hadley: Counter example though: When we were chartering Data on the Web, there was a lot interest in the open data community in having a broader, championing group for open data. (Almost an interest group) If we'd overly democratised the early chartering process, we would have ended up with a talking shop with no clear deliverables.

Alex: Sounds like that wouldn't have been ideal for a working group.

Hadley: Exactly.

Mike:  Expert review of the work early on — that's why I would want to do it.  Like the AC, but another level.

DKA: the meta-issue: the TAG is an elected body that has a mandate: to guide the technical areas of the W3C.  Chartering, headlights and workshops guide the W3C.

Mark: If this is couched in obligations, then we have an opportunity cost. But if just's a trigger to notify us, then at least we have the information.

DKA: to put into the checklist that the Director asks when a new charter is coming up for a vote: "Has the TAG seen it?"

Tim:  Assign a person on the TAG to lead that review, or try to go along to the workshop?

DKA: Yes, as long as the review/input is coming from the TAG as a whole.

Tim: We shouldn't have an obligation to reply to every charter.  If we can't find anything worrying, contentious, exciting — 

Mark: one word review: Ok.

-------  LUNCH -------

### Powerful Features, Security & Privacy review process

… with special guests Tantek, Nick Doty, and Mike West.

[Tantek's blog post on security](http://tantek.com/2015/068/b1/security-towards-minimum-viable-web-platform)  
[Mike West's security review questionaire](https://mikewest.github.io/spec-questionnaire/security-privacy/)  

Tantek: yan and I had a conversation about the complexity of W3C specs. The particular concern is the expanding size of the security surface. It seems to be spiralling out of control. I posted questions on twitter that started a conversation. Mike proposed a way to think about evaluating specs.

Tantek: There are 2 ways to think about it; one is how to [....] and another is how to reduce the number of features in a particular spec. If the only reason to minimize is to reduce the security surface area, then I assert that's good enough. The motivation is that the Web should be more secure than any "native" app platform.

Alex: it already is

[document presented]

Tantek: the question of course is how you determine minimum viability. I've asked more questions than I've got answers. I think it applies to any spec in any form.

DKA: mike, anything to add?

mkwst: I see two distinct topics: the first is what should we be specifying. The second is, once specified, how do we evaluate these things...particularly as we need to help designers who might not be experts in privacy/security.

mkwst: I put together a very straw-man document with many broad questions. The intent of the questions is to help focus spec authors on things that they might not be expecting. I tried to lay out important areas (passive/active network attackers, same origin violations, etc.). The document isn't finished yet, but the goal is to have a reasonable explanation about what the questions are meant to address.

mkwst: at the bottom, there's a discussion of general mitigation strategies. This has some overlap with secure origins/etc. Another strategy is to ask the user, and this is difficult. Many prompts are hard to do and @__apf__ has been looking hard at this. The last way of approaching these features is to perhaps drop a feature to reduce the risk. 

mkwst: I'm not sure that these topics go together, though. Minimum viability might be different than trying to decide what to build.

Tantek: I'm not sure...I think there's a feedback loop here.

mkwst: one example of an aspect here might be a11y...if you can't make a feature accessible, maybe you should cut it. It isn't clear to me that a document focusing on either security/privacy should be talking about broader, cross-cutting concepts.

mkwst: nick has gone through an earlier version of the questionaire

ndoty: many people aren't sure about what the basic security properties of the web really are. Frequently refer to common assumptions and not a single document that actually defines what things we need to satisfy for every new feature.

ndoty: we have an architecture of the www...do we have a security architecture of the web?

timbl: particularly the SOP?

ndoty: this is the one that comes up most frequently

DKA: this has come up before, gets stalled, but unsure why

timbl: if you had a document that explained the benefit and didn't just waffle, that might be good

travis: there's a draft doc that outlines the same origin policy?

ndoty: there's abarth's origin concept document (RFC6454).

[Principles of the Same-Origin Policy](https://tools.ietf.org/html/rfc6454#section-3) from RFC 6454, “The Web Origin Concept”

travis: that's one, but it wasn't what I heard requested. We wanted the larger picture, right?

timbl: the SOP has lots of implications and side effects...and we have the PKI system...if you wanted to document the security architecture of the WWW, would you do a series of documents, or connect them together?

ndoty: we shouldn't stop doing reviews until we have a more general document. But it'd help to have that documentation about the architecture.

DKA: we've heard a request for that before, but it shouldn't be blocking.

DKA: what's the role of the TAG in this checklist doc? Is the idea that this can be part of the TAG review process?

yan: I believe that this was intented as a self-review questionaire. Tantek and i think it would be good to give this some weight. 

DKA: in the work we do, we should add a review of this document to our list so we can suggest additional content

mnot: what's the intended venue?

mkwst: don't care. Could be webappsec as a Note. Talked to privacy. Have shopped it around but the conversation hasn't gone beyond interest. If there's appetite to post it as a TAG doc, that'd be great. The important thing is that it has visiblity.

hbeeman: do you think this needs to be an official part of the W3C process?

mkwst: the value would be visibility. Don't think it needs to be an official part of the process, but might potentially be useful to have it as part of the process. The TAG review process could ask "have security and privacy been considered?", if not, could point to this doc.

Tantek: dissagree with mike, I think this is as important as all the other reviews we require.

mkwst: it's frequently the case that specs only get security review at implementation time. Security teams are frequently coming up with things that just weren't considered in the design process. Would be better to be giving feedback earlier in the process.

Tantek: we run into the same things at Mozilla. Our I2I process suggests a security review.

[Mozilla's Intent to Implement process](https://wiki.mozilla.org/WebAPI/ExposureGuidelines#Intent\_to\_Implement)

ndoty: we've had various places where people can look. It would be good to have a way to say "yes, this is important and here's how to think about it".

Tantek: a straw man: require this for CR entry?

timbl: every time you make another explicit step required, it's a risk. It's good to document what we learned from the previous attempts, but we should be careful about bureaucracy. It's easy to write process documents that make life hard for other people.

timbl: we want them to not be immigration/tax-style questions

hbeeman: making it mandatory creates an implied commitment to keep the questionaire up-to-date?

travis: you could also turn this into a walk-through thing.

ndoty: the IETF did a security-considerations thing...mandatory

timbl: many were sarcastic

ndoty: many were one line

mnot: it's pro-forma now, but there's a process you go through

ndoty: we know from experience that if you add the requirement without giving them help, it won't work

[deck-chair re-arrangement]

dka: there's a risk that documents like this could languish, but we have some horsepower to keep this up to date

Alex: I'm worried that this won't be part of a larger process...that it'll be disconnected from all the other things we ask them to consider

[discussion of virtual currencies as they could relate to gaming the TAG]

DKA: I'm concerend about the production of the document...if we keep it as a self-review questionaire, then it could earn its place in the process vs. if we invest our hopes into the document and then need to make sure it's fit for purpose

mnot: I'm worried about making this a joint-effort with WebAppSec because I've heard concerns that there are WGs who aren't happy with WebAppSec creating constraints on other groups. IF it's published, would like to see it published by us.

mkwst: if the TAG wants to pick it up and publish/use it, then that'll mean I should sit down and finish it. I know some things about security/privcy, but my opinion alone won't produce a document that's comprehensive. Input will be required.

mnot: does anyone think this needs to be a Rec? A finding might be an appropriate agreement.

DKA: ...with the caveat that Privacy IG/WebAppSec are consulted.

[tightweight coordination discussion]

[discussion of...#scribefail]

mkwst: I presented this to the Privacy IG last year, and ndoty had a fingerprinting doc and there's some overlap in the style of these documents. I don't care if my document is the one that gets published, want the content to be published.

Tantek: do you think the document is in good-enough a state to be useful?

mkwst: ndoty reviewed Manifests with it

Tantek: but that wasn't a self-review?

mkwst: doc is good enough to start with, but it's not done.

hbeeman: it helps to consider what sort of spec you're looking at. PII in best-practices for publishing data confounds this. More context \& use-cases would help.

ndoty: there were awkward cases about PII, e.g.

[agreement that mkwst will take pull requests and issues on github]

timbl: does this ask questions about impersonation? e.g. phishing and fullscreen.

mnot: would love to discuss how appropriate these sections are in specs, but not right now

tantek: who here is editing a rec-track WD and would be willing to add a self-review and a security \& privacy considerations section?

ndoty: I have a [fingerprinting draft](http://w3c.github.io/fingerprinting-guidance/)

mnot: it doesn't reflect my understanding about how the browser folks feel...

ndoty: I've tried to update the document to reflect skeptical views, but maybe not enough

timbl: I've expressed before that SOP is too big. Browser folks have expressed that they don't see how they can do path-based restrictions. I would love to have a spoof version of the W3C site where all the slashes are replaced by dots just to prove the point.

Tantek: you want sub-directories to be separate origins?

mkwst: have you looked at the sub-origins proposal? (http://blog.joelweinberger.us/2013/08/suborigins-for-privilege-separation-in.html)

mkwst: it isn't clear to what extent we can do that, but it's somethign WebAppSec can do

timbl: it seems like all the infrastructure is already there.

slightlyoff: most storage systems are exclusive, not hierarchial

[everyone points out why/where that isn't true, e.g. cookies, document.domain, wildcard DNS]

mnot: we regret those decisions and would take them away if we could. We can't chagne browsers too much without breaking things.

plinss: Priviledged Contexts discussion?

yan: summary here was that we can start to use this for TAG spec reviews?

plinss: can we take a resolution to publish this?

[discussion about repository location]

resolution: will move from mike's repo to TAG repo, tantek will test it out on the spec he's editing. the tag takes it up as a publishing item.

tnatek: looking forward to seeing the TAG repo URL - will be adding non-normative self-review to CSS3-UI: http://dev.w3.org/csswg/css-ui-3/


### Priviledged Contexts (née: powerful features) - https://w3c.github.io/webappsec/specs/powerfulfeatures/

mkwst: there was a lot of debate, held up rechartering, etc. Long story short, there's now a document. There's a definition that scopes it to particular types of connections.

dka: I understood it when it was called "powerful features" and "privileged contexts" as it felt like we were discussing the nature of the powerful feature, but I don't understand it if we're just talking about it in terms of features that need security... talking about "secure features" seems like a loop.

mkwst: I agree. It feels like a challenge to lay out a story in this spec because if how we had to navigate the chartering. The objections were about the tone of the document and I think we can say the same thigns without falling into language that's too advisory towards other WGs.

mkwst: doing a joint-deliverable with the TAG allows us to better provide recommendations. The spec will be reworked to provide non-normative advice about what to be considered.

nick: are you also giving non-normative advice on how to mitigate issues?

mkwst: we're looking at many features that are currently available over plaintext but which shouldn't be. Chrome and FF are looking at how to migrate sites without breaking everyone. Geolocation will need to be secure-origin only but others might not.

mnot: what's the timeline?

mkwst: 2 questions: how long will it take? and when can I start? Won't take long. Substantial agreement about definition of priviledged context. Rewriting the spec will take a few weeks. Getting consensus a few more weeks. Starting now, middle-of-the-year.

mkwst: yan and I should sit down and get it done. There hasn't been a whole lot of practical impetus to get the doc done because Chrome \& Mozilla are already doing the right things. THe right stuff is already happening.

Tantek: disagree. Documenting it will have strong value for developers and other companies to point to. It lets them say "W3C is going down this path..."

mkwst: not sure that has more weight than "Chrome has stopped supporting this thing..."

yan: e.g. WebCrypto, only over HTTPS in Chrome but HTTP and HTTPS in FF. Extended discussion on Mozilla security list on this.

mkwst: that discussion is one of the reasons mozilla was reticent about first draft.

mnot: would be good to get you an FF sec in a room to talk about this.

slightlyoff: to what end?

mnot: to get agreement between those teams?

DKA: it would be helpful if it represents reality. If it doesn't, it isn't useful.

timbl: to what extent have you looked at unintended consequences of introducing this? Seems like mixed content.

[discussion of dividing the world into two distinct buckets]

mnot: long discussions with Mozilla where they'd like to see an across-the-board policy of some variety. Maybe just misunderstanding?

hbeeman: is there a use-case doc for this?

mkwst: there's a section that talks about problematic charachteristics.

hbeeman: threat model section?

mkwst: Section 3. bing maps, yandex/yahoo/someone have a mapping service over HTTP and do geolocation; they'll break. Many WebRTC demos are over http and we'd like to turn getUserMedia() off over HTTP. EME also should have been HTTPS-only. Going forward, Mozilla has announced a desire to deprecate HTTP. They'd like new features to exist on HTTPS and not HTTP.

timbl: so Mozilla wants to deprecate the existing web?

mnot: no, they'd like new features not to be available to the existing web.

mkwst: need to find the actual thread to avoid misquoting.

[intent to deprecate HTTP](https://groups.google.com/forum/#!topic/mozilla.dev.platform/xaGffxAM-hs%5B1-25%5D)

DKA: can we have a more focused conversation? Building on top of the "securing the web" publication seems more focused.

DKA: I think we should have a conversation about geolocation because I do see it abused in the wild. The prompting when you land on a page, e.g.

slightlyoff: if we're going to talk about geolocation ,I think we should talk to that WG... there's lots wrong with it, we should discuss with them

mikesmith: they are also working on geofencing. That happened after a discussion with them about powerful features. You didn't have the opportunity then but you do now.

ndoty: there's a SW angle there and that might require HTTPS implicitly

[recounting history of TLS/SW decision]

Thanks, mkwst!

### Packaging! with special guest Ilya (https://github.com/w3ctag/packaging-on-the-web)

dka: packaging spec or packaging general topic? we have this joint spec in webapps.

ilya: background -  wasn't aware of work on packaging until recently in mailing list to web-perf group. Long discussion of pitfalls. Specifics of the solution are counterproductive to performance best practices, esp in HTTP/2 world, however. Concerned with "streamable package" packaged into one deliverable sent over the wire. How to prioritize, invalidate, update, download efficiently? I could go on and on, but the pitfalls aren't necessary to achieve the goals.

DKA: Last year, there was a lot of discussion of "do we really need this, given ServiceWorkers, other approaches?" Yehuda was a vocal advocate, coming from the js library use case (dependency resolution and fetching).

Ilya: In the js lib use case, no need to actually send everything as one file. Lot of package/module reuse, so being granular is a benefit. So I think you can achieve most runtime goals of packaging.

plinss: note that individual parts of a package are individually addressable by the server.

ilya: have not heard that need from server developers.

plinss: then there's the ePub use case. There is a collection of web resources that I want to email - what do I do?

alex: so the proposal is change the spec to allow references to other resources? instead of inlining?

mark: lot of concern in http2 server community that this is uncharted territory. Seems odd to standardize package format, expecting that we'll meet all these needs.

alex: sounds like large community of http1.1 people for whom this is a net win as long as the packaging format is reasonable. HTTP2 is a separate issue. It doesn't codify any practices at the wire level - can feed resources preemptively out of cache.

ilya: confused. HTTP2 makes a lot of this stuff unnecessary due to things like server push; i don't agree that this is always a win for http1, however. This can cause lack of priority control, causing issues for HTTP1 servers. Wanted: cache fill mechanism, list of files to fetch, etc. Should be protocol-agnostic.

Alex: Can put file descriptors at the front, then the question of whether file bodies is included in the format is separable.

Mnot: so the client would abandon the connection after getting metadata if it has the resource in cache?

Alex: in trouble for http 1

mnot: [clarification on current state of the package spec WRT cache filling]

Alex: start fetching package over wire when you hit a link rel in the document. meanwhile you scan for more things to request. We've discussed ways for smart servers and clients to cooperate to make this more efficient.

ilya: [explains mapping to http2 pushes]

mnot: I don't understand the benefit of including payloads in the package if we have to support non-package-aware clients for legacy.

Alex: this is an open question. considering format where we only have references, or optional payloads.

ilya: seems useful to have a cache fill manifest for optimization.

Alex: can do that with packaging today.

ilya: how is this not just an html import? seems like lots of mechanism in place.

alex: not as contentious. doesn't require executable context of html, can be used for epub or any grouped resources.

dka: epub use case, is it something digital publishers are looking for?

plinss: yes. epub is just zip with a manifest, they want something better.

alex: zip has ordering issues - the directory is at the end for ease of concatenation. bad for streaming. also signing issue.

plinss: [explains need for easy epub distribution mechanism for non-developers]

ilya: fair enough, but use cases on the doc are antipatterns. afraid of this being abused.

mnot: my suggestion is to take the performance benefits section out. add caveats section. lots of question about whether clients/servers will be written to do the right thing with packages.

ilya: back to epub. user doesn't care whether package contains bodies. i click on file and download starts.

dka: but users expect that an epub file they downloaded contains the actual book.

ilya: slight tangent, but have you seen the bitorrent browser? i think the distinction b/w having a file and having a file descriptor is valid. but i may not want to email the entire file, just a descriptor like in torrent.

timbl: there's UI precedent for showing "partial" files in OS X

yves: to me what is interesting is relationship tree between URIs. this html loads this CSS, etc.

plinss: also a use case is "save as" -> client can save webpage in a format that another browser can understand.

mnot: what is the TAG's involvement? this is interesting to many groups. should encourage collaboration with web perf and epub groups.

timbl: is there a mime type for this?

yan: i think so? application/package?

ilya: i agree the file metadata is interesting to have and potentially useful. the method of fetching data could be a separate discussion, more contentious

alex: what to do next? jeni no longer in tag.

mnot: any intent to implement?

alex: need potential for signing. can't predict outcome.

yves: figure out references

dka: remove discussion of performance

ilya: reverse terminology - "inflated" package can be achieved through multiple means; we can explore mechanisms of inflation.

[Yves to work on spec, dka creates an issue on github]

[break - we decide to have the July TAG meeting in Berlin]

### Web performance with special guest Ilya

dka: what can tag do to help?

ilya: we are rechartering the web perf group. there is a github repo with the current charter. we get a lot of feedback in the group about performance, like developers who want to know when something is visible on the screen. digress into deep discussion of rendering engines. We're trying to figure out how to charter so we can divert feedback to other groups productively. effectively agreed on this today.

[Web Performance Group draft charter](https://w3c.github.io/charter-webperf/)

[scribe problems and catch-and-release portal commentary]

Travis: I was drawing a parallel to what we discussed with the security considerations document. In WebAppsSec, we got pretty far along and decided to publish it. Here, this is a set of use cases — performance is cross-cutting.  Could ultimately be a document the TAG could adopt. Perhaps add that to your charter?  To collect the feedback you're receiving, so that it's official, and that the TAG may be involved in what happens next.

Ilya: With a view that publishing by the TAG would get other groups to...

Travis: in the extreme, to create a new working group to handle something.  
… Is that crazy?

Alex: Not sure. Curious: are there areas where we could help create more or better channels to help you get things done with other groups?

Ilya: Right now: visilbilty observer. General concept of: I want to know when something is shown on the screen. Turns out to be complicated.

Tim: And then what do they want to do? Change the DOM?

Tantek: count it as a view on the ad server?

Alex: Three use cases.  
… 1 Count as that – the IAB has a viewability requirement for ad impressions.  50% viewable for one second, then a transitionary period of 70% viewable for a period. People are running inefficient polling code, draining batteries. CPU wakeups, all the rest.  
… 2. Scrolling — I don't want to have to stamp out the DOM for all the potential elements in the list (or load all the data for them) when you only need to stamp out the DOM for the visible elements (Facebook has given feedback about scrolling as a use-case)  
… 3. Delayed loading. People don't want heavy resources until they're in/near the primary viewport. Common across panel-based UIs in iOS or Android. Today's JS application architecutures are heavily penalised for not knowing what's on the screen.

FYI in the WebDriver spec we have a [element displayed algorithm](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-element-displayed) for ascertaining an element's visibility.

Ilya: We're being asked: give us a better way to measure our performance for what we care about. If I'm Amazon, it's about the product. On-load firing is arbitrary.

Alex: Do you think the Web Perf group is the right home for that?

Ilya: I don't know. There is a big audience for that group who are really interested in it.  The group has concrete and useful feedback for these questions.  
… At a minimum, we can document these things.  Running list of complaints, similar things.  Then we can discuss what to do with them (TAG or not)

Peter: Crosses into the Houdini task force as well.  It would be polyfillable, with Houdini APIs in place

Ilya: these discussions happen — somebody comes up with some idea — but then I get feedback from a rendering team or someone else which disagrees and asks us for time to solve it.  We don't know what they're doing, what their timing is, if we agree…  … Just drafting a document would be a good start.

### HTTP to HTTPS

```
 \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
< encrypt the web! >
 ------------------
        \   ^\_\_^
         \  (oo)\\_\_\_\_\_\_\_
            (\_\_)\       )\/\
                ||----w |
                ||     ||
                
```

dka: there is still lots of content served from HTTP urls, they aren't encrypted but could be. Most browsers hide scheme part of the URL but show the lock icon. 

tbl: The "s" was an unfortunate mistake. The important part is that the connection is encrypted and authenticated. People feel like that they have to move everything to HTTPS and change all their links.

dka: can't the expectation be that http(s) is decoupled from whether the connection is encrypted and authenticated?

tbl: many details, like whether to use the same port.

dka: we assume that encryption is good, especially authenticated encryption. mark, why is none of this possible?

mnot: lots of discussion in last 2 years. The high order bit is that for backwards compatibility to existing servers, we need to negotiate the upgrade securely. However the negotiation is happening over an insecure channel the first time you connect. Attacker can downgrade.

dka: isn't this an issue with SNI?

mnot: that's authenticated

mnot: so you can remember that a site was upgraded like in HSTS. this is still subject to a window of downgrade of course. security folks have not said they want to do this. the focus has just been about pervasive monitoring.

timbl: in previous discussions -  we decided it was possible to negotiate upgrade. the problem is that the browser is indicating secure vs non secure site.

mnot: with OE, don't indicate security of the connection ever. Not even if authenticated.

plinss: why not?

mnot: security UX folks are concerned that the same page can change security state in the UX.

tbl: i think it is misplaced for browser ux to lead ppl to expect that HTTPS = secure lock icon. The browser and user have the burden of making sure user is not attacked, not the creator of the link.

mnot: we have discussed whether the cert needs to be authenticated in OE.  we decided not to because one of the main goals is to make it easier to deploy encryption, without getting a cert.

tbl: why on earth would you want to do that?

mnot: because under the very large assumption that surveillance is passive, this is useful

plinss: but if this is shown as equivalent to HTTP for the user, no harm?

yan: that is contentious. server operators may not implement https because of this, etc.

dka: ok, ignore opportunistic encryption for a second. you can still negotiate to a enc., auth. connection that shows HTTP in the browser.

mnot: we can convince ourselves of this but we need webappsec and security UX people engaged in the conversation.

dka: wouldn't one way to start the conversation be to start a strawman?

dka: say that i go to bank.com in a fresh browser. it's a redirect HTTP to HTTPS. how is this better than HTTP being upgraded to secure HTTP?

mnot: what if the cert doesn't match?

dka: hard fail, whatever browesr does nowadays with bad cert.

plinss: this mechanism is missing the property of HTTPS where I get either secure or nothing when I type into a browser addressbar.

yan: my understanding is that we don't get rid of HTTPS, just add additional mechanism to upgrade HTTP transparently

plinss: try port 80 first or 443 or something else?

mnot: happy eyeballs

tbl: let's just deprecate HTTP on IPv6! just kidding

mnot: one problem is request doesn't indicate whether it's in the context of TLS or not in this new proposal.

[summary: proposal is to do a sticky upgrade to HTTPS with cert validation and put that in the user experience.]

mnot: but will http and https be different via same-origin policy?

timbl: one idea is if there is an hsts header, they are the same.

mnot: seems like we should engage with webappsec.

timbl: it's about the transition plan, not breaking the web, motivating people to move to encryption.

plinss: it will take years for this to move into stable releases of ubuntu, debian, etc.

dka: is it worth writing a strawman?

mnot: maybe a better proposal is to go in with questions?

tantek: i'm confused about what use cases are. upgrade insecure requests spec already addresses some use cases (preventing mixed content with legacy links, upgrading navigation). the TAG can add value by documenting these use cases.

mnot: was hinted in securing the web finding.

(TODO: start documenting use cases for upgrades, AKA https that looks like http.)

tantek: use-case contribution from IRC: Billions of hyperlinks on pages use "http:" - one goal is to have those links "just work" when the user clicks them without being vulnerable to a MiTM attack

Relevant to this topic, the TAG should be aware of [Web  Security Context: User Interface Guidelines](www.w3.org/TR/wsc-ui/) from 2010,
and [Web Security Experience, Indicators and Trust: Scope and Use Cases](http://www.w3.org/TR/wsc-usecases/) from 2008

[TAG returns from mandatory team building event]



