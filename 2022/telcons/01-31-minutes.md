# TAG Telecons Week-of 31 Jan 2022

## Call Agenda

### Breakout A (Europe / US) - [2022-01-31](https://www.timeanddate.com/worldclock/converter.html?iso=20220131T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @kenchris
* [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @kenchris, @hadleybeeman
* [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @torgo, @rhiaro, @hadleybeeman, @plinss, @atanassov
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @kenchris, @plinss, @atanassov
* [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @kenchris, @plinss, @atanassov

### Breakout B (US / APAC) - [2022-02-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220201T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @cynthia, @rhiaro, @hadleybeeman


### Breakout C (APAC / Europe) - [2022-02-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220201T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Pen Events API](https://github.com/w3ctag/design-reviews/issues/553) - @cynthia, @kenchris, @atanassov
* [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou
* [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro
* [Credential Management: Conditional Mediation](https://github.com/w3ctag/design-reviews/issues/692) - @torgo, @rhiaro, @hadleybeeman
* [ObservableArray, and its use by adoptedStyleSheets](https://github.com/w3ctag/design-reviews/issues/693) - @LeaVerou


### Plenary Session - [2022-02-02](https://www.timeanddate.com/worldclock/converter.html?iso=20220202T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22)
* Council(s) latest news and discussion

## Minutes 

### Breakout A (Europe / US) - [2022-01-31](https://www.timeanddate.com/worldclock/converter.html?iso=20220131T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Hadley, Yves, Tess, Peter, Rossen
Regrets: Lea

#### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662) - @torgo, @kenchris

[assigned rossen - will look again at the plenary]

#### [Secure Payment Confirmation - Part 2](https://github.com/w3ctag/design-reviews/issues/675) - @hober, @torgo, @kenchris, @hadleybeeman

[reviewing Ian's last comment](https://github.com/w3ctag/design-reviews/issues/675#issuecomment-989036837)

Tess: [regarding some of the feedback on this issue] (speaking about pragmnatism)

Hadley: in discussions with the automotive wg we still pushed them to be more webby.

Tess: the working group has taken [the] feedback and agreed to disagree ...

Dan: Ok we need to review the videos and the spec links that he's provided.

[we will try to make headway at the plenary]

#### [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @torgo, @rhiaro, @hadleybeeman, @plinss, @atanassov

Hadley: reviewing a comment that came in...

[discussion of sync fabrics]

Tess: regarding e.g. iCloud keychain - Apple doesn't have access to contents of the keychain. Only your devices have access because they're in the same ring of trust.

Hadley: from a user perspective -I have to trust that Apple has done that.

Tess: yes you have to trust the company that built it. Different companies have different ways of demonstrating they are worthy of that trust.  Apple makes some kinds of devices available to security researchers.  People in in the industry can review that research.

Hadley: makes me wonder if we should recommend to the working group a checklist - if a key sync fabric provider meets these criteria then they can be said to be compliant with the spec. E.g. letting independent researchers have a look.

Tess: yes it would make sense for the working group to have that .. best practices. And notes for auditing. If you're been charged with evaluating .. then you should look at xyz.  A little concerned - hard to have the working group require.

Hadley: problem I'm trying to solve: me as a user - i see the web site I want to log into has implemented this new version of webautn and I want to know if I should trust it. I have nothing beyond the reputation of the browser / key syncing company...

Tess: also true for Yubikey...

Yves: if the key is stored in the browser then you have to make sure you're trusting the browser maker. 

Dan: browsers should be able to interoperate with multipls 3p sync fabrics?

Hadley: they are talking about the phones...

Tess: you can still use hardware security keys -- but that won't sync across a sync fabric.  It's not a replacement - it's an alternative.  Some might say "in order to access this you have to have a physical key" - but for the common case - vast majority don't have a hardware key... A feature like this opens up webauthn to be used in a wider context (so it can displace passwords).  We should welcome an effort to reduce that threat.

Dan: [raising issues of requests from governemnts to providers of key sync fabric]

Tess: we can't address policy issues.

Hadley: potentially opens up users to ...  Feels like we need external credentialling.

Tess: For centralizing - sympathetic - we require our browsers to have 3p architetcure for these things - then a less scrupoulous company implements one - and they use it to snarf up your credentials - now they can impersonate you wherever they want.  So there's a concern but remedy might be worse.

Tess: ... or governments.

Hadley: similar issue of using phone OS as credential storage fabric - you still need to trust your phone OS.  There are lots of phones out there on old versions of OS or less maintained forks... 

Peter: interesting option - you can build a system where you have a hardware key that you use to sign your syncable keys - so the system lets you log in with any key signed by that key. You have your phone and you have your ubikey - once a month you can re-gen the keys but they expire...  Device key extension - might be this. 

Dan: we can ask them about key sync fabric providers.. we can ask them about device key extension... 

Tess: his is a decent overview video btw: https://developer.apple.com/videos/play/wwdc2021/10106/

````
Hi @agl. We are discussing this in our W3CTAG breakout today.

This has generated an interesting discussion, and we have a couple of questions you may be able to help with.

1. **How safe are sync fabric providers?** We talked through a number of scenarios in which this could fail to protect users: 

* one where the sync fabric provider has access to the credentials themselves and abuses them, 
* one where authorities could serve warrants on sync fabric providers and gain access to all of a user's accounts, and
* one in which an unscrupulous but widely-used site requires that users use their sync fabric to log in — and then they have access to all of that user's accounts. 
  
Have you and the working group considered these types of scenarios? What sort of mitigations might be added to the spec or the ecosystem to protect users from scenarios like these?

2. **Can you say more about device-key extension?** We were intrigued with the protections that come from pairing syncable credentials in a phone or sync fabric to an automatically-generated, device-bound key pair. Would you imagine those keys expiring regularly (monthly or weekly, etc)? And while this clearly mitigates some of the danger to the user (their older credentials would no longer be available, should they be exposed or exfiltrated) — how much damage could still be done if credentials were leaked before they expire? And are there other ways to protect users in this scenario?


````
Dan: +1
Peter: +1
Tess: +1
Rossen: +1

#### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @kenchris, @plinss, @atanassov

#### [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @kenchris, @plinss, @atanassov

Rossen: will drill down on this - what does he mean on additional privscy characterics that are not already exposed through viewport or screen API.

Dan: why are there 2 reviews here?

Rossen: one is a subset of the other...

Dan: we've gone through the major bits of the revieww on both and it's been largely positive.. maybe we can shoot to close these at the plenary?

### Breakout B (US / APAC) - [2022-02-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220201T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Hadley, Rossen
Regrets: Lea, Max

#### [Pen Events API](https://github.com/w3ctag/design-reviews/issues/553) - @cynthia, @kenchris, @atanassov

#### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

#### [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @cynthia, @rhiaro, @hadleybeeman

Hadley: Left this comment:

````
Looking at this in our W3CTAG breakout session.

Just noting that in two of the issues that @rhiaro opened, the working group minutes (mentioned in @iherman's reply) indicate that they are planning to address them and will get back to us.

And it doesn't look like there is any comment yet on the third: [TAG] Reading systems and permissions prompts #1958.
````


### Breakout C (APAC / Europe) - [2022-02-01](https://www.timeanddate.com/worldclock/converter.html?iso=20220201T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Dan, Sangwhan, Yves
Regrets: Max

#### [Pen Events API](https://github.com/w3ctag/design-reviews/issues/553) - @cynthia, @kenchris, @atanassov

Dan: this goes way back.. Recently the requester got back with more information

Sangwhan: Design been ossified... 

Dan: so should we close? Should we say we're not satisfied because they won't make changes? Are they fundamental or API shape?

Sangwhan: API shape.. pointer events already exist, but they're using a different delivery mechanism for button events. You have to listen to a different set of events, seems inconvenient. They say it's a better semantic match to mint a new set of events. Pen buttons are a very specific use case. I'm not sure we warrant that. But it's not the end of the world. 

Dan: sounds like **resolution ambivalent**? And a closing comment with those points.

Sangwhan: they're imposing a windows specific implementation detail into the api surface. I can write a closing comment.

Dan: we could say we don't think it w ould be harmful but we think it could be better and we're disappointed our feedback hasn't been received

```
Thank you for getting back to us, and apologies this took so long. While we aren't entirely satisfied with the outcome of the discussion, we also would prefer not to block work from happening. If you have future iterations which warrants a second round of reviews, feel free to request us to reopen. Thank you for bringing this to our attention.
```

**closed with above comment and status of ambivalent**

#### [Compute Pressure API](https://github.com/w3ctag/design-reviews/issues/621) - @LeaVerou
#### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro

Amy: we asked for updated explainer and privacy & security. No update yet. They said they hope to reach an agreed api shape in january or earlier with webrtc wg so we could ask about that

Dan: [writes comment]

Sangwhan: trying the demo, it makes perfect sense what they're doing here

#### [Credential Management: Conditional Mediation](https://github.com/w3ctag/design-reviews/issues/692) - @torgo, @rhiaro, @hadleybeeman

Sangwhan: curious about other stakeholders / web authn in general.. Is any other browser interested in webautn in the first place?

Dan: I was starting to see so many things about webauthn so I bought a yubikey.. I found it working with safari on mac and iOS, and on samsung internet (behind a flag) and I found it surprisingly easy to get it to work with the nfc mode and the usb mode. It looked like twitter and github are supporting it from a UI perspective, I know google is, lots of other websites do. Looks like it's a thing. The other issue we discussed in breakout A was about expanding the use of non hardware key based solutions for storing key material to encourage greater adoption so you could really use it as a replacement for passwords, eg. if you have sync between different devices, and how does that play into this secure side of it because then you have to trust a sync provider in order to .. It' sspecifically about how the web ui can lead a user into an experience where they're more likely to adopt webauthn. The main issue we raised before was more a privacy related issue. Does this conditional UI provide additional information to the website about whether or not the user already has what type of key they have or what type of credentials they already have, and I think the answers we got are pretty good. And they've updated their explainer privacy considerations. I'm happy with these responses.

Amy: looks good to me

Sangwhan: seems sensible

Dan: [leaves comment]

**closed**

#### [ObservableArray, and its use by adoptedStyleSheets](https://github.com/w3ctag/design-reviews/issues/693) - @LeaVerou

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22)

**we triaged some stuff**

### Plenary Session - [2022-02-02](https://www.timeanddate.com/worldclock/converter.html?iso=20220202T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Amy, Peter, Dan, Yves, Rossen
Regrets: Lea, Max, Hadley

#### Breakout Rollup

Dan: in breakout A we talked about gamepad, looking again at the plenary but that was based on Rossen being here. Secure payment confirmation but we're not in a position to make headway. WebAuthn was a good discussion. Hadley left a comment, they replied. Also talked about talking more about viewport segments and foldable device at plenary, but will reset for next week.

Peter: breakout B... Hadley made progress on EPUB.

Dan: in C we talked about pen events API and closed it ambivalent. Credentials management we closed with a positive response. It's related to the wider discussion about WebAuthn. And did some Triage.

#### Broadining the user base of WebAuthn #686

Dan: we had a [comment back](https://github.com/w3ctag/design-reviews/issues/686#issuecomment-1027197167) responding to Hadley. Pushing back on the idea of normative requirements about safety.. The question is not about desigining UI, it's about ensuring that it's secure, which means thinking about scenarios.

Peter: where is he talking about UI?

Dan: ...HTML5 mandated designs for passowrd manages.. misconstruing comments as about user interface..

Peter: I think that's about how password managers store passwords, not UI. Accepting an issue, but that it's an issue for implementations and not the spec

Amy: a spec could make recommendations for best practices...

Peter: talking about 3rd party systems outside the browser that you can't really control. But agree there's no reason the spec can't make strong recommendations

Rossen: when we talk about secret management and usage that goes through our api layer, on one side you have systems that are capable of managing and storing secrets, regardless of where this is, on device or off device or generated on the fly. On the other hand you have all of those secrets used by the user through all of these apis to be able to provide them to a different set of services. That's in a nutshell the management and flow of data we're discussiong. I do'nt know we can make very strong recommendations on either of the two sides outside, storage and retreival management as well as how those secrets are used afterwards. If I read adam's respone he seems to be threading a similar line. Which is we can say please be good but that's about it. Please don't do bad things. That's how these recommendations read. If we have to be more precise and technical we can go down the path of specifying exactly how secret retrieval and storage is encrypted and how that can be made secure. But I don't know we can make a strong case on the other side to say when you store those secrets they need to be stored in a certain way. For the same reason we don't demand how netflix stores their content before they deliver it to the user.

Dan: this is something that changes the se

Rossen: if that's where we draw the line - this path doesn't seem to be good for us - doesn't meet the same guarantees to the user.  

Dan: it feels to me that the spec itself could help mitigate the gap between the secruity guarantee of webauthn with a secure key vs. with a synced key... - either through best practices or requirements.

Peter: 2nd half of response dealing with device keys... his response - sounds the opposite to what I was thinking?

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22)

#### Face to face

We take a firm decision at plenary in 2 weeks time to see if there are enough people who aren't definite nos to go ahead.

#### Council(s) latest news and discussion
