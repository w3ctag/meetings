## TAG Teleconference
##### 15-17 March 2021

---

### Agenda:

#### Breakout A (Europe / US) - [2021-03-15](https://www.timeanddate.com/worldclock/converter.html?iso=20210315T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo, @atanassov
* [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman
* [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss
* [HTMLPopupElement - popup](https://github.com/w3ctag/design-reviews/issues/599) - @hober, @LeaVerou, @kenchris, @atanassov
* [TAG Specification review for viewport height client hint](https://github.com/w3ctag/design-reviews/issues/615) - @ylafon, @plinss
* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @torgo, @hadleybeeman

#### Breakout B (US / APAC) - [2021-03-16](https://www.timeanddate.com/worldclock/converter.html?iso=20210316T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311) - @cynthia, @plinss
* [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia
* [CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @LeaVerou
* [Early Design Review: document.prerendering](https://github.com/w3ctag/design-reviews/issues/613) - @hober, @atanassov
* [ARIA in HTML review](https://github.com/w3ctag/design-reviews/issues/614) - @hober, @atanassov

#### Breakout C (APAC / Europe) - [2021-03-16](https://www.timeanddate.com/worldclock/converter.html?iso=20210316T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Get Installed Related Apps](https://github.com/w3ctag/design-reviews/issues/436) - @torgo, @kenchris, @hadleybeeman
* [Limit allowed "accepted" extensions in File System Access API file pickers.](https://github.com/w3ctag/design-reviews/issues/580) - @cynthia, @kenchris
* [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman
* [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris
* [WebCodecs (again!)](https://github.com/w3ctag/design-reviews/issues/612) - @cynthia, @kenchris
* [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @torgo, @hadleybeeman

### Plenary Session - [2021-03-17](https://www.timeanddate.com/worldclock/converter.html?iso=20210317T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### [Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611)

* Breakout Rollup
* Issue Triage

-----


### Breakout A

Present: Peter, Kenneth, Dan, Amy, Lea, Yves, Tess, Hadley

Regrets: Rossen


##### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo, @atanassov

Dan: kind of stalled still - we have left feedback and the group chairs have been contacted but no resposne yet.

##### [Digital Goods API](https://github.com/w3ctag/design-reviews/issues/571) - @hober, @hadleybeeman

Amy: i left some feedback a while ago - i asked a question they haven't answered - about implementer buy-in.

Amy: ... there's a lot of people in their issues in this spec arguing that it's not needed...

Tess: no traction outside of their own ecosystem... we already have payment request API to buy things - typically showing a list of goods you can buy is...  ... if amazon (e.g.) were to adopt this - would they want the browser to know about what products are on the page?

Amy: a bit confused - because they say it's not for payments, but they say it's so webapps can be listed in native app stores so that native app stores can use their payment processing.

Ken: we were the ones that asked them to run it through the TAG... 

Hadley: if we do care about there being an ecosystem of app stores behind webapps then we should care about this being an API as part of the platform...

Ken: MS might be interested of this...

Amy: I get the impression that this API doesn't enable an ecosystem of app stores (diversification) but ties in to existing APP stores.

Hadley: it feels like this is a work-around because Play store won't do what they want.

Tess: app stores come and go, the web is enduring. We should be reluctant to add work-arounds ... for things. we will need to maintain it for compat even if the feature doesn't make sense any more.  If the Play store has some specific limitationm, we shouldn't permenantly change the web to work around that.

Lea: absolutely.

Hadley: I agree although - but don't we have examples of where stuff has become open because we worked around closed things.

Tess: well with EME we reduced the proprietary surface...  Yes sometimes - but it's something we resort to. There are lots of web sites on which you can buy digital goods. They use the table element and that seems to work fine. And they can use the payment request API.

Amy: is the difference that they don't want to be listed in the play store?  

Tess: if the policy is that you have to use their pauyment processor then Chrome could sovle that by introducing a play store payment method - in the payment request API. That's doable today without any new API.  

Dan: I agree...

see also: https://github.com/WICG/digital-goods/issues/5#issuecomment-635718224

##### [CORS-RFC1918](https://github.com/w3ctag/design-reviews/issues/572) - @torgo, @hadleybeeman, @plinss

Hadley: [comment from mike](https://github.com/w3ctag/design-reviews/issues/572#issuecomment-768118905) - Mike has good will, however...

Peter: could be that everyone thinks this is the right direction but they are happy with Chrome to lead the way and see what breaks... 

Dan: not enough input from other parties. I'd love to know mnot's view on this, it leads to IETF territory.

Hadley: in one of the issues linked, Anne has [expressed support](https://github.com/mozilla/standards-positions/issues/143#issuecomment-768138667).

Dan: do *we* have any concern about it?

Yves: if there is no implementation traciton - it won't reach a point where it will be implemented in a reasonable way...

Peter: my key concern is about ipv6 - how to tell private from public.  Not everyone uses NAT... ipv6 can be tricky. Their response addresses one of the issues. They do have issues tracking these things. I'm OK to let them grind away at it.

Yves: there are link local addresses in ipv6.

Peter: some isps will give you an entire .. 

[discussion on the ins and outs of ipv6]

Peter: my computer for example gets a public ipv6 address but i have 2 other /64 subnets behind my firewall. .. so might be considered public but actually private... but they know about this problem.

Dan: close it and say "we've already expressed our feedback - we look forward to hearing about your implementation experience" and I have reached out to Mark.

[proposed close]

##### [HTMLPopupElement - popup](https://github.com/w3ctag/design-reviews/issues/599) - @hober, @LeaVerou, @kenchris, @atanassov

Lea: we gave a fair bit of feedback - they added an `open` attribute as part of that response. They also added a popup attribute - you put it on elements you want to trigger a specific popup but no indication on [how to use it]. Also: there was a lot of talk about how this relates to CSS. But this then becomes a 2-part proposal and the other part hasn't been proposed yet. There are `autofocus` and `delegatesfocus` attributes.. scoping issues. Dismiss behavior - no way to turn it off - has been a problem for `dialog` authors are complaining about customization. Could mean any time they have to do something custom they just implement it themselves.

Peter: there was another proposal for a dismiss listener

Tess: I like dialog behaviour, escape is always a way to get out. Sites don't always do the right thing, we don't want a user to get stuck in a modal without any way to get back to the page. Agree sites should be able to add custom ways of exiting the thing, but important for the browser to always provide a way to get out

Lea: there are valid reasons where you might want to make a popup not closeable. Isn't that the point of a modal?

Tess: fullscreen as an example, it has to be exitable. The app might have lots of reasons for making it not, but the applications reasons are lower than the users needs.

Lea: absolutely, but fullscreen takes over your entire screen where as a modal is only within the current page

Ken: on mobile it's full screen...

Tess: backdrop overlay behind a modal prevents selecting text on the page.. A lot that a modal can stop you from doing.

Lea: light dismiss is not.. it's easier to dismiss a popup than a dialog, not just escape key, cicking outside dismisses it, this seems like something authors would want to be able to trap

Tess: I think you should be able to exit by clicking outside, should be default

Ken: yeah

Lea: default yes, but only behaviour?

Tess: additional ways to exit that's fine. I don't think it should get in the way

Ken: don't want people to block it from exiting. Stupid mistakes like a cookie banner behind that you can't exit. I want really compelling use cases where you want to block people from exiting

Tess: block until you make a choice between three things but a script inserts content so you can't pick the things, and never get out of it

Lea: okay

Peter: if the api surface guarantees that there's always a way to exit the apps have to design around that, and respect the fact it might be exited without a choice and deal with that however they deal with it, and that's a better user experience. Agree that there should be a way for the authors to be notified of the fact it was dismissed, regardless of how it was dismissed

Lea: they have a close event, like dialog

Peter: context that it was dismissed vs closed because it was interacted with?

Lea: I don't think so.

Peter: might be important to know that

Lea: it's a hide event. That should probably be harmonised with dialog and have the same event name

Ken: that would make sense

Tess: yes should align with dialog. Consistency is good.

Peter: and there was [another proposal](), dismiss watcher, we had issues with that and think it shouldn't proceed but if it does, they should use that, consistently across the platform

Lea: what about the popup attribute?

Tess: am worried about it because we still don't know the positioning story. How that's going to work? We shouldn't be sprouting html features that tie into an undefined positining thing. The positining thing might inform us of how it should tie into html, maybe an attribute isn't the right way, we shouldn't constrain the CSS WG before it makes progress on this.

Lea: apply to anchor attribute as well? seems more essential

Tess: Maybe. Cart before the horse. I get the temptation to do the parts that aren't hard. We need enough of an idea of how the hard parts work so we can do this part.

Lea: what do you think about tabbing? if you have a popup anchored to another element should tabbing from the anchor focus the popup?

Tess: I don't know

Ken: should be easy to focus a popup

Tess: if anchor is a button and you press the button it causes the popup I wouldn't want the popup until I activate the button not just focus

Ken: but don't want focus on something behind the popup

Tess: if the popup pops up automatically when the button gets focussed you're in a weird positon where the focused element is behind the popup. If you wanta  UI with a button to cause a popup, pressing the button should cause focus to move to inside the popup. Other UIs you might ave something that isn't a button that is focusable and you want when it focuses to cause a popup to come up.. can imagine wanting that.. seems problemantic because you get a cycle where youf ocus the thing, casues thepopup, focus gets moved inside the popup which blurs the thing that causes the popup to appear which causes the popup to disappear

Lea: moving automatically to the popup is disruptive

Ken: more weird if it stays behind and is like a toggle

Lea: anchor doesn't specify how the popup is shown, that is managed separately by adding open attribute or calling show method. Anchor tells the popup what was the invoker element. If you have an invoker element and press tab, where should focus go?

Tess: focus is currently in the popup?

Lea: no, focus is on the button that triggers the popup, button is still focussed, press tab

Tess: the button blurs and there's a chance the popup goes away. If you focus inside the popup and make the popup disappear that's not great

Lea: that will happen regardless of what the next focus eleemnt is. Should the anchoring relaitonship between the popup and the invoker override any existing tab order? should it also establish a tabbing order when you make an element the anchor of a popup?

Tess: if the popup is open you should be able to tab to the things in it, somehow. Where in the order I don't know.

Lea: that's a separate issue. Sometimes authors put the popup in a separate place in the DOM so without manual management of the tabbing order tabbing would go to another element not the popup. Could the relationship mandate a tabbing order? could help accessibility but could get in the way. Enforcing a tabbing order that is relative is a pain. if authors have to do this manually

Tess: they'll get it wrong. Does seem like it should do it.

Lea: maybe it should be easier to have a relative tabbing order

Peter: if you've activated a button that should move the focus within the popup

Lea: without tabbing? They have a separate attribute for that, autofocus. Also delegates focus attribute which means if the popup gets focussed the focus moves automatically to the first descendent element that is focusable. 

Ken: that exists in web components

Lea: that sounds like more useful as a global concept and not special to popup

Ken: maybe

Dan: we're trying to design a feature.. What feedback can we give?

Hadley: have we asked them about tabbing?

Lea: they are trying to decide so wondering if we can provide input

Hadley: sounds like we might be in a better position to react to what they propose? I didn't hear consensus between all of you.

Peter: we'd like to see the rest of this designed before we thumbs up and they should come back when the rest has been figured out.

Lea: yeah

Peter: someone write that. Maybe premature to define some of these attributes until we have the rest of the story.

Lea: [will write](). Ask them to ping us when the rest is designed.

Ken: or maybe we have given the feedback on early and they should file a more mature review?

Peter: yeah. Close but tell them when the rest is designed please open a new issue and link a reference to this one.

Dan: feels like a lot of good valuable discussion just now. 

##### [TAG Specification review for viewport height client hint](https://github.com/w3ctag/design-reviews/issues/615) - @ylafon, @plinss

Peter: this is a small delta - and there is already a width ch.

Yves: I reviewed - i am not happy with client hints in general but apart from that i think it's fine. 

Yves: not dure having a precise number here is useful - wondering if some fuzziness is expected or not.

Ken: I left a comment.

Peter: Spec says it shoould be the window's inner height.

Yves: can we close it with "it won't harm" but neither good or bad?

Dan: could say "ambivalent".

Ken: I don't think we need to block.

Yves: let's close.

Dan: +1

**closed**

##### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo

##### [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @torgo, @hadleybeeman

Dan: I sat in on this privacyCG call and saw how aggressively google is pushing this forward in a product management way as opposed to a technical spec way... I left feedback. How are we going to mitigate against misue, creating a third party ad network by redefining third party and first party? One of the answers was "we" will make sure that all the domains in the FPS are the same org

Tess: who determines that? 

Dan: in what sense are they affiliated? In some senses amazon.com and .co.uk are the same, but for data protection they are not. Different regulatory regimes. Facebook and Salesforce are very strongly in favour. Use cases I'm hearing are not thinking through regulatory and data protection issues, that concerns me. Might be other things we need to examine more closely. Google are trying to build other specs on top of this spec. We've pushed back. Hopefully we can examine different parts and feedback architectural issues.

Peter: lukas has been blogging about CNAME abuse.. 

Dan: Discuss more in breakout C
  
### Breakout B

Present: Lea, Peter, Rossen

Regrets: Sangwhan


##### [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311) - @cynthia, @plinss

Reviewed, set to propose close pending Sangwhan's input.

##### [Media Source Extensions for WebCodecs](https://github.com/w3ctag/design-reviews/issues/576) - @hober, @cynthia

Bumped waiting for Sangwhan.

##### [CSS Custom Highlight API Module Level 1](https://github.com/w3ctag/design-reviews/issues/584) - @hober, @LeaVerou

Bumped waiting for feedback from CSSWG

##### [Early Design Review: document.prerendering](https://github.com/w3ctag/design-reviews/issues/613) - @hober, @atanassov

Some discussion about API shape, comments left.

Rossen has some concerns about exposing prerender state to the document.


##### [ARIA in HTML review](https://github.com/w3ctag/design-reviews/issues/614) - @hober, @atanassov

##### [WebXR Hit Test Module](https://github.com/w3ctag/design-reviews/issues/463) - @hober, @torgo, @atanassov

Closed with feedback for more examples in spec.


### Breakout C

Present: Ken, Amy, Dan, Yves, Hadley

Regrets:


##### [Get Installed Related Apps](https://github.com/w3ctag/design-reviews/issues/436) - @torgo, @kenchris, @hadleybeeman

Dan: maybe didn't close because Ken wasn't there. Proposal from Mozilla hasn't bee considered, concerning, means what? They haven't listened to our feedback? API design itself seems fine but fingerprinting issue hasn't been looked at so we're not happy, or ambivalent..

Ken: they shipped it

Dan: we can say we're ambivalent then

Ken: close now?

Dan: I think it should be resolution: ambivalent. Unsatisfied would connote this is really deeply harmful, or the design is really bad.

Ken: will figure out what to [write](https://github.com/w3ctag/design-reviews/issues/436#issuecomment-800047349)

Dan: look forward to hearing more once it goes through incuation (the I in WICG is incubation, we should always say that)

**closed**

Dan: boom.

##### [Limit allowed "accepted" extensions in File System Access API file pickers.](https://github.com/w3ctag/design-reviews/issues/580) - @cynthia, @kenchris

Ken: no feedback. About what file extensions you can use, they added .c++ ... if you're adding that you need .c# and others commonly in use that are weird, I researched and aded screenshots and we haven't heard anything back.

Dan: will ping Chris H about it. Re-review in plenary and see if there's anything new.

##### [WebXR Dynamic Viewport Scaling](https://github.com/w3ctag/design-reviews/issues/588) - @torgo, @hadleybeeman

Dan: I left feedback, we got some responses 7 days ago, which I reviewed, but it is a small delta in an existing spec and it looks like we're ready to close this. Nothing further to be done. They've taken our feedback on board. Came across because of blink process. I also raised it to webxr group chairs to make sure they're aware of it (going to raise with Chris H: that blink people don't raise reviews without looping in editors and group chairs if it's in a proper WG; another thing if it's in WICG).

[proposed closing]

##### [App history API](https://github.com/w3ctag/design-reviews/issues/605) - @cynthia, @kenchris

Ken: haven't had time to look in detail. It's really big.

Dan: feedback from domenic 6 days ago. [He left four points](https://github.com/w3ctag/design-reviews/issues/605#issuecomment-794606658) about where to focus our review.

Ken: not easy questiosn to answer.. the API is designed around the weirdness of some APIs so replacing them would mean re-adding weirdness... could be done as an opt in, but something I have to think about. I can look at those issues.
... First one is more of a question to web devs than it is to us. Issue 66. Web developers might nt want to update the address bar immediately, but I don't know what the use cases are, I'm not one of those developers who don't want it to update..

Dan: we can try to channel the needs of web developers.

Ken: they don't know if anyone is doing it.. you'd want to include people working on routing frameworks and things like that. I could ask my friends at ionic if this is something..

Dan: I get nervous any time we start talking about rewriting the URL bar. I need to re-review security & privacy quesitonnaire and considerations section. I recall being pleased with what I read there but don't remember what.

Ken: asked someone working on angular.

Dan: are they doing anything with the URL bar that can't already be done with the existing history API?

Ken: can't do that today because you're changing the state. By not having push state in this new API might be an issue.

Dan: making a note about potential for misuse. Discuss more at plenary, can bump to next week.

Ken: adding some comments into their issue (the ones linked).

##### [WebCodecs (again!)](https://github.com/w3ctag/design-reviews/issues/612) - @cynthia, @kenchris
  
Ken: Sangwhan gave comments and they responded and he wants to look further. Need Sangwhan for this one.

Yves: we did add something about adding to the web platform in the guidelines.. we can look if the guide is okay with what they proposed? ... Is it okay to add examples on how things can go wrong in design principles if they are not respected?

Dan: I think so... raise it as an issue and we can discuss it in design week.

Yves: in the case of the HTTP header syntax, explaining that it's imporatn to respoect it, and counter example is the cookie header which has been a nightmare.
  
Dan: if you have a fully formed idea of what you want to put in, make a PR.

Yves: the style is usually very terse 

Dan: depends which part of the document you're in.. We need to keep balance. Having examples is always good.

Yves: first was too terse, I'll work on that.

.. for web codecs we should wait for Sangwhan.
  
##### [Temporal proposal](https://github.com/w3ctag/design-reviews/issues/311) - @cynthia, @plinss

Can we close?

Ken: already moved to stage 3 or 4

Dan: taking a look at [an issue](https://github.com/tc39/proposal-temporal/issues/1219).. they're being responsive to our feedback. It's already on proposed closed. Close at plenary?  

##### [First Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @torgo, @hadleybeeman

Dan: we have had some [feedback](https://github.com/w3ctag/design-reviews/issues/342#issuecomment-799709089). 

Ken: agree that is what is happening on the web today. Same issues when working on the web app manifest, microsoft commented they had multiple domains they considered the same. Not an invented thing, actually an issue.

Hadley: my instinct would be to put a lot of time and energy int listing everything this is going to break. Same origin policy... and issue a finding. I don't know if we've got TAG consensus. It feels like this group are arguing that thes ame orogin policy doesn't work fo rthem so they want to change the web. I'm not convinced on fthe use case, and second the knock on effects of doing this..

Dan: yes, concerned with the knock on effects. The potential for abuse. They are talking about how we'll have these allowlists for ... there's always an angle, a commercial angle, business angle, a we-know-these-people angle

Hadley: very different from whether someone gets a TLS cert from a cert authority, authority is not passing any judgement or saying anything about how someone interacts with the site. They're just saying "we've issued this certificate to this website".

Amy: what happens if different browsers implement different allowlists?

¯\_(ツ)_/¯

Hadley: in an unhelpful world each site could have different allowlists per browser..

Yves: some mistakes might disclose information from a site to the owner of the allowlist. if you accidentally add another site to the FPS that you are owning then you can get informationa bout new cookie from there and retreive it.

Hadley: interesting hack.. if you can get into a site's allowlist and add your own site to it suddenly you've got... could you borrow their auth tokens? Get someone to log in yoru site and have access to others?

Yves: go over the restriction that those cookies won't be reused, or can use them as remote login

Dan: what user visibility will be present? It seems like they're assuming there will be a user facing prompt that says .. that allows users to accept that the browser will treat these different domains as the same organisation. That seems to be.. not well thought through. Other potential for abuse is an ad network that is able to claim "we're the same org" and has a relaitonship with a browser maker, will therefore have a very strong competitive advantage, over an ad network that doesn't have a relationship with a brwoser vendor because they can say that their ads are all .. they can take advantage of the FPS allowlist. There's an antitrust almost thing?

Hadley: antitrust isn't our thing. User expectations and user trust is our thing. If the browser is no longer just serving the user but is serving the ad network that' screws up the web.

Dan: question.. considering the feedback from Mozilla and webkit community is that they find this deeply flawed. Is there any way.. under what conditions is a first party set like proposal acceptable? What are the mitigations that we and the rest of the community would find acceptable? Eg. full visibility of the allowlists within the browser UI prompting ability to turn off the feature. Things like that? Visibility to ad blocking extensions. The list of things that would need to be in the  mitigations or privacy and security in order to make it acceptable, if that exists at all.

Hadley: good quesiton. If we take the example of facebook and instagram, which are two we've talked about being put together in a set, I can't imagine without designating browser UI a scenario in which we'd feel comfortable with users having the expectation that one is the other, that logging into one means you're logging into the other, that they have the same cookie access. All of the mitigations you've talkeda bout can try to teach users that the web is doing something new and different, which may work..... but.. I'm struggling to think of something we could do with the existing features that would help someone understand that if they've given access to facebook to their microphone that instagram should have it too.

Amy: whatsapp is even worse in that set

Hadley: different use cases, they are used in different ways, eg. location

Dan: one place that permission prompts is mentioned in the explainer is avoiding the use of valuable screen real estate or presenting confusing permission prompts.. which sounds like exactly what you're talking about in that they are subverting users expectations. If you give instagram access to your camera, are we then.. if fb and instagram are in the same FPS are we giving facebook access to the camera as well? Which users would probably not agree to. They say it's an explicit non-goal to to have information exchange between unrelated sites for ad targeting or conversion measurement. I agree with Hadley that we need to have a more detailed feedback document at least. It could be a finding depending.. a finding would be a nuclear option. I would rather find a way forward where eg. it could say FPS only applies to these targeted cases and doesn't apply to permission prompts for access to bluetooth or camera etc. It could really narrow the scope.

Hadley: right about finding being a nuclear option, that sounds sensible. Probably good to have that conversation, I'd still be frustrated. But better than having a wide scope.

Dan: have a dedicated TAG/google breakout on this? Where we invite Mike and ..

Ken: I would be supportive of that.

Dan: discuss in plenary. Also a question of this is being discusssed in the privacyCG, would like Tess's feedback as well. Tess might be aware more than we are of what mitigations are being discussed.

Hadley: sounds good. If it were something that were just being discussed in the privacyCG my instinct would be to let them continue to hash it out, but we're seeing other specs being built on it

Dan: we're seeing other specs referencing it as ground truth and my impression from attending the privacyCG call is that they were not very receptive to feedback.

Hadley: anywhere in ethical web principles that the user agent should serve the user? Part of my problem with this is the potential for my user agent to have advertisers needs in mind ahead of my privacy needs. That feels like an ethical thing. We hit it in priority of consistencies but I dn't know if we say anything explicitly about the role of the user agent. We do say atthe last principle UAs represent preferences on the user's behalf, respect user authority. Something there.

Dan: we could put an extra sentence in The Web is for All People or the Web Must Enhance Individuals Control and Power

Hadley: open issue

Dan: the concerning thing is the way it changes the Web's security model. And the knock-on effects of that change. The other question - what changes with FPS? is it just configuration? People are already doing this. I can go onto youtube and it'll ask me to log in and it'll just dance me over to google, oauth me, and I'm back to youtube authenticated as my google identity. This already happens. Sites are already able to do this across domains. What changes with first party sets? Is it easier? Faster? 

hadley: or without the user seeing it?

### Plenary Session

Present: Ken, Peter, Dan, Sangwhan, Lea, Tess, Rossen, Hadley

Regrets: Yves


#### [Speculation Rules](https://github.com/w3ctag/design-reviews/issues/611

[bumped to next week]

#### [Keyboard API](https://github.com/w3ctag/design-reviews/issues/507)

[bumped to next week]

#### [Eyedropper API]

[bumped to next week]


##### Breakout Rollup

###### Breakout A

Tess: we talked about webxr hit test... left feedback. .. Digitla goods .. I will write feedback.  We talked about cors rfc1918 - we decided to close.

Dan: brought to attention of Martin Thomson and Wendy Seltzer and bumped.

Tess: HTML popup... very long discussion... Lea was going to write a comment.  

Lea: our conclusion was that we need to see all parts of the proposal. Also we had some discussion of the lower level details when minutes published. 

Rossen: quick question - for an early idea what is the expectation?

Tess: It's hard to evaluate some of the details of the popup element & attribute without seeing some of the CSS details...  We want to see more of the CSS side of things.

Lea: Half the proposal isn't there.  The CSS half. They mentioned that there is a CSS proplsal coming that explains how the positioning will work but that's not there yet.

Tess: Next was subresource loading - we skipped to first party sets... Dan expressed concerns... 

Dan: we had a [response](https://github.com/w3ctag/design-reviews/issues/342#issuecomment-799709089).

Tess: skepical about this... justification is quite narrow... wanting to have a standardised mechanism for this is a sensible desire... concerns are coming out from their uses... potential of using this new mechanism to expand what is a 3rd party for cookies that is [concerning]. They have a proposal at IETF for 1st party cookies... which is based on 1st party sets...  Both proposals related... 

Ken: would orgs be able to register orgs in some place?

Dan: I think it's up the browser?

Dan: could we come to consensus on what would need to change?  Would a single point of reg be one thing -?

Tess: Like public suffix list?

Rossen: has there been discussion on what data compliance changes would be needed with this proposal? If we have a 1st party set that spans germany and china - which have clear compliance bounderies - would that change anything?

Amy: I think their response is that the sites would still be responsible for doing due dilligence and that's nothing to do with the browser - but not sure if that's true.

Rossen: Maybe...

Tess: DBaron and Dan have commented...  We've had TAG alumni chime in. We've had folks from Mozilla and Webkit comment. There has been quite a lot conversation... 

"We discussed in today's TAG call and one thing that came up is the transparency of registration of these sets when it comes to these allow-lists... how would an org register these?  Is there a scope for a standarised approach to registration / vetting / approval process?  Secondly, we discussed permissions prompts - would allowing camera acess for one site in a first party set (like instagram) then allow it for other sites in the set (such as whatsapp)?"

Dan: left above comment.

Hadley: we've set expectation with users that an origin is an origin so I don't see how we can [change this] and expect them to suddenly understand?  

Peter: Concerned about this spreading same-origin violations into other parts of the platform 


##### Breakout B

Rossen: Temporal proposal - proposed closing.    Pending Sangwhan.  

Sangwhan: Had a chat with littledan -  they [tc39] don't think our feedback is actionable.  Some of the feedback was about the complexity of the API and the fact that they use a factory pattern instead of constructors.  There's a bunch of different objects... a little complicated to use.  They weren't keen on changing the design.

Lea: we knew that when we left the feedback.

Dan: maybe we should close - *ambivalent* ? 

Peter: we were ready to close.. I think we had some open issues - they're being addressed. 

Sangwhan: I'm OK closing it... 

Lea: I'm OK closing... 

**closed**

Rossen: Media source extension web codecs...  bumped for a couple weeks.  CSS custom highlight - also bumped. We quickly looked at document.prerendering. Peter added a few feedback comments.   Last thing we looked at was webxr hit test - waiting for my feedback. My feedback remained the same but we did close it. Feedback was about the state of the spec - no examples, how it's supposed to work... 

##### Breakout C

Torgo: we did Get Installed Related Apps and closed it, since it had been proposed closed for a while.

We got a [response](https://github.com/w3ctag/design-reviews/issues/436#issuecomment-800405016) from the requester. I'll look at it later.

Limited allowed accepted file extensions / file pickers... I pinged Chris Harrelson about it, for a response. Nothing yet.

I'll bump it.

WebXR dynamic viewport scaling. They've taken our feedback on board. It came across to us because of Blink process, so I also raised it with the webXR chairs. I suggest we close it.

Rossen: did they come back to us .. with whether or not there is .. 

"What is the event mode for when a scale changes for a particular view - like a DPI change on a particular display? Not apparent that the `view` object has an event for it?"

##### Issue Triage
