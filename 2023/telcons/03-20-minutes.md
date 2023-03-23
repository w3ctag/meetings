# TAG Teleconference
#### 20-22 March 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-03-20](https://www.timeanddate.com/worldclock/converter.html?iso=20230320T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Popover API](https://github.com/w3ctag/design-reviews/issues/743)
* [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo
* [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia
* [text-wrap: balance](https://github.com/w3ctag/design-reviews/issues/822) - @LeaVerou
* [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov
* [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia
* [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

### Breakout C (APAC / Europe) - [2023-03-21](https://www.timeanddate.com/worldclock/converter.html?iso=20230321T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion
* [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion
* [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo
* [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo
* [(Document Subtitle): Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @torgo
* [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro
* [Review of DPUB-ARIA 1.1 and DPUB-AAM 1.1](https://github.com/w3ctag/design-reviews/issues/821) - @rhiaro
* [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @rhiaro, @hadleybeeman

### Plenary Session - [2023-03-23](https://www.timeanddate.com/worldclock/converter.html?iso=20230323T070000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Dan, Hadley, Lea, Peter, Tess, Yves

Regrets:


### [Popover API](https://github.com/w3ctag/design-reviews/issues/743)

*debate over whether it's appropriate in this case for the requestor to close their own review*

Dan: I don't think this is *withdrawn*.  Withdrawn means the requestor halted work or refactored ...

Peter: unsatisfied?

Lea: we have concerns of the whole design of this.

Peter: my largest outstanding concern is the whole top layer design...   The rest of it - whether it's an element or an attribute - i see their point...  I think this could be brought to Chris Harrelson. 

Lea: to be fair this has been open for a long time - i do see their point from that PoV.

Peter: I hear you.

Dan: is there multi-implementer support as the requestor has stated?

Tess: is the issue with the top layer in general, or popover specifically?

Peter: i think top layer is not well thought out... not suitable for popover.

Tess: it was thrown together for Dialog element and got used for fullscreen and now popover.  It's been around for a long time. I think complaining to popove people - it might not be the right audience. Better they build on something that exists than to invent a bespoke thing.

Peter: i want top layer to be part of css. The part of toplayer in the html spec i'm fine with.  But CSS group needs.

Tess: I think it would be reasonable to say "...you opened the issue - please don't close it... we prefer to be the ones who close issues..." and "this is the 3rd thing that's building on toplayer... and we're concerned about its suitability... could you help..."

Dan: Including "please reference the issues Anne has referenced above."

Hadley: i think it's valuable to record our feedback for other people... having the record ... helps.

Lea: I don't think we can close it as satisfied with concerns.  ... the requestor closed the review to force us to resolve.  Doesn't set a good precedent.

Hadley: agree.

"Hi - there seems to be a bit of confusion here. just because it's in WHATWG it doesn't mean the review should be closed.  In general TAG should be closing issues with our own process.  We're going to go ahead and re-open and leave some additional feedback.  We remain concerned about the toplayer spec itself which this is based on. We recognize that this isn't an issue with this spec itself.  We would like to suggest that you help us work through these issues in the CSS working group (see the links from Anne above)."

Lea: I do actually have concerns with the design as well. but closing it might be the right corse of action.  We've gone back and forth... our value may have been exausted.

Dan: https://github.com/w3ctag/design-reviews/issues/743#issuecomment-1476663879

Rossen: *checks CSS agenda*

### [Early design review: Subresource loading with Web Bundles](https://github.com/w3ctag/design-reviews/issues/616) - @hober, @torgo



### [Sync Methods for FileSystemSyncAccessHandle in File System Access API](https://github.com/w3ctag/design-reviews/issues/772) - @hober, @cynthia

### [text-wrap: balance](https://github.com/w3ctag/design-reviews/issues/822) - @LeaVerou

Tess: I think we can close it.  They've thought about the issue.. Algorithmic complexity... 10 or more lines...  

Peter: just for screen?

Tess: in most browsers the user experience of print styles being different from screen styles confuses people..  it's worth raising...

Rossen: what's the printing point?

Tess: if you're printing the UA can...

**agreed to close with satisified**

### [Design Review: Speculation Rules (Prefetch)](https://github.com/w3ctag/design-reviews/issues/721) - @hober, @rhiaro, @atanassov

### [early design review: bfcache/prerendering eviction APIs](https://github.com/w3ctag/design-reviews/issues/786) - @hober, @cynthia

### [Moving local files with the File System Access API](https://github.com/w3ctag/design-reviews/issues/805) - @torgo, @ylafon

Dan: I will follow up.

## Breakout C

Present: Hadley, Yves, Sangwhan, Dan

Regrets: Amy, Max


### [MiniApp Lifecycle](https://github.com/w3ctag/design-reviews/issues/523) - @cynthia, @torgo, @maxpassion

### [MiniApp Packaging](https://github.com/w3ctag/design-reviews/issues/762) - @cynthia, @ylafon, @maxpassion

### [early design review: Permissions-Policy: unload](https://github.com/w3ctag/design-reviews/issues/738) - @cynthia, @torgo

### [Compute Pressure Specification Review](https://github.com/w3ctag/design-reviews/issues/795) - @cynthia, @torgo

### [(Document Subtitle): Early review for adding a new value to the standard list of `name`s for a meta tag](https://github.com/w3ctag/design-reviews/issues/819) - @torgo

### [Web Authentication: Large Blob extension](https://github.com/w3ctag/design-reviews/issues/820) - @torgo, @rhiaro

### [Review of DPUB-ARIA 1.1 and DPUB-AAM 1.1](https://github.com/w3ctag/design-reviews/issues/821) - @rhiaro

### [Early design review request: IPA](https://github.com/w3ctag/design-reviews/issues/823) - @rhiaro, @hadleybeeman

### Filesystem issue

Sangwhan: ken and I worked together with them on the abuse scenarios...  what do we want the implementers and the spec authors to do about it?

Yves: one of the issues is that both Apple and Mozilla are against it due to security problems... Finding a way that they would accept it would be a huge win. 

Sangwhan: I think every possible approach has been attempted.

Dan: installation of malware.

Sangwhan: for mobile OSs there are OS mitigations in place...  There are malware checks... 

Dan: what's the permission story?

Sangwhan: you can request read or read-write.  2.3 - fshandle triggers the permission grant... Permission is origin bound to a specifc set of files that the user has allowed.  You request permission to use the filesystem. And then you make an APi request that shows a picker.

Dan: The user picks a directory or file or set of files...

Sangwhan: and then the webapp can open those files as handles... As if it was OPFS...

Sangwhan: in fs spec - filesystem writable file system constructor... if you go to 4.2.3 ... malware scan defined in fs spec... It's implementation defined though...

Sangwhan: excutable... you can have a memorymapped file that translates to an address of memory...

Yves: it's not only malware. when you have access to the download directory you could have access to private info...

Dan: for https://wicg.github.io/file-system-access/#privacy-considerations i would like some of those suggestions to be normative requirements... or stronger language.

Dan: i think the multi-stakeholder issue is important but not blocking.

Sangwhan: should we ask them to unship?  The risk of making that text normative is that it's not exhaustive?

Dan: can they strengthen the language in 5.1?

Dan: I just think "Examples of directories that user agents might want to restrict" is too weak.

Sangwhan: I'll try to get some time from them...

## Plenary Session

Present: Peter, Max, Dan, Yves

Regrets: Amy, Hadley, Tess, Lea, 

### Fast Track Process

Dan: Sangwhan thinks that it should be more than just a thunbs up from 2 tag members to fast-track close something. But members should have to write some text...

Peter: I agree with Sangwhan there should be some justification raised as to why this something that can be closed... I expect the person who proposes to fast track it does that. "We can close this because ...".  If 2 or 3 people gives thumbs up then that's fine. We have the closing text we know what we're doing.  Expectations of what's in the initial proposal.

Dan: I'm concerned as well about documenting our work.  If it just happens in the slack then it won't be in the public record.

Peter: i would expect whoever closes the issue to give a closing comment that says what was discussed in the proposal. and cite "bob and alce looked at this and agreed."  We can document the response in the issue. As long as whoever closes it captures it in slack then I think we're oK.

Dan: [creates PR](https://github.com/w3ctag/process/pull/30)

Sangwhan: overall I think it's a good idea... A lot of these async / efficiency efforts have been constraines by people's time...

Sangwhan: somewhere in the process it should make it clear that if people are commenting on specs that we have reviewed or are reviewing and provide feedback that is not consensus feedback that they are doing so as themselves and not "as TAG".

Dan: we may need to add something to perocess document on that.

Peter: i don't disagree. also we can always re-open issues.  It's one thing to say "I don't think the TAG would like this" but not "The TAG doesn't like this" (unless there is a documented consensus).

Peter: people should turn notificaitons on.

### Breakout Rollup

#### Breakout A

#### Breakout C

Dan: *summarizes filesystem stuff*

Peter: I'm sure they've thought of it...

Dan: I agree - and they should write it down.  Let's normalize doucmenting the abuse scenarious... 

Dan: Miniapp - we got a [positive comment](https://github.com/w3ctag/design-reviews/issues/523#issuecomment-1477442889) back on our feedback.

### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
