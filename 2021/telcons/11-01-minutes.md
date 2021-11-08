# TAG Minutes Week-of Nov 1 2021

## Agenda

### Breakout A (Europe / US) - [2021-11-01](https://www.timeanddate.com/worldclock/converter.html?iso=20211101T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)
* [New principle: Do NOT reuse similar attribute names for different behavior](https://github.com/w3ctag/design-principles/issues/328)
* [New principle: Avoid introducing new parser-blocking features](https://github.com/w3ctag/design-principles/issues/329)
* [New principle: Why we should not expose native object lifecycles](https://github.com/w3ctag/design-principles/issues/333)
* [New principle: CSS and HTML syntax should be side effect free](https://github.com/w3ctag/design-principles/issues/336)
* [New principle: Just because you can do xyz bad thing using another API doesn't mean it's OK to design a new API tha can also to xyz bad thing](https://github.com/w3ctag/design-principles/issues/340)
* [New principle: when to use permissions, when to use user activation, and what if neither are adequate](https://github.com/w3ctag/design-principles/issues/341)

### Breakout B (US / APAC) - [2021-11-01](https://www.timeanddate.com/worldclock/converter.html?iso=20211101T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Review Open PRs](https://github.com/w3ctag/design-principles/pulls)

* [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia, @atanassov
* [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)
* [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299) - @hober
* [New principle: Patterns for URLs in APIs](https://github.com/w3ctag/design-principles/issues/303) - @cynthia
* [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306) - @hober
* [Second consistency pass for attributes/properties/methods/functions etc.](https://github.com/w3ctag/design-principles/issues/315)
* [Encourage UTF-8 for new formats and APIs](https://github.com/w3ctag/design-principles/issues/322)
* [Discourage depending on the WTF-16 nature of JavaScript strings](https://github.com/w3ctag/design-principles/issues/323)
* [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342)
* [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344)


### Breakout C (APAC / Europe) - [2021-11-02](https://www.timeanddate.com/worldclock/converter.html?iso=20211102T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
* [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
* [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou
* [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
* [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris
* [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro
* [New principle: Do not design around third-party tools unless it actually breaks the Web](https://github.com/w3ctag/design-principles/issues/335) - @LeaVerou
* [New principle: Ethical Principles](https://github.com/w3ctag/design-principles/issues/338)
* [ethics: digital human rights](https://github.com/w3ctag/ethical-web-principles/issues/52)
* [ethics: hedging](https://github.com/w3ctag/ethical-web-principles/issues/51)
* [ethics: built form](https://github.com/w3ctag/ethical-web-principles/issues/45)

### Plenary Session - [2021-11-03](https://www.timeanddate.com/worldclock/converter.html?iso=20211103T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage


## Minutes

### Breakout A (Europe / US) - [2021-11-01](https://www.timeanddate.com/worldclock/converter.html?iso=20211101T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Lea, Ken, Amy

#### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss

Lea: can of worms.. I wish we could hear more from Anne about these issues. Mentioned in passing. Unclear if the problem is with the guidence or with the dialogue.

Dan: you tried to get more info from him in Feb.. can you leave a new message to ask for more insight?

Lea: hmm

#### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)

Lea: might be easy, we don't need to hear from anyone external.. 

Dan: I like the idea of discussion and a forum for people to ask questions and encouragement for peple to ask questions and read design principles while they're still in the design phase, not just review phase

Lea: I envision this thing to be very small self contained problems. There are a lot of these micro decisions you make when you're designing an API. When we were designing proposal for colour api i wished to ask the TAG about things, but didn't want to waste peoples time. Great if there was a casual q&a for this sort of thing.

Dan: the other forum might be the TAG channel on the w3c community wiki. Both could make sense as a place to .. shunting it to one place, in particular a place on github that might have more public access could be a good thing becuase if somebody is casually looking for the answer to something they could come across this opinion rather than it being stuck in a chat somewhere.

Lea: hiding it in a mailing list or wiki is a guarantee for it to not be used. GH discussions is appropriate, maybe design reviews rather than design principles?

Dan: I feel we push people to design reviews repo when they are requesting a design review. Maybe we want to.. I'm trying to figure out which would be more friendly

Lea: I find there are two components to each tag review - security and privacy, and api design review. Not sure this is useful for the first kind of thing, but api design has a lot of incremental small decisions. If it's more about that sort of thing then maybe the design principles repo would be mre appropriate.

Amy: +1 design principles repo

Dan: creating a space doesn't mean people will join us there. We need to do publicity to draw people there.

Lea: also how much... we don't want an influx of developers.. needs to be for people designing web apis in particular

Dan: we could do a blog post on the TAG blog and a post to chairs mailing list calling attention. We have to be clear it's covered by the w3c CEPC guidelines. Does it allow anybody to come in or do we have to expose it to certain groups? W3C or everybody?

Amy: we need to build in time in our week to make sure we check it too, or people might post and never get a reply

[discussions switched on]

Dan: [writes announcement]

[discussion of discussions]

Lea: we can close the issue once the discussions section is ready and we publicise it

#### [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)

Ken: talked about that a couple of times.. about webcodec I believe. I think the thing is if you expose it on worker, try to expose it on window as well, not necessarily the other way around. One case that makes sense is web codecs. I wonder if we can make guidence on this with one case? Depend on context.

Dan: we could ask Chris [in issue] to...

Ken: the discussion Chris is pointing to is the other way around. Webcodec only exposes on workers, but other people want to expose on the main thread because it's faster, it's already running, less overhead. But Chris is pointing out this thing on the main thread that should be available on worker like web usb, web audio. But workers will turn into this big thing if you expose the whole dom to them, becomes very expensive. Workers should have limited scope is the thinking. I think it depends on context

Dan: isn't that worth exploring? If the thining behind workers is to have limited scopes in order for them to be light then that needs to be spelled out somewhere?

Ken: I think it is in the workers spec, which I guess is html now. Anne would have input. Do we need design principles for these things? 

Dan: if the media wg is an example of one group paying attention who are asking for it, so there might be others who need the guidence. If there's somebody looking for guidence and it's a design issue arguably we should have a principle. Could we do a call to the community? Tempted to ask Chris who has engaged for further feedback.

Ken: they already made a decision on webcodecs. They asked if they can also expose it on the main thread. People said they don't neessarily need the flexibility of a separate thread, it's faster if it's on the main thread. On the main thread you have access to webusb and web audio so they're all good. I don't think we'll see webusb and web audio exposed to workers.

Dan: anything came out of this call for consesnus they ran to help us to craft a... [writes reply]

#### [New principle: Do NOT reuse similar attribute names for different behavior](https://github.com/w3ctag/design-principles/issues/328)

Dan: reverse of 281 which was closed.. examples of the antipattern

Lea: could be written together with 281. I could take this one.

Dan: do you think this could be a subsection?

Lea: yea, just a sentence

Dan: maybe we can do that this week

[added to project]

#### [New principle: Avoid introducing new parser-blocking features](https://github.com/w3ctag/design-principles/issues/329)

Lea: Jake wrote some text, I asked for a PR

Dan: we could do the PR. There's another meta issue which is... we don't have a proper contributors section in this document

Lea: I thought we did... Acknowledgements, Jake is already in it

Dan: great. Where?

Lea: under the HTML section. Okay for two setions? We can iterate on the PR

Dan: in HTML there's only one thing

Lea: but lots of outstanding issue

Dan: fine to add two things

Lea: **[PR Raised](https://github.com/w3ctag/design-principles/pull/347)**

#### [New principle: Why we should not expose native object lifecycles](https://github.com/w3ctag/design-principles/issues/333)

#### [New principle: CSS and HTML syntax should be side effect free](https://github.com/w3ctag/design-principles/issues/336)

Dan: we got to a weird place with this last week with Rossen.. in the contains intrinsic size thing (which is referenced)

Lea: separate discussion for general guidence. 

Dan: looks like you're hashing that out with Anne

Lea: idea being if you see it very strictly network requests themselves cause side effects... this is more of a be careful how you phrase it, not this should not be a principle

Dan: purism point of view rather than as practiced.. about how you define side effects. We need a definition that makes sense.

Lea: not sure if this applies to html. CSS only or also html? Originally I thought it applies to all declarative languages, but maybe it's just css, maybe html already has side effects. Eg. what about form controls?

Dan: more involved discussion, **plenary**?

#### [New principle: Just because you can do xyz bad thing using another API doesn't mean it's OK to design a new API tha can also to xyz bad thing](https://github.com/w3ctag/design-principles/issues/340)
#### [New principle: when to use permissions, when to use user activation, and what if neither are adequate](https://github.com/w3ctag/design-principles/issues/341)

### Breakout B (US / APAC) - [2021-11-01](https://www.timeanddate.com/worldclock/converter.html?iso=20211101T230000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### [Review Open PRs](https://github.com/w3ctag/design-principles/pulls)

#### [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia, @atanassov
#### [New text re: balancing concerns between interoperability and implementability](https://github.com/w3ctag/design-principles/pull/290)
#### [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299) - @hober
#### [New principle: Patterns for URLs in APIs](https://github.com/w3ctag/design-principles/issues/303) - @cynthia
#### [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306) - @hober
#### [Second consistency pass for attributes/properties/methods/functions etc.](https://github.com/w3ctag/design-principles/issues/315)
#### [Encourage UTF-8 for new formats and APIs](https://github.com/w3ctag/design-principles/issues/322)
#### [Discourage depending on the WTF-16 nature of JavaScript strings](https://github.com/w3ctag/design-principles/issues/323)
#### [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342)
#### [General principle around time measurement units/formats for various domains (JS, HTTP, HTML, etc)?](https://github.com/w3ctag/design-principles/issues/344)


### Breakout C (APAC / Europe) - [2021-11-02](https://www.timeanddate.com/worldclock/converter.html?iso=20211102T090000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Sangwhan, Yves, Ken, Amy, Lea, Hadley

#### [PR 345](https://github.com/w3ctag/design-principles/pull/345)

**merged**

#### [PR 347](https://github.com/w3ctag/design-principles/pull/347)

Dan: this changes the html section from having one thing to three things so it's fairly substantive

Sangwhan: this kind of behaviour is rarely defined as part of a spec. For a spec normatively to say pause the html parser and do this action and continue parsing after you're done. Probably only html does that. How wide is the audience?

Lea: this started from a whatwg thread because people were proposing a parser blocking feature. A clientisde include feature. 

Sangwhan: yeah that would do it. Unless we had that partial docuent loading thing, preloading thing

Dan: do you think there needs to be more explanation here about what we mean? Or what kinds of features could cause this behaviour?

Sangwhan: this principle is sort of a consequence of such a request and I don't think the developers that requested this thought about it that much, they said we want this feature without thinking of the consequences of stopping the world of the html parser. How well versed are devs in terms of understanding quirks and weirdness of html parser?

Ken: very few people

Dan: what does that mean for this? You think we shouldn't have it? Or expand it? I don't know whether it's the job of this doc to explain how the html parser works

Lea: we shouldn't have a principle becuase nobody that knows about it is proposing parser blocking features?

Sangwhan: yeah. The primary audience of the design principles is spec authors,a nd spec authors would probably recognise a parser stopping requirement when they see one and that would trigger within the group. I see we'd want something like this in here but not sure if this exact text is the form. The target audience probably already knows

Dan: I'm probably guilty of starting this discussion. When I saw [Jake's comment](https://github.com/whatwg/html/issues/2791#issuecomment-892790934) I thought okay great you know that, people in the html community know that, but where is it written down or is that just found knowledge? If our doc isn't the place it should be written down, where should it be written down?

Lea: that's why I suggested a principle, I don't like this secret knowledge. I think the audience of the principles isn't just spec designers, it's anyoen keen to propose apis for the web platform. Not to mention we have another issue about extending design principles wider

Sangwhan: not suggesting we don't need this kind of principle, but how it's worded for the people who know it's very obvious and the people who don't it doesn't associate very well

Lea: good feedback

Sangwhan: how do we make it digesetable by web developers who don't really know

Lea: don't feel it warrants two separate sections, happier if they were one, but wanted the initial pr to preserve jake's text

Sangwhan: agree, don't think it should be two sections

Lea: its' a minor point, I envison a small section

Sangwhan: don't block the render thread is the tl;dr

Hadley: 'Don't block the render thread' — that's a lot easier for me to take in and do something with than what's written. Useful to have the main point be drawn out more.

Sangwhan: I'll have a go and have Lea review

Lea: yeah


#### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
#### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
#### [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
#### [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
#### [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou
#### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
#### [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris
#### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro
#### [New principle: Do not design around third-party tools unless it actually breaks the Web](https://github.com/w3ctag/design-principles/issues/335) - @LeaVerou
#### [New principle: Ethical Principles](https://github.com/w3ctag/design-principles/issues/338)
#### [ethics: digital human rights](https://github.com/w3ctag/ethical-web-principles/issues/52)

[Discussion of human rights and the UNHCR and whether it's appropriate to have a reference to the UN declaration on human rights in the document...]

...looking for other sets of internationally recognized human rights to not imply that UNHCR is the only one...

```
Hi folks – This has been a wide-ranging and interesting discussion.  As we're trying to focus our work on specific changes or additions I'm going to close this. However if there are specific and actionable contributions to the document that people would like to make then I encourage you to open up a new issue on that specific suggestion.  
```

#### [ethics: hedging](https://github.com/w3ctag/ethical-web-principles/issues/51)
#### [ethics: built form](https://github.com/w3ctag/ethical-web-principles/issues/45)

### Plenary Session - [2021-11-03](https://www.timeanddate.com/worldclock/converter.html?iso=20211103T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Dan, Peter, Tess, Hadley, ROssen, Lea, Yves, Sangwhan, Amy

#### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

Lea: last time it was brought up Rossen had thoughts..

Rossen: I added a comment

Lea: I think we should have guidence, I'm not sure what it should be. Should we have guidene about serlialisation for CSS? We keep having discussions about how to serialise css syntax, deiciding an an ad hoc way, dbaron at some point tried to put guidelines down, eg. shortest from all things being equal, or oldest form. In general apart from small things not described anywhere, just in the wg heads, there's no other way to decide. We keep having these discussions and decide on each topic in an ad hoc way. 

Tess: I have an idea with TAG hat on. The CSS WG could write down its own principles? Every WG gets to do its thing well. If this is causing churn in the CSS WG they can fix it.

Lea: this is a larger issue... tc39 and whatwg should have their own.. so what's the point of design principles?

Tess: they should.. they should capture that learning and we find out that when it generalises beyond that group they should come to us and it applies across wgs?

Lea: so we shouldn't have html and css sections because they are specific to wgs?

Tess: not that dogmatic. Groups should generate their own principles an dif we think they apply we should adopt them. More than one group defines things like html elements and css properties

Dan: could we ask the css wg to generate this principle with the offer that if appropriate we can put it in our design principles doc?

Tess: that'd be great

Lea: we probably shouldn't be duplicating content

Tess: move not a copy

Lea: we could link to it. I'm having trouble understanidng what is supposed to live in our principles and what in individual wgs. We do have specific things that are only pertinent to a specific wg

Tess: we should have in our doc whatever we want. It shouldn't be an excuse for wgs to not do their own work. 

Lea: wgs and what they work on can vary.. css would define properties that apply to svg.. serialisatin was an svg problem as well

Tess: effects task force would have to produce its own thing

Dan: let's ask the css wg if they have text, or if they don't want us to do that we can let them do it, but that we have the sense that this needs to exist. Not duplicating effort, but soliciting. Conscious of the fact we have got trouble in the past with css wg for putting stuff into our doc about css and someone comes and says we're not the css principles police. If we want to do this and there's a need for it, the right thing to do would be to ask the css group for text

Rossen: I agree with Dan. A good issue to be worked on. If we're talking about serialisation in general, that is something it's good principle on how to serialise things.. how do you serialise things so that they're applicable to the different constintuencies that serialisations is used by, users tools, platform apis, if there's general guidence that could apply here maybe we can work on it. The specifics of css serialisation itself is something that should be produced by css wg same way the type system is. Anything else syntax related. Our design principles are about designs, not the specifics of a given language or capabilities. I am happy to bring this to to the CSS WG. 

Lea: do you think there is general guidence we could have?

Rossen: that's where I was going.. generally if your'e talkinga bout users, some of the principles I added should apply to any language not css only. Being able to roundtrip thigns through tools and not generate error, that's a general principle of serialisation that could apply to anything. Could apply to DOM API.

Sangwhan: this came up about 5 years ago during a f2f, we didn't get anywhere because json is very limiting. 

Rossen: If we try to generalise across the entire web platform the least common denominator is so restrictive there's almost nothing you can say?

Sangwhan: we'd have to force specs to define serialisation and deserialisation, and nobody was willing to. We were looking at it from a context of bigint and date and time proposal. json doesn't have the flexibility to do it without weird syntactic sugar. I think we should look into it. I'd be happy to write a princple, but right now we have to think about it for a while. 

Lea: is there an issue about that discussion?

Sangwhan: I don't think so, might have been closed. [Here's one](https://github.com/w3ctag/design-principles/issues/116). This discussion came up multiple times.

Lea: that's about json specifically

Sangwhan: with json there's an implicit expectation that it will roundtrip without breaking stuff

Lea: seems like a separate issue. In the context of html it would affect things like innerHTML, outerHTML, how html serialises itself, in the same way css serialisation affects computed style

Sangwhan: these are multiple things..

Lea: in js side theres serialisation of js with function to string.. serialising to json is a specific format with its own constraints

Dan: is there an issue that captures this? will you open one?

Sangwhan: i would if we could action on it... we don't really know what to do

Dan: if we want to address it it'd be good to open an issue even if we can't get to it immediately

* Breakout Rollup

#### Breakout A

Dan: github discussions set up...

Lea: no template for questions. Should be seeded with the kinds of questions we want people to ask. Ideally not by us. Then write a blog post

Dan: and be prepared to moderate. Also guidence on window vs worker.. I wrote a reply. Do not use similar attirbute names

Lea: merged the PR on that

Dan: avoiding parser blocker features we talked a lot about

Lea: Sangwhan is going to reword existing PR. 

#### Breakout B

#### Breakout C

Lea: went through guidelines for web component authors.. went through the document and kept notes on which are suitable for design principles. Primarily part about attributes which became its own separate issue. Current guidence is not something that html does. Use attribute for complex data.. also a sub-bullet about a js api.. a lot of web components do, but not what native html does. In html when the input needs to be an array or object its provided through a certain structure of thes ubtree of the children, eg. data list. INput is an array of objects, with value. We don't do that via a js api, but by nesting a list of option elements inside it. That's generally the prevailing way html does this. It's not right to advise web component authors do something different, but there are clear performance implications with not having to modify an entire subtree. Opened a separate issue. 

Dan: new issue on a milestone of f2f?

Lea: will do

Dan: in the other half of breakout C we talked about ewp and closed a design principles issue which was the one on adding ethical principles to design princples because we felt it had already been done. Talked about digital human rights, ewp issue 52. We were being challenged that we should be basing the ethical principles on digital human rights, and this concept is woolly. We ended up closing this and encouraging people to raise specific change requests or additions. There's work going on in the UN on digital human rights but it's early days and not really referenceable, trying not to get too far into geopolitics. Also the PR Tess made to add the explicit link to the UN declaration of human rights. I think that will come up if this doc gets upgraded to a w3c statement (which we should do). Do we have TAG consensus to try that? Use EWP as a test case for statement process? Or a different document?

Hadley: is it then frozen or are we able to iterate it?

Yves: it's like a note

Tess: can publish another one like a rec

Yves: we can update it. To publish a new statement to replae it it has to go through review

Hadley: a draft will have to go through the whole reviwe process?

Tess: if you want a new version to become a statement  you have to do the whole rigamerole. We can keep working on a WD in a lightweight way, but every so often when we want to elevate it

Hadley: I love the idea long term of ewp being a w3c statement, but I feel like it's still evolving, don't want us to do it now then again in 6 months

Tess: let it settle down a bit first

Yves: we can say in the status that we intend it to become a statement at some point

Dan: that would be a good thing to do

Sangwhan: would design princples be too much of a lviing document?

Dan: design princples shouldn't have to go through AC review. Value of statement process is to say not only does the TAG say this but the w3c has consensus on this as well. I don't know if that's as meaningful for the design principles.

Sangwhan: just to try out the process.. design principles is less contentious 

Hadley: could be a big can of worms.. interpreting little bits different ways. It's solid for the use case we use it for, but getting the entire w3c to put their name to it will waste cycles on our part

Tess: I think the ewp is a better fit, but sympathetic to Hadley's point that you think it's not ready. Is it being ready based on rate of change over time? Or?

Dan: we had feedback that some people thought it didn't go far enough. There are a few open issues. It is stablising.

Tess: shall we create a label for resolving for statement?

Hadley: my concerns aren't in an issue, we keep having really good discussions about ewp and as a result they're evlovling. I don't think we're done with those discussions yet. 

Tess: how can we get a sense of whether or not we're getting to that point. Is there a way for us to feel like we're making measurable progress?

Dan: we should have a goal of doing this. We haven't had this ability up until now. Maybe we need to timebox it so we know when we're getting there. We could continue to wordsmith things and draw it out. However we have had discussions this week about whether we could put wording in that makes it work across more cultures, those are discussions we need to have. Be good to signpost that we want to do it. We have been asked to do this too. The process is designed for this kind of document. Also the privacy principles should eventually be put forward as a w3c statement. 

Tess: the TAG has generated a lot of documents over its history.. findings that are relevant and stood the test of time that we should try elevating? Take something like unsactioned tracking, as is, and see if we can make them w3c statements

Hadley: I love that idea

Dan: try it with securing the web. Should be something nobody is objecting to.

Tess: if it falls over in the AC clearly we'll never get EWP through the process if we can't get securing the web through it

Dan: what do we need to do to start  the process for securing the web?

Yves: wait. The tooling is not there yet. A few days. Request horizontal review and AC review.

Tess: cool

* Issue Triage
