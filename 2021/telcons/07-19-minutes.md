# TAG Minutes Doc

## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/07-19-agenda.md).

### Breakout A (Europe / US) - [2021-07-19](https://www.timeanddate.com/worldclock/converter.html?iso=20210719T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Main topic:

* [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - with special guest Mike West

If we have tine:

* [Trust Token API](https://github.com/w3ctag/design-reviews/issues/414) - @hober, @torgo, @hadleybeeman, @plinss
* [User-Agent Client Hints & UA Reduction](https://github.com/w3ctag/design-reviews/issues/640) - @hober, @torgo
* ["credentialless" embedder policy.](https://github.com/w3ctag/design-reviews/issues/582) - @ylafon

### Breakout B (US / APAC) - [2021-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20210720T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober
* [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov

### Breakout C (APAC / Europe) - [2021-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20210720T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov
* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris
* [private networks](https://github.com/w3ctag/design-reviews/issues/572)

### Plenary Session - [2021-07-21](https://www.timeanddate.com/worldclock/converter.html?iso=20210721T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov
* [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @kenchris, @hadleybeeman, @atanassov

* Breakout Rollup
* Issue Triage

## Call Minutes

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/07-19-agenda.md).

### Breakout A (Europe / US) - [2021-07-19](https://www.timeanddate.com/worldclock/converter.html?iso=20210719T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Amy, Tess, Peter, Rossen, Hadley, Mike West, Anne, Yves, Lea

Main topic:

#### [COOP same-origin-allow-popups-plus-coep](https://github.com/w3ctag/design-reviews/issues/649) - with special guest Mike West

Dan: we were reviewing this, looking at user needs and trying to understand how this could weaken the current security guarantees of the overall browser. That lead us to this discussion

Tess: a lot of relevant conversation in the WHATWG

Mike: it seems like cross origin isolation is an important primitive that security teams in different browsers are trying to push on. The conversation in this review as well as others seemed like there were some questions popping up about what it is that's going on more generally. Less about specifics, but the world in which this proposal lives. I wanted to give you a two minute overview of what I think about this stuff. I'd love for Anne to jump in. Then maybe we can dive into specifics of one or more proposals. Sketching out the broad story would be interesting. A couple of different docs to get started:

* https://w3c.github.io/webappsec-post-spectre-webdev/ - tries to summarise a couple of documents
* https://arturjanc.com/coi-threat-model.pdf - does a fantastic job of going into detail about what this is and why
* https://resourcepolicy.fyi/

Mike: we want to align the origin model on the web with the process model in hardware. Computers are broken. Cross origin isolation is a set of compromises that allows developers to opt into a subset of the status quo web that enables us to isolate origins from each other more deeper than we can normally. We have a number of ways origins can reach into each other from a site. \*.example.com can become same origin with other \*.example.com pages through eg. document.domain. We have to keep the process isolation at the site level not the origin level. It's important to keep thing sprocess isolated because everything that comes in can be read by an attacker. We had a variety of mechanisms that allowed the browser to enforce explicit legibility of resources. If I can get the result into my process with spectre attacks I can read those bits. 

...With that in mind, we know the process boundary is the only one that counts for this set of attacks. Given that, the cross origin isolation proposals are really wrapped up in not solving the problem of legibility, not possible, but ensuring data only enters your process if it has chasen to do so. You can make requests to cross origins ites, eg img or iframe, those responses will only be allowed to enter your process if they opt into do so with the cross origin resource policy header, or more with iframes. 

...The work that is shipping today in firefox and chrome is wrapped up in two primitives. Cross origin opener policy and cross origin embedder policy. Today they are quite strict in what they allow. In order to be considered cross origin isolationed and get access to eg. shared array buffer you must opt into the same origin cross origin openeer policy. This breaks the opener relationship with any window that navigates to a cross origin page.

Dan: opt in how?

Mike: you opt in by sending a cross origin opener policy header with your document. As the attacker in order to get access.. cross origin isolation wer'e using as a gate for things we know make attacks more effective. sharedarraybuffer can increase the bandwidth of spectre attacks. It's possible to execute spectre attacks without it, but its a lot slower. By limiting your access to high resolution timers we meaningfully affect the ability of the attacker to get data. The attacker wants to be cross origin isolated for a good attack surface. They have to opt into an opener policy of same origin, which breaks oopener relationships, which allows us to process isolate the window. Some browsers can do it by default some need the heuristic that cross origin windows can live in a separate process. that has the impact of any cross origin navigation is going to break the relationship. Has impact with oauth flows and popups, payment providers, and other things that folks have found when doing things. 

...The other thing you have to opt into is the embedder policy - require-corp. This has the effect of ensuring that you can only load resources that epxplicitly opt into being loaded by you or something that looks like you. If attacker.com makes a no cors request to bank.com using a script or image tag, the request goes out and if it doesn't come back explicitly labelled with a cor policy of cross origin you don't get access to that thing, it's blocked. The server is opting in to allowing their resources to be loaded in cross origin contexts. The only things loaded in cross origin contexts are the set of resources the server has chosen to make available to third parties.

... The combination of these two we think is robust. Gives us the ability to provide devs with powerful tools without being able to attack the rest of the web. At the same time - a number of constraints. Feedback from devs is they're having problems deploying apps in a cross origin isolationed mode. It's unfortunate .We want apps to be cross origin isolationed.  Opting into cross origin isolation model allows us to move from site based to origin based isolation. Domains with lots of applications at different subdomains. Google is an example. 

...It would be excellent if they could remain separated at the process level so a bug in one doens't turn into a bug in the other. With site isolation it's a single site based process. So we need to shift to cross origin isolated. Difficult for apps because of restrictions - popups are a problem for a number of work flows. Subresources and subframes are a problem. Apps like google earth that have user generated content from millions of years of internet history and its infeasible to imagine that they'll go back trhough and ensure third party servers referenced are going to be updated. Quite unlikely. 

...Two proposals for today are about ways in which we think we can change the reqs in a way that don't weaken security but increase developers ability to deploy these. The first is the opener policy mentioned at the beginning. The second is the credentiallless cross origin embedder policy. One other thing in the future is a proposal for anonymous iframes. 


...Taken together we hope thse mechanisms will give us the ability to more broadly deploy cross origin isolation in order to put users into a world where they have better guarantees about the ways their data might be accessed. Today it's difficult for devs to do that work.

Rossen: about having a difficult time moving some legacy.. what is the solution going forward?

Mike: the solutions right now are ways in which we can create isolation without requiring an opt in. On one hand the opener policy today is the opened window doesn't need to opt into being spoken to. We'd be able to open it and the behavioural changes in that proposal make it possible to maintain process isolation while doing so. The embedder policy change makes it so i fyou don't send credentials with the request the resulting data is somtehing the attacker could have got anyway so it's not necessary to explicitly require an opt in. Anon iframes is similar - it aims to break the credentialled relationship between the frame and the origin to which it lives by separating it out and not sending credentials with the initial request.

Hadley: you are talking about as a user when I am doing something on a page that is going to open another page, you want to restrict both ends of that journey into the same process, to be treated as one isolated security unit?

Mike: the opposite of that. I want to ensure that the application and its cross origin dependencies can remain in distinct processes. If I"m on twitter.com and twitter wants to run a SSO flow with some other entity, that those distinct entities need to live in separate processes, it's critical that they're protected by a process boundary

Hadley: and then same concept separating two entities by process bounddary for resources embedded in the page, to keep the iframe separate?

MIke: i would distinguish iframes and other subresources. irames create their own environment that is a separate origin from its embedding page. We do want that to be in a distinct process, we can't always guarantee it. Chrome on android for instance, often the case that we don't have more processes to give. In those cases today we want to ensure the frame is explicitly opting in to live in that kind of environment. Today we do it with a cross origin resource policy and embedder policy. The anon iframes proposal is another path to getting there, but that's distinct from subresources. Today subresources need to opt into being loaded. If I grab an image from a server I"m goign to process that in the rendererer, and I might found out it's not an image, it's data. Reading it gives the attacker access. I need to block before I can read it. Looking for an a priori assertion about the resource before we parse it. Look at headers, if its opted in it can be loaded.

... example.com is loading an image from cdn.net. cdn.net needs to say my resources are loadable by third parties, that's my reason for existance, I expect them to be loaded by someone other than me. We're asking them to explicitly assert that by sending a header that says that. 

... If i am an attacker and I want access to very high resolution timers i have to opt into a mode that only allows me to load resources that have done that opt in. cdn.com is fine, it's going to assert this for all of its resources. but bank.com isn't going to make that - they don't know, or they don't want their resources to be loaded by others.

Dan: root assumption that is driving this is it's about minimisation. It's minimising the surface area of attack by minimising the number of times that access to the sharedarraybuffer can happen?

Mike: I suppose minimisation is a reasonable frame. We want to provide certain capabilities only in a framework that allows us to provide them as safely as possible. W eset up a number of restrictions that we think made this thing safe and ask the developer to opt in to those restrictions before we give it to them.

Anne: same origin policy has a number of holes that make spectre attacks feasible. img doesnt enforce the same origin policy, you can load images from anywhere. You oculd point the image element to a bank statement and it would fetch it into your process, end up in the incorrect process and it oculd be spectre read. Cross origin isolation idea is that we have a set of headers that patch these known problems in thes ame origin policy by requiring everyone to consent to being in that process. If everyone consents to being in that process it no longer has the flaws of the same origin policy so we can give it certain capabilities.

Dan: you're not consenting for a specific other origin? Just I consent to be cross loaded?

Hadley: we're assuming that the bank statement exmaple, the bank is never going to want to serve my bank statement in another origin?

Anne: yes

Hadley: do we feel comfortable about that?

Rossen: goes back to questions around banks that are not moving as fast. Or the google earth user content, you can't move it to adopt the new embedder policy

Mike: my claim is twofold. First, the resources of that slow moving bank are protected by default. As soon as the attacker opts into a set of restrictions they can now no longer load things from that bank, because they haven't opted in

Anne: what if the bank wants to have cross origin isolation and also wants to embed resources from a cdn? we haven't really encountered that thus far. But they could load the resources via CORS. The cross origin embedder policy only applies to non-cors resources. cors are already consent. it's about no cors loads. You can do cors loads for images with crossorigin attribute. If a bank wants to do that they can use cors.

Dan: what happens when an ads/marketing/analytics agency says to the banks or whoever: in order ot make our analytics work please add this header to this http configuration. Maybe that wouldn't make sense for banks because they generally hav ea robust security department that looks at that, but thinking about this in the context of where we've been talking about advertising mechanisms and trackers and how there's a lot of pattenrns emerging of ad networks that compel third parties to make config changes or add cnames.. whereas that might not be something that's really understood to the party, but they're compelled to do it becuase they want to participate in this other thing

Anne: already hard to avoid.. these providers often say just include a script tag.. by that point they have all yoru data and your storage

Rossen: would weakening of that policy open it to tohers besides the analytics company. In the example hadley was pointing out, if that page includes that policy to be read by a third party, does that mean that now you're also weakening it for other third parties and not just yourself?

Mike: I don't feel like I understand what data is being leaked. If I'm an advertiser, with complete power over you and tell you to do a thing. I think the thing yo'ure suggesting is I'd tell you to cross origin isolate your site and send an opener policy and an embedder policy? that sounds good. Higher restriction. Opener policy and embedder policy are restrictive by nature

Anne: the host has a trusted third party and an untrusted third party, and the trusted one forces these headers and the host doesn't realise the implications of doing that

Rossen/Dan/Hadley: yes

Mike: if you include script from someone who is going to do bad things on your page you're going to have a bad day, regardless of cross origin isolation. If someone has script execution on your page they are you

Anne: they might be in a sandboxed iframe but because of resource limitations the host, trusted party and untrusted party all end up in the same process with access to sharedarraybuffer. I don't think it's in firefox yet ubt we did add permissions policy restrictions on shared array buffer access. The third parties wouldn't necessarily have accesso to higher resolution timers, mitigates to this to some extent

Mike: the cross origin isolated needs to be expicitly delegated to iframes via the allow attirbute. Shipping in chrome. Attacker would be able to without hosts permission take action would be if they had script access at the top level. In that case they don't need the allow attribute.

Dan: User needs - it always comes back to payment flows or oauth type flows. Is the use of sharedarraybuffer with these types of flows so compelling? Why is it not possible to do these flows without something as powerful as sharedarraybuffer?

Mike: sharedarraybuffer might or might not be necessary for the thin in the popup. Seperable from the application. One thing is that the paplication is what the user actually cares about. I go to a webpage because it does cool/useful things. I want them to work. If that application has a third party dependency of some sort, a sign in flow that gates my access, whether it's a payment flow, that's part of the applications flow regardless of whether that piece needs sharedarraybuffer or not. You could imagine applications that shunt useres off to a seprate page that is deprivileged. They take you out of the application, put you on a special page that didn't opt into to cross origin isolations, kick off sign in flow, then take you back. That could work but is disruptive for the application. Need to take the user out of what they're doing and no longer have a sign in form on every page or a donate button on every page. That' sthe kind of friction that we're talking about. It's user facing insofar as th euser expects the application to work and do the kinds of things the application wants ot do in a low friction way.

Dan: that really captures what I was looking for for user needs. Makes sense.

Hadley: helps. I'd love to broaden it. In the use cases, what's on the list that isn't payment or login?

Mike: those are the easiest. The others are stuff that pops up in enterprise. Salesforce applications talking to other parts of their infrastructure. A weird thing broke iwth a printer that has a service in a popup. Salesforce integration with this printer, sends information, bidirectional communication, printer is not going to be updated any time soon. Long tail, but is going to be the case that the general assumptino on the web to now if I pop open a window I can talk to that window and that window can talk to me. people build flows around that. Payments and identity are the flows most people will come into contact with most often. I think there is more out there that we discover as we get people to roll this stuff out.

Hadley: helpful, thanks. I can imagine other longtail stuff with other hardware.

Mike: one thing about printers is they  usually live on local networks. Credentiallless - private network access is one of the plaes where that is not good enough. Todya it's the case that you can make requests from the internet to the intranet and to localhost and we want to change that. There is a proposal for private network acces,s used to be [cors-rfc1918](https://github.com/w3ctag/design-reviews/issues/572). When you're thinking about credentiallless I"d ask you also thinks about risks associated witih private networks. If we remove necessity of server to opt in, the attacker can continue to access things that live on local networks until such time as we can get private network access rolled out which does create an affirmative opt in requeriment using a cors like framework for all pages all the time.

Hadley; helpful, makes sense

Tess: lots of discussion in [whatwg issue 6364](). Anne, do you think we've surfaced enough of that? COuld you help us understand the remaining disagreement?

Anne: out of privacycg wokr we know that popups are bad for privacy. Most browser that have various privacy protections, popups end up being an escape hatch. I'm not sure happy with continuing catering to the popups use case, since I don't think we want to have popups around in the long term. I can undersatnd the argument for doing it, but wonder if we should hold off.

Tess: a common use case for popups today is oauth flows and authn stuff. I suppose there's also the webid work that's happening to maybe deprecate that kind of thing and replace it with a browser mediated thing. Is that how we might make popups go away?

Anne: login or oauth type flows are the primary use case. The federated auth ..

Dan: brings the question of how much work should the web do to accommodate this case, if we think popups in general we want to see go away in the medium to long term?

Tess: adding features to the web is .. the web is additive, it's very hard to undo, to stop shipping things. Do we want to permanently add this level of complexity for a class of feature we want to go away in the long run?

Mike: this version of cross origin opener policy is likely we'd be able to deploy by default. The current mechanism for opting in, we have two cross origin opene rpolicies - same-origin and same-origin-allow-popup. The forme rallows cross origin isolation and is iimpossible to deploy by defautl today - breaks flows that exist. We are past the point of developrs depending on popups exisitng. Correct to remove things from the web is hard. If we want to get rid of popups my bold assertion is that this is not going to be the straw that breaks the camesl back.. camel is already in a bad state. To get rid of popups, webid and web payments are good to push on, but take a while to get close to the long tail of sites. We want mechanisms we can roll out quickly to get security benefits for a set of websites that are unable to shift off their current worflows. We can all agree how bad popups are, but sites depend on them for things today. If we give them a choice between origin isolation or their users signing in, they're not going to pick origin isolation. and lose the thing that makes them valuable in the first place.

Dan: mentioned privacy network access, our issue 572. And crednetialless embedder policy. Any topics in those issues we can bring to the table?

Rossen: any of the two documents you posted earlier a good framing that stitches all of the different proposals in flight that we could see as a timeline and dependencies? And what is necessary and critical and what are things at risk?

Mike: artur's threat model doc is a good read and give syou the conceptual framework within which we've been working. I don't think there's a doc with a timeline and dependenceis. My view is there are in both firefox and chrome coop and coep are shipping today. Firefox is gating sharedarraybuffer behind cross origin isolation. Chrome will probably be shipping that tomorrow. That creates a status quo with multi browserimplementation with the core of cross origin silation, agreement to limit known timers behind that.. sharedarraybuffer is only available in origin isolated environments. performance.now is .. 100mil and 5ms depending on if you're in cross origin isolation or not. Large differenc in granulaity. APIs we want locked behind cross origin isolation - memory measurement api and others. We epxect it to be a primitive used mor erather than less going forward. Question in my mind is how we get more people to shift into this world that llows us to isolate origns itno processes. Turns into a deployment question. Feedback has been around these popups on one hand, and subresources on the other. Proposals on y'all's plates are response to developers wanting to deploy these things in the wild.

Rossen: thanks

Dan: Feedback you'v ehad from developers and developer research in general. Is there developer research which you can surface as part of the public information? x developers are using this api in this way or we saw this much potential fraud which could be mitigated if this were in place

Mike: wrt to data I can point you to mitigation.supply/#isolation .. not super useful for specifics, but give you a wide story. Some big sites have started using it, so the useage numbers are starting to go up. Also the anecdotes that have popped up on variosu review threads. This one or the threat against html (?) - examples from google earth, twitter, zoom, docs - an addon mechanism for companies all using third party stuff has been a problem.

Dan: the other thing to mention is complexity.. something we often find ourselves talking about. Is it worth it to add xyz feature when it is increasing complexity. And anonymouse iframes have been discussed - a lot of proposals about variation son iframe - feels like a layering issue, need to get people to talk to each other and think how they can be built in a more layered way.

MIke: agree, the things we're proposing turn out to be complicated. THe model is mor ethan i want most people to think about most of the time. It is complicated, there's a lot of interaction between pages and resources. We've talked in various forums about the things we should be aiming for and the kind of direction we might be able to push in that could simplify things. Presentation I gave around what it would take to shift toward a model of isolation by default. 

...The [proposals](https://speakerdeck.com/mikewest/isolation-by-default?slide=5) are the building blocks I think we might start being able to turn on by default, such tha twe don't ask devs to think about them unless they need the weird stuff. If they need the weird stuff we can ask them to deal with complexity. Problem today is introducing it to a status quo we don't like and creating changes to the status quo. My hope is we can work toward inverting that picture so the complicated things are the status quo, and the complication come swhen you want to opt into something different than that status quo. I hope.

Yves: question about service worker - using credential mode could be used as a cache key? To mimic the fact there are differences between what's cacheable at public and private level. Anonymous or using the authn information. If it's part of the cache key then you might have a way to solve th eissue for service worker as well

Mike: yes I think it would be reasonable for us ot use the crednetialled state of a request as part of it's cache key. Probalby necessary. Service workers ar ea problem for privacy related proposals. We need to find ways to partian service workers. Similar to safari maybe or other options. Seems likely we'll need to do something.

Hadley: this was really helpful, thank you. I'd like time to read through the docs you sent and wrap my head around the specifics.

Amy: +1

Dan: worth us tying the three issues together

Rossen: how much is shipping?

Mike: core of coop and coep are shipping today in firefox and chrome. Credentialless is going to origin trial in chrome 93, a couple of weeks, through 96, and look at developer feedback which we can share. Anon iframes as well as cross origin opener policy proposal we hope to implement in Q3. Expect implementations behind a flag at the end of a quarter. Origin trial then would be nice.

Rossen: stacking up most to be ready by Q4?

Mike: these are blocking some sites from using cross origin islation. My teams are doing implementation to make sure they're solving the problem. Love feedback into whether this fits in the way the platform works. Not shipping tomorrow, working on it now, expect we'll have it behind a flag in two or three months

Anne: timeline for changing defaults? that's the most interesting aspect

Mike: agree. Not where we've been putting our time. We're getting back tot he resource I started at the end of lats year around document.domain. A few sites using it widely. Hope to start reaching out sometime soon. But haven't yet. Deprecations and behavioural changes are the important thing. Looking at opt ins first then opt outs, and path from one to the other. But we need opt ins done in order to have something to opt out of.


### Breakout B (US / APAC) - [2021-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20210720T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### [scheduler.postTask()](https://github.com/w3ctag/design-reviews/issues/647) - @hober
#### [Cookies Having Independent Partitioned State (CHIPS)](https://github.com/w3ctag/design-reviews/issues/654) - @hober, @torgo, @atanassov


### Breakout C (APAC / Europe) - [2021-07-20](https://www.timeanddate.com/worldclock/converter.html?iso=20210720T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Yves, Hadley
Regrets: Amy, Lea


#### Process Isolation / breakout A

Yves: he talked about changing the defaults on the platform towards more isolation.  How can people remediate... etc... 

Dan: do you think we should support changing the defaults?

Yves: will people be forced to use recipes to allow access... the default will be ... better to break more thanings and force people to opt in...? Have to check the issues we have...

Hadley: I like the concept - i think it sounds sensible. I'm concerned about knock-on effects. e.g. the bank example - what if the bank does want to be able to surface the PDF of my statement ina  different origin - the question seemed a surprise. hesitant about making a substantial change without thorough user research.

Yves: might be able to send somee secure document to a government website ... possibility to export to certai sites and not all of them - currently it's only "Ok cross origin" and "not OK cross origin" - no finer grain than that.

Dan: I'm concerned about complexity - but also in terms of server config... it means once again we have 2 webs - the web for the big players who can afford the complexity and the less secure small web for those who can't. 

...If I'm a fintech startup and don't have the resources of a big bank, i will be more of a target for this kind of processor-level attack.

Hadley: i was thinking about what will be updated and what won't be - you can bias search results according to that - or UX in the browser of what's safe and not safe. But we did tell the web in the evergreen finding that they've got to stay up to date.  That's not necesarilly complexity - it's staying up to date. 

Dan: yes. I guess evergreen web also applies to the server.

Yves: you already have this issue for web using SSL - all the servers using TLS 1.0 and 1.1 mostly unreachable now.  Deprecated older versions of TLS.

Hadley: it biases towards those with money.

Yves: or possibility of knowing how to upgrade things. In many cases people are using pre-made [configs].

Yves: what I heard from Mike was quite positive - they're doing an origin trial and seeing how things break. They care about not breaking things.

Yves: isolation by default or isolation by opt in.

Hadley: going straight to default too big of a disruption. so if you start with an opt in and heavily bias users and servers towards it - then you end up effectively creating the default.

Dan: question is - do we need to be more aggresive?

#### [private networks](https://github.com/w3ctag/design-reviews/issues/572)

Yves: a bit wary. understand the cocnern about use of older hardware but why not us a proxy of some kind?

#### [Performance Timeline](https://github.com/w3ctag/design-reviews/issues/644) - @cynthia, @kenchris, @atanassov

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @kenchris

Dan: I will pink Mike about this one - since we had a related security question on access to camera as an exploit...


### Plenary Session - [2021-07-21](https://www.timeanddate.com/worldclock/converter.html?iso=20210721T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)


Present: Dan, Peter, Yves, Lea, Tess, Rossen, Hadley, Amy

Regrets: Sangwhan

#### Further Discussion of origin isolation

Dan: what kind of feedback can we give?

Rossen: lgtm and good luck?

Rossen: I do agree about the defaults - how do we being legacy content safely in a way that continues to prvide functionaloty they want to provide. How do we make sure it doesn't [do damage].  Some of the discussions in blink-dev and chrome dev... didn't find concrete answers.  Didn't find exact place...  to bring old content ..   It would be a good sumarry to have...

Hadley: my thoughts - I feel like this is potentially very disruptive - not a bad thing and with the evergreen web finding we've said you need to be continuing evolving... i laid out what I saw as an evolutionary path - starting with opt in and heavily bias users and servers towards it...  then you can end up with it being essentially the default. Like the SSL->TLS journey. Getting an indicator that the site is not safe...

Rossen: that also taught terrible behaviours - because of confusion on certificates.

Hadley: we're imagining a roll-out path. I don't remember Mike talk about the long term path. One of our bits of feedback could be to ask.

Dan: relating to the complexity issue - can we encourage them to document this stuff in a very non-security-expert-web-developer-friendly way? e.g. an MDN page that really breaks it down. otherwise it will just be magic. 


Hadley: Popups, anonymous iframes, credentialless embedder policy

Dan: and local networks... I think that's different, it's a different time frame with other dependencies on it.. but for the three above we can do this

#### [HTMLMediaElement controlsList](https://github.com/w3ctag/design-reviews/issues/643) - @hober, @LeaVerou, @atanassov

Lea: peter asked them a question but we didn't get a response.. FWIW my opinion is - custom controls almost always on wrong side of history.. customization - as browsers add more native controls it's reasonable to not want to have some things customizable - doesn't necesarilly mean that it's user-hostile.

Rossen: i can see a lot of cases - scenarios.. taking surveys - coursework, you don't want people to skip ahead .. i can see these as valid use cases... if they didn't list those use cases that's a miss on their behalf..  not advocating for this feature or against it - can see this being applied and used on edu...

Lea: the students use case - they can circumvent by running code in the console... 

Rossen: yes but.... that's only for people who can use the console...

Lea: it only takes one student figureing it out...

Dan: +1

Lea: not the major use case - with the current design that's not possible. Right now it only enables disabling specific controls - but it could be extended.... Bigger philosophical issiue at play - 2 different philosophies - this behaviour could be user hostile but if we don't allow it we could end up with much more hostile results. 

Dan: what's the user hostility and what's the more hostile?

Peter: user hostility - diabling the ability to cast the video to an external device - ally issue here, I may not be able to see detail in the video on a mobile device. why can't i do that just because the author didn't like the look of those controls?

Tess: that's an argument for 2 things - allow people to implemet casting in their controls also.. also the youtube use case, no download

Peter: that's also user hostile

tess: weird that chrome has a no download feature but doesn't use it to remove the rightclick menu item

Lea: apparently feedback was authors didn't like how prominent the download button was but didn't mind it was present in the context menu

Tess: sounds like UI feedback, doesn't sound like a reaseon to add a feature to make controls mor euser hostile

Peter: I get the look and feel thing, that the app designer wants, but not to disable functionality. For that we need better tools to change look and feel. Could be abused to hide controls too, but..

Tess: separately there's an issue of how stylable should the default controls be? I think that should be a separate question but they're inextricably linked. Sometimes the only reason people resort to make thier own controls is theming. They'd be happy if they had lmited stylability of detaults - changing colours. Seems like adding ability to do some limited customisability is probably a good thing. but how do you do that without display: none or visibility: hidden?

Lea: I don't think it's always user hostile to hide controls. Add browsers add mor econtrols to native interface it's reasonable to limit how many are shown all at once

Tess: up to browse,r not the site

Lea: how does browser decide what's relevant?

Tess: look at things like size of display. If it's really small only show pause/play, etc.. user agent has the relevant context to choose what to display and not. in this context the esite is  the antagonist relative to the user need

Lea: website is part of the context.. UA has no access to that

Tess: Sure. Cases where format negotiation.. conneg.. you have a video element with a bunch of source elements that are different formats and the UA might have a more granular understanding of what formats are supported than the site can. UA might know that it's currently on battery power and knows that software decoders are battery intensive so it could intentionally not choose formats it knows it support sbecuase it wants the one that gets the hardware decoder to preserve battery life over whatever the site would prefer gets loaded. The ua has a lot of context that the webpage does not. Webpage knows things the browser does not - eg. which video it would prefer to load - sometimes the ua does things the site doesn't want and that's okay

Lea: allowing authors to remove certain controls does not remove the ability of the ua to customise the default interface. ua could still change how default controls are displayed

Tess: if this controls list thing is spsecified as a hint that the ua can freely ignore i think even in that case we run the risk of sites that use the feature blocking browsers that dont respect the hint

lea: what if it's undetectable whether the browser detects the hint?

Tess: Ua sniffing. If some browser, say safari, decides to never respect the no download value of the controlslist, what you get is sites blocking safari for video playback - :(

Dan: what are the further harms? to not having this feature?

Lea: it pushes authors towards  having custom controls which is much worse than any of the alternatives. Pushes browsers to not add a download button or other user friendly capabilities if authors don't want it and have no way to remove it

Tess: agree, there is a tension. I think there are plenty of user hostile things possible for websites to do. Ideally the friction of the platform shoudl be user friendly things are easy and user hostile things are hard. If we can't make it impossible we can at least make it hard. It is harder to make custom controls

Lea: only fractionally harder - including a library

Tess: library is more likely to have implemented custom controls correctly in terms of accessibility. Less user harm than without a library. That fits my gradient of difficulty.

Peter: I'd like to know this was part of their discussion. I'd like to hear what was talked about. I think there's a bigger picture here. 

Tess: it's been discussed off and on for years. a pr on html years ago about this. I think a lot of this did get discussed.. and afaict both geckon and webkit are opposed to the feature. The other concern here is these people get go ahead from the tag they're going to do it anyway and have another single engine feature with dubious value.. not good for the web in the long run

Dan: the multi-stakeholder thing is an issue.

Tess: we could loop in paul (or jean yves?) from mozilla or (??) - the two most vocally opposed years ago

Dan: other people in other orgs with reelvant feedback? EFF? Privacy focussed browsers, duckduckgo? More of a user empowerment issue than a privacy issue. But since it's also related to media, useful to get feedback about whether this empowers or disempowers users

Tess: i think that's a good idea

Dan: I'll send an email. And feedback from stakeholders of the ecosystem who aren't browsers? [leaves feedback]

#### [Note Taking: New Note URL field](https://github.com/w3ctag/design-reviews/issues/648) - @kenchris, @hadleybeeman, @atanassov

Hadley: a link to an explainer - that 404s.. 

Amy: [found it](https://github.com/WICG/manifest-incubations/blob/gh-pages/note_taking-explainer.md)

Hadley: a bunch of user need assumptions based into this.. be nice to spell it out

Rossen: [writes comment]

#### Breakout Rollup
#### Issue Triage
