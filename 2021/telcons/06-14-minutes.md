## TAG Teleconference
##### 14-16 June 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-06-14](https://www.timeanddate.com/worldclock/converter.html?iso=20210614T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Design Principle - When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - with guests
* [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov
* [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss
* [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov
* [WebID](https://github.com/w3ctag/design-reviews/issues/622) - @hober, @rhiaro, @hadleybeeman, @atanassov


#### Breakout B (US / APAC) - [2021-06-15](https://www.timeanddate.com/worldclock/converter.html?iso=20210615T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov
* [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss
* [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

#### Breakout C (APAC / Europe) - [2021-06-15](https://www.timeanddate.com/worldclock/converter.html?iso=20210615T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris
* [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo
* [API for display-capturing the current tab](https://github.com/w3ctag/design-reviews/issues/625) - @cynthia, @LeaVerou

#### Plenary Session - [2021-06-16](https://www.timeanddate.com/worldclock/converter.html?iso=20210616T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Rossen, Dan, Yoav Weiss (Guest), François Beaufort (Guest), Mike Taylor (Guest), Amy, Yves, Hadley

Regrets: Sangwhan, Tess, Kenneth, Lea

##### [Design Principle - When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - with guests from Google

Dan: we had a design principles discussion about when to use client hints. That came up in the design review on [client hints reliability](https://github.com/w3ctag/design-reviews/issues/549). The question came why is this a client hint. The discussion in that meeting came around to client hint would be a appropriate mechanism but we were thinking that there should be another way to do it. For web devs that don't have access to the server config required to set such a hint. That brought us back to the question of should there be a design principles about this? ([design principles context](https://github.com/w3ctag/design-principles/issues/307)). Also because client hints is intertwined with new activity coming from chrome on the user agent.

Yoav: in terms of design principles it makes sense.. the question of what should and shouldn't be a client hint has come up as part of the ietf rfc process, was thoroughly discussed in http wg, and is codified in that rfc. Which is client hints shouldn't be the only way to expose capabilities; there should be js or css based way, or even html one in some cases that would expose that capability. Client hints should only come as an optimisation. As far as I know this is a rule we've kept for all client hint sin chromium. If it's something we don't want to expose to js means we also shouldn't expose it to client hints. Doesn't mean everything exposed to js should also be exposed to cient hints. A principle by martin thompson from mozilla is for highly variable information is not something that should be exposed as a client hint. Eg. precise geolocation. That seems like a reasonable principle. My take on client hints, assuming exposed in js, theyr'e an optmisation that enables the server to act on that information earlier. Doesn't expose any new information beyond something the developer can pull on their own. That is particularly true for everything that is media query based, because anything based on a media query condition can have a listener in js that sends that information to the server. That is the set of guideing principles that led us through the design of the feature. I think it makes sense to document that as a TAG design principle if you see fit.

Dan: that sounds aligned with what we were thinking. That means that we're more aligned than I understood. 

Yoav: one thing that came up in the review for user preferences media features client hint was a question around phishing that I did not understand.

Rossen: the optimisation and intent around using client hints to save bits going down the wire makes sense to me. From user benefit and serverside benefit I can see how this approach  makes total sense. What i pointed out in the [media feature client](https://github.com/w3ctag/design-reviews/issues/632) hints issue, this started as lets expose the prefers colour scheme only.. more poeple said why don't we expose all the relevant media featurse. As I was reading the set of media features you want to expose what became clear is i can create evasaion techniques that are much early on.. most capabilities and most anti-phishing solutions today work by employing a lot of automation to go and scout information to impersonate a user for an ill intended domain to give the same content to the target user, so they can discover phishing sites and start blocking them... game of cat and mouse.. more often than not people working on trying to make money out of this are pretty good at fingerprinting this kind of synthetic info that is scouting what they're doing and they have evasion techniques. Most happen on the clientside today. I can see how something like this can fingerprint a device setting, like a VM default setting, like what an antiphishing bot is doing, and evade it during client hints and not send any kind of content to the crawler. That prompted my questioning.. maybe you have thought of this. The way this would happen today, if I was evading based on trying to figure out this default VM setting I"d send you the js that was posted immediately by thomas and get your media features and screen capabilities and all of that that way, and then evade from there.

Yoav: if I understand... not familiar with that world.. your concern is that server-side fingerprinting in those cases will be more covert than clientside fingerprinting even though one will be close to the logic as a person who is running the browser

Rossen: the browser or just a crawler trying to get to the content

Yoav: if all you get on the clientside is just .. collecting a bunch of bits, sending to the server, you get a response from the server that gives you the content. Not different than just sending those bits .. asking for those bits of entropy and you send it to them

Rossen: it makes sense.. I don't know how much I can go into details of why I believe this is a problem. I have seen some of these evasion techniques being similar to this pattern. I can see it becomes much more opaque to the clientside. 

Dan: could you examine a mitigation? is there a team in google that focuses on this that could be helpful?

Yoav: possible..

Mike: there's folks who work on these type sof problems. it's too abstract for me to be able to come up with someone to talk to.. maybe there's a way to discuss more details

Rossen: I have folks from your side I work with closely, safe browsing and security. These are not unfamiliar problems. Curiosu if you have a chance to check with them. I don't know wht kind of threat modelling you do. Maybe it becomes a nonissue. Provoking checking in and making sure it's not going to be making things a lot easier for the other side

Yoav: next step we can ask and see the understanding of the problem space

#### [UA cleint hints...](https://github.com/w3ctag/design-reviews/issues/640)

Dan: third thing is about user agent and .. I had a [post from chromium](https://blog.chromium.org/2021/05/update-on-user-agent-string-reduction.html) about relaunching the plan to deprecate some parts of the user agent string in favour of client hints, and wondering how does this .. what kind of information would you like from the TAG on this? How would you like us to review? How can we be helpful?

Mike: we announced we're ready to re-begin this process to reduce the user agent string, or the amount of information you can fingerprint from the UA string. We want to do this in a safe way, not our intent to break the web, UA strings are very tricky and sensitive to change. We propose an end step process, seven phases. Predicated on our ability to have an origin trial for sites to opt into and tes tproposed changes with a long period of feedback, at least 6 months, so we can discover what we're not thinking of. We've done testing, we think it's safe, but the internet is big and scary, based on this 6 month feedback period if we feel its safe to proceed we do.. first step is removing minor build patch numbers from chromium string and sending 000. It feels like a safe change and if you rely on that information you can get them from clients hints api. Then we aim to change desktop user agent string, then mobile. What you will reliably be able to get without caringa bout client hints is the name of the browser, the platform, major version, and the mobileness. We feel like that covers the majority of use cases for most web apps today. If you need something more nuanced like the device model of your phone for optimization you can request that through client hints. That's a broad overview of the plan. If you find that blog post you can follow a link to th echromium wiki and see all the ua strings at their various phases. What kind of feedback are we looking for? Should we be giving away the platform by default? Prtend everyone is on a windows device becuase its less fingerprinty, but it breaks too much of the web? Real accessibility use cases.. 

Dan: that information is still accessible via a client hint?

Mike: correct, get it on the next request

Yoav: information exposed by default and considered low entropy are not going to be reduced from the orignal ua string content that relies on the platform, ctrl+c vs cmd+c work even if they don't change their code to rely on the user agent client hints. that and the fact that platform is somehow still already expoed becuase of tcp level fingerprinting that won't go away. 

Mike: the legacy part is also important to consider. You could upgrade your site to upgrade that platform information assuming you have a maintained site which is not true for a large part of the web. 

Rossen: owe more time on the media feature ones, at least to convince ourselves that some concerns are a non issue. What else?

Dan: we're going to continue to work on this issue, on 604, and get feedback. It's the case that ua string is used for fingerprinting and its well known for years now that privacy focussed browsers are normalising the ua string including the platform. That's what Tor does. Very sympathetic to that. To what extent do small players, some of the use cases around content transcoding in africa for instance where they're using the ua string to identify .. how much are we taking into accoun those use cases? sounds like you are because you're going through this very cautious process and keeping a certain amount of the string, but has that been part of your thinking? how much have you been able to listen to the communityi?

Mike: for background, I spent the last 10 years wokring on web compatibility at mozilla and opera. "All sites must work." Very sensitive to this idea of not breaking the web for users of underdog browsers, or countries that are not 'silicon valley targets'. To the extent that we get feedback from web devs and other interested parties it's in our interest to take that seriously and try to design soultions for that. I expect that during this origin trial feedback period we may learn some uncomfortable facts that cause us to reconsider our plans. Not convinced we know all the answers yet. I'm hopful we can get to a place where passive fingerprinting thorugh the ua string is less fruitful. The client hint reliability effort - how to solve for that on the first request - would solve for use cases where an extra round trip is very expensive. Some evidence that we're trying to make this work for a lot of people. 

Hadley: good to hear.

Yoav: also on the feedback front - point of feedback that already changed what's exposed by default is the platform. Mobile vs non mobile.. for the africa use case that was the first case that convinced me that that extra bit of entropy [??] expose by default in order to address the low-bandwidth networks / content adaptation case, I don't now the %, but a large portion, exposing device model by default exposes a ton of entropy. So the calculus there doesn't make sense. But client hints reliability will make it easier for folks to get that on that request. And hosting providers can get that out of the gate without requirng people to create custom server side logic for them

Dan: great to hear. Anything else we can help with right now? What's the time sensitivity of us getting back to you? Other design reviews pending that you're waiting on?

Mike: in the next week or so would help convince some of the blink api owners to be comfortable. Next two weeks is still fantastic.. 

##### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632) - @torgo, @atanassov

##### [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss

Hadley: we left this pending editor update and we have not heard [nudges]

##### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

Peter: tess and ken, but neither are here. [deferred]. The question is the boundary between realms. Dominic has been pushing to make  it a callable boundary, that blocked a whole lot of use cases but it looks like that is moving forwad. There's a way, a shim library, which lets you fake sharing objects between realms by wrapping everything in callables. Looks like that's the approach going forward. Not sure that hard decisions were made. 

Rossen: what was blocked?

Peter: if you want to ahve an object that is shared between parent and realm; have an object returend by a server along with some js that can manipulate that object but nothing else. Can change internal sate of that object but not access to the dom or navigator state. That's not easily done directly with a callable boundary. This other library they've developed lets you syntehsize something that has callable boundaries that can be passed back and forth between realms. Think we're okay, just a performance question at that point. I think dominic has concerns that without that restriction you don't get some of the security guarantees that people think realms gives you. 

##### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

Hadley: also waiting for a response [nudged]

##### [Screen Fold API](https://github.com/w3ctag/design-reviews/issues/575) - @torgo, @plinss, @atanassov

Dan: Screen fold renamed [device posture](https://w3c.github.io/device-posture/). Hasn't been that many updates. Maybe we want to ping the editors and see if there are additional updates since the issue was raised.

Rossen: i pinged them just now

##### [WebID](https://github.com/w3ctag/design-reviews/issues/622) - @hober, @rhiaro, @hadleybeeman, @atanassov

Amy: there was a workshop that Tess attended

Hadley: we got stalled because I asked Sam for use cases. The explainer was talking about improving privacy and security and creating federated ID but not explaining what he wanted to solve. I asked and he came back with the same general words, some examples that explains ome of the problems with the ID ecosystem which are raelly interesting - too many ways of logging into something, the ossification problem that the web hasn't evolved its ID technologoies. I don't see any problems with what he's erecommending, but I'm still not clear what happens if what we're trying to do here is to make it possible to operate with 3p cookies, what happens after you log in and how that's different 

Amy: Sounds like a good summary. The core is that they're not coming up with soultions yet - just exploring the problem. They are creating a CG. Maybe there is not much more we can do. Good for us to keep an eye on it.  If there's a CG with broader participation that is good.

Hadley: Agreed.

Yves: can investigate the webID CG

Hadley: not really something to review... I think we can give Sam  the feedback that what they are exploring makes sense and we support a CG... we'd like to see designs as group comes up with them...

Amy: I'd be "happy" to join the CG.

Dan: I have questions related to the use cases - my question in the session that we held was what cases are you really going after. THey talk a lot about federated identity, but you can still do it... they need to be specific. They know that but have a lot of discussion about cases around federated identity but they're not addressing "and these are the things that cannot be done without 3p cookies"

Amy: other things as well to get ahead of further changes after 3p cookies go away - documented in [our minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/05-17-agenda.md) from our special session. 



Dan: +1

### Breakout B

Present:

Regrets: Tess, Sangwhan


#### [Handwriting Recognition API](https://github.com/w3ctag/design-reviews/issues/591) - @cynthia, @atanassov

#### [Early design review of modal close signals/ModalCloseWatcher](https://github.com/w3ctag/design-reviews/issues/594) - @hober, @plinss

#### [CSS: contain-intrinsic-size: auto, and converting to a shorthand property](https://github.com/w3ctag/design-reviews/issues/624) - @hober, @LeaVerou, @plinss, @atanassov

#### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia


### Breakout C

Present: Ken, Amy, Yves

Regrets: Dan, Lea


##### [Managed Device Web API](https://github.com/w3ctag/design-reviews/issues/606) - @cynthia, @kenchris

Ken: they are discussing internally about security.... [writes comment to ask them to get back to us about that]

Amy: their response justifies it with a very narrow scope, but that scope seems to me to not have a place on the web platform

##### [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) - @LeaVerou, @torgo

##### [API for display-capturing the current tab](https://github.com/w3ctag/design-reviews/issues/625) - @cynthia, @LeaVerou


### Plenary Session

Present: Peter, Amy, Yves, Hadley, Rossen

Regrets: Dan, Lea, Kenneth

#### [Canvas 2D color management](https://github.com/w3ctag/design-reviews/issues/646)

Assigned to next week.

#### Breakout Rollup

##### Breakout A

##### Breakout B

##### Breakout C

#### Issue Triage
