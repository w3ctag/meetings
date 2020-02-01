## TAG Teleconference
##### 27-29 Month 2020

---

### Agenda:

### Breakout A (Europe / US) - [2020-01-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200127T170000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris
* [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo
* [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris
* [Contact Picker](https://github.com/w3ctag/design-reviews/issues/337) - @torgo, @hadleybeeman, @kenchris, @dbaron
* [UA Freeze Proposal](https://github.com/w3ctag/design-reviews/issues/467) - @torgo

### Breakout B (US / APAC) - [2020-01-27](https://www.timeanddate.com/worldclock/converter.html?iso=20200127T230000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @hadleybeeman, @plinss
* [HTML horizontal review: Accessibility](https://github.com/w3ctag/design-reviews/issues/459)

### Breakout C (APAC / Europe) - [2020-01-28](https://www.timeanddate.com/worldclock/converter.html?iso=20200128T080000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* [File Handling](https://github.com/w3ctag/design-reviews/issues/371) - @alice, @dbaron, @kenchris
* [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo
* [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo
* [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @torgo, @ylafon, @hadleybeeman, @lknik
* [Prefetch request changes to improve privacy](https://github.com/w3ctag/design-reviews/issues/398) - @lknik

### Plenary Session - [2020-01-29](https://www.timeanddate.com/worldclock/converter.html?iso=20200129T210000&p1=224&p2=43&p3=136&p4=195&p5=248&p6=240)

* Breakout Rollup
* Issue Triage

-----

### Breakout A

Present: Dan, David, Hadley

Regrets: Tess, David

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Bumped 2 weeks.

####  [[Payments] shipping and contact info delegation](https://github.com/w3ctag/design-reviews/issues/425) - @dbaron, @torgo, @kenchris

David to review and close if appropriate.

#### [Feature Policy: Document Policies](https://github.com/w3ctag/design-reviews/issues/408) - @torgo

bumped and Dan will try to find someone to work with on it.

#### [CSS Modules](https://github.com/w3ctag/design-reviews/issues/405) - @hober, @dbaron, @kenchris

[possibly can close based on latest feedback]

#### [Contact Picker](https://github.com/w3ctag/design-reviews/issues/337) - @torgo, @hadleybeeman, @kenchris, @dbaron

Dan: Made a comment thanking the author for their feedback and changes. Still need to address Peter's concern re ithe input type=file alternative... 

#### [UA Freeze Proposal](https://github.com/w3ctag/design-reviews/issues/467) - @torgo

Dan: just to note: Yoav raise a new issue – Yoav thought we'd covered this already. We talked about the topic in [issue #320](https://github.com/w3ctag/design-reviews/issues/320), but not the same question.

...I was hoping we could use this issue as a way to collect any/all feedback from the TAG on the risks of deprecating or freezing the UA string. 

Hadley: That sounds like a good idea. I'm in favour. 

Dan: So I suggest we ask people to comment. 

Hadley: I'll ask Leonie. 

### Breakout B

Present: Alice, Peter, Tess

Regrets: Sangwhan, David

#### [File Handling](https://github.com/w3ctag/design-reviews/issues/371) - @alice, @dbaron, @kenchris

Tess: Should we move this to breakout C, since David is unavailable this week and the other two assignees overlap in C?

Alice: Sure

Moved to breakout C.

#### [Trusted Types](https://github.com/w3ctag/design-reviews/issues/198) - @hober, @cynthia, @alice, @hadleybeeman, @plinss

Alice: Lukasz said that it was going to ship in Chrome soon, let me check

Alice: Origin trial ended, it hasn't shipped yet, there are no LGTMs on the Intent thread.

Alice: Anne pointed out on the intent thread that there are a bunch of open issues

... BZ commented: To be clear, Mozilla is interested in solving some of the problems Trusted Types aim to solve, but last I checked our general feeling at this time is that the specific Trusted Types proposal at hand may not be the right solution, and has various known and unaddressed design-level problems."

... Daniel V responded: "Known and unaddressed design-level problems" is new feedback for us. We're happy to pause this intent while we figure out those areas of disagreement."

... Then, a fuller list of issues:
- DOM node manipulation and the `<script>` tag.
- [Extensibility](https://github.com/w3c/webappsec-trusted-types/issues/241)
- Developer support / Support by Frameworks

Tess: maybe we should ask on the Intent thread for specific issue links for the above things, instead of spelunking in the issues & PRs ourselves?

Alice [commented on the TAG design review issue](https://github.com/w3ctag/design-reviews/issues/198#issuecomment-579006123) asking for specific issue numbers for the above remaining issues.

#### [HTML horizontal review: Accessibility](https://github.com/w3ctag/design-reviews/issues/459)

Closing; filed https://github.com/w3ctag/design-reviews/issues/468 as a followup, and https://github.com/w3ctag/process/issues/3 to create a template for such followups.

### Breakout C

Present: Alice, Dan, Yves

Regrets: Lukasz

#### [File Handling](https://github.com/w3ctag/design-reviews/issues/371) - @alice, @dbaron, @kenchris

Alice: David had a good point about things on the filesystem vs things fetched. ... some issues in their repo open... none of which are closed yet.

Dan: what's the implementation status?

Alice: Currently ["proposed" in Chromium](https://www.chromestatus.com/features/5721776357113856) - under active development.

Dan: Feels like we have raised concerns, those have been listened to and issues raised...

Alice: It would ne nice to hear from David and for their issues to be closed...

Dan: Agreed.

#### [Web NFC](https://github.com/w3ctag/design-reviews/issues/461) - @dbaron, @torgo

Bumped.

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

Discussion of [new explainer](https://github.com/WICG/badging/blob/master/explainer.md). 

Alice: two different types of badge...  Two separate APIs - I believe it's necessary...

Alice: good to see feature detection right in the explainer... That seems to address the feature detection side of things.

Dan: I was concerned about the need for 2 APIs...  I was concerned about the simplest use of this API - e.g. by indie app developers... 

Alice: in their issue [#49](https://github.com/WICG/badging/issues/49#issuecomment-521882946) I wrote some explanation.

Alice: I feel like I want to bikeshed the names... 

Alice: "Client" is document, not Scope...  App is Scope. 

Alice: if you're badging a scope then it's also going to badge things like bookmarks.

Dan: Scope has a lot of different contexts.

Alice: I think Client should be Document...  I think we need Tess on this as well.  Tess was asking why it couldn't be declarative.   Let's pull it into the plenary discussion.

#### [HTTP State Tokens](https://github.com/w3ctag/design-reviews/issues/297) - @torgo, @ylafon, @hadleybeeman, @lknik

Yves: the issue is that it's a high cost to replace cookies with something new. It might be better for incremental changes to cookies achive that goal. I don't think just changing to http state tokens would be easy because of all of the different paerts of the [the ecosystem] which rely on cookies.

Yves: we did discuss this feedback previously. Not a new thing.  So - should we review technical points on the latest spec or close it because we're waiting for a clear upgrading path from cookies...

Dan: should we provide some clear TAG feedback that we would like to see this couched as an incremental upgrade from cookies rather than a replacement - like what is the gradual approach?

Yves: there are experiments ongoing on cookies - lifetime, etc... 

Dan: it would be good to understand the outcomes of those experiments.

Yves: not sure replacing cookies with soemthiing new will help - people will find other ways to track.

Dan: I feel like we should aim to close this issue with some definitive feedback at our f2f.

#### [Prefetch request changes to improve privacy](https://github.com/w3ctag/design-reviews/issues/398) - @lknik

lukasz: (suggested to close / low priority / no new input in the gh issue?)

### Plenary Session

Present: Peter, Lukasz, Tess, Alice, Yves, 

Regrets:

#### Issue triage for Design Principles

Issues assigned to next week.

Peter: This is Lukasz's last official meeting, I wanted to thank him for his participation and extend an invitation to continue participating informally in relevant issues as he sees, fit.

#### [Badging API](https://github.com/w3ctag/design-reviews/issues/387) - @hober, @alice, @torgo

Alice: Tess, let's hang on the line to chat about this if we have time

Tess: ok






