## TAG Teleconference
##### 24-26 May 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-05-24](https://www.timeanddate.com/worldclock/converter.html?iso=20210524T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman
* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @torgo
* [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov
* [Partitioning Storage, Service Workers, and Communication APIs](https://github.com/w3ctag/design-reviews/issues/629) - @hober, @rhiaro, @ylafon
* [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro


#### Breakout B (US / APAC) - [2021-05-25](https://www.timeanddate.com/worldclock/converter.html?iso=20210525T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia
* [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro

#### Breakout C (APAC / Europe) - [2021-05-25](https://www.timeanddate.com/worldclock/converter.html?iso=20210525T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632)
* [Pre CR review request of CSS Multi-column layout Level 1](https://github.com/w3ctag/design-reviews/issues/634) - @LeaVerou, @torgo, @rhiaro
* [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro
* [Pickling for Async Clipboard API](https://github.com/w3ctag/design-reviews/issues/636) - @cynthia, @torgo
* [HTTP 103 Early Hints](https://github.com/w3ctag/design-reviews/issues/638) - @torgo, @ylafon, @plinss
* [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro


#### Plenary Session - [2021-05-26](https://www.timeanddate.com/worldclock/converter.html?iso=20210526T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Tackling design problems earlier than design review](https://github.com/w3ctag/design-principles/issues/319)
* [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro

* Breakout Rollup
* Issue Triage



-----


### Breakout A

Present: Peter, Tess, Hadley, Rossen, Lea

Regrets: Amy, Dan, Yves, Kenneth


##### [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @hober, @torgo, @hadleybeeman

Moved to next week

##### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @torgo

Tess took a look a the explainer updates, wants to re-review, moved to next week.

##### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

Reviewed some back-channel communication. TC39 meeting tomorrow. Some TAG members will try to attend.

##### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

Still waiting for feedback, punted

##### [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov

Still waiting for feedback, punted

##### [Partitioning Storage, Service Workers, and Communication APIs](https://github.com/w3ctag/design-reviews/issues/629) - @hober, @rhiaro, @ylafon

Punted to next week for Amy's feedback

##### [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro

Existing media queries expose *whether* forced colors mode is on, but computed style can expose the specific colors. Is that an extra privacy leak? 

Tess presents example where specific colors may be set based on screen brightness, which would expose screen brightness.

Lea: But in modern devices where screen brightness is set based on ambient light, that would be a very poor choice for fingerprinting as it would fluctuate all over the place. 

Tess: If it exposes ambient light information that also makes it a privacy leak

Lea: Isn't there an Ambient Light API? 

Tess: Yes, and work has stalled due to privacy concerns! I hope nobody implements it!

... Also, even if another platform feature exposes privacy sensitive info, that is not justification to add this info on other APIs because it makes it harder to get rid of. WebGL example where WebGL is primarily used for fingerpinting. If we use WebGL as justification for exposing sensitive info elsewhere, it means we can't get rid of it by just getting rid of WebGL one day.

Peter: Maybe we should not only discuss this among CSS WG members. 

Discussion follows, with decision to to punt to Breakout C so that others can weigh in


### Breakout B

Present:

Regrets: Amy

##### [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss

##### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia


### Breakout C

Present: Dan, Ken

Regrets: Amy

##### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

[Revisiting situation on Realms proposal in TC39]

Ken: Lea had use cases. Peter had use cases. Domenic had a pushback and an alternartive proposal - callable boundary realms.

Dan: looks like there's a TC39 meeting coming up today and Domenic will join.

Lea: Peter will also try to join.  

Dan: Anything else we can do?

Ken: Let's see the result...

##### [Pre CR review request of CSS Multi-column layout Level 1](https://github.com/w3ctag/design-reviews/issues/634) - @LeaVerou, @torgo, @rhiaro

Lea: if they want to review the spec

Dan: proposed comment:

`Hi @rachelandrew we are just taking a look at this in our TAG breakout this morning. We're trying to figure out how we can best add value. It doesn't look like there's much for us to do. You mentioned interop issues - can you be more specific?  Is there something you would specifically like the TAG's opinion on here? Otherwise we think this is proabbly good to go and we'll close this issue.`

Dan: Posted.

##### [Find the best terminology to restrict the usage of data urls](https://github.com/w3ctag/design-reviews/issues/635) - @torgo, @rhiaro

Dan: missing some context here 

Hadley: "reading systems mush prevent data URLs opening as if they are top level content documents..."

Hadley: why don't we invite someone from the wg to come and chat.

Hadley: [posts comment](https://github.com/w3ctag/design-reviews/issues/635#issuecomment-847666940)

##### [Pickling for Async Clipboard API](https://github.com/w3ctag/design-reviews/issues/636) - @cynthia, @torgo

Hadley: do we need a design principle about using metaphors? E.g. Toast. 

[discussion on use of pickling]

Dan: do we want to bikeshed?

Ken: pickling takes time - i hope this will be a quick operation?

Hadley: we should because we should make it clear that people outside their community will need to use this.

Ken: one concern - say a web site creates a custom format - then other web sites start to adopt this - then it becomes widespread without santization. Is this being restricted to a domain name?  People reverse-engineer formats.

Dan: could lead to a lot of unsanitized content in clipboards...

Ken: right.  

Lea: if the custom format gets sanitized it would have a different mime type - 

Ken: one of the goals is to not sanitized...

Lea: they would have to change their code if the format ever became standardised 

Ken: but could become a defacto standard...  That's a risk because it becomes ...  Example: I'm figma and I allow people to paste javascript because it's in my format. Now someone creates a figma clone. That adds malicious javascript which will be executed in figma if people place it in there.  But if it comes from a different site and there's no way to see where it originates.. needs to be sanitized...

Lea: a little unclear how someone opts in to the pickling... is it based on name?

Ken: they do assume that native apps will support these formats as well.. so that is also a risk.

Dan: the risk is executtable code?

Ken: or triggering code paths that haven't been [locked down]...

Dan: some [worrying stuff here](https://www.w3.org/TR/clipboard-apis/#privacy-events) about the clipboard event API...  Looks like [this issue](https://github.com/w3c/clipboard-apis/issues/52) is still open... not sure what the current state of things is here... Not sure what to do.

Ken: 

##### [HTTP 103 Early Hints](https://github.com/w3ctag/design-reviews/issues/638) - @torgo, @ylafon, @plinss

##### [[css-color-adjust-1] Privacy Impact of System Colors in Forced Colors Mode](https://github.com/w3ctag/design-reviews/issues/637) - @hober, @rhiaro

### Plenary Session

Present: Dan, Peter, Kenneth, Rossen

Regrets: Amy, Lea, Tess, Hadley

##### [Tackling design problems earlier than design review](https://github.com/w3ctag/design-principles/issues/319)

##### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632)

##### Breakout Rollup

Peter: breakout B: realms; digital goods punted; talked about css color adjust - what's getting exposed from fingerprinting pov... implications...   Punted... 

Rossen: here's the to p level summary of 637. If you have a base functionality - a media query - that says "on or off" - based on this you can get some type of info about the user - are they using dark mode or not for example.  You can argue that this is privacy breaching... however after a bunch of discussions it's shipped and adopted - proves to be useful. So we extend it. Now the way we are extending so we can target the system colors - so you can create your site or app to what the native colors look like... 

Ken: in Android the system colors will be adopted to a custom background - so if that's going to be exposed to the web then that's definitely identifying...

Rossen: Don't know if Android is using forced colors and how.. but the issue is you can expose more colors ... what do we return from a get computed style? We could go ahead and return the color itself - you can read back pink directly.  most developer info but highest entropy.  We can lie about the colors - becasue we don't want to expose [this info]. We can just return the keywords of the system colors - "background" or "text color"... so this is where the tech discussion is. We have a media query that was shipped - and on top more things which give more entropy.  So we have the media query - but what about the system colors? Do they expose more info than what we had before?  

Dan: specific colors - could expose very individual fingerprinting info...

Ken: with keywords - you're gonna get some colors from the ststem and the rest ... you need to get the right contrast...

Rossen: we have color mixing capabilities.. the problem is - do we allow easy access to the system colors so people can read back the values of these colors?

Ken: Use case?

Rossen: good use case is - i want to know what your background - to adjust color scheme.  Trying to figure out unique design scenarios where color mixing is not enough... It is going to be harder than if you had the color value itself...

Ken: seems like a really bad issue if we're going to expose colors and they can be read back...

Rossen: forced color mode... capabilities .. have been in windows. Most notable use case - when you're in a windows forced colors mode - an accessiblity application - reduce to a small pallate of colors. 

Dan: contravenes the "don't expose assistive tech" in our design principles...

Rossen: difficult to thread... 

Dan: on/off is one thing - knowing the specific colors is another.

Rossen: or you can say for example - get-computed-style for a particular div and i read its color value - but get back "system background" -

Peter: preventing other channels from getting that info like canvas...  so we'd need to taint the canvas...

Peter: let's come back to it.

[time passes]

Rossen: I don't see harm in exposing the keywords...

Dan: but will need to pay attention to the canvas read issue...  

Peter: set of system colors has been around since the 90s.

Rossen: other possible read-back mechanisms... the values of these system colors should be able to be retreived somehow... they can be mixed, eg. and do math with them.. you will be able to get to the color value.  Usin the keywords you're making that non-trivial.  If we need to go to the next step we can lie about them....  

Peter: **Breakout B** didn't happen.

Dan: **Breakout C** data urls - Hadley posted a comment ; on pickling ..  we bikesheeded a bit on the name.

Ken: also some privacy issues - custom formats can become defacto formats... 

Dan: some issue with clipboard pasting....

Dan: should it behave differently in incognito / private mode?

Rossen: not sure... 

Dan: WWTD - what would Tor do?  They turn off features such as canvas reads...

Rossen: we've arrived at something pretty good here.  We're trending towards lying or using keywords - but still allowing developers to adapt content to match system colors.



Dan: [**user preference media features client hints headers**](https://github.com/w3ctag/design-reviews/issues/632)

Dan: why a client hint?

Rossen: media query not performant enough...

Peter: bit of a stretch... if you're putting everything in style attributes...

Dan: worried about the poliffieration of client hints...

Ken: it's an addition to something else - there's always another way to accomplish the same... Same with manifest... should always be another way to do it. 

Dan: that could be a good design principle.

Peter: it's front-loading info that you could get later in a handshake...

[discussion on why not all media queries?]

Peter:  who not viewport size, color depth, etc.. 

Rossen: in terms of evasion - this capability will allow me to fingerprint the device and the user settings and evade and serve complete different content - phishing content.   If I have bots and other infra that is used to detect phishing web sites - this will make evasion easier. You don't have to send any bytes at all.. 

Rossen: whole bunch of scanning and bots that are constantly indexing content to see if it's safe or not. Detecting phishing, malware, etc... This is gonna make it easier for them to evade.  So I'm not motivated by this one.

Ken: it's about getting resources...

Rossen: they want to reduce bandwidth - on the server side.

Peter: reducing bandwidth for the client has a huge benefit.



##### Issue Triage

