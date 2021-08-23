# TAG Teleconference
#### 16-18 August 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-08-16](https://www.timeanddate.com/worldclock/converter.html?iso=20210816T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss
* [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov
* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @kenchris, @hadleybeeman, @atanassov
* [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov
* [Review Reqest: CSS Fonts src: descriptor syntax for client side font selection](https://github.com/w3ctag/design-reviews/issues/666) - @LeaVerou, @kenchris, @atanassov

### Breakout B (US / APAC) - [2021-08-17](https://www.timeanddate.com/worldclock/converter.html?iso=20210817T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober, @cynthia
* [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov
* [Review Request for prefers-contrast media query](https://github.com/w3ctag/design-reviews/issues/663) - @hober, @atanassov

### Breakout C (APAC / Europe) - [2021-08-17](https://www.timeanddate.com/worldclock/converter.html?iso=20210817T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [JPEG XL decoding](https://github.com/w3ctag/design-reviews/issues/633) - @cynthia
* [Review of AccessHandles for the Origin Private File System ](https://github.com/w3ctag/design-reviews/issues/664) - @cynthia, @kenchris

### Plenary Session - [2021-08-18](https://www.timeanddate.com/worldclock/converter.html?iso=20210818T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Peter, Tess, Lea, Amy, Rossen

Regrets: Yves, Dan, Ken, Hadley

### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss

Peter: looks like we're waiting for input from them

Tess: update a month ago about an update to the explainer that should land.. they did make three changes in august but not to the explainer

Peter: Let's check in in a couple of weeks, and if not, face-to-face

### [Anonymous iframes](https://github.com/w3ctag/design-reviews/issues/639) - @hober, @hadleybeeman, @atanassov

Rossen: last time we talked I felt like we went through the document fairly extensively, there was a bunch of us, Hadley and I had three meta questions around usre needs, security and privacy and the overall scoping of that into the set of other documents and other proposals. I see that Camille has put another document which I haven't had a chance to look through. Sounds like they are trying to list here a number of challenges rather than user secnarios.. around popups and subresources and third party iframes and how that solution is going to address those. I haven't had a chance to digest this. From actual end user point of view scenarios it's still doesn't feel this addresses what Hadley was asking for. THeyr'e saying they've identified some problems.. but are these problems that people are fine with? They coudl be problems and nobody cares. Identifying them doesn't make them good use cases. They're using these pivots to fit what they're proposing, not necessarily the conversation around scenarios or uses cases that sucks today and they're going to make it better. Like "we're going to get rid of popups." That would be something I'd be excited about... or "we're going to solve auth and single sign on forever"... That is my take on this through reading quickly the first few paragraphs. They go on to say how their solution is solving this becuase they explain how their solution fits these problems.... I'll ping Hadley and work out another response. I don't see how the user needs are expressed, even if the users are web developers.

Peter: it seems like a mechanism for creating an iframe without having to do all the CO* headers and still get some of that behaviour. Am I reading that correctly?

Rossen: generally yes.. Is there a task force on iframes?

Tess: not that I know of

Rossen: that's what Hadley said.. to help bring that together we will be recommending a task force on iframes.. 

Tess: first I've heard of it. What WG would the task force be under?

### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Lea: both Tess and I pinged several people but none of them have commented. Punt it more? We've had input from various people, but none of the people we actually invited

Peter: push it another week or two? Ping?

Lea: I don't know how to get these people, we have pinged them. Some other channels? We could punt and see what happens

### [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @kenchris, @hadleybeeman, @atanassov

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650) - @kenchris, @atanassov

### [Review Reqest: CSS Fonts src: descriptor syntax for client side font selection](https://github.com/w3ctag/design-reviews/issues/666) - @LeaVerou, @kenchris, @atanassov

Lea: Chrome is interested in pushing this forward fast

Rossen: I'm very aware of the origin of this work, but not familiar with the current exposure through CSS. The color v1 format stuff and some of the addtiions that they were intending to add for colour fonts and added gradient support which is going to bring that work close to the capabilities of things like svg fonts on the lower font capability level. Sounds like they want to expose this through CSS afterwards. Sounds pretty good to me.

Lea: I was not involved in the CSS WG discussions. I just caught up today. This is not about adding specifically capabilities, this is about adding feature detection for these capabilities so that authors can load different font files depending on what the browser supports. Right now even though these technologies are designed to be forwards compatible and you can load a colour font in browsers that don't support it you probably don't want to load huge files in browsers that can't take advantage of them. There is no explainer.. I needed to do some hunting down to figure out examples of usage and user needs.. After this digging, I do now think there is a strong need for this. A bit skeptical about the syntax, though CSS WG specs are often well thought out so maybe I'm missing something. Currently CSS has an existing feature detection mechanism (@supports) and this is adding an entirely separate microsyntax. I personally find it hard to read. First, it is just a list of keywords with no hierarchy: format specifier, supports keywords, and feature detected features all look the same. But primarily, it's unclear whether this is a feature detection for the browser or telling the browser what the font can do. I know which one it is after reading, but just looking at the syntax, I wouldn't know what it does. My bottom line is the functionality is needed, not sure about if this is the best way to expose it.

Rossen: I'm going to ask for an explainer. 

Lea: the spec itself only has one example.. revisit in plenary to see if they provided explainer?

Rossen: if this is time sensitive hopefully they will get back to us

Peter: about the supports mechanism.. if you don't have the microsyntax in the source description, how would you do it? Wrap font face in an @support rule?

Lea: we resolved to be able to nest @supports rules inside regular rules, so we could also allow them inside @font-face. I posted [a proposal](https://github.com/w3c/csswg-drafts/issues/6520) about this to the CSS WG repo after looking at this, with my CSS WG hat on

Peter: putting @supports around the individual descriptor?

Lea: yep, and current browsers only get rid of the @supports rule, not the entire @font-face rule, so it is backwards compatible. I must be missing something.. we'll see.

Peter: normally @supports doesn't dig into these microfeatures

Lea: See, it was originally designed for property value pairs but it does have a selector() function.. so it does allow for testing specific capabilities.. you could conveive a font-technology() function or something like that. 

Peter: my extremely weak argument would be you can make the same argument for the format of the descriptor, that it should be in a supports rule around it

Lea: the format predates @supports by many years

Peter: I'm sure it does.. but as far as the mechanism goes, it's six of one and half a dozen of the other.. not disagreeing.. just looking from all angles. I think I tend to agree we should keep supports like things in @supports

Lea: if we only have one feature querying mechanism in CSS that would be a good thing

Rossen: we definitely need to exhaust the possibilities of @supports before we consider anything else

Lea: looking at discussions, I didn't see one about using @supports. All about do we use the format function or a separate supports function inthe src descriptor... am I missing something obvious? to nest conditional rules inside other rules is fairly recent

Rossen: a couple of conversations here.. one around whether or not this capability makes sense and the approach for this feature is a good addition to the overall platform. That's us saying yes or no.. the other discussion is all of the details and how we're going to spec this out in CSS WG. We will go and do that in CSS WG, we'll make sure that @supports is the way to go and why is this not considered. I don't want us to come too heavy handed from the CSS pov in terms of feedback here

Lea: we don't want to design the feature

Rossen: right..

Peter: there were some resolutions in CSS WG about adding this.

Lea: it is part of the fonts 4 spec, no implementations yet. Definitely part of the draft. Since there's no explainer we can wait until plenary.

Rossen: knowing how much push they have on the lower font capabilities this is the icing on the cake. They are at the final stretch with all of that work. It's good to see that come together.

Lea: this functionality is really needed

### [Review Request for prefers-contrast media query](https://github.com/w3ctag/design-reviews/issues/663) - @hober, @atanassov

Rossen: another without an explainer... "see the specification"... this is a differential review based on [#583](https://github.com/w3ctag/design-reviews/issues/583). Having a hard time figuring out what changed.

Tess: I don't understand how this custom value isnt just a rename of the old forced value.

Rossen: we had a long conversation.. with that naming we were able to come around and have good enough consensus in the CSS WG. 

Tess: i'm going to post a question in [CSS WG issue 5433]()... most recent conversation at the end of 6036... pinged on that.. there's an implication that operating systems have a pretty big space in between what would match more and what would match less. Some value in having a value that matches in between them. If I read correctly.. windows matches high when it's a contrast ratio of 7:1 or higher, whereas on mac it's 4.5:1 or higher. Maybe it's less clear if there's a value in having that middle value on platforms where high contrast isn't that high? Or low isn't that low. I'm happy to defer to James on what would make sense of any of our platforms.

Rossen: how does that fit into what we're asked to review here?

Tess: I love the comment you already made, asking for an explainer. When they have one it'll be nice to see how they talk about this. I think we can leave it at that.

## Breakout B

Present:

Regrets:


### [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober, @cynthia

### [Capability Delegation](https://github.com/w3ctag/design-reviews/issues/655) - @atanassov



## Breakout C

Present: Sangwhan, Ken, Hadley

Regrets: Yves, Dan, Amy, Lea


### [JPEG XL decoding](https://github.com/w3ctag/design-reviews/issues/633) - @cynthia

Ken: Looking at this, it seems that we have given advice (no more mime sniffing) and that it is being discussed by the right people in the mime sniffing repo

Ken: propose close

### [Review of AccessHandles for the Origin Private File System ](https://github.com/w3ctag/design-reviews/issues/664) - @cynthia, @kenchris

Ken/Sangwhan: We looked at it during our breakout today, the proposal and problem statement looks good to us. We'll discuss this further in the plenary and see if we can close this.

### [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @kenchris, @hadleybeeman, @atanassov

Ken: Thanks for the explainer. Looking at the future considerations section, I am wondering whether this is flexible enough. Why does creating a new note have to result in a URL change? I could imagine a canvas app, where I would just add a graphical overlay (post it notes) on top. Could this be a global event instead where you give the options (including future ones) as part of the event details? It doesn't look like you considered this. We would like to hear your thoughts on this.

### Capability Delegation - @atanassov

Hadley: Can advertisers ask top-level sites to give them this permission, and get more control than they have now?

Sangwhan: Let's say news.com embeds ad script from evilads.com, then everything hte evilads.com asks for is provided to news.com. I'ts problematic because the news site is asking for permission when in fact hte avertiser is asking for it.

Ken: UI could show what's actually happening?

Sangwhan: could make delegation transparent.

## Plenary Session

Present: Peter, Rossen, Lea

Regrets: Yves, Dan, Amy, Kenneth, Sangwhan, Hadley

### [Review Reqest: CSS Fonts src: descriptor syntax for client side font selection](https://github.com/w3ctag/design-reviews/issues/666) - @LeaVerou, @kenchris, @atanassov

Rossen: Adding comments and closed.

### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

### Issue Triage
