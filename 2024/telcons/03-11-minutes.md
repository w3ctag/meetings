# TAG Teleconference
#### 11-13 March 2024

---

## Agenda:

### Breakout A (Europe / China) - [2024-03-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240311T100000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [DeviceOrientation Event Specification](https://github.com/w3ctag/design-reviews/issues/928) - @torgo, @matatk
* [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @cynthia, @torgo

### Breakout B (California / Europe)  - [2024-03-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240311T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss
* [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss
* [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss

### Breakout C (California / Australia) - [2024-03-11](https://www.timeanddate.com/worldclock/converter.html?iso=20240311T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Invokers API](https://github.com/w3ctag/design-reviews/issues/920) - @hober, @plinss
* [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson, @LeaVerou

### Breakout D (California / Australia) - [2024-03-12](https://www.timeanddate.com/worldclock/converter.html?iso=20240311T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo

### Breakout E (Europe / China) - [2024-03-13](https://www.timeanddate.com/worldclock/converter.html?iso=20240311T210000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman
* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

-----


## Breakout A

Present: Dan, Matthew, Max, Amy, Yves

Regrets:


### [DeviceOrientation Event Specification](https://github.com/w3ctag/design-reviews/issues/928) - @torgo, @matatk

Dan: we had a message from anssi .. they gave us a deadline that we've missed. the update aligns the spec with implementations. Sounds good in terms of multi implementer support.

Matthew: apa provided comments relating to a11y. On the cusp of proposing an accessibility considerations section for them, hopefully today. No major concerns - just alternatives to things that developers should provide.  Didn't see anything risky from an architectural perspective. They have S&P which we should pay attention to. They are doing testing to get feedback on s&p issues.

Dan: I've reviewed their responses to the self-review - no red flags. Should we be evaluating this against our new guidence on access to devices?

Matthew: app should not be able to distinguish between denying permission and... I don't remember seeing anything along those lines but worth checking

Dan: this is an iteration on an existing thing

Matthew: we didn't land [the PR](https://github.com/w3ctag/design-principles/pull/470)

Dan: we got positive reviews and addressed the requested change

Matthew: if we're talking about permssions stuff in this principle I agree with sangwhan's review... wouldn't have expected permissions in it from the title of the issue. If we land this it's worth raising an issue for this so we think about it again, but not hold it up on this.

<blockquote>
Hi @anssiko - thanks for sending this our way and thanks for the additional metadata.  
  
We're largely happy from an architectural point of view and I appreciate this is an update to an existing spec and that there is multi-implementer consensus - so great! 
  
In line with generally tightening up our privacy-related guidance, we have just updated our wording in the Design Principles about [exposing identifying information about devices](https://w3ctag.github.io/design-principles/#device-ids) and I'd like to draw your attention to it:  In our new guidance in 9.1, we say "A web app should not be able to distinguish between the user rejecting permission to use a sensor/capability, and the sensor/capability not being present."  From our read on the current spec, it's not clear what the behaviour is if a user rejects permission. Can you clarify?
</blockquote>

Matthew: filed w3ctag/design-principles#479 for us to keep track of Sangwhan's review of w3ctag/design-principles#470.

### [Allow transferring ArrayBuffer into WebCodecs object constructors](https://github.com/w3ctag/design-reviews/issues/889) - @cynthia, @torgo

Amy: they've asked a very specific question, maybe they know by now

Dan: remember a discussion with Sangwhan around this, no conclusion, didn't seem like architectural concern  https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/10-16-minutes.md#allow-transferring-arraybuffer-into-webcodecs-object-constructors

Amy: looking at S&P there are increased fingerprinting and exploitations on underlying codecs in their considerations sections, but maybe not significant enough to worry about - I don't know enough about codecs to know. There are mitigations mentioned.

Amy: the spec has editors from Google, Microsoft and Mozilla... so... [multi-stakeholder]

Matthew: a lot of info people could get out of the raw stream.

Amy: shipping

Matthew: ...since December

<blockquote>
Hi @Djuffin
  
My apologies it's taken us so long to get back to you on this. I realize things may have moved on signifigantly since you filed this review.  We *did* have a fairly detailed discussion on this review [in October](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/10-16-minutes.md#allow-transferring-arraybuffer-into-webcodecs-object-constructors) but unfortunately the output didn't make its way into this issue. Specifically you've asked "Should we just use a boolean value instead of a transfer list to indicate transferring of the ArrayBuffer contents to a WebCodecs object". In the absence of our feedback have you made any decision in the group thus-far on this? In any case, we don't see any issues and we're happy with the multi-stakeholder story here. 
</blockquote>

### AOB

Matthew: general opinion request : what would you say the current state of / need for CSS speech. The current state is it's not been implemented -- are people objecting or is it lack of bandwidth?  In APA we're doing some work on pronounciation... if CSS speech did exist we would have less work to do. Within the Accessibility community there has been respect for CSS speech but it hasn't been implemented...

Yves: I don't think we've done a review... 

### Appointees...



## Breakout B

Present: Peter, Amy, Yves

Regrets:


### [FedCM multi IDP support](https://github.com/w3ctag/design-reviews/issues/803) - @rhiaro, @plinss

Amy: they say they have not made much progress... re-reading [their brainstorm](https://github.com/w3ctag/design-reviews/issues/803#issuecomment-1771557647)... seems like 5 might be least bad from a ux perspective... but is maybe excessive tracking?

Peter: not sure if I have an opinion... none seem great

Amy: I had a reaction to the one that suggests buttons might move around just as you're about to click on something. Definitely not that.

Peter: dynamic updates don't necessarily require layout shifts if the designer does it right. But not not sure if they'd have enough information to know how many placeholders and where. Or add the new ones at the bottom.. but screws up other content

Amy: if it's waiting for some it could display a loader in a correctly sized gap..

Peter: if you know how many you're waiting for.. because you've made the get calls.  Why is this UI in the webpage? FedCM login UI should be in the browser itself?

Amy: excellent point

Peter: would be a departure from everything they've designed so far. Doesn't it make sense to be part of the browser chrome?

Amy: I guess had assumed they were making it part of the browser and didn't really click that's not what they're doing

Peter: I think that's not what they're doing... they did talk about using iframes. This is coming from trying to replicate existing behavious which was all done in the content. Always felt the browser should play a stronger role in session management, indicating whether you're logged in or not, regardless of whether it's fedcm. Browsers do a horrible job of UX for basic auth and certificate auth. Be nice to see..

Amy: agree. You can already sign into chrome with google... it's not new.

Peter: hoped this would go the direction of persona. The whole notion of browser managed login status and session management is beyond fedcm, but would love to see a unified ux for that that fedcm could just plug into, and take it out of the content entirely. Login button triggers the browser ux. Allows dynamic updates that don't cause layout shifts in the content. Doesn't necsssarily solve all of the timing and perf issues.

<blockquote>

We discussed this in our call today. It seems like a good solution from a UX perspective would be if the IDPs are loaded dynamically, but without causing layout shifts in the content of the webpage (we all hate when a button we were about to click on is suddenly displaced from under our pointer). Have you thought about making this part of the browser chrome, rather than the site? Essentially moving the rendering responsibilities from the RP to the user agent.

User agents have historically had horrible UX with basic auth and certificate auth, it would be good for users if the UA could play a more active, and consitent, role in managing logged in state and UX for all forms of authentication. This implies creating other APIs beyond FedCM to handle other forms of authentication, but they could have a uniform UX.  Do you think this is a direction you could see FedCM going in, in the future?
</blockquote>


### [FedCM: LoginHint, UserInfo, and RPContext](https://github.com/w3ctag/design-reviews/issues/839) - @rhiaro, @hadleybeeman, @plinss

Amy: they've replied that the thing we were worried about with UserInfo is not actually a thing that happens

Peter: their answer conflicts with my understanding of what they were asking for

Amy: what is it querying? if you log out and walk away and the next person sits down..

Peter: you only get continue as if you're already signed into the IdP.. maybe that's what we were misunderstanding

Amy: so you have to remember to sign out of your IdP as well as your RP

Peter: what's the log out story.. if I click on log out on pinterest, did I also log out of google? Is that clear? When I log into google now, I immediately log out, then next time I go to log in it says 'continue with..' so they are storing a cookie

Amy: so that's what they're replacing?

Peter: if I'm signed out of the idp does the idp really have no knowledge ..?

Amy: with the google xample it would be a first party cookie, this is replacing third party cookie

Peter: it's only reflecting the fact that you're signed in, not that the idp might not know who you are when you're not signed in.. that bears out in their flow chart

Amy: very slight security problem in that it makes it easier for a malicious next user to sign into an RP if you forgot to sign out of your idp, whereas they couldn't before

Peter: this is a general problem with fedcm... need to make it clear when you sign out of an RP are you also signing out of the IdP or not. Single sign out - it's a problem with lots of single sign on

Amy: where is the best place to ask about this... An issue on their repo?

Peter: is it more explicit in their spec? Not seeing much. CG report about sign out flow. Not seeing anything about it in explainers. *asks in issue*

Amy: and propose close? This is sort of orthogonal

Peter: yes, we were fine with their original question, this is higher level

### [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss

Amy: it's shipping, and they did change the name

Peter: sounds like it's moving in the direction of letting the browser manage all of this. Let's the IDPs tell the browser whether they're logged in or not. Doing it with a header ... would only apply during a direct interaction with the idp? They are putting this in a separate object which isn't in a namesapce, ties into DP conversation last week...

Amy: we could give them guideance if we have an opinion...

Peter: I'd prefer the extra namespacing... but they're only adding one method, which is an argument for putting it on the navigator. I could see this api expanding in future. NO way to query this logged in state. Which is good. My main concern is tying it into the privacy cg is logged in api. Can we just combine all of these things?

Amy: sounds like it has overtaken/superseded that API?

Peter: happy to close this? Can check with Dan

Amy: yep

## Breakout C

Present: Peter, Tess, Martin, Lea (latter 1/2)

Regrets:

### [Invokers API](https://github.com/w3ctag/design-reviews/issues/920) - @hober, @plinss

<blockquote>
  We're broadly in favor of invokers because it unifies some existing interaction patterns.
  
  We feel it makes sense to have an `invoke(action, invoker)` method because it lays a path for future interactions with elements.  We think that this might be more useful for custom elements or future features that are added to the platform.
  
  We observe that a lack of additional arguments to invocations (or `invoke()`) are a concession toward the declarative nature of the core feature.  Rather than a flaw, we see this as an important characteristic of the design.  It simplifies this design and this characteristic seems like it is worth protecting.  Richer interactions can remain the domain of script.
  
  Having `invoke()` also helps discoverability.  We think that this would be more useful if it were possible to get the list of available actions from elements.
  
  (A footnote from me: when we ask questions, like the one above about focus, we appreciate your helpful answers.  We appreciate those answers being added to documentation even more.)
</blockquote>

### [Isolated Web Apps](https://github.com/w3ctag/design-reviews/issues/842) - @martinthomson, @LeaVerou

Discussed https://cryptpad.w3ctag.org/code/#/2/code/edit/6L3cfzmBjZv5tKRRkwV4k-ll/

Discussion about whether to close the issue and whether the advice here, which seems final is indeed so.  Resolution was to provide the feedback, but leave the issue open to give the proponents a chance to respond.

## Breakout D

Present: Peter, Tess, Martin

Regrets:

### [Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @hober, @LeaVerou, @torgo

Tess to draft comment based on discussion today

```
... and that the new one will solve some problem the others cannot
MDN has three levels, I see
"short_name - Web app manifests | MDN" -> presented in reverse order
"Request for Position: Topics API · Issue #622 · mozilla/standards-positions"
```

## Breakout E

Present: Dan, Yves, Matt, Max

Regrets:

### Discussion on Breakout Day



### [Review Request for Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724) - @torgo, @rhiaro, @hadleybeeman

*bump*

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: latest response difficult to understand.. their extension extends site A's capabilities to serve things from site B... That's where the problem is.

Matt: one of the questions raised was about uniqueness of IDs for apps - they've pointed to an explainer that talks about unique app ids... after that sangwhan was still concerned about guaranteeing the unique keys... they are claiming there can be a unique ID but there is some question about that.

<blockquote>

Hi @LuHuangMSFT - just coming back to this now. I think the risk is not necessarily that https://siteb.com can spoof https://sitea.com, but rather than since https://sitea.com can serve content from https://siteb.com *as if it comes from https://sitea.com* that content from https://siteb.com can therefore completely hijack https://sitea.com without the user's knowledge.  So if that understanding is correct then that breaks the security guarantee for web content.  The proposal would need to mitigate against this risk in some way way - for example, scoping this very tightly so that it cannot be abused in this way.  We also think the spec needs a [privacy review](https://github.com/w3cping/privacy-request/issues/new/choose) and we would suggest that you request that separately.  Also, as Sangwhan mentioned, we remain concerned about the uniqueness of the identifier.

</blockquote>

### [TAG review request for the IDP signin status API](https://github.com/w3ctag/design-reviews/issues/884) - @rhiaro, @hadleybeeman, @plinss

[Peter:] Amy and I looked at this and think we can close as satisfied, but wanted Dan's feedback since he posted a number of questions.

### [showPicker()](https://github.com/w3ctag/design-reviews/issues/900#issuecomment-1889327793)

Matt: no progress since we posted that issue... right now it's open - our main concern is consistency... We're hoping if we need to change what the default is that it's still new enough to do that.  I'd like to post on this WHATWG thread... to encourage them to come back and let us know "this is why we think it would be the default behaviour"...  OK?  I will subset the TAG comment. Some assistive tech people have said "you should do this" some platform providers "you should do that"... 

Dan: Sounds good to me.
