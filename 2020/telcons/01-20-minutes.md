## W3C TAG Breakout A - 20 Jan 2020

### Breakout A (Europe / US) - [2020-01-20](https://www.timeanddate.com/worldclock/converter.html?iso=20200120T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### Pre

#### Agenda

* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris
* [UA String deprecation proposal](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/-2JIRNMWJ7s/yHe4tQNLCgAJ) - do we have anything to say as TAG on this?

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Dan: it looks like Ken issued some changes to the explainer that addrressed some of my feedback from last time. 

Moving this topic to breakout C

#### [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris

Moving this topic to breakout C

#### [UA String deprecation proposal](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/-2JIRNMWJ7s/yHe4tQNLCgAJ) - do we have anything to say as TAG on this?

Tess: When we (WebKit) tried to completely freeze the UA string, we found we had to unfreeze parts of it for compat. I think we can be supportive of "mostly" freezing the UA string... You can't freeze everything.  Evaluating the client hints UA stuff is a separate question.

From the I2D:

> Safari: Shipped to some extent. Safari has attempted to completely freeze the UA string in the past, without providing an alternative mechanism. That got a lot of pushback, which resulted in somewhat reverting that decision. Nowadays, their UA string seems frozen, other than updates to the OS version and the browser major version.

Dan: maybe we should invite TAG review on that particular issue...

Dan: My concern is that it's something that impacts all browsers and a lot of corners of the web that rely on UA string.  Some example feeebdack f

Yves: we did some experiments with w3.org with upgrade-insecure-requests.  we had to rely on UA string for some older browser versions that don't allow for this...  the fact that it was done at the server level without even reaching the JS stack... UA detection is important - before...

Hadley: this seems wide ranging - lots of potential knock-on effects  - acccessibility, privacy, changes the construct the user uses... Complications. It's [the UA string] isn't the best thing in how the web works but I havent seen eniugh research about how this isn't going to break everything.

Dan: I will ask Yoav to seek a TAG review and we can continue discussion on this point... 

Hadley: can we bring in Léonie?  She published a blog post in 2004 - not in favour of detecing a screen reader.  Would like to make sure we surface any accessibility issues.

## W3C TAG Breakout C - 21 Jan 2020

### Breakout C (APAC / Europe) - [2020-01-21](https://www.timeanddate.com/worldclock/converter.html?iso=20200121T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### Agenda

* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris
* [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @alice, @torgo, @ylafon

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Dan: feels like our feedback has been taken on board... maybe close?

David: might be some things from the larger disucssion - Mozilla standards position, etc... Security & privacy concerns.  Not sure how much it should be the TAG's job to dig into those.

Tess: has PING done a review?  if there are outstanding privacy concerns we could ask them to do a review, or suggest that they ask PING to do a review.

David: i suspect not...

[linking these discussions in to our issue]

David: i have seen a concern that looked like "you can use NFC to do the same thing you can do with form posts and xhr..." i'm skeptical on pushing something back on something with security issues when those issues are common to other web technologies.

Dan: is writing to a NFC tag restricted to a domain?

David: is it more unexpected for the web to be able to write to an NFC tag?

Dan: we need ken to answer these...

#### [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris

David: i think this is close to being able to close....

Dan: should we "propose close" this and close it in the plenary?

David: i need to go throuhg the responses in more detail but probably.

#### [ads.txt](https://github.com/w3ctag/design-reviews/issues/201) - @alice, @torgo, @ylafon

Alice: my thoughts: this has been open a long time. Kenneth raised - is this in use? The last 3 comments we haven't heard feedback on. 

Yves: it would be good to have a group taking care of this.  Considering they didn't take our feedback into their revised spec, we should probably drop it.  

Dan: propsosal is to close with "not satisfied" and make some specific recommendations? Those might be : do this as a real standards group...  Isn't there an advertising community group?

Tess: there is a business group.

Dan: let's agree this in plenary.

## W3C TAG Plenary - 22 Jan 2020

Present: Peter, Dan, Alice, Yves

Regrets: Tess, David, Hadley, Sangwhan, Lukasz, Rossen

#### Agenda

### ads.txt - proposal to close

Alice: someone in google is working on it.  I still need to follow up...

[agreed to keep it open one more week]

### webnfc - proposal to close

Dan: we may be ready to close, with a recommendation that PING also do a review, but we may need to wait for Ken.

Yves: I think it's betetr to wait for Ken.

[agreed to keep it open one more week]

### UA Strng

[still in progress]

### planning for non-issues week

we agreed to work on design principles.

Dan: We discussed having a week on updating the design principles document https://w3ctag.github.io/design-principles/ on the first week of Feb. We will triage out the open issues in the plenary on the previous week. Please everyone have a read through the document and cast your eyes :eyes: over the open issues https://github.com/w3ctag/design-principles/issues?page=1&q=is%3Aissue+is%3Aopen
