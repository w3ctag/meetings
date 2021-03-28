## TAG Teleconference
##### 22-24 March 2020

---

### Agenda:

#### Breakout A (Europe / US)

* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [Early Design Review: Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611) - @hober, @rhiaro, @atanassov
* [Support WebOTP API and origin-bound one time code in cross-origin iframes](https://github.com/w3ctag/design-reviews/issues/604) - @hober, @cynthia, @kenchris
* [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov
* [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss
* [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @hober, @torgo, @rhiaro, @plinss

#### Breakout B (US / APAC)

* [inert attribute](https://github.com/w3ctag/design-reviews/issues/610) - @hober, @LeaVerou
* [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia
* [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou
* [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris

#### Breakout C (APAC / Europe)

* [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman
* [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @torgo, @hadleybeeman
* [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @kenchris
* [Limit allowed "accepted" extensions in File System Access API file pickers.](https://github.com/w3ctag/design-reviews/issues/580) - @cynthia, @kenchris
* [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris

#### Plenary Session

* [Temporal Proposal Feedback Feedback](https://github.com/w3ctag/design-reviews/issues/311#issuecomment-804496493)
* detectiblity of AT - Sangwhan

* Breakout Rollup
* Issue Triage


-----


### Breakout A

Present: Dan, Peter, Lea, Hadley, Yves, Amy, Ken, Tess (second half)

Regrets: Rossen, Tess (first half)

##### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo

Tess: if you take a step back - and look at reality - people already bundle things - concat js files together - etc... I'm sympathetic to the motivation.  It should be known by the browser so the browser can make better decisions ...

Dan: Paving cow paths?

Tess: It's not.  Paving cowpaths would be to standardize things being used - like js minifiers - etc...  The devil is in the details and there are a lot of details.

Dan: we've been talking about bundlding and packaging for ages. The web already bundles, it's true, but if so why are there people asking for bundling technology? Where does this need come from? 

Ken: you can bundle everything - and you don't have to download all of the bundle.  I think what Dan E is working on - is a separate but related effort. Why multiple efforts in parallel?  [link](https://github.com/WICG/resource-bundles/) and they [responded](https://github.com/w3ctag/design-reviews/issues/616#issuecomment-790405371).

Tess: sounds like they want to converge but haven't yet? That answer suggests we should close this issue and wait for them to progress on converging. If they get to somewhere better than this .. I want them to figure that out and come back to us.

Dan: +1 

Ken: or state clearly why this is a separate effort.

Tess: it would be a waste to give redundant feedback - we shoiuld encourage them to work together.

Dan: This is architecture.

Hadley: sounds good.

Peter: I know bundling has been part of the web - there was an attitude that h2 was going to solve this - but hasn't worked. Has that been addressed by h3?

Tess: [Martin's post](https://lowentropy.net/posts/bundles/) goes into a lot of that... 

Peter: if this is on the cusp of being solved at the network layer maybe we shouldn't add another thing to the web platform

Lea: I agree it makes sense to solve at the network layer, instead of adding another step in the number of steps that developers need to follow to deploy...

Tess: I'll post it and close it.

##### [Early Design Review: Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611) - @hober, @rhiaro, @atanassov

Amy: i had a look - and had some questions.  Main thing: how it relates to [resource hints](https://github.com/w3c/resource-hints/). Seems to be an alternative to resource hints. Seems to be an old spec that is in CR...  .. there's an issue in design reviews - https://github.com/w3ctag/design-reviews/issues/398  Supposed to be a privacy-respectint alternative to resource hints... but may be history that I'm not aware of...

##### [Support WebOTP API and origin-bound one time code in cross-origin iframes](https://github.com/w3ctag/design-reviews/issues/604) - @hober, @cynthia, @kenchris

Ken: they are shipping it... I think it's quite sensible.   Safari implements the formart.  

Dan: it's a delta but it changes a security boundary so ... should bear analysis...

Ken: it's im response to an issue filed by Tess.

Hadley: it's a big change. Also tess is listed as one of the contacts

Ken: one of the parts is SMS one time codes - extension to text message - they are looking at different options.  Then WebOTP part is google only.  The cross-origin part seems to be in the SMS format.

Hadley: the [issue ken linked](https://github.com/WICG/sms-one-time-codes/issues/4) to also talks about cross-origins.  Feels very first party sets-y to me.

Peter: this more about like double-keying cache or cookes - only works in this iframe when it's embedded in this origin.

Ken: the SMS contains a one time password and you only want to auto-deliver it to the proper recipient.  They want to extend it so that the iframe can actually get it 

Hadley: so the SMS would include both.

Peter: the browser would see it and auto-fill it.

Dan: if the sms contains both - double keyed - then it's a one time thing, the intetion is to streamline the OTP process when you're using SMS, so it seems to me that it's reasonable. Maybe mark as proposed closed?

Ken: it says it's been discussed with Safari as well- sounds good.

Hadley: me too. point of trust has to be the user agent - that feels like the right place to put the trust.

Dan: and it doesn't rely on an allowlist, which is good

Amy: [related issue in wicg](https://github.com/WICG/proposals/issues/2)  - commen about web pages don't use reseouce hints because [performance]... 

Tess: but they have to do that work do generate the speculation rules... 

Amy: i had questions on where the heuristics come from on deciding which links to preload.  I think there is a privacy & security thing - might reval info - an origin could game the rules to reveal as much data as possible. Will leave [a comment]()

##### [Design review of SameParty cookie attribute](https://github.com/w3ctag/design-reviews/issues/595) - @hober, @ylafon, @hadleybeeman, @atanassov

##### [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss

Dan: Will ask Wendy for a liaison with IETF on the issue.

##### [CAPTCHAs are horrible](https://github.com/w3ctag/design-reviews/issues/558) - @hober, @torgo, @rhiaro, @plinss

Peter: we talked about pinging Ping and we haven't heard anything back yet...  Will ping again.

#### Upcoming AC meeting

Tess: AC meeting is coming up.  I've been asked to be on the panel talking about privacy work at w3c - will be talking about s&p questionnaire and the priv cg.  I'd like to be able to use examples. FLOC request - we immediately asked PING to review as well.  Can we think of other examples of ways in which we're collaborating.

Yves: first party sets as well?

Dan: the discussion about the clipboard API, is it okay for a webpage to ever snoop on your clipboard without you knowing. That's a complete betrayal of web users if we allow that to happen. It's a good example because its historical, the issue was resolved, but people were thinking about doing that and there's a constant pressure from commercial requirements to weaken the privacy guarantees of the web and that's why we have to have the privacy questionnaire and why PING and privacycg exists and why we put energy in this.

Yves: another example is the font enumeration API. The fact we didn't want that to be used as a fingerprinting vector and that led to the API minimisation that we have right now. The kind of thing that was driven by the review and that led to more advice for better privacy on API design.

Dan: good opportunity to wave the TAG banner

Tess: ethical web principles are underpinning what we're doing here

Dan: our feedback documents have our opinions in them.

### Breakout B

Present: Peter, Sangwhan, Rossen, Lea

Regrets: Tess

##### [inert attribute](https://github.com/w3ctag/design-reviews/issues/610) - @hober, @LeaVerou

Propose closing, waiting for feedback from Tess

##### [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia

Sangwhan: Use case makes sense. Propose close, but want Tess to take a look at the plenary

##### [Review Request for CSS Color Adjust Level 1](https://github.com/w3ctag/design-reviews/issues/583) - @hober, @LeaVerou

Still pending feedback from the CSSWG

##### [EyeDropper API](https://github.com/w3ctag/design-reviews/issues/587) - @cynthia, @LeaVerou, @kenchris

Still pending feedback


##### [Temporal Proposal](https://github.com/w3ctag/design-reviews/issues/311)

Reviewed recent feedback.

### Breakout C

Present: Dan, Ken, Amy, Yves

Regrets:

##### [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman

Dan: let's bring this to the plenary.

##### [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @torgo, @hadleybeeman

Dan: I've been thinking about this... Hadley's opinion was we should write more substantive feedback. That feedback should center around the fact that the web security model is based on origin and origin is tied to the domain name system. The proposal on the table from the FPS folks by design is that the current origin system does not work for the use cases they want to accommodate and we're uncomfortable with making such a basic change to a fundamental layer of the web architecture without being extremely careful and that some of the discussion that's come back when we've asked questions has indicated to me that there's not full consideration of the implications, despite there being a lot of work going on. Things like "we" will make sure all the FPS belong to the same organisation, and how do you do that? Very handwavey. In practice is impossible. Because the browser would need allowlists, and talking about allowing these orgs to set up their own FPS so.. We need a document that pushes back on this concept which articulates the conditins under which we would be happy for FPS to exist as part of the web. Those conditions need to be it's limited in this way, only works in this way. Eg. we asked does this apply to permissions? If I give my permission to insagram to use my camera am I also allowing facebok? The response was no it doesnt apply to permissions. SO what does it apply to? Some is in the spec, but it's not very clear, and especially the name is FPS it sounds like everything where we're thinking about first party and third party this will apply. We need to come up with consensus that the TAG can sign onto which is pushing back or listing what we think are the criteria that we would like to see implemented in the FPS proposal. And the fact we've had negative feedback from other implementers. Even if we say we think it would be okay under these criteria there's no guarantee that other implementers would also say it. We shuld also take that into account.

Amy: +1 can help write

Sangwhan: it's not good.....

Dan: they have a section about why it's not intended to support ad networks

Sangwhan: it will

Dan: it will and there's a designa pproach here which is that from a google pov protecting user privacy is about protecting privacy between the user and google. From a Brave pov google is one of the things to protect the user from. There's a mismatch there of the threat model.

Sangwhan: these companies go to great lengths to track you, [CNAME cloaking](https://dev.to/dnsadblock/cname-cloaking-or-how-are-we-being-tracked-even-with-ad-blockers-installed-5ok), ad companies have been using. FPS on DNS level.. suborigin on your domain.

Amy: the bit about it's not supporting 3rd party ad network - right, it only supports google's ad network. It upsets ad tech people and people who are against surveillance capitalism. 

Dan: Facebook and Salesforce also came out in favour of this propsoal. 

Amy: it supports compamies that run big ad networks.

Dan: there's an arguement Andrew Betts made in the discussion about AMP. When you have ad networks with sufficient power they can compel third parties to do whatever they want. If you've got an ad network that is supplying revenue for parties like the guardian or somebody they'll be very incentivsed to instrument their webpages in whatever way the ad network wants to get more revenue from that ad network, including in ways that leak their users information without the users knowledge. We can start a document with me Amy and Hadley and come back to the TAG

Sangwhan: any piece of tech that looks innocent is going to be abused to serve ads.. CNAMEs looked very innocent..

Dan: any sufficiently advanced web technology will eventually be used to serve ads.

##### [Virtual Keyboard API - boundaries of docked overlay keyboard](https://github.com/w3ctag/design-reviews/issues/507) - @cynthia, @kenchris

Sangwhan: They came back with a response... 

[...working on this one...]

Ken: they seem to have fixed a lot of the things I wanted them to fix... just wondering about API .. getter and setter ... normally when you have an attribute as well it's just a getter.

Sangwhan: tbh I don't think this is satisfactory ... this felt very one off. It's an occlusion but specific to keyboards.

Ken: but keyboards are very special.

Sangwhan: being handled as a special case... I don't think this is enough of a rationale. 

Ken: Actually I think that keyboards are very special - especially on mobile devices. I kind of disagree that you should have a generic occlusion api .. i think there are many cases but keyboard is very important. This is a needed feature.

Sangwhan: there is also implementer disagreement.  Webkit has [disagreed to this API design](https://github.com/w3c/editing/issues/225#issuecomment-614902156).

Ken: I thought they objected to the other part?  Also webkit they don't have issues ... 

Sangwhan: they have the same concerns... 

Sangwhan: mozilla also objects... 2 other browsers are objecting.

Ken: 2 individuals from other browsers...  They did look at reusing the visual viewport API and it doesn't make sense...

Sangwhan: as is.. and if visual viewport API doesn't work that way for keyboards then it should be fixed... that was the feedback we had.

Ken: you could argue the same with the insert area ... fixed with CSS..  that was one of my solutions here... if you're using CSS then you probably want something else besides a javascript API.  For keyboard this is an actual issue... Have you ever seen any native app adjust to picture-in-picture?  not even native apps do that.  I haven't heard any good use case for having to work on a windown occluding another window... but for keyboard there is definitely a case.  This is a bounding rect - i think that's OK. 

Sangwhan: I'll set proposed closing...

Ken: I want people to agree..

Sangwhan: the part where viewport doesn't support CSS is a limitation of that spec, it should, but it's not there. It's not even FPWD. Just feels weird. I have the same concerns of the others who raised concerns on the original one.

Ken: I know it was an issue when we worked on browsers at nokia, it's worth solving. It's a big enough issue that I'm okay with it being a specific API for this use case instead of waiting on the holy grail api that might never appear

Sangwhan: we suggested the namespace could be better. That's what my feedback boiled down to. If you can do it somehow with visual viewport that would be nice, but if visual viewport is unusable then the namespace should be unified. Right now its in navigator.keyboard or something.. occlusions are defined there, imgagine another virtual input modality comes out.. navigator.??.occlusions I thought was short sighted

Ken: that's something I would care about, but nitpicking. Unless you have good suggestions

Sangwhan: if you want to enumerate through things that are occluding the content you want to find it in one place

Ken: so something like navigator.occlusions.keyboard

Sangwhan: could be a list, should be in one place. Other parts about implementation details.. 

Ken: I'm okay with having a different name, I'm afraid of ding a list and people have to query what it is. If there's nothing else but keyboard people are going to hardcode it and when you add something it will break. You can already iterate properties

Sangwhan: you have to enumerate because of support for split keyboard?

Ken: no split keyboard is always overlay, you can move it around. It's only relevant in the case.... maybe I'm wrong. 

Sangwhan: split keyboard reqires you to enumerate

Dan: this sounds like feedback we should be giving them in a closing comment and say this is what we think based on our analysis, but it's up to you.. Not design the solution for them. If we can come up with feedback that both of you can get behind we could leave it in the closing comment and close this off.

Ken: yeah

Sangwhan: they don't have support for split keyboard

Ken: i can write some of this feedback now 

Sangwhan: every piece of feedback was bounced back.. we don't know how many ways to split a keyboard, we can't define that, what if it's for accessibility reasons... a corner case

Ken: always the question with trying to figure otu the generic solution, a balance..

Sangwhan: it's not that hard, you need a list of recs instead of a rec

Ken: they'll assume it's one and you'll end up with the same issues. Then you need an API to force developers to not ignore it

Sangwhan: if developers are going to ignore the spec, then...

Ken: if it's a corner case people are not even thinking about that case and will write code that doesn't account for it. Unless you make an API that makes it clear you cannot ignore it

Dan: this is feedback we should provide int he closing comment and making it clear that we think they should be accommodating these cases and working with the applicable communities. Sangwhan mentioned accessibility as a case. They should be working with the community who cares about that case and making sure that what they have accommodates that case. I don't know that it's our role to get into that conversation other than pointing them in the right direction.

Sangwhan: we tried multiple things... 

Dan: we should point that out. We don't feel that our feedback has been received. 

Ken: that doesn't seem t be the case, they have been responsive. Whether they get what we mean.. it's not that they're not listening

Dan: better to provide actionable feedback.

Sangwhan: it was actionable. Split keyboards is actionable, an API change that's actionable... decided that it's not an action they want to take. We were very specific.

Dan: the question becomes do we close it with ambivalent or unsatisfied? I'm hearing more like ambivalent because there are some areas where Ken feels they've been responsive and some where Sangwhan feels they haven't.

Ken: they have taken some feedback. The thing with CSS environmental variables is in the explainer now. Whether they agree or not is different..

Sangwhan: maybe 10%.. the CSS one is the one thing that changed. I would propose closing.

Ken: I'm going to follow up on it.

Dan: finalise and close at the plenary. Come up with feedback that correctly channels the consensus view that we have

Sangwhan: we should mention that two representatives from different implementers have raised concerns and we don't feel that was properly addressed.

Dan: very valid

Ken: do that and link to exactly those comments and summarize what they said.

Dan: we don't have consensus. We have consensus that they haven't listened to feedback from other implementers and should be working to engage more on cases such as split keyboard and that they have listened to some feedback but not the majority of the feedback. I'm happy with that feedback (below) however the one thing I'm concerned about is are we leaving it unsatisfied or ambivalent.. I think we need to take a TAG straw poll on that one. I don't have a strong opinion. I'd rather not leave something as unsatisfied... it seems to be reserved for things that really haven't listened to us at all.

Ken: [posted a personal comment](https://github.com/w3ctag/design-reviews/issues/507#issuecomment-804719637)

Dan: can we discuss at plenary and don't say unsatisfied. 


##### [Limit allowed "accepted" extensions in File System Access API file pickers.](https://github.com/w3ctag/design-reviews/issues/580) - @cynthia, @kenchris

Sangwhan: no response to our feedback

Dan: I'll ping the requester and Chris

##### [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris

Ken: I added people from Angular and Vue to comment - they are going to look at this in detail... I think we should let it be for a while...

Dan: mixed signals about how urgent this is

Ken: needs to work for developers or it doesn't make sense. People who work on frameworks are looking now, which is better feedback than what I can provide. See what they say instead of me trying to come up with feedback. 

Dan: it looks like dominic did make a change to the explainer that clarified the issue that I raised about privacy and security about spoofing URl bar (really good). If we could indicate in our issue that this work is going on that you mentioned so we show some more progress

Ken: their issue 66 there is discussion. Will link to our issue.

Dan: we can bump this issue a couple of weeks and come back to it.

### Plenary Session

Present: Ken, Dan, Lea, Amy, Rossen, Yves, Tess, Peter

Regrets: Sangwhan, Hadley


#### Breakout A

##### Speculation rules

Amy: Left feedback and got [responses](https://github.com/jeremyroman/alternate-loading-modes/issues/56). Wanted to figure out if there's any history with Resource Hints...  Getting moved to WHATWG...? Aked the requestors - they say it supersets resource hints...

Rossen: does that mean that resource hints will be subsumed?

Amy: not sure

Dan: bumped to next week

#### Breakout B

Rossen: [**inert**](https://github.com/w3ctag/design-reviews/issues/610)  proposed closed - can we close it?

Tess: fine with me.

Dan: can someone close it with a nice comment?

Lea: I will do.

[**media source extensions**](https://github.com/w3ctag/design-reviews/issues/576)

Rossen: quick discussion - 

Tess: I will take a look.

Peter: sangwhan said he was ok with proposing close...

[**color adjust lvl 1**](https://github.com/w3ctag/design-reviews/issues/583)

Lea: seems stalled... 

Rossen: we will make progress at the f2f.

[bumped to the 19th april]

[**eyedropper**](https://github.com/w3ctag/design-reviews/issues/587)

Lea: "no no no" on all our feedback points.... seems they are not responsive to our feedback. 

Rossen: I've gone through to make sure the feedback was appropriate.

Lea: responses were not dismissive but did they want the feedback? It's unlikely that you want feedback and then disagree with every single point of feedback.

[bumped to next week]

##### Breakout C

**webxr dynamic viewport**

Rossen: Klaus's [explanation](https://github.com/w3ctag/design-reviews/issues/588#issuecomment-801253226) was reasonable.  I am fine with closing.

Dan: let's close with "satisfied" label.

Rossen: sure.

**first party sets**

Dan: we're formulating feedback - we've had some [feedback from Apple](https://github.com/w3ctag/design-reviews/issues/342#issuecomment-801517385) on the issue.

**virtual keyboard**

Dan: should we close it ambivalent or unsatisfied.

Tess: i think it should be unsatisfied because I think the TAG should not be ambivalent about single-engine tech.

Ken: [discussion of using visual viewport API]... if that feedback from 3rd parties was that it should work together from visual viewport API - but nobody has maintained the visual viewport API...   I think they have listened to some of the feedback.  

Rossen: both of the comments linked to are about using the visual viewport API - they said they looked at it and they didn't think it's the path forward.

Dan: I agree TAG shuld be forceful in our pursuit of multi implementer, but as it's a WG and not WICG. We could say ambivalent regarding design, some feedback has been listened to ands ome hasn't, multi implementer support is still a red flag and if you want to progress it in Web Apps you need multiple implementers. I can write that.

Tess: sounds good to me.

Dan: proposed feedback (for ambivalent resolution):

*Hi folks – thanks again for sending this review. We are going to close this with an 'ambivalent' status.  As indicated above, some of the feedback has been actioned but we feel there are some important points that haven't been addressed. More importantly there is an issue with multi-implementer support and considering the work is going in in webapps, you will need to gain implementer support before advancing this spec to the next stage there. We hope that happens.*

**file system extensions**

Dan: we did have a [response](https://github.com/w3ctag/design-reviews/issues/580#issuecomment-805112372)...

Ken: they say they did look at it but we don't know if they agree or disagree...

Dan: I think they've ack'd our feedback. Maybe we close it?

Ken: Ok I will close.

**App history**

Dan: Ken you got some feedback [from framework](https://github.com/w3ctag/design-reviews/issues/605#issuecomment-804728118) authors...

##### Temporal Proposal

[feedback feedback](https://github.com/w3ctag/design-reviews/issues/311#issuecomment-804496493)



##### AT detectability

Rossen: put it on Breakout B next week.

##### Breakout Rollup
##### Issue Triage
https://github.com/w3ctag/design-reviews/issues/577#issuecomment-805597552
