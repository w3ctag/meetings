# TAG Teleconference
#### 20-22 November 2023

---

## Agenda:

### Breakout A (Europe / US) - [2023-11-20](https://www.timeanddate.com/worldclock/converter.html?iso=20231120T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss
* [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov
* [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou
* [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @atanassov
* [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo
* [Animating font-palette](https://github.com/w3ctag/design-reviews/issues/915) - @hober, @atanassov
* [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss

### Breakout C (APAC / Europe) - [2023-11-21](https://www.timeanddate.com/worldclock/converter.html?iso=20231121T073000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon
* [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @torgo, @rhiaro
* [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman
* [WebCodecs support for AV1 screen content coding tools](https://github.com/w3ctag/design-reviews/issues/912) - @cynthia, @torgo
* [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @hadleybeeman
* [CSS Spelling and Grammar Customization](https://github.com/w3ctag/design-reviews/issues/913) - @torgo

### Plenary Session - [2023-11-22](https://www.timeanddate.com/worldclock/converter.html?iso=20231122T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

-----


## Breakout A

Present: Peter, Dan, Amy, Hadley, Yves, Rossen

Regrets: Lea


### [Soft Navigations](https://github.com/w3ctag/design-reviews/issues/879) - @LeaVerou, @plinss

*bumped*

### [Intersection Observer Scroll Margin](https://github.com/w3ctag/design-reviews/issues/905) - @LeaVerou, @atanassov

Rossen: looks like they haven't replied to us...  Original issue ... still only an issue and not an explainer... No update based on last week's ask...   I'm somewhat familiar with the issue but prefer to stick to the process even if's just to improve habits. 

Dan: [reaches out to chris harrelson]

### [View Transitions: list of types](https://github.com/w3ctag/design-reviews/issues/908) - @hober, @LeaVerou

### [Long Animation Frame API (LoAF)](https://github.com/w3ctag/design-reviews/issues/911) - @hober, @atanassov

Rossen: implementability... my top level understanding is - the authors want to introduce a way for developers to get better details of the user experience... through a set of events they can get back .. in order to help with long running animations. the way they are proposing - having a set of events that are annotating each part of the render pipeline... when you start layout; end the layout; start rendering; end rendering; style, etc... at a high level you can say every browser has these stages - but if you expose this level ... how do you correlate the actual triggers for that long running animation?  Maybe there was a user action that invalidated a layout rule?  If I go back to the motivation ... to better explain "why" the "sluggishness" is happening.  Not able to connect the dots...  Maybe need to [read it deeper]. It also overlaps with event timing .. and pre-existing tech. 

Dan: is there a cross-browser issue here?  Would this only apply to chromium and not gekko, for example?  

Rossen: possibly - i know that there are differences... i don't know if by exposing this people will only optimise for chromium ... this isn't clear to me.

Peter: i don't see anything in LoAF that would be problematic for gekko....

Rossen: might see more cross-origin information caused by user inetraction... hover an ad, ad calls "bounding client rect" - now the user can be targetted more..

Dan: that triggers a privacy alarm

Rossen: they do delve into this in the privacy & security consideration section... available to all of the same agent windows -- global state exposure, which is peculiar.

*rossen to formulate further response*

### [CSS ::selection Inheritance Model](https://github.com/w3ctag/design-reviews/issues/914) - @LeaVerou, @torgo

### [Animating font-palette](https://github.com/w3ctag/design-reviews/issues/915) - @hober, @atanassov

### [Adding support for High Dynamic Range (HDR) imagery to HTML Canvas](https://github.com/w3ctag/design-reviews/issues/917) - @LeaVerou, @plinss


### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

Yves: don't know if they want to circumvent cross domain comms ... 

### [Permissions Policy Reporting and Report-Only mode](https://github.com/w3ctag/design-reviews/issues/909) - @torgo, @hadleybeeman

Hadley: report-only mode - that feels like a fingerprinting thing... sending a lot of info without the user being aware of it...  Could it be misused?

Yves: you could intentionally generate errors...  But probably other ways of doing that... especially if there is a possibility of sending the report to  another host...

Peter: most things - like CSP - let you send it to a 3rd party service... some require it. 

*we discuss writing a comment to ask what abuse scenarios there are and what mitigations might exist?*

Peter: the same information can be gotten via an API https://w3c.github.io/permissions/




### [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @hadleybeeman

*Hadley and Dan try to unwind what exactly is being proposed in https://arichiv.github.io/opener-storage-partitioning/*

Hadley: the risk is that they can share unpartitioned storage?   The goal is to maintain cross-page communication... How often do we really want cross page communication?

Rossen: payment... auth... there are a bunch...

<blockquote>
@arichiv It would be really helpful to have a bit more information in the examples - that you've laid out - so we can understand what risk is being introduced / mitigated against at each step?  I think this info is evident to you, but not evident to the reader. Could you build on the example that you provided in the comment above and extend that a bit? 
</blockquote>

## Breakout C

Present: Dan, Max, Yves, Sangwhan

Regrets: Hadley, Lea

### [TAG review for web app `scope_extensions`](https://github.com/w3ctag/design-reviews/issues/875) - @torgo, @ylafon

*no response yet*

### [Extending Storage Access API (SAA) to non-cookie storage](https://github.com/w3ctag/design-reviews/issues/906) - @torgo, @rhiaro

Dan: can we provide some guidance to the spec authors here?

*bumped 2 weeks*

### [WebCodecs support for AV1 screen content coding tools](https://github.com/w3ctag/design-reviews/issues/912) - @cynthia, @torgo

Dan: can we close this?

Sangwhan: contenthint is fine - but there seems to be an antipattern -- worried about developer copy-pasting a config from somewhere - which would result in a contradicting set-up. The counter-argument would be "everyone who works on web codecs would know what they're doing" - i think it's bad ergonomics.  Force screen content tools.  It does an optimization specific for static content... only certain parts get updates... shooting over a presentation... the naming does not tell you that at all.  If you say "i am optimizing for smoothness" and for some reason you opt for screen content tools ... Maybe it should at least show a warning - in the developer console?

... Screen content optimizations are also available in other codecs but this terminology is very specific to AV1... I'll write a comment.

Yves: it's fair to have specific optimnization for specific codecs but maybe prefixed?

Sangwhan: maybe an enum?  codec config and an enum of possible values... This feature is similar enough between AV1 and HEVC... 

Yves: would it do nothing if not supported?

Sangwhan: yes. 

Yves: graceful degredation is better than failing.

### [Early Design Review: Opener Protections](https://github.com/w3ctag/design-reviews/issues/916) - @torgo, @hadleybeeman

### [CSS Spelling and Grammar Customization](https://github.com/w3ctag/design-reviews/issues/913) - @torgo

Amy: my question - shouldn't the user agent be in charge of picking a color?

Yves: in the explainer it talks about range... but not specification of different types of ranges... the ranges should be indicated in some way... 

Dan: let's talk more about this at the *plenary*

## Plenary Session

Present: Dan, Peter, Amy, Rossen

Regrets: Hadley, Lea, Yves

### Breakout Rollup

#### Breakout A

#### Breakout C

### [CSS Spelling and Grammar Customization](https://github.com/w3ctag/design-reviews/issues/913) - @torgo

Peter: spelling and grammar already exist - so this is about highlighting text without modifying the DOM... custom highlight ... 

Dan: So maybe it should be called "custom highlights" ?

Peter: the explainer is just talking about the highlight API... 

*some discussion*

Peter: I don't think the explainer goes into it...

Dan: should we close this?

Peter: custom styling... 

Amy: it's in the open questions... overrides...

Peter: that might be for overlapping -- when you have a highlight and spelling error which one wins?  You can have 2 highlights that are overlapping... what do you do with that?

Dan: I think we should leave it up to them....

Peter: yeah.

<blockquote>
Hi @schenney-chromium - thanks for the opportunity to review this.  We're happy to see this proceed. ✨✨
</blockquote>

**agreed and closed with satisfied**

### Issue Triage

#### VC

Amy: Hadley & I are working on review... I don't see objections...

Dan: if that's the case then 

#### https://github.com/w3ctag/design-reviews/issues/891

Amy: Can we close?  Dictionary leak?

Rossen: generally I think this is fine - i also agree that they are ignoring the leak problem but not saying it's not a concern.  I think it's fine to ask why and then close.
