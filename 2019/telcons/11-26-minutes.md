## TAG Teleconference
##### 26 November 2019

Present: Dan, Peter, Kenneth, Hadley, David, Yves

Regrets: Sangwhan, Tess

---

Agenda:

* [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @alice, @hadleybeeman
* [Serial API](https://github.com/w3ctag/design-reviews/issues/431) - @cynthia, @kenchris
* [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon
* [HTMLVideoElement.requestAnimationFrame()](https://github.com/w3ctag/design-reviews/issues/429) - @cynthia, @dbaron, @kenchris
* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris
* [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394) - @dbaron, @kenchris
* [Periodic Background Sync](https://github.com/w3ctag/design-reviews/issues/367) - @ylafon, @kenchris
* [Web Bluetooth Scanning](https://github.com/w3ctag/design-reviews/issues/333) - @cynthia, @dbaron, @torgo, @kenchris, @lknik
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman

---

### [Timed Text Markup Language (TTML2) 2nd Edition](https://github.com/w3ctag/design-reviews/issues/432) - @hober, @alice, @hadleybeeman

[pending]

### [Serial API](https://github.com/w3ctag/design-reviews/issues/431) - @cynthia, @kenchris

Ken: we got an update - haven't looked at it yet. they want to know about open / close, get and set signal, and readable / writable.

Ken: let's bump it

Dan: bump to after the f2f considering we have a lot to get through?

Ken: yes, [some description of how eatly this is and what is missing]  I told Reilly at CDS about [what is missing].  Need some descriptions of what these methods and functions are...

Dan: Will reach out to some others as well.

### [WebXR Gamepads Module](https://github.com/w3ctag/design-reviews/issues/430) - @hober, @alice, @torgo, @ylafon

bump to f2f

### [HTMLVideoElement.requestAnimationFrame()](https://github.com/w3ctag/design-reviews/issues/429) - @cynthia, @dbaron, @kenchris

David: I made some brief comments about API shape. I think Sangwhan might have had more comments about hte substance.

### [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris

Ken: we have regular payment requests -- there is an extension, payment handler. you create a payment handler app. this allows these payment handlers to handle shipping addres, etc... using the same approach as payment request. I'm OK with the idea.  Seems to mimic what they have in payment request.

Dan: What security context does the payment handler app run in?

Dan: re data minimization - 

Ken: you only get access to this when you pay for something. you have to trust it when you install it.

Dan: if you install this payment handler app - say paypal - and then you visit multiple vnedors or websites that support this payment handler - can the payment handler provider track your activity across those properties?

Ken: i think it's only instantiated when you pay for something.  the payment handler gives you a list of stored addresses.  It gives it not to the web app but to the browser UI so thr payment UI can see the addresses. Then you choose one and it gets sent to the web site.

Hadley: so you only get info (for the wbe site) during a payment?

Ken: yes.

David: the permission to see the addresses doesn't worry me too much as long as the browser UI is designed well.  I think i agree with what Kenneith said here.  The handlet probably has your address already... the consent is the point.

Ken: your payment app should know your addresses and not the web app... that's the idea.

Hadley: it would be good to make sure our assumptions are spot on.

Dan: i could write something in the issue summarizing this discussion and just ascking for confirmation.

Ken: API looks good to me.  The only think i don't understand is "enabledelegates".

Dan: what is the multi-implementation story?

### [WebSocketStream](https://github.com/w3ctag/design-reviews/issues/394) - @dbaron, @kenchris

David: Adam suggested maybe we should look at it later.  We might want to do a breakout at the f2f.

### [Periodic Background Sync](https://github.com/w3ctag/design-reviews/issues/367) - @ylafon, @kenchris

Ken: Some contraversy at TPAC - was wodnering if anything changed after TPAC

Yves: some will not implement it because of the privacy issues it will raise.

David: I think there has been a bunch of discussion in the rechartering of the serviceworkers working group.

Yves: this is not in the proposed charter.

Ken: Jake Archibald has wrote that it's blocked on privacy concerns in other engines.  

https://jakearchibald.com/2019/service-workers-tpac/

... in some cases you can use background fetch instead of background sync.

Ken: it seems like the model for backhround fetch lets you cancel ...  it seems like this ties into a UX problem - not visible to the user that it's happening.  The web is good because things don't happen unless you know it's happening.  [but this breaks this model.] 

Peter: there's a valid use case going the other direction - a PWA when you're offline - you take a photo and then when you connect you sync.

HadleY; to those who commute e.g. offline on the tube - this makes a difference.

Yves: that could be done with a going online event

David: some of the concerns people have had is how some of these APIs have let sites run script in response to events. Some of the proposals have been you can run network activity but no script.

Peter: just updating your cache?

David: here's some stuff we want to upload / download.

Dan: [quesiton of whether you need this API to do sync when you go online]

Ken: serviceworker doesn't get activated for a "go online" event

Ken: the reading app, news app, ....

Dan: FT doesn't need this and they do it.

Ken: yeah but a lot of data , especially when roaming...

Hadley: podcast apps do this

Peter: workaround is a push notification - silent push - that triggers the update

Ken: All push notifications need to show UI, there are no silent push notifications

Peter: worth asking what the feedback from the origin trial has been.... Can someone write that query back to them?

### [Web Bluetooth Scanning](https://github.com/w3ctag/design-reviews/issues/333) - @cynthia, @dbaron, @torgo, @kenchris, @lknik

Dan: No feedback. I suggest we close this and ask them to re-open when they want to come back into our agenda.

Dan: I will write feedback and close this unsatisfied.

### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @dbaron, @torgo, @hadleybeeman

Hadley: complications - we discussed tradeoffs and knock-on effects. We agreed they would expand on these issues in the explainer which has not really been done. This is largely where it was. they did add a ToC which we asked for. doesn't encapuslate the richness of our discussion. We had concerns - not reflected. David commented - expanding on his concern that the asusmption is that one site knows more about the language preference than the browser, this promotes a walled garden view of the web.  I understood they had made  achange to make it more browser-centric.

David: it was always a hint to the browser to translate that site into the language specificed.

Hadley: so the browser must do something sensible with that?

David: if the search engine sends to the browser that the user wants this translated into X then maybe the browser should ask "is this your prefered language"?

Hadley: what would you like them to do with it?  ... permisison prompt when href tranfstalte is encountered from non-trusted sites.  how much belongs in the spec vs implementation specific. 

David: i think it's worth mentioning that idea informatively.

Hadley: I don't see most of what we wanted in the explainer. we talked about the permission model and the danegrs of giving blanked protections.  They have added one line to the answer to the privacy & security questionnaire.  I feel the explainer doesn't capture the thought process that went into shaping htis proposal - so UAs can't make sensible decisions about what the dangers are.  So i feel we have put a lot into this - open for a year  - 2 calls on it - and a long issue thread - don't feel we can go further.

Dan: We should close ?

David: we should say something like "we were expecting a bit more change to the explainer" - one last chance.  I could craft that.

OK
