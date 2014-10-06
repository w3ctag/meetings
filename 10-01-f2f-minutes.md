## W3C Technical Architecture Group face-to-face
### - DRAFT -
### October 1 

---

### Attendees

*Present:* Daniel Appelquist, Tim Berners-Lee, Domenic Denicola, David Herman (afternoon), Yehuda Katz, Sergey Konstantinov, Yves Lafon, Peter Linss, Mark Nottingham, Alex Russell (afternoon)

*Regrets:* Jeni Tennison

*Guests:* Virginie Galinto (Security / Crypto), Robin Berjon (URL Session)

*Chairs:* Daniel Appelquist, Peter Linss
*Scribes:* Domenic Denicola, Yehuda Katz

### Contents

- Security / Crypto
- Yesterday's Event
- URL
- Modularization / future of specifiction...
- Extensible Web Report Card

---

### Topic: Security / Crypto

>  **wycats** Hiiii

>  **virginie** note that I have created some material to discuss here https://www.w3.org/Security/wiki/images/9/98/Web_Authentication_and_other_security_services.pptx

>  **SteveF** SteveF has joined #tagmem

>  **dka_air** ok try https://purl-app.com/uhsh43uo

>  **dka** ok

>  **twirl** twirl has joined #tagmem

>  **wycats** Man London traffic in the morning is bad news

>  **dka** trackbot, start meeting

>  **trackbot** RRSAgent, make logs public

>  **Zakim** Zakim has joined #tagmem

>  **trackbot** Zakim, this will be TAG

>  **Zakim** I do not see a conference matching that name scheduled within the next hour, trackbot

>  **trackbot** Meeting: Technical Architecture Group Teleconference

>  **trackbot** Date: 01 October 2014

>  **Domenic** ScribeNick: Domenic

 __dka:__ we are about to send over some technical feedback on the EME spec

 __dka:__ one of the points of discussion yesterday was about how in some jurisdictions it's illegal to do security testing of DRM mechanisms

 __dka:__ wondering if we could have some kind of process lever, similar to the patent policy, to compell W3C members who are part of the EME group to agree not to sue companies or individuals doing this kind of security testing

 __dka:__ a good point of discussion between the TAG and the AB, as a new kind of policy-level thing

 __virginie:__ are you confident this is illegal?

 __domenic:__ yes, anti-circumvention law in the DMCA in the US

 __twirl:__ actually that's very controversial. In theory if you prove you have no intent to crack the system, you wouldn't be in trouble. But in practice it is used a lot.

>  **twirl** http://en.wikipedia.org/wiki/United_States_v._ElcomSoft_and_Sklyarov

 __twirl:__ if I were a security specialist I would be scared

 __dka:__ we thought this would be good to bring up because it's not a part of the technical feedback we want to give, but it is important feedback we want to give, if possible. We are not lawyers so we are not sure, but we wanted to bring it up.

>  **twirl** s/to crack the system/to violate copyright

>  **virginie**  https://www.w3.org/Security/wiki/images/9/98/Web_Authentication_and_other_security_services.pptx

>  **virginie** https://www.w3.org/Security/wiki/IG/webcryptonext_workshop

 __virginie:__ (reviews slides)

 __virginie:__ it was asked which features you would be willing to contribute to in the WG?

 __virginie:__ (reviews wiki link)

 __virginie:__ it was unclear where to put new topics as they were raised; this is a more general W3C issue

>  **virginie** http://lists.w3.org/Archives/Public/public-web-security/

 __virginie:__ there were lots of non-members involved in the discussion, so we decided to have the conversation on public-web-security

>  **Domenic** Domenic: does webcrypto not have a public mailing list?

 __virginie:__ it is readable to all, but not writable to all

 __virginie:__ also we did not want to disturb the progress on finalizing webcrypto

 __domenic:__ sounds good :)

 __virginie:__ the web security interest group does not have resources at the moment

>  **Domenic** (next slide, "Other topics")

 __Domenic:__ how much interest was there from implementers on new features for web crypto?

 __virginie:__ definitely Microsoft is interested in having credentials or sensitive information being stored in something that is external to the browser

>  __virginie:__ Mozilla already has an implementation to integrate with **secure** element, but they are not interested in standardizing it

>  **dka** https://wiki.mozilla.org/WebAPI/WebNFC#Fifth_iteration:_Secure_Element_.28Firefox_OS_v2.2.29

>  __virginie:__ we could define a way to integrate with other secure (authentication) services, which could offer some of the stuff a **secure** element could offer, but we would want it to be as open as possible

>  **dka** cf http://www.w3.org/TR/nfc/

 __virginie:__ FIDO alliance is interested in secure tokens

 __domenic:__ but they're not a browser vendor, right?

 __virginie:__ right

 __virginie:__ unclear whether these next steps are a high priority in the browsers

 __domenic:__ I am scared that you guys will do good work coming up with cool things and then it won't be implemented in browsers

>  **virginie** are you talking about http://mikewest.github.io/credentialmanagement/spec/

>  **Domenic** yes

>  **Domenic** (Domenic asked about interest within webcrypto about that proposal)

 __virginie:__ there is nothing too security-related here; we didn't have a chane to discuss it

 __virginie:__ also unclear where it should go

 __virginie:__ maybe webapps

>  **mnot** mnot has joined #tagmem

 __virginie:__ probably doesn't need cryptographers to review it

 __virginie:__ maybe webappssec

 __virginie:__ but once again no security concerns, it's basically about managing data

>  **wycats** adoption hacks ðŸ‘

>  **Domenic** Yves: webappssec would be a nice place to have this kind of work

>  **Domenic** Yves: they could help review to avoid e.g. exposing credentials when you don't want to

>  **Domenic** ScribeNick: wycats

>  **wycats** domenic: good job getting it over the finish line. I understand it was long and hard.

>  **wycats** ... and shipping everywhere is good

__virginie__ it's not done yet

>  **twirl_** twirl_ has joined #tagmem

__domenic:__ it's shipping!

__virginie:__ we have to decide whether to include auth in the WebCrypto charter

>  **wycats** __.__.. we could use help to avoid creating thousands of working groups

>  **wycats** __.__.. your advice would be helpful

>  **wycats** ... would you create a new auth WG?

__domenic:__ it really depends how people want to work

>  **wycats** ... for example the mega-web-apps WG seems to work fine

>  **wycats** ... other people may not

__wycats:__ it probably depends on whether the exact same group of people in an existing WG is the same group that needs to work on another work item

__dka:__ unless someone doesn't WANT to work on something, expanding the reach of an existing group seems better

>  **wycats** ... **thanks virginie**

>  **virginie** thanks for listening, will keep you informed about the next achievement of chartering discussion

### Topic: Yesterday's event

__dka:__ where should we tell people to engage if they're interested

>  **wycats** ... specifically engagement on our developer activities

__mnot:__ perhaps we want a repo for meta-issues

__wycats:__ opening issues about developer meetups on github is weird

>  **wycats** ... I think specifiction is the new mailing list

__mnot:__ who runs specifiction? w3c?

__dka:__ robin

>  **wycats** **scattered discussion about mailing lists**

__dka:__ so specifiction

>  **wycats** ... I feel like it should be an issue on Github

__domenic:__ I like Github

>  **wycats** ... instead of having many mailing list, it seems Specifiction / Discourse's model is one big list

>  **wycats** ... Github is a place to talk about concrete issues

______wycats:__ The way Ember uses Discourse is as a place for unstructured comments that can get routed to Github Issues

__domenic:__ this is different from the WHATWG's use of mailing list

>  **wycats** wycats: it's good to have a sense of what goes on Github, Stack Overflow, etc.

>  **wycats** ... but if you just semi-automatically close issues on Discourse, people feel bad

>  **wycats** ... this was our experience in Ember

>  **wycats** **dka talks about developer participation in the summits**

__dka:__ it seems good to have a developer outreach component to our f2f meetups

__wycats:__ it seems like the group of people who show up are from a closed circle

__dka:__ it depends on the city

__wycats:__ I think that JS users are our dominant audience

__dka:__ last night about 1/2 the audience didn't identify as JS developers

__dka:__ so what's the topic in Discourse?

__domenic:__ "standards / developer interfacing"

>  **darobin** darobin has joined #tagmem

>  **dka** darobin ready to join us?

>  **darobin** sure!

>  **darobin** do I skype you?

>  **darobin** or webrtc something?

>  **mnot** http://w3ctag.github.io

### **wycats** Topic: URL

>  **wycats** **discussion about TC39 and normative references**

__wycats:__ the optics of this are very bad

__domenic:__ please proceed Robin

__darobin:__ there's a lot of ground to cover

>  **wycats** ... the core of the issue is whether the HTML specification can reference the URL specification normatively

>  **wycats** ... and in particular whether it's the WHATWG authored version or the W3C copy of it

>  **wycats** ... from a technical perspective I think we're ok

>  **wycats** ... the HTML spec is pretty modular

>  **wycats** ... but there are more complex social and political issues

__dka:__ this is related to an effort to get the HTML5 spec published

>  **wycats** ... I had asked Philippe if the TAG could help

>  **wycats** ... I had a goal of trying to figure out where we go from here

>  **wycats** ... the initial feedback I had from Philippe is that we need a URL spec in W3C space

>  **wycats** ... so we talked about using the same approach as the DOM spc

>  **wycats** ... it's not a copy

__wycats:__ in what important ways is it not a copy?

__dka:__ it's a reprint

>  **wycats** ... but I didn't realize that WHATWG agreed to snapshots

>  **wycats** ... and that there was ongoing IPR efforts

>  **wycats** ... I don't think it was the right approach

__wycats:__ in what way?

__dka:__ because they were pointing to the CG W3C agreement

>  **wycats** ... and a stronger approach would be to use the W3C patent policy

>  **wycats** wycats: it was not clear to me before that the normative reference requirements involve a policy that is as strict as the W3C

__dka:__ moving on...

>  **wycats** ... we thought maybe there was a middle ground

>  **darobin** q+ to try to process the three aspects of this separately

>  **JeniT** JeniT has joined #tagmem

>  **wycats** ... to make it explicit that the spec was a reprint

>  **wycats** ... but to get the stronger IPR from the Web Apps WG

>  **wycats** ... it feels like we almost got there

__wycats:__ am I correct in understanding that the current state of the debate is about which CSS stylesheet is applied to the document?

__dka:__ that would be very silly

__wycats:__ I agree, that's why I phrased it that way ;)

__darobin:__ there are several issues here

>  **wycats** ... 1) the core technical problems with URL

>  **wycats** ... it is far from perfect

>  **wycats** ... we have browsers that are not aligned with it

>  **wycats** ... how do we unify URLs in browsers with how they are used in other systems

>  **wycats** ... we probably can't solve it quickly

>  **wycats** ... 2) dka said that there was a controversy about what HTML needs to ship

>  **wycats** ... and this was framed as requiring a W3C spec

>  **darobin** http://www.w3.org/2013/09/normative-references

>  **Domenic** http://www.w3.org/community/w3process/track/issues/124

>  **wycats** ... the current normative reference draft provides a set of considerations

__timbl:__ indeed. I was misquoted.

>  **wycats** ... WHATWG specs can be referenced, but there are case-by-case considerations

>  **wycats** ... that are defined by the normative reference guidelines

>  **wycats** wycats: the mailing list post said "However, based on my conversations with Consortium staff last week, the Director will NOT permit a Proposed Recommendation to include a normative reference to a WHATWG spec"

>  **wycats** ... and it would have been good to get clarification

__timbl:__ it was hard to figure out how to reply

>  **wycats** ... for example marcos asked why W3C won't accept WHATWG as a peer org

__domenic:__ I would like that to get resolved

__timbl:__ for example, when you look at the WHATWG charter, it says it's a closed WG by invitation only

>  **wycats** ... it's good to know the clear process

>  **wycats** ... the WHATWG advertises it as an invitation-only group

__darobin:__ my personal analysis is that the way that HTML interfaces with the URL spec is sufficiently modular and orthogonal that it's ok to reference something we know is going to be updated

>  **wycats** ... Domenic and I worked hard on figuring out a way to do joint applications

>  **wycats** ... there are some issues right now but we can find agreement

>  **wycats** ... I thought the WHATWG did a friendly thing by handing over DOM parsing to W3C

>  **Domenic** domparsing.spec.whatwg.org redirects to https://dvcs.w3.org/hg/innerhtml/raw-file/tip/index.html

__dka:__ I think it's good to have HTML5 in the W3C

>  **darobin** and I heartily applaud that

>  **Domenic** as it was realized the W3C is doing a better job there

__dka:__ enterprise IT consultants want to know that it's stable

__timbl:__ people working in the government want to know if they should revise their procurement policy

__dka:__ they find it important to know

>  **darobin** q+ to close that rathole

>  **wycats** wycats: nobody is waiting for HTML5 to ship in order to use features that are post-HTML4

>  **wycats** ... I think it is self-evidently absurd to claim anything of the sort

__darobin:__ we're not going to get agreement

>  **wycats** ... I would like to get it to REC to free up resources

__domenic:__ a core issue is that it's a big web and many orgs doing many things

>  **wycats** ... it's unnecessarily combative

>  **darobin** q?

>  **darobin** ack dar

>  **Zakim** darobin, you wanted to try to process the three aspects of this separately and to close that rathole

__wycats:__ the high order bit is whether people are implementing

__timbl:__ let me tell you a story

>  **darobin** [timbl explains how W3C was the WHATWG before the WHATWG was cool]

>  **dka** Correction to what I said - I think itâ€™s good to have w3c html5 go to Rec.

>  **mnot** q+

>  **dka** q?

__timbl:__ you said the high order bit is that it's where "cool things are happening"

>  **mnot** q+

>  **wycats** ... but what about closed membership?

>  **darobin** +1 to Domenic

__domenic:__ I think the WHATWG meets the criteria by any definition

>  **wycats** ... there is just a terminology issue

>  **dka** +1 as well, with explict respect to URL

>  **timbl** q?

__dka:__ I think WHATWG meets the criteria 100%

>  **wycats** ... especially for URL

__mnot:__ I have historically been circumspect about the WHATWG

>  **wycats** ... it would be ok if it was closed to browser vendors

>  **wycats** ... but with a clear governance model

>  **wycats** ... but if the lawyers at browser vendors are ok with the WHATWG, it seems fine

>  **mnot** http://tools.ietf.org/html/rfc2026#section-7.1

__mnot:__ there is precedent for incorporating proprietary specifications

__wycats:__ and proprietary standards are strictly worse than what the WHATWG is doing

__mnot:__ I don't think the high bar is actually required

__domenic:__ and if you look at the OpenStand principles, I think it is very clear that we [the WHATWG] actually adhere very strongly to those

>  **wycats** http://imgs.xkcd.com/comics/standards.png

__dka:__ what does the IETF think

__mnot:__ we'll clean up whatever mess you guys make

>  **dka** :)

>  **wycats** ... we are eagerly awaiting the results

>  **wycats** ... many IETF people think that this could be solved via a preprocessing step

>  **wycats** ... where "this" means the difference between the WHATWG spec and the the RFC

>  **wycats** ... there is a difference between URIs and URLs

__Domenic and timbl:__ no

>  **wycats** wycats: real-world cases need to worry about the browser's version of "URL"

__timbl:__ keeping things as a preprocessor ("liberal" vs. "conservative" spec) is a good idea

>  **Yves** wycats, which browser version. The unparsed one or the parsed one? (or both)

__Yves:__ the semantics of a URL defined in the platform

>  **wycats** which includes both

__wycats:__ 100% of web servers in the real world do some error correction

__darobin:__ we had to write a special server for the platform test

__mnot:__ the WHATWG can own URL

__wycats:__ I like how the HTML5 parser works with "error states" + error correction

>  **darobin** http://galimatias.mola.io/

>  **wycats** ... I think it's analogous to what Tim wants

>  **Domenic** there was also one in C

__domenic:__ can we normatively reference the WHATWG?

__dka:__ the TAG seems to have consensus

__dka:__ maybe we can scope to URL?

__domenic:__ we can try to make it precedent

>  **wycats** ... get rid of the bad blood

__dka:__ the bad blood is there because there is a perception that that the WATWG actors have negative actions

>  **wycats** ... we have to end the fighting

__wycats:__ it's not doing anybody (the WHATWG included) any favors

__dka and domenic__ confirm

__timbl:__ things have changed in 25 years

__.__.. we knew we were forking the IETF

>  **dka** correction: "also because there is a perception that the whatwg actors have..."

>  **dka** key word "also" - there has been lots of negativity on both "sides" of this topic

__tim:__ [suggests something needs to happen for w3c to consider whatwg to be a â€œfirst class standardsâ€ body]

>  **dka** [discussion now on what that would be]

>  **dka** My pereception is that it is a first class standards body.

__timbl:__ maybe we could look through the openstand principles and see if we would want to add things, to define how we should interact with any group

>  **wycats** I ____think it's very destructive to say that a standard that is interoperably implemented is "not a standard"

>  **dka** Tim is talking about a specific thing when he mentions OpenStand: http://open-stand.org

>  **darobin** more specifically http://open-stand.org/about-us/principles/

>  **dka** Indeed.

>  **timbl** TLDR â€œI was a pretty respectful teenagerâ€

>  **wycats** TLDR "When I was a boy, children had respect for their elders" :P

>  **darobin** q+ to point out that the H264 case is at the extreme end of the spectrum

>  **darobin** ack mnot

__wycats:__ is strict patent policy actually a requirement for normative references?

__domenic:__ points out that non-REC docs don't have patent commitments

__darobin:__ it would be awesome if the W3C would help the WHATWG with patent commitments

>  **wycats** ... for example, an experimental attempt to get patent commitments through the process

>  **dka** +1

__domenic:__ via the CG FSA form

__dka:__ telefonica is prepared to make a commitment through that mechanism

>  **dka** confirmed

__domenic:__ helping the WHATWG getting a better patent process in place is a good longer-term work item

>  **wycats** ... it seems like a new process would be helpful

>  **wycats** 1+

>  **wycats** q+

>  **darobin** q-

>  **dka** https://pad.w3ctag.org/p/resolutions-1oct2014

>  **dka** q?

>  **dka** A proposed resolution here: https://pad.w3ctag.org/p/resolutions-1oct2014 - please help me wordsmith this so that we can have lunch.

>  **darobin** [I just want to go on the record as strongly supporting the idea that we as a community need to do a much better job at flagging what's implemented and what's a proposal]

>  **Domenic** +1

>  **wycats** wycats: if the W3C is pointing at a WHATWG spec that is interoperably implemented, it can sure it will not change

>  **marcosc** marcosc has joined #tagmem

>  **wycats** **working on the resolution**

>  **dka** http://www.w3.org/2013/09/normative-references

>  **timbl** wycats, IPR in OpenStand is not very strong but is there â€” Affirming standards organizations have defined procedures to develop specifications that can be implemented under fair terms. Given market diversity, fair terms may vary from royalty-free to fair, reasonable, and non-discriminatory terms (FRAND).

>  **JeniT** JeniT has joined #tagmem

>  **dka** resolution: With regard to normative references from w3c documents, we agree that the whatwg adheres to open standards principles and that in principle there is no barrier to w3c documents refeferencing whatwg documents normatively. In the specific case of URL being rerefenced from HTML5, we recommend that the W3C HTML5 spec should reference the whatwg URL specification and that between W3C and WHATWG we should continue to resolve any remaining technical and editorial

>  **dka** issues in the spec.

>  **dka** resolution: we are heartened that the WHATWG has made moves towards having a stronger IPR policy. We propose to issue a call for patent commitments via the WHATCG's FSA patent commitment form: http://blog.whatwg.org/make-patent-commitments

>  **dka** rrsagent, make minutes

>  **RRSAgent** I have made the request to generate http://www.w3.org/2014/10/01-tagmem-minutes.html dka

>  **dka** rrsagent, make logs public

>  **dka** hm...

>  **dka** This is the raw IRC log: http://www.w3.org/2014/10/01-tagmem-irc

### Topic: Modularization / future of specifiction...

 __darobin:__ I was hoping to have a prototype implementation of the ideas

>  **wycats** ... I'm behind schedule

>  **wycats** ... The feedback from the EWS was very positive

>  **wycats** ... TLDR modularize HTML to make it easier to contribute to

>  **wycats** ... put everything on Github

>  **wycats** ... use Specifiction for broad feedback

>  **wycats** ... specific feedback on Github

>  **wycats** ... There was a general discussion about the "CSS Problem" aka millions of standards

>  **wycats** ... Another thing that came up was that there's quite a bit of interest

>  **wycats** ... people want to submit proposals

>  **wycats** ... also we want to standardize on bikeshed

 __wycats:__ I talked about feature flags once features are being actively implemented so you can build a "canary" version of the spec vs. a "release" build

>  **wycats** ... as a way to enable a more "living standard" approach with more stability marking

>  **Yves** stability markings... and implementation reports linked as well? (ala caniuse with a finer grain)

>  **wycats** **feedback is generally extremely useful**

 __wycats:__ Yves: yes, you would be able to attach implementation reports to a feature name

 __dka:__ it seems like there's a lot of synergistic work going on

 __darobin:__ we should all be paying attention to what each other are doing

>  **wycats** my closing slide from my talk yesterday: http://note.io/1rGZOo3

 __dka:__ so what's the plan?

 __darobin:__ some tooling and then some experimental work on pulling out a few initial things

 __domenic:__ it seems weird to have the W3C do the modularity work

>  **wycats** ... given that it originates with the WHATWG

 __darobin:__ it's more of a proof of concept

>  **wycats** ... some of the work will be on new features

 __plinss:__ is this like the CSS model (for new work only)

 __darobin:__ we'll start that way

>  **wycats** ... but it's important to know what's been superseded

 __domenic:__ be clear this is proof of concept so as not to confuse developers, other standards people, etc.

 __darobin:__ sounds good

>  **JeniT** JeniT has joined #tagmem

 __wycats:__ this isn't intended to be hostile, so let's make sure that we don't come off that way by accident

 __domenic:__ I liked the way you described the different venues for feedback

>  **dka_** dka_ has joined #tagmem

>  **slightlyoff** morning all.

### Topic: Extensible Web Report Card

>  **dka_** hi alex!

>  **dka_** we are about to start in on extensible web report card brainstorming

>  **dka_** can you join?

>  **slightlyoff** yep

>  **dka_** domenic will be live-editing an etherpad and we hope to transfer this over to a github repo before the end of the day

>  **Domenic** https://pad.w3ctag.org/p/ew_report_card

>  **slightlyoff** and you still can't participte in serializing something that submits a file

>  **slightlyoff** do y'all have a camera on? I can't see London

>  **slightlyoff** no worries

>  **Zakim** Zakim has left #tagmem

>  **slightlyoff** isn't there work on ambient light sensors?

>  **slightlyoff** https://groups.google.com/a/chromium.org/forum/#!topic/blink-dev/AAtN0xjI9Gc

>  **slightlyoff** brb, coffee

>  **slightlyoff** back,s orry

>  **slightlyoff** so I'm not 100% sold that ASM.js plays well with others; its default model makes FFI hard from JS and doesn't exactly have a mapping to DOM

>  **slightlyoff** it's good, and enabling, but I'm not sure it's "there"

>  **slightlyoff** minor quibbles

>  **slightlyoff** on it

>  **Domenic** wycats: see slightlyoff's take above ^

 __slightlyoff:__ ðŸ‘

 __wycats:__ move to is disruptive in class?

>  **wycats** hm

>  **wycats** I am concerned

>  **wycats** because I am unsure if FFI ever can be optimal

>  **wycats** what do you mean by mapping to DOM?

>  **wycats** I agree that these are good things to research

>  **Domenic** it seems like it could be as optimal as the C++ DOM **-** JS mappings that exist

>  **wycats** sure

>  **Domenic** you should be able to get s/C++ DOM/asm.js

 __dherman:__ what do you know about this?

>  **wycats** could in theory be more optimal

>  **wycats** since you could imagine stronger inlining

>  **wycats** but I don't know

>  **dherman** we've talked about ways to improve the FFI

>  **dherman** I agree it's an area that needs research

>  **dherman** it's better than its competitors at FFI ;)

>  **wycats** lolol

>  **slightlyoff** "better than competitors at FFI" -- I want that shirt

>  **slightlyoff** "ASM.js -- it's not SWIG"

>  **dka** dka has joined #tagmem

>  **slightlyoff** brb

>  **slightlyoff** agree that the event loop is something we can call out

>  **slightlyoff** also, coordination with other threads

>  **slightlyoff** e.g., render thread

>  **slightlyoff** audio thread

>  **slightlyoff** etc.

>  **wycats** sniffing is not exposed

>  **wycats** would be a trivial API

>  **wycats** window.sniff(blob) :P

>  **wycats** window.ðŸ‘ƒ(blob)

>  **slightlyoff** back, sorry

>  **wycats** welcome back

>  **slightlyoff** what is this URL?

>  **slightlyoff** can someone paste it here?

>  **wycats** unknown

>  **dka** dka has joined #tagmem

>  **Domenic** http://w3ctag.github.io/extensible-web-report-card/ but wanted it auto-generated from markdown so that's not good...

>  **slightlyoff** thanks

>  **twirl** looks ok to me

>  **twirl** except fonts

>  **slightlyoff** so a question

>  **slightlyoff** the Scrolling section says "scrolling is a fundamentally native capability", but I don't think this is true

>  **slightlyoff** input handling is

>  **slightlyoff** scrolling is what a system does in response to input handling

>  **slightlyoff** disconnected = \

>  **slightlyoff** will get coffee = )

>  **Domenic** wycats ^

>  **wycats** hello

>  **Yves** disconnected as well, needs to drop soon anyway

>  **slightlyoff** so I'm pretty sure that the bit that isn't being currently standardized for push is the low-level protoocol set (e.g., GCM)

>  **wycats** what I mean is that what happens when the user moves his finger is always intermediated by the system

>  **wycats** and trying to reinvent that in JS is insane

>  **wycats** and basically impossible to do reliably

>  **wycats** finger/mouse/etc

>  **slightlyoff** that doesn't make sense to me

>  **wycats** then I'm being unclear

>  **slightlyoff** the reason we can't do it reliably is that we haven't been given events

>  **slightlyoff** at least not until recently

>  **wycats** deny

>  **wycats** we have the events

>  **wycats** the user moved his finger

>  **slightlyoff** no, we don't

>  **wycats** how fast should the content move in the viewport?

>  **slightlyoff** I know from an engine perspective that we weren't giving them to you

>  **slightlyoff** up to the program.

>  **wycats** how do you know if the user meant to scroll or click?

>  **wycats** it's actually NOT up to the program

>  **slightlyoff** sure it is

>  **wycats** you do NOT want to do that

>  **wycats** no

>  **wycats** absolutely not

>  **slightlyoff** I *MIGHT* want to do that

>  **wycats** you might

>  **wycats** it is good to be able to

>  **slightlyoff** and when I do, the system damned well better let me

>  **wycats** but in most cases you want the system to decide things like momentum, what happens when you get to the top, etc.

>  **wycats** because they are OS-wide policies

>  **wycats** and you would like consistency with the OS

>  **wycats** trying to reverse engineer the OS policy *per device* and write JS libraries is crazy

>  **wycats** people do it and it's horrible

>  **wycats** they end up just applying the iOS policy to android

>  **wycats** etc.

>  **wycats** and when iOS tweaks the global policy, you're stuck with an old algorithm

>  **slightlyoff** sorry...was getting coffee

>  **slightlyoff** so you get to decide: do you want to empower developers or not?

>  **wycats** you would like a way to delegate to the native policy but still understand what is happening so you can put things on the moving element

>  **wycats** deny

>  **wycats** layering bro

>  **slightlyoff** if the answer is yes, then we must accept that there will be both high and low level

>  **wycats** there is always an intermediate layer

>  **slightlyoff** and not deny developers the low-level power just because there is high-level interaction

>  **wycats** which does the native functionality with hooks

>  **wycats** that is the hardest part of web dev

>  **slightlyoff** I think you're used to having your SDK fused into the platform

>  **wycats** it's where "rebuilding the stack" happens the most

>  **slightlyoff** in a really unhelpful way

>  **wycats** disagree

>  **wycats** people want the ability to have consistency with the native SDK on the web

>  **slightlyoff** look at "pull to refresh" as a gesture

>  **wycats** not always

>  **wycats** but sometimes

>  **slightlyoff** it didn't come from iOS

>  **slightlyoff** or android

>  **slightlyoff** it came from programs having the freedom and power to do the Right Thing (TM) becaues they had low-level, synchronous access to events

>  **wycats** not originally

>  **wycats** you're misunderstanding me but I don't know why

>  **wycats** I absolutely want people to have access to the low level

>  **wycats** absolutely 100%

>  **slightlyoff** great, then we agree

>  **wycats** but I think you can assume that once you've done that you're "done"

>  **wycats** or once you've done that plus the high level you're "done"

>  **wycats** and I'm saying there's a specific interaction that is the hard part

>  **wycats** that we do very poorly

>  **wycats** which is the interaction between content and native display/interactions

>  **slightlyoff** thinking specifically about scrolling, it's hard

>  **slightlyoff** so there's a threaded scrolling system in most impls

>  **slightlyoff** where a texture is sent to a separate thread to move in order to prevent main-thread jank

>  **slightlyoff** (this is slow, BTW, but less janky)

>  **slightlyoff** "native" apps don't do this

>  **slightlyoff** they just implement scrolling in direct response in their input handling thread

>  **slightlyoff** and now we're in a place with beforescroll that we can hint the system to say "no, I want to behave like a real boy and do my scrolling on the main thread"

>  **slightlyoff** "don't context switch me, bro"

>  **slightlyoff** this is both potentially quite a bit faster/more-responsive and more like what "regular" programs can do

>  **slightlyoff** but it means taking over the control

>  **slightlyoff** by _switching model_

>  **slightlyoff** the alternative is to expose the off-thread scroll behavior and...I dunno...invent a "scroll worker"?

>  **slightlyoff** but that's not actually something anyone wants

>  **slightlyoff** and we frequently have this issue where control means switching systems or models

>  **slightlyoff** e.g., JS and __proto__

>  **slightlyoff** you go slow path for using it

>  **slightlyoff** it's the price of control

>  **slightlyoff** there seems to me to be something fundamental in the idea that you'll have 2 systems and, as much as everyone hates it, it's unavoidable

>  **wycats** I agree

>  **slightlyoff** I think dherman makes this point frequently and better than I can

>  **wycats** :P

>  **wycats** I think this point of interaction is the key thing that triggers stack rebuilding

>  **wycats** so if you don't want people to have to rebuild stacks

>  **wycats** you need to contend with it

>  **slightlyoff** yeah

>  **slightlyoff** and there needs to be general advice to implementers in the form of "get over it"

>  **wycats** similar things happen with form elements

>  **wycats** you have to choose between "black box" and "I'll do it myself"

>  **slightlyoff** yep yep

>  **dherman** what'd I do?

>  **slightlyoff** hah

>  **dherman** http://38.media.tumblr.com/tumblr_m9027aTjbq1qkthyyo2_400.gif

>  **wycats** All I know is that Stalin still uses Geocities

>  **wycats** sbb

>  **JeniT** JeniT has joined #tagmem

>  **slightlyoff** my fault, sorry = \

>  **slightlyoff** what's the repo?

>  **dka** https://github.com/w3ctag/extensible-web-report-card/tree/gh-pages

>  **slightlyoff** thanks!

>  **dka** See http://w3ctag.github.io/extensible-web-report-card/

>  **JeniT** JeniT has joined #tagmem

>  **virginie** virginie has joined #tagmem

>  **virginie** rrsagent, please generate minutes

>  **RRSAgent** I have made the request to generate http://www.w3.org/2014/10/01-tagmem-minutes.html virginie

>  **SteveF** SteveF has joined #tagmem

>  **Domenic** plinss: https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages

>  **JeniT** JeniT has joined #tagmem

>  **slightlyoff** it occurs to me that the report card maybe should have letter grades?

>  **Domenic** it's more like a kindergarten report card, I think :P

>  **dka** I believe that is https://github.com/w3ctag/spec-reviews/commit/b9643fb8f3a4463ee5084cf2dddab09c561658f3

>  **dka** White boards from todayâ€™s meeting: https://github.com/w3ctag/f2f-meetings/tree/gh-pages/2014/sept29-oct1

>  **dka** rrsagent, make minutes

>  **RRSAgent** I have made the request to generate http://www.w3.org/2014/10/01-tagmem-minutes.html dka

>  **slightlyoff** love the whiteboards, thankyou!

>  **slightlyoff** so good

>  **Domenic** plinss: https://github.com/jasonlong/architect-theme

>  **Domenic** http://extensiblewebreportcard.org/

>  **marcosc** marcosc has joined #tagmem

>  **rubys** rubys has joined #tagmem

>  **rubys** The following is what the AC reviewed in the Proposed Recommendation:

>  **rubys** http://www.w3.org/TR/html5/references.html#refsURL

>  **rubys** The following is what the TAG recommends:

>  **rubys** http://www.w3.org/2014/10/01-tagmem-minutes.html#item02

>  **rubys** This is what I would like to suggest as a replacement:

>  **rubys** http://intertwingly.net/tmp/references.html#refsURL



