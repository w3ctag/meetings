# TAG Teleconference
#### 14-16 August 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-08-14](https://www.timeanddate.com/worldclock/converter.html?iso=20230814T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov
* [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro
* [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman
* [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou
* [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov
* [TAG spec review of Bounce Tracking Mitigations](https://github.com/w3ctag/design-reviews/issues/862) - @hober, @hadleybeeman

### Breakout C (APAC / Europe) - [2023-08-15](https://www.timeanddate.com/worldclock/converter.html?iso=20230815T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @cynthia, @torgo, @ylafon
* [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo
* [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo
* [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov

### Plenary Session - [2023-08-16](https://www.timeanddate.com/worldclock/converter.html?iso=20230816T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Rossen, Hadley, Amy

Regrets: Dan, Lea


### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

Hadley: UA making the decision which servers to trust... seems like a way it could all fall apart. How would you know if UA was unscrupulous?

Rossen: how is the user data managed? is it per account? if I have my own session and I'm logged in mas myself and then I log out so my daughter can use the computer for school, is she going to be targeted with running shoes because that's what I was looking at before that?

Hadley: not clear. Arguably unless you'd cleared your cookies with 3p cookies that would happen?

Rossen: with the browser account which usually has the ability to integrate with web content as well. I'd be surprised if they didn't think about this.

Hadley: explainer says browser keeps track of the set of interest groups joined. Up to the browser how to handle it?

[discussion about taking state out of the web and into the browser. Eg. browser account management is not standardized in any way, whereas with 3p cookies browser is just a transport/storage mechanism. Giving more power to browser, a direction we want to go in? ]

Hadley: browser provides protection against microtargeting by only showing ads shown to a sufficiently large number of people - how does the browser find out how many people saw an ad? In a way that preserves privacy of user?

Rossen: is the identifier the ad? I can imagine an ad id that I can ping the server and the server gives me back a number.. as long as I don't send any more data to the server

Amy: is the server motivated to lie to make sure people see the ad?

Rossen: there's that. And I have to go back and tell the server +1

Peter: the browser is also running the ad auction so I don't know if the browser has to go back to the server. Part of the auction process to know who won.

Peter: the api for running an ad auction.. there's a lot of urls.. hard to understand how this could be abused. A lot of vectors for abuse

Hadley: and a lot of traffic.

Peter: true, but the current ad network genereates a lot of traffic. This is probably less. Not uncommon for an ad auction to go through 20-30 different vendors

Hadley: does this make all of those requests my problem on my network?

Peter: also it's talking to soembody to run the ad auction. What's stopping them from passing this on upstream?

Hadley: and what's stopping the browser from .. right now ad blockers can operate because the browser is separate from the advertising process, so you can ask your browser to treat ads differently. What's stopping browsers from saying you can't use the web unless you participate in our ad network?

Amy: competition between browsers, but that's not ideal because not everyone knows there are other browsers..

Hadley: and what if every browser went that route for money?

[discussion about browser as UA vs browsers as advertiser agent]

Hadley: this biases the system towards ad networks that are aligned with the browser. Not good for competition.

Amy: it kind of moves the probem rather than solving the problem

Peter: I see where it can improve privacy for individuals, a little -- I'm not sure it goes far enough. But i have very big concerns.

Amy: why do they need this as well as Topics? They have an 'alternatives considered' section that mentions Floc but I'm not sure if that's still current since Floc is Topics now...

[trying to figure out difference between this and Topic.. "remarketing".. more specific about having had an interaction, rather than generally this kind of person]

Amy: is it the same mechanism as topics? but more granular? So one of the mitigations for privacy in Topics was to make it *less* granular

Peter: browser can offer user to join groups for an item. Site gets to decide level of granularity to register

Hadley: can the site pay more to have a monopoly on the kinds of ads the user sees afterwards?

Peter: the only reason a site would make that call is because they intend to advertise to you later on other sites

Hadley: like opening up your 3p cookies to others who want to know you have a 3p cookie about a particular thing

Peter: I think this is all this accomplishes. And reduces information about what can be stored in the cookie. Concerend about how far that can be pushed. WE've already seen how advertisers can target individuals on the basis of data we never thought would be unique or personally identifiable. The one thing about this I do like is at least ideas in the explainer about UI controls. allows the UA to do things like keep track of what ads you've been shown and why. Who targeted you, what interest groups you're in, why you're on the list, block an advertiser. User could theoretically switch the whole things off, which is like blocking 3p cookies. If you're buidling a privacy prserving browser you can shut this off.

Amy: user settings for this is not realistic or reasonable - same feedback that we gave to Topics

Peter: it doesnt' give the user the ability to opt in - but surfaces the information after the fact. If every interest groups popped up a permission prompt

Hadley: everyone would be horrified

Amy: ... for 5 minutes, until prompt blind and agreeing with everything.

Amy: point them at the Topics feedback and say it all still applies?

```
The [feedback we left for the Topics API](https://github.com/w3ctag/design-reviews/issues/726#issuecomment-1612522047) is applicable to this API as well. The coarse nature of the set of possible topics has been proposed as a mitigation to some of our concerns there, whereas the set of interest groups proposed here seems far more fine-grained, an unrestricted. As we said for Topics, user controls for opting out of particular topics/interests are not sufficient to indicate informed consent to being tracked in this way.
```

### [WebAssembly JavaScript Promise Integration API](https://github.com/w3ctag/design-reviews/issues/809) - @cynthia, @atanassov

### [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro

Peter: naming is unfortunate. It's not large and it's not a blob. Other than that okay. Has shipped. Apple are using it.

### [Private Aggregation API](https://github.com/w3ctag/design-reviews/issues/846) - @hober, @hadleybeeman

### [Incremental Font Transfer: Patch Subset](https://github.com/w3ctag/design-reviews/issues/849) - @hober, @LeaVerou

### [deliveryType (Resource Timing)](https://github.com/w3ctag/design-reviews/issues/858) - @hober, @atanassov

### [TAG spec review of Bounce Tracking Mitigations](https://github.com/w3ctag/design-reviews/issues/862) - @hober, @hadleybeeman


## Breakout C

Present:

Regrets:


### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo

### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @cynthia, @torgo, @ylafon

### [Eligibility for autofill](https://github.com/w3ctag/design-reviews/issues/831) - @cynthia, @torgo

### [Bluetooth RFCOMM in Web Serial API](https://github.com/w3ctag/design-reviews/issues/854) - @cynthia, @torgo

### [Web Audio API: RenderCapacity API](https://github.com/w3ctag/design-reviews/issues/843) - @cynthia, @atanassov


## Plenary Session

Present: Peter, Rossen, Hadley

Regrets: Dan, Lea


Lack of quorum


### Breakout Rollup

#### Breakout A

#### Breakout C

### Issue Triage
