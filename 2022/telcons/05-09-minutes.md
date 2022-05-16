# TAG Call Minutes - Week of 9 May 2022

## Agenda

### Breakout A (Europe / US) - [2022-05-09](https://www.timeanddate.com/worldclock/converter.html?iso=20220509T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [File Handling](https://github.com/w3ctag/design-reviews/issues/371)
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss
* [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss


### Breakout B (US / APAC) - [2022-05-10](https://www.timeanddate.com/worldclock/converter.html?iso=20220510T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
* [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
* [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss



### Breakout C (APAC / Europe) - [2022-05-10](https://www.timeanddate.com/worldclock/converter.html?iso=20220510T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
* [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro
* [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman


### Plenary Session - [2022-05-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220511T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

## Minutes

### Breakout A (Europe / US) - [2022-05-09](https://www.timeanddate.com/worldclock/converter.html?iso=20220509T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Peter, Amy, Hadley, Lea, Yves, Tess
Regrets:

#### [File Handling](https://github.com/w3ctag/design-reviews/issues/371)

Dan: Last comment from dbaron was happy.. fine to ask for rereview based on there being a new spec. Let's look at the status.

Dan: explainer updated

Hadley: [updated of what's changed](https://github.com/w3ctag/design-reviews/issues/371#issuecomment-1022586011) from 26 jan.

Lea: seems to have mime types and extensions linked to eachother.. what happens if you try to open a file with not the correct mime type. Shouldn't these be seperate?

Yves: for local files?

Peter: taking the extension and mapping it to a mime type...

Lea: shouldn't the extension be the key in that case...?

Peter: multiple extensions mapped to one mime type...  convenient but error prone...

Lea: seems to make it mandatory to define a mime type - which is not something you need.

Peter: don't you need it when you open the file?  Presuming you send it toa blob which is a mime type.

Peter: you're making the browser dispatch it - you go to the OS, double click the file, it sends you to the URL (of the webapp). 

Hadley: explaienr gives an example on linux - requires all extensions to map to a known mime type... UA enforces app to only open files with specified extensions... introducing new rules...

Dan: I'm wondering about security boundary violations ... 

Hadley: they want to follow users' applications... but what if it's doing something the user doesn't expect?

Dan: will review security & privacy...

Peter: the explainer says the UA can issue a permissiomn prompt....


#### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

Dan: Reviewing status ... no info on multistakeholder but some developer feedback has come in.

[punted to B hope to get some feedback from Rossen]

#### [Early design review: CSS Toggles](https://github.com/w3ctag/design-reviews/issues/730) - @LeaVerou, @plinss

Lea: we have to take a look... 

Dan: let's tee up for the **plenary** 

#### [Early design review: Focusgroup](https://github.com/w3ctag/design-reviews/issues/732) - @LeaVerou, @plinss

Lea: I think it's a first that focus can be controlled by CSS this way. No precedent. Not sure how it interacts with the HTML attribute.

Peter: something similar about navigation...  TV set top box uses case...

Lea: i think it's an amazing idea - but departure from precedent. Says CSS values will override HTML values if they conflict. Like presentation attributes in SVG.

Dan: is this primarily or tangientally an accessibility thing?

Lea: I think it's an accessibility and usability thing

Dan: should we get accessibility people to look at it?

Lea: Can't hurt



#### F2F discussion

zeroing in on the week of the 13th of June in Edinburgh

### Breakout B (US / APAC) - [2022-05-10](https://www.timeanddate.com/worldclock/converter.html?iso=20220510T000000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, 
Regrets:

#### redux of [speculation rules](https://github.com/w3ctag/design-reviews/issues/721)

#### [EditContext API](https://github.com/w3ctag/design-reviews/issues/416) - @cynthia, @atanassov
#### [Early design review for Range API improvements](https://github.com/w3ctag/design-reviews/issues/725) - @cynthia, @LeaVerou, @plinss
#### [Review request on `blocking=render` attribute for scripts, stylesheets and link resources](https://github.com/w3ctag/design-reviews/issues/727) - @hober, @cynthia, @plinss


### Breakout C (APAC / Europe) - [2022-05-10](https://www.timeanddate.com/worldclock/converter.html?iso=20220510T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Yves, Max, Hadley
Regrets: Amy

#### [WebXR Raw Camera Access API](https://github.com/w3ctag/design-reviews/issues/652) - @torgo, @rhiaro
#### [Conditional Focus (When Display-Capture Starts)](https://github.com/w3ctag/design-reviews/issues/679) - @torgo, @rhiaro
#### [I18N String-Meta and WebIDL](https://github.com/w3ctag/design-reviews/issues/716) - @maxpassion, @hadleybeeman

Sangwhan: why is it a type shouldn't it be a trait. oh webid doesn't have trait?  An object that can have a string represetnation should be localizable.  For example if you have an object that has a `toString`... you want `toString` to return a string that has a localizable trait.

Yves: in unicode there were specific codes to identify the direction.. currently it's deprecated... about to be removed... [from unicode]... 

Sanghwhan: RLM? https://en.wikipedia.org/wiki/Right-to-left_mark 

Yves: https://w3c.github.io/string-meta/#unicode_enough  - the problem is what happens when you want to do string equality...  this would be a good way of doing it because from the API point of view there is no change but from everything that needs to process strings there is an issue. I don't think there is a "right solution" - it's just trade-offs. 

Dan: can the priority of constiuencies be helpful?

Sangwhan: we have to think about it from a developer perspective... something similar from the I18N wg that we reviewed... it was possible to decide which was better based on ergonomics. I don't see an immediate difference here. 

Dan: easier for developers to use -> more use of I18N -> better I18N of the web overall?

Yves: the balance is the need for I18N on one side and... inconvenience for developers... The issue is that localizable strings are mixing data and metadata ... more difficult than an object that represents some data... 

Yves: if it's a new type in the language [js] then it's easy to use it in WebIDL and everywhere else. but you could say the same for mandating the use of unicode description characters... if it's present in the way JS is handling strings for instance then it solves the issue.. not sure what the impact would be for the browsers.. if info [meta] would be kept along with the data.  It's easy to get the data to process it and forget about the metadata... either having a specific type or mandating the use of the description ... which was deprecated because nobody was using it.  To me it's more of an ecmascript thing for them to decide first.  Either add a new type or processing of unicode characters...

Dan: we could recommend that ecmascript community makes this decision

Yves: ensuring that the data and metadata are as closly tied togetether as possible so the metadata is not lost.

Hadley: given that they are already talking to ecmascript community what is they want us to do?

Sangwhan: weigh in on which tradeoff the web should go for?

Max: agree what Yves said - it should be coupled - centralized way for metadata and text tu run together to make it easier for the developer to use... otherwise difficult to be consistent.

Sangwhan: they want to have a proposal into TC39 that also is adapted by WebIDL... 

Yves: i think it's better to start with the native type - ecmascript. 

Dan: since the webidl people follow TC39 ... TC39 is the right place...

Yves: it would be good to get Apple's and MS's opinion... people working on I18N.

[discussion of DOM string and TC39 string]

Dan: draft tag view might be - "be guided by developer ergonomics; data and metadata closely bound; should follow from TC39 consensus on what the right approach is and then adjust WebIDl accordingly..."

#### discussion on f2f options



### Plenary Session - [2022-05-11](https://www.timeanddate.com/worldclock/converter.html?iso=20220511T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Rossen, Max, Amy, Yves, Hadley, Lea, Tess, Peter

Regrets:

#### https://github.com/w3ctag/design-reviews/issues/626 webgpu



#### https://github.com/w3ctag/design-reviews/issues/714 search - response from Anne

Dan: Peter left commentary on 11th April, what can we do to progress?

Peter: changing HTML parser seems like a bad thing

Dan: Anne [says it's worth it](https://github.com/w3ctag/design-reviews/issues/714#issuecomment-1105430727)...

Tess: we changed for the template elemnet - that was worth it...  I'm ambivelent ... there's an ARIA role and we need to elements for ARIA roles... But are people asking for it?  It would be nice if search auto-closed... but feels like a weak argunent.

Peter: agree...

Dan: maybe we'd like to see more evidence?

Peter: we're not pushing back on the entire conceopt - but rather does this merrit a parser change.

**peter to write some feedback**

Rossen: multi implementer?  

Dan: seems like Mozilla is interested as well..

Rossen: Sounds like paper pushing... worried about stalling progress.

Peter: if i put a `<p> <search> </search>` then different browsers will create a different DOM. How bad is the breakage?  could break CSS. Could break script?

Rossen: these risks would be assessed by implementers...  

Peter: it's not an argument designed to stall - but rather to live up to promises of the parsing algo.  I think it's a good change but can we change it in a way that allows us to make this declarative somehow - make a parser change once that will allow these changes to be not a big deal in the future?  We've lose extensibility?

Rossen: opening a can.  But I would suggest adding that to the issue.

Peter: that's my intended feedback.  I think "a promise was made - we're breaking that promise" 

#### https://github.com/w3c/mediacapture-region/issues/11 (region capture) - their issue 11 could we say "either would work and we don't see a strong reason why further debate is needed" <- posting the result into our issue.

Our issue [710](https://github.com/w3ctag/design-reviews/issues/710)

Dan: sangwhan may have more detail...

#### https://github.com/w3ctag/design-reviews/issues/400 font table - reopened - dbaron - re-triage

[discussed and re-triaged]

#### Breakout Rollup



#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

#### DID discussion

Tess: URL spec first developed - URL spec contained URL schemes... they modularized it later.  "You can use these 8 schemes." Demonstrated interop on real things.  The first version of this thing should contain non-trivial schemes.   I don't think it should go to CR unless it contains that level of detail.

Hadley: wider consideration besides w3c... Also how much of the objection here is process / AB territory not architectural?

Tess: technical components... 

TAG consensus points:

**We do not have consensus from the TAG on whether the FO should be upheld.** 

**We think a set of methods should be standardised, and one of the core considerations for those methods should be sustainability.**

**We recognize that a substantial amount of DID methods have been designed outside the working group but that it hasn't happened inside the REC track process.**

**There may have been a charter issue.  Had there been DID methods in the charter and interoperability of these methods in this spec had been demonstrated then that would have been better. The TAG notes that we [did review](https://github.com/w3ctag/design-reviews/issues/216) and we did raise the issue of ineroperability.**

#### F2F

https://doodle.com/meeting/participate/id/b2kmoRNd

