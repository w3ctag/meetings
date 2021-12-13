# TAG Virtual F2F - Madripoor

Week of 6-December-2021

[Agenda](agenda.md)

This W3C Technical Architecture Group virtual face-to-face meeting was held as a series of 26 breakout slots over the course of the week of 6 December, 2021. The mintues are presented as breakout notes and are not necessarily chronological.  Many of the breakout slots are subdivded into breakout A and B - in which case a note of who attended each breakout is made.  In some cases there are some additional "rollup" notes presented in line where additional substantive discussion took place. 

Present at this F2F:

* Daniel Appelquist (Samsung Electronics) (Chair)
* Rossen Atanassov (Microsoft Corporation)
* Hadley Beeman (W3C Invited Expert)
* Kenneth Rohde Christiansen (Intel Corporation)
* Amy Guy (Digital Bazaar)
* Yves Lafon (W3C) (staff contact)
* Peter Linss (W3C Invited Expert) (Chair)
* Sangwhan Moon (Google)
* Theresa O'Connor (Apple, Inc.)
* Lea Verou (W3C Invited Expert)

## Breakout 3A

Participants: Ken, Yves, Lea, Dan

### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652)

Dan: I understand from talking to the group chairs that there is work ongoing on figuring out how to address the issues we've raised.  No response on our issue yet but I think the work is going on.

### [Gamepad API input events](https://github.com/w3ctag/design-reviews/issues/662)

Dan: Can we close this off?

Ken: My concern is .. it's unclear .. two different events but can't use both at the same time... Two modes of getting the events... coelesced and non-coalesced.  Grey area...  Should there be a start function like we have with generic sensors?

Ken: [writes comment](https://github.com/w3ctag/design-reviews/issues/662#issuecomment-987700244) regarding side effects... 

### [State extension for JS Self-Profiling API.](https://github.com/w3ctag/design-reviews/issues/682)

Dan: so one feedback is that they jump right into talking about JS profiling without talking about the developer or user need.... A sentence such as "this is in service of making web apps more reliable" etc.. might be helpful.

Yves: can it be used to detect on the mobile if you are on battery saver mode... If you're profiling and you realise youre running slower than usual...

Dan: Fingerprinting issue?

Lea: seems like a stretch

Ken: Agree

Dan: Worth asking the question - have they considered how this could be used by fingerprinters and mitigation strategy...?

Ken: this is the extension of the existing profile API using markers...  adding a marker to what's going on... so more detailed information...  The developer marks what they're interested in .. they get a timestamp .. 

Ken: not just scripting... also css, etc...   system might work well on your super fast machine .. but might be very expensive layout on older devices...

Yves: if it's just markers then...

Ken: The sspec is called js self profiling but profiling things that are not javascript...

Lea: given that these markers are predefined the scope seems limited.  At first I thought it was general purpose but doesn't seem to be the case...

Ken: you give the profiling a set of markers...

Dan: any cross-origin info?

Ken: no it's only for that tab - only for that origin.

Dan: seems like they need to be explain [the mitigation](https://github.com/WICG/js-self-profiling/blob/main/markers.md#privacy-and-security) a but more...  [leaves comment](https://github.com/w3ctag/design-reviews/issues/682#issuecomment-987685841).

Ken: fine with the API...  No difference.

Dan: it does enlarge of the scope ....

Ken: Definitely.  Maybe it would be nice if ... it's good gor UAs ... 

## Brekout 4A

Participants: Amy, Dan

### [Same-origin prerendering triggered by speculationrules](https://github.com/w3ctag/design-reviews/issues/667)

Amy: they responded to question about status but they haven't responded to the issues I left in their repo.... So not sure there's anything else we can do at the moment... [comment](https://github.com/w3ctag/design-reviews/issues/667#issuecomment-987733917)

### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679)

Amy: all of the use cases are from the perspective of the user agent... the browser needs to x, etc... no privacy & security review... About the browser deciding what needs to be in focus... They've not explained why it might benefit the user...  One security concern about clickjacking...

```
Hello, @torgo and I looking at this in our virtual face-to-face today. We noticed the problem statement in the explainer is from the perspective of the user agent, rather than the end user. Would you mind adding some examples/use cases/scenarios of how the end user of an application benefits or is affected by this feature? We appreciate that you have noted one security concern in the explainer; do you have an idea of when you will be able to complete the [privacy and security questionnaire](https://www.w3.org/TR/security-privacy-questionnaire/)? Are you expecting to take this work to the WebRTC WG?
```

## Breakout 5A

Participants: Kenneth, Rossen, Peter

### [Pen Events API](https://github.com/w3ctag/design-reviews/issues/553)

Still pending external feedback, pinged and punted.

### [Viewport Segments Property](https://github.com/w3ctag/design-reviews/issues/689)



### [Foldable Device CSS Primitives](https://github.com/w3ctag/design-reviews/issues/690)

## Breakout 6A

Present: Ken, Tess, Hadley, Rossen, Lea, Amy

### [Compute pressure](https://github.com/w3ctag/design-reviews/issues/621)

Ken: Intel is taking over, not sure of status, will reopen the issue when we're ready. Proposed close?

### [HTML Popup](https://github.com/w3ctag/design-reviews/issues/680)

Ken: there's a comment from Peter.. Is this an early review?

Tess: second time asking. Since then, prototype in chromium complete. Later than early review.

Ken: a lot of issues.. a lot of work still ongoing.. lots of crucial stuff discussed... is this really time for review?

Tess: might be a mistake to review something that is likely to change significantly. But Dom has been doing the work of the TAG for us here... he's forcefully making points.. if we're going to say we hold off on review until things settle down we should say something stronger about the content of that churn. Sometimes when groups come to us for review they ask for feedback on a thing they're happy with. But we could influence this debate. I don't was us to be totally neutral.

Ken: does seem like they do have some agreement now

Tess: haven't got that far... say something like there's a whole lot of discussion and a gap between what you have consensus on and what is written down. Please come back to us when you have made the text reflect consensus..

Draft closing comment:

> Hi everybody! Thank you for your patience as we've taken a while to get back to you on this one. Special thanks to @domenic for his thorough review of this feature. We're happy to see that there's been a bunch of productive conversation on this here and in various OpenUI issues. It sounds like the direction you expect this to go in is pretty different from what the current documents describe. We'd like to hold off on reviewing until you've updated the documents to match the current understanding. Please let us know when to revisit this!

### [Launch handler](https://github.com/w3ctag/design-reviews/issues/683)

Tess: reading explainer, you need a lot of context, assumes you know a lot

Hadley: nothing on user need

Lea: use cases also assume context

Ken: found it very confusing.. and the repo has other proposals.. commented for that

Lea: i can think of cases where this is user hostile. Google maps on mobile, the native app doesn't let you open multiple tabs and compare different routes. If you click on a google maps link it overrides what you already have open. It looks like this is trying to emulate this behaviour on pwas as well. I think there are many cases where that behaviour is not desirable

Ken: is in other cases. Every time I open Teams... super annoying. On the web it puts you in control, right click open in another tab is going to work

Tess: but does it? if I click on a maps ink maybe my browser opens in a new tab or maybe it gives the same bad behaviour Lea described

Ken: should make it clear that right clicking open in a tab should be followed, not use this infrastructure. Should be only for a regular click.

Tess: I thin kyou're right, there needs to be explicit mitigation. Lea's broader point is worth expressing - this feels like taking some of the hostile behaviours of native platforms and making the web as hostile as native

Lea: users dn't just click on links in a browser. In a email client, how would you open a new tab?

Tess: yep. I have a maps thing that I've installed and I click on a link and then state is blown away. They do have an example of a music player. That's a good example. If I click on a play a song thing people want that to play instead of the song I'm currently listening to

Lea: but do you want to lose your state in the other song?

Tess: good quesiton

Ken: it's not navigating

Tess: it's the same as the maps app.. opens my existing music player which is already playing something and blows away the old thing.. how do I go back to what I was doing? Maybe I had a playlist? But I click on a song in another app and there's no way to get back to my history

Ken: you can configure this. Configure existing client.. don't know if that's replacing it or adding a new history entry. navigateexistingclient.. assume it adds another history so you can go back to where you were. That would be my guess but good to get that clarified. There isthe option to use this api where you're not replacing the existing client, gets an event that someone tried to load this new url and you can act on it, that's the consumer api. I don't see how the existing client works.. what event do you get?

Tess: mod params get queued into launch queue

Ken: hw do you know it's changed? Oh so it's always called...

Tess: I like that part of the design, it's well done. Lea's underlying point stands

Ken: replacing the existing client api

Tess: this is a great example of the race to make the web equal to native without realising that the web has unique properties. This might be a feature that making the web as bad as native as opposed to equivalent functionality

Ken: the only thing I disike is replace existing cient. If it added a way that you can intercept a new url loading and you can act as a nice way in an app. S you don't lose your state. Like if you click a song, like youtube asks if you want to play a song or addi tto a playlist. 

Tess: The app has to do that. Most apps don't. What Lea is saying.. what we see on native platforms, the app author doesn't do that.

Ken: you have an api here, you're opting in as an app devleoper. You have to set the route to this feature, and to set a consumer. If you dn't do the right thing you can't trust the app at all

Tess: why should we help app developers be bad..

Lea: if we don't help them they might move to native....

Ken: i find it annoying clicking on a link and music is launching in another spotiify instance.. i would like it to focus it and ask if i want to play it now or put it on the playlist. I don't like the reloading, I hate that on mobile. I'm watching so enews and click on soething else andwhat I was doing is gone and no way to get back to it. What URL was it? That is very hostile on android. 

Lea: I can see that point as well. I've often been annoyed at things opening new windows for every single thing.. compared to native app.. on the other hand I also don't want to lose my current state

Ken: if we forget about new client.. it allows the app to do that. It allows the api to say I'm going to handle this, and set a consumer. Consumer gets the new url and they can decide, save state, if they do it right

Tess: my cocnern is that's not the default. Suppose this was an extension of the history api. The app can push and pop state.. the browser would do the right thing without the app developer having to do anything

Ken: how people design these single page apps is going to be worse. Then they're not going to handle it, and their framework is not going to handle it. IN that case it's going to be easier for them to handle it and say they're doing another view. 

Lea: pwas don't have a back button

Ken: they can... on android... at OS level I can always..

Lea: specific to android

Ken: on windows now.. time bar..

Tess: respond with worries and excitements... Lea's example of blowing away state in eg. a maps app. Maybe you need that in some cases. We said this explainer is written for people who already know what it's about.

Lea: I can comment

Rossen: the throwaway state... state handling is very application specific. I'm not sure we can or should generalise here. 

Hadley: nothing wrong with saying to implementers you might want to consider very carefully what you're doing with the state

Rossen: best practice guidence is always welcome. From an API point of view, state management is very application specific. So I agree with the point, I'm just not sure in general what else can be done besides saying do better.. To me this is a pretty generic warning that is very inactionable. It's almost a comment for the sake of a comment.

Ken: i think they can remove navigate new client. If people want that they can add a consumer that reloads. You can reload from the DOM.

Rossen: from capability point of view, some things that are not obvious to me.. this is written in a pretty contextualised way... how do you deal with multiplicity. If I have 3 different mail client apps and I click a mailto link which do I click? Is it contextual based on where it starts from? Starts from a browser vs slack app vs twitter app... always the same? does it stay?

Tess: depend on platform? One case is I could be in some map application and tap inside mail app it probably knows to handle it itself.. other case is you're in some other app and its almost always the system default.. there's some underlying platform

Rossen: that was my expectation..

Tess: they don't say that. That's the status quo in the world (maybe) but that's nt in the explainer. They should add it..

Rossen: the scenarios here are I fall back to system defaults in which case there is a file handler registered somewhere that's going to go and handle it correctly... is this the same if I have the second mail app open? My web mail app open? Would that same experience happen? It's unclear to me. Other question around breaking out of this... on one side I agree with having control of an in app experience as much as it makes sense, at the same time breaking the ability to have multiplicity here bothers me. So we should add these comments?

Tess: a bunch of comments... I'll do the one about the explainer assumptions

Rossen: I'll comment about being explicit in terms of behaviour about default file handling. Related proposals that they list here.. are these mentioned becuase they're complementary, or because they're similar but different... they are related how? Do I have to go and read all of these?

Draft comment:
```
Hi @alancutter,

We looked at this today during our virtual f2f. @hober and @kenchris have already relayed some of our questions above.

Bigger picture, one of our concerns is that this facilitates user hostile behavior, where new content entirely replaces old content and the user loses their current state.

For example, consider the native Google Maps application. Clicking a maps link from anywhere else *replaces* your current state with no means to retrieve it or toggle between the two (e.g. to compare routes). Even in the music player example, does the user desire for their state to be entirely replaced, or merely for the previous song to be paused?

We understand that it *is* possible to maintain the previous state with custom coding, but we are concerned that the easiest, most straightforward thing to do is what most native apps do, which is to entirely replace user state. We'd love it the Web could do better.

What are your thoughts about how to address this?
```

## EWP

Present: Dan, Hadley, Amy, Sangwhan

### [Intro: add paragraph about balancing principles, for #62](https://github.com/w3ctag/ethical-web-principles/pull/64)

[discussion on whether this is additional 'hedging']

Hadley: agree but important since these aren't the actionable principles these are guidelines to help us review...

Amy: it's hedging but it needs to be there.. need to hedge in this context as principles have no heirarchy, depends on context

Hadley: how to make this useful for other people?  We kept going through design reviews and saying making this choice is complicated, there were patterns going back to something bigger. Principles as written are a bit nebulous and harder to make practical than design principles, which we did deliberately. Is part of the reason we have confusion because people are trying to make them practical and we haven't designed for that user need?

Dan: yes, I've had people ask me that it doesn't have any actionable advice, and I have to say that's by design. That clears up their misperception. Do we want wording about that? Might be shooting ourselves in the foot. Want to think about criteria by which we would say it's ready for w3c statement.

... I think the PR is okay.

Hadley: text is fine, looking at how it fits. Let's put it in and see how community responds.

**reviewed and approved the PR - squashed and merged**

### [Editorial pass](https://github.com/w3ctag/ethical-web-principles/pull/65)

[discussing contents of the PR]

**Agreed to merge and merged **

### [Sustainability Issue](https://github.com/w3ctag/ethical-web-principles/issues/66)

Amy: how do we define civilisation, moving forward etc... "beneficially advance" for whom? 

Hadley: [we should put this together with how principles fit together....]

Hadley: we should avoid backing economic models.

Dan: there's a perception that the sustainability principle demonises energy production for systems that require energy unfairly and doesn't take into account the benefits to society that can be inherant for systems that rely on on energy production. The way it's currently written is too far on one side. We can't say energy production helps civilisatin move forward, it's a blinkered way to look at things, but we could say something like whilst there are cases... energy production can be beneficial to society and also be damaging to society and .. if you take a look at 

Amy: energy production can't be talked about as a blanket term because different modes have different impacts...

Hadley: also heavy metals in chips - also a sustainability issue.

Amy: planned obselescence, hardware manufacturing ... 

Amy: probably not an issue they're trying to argue because they're talking about energy production... We could say that not all energy production is equal... anything you want to power with electricity you should think about how it is produced... not just the web... so seems out of scope.

Amy: "Considering the status quo," "if all energy is produced using fossil fuels then we should reduce".. All part of the context. 

Hadley: The principle is very heavily weighted towards carbon emissions... 

Dan: we got feedback early on about adding wording about carbon emissions. Sustainable tech advocates asked us to add more specific wording.

Hadley: maybe we should start out with something more general - start with "the web is a potential cause of environmental damage" and then talk about carbon emissions, hardware production, .. less demonising carbon emissions, more the general point and carbon emissions are part of it

Dan: should also ack that the web can be a net positive for environmental.. if you look at remote working. We should not just say that it's an environmental damage. Something like although the web can be a positive.. have positive impact on the environment... there are aspects that are negative. eWaste also fits in with hadware... mining of materials and also constant churn of new hardware creates an ewaste problem

Hadley: immediately actionable that people can make better websites, but can't easily solve the heavy metals

Amy: [will make a go at re-writing para]

```
We (@torgo, @hadleybeeman, @cynthia and I) discussed this in a breakout at the TAG face-to-face today.

I want to acknowledge that "power consumption" and "emissions" are broad generalisations that are not actually that helpful when thinking about environmental impact of technology. All power generation is not created equal, so talking about "more" or "less" of it in a broad sense doesn't mean a lot. However it isn't in scope to turn this section into a primer on power generation. It *is* in scope to remind the reader to think beyond their immediate world view about these issues, which is perhaps where a lot of the knee-jerk reactions for/against certain technologies come from.

Terms like "civilization" are extremely subjective and vary across cultures (and time). What is "civilized" to one group of people may be extremely objectionable to another. I think perhaps what is meant here is more like "society" in the sense of "everyone in the world".

I want to be careful with using "net" (emissions, efficiences, benefits, etc) because for the most part this is extremely difficult if not impossible to measure objectively, even if you constrain it within a particular time frame. Weighing the perceived benefefits against perceived costs of a particular technology can result in completely different judgements depending on a person's priorities (and ability to predict the future). It also feels like there's a risk of an assumption of utilitarian ethics here, but it is also out of scope for this document to suggest a particular way of weighing up ethical considerations (thousands of years of philosophy study hasn't figured out yet afaik).

Following our discussion today and this and related threads, I'll rewrite the sustainability principle to make it say more what we mean, and hopefully make it less weaponisable.
```

## Breakout 10A

### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523)

Dan: is [origin](https://github.com/w3c/miniapp-lifecycle/blob/main/docs/explainer.md#miniapp-origin) the same as we think about origin?

Sangwhan: no it's not the same.

Dan: Well from an arch perspective we could ask them to clarify how their concept of origin fits together with the web security model's version of origin.

Sangwhan: concerns with this [general] approach - redefefining a lifecycle... miniapp will be cached in the hosted native app for some duration. It's packaging to some extent.  There's an analog to page lifecycle except for putting things in the foreground or background...

Sangwhan: are they still using their own URI scheme? (as referenced in the explainer)

[privacy & security](https://w3c.github.io/miniapp-lifecycle/#privacy-and-security)

Sangwhan: they have the concept of running in the background - this is different from the mode we usually operate on. A user thinks they dismissed a miniapp and gave geolocation access - it's running in the background and user doesn't know it. That's a privacy risk.

Dan: isn't that why when web apps want to do this kind of thing they use serviceworker ...

Sangwhan: there's a reason why you can't do certain things in serviceworker - this kind of breaks that model.  If you switch between two geolocation apps - when you give geo info to a background miniapp it will look like your current foreground app is the one using it... It will be telling you that the geo info is being used by the superapp shell.

Dan: shouldn't we be guiding them to make use of serviceworker instead of having this separate notion of foreground and background miniapps?

Sangwhan: Serviceworker doesn't provide what they need. it just keeps local cache proxy data up to date... their use case is more subtle than that.  

Dan: when I launch twitter and launch pinafore (PWAs) I can switch between them seamlessly no problem... what is the difference?

Sangwhan: you would definitely not want to grant a miniapp in the background a permission... for a PWA on Android when a webapp is using a permission you're switching between origins so it's clear where the permission is. With miniapps you have app nesting.  We should probably bring that up.

Dan: [can't they just use service worker?]

Sangwhan: I think background is entirely for lanuch performance.  I can see why they are thinking in this way.  The urge to make the launch faster.  PWA launches are time consuming.

Dan: *Outlines the lifecycle of walking into a Starbucks and paying with Alipay - in both PWA and miniapp world - would both involve a starbucks origin and a web payment "application" using Alipay.*

Sangwhan: this could be made to work in conjunction with the web and PWAs - but they are re-inventing because they have existing implementations.  It doesn't follow the common principles of the web.

Dan: I think there are 2 levels: 1st level is using the common principles of the web ; 2nd level is maybe making more use of PWA stuff.... right now we have neither.

Dan: could we push on web security model - origin...

Sangwhan: yes - and the privacy & security section of the spec doesn't really discuss privacy & security.  General concerns: a lot of reinventing the wheel happening. The reason why the web is the way it is - is that we have iterated over multiple decades to have the right security model to protect users.  This reinvention repeats the same mistakes and has to reiterate.  For that reason we can't be supportive of this isolated ecosystem and would prefer to build towards a convergerd web.

Dan: back to serviceworker - if it doesn't work for them because it doesn't provide the functionality they need for miniapp then bring those requirements to the table in webapps wg so we can work on that.

Dan: they did talk about building extensions to webapp manifest...  so why not extensions or similar to service worker, or others... right now we're on a path towards greater divergence..  We need a meeting of the minds between PWA and miniapp people...  Both are inventing new things and these things are nor compatible.

## 11a

Present: Dan, Hadley, Amy, Yves, Peter, Rossen

### [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342)

Rossen: I get .. but what does that mean for a next step where the enteprise acquires a different company with different constituents, has a different privacy policy, etc...?  I don't see what's stopping anyone from having a hostile acquisition mode where people acquire sets.

Amy: I think K would say that's addressed by regulatory. I also raised what about cooperatives... equally owned by members.. could have one set ...

Dan: Aren't we talking still about hard limits to the number of sites in a set?

Amy: there's an [open issue](https://github.com/privacycg/first-party-sets/issues/29) on that...

Dan: sets for a specific reason, to support a user journey... a company could have multiple sets.. a set to facilitate a user journey, just because the buy another company doesn't mean it automatically gets added... they could have a different set

Rossen: it's a good point but...

Amy: they *could* but they don't have to... The numbers they were looking at for that max set size is 300, 1000.. not small..

Rossen: let's say Meta didn't have Instagram... all of a sudden they get Instagram ... has user generated content which is not part of their other network..  now you join these user graphs - creating from a user's point of view an undesirable experience... 

Dan: because they could put them into the set together, following that logic, they wouldn't need user consent in order to establish a linkage between that users facebook account and instagram accounts because they would be under the same set so they'd be privy to the same cookies.   Doesn't that bring up the idea of permission prompts?

Rossen: You can extend your graph without consent. Say this happened today... the domains are there, networks are there, users etc, but you don't have cookie sharing. They're stll third party from the pov of domains and the way they currently stand. That automatic cookie sharing that would be allowed by adding them to the same set and allowing cookies and state to flow between the two isn't there.

Dan: what happens now without fps is facebook acquires instagram and then they decide they want to merge user data and they ask the users of instagram to authorise facebook. There's a user permission step that the users have to agree to a t&c or to authorise so data can flow back and forth. In the fps world maybe the equivalent of that is the browser says "the set you were in now has a new party" - inform the user and make sure they understand they're okay with it. Or at the ifrst use of anything that includes a FPS the browser needs to tell the user who the set includes

Amy: there's language in there about surfacing it in the UI... Your point about a new party appearing in the set ... what if the answer is no. User is already invested in the services. It's not meaningul consent... 

Hadley: also where regulators might get into the game -- if they approve the merger. When facebook bought instagram the dp regulator approved the purchase on the grounds that the data would never be mixed and then it was mixed... Another factor.

Yves: can a first party set be part of a business relationship -- result of a partnership? or only same set of compamnies?

Amy: the idea is the same company.

Yves: to be able to do some good statistics you might require you to be part of a first party set.

Dan: I think that's ruled out but the issue is it's not clear how they would police it.

Amy: In terms of how they police it - you can't check every site... their response would be spot checks. I think it's not good enough. So we have a loop.  But: first party sets is use caseless by itself -- and leaning on this for same party cookies - and chips - maybe we should push back and say "come back with a specific use case"...  If we were just gonna review same party cookies - and same party cookies redefined what a party is in order to have same party cookies then we might be able to think more productively about it.

Dan: trying to think what actionable things they can do to make something that will pass muster. We've gone round about different things. Early on technical only enforcement came to mind. There's no need for an enforcement authority or curation of allowlists or blocklists or anything like that if everything that constitutes a fps is done in some way that is technical only. However that would rule out that fps are only the same entity or ownership because that's impossible to determine from a technical only perspective. We could determine these sites all agree to be in a fps together. We could determine that no site is in some other fps. We could determine that fps are not very big, there's an upper limit. There might be other technical mitigations on top of that. All the domains need to be registered under the same registrar or something... or all need... some discussions about this already. Seems to have **been rejected**. And even in the case of tech only enforcement you still nee the browser to play the role of trying to stop abuse as a tracking mechanism

Yves: being able to define what's in the set gives an unfair advantage over people who would be required to pay to be in a set..

Amy: if we try to help them out - we should go back to what is it for - if it's for sharing cookies in a world where there is no third party cookies - how does that help the user? and if you enumerate the user needs are they indeed a match for what first party sets does?  Can we do something better?  Or do we not want 3rd party cookies in any form - cookies 

Yves: SSO?

Amy: yes it's one of the use cases... 

Dan: for SSO we need Federated Credentials Management. People already do SSO.. before fedCM comes along you don't need that because..

Peter: losing all 3rd party cookies might break ... something.  There are other people working on fixing that.

Dan: I don't buy the argument that the web will break without 3rd party cookies.

Peter: but some people's business models will break.

amy: what if it's off by default and users had to explicitly enable one 1st party set at t a time... or would it just mean users are compelled to install an extsnsion which turns on a bunch of fpss.

Hadley:

Rossen: would [a non-technical user] be able to make sense of it?

Yves: they will turn it on because there will be instruction on the web telling people to turn it on...

Dan: or they'll use a mechanism of trying to trick people to prove you're not a robot by turning on fps... people are used to that now

Peter: i think it should require user consent and if the permission system is broken we should fix that.

Amy: I can't see a way of getting meaningful consent from users for all of this

```
Hi @krgovind we discussed today at our [virtual f2f](https://github.com/w3ctag/meetings/tree/gh-pages/2021/12-Madripoor)...  We're concerned we may be going around in circles on this.  One idea we had to break the cycle is to refocus our attention on a specific use cases linked to FPS - e.g. SameParty cookies or possibly CHIPS. This would enable us to go back to the problems we're trying to solve and maybe find better ways to try to solve them.  Would that make sense to you?  We could then take a look at the specific user needs addressed by those designs and evaluate FPS on the basis of those needs.  Yes: we had previously said that we would hold off on reviewing Same Party Cookies until we reviewed FPS - but by talking about Same Party Cookies in isolation we may be able to make some progress here. 
```

Amy: what do we want to say about tightly coupling it to eg. same party cookies instead of having fps as a standalone thing?

Dan: different from the layering advice we usually give, but I agree. Take some of the concepts from FPS and package them up with same party cookie and solve the problems that same party cookie solves without creating this general thing

## 12A

Present: Ken, Amy, Hadley

### [Secure Payment Confirmation](https://github.com/w3ctag/design-reviews/issues/675)

Hadley: looks early, mozilla and webkit haven't taken a stand

Ken: seems to be adding webauthn to payments.. assumption.. this is because eg in europe you have this 3D Secure and a lot of these could be delegated and use webauthn instead. The way I'm seeing this you use it the first time, do a payment then it uses a backchannel like 3DS to ask for credentials, whatever your bank or card is, but from that point it can register things and say use fingerprint in the future or something like that using webauthn. So in the future you just use yoru fingerprint r face to do 3DS. That is how I read it. Not really said in the explainer. What is a webauthn credential? Assume it's a fingerprint..

Hadley: proposed solution... says it builds on top of webauthn to add payment data

Ken: and to relax assumptin to allow api called in payment context.. I assume that means I can use my webauthn instaed of 3DS. Assume the way it works is I make a payment, goes to my bank or whoever, they have auth system like 3DS, they can say do you want to register with webauthn as well do you want to use that in future? and you can decide to do that on that device. But the text is very complicated..

Amy: I don't think I"m getting the same reading but I don't know it well... but we shouldn't be guessing what it means, explainer is not well written, not focussed on user needs

Hadley: the proposed solution is after you have registered with a given device and a given provider

Ken: I assume you do that on the first payment, and in the future just log in with your credentials. If I say yes it will register that on that device. A bit like how it works on native apps today.

Hadley: the 9 step process is what happens for any transaction after you've registered. That answers the question I had about the difference between registering and transactins after the registration. Be nice if they could explain the registration process

Ken: later it explains they're extending webauthn

Hadley: what else?

Ken: lots of improvements to explainer.. assumes you know about webauthn.. some examples of webauthn credentials.  Generally I think it makes sense. Would make it more effortless to do payments. Today I have to sign in with this national ID.. open an app.. swipe... and people are using less secure things with phone numbers instead. Feature makes sense. Not sure if it's right with webauthn.. technicalities I don't know.


```
Hi, @ianbjacobs and @stephenmcgruer. We (@rhiaro, @kenchris and I) are looking at this in our [W3CTAG face-to-face](https://github.com/w3ctag/meetings/tree/gh-pages/2021/12-Madripoor). We are scrambling to follow the information flows in the explainer (perhaps a diagram would be a clear way to communicate this?), and to see how this works from a user's perspective (especially the registration process). Would it be possible to add those to the explainer? 

Also, it seems like the explainer assumes a strong familiarity with webauthn, which seems complicated in light of [the ongoing work with them](https://github.com/w3c/webauthn/issues/1667). It would help us a lot if you explain in plain English how you see those working together, again especially from the user's perspective. 

And finally, for our notes: we are reassured to see how much you're focused on privacy, based on the issues in your repo and the thorough Security and Privacy questionnaire responses. That's important in this area and we're pleased to see how much emphasis you are giving to it.


```

[issues rabbitholes]

https://github.com/w3c/secure-payment-confirmation/issues/128

https://github.com/w3c/webauthn/issues/1667

Hadley: did we review webathn?

Ken: [2015](https://github.com/w3ctag/design-reviews97)..... and [2020](https://github.com/w3ctag/design-reviews/issues/577).. doesn't seem to have been deeply reviewed

Amy: I think there was a breakout about payments with Ian a while back that I wasn't in

Hadley: me neither

### Process tangent

Amy: WebAuthn review feels like a pattern - of really big specs that nobody has time to dig into for ages, and then time runs out and a too small review is done. Or they come too late in the process to really do much about it so we just feel like we have to sign off. Would be good to spot these early and get a meeting to have them explain it to us instead of sitting on them for ages.

Hadley: definitely a pattern. Be nice if we could engage WGs earlier in their process

Amy: something like a TAG checkin with a small explainer and their main issues, doens't have to be formal. 

## 15a

Present: Ken, Yves, Dan, Sangwhan, Lea, Hadley

### [Design Principles PR290](https://github.com/w3ctag/design-principles/pull/290/)

Sangwhan: ...don't think market dominance should be part of the design principles... 

Dan: Agree.

Lea: we have design principles that are not technical ...

Sangwhan: contents of our design principles doc does not snipe on a specific implementer.  that said, explicitly calling out features that only have one interested imlementer - not a technical issue more of a policy & process question.  

Dan: kind of agree... we could say something like "features that are only implementable by one vendor are not appropriate.." or something similar.

Sangwhan: intent of original issue is that designes should be made in a way that multiple implementations should be possible. If we invert that sentence then that's a different tone we're setting.

### [Private Network Access (aka CORS-RFC1918)](https://github.com/w3ctag/design-reviews/issues/572)

Yves: the goal was to ensure legacy devices that cannot be updated can still be available ... otherwise blocking everything else... also focusing on the difference between private network and local network... difference between what you have in your LAN and a private network.

[reviewing response](https://github.com/w3ctag/design-reviews/issues/572#issuecomment-980103232)

Yves: the first part - part of dealing with legacy devices that might not be upgraded to support this specification but not related to this specificaiton directly.  On the 2nd part it's up to the user agent to decide what devices they want to surface or not.  There needs to be agreement between the browsers.  But not something that can be decided in the review.

Dan: Can I suggest that we close this then with a "satisfied"?

Yves: yes.  I will close it.

### [Feature policy for Keyboard API](https://github.com/w3ctag/design-reviews/issues/685)

Dan: fingerprinting issue

Yves: yes but less intrusive than the font list

Lea: I think this feature adds a lot of value

Sangwhan: this increases risk for outliers - people who use minority keyboards.  

Yves: accessibility devices as well?

Sangwhan: A small subset of users who rely on AT can be fingerprinted...  So if your IP is french, your language is french, and keyboard is us-english then that fingerprints you...  However the gains outweigh the risks.  So many other ways to detect these kinds of outliers.

Yves: I agree.

Dan: Someone want to leave a closing comment?

Sangwhan: good idea.

### [Add first pass at principle about designing around third-party tools](https://github.com/w3ctag/design-principles/pull/351)

Dan: taking a look now....

## 17A

Present: Dan, Amy

### [Conditional Mediation](https://github.com/w3ctag/design-reviews/issues/692)

Summarizing: we discussed the user flow of webauthn as documented in the explainer for this issue and for #686.  We went through the design from a privacy & security perspective - looking at how authn credentials are not exposed to the web app unless and until the user completes the user flow.  Also 

```
Hi @nsatragno - we're looking at this (and the general topic of making webauthn more friendly) at our virtual f2f this week.  A couple of questions: if the user *does* have an appropriate credential but they don't want to use it - for example, they want to log in as another identity - then what information does the web app know about the user's choice?  If the web page displays a username and password dialog at the same time that the browser surfaces a webauthn UI of some kind to pick a credential, isn't that going to be confusing to the user?  Since the web page won't know that the browser is supplying this UI (which seems important from a privacy & security standpoint) how is that expected to work? We can see the screenshot in the explainer under Conditional UI, but it isn't clear if this is the current status quo or if this is the aspirational UI.

Also: can you please bring the (well written!) explainer over to a markdown file in the appropriate webauthn repo? Also can we suggest that you link to [this document](https://github.com/w3c/webauthn/wiki/Explainer:-broadening-the-user-base-of-WebAuthn) from the explainer in order to help put this one in context?
```

## Breakout 3B

Present: Lea, Sangwhan, Yves


## Breakout 4B

Present: Ken, Sangwhan

This is a very nice explainer and it is quite clear that you have put a lot of effort into this and it really shows! @cynthia and I discussed in our breakout that as this has more raw access to the GPU, what is the mitigation in place to make sure this doesn't negatively affect other GPU intensive apps, like the browser itself or the host OS?

If you have a misbehaving web app, how is this handled? For CPU in Chrome today there is infinite loop detection and the tab can be closed, but GPU can affect the whole system and not just a single tab.

## Breakout 5b

Present:  Tess, Hadley, Amy, Dan

### [EPUB 3.3](https://github.com/w3ctag/design-reviews/issues/684)

Amy: books spying on us? no thanks.

Tess: I have a meta question - first time epub has come to the tag for review - so this is an opportunity. All versions of epub since 3.0 have been tighlty scoped... not changing a lot of things.  It's an ecosystem where you tend ot have low power devices - you want to be able to buy a book in the future and being able to read it - so backwards compatible. People **buy** digital books - so unlike browsers there's a responsibility - to be able to continue to read the book into the future.  Since 3.0 the compat constraints have been really tight.  If we did a full review from the ground up we might end up wasting their time... choices they've made that they are stuck with for compat reasons.  Our first opportunity to be useful to them - so we should focus on things they can actually change.

Dan: we should focus on feedback where they can make changes...

Tess: where things have an impact...

Amy: most of the things that struck me were privacy & security related - a lot of their answers to the s&p questionnaire are "the spec says nothing about this" - but maybe in some cases the spec should say something about it.  E.g. the question abut PII... could they write some guidance about how reading systems should be doing xyz... Seems like the direction of travel is to bring it closer to the web platform... gradually... could subvery user expectation... because ebooks are not websites... reading systems depending on the implementation could track users' IP address, location, etc... but they don't say anything about permission prompts or warnings...

Tess: permission prompt interesting to me –– when you turn a page in a book you're not expecting a modal dialog to interrupt you.

Amy: The e-reader should not be doing stuff that would warrent interrupting the user with a permission prompt.

Tess: when you load the web site or when the user is interacting with the web site - kind of the same - but for books you download the book and the reading system has an opportunity to inspect the book and figure out what permissions prompts it's going to need. One way would be to front load some of that...   For example in an educational context - a digital text book that has excercises - you can fill them out and hit submit - submits to a server that checks your work. You would want a permission to access the network... vs when they're in the middle of the assignment... The baseline should be to not do stuff like that. But they should see the opportunity to be better than browsers... For browsers we have webapp manifest.. 

Amy: for localisation .. could be useful but also surveilance... 

Tess: as an example - i hate it when i go to google in japan and it's in japanese instead of following my lang preferences.

Amy: a use case for an external system knowing where you are in a book for syncing across devices - but that comes with an external system knowing where you are in a book.  

Tess: like scroll linking browsers... you can imagine a browser syncing that...   User agents are reading system but there is an issue of trust... 

Amy: the key for me is that it feels like a different set of expectations...  a device that just reads books... 

Tess: yes - low power devices ... 

Dan: you can do something like that on samsung internet

Tess: reading systems are user agents. UA features to help people seem cool but ultimately the question of trust

Dan: feedback about questionnaire.. big chunk of work but we can do that to start.. We should take as guidence what Tess said that we should be giving useful feedback, not a full top to bottom review of the technology.

Tess: if 98% of oru review is things they can't revisit we wouldn't be providing value. Everything Amy already said can go into the issue.. a bunch of stuff unspecified in p&s

Tess: on their response to s&p questionnaire regarding the download of files -- https://github.com/w3c/epub-specs/blob/main/epub33/explainers/EPUB-33-security-privacy.md#17-what-should-this-questionnaire-have-asked - feels like if all user agents are doing something that spec says not to do then ... maybe they should say something else instead...

### [Dystopia Avoidance](https://github.com/rhiaro/societal-impact-questionnaire)

Hadley: implied in power dynamics but nice to nbring out is how can this be used in a completely different use case. Eg. we talk about things that are useful for login, but we in the TAG brainstorm other use cases like how can it be abused in the context of advertising, that might not be what you are trying to accomplish with this feature, but nothing to stop people with a different motivation from hijacking it.

Dan: unintended consequences

Hadley: not everyone is going to use it with the same motivations. Not everyone is trying to solve that problem that you spent so long focussed on. you've created an amazing thing that could be used in a comppletely different way for terrible things, but we want to draw out and have a conversatin about.

Amy: can expand misuse question

Tess: misuse question should come after use question. While they're thinking about how people can use this, they should think about the other ways people can use this.

Dan: agree

Amy: +1

Hadley: what I'm trying to articulate is if we were designing cookies right now, which were not originally designed with the advertising use case, how do we get that person thinking about things like advertising that could completely hijack thi sfeature.

Dan:
```
An idea to add:
Thinking about the bad actors who mislead people, try to trick people, try to inject malware, steal information, track people's activities without their knowledge or consent, leak information across origin bounderies, game people's consent, surveil people etc... how could your new proposed technology could be used to further these harmful aims?  
``` 

Tess: one thing that comes to mind is coordination. cookies were designed to be used in isolation, for a login state, etc.And in fat if that is how cookies continue to be used, even for advertising isolated to that site, then maybe things wouldn't be so bad. But there's two kinds of coordination that happen. One is third party resources getting their cookies on different sites. The other is on the backend. Cookies checked behind the scenes. It's a grey area between use and misuse. Not that cookies are being misused, that the use is not what the designer intended. 

Dan: not overtly bad. Not like you're taking it and using it to... hack someone. Or steal directly from them. But itis still an unintended use that may be contrary to what you're goals are

Amy: could be a good use case too. Could indicate there are other groups to reach out to about the feature.

Tess: a positive version of enabling use cases you hadn't thought of. You were designing this feature for academic use, or to help engineers get their job done, but it turns out what you've done is enabled a new kind of artistic expression

Amy: like the web platform itself..

Tess: generativity. In the context of the case like domestic abuse and stalking. Very real concerns. Features which have a clear use in helping people who are forgetful keep track of their stuff... that's a good feature... better be thinking about what people consider to be their stuff. 

Tess: one of the questions with no content about centralisation... should figure out something to say. This is a tricky one to express in a morally neutral way. We all assume centralisation si bad..

Amy: EWP says we prefer decentralised architectures

Dan: debate around whether decentralising finance is a good goal, regulation can protect people and you can't implement as easily in a decentralised system. If we focus too much on the decentralised thing I'm worried... another meta concern is that I want to make it difficult to weaponise documents like this (and EWP) without .. I want people to take.. don't want to depower thse documents but don't want poeple to use them as weapons in flame wars. Maybe a code of conduct thing.

Tess: on centralisation.. finance example... one mans freedom fighter is another mans terrorist etc... there are better governments and worst governments in the world. A great thing about the web is that it can help people route around the bad ones. But one of the risks is exactly, peoplle will try to use that as an opportunity to route around the good ones too. Of course overly simplistic... but the surveillence thing

Dan: there are people out there who want to steal stuff at scale from other people. Comment above.. an appropriate place to talk about bad actors. There are people that are building.. It does feel like that is another aspect. It is a dystopia if we're constantly living in fear of the web, then people are not going to use the web for its intended purupose

Tess: absoultely. We make a big deal, eg in design principles and ewp, that the web is a unique platform that has certain advantages over all of the other platforms and the baseline idea of safety is higher generally than other platforms. 

Dan: i do feel that surveillence is something that should hav ea separate item in this list. Judgy to say people who want to steal info are bad, but..

Hadley: not that they're bad people.. they're doing something that doesn't fit.. ways to talk about these things without getting judgy. Same is true of government surveillence or governments causing trouble. There are ways to pick apart the fundamentally the ethical problems

Amy: on not weoponizing - doing it as questions makes it less like a document that can be weoponized ... to help people critically think about their work ...  If it's questions people are answering, want to make sure they are pointed questions people can't weasle out of answering ... also need to make sure they aren't leading

Tess: P&C questionnaire says "we're trying to prompt your brain" .. it's not just a box checking excercise... so you say "oh i didn't think of this" or "i didn't think about it that way" ... easy in a narrowly scoped working group - to only talk to people who are as familiar as your thing as you are... and the group doesn't think outside the box.  "What can we do to protect users against this kind of threat..."

Amy: does tag want to adopt this? move repo to tag space?

Dan: with ewp.. channeling people who said this isn't architecture and was out of our remit. To make the point you can't do architecture without fundamental principles. I have defended that work as architecture. S&P is defensible in that way because it is intended to be read by people that are creating new specs in the same way Tess just said, to promote thoughts and thinking about things.. everything in this document should be channelling that from the s&p... but anything else we can do to emphasise the architectural relevance of this?

Tess: looking at this.. the longievity section.. we could make architectural points about. When you add features to the web once they're above some useage we can remove them for compatibility reasons without a herculean effort. The kind of coordination across the industry for a decade for Flash.. adding features is relatively easy, removing features is incredibly hard.  Are you trying to enable something that is probably an emphemeral aspect of our place and time or are you adding something that you expect to endure. Which isn't saying you should never add things that have a narrow shelf life but you should be thinking about what is the long term version of this. Eg. When Tim first made the web and other people got involved and suddenly javascript happened we ended up with keyword events like key presses. We didn't end up with ps2 events and sun keyboard bus events... that's great because now we live in a world of usb and bluetooth keyboards. If websites had been built in the 90s expecting keyboard architecture specific events we would have missed the ability to make the platform make ssense in the longer term. We kind of do that in cases like mouseevents... nw we have touch screen... but longievity is ag reat example of an architectural question. We can couch it in terms of what makes the web unique which touches into ethical components. The web has a longer lifetime than other things that you may have worked on in your engineering career. Different from thinking about an API that you can deprecate whenever you want. There is no whenever you want. 

Hadley: agree. 

Tess: we can frame questions to establish architectural concern to help people understand it's not just a random set of questions.. understand the pushback we're going to get.

Dan: having a questionnaire style will help to blunt that criticism

Tess: yes it's a tool to help your improve your own work

Dan: be careful to position as a companion piece to ewp, design p, s&p.. part of a suite of things to help people think about problems.

Hadley: it's architectural becuase we as the TAG a thing we think about is how work in one WG might interact with another. We are often the ones saying you realise you're doing something that will impact another WG or that two things are the same, or two things are close... the use case stuff from earlier was very much that big picture architectural view across different pieces of work. It's prompting the spec author to think more broadly about the architecture not just their narrow problem.

Dan: do we have some actions? Take it to TAG repo space. My suggestion is you mke edits based on this conversation. Then we start the process of raising issues and PRs and stuff. 

Amy: yes

Tess: "societal"... what's the scale of the problem? Are threats to individuals in scope? Having thought on that.. I thought this was the right document for those things but we need to be clear about what we're trying to do. It is the right document. That scope is an artificial ... pretending like threats to individuals are not societal is not good.. 

Dan: any threats we talk about like surveilling it becomes a societal level threat when it's amplified through the web. If the web is providing a tool to allow anyone to surveil anyone that's a societal level threat.

Tess: or just making it easier to do an individual thing... easier to stalk at the individual level... we're making a society where stalking is more prevelant. Absoultely that stuff should be in here. Worth expanding... I don't want a list of 'minority groups'..

Dan: we can use blanket terms like underrepresented, marginalised.. that's transferable across cultures

Tess: useful to have a list of common threats or concerns among underrepresented folks..

Dan: also goes through my head hearing that is that we need some intro text that says that.. threats against individuals become societal level threats. that thinking has informed this document. You may read one of these things and think it's an individual threat, but it is a societal threat when it's amplified across the web

Tess: we could quote the first sentence of EWP... the web should be a platform... net positive social benefit.

Hadley: remembering conversationsa bout cookies... and early conversations with Tim about the early days of email and spam.. and how anticipatable it was

Tess: fantastic example

Hadley: they have to do with making money... financial interests... feels like an awful lot of not thinking about that in th eearly days and now there's a huge amount of decisions driven by immediate profits. We can talk about that in a way that.. going back ot use cases.. helps people thinka bout what else someone might want to do with what they're designing without saying making money is bad. Prompt other motivations for using web platform tech.

Amy: I stuggled to come up with a name. Thoughts?

Tess: email spam example is great, can we find quotes about their lifetime of regret? Societal impact is a professional and neutral sounding name. 

Hadley: as long as we expressly link to the Ethical Web Princples, stay grounded in it.

## Session 12B

### [Overall review of features which enable/disable subframe or subresource capabilities](https://github.com/w3ctag/design-reviews/issues/525)

### [Deprecating `document.domain` setter.	](https://github.com/w3ctag/design-reviews/issues/564)

Dan: proposed text ...
```
Hi folks - we are looking at this at our virtual face to face and it looks like this has progressed signfigtantly with a new (tri-state) [proposal](https://github.com/mikewest/deprecating-document-domain/). That looks reasonmable though we have concerns around compat.  Is this work still in flux or is it appropriate for us to re-review at this time based on this propsoal?
```

### [User Preference Media Features Client Hints Headers](https://github.com/w3ctag/design-reviews/issues/632)

Dan: I think they were going to come back to us with some data...

Rossen: i don't question the performance improvement... we're not arguing about that... they were however using this as the primary motivation .. if they bring it data great - it will only validate that statement. And then there's the rest of the web and patterns that have existed for 20 some years... 

Dan: In defense of the requtors - they have talked about other stakeholder feedback...  Facebook, tiktok, etc...

Rossen: Of course, all of these comapnies will all say yes to any small feature that will save them bandwidth. Again, this is a point I agree with.

Dan: maybe we shoiuld provide them advice about guard rails to put around this rather than telling them to go away and do it outside of standards...

Rossen: not targeting the use case of saving some momey on a big property - it's about the model of media feature state tracking... and handling.  Which by definition is a device capability that is changed by the enviroment or user action on that device. Devices go back and forth (e.g. dark mode)... So that state is handled from the user pov - ... 

Peter: on initial load the server should inline the appropriate asset... if you do it all correctly - the logic stays on the client but the server still has responsibility to ship both assets.  Our concern is that developers will do this wrong ... and not ship both assets... If you don't get it just right you've broken it...

Rossen: the set of features here... apart from Light Mode / Dark mode is large... 

Dan: http3/2 push... Yoav said ... yes some browsers never shiped push... the network stack doesn't know about it... he thinks the practice of doing server push on both... not good. I'd like to see real world data...  I think it fixes the round trip issue but not the delay issue...  

Rossen: the fact that you're not .. that this is the case.. establishing tls handshake etc...not necessarilly a good thing.  If i'm penetrating a network and want to go look for specific veunerable devices based on their state... this gives me more feedback that's much harder to detect and protect against.



Peter: kind of true for all client hints...  TLS handshake you can avoic by using H2.  I accept the fact that they will do it anyway... Are we better off not having a w3c standard? I don't know. If it's a standard it should have big red letters over it saying "don't use this unless you're google/facebook"

Dan: could we ask them to put mitigations in place...

Peter: [ekeptical that such mitigations could work]

Rossen: besides light mode / dark mode - you have contrast, color management, accessibility, viewport etc. etc. - a permuation of many media features. Assume we have a device in "i'm in dark mode; i'm also in high contrast mode".  Now it's less dark so not in high contrast any more. The UA will send the UACH that it's not in high contrast. Back to their motivation - in order to preserve bandwidth CSS is inlined as much as possible to the user preferences that they detec - btw, today this is done using a media query on the client. They have to cascade and inline the resulted rules on the server side - the combination between dark mode and low contrast in the current example.  So now all the rules that have to cascade and inline are calculated on the server side.  To Peter's point - add 2 or 3 more features now you're hangling cascade on the server side. This capability can be used this way, this is my assertion.

Dan: (even if not intended)

Peter: one thing in defence - you can put certain style sheets at the head of the queue so your initial paint can be faster.  If you use server push just right you can make sure that those stylesheets are available pretty much at the same time. I would like to see data that this is better than server push.  I think there are situations when server push might be better.  Not sure this is the best solution to the problem.

Rossen: there are many of these... I don't agree with allowing all the media features... viewport segments, color management, pointer... etc... 

Peter: we did ask them for data for this vs server push.  If we close it off we can say so - but please continue to explore other options to get the same benefits such as server push.  

Dan: We also would like to see some thinking about mitigations against misuse?

Rossen: from a pure technical PoV... They started with a great premise... can we deprecate user agent strings... let's start working on client hints... because UA strings allow you to know aboout the hardware capabilities... Ok. now they are using this for saving bytes by looking at user state based on these capabilities.  From the runtime what else can we start extracting. Everything else that media feature captutes are triggered by env variables or user intent or action... This has nothing to do with the fact that this device e.g. is running windows vs iOS for example. So now we want to know what the user is currently doing so you can give them something quicker... 

Peter: there's a pretty strong line here you can draw - **client hints should be about the capabilities of the client, not the state of the client**. A useful client could be "does this device support auto detection of light or dark mode" - but not "I'm in dark mode now." 

## Session 16B

Present: Dan, Hadley, Ken, Yves, Amy

### [Distributed Tracing WG: Baggage specification](https://github.com/w3ctag/design-reviews/issues/650)

Hadley: no response to comments, but a new issue that references ours, responding to Yves question

Dan: that's merged. Can ask Yves if he's happy

Ken: it's meta data.. you can carry around a lot because there's no limits, you're in control. You need to understand telemetry, distributed compute.. not something you're going to get from a random website

Dan: I guess that's the point.. could a random website misuse it

Ken: they need to collaborate with someone otherwise it's their own data. The thing is people want.. distributed tracing you want not just from the frontend but from the backend and carry it around so you know how everything works together, front and back end. Normally you do that for yourself. I don't think you can do the tracing across random websites and get it to you, that would be a major issue. I think this is okay.

Dan: they say under privacy of the baggage header.. can contain user identifiable data. Must ensure it does not leak beyond defined trust boundaries... and channel is secured. What does that mean in real terms? 

Ken: is there any obvious way it can leak?

Dan: it doesn't define the trust boundaries. What are the trust boundaries? It doesn't say therefore it must be in secure contexts, just says it is secure. The requirement here is good but it's not as strong as it could be. I would say something like...

```
In the [Privacy & Security Section](https://w3c.github.io/baggage/#privacy-of-the-baggage-header) it states "As such, the baggage header can contain user-identifiable data. Systems MUST ensure that the baggage header does not leak beyond defined trust boundaries and they MUST ensure that the channel that is used to transport potentially user-identifiable data is secured." But the term "trust boundaries" is not itself defined in the document. Also maybe you should refernece [secure contexts](https://www.w3.org/TR/secure-contexts/) directly instead of just saying "secured" to be clear about what you mean by secured here?

We're also still waiting for a response on the issues raised by Hadley about incognito mode and naming.
```

Yves: they updated the token to the same RFC, that looks good

Dan: they need to define their privacy and security considerations better

Yves: the question Hadley raised about incognito mode still stands. Waiting on those to be answered.

Hadley: and 'baggage' being a US idiom, haven't heard back on that either

## Session 17b

Present: Lea, Peter

### [Review of new window.open() behavior](https://github.com/w3ctag/design-reviews/issues/691)

#### Draft comment

@plinss and I took a look at this during our virtual f2f today.

We think that a boolean argument (`popup=0` or `popup=1`) is not extensible, if in the future authors want to select 
between more than these two kinds of window UI, whereas a keyword-based argument (e.g. `type=popup`)
would not have this problem.

As a side point, this sentence in the explainer was unclear:

> The window.open() API is currently confusing to use, in terms of trying to get it to open a popup vs. a tab/window. 

until I read [this section on MDN](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#popup_condition):

> Most modern browsers (listed below) don't allow web content to control the visibility of UI parts separately.
> [snip]
> UI-related items of `windowFeatures` are used as a condition to whether opening a popup or a new tab, or a new window, and UI parts visibility of each of them is fixed.

Furthermore, we understand that this method has a long history, but if it were designed today we would strongly recommend using a dictionary instead of a serialized string that has to be parsed and re-serialized, see: https://github.com/w3ctag/design-principles/issues/213. It may be worth considering allowing users to pass a dictionary in place of this string for future enchancements, similarly to what was done for `addEventListener()`.

We generally encourage people to seek feedback before features have already shipped in browsers.
Given that this has already shipped in both Blink and Gecko, it seems too late to have any of our feedback taken on board. Therefore we're closing this issue, feel free to ping us if there's anything further to discuss.

### DOM spec

Notes about response:
- Ask about precustomized, what does this state mean, how do you get there. Seems to be completely undefined

#### Draft comment

Hi @siusin,

@plinss and looked at this today during our virtual f2f.

We had some questions:

- We see references to a new "precustomized" state for custom elements, but we did not find a definition of what this state means, and how do you get there. It seems to be completely undefined.
- There is an "is available to element internals" flag, but no definition of what it means
- If `shadowRoot` is available to internals, is there a difference between `this.shadowRoot` and `this.internals.shadowRoot` or do they point to the same thing?
- We see a new `delegatesFocus` property has been added on `ShadowRoot`, but there is no description of what it's supposed to do. By looking around we found [this](https://html.spec.whatwg.org/multipage/interaction.html#data-model), but it's still unclear what use cases it solves and what exactly it does.

The rest of the changes seem fine.

## Rollup for Breakouts 3 and 4

Present: Lea, Yves, Ken, Amy, Dan

### 3a

Dan: Gamepad, js self profiling API and WebXR raw camera...  Raw camera we're still waiting for feedback; gamepad ken left some additional feedback; js self profiling - we also left questions.

### 3b

Ken: Sangwhan drafted bundling finding, needs review

### 4a

Amy: we talked about speculation rules and same origin prerendering triggers. we're waiting for feedback on both of those...

### 4b

Ken: WebGPU -- biggest explainer. Well written. Sangwhan going to look through some details and file comments.  Question - if you have js in one of your documents and youre using raw gpu access you can take down the browser and OS.  We pointed that out... want to hear what they have to say about that.  left that feedback...

### 5a

Peter: Pen events - still pending feedback - we talked about viewport segments - still a lot of confusiomn about what they mean by screen...  Ken sent some feedback.  A response...

### 5b

Tess: dystopia avoidance and EPUB 3.3.. most time on societal impact questionnaire. Amy provided a first draft. Good conversation. Next steps are Amy will edit then move the repo to the TAG org and then we can open issues. 

On EPUB.. conversation about how to go about doing this review... first time epub spec has come to us. Given unique constraints they operate under.. are we reviewing whole thing or a delta or something in between and what does that look like? Agreed to focus feedback on things we think are actionable. A lot of things they can't change for compat reasons. Looked at answers to S&P and had followup. That review needs more time and effort. Good direction.

### 6a

Tess: compute pressure...

Ken: proposed close, reopen when it's the right time

Tess: html popup... they filed the review request and then a design review happened that wasn't from us. Dominic chimed in with feedback and some in their own issues, tons of good conversation. Current state of where they want it is different from text they asked us to review. Left comment. 

Webapp launch handler... tension between what native apps can do that are bad..

Dan: you've already got a tab open.. a pinned tab of a calendar... you click on a link and it opens another tab with the same content.. is that what you want or not?

Tess: user expectations, and existing app platform behaviour and web platform behavour and none quite line up. Music app example.. don't want both songs to play at the same time. Lea brought up an example of native maps app and tapping on a maps link and it switches to the maps app and blows away whatever you had open. Opportunity for app developers to do clever things but when we look at existing behaviour we see a lot of bad behaviour. How do we help the web be better than that? A bunch of us added comments.

### 9a

Ethics...  

Amy: Drafted a comment to issue 66...   We also merged some PRs...  New part of the intro to talk about conflicts between principles.  Also an editorial pass and fixed some typos....

### 9b

Dan: Sangwhan worked on the *Finding: Bundling and Caching Sustainability* finding.  will be brought over to github and we can work on it after the f2f and issue it at a subsequent call...

Sangwhan: I'd love feedback.

### 10a

Dan: Miniapp lifecycle - Sangwhan will leave a comment specifically about the privacy & security issue... they have a part of the doc that says "s&p" but it doesn't talk about that topic.  We also have a general concern that the miniapp people are reinventing wheels... building stuff that doesnt adhere to web architecture, and not reusing existing things. Need to get them aligned with the webapp people. New things coming to pwa like launch control, uri schemes, and a lot are the same in mini apps.

### 10b

Ken: design principles for time -- currently a recommentation that isnt't good advice. I will try to write something. We looked at relationship between worker and window... agreed if you expose on dedicated worker then you should expose it on window... other way around we're not certain about... 

### 11a

Hadley: first party sets....   

Dan: we left comments...

### 11b

Peter: focused on design principles...

Dan: Sangwhan and Lea?

### 12a

Amy: Secure payment confirmation.. Me, Hadley and Ken...  We looked at some of their issues with privacy and with the webauthn working group.  Hadley left a comment. Ian replied.

...We also had a tangent for process fo really big specs... too late to give substantive feedback.  We could flag it immediately and schedule a meeting.  Or find a place in the workimg group process to flag it earlier in the process.

...specs do take a long time and soemtimes there can be turnover in TAG membership...  

### 12b

Dan: user preferences media features client hint headers. Rossen and Peter laid out good arguements about why it's a bad idea. It's still something that the requesters seem to think is a good idea for an optimisation of bytes on the wire or speed, but it has unintended consquences, especialy with moving some computation of style to the server. Rossen is going to write a comment. Proposal is ti close as unsatisfied but to open the door to if they com back with a different design to reopen or ping us, we can reevaluate. Peter mentioned an important potential principle which is client hints should be about capabilities of the client not the current state of the client

Rossen: I'll elaborate on closing comment... the actionable hint is that they can expose whether or not a device has the capability of detecting light or whatever which will already have quite a bit of effect. If this device doesn't have the capability of light sensing it's not going to go back and forth between dark and light mode. It's an assumption, I can turn dark mode on inside user preferences, but as a crude way this will get them closer to their goal

Peter: or if the UA even has the capability of having that preference, so why send both stylesheets

Dan: okay with closing

### 14a

??

### 15a

Dan: we talked about landing some PRs (351, 290).. and closed issue 572 and 685.

[reviewing PRs] ... need Sangwhan

### 15b

### 16a

### 16b

### 17a

Dan: Amy and I talked about conditional mediation of webauthn and left comments. In general about making webauthn more usable and getting more serices to deploy it because the ui will be more intuitive

### 17b

Lea: in 691 - window open... explainer was a link to chrome status... we closed it.   We had the HTML and DOM reviews... We basically completed the DOM review... They fall into 3 buckets - editorial; something straightforward; some new feature not documented (we fed back and asked and asked).


### 18b

