# TAG Teleconference
#### 15-17 April 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-04-15](https://www.timeanddate.com/worldclock/converter.html?iso=20240415T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @ylafon, @maxpassion
* [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion

### Breakout B (California / Europe)  - [2024-04-15](https://www.timeanddate.com/worldclock/converter.html?iso=20240415T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk

### Breakout C (California / Australia) - [2024-04-15](https://www.timeanddate.com/worldclock/converter.html?iso=20240415T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk
* [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### Breakout D (California / Australia) - [2024-04-16](https://www.timeanddate.com/worldclock/converter.html?iso=20240415T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

### Breakout E (Europe / China) - [2024-04-17](https://www.timeanddate.com/worldclock/converter.html?iso=20240415T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* ¯\\\_(ツ)_/¯

### Plenary Session - [2024-04-17](https://www.timeanddate.com/worldclock/converter.html?iso=20240417T200000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)


-----


## Breakout A

Present:

Regrets:


### [Local Peer-to-Peer API](https://github.com/w3ctag/design-reviews/issues/932) - @ylafon, @maxpassion

### [Updated review of WebNN API](https://github.com/w3ctag/design-reviews/issues/933) - @torgo, @matatk, @maxpassion


## Breakout B

Present: Peter, Lea

Regrets: 


Deferred to C 


### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

### [Early TAG review request for Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939) - @hober, @matatk


## Breakout C

Present: Peter, Tess, Lea

Regrets: Martin

### [Web Install API](https://github.com/w3ctag/design-reviews/issues/888) - @hober, @LeaVerou


Questioning what a manfest id is, and why use that instead of a url to the manifest.

Questioning why cross-origin re-invents a CORS-like mechanism for install sources.

* Discussed that the web needs a cross-server mechanism to declaratively set server beahviors, like setting headers.


Issues:
- Separate the two reviews

Same-origin:
- Related apps doesn't make sense without cross-origin version of the API

Cross-origin:
- CORS vs manifest fields
- What is a manifest id?


### [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo

### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @hober, @matatk

### [Document Render-Blocking](https://github.com/w3ctag/design-reviews/issues/886) - @hober, @LeaVerou

### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss


## Breakout D

Present: Dan, Matthew, Peter, Tess, Diego Gonzales, Lu Huang, Dan Murphy, Lea, Yves

Regrets:

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Lu Huang: web app windows do this thing when you navigate outside the scope - or outside the origin - a big warning bar - the warning "you've gone somewhere else" the button "do you want to go back"? Some people say this is not desirable... because the webapp owner also owns the other domain...  You can tell your webapp that these origins are also aprt of the app.

Dan Murphy: concrete examples - if you've tried to use slack as an installable webapp - there's always an issue with different origins for multiple orgs...

Tess: i don't think that happens when you add slack to a webapp on the doc in safari in macos....

Dan Murphu: slack may have changed... maybe safar is operating in a different way .. i know safari doesn't show the banner for login pages... when to do out of safari and when to stay in the app... the way that scope is defined needs to be in the same origin no way for it to be visible without 

Dan: Embedded content as well?

Lu Huang: to me, it's similar to being not in a webapp window just in a browswer window... you navigate to another site and no alarm bells go off.  For the implementation in chromium we show the user the (new) orgiin and also have security & origin info in the main menu in the webapp window...  In this issue what

Lu Huang: iframes would work exactly the same way - everything we're talking about here is top level navigation... even then when you navitage to the new site it doesn't inheret any preferences...

Matthew: slightly related: we've been having conversations about heuristics ... might be something in relation to that...

Dan Murphy: there's product and then web platform... if there's a navigate=self link that navigates to the current document... this feature is all about the primary browsing context... the web content is in this other frame... Worst case scenario might be: a link in mastodon... there's a link in that page to another origin and it's a navigate=self link... user clicks on that, it goes to a different origin,... worst case scenario is .. mastodon.com origin says x.com is part of me, x.com says mastocon.com is part of me... In that case no notification would show...

Yves: what is the implication of considering that the application encompass other scope? sharing data between different. 

Lu Huang: no tha's not part of the proposal... 

Peter: is that always going to be clear to the user?  I start out on one site and I move to another site that is related?  Is that going to be clear to the user?  Even if that's not the intent then we have a concern that someone will try to 

Dan Murphy: the requirement for this feature is establishing an edge on a graph of origins - in a way that is safe... the feature needs that so we don't show the security boundary... 

Peter: if you navigate to another origin and it's not displaying a URL bar... 

Lu Huang: usually a clear origin that is asking for microphone or location permission... The UI should always make it clear. That's a reasonable thing to recommend in spec language.  Also a way for the user to look up where am I...

Dan: Murphy - we can say "this is not an extentison of storage, or permission" .. 

Peter: still concerned - the permissions case - most users don't understand the concept of origin so we need to be careful how we expose... maybe we should double-key these permissions... 

Lea: reading the goals it reminded me of first party sets, related website sets...

Lu Huang: it's been suggested we look at that but related website sets does too much - has security implications we don't want.  It works at the domain level.  We can't use it to put together a set of subdomains..  For this set we have tried to not change assumptions aboue security, permissions, storage... not changing the model at all.  Strictly talking about webapp features...  The one effect we're talking about ... just the UI around the cct - custom tab bar - warns you that you're out of scope... Maybe there reasonable other webapp features to add to this...

Lea: my concern is that we don't want a bunch of differen to APIs to declare the same intent... should only declare this once... should not have to scatter this through multiple different APIs...

Dan Murphy: this is constructed for "manifest entities" a manifest isn't a whole origin it's often a subset of an origin... Really it's just a message to the user agent... file handlers is an example of a feautre added to manifest... I agree it's annoying that there are too many concepts. This one is specific to manifest files... tied to a specific app... ID that is specified there... In terms of furture APIs ... don't see any APIs that it makes sense for..  Chrome may have wanted to ehhance the user experienced based on this manifest entity...

Lea: once this ships if it enables certain permissions... scope has a certain meaning...   Concerned about the increase in API sufrace area for declaring similar things.

Yves: if you have different origins 

Lea: looks like this also specifies domains but also specifies subdomains as well?

Lu Huang: right now the entries are origins... we want it to be able to support more specific path filtering... we don't know what the right syntax is... URLpattern is supposed to solve that. but does it translate well to native for differnt to operating systems?   Does it translate to OS specific registrations. We split it into two problems.. 

Lea: right now all the examples related to URLs... is there an example that shows an OS specific scope?

Lu Huang: as it stands web app scope is single origin and some path with the single origin..  if we make webapp scope more complicated then it's whether you can translate it to things you care about in operating systems... future concerns...  that's why we didn't include a filtering syntax...

Lea: but wildcards are such a syntax.. if anything it seems to me that example under number 1 that could be a single URL pattern...

Yves: in service worker the patterns are similar for performance reasons...

Lea: we don't want multiple related patterns... different microsyntaxes for URL patterns...

Lu Huang: good point..

Dan Murphy: no way to parse that syntax right now .. our feedback was to make a separate entry for eTLD+1... happy to have other ways... it should be parsable by spec... simplest way to do what our partners need...

Lea: if the pattern is that URLpattern is more broad... you could just say that's it's a URLpattern with only host or only origin keyword... you can define that pattern as a hostname pattern...

Lu Huang: the examples are meant to be origins...  the scheme is assumed to be https given that webapps only care about https urls...  even if we set the same limitations - should only be an origin - we can still express that in terms of URLpattern...

Lea: yes because users can learn that only once...  my cocnerns are (a) the patterns and (b) yet another API to 

Dan: *developer complexity*

Lea: for smaller teams if you have to maintain a list of domains in different places... concerned about keeping those in scope...

Dan: other than fps ... related web sites .. is there anything else?

Lea: maybe a a CORS extentension?  actual intent authors are trying to express ... how does this web site relate to other origins..  can they navigate, install, etc...

Lu Huang: CORS extension has not come up... I wonder how it would make a relationship between an APP ID and an origin... scope extensions can be split into 2 parts... what you do with it and what the webapp manifest says... not married to a brand new association format, but of the things we looked at there wasn't one that satisfied our requirements... we can have this without being fixed on one things...

Lea: this seems to keep coming up so maybe work with the first party sets people....

Dan: *webapp manifest files vs. http headers*

Lu Huang: I think the maifest is the right surface to have that... I think our discussion ... for those origins to confirm they want to take part in this... do they want a .well-known config file... cors header... the related website thing doesn't work... heavy burden... you have to apply to get your configurations...

Lea: i think the permissions should be explicit...  Right now as someone reading the manifest ... unclear what these permissions are... can they change... what if the API made this explicit... these origins share these types of permissions... 

Lu Huang: tagging syntax... can we also add tags there... the syntax is extensible... 

Dan Murphy: I think we want to be ware of permission grant... my interpretation of the feature is that this tells UAs about a feature.. but could also be useful for install...



## Breakout E

Present:

Regrets:



## Plenary Session

Present: Martin, Amy, Peter, Matthew, Yves

Regrets: 


### Breakout Rollup

#### Breakout A

#### Breakout B

#### Breakout C

#### Breakout D

#### Breakout E

### Issue Triage
