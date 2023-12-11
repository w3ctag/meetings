# TAG Minutes Doc - Mon, 4 December 2023

### Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2023/telcons/12-04-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2023-12-04](https://www.timeanddate.com/worldclock/converter.html?iso=20231204T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [New principle: When introducing heuristics, also include a way to override the heuristic](https://github.com/w3ctag/design-principles/issues/455)
* [duplicate section?](https://github.com/w3ctag/design-principles/issues/458)
* ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456)
* [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457)
* [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454)
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss
* [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober
* [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391) - @LeaVerou
* [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou
* [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453)
* [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)

### Breakout C (APAC / Europe) - [2023-12-05](https://www.timeanddate.com/worldclock/converter.html?iso=20231205T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* Findings
* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
* [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia
* [ethical web prunciples open issues](https://github.com/w3ctag/ethical-web-principles/issues)

### Plenary Session - [2023-12-06](https://www.timeanddate.com/worldclock/converter.html?iso=20231206T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

* [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov
* Web is not Versioned Finding
* Sustainability of Bundling & Caching Finding
* [Privacy Principles](https://w3ctag.github.io/privacy-principles/) call for TAG consensus
* Finalizing dates & venue for January f2f
* Breakout Rollup
* [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)
 

## Minutes

### Breakout A (Europe / US) - [2023-12-04](https://www.timeanddate.com/worldclock/converter.html?iso=20231204T170000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Dan, Tess, Yves, Peter, Hadley, Lea, Amy

#### [New principle: When introducing heuristics, also include a way to override the heuristic](https://github.com/w3ctag/design-principles/issues/455)

#### ["while a JavaScript event loop is running." is probably not intended](https://github.com/w3ctag/design-principles/issues/456)

Tess: he's technically correct... 

Dan: is this dangerously wrong?

Tess: yes - I think we might mean "during this run of the event loop" - he's right - "don't change things out from under the running script" I think we need to say that very differently.. An JS example ... looping over live collections... and mutating the collection never does what you expect. Same deal... 

Tess: tasks and microtasks... task checkpoints... this change shouldn't be observable until the next task checkpoint... We can crib from other specs that do this.  

Dan: *leaves a [comment](https://github.com/w3ctag/design-principles/issues/456#issuecomment-1839127711)*

#### [duplicate section?](https://github.com/w3ctag/design-principles/issues/458)

Tess: Same text -  maybe turned out wrong - 

#### [Use of "attribute" confusing/ambiguous](https://github.com/w3ctag/design-principles/issues/457)

Lea: ...

Tess: we should be clear what attribute means .. 

*we consider 457 and 458*

Tess: it looks like [this](https://github.com/w3ctag/design-principles/pull/350) is where it got duplicated... and [earlier PR](https://github.com/w3ctag/design-principles/pull/262)... So we should be able to just remove the earlier version.. so revert PR 262.   That addresses 458 but not 457...

Tess: [on 457] we can go through and change attribute...

Lea: I have proposed we should not use WebIDL terms and use established js terms instead.. but that was shot down.

Tess: if the primary audience were web devs I would agree... but WebIDL is the tool of spec authors...  Anyway just a simple search...

Peter: keeping the term attribute?

Tess: document wide - going through every case of the word attribute and making it clear whether it's a DOM attribute or a WebIDL attribute.

Peter: it would be nice [for 458] ... 

Tess: i will give jake feedback.

#### [I18N string best practices vs. design-principles](https://github.com/w3ctag/design-principles/issues/454)

Yves: I created a triage group `i18n-needs-resolution` - and added this to that...

Tess: we have text about how to use dom string and 

Lea: what if we changed it to "be consistent with rest of the language" - say "follow the conventions of the rest of the specs in the space"... 

Tess: the existing text could be made more clear - it's about the dom/js/html world... 

Tess: if it happens to be the case that our design principles are usable for other things then great... but ... 

Yves: we could link to the def of strong int he i18n best practice doc...

Dan: *adds [comment](https://github.com/w3ctag/design-principles/issues/454#issuecomment-1839141241)*

#### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @hober, @LeaVerou

Tess: Still worth doing.

#### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @hober, @LeaVerou, @plinss

Lea: still worth doing. useful for both spec authors and wc authors.

*noting that peter and lea are best placed to write this and both are swamped so might have to wait on the back burner*

#### [New principle: Discourage overloading (in HTML)](https://github.com/w3ctag/design-principles/issues/370) - @hober

Tess: related to #270.

#### [New principle: Guidance on options dictionaries and default values](https://github.com/w3ctag/design-principles/issues/391) - @LeaVerou

*assigned to Lea*

#### [Web platform features that augment HTML elements en masse](https://github.com/w3ctag/design-principles/issues/423) - @LeaVerou

Lea: this highlights a problem - a lot of web plat technologies that need to apply things to html elements.. this comes up multiple times in the past... each of these techs has an ad hoc solution... also aria could benefit.. 

Dan: tee it up for the f2f?

Tess: mostly i recoil at complexity... I'd be happy to participate in discussion...

#### [New principle: Text-based syntaxes should be designed to be usable by humans](https://github.com/w3ctag/design-principles/issues/453)

Lea: shared this at TPAC... argument back was "this wil most frequently be consumer by tools" but Tess [agreed](https://tess.oconnor.cx/2006/02/argumentum-ad-adminiculum)

Dan: Should this be generic?

Lea: we should have examples to make it concrete...

#### [New principle: Avoid adding (non-constructor) functions to the global scope](https://github.com/w3ctag/design-principles/issues/426)

Lea: this is a cultural difference between different standards groups -- imo what happened with the file system access api shouldn't happen again - others disagree. we need to discuss.

*dan to add to the f2f*


#### F2F Planning

Lea: we should put aside some time at the next f2f for design principles.

Dan: pair people up for design principles?

Lea: sounds good...

Lea: actual booking?

Tess: plan is Apple to host but waiting to hear confirmation... hoping this week.

### Breakout C (APAC / Europe) - [2023-12-05](https://www.timeanddate.com/worldclock/converter.html?iso=20231205T083000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Yves, Max, Amy, Sangwhan, Dan

#### Finding on no versions

Amy: I think current language is safe to put in github but language may need to be "diplomaticised" more.

Max: not sure about the conclusion -- any trend towards versioning the web is harmful. 

Dan: Any suggested?

Max: I think it's not consistent...  We say we don't have an opinion... 

Dan: *makes a suggested change to strengthen the language*

**We agree to bring it over to a github repo**

#### [bundling & caching finding](https://github.com/w3ctag/caching-bundling-sustainability)

*We look at [latest version](https://github.com/w3ctag/caching-bundling-sustainability/blob/main/index.html)*

Dan: reference for "security research"

Dan: "delta transport" - is that what we [discussed in Tokyo](https://github.com/w3ctag/meetings/blob/gh-pages/2023/04-tokyo/minutes.md#packaging-discussion)? Brotli, etc...

Sangwhan: correct.

Dan: could we encourage that work?

Sangwhan: need to figure out which RFC... 

**we agree to bring this to the plenary call**

##### https://github.com/w3ctag/caching-bundling-sustainability/issues/1

Sangwhan: fixed.

##### https://github.com/w3ctag/caching-bundling-sustainability/issues/2

Sangwhan: I will noodle on this - the abstract needs work.

**assigned sangwhan**

##### https://github.com/w3ctag/caching-bundling-sustainability/issues/3

Sangwhan: will address right now.

##### https://github.com/w3ctag/caching-bundling-sustainability/issues/4

Yves: I think this is more or less taken care of... we outlined some solutions... I think it's already there.

##### https://github.com/w3ctag/caching-bundling-sustainability/issues/5

Sangwhan: I need to spend some time... 

Yves: we should try to get Mark's input...

##### https://github.com/w3ctag/caching-bundling-sustainability/issues/7

Yves: regarding this - a shared cache that has privacy characteristics - would remove ... I'm not sure a malicious outsider could do something....

Sangwhan: if you're not reaching out to the server you wouldn't have that problem...  This is mitigated by things like subresource integrity... 

Yves: if you're tracking users and consider that a shared resource then it's unsanctioned tracking...

Sangwhan: we need to think more about this one...

##### https://github.com/w3ctag/caching-bundling-sustainability/issues/8

Yves: this is in sync with the previous comment... 

#### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344) - @cynthia, @torgo
#### [New principle: Naming of factory methods](https://github.com/w3ctag/design-principles/issues/378) - @cynthia
#### [ethical web prunciples open issues](https://github.com/w3ctag/ethical-web-principles/issues)

#### [rose colored](https://github.com/w3ctag/ethical-web-principles/issues/100)

Amy: I think we can tweak the language... to make Chaals happy.

Dan: Agreed.  We could clarify "offered under a royalty-free liicense" or "developed under a process that allows it to be offered under a roytlty-free license"... 

### Plenary Session - [2023-12-06](https://www.timeanddate.com/worldclock/converter.html?iso=20231206T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=33&p7=248&p8=235)

Present: Peter, Dan, Hadley, Yves, Amy, Rossen, Lea


#### Expectations of How Browsers work with TAG
#### [Classes (WebIDL interfaces) should only be used when you have both data and behavior](https://github.com/w3ctag/design-principles/issues/11) - @cynthia, @LeaVerou, @atanassov

#### [Web is not Versioned Finding](https://github.com/w3ctag/the-web-is-not-versioned)

Dan: [summarises]

Peter: maybe call out new efforts in CSS WG to do a marketing version of CSS? Not a version like an API version, but improving on CSS3 in terms of what people can put on their resume. I have mixed feelings, but it has strong support in the WG and developers.

Hadley: we put versions from w3c as opposed to live spec in whatwg - consuming world govts need to be able to point to a stable stack... I don't know that we need to go into that but would be concernned about just calling it "marketing"

Lea: marketing not a dirty word - css3 and html5 were important partly because job ads were asking for that... 

Rossen: for regulatory purposes you have wcag and other things - should be more structured "there is no web 3"... 

Dan: the question is not about is software versioning meaningful, but about the web platform as a whole

Hadley: nothing in this draft that i disagree with but ... 

Rossen: is there no reason why the narrative should be closer to what peter / hadley & i were arguing - "web 3 is a marketing only term, if you heard of it then don't think it's meaningful"

Hadley: "and it has nothing to do with the web platform"...

Dan: I can summarise this and feed it back to Sangwhan

#### [Sustainability of Bundling & Caching Finding](https://github.com/w3ctag/caching-bundling-sustainability)

Dan: this finding doesn't call for a specific thing, it just points out an issue

Hadley: should it not be a finding then? If we're not finding something?

Dan: finding that the state of things is not so great? Key points is with the way things are currently set up there's a lot of redundant javascript and other things that are loaded over teh wire, this causes problems for networks and all intermediaries, battery life

Lea: this should cause browsers to brainstorm on something that is not so wasteful.

Rossen: the one thing that jumps at me - the whle packaging / resistrubuting... degrading security & privacy promises ... I think there is a stronger point to be made there.  It's in the opening paragraph...

Hadley: i think that call to action is missing at least in the abstract.  we should spell that out and make it clear.

Lea: it does say the call to action.... "finding suggests..."  

Hadley: doesn't say "by browser vendors"...

Lea: there's a to-do in the closing remarks as well...  

Dan: discussed in breakout C adding a reference to this document, Sangwhan was going to make sure it was the right reference

#### [Privacy Principles](https://w3ctag.github.io/privacy-principles/) call for TAG consensus

Yves: some words I needed to look up... apart from that it was good.

Hadley: I have some editorial comments...

Amy: there are a few issues already opened for editorial comments for each section...

Dan: *explains situation with taskforce* i'd like to get TAG consensus so this becomes a TAG document and we can wind down the task force over the coming months, first lowering the cadence of meetings and relegating editorial work to the task force and then (possibly 6 months from now) closing the task force and letting the doc become a TAG doc...

Rossen: it's well written but it's a long doc... getting to the crux you need to go through a bit of text...  Suggest a week we close next week...

#### Finalizing dates & venue for January f2f
#### Breakout Rollup
#### [Issue Triage](https://github.com/w3ctag/design-reviews/issues?q=is%3Aissue+is%3Aopen+label%3A%22Progress%3A+untriaged%22)

#### Enrollment

Amy: Google have a process to register with a third party company in order to use certain privacy sandbox apis as a mitigation against abuse but it doesn't seem appropriate.. 

Hadley: That's not very open.

E.g:
 
* [Topics](https://github.com/w3ctag/design-reviews/issues/726)
* [Shared Storage](https://github.com/w3ctag/design-reviews/issues/747)
* [Attribution Reporting API](https://github.com/w3ctag/design-reviews/issues/724)

Dan: Noting that we said in [closing comment to 747](https://github.com/w3ctag/design-reviews/issues/747#issuecomment-1770139425) : "We're a little concerned by the addition of the attestation mechanism mentioned. Registering in order to use an API is not something we see having a place in the web platform."

Dan: how can we be clearer about this?

Hadley: a finding?  A 2 or 3 paragraph finding that says "this is not on"?

Peter: I agree.

Hadley: we could file the review ourselves...

Peter: a finding might be stronger than a negative review...

Hadley: and repurposable, in lots of other reviews...

Amy: I read the explainer and clicked through the the registration - with a us company - includes an faq stating you can still register even if you're not a US company....

Amy: it doesn't address the problems these APIs are causing...

Dan: it changes it to "you can use these APIs as long as we [google] trust you..." which is really  not the trust dynamic of the web.


