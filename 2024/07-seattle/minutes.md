# TAG F2F - Day 1

Present: Amy, Jeffrey, Tristan, Hadley, Peter, Tess, Dan, Matthew, Yves, Martin, Max
Guests: Johann, Kaustubha, Shivani, Chris F. (from google Privacy Sandbox team)

## Welcome Session

## Discussion on Privacy Sandbox

## Privacy Sandbox 

*Johann presents slides, can be found here: https://drive.google.com/file/d/1iSskMcnyF3I9czSi-IJPSqjBBzjzNUOC/view*

Johann: Firefox and safari are blocking 3p cookies in some way - chrome is at 1% - we are hoping to block in 2025 pending regulatory. Right now there is breakage due to 3p cookies. Many browsers ship mitigations - cookie access heuristics. Overrides, per-site settings, etc... We don't want that. We want to give the web a well-lit path to legacy deployments of 3p cookies. Over time we phase out the mitigations. At the beginning, a temporary allow list then a deprecation trial... slowly we phase those out in favour of other solutions - eventually passing the border to long term web APIs... Solutions need to be good enough and flexible enough to get developer adoption as soon as possible.  So how do we go about identifying web breakage from 3P cookie deprecation (3PDC). https://app.slack.com/client/T0AQVAJ2H/C07CGQ636LT?cdn_fallback=1 We look at issues filed and identifies API gaps. That drives prioritization. We also want to build good UX, get feedback from partners, doing right by security & privacy. We would like input from TAG ... Questions are: How can we support non-federated flows such as enterprise; what is the ideal user prompting experience; how can we increase adoption of APIs with improved prompts....

Johann: some of the work we've been doing: federated and non-federated identities; promot-less privacy preserving APIs; interop and standardization of privacy / security boundaries.

Dan: explain promptless?

Johann: We're convinced that we should avoid prompts when we can. How can we design APIs that are privacy-preserving out of the box - that shields info by default. CHIPS is a good example - if data is partitioned for a third party... Fenced frames is another example - give access to top level data... 

Shivani: for fenced frames the use case that motivated was personalized payment frames...  an example where having a prompt adds a lot of friction. 

Martin: We don't have to give web sites ways to manipulate their users... I think it's not good to be able to manipulate people... 

Johann: Would be interested in hearing more about this. What does manipulation mean to you?

Martin: I'd like to take that off line... fundamentally a lot of these capabilities rely on, getting people more accostomed to the idea of a privacy invasion....e.g. You'd go to a random web site and if you didn't have 3rd party cookies you would see a frame showing you a friendly log in page wit your name... give the impression that you've been there before even if you haven't - that would be 

Lea: do we have any data on that? If users do understand it then it seems like a win-win but we don't have data to assert one way or another.

Shivani: fenced frames wouldn't work unless that user had been to that site - engagement would have happened...

Martin: but in a different context

Shivani: in a different tab (e.g.)... The user should have been to that site earlier.

Johann: another example - services that provide access to scientific articles... infer whether the user is able to read the article free of charge... so I can go to the site sponsored by my institution.... You can't prompt everyone. Classic dilemma. A developer might want to use a capability - but not willing to ask everyone to prompt. I get the concern about creeping into the 

Jeffrey: I would add 2 things - category number 2 (promptless APIs) is about APIs that don't create any privacy issues without a prompt. CHIPS definitely. Fenced frames... If it's tricking people in practice, that would be a privacy problem... 

Kaustubha: if the user's has a trusted payment provider should we give them a way to interact with the web - in the payments case, if we don't have a wen platform API... then the user is restricted to platform APIs... (e.g. applePay)/.

Jeffrey: privacy risks beyond cross-site tracking.

Martin: a trusted payment provider... it would be better if we could be assured that this a trusted partner... but if any website can do this on any other website, as per the api presented here, the word 'trusted' doesn't enter into it

Jeffrey: if it were a more targeted API... As a very general API it's not clear that it accomplishes a particular goal.

Johann: I would be interested in seeing such an attack constructed - it's very abstract. 

Martin: protected audience - you have a bunch of info that is priveliged... which is used to display info on the screen - when you click it leads to escape the confinement of the fenced frame?

Shivani: in the case of fenced frame *presents from slide* - state 2, it has to invoke API... at that point it's able to access / display the cross-site data... No way of exfiltrating the data as network access is revoked... Only thing that goes back to the page is that a click happened. Then the merchant page would have to invoke payment handler ... not with access to this information.

Martin: that's useful information.

Dan: you've talked about the process by which you are determining which apis to prioritize through understanding breakage. Very often I'm finding when I see ... I wonder whether claims of breakage are as a bad as they are being presented. I can see using a browser with 3p cookies turned off or a raft of privacy mitigations installed that the thing that is claimed to be broken is working or can work. Do you also consider giving the developers a workaround? Informing developers on the use of existing technologies? Does a new technology need to be added here?

Johann: a lot of the times the existing workarounds are also privacy invasive. We don't want to just kick the can. We'll have to fix them up at some point. Froma  web platform perspective we'd like to get people through this pain of using our sanctioned standardised apis eventually. You're right, if you use the web in a certain way you don't perceive that much breakage. A lot of the breakage we see reported, particularly severe ones where sites don't work any more, are Enterprise. Their customers only use chrome so 3p cookie blocking hasn't affected them yet. They're interested in solutions to those problems and looking to us to solve them. SAS provider using 3p cookies for everything... SSO, their own IDPs, dashboards ... We need to work thorugh this with these partners, and using existing technologies would be a restructure for them as well so we might as well push them towards the path... and often would be more work. Cookies provide security guarantees that they wouldn't have if they were throwing identifiers around in javascript. That's why storage access. They're putting SA prompts in front of users but we're not fond of that. Can we use FedCM in these cases? Partitioned pop-in? A promptless api with certain privacy guarantees. I think you're not seeing the breakage because you're not using these corners of the web, but they definitely exist.

Dan: thanks

Shivani: that a click has happened as a privacy channel... wer'e in the proecess of maybe adding more rate limits. We are thinking about attacks that could happen. If there were multiple same origin fenced frames, and some are visible.. rate limiting same origin fenced frames that can use this functionality at the same time.

Martin: rate limiting may be necessary but probably won't totally solve. There's a demo page on protected audience that uses visited decorations on links to do exfiltrating .. applies to protected audience, and probably applies here as well.

Shivani: about link decoration? wouldn't be thes ame issue here, there's no navigation from the fence frame allowed

Johann: visited styling attack.. side channels are definitely a challenge for everyone. We also have teams working to mitigate those. Maybe a separate conversation.

Dan: In terms of feedback from the TAG. We're driven by design principles, and we have Leave the Web Better than you Found it. That's central to a lot of our feedback. One fo the overarching concerns that we always have is if we're deprecating something let's not just build another thing that preserves the probelmatic nature of the thing we're deprecating. And we have this new great set of [privacy principles](https://www.w3.org/TR/privacy-principles/) that we're pushing toward w3c statement, and it's worth taking a look. As we move forward we're going to be looking to that as a way to drive our feedback on future reviews.

Johann: if the feedback on a features i that it seems to violate this principle, that's helpful feedback. Maybe we could make the [S&P questionnaire](https://www.w3.org/TR/security-privacy-questionnaire/) a bit lighter? And update the privacy part to be more specific.

Martin: the ideal end user prompting experience is that people are only asked questions they're prepared to answer, and the consequences ... and .. recourse. IT's more challenging. We get away with it in some cases more than others, because there is recourse when someone makes mistakes. That's not so true when it comes down to I clicked on a thing and now I have established a cross site linkage that wasn't there previously and I didn't want to happen. That's now done. As much as reputable websites will respect a request to delete the information, even the good ones aren't that good. I know this because I've been working with our data people and it's not as good as I thought it was. Even people working very hard to do the right thing ultimately end up doing the wrong thing.

Johann: established relationship with the user... do we really know the site is providing the service they're asking for.. the more information we can give them, there's a strong instinct that this creats much better prompts. I'm thinking of FedCM.

Martin: FedCM is good in that regard. It gives users the opportunity to say you're logging in with this identity from thsi website over here.. but there's not takebacks. 

Johann: we can improve upon FedCM in future to show additional information. Interesting generally. Having this established relationship with the providers, the developers of these IDPs have to do a certain amount of work to provide the right information for the user. It also means, it's a tradeoff, they have to meet all these requirements. That often prevents people from prototyping or adopting legacy usecases. We have to grapple.. how do we keep this lightweight, adoptable, and at the same time put these requirements for talking to users the right way. 

Peter: I'm looking at partitioned pop ins explainer. Seems to be designed to satisfiy a very particular SSO use case, which I accept would break without 3p cookies. There are other ways to do SSO which maybe are not as user friendly? They would work just fine without 3p cookies and without adding .. Curious.. I accept you get customers ssaying they have this workflow and their system will break. How many times do you just say "tough"? It's goign to break, there are other ways of doing it, use one of those, rather than a new api surface to keep your way of doing things working. or maybe that way was never supposed to work. How often does that happen? It seems to us that the default is to find a way to keep things working, rather than saying no go do something else.

Kausthbha: any login use case, the whole thing is identity. The IDP is enabling login on another site, the RP. It's like cross site tracking. Today you're right a lot of SSO happens via a top level redirect. 3p cookie deprecation doesn't necessarily break the act of authenticating. Generally within the privacy community we are talking about navigational tracking. As browser intervene on 3p cookies, tracking migrates to other mechanisms like bounce tracking. We could tell them to use redirects or popups but it's kicking the can down the road. Without a well lit path that legitimate use cases can migrate to it's goign to be another vector we have to tackle. How often do we say we're not doing anything? None of these use cases really have an api surface. They're a year or two from shipping. This is constructing a well lit path. As more of the ecosystem migrates to these well lit paths we can have more leeway of turning down those tracking vectors. For login, even though the act of authentication itself only depends on popups or redirects, there's session management - getting logged out of the other top level site, today that session is kept alive, so that pattern goes away. Some IDPs are moving to capability URLs so there's a little more user friction or they're less secure. If you're just using tokens or capability urls in an enterprise environment, say an embedded video, the user is logged in, store an access token.. someone could take that outside of the corporate network or access control and put it on another device. We have seen idps migrate to these things but they're not great in terms of security. There's a patchwork of different solutiosn right now but we don't see that as being a sustainable path.

Peter: sometimes I think it might be useful to get that extra context in the explainers

Kausthbha: white lable identity... bank, utilities, identity as a surface. The cookie really needs to be scoped to that site. It's nto like google sign in where the user has a relaitonship with the idp. The use rin this case has no idea who the identity provider is, the relationship is with the top level site, but they're contracting out the login services. Okta is an example. The way they manage this today is create per customer subdomains. The user has no idea who Okta is. Partiioning that browsers are moving towards. When we built the partition cookies proposal and put it out there ... ... from within the iframe that opens a popup, why doesn't the popup have access to the same cookies in the iframe?  ...

Lea: a lot is overfit to authentication. There's a lot of work in letting the browser manage identity. Seems to be designed around a more generic use case, but explainer centers around specific one. If there are more use cases it would be great to integrate them into the explainer so we can see how it works

Johann: I like it because it's the way popups should work. The problem on the web platform around popup opener relationships tracking. a potential vector for cross site sharing that's not at all transparent to the user. You can open a new tab and it could have an opener relationship and you don't know. We weant to eventually get rid of that. If you open a proper new tab or you navigate somewhere it should all be the same to the user and should have no connection, invisible or not, tot hte previous site they were visiting. But this functionality is sometimes needed. Sometimes they need to communicate with their opener site. Partitioned popins to me is a solution for that. If you are as a site are allowed to communicate with yor openeer the user should have a clear indication of this. Whatever they're seeing is embedded in the other site. 

Lea: I agree that popups on the Web can use a big redesign. However, there are also several user needs that `window.open()` doesn't cover (most recently document PiP), if this is supposed to be a general purpose alternative to popups, it should also cater to these user needs so we don't have to reinvent popups once more in a few years 

Johann: I think I disagree with the premise that PiP isn't needed because popups exist. Pop ins wouldn't be able to solve picture in picture for a very good reason. Popups shouldn't be used for PiP. Sounds like a perfect example of a purpose driven api. Popups are a proper browsing context. ... 

Lea: I was referring to document picture in picture, not the general video picture in picture that we already have. It allowed websites to spawn popups with arbitrary content like a cooking timer that was always on top and closed when the opener closed, basically a collection of orthogonal features useful for popups in general. 

Johann: Ok, that's useful, I have not seen that proposal

Kaustubha: a lot of identity providers are security conscious. They don't want to be subjected to script injection attacks that their top level users might be vulnerable to. They don't like serving tehir login forms wihin iframes for that reason. Rampant pattern on the web - typically redirects. Why do we need a new UX affordance here? That is where we started, then we talked to privacy and security reviewers in the chrome team, potential for an aggregator attack where the attacker opens every article a user clicks on in a popup so the aggregator can track them across all the articles. We designed it in a way so it couldn't be useful ... 

Peter: to the extent this seems centered around authentication. The lighted path .. is FedCM.. login is mitigated by browser chrome, it's not a popup or an iframe. There's another way of doing it. If we build too many interim steps we're delaying getting to the place we want to get to eventually, and we're adding a whole lot of new functionality we're going to carry around. More of an attack surface. Reluctant to add new features that are interim features that we expect to be phased out when we get to some better way of doing identity down the road. Makes me question some of this stuff. Other uses beyond identity helps give more reason to approve of these things but ..

Dan: Lea mentioned it and Peter did... we're supposed to be looking at the whole web platform and sometimes that means asking the question about doing things in a way that makes sense for all the cases. That also speaks to the issue of developer complexity. We tangle with this so much. The web is a huge bunch of apis that have all been developed by different teams at different times across decades. One of the biggest blockers that developers have is its complexity and heterogeneity. It's also one of it's assets, but we often find ourselves raising the developer complexity issue as well. Just highlighting some of our motivations. We're not just trying to wreck everything. We're tryign to answer the question does this new technology make the web better than it has been. Or are we adding something that is another complexity.

Johann: appreciate the sentiment. We're not only thinking about keeping the simplest thing.

## Breakout 2c

Present: Yves, Peter, Amy

### VC JOSE and COSE

agree to close, after checking if Martin and Tess have anything to flag

### FedCM Multi IDP Support

Peter: concerns about layout shifts... we asked about this being handled by the browser chrome, that is their goal.

Peter: curious how this plays with the register API (#974)... in this api you give a list of IDPs you're willing to work with. Ideally you should be allowing ones you've never heard of. Currently when you do the get you just say any with the url, and you get whatever the browser knows about.

... during this process, there's multiple idps, the ua wants to show some chrome around them.. even though you're only making one get call it may come back in different times.. I don't remember now how is the ua getting information about the idps? It seems like this promise doesn't resolve until the login is complete. What other apis are being used in the meanwhile?

### FedCM API extension: Button Mode and User Other Account API



### FedCM bundle: Continuation API, account labels, custom parameters, scopes


### General FedCM

We'd like to see the big picture and how the pieces fit together. They have replaced at least one explainer with a long issue thread which isn't helpful.

## Breakout 2b

Lea, Martin, and Tess worked on and filed a few PRs on the Design Principles document:

* https://github.com/w3ctag/design-principles/pull/500
* https://github.com/w3ctag/design-principles/pull/501

## Breakout 3a

### [Playout Statistics API for WebAudio](https://github.com/w3ctag/design-reviews/issues/939)

Issues raised:
- Lea: Impossible to tell if this is a good design without use cases. Use cases listed are very low level "we need to get statistic X". But what will you do with it?? E.g. sending the stats to a server for future analysis vs adapting the playback somehow are markedly different use cases.
- Lea: Web Audio is not the only API that playback glitchiness is relevant to. Would e.g. HTMLMediaElement benefit from this too? How would catering to video glitchiness change the shape of the API?
  - Peter: apparently an AudioContext can be created from Video and Audio elements, so if the stats are desired they can be gotten with some degree of plumbing.
  - Lea: Yes but glitchiness is not just about audio. Not ideal if we have a whole different API about video glitchiness.


<blockquote>

**NOTE FROM MATTHEW BEFORE SENDING: did we agree to also ask the wider quesition? If not, the 2nd para can go. Will check up on this after lunch :-).**
  
Hi @Hernqvist, we noticed that the RenderCapacity API isn't going ahead at the moment - do you know about the implementation barriers encountered there, and do you anticipate similar implementation challenges here too?
  
Further, we note that other types of media can be affected by glitchy playback, too (e.g. video, animation) - have you considered whether there are any parallels between this work and those other domains?
  
</blockquote>


## Breakout 4b

Present: Lea, Peter, Yves, Matthew

### [Meta: How do we work with other WGs?](https://github.com/w3ctag/design-principles/issues/387)

Discussion started from https://github.com/w3ctag/design-principles/issues/284 but evolved into a question of what's the point of maintaining CSS design principles if the CSS WG is not involved in authoring them or reading them.

Lea: Similar issues with HTML and JS principles: WHATWG specifies HTML, but is minimally involved in design-principles discussions. JS APIs are specified by multiple groups (TC39, WHATWG, and others) apparently operating under different principles. 
However authors neither care nor understand this difference. 
To them the DOM and e.g. Temporal are both JS APIs, and it's confusing if they are designed with different principles in mind. 

Matthew: Should we reach out to people from different WGs?

Lea: We should first decide what our policy is, how do we want to collaborate with different WGs?

Peter: I’m unconvinced we should have the policy. It makes a difference if multiple groups are working on a technology vs just one.

Lea: But when is it really just one? E.g. CSS things have in the past been specced by the SVG WG, WHAT WG, even the WebVTT group. 

Matthew: We need to make a case with organizations we've not worked with in the past to justify we are a good repository for their principles.

Lea: Agreed. But to play devil's advocate, what happens when we actively *disagree* with the group? E.g. groups often prioritize implementer needs over author or end-user needs.

Matthew: And what about the effort of principles for developers? Or individual companies' principles?

Lea: Indeed, orgs have their own principles. And I wonder if we'd be creating separate documents for web devs. E.g. CSS' extensibility mechanisms are much more limited than HTML's or JS', so authors aren't creating much in terms of CSS APIs. Though that's about to change.

Matthew: Some of our principles relate to both implementers and web devs; others relate to implementers primarily - maybe considering those separattely provides a way to start building consensus on what we agree on.

Lea: Also, I realized, this is not about hiding content. We will need to change certain terms that make no sense to authors, e.g. "IDL attributes", "content attributes".

Lea: Which brings up another point. I've previously tried to promote using JS terms when discussing JS APIs, but there was no consensus. We won't be able to get participation from groups like TC39 if the principles are phrased using WebIDL terminology. 

### [New principle: Incorporate from existing CSS Design Principles](https://github.com/w3ctag/design-principles/issues/490)

Resolved to discuss this in another breakout.

### [New principle: The value of HTML boolean attributes doesn't matter](https://github.com/w3ctag/design-principles/issues/451)

Lea: It's rough to not be able to specify Booleans that default to false. We have to name things in potentially confusing ways. Propose way to fix Booleans across HTML and ARIA (if data shows its webcompat): specify that any value (including empty value) means `true` but no value, or "false" means `false`. This would also fix ARIA.

Matthew: Oooh

Peter: What about the way it's specified in ARIA - has to be a string regardless?

Lea: Maybe we can still change this? It seems to have shipped recently: https://developer.mozilla.org/en-US/docs/Web/API/Element/ariaChecked

Matthew: for historical context, a couple of related ARIA issues are: [Add ARIA property string reflection on Element](https://github.com/w3c/aria/issues/691); and [Boolean attribute oddity with relation to HTML5](https://github.com/w3c/aria/issues/703) (Alice also linked to a good comment on this from the title design principles issue (451)).

Lea: How does an invalid value get handled now?

Matthew: checked in DevTools quickly; unclear at the moment; will need a bit longer to check properly. Even the "true/false" values tend to be enums, with furhter states, hence the confusion.


# TAG F2F - Day 2

Present: Peter, Martin, Lea, Yves, Tess, Jeffrey, Dan

## Discussion on Privacy Sandbox

*We discussed different topics in the privacy sandbox*

*FedCM Discussion*

Federated authentication (FedCM)

Jeffrey: the use cases are in the explainer...

Peter: There are a lot of rube goldberg machines that have been build around web technologies - SSO, etc.. - all sorts of weird tricks - and people have built businesses around each way .. when there's another way to solve the use case.  E.g. Popins to do SSO.  Instead of inventing another way to solve SSO... Seems like if someone complains that their particular approach is breaking then the approach is to fix that problem rather than [redirecting them to another way].

Jeffrey: The FedID folks do have a flow chart where some of the results are "don't do this". ..

Yves: in many cases, solving ... 

Martin: this is one of the discussions early on in FPS discussion.. it was hard to pin down if this was intended as a transionary technology or as the future of the web... I consider the storage access API as an escape valve but not a permenant feature of the web.

Tess: I suspect we will need it indefinitely but I agree.

Martin: i think if we manage to work through this list of things there's a lot of things can be solved by federated login... 

Peter: a web site may still have their own auth mechanism ... or FedCM... 

Jeffrey: Credential management is supposed to handle that - ... nobody has build that all the way out...

Peter: basic auth could have changed all of this .. but UX was bad. I would love the path be ... the browser is the ... center of auth and session management.

Tess: i'd rather people use passkeys... federated login is a vestigial flow... 

Martin: this idea that we create a single identity and then use it across other web sites is horrible... but a lot of web sites don't want to be in the business of holding credentials and passkeys... and passkeys are not easy to do.  

Dan: I think use of identity providers and passkeys together is not a bad thing.

Peter: if we can build into the browser enough of the auth APIs and session APIs then...

Martin: one of the things most concerning about development of FedCM was ... new capabilities ... session management ... we don't want the browser in the way.  The thing that we are most concerned with is providing the web site tools to get the job down. Establishing linkability is giving web site a choice... [?] 

Peter: sometimes session management overlooked security hole.. it would be nice if browser could help user to manage that.

Martin: other one to talk about is .. the fraud management stuff ... canonical use case for tracking... distinguish between activity on site I want and activity I don't want... so giving web site some amount of info about visitors to make that distinction ,... is important.

Peter: I accept fraud protection is a legit use case... don't accept the only way to deal with it is through tracking / fingerprinting.  

Tess: also private access tokens...

Martin: comes down to who do you trust...

Martin: what people are looking for is a scarce resource... that is then hard to fake... bank thing... another : offer a token that shows proof you have a govt id.  Also nothing is ever sufficient to the anti-fraud people.

Martin: google is shipping private state tokens, apple shipping private access tokens.. different trade-offs. Apple has gone for a centralization bias, google have gone for a decentralization bias and weaker privacy controls.

*discussion of client hints as an example of an API provides info to the server*

Martin: the UA String evolution plan ... was to break out things from the UA into client hints.

Peter: started off as a good idea and then got out of hand... client hints have also lied...

Martin: If you get better market share by sending certain client hints then people will send those hints even if they are lies...

Lea: looking at slides https://drive.google.com/file/d/1iSskMcnyF3I9czSi-IJPSqjBBzjzNUOC/view ... 

Dan: could we look at the list of questions?

Jeffrey: I'd like to go to use cases....  we need the use cases first.

Martin: SSO example is one of the use cases... Answer could be FedCM works and it's a pretty good solution ...

*discussion of bounce tracking*

Peter: a lot of enterprises moving to a hybrid model with external services...

Martin: and fedCM is a good way to manage that...

Peter: we don't want people "trained" to enter their credentials every where they go...

Martin: talking of enterprise SSO... what is the ideal end user prompting experience... "don't ask questions to which people won't answer yes"... Most people make the wrong choice...  This comes back to the privacy principles...  It should be private by default - private no matter what choices are made.  Some nice consent interactions...  E.g. webUSB and web Bluetooth have the same properties...  Choosers.  Some places where choosers are wrong... e.g. in media scenarios...

Martin: geolocation and notifications are 2 examples where web sites throw up a choice dialog often without context information.

Peter: is there consensus... on any of these topics?

Tess: I think there is consensus that the enterprise SSO question is answered with FedCM.

Peter: I think i heard consensus that a lot of the other types of federated login should be part of fedcm...

Jeffrey: *on partitioned popins* ...multiple domains and... sometiomes they want to open a popup... how do you idnetiify that this is the partitioned version...

Peter: related to the related web site... some people want amazon.co.uk , amazon.com to be the same... But some people *don't* want that - they want to be able to make the choice. Same things with the blogs comments... some people don't want their blog comments to be relatable across sites...  User should explicitly opt in... 

Lea: we say "the disquss use case"... but what are other use cases that share similar things...  We need to have diverse use cases...

Peter: I accept that there are use cases... for coerlation between tlds but I don't want that ever to happen by default.

Martin: one example given was... a service that maintained a number of resources.. a museum ... a repository of artworks... but you have to be logged in in able to obtain those images. And a number of institutions would use those images on their web sites... the credentials tied to that person would be on those images... entirely possible with fedCm to build that service... but direction they went was storage access... because it's awkward to use fedCM.

Peter: if you go to my web site and log in with fedcm via google you just get a name... .. minimal info... some of the fedcm APIs it's unclear... how much of that is only visible to the browser vs. "my site." before I log in.

Martin: your web site gains an identifier which can be dereferenced for a user to google's identity provider...

Lea: use case of payment provider buttons... that show last 4 digits of your CC?

Martin: i think it's a terrible use cases...  the tools that we're providing gain access to cross-site informtion and throw it on the page.. might not be your last 4 digits.. might be private photos... 

Lea: web sites can do that...

Jeffrey: not anymore

Martin: partitioning prevents that...

Peter: if i go to a web site i haven't seen before and it says "pay with your card ...1234" then user might assume they have been there before...

Martin: google accounts did this ... showed in a iframe in a page i'd never been to... it's a deception that I've logged i

Dan: web payment? [payment handler]

Tess: people complain about the centralization...

Peter: You need to be able to register payment handlers...  I will only trust a few small set of payment providers...  We don't want to create an ecosystem that says "just use stripe"...  

Jeffrey: fenced frames is what we get if we don't user payment handler... 

**Break**

# TAG F2F - Day 3



## Joint Session with the AB

Present: Peter, Martin, Lea, Yves, Tess, Dan, Hadley


## Breakout 14

Present: Peter, Martin, Lea, Yves, Tess, Dan
Guests: Kaustubha Govind, Shivani Sharma, Stephen McGruer, Josh Karlin, Michael Kleber

### [Fenced Frames](https://github.com/w3ctag/design-reviews/issues/838)


<blockquote>
  
Thanks so much to those who joined our F2F session today to go into further depth on Fenced Frames. 
  
First, we wanted to reiterate the importance of security and privacy. As we mentioned, we have just put forward the [Privacy Principles](https://www.w3.org/TR/privacy-principles/) document for W3C Statement. We want to make sure the web works for everyone, especially marginalised communities for whom privacy risks are often magnified. In that light, we are urging you to pay further attention to abuse cases, where bad actors could potentially make use of this technology to exfiltrate sensitive data. 
  
We are concerned that some of the use cases described might be considered abuse cases in some situations. The payment case raised, for example, involved the presentation to a user of a newly visited site of information that could make them erroneously believe that they had been to the site before.

We are also concerned with the amount of complexity this is introducing into the platform.
Beyond the obvious usability issues, too much complexity is also a security risk in itself, as developers are using primitives they do not understand rather than making informed decisions. If the solutions are too complex, developers will use a solution "that works" without understanding the drawbacks, and it can be "open everything from the top-level".

Some of us have reservations that a new element is warranted, rather than augmenting `iframe` which conceptually has the same general purpose (embedding and displaying another HTML page). 
Or, perhaps it would be more appropriate to build a baseline abstraction from which each specific usage is derived.
  
In addition, we don’t fully understand whether the use cases warrant an API that is such a significant departure from the way other embedding elements work. Is it not possible to implement these privacy mitigations and new capabilities with a syntax and DOM API more similar to other HTML elements like iframe? (e.g. with a `src` content attribute and corresponding IDL attribute). If so, why? 
  
This introduces a new wrinkle on the threat model for the web.  Presently, websites cooperate with the browser to keep information that is jointly held by sites and the browser as private from other websites.  Fenced Frames introduce a case where websites might cooperate to attack information that is held by the browser as private.  This new threat model requires new forms of isolation that ensure that content in a fenced frame cannot release information to the site outside of that context.  We would like to see more work done to analyze this and better understand it.
</blockquote>

## Breakout 15


Present: Peter, Martin, Lea, Yves, Tess, Dan

### [calc-size()](https://github.com/w3ctag/design-reviews/issues/955)

Invited Tab et al to a breakout

### [Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724)

**DP parameters**

Martin: *explains differential privacy* 

Dan: attribution reporting.. epsilon value is supposed to be small but .. 

Martin: no agreement on epsilon values.  Different epsilon values can mean differentiation between browsers.  
  
Peter: should we even do this?

Martin: *spirited defence of attribution reporting*

Peter: Technology in the UA that is not acting on the user's behalf ... so may not meet the threshold for me personally...

Martin: there are a number of ways that this could be much worse... ... is there a collective benefit that is obtained through the use of this ... so we still offer individual choice... these matters are really complex - having a specialised governance bodies decide ... Is there a collective benefit to having this kind of capability. 

Peter: I don't think the ad industry have a right to it.

Martin: but they may deserve it. The argument : there is a lot of content out there supported by advertising. the quality of the support degrades if you take away these capabilities. The rich people who see the ads and buy stuff subsidize the content. 

Peter: I hear you.  I am not anti-advertising.  However there are a whole separate set of people who benefit from advertising that are just a vector.  

Martin: this is where protected audience comes into the conversation...

Peter: worried about trading one horrible thing for another slightly less horrible thing.   So what is the path to the next step?

Martin: next step for me is much tighter restrictions...

Peter: we need to do this incrementally... won't block something I think is a reasonable step... but worried it becomes the end state.

Martin: one of the nice things about this - it places a knob in our hands - dial up or down - you personally have a dial.  You can set it to whatever. 

Dan: is that mandated?

Martin: good reception to that... 

Peter: my concern : this thing is not ideal but good enough - but people who want to abuse it can tie it with something else and then we're back where we started.

Martin: you can cut one campaign into two campaigns... I'm advertising to who I think are women or who i think are men - and then you have info about those groups... if you keep subdividing you are learning things about subsets of the populace - and that is targeting. However all ads are targeted in some way.  

*targeting through the ages*

*Discussion of political advertising... as a negative use case.*

Yves: There is a reason advertising targeted to children is forbidden in some countries.

Martin: I would like to encoyeage folks to continue their engagement in PAT xG..  but more or less decline to review... We can provide feedback about privacy parameters... 

Tess: I think that's basically right. CMA asked them to make ... a change... we could pile on and say the same thing... the thing I want to encourage: I've been impressed by the convergence between the 3 proposals... I'd like them to keep doing that.  This should be one thing.

Martin: the oucome where there are propeatary APIs in each browser for this is a bad outcome. Particularl for [small market share browsers]. 

Dan: the parameter... should be available to the end user ...

Martin: worried about ... that's in the relationship between browsers and their users...  

Tess: i see your point, Dan, but I don't think TAG can ask us to have a ..

Dan: we could say in our feedback to encourage the spec to include language to encourage implementations to put the user in control. In line with Privacy Principles....

Tess: could be a range ... if we worded that in a way to require browser to allow the user to access the entire range, there could be values that are not acceptable from a ...

Dan: also not detectable when you turn it off..

Martin: that's already inccorporated. 

*consensus to close this on this basis*

Martin: aggregated vs. disaggretated? 

Tess: i'd be inclined to prioritising aggregated.  

<blockquote>
The TAG has general agreement that providing some form of attribution is worth pursuing.

We encourage the proponents of this work to continue engaging in the discussions in PATCG (eventually PATWG).
The work there on aggregated solutions seems to be making significant progress, and we hope that you will succeed in converging on a single, consensus-based approach.

We are formally marking this request as "declined" because of the ongoing work.
We're otherwise supportive.
</blockquote>

# TAG F2F - Day 4

Present: Tess, Yves, Lea, Martin, Peter, Dan, Amy, Hadley

## [Identity on the web (broad discussion)](https://github.com/w3ctag/design-principles/issues/324)

Martin: identity is who you are ... the handles that we use to label people. Names, email addresses.. government issued credentials are identifiers, not identity

Yves: giving some trust relationship between you and the people using this identifier

Martin: main thing of interest is you can take what someone does in a given context and that identifier gives you a lever to use. Having a consistnent identifier across different context gives someone the ability to connect all that activity together. Given that people are different in different contexts, having an identifier cshared across those contexts gives them the ability to put things together and effectively deny you control of how yuo present yourself

Amy: we merged a pr.. we have [a principle](https://w3ctag.github.io/design-principles/#identity). Does it still meet our needs?

Dan: underscore that you are not your passport. Identity at border crossing is a key way to think about this problem. Less useful to talk about identity in a philosophical way, than int erms of use cases. Overreach and linkability are the biggest problems. ... We didn't want the justice ministery to have access to the home office information about .. the fact that even within the UK government there were firewalls set up to mitigate certain ministries getting access to information that links to your immigration status because that's not relevant.. I think some of that might have been broken down.

Martin: Tracking and the entire system of brokers and whatnot is gossip on crack. The whole thing is supercharged gossip. People gossip about each other and it's kind of beniegn but sometimes it's really bad... I saw someoen at the doctors office and overheard something, or so and so is having an affair with so and so ... that sort of stuff.. when it's weaponised and you do it at scale it's totally dehumanizing. You're taking peopless ability to control who they are in a given context completely away from them. There's a lot of incentive to do that..

Amy: I think we all agree on the principles... and we also have some of this in privacy principles, including the fact the web makes this so much more serious, at scale. What do we need to do now?

Martin: things happening now that are interesting. Increased push to make various forms of credential available on the web. Maybe we should have an opinion about that. The idea that it might be more easy to ask people for their drivers license or passport can be somewhat dangerous.

Yves: distinction between identities that you can repudiate or not. Governmetn based one, is non-repudiation. For others, you can say no it's not... eg. some whebsite that requires you to log in to get access to something.. you don't want to give your identity, you can get a random password, get a shared identity, no one really cares. It's a repudiatable identity, it's not you. Big distinction here. 

Hadley: one of the biggest challenges in this area is not only are we talking about so many different use cases around the term identity we're looking at an overlapping venn diagram of credentials, establishing uniqueness, and questions of privacy. Browsing history, purchase history, travel history etc.. really hard to talk about this stuff without being specific. One of the things that we can make things worse by not being specific and coming up with vague statements that may or may not be useful. Or we can be selective about what we say in the context of specific use cases such that we don't end up muddying the waters further. What problem are we trying to solve with our words?

Dan: +1. One way that we could focus is by use cases or user stories or user needs, and not coming up with our own but focussing on what user needs have been expressed in the proposed work around age verification, the stuff that was being proposed to be added to the FedCM WG (has that been removed?). There must be some work that has already gone on. We could comment on those user stories, and relate it to our principles.

Martin: A lot of the scenarios that are presented may be reasonable but there are other ways in which the same thing in a different context might be inappropriate. Eg. government identity, you have a government credential in a wallet somewhere and a website asks you for that. A government service asks for a government credential

Dan: is this a scenario documented in some proposed charter or somewhere we can point to?

Martin: the FedID thing. Digital Credentials spec has no explainer and no introduction. The use case I've heard expressed is government issues an identity credential to everyone, used to access government services. Pretty stragithforward and benign application. Having the ability to do that in a verifiable safe and easy way on the web would be a positive thing. I think that's generally regarded as fine. But once a credential is there anyone can ask for it. Estonia and bank ID in Sweden is ancient... what we see happening in India for example is aadhaar was intended for use in going to see a doctor or getting benefits, but it turns out if you want to buy a milkshake you're giving them your aadhaar. That's not the web that I want.

Dan: that's an example of overreach

Tess: it's fair to be concerned that the feature could be an attractive nuisance. Sites that know they want some kind of heightened idea that you are who you say you are. The space of social media sites today, one of the axes along which they vary is having a real name policy. I don't particularly want sites that have that policy to start prompting for a government ID

Peter: I do accept social media and dating sites etc are rife with abuse and it's a problem and I accept the use case that it's beneficial to them to be able to prove it's a real person's account and not a sockpuppet. But we want to make sure they can solve that without having to bind their social account to government ID

Tess: the other day linkedin prompted me to upload a copy of my driver's license..

Dan: [The digital credentials spec](https://wicg.github.io/digital-credentials/) in WICG. It had been proposed to be added to the federated identity wg. It looks like it's no longer in that charter.

Tess: the FedID WG is already chartered, but there's [a proposal to add it](https://github.com/w3c/strategy/issues/450). I'm not sure how that is tracked.

Dan: https://w3c.github.io/charter-drafts/2024/wg-fedid.html Where is our feedback best placed? What do we have to point to as a way to bolster this feedback?

Martin: Explainer doesn't really address a user need. It mentions risks of abuse - surveillence, censorship, intrusion. We have a lot of that in the privacy principles already.

Hadley: Simone says EWP 2.5 points out we don't create threats, and mitigate threats we already have

Dan: I think we're all violently in agreement on a lot of these topics about identity and avoiding dystopia. How can we best focus our energies so we can achieve that goal. Would pointing them towards these things be the right thing to do it? 

Tess: in the short term yea. In the longer term..

Martin: we need a strategy. That's what I'd hope to get from this discussion. Can we argiculate the use cases? And also risks.

Hadley: and clarify who are we trying to convince, and what of. it's going to bie different points for different audiences.

Martin: I'm not sure it's about convincing. There are a lot of people working in this space that there are risks and don't want to be resoponsible for making those risks a reality but they don't know what to do about it

Hadley: with this charter, who is making a decision and what decision do we want them to make? We could have something avaialble to pint to in spec reviews in order to convince a spec author that what they're doing is going to be harmful. We could burn a lot of energy just opining, without any focus.

Tess: sometimes we burn energy opining and turn the result into a finding. Pointed strategic advice to an area..

Martin: seems like something..

Hadley: I'd still ask who we're trying to convince, and of what?

Tess: if we only narrowly focus on the immediate quesiton of this charter update, we're missing the real ability to be impactful here. We should help with the charter, but it's just paperwork.. we need to help them succeed

Dan: I like the idea of doing a finding. Tess and I discussed in Hiroshima about doing a finding around this topic that would focus on putting the UA in the driver's seat wrt mediating users' 'digital identities' between them and third parties. Tess was concerned that some of the work going on was viewing the UA as the threat.

Tess: there's prior art here trying to route around the browser.. that's what makes the web different, the UA as mediator

Martin: it's pretty close to critical, protecting the user's identity from abuse, as a UA

Dan: privacy principles many are pointed at UAs, this fits. And the use case about having multiple digital credentials which the user gets to choose which one to assert. The user is in control via the auspices of the UA. The UA might know I have two digital passports, but the third party doesn't get to know that unless I say that it's okay

Tess: in order to enter the US you are required to use your US passport even though you hold other ones. We could not bother presenting you the choice of yoru british passport because we know you're not allowed

Hadley: and countries where you could enter on your british passport and you don't want them to know you have a US passport because it's a security risk

Yves: ... multiple passports ...

Peter: minimum amount of information need. That should be part of this advice that the UA could help broker that, shield from over exposure of information

Martin: very basic use case of passport through border control. Those are invasive use cases that have this absolute requirement. I'm concerned about the milkshake case. Dating website that wants to know if you're creating multiple accounts.

Peter: age verifiation and home address

Tess: and not even the issuer of the identifier that proves that

Peter: or how far past 21 you are

Martin: Spain has put out a spec for age verification for adult websites. it's horrific

Tess: several state level ones in the US that are awful

Martin: a problem there is in the buying alcohol case, maybe you don't really care that the government who issued you that credential would be able to find out, maybe they shouldn't, but mayube it's not such a big deal. But in the case of Spain the way they propose it works is you go to some goverment application and grab a token, a QR code, give the token to the website. The website and the government can danonymise you through that process. 

Tess: systems like national health care. Government issues id and are your healthcare provider.. if they can link alcohol to medical records.. this is going to materially affect your access to care

Martin: and when they outsource the care to a for-profit company...

Martin: realised realtively early on is that all of these use cases have commonalities. A lot of the way sin which people think about them drives them all to the sam econclusion. The Technical mechanism you use in each one of these scenarios may be funadmentally different, with a specialised response. 

Tess: we tend to not restrict expose of web apis to certain websites. We quirk things in that way. You can imagine saying in order to get access to the government api we have to have pretty solid assurance that you're a government.

Martin: exactly. Then you don't have the milkshake vendor asking for your credentials because they're not authorised for that. Adult content - we need unlinkable proof that you're of an age, and that's it. Creating an account on a social media service and proving that your'e a unique person, perhaps rooted in the fact you have a government issued credential is different again. Also comes up - the fraud mitigation scenarios. Being able to say to an arbitrary website I have a credential - I'm not a robot.

.. use cases ..

Martin: are we looking to leverage third party reputation? this third party thinks I'm an honest participant? Or yoru identity as known to that third party

Hadley: both plausible, depends

Martin: two things or more..

Martin: this seeds a discussion for saying something about this broader topic

Peter: can we get people to think about operating at a slightly higher level of abstraction? In the case of age verification, it would be nice instead of giving a digital credential that asserts I'm over this age, but the credentail says I have the right to buy alcohol. It's possible to decouple that from the age

Martin: it is decoupled in a lot of jurisdictions. Other reasons they don't have the right to buy alcohol even if over age

Peter: appropriate jurisdiction has the ability to restrict someone's access to something that is normally keyed by age

Martin: ways that would also fail... a citizen of the country of saudi arabia would probably never get that flag attached to a credential, but they might not be resident in that country. When you build a system like this and start to depend on it can be inflexible

Peter: can and will have problems.. just suggest people think about what's possible

Martin: we identified that a lot of people aren't necessarily able to access services that can provide them with credentials. Having a way for those people to be able to access a service was critical. For age verification - there are people who just can't get a drivers license or passport. Stateless, undocumented.

Peter: huge problem of people not being able to get IDs, citizens, don't have a bank account. We should probably say something about that.

Martin: potential for discrimination based on who has issued a credential. In these scenarios, you can see if you're trying to buy alcohol in louisiana they won't take an out of state driver's license

Tess: even within an issued by a US jurisdiction and being asked for in a US jurisidction case... in some states you're not allowed to buy alcohol using an out of state but in country id that is not a drivers license. You don't know how to ..

Dan: can we also add voting

*discussion about disenfranchisement*

Hadley: would also help to have a list of anti use cases. "As an advertiser I want more information on the people I'm advertising to". We see these patterns.

Martin: centralisation bias that comes with some of these - a small number of identities who now get the ability to control the flow of this information. One of the solutions for age verification as proposed by the UK government was banks be responsible for doing that

Hadley: propsed because some of these orgs are more palatable than the government - more 'decentralised'. We should be careful using 'centralisation' here

Martin: what we'd like to see is people having the ability to choose who acts on their behalf. Some kind of control or governance that can be used to help decide who can participate, who is trusted.

Hadley: agree and accept that. That logic is how they ended up with the banks in the first place. Agree with your point, just not "centralization as words"

Amy: gatekeepers

Dan: who wants to edit this?

Martin, Tess, Hadley and Dan: let's do it.

Dan: a finding is a few related points. Centrality of the UA when it comes to helping the user assert or protect their identity in a hostile world.

Hadley: that's very much web architecture. I agree.

Tess: two things - reasserting that the UA being a UA is a central tenant of web architecture. Then applying that in this very specific case. Guide people who aren't trying to create dystopia but might do accidentally.

*we wordsmith this doc*

## Fodder for Identity Finding - the role of the User Agent in something something Identity on the Web

Key point: putting the user agent at the center of allowing the user to control what aspects of their digital identities are being asserted or exposed at different points. Adhere to the principles of data minimization... 

### Use cases

* "Milk Shake" Case

  Milk shake vendor asks for gov. credentials and therefore knows more about you.

* Multiple Passports

  User should be able to choose which digital credential to assert.

* Age verification in context of buying alcohol

  Maybe you don't care the the govt that issued you the credential knows that you bought alcohol, but maybe you do...

* Age verification for adult web sites

  In some proposals, the govt can de-anonymize users.  It should be some proof of age and that's it.  
  
* Fraud migitation 

  e.g. "I'm not a robot."
  
* Demonstrating credibitlity from references in a social graph.

* Demonstrating that I'm a person with access to such and such stuff... e.g. for Amazon, I am this person and should be able to make purchases and see previous purchases... 

* Person demonstrating another 3rd party relationship. When the site asks you to log in with facebook / google, you say that you havea a relationship with that 3rd party. 

  Reputational 

* Demonstrating uniqueness

* Repudiation of identity - proving that someone else who is impersonating you is not you.

### Anti-Use Cases

Things we don't want to support in our specs - e.g. state surveillance. Tracking for tarteting ads. Etc. 

### What else can we say?

Adhere to the design principle and principles articulated in the privacy principles document. Adhere to data minimization.

Decoupling credentials from things like age.  For exmaple, some people who are over *drinking age* may not be allowed to buy alcohol.

A lot of people are not able to access services that can provide them with credentials. This creates a massive underclass. Maybe they're unbanked / Stateless / undocumented / etc... 

Potential for discrimination based on who has issued the credential. If you're trying to buy alcohol in XYZ state they won't take an out-of-state driver's license... 

Voting ID requirements - making it even more difficult - disenfranchising people who are already marginalised 

Centralization bias that comes with these systems - taking a small number of entities that get to control the flow if information. One solution proposed for age verification for example is that banks be responsible - that gives banks info they shouldn't have and also doesn't serve the unbanked - leads to concentrations of power. 

improving privacy is also improving usability for users, in this case.

## Ethical Web Principles 

Martin: this is a declaration of what we value... it's a statement of goals... 

Dan: I think this is ethics. I think this is principles.

Peter: I think there's value in documenting the ethical framework that went into the decisions... that underlies what the web is. you can't separate ethics from technologies. every tech choice is an ethical choice.  I think it helps to frame it in terms of ethics.

Tess: ethics / values / morals are often popularly interchanged

Tess: because of level of socialisation this has had under this name I think it's not worth changing the name at this point.

Peter: if we change it away from ethics then people will see us as backing away from ethics... 

Dan: can we therefore close this issue?

Dan: *merges PR from Martin* https://github.com/w3ctag/ethical-web-principles/pull/129

Martin: transplant priority of constiuences ...?

Dan: i think that belongs where it is, in the design principles doc...

Peter: only heading is 2.12 - 

*we bikeshed the 2.12 a litle*

*we [look at a PR](https://github.com/w3ctag/ethical-web-principles/pull/130)*

*we agree to put other PRs and issue 128 on back burner*

*we agree to tell PLH we have closed the open issues and we are good to go with the call for the AC vote*

## Discussion on next meetings

*Discussion of idea of F2f not long after tpac...*

*We zero in on first week of December, split between Boston and Edinburgh, or Edinburgh with remote participation for those who can't make it.*

## Discussion on breakouts 

Too many meetings right now.

Peter: rather have fewer breakouts with more people in them... 

*discussion of how we can make more of this work async*

Martin: *Suggestion that design reviews first cut is farmed out to a larger group of people who can do the initial reviews... Our time is spent looking across the design reviews and establishing patterns...*

## Afternoon session

### [High-level web platform vision and improving the TAG’s Impact/Effort ratio](https://github.com/w3ctag/process/issues/36)

Present: Peter, Lea, Martin, Tess, Amy, Dan, Yves

Consensus to start a gap analysis repo.

Consensus that it’s a good idea to prirotize reviews based on some rubric, though the devil is in the details.
Factors discussed:
  - Early vs Late: no consensus
  - Buy-in: consensus
  - Urgency: consensus, as long as we're the ones assessing it
  - Scope: no consensus 
  - Recency: consensus

Consensus to update explainer guidance explicitly encouraging conciseness.
We don’t necessarily have to mention that they will be reviewed synchronously.

New design review template is a mess, move towards a form

Explainer reform:
- Our explainer explainer is a wall of text that does not make it clear what is the top priority
- Some good material here: https://github.com/mozilla/explainers#minimum-viable-explainer
- Consensus that we should make it clear that the most important sections are:
  1. User needs / high level use cases (at least 2 diverse ones to avoid overfit)
  2. Usage examples iff code is involved
  3. Alternatives considered





