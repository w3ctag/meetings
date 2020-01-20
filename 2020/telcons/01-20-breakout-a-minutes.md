## W3C TAG Breakout A - 20 Jan 2020

### Breakout A (Europe / US) - [2020-01-20](https://www.timeanddate.com/worldclock/converter.html?iso=20200120T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

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