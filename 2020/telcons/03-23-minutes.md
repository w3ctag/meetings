## TAG Teleconference
##### 23-25 March 2020

---

## Agenda:

### Breakout A (Europe / US) - [2020-03-23](https://www.timeanddate.com/worldclock/converter.html?iso=20200323T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Rossen, Peter, Kenneth, Dan, Yves, David

Regrets: Tess

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

David: bump a week?

Peter: 2 weeks.

#### [Origin isolation](https://github.com/w3ctag/design-reviews/issues/464) - @hober, @hadleybeeman, @atanassov

Rossen: ... want to do a deeper review of this.  The explainer is really good. Goes into some fairly detailed examples and overall proposal of the feature. We should certainly do our part and provide good feedback here. The work done by the team is solid. I don't know that we're going to have a lot to offer – but i want to take time to digest.

Peter: bump how long?

Rossen: I would give it a couple of weeks.

[moved to April 6]

#### [URL Protocol Handler Registration for PWAs](https://github.com/w3ctag/design-reviews/issues/482) - @hober, @dbaron, @torgo, @kenchris

Kenneth: looked at this and it seems sensible. Similar to register protocol handler but in the web app manifest... all can be done at "install" time. Same mitigation that exists in `registerProtocolHandler`. Not all protocols.  Thinking about extending that a bit.  Registering a scheme.. associated a title + and icon.. 

Dan: Tess said " could this be syntactic sugar on top of `registerProtocolHandler`"?

Ken: not totally – eg you can't associated an icon. 

peter: you can have a tittle with `registerProtocolHandler`. I'd like to see the two things be more integrated. Maybe turn it to an options dictionary.

Ken: yes –  also I'm worried that people will register a handler and use an icon and title that makes it look like another application. Something like that could be solved in the UI... 

Yves: my comment last week was more about the use case section - e.g. for powerpoint. For magnet it's OK because it's a protocol to retrieve something. But web+powerpoint is a media type – there should be an option for what you encounter when you use a media type.

Ken: already another proposal for file extensions .. mime types vs file extensions discussion...

Peter: the thing about mime type is that you don't know what the content type is before you fetch it.

Yves: if it's in the link header you can ...

Ken: [file handling](https://github.com/WICG/file-handling/blob/master/explainer.md) proposal ([#371](https://github.com/w3ctag/design-reviews/issues/371)). Instead of protocol handlers you have file handlers... so why are these not working the same way?  Action thing instead of a URL. No icon associated with the file handler – should there be?  Maybe these could just be "handlers" ...

Dan: feels like it could be confusing for the developer – different ways to do similar things. 

Yves: if you're abusing media types and the way you're doing things based on content then it's another way of doing things differently from the current way of the web.

David: the file handling proposal is tied to the native filesystem API - lets the web page read and write files. Some concerns about native filesystem.

Ken: I still think the APIs could be similar. 

Yves: [official URI scheme](https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml) – doesn't contain powerpoint, etc...

Peter: i noticed that `registerProtocolHandler` contains a [list of safe schemes](https://html.spec.whatwg.org/multipage/system-state.html#custom-handlers:safelisted-scheme). That seems like something that should be harmonized or at least explained. Like to see some explanation of how this interacts with `registerProtocolHandler`.

Ken: also what happens if the manifest is updated and they add another one.

Peter: I'd also like to see the icon backported into `registerProtocolHandler`.

Ken: the UI should mitigate against misuse of this to confuse users.

David: that might involve something like showing the origin.

Peter: related topic: the list of safe listed schemes is being managed in the HTML spec... This should be an external registry. 

Dan: isn't this encompassed in the evergreen /ever blue / ever teal / whatever color we are using proposal?

David: living standards have some of the advantages of registries too.

Rossen: will summarize on the github.

#### [PWA Change logs](https://github.com/w3ctag/design-reviews/issues/484) - @torgo, @kenchris

Ken: I looked at that as well. It's kind of like you add to a webapp manifest a new entry and link to a resource - like a web site or could be "something else." I like the idea of one place to find the release notes. But if it's just html then it could look different from app to app. Maybe something like markdown could make more sense in this case. It might also be that you want to show the history in different formats. Most app stores just allow you to give it as text.

Dan: [in defence of having different look and feel for different webapp release notes]

Ken: but you want to have it in a trusted UI – you wouldn't want ads in it, etc...

Rossen: how is this different from other places where we use HTML?

Dan: some value in having uniform formatting rather than turning release notes into advertisements

Rossen: animated example at https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/VersionHistory/user-experience.gif

Ken: what i didn't understand from that GIF - is it trusted UI or not. At a minimum people should be able to provide different formats. Web site, markdown?

Rossen: I'm not sure why the full richness of html would be required here. If you compare this to a lot of the extension model type UIs, this is the closest I would compare with. I wouldn't compare it to native apps. Perhaps something like markdown would be sufficient here. 

Ken: for accessibility purposes it might make sense that it works across ...

Rossen: Do we make the web apps more web like or more app like?  From design review PoV the overall feature makes sense and having the mechanism of providing back the version history in a well formed format is a great addition to PWAs. I'm less keen on the details of the actual format.

Ken: but html isn't a "standardized format"-  it's very flexible.

Dan: shall we push it back to them and ask them to consider the issues we've raised?

Rossen: i don't see a solid justification in the explainer itself.

Ken: I don't like they dictionary is called Resource – too generic.

Ken: also - if it's a standardized format like markdown you could implement search and make sure it works... 

[debate between low-formatting change log and using a HTML web resource]

Ken: what about sharing a change log with my friends? (could always add a html link in addition to markdown and have a link to open it in the browser for easy reading and sharing)

Dan: I will write up some notes based on this conversation.

#### Breakout B (US / APAC) - [2020-03-23](https://www.timeanddate.com/worldclock/converter.html?iso=20200323T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### [Intersection Observer review](https://github.com/w3ctag/design-reviews/issues/197) - @dbaron

Rossen: This is a shipped feature... what's remaining. 

David: Specifying what's actually shipped and if it is interoperable. My concern was that the HTML event loop spec is not specified clearly enough and not very interoperable. So then, how intersection observer fits into all of this. I recall writing one event loop test and that failed everywhere. 
Don't think keeping the issue open is going to do anything else other than nag me to look at it. 

Peter: Specifying the event loop has been a long time coming :) and not there still.

Rossen: So what's really remaining for TAG here?

David: I'm OK closing this one and file a separate issue for tracking the specific dependencies between intersection observer and the event loop.

#### [Delegated Ink Trail](https://github.com/w3ctag/design-reviews/issues/473) - @dbaron, @atanassov

Rossen: I moved the issue out by couple of weeks (to April 6) as the feature authors are actively addressing the feedback provided by David and myself during last round of reviews in Wellington.

### Breakout C (APAC / Europe) - [2020-03-24](https://www.timeanddate.com/worldclock/converter.html?iso=20200324T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

Alice: Still haven't written up a comment.

[bumped]

#### [Service Worker Scope Pattern Matching explainer](https://github.com/w3ctag/design-reviews/issues/417) - @cynthia, @torgo, @kenchris

Ken: No updates on the review. Bumped 2 weeks.

#### [Title Bar Customization for PWAs](https://github.com/w3ctag/design-reviews/issues/481) - @alice, @torgo, @kenchris, @plinss

Ken: Haven't heard anything back on our questions.

... Thought Rossen was going to talk to the team?

Ken: not just about where not to draw... about how to drag the window around... New display modifier in the webapp manifest for how it would look, new api for bounding rects and states... Environment variables.. system drag region...  So lots of stuff.  Should we look at each of these in separation?

Dan: so each of these becomes a separate proposal?

Ken: yes, like something related to CSS needs to go to the CSS working group... Also there should be some restrictions on drag regions.. CSS environment variables could be fine ... also used for dual screen API... Right names, right properties... using `left` and `right` – does that work for accessibility?  Maybe `start` and `end` might make more sense?

#### [Scheming Cookies](https://github.com/w3ctag/design-reviews/issues/483) - @torgo, @ylafon

Ken: definitely support an incremental approach.

Dan: totally agree. we also need to ensure it's subject to wide review – TAG can help.

Ken: this seems very sensible.  Gives more incentive to move to https.

Dan: agreed.

Ken: We talked about schemes with microsoft. If you open something with a protocol handler, that has to be a different scheme. How does that tie in?

Ken: why does this need to be specified? Interop?  Not really a whole new thing – just about moving people to https. If there's something else here than it needs to be pointed out – something more fundamentally different.
  
#### [WebCodecs](https://github.com/w3ctag/design-reviews/issues/433) - @cynthia, @dbaron

[bumped but we can still chat in the plenary]

## Plenary Session - [2020-03-25](https://www.timeanddate.com/worldclock/converter.html?iso=20200325T210000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

Present: Dan Kenneth David Rossen Yves Peter Tess

Regrets: Alice Sangwhan Hadley

* Breakout Rollup

See below

* [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471) - @torgo, @plinss, @ylafon
* Re-re-discuss plenary time slot
* Issue Triage


-----

### Breakout rollup

#### Breakout A Rollup

Present: Peter, Yves, Dan, Ken, Rossen, David

Regrets: Tess, Hadley

Dan: Web NFC bumped

... Origin Isolation, bumped

... URL protocol handler, fairly long discussion on this. Basically coming back to the point that this should not be in isolation, but be integrated with other things related to protocol handlers like the existing API as well as the file handlers. Rossen has an action item, no update yet. (but Rossen is working on it as we type)

... PWA changelog, seems reasonable, but should it really be html or something simpler/cut down - do we need the full expressiveness of html or not. Dan will write up notes but hasn't done any work yet.


#### Breakout B Rollup

Present: David, Peter, Rossen

Regrets: Tess, Hadley

David: Intersection Observer - held up because of a more generic issue... still waiting on an unresolved issue. Maybe still leave it open for that.

Dan: Delegated ink trail - Rossen moved it. Gave pretty detailed feedback during f2f and author is working on some of the problem. Explainer moved to WICG and working on updating and will ping us when ready.

David, one issue moved to C if Sangwhan was around which he wasn't - web codecs


#### Breakout C Rollup

Present: Dan, Ken, Alice

Regrets: Hadley

Dan: Badging API was bumped

... sw scoped matching patters - no update

... title bar customization - some discussion, multiple parts would go to different places. Should it be multiple proposals?

... Ken left some comments - we should have bumped it but didn't - Dan doing now

... Scheme-bound cookies (used to be scheming cookies) name changed and makes sense now. Left some feedback. Dan needs to review the feedback, but it looks like our feedback was useful. Bumped two weeks. additional work for us to read up on the changes.

(discussion around what feedback Rossen should bring to the team on title bar customization)

Ken: I think open question is about how it could be abused (or more easily abused than today).

### [Securer Contexts](https://github.com/w3ctag/design-reviews/issues/471)

Dan & Peter will organize a separate breakout session on Friday.

### Re-re-discuss plenary time slot

### Issue Triage

[Web Assembly SIMD](https://github.com/w3ctag/design-reviews/issues/487)

Tess has something to say.

[CSS Color: lab(), lch()](https://github.com/w3ctag/design-reviews/issues/488)

Peter: Is there any point of us looking at this apart from our 3 people already looking at it in CSS WG.

David: It probably has more arch influence than most - so maybe some coord is needed. Q is whether we should coord that or not.

[review HTML event loop and how things fit into it](https://github.com/w3ctag/design-reviews/issues/489)

David: Split off of intersection observer review

[For Review: Image Resource](https://github.com/w3ctag/design-reviews/issues/490)

David/Ken: Taken out of web app manifest and into its own spec for reuse :)

Dan: no explainer

David: I think the 2 sentence abstract is all you need, really.

## Secure-er contexts breakout (Friday)

Present: Peter, Dan

Peter: so my issue is that we are adding another set of switches to lock things down , on top of other things like feature policy, etc....  You mark certain things that they will only work under certain conditions and the conditions are that other things have to be switched off..

Dan: does it unnecessarily complicate the platform?

Dan: what's an example?

Peter: shared array buffer - you can make it only work if you lock down some CORS stuff.  Or you can lock down content injection unless you have CSP headers. A spec author can decide that a feature will only work if xyz condition is met. CSP in effect, secure cors, etc...

Yves: you can restrict the use of sharedarray buffers.. not mutable for example. Like isolation.

Dan: feels like this should be a elaboration on secure contexts..

Peter: yes it is.  Takes the existing notion of secure contexts and redefining it as secure context: transport.

Yves: parameterize things ... 

Dan: issue of complexity for the developer... 

Peter: i gave this feedback - confusing for authors - mike's response is that a lot of these switches are orthogonal.  Having these as primitive switches as a starting point.. and then simplifying. that's reasonable.

Dan: my concern is that there is an unintended consequence of some kind because of the complexity - 

Peter: it'll be more an issue of author/developer confusion..... a feature will not work, they will find they have to turn off a switch (e.g. cors) and people will add a header without understanding it which could witch could cause additional issues. With that said I do think it's worth locking down some stuff.

Dan: could we encourage them to do something more for developers - a wizard or flow chart of some kind... that could help peo (e.g. cors) and people will add a header without understanding it which could 

Yves: here... in our feedback we can say we don't want this to have the same fate as  hpkp  - so guidance for developers is needed.

Dan: can we leave that feedback and then say but other than that it looks good to us.  

Peter: they do see a path to having a higher level path for setting these modes. having one place to go to to help them use this feature would be a good thing.

Dan: this should be in MDN. In MDN there is a page about secure contexts and a table of all the features that require secure contexts - so this should be something similar - or a modification to those pages.

[feedback to be left and to be marked as proposed closed]