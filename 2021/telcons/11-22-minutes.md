# TAG Teleconference
#### 22-24 November 2021

---

## Agenda:

### Breakout A (Europe / US) - [2021-11-22](https://www.timeanddate.com/worldclock/converter.html?iso=20211122T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss
* [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @kenchris, @plinss, @atanassov
* [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @kenchris, @plinss, @atanassov
* [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @hadleybeeman, @plinss, @atanassov
* [WebAuthn minPinLength](https://github.com/w3ctag/design-reviews/issues/687) - @torgo, @hadleybeeman
* [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov

#### 2nd Half - With Guests

* [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov

### Breakout B (US / APAC) - [2021-11-23](https://www.timeanddate.com/worldclock/converter.html?iso=20211123T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

n/a

### Breakout C (APAC / Europe) - [2021-11-23](https://www.timeanddate.com/worldclock/converter.html?iso=20211123T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov
* [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @rhiaro, @hadleybeeman
* [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @torgo, @kenchris
* [Feature policy for Keyboard API](https://github.com/w3ctag/design-reviews/issues/685) - @cynthia, @torgo, @ylafon, @atanassov
* [Web App Launch Hander](https://github.com/w3ctag/design-reviews/issues/683) - @kenchris, @hadleybeeman

### Plenary Session - [2021-11-24](https://www.timeanddate.com/worldclock/converter.html?iso=20211124T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


## Breakout A

Present: Peter, Dan, Yves, Lea, Amy, Rossen

Regrets: Tess, Hadley

Guest: Thomas Steiner (Google) for discussion on User Preference Media Features Client Hints Headers

### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss

Dan: one of the quesitons was to do with trusttoken being based on top of privacypass, an ietf spec. It was not clear what mozilla's disposition toward privacypass is. I marked it as a potential multistakeholder issue. [They responded](https://github.com/w3ctag/design-reviews/issues/414#issuecomment-975506121) - looks on track... not clear which bits will get standardised... maybe webappsec after incubation. My sense is that addresses the issues we've raised. Maybe mark as satisfied with caveats and close?

Amy: worth asking to open a new review when they have a concrete spec

Peter: agree

```
Hi - thanks for the chance to give this important work an early review.  We're largely happy with the design and approach.  We're still concerned about the multi-stakeholder issuee and the dependency on PrivacyPass. We'd like the opportunity to review again when the spec is more concrete. Can you please either open a new issue or ping us and we can re-open this one.  In the mean time we're closing this.
```

### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689) - @torgo, @kenchris, @plinss, @atanassov

### [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690) - @torgo, @kenchris, @plinss, @atanassov

### [Broadening the user base of WebAuthn](https://github.com/w3ctag/design-reviews/issues/686) - @hadleybeeman, @plinss, @atanassov

Dan: explainer looks good and detailed and talks about user needs but is quite in depth. Don't seem to have a security and privacy questionnaire response.

Peter: seems more like broad ideas than something that would warrant an s&p

Dan: spend time at the f2f

### [WebAuthn minPinLength](https://github.com/w3ctag/design-reviews/issues/687) - @torgo, @hadleybeeman

Dan: we discussed it, seems like a small change, but they want us to review. If we think its fine we just need to say that. Make it a short review.

### [HTMLInputElement showPicker()](https://github.com/w3ctag/design-reviews/issues/688) - @hober, @LeaVerou, @atanassov

Lea: adding a showpicker method... only for inputs.. so people can programmatically trigger pickers. It's subject to user activation - addresses privacy concerns. This spec changes mandates that the current behaviour change - right now users open the file picker on synthetic clicks... this changes .. my main rservation is that it seems weird to have synthetic clicks only open some pickers.. also though I can see the future possibility some authors may want to make more complex UI...  if in the future these needs arise then we can add a separate API call.. this proposed change makes things inconsistent and adds a seperate method...  I'm gonna [post this](https://github.com/w3ctag/design-reviews/issues/688#issuecomment-975754941) from my PoV...

Peter: modal?

Lea: some modal some not... file p

Peter: [ for a synthetic click ] show file picker would not fire event listeners

Lea: correct.

Peter: what does this API surface buy ... over calling the click method or dispatching a click event. 

Lea: there's value in the predictability - of triggering it with a click event... have seen comments on StackOverflow asking about this.  

Peter: for me the biggest problem with date pickers that they're inconsistently implemented...

Lea: this doesn't help with that.

Peter: it's hard to feature detect. 

Lea: if you have a colour input ..... it's weird if you use showpicker and it shows the data list instead of the picker. It's more natural that a synthetic click just does what a click would have done, it's easier to have a mental model about this. [will comment]

### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov

Thomas: this feature has rolled out in chrome, we've been using it at google and it's been working fine. This is chrome status, we start seeing first page loads that make use of this. Going up. The top sites using this are whatismybrowser, and we have been using it in google internally. You might be able to see it if you go to google right now depending.. [live demo]. The client sends information to server so the server can inline the right CSS. What does this mean? Google in this barebones experience is simple, but when you search you see more things come into play. You can see there's a map component respecting dark mode. It's not just the CSS of the google page, but also all the widgets and images. In the end, the saved bytes adds up significantly. Which is why we proposed this feature in the first place, for high perf sites with lots of traffic. Francois built a boiled down version of this that shows how it can deal with dynamic traffic. Core idea is server sends initial scheme, I can mid way through manually change my colour scheme and the site dynamically updates. On demand, like any other dynamic request mechanism. By dynamically switching out the media on the link based on that, so we know if it's dark it will be light and vice versa. We can see the page dynamically pulls in the featureset it needs. 

Dan: What you demo'd tries to address the issue that was raised in the review. The question I have is if you need to add a whole bunch of js into the page in order to get the end result that would have been the case anyway if you had simply used the media query in order to make this work in a way that addresses the issue of what if your computer changes from light to dark. Isn't that cancelling out the performance gain? The tension here seems to be between something that developers expect to happen on the client, purely within css, and the idea that in some cases we might want to optimise delivery of bytes, and that's important, and imporant from a sustainability perspective, but if in the end in order to make it work in a way that respects the possibility of somebody's media features changing dynamically you have to add javascript into the page, it feels like we're back where we started

Thomas: you don't have to. It has no js at all apart from this thing that makes sure we are on https. It's happening dynamically on the server. THe client has no js dependency here. The server dynamically changes the style media prefers colours cheme so when the media conditions change it will request hte missing css that is needed in the new situation. this is boiled down tot heminimum demo, it's the same logic that we have in google.com. The core logic responsible for fetching the css is all happening on the server... the html generation on the serverside based on the value we get from the request, then pass it to this html generation function.. it's just html

Dan: what happens on the client when the condition changes? The client has to do something new, it has to send a request to the server now saying my condition has changed, what triggers that?

Thomas: just done by the browser. If the media attribute changes, same if you think media print, not loaded initially, if the media condition changes - you activate print styles, or maximum width - the same mechanism here for perfers colour scheme

Dan: thanks, I get it

Thomas: what we tend to see in practice is los of site offer a dark mode toggle so it overrides the scheme for the system for the site. Can register an event listener in js that can inform your toggle that the users preferences have changed. 

Peter: if you're building this without this clienthint what you'd do is link two different stylesheets with the media, if you're in light mode fetch this stylesheet and dark mode fetch this... what this feature buys is it gives this server the opportunity to know which one the client would have requested and inline that one. Shaves some bytes off the wire.

Thomas: correct. 

Peter: the concern Rossen and I have is effectively, historically this was a decision made entirey clientside. You're putting a server into that flow. We accept that if you do it just right you can get a slight optimisation by inlining stylesheet, but there's a whole lot of opportunities to get it wrong. It may look right at first, but what happens if it changes dynamically, people use script to do it, the browser now lost its opportunity to prefetch that sytlsheet, there are all sorts of ways to make this worse by trying to use this feature and not getting it quite right

Thomas: [demos blog] .. fetched with lowest priority because media doesn't match. Expensiveness is I have to make the initial request... then if it needs one or the other with higher or lower priority. If this automatically changes we have the place here that the media attribute would all of a sudden match so the client fetches it. Only works if we have informatin here. If no information, we fall back to a regular flow of making the initial request and letting the client decide what it needs. This is an optimisation that will work if the client hint is being sent. Everything else is regular flow if the media attribute changes.

Rossen: What happens when you have mixed modes? You have stylesheets and documents that are cming from documents that do support or they were sent from ... how does the mixed mode work in this case? where you have half of your documents essentially sending the client hint and half don't because they were not made ready? That becomes hell for the serverside to coordinate and reconcile doesn't it?

Thomas: client hints would be sent by the browser. If the browser supports it and server requests it then itw ould respond. It's not possible that one document would send and another wouldn't becasue it's happening at the browser level.

Rossen: my point was that if you have half of your documents on the serverside not recognising the client hints because they weren't updated to, and the others do, you have a component that is old and it doesn't recognise clienthints and it's doing its styling based on that, that component is in a document that *does* actually on the serverside recognise clienthints. What does that lookl ike?

Thomas: if your server doesn't support this it will not request a clienthint so the browser will not send it. The server can of course decide to ignore it if the browser sends something it doesn't like. I'm showing a server that creates html dynamically based on the fact a client hint is sent. Everything else if you don't request this you don't get it. It's not a fallback, it's a progressive enhancement. You use the regular flow of showing and deciding by whatever means, it can be a manual toggle, can be perfers colour scheme media attribute of link in css. If you do css in js and clientside handle this you can do this. It's a complete optimisation for sites that want to use this feature. If there's nothing that doesn't want to make use of this nothing happens.

Peter: if this is done right - best case scenario - it saves a round trip. But in order to use this in the first place doens't the client hint cause this rt anyway?  So what are we saving?

Thomas: Critical client hint - an additional opt-in mechanism. For the follow up requests sent - but for the initial request you have to say it's a critical client hint in order to see it.  Our measurements show this still outperforms inlining both style sheets ... critical thing is - people having this set to automatic. Even if you have set a cookie you can't be sure it's using dark mode still.  

Rossen: Way I see it - CSS today is designed to be client side tech.  I can write a style sheet and ship it to any client and have it apply .. the feature that you're suggesting breaks that and requires me to write server side code ....

Thomas: [Disagreeing] This doesn't break anything because if the server doesn't request it then the client won't send it... 

Rossen: If you want to create this experience for large sites then so be it... just don't see why this should be standadized...

Lea: also having trouble understanding the use cases here... there's also the media attribute on link elements... if a user changes their preference then things will start bring broken - CSS will chnage reactively and things will break... you could end up with an inaccessible intermediate state where some images assume dark mode and css assumes light mode...

Thomas: high perf sites inline everything. If you inline dark and light you will end up with a lot of css that is not used. You have to load this either way even if you don't use it. If you want to continue like today you can do that. With this optimisation the browser can also just say.. at this stage inlines critical css.. browser has same optimisations it has done before. We're in dark mode we inline dark css... light is fetched with lowest priority. Just fetches the nonmatching one with lowest priority. Were in light mode now but it has already fetcehd lowest priority lazily because it might need it. If we have a picture with a source depnendant on the mdia the browser will apply the same optimisations. Browser will run some heuristics and prefetch

Peter: we accept this can be done right in such a way that you're inlining some data, shaving some bytes, and accept that for very large sites that can get this right there are some savings. The volume of the savings add up. Our concern is that there are a lot of opportunitites to get this wrong. For people without the resources of large site we're going to see a lot of sites trying to do it half way / part way and get it wrong, and create a worst user experience and get it wrong because they're not testing walking with a mobile phone from a light room to a dark room while offline. This may propagate out to a lot of sites and cause breakage for not a lot of benefit for smaller sites because they're not at the same scale. we're wondering if it makes sense to add it to the platform. Someone does it on puprpose but doesn't quite get it right because they're not complete experts and picking it up from blog posts.

Thomas: this can happen with everything... 

Peter: i understand it happens everywhere, they may break their site and not realise

Lea: a difference between things that break immediately and thing sthat break if certain conditions are true

Peter: certain conditions for certain users. We see the advantages but we're worried it's a footgun. For general user do risks outweigh advantages, or vice versa? That's our main cconern.

Thomas: no for the general user, for the general site...

Peter: does it make sense to add this to the entire platform in perpetuity, or just leaving this as a non standard feature that google has that they know how to opt into. We're not saying don't do it, we're saying should it be part of the platform?

Thomas: we're including high performance sites.. Why is something used for a high perf site not standardised where something useful in general would be?

[Yves in chat: well, having two ways of doing the same thing is always an issue, especially when one is just an optimisation for just a few selected high profile sites
Also starting the trend to put all css media queries in CH would make very chatty requests]

Peter: not everything in a browser has to be standardised. If this becomes a standard I would highly recommend it includes verbiage that says it's for these conditions and not the general case, don't use this for your blog.

Thomas: we make clear this is for high perf traffic sites. Applies to all google.com users on firefox, on safari, if it was standardised. Not just chrome, browser in general, these benefits could add up universally. There are a couple of pages where this would apply - tiktok, facebook - there is a set of pages where this could benefit. If they wanted to and if they knew what they were doing they can use this. Not just in chrome ideally. We were hoping to convince others to move forward with this.

Peter: it's not that it can't be standardised, but our opinion. One thing that may help is to see some real data.. overhead to the request by adding extra headers? vs what you're gaining by inline a single stylesheet. nto comparing by inlining both stylesheets. If I was just linking both of them and using h2 and the roundtrip is faster..  Getting similar effects with alternatives to this feature

Thomas: I can ask. The blocking behaviour would only happen for the very initial request. The server is requesting these clienthints so it would respect them from then on

Peter: there is a block, it's unfair to ignore that

THomas: only until the client has learn this server respects this client hint

Peter: just make sure we're comparing apples to apples, and big picture. If we look at one part of the load we can say this part got 10%, 15% over here... data is important to look atthe broad picture

Thomas: I'll see what I can get. We did look at data or we wouldn't have pushed this forward.

Rossen: I meant to close this two weeks ago but I was away. I do expect to be able to write the closing paragraph and close it as far as the TAG review is concerned. 

Peter: suggest we take time to revisit and wait for data. [defer to f2f]

Thomas: encourage everyone to look at [the demo](https://glitch.com/edit/#!/bloom-accessible-offer?path=server.js%3A31%3A112) / [demo](https://bloom-accessible-offer.glitch.me/) and https://blog.tomayac.com/ (dynamic media attribute case)

## Breakout C

Present: Dan, Amy, Lea

Regrets: Yves, Ken

### [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667) - @torgo, @rhiaro, @atanassov

Dan: is now in WICG [leaves comment]

[Discussion on pre-rendering and how it fits into surveilance on the network ...]

Amy: the site itself sends the signal to the browser...  Then the browwser decides to act on that based on what else is going on the user's device...

Dan: [reasonable answer here](https://github.com/WICG/nav-speculation/blob/main/same-origin-security-privacy-questionnaire.md#how-do-the-features-in-your-specification-deal-with-personal-information-personally-identifiable-information-pii-or-information-derived-from-them)

Dan: are there other unintended consequences - things that might trigger even if the person does not actually visit the pre-rendered page?

Amy: they've caught that - "restrictions apply to prerendered page" "promises do not resolve" and "preventing intrusive behaviours" seems like a work in progress. "downloading resource" "user prompts" "Async apis" A list of APIs that are delayed inlcuing EME. Also a section for preventing nonsenical behaviours... 

Dan: looks like they are considering the issues.

Amy: haven't seen an answer to server-side traffic monitoring.  There's a javascript function to see if a page is prerendered or not but how about from a server's perspective?  Case that a whole lot of server code would need to be updated -- and most of the web is not going to be updated.
 
### [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684) - @rhiaro, @hadleybeeman

[reads epub 3.2 and 3.3 diff]

Dan: looking at security and privacy.. Tess will also have opinions. We need to schedule a f2f session

### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682) - @torgo, @kenchris

### [Feature policy for Keyboard API](https://github.com/w3ctag/design-reviews/issues/685) - @cynthia, @torgo, @ylafon, @atanassov

### [Web App Launch Hander](https://github.com/w3ctag/design-reviews/issues/683) - @kenchris, @hadleybeeman


## Plenary Session

Present: Peter, Dan, Yves, Amy, Lea

Regrets: Rossen, Tess, Hadley, Sangwhan

### Breakout Rollup

#### Breakout A

##### discussion on CH media features and whether standardizing it is better than not

Amy: [Better to standardize it if there are multiple sites that want it and multiple browsers that want it?]

Dan: any way we can put pressure on browsers to mitigate against the complexity issues we've raised?

Peter: I am concerned about that- could cause reloads... Fear people using this first and not setting up the clientside hint properly... or if you just use client hints you don't have to bother setting up media queries and other stylesheets. Lots of warnings?

Dan: agree better to standardise, close approve with concerns

Yves: starts a precedent.. what people are used to do things on certain characteristics of the device using css and media queries. Now they want to use that to do a kind of content negotiation or ad hoc regeneration based on that.. it seems that it's opening the gate of adding more things that can be discovered that way. I wonder if that's a good thing or not.

Peter: are there actually other vendors?

Amy: Thomas said something about it but I don't know if it's hypothetical

Peter: wondering if people will do it

Amy: I agree that if it's only Chromium and Google then it doesn't need to be in the web platform - but if others are involved then it should be a standard.

Peter: we could advise people to not use the CH except in certain circumstances?

Amy: is there something we could do with encouraging them to work with CSS to improve perf instead?

Lea: How could this be added to CSS?

Amy: I wasn't thinking added - I was thinking how do you optimize it from a CSS angle...

Peter: the way I would solve this problem would be to use http push. You have 2 stylesheets, you want to avoid the RT, so normally you would link to 2 stylesheets. They are saying the server can know which and choose to inline one of them. Alternartive would be to link them both and the server uses h2 push - client could then say "I don't need this now so I'll denythis push". You need some logic on the server... 

Dan: worth discussing, have they even thought about h2 push? But some people have been having trouble with it.

Peter: not sure what the status of h2 push is. Everyone was very excited about it

Dan: I don't know the specifics but I heard that some people were finding it less useful than expected

Yves: there were issues based on the ordering you need to push things. There were experiements about some kinds of trees sent that gives priority to the server but it was just an experiment and didn't reach any production

Peter: general problems with h2 in general... h3 push should be fine.. Agree it's worth mentioning, I'll post it.

### [WebAuthn minPinLength](https://github.com/w3ctag/design-reviews/issues/687) - @torgo, @hadleybeeman

Dan: hadley left a comment.. I can't see any issue, looks like a small thing, recommend we close approved, small delta to existing spec. If anything it adds security.

Peter: there was something weird about where the minpinlength is specified, only works for certain origins or something. Last paragraph.. 

Dan: now I'm re-reading that I'm realising what explicitly preconfigured means. I had assumed it meant something like a header. But ..

Peter: set on the key through some out of band mechanism.

Dan: what do they mean by preconfigured? Sending special ctap messagse to the security key..

Peter: not exposed over the internet. A company can preconfigure the key..

Dan: that's okay. As long as it doesn't require some kind of allowlist in the browser that makes sense. Those keys need to be configured somehow, out of band. 

Peter: if it's purely on the key... i think this is okay. Okay closing this.

Dan: [closed]

#### Breakout C

Dan: reopened same-origin preredinger triggered by speculation rules because speculation rules was brought into wicg. There are a lot of potential unintended consequences of trying to prerender something. A lot we could think of were taken into account in the spec and explainer. They had a good story around privacy and security. Choice on what to prerender shouldn't happen based on knowledge the client might have, and things like that. The issues still remains what's the story with speculation rules - no signals. We have new contacts for it. 

### Issue Triage
