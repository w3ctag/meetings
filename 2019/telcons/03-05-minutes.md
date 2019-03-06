## TAG Teleconference
##### 05 March 2019

Present: Dan, David, Tess, Alice, Peter, Yves, Hadley, Kenneth

Guest: Dave Tapuska

Regrets:

---

Agenda:

* [User Activation API](https://github.com/w3ctag/design-reviews/issues/300) with special guest Dave Tapuska - @hober, @dbaron, @hadleybeeman

* [First-Party Sets](https://github.com/w3ctag/design-reviews/issues/342) - @dbaron, @torgo
* [Feature policy control over sandbox features](https://github.com/w3ctag/design-reviews/issues/339) - @dbaron, @torgo
* [IntersectionObserver V2](https://github.com/w3ctag/design-reviews/issues/328) - @slightlyoff, @dbaron
* [Event Timing API](https://github.com/w3ctag/design-reviews/issues/324) - @dbaron, @travisleithead
* [CSS Properties and Values API Level 1](https://github.com/w3ctag/design-reviews/issues/318) - @hober, @alice, @dbaron
* [Base used to resolve relative URIs to absolute URIs in HTML5 data-blocks](https://github.com/w3ctag/design-reviews/issues/312) - @hober, @slightlyoff, @hadleybeeman
* [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301) - @torgo, @hadleybeeman
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @slightlyoff, @torgo, @ylafon
* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @slightlyoff, @hadleybeeman, @travisleithead, @plinss
* [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) - @slightlyoff, @dbaron
* [Task Scheduling](https://github.com/w3ctag/design-reviews/issues/72) - @dbaron
* [Clear Site Data](https://github.com/w3ctag/design-reviews/issues/62) - @hober
* [The web platform needs a service discovery mechanism](https://github.com/w3ctag/design-reviews/issues/240) - @cynthia, @hadleybeeman, @plinss


---
### [User Activation API](https://github.com/w3ctag/design-reviews/issues/300)

dtapuska: (missed start)

...workarounds used today due to lack of this API:
 - ?
 - audio tag
 - clipboard

...in chrome proposed this user inetractibe 

...don't want to tie it to permissions

...don't want to expose timestamp of last interaction; security issues

... some of this ties to other TAG requests, e.g., User Activation v2.  This API applies to both old model and new model.

dbaron: more OK with this given those uses you presented -- but still worried about people misusing it for browser-specific permissions issues

peter: this would be useful to me for (reasons missed)

tess: Good to get additional context.  Was thinking about autoplay case; was just discussing exposing whether autoplay would be allowed.  Was worried about same thing as David; reasonably comfortable now.

dka: That other things sounds worrying:  "Sorry, this page doesn't work unless you allow autoplay".

tess: High level concern is page assuming particular permission model and using this API to make decisions about what to do -- but that's not what this API is for.  Shouldn't be inferring what will happen with permissions based on these 2 bits of information; should just use the permissions API.

dka: Is that flowchart something that could be in the explainer?

dtapuska: I can edit that in if that's your feedback.

dka: We're keen to close the issue.  Thanks for listening to our feedback.

hadley: closing seems reasonable; would be nice to check in again further on.

The flow chart: https://dtapuska.github.io/useractivation/example.html

### [hrefTranslate attribute](https://github.com/w3ctag/design-reviews/issues/301)

dka: where are we?

dtapuska: Search sometimes redirects pages to server-side translation.  That misses out on a whole lot of dynmaic pages. Client-side translation exists in some browsers; produces better experience.  Want to avoid server-side translation if we can.  Can detect based on prototype chain.  Was some discussion in the github issue about whether we should be doing this, whether you know the locale.  The server is returning the page, and putting text there and directing you to the server-side translation, so user settings don't come into pplay.  The server is controlling things.  So I don't think we're taking anything away from the user; allowing use cases that weren't possible before.

hadley: what concerned me when we last looked is that the model of the web is that user gets to control the experience through teh user-agent.  Thus the client-server relationship is between the user and the server.  This looks like puts a different server in control and takes power away from the user.  Specific example?

dtapuska: Example was searching in Google search, searching for a german news site.  Ends up with translate attribute that redirects to translate.google.com with url that you were loading.  The page you're interacting with is responsible for the next links; that's what we're trying to cnotrol.  What's happening with server side translation is that half the page isn't translated (javascript).

dka: the underlying assumption is that the referring site knows something the browser doesn't know?  Doesn't the browser send header with its language preferences?  What if the server gets two signals that are conflicting?  Is the current client-side signal not adequate?

dtapuska: The client-side signal won't translate.  What we're after is that search can return pages in any language.  If you think about the web from the point of view of non-English, when much of the web is in English.  We're trying to enhance the web for that opportunity.  If a language is in your accept-language, the server's probably not going to set the hrefTranslate attribute.

hadley: I understand you want the UX in the translate mode to work smoothly; still confused about why to do that in the page rather than in the browser.

dtapuska: in the referrer page, would use hrefTranslate and original href instead of setting href to translate.bing.com?url=... .  And translation then works better because it's client-side rather than server-side.

hadley: wouldn't make more sense to do that in http rather than in the referring page?

tess: e.g., browser UI that begins the auto-translating browsing mode.

dka: I still don't understand why accept-language header isn't sufficient.  I click link to Der Spiegel, why doesn't Der Spiegel ask me to translate the content to English through its use of Google Translate?

dtapuska: You could handle those pages using accept-language, but a lot of the web doesn't have the resources to deliver that content in different languages.

hadley: Would it make more sense... if you want it to all run in the client... to build a version of translate into the browser?

dtapuska: That's what this is -- that's the client-side translation that occurs.

... it allows the referrer page to serve pages that don't match the language that you can read.

tess: given that the idea is having a browser feature that does translation, presumably with UI in the browser to activate this mode... why does there have to be any difference in the web content at all?  Why do I need to cause the translation to happen in my page content?  Why does content have to change at all?

dtapuska: mainly, problems with mixed content modes.  If you combine language, you get into wierd scenarios where you don't know if you should translate.  So we took the approach of being explicit.

tess: Isn't the user turning the feature on the explicit signal?

dtapuska: I'd assume the feature would be on be default.  That's the way it works in Chrome today -- translate is on by default but opt-out.

hadley: Since many users aren't native English speakers or don't want content in English, would you imagine this being included on every href since we don't know what users will need translated?

dtapuska: What search team was after was how to make translate attribute work better.  I don't think it's applicable to every single href.  Not a magical attribute you'd add everywhere.

hadley: It does a bit... it makes it feel it's trying to solve a problem for a particular kind of user that's not about the web itself but about how they expeirence the web -- seems to be the kind of thing that lives in the user agent.

dtapuksa: This attribute lies between the HTML and the user-agent.  The user agent looks at this and decides to do something different... like an accessibility thing where you could do something different at the user agent level.

hadley: not more efficient to just have the UA translate things if the user wants them translated?

dtapuska: comes down to that we could get it wrong sometimes

tess: the browser can get it wrong, so sites that link to other sites should change their content to work around it?

tess: so today if your browser backend for autottranslation... what if one browser has a good result and the other browser doesn't.  How do you write the page?

dka: One thing I'd like to see is how this works with any translation service, any search provider, and any browser.  I'm hearing a lot about how this works with Google ones.

dtapuska: The attribute is feature-detectable.  But Tess's problem of whether one browser returns a good result or not is certainly a problem.  The referrer page has to pick a translation service...

tess: But with the attribute the referrer page doesn't choose a translation service, that's now a browser decision.

dtapuksa: I don't have a good answer there.

... Previously, if the page wanted translation, they were choosing a translation service that would be good.  I'd imagine if it were bad in some browsers they'd have to use hrefTranslate in only some browsers.

tess: Since it's an attribute it's feature detectible... so if writing HTML and most browsers don't have this feature... if I'm writing HTML with translate.google.com?url=... for browsers that don't support hrefTranslate, won't the hrefTranslate then translate it twice if you add it.  The fallback story is strange; you have to do content-rewriting.

dtapuksa: The primary target of this is machine-generated pages, not handwritten HTML.

kenneth: how does this work when sharing URLs?  This seems like it would be very confusing to people.

dtapuksa: Hopefully in those cases the translation engine pops up and solves it.  This is mainly avoiding the roadblock of having users click "I want to translate this page"

Kenneth: so if I'm on a page that's already translated I probably want those translated as well?

dka: Isn't there a social value to the user knowing that the text has been translated and wasn't written as-is by the author?  Translation is imperfect.  Can get the gist.  If I found myself reading broken English and didn't know the pgage hade been translated, is that the experience I want?  Shouldn't the user know it's been translate.

dtapuksa: I think there's a user-agent point of view -- UA could indicate that pages are translated in all sorts of fashions.  It's up to the UA to provide that signal.  That said, people may key off URL being translate.....com?url=...

dka: Feel like this has been a good discussion; sorry if you're hearing negativity.

dtapuksa: This is a proposal, what we wanted to do was experiment with this and determine whether it gets better engagement.  That's the state of the world for this feature.  Trying to run experiments with this attribute.  See if it's a good/bad idea.  Obviously want to get TAG feedback on the approach we prototyped.

dka: Would also be good to get feedback from other search providers and other translation service providers.

dtapuska: Do have feedback from Microsoft, not from others.  If you have contacts, happy to reach out.

dka: Leave this open in a monitoring sense, and hear back about the experiment?

dtapuska: I'll ping the issue when we have experiment feedback.
