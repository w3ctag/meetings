### W3C TAG Call Agenda / w/o 7 June 2021

NB: This is a [design principles](https://w3ctag.github.io/design-principles/) week. 

This agenda can be viewed and updated on [Github](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/06-07-agenda.md).

If you would like to add an item to the agenda or volunteer to scribe please open a pull request against this agenda.

### Breakout A (Europe / US) - [2021-06-07](https://www.timeanddate.com/worldclock/converter.html?iso=20210607T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [New principle: When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - @hober, @torgo
* [New principle: Guidance on User Activation](https://github.com/w3ctag/design-principles/issues/314)
* PR [Add some text for factory methods vs constructors (resolves #44)](https://github.com/w3ctag/design-principles/pull/321)
* PR [Add a new principle for crypto.](https://github.com/w3ctag/design-principles/pull/310)
* [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286)
* [New principle: New features must not break existing ones](https://github.com/w3ctag/design-principles/issues/297)
* PR [Add text for low-level vs high-level APIs (related to #117)](https://github.com/w3ctag/design-principles/pull/291)


### Breakout B (US / APAC) - [2021-06-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210608T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* PR [Two new principles (actually one existing one recycled) for devices.](https://github.com/w3ctag/design-principles/pull/320)
* [Several core architectural features of the Web Platform may allow heuristic detectability of assistive technology](https://github.com/w3ctag/design-principles/issues/293)
* [Guidance for when to use inheritance vs composition](https://github.com/w3ctag/design-principles/issues/298)
* [Principle against tying APIs too closely to hardware](https://github.com/w3ctag/design-principles/issues/308)

### Breakout C (APAC / Europe) - [2021-06-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210608T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [Identity of identification identifiers](https://lists.w3.org/Archives/Public/www-tag/2021Jun/0000.html)
* PR [Add consistency section, closes #285](https://github.com/w3ctag/design-principles/pull/313)
* PR [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306)
* Ethical Principles PR from Marcos: [Refactor: use markdown](https://github.com/w3ctag/ethical-web-principles/pull/41)
* [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - is this redundant to #313?
* [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281)
* [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282)

### Plenary Session - [2021-06-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210609T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

* [again with the access to the clipboard](https://github.com/w3ctag/design-reviews/issues/636#issuecomment-853319479)
* [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
* Triage: [Discourage depending on the WTF-16 nature of JavaScript strings](https://github.com/w3ctag/design-principles/issues/323), [Encourage UTF-8 for new formats and APIs](https://github.com/w3ctag/design-principles/issues/322)
* Possible new joint work with Privacy Interest Group
* Triage [new issues](https://github.com/w3ctag/security-questionnaire/issues) on security & privacy document?

* Breakout Rollup
* Issue Triage


## Minutes

### Breakout A (Europe / US) - [2021-06-07](https://www.timeanddate.com/worldclock/converter.html?iso=20210607T160000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### [New principle: When to use client hints](https://github.com/w3ctag/design-principles/issues/307) - @hober, @torgo

Ken: francois talked to yoav and they want a meeting

Dan: yoav left a question for me in particular.. came out of client hints reliability mechanism. [writing reply]

Yves: think of people disabling client hints for privacy purposes and have that affect what you get. Don't want figuring out client hints disabled and get served something different.

Dan: should reach out to yoav for a breakout? Breakout A. [emailed]

#### [New principle: Guidance on User Activation](https://github.com/w3ctag/design-principles/issues/314)

Dan: asked for in discussion on webid. Anne has linked to where user activation is defined.

Tess: a principle of what sorts of things should be behind a user gesture description maybe belongs more in a PING document? Eg. they have a fingerprinting document that includes tons of info about mitigations that different spec authors could do. Maybe the permissions api or a PING doc is something where "you have a powerful feature, here are the mitigations to avoid abuse". Maybe that is ours?

Dan: we should have at least a couple of sentences. Not unreasonable for someone tos earch design design principles for 'activation'. Weird it's not there. We could say "if your api has potential to infringe peoples' privacy decide whether or not user activation would be wise. See here for the definition of user activation, here for more detail, visit security & privacy self check.."

Tess: important in a summary to convey that gating something on user activation is only one mechanism, not always the one, not a pancea. Can't say it's powerful, just put it behind a user gesture and not think about anything else. That needs to be in the summary, then there can be a reference. Follup is to figure out where that should be fleshed out to encourage people to do that.

Dan: came up as well in the discussion on [clipboard access discussion](https://github.com/w3ctag/design-reviews/issues/636#issuecomment-853319479)

Tess: general user activation is not what you want there. An explicit paste command... ctrl+v, clicking paste.. you don't want access to paste board by user tapping on the screen somewhere. 

Dan: they were talking about 3 different levels, one behind a permission, one was user activation, third that it had to be the active tab. You couldn't just have you have interacted with this webpage but it's sitting in the background and has a permission but still cant' snoop because it's in the background

Tess: all good examples. Their case may be unique but a case where general user activation even with other mitigations isn't enough, a restricted form of user activation, certain kinds and not others. which as far as I know isn't spec'd anywhere. User actiation in html should be expanded - I'll file an issue.

Dan: give this a writeme and assign to me. Somebody else can jump in.

Tess: please add me.



#### PR [Add some text for factory methods vs constructors (resolves #44)](https://github.com/w3ctag/design-principles/pull/321)

Dan: [Sangwhan said](https://github.com/w3ctag/design-principles/pull/321/files#r640568069) we should solicit group consensus

Lea: it's okay to have factory vs constructor when they can produce any subclasses (??) ... but why is it on document? these factory methods are usuallys tatic methods on the class. In this case it's on the document instance. Is that a good thing? or would it have been element.create if it was designed today?

Tess: when yu create an element you're usally trying to attach it to a document so it makes sense to attach it to a document at construction time, but I don't think that actually holds much water

Lea: if it was element.create you could pass the document as a parameter. If you  need to associate an object with another object is it okay to put the factory method on that object as a pattern?

Ken : if I'm a developer I look at [...factory...] so many methods...

Tess: suppose the DOM added a new thing.. not an element, a molecule. For consistency with everything else, it would be the right thing to do the factory method off the document object even though we all agree its weird. would be weirder to have one thing not like that

Lea: we did have the document.init methods that we got rid of in favour of constructors. If in the future you could create elements not attached to a document you'd need a new method. Entire element creation method is designed around the fact it needs to be attached to a document

Tess: you'd expect a constructor in that case

Lea: if you had different subclasses you'd want a factory method for convenience. Nice to provide the tag and get the right subclass back, still need a factory

Dan: worried about having the text that says "if it were designed today". It's a bit speculative.

Tess: the CSS WG maintains a document of mistakes basically.. things they wish they had done differently but we're stuck with. That's a useful document, in particular for new participants in CSS WG who might want to bring something up that we've talked about before and all want it but we can't have nice things. There is value in documenting why we can't have nice things. That seems more negative than positive. Maybe separate?

Dan: doesn't belong in design prinnciples where people are looking for affirmative guidence. I'd suggest dropping that clause.

Lea: using a different exmaple or dropping the part about maybe?

Dan: dropping that bit.

Lea: if anyone has a positive examples of a factory method that is popuplar that people are likely to be familiar with? Otherwise I'll just drop that sentence

Rossen: do we have something similar.. graveyard examples for html?

Tess: whatwg faq might have some but don't remember. Would be useful

Dan: if Lea does that change [take out from "if this were today..."] we can agree to land this?

Rossen: Makes sense.

[consensus to do so]

#### PR [Add a new principle for crypto.](https://github.com/w3ctag/design-principles/pull/310)

Hadley: feedback from ryan sleevi. Web crypto is not hallmark of good design. Arguing for baking in algorithms to specs. Does avoid any ambiguity. I see the argument. Doesn't solve the problem we were concerned about which is that algorithsm move faster than specs

TesS: in particular [the specific concern regarding this issue] 

Hadley: worth bringing ryan in for discussion?

Tess: probably is. If we can explain the nuance it would be helpful.

Dan: we will revisit in plenary and ask Sangwhan

#### PR [Add text for low-level vs high-level APIs (related to #117)](https://github.com/w3ctag/design-principles/pull/291)

Lea: Rossen left comments and i wondered if this should be merged with 306 which is the same but clearer

Tess: I don't think that's the case, 306 is trying to say when in doubt pick the simplest. This is about layering and how to ifnd the layers to expose

Lea: 306 is about making common things easy and complex thing spossible so it is about layering

Tess: i think they're distinct but might affect the same text

Rossen: you can achieve simplicity through layering but it's not necessarily the only way to do it

Lea: should 306 be merged into this? or separate things?

Tess: separate

Dan: separate, 306 is more high level...

Tess: the jokes write themselves

Dan: it fits more into the safe to browse section rather than being specific advice. Not in the same area, but that it should be in section 1, along with priority of constiutencies etc. Rossen left feedback on 291 - are you okay if we decide to merge this?

Rossen: has it been addressed? I don't think so

Lea: Rossen's comments have not been addressed, I wasn't sure how to address them

Rossen: can sort it out together. Impression was we need to get crisper on the guidence and how it lands.

Lea: wasn't sure about the second comment - I find myself rewording the text and it starts sounding a lot like 306. But they should be separate so reword differently. Sounds to me like they're very similar. Sounds to other people like they're not.

Dan: isn't the guidance more nuanced than what Rossen is saying? Not just start by expsing the highest level possible. Think about the highest level problem.. be mor ethoughtful about what you're exposing at a high level when you're building the primitives?

Rossen: right but the guidence was to start at that high altitude rather than walk through all of the details underneath becuase details will change as you go because usage, adoption, new ideas emerge as people use, etc. If you don't start at a high level you're losing the chance to probe and learn and adapt to where the extensibility needs to be added. Where you think it needs to be added today may not be the same as tomorrow. When I read Lea's text - great text - if we were to flip the order of examples I think it'll land the way we thought about it. Instead of starting at low level, talk about starting at high level as a well layered solution and build any lower level apis as needed. And leave it at that. Will take wordsmithing but not too far off, just haven't had a chance to write the proposed changed.  We can have a tentative group resolution to merge it when we're fine with it.

Dan: be great to land it at plenary

#### [Guidance about return values of (conceptually) void functions](https://github.com/w3ctag/design-principles/issues/286)

Tess: that was a good conversation.

Lea: consensus was they should return undefined because that allows u s to add return values in the future. No PR.

Dan: last commented on by dominic 12th feb

Tess: I can take action to write PR

#### [New principle: New features must not break existing ones](https://github.com/w3ctag/design-principles/issues/297)

Rossen: that's right, they shouldn't.

Tess: just don't break the web? Not just new features, changing behaviour of existing features.. the web doesn't change, it grows. Long tail of webpages mostly don't change and we have to keep working with them. When you make changes you need to be cognizant of how things actually work in the wild. That's the compatibility that we care about. Not about what the spec used to say vs what the spec says now

Rossen: I like the philosphical explanation. The direct use case here is that when there was an explicit "we're going to break this but it's okay because to a certain extent the benefit of the new thing outweighs the breakage of the other one"... eg. accessibility related capabilities. We're going to break accessibility, give you stuff that's not supposed to be there, they're saying it's less good for accessibiliity needs but this great benefit of everybody else who can scroll much faster or something of that nature. That is where we need an explicit principle that says just becuase you want to have your hot sauce thing right now doesn't mean you have to break other constituiences or go against things that are working well today. That was the reason I wanted this more explicit one. On its own or fold it into something else and make it more strong? 

Tess: couldn't agree more

Dan: we don't have anything on not breaking the web in the design principles

Tess: text on this in old html design principles. Already on my todo list to port that over. Rossen is right there's a difference between general don't break the web and specific thing that is more nuanced. 

Rossen: remaining is just to write the text

Dan: [writes comment]

Rossen: both - don't break web, and don't break existing

Tess: issue 174

Dan: close this issue?

Tess: two PRs... one general from 174.. maybe not? the text Rossen wants from thsi one will probably end up in the same section

Dan: I think it's sthe same, stronger rewording of html design principle with a slug of dont-break-the-web

Tess: 174 could land and this could be done after, or all at once

Rossen: figure it offline. Linked both. Added writeme.

### Breakout B (US / APAC) - [2021-06-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210608T010000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### PR [Two new principles (actually one existing one recycled) for devices.](https://github.com/w3ctag/design-principles/pull/320)
#### [Several core architectural features of the Web Platform may allow heuristic detectability of assistive technology](https://github.com/w3ctag/design-principles/issues/293)
#### [Guidance for when to use inheritance vs composition](https://github.com/w3ctag/design-principles/issues/298)
#### [Principle against tying APIs too closely to hardware](https://github.com/w3ctag/design-principles/issues/308)

### Breakout C (APAC / Europe) - [2021-06-08](https://www.timeanddate.com/worldclock/converter.html?iso=20210608T080000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

#### [Identity of identification identifiers](https://lists.w3.org/Archives/Public/www-tag/2021Jun/0000.html)

Dan: we had a post to our mailing list. Some discussion. Occurred to me we were approached by google about WebID as well, they had a workshop, multi year process to bring federated id into browser, possibly opening a CG around that. Is there something the TAG should say that would be relevant to both communities?

Amy: lots of people saying something about identity - might be good for TAG to have an opinion - it's a huge space - at the same time it's really developing.  I wonder if there's something very small that could go in the design principles about it? 

Dan: I like the idea of doing something small. A TAG finding like the ethical principles? A set of short principles. Something we could do that is small that other people can build on. Either in design principles or as a finding...

Amy: maybe.  Quite a daunting topic.   Doing something short and simple - we could be criticized for oversimplifying.  We could make a point that this is really complex and messy - as one of the principles.

Amy: will start to think about it... inclination is to see if we can put it in the design principles...

#### PR [Add consistency section, closes #285](https://github.com/w3ctag/design-principles/pull/313)

[discussion on examples]

Lea: we need more examples of the kinds not covered.

Dan: I take the point that example on colours is something from an outside domain, however I feel like we could use one other example

Lea: the more the merrier

Dan: propose to merge the PR and keep the 

[merged and noted and #285 assigned to next design principles week]

#### PR [Incorporate Alan Kay's maxim into 'Prefer simple solutions'.](https://github.com/w3ctag/design-principles/pull/306)

Dan: in breakout A we talked about whether this should be merged with simple things should be easy and decided not

Lea: last time I looked at this we discussed with Tess and she said she'd work on it some more. Left some comments. Difference between simple things and common things. Simple are not always commmon and vice versa. Sanitizer is a good example.

Dan: what are we trying to say? is it useful or an academic exercise / philosophical question?

Yves: e.g. security knobs added to the web platform - difficult for authors to understand and to use.. lacking simple understanding / simple API to to multiple things at once.

Lea: prehaps things that are simple to conceptualize...  Worried that if we phrase it as simple things should be easy then API designers could make simnple things easy even if they're not useful.

Yves: objective is to make sure that APIs are not misused.  So make it simple - simple to understand so you know what it should do - but implementation might be complex.

Lea: about designing APIs...  APIs should serve their main use cases easily. APIs should be sufficiently flexible to serve rare cases but it's ok if devs need to do a bit more work. Should be flexible to serve the complex cases but OK if the author needs to do more work.

Dan: something like common cases

Lea: or main use cases

Dan: can you reword pr based on that? plenary?

#### Ethical Principles PR from Marcos: [Refactor: use markdown](https://github.com/w3ctag/ethical-web-principles/pull/41)

Dan: I'm okay either way. Interested in why Marcos raised this? Easier to maintain as part of W3C specs, or easier to maintain just this doc? Impact on other documents? [writes comment]

#### [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - is this redundant to #313?

Lea: Dan added a comment but I don't see how it would be redundant more than any other naming guidence. Isn't every naming guidence about consistency?

Dan: yeah you're right

Lea: remember discussing...

Dan: we had a whole big list of [events in f2f minutes](https://github.com/w3ctag/meetings/blob/gh-pages/2021/05-Arakeen/minutes.md#event-naming)

Lea: we should link to that. We started discussing because it would be simple.... but ended up a huge can of worms.

Dan: result of [twitter poll](https://mobile.twitter.com/LeaVerou/status/1392403095234228231)?

Lea: don't remember any patterns we hadn't found.... comment about verbs vs nouns.. if they are nouns, changes discussion about past/present tense. List is misleading because it weighs all event names the same. They shouldn't. Some events should be weighed more - more popular ones.

Dan: how do we priortise this list?

Lea: vague thoughts about using http archive to see which event names are more popular. They added a custom metric, I can check on status. Takes a month to get results.

Dan: yes, need more data

#### [HTML: Re-use existing attribute names for similar concepts](https://github.com/w3ctag/design-principles/issues/281)

Dan: is this something we know enough about to write a PR?

Lea: I could take a stab at it

Dan: [agenda for next design principles week]

[meta discussion about issue labelling for assignees -> plenary]

#### [Link with Ethical Web Principles](https://github.com/w3ctag/design-principles/issues/282)

[bumped to next design principles week]

Amy: May get something done this week.

### Plenary Session - [2021-06-09](https://www.timeanddate.com/worldclock/converter.html?iso=20210609T150000&p1=224&p2=43&p3=136&p4=195&p5=26&p6=248&p7=240)

Present: Tess, Peter, Hadley, Yves, Dan, Lea, Amy, Rossen

Regrets: Sangwhan, Kenneth

#### f2f dates

[Proposing week-of 13th of Sept]

#### [again with the access to the clipboard](https://github.com/w3ctag/design-reviews/issues/636#issuecomment-853319479)

Dan: discussion about other issues on previous clipboard APIs on privacy and user gesture. Question I still have is the statement from ?? seems to be that the discussion to mitigate against random sites accessing clipboard content users need to user permissions api, and a 'sticky' user activation requirement..

Tess: once the page gets a sticky user activation gesture it retains it so in the future when the user activation check happens it checks if it ever happened. Transient means at the time of the check it has to have one. I don't think that's good enough here. It does not define the nature of the user gesture that is causing the user activation to be the case. Just tapping on a page is not sufficient - what we wanted is for the user to have explicitly done something which maybe OS depending, that is explicitly a paste gesture. That might be cmd+v or tapping in a textarea on a mobile device and picking paste from the pill menu. It would actually be a paste. Tapping on the page for some other reason, like as a prelude to scrolling the page isn't sufficient for the user to say the page can know about the pasteboard. 

Dan: Would changing it to transient fix the issue?

Tess: no. I don't believe user activation stuff in HTML spec contains a notion of a restricted form of user activation that carries some kind of intent. If they want to add this feature to the web they have to add that too.

Hadley: they were talking about the permissions API?

Tess: that's an upfront prompt

Hadley: what they've pointed to in the html spec is the kind of activation that means that... to prevent abuse of certain apis that could be annoying... allowed when user interacted with page at least once. Possible that sticky activation could  happen for a site in the background?

Tess: I don't remember

Dan: eric is saying it nees to be active tab, they've taken that into account. STill feel like you could imagine a situation where you're phised to a site pretending to be your bank, it games your permission activation, it's the active tab and your user gesture has been satisified because through a dark pattern it tricks you into clicking the permission prompt, then it has access to your clipboard

Tess: it would take two tabs. Agreeing to the permission prompt doesn't provide user activation to the page. But there are a number of ways to induce you to tap on the page after you've accepted the permission. It's not clear to me that browsers would have an explicit permisson prompt here. If you look at existing platforms and the paste behaviour my understanding is that browsers have the freedom to always grant or always deny without bugging the user about it.. They put it behind permission api but that doesn't tell us if the user has explicitly agreed to anything. The only explicit signal from the user that they want to share the contents of the pasteboard is when they do a paste command - that's the vital thing. THe browser has to know they intend to paste. Pulling up edit and clicking paste, or pressing paste keyboard shortcut, or equivalent touch gesture

Hadley: why do we need a web api if those things are already in the OS?

Tess: there might not be a focusable field on the page in which you'r epasting. CUrrently  if you focus an input type text and you pick paste the page doesn't get to know that was from yoru clipboard, it's just a new value for the input.

Dan: pasting pickled graphics formats onto a blank canvas you're not pasting text into a text field, it's complex into an application

Tess: exactly. No affordance for that. The page has to ask for the contents of the pasteboard. Common case is taken care of already.

Dan: when they say performance issue, they want that active tab to be able to start uploading a large piece of graphic ot the destination site... I dunno.. .maybe a way for these large things to be held in some kind of escrow buffer until there's an affirmative activation by the user?

`Replaying [our discussion](https://github.com/w3ctag/meetings/blob/gh-pages/2021/telcons/06-07-agenda.md) in today's TAG plenary call where we discussed this issue. The TAG consensus is that the mitigation described - permission, sticky activation, active document - is not sufficient.  This is because it still could lead to unintentional leakage of the information held in the user's clipboard.  We don't believe that the user activation as specified contains a notion of a restricted form of activation that carries some kind of intent (a specific intent to paste content). And if this feature should be added to the web, then that kind of activation feature (with intention) should also be added.  

One scenario is:  you're phished to a page that looks like your bank's web site. that page induces you to agree to the permission through a dark pattern (and also induces some additional interaction in the same way), and then (without an explicit paste command) the web page in question has access to the contents of your clipboard.  

Another scenario: you're on a legitimate site and you explicitly paste something into a page which has permission to access your clipboard. Now you go off and copy something else (say a password) into your clipboard which is unrelated to your interaction with this site.  And bring the browser window back up.  Assuming this site is the active tab, this site would have access to your sensitive information on the clipboard.

We understand the performance issue that's been articulated. Is there another way to address this issue that can afford the user the protection we think they need here.`

Rossen: is your scenario that if I activate access to clipboard from site A, however I obtained the access to the clipboard, I'll be able to have acces to everything on the clipboard from what was put there by site B?

Dan: or by anything.. say you have a password copied from somewhere else, or a URL to a private document. Site A would have access to that information without you having used an explicit user activation.

Hadley: the user action doesn't necessarily means the user understands or thinks they're making happen whath is happening

Tess: only certain user gestures mean I'm trying to paste something

Rossen: the edit command is activate by something - gesture,  keyboard, something else - is the trigger. Not necessarily ..

Dan: yes, but they're saying that that wouldn't be the case. Site A would have access to clipboard simply by you having clicked anywhere on the page after you have given permission. You've accepted the permission prompt, the tab is active, and you'v eclicked somewhere on the page. Doesn't need to be explicitly I want to paste a thing. Simply 'click okay to prove you're not a robot'. Now all the conditions are met for that site to have access to the contents of your clipboard. Tess is saying no, the user needs to explicitly say I want to paste. 

Hadley: another scenario - you go to a site that is operating in good faith, you give it permission, you paste in whatever you intended to paste, then go off and do something else including copying in other sensitive information, then go back to that site. Then that site has access to the stuff you've copied in for something else, because it's sticky. That's not what a user would expect.

Amy: what if you've changed your mind after you've given permission? You go to the site and accept the permission because maybe you want to paste, do some other stuff on the site (interactions), and don't end up pasting. It would still have access to the clipboard then. 

#### [[Meta] Tackling design problems earlier than design review / A Q&A section for API design](https://github.com/w3ctag/design-principles/issues/319)
#### Triage: [Discourage depending on the WTF-16 nature of JavaScript strings](https://github.com/w3ctag/design-principles/issues/323), [Encourage UTF-8 for new formats and APIs](https://github.com/w3ctag/design-principles/issues/322)
#### Possible new joint work with Privacy Interest Group
#### Triage [new issues](https://github.com/w3ctag/security-questionnaire/issues) on security & privacy document?

#### Breakout Rollup

##### Breakout A

Dan: wanted to talk to sangwhan about PR 310

Lea: 291, comment by rossen, who will help

##### Breakout B

no spoon

##### Breakout C

Dan: PR 285 merged

Lea: we need more examples for this section, linked issue is still open - ideas please

Dan: PR 306 .. talked about nuance between simple things easy and common cases easy

Tess: PR captures one of those, I think it should capture both

Dan: more work on this. Don't have to wait until design principles week.

... PR from Marcos on ethical web principles to change to markdown.

Yves: as long as respec can produce the same html it's fine, up to the editors to decide if they want to author markdown or have more control and edit html

Dan: marcos clarified by saying he only changed to markdown not content

Hadley: not clear what marcos wants to accomplish

Dan: says its more maintainable. Leaning towards accepting and merging it. He's responsible for how this doc fits into workflow, probably why he's asking us to do this.

Hadley: still don't understand enough about why this is different, but he's clearly made a big effort. I don't see a problem.

Tess: entirely a question of editor preference. 

Dan: does make the front matter more simple to read.

Peter: makes diffs easier, and makes it easier for other people to contribute. Bikeshed and respec have tools for doing autolinking to other specs, which are kept up to date.

Hadley: markdown isn't a w3c standard

Tess: not a question of conforming to markdown standard, respec has a feature where it can process markdown looking stuff.

[syntax bikeshedding discussion]

Dan: merged.



#### PR [Two new principles (actually one existing one recycled) for devices.](https://github.com/w3ctag/design-principles/pull/320)

Lea: Sangwhan worked on it, seems fine to me

Dan: people need to review

* Issue Triage

#### [Guidance for naming events](https://github.com/w3ctag/design-principles/issues/280) - is this redundant to #313?

Lea: guidence for naming events PR 280 - http archive guys added a custom metric - they'll have results at the end of june.
Lea - 

