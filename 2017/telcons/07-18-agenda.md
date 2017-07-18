### TAG Teleconference – 18 July 2017 ; 15:00 UTC

<table>
<tr><td> San Francisco (U.S.A. - California) <td> Wednesday, 18 July 2017 <td> 08:00 PDT <td> UTC-7 hours
<tr><td> Boston (U.S.A. - Massachusetts) <td> Wednesday, 18 July 2017 <td> 11:00 EDT <td> UTC-4 hours
<tr><td> London (United Kingdom - England) <td> Wednesday, 18 July 2017 <td> 16:00 BST <td> UTC+1 hours
<tr><td> Paris (France) <td> Wednesday, 18 July 2017 <td> 17:00 CEST <td> UTC+2 hours
<tr><td> Tokyo (Japan) <td> Thursday, 19 July 2017 <td> 00:00 JST <td> UTC+9 hours
<tr><td> Corresponding UTC (GMT) <td> Wednesday, 18 July 2017 <td colspan=2> 15:00 UTC
</table>

### Call Agenda

* Malte joining as special guest to discuss AMP
* Any updates regarding next week's f2f

Followups:
* [Spec style/structure checklist](https://github.com/w3ctag/design-reviews/issues/136) - Alex
* Finalize dates/location of [September meeting](https://github.com/w3ctag/meetings/tree/gh-pages/2017/09-nice)

Triage:
* not this call

### Logistics

Chair: Peter

Scribe: ?

IRC : irc.w3.org / #tagmem

Trying https://appear.in/w3ctagpro first then going to https://meet.jit.si/w3ctag if that doesn't work

*Please note*: this meeting is open to TAG members and invited guests. If you would like to participate, please email the chairs.

### Minutes

```
Minutes for W3C TAG Teleconference - 18 July 2017

Present: Dan, Peter, Yves, Andrew, David, Malte Ubl (guest), Hadley, Sangwhan, Alex
Chair: Peter
Special Guests: Malte to discuss AMP
Scribe: Andrew, David

# AMP

<Dan introduces the TAG and its function>
Dan: Links on twitter, apple.news etc.
Malte: Whenever you have share button, the original URL should be the
  one shared.  AMP recommends platforms do this.
... in Google's native apps, the canonical URLs are shared
... if the app has the ability to do the right thing, it should do the right thing
... we do the best thing supported by the capabilities of the platform
  [ dbaron side comment: similar things with m.* URLs?  Also risks of
    "canonical URL" mechanisms, esp. for browsers? ]
Dan: primary driver? Mobile web performance?  Same URL across devices?
Malte: the name is really to convince people to pay attention
... UX in general is the more direct goal
... Google has been trying to get people to make pages fast
... even internally people didn't do it well
... a more prescriptive approach worked
... empowers web developers to say no
... we see urgency because of threat from closed publishing platforms
... this is competitive with native alternatives
... "non-traditional navigation" is common in apps, swiping, endless
  scrolling etc.  We wanted to built that.
... wanted to retain publisher control over monetization (ads, paywalls)
Andrew: There's this misdirection thing that Dan's covered.  I feel like
  we haven't gotten to the root of the "one Web" issue.  We had m., now we
  have amp..  Does that problem go away at some point?
Malte: What we now recommend is that AMP is a great technology for
  canonical use.  Show AMP page on first use, and our recommendation is to
  then install a service worker that can provide a better experience for
  repeat visitors.  This isn't necessarily something that everyone has
  adopted.
... Some people do amp. Mike West proposed a way to fix it last week
  (without knowing to have done so)  because we don't allow iframing of
  same origin content (?).  Want to iframe ads on www origins.  We don't
  want people to have same origin iframes to avoid JS access to the
  primary frame which wouldn't work on different origins.  The ability to
  have iframes that can't mess with the parent -- proposal for
  'document.domain = null' -- to say "nothing has my origin" at runtime.
  Promising for this.  Though only addresses different origin, not
  necessarily different URL.
Malte: You have a URL -- if no service worker, you get the AMP document.
  If you have a SW, you can have a different experience on the same URL
  space. 
Andrew: Only works as long as there's only one "AMP" standard.
Alex: I think there's a point often lost here.  There are 2 origins in
  play. There's the origin that published the AMP content, and then the
  3rd party CDN (not a traditional CDN -- just for root level documents).
  The AMP cache today doesn't get itself into doing what a CDN does.
  Doesn't do traffic proxying for the root origin.  Thus URLs loaded into
  an AMP viewer, e.g., from google search, are different URL.  So question
  of how true is <link rel=canonical>?   ... nontraditional scrolling.  To
  what extent is it good or bad for the web that amp caches create and
  promote URLs for content that are not legitimate.
Dan: One thing we've been worried about is this issue where, somebody
  views an article, and according to the browser, the origin is
  google.com.  But the article is actually coming from some other website.
  Is that part of this issue, or separate?
Malte: On google, 3 urls involved in an AMP document.  Publisher URL
  (not serving directly), AMP cache URL, and the URL that's displayed in
  the browser (has to be google.com).  Can't be a browser navigation.
  Actual document displayed on its cache origin.  But no way to maintain
  same implementation for prerendering, swiping, etc., without keeping the
  same top level origin.
Alex: I think talking about extent to which AMP takes up large portion
  of user's consumption of Web content.  Significant portion of Web's
  traffic -- different from user intentionally going and using feed.ly.
  Is this minting a pattern where URLs are no longer canonical for
  content?
Dan: What if there's additional security context associated with that
  piece of content.  What if it's requesting location?
Alex: Many things we can't provide access to AMP content to do because
  it's not running on its origin.  The tracking thing in ads is one side
  of it.  But we can't offer progressive web app installation, or opt-in
  for push, or store user data, or make real apps.  So end up in uncanny
  valley ... parallel universe.  To what extent is parallel universe
  impinging on real one?
Malte: All good questions.  If I could have a wish, I'd want to display
  the correct origin.  Would like to be able to make CORS request to ask
  permission to do a cross-origin pushState, or promote an iframe to be
  toplevel window at runtime.  A number of primitives with different
  tradeoffs.  Should this type of interaction be supported by web
  platform?  But given that... should it then be left only to native apps?
  If you go to the Google iOS app, this just works, right?
Alex: ... the google iOS app is a browser.  But doesn't share any state
  with Safari.
Malte: The AMP documents still not served from displayed origin --
  permissions issues.  From primary user experience pov, a better
  experience.  Should it be possible to build this on the Web?  We tried
  to build it anyway.  I no longer accept that I can't do things -- we
  built it using the primitives we have.
Dan: Next question in my mind:  what can the web platform do to
  ameliorate some of these issues, so we can solve the same issues without
  the problems?  I agree these are pressing issues (native vs web), and a
  fight where I feel we're turning a corner.  I think we're seeing
  groundswell in browser-based applications.  How can we encourage the
  development of web standards that ameliorate the issues?
Andrew: I noticed Paul Backaus posted a comment to WICG yesterday --
  worth looking at.
  https://discourse.wicg.io/t/pre-render-meets-feature-policy-alternative-to-amp/2173/5
Malte: One technology that's promising in solving... Alex mentioned way
  the AMP cache works -- different from traditional CDNs which are bound
  to referring platform rather than destination platform, at cost of
  changing the origin.  Relatively obvious medium-term technology that
  would allow this type of delivery model without changing origins is web
  packaging.  Web packaging doesn't do the nontraditional navigation.
  iframe issue still separate.  For vast majority of AMP interaction on
  google, web packaging might be good tradeoff.  Produces right origins
  with right performance -- tradeoff with advantages that iframe based
  rendering gives.  But still only a partial solution.  Could still try to
  come up with a good proposal for the other problem.
Andrew: I'd like to move on to other things.  Question of popularity is
  important.  Difficult to answer:  how ??? popular is AMP?  Can we look
  at uptake, or should a certain part of adoption of AMP be considered  a
  necessary step by publishers that they may not be taking for purely
  technical reasons?
Malte: Whether popularity is relevant?  Original question was about
  standardization.  Standardization runs into barriers, for good reasons.
  Everything you standardize about it, you'd put application layer things
  into the platform.  Do you want to standardize AMP carousel web
  component?  Probably not.  There are some promising things we're eager
  to drive, e.g., feature policy.  I'm excited about forbidding iframes
  from making sync XHR... new primitive.  But I don't know what it means
  to standardize AMP, within the layering requirements of the Web.
Alex: When we add things to the platform, things don't necessary layer.
  When we add apis that do what JS libraries did, they're in a different
  layer.
Malte: An interesting property of AMP is that it's inert before user
  action -- so allows prerendering, without side effects (e.g., ad
  tracking).  That's impossible to build with general web content.
  Interesting to see if that could be standardized.  I'd be excited to
  participate in that.  Should be concrete about what it would mean to
  standardize AMP, and which parts.
Andrew: Prompt for that question is really... 2 questions here: (1) what
  do you standardize and (2) motivations for standardizing it.  Thigs like
  Chrome status will use sentiment as guide to priorities for
  implementing.  That's difficult to judge for AMP.  Tightly bound set of
  stuff with many moving parts.
Malte: I think it would help to pick out concrete things.  We're excited
  about it.  Make new primitives that can make horrible hack in AMP go
  away, or something bad like URLs be fixable.  We'd be very excited.
  Higher priority to add primitives rather than things higher up the
  stack.
Andrew: Another issue about trust.  Content trust signals provided by
  the platform itself are insufficient.  AMP provides an opportunity to
  improve them but doesn't at the moment.  Is that something we can do in
  the platform itself?  Could it be part of a standardization effort?
  Build standard-based provenance and trustworthiness.
Malte: Think it's the last thing to standardize.  No one found a good
  way to do it yet.  If you look at newspapers -- they're a proprietary
  platform with editors, etc.  Google might go with objective facts, e.g.,
  pulitzer prizes.  Might be a browser-level feature.  If referring
  platform can provide context about what it's linking to, that's an
  opportunity to give additional information.  Everyone agrees there's a
  problem, but I don't have a solution, so can't standardize anything.
  But worth trying different things, see if they help consumers.
Andrew: Last thing on my mind is role of the cache.  What's the value of
  an AMP cache that isn't the google one?  I know cloudflare has built a
  cache.  I work for a CDN, we've been approached.  I don't understand
  value of building an AMP cache ... value for something that isn't the
  google AMP carousel viewer?
Malte: Our idea is you move responsibility to referring platform.  That
  addresses issues with centralization.  The value of building additional
  caches, say, if bing wants to make an AMP experience and control
  delivery experience, you can do so.
Andrew: So were there to be other AMP viewers, it would make sense for
  them to roll their own cache, or use a CDN.
Malte: There's the option of using ours, or cloudflare's, or building
  their own?
Andrew: Aware of any other AMP client/viewers other than Google?
Malte: Many.  Some confidential.  We've open-sourced the infrastructure
  to build web viewer.  And in process of open sourcing infrastructure to
  build iOS and Android viewers.
Andrew: I want to probe question of how this addresses/attacks
  decentralization.  Instead of addressing... burns in largest traffic
  producers without changing how publishers send content to users.
  Decentralization doesn't mean more referring platforms ... it means
  publishers can maintain control from their own origin.  ???  That seems
  to be a major asterisk over that.
Andrew: Question:  IS AMP acting to centralize the Web?
Malte: Easier to answer the direct question.  AMP has decentralized
  hosting, different from competing platforms like flipboard, apple news,
  facebook instant articles.  When a cache goes down, AMP documents still
  work, although the cache URLs might not work. Having said that, we don't
  like seeing cache URLs everywhere -- would like to not do that.  Web
  packaging is most promising technology to change delivery mechanism
  without impacting origins.  I think there's a few interesting... thought
  about this a lot when designing the system.  You mentioned apple news
  links, url shorteners in general.  Possibility of proliferating, but
  then going down in future.  Make a URL format redirectable without going
  through database?  AMP cache must pledge to maintain URL space forever.
  Something like archive.org could take over running of an amp cache.
  Designed to be resilient in long term, work around negative effects as
  much as possible.
Alex: In defense of AMP, worth noting other alternatives -- things like
  fb instant articles, apple news -- don't attempt to traffic in URLs.
Andrew: though counterargument is that those aren't on the web.
Alex: Malte's point is that they're attempting to compete, as the web,
  against these other platforms.
Dan: One thing I'd like to point out:  there've been good examples,
  e.g., FT, doing nonstandard navigation -- some things have been solved
  in other ways.  Saying we need AMP to do nonstandard navigation to
  display articles immediately
Alex: In FT app, you're looking at content from a single publisher.
  You're browsing ft content; platform gives FT power to do that.  Malte
  trying to mash up multiple publishers content, that's different and not
  supported well today on the platform.
Andrew: To what extent is is the content the words and pictures on the
  page, vs to what extent is the content the UI and the ???.  If a
  publisher creates a complex webpage that's not currently packagable by
  AMP.  That's a call AMP team has made about what counts as content and
  what counts as function/delivery that AMP chooses to take control of.
Malte: We specifically tried not to solve all problems.  We limited
  problem space to one we could address.
Dan: If we're looking to wrap up:  want to thank Malte for joining us.
  One takeaway:  heard web packaging mentioned a bunch of times -- was
  initiated in TAG, now elsewhere.  TAG has had interest.  I think could
  put some energy behind some efforts to standardize some of these
  primitives, to solve these issues.  If we can get to a place where some
  of these issues around trust, sharing, etc., can be addressed, then
  we'll be in a much better place.
Peter: We often talk about competition between web and native.  People
  often try to recreate the native experience on the web -- sometimes
  throws away benefits of web.  Want to leverage URLs, origin model, etc.,
  and get those benefits.  Bringing more primitives will help this without
  throwing away baby with the bathwater.  We can bring up these issues
  across multiple working groups.  We can help create new initiatives --
  if there are things we can do to help there, please bring that to us.
Malte: Thanks for having me; happy to jump in and answer questions.
  Right next step is to identify which primitives are the right path
  forward.  Definitely properties of the Web we shouldn't throw away.
Hadley: I also love that you're doing this -- the problems you're trying
  to solve are critical to the success of the Web.  Some of this we'll
  only get through by trying to build new things.
```

