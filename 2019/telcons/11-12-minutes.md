## TAG Teleconference
##### 12 November 2019

Present: Peter, Alice, Hadley, Tess, David, Dan

Guest: Dave Tapuska, Chris Harrelson

Regrets: Yves, Sangwhan

---

Agenda:

* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman

hadley: I can lead the discussion... 

... We've been working on this thread for a while, I felt like we were talking in circles.

... Might be useful to talk through these things in person.

... David, walk to talk about what is client side and what is server side?

david: Feature seems to assume that all browsers would have client side translation... pretty clear that's not the case.

dtapuska: Well there is feature detection here, so you wouldn't support the feature if you didn't have a client side translation library.

david: .. I'm not sure this is the issue we want to focus on first, in any case.

hadley: Ok. 

... Another issue was whether this was a single vendor, single use case (API).

... Alice asked for an example in the explainer of a non-search website, since the explainer is based largely around search. Chris responded with an example of Facebook.

... Two piece of this... Alice hoped this would be in the explainer. 

dtapuska: Yes, we can add it.

hadley: Great. It also felt at various points in this evolution that this was surely driven out of Chromium, therefore the single vendor, single use case concern was around this not being a collaborative effort.

dtapuska: Well, there are other Chromium vendors interested in the feature, for example Microsoft, for very similar use cases. That doesn't address the multiple (engine) issue, but there are multiple browsers interested in it.

... We gave different examples ... there was a Google translate widget in the past that allowed pages to embed a piece of script that allowed them to influence the translation of the page. We believe there are use cases other than search use cases, based on adoption of that widget.

hadley: We're talking about the difference between how this is being created... normally we need two independent implementations for the standards process. Is any of this a collaboration with another engine?

dtapuska: No. Part of the blink intent process is that we solicit feedback from the TAG, but that we don't require another vendor implementation. We don't have another implementation on board at this time.

hadley: We talked about the blink guidance at TPAC... I haven't seen it. This raises an issue where TAG ends up doing work reviewing and helping on features which don't end up being multi-vendor [i.e. not standard]. So this might be a point where we say we've given you the advice that we can...

chris h: When you say blink or chromium only... when new features are proposed, it's not uncommon for them to start off in one browser. This is not only chromium, safari has certainly done this in the past. It would be good to separate comments about whether the use cases are reasonable from whether, at the moment, only one browser has committed to implementing it.

hadley: That is very reasonable.

... The last issue, which has been a regular theme in this review, is the fundamental issue of the nature of the web and how users express their preferences. Have we inflicted our ethical web principles on you? We produced it at our f2f in Iceland in May. One thing we wanted to capture was how the user expresses their preferences through the user agent, and the user agent mediates that with the site. In this case, the referring site is passing on some information to the ... referee site. This takes away the user's ability to ask or instruct their user agent to perform language selection on their behalf.

.. We've gone around in circles on this, so I was wondering whether we weren't expressing this concern well, or whether we just aren't on the same page.

dtapuska: We keep coming back to what the site knows about users. I wanted to talk about the use case of an opaque user to the service, doing something the UA can't detect. For example, using speech to interact directly with a website. The website may want to redirect you somewhere... they may redirect you to a website which is prefixed with translate.google.com or translate.bing.com... they can do that since they are referring you there. Those models break attribution on the web.. you load the URL and the URL is a google.com URL, not the website URL. The influence you're concerned about is aleady there... if you're concerned aboutthat the user is signed in... 

hadley: I hadn't been thinking about the logged in use case. It feels to me like the question is, who is the authoritative decider of what language I would like to see the website in? Usually these preferences are set and expressed through the user agent.

dtapuska: The user would get a prompt saying that the browser would like to translate the page based on the hint that is passed on. So it's very clear to the user that the browser will be doing translation.

chris h: To clarify, the hint is *only* sent to the User Agent, not to the site. So the User Agent can use that hint if it wants, to translate the site to the desired language. It's not acutally leaking information between sites. It's using information the user has given to one site, because the user trusts that site, to pass on a hint to the user agent about the next site. This seems to be compliant with the ethical web principles. We think this actually helps preserve the origin model of the web. It gives users an opportunity to see information in their preferred language.

hadley: That is helpful, thanks

david: It's not clear to me... 

chris: It's not that the user does or doesn't want certain pages... they may be using search engines to explore information, and the search engine can use information they glean from the user's interaction, rather than trying to teach the user how to configure their user agent.

david: That's reasonable... if the user speaks a particular language, won't the browser want to trnslate everything into that language? Perhaps the mechanism you want is not a hint from the site to translate the next link, but a hint to the user agent that the user may want their language setting to be changed.

chris: Maybe...

hadley: what have you found in your experiments?

dtapuska: We are surfacing a lot more search results that are relevant to users. That's mainly the feedback that we've had.

hadley: You don't know (how consistent the language preferences are)?

dtapuska: no

chris: Language is complicated... in countries with multiple spoken languages, language settings may be a vanity (class) issue, or people may not consistently use one single language

plinss: Do you see sites not using correct lang attributes, not exposing the correct language to the page?

.. if the UA knew what langauge the page was in, and the user's language needs, the UA should be able to figure this out on its own.

dtapuska: It's not that the websites are written in the right language, but marked up incorrectly...

plinss: My UA should know that I prefer english, if I visit a website..

dtapuska: Yes, that already works. This is about linking to that site. If you look at the w3c wikipedia site, there is much less content on a non-english version than the English version. So for a non-English speaker you might want to link to a translated version of the English site rather than the localised site for that language.

torgo: One thing that raised alarm bells for this review was that privacy considerations seemed kind of light... it seems like you've thought a lot about this in fact, and it would be good to see that thinking reflected in the privacy review and/or explainer.

dtapuska: will do.

chris h: Coming back to the previous point... it's proven difficult to get the browser settings right; for a variety of reasons they often don't match the user's preferred language. But sites have more ability to understand the context of the user, and can use this context to send a hint.

hadley: How much of this is a UX failure in the browser?

chris h: I don't know, but I know that we've been trying for years to address this problem in the browser and we haven't been able to find a way to get it right. It seems like we can systematically improve the amount that people can read and access information, in a way that potentially augments the structure of the web; and is privacy perserving

david: I understand what you're saying about sites being able to understand what language a user is primarily using, but I'm concerned that this solution offers a way to fix it but only when a user is getting all of their links from a source that knows what language they want to speak (google, facebook, etc.). That's pretty concerning to me.

... it would be good to see a way to solve this problem in a way that a user can go to any site and have the browser offer to translate it into their preferred language.

chris h: I agree, but we don't have a solution to that problem at this time. Right now we don't have any way for any sites to help the user in this way; the status quo is to go through a translation site.

david: what about suggesting a user profile change?

chris h: I hadn't considered that one.

hadley: Can we highlight what the potential knock-on effects are?

david: I can probably write something in the issue...

hadley: I think this is the kind of thing we look for in an explainer... Chris has observed that we don't have a solution for this problem, it seems worth noting down.

chris h: This is a pretty simple feature that I don't see any immediate downside to... it doesn't solve everything, but I don't think we should let the perfect be the enemy of the good.

hadley: well it sounds like david does see some downsides...

chris h: Of course if their are some, we should consider those.

dtapuska: It might makes sense to add a note that user agents may observe the hints over time, and ... add languages into accept-language, or prompt the user to set that as their preferred langauge. We can certainly add that into the discussion.

plinss: I've certainly had Google assume that I want the country of the language I've travelled to, like when I go to Japan and it assumes I want everything in Japanese. This is a messy situation and I could see it going wrong.

dtapuska: I think we're hoping that this feature would improve that situation, but I can understand your concerns.

plinss: This seems a bit like the captive portal problem... everyone trying to solve it in different ways, and the solutions end up fighting each other.

hadley: It seems like we can wrap up our discussion.. would like to see more detail in the explainer on the trade-offs made.

... I would like David Baron and Peter to flesh out their concerns in the review, and to have those concerns addressed.

dtapuska, chris h: Sounds good.


* [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon

tess: let's push this out two weeks

* [HTMLVideoElement.requestAnimationFrame()](https://github.com/w3ctag/design-reviews/issues/429) - @cynthia, @dbaron, @kenchris

dbaron: Need to punt this one, unfortunately.

* [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394) - @dbaron, @kenchris

Punt.

* [Web Bluetooth Scanning](https://github.com/w3ctag/design-reviews/issues/333) - @cynthia, @dbaron, @torgo, @kenchris, @lknik

torgo: Heard some good stuff at TPAC about the privacy considerations. Has that been reflected in the issue?

plinss: Don't see anything.

torgo: There was a comment on 22 September... let's leave a comment asking for clarification on the privacy concerns and then revisit next week.

plinss: Are you able to write that comment in the issue?

---



