## TAG Teleconference
##### 11-13 May 2020

---

### Agenda:

#### Breakout A (Europe / US) - [2020-05-11](https://www.timeanddate.com/worldclock/converter.html?iso=20200511T160000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Same-Origin iframe document-access limiting attribute](https://github.com/w3ctag/design-reviews/issues/397) - @hober
* [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482) - @hober, @dbaron, @torgo, @kenchris
* [Window Segments API](https://github.com/w3ctag/design-reviews/issues/492) - @torgo, @kenchris, @plinss
* [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris

#### Breakout B (US / APAC) - [2020-05-11](https://www.timeanddate.com/worldclock/converter.html?iso=20200511T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov
* [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @dbaron
* [SM series algorithms in Web Cryptography](https://github.com/w3ctag/design-reviews/issues/491) - @hober, @dbaron
* [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

#### Breakout C (APAC / Europe) - [2020-05-12](https://www.timeanddate.com/worldclock/converter.html?iso=20200512T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [MediaStream Image Capture API PTZ (Pan/Tilt/Zoom feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @torgo, @kenchris
* [AVIF Decode](https://github.com/w3ctag/design-reviews/issues/495) - @cynthia, @torgo, @kenchris
* [Content Indexing API](https://github.com/w3ctag/design-reviews/issues/496) - @cynthia, @torgo, @kenchris
* [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris
* [shortcuts member of Web App Manifest](https://github.com/w3ctag/design-reviews/issues/510) - @alice, @torgo, @kenchris

#### Plenary Session - [2020-05-13](https://www.timeanddate.com/worldclock/converter.html?iso=20200513T200000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage


-----


### Breakout A

Present: Tess, Dan, Rossen, David

Regrets: Ken

#### [Same-Origin iframe document-access limiting attribute](https://github.com/w3ctag/design-reviews/issues/397) - @hober

Tess: this got filed mid last year - has not got attention - no comments from me or lukasz. Shall add Ken?

Dan: yes sounds like a good idea to do that, Tess.

[bumped to f2f]

#### [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482) - @hober, @dbaron, @torgo, @kenchris

Tess: i wonder about the security implications of the manifest and registerProtocolHandler being out of sync...

Tess: Seems like they allow the PWA to handle `https` too, which is worrisome.

Dan: i left a comment and pushed to f2f

#### [Window Segments API](https://github.com/w3ctag/design-reviews/issues/492) - @torgo, @kenchris, @plinss

Rossen: this was discussed at the css f2f a week ago - at this point it's well engaged discussion with the working group. that's the main venue for that work.  The issue that Peter brought up is more general - this explainer doesn't aim to address it.  The main motivation is for portable devices vs multi-screen. As we discussed in the css f2f call - we're not interested in watering down this proposal to address all permutations of devices... use case here is a lot more narrow: portable devices where it's subdived or physical hinged screens...  The overall shape is still being worked on by the CSS working group.  Not quite sure what else we need to... .. one question was making sure foldable devices that have no physical hinge addressed by - in another explainer.

Dan: Kenneth and Diego (from Samsung) are working on [another explainer](https://github.com/SamsungInternet/Explainers/blob/master/Foldables/FoldState.md)...

Dan: so if we don't think there's much to do here we could propose close...

Rossen: overall architecture review and feedback - which was provided initially - is valid.  All of these questions are answered.   From security & privacy, no concerns raised. Remaining work - we trust that CSS wg will do it.

[set to "propose close"]

#### [Navigation to Unsigned Web Bundles (Web Packaging)](https://github.com/w3ctag/design-reviews/issues/509) - @hober, @dbaron, @kenchris

Tess: [venue] - going to IETF ...  have they talked to the IAB?

David: they are proposing a split standardization thing...

Dan: f2f? special guest?

Tess: a good thing to use f2f time...  I'm less worried about it then bundling signed exchanges...

Rossen: we should see what parts belong to "us" and see what feedack we can provide...

Dan: should we get a guest joining? I will invite people...

### Breakout B

Present: Alice, David, Rossen, Tess

Regrets: Peter

#### [CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488) - @hober, @dbaron, @atanassov

David: I emailed Chris Lilley, he responded but I haven't processed his response fully yet. 

Tess: David wrote a comment two weeks ago... 4 distinct threads of conversation in the issue, main reason was to monitor progress on what other parts of the web platform would need to change.

David: Chris filed 4 issues on w3c/ColorWeb-CG on that.

... We might want to bump this to a longer time interval...

Tess: Why don't we add TAG-tracking labels to all the issues on other specs, and track those issues that way?

Rossen: One other concern... harmonising colours and colour spaces across the platform is definitely important, but the other issue was computed values. Can we request computed values in these colour spaces from the OM? What is the implication on how these colour functions become more useful for things like colour contrast and other a11y features?

Alice: Would be nice to get computed values, but David calculated that the L* value isn't useful for that. Might be worth asking the question directly of whether we could have APIs to get computed luminance directly, although there is work in progress (?) on a new contrast ratio computation. https://github.com/w3c/wcag/issues/695

Rossen: Looking at current state of CSS Typed OM, whether or not we are defining typed colour values in a way that we can provide an API to simply compute the contrast ratio. Currently no, simply mapping to CSS Color (rgba) value.

Alice: Would be nice to be able to provide results of colour math specifically for the purposes of computing contrast ratio, but I think that's mostly orthogonal to this issue. For this issue we're probably alright with just adding trackbacks as Tess suggested, and closing the issue.

#### [review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489) - @hober, @dbaron

Tess: David filed this as a result of other design reviews... had implications for the event loop and how things hook into it. Intent was to take a closer look at what's in the HTML spec, figure out if it can be hooked into by other specifications. We haven't done that... think it's a good idea to use some of the f2f to do this, walk through the existing spec. I moved the milestones onto the f2f. Kind of deep dive that f2f time is better for.

David: Sounds good.

#### [SM series algorithms in Web Cryptography](https://github.com/w3ctag/design-reviews/issues/491) - @hober, @dbaron

Tess: This doesn't seem to have a viable venue, given that the Web Crypto WG doesn't exist any more. These specs aren't being maintained, so it's unclear how this change would make it into the spec. Would be nice to get a sense from them that they see a way forward.

David: The WebCrypto group was disbanded because they finished their spec. Probably around 2017.

Tess: [standard complaint re: disbanding groups which define APIs that need to be maintained]

... Already raised the issue about venue in April. Not sure what to do with this.

... We're not the right people to help with process/governance issues, per our charter.

Tess: Let's take this one to plenary.

#### [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494) - @hober, @alice, @kenchris, @plinss

Alice: I've been asking them to flesh out the use cases more. The last comment confused me a litle. Let me see if I can summarize.

...: What is this for? It's for people using web components, to get things on the screen faster, to expose contents of shadow dom to search engines, also serialization and deserialization of DOM which has shadow DOM

...: CSS developers interested in style isolation but using a design system that prohibits JavaScript

Tess: Last point seems to be that there is no way to do style isolation other than Shadow DOM, which requires JS, and some design systems prohibit JS, so there is no way to do style isolation. 

... Only reason they're using Shadow DOM is because of a missing feature in CSS. Not sure it makes sense to add this feature to Shadow DOM solely for this reason.

Alice: the serialization case didn't make sense to me either

Tess: Was imagining a third party... don't have fully worked out example. Non-coordinated serialisation and de-serialisation... 

You're on a page, the page uses a component... you're the author of a tool that page embeds... the tool needs to serialise a chunk of DOM... would be nice to get a "innerHTML on steroids" and then ... do something ... 

... Would need to be deserialised on a page that knew about the component.

Alice: Mason mentions "already hydrated" page for SSR - but would still need to re-attach event listeners.

... Raised concerns about the missing CSS feature, response was that we should fix the problems in Shadow DOM regardless.

Tess: Weird to me to pursue this just for style isolation... if style isolation is the motivation for this, why isn't that same motivation being used for style isolation?

... If we had style isolation as its own independent feature, that might impact the shape of this design. Might affect the syntax of what gets serialised. There might also be other lessons learned from that that might impact the design here.

Alice: Main question for me is how event listeners etc. get re-attached.

Tess: Are you going to end up in a weird state when trying to re-attach those event listeners?

Alice: Let's bump this to the F2F.

### Breakout C

Present: Ken, Sangwhan, Dan

Regrets:

#### [MediaStream Image Capture API PTZ (Pan/Tilt/Zoom feature)](https://github.com/w3ctag/design-reviews/issues/358) - @cynthia, @torgo, @kenchris

Dan: [pings the issue to see if there have been any progress...]

#### [AVIF Decode](https://github.com/w3ctag/design-reviews/issues/495) - @cynthia, @torgo, @kenchris

Ken: [researches ship status in Chromium]

Sangwhan: they wanted to check with Blink owners ... was that thread updated?

Ken: no, not mentioned here...

####  [Content Indexing API](https://github.com/w3ctag/design-reviews/issues/496) - @cynthia, @torgo, @kenchris

Ken: they are waiting for TAG [image resource review....](https://github.com/w3ctag/design-reviews/issues/490)... It's closed...

Ken: they added an abuse considerations section but it's small...

Dan: can we encourge them to think more about  mitigations against abuse?  Should any of the things they've listed be considered to be aprt of the spec itself?

Ken: i think it's difficult...  but the spec should also be part of the spec itself...

[ken leaves a comment]

#### [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @alice, @kenchris

Sangwhan: why does it have to be solved this way?

Ken: when the keyboard appears it resizes the viewport... working around that is relaly tough.. So you rather just want the keyboard to appear on top of the content and not resize... Plus if you have dual screen you also don't want it to resize on the other screen that makes no sense...

Sangwhan: ok

Ken: they did file issues... filed 3 days ago...  They are still working on it. Maybe we should wait for them to ping us when they have an update...

Sangwhan: this does add entropy because of user-installable keyboards. Exposes info that wasn't exposed before.. could be problematic...

Dan: leave for now - let's mark it as pending editor update and bring it up at the plenary

#### [shortcuts member of Web App Manifest](https://github.com/w3ctag/design-reviews/issues/510) - @alice, @torgo, @kenchris

Ken: like "shorcuts" on android... limit how many you can  have... you add on install time... 

Dan: what's the mozilla standards position?  Multi-engine support?

### Bonus issue [payment field optionality](https://github.com/w3ctag/design-reviews/issues/512)

Dan: this looks small

Ken: this looks ok to me maybe we can just pass it and propose close?

Sangwhan: ok with me...

### Plenary Session

Present:  Alice, Ken, Tess, Peter, Dan, Rossen, David

Regrets: 

#### Breakout Rollup

##### Breakout A

Tess:  We added one thing to the f2f and added kenneth.

... URL protocol handler reg for PWAs... We had some questions to reg protocol handler.. We'll talk about it again at the f2f...

... Window segments API... we think we're done and proposed we close...

... Navigation to unsigned web bundles... we could use some f2f time on it - has it got any design review from IAB?  [Dan to also invite people to a session at the f2f]

Peter: do we want to close window segments...?

[yes]

Peter: I can close it.

##### Breakout B

Tess: CSS Color topic... this is proposed close... 

Alice: can someone take computed values back to the CSS wg?

Tess: Talked about HTML event loop... we want to set aside f2f time for it.. deep dive on html spec... moved to f2f milestone.

... web crypto issue.....  There is a clear venue problem... no clear route toward updaing spec.. we'd like to see some progress made... 

... declarative shadow dom...  CSS lacks a mechanism for style isolation - only available with shadow dom [which is overkill] - also bumped to the f2f.

Alice: I had some conversations on that - not just style isolation - people like slotting. That's the other main shadow dom feature they're after.  Also declarative custom elements.  

##### Breakout C

Ken: pan/tilt zoom - waiting from them...

... avif , also waiting...

... Content Indexing ... left some more comments...  We got an update - they expanded 

[we agreed to close this issue with good feedback]

... Virtual Keyboard... adding more fingerprinting surface?  

... Shortucts member of web app manifest...   asking for multi-implementer feedback...

[we agreed to close]

... bonus issue payment field optionality...

Tess: ... think the use case is already satisfied by the 'pending' type of total - might be confusing to also make it optional... hopefully they'll get back to us...


#### [SM series algorithms in Web Cryptography](https://github.com/w3ctag/design-reviews/issues/491) - @hober, @dbaron


... discussion of web crypto...

When the web crypto group closed, they said to send future reqeuests to the public-web-security  mailing list. We are hence going to close this issue and refer the requestor to that mailing list. 




#### Issue Triage

# 511 - Kenneth Self-assigned 
