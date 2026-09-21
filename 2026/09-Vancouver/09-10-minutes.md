# TAG Minutes - 10 Sep 2026 - Vancouver F2F

Present: Yves, Christian, Marcos, Brian, Heather, Jeffrey, Sarven, Lola, Matthew

Guests (Web Install Finding): Alex Russell, Jeremy Keith

## Notes

### Web Install Finding

https://docs.google.com/presentation/d/1bb42RNaXoBENsziOlEH7RRaD58C64Y0bLyPrNYM-TxI/edit?slide=id.g3f9f9f28506_0_37#slide=id.g3f9f9f28506_0_37

Christian: Web Install is an area that can use unblocking, which is in the remit of the TAG. So, I suggest we talk about a finding. We have three people prepared to talk about this: Marcos (wearing his WebApp and Apple hat, not TAG), Alex, and Jeremy. For context, this is about installable web apps to a device. This has been around for a while. Depending on platform, this enables additional capabilities (e.g., push capabilities on iOS, setting a program as the one to open a particular file extension on Chromium). It is not obvious (to me) that users know they can install apps, nor do they seem to know how to do it. This is a point where the TAG could make a statement to improve the situation. Also under discussion are proposals to show the install prompt from within the website (e.g., an install button that would install its own app or a third-party app from within the websites viewport, controlled by the developer). This is stuck in the WG. Microsoft has proposals that were sent to the TAG. WebKit has negative positions on these proposals, Mozilla has not responded either way. Back to the install support on the web, it is possible to install web apps on all the platforms and browser engines. The way to do it varies per operating system & engine. Chrome and Firefox have an install button in the address bar on a desktop. On mobile operating systems, it's a bit different and not as intuitive across the major platforms. This is not great and a pain point for developers. With installation not obvious, the assertion is that this is why users aren't installing the web apps. So, developers are requesting a programmatic solution. Which leads to a recurring question: how can we do this? One proposal is to let web apps propose installation themselves (WebKit opposes, no feedback from Mozilla). Previous TAG feedback was that they were ok with same-origin installs, but not satisfied with cross-origin installs. Suggest that the TAG draft a finding on this specific architectural 
issue. We would answer three questions:
    
    * Declare web app installation as a core part of the paltform
    * expect that user agents make installations simple/obvious
    * the role of programmatic install APIs
    
Lola: Who would be the audience for this finding? Alex made a point in the chat that developers have asked for cross-origin installs. We would need to explain why we don't recommend that. Would that be in the scope of this finding?

Christian: It could be a fourth question, but suggest we focus on the first two points where the audience would be browser manufacturers.

Marcos: Any finding is a living document; it will evolve as new use cases and information are collected.

Marcos (representing WebKit, not TAG) : We question how this would impact the user's experience with the website. Prompting the user to 'install' a website makes it hard to tell whether they actually wanted to save the website for later use, or the user just wanted to pass through the prompts. Installation shouldn't gate features; that goes directly against the goal of differentiating websites that the user trusts. Users may just tap through from habit, so if a website is asking the user to save it on the home screen, that's less of a signal to the UA that the user had intentionall done. Browser UI is preferred over site-triggered behavior. If the user were to manually add it to the home screen via the browser, then that's more of a positive signal. Upfront permission requests are problematic because they may confuse the user with what they are actually getting/doing. So, the challenges are around what users actually want. UI is hard, and user education is needed. The developer/site incentives change when you give them an API. We also have a challenge with WebViews (e.g., Instagram). Two solutions are on the table: display-mode: application, or "installable" surface. These two things will solve at least part of the problems. 

Brian: I don't disagree, but am curious how you address the fact that the web is plagued with people being pushed to "use the app, there is a better experience there." So, the assertion that this would add an annoyance misses the point because it's already annoying.

Marcos: It's not whether it's a native app or not, we're talking about the experience with the web. The install is different from the overall capabilities of the platform.

Brian: So, if we had this, then there would still be the drive to use native apps?

Marcos: Yes.

Jeffrey: You mentioned that asking user's to install the website is an annoyance, so WebKit wouldn't want to have a banner. But there's already a banner asking user to install the native app. In a prospective finding, would you (as a TAG member) support us objecting to that?

Marcos: Yes. Safari is just one expression of WebKit. The interesting question is why the other browsers on iOS haven't changed their behavior.

Jeffrey: If other browsers use the share sheet to install, does it open Safari regardless of what browser it installed? 

Marcos: It's WebKit all the way down.

Jeffrey: Implenting features with OS integration is a choice. The native browser could accept push notifcations and forward them; it's not required by the OS.

Marcos: I potentially disagree. That might lead to an inconsistent experience. From a platform perspective, you do want integration at that point. Also, given the role of notifications, you want them integrated at that level.

Jeffrey: The UI on iOS, you have to click "Share" to install something. Does WebKit think that makes sense to users?

Marcos: Since WebKit is an engine, we don't have control over what other entities do. But I can see it's confusing.

Alex: I'm confused by the description that other browsers can access internals to configure the UI more than to promote without extra stuff around it the share sheet. The normal flow we would implement in Chromium is not available to us in WebKit. It's difficult to inform users what they're getting into, so we should steer clear to say that's where browsers can differ.

Marcos: That's fair game for a finding, "What's up with these limitations?"

Alex: I'll talk about the perspective of Chromium. In Chromium, we launched a version of installability in 2014, based on an implementation of service workers. This would provide developers for the option to provide for native or mobile applications. As part of that, we spent time thinking about the details. One was that you're likely not going to get this right the first time and will need to adapt. One thing that I think was a good choice was that when devs asked for a version of an API for onbeforeinstall. There is an event when the system has verified certain details. Anti-abuse is a strategic ambiguity; it allows more flexibility in changing what you verify. Think of it as an API that you can use to prevent a banner kicking off. The TAG review request from Edge is focused on cross-origin install. For example, a decorated link type. What we landed on is that a cross-origin install needs to be a different API. If the TAG is going to way in on this, it sounds like the interested is about same-origin. If that's the case, please see https://github.com/w3ctag/design-reviews/issues/1245. 

Jeremy: It's weird that I'm representing all web developers, but I think I'm fairly typical. Web developers would love a way to initiate to install a webapp. We just want to initiate the same flow that already gets initiated through the browser UI. That's what's being installed by the API. Most web developers don't care about cross-origin. They care about the user having the opportunity to install from that site, not another. I recognize the use case of a web app store, but that's not my biggest problem. I've used install prompt, and it's not useful. WebKit's position is totally understandable, but don't throw out the install API part because of the onbeforeinstall prompt API. I share the misgivings about gating features to install apps. It could encourage users to install apps to unlock more features. One reason I think some kind of install API would be helpful is that devs could stop spending time complaining to browser vendors for the difficult user experience. It's worth noting that Safari is going against WebKit by making install that much more complicated. It's a fine experience on desktop, but it's terrible on mobile. So, ideally, there would be an API for developers to use that would let a user click a button that would only initiate the action, not install the app. Worse case scenario is what we have on Safari on iOS, something that's buried 5 menus deep. The middle ground would be to say we're not going support the install API, but we'd make the UX reasonable in the browser. To address the question of user need and whether they even want this, users have been driven towards native apps for decade. There is no longer a technical reason for this. The reason the finger is so heavily on native apps is the gated features. A native app will have more access than the browser has. The browser sandbox that keeps things as secure and private as possible has worked, so it's actually in the best interest of the web to encourage whatever we need to make webapps easier.
 Whether that's an install API, or the UX for installing should be clear and sensible, that's up to the TAG.
 
#### General discussion

Marcos: I'd like to speak more on the notification side of things. From a user's perspective, notifications and phone usage are overwhelming. Similarly with badging things. Just allowing sites to opt in to notifications is highly disruptive and most users won't do that. Management of those notifications has to be carefully managed because it is a core part of the experience of using a device. When you do install a webapp, similar to a native app, some of these capabilities become available because they enhance the experience (hence the higher bar of getting the user to engage). Are we trying to route around the problem Safari is created with all the taps? Would we need the API if there was the better UX in the browser? 

Alex: Of course this (notification, badging) is something you'd have to deal with carefully. Those things are subject to abuse. Chromium has put in a lot of time to help mitigate that abuse. I want web and native to have an equal experience, and I want to put more control in the hands of the user while still protecting them from abuse. The interventions are only possible because the browsers are making them possible. If we're going to compete, or if we say we're not going to compete, it seems like we have nothing to talk about. The framing mechanism to say there difficult problems for users to understand when other browsers gate those important moments through other mechanisms seems nonsensical. We're going to keep on the path to improve these other mechanisms, so a finding might just be to encourage the continued exploration of those other mechanisms. This discussion frames a false problem. 

Jeffrey: Install shouldn't gate features, except for exceptional features, and we're going to disagree on what's exceptional. I don't know if that's worth putting in the finding other than to point out this isn't an absolute line. Also, the DMA in Europe says what Apple should allow other people to ship. What are the arguments for/against mentioning that? There are risks to us mentioning regulation.

Alex: For the affordance question. For the bookmark question, we have trained users to use them by putting them in the omni box. They are everywhere, in the same places in chromium browsers. That's been very effective to train users. If that's part of the TAG finding, I would support.

Marcos: We can go out to the developer community to ask them more about what they'd like in a finding. The enablement model may not fall in the scope of this. We have many things we could talk about to inform what's restricting UI innovation. 

Sarven: I'd like to hear more about the delta between the web extension work and web install. The direction the web ext group is going is that people will have to go through webstore to install an extension. If it's not signed, the browser won't do it. There are ways around it, but that takes effort. Now we have an alternative approach, a decentralized distribution of control. 

Alex: Extensions exist because the power they provide more cross-origin capabilities. Extensions can do what browsers cannot do natively. We're not talking about changing the origin model in web install. 

Jeremy: The main difference between installing a website vs extension is that you get super powers with extensions. But it's a great thing to bring up as they are both being used in the WebKit position. We have trained users to understand bookmarks, so we don't need an install API if we make it equally simple. But then, we also get concerns because the webapp gets more permissions once installed. Those two metaphors are mutually incompatable. Either installing a webapp is similar to bookmarking, OR it's more like a web extention that gives the super powers. 

#### TAG discussion

Lola: Regarding including regulation, I'm comfortable with that as long as we get legal advice as long as we confirm we are using the exact legal interpretation. Would we want to point to more than just the DMA?

Marcos: We should be careful with the inclusion of regulations. 

Heather: I'd rather put in the Finding, there's a reason the DMA has that, so use the logic that got them there, rather than pointing to any regulation at all.

Christian: Let's talk about next steps. Do we want to do a finding, and if yes, what's the scope? Personally, I think we should do it. It would be easier not to talk about the store use cases and instead focus on install as a core part and that the UI should be improved. We can think about the DMA.

Brian: What does it mean to say it's a core part of a platform?

Christian: Like we had the private browsing mode finding, we say there is a feature on the web platform implemented across platforms and OSs, and when you open them they take a different form.

Brian: But you could have a browser that doesn't support it at all, which is a choice.

Christian: Yes.

Heather: Specific question of whether the TAG should work on this: Yes. Should the scope be "install" and not necessarily "store"? Yes. I'm happy to help this happen.

Marcos: I think we should call it the cross-origin use case, not the store use case. For the 'declare' part, it's a valid point that some UAs may not be able to support this. But we can say the ability to integrate with the OS is core. Expecting UA to make it simple and obvious, I think that's important to say, but it is wading into UX. People may complain that the UX is bad, but if we go to the world's best UX designers, they may have very good reasons why they did what they did and we don't have insight into that. For the role of programmatic APIs, I presented the case of what the impacts are; I am convinced it changes the dynamics and motivations. So there are risks. Whether we go into the capability side, I'm unsure. That might be outside the scope.

Jeffrey: I am onboard with keeping cross-origin and DMA out of scope. The thing the DMA touches on is that the install should be independent of the browser; the result should stay within the browser. We should mention both of these principles. 

Christian: Would like to do this sooner rather than later; keeping the scope to what we think we can reach consensus on seems like a good idea. 

Marcos: I have some research that covers a decade that we should consider building on. See <https://w3c-webmob.github.io/installable-webapps/>

Brian: Does that document include statistics to determine how much people use stuff and what mechanism they use to get to it?

Marcos: We did do a bunch of research on that; I will look for it. 

Christian: Would anyone object to us writing a finding on WebInstall? <no objections>

### User agent finding, especially [web views](https://github.com/w3ctag/user-agents/issues/36#issuecomment-5331981342)

Marcos: Web views are the engine, and UAs make use of them. You build the UA using the web view. Not sure there's much left to discuss on the doc? Suggest we have a focused working session to see if we can wrap up the UA finding. 

Lola: suggest we work on this async or in a separate breakout.

### Retrospective for the week

What worked:
    * Dev meetup was useful; we should keep doing them
    * We've been decisive on several topics
    * Venue is good
    * More hands-on than the last one, so we got a lot done
    * The discussions around web vs web platform and the breakout discussions
    * Good having invited people come to speak about hard topics, particularly having a representative from developers and not just other standards people
    * That we could discuss as a group some of our bigger issues. That helped raise understanding of some issues.
    * Feel more a part of the group thanks to the personal interactions
    * We did better separating individual positions from employer positions, which was as much other members figuring out how to ask questions as it was individuals modifying their behavior
    * Remote participation worked fairly well. Sound issues were handled quickly and timezones weren't as bad as expected. Onsite did a good job at being inclusive of remote participants.
    * Happy with the composition of the group.

What didn't:
    * Not all sessions were well-planned by the presenters; not sure if that was because the chair wasn't clear or if people didn't look at what was assigned in advance
    * Guests said they felt unprepared; we should have done more making them comfortable
    * In the doc sessions, it wasn't clear what one thing to focus on when many docs are assigned
    * We missed there was a public holiday our first day which complicated venues
    * We missed the mark with high-bandwidth interaction because the number of people not available on-site
    * We couldn't split into small groups and come back to the whole group; onsite wasn't enough people and the timezone split was hard.
    * Need to do better about avoiding speaking over people. Mind the queue and remember it's a conversation with the whole group.
    * Not enough time to break out and do things. Would like a whole day to breakout into groups and work on stuff. Even if we're in separate time zones, we can make effective use of whatever our "day" is.
    * It's an ongoing problem that people have to participate remotely. We need to lobby for funding.
    * We didn't find an opportunity to include the associates. We didn't do enough to let them know they were welcome to join.
    * A/V struggles delayed our start several days.
    * TAG still feels too elite; we're too separate from what the average user is experiencing on the web. Can we hear more from digital literacy organizations that have more hands' on experience of end users and what they are struggling with on the web? 
    * Because we didn't have as many projects, we didn't triage the agenda like we usually do.
    * We need more user research. Is there a role for the TAG to provide leadership by getting people to focus on this problem? The W3C would be a good home for this work. Remember that there is a group, WebDX, in the W3C that is doing this for developers (but not end users). There is a lot of burden on groups like Accessibility to respond to the requests that require user research. Engineers often overlook the importance of understanding the needs of users, despite the fact that users are at the top of the constituency lift. The TAG could encourage sharing information about their own studies, because sometimes they are done in the process of designing things, but there is very little shared about that R&D
    * We opened the issue for f2f planning early, but it still didn't help. Not sure what to do about that. 
    * Need to divide notes duty more equitably 
    * We need to focus more on closing things. We get easily scattered and focused on status updates rather than doing and closing stuff. People to do more to take advantage of using the agenda+ tag for plenary and breakouts to let the chairs know. 
    * We forget to write down what are our next steps.

### New Plenary & meeting times

Lola: we change our times twice a year when clocks change in the northern hemisphere. Please fill out the markdown file (link in TAG slack)

### Next F2F

Lola: Locations on the table are Switzerland (Zurich, potentially hosted by Google), Spain (hosted by Igalia), or Germany as a fallback.

Heather: I'm open to locations, but I'll be on the other side of the IDL from Feb 22-March 13.

Jeffrey: Suggest after March 13 so we can get give new members time to schedule. 

Yves: Reminder that currency conversions makes Switzerland more expensive. 

Lola: Let's make a decision at our next plenary (22 September), and consensus for Germany in March.

Heather: Date suggestion - March 16-19, 2027.

### TPAC Planning

Matthew: I will run the tool to figure out working group sessions. 

Lola: We have our TAG meetings being handled by the team. 

Jeffrey: we need to start preparing for TPAC. 

Matthew: 
    
Jeffrey: we started with a repo that was private first for issues, but we didn't end up making use of it that much, so I suggest we just use a public repository to track issues. 

Heather: I see. There are significant issues. 

Jeffrey: yes, there's one issue per meeting. We were concerened about our issue comments might be misconstrued so we thought about making them private. But I think this time we can just make it public. I'm going to go ahead and make it public. 

Jeffrey: Mathew you can go ahead and run your tool over that. 

Matthew: as we file issue the tool will pick on on the issue. The tool will let us say that we want to attend part of a meeting, but it does provide flexibility for particular parts of a WG meeting. So it deos work with some flexibility. 

Jeffrey: Please post it to slack and we can set up github actions to get it all going. 

Lola: I was going to ask if Mathew can do a walkthrough of the tool. 

Mathew: sure, I can do that. There's a couple of things that it does. I'll start by showing some example images of what it does. The first things is that it gives you a grid layout of all the meetings... so you can see everything at a glance. The second thing is a group timetabling, so as a "group" (can be any set of people), it let's you see what/when you are doing something on a particular day. So I do one of those for everyone in the group. So what you do is file issues, and you assign yourself to an issue and that makes the semantic link between yourself and meeting that is happening. Multiple people can assign themselves to an issue. So please assign yourself to issues. We can go through this synchronously. Be mindful of what you put into the issue because the first line shows up in the grid, so put in useful things there that will help people at a glance. We can run when new issues are added and on a temporal basis as often as we need... more so closer to TPAC to make sure it stays in sync. Questions? 

Lola: so the purpose of this is for us TAG to coordinate... do we also want to norminate which things we might be at regardless of TAG participation or not? 

Matthew: that's a great question. Last year I had to be at multiple groups... the tool can look at multiple repos. Maybe we can use a label to indicate that a tag member is there at a personal capacity instead of representing the TAG. 

Lola: I wonder if we should decide on that (labels) sooner rather than later. 

Heather: it would make sense to do that above, 

Jeffery: I agree... 

Heather: but I'll be there, for example, as Chair of a WG.

Jeffrey: right, but when we are stretched and we can't get someone there it could help. 

Matthew: I can expose something to make the differentiation via the label. As long as we use the same thing

Jeffrey: Lola suggestion "personal capacity"

Matthew: that sounds good. 

Jeffrey: anyone else have questions about how the tool works? 

Heather: I'd like to see more how it works? 

Yves: what happens if you realize you can't attend something?

Jeffrey: you can unassign youself

Matthew: correct. But please leave a comment so you don't get re-assigned to the issue by the chairs, for example. Let me show you how it works by assigning myself to one... <Matthew shows how to use the tool... drop down.. .clicking... double clicking... computers... repos... assigned myself ... "personal capacity"....> so now that will appear in the tool... so now you see it in the tool. Assigning ourselves should be daoble async and folks can do this on their own or at the next planary

Jeffrey: last year we finalized everything the week before. We also asked chairs to invite us to their working groups if they want us there. So WG chairs can file issues and we (the TAG) can assign people. 

Jeffrey: I think that's it for today for this sessions... we can now break out into seperate sessions. 

Lola: it would be good after you all work on stuff to report on what you've done. 

Jeffrey, Mathew, Lola,  etc.... safe flights and thanks everyone! All the best!
 