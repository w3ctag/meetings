##TAG teleconf

###27 May 2015


###Present: Dan (dka), Hadley, Peter, Mark (mnot), Yan, Travis, Tim

###Guests: Nick Doty (W3C), Wendy Seltzer (W3C), Javun (Mozilla)

###Regrets: David, Yves

###Chair: Dan

###Scribe: Yan

###Topic Fingerprinting 

--

[Agenda](https://github.com/w3ctag/meetings/blob/gh-pages/2015/telcons/05-27-fingerprinting-redux-agenda.md)

*mnot:* when i first read the doc, i thought it wasn't reflective of browsers' position. on a later reading, seems less misaligned. Last week, decided need to make clearer that we can't defend against fingerpritnting from a determined attacker. perhaps a TAG finding that "fingerprinting is bad for the web" for legislators. I added a spec review for the fingerprinting draft in the TAG repo.

Talking about https://github.com/w3ctag/spec-reviews/blob/master/2015/05/fingerprint.md

*mnot:* need more examples of why fingerprinting is a lost cause, put earlier in doc to make expectations more clear. Also, should this be a WG document or just a note? Also talked about mitigations like adding explicit controls in specs for browser to help prevent fingerprinting, ex: browser extensions. 


*dka:* Active, targeted ID/attack vs tracking via fingerprinting seem different

*mnot:* i would include non-cookie fingerprinting as an attack since it doesn't involve user consent. We're always a library away from everyone being able to be a fingerprinting attacker.

*hadley:* do we want to talk about what ppl are currently doing or what is possible?

*mnot:* hard to tell what ppl are currently doing

*nick:* there is limited research on what ppl are currently doing. Active vs passive distinction is relevant.

*hadley:* I really like how mark suggested a TAG finding. I'm confused about the line about W3C thinking fingerprinting is hostile to the web, which makes it seem like we've made up our minds.

*wendy:* i appreciate the attention to fingerprinting and calling it an attack. the TAG is a great place for us to get more privacy user-driven focus. Fingerprinting as a way of identifying a user without consent is subverting the architecture of the web.

*nick:* I think it would be useful to note which things can be done technically and which things can be done through law or regulation. Kind of frustrated about "lost cause" because there are things we can still do.

*mnot:* I'm excited about working on a finding but big question is what is the relationship to your document?

*nick:* I think we can collaborate with you on this document or [...]?

*mnot:* WHen i have something vaguely readable for the finidng, i might just put it up as a gist for people to review.

*wendy:* i try to avoid using the word "consent" WRT fingerprinting

*hadley:* what is the alternative?

*wendy:* I think it needs to be designed at the level of web architecture; users should be able to browse anonymously.

*timbl:* third party cookies; automatically allow cookies for reasonable cases, only ask people about dubious cases

*mnot:* we could have an interesting discussion about the current balance of power WRT cookies; acknowledging we can't do that in the short term. 

*mnot:* re: active vs passive. The document draws a line based on whether code runs in the client. The useful distinction seems to be whether it's detectable.

*nick:* "detectable" is a tricky term. Depends on user's machine. But i agree the main reason we want to distinguish is detectability.

*hadley:* is the question more around the evidence of fingerprinting or where the power is (client vs server)?

*dka:* when you have a browser like tor, that gets in the way of fingerprinting, is that your mental model for detectability?

*mnot:* could be user agent, could be a researcher, etc.

*yan:* prevention doesn't require detection; ex - Tor sets UA string and screen size to the same for all users

*dka:* what to do for mitigation and best practices?

*mnot:* for which parties?

*dka:* spec authors?

*nick:* tor has a doc about sources of fingerprintability in tor browser. minimize entropy and increase anonymity set. there are things we can do to make fingerprinting harder to do in all browsers.  https://www.torproject.org/projects/torbrowser/design/#fingerprinting-linkability

*mnot:* in the past, people come to us with features that add N bits of entropy. But then they say fingerprinting is impossible to prevent. Need realistic advice.

*nick:* would love to see more examples. if a feature adds significant fingerprintability, maybe can turn it off?

*mnot:* agree, can find examples of graceful degradation

*dka:* what is useful for us to do next?

*mnot:* happy to hear what nick wants. as long as people are reasonably happy with the feedback, i think we can let it stand. if we're producing a finding, we can make  a rough draft then figure out the alignment between the two docs.

*nick:* +1. still concerned about "lost cause". 

[more discussion of "lost cause" - important to note that this is for a "determined attacker", similar to pervasive monitoring]

*dka:* modulo minor changes, i think we should consider this document done and work on the TAG finding.

*yan:* fingerprintability != linkability. ex: even if a browser is unique, can't necessarily link it to someone's identity. linkability does not seem like a lost cause.

*nick:* i like the idea of having guidelines on "unnecessary" in the context of unnecessary entropy.

*mnot:* ex - webrtc exposes private IP addresses but people use it anyway.

*dka:* we could open an issue for defining necessary

*dka:* next topic - any comment on media capture and streams? https://lists.w3.org/Archives/Member/chairs/2015AprJun/0017.html

[nothing raised]

*dka:* Meeting adjourned.
