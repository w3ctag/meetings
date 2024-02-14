# TAG Teleconference
#### 12-14 February 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-02-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240212T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman


### Breakout B (California / Europe)  - [2024-02-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240212T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @LeaVerou, @torgo
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss
* [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman
* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

### Breakout C (California / Australia) - [2024-02-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240212T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman
* [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @martinthomson, @hadleybeeman, @plinss
* [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

### Breakout D (California / Australia) - [2024-02-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240212T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman
* [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou
* [Zstandard Content-Encoding](https://github.com/w3ctag/design-reviews/issues/930) - @martinthomson, @ylafon
* [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss


### Breakout E (Europe / China) - [2024-02-14](https://www.timeanddate.com/worldclock/converter.html?iso=20240212T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [WAI-ARIA 1.3 FPWD](https://github.com/w3ctag/design-reviews/issues/927) - @matatk, @maxpassion


-----


## Breakout A

Present: Matthew, Dan, Martin, Amy, Yves

Regrets:


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

Yves: feedback we already gave still stands... 



### [Review request for Protected Audience](https://github.com/w3ctag/design-reviews/issues/723) - @torgo, @rhiaro, @hadleybeeman

*discussion on what we can say*

Martin: some fairly fundamental flaws...  it fails on achiveing the goals it sets out for itself.

Matthew: as the technical architecture group - are there technical limitations?  Is this implementable?  If not then we could close on that basis - our technical concerns.

Martin: I think that's a reasonable positon to take.

Dan: we could say it's not a fundamental part of the web if we think it's not a fundamental part of the web...

Matthew: not strictly a technical thing...  We need to represent the people that elected us.

Dan: you're right that we need to represent the w3c community, however I think one thing that's part of that is that the w3c community have chosen candidates who have strong views on privacy, which I see as a mandate

Martin: I don't think our role here is the same as a rep in a representative democracy. We've been delegated this responsibility. To that end we need to be true to that to some extent, but what we're really here for is to provide technical guidence at the platform level - that's a broad remit, and we can exercise our discretion. There's a separate control that the w3c as a whole has, which is through the rec process. If protected audience ever gets to the point where it goes to a WG and comes out the other side I expect it would look different, then the w3c has an opportunity to say something about it. I can be true to my own principles, and tha'ts what I'm going to do in any of these things.

Amy: all technology is inherantly political.. pretending it's not is taking a stance in favour of the status quo

Martin: this is how the IAB approaches this problem.. when you ground your arguements in things in which you have expertise, your arguements are much stronger. As the TAG our expertise is perceived as being in a particular area - that's a far stronger position to take. We need to be careful to cleave to the things we're perceived as being competent at. Privacy is one of those things, so we can make arguements on that basis.

Dan: besides the technical comments can we make callbacks to the privacy principles document?

Martin: concerned about this issue https://github.com/WICG/turtledove/issues/990

Matthew: might consensus emerge around the attribution reporting...? or another area?

Martin: TAG has looked at fenced frames ... this is the fundamental flaw with fenced frames... And this is necessary for protected audience...

Dan: what happens when user is using a browser that doesn't allow 3rd party cookies...

Martin: coping mechanisms... e.g. contextual... asking people for primary identifiers... fingerprinting... fingerprinting-adjacent (e.g. looking at characteristics of things people are doing and applying modelling to match interest...)  ... pseudo-science.  Also very proprietary... Throwing ML at the info they have...

Yves: other browsers are not currently subject to the same scrutiny as Google Chrome is... Plain removal or 3rd party cookies leads to political issues because of concentrations of power.

Martin: isolation is unattainable as they've dscribed it. Core property of web platform - you interact with a site, and that site can keep it from other sites that you visit in the browser. The website has an interest in keeping its shared secrets with you separate from other websites you might visit. It's cooperative. There's another form of sandboxing that's increasingly important - preventing a site that you visit from learning that you visited another site when those sites both actively want to know that the same persion visited them. The sandbox we have is not built for that, fundamentally. We need to be up front and acknowledge that's a flaw in the web platform. We don't necessarily know how to fix but we're in the process of fixing it anyway

Dan: removing 3p cookies is part of that. The issue is - there are other ways to do this cross site recognition, there are already holes in the platform. 

Martin: google asks websites to commit that they won't perform cross site recognition. I don't know why you'd ask them not to do that at the same time as giving them tools to do it, it's at odds. If you believed in that registration and committment it would be fine...

Dan: reliance on fenced frames.. which doesn't offer the protections when used in this context that it should be

Martin: it cannot

Dan: we gave a positive reivew on the original version of fenced frames, they requested a rereview because they changed it. That's still open.

Matthew: it's not our job to say how to fix fenced frames, although hard to say this if it's fundamentally impossible

## Breakout B

Present: Dan, Matthew, Amy, Peter, Yves, Hadley, [Lea]

Regrets: Lea


### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @LeaVerou, @torgo

Lea: we got feedback. Not sure what they mean by IWAs are not deep linkable and ephemeral... because you're downloading an app you don't get automatic updates? Presumably internal links would work fine? 

Yves: talking back to the origin - in that case having the webapp serving things locally and perhaps invented a kind of fake origin when it's installed or something like that? That would be definitely bad because you wont' have a proper verified origin and it can be an issue for the security model - repeating what happened for miniapps.

Lea: does that mean these apps cannot talk, send requests to remote server?

Yves: possibly. Not clear.

Lea: should be clear.. regular apps, native apps, do have that capability. Seems like a weird restriction. Especially if users go through this whole thing of downloading the app

Yves: they want to have apps installed to bypass some of the security rules that regular webapps have. I don't know what other limitation they want to circumvent.. filesystem accesss? webusb? In that case should they be allowed to do whatever they want?

Lea: even native apps have to ask for permissions. I'm not sure if the reason this is happening is so the user demonstrates enough intent. I don't understand why they'd go through this whole process of downloading the web bundle and installing it, as long as the UX makes it clear that's what you're doing. More relevant.. They should clarify what they mean by deeplinking doesn't work.

Dan: Why do they need to do this? if this is like a native app then why not make it a native app? Why do isolated web apps need to be web apps, if they're downloaded and installed separately and run in a separte instance and nto linkable and have different security characteristics from the rest of the web... maybe they're not the web. Why do we need isolated web apps?

Lea: the web is many things. The web includes the origin modle, but is also a set of technologies that many people find very convenient. I do think this set of technologies is.. open, not proprietary, most technologies for native apps are tied to a specific organisation. I don't think there is anything that is as convenient as the web for developers and is not proprietary. There are frameworks that let you use web technologies to transpile to native... but I don't think that should be necessary. We should not need electron, it's a workaround because of the lack in the web platform.

Dan: is that the intention? Is it a standardisation of the model that electron has? In which case that's a lot more understandable. We also discussed that as a motivating use cases for the powerful apis idea that we talked about in the breakout at tpac.

Lea: I think it's part of it. I don't think they're trying to cover all of the use cases. We should definitely ask them to clarify. Do we want to see the web's origin model as intrinsically part of the web platform?

Dan: that's the feedback we gave to miniapps. They were using web technologies but without the security guarantees.

Lea: if it is identical to a native app then whether it uses web technologies is an implementation detail

Yves: depends where it is served from

Lea: it's installed locally

Peter: I think IWAs still have a lot of the web security model, still have an origin.. CSPs, cross origin is being applied..

Lea: so it's more secure than a native app. And the UX is similar so users know what they're getting into? One thing is that users don't have permission to install applications into certain environments, would it bypass that?

Peter: weird that it has all these extra security restrictions, but enables direct network sockets which bypasses everything. Is it more locked down or not?

Dan: I think they'd say by putting all those other security structures in place they make it less possible to abuse the things they want to open up further? Like more powerful network apis. 

Peter: but if I can open up a raw tcp connection to anything then origin restrictions are irrelevent. [...]

Lea: that is weird. I don't think should be prevented. I think part of the issue here is they're framing it as installable web applications but there's this extra security thing.. but I'm not sure what they're protecting you against..

Peter: they're adding all this extra security, then opening up the world at the same time

Lea: yes, it's weird


<blockquote>
  
Hello there,

Thank you for responding to our questions, and apologies for taking so long to respond.

> This means that IWAs aren't the deep-linkable and ephemeral experiences that a normal web app is, which is an unfortunate but I believe necessary tradeoff.

Could you please elaborate on this? What is not possible compared to a normal web app?

> Chrome is still exploring what the user experience will look like

We think that’s an important piece of the puzzle. Perhaps since it's been a while since that comments, there is some evolution 
  
</blockquote>


### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### [BBS Cryptosuite v2023 Securing Verifiable Credentials with Selective Disclosure using BBS Signatures](https://github.com/w3ctag/design-reviews/issues/922) - @rhiaro, @hadleybeeman

*We review comments including Manu's call for the TAG to get involved and weigh in on the topic of unlinkable digital signatures.*

Dan: Could we delegate this to PING?

Yves: It could be if it's part of wide review.

Hadley: I second that.

Yves: also PING should have credibility here...

*Dan to contact Jeffrey and float this possibility*

*we need to work on a response here....  we know that PING is working on this here https://github.com/w3cping/credential-considerations .. should we just review their outputs? unknown at this point*

### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

<blockquote>
Hi @linnan-github can you clarify this? Is this meant to be a new review request or does it in some way replace the existing request for this review?  We're still in a kind of hold mode because as noted [in patcg issue 22](https://github.com/patcg/private-measurement/issues/22) we are looking for the group to come to us with a unified proposal.  Do you have any further information on that?
</blockquote>

Dan: *[leaves comment](https://github.com/w3ctag/design-reviews/issues/724#issuecomment-1939228404) and leaves [comment](https://github.com/patcg/private-measurement/issues/22#issuecomment-1939232273) on issue 22*

### [requestStorageAccessFor](https://github.com/w3ctag/design-reviews/issues/808) - @torgo, @rhiaro, @hadleybeeman

Hadley: from Johan's comment from last year it sounds like they need more time.. could be fine for us to close and ask him to re-open... 

## Breakout C

Present: martin, tess, peter

Regrets:


### [Delayed Clipboard Rendering](https://github.com/w3ctag/design-reviews/issues/925) - @hober, @martinthomson, @hadleybeeman, @plinss

```idl
typedef (DOMString or Blob) ClipboardItemValue; // should this be `Promise<ClipboardItemValue>` instead?
callback ClipboardItemValueCallback = ClipboardItemValue(); // this should take a `DOMString type` argument so you don't need a closure always
typedef Promise<(ClipboardItemValue or ClipboardItemValueCallback)> ClipboardItemData; // A promise here is a bit strange.  I might accept that you have three things: (DOMString or Blob), Promise<(DOMString or Blob)>, or a callback.

[SecureContext, Exposed=Window] // should this be transferrable?
interface ClipboardItem {
  constructor(record<DOMString, ClipboardItemData> items,
              optional ClipboardItemOptions options = {});

  readonly attribute PresentationStyle presentationStyle;  // what populates this? options?
  readonly attribute FrozenArray<DOMString> types;

  Promise<Blob> getType(DOMString type); // maybe just `get(DOMString type)`
};
```

### [Securing Verifiable Credentials using JOSE and COSE](https://github.com/w3ctag/design-reviews/issues/899) - @hober, @hadleybeeman

## Breakout D

Present:  Matthew, Peter, Amy, Tess, Martin, Lea

Regrets:


### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @hober, @rhiaro, @hadleybeeman

Tess: last time there had been a unified approach... do you think it's worth spending time reviewing IPA as it is right now? Should we ask the PATCG to circle back when that happens?

Martin: Right, we've had a number of conversations about iterations that remove a persistant identifier, which is generally an all round improvement. We might appreciate guidance on the abstract notion - is it a good idea to support this use case - I don't think anything further than that would be useful

Tess: I propose we close this nicely and ask that they file a new request when the new proposal is ready

Peter: so is this a good idea?

Tess: we know that advertisers want to measure effectiveness, and they'll do so in a bunch of ways that are indistinguishable from cross site tracking. Since we're cracking down on cross site tracking, we're also cracking down on anything that resemebles cross site tracking because we can't distinguish. It's a good thing that people are trying to move off technology that is indistinguishable from cross site tracking. I'm happy that the industry is collaborating on something that is reasonbly privacy preserving, and I want to encourage that. I'd rather see a convergent solution.

Martin: there are a bunch of nonobvious properties of a system like this. We talked about targeted advertising previously. All advertising is targeted to some extent. Also, being able to measure effectively creates the ability to better target your advertising, whether or not that comes with the ability to gain more information about people is orthogonal. Assuming you have some amount of information about people, the ability to measure the effect of advertising on people gives you the ability to realise which people will be more receptive to your message.

Peter: that's my concern. In general I'm against targeted advertising because it does what it does in a harmful way. I get the business case for wanting to measure the effectiveness. I don't want to add technology to the web to just enable a business case. But as long as we can come up with a way that doesn't cause harm - if it can't be abused, I can't oppose it. There is a fine line between effective commercial advertising and effective manipulation of peoples opinions. There's a lot of evidence that social networks in general have caused all sorts of harm this way.

Martin: we thought a lot about this. We concluded the harm minimisation aspects were significant enough to justify doing it, but only on the basis that the privacy tuning of the proposal was sufficiently good. Effectively making sure that the information made available to advertisers isn't good enough for them to do some of the more sophisticated stuff. We may not ever achieve that - really bad information is still pretty good for some people. Some really interesting equity questions that raises. With our primary tool being differential privacy, what are the tuning parameters we put on this? At oen end of the scale it's useless, and at the other end you've not moved the privacy needle at all.

Peter: when it comes to harm reduction, there are lots of existing mechanism used to track and identify people. If we give them a way to get the same effect without that level of invasiveness, but the amount of information they get they don't believe is as good they'll still do the harmful thing. We have to remove the ability to do the harmful thing, and if we can do that, why do we have to give them a less harmful thing?

Tess: comes back to tuning the parameters.. technological intervention to prevent it from happening is... an arms race. If we push things to the point where that happens... If we can push them to a beter place and have it be good enough that they're not going to engage in escalation then that seems like a good thing. One of the nice things about the escalation is that it's more obvious that you're doing it, then it's easier to get to a policy intervention. On the technical side, the status quo in browsers with 3p cookies is widespread cross site tracking that is technologically indistinguishable from a number of otherwise legitimate use cases. Having a mechanism like this means that those things are technologically distinguishable to some extent. It's not as good as what you were doing before - but what you were doing before is going away. So it's adopt this, or do something that's beyond the pale. If we can tune this so it's good enough that people can get 80% of what they want and not run afoul of non-technical interventions, we're hitting the sweet spot. If we push them too hard and they all just do the worst thing, then we're worse off than we were at the beginning. I feel like this is worth trying. I don't know what the end state is.

Peter: so we're not saying no

<blockquote>

We talked about this today during our call, and it's our understanding that there is a promising path forward to merge IPA, PAM and the relevant portions of ARA. Given that, we don't think it's prudent to review the details of IPA since this is subject to change.

We're happy to see these attempts to converge on a way of measuring advertising effectiveness that is more privacy preserving. We encourage you to keep fine-tuning the privacy properties of your proposals, and then to open a new design review request when it's ready and we'll take a look then. Thanks!

</blockquote>

### Protected Audience feedback

Tess: looks good

Martin: +1

Matthew: if we're asking them to do a rigorous analysis of the privacy properties, and to come up with an alternative that doesn't do harm, I'm not sure the last two paragraphs encourage them to do that. It sounds like if they could do that we might be happy with it. Can we shorten it to a more direct call to action?

Martin: I don't want this to be a repeat of the document I'm writing. We need to talk about the use case in relationship with the analysis they're doing. Even with an analysis, we're not yet convinced of the values of pursuing this use case.. which I think is different than what Matthew is suggesting

Matthew: I think it is slightly different, but also we want to have consensus

Martin: I think what is written is correct

Matthew: not blocking

Amy: I'll run it by Dan and Dan can post it

### [Observable API](https://github.com/w3ctag/design-reviews/issues/902) - @hober, @LeaVerou

Lea: Seems to have been validated by author pain points extensively, there are a ton of libraries for it. Does improve a part of the platform that does not currently have the best dx events. It does to events what promises did to callbacks. One minor point is I'm missing a discussion of how this compares to the xisting listener.. does add a property to event objects but doe sit have compelte parity with addeventlistener. Do authors still need addeventlistener for some things? I wouldn't immediately know how to do the same thing as the once option on addeventlistener. As a library author I'm missing discussion on how to create classes that leverage this in the best way. Right now if you want to create a library or a class in the best way that authors can listen to you have to create an event target which is suboptimal - I was wondering if this fixes that. Can library authors leverage observable so they don't have to extend event target. By looking at the explaienr I'm not sure. I can ask. Leaning positive.

Matthew: looks like someone is replying to something... the last comment is answers to questions asked previously, except I don't see those questions in this thread. The issue of really adding something new and different, or could this be duplicating stuff has come up. The things you specifically just highlighted haven't come up so I'd say it's worth asking.

Tess: Meta comment... I get worried when people are proposing a new feature whcih is a variant of an existing feature. We're doubling API surface. Two APIs which accomplish similar things might not be great. Counter example - xhr vs fetch - we couldn't adjust xhr to get to the future we wanted. It's an instructive example. The other concern I have is we can't get rid of the old thing. We can add this new thing which is a variant of the old thing, but it's critical when we do that kind of thing that the old thing and the new thing are defined in terms of a common model so it's clear how they relate and how they interoperate and hook into the underlying platform. If you don't do that you end up in a world of pain. We have enough pain on the web platform. The example from the past is the portal element... a variant of iframe... Maybe they've done all of this work. This is my gut reaction. The benefit of the new thing needs to be worth the cost of the api surface duplication. Maybe the answer is that they've done it and it's great.

Peter: this feels more like a wrapper around events. They're not replacing events, they're polishing the api surface for dealing with them. Which is fine. How does it work with once - my guess would be it's not designed to, this is for things that are going to happen over and over.

Lea: the once option in addeventlistening is not about things that only happen once, only things you want to listen to once. Shorthand to having a listener that you then remove

Peter: that's what I meant. If you only care about it happening once, why would you build an observable? It's not replacing a one time event listening, but something you want to be reacting to over and over

Lea: the idea that it has filtering built in... it seems to have a lot of quality of life improvements.. you might want to only listen once but only have all the filtering of targets and all of that that it supports

Peter: raises the question - do youw ant to keep listening until you find something that passes your filter, or just ignore if it doesn't..

Lea: use cases for both. Another concern - it seems that this is meant to be standardised in a venue that is not tc39. For something like this... we don't want to repeat the abort signal and abort controller situation. This should live on tc39. Kind of a problem that WHATWG is adding primitives that should live on ECMAScript.

Peter: this went through tc39 in the pat and was rejected.. but not necessarily in this form

Lea: what were the reasons? They might apply. addeventlistener carries a lot of baggage. This api should definitely have primitives that work together with existin events, but it should be independant of the DOM. Right now the only solution we have is that we can extend event target to apply to objects unrelated to the DOM. .... No question that the user need is there, but question is this the best solution.

Tess: about the [venue](https://github.com/WICG/observable/issues/46) .. also [relevant](https://github.com/WICG/observable/issues/56)

Peter: ... or are they purely one off? Also promises made thing scomposible.. also meant async and await to hide complexity but give all that power in a simple way. Does this have a similar path?

Tess: really highlights the importance of the venue concern. If this is a stepping stone towards a js language feature it really needs to be tc39..

Lea: worth trying to get right and not just ship something to be done with it. An observable designed well is something that will be used for decades. Should be done by the right venue. They do have a section about standards venue.

Tess: lots of interesting thoughts.. let's post lots of interesting comments.

<blockquote>
  

  
</blockquote>

### [Zstandard Content-Encoding](https://github.com/w3ctag/design-reviews/issues/930) - @martinthomson, @ylafon

Martin: ...small increments can mean a lot for people who have to deal with bloated webpages. This is pretty straightforward. I'll check with Yves.

Natthew: seems like a really impressive algorithm, I wondered about this. What is coming next?

*nice nerdy discussion about codecs*

(mt) Propose the following:

<blockquote>
  
The TAG recognizes that small improvements in efficiency, both in compression ratio and CPU cost, do have real benefits for web users.  There are costs to adding more code to the platform and having more choices available does increase the cost and complexity of negotiation.  However, those costs only mean that the benefits need to be meaningful. zstd generally [performs better than brotli](https://peazip.github.io/fast-compression-benchmark-brotli-zstandard.html), the current best of the (other) standardized options.  Adding zstd would be welcome.

</blockquote>  
  
### [Specification review for fenced frames](https://github.com/w3ctag/design-reviews/issues/838) - @hober, @rhiaro, @hadleybeeman, @plinss


## Breakout E

Present: Dan, Yves, Matthew

Regrets: 

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

*dan asks for an update from requester*

### [WAI-ARIA 1.3 FPWD](https://github.com/w3ctag/design-reviews/issues/927) - @matatk, @maxpassion

Matthew: still looking at this - in terms of the major changes - certain things are fantastic and have been needed for some time - others are natural extension of what they were doing before. They know what they're doing. Worried that some features might be used in replacement of other features they should use... But that's only my personal concern. Those aren't architectural concerns. Some of the things that have been added - e.g. semantics for change suggestions - when supported that will be really helpful. I haven't been all the way through list of substantive changes but so far i haven't seen anything concerning.  Will be done by next week...

Yves: why is ARIA description just a string? You may want to have translations?

Matthew: there are good reasons for it - and the precedent has been set a long time ago -- there used to be "ARIA described by" pointing to an ID.. The hope is people use existing text in the DOM... For providing an accessible name - it usually comes from the content of the element - or a label - but ARIA gives you a way of overriding.  I understand why they've allowed this - but needs to be stronger in the documentation - don't use the string attribute if you can avoid it.  If you've used "described by" and you also have description the described-by takes precedence. I've been told by accessibility experts that this can make translations harder... however precedent has been set... They've also now got "ARIA details" - it seems this more heavy descirption - but this is an ID Ref - not a string. It's like a description but expected to be more detailed...  You've got a name (short), described by (longer), details (a bit more about it). Pretty certain that they've called it that on purpose... 

Yves: it seems inconsistent...

Matthew: Agreed... however overall it looks good. It may be worth asking some questions. This isn't a horizontal review request so I think it's worth taking a little longer and noting those things down...

Yves: should *comment* be *comments*?

Matthew: it's a tree so *comment* is appropriate.  Also braille label and braille description - also string values - that makes more sense. 
