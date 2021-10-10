# TAG Minutes - week-of Monday, 4 October 2021

## Call Agenda

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/10-04-agenda.md).

### Breakout A (Europe / US) - [2021-10-04]

* [New principle: Do not design around third-party tools unless it actually breaks the Web](https://github.com/w3ctag/design-principles/issues/335)
* [New principle: CSS and HTML syntax should be side effect free](https://github.com/w3ctag/design-principles/issues/336)
* [[Meta] HTML Design Principles section](https://github.com/w3ctag/design-principles/issues/269) - @LeaVerou
* [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou
* [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov
* [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss
* [Inconsistent capitalisation of "web platform"](https://github.com/w3ctag/design-principles/issues/294)
* [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299) - @hober
* [Editorial: Add link to published version on /TR](https://github.com/w3ctag/design-principles/issues/318)
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* [New principle: Avoid introducing new parser-blocking features](https://github.com/w3ctag/design-principles/issues/329)

### Breakout B (US / APAC) - [2021-10-05]

* [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia
* [New principle: Patterns for URLs in APIs](https://github.com/w3ctag/design-principles/issues/303) - @cynthia
* [Second consistency pass for attributes/properties/methods/functions etc.](https://github.com/w3ctag/design-principles/issues/315)
* [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)
* [Discourage depending on the WTF-16 nature of JavaScript strings](https://github.com/w3ctag/design-principles/issues/323)
* [Encourage UTF-8 for new formats and APIs](https://github.com/w3ctag/design-principles/issues/322)
* [New principle: Do NOT reuse similar attribute names for different behavior](https://github.com/w3ctag/design-principles/issues/328)
* [New principle: Why we should not expose native object lifecycles](https://github.com/w3ctag/design-principles/issues/333)
* [New principle: when to use permissions, when to use user activation, and what if neither are adequate](https://github.com/w3ctag/design-principles/issues/341)
* [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342)

### Breakout C (APAC / Europe) - [2021-10-05]

* [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
* [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
* [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
* [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou
* [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
* [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris
* [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro
* [New principle: Ethical Principles](https://github.com/w3ctag/design-principles/issues/338)
* [New principle: Just because you can do xyz bad thing using another API doesn't mean it's OK to design a new API tha can also to xyz bad thing](https://github.com/w3ctag/design-principles/issues/340)
* [Ethical: Digital Human Rights](https://github.com/w3ctag/ethical-web-principles/issues/52)
* [Ethical: Dark Paterns](https://github.com/w3ctag/ethical-web-principles/issues/25)
* [Ethical: Abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)
* [Ethical: Less Hedging](https://github.com/w3ctag/ethical-web-principles/issues/51)

### Plenary Session - [2021-10-06](https://www.timeanddate.com/worldclock/converter.html?iso=20211006T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* Breakout Rollup
* Issue Triage

## Call Minutes

### Breakout A (Europe / US) - [2021-10-04]

Present: Dan, Amy, Lea, Yves, Peter, Rossen

#### [New principle: Do not design around third-party tools unless it actually breaks the Web](https://github.com/w3ctag/design-principles/issues/335)

Dan: a lot of conversation..

Lea: I left a comment with a clarification and people seemed okay with that. IMO I didn't change my mind, just elaborated. Devil in the details.. in the example that started it, if one of two options has significantly better usability it doesn't make sense to choose the other because it breaks a third party tool unless it breaks the web also. But in the exmaple that started it I thought one had significantly worse usability.. but as long as people agree on the general principle.

Dan: set this to 'writeme'?

Lea: I'll do it

Peter's cat: HELP

[github projects meta conversation]

#### [New principle: CSS and HTML syntax should be side effect free](https://github.com/w3ctag/design-principles/issues/336)

Lea: came out of discussion on contain intrinsic size auto. Introducing a feature where once a set of properies would stop applying the browser would have to remember the size of the element that those properties would have to introduce. We basically told them that no this is breaking one of the design principles of CSS that it should be side effect free. Once a property stops applying it stops having any effect. but the DP we were referring to was only in our heads.

Dan: but Anne has an objection

Lea: I made it a bit more generic in the issue, I included html. Anne said it would outlaw... iframe script something.. not sure I see it. Anything that can contain script introduce side effects, that's the whole point. But how cna style or background image introduce side effects?

Yves: because it's async, then you have a paint, receive CSS, then another repaint, has a side effect when it's loaded

Lea: you add a style and it triggers an http request and if you rememver it http request is still running? SEems edge case

Yves: I mean if the http req to load the css takes time the browser will probably try to render it in one way before the css then paint it when the css is there

Peter: but it will still render it based on the state it has at the time

Yves: but css is a side effect

Peter: I'd define that as an effect not a side effect

Yves: I think that's what Anne inferred

Lea: ask for clarification?

Dan: another option would be to write what you want to write wrt css

Lea: anne has a lot of experience, might see something I'm not seeing, I'd like to see

Dan: get anne to expand. Will you reply?

Lea: yep

#### [[Meta] HTML Design Principles section](https://github.com/w3ctag/design-principles/issues/269) - @LeaVerou

Lea: we already added an html section

Dan: is this redundant?

Lea: section 3.. PR 326 added one principle under that section

Dan: shoudl we close this issue? The other issues raised.. do we need this issue open in order to track those?

Lea: nothing tracked in here except the section, I think we can close

Peter: other principles that should be moved into this section?

Lea: I don't think so off the top of my head

#### [New principle: Guidance on when to use a child element vs an attribute](https://github.com/w3ctag/design-principles/issues/270) - @LeaVerou

Lea: part of a bunch of html related issues I opened.

Dan: is this urgent?

Lea: we don't get that many html features being added to the web platform. Nothing HTML related is super urgent..

Dan; urgent in the sense that there is an open design review..

Lea: no open design review

Dan: how to prioritize

Rossen: how useful woult this be to web devs working on components?

Lea: this is where it came from...  this came from a list of principles I had written for web component developers.

Rossen: What are we improving?  Is the guidance intended to improve the effect better structure of components could have on a11y for example?  Calendar control - would following this guidance make it easier to create ...

Lea: there are i18n concerns between these 2 attributes - when you use a child element you can include lang attribute more easily...

Rossen: if i have a soup of elements - for a11y it makes it harder...

Lea: of you use an element it allows more metadata - an attribute is more compact. That's the tension and that's why the web plartform is inconsistent. We encourage component developers to look to the web platform but the platform is inconsistent.

Peter: an attribute can't contain structure. Also a lot of thigns happened the way it did because of backwards compat.

Dan: consensus we should do something.

Peter: we should document the mistakes of the past so we don't repeat them...

Lea: web develoeprs designing html syntax don't necesarilly know that the recognized mistakes are mistakes.

Dan: let's bring this to the plenary...

Peter: input, placeholder, source for video... we can tear into those...


#### [CSS: Guidance about serialization](https://github.com/w3ctag/design-principles/issues/284) - @LeaVerou, @atanassov

Rossen: [round-tripping important]

Rossen: one of the clearl principles should be that serialization should minimise or try to eliminate rount trip error.

Lea: any conter-examples?

Rossen: e.g floating point serialization... and we have explicit places where we are undefined in terms of percision. Empty spaces are another example. Do they matter for humans? Do they matter for tools?  In some case the will be domain specific...  First principle: serialization is the output.  It's exhaust.  

Lea: a lot of good thoughts....

Rossen: **I will draft something a comment to provoke more discussion.**

Rossen: We need to agree on what the order of constituencies is here... optimising for human readability or for tools?

Lea: the more cannoinicalized the form the better the tool can parse it.  This is where we get into old guard vs. new guard.

Dan: not one size fits all maybe? (human vs tool)

Rossen: if I serialize the content out of a script element - do I PP it for you?  White space? etc...?  

Lea: I agree this is over-arching and shouldn't be CSS specific...

#### [Guidance about which state properties should be reflected as HTML attributes](https://github.com/w3ctag/design-principles/issues/289) - @LeaVerou, @plinss


#### [Inconsistent capitalisation of "web platform"](https://github.com/w3ctag/design-principles/issues/294)

Amy: did a PR #343

Dan: I think it's a good thing to do because it signifies web platform in the abstract rather than a particular definition

Lea: there's one Web Platform, it's a proper noun... but not the hill I want to die on

Dan: suggest we merge, then this issue is closed

#### [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299) - @hober

Lea: discuss with Tess

#### [Editorial: Add link to published version on /TR](https://github.com/w3ctag/design-principles/issues/318)

Yves: see [PR 337](https://github.com/w3ctag/design-principles/pull/337)

Dan: looks good, lets merge

Amy: +1

#### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
#### [New principle: Avoid introducing new parser-blocking features](https://github.com/w3ctag/design-principles/issues/329)

Lea: that did come from a design review.. no it was a whatwg discussion where people were requesting a certain feature and getting the input that it would be parser blocking therefore it should not be introduced. Wanted your opinion - are they a mistake?

Dan: what do we mean by parser blocking

Lea: when a script element is read nothing else can continue because that could be doing document.write and completely changing the document, it disables a lot of optimisations. Newer behaviours for script elements essentially imply defer even if you don't actually add the attribute

Rossen: what kind of principle are you trying to suggest that will work around this limitation? 

Lea: not that will work around this limitation. If we all agree this limitation should be followed maybe there should b ea princple about it so people don't design principles that violate it.

Dan: in the future when someone says parser blocking scripts are a design mistakes, there can be a reference to that a design principles doc. Rather than just in somebody's head.

Rossen: Jake is not wrong here

Dan: no he's not

Lea: that's the point of the principle. If he's right we should have a principle about it.

Rossen: is the principle intended to guide implementers away from adding equivalents of document.write?

Lea: not just implementers proposing new apis for the web

Rossen: this design principle is applicable to implementers as well as anyone else adding modules and scripts in their app.. isn't that the case? Trying to figure out what such a design principle would sound like. Don't expose API that are parser blocking?

Lea: do not add new syntax to html that wolud be parser blocking. I think that only applies to new html features. How else would add something that's parser blocking? Can't add a js api or any css syntax that's parser blocking?

Dan: maybe a new principle in the html section?

Lea: I think so. If we agree that it should be a principle it sholud be in the html section. I think Rossen is not sure?

Rossen: not sure if it's principle here or in whatwg.. I don't disagree with the principle

Lea: do we not add principles about html?

Dan: I don't think that's true, I think we want this doc to be seen as design guidance for anybody, for whatwg as well. Appropriate for it to be i nthis doc.

Rossen: design princples for html? Not updated for many years..

Dan: whole point of Tess's work was importing design principles for html into this. Not a land grab.. Take the wisdom of that group and bring it into this doc so it's clearly spelled out.

Rossen: wonderful effort. Just curious if there are any other .. don't know how much of this is going to go into effect once we have it

Dan: I suggest we write something and get people like anne and dominic to come in and give us their thoughts. People in whatwg community to make sure they're happy

Lea: would go as far as to say someone from that community might be the best person to prototype it. Since we're okay with inviting outside peopel tod raft principles. I don't feel I have the expertise.

Dan: I wonder if Jake might be interested. [writes comment]

### Breakout B (US / APAC) - [2021-10-05]

#### [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia
#### [New principle: Patterns for URLs in APIs](https://github.com/w3ctag/design-principles/issues/303) - @cynthia
#### [Second consistency pass for attributes/properties/methods/functions etc.](https://github.com/w3ctag/design-principles/issues/315)
#### [Guidance about exposing on Window vs Worker only (and other contexts)](https://github.com/w3ctag/design-principles/issues/325)
#### [Discourage depending on the WTF-16 nature of JavaScript strings](https://github.com/w3ctag/design-principles/issues/323)
#### [Encourage UTF-8 for new formats and APIs](https://github.com/w3ctag/design-principles/issues/322)
#### [New principle: Do NOT reuse similar attribute names for different behavior](https://github.com/w3ctag/design-principles/issues/328)
#### [New principle: Why we should not expose native object lifecycles](https://github.com/w3ctag/design-principles/issues/333)
#### [New principle: when to use permissions, when to use user activation, and what if neither are adequate](https://github.com/w3ctag/design-principles/issues/341)
#### [New principle: Support common promise practices](https://github.com/w3ctag/design-principles/issues/342)

### Breakout C (APAC / Europe) - [2021-10-05]

#### [Generate a subset of the Design Principles doc for web developers](https://github.com/w3ctag/design-principles/issues/268) - @LeaVerou
#### [Are some of the "Guidelines for web component authors" more broadly applicable Design Principles?](https://github.com/w3ctag/design-principles/issues/271) - @LeaVerou, @kenchris
#### [Generalize principle about avoiding abbreviations?](https://github.com/w3ctag/design-principles/issues/276) - @LeaVerou
#### [HTML: Guidance about lists of values in attributes](https://github.com/w3ctag/design-principles/issues/277) - @cynthia, @LeaVerou
#### [HTML: Guidance about URL-containing attributes](https://github.com/w3ctag/design-principles/issues/278) - @LeaVerou, @ylafon
#### [HTML: IDL attributes and HTML attributes should be kept in sync](https://github.com/w3ctag/design-principles/issues/279) - @LeaVerou, @kenchris

[discussed]

#### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro
#### [New principle: Ethical Principles](https://github.com/w3ctag/design-principles/issues/338)
#### [New principle: Just because you can do xyz bad thing using another API doesn't mean it's OK to design a new API tha can also to xyz bad thing](https://github.com/w3ctag/design-principles/issues/340)
#### [Ethical: Digital Human Rights](https://github.com/w3ctag/ethical-web-principles/issues/52)

Amy: [summarises thread]

Hadley: in the early days someone wanted one principle to be more important than others, or that you have to compromise one principle for another and that makes the document invalid. We responded this isn't meant to be that kind of a checklist, but these are for us to be able to reference in different conversations and inevitably as a spec author / designer / developer you're going to be at different practical implementing .. similar logic .. I don't think our intention to come up with something that is a heirarchy or an overarching principle. It's a bunch of things we've learned over our experience are useful and necessary. The web is more complex than just being able to roll it all upinto a nicely ordered set of steps

Amy: [says loads of smart stuff]

Hadley: we can leave it open and say there's not much to do right now or we can close it. I'm in favour of everything you said, doesn't sound like it'd be useful to build into the document

Amy: there are people worried about the wording in the document to block work, use EWP as a weapon

Hadley: not much we can do to stop people form using the document in this way no matter what we write in it

Yves: put an article to a [study on block chains](https://link.springer.com/article/10.1007/s12599-020-00656-x)... showing "as bad as bitcoin"...

Amy: you can find an article to support any position on this you want if you look hard enough...

Amy: leave this with me .... I will review thread and see if there's any language we can add to make use of the principles clearer that will make people in the thread happier



#### [Ethical: Dark Paterns](https://github.com/w3ctag/ethical-web-principles/issues/25)

Amy: the PR is done in the way that tantek approved.  Lea added a comment that Dark Patterns is not prefered term...

Lea: has been raised on a mailing list at work...

Yves: we could raise an issue to show we care about this issue.

Hadley: I like this approach.

Lea: I agree - and we should do some research...

Hadley: a quick search yields 1 result discusses the term being potentially racist and exclusionary... One anectotal result.

Dan: So I think use of it in the way we are using it - and linking to the wikipedia article - are OK for now and we can open an issue to discuss... Feels like we are not amplifying the issue but rather acknowledging its use as a term of art.  Feels more helpful than harmful.

Amy: yep.

Dan: So I think we should merge the PR... 

Amy: Also conversation on federated vs decentralized...  I will open a new issue.

Hadley: re-decentralized movemenent is doing good things we don't want to alienate them either.. 

#### [Ethical: Abuse](https://github.com/w3ctag/ethical-web-principles/issues/44)

Dan: I can write something... Will have a think about it...

Hadley: this connects to the issue - the design review for enterprises controlling devices...   [Managed device API](https://github.com/w3ctag/design-reviews/issues/606)...

Dan: Yes - will channel that.

#### [Ethical: Less Hedging](https://github.com/w3ctag/ethical-web-principles/issues/51)

Hadley: we should go back to Olu and ask them for specific thoughts / specific areas that would benefit from attention?

Dan: Agreed - 

Hadley: Will leave comment...  Agreed we should do a pass through the text to strengthen the language.

Amy: +1

Dan: trying to channel Olu's feedback.. things like "should not cause harms to society.. *consider* what harm".. that could be seen as an example of hedging language. Rather than considering, we could say we will will *prioritise*, that' sthe kind of stuff that came to mind. Where in here are we using language that's a bit like "sort of, talk about.."

Hadley: our current practice is to ask people who come ot use for spec review to not just considerations but also think about mitigations.. be nice to take it to that next step so not only the TAG can act on it but also spec authors and designers

Dan: To encourage .. we can't make people do anything.. we can encourage them to think about these issues at the same level of whatever requirements they're building their new tech towards

Amy: creeps into the design principles - since it's actionable rather than high level. I'd like to see a dystopia advoidance questionnaire - a social and ethical considerations questionnaire - which would ecourage thinking about mitigations...

Dan: we could mention mitigations in the principles here and then say look to the design principles for specific design advice, look to the security and privacy questionnaire, the things that currently exist. People should be thinking about mitigations not after only reading this document

Amy: I can do a pass to look at the language.

#### [PR 47](https://github.com/w3ctag/ethical-web-principles/pull/47) on environmental

[we agree to squash and merge]

**MERGED**

#### [PR 49](https://github.com/w3ctag/ethical-web-principles/pull/49) 

[some more work to do we will merge it at the plenary]

#### [UN Human Rights Link](https://github.com/w3ctag/ethical-web-principles/pull/53)

[discussion on the difference between digital human rights and human rights]

Dan: adding this link is separate from the discussion on digital human rights.

Amy: Agreed.

[general agreement]

**MERGED**

### Plenary Session - [2021-10-06](https://www.timeanddate.com/worldclock/converter.html?iso=20211006T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### [New principle: Discourage language sniffing for language-specific features](https://github.com/w3ctag/design-principles/issues/266) - @cynthia

Rossen: discussion in css text level 3... it's what sparked this... i don't think we can discuss this one just on the fly without the details and the background of it... 

#### [Second consistency pass for attributes/properties/methods/functions etc.](https://github.com/w3ctag/design-principles/issues/315)

Sangwhan: this is actionable.  

[added to project]

#### [Discourage depending on the WTF-16 nature of JavaScript strings](https://github.com/w3ctag/design-principles/issues/323)

Dan: Dom opened it in June - we haven't had any engagement...

Peter: it looks like this tide is turning in whatwg..   I've been of the opinion that new APIs should use USVstring - there's a cost however - a dom string - you have to run a test - i accept there's a cost. but idelaly everything is just usvstrings and throw away the domstring legacy behaviour.  As opposed to carrying on domstring in perpituity.

Sangwhan: I think it makes sense for santization where we don't have guarantees - e.g. from webassembly.

Peter: I accept we may need to carry it around in DOM but do we need it in APIs that don't interact with the DOM?

Dan: doesn't sound like 'low hanging fruit'.. what should we do?

Peter: we should try not to rely on domstring behaviour.. kind of a hybrid approach.. 

Dan: that paves the way for the world you envision?

Peter: if that's what he's proposing then I agree, it's worth doing

Dan: if we want to aim the platform towards universal use of usv strings it's worth saying that? Rather than saying you should design this way, say "because we want to try to move towards this.."

Ken: sounds like better approach

Peter: he is proposing an extra bullet point on guidance on strings:

```
Avoid dealing with the string's code units. This is only appropriate when doing developer-driven indexing, length, or substring operations, like CharacterData does or like the native JS string methods such as substring() do.
```

Peter: the argument against is performance...  Increased use will create incentive to make it fasrer?

Tess: seems like a gamble.

Peter: would like signals from JS engineers.

Dan: I don't understand if Peter's statement is in support of or not insupport of adding this bullet from Dom

Peter: in support

Ken: just do it then

Sangwhan: likewise

Tess: yeah

Peter: doesn't hurt

Dan: puts it in the projects board

#### [Simple things should be easy, complex things should be possible](https://github.com/w3ctag/design-principles/issues/299) - @hober

Tess: need to incorporate the feedback on the PR...

#### [EWP subheadings PR](https://github.com/w3ctag/ethical-web-principles/pull/49) 

[merged]

#### [not dark patterns PR](https://github.com/w3ctag/ethical-web-principles/pull/55)

[merged and issue 25 closed]


#### [Principle(s) about identity on the Web?](https://github.com/w3ctag/design-principles/issues/324) - @torgo, @rhiaro

Tess: active area of discussion and we shouldn't weigh in.

Hadley: I agree - we don't crown winners.

Sangwhan: i try to avoid referencing things that are not agreed standards - one of the things we didn't put in was bigints or temporarls for instance - because there were competing proposals. We shouldn't put anything like that into the principles doc.

Dan: So shall we close this and say the TAG consensus is to not write something on this?

Amy: there are a bunch of community groups and working groups we could close it with links to those things...

Sangwhan: we should try to keep the principles doc terse and with actionable advice.

Amy: [will write that as a closing comment]

#### [Don't pee in the pool](https://github.com/w3ctag/design-principles/issues/340)

Dan: we see this a lot when we do reviews.. came up in clipboard..

Tess: people do this with fingerprinting too

Dan: webxr raw camera access recently.. is this something we could put into an actionalbe principle?

Sangwhan: yes. Section 1. With put user needs first etc, fits there.

Hadley: definitely something we talk about a lot.

Dan: is there a term that we could use for a negative thing that is not necessarily a privacy risk but a security/privacy/risk factor for web users?

Dan: I can put my name to it...

Amy: me too

#### Gardening

Sangwhan: 314, 144 and 341 are all related

Tess: close two ofthose as dups?

Sangwhan: open a new issue that captures all and close all 3? They have different intents.

Dan: I don't agree they're the same, specific to concept of user activation.. requires user activation seems to be used as justification for not requiring permission or osmething like that. We don't talk about user activation in the design principles. I don't know whether it's the same as the meta issue 341 and the harmonize permissions, that's a project which we can only participate in, this is not actionable within the design principles.

Sangwhan: there's a bunch of discussion in that issue that should be referenced, some important points. the part about permissions and user activation is that there has been some concerns raised about too many permissions, which I partially agree with, also average user pressing yes to everything

Dan: active discussion in raw camera access api.  We knwo of permission fatigue. Doesn't mean permissions are useless, just we need to not overburden. It can only ever be a mitigation. In the case of raw camera access api we need to push back and ask what else they can do besides permissions, design to be privacy perserving from the beginning. For other ones they might say user activation is one of the mitigation steps.  Talk about permissions fatigue in the principles?

Sangwhan: we don't bring up permissions adequately

Dan: might be something in the privacy principles doc..

* Breakout Rollup
* Issue Triage

