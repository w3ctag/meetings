TAG Minutes for Week-Of 17-May-2021

### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/05-17-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-05-17](https://www.timeanddate.com/worldclock/converter.html?iso=20210517T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Special session on [WebID](https://github.com/w3ctag/design-reviews/issues/622) with guest @samuelgoto

### Breakout B (US / APAC) - [2021-05-18](https://www.timeanddate.com/worldclock/converter.html?iso=20210518T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529) - @hober, @torgo, @hadleybeeman, @plinss
* [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia
* [Design Principles PR: Make naming consistent about methods and arguments](https://github.com/w3ctag/design-principles/pull/312)
* [Design Principles PR: Add text for low-level vs high-level APIs](https://github.com/w3ctag/design-principles/pull/291)
* [Design Principles PR: New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

### Breakout C (APAC / Europe) - [2021-05-18](https://www.timeanddate.com/worldclock/converter.html?iso=20210518T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Special session on dueling tab capturing proposals featuring special guest @dontcallmedom
  * [Early TAG design review for captureTab](https://github.com/w3ctag/design-reviews/issues/609) 
  * [API for caputuring the current tab](https://github.com/w3ctag/design-reviews/issues/625) 
* [Shared Element Transitions - Early Review](https://github.com/w3ctag/design-reviews/issues/631) - @cynthia, @LeaVerou, @plinss

### Plenary Session - [2021-05-19](https://www.timeanddate.com/worldclock/converter.html?iso=20210519T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @torgo
* [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22)


## Minutes

### Breakout A (Europe / US)

#### Special session on [WebID](https://github.com/w3ctag/design-reviews/issues/622) with guest @samuelgoto

Present: Dan, Tess, Peter, Amy, Rossen, Lea
Guests: Sam Goto, Ken Kaan, Alex Russell, Kastuba Govind, Majid, Christ Wilson, Heather Flanagan, Michael Knowles, Yi Gu, Majid Valipour, Kaan

Dan: circulated [notes](https://github.com/w3ctag/meetings/blob/gh-pages/2021/05-Arakeen/minutes.md#webid) from f2f. We were curious about this and have a back and forth.

Rossen: one of the topics was how does WebID fit into the overall umbrella of efforts around identity?

Dan: it's a big topic. Everyone has some battle scars from something to do with digital identity, so when something comes up about that it raises a few eyebrows. It has the potential to touch every single piece of the web platform. That's why we're trying to give it a lot of energy and try to understand it so we give you some value.

Sam: thanks for taking this on. We apologise for verbosity and lack of clarity with a massive amount of documents. This feels like a big project, and a massive stream of dead bodies in the past. WebID was formed as a preservation effort, looking at how other browsers were moving and how Chrome was intentding to move to a more privacy oriented world, and how some of that was in conflict with federation. General observation that federation was something we'd want to have in the future. Alternatives are usernames and passwords and native applications. Anchored itself into this preservation effort, federation is very good, better than usernames and passwords. Let's find ways to get ourselves out of the existential threat to federation as browsers are moving towards mor eprivate things. That's the overall contet. We started to understand more some of the breakages of federation, as they are locking down third party cookies, certain aspects of federation break. There's a sequency art of understanding what's going to break when 3p cookies go away and being very pragmatic and finding alternatives ot the things that will break. A lot of the things federation was built on are also the things being abused by tracking. What I go over in the explainer is the classification problem. A problem that browsers cannot tell the difference between federation and tracking. They are both using the same low level primtiives. iframes, 3p cookies, redirect and top level navigation. The first order has been how to tell these things apart so we can apply different policies. Let's continue to tighten up the low level primtives like iframes and 3p cookies and redirects, and offer high level alternatives that make a tradeoff for the browser to apply identity specific policies. That was the overall context in which this project forms. Early on attempt to preserve federation so it doesn't go away with 3p cookies. Lead us to high vs low leve primitives.

Dan: from our discussion last week, I wanted to drill down on this statement that 3p cookies being deprecated or no longer working doesn't allow for federation. All the browsers I use have 3p cookies turned off, an option to turn it off, I regularly log into services with other services. I use medium where I'm logged in via twitter, dev.to via github. In those cases identify federation seems to be working. What is perceived as not working when 3p cookies are off? The specific things that are not working?

Sam: meta point - generally understood that breakages of 3p cookies in federation are substantially smaller than when link decoration gets tidied up. Not something we expect to be an existential threat. Most things can fall back to other mechanisms. One of the challenges we expect federation to evolve as 3p cookies go away is things to look like redirect and link decoration so we may corner ourselves. It's why you'r enot feeling a massive amount of tension - there isn't one, the things are light. They're not zero. In the [link](https://github.com/WICG/WebID/blob/main/cookies.md) it enumerates the things we expect to break. Sprinkles over social login and some enterprise use cases. Button personalisation is a good example - when they know your  name and profile pic. iframes and 3p cookies. Other thing, less sprinkle,  is session management. The ability to log yourself out of all the rps you have logged into. More for enterprise than consumers. Things like refresh tokens too are something we're learning. Going around the industry asking for things that are going to break when 3p cookies go away, those are the hands raised. This is the use case we want to preserve. 

https://github.com/WICG/WebID/blob/main/cookies.md

Kaustubha: ITP and ... they have heuristics, Safari has it in an earlier version, I tried digging through and didn't see a mention of this being removed, if clicking on signing invokes a popup and user interacts with popup then the popup gets access to the cookies and you can communicate that back.. in the case of safari and firefox they have heuristics to ensure that federated login keeps working.

Dan: what are the mechanisms being proposed?

Sam: we're going through and understanding all of the surface area, low level primtives, every single one that federation uses and trying to come up with alternatives. 3p cookies and iframes. What makes it more broken is top level navigations and post messages across sites. If you use federation for the most part it's a cross-site communcation. You get redirect to twitter, from eg. medium, twitter gets 1p cookies, you log into twitter, twitter asks do you want to allow medium to know who you are, then use a post request on twitter across to medium.com. That is a cross site communication channel like 3p cookies and iframes in popups. This is a uncontrolled cross site comms channel that allows one origin to talk to another in an uncontrollable fashion, and to exchange things like global identifiers, when you log into medium with twitter medium is getting access to your twitter account or any other global identifier like your email. Having access to these it can build it sown profile and also join that profile with someone else. Medium can take all your articles read and sell that to NYTimes. if you log into NYTimes with twitter both can join your twitter handle as the key and build a larger profile. That constitutes uncontrolled cross origin comms. What we imagine is all thes elow level primtiives, post messages etc, are indistinguishable from tracking. Trackers go to this after 3p cookies being blocked. We're imagining high level apis as opposed to general purpose api like top level navigation or iframes. High level apis that allow comms to be done with IDP in a way a browser can reason over it. There are only so many protocols for federation, OIDC being the largest. It is not inconveiveable for a browser to enumerate, OIDC, SAML.. all these are interoperable, so browser can control that channel and gather the users consent as the users are running into trouble oversharing information. 
... tl;dr - replace window.location.href or form.submit with a credential manager api like navigator.credentials.get that makes the brokering between ther elying party and IPD in a channel that is well understood and controlled.

Dan: what's to stop those parties having that out of band comms in any case?

Sam: that's a good question. We cannot once you have that initial identifier exchanged there's nothing to preven them from colluding. The point is to make sure that first connection, exchange, is the browser gathering enough user understanding and consent such that they can feel comfortable knowing that collusion could happen. The other thing is for collusion to happen at scale it becomes observable. If twitter as an IDP provides a service for RPs saying here's how you can dereference your global identifiers, that becomes known, the web as a whole can see this is where they are colluding. While the browser cannot enforce that offline collusion it can make it observable.

Dan: point of clarity - in this world, the browser would prompt the user for 'would you like to be identified through this federated approach'? We're trying to balance security & privacy & fingerprinting concerns, ensuring that, I go to site xyz.com and I don't want that site to know that I am logged in or have an identity on github.com or twitter.com. Is that encompassed in your model? that everything is under user control in terms of.. even allowing that site to know informatin that could let them know that I participate in this other identity that is federated?

Sam: yes, absolutely. As a privacy-forward api its preserving that confidentiality of your status with your IDP as you go through websites. We would protect. That is how federation works today - if you are on medium and you click s ign in with twitter you get redirected to twitter. If you're logged out of twitter it does a page auth. After you consent then you get redirected back. An RP today with redirects doesn't get to learn that bit of your status on twitter unless twitter does it. Which isnt' the case for most of the big consumer IDPs. 

Dan: what we're trying to focus on is more the thinking about the TAG design principle 'safe to browse'. You could receive a link to any website.. limiting the amount of damage when someone clicks on a link is one of the core design principles. 

Sam: 100% in aligment. Recently ran into this personally. I had comment widgets on my blog, I didn't know I was imposing on the readers of my blog telling your IDP that you were reading my blog. I didn't know I was imposing that by sending people link to my blog, they were paying the price of their IDP knowing they were reading my blog without your consent.

Dan: this has been thrown at different identity schemes - a few years ago in the UK the NHS decided to put facebook like buttons on every single page of their website ,including if you were researching symptoms a disease, whether you were interacting with the button or not facebook could correlate that information back. Was all written up. Exactly that. Good to hear it's on your mind.

Sam: a couple of philosophical things - we've been asking ourselves the role of the browser when it comes to ID. We have drawn very cleary privacy and security that the browser should pull for itself. Between ID providers in a secure and private way, all clear. but whether a browser should b eopinionated about intrusiveness or UX. What are the principles that one should use to make an asssessment over intrusiveness of UX. What are the principles that decide if a notifications api is put behind a user gesture. Or starting a download behind a gesture? or a Webauthn flow? Popup blocker? What is the principle that made us say you can only window.open if you have a user.. aside from privacy and security they are all intrusiveness consequences. Any guidence?

Dan: in the design principles we have .. this has come up on a few reviews .. certainly part of safe to browse, and in security and privacy self. 

Tess: a couple of others. Meaningful user consent for dangerous or powerful actions. All three documents - ethical web, design principles, and security & privacy questionnaire touch on this, though not under a single heading.

Dan: one thing that comes to mind is the discussion we had about the clipboard api. The view in the TAG when we discussed this was a user gesture or affirmative user action of some kind must take place in order for the webpage to gain access to the clipboard. Whereas that information might be available to a native app, coming back to safe to browse, there's an expectation of more safety when it comes to running in the web context. Between ethical web, design principles, and security and privacy we do address some of those. We'll raise an issue to discuss more clarity on that.

Sam: yes, looking for guidence there. Hadley  mentioned some of this. Some may be percieved as abusive or intrusive . Wondering where to draw the line there.

Dan: especially because this could be construed as trusted UI. Any time you have trusted UI ncluding things like permission prompts we see people in the wild gaming that system. The famous screenshot of the webpage that says a popup okay with notifications and an arrow pointing to it saying prove you're not a robot by clicking okay.

Sam: the notification api is the best to derive principles from. None are easy questions. Struggling with the ossification problem . Problem you get as you trade genralisation to specialisation with high level apis. By browser being opinionated about the transaction the exchange of information between RPs and IDPs. There are fewer browser engineers than idnetity people. Whath todya is done by an army of facebook/google/etc engineers will be done by fewer in the future. The mor ethe browser pulls for itself in terms of UX the more it strangles innovation and accessibility. We're trying to minimise that to have our privacy and security goals. We don't know an answer but want to see ifthere's precdence.

Dan: clarify ..? worried about the UX becoming too ..?

Sam: concrete example - in authentication, Basic Auth. Browsers invented an HTTP header. that has never been use because it's faster to innovate in user land than browser land.

Dan: web payemnts more recent - struggles because of its advantage that it provides the payment UI in a very single way that is not customisable. That's both an advantage but from a service designer perspective a disadvantage. You can't differentiate as easily. 

Sam: we imagine progressive disclosure of identification - to pull as little as we can for ourselves, but have that as the starting point. Things we believe are common between federated auth. A  numeric identifier, first name, last name, email, etc. To have that as the things the browser can be opinionated about, but very quickly open into a web view like feature that enables an IDP to offer more things. But to be opinionated on that very first instance. I just wanted to give you a sense of the struggles here. We have to opine on privacy & security but by doing so we're also struggling innovation. As opposed to basic auth, we expect that a lot of the other leaky ways you can do cross site comms can be tightened up and that's going to drive demand for the safer way. IDPs and RPs are going to use the weakest link, but as browsers are tightening up every link that becomes the most streamlined way to do federation o the web.

Dan: hw can we guarantee that this new system enables anybody to become an IDP and also doesn't enable spammy IDPs and bad actors? Two conflicting requirements. What we don't want in the web is we don't want in place a system where only large orgs can become IDPs. I should be able to provide my own IDP facilty on my blog. Anybody should be able to take advantage of that without having to register or become part of an allow list. 

Sam: this is the NASCAR flag problem. We have never as an industry been able to make progress on this. For the most part for consumers IDPs are not interoperable. THey don't interoperate with one another. Email is the opposite. SMPT and POP interop. IPDs don't today. it's not th einitial pull for webid, but a positive unintended consequence, that by being opinionated by how that initial thing gets exchanged in browser land you're forcing them to interop with one another. You're in a much better position to decouble identity providers. Not only a technical problem, also economic. That initial point of interop is one step forward. 

... Also.. we're planning to do a [workshop on WebID](https://github.com/WICG/WebID/blob/main/meetings/2021/25-26_May_2021.md) in a couple of weeks, May 25/26 after PrivacyCG f2f. Browser engineers, and IDPs, where they stand on this problem. All invited. 

... TAG is uniquely positioned - to look at all browsers at the same time. You can see what we cannot see. You can see how firefox positions itself, Edge, Chrome, and find commonalities. Be specific about versions. We were doing approximations, but we could use some guidence in helping us understand how browsers are evolving to a more private web.

Dan: I don't think we have privileged knowledge.. we try not to operate with privileged knowledge about the internal workings of different browser groups. we do put a high value on interoperability. That's one of the first thing swe look at in review process. What's the multi stakeholder buyin? Is it one browser engine? Something with multiple parties engaged? Looked to us like there were good signals wrt to WebID. Also look to see published standards positions. 

... If there are issues with that we will comment. We don't necessarily.. it's a red flag. We can't stop work. We will raise lack of multi stakeholder support. If things move into a WG with W3C process you have to demonstrate multiple implementations. We see it as part of our guidance to push as muc has we can to get people to talk to each other.

Rossen: to me stands out as one of the much better well organised proposals in terms of how much prior leg work brought to this issue. This highlights how huge of an uptaking this is and I'm looking forward to see if this is going to be covered in this one reivew. This is such a huge undertaking. Curiosu to see how and where this goes. The highlight of prior art and transparency to the process is really well organised for this review. Great job. 

Dan: we discussed this a lot during our discussion.. referenced everything

... appreciate being able to have this discussion. We're going to come back to this and try to provide further value. And address the issues you have raised on this call. If you have further points you'd like to raise with us, put them on our issue. 

Sam: appreciate the time, we'll take the feedback seriously, I'll try to articulate better the things we're struggling with in the issue for the review. To Rossen's point, we expect this to be a decade long project not a quarter long project. We want to know if it's directionally correct, not a spec to bikeshed on.

Rossen: What is the expectation of this particular review, you answered it. This is the right direction, obviously not the last review. 

Dan: thanks everybody!

_Curated comments from whereby chat:_

[Heather Flanagan] This might be of interest: this is a list of issues put together by the OIDF browser interactions group. The items noted as being impacted specifically by 3p cookies are tagged: https://github.com/IDBrowserUseCases/docs/issues

[Kaustubha Govind (Chrome)] https://developer.mozilla.org/en-US/docs/Web/Privacy/Storage_Access_Policy#storage_access_grants
See "Temporary Compatibility Fix: Automatic Storage Access for Popups" on https://webkit.org/blog/8311/intelligent-tracking-prevention-2-0/

[Heather Flanagan] It's tricky because it's not always the user's choice. I'm thinking of examples in federal government where they are explicit that they are tracking All The Things for their users.

[Alex Russell] should point out that the benefit of putting that in trusted UI and using our long-agreed promise-based request pattern allowed browsers to build trust mechanisms about that sort of thing
that is, the work we (the TAG) did back in '14 and '15 on this enabled exactly what we hoped it would

[Heather Flanagan] https://github.com/WICG/WebID/blob/main/meetings/2021/25-26_May_2021.md


### Breakout B

Present: Peter, Sangwhan, Rossen (partial)

Regrets:

##### [Geolocation API](https://github.com/w3ctag/design-reviews/issues/529) - @hober, @torgo, @hadleybeeman, @plinss

##### [WebGPU and WGSL](https://github.com/w3ctag/design-reviews/issues/626) - @hober, @cynthia

##### [Design Principles PR: Make naming consistent about methods and arguments](https://github.com/w3ctag/design-principles/pull/312)

Merged

##### [Design Principles PR: Add text for low-level vs high-level APIs](https://github.com/w3ctag/design-principles/pull/291)

##### [Design Principles PR: New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)

### Breakout C

Present: Kenneth, Lea, Dom (guest)

Regrets: Hadley, Dan, Amy

Dom described the differences between these proposals. It appears that the main difference is how they handle embedded content and whether browsers do any re-rendering (e.g. to hide visited links). Apparently 609 is the one worked on by WebRTC, whereas 625 has no support by WebRTC and is just a proposal by Google. The author of 625 is working together with WebRTC now though. 609 requires websites to opt in to embedded content capturing through a header.

Lea: I'm concerned about introducing yet another opt-in to the Web. Most websites will not be updated to include it, even if they're perfectly fine with being captured. Can we can re-use one of the existing opt-ins, even e.g CORS while still preserving user privacy?

DOM: CORS is too powerful for this

Lea: In that case, what if when CORS is turned on, the new opt in is not required? Many websites already have CORS headers.

Dom: That's a good idea, we should discuss it. 

...

Dom: So in the end, was this helpful?

Ken: Yes, but this should all be written down somewhere, ideally in the issue.

Lea: Yes, it would be good if one of you posts a comparison between these two proposals in the issue, especially since 80% of the TAG is not in this call.

### Plenary

Present: Dan, Peter, Lea, Amy

#### Rollups

##### Breakout A

Dan: I asked Sam why it's in WICG. It doesn't make sense. Should be in its own CG, it's such a big topic. Maybe a new Web Identity CG. Bring in a wider community by taking that approach. WICG limits. He asked us to help them outreach to other browsers.. which is odd.

Peter: agree, own CG

Dan: positive on the ideas

Peter: WebID is going to be a long process, right now it's identifying problems and vague solutions. Maybe proposed solutiosn oculd get incubated in WICG but a separate CG to hold the big picture and collect proper stakeholders and information  *crackle crackle*

Dan: model of the immersive web, a community of practice around people that were working around XR/VR/AR and was very effective in focussing that and creating a bunch of specs which then were promoted into W3C WGs. But it doesn't need to be a new WG, could be existing. Process issue more than content. Content-wise I'm unsure if I understand what really breaks when you don't have third party cookies. Is the answer to have browser mediated UI? Or is that they want browser mediated identify federation, so it's the answer to when 3p cookies go away? I don't see the justification

Amy: They were trying to get ahead of things - there are lots of things that will break because 3rd party cookies go away and there will be follow-on impacts.

Peter: losing 3p cookies doesn't break, but breaks smaller aspects of federated identity, to get those back you  need other comms channel, and we're either inventing something that looks like 3p cookies, or something with a very narrow use just for login, so in that case why not build federated identity into the browser. I think it's high time we do that - we've had basic auth, clientside certs since early days, both suck. Seriously problematic, almost unusable. Nobody uses them in the wild. Only on private sites. No good UI for managing your login state. High time we have identity management done well in the browser. I'm in favour of this work.

Dan: yes and.. identity federation is such an important aspect of how these sites operate, and it has to do with branding and brand identity how brands are represented. People get really fussy about that kind of thing. I'm worried that if we constrain it to something that needs to be part of a browser based UI that's different for every browser, people won't want to use it, they'll want an alternative, there will be other approaches, so we'll end up in a similar situation to web payment. It's out there, and it's getting some usage, but not mainstream because vendors and payment processors want to control the UX. They're scared of outsourcing the payment UX to the browser. They're only willing to do that where they see an enormous benefit, eg. using apple pay. Enormous challenge.. not technical.

Peter: and social aspect. If this is done right it should tie in nicely with webauthn, so we can get nice passwordless experiences and better 2fa as part of a universal login flow, will help with adoption. I don't get - a lot of the users seem to want to have integrated federated identity. Even browser engineers who don't want to create a new account, want to use eg. fb login.. that attiude blows my mind. Why do I want to conflate my identity across all sites. Accept that there's a use case... but I don't get it

Dan: personally, I use it when it makes sense. If I'm logging into something like glitch I use my github id

Peter: because there's a reason to tie those two together, that makes sense. Then you go to some random other site.. to leave a comment.. use your fb? github? convenience for driveby..

Dan: argument to using social media identity to do something on someone else's social media thing. Disquss which allow for various social identities.. Could be an antipattern.

Peter: could be a random store.. .don't want to log in with fb.. I get why they want it.. that's why I don't want to use it, don't want to correlate

Amy: they want it because they get better stuff from Facebook but people also don't realize that's happening [the data leakage]  I wrote my PhD thesis on this.  I agree it's an important set of problems to solve - and can be done well in the browser. Managing identities and context in a really smooth way that matches how we do it naturally offline is the decentralized social web dream.  I think getting a CG and getting a wide community is a good thing - decentralized web crowd, oauth... 

Peter: agree.

Dan: there are so many different efforts, a concern is that lots of people with opinions get together and stall it.. sympathetic to that. It needs to be actively managed. The model that Tess and PrivacyCG have used, very prescriptive about work items.. 100s of people from a wide community but also managing to get things done and not get bogged down. 

Amy: Credentials CG also a good model for process.

##### Breakout B

Peter: we skipped geo and webgpu -  we merged a coiuple of PRs - consistency, reviewed a few others.  Attributes vs methods comments from Lea. We're going to merge.

Lea: OK.

Dan: have we had enough changes to ask Yves to make a new version of design principles?

Lea: when was the [last one](https://www.w3.org/TR/2020/NOTE-design-principles-20201110/)?

Dan: Need a stable URL for design principles. We've gotta fix that somehow.

Peter: will do some tweaking on the PR... Redoing that brought up another issue - on functions/methogs args/params - we were also inconstant about attributes vs properties. JavaScript uses properties WebIDL uses attritubes.  We should have an editorial guideline and apply it consistently. Sangwhan raised #315

Dan: i opened a design principles issues on user activation on the back of our discussion in breakout A

##### Breakout C

Lea: Dom described the differences between the tab proposals - differences in how they handle embedded content. 625 is just a proposal by google but not brought to the webrtc working group.  in 609 there is an opt-in by header - but that's problematic.  CORS too powerful...?  Dom said he would write it in the proposals. Still unclear on what the differences are. Dom has written some comments in the 2 issues... Privacy and security issuse need to be addressed but skeptical about introducing another opt-in.  

Dan: is the google proposal something in WICG?

Lea: the guy who posted the google proposal is now working with them.. so can't they consolidate and come back?

Dan: this is why we closed 609, because Dom said they're working together, but we got pushback. Agenda for next week?

Lea: Dom posted, suggesting closing 609..

Dan: jan ivar said they'll work on an explainer

Lea: pending external feedback?

Dan: might be yeah.. set it for a couple of weeks

#### [WebXR DOM Overlay Module](https://github.com/w3ctag/design-reviews/issues/470) - @hober, @torgo

#### [Realms API ECMAScript Proposal](https://github.com/w3ctag/design-reviews/issues/542) - @hober, @kenchris

#### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

[bumped]

#### [elevation of design principles](https://github.com/w3ctag/design-principles/issues/316)

Dan: the thing to do is to ask people to pay attention to design principles. Through references to ethical principles as an underpinning. Would be more impactful that way. Right approach is through design princpiles, which should have references back.

Lea: he's asking if it's mature enough to be included in charters

Dan: I think it is

Lea: I agree

Dan: the answer is we would encourage people to start looking at it and yes, include it in charters

Amy: +1

Dan: Sangwhan is the editor, Tess has put a lot of work in, we've all put work in, but I don't think there's anything controversial in what Chris is asking about, this is exactly why we've written it. We ask people to read it when they go for review, would be great if they read it before they started working on the thing.

Peter: minor concern is that if a charter says they will follow it and they have a really good reason to leave an exception and we didn't leave vague language in the doc to willfully violate these principles.. not worried that much, just a potential issue

Dan: it shouldn't say we will follow the design principles... say wherever possible we will adhere to..

Peter: text is proposed is to that effect. In general we leave escape hatches in the design principles, but we may not do that universally. Not overly concerned, just make sure we're not imposing strict rules on anybody 

Lea: ethical principles as well?

Peter: not at this point

Lea: we link to ethical from design

Dan: we're goign to have a separate discussion about that, we'll go through some process of elevating ethical principles to a w3c statement. At that point we can get a lot of feedback and discussions.

Peter: AB issue to incorporate it into the process at a higher level

Lea: [writes response]

Dan: we can close? Doesn't call for any change to our text

Peter: ethical is a fine line between architecture and policy. We can't make policy statements, but we can speak to ethics inherant in the architecture of the web.

Dan: that's the line we're trying to walk

Peter: fine for the AB to set policy

#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aopen+is%3Aissue+label%3A%22Progress%3A+untriaged%22)
