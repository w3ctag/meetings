## W3C Technical Architecture Group face-to-face
### - DRAFT -
### September 29

---

### Attendees

*Present:* Daniel Appelquist, Tim Berners-Lee, Domenic Denicola, David Herman (afternoon), Yehuda Katz, Sergey Konstantinov, Yves Lafon (remote), Peter Linss, Mark Nottingham, Alex Russell (afternoon), Jeni Tennison

*Guests:* Noah Mendelsohn (for discussion on Capability URLs)

*Chairs:* Daniel Appelquist, Peter Linss
*Scribes:* Domenic Denicola, Yehuda Katz

### Contents

- [HTTP/2 Update](#http)
- [EWS Berlin](#ews)
- [Packaging on the Web](#packaging)
- [Capability URLs](#capability)
- [Extensible Web Report Card](#reportcard)
- [TPAC Hack on Service Worker](#tpachack)
- [F2F Planning](#f2f)

[Agenda](https://www.w3.org/wiki/TAG/Planning/2014-09-F2F)

---


<a name="http2"/>
###Topic: http2 update

__mnot:__ WG last call ended a few weeks ago

... there are a few small-medium issues remaining

... should be closed in week or so

... IETF last call will take a couple of weeks

... RFC in Jan/Feb if all goes well

... large number of implementations (about 20)

... IE & ISS, Firefox very eager, Chrome is shipping, Akamai, nginx will implement, Varnish are rewriting their core

__wycats:__ isn’t Varnish not compatible with caching?

__mnot:__ it’s an application-specific cache, but http/2 doesn’t say anything about caching really

__mnot:__ Apple, we don’t know, but probably they’ll implement

... the big question is Apache; Google has given them the modspdy code base

__dka:__ the big question at the NY meeting the sense of urgency was about SPDY having such momentum

... and the fact that Apple was supporting SPDY

... leading to the question of whether there would be enough momentum to get off SPDY to http/2

__mnot:__ we were a big confused by the Apple announcement

__wycats:__ they’re doing it because there’s lots of SPDY that exists

__mnot:__ Twitter have been very active, they’ve shipped very rapidly

... both Google & Microsoft have said that they’ll turn off SPDY support when http/2 comes through

... SPDY is really hacky, so they do want to get away from it

> **dka** Related URL: http://http2.github.io

__wycats:__ it would only affect super advanced sites in practice anyway

__mnot:__ they’ve been versioning SPDY very rapidly

> **wycats** proof: DEPRECATION WORKS ON THE WEB!

... after RFC there are a few things more eg opportunistic encryption

... there are a group of mobile operator vendors talking about proxies

... lots of privacy & security concerns around that

__wycats:__ http/2 doesn’t mandate SSL right?

__mnot:__ it doesn’t, we decided to move on and not require it

... but the browsers are saying they’ll only support http/2 for SSL

__wycats:__ we’ve talked about making it easier to get certs

__mnot:__ there’s an active discussion in the community about that

__timbl:__ what kinds of plans are there?

__Domenic:__ Cloudflare have a blog post yesterday spelling out they’re giving free SSL/TLS

__wycats:__ that’s great for Cloudflare customers

__timbl:__ I want to enable certificates signed by my family, people I trust

__wycats:__ that restricts what content you can see, because other sites aren’t signed by those certificates

__timbl:__ creating socially-signed certificates only as complicated as social network sites

... the existing tools are bad, but they could be redesigned

__wycats:__ I don’t think this is a standards issue: I think the standards are there

... I think write it and see

__timbl:__ I think it requires some redesign, some P2P-oriented protocols

__wycats:__ I don’t think they should be designed up front

__timbl:__ it would be nice for the TAG to be somewhere where we can imagine a different world

> **wycats** "role of the TAG" is a good discussion to have every time we have a new member

> **JeniT** [pop]

__dka:__ is there anything that the TAG can do to help http/2?

__mnot:__ in the long run, the issue of the role of the network in communication is interesting

... comms between client/server is a 2 party problem not a 3 party problem

... we’ve pushed back around breaking encryption etc

__dka:__ what timbl was saying about Verizon putting ads into pages sounds horrifying

__mnot:__ there’s variability in cluefulness in mobile operators

... is it appropriate for the TAG to publish an opinion that says “X on the Internet sucks”

__dka:__ it can be useful to publish a blog post or an official Finding

... we can more actively intervene to get people talking

__wycats:__ in this case what they’re doing is against existing standards

__dka:__ we can also use the relationship between GSMA and W3C

... when the issue is about getting information out there we can use that

__mnot:__ in the IETF we have a position that writing words down has very little effect & regulation has little effect

... we’re moving towards enforcing what we believe technically

... eg if you think that connections should be end-to-end then use encryption & make it hard to break

... enforcement through technical means

... “standards & protocols & code is making law”

__timbl:__ I think that’s a dangerous possible route

> **dka** CF: https://github.com/w3ctag/secure-the-web

... it’s going towards an all-out battle of the robots, on who can out-design the other one

__wycats:__ we can say what we want in the code protocols, but we have to persuade people too

__mnot:__ it’s not that we’re making law by making code, but the way we write the protocols shapes the world

__timbl:__ I think you need to start off with the principle/rule “your stuff shall not get interfered with”

... and if people break that “you’re banned”

... when you put in your fortress, when they find a way to break it, you need to have a paper trail

... you need to have a principle to point to

__wycats:__ I think you need human beings talking to other human beings

... you have to get the people in the room

... most people aren’t acting maliciously, they’re just confused/misinformed

__mnot:__ I don’t know, I think it’s a business decision, not confusion

__timbl:__ it’s a huge income stream, it’s deliberate

> **wycats** wycats: opt-outs don't affect the income stream

> **wycats** wycats: this is why ads are ok with DNT opt-outs

__dka:__ we talked about writing “Secure the Web”

... about crypto everywhere etc

... it’s out of date now, but we could update it

__mnot:__ there are lots of people writing, we could throw our weight behind them

__Domenic:__ there are things we can say around API design

__wycats:__ we can talk about the browser as the platform, and security in the browser

...

__Domenic:__ our recommendation should say “browsers should tell the user when NX records are compromised”

__wycats:__ there’s a way that user agents could surface the sniffing/spying more effectively

__mnot:__ there are ways to tell the user when the CA isn’t one built in to the OS

... you get a different icon in the location bar if the CA isn’t one built in to the OS

... that’s a step forward

... the pushback is that users ignore that UX

... but there are users for whom it is important

__wycats:__ Chrome makes it hard to click through now

... NXDOMAIN hijacking should be pretty easy to detect

__mnot:__ easier than captive portal detection

> **wycats**  we could standardize a domain like: iamhijacked.com :P

__dka:__ is there an action we could take as the TAG?

> **SteveF** SteveF has joined #tagmem

... should we be moving towards minimisation, only allowing privacy-infringing information passed through secure channels

__mnot:__ we should definitely talk about privacy-sensitive features as the TAG

__wycats:__ Alex has the idea that we could do more with hosted apps if we let them opt in to stricter security

__dka:__ the balanced approach: to have access to the camera, I’ll give up something

__wycats:__ eg not running third party scripts

__dka:__ this runs into permissions, which we’ll discuss Tue afternoon

__wycats:__ there’s a lot that’s already in the platform, there’s a social problem: we need to let people extend the platform

__mnot:__ “prefer secure origins” is just about prefering HTTPS

__dka:__ the thing about third-party ads is important

... people don’t want to go to HTTPS because it prevents them displaying the ads & limits their revenue

__wycats:__ because if you opt into HTTPS you opt out of mixed content

__dka:__ moving to HTTPS has major implications

__Domenic:__ our position should be “privacy sensitive features”: these are things that have the ability to, if they’re man-in-the-middled, compromise people’s privacy

__timbl:__ I worry that browser vendors are slapping on security constraints

> **wycats** sigh

... the mixed content thing that forces abandoning HTTPS or abandoning HTTP

... is there a model of the world in which we could access HTTP things from HTTPS pages, then fine

> **Yves** talking about UI and mixed-content, https://bugzilla.mozilla.org/show_bug.cgi?id=838395 is not really helping

... but they way Chrome “refused” messages, I get the impression people are slapping on constraints on developers

__wycats:__ there are features on the web that expose private information, and web browsers would like to avoid leaking that

... one large mechanism for leaks is plain text HTTP

... if you just serve the HTML page over HTTPS, there are many other things (like scripts) that can access that information

... they want to offer some assurance that the private information is private

__timbl:__ as a result, they turned off the ability to read completely public data over HTTP

... an intermediate library can’t access it either

__Domenic:__ it’s better not to give false positives on privacy

__wycats:__ another common way of leakage is third party scripts

... the solution the Chrome guys used for mixed content is the same as for connecting to CNN, the ‘ad view’ tag

... a way of putting in content in a completely sandboxed way

__timbl:__ that’s fine in HTML, but when I’m writing a web app, how can I tell Chrome that I want to access stuff that’s completely public

... it’s got a CORS-Origin: * because it’s accessable by everyone

__wycats:__ the analogous thing for ‘ad tag’ is to have a sandboxed area that enables your script to access the data

__timbl:__ no, we have to move towards either writing my code inside browser extensions, or have a way of users saying that they trust scripts from a particular location

> **wycats** this is not the correct group to have this discussion

> **wycats** unfortunately

__wycats:__ the problem is not that we don’t trust authors, it’s that the authors don’t know what they’re putting in their pages

... you have to limit what the third-party script can do

... eg prevent a third-party script from getting your geolocation

__dka:__ you can still fingerprint or do other things in that kind of environment

__wycats:__ the script would have access to nothing except post message

... the environment that contains the script could still pass that information

... but the author that’s installing the script will have to be explicit about what it’s giving the script

__dka:__ what’s the status of this work

__wycats:__ iframe sandbox and CSP give you reasonably close to lock down, there’s also realms in Javascript, which could give you a just-Javascript context

... but timbl’s original point is correct: there isn’t a model for how you avoid leakage

> **wycats** it isn't coherent

> **wycats** people are just stabbing around trying to lock things down

> **wycats** but it's kind of random

> **wycats** and driven in large part by what you can get away with

> **JeniT** [discussion that browser extensions, plugins, wifi etc insert scripts into pages the author never knew about]

__Domenic:__ CSP is a pretty big hammer; it would be great if you could allow geolocation but not enable those to be passed to the third party scripts

__wycats:__ the ad tag which the Chrome appstore does is the correct approach

__Domenic:__ secure origins is a clear feature which we can recommend

> **Yves** tagging data in the engine... but it would require a huge change

__mnot:__ the ‘prefer secure origins’ approach has consensus

__dka:__ we have to address the way that impacts people who have ads in pages

> **wycats** <adview> would allow mixed content that didn't trigger a mixed content warning

__dka:__ what’s the action?

__mnot:__ we should ratify ‘prefer secure origins’

__wycats:__ a large number of geolocation-using sites would break with this policy

__mnot:__ this is for new features, right?

__Domenic:__ no

__timbl:__ the resolution is that you should only be able to call features which are sensitive from HTTPS?

__dka:__ yes

__timbl:__ my point is if a developer wants to access something which is private, and therefore needs to use a secure page, it means that he can’t access public data

__mnot:__ until it goes HTTPS

... if I’m relying on government data, I’d hope it was from the government

__JeniT:__ GOV.UK is https, but that’s not the case for smaller organisations

__dka:__ if I take the user’s location in script & make a request to https://gov.uk with my location in the query string, I can do that, right?

... there are still leakage possibilities

__Domenic:__ in theory the browser could surface all the places that have access to your location, but if you allow the page to access http sites then it could be everyone

> **JeniT** [NSA knows everything already]

__dka:__ we could draft a statement that says “for new privacy-sensitive APIs, we want these to require secure origin”

...”

> **Domenic** Draft recommendation here http://oksoclap.com/p/kCUkARlDtn

> **wycats** 👍

> **wycats** https://hackpad.com/Untitled-RQucKs6BLTT

> **JeniT** [drafting in oksoclap not hackpad]

> **JeniT** [drafting in hackpad not oksoclap]

> **JeniT** [drafting in oksoclap not hackpad]

> **JeniT** [hackpad requires access to Google contacts, oksoclap isn’t https]

> **dka** https://etherpad.mozilla.org/qPTpp2UKfa

> **JeniT** [drafting in etherpad]

> **wycats** https://developer.chrome.com/apps/app_runtime

> **JeniT** proposed resolution: https://etherpad.mozilla.org/qPTpp2UKfa

__Mnot:__ how should the TAG communicate?

__Domenic:__ on EME they would have preferred us to file a bug rather than issuing an edict

__wycats:__ when it’s more architectural, and there isn’t a spec, then a post etc would be more appropriate

__mnot:__ just having it in the minutes doesn’t work

__dka:__ we could put it on the blog, or on our GitHub-hosted home page

... like the http group did

__mnot:__ have one place

... why not move the findings to github, and CNAME tag.w3.org to github

__Domenic:__ we have lots of different kinds of things we publish: Findings, guides, short statements

__mnot:__ TAG Findings are architectural: this is a short one but fits into that scope

> **wycats** see https://github.com/tc39/ecma262

> **JeniT** [discussion on publication process]

> **JeniT** Domenic & mnot propose to create a home page for the TAG onto a GitHub Pages page

__dka:__ we could use w3ctag.org

... the W3C page would be static, only change when the membership of the TAG changes

__timbl:__ w3.org should have a record of everything that we do

... we need to make sure we have the archive

__mnot:__ for IETF we save all the state from GitHub, using API access to the issues as JSON

... we check the JSON into the repo it’s associated with

... if GitHub were to go down, we’d need to do some work to reconstruct it

__dka:__ keeping the history, getting it archived on w3.org, is really important

... w3.org has the longer lifetime

__timbl:__ I will talk to the sysadmins about the TAG having the subdomain tag.w3.org

> **dka** PROPOSED RESOLUTION: We support efforts by browser vendors to restrict privacy-sensitive features to secure origins. This includes ones that have not historically been restricted as such, like geolocation or webcam access.

> **dka** We also support investigation into ways of preventing these features from leaking to third-party scripts within a webpage (although the exact technology to do so is unclear as yet, probably involving some combination of CSP and/or something like <iframe sandbox>).

> **dka** +1

> **Domenic** +1

> **wycats** 👍

> **plinss** +1

> **twirl** +1

__timbl:__ I’m concerned this will break code

__mnot:__ I think a little context about medium term pain would be good

__Domenic:__ this is an aspirational resolution

> **dka** Agreed.

> **wycats** architecture architecture architecture

> **Domenic** Adding: "We appreciate this could cause some short and medium-term pain (breaking some existing content), and so this needs to be done with care, but it is a worthy goal to aspire to."

<a name="tag-resolution-29sep2014-2"\>
> **dka** RESOLUTION: We support efforts by browser vendors to restrict privacy-sensitive features to secure origins. This includes ones that have not historically been restricted as such, like geolocation or webcam access.

> **dka** We also support investigation into ways of preventing these features from leaking to third-party scripts within a webpage (although the exact technology to do so is unclear as yet, probably involving some combination of CSP and/or something like <iframe sandbox>).

> **dka** We appreciate this could cause some short and medium-term pain (breaking some existing content), and so this needs to be done with care, but it is a worthy goal to aspire to.

> **dka** now lunch

> **JeniT** LUNCH

> **dka** we will be back at 13:00 UK - for web of things discussion

> **twirl_** twirl_ has joined #tagmem

> **timbl** mnot, code for extracting discussion state and issues into gitable files?

> **dka_air** dka_air has joined #tagmem

> **dka_air** https://call.mozilla.com/#call/awwfKaBNSJk

> **mnot** mnot has joined #tagmem

> **mnot** mnot has joined #tagmem

> **mnot** mnot has joined #tagmem

> **dka_air** https://opentokrtc.com/w3ctag

> **mnot** mnot has joined #tagmem

> **dka** ok that looks stable - we’re going to try to use opentokrtc.com

> **dka** Seems to work best with either Firefox Aurora or Chrome Beta/Canary.

__ScribeNick:__ Domenic

__ScribeNick:__ JeniT

> **Domenic** https://w3ctag.github.io/promises-guide/

__Domenic:__ the promises guide has been converted to look fancy

... also updated the readme, and contacted PLH to get the w3.org URL proxy to here

... at which point I can update the links

... there are a few issues but none are particularly big

__wycats:__ is this where you’re adding the ECMAScript++?

__Domenic:__ no

__dka:__ there’s nothing here that states the status of this document

... and talks about the stability of the document

... and the fact that it’s going to be updated etc

... also you have it as public domain

... I’m happy with that, don’t care, PLH might say it should have a W3C something or other on it

__Domenic:__ I wanted to use the W3CTAG logo

... this is using Tab Atkins bikeshed tool

... people like it and have been using it

__wycats:__ I think we should get streams done, because people will be creating promises that should be streams

> **Yves** +1 to streams

> **Domenic** http://w3c.github.io/mediacapture-main/getusermedia.html#dom-mediadevices-getusermedia

... the new Ember is based on streaming stuff

__Domenic:__ ^this^ is now returning a promise

> **dka** PROPOSED RESOLUTION: pending a couple of document boilerplate changes (document status, logo, etc...) we agree that the Promises Guide is a published finding of the TAG.

__Yves:__ I saw the issue about using ‘parallel’ rather than ‘async’, and I didn’t understand why

__Domenic:__ there was a lot of confusion, when we looked at how it was actually be used, it’s actually about using a different thread

... we actually mean ‘don’t block’

__wycats:__ maybe you should say ‘concurrently’

__Domenic:__ all of the uses of ‘in parallel’ are actually in separate threads

__wycats:__ it’s all giving instructions to things that actually have threads

__Domenic:__ right, this is writing specs for browser implementers

__Yves:__ I think that’s misleading if you’re writing a guide that’s directed a JS programmers

__Domenic:__ that’s a good point; in the document there are places ‘this is more applicable to spec writers’, it would be worth calling that out

... and say ‘in JS you would use a WebWorker’

__Yves:__ for me, it feels that there are synchronisation things that need to happen

__Domenic:__ currently when we say ‘in parallel’ we actually do need to double check that

__dka:__ we should publish this as a Finding

... the boilerplate changes don’t change that

<a name="tag-resolution-29sep2014-1"\>
> **dka** RESOLUTION: pending a couple of document boilerplate changes (document status, logo, etc...) we agree that the Promises Guide is a published finding of the TAG.

<a name="ews"/>

### Topic: EWS Berlin

__Domenic:__ it went pretty well; we got the word out to a lot of developers

... discussions that stood out:

... editing (guy from MS was there)

... contenteditable, intention events like ‘cut’ instead of Ctrl-X

__wycats:__ is that because the platforms have different key bindings?

__Domenic:__ yes

... the rest of the things are eg cursor support

__wycats:__ instead of trying to fix contenteditable, we should figure out what we need

__Domenic:__ that’s what they’re doing

__dka:__ we got some good input from developers who need this

__Domenic:__ I noticed that it’s easy for someone to take over the discussion

... in the future we should be clearer about the messaging that this is not for you to present

... this happened in a couple of sessions

__dka:__ it’s a fine line: you have to enable people to talk about their project, but you can’t let it overload the session

... hosts should be a moderator, not a leader

__dka:__ being a moderator is the key thing: you have to be in charge of the conversation, and making sure that everyone has input

__Domenic:__ even if the messaging is ‘we don’t want one person to take over the session’

> **dka** yes we do

> **dka** hold on

__dka:__ I think we did a better job of talking about moderators at this session

> **dka** https://opentokrtc.com/w3ctag

__JeniT:__ people need to be happy to leave if they are bored of one person hogging the discussion

__wycats:__ sometimes the people who are talking need to have that discussion

> **dka** best viewed on Firefox Aurora™

> **dka** (or chrome)

__dka:__ the only other thing on EWS is that you’re talking to other people who are taking that name and running something in Oakland

... but we should write a one pager on what EWS is

... for other people who want to run them

__wycats:__ in particular having implementers & practitioners in the same room

__dka:__ I’ll start that document

> **dka** :)

> **wycats** The place where practitioners and implementors meet is exactly "The Extensible Web"

> **wycats** For the record, I think Hangouts works grea

> **wycats** great*

> **wycats** all hail NaCL



<a name="tc39"/>

###Topic TC39 update



__wycats:__ we’re still in the process of finishing ES6

... not a huge number of changes in ES6

... change of process for ES7 is going well

... there’s a website that have the 17 features in the ES7 features

... we’re using github

... github has list of proposals, which you can keep an eye on

> **wycats** https://github.com/tc39/ecma262

__wycats:__ we’re moving to a process where when it’s implemented we stamp it ‘standard’

... rather than creating a ‘standard’ which we then expect to be implemented

__dka:__ this is also about the pattern of enabling practitioners to extend the web, and how this impacts standards

... this is related to what we have about the future of the future of standards, on our agenda on Wed

__wycats:__ also in TC39, we moved the loader into a separate document

... we realised it’s intertangled with the browser loader

... need to let it evolve with the web and with node

__Domenic:__ we also had some discussions about how to make DOM objects subclassable

... and arrived at a solution which people have varying opinions on

... but that can ship in ES6 without us having to do lots of work

... the new process is going well

__wycats:__ almost everything that’s happening now is about locking down ES6 and moving to the new process

__JeniT:__ what counts as implemented?

__wycats:__ when web content relies on it, which could mean one browser

> **wycats** depends on reality

__dherman:__ it’s been the understanding of TC39 for a while that you need two implementations to advance to one of the last stages

__wycats:__ yes, that’s in practice what’s going to happen

> **wycats** my thinking is that the closer things match realpolitik the more useful they are

> **wycats** so why does 2 impls matter? because it means people rely on it

> **wycats** it says 2 impls

> **Domenic** i agree that the new process document says 2. i find wycats interpretation is good too, possibly better.

> **wycats** the more we can base in on reality, the less standards lawyering can get in the way imo

> **JeniT** /me votes for using technology that works rather than technology you wish would work

> **wycats** dherman: c

> **wycats** my interpretation is derived from Brendan's general analysis

> **wycats** dherman: totally agree

> **wycats** dherman: I understood your point 5m ago :P

> **wycats** dherman: c



<a name="packaging"/>

### Topic: Packaging on the Web

> **JeniT** ScribeNick: Domenic

__JeniT:__ we discussed the general issue of how to send packages of files over the web in an efficient, easy-to-deploy way

__JeniT:__ one of the main drivers of this was JS modules

__JeniT:__ (but not the only driver)

__JeniT:__ the initial discussion focused on using special URL syntax

> **JeniT** URL syntax: package/!/filepath

> **wycats** package/!//filepath

__wycats:__ the point is there is some separator syntax that doesn't conflict with existing web content

> **Yves** what would // uris mean then? (protocol-relative URLs)

> **JeniT** http://example.com/path/to/package.pack/!//home.html#section1

__mnot:__ so the package is downloaded in toto and deconstructed on the client side?

__JeniT:__ that is absolutely correct

> **JeniT** http://example.com/path/to/package.pack

__JeniT:__ so we looked at that, and wrote a readme which was

> **JeniT** https://github.com/w3ctag/packaging-on-the-web

__JeniT:__ it looked at the various options and decided this wasn't quite the right plan

__JeniT:__ we decided on a different way of doing it which was using link relations

__JeniT:__ there would then be a separate syntax within the HTML page which said what the scope of the package was

__timbl:__ the scope being everything up to the /!//, in the previous proposal

> **JeniT** http://w3ctag.github.io/packaging-on-the-web/

__JeniT:__ that was written up at ^

> **SteveF** SteveF has joined #tagmem

__JeniT:__ we then had, via dherman, some pushback (which was from Jonas I think?) but which hasn't yet surfaced on the www-tag list or elsewhere from what I can tell

__wycats:__ explaining the critique: the proposal you suggested requires that someone navigate to or embed the URL from a document which has the context

__wycats:__ however you could not give people a link to the document

__wycats:__ for example you could not give people a link to slide 15 since we no longer have URLs for each part of the package

__dherman:__ my interpretation of the objection is pretty close but...

__dherman:__ it is---the only way to understand the contents of a package is by consulting the webpage context that established the <link rel="package">; i.e. it's contextual

> **JeniT** see http://w3ctag.github.io/packaging-on-the-web/#fragment-identifiers

__dherman:__ you can't hand out the link because to get into the package they have to start from the document which references it via the link tag

> **JeniT** or http://example.org/downloads/editor.pack#url=/root.html;fragment=colophon

> **timbl** q+

__dherman:__ this is a concern for the far-off future

__dherman:__ any interim solution will be contextual

__timbl:__ did we discuss redirections?

__wycats:__ we discussed lots of things that require a server but we decided it was our constraint to not require a server

__timbl:__ you could use a 209/303 something

__timbl:__ the pushback for that from a lot of people was that we want the packaging system to work on gh-pages without GitHub changing their code

__mnot:__ I have a much bigger problem with this spec, which is that we're spending a lot of effort in HTTP2 to make the web more fine-grained, because it's better for performance

__wycats:__ we absolutely discussed at great length the objection you are about to raise

__mnot:__ (continuing) web performance has been moving toward higher granularity because for example when you concatenate libraries it causes large downloading and parsing times

__mnot:__ finer-grained also gives you more efficient caching

__mnot:__ it's a little disheartening to see a trend in the other direction

> **Domenic** +1

__wycats:__ the goal of this spec is absolutely not to replace http2 or to suggest that http2 is not the future

__mnot:__ but i was reading the goals and they're about e.g. populating caches...

__wycats:__ there are two primary goals not handled by http2. 1) a transitional technology while people have not deployed http2

__mnot:__ we'll see....

> **Yves** archive has the advantage that you can send a coherent set of resources, like js files in a library

__wycats:__ this packaging tech can be polyfilled with service worker, and in general browsers can be deployed to consumers faster than servers

__wycats:__ there are servers taht will not be upgraded but people have access to what files they store there

__wycats:__ basically for people who have access to "FTP servers" somewhere they can dump files

__wycats:__ use case 2) I am ember or jquery and I want an archive I can dump somewhere that includes all the HTTP metadata and semantics

__wycats:__ in my view the ideal world is that I give you Ember via a package and you serve it via SPDY. But I don't have to configure it on the server, the configuration is in the package.

__mnot:__ 1) seems iffy, but 2) could be really exciting.

> **dherman** fuuuu

__mnot:__ other question---why multipart mime instead of .zip?

> **Domenic** wycats/JeniT: streamability

> **dherman** headers!

> **JeniT** http://w3ctag.github.io/packaging-on-the-web/#streamable-package-format is the definition of the format

__mnot:__ from a performance standpoint, packages are a big footgun. But there are some possibilities too.

__timbl:__ would you imagine caches understanding this?

__mnot:__ similar to service worker case; this is a security problem for people using the same use case

__mnot:__ note that alice's plain HTML page being attacked by bob's JS page on the same origin is a *new* security problem

__JeniT:__ so should we go back to the URL-pointer issue dherman/wycats raised?

> **JeniT** http://w3ctag.github.io/packaging-on-the-web/#fragment-identifiers

__JeniT:__ I get what you are saying; the way it is described currently in the spec is that you would use a particular fragment identifier for the files within the package that would be interpreted as reaching into the package

__JeniT:__ see link

> **JeniT** http://example.org/downloads/editor.pack#url=/root.html;fragment=colophon

__JeniT:__ it's ugly, but it works, addressing your issue

__wycats:__ you could also do this with client-side hacks

__dherman:__ the reason why any of those solutions are scary are that they all rely on everybody doing extra work when they have a package to make the links continue to work

__dherman:__ the browser has UI e.g. right-clicking on an image

__dherman:__ and getting a URL

> **Domenic** why doesn't the URLs in JeniT's proposal work for that purpose? Right-click, get fragment-identifier URL

> **JeniT** or just the relative link, I don’t get it

__dherman:__ if you put some effort into figuring out how to mitigate this cost, i would feel better. e.g. wycats'

__dherman:__ s suggestion of a JS library

__dherman:__ my other reason is that we said in the last meeting that there isn't any reason why we couldn't eventually have both solutions

> **wycats** dherman is raising issues related to "open image in new tab" kinds of UIs

> **wycats** the fact that all of these assets are not universally addressable

__dherman:__ i am not blocking this work i just have this URL issue

__wycats:__ i just had a spidey-sense realization. people complained that they could not adopt webp because even though it worked on the web people couldn't right-click and save it and view it on their computer

__Domenic:__ dherman I don't understand; JeniT's proposal has URLs you can get to

__wycats:__ JeniT's proposal would allow to only serve the package if you knew you were dealing with only a new browser?

__JeniT:__ yes. But the URL would work in any case.

__wycats:__ but that won't work with relative URLs

__JeniT:__ that's right

__dherman:__ but that's OK! it creates a canonical absolute URL. Oh wait but relative addressing with a HTML file will not work...

__JeniT:__ right, that won't work. So in the general case you create un-packaged stuff and serve that too.

__dka:__ what is the status of the actual packages document?

__wycats:__ maybe the right thing to do is to say the document is done ("a draft") and ask for polyfills on top of service worker

__dka:__ right but ipr issues

__dka:__ can we outline the issues and where we agree/disagree?

__JeniT:__ we are generally happy about streamable package formats and its rough struture, with the proviso that IETF guys may have issues

__mnot:__ yeah, multipart media types have a long history and set of corner cases

__JeniT:__ then we have the two alternatives of package link relation or URL separator

__dherman:__ we could go in this direction, that doesn't preclude is investigating the other direction

__dherman:__ "also" not "instead of"

__dherman:__ i also have another set of extensions that i'd like to explore when we have a chance, but that's an orthogonal point

__JeniT:__ so the question is should we also in parallel with getting package link stuff implemented try to get the URL stuff implemented

> **JeniT** https://github.com/w3ctag/packaging-on-the-web#specialising-urls

__JeniT:__ my original feeling was that trying to specialize URLs is a bad idea and we shouldn't go there

__wycats:__ one area of exploration we didn't do because we didn't have dherman's constraint before was separating getting a resource from inside a page that knows about packages, to having a link to a resource that is inside a package. maybe by separating them we can get new design space.

__wycats:__ e.g. schemes work fine, jar does it, but there were other issues

__wycats:__ the other issues being about embedding not relative addressing

__dherman:__ one of the issues is http vs. https, so you need to compose

__dherman:__ the question is, will I ever shut up about the URL approach? I think I don't need to shut up about it for the <link> approach to proceed.

__dherman:__ I think it's important for the <link> approach to also solve the linking problem

__dherman:__ the more we can address the linking constraint the better

__dherman:__ i will be less worried about the need for an additional URL approach if we can be sure the <link> approach addresses that

> **JeniT** http://w3ctag.github.io/packaging-on-the-web/#installing-web-applications

> **Domenic** (discussion of how to extend the format)

__wycats:__ what we probably want is a way to register with the service worker a decoder for certain package mime types

__wycats:__ i.e. with a polyfill you could do this all you want, but if it gets implemented in browsers you'd have to reimplement the entire polyfill to get this extensibility back

__dka:__ next steps?

__JeniT:__ who should I contact within webapps to push this forward?

> **Yves** art & chaals, start a CfC to publish a first draft

__dka:__ send a message to art, cc me, let's get things started

__dka:__ you may wish to join webapps first

__Yves:__ note that this work is in the webapps charter that was approved so it won't be a surprise to anyone

__dka:__ and Yves is the TAG contact for webapps so he should be able to help

__Yves:__ you should ask Art for a call for CfC if you want to move faster

__JeniT:__ I think it's good enough for a first working draft

__dka:__ let's do this!

__wycats:__ we should find someone good to do the polyfill

__wycats:__ like maybe guy bedford who has done great module polyfills

__dka:__ can you contact him?

__wycats:__ i will ask him to come to tomorrow's developer meetup

__wycats:__ this is basically http2 in the browser, in the same way service worker is a server in the browser

__mnot:__ but it's http2 without any of the benefits

__wycats:__ umm ... no?

__mnot:__ i want to see some numbers

> **Noah** Noah has joined #tagmem

__plinss:__ we should use the new pub process

> **Noah** OK, guessed that would likely happen. No prob. at all. Best guess on end of break?

<a name="capability"/>
### Topic: Capability URLs

__JeniT:__ the current draft came about because of some discussions about a year ago where we thought it'd be a good idea to put down some good practices around capability URLs

__JeniT:__ recognizing that people are using them; recognizing that there are issues with using them; and trying to get a balanced view between people who thing they're bad and those who think they're useful

> **JeniT** http://w3ctag.github.io/capability-urls/

__JeniT:__ we have a draft ^

> **JeniT** http://www.eecs.tufts.edu/~noah/w3c/capability-urls/2014-09-27-Noah.html

__JeniT:__ Noah has some comments he has created an amended version at ^

__Noah:__ (recaps comments from email)

__Noah:__ could be useful to give more "be careful" advise

**Noah** http://lists.w3.org/Archives/Public/www-tag/2014Sep/0045.html

__Noah:__ substantive changes in section 4.1.2

__Noah:__ (recaps examples)

> **Noah** Punchline from example section: It is essential when deploying Capability URLs to analyze risks such as these and to ensure that countermeasures are appropriate to the requirements of the application. For some applications, Capability URLs will not provide sufficient security.

> **Noah** Deleted: If you have decided to use capability URLs, depending on the level of risk associated with the discovery of a capability URL, you should employ as many of the following security measures as possible.:

> **Noah** Replaced with: The sections above on Risks of Exposure highlight the challenges of protecting Capability URLs from unintented discovery. When considering use of Capbility URLs it is essential to ensure that such risks can me sufficiently mitigated to provide the security required for the each particular application. The following techniques are recommended and will in many cases provide adequate security:

__dka:__ these changes look really good to me. i am happy with the balance

__JeniT:__ I'm happy

__timbl:__ did we discuss about browsers indicating capability URLs?

__JeniT:__ we did, 4.3 "Future Work"

> **JeniT** http://w3ctag.github.io/capability-urls/#future-work

> **Noah** I did not intentionally renumber an appendix to be a section.

> **Domenic** s/4.3/A/

__JeniT:__ outside the scope of this document, but in the scope of possible future work

__JeniT:__ mnot you said you had some comments?

__mnot:__ nah, i reviewed this a while back and was reasonably happy

__JeniT:__ we have got this out as a FPWD (the previous version)

__JeniT:__ there are a few bits I need help with; search for "Issue 1" and "Issue 2"

> **JeniT** http://googleonlinesecurity.blogspot.co.uk/2012/08/content-hosting-for-modern-web.html

> **JeniT** http://lists.w3.org/Archives/Public/www-tag/2014Jun/0003.html

> **Noah** One other thing that we don't need to discuss explicilty: I listed myself as editor for revised draft but that is not intended as a proposal that I be listed as editor of the final document (unless Jeni wants help with that)

__mnot:__ i would shy away from specific security recommendations

__Domenic:__ "consult your nearest security professional?"

> **Domenic** mnot/dka: yes

__plinss:__ but will people do that?

__dka:__ (this is regarding issue 2 btw)

__dka:__ this relates to a specific piece of mailing list feedback. did it provide anything more helpful, e.g. suggested tet?

> **Domenic** s/tet/text/

__JeniT:__ yes, it included some stuff I incoroporated, but not the hard part

__JeniT:__ can we find someone else who's written a fantastic guide on creating such URLs? Or shoudl we?

> **mnot** http://tools.ietf.org/html/bcp106

__dka:__ I think it's acceptable to say that it's not in the scope of this document

> **Domenic** timbl/Domenic: there are good xkcds on this subject ;)

http://xkcd.com/221/

http://xkcd.com/936/

> **Noah** You should get permission to include those images in the finding.

> **JeniT** noah2: I should get permission to include screenshots?

> **Noah** Said mostly in jest, but yes.

> **Noah** I meant of the xcds

> **JeniT** ah!

> **Noah** s/xcds/xkcds/

__Domenic:__ web crypto!

__wycats:__ uuid.js!

__JeniT:__ or some equivalent rubygem

__JeniT:__ basically saying "use someone that exists don't invent it yourself"

> **Domenic** dka/wycats: can we say "use something cryptographically secure"

> **slightlyoff** Very sorry for being late. OMW

> **dka** Suggested text fo address issue 2: 2nd para of 5.2 - cut our second sentence and insted just say “you should use the mechanisms cryptographically secure …”

> **JeniT** “you should use the cryptographically secure mechanisms available within your web application framework to create these secure random numbers, rather than trying to invent your own approach”

> **Noah** Is that actually in all cases good advice?

> **slightlyoff** E.g. webcrypto?

> **slightlyoff** Yes.

> **Domenic** +1

> **timbl** +

> **plinss** +1

> **timbl** 1

> **Noah** Are there not cases where a sophisticated corporation, e.g. would know to provide something better than the app framework?

> **timbl** s/+\n1/+1\n/

> **Noah** I think it would be better to say "you should typically use"

> **JeniT** ok

> **slightlyoff** Thanks

> **Yves** +1

> **twirl_** +1

> **dka** +1

> **slightlyoff** It's *always* good advice.

> **JeniT** “issue 1: http://w3ctag.github.io/capability-urls/#managing-access-on-sandboxed-domains”

__JeniT:__ OK what about issue 1

> **Noah** I suspect the NSA might disagree when they're using it for their own work, but you could be right.

> **slightlyoff** NSA has enough math majors on staff that they don't need our advice

> **slightlyoff** But if they *are* looking for a piece of my mind....

> **Noah** That doesn't make the "always" claim correct does it?

> **slightlyoff** Indistinguishable from "always" is "always"

__JeniT:__ I didn't understand this feedback enough to really incorporate it

__Domenic:__ maybe get in touch with the guy who submitted that feedback?

__JeniT:__ OK, I'll try that

__JeniT:__ once those are done I'd say it's ready for a new public working draft

__dka:__ shall we just say it's an agreed finding that we may amend as new information comes in?

> **slightlyoff** Gimmie 3 minutes

__JeniT:__ sure

> **Noah** Wanted to say that my additions were written in some haste. I would welcome tweaks Jeni might make to either the scenarios or the wording.

__JeniT:__ it's in /TR/ space currently

> **JeniT** Noah, no problem, I’ll fix up while incorporating

__dka:__ have findings previously been in TR space?

__Noah:__ not sure but I believe that the ones that become RECs are

__dka:__ so if it's REC track ...

> **Domenic** noah2: at times we made findings notes

> **noah2** There's been some history of the community not noticing Findings. Recommendations do get more visibility IMO and have more force, but you sometimes have to work through more process stuff (good and bad) to get there.

__dka:__ probably best to publish it *somewhere*, TR space may not be the best space

__dka:__ (recapping) TODO:

> **Noah** BTW: another usage scenario is: user gets Capability URL, user accesses Capability URL, the corporation for which he works logs all URI request, sysadmin finds the URL in the log.

__dka:__ 2 changes from Noah's draft into updated draft

__dka:__ change status from "draft" to "TAG finding"

> **Noah** FWIW: the status of document in Jeni's draft says "This is intended to become a TAG finding"

> **Noah** IMPORTANT: TAG Findings have historically been linked from: http://www.w3.org/2001/tag/findings

__Domenic:__ I think the strategy we like is gh-pages + proxy on w3.org

> **Domenic** Domenic/dka: we can also reduce boilerplate in document heading if it's not REC track, and we can CC0 it

<a name="reportcard"/>
### Topic: Extensible Web Report Card

__slightlyoff:__ the EdgeConf panel on different image formats was relevant, about how it's not possible to polyfill new image formats or decompression algorithms on the client side in an extensible way

> **slightlyoff** what is an image that doesn't fit in memory?

__Domenic:__ with service worker you can do this for images that fit in memory. With streams, you can do it for images that don't fit in memory

> **slightlyoff** does any browser currently handle images like that?

> **Domenic** a video :). Or a 5 MB animated gif

> **Domenic** on a mobile phone

> **slightlyoff** yes

> **slightlyoff** navigator.connect()

> **slightlyoff** ah, yes, video

> **Domenic** (discussion turns to exposing hardware capabilities via service workers to allow hardware vendors and not browser vendors to add capabilities)

> **slightlyoff** Domenic: my example was something like new sensors mapped, e.g., to http://device.example.com/apis/v1/thinger/

__wycats:__ generally we haven't been spending much time talking about ways to add new device capabilities into the platform

> **Domenic** +1

> **slightlyoff** so you'd be able to do navigator.connect("https://device.example.com/apis/v1/thinger")

> **slightlyoff** .then(...)

__dka:__ let's pop back up from the specifics for one second...

__dka:__ we want to get the word out to the web developers about what we concretely mean with these extensible web design principles

> **slightlyoff** speaking of scrolling....

__dka:__ divide things into "Good" vs. "Needs improvement"

__wycats:__ anything to do with scrolling is "needs improvement"

> **slightlyoff** Apple has done as good thing in iOS 8 with scrolling

> **slightlyoff** they've started to dispatch events such that you can over-ride scrolling more easily

> **slightlyoff** and create your own behavior

__dka:__ caniextend.it

> **slightlyoff** and that's a great thing for extensibility

> **slightlyoff** I think it's a good idea

> **Domenic** +1

__dka:__ suggest Wednesday afternoon we collaboratively edit the document

> **slightlyoff** +1

> **slightlyoff** does IE optimize for ASM?

__slightlyoff:__ not yet but under development

__wycats:__ asm.js is good

__Domenic:__ CSS is needs improvement but there are a few steps in the right direction

__wycats:__ web components are not widely implemented yet

> **slightlyoff** oh, wow, it looks like IE 11 is doinga solid job on ASM

__dka:__ I think web components would be in the positive side

> **slightlyoff** custom elements are also the easiest thing to polyfill

> **slightlyoff** don't forget O.o and Mutation Observers

> **slightlyoff** we spent years on those = )

> **slightlyoff** and they talk about how other systems' semantics work

> **wycats** O.o has miles to go before we sleep

> **wycats** mutation observers are amazing

__slightlyoff:__ O.o and Mutation Observers help you understand how you would implement from the browsers perspective the dirty checking etc. that you do within a browser. They help you get grips on how the internal systems watch would otherwise be closed behaviors

__slightlyoff:__ so e.g. attribute and property values changing the behavior of a system

> **slightlyoff** CSP is interesting

> **slightlyoff** we don't have an API for it yet

> **slightlyoff** but it's good that it controls parts of the system that aren't otherwise controllable

> **slightlyoff** well, the CSP WG was responsive

> **slightlyoff** I wrote

> **slightlyoff** https://infrequently.org/2013/05/use-case-zero/

__slightlyoff:__ getting CSP to have more API is still in progress and is going well

> **slightlyoff** well, I wouldn't say "going well", I'd say "the window is open for us to collaborate with them again soon"

> **slightlyoff** ARIA is sad-making = (

> **slightlyoff** we don't have a lot of data

> **slightlyoff** e.g., how do I know that I'm in high-contrast mode?

> **slightlyoff** how do we know the zoom level?

> **slightlyoff** also, we should be calling out screen reader vendors for not doing this sort of thing correctly. They get a free pass too frequently

__Domenic:__ accessibility is not very extensible

> **slightlyoff** it's not shark-infested. It's opinion-infested. Data is immune to opinion

__dka:__ internationalization?

__wycats:__ the i18n ecmascript api seems OK? I am not sure.

__wycats:__ high-level APIs like the compass are underpinned by low-level sensors like a magnetometer. it would be ideal to expose the lower-level sensor

> **slightlyoff** whoa: http://blog.cloudflare.com/introducing-universal-ssl/

__dka:__ URL parsing?

__Domenic:__ yes. It previously was locked up in <a> and <base>. It is now exposed.

__wycats:__ archeaology -> extension

__dka:__ we should document that topic on this site

> **slightlyoff** document.all's falsyness is just a bug

> **slightlyoff** Brendan was too clever by half

__Domenic:__ the DOM. Being fixed from two sides: making DOM APIs more JavaScript-ey, and giving JS more capabilities to do powerful things like the DOM does

> **slightlyoff** we need to turn it off and call it a mistake

__wycats:__ yes, there are no longer host objects; there are exotic objects and users can create exotic objects

> **slightlyoff** there *is* a complexity cost to the system for all of these corner cases

> **slightlyoff** and something like the document.all hack need to die in the fire of history

> **slightlyoff** very sorry about that = |

> **Noah** Noah has joined #tagmem

> **Yves** +1

> **slightlyoff** will be there

<a name="tpachack"/>
###Topic: TPAC Hack on Service Worker

__wycats:__ will caches be implemented in Canary before TPAC?

__slightlyoff:__ yes

__slightlyoff:__ (behind a flag)

__slightlyoff:__ we also have a polyfill

> **slightlyoff** also, Jake's polyfill lives on: https://github.com/coonsta/cache-polyfill

__dka:__ how to schedule this?

__mnot:__ 15 minutes intro, 1-1.5 hour session?

__dka:__ longer!

__wycats:__ yes, many hours

__mnot:__ as long as there is a definite start time

__dka:__ all afternoon after lunch?

> **Domenic** (monday)

__dka:__ would it be bad to overlap with webapps?

__Yves:__ probably yes

__mnot:__ schedule for TPAC is 11am-3pm ad-hoc meetings

__plinss:__ a lot of WGs are scheduling joint meetings during that time

> **slightlyoff** QOTD: "TPAC agenda has no concept of lunch"

__dka:__ starting at 1, going until end of day

__mnot:__ some people might have to leave at 3

> **Domenic** (general agreement)

__slightlyoff:__ will we allow people to drop in who aren't officially attending TPAC?

__dka:__ i will ask, unsure whether it will work

> **slightlyoff** hah. Good point.

__dka:__ there are concerns about there being enough muffins

__slightlyoff:__ we should think harder about how to make it not an issue

> **slightlyoff** that said, I think it'd still be valuable

> **slightlyoff** getting browser vendors nearer to actual deployed tech is good

> **slightlyoff** sorry

> **slightlyoff** mute

> **slightlyoff** muted

<a name="f2f"/>
### Topic: F2F Planning

__dka:__ current plan of record is april in san francisco

__dka:__ however, suboptimal for mark and i

__dka:__ mnot's proposal was june in melbourne

__mnot:__ except it's the middle of the winter

__Yves:__ there was a proposal for Paris as well

> **darobin** I need a heads-up some time in advance to make sure it works out, but I should be able to host a meeting at Le Tank (a nice co-working space)

__mnot:__ do we want to host another EWS event in April? The last one felt a little unfocused.

__dka:__ that's kind of the idea, as opposed to a normal conference...

__Domenic:__ I think the strongest sessions are the ones where implementers are involved

> **Domenic** mnot/wycats: agree

__dka:__ open to changing the format, making it more relevant, ...

__Domenic:__ maybe make use of the EdgeConf software? It was very useful

> **Domenic** (discussion of details of colocating with Fluent)

> **dka** adjourned


